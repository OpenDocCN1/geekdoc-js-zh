# HTML5 和 JavaScript Windows 8 应用实战





























Greg Weinberg

Neil Rowe

Mark Frankel

Kristy Hart

Betsy Harris

Tim Wright

Williams Woods


Jeff Burto

Cindy Teeters

Mark Shira

Gloria Schurick





引言 1

## 1 构建 Windows Store 应用程序 5
- 什么是 Windows Store 应用程序？5
- 微软设计风格原则 6
- Windows Store 应用程序的常见特性 8
- 创建你的第一个 Windows Store 应用程序 13
- 创建 Visual Studio 项目 13
- 声明应用能力 15
- 创建 HTML 页面 16
- 创建样式表 17
- 创建 JavaScript 文件 18
- 运行应用程序20
- Windows Store 应用程序的元素 20
- JavaScript 21
- HTML5 21
- 级联样式表 (CSS) 3 22
- Windows Runtime 22
- JavaScript 的 Windows 库 23
- jQuery 怎么样？23
- 使用 Visual Studio 构建 Windows Store 应用程序 26
- Windows Store 应用程序项目模板 26
- 运行 Windows Store 应用程序 34
- 调试 Windows Store 应用程序 35
- 使用 Visual Studio JavaScript 控制台窗口 35
- 设置断点 37
- 使用 DOM 资源管理器 37
- 发布到 Windows Store 38
- 注册 Windows 开发者 38
- 提交你的应用程序 39
- 通过应用认证 41
- 总结 42

## 2 WinJS 基础知识 45
- 命名空间、模块和类 45
- 使用命名空间 46
- 使用模块 48
- 类 51

### 异步异步编程 56
- 使用 Promise 57
- then() 与 done() 58
- 创建 Promise 60
- 超时 61
- 取消 Promise 62
- 组合 Promise 63
- 使用 DOM 资源管理器获取 Promise 64
- 使用 WinJS.Utilities.query() 方法获取 Promise 66
- 使用 WinJS.Utilities.id() 方法获取 Promise 67
- 使用 WinJS.Utilities.children() 方法获取 Promise 68
- 使用 Collection 69
- 使用 Ajax 调用 72
- 定义类型 73
- XMLHttpRequest 对象 74
- 总结 75

## 3 观察者、绑定和模板 77
- 理解观察者 77
- 创建观察者 78
- 监听器 79
- 合并通知 81
- 消除 82
- 使用 WinJS.Collection 获取观察者 83
- 创建观察者 86
- 声明式数据绑定 86
- 声明式数据绑定 89
- 获取 HTML 中的观察者 91
- 声明式数据绑定和 WinJS 94
- 声明式数据绑定 96
- 理解模板 100
- 创建声明式模板 100
- 创建命令式模板 103
- 使用选择器创建模板 104
- 创建模板 106
- 总结 108

## 4 使用 WinJS 控件 109
- WinJS 控件简介 109
- 声明式地使用 WinJS 控件 111
- 命令式地使用 WinJS 控件 113

## 使用 HTML5 和 JavaScript 的 Windows 8 应用程序

- 设置控件 14
- 从文档获取控件 15
- 使用 Tooltip 控件 16
- content 属性 17
- 样式 Tooltip 17
- 使用 ToggleSwitch 控件 18
- 获取 ToggleSwitch 状态 18
- 使用 Rating 控件 120
- 自定义评分 121
- 提交评分 121
- 使用 DatePicker 控件 123
- 格式化年份、月份和日期 124
- 仅显示年份、月份或日期 126
- 获取所选日期 127
- 使用 TimePicker 控件 128
- 获取和设置当前时间 130
- 格式化小时、分钟和周期 131
- 使用 FlipView 控件 132
- 显示页码 135
- 创建自定义 FlipView 按钮 137

总结 139

## 5 创建表单 141
- 使用 HTML5 表单验证 141
- 使用 required 属性 142
- 使用 pattern 属性 142
- 执行自定义验证 143
- 自定义验证错误样式 144
- 重置表单 146
- 使用 HTML5 输入元素 147
- 标记表单字段 148
- 输入数字 149
- 从范围输入值 151
- 输入电子邮件地址、URL、电话号码 151
- 以及搜索词 151
- 从列表输入值 153
- 选择文件 154

- 创建富文本编辑器 155
显示进度 156
总结 158






## 6 菜单和飞出控件 161

- 使用 Flyout Control 161
- 使用 Menu Control 163
- 使用 AppBar Control 167
- 创建简单的 App Bar 168
- 使用 App Bar 命令 170
- 显示上下文命令 173
- 配置应用设置 175
- 创建“关于”页面设置 176
- 创建个人设置 178
- 显示窗口对话框 182
- 总结 184

## 7 使用 ListView Control 185

- ListView Control 简介 185
- 使用列表布局对比网格布局 190
- 防止 ListView 项目重叠 193
- 在 ListView Control 中选择项目 197
- 创建主/详细视图 198
- 选择多个项目 202
- 在 ListView Control 中排序项目 204
- 在 ListView Control 中过滤项目 206
- 在 ListView Control 中分组项目 208
- 使用语义缩放切换视图 211
- 动态切换到 ListView 模板 216
- 增量加载 ListView 项目 219
- 总结 221

## 8 创建数据源 223

- 创建自定义数据源 223
- 创建数据源类 224
- 创建数据适配器 224
- 实现 getCount() 方法 225
- 实现 itemsFromIndex() 方法 225
- 实现 insertAtEnd() 方法 227
- 实现 remove() 方法 227
- 实现 change() 方法 228
- 处理错误 228
- 实现 setNotificationHandler() 方法 229
- 创建文件数据源 230
- 使用文件数据源 231

# 使用 HTML5 和 JavaScript 释放 Windows 8 应用

- 创建 Web 服务数据源 ................................... 236
- 创建数据源 ..................................................... 236
- 创建 Web 服务 ....................................................... 237
- 使用 Web 服务数据源 ....................................... 240
- 创建 IndexedDB 数据源 ........................................ 241
- IndexedDB 概述 ............................................................ 241
- 使用 IndexedDB 数据源 ........................................ 245
- 总结 ................................................................................ 252

- 9 应用事件和状态 .................................................... 253
- 应用事件 ............................................................ 253
- 处理 Activated 事件 ................................................ 254
- 处理 Error 事件 ....................................................... 255
- 使用 Promises 延迟事件 ........................................ 256
- 创建自定义事件 ....................................................... 257
- 挂起、终止和恢复应用 ................... 257
- 检测应用何时挂起和终止 ... 258
- 检测之前的执行状态 ................................ 258
- 使用 Visual Studio 测试应用状态 ............... 259
- 使用 Session State 存储状态 ........................................ 260
- 应用视图状态 ................................................. 261
- 靠上、全屏、竖屏和横屏 ................................ 261
- 使用媒体查询 ........................................................ 264
- 使用 JavaScript mediaMatch 方法 ................................ 266
- 定义视口 ........................................................ 267
- 总结 ................................................................................ 270

- 10 页面片段和导航 ................................... 273
- 使用 HtmlControl  ........................................ 273
- 创建页面控件 ................................................... 276
- 创建多页应用 ................................................... 280
- 创建导航应用 ............................................ 280
- 理解导航应用的默认 default.html 页面 ... 281
- 在导航应用中添加新的页面控件 283
- 导航到另一个页面 ........................................ 285
- 理解导航 API ................................... 286
- 理解 PageControlNavigator  ... 287
- 理解导航状态 ................................ 287
- 总结 ................................................................................ 291

## 11 使用 Live Connect API 293

- 安装 Live SDK 294
- 添加 Live SDK 引用 294
- 注册你的应用 294
- 初始化 Live Connect SDK 296
- 指定不同的作用域 296
- 验证用户身份 299
- 使用 WL.login() 299
- 使用 SignIn Control 300
- 身份验证事件 302
- 将身份令牌传递给 Web 服务 303
- 从 Windows Store 应用 发送身份令牌 303
- 在 Web 服务中验证身份令牌 306
- 获取用户 ID 308
- 获取基本用户信息 309
- 从 SkyDrive 上传和下载文件 311
- 列出 SkyDrive 文件夹和文件 312
- 从 SkyDrive 下载文件 314
- 上传文件到 SkyDrive 316
- 总结 318

## 12 图形与游戏 319

- 游戏概述 320
- 创建游戏 Tile 321
- 播放游戏声音 322
- 创建游戏画布 323
- 捕获用户交互 325
- 创建更新循环 327
- 创建渲染循环 329
- 总结 331


## 关于作者

Stephen 曾是微软的高级经理，现在经营自己的咨询公司。他在麻省理工学院获得博士学位，并提供构建 Windows 8 应用的培训。

## 献辞

本书献我的妻子 Ada。

## 致谢

我要感谢我的编辑 Neil Rowe 为本书提供的帮助。我也想感谢 Ruth 的支持。最后，我要感谢我的编辑 Jeff Burtoft 在这个项目中付出的努力。

## 我们想听听你的意见！

作为本书的读者，你是我们最重要的评论家和反馈者。我们重视你的意见，并想知道我们哪些做得是正确的，哪些可以做得更好，以及你希望在未来的书中看到的领域。


Indianapolis, IN 4624
## 读者服务

访问我们的网站并在 sams.com/register 注册本书，以便获取任何可能的更新、下载或错误说明。

## 引言

如果你想构建一个软件应用程序并接触最大的客户市场并赚取最多的钱，那么构建 Windows 8 应用是有意义的。

Microsoft Windows 是世界上最流行的操作系统。Windows 占据了 90% 以上的操作系统市场。截至 2012 年 6 月，Windows 7 的许可证已售超过 6 亿份。





# 商店

焦点聚焦

游戏 >

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_15_0.png)

图 I.1

本书完全介绍如何构建你可以在 Windows 商店中销售的 Windows Store 应用。特别是，你将学习如何使用 JavaScript 和 HTML5 来构建 Windows Store 应用。

为什么选择 JavaScript 和 HTML5？你可以使用 C#、XAML 或 C++ 等其他技术来构建 Windows Store 应用，但本书专门关注于使用 JavaScript 和 HTML5 构建 Windows Store 应用。

使用 JavaScript 和 HTML5 构建 Windows Store 应用的优势在于，你可以利用现有的网站构建技能来开发 Windows 应用程序。如果你已经熟练使用 JavaScript、HTML 和层级样式表（CSS）进行编程，那么你会发现构建 Windows Store 应用非常易 way。

本书涵盖了构建 Windows Store 应用所需的所有内容。你将学习如何使用 JavaScript Windows 库（WinJS）来创建 Windows Store 应用。特别是，你将学习如何使用 WinJS 控件，例如 Rating（评分）、Menu（菜单）和 ListView（列表视图）控件。

你还将学习如何处理 Windows Runtime（Windows 运行时）。通过利用 Windows Runtime，你可以访问 Windows 8 功能，实现在纯 Web 应用中无法实现的操作，例如捕捉视频和声音。

读完本书后，你将理解如何创建效率应用和游戏等 Windows Store 应用。例如，在第 7 章和第 8 章中，你将学习如何使用 ListView 控件创建一个简单的任务列表应用。在第 12 章中，你将学习如何创建一个简单的街机游戏——“大脑噬者”（Brain Eaters）。

阅读这本书，构建一个 Windows Store 应用，卖出很多副本，然后买架喷气飞机。

# 本书的准备工作

如果你可以使用 JavaScript、HTML 和层级样式表构建网站，那么已经了阅读和理解本书所需的技能。

构建 Windows Store 应用以及使用本书中的代码有两个软件方面的要求。

首先，你必须在 Windows 8 操作系统上构建 Windows Store 应用。让我重复一遍：你必须在电脑上安装了 Windows 8 才能使用本书中的代码。

其次，为了使用本书中的代码，你需要 Microsoft Visual Studio 2012。Visual Studio 2012 有一个免费版本——适用于 Windows 8 的 Microsoft Visual Studio 2012 Express，你可以从 Microsoft.com 网站下载。

> 注意
在纸质书中，偶尔当某一行代码太长无法适应页面宽度时，会插入代码延续接符 ➥ 来标记续接。

# 源代码

与本书相关的所有源代码都可以从 GitHub 下载：https://github.com/StephenWalther/Windows8AppsUnleashed

点击 Downloads 链接以 ZIP 文件格式下载最新版本的代码。

# 第 1 章

# 构建 Windows Store 应用

## 什么是 Windows Store 应用？

在本章中，我将向你介绍构建 Windows Store 应用的基础知识。我首先会解释 Windows Store 应用与传统的 Windows 桌面应用程序有什么不同。你将学习让一个 Windows Store 应用成为 Windows Store 应用的关键。

带着无畏和勇敢，并希望你也能感到无畏勇敢，我将引导你构建自己的 Windows Store 应用。你将学习如何利用 Microsoft Visual Studio 2012 的功能来构建、运行和调试 Windows Store 应用。

- 什么是 Windows Store 应用？
- 创建你的第一个 Windows Store 应用
- Windows Store 应用的元素
- 调试 Windows Store 应用
- 发布到 Windows 商店

接下来，我们将深入讨论 Windows Store 应用的基础元素。你将学习 Windows Store 应用是如何由 HTML5、JavaScript、JavaScript Windows 库和 Windows Runtime 构筑而成的。

最后，我们进入关于钱的部分。我将解释如何将你的 Windows Store 应用发布到 Windows 商店并开始赚取美元。

## 什么是 Windows Store 应用？

我仍然记得第一次使用 iPhone 的时候。当你在 iPhone 上滑动屏幕时，屏幕实际上会产生回弹效果！当你把邮件移到垃圾桶时，邮件会卡在垃圾桶里！这就像是 iPhone 内部有一个微型宇宙，并且它遵循我们的物理定律。

出于某种原因——我尚未探索且并不完全理解——这种我的 iPhone 内部存在第二个宇宙的错觉让我感到很快乐。它让与 iPhone 的交互变得充满趣味。

现在我们来看 Windows。除了 Windows 纸牌游戏里那个跳动的卡片，我想不起 Windows 中还有什么什么东西曾创造过同样的乐趣。我不记得上一次 Windows 让我大笑或带来快乐是什么时候了。通过 Windows Store 应用，微软终于承认了用户体验至关重要——而且是非常重要。Windows Store 应用的核心是一组被称为“微软设计风格原则”的用户体验设计原则。通过拥抱微软设计风格原则，你可以创建看起来更有活力且更易于使用的 Windows Store 应用。

## 微软设计风格原则

微软设计风格原则是微软在构建 Windows Phone、Xbox Live 以及（已停产的）Zune 背景下开发的一套用户体验设计原则。你也会在微软网站（如 Microsoft SkyDrive 和 Windows Azure Portal）上看到微软设计原则的应用。准备好了，它们是：

1. 对卓越工艺的自豪。
- 投入时间和精力在那些他人经常看到的细节上。

2. 少事多得。
- 解决干扰问题，专注于内容。
- 通过移除不必要的元素创建简洁的体验。

3. 快速且流畅。
- 快速、流畅地响应操作。
- 通过有意义的动画赋予体验生命。

4. 真正的数字化。
- 接受我们正在使用屏幕这一事实。
- 使用鲜艳的色彩和图像进行设计。

5. 共赢。
- 利用生态系统，并在应用和设备之间进行协作。
- 符合 UI 模型以减少冗余并提供熟悉感。





### Windows Store 应用的共同特性

Windows Store 应用是遵循微软设计风格原则的应用程序。此外，Windows Store 应用设计用于在 Windows 8 或 Windows RT 系统上运行。

所有 Windows Store 应用都有一组共同的特性。让我通过 Windows 8 版本的 Internet Explorer 的背景来向大家解释这些特性。

### 支持键盘、鼠标、触摸和手控笔

Windows Store 应用最显著的特征之一是其超大的磁贴和按钮，以及对留白的大量使用。所有这些 UI 响应式设计使得 Windows Store 应用对手指非常友好。

Windows Store 应用的设计旨在确保它们在仅限触摸的平板电脑和在带有键盘和鼠标的台式电脑上使用时都能同样运行。Windows Store 应用的设计目标是易于抓取的。

Windows 8 工作方式的优之处在于，作为开发者，你不需要花费大量精力去支持触摸。只要你坚持使用标准的 WinJS 控件，就可以免费获得键盘支持。

## 使用应用栏和导航栏

图 1.1 包含了 Windows 8 版本的 Internet Explorer 截图，此时打开了《纽约时报》的首页。请，你看到的唯一内容是《纽约时报》的内容。没有工具栏，也没有状态栏。


图 1.1 Windows 8 Internet Explorer

## 什么是 Windows Store 应用？

在 Windows Store 应用中，你将所有命令都隐藏在应用栏中。只有当你从屏幕底部或顶部滑动，或者右键点击屏幕时，应用栏才会出现。

Internet Explorer 的应用栏包含地址栏以及返回按钮和刷新按钮等按钮（见图 1.2）。


图 1.2 使用应用栏和导航栏

注意图 1.2，屏幕顶部还有另一个栏。这条栏被称为导航栏（nav bar），你用它进行导航。在 Internet Explorer 中，导航栏包含你所有浏览器标签页的缩略图。

## 使用实用功能（Charms）

如果你从屏幕右边缘滑动或将鼠标移动到右角，或者按下组合键 Win+c，实用功能面板就会显示（见图 1.3）。

# 第 1 章 构建 Windows Store 应用


图 1.3 查看实用功能

以下是标准实用功能的列表：

- 搜索—允许你在当前应用和其他应用中搜索内容。
- 共享—允许你与其他应用共享当前应用中的内容。
- 开始—将你导航到“开始屏幕。
- 设备—允许你连接到设备。
- 设置—允许你配置应用设置和系统设置。

这些实用功能为你提供了放置常用应用程序功能的标准位置。例如，所有 Windows Store 应用的设置都应该出现在“设置”实用功能面板中（见图 1.4）。这使得用户能够更容易找到你的设置。

## 什么是 Windows Store 应用？


图 1.4 设置实用功能面板

当你构建 Windows Store 应用时，你不需要构建自己的设置菜单。相反，你通过自定义应用设置来扩展实用功能面板。我将在第 6 章“菜单和弹出窗口”中讨论此操作的细节。

**全屏、并接和填充**

Windows Store 应用可以处于三种不同的视图状态：全屏（Full screen）、并接（snapped）和填充（filled）。默认状态是全屏——应用程序占据所有可用的屏幕空间。

你可以通过按下组合键 Win+(句号)，或从屏幕顶边缘滑动到左边缘，或者移动到左上角并向下拖动，在不同的视图状态之间切换。

> **警告**
> 你只能在水平分辨率为 1366 像素或更高的 Windows 设备上切换到“并接”状态。否则，没有足够的屏幕空间同时查看超过一个应用。

图 1.5 显示了屏幕上同时运行的两个 Windows 8 应用。天气应用处于“并接”状态，Internet Explorer 应用处于“填充”状态。并接的应用水平分辨率始终为 320 像素。填充的应用占据了剩余的屏幕空间。

# 第 1 章 构建 Windows Store 应用


图 1.5 并接和填充的应用

在构建 Windows Store 应用时，你需要设计应用使其能够在全屏、并接或填充状态下工作。在任何时刻，应用程序的水平分辨率都可能发生剧变。我将在第 9 章“应用事件和状态”中讨论如何处理不同视图状态之间的切换。

## 关闭 Windows Store 应用

现在通过将光标移动到屏幕右上角的 x 来关闭 Windows Store 应用。哈！

## 创建你的 Windows Store 应用

让我们无畏些。在这一部分，我将引导你构建你的第一个应用。

> **注意**
> 完成的应用代码可以在“第一个 Windows Store 应用”章节找到。


图 1.6 你的应用

### 创建 Visual Studio 项目

第一步是创建 Visual Studio 项目。我使用 Visual Studio 2012 创建了书中几乎所有的代码。在大多数情况下，我使用的是 Visual Studio 的免费版本——适用于 Windows 8 的 Studio 2012 Express——你可以从 Microsoft.com 下载。

> **注意**
> 在创建 Web 服务项目的章节，我使用了 Visual Studio Professional 2012，因为需要在同一个解决方案中创建一个 Windows Store 应用和一个 ASP.NET 项目。

# 第 1 章 构建 Windows Store 应用

> **注意**
> 你可以使用 Studio 2012 或 Microsoft Blend 创建 Windows Store 应用。如果你需要发布到 Windows Store，我建议使用 Visual Studio 2012。
为了构建 Windows Store 应用，你必须在 Windows 8 上使用 Visual Studio。如果你没有专门的 Windows 8 电脑，可以使用 VMware Player 等虚拟机 Windows 8。

启动 Visual Studio。接下来，选择菜单文件、新建项目。在新建项目对话框的左侧，选择 JavaScript 并选择空白应用模板。为你的项目输入名称 App1 并点击确定 按钮（见图 1.7）。


图 1.7 使用 Visual Studio 新建项目对话框

创建项目后，你可以在解决方案管理器窗口中看到项目的所有文件（图 1.8）。当你创建一个新的 Windows Store 应用时，你会得到一个 default.html 文件（在项目根目录下）、一个 default.js 文件（在 js 文件夹中）以及一个 default.css 文件（在 css 文件夹中）。这三个文件是你的应用的起点。


图 1.8 Windows Store 应用默认文件





## 声明应用能力

在我们开始编写代码之前，还有另一件事必须先完成。我们正在构建一个可以拍照的应用。这听起来有点吓。理论上，应用可以在你不知情的情况下拍摄你的照片，并将照片发送给潜伏在互联网上的恶意黑客（或者坐在微软办公桌背后的 Steve Ballmer）。

当你的应用执行某些危险操作时，你必须提前声明你的应用将执行此类操作，以便用户能够同意。你可以在应用程序清单文件（manifest file）中声明应用的能力。你可以通过双击解决方案窗口中的 `package.appmanifest` 文件来打开应用清单的编辑器。

点击“Capabilities”（能力）选项卡以查看应用程序的所有声明能力。例如，如果你希望你的应用能够从计算机麦克风录音，你需要选择“Microphone”（麦克风）能力；如果你希望应用能够将新照片保存到用户的“图片”库中，你需要选择“Pictures Library”（图片库）能力。对于我们的应用，我们需要启用“Webcam”（摄像头）能力以便拍照（图 1.9）。

| 应用 UI | 能力 (Capabilities) | 声明 (Declarations) |
| --- | --- | --- |
| 使用此页指定应用可以使用的系统功能或设备 | | |
| 能力: | 描述: | |
| [ ] Documents Library (文档库) | 提供对连接摄像头的访问 更多信息 |
| [ ] Enterprise Authentication (企业身份) | | |
| [x] Internet (Client) (互联网（客户端)) | | |
| [ ] Internet (Client & Server) (互联网（客户端与服务器)) | | |
| [ ] Location (位置) | | |
| [ ] Microphone (麦克风) | | |
| [ ] Music Library (音乐库) | | |
| [ ] Pictures Library (图片库) | | |
| [ ] Private Networks (Client & Server) (私有网络（客户端与服务器)) | | |
| [ ] Proximity (距离) | | |
| [ ] Removable Storage (可移动存储) | | |
| [ ] Shared User Certificates (共享用户证书) | | |
| [ ] Videos Library (视频库) | | |
| [x] Webcam (摄像头) | | |

图 1.9 启用拍照能力

当用户首次运行我们的应用时，用户需要同意允许应用访问摄像头（见图 1.10）。用户只需要同意一次。


图 1.10 请求访问您摄像头的许可

> 注意
在用户同意后，用户可以使用 Settings（设置）小抽屉下的 Permissions（权限）设置来拒绝应用使用某个特定能力的权限。

## 创建 HTML 页面

当你创建一个 Windows Store 应用时，你会在应用程序的根目录下得到一个 `default.html` 文件。这是运行应用时打开的第一个页面。让我们为我们的拍照应用对此页面进行自定义（见列表 1.1）。

+ 列表 1.1 修改后的 default.html 页面

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<title>App1</title>

<!-- WinJS references --
<link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="Microsoft.WinJS.1.0/js/base.js"></script>
<script src="Microsoft.WinJS.1.0/js/ui.js"></script>

<!-- Appl references --
<link href="css/default.css" rel="stylesheet" />
<script src="js/default.js"></script>
</head>
<body>
<img id="imgPhoto" src="/images/placeholder.png" />

<!-- AppBar Control -->
<div id="appBar"
    data-win-control="WinJS.UI.AppBar">
    <button data-win-control="WinJS.UI.AppBarCommand"
    data-win-options="{
      id:'cmdTakePicture',
      label:'Take Picture',
      icon:'camera',
      tooltip:'Take Picture'
    }">
    </button>
</div>
</body>
</html>
```

列表 1.1 中的 HTML 页面已经过修改，其在页面主体（body）中包含了新内容。首先，注意该页面包含一个 ID 为 `imgPhoto` 的 `IMG` 标签。我们将在这里显示从相机中拍摄的照片。

此外，请注意该页面包含一个带有 `data-win-control="WinJS.UI.AppBar"` 属性的 `DIV` 标签。这是一个 WinJS 控件示例。该控件渲染一个包含拍照命令的应用程序标题栏（见图 1.11）。


## 创建样式表

创建一个新的 Windows Store 应用时，你还会得到一个名为 `default.css` 的默认样式表，它位于 `css` 文件夹中。该文件包含了处理不同视图状态下 Windows Store 应用的默认样式规则。

> 注意
在第 9 章中将详细讨论 Windows Store 应用的不同视图状态。

# 第 1 章构建 Windows Store 应用

对于我们的应用，我修改了 `default.css`，按如下方式格式化 `IMG` 标签中照片的外：

```css
#imgPhoto {
display: block;
margin: 15px auto;
border: 10px solid white;
max-width: 90%;
max-height: 90%;
}
```

## 创建 JavaScript 文件

我们需要修改的第三个文件是位于 `js` 文件夹下的 `default.js`。该文件包含了应用的所有逻辑。

列表 1.2 default.js

```javascript
(function () {
  "use strict";

  // DOM 元素的引用
  var imgPhoto = document.getElementById("imgPhoto");
  var cmdTakePicture = document.getElementById("cmdTakePicture");

  // 处理 DOMContentLoaded 事件
  document.addEventListener("DOMContentLoaded", function () {
    // 初始化捕获
    var captureUI = new Windows.Media.CameraCaptureUI();

    // 为拍照命令设置事件处理程序
    cmdTakePicture.addEventListener("click", function () {
      // 文件
      captureUI.captureFileAsync(function (photo) {
        if (photo) {
          // 为照片创建 URL
          var photoUrl = URL.createObjectURL(photo);
          // 在 img 中显示照片
          imgPhoto.src = photoUrl;
        }
      });
    });
  });
})();
```

## 创建你的第一个 Windows Store 应用

default.js 中的 JavaScript 代码用于处理激活和挂起等应用事件。我在第 9 章中详细讨论这些应用事件。

首先，我将所有代码放入 `init()` 函数中，以便在 DOM 准备好后执行代码。否则，如果我尝试访问任何 HTML 元素，将产生异常。

我在 `init()` 函数内部执行的第一件事是调用 `WinJS.UI.processAll()` 方法。具体来说，它将带有 `data-win-control="WinJS.UI.AppBar"` 属性的 `DIV` 标签转换为实际的标题栏。

接下来，我为拍照命令设置事件处理程序。当你点击标题栏中的拍照命令时，会创建一个 `Windows.Media.CameraCaptureUI` 类实例。CameraCaptureUI 是 Windows Runtime 类的示例。

`CameraCaptureUI.captureFiles` 方法显示拍摄屏幕（见图 1.12）。当你点击 OK 按钮时，会调用 `done()` 方法并将照片显示在 HTML 页面上。


图 1.12 摄像头捕捉界面

## 运行应用

创建应用后，可以通过点击 Visual Studio 工具栏中的绿色运行按钮（见图 1.13）或按 F5 键来运行它。


图 1.13 运行 Windows Store 风格的应用

假设笔记本电脑或平板电脑带有摄像头，你就可以开始拍照了。





# Windows Store 应用元素

请记住，“拍摄”（Take Picture）命令包含在应用栏（app bar）中，且应用栏默认是不显示的。你需要右键点击应用，或者从计算机的顶部或底部边缘滑动来显示应用栏。

# Windows Store 应用元素

正如我们在上一节中看到的，Windows Store 应用是使用多种技术构建的。Windows Store 应用是由开放且熟悉的 Web 技术（如 HTML5、JavaScript 和 CSS 3）以及微软技术（如用于 JavaScript 的 Windows 库和 Windows 运行时）结合而成的。让我再详细介绍一下这些 Windows Store 应用的每个元素。

# JavaScript

本书专门介绍如何使用 JavaScript 编写 Windows Store 应用。作为 JavaScript 的替代方案，你也可以使用 C#、Visual Basic 甚至 C++ 来编写 Windows Store 应用。

编写 Windows Store 应用时，你可以利用 ECMAScript 5 的特性，它是 JavaScript 的最新版本。这意味着你可以使用新的 JavaScript 方法，如 `indexOf()` 和 `forEach()`。你还可以使用属性的 setter（设置）和 getter（获取），并使用 "strict"。

# HTML5

在编写 Windows Store 应用时，你可以利用 HTML5 及相关标准的许多新特性。以下是这些新特性中最重要的列表：

- 表单验证属性（Form Validation Attributes）：你可以利用 HTML5 标准中新的验证属性来执行表单验证。我在第 5 章“创建表单”中讨论了这些新的验证属性以及如何在 Windows Store 应用中使用它们。

- data-* 标准（the data star standard）允许你为现有的 HTML5 元素添加自定义属性。WinJS 库使用 `data-` 进行声明式数据绑定和声明式控制实例化。

- 索引数据库 API（IndexedDB）——Indexed API 在浏览器中暴露了一个数据库。如果你需要在 Windows Store 应用的数据库中存储产品列表，那么你可以利用 IndexedDB。我将在第 8 章“创建数据源”中解释如何使用 IndexedDB。

- 文件 API（File API）——HTML5 File API 允许你在浏览器中处理文件。在上一节节构建我们的第一个 Windows Store 应用时，我们就使用了该 HTML5 API。

- 画布（Canvas）——允许你使用 JavaScript 绘制图形。我在第 12 章“图形与游戏”中为你提供了 Canvas 的介绍。

# 第 1 章 构建 Windows Store 应用

- Web Workers——允许你在不阻塞用户界面线程的情况下执行后台任务。

# 层级样式表 3 (CSS 3)

当你构建 Windows Store 应用时，你可以利用层级样式表 3 标准（及相关标准）的新特性，包括：

- 媒体查询（Media Queries）：允许你根据设备的特性（如设备的高度、宽度或视图状态）应用不同的样式。我在第 9 章中讨论了媒体查询。

- CSS3 网格布局（CSS3 Grid Layout）——允许你在不使用 HTML 表格的情况下，按列和行布局 HTML 内容。

- CSS3 弹性布局（CSS3 Flexible Box Layout）——允许在不同设备上显示 HTML 内容时保留元素的位置和大小。

# Windows 运行时 (Windows Runtime)

Windows 运行时 (WinRT) 包含一个可以在 Windows Store 应用中使用的类库。这些类被投影到 JavaScript 中，因此看起来像是内置的 JavaScript 对象。

例如，当我们编写 Windows Store 应用时，利用了 WinRT 的 `Windows.Media.Capture.CameraCaptureUI` 类。当我们调用 `CameraCaptureUI.captureFileAsync()` 方法时，我们能够拍照。

所有的 WinRT 类都从根 `Windows` 命名空间暴露在 JavaScript 中。例如，你可以用以下代码创建 `CameraCaptureUI` 类的实例：

```javascript
var captureUI = new Windows.Media.Capture.CameraCaptureUI();
```

> 注意
注意 WinRT 的类名可能会变得非常长。出于这个原因，像这样为命名空间设置别名是个好主意：
var capture = Windows.Media.Capture;

WinRT 类扩展了 JavaScript 构建 Windows 应用所需的所有功能。包含了你在构建网站时被禁止执行——或根本没有意义执行的所有操作。这些类允许你完成一些惊人的事情，例如：

- 地理位置（Geolocation）：使用 WinRT `Windows.Devices.Geolocation.Geolocator` 类使用你当前的经纬度。

- 文件访问（File Access）：通过利用 `Windows.Storage` 命名空间中的 WinRT 类来读写文件系统。

- 罗盘（Compass）：使用 `Windows.Devices.Sensors.Compass` 类随时感知正北方向。

- 打印（Print）：使用 `Windows.Printing.PrintManager` 类从你的 Windows Store 应用中打印。

- 压缩文件（Compress Files）：使用 WinRT `Windows.Storage.Compression` 命名空间中的类压缩和解压文件。

# 用于 JavaScript 的 Windows 库

用于 JavaScript 的 Windows 库 (WinJS) 是微软专门为构建 Windows Store 应用创建的纯 JavaScript 库。理解如何使用此库是本书的侧重点。

WinJS 库包含了所有的 WinJS 控件。这些是你用于构建 Windows Store 应用界面的控件。例如，WinJS 库包含一个 `DatePicker` 控件，它显示一个用于选择日期的用户组件。

# jQuery 怎么样？

jQuery 是宇宙中最流行的 JavaScript 库。有一个明显的问题：在构建 Windows Store 应用时是否可以使用 jQuery？

> 注意
根据 BuiltWith 的数据，前 10,000 个网站中超过 57% 使用了 jQuery。这是网站上最常用的 JavaScript 框架。参见 http://trends.BuiltWith.com/javascript。

答案是肯定的。
[/content]

等待，我注意到提供的 35-38 页的 OCR 文本非常碎片，且第一遍处理包含一些错误。让我根据你的指令提供所有页面的完整文本。

[content]
# Windows Store 应用元素

请记住，“拍摄”（Take Picture）命令包含在应用栏中，且应用栏默认是不显示的。你需要右键点击应用，或者从计算机的顶部或底部边缘滑动来显示应用栏。

# Windows Store 应用元素

正如我们在上一节中看到的，Windows Store 应用是使用多种技术构建的。Windows Store 应用是由开放且熟悉的 Web 技术（如 HTML5、JavaScript 和 CSS 3）以及微软技术（如用于 JavaScript 的 Windows 库和 Windows 运行时）结合而成的。让我再详细介绍一下这些 Windows Store 应用的每个元素。

# JavaScript

本书专门介绍如何使用 JavaScript 编写 Windows Store 应用。作为 JavaScript 的替代方案，你也可以使用 C#、Visual Basic 甚至 C++ 来编写 Windows Store 应用。

编写 Windows Store 应用时，你可以利用 ECMAScript 5 的特性，它是 JavaScript 的最新版本。这意味着你可以使用新的 JavaScript 方法，如 `indexOf()` 和 `forEach()`。你还可以使用属性的 setter 和 getter，并使用 "strict"。

# HTML5

在编写 Windows Store 应用时，你可以利用 HTML5 及相关标准的许多新特性。以下是这些新特性中最重要的列表：

- 表单验证属性（Form Validation Attributes）：你可以利用 HTML5 标准中新的验证属性来执行表单验证。我在第 5 章“创建表单”中讨论了这些新的验证属性以及如何在 Windows Store 应用中使用它们。

- data-* 标准（the data star standard）允许你为现有的 HTML5 元素添加自定义属性。WinJS 库使用 `data-` 进行声明式数据绑定和声明式控制实例化。

- 索引数据库 API（IndexedDB）——Indexed API 在浏览器中暴露了一个数据库。如果你需要在 Windows Store 应用的数据库中存储产品列表，那么你可以利用 IndexedDB。我将在第 8 章“创建数据源”中解释如何使用 IndexedDB。

- 文件 API（File API）——HTML5 File API 允许你在浏览器中处理文件。在上一节构建我们的第一个 Windows Store 应用时，我们就使用了该 HTML5 API。

- 画布（Canvas）——允许你使用 JavaScript 绘制图形。我在第 12 章“图形与游戏”中为你提供了 Canvas 的介绍。

# 第 1 章 构建 Windows Store 应用

- Web Workers——允许你在不阻塞用户界面线程的情况下执行后台任务。

# 层级样式表 3 (CSS 3)

当你构建 Windows Store 应用时，你可以利用层级样式表 3 标准（及相关标准）的新特性，包括：

- 媒体查询（Media Queries）：允许你根据设备的特性（如设备的高度、宽度或视图状态）应用不同的样式。我在第 9 章中讨论了媒体查询。

- CSS3 网格布局（CSS3 Grid Layout）——允许你在不使用 HTML 表格的情况下，按列和行布局 HTML 内容。

- CSS3 弹性布局（CSS3 Flexible Box Layout）——允许在不同设备上显示 HTML 内容时保留元素的位置和大小。

# Windows 运行时 (Windows Runtime)

Windows 运行时 (WinRT) 包含一个可以在 Windows Store 应用中使用的类库。这些类被投影到 JavaScript 中，因此看起来像是内置的 JavaScript 对象。

例如，当我们编写 Windows Store 应用时，利用了 WinRT 的 `Windows.Media.Capture.CameraCaptureUI` 类。当我们调用 `CameraCaptureUI.captureFileAsync()` 方法时，我们能够拍照。

所有的 WinRT 类都从根 `Windows` 命名空间暴露在 JavaScript 中。例如，你可以用以下代码创建 `CameraCaptureUI` 类的实例：

```javascript
var captureUI = new Windows.Media.Capture.CameraCaptureUI();
```

> 注意
注意 WinRT 的类名可能会变得非常长。出于这个原因，像这样为命名空间设置别名是个好主意：
var capture = Windows.Media.Capture;

WinRT 类扩展了 JavaScript 构建 Windows 应用所需的所有功能。包含了你在构建网站时被禁止执行——或根本没有意义执行的所有操作。这些类允许你完成一些惊人的事情，例如：

- 地理位置（Geolocation）：使用 WinRT `Windows.Devices.Geolocation.Geolocator` 类使用你当前的经纬度。

- 文件访问（File Access）：通过利用 `Windows.Storage` 命名空间中的 WinRT 类来读写文件系统。

- 罗盘（Compass）：使用 `Windows.Devices.Sensors.Compass` 类随时感知正北方向。

- 打印（Print）：使用 `Windows.Printing.PrintManager` 类从你的 Windows Store 应用中打印。

- 压缩文件（Compress Files）：使用 WinRT `Windows.Storage.Compression` 命名空间中的类压缩和解压文件。

# 用于 JavaScript 的 Windows 库
用于 JavaScript 的 Windows 库 (WinJS) 是微软专门为构建 Windows Store 应用创建的纯 JavaScript 库。理解如何使用此库是本书的侧重点。

WinJS 库包含了所有的 WinJS 控件。这些是你用于构建 Windows Store 应用界面的控件。例如，WinJS 库包含一个 `DatePicker` 控件，它显示一个用于选择日期的用户组件。

# jQuery 怎么样？

jQuery 是宇宙中最流行的 JavaScript 库。有一个明显的问题：在构建 Windows Store 应用时是否可以使用 jQuery？

> 注意
根据 BuiltWith 的数据，前 10,000 个网站中超过 57% 使用了 jQuery。这是网站上最常用的 JavaScript 框架。参见 http://trends.BuiltWith.com/javascript。

答案是肯定的。

## LISTING 1.3 在 Windows Store 应用中使用 jQuery

将 jQuery 添加到 Windows Store 应用最简单的方法是使用 Visual Studio 中的包管理器（Package Manager）。选择工具（Tools）菜单，包管理器（Package Manager），包管理器控制台（Package Manager Console）。输入 install-package 命令（见图 14）。

```powershell
PS> Install-Package jQuery
Successfully installed '1.8.2'.
```

执行 install-package 命令会在 Scripts 文件夹，包含三个文件。

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<title>jQueryWindows8</title>

<!-- WinJS 引用 -->
<link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="//Microsoft.WinJS.1.0/js/base.js"></script>
<script src="//Microsoft.WinJS.1.0/js/ui.js"></script>

<!-- jQuery 引用 -->
<script type="text/javascript" src="Scripts/jquery-1.7.2.js"></script>

<style type="text/css">
#divMessage {
  display:none;
  padding:10px;
  border: solid 1px;
  background-color: #ff6a00;
}
</style>
</head>
<body>
<button id="btnShow">点击这里</button>
<div id="divMessage">
秘密消息
</div>

<script type="text/javascript">
  $("#btnShow").click(function () {
    $("divMessage").fadeToggle("slow");
  });
</script>
</body>
</html>
```

列表 1.3 包含一个按钮和一个 DIV 元素。DIV 元素的内容默认是隐藏的（带有 display:none）。当你点击按钮时，DIV 的内容会缓慢淡入视图（见图 1.15）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c5_38_0.png)

图 1.15 – 使用 jQuery 动画 DIV

> 注意
列表 1.3 中的代码位于 Chapter1 项目中名为 jQueryWindows8 的文件夹中。

> 警告
Windows Store 应用在本地上下文中执行的 JavaScript 代码具有额外的安全限制以防止脚本注入攻击。特别是你不能将包含潜在危险内容（如脚本或不完整的 HTML）的 HTML 赋值给元素的 innerHTML 属性。如果你在使用没有考虑这些安全限制的 JavaScript 库（例如 jQuery），那么你可能需要修改该库以适应 Windows Store 应用。如果你信任赋值给 innerHTML 属性的内容，那么与其使用 innerHTML 属性，不如使用 WinJS.Utilities.setInnerHTMLUnsafe() 方法。





## 使用 Visual Studio 构建 Windows Store 应用

本书侧重于如何使用 Visual Studio 构建 Windows Store 应用。在本节中，我打算花几页纸来介绍在构建 Windows Store 应用时重要的 Visual Studio 特性。你将学习如何为 Windows Store 应用选择项目模板、如何运行 Windows Store 应用以及如何调试 Windows Store 应用。

## Windows Store 应用项目模板

当你在 Visual Studio 中选择“文件 > 新建项目”菜单项时，你可以从五种不同的项目模板中选择一个作为你 Windows Store 应用的起点：

- 1. 空应用（Blank App）——最简单的模板。包含单个默认的 `default.html`、`default.css` 和 `default.js` 文件。
- 2. 导航应用（Navigation App）——需要多个页面的应用使用此模板。
- 3. 网格应用（Grid App）——包含两个页面。一个页面显示不同分组的项列表。另一个页面显示你点击的项目的详情。
- 4. 分割式应用（Split App）——包含两个页面。一个页面显示组列表。另一个页面显示项列表和某个项的详情。
- 5. 固定布局应用（Fixed Layout App）——无论屏幕分辨率如何，始终将元素缩放为相同大小且具有相同的宽高比例。

在上面创建第一个 Windows 应用时，我们已经使用了“空应用”项目模板。让我详细讨论一下其他项目模板。

## 导航应用项目模板

“空应用”模板是构建简单的单页应用时的良好模板。相反，如果你需要支持多个页面，你应该使用“导航应用”模板。

导航应用项目模板包含一个名为 `home.html` 的单页。你可以通过向 `pages` 子文件夹中添加新的页面控件来添加额外页面（见图 1.16）。我将在第 10 章“页面片段与导航”中详细描述如何创建多页应用程序。

## 使用 Visual Studio 构建 Windows Store 应用

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_40_0.png)

图 1.16 使用导航应用模板创建多页应用

接下来的两个项目模板——网格项目模板和分割式应用项目模板是在导航应用模板的基础上的。换句话说，网格和分割式应用项目模板是带有额外页面的多页应用。

## 网格应用项目模板

网格应用项目模板显示不同分组的项集。你可以点击某项以查看该项目的详情。

例如，想象你正在创建一个产品目录。在这种情况下，你可能会创建不同的产品类别，如饮料和水果。每个类别都是一个组，每个类别包含一组产品项。

网格应用项目模板根据你的应用的视图状态显示不同的页面。如果你的应用未处于“靠上（snapped）”状态，则有两个页面。`groupedItems` 页面显示组及其对应的项（见图 1.17）。当你点击某项时，`itemDetail` 页面会显示特定项目的详情（见图 1.18）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_40_1.png)

图 1.17 网格应用的 groupeditems 页面

# 第 1 章 构建 Windows Store 应用

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_41_0.png)

图 1.18 网格应用的 itemDetails

如果你的 Windows Store 应用处于“靠上”状态，则会有一个额外的页面。你选择一个组（见图 1.19），然后选择一个项（见图 1.20），最后看到项目详情（见图 1.21）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_41_1.png)

图 1.19 靠上状态下网格应用的 groupedItems 页面

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_42_0.png)

图 1.20 靠上状态下网格应用的 groupDetail 页面

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_42_1.png)

图 1.21 靠上状态下网格应用的 itemDetail 页面

## 分割式应用项目模板

分割式应用项目模板也可以用于将项分组显示在产品类别中。分割式应用项目模板有两个页面：`items` 和 `split`。

`items` 页面显示组列表。例如，在图 1.22 中，`items` 页面显示产品类别。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_43_0.png)

图 1.22 分割式应用的 items 页面

如果你点击一个组，就会导航到 `split` 页面。该页面显示项列表——该类别中的产品——并允许你选择某项以查看项详情（见图 1.23）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_44_0.png)

图 1.23 分割式应用的 split 页面

与网格应用模板一样，分割式应用项目模板在应用处于“靠上”时提供了不同的用户体验。当分割式应用处于“靠上”状态时，你从组导航到项。

## 固定布局模板

固定布局模板适用于非常特定的场景。该模板包含一个 `Viewbox` 控件，它可以调整内容以适应屏幕，同时保持正确的宽高比例。例如，假设你有一张 800x480 的图片。图 1.24 显示了在 1024x768 分辨率下该图片。。注意，图片已自动缩放以适应可用空间。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_45_0.png)

图 1.24 1024x768 分辨率下的图片

如果你在不同分辨率下查看该图片，它会自动调整以适应新分辨率。例如，图 1.25 展示了在 1920x1080 分辨率下的情况。注意，图片将填充整个可用空间。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_45_1.png)

图 1.25 1920x1080 分辨率下的图片

## 使用 Visual Studio 构建 Windows Store 应用

当应用“靠上”时，MessageBox 会自动调整其子元素的大小（见图 1.26）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_46_0.png)

图 1.26 应用靠上时调整图片大小

MessageBox 控件有一些显著的局限性。你只能向 MessageBox 添加一个子元素。例如，它无法处理一组图片。

此外，MessageBox 不支持文本。你可以使用 MessageBox 调整图片或画布的大小。

使用 MessageBox 的主要场景是你想要创建一个游戏，并希望游戏在电脑和平板电脑上看起来都很完美。你不希望你的愤怒小鸟在某台电脑上看起来很胖，而在另一台上看起来很瘦。

> 注意
> 在后台，MessageBox 控件使用层样式表的 `translate` 和 `scale` 函数。

## 运行 Windows Store 应用

Visual Studio 为你提供了运行 Windows Store 应用的不同选项：

- 本地机器（Local Machine）
- 模拟器（Simulator）
- 远程机器（Remote Machine）

本地机器选项像应用安装在本地上一样运行 Windows Store 应用。Windows Store 应用将使用你的开发机器（运行 Visual Studio 的机器）的屏幕分辨率和功能。

模拟器选项在一个独立的窗口中运行你的应用（见图 1.27）。使用模拟器的优点是你可以模拟不同类型的设备。例如，你可以从鼠标模式切换到基础触摸模式，以模拟平板等触摸设备。你还可以切换到不同的屏幕分辨率来测试不同分辨率下的应用。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_47_0.png)

图 1.27 使用 Visual Studio 模拟器

最后一个选项是在远程机器上部署并运行 Windows Store 应用。在远程机器上运行应用之前，你必须先在项目属性窗口中指定远程机器名称（见图 1.28）。





![](img/3fb402034fe87fe7c8b9c70e5eae6c75_48_0.png)

指定远程机器名称后，您可以通过从 Visual Studio 工具栏中选择此选项在远程机器上部署并运行您的应用程序。

> **警告** 在远程机器上部署和运行应用程序，您需要在远程机器上安装 Visual Studio 2012 远程工具（Remote Tools）。您可以从 Microsoft.com 网站下载这些工具。

# 调试 Windows Store 应用

我总是很乐观，相信我编写的任何代码在第一次运行时都不会出现错误。到目前为止，这种情况从未发生过。我花费了大量时间调试那些并没有按照我预期的代码。

在本节中，我将讨论 Visual Studio 中可以用于调试代码的工具。我将介绍如何使用 JavaScript 控制台窗口、断点以及使用 DOM 探测器。

## 使用 Visual Studio JavaScript 控制台窗口

当我为网站使用的页面编写 JavaScript 时，我会使用 JavaScript 控制台窗口查看 JavaScript 错误。我还会使用 `console.log()` 向控制台窗口写入自定义消息，以便调试代码（见图 1.29）。

# 第 1 章 构建 Windows Store 应用

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_49_0.png)

图 1.29 使用 Google Chrome JavaScript 控制台调试

运行 Windows Store 应用时，您无法访问浏览器的 JavaScript 控制台。您不需要使用浏览器的 JavaScript 控制台，而是需要使用 Visual Studio JavaScript 控制台（见图 1.30）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_49_1.png)

图 1.30 发送到 Visual Studio JavaScript 控制台窗口的错误和调试消息

您可以使用与写入浏览器控制台完全相同的方式通过 `console.log()` 在 JavaScript 控制台窗口查看 JavaScript 错误和调试消息。

如果您遇到错误并想显示 JavaScript 变量的值，可以在 JavaScript 控制台的底部输入变量名（见图 1.31）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_49_2.png)

图 1.31 将 JavaScript 变量导出到 JavaScript 控制台窗口

> 注意
Visual Studio 控制台窗口仅在应用程序运行时出现。如果您找不到该窗口，请使用菜单选项 调试（Debug）> Windows（Windows）> JavaScript 控制台（JavaScript Console）。

## 设置断点

如果您正在构建 Windows Store 应用，并且该应用的行为让您无法理解，那么设置断点并逐行执行代码将非常有帮助。

您可以通过点击 Visual Studio 代码编辑器中想要中断的行旁左侧间隙来设置断点（见图 1.32）。当您在调试模式下运行应用程序并命中断点时，您可以通过鼠标悬停在变量上检查其值。

```
getCount: function () {
  var that = this;
  return new jQuery.Promise(function (complete, error) {
    that.getStore().then(function (store) {
      var defaultConfig;
      if (cursorOptions) {
        var cursorOptions = that.cursorOptions;
        var index = store.index(cursorOptions.indexOf);
        var keyRange = cursor.Range(cursorOptions);
        if (index < lower) {
          reCount++;
        } else if (index > upper) {
          reCount--;
        }
      }
      reCount.onerror = function (err);
      reCount.success = function (evt) {
        complete(evt.target.result);
      };
    });
  });
};
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_50_0.png)

您可以通过使用工具栏上的“单步进入”（Step Into）按钮或按 F11 来逐行执行代码。

> 作为使用 Visual Studio 设置断点的替代方案，您可以使用 JavaScript 调试器在代码中创建断点。

## 使用 DOM 探测器

您使用的浏览器开发工具的另一个是 HTML 检查器（例如 Firefox 的一项功能）。您可以使用此工具查看文档中实时的 HTML 和 CSS。

Visual Studio 支持一个名为 DOM 探测器（DOM Explorer）的类似工具。您可以使用 DOM 探测器来检查运行中的 Windows Store 应用中任何 HTML 元素的属性。

在 Visual Studio 中运行 Windows Store 应用后，可以通过选择菜单选项 调试（Debug）> DOM 探测器（DOM Explorer）来查看 DOM 探测器窗口。在 DOM 探测器窗口中，您可以点击任何元素并查看该元素的所有属性，包括与元素相关的所有样式信息（见图 1.33）。

# 38 第 1 章 构建 Windows Store 应用

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_51_0.png)

图 1.33 使用 DOM 元素探测器

如果您点击与 WinJS 控件关联的元素，就可以看到该控件渲染的所有 HTML 属性和元素。

## 发布到 Windows Store

构建 Windows Store 应用的主要动机之一是销售您的应用。在本节中，我将讨论需要遵循的步骤。

> 警告
在远程机器上部署和运行应用程序，您需要在远程机器上安装 Visual Studio 2012 远程工具（Remote Tools）。您可以从 Microsoft.com 网站下载这些工具。

> 注意
Visual Studio 控制台窗口仅在应用程序运行时出现。如果您找不到该窗口，请使用菜单选项 调试（Debug）> Windows（Windows）> JavaScript 控制台（JavaScript Console）。

> 作为使用 Visual Studio 设置断点的替代方案，您可以使用 JavaScript 调试器在代码中创建断点。

> 注意
Windows Store 认证要求详见：http://msdn.microsoft.com/en-us/library/windows/apps/hh694083.aspx。

> 注意
应用认证工具包（App Certification Kit）在您安装 Visual Studio 时同时安装。您可以通过从启动屏幕运行 Windows 应用认证工具包（Windows App Cert Kit）独立于 Visual Studio 运行它。





# 第 1 章 构建 Windows Store 应用

当你运行 Windows App Certification Kit 时，该工具包会启动你的应用，并在你的电脑进行了一段时间“疯狂操作”后，会生成一份报告，详细说明你的应用是通过还是失败（见图 1.38）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_55_0.png)

图 1.38 由 Windows App Certification Kit 生成的（成功的）认证报告

> 注意：如果你使用 Team Foundation Server，甚至可以将 Windows App Certification Kit 集成到你的构建过程中。每当你对应用进行新构建时，都可以自动运行技术认证测试。

当你的应用通过所有认证要求——在获得微软批准后——你的应用将出现在 Windows Store 中，你可以开始赚钱了。当任何人购买你的应用时，资金将添加到你在 Windows Store 仪表板上设置的付款账户。

## 总结

本章的目标是向你介绍 Windows Store 应用。我在本章的开始为你提供了微软设计风格原则的概述。你还学习了 Windows Store 应用的标准功能，如应用栏（app bar）、小功能（charms）和贴靠视图状态（snapped view state）。

然后，我引导你逐步完成了第一个 Windows Store 应用的构建。我们创建了一个非常酷的摄像头应用，这种应用是你无法作为标准 Web 应用实现的。

你学习了 Windows Store 应用的标准元素。你学习了 Windows Store 应用是如何由标准的 HTML5、JavaScript 和 CSS3 组成的。你还学习了 Windows Store 应用如何利用 Windows Runtime 和 Windows JavaScript 库等微软技术。

我还解释了在构建 Windows Store 应用时如何利用适用于 Windows 8 的 Visual Studio 功能。你学习了如何使用模拟器运行 Windows Store 应用。你还学习了如何使用断点和 Visual Studio JavaScript 控制台窗口来调试 Windows Store 应用。

最后，你学习了如何通过将应用发布到 Windows Store 来从中盈利。你学习了如何注册应用、提交应用并通过认证。

# 第 2 章

## WinJS 基础

- 命名空间、模块和类
- 使用 Promises 进行异步编程
- 使用 Query Selectors 获取 DOM 元素
- 使用 xhr 函数执行 Ajax 调用

本章的目标是解释基础 WinJS 库中包含的功能。这些功能在你构建的几乎任何应用程序中都会用到。

本章的第一部分专门介绍命名空间、模块和类的主题。你学习了组织 JavaScript 代码的推荐模式。

接下来，你学习了如何利用名为 *promises* 的基础 WinJS 库。Promises 为你提供在 JavaScript 代码中执行异步编程的优雅方式。

在本章中，你还学习了在处理 WinJS 库工作时如何使用 *Query Selectors*。Query Selectors 允许你高效地从 HTML 文档中检索 DOM 元素（类似于 jQuery 选择器）。

最后，你学习了如何使用基础 WinJS 库中包含的名为 `xhr()` 的函数。`xhr()` 函数允许你执行 Ajax 调用——包括跨域调用。

## 命名空间、模块和类

***

当你使用 WinJS 库构建 Windows Store 应用时，微软建议在组织 JavaScript 代码时遵循特定的模式。特别是，他们建议将代码组织成命名空间、模块和类。

通过遵循这些模式，你可以构建出 bug 较少且随时间推移更容易维护的 JavaScript 代码。

### 使用命名空间

让我先解释一下 WinJS 库中定义命名空间的方法。

在做任何其他操作之前，我们应该开始回答这些问题：为什么我们需要命名空间？它们起什么作用？它们会给我们的 Windows Store 应用增加不必要的复杂性吗？

毕竟，许多 JavaScript 库在不引入命名空间支持的情况下运行得很好。例如，jQuery 不支持命名空间，而 jQuery 是宇宙上最流行的 JavaScript 库。如果 jQuery 不需要命名空间也能运行，我们又何要担心命名空间呢？

命名空间在编程语言中起到两个作用。首先，命名空间防止命名冲突。换句话说，命名空间允许你创建多个同名对象而不产生冲突。

例如，想象两家公司——A 公司和 B 公司都想制作一个 JavaScript 购物车控件，并且两家公司都想命名为 ShoppingCart。通过创建 CompanyA 命名空间和 CompanyB 命名空间，两家公司都可以创建自己的购物车控件：CompanyA.ShoppingCart 和 CompanyB.ShoppingCart。

命名空间的第二个功能是组织。当功能定义在不同的物理文件中时，命名空间用于对相关功能分组。我知道 WinJS 库中所有与类相关的方法都可以在 WinJS.Class 命名空间中找到。命名空间更容易理解库中可用的功能。

如果你正在构建一个简单的 JavaScript 应用，那么你没有多少理由关心命名空间。如果你需要使用由不同的人编写的多个库，命名空间就会变得非常重要。

### 使用 WinJS.Namespace.def()

在 WinJS 库中，创建命名空间最基本的方法是使用 WinJS.Namespace.def() 方法。该方法允许你声明一个命名空间（任意深度）。

WinJS.Namespace.def() 方法具有以下参数：

- name: 代表新命名空间名称的字符串。你可以使用点表示法添加嵌套命名空间
- members: 要添加到命名空间的可选对象集合

***

（注：此处后续由于原文存在大量重复和 OCR 错误，已根据要求进行了去重和整合，保留核心逻辑翻译）





# 命名空间、模块与类 49

JavaScript 不支持访问修饰符。你无法将对象或方法标记为公共或私有。任何人都可以调用任何方法并与任何对象进行交互。

JavaScript 中封装（隐藏）方法和对象的唯一机制是利用函数。在 JavaScript 中，函数决定了变量的作用域。JavaScript 变量要么具有全局作用域——它在任何地方都可用——要么具有函数作用域——仅在函数内部可用。如果你想隐藏一个对象或方法，你就需要将其放在函数内部。

例如，以下代码包含一个名为 `doSomething()` 的函数，其中包含一个嵌套函数 `doSomethingElse()`：

```javascript
function doSomething() {
  console.log("doSomething");

  function doSomethingElse() {
    console.log("doSomethingElse");
  }
}
```

```javascript
doSomething(); // 输出 "doSomething"
doSomethingElse(); // 抛 ReferenceError
```

你只能在 `doSomething()` 函数内部调用 `doSomethingElse()`。`doSomethingElse()` 函数被封装在 `doSomething()` 函数中。

WinJS 库利用函数封装来隐藏其所有的内部方法。所有的 WinJS 方法都定义在自执行匿名函数中。默认情况下一切都是隐藏的。公共方法通过显式地将公共方法添加到全局作用域中定义的命名空间来暴露。

例如，假设我想建立一个小型实用方法库。我想创建一个用于计算销售税的方法以及一个用于计算产品预计发货日期的方法。列表 2.2 中的代码通过一个自执行匿名函数封装了我的库：

# 列表 2.2 使用模块封装函数 (modules\modules.html)

```javascript
(function global() {
  // 计算销售税的公共方法
  function calculateTax(price) {
    return calculateFederalTax(price) + calculateStateTax(price);
  }

  // 计算州税的私有方法
  function calculateStateTax(price) {
    return price * 0.08;
  }

  // 计算联邦税的私有方法
  function calculateFederalTax(price) {
    return price * 0.02;
  }

  // 返回预计发货日期的公共方法
  function calculateShipDate(currentDate) {
    currentDate.setDate(currentDate.getDate() + 4);
    return currentDate;
  }

  // 输出公共方法
  WinJS.Namespace.define("CompanyA.Utilities",
    calculateTax: calculateTax,
    calculateShipDate: calculateShipDate
  );
})(this);

// 显示预计发货日期
var shipDate = CompanyA.Utilities.calculateShipDate(new Date());
console.log(shipDate);

// 显示 价格 + 税
var price = 12.33;
var tax = CompanyA.Utilities.calculateTax(price);
console.log(price + tax);
```

在之前的代码中，该自执行匿名函数包含了四个函数：`calculateTax()`、`calculateStateTax()`、`calculateFederalTax()` 和 `calculateShipDate()`。以下语句用于仅暴露 `calculateTax()` 和 `calculateShipDate()` 函数：

```javascript
// 输出公共方法
WinJS.Namespace.define("CompanyA.Utilities",
  calculateTax: calculateTax,
  calculateShipDate: calculateShipDate
);
```

# 命名空间、模块与类

由于 `calculateTax()` 和 `calculateShipDate()` 函数被添加到 `CompanyA.Utilities` 命名空间中，你可以在自执行函数外部调用这两个方法。这些是你的库的公共方法，构成了公共 API。

另一方面，`calculateStateTax()` 和 `calculateFederalTax()` 方法被隐藏在自执行函数的“黑洞”中。这些方法被封装起来，并且永远无法在自执行函数的作用域之外被调用。这些是你库的内部方法。

## 使用类

与其他许多流行的计算机语言（如 C# 或 Java）不同，JavaScript 没有对类提供任何内置支持。在 JavaScript 中，你不需要区分类型（类）和该类型的实例（对象）。JavaScript 中的一切都是对象。

WinJS 库包含了用于创建类的 JavaScript 扩展。这些方法在 WinJS 库内部被广泛使用。例如，所有的 WinJS JavaScript 控件都是使用这些方法创建的。在本节中我们将讨论如何利用 WinJS 库的方法来定义新类。

### 使用 WinJS.Class.define()

在 WinJS 库中，通过调用 `WinJS.Class.define()` 创建新的 JavaScript 类。该方法接受三个参数：

- constructor——用于初始化新对象的函数。如果你传递 `null`，则会创建一个空构造函数
- instanceMembers——实例属性和方法的集合
- staticMembers——静态属性的集合

列表 2.3 中的代码演示了如何创建一个 `Robot` 类，然后从 `Robot` 类创建一个 `Roomba` 机器人对象：

列表 2.3 创建类 (classes\classes.define(

```javascript
var Robot = WinJS.Class.define(
  function (name, price) {
    this.name = name;
    this.price = price;
  },
  _name: undefined,
  _price: 0,
  price: {
    set: function (value) {
      if (value < 0) throw new Error("Invalid price!");
      this._price = value;
    },
    get: function () {
      return this._price;
    }
  },
  _name: function () {
    return this._name;
  },
  _price: function () {
    return this._price;
  },
  name: {
    set: function (value) {
      this._name = value;
    },
    get: function () {
      return this._name;
    }
  },
  makeNoise: function () {
    return "My name is " + this.name + " and I am a Roomba";
  }
);

var roomba = new Robot("rover", 20.33);
console.log(roomba.name);
console.log(roomba.price);
console.log(roomba.makeNoise());
```





## 命名空间、模块与类

```javascript
var Roomba = WinJS.Class.mix(
  function (name) {
    this.name = name;
  },
  Robot
);
```

```javascript
var myRoomba = new Roomba("rover");
console.log(myRoomba.makeNoise()); // 输出 "beep"
```

在前面的代码中，`Roomba` 类包含了 `Robot` 类的所有方法。混入（mixins）的优点之一是你可以使用混入来支持类似多重继承的功能。你可以使用混入来组合任意数量的方法和属性集。例如，列表 2.6 中的代码示例演示了如何通过 `Robot` 方法、`Product` 方法和 `Vacuum` 方法来构建一个 `Roomba`。

## 列表 2.6 组合多个对象 (mixinMultiple/mixinMultiple.html)

```javascript
"use strict";
var Robot = {
  makeNoise: function () {
    return "beep";
  }
};
```

```javascript
var Product = {
  price: {
    set: function (value) {
      if (value < 0) {
        throw new Error("无效的价格!");
      }
      this._price = value;
    },
    get: function () { return this._price; }
  },
  sayName: function () {
    return this.name;
  }
};
```

```javascript
var Vacuum = {
  vacuum: function () { return "bzzzzzz"; }
};
```

```javascript
var Roomba = WinJS.Class.mix(
  function (name) {
    this.name = name;
  },
  Robot, Product, Vacuum
);
```

```javascript
var myRoomba = new Roomba("rover");
console.log(myRoomba.makeNoise()); // 输出 "beep"
console.log(myRoomba.setName()); // 输出 "rover"
console.log(myRoomba.vacuum()); // 输出 "bzzzzz"
myRoomba.price = -88 // 抛出 Error
```

注意，混入可以同时包含方法和属性。此外，混入属性可以包含 setter（设置）和 getter（get）。例如，`Product` 混入中包含的 `price` 属性包含一个执行验证的 setter。

当你执行上述代码时，图 2.3 所示的 Visual Studio JavaScript 代码窗口中将显示以下结果。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_69_0.png)

图 2.3 Robot 的噪音

> 注意
> WinJS 库包含了几个你可以在代码使用的混入，包括 `WinJS.Utilities.eventMixin`、`WinJS.UI.DOMEventMixin` 以及 `WinJS.Binding.dynamicObserver-Mixin`。

## 使用 Promises 进行异步编程

某些代码会立即执行，某些代码需要时间完成，或者可能永远不会完成。例如，获取本地变量的值是一个即时操作。通过 Ajax 请求从远程网站获取数据需要更长时间，或者可能根本无法完成。

当一个操作可能需要长时间才能完成时，你应该编写代码使其以异步执行。与其等待操作完成，你应该启动该操作，然后去做其他事情，直到接收到操作完成的信号。

一个类比：某些电话客服热线需要你在候音期间等待——听着非常难听的音乐——直到客服代表可用。这是同步编程，非常浪费你的时间。

一些较新的客服热线允许你输入电话号码，这样当客服代表有空时，就可以给你回电。这种方法浪费的时间要少得多，因为你可以在等待回电的同时做些事情。

有几种模式可以用于编写异步执行的代码。在 JavaScript 中最流行的模式是**回调模式**（callback pattern）。当你调用一个可能需要长时间才能返回结果的函数时，你向该函数传递一个回调函数。

使用回调是 JavaScript 异步编程的自然方式。与其等待操作完成并坐在那里听着非常难听的音乐，你可以在操作完成后获得一个回调。

## 使用 Promises

CommonJS 网站对 promise 的定义如下 (http://wiki.common.org/wiki/Promises)：

Promise 为与对象交互提供了一个良好定义的接口，该对象代表一个异步执行的操作的结果，且该操作在任何给定时间可能已经完成，也可能尚未完成。通过利用标准接口，不同的组件可以为异步操作返回 promise，消费者可以以可预测的方式利用 promise。

Promise 为指定回调提供了标准模式。在 WinJS 库中，当你创建一个 promise 时，可以指定三个回调：完成回调（complete callback）、失败回调（failure callback）和进度回调（progress callback）（失败和进度回调都是可选的）。

Promises 在 WinJS 库中被广泛使用。动画库、控件库和绑定库中的方法都使用了 promise。

例如，WinJS 基础库中包含的 `xhr()` 方法返回一个 promise。`xhr()` 方法将对标准 `XMLHttpRequest` 对象的调用封装在 promise 中。列表 2.7 演示了如何使用 `xhr()` 方法执行 Ajax 请求以从 StephenWalther.com 获取馈送（feed）：

## 列表 2.7 创建 Promise (promises/promises.html)

```javascript
var options = {
  url: "http://stepwalther.com/blog/feed",
  responseType: "document"
};
```

```javascript
WinJS.xhr(options).done(
  function (XMLHttpRequest) {
    console.log("success");
    // 显示第一条目的标题
    var firstTitle = XMLHttpRequest.response.querySelector("item>title");
    console.log(firstTitle.textContent);
  },
  function (XMLHttpRequest) {
    console.log("fail");
  },
  function (XMLHttpRequest) {
    console.log("progress");
  }
);
```

WinJS 基础库包含的 `xhr()` 方法返回一个 promise。`xhr()` 方法将对标准 `XMLHttpRequest` 对象的调用封装在 promise 中。Promise 类包含 `done()` 方法，它接受三个回调：

Promise.done(完成回调, 错误回调, 进度回调)

在代码中，传递了三个匿名函数。除非发生网络错误，否则错误函数不会被调用。进度函数在 Ajax 请求期间会被多次调用。最后，当 Ajax 调用完成后，完成回调会显示条目的标题（见图 2.4）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_71_0.png)

图 2.4 使用 promise

## then() 与 done()

上一节中，我们使用 Promise 对象的 `done()` 方法来设置完成、错误和进度回调。Promise 对象暴露了另一个与 `done()` 密切的方法：`then()` 方法。

## 使用 Promises 进行异步编程

`then()` 方法——就像 `done()` 方法一样——允许你设置完成、错误和进度回调函数。为什么存在 `then()` 方法？`then()` 和 `done()` 之间有两个重要的区别。

`then()` 方法与 `done()` 方法不同，它支持链。如果你需要链多个 promise，必须使用 `then()` 方法。例如，列表 2.8 中的代码演示了如何通过一个 Ajax 请求获取博客中最新文章的 URL，然后通过第二个 Ajax 请求下载该文章的内容。第二个 Ajax 请求在第一个请求完成前不会执行。

## 列表 2.8 Promise 链式 (promiseChain/promiseChain.html)

```javascript
var options = {
  url: "http://stephenwalther.com/blog/feed",
  responseType: "document"
};
```

```javascript
WinJS.xhr(options).then(
  function (XMLHttpRequest) {
    // 获取第一条目的链接
    var firstLink = XMLHttpRequest.response.querySelector("item>link");

    // 发起第二次 Ajax 请求（返回一个 promise）
    return WinJS.xhr({
      url: firstLink.textContent,
      responseType: "document"
    });
  }).then(
  function (XMLHttpRequest) {
    // 获取博客正文
    var postBody = XMLHttpRequest.response.querySelector("div.entry");

    // 打印博客的前 200 个字符
    console.log(postBody.textContent.trim().substr(0, 200));
  }
);
```

在列表 2.8 中，注意传递给 `then()` 方法的完成函数返回了第二个 promise。调用 WinJS.xhr() 返回一个新的 promise。

如果第二个 promise 成功完成，则传递给 `done()` 方法的完成回调就会执行。该方法显示博客文章的前 200 个字符。





# 第 2 章 WinJS 基础

你可以通过调用 `call().then().then()` 来链任意任意数量的 promise。链中的最后一次调用应该是调用 `done()`。

`then()` 和 `done()` 之间的第二个区别在于错误处理。你可以将错误函数作为第二个参数传递给 `then()` 和 `done()` 方法以处理错误，作为一种最佳实践，你应该这样做。但是，如果你不提供错误函数，`done()` 方法会抛出异常，而 `then()` 方法则不会。
相反，`then()` 方法会返回一个处于错误状态的 promise。

例如，列表 2.9 中的代码执行了一个带有错误 URL 的 Ajax 请求。使用 `then()` 方法发起的请求不会抛出错误。虽然错误信息会被写入 JavaScript 控制台，但应用程序不会停止。

**列表 2.9 done() 与 then() 的对决 (promiseErrors\promiseErrors.html)**

```javascript
var options = {
  url: "http://BadURL"
};

WinJS.xhr(options).then(); // 不抛出异常

WinJS.xhr(options).done(); // 会抛出异常
```

如果你不希望代码像列表 2.9 中的 `then()` 方法那样静默失败，你应该使用 `done()` 而不是 `then()`。如果你在链式调用 promise，请始终使用 `done()` 作为链中的最后一个环节。

## 创建 Promise

你可以通过创建 `Promise` 类的一个新实例来创建你自己的 promise。`Promise` 类的构造函数需要一个接受三个参数的函数：`complete`、`error` 和 `progress` 函数参数。

例如，列表 2.10 中的代码说明了如何创建一个返回 promise 的方法 `wait10Seconds()`。`progress` 函数每秒被调用一次，在通过 10 秒之前，`complete` 函数不会被调用：

**列表 2.10 创建一个 Promise (promiseCreate\promiseCreate.html)**

```javascript
function wait10Seconds() {
  return new WinJS.Promise(function (complete, error, progress) {
    var seconds = 0;
    var intervalId = window.setInterval(function () {
      seconds++;
      progress(seconds);
      if (seconds > 9) {
        window.clearInterval(intervalId);
        complete();
}, 1000);
}
```

```javascript
wait10Seconds().done(
  function () { console.log("complete") },
  function () { console.log("error") },
  function (seconds) { console.log("progress: " + seconds) }
);
```

所有的工作都在 promise 的构造函数中完成。`window.setInterval()` 方法用于每秒执行一次代码。每秒，`progress()` 回调方法都会被调用一次。如果超过了 10 秒，则会调用 `complete()` 回调方法并调用 `clearInterval()` 方法。

当执行执行上述代码时，你可以在图 2.5 中的 Visual Studio JavaScript 控制台中看到输出。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_74_0.png)

图 2.5 自定义 promise 的输出

## 创建超时 Promise

在上一节中，我们创建了一个自定义的 Promise，它使用 `window.setInterval()` 方法在 10 秒后完成 promise。实际上我们并不需要创建自定义 promise，因为 `Promise` 类已经包含一个静态方法，用于返回在特定间隔后完成的 promise。

列表 2.11 中的代码说明了你如何使用 `timeout()` 方法。`timeout()` 方法返回一个在指定毫秒数后完成的 promise。

**列表 2.11 一个超时 Promise (promiseTimeout.promiseTimeout.html)**

```javascript
WinJS.Promise.timeout(3000).then(
  function () { console.log("complete") },
  function () { console.log("error") },
  function () { console.log("progress") }
);
```

在上述代码中，Promise 在 3 秒（3000 毫秒）后完成。`timeout()` 方法返回的 promise 不支持 promise 事件。因此，写入控制台的唯一消息是 10 秒后的“complete”消息。

## 取消 Promise

某些 promise（并非所有）支持取消。当你取消一个 promise 时，该 promise 的错误回调将被执行。

例如，列表 2.12 中的代码使用 `WinJS.xhr()` 方法执行 Ajax 请求。然而，在 Ajax 请求发出后立即，请求被取消了。

**列表 2.12 取消一个 Promise (promiseCancel\promiseCancel.html)**

```javascript
// 指定 Ajax 请求选项
var options = {
  url: "http://StephenWalther.com"
};

// 发起 Ajax 请求
var request = WinJS.xhr(options).then(
  function (XMLHttpRequest) {
    console.log("success");
  },
  function (XMLHttpRequest) {
    console.log("fail: " + XMLHttpRequest.message);
  },
  function (XMLHttpRequest) {
    console.log("progress");
  }
);

// 取消 Ajax 请求
request.cancel();
```

当你运行上述代码时，消息“fail: Canceled”会被写入 Visual Studio JavaScript 控制台（见图 2.6）。取消操作仅在使用 `then()` 时支持，使用 `done()` 则不支持。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_75_0.png)

图 2.6 取消一个 promise (promiseCancel.html)





# 使用查询选择器检索 DOM 元素

```html
<h1>Secret Message</h1>
</div>
<body>
</html>
```

该文档包含了对列表 2.14 中名为 `selectors-Query.js` 的 JavaScript 引用。

# 列表 2.14 使用选择器 (selectorsQuery\selectorsQuery.js)

```javascript
function () {
  "use strict";

  function initialize() {
    WinJS.Utilities.query("button").listen("click", function () {
      WinJS.Utilities.query("div").clearStyle("display");
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}();
```

`selectorsQuery.js` 脚本使用 `WinJS.Utilities.query()` 方法检索页面所有的 `BUTTON` 元素。`listen()` 方法用于将事件处理器绑定到 `BUTTON` 点击事件。当你点击 `BUTTON` 时，隐藏 `DIV` 元素中包含的秘密将被显示。`clearStyle()` 方法用于移除 `DIV` 元素的 `display:none` 样式属性（参见图 2.7）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_79_0.png)

## 警告

确保你在文档加载之后再尝试使用 `WinJS.Utilities.query()` 方法。在列表 2.14 中，对 `WinJS.Utilities.query()` 的调用包含在 `initialize()` 函数中，该函数由 `DOMContentLoaded` 事件触发。

在底层，`WinJS.Utilities.query()` 方法使用了标准的 `querySelectorAll()` 方法。这意味着你可以使用任何与 `querySelectorAll()` 方法兼容的选择器。`querySelectorAll()` 方法定义在 W3C Selectors API Level 1 标准中，地址位于：http://www.w3.org/TR/selectors-api/

与 `querySelectorAll()` 方法不同，`WinJS.Utilities.query()` 方法返回的是一个 `QueryCollection`。我将在下文中介绍介绍 `QueryCollection` 类的方法。

## 使用 WinJS.Utilities.id() 方法检索单个元素

如果你想从文档中检索单个元素，而不是匹配一组元素，那么可以使用 `WinJS.Utilities.id()` 方法。例如，下行代码将元素的背景颜色更改为红色：

```javascript
WinJS.Utilities.id("message").setStyle("background-color", "red");
```

# 使用查询选择器检索 DOM 元素

上述语句匹配 id 为 `message` 的唯一元素。例如，该语句匹配以下 `DIV` 元素：

```html
<div id="message">Hello!</div>
```

注意，当使用 `WinJS.Utilities.id()` 方法匹配单个元素时，不需要使用哈号（#）。当你使用 `WinJS.Utilities.query()` 方法执行此类操作时，则需要使用哈号：

```javascript
WinJS.Utilities.query("#message").setStyle("background-color", "red");
```

在底层，`WinJS.Utilities.id()` 方法调用了标准的 `document.getElementById()` 方法。`WinJS.Utilities.id()` 方法将结果作为 `QueryCollection` 返回。

如果没有元素匹配传递给 `WinJS.Utilities.id()` 的标识符，你不会得到错误。相反，你会得到一个没有任何元素的 `QueryCollection`（length=0）。

## 使用 WinJS.Utilities.children() 方法

`WinJS.Utilities.children()` 方法允许你检索一个包含 DOM 元素所有子元素的 `QueryCollection`。例如，假设你有一个包含类似子 `DIV` 元素的 `DIV` 元素，如下：

```html
<div id="discussContainer">
  <div>Message 1</div>
  <div>Message 2</div>
  <div>Message 3</div>
</div>
```

你可以使用以下代码为所有子 `DIV` 元素添加边框，而不是为容器 `DIV` 元素添加边框（参见图 2.8）。

```javascript
var discussContainer = WinJS.Utilities.id("discussContainer").get(0);
WinJS.Utilities.children(discussContainer).setStyle("border", "2px dashed red");
```

# 第二章 WinJS 基础

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_81_0.png)

图 2.8 检索子元素

重要的是理解，`WinJS.Utilities.children()` 方法仅适用于 DOM 元素，而不适用于 `QueryCollection`。注意，使用 `get()` 方法是为了检索代表 `discussContainer` 的 DOM 元素。

## 使用 QueryCollection 类

`WinJS.Utilities.query()` 方法和 `WinJS.Utilities.id()` 方法都返回 `QueryCollection` 类的实例。`QueryCollection` 类派自基础的 JavaScript `Array` 类，并添加了一些处理 HTML 元素的有用方法：

- *addClass(name)* — 为 `QueryCollection` 中的每个元素添加类名
- *clearStyle(name)* — 移除 `QueryCollection` 中每个元素的样式
- *control(ctor, options)* — 允许你将 `QueryCollection` 中的项转换为 WinJS 控件
- *forEach(callbackFn, thisArg)* — 允许你对 `QueryCollection` 中的每个项执行操作
- *get(index)* — 从 `QueryCollection` 中检索指定索引的元素
- *getAttribute(name)* — 检索 `QueryCollection` 中第一个元素的属性值
- *hasClass(name)* — 如果第一个元素具有某个特定类，则返回 true

`xhr()` 函数是 `XMLHttpRequest` 对象的轻量级封装。与对 `XMLHttpRequest` 对象的操作不同，`xhr()` 返回一个 promise（承诺）。每当你想要发送 Ajax 请求时，就可以使用 `xhr()`。

列表 2.15 和 2.16 包含了执行简单 Ajax 请求的代码。检索了微软网站首页并显示了该页的所有提取内容的列表（图 2.9）。





## 使用 xhr 函数执行 Ajax 调用

);

document.addEventListener("DOMContentLoaded", initialize);
))();

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_84_0.png)

* http://www.microsoft.com/en-us
* http://www.microsoft.com/en-us/download.aspx?id=35759-5406-4d05-b71-default.aspx?ids=1-0
* http://windows.microsoft.com/en-US/home
* http://office.microsoft.com/en-us/
* http://www.microsoft.com/en-us/download.aspx?id=31779
* http://www.microsoft.com/en-us/windows/microsoft-support/home
* http://windows.microsoft.com/en-us/product/security-essentials
* http://update.microsoft.com/en-us/visualstudio/default.aspx?lang=en-us
* http://www.gameforums.com/en-US
* http://www.microsoft.com/en-us/download.aspx?id=24683
* http://support.microsoft.com/en-us/help_js-MSCOM.HP_US_BI_PinPool
* http://www.microsoft.com/enterprise/
* http://www.microsoft.com/download/default.aspx
* http://support.microsoft.com/en-us/help?id=49
* http://www.microsoft.com/
* http://www.microsoft.com/en-us/legal/privacy

图 2.9 请求并显示来自微软首页面的链接

WinJS.xhr() 函数返回一个 promise。在列表 2.16 中，向 WinJS.xhr() 传递了两个匿名函数：一个 promise 完成函数和一个 promise 错误函数。完成函数在 HTML UI 元素中显示链接列表，而错误页面则向用户显示消息。

注意列表 2.15 中的代码对远程网站发起了请求。这可能会令人惊讶。通常，XMLHttpRequest 对象受同源策略的限制，该策略阻止你从另一个域请求内容。然而，在 Windows Store 应用的上下文中，你没有这种限制。

> 注意：“Internet Explorer 10（以及更早的版本）支持 W3C 跨源资源共享 (CORS) 标准。如果远程服务器返回 HTTP 头部，你就可以对远程服务器发起 Ajax 请求。在 Windows Store 应用的上下文中，你可以忽略 CORS并在不进行任何特殊操作的情况下进行跨源请求。”

注意传递给 WinJS.xhr() 函数的选项对象的第二个参数中，Ajax 请求所使用的 URL。你可以传递以下任何选项：

* type—允许你指定 Ajax 请求中使用的 HTTP 方法。例如，“POST", "GET", "PUT", "DELETE", "HEAD"。
* url—允许你指定发起 Ajax 请求时使用的 URL。

- user—允许你在发起 Ajax 请求时指定凭据。
- Password—允许你在发起 Ajax 请求时指定凭据。
- headers—允许你自定义 Ajax 请求中使用的 HTTP 头部。
- data—允许你指定在 Ajax 请求中传递到远程服务器的数据。可以使用字符串、无符号字节数组，甚至是文档。使用 `JSON.stringify()` 将其他类型的 JavaScript 对象转换为字符串。
- responseType—允许你指定从服务器返回的数据类型。可能的值有 "arraybuffer", "blob", "document", "ms-stream" 或 "text"。
- customRequestInitializer—允许你自定义底层 XmlHttpRequest 对象的属性。

我将在后续章节中详细讨论 `responseType` 和 `customRequestInitializer`。

## 指定不同的响应类型

XMLHttpRequest 对象——因此是 WinJS.xhr() 函数——可以用于返回多种不同类型的数据，包括块、文档和文本。你可以使用 `responseType` 选项来指定你希望返回数据的方式。

`responseType` 的默认值为 "text"。例如，以下请求将把 XML 数据的内容作为字符串返回：

```javascript
var options = {
  url: "http://stephenwalther.com/blog/feed"
};
```

```javascript
WinJS.xhr(options).done(
  function(xhr) {
    var result = xhr.response; // xhr.response 是一个字符串
  }
);
```

你可能并不希望将 XML 文档作为字符串返回，因为这样你就无法使用 `querySelector()` 和 `querySelectorAll()` 等方法从文档中提取元素。相反，你希望将 XML 文档作为文档返回，如下所示：

```javascript
var options = {
  url: "http://stephenwalther.com/blog/feed",
  responseType: "document"
};
```

```javascript
WinJS.xhr(options).done(
  function(xhr) {
    var result = xhr.response; // xhr.response 是一个文档
  }
);
```

注意 options 对象包含一个值为 "document" 的 `responseType` 属性。当你调用 `WinJS.xhr()` 方法时，数据将作为文档而不是字符串返回。这意味着你可以使用 `querySelector()` 和 `querySelectorAll()` 等方法。

注意为了向后兼容，XMLHttpRequest 对象还有 `responseText` 和 `responseXML` 属性。你应该优先使用新属性而不是这些属性。

## 自定义 XMLHttpRequest 的属性

WinJS.xhr() 函数只是 XMLHttpRequest 对象的封装。某些情况下，你可能需要使用 options 没有提供的 XMLHttpRequest 功能。例如，你想利用 customRequestInitializer 来挂进度。

列表 2.17 自定义 XMLHttpRequest (xhr)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>自定义</title>
  <link rel="stylesheet" href="default.css">
</head>
<body>
  <progress id="prgResults" max="100"></progress>
  <div id="divResults"></div>
  <script src="xhrCustom.js"></script>
</body>
</html>
```

```javascript
function () {
  "use strict";

  function initialize() {
    // 缓存元素
    var prgResults = document.getElementById("prgResults");
    var divResults = document.getElementById("divResults");

    // 创建 xhr 
    var options = {
      url: "products.txt",
      customRequestInitializer: function (xhr) {
        xhr.onprogress = function (evt) {
          if (evt.lengthComputable) {
            var percentComplete = (evt.loaded / evt.total) * 100;
            prgResults.value = percentComplete;
          }
        }
      }
    };

    // 执行 Ajax 请求
    WinJS.xhr(options).done(
      function (xhr) {
        divResults.innerHTML = xhr.response;
      }
    );
  }
}
document.addEventListener("DOMContentLoaded", initialize);
```

注意 options 对象有一个 `customRequestInitializer` 属性，它代表一个初始化 XmlHttpRequest 对象的函数。该函数添加了 `onprogress` 处理程序，使用 HTML 元素显示完成的进度。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_88_0.png)

图 2.10 显示 Ajax 请求进度

## 总结

本章的目标是介绍 WinJS 库的功能。在第一节，你学习了如何将 JavaScript 代码组织成模块、命名空间和类。通过利用模块和命名空间，你可以避免全局命名空间并使应用程序更容易维护。

接下来，我讨论了在编写异步代码时如何利用 promise。例如，我讨论了在执行 Ajax 请求时如何使用 promise。你学习了如何创建 promise、取消 promise、链式调用 promise 以及组合新的 promise。

我还讨论了如何使用 WinJS 选择器获取 DOM 元素。你学习了如何使用 `WinJS.Utilities.query()` 使用选择器执行查询并返回查询集。你还学习了如何使用 `WinJS.Utilities.id()` 获取单个元素。

最后，我解释了如何使用 `WinJS.xhr()` 函数在 Windows Store 应用中执行 Ajax 查询。你学习了通过设置 `responseType` 选项来控制 `WinJS.xhr()` 函数返回的数据类型。例如，你学习了如何将 Ajax 查询的结果作为字符串或文档返回。





## 第3 章
## 可观察对象、绑定与模板

在本章中，我将解释如何在 Windows Store 应用程序的页面中显示 JavaScript 对象，例如单个产品或产品数组。

我将首先开始介绍可观察对象（observables）。可观察对象允许你自动检测 JavaScript 属性是否发生了变化。我还会解释如何利用 `WinJS.Binding.List` 对象来检测数组元素的变化。

接下来，我将重点关注声明式数据绑定（declarative data binding）这一主题。我们将学习如何对普通 JavaScript 对象和可观察对象使用声明式数据绑定。

最后，我将讨论如何使用 WinJS 模板显示对象数组。模板允许你同时格式化并显示多个 JavaScript 对象。

## 理解可观察对象

可观察对象是一种对象，当属性值改变时，它可以通知一个或多个监听者。

可观察对象能够让你保持用户界面和应用程序数据的同步。例如，通过利用可观察对象，每当产品属性变化时，你可以自动更新用户界面。可观察对象是 WinJS 库声明式绑定的基础。

> 注意
> WinJS 库并不是第一个支持可观察对象的 JavaScript 库。例如，Backbone、Knockout、Ember 以及 Microsoft Ajax Library（现为 Ajax Control Toolkit 的）都支持可观察对象。

## 创建可观察对象

假设我创建了这样一个产品对象：

```
var product = {
  name: "Milk",
  description: "Something to drink",
  price: 12.33
};
```

这个产品并没有特别奇妙。它有三个名为 name、description 和 price 的属性。

现在，假设我希望在这些属性的任何一个发生变化时自动收到通知。在这种情况下，我可以像这样从我的 product 对象创建一个可观察的产品对象：

```
observableProduct = WinJS.Binding(product);
```

这行代码从现有的名为 `product` 的 JavaScript 对象创建了一个新的 JavaScript 对象 `observableProduct`。这个新对象也具有 name、description 和 price 属性。然而，与原始产品对象的属性不同，可观察产品对象的属性在发生变化时会触发通知。

新可观察产品对象的每个属性都已转换为了访问器属性（accessor properties），这些属性同时具有 getter（get）和 setter（set）。例如，可观察产品的价格看起来像：

```
price: {
  get: function () { return this.getProperty("price"); }
  set: function (value) { this.setProperty("price", value); }
};
```

当你读取 price 属性时，会调用 `getProperty()` 方法；当你设置 price 时，会调用 `setProperty()` 方法。`getProperty()` 和 `setProperty()` 方法都是可观察产品对象的方法。

可观察产品对象支持以下方法：

- addProperty(name, value)——向可观察对象添加新属性并通知所有监听者。
- backingData——一个表示每个属性值的内部对象。
- bind(name, action)——允许在属性发生变化时执行一个函数。
- getProperty(name)——使用属性的字符串名称返回该属性的值。
- notify(name, newValue, oldValue)——一个私有方法，用于执行监听者数组中的每个函数。
- removeProperty(name)——移除一个属性并通知所有监听者。
- setProperty(name, value)——更新一个属性并通知所有监听者。
- unbind(name, action)——允许停止执行响应属性变化而触发的函数。
- updateProperty(name, value)——更新一个属性并通知所有监听者。

所以，当你创建一个可观察对象时，你会得到一个与现有具有相同属性的新对象。然而，当你修改可观察对象的属性时，你可以自动通知该可观察对象的任何监听者特定属性的值已发生变化。

假设你这样更改 price 属性的值：

```
observableProduct.price = 2.99;
```

在这种情况下，会触发以下事件序列：

1. price 的 setter 调用 `setProperty("price", 2.99)` 方法
2. `setProperty()` 方法更新 `backingData.price` 属性的值并调用 `notify()` 方法
3. `notify()` 方法执行与 price 属性关联的监听者集合中的每个函数

当可观察属性被更新时，你可以自动执行一个或多个函数（监听者）。

> 警告
> 如果你在 WinRT 对象上调用 `WinJS.Binding.as()` 方法，将得到异常。问题在于 WinRT 对象是不可变量的，而 `WinJS.Binding.as()` 方法尝试向该不可变对象添加名为 `_getObservable()` 的新方法。你可以让 JavaScript 对象变为可观察的，但不能让 WinRT 对象变为。

## 创建可观察监听者

如果你想在可观察对象的属性发生变化时收到通知，你就需要注册一个监听者。你像列表 3.1 所示，使用 `bind()` 方法注册监听者。

列表 3.1 将对象属性绑定到监听者 (observables\observables.html)

```
// 简单产品对象
var product = {
  name: "Milk",
  description: "Something to drink",
  price: 12.33
};
```

```
// 创建可观察产品
var observableProduct = WinJS.Binding.as(product);
```

```
// 当价格发生变化时执行函数
observableProduct.bind("price", function(newValue, oldValue) {
    console.log(newValue + " was " + oldValue);
});
```

// 修改价格
observableProduct.price = 2.99;
```

在上面的代码中，使用 `bind()` 方法将 price 属性与一个函数关联起来。

> 注意
> 你可以通过向 `WinJS.bind()` 方法的第二个参数提供对象来为复杂属性绑定监听者，如下所示：

```
// 创建具有复杂属性的对象
var customer = {
    shippingAddress: {
        street: "312 Main Street"
    }
};
```

```
// 创建可观察对象
var observableCustomer = WinJS.Binding.as(customer);

// 绑定复杂属性
WinJS.Binding.bind(observableCustomer, {
  shippingAddress: {
    street: function(newValue) {
      console.log("Modified shipping address to "
      + newValue);
    }
  }
});
```

// 修改复杂属性的值
observableCustomer.shippingAddress.street = "100 Grant Street";

## 通知合并

如果你对属性进行多次更改——一个接一个——则不会发送分开的通知。相反，监听者只通知一次。通知会被合并为一次。

例如，在列表 3.2 的代码中，产品的价格属性被更新了三次。然而，JavaScript 控制台只写入了两消息。只有赋值给价格属性的初始值和最后一个值被写入 JavaScript 控制台窗口。

列表 3.2 通知合并 (observablesCoalesce\observablesCoalesce.html)

```
// 简单产品对象
var product = {
  name: "Milk",
  description: "Something to drink",
  price: 12.33
};
```

```
// 创建可观察产品
var observableProduct = WinJS.Binding.as(product);
```

```
// 当价格发生变化时执行函数
observableProduct.bind("price", function(newValue, oldValue) {
  console.log(newValue + " was " + oldValue);
});
```



```javascript
// 修改价格
observableProduct.price = 3.99;
observableProduct.price = 2.99;
observableProduct.price = 1.99;
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_95_0.png)

图 3.2 合并通知

如果属性的更改之间存在时间延迟，那么这些更改将导致不同的通知。

如果你需要防止多个通知被合并为一个——而且你不想创建人为的时间延迟——那么你可以利用 promise（承诺对象）。由于 `updateProperty()` 方法返回一个 promise，你可以使用以下代码为属性的每次更改创建不同的通知：

```javascript
// 修改价格
observableProduct.updateProperty("price", 3.99)
.then(function () {
    observableProduct.updateProperty("price", 2.99)
    .then(function () {
        observableProduct.updateProperty("price", 1.99);
    })
});
```

在这种情况下，尽管价格立即从 3.99 更改到 2.99 再到 1.99，但价格属性的每个新值都会发送单独的通知（参见图 3.3）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_95_1.png)

图 3.3 在 observables 中使用 promises

## 绕过通知

通常，如果可观测对象的属性有监听器且你更改了该属性，监听器就会收到通知。但在某些情况下，你可能希望跳过通知。换句话说，你可能需要静默地更改属性值，而不触发任何注册用于通知的函数。

如果你想在不触发通知的情况下更改属性，你应该通过使用 `backingData` 属性来更改属性。列表 3.3 中的代码说明了如何静默地更改价格属性：

列表 3.3 绕过通知 (observablesBypass.observablesBypass.html)

```javascript
// 简单的产品对象
var product = {
  name: "Milk",
  description: "Something to drink",
  price: 12.33
}

// 创建可观测对象
var observableProduct = WinJS.Binding.as(product)

// 当价格更改时执行函数
observableProduct.bind("price", function (newValue) {
  console.log(newValue);
});

// 静默更改价格
observableProduct.backingData.price = 5.99;
console.log(observableProduct.price); // 写入 5.99
```

通过更改 `backingData.price` 的值将价格更改为 5.99。由于没有直接设置 `observableProduct.price` 属性，与价格属性关联的监听器不会通知。

当你使用 `backingData` 属性更改属性值时，属性的更改是同步完成的。然而，当你直接更改可观测属性的值时，更改始终是异步的。

## 使用 WinJS.Binding.List 对象

如果你希望在项目数组发生任何更改时收到通知——换句话说，你想与可观测集合一起——那么你应该使用 `WinJS.Binding.List` 对象。

`WinJS.Binding.List` 对象将标准的 JavaScript 数组封装在一个新对象中，并添加了额外的方法和事件以支持更改通知。`WinJS.Binding.List` 对象支持以下事件：

- iteminserted——当向列表添加新项时触发。
- itemchanged——当使用 `setState()` 方法替换列表中的项时触发。
- itemremove——当使用 `move()` 方法移动列表中的项时触发。
- itemmutated——通过调用 `notifyMutated()` 方法触发。
- itemremove——通过从列表中删除项时触发。
- reload——通过调用 `sort()` 或 `reverse()` 重新排序列表中的项触发。也可以通过调用 `notifyReload()` 方法触发。

列表 3.4 中的代码演示了你如何触发这些事件中的每一个，以及传递给每个事件处理程序的信息。

列表 3.4 使用 WinJS.Binding.List (observablesList\observablesList.html)

```javascript
var products = [
  { name: "Milk", price: 2.99 },
  { name: "Oranges", price: 2.50 },
  { name: "Apples", price: 1.99 }
];

// 创建 List
var productsList = new WinJS.Binding.List(products);

// 设置事件处理器
productsList.oniteminserted = function (evt) {
  var message = "Item Inserted: " + evt.detail.value.name
  + " at index " + evt.detail.index
  + " with key " + evt.detail.key;
  console.log(message);
};

productsList.onitemchanged = function (evt) {
  var message = "Item Changed: " + evt.detail.oldValue.name
  + " to " + evt.detail.newValue.name
  + " at index " + evt.detail.index
  + " with key " + evt.detail.key;
  console.log(message);
};

productsList.onitemmutated = function (evt) {
  var message = "Item Mutated: " + evt.detail.value.name
  + " with key " + evt.detail.key;
  console.log(message);
};

productsList.onitemremove = function (evt) {
  var message = "Item Removed: " + evt.detail.value.name
  + " at index " + evt.detail.index
  + " with key " + evt.detail.key;
  console.log(message);
};

productsList.onitemmoved = function (evt) {
  var message = "Item Moved: " + evt.detail.value.name
  + " from index " + evt.detail.oldIndex
  + " to index " + evt.detail.newIndex
  + " with key " + evt.detail.key;
  console.log(message);
};

productsList.onload = function (evt) {
  var message = "List Reloaded";
  console.log(message);
};
```
*(注：原文中 itemremove 出现了两次，根据语境一处应对应删除项逻辑)*




你可以使用 `data-win-bind` 属性将 HTML 元素的（几乎）任何属性绑定到 JavaScript 属性的值。例如，特斯拉的图片通过将值绑定到 `IMG` 元素的 `src` 和 `alt` 属性来显示：

```
<img data-win-bind="src:photo;alt:name" />
```

注意，`data-win-bind` 属性使用分号分隔的 HTML 属性名称和 JavaScript 对象名称列表。

> 声明式绑定无法使用的唯一属性是 `ID` 属性。默认情况下，WinJS 库会自动为每个元素生成唯一的 ID。你可以通过将 `optimizeBindingReferences` 属性设置为 `false` 来禁用此行为。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_101_0.png)

图 3.5 使用声明式数据绑定显示产品详情

列表 3.6 中的代码包含了列表 3.5 中 HTML 页面显示的商品。

列表 3.6 简单声明式数据绑定 (data\data.js)

```javascript
function () {
  "use strict";

  function initialize() {
```

## 理解声明式数据绑定

```javascript
var product = {
  name: "Tesla Roadster",
  price: 34,
  photo: "tesla.jpg"
};

WinJS.Binding.processAll(null, product);

document.addEventListener("DOMContentLoaded", initialize);

```

列表 3.6 中的 `product` 对象并没有特别之处——它只是一个普通的 JavaScript 对象。

注意列表 3.6 中对 `WinJS.Binding.processAll()` 的调用。页面中的声明式数据绑定属性在调用此方法之前是不会处理的。当你调用 `WinJS.Binding.processAll()` 方法时，你必须指定两个参数：根元素和数据上下文。

根元素决定了页面中哪些元素会被处理。如果你传递 `null`，则会整个整个文档进行解析。

数据上下文包含了你想要绑定到 HTML 属性的数据。在列表 3.6 中，`product` 对象作为数据上下文传递给 `WinJS.Binding.processAll()` 方法。

> 警告
> 在包含 HTML 元素的文档加载之前，不要调用 `WinJS.Binding.processAll()`。否则，没有任何内容需要处理。在列表 3.6 中，`WinJS.Binding.processAll()` 方法是在由 `DOMContentLoaded` 事件触发的函数内部调用的。

## 声明式数据绑定与可观察

声明式数据绑定和可观察（Observables）是一个强大的组合。如果你在数据绑定中使用可观察对象，那么每当你更改底层 JavaScript 对象时，就可以自动更新 HTML 文档的内容。

例如，列表 3.7 中的 HTML 页面包含一个 `SPAN` 和一个 `BUTTON` 元素。页面显示按钮被点击的次数（见图 3.6）。

（你点击了它）按钮点击 3 次。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_103_0.png)

图 3.6 显示点击计数

列表 3.7 使用可观察对象数据绑定 (dataBindingObservables\dataBindingObservables.html)

```html
<html>
<head>
  <meta charset="UTF-8" />
  <title>Chapter03</title>

  <!-- WinJS references --
  <link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="//Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="//Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- Chapter03 references --
  <link href="css/default.css" rel="stylesheet" />
  <script src="dataBindingObservables.js"></script>
</head>
<body>

<div>
  你点击了按钮
  <span data-win-bind="innerText:timesClicked"></span> 次。
  <br />
  <button data-win-bind="onclick:click">点击这里！</button>
</div>

</body>
</html>
```

注意列表 3.7 中的页面包含了两个 `data-win-bind` 属性。第一个 `data-win-bind` 属性用于 `SPAN` 元素以显示点击计数，第二个 `data-win-bind` 属性用于 `BUTTON` 元素以处理点击事件。

列表 3.8 中的 JavaScript 代码包含一个名为 `viewModel` 的可观察对象，它跟踪点击计数。

列表 3.8 使用可观察对象数据绑定 (dataBindingObservables\dataBindingObservables.html)

```javascript
function () {
  "use strict";

  function initialize() {
    // 创建一个视图模型
    var viewModel = {
      timesClicked: 0,
      click: function (evt) {
        evt.preventDefault();
        viewModel.timesClicked++;
      }
  }

    // 使视图模型变为可观察
    viewModel = WinJS.Binding.as(viewModel);

    // 将视图模型绑定到文档
    WinJS.Binding.processAll(null, viewModel);
  }

document.addEventListener("DOMContentLoaded", initialize);
}();
```

列表 3.8 中的 `viewModel` 拥有属性 `timesClicked`，用于更新按钮被点击的次数。通过 `WinJS.Binding.as()` 方法的帮助，`viewModel` 被转换为可观察对象。最后，通过调用 `WinJS.Binding.processAll()` 将 `viewModel` 绑定到页面。

## 获取 HTML 表单的内容

WinJS 库不支持双向绑定。如果你想获取 HTML 表单的内容，你需要自己完成获取值的工作。列表 3.9 中的页面包含了创建新产品的 HTML（见图 3.7）。表单使用单个 `data-win-bind` 属性来接接提交处理器。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_105_0.png)

图 3.7 创建新产品

列表 3.9 双向数据绑定 (dataBindingWay\dataBindingWay.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Chapter03</title>
  <!-- WinJS references --
  <link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="//Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="//Microsoft.WinJS.1.0/js/ui.js"></script>
  <!-- Chapter03 references --
  <link href="css/default.css" rel="stylesheet" />
  <script src="dataBindingWay.js"></script>
</head>
<body>
<form data-win-bind="onsubmit:submit">
<div class="field">
<label>名称:</label>
<input id="productName" required />
</div>
<div class="field">
<label>价格:</label>
<input id="productPrice" required />
</div>
<div class="field">
<button>添加产品</button>
</div>
</form>
</body>
</html>
```

## 理解声明式数据绑定

当提交 HTML 表单时，列表 3.10 中的 `viewModel.submit()` 方法会被调用。该方法获取 HTML 表单字段并创建一个名为 `productToAdd` 的新产品对象。

列表 3.10 双向数据绑定 (dataBindingWay\dataBindingWay)

```javascript
(function () {
  "use strict";

  function initialize() {
    var viewModel = {
      submit: function (evt) {
        // 防止页面提交
        evt.preventDefault();

        // 获取表单字段
        var productToAdd = {
          name: document.getElementById("productName").value,
          price: document.getElementById("productPrice").value
        };

        // TODO: 将新产品添加到数据库
      }
    };

    WinJS.Binding.processAll(null, viewModel);
  }
  document.addEventListener("DOMContentLoaded", initialize);
})()
```

为什么要使用声明式数据绑定？使用声明式绑定连接事件处理器的优势在于你不需要通过命名空间暴露处理器。在使用声明式绑定时，处理器不需要是公共方法——唯一的要求是它是 `WinJS.Binding.processAll()` 方法所用数据上下文的一部分。




# 第 3 章 观察者、绑定与模板

> 注意
列表 3.9 中的 HTML 表单使用了 HTML5 的 `required` 属性，以确保在 name 和 price 的 INPUT 元素中输入了值。

## 声明式数据绑定与 WinJS 控制

我们将在下一章详细讨论 WinJS 控制；然而，我想确保你理解，你可以像对元素属性使用声明式数据绑定一样，在 WinJS 控制属性上使用声明式数据绑定。

技巧是使用由每个 HTML 元素暴露的 `winControl` 属性，该属性与控件相关联。你可以配合 `data-win-bind` 属性使用 `winControl` 属性。

例如，列表 3.11 中的页面包含一个 WinJS Rating 控件（见图 3.8）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_107_0.png)

图 3.8 使用声明式数据绑定显示平均评分

列表 3.11 在 WinJS 控制上使用声明式数据绑定 (dataBindingControls\dataBindingControls.html)

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<title>Chapter03</title>
<!-- WinJS references -->
<link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="//Microsoft.WinJS.1.0/js/base.js"></script>
<script src="//Microsoft.WinJS.1.0/js/ui.js"></script>
<!-- Chapter03 references -->
<link href="//css/default.css" rel="stylesheet" />
<script src="dataBindingControls.js"></script>
</head>
<body>
<div data-win-control="WinJS.UI.Rating" data-win-bind="winControl.averageRating:averageRating"></</div>>
<div>
  该产品的平均评分是：
  <span data-win-bind="innerText:averageRating"></span>
</div>
</body>
</html>
```

列表 3.11 包含一个 WinJS Rating 控件。WinJS Rating 控件的 `averageRating` 属性通过以下 `data-win-bind` 属性设置：

```
data-win-bind="winControl.averageRating:averageRating"
```

`winControl` 属性带你从 HTML 元素到其关联的控件。列表 3.12 中的 JavaScript 文件说明了你如何将平均评分绑定到 Rating 控件。

列表 3.12 在 WinJS 控制上使用声明式数据绑定 (dataBindingControls.js)

```javascript
(function () {
  "use strict";

  function initialize() {

    // 创建一个视图模型
    var viewModel = {
      averageRating: 3
    };

    // 将视图模型绑定到文档
    WinJS.UI.processAll()
    .done(function () {
      WinJS.Binding.processAll(null, viewModel);
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}
();
```

列表 3.12 中的代码包含了两次对 `processAll()` 方法的调用。首先，调用 `WinJS.UI.processAll()` 方法处理页面中所有的 WinJS 控件。接下来，调用 `WinJS.Binding.processAll()` 方法处理页面中所有的数据绑定属性。你必须按照该顺序调用这两个 `processAll()` 方法，否则将没有带属性可以绑定的控件。

## 声明式数据绑定与绑定转换器

绑定转换器（Binding converters）允许你在使用 `data-win-bind` 属性中的属性时，转换该属性的值。

在很多情况下，绑定转换器非常有用；例如，格式化日期和时间，或者根据属性值隐藏或显示内容。每当你需要在显示之前使用 JavaScript 属性值时，请使用绑定转换器。

例如，假设你只想在产品促销中时才显示“促销中！”文本。列表 3.13 中的页面显示了两个产品（见图 3.9）。它使用绑定转换器来隐藏或显示包含“促销中！”文本的 DIV 元素的内容。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_109_0.png)

图 3.9 使用绑定转换器

列表 3.13 使用绑定转换器 (dataBindingConverters/dataBindingConverters.html)

```html
<!DOCTYPE html>
<html
<head>
<meta charset="utf-8" />
<title>Chapter03</title>

<!-- WinJS references -->
<link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="//Microsoft.WinJS.1.0/js/base.js"></script>
<script src="//Microsoft.WinJS.1.0/js/ui.js"></script>
<!-- Chapter03 references -->
<link href="//css/default.css" rel="stylesheet" />
<script src="dataBindingConverters.js"></script>
</head>
<body>
```
（注：由于原文文本在 HTML 代码部分存在严重的错乱和重复，译文已根据上下文逻辑进行了重组和修正，以确保符合文档工程师的专业输出标准并遵循“不要重复输出原文”的原则。）





## 列表 3.17 使用日期和价格转换器

```html
<div>
<h1 data-win-bind="innerText:product1.name"></h1>
<div>
  价格:
  <span data-win-bind="innerText:product1.price">MyBindingConverters.price</span></span>
</div>
<div>
  可用日期:
  <span data-win-bind="innerText:product1.dateAvailable">MyBindingConverters.shortdate</span></span>
</div>
</div>
</div>
```

价格转换器使产品显示为 $100.00 而不是 99.99999。`shortDate` 转换器使 `dateAvailable` 属性显示为 12/25/2012 而不是 Tue Dec 25 00:00:00 PST。

> 遗憾的是，在使用绑定转换器时无法传递额外的参数。如果可以传递额外的参数（例如代表日期格式的参数）就太好了。但你无法这样做。相反，你必须创建单独 `dateShort` 和 `dateLong` 绑定转换器。

## 理解模板

如果你需要在页面中多次显示同一个 HTML 片段，你应该创建一个模板。模板是一个可以包含声明式数据绑定表达式的 HTML 片段。创建模板有两种方法：命令式和声明式。

## 创建命令式模板

假设你想要在 HTML 页面中显示产品数组。在这种情况下，你可以使用模板来格式化数组中的每个产品（见图 3.10）。

| 名字 | 价格 |
|--- |--- |
| tmpl | $20000 |
| BMW | $19000 |
| hert | $9600 |

**图 3.10** 使用模板显示产品列表

列表 3.18 中的 HTML 页面包含一个名为 `tmplProduct` 的 DIV 元素。该 DIV 元素在页面渲染时不会被显示。相反，它包含了模板的内容。

页面还包含另一个名为 `conProducts` 的 DIV 元素。该 DIV 元素充当模板的目标容器。当每个产品被渲染时，它会被渲染到 `conProducts` DIV 元素中。

**代码列表 3.18** 创建命令式模板 (templatesImperative|templatesImperative.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Chapter03</title>

  <!-- WinJS 引用 -->
  <link href="http://Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="http://Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="http://Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- Chapter03 引用 -->
  <link href="templatesImperative.css" rel="stylesheet" />
  <script src="templatesImperative.js"></script>
</head>
<body>
  <!-- 模板 -->
  <div id="tmplProduct">
    <div class="product">
      名字: <span data-win-bind="innerText:name"></</span>
      <br />
      价格: <span data-win-bind="innerText:price"></</span>
```

```html
</div>
</div>

<!-- 模板渲染的位置 -->
<div id="conProducts"></div>

</</body>>
</html>
```

列表 3.19 中的 JavaScript 代码说明了你如何创建一个新模板并为数组中的每个项渲染模板。

列表 3.19 创建命令式模板 (templatesImperative\templatesImperative.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    var products = [
      { name: "Tesla", price: 300000 },
      { name: "BMW", price: 80000 },
      { name: "Pinto", price: 10000 }
    ];

    // 获取模板和容器
    var tmplProduct = document.getElementById("tmplProduct");
    var conProducts = document.getElementById("conProducts");

    // 创建模板
    var template = new WinJS.Binding.Template(tmplProduct);

    // 使用模板渲染数组中的每一项
    products.forEach(function (product) {
      template.render(product, conProducts);
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}
)
```

模板是通过创建 WinJS Template 控制的新实例创建的：

```javascript
var template = new WinJS.Binding.Template(tmplProduct)
```

接下来，在 `foreach()` 方法中为数组中的每个项渲染模板：

```javascript
products.forEach(function (product) {
  template.render(product, conProducts);
});
```

当模板被渲染时，每个数据项只会渲染模板的内部内容。包含它的的 DIV 元素（在之前的代码中名为 `tmplProduct`）不会被渲染。

## 创建声明式模板

如果你愿意，可以以声明式而非命令式来创建模板。列表 3.20 中的页面包含一个与 `tmplProduct` DIV 元素关联的 WinJS Template 控件。

- 列表 3.20 声明式创建模板 (templatesDeclare\templatesDeclare.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Chapter03</title>

  <!-- WinJS 引用 -->
  <link href="http://Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="http://Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="http://Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- Chapter03 引用 -->
  <link href="templatesDeclare.css" rel="stylesheet" />
  <script src="templatesDeclare.js"></script>
</head>
<body>
  <!-- 模板 -->
<div id="tmplProduct" data-control="WinJS.Binding.Template">
    <div class="product">
      名字: <span data-win-bind="innerText:name"></</span>
      <br />
      价格: <span data-win-bind="innerText:price"></</span>
    </div>
  </div>
</div>

<!-- 模板渲染的位置 -->
<div id="conProducts"></div>
</</body>>
</html>
```

```在列表 3.20 中，模板控件通过 `data-control="WinJS.Binding.Template"` 属性声明。列表 3.21 包含了用于渲染数组的 JavaScript 代码。

列表 3.21 声明式创建模板 (templatesDeclare.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    var products = [
      { name: "Tesla", price: 300000 },
      { name: "BMW", price: 80000 },
      { name: "Pinto", price: 10000 }
    ];

    // 获取模板和容器
    var tmplProduct = document.getElementById("tmplProduct");
    var conProducts = document.getElementById("conProducts");

    // 使用模板渲染
    WinJS.processAll().done(function () {
      products.forEach(function (product) {
        tmplProduct.render(product, conProducts);
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}
```

使用声明式模板时，必须调用 `WinJS.processAll()` 方法。否则，DIV 元素不会转换为模板。

## 使用选择器应用模板

查询集合包含 `template()` 方法，你可以使用它将模板应用到单个元素或一组 DOM 元素。例如，列表 3.22 显示了产品列表。

- 列表 3.22 使用 WinJS.id() 应用模板 (templatesQuery\templatesQuery.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Chapter03</title>

  <!-- WinJS 引用 -->
  <link href="http://Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="http://Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="http://Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- Chapter03 引用 -->
  <link href="templatesQuery.css" rel="stylesheet" />
  <script src="templatesQuery.js"></script>
</head>
<body>
  <!-- 模板 -->
<div id="tmplProduct" data-control="WinJS.Binding.Template">
    <div class="product">
      名字: <span data-win-bind="innerText:name"></</span>
      <br />
      价格: <span data-win-bind="innerText:price"></</span>
    </div>
  </div>
</div>

<!-- 模板渲染的位置 -->
<div id="conProducts"></div>
</</body>>
</html>
```

列表 3.23 中的 JavaScript 代码演示了你如何使用 `WinJS.Utilities.id()` 方法将模板应用到 `conProducts` DIV 元素。

列表 3.23 使用 WinJS.id() 应用模板 (templatesQuery\ntamplesQuery.js)

```javascript
(function () {
  "use strict";
```





```javascript
function initialize() {

  var products = [
    { name: "Tesla", price: 300000 },
    { name: "BMW", price: 80000 },
    { name: "Pinto", price: 10000 }
  ];

  WinJS.UI.processAll().done(function () {
    var tmplProduct = document.getElementById("tmplProduct");
    WinJS.Utilities.dom("products").template(tmplProduct, products);
  });

  document.addEventListener("DOMContentLoaded", initialize);
}
();
```

注意，当您使用查询集合模板 `template()` 方法时，不需要调用 `forEach()`。该方法会在内部执行 `forEach()`。

## 创建外部模板

如果你想在多个页面中使用同一个模板，那么创建一个外部模板是有意义的。换句话说，你可以将模板放置在包含模板的页面单独文件中。

以下是如何声明一个 Template 控件使其引用外部模板文件。注意下面的 Template 包含一个 `href` 选项，指向名为 `productTemplate.html` 的文件。

```html
<!-- Template -->
<div id="tmplProduct"
  data-win-control="WinJS.Binding.Template"
  data-win-options="{
    href:'productTemplate.html'
  }">
</div>
```

`productTemplate.html` 包含了产品模板，内容如下：

```html
<div class="product">
  Name:<span data-win-bind="innerText:name"></span>
  <br />
  Price:<span data-win-bind="innerText:price"></span>
</div>
```

最后，列表 3.24 包含了用于渲染外部模板的 JavaScript 代码。

# 列表 3.24 渲染外部模板

```javascript
function (function () {
  "use strict";

  function initialize() {
    var products = [
      { name: "Tesla", price: 300000 },
      { name: "BMW", price: 80000 },
      { name: "Pinto", price: 10000 }
    ];

    // 获取模板和模板容器
    var tmplProduct = document.getElementById("tmplProduct");
    var conProducts = document.getElementById("conProducts");

    // 使用模板渲染每个数组项
    WinJS.UI.processAll().done(function () {
      tmplProduct.render({{}}).then(function () {

        products.forEach(function (product) {
          tmplProduct.winControl.render(product, conProducts);
        });
      });
    });
  }
  document.addEventListener("DOMContentLoaded", initialize);
})();
```

你可以从位于不同页面的多个 Template 控件中引用同一个 `productTemplate.html`。

> 注意
> 在列表 3.24 中，调用 `render()` 方法时传入了一个空对象，如下：
> tmplProduct.winControl.render({{}}).then(function () {});

这样做是为了绕过 WinJS 库中的一个已知 bug。

## 总结

本章主要关于如何在页面中显示 JavaScript 对象。在第一节中，你学习了观察对象（observables）。特别是，你学习了观察对象如何让你能够自动检测 JavaScript 对象的属性变化。我们还讨论了如何使用 `WinJS.Binding.List` 对象来检测项目数组中不同类型的变化。

接下来，你学习了如何利用普通 JavaScript 对象和观察性 JavaScript 对象的声明式数据绑定，在页面中显示 JavaScript 属性的值。

最后，我讨论了如何使用 WinJS 模板来格式化和显示对象数组。你学习了如何通过命令式和声明式创建模板。

# 第 4 章
使用 WinJS 控件

本章的目标是为你提供 WinJS 库中包含的控件的概述。我首先解释如何向你的页面添加控件。你将学习如何通过声明式和命令式创建 WinJS 控件并设置选项。

本章的大部分在于描述和示例如何使用 WinJS 库包含的基础控件。在本章中，我重点描述了如何使用以下控件：

- Tooltip——用于显示弹出提示框。
- ToggleSwitch（切换开关）——用于显示切换开关，可在与复选框相同的场景中使用。
- Rating（评分）——用于显示和输入用户评分。
- DatePicker（日期选择器）——用于输入日期。
- TimePicker（时间选择器）——用于输入时间。
- FlipView（翻页）——用于显示集合中某一项的详情。

# WinJS 控件简介

你通过使用 `data-win-control` 属性在页面声明 WinJS 控件。例如，你可以通过向页面添加以下 DIV 元素来声明 WinJS DatePicker 控件：

```html
<div id="dateBirthday"
  data-win-control="WinJS.UI.DatePicker"></div>
```

## 本章内容
- WinJS 控件简介
- 使用 tooltip 控件
- 使用 ToggleSwitch 控件
- 使用 Rating 控件
- 使用控件
- 使用 TimePicker 控件
- 使用 FlipView 控件

该 DIV 元素并没有执行任何操作。它只是作为控件的占位符。它是 DatePicker 控件的“宿主”。`data-win-control` 属性用于指示与元素关联的控件类型。

在调用 `WinJS.ui.processAll()` 方法之前，WinJS 实际上不会变成控件。该方法解析 HTML 文档，识别任何包含 `data-win-control` 属性的元素，并为它们生成控件。

WinJS 控件还有一个重要要求：必须包含正确的 JavaScript 和样式表文件。为了使用任何控件，你必须在 HTML 顶部添加以下三个引用：

```html
<link href="Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="Microsoft.WinJS.1.0/js/base.js"></script>
<script src="Microsoft.WinJS.1.0/js/ui.js"></script>
```

第一个引用是名为 `ui-dark.css` 的样式表。WinJS 库包含两个样式表：`ui-dark.css` 和 `ui-light.css`。如果你用 `ui-light.css` 引用替换 `ui-dark.css` 引用，就可以为所有控件使用浅色主题。

（此处省略后续重复内容）

你通过使用 `data-win-control` 属性在页面声明 WinJS 控件。例如，你可以通过向页面添加以下 DIV 元素来声明 WinJS DatePicker 控件：

```html
<div id="dateBirthday"
  data-win-control="WinJS.UI.DatePicker"></div>
```

该 DIV 元素并没有执行任何操作。它只是作为控件的占位符。它是 DatePicker 控件的“宿主”。`data-win-control` 属性用于指示与元素关联的控件类型。

在调用 `WinJS.ui.processAll()` 方法之前，WinJS 实际上不会变成控件。该方法解析 HTML 文档，识别任何包含 `data-win-control` 属性的元素，并为它们生成控件。

WinJS 控件还有一个重要要求：必须包含正确的 JavaScript 和样式表文件。为了使用任何控件，你必须在 HTML 顶部添加以下三个引用：

```html
<link href="Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="Microsoft.WinJS.1.0/js/base.js"></script>
<script src="Microsoft.WinJS.1.0/js/ui.js"></script>
```

第一个引用是名为 `ui-dark.css` 的样式表。WinJS 库包含两个样式表：`ui-dark.css` 和 `ui-light.css`。如果你用 `ui-light.css` 引用替换 `ui-dark.css` 引用，就可以为所有控件使用浅色主题。

## 声明式创建 WinJS 控件

你有两种方式创建 WinJS 控件：声明式和命令式。列表 4.1 中的 HTML 页面演示了如何声明式创建 WinJS 控件：

# 列表 4.1 声明 WinJS 控件 (declarative.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Chapter04</title>

<!-- WinJS 引用 -->
  <link href="//ui-dark.css" rel="stylesheet" />
  <script src="//base.js"></script>
  <script src="//ui.js"></script>

<!-- Chapter04 引用 -->
  <link href="//default.css" rel="stylesheet" />
  <script src="//declarative.js"></script>
</head>
<body>
  <div id="dateBirthday"
    data-win-control="WinJS.UI.DatePicker"></div>
</body>
</html>
```

在列表 4.1 中，DatePicker 控件被声明在 HTML 页面的 body 部分。注意页面包含了 `ui-dark.css`、`base.js` 和 `ui.js` 文件的引用：使用 WinJS 控件所需的所有文件引用。

页面还包含了对名为 `declarative.js` 文件的引用。该文件包含了与页面相关的自定义 JavaScript 代码。`declarative.js` 文件的内容在列表 4.2 中。

# 列表 4.2 声明 WinJS 控件 (declarative.js)

```javascript
function (function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll();
  }

  document.addEventListener("DOMContentLoaded", initialize);
}
```





# WinJS 控件简介

列表 4.2 包含了对 `WinJS.UI.processAll()` 方法的调用。如果你忘记调用此方法（这非常容易），那么 HTML 页面中声明的控件将不会转换为控件。

请注意，对 `WinJS.UI.processAll()` 的调用发生在 `initialize()` 方法中，该方法在 `DOMContentLoaded` 事件触发之前不会被调用。`DOMContentLoaded` 事件在 HTML 文档加载后发生。你必须在调用 `WinJS.UI.processAll()` 之前等待文档加载，否则将没有任何可以处理的内容。

## 命令式创建控件

在上一节中，我以声明的方式创建了 `DatePicker` 控件的实例。我在页面的 HTML 标记中声明了该控件。

作为声明式创建 WinJS 控件的替代方案，你也可以命令式创建控件。也就是说，你完全可以在你的 JavaScript 代码中创建控件。

考虑列表 4.3 中的页面。它包含一个 id 为 `dateBirthday` 的 DIV 元素。该 DIV 元素没有 `data-win-control` 属性。

列表 4.3 命令式创建 WinJS 控件 (controlImperative\controlImperative)

```html
<!DOCTYPE html>
<html
<head>
  <meta charset="utf-8" />
  <title>Chapter04</title>

  <!-- WinJS references --
  <link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="//Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="//Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- Chapter04 references --
  <link href="//css/default.css" rel="stylesheet" />
  <script src="controlImperative.js"></script>
</head>
<body>

  <div id="dateBirthday"></div>
</body>
</html>
```

列表 4.4 中的代码创建了一个 `DatePicker` 控件，并将新控件与 `dateBirthday` DIV 元素关联起来。

# 列表 4.4 命令式创建 WinJS 控件 (controlimperative\controlimperative.js)

```javascript
function () {
  "use strict";

  function initialize() {
    var dateBirthday = document.getElementById("dateBirthday");
    var ctlBirthday = new WinJS.UI.DatePicker(dateBirthday);
  }

  document.addEventListener("DOMContentLoaded", initialize);
}();
```

列表 4.4 中的代码创建了 JavaScript `WinJS.UI.DatePicker` 类的新实例。`DatePicker` 类是通过将 `dateBirthday` DIV 元素传递给 `DatePicker` 类的构造函数创建的。注意，你不需要调用 `WinJS.processAll()`，因为在命令式创建 WinJS 控件时不需要传递文档。

列表 4.4 中的代码阐述了一个事实：WinJS 控件本质就是一个 JavaScript 类。你可以通过 `data-win-control` 属性声明式地创建，也可以通过在代码中实例化来命令式地创建。但归结底，它们都是 JavaScript 类。

在本书中，采用声明式而不是命令式来创建控件。这两种方法都没有错。然而，由于微软的示例倾向于声明式方法，我将遵循微软的做法，也使用声明式方法。

## 设置控件选项

大多数控件支持选项。例如：

你可以利用 `data-win-options` 属性声明式地指定控件。例如，下面的 HTML 代码段演示了如何设置 `TimePicker` 控件显示的当前时间为 `3:04pm`，并将时钟格式设置为 24 小时制：

```html
<div id="timeLunch"
  data-win-control="WinJS.UI.TimePicker"
  data-win-options="{
  current: '3:04pm',
  clock: '24HourClock'
}"></div
```

传递给控件的选项对象是一个 JavaScript 对象——因此在属性名和值周围使用了大括号。

# WinJS 控件简介

如果你愿意，可以命令式地设置这些选项。以下是如何在代码中创建 `TimePicker` 控件实例并设置其当前和时钟选项的方法：

```javascript
function () {
  "use strict";

  function initialize() {
    var divLunch = document.getElementById("timeLunch");
    var ctrlLunch = new WinJS.UI.TimePicker(timeLunch, {
      current: '3:04pm',
      clock: '24HourClock'
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}();
```

选项作为第二个参数传递给 `TimePicker` 构造函数。当前时间和时钟选项已设置完毕。

> **注意**
> 你也可以利用 `WinJS.UI.options()` 方法来命令式地设置控件选项。你可以在控件构造完成后调用 `setOptions()` 方法。

## 从 HTML 获取控件

当控件被创建时，它会与一个 DOM 元素关联。你可以使用 `winControl` 属性从其 HTML 元素中获取控件。例如，如果你像这样声明式声明 `DatePicker`：

```html
<div id="dateBirthday"
  data-win-control="WinJS.UI.DatePicker"></div
```

你可以像这样在你的 JavaScript 代码中获取控件：

```javascript
function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      var ctlBirthday = document.getElementById("dateBirthday").winControl;
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}();
```

## 使用 Tooltip 控件

你可以使用 WinJS Tooltip 控件在任何元素上显示自定义的工具框（见图 4.4）。当悬停在元素上时，工具框会出现几秒钟。当你将光标移开元素时，工具框就会消失。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_129_0.png)

图 4.4 使用 Tooltip 显示工具框 (tooltip.html)

你像这样在页面中声明 Tooltip 控件：

```html
<button id="btnDelete"
  data-win-control="WinJS.UI.Tooltip"
  data-win-options="innerHTML: 'Deletes <b>record</b> from the database'}">Delete</button
```

> **警告**
> 记得调用 `WinJS.UI.processAll()` 方法，否则 Tooltip 控件与其他任何控件一样不会出现。

注意你使用 `innerHTML` 选项来设置工具框的文本，该文本可以包含 HTML。

## 使用 contentElement 属性

如果你有大量的 HTML 内容显示（见图 4.5），你可以像这样将工具框内容放在单独的元素中：

```html
<button id="btnDelete"
  data-win-control="WinJS.UI.Tooltip"
  data-win-options="{
    contentElement: '#btnDeleteTooltip'
  }"></button

<div style="display:none">
  <div id="BtnDeleteTooltip">
    从数据库中删除 <p/>。你*真的，真的想*要这么做吗？该记录将永远消失，你可能会流泪。
  </div>
</div>
```

`contentElement` 选项用于指定一个包含工具框 HTML 内容的单独元素。在上面的代码中，工具框的内容包含 id 为 `btnDeleteTooltip` 的 DIV 元素中。

注意 `btnDeleteTooltip` 被在一个具有 `style="display:none"` 属性的 DIV 元素中。这个外部 DIV 元素用于防止 `btnDeleteTooltip` 的内容在页面上显示。你希望 `contentElement` 的内容只在工具框中出现。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_130_0.png)

图 4.5 显示长工具框

## Tooltip 样式

由于 HTML 已经包含了一个工具提示属性，你可能疑惑为什么微软引入了 WinJS Tooltip 控件。这完全是为了自定义。你可以创建与你的 Windows 应用风格匹配的工具框。

你可以通过修改 `win-tooltip` 样式表类来自定义 Tooltip 控件的外观。例如，图 4.6 描述了当你定义了 `win-tooltip` 样式时 Tooltip 控件的显示。





# 第 4 章 使用 WinJS 

```css
.win-tooltip {
  background-color: #ffd800;
  border: solid 2px red;
  border-radius: 15px;
}
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_131_0.png)

图 4.6 自定义工具提示（tooltip）的外观

## 使用 ToggleSwitch 控制

你可以在与使用标准 HTML 复选框（<input type="checkbox">）相同的情况下使用 WinJS ToggleSwitch 控制。ToggleSwitch 控制与复选框控制之间的区别在于 ToggleSwitch 更符合指部操作：你可以在 ToggleSwitch 上滑动手指来勾选或取消勾选它（见图 4.7 和 4.8）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_131_1.png)

图 4.7 一个被勾选的 ToggleSwitch

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_131_2.png)

图 4.8 一个未勾选的 ToggleSwitch

以下是如何在页面中声明 ToggleSwitch 控制的：

```html
<div
  data-win-control="WinJS.UI.ToggleSwitch"
  data-win-options='{
    title: 'Flux Capacitor State',
    labeloff: 'Disabled',
    labelOn: 'Enabled',
    checked: true
  }'></div>
```

## ToggleSwitch 的状态

你可以通过读取 ToggleSwitch 控制的 `checked` 属性来检测 ToggleSwitch 控制处于勾选还是未勾选状态。例如，列表 4.5 中的页面包含一个 ToggleSwitch 控制和一个 DIV 元素，该元素会根据 ToggleSwitch 控制的状态显示不同的消息（见图 4.9）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_132_0.png)

图 4.9 根据 ToggleSwitch 的状态显示消息

### 列表 4.5 使用 ToggleSwitch 控制 (toggleSwitchChecked/toggleSwitchChecked)

```html
<div id="flux"
  data-win-control="WinJS.UI.ToggleSwitch"
  data-win-options="{
    title: 'Flux Capacitor State',
    labelOff: 'Disabled',
    labelOn: 'Enabled',
    checked: true
  }"></div>

<div id="divMessage"></div>
```

列表 4.6 中的代码为 ToggleSwitch 控制接线了一个事件处理程序。当你更改 ToggleSwitch 控制的状态时，就会调用该处理程序。该处理器在 DIV 元素中显示两条消息中的一条。

### 列表 4.6 使用 ToggleSwitch 控制 (toggleSwitchChecked/toggleSwitchChecked)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {

      var togFlux = document.getElementById("flux").winControl;
      var divMessage = document.getElementById("divMessage");

      togFlux.addEventListener("change", function (evt) {
        if (togFlux.checked)
          divMessage.innerHTML = "Flux Capacitor activated!";
        } else {
          divMessage.innerHTML = "Flux Capacitor de-activated.";
        }
      });
    });
  }
  document.addEventListener("DOMContentLoaded", initialize);
})();
```

记住在尝试获取 ToggleSwitch 控制并修改其属性（包括接线事件处理程序）之前调用 `processAll()`。在对其进行任何操作之前，ToggleSwitch 控制必须存在。

## 使用 Rating 控制

你可以使用 WinJS Rating 控制来收集和显示用户评分。默认情况下，Rating 控制允许你在 1 到 5 星之间选择以进行评分（见图 4.10）。你可以使用鼠标、手指或通过将焦点移动到控件并使用上下/左右箭头键来更改评分。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_133_0.png)

图 4.10 收集用户评分

以下是声明 Rating 控制的方法：

```html
<div id="ratingProduct" data-win-control="WinJS.UI.Rating"></div>
```

在声明 Rating 控制时，你可以设置几个选项：你可以设置默认评分（`averageRating`），并设置是否允许用户清除评分（默认值为 `true`）。

```html
<div id="ratingProduct"
  data-win-control="WinJS.UI.Rating"
  data-win-options="{
    averageRating:3,
    enableClear:false
  }"></div>
```

通过在 Rating 控制上从右向左滑动可以清除评分。这将导致没有星星被选中。

> **警告** 记住调用 WinJS.UI.processAll()，否则 Rating 控制将永远无法变为一个控件。

## 自定义评分

你可以通过设置 `maxRating` 和 `tooltipStrings` 属性来控制显示的评分数量以及每个评分显示的工具提示。例如，接下来的 Rating 控制仅显示三颗星，且这些星有有“bad”、“okay”和“great!”的工具提示（见图 4.11）。

```html
<div id="ratingProduct"
  data-win-control="WinJS.UI.Rating"
  data-win-options="{
    averageRating:3,
    tooltipStrings: ['bad', 'okay', 'great!'],
    maxRating:3
  }"></div>
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_134_0.png)

图 4.11 自定义评分

注意，`tooltipStrings` 属性接受一个数组。数组中的每项对应一个星。

## 提交评分

Rating 控制触发三个事件：preview、cancel 和 change。当你将鼠标悬停在评分星上时，preview 处理程序会显示不同的消息。当你点击一颗星时，会触发 change 事件，change 处理程序会显示消息。列表 4.7 中的页面包含一个 Rating 控制和一个 DIV 元素，当你点击评分或更改评分时，DIV 元素中的消息会更新。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_134_1.png)

图 4.12 处理 Rating 的 preview、cancel 和 change 事件

### 列表 4.7 处理 Rating 控制事件 (ratingSubmit.html)

```html
<html>Rate our Store!</html>

<div id="ratingStore"
  data-win-control="WinJS.UI.Rating"
  data-win-options="{
    maxRating: 3
  }"></div>

<div id="divMessage"></div>
```

### 列表 4.8 处理 Rating 控制事件 (ratingSubmit.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      var ratingStore = document.getElementById("ratingStore").winControl;
      var divMessage = document.getElementById("divMessage");

      ratingStore.addEventListener("previewchange", function (evt) {
        var tentativeRating = evt.detail.tentativeRating;

        switch (tentativeRating) {
          case 1: divMessage.innerHTML = "Don't do it! That's just mean!";
            break;
          case 2: divMessage.innerHTML = "Okay, you sure? We'll try harder!";
            break;
          case 3: divMessage.innerHTML = "Thanks!";
            break;
        }
      });

      ratingStore.addEventListener("cancel", function (evt) {
        divMessage.innerHTML = "";
      });

      ratingStore.addEventListener("change", function (evt) {
        var userRating = ratingStore.userRating;

        switch (userRating) {
          case 1: divMessage.innerHTML = "You gave us the worst rating.";
            break;
          case 2: divMessage.innerHTML = "You gave us an okay rating.";
            break;
          case 3: divMessage.innerHTML = "You gave us a good rating.";
            break;
        }
      });
    });
  }
  document.addEventListener("DOMContentLoaded", initialize);
})();
```

## 使用 DatePicker 控制

WinJS DatePicker 控制——希望你不会觉得这很意外——允许你选择日期。它显示了三个下拉列表：月、日和年（见图 4.13）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_136_0.png)

你可以这样声明 DatePicker：

```html
<div id="dateBirthday" data-win-control="WinJS.UI.DatePicker"></div>
```


默认情况下，DatePicker 控件选中今天的日期。你可以通过如下设置控件的 `current` 属性为 DatePicker 控件分配特定日期：

```
<div id='dateBirthday'
data-win-control='WinJS.UI.DatePicker'
data-win-options='{
  current: '12/25/1966'
}'>
```

上述代码会导致 DatePicker 控件将 '12/25/1966' 设为默认日期。

## 格式化年、月、日

你可以为 DatePicker 的 `yearPattern`、`monthPattern` 和 `datePattern` 属性分配格式化字符串，以控制年、月、日的显示方式。格式化字符串可以包含任何字符。在格式字符串内部，你可以使用一个或多个格式指定符（format specifiers）。日期格式指定符是一个魔法字符串（magic string），使用特定的格式显示日期的部分。

`yearPattern` 属性接受以下日期格式指定符：

- [year.full]
- [year.full(n)]
- [year.abbreviated]
- [year.abbreviated(n)]
- [era.abbreviated]
- [era.abbreviated(n)]

`monthPattern` 属性接受以下日期格式指定符：

- [month.full]
- [month.abbreviated]
- [month.abbreviated(n)]
- [month.solo.full]
- [month.solo.abbreviated]
- [month.solo.abbreviated(n)]
- [month.integer]
- [month.integer(n)]

最后，`datePattern` 属性接受以下日期格式指定符：

- [day.integer]
- [day.integer(n)]
- [dayofweek.full]
- [dayofweek.abbreviated]
- [dayofweek.abbreviated(n)]
- [dayofweek.solo.full]
- [dayofweek.solo.abbreviated]
- [dayofweek.solo.abbreviated(n)]

(n) 代表数字。例如，如果你始终希望用两位数字显示日期（可能包括前导零），则应使用日期格式指定符 `[day.integer(2)]`。

以下是如何显示年、月、日的整数：

```
<div id="dateBirthday"
  data-win-control="WinJS.UI.DatePicker"
  data-win-options={
    monthPattern: '{month.integer(2)}',
    datePattern: '{day.integer(2)}',
    yearPattern: '{year.abbreviated}'
  }>
</div>
```

由于 `datePattern` 设置为值 `[day.integer(2)]`，个位数日期将显示前导零（见图 4.14）。

![](img/3fb402034fe87fe7c8b9c70eeae675_138.png)

图 4.14 格式化年、月、日

## 使用 DatePicker 控件

WinJS 控件可以在单个格式字符串中组合多个格式指定符。例如，如果你只想通过日期和星期来显示日期，而不仅仅是年份，而是年份和纪元，那么你可以这样声明 DatePicker：

```
<div id="dateBirthday"
  data-win-control="WinJS.UI.DatePicker"
  data-win-options="{
    monthPattern: '{month.integer(2)} - {month.full}',
    datePattern: '{day.integer(2)} {dayofweek.abbreviated}',
    yearPattern: '{year.full} {era.abbreviated}'
  }">
</div>
```

注意，`monthPattern` 的格式包含一个连字符 (-)。你可以在格式字符串中插入任何需要的额外字符（见图 4.15）。

![](img/3fb402034fe87fe7c8b9c70eeae675_139.png)

图 4.15 组合格式字符串

在底层，DatePicker 利用了 `WinRT.Globalization.DateTimeFormatter` 类来格式化日期。它使用了该类使用的模板字符串。

## 仅显示年、月或日

有时，你只想允许用户选择月份，而不是年份或日期。例如，你正在创建一个私有服务，必须预留整个月份。代码列表 4.9 展示了如何使用 DatePicker 控件隐藏年份和日期，仅允许选择月份。

代码列表 4.9 仅显示月份 (dateTimePickerMonthOnly.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>第 4 章</title>

  <!-- WinJS 引用 -->
  <link href="WinJS.1.0/css/ui.css" rel="stylesheet" />
  <script src="WinJS.1.0/js/base.js"></script>
  <script src="WinJS.1.0/js/ui.js"></script>
```

```html
<!-- 第 4 章引用 -->
<link href="css/default.css" rel="stylesheet" />
<script src="datepickerMonthOnly.js"></script>

<style type="text/css">
#dateBirthday .win-datepicker-date {
  display:none;
}

#dateBirthday .win-datepicker-year {
  display:none;
}
</style>

</head>
<body>
<div id="dateBirthday"
  data-win-control="WinJS.UI.DatePicker"
  data-win-options="{
  monthPattern: 'month.solo.full'
}"></div>

</body>
</html>
```

代码列表 4.9 中的页面包含了两个级联样式表规则，这些规则隐藏了 DatePicker 控件的日期和年份选择列表（见图 4.16）。

![](img/3fb402034fe87fe7c8b9c70eeae675_140.png)

图 4.16 显示月份选择列表

## 获取选定的日期

DatePicker 控件在更改月份、日期或年份时会触发相同的事件：`change` 事件。你可以通过处理此事件来获取当前选中的日期。例如，4.10 中的 HTML 页面包含一个 DatePicker 控件和一个显示所选日期的 DIV 元素（见图 4.17）。

![](img/3fb402034fe87fe7c8b9c70eeae675_140.png)

图 4.17 DatePicker 日期

代码列表 4.10 获取日期 (dateTimePickerChange.html)

```html
<label>日期:</label>
<div id="dateBirthday"
    data-win-control="WinJS.UI.DatePicker"></div>

<div id="divMessage"></div>
```

代码列表 4.11 JavaScript 文件展示了如何处理 `change` 事件以便获取选定的日期。

```javascript
function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      var dateBirthday = document.getElementById("dateBirthday");
      var divMessage = document.getElementById("divMessage");

      dateBirthday.addEventListener("change", function (evt) {
        divMessage.innerHTML = "你的生日是 " + dateBirthday.current.toDateString();
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}
```

## 使用 DatePicker 控件

DatePicker 允许选择小时、分钟和周期（AM/PM）。

![](img/3fb402034fe87fe7c8b9c70eeae675_141.png)

图 4.18 TimePicker 控件

## 使用 TimePicker 控件

你可以这样声明 TimePicker：

```html
<div id="timeLunch"data-win-control="WinJS.UI.TimePicker"></div>
```

> 注意：忘记调用 `WinJS.UI.processAll()`，否则 TimePicker 将无法工作。

最后，如果你想以 15 分钟为增量显示分钟（见图 4.19）而不是默认的 1 分钟，可以设置 `minuteIncrement` 属性：

```html
<div id="timeLunch"
data-win-options="{
minuteIncrement: 15
</div>
```

![](img/3fb402034fe87fe7c8b9c70eeae675_142.png)

图 4.19 修改 TimePicker 控件的增量

如果你你将计算机区域设置改为 24 小时制而不是 12 小时制，那么 TimePicker 将默认显示 24 小时制。

## 获取和设置当前时间

默认情况下，TimePicker 控件显示当前时间。你可以使用 `current` 属性来获取或设置 TimePicker 控件显示的时间。例如，4.12 中的页面包含一个 TimePicker 控件和一个显示消息的 DIV 元素（见图 4.20）。TimePicker 控件被声明为默认显示 12:00pm。

![](img/3fb402034fe87fe7c8b9c70eeae675_143.png)

图 4.20 使用 TimePicker 显示选择时间

代码列表 4.12 设置当前时间 (timePickerSet.html)

```html
<label>选择午餐时间:</label>
<div id="timeLunch"
data-win-control="WinJS.UI.TimePicker"
data-win-options={
  current: '12:00pm'
}></div>
```

```html
<div id="divMessage"></div>
```

代码列表 4.13 JavaScript 文件展示了如何捕获 TimePicker 控件选择的新时间。当选择了新时间时，DIV 元素显示的消息将进行更新。

```javascript
function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      var timeLunch = document.getElementById("timeLunch");
      var divMessage = document.getElementById("divMessage");

      timeLunch.addEventListener("change", function (evt) {
        divMessage.innerHTML = "你的午餐时间是 " + timeLunch.current.toDateString();
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}
```
 标签中似乎不完整（在“Displaying Page Numbers”章节处截断了），且后面包含了大量的示例代码和说明。根据你提供的格式和要求，我为你翻译了已提供的文本部分。

以下是针对你提供文本的翻译：

[content]

# 使用 TimePicker 控制 131

```javascript
document.addEventListener("DOMContentLoaded", initialize);
)();
```

JavaScript 语言没有独立的 Time（时间）类型，TimePicker 控件的 `current` 属性同时返回日期和时间。`current` 属性代表当前日期和选定的时间。在列表 4.13 的代码中，通过 JavaScript 的 `toTimeString()` 方法提取了时间部分。

注意

我在维基百科上查了此内容（http://en.wikipedia.org/wiki/Noon）。显然，中午（noon）既不是上午 12:00 (12 am) 也下午 12:00 (12 pm)，而是中午12 点。真奇怪。

## 格式化小时、分钟和时段

你可以使用模板字符串（template strings）来格式化小时、分钟和时段选择列表中出现的项目外观。模板字符串可以包含你想要的任何字符，但在显示时间的不同部分时，可以使用一些特殊的格式占位符。

你可以在 TimePicker 的 `hourPattern` 属性使用以下格式占位符：

- [hour.integer]
- [hour.integer(n)]

你可以在 TimePicker 的 `minutePattern` 属性使用以下格式占位符：

- [minute.integer]
- [minute.integer(n)]

你可以在 TimePicker 的 `periodPattern` 属性使用以下格式占位符：

- [period.abbreviated]
- [period.abbreviated(n)]

`n` 代表一个数字。例如，如果你使用 `hour.integer(2)`，那么个位数将显示前导 0。

以下 TimePicker 控件的声明说明了你如何自定义小时、分钟和时段选择列表的外观（见图 4.21）。

```html
<div id="timeLunch"
  data-win-control="WinJS.UI.TimePicker"
  data-win-options="
hourPattern: 'hour: {hour.integer(2)}',
  minutePattern: 'minute: {minute.integer(2)}',
  periodPattern: 'period: {period.abbreviated}'
</div>
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_145_0.png)

图 4.21 格式化小时、分钟和时段

# 使用 FlipView 控制

FlipView 控件可显示一组项目。与 ListView 控件（详见第 7 章“使用 ListView 控件”）不同，FlipView 每次只显示集合中的一个项目。

FlipView 控件非常适合显示相册：一次显示一张图片。它也可以用于翻阅杂志或报纸的文章列表。

当你使用 FlipView 时，只会显示数据源中的单个项目。但是，会显示箭头以便你可以移动到数据源中的下一个或上一个项目。

例如，列表 4.14 中的 JavaScript 列表包含了一个三篇文章的集合。每篇文章都有 `title`（标题）、`author`（作者）和 `articleText`（文章文本）属性。

# 列表 4.14 文章列表

```javascript
function () {
  "use strict";

  // 创建文章列表
  var listArticles = new WinJS.Binding.List({
    title: "Why Dogs are Better than Cats",
    author: "Arnold Wiggles",
    articleText: "Pellentesque habitant morbi triste senectus et netus \
et malesuada fames ac turpis egestas. Proin pharetra nonumny pede. Mauris et \
orci.",

    {
      title: "Why Dogs are Better than Fish",
      author: "Jane Rumble",
      articleText: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. \
Maecenas porttitor congue massa. Fusce posuere, magna sed pulvinar \
ultricrices, purus lectus malesuada libero, sit amet commodo magna \
ereros quis urna.",

      title: "Why Dogs are Better than Mice",
      author: "Eric Alexander",
      articleText: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. \
Maecenas porttitor congue massa. Fusce posuere, magna sed pulvinar \
ultricrices, purus lectus malesuada libero, sit amet commodo magna \
eros quis urna.",
    };
});

WinJS.Namespace.define("MyData",
{
  listArticles: listArticles
});

})();
```

现在想象你想在 Windows Store 应用中一次一次地显示这些文章。列表 4.15 中的页面说明了你如何使用 FlipView 控件从文章列表中显示单篇文章（见图 4.22）。

注意，列表 4.15 中的页面包含了对列表 4.14 中 `articles.js` 文件的引用，该文件包含了 FlipView 的数据。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_147_0.png)

图 4.22 使用 Flip Control 显示文章

列表 4.15 使用 FlipView 显示文章 (flipView\flipView.html)

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<title>Chapter04</title>
<!-- WinJS 引用 --
<link href="///Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
<script src="//Microsoft.WinJS.1.0/js/base.js"></script>
```

*(注：由于你提供的原文在此处截断，后续关于列表 4.15 的详细描述及代码部分未翻译。)*





## 列表 4.17 使用 FlipView 显示当前页码 (flipViewPageNumber/flipViewPageNumber.js)

```javascript
(function () {
  "use strict";

function initialize() {
  WinJS.UI.processAll().done(function () {
    var fvArticles = document.getElementById("fvArticles").winControl;
    var divPageNumber = document.getElementById("divPageNumber");

    // 显示页码和页数
    function updatePageNumber() {
      var currentPage = fvArticles.currentPage + 1;
      fvArticles.count.done(function (count) {
        divPageNumber.innerHTML = "Page " + currentPage + " of " + count;
      });
    }
    updatePageNumber();

    // 在选择页面时更新页码
    fvArticles.addEventListener("pageselected", updatePageNumber);
  });
}

document.addEventListener("DOMContentLoaded", initialize);
}());
```

HTML 中显示的页码和页数是通过列表 4.17 中包含的 `updatePageNumber()` 函数更新的。该函数更新了页面中的 `divPageNumber` 元素。

注意，`FlipView.count()` 方法并不直接返回计数。相反，它返回一个 promise，在 promise 完成时返回计数。这使得 `updatePageNumber()` 函数变得稍微复杂。

## 创建自定义 FlipView 按钮

你可能想要创建自定义按钮，以便在 FlipView 的项目之间来回导航。用于 FlipView 之间导航的默认箭头非常微妙；除非你将鼠标悬停在控件上，否则它们不会出现。你可能想为用户提供更显式的按钮。

### 图 4.24 自定义 FlipView 按钮

你可以利用 FlipView 控件的两种方法来通过编程控制导航：`previous()` 和 `next()` 方法。例如，列表 4.18 中的页面包含了两个名为 `Previous` 和 `Next` 的按钮。

## 列表 4.18 带有自定义按钮的 FlipView (flipViewButtons.html)

```html
<div id="tmplArticle">
  <data-win-control="WinJS.Binding.Template">
    <div class="articleitem">
      <h2 data-bind="innerText:title"></h2>
      Author: <span data-bind="innerText:author"></span>
      <p data-bind="innerText:articleText"></p>
    </div>
  </data-win-control>
</</div>
```

```html
<div id="fvArticles">
  <data-win-control="WinJS.UI.FlipView"
    data-win-options="{
      itemDataSource: listArticles.dataSource,
      itemTemplate: '#tmplArticle'
    }">
  </data-win-control>
</</div>

<div id="divNavigation">
  <button id="btnPrevious">Previous</button>
  <button id="btnNext">Next</button>
</</div>
```

列表 4.19 中的 JavaScript 代码包含了将 `Previous` 和 `Next` 按钮连接到事件处理程序的代码。当你点击 `Previous` 按钮时，会调用 `previous()` 方法；当你点击 `Next` 按钮时，会调用 `next()` 方法。

## 列表 4.19 带有自定义按钮的 FlipView (flipViewButtons/flipViewButtons.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      var fvArticles = document.getElementById("fvArticles").winControl;
      var btnPrevious = document.getElementById("btnPrevious");
      var btnNext = document.getElementById("btnNext");

      // 设置按钮
      btnPrevious.addEventListener("click", function () {
        fvArticles.previous();
      });
      btnNext.addEventListener("click", function () {
        fvArticles.next();
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

## 总结

本章重点介绍了 WinJS 库包含的核心控件。我讨论了 Tooltip、ToggleSwitch、Rating、DatePicker、TimePicker 和 FlipView 控件的功能。

你学习了如何通过声明式和命令式方法创建这些控件。此外还提供了示例代码，演示了你如何在不同的场景下使用这些控件。

但还有更多控件要讨论！会有更多乐趣！在随后的章节中，我将向你介绍额外的 WinJS 控件，例如菜单控件和 ListView 控件。不过，我们需要先谈表单。

## 第 5 章

## 创建表单

## 本章内容

- 使用 HTML5 表单验证
- 使用 HTML5 输入元素
- 创建富文本编辑器
- 显示进度

我假设任何读这本书的人都已经熟悉 HTML 的基础知识，但我并不假设你熟悉 HTML5 的最新功能。特别是，我不假设你熟悉 HTML5 标准中包含的对 HTML 表单的更改。

在本章的第一节中，我描述了你如何在 Windows Store 应用中利用 HTML5 表单验证。你将学习如何使用验证属性——例如 `required` 和 `pattern` 属性——来强制执行验证约束。

接下来，我讨论了 HTML5 中包含的输入元素的新功能。你将学习新的 HTML5 输入类型如何允许你控制输入到表单字段中的数据类型。

最后，我谈到了 HTML5 的另外两个重要的新功能。我解释了你如何利用 `contenteditable` 属性来创建可以接受富文本（如粗体和斜体文本）的输入元素。我还讨论了新的 HTML5 progress 元素。

## 使用 HTML5 表单验证

在 Windows Store 应用中，验证 HTML 表单字段的最简单方法是利用 HTML5 验证属性。例如，假设你想为安全号码创建一个表单。

## 使用 required 属性

下面的 HTML 表单说明了如何使用 `required` 属性：

```html
<form>
  <div>
    <label>
      Security Number:
      <input id="ssn" required />
    </label>
  </div>
  <div>
    <input type="submit" />
  </div>
</form>
```

如果你提交上述表单，且没有为 ssn 字段输入值，那么你就会得到图 5.1 所示的错误消息。输入字段周围有一个红色的边框，并显示了一个提示消息。

### 图 5.1

## 使用 pattern 属性

你使用 pattern 属性根据正则表达式验证输入到输入字段的值。例如，下面的 HTML 表单验证了安全号码：

```html
<form>
  <div>
    <label>
      Security Number:
      <input id="ssn"
        required
        pattern="\d{3}-\d{2}-\d{4}"
        title="###-##-####" />
    </label>
  </div>
  <div>
    <input type="submit" />
  </div>
</form>
```

注意 ssn 字段同时具有 **required** 和 **pattern** 属性。除非输入了值，否则 **pattern** 属性不会触发。

此外，ssn 字段包含一个 **title** 属性。**title** 属性包含了错误消息显示的格式。

如果你输入无效的安全号码，你就会得到图 5.2 所示的验证错误消息。

### 图 5.2

## 执行自定义验证

如果你需要为表单元素添加自定义验证规则，可以利用 JavaScript 的 `setCustomValidity()` 方法。你可以使用此方法为表单字段关联自定义验证错误消息。

例如，假设你对用户注册表单中的用户名验证有一套复杂的规则。例如，你确保确保用户名具有特定的长度、在数据库中是唯一的，并且不包含特殊字符。这是自定义验证的一个良好候选方案。

下面的 HTML 表单包含一个 userName 字段：

```html
<form>
  <div>
    <label>
      User Name:
      <input id="userName" required />
    </label>
  </div>
  <div>
    <input type="submit" />
  </div>
</form>
```





# 第 5 章 创建表单

以下 JavaScript 代码演示了当用户用户名过短时，如何显示验证错误消息：

```
var userName = document.getElementById("userName");

userName.addEventListener("input", function (evt) {
  // 用户名必须大于 3 个字符
  if (userName.value.length < 4) {
    userName.setCustomValidity("User name too short!");
  } else {
    userName.setCustomValidity("");
  }
});
```

在上面的代码中，创建了一个针对 `input` 事件的事件监听器。当输入元素的值发生变化时，程序会检查该值的长度。如果用户名少于 4 个字符，则使用 `setCustomValidity()` 方法使输入元素失效。否则，调用 `setCustomValidity()` 方法并传入一个空字符串，以清除与用户名元素关联的任何之前的验证错误。

> 注意：一旦 input 元素的内容发生变化，就会触发 `input` 事件。`input` 事件与 `change` 事件的不同之处在于，`change` 事件在 input 元素失去焦点后才会触发。

你必须提交表单才能看到验证错误消息。提交表单后，你会在图 5.3 中看到错误。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_157_0.png)

图 5.3 使用自定义验证

## 自定义验证错误样式

默认情况下，表单中无效的 HTML 表单会带有红框显示。例如，如果你在提交 HTML 表单时没有在必填字段输入值，该字段将显示红色框。

你可以使用以下层叠样式表（CSS）伪类来自定义表单字段在不同有效性状态下的外观：

- valid—当输入元素有效时应用。
- invalid—当输入元素无效时应用。

## 使用 HTML5 表单验证

- :required—当输入元素是必填（具有 `required` 属性）时应用。
- :optional—当输入元素不是必填（不具有 `required` 属性）时应用。

假设你创建了以下用户注册表单：

```
<form>
  <div>
    <label>
      姓：
      <input id="firstName" required />
    </label>
  </div>
  <div>
    <label>
      名：
      <input id="lastName" required />
    </label>
  </div>
  <div>
    <label>
      公司：
      <input id="company" />
    </label>
  </div>
  <div>
    <input type="submit" />
  </div>
</form>
```

上面的表单包含用户姓和名的必填字段。它还包含一个用户公司的可选字段。

你可以使用以下样式规则来控制输入元素的样式样式：

```
:valid {
  background-color: green;
}
:invalid {
  background-color: yellow;
}
:optional {
  border: 4px solid green;
}
```

# 第 5 章 创建表单

```
:required {
border: 4px solid red;
}
```

这些规则使得有效字段显示绿色背景，无效字段显示黄色背景。可选字段显示绿色边框，而必填字段显示红色边框。

## 重置表单

在成功提交表单后，重置它是一个好主意，这样你可以再次使用该表单。例如，你的应用可能包含一个添加新电影的表单。每当你添加一个新电影时，都希望表单重置为默认状态。

如果你在使用验证属性，不能简单地通过给表单字段分配空字符串来重置表单。如果你给必填字段分配空字符串，那么该字段将处于无效状态。

相反，你应该通过调用 `reset()` 方法来重置表单。例如，为了重置标题，你可以使用以下 HTML 代码：

```html
<form id="myForm">
  <div>
    <label>
      标题：
      <input id="title" required />
    </label>
  </div>
  <!-- 其他字段 -->
</form>

<script>
  document.getElementById("myForm").reset();
</script>
```

（注：由于原文文本中存在大量重复的章节和相似的内容，译文已根据要求进行了结构化翻译并确保格式完整性）




```html
type="number"
placeholder="###" />
</label>
```

当输入类型的值为 `number` 时，如果你输入了任何非数字内容，值会在字段失去焦点时立即消失。这可能会让用户感到困惑。因此，包含一个 `placeholder` 属性或说明文本来指示该字段仅接受数字（不包含美元符号，只需数字）是一个好主意。

你可以使用 `min` 和 `max` 属性为输入字段指定最小值和最大值，如下：

```html
<label>
数量:
<input id="inpQuantity"
type="number"
placeholder="###"
min="1"
max="10" />
</label>
```

如果你输入的数字不在指定的范围内，将显示一条验证错误消息（见图 5.6）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_163_0.png)

FIGURE 5.6 超出范围的数字

在默认情况下，你只能向 <input type="number" /> 字段中输入整数值。如果你想输入非整数值（例如 1.5），则需要像所示修改 `step` 属性：

```html
<input id="inpFavNumber"
type="number" step="0.5"
placeholder="###" />
```

`step` 属性决定了数字之间的允许增量。

当你在 Windows Store 应用中使用数字字段并使用触摸键盘时，你将获得一个用于输入数字的特殊键盘（见图 5.7）。

# 从数值范围内输入值

如果你想显示一个滑块，可以创建一个 <input type="range" /> 元素。例如，接下来的 HTML 表单显示了一个滑块，允许你选择购买的糖果数量：

```html
<label>
糖果数量:
<input id="quantity"
type="range"
min="10"
max="100"
step="5"
value="30"/>
</label>
```

该滑块显示 10 到 100 之间的范围值，并以 5 为单位进行增量。默认值设置为 30（见图 5.8）。

![](img/3fb4022034fe87fe7c8b9c70e5eae6c75_164_0.png)

FIGURE 5.8 显示滑块

# 输入电子邮件地址、URL、电话号码和搜索词

你可以使用输入类型 `email`、`url`、`tel` 和 `search` 来允许用户输入 URL、电子邮件地址、电话号码和搜索词。

如果你使用 <input type="email"/> 并使用触摸键盘，那么你将获得图 5.9 所示包含 @ 和 .com 键的专用键盘。

FIGURE 5.7 使用触摸键盘输入数字

# 152 第 5 章 创建表单

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_165_0.png)

FIGURE 5.9 <input type="email" /> 用于电子邮件的触摸键盘

使用 <input type="email" /> 还能为你提供自动验证。你必须输入有效的电子邮件地址，否则你将收到图 5.10 中的验证错误消息。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_165_1.png)

FIGURE 5.10 电子邮件验证

使用 <input type="url" /> 创建了一个输入 URL 的特殊输入字段。你将获得图 5.11 所示包含特殊 / 和 .com 键的触摸键盘。

> 注意
> 只有当机器上没有连接键盘或你显式打开触摸键盘时，触摸键盘才会出现。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_165_2.png)

FIGURE 5.11 用于 URL 的触摸键盘

<input type="url" /> 要求你输入有效的 URL。例如，URL http://Superexpert.com 和 URL ftp://Superexpert.com 是有效的，但 URL superexpert.com 和 URL www.superexpert.com 是无效的，因为它们不是绝对 URL（见图 5.12）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_165_3.png)

FIGURE 5.12  URL

## 使用 HTML5 输入元素

你使用 <input type="tel" /> 元素输入电话号码。因为电话号码有许多不同的格式，这种输入类型不执行任何验证。相反，你可以使用 <input type="tel" /> 显示用于电话号码的专用触摸键盘（见图 5.13）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_166_0.png)

FIGURE 5.13 输入电话号码

最后是 <input type="search" />。关于没有什么可以说的 <input type="search" /> 的，因为这种输入类型的行为与 <input type="text" /> 完全相同。它没有键盘，也没有特殊的验证。

# 从列表中输入值

你可以使用新的 HTML5 `list` 属性为用户提供自动补全体验。例如，以下代码为汽车品牌提供了三个建议的列表：

```html
<label>
汽车品牌:
<input id="inpCarMake" list="dlCarMakes" />
<datalist id="dlCarMakes">
  <option>BMW</option>
  <option>Ford</option>
  <option>Tesla</option>
</datalist>
</label>
```

`list` 属性指向 HTML5 `datalist` 元素，该元素包含了建议列表。当你开始向输入元素中输入文本时，你将看到图 5.14 所示的建议。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_166_1.png)

FIGURE 5.14 获取建议列表

## 选择文件

你不强制从列表中选择。使用 `list` 属性使输入元素的工作更像一个组合框（combo-box）而不是选择列表。

你可以使用 <input type="file" /> 创建图片选择器。例如，你可以使用 <input type="file" /> 允许用户从硬盘硬盘选择图片文件。

以下 HTML 页面包含一个 <input type="file" /> 元素和一个 ID 为 `imgPicture` 的 DIV 元素。当你从硬盘选择一张图片后，图片将出现在 img 元素中（见图 5.15）。

```html
<form id="frmAdd">
  <div>
    <label>
      图片:
      <input id="inpFile" type="file" accept="image/*" />
    </label>
    <input type="submit" />
  </div>
</form>
```

当使用 <input type="file" /> 元素时，你可以使用 `accept` 属性来限制可以上传的文件类型。例如，在上面的标记中，`accept` 元素的值为 "image/*"，这防止了除图片文件以外的任何文件被选中。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_167_0.png)

FIGURE 5.15 选择图片文件

以下 JavaScript 代码用于处理表单提交事件。此代码从输入元素获取选定的图片 img 元素中显示：

```javascript
(function () {
  "use strict";

  function initialize() {
    var frmAdd = document.getElementById("frmAdd");

    frmAdd.addEventListener("submit", function (evt) {
      evt.preventDefault();

      var imgPicture = document.getElementById("imgPicture");
      var inpFile = document.getElementById("inpFile");

      if (inpFile.files.length > 0) {
        // 使用 HTML5 File API 创建引用图片的 URL
        var pictureURL = URL.createObjectURL(inpFile.files[0]);

        // 在 img 元素中显示图片
        imgPicture.src = pictureURL;
      }
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})
```

## 创建富编辑器

如果你想创建一个接受富文本（如加粗、斜体或下划线）的表单字段，可以使用 `contenteditable` 属性。假设你想允许用户输入大学论文。在这种情况下，你可以使用以下 HTML：

```html
<form>
  <label for="inpEssay">
    大学录取论文:
  </label>
  <div id="inpEssay" contenteditable="true" class="win-textarea richtext"></div>
  <br />
  <input type="submit" />
</form>
```

在上面的表单中，`contenteditable` 属性应用于 id 为 `inpEssay` 的 DIV。该属性使得 DIV 元素的内容可编辑（见图 5.16）。

注意带有 `contenteditable` 属性的 DIV 应用了两个 CSS 类：`win-textarea` 和 `richtext`。`win-textarea` 类是 WinJS 库的一部分，该类为编辑器应用了标准的 Windows 应用样式。

`richtext` 类定义如下：

```css
.richtext {
width:300px;
height:100px;
white-space:pre-wrap;
}
```

## 显示进度

HTML5 规范包含了一个名为 `progress` 的新元素，它允许你显示进度指示器。进度指示器基本有两种类型：不确定进度指示器和确定进度指示器。




当你想显示忙碌等待指示器且不知道任务还需要多久才能完成时，可以使用不确定进度指示器。以下是声明不确定进度指示器的方法：

```
<progress id="progress1"></progress>
```

在 Windows Store 应用中，默认的进度指示器显示一组水平移动的动画圆点（见图 5.17）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_170_0.png)

图 5.17 显示不确定性进度

如果你想显示一个确定性进度指示器，则需要为 `progress` 元素的 `max` 和 `value` 属性提供值。例如，这里是创建一个显示值在 1 到 20 之间进度的进度指示器的方法：

```
<progress id="progress1"
max="20"
value="1">
</progress>
```

此外，这里有一段每隔 1 秒更新一次进度的 JavaScript 代码：

```javascript
(function () {
  "use strict";

  function initialize() {
    var progress1 = document.getElementById("progress1");
    var ivProgress = setInterval(updateProgress, 1000);
  }

  function updateProgress() {
    progress1.value = ++progress1.value;
    if (progress1.value === 20) {
      window.clearInterval(ivProgress);
    }
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

通过这种方式声明 `progress` 元素将得到一个传统的进度条（见图 5.18）。

# 158 第5章 创建表单

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_171_0.png)

图 5.18 显示确定性进度

在 Windows Store 应用中，你可以可以使用与 `progress` 元素一起的一些样式选项。在创建不确定进度指示器时，你可以使用 `win-ring` 类来显示动画圆点环，而不是默认的动画水平圆点（见图 5.19）：

```
<progress id="progress2" class="win-ring">
</progress>
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_171_1.png)

图 5.19 显示动画圆环进度指示器

如果你想控制不确定进度指示器的大小，可以使用 `win-medium` 或 `win-large` 类。例如，以下页面包含三个大小递增的进度指示器：

```
<progress id="progressRing1" class="win-ring">
</progress>
<br /><br />
<progress id="progressRing2" class="win-ring win-medium">
</progress>
<br /><br />
<progress id="progressRing3" class="win-ring win-large">
</progress>
```

## 总结

本章的重点是为 Windows Store 应用创建 HTML 表单。在第一部分，我解释了如何利用 HTML 中包含的新型表单验证功能。你学习了如何使用 `required` 和 `pattern` 属性执行基本验证，以及使用 `setCustomValidity()` 方法执行高级验证。

接下来，我描述了如何利用新的 HTML5 输入类型。你学习了如何使用 `number` 和 `range` 类型来接受数字。你还学习了如何接受电子邮件地址、URL、电话号码和搜索词。我还演示了如何使用 `<input type="file" />` 从你的计算机硬盘中选择文件。

最后，我演示了如何使用 `contenteditable` 属性创建一个富文本编辑器，并使用新的 HTML5 `progress` 元素创建一个进度指示器。

# 第 6 章

# 菜单与弹出层（Flyouts）

## 本章内容

- 使用弹出层（Flyout）控件
- 使用菜单（Menu）控件
- 使用应用栏（Appbar）控件
- 配置应用设置
- 显示 Windows 对话框

本章重点关注弹出层、菜单、工具栏、设置和对话框等主题。你将学习如何向用户提供选项并获取他们的响应。

我首先解释了如何使用 Flyout 控制在页面主体内显示选项。你学习了如何使用 Menu 控制显示按钮、切换、弹出层和分隔符。

接下来，我讨论了应用栏。应用栏是 Windows Store 应用中放置应用程序命令的标准位置。你学习了如何创建全局命令和选择命令。

你还学习了如何配置你的应用设置。你学习了如何利用 `SettingsFlyout` 控件来扩展由 Settings 磁 显示的标准设置。

最后，我向你展示了如何使用 `MessageDialog` 类创建模态对话框。你学习了如何创建警告对话框和“是/否”对话框。

# 使用弹出层（Flyout）控件

你使用 Flyout 控件在页面中显示弹出窗口。当你点击弹出窗口外部（或按下 ESC 键）时，弹出窗口就会消失。你可以使用 Flyout 控件显示信息、显示关闭或收集输入。

Flyout 控件支持轻量级关闭（light dismiss）。当你点击 Flyout 控件外部时，控件会自动消失。

弹出层的一个常见用途是显示警告。例如，如果你的应用程序恰好包含一个“永久删除所有数据”按钮，那么使用弹出层警告用户将是一个好主意。

弹出层的另一个常见用途用于显示内联表单。例如，图 6.1 所示页面

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_170_0.png)

图 6.1 显示弹出层

```html
<!-- 点击此按钮显示弹出层 -->
<button id="btnType">字体</button>

<!-- 弹出层 -->
<div id="flyout" class="win-ring">
  <label>字体:</label>
  <select id="selectType">
    <option>Arial</option>
    <option>Impact</option>
    <option>Comic Sans</option>
  </select>
</div>
```

在示例 6.1 中，你可以使用弹出层来选择字体。

```javascript
(function () {
  "use strict";

  function initialize() {
    var btnType = document.getElementById("btnType");
    var selectType = document.getElementById("selectType");
    var flyout = document.getElementById("flyout");

    btnType.addEventListener("click", function () {
      // 显示弹出层
    });

    selectType.addEventListener("change", function () {
      // 更新字体
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

# 使用菜单（Menu）控件

WinJS Menu 控件继承自 Flyout 控件——因此具有许多功能。与 Flyout 控件一样，Menu 控件以弹出窗口的形式出现，并在点击菜单区域外时消失。

然而，与 Flyout 控件不同，Menu 控件专门用于显示菜单命令。你只能在 Menu 控件中放置菜单命令，而不是其他类型的控件或 HTML 元素。Menu 控件支持以下类型的命令：

- 按钮——点击菜单项执行操作。
- 切换——切换菜单项。
- 弹出层——点击菜单项显示一个弹出层。
- 分隔符——不同组命令之间的分隔符。

列表 6.3 说明了如何声明 Menu 控件以使用这些这些菜单命令。

# 列表 6.3 显示菜单 (menu.html)

```html
<!-- 点击此按钮显示菜单 -->
<button id="btnEdit">编辑</button>

<!-- 菜单控件 -->
<div id="menuEdit"
  data-win-control="WinJS.UI.Menu">
  <button
    data-win-control="WinJS.UI.MenuCommand"
    data-win-options={
      id:'menuCommandDelete',
      label:'删除',
      type: 'button'
    }></button>
  <hr>
  <button
    data-win-control="WinJS.UI.MenuCommand"
    data-win-options={
      type: 'separator'
    } />
  <button
    data-win-control="WinJS.UI.MenuCommand"
    data-win-options={
      id:'menuCommandBold',
      label:'加粗',
      type: 'toggle'
    }></button>
</div>
```


```html
type: 'toggle'
</button>
<button>
data-win-control="WinJS.UI.InputCommand"
data-win-options="{
  id:'Typeface',
  label:'Typeface',
  type:'flyout',
  flyout: select('#Typeface')
}
></button>
```

```html
<!-- Flyout 控制 -->
<div id="flyTypeface"
data-win-control="WinJS.UI.Flyout">
<label>选择字体:</label>
<select id="selectTypeface">
<option>Arial</option>
<option>Impact</option>
<option>Comic Sans MS</option>
</select>
</>
```

```html
<!-- 需要样式的文本 -->
<p id="pText">
Lorem ipsum dolor sit amet, consectetuer adipiscing elite
Maecenas porttitor massa. Fusce posuere, magna sed
pulvinar ultricies, purus lectus malesuada libero, sit amet
commodo magna eros quis urna.\n</p>
```

列表 6.3 中的页面包含了一段 lorem ipsum 文本。你使用菜单控件来修改文本的外观（参见图 6.2）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_178_0.png)

# 第 6 章 菜单与弹出层 (Flyouts)

此菜单包含五个菜单命令（WinJS.UI.InputCommand 类的实例）。它包含一个按钮、一个分隔符、两个切换按钮和一个弹出层命令。

按钮命令会删除所有文本。该命令连接到列表 6.4 JavaScript 文件中的点击事件处理程序。

分隔符命令什么都不做。它只是在菜单上不同组的命令之间显示一个分隔符（即一条水平线）。

**两个切换命令允许你在文本的**粗体/正体**和*斜体/正体*之间进行切换。这些命令的点击事件处理程序包含在列表 6.4 中。

最后，弹出层命令会显示一个 Flyout 控制。Flyout 控制包含在 6.3 的 HTML 页面中，名为 `flyTypeface`。弹出层允许你为文本选择字体（参见图 6.3）。当弹出层出现时，它会消失。

列表 6.4 显示菜单 (menu\menu.js)

```javascript
function () {
  "use strict";
}

function initialize() {
  WinJS.UI.parentElement.done(function () {
    var btnEdit = document.getElementById("btnEdit");
    var menuEdit = document.getElementById("menuEdit").winControl;
    var selectTypeface = document.getElementById("selectTypeface");
    var pText = document.getElementById("pText");

    // 点击编辑时显示菜单
    btnEdit.addEventListener("click", function () {
      menuEdit.show(btnEdit);
    });

    // 连接命令
    document.getElementById("menuCommandDelete").addEventListener("click",
    function (evt) {
      pText.innerHTML = "[deleted]";
    });
    document.getElementById("menuCommandBold").addEventListener("click",
    function (evt) {
      var toggleState = document.getElementById("menuCommandBold").selected;
      if (toggleState) {
        pText.style.fontWeight = 'bold';
      } else {
        pText.style.fontWeight = 'normal';
      }
    });

    document.getElementById("menuCommandItalic").addEventListener("click",
    function (evt) {
      var toggleState = document.getElementById("menuCommandItalic").selected;
      if (toggleState) {
        pText.style.fontSize = 'italic';
      } else {
        pText.style.fontSize = 'normal';
      }
    });
    selectTypeface.addEventListener("change", function () {
      pText.style.fontFamily = selectTypeface.value;
    });
  });
document.addEventListener("DOMContentLoaded", initialize);
}
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_180_0.png)

图 6.3 使用菜单控件显示弹出层

# 使用应用栏控件 (AppBar Control)

Windows 应用程序有一个应用程序命令的标准位置：应用栏通常出现在底部。然而，你也可以在应用的顶部和底部都显示应用栏。只有当你从页面的底部或顶部滑动或使用鼠标右键点击时，应用栏才会出现。

例如，6.4 示例了 Windows 8 版本 Internet Explorer 中两个应用栏的外。底部应用栏包含用于导航到网站的地址栏，顶部应用栏包含活动标签页。如果你点击页面，两个应用栏都会消失，你将获得全屏体验。

由于顶部应用栏通常用于导航到不同页面，因此顶部应用栏也称为导航栏 (nav bar)。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_181_0.png)

图 6.4 Internet Explorer 应用栏

# 创建简单的应用栏

你使用 WinJS AppBar 控件为你的 Windows 应用程序添加应用栏。例如，这里是如何声明一个出现在应用程序底部的应用栏的：

```html
<div id="appBar"
  data-win-control="WinJS.UI.AppBar">
  <button data-win-control="WinJS.UI.AppBarCommand"
    id:'Play',
    label:'Play',
    icon:'play'
  ></button>
  <button data-win-control="WinJS.UI.AppBarCommand"
    id:'Pause',
    label:'Pause',
    icon:'pause'
  ></button>
</div>
```

> 注意：AppBar 控制包含在 HTML 页面中。应用栏包含两个按钮：Play 和 Pause。![](img/3fb402034fe87fe7c8b9c70e5eae6c75_182_0.png)

图 6.5 一个简单的应用栏

如果你想创建一个出现在应用程序顶部的应用栏（导航栏），你需要这样设置 AppBar 属性：

```html
<div id="appBar"
  data-win-control="WinJS.UI.AppBar"
  data-win-options="{
    placement:'top'
  }">

  <button data-win-control="WinJS.UI.AppBarCommand"
    id:'Save',
    label:'Save',
    icon:'save'
  ></button>
</div>
```

placement 属性默认值为 "bottom"。上面，我将属性设置为 "top"，以便应用栏出现在应用程序顶部（参见图 6.6）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_183_0.png)

图 6.6 创建顶部和底部应用栏

# 使用应用栏命令

有四种应用栏命令：

- 按钮 (button)：执行某些操作。
- 切换 (toggle)：在两种状态之间切换的切换按钮。
- 弹出层 (flyout)：用于显示表单的弹出层。
- 分隔 (separator)：命令之间的分隔符。

列表 6.5 包含了包含所有四种命令的应用栏示例：

```html
<!-- 应用栏控件 -->
<div id="appBar"
data-win-control="WinJS.UI.AppBar">

<!-- 应用栏命令 -->
<button data-win-control="WinJS.UI.AppBarCommand"
  id:'Play',
  label:'Play',
  icon:'play'
></button>
<button data-win-control="WinJS.UI.AppBarCommand"
  id:'Mute',
  type:'toggle',
  label:'mute',
  icon:'mute'
></button>
<hr data-win-control="WinJS.UI.AppBarCommand"
  data-win-options='{
    type:'separator'
   />
<button data-win-control="WinJS.UI.AppBarCommand"
  id:'AddSong',
  type:'flyout',
  label:'Add',
  tooltip:'Add Song',
  flyout: select('#Typeface')
>
></button>
</div>
```

```html
<!-- 添加歌曲弹出层 -->
<div id="flyAddSong" data-win-control="WinJS.UI.Flyout">
<form>
  <input id="inpNewSong" required />
  <input type="submit" value="Add" />
</form>
</div>
```

当你滑动或右键点击时，就会得到图 6.7 所示的应用栏。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_185_0.png)





```javascript
(function () {
  "use strict";

  function initialize() {
    WinUS.UI.processAll().done(function () {

    var cmdMute = document.getElementById("cmdMute");
    cmdMute.addEventListener("click", function () {
      console.log(cmdMute.winControl.selected);
    });
  });
}

document.addEventListener("DOMContentLoaded", initialize);
});

```

分隔符命令在命令之间创建一个垂直条，以便你对其进行分组。创建分隔符命令时，请使用 `<HR>` 元素而不是 `<BUTTON>` 元素。

最后，弹出层命令（flyout command）显示一个 Flyout 。在列表 6.5 中，`cmdAdd` 命令显示了一个包含输入新歌曲标题表单的 Flyout。

## 显示上下文命令

某些应用栏命令适用于整个应用程序。其他应用栏命令则仅在选中某个项目时生效。例如，在应用栏中始终显示“添加”按钮可能是有意义。相反，显示“删除”或“编辑”按钮只有在选中某个项目时才有意义。

该应用有两个内置部分，分别命名为“全局（global）”和“选择（selection）”。默认情况下，当你向应用栏添加命令时，这些命令将出现在全局部分。这些命令位于应用栏的右侧。

你还可以选择将命令添加到选择部分。这些命令出现在应用栏的左侧。选择部分中的命令应该只在选中某些内容时显示。

想象一下，你想使用 `ListView` 控件显示任务列表。你希望用户能够添加新任务并删除现有任务。在这种情况下，将“添加”按钮放置在应用栏的全局部分，将“删除”按钮放置在应用栏的选择部分是有有意义的（见图 6.8）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_187_0.png)

图 6.8 全局与选择应用栏

以下是你可以如何声明应用栏，使其包含“添加”和“删除”命令的方法：

```html
<div id="appBar" data-win-control="WinJS.UI.AppBar">
  <button data-win-control="WinJS.UI.AppBarCommand"
    data-win-options="{
      id:'cmdAdd',
      label:'Add',
      icon:'add',
      tooltip:'Add Task',
      type:'flyout',
      flyout:select('#flyAdd'),
      section:'global'
    }">
  </button>
  <button data-win-control="WinJS.UI.AppBarCommand"
    data-win-options="{
      id:'cmdDelete',
      label:'Delete',
      icon:'delete',
      tooltip:'Delete Task',
      section:'selection',
      extraClass:'appBarSelection'
    }">
  </button>
</div>
```

## 配置应用设置

注意，“添加”命令被放置在应用栏的全局部分。你实际上不需要显式指定这一点——全局是默认值。

“删除”命令被放置在选择部分。此外，请注意到额外的 CSS 类名 `appBarSelection` 与“删除”命令相关联。稍后我将利用该类来隐藏和显示“删除”命令。

以下是隐藏和显示应用栏的 JavaScript 代码：

```javascript
// 默认隐藏选择命令
appBar.hideCommands(document.querySelectorAll('.appBarSelection'));

// 当 ListView 项被选中时，显示应用栏
vTasks.addEventListener('selectionchanged', function () {
  if (lvTasks.selection.count() == 1) {
    appBar.showCommands(document.querySelectorAll('.appBarSelection'));
    appBar.show();
  } else {
    appBar.hideCommands(document.querySelectorAll('.appBarSelection'));
  }
});
```

当应用首次启动时，你想隐藏“删除”命令，因为没有任何项目被选中。在上面的代码中，使用 `hideCommands()` 方法隐藏与 `appBarSelection` CSS 类相关的所有命令。

接下来，代码处理由 `ListView` 控件触发的 `selectionchanged` 事件。当你选中 `ListView` 中的某个项目（通过滑动或右键点击该项目）时，通过 `showCommands()` 方法显示选择命令。

由于应用栏默认是隐藏的，你可能不会注意“删除”命令。因此，代码调用了 `show()` 方法来强制显示应用栏。当你选中 `ListView` 中的一个项目时，应用栏会自动显示，你就知道可以删除该项目了。

> 注意
你可以可以使用应用栏控件的 `sticky` 属性强制应用栏始终出现。当 `sticky` 属性值为 `true` 时，应用栏不会自动消失。

## 配置应用设置

Windows 商店应用有一个标准位置供用户配置应用设置。你可以从特征栏（charm bar）中的设置访问应用设置，可以通过以下方式打开设置：

- 将鼠标移动到屏幕右下角
- 用手指从屏幕右边缘向左滑动
- 按 Windows + i 键

默认情况下，系统设置（如网络和音量设置）出现在设置窗口的底部。权限设置也会自动出现。最后，如果你确实是从 Windows 商店获取的 Windows 商店应用，设置窗口还将包含评分和评论设置。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_189_0.png)

图 6.9 默认设置

你可以为你的应用向设置窗口添加自定义设置。这些自定义设置可以是配置设置，例如用户偏好。自定义设置还可能包含有关你应用的信息，包括“帮助”和“关于”页面。

你可以借助 `SettingsFlyout` 控件创建自定义应用设置。对于你想要创建的每个应用设置部分，你需要创建一个包含 `SettingsFlyout` 的独立 HTML 文件。我将通过创建“关于”页面设置和“个人”设置来演示其工作原理。

## 创建关于页面设置

大多数应用都包含一个“关于”页面，提供有关构建应用程序的公司的信息。“关于”页面是纯信息性的（见图 6.10）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_190_0.png)

图 6.10 创建关于设置

如果你想在设置窗口中创建一个“关于”设置，你首先需要创建一个包含 `SettingsFlyout` 的新 HTML 文件。列表 6.6 中的页面说明了如何创建一个。

列表 6.6 关于设置

```html
<!DOCTYPE html>
<html>
<head>
  <title>About</title>
</head>
<body>
  <div id="divAbout"
    data-win-control="WinJS.UI.SettingsFlyout"
    data-win-options="{
      width: 'narrow'
    }">
    <div class="win-header"
      style="background-color:#464646">
    <button onclick="WinJS.UI.SettingsFlyout.show()"
      class="win-backbutton"></button>
    <div class="win-label">About</div>
  </div>
  <div class="win-content">
    This app was created by the skilled programmers of Acme
    Incorporated.
  </div>
</body>
</html>
```

列表 6.6 中的页面包含一个 `SettingsFlyout` 控件。注意该控件被定义为窄宽度。当你以窄宽度打开设置时，设置的大小与设置窗口相同。或者，你可以将宽度设置为“宽（wide）”，为显示设置创建一个更大的空间。

你可以在 Flyout 中放置任何你想要的内容，内容会在打开设置时就会显示。然而，微软提供了一些准则。列表 6.6 中的 `SettingsFlyout` 控件包含一个返回按钮，以便你可以返回设置窗口。该控件还利用了标准的 WinJS 样式，如 `win-label` 和 `win-content`。

在使用“关于”设置之前，你必须通过如下处理 `WinJS.Application` 事件来注册设置：

```javascript
(function () {
  "use strict";
  WinJS.Application.onsettings = function (e) {
    e.detail.applicationcommands = {
      "divAbout": { href="AboutSettings.html", title: "About" }
    };
    WinJS.UI.SettingsFlyout.populateSettings(e);
  };
};
WinJS.Application.start();
})();
```

你将一组设置命令分配给 `e.detail.applicationcommands` 对象。在上面的代码中，“关于”设置的路径和标题被分配给命令集合。

> 警告
在创建设置时，必须调用 `WinJS.Application.start()`，否则设置事件永远不会触发。

## 创建个人设置

想象你想让用户在 Windows 商店应用的设置中输入他们的姓（见图 6.11）。你正在开发一个友好的应用，并希望通过姓名称呼用户。





## 配置应用设置

# 179

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_192_0.png)

图 6.11 收集个人设置

列表 6.7 中的 HTML 页面——命名为 personalSettings.html——包含一个包含 HTML 表单的 SettingsFlyout。该表单有两个表单字段 `inpFirstName` 和 `inpLastName`，且两者都是必填的。

列表 6.7 用于个人设置的 SettingsFlyout

```html
<!DOCTYPE html>
<html>
<head>
  <title>Security</title>
  <script type="text/javascript" src="personalSettings.js"></script>
</head>
<body>
  <div id="divPersonal"
    data-win-control="WinJS.UI.SettingsFlyout"
    data-win-options={
      "width":"narrow"
    }>
    <div class="win-header"
      style="background-color:#464646">
      <button
        onclick="WinJS.UI.SettingsFlyout.show()"
        class="win-backbutton"></button>
      <div class="win-label">Personal</</div>
    </div>
  </div>
<div class="win-content">
<form id="frmPersonal">
```

# 第 6 章 菜单与飞出显示层

```html
<div>
  <label>
    First Name: <br />
    <input id="firstName" required />
  </label>
</div>
<div>
  <label>
    Last Name: <br />
    <input id="lastName" required />
  </label>
</div>
<div>
  <input type="submit" value="Save" />
</div>
</form>
</div>
</body>
</html>
```

注意，列表 6.7 中的页面引用了一个名为 `personalSettings.js` 的 JavaScript 文件。该文件包含在列表 6.8 中。此 JavaScript 文件负责加载和保存名字和姓氏。

## 6.8 加载和保存设置

```javascript
(function () {
  'use strict';

  WinJS.Pages.define("personalSettings.html", {
    loaded: function (element, options) {
      var roamingSettings = window.Storage.ApplicationData.current.roamingSettings;
      var divPersonal = document.getElementById("divPersonal").winControl;
      var frmSecurity = document.getElementById("frmPersonal");
      var inpFirstName = document.getElementById("firstName");
      var inpLastName = document.getElementById("lastName");

      // 读取名字和姓氏
      divPersonal.addEventListener("befhow", function () {
        inpFirstName.value = roamingSettings.values["firstName"] || "";
        inpLastName.value = roamingSettings.values["lastName"] || "";
      });
    }

    // 保存名字和姓氏
    frmSecurity.addEventListener("submit", function () {
      roamingSettings.values["firstName"] = inpFirstName.value;
      roamingSettings.values["lastName"] = inpLastName.value;
    });
})();
```

列表 6.8 中的 JavaScript 代码包含一个针对 `SettingsFlyout` 事件的事件处理器。该事件在 SettingsFlyout 显示之前触发。在列表 6.8 中，用户的名字和姓氏将从漫游设置中加载并分配到表单字段。

列表 6.8 中的代码还包含一个针对表单提交事件的事件处理器。该处理器将用户的名字和姓氏保存到漫游设置中。名字和姓氏会永久保存在计算机上，以便用户再次运行应用时可以使用。由于设置存储在漫游存储中，它们在不同的计算机之间可用。

> 注意 漫游设置存储在计算机注册表中并跨设备同步。目前，微软限制您在漫游存储中存储 100KB（使用 `ApplicationData.RoamingQuota` 查看限制）。

若要在页面中使用个人设置，您必须在与页面相关的 JavaScript 文件中注册这些设置。以下代码注册了关于页面（来自上一节）和个人设置：

```javascript
function () {
  "use strict";
  WinJS.Application.settings = function (e) {
    e.detail.applicationcommands = {
      "divPersonal": { href: "personalSettings.html", title: "Personal" },
      "divAbout": { href: "aboutSettings.html", title: "About" }
    };
    WinJS.UI.SettingsFlyout.populateSettings(e);
  }
  WinJS.Application.start();
}();
```

# 显示 Windows 对话框

有时没有什么比经典的模态对话框更好的了。模态对话框会阻塞用户与应用的所有交互，直到模态对话框获得回答。

当您的应用如果没有某些关键信息无法工作时，模态对话框是必要的。例如，天气应用在不知道用户位置的情况下无法显示天气。因此，在应用首次运行时使用模态对话框询问用户的位置是合理的。

在您确实需要向用户传达关键警告或信息时，也可以在原本使用 JavaScript 警报的情况下使用模态对话框。您应该谨慎使用模态对话框。

> 在用 JavaScript 编写的 Windows Store 应用中不支持 JavaScript 警报。由于我认为 JavaScript 警报与（已弃用的）HTML blink 标签密切相关，这是一件好事。

您通过使用 `MessageBox` 类创建模态对话框。以下是如何打开一个显示“你知道你的拉链没拉吗？”的对话框（见图 6.12）。

```javascript
var message = new Windows.UI.Popups.MessageBox(
  "Did you know that your fly is unzipped?"
);
message.showAsync();
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_195_0.png)

图 6.12 使用消息对话框

您可以通过提供命令来自定义对话框的外观。例如，这里是创建“是/否”对话框的方法：

```javascript
// 创建对话框
var message = new Windows.UI.Popups.MessageDialog(
  "Did you know that your fly is unzipped?",
  "Warning!"
);
```

```javascript
// 添加命令
message.commands.append(new Windows.UI.Popups.UICommand("&Yes"));
message.commands.append(new Windows.UI.Popups.UICommand("&No"));
```

```javascript
// 显示对话框
message.showAsync().done(function(answer) {
  if (answer.label === "&Yes") {
    console.log("You picked yes");
  } else {
    console.log("You picked no");
  }
});
```

该代码向消息对话框添加了两个标签为“是”和“否”的 UICommand 对象（见图 6.13）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_196_0.png)

图 6.13 是/否对话框

> 注意 按钮标签为 "&Yes" 和 "&No"。使用 & 符号指定快捷键。您可以按住 ALT 键来确定点击了哪个按钮。

## 总结

本章主要介绍了飞出显示层（flyouts）、菜单、工具栏和对话框。
- 我首先讨论了如何使用 Flyout 控件创建包含任何 HTML 内容的简单弹出窗口。
- 接下来，我解释了如何使用 Menu 控件来显示命令。你学习了如何在菜单中包含按钮、切换器和分隔符。
- 我还讨论了应用栏（app bar）。你学习了如何向应用栏添加全局命令和选择命令。
- 你还学习了如何利用 SettingsFlyout 控件来扩展你的 Windows Store 应用设置窗口中显示的设置。你学习了如何从漫游设置中检索设置。
- 最后，我向你展示了如何利用 MessageDialog 类来创建对话框。我们创建了警告对话框和“是/否”对话框。

请继续关注。在下一章中，我们将讨论最重要的控件：ListView 控件。

# 第 7 章

# 使用 ListView 控件

整个章节都致力于一个控件：ListView 控件。这是 WinJS 库中包含的最强大的控件。如果你需要显示项目列表——例如，电影列表、产品列表、文件列表、照片列表——那么 ListView 控件就是你要使用的控件。

在本章中，我解释了如何利用 ListView 控件的所有最重要功能。你将学习基础知识，包括如何在 ListView 中选择、排序、过滤和对项目分组。

# ListView 控件简介

让我们从基础知识开始。你可以将 ListView 绑定到任何实现 JavaScript IListData 接口的数据源。WinJS 库包含了两个实现了此数据源的对象：

- WinJS.Binding.List—允许你将 JavaScript 数组作为数据源
- WinJS.UI.Storage—允许你将计算机硬盘上的文件作为数据源。





## 186 第 7 章 使用 ListView 控件

在本章中，我们重点关注使用 `WinJS.Binding.List` 数据源，因为这是最灵活的数据源。你可以从任何 JavaScript 数组创建 `WinJS.Binding.List` 数据源的实例。

例如，你可以对远程服务器执行 Ajax 请求并检索产品数组。然后，你可以使用 ListView 控件配合 `List` 数据源显示该产品数组。

> 注意
> 无论使用 WinJS.Binding.List 还是 WinJS.UI.Storage 数据源，你都可以创建自定义数据源并将其与 ListView 控件配合。如果你需要使用 ListView 控件显示来自 IndexedDB 数据库的数据，你可能需要创建一个自定义数据源。我们将在下一章中创建几个自定义数据源——包括一个 IndexedDB 数据源。

让我们看看如何配合 `WinJS.Binding.List` 数据源使用 ListView 控件。列表 7.1 中的页面包含一个 ListView 控件，它用于显示一组产品（见图 7.1）。

### 列表 7.1 绑定到列表数据源 (simple.html)

```html
<!DOCTYPE html>
<html
<head>
    <meta charset="utf-8" />
    <title>Chapter05</title>
    <!-- WinJS references --
    <link href="//Microsoft.WinJS.1.0.RC/css/ui-dark.css" rel="stylesheet" />
    <script src="//Microsoft.WinJS.1.0.RC/js/base.js"></script>
    <script src="//Microsoft.WinJS.1.0.RC/js/ui.js"></script>
    <!-- Chapter05 references --
    <link href="simple.css" rel="stylesheet" />
    <script src="simple.js"></script>
</head>
<body>
    <div id="tmplProduct">
        <div data-control="WinJS.Binding.Template">
            <div>
                <h2 data-win-bind="innerText:name"></h2>
                Price: <span data-win-bind="innerText:price"></span>
            </div>
        </div>
    </div>
</body>
</html>
```

### ListView 控件简介

```html
<div id="lvProducts"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplProduct')
  }"></div>
```

列表 7.1 中的 ListView 控件使用模板来渲染每个产品。该模板包含在 id 为 `tmplProduct` 的 Template 控件中。

> 警告
> 请确保在 ListView 控件之前在页面中声明 Template 控件，否则你将得到一个神秘且难以调试的异常。

列表 7.2 中的 JavaScript 文件包含产品数组。从产品数组创建了一个 `WinJS.Binding.List` 对象，并在 `itemDataSource` 属性的帮助下将该 `List` 对象绑定到 ListView 控件。当你查看页面时，你会看到来自 JavaScript 数组的产品列表。

### 列表 7.2 绑定到列表数据源 (simple.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 ListViewById 的引用
      var lvProducts = document.getElementById("lvProducts").winControl;

      // 创建产品列表
      var listProducts = new WinJS.Binding.List(
        { name: "Bread", price: 2.20 },
        { name: "Cheese", price: 1.19 },
        { name: "Milk", price: 2.33 },
        { name: "Apples", price: 5.20 },
        { name: "Steak", price: 12.99 }
      );

      // 将产品列表绑定到 ListView
      lvProducts.itemDataSource = listProducts.dataSource;
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_201_0.png)

图 7.1 显示产品列表

你可以将任何内容放入 JavaScript 数组中：数据库查询结果、Ajax 调用结果、斐波那契数列。正由于这个原因，当你将 ListView 控件绑定到 `List` 时，你可以绑定到几乎任何类型的数据。

例如，列表 7.3 中的 ListView 显示了从博客馈送（blog feed）检索的博客文章列表。

- 列表 7.3 绑定到博客馈送 (blog.html)

```html
<div id="tmpBlog" data-win-control="WinJS.Binding.Template">
  <div>
    <span data-win-bind="innerHTML:title.text; WinJS.Binding.oneTime"></span>
  </div>
</div>

<div id="lvBlog"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplBlog')
  }"></div>
```

## 188 第 7 章 使用 ListView 控件

### ListView 控件简介

博客文章列表是通过 `Syndication` 类从 http://stephen.com/ 的博客馈送中检索的。

### 列表 7.4 绑定到博客馈送 (blog.html)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 lvBlog 的引用
      var lvBlog = document.getElementById("lvBlog").winControl;

      // 获取馈送
      var client = new Windows.Web.Data.Syndication.SyndicationFeed();
      var feedURI = new Uri("http://stephen.com/");
      client.GetFeedAsync(feedURI).then(function (feed) {
        // 从项目创建列表
        var list = new WinJS.Binding.List(feed.Items);
        // 绑定到 ListView
        lvBlog.itemDataSource = list.dataSource;
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

ListView 控件支持两种布局：网格布局（grid layout）和列表布局（list layout）。默认布局是网格布局。当 ListView 使用网格布局时，项目将多列显示。如果项目过多无法放入 ListView，你可以向右滚动查看更多项目（见图 7.3）。

> 注意
> 网格布局使用了 W3C CSS Grid 建议。你可以在此处查看详细信息：http://dev.w3.org/css3-grid-layout/

## 191 ListView 控件简介

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_204_0.png)

图 7.3 使用网格布局的 ListView

当 ListView 使用网格布局时，你可以设置 `maxRows` 属性来设定应显示的最大网格行数。以下是设置 `maxRows` 使 ListView 只显示一行的方法（见图 7.4）：

```html
<div id="lvProducts"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplProduct'),
    layout: {type:WinJS.UI.GridLayout, maxRows:1}
  }"></div>
```

ListView 控件另一种布局模式是列表布局。在列表布局模式下，项目垂直显示。如果所有项目都无法放入 ListView，你可以垂直滚动 ListView（见图 7.5）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_205_1.png)

图 7.5 使用列表布局的 ListView 控件




# ListView 控制介绍

```html
<div id="lvProducts"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: itemTemplate='#tmplProduct',
    layout: {type:WinJS.UI.ListView}
  }">
</div>
```

ListView 的项目是以列表布局渲染的，因此这些项目实际上并不是使用 HTML 的 UL 和 LI 元素显示的。相反，每个项目都会渲染成一个 DIV 元素。

# 防止 ListView 项目重叠

在网格模式下在 ListView 控制中显示项目可能会令人沮丧，除非你理解 ListView 控制用于显示每个项目的技巧。

请考虑图 7.6 所示的 ListView。该 ListView 显示了 7 个项目：
AA
BBBBBBBB
CC
DD
EE
FF
GG

然而，BBBBBBBB 重叠了下一列的 FF 列表项目。宽大的 B 项目破坏了 ListView 的渲染。这看起来并不美观！

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_206_0.png)

图 7.6 重叠 ListView 项目

如果你将 BBBBBBBB 项目移动到列表顶部，重叠问题就会消失（图 7.7）。所有项目都按照 BBBBBBBB 项目的宽度进行渲染。然而，现在的问题是 ListView 中的每个项目宽度都和 BBBBBBBB 一样，这看起来很奇怪。

# 第 7 章 使用 ListView 控制

| BBBBBB | EE |
| AA | FF |
| CC | GG |
| DD | |

图 7.7 不重叠但超宽的 ListView 项目

这就是 ListView 用于计算每个列表项目宽度和高度的技巧。ListView 仅计算第一个项目的宽度和高度，并将该宽度和高度用于所有其他项目。

由于 ListView 控制计算列表项目宽度和高度的方式，我建议你始终显式地指定项目的宽度和高度。否则，根据第一个项目的宽度和高度，你可能会得到重叠或不必要的宽或过高的列表项目。

那么，如何显式地指定列表项目的宽度和高度呢？当 ListView 渲染其项目时，项目是在类似这样的 DIV 元素中渲染的：

```html
<div class="win-listview">
  <div class="win-container" style="width:142px;height:54px">
    <div class="win-item">
      AAAA
    </div>
  </div>
  <div class="win-container" style="width:142px;height:54px">
    <div class="win-item">
      BBBB
    </div>
  </div>
  <div class="win-container" style="width:142px;height:54px">
    <div class="win-item">
      CCCC
    </div>
  </div>
  ... 以此类推 ...
</div>
```

为了简单起见，我省略了多级嵌套的 DIV。但基本思想是 ListView 为每个列表项目渲染一个 win-container DIV 元素，该元素包含一个 win-item DIV 元素。

# ListView 控制介绍

注意，每个 win-container DIV 元素都有一个带有显式宽度和高度的 style 属性。所有的 win-container DIV 元素具有相同的宽度和高度。ListView 控制根据第一个列表项目的大小分配宽度和高度。

由于 style 属性的高于 win-container 类属性，你尝试用 win-container 类分配的任何宽度和高度将被忽略。

在网格布局模式下，你可以使用 win-item 类为每个列表项目提供显式的宽度和高度。然而，在列表布局模式下 win-item 类会导致其他问题。注意图 7.8 中的灰色背景没有延伸到最侧。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_208_0.png)

图 7.8 灰色选择背景宽度不够

这是我推荐的解决方案。该解决方案同时适用于网格和列表布局模式。我建议你始终在 ListView 控制的项目模板中提供一个带有关联类的 DIV 元素。例如，以下模板包含一个 productItem DIV 元素：

```html
<div id="emplProduct"
  data-win-control="WinJS.Binding.Template">
  <div class="productitem">
    <h2 data-bind="innerText:name"></h2>
  </div>
</div>
```

使用网格布局时，你应该始终为 productItem 提供显式的宽度和高度。例如，以下 productItem 类：



```html
<div class="categoryItem">
  <h2 data-win-bind="innerText:categoryName"></h2>
</div
```

```html
<div id="tmplProduct"
  data-win-control="WinJS.Binding.Template">
  <div class="productItem">
    <h2 data-win-bind="innerText:productName"></h2>
    Price: <span data-win-bind="innerText:price"></span>
  </div>
</div
```

```html
<div id="container">
<!-- Categories主列表 ListView -->
<div id="lvCategories"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    select('#tmplCategory'),
    selectionMode: 'single',
    tapBehavior: 'directSelect',
    swipeBehavior: 'select',
    layout: {type: WinJS.UI.ListAdapter}
  }"></div

<!-- Products详情列表 ListView -->
<div id="lvProducts"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    select('#tmplProduct'),
    selectionMode: 'none',
    layout: {type: WinJS.UI.ListAdapter}
  }"></div
```

请注意，分类 ListView——ID 为 `lvCategories` 的 ListView——设置了 `selectionMode`、`tapBehavior` 和 `swipeBehavior` 属性。你可以通过点击或滑动来选择类别。

列表 7.6 中的 JavaScript 文件包含了在选择某个类别时显示相应产品的代码。

# 列表 7.6 创建主/详情表单 (masterDetail\masterDetail.js)

```javascript
(function () {
  "use strict"

function initialize() {
  WinJS.UI.processAll().done(function () {
    // 获取 ListView 控件的引用
    var lvProducts = document.getElementById("lvProducts").winControl;
    var lvCategories = document.getElementById("lvCategories").winControl;

    // 创建类别和产品的数组
    var products = [
      {
        categoryName: "Beverages",
        products: [
          { productName: "Pepsi", price: 4.00 },
          { productName: "Milk", price: 2.11 },
          { productName: "Moxie", price: 1.33 }
        ]
      },
      {
        categoryName: "Meat",
        products: [
          { productName: "Steak", price: 34.33 },
          { productName: "Chicken", price: 2.01 }
        ]
      },
      {
        categoryName: "Fruit",
        products: [
          { productName: "Apples", price: 2.88 },
          { productName: "Oranges", price: 7.01 }
        ]
      }
    ];
    // 创建类别和产品的列表
    var listProducts = new WinJS.Binding.List(products);

    // 将列表绑定到分类 ListView
    lvCategories.itemDataSource = listProducts.dataSource;

    // 处理 selectionchanged 事件
    lvCategories.addEventListener("selectionchanged", function () {
      if (lvCategories.selection.count() > 0) {
        lvCategories.selection.getItems().done(function (items) {
          // 获取第一个选中项的产品
          var selectedProducts = items[0].data.products;

          // 转换为列表
          var listSelectedProducts = new WinJS.Binding.List(selectedProducts);

          // 绑定到产品 ListView
          lvProducts.itemDataSource = listSelectedProducts.dataSource;

        });
      }
    });
  });
});

document.addEventListener("DOMContentLoaded", initialize);
}();
```

类别和相关产品都包含在一个名为 `products` 的单一 JavaScript 数组中。在转换为 `WinJS.Binding.List` 后，该数组被绑定到分类 ListView 上。

当你选择一个类别时（无论通过点击还是滑动），会触发 ListView 的 `selectionchanged` 事件。列表 7.6 中的代码包含了一个用于此事件的句程序：

```javascript
// 处理 selectionchanged 事件
lvCategories.addEventListener("selectionchanged", function () {
    if (lvCategories.selection.count > 0) {
        lvCategories.selection.getItems().done(function (items) {
            // 获取第一个选中项的产品
            var selectedProducts = items[0].data.products;

            // 转换为列表
            var listSelectedProducts = new WinJS.Binding.List(selectedProducts);

            // 绑定到产品 ListView
            lvProducts.itemDataSource = listSelectedProducts.dataSource;
        });
    }
});
```

# 使用 ListView 控件

调用 ListView 的 `selection.getItems()` 方法来获取所选的类别。该方法返回一个 promise。在 promise 的 `done` 处理程序中，获取与所选类别相关的产品并将其转换为 `WinJS.Binding.List`。该列表被绑定到产品 ListView，并显示匹配的产品。

# 选择多项

如果你将 ListView 控件的 `selectionMode` 属性设置为值 `'multi'`，那么你就可以同时选择多个 ListView 列表项。假设你想显示一个产品列表，并允许客户将多个产品添加到购物车中（请见图 7.12）。在这种情况下，你可以使用两个 ListView 控件来显示产品和购物车（见列表 7.7）。

![](img/3fb402034fe87fec8b9c70eeae6c75_215_0.png)

图 7.12 选择多项

# 列表 7.7 选择多项 (selectMultiple.html)

```html
<!-- 模板 -->

<div id="tmplProduct"
  data-win-control="WinJS.Binding.Template">
    <div class="productItem">
      <h2 data-win-bind="innerText:productName"></h2>
      Price: <span data-win-bind="innerText:price"></span>
    </div>
</div>

<div id="tmplShoppingCart"
  data-win-control="WinJS.Binding.Template">
    <div class="shoppingCartItem">
      <h2 data-win-bind="innerText:productName"></h2>
    </div>
</div
```

```html
<div id="container">
  <div id="containerProducts">
    <h1>Products ListView</h1>
    <!-- Products ListView -->
    <div id="lvProducts"
      data-win-control="WinJS.UI.ListView"
      data-win-options="{
        itemTemplate: '#tmplProduct',
        selectionMode: 'multi',
        tapBehavior: 'toggleSelect',
        swipeBehavior: 'select'
      }"></div>
  </div>
  <div id="containerShoppingCart">
    <h1>Shopping Cart</h1>
    <!-- Shopping Cart ListView -->
    <div id="lvShoppingCart"
      data-win-control="WinJS.UI.ListView"
      data-win-options="{
        itemTemplate: '#tmplShoppingCart',
        selectionMode: 'none',
        layout: {type: WinJS.UI.ItemLayout}
      }"></div>
  </div>div
```

产品 ListView——ID 为 `lvProducts` 的 ListView——其 `selectionMode` 设置为值 `'multi'`，`tapBehavior` 设置为值 `'toggleSelect'`。值 `'toggleSelect'` 在点击项时会在选中和未选中状态之间切换。

列表 7.8 包含了将选中项复制到购物车的代码。当你选择一个项时，会触发 `selectionChanged` 事件，选中项会被复制到一个新的数组中。该数组被转换为 `WinJS.Binding.List`。

# 列表 7.8 选择多项 (selectMultiple\selectMultiple.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 ListView 控件的引用
      var lvProducts = document.getElementById("lvProducts").winControl;
      var lvShoppingCart = document.getElementById("lvShoppingCart").winControl;

      // 创建产品列表
      var listProducts = new WinJS.Binding.List([
        { productName: "Bread", price: 2.20 },
        { productName: "Cheese", price: 1.19},
        { productName: "Milk", price: 2.33 },
        { productName: "Apples", price: 5.20 },
        { productName: "Steak", price: 12.99 }
      ]);

      // 将列表绑定到产品 ListView
      lvProducts.itemDataSource = listProducts.dataSource;

      // 处理 selectionchanged 事件
      lvProducts.addEventListener("selectionchanged", function () {
        lvProducts.selection.getItems().done(function (items) {
          // 将选中项复制到新数组
          var selectedProducts = [];
          items.forEach(function (item) {
            selectedProducts.push(item.data);
          });

          // 将选中产品转换为 List
          var listProducts = new WinJS.Binding.List(selectedProducts);

          // 将列表绑定到购物车
          lvShoppingCart.itemDataSource = listProducts.dataSource;
        });
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
}();
```

![](img/3fb402034fe87fec8b9c70eeae6c75_216_0.png)

#  ListView 控件中的项

你可以通过对 ListView 的数据源进行排序来排序显示的项。例如，你可能想按产品名称或价格对列表进行排序。

`WinJS.Binding.List` 对象支持 `createSorted()` 方法。该方法接受一个排序函数，该函数返回一个根据该函数排序的新的 `WinJS.Binding.List`。





# 在 ListView 控制中排序项目

例如，以下代码按产品名称对产品列表进行排序：

```javascript
// 创建产品列表
var listProducts = new WinJS.Binding([
  { name: "Bread", price: 2.20 },
  { name: "Cheese", price: 1.19 },
  { name: "Milk", price: 2.33 },
  { name: "Apples", price: 5.20 },
  { name: "Steak", price: 12.99 }
]);

// 对产品排序
var sortedListProducts = listProducts.createSorted(function(item1, item2) {
  return item1.name > item2.name ? 1 : -1;
});

// 将产品列表绑定到 ListView
lvProducts.itemDataSource = sortedListProducts.dataSource;
```

上述代码使用 `createSorted()` 方法根据原始未排序的产品数据源创建一个新的排序后的数据源。ListView 绑定到新的数据源，而不是原始数据源。

在上述代码中，使用以下排序函数对产品进行排序：

```javascript
function (item1, item2) {
  return item1.name > item2.name ? 1 : -1;
}
```

排序函数通过返回三个可能值之一对项目进行排序：

- 0—当两个项目应该按相同顺序排序时。
- -1—当第一个项目应该在第二个项目之前排序时。
- 1—当第一个项目应该在第二个项目之后排序时。

`sortedListData` 数据源是一个活动数据源。如果你向 `listProducts` 数据源添加新项，新项将按正确的顺序出现在 ListView 中。对 `listProducts` 数据源的更改会被自动获取。

> 注意
你可以在 WinJS `createSorted()` 方法中使用相同类型的排序函数，这与你使用标准 JavaScript 数组 `sort()` 方法时相同。

# 在 ListView 控制中过滤项目

你可以通过过滤与 ListView 关联的数据源中的项目来过滤显示在 ListView 中的项目。例如，在浏览大量产品时，你可能希望允许用户通过仅显示匹配过滤字符串的产品来过滤产品（见 7.13 节）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_219_0.png)

图 7.13 过滤产品列表

你可以通过调用 `createFiltered()` 方法对现有的 WinJS.Binding.List 创建一个新的过滤后的 `WinJS.Binding.List`。该方法接受一个过滤函数，该函数返回 true 或 false，取决于原始列表中的项目是否应该包含在新列表中。

列表 7.9 和 7.10 中的代码说明了如何使用 `createFiltered()` 方法创建一个键盘按键搜索表单。列表 7.9 中的页面包含一个输入框和一个 ListView 控件。

列表 7.9 过滤产品列表 (filtering.html)

```html
<<div>
  <input id="inputFilter" />
</div>
<div id="tmplProduct" data-win-control="WinJS.Binding.Template">
    <div class="productItem">
      <h2 data-win-bind="innerText:name"></h2>
      Price: <span data-win-bind="innerText:price"></span>
    </div>
</</div>

<div id="lvProducts"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplProduct')
  }">
</div>

```

# 在 ListView 控制中过滤项目

列表 7.10 中的 JavaScript 代码过滤了 ListView，使其只显示匹配过滤字符串的产品。

# 列表 7.10 过滤产品列表 (filtering.js)

```javascript
(function () {
  "use strict";

  // 创建产品列表
  var listProducts = new WinJS.Binding.List([
    { name: "Bread", price: 2.20 },
    { name: "Broccoli", price: 1.19 },
    { name: "Bananas", price: 2.33 },
    { name: "Apples", price: 5.20 },
    { name: "Apple Sauce", price: 12.99 }
  ]);

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 DOM 元素和控件的引用
      var lvProducts = document.getElementById("lvProducts").winControl;
      var inputFilter = document.getElementById("inputFilter");

      // 将未过滤的产品列表绑定到 ListView
      lvProducts.itemDataSource = listProducts.data;

      inputFilter.addEventListener("keyup", function () {
        // 过滤数据源
        var filteredProducts = listProducts.createFiltered(function (item) {
          return item.name.toLowerCase().indexOf(inputFilter.value) == 0;
        });

        // 将产品列表绑定到 ListView
        lvProducts.itemDataSource = filteredProducts.data;
      });
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

这里是使用 `createFiltered()` 方法的代码部分：

```javascript
// 过滤数据源
var filteredListProducts = listProducts.createFiltered(function (item) {
    return item.name.toLowerCase().indexOf(inputFilter.value) == 0;
});
```

```javascript
// 将列表绑定到 ListView
lvProducts.itemDataSource = filteredListProducts.dataSource;
```

传递给 `createFiltered()` 方法的函数决定了过滤后的产品列表包含哪些项目。该函数仅匹配数据源中以输入框中输入的文本开头的项目。因此，如果你在输入框中输入 "br"，则会匹配 "Bread" 和 "Broccoli"，但不会匹配 "Bananas"。

# 在 ListView 中分组项目

你可以对显示在 ListView 控件中的项目进行分组。例如，与其扁平的产品列表，不如按类别对产品进行分组（见图 7.14）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_221_0.png)

图 7.14 分组 ListView 项目

如果你想利用分组功能，你需要创建一个分组数据源。你通过调用 `WinJS.Binding.List createGrouped()` 方法创建一个分组数据源。

列表 7.11 和列表 7.12 中的代码说明了如何使用 `createGrouped()` 方法按类别对产品进行分组。

列表 7.11 分组 ListView 项目 (grouped.html)

```html
<!-- 模板 -->
<div id="tmplGroupHeader" data-control="WinJS.Binding.Template">
    <div class="productGroupHeader">
        <h1 data-win-bind="innerText: title"></h1>
    </div>
</div>
```

```html
<div id="tmplProduct" data-win-control="WinJS.Binding.Template">
  <div class="productItem">
    <h2 data-win-bind="innerText:name"></h2>
    Price: <span data-win-bind="innerText:price"></span>
  </div>
</div>

<div id="lvProducts"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplProduct'),
    groupHeaderTemplate: select('#tmplGroupHeader')
  }">
</div>
```

7.11 中的 HTML 页面包含两个模板：一个用于分组头，一个用于单个项目。分组头通过 `groupHeader` 属性声明式与 ListView 控件关联。

> 注意
ListView 在网格模式下支持分组。

# 列表 7.12 分组 ListView 项目 (grouped.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 DOM 元素和控件的引用
      var lvProducts = document.getElementById("lvProducts").winControl;

      // 创建产品列表
      var listProducts = new WinJS.Binding.List([
        { name: "Milk", price: 2.44, category: "Beverages" },
        { name: "Oranges", price: 1.99, category: "Fruit" },
        { name: "Wine", price: 8.55, category: "Beverages" },
        { name: "Apples", price: 2.44, category: "Fruit" },
        { name: "Steak", price: 19.99, category: "Other" },
        { name: "Eggs", price: 2.44, category: "Other" },
        { name: "Mushrooms", price: 19.99, category: "Other" },
        { name: "Yogurt", price: 2.44, category: "Other" },
        { name: "Soup", price: 19.99, category: "Other" },
        { name: "Cereal", price: 2.44, category: "Other" },
        { name: "Pepsi", price: 1.99, category: "Beverages" }
      ]);

      // 创建分组数据源
      var groupProducts = listProducts.createGrouped(
        function (dataItem) {
          return dataItem.category;
        },
        function (dataItem) {
          return { title: dataItem.category };
        },
        function (group1, group2) {
          return group1 > group2 ? 1 : -1;
        }
      );

      // 将产品列表绑定到 ListView
      lvProducts.groupDataSource = groupProducts.groups.dataSource;
      lvProducts.itemDataSource = groupProducts.dataSource;
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```





# 使用语义缩放切换视图 211

这两个数据源——分组数据源和项目数据源——通过以下两行代码绑定到 `ListView` 控件：

```
// 将产品列表绑定到 ListView
lvProducts.groupDataSource = groupListProducts.groups.dataSource;
lvProducts.itemDataSource = groupListProducts.dataSource;
```

分组数据源是一个实时数据源——因此，当你更改数据源时，`ListView` 显示的分组随之更改。此外，你可以将分组数据源与过滤后的数据源配合使用。

# 使用语义缩放切换视图

语义缩放（Semantic Zoom）是 Windows 8 的一项功能，允许你在两个不同的缩放级别查看数据。例如，Windows 8 的开始屏幕利用了语义缩放。默认情况下，当你打开开始屏幕时，你看到的是应用的特视图（见图 7.15）。然而，你可以缩小以查看应用的更远景视图（见图 7.16）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_224_0.png)

图 7.15 默认开始屏幕

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_225_0.png)

使用鼠标时，可以通过点击屏幕右下角出现的 – 按钮来缩小。使用触摸屏时，可以使用捏合和拉伸手势来放大和缩小。

你可以通过利用 WinJS `SemanticZoom` 控件在你的 Windows Store 应用中实现语义缩放。与 `ListView` 控件配合使用时，`SemanticZoom` 控件允许你为相同数据提供两种视图：百英视图（hundred foot view）和十英视图（ten foot view）。

假设你正在处理大量产品，这些产品可以按类别分组。为了方便用户导航到不同的类别，你可以利用语义缩放。默认情况下，你会看到按类别分组的产品（图 7.17）。然而，如果你缩小视图，就可以看到类别列表（图 7.18）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_226_0.png)

图 7.17 使用语义缩放（十英视图）

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_226_1.png)

图 7.18 使用语义缩放（百英视图）

列表 7.13 中的 HTML 页面说明了你如何实现语义缩放。该页面包含一个 `SemanticZoom` 控件，它有两个子 `ListView` 控件。不同的 `ListView` 在不同的缩放级别下显示。

列表 7.13 使用语义缩放缩放 (semanticZoom\semanticZoom.html)

```
<!-- 放大模板 -->
<div id="tmplProductGroupHeader" data-win-control="WinJS.Binding.Template">
  <div class="productGroupHeader">
    <h1 data-win-bind="innerText: title"></h1>
  </div>
</div>

<div id="tmplProduct" data-win-control="WinJS.Binding.Template">
  <div class="productItem">
    <h2 data-win-bind="innerText:name</h2>
    Price: <span data-win-bind="innerText:price"></span>
  </div>
</div>

* With Item *
```

```
</div>

<!-- 缩小模板 -->
<div id="tmpCategory" data-win-control="WinJS.Binding.Template">
  <div class="categoryItem">
    <h2 data-bind="innerText:title</h2>
  </div>
</div>
</div>
```

```
<!-- SemanticZoom 和 ListViews -->
<div id="SemanticZoom" data-win-control="WinJS.UI.SemanticZoom">
  <!-- 放大 ListView (产品) -->
  <div id="lvProducts"
    data-win-control="WinJS.UI.ListView"
    data-win-options="{
      itemTemplate: select('#tmplProduct'),
      groupHeaderTemplate: select('#tmplGroupHeader')
    }">
  <!-- 缩小 ListView (类别) -->
  <div id="lvCategories"
    data-win-control="WinJS.UI.ListView"
    data-win-options="{
      itemTemplate: select('#tmplCategory')
    }">
  </div>
</div>
```

这里是列表 7.13 中使用 `SemanticZoom` 控件的代码行：

```
<div id="SemanticZoom" data-win-control="WinJS.UI.SemanticZoom">
  <!-- 放大 ListView (产品) -->
  <div id="lvProducts"
    data-win-control="WinJS.UI.ListView"
    data-win-options="{
      itemTemplate: select('#tmplProduct'),
      groupHeaderTemplate: select('#tmplGroupHeader')
    }">
  <!-- 缩小 ListView (类别) -->
  <div id="lvCategories"
    data-win-control="WinJS.UI.ListView"
    data-win-options="{
      itemTemplate: select('#tmplCategory')
    }">
  </div>
</div>
```

# 使用语义缩放切换视图 228

`SemanticZoom` 控件包含两个具有不同缩放级别的 `ListView` 控件。它在两个 `ListView` 之间切换，显示其中某一个缩放级别。

列表 7.14 中的 JavaScript 文件包含了实现语义缩放的代码。表示产品列表的数据源被绑定到缩放后的 `ListView`。此外，一个分组数据源被绑定到放大和缩小的两个 `ListView` 控件。

# 列表 7.14 使用语义缩放缩放 (semanticZoom\semanticZoom.js)

```
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 ListView 控件的引用
      var lvProducts = document.getElementById("lvProducts").winControl;

      // 创建产品列表
      var products = new WinJS.Binding.List(
        { name: "Milk", price: 2.44 },
        { name: "Oranges", price: 1.99 },
        { name: "Wine", price: 8.55 },
        { name: "Apples", price: 2.44 },
        { name: "Steak", price: 1.99 },
        { name: "Eggs", price: 2.44 },
        { name: "Mushrooms", price: 1.99 },
        { name: "Yogurt", price: 2.44 },
        { name: "Soup", price: 1.99 },
        { name: "Cereal", price: 2.44 },
        { name: "Pepsi", price: 1.99 }
      );

      // 创建分组数据源
      var groupListProducts = products.createGroup(
        function (dataItem) {
          return dataItem.category;
        },
        function (dataItem) {
          return dataItem.title;
        },
        function (dataItem) {
          return dataItem.onSale;
        }
      );

      // 将产品列表绑定到放大的 ListView
      lvProducts.itemDataSource = groupListProducts.dataSource;
      // 将分组数据源绑定到放大的 ListView
      lvProducts.groupDataSource = groupListProducts.groups.dataSource;

      // 将类别列表绑定到缩小的 ListView
      lvCategories.itemDataSource = groupListProducts.dataSource;
      // 将分组数据源绑定到缩小的 ListView
      lvCategories.groupDataSource = groupListProducts.groups.dataSource;
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```

# 动态切换 ListView 模板

你可以动态设置 `ListView` 控件的 `itemTemplate` 属性。这很棒，因为你可以在运行时切换所使用的模板。例如，你想要使用两个模板显示产品：一个普通产品模板和一个促销产品模板（见图 7.19）。

| 产品 | 价格 |
| :--- | :--- |
| Bread | 2.44 |
| Sushi | 1.99 |
| Eggs | 8.55 |
| (On Sale!) | 2.44 |
| Milk | 1.99 |
| (On Sale!) | 2.44 |
| Apples | 1.99 |

图 7.19 使用语义缩放切换模板

列表 7.15 切换模板 (dynamicTemplate.html)

```html
<!-- 放大模板 -->
<div id="tmplProductGroupHeader" data-win-control="WinJS.Binding.Template">
  <div class="productGroupHeader">
    <h1 data-win-bind="innerText: title"></h1>
  </div>
</div>

<div id="tmplProduct" data-win-control="WinJS.Binding.Template">
  <div class="productItem">
    <h2 data-win-bind="innerText:name</h2>
    Price: <span data-win-bind="innerText:price"></span>
  </div>
</div>

* With Item *
```

```html
</div>

<!-- 缩小模板 -->
<div id="tmpCategory" data-win-control="WinJS.Binding.Template">
  <div class="categoryItem">
    <h2 data-bind="innerText:title</h2>
  </div>
</div>
</div>
</div>
```

```html
<!-- SemanticZoom 和 ListViews -->
<div id="SemanticZoom" data-win-control="WinJS.UI.SemanticZoom">
  <!-- 放大 ListView (产品) -->
  <div id="lvProducts"
    data-win-control="WinJS.UI.ListView"
    data-win-options="{
      itemTemplate: select('#tmplProduct'),
      groupHeaderTemplate: select('#tmplGroupHeader')
    }">
  <!-- 缩小 ListView (类别) -->
  <div id="lvCategories"
    data-win-control="WinJS.UI.ListView"
    data-win-options="{
      itemTemplate: select('#tmplCategory')
    }">
  </div>
</div>
</div>
```

普通产品模板和促销模板之间的唯一区别是促销模板包含了“On Sale!”消息。注意，`ListView` 控件使用的模板并不是声明式设置的；相反，我们在列表 7.16 的 JavaScript 文件中通过命令式进行设置。

# 列表 7.16 动态切换模板 (dynamicTemplate\dynamic.js)

```javascript
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 ListView 控件的引用
      var lvProducts = document.getElementById("lvProducts").winControl;

      // 创建产品列表
      var listProducts = new WinJS.Binding.List(
        { name: "Milk", price: 2.44 },
        { name: "Oranges", price: 1.99 },
        { name: "Wine", price: 8.55 },
        { name: "Apples", price: 2.44 },
        { name: "Steak", price: 12.99 },
        { name: "Eggs", price: 2.44 },
        { name: "Mushrooms", price: 1.99 },
        { name: "Yogurt", price: 2.44 },
        { name: "Soup", price: 1.99 },
        { name: "Cereal", price: 2.44 },
        { name: "Pepsi", price: 1.99 }
      );

      // 分配一个项目模板函数
      lvProducts.itemTemplate = function (itemPromise) {
        return itemPromise.then(function (item) {
          // 选择普通产品模板或促销产品模板
          if (item.onSale) {
            return document.getElementById("tmplProductOnSale");
          } else {
            return document.getElementById("tmplProduct");
          }
        });
      };
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})();
```




# 第 7 章 使用 ListView 

```
var itemTemplate = document.getElementById("tmplProduct");
if (item.data.onSale) {
  itemTemplate = document.getElementById("tmplProductOnSale");
}

// 将选定的模板渲染到DIV容器
var container = document.createElement("div");
itemTemplate.winControl.render(item.data, container);
return container;
};

// 将产品列表绑定到 ListView
lvProducts.itemDataSource = listProducts.dataSource;
});
document.addEventListener("DOMContentLoaded", initialize);
}();
```

动态模板切换发生在以下代码段，需要对其进行解释：

```
lvProducts.itemTemplate = function (itemPromise) {
  return itemPromise.then(function (item) {
    // 选择普通产品模板或特价模板
    var itemTemplate = document.getElementById("tmplProduct");
    if (item.data.onSale) {
      itemTemplate = document.getElementById("tmplProductOnSale");
    }

    // 将选定的模板渲染到DIV容器
    var container = document.createElement("div");
    itemTemplate.winControl.render(item.data, container);
    return container;
  });
};
```

当每个 ListView 项目被渲染时，一个 promise会被传递给该函数。与 ListView 项目关联的数据项在 promise 完成之前是不可用的。注意，传递给函数的 `item` 参数包含一个 `data` 属性，该属性代表与 ListView 项目关联的数据项。你可以使用 `item.data.onSale` 属性来判断产品是否正在特价。

当 promise 完成时，你可以返回用于渲染 ListView 项目的 HTML 片段。在上面的代码中，HTML 片段是通过 `tmplProduct` 模板（用于普通产品）或 `tmplProductOnSale` 模板（用于特价产品）辅助渲染的。模板被渲染到名为 `container` 的 DOM 元素，并由该函数返回。

## 增量加载 ListView 项目

假设你想使用 ListView 控件滚动浏览巨大的产品目录。例如，一个包含数千种产品的目录。你如何高效地滚动如此庞大的目录呢？

ListView 控件自动支持对包含数千个项的数据源进行随机访问，ListView 将加载和渲染显示当前页和下一页所需的项子集。因此，ListView 可能只需要加载和渲染少数项，而不是渲染数千个项。

当数据项可以快速加载时，这种方法非常有效。然而，当数据项需要跨网络加载（通过 Ajax 调用）时，这种方法并不理想。在这种情况下，为了提供流畅的用户体验，你需要增量加载由 ListView 控件显示的项。

以下属性用于控制 ListView 如何从数据源加载项：

-   automaticallyLoadPages—获取或设置一个布尔值，决定 ListView 控件是否会自动加载额外页面。当用户滚动范围超过 `pagesToLoadThreshold` 指定的页数时，会自动加载额外页面。

-   loadingBehavior—获取或设置 ListView 加载额外项的策略。两个可能的值是"randomaccess"随机访问）和"incremental"增量）。

-   loadingState—获取一个表示 ListView 加载状态的字符串。两个可能的值是"complete"已完成）和"loading"加载中）。

-   pagesToLoad—获取或设置一个整数，确定要加载的新页数。当启用 `automaticallyLoadPages` 或调用 `loadPages()` 方法时，会使用此属性。

-   pagesToLoadThreshold—获取或设置一个整数值，决定何时加载一组新页面。当启用 `automaticallyLoadPages` 时，用户滚动超过 `pagesToLoadThreshold`，则会自动加载新页面。

你可以使用以下方法手动触发 ListView 控件加载更多项：

-   loadMorePages—当 `loadingBehavior` 的值为 "incremental" 时，它会促使 ListView 控件加载更多页的项目。加载项的数量由 `pagesToLoad` 属性决定。

最后，ListView 控件在加载项的过程中会引发以下事件：

-   loadingstatechanged—当 ListView 控件完成加载时触发。

ListView 控件的 `loadingBehavior` 属性决定 ListView 是否增量地加载项。当启用增量加载时，你可以通过设置 `automaticallyLoadPages` 属性来选择自动或手动加载额外页面。

例如，列表 7.17 中的 JavaScript 创建了一个包含 10,000 个产品的数组（一个非常大的产品目录）。

# 列表 7.17 增量加载 ListView 项目 (incremental.js)

```
(function () {
  "use strict";

  function initialize() {
    WinJS.UI.processAll().done(function () {
      // 获取 ListView 的引用
      var lvProducts = document.getElementById("lvProducts").winControl;

      // 创建一个产品数组
      var products = [];
      for (var i = 0; i < 10000; i++) {
        products.push({
          name: "Product " + i,
          price: Math.floor(Math.random() * 5000) + 1
        });
      }

      // 创建产品列表
      var listProducts = new WinJS.Binding.List(products);

      // 启用增量加载
      lvProducts.loadingBehavior = "incremental";
      lvProducts.automaticallyLoadPages = true;
      lvProducts.pagesToLoad = 10;

      // 将产品列表绑定到 ListView
      lvProducts.itemDataSource = listProducts.dataSource;
    });
  }

  document.addEventListener("DOMContentLoaded", initialize);
})()
```

在列表 7.17 中，通过以下代码行启用了增量加载：
lvProducts.loadingBehavior = "incremental";
lvProducts.automaticallyLoadPages = true;
lvProducts.pagesToLoad = 10;

当 ListView 首次渲染时，它仅显示前 152 个 ListView 项目。当你滚动到 ListView 项目的末尾附近时，将检索并显示下一批 152 个 ListView 项目。这些项是增量添加到 ListView 中的。

## 注意

ListView 加载的项的精确数量取决于每页可以显示的项数。注意，你使用 ListView 的 `pagesToLoad` 属性来指定页数，而不是加载项的数量。ListView 加载项的精确数量取决于 ListView 的宽度和高度以及 ListView 项目的宽度和高度。ListView 将计算屏幕上可以显示的项数量（页面大小）。例如，如果屏幕一次可以显示 10 个项，且 ListView 的 `pagesToLoad` 属性设置为 5，那么 ListView 每次将加载 70 个项（额外的 20 个用于上一页和下一页）。

## 总结

本章主要介绍了 ListView 控件。你学习了如何利用此控件以列表或网格的形式显示项目集合。

首先，我解释了该控件的基本功能。你学习了如何在 ListView 中选择、排序、过滤和分组项目。我还讨论了控件的若干高级功能，包括如何动态切换 ListView 项目模板以及如何增量加载 ListView 项目。

在下一章中，我将向你展示如何配合不同类型的自定义数据源使用 ListView，包括 IndexedDB 数据源和 Web 服务数据源。

# 第 8 章

# 创建自定义数据源

## 本章内容

-   创建自定义数据源
-   创建文件数据源
-   创建 Web 服务数据源
-   创建 Indexed 数据源

WinJS 库包含了两个可以作为数据源的对象：`List` 和 `StorageDataSource` 对象。如果你需要对其他类型的数据使用 ListView 或 FlipView，那么你需要编写自定义数据源。

本章的目标是解释你如何编写自定义数据源。在本章中，我解释了如何创建三种自定义数据源：

-   FileDataSource—文件数据源在本地文件系统上存储数据。
-   WebServiceDataSource—Web 数据源允许你使用远程 Web 服务来检索和存储数据。
-   IndexedDBDataSource—IndexedDB 数据源允许你使用 IndexedDB 数据库检索和存储数据。

这些数据源的完整源代码包含本书的 GitHub 项目（https://github.com/StephenWalther/Windows8AppsUnleased）。

# 创建自定义数据源

让我先为你概述一下如何创建自定义数据源。在本节中，我将解释如何实现使用 JavaScript 数组存储数据的自定义数据源的方法。我将详细介绍该数据源的构造函数以及它最重要的方法。在本节讨论完这个（过于简单的）数据源后，我们将在后续章节中深入构建更实用的数据源，例如 Web 服务数据源和 IndexedDB 数据源。





## 创建数据源类

创建自定义数据源的最简单方法是从基类 `VirtualizedDataSource` 派生新类。例如，你可以使用以下代码创建一个名为 `MyDataSources` 的新数据源：

```javascript
var MyDataSources = WinJS.Class.derive(
  WinJS.UI.VirtualizedDataSource,
  // 构造函数
  function () {
    this._adapter = new MyDataAdapter();
    this._baseDataSourceConstructor(this._adapter);
  }
);
```

在上面的代码中，向 `WinJS.Class.derive()` 方法传递了两个参数来创建新的 `DataSource` 类：基类（WinJS.UI.VirtualizedDataSource）和新类的构造函数。

在你派生的 `VirtualizedDataSource` 类的构造函数中，你使用数据适配器调用 `_baseDataSourceConstructor()` 方法。构建自定义数据源的大部分工作都在创建这个数据适配器类中。

# 创建数据适配器

你通过实现 `IListDataAdapter` 接口来创建数据适配器。该接口包含以下方法：

- change()
- getCount()
- insertAfter()
- insertAtEnd()
- insertAtStart()
- insertBefore()
- itemsFromDescription()
- itemsFromEnd()
- itemsFromIndex()
- itemsFromKey()
- itemsFromStart()
- itemSignature()
- moveAfter()
- moveBefore()
- moveToEnd()
- moveToStart()
- remove()
- setNotificationHandler()

该接口还包含以下属性：

- compareByIdentity

幸运的是，你不需要实际上实现所有这些方法和属性。你只需要实现你需要的方法。

例如，如果你想创建一个简单的、只读的数据源，那么你只需要实现 `getCount()` 和 `itemsFromIndex()` 方法。如果你想创建一个更复杂的、读写的数据源，那么你需要实现 `change()`、`insertAtEnd()` 和 `remove()` 方法。

在接下来的章节中，我将描述如何实现其中几个方法，例如 `getCount()` 和 `itemsFromIndex()` 方法。

## 实现 getCount() 方法

`getCount()` 应该返回数据源所代表的记录总数。例如，如果你将项目存储在 JavaScript 中，那么 `getCount()` 方法应该返回数组的长度：

```javascript
getCount: function () {
  return WinJS.Promise.wrap(this._arrayData.length);
}
```

`getCount()` 必须返回一个 `Promise`。因此，你需要使用 `WinJS.Promise.wrap()` 将值封装在 Promise 中，或者你需要创建一个新的 `Promise` 对象。

## 实现 itemsFromIndex() 方法

`itemsFromIndex()` 方法从数据源返回一组项目。该方法接收三个参数：

- requestIndex: 从数据源中要检索的第一个项目的索引。
- countBefore: 在请求索引之前，从数据源中检索的项目数量。
- countAfter: 在请求索引之后，从数据源中检索的项目数量。

`countBefore` 和 `countAfter` 参数旨在被解释为提示。如果你愿意，可以返回多于 `countBefore` 或 `countAfter` 数量的项目。

这里是 `itemsFromIndex()` 方法的一个简单实现。该方法返回 JavaScript 数组的一部分。

```javascript
function itemsFromIndex(requestIndex, countBefore, countAfter) {
  var startIndex = Math.max(0, requestIndex - countBefore);
  var subItems = this._arrayData.slice(startIndex);
  return WinJS.Promise.wrap({
    items: subItems,
    offset: requestIndex - startIndex,
    totalCount: this._arrayData.length
  });
}
```

`itemsFromIndex()` 方法应该返回一个实现 `IFetchResult` 接口的对象。在上面的代码中，返回了 `IFetchResult` 的三个属性：`items`、`offset` 和 `totalCount`。

`items` 代表 `itemsFromIndex()` 方法返回的项目数组。`items` 数组中的每个项目都必须实现 `IListItem` 接口。至少，每个项目必须有一个 `key` 和一个 `data` 属性。

`offset` 属性代表数组中对应于 `requestIndex` 的项目的位置。如果你返回了请求索引之前的项目，那么 `offset` 将大于 0。

最后，`totalCount` 属性返回数据源所代表的项目总数，而不仅仅是正在返回的项目数量。

`itemsFromIndex` 返回的 `items` 数组中的每个项目必须实现 `IListItem` 接口。以下是 `itemsFromIndex()` 方法返回的数据示例：

```json
{
  items: [
    {key: "1", data: {name: "wake up"}},
    {key: "3", data: {name: "get out of bed"}},
    {key: "4", data: {name: "drag the comb across my head"}}
  ],
  offset: 0,
  totalCount: 30
}
```

除了 `items` 外，你还可以实现 `itemsFromDescription()`、`itemsFromEnd()`、`itemsForKey()` 或 `itemsFromStart()` 方法。

## 实现 insertAtEnd() 方法

如果你想支持创建项目，你需要实现 `insertAtEnd()` 方法。该方法接收两个参数：键和实际项目。

以下示例演示了如何使用 `insertAtEnd()` 方法向数组添加新项目：

```javascript
insertAtEnd: function (key, data) {
  var newItem = {
    key: (++this._max).toString(),
    data: data
  };
  this._arrayData.push(newItem);
  return WinJS.Promise.wrap(newItem);
}
```

通常，你不需要提供键，而是让数据源为你生成键。注意 `insertAtEnd()` 方法返回新项目。

> 警告
> 数据源的键必须是字符串。

## 实现 remove() 方法

如果你需要从数据源中删除项目，你需要实现 `remove()` 方法。该方法接收要删除项目的键。如果项目被删除，则方法返回空。以下是移除数组项目的示例代码：

```javascript
remove: function (key) {
  var i = this._getIndexFromKey(key);
  this._arrayData.splice(i, 1);
  return WinJS.Promise.wrap(null);
}
```

```javascript
_getIndexFromKey: function (key) {
  for (var i = 0; i < this._arrayData.length; i++) {
    if (this._arrayData[i].key == key) {
      return i;
    }
  }
}
```

## 实现 change() 方法

如果你需要编辑项目，你需要实现 `change()` 方法。该方法接收三个参数：被编辑项目的键、项目的新值以及项目的索引。

以下是实现 `change()` 方法的示例代码：

```javascript
change: function (key, data, indexHint) {
  var newItem = {
    key: key,
    data: data
  };
  var i = this._getIndexFromKey(key);
  this._arrayData[i] = data;
  return WinJS.Promise.wrap(null);
},
_getIndexFromKey: function (key) {
  for (var i = 0; i < this._arrayData.length; i++) {
    if (this._arrayData[i].key == key) {
      return i;
    }
  }
}
```

注意 `change()` 方法返回一个空 Promise。该方法仅完成而不返回任何特殊内容。

## 错误处理

如果在插入、删除或更改项目时发生错误，你可以返回一个 `EditObject`。你可以返回以下值之一：

- WinJS.UI.EditError.canceled——当编辑操作由于任何原因被取消时，返回此错误。
- WinJS.UI.EditError.noResponse——当编辑操作超时时，返回此错误。
- WinJS.UI.EditError.notPermitted——向只读数据源写入时，返回此错误。
- WinJS.UI.EditError.noLongerMeaningful——当项目已经发生变化时，返回此错误。




例如，在创建一个只读数据源时，你可以这样创建 `insertAtEnd()` 方法：

```
insertAtEnd: function (unused, data) {
  return WinJS.Promise.wrapError(new
  WinJS.ErrorFromName(WinJS.UI.EditError.notPermitted);
}
```

## 实现 setNotificationHandler() 方法

`setNotificationHandler()` 方法允许你在数据源状态发生变化时引发通知。你可以调用以下任何一个方法：

- beginNotifications()
- changed()
- countChanged()
- endNotifications()
- indexChanged()
- inserted()
- invalidateAll()
- itemAvailable()
- moved()
- reload()
- removed()

在使用上述讨论的标准数据适配器方法（如 `insertAtEnd()`、`remove()` 和 `change()` 方法）时，你不需要引发这些通知。然而，当你向数据源添加自定义方法时，你就需要引发这些通知。

例如，假设你想向数据源添加一个 `nuke()` 方法。当你调用 `nuke()` 方法时，所有的数据都将从你的数据源中被移除。

以下是如何在数据适配器类中实现 `nuke()` 方法：

```
setNotificationHandler: function (notificationHandler) {
  this._notificationHandler = notificationHandler;
},

nuke: function () {
  this._arrayData = [];
  this._notificationHandler.reload();
}
```

在上面的代码中，`setNotificationHandler()` 方法将预定义的 `notificationHandler` 方法赋值给名为 `_notificationHandler` 的变量。这使得预定义的 `notificationHandler` 方法对数据适配器中的所有方法可用。

`nuke()` 方法是我们的自定义方法，它将数据源数组设置为空数组并调用 `notificationHandler.reload()` 方法。如果你不调用 `reload()`，那么绑定到数据源的 `ListView` 将不会清除其项。

以下是你如何从数据源暴露自定义的 `nuke()` 方法：

```
var MyDataSource = WinJS.Class.derive(
  WinJS.UI.VirtualizedDataSource,
  // 构造函数
  function(fileName) {
    this._adapter = new MyDataAdapter();
    this._baseDataSourceConstructor(this._adapter);
  },
  // 实例方法
  {
    nuke: function () {
      this._adapter.nuke();
    }
  }
);
```

上述代码中的 `MyDataSource` 类包含一个 `nuke()` 方法。该 `nuke()` 方法简单地委托给了数据适配器的 `nuke()` 方法。

# 创建文件数据源

在本节中，我将讨论如何创建一个自定义的文件数据源。文件数据源从文件系统中存储和检索数据。

> 注意
> `FileDataSource` 的完整源代码包含在 GitHub 源代码中名为 `file` 的文件夹中。

`FileDataSource` 包含了 `getCount()`、`itemsFromIndex()`、`insertAtEnd()`、`remove()` 和 `change()` 方法的实现。

当你调用 `getCount()` 或 `itemsFromIndex()` 方法时，`FileDataSource` 会从文件系统加载数据并调用 `JSON.parse()` 将数据解析为 JavaScript 数组。`FileDataSource` 在其 `_ensureData()` 方法中加载数据：

```
_ensureData: function () {
  var that = this;

  // 尝试返回缓存数据
  if (this._cachedData) {
    return WinJS.Promise.wrap(that._cachedData);
  }

  // 否则从文件加载
  return new WinJS.Promise(function (complete, error) {
    var local = WinJS.Application.local;
    var def = {"MaxKey":-1,"items":[]};
    local.readText(that._fileName, def).done(function(fileContents) {
      this._cachedData = JSON.parse(fileContents);
      complete(that._cachedData);
    });
  });
}
```

`readText()` 方法从文件系统读取文件。如果文件文本不存在，则 `readText()` 方法将返回值 `def`。在何种情况下，读取文件文本的结果都会通过 `JSON.parse()` 方法帮助转换为 JavaScript 数组。

当你调用 `insertAtEnd()`、`remove()` 或 `change()` 方法时，`FileDataSource` 会调用 `JSON.stringify()` 将数据转换为字符串。`FileDatasource` 将数据保存到文件系统。`FileDataSource` 在其 `_saveData()` 方法中保存数据：

```
_saveData: function (data) {
  this._cachedData = data;
  var local = WinJS.Application.local;
  var str = JSON.stringify(data);
  return local.writeText(this._fileName, str);
}
```

`_saveData()` 方法通过调用 `JSON.stringify()` 将 JavaScript 数组转换为字符串。接下来，通过调用 `writeText()` 将字符串保存到文件系统。

# 使用文件数据源

假设你想使用文件数据源创建一个简单的任务列表应用。你希望能够显示现有任务的列表并创建新任务（见图 8.1）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_245_0.png)

图 8.1 使用文件数据源创建的任务列表

你还希望能够通过右键点击/滑动任务并点击“删除”按钮来删除单个任务（见图 8.2），或者通过“Nuke”按钮删除所有任务。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_245_1.png)

图 8.2 使用文件数据源删除任务

任务列表应用的用户界面包含在列表 8.1 的 HTML 页面中。该 HTML 页面包含一个 `ListView` 控件，用于显示任务列表。

# 列表 8.1 文件数据源 (file\file.html)

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>List Data Source</title>
  <!-- WinJS references -->
  <link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="//Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="//Microsoft.WinJS.1.0/js/ui.js"></script>
  <!-- DataSources -->
  <link href="file.cs" rel="stylesheet" />
  <script type="text/javascript" src="fileDataSource.js"></script>
  <script src="file.js"></script>
</head>
<body>
  <div id="lvTasks">
    <div id="tmplTask" x:template="WinJS.Template">
      <div class="taskItem">
        <span data-bind="innerText:name"></span>
      </div>
    </div>
  </div>
  <form id="frmAdd">
    <fieldset>
      <legend>Add Task</legend>
      <input id="inputTaskName" />
      <button id="btnAdd">Add</button>
    </fieldset>
  </form>
  <button id="btnNuke">Nuke</button>
  <button id="btnDelete">Delete</button>
</body>
</html>
```

与 HTML 页面关联的 JavaScript 文件包含在列表 8.2 中。该 JavaScript 代码包含了将 `ListView` 控件绑定到 `FileDataSource` 的代码。

# 列表 8.2 文件数据源 (file.js)

```
 <reference path="Microsoft.WinJS.1.0/js/base.js" />
/// <reference path="Microsoft.WinJS.1.0/js/ui.js" />
function init() {

  WinJS.UI.processAll().done(function () {
    var lvTasks = document.getElementById("lvTasks").winControl;

    // 创建数据源并绑定到 ListView
    var tasksDataSource = new DataSources.FileDataSource("tasks.json");
    lvTasks.itemDataSource = tasksDataSource;


    // 为接 frmAdd、Delete 和 Note 按钮
    document.getElementById("frmAdd").addEventListener("submit", function (evt) {
      evt.preventDefault();
      tasksDataSource.beginEdits();
      tasksDataSource.insertAtEnd(null, {
        name: document.getElementById("inputTaskName").value
      }).done(function (newItem) {
        tasksDataSource.endEdits();
        document.getElementById("inputTaskName").reset();
        lvTasks.ensureVisible(newItem.index);
      });
    });

    document.getElementById("btnDelete").addEventListener("click", function () {
      if (lvTasks.selection.count() == 1) {
        lvTasks.selection.getItems(0).done(function (items) {
          tasksDataSource.beginEdits();
          tasksDataSource.remove(items[0].key).done(function () {
            tasksDataSource.endEdits();
          });
        });
      }
    });
  });
}
```




# 创建文件数据源 235

```javascript
document.getElementById("btnEdit").addEventListener("click", function () {
  if (lvTasks.selection.count == 1) {
    lvTasks.selection.getItems().done(function (items) {
      tasksDataSource.beginEdits();
      tasksDataSource.change(items[0].key, { name: "Changed!"});
    }).done(function () {
      tasksDataSource.endEdits();
    });
  }
});

document.getElementById("btnNuke").addEventListener("click", function () {
  tasksDataSource.nuke();
});

document.addEventListener("DOMContentLoaded", init);
```

通过以下代码行创建文件数据源并将其绑定到 ListView：

```
var tasksDataSource = new DataSources.FileDataSource("tasks.json");
lTasks.itemDataSource = tasksDataSource;
```

要创建的文件名被传递给 FileDataSource 的构造函数。在上面的代码中，使用了一个名为 `tasks.json` 的文件来存储任务列表。

通过以下代码可以创建新任务：

```javascript
document.getElementById("frmAdd").addEventListener("submit", function (evt) {
  evt.preventDefault();
  tasksDataSource.beginEdits();
  tasksDataSource.insertAt(null, {
    name: document.getElementById("inputTaskName").value
  }).done(function (newItem) {
    tasksDataSource.endEdits();
    document.getElementById("frmAdd").reset();
    lvTasks.ensureVisible(newItem.index);
  });
});
```

当你提交添加新任务的 HTML 表单时，会调用文件数据源的 `insertAtEnd()` 方法来创建新任务。如果新任务创建成功，则调用 ListView 控件的 `ensureVisible()` 方法确保新任务滚动到视图中。

> 警告
> 在使用数据源插入、编辑或删除数据时，务必调用 `beginEdits()` 和 `endEdits()`。如果你忽略使用 `beginEdits()` 和 `endEdits()`，在编辑项目过快时可能会遇到空引用异常。

## 创建 Web 服务数据源

在本节中我将讨论如何构建 Web 服务数据源。Web 服务数据源允许你构建一个列表控件来管理远程 Web 服务。你可以使用数据源来检索和修改数据。

你可以使用 Web 服务数据源，例如从存储在远程网站数据库中的产品目录中检索产品列表。这样，当目录产品更新时，你的 Windows Store 应用将显示最新产品。

> 注意
> 在使用 Ajax 时，我强烈建议你利用免费的 Fiddler2 工具来帮助调试 Ajax 请求。你可以从 http://fiddler2.com 下载 Fiddler2——它支持 Windows 8。

> 注意
> WebDataSource 的完整源代码包含在 GitHub 源码中名为 WebService 的文件夹内。

# 创建数据源

Web 服务数据源使用 `WinJS.xhr()` 方法向远程 Web 服务发起 Ajax 调用。例如，`getCount()` 方法如下所示：

```javascript
getCount: function () {
  var that = this;

  return new WinJS.Promise(function (complete, error) {
    var options = {
      url: that._url + "/getCount"
    };
    return WinJS.xhr(options).then(function (xhr) {
      var count = JSON.parse(xhr.response);
      complete(count);
    }, function (xhr) {
      console.log("Could not call getCount()");
    });
  });
}
```

`getCount()` 方法通过执行 HTTP GET 请求调用名为 `getCount()` 的远程 Web 服务操作。

`remove()` 方法通过执行 HTTP DELETE 请求调用名为 `remove()` 的远程 Web 服务操作。`remove()` 方法如下所示：

```javascript
remove: function (key) {
    var that = this;
    return new WinJS.Promise(function (complete, error) {
        var options = {
            url: that._url + "/remove/" + key,
            type: "DELETE",
            headers: {
                authenticationToken: that.authenticationToken
            }
        };
        WinJS.xhr(options).then(
            function (xhr) {
                complete();
            }, function (xhr) {
                console.log("Could not call remove()");
            }
        );
    });
}
```

通常情况下，Web 服务数据源的每个方法都会委托给具有相同命名的远程 Web 服务操作。

# 创建 Web 服务

创建 Web 服务有多种方法。即使你限制在 Microsoft 技术范围内，你也有多种选择。你可以创建 WCF 服务、WCF 数据服务、ASMX Web 服务、Windows Azure Mobile Services 服务或 ASP.NET Web API 服务。

我决定利用 ASP.Net Web API 来创建一个 Web 服务。你可以向 ASP.NET Web Forms 或 ASP.NET MVC 项目添加 Web API 控制器。我决定创建一个一个 ASP.NET MVC 4 项目。在创建 ASP.NET MVC 4 项目时，我选择了 Web API 项目模板（见图 8.3）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_251_0.png)

图 8.3 使用 Web API 项目模板创建 ASP.NET MVC 4 项目

为了利用 ASP.Net Web API 服务，你需要在 `App_Start\RouteConfig.cs` 文件中添加正确的路由。这些路由将传入的浏览器请求映射到正确的 API 控制器（controller）和 API 操作（action）。

我在 `App_Start\RouteConfig.cs` 文件中添加了以下路由：

```csharp
routes.MapHttpRoute(
    name: "TasksGetCount",
    routeTemplate: "api/tasks/getCount",
    defaults: new { controller="tasks", action="getCount" }
);
```

```csharp
routes.MapHttpRoute(
    name: "TasksItemsFromIndex",
    routeTemplate: "api/tasks/itemsFromIndex",
    defaults: new { controller = "tasks", action = "itemsFromIndex" }
);
```

```csharp
routes.MapHttpRoute(
    name: "TasksInsertAtEnd",
    routeTemplate: "api/tasks/insertAtEnd",
    defaults: new { controller = "tasks", action = "insertAtEnd" }
);
```

```csharp
routes.MapHttpRoute(
  name: "TasksRemove",
  routeTemplate: "api/tasks/remove/{key}",
  defaults: new { controller = "tasks", action = "remove" }
);
```

```csharp
routes.MapHttpRoute(
  name: "TasksNuke",
  routeTemplate: "api/tasks/nuke",
  defaults: new { controller = "tasks", action = "nuke" }
);
```

例如，你对 `/api/tasks/getcount` 发起 HTTP GET 请求，然后就会调用 TasksController.GetCount() Web API 控制器。

该 Web API 控制器名为 `TasksController`。它包含了 `GetCount()`、`ItemsFromIndex()`、`InsertAtEnd()`、`Remove()` 和 `Nuke()` 控制操作。控制器使用 Microsoft Entity Framework 与任务数据库表进行交互。

以下是 `GetCount()` 控制操作的形式：

```csharp
[HttpGet]
public int GetCount() {
  return _db.Tasks.Count();
};
```

`getCount()` 方法返回存储在 Tasks 数据库中的任务总数。注意 `getCount()` 方法装饰了 `[HttpGet]` 特性。该特性允许你通过执行 Ajax GET 请求来调用 `getCount()` 方法。

`Remove()` 控制操作如下：

```csharp
[HttpDelete]
public bool Remove(string key)
{
  var id = int.Parse(key);
  _db.Tasks.Remove(_db.Tasks.Find(id));
  _db.SaveChanges();
  return true;
}
```

`Remove()` 控制操作接受一个代表要删除项目的 `key` 参数。该键必须是字符串，因为 WinJS ListView 数据源要求键为字符串。

注意 `remove()` 方法装饰了 `[HttpDelete]` 特性。`remove()` 操作只能通过 HTTP DELETE 请求调用。

在使用非标准 HTTP 方法（如 HTTP DELETE 或 HTTP PUT）时有一个特殊情况。你还需要在 ASP.NET MVC 程序的根 `Web.config` 中添加以下节：

```xml
<system.webServer>
  <modules runAllManagedModulesForAllRequests="true">
  </modules>
</system.webServer>
```

如果你不在 Web.config 文件中添加上述节，所有的 DELETE 请求将返回 404 状态码。

## 使用 Web 服务数据源

在创建并配置远程 Web 服务之后，使用 Web 服务数据源非常简单。以下代码演示了如何创建一个 Web 服务数据源并将其绑定到名为 `lvTasks` 的 ListView 控件：

```javascript
var lvTasks = document.getElementById("lvTasks").winControl;
var tasksDataSource = new 
  DataSources.WebServiceDataSource("http://localhost:51807/api/tasks", "id");
lvTasks.item = tasksDataSource;
```

创建 Web 服务数据源时，你必须向构造函数提供两个参数：Web 服务的 URL 和要检索的数据的主键属性名称。

URL `http://localhost:51807/api/tasks` 是使用端口 51807 的本地 Web 服务地址。该端口是随机生成的。你可以通过打开项目属性框并选择“Web”选项卡来确定使用的端口号（见图 8.4）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_253_0.png)

图 8.4 确定 Visual Studio 项目使用的端口号





## 创建 IndexedDB 数据源

> 注意
> 如果您想避免使用 ASP.NET Web API 构建自定义 Web 服务，那么一个极好的替代方案是利用 Windows Azure Mobile Services。Windows Azure Mobile Services 允许您轻松地在 Windows Azure 云中存储和检索数据。更多信息请访问 https://www.windowsazure.com/en-us/develop/mobile/。

## 创建 IndexedDB 数据源

IndexedDatabase API (IndexedDB) 是 W3C 推荐的一项标准，用于在浏览器中暴露数据库。IndexedDB 推荐标准受到 Firefox 12、Chrome 19 和 IE 10 的支持。当然，Windows Store 应用也支持 IndexedDB 推荐标准。

在后台，不同的浏览器在 IndexedDB API 之后使用不同的数据库。例如，Firefox 使用 SQLite，而 IE 使用 SQLCE。IndexedDB API 提供了一种种跨浏览器、跨平台与这些数据库进行交互的标准方法。

如果您需要在 Windows Store 应用程序中存储大量数据，并查询这些数据的子集，那么 IndexedDB 是一个很好的选择。因为 IndexedDB 支持索引和游标，您可以高效地处理大型数据集。

在本节中，我将讨论如何创建一个 IndexedDB 数据源。我将讨论如何构建一个简单的应用程序，允许您按类别过滤电影列表（见 8.5）。

| 类别 | 全部 |
|---|---|
| Id: 1 | |
| 标题: 音乐 | |
| 类别: 科幻 | |
| Id: 2 | |
| 标题: 任务计划 | |
| 类别: 科幻 | |

图 8.5 使用 IndexedDB 数据源

## IndexedDB 概述

IndexedDB 数据库可能与通常使用的数据库类型不同。IndexedDB 数据库是一个面向对象的数据库，而不是关系型数据库。它不是将数据存储在表中，而是存储在对象存储（object stores）中。IndexedDB 数据库包含一个或多个对象存储，每个对象存储包含一组 JavaScript 对象。

# 第 8 章 创建数据源

IndexedDB API 包含异步和同步方法。目前，只有异步方法被浏览器广泛支持。如果您需要打开数据库连接、向对象存储添加对象或获取对象存储中的项目计数，那么您需要异步执行这些操作。

## 创建或连接到 IndexedDB 数据库

您不需要预先创建一个新的 IndexedDB 数据库——相反，当新用户首次连接到您的数据库时，您才创建一个新数据库。在尝试连接到 IndexedDB 数据库时，通过处理 `upgradeneeded` 事件来创建新的 IndexedDB 数据库。

例如，以下是当名为 TasksDB 的现有数据库不存在时，您如何打开该它的连接：

```javascript
var reqOpen = window.indexedDB.open("TasksDB", 2);
reqOpen.upgradeneeded = function (evt) {
  var db = evt.target.result;
  db.createObjectStore("Tasks", { keyPath: "id", autoIncrement: true });
}
reqOpen.onsuccess = function () {
  var db = reqOpen.result;
  // 对 db 进行某些操作
}
```

当您调用 `window.indexedDB.open()` 且数据库不存在时，会触发 `upgradeneeded` 事件。在上面的代码中，`upgradeneeded` 处理器创建了一个名为 tasks 的新对象存储。该新对象存储具有自动递增列 id，该列作为主键列。

如果数据库已以正确的版本存在，且您调用了 `window.indexedDB.open()`，则会触发成功事件。此时，您已有了指向现有数据库的打开连接，可以开始对数据库进行一些实用的操作。

## 向对象存储添加对象

您使用异步方法与 IndexedDB 数据库交互。例如，下面的代码说明了您如何向 tasks 对象存储中添加新对象：

```javascript
var transaction = db.transaction("tasks", "readwrite");
var store = transaction.objectStore("tasks");
var reqAdd = store.add({
  name: "Feed the dog"
});
reqAdd.onsuccess = function () {
  // 任务添加成功
}
```

## 创建 IndexedDB 数据源

上面的代码创建了一个新的读写数据库事务，向 tasks 对象存储中添加了一个新任务，并处理了成功事件。如果新任务成功添加，则会触发成功事件。

## 获取对象存储中的对象计数

您可以利用 `count()` 方法获取特定对象存储中对象的计数。例如，您可以使用以下代码来确定 tasks 对象存储中的项目数量：

```javascript
var transaction = db.transaction("tasks");
var store = transaction.objectStore("tasks");
var reqCount = store.count();
reqCount.onsuccess = function (evt) {
  var count = evt.target.result;
  console.log(count);
};
```

上面的代码创建了一个新的只读数据库事务，并通过调用 `count()` 方法获取 tasks 对象存储中对象的计数。

注意，对 `count()` 方法的调用是异步的。您通过处理成功事件并读取 `target.result` 属性来计数。

## 从对象存储中检索对象

您通过打开游标并逐个移动游标来从对象存储中检索对象。例如，下面的代码打开了一个从 tasks 对象存储中检索对象的游标：

```javascript
var items = [];
var transaction = db.transaction("tasks");
var store = transaction.objectStore("tasks");
var req = store.openCursor();
req.onsuccess = function (evt) {
  var cursor = evt.target.result;
  if (cursor) {
    items.push(cursor.value);
    cursor.continue();
  } else {
    // 结束
  }
};
```

上面的代码打开了一个游标，它从 tasks 对象存储中检索对象。

在 IndexedDB 中，游标允许用于遍历对象存储。通过移动游标，您可以一个一个地处理对象。例如，如代码所示所示所示：

```javascript
var items = [];
var transaction = db.transaction("tasks");
var store = transaction.objectStore("tasks");
var req = store.openCursor();
req.onsuccess = function (evt) {
  var cursor = evt.target.result;
  if (cursor) {
    items.push(cursor.value);
    cursor.continue();
  } else {
    // 结束
  }
};
```


```js
// 创建 IndexedDB 数据源
var moviesDataSource = new DataSources.IndexedDBDataSource("movies", createOptions);
```

在上述代码中，`createOptions` 代表 IndexedDB 数据库、对象存储和索引的属性。如果数据库不存在，IndexedDB 数据源将创建该数据库。

以下是 `createOption` 对象的属性：

- * databaseName—IndexedDB 数据库的名称
- * databaseVersion—IndexedDB 数据库的版本
- * indexNames—为此数组中的每个属性名称创建一个索引。

当你创建一个 IndexedDB 数据源的实例时，你还可以选择提供一个 `cursorOptions` 对象。该 `cursorOptions` 对象用于过滤对象存储。以下是 `cursorOptions` 对象的属性：

- * indexName—使用此索引创建一个键范围（key range）。
- * only—创建一个键范围并仅返回匹配此值的对象。
- * lowerBound—创建一个键范围，并仅返回值大于此下界的对象。
- * upperBound—创建一个键范围，并仅返回值小于此上界的对象。

例如，以下是你可以如何过滤任务以便返回 1999 年之前创建的任务：

```js
JS.UI.processAll().done(function () {
  var lvTasks = document.getElementById("lvTasks").winControl;

  var createOptions = {
    indexNames: ["dateCreated"],
    databaseVersion: 3
  };

  var cursorOptions = {
    indexName: "dateCreated",
    upperBound: new Date("1/1/1999")
  };

  var tasksDataSource = new DataSources.IndexedDbDataSource("tasks",
    createOptions, cursorOptions);
  lvTasks.itemDataSource = tasksDataSource;

});
```

## 创建 IndexedDB 数据源

在上述代码中，`createOptions` 对象导致任务存储（tasks store）在创建时在其 `dateCreated` 属性上带有一个索引。`cursorOptions` 对象使用索引仅返回那些 `dateCreated` 低于 `upperBound` 1/1/1999 的任务。

我想向你展示一个使用 IndexedDB 数据源的更完整的示例。列表 8.3 和列表 8.4 包含的电影应用（Movie app）允许你选择不同的电影类别，并仅显示所选类别中的电影。该应用还允许你创建新电影和删除电影（见图 8.6）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_260_0.png)

图 8.6 使用 IndexedDB 数据源

# 列表 8.3 使用 IndexedDB 数据源创建电影应用 (indexedDb\indexedDb.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>DataSources</title>

  <!-- WinJS references --
  <link href="//Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="//Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="//Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- DataSources references --
  <link href="//indexedDb.css" rel="stylesheet" />
```

```html
<script type="text/javascript" src="indexedDbDataSource.js"></script>
<script src="indexedDB.js"></script>
</head>
<body>
```

```html
<div id="tmplMovie" data-win-control="WinJS.Binding.Template">
  <div class="movieItem">
    Id: <span data-win-bind="innerText:id"></span>
    <br /><br />
    Title: <span data-win-bind="innerText:title"></span>
    <br /><br />
    Category: <span data-win-bind="innerText:category"></span>
  </div>
</div>
```

```html
<div>
  <label>Category</label>
  <select id="selectCategory">
    <option>All</option>
    <option>SciFi</option>
    <option>Musical</option>
  </select>
</div>
```

```html
<div id="lvMovies"
data-win-control="WinJS.UI.ListView"
data-win-options="{
  itemTemplate: select('#tmplMovie'),
  selectionMode: 'single'
}"></</div>
```

```html
<form id="frmAdd">
  <fieldset>
    <legend>Add Movie</legend>
    <div>
      <label>Title</label>
      <input id="inputMovieTitle" required />
      <label>Category</label>
      <select id="selectMovieCategory">
        <option>SciFi</option>
        <option>Musical</option>
      </select>
      <button>Add</button>
    </div>
  </fieldset>
```

```html
</fieldset>
</form>
```

```html
<button id="btnNuke">Nuke</button>
<button id="btnDelete">Delete</button>
```

```html
</body>
</html>
```

列表 8.3 中的 HTML 页面包含一个选择列表（select list），允许你选择电影类别（全部、科幻、音乐剧）。当你选择某个特定的电影类别时，只有该类别中的电影显示在 ListView 控件中。

列表 8.4 使用 IndexedDB 数据源创建电影应用 (indexedDB\indexedDB.js)

```js
// <reference path="Microsoft.WinJS.1.0/js/base.js">
// <reference path="Microsoft.WinJS.1.0/js/ui.js">

function init() {

  WinJS.UI.processAll().done(function () {
    var lvMovies = document.getElementById("lvMovies").winControl;

    // 创建数据源选项
    var createOptions = {
      databaseName: "MoviesDB",
      databaseVersion: 1,
      indexNames: ["category"]
    };

    // 创建 IndexedDB 数据源
    var moviesDataSource = new DataSources.IndexedDbDataSource("moviesDB", createOptions);

    // 添加种子数据
    addSeedData().done(function () {

      // 将数据源绑定到 ListView
      lvMovies.itemDataSource = moviesDataSource;
    });
  });
}

function addSeedData() {
  return new WinJS.Promise(function (complete) {
```

```js
moviesDataSource.count().then(function (count) {
  if (count > 0) {
    complete();
  } else {
    var seedData = [
      { title: "Star Wars", category: "SciFi" },
      { title: "Forbidden Planet", category: "SciFi" },
      { title: "Show Boat", category: "Musical" }
    ];

    var promises = [];
    seedData.forEach(function (data) {
      promises.push(moviesDataSource.insertAt(null, data));
    });

    WinJS.Promise.join(promises).done(function () {
      complete();
    });
  }
});

// 绑定 SelectCategory, Add, Delete, Nuke 按钮
document.getElementById("selectCategory").addEventListener("change", function (evt) {
  var category = document.getElementById("selectCategory");
  if (category === "All") {
    moviesDataSource = new DataSources.IndexedDbDataSource("movies", createOptions);
  } else {
    var cursorOptions = {
      indexName: "category",
      only: document.getElementById("selectCategory").value
    };
    moviesDataSource = new DataSources.IndexedDbDataSource("movies", cursorOptions);
  }
  lvMovies.itemDataSource = moviesDataSource;
});

document.getElementById("frmAdd").addEventListener("submit", function (evt) {
  evt.preventDefault();
  moviesDataSource.beginEdits();
  moviesDataSource.insertAt(null, {
    title: document.getElementById("inputMovieTitle").value,
    category: document.getElementById("selectMovieCategory").value
  }).done(function () {
    moviesDataSource.endEdits();
    document.getElementById("frmAdd").reset();
    lvMovies.ensureVisible();
  });
});

document.getElementById("btnDelete").addEventListener("click", function () {
  if (lvMovies.selection.count() == 1) {
    moviesDataSource.beginEdits();
    lvMovies.getItems().done(function (items) {
      moviesDataSource.remove(items[0]);
      moviesDataSource.endEdits();
    });
  }
});

document.getElementById("btnNuke").addEventListener("click", function () {
  moviesDataSource.nuke();
});

});

document.addEventListener("DOMContentLoaded", init);
```

列表 8.4 包含了电影应用的 JavaScript 代码。当你首次打开应用时，不带任何 `cursorOption` 创建 IndexedDB 数据源，源中的所有电影都会显示出来：

```js
// 创建 IndexedDB 数据源
var moviesDataSource = new DataSources.IndexedDbDataSource("movies", createOptions);
```

```js
// 添加种子数据
addSeedData().done(function () {
  // 将数据源绑定到 ListView
  lvMovies.itemDataSource = moviesDataSource;
});
```

注意上述代码还包含了对 `addSeedData()` 方法的调用。该方法向 IndexedDB 数据库添加种子数据，以便在首次运行运行时数据库不是空的。

如果你使用选择列表选择了一个特定的电影类别，将执行以下代码：

```js
document.getElementById("selectCategory").addEventListener("change", function (evt) {
  var category = document.getElementById("selectCategory").value;
  if (category === "All") {
    moviesDataSource = new DataSources.IndexedDbDataSource("movies", createOptions);
  } else {
    var cursorOptions = {
      indexName: "category",
      only: document.getElementById("selectCategory").value
    };
    moviesDataSource = new DataSources.IndexedDbDataSource("movies", cursorOptions);
  }
  lvMovies.itemDataSource = moviesDataSource;
});
```

该代码使用 `cursorOptions` 对象创建一个新的 IndexedDB 数据源，它仅代表电影存储中对象的子集。

## 总结

在本章中，我重点关注了用于 WinJS 库控件的自定义数据源。你学习了如何从基类 `VirtualizedDataSources` 派一个新的数据源。

我讨论了三个自定义数据源。首先，我创建了一个文件数据源，允许你从计算机的文件系统中存储和检索数据。接下来，我创建了一个 Web 服务数据源，允许你与远程 Web 服务交互。最后，我讨论了如何创建一个与 IndexedDB 协作的数据源。




# 第9 章
## 应用事件与状态

本章的目标是解释 Windows Store 应用的事件、生命周期和视图状态。在第一部分，我将解释每当启动 Windows Store 应用时都会触发的标准事件序列。你将学习如何处理加载（loaded）、激活（activated）和准备就绪（ready）事件。

在接下来的部分，我将解释如何处理应用程序的挂起（suspension）、终止（termination）和恢复（resumption）。你将学习如何在会话状态（session state）中存储和检索应用程序的状态，以便你可以保持应用程序始终在运行的错觉。

最后，我将讨论应用视图状态。你将学习如何在贴凑（snapped）、填充（filled）和全屏（full-screen）视图状态之间切换，以及如何使用 CSS 和 JavaScript 中的媒体查询（media queries）检测不同的视图状态。

## 应用事件

每当启动 Windows Store 应用时，都会按照顺序触发以下 WinJS 应用事件：

- * WinJS.Application.loaded——由标准的浏览器 DOMContentLoaded 事件触发，在 HTML 文档加载完成后立即触发。
- * WinJS.Application.activated——当你的应用程序被激活时触发。
- * WinJS.Application.ready——在加载和激活事件后触发。
- * WinJS.Application.unload——由标准的浏览器 beforeunload 事件触发，在页面卸载之前触发。

你还可以处理这些由特定事件触发的其他应用事件：

- - WinJS.Application.error——由应用程序中未处理的错误触发。
- - WinJS.Application.checkpoint——当你的应用程序被挂起时触发。
- - WinJS.Application.settings——当应用程序设置更改时触发。

除非调用 `WinJS.Application.start()`，否则这些事件都不会被触发。事件会被排队，在调用 `WinJS.Application.start()` 方法之前，事件不会触发。

以下 JavaScript 代码说明了如何为这些事件中的每个事件创建一个处理器，以及何时它们记录到 Visual Studio JavaScript 控制台窗口中：

```javascript
WinJS.Application.addEventListener("loaded", function (evt) {
  console.log("loaded");
}
```

```javascript
WinJS.Application.addEventListener("activated", function (evt) {
  console.log("activated");
}
```

```javascript
WinJS.Application.addEventListener("ready", function (evt) {
  console.log("ready");
}
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_267_0.png)

图 9.1 记录 WinJS 应用事件

## 处理 Activated 事件

当 Windows Store 应用被激活（启动）时，会触发 activated 事件。Windows Store 应用可以通过多种方式被激活，你可以使用 `ActivationKind` 属性来确定应用具体是如何被激活的：

```javascript
WinJS.Application.addEventListener("activated", function (evt) {
  var activationKind = Windows.ApplicationModel.Activation.ActivationKind;
  switch (evt.detail.kind) {
    case activationKind.launch:
      console.log("Launched from a tile");
      break;
    case activationKind.search:
      console.log("Activated from a search");
      break;
    default:
      console.log("Activated for some other reason");
  }
});
```

Windows Store 应用激活的最常见方式是用户点击开始屏幕上的应用磁贴。在这种情况下，`ActivationKind` 枚举的值为 `Launch`。

然而，还有其他方式可以激活 Windows Store 应用。例如，应用可以响应于用户从搜索磁贴（Search charm）执行搜索，或者响应于用户从共享磁贴（Share charm）共享某些内容，或者响应于用户从另一个应用程序（如邮件应用）点击文件。在这些情况下，你可以使用 `ActivationKind` 属性来确定应用被激活的具体原因。

## 处理 Error 事件

默认情况下，当 Windows Store 应用中出现未处理的错误（未在 `try...catch` 块中处理的错误）时，会发生以下情况：

1. 通过 `WinJS.log()` 方法记录错误。
2. 当应用在 Visual Studio 调试模式下运行时，会调用 `debugger` 语句以进入调试器器。
3. 通过调用 `MSApp.terminateApp()` 方法终止应用。

在调用 `terminateApp()` 方法后，用户会被抛回 Windows 屏幕（非常生硬，且没有任何解释）。

你可以处理应用程序错误事件以提供更好的用户体验。例如，以下是当发生未处理错误时如何向用户显示消息的方法：

```javascript
WinJS.Application.addEventListener("error", function (evt) {
    var message = new Windows.UI.Popups.MessageDialog(
        "There was an error."
    );
    message.showAsync();
    return true;
});
```

```javascript
WinJS.Application.addEventListener("ready", function ( ) {
    throw new WinJS.ErrorName("MyError", "Yikes! An Error!");
});
```

```javascript
WinJS.Application.start();
```

之前的代码在发生消息为“There was an error.”的错误时显示模型对话框（见图 9.2）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_269_0.png)

图 9.2 显示错误消息

注意错误处理器返回了值 `true`。当错误处理器返回 `true` 时，该错误被视为已处理，应用程序不会终止。如果你想在执行自定义错误处理器代码后终止应用，请不要返回 `true`。

> 警告
> 如果错误发生在调用 `WinJS.application.start()` 方法之前，那么你的自定义错误处理器将不会被调用。

## 使用 Promise 延迟事件

WinJS.Application 事件与普通的 DOM 事件不同，因为它们支持 promise。你可以在 `WinJS.Application` 事件期间执行异步任务，并推迟下一个事件，直到一个 promise 完成。

例如，在创建新的 Windows Store 应用项目时创建的 `default.js` 文件将 `WinJS.Application.activated` 事件的完成推迟，直到对 `WinJS.UI.processAll()` 的异步调用完成。这确保了在启动界面拆除之前，页面上的所有控件都已处理。

以下是 `default.js` 文件中 `WinJS.Application.activated` 事件处理器（删除了部分代码）：

```javascript
app.onactivated = function (args) {
    if (args.detail.kind === activationKind.launch) {
        args.setPromise(WinJS.UI.processAll());
    }
};
```

在上面的代码中，使用 `args.setPromise()` 来执行一个返回 promise 方法：即 `processAll()` 方法。`processAll()` 方法异步执行，在 `processAll()` 方法完成之前，`ready` 事件不会被触发。

## 创建自定义事件

你可以创建并监听自定义应用事件。你可以根据喜意创建任何类型的事件。

例如，如果你正在创建一个游戏，你可能想要创建一个秒触发一次的心跳（heartbeat）事件，以便刷新游戏面板。以下代码演示了如何创建和监听自定义事件：

```javascript
window.setInterval(function () {
  WinJS.Application.queueEvent({ type: "heartbeat" });
}, 1000);
```

```javascript
WinJS.Application.addEventListener("heartbeat", function (evt) {
  console.log("heartbeat");
});
```

```javascript
WinJS.Application.start();
```

上面的代码使用 `setInterval` 方法每秒执行一次代码。调用 `queueEvent` 方法来队列自定义事件。使用 `addEventListener` 方法来监听事件。你可以在队列事件时通过提供 `detail` 属性提供额外的事件详细信息：

```javascript
WinJS.Application.queueEvent({
  type: "heartbeat",
  detail: { numberOfPlayers: 12 }
});
```





## 检测应用何时挂起和终止

你可以通过处理 `WinJS.Application.checkpoint` 事件来检测应用何时被挂起。你应该使用此事件来保存应用的状态，以防应用在挂起后被终止，这样你可以在应用再次启动时重新加载状态。

Windows Store 应用内部没有方法可以检测应用何时被终止。特别是，并没有一个“应用终止（terminated）”事件。因此，如果你需要保存应用状态以便在终止后重新加载，那么你应该在 `checkpoint` 事件期间保存应用状态。

以下是处理此事件的示例代码：

```
WinJS.Application.addEventListener("checkpoint", function () {
  // Save app state
});
```

## 检测之前的执行状态

当 Windows Store 应用被激活时，你可以使用 `previousExecutionState` 属性来确定应用是新启动的、之前是由用户关闭的，还是在挂起和终止后重新返回的。

根据 `previousExecutionState` 的值，你可能想要加载默认值或加载之前的应用状态。例如，如果你正在创建一个新闻应用，你可能想要加载用户之前正在阅读的某篇文章。相反，如果用户从未运行过该应用，你可能想要加载一个默认页面（如首页）。

以下是检查之前的状态的代码：

```
WinJS.Application.addEventListener("activated", function (evt) {
  var appState = Windows.ApplicationModel.Activation.ApplicationExecutionState;
  if (evt.detail.previousExecutionState == appState.Running) {
    // 应用在当前用户会话中尚未运行
    // 或者它崩溃了。
    // 应加载默认值。
  }
  if (evt.detail.previousExecutionState == appState.closedByUser) {
    // 应用是由用户关闭的。
    // 应加载默认值。
  }
  if (evt.detail.previousExecutionState == appState.terminated) {
    // 应用被挂起并终止了。
    // 应该恢复之前的状态。
  }
});
```

## 挂起、终止和恢复应用

代码包含一个 `WinJS.Application.activated` 事件的处理器。`event.previousExecutionState` 属性代表应用程序之前的状态。所有的之前的状态都由 `ApplicationExecutionState` 枚举表示。以下是 `ApplicationExecutionState` 枚举的所有可能值：

- notRunning—用户在从 Windows Store 安装应用后、重启电脑、登录和注销、结束任务、应用崩溃或在 10 秒内关闭并重启应用后激活了应用。
- running—应用已经在运行，用户通过二级磁贴或一个激活协议或扩展激活了它。
- suspended—应用处于挂起状态，用户通过二级磁贴或其中一个激活协议或扩展激活了应用。
- terminated—应用被 Windows 终止了。
- closedByUser—应用由用户关闭且在 10 秒内没有重启。

> 注意：你无法检测应用是否在挂起后被激活。你只能检测应用程序在挂起和**终止**之后被激活的情况。对于只被挂起而未被终止的应用，不会触发 `activated` 事件。

## 使用 Visual Studio 测试应用状态

你可以使用 Visual Studio 测试你的 Windows 应用在挂起、终止或恢复时的行为。当你从 Visual Studio 运行应用时，会出现图 9.3所示所示的菜单（它是调试位置工具栏的一部分）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_272_0.png)

图 9.3 应用状态选项

如果你想模拟应用的挂起和恢复，可以点击 `Suspend` 选项挂起你的应用，然后点击 `Resume` 选项再次恢复应用。当你点击 `Suspend` 选项时，会触发 `checkpoint` 事件。当你点击 `Resume` 选项时，不会触发 `activated` 事件（你的应用不知道自己何时从挂起中恢复的）。

# 第 9 章 应用事件和状态

如果你想模拟应用的挂起和终止，可以点击 `Suspend and shutdown` 按钮。当你点击 `Suspend and shutdown` 按钮时，会触发 `checkpoint` 事件并且你的应用会停止。当你再次运行应用（通过在 Visual Studio 中实际运行应用），`previousExecutionState` 属性的值将为 `terminated`。

# 使用会话存储存储

如果应用被挂起，应用不会丢失状态。然而，如果应用被挂起并终止，任何变量的状态将丢失其值，应用将从头开始。

有一个特殊对象 `WinJS.Application.sessionState`，你可以用它来跨应用挂起存储状态。你添加到会话状态中的任何内容都会一直持续到应用激活为止。

以下代码说明了如何使用会话状态存储用户的当前分数：

```
(function () {
  "use strict";

  var _gameScore;

  WinJS.Application.addEventListener("activated", function (evt) {
    var appState = Windows.ApplicationModel.Activation.ApplicationExecutionState;
    if (evt.detail.previousExecutionState == appState.notRunning ||
        evt.detail.previousExecutionState == appState.closedByUser) {
        // 设置默认游戏分数
        _gameScore = 0;
    }
    if (evt.detail.previousExecutionState == appState.terminated) {
      // 从会话状态加载游戏分数
      _gameScore = WinJS.Application.sessionState.gameScore;
    }
  });

  WinJS.Application.addEventListener("checkpoint", function (evt) {
    // 将游戏分数保存到会话状态
    WinJS.Application.sessionState.gameScore = _gameScore;
  });

  WinJS.Application.addEventListener("ready", function (evt) {
    // 外星人，通过 ID
    document.getElementById("btnKillAlien").addEventListener("click", function () {
      _gameScore++;
    });
  });

  WinJS.Application.start();
}()); 
```

之前的代码包含了三个事件处理器：

- click—当你点击 `btnKillAlien` 按钮时，当前游戏分数加 1。
- checkpoint—当应用被挂起时调用。此事件处理器将当前游戏分数存储在会话状态中。
- activated—当应用被激活时调用。如果应用在终止后被激活，则从会话状态加载当前游戏分数。否则，将为游戏分数分配一个默认值。

会话状态仅在应用终止后被激活时加载。会话状态会被保留，例如当用户显式关闭应用或重启机器时。

> 注意
在后台，会话状态存储在名为 `_sessionState.json` 的本地存储文件文件中。在 `checkpoint` 事件之后，会话状态会自动写入此文件。当应用在终止后被激活时，会话状态会自动从此文件加载。

## 应用视图状态

Windows 应用可以用几种不同的视图状态显示。不同的视图状态决定了你的应用程序可用的水平和垂直空间。

设计良好的 Windows 应用会智能地适应可用空间。例如，如果一个宽屏应用被迫变得狭窄，它会自动隐藏额外内容。

在本节中，你将学习不同的 Windows 应用视图状态，以及你如何利用媒体查询来适应不同的视图状态。

## 并靠、填充、竖屏和横屏

Windows 应用可以处于并靠（snapped）、填充（filled）或全屏状态。这些状态中的每一个都对应不同的水平分辨率。例如，一个 Windows 应用可以靠在屏幕的左边缘或右边缘，而第二个 Windows 应用填充屏幕的剩余部分。第一个应用处于并靠状态，第二个应用处于填充状态。

图 9.4 展示了并靠和填充视图状态之间的区别。在图 9.4 中，Internet Explorer 处于填充状态，而天气应用处于并靠状态。




262 第 9 章 应用事件与状态

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_275_0.png)

## 警告

你只能在水平分辨率为 1366 像素或更高的 Windows 设备上将应用切换到停靠状态（snapped state）。否则，将没有足够的屏幕空间来同时显示一个以上的应用。

使用键盘时，你可以通过 Win + .（句号）键将当前应用从左侧停靠、右侧停靠或全屏视图状态切换。使用触摸屏时，你可以从屏幕左侧缓慢拖动应用。

停靠应用的水平分辨率始终为 320 像素。分栏器（splitter）会占用另外 22 像素。最后，填充状态的应用分辨率为 1024 像素或更高（仅限于你的屏幕分辨率）。见图 9.5。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_276_0.png)

图 9.5 停靠应用的尺寸

当你创建一个 Windows Store 应用时，你的应用可能会以横屏或竖屏模式显示。例如，当我旋转平板电脑时，我期望任何打开的 Windows Store 应用会自动从横屏切换到竖屏（见图 9.6 和图 9.7）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_276_1.png)

图 9.6 横屏

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_277_0.png)

图 9.7 竖屏

良好的 Windows Store 应用样式在全屏、停靠或填充视图状态下都会很好看。它在横屏和竖屏模式下也同样。。

## 使用媒体查询

你可以结合级样式表（CSS）利用媒体查询来自动适应不同的视图状态。你可以使用媒体查询检测设备的特性并修改内容的呈现方式。

> 注意
> 媒体查询是 W3C 的建议标准。你不仅可以在 Windows Store 应用中使用媒体查询，也可以在普通网站中使用。Google Chrome 4+、Mozilla Firefox 3.5+、Apple Safari 4+ 以及 Microsoft Internet Explorer 9+ 均支持媒体查询。

例如，假设你想要根据设备的水平分辨率显示不同的内容。在这种情况下，你可以通过使用 `@media` 规则对样式进行分组。

例如，以下 HTML 页面包含三组样式规则。一组适用于所有设备，一组适用于中分辨率设备，另一组适用于高分辨率设备：

```html
<!DOCTYPE html>
<head>
  <title></title>
  <style type="text/css">
  /* 默认样式 */
  .displayMedium, .displayInHigh {
    display:none;
  }
  /* 大于或等于 1,366px */
  @media (min-width:1366px) {
    .displayInMedium {
      display: block;
    }
  }
  /* 大于或等于 1,920px */
  @media (min-width:1920px) {
    .displayInMedium, .displayInHigh {
      display: block;
    }
  }
  </style>
</head>
<body>
  <div>
    <h1>在所有分辨率下你都能看到我。</h1>
  </div>
  <div class="displayInMedium">
    <h1>在中等分辨率下你可以看到我。</h1>
  </div>
  <div class="displayInHigh">
    <h1>在高分辨率下你才能看到我。</h1>
  </div>
</body>
</html>
```

你可以通过使用 Visual Studio 模拟器运行 Windows Store 应用并选择不同的分辨率来模拟不同的设备。当你切换到不同的分辨率时，不同的 DIV 元素将会显示。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_279_0.png)

图 9.8 在模拟器中更改分辨率

> 警告
> 并非所有电脑都支持模拟器列出的所有分辨率。例如，在我的笔记本电脑上，无法切换到 2560x1440。

Microsoft 为媒体查询了自己的扩展。当你创建一个新的 Windows Store 应用时，得到的 `default.css` 文件包含以下样式规则：

```css
@media screen and (-ms-view-state:fullscreen) { }
@media screen and (-ms-view-state:filled) { }
@media screen and (-ms-view-state:snapped) { }
@media screen and (-ms-view-state:portrait) { }
```

`-ms-view-state` 功能允许你在应用切换全屏（横屏或竖屏）、填充或停靠状态时显示或隐藏不同的内容。

## 使用 JavaScript media 方法

在上一节中，你学习了如何使用级样式表执行媒体查询。你也可以利用 `window.matchMedia()` 方法使用 JavaScript 执行媒体查询。该方法返回一个 `MediaQuery`，表示成功或失败。

例如，以下代码检查当前设备是否处于竖屏模式：

```javascript
if (window.matchMedia("orientation:portrait").matches) {
  console.log("portrait");
} else {
  console.log("landscape");
}
```

如果 `matches` 属性返回 `true`，则设备处于竖屏模式，“portrait”会被写入 Visual Studio 窗口。否则，“landscape”会写入控制台窗口。

你可以创建一个事件监听器，每当媒体查询结果变化时触发代码。例如，当设备从横屏切换到竖屏或从竖屏切换到横屏时，事件监听器都会被触发：

```javascript
window.matchMedia("orientation:portrait").addListener(function (mql) {
  if (mql.matches) {
    console.log("Switched to portrait");
  }
});
```

注意，每当媒体查询结果变化时，事件监听器都会触发。因此，在写入消息之前验证 `matches` 属性是否为 `true`。

## 定义视口 (Viewport)

你可以利用 `@ms-viewport` 规则自动调整内容以适应设备分辨率（不同宽度的设备）。当你希望适应停靠或填充等不同状态时，使用 `@ms-viewport` 规则也是非常有用的。

`@ms-viewport` 规则允许你定义视口。视口决定了用于显示内容的可用空间，独立于屏幕大小。

例如，以下页面显示了一些文字和一张特斯拉：

```html
<!DOCTYPE html>
<head>
  <title>viewport</title>
</head>
<body>
  <h1>一辆红色的特斯拉</h1>
  <img src="../images/tesla.jpg" />
</body>
</html>
```

当页面在全屏状态下显示（见图 9.9）时，一切看起来都良好。但当你切换到停靠状态时，图片会被裁剪（见图 9.10）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_281_0.png)

图 9.9 全屏页面

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_281_1.png)

图 9.10 停靠页面

以下是你可以使用 `@ms-viewport` 规则自动缩放页面：

```html
<!DOCTYPE html>
<head>
  <title>viewport</title>
  <style type="text/css">
    @ms-viewport {
      width: 1024px;
    }
  </style>
</head>
<body>
  <h1>一辆红色的特斯拉</h1>
  <img src="../images/tesla.jpg" />
</body>
</html>
```

在上面的页面中，视口被设置为 1024px x 768px。如果页面以低于 1024px x 768px 的分辨率显示，则页面内容会缩小（见图 9.11）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_282_0.png)

图 9.11 停靠与缩小

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_283_0.png)

图 9.12 全屏与扩展状态

如果你只想在应用停靠时指定视口（缩放页面内容），则可以结合之前描述的 `-ms-view-state` 媒体功能使用 `@ms-viewport` 规则。例如，以下 CSS 规则仅在应用停靠时更改视口宽度：

```css
@media screen and (-ms-view-state:snapped) {
  @ms-viewport {
    width: 1024px;
  }
}
```

> 注意
> `@ms-viewport` 规则是级样式表的 Microsoft 扩展，基于 W3C 即将推出的 `@viewport` 规则。`@viewport` 规则的草案规范是 CSS 设备适配规范的一部分，可以在此处找到：http://dev.w3.org/csswg/css-device-adapt/

## 总结

本章介绍了 Windows Store 应用事件和视图状态。在第一部分，我解释了每当运行 Windows Store 应用时触发的标准事件类型。你学习了如何处理应用程序加载、激活和就绪事件。

接下来，我讨论了 Windows Store 应用在 Windows 8 中如何自动挂起和终止。你学习了如何利用会话状态来存储和检索应用数据。




最后，你已经学习了 Windows Store 应用不同的应用视图状态，例如贴靠（snapped）和填充（filled）视图状态。我演示了如何利用媒体查询（涵盖 CSS 和 JavaScript）来检测不同的应用视图状态并显示不同的内容。

# 第 10 章
页面片段与导航

- 使用 HtmlControl
- 创建 Page Control
- 创建多页应用

本章的目标是解释三个控件：HtmlControl、Page Control 和 ControlNavigator 控件。这三个控件都允许你使用 Ajax 在另一个 HTML 页面中显示一个 HTML 页面的内容。

HtmlControl 允许你向页面添加一段 HTML 块。你可以使用此控件在应用程序的多个处复用相同的 HTML 标记。

创建 Page Control 允许你从 HTML 页面、JavaScript 文件和样式表轻松地创建新的 JS 控件。当你想要在一个新控件中封装标记和行为时，就可以创建一个 Page Control。

最后，ControlNavigator 控件允许你构建包含多个页面的单页应用（SPA）。ControlNavigator 允许你加载 Page Controls 来模拟页面之间导航的体验。

# 使用 HtmlControl 控件

如果你想在 Windows Store 应用的多个页面中包含相同的 HTML 块，或者你想将现有页面拆分为更易管理的部分，那么你可以使用 JS HtmlControl 控件。此控件要求你设置一个选项：URI。你设置 URI 来指定你想要加载的内容。

> 注意
> 本节讨论的代码可以在 GitHub 源码的 Chapter10\Frags 文件夹中找到。

例如，假设你想显示一个包含账单地址和收货地址表单的页面。换句话说，你想显示两次同一个表单（见图 10.1）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_287_0.png)

图 10.1 使用 HtmlControl 显示地址表单

在这种情况下，你可以在名为 addressForm.html 的独立 HTML 文件中创建地址表单：

```html
<div>
  <div class="label">
    <label for="inpStreet">Street:</label>
  </div>
  <div class="field">
    <input class="inpStreet" required />
  </div>
</div>
<div>
  <div class="label">
    <label for="inpCity">City:</label>
  </div>
  <div class="field">
    <input class="inpCity" required />
  </div>
</div>
```

## 注意

注意，我在表单字段中使用了类名而不是 ID，因为我想要避免在表单显示两次时创建冲突的 ID。

接下来，你可以像这样使用 HtmlControl 控件在同一个页面中加载两次此表单：

```html
<Order Form/>
<form id="frmOrder">
<fieldset>
  <legend>Billing Address</legend>
  <div id="divBillingAddress"
    data-win-control="WinJS.UI.HtmlControl"
    data-win-options="
      uri:'address.html'
  </div>
</fieldset>
<fieldset>
  <legend>Shipping Address</legend>
  <div id="divShippingAddress"
    data-win-control="WinJS.UI.HtmlControl"
    data-win-options="
      uri:'address.html'
  </div>
</fieldset>
<input type="submit" value="Submit Order" />
</form>
```

最后，这里是你可以处理表单提交事件的方法，以获取账单地址和收货地址表单的值：

```javascript
WinJS.UI.process.All().done(function() {
  var frmOrder = document.getElementById("frmOrder");

// 获取订单
  frmOrder.addEventListener("submit", function (e) {
    e.preventDefault();
    var order = {
      billing_street: document.querySelector("#divBillingAddress .inpStreet"),
      billing_city: document.querySelector("#divBillingAddress .inpCity"),
      shipping_street: document.querySelector("#divShippingAddress .inpStreet"),
      shipping_city: document.querySelector("#divShippingAddress .inpCity")
    };
    // 保存到数据库
});
```

在上面的代码中，使用了 `querySelector()` 方法来获取账单地址和收货地址表单字段的值。所有字段的值都被赋值赋值了一个名为 `orders` 的对象。

> 警告
> 不要忘记调用 WinJS.UI.processAll()，否则 HtmlControl 将永远不会变成一个控件。

> 注意
> 在 Windows Store 应用中，你不能使用服务器端的 #INCLUDE 指令来包含其他文件的内容。如果你想包含内容，则需要使用 HtmlControl。

## 创建 Page Control

正如其名所示，Page Control 允许你从页面创建一个控件。Page Control 为你提供了一种创建自定义 WinJS 控件的简单方法。当你创建一个 Page Control 时，你实际上 HTML 页面、JavaScript 文件和 CSS 文件创建一个新的 WinJS 控件。

当你需要的不仅仅是简单地向页面添加一段 HTML 块时，创建一个 Page Control 就很有意义。Page Control 允许你在控件中封装外观和行为。

此外，Page Control 有它自己的事件生命周期。例如，Page Control 有自己的 ready 事件，你可以在其中初始化控件。

例如，假设你想创建一个 Alert 控件。当有人点击 Alert 控件渲染的按钮时，会出现一个 WinRT 模态对话框并显示消息（见图 10.2）。我将介绍作为 Page Control 创建 Alert 控件所需的每个步骤。

## 创建 Page Control

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_290_0.png)

图 10.2 使用自定义 Page Control 显示警报

首先，我们需要创建以下三个文件：

- alert.html
- alert.js
- alert.css

你可以通过向项目添加 HTML 页面、JavaScript 文件和样式表来创建这三个文件。

alert.html 页面包含了我们新控件的所有标记：

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>confirmButton</title>
  <link href="alert.css" rel="stylesheet" />
  <script src="alert.js"></script>
</head>
<body>
  <button class="alert">alert</button>
</body>
</html>
```

注意，alert.html 页面看起来像一个普通的 HTML 页面，既有 HEAD 部分也有 BODY 部分。HEAD 部分包含了页面所需的所有样式表和 JavaScript 文件。BODY 部分包含了 Alert 控件所需的所有标记。

## 注意

在 Page Control HTML 文件头 中引用的所有脚本和样式表都会从 HTML 文件中移除，并添加到父页面中。换句话说，所有的脚本和样式都提升到了包含它的页面。

alert.css 文件看起来如下（并不特别有趣）：

```css
alert {
  background-color: red
}
```

该 CSS 文件将 Alert 按钮的背景颜色改为红色。

最后，alert.js 文件看起来如下：

```javascript
// <reference path="WinJS.1.0/js/base.js" />
// <reference path="WinJS.1.0/js/ui.js" />
(function () {
  "use strict";

  var Alert = WinJS.Pages.define("alert.html", {

  ready: function (element, options) {
    var btn = WinJS.Utilities.query("button", element);

    // 设置默认选项
    options.buttonLabel = options.buttonLabel || "Show Alert";
    options.message = options.message || "Alert!";

    // 更新按钮文本
    btn.innerText = options.buttonLabel;

    // 设置点击处理程序
    btn.listen("click", function () {
      var md = new Windows.UI.Popups.MessageDialog(
        options.message
      );
      md.showAsync();
    });
  }
});

WinJS.Namespace.define("MyControls", {
  Alert: Alert
});
})();
```




280 第 10 章 页面片段与导航

注意，上面的页面引用了 alert.js JavaScript 文件。在任何声明式使用该控件的页面中，你必须包含对你自定义页面控件（Page Control）的引用。

Alert 页面控件是在页面的 body 中声明式创建的，就像其他标准 WinJS 控件（如 ListView 或 DatePicker 控件）一样。

> 警告
> 记得调用 WinJS.UI.processAll()，否则你的页面控件将像其他任何 WinJS 控件一样， 无法被处理并转换为控件。

## 创建多页应用

你可以创建一个包含多个 HTML 页面的 Windows Store 应用，并在页面之间建立链接。然而，微软强烈不建议你这样做。相反，他们鼓励你创建一个单页应用（single page app），并动态加载代表单独页面的页面控件。

为什么微软给出这样的建议呢？当你构建 Windows Store 应用时，你并不是在构建网站（尽管你使用了许多相同的技术）。相反，你正在构建一个 Windows 应用程序。

用户对 Windows 应用程序和 Web 应用程序会有不同的预期。在 Web 应用程序中，点击链接并等待（等待、等待、等待）另一个页面加载是正常的。在你等待时，应用程序会冻结。当新页面加载时，你将在全新的上下重新开始——即新页面的上下文。

在 Windows 应用程序中，这种体验是不可接受的。例如，Microsoft Word 在你点击按钮时永远不会冻结（嗯，几乎）。你不会在 Windows 应用程序的页面之间跳转。相反，你通过打开对话框和切换标签来导航内容。

为了在 Windows Store 应用中创建这种 Windows 应用程序体验，鼓励你创建一个单页应用。

## 创建导航应用

创建包含多个页面的单页应用简单的方法是利用 Visual Studio 导航应用项目模板（见图 10.3）。该模板与空白应用（Blank App）模板之间存在差异。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_294_0.png)

图 10.3 创建导航应用

首先，导航应用模板包含一个 pages 文件夹。pages 文件夹包含了代表应用程序中所有页面的页面控件。每个页面控件都包含 pages 文件夹的一个独立的子文件夹中。

导航应用包含一个 pages/home 文件夹，其中包含一个代表主页面的页面控件。当启动导航应用时，该页面控件会被默认加载。

导航应用模板和空白应用模板一样，包含一个 default.html 文件。然而，此文件主要作为从 pages 文件夹加载不同页面控件的外壳。当你从一个页面导航到另一个页面时，default.html 文件 body 中的内容会被新内容加载

最后，导航应用模板包含一个空白应用模板未包含的 WinJS 滚动控件，名为 PageNavigator 控件。该控件位于名为 js/navigator.js 的文件中。PageNavigator 控件处理将页面控件加载到 default.html 页面的所有细节。

让我们深入了解一下这一切是如何运作的。

## 理解导航应用的 default.html 页面

正如我之前提到的，导航应用中的 default.html 页面主要是页面控件中包含内容的空壳。default.html 页面的全部内容包含在列表 10.1 中。

282 第 10 章 页面片段与导航

# 列表 10.1 default.html 页面

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>MultiPage</title>

  <!-- WinJS references -->
  <link href="Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- MultiPage references -->
  <link href="css/default.css" rel="stylesheet" />
  <script src="js/navigator.js"></script>
</head>
<body>
  <div id="content" data-win-control="Application.PageControl">
    <div data-win-options="{home: 'pages/home.html'}"></div>
    <div id="appbar" data-win-control="WinJS.UI.AppBar">
      <button data-win-options="{id: 'cmd', label: 'Command', icon: 'placeholder'}"></button>
    </div>
  </div>
</body>
</html>
```

列表 10.1 中的页面 body 包含两个控件。第一个控件是 PageControl 的宿主。该控件具有 ID content，并从页面控件加载。我将更深入地讨论 PageNavigator。

第二个控件（被注释掉了）是一个 AppBar 控件。你在 default.html 页面放置的任何内容都将显示在应用程序的每个页面。因为 AppBar 在 Windows Store 应用的所有页面中应该是一致的，所以 default.html 页面是声明它的好地方。

> 注意 我在第 6 章“菜单和浮动窗”中讨论过 AppBar 控件。

你添加到 default.html 页面上的任何其他内容也将显示在导航应用的所有页面中。例如，如果你想创建一个标准的页眉、页脚或侧边栏，将这些标准内容添加到 default.html 页面是有意义的。

## 向导航应用中添加新页面控件

一个只包含单个页面控件（主页）的单页应用是不值得费力的。所以让我向你展示如何添加第二个页面。

向你的项目添加新页面控件简单的方法是利用 Visual Studio 页面控件模板。在 pages/anotherPage 创建名为 anotherPage 的新子文件夹。选择项目项，添加新建项，并选择页面控件模板（见图 10.4）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_296_0.png)

图 10.4 使用 Visual Studio 创建新的页面控件

当你向项目添加名为 anotherPage.html 的页面控件时，你会得到以下三个文件：

- anotherPage.html
- anotherPage.js
- anotherPage.css

当然，你可以手动创建这些完全的文件，但使用 Visual Studio 模板可以节省一些时间。

anotherPage.html 的全部内容包含在列表 10.2 中。注意页面的 body 包含一个 HTML5 header 标签（不要与 HEAD 标签混淆）。页面 包含一个按钮， header 标签包含一个标题。

297 第 10 章 页面片段与导航

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_296_0.png)

图 10.5 页面控件的 header

# 列表 10.2 default.html 页面

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>MultiPage</title>

  <!-- WinJS references -->
  <link href="Microsoft.WinJS.1.0/css/ui-dark.css" rel="stylesheet" />
  <script src="Microsoft.WinJS.1.0/js/base.js"></script>
  <script src="Microsoft.WinJS.1.0/js/ui.js"></script>

  <!-- MultiPage references -->
  <link href="css/default.css" rel="stylesheet" />
  <script src="js/navigator.js"></script>
</head>
<body>
  <div id="content" data-win-control="Application.PageControl">
    <div data-win-options="{home: 'pages/home.html'}"></div>
    <div id="appbar" data-win-control="WinJS.UI.AppBar">
      <button data-win-options="{id: 'cmd', label: 'Command', icon: 'placeholder'}"></button>
    </div>
  </div>
</body>
</html>
```

（注：此处原文中列表10.2的内容似乎与10.1重复或逻辑有误，已按原文结构翻译）

anotherPage.html 的全部内容包含在列表 10.2 中。注意页面的 body 包含一个 HTML5 header 标签（不要与 HEAD 标签混淆）。页面 包含一个按钮，header 标签包含一个标题。

为了我们可以知道我们已经导航到 anotherPage，我将把 body 中的“Content goes here”替换为“Hello Page!”，

anotherPage.js 文件的内容包含在列表 10.3 中。

# 列表 10.3 anotherPage.js

```javascript
(function () {
  "use strict";

  WinJS.Pages.define("/pages/anotherPage/anotherPage.html", {
    // 此函数在用户导航到此页面时调用
    // 用数据填充页面元素。
    ready: function (element, options) {
      // TODO: 在此处初始化页面。
    },

    updateLayout: function (element, viewState, lastViewState) {
      /// <param name="element" domElement="true" />
      /// <param name="viewState" value="Windows.UI.ViewManagement.ApplicationView" />
      /// <param name="lastViewState" value="Windows.UI.ViewManagement.ApplicationView" />
      // TODO: 响应 viewState 的变化。
    },

    unload: function () {
      // TODO: 响应离开此页面的导航。
    }
  });
})();
```

注意列表 10.3 中的 JavaScript 文件包含了定义新页面控件的代码。页面控件有三个事件处理器：ready、updateLayout 和 unload。我在下一节中修改事件处理器以支持页面导航。

## 导航到另一个页面

我的应用有一个名为 anotherPage 的页面和一个名为 anotherPage 的页面；我如何在这两个页面之间导航？你使用 WinJS.Navigate() 方法进行导航。

让我向你展示我们如何从主页导航到 anotherPage。在主页的主区域添加如下所示的超链接：

```html
<section aria-label="Main content" role="main">
  <p>Content goes here.</p>
  <a id="lnkAnotherPage">访问另一个页面</a>
</section>
```




本节讨论的代码可以在 GitHub 源码的 `Chapter10\Multipage` 文件夹找到。

接下来，我将修改 `home.js` 文件中的代码，以便在其 `ready` 处理器中为链接设置点击处理器：

```javascript
WinJS.Pages.define("/pages/home/home.html", {
  ready: function(element, options) {
    var lnAnotherPage = document.getElementById("lnAnotherPage");
    lnAnotherPage.addEventListener("click", function (evt) {
      evt.preventDefault();
      WinJS.Navigation.navigate("/pages/anotherPage/anotherPage.html");
    });
  }
});
```

点击事件处理器调用 `preventDefault()` 来防止正常的链接导航发生。请记住，我们正在模拟导航。

接下来，调用 `WinJS.Navigation.navigate()` 方法跳转到 `anotherPage`。

当你点击主页上的链接时，你将跳转到 `anotherPage` 页面（见图 10.6）。更酷的是，在 `anotherPage` 上，返回按钮是可用的。如果你点击返回按钮，将回到主页。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_299_0.png)

图 10.6 页面间的导航

## 理解导航 API

`WinJS.Navigation.navigate()` 方法只是 WinJS 导航 API 的一种方法。你可以使用以下所有方法来控制用户导航：

- back()—允许你返回历史记录。如果你提供一个整数参数，就可以返回历史记录中特定数量的条目。
- forward()—允许你向后记录历史记录。如果你提供一个整数参数，就可以向前历史记录中特定数量的条目。
- navigate()—允许你跳转到特定页面（页面控件）。你还可以提供一个表示页面初始状态的自定义对象。

并且，你可以在导航时使用以下属性：

- canGoBack—当可以返回导航时，返回 `true`。
- canGoForward—当可以向后导航时，返回 `true`。
- history—返回一个表示所有历史条目的对象。该历史对象具有 `current`、`backStack` 和 `forwardState` 属性。
- location—返回与当前页面关联的 URL。
- state—返回与当前页面关联的状态。

最后，导航 API 支持以下三个导航事件：

- beforenavigate
- navigating
- navigated

对于这三个事件中的每一个，你都可以使用 `event detail` 属性来读取 `location` 和 `state` 属性。

## 理解 PageControlNavigator 控件

`PageControlNavigator` 包含在 Navigation App、Grid App 和 Split App Visual 项目模板中——但不包含在 Blank App 或 Fixed Layout App 模板中。该控件主要两件事。

首先，`PageControlNavigator`控件处理 `navigated` 事件并根据此事件加载正确的页面控件。例如，如果你调用 `WinJS.Navigation.navigate("/pages/somePage/somePage.html")`，则 `PageControlNavigator` 会将 `somePage.html` 页面控件加载到默认 HTML 页面中。

其次，该控件启用或禁用返回按钮。如果 `WinJS.Navigation.canGoBack` 的值为 `true`，则启用返回按钮。否则，禁用返回按钮。

## 理解导航状态

在使用导航 API 构建多页面应用时，你可以利用导航状态在返回和页面之间跳转时保留你的状态。历史记录中的每个条目都有一个与之关联的 `state` 属性。你可以为此 `state` 属性分配任何想要的值。

例如，假设你正在构建一个简单的产品目录。应用只有两个页面：显示类别列表的主页，以及显示匹配产品列表的详情页（见图 10.7 和图 10.8）。当你点击主页上的某个类别时，你会在详情页上看到匹配的产品列表。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_301_0.png)

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_302_0.png)

图 10.9 导航状态

当你点击主页上的某个类别时，你会在详情页上看到匹配的产品列表。

当你点击主页上的某个类别时，你会在详情页上看到匹配的产品列表。

图 10.9 导航状态

当你点击主页上的某个类别时，你会在详情页上看到匹配的产品列表。

## 创建多页面应用 287




接下来，我讨论了如何创建页面控件（Page Controls）。页面控件为你提供了一种简单的方法，可以通过 HTML 页面、JavaScript 文件和样式表创建新的 WinJS 控件。

最后，我解释了如何创建一个包含多个页面的单页应用。你学习了如何使用 `PageControlNavigator` 控件——结合导航 API——来动态加载页面控件并模拟导航到单独页面的体验。

# 第 11 章

# 使用 Live Connect API

Live Connect API 允许你从 Windows Store 应用连接到 Live Services。Live Services 为你提供用户身份验证、检索用户信息（包括用户的日历和联系人）以及与用户的 SkyDrive 交互的服务。

在本章的第一部分中，我解释了安装和设置 Live SDK 所需的步骤。例如，学习如何在 Live Connect 网站注册你的 Windows Store 应用。

接下来，我讨论了如何利用名为“零点击单点登录”（zero-click single sign-on）的功能。该功能允许你在无需用户输入用户名和密码的情况下验证其 Windows Store 应用的用户身份。

我还解释了当你的 Windows Store 应用与远程 Web 服务通信时如何利用身份验证。我演示了如何从你的 Windows Store 应用将身份验证令牌传递到 Web 服务。

你还学习了如何从 Live Services 检索用户信息。例如，我向你展示了如何检索当前用户的姓名、生日和个人资料图片。

最后，我讨论了 SkyDrive。你学习了如何从你的 Windows Store 应用将文件上传和下载到被称为“云端硬盘”的 SkyDrive。

## 本章内容

- 安装 Live SDK
- 验证用户身份
- 向 Web 服务传递身份验证令牌
- 检索基本用户信息
- 从 SkyDrive 上传和下载文件

# 安装 Live SDK

在使用 Live Connect API 之前，你需要从微软网站下载适用于 Windows 和 Windows Phone 的最新版本 Live SDK。你可以从 Windows Store 应用开发者中心下载 SDK：http://msdn.microsoft.com/en-us/windows/apps/

# 添加对 Live SDK 的引用

下载 Live SDK 后，你需要为你的 Visual Studio Windows Store 应用项目添加 Live SDK JavaScript 库的引用。选择菜单选项“项目”（Project）、“添加引用”（Add Reference）。在选择“Windows”（Windows）、“扩展”（Extensions）后，勾选 Live SDK 旁复选框（见图 11.1）。

> 警告

下载 Live SDK 后，你需要停止并重新启动 Visual Studio，Live SDK 才会出现在引用管理器中。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_307_0.png)

图 11.1 添加 Live SDK JavaScript 库的引用

接下来，展开你的 References、Live SDK、JS 文件夹，并将 `wl.js` 文件拖入你的默认 HTML 页面。这将添加以下 JavaScript 引用：

```
<script type="text/javascript" src="/LiveSDK/js/wl.js"></script>
```

# 注册你的应用

在使用 Live Connect API 之前，你必须先在 Live Connect 中注册你的应用。访问以下网站：https://manage.dev.live.com/build。

# 安装 Live SDK

不要被网站标题——Windows Push Notifications & Live Connect——误导；这里这里。按照网站上的说明注册你的 Windows Store 应用。不要忘记按照第 3 步的说明更新 Windows Store 应用清单中的信息。

注册后，将显示客户端密钥（client secret）（见图 11.2）。记录此客户端密钥，因为你之后会需要它（在 Web 服务中使用）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_308_0.png)

图 11.2 获取客户端密钥

> 注意
我不认为这是不言说的，但请保好你的客户端密钥。我重新生成了截图中的那个。

你还需要配置另一件事。你必须通过访问以下网站输入你的重定向域名（Redirect Domain）：https://manage.dev.live/Applications/Index。

点击你的应用名称，点击“编辑设置”（Edit Settings），点击“API 设置”（API Settings）选项卡，为重定向域名字段输入值。你可以输入任何喜欢的域名，只要该域名未被占用（见图 11.3）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_308_1.png)

图 11.3 创建重定向域名

为了本章代码get，我输入的重定向域名是 http://livesdkdemo.supersecret.com。

警告
重定向域名必须是域名而不是 URL。如果你没有域名主意了，记住你可以更改主机名，并记住该域名并不指向任何真实内容。

注意
如果你已经将应用提交到 Windows Store，那么在 Live Connect 中注册应用的过程将会有所不同。编辑仪表板（Dashboard），编辑你的应用并点击高级功能（Advanced Features）。遵循配置 Live Connect 服务的说明。

# 初始化 Live Connect SDK

在调用 Live Connect API 提供的任何服务之前，你必须先初始化连接。如代码列表 11.1 所示，通过调用 `WL.init()` 方法初始化连接。

代码列表 11.1 初始化你的连接

```
var REDIRECT_DOMAIN = "http://liveSDKDemo.Superexpert.com";
var scopes = ["WL.signin"]
W.init({
  scope: scopes,
  redirect_uri: REDIRECT_DOMAIN
});

WL.login().then(
  function (LoginResults) {
    // 成功！现在做些什么...
  },
  function (LoginResponse) {
    throw WinJS.ErrorFromName("登录失败!");
  }
);
```

```
$111.1 中的 `WL.init()` 方法调用时带有两个参数：`redirect_uri` 和一个 `scopes` 数组。`redirect_uri` 必须与你在上一节中配置的重定向域名完全匹配。下一节将讨论 `scopes` 数组。

# 指定作用域

你传递给 `WL.init()` 方法的 `scopes` 数组决定了你有权限访问的信息。你可以从 Windows Live 用户账户中提取出各种有趣且令人不安的信息，包括用户的生日、电子邮件地址、邮寄地址、照片和联系人。

以下是作用域（scopes）的部分列表：

- wl.signon——单点登录行为
- wl.basic——对基本个人资料信息和联系人的读取权限。
- wl.offline access——在用户未登录并使用你的应用时读取和更新用户信息的能力。
- wl.birthday——对用户生日的读取权限。
- wl.calendars——对用户日历和事件的读取权限。
- wl.calendars_update——对用户日历和事件的读写权限。
- wl.contacts_birthday——对用户生日和用户联系人生日的读取权限。
- wl.contacts_create——对用户联系人的写入权限。
- wl.contacts_calendars——对用户日历、事件日历及事件的读取权限。
- wl.contacts_photos——对用户媒体和其他用户共享媒体的读取权限。
- wl.skydrive——对用户 SkyDrive 和其他用户共享文件的读取权限。
- wl.emails——对用户电子邮件地址的读取权限。
- wl.events_create——创建事件的写入权限。
- wl.messenger——允许你登录用户的即时消息服务。
- wl.phone_numbers——对用户电话的读取权限。
- wl.photos——对用户媒体的读取权限。
- wl.postal_addresses——对用户邮寄地址的读取权限。
- wl.share——允许你更新用户的状态消息。
- wl.skydrive——对 SkyDrive 用户文件的读取权限。
- wl.skydrive_update——对 SkyDrive 用户文件的读写权限。
- wl.work_profile——对用户工作和就业信息的读取权限。

> 注意
要查看作用域完整列表，请访问 http://msdn.microsoft.com/en-us/library/live/hh243646.aspx。

显然，并不是所有 Windows Store 应用的用户都想要分享关于自己的所有信息。因此，你的 Windows Store 应用必须获得同意才能访问这些信息。





# 第 11 章 使用 Live Connect API

当你首次运行需要特定范围（scope）的 Windows Store 应用时，会弹出一个模态对话框请求用户提供权限。例如，当你带有 `wl.signon` 范围调用 `wl.init()` 时，会显示图 11.4 所示的表单。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_311_0.png)

图 11.4 Windows Store 应用请求登录权限

即使你授予 Windows Store 应用访问你的 Windows Live 用户信息的，也可以在以后撤销这些信息。要撤销权限，请在 Live.com 网站登录你的账户，选择该应用并移除权限（参见图 11.5）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_311_1.png)

图 11.5 撤销 Windows Store 应用权限

# 验证用户身份

Live Connect 为你提供的最有价值的服务是身份验证。Live Connect 支持所谓的“零点击单点登录”（zero-click single sign-on）。

如果你使用 Windows Live 账户登录 Windows 8 电脑，或者你的 Windows Live 账户与你的 Windows 账户关联，那么在使用 Windows Store 应用时无需登录 Windows Live。在运行 Windows Store 应用时，你不需要输入用户名或密码。

注意
用户首次访问你的 Windows Store 应用时，确实需要授予 Windows Store 应用自动登录的权限（参考图 11.4）。然而，用户不需要输入凭据。

# 使用 WL.login()

登录 Live Connect 有两种方式：编程方式或声明式方式。你可以使用 `WL.login()` 方法或使用 `WL.UISignon` 控件。如果你想在应用启动后立即验证用户身份，则应该使用 `WL.login()` 方法。

例如，列表 11.2 中的代码说明了如何为当前用户登录。如果一切正常，页面上将显示“Connected”（已连接）消息。

列表 11.2 使用 WL.login() 方法

```
function () {
  "use strict";

var REDIRECT_DOMAIN = "http://liveSDKDemo.Superexpert.com";

function init() {
  var REDIRECT_DOMAIN = "http://liveSDKDemo.Superexpert.com";
  var spanResults = document.getElementById("spanResults");

  var scopes = {"wl.signin"};
  WL.init({
    scope: scopes,
    redirect_uri: REDIRECT_DOMAIN
  });

  WL.login().then(
    function (loginResults) {
      spanResults.innerText = "Connected";
    },
    function (loginResponse) {
spanResults.innerText = "Error when calling WL.login";
}
document.addEventListener("DOMContentLoaded", init);
}();
```

# 使用 SignIn 控件

对于某些 Windows Store 应用，强制要求在使用应用前进行身份验证并没有意义。你可能想让身份验证成为可选的。如果有人通过验证，他们可能会获得更好的体验（你可以显示他们的姓名）。

在这种情况下，使用 Windows Live SignIn 控件是合理的。你可以将 SignIn 控件放置在抽屉（Flyout）中，以便用户从中登录（参见图 11.6）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_313_0.png)

图 11.6 从抽屉登录

> 注意我在第 6 章中讨论过抽屉（Flyout）控件。

列表 11.3 包含了 signInSettingsFlyout 的 HTML。注意，它包含一个名为 `divControl` 的元素。

列表 11.3 signInSettingsFlyout HTML 文件

```
<!DOCTYPE html>
<html>
<head>
  <title>Security</title>
  <script type="text/javascript" src="signInSettings.js"></script>
</head>
<body>
  <div id="divSignIn"
    data-win-control="WinJS.UI.SettingsFlyout"
    data-win-options="{
      width:'narrow'
    }">
    <div class="win-header"
      style="background-color:#464646">
      <button
        onclick="WinJS.UI.SettingsFlyout.show()"
        class="win-back"></button>
      <div class="win-label">Sign-in</div>
    </div>
    <div class="win-content">
      <div id="divSignIn"></div>
    </div>
  </div>
</body>
</html>
```

Windows Live SignIn 控件是在 `signInSettings.js` 文件中创建的。

列表 11.4 signInSettingsFlyout JavaScript 文件

```
(function () {
  'use strict';

  WinJS.UI.Pages.define("signInSettings.html", {
    ready: function (element, options) {
      WL.ui({
        name: "signin",
        element: "divSignIn",
        theme: "dark"
      });
    }
  });
})
```

Windows Live SignIn 控件通过调用 `WL.ui` 并传入以下选项创建：

- name——要创建的控件类型（目前只有 signin 一个选项）。
- element——与控件关联的 DOM 元素。
- theme——使用“light”或“dark”主题。

> 警告如果你已经授予了应用登录权限，那么 SignIn 控件将没有任何作用——它只会显示一个不会执行注销的按钮。

# 身份验证事件

Live Connect API 支持以下事件：

- auth.login——用户登录时触发。
- auth.logout——用户注销时触发。
- auth.sessionChange——用户访问令牌发生变化时触发。
- auth.statusChange——用户状态变化时触发。
- wl.log——调用 Live 服务时发生错误时触发。

以下代码演示了如何订阅 auth.login 和 auth.logout 事件并显示消息：

```
var spanResults = document.getElementById("spanResults");

WL.Event.subscribe("auth.login", function () {
  spanResults.innerText = "Signed In";
});

WL.Event.subscribe("auth.logout", function () {
  spanResults.innerText = "Signed Out";
});
```

注意，你不是单独使用 `alone` 来监听事件。相反，你使用 Windows Live 的 `WL.Event.subscribe()` 方法来订阅事件。

# 向 Web 服务传递身份验证令牌

假设你想从 Windows Store 应用调用一个远程 Web 服务。例如，如果你正在构建一个任务列表应用，你可能想要调用远程服务获取与远程数据库关联的任务列表。

你如何在 Web 服务中验证用户身份？你需要确保用户无法读取彼此的任务。在远程 Web 服务中，你需要一种方法来识别请求任务的 Windows Store 应用用户。

当你使用 Live Connect API 登录时，你会获得一个身份验证令牌。该令牌包含了你的密钥的哈希值（重新参考“注册你的应用”章节）。

> 注意
身份验证令牌使用名为 JSON Web Token (JWT) 的开放标准。该标准详见：http://tools.ietf.org/search/draft-jones-json-web-token-00。

你可以将此身份验证令牌传递给远程服务。在远程 Web 服务中，你可以使用客户端密钥重生成哈希并验证身份验证令牌。

遵循这一过程，你可以安全地识别与 Web 服务调用关联的用户。让我逐步演示这一过程。

# 从 Windows Store 应用发送身份验证令牌

让我从 Windows Store 应用开始。在第 8 章“创建数据源”中，我展示了如何使用 Web 服务数据源与远程 Web 服务通信。让我再次使用该 Web 服务数据源。

列表 11.5 中的 HTML 页面包含一个 `ListControl`，用于显示任务列表（参见图 11.7）。

列表 11.5 显示任务列表的 HTML 页面

```html
<div id="tmplTask" data-win="WinJS.Binding.Template">
  <div class="taskitem">
    ID: <span data-bind="innerText:id"></span>
    <br /><br />
    名称: <span data-bind="innerText:name"></span>
    <br /><br />
    创建日期: <span data-bind="innerText:dateCreated"></span>
  </div>
</div>
```

```html
<div id="lvTasks"
data-win-control="WinJS.UI.ListView"
data-win-options="{
  itemTemplate: select('#tmplTask'),

  selectionMode: 'none'
}"></</div>
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_317_0.png)

图 11.7 显示任务列表

任务列表通过列表 11.6 中的代码从远程 Web 服务获取。该代码利用了我们在第 8 章创建的 Web 服务数据源。





# 向 Web 服务传递身份令牌

```javascript
));

// 登录到 Live Connect
WL.login().then(
    function (loginResults) {
        // 将 ListView 绑定到数据数据
        var tasksDataSource = new DataSources.WebServiceDataSource(
            serviceURL,
            "id",
            loginResults.session.authentication_token
        );
        lvTasks.itemDataSource = tasksDataSource;
    };
    function (loginResponse) {
        spanResults.innerText = "调用 WL.login 时出错";
    }
});

document.addEventListener("DOMContentLoaded", init);
)();
```

注意，使用 `WL.login()` 方法让当前用户登录 Windows Live。
用户登录后，将从 `session.authentication_token` 属性中获取与用户关联的 Windows Live 身份令牌。

在创建 Web 服务数据源实例时会使用该身份令牌。Web 服务数据源中的每个方法在调用远程服务时都会使用该身份令牌。

例如，列表 11.7 包含了 Web 服务数据源 `getCount()` 方法的代码。注意身份令牌是如何添加到 `WinJS.xhr()` 调用选项中的标头集合中的。

-   LISTING 11.7 Web 服务数据源 getCount() 方法

```javascript
getCount: function () {
    var that = this;

    return new WinJS.Promise(function (complete, error) {
        var options = {
            url: that._url + "/getCount",
            headers: { authenticationToken: that._authenticationToken }
        };
        return WinJS.xhr(options).then(function (xhr) {
            var count = JSON.parse(xhr.response);
complete(count);
}
function(xhr) {
    console.log("Could not call getCount()");
    debugger;
}
}
}
```

重要点是，每当你调用远程 Web 服务时，都需要包含身份令牌。该令牌标识了发起远程 Web 请求的用户。

# 在 Web 服务中验证身份令牌

使此安全流程生效的另一半是在 Web 服务中验证身份令牌。Windows Store 应用调用任务服务，该服务返回一组任务。

Web 服务是使用 ASP.NET Web API 实现的。具体而言，Web 服务被实现为名为 `TasksController` 的 API 控制器类。该类使用 C# 编写。

在 `TasksController` 中，你需要验证身份令牌。Windows Live 团队在 Live SDK 中包含了一个用于验证身份令牌的示例类。该类的名称是 `JsonToken`。

> 注意
> 你可以从位于 https://github.com/liveservice/LiveSDK 的 Windows Live GitHub 账户下载 `JsonToken` 类。查看 ASP.NET 示例部分。

列表 11.8 包含一个名为 `AuthenticationAttribute` 的操作过滤器，它利用了 `JsonToken` 类。此操作从请求头中获取身份令牌，并使用 `JsonToken` 类来验证令牌。

# 列表 11.8 这里的 AuthenticationAttribute 操作过滤器

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web.Configuration;
using JWTSample;

namespace WebServices.Infrastructure
{
    public class AuthenticationAttribute : System.Web.Http.Filters
    {
        [ActionFilter]
        protected override void OnActionExecuting(System.Web.Http.Controllers.HttpContext context)
```

// 从标头中获取 Windows Live 身份令牌
string authenticationToken = null;
try {
    authenticationToken = appContext.Request.Headers.GetValues("authenticationToken").FirstOrDefault();
} catch {
    appContext.Response = new System.Net.Http.HttpResponseMessage(System.Net.HttpStatusCode.Unauthorized);
}

// 从 Web.config 加载客户端密钥
var clientSecret = WebConfigurationManager.AppSettings["CLIENT_SECRET"];
if (string.IsNullOrWhiteSpace(clientSecret)) {
    throw new Exception("缺少身份验证客户端密钥");
}

// 验证令牌
var d = new Dictionary<int, string>();
d.Add(0, clientSecret);
try {
    var myJWT = new JsonWebToken(authenticationToken, d);
} catch {
    app.Response = new System.Net.Http.HttpResponseMessage(System.Net.HttpStatusCode.Unauthorized);
}
```

注意，`AuthenticationTokenAttribute` 从 `Web.config` 文件加载客户端密钥（这是你在注册 Windows Store 应用时获取的）。你需要如下将你的客户端密钥添加到 `Web.config` 的应用设置部分：

```xml
<appSettings>
<add key="aspnet:UseTaskFriendlySynchronizationContext" value="true" />
<add key="webpages:Version" value="2.0.0.0" />
<add key="webpages:Enabled" value="false" />
<add key="PreserveLoginUrl" value="true" />
<add key="ClientValidationEnabled" value="true" />
<add key="UnobtrusiveJavaScriptEnabled" value="true" />
<add key="CLIENT_SECRET" value="bjK0Xdm479wGLp-Ed2sy-09v8jRK6Wb" />
</appSettings>
```

创建 `AuthenticationTokenAttribute` 过滤器操作后，你就可以在 ASP.NET Web API 控制器方法中使用该操作过滤器。例如，`GetCount()` 方法使用 `AuthenticationTokenAttribute` 过滤器修饰如下：

```csharp
[HttpGet]
[AuthenticationToken]
public int GetCount() {
    return db.Tasks.Count();
}
```

如果你尝试在不提供正确身份令牌的情况下访问任何控制器的操作方法，该操作方法将返回 401 Unauthorized 结果。如果你使用 Visual Studio 调试器运行 Windows Store 应用，且没有提供有效的身份令牌，你将看到图 11.8 所示的错误。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_321_0.png)

图 11.8 带有无效身份令牌的 Web 请求

# 获取用户 ID

传递给 Web 服务的身份令牌包含了几个有用信息：

-   AppID—例如，“000000000440CF112”
-   Audience（受众）例如，“liveskedesk.superexpert.com”，
-   ClientIdentifier（客户端标识符）例如，“ms-app://S-1-15-2-3”

# 获取基本用户信息

-   Expiration（过期时间）—例如，7/31/2012 12:51 AM
-   expTime—例如，1343695891
-   Issuer（发行者）例如，“urn:windows:liveid"
-   UserID—例如，“ed63ad02ac2a8522d562fa988699"
-   Version（版本）例如，1

`UserId` 属性特别有用，因为你可以使用 `UserId` 来唯一标识用户并在 Web 服务中关联数据。遗憾的是，它不是用户名或电子邮件地址。列表 11.9 中的代码演示了如何从身份令牌中提取 `UserID` 的值。

# 列表 11.9 获取用户 ID

```csharp
// 获取用户 ID
var authenticationToken = Request.Headers.GetValues("authenticationToken").FirstOrDefault();
var clientSecret = WebConfigurationManager.AppSettings["CLIENT_SECRET"];
var d = new Dictionary<int, string>();
var myJWT = new JsonToken(authenticationToken, d);
var user = myJWT.Claims.UserId;
```





# 310 第 11 章 使用 Live Connect API

> 注意
> Live Connect 支持的所有 REST 对象的文档位于 http://msdn.microsoft.com/en-us/library/live/hh243648.aspx。

让我通过创建一个显示若干用户信息的页面（见图 11.9）向你展示它是如何工作的。JavaScript 源代码包含在列表 11.10 中。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_323_0.png)

图 11.9 从 Live Connect 显示用户信息

# 列表 11.10 从 Live Connect 获取基本用户信息

```javascript
function () {
  "use strict";
  var REDIRECT_DOMAIN = "http://liveSDKDemo.Superex.com";
  function init() {
    var firstName = document.getElementById("spanFirstName");
    var lastName = document.getElementById("spanLastName");
    var birthday = document.getElementById("spanBirthday");
    var status = document.getElementById("spanStatus");
    var imgPhoto = document.getElementById("imgPhoto");

    // 初始化 Windows Live
    var scopes = ["wl.signin", "wl.basic", "wl.birthday"];
    WL.init({
      scope: scopes,
      redirect_uri: REDIRECT_DOMAIN
    });

    // 登录 Windows Live
    WL.login().then(function (loginResults) {
      // 显示基本信息
      callLiveConnect("me", "GET").then(function (results) {
        firstName.innerText = results.first_name;
        lastName.innerText = results.last_name;
        birthday.innerText = results.birth_month
        + "/" + results.birth_day;
      });
    });
}

// 显示个人图片
callLiveConnect("me/picture", "GET").then(function (results) {
  imgPhoto.src = results.location;
});

// 调用 Live
function callLiveConnect(path, method) {
  return new WinJS.Promise(function (complete, error) {
    WL.api({
      path: path,
      method: method
    }).then(function(results) {
      complete(results);
    }, function(results) {
      // 调用 WL.api() 错误
      debugger();
    });
  });
}
document.addEventListener("DOMContentLoaded", init);
}();
```

在列表 11.10 中，所有的重工作都是由 `callLiveConnect()` 方法完成的。该方法使用 `WL.api()` 方法来调用 REST 服务。

`callLiveConnect()` 方法被调用了两次：第一次获取基本用户信息，第二次获取用户照片。

# 在 SkyDrive 上上传和下载文件

Microsoft SkyDrive 允许你将文件存储在云端，以便在不同设备之间轻松共享。每个人都可以获得 7 GB 的免费 SkyDrive 存储空间供你使用。你可以根据喜意向 SkyDrive 添加照片、文档或任何其他类型的文件。

你可以利用 Live Connect API 与用户的 SkyDrive 交互。例如，你可以使用该 API 在 SkyDrive 上上传、下载、复制、移动和删除文件。

# 312 第 11 章 使用 Live Connect API

例如，假设你想创建一个显示照片的 Windows Store 应用程序。你希望用户能够从任何地方的任何计算机查看他们的照片库。在这种情况下，将照片存储在 SkyDrive 上是有意义的。

在本节中，我将解释如何列出用户 SkyDrive 中的文件和文件夹。你可以下载文件，以及如何上传新文件。

> 注意
> 你可以通过访问 http://SkyDrive.Live.com 来访问你的 SkyDrive。

# 列出 SkyDrive 文件夹和文件

让我从基础开始；让我解释你如何获取用户 SkyDrive 上的文件和文件夹列表（见图 11.10）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_325_0.png)

图 11.10 显示 SkyDrive 文件和文件夹列表

我将使用 `ListView` 控件显示 SkyDrive 文件夹和文件列表。列表 11.11 中的 HTML 页面包含一个模板（Template）和一个 `ListView` 控件。该模板显示从 SkyDrive 获取的每个项目的的名称和类型。

# 列表 11.11 用于显示 SkyDrive 文件的 HTML

```html
<div id="tmpl" data-control="WinJS.Binding.Template">
  <div class="fileItem">
    Name: <span data-win-bind="innerText:name"></span>
    <br />
    Type: <span data-win-bind="innerText:type"></span>
  </div>
</</div>
<div id="Files"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplFile'),
    selectionMode: 'none'
  }">
</div>
```

列表 11.12 中的 JavaScript 文件从用户的根 SkyDrive 文件夹中检索文件和文件夹列表。

# 列表 11.12 用于从 SkyDrive 获取文件列表的 JavaScript

```javascript
(function () {
  "use strict";
  var REDIRECT_DOMAIN = "http://liveSDKDemo.Superex.com";

  function init() {
    WinJS.UI.processAll().done(function () {
      var lvFiles = document.getElementById("lvFiles").winControl;

      // 初始化 Live Connect
      var scopes = ["wl.signin", "wl.skydrive"];
      WL.init({
        scope: scopes,
        redirect_uri: REDIRECT_DOMAIN
      });

      // 登录 Live Connect
      WL.login().then(function (loginResults) {
        // 获取顶层 SkyDrive 文件列表
        callLiveConnect("me/skydrive/files", "GET").then(function (results) {
          var items = [];
          for (var key in results.data) {
            items.push(results.data[key]);
          }
          var dsItems = new WinJS.Binding.List(items);
          lvFiles.itemDataSource = dsItems.dataSource;
        });
      });
    });
  }

  // 调用 Live Connect
  function callLiveConnect(path, method) {
    return new WinJS.Promise(function (complete, error) {
      WL.api({
        path: path,
        method: method
      }).then(
        function (results) {
          complete(results);
        },
        function (results) {
          // 调用 WL.api() 错误
          debugger;
        }
      );
    });
  }
document.addEventListener("DOMContentLoaded", init);
})();
```

上述代码的第一部分通过调用带有 `wl.skydrive` 范围的 `wl.init()` 方法初始化与 Live Connect 的连接。要从 SkyDrive 读取文件和文件夹，用户必须同意 `wl.skydrive` 权限。要更新 SkyDrive 中的文件和文件夹，用户必须同意 `wl.skydrive_update` 权限。

接下来，通过调用 `wl.login()` 用户登录。登录后，通过调用路径为 "me/skydrive/files" 的 `callLiveConnect()` 获取用户 SkyDrive 的文件和文件夹列表。此调用从用户的根 SkyDrive 文件夹中检索项目（包括文件和文件夹）。

文件和文件夹列表在 `data` 对象中返回。奇怪的是，文件文件夹列表并没有以 JavaScript 数组的形式返回。相反，列表是以 JavaScript 对象的形式返回的。由于由于原因，使用以下代码将列表转换为数组：

```javascript
for (var key in results.data) {
  items.push(results.data[key]);
}
```

最后，`items` 数组被转换为 List 数据源并绑定到 `ListView`。文件和文件夹列表被显示出来。

# 从 SkyDrive 下载文件

你可以使用 `WL.backgroundDownload()` 方法从用户的 SkyDrive 下载文件。当你调用此方法时，你提供了用户 SkyDrive 上的文件路径以及保存该文件的 `StorageFile`。

让我让我修改我们在上一节中讨论过的 `ListView`，使其支持下载文件。我将修改 `ListView`，使得当你点击 `ListView` 中的一个文件时，会出现一个保存文件的窗口，使你能够将文件从 SkyDrive 保存到本地硬盘上（见图 11.11）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_328_0.png)

图 11.11 从 SkyDrive 保存文件

首先，我需要修改 `ListView` 的选项，以便在点击 `ListView` 目时触发 `iteminvoked` 事件：

```html
<div id="Files"
  data-win-control="WinJS.UI.ListView"
  data-win-options="{
    itemTemplate: select('#tmplFile'),
    tapBehavior: 'invokeOnly'
  }">
</div>
```

接下来，我需要为 `iteminvoked` 事件实现一个处理器，将点击/触摸的项目保存到硬盘上（见列表 11.13）。

列表 11.13 iteminvoked 事件处理器

```javascript
// 设置 invoke 处理器
lFiles.addEventListener("iteminvoked", function (evt) {
  evt.detail.itemPromise.done(function (invokedItem) {
    var itemData = invokedItem.data;

    // 不要下载文件夹和专辑
    if (itemData.type == "folder" || itemData.type == "album") {
      return;
    }

    // 创建保存选择器
    var savePicker = new Windows.Storage.Pickers.FileSavePicker();
```





# 316 第 11 章 使用 Live Connect API

```javascript
savePicker.suggestedStartLocation = Windows.Storage.Pickers.
PickerLocationId.documentsLibrary;
savePicker.suggestedFileName = itemData.name;
savePicker.fileTypeChoices.insert("PNG file, [
```

```javascript
// 显示选择器
savePicker.pickSaveFileAsync().then(function (file) {
  if (file) {
    WL.backgroundDownload({
      path: itemData.id + "/content",
      file_output: file
    });
  }
});
```

当事件被触发时，列表 11.13 中的代码通过 `itemPromise()` 方法获取被点击/触摸的 ListView 项目。

接下来，创建一个 `FileSavePicker` 来保存所选的文件。`FileSavePicker` 被配置为处理 PNG、JPEG 和 Microsoft Word 文。如果你想处理下载其他类型的文件，则向 `FileSavePicker` 的 `fileTypeChoices` 集合中添加新的文件类型。

通过调用 `pickSaveFileAsync()` 方法显示保存屏幕。当用户点击“保存”按钮时，会调用 Live Connect `WL.backgroundDownload()` 方法。该方法从 SkyDrive 下载文件内容，并将文件保存到用户用保存选择器选择的位置。

注意用于保存文件的路径：`itemData.id + "/content"`。你通过使用文件 ID 后接 `/content` 来获取文件的内容（而不是文件的描述）。

# 上传文件到 SkyDrive

如何将文件上传到 SkyDrive 呢？

在上传文件到 SkyDrive 之前，你必须获得用户对更高级权限请求的同意。你需要使用 `wl.skydrive_update` 范围初始化对 Live API 的连接：

```javascript
// 初始化 Live Connect
var scopes = ["wl.signin", "wl.skydrive_update"];
WL.init({
```

```javascript
scope: scopes,
redirect_uri: REDIRECT_DOMAIN
));
```

为了允许用户上传文件，我将修改上一节中的应用，使其包含一个带有上传命令的应用程序栏（见图 11.12）。应用程序栏的声明如下：

```html
<div data-win-control="WinJS.UI.AppBar">
  <button data-win-control="WinJS.UI.AppBarCommand"
    data-win-options={
      id:'cmdUpload',
      label:'Upload',
      icon:'upload',
      tooltip:'Upload File'
    }>
  </button>
</div>
```

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_330_0.png)

图 11.12 上传应用程序栏命令

最后，我需要编写处理调用上传命令的代码。处理上传命令以及上传文件到 SkyDrive 的代码包含列表 11.14 中。

# 列表 11.14 处理上传命令

```javascript
// 设置上传处理器
var cmdUpload = document.getElementById("cmdUpload");
cmdUpload.addEventListener("click", function () {
    var openPicker = new Windows.Storage.Pickers.FilePicker();
    openPicker.fileType.replaceAll(["*"]);
    openPicker.pickingFileAsync().then(function (file) {
        Wi.backgroundUpload({
            path: "me/skydrive",
            file_name: file.name,
            file_input: file
        }).then(function () {
            getFileList();
        });
    });
});
```

列表 11.14 中的代码显示了一个文件选择器，允许你从硬盘中选择文件。当你选择一个文件时，会调用 Live Connect 的 `Wi.backgroundUpload()` 方法，并带有三个参数：

- path—你想要上传文件的 SkyDrive 上的路径。
- file_name—在 SkyDrive 上创建的新文件的名称。
- file_input—从打开的选择器中选取的存储文件。

文件上传后，将调用 `getFileList()` 方法来刷新 ListView 控制显示的文件列表，以便 ListView 控制将显示新上传的文件。

## 总结

本章重点关注了 Live Connect API 这一主题。你学习了如何使用 Live Connect API 支持零点击登录，以便在不需要用户输入用户名和密码的情况下验证用户身份。你还学习了如何将身份验证令牌从 Windows Store 应用传递到远程 Web 服务。

接下来，你学习了如何从 Live Services 中提取关于当前用户的大量信息。例如，我演示了如何从 Live Services 获取当前用户的姓、名、生日和头像。

最后，我解释了如何从 Windows Store 应用与 SkyDrive 交互。你学习了如何列出、下载和上传文件到用户的 SkyDrive 账户。

# 第 12 章

# 图形与游戏

在本章中，你将学习如何使用 Windows Store 应用创建一个简单的游戏。你将学习如何创建一个名为 **Brain Eaters**（大脑吞噬者）的游戏。

Brain Eaters 游戏的目标是在吃食物颗粒的同时避免被僵尸吃掉。如果你吃了所有 5 个食物颗粒，你就赢了游戏。如果你的角色被僵尸吃掉，你就输了（见图 12.1）。

## 本章内容

- 游戏概述
- 创建游戏瓦片
- 播放游戏声音
- 创建游戏画布
- 捕获用户交互
- 创建更新循环
- 创建渲染循环

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_333_0.png)

游戏支持键盘、鼠标、触摸和手写笔。你可以使用键盘上的方向键移动你的角色。或者，如果你使用的是平板电脑，可以触摸屏幕来指示角色应该移动的方向。

游戏还支持不同的显示分辨率。游戏板会自动调整大小以适应可用的屏幕尺寸，因此你可以在低分辨率和高分辨率屏幕上玩该游戏。

> 注意
Brain Eaters 游戏的所有代码都包含在本书源码的 Chapter12\Game 文件夹中。

# 游戏概述

我使用 Visual Studio 导航应用模板创建了 Brain Eaters 游戏。游戏包含以下四个页面：

- Home（首页）——首页包含一个解释规则的简介。
- Play（游戏）——游戏页面包含实际的游戏。
- Lose（失败）——如果你被僵尸抓住，你就输了。
- Win（胜利）——如果你吃了所有 5 个食物颗粒，你就赢了。

首页、失败和胜利页面是简单的 HTML 页面，链接到游戏（见图 12.2）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_334_0.png)

图 12.2 首页

游戏几乎所有的代码都包含在一个名为 `game.js` 的 JavaScript文件中。该类包含了启动游戏、停止游戏、更新僵尸位置以及渲染游戏的代码。

# 创建游戏瓦片

Eaters 游戏是由一组图像瓦片渲染的。图像瓦片简单来说 50 像素乘以 50 像素的图像。游戏板由背景瓦片和墙瓦片渲染。游戏还包含了僵尸、玩家和食物的瓦片。

所有的游戏瓦片都创建一个在一个名为 `tiles.js` 的 JavaScript文件中（见列表 12.1）。

列表 12.1 tiles.js 文件

```javascript
function () {
  "use strict";

  function Tile(url) {
    this.image = new Image();
    this.image.src = url;
```

```javascript
var tiles = {};
tiles.background = new Tile("/images/background.jpg");
tiles.wall = new Tile("/images/brick.jpg");
tiles.player = new Tile("/images/hero.png");
tiles.zombie = new Tile("/images/zombie.jpg");
tiles.hamburger = new Tile("/images/hamburger.gif");

WinJS.Namespace.define("Unleashed", {
  Tiles: tiles
});

}());
```

每个瓦片代表从 images 文件夹加载的图像。例如，墙瓦片代表名为 `brick.jpg` 的图像。

注意游戏包含了 PNG、GIF 和 JPG 图像。可以使用浏览器支持的任何类型的图像创建瓦片。

瓦片集作为属性从 `Unleashed.Tiles` 对象暴露。例如，你可以通过 `Unleashed.Tiles.wall` 属性引用墙瓦片。

# 播放游戏声音

当你被僵尸吃掉时，你会经历嘈闹的死亡。当你吃食物颗粒时，你的角色会说“Yum！”

游戏声音包含在一个名为 `sounds.js` 的文件中（见列表 12.2）。

列表 12.2 sounds.js 文件

```javascript
(function () {
  "use strict";

WinJS.Namespace.define("Unleashed", {
  Sounds:
    yum: new Audio("/sounds/yum.wav"),
    eaten: new Audio("/sounds/eaten.wav"),
    cheer: new Audio("/sounds/cheer.wav"),
  }
});

}());
```




# 创建游戏画布

注意，游戏声音是 WAV 格式的文件。我使用一个名为 Audacity 的程序录制了这些文件，它是一个免费的开源录音器和编辑器。

这些声音以 Unleashed.Sounds 对象的属性形式暴露。例如，使用以下代码播放 Yum 音效：

```
Unleashed.Sounds.yum.play();
```

> 注意
> 我通过录制我的孩子 Jon、Ada 和 Athena 发出僵尸的声音创建了这些文件。

# 创建游戏画布

游戏图形使用 HTML5 Canvas 元素渲染。Canvas 元素在 play.html 页面中如下创建：

```
<div
  data-win-control="WinJS.UI.ViewBox">
    <canvas id="canvas" width="1000" height="750"></canvas>
</div>
```

注意，Canvas 元素包含在一个 WinJS ViewBox 控件中。ViewBox 控件会自动缩放 Canvas 以适应屏幕分辨率。你可以在竖屏模式下的 1,024px x 768px 屏幕上玩游戏（见图 12.3），也可以在横屏模式下的 2,560px x 1,440px 屏幕上玩（见图 12.4）。ViewBox 会自动缩放 Canvas 以适应可用屏幕。

324 第 12 章 图形与游戏

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_337_0.png)

图 12.3 竖屏模式下缩放到 1,024px x 768px 屏幕的游戏

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_337_1.png)

图 12.4 横屏模式下缩放到 2,560px x 1,440px 屏幕的游戏

Canvas 元素声明的宽度为 1,000 像素，高度为 750 像素。所有的游戏瓦片——例如僵尸和墙瓦片——都绘制在这个 Canvas 元素上。

当在 game.js 文件初始化 Game 类时，通过以下代码从 Canvas 元素获取 2D 上下文：

```javascript
// Setup Canvas
this._canvas = document.getElementById("canvas");
this._ctx = this._canvas.getContext("2d");
```

2D 上上下文包含了用于在 Canvas 上绘图的图形 API。例如，图形 API 包含 lineTo()、rect() 和 arc() 等方法，用于绘制线、矩形和弧。

Brain Eaters 游戏仅利用了 Canvas API 的单一方法：drawImage() 方法。drawImage() 方法在 Canvas 的特定位置绘制图像。

例如，玩家瓦片使用以下代码进行渲染：

```
renderPlayer: function () {
  this.drawImage(this._player.tile.image, this._player.x, this._player.y);
}

drawImage: function (image, x, y) {
  this._ctx.drawImage(image, x * TILE_WIDTH, y * TILE_HEIGHT);
}
```

renderPlayer() 方法调用 drawImage() 并传递图像以及 x 和 y 坐标。drawImage() 方法通过调用 2D 上下文的 drawImage() 方法在 Canvas 上绘制图像。

> 注意
> 遗憾的是，你不能在 drawImage() 方法中使用动画 GIF。根据 HTML5 规范，“当向 drawImage() 方法传递动画图像作为参数时，用户代理必须使用动画的预览帧（poster frame），或者如果没有预览帧，则使用动画的第一帧。”真遗憾。

# 捕获用户交互

Brain Eaters 游戏支持键盘、鼠标、触摸和手笔交互。如果你使用键盘，可以使用方向键移动你的角色。

使用以下代码来捕获键盘交互：

```javascript
document.addEventListener("keydown", this.movePlayerKeyboard.bind(this));
```

当你按下按键时，会调用 movePlayerKeyboard() 方法。该方法检测被按下的方向键并改变玩家的方向。

```
movePlayerKeyboard(): function (e) {
  switch (e.keyCode) {
    case WinJS.Utilities.Key.upArrow:
      this._player.direction = Unleashed.Direction.up;
      break;
    case WinJS.Utilities.Key.downArrow:
      this._player.direction = Unleashed.Direction.down;
      break;
    case WinJS.Utilities.Key.leftArrow:
      this._player.direction = Unleashed.Direction.left;
      break;
    case WinJS.Utilities.Key.rightArrow:
      this._player.direction = Unleashed.Direction.right;
      break;
    case WinJS.Utilities.Key.space:
      this._player.direction = Unleashed.Direction.none;
      break;
  }
}
```

movePlayerKeyboard() 方法利用 WinJS.Utilities.Key 枚举来检测按了哪个键盘按键。该枚举包含了键码的人类易读名称列表，因此你可以使用 WinJS.Utilities.Key.upArrow 代替 38。

如果你使用平板设备，则你想使用触摸而不是键盘。在这种情况下，你触摸屏幕来指示角色想要移动的方向。

使用以下代码捕获 MSPoDown 事件。当你按下鼠标按钮、用手指触摸屏幕或用手笔触摸屏幕时，会触发此事件：

```javascript
this._canvas.addEventListener("PointerDown", this.movePlayerTouch.bind(this));
```

当 MSPoDown 事件触发时，会调用 movePlayerTouch() 方法。该方法负责改变角色移动的方向：

```
movePlayerTouch(): function (e) {
  var playerX = this._player.x * TILE_WIDTH;
  var playerY = this._player.y * TILE_HEIGHT;
  var absX = Math.abs(e.offsetX - playerX);
  var absY = Math.abs(e.offsetY - playerY);

if (absX > absY) {
    if (e.offsetX > playerX) {
      this._player.direction = Unleashed.Direction.right;
    } else {
      this._player.direction = Unleashed.Direction.left;
    }
} else {
    if (e.offsetY > playerY) {
      this._player.direction = Unleashed.Direction.down;
    } else {
      this._player.direction = Unleashed.Direction.up;
    }
}
},
```

根据你触摸屏幕的位置，你的角色向不同的方向移动。例如，如果你触摸角色下屏幕，你的角色就会改变方向向下移动。如果你触摸角色的右侧，你的角色就会向右移动（见图 12.5）。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_340_0.png)

图 12.5 触摸屏幕改变方向

# 创建更新循环

Brain Eater 游戏在游戏过程中使用两个循环。游戏执行一个更新循环来更新玩家和僵尸的位置。游戏还执行一个渲染循环来渲染游戏。

更新循环每 250 毫秒执行一次。当开始游戏时，通过对 window.setInterval() 方法的调用触发 executeUpdateLoop() 方法：

```javascript
this._updateLoopId = window.setInterval(this.executeUpdateLoop.bind(this), UPDATE_LOOP_RATE);
```

341 第 12 章 图形与游戏

> 注意
> 在 executeUpdateLoop 方法上调用的 bind() 方法用于将 Game 实例绑定到 executeUpdateLoop 方法上。换句话之，它确保 this 变量在 executeUpdateLoop 方法中指向 Game 实例。

UPDATE_LOOP_RATE 常值为 250 毫秒。如果你想让僵尸追逐，可以减小这个值（数值越小，游戏通常越难）。

executeUpdateLoop() 方法如下：

```
executeUpdateLoop: function () {
    this.updateMonsterPositions();
    this.updatePlayerPosition();
}
```

该方法更新僵尸和玩家的位置。例如，updateMonsterPositions() 方法让所有僵尸向玩家的方向移动。

在更新僵尸和玩家位置的同时，更新循环还会检查碰撞。更新循环必须检查玩家与僵尸以及玩家与食物片之间的碰撞。

例如，updatePlayerPosition() 方法调用以下 collideFood() 方法检测玩家是否走进了食物片：

```
collideFood: function () {
    for (var i = 0; i < this.food.length; i++) {
        var food = this.food[i];
        if (this.player.x === food.x && this.player.y === food.y) {
            Unleashed.Sounds.yum.play();
            this.food.splice(i, 1);
        }
    }

    // 如果没有更多食物，玩家赢了！
    if (this.food.length === 0) {
        this.win();
    }
}
```

collideFood() 方法遍历 JavaScript _food 数组，并检查任何食物片的 x 和 y 坐标是否与玩家的 x 和 y


如果有匹配项，就会播放“Yum！”的声音，并使用 _food.splice()_ 从食物数组中移除食物颗粒。如果所有食物都被吃完，玩家就赢了。

更新循环不会向屏幕渲染任何内容。更新循环负责游戏状态。渲染游戏是渲染循环的职责。

## 创建渲染循环

渲染循环负责渲染游戏板。与由 `window.setInterval()` 方法触发的更新循环不同，渲染循环是通过调用 `requestAnimationFrame()` 方法执行的。

`requestAnimationFrame()` 方法被定义为 W3C 脚本动画计时控制标准的一部分。该方法专门为了创建动画的目的而引入。

当你使用 `requestAnimationFrame()` 方法时，不需要指定屏幕渲染的频率。相反，让浏览器来决定最佳帧率。

这种做法的核心是，浏览器在确定最佳帧率方面比你做得更好。浏览器可以考虑到所有正在渲染的动画，从而让所有动画都变得更加流畅。如果页面当前不可见，浏览器可以限制动画并减少 CPU 资源的消耗。

在 Brain Eaters 游戏中，通过以下代码启动渲染循环：

```
this.animationLoopId = window.requestAnimationFrame(this.executeRenderLoop.bind(this));
```

`executeRenderLoop()` 方法被传递给 `requestAnimationFrame()` 方法。`executeRenderLoop()` 方法如下所示调用它：

```
executeRenderLoop(): function () {
  this.render();
  this._animationLoopId = window.requestAnimationFrame(this.executeRenderLoop.bind(this));
}
```

`executeRenderLoop()` 调用 `render()` 方法，然后立即再次调用 `window.requestAnimationFrame()` 方法。多快再次调用 `executeRenderLoop()` 方法取决于 `window.requestAnimationFrame()` 方法的决定。

> 注意
> `window.requestAnimationFrame()` 方法与 `window.setTimeout()` 方法类似，关键区别在于你不需要指定超时值。`window.requestAnimationFrame()` 方法会计算自己的超时值。

# 第12 章 图形与游戏

`render()` 方法负责绘制屏幕，它的样子如下：

```
render: function () {
  this.renderBoard();
  this.renderFood();
  this.renderMonsters();
  this.renderPlayer();
},
```

`render()` 方法绘制游戏板、食物颗粒、怪物和玩家。

`renderBoard()` 方法通过为游戏板中的每个瓦格调用 `drawImage()` 方法来绘制 20x15 的游戏网格。这里是 `renderBoard()` 方法的样子：

```
renderBoard: function () {
  for (var y = 0; y < VERTICAL_TILES; y++) {
    for (var x = 0; x < HORIZONTAL_TILES; x++) {
      var tile = this.getTile(x, y);
      if (tile) {
        this.drawImage(tile.image, x, y);
      } else {
        this.drawImage(Unleashed.Tiles.background.image, x, y);
      }
    }
  }
}
```

`renderFood()` 和 `renderMonsters()` 方法非常相似；两个方法都会遍历数组并将数组中的每个元素渲染到屏幕。这里是 `renderMonsters()` 方法的样子：

```
renderMonsters: function () {
  for (var i = 0; i < this.monsters.length; i++) {
    var monster = this.monsters[i];
    this.drawImage(monster.tile.image, monster.x, monster.y);
  }
}
```

在之前的代码中，_monsters_ 数组包含一个怪物对象的数组。`drawImage()` 方法被用于将每个怪物绘制到 Canvas 元素上。

最后，`renderPlayer()` 方法如下所示将玩家（游戏主角）渲染到屏幕上：

```
renderPlayer: function () {
  this.drawImage(this.player.tile.image, this.player.x, this.player.y);
}
```

> > 注意
> `requestAnimationFrame()` 方法定义在脚本动画计时控制标准中，地址位于：http://dvcs.w3.org/hg/webperf/raw-file/tip/specs/RequestAnimationFrame/Overview.html

## 总结

本章的目标是通过创建一个 Windows Store 应用来创建一个简单的游戏。我向你展示了如何为游戏创建图像和声音文件，并向了了如何使用 HTML5 Canvas 元素渲染图像。

你还学习了如何创建更新循环和渲染循环。更新循环用于更新游戏板上怪物和玩家的位置。渲染循环用于通过调用 `requestAnimationFrame()` 方法绘制图像瓦片来渲染游戏板。

祝你赢得游戏好运！如果你赢了游戏，你就能听到我孩子的欢呼声。

# 索引

# A

- 关于页面设置、创建, 176-178
- 访问 SkyDrive, 312
- 使用媒体查询自动调整视图状态, 264-266
- 向对象存储中添加对象, 242-243
- 页面控件 (Page Controls) 到导航应用, 283-285
- Live SDK 引用, 294
- Ajax 请求，使用 `xhr()` 函数执行, 69-74
- `any()` 方法, 63
- 应用栏 (app bar), 8-9
- 应用栏命令, 170-173
- 应用栏命令，显示, 173-175
- 应用栏命令，显示, 168-169
- 应用事件 (app events), 253-255
- 激活事件 (activated event),处理, 254-255
- 自定义事件，创建, 257
- 使用 Promise 延迟, 256
- 错误事件 (error event),处理, 255-256
- AppBar 控件 (AppBar control), 167-175
- 应用栏命令, 170-173
- 应用栏命令，显示, 173-175
- 使用查询选择器应用模板, 104-106
- 多页面应用，创建, 280-282
- 导航应用 (Navigation App),撤销, 298
- 权限 (permissions),撤销, 298
- 之前的执行状态，检测, 258-259
- 发布，认证过程, 41-42
- 注册, 294
- 状态同态性 (stateomorphism), 7
- 状态，使用会话 存储, 260-261
- 提交到 Windows Store 发布, 39-40
- 挂起的应用，检测, 258
- 视图状态 (view states), 261-270
- 异步编程, 56-63
- 回调 (callbacks), 57
- Promise, 57-63
- 取消 (canceling), 63
- 组合 (composing), 60-61
- `then(1)` 与 `done()` 方法, 58-60
- 超时 (timeouts),创建, 61-62
- 属性，HTML 验证
- 模式属性 (pattern attribute), 142
- 必须属性 (required attribute), 142
- 音频，播放 Brain Eaters 游戏, 322-323
- 用户验证
- 认证事件，传递到 Web 服务, 302-309
- Web 服务中的认证, 306-308
- 身份验证令牌 (authentication tokens)，登录 Live Connect, 300-302
- 身份验证令牌，传递到 Web 服务, 303-309
- 身份验证令牌，传递到 Web 服务, 303-309
- 身份验证令牌, 308-308
- 验证过程, 306-308
- 获取 userID, 309

# B

- 绑定转换器 (binding converters), 96-100
- 日期和价格绑定转换器, 99-100
- Brain Eaters 游戏
- Canvas 元素，创建, 323-325
- 游戏瓦片，创建, 321-322
- 页面 (pages), 320-321
- 渲染循环，创建, 329-331
- 声音，播放, 322-323
- 更新循环，创建, 327-329
- 用户交互，捕获, 325-327
- 为 Windows Store 应用设置断点
- 使用 Visual Studio 构建 Windows Store 应用,
- 项目模板, 26-33
- 绕过观察对象 (bypassing observables), 82-83

# C

- 回调 (callbacks), 57
- 取消 Promise, 62
- Canvas 元素 (Brain Eaters 游戏),创建, 323-325
- Windows Store 应用的功能 (capabilities),声明, 15-16
- HTML 表单的内容, 91-94
- 日期选择器控件 (DatePicker), 127-128
- Brain Eaters 游戏用户交互, 325-327
- Windows Store 应用认证过程, 41-42
- 链式 Promise, 60
- `change()` 方法，实现, 228
- 魅力 (charms), 9-11
- 类 (classes), 51-56
- 定义, 51-52
- 派自其他类, 53-54
- 合并通知 (coalescing notifications), 81-82
- 关闭 Windows 应用, 12
- 集合 (collections),观察性集合, 83-86
- 组合方法到 JavaScript
- 对象 (object), 54-56
- 跨源资源共享 (CORS), 71
- 微软设计风格, 6
- 应用栏命令, 170-173
- `done()` 与 `then()` 方法, 58-60
- 完整回调 (complete callbacks), 58
- 连接到 IndexedDB 数据库, 242
- 上下文命令，显示, 173-175
- 应用栏 (app bar), 168-169
- Canvas 元素 (Brain Eaters 游戏), 323-325
- 命令式创建, 113-114
- 声明, 109-111
- 日期选择器控件 (DatePicker control), 123-128
- 切换视图控件 (FlipView control), 132-139
- HTML 控件 (HtmlControl), 273-276
- 列表视图控件 (ListView control), 185-196
- 网格布局 (grid layout), 190-193
- 过滤 (filtering), 206-208
- 组组 (grouping), 208-211
- 增量加载 (loading incrementally), 219-221
- 选择 (selecting), 197-204
- 排序 (sorting), 204-205
- 列表布局 (list layout), 190-193
- 主/详情视图 (master/detail view),创建, 198-202
- 多项选择 (multiple items), 202-204
- 防止重叠项 (overlapping items), 193-196
- 动态切换模板 (templates), 216-219
- 自定义应用事件, 257
- 自定义数据源
- `change()` 方法，实现, 228
- 错误处理, 228-229
- `IListDataAdapter` 接口, 224-225
- `insertAtEnd()` 方法，实现, 227
- `itemsFromIndex()` 方法，实现, 225-226
- `remove()` 方法，实现, 227-228
- `setNotificationHandler()` 方法，实现, 229-230
- 数据适配器 (data adapter), 224-225
- 日期和价格绑定转换器, 99-100
- 外部模板 (external templates), 106-107
- 文件数据源 (file data sources), 230-236
- 游戏瓦片 (Brain Eaters 游戏), 321-322
- IndexedDB 数据源, 241-252
- 混入 (mixins), 54-56
- 多页面应用 (multipage apps), 280-291
- 观察对象 (observables), 78-79
- 监听器 (listeners), 79-81
- 页面 (Page), 276-280





# D

承诺 (promises), 60-61

数据适配器, 创建, 224-225

超时 承诺, 61-62

渲染循环 (Brain Eaters 游戏), 329-331

数据绑定
- 富文本编辑器, 155-156
- 绑定转换器, 96-100
- 更新循环 (Brain Eaters 游戏), 327-329
- 声明式数据绑定, 86-100
- Web 服务数据源, 236-241
- 绑定转换器, 96-100

Windows Store 应用
- HTML 文档, 获取内容,
    + 应用功能, , 15-16
    + 91-94
    + HTML 页面, 16-17
    + 以及 WinJS 控件, 94-95
    + JavaScript 文件, 16-18
- 数据源
    + 样式表, 17-18
- 自定义数据源, 创建
    + Visual Studio 项目, 13-14
- `change()` 方法, 实现, 228
- WinJS 控件, 命令式创建, 113-114
- 数据适配器, 创建, 224-225
- 错误处理, 228-229

CSS3 (层叠样式表 3)
- 作为 Windows Store 应用元素, 22
- 视图状态, 自动适配
    + 媒体查询, 264-266
- `getCount()` 方法, 实现, 225
- `insertAtEnd()` 方法, 实现, 227
- 自定义应用事件, 创建, 257
- `itemsFromIndex()` 方法, 实现, 225-252

- 自定义数据源, 创建
    - 数据适配器, 创建, 224-225
    - 错误处理, 228-229
- `remove()` 方法, 实现, 227-228
- `getCount()` 方法, 实现, 225
- `insertAtEnd()` 方法, 实现, 227
- `itemsFromIndex()` 方法, 实现, 225-252
- `setNotificationHandler()` 方法, 实现, 229-230
- `setNotificationHandler()` 方法, 实现, 229-230
- 文件数据源, 创建, 230-236
- 自定义表单验证 (HTML), 143-144
- IndexedDB 数据源, 创建, 241-252, 245-252
- 定制
    - 日期显示 (DatePicker 控件), 126-127
    - Web 服务数据源, 创建, 236-241
- data-*
- 表单验证错误, 144-146
- 数据库
- 评分 (Ratings 控件), 121
- IndexedDB, 241-245
- XMLHttpRequest 对象属性, 73-74
- 数据库, IndexedDB
    - 连接到, 242-245
    - 索引, 244-245
    - 键范围, 244-245
    - 对象, 添加到对象存储, 242-243
    - 对象, 从对象存储中检索, 243-244

# 错误样式
- 337

data-win-bind 属性 (SPAN 元素), 87-88
日期和价格绑定转换器, 创建, 99-100
设备 Charm (Devices charm), 10
对话框, 显示, 182-183
显示
- DatePicker 控件, 123-128
- 日期
- 标题栏上下文命令, 173-175
- 表单进度, 156-158
- 模态对话框, 182-183
- 获取, 127-128
- 显示, 定制, 126-127
- 格式化, 124-126
- 页码 (FlipView), 135-137
- 弹出层, Flyout 控件, 161-163
- 调试 Windows Store 应用, 35-38
- 断点, 设置, 37
- DOM 资源器, 37-38
- 少即多, 微软设计风格原则, 6
- Visual Studio JavaScript 控制台, 35-36
- 声明式数据绑定, 86-100
- 绑定转换器, 96-100
- HTML 表单, 获取内容, 91-94
- 以及可观察对象 (observables), 89-91
- 以及 WinJS 控件, 94-95
- `done()` 方法对比 `then()` 方法, 58-60
- 从 SkyDrive 下载文件, 314-316

# E
Windows Store 应用元素
- CSS3, 22
- HTML5, 21-22
- JavaScript, 21
- 查询, 23-25
- Windows Runtime, 22-23
- WinJS, 23
- 声明式模板, 103-104
- 声明
    - 菜单控件, 164-165
    - Windows Store 应用功能, 105, 111-113
    - WinJS 控件, 109, 111
- 使用承诺延迟应用事件, 256
- JavaScript 类, WinJS.ClassName(method, 51-52
- 命名空间
    - WinJS.Namespace.define(method), 46-48
    - WinJS.Namespace.defineWithParent(method), 48
    - 从其他类派生, 53-54
    - 视口 (viewports), 267-270
- 检测
    - 之前的应用执行状态, 258-259
    - 挂起的应用, 258
- 确定性进度指示
- 电子邮件地址, 在 HTML 表单中输入, 151-153
- 封装函数, 48-51
- 在 HTML 表单中输入数字, 149-150
- 错误回调, 58
- 错误事件, 处理, 255-256
- 错误处理
    - 自定义数据源, 228-229
    - `done()` 方法对比 `then()` 方法, 58-60
    - 针对 HTML 验证定制的错误样式, 144-146

# 事件
- 事件, 应用事件, 253-257
- 激活事件, 处理, 254-255
- 自定义事件, 创建, 257
- 使用承诺延迟, 256
- 错误事件, 处理, 255-256
- 外部模板, 创建, 106-107
- 表单, 重置, 146-147
- 模式属性 (pattern attribute), 142-143
- 必须属性 (required attribute), 142
- 格式化
    - 日期 (DatePicker 控件), 124-126
    - 时间 (TimePicker 控件), 131
- 表单
    - 输入元素, 147-153
    - 电子邮件地址, 151-153
    - 字段, 154-155
    - 字段, 标签, 148-149
    - 数字, 输入, 149-150
    - 搜索词, 151-153
    - 电话号码, 151-153
    - URL, 151-153
- 特性
    - CSS3, 22
    - HTML5, 21-22
    - Windows Store 应用, 8-12
    - Fiddler 工具, 236
    - 文件 API (HTML5), 21
    - 文件数据源, 创建, 230-236
    - Microsoft SkyDrive
        - 下载, 314-316
        - 列表, 312-314
        - 上传, 316
    - 列表中的值, 153-154
    - 进度指示器, 156-158
    - 富文本编辑器, 创建, 155-156
    - 封装, 48-51
    - 指定类型, 72-73
    - 填充视图状态, 11-12, 261-264
    - ListView 列表项, 206-208
    - 固定布局 (Visual Studio), 31-33
    - FlexBox, 222
    - FlipView 控件, 132-139
    - 页码, 显示, 135-137
    - 游戏磁片, 创建 (Brain Eaters), 321-322
    - Grid 模板 (Visual Studio), 27-28
    - 网格布局 (ListView 控件), 190-193
    - ListView 列表项, 208-211
    - SkyDrive 文件夹, 312-314
    - 表单验证 (HTML5)
        - 自定义验证, 143-144
        - 错误样式, 定制, 144-146

# jQuery 339

# 处理
- 激活事件, 254-255
- 错误事件, 255-256
- 内部方法, 48-51
- 选择器, 63
- QueryCollection 类, 68-69
- WinJS.Utilities.Children() 方法, 67-68
- WinJS.Utils.Id() 方法, 66-67
- WinJS.Canvas 方法, 64-66

# HTML 文档
- HTML 表单, 获取内容, 21-94
- HTML 页面, 创建用于 Windows Store 应用, 16-17
- HTML5
    - 作为 Windows Store 应用元素, 21-22
    - 元素, 创建, 323-325
    - 表单验证
        - 自定义验证, 143-144
        - 错误样式, 定制, 144-146
        - 表单重置, 146-147
        - 模式属性, 142-143
        - 必须属性, 142
    - 输入元素, 147-155
    - 电子邮件地址, 151-153
    - 字段, 154-155
    - 字段, 标签, 148-149
    - 数字, 输入, 149-150
    - 搜索词, 151-153
    - 电话号码, 151-153
    - URL, 151-153
- 列表中的值, 153-154
- `insertEnd()` 方法, 实现, 227
- 安装 Live SDK, 244-298
- 智能提示文件, 24
- 隐藏内部方法, 48-51

# J
- JavaScript
    - 类
        - 定义, 51-56
        - 从其他类派生, 53-54
        - 作为 Windows Store 应用元素, 21
        - 混合入 (mixins), 创建, 54-56
- 用于 Windows Store 应用的 文件, 18-20
- `join()` 方法, 63
- jQuery, 作为 Windows Store 应用元素, 23-25

# K-L
- 键范围, 244-245
- 键盘支持, 8
- 标签表单字段, 148-149
- 横屏视图状态, 261-264
- 轻量消失, 161
- 列表布局 (ListView 控件), 190-193
- 监听器, 创建, 79-81
- Microsoft SkyDrive 文件和文件夹, 312-314
- ListView 控件, 185-196
- 网格布局, 190-193
- 过滤, 206-208
- 分组, 208-211
- 增量加载, 219-221
- 选择, 197-204
- 排序, 204-205
- 列表布局, 190-193
- 主/详情视图, 创建, 198-202
- 多个项, 选择, 202-204
- 防止重叠项, 193-196
- 动态切换模板, 216-219
- 使用 Semantic Zoom 切换视图, 211-216
- Live Connect API
- 身份验证事件, 302
- 安装 Live SDK, 294-298
- 登录 SignIn 控件, 300-302
- `WL.login()` 方法, 299-300
- 用户信息, 检索, 309-311
- 用户, 验证, 299-302
- Live SDK
    - 初始化, 296
    - 安装, 244-298
    - 添加引用, 294
- Live Services, 293
- 增量加载 List 控件, 219-221
- 登录 Live Connect
    SignIn 控件, 300-302
    - `WL.login()` 方法, 299-300

# M
- 主/详情视图 (ListView 控件), 创建, 198-202
- 媒体查询, 22
- 使用 `mediaMatch()` 方法执行, 266-267
- 视图状态, 适配, 264-266
- `mediaMatch()` 方法, 266-267
- 菜单命令支持 (菜单控件), 164
- 菜单控件
    - 声明, 164-165
    - 弹出层, 显示, 165-166
    - 支持的菜单命令, 164
- 方法
    - `change()` 方法, 实现, 228
    - `done()` 方法对比 `then`, 58-60
    - 封装, 48-51
    - `getCount()` 方法, 225
    - `getCount()` 方法, 实现, 225
    - IListData 接口, 224-225
    - `insertEnd()` 方法, 实现, 227
    - `mediaMatch()`, 266-267
    - 对于 QueryCollection 类, 68-69
    - `remove()` 方法, 实现, 227-228
    - `setNotificationHandler()` 方法, 实现, 229-230
    - `timeout()` 方法, 61-62
    - `window.setInterval()`, 61
    - `nJS.Classdefine()`, 51-52





WinJS.Class.derive(), 53-54
WinJS.Class.mix(), 54-56
WinJS.Namespace.define(), 46-48
WinJS.Namespace.defineWithParent(method), 48
WinJS.Utilities.children(), 67-68
WinJS.Utilities.id(), 66-67
WinJS.Utilities.query(), 64-66
WL.api(), 309
WL.login(), 299-300

Microsoft 设计风格原则, 6-7
Microsoft SkyDrive
访问, 312
文件
下载, 314-316
列出, 312-316
上传, 316-318
mixins, 创建, 54-56
模态对话框, 显示, 182-183
鼠标, 支持, 8
多页应用,创建, 280-291
导航应用 (Navigation App), 280-282
多继承，通过 mixins 支持, 55
多项目 (ListView 控件), 选择, 202-204

# N

命名空间, 46
定义
WinJS.Namespace.define(method) 方法, 46-48
WinJS.Namespace.defineWithParent(method), 48
导航栏, 8-9
页面间导航, 285-286

重叠项目 (ListView 控件) 341

导航 API (Navigation API), 286-287
导航状态, 287-291
导航应用 (Navigation App)
创建, 280-282
页面间导航, 285-286
页面控件 (Page Controls), 233-285
PageControlNavigator 控件, 287
导航状态, 278-291
通知
绕过, 82-83
合并, 81-82
数字,在 HTML 表单中输入, 149-150

# 0

对象
添加到对象存储器, 242-243
可观察对象 (observables)
创建, 78-79
以及声明式数据绑定, 89-91
WinJS.Binding.List, 83-85
可观察对象
集合, 配合, 83-86
创建, 78-79
以及声明式数据绑定, 89-91
监听器, 创建, 79-81
通知
绕过, 82-83
合并, 81-82

选项
WinJS 控件, 114-115
xr(function, 71-72
重叠项目 (ListView 控件), 防止, 193-196

342 页面控件

# P

页面控件 (Page Controls)
添加到导航应用, 238-285
创建, 276-280
页码, 显示 (FlipView 控件), 135-137

PageControlNavigator 控件, 287
页面

+   Brain Eaters 游戏, 320-321
页面间导航, 285-286

向 Web 服务传递身份验证令牌, 303-306
验证过程, 306-308

pattern 属性, HTML 表单验证, 142-143

权限,为 Windows Store 应用撤销, 298
个人设置,为 Windows Store 应用创建, 178-181

 弹出窗口, Flyout 控件, 161-163
竖屏视图状态, 261-264

防止重叠项目 (ListView 控件), 193-196
工匠精神, Microsoft 设计风格原则, 6

私有方法, 48
进度回调, 156-158
项目模板,在 Visual Studio 中选择, 26-33

固定布局模板 (Fixed Layout template), 31-33
Grid App 项目模板, 27-28
Split App 项目模板, 30-31

承诺 (promises)
应用事件, 延迟执行, 256
取消, 62
链式调用, 60
组合, 63

创建, 60-61
计时承诺 (time promises), 创建, 61-62
原型继承,从其他类派生类, 53-54
公有方法, 48

将 Windows Store 应用发布到 Windows Store, 38-42
认证过程, 41-42
提交你的应用, 39-40

# Q

查询选择器 (query selectors), 63-69
QueryCollection 类, 68-69
语法, 64
模板, 应用, 104-106
WinJS.Utilities.children(parent) 方法, 67-68
WinJS.Utilities.id(id) 方法, 66-67
WinJS.Utilities.query() 方法, 64-66
QueryCollection 类, 68-69

# R

评分控件 (Rating control), 120-123
评分 (ratings)
自定义, 121
提交, 121-123
引用, 添加到 Live SDK, 294
注册
Windows Store 应用, 294-296
作为 Windows Store 开发者, 38-39
remove() 方法, 实现, 227
渲染循环 (Brain Eaters 游戏), 创建, 329-331
请求 (Ajax),使用 xr() 执行, 69-74
required 属性, HTML 表单验证, 142
重置 HTML 表单, 146-147
分辨率 (resolution)在 Visual Studio 中更改, 265
视口 (viewports), 定义, 267-270

检索 (retrieving)
来自对象存储器, 243-244
来自 Live Connect, 309-311
来自身份验证令牌, 308
来自 WinJS 控件, 115-116
为 Windows Store 应用撤销, 298
富文本编辑器, 创建, 155-156

运行
Windows Store 应用, 31-35

# S

范围 (scopes),为 Windows Store 应用指定, 296
屏幕分辨率,在 Visual Studio 中更改, 265
搜索 (search), 10
在 HTML 表单中输入, 151-153
ListView 控件中的项目, 197-204
带缩放功能的 ListView , 211-216
会话状态, 260-261
setNotification 方法, 实现, 229-230
设置器 (setters)
调试 Windows Store 应用, 37-38
状态 (TimePicker 控件), 130-131
设置 (settings)
为 Windows Store 应用创建, 176-178
共享, 10
登录到 Live Connect, 300-302
拟物化, 7
SkyDrive
访问, 312
下载, 314-316
列出, 312-316
上传, 316-318
吸附视口状态, 11-12, 261-264
排序 ListView 项目, 204-205
声音 (Brain Eaters 游戏), 322-323
data 属性 (HTML), 87-88
指定 Windows Store 应用范围, 296-298
流畅性, Microsoft 设计原则, 6
Split App 项目模板 (Visual Studio), 30-31
开始, 10
状态 (ToggleSwitch 控件), 确定, 118-120
存储会话状态, 260-261
样式表,为 Windows Store 应用创建, 17-18
提示 (Tooltip), 117
支持, 8
提交应用到 Windows Store, 39-40
评分 (Rating 控件), 121-123
通过 mixins 支持多继承, 95
悬挂应用, 检测, 258
悬挂应用 343
切换
用户体验, Microsoft 设计原则, 6-7
动态切换 ListView 模板, 216-219
来自 Live Connect 的信息, 309-311
带缩放功能的 ListView 控件, 211-216
用户交互 (Brain Eaters 游戏), 捕获, 325-327
查询选择器语法, 64
来自身份验证令牌, 308-309

# U

# V

电话号码,在 HTML 表单中输入, 151-153
验证属性 (HTML5), 21
模板
从值列表中在 HTML 表单中输入, 153-154
使用查询选择器应用, 104-106
声明式模板, 103-104
变量范围, 49
外部模板, 创建, 106-107
命令式模板, 100-103
在 Web 服务中验证身份验证令牌, 306-308
ListView 控件动态切换, 216-219
视图状态, 11-12, 261-270
模板 (HTML), 100-107
使用媒体查询自动适应, 264-266
在 Visual Studio 中测试 Windows Store 应用, 259-260
全屏视图状态, 261-264
then() 方法与 done(), 58-60
横屏视图状态, 261-264
超时承诺, 创建, 61-62
竖屏视图状态, 261-264
TimePicker 控件, 128-131
吸附视口状态, 261-264
time
视口, 227-270
格式化, 131
查看技巧, 9
设置, 130-131
视口, 定义, 267-270
views





# Y-Z

- 选项, 114-115
- 级控制, 120-123
- 从 HTML 文档中检索, 115-116
- TimePicker 控制, 128-131
- ToggleSwitch 控制, 118-120
- Tooltip 提示控件, 116-118
- 模块, 封装函数, 48-51
- 命名空间, 定义, 46-48
- 导航 API, 286-287
- WinJS.Binding.List 对象, 83-85
- WinJS.Class.define() 方法, 51-52
- WinJS.Class.derive() 方法, 53-54
- WinJS.Class.mix() 方法, 54-56
- WinJS.Namespace.define() 方法, 46-48
- WinJS.Namespace.definePropertyWith(method, 48
- WinJS.Utilities.children() 方法, 67-68
- WinJS.Utilities.id() 方法, 66-67
- WinJS.Utilities.query() 方法, 64-66
- 胜出一筹，微软设计风格原则, 7
- WL.api() 方法, 309
- WL.login() 方法, 登录 Live Connect, 299-300
- 自定义数据源, 133
- 是/否对话框, 创建, 183
- 零点击登录, 299

# X

- xhr() 函数
- Ajax 请求, 执行, 69-74
- 选项, 71-72
- 指定响应类型, 72-73
- 自定义 XMLHttpRequest 对象属性, 73-75

# UNLEASHED (释放)

Unleashed 带你超越基础知识，为需要充分挖掘技术潜力的专业人士提供了一份详尽且技术上精深的参考。它是获取专家实用建议的最佳资源，也是对最新技术最深入的覆盖。

Informit.com/unleashed

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_364_0.png)

Microsoft Visual Studio LightSwitch Unleashed

ISBN-13: 9780672335532

# OTHER UNLEASHED TITLES (其他 Unleashed 系列书目)

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_364_1.png)

Windows 8 Apps with XAML and C# Unleashed

ISBN-13: 9780672336010

- Windows Phone 7.5 Unleashed
ISBN-13: 9780672333484
- ASP.NET Dynamic Data Unleashed
ISBN-13: 9780672335655
- Microsoft System Center 2012 Unleashed
ISBN-13: 9780672336126
- System Center 2012 Configuration Manager (SCCM)
ISBN-13: 9780672334375
- Windows Server 2012 Unleashed
ISBN-13: 9780672336225
- Microsoft Exchange Server 2013 Unleashed
ISBN-13: 9780672336119
- MVVM Unleashed
ISBN-13: 9780672334382
- System Center 2012 Operations Manager Unleashed
ISBN-13: 9780672335914
- Microsoft Dynamics CRM 2011 Unleashed
ISBN-13: 9780672335389
- SharePoint Designer 2010 Unleashed
ISBN-13: 9780672331053
- ASP.NET 4.0 Unleashed
ISBN-13: 9780672331121
- Silverlight 4 Unleashed
ISBN-13: 9780672333361

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_364_2.png)

Microsoft Visual Studio 2012 Unleashed

ISBN-13: 9780672336256

informit.com/sams

# 获取构建 Windows Store 应用的帮助

来自《Windows 8 Apps with HTML5 and JavaScript Unleashed》作者 Stephen Walther

如果您需要构建 Windows Store 应用的培训，我们可以上门赴贵公司提供实操培训。请访问 SuperexTraining.com 了解更多信息。

我们的开发者团队可以帮助您构建 Windows Store 应用。访问 Superexpert.com 了解更多信息。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_365_0.png)

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_366_0.png)

注册您拥有的 Addison-Wesley、Exam Cram、Prentice Hall、Que 和 Sams 产品以解锁丰厚福利。

注册您的产品可以解锁以下福利：

- 访问补充内容，包括赠送章节、源代码或项目文件。
- 可在下次购买时使用的优惠券。

要开始注册流程，请访问 informit.com/register 登录或创建账户。随后系统将提示您输入产品封封上显示的 10 位或 13 位 ISBN。

注册福利随产品而异。福利将列在您账户的“已注册产品”（Registered Products）下。

# InformIT — 值得信赖的技术学习源

INFORM 是旗下领先技术出版品牌的所在地，包括 Addison-Wesley Professional、Cisco Press、Exam Cram、IBM Press、Prentice Hall Professional、Que 和 Sams。在这里，您将获得来自技术作者、创作者、创新者和领导者的高质量且值得信赖的内容和资源。无论您是在寻找关于新技术的书籍、有帮助的文章、及时的时报，还是访问 Safari Books Online 数字图书馆，Informit 都能为您提供解决方案。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_366_1.png)

Addison-Wesley | Cisco Press | Exam Cram IBM Press | Que | Prentice Hall | Sams SAFARI BOOKS ONLINE

# informIT.com — 值得信赖的技术学习源

**InformIT** 是皮森的一个品牌，也是全球领先技术出版者的在线平台。它是您获取可靠、合格的内容与知识的来源，提供访问技术社区顶尖品牌、作者和贡献者的渠道。

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_367_0.png)

# 在 InformIT 学习 IT

正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？正在寻求及时且相关的信息和教程？正在寻找关于新技术的书籍、电子书或培训视频吗？



# 使用 HTML5 和 JavaScript 释放 Windows 8 应用

已经熟练掌握 JavaScript 和 HTML 吗？微软刚刚赋予了你为 Windows ® 构建突破性应用的能力。这是一个难得的机会——畅销书、微软开发书籍作者 Stephen Walther 将向你展示如何充分利用它。

Walther 提供了深度的见解和实用的代码，这曾让他的《ASP.NET Unleashed》成为有史最畅销的 ASP.NET 书籍。书中涵盖了你使用 JavaScript 和 HTML5 构建、测试和分发卓越 Windows 8 软件所需的所有内容。

Walther 阐明了 Windows 8 为 Web开发者提供的独特优势。他将引导你如何微软微软新的 WinJS 库来为微软全新的 Windows 版本开发应用——你将学习如何使用 Windows 模板、控件和绑定——你将发现从使用 ListView 显示数据到支持 SkyDrive 云存储，以及使用 IndexedDB 和 HTML5 表单创建游戏等所有内容的深度介绍。

如果你是一名开发者，Windows 8 为你提供了许多潜在用户——而你已经拥有触达他们所需的技能。通过此书，掌握你尚未掌握的工具和技术——去开拓你的新市场吧！

## 关于如何...详细信息

- 在 Windows Store 中发布你的应用
- 创建与触摸、键盘、手写笔和鼠标完美运行的应用
- 使用 JavaScript 控件，例如 Tooltip、Rating 和 FlipView 控件
- 彻底掌握 WinJS ListView 以显示、排序和过滤数据
- 使用 HTML5 Canvas 构建街机游戏
- 在本地文件系统、通过远程 Web 服务或 IndexedDB 数据库中存储数据
- 使用 Live Services 验证用户身份、检索用户配置并与 SkyDrive 交互
- 使用 Page Controls 创建自定义 WinJS 控件
- 构建能够优雅适应不同屏幕分辨率和方向的应用
- 从网络摄像头拍摄照片并播放声音

**Stephen Walther** 曾任 ASP.NET 团队高级程序经理，负责微软 Ajax 并与 jQuery 团队紧密合作。他现在拥有 Superex，这是一家软件咨询和培训公司，为微软等客户使用 JavaScript、HTML5 和 ASP.NET MVC 构建应用程序。

类别：编程/Windows Store 应用
涵盖内容：Windows Store 应用
用户级别：中级/高级

> 购买此书即可可获得 45 天在线版免费访问权限 = 详情见最后一页

ISBN-13: 978-0-672-33605-8
ISBN-10: 0-672-33605-9

53999

SAMS
informit.com/sams
informit.com/unleashed

9 768062 336058

网络资源：
在可用时，请从 informit.com/title/97806723 下载书中介绍的所有示例和源代码。

$39.99 美元 / $41.99 加元

![](img/3fb402034fe87fe7c8b9c70e5eae6c75_371_0.png)

永无学习

# PEARSON

