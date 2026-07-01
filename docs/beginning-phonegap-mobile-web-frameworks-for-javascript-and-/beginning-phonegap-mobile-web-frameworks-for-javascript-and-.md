# PhoneGap 入门指南：面向 JavaScript 和 HTML5 的移动 Web 框架

为方便读者，Apress将部分前言材料置于索引之后。请使用“书签”和“快速目录”链接访问。


## 引言

### 目标读者

本书适合任何希望跨多个移动平台开始移动应用开发的读者。本书对PhoneGap进行了介绍和详细讲解，并帮助读者：

1.  识别最适合自己的JavaScript UI框架
2.  介绍JavaScript UI框架及其与PhoneGap的集成
3.  解释插件的概念以及如何使用它进行OAuth身份验证和云端推送
4.  解释如何编写自定义插件

### 本书结构

本书首先解释了移动操作系统世界的碎片化现象及其影响。进而讨论了如何弥合这种碎片化带来的差距，以及如何编写一次代码即可跨移动平台部署。

在阐明PhoneGap背后的概念后，本书接着解释了如何在Android上使用PhoneGap，然后介绍了如何在其他移动平台上进行同样的操作。

接下来，本书介绍了如何在PhoneGap之上使用JavaScript UI框架，并讨论了在何种场景下使用哪种JavaScript UI框架。

最后，本书将焦点转向插件。它展示了如何使用社区插件扩展PhoneGap框架的几个示例。然后解释了如何在iOS、Android和BlackBerry上构建这些插件。

### 代码下载

本书中提及的所有源代码均可在 https://bitbucket.org/rohitghatol/apress-phonegap 获取。各章节中会说明此信息。代码也可在Apress网站Apress.com上获取。

### 联系作者

可通过LinkedIn个人资料联系作者：
Rohit Ghatol—http://in.linkedin.com/in/rohitghatol
Yogesh Patel—www.linkedin.com/profile/view?id=19911394

## 第1章

## 理解跨平台移动应用开发

本书是关于移动应用开发的；更具体地说，是关于如何减轻移动应用开发的痛苦。市场上有许多智能手机平台：Android、iPhone、BlackBerry、Nokia、Windows 7 Phone和WebOS。新的平台也在兴起，例如三星的Bada和Meego。

移动应用的开发平台数量之多可能令人望而生畏。这是处理移动应用开发时必须牢记的众多要点中的第一点。

在2000年，我们在桌面世界看到了类似的情况。我们拥有Microsoft Windows、苹果的Mac以及各种版本的Linux和UNIX。当时，很难构建能在所有这些平台上运行的产品。由此产生的碎片化通常通过内部解决方案来解决，即用C++构建框架，并抽象出特定于操作系统（OS）的模块。幸运的是，Sun的Java拯救了我们，提供了一个共同的构建平台。凭借Java“编写一次，到处运行”的策略，构建桌面产品变得轻而易举。

在2004年至2008年间，开发社区看到了另一种不同的碎片化；这次发生在浏览器世界。它涉及当时非常流行的Internet Explorer 6与Firefox和Safari的对比——随后，Chrome和其他浏览器纷纷出现，导致了进一步的碎片化。

然而，这种碎片化的性质有所不同，也更为温和：它主要是由于浏览器没有遵循万维网联盟（W3C）制定的规范。通常，这种碎片化通过编写“如果是IE浏览器，就执行这个，否则执行那个”或“如果某个功能存在，就执行这个，否则执行那个”来解决。

许多JavaScript库应运而生，帮助编写跨浏览器的Web应用程序。情况已经改善到所有浏览器都在努力更严格地遵守W3C规范。浏览器作为一个平台，如今已成为一个强有力的竞争者。

本书关注的是移动世界中的碎片化。移动操作系统碎片化非常严重，因为该开发领域缺乏规范或标准。

2007年，苹果和谷歌推出了各自的移动平台。2008年，两家公司都推出了移动应用商店，允许智能手机用户下载移动应用程序。移动应用时代从此开启；自那时起，便一发不可收拾。智能手机用户数量呈指数级增长。

公司开始专注于在新的智能手机平台上提供服务和内容。企业意识到他们需要将重心转向智能手机用户。不仅用户数量增加，智能手机的使用频率也提高了。

想象一下，你的开发者夜以继日地工作，以便在iPhone、Android、BlackBerry、WebOS和Symbian上发布相同的产品——现在，让我们把三星Bada也加到那个列表里！你可以看到这里的挑战。操作系统平台，从其开发环境开始，就如此碎片化。对于iPhone，你需要Mac机器；对于BlackBerry，你需要Windows。本章将更详细地讨论这些内容。

现在，对于那些刚开始接触移动应用开发的读者，我们将首先关注创建移动应用是什么样的。我们将回答诸如“移动应用与传统的基于Web或基于桌面的应用有何不同？”之类的问题。我们将探讨为各种平台开发移动应用所面临的挑战。

### 移动应用的类型

理解不同类型的移动应用很重要。我将根据它们的功能将其分为两类。

1.  独立移动应用
2.  移动应用（基于Web服务）

独立移动应用是指闹钟、电话拨号器和离线游戏等应用。基于Web服务的移动应用则是指电子邮件、日历、Twitter客户端、在线游戏以及与Web服务交互的应用。

这种对移动应用的区分是本书背景下的独特之处。尽管PhoneGap可以用来实现独立移动应用，但基于PhoneGap的移动应用的性质通常属于“服务支持的移动应用”类别。



## 理解 Web 服务

作为一名开发者，当你审视互联网上的 Web 应用程序时，你需要考虑两种 Web 开发方式。

1.  通过浏览器访问的 Web 应用程序（面向人类交互）。
2.  通过 RESTful Web 服务等协议访问的 Web 服务（面向程序化交互）。

所有流行的 Web 应用程序，如 Google、Facebook、Twitter、LinkedIn、MySpace、Flickr 和 Picasa，都为其服务提供了 RESTful 接口。有许多针对此类站点的在线目录。如果你访问 www.programmableweb.com，你会看到一份庞大的清单，列出了所有提供此类程序化交互服务的 Web 应用程序（参见图 1–1）。

![img/4a75e501abc949744a790d09257a5b1e_6_0.png](img/4a75e501abc949744a790d09257a5b1e_6_0.png)

图 1–1. 可编程 Web API 目录

许多希望为多个平台开发移动应用的公司，要么拥有自己的 Web 服务，要么依赖其他 Web 服务。虽然 PhoneGap 可以用于独立的移动应用程序，但它非常适合那些利用 Web 服务的移动应用。原因在于 PhoneGap 应用程序主要是增强了设备功能的 Web 应用程序。想一想一个能访问设备摄像头的 Flickr Web 应用，或者一个能访问 GPS 的 Google Maps 应用。另一个例子是 Foursquare，它既可以访问你的 GPS，也能访问你的手机通讯录。

这或多或少意味着，大多数基于 PhoneGap 的应用程序将使用 JavaScript 来访问 Web 服务。这使得使用 PhoneGap 的开发者掌握如何使用 Web 服务变得很重要。

对于想在阅读本书后编写 PhoneGap 应用程序的开发者，我建议在 ProgrammableWeb.com 上找一些 Web 服务，并以此为练习，为这些服务编写一个 PhoneGap 客户端。

本书将提供一个此类服务的示例，即 AlternativeTo.Net。

## 移动应用程序概述

虽然你们中许多人至少有一些移动应用程序开发的经验，但更多人可能更熟悉非移动平台（例如 Web 平台）。因此，本书将明确探讨移动应用程序的本质及其相关的挑战。如果你来自非移动开发背景，这将有助于你理解开发移动应用意味着什么。

## 移动应用程序特性

![img/4a75e501abc949744a790d09257a5b1e_7_0.png](img/4a75e501abc949744a790d09257a5b1e_7_0.png)

首先要注意的是，移动应用程序不是 Web 应用程序。区别在于特性的本质和提供特性的数量（参见图 1–3）。

移动应用程序可能具有较少的功能。

你可以预期你的移动应用程序看起来与你的 Web 应用程序大不相同。首先，你智能手机的屏幕尺寸与台式机不同。在 Web 应用上，屏幕更大，你有更多空间放置菜单、工具栏和小部件。

鉴于智能手机屏幕尺寸的限制，你会看到更多仪表板类型的主屏幕。

智能手机用户需要通过多个级别的导航才能到达他或她想要使用的功能。

智能手机用户和 Web 用户的意图不同。智能手机用户希望随时随地使用应用程序，以最少的努力获得最大的生产力，而 Web 用户可能会花更多时间使用 Web 应用程序。

由于上述差异，你会看到智能手机上最高效（或最常用）的功能被突出显示。无论移动应用程序提供的是全部功能还是功能子集，这些少量高效的（且最常用的）功能都会以最易于访问的方式组织在移动应用程序中。

![img/4a75e501abc949744a790d09257a5b1e_8_0.png](img/4a75e501abc949744a790d09257a5b1e_8_0.png)

图 1–3. 移动功能与 Web 应用功能并不相同。

### 用户交互

用户与移动应用程序交互的方式与传统 Web 应用程序非常不同（参见图 1–4）。

借助智能手机的触摸屏功能以及基于加速度计和指南针的更生动的用户交互，移动应用程序的构建方式必须有所不同。

想一想赛车游戏应用，通过向左或向右倾斜手机来操控汽车，这基于加速度计。再想一想地图应用，当用户改变方向时，它始终指向北方，这基于指南针。

虽然这种新的交互方式提升了用户体验，但较新的移动平台上缺少物理键盘，给重度键盘用户带来了一些额外的约束。在详细阐述移动应用程序需求时，需要考虑到这一点。

此外，智能手机有两种显示模式：横向和纵向；这些在早期的浏览器中闻所未闻。需求规格文档的一个重要部分就是定义设备在纵向或横向模式下应用程序的外观、感觉和行为。

![img/4a75e501abc949744a790d09257a5b1e_9_0.png](img/4a75e501abc949744a790d09257a5b1e_9_0.png)

- 触摸屏
- 方向键
- 轨迹球
- 键盘
- 加速度计
- 指南针

- 键盘
- 鼠标
- 触控板

**图 1–4.** 智能手机和 Web 应用拥有不同的用户输入接口。

### 位置感知

位置感知是智能手机与生俱来的能力。Google Maps、本地搜索、Foursquare 以及许多其他移动应用都利用了智能手机精细的 GPS。Web 应用也使用位置感知；然而，这些应用使用的 GPS 系统精度相对较低（例如，国家级别）（参见图 1–5）。

![img/4a75e501abc949744a790d09257a5b1e_9_1.png](img/4a75e501abc949744a790d09257a5b1e_9_1.png)

具备位置感知且精度高

可具备位置感知，但精度为近似值

**图 1–5.** 智能手机应用与 Web 应用的位置感知能力对比

## 推送通知

应用用户希望收到有用事件的通知，例如收到的电子邮件和消息。智能手机是通知的最佳平台，因为它几乎时刻贴近用户。

除了电子邮件或消息等通知外，任何服务都可以向智能手机用户发送通知（参见图 1–6）。想象一下组织中的一个工作流。与其让用户总是登录到 Web 应用程序来完成涉及他或她的工作流，不如让应用程序通知用户他或她需要执行操作来完成工作流，这样效率会高得多。这样，无论用户是否在其笔记本电脑或台式机附近，他或她都能保持高效。

![img/4a75e501abc949744a790d09257a5b1e_10_0.png](img/4a75e501abc949744a790d09257a5b1e_10_0.png)

## 跨平台移动应用程序开发的挑战

虽然移动应用程序开发令人兴奋，但鉴于移动操作系统（OS）数量不断增长，开发移动应用程序也面临着许多挑战。

让我们来看看这些挑战。

### 操作系统碎片化

碎片化加剧的趋势与移动平台数量的增长同时出现（参见图 1–7）。最初，有 BlackBerry 和 Symbian 智能手机——然后出现了强大的 iPhone 和 Android 平台。可以肯定的是，移动平台并未止步于此。惠普推出了 WebOS；微软推出了 Windows 7 Phone；现在，三星正在开发 Bada。

这意味着公司必须不断推出新产品，以在所有移动平台上保持存在感。

![img/4a75e501abc949744a790d09257a5b1e_11_0.png](img/4a75e501abc949744a790d09257a5b1e_11_0.png)

**图 1–7.** 移动操作系统数量增长导致的碎片化

假设你想开发一个移动应用程序，并以 iPhone、Android、BlackBerry 等为目标平台。由于每个移动平台的操作系统不同，请考虑以下事项：

1.  首先，你必须为每个平台设置不同的开发环境。
2.  其次，你需要对每个相应的操作系统有一定的专业知识。对于移动开发者来说，学习曲线可能很长。
3.  不同的移动平台需要不同的编程语言。
4.  你需要熟悉每个移动平台支持的特性；参见图 1–10。

表 1–1 描绘了移动应用程序开发（针对各种移动平台）所需的设置。

过去，我们曾见过类似的操作系统碎片化，始于 Windows、Linux 和 Mac 之间的跨桌面碎片化，这通过 Sun 推出 Java 得到了解决。在更近的时期，我们面临着浏览器碎片化，这通过跨浏览器的 JavaScript 框架如 jquery、YUI 和 Google Web Toolkit 得到了解决。

移动操作系统碎片化是所有碎片化中最糟糕、最多样的。这为在所有移动平台上启动移动应用程序增加了相当大的技术挑战。



## 多团队/多产品

如果我们选择为每个平台使用多个团队来构建移动应用程序，我们将面临诸多问题；增加团队数量会带来更多的项目交付风险；增加产品数量则意味着产品管理团队将承担更多责任（参见图 1–8）。由于功能特性在所有移动平台上也是碎片化的，产品管理团队必须针对每个平台上的产品制定具体的需求。

最终，增加更多团队、加强多团队之间的协调以及增加多个产品，都会给管理和开发团队带来额外的开销。

![](img/4a75e501abc949744a790d09257a5b1e_12_0.png)

**图 1–8.** *为不同的移动操作系统增加多个团队会带来新的问题。*

## 一致的用户体验

鉴于你希望你的应用程序在多个移动平台上保持一致，你的应用程序需要在所有平台上提供相似且一致的用户体验（参见图 1–9）。这也与你的最终用户可能会从一个平台迁移到另一个平台，或者可能同时使用多个平台有关。想想那些同时拥有 Android 智能手机和 iPhone iPad 的用户。他们可能在家或办公室时使用 iPad，而在出行途中使用 Android 智能手机。

这是你的应用程序必须在不同移动平台上提供相似用户体验的众多原因之一；当然，由于设备功能和特性的碎片化，用户体验在一定程度上会因移动平台而异。

## 第一章：理解跨平台移动应用开发

![](img/4a75e501abc949744a790d09257a5b1e_13_0.png)

## 功能碎片化

设备的功能和特性在不同平台上各不相同（参见图 1–10）。这意味着，虽然一些 Android 和 iPhone 手机内置了指南针来显示方向，但其他智能手机则没有。这可能意味着其他智能手机上的导航应用程序可能无法像 Android 或 iPhone 应用程序那样旋转地图。

总的来说，同一应用程序在某些移动平台上会禁用某些功能，这是一个现实情况；应用程序的逻辑需要以此种方式进行编写。

| 功能 | iOS (iPhone / iPhone 3GS) | iOS (iPhone 3GS 及更新型号) | Android (OS 4.6-7) | Android (OS 5.x) | Android (OS 6.0+) | Palm OS | Windows 7 Mobile | Symbian N95 |
|---|---|---|---|---|---|---|---|---|
| 加速度计 | ✓ | ✓ | ✓ | ✗ | ✓ | ✓ | ✓ | ✓ |
| 相机 | ✓ | ✓ | ✓ | ✗ | ✓ | ✓ | ✗ | ✗ |
| 指南针 | ✗ | ✓ | ✓ | ✗ | ✗ | ✗ | ✗ | ✗ |
| 通讯录 | ✓ | ✓ | ▲ | ✗ | ✓ | ✓ | ✓ | ✓ |
| 文件 | ✗ | ✗ | ✓ | ✗ | ✓ | ✓ | ▲ | ✗ |
| 地理位置 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| 媒体（音频录制） | ▲ | ▲ | ✓ | ✗ | ✗ | ✗ | ▲ | ✗ |
| 通知（声音） | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ |
| 通知（振动） | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | ✓ | ✓ |
| 存储 | ✓ | ✓ | ▲ | ✗ | ▲ | ✓ | ✓ | ✗ |

![](img/4a75e501abc949744a790d09257a5b1e_13_1.png)

## 开发环境碎片化

开发环境是一个特别重要的碎片化方面。如果你想开发针对以下平台的移动应用程序，你将至少需要两个操作系统——Windows（最好是 Windows 7）和 Mac（最好是 Leopard）：

1. iOS
2. Android
3. BlackBerry
4. WebOS
5. Symbian
6. Windows 7

此外，你将不得不使用各种 IDE 和编程语言，例如 Java、C++ 和 Objective C。同时，你将使用多种 IDE，例如 Xcode 和 Eclipse。

表 1–1 显示了开发环境的需求（针对各种移动平台）。

### 表 1–1. 开发需求

| 移动操作系统 | 操作系统 | 软件/IDE | 编程语言 |
| :--- | :--- | :--- | :--- |
| iOS | 仅限 Mac | Xcode | Objective C |
| Android | Windows/Mac/Linux | Eclipse/Java/Android 开发工具 (ADT) | Java |
| BlackBerry | 主要使用 Windows | Eclipse/JDE, Java | Java |
| Symbian | Windows/Mac/Linux | Carbide.c++ | C++ |
| WebOS | Windows/Mac/Linux | Eclipse/WebOS 插件 | HTML/JavaScript/C++ |
| Windows 7 Phone | 主要使用 Windows | Visual Studio 2010 | C#, .NET, Silverlight 或 WPF |

## PhoneGap 的跨平台移动应用策略

PhoneGap 之所以成为可能，是因为所有移动平台之间存在一个共同点。如果没有这个共同组件，PhoneGap 就不可能实现。

### 浏览器组件作为公共平台

就在几年前，浏览器领域还存在严重的碎片化。当时，不同的浏览器对 W3C 标准的遵循程度各不相同。Firefox 和 Safari 浏览器在遵循标准方面处于前列，而其他浏览器则落后。

自那时起，情况已大有改观。现在，浏览器在遵循标准方面表现得更好了（在移动平台上尤其如此）。这也是因为大多数现代移动平台都拥有基于 webkit 的浏览器。

此外，无论是桌面端还是智能手机上的新型浏览器，都已开始遵循 HTML5/CSS3 等新标准。这为浏览器世界增添了更多功能，并减少了移动平台之间的碎片化（参见图 1–11）。

![](img/4a75e501abc949744a790d09257a5b1e_15_0.png)

**图 1–11.** *移动浏览器*

让我们看看表 1-2，它列出了移动平台及其对应的浏览器平台。如你所见，除了 Windows 7 Phone 之外，所有移动平台都使用基于 webkit 的浏览器。虽然 Windows 7 Phone 有其自己的浏览器，但好消息是，此处列出的所有浏览器都已遵循 HTML5/CSS3 标准，并且随着时间的推移，它们的遵循程度将继续提高。

| 移动操作系统 | 浏览器 |
|-----------|---------|
| Android | 基于 Webkit |
| iPhone | 基于 Webkit |
| BlackBerry 6.0 + | 基于 Webkit |
| Windows 7 Phone | 基于 IE 7 * |
| WebOS | 基于 Webkit |
| Nokia | 基于 Webkit |
| BADA | 基于 Webkit |

PhoneGap 使用这些现代浏览器作为构建基于 HTML5/CSS3 应用程序的平台。可以将所有的 PhoneGap 应用程序看作内嵌了浏览器并运行这些基于 HTML5/CSS3 的应用程序。

### 移动应用 WebView

所有这些移动平台都支持在应用程序中嵌入浏览器。这意味着你的移动应用程序的一个屏幕实际上可以是一个显示 HTML 页面的浏览器。

这些嵌入式浏览器通常被称为 *webviews*。这意味着你可以将应用程序的一个屏幕定义为一个 webview。

想象一下你的应用程序有一个名为“关于我们”的屏幕。这个“关于我们”屏幕显示你公司的信息。现在，假设我们公司的“关于我们”信息频繁变更。你的移动应用程序的一个需求是显示最新的“关于我们”信息。因此，你可以不显示一个硬编码的“关于我们”屏幕，而是显示一个指向你公司“关于我们”页面（最好是网页的移动版本）的 webview。它将从网上加载“关于我们”页面。此外，webview 可用于加载和显示存储在移动设备本地的 HTML 页面。我们可以将这个概念更进一步：与其显示静态网页，我们可以显示基于 Ajax 的网页，与 Web 服务进行交互。

### 用于暴露设备功能的原生钩子

既然我们知道可以在 Web 应用程序中嵌入浏览器，让我们把重点转向通过这些嵌入式浏览器来暴露设备功能。

假设你正在开发一个基于 Flickr API 的 Flickr 应用程序。借助这些 API，你可以登录 Flickr、列出图库、下载并显示你的图片。

虽然对于 Web 应用程序来说这是一个好主意，但当我们把同样的应用程序展示在手机上时，请记住手机通常带有相机。允许 Flickr 应用程序从相机拍照并将其上传到 Flickr 将是非常合理的。

为了做到这一点，我们可以让嵌入式浏览器（或 webview）暴露 JavaScript API，当调用该 API 时，相机就会拍照，并将图片的二进制数据返回给我们（参见图 1–12）。

![](img/4a75e501abc949744a790d09257a5b1e_17_0.png)

从技术上讲，所有这些平台都支持在 webview 中向 JavaScript 暴露原生模块。这意味着，从编程角度来说，所有这些平台都允许 JavaScript 代码调用原生的 Java/C++/Objective C 代码，反之亦然。

让我们来看一个例子。我们的 webview 托管着一个 HTML 页面，该页面正在显示一个谷歌地图。我们希望根据手机的 GPS 定位来居中显示地图。为此，我们需要编写一个原生组件，用于查询设备的 GPS 位置。

然后，我们编写代码，将这个原生模块从 webview 中暴露出来。webview 中的 JavaScript 代码调用此代码以获取 GPS 坐标。一旦代码获取到 GPS 坐标，它就会相应地将地图居中。这就是 PhoneGap 框架背后的主要原理。



## HTML5 和 CSS3：编写应用程序的标准

HTML5 和 CSS3 是新兴的 Web 技术。它们正使 Web 应用程序更具交互性和功能丰富性。

HTML5 不仅增加了新的标记以提供更强大的多媒体支持；它还增加了诸如用于后台处理的 Web Worker、离线支持、数据库支持等诸多功能。

CSS3 是打造无缝、丰富用户界面 (UI) 的新标准。设计师费力去实现按钮或边框上简单圆角或渐变效果的时代已经过去。有了 CSS3，事情变得更简单、更快速、也更出色。

得益于对动画的支持，基于 CSS3 的网站现在可以与基于 Flash 的网站一较高下。不仅如此，只需更改 CSS 文件，一个门户网站就能轻松转换为移动网站。此外，现在可以通过不同的 CSS 文件实现打印预览。

众所周知，移动浏览器是 W3C 标准的早期采用者。这意味着手机是运行 HTML5/CSS3 应用程序的理想平台。

## 同源策略不适用

对于那些使用过基于 Ajax 应用程序的人来说，您知道托管在 “abc.com” 的 Web 应用程序无法对托管在 “xyz.com” 的 Web 服务发起 Ajax 调用。这意味着如果有人正在开发一个基于 Ajax 的应用程序——比如说，托管在 myphotobook.com——他或她将无法向 flickr.com 发起 Ajax 调用。

这被称为*同源策略*——您可以在 http://en.wikipedia.org/wiki/Same_origin_policy 上阅读更多关于同源策略的信息。

对于 PhoneGap 应用程序则情况不同。PhoneGap 应用程序打包了所需的 HTML、JavaScript 和 CSS 文件，并且 PhoneGap 应用程序没有像 “abc.com” 这样的域名。这使得 PhoneGap 成为一个易于开发混搭应用 (mashups) 的平台，这些应用可以自由地向各种其他站点发起 Ajax 调用。

想象一下，只需几行 JavaScript 代码，您的 PhoneGap 应用程序就能将 Facebook、Twitter 和 Flickr 全部整合到一个混搭应用中。

这使得 PhoneGap 成为在 programmableweb.com 上列出的 Web 服务创建移动应用程序的理想平台。

其限制如图 1–13 所示：

# 第 1 章：理解跨平台移动应用开发

![](img/4a75e501abc949744a790d09257a5b1e_19_0.png)

## 结论

PhoneGap 使用 HTML5、JavaScript 和 CSS3 来开发移动应用程序。这些是 Web 世界中的标准技术。通过使用 PhoneGap，具有很少或没有原生语言背景的开发人员就可以开始为所有流行的移动平台开发移动应用程序。

尽管 PhoneGap 提供了对移动应用程序标准原生功能的访问，但其插件框架足够灵活，可以在需要时进行扩展和添加新功能。

PhoneGap 是一项不断发展的技术，用于开发跨移动平台的应用程序。

# 第 2 章

## PhoneGap 入门

PhoneGap 是一个 HTML5 应用程序框架，用于通过 Web 技术开发原生应用程序。这意味着开发人员可以利用其现有的 HTML、CSS 和 JavaScript 知识来开发智能手机和平板电脑应用程序。使用 PhoneGap，开发人员不必学习像 iPhone 使用的 Objective-C 这样的语言。

使用 PhoneGap 开发的应用程序是混合应用程序。这些应用程序既不是纯粹基于 HTML/JavaScript，也不是原生的。应用程序的部分内容，主要是 UI、应用程序逻辑以及与服务器的通信，是基于 HTML/JavaScript 的。应用程序的另一部分，即与设备（手机或平板电脑）进行通信和控制的部分，则是基于该平台的原生语言。PhoneGap 提供了从 JavaScript 世界到平台原生世界的桥梁，允许 JavaScript API 访问和控制设备（手机或平板电脑）。

PhoneGap 本质上为 JavaScript API 提供了对设备（手机或平板电脑）功能的访问，例如摄像头、GPS、设备信息等等。这些 API 将在第 4 章中详细介绍。

本章首先提供适当的信息以帮助您理解 PhoneGap 的整体架构。然后我们将在一个 PhoneGap 示例中应用这些信息。在本章结束时，我们将使用 PhoneGap 编写一个小型的 Hello World 应用程序。

> **注意：** PhoneGap 是一个框架；它不提供任何用于编码的 IDE 或特殊开发环境。您需要使用 Eclipse 和 Android SDK 来为 Android 开发 PhoneGap 应用程序；您需要使用 Xcode 来为 iPhone 开发 PhoneGap 应用程序。

## PhoneGap 架构

![](img/4a75e501abc949744a790d09257a5b1e_21_0.png)

**图 2–1.** *PhoneGap 应用程序架构*

PhoneGap 框架主要是一个 JavaScript 库，允许 HTML/JavaScript 应用程序访问设备功能。PhoneGap 框架还有一个原生组件，它在后台工作并在设备（手机或平板电脑）上执行实际操作。

请参考图 2–1 了解 PhoneGap 的整体架构。使用 PhoneGap 构建的应用程序主要有两个部分：

- 1. JavaScript 业务逻辑部分，驱动 UI 及其功能。
- 2. JavaScript 部分，用于访问和控制设备（手机或平板电脑）。

考虑一个 Facebook 应用程序。应用程序的主要部分将是登录页面和下载照片库。现在您想要添加一个模块，让您能够拍摄照片并将其上传到 Facebook。为此，您将调用 PhoneGap 的摄像头 API 来访问手机的摄像头，拍摄照片，并获取照片文件。下一步是进行 AJAX 调用到 Facebook 服务器，以上传照片。

另一个可以应用的示例是使用 PhoneGap 将好友列表存储在数据库中，以便我们可以搜索本地好友。

前面的描述给人一种印象，即在 PhoneGap 中开发移动应用程序更多地涉及编写业务逻辑和 UI，而较少涉及访问设备的功能，这是正确的。本书不仅解释了 PhoneGap API，而且还是创建基于 HTML5/CSS3 移动应用程序的指南。

## 在 Android 上设置环境

创建 PhoneGap 应用程序的第一步是设置移动开发环境。我们将从 Android 开始，因为 Android 应用程序开发使用的是基于 Eclipse 的 Java，并且支持 PhoneGap 的几乎所有功能。

您需要为 Android 下载并安装以下先决条件：

- 1. JDK 1.6+
- 2. Eclipse 3.4 到 3.6
- 3. 包含 Android 2.2 平台的 Android SDK
- 4. Eclipse 的 Android ADT 插件
- 5. Android 2.2 的 Android AVD
- 6. Android 版 PhoneGap SDK 1.1.0

由于 Android 使用 Java 编程，我们需要 JDK 1.6+ 和 Eclipse 3.4+。然后我们将安装 Android SDK。Android SDK 是一个通用 SDK，不包含对任何特定平台的支持。平台是指操作系统版本，例如 2.2 Froyo、2.3 Ginger Bread 和 3.0 Honeycomb。需要下载这些平台才能创建、构建和运行 Android 项目。这个插件被称为 Android ADT 插件。

一旦 Eclipse、Android SDK 和 Android ADT (Eclipse 插件) 都设置好，我们需要为 Android 创建一个模拟器环境。这称为准备 Android AVD（Android 虚拟设备）。如果我们正在为 Android 2.2 Froyo 开发 PhoneGap 应用程序，我们需要相同 Android 平台的 AVD。

以下步骤将解释如何创建一个 Android 项目并将 PhoneGap 库注入到 Android 中。

## PhoneGap Android 项目所需的安装

- 1. 安装 3.4 版本的 Eclipse。
- 2. 安装 Android SDK。
- 3. 安装 Eclipse 的 Android ADT 插件。
- 4. 为模拟器创建 AVD。
- 5. 安装 PhoneGap 库。

### 步骤 1：设置 Eclipse

此步骤假设您已经安装了 Java SDK 1.6。安装完成后，从 www.eclipse.org/downloads/ 下载 Eclipse。请参见图 2–2 查看 Eclipse 下载页面。我们需要一个支持 JDT (Java 开发环境) 的 Eclipse IDE 3.4+ 版本。您应该安装用于 Java 开发人员的 Eclipse IDE。

![](img/4a75e501abc949744a790d09257a5b1e_23_0.png)

图 2–2. *Eclipse 下载页面*

### 步骤 2：安装 Android SDK

设置 Android 开发环境的一些步骤是平台相关的。为避免任何混淆，我们将以特定平台的方式解释如何执行每个步骤。



首先，从 http://developer.android.com/sdk/index.html 下载 Android SDK（参考图 2-3）。

![](img/4a75e501abc949744a790d09257a5b1e_24_0.png)

## Windows 系统说明

使用 Android 安装程序 `installer r11-windows.exe` 安装 Android SDK。这是 Windows 系统的推荐安装方式。另一种方式是下载 `android-sdk_r11-windows.zip` 文件并解压到一个文件夹中。我们假设 Android SDK 解压到了 `c:\android_sdk`。

## Linux 系统说明

下载归档文件 `android-dk_r11-linux_x86.tgz` 并解压到一个文件夹中。

## Mac OSX Intel 系统说明

下载归档文件 `android-sdk_r11-mac_x86.zip` 并解压到一个文件夹中。

此 Android SDK 支持迄今为止已发布的所有 Android 平台。这些平台包括 Android 1.1 平台至最近的 Android 3.0（蜂巢）平台。由于并非每个人都需要所有平台，因此 Android SDK 初始并未预装任何平台。

对于本书，我们将仅关注 SDK 平台：Android 2.2，API 8，修订版 3。由于没有预装平台，下一步是安装你感兴趣的平台。转到 Android SDK 位置（在我们的例子中是 `c:\android_sdk`），并在 `tools` 文件夹中打开名为 `Android` 的可执行文件。如果你有带宽限制，可以不下载所有平台，而只下载 Android 的 2.2 平台（SDK 平台 Android 2.2，API 8，修订版 3）。

这将打开图 2-4 所示的屏幕。选择“可用软件包”选项，勾选“Android 仓库”，然后点击“安装”。

![](img/4a75e501abc949744a790d09257a5b1e_25_0.png)

*图 2-4. 可安装的可用平台软件包*

现在你已下载平台，便拥有了为迄今为止所有已发布 Android 版本创建应用程序所需的工具。

建议你安装所有可用软件包，这样你便拥有为任何已发布 Android 平台创建 Android 项目的工具。

如果你想为 Froyo（Android 2.2）开发移动应用，则需要确保在已安装的软件包列表中包含 Froyo（Android 2.2）。

## 步骤 3：为 Eclipse 安装 Android ADT 插件

1.  启动 Eclipse 并点击 Help->Install New Software 以打开“可用软件”对话框。
2.  在“Work With”文本框中输入 URL `https://dl-ssl.google.com/android/eclipse`，如图 2-5 所见。
3.  当你看到安装“Developer Tools”的选项时，点击它，勾选“Developer Tools”下的所有复选框，然后点击 Next。

# 第 2 章：开始使用 PhoneGap

![](img/4a75e501abc949744a790d09257a5b1e_26_0.png)

*图 2-5. 为 Eclipse 安装 Android ADT 插件*

4.  使用之前安装的 Android SDK 路径配置 Android ADT 插件。通过点击 Windows->Preferences（Windows 系统）或 Eclipse-->Preferences（Mac 系统）打开 Eclipse 的首选项设置。如果你收到“未签名内容警告”对话框，可以安全地忽略它。
5.  在“首选项”窗格中，点击并展开“Android”选项。你将看到如图 2-6 所示的 Android 首选项窗格。在 Android 首选项窗格中，在 SDK Location 文本框中输入 Android SDK 的位置，然后点击“Apply”。

如果 Android SDK 路径正确，你应该能在 Target Name 下看到多个选项，包括 Android 2.2。

![](img/4a75e501abc949744a790d09257a5b1e_27_0.png)

## 步骤 3：为 Android 2.2 平台创建 Android AVD

1.  打开 Eclipse 并为 Android PhoneGap 创建一个工作空间。下一步是为 Android 创建一个模拟器。由于 Android 有多个平台版本，我们必须为每个目标平台创建一个 Android 虚拟设备（AVD）。在图 2-7 中，你将看到屏幕上描绘的 Eclipse。

请注意，Android 模拟器运行的是一个 Android 虚拟设备（AVD）。

![](img/4a75e501abc949744a790d09257a5b1e_28_0.png)

*图 2-7. 带有 ADT 插件的 Eclipse。*

2.  点击工具栏上的按钮以打开 Android SDK 和 AVD 管理器。选择如图 2-8 所示的“Virtual Devices”选项。

![](img/4a75e501abc949744a790d09257a5b1e_28_1.png)

*图 2-8. Android SDK 和 AVD 管理器*

3.  点击“New”按钮以创建一个新的 AVD。选择 Android 2.2 平台（也称为 Froyo）。选择 128 MB 的 SD 卡大小，并选择内置皮肤为 HVGA。填写完毕后，点击“Create AVD”。参考图 2-9 查看“AVD 屏幕”的样子。

![](img/4a75e501abc949744a790d09257a5b1e_29_0.png)

**图 2-9.** 创建一个将在 Android 模拟器中运行的新 Android 虚拟设备（AVD）

你将看到已创建的 AVD，如图 2-10 所示。

## 步骤 4：安装 PhoneGap SDK

1.  从以下链接下载 PhoneGap SDK 1.1.0：`http://phonegap.googlecode.com/files/phonegap-1.1.0.zip`。解压此 zip 文件后，你应该会看到如图 2-11 所示的目录结构。

*图 2-10. Android 2.2 平台（Froyo）的 AVD*

![](img/4a75e501abc949744a790d09257a5b1e_30_0.png)

![](img/4a75e501abc949744a790d09257a5b1e_30_1.png)

*图 2-11. PhoneGap SDK 1.1.0 目录结构*

2.  选择 Android 目录，你将看到 `phonegap-1.1.0.jar` 和 `phonegap-1.1.0.js` 文件（见图 2-12）。

![](img/4a75e501abc949744a790d09257a5b1e_30_2.png)

*图 2-12. PhoneGap SDK 内的 Android 文件夹。*

至此，PhoneGap for Android 的设置完成。

## 创建新项目

本书的第一个应用程序是一个 Hello World 应用程序。Hello World PhoneGap 移动应用程序会在 PhoneGap 框架加载后在屏幕上显示“Hello World”。

### 步骤 1：创建一个 Android 项目

打开 Eclipse，点击 File->New Project->Android Project。这将打开一个 Android 项目对话框，如图 2-13 和图 2-14 所示。具体步骤如下：

1.  在“Project name”中输入 `PhoneGap-helloworld`。
2.  确保已选择 Android 2.2 作为构建目标。
3.  在“Application name”中输入 `Helloworld`。这是应用程序的可读名称。
4.  在“Package name”中输入 `org.examples.phonegap.sample`。Android 市场上的应用程序通过包名唯一标识。Android 市场上不能有两个包名相同的 Android 应用程序。
5.  勾选“Create Activity”复选框，并在“Activity name”中输入 `helloworld`。Android 中的 activity 是一个屏幕。activity 名称也是该 activity 的类名。
6.  在“Min SDK Version”中填入 `7`。这意味着你将允许此应用程序被所有 Android 2.1 设备平台（也称为 Éclair Android 手机）搜索和安装。

![](img/4a75e501abc949744a790d09257a5b1e_32_0.png)

![](img/4a75e501abc949744a790d09257a5b1e_32_1.png)

**新建 Android 项目**

必须指定包名。

项目名称：PhoneGap-HelloWorld

内容
- 在工作空间中创建新项目
- 从现有源创建项目
- 使用默认位置
位置：/Users/rohit/Documents/workspaces/phonegap-android 浏览...

- 从现有示例创建项目
示例：ApiDemos

构建目标

| 目标名称 | 供应商 | 平台 | API |
|---|---|---|---|
| Android 1.5 | Android Open Source Project | 1.5 | 3 |
| Google APIs | Google Inc. | 1.5 | 3 |
| Android 1.6 | Android Open Source Project | 1.6 | 4 |
| Google APIs | Google Inc. | 1.6 | 4 |
| Android 2.1-update1 | Android Open Source Project | 2.1-update1 | 7 |
| Google APIs | Google Inc. | 2.1-update1 | 7 |
| Android 2.2 | Android Open Source Project | 2.2 | 8 |
| Google APIs | Google Inc. | 2.2 | 8 |
| GALAXY Tab Addon | Samsung Electronics Co., Ltd. | 2.2 | 8 |
| GALAXY Tab Addon | Samsung Electronics Co., Ltd. | 2.2 | 8 |
| GALAXY Tab Addon | Samsung Electronics Co., Ltd. | 2.2 | 8 |
| GALAXY Tab Addon | Samsung Electronics Co., Ltd. | 2.2 | 8 |
| GALAXY Tab Addon | Samsung Electronics Co., Ltd. | 2.2 | 8 |
| Android 2.3.1 | Android Open Source Project | 2.3.1 | 9 |
| Google APIs | Google Inc. | 2.3.1 | 9 |
| Android 2.3.3 | Android Open Source Project | 2.3.3 | 10 |

< 后退 下一步 > 取消 完成

*图 2-13. Android 项目创建*

www.it-ebooks.info



## 步骤 2：将 PhoneGap 库添加到项目中

Android 项目创建完成后，就该将 PhoneGap 框架注入到 Android 项目中了。正如我们之前提到的，PhoneGap 包含三个主要组件：原生组件、XML 插件和一个 JavaScript 文件。

- 1. 要在 Android 中安装原生组件，请在项目中创建一个名为 `lib` 的目录，并将 PhoneGap jar 文件复制到其中。你可以将 `phonegap-1.1.0.jar` 拖放到 `lib` 文件夹中，也可以在 Eclipse IDE 中将其复制并粘贴到 `lib` 文件夹中。接下来，右键单击 Build Path -> Add to Build Path，将 PhoneGap jar 添加到类路径。此步骤在图 2–15 中有高亮显示。

- 2. 将 PhoneGap 的 Android 目录中的 XML 目录复制到 `res` 文件夹中。

![Android Project creation.](img/4a75e501abc949744a790d09257a5b1e_33_0.png)

**图 2–14.** Android 项目创建。

![Highlighting the location of the PhoneGap jar in the Android Project](img/4a75e501abc949744a790d09257a5b1e_34_0.png)

**图 2–15.** 高亮显示 PhoneGap jar 在 Android 项目中的位置

3. 将 PhoneGap Jar 添加到 Android 项目后，就该将 PhoneGap 的 JavaScript 文件注入到项目中了。我们将在 Android 项目的 Assets 文件夹下创建一个 `www` 文件夹。Assets 文件夹就像是 Android 应用程序的媒体文件夹。在我们的例子中，我们将把所有基于浏览器的应用程序文件放在 `www` 文件夹内。首先，将 Assets 文件夹中找到的 PhoneGap JavaScript 文件添加到 `www` 文件夹中。此步骤在图 2–16 中有高亮显示。

## 第 2 章：PhoneGap 入门

![Highlighting the location of the PhoneGap JavaScript file in the Android Project](img/4a75e501abc949744a790d09257a5b1e_35_0.png)

**图 2–16.** 高亮显示 PhoneGap JavaScript 文件在 Android 项目中的位置

## 步骤 3：修改 Android 权限

在 Android 应用程序中，主文件是 Android Manifest 文件。在这个文件中有很多具体的信息，比如包名，它唯一标识市场上的应用程序。主文件包含一个名为 permissions 的部分。Android 使用此部分来通知用户该应用程序将使用手机的某些功能。假设一个应用程序打算使用互联网获取数据；为了安装该应用程序，需要获得相应的权限。当用户安装该应用程序时，Android 市场会向他显示该应用程序将被授予使用互联网的权限。

对于 PhoneGap，需要添加以下权限：

- 1. 将以下权限添加到 Android Manifest XML 中：

```xml
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.VIBRATE" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_LOCATION_EXTRA_COMMANDS" />
<uses-permission android:name="android.permission.READ_PHONE_STATE" />
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.RECEIVE_SMS" />
<uses-permission android:name="android.permission.RECORD_AUDIO" />
<uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
<uses-permission android:name="android.permission.READ_CONTACTS" />
<uses-permission android:name="android.permission.WRITE_CONTACTS" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

2. 我们还需要在 Manifest 文件中添加 `supports-screen` 选项，如下所示：

```xml
<supports-screens
    android:largeScreens="true"
    android:normalScreens="true"
    android:smallScreens="true"
    android:resizeable="true"
    android:anyDensity="true" />
```

3. 在 Android Manifest 中的 activity 添加 `android:configChanges="orientation|keyboardHidden"`。这会告诉 Android 当用户翻转手机，屏幕在纵向和横向之间切换时，不要销毁并重新创建该 activity。

4. 通过应用以下 XML 代码片段，在前一个 activity 之后添加第二个 activity：

```xml
<activity android:name="com.phonegap.DroidGap" android:label="@string/app_name"
    android:configChanges="orientation|keyboardHidden">
    <intent-filter> </intent-filter>
</activity>
```

按照之前的说明修改 Android Manifest 后，将出现如下所示的 Android Manifest XML：

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="org.examples.phonegap.helloworld" android:versionCode="1"
    android:versionName="1.0">
    <supports-screens android:largeScreens="true"
        android:normalScreens="true" android:smallScreens="true"
        android:resizeable="true" android:anyDensity="true" />
    <uses-permission android:name="android.permission.CAMERA" />
    <uses-permission android:name="android.permission.VIBRATE" />
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_LOCATION_EXTRA_COMMANDS" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE" />
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.RECEIVE_SMS" />
    <uses-permission android:name="android.permission.RECORD_AUDIO" />
    <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
    <uses-permission android:name="android.permission.READ_CONTACTS" />
    <uses-permission android:name="android.permission.WRITE_CONTACTS" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-sdk android:minSdkVersion="7" />

    <application android:icon="@drawable/icon" android:label="@string/app_name">
        <activity android:name="HelloWorld" android:label="@string/app_name"
            android:configChanges="orientation|keyboardHidden">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        <activity android:name="com.phonegap.DroidGap"
            android:label="@string/app_name"
            android:configChanges="orientation|keyboardHidden">
            <intent-filter>
            </intent-filter>
        </activity>
    </application>
</manifest>
```

## 步骤 4：修改主 Activity

在 Android 中，一个名为 activity 的类代表一个屏幕。为了在 Android 中使用 PhoneGap，我们将屏幕从一个 activity 更改为一个 DroidGap。DroidGap 是一个特殊的 activity，它允许我们显示 HTML 页面。HelloWorld 类如图 2–17 所示。

> 注意：我们是在告诉 DroidGap 加载 Android Assets 中的 `index.html` 文件。

```java
package org.examples.phonegap.helloworld;

import android.os.Bundle;

import com.phonegap.DroidGap;

public class HelloWorld extends DroidGap {
    /** Called when the activity is first created. */
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        super.loadUrl("file:///android_asset/www/index.html");
    }
}
```

## 编写 HelloWorld 应用程序

PhoneGap 应用程序是一个 HTML/JavaScript 应用程序。请参考图 2–18。以下是 `index.html`。

- 1. 在 HTML 页面中包含 PhoneGap JavaScript 库版本 1.1.0。
- 2. 将 `init()` 方法注册到 body 的 `onload` 事件。
- 3. 在 `init()` 函数中，将 JavaScript 回调函数 `onDeviceReady` 注册到 `deviceready` 事件。
- 4. 在 `onDeviceReady` 回调函数中，用文本 “hello World! Loaded PhoneGap Framework!” 更改 ID 为 "helloworld" 的 `h1` 元素的内容。

完整的源代码如下：

```html
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
```



## 第2章：PhoneGap入门

```html
<script type="text/javascript">

    /** 当PhoneGap JavaScript加载完成时调用 */
    function onDeviceReady(){
        document.getElementById("helloworld").innerHTML
        ="Hello World! PhoneGap框架已加载！";
    }

    /** 当浏览器加载此页面时调用 */
    function init(){
        document.addEventListener("deviceready", onDeviceReady, false);
    }

</script>
</head>
<body onLoad="init()">

    <h1 id="helloworld">...</h1>

</body>
</html>
```

![](img/4a75e501abc949744a790d09257a5b1e_39_0.png)

**图 2–18.** *PhoneGap项目的Index.html文件*

你可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/67848b004644/android/PhoneGap-Helloworld 下载本章的完整源代码

## 部署到模拟器

要运行Android应用程序，请右键单击PhoneGap-helloworld项目，选择“运行方式”，然后选择“Android应用程序”。

这将启动我们之前创建的AVD模拟器。当应用程序加载时，你将看到如图2–19所示的屏幕。应用程序启动时，你将在屏幕上看到……，如图2–19所示。

![](img/4a75e501abc949744a790d09257a5b1e_40_0.png)

**图 2–19.** *PhoneGap应用程序加载时显示...几秒钟。*

PhoneGap框架加载完成后，你将看到应用程序显示一条消息，如图2–20所示。

![](img/4a75e501abc949744a790d09257a5b1e_41_0.png)

**图 2–20.** *PhoneGap框架加载完毕后，PhoneGap应用显示一条消息。*

到目前为止，我们已经了解了如何在模拟器上测试应用程序。然而，某些功能无法在模拟器上进行测试。为了测试GPS、摄像头、加速度计、指南针以及实际的用户感知，需要在实际设备上进行测试。

## 部署到设备

将Android应用程序部署到设备是一个两步过程：

### 第1步：准备设备。

1.  解锁你的设备并按菜单键。这将显示一个类似图2–21的界面。

![](img/4a75e501abc949744a790d09257a5b1e_42_0.png)

2.  单击“设置”，屏幕上将出现图2–22所示的界面。选择“应用程序”选项。

![](img/4a75e501abc949744a790d09257a5b1e_43_0.png)

**图 2–22.** *进入应用程序设置*

3.  现在我们必须确保可以在设备上部署非电子市场应用程序。这通过单击“未知来源”来完成，如图2–23所示。

![](img/4a75e501abc949744a790d09257a5b1e_44_0.png)

**图 2–23.** *单击“未知来源”以便我们可以添加非电子市场应用程序*

4.  下一步是进入开发选项（参见图2–24）并启用USB调试（参见图2–25）。这允许你将USB线的一端插入Android设备，另一端插入你的PC或Mac。使用Eclipse来调试在你设备上运行的应用程序。

![](img/4a75e501abc949744a790d09257a5b1e_45_0.png)

**图 2–24.** *进入开发选项*

![](img/4a75e501abc949744a790d09257a5b1e_46_0.png)

**图 2–25.** *启用USB调试*

现在你的设备已准备好部署应用程序。

Android ADT插件为Android提供了Dalvik调试监控服务器（DDMS）。DDMS具有许多功能，例如列出当前可用于部署和调试Android应用程序的设备/模拟器，允许用户查看从部署在设备/模拟器上的应用程序发出的日志消息，以及浏览设备/模拟器的文件系统。

### 第2步：在“应用程序启动类型”处，提供我们要部署到设备的信息。

1.  将USB线插入你的设备，并将USB端插入你的开发机器。现在打开Eclipse并进入DDMS透视图（转到Eclipse->窗口->打开透视图->DDMS）。你将看到如图2–26所示的屏幕。此屏幕显示我们有一个Android模拟器正在运行，并且我们还有一个Android设备插入到机器的USB输入端口。

![](img/4a75e501abc949744a790d09257a5b1e_47_0.png)

**图 2–26.** *DDMS显示我们有一个模拟器正在运行，并且有一个设备已插入USB。*

2.  当你单击Android项目中任何Android应用程序的“运行方式”时，你将看到图2–27所示的屏幕。之所以显示此屏幕，是因为你同时有模拟器和设备可用。这里Eclipse正在询问你要将应用程序部署到何处。如果你只插入了设备而没有运行模拟器，则不会看到此屏幕。

![](img/4a75e501abc949744a790d09257a5b1e_48_0.png)

**图 2–27.** *如果存在多个设备或模拟器，DDMS会提示用户选择将应用程序部署到何处。*

## 探索PhoneGap功能

本节将深入探讨更多PhoneGap功能。

以下是PhoneGap支持的功能简要概述：

1.  PhoneGap的加速度计API使应用程序能够感知设备方向的变化，因此能够做出相应的反应。这对于创建具有气泡水平仪的应用程序（确保手机与地面水平对齐）非常有用。可以选择获取一次设备方向变化的读数，或持续接收设备方向的变化。
2.  PhoneGap的摄像头API允许应用程序从摄像头获取图片（这对于Facebook和Picasa等应用程序非常有用），或者从现有的照片库中获取图片。
3.  PhoneGap的指南针API帮助应用程序了解手机的方位。这对于地图和导航应用程序非常有用，因为当用户改变手机方位时，地图会随之旋转。可以选择获取一次设备方位变化的读数，或持续接收设备方位的变化。
4.  PhoneGap的通讯录API是应用程序读取和写入通讯录的一种方式。许多社交应用程序可以通过将手机通讯录与社交渠道上的联系人同步而受益。
5.  PhoneGap的文件API允许应用程序读取、写入和列出目录及文件系统。如果应用程序计划更改手机文件系统中的文件内容，这将非常方便。此API还可以帮助编写文件管理器应用程序。
6.  地理位置API有助于获取设备的地理位置。这对于许多应用程序都非常有用，包括基于地图的应用程序，以及像Foursquare这样的应用程序，用户可以使用他们的GPS位置签到某个地点。可以选择获取一次设备地理位置变化的读数，或持续接收设备地理位置的变化。
7.  媒体API允许应用程序控制设备上的媒体传感器和应用程序。此API允许应用程序录制和播放音频及视频记录。
8.  PhoneGap的网络API为应用程序提供了查看网络状态的能力。此状态不仅仅是在线和离线，它还告诉应用程序设备是在2G/3G/4G网络还是Wi-Fi网络上。这些信息通常有助于应用程序决定何时检索特定类型的信息。
9.  通知API允许应用程序通过发出嘟嘟声、振动或提供视觉警报来通知用户某事已发生。
10. PhoneGap的存储API为应用程序提供了内置的SQL数据库。应用程序可以通过SQL语句插入、检索、更新和删除数据。应用程序可以查询数据库中的数据，并在本地存储的电子邮件列表中搜索特定的电子邮件。

## PhoneGap教程

并非所有PhoneGap教程都可以在Android模拟器上完成，因此我们将说明以下检查教程的方法：

-   可以在Android模拟器上完成的教程。
-   需要Android手机才能进行的教程。

### 模拟器示例

#### 获取设备信息

PhoneGap允许以编程方式读取设备信息。为此，你需要确保PhoneGap框架已加载。框架加载后，你可以使用JavaScript提取设备信息。设备信息的所有属性列于表2–1中。

*表 2–1. 设备信息属性*

| JavaScript属性 | 描述 |
| :--- | :--- |
| device.name | 获取设备的型号名称。 |
| device.phonegap | 获取设备上运行的PhoneGap版本。 |
| device.platform | 获取设备的操作系统。 |
| device.version | 获取设备操作系统的版本。 |
| device.uuid | 获取设备的通用唯一标识符号码。 |

以下代码将允许你访问设备的信息。请参考图2–28。

```html
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript">
      /** 当PhoneGap JavaScript加载完成时调用 */
```



## **获取设备的联系人信息**

我们将使用 PhoneGap 来获取设备的通讯录联系人号码。在此之前，我们需要先在 Android 模拟器上设置一些联系人信息。

1.  点击拨号应用程序图标，如图 2-30 所示。

2.  这将打开拨号应用程序。点击“联系人”标签页，如图 2-31 所示。

图 2–31. *在手机应用中添加联系人*

3.  点击菜单并选择“新建联系人”。在新建联系人中，输入名字、姓氏和电话号码。请参考图 2–32 和 2–33。

图 2–32. 点击菜单并点击“新建联系人”

图 2–33. 添加联系人并点击“完成”。

4.  输入所需信息后，点击“完成”，你应该会在联系人列表中看到一个联系人（如图 2–34 所示）。

图 2–34. 联系人列表

为了使用 PhoneGap 访问联系人列表，我们需要使用以下 API：`navigator.service.contacts.find(contactFields, contactSuccess, contactError, contactfindOptions);` 表 2–2 提供了每个参数的说明。

**表 2–2. PhoneGap 联系人 API 的参数**

| 参数 | 描述 | 示例 |
| :--- | :--- | :--- |
| contactField | 必需参数。这是一个需要返回的联系人字段的数组。 | ["name","phoneNumbers"] |
| contactSuccess | 一个 JavaScript 回调函数，接收一个联系人数组作为参数。 | function onSuccess(contacts){ } |
| contactError | 一个 JavaScript 回调函数，接收一个错误作为参数。 | function onError(error){ } |
| contactfindOptions | 可选项，如按姓名筛选 | var options = new ContactFindOptions() options.filter="Bob"; |

以下提供了获取联系人的完整代码步骤：

1.  创建一个 `ContactFindOptions` 对象。通过设置 `options.filter` 等于 `""`，我们表示希望获取所有联系人。如果 `options.filter` 是 "Bob"，则意味着我们希望筛选搜索结果，使得所有结果都必须在联系人字段的某处包含关键词 "Bob"。

    ```javascript
    var options = new ContactFindOptions();
    options.filter="";
    ```

2.  我们需要定义要获取的联系人字段。当我们搜索联系人时，会出现一个联系人列表。联系人本身是一个联系人字段的关联数组。这意味着，如果我们指定只希望获取姓名和电话号码这两个联系人字段中的信息，那么只会返回这些信息。

    ```javascript
    var fields = ["name","phoneNumbers"];
    ```

3.  定义成功和失败的回调方法。当我们调用 `Navigator.service.contacts.find()` 方法时，需要提供两个回调。这是因为 find() 方法是一个异步方法。

    ```javascript
    function onSuccess(contacts) {
        for(var index=0;index<contacts.length;index++){
            var contact= contacts[index];
            var contactName = contact.name.formatted;
        }
    }
    function onError(error) {
    }
    navigator.service.contacts.find(fields, onSuccess, onError, options);
    ```

4.  使用 Android 的 Linkify 功能来允许我们拨打电话号码。虽然我们作为 HTML 列表的一部分来列出通讯录中的联系人（如下面的代码所示），

    ```html
    <ul>
    <li>Rohit Ghato1</li>
    </ul>
    ```

    但我们可以通过为联系人使用链接使列表更有用。如下所示：

    ```html
    <ul>
    <li>
    <a href="tel://999-999-9999">Rohit Ghato1</a>
    </li>
    </ul>
    ```

    当用户点击链接 "Rohit Ghato1" 时，Android 会读取 URL 中的 `tel:` 协议并打开拨号器来拨打该号码。

    这如图 2–36 和图 2–37 所示，展示了应用程序在 Android 模拟器上的样子。

使用以下代码来应用我们迄今为止所学的内容。参考图 2–35 查看 index.html 的源代码。

```html
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript">
      /** 当 PhoneGap JavaScript 加载时调用 */
      function onDeviceReady(){
          // 查找所有联系人
          var options = new ContactFindOptions();
          options.filter="";
          var fields = ["phoneNumbers", "name"];
          navigator.service.contacts.find(fields, onSuccess, onError
          , options);
      }
      function onSuccess(contacts) {
          var ul = document.getElementById("list");
          for(var index=0;index<contacts.length;index++){
              var name = contacts[index].name.formatted;
              var phoneNumber = contacts[index].phoneNumbers[0].value;
              var li = document.createElement('li');
              li.innerHTML = "<a href=\"tel:"+phoneNumber+"\">"+name+"</a>";
              ul.appendChild(li);
          }
      };
      function onError() {
          alert('onError!');
      };
      /** 当浏览器加载此页面时调用*/
      function init(){
          document.addEventListener("deviceready", onDeviceReady, false);
      }
    </script>
  </head>
  <body onLoad="init()">
    <h1>Contacts</h1>
    <ul id="list">
    </ul>
  </body>
</html>
```

图 2–35. PhoneGap 联系人应用 HTML/JavaScript 源代码

图 2-36. 列出联系人

图 2-37. 点击联系人会打开手机拨号器。

你可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/67848b004644/android/PhoneGap-Contacts 下载此示例的完整源代码。

你可以参考 Contacts API 的官方文档：http://docs.phonegap.com/en/1.1.0/phonegap_contacts_contacts.md.html#Contacts。

## 获取 SD 卡文件列表

本节将解释如何列出 Android 设备的 SD 卡内容。本节结合使用了 W3C 标准和 PhoneGap API。

列出 Android 设备 SD 卡内容有两个步骤。步骤如下：

1.  我们解析目录 `file:///sdcard` 并获得对 directoryentry 的访问权限。
2.  当我们获得对 directoryentry 的访问权限后，可以从中创建一个 directoryreader，并获取目录（SD 卡）的内容。

在步骤 1 中，我们调用以下函数：

```javascript
window.resolveLocalFileSystemURI("file:///sdcard", onResolveSuccess, onError);
```

作为对上述函数的响应，`onResolveSuccess` 回调将被激活。`onResolveSuccess` 回调可以在下面的代码中看到。一旦我们获得对 fileEntry 的访问权限，我们就从中创建一个 directoryReader，并对该 directoryReader 调用 `readEntries`。

```javascript
function onResolveSuccess(fileEntry){
    var directoryReader = fileEntry.createReader();
    directoryReader.readEntries(onSuccess,onError);
}
```

当路径 `file:///sdcard` 成功解析后，`onSuccess` 方法将被调用。`onSuccess` 方法如下：

```javascript
function onSuccess(entries) {
    document.getElementById("loading").innerHTML="";
    var ul = document.getElementById("file-listing");
    for(var index=0;index<entries.length;index++){
        var li = document.createElement('li');
        li.innerHTML = entries[index].name;
        ul.appendChild(li);
    }
}
```

## 部署到模拟器

以下代码提供了如何部署到模拟器的完整示例：

```html
<!DOCTYPE HTML>
<html>
<head>
```



## 读写文件

本节将向你展示如何使用 PhoneGap API 来操作文件系统。

> **注意：** PhoneGap 实际上实现并支持了 W3C 在 http://www.w3.org/TR/file-system-api/ 中提到的文件系统规范。

让我们先熟悉文件系统 API 中的一些关键概念。这些关键概念是：

-   LocalFileSystem
-   fileSystem
-   fileEntry
-   directoryEntry

## LocalFileSystem

LocalFileSystem 为我们提供了访问本地文件系统及其文件和目录的能力。文件系统有两种类型：

1.  **LocalFileSystem.PERSISTENT：** 存储在持久文件系统中的数据，在没有用户明确授权的情况下，不应被用户代理（UA）删除，除非是响应移除 API 的调用。
2.  **LocalFileSystem.TEMPORARY：** 存储在临时文件系统中的数据，用户代理（UA）可以自行决定删除，无需应用程序或用户干预。

`localFileSystem` 方法可以从 `window` 对象访问。具体方式如下：

1.  `window.requestFileSystem()` – 用于获取对根文件系统的访问权限。
2.  `window.resolveLocalFileSystemURI()` – 用于直接获取对文件或目录的 FileEntry 或 DirectoryEntry 对象的访问权限，前提是该 URI 对应的目录或文件是可用的。

## fileSystem

`fileSystem` 代表了文件系统。它有两个主要属性：

1.  name – 两个选项 “PERSISTENT” 或 “TEMPORARY” 之间选择。如果你希望即使在应用被终止后文件仍然保留，就选择 “PERSISTENT”。
2.  root – 文件系统的根目录（DirectoryEntry）。

你需要使用以下 API 来获取对 `fileSystem` 的访问权限：

```javascript
void requestFileSystem (
    short type,  // LocalFileSystem.PERSISTENT 或
                //LocalFileSystem.TEMPORARY
    long long size, //临时文件系统 (FS) 的大小
    FileSystemCallback successCallback,  //成功回调
    optional ErrorCallback errorCallback);  //失败回调
```

获取对 `fileSystem` 访问权限的代码片段如下：

```javascript
window.requestFileSystem(LocalFileSystem.PERSISTENT
    ,0 //size
    ,function(fileSystem){ // 成功回调
        alert("Got FileSystem "+fileSystem);
    },
    function(err){ //失败回调
        alert("Got Error requesting FileSystem");
    }
);
```

你需要使用以下 API 来获取对 fileEntry 或 directoryEntry 对象（代表文件或目录的对象）的访问权限：

```javascript
void resolveLocalFileSystemURL (
                DOMString url,  //文件系统中文件或目录的 URL
                EntryCallback successCallback,  //成功回调
                optional ErrorCallback errorCallback); //失败回调
```

## fileEntry

为了操作文件，你需要一个 `fileEntry` 对象。获取 `fileEntry` 有多种方式，但如果你知道一个文件的 URI，可以这样获取该对象：

```javascript
window.resolveLocalFileSystemURL(
        "file:///sdcard/read-write.txt",
        function(fileEntry){
        },
        function(err){
        }
);
```

为了查阅 `fileEntry` 的所有属性和方法，你需要访问其附录。有两种方式可以获取此访问权限：

1.  `createWriter()`：创建一个 FileWriter 对象，可用于向文件写入内容。
2.  `file()`：创建一个包含文件属性的 File 对象，包括读取其内容。

## directoryEntry

为了列出目录中的文件，你需要一个 `directoryEntry` 对象。获取 `directoryEntry` 有多种方式，但如果你知道一个目录的 URI，可以这样获取该对象：

```javascript
window.resolveLocalFileSystemURL(
        "file:///sdcard/mydir/",
        function(directoryEntry){
        },
        function(err){
        }
);
```

为了查阅 `directoryEntry` 的所有属性和方法，你需要访问其附录。有一个方法可以获取此访问权限：`getFile()`：在给定目录中创建文件，或从给定目录中获取文件。

## 程序布局

我们的文件读写程序很简单。它包含一个 TextArea，我们在其中读取文件内容，或者将 TextArea 的内容写入文件。我们使用两个按钮——“读取”和“写入”——来读写一个名为 `read-write.txt` 的文件。

以下是该程序的代码。

```html
<!DOCTYPE HTML>
<html>
    <head>
        <title>PhoneGap</title>
        <script type="text/javascript" src="phonegap-1.1.0.js"></script>
        <script type="text/javascript">
            var filename = "read-write.txt";
            var filePath = "file:///sdcard/read-write.txt";
            var textarea = document.getElementById("textarea");
            /** 当 PhoneGap JavaScript 加载完成时调用 */
            function onDeviceReady(){
                var readButton = document.getElementById("read");
                var writeButton = document.getElementById("write");

                readButton.addEventListener("click", readFile, false);
                writeButton.addEventListener("click", saveFile, false);
            }

            function readFile(){
                //内容如下所示
            }

            function saveFile(){
                //内容如下所示
            }

            /** 当浏览器加载此页面时调用 */
            function init(){
                document.addEventListener("deviceready", onDeviceReady, false);
            }
        </script>
    </head>
    <body onLoad="init()">
        <h1>读写文件</h1>
        <table>
            <tr>
                <td colspan="2">
                    /sdcard/read-write.txt
                </td>
            </tr>
            <tr>
                <td colspan="2">
                    <textarea id="textarea" rows="10" cols="30"></textarea>
                </td>
            </tr>
            <tr>
                <td>
                    <button id="read">
                        读取
                    </button>
                </td>
                <td>
                    <button id="write">
                        写入
                    </button>
                </td>
            </tr>
        </table>
    </body>
</html>
```

这段代码运行后的效果如图 2–39 所示。

![图 2–39. 读写文件。](img/4a75e501abc949744a790d09257a5b1e_68_0.png)

现在，让我们来实现 `readFile()` 方法，以读取文件并将其内容显示在 TextArea 中。步骤非常简单：

1.  **步骤 1：** 解析 URL `file:///sdcard/read-write.txt`。
2.  **步骤 2：** 如果解析成功，使用 `fileEntry.file()` 方法创建一个 reader。
3.  **步骤 3：** 如果解析失败，向用户显示一条消息，告知用户需要先写入文件才能读取。参见图 2–40。



## 第2章：PhoneGap入门

```javascript
function readFile(){
    window.resolveLocalFileSystemURI(    //要读取的文件名
        filePath,    //成功回调
        function(fileEntry){
            fileEntry.file(
                function(file){
                    var fileReader = new FileReader();
                    fileReader.onloadend =
                    function(evt){
                        document.getElementById("textarea").value
                        = evt.target.result;
                    };
                    fileReader.readAsText(file);
                },
                function(error){
                    alert("读取时出错 "
                    +filePath);
                })
        },    //错误回调
        function(error){
            alert(filename + " 不存在，请先添加内容并点击"
            + "保存");
        }
    );
}
```

![img/4a75e501abc949744a790d09257a5b1e_69_0.png](img/4a75e501abc949744a790d09257a5b1e_69_0.png)

**图 2–40.** *无法读取，因为尚未写入任何文件。*

让我们实现 `writeFile()` 方法，以读取 TextArea 中的文本，并将其写入 `file:///sdcard/read-write.txt`。

步骤 1：访问文件系统根目录。

步骤 2：从文件系统根 DirectoryEntry 创建文件 `read-write.txt`（如果它不存在）。

步骤 3：创建 fileWriter 并将 TextArea 的内容写入文件。以下代码展示了这一点：

```javascript
function saveFile() {
    window.requestFileSystem(
        LocalFileSystem.PERSISTENT, 0,
        //成功回调
        function (fileSystem) {
            var sdcardEntry = fileSystem.root;
            sdcardEntry.getFile(
                filename,
                //指示创建文件的标志
                {
                    create: true
                },
                //成功回调
                function (fileEntry) {
                    fileEntry.createWriter(
                        function (fileWriter) {
                            fileWriter.onwrite = function (evt) {
                                alert("写入成功！");
                                document.getElementById("textarea").value = "";
                            };
                            fileWriter.write(document.getElementById("textarea").value);
                        },
                        //错误回调
                        function (error) {
                            alert("无法获取 " + filename + " 的文件写入器");
                        });
                },
                //错误回调
                function (error) {
                    alert("读取 " + filename + " 时出错 " + error);
                });
        }, function (error) {
            alert("访问文件系统时出错");
        });
}
```

当用户在 TextArea 中输入文本并点击“写入”时，内容将被写入文件，并显示一条提示消息，表示写入成功。你会注意到，当你点击“写入”时，程序会清空 TextArea。请参考图 2–41 查看文件写入成功时的消息。

![img/4a75e501abc949744a790d09257a5b1e_71_0.png](img/4a75e501abc949744a790d09257a5b1e_71_0.png)

**图 2–41.** *写入成功*

现在，尝试点击“读取”按钮来读取你写入文件的内容。你写入的内容应该会出现在 TextArea 中。请参考图 2–42 查看读取成功时文本区域填充的情况。

![img/4a75e501abc949744a790d09257a5b1e_72_0.png](img/4a75e501abc949744a790d09257a5b1e_72_0.png)

你可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/62c45e339662/android/PhoneGap-FileReadWrite 下载此示例的完整源代码。

你可以参考 File API 的官方文档：http://docs.phonegap.com/en/1.1.0/phonegap_file_file.md.html#File。

## 数据库的读写操作

本节将解释如何读取、存储和操作数据库。我们将以在数据库中存储一个联系人列表（firstName 和 lastName）为例，然后读取它并删除条目。

有三个表格：一个用于表头列，一个用于内容，还有一个允许用户向联系人列表中添加条目。

以下是用于数据库读写的 `index.html` 代码：

```html
<!DOCTYPE html>
<html>
    <head>
        <title>PhoneGap DB</title>
        <script type="text/javascript" src="phonegap-1.1.0.js">
        </script>
        <script type="text/javascript">
            var firstNameBox = null;
            var lastNameBox = null;
            var db = null;
            var dataTable = null;
            /** 当 phonegap javascript 加载时调用 */
            function onDeviceReady(){
                //内容将在下面显示
            }
            /** 当浏览器加载此页面时调用 */
            function init(){
                document.addEventListener("deviceready",
                                onDeviceReady, false);
            }
        </script>
        <style>
            td {
                width: 100px;
            }
            input {
                width: 100px;
            }
        </style>
    </head>
    <body onLoad="init()">
        <h3>数据库读写</h3>
        <table border="1">
            <tr>
                <td>
                    <b>名</b>
                </td>
                <td>
                    <b>姓</b>
                </td>
                <td>
                    <b>操作</b>
                </td>
            </tr>
        </table>
        <table id="data-table">
        </table>
        <table>
            <tr>
                <td>
                    <input id="firstName" type="text">
                    </input>
                </td>
                <td>
                    <input id="lastName" type="text">
                    </input>
                </td>
                <td>
                    <button id="add">
                        添加
                    </button>
                </td>
            </tr>
        </table>
    </body>
</html>
```

如果你运行此程序，应该会看到类似于图 2–43 所示的布局。

![img/4a75e501abc949744a790d09257a5b1e_74_0.png](img/4a75e501abc949744a790d09257a5b1e_74_0.png)

**图 2–43.** *从数据库读取和写入数据*

现在，让我们添加一些代码来从数据库读取、写入和删除联系人条目。
第一步是获取数据库对象的访问权限。操作如下：

```javascript
var firstNameBox = null;
var lastNameBox = null;
var db = null;
var dataTable = null;
/** 当 phonegap javascript 加载时调用 */
function onDeviceReady(){
    var addButton = document.getElementById("add");
    firstNameBox = document.getElementById("firstName");
    lastNameBox = document.getElementById("lastName");
    dataTable = document.getElementById("data-table");

    db = window.openDatabase("contactDB", "1.0", "联系人数据库", 1000000);
    //名称, 版本, 显示名称, 大小
}
```

让我们重点关注用于创建数据库对象的 API。操作如下：

```javascript
window.openDatabase(
    databaseName,
    versionNumber,
    displayName,
    sizeInBytes);
```

现在让我们看看下面的代码（参见 `addButton.addEventListener` 部分），它解释了点击“添加”按钮并向数据库中的联系人表添加条目的过程。

为了向联系人表添加条目，我们将使用数据库对象上的 `transaction()` 方法。以下是此方法的 API：

```javascript
db.transaction(
    function(tx){ //执行 sql 语句的函数
        //使用 tx 执行 sql 语句
    },
    function(err){ // 错误回调
        //使用 err.code 和 err.message 来理解错误
    },
    function(){ //成功回调
        // 更新 UI，记录日志消息
    }
);
```

我们希望在用户点击按钮时添加新条目。因此，我们的添加功能位于“添加”按钮的点击事件监听器中。以下代码展示了这一点：

```javascript
addButton.addEventListener(
    "click",
    function(){
        db.transaction(
            //sql 语句函数
            function (tx){
                ensureTableExists(tx);
                var firstName = firstNameBox.value;
                var lastName = lastNameBox.value;

                var sql = 'INSERT INTO Contacts '
                    + '( firstName, lastName ) VALUES '
                    + '("' + firstName + '","' + lastName + '")';

                tx.executeSql(sql);
            },
            //错误回调
            function (err){
                alert("错误回调 "+err.code);
            },
            //成功回调
            function (){
                loadFromDB();
            }
        );
    }
);
```



## 第2章：PhoneGap入门

```javascript
);

},false);

function ensureTableExists(tx){
    tx.executeSql("CREATE TABLE IF NOT EXISTS Contacts (id INTEGER PRIMARY KEY, firstName,lastName)");

}
```

我们使用了一个名为`ensureTableExists(tx)`的方法，该方法确保在进行数据库CRUD（增删改查）操作之前，数据库表是存在的。

我们使用SQL插入语句（insert statement）来在数据库事务的SQL函数中向数据库添加一条记录。

> 注意：SQLite中的主键默认是自增的，因此我们只需要写入`firstName`和`lastName`，数据库实际上会自动递增ID。

一旦数据库成功添加了操作，我们就会调用`loadFromDB()`方法，从数据库表中填充HTML表格。

请参考图2-44查看“添加联系人”功能的UI界面。

![](img/4a75e501abc949744a790d09257a5b1e_76_0.png)

现在，让我们来看看`loadFromDB()`方法。这里我们使用了相同的`tx.executeSql`，但在这种情况下，我们期望得到一些不同的结果，所以我们使用了`tx.executeSql`的以下版本：

```javascript
tx.executeSql(
    sqlStatement,
    options,
    successCallbackWithResultSet,
    errorCallback);
```

`successCallbackWithResultSet`是一个函数，它接收两个参数：

+   1. tx
2. 结果集（resultset）

```javascript
function loadFromDB(){
    db.transaction(
        //function sql statements
        function (tx){
            ensureTableExists(tx);
            tx.executeSql('SELECT * FROM Contacts',
                [],
                //success callback
                function(tx, results){
                    var htmlStr="";
                    for(var index=0;index<results.rows.length;index++){
                        var item = results.rows.item(index);
                        htmlStr = htmlStr +"<tr><td>"+
                            item.firstName+"</td><td>"
                            +item.lastName
                            +"</td><td><button
                            onclick=\"deleteEntry('"
                            +item.id+
                            "')\">X</button></td></tr>";
                    }
                    dataTable.innerHTML=htmlStr;
                },
                //error callback
                function(err){
                    alert("Unable to fetch result from Contacts Table");
                }
            );
        },
        //error callback
        function (err){
            alert("error callback "+err.code+" "+err.message);
        },
        //success callback
function (){
    firstNameBox.value="";
    lastNameBox.value="";
});
```

现在运行代码，我们可以在HTML表格中看到之前添加的条目。参考图2-45，它显示了HTML表格中之前添加的行。

![](img/4a75e501abc949744a790d09257a5b1e_78_0.png)

**图2-45。** *从数据库中读取所有条目*

最后要做的事情是在用户点击X按钮时删除条目。当填充HTML表格时，我们在HTML中定义了按钮如下：

```html
<button onclick="deleteEntry('"+item.id+"');">X</button>
```

参考图2-46查看其在HTML中的样子。

当用户点击X按钮时，`deleteEntry`函数被调用，并传递要删除的条目的主键。这里，我们使用DELETE SQL语句来删除指定主键的记录。

```javascript
function deleteEntry(id){
    db.transaction(
        //function sql statements
        function (tx){
            ensureTableExists(tx);

            tx.executeSql('Delete FROM Contacts where id='+id);

        },
        //error callback
        function (err){
            alert("error callback "+err.code+" "+err.message);

        },
        //success callback
        function (err){
            loadFromDB();
        }

    );
}
```

![](img/4a75e501abc949744a790d09257a5b1e_79_0.png)

**图2-46。** 从数据库中删除条目

现在，当用户点击X按钮时，条目被删除，并调用`loadFromDB()`，从数据库表刷新HTML表格。

![](img/4a75e501abc949744a790d09257a5b1e_80_0.png)

**图2-47。** *删除条目已反映*

完整的`index.html`源代码如下所示：

```html
<!DOCTYPE HTML>
<html>

    <head>
        <title>
            PhoneGap DB
        </title>
        <script type="text/javascript" src="phonegap-1.1.0.js">

        </script>
        <script type="text/javascript">
                                    var firstNameBox = null;
            var lastNameBox = null;
            var db = null;
            var dataTable = null; /** Called when phonegap javascript is loaded */

            function onDeviceReady() {
                var addButton = document.getElementById("add");
                firstNameBox = document.getElementById("firstName");
                lastNameBox = document.getElementById("lastName");
                dataTable = document.getElementById("data-table");

                db = window.openDatabase("contactDB",
                    "1.0",
                    "Contact Database",
                    1000000); //name,version,display name, size
                addButton.addEventListener("click", function() {

                    db.transaction(
                        //function sql statements
                        function(tx) {
                            ensureTableExists(tx);
                            var firstName = firstNameBox.value;
                            var lastName = lastNameBox.value;

                            var sql = 'INSERT INTO Contacts (firstName, lastName) VALUES (''"' + firstName + '"","'"' + lastName + "'")";
                            tx.executeSql(sql);
                        },
                        //error callback
                        function(err) {
                            alert("error callback " + err.code);
                        },
                        //success callback
                        function(err) {
                            //alert("success callback "+err.code);
                            loadFromDB();
                        }
                    );
                }, false);
                loadFromDB();

            }

            function loadFromDB() {

                db.transaction(
                    //function sql statements
                    function(tx) {
                        ensureTableExists(tx);
                        tx.executeSql('SELECT * FROM Contacts', [], function(tx, results) {
                            var htmlStr = "";
                            for (var index = 0; index < results.rows.length; index++) {
                                var item = results.rows.item(index);
                                htmlStr = htmlStr
                                + "<tr><td>"
                                + item.firstName
                                + "</td><td>"
                                + item.lastName
                                + "</td><td><button onclick=\"deleteEntry("
                                + item.id
                                + ");\">X</button></td></tr>";
                            }
                            dataTable.innerHTML = htmlStr;
                        }, function(err) {
                            alert("Unable to fetch result from Contacts Table");
                        });

                    },
                    //error callback
                    function(err) {
                        alert("error callback " + err.code + " " + err.message);

                    },
                    //success callback
                    function() {
                        firstNameBox.value = "";
                        lastNameBox.value = "";

                    });

            }

            function deleteEntry(id) {
                db.transaction(
                    //function sql statements

                    function(tx) {
                        ensureTableExists(tx);
                        tx.executeSql('Delete FROM Contacts where id=' + id);

                    },
                    //error callback

                    function(err) {
                        alert("error callback " + err.code + " " + err.message);

                    },
                    //success callback

                    function(err) {
                        //alert("success callback ");
                        loadFromDB();

                    });

            }

            function ensureTableExists(tx) {
                tx.executeSql('CREATE TABLE IF NOT EXISTS Contacts (id INTEGER PRIMARY KEY, firstName,lastName)');

            } /** Called when browser load this page*/

            function init() {
                document.addEventListener("deviceready", onDeviceReady, false);
            }
        </script>
        <style>
            td { width: 100px; } input { width: 100px; }
        </style>
    </head>

    <body onLoad="init()">
        <h3>
            Read Write DB
        </h3>
        <table border="1">
            <tr>
                <td>
                    <b>
                        First Name
                    </b>
                </td>
                <td>
                    <b>
                        Last Name
                    </b>
                </td>
                <td>
                    <b>
                        Action
                    </b>
                </td>
            </tr>
        </table>
        <table id="data-table">
        </table>
        <table>
            <tr>
                <td>
                    <input id="firstName" type="text">
                </td>
                <td>
                    <input id="lastName" type="text">
                </td>
                <td>
                    <button id="add">
                        Add
                    </button>
                </td>
            </tr>
        </table>
    </body>
</html>
```

您可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/62c45e339662/android/PhoneGap-DB 下载此示例的完整源代码。



你可以参考 Storage API 的官方文档，网址为 http://docs.phonegap.com/en/1.1.0/phonegap_storage_storage.md.html#Storage。

## 获取蜂窝设备或 Wi-Fi 网络的详细信息

移动应用通常需要连接服务器以获取某些数据。现代智能手机可能通过 3G/4G 网络或 Wi-Fi 网络下载数据。一款优秀的应用应当尊重这种区别，在 3G/4G 网络下仅下载特定类型的数据，而在 Wi-Fi 网络下才下载大流量数据。

本节将解释如何使用 PhoneGap 来查明智能手机正在使用哪种网络。

我们需要使用以下 API：

`navigator.network.connection.type`

该 API 返回连接类型。不同连接类型的值如下所示：

```
Connection.UNKNOWN = "unknown";
Connection.ETHERNET = "ethernet";
Connection.WIFI = "wifi";
Connection.CELL_2G = "2g";
Connection.CELL_3G = "3g";
Connection.CELL_4G = "4g";
Connection.NONE = "none";
```

index.html 的完整源代码如下：

```
<!DOCTYPE HTML>
<html>
<head>
    <title>PhoneGap DB</title>
    <script type="text/javascript" src="phonegap-1.1.0.js">
    </script>
    <script type="text/javascript">

        /** Called when phonegap javascript is loaded */
        function onDeviceReady(){
            fetchNetworkConnectionInfo();
        }

        function fetchNetworkConnectionInfo(){

            var networkType = navigator.network.connection.type;

            var networkTypes = {};

            networkTypes[Connection.NONE]     = 'No network connection';
            networkTypes[Connection.UNKNOWN]  = 'Unable to identify Network Connection Type';
            networkTypes[Connection.CELL_2G]  = '2g network';
            networkTypes[Connection.CELL_2G]  = 'Network Connection is of type 2G';
            networkTypes[Connection.CELL_3G]  = 'Network Connection is of type 3G';
            networkTypes[Connection.CELL_4G]  = 'Network Connection is of type 4G';
            networkTypes[Connection.WIFI]     = 'Network Connection is of type WiFi';
            networkTypes[Connection.ETHERNET] = 'Network Connection is of type Ethernet';

            document.getElementById("network-status").innerHTML
                = networkTypes[networkType];
        }

        /** Called when browser load this page*/
        function init(){
            document.addEventListener("deviceready",
                onDeviceReady, false);
        }
    </script>
</head>
<body onLoad="init()">
    <h3>Phone Network Info</h3>
    <div id="network-status">
    </div>
</body>
</html>
```

运行这段代码后，将显示如图 2-48 所示的网络信息。

![](img/4a75e501abc949744a790d09257a5b1e_86_0.png)

*图 2-48. PhoneGap 网络信息显示网络连接类型为 3G*

你可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/67848b004644/android/PhoneGap-Network 下载本示例的完整源代码。

你可以参考 Connection API 的官方文档，网址为 http://docs.phonegap.com/en/1.1.0/phonegap_connection_connection.md.html#Connection。

## 设备示例

鉴于这些特性的性质，以下示例只能在真实的 Android 设备上运行。Android 模拟器不支持以下功能。

### 获取地理位置

在本示例中，我们将尝试获取设备的地理位置。为此，我们将使用 navigator.geolocation API。该 API 是一个异步 API，这意味着一旦我们向该 API 请求地理位置，API 将通知调用程序，并使用注册到该 API 的两个回调函数之一。

调用的 API 如下：

```
navigator.geolocation.getCurrentPosition(onynchronized, onErrorCallback);
```

当 API 能够获取 GPS 坐标时，会调用 onSuccessCallback 函数。当获取 GPS 坐标出现问题时，API 会调用 onErrorCallback。

onSuccessCallback 将接收一个名为 position 的参数。position 包含有关地理位置的详细信息，如表 2-3 所示。

*表 2-3. PhoneGap 地理定位 API 的 Position 对象详解*

| Position result | Description |
| --- | --- |
| position.coords.latitude | 十进制度数的纬度 |
| position.coords.longitude | 十进制度数的经度 |
| position.coords.altitude | 十进制度数的海拔 |
| position.coords.accuracy | 纬度和经度的精度，单位为米 |
| position.coords.altitudeAccuracy | 海拔的精度，单位为米 |
| position.coords.heading | 行进方向，以正北方向顺时针度数表示 |
| position.coords.speed | 行进速度，单位为米每秒 |
| position.timestamp | GPS 坐标的创建时间戳 |

该示例的完整代码如下：

```
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript">
      /** Called when phonegap javascript is loaded */
      function onDeviceReady(){
          navigator.geolocation.getCurrentPosition(onSuccess, onError);
      }

      function onSuccess(position) {
          document.getElementById('latitude').innerHTML = position.coords.latitude;
          document.getElementById('longitude').innerHTML = position.coords.longitude;
          document.getElementById('altitude').innerHTML = position.coords.altitude;
          document.getElementById('timestamp').innerHTML = new Date(position.timestamp);
      }

      function onError(error) {
          alert('code: ' + error.code + '\n' + 'message: ' + error.message + '\n');
      }

      /** Called when browser load this page*/
      function init(){
          document.addEventListener("deviceready", onDeviceReady, false);
      }
    </script>
  </head>
  <body onLoad="init()">
    <h1>GeoLocation</h1>
    <table border="1">
        <tr> <td>Latitude</td> <td id="latitude"></td> <tr>
        <tr> <td>Longitude</td> <td id="longitude"></td> <tr>
        <tr> <td>Altitude</td> <td id="altitude"></td> <tr>
        <tr> <td>Timestamp</td> <td id="timestamp"></td> <tr>
    </table>
  </body>
</html>
```

这段代码如图 2-49 所示。

![](img/4a75e501abc949744a790d09257a5b1e_88_0.png)

**图 2-49.** PhoneGap 地理位置运行示例

你可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/67848b004644/android/PhoneGap-GeoLocation 下载本示例的完整源代码。

你可以参考 Geolocation API 的官方文档，网址为 http://docs.phonegap.com/en/1.1.0/phonegap_geolocation_geolocation.md.html#Geolocation。

### 获取加速计读数

在本示例中，我们将尝试监测设备的加速计读数。现代智能手机中的加速计功能为用户提供其在 x、y 和 z 坐标系中的运动方向。

调用的 API 如下：

```
navigator.accelerometer.watchAcceleration(onSuccessCallback, onErrorCallback, accelerometerOptions);
```

该 API 将持续监测加速计读数，并在定义的间隔内重复调用 onSuccessCallback，直到调用 navigator.accelerometer.clearWatch() 为止。间隔在 accelerometerOptions 中定义，以 `{"frequency":"3000"}` 的形式提供值。间隔的单位为毫秒。如果 accelerometerOptions 未提供该值，则使用默认的 1000 毫秒间隔。

如前所述，当获取加速计读数出现问题时，API 会调用 onErrorCallback。

onSuccessCallback 将接收一个名为 acceleration 的参数。acceleration 包含有关设备运动的详细信息，如表 2-4 所示。

*表 2-4. 加速计 Acceleration 对象详解*

| Acceleration | Description |
|---|---|
| x | 绕 x 轴的运动，数值范围为 0-1 |
| y | 绕 y 轴的运动，数值范围为 0-1 |
| z | 绕 z 轴的运动，数值范围为 0-1 |
| timestamp | 设备运动的创建时间戳 |

该示例的完整代码如下：

```
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript">
      /** Called when phonegap javascript is loaded */
    </script>
```



function onDeviceReady(){
    var options = { frequency: 1000 }; // 每秒更新1次
    navigator.accelerometer.watchAcceleration(onSuccess,
                                              onError,options);
}

function onSuccess(acceleration) {
    document.getElementById('x').innerHTML = acceleration.x;
    document.getElementById('y').innerHTML = acceleration.y;
    document.getElementById('z').innerHTML = acceleration.z;
    document.getElementById('timestamp').innerHTML
        = acceleration.timestamp;
}

function onError(error) {
    alert('code: '    + error.code    + '\n' +
              'message: ' + error.message + '\n');
}

/** 当浏览器加载此页面时调用 */
function init(){
    document.addEventListener("deviceready", onDeviceReady, false);
}
</script>
</head>
<body onLoad="init()">
    <h1>加速度计</h1>
    <table border="1">
        <tr>  <td>X</td>                  <td id="x"></td>           <tr>
        <tr>  <td>Y</td>                  <td id="y"></td>           <tr>
        <tr>  <td>Z</td>                  <td id="z"></td>           <tr>
        <tr>  <td>时间戳</td>  <td id="timestamp"></td>  <tr>
    </table>
    </ul>
</body>
</html>

此代码在图2-50中说明。

![](img/4a75e501abc949744a790d09257a5b1e_91_0.png)

## **图2–50。*PhoneGap 加速度计示例***

同一加速度计的图形版本见图2–51。通过将手机平放在表面上，加速度计可用于检查表面是否水平。

你可以在 http://code.google.com/p/beginningphonegap/downloads/list 找到此示例的图形资源。

![](img/4a75e501abc949744a790d09257a5b1e_92_0.png)

图2–51。使用 PhoneGap 加速度计 API 构建的气泡应用

上一个示例中使用了四张图片。这些图片从圆形气泡到椭圆形气泡不等。代码的完整示例如下所示：

```
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript">
      /** 当 phonegap javascript 加载完成时调用 */
      function onDeviceReady(){
          var options = { frequency: 0100 }; // 每秒更新1次
          navigator.accelerometer.watchAcceleration(onSuccess,
                                                    onError,options);
      }

      function onSuccess(acceleration) {
          moveX(acceleration);
          moveXY(acceleration);
      }

      function moveXY(acceleration){

          var xyBase = document.getElementById("x-y-base");
          var circle = document.getElementById("circle");
          var position = getPos(xyBase);
          var adjustX = 20;
var adjustY = 20;
var radius = 160;
var left = position.x;
var top  = position.y;
var width  = xyBase.clientWidth;
var height = xyBase.clientHeight;

var centerX = left + width/2 - adjustX;
var centerY = top + height/2 - adjustY;
centerY = centerY - (radius * acceleration.y *  1.2) /10;
centerX = centerX - (radius * acceleration.x * -1.2) /10;

circle.style.left=centerX+"px";
circle.style.top=centerY+"px";
```

```
function moveX(acceleration){
    //FIXME 移动局部变量使其成为全局变量
    var xBase = document.getElementById("x-base");
    var oval = document.getElementById("oval");
    var basePosition = getPos(xBase);

    var ovalLeft = basePosition.x + (xBase.clientWidth/2) -
        (xBase.clientWidth * acceleration.x * -1)/10;

    if( ( ovalLeft + oval.clientWidth )>
        (xBase.clientWidth+basePosition.x) ){
        ovalLeft = xBase.clientWidth + basePosition.x -
            oval.clientWidth;
    }
    if (ovalLeft < basePosition.x){
        ovalLeft = basePosition.x;
    }
    oval.style.left=ovalLeft+"px";
}
```

```
function onError(error) {
    alert('code: '    + error.code    + '\n' +
          'message: ' + error.message + '\n');
}
```

```
/** 当浏览器加载此页面时调用 */
function init(){
    document.addEventListener("deviceready", onDeviceReady, false);
}
```

```
function getPos(el) {
    var position = {};
    if (document.getBoxObjectFor) {
        var bo = document.getBoxObjectFor(el);
        position.x = bo.x;
        position.y = bo.y;
    }
    else {
        var rect = el.getBoundingClientRect();
        position.x = rect.left;
        position.y = rect.top;
    }
return position;
}
</script>
</head>
<body onLoad="init()">
  <h1>加速度计</h1>

  <div id="horizontal-bubble">
    <img id="circle" src="accelerometer-circle-bubble.png"
      style="position:absolute"></img>
    <img id="x-y-base" src="x-y-accelerator-base.png"></img>
  </div>

  <div id="vertical-bubble">
    <img id="x-base" src="z-accelerator-base.png"></img>
    <img id="oval" src="accelerometer-circle-oval.png"
      style="position:absolute;left:0px"></img>
  </div>

</body>
</html>
```

你可以从 https://bitbucket.org/rohitghatol/apress-phonegap/src/67848b004644/android/PhoneGap-Accelerometer-Image 下载此示例的完整源代码。

你可以参考 Accelerometer API 的官方文档：http://docs.phonegap.com/en/1.1.0/phonegap_accelerometer_accelerometer.md.html#Accelerometer。

# 获取指南针方位

现在让我们转向一个与加速度计功能类似的应用程序：指南针。与加速度计一样，指南针以 x、y 和 z 轴的度数提供设备运动信息。指南针以度数提供设备相对于真北顺时针方向的航向。

你可以在 http://code.google.com/p/beginningphonegap/ 找到此示例的图形资源。

调用的 API 如下：

```
navigator.compass.watchHeading (onSuccessCallback, onErrorCallback,compassOptions);
```

此 API 将持续监测指南针指向的方向，并按照预定义的时间间隔调用 onSuccessCallback，直到调用 `navigator.compass.clearwatch()`。该间隔在 `compassOptions` 中定义，并以 `{"frequency":"3000"}` 的形式提供一个值。间隔的单位是毫秒。如果未提供 `compassOptions`，则使用默认的 1000 毫秒间隔。

如前面的示例所述，当获取 GPS 坐标出现问题时，API 将调用 `onErrorCallback`。

`onSuccessCallback` 将获得一个名为 `heading` 的参数。航向是一个介于 0 到 360 之间的度数，它从真北开始按顺时针方向测量。

完整的示例如下。此示例使用 CSS3 来直观地显示一个指南针。为此，我们使用了一个指南针指针图像。该图像如图2–52所示。

![](img/4a75e501abc949744a790d09257a5b1e_95_0.png)

图2–52。PhoneGap 示例中使用的指南针图像

首先，我们使用 `navigator.compass.watchHeading()` 方法注册我们的 `onSuccess` 方法。当我们的 `onsuccess` 方法被调用时，我们使用 CSS3 旋转变换来改变指南针图像指向的方向。这是一个可视化的指南针应用程序。

此应用程序的完整 `index.html` 如下所示：

```
<!DOCTYPE HTML>
<html>
  <head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript">
      /** 当 phonegap javascript 加载完成时调用 */
      function onDeviceReady(){
        var button = document.getElementById("capture");
        var compassOptions = { frequency: 1000 };
        navigator.compass.watchHeading(onSuccess, onError,
                                       compassOptions);
      };

      function onSuccess(heading) {
        var image = document.getElementById('compass');
        var headingDiv = 
          document.getElementById('compassHeading');
        headingDiv.innerHTML=heading;
        var reverseHeading = 360 - heading;
        image.style.webkitTransform = 
          "rotate("+reverseHeading+"deg)";
      }

      function onError(error) {
        alert('code: '    + error.code    + '\n' + 'message: ' + error.message + '\n');
      }
    </script>
  </head>
```



## 从摄像头捕获图像

本章的最后一节是关于从摄像头捕获图像。这是一个很酷的功能，确实为基于HTML的应用增添了很多价值。让我们看看如何使用这个功能。

调用的API如下：

`navigator.camera.getPicture (onSuccessCallback, onErrorCallback,cameraOptions);`

虽然cameraOptions中有很多选项，但我们将重点关注一个名为quality的属性。cameraOption看起来像`{"quality":75}`。

使用上述cameraOptions，`onSuccess()`方法将获取一个base64编码的二进制图像。

Camera应用程序的完整示例如下：

```
<!DOCTYPE HTML>
<html>
    <head>
        <title>PhoneGap</title>
        <script type="text/javascript" src="phonegap-1.1.0.js"></script>
        <script type="text/javascript">
            /** 当phonegap javascript加载完成时调用 */
            function onDeviceReady(){
                var button = document.getElementById("capture");
                button.addEventListener("click",captureImage,false);
            }

            function captureImage(){
                var cameraOptions = { quality: 50 };
                navigator.camera.getPicture( onSuccess, onError,
                                            cameraOptions );
            };

            function onSuccess(imageData) {
                var image = document.getElementById('cameraImage');
                image.src = "data:image/jpeg;base64," + imageData;
            }

            function onError(error) {
                alert('code: ' + error.code + '\n' + 'message: ' + error.message + '\n');
            }

            /** 当浏览器加载此页面时调用 */
            function init(){
                document.addEventListener("deviceready", onDeviceReady, false);
            }
        </script>
    </head>
    <body onLoad="init()">
        <h1>Camera</h1>
        <button id="capture">Capture Image</button>
        <img id="cameraImage"></img>
    </body>
</html>
```

这段代码在图2–54和图2–55中进行了说明。

![](img/4a75e501abc949744a790d09257a5b1e_98_0.png)

**图2–54.** PhoneGap Camera应用程序显示“捕获图像”按钮

![](img/4a75e501abc949744a790d09257a5b1e_99_0.png)

**图2–55.** 图像捕获后的PhoneGap Camera应用程序

您可以从https://bitbucket.org/rohitghatol/apress-phonegap/src/67848b004644/android/PhoneGap-Camera下载此示例的完整源代码。

您可以参考Camera API的官方文档：http://docs.phonegap.com/en/1.1.0/phonegap_camera_camera.md.html#Camera。

# 第3章
## 设置环境

PhoneGap环境可以通过以下两种方式设置：

- 您的机器上的本地开发环境
- PhoneGap Build上的云端构建环境

本地开发环境设置包括开发人员为希望启动PhoneGap应用程序的每个移动平台设置环境。本章详细介绍了本地环境设置，并希望读者无需其他文档即可在每个平台的模拟器上运行PhoneGap应用程序。

为了在特定平台的设备上运行PhoneGap应用程序，用户需要查看平台特定的文档。本章提供了这些文档的参考。

另一方面，名为“PhoneGap Build”的云端构建环境允许您在无需本地开发环境的情况下构建PhoneGap应用程序。这意味着开发人员只需编写应用程序中需要HTML、JavaScript和CSS的PhoneGap部分代码。然后，此代码将提供给PhoneGap Build服务。PhoneGap Build服务将为每个平台构建所需的二进制文件，开发人员可以下载这些文件。我们将在本章更详细地探讨这个过程。

## 本地开发环境

本地开发环境与我们在第2章中为Android所做的类似。在本章中，我们将看到如何在以下平台的开发机器上设置PhoneGap环境：

1. iOS
2. BlackBerry
3. Symbian
4. webOS

需要注意的是，iOS只能在Mac上使用Xcode构建，而BlackBerry的首选操作系统是Windows。

## 先决步骤

在进一步操作之前，我们将预先完成所有平台的共同步骤。第一步是下载PhoneGap。

## 下载PhoneGap

您可以从www.phonegap.com下载PhoneGap SDK。本书使用的是PhoneGap 1.1.0版本，这是当时的最新版本。

下载PhoneGap SDK并解压缩后，您将看到如图3–1所示的文件夹结构。

![](img/4a75e501abc949744a790d09257a5b1e_101_0.png)

PhoneGap支持的每个平台都有一个单独的目录。每个目录包含用于帮助设置本地开发环境的该平台的库、工具和源代码。

## 使用Xcode 4设置iOS环境

为了使用iOS，您将需要一台基于Intel的Mac OS X Snow Leopard (10.6)计算机。

您还需要以下条件才能在设备上测试您的PhoneGap应用程序：

1. Apple设备，如iPhone、iPad或iPod Touch
2. iOS开发者账户和证书

接下来，您需要执行以下安装步骤：

1. 安装Xcode和PhoneGap。Xcode安装程序可以从http://developer.apple.com/xcode/index.php（Apple开发者门户）下载。请注意，您需要一个Apple开发者账户。或者，您可以从iTunes购买并下载Xcode 4，费用约为5美元。
2. 导航到您解压PhoneGap SDK的iOS目录。运行PhoneGap安装程序直到完成。
3. 创建一个新的PhoneGap项目。打开Xcode并创建一个新项目。这将显示以下对话框。选择“PhoneGap Based Application”选项，然后单击“下一步”按钮（参见图3–2）。

![](img/4a75e501abc949744a790d09257a5b1e_102_0.png)

**图3–2.** 创建一个新的iOS PhoneGap项目

4. 在下一个屏幕（如图3–3所示）上，为项目创建向导提供产品名称和公司标识符。单击“下一步”。

![](img/4a75e501abc949744a790d09257a5b1e_103_0.png)

**图3–3.** 创建一个新的iOS PhoneGap项目

5. 为项目选择适当的目录，然后单击“创建”按钮。

Xcode提供了一个为项目创建git仓库的选项。可以通过单击图3–4所示的“源代码管理”复选框来启用或禁用此功能。

![](img/4a75e501abc949744a790d09257a5b1e_104_0.png)

**图3–4.** 创建一个新的iOS PhoneGap项目

现在您应该在Xcode中看到HelloWorld项目。

### 输入PhoneGap的HTML和JavaScript

请注意，我们的项目中没有www文件夹。要创建www文件夹，请单击Xcode左上角的“运行”按钮。它将构建项目并在模拟器中启动它。不用担心模拟器中显示“未找到index.html”的错误。这是预期的，因为我们还没有将HTML放入文件中。

2. 在Finder中打开项目（参见图3–5）。



你将在项目文件夹旁边看到一个www文件夹。我们需要将这个文件夹复制到Xcode项目中。

1.  将www文件夹拖放到Xcode中。Xcode现在会提示几个选项。为所有添加的文件夹选择“Create Folder References”，然后点击“Finish”按钮。现在你应该能在Xcode中看到如图3-6所示的项目结构。

*图3–6.* iOS项目中的PhoneGap WWW文件夹

2.  编写PhoneGap应用程序

你可以通过修改`index.html`文件来编写PhoneGap应用程序。要打开`index.html`，请打开www文件夹，然后在编辑器中打开`index.html`页面。
在`index.html`文件中输入你的内容。你也可以在`index.html`页面中指定相关的Javascript和CSS文件。

3.  部署到模拟器。确保在左上角的菜单中选择了“Simulator”版本作为“Active SDK”。

4.  点击Xcode项目标题栏中的“Run”按钮来构建项目并在模拟器中启动应用程序（参见图3–7）。

**图3–7.** *在iOS上运行的PhoneGap示例应用程序*

### 部署到设备
你可以在开发者设备上启动PhoneGap应用程序。为了在设备上运行应用程序，打开`HelloWorld-info.plist`并更改**BundleIdentifier**。如果你有开发者许可证，可以从Apple获取BundleIdentifier。
2.  确保在左上角的菜单中选择了“Device”版本作为“Active SDK”，然后点击Xcode项目标题栏中的“Run”按钮。它将构建项目并在设备上启动应用程序。

## 设置黑莓环境

你需要一台基于Intel、运行Windows XP（32位）或Windows 7（32位和64位）的计算机来处理黑莓开发。你需要在PC上安装以下软件：

1.  Java SE 6 JDK 32位
2.  Apache Ant
3.  BlackBerry WebWorks SDK v2.0+
4.  任何Java IDE环境
5.  拥有黑莓开发者区域的账户
6.  安装J2SDK 6（32位）

你可以从http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html下载J2SDK。运行J2SDK安装程序直至完成。将`Installation_directory/J2SDK/bin`添加到PATH环境变量中。

接下来，你需要执行以下安装步骤：

1.  安装Apache Ant

你可以从http://ant.apache.org/bindownload.cgi下载Apache Ant包。Apache Ant包是一个zip文件。解压ant zip文件，并将**解压后的目录/apache-ant-1.8.2/bin**放入PATH环境变量中。

2.  安装黑莓SDK

从https://bdsc.webapps.blackberry.com/html5/download/sdk网站下载适用于智能手机的BlackBerry WebWorks SDK。运行黑莓安装程序直至完成。通常，BlackBerry WebWorks SDK安装程序会将文件安装在`C:\BBWP`文件夹中。如果你将其更改为其他目录，请记住安装路径，因为稍后步骤中需要使用它。我们建议使用路径“c:\BBWP”，因为本章剩余部分将使用该路径。

3.  创建新的PhoneGap项目

为了创建黑莓PhoneGap应用程序，PhoneGap框架提供了一个ant脚本。

导航到PhoneGap黑莓目录

在命令提示符中运行 `ant create –Dproject.path=C:\Dev\Sample` 命令

请注意，如果你无法运行上述命令，请尝试从https://github.com/callback/callback-blackberry/downloads下载PhoneGap的黑莓回调，并将其解压到PhoneGap的BlackBerry-WebWorks目录中。

这将创建如图3–9所示的项目文件夹。注意www文件夹。此文件夹包含html文件和PhoneGap JavaScript文件。

www.it-ebooks.info

图3–9. 黑莓PhoneGap项目目录结构

你必须将**project.properties**文件中**bbwp.dir**属性的值更改为`C:\\BBWP`。如果你在安装期间更改了黑莓安装目录，如步骤3所述，请确保为**bbwp.dir**属性输入相同的目录（参见图3–10）。

图3–10. 配置project.properties指向BlackBerry Works SDK目录

4.  编写PhoneGap应用程序

编写PhoneGap应用程序就像修改`index.html`文件一样简单。要打开`index.html`，请打开www文件夹，并在你最喜欢的编辑器中打开`index.html`页面。在`index.html`文件中包含你的CSS和JavaScript文件。

5.  部署到模拟器

在黑莓模拟器上部署需要以下步骤。

-   启动黑莓模拟器，运行如下所示的ant target。这将启动黑莓模拟器

```
C:\Dev\Sample>ant load-simulator
```

-   在模拟器上选择BlackBerry按钮

-   选择Downloads文件夹

在那里你将看到PhoneGap示例应用程序。选择它以打开它（参见图3-11）。

www.it-ebooks.info

图3–11. *从黑莓模拟器的Downloads运行PhoneGap应用*

6.  部署到设备

为了在黑莓设备上部署PhoneGap应用程序，你需要从RIM获取签名密钥。你可以使用以下站点获取签名密钥https://www.blackberry.com/SignedKeys。

导航到你的项目目录，并在命令提示符中运行以下ant命令：

```
C:\Dev\Sample>ant load-device
```

## 设置塞班环境

为了使用塞班，你需要一台基于Intel、运行Windows操作系统的计算机。尽管PhoneGap的官方文档声称塞班应用程序可以在所有操作系统上开发，但我们建议在Windows上使用Nokia Symbian S60 SDK来测试在塞班模拟器上运行的PhoneGap应用程序。

接下来，你需要执行以下安装步骤：

1.  安装Cygwin
为了设置塞班环境，我们需要在Windows上安装Cygwin。从http://cygwin.com/install.html下载`Cygwin.exe`文件并开始安装直至完成。请注意，在安装Cygwin时，你必须选择两个包，即zip和make包。

2.  安装Symbian S60 SDK
从http://www.forum.nokia.com/info/sw.nokia.com/id/ec866fab-4b76-49f6-b5a5-af0631419e9c/S60_All_in_One_SDKs.html下载Symbian S60 SDK。请注意，此SDK大约800多MB，安装需要大约3GB以上的空间。安装大约需要30多分钟。

3.  创建新的PhoneGap项目
PhoneGap目录中有一个名为Symbian的文件夹；此目录是一个模板项目。为了创建新的塞班PhoneGap项目，只需复制此目录并将其粘贴到你希望创建新塞班PhoneGap项目的位置。此目录的内容如图3–12所示。

4.  编写PhoneGap应用程序
打开www文件夹，并在你最喜欢的编辑器中打开`index.html`。根据需要编辑HTML内容并包含CSS和JavaScript。

5.  部署到模拟器
塞班PhoneGap使用makefile来构建项目。在Mac或Linux机器上，只需在终端中运行`make`即可构建。在Windows上，你需要Cygwin来构建。只需在终端/Cygwin中运行“make”，塞班项目就会被构建并创建“wgz”文件。这些步骤如图3–13所示。

> 图3–13. 构建塞班项目

> 图3–14. 构建塞班项目

`app.wgz`文件需要被加载到塞班模拟器中。使用模拟器的文件选项来导入`.wgz`文件。这将提示你安装应用程序。选择“是”以安装应用程序。

应用程序安装后，我们需要点击塞班模拟器中下部的中间按钮来查看所有已安装的应用程序。从此屏幕启动我们的应用程序。一旦你启动应用程序，你将看到



## 为 webOS 设置环境

您可以在 Windows、Mac 和 Linux 上开发 webOS 应用程序。您需要在开发机上安装以下软件：

- 1. 32位 Java SE 6 JDK
- 2. 3.0 至 3.2 版本的虚拟机
- 3. 3.0.4 版本的 webOS SDK

接下来，您需要执行以下安装步骤：

- 1. 安装 32位 Java SE 6 JDK
    您可以从 www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html 下载 J2SDK。运行 J2SDK 安装程序直到完成。将 `Installation_directory/J2SDK/bin` 添加到 PATH 环境变量中。

- 2. 安装 Virtual Box
    从 www.virtualbox.org/wiki/Download_Old_Builds_4_0 下载 VirtualBox 3.0 – 3.2。开始安装直到完成。

- 3. 安装 webOS SDK
    从 https://developer.palm.com/content/resources/develop/sdk_pdk_download.html 下载 webOS SDK。开始安装直到完成。

- 4. 仅为 Windows 安装 Cygwin
    如果您使用 Windows，则必须安装 Cygwin 来为 webOS 构建和部署 PhoneGap 应用程序。请参阅 Symbian 安装的第 1 步。

- 5. 创建新的 PhoneGap 项目
    PhoneGap 目录包含一个名为 webOS 的目录。这是 PhoneGap webOS 的模板项目。为了创建 PhoneGap webOS 项目，请将此目录复制到您的项目区域。

- 6. 编写 PhoneGap 应用程序
    打开 www 文件夹，并在您喜欢的编辑器中打开 index.html。根据需要编辑 HTML 内容并包含 CSS 和 JavaScript。

- 7. 部署到模拟器
    在部署项目之前，请确保您的 webOS 模拟器正在运行。从您的应用程序文件夹/开始菜单运行 palm-emulator。
    在项目文件夹中运行 `make`。这将创建最终的 javascript 文件。将项目打包为 webOS 移动应用程序包，并将其安装到 webOS 模拟器中。

- 8. 部署到设备
    为了将 PhoneGap 项目部署到 webOS 设备，您必须启用“开发者模式”并将其插入。在 Cygwin 终端中的项目文件夹中运行 `make`。

## 使用 PhoneGap Build 的云构建环境

到目前为止，我们看到在不同移动平台上构建 PhoneGap 应用程序是乏味的。虽然 PhoneGap 开发减轻了跨平台移动应用开发的痛苦，但对于开发者来说，在每个移动平台上构建 PhoneGap 仍然很乏味。
为了减轻这种痛苦，PhoneGap 推出了 PhoneGap Build。PhoneGap Build 是一个云构建服务。开发者将他们的 PhoneGap 应用程序代码提交给 PhoneGap Build，然后 PhoneGap Build 在以下平台上构建应用程序：

- 1. iOS
- 2. Android
- 3. Blackberry
- 4. webOS
- 5. Symbian

在本节中，我们将了解如何在 PhoneGap 上设置账户并构建应用程序。

## 在 PhoneGap Build 上注册

- 1. 第一步是获取 PhoneGap beta 的账户。访问 http://build.phonegap.com 并提供您的详细信息。
- 2. 一旦您提交了详细信息，您将收到来自 PhoneGap 的电子邮件。在这封电子邮件中，PhoneGap 将提供 beta 代码。您需要在 PhoneGap 的注册页面上提供 beta 代码。

## 第三章：设置环境

虽然 PhoneGap Build 将为您构建应用程序，但您需要拥有这些应用程序。这是必要的，因为您将要在 Appstore、Android Market 和 BlackBerry 市场上发布从 PhoneGap Build 获得的构建。

让我们试着理解拥有应用程序意味着什么。应用程序需要由某些证书签名，将您的所有权印记在应用程序上。对于像 iOS 这样的平台，您需要获取开发者账户并从 Apple 获取证书。

PhoneGap 需要您提供这些证书来为以下平台构建应用程序：

- 1. iOS
- 2. Android
- 3. BlackBerry

以下部分将演示如何生成这些证书并提供给 PhoneGap Build。

## 在 PhoneGap Build 上注册您的应用程序

使用 PhoneGap Build 的第一步是在 PhoneGap Build 上注册您的应用程序。您可以通过三种方式在 PhoneGap Build 上注册。

- 1. 在 PhoneGap 服务器上创建一个新的 git 仓库并将代码推送到那里。
- 2. 从现有的 git 仓库拉取代码。
- 3. 上传您的 PhoneGap 应用程序的存档。

为了简单起见，我们将选择第二个选项，从 PhoneGap git 仓库拉取入门 PhoneGap 项目（如图 3–15 所示）。

> 注意：PhoneGap Build 需要访问您的源代码，因为它是一个构建工具。这意味着您需要与 PhoneGap Build 共享您的源代码。这就像我们想要构建 PhoneGap 在其某个 git 仓库中提供的 PhoneGap 示例代码。这样我们就不需要提供任何源代码，并且我们将使用示例源代码进行练习。

![](img/4a75e501abc949744a790d09257a5b1e_118_0.png)

**图 3–15。** *从 PhoneGap 仓库拉取 PhoneGap 入门代码*

现在您可以看到您的应用程序列在“your apps”部分下。请注意，对于每个平台，都有一个下载图标（如图 3–16 所示）。单击下载按钮允许您下载特定于平台的二进制文件。所有这些二进制文件都是在 PhoneGap Build 服务器上构建的，因此不需要您为 iOS、Android、BlackBerry、Symbian 和 webOS 设置环境。

![](img/4a75e501abc949744a790d09257a5b1e_119_0.png)

请注意图 3–16 中 iOS 构建的橙色警告。对于 iOS，构建需要由开发者证书和配置文件签名。配置文件与 Apple 开发者账户相关联。如果开发者希望在 iOS 设备上测试应用程序，则设备需要在此配置文件中注册。

现在，在上面列出的 5 个平台中，我们需要为其中 3 个平台向 PhoneGap Build 提供某种开发者私钥。这是为了获得特定于平台的构建所必需的，这些构建可以：

- 1. 安装在设备上。
- 2. 上传到各自的应用程序商店。

这些平台是：

- 1. Android
- 2. iOS
- 3. BlackBerry

## 设置 Android 构建环境

Android 应用程序在发布到 Android 市场之前，需要使用自签名密钥库进行签名。Android 不需要中央机构来认证开发者的应用程序。但是，如果应用程序的版本 1 是使用 xyz 开发者密钥库签名的，那么应用程序的下一个版本也必须使用相同的开发者密钥库签名。如果不这样做，将导致应用程序的下一个版本被 Android Market 拒绝。

以下是配置 PhoneGap Build 以生成可以部署到 Android Market 的适当 Android 构建的步骤：

- 1. 创建私钥库
- 2. 将私钥库上传到 PhoneGap Build
- 3. 运行 PhoneGap Build

### 1. 创建私钥库

这方面的起点是理解 http://developer.android.com/guide/publishing/app-signing.html#cert 上列出的 Android 应用程序发布指南。在本节中，我们将引导您完成创建私钥库所需的步骤。

创建私钥库的要求是您需要在机器上安装 Java JDK 1.6 及以上版本。通过打开终端/命令提示符并键入以下内容来确认：

```
$> keytool
```

如果这显示了某种帮助信息，那么您就可以开始了。如果这告诉您没有名为 keytool 的工具，请确保您的 java bin 目录在路径中。

现在，要实际创建您的私钥库，请按照以下提供的步骤操作：

```
$> keytool -genkey -v -keystore my-release-key.keystore
```

系统将提示您输入密码。输入密码并记下它。

```
$>Enter keystore password: welcome
```

系统会要求您重新输入密码。

```
$>Re-enter new password: welcome
```

接下来，您将被问及一系列问题，以在私钥库中记录您的身份。请回答这些问题。

```
$>What is your first and last name?
  [Unknown]:  Rohit Ghatol
$>What is the name of your organizational unit?
  [Unknown]:  Engineering
```



## 2. 将私钥库上传至 PhoneGap Build

> 你的组织名称是什么？
[Unknown]: QuickOffice

> 你的城市或地区名称是什么？
[Unknown]: Pune

> 你的州或省份名称是什么？
[Unknown]: Maharastra

> 此单位的两位字母国家代码是什么？
[Unknown]: IN

现在，系统将要求你确认到目前为止输入的数据是否正确。
> CN=Rohit Ghatol, OU=Engineering, O=QuickOffice, L=Pune, ST=Maharastra, C=IN 是否正确？
[no]: yes

> 注意：该工具会询问你用于创建自签名证书的密码。要使其与之前的密码保持一致，只需按回车键即可。

> 正在为 CN=Rohit Ghatol, OU=Engineering, O=QuickOffice, L=Pune, ST=Maharastra, C=IN 生成 1,024 位 DSA 密钥对和有效期为 90 天的自签名证书 (SHA1withDSA)

> 请输入 <mykey> 的密钥密码
（如果与 keystore 密码相同，直接按回车）：

[正在存储 my-release-key.keystore]

现在，你的名为 “my-release-key.keystore” 的私钥库文件已创建，并保存在相同目录中。

在 PhoneGap Build 上导航到你的应用程序，点击编辑按钮，你将看到如图 3–17 所示的屏幕。

**图 3–17。** *PhoneGap Build 编辑应用程序屏幕*

导航到签名部分，并在该屏幕上上传 Android 密钥库信息（如图 3–18 所示）。

## 第 3 章：设置环境

图 3–18。输入 Android 发布密钥库详细信息

在此处为你的密钥库提供一个标题。在 PhoneGap Build 上，你可以提供多个密钥库，并选择用于构建应用程序的密钥库。此标题用于在浏览上传到 PhoneGap Build 的各种密钥库时识别它们。

接下来，上传密钥库文件并提供一个别名。在密码字段（两个都要）中，你需要输入创建密钥库和私有证书时使用的密码（在我们的例子中是 “welcome”）。

## 3. 运行 PhoneGap Build

最后，点击创建，PhoneGap Build 将代你存储此密钥库。

现在你应该会看到一个类似图 3–19 的屏幕，告诉你 “my release key” 密钥库已用于构建 Android 版本。

图 3–19。*为 PhoneGap 应用程序注册的 Android 密钥库*

## 设置 iOS 构建环境

在开始之前，我们先注意一下在 PhoneGap 上构建 iOS 的前提条件列表。

- 1. Apple 开发者账户，可以是 Apple 开发者计划 (http://developer.apple.com/programs/ios/) 或 Apple 企业开发者计划 (http://developer.apple.com/programs/ios/enterprise/)。选择最适合你需求的计划。
- 2. 带有 Xcode 的 Mac 机器，用于提取开发者证书和配置文件。提取此信息后，开发者可以从任何操作系统使用 PhoneGap Build。

接下来的步骤如下：

- 1. 获取 iOS 密钥
- 2. 将 iOS 密钥提供给 PhoneGap Build

### 1. 获取 iOS 密钥

有关如何将你的 Xcode 与 iOS 开发者账户配置的完整信息，请参阅 http://tiny.cc/appleprov。

按照上述步骤操作，并确保你能够构建并在模拟器（最好是在已添加到配置文件的 iOS 设备）上安装一个示例 iPhone 应用程序。

现在下一步是从 Xcode 导出开发者证书和配置文件，并将它们放入 PhoneGap Build。

### 2. 将 iOS 密钥提供给 PhoneGap Build

正确设置 iOS 开发环境后，我们需要提取开发者证书和移动配置文件，并将它们上传到 PhoneGap Build。

第一步是从 Mac 的钥匙串访问中提取开发者证书。打开钥匙串访问，定位开发者证书并导出。导出时，系统会要求你提供一个文件夹和密码。请记录此密码，因为在将开发者证书上传到 PhoneGap Build 网站时会用到。

之后，我们将继续提取配置文件。配置文件位于 Xcode 内部。打开 Xcode，转到 window->organizer 并启动它。从这里导出 “team provisioning profile”。请注意，配置文件是你向 Apple 表明你已将 iPhone/iPod/iPad 注册为开发者设备以测试应用程序的地方。PhoneGap Build 需要此配置文件来签名你的应用程序 (ipa)。

我们现在已将开发者证书和移动配置文件提取到一个名为 ios-Keys 的目录中。

图 3–20。包含开发者证书和配置文件的目录

我们需要在 PhoneGap Build 上上传这些密钥。再次访问应用程序的编辑屏幕，导航到签名部分，对于 iOS，点击 “add keys”（在 “select a key” 下拉菜单下方）。

图 3–21。iOS 添加密钥屏幕

这将打开 iOS 证书和配置文件配对屏幕。上传所需的密钥以及导出开发者证书时使用的相同密码。

图 3–22。向 PhoneGap Build 提供开发者证书和配置文件

一旦你启动 PhoneGap Build，你应该会注意到 iOS ipa 构建上的橙色警告已经消失，构建已变为绿色。点击 ipa 按钮将为你下载 iOS ipa。

## 设置 BlackBerry 构建环境

设置 BlackBerry 构建环境所需的主要操作如下：

- 1. 获取 BlackBerry 密钥
- 2. 将 BlackBerry 密钥提供给 PhoneGap Build

### 1. 获取 BlackBerry 密钥

PhoneGap Build 提供开箱即用的支持，用于构建可安装在你的设备上的 BlackBerry 应用程序。但是，为了将这些应用程序上传进行分发，你需要拥有 RIM 提供的密钥。要获得这些密钥，你需要使用此网站注册 RIM：https://www.blackberry.com/SignedKeys/。

注册后，你将收到来自 RIM 的电子邮件，其中包含有关如何将这些密钥与你的 BlackBerry 开发环境安装的步骤。由于法律禁止分享这些说明，我们无法在此详述。

### 2. 将 BlackBerry 密钥提供给 PhoneGap Build

下一步是从 BlackBerry 开发环境中提取密钥。BlackBerry 开发环境可以使用 eclipse 或独立的 BlackBerry WebWorks 来设置。BlackBerry 密钥位于 BlackBerry 的 sdk 目录中。

第一个任务是定位 sdk 目录。

如果 BlackBerry 开发环境是使用 eclipse 安装的，你应该能在 <<eclipse location>>\plugins\net.rim.ejde.componentpackX.X.X_X.X.X.X\components 找到 BlackBerry sdk 目录。一个例子是 d:\worksoft\eclipse-helios\net.rim.ejde.componentpack5.0.0_5.0.0.25\components。

如果 BlackBerry 开发环境是使用 BlackBerry Widget/WebWorks Packager Standalone SDK（如本章前面所示）安装的，那么安装目录就是 sdk 目录。在本章前面部分，这显示为 “c:\BBWP” 目录。

代码签名文件/密钥位于 sdk 目录中。

```
<<webworks_sdk_dir>>\bin\sigtool.csk
<<webworks_sdk_dir>>\bin\sigtool.db
```

现在我们已经获得了 BlackBerry 密钥的访问权限，请继续到你在 PhoneGap Build 上的应用程序，点击编辑，转到签名部分。从下拉菜单中，选择 BlackBerry 的 “add a key” 选项。

**图 3–23。** *BlackBerry 添加密钥屏幕*

在下面显示的对话框中上传 BlackBerry 密钥。使用你在按照 BlackBerry 电子邮件中说明操作时创建的相同密码。这为 PhoneGap Build 提供了构建 BlackBerry 应用程序所需的所有信息，这些应用程序可以在 BlackBerry 分发渠道上分发。



## 启动 PhoneGap Build

PhoneGap Build 可以通过两种方式启动：

1.  在 PhoneGap Build 上手动点击“rebuild all”按钮，如下图所示。这将把构建任务加入 PhoneGap Build 服务器的队列中。
2.  第二种方式是使用 PhoneGap Build 的 RESTful API 来创建应用、更新代码并触发构建。你可以将 PhoneGap Build 作为你的持续集成构建（例如来自 Bamboo、Jenkins 或任何其他 CI 系统）的一部分。让 CI 构建脚本调用 PhoneGap Build 的 RESTful API。有关 PhoneGap Build API 的详细信息，请访问 https://build.phonegap.com/docs/api。

## 结论

随着云服务在托管 Web 服务和应用程序方面日益普及，许多公司正在寻找基于云的 SaaS 服务来辅助其开发周期。

像 Pivotal Tracker 这样的公司用于敏捷规划，Bitbucket 用于托管源代码，甚至还有在线的 CI 构建工具（例如 Jira Studio）。PhoneGap Build 的出现并不令人意外。

## 第三章：环境设置

通过不额外购买 Windows 和 Mac 机器专门用于 CI 来节省基础设施成本是有意义的。降低成本和租用基础设施（就像我们支付电费一样）已成为当今的趋势。

PhoneGap Build 适合那些希望摆脱基础设施负担、并使用基于云的 SaaS 服务来构建 PhoneGap 应用程序的中小型公司。

## 第四章：在 jQuery Mobile 中使用 PhoneGap

虽然 PhoneGap 提供了一个平台，允许 JavaScript 应用访问手机原生功能，但开发移动 HTML 应用还有许多其他方面需要考虑。

移动 HTML 应用程序最重要的部分之一是 UI。你可以完全手动使用 HTML、JavaScript 和 CSS 来编写整个 UI。然而，任何 Web 开发者都会告诉你这种方法存在很多问题，包括以下几点：

1.  并非所有浏览器都相同；你需要一个跨浏览器框架才能取得成功。即使大多数移动浏览器都是基于 WebKit 的，最好使用一个能为开发者抽象掉浏览器差异的框架。
2.  如果你手动编码，你的大部分代码将是用于绘制 UI、修改 DOM 和进行 Ajax 调用。一个能让你“写得更少，做得更多”的框架将帮助你真正专注于业务逻辑。
3.  创建一个美观的 HTML UI 需要设计师的技能。同时，大多数移动客户端都有预定义的主题或模式。如果一个框架能提供开箱即用的美观 UI，对开发者会很有帮助。这样，开发者就可以专注于业务逻辑。

话虽如此，与 PhoneGap 一起使用来编写 UI 的最简单的框架之一是 jQuery Mobile。首先，jQuery Mobile 是建立在非常流行的 jQuery 之上的。jQuery 以其作为提高开发者生产力、并帮助开发者处理跨浏览器兼容性的 JavaScript 库而闻名。同时，jQuery 还有许多免费的插件可用于完成各种任务。

jQuery Mobile 是一个为移动 UI 构建的 UI 框架。它具有声明式的 UI，这意味着你无需在 JavaScript 中编码你的 UI，而可以在 HTML 中声明它。jQuery Mobile 还提供了开箱即用的、外观出色的 UI。

所有这些使得 jQuery Mobile 成为最易于使用的 JavaScript UI 框架，也是适合中等复杂度移动 UI 的最合适的框架。

话虽如此，jQuery Mobile 为智能手机和平板电脑提供了相同的 UI。如果你的需求不同，并且需要为智能手机和平板电脑提供不同的布局，你应该参阅第五章。

## 熟悉 jQuery

jQuery 是最好的 JavaScript 库之一，它可以帮助你执行 Ajax 调用、在 HTML DOM 中搜索特定元素以及修改 DOM。它还有自己的插件框架。最棒的是它的跨浏览器兼容性，免去了处理浏览器差异的烦恼。你可以参考以下 jQuery 教程：www.w3schools.com/jquery/default.asp。

## jQuery 初始化

jQuery 初始化是一个两步过程。

1.  在你的 HTML 页面中包含 jQuery JavaScript。
2.  声明一个回调函数，当 jQuery 库加载完成后，jQuery 将调用此回调。

这是必要的，因为一个 HTML 页面可能包含许多文件，如 CSS、JavaScript 和图像。浏览器将下载所有这些资源并开始执行所有 JavaScript 代码块。如果在未正确初始化之前就开始使用 jQuery API 调用，你将会遇到错误。因此，你需要声明一个回调函数，它是我们应用程序的入口点，jQuery 将调用此回调并引导应用程序启动。

通常，当开发者不使用 jQuery 时，他会以如下方式编写代码：

```
window.onload = function(){
    alert("Page Loaded");
}
```

使用 jQuery 时，相同的代码将如下所示：

```
<html>
    <head>
        //Step 1 - include jquery library
        <script type="text/javascript" src="jquery.js">
        </script>
        <script type="text/javascript">
            //Step 2 - Declare a callback for jquery to call when it loads
            $(document).ready(function() {
                //Place to bootstrap your application
                alert("jquery loaded");
            });
        </script>
    </head>
    <body>
        <h1>
            jQuery Demo
        </h1>
    </body>
</html>
```

当你在任何浏览器中运行此代码时，你会在页面加载时看到一个弹出框。该弹出框将显示“jQuery loaded”。

## jQuery 选择器

现在你已经了解了如何初始化 jQuery 并注册一个 onload() 方法，让我们继续了解如何查找 HTML DOM 元素。

通常，开发者会使用以下代码来获取 id 为“placeholder”的 div 元素：

```
document.getElementById("placeholder").innerHTML = "hello world";
```

在 jQuery 中，你会将上述函数写为：

```
$("#placeholder").html("hello world");
```

jQuery 提供了多种定位 HTML 元素的方式。一个例子是 `$("#placeholder")`，它返回一个包装了 id 为“placeholder”的元素的 jQuery 元素。一旦你获得这个 jQuery 包装器，你就可以调用 jQuery 函数来操作 DOM。在上面的例子中，你正在将其 HTML 内容更改为“hello world”。

让我们结合一个代码示例，回顾一些其他有用的选择器示例：

```
<html>
    <body>
        <h1 class="title">
            JQUERY SELECTOR Tutorial
        </h1>
        <p>
            simple paragraph
        </p>
        <p class="title">
            Paragraph with class title
        </p>
        <p>
            another paragraph
        </p>
        <ul id="selector">
            <li>
                Element based - $("p")
            </li>
            <li>
                Id based - $("#selector")
            </li>
            <li>
                CSS Class based - $(".title")
            </li>
            <li>
                Element + Class based - $("p.title");
            </li>
            <li>
                Element+ID+Position - $("ul#selector li:first")
            </li>
        </ul>
    </body>
</html>
```

### 基于元素的选择器

`$("p")` 选择所有的段落元素：

```
<p>simple paragraph</p>
<p class="title">Paragraph with class title</p>
<p>another paragraph</p>
```

### 基于 ID 的选择器

`$("#selector")` 选择 id 为“selector”的元素。请记住，# 被添加在你要搜索的 id 之前。此选择器选中以下元素：

```
<ul id="selector">
```

### 基于 CSS 类的选择器

`$(".title")` 选择 class 为“title”的元素。请记住，类名前加“.”来搜索具有该类的元素。此选择器选中以下元素：

```
<h1 class="title">JQUERY SELECTOR Tutorial</h1>

<p class="title">Paragraph with class title</p>
```

### 组合选择器

以下是一些示例，展示如何混合和匹配选择器以精确锁定特定元素：

`$("p.title")` 选择 class 为“title”的段落元素，它选中以下元素：

```
<p class="title">Paragraph with class title</p>
```

`$("ul#selector li:first")` 从 id 为“selector”的 ul 元素中选择第一个 li 元素。它选中以下元素：

```
<li>Element based          - $("p")</li>
```

完整的 jQuery 选择器列表可在以下链接找到：www.w3schools.com/jquery/jquery_ref_selectors.asp。



## jQuery DOM 操作

首先，让我们看看如何从 HTML 中检索值。你可以检索元素的值或内部 HTML。

如果你执行 javascript `$("#selector").html()`，你将得到以下文本：

-   <li>基于元素 - $("p")</li>
-   <li>基于 ID - $("#selector")</li>
-   <li>基于 CSS 类 - $(".title")</li>
-   <li>基于元素 + 类 - $("p.title")</li>
-   <li>元素+ID+位置 - $("ul#selector li:first")</li>

下面的示例展示了如何从 jQuery 选择器结果中提取值。首先，该示例展示了当你假设 jQuery 选择器只返回一个值时会发生什么。也就是说，假设 `$("p")` 只返回一个段落。然后你将尝试使用 `html()` 函数获取该段落的值。请注意，`$("p")` 返回的是一个 jQuery 选择器，而 `html()` 函数属于 jQuery 选择器。在这种情况下，jQuery 将对 `$("p")` 选择器找到的第一个元素运行 `html()` 方法。这意味着当你调用 `$("p").html()` 时，`$("p")` 将定位到如下第一个段落，并给出值 "simple paragraph"。

```
<p>simple paragraph</p>
```

现在你知道了 `$("p")` 应该会给你很多值，因为前面的例子中有许多段落，如下所示：

```
<p>simple paragraph</p>
<p class="title">Paragraph with class title</p>
<p>another paragraph</p>
```

为了遍历任何列表，jQuery 提供了一个方法："each()"。要使用 "each()"，你需要在 jQuery 选择器上调用它，就像我们例子中的 `$("p")`。"each()" 方法接受两个参数：第一个是索引（迭代中的位置），第二个是该位置上的实际条目。

因此，当你调用 `$("p").each(function(index,element){})` 时，`element` 就是每个段落上的实际 jQuery 选择器。

```
<script type="text/javascript">
$(document).ready(function() {
    alert("Simple extraction = " + $("p").html());

    $("p").each(function(index, element) {
        alert(index + " - '" + $(element).html() + "'");
    });
});
</script>
```

现在，让我们继续探讨修改 HTML DOM。我们将快速介绍操作 DOM 的最简单方法。

当你执行以下 JavaScript 时，它会将段落的内容修改为 "Changed to 123."。

```
<script type="text/javascript">
$(document).ready(function() {
    $("p.title").html("Changed to 123");
});
</script>
```

完整的 jQuery HTML 操作列表可以在 www.w3schools.com/jquery/jquery_ref_html.asp 找到。

## jQuery Ajax 调用

jQuery 提供了许多用于进行 Ajax 调用的实用方法。

以下是向 URL 发起 Ajax GET 调用的示例。这是一个典型的"写得更少，做得更多"的例子。以下代码对 `service/employee/details.txt` 发起了一次 Ajax GET 调用，并将内容放入 id 为 "details" 的 div 中：

```
$.get("service/employee/details.txt", function (result) {
    $("div#details").html(result);
});
```

以下是向 URL 发起 Ajax POST 调用的示例，发布数据 `{name:employeeName}`：

```
$.post("service/employee/details", {
    name: employeeName
}, function (result) {
    alert("Post successful");
});
```

完整的 jQuery Ajax 操作列表可以在 www.w3schools.com/jquery/jquery_ref_ajax.asp 找到。

## 了解 jQueryMobile

jQueryMobile 通过提供一个通用的 UI 平台来开发跨多种流行移动平台的应用程序，将 jQuery "写得更少，做得更多"的理念提升到了新的水平。

jQueryMobile 构建在非常流行且强大的 jQuery 和 jQuery UI 框架之上。jQueryMobile 提供了开箱即用、支持触摸的移动小部件，例如列表视图、带返回按钮的标题、导航动画以及更多功能。这些小部件具有专业和精致的外观，使得开发准备发布的成品应用变得更加容易。

jQueryMobile 的主页是 http://jquerymobile.com/。

此外，jQueryMobile 为你提供了五种开箱即用的主题供选择。以下示例展示了按钮在不同主题下的外观。总体来说，我们有五种主题——主题 A、主题 B、主题 C、主题 D 和主题 E——如图 4-1 所示。

![](img/4a75e501abc949744a790d09257a5b1e_136_0.png)

同时，jQueryMobile 为表 4-1 中列出的平台提供分级支持。

**表 4-1. jQueryMobile 支持的平台**

| OS 平台 | 平台版本 |
| :--- | :--- |
| iOS | 版本 3.1.3 及更高 |
| Android | 版本 1.5 及更高 |
| Symbian | S60 版本 5 及更高 |
| BlackBerry OS | 版本 5.0 及更高 |
| WebOS | 版本 1.4.1 及更高 |
| Windows 7 | 版本 7.0 及更高 |
| Samsung Bada | 版本 1.0 及更高 |
| MeeGo | 版本 1.1 及更高 |

## 在移动应用中引入 jQueryMobile

从 http://jquerymobile.com/download/ 下载 `jquery.mobile-1.0rc2.zip` 并解压。解压后，你将看到如图 4-2 所示的文件夹结构。它包含两对 jQueryMobile JavaScript 和一个 CSS 文件。顾名思义，你应该在生产环境中使用 `.min` 的 JavaScript 和 CSS 文件，因为它们是经过压缩的文件。

除此之外，你还需要在移动应用中包含 images 文件夹。

![](img/4a75e501abc949744a790d09257a5b1e_137_0.png)

图 4–2. *jQueryMobile 文件夹结构*

以下是 jQueryMobile 示例的 HTML 模板：

```
<!DOCTYPE HTML>
<html>

    <head>
        <title>
            jQuery Mobile Demo
        </title>
        <link rel="stylesheet" type="text/css" href="jquery.mobile-1.0rc2.min.css"/>
        <script type="text/javascript" src="jquery-1.6.4.min.js"></script>
        <script type="text/javascript" src="jquery.mobile-1.0rc2.min.js"></script>
    </head>

    <body>
        ...
    </body>

</html>
```

## jQueryMobile 声明式 UI

声明式 UI 构建是 jQueryMobile 的精髓所在。你无需编写复杂的 JavaScript 代码来构建 UI。UI 构建就像添加普通的 HTML 元素，只需添加一些 jQueryMobile 特定的属性和它们的值。

## 页面和对话框

你在上一节看到了 HTML 模板。现在，你将向其中添加 jQueryMobile 布局和小部件。

你可以使用 body 标签内 div 元素的 `data-role` 属性来声明页面。因此，在一个 body 标签内，你只需声明以下内容即可声明多个页面：

```
<div data-role="page"></div>
```

同样，你可以通过将 `data-role` 声明为 "header"、"content" 和 "footer" 来声明页面的组成部分。以下是 jQueryMobile 中一个页面的示例：

```
<div data-role="page">
    <div data-role="header"></div>
    <div data-role="content"></div>
    <div data-role="footer"></div>
</div>
```

一个页面的完整示例如下所示。

```
<!DOCTYPE HTML>
<html>
<head>
    <title>jQuery Mobile Demo</title>
    <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
    <script src="jquery-1.6.4.min.js"></script>
    <script src="jquery.mobile-1.0rc2.min.js"></script>
</head>
<body>
    <!-- Page Start-->
    <div data-role="page">
        <!-- Page Header Start -->
        <div data-role="header">
            <h1>Page Title</h1>
        </div>
        <!-- Page Header End -->

        <!-- Page Body Start -->
        <div data-role="content">
            <p>
                Page content goes here.
            </p>
        </div>
        <!-- Page Body End -->

        <!-- Page Footer Start -->
        <div data-role="footer">
            <h4>
                Page Footer
            </h4>
        </div>
        <!-- Page Footer End -->
    </div>
    <!-- Page End -->
</body>
</html>
```

这段 HTML 在浏览器中运行时，显示的界面如图 4-3 所示。

## 第 4 章：将 PhoneGap 与 jQuery Mobile 结合使用

![](img/4a75e501abc949744a790d09257a5b1e_139_0.png)

图 4-3. jQueryMobile 页面

既然你已经了解了 jQueryMobile 中页面的概念，让我们来看看一个拥有多个页面或对话框的场景。

典型的应用程序有多个页面和对话框。jQueryMobile 的妙处在于，你可以在同一个 HTML 页面内定义所有这些不同的页面和对话框。

方法如下。在一个 HTML 页面中定义多个 div，并给它们以下属性：

1. 一个名为 `data-role` 的属性，设置为 `page`。看起来像这样：`data-role="page"`
2. 一个名为 "id" 的属性，以便在代码中标识它们

你使用链接和按钮来导航到这些页面和对话框。最简单的方法如下：

1. 定义一个链接，其 `href` 为 `#<<页面/对话框的id>>`
2. 给该链接一个 `data-role="button"`

请注意，页面和对话框的声明方式相同。事实上，并没有专门的对话框，但你可以将页面以弹出窗口的形式作为对话框加载。

以下是一个指向页面的链接示例。当此链接被点击时，将过渡到 id 为 "page2" 的页面。还要注意，因为链接被赋予了 `data-role="button"`，所以它看起来像一个按钮。

```
<a data-role="button" href="#page2">Page Navigation</a>
```

以对话框形式打开页面与导航到页面非常相似。你只需要向链接添加两个属性：

1. `data-rel="dialog"`



## 工具栏与按钮

-   在 jQueryMobile 中，有两种类型的工具栏：
    -   `Header bar`（页头栏）
    -   `Footer bar`（页脚栏）

通常，创建一个工具栏就像在页头或页脚栏中声明一些按钮一样简单。这一点在图 4–7 中有所描绘。

## 表单元素

jQueryMobile 中的表单元素是典型的 HTML 表单元素——它们只是外观不同。这意味着你可以运用你的 HTML JavaScript 技能来渲染出外观精美、精致的 jQueryMobile 小部件，并使用传统的事件处理技术快速编写你的移动 Web 应用程序。

让我们来看几个表单元素的例子。在第一个示例中，我们使用了一个输入文本框、一个文本域和一个搜索框。所有这些元素都被分配了一个标签。它们被包裹在一个 `fieldset` 中，以形成一个包含标签和关联小部件的分组。参见图 4–8 了解 jQueryMobile 中表单元素的外观。

```html
<!DOCTYPE html>
<html>
<head>
    <title>jQuery Mobile Demo</title>
    <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
    <script src="jquery-1.6.4.min.js"></script>
    <script src="jquery.mobile-1.0rc2.min.js"></script>
</head>
<body>
    <!-- Main Page-->
    <div data-role="page" id="main">
        <div data-role="header" data-position="inline">
            <a href="index.html" data-icon="delete">Cancel</a>
            <h1>Edit Contact</h1>
            <a href="index.html" data-icon="check">Save</a>
        </div>
        <div data-role="content">
            <div data-role="fieldcontain">
                <label for="firstname">First Name:</label>
                <input type="text" name="firstname" id="firstname" value=""/>
            </div>
            <div data-role="fieldcontain">
                <label for="lastname">Last Name:</label>
                <input type="text" name="lastname" id="lastname" value=""/>
            </div>
            <div data-role="fieldcontain">
                <label for="notes">Notes:</label>
                <textarea name="notes" id="notes"></textarea>
            </div>
            <div data-role="fieldcontain">
                <label for="search">Search:</label>
                <input type="search" name="search" id="search" value=""/>
            </div>
        </div>
        <div data-role="footer">
            <div data-role="navbar">
                <ul>
                    <li><a href="index.html" data-icon="delete">Remove</a></li>
                    <li><a href="index.html" data-icon="plus">Add</a></li>
                    <li><a href="index.html" data-icon="arrow-u">Up</a></li>
                    <li><a href="index.html" data-icon="arrow-d">Down</a></li>
                </ul>
            </div>
        </div>
    </div>
</body>
</html>
```

2. data-transition="pop"（这是动画效果）

<a data-role="button" href="#dialog1" data-rel="dialog" data-transition="pop">Open Dialog </a>

这是一个完整的示例供你尝试。图 4–4 显示了“main”页面，图 4–5 显示了“page2”页面，图 4–6 显示了“dialog1”页面，它充当一个对话框：

```html
<!DOCTYPE html>
<html>
    <head>
        <title>jQuery Mobile Demo</title>
        <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
        <script src="jquery-1.6.4.min.js"></script>
        <script src="jquery.mobile-1.0rc2.min.js"></script>
    </head>
    <body>
        <!-- Main Page-->
        <div data-role="page" id="main">
            <div data-role="header">
                <h1>Main Page</h1>
            </div>
            <div data-role="content">
                <h1>Page Nav and Dialog Example</h1>
                <a data-role="button" href="#page2">Page Navigation</a>
                <a data-role="button" href="#dialog1" data-rel="dialog" data-transition="pop">Open Dialog </a>
            </div>
            <div data-role="footer">
                <h4>Main Page Footer</h4>
            </div>
        </div>
        <!-- First Page End -->
        <!-- Second Page-->
        <div data-role="page" id="page2" data-add-back-btn="true">
            <div data-role="header">
                <h1>Second Page</h1>
            </div>
            <div data-role="content">
                <h1>Second Page</h1>
            </div>
            <div data-role="footer">
                <h4>Click back to go back to main page</h4>
            </div>
        </div>
        <!-- Second Page End -->
        <!-- Dialog -->
        <div data-role="page" id="dialog1">
            <div data-role="header">
                <h1>Dialog Title</h1>
            </div>
            <div data-role="content">
                <h1>Dialog body</h1>
            </div>
            <div data-role="footer">
                <h4>Click close button to go back to main page</h4>
            </div>
        </div>
        <!-- Dialog End -->
    </body>
</html>
```

在第二个示例中，HTML 的 select 元素被包装在一个美观的开/关开关中。请注意，当你以编程方式从中获取值时，你将把它用作一个 HTML select 框。你还用滑块包装了一个文本框。滑块的值会进入文本框。这就像用户在文本框中输入一个数字一样好，但通过 jQueryMobile，用户可以使用滑块在给定范围内选择一个值。参见图 4–9 了解此 HTML 的渲染效果。

```html
<!DOCTYPE html>
<html>
<head>
    <title>jQuery Mobile Demo</title>
    <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
    <script src="jquery-1.6.4.min.js"></script>
    <script src="jquery.mobile-1.0rc2.min.js"></script>
</head>
<body>
    <!-- Main Page-->
    <div data-role="page" id="main">
        <div data-role="header" data-position="inline">
            <a href="index.html" data-icon="delete">Cancel</a>
            <h1>Edit Contact</h1>
            <a href="index.html" data-icon="check">Save</a>
        </div>
        <div data-role="content">
            <form action="#" method="get">
                <h2>Simple Form Elements</h2>
                <div data-role="fieldcontain">
                    <label for="onoff-slider">On/Off Switch:</label>
                    <select name="onoff-slider" id="onoff-slider" data-role="slider">
                        <option value="off">Off</option>
                        <option value="on">On</option>
                    </select>
                </div>
                <div data-role="fieldcontain">
                    <label for="number">Number Input:</label>
                    <input type="number" name="number" id="number" value="" />
                </div>
            </form>
        </div>
        <div data-role="footer" class="ui-bar">
            <a href="index.html" data-role="button" data-icon="delete">Remove</a>
            <a href="index.html" data-role="button" data-icon="plus">Add</a>
            <a href="index.html" data-role="button" data-icon="arrow-u">Up</a>
            <a href="index.html" data-role="button" data-icon="arrow-d">Down</a>
        </div>
    </div>
</body>
</html>
```



## 146
第4章：结合使用PhoneGap与jQuery Mobile

在接下来的示例中，你可以看到将HTML单选按钮和复选框包装成美观的界面组件是多么容易。这是通过使用 `data-role` 属性值为 `controlgroup`，以及 `data-type` 属性值为 `horizontal` 来实现的。参考图4-10，了解单选和多选表单元素的效果：

```html
<!DOCTYPE html>
<html>
<head>
    <title>jQuery Mobile Demo</title>
    <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
    <script src="jquery-1.6.4.min.js"></script>
    <script src="jquery.mobile-1.0rc2.min.js"></script>
</head>
<body>
    <!-- Main Page-->
    <div data-role="page" id="main">
        <div data-role="header" data-position="inline">
            <a href="index.html" data-icon="delete">Cancel</a>
            <h1>
                Edit Contact
            </h1>
            <a href="index.html" data-icon="check">Save</a>
        </div>
        <div data-role="content">
            <form action="#" method="get">
                <h2>
                    Single and MultiSelect Form Elements
                </h2>
                <div data-role="fieldcontain">
                    <fieldset data-role="controlgroup">
                        <legend>
                            Choose a base:
                        </legend>
                        <input type="radio" name="radio-choice-1" id="radio-choice-1" value="choice-1" checked="checked" />
                        <label for="radio-choice-1">
                            Thin Crust
                        </label>
                        <input type="radio" name="radio-choice-1" id="radio-choice-2" value="choice-2" />
                        <label for="radio-choice-2">
                            Double Cheese Burst
                        </label>
                        <input type="radio" name="radio-choice-1" id="radio-choice-3" value="choice-3" />
                        <label for="radio-choice-3">
                            Class Hand Tossed
                        </label>
                    </fieldset>
                </div>
                <div data-role="fieldcontain">
                    <fieldset data-role="controlgroup">
                        <legend>
                            Choose Pizza toppings
                        </legend>
                        <input type="checkbox" name="checkbox-1a" id="checkbox-1a" class="custom" />
                        <label for="checkbox-1a">
                            Jalepeno
                        </label>
                        <input type="checkbox" name="checkbox-2a" id="checkbox-2a" class="custom" />
                        <label for="checkbox-2a">
                            Olives
                        </label>
                        <input type="checkbox" name="checkbox-3a" id="checkbox-3a" class="custom" />
                        <label for="checkbox-3a">
                            Cheese
                        </label>
                        <input type="checkbox" name="checkbox-4a" id="checkbox-4a" class="custom" />
                        <label for="checkbox-4a">
                            Capsicum
                        </label>
                    </fieldset>
                </div>
                <div data-role="fieldcontain">
                    <fieldset data-role="controlgroup" data-type="horizontal">
                        <legend>
                            Non Veg topping:
                        </legend>
                        <input type="checkbox" name="checkbox-6" id="checkbox-6" class="custom" />
                        <label for="checkbox-6">
                            Pepperoni
                        </label>
                        <input type="checkbox" name="checkbox-7" id="checkbox-7" class="custom" />
                        <label for="checkbox-7">
                            Ham
                        </label>
                        <input type="checkbox" name="checkbox-8" id="checkbox-8" class="custom" />
                        <label for="checkbox-8">
                            Turkey
                        </label>
                    </fieldset>
                </div>
                <div data-role="fieldcontain">
                    <fieldset data-role="controlgroup" data-type="horizontal">
                        <legend>
                            Payment Type:
                        </legend>
                        <input type="radio" name="radio-choice-b" id="radio-choice-c" value="on" checked="checked" />
                        <label for="radio-choice-c">
                            Cash
                        </label>
                        <input type="radio" name="radio-choice-b" id="radio-choice-d" value="off" />
                        <label for="radio-choice-d">
                            Coupons
                        </label>
                        <input type="radio" name="radio-choice-b" id="radio-choice-e" value="other" />
                        <label for="radio-choice-e">
                            Credit Card
                        </label>
                    </fieldset>
                </div>
            </form>
        </div>
        <div data-role="footer" class="ui-bar">
            <a href="index.html" data-role="button" data-icon="delete">Remove</a>
            <a href="index.html" data-role="button" data-icon="plus">Add</a>
            <a href="index.html" data-role="button" data-icon="arrow-u">Up</a>
            <a href="index.html" data-role="button" data-icon="arrow-d">Down</a>
        </div>
    </div>
    <!-- First Page End -->
</body>
</html>
```

![](img/4a75e501abc949744a790d09257a5b1e_151_0.png)

图4-10. *jQueryMobile* 表单元素

## 列表视图

到目前为止，你已经了解了使用简单的HTML元素配合 `data-role` 和CSS类来声明各种UI组件是多么容易。嗯，在jQueryMobile中，列表视图也不例外。以下示例将向你展示如何轻松地将HTML列表转换为可滚动的移动端列表。

```html
<ul data-role="listview" data-theme="g">
    <li>
        <a href="usa.HTML">USA</a>
    </li>
    <li>
        <a href="uk.HTML">UK</a>
    </li>
    <li>
        <a href="russia.HTML">Russia</a>
    </li>
</ul>
```

以下是在HTML中声明一个列表的完整代码示例。对于动态数据，你只需在运行时向 `ul` 元素内追加 `li` 元素即可。参考图4-11，查看列表视图在jQueryMobile中的效果。

```html
<!DOCTYPE HTML>
<HTML>
    <head>
        <title>jQuery Mobile Demo</title>
        <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
        <script src="jquery-1.6.4.min.js"></script>
        <script src="jquery.mobile-1.0rc2.min.js"></script>
    </head>
    <body>
        <!-- Main Page-->
        <div data-role="page" id="main">
            <div data-role="header">
                <h1>
                    Header
                </h1>
            </div>
            <div data-role="content">
                <ul data-role="listview" data-theme="c">
                    <li>
                        <a href="usa.HTML">USA</a>
                    </li>
                    <li>
                        <a href="uk.HTML">UK</a>
                    </li>
                    <li>
                        <a href="russia.HTML">Russia</a>
                    </li>
                </ul>
            </div>
            <div data-role="footer" class="ui-bar">
                <h1>
                    Footer
                </h1>
            </div>
        </div>
        <!-- First Page End -->
    </body>
</HTML>
```

![](img/4a75e501abc949744a790d09257a5b1e_153_0.png)

图4-11. jQueryMobile列表视图

你可以在jQueryMobile网站上了解更多相关信息。通过此链接查看演示和文档：http://jquerymobile.com/demos/1.0a4.1/。

## jQueryMobile事件处理

在jQueryMobile中，事件处理可以分为两个领域：

1.  由非jQueryMobile组件生成的事件。例如文本框、文本域、按钮、单选按钮等。
2.  由jQueryMobile组件和框架生成的事件。例如触摸事件、方向更改事件、滚动事件以及页面生命周期事件。

## 普通事件

普通事件应按照jQuery通常的方式处理。在jQuery中，有一个通用的 `bind` 方法可以通过jQuery选择器使用，它允许我们绑定任何事件。

```html
<html>
    <head>...</head>
    <body>
        <button id="mybutton">mybutton</button>
    </body>
</html>
```

```javascript
$("#mybutton").bind("click",function(event){
    alert("clicked mybutton");
});
```

jQuery还为事件提供了许多便捷方法，例如上述方法的简写形式 `click` 方法，它将回调函数绑定到点击事件。

```javascript
$("#mybutton").click(function(event){
    alert("clicked mybutton");
});
```

你可以在以下网站上了解更多关于jQuery事件的内容：
http://api.jquery.com/category/events/

现在，谈到jQueryMobile生成的事件。请注意，无论事件来源如何，所有事件都需要按照上述方式处理。以下记录的事件同样适用。

以下章节将讨论jQueryMobile框架和组件生成的各种事件。

## 触摸事件

移动设备或平板电脑上的触摸事件与传统的鼠标事件（如点击或双击）非常不同。同样地，在传统的鼠标事件中，手势操作是不可能的。jQueryMobile提供了一组用于触摸手势的新事件。这些事件在表4-2中描述。

**表4–2. *jQueryMobile触摸事件***

| 事件名称 | 描述 |
| :--- | :--- |
| Tap | 此事件在快速触摸并抬起后生成。 |
| Taphold | 这是一个触摸事件，手指（或任何物体）在屏幕上保持按住状态约一秒钟，类似于长按。 |
| Swipe | 这是一个触摸手势，其中在任意方向上进行至少30像素的水平拖动，同时将垂直移动限制在20像素以内。所有这些操作在一秒内完成。 |
| Swipeleft | 这是一个滑动事件，但滑动方向朝左。 |
| Swiperight | 这是一个滑动事件，但滑动方向朝右。 |



以下是一个关于触摸事件如何与 jQueryMobile 配合工作的示例。请参考图 4-12。

```html
<!DOCTYPE html>
<html>
    <head>
        <title>jQuery Mobile Touch Events Demo</title>
        <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
        <script src="jquery-1.6.4.min.js"></script>
        <script src="jquery.mobile-1.0rc2.min.js"></script>
        <script>
            $(document).ready(function() {
                $("#tap").bind("tap", function() {
                    alert("Tap Event");
                });
                $("#taphold").bind("taphold", function() {
                    alert("Tap Hold Event");
                });
                $("#swipe").bind("swipe", function() {
                    alert("Swipe Event");
                });
                $("#swipeleft").bind("swipeleft", function() {
                    alert("Swipe Left Event");
                });
                $("#swiperight").bind("swiperight", function() {
                    alert("Swipe Right Event");
                });
            });
        </script>
    </head>
    <body>
        <!--Main Page-->
        <div data-role="page" id="main">
            <div data-role="header">
                <h1>
                    Touch Events
                </h1>
            </div>
            <div data-role="content">
                <h1>
                    Touch Events example
                </h1>
                <p id="tap">
                    Tap here
                </p>
                <p id="taphold">
                    Tap and hold here
                </p>
                <p id="swipe">
                    Swipe in this area.
                </p>
                <p id="swipeleft">
                    Swipe Left &lt;-- in this area.
                </p>
                <p id="swiperight">
                    Swipe Right -- &gt; in this area.
                </p>
            </div>
            <div data-role="footer" class="ui-bar">
                <h1>
                    Footer
                </h1>
            </div>
        </div>
        <!-- Main Page End -->
    </body>
</html>
```

![](img/4a75e501abc949744a790d09257a5b1e_156_0.png)

图 4–12. *jQueryMobile* 触摸事件。

## 方向变化事件

手机和平板设备都可以检测并响应方向变化。这非常有用，因为手机或平板在竖屏模式和横屏模式下的宽高比是不同的。jQueryMobile 允许开发者利用这种方向变化，在两种模式下都充分利用屏幕空间。为此，你需要监听 `window` 元素的 "orientationchange" 事件。以下示例展示了这一点。请参考图 4–13 和 4–14。

```html
<!DOCTYPE html>
<html>
    <head>
        <title>jQuery Mobile Touch Events Demo</title>
        <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
        <script src="jquery-1.6.4.min.js"></script>
        <script src="jquery.mobile-1.0rc2.min.js"></script>
        <script>
            $(document).ready(function(){
                $(window).bind('orientationchange', function(event){
                    $("#placeholder").html("Orientation changed to "+event.orientation);
                });
            });
        </script>
    </head>
    <body>
        <!-- Main Page-->
        <div data-role="page" id="main">
            <div data-role="header">
                <h1>
                    Touch Events
                </h1>
            </div>
            <div data-role="content">
                <h1>
                    Orientation Events example
                </h1>
                <div id="placeholder">
                </div>
            </div>
            <div data-role="footer" class="ui-bar">
                <h1>
                    Footer
                </h1>
            </div>
        </div>
        <!-- First Page End -->
    </body>
</html>
```

![](img/4a75e501abc949744a790d09257a5b1e_158_0.png)

图 4–13. *jQueryMobile 方向变化事件*

![](img/4a75e501abc949744a790d09257a5b1e_158_1.png)

图 4–14. *jQueryMobile 方向变化事件*

## 滚动事件

移动设备的一个重要方面是能够在滚动发生时执行操作并在后台进行处理。想象一下懒加载列表，它在用户滚动列表时获取数据。

为此，你需要滚动事件（见表 4–3）。jQueryMobile 提供了滚动事件。请注意，在 iOS 上 `scrollstart` 事件可能无法按预期工作，我们建议不要在 iOS 上依赖 `scrollstart` 事件。

表 4–3. *jQueryMobile 滚动事件*

| 事件名称 | 描述 |
| --- | --- |
| scrollstart | 当滚动开始时触发此事件。请注意，在 iPhone 上此事件无法正常触发。这是因为 iOS 设备会冻结 DOM 操作。期间的所有事件会被排队，并在滚动停止时触发。 |
| scrollstop | 当滚动停止时触发此事件。 |

## 页面事件

jQueryMobile 有页面的概念。jQueryMobile 中的页面会被创建、显示和/或隐藏。jQueryMobile 提供了事件，以便开发者可以在页面创建之前、创建之后、显示之前、显示之后、隐藏之前和隐藏之后执行相应的处理。所有这些事件在表 4–4 中有文档记录。

表 4–4. *jQueryMobile 页面事件*

| 事件名称 | 描述 |
| --- | --- |
| pagebeforecreate | 在页面创建之前触发此事件。 |
| pagecreate | 在页面创建之后触发此事件。 |
| pagebeforeshow | 在页面显示之前触发此事件。 |
| pagebeforehide | 在页面隐藏之前触发此事件。 |
| pageshow | 在页面显示之后触发此事件。 |
| pagehide | 在页面隐藏之后触发此事件。 |

## PhoneGap jQueryMobile 集成

既然你已经了解了 jQueryMobile 的工作原理，让我们开始集成 PhoneGap 和 jQueryMobile 的功能来创建应用程序。

请注意，当你将 jQueryMobile 与 PhoneGap 一起使用时，有三个 JavaScript 框架，每个框架都独立引导自身。

- 1. PhoneGap 框架
- 2. jQuery 框架
- 3. jQueryMobile 框架

虽然所有框架都提供了自己的引导机制，但最好按以下顺序引导这些框架：

- 1. PhoneGap
- 2. jQuery
- 3. jQueryMobile（如果确实需要）。

以下示例展示了这一点：

```javascript
<script>
    //onDeviceReady is called when PhoneGap is initialized
    function onDeviceReady() {
        $(document).ready(function() {
            //Call any jQuery functions here
        });
    }
    document.addEventListener("deviceready", onDeviceReady);
</script>
```

## 使用 jQueryMobile 和 PhoneGap 进行本地搜索

让我们测试一下 jQueryMobile 和 PhoneGap。你将构建一个混合应用，结合 PhoneGap 的地理位置、指南针和数据库功能，以及 Google Maps Places API，并使用 jQueryMobile 构建界面。请参考图 4–15。

这个混合应用被称为本地搜索。它具有以下功能：

- 1. 允许用户在其当前位置给定半径内搜索感兴趣的地方。
- 2. 允许用户查看该地点的详情并访问其网站。
- 3. 允许用户将某个地点保存为收藏并从收藏中移除。
- 4. 允许用户浏览其已保存的收藏。
- 5. 允许用户在 Google 地图上查看所有搜索结果地点。

![](img/4a75e501abc949744a790d09257a5b1e_161_0.png)

图 4–15. 使用 jQueryMobile 和 PhoneGap 进行本地搜索

此屏幕中最重要的两个功能如下（参考图 4–16）：

- 1. 搜索按钮，用于在用户位置 5 公里半径内搜索披萨店
- 2. 收藏按钮，用于向用户显示所有标记为收藏的地点

![](img/4a75e501abc949744a790d09257a5b1e_162_0.png)

**图 4–16.** *使用 jQueryMobile 和 PhoneGap 进行本地搜索*

搜索结果可以显示为列表，也可以显示为地图上的标记。图 4–17 展示了结果如何作为列表显示。

# 第 4 章：将 PhoneGap 与 jQuery Mobile 结合使用

![](img/4a75e501abc949744a790d09257a5b1e_163_0.png)

**图 4–17.** *本地搜索结果*

当用户点击其中一个搜索结果时，会跳转到商家详情页面。此页面显示商家的名称、地址、电话号码和周边信息等详情。它还允许用户将商家条目添加到收藏中或从收藏中移除。如图 4–18 所示。



当用户将某个商家添加到收藏夹后，可以从主页面导航到收藏夹页面。在这里，用户会看到已保存为收藏的地点/商家。这些条目实际上存储在应用程序的内部数据库中（由 PhoneGap 提供）（参见图 4–19）。

同样，当用户点击其中一个条目时，会被带到详情页面。如果你注意观察，我们会看到“从收藏中移除”按钮，因为这个商家/地点已经是收藏夹的一部分。请参阅图 4–20。

**图 4–20.** 收藏夹详情。

最后但同样重要的是，所有搜索结果都绘制在 Google 地图上。为此，你需要进入主页面，点击搜索，然后点击地图标签。你将看到如图 4–21 所示的屏幕。

## 引导 PhoneGap 和 jQuery

引导按以下顺序进行：

- 当 PhoneGap JavaScript 库被调用时，引导 PhoneGap 以调用 onDeviceReady() 函数
- 在 onDeviceReady 中，引导 jQuery 以在 jQuery 加载完成后调用匿名函数

```
<script>
function onDeviceReady(){
    $(document).ready(function(){
        //Register event handlers
    });
}
document.addEventListener("deviceready",onDeviceReady);
</script>
```

## 安装必要的 JavaScript 库

对于这个项目，你需要以下 JavaScript 库

- jQuery: http://docs.jquery.com/Downloading_jQuery#Download_jQuery
- jQueryMobile: http://jquerymobile.com/download/
- jQuery ui map: http://code.google.com/p/jquery-ui-map/downloads/list
- PhoneGap: www.phonegap.com/download/

假设你的应用程序 JavaScript 文件名为 app.js，应用程序 CSS 文件名为 app.css，你的 www 文件夹结构应如图 4–22 所示。请注意 images 文件夹属于 jQueryMobile 库。

图 4–22. 本地搜索项目结构

## 本地搜索的布局

本地搜索页面是应用程序中的主页面。它需要三个输入才能执行本地搜索。

- 来自 PhoneGap 的地理位置
- 来自搜索文本框的搜索关键词
- 来自 jQueryMobile 滑块的搜索半径

一旦完成此操作，它将获取搜索结果并显示在搜索结果页面中。

```
<!-- Main Search Page -->
<div data-role="page">
    <div data-role="header">
        <h1>
            Local Search
        </h1>
    </div>
    <!-- /header -->
    <div data-role="content">
```

```
<div data-role="fieldcontain">
    <label for="search">
        Local Search
    </label>
    <input type="search" name="searchbox" id="searchbox" value="Pizza" />
</div>
<div data-role="fieldcontain">
    <label for="slider">
        Search Range(kms):
    </label>
    <input type="range" name="range" id="range" value="5" min="1" max="25" />
</div>
<div data-role="fieldcontain">
    <button name="search" id="search">
        Search
    </ postcode>
</div>
<div data-role="controlgroup" data-type="horizontal">
    <a href="#fav" data-role="button" data-icon="home">Favorites</a>
    <a href="index.html" data-role="button" data-icon="info">About us</a>
</div>
</div>
<!-- /content -->
</div>
```

## 搜索本地商家

为了搜索感兴趣的地点，我们正在使用 Google Maps Places API。可以通过对 Google Maps Places 服务端点进行 RESTful 调用来搜索感兴趣的地点。进行此 RESTful 调用需要许多参数；这些参数如表 4–5 所示。

表 4–5. Google Place API 参数

| 参数名称 | 描述 |
| --- | --- |
| API 密钥 | 你需要一个 API 密钥来告诉 Google 是你的应用程序在发起 REST 调用。你需要向 Google 注册并为你的网站生成一个密钥。访问此 URL 获取更多详情：http://code.google.com/apis/maps/signup.html |
| 纬度 | 由于 Google Maps Places 是一项地理位置服务，它需要你的坐标 |
| 经度 | 由于 Google Maps Places 是一项地理位置服务，它需要你的坐标 |
| 半径 | Google Maps Places 需要你提供一个半径来确定搜索范围 |
| 名称 | 查找地点的搜索关键词 |
| 类型 | 地点的类别；在此示例中为 "food" |

以下是带有每个参数占位符的 URL：

https://maps.googleapis.com/maps/api/place/search/json?location={latitude,longitude}&radius={radius}&types=food&name={search_keyword}&sensor=false&key={api_key}

对于以下 URL，JSON 响应如下：

https://maps.googleapis.com/maps/api/place/search/json?location=-33.8670522,151.1957362&radius=500&types=food&name=harbour&sensor=true&key=<<api_key>>

JSON 响应如下：

```
{
    "html_attributions": ["Listings by \u003ca href=\"http://www.yellowpages.com.au/\"\u003eYellow Pages\u003c/a\u003e"],
    "results": [{
        "geometry": {
            "location": {
                "lat": -33.8719640,
                "lng": 151.1985440
            }
        },
        "icon": "http://maps.gstatic.com/mapfiles/place_api/icons/restaurant-71.png",
        "id": "aefbc59325ffd5f3e93d67932375d20d143289de",
        "name": "Toros Restaurant Darling Harbour",
        "reference": "CoQBdgAAAE6oRybc1OZYNHOWeuwKzTfzjYXO8nuWyGqCqSTBoqR_BZxE30fgXsyb0l_wIRos_uuHLZqq-17DTgpGHZoSehSb0G73dfIxO3rpOak2OmNuBb5Kg63rPN_afbH_PnbILiofw6WSODYOCkqhf13BqSXyujAPkQKZU76NJypgT6mEhCg1MhyNAuyark4X8YfRg4YGTn_MXroge1HUHPe3JMCic-cHlu3A",
        "types": ["restaurant", "food", "establishment"],
        "vicinity": "Darling Dr, Sydney"
    }, ...]
}
```

请注意，在前面的 JSON 中，有一个 id 和 reference。你需要更好地理解它们才能构建你的应用程序。

id 是一个地点的唯一标识符。当你将地点/商家存储在数据库中时，你会将 id 用作主键。但是，id 不能用于获取最新信息。

reference 是用于从 Google Places 服务器获取地点/商家详情的键。但请注意，reference 在多个搜索结果中不是唯一的。

因此，你将在数据库中同时存储 id（作为主键）和 reference（作为字符串），这样你就可以唯一地标识一个地点/商家（使用 id），并随时使用 reference 从 Google Places 获取信息。

## HTML 中的整体布局

以下是应用程序的整体布局。应用程序中总共有五个页面：

- 搜索页面
- ID 为 "list" 的搜索结果页面
- ID 为 "DETAILS" 的详情页面
- ID 为 "fav" 的收藏夹列表页面
- ID 为 "map" 的地图页面

```
<!DOCTYPE HTML>
<html>
<head>
    <title>PhoneGap</title>
    <link rel="stylesheet" type="text/css" href="app.css" />
    <script type="text/javascript"
src="http://maps.google.com/maps/api/js?sensor=true"></script>
    <script type="text/javascript" src="jquery.ui.map.min.js"></script>
    <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
    <script src="jquery-1.6.4.min.js"></script>
    <script src="jquery.mobile-1.0rc2.min.js"></script>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript" src="app.js"></script>
</head>
<body>
    <!-- Main Search Page -->
    <div data-role="page">
        <div data-role="header">
            <h1>
                Local Search
            </h1>
        </div>
        <!-- /header -->
        <div data-role="content">
            <div data-role="fieldcontain">
                <label for="search">
                    Local Search
                </label>
                <input type="search" name="searchbox" id="searchbox" value="Pizza" />
            </div>
            <div data-role="fieldcontain">
                <label for="slider">
                    Search Range(kms):
                </label>
                <input type="range" name="range" id="range" value="5" min="1"
max="25" />
            </div>
```



## 第4章：结合jQuery Mobile使用PhoneGap

```html
<div data-role="fieldcontain">
    <button name="search" id="search">
        Search
    </button>
</div>
<div data-role="controlgroup" data-type="horizontal">
    <a href="#fav" data-role="button" data-icon="home">Favorites</a>
    <a href="index.html" data-role="button" data-icon="info">About us</a>
</div>
</div>
<!-- /content -->
</div>
<!-- /page -->
<!-- Search Result List Page -->
<div data-role="page" id="list">
    <div data-role="header" data-position="fixed">
        <h1>
            Result
        </h1>
    </div>
    <!-- /header -->
    <div data-role="content">
        <ul id="result-list" data-role="listview" data-theme="g">
        </ul>
    </div>
    <!-- /content -->
    <div data-role="footer" data-id="result-footer" data-position="fixed"
         class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay"
         role="contentinfo" style="top: -1263px; ">
        <div data-role="navbar" class="ui-navbar ui-navbar-noicons"
             role="navigation">
            <ul class="ui-grid-a">
                <li class="ui-block-a">
                    <a href="#list" data-theme="a"
                       class="ui-btn-active ui-state-persist ui-btn ui-btn-up-a">
                        <span class="ui-btn-inner"><span class="ui-btn-text">List</span></span>
                    </a>
                </li>
                <li class="ui-block-b">
                    <a href="#map" data-theme="a"
                       class="ui-state-persist ui-btn ui-btn-up-a">
                        <span class="ui-btn-inner"><span class="ui-btn-text">Maps</span></span>
                    </a>
                </li>
            </ul>
        </div>
        <!-- /navbar -->
    </div>
    <!-- /footer -->
</div>
<!-- /page -->
<!-- Maps Page -->
<div data-role="page" id="map">
    <div data-role="header">
        <h1>
            Map
        </h1>
    </div>
    <!-- /header -->
    <div data-role="content" class="map-content">
        <div id="map_canvas">
        </div>
    </div>
    <!-- /content -->
    <div data-role="footer" data-id="result-footer"
        data-position="fixed"
        class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay"
        role="contentinfo" style="top: -1263px; ">
        <div data-role="navbar" class="ui-navbar ui-navbar-noicons"
        role="navigation">
            <ul class="ui-grid-a">
                <li class="ui-block-a">
                    <a href="#list" data-theme="a" class="ui-state-persist ui-btn ui-btn-up-a">
                        <span class="ui-btn-inner"><span class="ui-btn-text">List</span></span>
                    </a>
                </li>
                <li class="ui-block-b">
                    <a href="#map" data-theme="a"
                        class="ui-btn-active ui-state-persist ui-btn ui-btn-up-a">
                        <span class="ui-btn-inner"><span class="ui-btn-text">Maps</span></span>
                    </a>
                </li>
            </ul>
        </div>
        <!-- /navbar -->
    </div>
    <!-- /footer -->
</div>
<!-- /page -->
<!--Favorite List Page -->
<div data-role="page" id="fav">
    <div data-role="header">
        <h1>
            Favorites
        </h1>
    </div>
    <!-- /header -->
    <div data-role="content">
        <!--
            <ul id="fav-list" data-role="listview" data-theme="g"></ul>
        -->
        <ul id="fav-list" data-role="listview" data-theme="g">
        </ul>
    </div>
    <!-- /content -->
    <div data-role="footer" data-id="result-footer" data-position="fixed"
        class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay" >
        <div data-role="navbar" class="ui-navbar ui-navbar-noicons"
            role="navigation">
            <ul class="ui-grid-a">
                <li class="ui-block-a">
                    <a href="#list" data-theme="a" class="ui-state-persist ui-btn ui-btn-up-a">
                        <span class="ui-btn-inner"><span class="ui-btn-text">List</span></span>
                    </a>
                </li>
                <li class="ui-block-b">
                    <a href="#map" data-theme="a"
                        class="ui-btn-active ui-state-persist ui-btn ui-btn-up-a">
                        <span class="ui-btn-inner"><span class="ui-btn-text">Maps</span></span>
                    </a>
                </li>
            </ul>
        </div>
        <!-- /navbar -->
    </div>
    <!-- /footer -->
</div>
<!-- /page -->
<!-- Business Details Page -->
<div data-role="page" id="details">
    <div data-role="header">
        <h1>
            Business Details
        </h1>
    </div>
    <!-- /header -->
    <div data-role="content">
        <table summary="Business Details">
            <caption>
                <h3>
                    Business Details
                </h3>
            </caption>
            <tfoot>
                <tr>
                    <td colspan="2">
                        <div id="remove">
                            <button id="removefav" data-role="button">
                                Remove to Favorite
                            </button>
                        </div>
                        <div id="add">
                            <button id="addfav" data-role="button">
                                Add to Favorite
                            </button>
                        </div>
                    </td>
                </tr>
                <tr>
                    <td colspan="2">
                        <a id="homepage" data-role="button" href="">Visit HomePage</a>
                    </td>
                </tr>
            </tfoot>
            <tbody>
                <tr>
                    <th scope="row">
                        Name
                    </th>
                    <td id="name">
                        ...
                    </td>
                </tr>
                <tr>
                    <th scope="row">
                        Address
                    </th>
                    <td id="address">
                        ...
                    </td>
                </tr>
                <tr>
                    <th scope="row">
                        Phone
                    </th>
                    <td id="phone">
                        ...
                    </td>
                </tr>
                <tr>
                    <th scope="row">
                        Rating
                    </th>
                    <td id="rating">
                        ...
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <!-- /content -->
</div>
<!-- /page -->
</body>
</html>
```

## 获取和显示搜索结果

函数启动的搜索将搜索按钮事件与实际执行搜索的函数绑定在一起。

以下是搜索的事件流程：

1.  显示一个加载图标给用户，让他/她知道一个长时间的操作正在进行。这是通过调用 `$.mobile.showPageLoadingMsg();` 来完成的。
2.  使用 PhoneGap 函数 `navigator.geolocation.getCurrentPosition(successCallback, failureCallback)` 获取用户当前位置。
3.  在上述调用的 successCallback 中，使用以下参数向 Google Places 发送一个 JSON 请求：
    a. 地理位置
    b. 搜索关键词
    c. 从地理位置开始的搜索半径
    d. Google Places 的开发者 API 密钥
    e. `var url="https://maps.googleapis.com/maps/api/place/search/json?location="+position.coords.latitude+","+position.coords.longitude+"&radius="+radius+"&name="+$("#searchbox").val()+"&sensor=true&key=<API_Key>";`
4.  使用 jQuery 的 `$.getJSON()` 发起一个 Ajax 请求到 Google Places 以获取 JSON 响应。请注意，由于 PhoneGap 应用程序没有域名，你不受浏览器单源策略的限制。向 `$.getJSON()` 函数注册一个 successCallback 和一个 failureCallback。
5.  在上述调用的 successCallback 中，获取地点响应并将其追加到 id 为 "result-list" 的 ul 元素。这个 ul 元素在 HTML 代码中被标注为 jQueryMobile 列表视图。一旦你将必要的 li 元素添加到 ul 元素，我们将调用 `$("result-list").listView("refresh")` 将 ul 元素重绘为 jQueryMobile 列表。
6.  注意，你将每个地点的 JSON 响应的引用部分作为链接（一个 `<a>` 元素）的 id。你这样做是为了当用户点击此条目时，他会跳转到详情页面。请注意，这个链接的 href 部分实际上是 "#details"。
7.  最后，你为地点的点击事件绑定一个点击处理程序，这样在导航用户到详情页面之前，你实际上可以向 Google Places 服务器发起调用以获取商业/地点条目的详细信息。
8.  最后一步是通过调用 `$.mobile.hidePageLoadingMsg();` 移除加载图标。

```javascript
/**
 * Binding Search button handler to go and fetch place results
 */
function initiateSearch(){
    $("#search").click(function(){
        try {
            $.mobile.showPageLoadingMsg();
            navigator.geolocation.getCurrentPosition(function(position){
                var radius = $("#range").val() * 1000;
                mapdata = new google.maps.LatLng(position.coords.latitude, position.coords.longitude);
                var url = "https://maps.googleapis.com/maps/api/place/search/json?location=" + position.coords.latitude + "," + position.coords.longitude + "&radius=" + radius + "&name=" + $("#searchbox").val() + "&sensor=false&key=AIzaSyC4vCfT_Knq1SGuNMahZqyrmZFiTuBsdlY";
                $.getJSON(url, function(data){
                    cachedData = data;
                    $("#result-list").html("");
                    try {
                        $(data.results).each(function(index, entry){
                            var htmlData = "<a href=\"#details\" id=\"" + entry.reference + "\"><img src=\"" + entry.icon + "\" class=\"ui-li-icon\"></img><h3>&nbsp;" + entry.name +
```

## 显示地点/商家详情

你在上面已经看到，当用户点击显示地点搜索结果列表中的某个地点条目时，会调用 `fetchDetails()` 函数。

`fetchDetails()` 函数的流程如下：

1.  显示一个加载图标。这是通过调用 `$.mobile.showPageLoadingMsg()` 完成的。
2.  详情地点的所有字段都被重置为空。例如，`$(“#name”).html();`。
3.  创建一个详情地点请求的 URL (`detailsURL`)，并使用 jQuery 的 `$.getJSON()` 调用发起 Ajax 请求。
4.  在 `$.getJSON()` 的 `successCallback` 中，你会得到页面的详情。这里你首先检查给定的地点是否已被用户收藏为收藏夹。根据此结果，向用户显示“添加到收藏夹”或“从收藏夹移除”按钮。
5.  填充此页面的字段。
6.  通过调用 `$.mobile.hidePageLoadingMsg()` 移除加载图标。

```javascript
/**
 * Fetch the details of a place/business. This function is called before user navigates to details page
 * @param {Object} reference
 */
function fetchDetails(entry){

    currentBusinessData = null;

    $.mobile.showPageLoadingMsg();
    var detailsUrl = "https://maps.googleapis.com/maps/api/place/details/json?reference=" +
        entry.reference + "&sensor=true&key=<API_Key>";
        $("#name").html("");
        $("#address").html("");
        $("#phone").html("");
        $("#rating").html("");
        $("#homepage").attr("href", "");

        $.getJSON(detailsUrl, function(data){
            if (data.result) {
                currentBusinessData = data.result;

                isFav(currentBusinessData, function(isPlaceFav){
                    console.log(currentBusinessData.name+" is fav "+isPlaceFav);
                    if (!isPlaceFav) {

                        $("#add").show();
                        $("#remove").hide();
                    }
                    else {

                        $("#add").hide();
                        $("#remove").show();
                    }
                    $("#name").html(data.result.name);
                    $("#address").html(data.result.formatted_address);
                    $("#phone").html(data.result.formatted_phone_number);
                    $("#rating").html(data.result.rating);
                    $("#homepage").attr("href", data.result.url);

        });
    });
}
}).error(function(err){
    console.log("Got Error while fetching details of Business " + err);
}).complete(function(){
    $.mobile.hidePageLoadingMsg();
});
}
```

# 将地点/商家添加和移除收藏夹

下一步是实际查看：

1.  我们如何将地点添加到收藏夹列表？
2.  我们如何从收藏夹列表移除地点？
3.  我们如何查找给定地点是否是我们收藏夹列表的一部分？

这里需要注意的是，你正在使用 PhoneGap 的数据库 API 来存储、检索和删除地点。所有这些信息都使用 PhoneGap 的数据库 API 存储在应用程序的数据库中。你将在名为 "favorite" 的表中存储收藏夹。

`initiateFavButton()` 将“添加到收藏夹”和“从收藏夹移除”按钮的点击处理程序绑定到实际的处理程序。“添加到收藏夹”按钮位于 id 为 "add" 的 div 中，“从收藏夹移除”按钮位于 id 为 "remove" 的 div 中。你通过隐藏或显示这些 div 来控制按钮的可见性。你还会分别调用 `addToFavorite()` 和 `removeFromFavorite()` 方法来实际执行添加和移除操作。

```javascript
/**
 * Called to bind the "Add to Favorite" Button
 */

function initiateFavButton() {
    $("#removefav").click(function () {

        try {
            if (currentBusinessData != null) {
                removeFromFavorite(currentBusinessData);
                $("#add").show();
                $("#remove").hide();

            }
        } catch (err) {
            console.log("Got Error while removing " + currentBusinessData.name + " error " + err);
        }

    });

    $("#addfav").click(function () {
        try {
            if (currentBusinessData != null) {
                addToFavorite(currentBusinessData);
                $("#add").hide();
                $("#remove").show();
            }
        } catch (err) {
            console.log("Got Error while adding " + currentBusinessData.name + " error " + err);
        }
    });
}
```

`ensureTableExists()` 是所有其他数据库函数使用的通用函数。此函数确保在对数据库执行任何插入、选择或删除操作之前，执行 SQL 脚本 "CREATE TABLE IF NOT EXISTS Favorite (id unique, reference, name, address, phone, rating, icon, vicinity)"。

```javascript
/**
 * Ensure we have the table before we use it
 * @param {Object} tx
 */
function ensureTableExists(tx) {
    tx.executeSql('CREATE TABLE IF NOT EXISTS Favorite (id unique, reference, name,address,phone,rating,icon,vicinity)');
}
```

`addToFavorite()` 是实际将给定地点插入收藏夹表的函数。请注意，你正在数据库表 "favorite" 中存储 id、reference、name、icon、formatted_address、formatted_phone_number、rating 和 vicinity。

```javascript
/**
 * Add current business data to favorite
 * @param {Object} data
 */
function addToFavorite(data) {
    var db = window.openDatabase("Favorites", "1.0", "Favorites", 20000000);

    db.transaction(function (tx) {
        ensureTableExists(tx);
        var id = (data.id != null) ? ("'" + data.id + "'") : ("");
        var reference = (data.reference != null) ? ("'" + data.reference + "'") : ("");
        var name = (data.name != null) ? ("'" + data.name + "'") : ("");
        var address = (data.formatted_address != null) ? ("'" + data.formatted_address + "'") : ("");
        var phone = (data.formatted_phone_number != null) ? ("'" + data.formatted_phone_number + "'") : ("");
        var rating = (data.rating != null) ? ("'" + data.rating + "'") : ("");
        var icon = (data.icon != null) ? ("'" + data.icon + "'") : ("");
        var vicinity = (data.vicinity != null) ? ('"' + data.vicinity + '"') : ('""');
        var insertStmt = 'INSERT INTO Favorite (id,reference,name,address,phone,rating,icon,vicinity) VALUES (' + id + ',' + reference + ',' + name + ',' + address + ',' + phone + ',' + rating + ',' + icon + ',' + vicinity + ')';
        tx.executeSql(insertStmt);
    }, function (error) {
        console.log("Data insert failed " + error.code + "  " + error.message);
    }, function () {
        console.log("Data insert successful");
    });
}
```

`removeFromFavorite()` 是从 "favorite" 表中移除收藏夹的函数。它只需要 id 即可完成此操作。

```javascript
/**
 * Remove current business data from favorite
 * @param {Object} data
 */
function removeFromFavorite(data) {
    try {
        var db = window.openDatabase("Favorites", "1.0", "Favorites", 2000000);

        db.transaction(function (tx) {
            ensureTableExists(tx);
            var deleteStmt = "DELETE FROM Favorite WHERE id = '" + data.id + "'";
            console.log(deleteStmt);
            tx.executeSql(deleteStmt);

        }, function (error) {
            console.log("Data Delete failed " + error.code + "  " + error.message);
        }, function () {
            console.log("Data Delete successful");
        });
    } catch (err) {
        console.log("Caught exception while deleting favorite " + data.name);
    }
}
```

`isFav()` 是查询 "favorite" 表以确定给定地点/商家是否已存在于表中，从而被用户标记为收藏夹的函数。

```javascript
/**
 *
 * @param {Object} reference
 * @return true if place is favorite else false
 */
function isFav(data, callback) {
    var db = window.openDatabase("Favorites", "1.0", "Favorites", 200000);
    try {
        db.transaction(function (tx) {
            ensureTableExists(tx);
```



```html
var sql = "SELECT * FROM Favorite where id='" + data.id + "'";
tx.executeSql(sql, [], function (tx, results) {

    var result = (results != null && results.rows != null &&
    results.rows.length > 0);

    callback(result);
}, function (tx, error) {

    console.log("Got error in isFav error.code =" + error.code + " error.message = " + error.message);
    callback(false);

});
} catch (err) {
    console.log("Got error in isFav " + err);
    callback(false);
}
```

## 加载您收藏的地点

到目前为止，您已经向收藏夹中添加和移除地点。您还看到了如何检查一个地点是否被用户设置为他的/她的收藏。现在，让我们来看看检索用户所有收藏地点的代码。

当用户点击主页上的“收藏夹”按钮时，会调用此代码。

此代码与 `isFav()` 非常相似，只不过这里您将实际从“收藏”表中获取所有条目，获取结果集，并填充 id 为“fav-list”的无序列表（UL）。

填充部分类似于显示搜索结果。

请注意，每次用户导航到“收藏地点”时，您都会从数据库表“favorites”中获取结果。这是通过监听页面的“pagebeforeshow”事件来实现的。“pagebeforeshow”事件在 jQueryMobile 页面向用户显示之前触发。

```
/**
 * 每次用户导航到收藏夹之前调用
 */

function initiateFavorites() {
    $("#fav").live("pagebeforeshow", function () {

        var db = window.openDatabase("Favorites", "1.0", "Favorites", 200000);
        try {
            db.transaction(function (tx) {
                tx.executeSql('SELECT * FROM Favorite', [], function (tx, results) {

                    $("#fav-list").html("");
                    if (results != null && results.rows != null) {
                        for (var index = 0; index < results.rows.length; index++) {
                            var entry = results.rows.item(index)

                            var htmlData = "<a href=\"#details\" id=\"" +
                            entry.reference + "\"><img src=\"" + entry.icon + "\" class=\"ui-li-icon\"></img><h3>&nbsp;" + entry.name + "</h3><p><strong>&nbsp;vicinity:" + entry.vicinity + "</strong></p></a>";

                            var liElem = $(document.createElement('li'));

                            $("#fav-list").append(liElem.html(htmlData));

                            $(liElem).bind("tap", function (event) {
                                event.stopPropagation();
                                fetchDetails(entry);
                                return true;
                            });

                        }
                        $("#fav-list").listview('refresh');

                    }
                }, function (error) {
                    console.log("Got error fetching favorites " + error.code + " " + error.message);
                });
            });
        } catch (err) {
            console.log("Got error while reading favorites " + err);
        }

    });
}
```

## 在地图上显示搜索结果

本练习的最后一个部分是在 Google 地图上显示地点的搜索结果。这有助于用户更好地了解地点的位置。在 `initiateSearch()` 函数中，当您收到搜索结果时，您将结果缓存在一个名为“cachedData”的 JavaScript 变量中。在这里，您将实际使用相同的数据在地图上绘制标记。

请注意，每次用户导航到“收藏地点”时，您都会重绘地图并根据 cachedData 绘制标记。这是通过监听页面的“pagebeforeshow”事件来实现的。

```
/**
 * 用于初始化地图页面
 */

function initiateMap() {
    $("#map").live("pagebeforecreate", function () {
        try {
            $('#map_canvas').gmap({
                'center': mapdata,
                'zoom': 12,
                'callback': function (map) {
                    $(cachedData.results).each(function (index, entry) {
                        $('#map_canvas').gmap('addMarker', {
                            'position': new google.maps.LatLng(entry.geometry.location.lat, entry.geometry.location.lng),
                            'animation': google.maps.Animation.DROP
                        }, function (map, marker) {
                            $('#map_canvas').gmap('addInfoWindow', {
                                'position': marker.getPosition(),
                                'content': entry.name
                            }, function (iw) {
                                $(marker).click(function () {
                                    iw.open(map, marker);
                                    map.panTo(marker.getPosition());
                                });
                            });
                        });
                    });
                }
            });

            console.log("Map initialized");
        } catch (err) {
            console.log("Got error while initializing map " + err);
        }

    });
}
```

## 完整源代码

以下是 index.html 的完整源代码：

```html
<!DOCTYPE HTML>
<html>

<head>
    <title>PhoneGap</title>
    <link rel="stylesheet" type="text/css" href="app.css" />
    <script type="text/javascript" src="http://maps.google.com/maps/api/js?sensor=true"></script>
    <script type="text/javascript" src="jquery.ui.map.min.js"></script>
    <link href="jquery.mobile-1.0rc2.min.css" rel="stylesheet" type="text/css"/>
    <script src="jquery-1.6.4.min.js"></script>
    <script src="jquery.mobile-1.0rc2.min.js"></script>
    <script type="text/javascript" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript" src="app.js"></script>
</head>

<body>
    <!-- 主搜索页面 -->
    <div data-role="page">
        <div data-role="header">
            <h1>
                本地搜索
            </h1>
        </div>
        <!-- /header -->
        <div data-role="content">
            <div data-role="fieldcontain">
                <label for="search">
                    本地搜索
                </label>
                <input type="search" name="searchbox" id="searchbox" value="Pizza" />
            </div>
            <div data-role="fieldcontain">
                <label for="slider">
                    搜索范围（公里）：
                </label>
                <input type="range" name="range" id="range" value="5" min="1" max="25" />
            </div>
            <div data-role="fieldcontain">
                <button name="search" id="search">
                    搜索
                </button>
            </div>
            <div data-role="controlgroup" data-type="horizontal">
                <a href="#fav" data-role="button" data-icon="home">收藏夹</a>
                <a href="index.html" data-role="button" data-icon="info">关于我们</a>
            </div>
        </div>
        <!-- /content -->
    </div>
    <!-- /page -->
    <!-- 搜索结果列表页面 -->
    <div data-role="page" id="list">
        <div data-role="header" data-position="fixed">
            <h1>
                结果
            </h1>
        </div>
        <!-- /header -->
        <div data-role="content">
            <ul id="result-list" data-role="listview" data-theme="g">
            </ul>
        </div>
        <!-- /content -->
        <div data-role="footer" data-id="result-footer" data-position="fixed" class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay" role="contentinfo" style="top: -1263px; ">
            <div data-role="navbar" class="ui-navbar ui-navbar-noicons" role="navigation">
                <ul class="ui-grid-a">
                    <li class="ui-block-a">
                        <a href="#list" data-theme="a" class="ui-btn-active ui-state-persist ui-btn ui-btn-up-a"><span class="ui-btn-inner"><span class="ui-btn-text">列表</span></span></a>
                    </li>
                    <li class="ui-block-b">
                        <a href="#map" data-theme="a" class="ui-state-persist ui-btn ui-btn-up-a"><span class="ui-btn-inner"><span class="ui-btn-text">地图</span></span></a>
                    </li>
                </ul>
            </div>
            <!-- /navbar -->
        </div>
        <!-- /footer -->
    </div>
    <!-- /page -->
    <!-- 地图页面 -->
    <div data-role="page" id="map">
        <div data-role="header">
            <h1>
                地图
            </h1>
        </div>
        <!-- /header -->
        <div data-role="content" class="map-content">
            <div id="map_canvas">
            </div>
        </div>
        <!-- /content -->
        <div data-role="footer" data-id="result-footer" data-position="fixed" class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay" role="contentinfo" style="top: -1263px; ">
            <div data-role="navbar" class="ui-navbar ui-navbar-noicons" role="navigation">
                <ul class="ui-grid-a">
                    <li class="ui-block-a">
                        <a href="#list" data-theme="a" class="ui-state-persist ui-btn ui-btn-up-a"><span class="ui-btn-inner"><span class="ui-btn-text">列表</span></span></a>
                    </li>
                    <li class="ui-block-b">
                        <a href="#map" data-theme="a" class="ui-btn-active ui-state-persist ui-btn ui-btn-up-a"><span class="ui-btn-inner"><span class="ui-btn-text">地图</span></span></a>
                    </li>
                </ul>
            </div>
            <!-- /navbar -->
        </div>
        <!-- /footer -->
    </div>
    <!-- /page -->
    <!-- 收藏夹列表页面 -->
    <div data-role="page" id="fav">
        <div data-role="header">
            <h1>
                收藏的地点
            </h1>
        </div>
        <!-- /header -->
        <div data-role="content">
            <ul id="fav-list" data-role="listview" data-theme="g">
            </ul>
        </div>
        <!-- /content -->
        <div data-role="footer" data-id="result-footer" data-position="fixed" class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay" role="contentinfo" style="top: -1263px; ">
            <div data-role="navbar" class="ui-navbar ui-navbar-noicons" role="navigation">
                <ul class="ui-grid-a">
                    <li class="ui-block-a">
                        <a href="#list" data-theme="a" class="ui-state-persist ui-btn ui-btn-up-a"><span class="ui-btn-inner"><span class="ui-btn-text">列表</span></span></a>
                    </li>
                    <li class="ui-block-b">
                        <a href="#map" data-theme="a" class="ui-state-persist ui-btn ui-btn-up-a"><span class="ui-btn-inner"><span class="ui-btn-text">地图</span></span></a>
                    </li>
                </ul>
            </div>
            <!-- /navbar -->
        </div>
        <!-- /footer -->
    </div>
    <!-- /page -->
</body>

</html>
```



## 收藏夹

<!-- /header -->
<div data-role="content">
    <!-- <ul id="fav-list" data-role="listview" data-theme="g"> -->
    <ul id="fav-list" data-role="listview" data-theme="g">
    </ul>
</div>
<!-- /content -->
<div data-role="footer" data-id="result-footer" data-position="fixed"
class="ui-bar-a ui-footer ui-footer-fixed fade ui-fixed-overlay" role="contentinfo" style="top: -1263px; ">
    <!-- /navbar -->
</div>
<!-- /footer -->
</div>
<!-- /page -->
<!-- 商家详情页 -->
<div data-role="page" id="details">
    <div data-role="header">
        <h1>
            商家详情
        </h1>
    </div>
    <!-- /header -->
    <div data-role="content">
        <table summary="Business Details">
            <caption>
                <h3>
                    商家详情
                </h3>
            </caption>
            <tfoot>
                <tr>
                    <td colspan="2">
                        <div id="remove">
                            <button id="removefav" data-role="button">
                                移除收藏
                            </button>
                        </div>
                        <div id="add">
                            <button id="addfav" data-role="button">
                                添加收藏
                            </button>
                        </div>
                    </td>
                </tr>
                <tr>
                    <td colspan="2">
                        <a id="homepage" data-role="button" href="">访问主页</a>
                    </td>
                </tr>
            </tfoot>
            <tbody>
                <tr>
                    <th scope="row">
                        名称
                    </th>
                    <td id="name">
                        ...
                    </td>
                </tr>
                <tr>
                    <th scope="row">
                        地址
                    </th>
                    <td id="address">
                        ...
                    </td>
                </tr>
                <tr>
                    <th scope="row">
                        电话
                    </th>
                    <td id="phone">
                        ...
                    </td>
                </tr>
                <tr>
                    <th scope="row">
                        评分
                    </th>
                    <td id="rating">
                        ...
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <!-- /content -->
</div>
<!-- /page -->
</body>
</html>

`app.js` 的完整源代码如下。请注意，您需要将 `<API_Key>` 替换为您自己的密钥。您可以从 http://code.google.com/apis/maps/documentation/places 获取 API 密钥。

```
var mapdata = null;

var cachedData = null;

var currentBusinessData = null;
/**
 * 获取地点/商家的详细信息。此函数在用户导航到详情页之前调用
 * @param {Object} reference
 */
function fetchDetails(entry) {

    currentBusinessData = null;

    $.mobile.showPageLoadingMsg();
    var detailsUrl =
        "https://maps.googleapis.com/maps/api/place/details/json?reference=" + entry.reference +
        "&sensor=true&key=<API_Key>";
    $("#name").html("");
    $("#address").html("");
    $("#phone").html("");
    $("#rating").html("");
    $("#homepage").attr("href", "");

    $.getJSON(detailsUrl, function (data) {
        if (data.result) {
            currentBusinessData = data.result;

            isFav(currentBusinessData, function (isPlaceFav) {
                console.log(currentBusinessData.name + " is fav " + isPlaceFav);
                if (!isPlaceFav) {

                    $("#add").show();
                    $("#remove").hide();
                } else {

                    $("#add").hide();
                    $("#remove").show();
                }
                $("#name").html(data.result.name);
                $("#address").html(data.result.formatted_address);
                $("#phone").html(data.result.formatted_phone_number);
                $("#rating").html(data.result.rating);
                $("#homepage").attr("href", data.result.url);

            });


        }
    }).error(function (err) {
        console.log("Got Error while fetching details of Business " + err);
    }).complete(function () {
        $.mobile.hidePageLoadingMsg();
    });

}

//------------------------------
/**
 * 用于初始化地图页面
 */
function initiateMap() {
    $("#map").live("pagebeforecreate", function () {
        try {

            $('#map_canvas').gmap({
                'center': mapdata,
                'zoom': 12,
                'callback': function (map) {
                    $(cachedData.results).each(function (index, entry) {
                        $('#map_canvas').gmap('addMarker', {
                            'position': new google.maps.LatLng(entry.geometry.location.lat, entry.geometry.location.lng),
                            'animation': google.maps.Animation.DROP
                        }, function (map, marker) {
                            $('#map_canvas').gmap('addInfoWindow', {
                                'position': marker.getPosition(),
                                'content': entry.name
                            }, function (iw) {
                                $(marker).click(function () {

                                    iw.open(map, marker);

                                    map.panTo(marker.getPosition());
                                });
                            });
                        });
                    });
                }
            });
            console.log("Map initialized");
        } catch (err) {
            console.log("Got error while initializing map " + err);
        }
    });

}

//------------------------------
/**
 * 用于绑定"添加收藏"按钮
 */
function initiateFavButton() {
    $("#removefav").click(function () {

        try {
            if (currentBusinessData != null) {
                removeFromFavorite(currentBusinessData);
                $("#add").show();
                $("#remove").hide();
            }
        } catch (err) {
            console.log("Got Error while removing " + currentBusinessData.name + " error " + err);
        }
    });

    $("#addfav").click(function () {
        try {
            if (currentBusinessData != null) {
                addToFavorite(currentBusinessData);
                $("#add").hide();
                $("#remove").show();
            }
        } catch (err) {
            console.log("Got Error while adding " + currentBusinessData.name + " error " + err);
        }
    });
}

/*
 * 每次在用户导航到收藏夹之前调用
 */
function initiateFavorites() {
    $("#fav").live("pagebeforeshow", function () {
        var db = window.openDatabase("Favorites", "1.0", "Favorites", 200000);
        try {
            db.transaction(function (tx) {
                tx.executeSql('SELECT * FROM Favorite', [], function (tx, results) {
                    $("#fav-list").html("");
                    if (results != null && results.rows != null) {
                        for (var index = 0; index < results.rows.length; index++) {
                            var entry = results.rows.item(index)
                            var htmlData = "<a href=\"#details\" id=\"" + entry.reference + "\"><img src=\"" + entry.icon + "\" class=\"ui-li-icon\"></img><h3>&nbsp;" + entry.name + "</h3><p><strong>&nbsp;vicinity:" + entry.vicinity + "</strong></p></a>";
                            var liElem = $(document.createElement('li'));
                            $("#fav-list").append(liElem.html(htmlData));
                            $(liElem).bind("tap", function (event) {
                                event.stopPropagation();
                                fetchDetails(entry);
                                return true;
                            });
                        }
                        $("#fav-list").listview('refresh');
                    }
                }, function (error) {
                    console.log("Got error fetching Favorites " + error.code + " " + error.message);
                });
            });
        } catch (err) {
            console.log("Got error while reading Favorites " + err);
        }
    });
}

//-----------------------------------------------------------------
/**
 * 确保在使用表之前它已存在
 * @param {Object} tx
 */
function ensureTableExists(tx) {
    tx.executeSql('CREATE TABLE IF NOT EXISTS Favorite (id unique, reference, name,address,phone,rating,icon,vicinity)');
}

//-----------------------------------------------------------------
/**
 * 将当前商家数据添加到收藏夹
 * @param {Object} data
 */
function addToFavorite(data) {
    var db = window.openDatabase("Favorites", "1.0", "Favorites", 20000000);

    db.transaction(function (tx) {
        ensureTableExists(tx);
        var id = (data.id != null) ? ('"' + data.id + '"') : ('""');
        var reference = (data.reference != null) ? ('"' + data.reference + '"') : ('""');
        var name = (data.name != null) ? ('"' + data.name + '"') : ('""');
        var address = (data.formatted_address != null) ? ('"' + data.formatted_address + '"') : ('""');
        var phone = (data.formatted_phone_number != null) ? ('"' + data.formatted_phone_number + '"') : ('""');
        var rating = (data.rating != null) ? ('"' + data.rating + '"') : ('""');
        var icon = (data.icon != null) ? ('"' + data.icon + '"') : ('""');
        var vicinity = (data.vicinity != null) ? ('"' + data.vicinity + '"') : ('""');
        var insertStmt = 'INSERT INTO Favorite (id,reference,name,address,phone,rating,icon,vicinity) VALUES (' + id + ',' + reference + ',' + name + ',' + address + ',' + phone + ',' + rating + ',' + icon + ',' + vicinity + ')';
        tx.executeSql(insertStmt);
```



 }, function (error) {
    console.log("数据插入失败 " + error.code + " " + error.message);
}, function () {
    console.log("数据插入成功");
});
}
```

```
//---------------------------------------------------------------------
/**
 * 从收藏夹中移除当前业务数据
 * @param {Object} data
 */
function removeFromFavorite(data) {
    try {
        var db = window.openDatabase("Favorites", "1.0", "Favorites", 20000000);

        db.transaction(function (tx) {
            ensureTableExists(tx);
            var deleteStmt = "DELETE FROM Favorite WHERE id = '" + data.id + "'";
            console.log(deleteStmt);
            tx.executeSql(deleteStmt);

        }, function (error) {
            console.log("数据删除失败 " + error.code + " " + error.message);
        }, function () {
            console.log("数据删除成功");
        });
    } catch (err) {
        console.log("删除收藏夹条目时发生异常 " + data.name);
    }
}
```

```
//---------------------------------------------------------------------
/**
 * @param {Object} data
 * @return 如果该地点是收藏夹条目则返回 true，否则返回 false
 */
function isFav(data, callback) {
    var db = window.openDatabase("Favorites", "1.0", "Favorites", 200000);
    try {
        db.transaction(function (tx) {
            ensureTableExists(tx);
            var sql = "SELECT * FROM Favorite where id='" + data.id + "'";
            tx.executeSql(sql, [], function (tx, results) {

                var result = (results != null && results.rows != null && results.rows.length > 0);

                callback(result);
            }, function (tx, error) {
                console.log("isFav 函数中发生错误，error.code = " + error.code + " error.message = " + error.message);
                callback(false);

            });
        });
    } catch (err) {
        console.log("isFav 函数中发生错误 " + err);
        callback(false);
    }
}
```

```
//----------------------------------------------------------------------
/**
 * 绑定搜索按钮处理器以获取地点结果
 */
function initiateSearch() {
    $("#search").click(function () {
        try {
            $.mobile.showPageLoadingMsg();

            navigator.geolocation.getCurrentPosition(function (position) {

                var radius = $("#range").val() * 1000;
                mapdata = new google.maps.LatLng(position.coords.latitude, position.coords.longitude);
                var url = "https://maps.googleapis.com/maps/api/place/search/json?location=" + position.coords.latitude + "," + position.coords.longitude + "&radius=" + radius + "&name=" + $("#searchbox").val() + "&sensor=true&key=<API_Key>";
                $.getJSON(url, function (data) {
                    cachedData = data;
                    $("#result-list").html("");
                    try {
                        $(data.results).each(function (index, entry) {
                            var htmlData = "<a href=\"#details\" id=\"" + entry.reference + "\"><img src=\"" + entry.icon + "\" class=\"ui-li-icon\"></img><h3>&nbsp;" + entry.name + "</h3><p><strong>&nbsp;附近区域:</strong> " + entry.vicinity + "</strong></p></a>";
                            var liElem = $(document.createElement('li'));
                            $("#result-list").append(liElem.html(htmlData));
                            $(liElem).bind("tap", function (event) {
                                event.stopPropagation();
                                fetchDetails(entry);

                                return true;
                            });
                        });

                        $("#result-list").listview('refresh');
                    } catch (err) {

                        console.log("将搜索结果显示在结果页面时发生错误 " + err);

                    }
                    $.mobile.changePage("list");
                    $.mobile.hidePageLoadingMsg();
                }).error(function (xhr, textStatus, errorThrown) {
                    console.log("获取搜索结果时发生错误 : xhr.status=" + xhr.status);

                }).complete(function (error) {
                    $.mobile.hidePageLoadingMsg();
                });
            }, function (error) {
                console.log("获取地理位置时发生错误 " + error);
            });

        } catch (err) {
            console.log("点击搜索按钮时发生错误 " + err);
        }
    });

}
```

```
//------------------------------------------------------------------
function bind() {
    initiateMap();
    initiateFavorites();
    initiateSearch();
    initiateFavButton();
}
//------------------------------------------------------------------
```

```
function onDeviceReady() {
    $(document).ready(function () {
        bind();
    });
}
document.addEventListener("deviceready", onDeviceReady);
//------------------------------------------------------------------
```

app.css 的完整源码如下

```
#map, .map-content, #map_canvas {
    width: 100%;
    height: 100%;
    padding: 0;
}
```

```
#map_canvas {
    height: min-height: 100%;
}
```

## jQueryMobile 的优点

jQueryMobile 是一个易于使用的 JavaScript UI 框架，面向移动应用开发者。jQueryMobile 最棒的部分是其声明式 UI 编程——许多控件都在 HTML 页面中声明为 div。此外，导航部分和历史记录管理部分都内置于 jQueryMobile 中。这免去了开发者自己实现历史记录管理部分的烦恼。

虽然 jQueryMobile 为控件和工具栏提供了良好的支持，但这些控件的编程要求开发者进行 DOM 操作。

jQueryMobile 最大的优势在于它建立在稳健的 jQuery 核心框架之上。另一个优势是 jQueryMobile 支持 iOS、Android、BlackBerry、HP WebOS、Nokia/Symbian、Windows Mobile、Opera Mobile/Mini、Firefox mobile 以及所有现代桌面浏览器。

jQueryMobile 为移动和平板应用程序提供了触摸事件支持。jQueryMobile 还提供了出色的主题支持。在主题之间切换就像更改 HTML 标签上的一个属性一样简单。

## jQueryMobile 的缺点

jQueryMobile 是一个很棒的轻量级框架，使用 jQuery 操作 DOM 允许用户以一种优雅而简单的方式构建应用程序。然而，随着应用程序复杂度的增加，以及对数据模型和相应视图需求的出现，在 jQueryMobile 中编程更多地是在 JavaScript 中实现自己的 MVC 框架。

简而言之，当你的应用程序比较复杂时，jQueryMobile 就难以使用了。由于缺乏 MVC 框架，甚至缺乏模型和 JavaScript 视图，与 Sencha Touch 等其他框架相比，在 jQueryMobile 中进行 JavaScript UI 编程会更加痛苦。

## 结论

如果移动应用程序相当简单，jQueryMobile 是一个很好的 JavaScript 移动 UI 开发框架。随着你的移动应用程序 UI 复杂度的增加，在 jQueryMobile 中编程将会变得更加繁琐。

## 第 5 章

## 结合 PhoneGap 使用 Sencha Touch

Sencha Touch 是来自一家最初名为 "ExtJS" 的公司的产品。"ExtJS" 是 Ajax RIA 领域中一家知名的公司，提供一个名为 "ExtJS" 的丰富而精良的 JavaScript UI 框架。该公司的知名产品包括 "ExtJS" JavaScript UI 框架、"Ext-GWT"（ExtJS 的 GWT 对应版本）、GWT UI 框架以及 "Sencha Touch"——一个面向移动端的 JavaScript 库。

"ExtJS" 公司最近更名为 "Sencha"。因此，虽然名字是新的，但 "Sencha Touch" 库中的内容是基于多年使用 JavaScript 构建 UI 的经验。

如果你熟悉 "ExtJS"，你会注意到 "ExtJS" 和 "Sencha Touch" 之间有许多相似之处，尤其是在基础类方面。然而，"Sencha Touch" 是专门为移动应用程序设计和开发的。

### 为什么使用 Sencha Touch？

Sencha Touch 允许你为 iPhone、Android 和 BlackBerry 开发基于浏览器的应用程序，并具有原生的外观和感觉。此外，Sencha Touch 基于 HTML5。

Sencha Touch 为你提供了以下优势：

-  为触摸优化的丰富控件集，以及支持点击、双击、滑动、长按、捏合和旋转、滑动手势的触摸事件。
-  新一代网络标准 HTML5 和 CSS3。
-  与 PhoneGap 集成。
-  支持 iOS、Android 和 BlackBerry，以及针对这些设备的原生主题。
-  开箱即用支持 Ajax、JSONP 和 Yahoo! Query Language (YQL)，并支持本地存储以支持控件。



简而言之，Sencha Touch 目前是移动应用开发领域最优秀的 JavaScript UI 库之一。如果你之前没有使用过 ExtJS，其学习曲线一开始可能会有些陡峭。

## Sencha Touch 的优点

Sencha Touch 的优点远大于缺点。首先，Sencha Touch 基于 Web 标准（如 HTML5 和 CSS3），而非任何专有技术。Sencha Touch 的社区支持也非常出色，且可免费用于商业用途。

你可以用 Sencha Touch 构建一个能够检测我们是在平板电脑还是手机上的应用程序，并可以编写代码使同一个应用在不同设备上呈现不同效果。例如，参考 kitchen sink 示例。当你在平板电脑和手机上查看它时，你会看到示例会自动调整自身以充分利用屏幕空间。

其组件集相当丰富。在 JavaScript 中构建整个组件确保了与用户的高度交互性，你拥有更多控制权。

Sencha Touch 的性能良好，并且在每个版本中都在持续改进。此外，随着 iOS 和 Android 操作系统新版本的发布，这些操作系统附带的 webkit 性能也在不断提升。

它支持国际化，并提供了如网格和轮播图等非常现代化的可视化辅助组件。

## Sencha Touch 的缺点

Sencha Touch 最大的缺点是其学习曲线。使用 Sencha Touch 时，你很少使用任何预先渲染的 HTML。所有内容都是通过 JavaScript 添加到 DOM 中的。这对某些人来说可能需要概念上的转变。

如果你的应用程序仅仅是包含几个带有导航的页面，且视图主要是列表视图、表单和工具栏，那么使用 Sencha Touch 可能就有些大材小用了。

## 下载 Sencha Touch

从 Sencha 官网下载 Sencha Touch 库 – www.sencha.com/products/touch/。下载并解压 SDK 后，你将看到如图 5–1 所示的目录结构。

![img/4a75e501abc949744a790d09257a5b1e_198_0.png]

## 将 Sencha 与 PhoneGap 集成

让我们开始将 Sencha Touch 与 PhoneGap 项目集成。本章假设我们针对 Android 平台。其他平台的步骤类似。

请参考第 2 章和第 3 章，为你目标平台设置 PhoneGap 项目。

如图 5–2 所示，你需要从 Sencha Touch SDK 中添加以下文件：

1.  将 sencha-touch.js JavaScript 文件添加到 www/lib 目录。
2.  将 resources/css 文件夹添加到 www/lib 目录。
3.  将所有应用代码放在一个名为 app/app.js 的文件中。这将是我们主要的 JavaScript 文件。

出于本章和示例的目的，请从 sencha-touch-1.1.0/examples/map 文件夹中复制 icon.png、phone_startup.png 和 tablet_startup.png 文件。

![img/4a75e501abc949744a790d09257a5b1e_199_0.png]

图 5–2. PhoneGap 和 Sencha Touch 项目结构

## 使用 Sencha Touch 构建本地搜索应用

本地搜索应用的需求与第 5 章中的类似。用户输入关键词进行搜索，指定从其当前位置开始搜索的范围，并在列表视图中获取本地场所列表。用户可以点击其中一个项目查看场所的详细信息。在详细信息页面，用户可以选择将该场所放入其收藏列表（存储在应用数据库中以供离线访问）。用户也可以在地图视图中查看搜索结果。

最后但同样重要的是，用户可以点击收藏按钮（星形图标）查看其收藏的列表。

让我们开始构建应用程序。请记住 Sencha Touch 相当庞大，本章将引导你了解构建此应用所需的 Sencha Touch API 子集。

## 初始化 Sencha Touch

第一步是确保 index.html 链接了 Sencha Touch 库、PhoneGap 库和 CSS。注意我们的 body 是空的。这是因为在 Sencha Touch 中，我们完全在 JavaScript 中构建 UI。注意我们包含了以下 JavaScript 和样式表。

1.  Sencha Touch 样式表
2.  Google Maps JavaScript
3.  我们的应用程序 JavaScript

```html
<!DOCTYPE HTML>
<html>
    <head>
        <title>Local Search</title>
        <link rel="stylesheet" type="text/css" href="lib/touch/resources/css/sencha-touch.css"></link>
        <!-- applications that determine the user's location via a sensor must
pass sensor=true when loading the Maps API JavaScript. -->
        <script type="text/javascript" src="http://maps.google.com/maps/api/js?sensor=true"></script>
        <script type="text/javascript" src="lib/touch/sencha-touch.js"></script>
        <script type="text/javascript" src="phonegap-1.1.0.js"></script>
        <script type="text/javascript" src="app/app.js"></script>
    </head>
    <body>
    </body>
</html>
```

现在让我们转向 app.js。PhoneGap 应用程序是在 `Ext.setup()` 函数中设置的。根据经验，请记住所有 Sencha Touch 函数都接受一个 JSON 结构作为配置。

我们将对 `Ext.setup` 做同样的事情。参见下面的代码。我们将为应用程序提供一些图标，以及手机和平板电脑的启动画面。但这些不是我们本章想要重点关注的部分。

这里最重要的部分是 `onReady` 函数。这类似于 jQuery 的 `document ready` 和 PhoneGap 的 `device ready` 函数。我们可以在这个函数中开始绘制 Sencha Touch 的 UI。

```javascript
Ext.setup({
    tabletStartupScreen: 'tablet_startup.png',
    phoneStartupScreen: 'phone_startup.png',
    icon: 'icon.png',
    glossOnIcon: false,
    onReady: function () {
        //Sencha Touch framework has initialized here.
        //Create Panels and bind event handlers.
    }
});
```

## 创建布局（应用骨架）

下一步是声明一个面板作为主面板。为此，我们将创建一个新面板 (`new Ext.Panel()`)，并在其配置 JSON 中声明以下内容：

1.  `layout: ‘card’` - 布局为卡片式布局，这意味着它是一叠卡片，一次只显示一张卡片
2.  `fullscreen: true` – 指定此面板将占据可用的 100% 宽度和高度，并自动绘制到页面上
3.  `items: [searchPanel, tabResultPanel, favourites, resultDetailPanel]` – 要添加到此面板的子组件数组。由于我们使用的是 ‘card’ 布局，它将一次显示一个子组件。我们的主面板中有四个子组件：searchPanel、tabResultPanel、favourites 和 resultDetailPanel。searchPanel 和 tabResultPanel 的声明方式与 mainPanel 相同。默认情况下，searchPanel 是可见的卡片，而其他面板隐藏在 searchPanel 后面
4.  `dockedItems: []` – 用于声明停靠的部件，通常用于工具栏按钮。
5.  在 `dockedItems` 内部，通过 JSON 表示声明了一个工具栏。这个工具栏包含两个按钮和一个用于分隔它们的间隔器。
    a. 对于主页按钮，我们使用 `iconCls:’home’`
    b. 对于收藏按钮，我们使用 `iconCls:’star’`

对于这两个按钮，我们都声明了一个处理程序，当按钮被点击时调用。

```javascript
//Main Panel with CardLayout
var mainPanel = new Ext.Panel({
    layout: 'card',
    fullscreen: true,
    items: [searchPanel, tabResultPanel, favorites, resultDetailPanel],
    dockedItems: [{
        xtype: 'toolbar',
        title: 'Local Search',
        dock: 'top',
        items: [{
            iconMask: true,
            ui: 'round',
            iconCls: 'home',
            handler: function () {

            }
        }, {
            xtype: 'spacer'
        }, {
            iconMask: true,
            ui: 'round',
            iconCls: 'star',
            handler: function () {}
        }]
    }]
});
```

在没有任何子部件的情况下，图 5–3 显示了此面板的外观。

![img/4a75e501abc949744a790d09257a5b1e_202_0.png]

接下来，我们声明搜索面板。搜索面板有一个文本框，用户可以在其中输入搜索关键词，还有一个范围选择器，允许用户选择搜索范围。最后，搜索面板有一个带搜索按钮的工具栏。其声明如下：

```javascript
var searchPanel = new Ext.form.FormPanel({
    layout: 'fit',
    fullscreen: true,
    scroll: 'vertical',
    standardSubmit: false,
    //Adding form field
    items: [{
```



## 第五章：在 Sencha Touch 中使用 PhoneGap

```
    xtype: 'fieldset',
    title: '本地搜索',
    items: [{
        xtype: 'textfield',
        name: 'search',
        label: '搜索',
        value: '披萨',
        userClearIcon: true,
        autoCapitalize: false
    }, {
        xtype: 'sliderfield',
        name: 'range',
        label: '范围 (0-10 公里)',
        value: 5,
        minValue: 0,
        maxValue: 10
    }]

}],
// 在底部停靠工具栏
dockedItems: [{
    xtype: 'toolbar',
    dock: 'bottom',
    items: [{
        xtype: 'spacer'
    }, {
        text: '搜索',
        iconCls: 'search',
        title: '搜索',
        iconMask: true,
        ui: 'confirm',
        handler: function () {

        }
    }]
}]
});
```

图 5–4 展示了搜索面板的显示效果。

![](img/4a75e501abc949744a790d09257a5b1e_204_0.png)

图 5–4. 应用程序搜索面板

当用户执行搜索时，会看到两个视图。

- 1. 显示搜索结果的列表视图
- 2. 显示搜索结果的地图视图

这两个视图都封装在一个选项卡面板中。我们如下声明选项卡面板：

```
var tabResultPanel = new Ext.TabPanel({
    layout: 'fit',
    tabBar: {
        dock: 'bottom',
        layout: {
            pack: 'center'
        }
    },
    items: [result, map],

});
```

图 5–5 显示了没有任何子面板的选项卡面板。注意，我们在配置 JSON 中定义了将选项卡栏定位在底部，用于“结果”和“地图”两个选项卡。默认情况下，“结果”选项卡将被选中。我们将在创建“结果”和“地图”对象时为两个选项卡定义标签和图标。

![](img/4a75e501abc949744a790d09257a5b1e_205_0.png)

图 5–5. 带选项卡的搜索结果面板

现在，我们将了解当用户执行搜索时如何显示搜索结果。本节中关于如何进行 AJAX 调用的内容将在本章后面部分介绍。

为便于本章讲解，假设您从 Google 地点服务器收到了如下所示的 JSON 数据：

```
{
  "status": "OK",
  "results": [{
    "name": "Zaaffran Restaurant - BBQ and GRILL, Darling Harbour",
    "vicinity": "Darling Drive, Darling Harbour, Sydney",
    "types": ["restaurant", "food", "establishment"],
    "geometry": {
      "location": {
        "lat": -33.8712950,
        "lng": 151.1984770
      }
    },
    "icon": "http://maps.gstatic.com/mapfiles/place_api/icons/restaurant-71.png",
    "reference": "CpQBwAAANM1CkdWcBxiExHin1oJpp7kX2D3nyb_DOqoQ_-RuBhq9cwJKYvU8-sRJUaXF4U2kET_OH3Oh3Yz4tf5_6gBgcsFAPyRappCrJ5WksvMkXrT5lA7q9U_SOZI0u3mrsvTtXnTDMKlBMywE_5Yy6lbshqPIatWZ6QkPZBNdmkifyN3vM7H2vL-300iY6EoartWuxIONckbMOBs4D946thThmK0sBoUCmGgFrtYgt00CIUc79fQi3wa00w",
    "id": "677679492a58049a7eae079e0890897eb953d79b"
  }, {
    "name": "Toros Restaurant Darling Harbour",
    "vicinity": "Murray Street, Sydney",
    "types": ["restaurant", "food", "establishment"],
    "geometry": {
      "location": {
        "lat": -33.8714080,
        "lng": 151.1975410
      }
    },
    "icon": "http://maps.gstatic.com/mapfiles/place_api/icons/restaurant-71.png",
    "reference": "CqQBeAAAALFuJbuIMXsGOluzs2SHeikzQNCsSbelIO-55zkhCiArbPkaCXRU-CcLZbeKsXaBpoBMH51yVjg6Nquct2LTE127X4CD1YtKpozmbjZpyCRFrJ_V5DIAIDGLCWeY_8NMxznbIq9bprR8mXJoAKv7jNz6KEMXaUGLRAXbi7G6CYEhBeK6Ur-x2AB1S3pKXskXKvGhRWFzL3Q5T0Oxe-gm_LJm9cgtzYjw",
    "id": "aefbc59325ffd5f3e93d67932375d20d143289de"
  }, {
    "name": "Strike Bowling Bar Darling Harbour",
    "vicinity": "Sydney",
    "types": ["restaurant", "food", "establishment"],
    "geometry": {
      "location": {
        "lat": -33.8662990,
        "lng": 151.2016580
      }
    },
    "icon": "http://maps.gstatic.com/mapfiles/place_api/icons/restaurant-71.png",
    "reference": "CqQBeAAAA0-prCRp9Atcj_rvavsLyv-DnxbGkw8OyRZb65m6OHOcwnw6lqFhIs2c7Ie6fMg3PZ4PhicfJl7ZWlaHaLDTqmRisoTOQUn61WTcSXAAiCOzcm0JDBnafqrskSpFtNUjzGA0x29WGnWSP44jmjtioIsJN9ik8yjK7uXP4buAmMPVEhBXPiCfHXk1CQ6XRuQhpztsGhQU4U6-tWjThCLSVzjbNxxiuihbA",
    "id": "0a4e24c365f4bd70080f99bb80153c5ba3faced8"
  }
  ...附加结果...
  ],
  "html attributions": ["Listings by \u003ca href=\"http://www.yellowpages.com.au/\"\u003eYellow Pages\u003c/a\u003e"]
}
```

既然我们已经看到了 Google 地点结果的 JSON 结构，我们将创建面板来显示结果。在这种情况下，我们扩展一个组件，并在组件中声明一个模板（tpl）。

模板化是 Sencha Touch 的一项特性，您可以在 `<tpl>` 标签中声明 html。在我们的例子中，我们传递上述 JSON 的 results 对象。results 对象实际上是一个数组。在我们的模板代码中，请注意 `<tpl for=".">`。这告诉 Sencha 模板引擎遍历 results 内的所有对象。

在 html 的后面部分，您会注意到像 {reference}、{icon}、{name} 这样的占位符。如果你们中有人使用过 java 的消息格式化，您会注意到这非常相似。这些 {} 条目将被 JSON 中的相应数据替换。

{name} 将被 results->entry->name 中的名称替换。

要将此面板填充数据，我们将调用以下 API：

```
// 这将调用模板引擎并绘制 AJAX 的响应
// 结果。这里 `result` 是用于显示结果的组件对象
// HTML，而 response.results 是 JSON 数组。
result.update(response.results);
```

现在，让我们看看用于创建结果面板的代码。

```
var result = new Ext.Component({

    title: '搜索结果',
    iconMask: true,
    iconCls: 'organize',
    cls: 'timeline',
    scroll: 'vertical',
    tpl: ['<tpl for=".">',
        '<div class="place" id="{reference}">',
        '<div class="icon"><img src="{icon}" /></div>',
        '<div>', '<h2>{name}</h2>',
        '<p>{vicinity}</p>',
        '</div>',
        '</div>',
        '</tpl>'],
    listeners: {
        el: {
            tap: detailClickHandler,
            // 处理点击事件
            // 的函数
        }
    }
});
```

注意末尾的 listeners 和 el 部分。这告诉 Sencha Touch 我们希望接收此组件元素上的事件。此外，我们还告诉它我们特别寻找点击事件。此代码的结果是，每当用户点击结果中列出的任何地点时，它将调用 detailClickHandler 函数。

![](img/4a75e501abc949744a790d09257a5b1e_208_0.png)

图 5–6. 搜索结果面板

Sencha Touch 的地图小部件使事情变得容易得多。否则，我们将不得不使用 Google 的地图 API。我们只需创建一个新的 Ext.Map 并为其提供一些选项。这是启动地图最简单的方式。注意，`map` 对象将在 AJAX 回调中用于向其添加地点标记。AJAX 调用在“获取地点列表”中描述。

```
var map = new Ext.Map({
    iconMask: true,
    iconCls: 'maps',
    title: '地图',
    // 此选项卡上显示的名称
    mapOptions: {
        // 用于渲染地图
        zoom: 12
    }
});
```

![](img/4a75e501abc949744a790d09257a5b1e_209_0.png)

图 5–7. 显示地点的地图面板

接下来是显示地点详情的面板。请注意，一旦用户点击搜索条目，应用程序将从 Google 地点服务器获取详细信息。此请求的 JSON 响应如下所示：

```
{
    "status": "OK",
    "result": {
        "name": "Google Sydney",
        "vicinity": "Pirrama Road, Pyrmont",
        "types": ["establishment"],
        "formatted phone number": "(02) 9374 4000",
        "formatted address": "5/48 Pirrama Road, Pyrmont NSW, Australia",
        "address_components": [{
            "long_name": "48",
            "short_name": "48",
            "types": ["street_number"]
        }, {
            "long_name": "Pirrama Road",
            "short_name": "Pirrama Road",
            "types": ["route"]
        }, {
            "long_name": "Pyrmont",
            "short_name": "Pyrmont",
            "types": ["locality", "political"]
        }, {
            "long_name": "NSW",
            "short_name": "NSW",
```

核心思路是以表格形式向用户展示上述信息。为此，我们将综合运用以下元素：

+   1. 一个用于将上述JSON数据作为表格部分展示的模板
+   2. 一个允许用户将此地点添加为收藏或移除收藏的按钮。

因此，我们使用了一个名为`resultDetailPanel`的包装面板。该面板采用`vbox`布局（垂直堆叠组件）。第一个子项是`placeDetailsPanel`（见下文），第二个是按钮。

按钮的文本会根据用户是否已将该地点设为收藏，在“添加到收藏”和“从收藏中移除”之间切换。应用程序中为此定义了一个名为`isFav()`的函数。

```javascript
var resultDetailPanel = new Ext.Panel({
    layout: {
        type: 'vbox',
    },
    items: [
    placeDetailsPanel,
    {
        xtype: 'button',
        text: 'Add to Favorite',
        handler: function (button, event) {
            if (button.text == "Add to Favorite") {
                addCurrentToFav();
                button.setText("Remove from Favorite");
            } else {
                removeCurrentFromFav();
                button.setText("Add to Favorite");
            }
        }
    }],
    dockedItems: [{
        xtype: 'toolbar',
        dock: 'bottom',
        items: [{
            ui: 'round',
            text: 'Back',
            handler: function () {}
        }]
    }]
});
```

这个面板将JSON结果展示为表格。它为此使用了一个模板。模板是一个HTML模板，其中包含由`{<<variable>>}`表示的占位符。模板代码被使用，占位符由实际值替换：

```javascript
var placeDetailsPanel = new Ext.Panel({
    tpl: ['<table>',
        '<tr>',
        '<td>',
        '</td>',
        '<td>',
        '<h1 class="bold">Business Details</h1>',
        '</td>',
        '</tr>',
        '<tr>',
        '<td>',
        '<h1 class="bold">Name</h1>',
        '</td>',
        '<td>',
        '<h1>{name}</h1>',
        '</td>',
        '</tr>',
        '<tr>',
        '<td>',
        '<h1 class="bold">Address</h1>',
        '</td>',
        '<td>',
        '<h1>{formatted_address}</h1>',
        '</td>',
        '</tr>',
        '<tr>',
        '<td>',
        '<h1 class="bold">Phone</h1>',
        '</td>',
        '<td>',
        '<h1>{formatted_phone_number}</h1>',
        '</td>',
        '</tr>',
        '<tr>',
        '<td>',
        '<h1 class="bold">Rating</h1>',
        '</td>',
        '<td>',
        '<h1>{rating}</h1>',
        '</td>',
        '</tr>',
        '<tr>',
        '<td>',
        '<h1 class="bold">Home Page</h1>',
        '</td>',
        '<td>',
        '<a href="{url}" target="_blank">Home Page</a>',
        '</td>',
        '</tr>',
        '</table>'
    ]

});
```

地点详情面板如图5-8所示。

![图5–8. 地点详情面板](img/4a75e501abc949744a790d09257a5b1e_212_0.png)

**图5–8. 地点详情面板**

## 第5章：在Sencha Touch中使用PhoneGap

现在我们已经了解了如何添加或移除收藏地点，接下来让我们看看列出用户收藏地点的面板。是的，这个面板与结果面板非常相似。唯一的区别是，结果面板接收来自Google Places服务器的JSON数据，而收藏面板接收来自数据库的JSON数据。

```javascript
var favorites = new Ext.Component({
    title: 'Favotites',
    iconMask: true,
    iconCls: 'organize',

    cls: 'timeline',
    scroll: 'vertical',
    tpl: ['<tpl for=".">',
        '<div class="place" id="{reference}">',
        '<div class="icon"><imgsrc="{icon}" /></div>',
        '<div>',
        '<h2>{name}</h2>',
        '<p>{vicinity}</p>',
        '</div>',
        '</div>',
        '</tpl>'],
    listeners: {
        el: {
            tap: detailClickHandler,
        }
    }
});
```

![图5–9. *收藏地点面板*](img/4a75e501abc949744a790d09257a5b1e_214_0.png)

**图5–9. 收藏地点面板**

## 在面板间切换

随着你深入探索应用程序代码，你将需要从一个面板切换到另一个面板。这就是我们为主面板使用‘card’布局的主要原因。

为了在卡片布局的面板间切换，我们将使用以下代码。注意，第一个参数是传递给`mainPanel`的`items`中组件的索引号。第二个参数是动画效果。

```javascript
mainPanel.setActiveItem(0, "slide");
mainPanel.setActiveItem(1, {type: 'slide', direction: 'right'});
```

此外，主面板拥有工具栏。我们需要更改此工具栏的标题，以告知用户当前所在位置。这可以通过以下代码实现：

```javascript
mainPanel.dockedItems.items[0].setTitle('Details');
```

## 获取地点列表

当用户点击搜索面板上的搜索按钮时，我们需要发起一个Ajax调用来获取Google Places的结果。以下函数展示了如何在Sencha Touch和PhoneGap中完成此操作。

步骤相当简单。

1.  从PhoneGap获取地理位置信息

2.  在`getCurrentPosition`的成功回调中，通过调用`Ext.ajax.request(url, successCallback, failureCallback)`发起一个Ajax调用

3.  在`Ext.ajax.request`的`successCallback`中，你将获得JSON字符串。

    a.  将此JSON字符串转换为JSON对象

    b.  通过调用`result.update(obj.results);`填充结果面板

    c.  在Google Maps上填充标记

```javascript
var fetchFromGoogle = function () {
    var keyword = searchPanel.items.items[0].items.items[0].value;
    var range = searchPanel.items.items[0].items.items[1].value * 1000;
    navigator.geolocation.getCurrentPosition(
        function (position) {
            var lat = position.coords.latitude;
            var lng = position.coords.longitude;

            map.update({
                latitude: lat,
                longitude: lng
            });

            var googlePlaceUrl =
                'https://maps.googleapis.com/maps/api/place/search/json?location='
                + lat + ',' + lng + '&radius=' + range + '&types=food&name=' + keyword
                + '&sensor=true&key=API_Key';
            //注意，你需要将API_Key替换为你自己的密钥。你可以从
            //http://code.google.com/apis/maps/documentation/places/ 获取API Key。
            Ext.Ajax.request({
                url: googlePlaceUrl,
                success: function (response, opts) {

                    var obj = Ext.decode(response.responseText);

                    result.update(obj.results);
                    var data = obj.results;
                    for (var i = 0, ln = data.length; i < ln; i++) { // 循环以向地图添加点
                        var place = data[i];

                        if (place.geometry && place.geometry.location) {
                            var position = new
                                google.maps.LatLng(place.geometry.location.lat, place.geometry.location.lng);
                            addMarker(place.name, place.reference, position); // 使用新数据调用addMarker函数
                        }
                    }
                },
                failure: function (response, opts) {
                    console.log('server-side failure with status code ' + response.status);
                }
            });
        },
        function (err) {
            console.log('Failed to get geo location from phonegap ' + err);
        }
    );
}
```

## 获取地点详情

从Google Places服务器获取地点详情甚至更容易。你需要的东西更少。

1.  通过调用`Ext.ajax.request(url, successCallback, failureCallback)`发起一个Ajax调用

2.  在`Ext.ajax.request`的`successCallback`中，你将获得JSON字符串。

    a.  将此JSON字符串转换为JSON对象

    b.  通过调用`placeDetailsPanel.update(obj.result);`填充地点详情面板

    c.  我们还将通过调用`isFav()`函数检查此地点是否为收藏

        i.  如果该地点是收藏，我们将按钮重命名为“从收藏中移除”

        ii. 否则，我们将按钮重命名为“添加到收藏”

```javascript
var cachedDetails = null;

/**
* 确保在使用表格之前它已存在
* @param {Object} tx
*/
var ensureTableExists = function (tx) {
    tx.executeSql('CREATE TABLE IF NOT EXISTS Favourite (id unique, reference, name, address, phone, rating, icon, vicinity)');
}

/**
* 将当前详情添加到数据库
*/
var addCurrentToFav = function () {
    addToFavorite(cachedDetails);
}

/**
```



# 从数据库存储和检索收藏

此应用程序的最后一个重要部分是定义函数来完成以下操作：

+   1. 将地点添加到收藏表
2. 从收藏表中移除地点
3. 检查地点是否已在收藏表中
4. 从收藏表中获取所有条目。

为了在不同函数调用间传递地点条目，我们在本应用程序中声明了一个名为 `cachedDetails` 的变量。当我们在显示地点详情的页面时，我们将当前地点缓存在 `cachedDetails` 中。`cachedDetails` 用于将地点添加到收藏、从收藏中移除，以及检查它是否已属于用户的收藏。

```javascript
var cachedDetails = null;

/**
 * 在使用表之前确保它存在
 * @param {Object} tx
 */
var ensureTableExists = function (tx) {
    tx.executeSql('CREATE TABLE IF NOT EXISTS Favourite (id unique, reference,
                            name,address,phone,rating,icon,vicinity)');
}

/**
 * 将 currentDetails 添加到数据库
 */
var addCurrentToFav = function () {
    addToFavorite(cachedDetails);
}

/**
 * 从数据库中移除 currentDetails
 */
var removeCurrentFromFav = function () {
    removeFromFavorite(cachedDetails);
}

/**
 * 将当前商业数据添加到收藏
 * @param {Object} data
 */
var addToFavorite = function (data) {
    var db = window.openDatabase("Favourites", "1.0", "Favourites", 20000000);

    db.transaction(function (tx) {

        ensureTableExists(tx);

        var id = (data.id != null) ? ('"' + data.id + '"') : ('""');
        var reference = (data.reference != null) ? ('"' + data.reference + '"') : ('""');
        var name = (data.name != null) ? ('"' + data.name + '"') : ('""');
        var address = (data.formatted_address != null) ? ('"' + data.formatted_address + '"') : ('""');
        var phone = (data.formatted_phone_number != null) ? ('"' + data.formatted_phone_number + '"') : ('""');
        var rating = (data.rating != null) ? ('"' + data.rating + '"') : ('""');
        var icon = (data.icon != null) ? ('"' + data.icon + '"') : ('""');
        var vicinity = (data.vicinity != null) ? ('"' + data.vicinity + '"') : ('""');

        var insertStmt = 'INSERT INTO Favourite (id,reference,
                    name,address,phone,rating,icon,vicinity) VALUES
                    (' + id + ',' + reference + ',' + name + ',' + address + ',' +
                    phone + ',' + rating + ',' + icon + ',' + vicinity + ')';

        tx.executeSql(insertStmt);

    }, function (error) {
        console.log("Data insert failed " + error.code + " " + error.message);
    }, function () {
        console.log("Data insert successful");
    });
}

/**
 * 从收藏中移除当前商业数据
 * @param {Object} data
 */
var removeFromFavorite = function (data) {
    try {
        var db = window.openDatabase("Favourites", "1.0", "Favourites", 20000000);

        db.transaction(function (tx) {
            ensureTableExists(tx);
            var deleteStmt = "DELETE FROM Favourite WHERE id = '" + data.id + "'";
            console.log(deleteStmt);
            tx.executeSql(deleteStmt);

        }, function (error) {
            console.log("Data Delete failed " + error.code + " " + error.message);
        }, function () {
            console.log("Data Delete successful");
        });

    } catch (err) {
        console.log("Caught exception while deleting favourite " + data.name);
    }
}

/**
 *
 * @param {Object} reference
 * @return 如果地点是收藏则返回 true，否则返回 false
 */
var isFav = function (data, callback) {

    var db = window.openDatabase("Favourites", "1.0", "Favourites", 200000);

    try {
        db.transaction(function (tx) {
            ensureTableExists(tx);

            var sql = "SELECT * FROM Favourite where id='" + data.id + "'";

            tx.executeSql(sql, [], function (tx, results) {
                var result = (results != null && results != null &&
                results.rows.length > 0);
                callback(result);
            }, function (tx, error) {
                console.log("Got error in isFav error.code =" + error.code + " error.message = " + error.message);
                callback(false);
            });

        }, function (error) {
            console.log("Got error in isFav error.code =" + error.code + " error.message = " + error.message);
            callback(false);
        });

    } catch (err) {
        console.log("Got error in isFav " + err);
        callback(false);
    }
}
```

# 第五章：将 PhoneGap 与 Sencha Touch 配合使用



## 第五章：结合Sencha Touch使用PhoneGap

本章涵盖应用程序的布局部分，如何从Google Places服务器填充数据，以及如何进行导航和使用数据库。

请参考下面列出的完整示例，以了解事件的处理方式。

### 1. index.html

```html
<!DOCTYPE HTML>
<html>
    <head>
        <title>Sencha Touch Layout</title>
        <link rel="stylesheet" type="text/css" href="lib/touch/resources/css/sencha-touch.css"></link>
        <script type="text/javascript" src="http://maps.google.com/maps/api/js?sensor=true"></script>
        <script type="text/javascript" src="lib/touch/sencha-touch.js"></script>
        <script type="text/javascript" src="app/app.js"></script>
        <style>
            .x-tabbar{
                padding-top: 10px;!important;
                border-bottom: 2px solid #306aa1 !important;
            }
            .place {
                padding: 10px 0 10px 68px;
                border-top: 1px solid #ccc;
                min-height: 68px;
                background-color: #fff;
            }
            .place h2 {
                font-weight:bold;
            }
            .place .icon {
                position: absolute;
                left: 10px;
            }
            .place .icon img{
                height:24px;
                width: 24px;
            }
            .bold{
                font-weight: bold;
            }
        </style>
    </head>
    <body>
    </body>
</html>
```

### 2. app.js

```javascript
Ext.setup({
    tabletStartupScreen: 'tablet_startup.png',
    phoneStartupScreen: 'phone_startup.png',
    icon: 'icon.png',
    glossOnIcon: false,
    onReady: function () {
        var lastPanelId = 0;

        var SEARCHPAGE = 0;
        var TABPAGE = 1;
        var FAVPAGE = 2;
        var DETAILSPAGE = 3;

        var cachedDetails = null;

        var searchPanel = new Ext.form.FormPanel({
            layout: 'fit',
            fullscreen: true,
            scroll: 'vertical',
            standardSubmit: false,
            //添加表单字段
            items: [{
                xtype: 'fieldset',
                title: '本地搜索',
                items: [{
                    xtype: 'textfield',
                    name: 'search',
                    label: '搜索',
                    value: 'Pizza',
                    useClearIcon: true,
                    autoCapitalize: false
                }, {
                    xtype: 'sliderfield',
                    name: 'range',
                    label: '范围 (0-10 Kms)',
                    value: 5,
                    minValue: 0,
                    maxValue: 10
                }]
            }], //在底部停靠工具栏
            dockedItems: [{
                xtype: 'toolbar',
                dock: 'bottom',
                items: [{
                    xtype: 'spacer'
                }, {
                    text: '搜索',
                    iconCls: 'search',
                    title: '搜索',
                    iconMask: true,
                    ui: 'round',
                    ui: 'confirm',
                    handler: function () {
                        lastPanelId = TABPAGE;
                        fetchFromGoogle();

                        mainPanel.dockedItems.items[0].setTitle('搜索结果');
                        mainPanel.setActiveItem(lastPanelId);
                    }
                }]
            }]
        });

        var detailClickHandler = function (event) {
            var reference = event.getTarget(".place").id;
            fetchDetails(reference);
            mainPanel.dockedItems.items[0].setTitle('详情');
            mainPanel.setActiveItem(DETAILSPAGE, "slide");
        }

        var result = new Ext.Component({
            title: '搜索结果',
            iconMask: true,
            iconCls: 'organize',
            cls: 'timeline',
            scroll: 'vertical',
            tpl: ['<tpl for=".">',
                '<div class="place" id="{reference}">',
                '<div class="icon"><img src="{icon}" /></div>',
                '<div>',
                '<h2>{name}</h2>',
                '<p>{vicinity}</p>',
                '</div>',
                '</div>',
                '</tpl>'
            ],
            listeners: {
                el: {
                    tap: detailClickHandler,
                    delegate: '.place'
                }
            }
        });

        var favorites = new Ext.Component({
            title: '收藏夹',
            iconMask: true,
            iconCls: 'organize',
            cls: 'timeline',
            scroll: 'vertical',
            tpl: ['<tpl for=".">',
                '<div class="place" id="{reference}">',
                '<div class="icon"><img src="{icon}" /></div>',
                '<div>',
                '<h2>{name}</h2>',
                '<p>{vicinity}</p>',
                '</div>',
                '</div>',
                '</tpl>'],
            listeners: {
                el: {
                    tap: detailClickHandler,
                    delegate: '.place'
                }
            }
        });

        var map = new Ext.Map({
            iconMask: true,
            iconCls: 'maps',
            title: '地图',
            // 此选项卡上显示的名称
            fullscreen: true,
            mapOptions: { // 用于渲染地图
                zoom: 12
            }
        });

        var tabResultPanel = new Ext.TabPanel({
            layout: 'fit',
            tabBar: {
                dock: 'bottom',
                layout: {
                    pack: 'center'
                }
            },
            items: [result, map],
        });

        var placeDetailsPanel = new Ext.Panel({
            tpl: ['<table>',
                '<tr>',
                '<td>',
                '</td>',
                '<td>',
                '<h1 class="bold">商户详情</h1>',
                '</td>',
                '</tr>',
                '<tr>',
                '<td>',
                '<h1 class="bold">名称</h1>',
                '</td>',
                '<td>',
                '<h1>{name}</h1>',
                '</td>',
                '</tr>',
                '<tr>',
                '<td>',
                '<h1 class="bold">地址</h1>',
                '</td>',
                '<td>',
                '<h1>{formatted_address}</h1>',
                '</td>',
                '</tr>',
                '<tr>',
                '<td>',
                '<h1 class="bold">电话</h1>',
                '</td>',
                '<td>',
                '<h1>{formatted_phone_number}</h1>',
                '</td>',
                '</tr>',
                '<tr>',
                '<td>',
                '<h1 class="bold">评分</h1>',
                '</td>',
                '<td>',
                '<h1>{rating}</h1>',
                '</td>',
                '</tr>',
                '<tr>',
                '<td>',
                '<h1 class="bold">主页</h1>',
                '</td>',
                '<td>',
                '<a href="{url}" target="_blank">主页</a>',
                '</td>',
                '</tr>',
                '</table>'
            ]
        });

        var resultDetailPanel = new Ext.Panel({
            layout: {
                type: 'vbox',
            },
            items: [
                placeDetailsPanel,
                {
                    xtype: 'button',
                    text: '添加到收藏夹',
                    handler: function (button, event) {
                        if (button.text == "添加到收藏夹") {
                            addCurrentToFav();
                            button.setText("从收藏夹移除");
                        } else {
                            removeCurrentFromFav();
                            button.setText("添加到收藏夹");
                        }
                    }
                }
            ],
            dockedItems: [{
                xtype: 'toolbar',
                dock: 'bottom',
                items: [{
                    ui: 'round',
                    text: '返回',
                    handler: function () {
                        if (lastPanelId == 0) {
                            mainPanel.dockedItems.items[0].setTitle('主页');
                        } else if (lastPanelId == 1) {
                            mainPanel.dockedItems.items[0].setTitle('搜索结果');
                        } else if (lastPanelId == 2) {
                            fetchFromDB();
                            mainPanel.dockedItems.items[0].setTitle('收藏夹');
                        } else if (lastPanelId == 3) {
                            //不应发生这种情况
                            mainPanel.dockedItems.items[0].setTitle('详情');
                        }

                        mainPanel.setActiveItem(lastPanelId, {
                            type: 'slide',
                            direction: 'right'
                        });
                    }
                }]
            }]
        });

        //使用CardLayout的主面板
        var mainPanel = new Ext.Panel({
            layout: 'card',
            fullscreen: true,
            items: [searchPanel, tabResultPanel, favorites, resultDetailPanel],
            dockedItems: [{
                xtype: 'toolbar',
                title: '本地搜索',
                dock: 'top',
                items: [{
                    iconMask: true,
                    ui: 'round',
                    iconCls: 'home',
                    handler: function () {
                        lastPanelId = SEARCHPAGE;

                        mainPanel.dockedItems.items[0].setTitle('主页');
                        mainPanel.setActiveItem(lastPanelId, "slide");
                    }
                }, {
                    xtype: 'spacer'
                }, {
                    iconMask: true,
                    ui: 'round',
                    iconCls: 'star',
                    handler: function () {
                        fetchFromDB();
                        lastPanelId = FAVPAGE;
                        mainPanel.dockedItems.items[0].setTitle('收藏夹');
                        mainPanel.setActiveItem(lastPanelId, "slide");
                    }
                }]
            }]
        });

        // 这些都是Google Maps API
        var addMarker = function (name, reference, position) {
            var marker = new google.maps.Marker({
                map: map.map,
                position: position,
                clickable: true,
                optimized: true,
                title: name
            });
            google.maps.event.addListener(marker, 'click', function () {
                fetchDetails(reference);

                mainPanel.dockedItems.items[0].setTitle('详情');
                mainPanel.setActiveItem(DETAILSPAGE, "slide");
            });
        };

        var fetchFromGoogle = function () {
            var keyword = searchPanel.items.items[0].items.items[0].value;
            var range = searchPanel.items.items[0].items.items[1].value * 1000;
            navigator.geolocation.getCurrentPosition(
                function (position) {
                    var lat = position.coords.latitude;
                    var lng = position.coords.longitude;
```

```javascript
tx.executeSql(sql, [],
    function (tx, results) {
        var result = (results != null && results.rows != null &&
            results.rows.length > 0);
        callback(result);
    },
    function (tx, error) {
        console.log("在isFav中出错，error.code = " + error.code + "
                error.message = " + error.message);
        callback(false);
    }
);
});

} catch (err) {
    console.log("在isFav中出错 " + err);
    callback(false);
}
}
```



## 第五章：在Sencha Touch中使用PhoneGap

map.update({
    latitude: lat,
    longitude: lng
});

var googlePlaceUrl =
'https://maps.googleapis.com/maps/api/place/search/json?location='
    + lat + ',' + lng + '&radius=' + range + '&types=food&name='
    + keyword + '&sensor=true&key=API_Key';
//注意：你需要将API_Key替换为你自己的密钥。
//你可以从以下地址获取API密钥：
//http://code.google.com/apis/maps/documentation/places/

Ext.Ajax.request({
    url: googlePlaceUrl,
    success: function (response, opts) {
        var obj = Ext.decode(response.responseText);
        result.update(obj.results);
        var data = obj.results;
        for (var i = 0, ln = data.length; i < ln; i++) { // 循环将点添加到地图
            var place = data[i];
            if (place.geometry && place.geometry.location) {
                var position = new google.maps.LatLng(place.geometry.location.lat, place.geometry.location.lng);
                addMarker(place.name, place.reference, position); // 使用新数据调用addMarker函数
            }
        }
    },
    failure: function (response, opts) {
        console.log('服务器端失败，状态码为：' + response.status);
    }
}, function (err) {
    console.log('从phonegap获取地理位置失败：' + err);
});

var fetchFromDB = function () {
    var db = window.openDatabase("Favourites", "1.0", "Favourites", 200000);
    try {
        db.transaction(function (tx) {
            tx.executeSql('SELECT * FROM Favourite', [], function (tx, results) {
                var arr = [];
                for (var i = 0; i < results.rows.length; i++) {
                    var data = results.rows.item(i);
                    arr[i] = data;
                }
                favorites.update(arr);
            }, function (error) {
                console.log("获取收藏夹时出错 " + error.code + " " + error.message);
            });
        });
    } catch (err) {
        console.log("读取收藏夹时出错 " + err);
    }
}

var fetchDetails = function (reference) {
    placeDetailsPanel.update({
        name: "",
        formatted_address: "",
        formatted_phone_number: "",
        rating: "",
        url: ""
    });
    Ext.Ajax.request({
        url:
            'https://maps.googleapis.com/maps/api/place/details/json?reference=' + reference +
            '&sensor=true&key=API_Key',
        success: function (response, opts) {
            var obj = Ext.decode(response.responseText);
            cachedDetails = obj.result;
            isFav(obj.result, function (result) {
                if (result) {
                    resultDetailPanel.items.items[1].setText("从收藏夹移除");
                } else {
                    resultDetailPanel.items.items[1].setText("添加到收藏夹");
                }
                placeDetailsPanel.update(obj.result);
            });
        },
        failure: function (response, opts) {
            console.log('服务器端失败，状态码为：' + response.status);
        }
    });
}

/**
 * 确保我们在使用前拥有该表
 * @param {Object} tx
 */
var ensureTableExists = function (tx) {
    tx.executeSql('CREATE TABLE IF NOT EXISTS Favourite (id unique, reference, name,address,phone,rating,icon,vicinity)');
}

var addCurrentToFav = function () {
    addToFavorite(cachedDetails);
}

var removeCurrentFromFav = function () {
    removeFromFavorite(cachedDetails);
}

/**
 * 将当前商家数据添加到收藏夹
 * @param {Object} data
 */
var addToFavorite = function (data) {
    var db = window.openDatabase("Favourites", "1.0", "Favourites", 20000000);
    db.transaction(function (tx) {
        ensureTableExists(tx);
        var id = (data.id != null) ? ('"' + data.id + '"') : ('""');
        var reference = (data.reference != null) ? ('"' + data.reference + '"') : ('""');
        var name = (data.name != null) ? ('"' + data.name + '"') : ('""');
        var address = (data.formatted_address != null) ? ('"' + data.formatted_address + '"') : ('""');
        var phone = (data.formatted_phone_number != null) ? ('"' + data.formatted_phone_number + '"') : ('""');
        var rating = (data.rating != null) ? ('"' + data.rating + '"') : ('""');
        var icon = (data.icon != null) ? ('"' + data.icon + '"') : ('""');
        var vicinity = (data.vicinity != null) ? ('"' + data.vicinity + '"') : ('""');
        var insertStmt = 'INSERT INTO Favourite (id,reference, name,address,phone,rating,icon,vicinity) VALUES (' + id + ',' + reference + ',' + name + ',' + address + ',' + phone + ',' + rating + ',' + icon + ',' + vicinity + ')';
        tx.executeSql(insertStmt);
    }, function (error) {
        console.log("数据插入失败 " + error.code + " " + error.message);
    }, function () {
        console.log("数据插入成功");
    });
}

/**
 * 从收藏夹中移除当前商家数据
 * @param {Object} data
 */
var removeFromFavorite = function (data) {
    try {
        var db = window.openDatabase("Favourites", "1.0", "Favourites", 20000000);
        db.transaction(function (tx) {
            ensureTableExists(tx);
            var deleteStmt = "DELETE FROM Favourite WHERE id = '" + data.id + "'";
            console.log(deleteStmt);
            tx.executeSql(deleteStmt);
        }, function (error) {
            console.log("数据删除失败 " + error.code + " " + error.message);
        }, function () {
            console.log("数据删除成功");
        });
    } catch (err) {
        console.log("删除收藏项 " + data.name + " 时捕获到异常");
    }
}

/**
 *
 * @param {Object} data
 * @return 如果该地点是收藏项则返回true，否则返回false
 */
var isFav = function (data, callback) {
    var db = window.openDatabase("Favourites", "1.0", "Favourites", 200000);
    try {
        db.transaction(function (tx) {
            ensureTableExists(tx);
            var sql = "SELECT * FROM Favourite where id='" + data.id + "'";
            tx.executeSql(sql, [], function (tx, results) {
                var result = (results != null && results.rows != null && results.rows.length > 0);
                callback(result);
            }, function (tx, error) {
                console.log("在isFav中出错 " + error.code + " error.message = " + error.message);
                callback(false);
            });
        });
    } catch (err) {
        console.log("检查收藏项 " + data.name + " 时捕获到异常");
        callback(false);
    }
}

## 结论

如果你正在构建一个相当复杂的移动应用，你应该使用Sencha Touch。jQueryMobile适用于更小、更简单的Ajax应用。虽然jQueryMobile也可用于更复杂的应用，但你将不得不自行处理DOM操作，情况会变得更为复杂。

Sencha Touch性能良好，组件丰富。它的一些组件使用数据存储与服务器组件通信。你可以在Sencha Touch中使用MVC设计模式，甚至可以将你的应用拆分成多个.js文件，以实现更模块化的代码。

# 在GWT中使用PhoneGap

Google Web Toolkit (GWT) 是Google提供的一个框架，你可以用它来开发基于浏览器的应用程序。GWT允许开发者用Java编写代码并生成基于JavaScript的应用程序。

GWT应用天生具有跨浏览器兼容性，它们是体积最小、速度最快的基于浏览器的应用程序。

本章将重点介绍如何使用PhoneGap为移动电话开发GWT应用。这些步骤基于Daniel Kurka开发的GWT PhoneGap库。你可以从 http://code.google.com/p/gwt-phonegap/ 下载这个库。

了解如何开发基于GWT的应用是必不可少的。如果你是GWT应用开发的新手，可以访问 http://code.google.com/webtoolkit/doc/latest/tutorial/index.html 以了解更多关于GWT的信息。

## 为什么使用GWT进行用户界面开发？

在我们深入探讨如何结合使用GWT和PhoneGap之前，让我们先考虑一下为什么GWT是用户界面开发的一个绝佳选择：

- GWT允许开发者编写基于浏览器的应用，而无需担心跨浏览器问题、JavaScript内存泄漏以及JavaScript语言本身的问题。
- GWT允许开发者使用Java编码，并将用Java编写的用户界面和业务逻辑编译成JavaScript。
- GWT还允许你使用诸如*延迟绑定*（它类似于JavaScript世界的运行时多态）这样的概念。这种方法允许开发者创建一个单一的应用，可以使用不同的类为移动浏览器提供服务，使用另一组类为桌面浏览器提供服务。
- GWT确保你能创建出体积最小、速度最快的JavaScript。



GWT是一项广受认可的技术，被众多公司和大量的开发者群体所采用。GWT正日益成为构建大型、复杂Ajax应用程序的事实标准选择。

除了上述优势，GWT还开箱即提供许多轻量级的现成组件。此外，还有像EXT-GWT和Smart-GWT这样的专业GWT库，它们能使用户界面看起来非常专业且完善。试想一下，你的Java开发者运用他们现有的Java技能，轻松地编写基于浏览器的应用程序，并遵循最佳的设计实践。GWT消除了编写基于浏览器应用程序的痛苦，同时提供最佳的浏览器应用程序体验。

## 了解GWT PhoneGap

GWT提供了一种名为JavaScript原生接口的机制，它允许GWT对现有的JavaScript库进行封装。这项能力使得开发者能够用Java进行编码，而无需担心底层的JavaScript函数是如何被调用的。

GWT PhoneGap是PhoneGap库的一个GWT封装。下一节将演示如何使用GWT PhoneGap编写一个helloworld应用。

## 构建PhoneGap GWT应用

构建GWT PhoneGap应用主要分为两个步骤。第一步是构建一个GWT项目。构建好GWT项目后，开发者将编译该项目以创建一个Web应用（一组HTML和JavaScript文件）。

第二步是构建一个Android PhoneGap应用（使用0.9.4版本的PhoneGap），并将GWT Web应用嵌入到PhoneGap应用中。

## 构建GWT应用

在构建GWT应用之前，你需要以下工具：

- JDK 1.6+
- Eclipse 3.6 Helios
- Eclipse Google插件
- PhoneGap 0.9.4库
- GWT PhoneGap 0.8版本库
- Chrome浏览器12+版本（用于测试）

创建一个新的Web应用项目（Google Web应用），并在向导中填写如图6–1所示的值。你需要勾选“Use Google Web Toolkit”，并取消勾选“Use Google App Engine”。

![](img/4a75e501abc949744a790d09257a5b1e_236_0.png)

**图6–1.** 创建GWT项目

为项目创建一个名为“lib”的文件夹。从 http://code.google.com/p/gwt-phonegap/downloads/detail?name=gwt-phonegap-0.8.jar 下载GWT-PhoneGap库，并将其复制到你应用的lib文件夹中。右键单击gwt-phonegap-0.8.jar，然后点击“build path” -> “Add to build path”，将其添加到类路径中。

现在打开PhoneGap_GWT_Helloworld.gwt.xml文件。在该文件中，添加以下条目：

```
<inherits name='de.kurka.phonegap.PhoneGap' />
<set-property name="user.agent" value="safari" />
```

请注意，通过将user.agent的set-property设置为safari，GWT将仅为基于webkit的浏览器生成JavaScript。在此场景中，将专门使用Chrome浏览器进行测试。

你的PhoneGap_GWT_Helloworld.gwt.xml文件现在应如下所示：

```
<?xml version="1.0" encoding="UTF-8"?>
<module rename-to='phonegap_gwt_helloworld'>
  <!-- Inherit the core Web Toolkit stuff.                    -->
  <inherits name='com.google.gwt.user.User'/>
  <!-- Inherit the default GWT style sheet.  You can change   -->
  <!-- the theme of your GWT application by uncommenting    -->
  <!-- any one of the following lines.                        -->
  <inherits name='com.google.gwt.user.theme.clean.Clean'/>
  <!-- <inherits name='com.google.gwt.user.theme.standard.Standard'/> -->
  <!-- <inherits name='com.google.gwt.user.theme.chrome.Chrome'/> -->
  <!-- <inherits name='com.google.gwt.user.theme.dark.Dark'/>     -->

  <!-- Other module inherits                                   -->
  <inherits name='de.kurka.phonegap.PhoneGap' />
  <set-property name="user.agent" value="safari" />

  <!-- Specify the app entry point class.                      -->
  <entry-point
class='com.phonegap.example.gwt.helloworld.client.PhoneGap_GWT_Helloworld'/>
  <!-- Specify the paths for translatable code                 -->
  <source path='client'/>
  <source path='shared'/>

</module>
```

现在打开位于项目war文件夹中的PhoneGap_GWT_Helloworld.html，并进行以下更改：

```
<!doctype html>
<!-- The DOCTYPE declaration above will set the            -->
<!-- browser's rendering engine into                       -->
<!-- "Standards Mode". Replacing this declaration        -->
<!-- with a "Quirks Mode" doctype may lead to some        -->
<!-- differences in layout.                                -->

<html>
  <head>
    <meta http-equiv="content-type" content="text/html; charset=UTF-8">

    <!--                                                     -->
    <!-- Consider inlining CSS to reduce the number of requested files -->
    <!--                                                     -->
    <link type="text/css" rel="stylesheet" href="PhoneGap_GWT_Helloworld.css">

<!--                              -->
<!-- Any title is fine              -->
<!--                                -->
<title>Gwt PhoneGap Demo</title>

<!--                                -->
<!-- This script loads your compiled module. -->
<!-- If you add any GWT meta tags, they must -->
<!-- be added before this line.      -->
<!--                                -->
<script type="text/javascript" language="javascript" src="phonegap_gwt_helloworld/phonegap_gwt_helloworld.nocache.js"></script>
</head>

<!--                                -->
<!-- The body can have arbitrary html, or     -->
<!-- you can leave the body empty if you want -->
<!-- to create a completely dynamic UI.       -->
<!--                                -->
<body>

</body>
</html>
```

如果你计划在Android上运行此示例，应在phonegap_gwt_helloworld/phonegap_gwt_helloworld.nocache.js标签之后添加以下内容：

```
<script type="text/javascript">
document.addEventListener("deviceready", (function(){ PhoneGap.available = true;}), false);
</script>
```

现在打开src文件夹中的PhoneGap_GWT_Helloworld.java，并进行以下更改：

```
package com.phonegap.example.gwt.helloworld.client;
import com.google.gwt.core.client.EntryPoint;
import com.google.gwt.user.client.ui.Label;
import com.google.gwt.user.client.ui.RootPanel;

/**
 * Entry point classes define <code>onModuleLoad()</code>.
 */
public class PhoneGap_GWT_Helloworld implements EntryPoint {

    /**
     * This is the entry point method.
     */
    public void onModuleLoad() {
        RootPanel.get().add(new Label("GWT Phone Gap Demo"));
    }
}
```

**236 第6章：将PhoneGap与GWT结合使用**

默认创建的GWT项目包含一个用于客户端-服务器通信的RPC组件，此应用并不需要它。因此，你可以从项目中移除以下条目：

- 客户端包中的GreetingService.java和GreetingServiceAsync.java
- Shared和server包
- web.xml中的任何servlet

现在，运行GWT项目（run as -> Web application），你应该会看到如图6–2所示的屏幕。请注意，此示例将在浏览器中运行，以确保你的GWT项目已正确设置。

![](img/4a75e501abc949744a790d09257a5b1e_239_0.png)

**图6–2.** 在Chrome浏览器中运行GWT项目

下一步是实际使用PhoneGap API将GWT项目编译成Web应用。

PhoneGap GWT库的一个好处是，当作为GWT Web应用启动时，它会模拟PhoneGap库。该库根据以下指令提供替代功能：

1. 如果在Android或iPhone上运行，则使用PhoneGap JavaScript。
2. 否则，使用内部模拟类并提供虚拟值。

首先使用延迟绑定创建一个PhoneGap对象：

```
PhoneGap PhoneGap = (PhoneGap)GWT.create(PhoneGap.class);
```

下一步是在PhoneGap框架内注册以下回调：

*Phonegapavailablehandler*：此回调将在一切正常且 PhoneGap 正确初始化时触发。简而言之，这是一个成功回调。

*Phonegaptimeouthandler*：此回调在 PhoneGap 未在给定时间限制内初始化时触发，可能是由于 PhoneGap 框架初始化失败。简而言之，这是一个失败回调。

最后，你需要通过调用 `PhoneGap.initializePhoneGap()` 来初始化 PhoneGap 框架。调用此 API 将触发上述回调之一。

主要代码将被编写为 `PhoneGapAvailableHandler` 回调，如下所示。使用 PhoneGap 变量是安全的，因为 PhoneGap 已正确初始化。在以下代码中，你从 PhoneGap 获取设备处理程序，然后在网格（一个 2 列 5 行的表格）中打印设备信息值：

```
Device device = phoneGap.getDevice();
Grid grid = new Grid(5, 2);
//Add a row mentioning Name Property of Device
grid.setWidget(0, 0, new Label("Name"));
grid.setWidget(0, 1, new Label(device.getName()));

//Add a row mentioning Platform Property of Device
grid.setWidget(1, 0, new Label("Platform"));
grid.setWidget(1, 1, new Label(device.getPlatform()));

//Add a row mentioning Version Property of Device
grid.setWidget(2, 0, new Label("Version"));
grid.setWidget(2, 1, new Label(device.getVersion()));

//Add a row mentioning Name Property of Device
grid.setWidget(3, 0, new Label("PhoneGapVersion"));
grid.setWidget(3, 1, new Label(device.getPhoneGapVersion()));

//Add a row mentioning Name Property of Device
grid.setWidget(4, 0, new Label("UUID"));
grid.setWidget(4, 1, new Label(device.getUuid()));

grid.setBorderWidth(1);
RootPanel.get().add(grid);
```

这是一个完整的示例：

```
package com.phonegap.example.gwt.helloworld.client;
import com.google.gwt.core.client.EntryPoint;
import com.google.gwt.core.client.GWT;
import com.google.gwt.user.client.Window;
import com.google.gwt.user.client.ui.Grid;
import com.google.gwt.user.client.ui.Label;
import com.google.gwt.user.client.ui.RootPanel;

import de.kurka.phonegap.client.PhoneGap;
import de.kurka.phonegap.client.PhoneGapAvailableEvent;
import de.kurka.phonegap.client.PhoneGapAvailableHandler;
import de.kurka.phonegap.client.PhoneGapTimeoutEvent;
import de.kurka.phonegap.client.PhoneGapTimeoutHandler;
import de.kurka.phonegap.client.device.Device;

/**
 * Entry point classes define <code>onModuleLoad()</code>.
 */
public class PhoneGap_GWT_Helloworld implements EntryPoint {

    /**
     * This is the entry point method.
     */
    public void onModuleLoad() {
        final PhoneGap phoneGap = GWT.create(PhoneGap.class);
        phoneGap.addHandler(new PhoneGapAvailableHandler() {

            public void onPhoneGapAvailable(PhoneGapAvailableEvent event) {
                Device device = phoneGap.getDevice();

                Grid grid = new Grid(5, 2);
                //Add a row mentioning Name Property of Device
                grid.setWidget(0, 0, new Label("Name"));
                grid.setWidget(0, 1, new Label(device.getName()));
                //Add a row mentioning Platform Property of Device
                grid.setWidget(1, 0, new Label("Platform"));
                grid.setWidget(1, 1, new Label(device.getPlatform()));
                //Add a row mentioning Version Property of Device
                grid.setWidget(2, 0, new Label("Version"));
                grid.setWidget(2, 1, new Label(device.getVersion()));
                //Add a row mentioning Name Property of Device
                grid.setWidget(3, 0, new Label("PhoneGapVersion"));
                grid.setWidget(3, 1, new Label(device.getPhoneGapVersion()));
                //Add a row mentioning Name Property of Device
                grid.setWidget(4, 0, new Label("UUID"));
                grid.setWidget(4, 1, new Label(device.getUuid()));
                grid.setBorderWidth(1);
                RootPanel.get().add(grid);

            }
        });

        phoneGap.addHandler(new PhoneGapTimeoutHandler() {
            public void onPhoneGapTimeout(PhoneGapTimeoutEvent event) {
                Window.alert("can not load phonegap");
            }
        });

        phoneGap.initializePhoneGap();
    }
}
```

你可以使用“run as -> web application”从 Eclipse 运行此示例，并在浏览器中访问 http://127.0.0.1:8888/PhoneGap_GWT_Helloworld.html?gwt.codesvr=127.0.0.1:9997 来查看代码。

你将看到如图 6–3 所示的表格。如上所述，当在浏览器中运行代码（而非在 Android 或 iPhone 上）时，GWT PhoneGap 会显示模拟值。

![](img/4a75e501abc949744a790d09257a5b1e_242_0.png)

**图 6–3.** *在 Chrome 浏览器中运行 GWT PhoneGap 项目*

最后一步是将此项目编译为 Web 应用程序。右键单击项目，选择 Google 选项，然后单击名为“GWT compile”的菜单选项。你将看到如图 6–4 所示的对话框。点击编译。

## 第六章：结合 GWT 使用 PhoneGap

![](img/4a75e501abc949744a790d09257a5b1e_243_0.png)

**图 6–4.** *GWT 编译界面*

编译完成后，在 Eclipse 中刷新项目，你应该会看到如图 6–5 所示的目录结构。在 war 文件夹内，你应该会看到一个包含许多 HTML 和 JavaScript 文件的 phonegap_gwt_helloworld 文件夹，如下所示。

![](img/4a75e501abc949744a790d09257a5b1e_244_0.png)

**图 6–5.** *GWT 编译后的 War 目录结构*

## 构建 PhoneGap Android 应用程序

构建 PhoneGap GWT 应用程序的最后一步是创建一个 Android PhoneGap 项目，如图 6–6 和图 6–7 所示，然后将 GWT 生成的 Web 应用程序复制到 assets/www 文件夹中。

第一步是创建一个 Android 项目。

## 第六章：结合 GWT 使用 PhoneGap

![](img/4a75e501abc949744a790d09257a5b1e_245_0.png)

**图 6–6.** *Android 创建项目界面*

![](img/4a75e501abc949744a790d09257a5b1e_246_0.png)

**图 6–7.** *Android 创建项目界面*

现在，将 PhoneGap 0.9.4 库注入到 Android 项目中。

## 第六章：结合 GWT 使用 PhoneGap

从
http://phonegap.googlecode.com/files/phonegap-0.9.4.zip 下载 PhoneGap 0.9.4 库。解压缩该文件，你将看到如图 6-8 所示的文件夹结构。

![](img/4a75e501abc949744a790d09257a5b1e_247_0.png)

在 Android 项目文件夹中创建一个 lib 文件夹，将 PhoneGap.0.9.4.jar 文件复制到 lib 文件夹中，然后将其添加到 Eclipse 的 classpath 中。（右键单击 jar 文件，选择“Build Path”，然后单击“Add to Build Path”。）

下一步是在 assets 文件夹内创建一个 www 文件夹，并将 PhoneGap.0.9.4.js 文件复制到 www 文件夹中。然后你需要将以下文件从 GWT 项目复制到同一文件夹：

- PhoneGap_GWT_Helloworld.html
- PhoneGap_Gwt_Helloworld.css
- phonegap_gwt_helloworld 文件夹

你的文件夹结构现在应该类似于图 6-9 中的示例。名为“gwt”的文件夹中的文件是在项目编译时生成的。

![](img/4a75e501abc949744a790d09257a5b1e_248_0.png)

**图 6–9.** *使用 Android 的 GWT PhoneGap 项目目录结构*

现在你需要修改以下文件：

- HelloWorld.java 文件
- PhoneGap_GWT_Helloworld.html

此外，你需要检查 HelloWorld.java 文件是否类似于以下内容：

```
package com.phonegap.gwt.helloworld;
import android.os.Bundle;
import com.phonegap.DroidGap;
public class HelloWorld extends DroidGap {
    /** Called when the activity is first created. */
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        super.loadUrl("file:///android_asset/www/PhoneGap_GWT_Helloworld.html");
    }
}
```

在 PhoneGap_GWT_Helloworld.html 文件中，你需要进行一些代码更改。

首先，添加适用于 Android 的 PhoneGap JavaScript 库 0.9.4 版本，如下所示：

```
<script type="text/javascript" src="phonegap.0.9.4.js"></script>
```

接下来，监听 deviceready 事件以确定 PhoneGap 库是否已准备好使用：

```
<script type="text/javascript">
    document.addEventListener(
        "deviceready",
        (function() {
            PhoneGap.available = true;
        }),
        false);
</script>
```

在此处显式地将 PhoneGap.available 变量设置为 true。这是 Android 平台的必需步骤。

以下是 PhoneGap_GWT_Helloworld.html 的完整源代码：

```
<!doctype html>
<!-- The DOCTYPE declaration above will set the -->
<!-- browser's rendering engine into -->
<!-- "Standards Mode". Replacing this declaration -->
<!-- with a "Quirks Mode" doctype may lead to some -->
<!-- differences in layout. -->
<html>

    <head>
        <meta http-equiv="content-type" content="text/html; charset=UTF-8">
        <!-- -->
        <!-- Consider inlining CSS to reduce the number of requested files -->
        <!-- -->
        <link type="text/css" rel="stylesheet" href="PhoneGap_GWT_Helloworld.css">
        <!-- -->
        <!-- Any title is fine -->
        <!-- -->
        <title>
            Gwt PhoneGap Demo
        </title>
        <!-- -->
        <!-- This script loads your compiled module. -->
        <!-- If you add any GWT meta tags, they must -->
        <!-- be added before this line. -->
        <!-- -->
        <script type="text/javascript" language="javascript" src="phonegap.0.9.4.js"></script>
        <script type="text/javascript" language="javascript" src="phonegap_gwt_helloworld/phonegap_gwt_helloworld.nocache.js"></script>
        <script type="text/javascript">
                        document.addEventListener("deviceready", (function() {
                PhoneGap.available = true;
            }), false);
        </script>
    </head>
    <!-- -->
```



## GWT PhoneGap 参考资料

以下列出了本 GWT PhoneGap 项目中使用的文档和源代码的链接。Daniel Kurka 是此库的作者。

主页 – http://code.google.com/p/gwt-phonegap/

入门指南 – http://code.google.com/p/gwt-phonegap/wiki/GettingStarted

下载 jar 包 – http://gwt-phonegap.googlecode.com/files/gwt-phonegap-0.8.jar

下载 Javadocs – http://gwt-phonegap.googlecode.com/files/gwt-phonegap-0.8-javadoc.jar

源代码 – http://code.google.com/p/gwt-phonegap/source/browse/

当前功能 – http://code.google.com/p/gwt-phonegap/wiki/Features

## PhoneGap 模拟器与远程调试

### 简介

我在开发 PhoneGap 应用时经历的最大痛点是以下循环：

- 1. 在 Eclipse/Xcode 或任意 IDE 中进行开发
- 2. 编译并将二进制可执行文件放入设备/模拟器
- 3. 在设备/模拟器上测试 PhoneGap 应用
- 4. 调整代码并从第 1 步重新开始

显然，这个循环非常耗时且令人沮丧。如果你是有经验的 JavaScript 开发者，这对你来说将是场噩梦。

JavaScript 开发者习惯使用以下现代浏览器中便捷的工具：

- 1. Firefox
- 2. Safari
- 3. Chrome
- 4. Internet Explorer

（请注意，对于 iPhone 和 Android 开发，Internet Explorer 没有用处。我们建议使用 Firefox、Safari 或 Chrome 进行 iPhone 和 Android 开发。）

这些工具中有少数是面向开发者的扩展程序。Firefox 有其 own Firebug，它是 JavaScript/HTML 调试工具系列中的第一个，允许你不仅调试页面元素（DOM 结构），还能调试脚本、样式表和网络。它还允许你即时更改这些内容并立即进行测试。

Chrome 和 Safari 内置了开发者工具。Internet Explorer 也不例外，也有自己的扩展程序来实现类似功能。

显然，在开发 PhoneGap 时，我们需要类似的东西。让我们在此列出两项需求。我们需要：

- 1. 能够使用 PhoneGap 模拟器在浏览器环境中创建和测试 PhoneGap 之外的应用程序
- 2. 能够在将 PhoneGap 应用部署到某个模拟器或设备后对其进行调试

在本章中，我们将讨论使用 PhoneGap 模拟器和远程调试工具。

### 适用于 Chrome 的 PhoneGap 模拟器 – 使用 Ripple

Ripple 是来自一家名为 tinyHippos 公司的多平台移动平台模拟器。最近，该公司被 Research In Motion (RIM) 收购。Ripple 之所以出现，主要是为了应对当今移动操作系统世界高度碎片化给移动 Web 开发者带来的挑战。

Ripple 是一个 Chrome 扩展程序，提供对以下平台的模拟：

- 1. PhoneGap
- 2. Webworks（来自黑莓）
- 3. WebWorks-Tablet-OS（来自黑莓）
- 4. 移动 Web
- 5. WAC
- 6. Opera
- 7. Vodafone

出于本书目的，我们将只关注 Ripple 对 PhoneGap 的模拟。

### 安装 Ripple

Ripple 的唯一先决条件是你需要 Chrome 浏览器。任何支持扩展程序的版本都可以，所以你不需要担心安装哪个版本的 Chrome。不过，我们确实建议使用最新版本。

打开 Chrome 并访问网站 – http://ripple.tinyhippos.com/

你将看到如图 7–1 所示的页面；你只需要点击“Get Ripple”按钮。

图 7–1. *Ripple 主页*

这将带你进入如图 7–2 所示的页面。现在点击“Install”。

**图 7–2.** 将 Ripple 安装为 Chrome 扩展程序

正如我们之前提到的，Ripple 是一个 Chrome 扩展程序。点击“Install”会将你带到 Chrome 网上应用店。当你点击“Add to Chrome”时，扩展程序/插件实际上是从 Chrome 网上应用店下载并自动安装到你的 Chrome 浏览器中（参见图 7–3）。

**图 7–3.** 从 Chrome 网上应用店安装 Ripple

一旦插件安装完成，你将看到类似图 7–3 所示的屏幕。

**图 7–4.** *在 Chrome 上安装 Ripple*

为了验证插件已正确安装，请在 Chrome 中打开一个网站，例如 www.google.com，然后在页面上单击右键。如果插件已正确安装，你应该会看到一个“Emulator”启用/禁用的选项。如图 7–5 所示。

**图 7–5.** *在 Chrome 上单击右键打开 Ripple 模拟器的选项*

继续点击“Emulator”并选择“Enable”。如果你看到图 7–6 中的屏幕，那么你的 Ripple 插件工作正常。要退出该屏幕，只需单击右键并选择 Emulator -> Disable。

图 7-6. *Ripple 首次启动*

### 高效地在 Chrome 中使用 PhoneGap

在继续使用 Chrome 上的 Ripple 之前。让我们了解如何高效地在 Chrome 中使用 PhoneGap。PhoneGap 与移动 Web 应用程序有相似之处，但在许多方面也存在差异。让我们列出两个主要区别。

- 1. PhoneGap 应用程序是基于 HTML/JavaScript 的应用程序，但它们从不托管。它们作为原生移动应用程序的一部分进行打包，并在应用程序内嵌的浏览器中显示。这类似于在 Chrome 上从磁盘测试你的 HTML/JavaScript 应用程序。需要调整 Chrome 以支持从磁盘运行 html/javascript 应用程序。
- 2. PhoneGap 没有任何与之关联的域名。这就是为什么它们不遵循同源策略。如果你想为从文件系统或本地 Web 服务器托管的 PhoneGap 应用程序模拟不遵循同源策略，你需要调整 Chrome 以支持关闭同源策略。

为了从本地文件系统测试 PhoneGap 应用程序且不使其遵循同源策略，你需要使用接下来几段讨论的命令行参数启动 Chrome。

### Windows

在 Windows 中，创建一个名为 chrome.cmd 的 .cmd 文件，并将以下脚本复制到该文件中。现在使用 chrome.cmd 启动 Chrome。

```
chrome.exe --disable-web-security --allow-file-access-from-files
```

### Mac 和 Linux

在 Mac 上，创建一个名为 chrome.sh 的脚本，并将以下脚本复制到其中。现在使用 chrome.sh 启动 Chrome。

```
open "/Applications/Google Chrome.app" --args --disable-web-security --allow-file-access-from-files
```

更改 chrome.sh 脚本的权限使其可执行（运行脚本所需）。

```
$>chmod +x chrome.sh
Run the script from terminal as follows:
$>./chrome.sh
```

### 使用 Ripple

现在我们将了解如何使用 Ripple 以及在 Ripple 中运行你的 PhoneGap 应用需要哪些更改。

以下是在 Ripple 中使用 PhoneGap 应用的先决条件：

- 1. 应用需要是纯 PhoneGap 应用，不包含任何插件。
- 2. 你需要从所有 HTML 文件中移除对 PhoneGap JavaScript 的任何引用。

### 为 Ripple 调整你的应用

让我们以第 2 章的代码示例为例。

我们将使用指南针应用的示例。从这个 URL 获取指南针图像 – http://beginingphonegap.googlecode.com/files/compass.png。此图像如图 7–7 所示。

图 7–7. 将在 PhoneGap 应用程序中使用的指南针图像

现在，让我们修改 index.html 文件使其如下所示。请注意，我们已经移除了对 phonegap.js 的所有引用。这是目前使用 Ripple 的先决条件。Ripple 正在与 PhoneGap 合作以消除此更改。希望在未来的版本中，我们将看到此要求消失。

```
<!DOCTYPE HTML>
<html>
    <head>
        <title>
            PhoneGap
        </title>
```



<script type="text/javascript">
    /** 当PhoneGap的JavaScript加载完毕时被调用 */

    function onDeviceReady() {
        var button = document.getElementById("capture");
        var compassOptions = {
            frequency: 1000
        };
        navigator.compass.watchHeading(onSuccess, onError, compassOptions);
    };

    function onSuccess(heading) {
        var image = document.getElementById('compass');
        var headingDiv = document.getElementById('compassHeading');
        headingDiv.innerHTML = heading;
        var reverseHeading = 360 - heading;
        image.style.webkitTransform = "rotate(" + reverseHeading + "deg)";
    }

    function onError(error) {
        alert('code: ' + error.code + '\n' + 'message: ' + error.message + '\n');
    }

    /** 当浏览器加载此页面时被调用 */

    function init() {
        document.addEventListener("deviceready", onDeviceReady, false);
    }
</script>
</head>

<body onLoad="init()">
    <h1>
        指南针
    </h1>
    <table>
        <tr>
            <td>
                指南针航向
            </td>
            <td>
                <div id="compassHeading">
                    ....
                </div>
            </td>
            <td>
                度数
            </td>
        </tr>
    </table>
    <img id="compass" src="compass.png" style="width:400px;height:400px;margin-left:auto;margin-right:auto;auto;display:block">
</body>

</html>

你的应用目录将如图 7–8 所示。它包含了应用程序的所有HTML、JavaScript和CSS文件。

![](img/4a75e501abc949744a790d09257a5b1e_260_0.png)

## 使用特殊标志启动Chrome

下一步是使用特殊标志启动Chrome（正如本章前面我们所做的那样）。

使用 `--disable-web-security --allow-file-access-from-files` 标志启动Chrome。

一旦Chrome启动，请前往 Window->Extensions，找到 “Ripple Mobile Environment Emulator” 扩展，并勾选 “Allow access to file URLs” 选项（参见图 7–9）。

![](img/4a75e501abc949744a790d09257a5b1e_260_1.png)

## 在Chrome中加载应用

现在在Chrome中加载指南针应用程序。在右上角，你会看到Ripple图标。点击该图标以为此应用启用Ripple。如图 7–10 所示。

请注意，因为我们使用了上述标志启动Chrome，所以Chrome才能够从本地文件系统加载HTML文件。此外，如果PhoneGap应用程序通过Ajax加载数据，它也能在Chrome中工作，因为我们已经禁用了同源策略。

![](img/4a75e501abc949744a790d09257a5b1e_261_0.png)

图 7–10. *在Chrome浏览器中加载指南针应用*

## 启用Ripple

首次启用Ripple时，你将看到图 7–11。我们需要选择PhoneGap选项。

![](img/4a75e501abc949744a790d09257a5b1e_261_1.png)

图 7–11. *为指南针应用启用Ripple*

## 试用Ripple设置

既然我们已经启用了Ripple，我们会看到网页发生了变化。这个原本占据整个屏幕的应用程序，现在看起来不一样了。这是因为现在Ripple是主应用程序。Ripple在一个iframe中加载我们自己的应用程序，并注入自身来模拟PhoneGap环境。在主页面上，Ripple提供了一系列控件，用于更改PhoneGap所模拟的设备的状态和属性（参见图 7–12）。

![](img/4a75e501abc949744a790d09257a5b1e_262_0.png)

图 7–12. 在启用了Ripple的Chrome浏览器中加载的指南针应用

## 使用Ripple测试应用程序

被测试的应用程序是一个指南针应用。为了测试这个应用程序，我们将使用右下角用红色标记的geo和compass控件（参见图 7–12）。如果我们更改航向，就意味着我们正在模拟用户移动其设备的指南针方位。

正如你在图 7–13 中所见，当我们更改航向时，可以看到指南针图像围绕中心旋转。

# 第七章：PhoneGap模拟器与远程调试

![](img/4a75e501abc949744a790d09257a5b1e_263_0.png)

图 7–13. *使用Ripple模拟PhoneGap的指南针API*

模拟PhoneGap只是Ripple的一个方面。Ripple允许开发者使用他们常规的浏览器工具来调试并更改其应用程序的DOM和CSS。在图 7–14 中，我们右键点击图像并选择了“检查元素”。然后我们可以检查被检查DOM元素的CSS样式，在我们的例子中就是html img。

![](img/4a75e501abc949744a790d09257a5b1e_264_0.png)

## 远程调试 – http://debug.phonegap.com

虽然使用Ripple来模拟、测试和调试PhoneGap应用程序是可行的并且非常有帮助，但没有什么比在真实的模拟器或设备上调试更棒的了。

在真实的模拟器或设备上进行调试的问题在于，用于显示PhoneGap应用程序的webkit webview基本上是隔离的，无法从外部访问。这与Chrome、Firefox或Safari不同，在这些浏览器中，用户可以检查HTML元素。但是运行在WebView内的应用程序（例如PhoneGap应用程序中的HTML/Javascript）是无法被检查的。

这就是远程调试发挥作用的地方。请参见图 7–15 以更好地理解这个概念。基本思想是将一个调试JavaScript注入到我们的PhoneGap应用程序中。这会打开一个与debug.phonegap.com服务器的通信通道。然后开发者在浏览器中打开debug.phonegap.com，并检查在设备/模拟器上运行的PhoneGap应用程序。

![](img/4a75e501abc949744a790d09257a5b1e_265_0.png)

**图 7–15. 远程调试架构**

## 设置远程调试

进行远程调试的第一步是在浏览器中打开 http://debug.phonegap.com。在这里你可以提供自己的指南（就像我们做的那样），或者使用服务器随机分配的一个。

## 将远程调试注入PhoneGap应用

下一步是从 http://debug.phonegap.com 复制JavaScript代码片段，并将其注入到你的PhoneGap应用程序中。如下所示（已添加下划线）。

```html
<!DOCTYPE HTML>
<html>
<head>
    <title>PhoneGap</title>
    <script type="text/javascript" src="phonegap.1.1.0.js">
    </script>
    <script type="text/javascript">
        /** 当PhoneGap的JavaScript加载完毕时被调用 */
        function onDeviceReady(){
            document.getElementById("deviceName").innerHTML = device.name;
            document.getElementById("phoneGapVersion").innerHTML = device.phonegap;
            document.getElementById("mobilePlatform").innerHTML = device.platform;
            document.getElementById("platformVersion").innerHTML = device.version;
            document.getElementById("uuid").innerHTML = device.uuid;
        }

        /** 当浏览器加载此页面时被调用 */
        function init(){
            document.addEventListener("deviceready", onDeviceReady, false);
        }
    </script>
    <script src="http://debug.phonegap.com/target/target-script-min.js#beginning-phonegap"></script>
</head>
<body onLoad="init()">
    <h1>设备信息</h1>
    <table border="1">
        <tr>
            <td>
                设备名称
            </td>
            <td id="deviceName"></td>
        </tr>
        <tr>
            <td>
                PhoneGap版本
            </td>
            <td id="phoneGapVersion"></td>
        </tr>
        <tr>
            <td>
                移动平台
            </td>
            <td id="mobilePlatform"></td>
        </tr>
        <tr>
            <td>
                平台版本
            </td>
            <td id="platformVersion"></td>
        </tr>
        <tr>
            <td>
                UUID
            </td>
            <td id="uuid"></td>
        </tr>
    </table>
</body>
</html>
```

![](img/4a75e501abc949744a790d09257a5b1e_266_0.png)

## 调试和修改DOM元素

下一步是在模拟器或设备上启动PhoneGap应用程序。当此应用程序启动时，其内部运行的JavaScript将与debug.phonegap.com服务器进行通信。然后我们就可以进行远程调试了（参见图 7-17）。

![](img/4a75e501abc949744a790d09257a5b1e_268_0.png)

最后一步是在浏览器中打开 http://debug.phonegap.com/client/#beginning-phonegap（参见图 7–18）。请记住，这个URL是从 http://debug.phonegap.com 网站获得的。

![](img/4a75e501abc949744a790d09257a5b1e_268_1.png)

现在切换到元素选项卡（参见图 7–19）。在这里，你将能够看到PhoneGap应用程序中页面的DOM元素。



## 第7章：PhoneGap 模拟器与远程调试

乐趣不止于此。现在你可以修改 DOM 元素（参见图 7-20）。为此，请双击任意 DOM 元素（在我们的例子中是 TD），然后手动输入样式部分。在我们的例子中，我们将为包含 0.9.5 文本的 td 添加样式 "style='background:red'"。现在，我们将切换到在模拟器中运行的 PhoneGap 应用程序，以查看更改生效。

**图 7–20.** *在 http://debug.phonegap.com 上修改 DOM 属性*

现在，包含 "0.9.5" 的 TD 元素的背景颜色变为红色（参见图 7–21）。这种调试方式有助于我们实时调试设备/模拟器上的应用程序。

*图 7–21. 在 http://debug.phonegap.com 上所做的更改反映在 Android 模拟器上*

## debug.phonegap.com 的问题

到目前为止，我们已经看到使用 http://debug.phonegap.com 对于检查真实设备或模拟器内部运行的内容非常有用。但是，我们不想使用它，原因如下：

- 在开发过程中，我们不想使用外部服务器。
- 我们希望节省带宽并提高调试速度。

注意：一个 Weinre（**web inspector remote**）服务器为 debug.phonegap.com 提供支持。PhoneGap 团队也开发了 Weinre，并且他们对此做了很好的文档记录。

## 安装本地 debug.phonegap.com

虽然 Weinre 的安装和部署不在本书的范围内，但我将以链接的形式提供一些关于如何本地部署 Weinre 的说明。

Weinre 的文档非常完善，如果您遵循它，应该可以毫无问题地在本地安装和使用 Weinre。

访问 http://phonegap.github.com/weinre/Installing.html 获取安装文档（参见图 7-22）。

*图 7-22. 如何安装 Weinre 的说明*

访问 http://phonegap.github.com/weinre/Running.html 获取运行说明（参见图 7-23）。

## 结论

在开发 PhoneGap 应用程序时，使用 iPhone/Android 模拟器测试代码非常耗时且令人沮丧。为了节省时间和精力并简化开发，请使用 Ripple PhoneGap 模拟器。充分利用 Chrome 的开发者工具来加速您的开发。对于远程调试，请使用 http://debug.phonegap.com 或本地安装的 Weinre 服务器。这有助于您了解应用程序在 iPhone/Android 模拟器或实际设备上运行时，HTML DOM 实际发生了什么。

## 第8章：使用 PhoneGap 插件

PhoneGap 附带一组 JavaScript API，用于访问原生手机功能，例如相机、存储、联系人、地理定位等，以构建跨平台移动应用程序。如果您想做一些 PhoneGap API 中未提供的功能，您可以利用 PhoneGap 插件。

在任何技术中，重用已经存在且经过测试的功能是常见的做法。有许多重要的第三方插件可用于 PhoneGap。例如，访问 Facebook 的身份验证机制、访问第三方移动推送通知服务等。

### 什么是 PhoneGap 插件？

PhoneGap 插件是 PhoneGap 功能的扩展。它访问手机上的一段功能。插件功能可能只能访问手机的原生功能，也可能提供访问云服务的功能。

任何 PhoneGap 插件至少由两个文件组成：

- JavaScript 文件
- 原生语言文件

插件的 JavaScript 文件是 PhoneGap 应用程序与 PhoneGap 插件之间的接口。插件的功能通过 JavaScript 文件使用 JavaScript 函数进行访问。

原生语言文件由 PhoneGap 框架使用，以便与手机交互以访问原生功能。作为插件用户，我们需要将原生代码放入我们的项目结构中。在下一节中，我们将详细研究如何使用此插件设置项目。

### Facebook 身份验证与获取好友

让我们利用 PhoneGap 插件构建一个小型应用程序，用于登录 Facebook 并从 Facebook 获取好友信息。

我们的 PhoneGap 应用程序将使用 Facebook 原生应用程序，通过 Facebook-PhoneGap 插件为用户执行单点登录（SSO）。

### 设置 Android 环境

首先，我们需要为 Android 设置 PhoneGap 项目。请参阅第2章设置您的 Android 项目。Android 项目配置如图 8–1 所示。

从 https://github.com/davejohnson/phonegap-plugin-facebook-connect/downloads 下载 Facebook-connect 插件。
Facebook-connect 插件是一个 zip 文件。将其解压缩到您喜欢的文件夹中。文件夹结构应类似于图 8–2。

*图 8–2. Facebook-connect 插件文件夹结构*

接下来，您需要执行以下安装步骤：

1. 注册 Facebook 插件
将以下 XML 元素作为 plugins.xml 文件中 "plugins" 元素的子元素添加，如图 8–3 所示。您可能需要使用以下命令在 res 文件夹中创建一个 xml 文件夹：

```xml
<plugin name="com.phonegap.facebook.Connect" value="com.phonegap.facebook.ConnectPlugin" />
```

*图 8-3. Facebook 插件注册*

2. 将插件的原生部分包含到项目中。从 Facebook-connect-plug-in 文件夹中复制 libs 和 src 文件夹（如图 8-4 所示），并将其粘贴到我们的 PhoneGap 应用程序根目录，即 "FaceBookPluginExample" 中。

*图 8-4. Facebook-connect-plug-in 的 Android 原生文件夹*

3. 在项目中包含插件的 JavaScript 部分

我们需要从 Facebook-connect 插件中将两个 JavaScript 文件包含到我们的项目中。

```
/www/pg-plugin-fb-connect.js
```

pg-plugin-fb-connect.js 文件位于 Facebook 插件的 www 文件夹下。将其复制并粘贴到我们项目的 assets/www 文件夹中。

```
/lib/facebook_js_sdk.js
```

facebook_js_sdk.js 文件位于 Facebook 插件的 lib 文件夹下。将其复制并粘贴到我们项目的 assets/www 文件夹中。

完成这三个步骤后，您将看到如图 8–5 所示的 FaceBookPluginExample 项目结构。

### 初始化 Facebook-Connect 插件

第一步是确保 index.html 引入了 Facebook-Connect 库、PhoneGap 库，并链接了 CSS。请注意，我们正在引入以下 JavaScript 文件。

1. PhoneGap JavaScript
2. Facebook 插件 JavaScript
3. Facebook SDK JavaScript

```html
<html>
<head></head>
<body>
<div id="friends"></div>
<!--phonegap -->
<script src="phonegap-1.1.0.js"></script>
<!--phonegap facebook plugin -->
<script src="pg-plugin-fb-connect.js"></script>
<!--facebook js sdk -->
<script src="facebook_js_sdk.js"></script>
</body>
</html>
```

现在，我们将在 index.html 页面中定义 JavaScript 函数，用于登录 Facebook 和获取好友列表。以下是登录函数的代码片段：

```javascript
function login() {
    FB.login(function(response) {...},
        { perms: "email" }
    );
}
```

login() 函数调用 Facebook SDK 的登录函数 FB.login()。Facebook 的 FB.login() 有两个参数。第一个是回调 JavaScript 函数，第二个是用于指定权限的 JSON 对象。我们将 'function(response){...}' 和 '{ perms: "email" }' 传递给 FB.login()。Facebook 的 FB.login() 会提示用户登录。登录成功后，它会调用回调 JavaScript 函数。回调函数获取 'response' 对象以识别登录状态。'perms' 用于指定用户权限。您可以在 Facebook 开发者网站 http://developers.facebook.com/docs/reference/api/permissions 上找到有关 Facebook 登录 API 和用户权限的更多详细信息。

接下来，我们将查看用于获取好友列表的代码片段。为此，我们将创建一个 JavaScript 函数 getFriendList()。

```javascript
function getFriendList(){
    FB.api('/me/friends', function(response) {
        if (response.error) {
            alert(JSON.stringify(response.error));
        } else {
            var friends = document.getElementById('friends');
            response.data.forEach(function(item) {
                var d = document.createElement('div');
                d.innerHTML = item.name;
                friends.appendChild(d);
            });
        }
    });
}
```

在 getFriendList() 函数中，对 Facebook API FB.api() 进行了调用。第一个参数是 Facebook 提供的图谱 API 的路径。在我们的例子中，'/me/friends' 用于获取已登录用户的好友列表。第二个参数是接收响应的 JavaScript 回调函数。在回调方法中执行以下操作：

1. 使用 'response.error' 检查响应状态是否为成功响应。
2. 如果是成功响应，则遍历响应中可用的结果数据。
3. 为每个项目创建一个 'div' 元素，并将其附加到 index.html 中定义的 'friends' div 中。

接下来，我们将修改 login() 函数，以便在登录成功时调用 getFriendList()。



## 第8章：使用PhoneGap插件

function login() {
    FB.login(
        function(response) {
            if (response.session) {
                getFriendList();
            } else {
                alert('未登录');
            }
        },
        { perms: "email" }
    );
}

在这里，我们检查 `response.session` 值的响应是否成功。如果它是有效的，我们就调用 `getFriendList()` 函数。

现在最后一步是将JavaScript函数与PhoneGap的初始化事件一起使用。

```javascript
document.addEventListener('deviceready',
    function() {
        try {
            /* 初始化Facebook插件。注意，你需要将 <app_id> 替换为你的Facebook app_id */
            FB.init({ appId: "<app_id>", nativeInterface: PG.FB });
            document.getElementById('data').innerHTML = "";
            login();
        } catch (e) {
            alert(e);
        }
    }, false);
```

最后，要运行该应用程序，你需要将你的Facebook app_secret密钥放入AndroidManifest.xml文件中，如图8-6所示。

![img/4a75e501abc949744a790d09257a5b1e_280_0.png](img/4a75e501abc949744a790d09257a5b1e_280_0.png)

**图8-6.** *Facebook app_secret密钥*

你可以从Facebook开发者网站 https://developers.facebook.com/apps 获取Facebook app_id和app_secret。

在模拟器上将FacebookPluginExample作为Android应用运行。第一个屏幕将显示Facebook登录页面，如图8-7所示。

![img/4a75e501abc949744a790d09257a5b1e_281_0.png](img/4a75e501abc949744a790d09257a5b1e_281_0.png)

**图8-7.** Facebook登录界面

成功登录后，你将看到你的好友列表，如图8-8所示。

![img/4a75e501abc949744a790d09257a5b1e_282_0.png](img/4a75e501abc949744a790d09257a5b1e_282_0.png)

**图8-8.** Facebook好友列表

你可以使用jQueryMobile或Sencha Touch，结合Facebook PhoneGap插件，来开发一个有吸引力的Facebook应用程序。此外，你还可以通过使用Facebook插件调用其他Facebook图谱API来添加更多功能。

## 用于向PhoneGap实现移动推送通知的C2DM插件

推送通知或服务器推送是从服务器向客户端发送数据的最新方式。你是否注意到Gmail如何接收和显示你收件箱中新到的邮件？你不需要刷新浏览器或点击某个刷新按钮来向服务器发送请求并接收最新数据。

在最近的过去，轮询（polling）是一种接收通知的流行技术。轮询技术会定期向服务器发送请求，并用收到的响应刷新UI。你可以将其视为一个在预定义的特定间隔发送请求，并从服务器接收更新或通知的后台进程。这种方法存在许多已知的缺点。轮询方式的主要缺点是确定发送请求的合适间隔。间隔过短可能会导致不必要的请求和响应往返，从而造成带宽和服务器资源的浪费。间隔过长则可能违背轮询的目的，因为接收通知会出现延迟，从而不再满足其发送的初衷。如果没有新数据可用，这种方法会消耗手机电池。

服务器推送（server push）允许服务器在无需等待请求的情况下，直接向客户端发送通知或更新。在推送技术中，客户端没有任何后台进程来定期发送请求。服务器在有任何更新时，都可以将其推送给所有已注册的客户端。如果客户端是移动应用程序，这种技术就称为移动推送（mobile push）。

你的PhoneGap应用程序也可以通过PhoneGap插件来利用移动推送技术。让我们为Android平台创建一个小型的PhoneGap应用程序，以接收来自C2DM服务的推送通知。

### 设置Android环境

首先，我们需要为Android设置PhoneGap项目。请参考第2章来设置你的Android项目。一个Android项目配置如图8-9所示。

![img/4a75e501abc949744a790d09257a5b1e_284_0.png](img/4a75e501abc949744a790d09257a5b1e_284_0.png)

**图8-9.** Eclipse Android项目配置

我们将使用Android云到设备消息传递（C2DM）框架进行推送通知。你可以在 http://code.google.com/android/c2dm/#intro 阅读更多关于C2DM服务的信息。

从 http://github.com/awysocki/C2DM-PhoneGap/downloads 下载C2DM PhoneGap插件。C2DM-PhoneGap插件是一个zip文件。将其解压到你喜爱的文件夹中。文件夹结构应类似于图8-10中的列表。

![img/4a75e501abc949744a790d09257a5b1e_285_0.png](img/4a75e501abc949744a790d09257a5b1e_285_0.png)

**图8-10.** C2DM插件文件夹结构

接下来你需要执行以下安装步骤：

1.  **注册C2DM插件**
    将以下XML元素作为plugins.xml文件中“plugins”元素的子元素添加，如图8-11所示。你可能需要在'res'文件夹下创建一个xml文件夹，并将plugins.xml从PhoneGap Android示例应用程序中复制过来。

    ```xml
    <plugin name="C2DMPlugin" value="com.plugin.C2DM.C2DMPlugin" />
    ```

    ![img/4a75e501abc949744a790d09257a5b1e_285_1.png](img/4a75e501abc949744a790d09257a5b1e_285_1.png)

    **图8-11.** 插件注册

2.  **将插件的原生部分包含到项目中**
    将src文件夹从C2DM插件文件夹中复制，如图8-12所示，并将其粘贴到我们的PhoneGap应用程序的根目录中，即“MobilePushPluginExample”。

    ![img/4a75e501abc949744a790d09257a5b1e_286_0.png](img/4a75e501abc949744a790d09257a5b1e_286_0.png)

    **图8-12.** *C2DM插件原生部分*

3.  **将插件的JavaScript部分包含到项目中**
    从C2DM插件文件夹中复制以下文件，如图8-13所示，并将它们粘贴到我们应用程序的assets文件夹中。

    ```
    C2DMPlugin.js
    jquery_1.5.2.min.js
    PG_C2DM_script.js
    index.html
    ```

    请注意，尽管index.html不是插件的一部分，但我们为了节省创建和包含js文件的时间，在我们的项目中使用了它。

    ![img/4a75e501abc949744a790d09257a5b1e_286_1.png](img/4a75e501abc949744a790d09257a5b1e_286_1.png)

    **图8-13.** *插件的JavaScript部分*

    注意，我们没有包含Phonegap.0.9.5.js文件，因为我们使用的是PhoneGap-1.1.0。我们将对PhoneGap-1.1.0进行所需的修改。

4.  **最后我们需要在AndroidManifest.xml文件中为C2DM添加所需的权限。**
    Manifest文件应类似于以下代码清单：

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <manifest xmlns:android="http://schemas.android.com/apk/res/android"
        package="org.examples.mobilepushplugin.example" android:versionCode="1"
        android:versionName="1.0">

        <uses-permission android:name="android.permission.CAMERA" />
        <uses-permission android:name="android.permission.VIBRATE" />
        <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
        <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
        <uses-permission android:name="android.permission.ACCESS_LOCATION_EXTRA_COMMANDS" />
        <uses-permission android:name="android.permission.READ_PHONE_STATE" />
        <uses-permission android:name="android.permission.INTERNET" />
        <uses-permission android:name="android.permission.RECEIVE_SMS" />
        <uses-permission android:name="android.permission.RECORD_AUDIO" />
        <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
        <uses-permission android:name="android.permission.READ_CONTACTS" />
        <uses-permission android:name="android.permission.WRITE_CONTACTS" />
        <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
        <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

        <!-- 开始：C2DM消息相关 -->
        <uses-library android:name="com.google.android.c2dm.C2DMessaging" />

        <permission
            android:name="org.examples.mobilepushplugin.example.permission.C2D_MESSAGE"
            android:protectionLevel="signature" />
        <uses-permission android:name="org.examples.mobilepushplugin.example.permission.C2D_MESSAGE" />

        <uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />

        <uses-permission android:name="android.permission.WAKE_LOCK" />
        <!-- 结束：C2DM消息相关 -->
        <uses-sdk android:minSdkVersion="8" />

        <application android:icon="@drawable/icon" android:label="@string/app_name">
            <activity android:name=".MobilePushPluginExampleActivity"
                android:label="@string/app_name">
                <intent-filter>
                    <action android:name="android.intent.action.MAIN" />
                    <category android:name="android.intent.category.LAUNCHER" />
                </intent-filter>
            </activity>
            <!-- 开始：C2DM消息相关 -->
            <service android:name=".C2DMReceiver" />

            <!-- 只有C2DM服务器可以为该应用发送消息。如果未设置该权限——任何其他应用都可以生成消息 -->
            <receiver android:name="com.google.android.c2dm.C2DMBroadcastReceiver"
                android:permission="com.google.android.c2dm.permission.SEND">
                <!-- 接收实际消息 -->
```



```xml
<intent-filter>
    <action android:name="com.google.android.c2dm.intent.RECEIVE" />
    <category android:name="org.examples.mobilepushplugin.example" />
</intent-filter>
<!-- 接收注册ID -->
<intent-filter>
    <action android:name="com.google.android.c2dm.intent.REGISTRATION" />
    <category android:name="org.examples.mobilepushplugin.example" />
</intent-filter>
</receiver>
<!-- 结束：C2DM 消息相关内容 -->
</application>
</manifest>
```

完成上述三个步骤后，您将看到如图 8-14 所示的 MobilePushPluginExample 项目结构。

![](img/4a75e501abc949744a790d09257a5b1e_288_0.png)

**图 8-14.** *MobilePushPluginExample 项目结构*

## 修改适用于 PhoneGap-1.1.0 的插件

在撰写本书时，C2DM 插件是基于 PhoneGap 0.9.5 版本开发的。要将其与 PhoneGap-1.1.0 配合使用，我们需要完成一些修改。

1.  C2DMPlugin.js 文件。

    打开 C2DMPlugin.js 文件，找到以下函数定义：

    ```
    PhoneGap.addConstructor(function() {
        // 向 PhoneGap 注册 javascript 插件
        PhoneGap.addPlugin('C2DM', new C2DM());

        // 向 PhoneGap 注册插件的 native 类
        PluginManager.addService("C2DMPlugin",
            "com.plugin.C2DM.C2DMPlugin");

        //alert( "added Service C2DMPlugin");
    });
    ```

    删除以下行：

    // 向 PhoneGap 注册插件的 native 类
    PluginManager.addService("C2DMPlugin", "com.plugin.C2DM.C2DMPlugin");

    在 PhoneGap-1.1.0 中，插件必须在 plugin.xml 文件中注册。PluginManager 在 PhoneGap-1.1.0 中已不再可用。我们已经在 plugin.xml 文件中注册了 C2DM 插件。

    修改后的函数如下所示：

    ```
    PhoneGap.addConstructor(function() {
        // 向 PhoneGap 注册 javascript 插件
        PhoneGap.addPlugin('C2DM', new C2DM());

        //alert( "added Service C2DMPlugin");
    });
    ```

2.  移动 C2DMReceiver.java

    我们需要将 C2DMReceiver.java 从 com.phonegap.c2dm 包移动到我们的应用程序项目，即 org.examples.mobilepushplugin.example。为此，请将 C2DMReceiver.java 从 com.phonegap.c2dm 包拖放到 org.examples.mobilepushplugin.example 中，如图 8-15 所示。

    ![](img/4a75e501abc949744a790d09257a5b1e_290_0.png)

    **图 8-15.** *C2DMReceiver.java 的位置*

    我们还需要修改从插件文件夹复制过来的 index.html 文件中的 PhoneGap 版本。为此，请在 script 标签中将 phonegap.0.9.5.js 替换为 phonegap-1.1.0。

## 注册 C2DM 服务

访问 http://code.google.com/android/c2dm/signup 并填写表格以注册发送者。您必须提供 Android 应用程序的包名、发送者账户电子邮件以及其他信息。对于我们的应用程序，包名应为 "org.examples.mobilepushplugin.example"，并且我们应该使用一个 Google 账户作为发送者账户电子邮件。我们需要在 PhoneGap 应用程序中使用该发送者账户电子邮件 ID 来注册设备以接收通知。

## 在 PhoneGap 中使用 C2DM 发送者账户

C2DM 插件附带了开箱即用的 PhoneGap deviceready 实现。我们需要使用我们的 C2DM 发送者账户来注册设备以接收通知。

打开 PG_C2DM_script.js 文件，找到 PhoneGap deviceready 事件实现部分。如图 8-16 所示，将 "your_c2dm_account@gmail.com" 修改为我们的 C2DM 发送者账户。

![](img/4a75e501abc949744a790d09257a5b1e_290_1.png)

**图 8-16.** *使用 C2DM 发送者账户注册应用程序*

## 用于启用 C2DM 服务的 Android 模拟器

您需要使用目标为 "Google APIs(Google Inc.) - API Level 8" 的 AVD（Android 虚拟设备）来运行启用 C2DM 的 Android 应用程序。请参考第 2 章，从 "Android SDK and AVD manager" 创建新的 AVD。

您还必须在模拟器中添加您的 Google 账户。为此，请运行模拟器并打开设置，如图 8-17 所示。

![](img/4a75e501abc949744a790d09257a5b1e_291_0.png)

**图 8-17.** *Android 设置选项*

转到 "Account & Sync"（账户与同步）并点击 "Add Account"（添加账户）。您必须输入您的 Google 账户 ID 和密码。请注意，这不是 C2DM 发送者账户，而是您用于从 Android 手机获取电子邮件和其他内容的 Google 账户。

现在您已准备好测试 C2DM 插件。将 MobilePushPluginExample 作为 Android 应用程序运行。请确保目标模拟器是 Google API 模拟器。您将在模拟器上看到如图 8-18 所示的屏幕。

![](img/4a75e501abc949744a790d09257a5b1e_292_0.png)

**图 8-18.** *模拟器上的 MobilePushPluginExample 输出*

为了理解屏幕上出现的输出，我们将介绍 PG_C2DM_script.js 文件中的 deviceready 事件回调函数。

在这里，`window.plugins.C2DM.register()` 调用插件的方法，将设备或模拟器注册到 C2DM 服务。注册成功后，C2DM 服务器会返回一个 Registration Id (REGID)。此 REGID 用于推送通知消息。但是等等，我们的设备不应该推送消息，它应该是通知接收器，对吧？这里，我们需要理解运行在移动设备上的 PhoneGap 应用程序与托管在 Google 上的 C2DM 服务之间的应用程序服务器所扮演的角色。

让我们用一个例子来理解 C2DM 推送的工作原理。假设 MobilePushPluginExample 安装在多部 Android 手机上。现在，每部手机都从 C2DM 服务接收到一个 REGID。本质上，每个 REGID 都是唯一的。在发送 REGID 之前，C2DM 服务会存储所有关于设备和网络的必要信息，以便后续发送通知。C2DM 负责向设备发送通知。现在，中间应用程序服务器的责任是识别更新的数据，并请求 C2DM 向实际的移动设备发送通知。为此，我们的服务器需要知道这些 REGID。

通常，启用 C2DM 的移动应用程序会将 REGID 发送到我们的服务器。服务器会存储所有运行此应用程序的移动设备的 REGID。一旦服务器决定发送通知，它就会使用 REGID 请求 C2DM 服务执行此操作。

如图 8-18 所示，我们已经从 C2DM 服务收到了 REGID。现在，您可以使用此 REGID 发送推送通知。您可以使用 Java servlet 或 php 来创建服务器端代码以发送消息。要了解更多关于如何发送推送通知的信息，请访问 Android C2DM 网站：http://code.google.com/android/c2dm/index.html#push。

此外，还有一个命令行工具可用于模拟服务器。访问 http://curl.haxx.se/download.html 并下载特定平台的 curl 工具。发送通知有两个步骤：

- 1. 获取认证密钥

    在控制台运行以下命令：

    ```
    D:\cURL>curl https://www.google.com/accounts/ClientLogin -d Email=<C2DM 发送者账户> -d "Passwd=<密码>" -d accountType=GOOGLE -d source=org.examples.mobilepushplugin.example -d service=ac2dm -k
    ```

    您需要将 <C2DM 发送者账户> 和 <密码> 替换为您注册的 Google 账户和密码。

    运行上述命令后，您将获得一个类似以下列表的认证密钥：

    ```
    Auth=DQAAAME%AAABrqkH2KYjDfCD93tndEF7n81IKgf5vczCwELPSXgW6xm_9EACDuolsJFGud7fNBIHcRVI0GzUmLwxFFJqosdnInYNmGahoYu7fpT8vfjNLAVx8hs5aymz9OULg-pzK0yWWai-6BDci1TBCoP2q6ZwJqEjzH6rArHSlD9DhruEKBrogjfBAWyeIm2fs9THvEkilSM0208utOqyfGOid9keCQad5QPV7o0vNSe6urKOV4ZWEXxG7KAlXCsjW18u_mZAz6jj7DlUoVD89MeLvXOW
    ```

- 2. 将消息发送到运行在模拟器上的应用程序

    为了发送通知，我们将使用认证密钥和 REGID，并使用以下 curl 命令：

    ```
    S:\cURL>curl --header "Authorization: GoogleLoginauth=<认证密钥>" "https://android.apis.google.com/c2dm/send" -d registration_id=<REGID> -d "data.message=This is a test message" -d "data.msgcnt=1" -d collapse_key=0 –k
    ```

    将 <认证密钥> 替换为从步骤 1 收到的认证密钥，将 REGID 替换为应用程序在模拟器上收到的 REGID。我们正在向模拟器发送 "This is a test message" 文本作为推送通知。

    我们将看到模拟器上应用程序收到的通知，如图 8-19 所示。



## 扩展PhoneGap

到目前为止，我们已经了解了PhoneGap由两部分组成：
1.  我们从PhoneGap应用程序调用的JavaScript部分。
2.  我们在PhoneGap项目中包含的原生部分，用于暴露手机原生功能。

这两部分适用于我们希望访问常见手机功能的场景，包括：
-   相机
-   加速度计
-   文件系统
-   地理位置
-   存储服务

然而，我们常常需要超越这些功能。

### JavaScript的局限性

我们已经看到JavaScript在过去十年中性能有所提升；它的速度比五年前快了100倍。然而，即使情况如此，有时应用程序仍需处理繁重任务、在后台运行或执行复杂操作。出于性能考虑，这些最好在原生代码中完成。

例如，如果我们想下载一个多部分文件，这涉及并行下载文件的不同部分，然后检查其校验和。这部分最好在Android上用Java编写，在iPhone上用Objective-C编写。

### 解决方案

如果你还记得第1章，我们说过PhoneGap是JavaScript世界和原生世界之间的一座桥梁。整个PhoneGap框架基于插件架构。这意味着PhoneGap提供了一种机制，让我们能够将JavaScript函数（以及参数、返回类型和回调）映射到原生代码。

我们可以将原生代码添加到PhoneGap应用程序中，并使用JavaScript轻松地公开这些代码。为此，我们需要两部分：
1.  执行繁重任务的原生代码。
2.  公开此原生代码的JavaScript代码。

这两部分由PhoneGap框架粘合在一起。

### 架构

PhoneGap的架构如图9-1所示。如我们所观察到的，PhoneGap有两部分：PhoneGap JavaScript引擎和PhoneGap原生引擎。我们将原生代码作为插件添加到PhoneGap原生引擎中，并将JavaScript代码作为插件添加到PhoneGap JavaScript引擎中。

### 范围

本章重点介绍如何扩展PhoneGap功能以暴露更多你的原生代码。

但是，请注意，即使你编写了PhoneGap插件，注入插件的唯一方法是将插件源代码添加到你的项目中。目前没有办法将插件构建到一个包中，然后将该包添加到你的PhoneGap项目中。这阻碍了你使用PhoneGap构建时使用你的自定义插件。

对于本章，我们让插件的本质保持非常简单。我们称之为helloworld插件。我们向插件传递一个名称，并返回一个字符串“Hello <name>! The time now is <Current Time>”。

通过这种方式，我们将主要关注插件的桥接方面。

### 为Android扩展PhoneGap

首先，我们作为Android PhoneGap应用程序的一部分创建插件，然后将其提取出来。这是必需的，因为：
1.  插件需要PhoneGap jar。
2.  我们需要测试插件。

一个插件有两个部分，分别位于PhoneGap框架（桥）的两侧。我们有一个原生部分（一个扩展Plugin的类）和一个使用PhoneGap JavaScript框架的JavaScript文件。

在开始之前，让我们创建一个Android PhoneGap项目（参见图9-2）。这在第2章中有介绍。

然后我们需要为PhoneGap配置基础Android项目：
1.  更改MainScreen类以扩展DroidGap。
2.  将PhoneGap jar添加到类路径。
3.  将PhoneGap JavaScript库添加到assets/www文件夹。

Android项目如图9-3所示。

### 声明插件的原生部分

现在我们为插件添加一个合适的包，例如“org.examples.phonegap.plugins.simpleplugin”。然后我们声明一个名为SimplePlugin的类，它扩展了PhoneGap的com.phonegap.api.Plugin类，如图9-4所示。

一旦你点击“Finish”按钮，你将得到如下代码：

```java
package org.examples.phonegap.plugins.simpleplugin;

import org.json.JSONArray;

import com.phonegap.api.Plugin;
import com.phonegap.api.PluginResult;

/**
 * @author rohit
 *
 */
public class SimplePlugin extends Plugin {

	/* (non-Javadoc)
	 * @see com.phonegap.api.Plugin#execute(java.lang.String, org.json.JSONArray, java.lang.String)
	 */
	@Override
	public PluginResult execute(String action, JSONArray data, String callbackId) {
		// TODO Auto-generated method stub
		return null;
	}
}
```

当我们扩展com.phonegap.api.Plugin类时，必须实现execute方法。execute方法的参数是：
1.  *Action*：要执行的操作。例如，对于一个基于文件的插件，可能是打开、关闭、读取、写入等。
2.  *Data*：从插件的JavaScript端传递的数据。这是从PhoneGap的JavaScript应用程序传递给原生代码的数据。例如，对于一个基于文件的插件，可能是文件名、数据等。
3.  *CallbackId*：用于回调JavaScript函数。

execute方法的返回类型是PluginResult。PluginResult通常接受一个Status枚举和另一个参数，用于描述原因或更多信息。例如，`new PluginResult(Status.OK);`

Status枚举有许多值；所有值列举如下（名称是不言自明的）：
-   NO_RESULT
-   OK
-   CLASS_NOT_FOUND_EXCEPTION
-   ILLEGAL_ACCESS_EXCEPTION
-   INSTANTIATION_EXCEPTION
-   MALFORMED_URL_EXCEPTION
-   IO_EXCEPTION
-   INVALID_ACTION
-   JSON_EXCEPTION
-   ERROR

以下是hello插件的实现，它接受一个名称并返回“Hello <name>! The time is <time>”文本。

```java
package org.examples.phonegap.plugins.simpleplugin;

import java.util.Date;

import org.json.JSONArray;
import org.json.JSONException;

import com.phonegap.api.Plugin;
import com.phonegap.api.PluginResult;
import com.phonegap.api.PluginResult.Status;

/**
 * @author rohit
 *
 */
public class SimplePlugin extends Plugin {

    public static String ACTION_HELLO="hello";

    /*
     * (non-Javadoc)
     *
     * @see com.phonegap.api.Plugin#execute(java.lang.String,
     * org.json.JSONArray, java.lang.String)
     */
    @Override
    public PluginResult execute(String action, JSONArray data, String callbackId) {
        PluginResult pluginResult = null;
        if (ACTION_HELLO.equals(action)) {

            String name = null;
            try {
                name = data.getString(0);

                String result = "Hello " + name + "! The time is "
                        + (new Date()).toString();

                pluginResult = new PluginResult(Status.OK, result);

                return pluginResult;
            } catch (JSONException e) {
                pluginResult = new PluginResult(Status.JSON_EXCEPTION, "missing argument name");
            }
        } else {
            pluginResult = new PluginResult(Status.INVALID_ACTION,
                    "Allowed actions is hello");
        }
        return pluginResult;
    }
}
```

你可以在上面的代码中看到，我们在处理请求之前会显式检查action。如果action不是插件处理的，我们会返回Status.INVALID_ACTION。第二个检查是针对参数的。如果在将第一个参数作为字符串获取时遇到任何JSON异常，我们会返回Status.INVALID_JSON。



当操作和参数正确时，我们创建字符串“Hello <name>! The time is <time>”，并返回带有 `Status.OK` 的结果。

请注意，你无需从此方法生成任何线程。你的整个方法可以是同步的。这不会阻塞调用此代码的 JavaScript 插件调用。这由 PhoneGap 内部处理，这就是为什么我们在 JavaScript 中有成功和失败回调（你将在下一节中看到）。

## 声明插件的 JavaScript 部分

此插件的 JavaScript 部分在名为 `simpleplugin.js` 的文件中声明。声明插件的 JavaScript 部分有三个步骤：

1.  插件注册
    在 PhoneGap 插件的 JavaScript 部分，一切始于调用以将插件添加到 PhoneGap。

```
PhoneGap.addConstructor(function() {
                        // Register the Javascript plug-in with PhoneGap
                        PhoneGap.addPlugin('SimplePlugin', new SimplePlugin());
});
```

插件在 `/res/xml/plugins.xml` 文件中注册。在 `plugins.xml` 文件中的 "plugins" 元素下添加以下 XML 元素作为子元素：

```
<plugin name="SimplePlugin"
        value="org.examples.phonegap.plugins.simpleplugin.SimplePlugin" />
```

注意：这里我们做两件事
a. 将一个 JavaScript 对象注册为名为“SimplePlugin”的插件。
b. 将一个 PhoneGap Java 类注册为名为“SimplePlugin”的服务。你可以将其视为类名“org.examples.phonegap.plugins.simpleplugin.SimplePlugin”的别名。

2.  创建 JavaScript 对象 `SimplePlugin`。
    这是通过声明一个 JavaScript 函数完成的。

```
var SimplePlugin = function() {
}
```

3.  添加插件函数。
    在这一步中，我们将添加插件函数，我们的 JavaScript 将调用它。在以下函数中，我们实际上是将调用委托给原生 PhoneGap 桥，要求它实际调用“SimplePlugin”服务，即“org.examples.phonegap.plugins.simpleplugin.SimplePlugin”类。此外，我们注册了两个回调：一个用于调用成功，一个用于调用失败。然后我们声明了我们想要调用的操作。

你可以回想一下，我们的插件类中有处理“hello”服务的代码。最后，请记住我们的插件类的 `execute` 方法接受一个参数 `JSONArray`；在这里，我们将其作为 `[name]` 传递。

```
SimplePlugin.prototype.hello = function(name, successCallback, failureCallback) {

        PhoneGap.exec(
        successCallback, // Success Callback
        failureCallback, // Failure Callback
        'SimplePlugin',  // Registered plug-in name
        'hello', // Action
        [name] //Argument passed in
        );
        };
```

完整的 JavaScript 文件 `simpleplugin.js` 如下：

```
/**
 *
 * @return Instance of SimplePlugin
 */
var SimplePlugin = function() {

}

/**
 * @param name
 *             The name passed in
 * @paramsuccessCallback
 *             The callback that will be called when simple plugin runs
 *             successfully
 * @paramfailureCallback
 *             The callback that will be called when simple plugin
 *             fails
 */
SimplePlugin.prototype.hello = function(name, successCallback, failureCallback) {
    PhoneGap.exec(successCallback, // Success Callback
                    failureCallback, // Failure Callback
                    'SimplePlugin',  // Registered Plug-in name
                    'hello',                   // Action
                    [ name ]);        // Argument passed in
};

/**
 * <ul>
 * <li>Register the Simple Listing Javascript plugin.</li>
 * </ul>
 */
PhoneGap.addConstructor(function() {
            // Register the Javascript plug-in with PhoneGap
            PhoneGap.addPlugin('SimplePlugin', new SimplePlugin());
});
```

## 调用插件

是时候测试我们的插件了。为此，我们需要以下内容：
1.  HTML 文件
2.  PhoneGap js 文件
3.  插件 js 文件
4.  插件 Java 文件

你的 Android 项目应如图 9-5 所示。

![](img/4a75e501abc949744a790d09257a5b1e_306_0.png)

**图 9-5.** *Android PhoneGap 插件项目结构*

你的 `index.html` 文件应如下所示：

```
<!DOCTYPE HTML>
<html>
<head>
<title>PhoneGap</title>
<script type="text/javascript" charset="utf-8" src="phonegap-1.1.0.js"></script>
<script type="text/javascript" charset="utf-8" src="simpleplugin.js"></script>
<script type="text/javascript" charset="utf-8">
document.addEventListener('deviceready', function() {
var btn = document.getElementById("hello");
var textbox = document.getElementById("name");
var output = document.getElementById("output");
btn.addEventListener('click', function() {

    var text = textbox.value;

    window.plugins.SimplePlugin.hello(text,
    //success callback

    function(result) {
        output.innerHTML = result;
    }
    //failure callback,
    , function(err) {
        output.innerHTML = "Failed to invoke simple plugin";
    });
});

}, true);
</script>
</head>
<body>
    <h1>
        Simple Plugin Demo
    </h1>
    <table border="1">
        <tr>
            <td>
                Enter Name
            </td>
            <td>
                <input type="text" name="name" id="name">
                </input>
            </td>
        </tr>
        <tr>
            <td>
                <b>
                    Output:
                </b>
            </td>
            <td>
                <div id="output">
                </div>
            </td>
        </tr>
        <tr>
            <td colspan="2">
                <button id="hello">
                    Say Hello
                </button>
            </td>
        </tr>
    </table>
</body>

</html>
```

在这里你应该注意到插件是这样调用的。我们首先传递包含名称的文本，然后注册一个成功回调和一个失败回调。

```
window.plugins.SimplePlugin.hello(
    text,
    //success callback
    function (result) {
        output.innerHTML = result;
    },
    //failure callback
    function (err) {
        output.innerHTML = "Failed to invoke simple plugin";
    }
);
```

最后，当我们运行这个 Android 项目时，我们看到如图 9-6 所示的输出。

![](img/4a75e501abc949744a790d09257a5b1e_308_0.png)

**图 9–6.** PhoneGap 插件在 Android 上的输出

## 分享 Android PhoneGap 插件

就 PhoneGap 框架版本 1.1.0 而言（本书撰写时的版本），没有办法打包和分享你的插件。

分享你的插件的唯一方法是
1.  分享 Java 源文件
2.  分享 JavaScript 源文件
3.  提供说明插件使用方法的 Readme 文件

PhoneGap 插件通常上传到 https://github.com/phonegap/phonegap-plugins。如果你希望贡献你的作品，可以与 PhoneGap 团队合作，将你的插件添加到此仓库中。

# 为 iPhone 扩展 PhoneGap

PhoneGap 为 XCode 提供插件，用于创建基于 PhoneGap 的应用程序。在本书撰写时，PhoneGap 从 0.9.5 版本升级到 1.1.0。iPhone-PhoneGap 插件框架发生了一些变化。本章重点介绍 1.1.0 版本的插件开发。

安装 1.1.0 XCode 扩展的步骤：
1.  下载 PhoneGap 1.1.0 zip 文件并解压。
2.  转到 iOS 文件夹并安装 `PhoneGapInstaller.pkg`。

一旦你安装了 PhoneGap 的 1.1.0 XCode 插件，就可以从 XCode 创建一个基于 PhoneGap 的应用程序，如图 9–7 和图 9–8 所示。

![](img/4a75e501abc949744a790d09257a5b1e_309_0.png)

图 9–7. 创建新的 iOS PhoneGap 项目

www.it-ebooks.info

![](img/4a75e501abc949744a790d09257a5b1e_310_0.png)

图 9–8. *创建新的 iOS PhoneGap 项目*

按照第 3 章的步骤将 `www` 文件夹添加到项目中。现在运行项目，确保你能看到基于 iPhone PhoneGap 的应用程序。

## 声明插件的原生部分

PhoneGap 1.1.0 插件的原生部分需要添加到 `plug-ins` 文件夹中。如图 9–9 所示。

![](img/4a75e501abc949744a790d09257a5b1e_310_1.png)

图 9–9. *iPhone 插件原生部分*

在 `plug-ins` 文件夹中创建一个 Objective-C 类。让我们将这个类命名为 `SimplePlugin`。`SimplePlugin` 扩展自 `PGPlugin`。`SimplePlugin.h` 文件如下所示。



# 第九章：扩展 PhoneGap

```objc
#import <Foundation/Foundation.h>
#ifdef PHONEGAP_FRAMEWORK
#import <PhoneGap/PGPlugin.h>
#else
#import "PGPlugin.h"
#endif

@interface SimplePlugin : PGPlugin {
}
/**
 * 将 idleTimerDisable 属性设置为 true，从而禁用空闲超时
 */
- (void) hello:(NSMutableArray*)arguments withDict:(NSMutableDictionary*)options;

@end
```

这里我们声明了一个名为 "hello" 的函数，其签名如下：
- (void) hello:(NSMutableArray*)arguments withDict:(NSMutableDictionary*)options;

此函数不返回任何内容，而是接受两个参数：
1. 参数 (Arguments)
2. 选项 (Options)

传递给插件的任何参数或输入（在我们的例子中是姓名）都通过 "arguments" 传递。
现在让我们来实现 SimplePlugin 的 hello 函数。在第一个版本中，我们将从插件返回一个字符串 "hello world"。此外，我们将解释如何访问传递的参数以及如何调用成功和失败回调。
请注意，插件在 JavaScript 中的调用方式如下：

```javascript
window.plugins.SimplePlugin.hello(
    "Bob",
    //成功回调
    function(result){
        alert("插件返回了 "+result);
    },
    //失败回调，
    function(err){
        alert("调用插件时出错");
    }
);
```

以下是插件方法的框架代码。
插件可以访问输入参数，在我们的例子中是 "Bob"，从 arguments 对象中提取它。请注意，arguments 数组中的第一个对象始终是 callbackId，用于调用 JavaScript 回调函数。我们可以从索引 1 开始提取实际的参数（在我们的例子中，只有 "Bob"）。

```objective-c
NSString * name = [arguments objectAtIndex:1];
```

如果我们有另一个参数，我们将从索引 2 处访问它。

现在让我们专注于如何调用成功或失败的 JavaScript 回调函数。这始于声明 PluginResult 对象。随后，我们再声明两个对象，一个用于 callbackId（帮助我们调用回调函数），另一个是字符串，即 JavaScript 字符串，我们将把它嵌入到 HTML 页面中以实际调用回调。

```objective-c
NSString* jsString = nil;
NSString* callbackId = [arguments objectAtIndex:0];
```

现在让我们了解成功和失败条件的代码流程。这在下面的代码中展示。

如果一切顺利，我们创建一个状态为 PGCommandStatus_OK 的结果对象。然后我们根据该结果创建 jsString 对象，并传入 callbackId。最后，我们通过调用 [self writeJavascript:jsString] 来实际执行 JavaScript 以调用成功回调。

在失败的情况下，我们创建一个状态不是 PGCommandStatus_OK 的 PluginResult 对象，并为错误/失败回调创建 jsString。最后，我们使用 [self writeJavascript:jsString] 调用错误/失败回调：

```objective-c
PluginResult* result=nil;
NSString* jsString=nil;
NSString* callbackId=[arguments objectAtIndex:0];
```

```objective-c
if(success){
  result=[PluginResult resultWithStatus:PGCommandStatus_OK];
    jsString=[result toSuccessCallbackString:callbackId];
}
else{
  result=[PluginResult resultWithStatus:PGCommandStatus_ILLEGAL_ACCESS_EXCEPTION];
    jsString=[result toErrorCallbackString:callbackId];
}

[self writeJavascript:jsString];
```

如果我们想在调用成功或失败回调时传递数据，可以在创建 PluginResult 对象时传递一个额外的参数来实现。这里我们通过调用 PluginResult 的 resultWithStatus: messageAsString 函数来传递一个字符串。

```objective-c
result = [PluginResult resultWithStatus:PGCommandStatus_OK messageAsString:@"Hello World"];
```

完整的 SimplePlugin 如下所示。请注意，这里我们没有处理失败路径，因此只为成功回调创建 jsString。

```objective-c
#import "SimplePlugin.h"

@implementation SimplePlugin
- (void) hello:(NSMutableArray*)arguments withDict:(NSMutableDictionary*)options
{
    PluginResult* result = nil;
    NSString* jsString = nil;
    NSString* callbackId = [arguments objectAtIndex:0];
    NSString* name = [arguments objectAtIndex:1];
    NSDate* date = [NSDate date];
    NSDateFormatter* formatter = [[[NSDateFormatter alloc] init] autorelease];
    
    //设置所需的日期格式
    [formatter setDateFormat:@"yyyy-MM-ddhh:mm:ss"];
    
    //获取日期字符串
    NSString* dateStr = [formatter stringFromDate:date];
    
    NSString* returnStr = [NSString stringWithFormat:@"Hello %@.The time is  %@", name,dateStr];
    
    result = [PluginResult resultWithStatus:PGCommandStatus_OK messageAsString:returnStr];
    jsString = [result toSuccessCallbackString:callbackId ];
    
    [self writeJavascript:jsString];
}
@end
```

仅仅为插件创建 .h 和 .m 文件，并将它们放在插件文件夹中是不够的。我们需要在 PhoneGap 框架中注册我们的 SimplePlugin。在 Supporting Files 文件夹中的 PhoneGap.plist 文件中添加一个条目可以实现这一点。

这在图 9-10 中展示。

![图 9–10. 注册 PhoneGap 插件](img/4a75e501abc949744a790d09257a5b1e_314_0.png)

## 声明插件的 JavaScript 部分

iPhone 插件的 JavaScript 部分与你在 Android 中看到的不同。

这主要通过两个步骤完成：
1. 声明一个名为 SimplePlugin 的 JavaScript 类，并为其添加一个方法，在我们的例子中是 "hello"。在 hello 函数中，我们将 JavaScript 参数映射到 Objective Plugin 类和方法。
2. 第二部分是为 SimplePlugin 创建一个 install 方法，并通过调用 PhoneGap.addConstructor(SimplePlugin.install) 来注册 JavaScript 插件。

让我们先关注一下插件的 hello 函数。注意，我们正在插件内部调用 PhoneGap.exec 函数。

以下是 PhoneGap.exec 的签名：

```javascript
PhoneGap.exec(<<成功回调>>,<<失败回调>>,<<插件名>>,<<操作名>>,<<参数数组>>)
```

注意我们如何将 hello 函数的第一个参数 "name" 作为参数数组的一部分传递。successCallback 和 errorCallback 作为 PhoneGap.exec 函数的第一和第二个参数传递。插件类和方法名作为第三和第四个参数传递。

```javascript
SimplePlugin.prototype.hello = function(name,successCallback, errorCallback) {
    PhoneGap.exec(
        successCallback,
        errorCallback,
        "SimplePlugin",
        "hello",
        [name]);
};
```

JavaScript 部分的完整代码如下所示。

```javascript
if (!PhoneGap.hasResource("simpleplugin")) {
    PhoneGap.addResource("simpleplugin");

    /**
     * @returns powermanagement 的实例
     */

    function SimplePlugin() {};

    /**
     *
     * @param name 给定姓名后，successCallBack 将收到字符串 "Hello <name>! The time is <time>."
     * @param successCallback 成功获取唤醒锁时调用的函数
     * @param errorCallback 获取唤醒锁出现问题时调用的函数
     */
     SimplePlugin.prototype.hello = function (name, successCallback, errorCallback) {
        PhoneGap.exec(successCallback, errorCallback, "SimplePlugin", "hello", [name]);
     };


     /**
      * 向 PhoneGap 注册插件
      */
     SimplePlugin.install = function () {
        if (!window.plugins) window.plugins = {};

        window.plugins.SimplePlugin = new SimplePlugin();

        return window.plugins.SimplePlugin;
     };

     PhoneGap.addConstructor(SimplePlugin.install);
}
```

## 调用插件

为了测试插件，我们将创建一个 PhoneGap 应用程序并从那里调用插件。这部分与 Android 的实现完全相同。

你需要遵循以下步骤：
1. 包含 PhoneGap 1.1.0 js 文件。
2. 包含 simpleplugin.js 文件。
3. 注册按钮点击事件以调用插件。
4. 注册成功和失败回调以显示结果。
index.html 的完整源代码如下：

```html
<!DOCTYPE HTML>
<html>
<head>
    <title>PhoneGap</title>
    <script type="text/javascript" charset="utf-8" src="phonegap-1.1.0.js"></script>
    <script type="text/javascript" charset="utf-8" src="simpleplugin.js"></script>
    <script type="text/javascript" charset="utf-8">
        document.addEventListener('deviceready', function() {
            var btn = document.getElementById("hello");
            var textbox = document.getElementById("name");
            var output = document.getElementById("output");

            btn.addEventListener('click', function() {
                var text = textbox.value;
                window.plugins.SimplePlugin.hello(text,
                //成功回调
                function(result) {
                    output.innerHTML = result;
                }
                //失败回调,
                , function(err) {
                    output.innerHTML = "调用简单插件失败";
                });
            });
        }, true);
    </script>
</head>
<body>
    <h1>
        简单插件演示
    </h1>
    <table border="1">
        <tr>
            <td>
                输入姓名
            </td>
            <td>
                <input type="text" name="name" id="name">
                </input>
            </td>
        </tr>
    </table>
</body>
</html>
```



```
        <tr>
            <td>
                <b>
                    输出：
                </b>
            </td>
            <td>
                <div id="output">
                </div>
            </td>
        </tr>
        <tr>
            <td colspan="2">
                <button id="hello">
                    说你好
                </button>
            </td>
        </tr>
    </table>
</body>

</html>
```

当你运行 PhoneGap 示例时，你将看到如图 9-11 所示的应用程序。

![](img/4a75e501abc949744a790d09257a5b1e_318_0.png)

图 9-11. *PhoneGap 插件输出*

## 共享 iPhone PhoneGap 插件

要共享插件，你需要共享以下文件。

1.  SimplePlugin.h
2.  SimplePlugin.m
3.  simpleplugin.js

将上述文件列表添加到插件文档中。同时，请记录如何从 JavaScript 调用该插件。

## 为 BlackBerry 扩展 PhoneGap

与 Android 类似，PhoneGap 的 BlackBerry 插件也由两部分组成，分别位于 PhoneGap 框架（桥）的两侧。我们有一个原生部分（一个扩展 PhoneGap 插件的类）和一个使用 PhoneGap JavaScript 框架的 JavaScript 文件。

我们假设你使用的 BlackBerry WebWorks SDK 版本高于 1.5。

我们假设 BlackBerry WebWorks SDK 安装在 C:\BBWP，并且我们已经安装了 Java 1.6 SDK 和 Ant 并且它们在系统路径中。我们还假设我们的开发目录是 D:\PhoneGap-Plugin，并且 PhoneGap SDK 位于 D:\PhoneGap-plugin\PhoneGap-1.1.0 目录中。请参考第 3 章以回顾 BlackBerry PhoneGap 开发的系统要求。

创建和测试 BlackBerry 插件的步骤如下：

1.  创建插件 Java 文件并将其放入 PhoneGap SDK 的框架中。
2.  创建 BlackBerry PhoneGap 项目以测试插件。
3.  然后编译 BlackBerry PhoneGap 项目，以编译你放入 PhoneGap SDK 框架文件夹中的插件 Java 文件。如果存在编译错误，你需要删除在步骤 2 中创建的项目，修复 Java 文件，然后从步骤 2 重复。
4.  当插件 Java 文件无误编译通过后，你就可以放入 JavaScript 插件文件并编写 HTML 页面来使用该插件了。

### 声明插件的原生部分

BlackBerry 插件类与 Android 插件类非常相似。唯一的区别是 BlackBerry 插件类使用 PhoneGap 1.1.0 框架；因此，存在一些差异。

以下是 BlackBerry 插件类的骨架代码：

```
package com.phonegap.plugins;

import com.phonegap.api.Plugin;
import com.phonegap.api.PluginResult;

import java.util.Date;
import com.phonegap.json4j.JSONArray;

public class HelloWorldPlugin extends Plugin {

    private static final String ACTION_HELLO="hello";

    /**
     * 执行请求的操作并返回一个 PluginResult。
     *
     * @param action 要执行的操作。
     * @param callbackId 操作完成后要调用的回调 ID。
     * @param args 操作的参数 JSONArray。
     * @return 一个包含状态和消息的 PluginResult 对象。
     */
    public PluginResult execute(String action, JSONArray data, String callbackId) {
        return null;
    }

    /**
     * 当插件暂停时调用。
     */
    public void onPause() {

    }

    /**
     * 当插件恢复时调用。
     */
    public void onResume() {

    }

    /**
     * 当插件销毁时调用。
     */
    public void onDestroy() {

    }
}
```

请注意，我们将这个插件类放入的不是我们的项目区域，而是 PhoneGap SDK 区域内。图 9-12 中的截图显示了我们将此插件类复制到的位置。你可能需要创建 plugins 文件夹。

## 第 9 章：扩展 PhoneGap

![](img/4a75e501abc949744a790d09257a5b1e_321_0.png)

图 9-12. 插件的原生部分

这里的关键点是，在进行下一步之前，你需要在上述目录中有一个正确的 Java 插件类（并且能够编译）。我们将引导你完成此过程。

下一步是创建 BlackBerry WebWorks PhoneGap 项目。

```
$>D:
$>cd d:\PhoneGap-plugin\phonegap-1.1.0
$>ant create -Dproject.path=D:\PhoneGap-Plugin\BB-Plugin-Test
```

这将显示如图 9-13 所示的目录结构。

![](img/4a75e501abc949744a790d09257a5b1e_321_1.png)

图 9-13. PhoneGap BlackBerry 项目结构

现在让我们检查一下我们的插件类是否能编译。

```
$>cd D:\PhoneGap-Plugin\BB-Plugin-Test
$>ant build
```

如果上述步骤在 HelloWorldPlugin 中显示了一些编译错误，你需要

1.  修复这些编译错误。
2.  删除位于 D:\PhoneGap-Plugin\BB-Plugin-Test 的项目。
3.  使用 `ant create -Dproject.path=D:\PhoneGap-Plugin\BB-Plugin-Test` 重新创建项目。
4.  使用 "ant build" 检查编译。

既然你已经解决了编译空白 Java 插件类的问题，让我们在里面放一些代码吧。

以下是插件类的完整代码（这与 Android 插件非常相似）。我们暴露一个名为 "hello" 的操作名，并且期望一个名为 "name" 的参数。假设有人调用了操作 "hello" 并传入了名字 "Rohit"，我们返回 "Hello Rohit! The time is <当前时间>。"

```
package com.phonegap.plugins;

import com.phonegap.api.Plugin;
import com.phonegap.api.PluginResult;

import java.util.Date;
import com.phonegap.json4j.JSONArray;

public class HelloWorldPlugin extends Plugin {

    private static final String ACTION_HELLO="hello";

    /**
     * 执行请求的操作并返回一个 PluginResult。
     *
     * @param action      要执行的操作。
     * @param callbackId 操作完成后要调用的回调 ID。
     * @param args 操作的参数 JSONArray。
     * @return            一个包含状态和消息的 PluginResult 对象。
     */
    public PluginResult execute(String action, JSONArray data, String callbackId) {
        PluginResult pluginResult=null;
        if (ACTION_HELLO.equals(action)) {

            String name;
            try {
                name = data.getString(0);
                String result = "Hello " + name
                        + "! The time is "
                        + (new Date()).toString();
                pluginResult =
                        new PluginResult(PluginResult.Status.OK,
                                result);
                return pluginResult;
            } catch (Exception e) {
                pluginResult =
                        new PluginResult(PluginResult.Status.JSONEXCEPTION,
                                "missing argument name");
            }
        } else {
            pluginResult =
                new PluginResult(PluginResult.Status.INVALIDACTION,
                "Allowed actions is hello");
        }
        return pluginResult;
    }

    /**
     * 当插件暂停时调用。
     */
    public void onPause() {

    }

    /**
     * 当插件恢复时调用。
     */
    public void onResume() {

    }

    /**
     * 当插件销毁时调用。
     */
    public void onDestroy() {

    }
}
```

请注意，你必须再次将修改后的 HelloWorldPlugin.java 放入 PhoneGap 的框架中，如图 9-12 所示。你还需要使用 `ant create -Dproject.path=D:\PhoneGap-Plugin\BB-Plugin-Test` 删除并重新创建项目来测试插件。

## 声明插件的 JavaScript 部分

同样，插件的 JavaScript 部分与 Android 的 JavaScript 插件部分非常相似。在这种情况下，我们在一个函数声明中声明所有内容并调用它。

```
(function () {
    var HelloWorld = function () {
        return {
            hello: function (message, successCallback, errorCallback) {
                PhoneGap.exec(successCallback, errorCallback, 'HelloWorldPlugin',
            'hello', [message]);
        }
        };
    };
```

```
PhoneGap.addConstructor(function () {
    // 将插件添加到 window.plugins
    PhoneGap.addPlugin('simpleplugin', new HelloWorld());

    // 在原生端注册插件
    phonegap.PluginManager.addPlugin('HelloWorldPlugin',
    'com.phonegap.plugins.HelloWorldPlugin');
});
```

第一步是创建一个名为 HelloWorld 的 JavaScript 对象，并在其中声明一个名为 "hello" 的函数。此函数内部调用一个 PhoneGap 注册的服务，该服务又调用实际的原生类。

现在我们有了这个将从 HTML 调用的对象，我们需要将其注册为 PhoneGap JavaScript 插件。我们还需要将服务名 "helloworldplugin" 映射到类 "com.phonegap.plugins.HelloWorldPlugin"。所有这些都在 PhoneGap.addConstructor() 调用内完成。

我们使用 PhoneGap.addPlugin() 将 "simpleplugin" 名称映射到 JavaScript 插件对象。这会将插件暴露为 window.plugins.simpleplugin。

然后我们使用 phonegap.PluginManager.addPlugin() 将服务名映射到实际的 Java 类。

这就完成了我们创建插件 JavaScript 部分的工作。我们将把此 JavaScript 放在项目的 www 目录中。

## 调用插件

要调用插件，我们修改项目 www 目录中的 index.html 文件。

这与我们之前为 Android 和 iPhone 所做的非常相似。

以下是用于调用我们插件的代码片段：

```
window.plugins.simpleplugin.hello(
    document.getElementById("name").value,
    // 成功回调
    function (message) {
        document.getElementById("output").innerHTML = message;
    },
    // 失败回调
    function () {
        log("Call to plugin failed");
    }
);
```

与之前一样，我们提供名字；在这种情况下，名字来自一个文本类型的输入元素。然后我们提供一个成功回调和一个失败回调。在成功回调中，我们将返回值设置在 id 为 "output" 的 div 中。

以下是 index.html 页面的完整代码：
```

## A

addToFavorite() 方法，175–177，
188–189

Android

Eclipse 的 ADT 插件安装，
22–24

应用，GWT

- 构建路径，244
- 设备信息，247
- 目录结构，244，245
- Eclipse 类路径，244
- GWT PhoneGap 参考，
  247–248
- HelloWorld.java 文件，245
- PhoneGap_GWT_Helloworld.html
  ，245–247
- 项目创建，241–243

AVD 创建，24–27

构建环境

- 私有密钥库创建，
  117–118
- 私有密钥库上传，118–120
- 运行 PhoneGap 构建，120
- 自签名密钥库，117

下载与安装，19

安装，20

- Eclipse 下载，20
- SDK，20–22

项目

- 应用启动类型，43–45
- 应用设置，39，40
- 创建，28–30
- Dalvik 调试监控服务器
  (DDMS)，43
- DroidGap，34，35
- HelloWorld 应用，35–36

JavaScript 文件，31，32

原生组件安装，30

权限修改，32–34

手机设置，39

模拟器部署，37–38

未知来源，40

USB 调试，41–43

XML 目录，30

模拟器

- 账户与同步，288
- 认证密钥，290
- C2DM 插件，移动推送
  通知，288–291
- 部署，37–38
- deviceready事件回调
  函数，289
- 消息发送，290
- MobilePushPluginExampleOutput，
  289
- 推送消息，291
- REGID，289–290
- 设置选项，288
- window.plugins.C2DM.register()，
  289

SDK（参见 SDK）

Android 虚拟设备 (AVD)，24–27，
288

app.css 源代码，191

app.js 源代码

- addToFavorite () 函数，188–189
- ensureTableExists() 函数，188
- 初始化 Map 页面，185–186
- initiateFavButton() 函数，186–187
- initiateFavorites() 函数，187–188
- isFav () 函数，189

地点/商家获取详情，
184–185
removeFromFavorite () 函数，189
搜索按钮处理绑定，190–191

## B

BlackBerry
构建环境
“添加密钥”选项，124
BlackBerry 密钥，123
分发渠道，124
文件上传，124，125
要求，123
SDK 目录，124

本地开发环境
Apache ant 安装，105
bbwp.dir 属性，107
BlackBerry SDK 安装，105
目录结构，107
index.html 文件，108
J2SDK 下载，105
PhoneGap 应用创建，
105–106
project.properties 文件，107，108
签名密钥，109
模拟器，108，109
软件安装，104

PhoneGap
JavaScript 部分，320–321
原生部分，316–320
插件调用，321–324
插件创建与测试，316
插件共享，324
WebWorks SDK 版本，316

BundleIdentifier

## C

CallbackId，299
C2DM 插件，移动推送通知
Android 模拟器，288–291
C2DM.Manifest 文件，283–285
Eclipse Android 项目
配置，281
文件夹结构，282
JavaScript 部分，283
MobilePushPluginExample 项目
结构，285

修改，PhoneGap-1.1.0，
286–287
原生部分，282–283
轮询技术，279–280
推送技术，280
注册，282
发送者账户，287
注册，287

Chrome，249
云构建环境，113
Android 构建环境
私有密钥库创建，
117–118
私有密钥库上传，118–120
运行 PhoneGap 构建，120
自签名密钥库，117

Apple 证书，114

BlackBerry 构建环境
“添加密钥”选项，124
BlackBerry 密钥，123
分发渠道，124
文件上传，124，125
要求，123
SDK 目录，124

iOS 构建环境
添加密钥屏幕，122
Apple 开发者，121
开发者证书与
配置文件，122，123
iOS 密钥，121
ipa 按钮，123
钥匙串访问，122
Mac 机器，121

PhoneGap 测试版，113
PhoneGap 构建启动，125
PhoneGap 构建注册
PhoneGap 起始代码，115
私钥，116
配置文件，116
起始项目构建下载
屏幕，116
注册方式，114

com.phonegap.api.Plugin 类，299
com.phonegap.plugins.HelloWorldPlugin
类，321

## D

Dalvik 调试监控服务器 (DDMS)，43

DroidGap，34，35

## E

ensureTableExists() 函数，176，188
枚举状态，299
回调，311

## F

Facebook 认证
app_secret 密钥，277
Eclipse Android 项目配置，272
插件 JavaScript，275
SDK JavaScript，275
FaceBookPluginExample 项目结构，274–275
文件夹结构，273
好友列表，278–279
getFriendList() 函数，276–277
初始化事件，277
登录函数，276
登录屏幕，278
原生文件夹，274
PhoneGap JavaScript，275
注册，273–274

fetchDetails() 函数，173，175

Firefox，249

表单元素
controlgroup data role 和 horizontal data 类型，145–148
fieldset，141
HTML 选择框，143–144
label 和关联的 widget，141–142

## G

getFriendList() 函数，276–277

Google Web 工具包 (GWT)，231
Android 应用
构建路径，244
设备信息，247
目录结构，244，245
Eclipse 类路径，244
GWT PhoneGap 参考，247–248
HelloWorld.java 文件，245
PhoneGap_GWT_HelloworId.html，245–247
项目创建，241–243

Chrome 浏览器中的应用项目，236，239
编译，239–240
创建，233–234
延迟绑定，236
目录结构，240–241
GreetingService.java，236
GreetingServiceAsync.java，236
Phonegapavailablehandler，237–238
PhoneGap_GWT_HelloworId.gwt.xml 文件，234
PhoneGap_GWT_HelloworId.html，234–235
PhoneGap_GWT_HelloworId.java，235
PhoneGap.initializePhoneGap()，237
Phonegaptimeouthandler，237
RPC 组件，236
共享和服务器包，236

工具，232

JSNI，232

PhoneGap 0.9.4 库，232

用户界面开发，231–232

GWT PhoneGap 参考，
247–248

HelloWorld.java 文件，245

PhoneGap_GWT_HelloworId.html，
245–247

项目创建，241–243

应用项目
在 Chrome 浏览器中，236，239
编译，239–240
创建，233–234
延迟绑定，236
目录结构，240–241
GreetingService.java，236
GreetingServiceAsync.java，236
Phonegapavailablehandler，
237–238
PhoneGap_GWT_HelloworId.gwt.
xml 文件，234
PhoneGap_GWT_HelloworId.html，
234–235
PhoneGap_GWT_HelloworId.java，
235
PhoneGap.initializePhoneGap()，
237
Phonegaptimeouthandler，237
RPC 组件，236
共享和服务器包，236

工具，232

JSNI，232

PhoneGap 0.9.4 库，232

用户界面开发，
231–232

## H

helloworld.js 文件，324

helloworldplugin.java 文件，324

HTML 文件，303

## I

index.html 源代码，180–184

initiateFavButton() 函数，175，
186–187

initiateFavorites() 函数，187–188

initiateSearch() 函数，179–180

Internet Explorer，249



## 索引

- **iOS**
    - 构建环境
        - 添加密钥屏幕，122
        - Apple 开发者，121
        - 开发者证书和配置文件，122，123
        - iOS 密钥，121
        - ipa 按钮，123
        - 钥匙串访问，122
        - Mac 机器，121
    - 使用 XCode 4
        - BundleIdentifier，104
        - 设备测试，98
        - 设备版本选择，104
        - HTML 和 JavaScript，101
        - index.html 文件，103
        - Mac OS X Snow Leopard，98
        - 创建新的 PhoneGap 项目，99–101
        - 项目自定义，102
        - 示例应用程序，104
        - 模拟器，103
        - www 文件夹，102–103
        - 安装 XCode 和 PhoneGap，98
- **iPhone**
    - 创建 iOS PhoneGap 项目，306，307
    - JavaScript 部分，311–312
    - 原生部分，307–311
    - 插件，312–315
- 1.1.0 XCode 安装，306
- isFav() 函数，177–178，189

## J, K

- JavaScript Native Interface (JSNI)，232
- jQueryMobile，127
    - 缺点，192
    - 声明式 UI，134
        - data-role 属性，134–135
        - 对话框页面，136–138
            - "dialog1" 页面，137，139
        - 表单元素。参见 表单元素
        - 列表视图，148–150
        - "main" 页面，137，138
        - 多个 div，136
        - "page2" 页面，137，139
        - 页面，135，136
        - 工具栏和按钮，140，141
    - 事件处理分类，150
    - 文件夹结构，133，134
- **jQuery**
    - Ajax 调用，132
    - 跨浏览器框架，128
    - 基于 CSS 的选择器，130
    - 定义，127
    - DOM 操作，131–132
    - 基于元素的选择器，130
    - HTML 元素定位，129–130
    - 基于 ID 的选择器，130
    - 初始化过程，128–129
    - li 元素，130
    - 混合搭配选择器，130
    - "placeholder"，129
- **本地搜索**
    - 应用程序内部数据库，161
    - 绑定搜索按钮处理程序，172–173
    - 引导程序，163
    - 业务入口，收藏夹，160
    - 收藏夹详情，162
    - 加载收藏地点，178–179
    - 功能，157–158
    - 函数发起的搜索，171
    - Google Maps Places API，157，158
    - HTML 布局，167–169，171
    - initiateSearch() 函数，179–180
    - JavaScript 库，163–164
    - 布局，164–165
    - 本地业务，165–166
    - 地点/业务搜索。参见 地点/业务搜索
    - 地图上的结果，163
    - 结果，160
    - 源代码，180–191
- 普通事件，150
- 方向改变事件，153–155
- 开箱即用的主题，132
- 页面事件，156
- PhoneGap 集成，156–157
- 优点，192
- 滚动事件，155，156
- SenchaTouch，230
- 支持的平台，133
- 触摸事件，151–153
- UI 问题，127
- jsString，309

## L

### 布局，应用程序骨架

- AJAX 调用，202
- '卡片'，198
- CardLayout，198
- detailClickHandler 函数，204
- dockedItems，198
- Ext.Map，205
- 收藏夹面板，210，211
- 全屏，198
- Google 地点服务器，202–203
- 主页和星标按钮，198
- items，198
- JSON 响应，206–207
- placeDetailsPanel，207–209
- 占位符，208–209
- 结果面板代码创建，204，205
- resultDetailPanel，207
- 搜索面板，199–200
- 标签面板，201
- <tpl> 标签，203
- 工具栏按钮，199

### 本地开发环境

#### BlackBerry

- 安装 Apache ant，105
- bbwp.dir 属性，107
- 安装 BlackBerry SDK，105
- 目录结构，107
- index.html 文件，108
- 下载 J2SDK，105
- 创建 PhoneGap 应用程序，105，106
- project.properties 文件，107，108
- 签名密钥，109
- 模拟器，108，109
- 软件安装，104

#### 使用 XCode 4 的 iOS

- BundleIdentifier，104
- 设备测试，98
- 设备版本选择，104
- HTML 和 JavaScript，101
- index.html 文件，103
- Mac OS X Snow Leopard，98
- 创建新的 PhoneGap 项目，99–101
- 项目自定义，102
- 示例应用程序，104
- 模拟器，103
- www 文件夹，102–103
- 安装 XCode 和 PhoneGap，98
- PhoneGap SDK 目录结构，98

#### Symbian

- Symbian，109–112

#### webOS 应用程序

- webOS 应用程序，112–113

#### Xcode

- Xcode，98

## M, N

### 移动应用程序

- 一致的用户体验，9
- 环境碎片化
    - 开发，11
- 功能碎片化，10
- 功能，4，5
- HTML5 和 CSS3，15
- 位置感知，6
- 多团队/产品，9
- 操作系统碎片化，8

#### PhoneGap 的策略

- 浏览器，12–13
- 设备能力，14
- webviews，13

- 推送通知，7
- 单一来源策略，15，16
- 类型，2
- 用户交互，5
- Web 服务，3–4

## O

- Opera，250

## P, Q

- PGCommandStatus_OK，309

### PhoneGap

#### Android。参见 Android

#### Android 项目

- 应用程序启动类型，43–45
- 应用程序设置，39，40
- 创建，28–30
- Dalvik 调试监控服务器 (DDMS)，43
- DroidGap，34，35
- HelloWorld 应用程序，35–36
- JavaScript 文件，31，32
- 原生组件安装，30，31
- 权限修改，32–34
- 手机设置，39
- SD 卡列表，59–61
- 模拟器部署，37–38
- 未知来源，41
- USB 调试，41–43
- XML 目录，30
- 应用程序架构，18
- 蜂窝设备/Wi-Fi 网络，81–83
- 数据库，69–81
- 设备示例
    - 加速计，86–91
    - 捕获图像，相机，94–96
    - 指南针方位，91–94
    - 地理位置，83–86
- directoryEntry，63
- 模拟器，249
- 通讯录代码，55–59
- 联系人列表，54
- 通讯录 API，54
- 通讯录选项卡，52
- Ripple，Chrome（参见 Ripple）
- 设备信息，47–50
- 拨号器应用程序图标，51
- 新建联系人，52，53
- 环境，97
    - 云构建环境。参见 云构建环境
    - 本地开发环境。参见 本地开发环境
- 功能，45–46
- fileEntry，63
- fileSystem，62–63
- 框架，18
- LocalFileSystem，62
- 程序布局，63–69
- SDK 安装，27
- 教程，47

#### PhoneGap 扩展，293

- 加速计，293
- Android
    - 配置，296
    - JavaScript 部分，301–302
    - 原生部分，297–301
    - 新项目，296
    - 插件，303–306
    - 项目结构，297
- 架构，294
- BlackBerry
    - JavaScript 部分，320–321
    - 原生部分，316–320
    - 插件调用，321–324
    - 插件创建和测试，316
    - 插件共享，324
    - WebWorks SDK 版本，316
- 相机，293
- 文件系统，293
- 地理位置，293
- helloworld 插件，295
- iPhone
    - 创建 iOS PhoneGap 项目，306，307
    - JavaScript 部分，311–312
    - 原生部分，307–311
    - 插件，312–315
    - 1.1.0 XCode 安装，306
- JavaScript 代码，294
- JavaScript 的局限性，293
- 原生代码，294
- 存储服务，293
- PhoneGap js 文件，303

#### PhoneGap 插件，271

- C2DM 插件，移动推送通知
    - Android 模拟器，288–291
    - C2DM.Manifest 文件，283–285
    - Eclipse Android 项目配置，281
    - 文件夹结构，282
    - JavaScript 部分，283
    - MobilePushPluginExample 项目结构，285
- Registration Id (REGID)，289–290
- 远程调试，294
    - 架构，262
    - debug.phonegap.com
    - 安装，268–270
    - 问题，268
    - 服务器，261
    - DOM 元素
        - Android 应用程序连接，265
        - 设备信息应用程序加载，265
        - 检查，266
        - 属性更改，267，268
    - 注入，PhoneGap 应用程序，263–264
    - 设置，262–263
    - webkit webview，261
- removeFromFavorite() 函数，177，189
- Research In Motion (RIM)，250
- resultWithStatus: messageAsString 函数，309

## Ripple

- 应用程序目录，257
- 带特殊标志的 Chrome，257
- 指南针应用程序加载，257–258
- 指南针图像，255
- 启用，258
- index.html 文件，255–256
- 安装
    - 在 Chrome 上，253
    - 作为 Chrome 扩展，252
    - 从 Chrome 网上应用店，252
    - 首次启动，254
    - 主页，251
    - 基于 HTML/JavaScript 的应用程序，254
    - 右键单击选项，253
    - 单一来源策略，254
    - Mac 和 Linux，254–255
- 移动 Web，250
- Opera，250
- PhoneGap，250
- RIM，250

#### 修改，PhoneGap-1.1.0，286–287

- 原生部分，282–283
- 轮询技术，279–280
- 推送技术，280
- 注册，282
- 发送者账户，287
- 注册，287

#### Facebook 认证

- app_secret 密钥，277
- Eclipse Android 项目配置，272
- 插件 JavaScript，275
- SDK JavaScript，275
- FaceBookPluginExample 项目结构，274–275
- 文件夹结构，273
- 好友列表，278，279
- getFriendList() 函数，276–277
- 初始化事件，277
- 登录函数，276
- 登录屏幕，278
- 原生文件夹，274
- PhoneGap JavaScript，275
- 注册，273–274
- 功能，271
- JavaScript 文件，271
- 原生语言文件，271

- PhoneGap.addConstructor，311，321
- PhoneGap.exec 函数，311
- PhoneGap.plist 文件，310
- phonegap.PluginManager.addPlugin()，321
- PhoneGap 的 com.phonegap.api.Plugin 类，297

### 地点/业务搜索

- addToFavorite() 方法，175–177
- ensureTableExists() 函数，176
- fetchDetails() 函数，173，175
- initiateFavButton() 函数，175
- isFav() 函数，177–178
- removeFromFavorite() 函数，177

- 插件 Java 文件，303
- 插件 js 文件，303
- PluginResult，299



## 索引

设置，258–259
测试应用，259–261
tinyHippos，250
沃达丰，250
WAC，250
Webworks，250
WebWorks-Tablet-OS，250
Windows，254
Ripple 移动环境模拟器，257

app.js，220–230
cachedDetails，216–219
获取地点详情，213–216
获取 Google 地点结果，211–213
index.html，219–220
索引编号与动画效果，211
初始化，197–198
布局，应用骨架。参见 布局、应用骨架需求，196
PhoneGap 集成，195，196
Web 标准，194
SimplePlugin.h 文件，315
simpleplugin.js 文件，315
SimplePlugin.m 文件，315
Status.INVALID_ACTION，300
Status.INVALID_JSON，300
successCallback，311

# S, T, U

Safari，249
SDK

- Linux 安装说明，21
- Mac OSX Intel 安装说明，21–22
- Windows 安装说明，21

SenchaTouch，193

- 优势，193
- 基于浏览器的应用，193
- 目录结构，194，195
- ExtJS 公司，193
- jQueryMobile，230
- 学习曲线，194
- 本地搜索

# V, W, X, Y, Z

沃达丰，250

# Beginning PhoneGap

面向 JavaScript 和 HTML5 的
移动 Web 框架

![](img/4a75e501abc949744a790d09257a5b1e_336_0.png)

Rohit Ghatol

Yogesh Patel

Apress®

# Beginning PhoneGap: 面向 JavaScript 和 HTML5 的移动 Web 框架

版权所有 © 2012 Rohit Ghatol 与 Yogesh Patel

保留所有权利。未经版权所有者和出版商事先书面许可，不得以任何形式或任何方式（电子或机械，包括影印、录制，或通过任何信息存储或检索系统）复制或传播本作品的任何部分。

ISBN-13（平装）：978-1-4302-3903-1

ISBN-13（电子版）：978-1-4302-3904-8

本书中可能出现商标名称、徽标和图片。我们不在每个商标名称、徽标或图片出现处使用商标符号，而仅出于编辑目的和商标所有者的利益使用这些名称、徽标和图片，无意侵犯商标权。

本出版物中使用商品名、商标、服务标志和类似术语，即使未明确标识，也不应被视为对它们是否受专有权约束的意见表达。

总裁兼出版人：Paul Manning
主编：Michelle Lowman
技术评审：Dave Caolo
编辑委员会：Steve Anglin，Mark Beckner，Ewan Buckingham，Gary Cornell，Morgan Ertel，Jonathan Gennick，Jonathan Hassell，Robert Hutchinson，Michelle Lowman，James Markham，Matthew Moodie，Jeff Olson，Jeffrey Pepper，Douglas Pundick，Ben Renow-Clarke，Dominic Shakeshaft，Gwenan Spearing，Matt Wade，Tom Welsh
协调编辑：Kelly Moritz
文字编辑：Scribendi, Inc.
排版：MacPS, LLC
索引编制：SPi Global
插图：SPi Global
封面设计：Anna Ishchenko

由 Springer Science+Business Media, LLC. 在全球图书行业发行，地址：233 Spring Street, 6th Floor, New York, NY 10013。电话 1-800-SPRINGER，传真 (201) 348-4505，电子邮件 orders-ny@springer-sbm.com，或访问 www.springeronline.com。

有关翻译信息，请发送电子邮件至 rights@apress.com，或访问 www.apress.com。

Apress 和 friends of ED 书籍可批量购买，用于学术、企业或促销用途。大多数书名也提供电子书版本和许可。更多信息，请参阅我们的批量销售–电子书许可网页 www.apress.com/bulk-sales。

本书信息按“原样”分发，不作任何担保。尽管在准备本作品时已采取一切预防措施，但作者或 Apress 对任何个人或实体因本作品所含信息直接或间接造成的任何损失或损害概不负责。

作者在本文中引用的任何源代码或其他补充材料，读者均可在 www.apress.com 获取。有关如何定位书籍源代码的详细信息，请访问 http://www.apress.com/source-code/。

www.it-ebooks.info

> *本书献给全世界无数辛勤工作的开发者，他们共同致力于将 HTML5/JavaScript/CSS 打造为开发应用的新标准。*

> 我要感谢我的妻子 Manija Ghatol 所展现的耐心，以及我的父母 S.G Ghatol 和 Manda Ghatol 的宽容。在撰写本书期间，我疏忽了对他们的责任。我很幸运能有一个理解并支持我理想的家庭。同时，我要感谢我的朋友兼同事 Yogesh Patel 及时的援助，他不仅是一位技术天才，更是一位出色的人。

— Rohit Ghatol

> *献给我的妻子 Smita，她一直陪伴着我。没有你，我无法达到今天的成就。*

> *我要感谢 Rohit 在我职业和个人生活中给予的巨大支持；你是我遇到过最鼓舞人心的人之一。*

— Yogesh Patel

# 目录

- **速览目录** iv
- **关于作者** ix
- **关于技术评审** x
- **致谢** xi
- **引言** xii

## 第 1 章：理解跨平台移动应用开发

- 移动应用类型 2
- 理解 Web 服务 3
- 移动应用概述 4
  - 移动应用特性 4
  - 用户交互 5
  - 位置感知 6
  - 推送通知 7
- 跨平台移动应用开发的挑战 7
  - 操作系统碎片化 8
  - 多团队/产品 9
  - 一致的用户体验 9
  - 功能碎片化 10
  - 开发环境碎片化 11
- PhoneGap 的跨平台移动应用策略 12
  - 浏览器组件作为公共平台 12
  - 移动应用 Webviews 13
  - 用于暴露设备能力的原生钩子 14
  - HTML5 和 CSS3：编写应用的标准 15
  - 同源策略不适用 15
  - 结论 16

## 第 2 章：PhoneGap 入门

- PhoneGap 架构 18
- 在 Android 上设置环境 19
  - PhoneGap Android 项目所需安装 20
  - 创建新项目 28



# 目录

-   编写 HelloWorld 应用程序 35
    -   部署到模拟器 37
    -   部署到设备 38
    -   探索 PhoneGap 特性 45
    -   PhoneGap 教程 47
    -   模拟器示例 47
    -   设备示例 83

## 第3章：设置环境 97

-   本地开发环境 97
    -   前置步骤 98
    -   下载 PhoneGap 98
    -   使用 Xcode 4 设置 iOS 环境 98
    -   设置 BlackBerry 环境 104
    -   设置 Symbian 环境 109
    -   设置 webOS 环境 112
    -   使用 PhoneGap Build 的云构建环境 113
        -   注册 PhoneGap Build 113
        -   通过 PhoneGap Build 注册您的应用 114
    -   搭建 Android 构建环境 117
    -   搭建 iOS 构建环境 121
    -   搭建 BlackBerry 构建环境 123
    -   启动 PhoneGap Build 125
    -   结论 125

## 第4章：将 PhoneGap 与 jQuery Mobile 结合使用 127

-   了解 jQuery 128
    -   jQuery 初始化 128
    -   jQuery 选择器 129
    -   jQuery DOM 操作 131
    -   jQuery Ajax 调用 132
-   了解 jQueryMobile 132
    -   在移动应用中包含 jQueryMobile 133
    -   jQueryMobile 声明式 UI 134
    -   页面与对话框 134
    -   工具栏与按钮 140
    -   表单元素 141
    -   列表视图 148
    -   jQueryMobile 事件处理 150
        -   普通事件 150
        -   触摸事件 151
        -   屏幕方向变化事件 153
        -   滚动事件 155
        -   页面事件 156
-   PhoneGap 与 jQueryMobile 集成 156
    -   使用 jQueryMobile 和 PhoneGap 实现本地搜索 157
    -   初始化 PhoneGap 和 jQuery 163
    -   安装必要的 JavaScript 库 163
    -   本地搜索的布局 164
    -   搜索本地商家 165
    -   HTML 中的整体布局 167
    -   获取并显示搜索结果 171
    -   显示地点/商家详情 173
    -   将地点/商家添加到收藏及从收藏中移除 175
    -   加载您的收藏地点 178
    -   在地图上显示搜索结果 179
    -   完整源代码 180
    -   jQueryMobile 的优点 192
    -   jQueryMobile 的缺点 192
    -   结论 192

## 第5章：将 PhoneGap 与 Sencha Touch 结合使用 193

-   为何使用 Sencha Touch？ 193
    -   Sencha Touch 的优点 194
    -   Sencha Touch 的缺点 194
-   下载 Sencha Touch 194
-   将 Sencha 与 PhoneGap 集成 195
-   使用 Sencha Touch 构建本地搜索应用 196
    -   初始化 Sencha Touch 197
    -   创建布局（应用骨架） 198
    -   在面板之间切换 211
    -   获取地点列表 211
    -   获取地点详情 213
    -   从数据库存储和检索收藏地点 216
    -   结论 230

## 第6章：将 PhoneGap 与 GWT 结合使用 231

-   为何使用 GWT 进行用户界面开发？ 231
-   了解 GWT PhoneGap 232
-   构建 PhoneGap GWT 应用程序 232
    -   构建 GWT 应用程序 232
    -   构建 PhoneGap Android 应用程序 241
    -   GWT PhoneGap 参考 247

## 第7章：PhoneGap 模拟器与远程调试 249

-   简介 249
-   适用于 Chrome 的 PhoneGap 模拟器 – 使用 Ripple 250
    -   安装 Ripple 250
    -   高效使用 Chrome 进行 PhoneGap 开发 254
    -   使用 Ripple 255
    -   为 Ripple 优化您的应用 255
    -   使用特殊标志启动 Chrome 257
    -   在 Chrome 中加载应用 257
    -   启用 Ripple 258
    -   操作 Ripple 设置 258
    -   使用 Ripple 测试应用 259
-   远程调试 – http://debug.phonegap.com 261
    -   设置远程调试 262
    -   在 PhoneGap 应用中注入远程调试 263



# 目录

-   调试和修改DOM元素 264
-   debug.phonegap.com 存在的问题 268
-   安装本地 debug.phonegap.com 268
-   总结 270

## 第八章：使用PhoneGap插件

-   什么是PhoneGap插件？ 271
-   Facebook身份验证与获取好友列表 272
    -   为Android设置环境 272
    -   初始化Facebook-Connect插件 275
-   用于向PhoneGap推送移动通知的C2DM插件 279
    -   为Android设置环境 280
    -   为PhoneGap-1.1.0修改插件 286
    -   注册C2DM服务 287
    -   在PhoneGap中使用C2DM发送者账户 287
    -   支持C2DM服务的Android模拟器 288
-   总结 291

## 第九章：扩展PhoneGap

-   JavaScript的局限性 293
-   解决方案 294
-   架构 294
-   适用范围 294
-   为Android扩展PhoneGap 295
    -   声明插件的本地部分 297
    -   声明插件的JavaScript部分 301
    -   调用插件 303
    -   分享Android PhoneGap插件 305
-   为iPhone扩展PhoneGap 306
    -   声明插件的本地部分 307
    -   声明插件的JavaScript部分 311
    -   调用插件 312
    -   分享iPhone PhoneGap插件 315
-   为BlackBerry扩展PhoneGap 316
    -   声明插件的本地部分 316
    -   声明插件的JavaScript部分 320
    -   调用插件 321
    -   分享BlackBerry PhoneGap插件 324
-   总结 324

## 索引

## 关于作者

**罗希特·加托尔 (Rohit Ghatol)** 从内心来说是一位技术布道者。他喜欢尝试新技术，并围绕它们编织未来的愿景。他目前担任QuickOffice和Synerzip的架构师。罗希特拥有超过10年的经验，是印度包括Indic Threads、SaltMarch和CSI在内的多个平台上的常客技术演讲者。他自己运营着meetup上的一个名为TechNext的平台。罗希特曾是谷歌员工，曾在OpenSocial团队工作过一段时间。

**约格什·帕特尔 (Yogesh Patel)** 是一位经验丰富的开发者，在过去8年里一直在构建基于Web 2.0的应用程序。他的专长在于JavaScript和GWT方面的可用性与Web 2.0技术，并且是JavaScript和基于GWT技术的企业培训师。约格什目前担任FuelQuest Inc.和Synerzip India的项目主管和可用性专家，他积极参与开发基于PhoneGap的移动应用，并支持云端推送功能。

## 关于技术审阅者

**贾科莫·巴利 (Giacomo Balli)** 是一位iOS领域的创业者和自由开发者，其应用在App Store上取得了成功。他是HTML5/CSS3/AJAX现代Web应用技术的专家，也是webkit的活跃审查者，与苹果公司合作。贾科莫喜欢研究新概念，并为常见问题寻找简单的解决方案。从PhoneGap多平台开发的最初阶段起，他就对其有了深入的接触。

**马库斯·洛伊特维勒 (Markus Leutwyler)** 是一位居住在瑞士的Web和移动开发者。他对许多基于Web的技术感兴趣，并认为PhoneGap是创建通用移动应用程序的最佳解决方案之一。

**尼克·麦克劳德 (Nick McCloud)** 从Commodore PET计算机起步，此后几乎用各种编程语言为各种台式计算机编程。他的经验可追溯到万维网出现之前，并对利用Web技术为小型企业提供竞争优势产生了浓厚兴趣。利用PhoneGap，尼克已经为客户开发了多个跨设备应用程序。

## 致谢

撰写一本书可能是一项重大的责任，当我开始时，这个想法既让我兴奋，也让我害怕。没有各位人士的帮助与善意，这本书就不可能问世。Apress团队让这项任务变得容易。举例来说：凯利·莫里茨 (Kelly Moritz) 帮我很好地理解了整个流程，让事情变得更容易；我从理查德·卡里 (Richard Carey) 和所有技术审阅者那里得到了出色而及时的建议。如果没有这些人的协作，这几乎是不可能完成的。我收录了丹尼尔·库尔卡 (Daniel Kurka) 的PhoneGap GWT库，我想感谢他的工作以及他在帮助我理解该库方面所给予的帮助。另外，约格什·帕特尔 (Yogesh Patel) 想要感谢他的实习生奥马尔·埃克博特 (Omkar Ekbote)，他帮助开发和测试了插件源代码。
最后，我想感谢我的同事尼克希尔·瓦尔韦卡 (Nikhil Walvekar) 的支持，他是一位兼具开发者和摄影专家身份的人，帮助我处理了书中的一些图片。

—罗希特·加托尔 (Rohit Ghatol)
