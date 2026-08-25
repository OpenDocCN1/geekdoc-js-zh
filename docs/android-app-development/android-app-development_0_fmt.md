
# Android 应用开发

## 献词

献给 Kristin、Héléna 和 Louis

## 前言

![](img/chapopener.jpg)

### 本书目的及读者对象

《Android 应用开发》涵盖了 Android 开发的核心主题：XML 资源（包括样式）、XML 定义的图形用户界面、程序化定义的图形用户界面、事件驱动编程、活动生命周期、如何管理多个活动、活动间的过渡、持久化数据（包括 SQLite）、如何管理屏幕方向、片段、如何制作设备无关的应用，以及如何在另一个应用中使用应用。本书还涵盖了“趣味”主题，如触摸、滑动、图形、声音和游戏编程。最后，还涉及一些更专业的主题：地图、语音识别、如何制作包含远程数据检索和 XML 解析的内容应用、GPS、如何制作小部件、应用内广告和加密。

本课程理想地安排在 Java 课程之后。虽然学生最好在参加 Android 课程之前接触过事件处理编程，但这并非必需。图形用户界面编程和事件处理将得到详细解释。

### 覆盖范围与方法

本书的方法是在每一章中使用一个应用来阐述所介绍的概念。该应用通常采用模型-视图-控制器架构。它以渐进的方式构建，从版本 0 开始，然后是版本 1，依此类推。我们随着应用版本的推进，根据应用的需要逐步添加概念和主题。因此，每个应用在课堂上都是可管理的。教师可以选择下载模型并简要解释，而不必详细讲解。模型类使用简单的 Java 代码，无需过多解释。我们还尝试使用简单而有意义的应用，使学生能够轻松理解和关联。如果教师不想涵盖某章的部分主题，可以只讲解应用的早期版本。此外，许多章节相互独立，不必按照本书呈现的顺序进行讲解。

### 教学法

在每一章中，也就是在每个应用中，教师可以选择要涵盖的主题、深度以及进度。模型通常使用基本的 Java 类且与 Android 无关，可以下载并简要解释。这样教师可以专注于视图和控制器，其中包含 Android 特有的主题。每章都包含屏幕截图、示例和表格，以说明当前的概念和章节应用的当前状态。软件工程和常见错误框突出显示了各章中的软件工程技巧和常见错误。每章末尾提供章节总结，随后是练习、问题和项目，以测试学生的知识。每章包含大量的选择题、代码填空和编写应用的练习。

- ▸ 模型：`TipCalculator` 类
- ▸ 视图：`activity_main.xml`
- ▸ 控制器：`MainActivity` 类

![](img/fm01fig01.jpg)

图 2.2 选定的布局管理器类

| XML 属性 | 方法 | 描述 |
| --- | --- | --- |
| `android:textSize` | `void setTextSize( int unit, float size )` | 设置文本的大小 |
| `android:hint` | `void setHint( int resource )` | 设置要显示的提示文本 |

表 2.6 `TextView` 的 `android:textSize` 和 `android:hint` XML 属性

### 逐章概述

前九章涵盖了 Android 应用开发的核心概念。最后七章涵盖了更具体的主题。

附录包括关于多个章节中使用的概念的迷你章节：获取设备的尺寸（包括状态栏和操作栏）、动态调整 `TextView` 的字体大小、使用 `AsyncTask` 在后台执行任务（以从远程位置检索数据），以及使用 Google Play 服务。这有助于使大多数章节相互独立，以便教师可以选择要讲解的章节。

许多基础概念涵盖在第 1 章、2 章、3 章和 4 章中，因此我们建议教师尽早按此顺序讲授这些章节。第 2 章广泛介绍了 XML 资源的概念，包括字符串、颜色和样式，以及事件驱动编程。这些概念在全书反复使用。第 3 章是我们首次以编程方式构建 GUI 的章节。我们在第 5 章、第 7 章和第 13 章中也采用了这种方式。因此，最好尽早讲授第 3 章。第 4 章是首个涉及多个活动的章节。第 5 章、10 章、12 章和 13 章也涉及多个活动。因此，第 4 章也应尽早讲授。第 7 章（触摸与手势）中的部分内容在第 8 章（图形、动画和声音）中使用，因此应按此顺序讲授。

以下是各章主题的摘要：

#### 第 1 章：Android 基础，第一个应用：Hello World

我们介绍如何使用 Android Studio 开发环境：如何使用模拟器、如何在设备上运行应用、如何输出到 `Logcat`、如何使用调试器。我们还介绍了与应用相关的各种资源：`AndroidManifest.xml` 文件、用于定义字符串、颜色和维度资源的各种 XML 文件，以及定义 GUI 的 XML 文件。

![](img/fm01fig02.jpg)

#### 第 2 章：模型-视图-控制器、GUI 组件、事件

我们解释了模型-视图-控制器架构，并使用 MVC 制作了第一个应用——小费计算器。我们使用 `RelativeLayout`、`TextView`、`EditText` 和 `Button` 定义了 GUI。我们解释了如何将应用中使用的各种样式与应用内容分离（类似于网页设计中的 CSS）。我们涵盖了事件处理：点击按钮和在软键盘上输入。

#### 第 3 章：以编程方式编写 GUI、布局管理器

继续 MVC 架构，我们解释了如何为井字棋应用以编程方式定义 GUI 并设置事件处理。我们介绍了如何使用内部类、布局参数和警告对话框。

![](img/fm01fig03.jpg)

#### 第 4 章：多个活动、活动间传递数据、转场、持久化数据

我们介绍了如何在应用中包含多个活动，并解释了如何在活动之间传递数据。我们探讨了活动的生命周期方法及其使用方式，特别是在包含多个活动的应用中。我们演示了如何在活动之间设置动画转场。我们更深入地探讨了 `RelativeLayout` 类以及 `TableLayout` 类。最后，我们展示了如何处理持久化数据。我们使用一个抵押贷款应用作为概念载体：第一个屏幕显示抵押贷款数据（包括月供），第二个屏幕允许用户编辑抵押贷款特征（金额、利率和年限）。

![](img/fm01fig04.jpg)

#### 第 5 章：菜单、SQLite

我们展示了如何在应用中包含菜单，以及如何使用 SQLite 处理持久化数据。在以编程方式生成 GUI 时，我们使用了 `ScrollView`。该应用是一个糖果店管理器，允许用户添加、更新和删除糖果，以及使用 `Toast` 类为顾客收银。

![](img/fm01fig05.jpg)

#### 第 6 章：管理设备方向

在本章中，我们展示了如何检测设备方向的变化，并探讨了多种编写 GUI 的方法，使应用在竖屏和横屏方向都能正常工作。具体来说，我们动态获取设备的尺寸，以便相应地调整 GUI 组件的大小和位置。本章没有有意义的应用，我们只是探讨了管理方向变化时 GUI 的各种方式。

#### 第 7 章：触摸与滑动

我们首先展示了如何检测和处理触摸或滑动事件。更一般地，我们还展示了如何检测和处理手势、单击或双击事件。我们使用触摸和手势处理构建了一个拼图游戏应用：用户可以通过触摸并移动拼图块来解谜。拼图颜色随机生成，当用户完成拼图时会收到反馈。

![](img/fm01fig06.jpg)

#### 第 8 章：图形、动画、声音与游戏

我们探讨了如何创建自定义视图、如何绘制形状和位图、如何通过动画化屏幕上的对象来创建游戏、处理事件以及播放声音。我们使用 `Timer` 和 `TimerTask` 类创建游戏循环，并以定义的频率更新游戏状态。在这个打鸭子应用中，一只鸭子以动画方式从屏幕右侧飞入，使用了四个 PNG 帧。用户可以通过触摸移动位于屏幕左下方的炮管来控制一门大炮（一个绘制的形状）。双击发射一颗子弹（一个绘制的形状），并检测与鸭子的碰撞。如果鸭子被击中，会播放声音，我们停止鸭子的动画，它垂直下落。

![](img/fm01fig07.jpg)

#### 第 9 章：片段

我们介绍了在活动中使用片段的各种方式、两个片段之间的通信，以及如何使片段可重用。该应用是一个刽子手游戏，其中各个片段包括游戏状态、游戏进度、剩余尝试次数，以及一个不可见片段。

![](img/fm01fig08.jpg)

#### 第 10 章：使用库及其 API：语音识别与地图

我们使用 Google 地图活动模板显示带有注释的地图，并使用语音识别来更改地图。我们还解释了如何使用 Google Play 服务。在这个应用中，用户可以通过说出城市名称（伦敦、巴黎、罗马或华盛顿特区）来显示以该城市为中心的地图，然后通过说出北、南、西或东来移动地图。

#### 第 11 章：使用 GPS 与位置服务

我们解释了如何使用 Google Play 服务，以及如何在应用中使用设备的 GPS。该应用管理到达目的地的剩余距离和时间，首先允许用户更新这些信息，最终实现定期自动更新。

![](img/fm01fig09.jpg)

#### 第 12 章：在应用内使用另一个应用：拍照、灰度化并发送邮件

我们解释了如何在应用内使用另一个应用（如相机应用）、如何将文件存储在外部存储中，以及如何在应用内使用邮件应用。我们还探讨了搜索条（滑块）。该应用打开相机应用，当用户拍照后，允许用户使用三个搜索条将图片灰度化。在模型中，我们解释了如何访问 `Bitmap` 的每个像素（包括读取和写入）。用户完成图片灰度化后，可以发送邮件给朋友，我们会自动附上灰度化后的图片。

![](img/fm01fig10.jpg)

#### 第 13 章：XML 与内容应用

我们使用 SAX 解析器解析本地和远程 XML 文档。我们展示了如何使用 `AsyncTask` 类在应用后台执行任务。我们在 `ListView` 中显示结果，并在应用内打开网页浏览器。该应用是一个内容应用，从远程 URL（http://blogs.jblearning.com/computer-science/feed/）检索数据，将其 XML 内容解析为 `ArrayList` 项，并在 `ListView` 中显示这些项。当用户点击其中一项时，我们会在浏览器中打开该项对应的 URL。

![](img/fm01fig11.jpg)

## 第 14 章：制作 Android 小部件

我们将介绍制作小部件的各个步骤：首先制作一个非常简单的静态小部件，然后使其动态化，接着从远程网站获取温度数据，最后让用户能够自定义小部件。我们从硬编码的城市和温度开始，然后为小部件添加样式，接着添加动态数据（从设备获取日期和时间），并允许用户通过点击小部件来更新数据。接下来，我们使用 `AsyncTask` 类从远程网站获取温度数据。数据以 `JSON` 字符串形式返回，因此我们访问 `JSON` 字符串中所需的数据（温度）并将其显示在小部件内。最后，我们通过允许用户设置要获取温度数据的城市和州，使小部件可自定义。

## 第 15 章：应用内广告

我们在一个简单的应用中放置 Google 广告，并解释 `AdView` 类的生命周期方法。我们还介绍了如何创建可绘制资源并将其用于按钮。在这个秒表应用中，我们创建了三个可绘制资源（`stop.xml`、`reset.xml` 和 `start.xml`），用作应用的按钮。我们在屏幕底部显示横幅广告，并展示如何获取虚假的远程 Google 广告来测试应用，以及如何使用真实的 Google 广告。无需注册为 Google 开发者即可请求 Google 提供的虚假广告。

## 第 16 章：安全与加密

我们解释对称加密和非对称加密，以及如何使用加密算法（`AES`）和非对称加密算法（`RSA`）。本章没有有意义的应用；主要目标是解释各种加密方案和算法，以及如何使用 Java 库中与加密相关的类和方法。

![](img/fm01fig12.jpg)

如果学生学完所有十六个章节，他们将创建以下应用：

- Hello Android（第 1 章）
- Tip Calculator（第 2 章）
- TicTacToe（第 3 章）
- Mortgage Calculator（第 4 章）
- Candy Store Manager（第 5 章）
- Puzzle Game（第 7 章）
- Duck Hunting Game（第 8 章）
- Hangman Game（第 9 章）
- Map Display Using Speech Input（第 10 章）
- Travel App Using the GPS（第 11 章）
- Photo Graying（第 12 章）
- Content App（第 13 章）
- Temperature Widget（第 14 章）
- StopWatch with Advertising（第 15 章）

## 附录

附录包括以下内容：

- ▸ 关于如何动态获取操作栏和状态栏高度的微章节（包含一个微型应用）：如果我们打算以编程方式编写 GUI 并使应用与设备无关，这一点很重要。
- ▸ 关于如何动态调整 `TextView` 内字体大小以使其完美适应一行的微章节（包含一个微型应用）：如果我们显示长度可能变化很大的动态数据，这一点很重要。
- ▸ 如何使用 `Google Play Services`：这对于涉及地图、GPS、广告和其他 Google 服务的应用很重要。
- ▸ 关于如何使用 `AsyncTask` 类的微章节（包含一个微型应用）：这对于从远程位置获取数据的应用很重要。

## 教师和学生资源

教师和学生资源可在 `go.jblearning.com/FranceschiAndroid` 下载。这些资源包括：

- ▸ 访问最新版本的 Android Studio
- ▸ 所有应用的源代码
- ▸ 章节末尾选择题和代码填空题的答案
- ▸ PowerPoint 格式的幻灯片
- ▸ 试题库，包括包含微型应用的期中考试和期末考试样题

## 联系作者

如果本文中发现错误，请通过 hjfranceschi@loyola.edu 联系作者。勘误表将发布在 Jones & Bartlett 目录页面上，网址为 `go.jblearning.com/FranceschiAndroid`。

## 致谢

我们感谢众多合作伙伴、同事和家庭成员对本书的贡献。

首先，我们要感谢我们的出版商 Jones & Bartlett Learning，特别是采编编辑 Laura Pagluica、副编辑 Taylor Ferracane、项目经理 Bharathi Sanjeev 和副制作编辑 Rebekah Linga。

其次，我们向审稿人表示感谢：

- Timothy E. Roden 博士  
  计算机科学副教授  
  德克萨斯州拉马尔大学

- Jeremy Blum 博士  
  计算机科学副教授  
  宾夕法尼亚州立大学哈里斯堡分校

- Jamie Pinchot 博士  
  计算机与信息系统副教授  
  罗伯特莫里斯大学

- Allan M. Hart 博士  
  助理教授  
  计算机信息科学  
  明尼苏达州立大学曼凯托分校

- Marwan Shaban 博士  
  兼职教授  
  中佛罗里达大学

- Georgia Brown 硕士  
  计算机科学系  
  北伊利诺伊大学

- Roy Kravitz  
  波特兰州立大学

- Sonia M. Arteaga 博士  
  哈特内尔学院

- Shane Schartz 博士  
  MIS、信息学助理教授  
  福特海斯州立大学

最后，我们感谢我的家人：我的妻子 Kristin、我的女儿 Héléna 和我的儿子 Louis，他们提供了支持、反馈和建议。

# 第一章：Android 基础，第一个应用：HelloAndroid

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

如今，几乎每个人都拥有智能手机并使用各种应用。这些应用可以查看电子邮件、查看天气、玩游戏、计算按揭付款、翻译语言、学习代数，甚至用于网站、社交媒体或新闻机构（如 Facebook、Twitter 或 CNN）。在本章中，我们将学习如何为 Android 设备开发第一个应用。

## 1.1 智能手机及其操作系统

### 1.1.1 智能手机

智能手机是一种智能蜂窝电话，或者说是一种内置计算机以及一些额外硬件的蜂窝电话。因此，程序员可以为它们编写应用软件；这种应用软件被称为 app。智能手机具备普通计算机的典型组件：CPU、内存、存储设备、操作系统以及其他设备，如摄像头、加速度计或 GPS。

最著名的两个操作系统是来自 Google 的 Android 操作系统和来自 Apple 的 iOS。其他流行的智能手机操作系统包括 BlackBerry、Windows 和 Symbian。全球每年销售的智能手机数量现已超过十亿部。此外，智能手机在销售的手机中所占比例越来越大。

### 1.1.2 Android 手机

目前有超过 100 种不同类型的 Android 手机或平板电脑。它们可能具有不同的 CPU、不同的屏幕分辨率以及不同的内存容量。这使得开发人员很难在实际设备上测试他们的应用。应用用户界面各个组件的尺寸可能因 Android 手机或平板电脑而异。此外，在速度至关重要的复杂游戏中，应用在老旧且速度较慢的 Android 设备上的运行方式可能与较新的设备不同。在开发面向 Android 市场的应用时，这一点需要牢记。

### 1.1.3 应用与 Google Play

Android 应用通过 Google Play（[`play.google.com`](https://play.google.com)）分发，该平台以前称为 Android Market。Google Play 实际上是一个数字内容商店，类似于 Apple 的 App Store，而不仅仅是应用商店。要在 Google Play 上分发应用，你需要注册成为开发者，费用为 25 美元。

目前 Google Play 上有超过一百万款应用，其中绝大多数是免费的。热门类别包括娱乐（游戏）、个性化、工具、书籍和参考。下载的应用大多是免费应用。还应注意，Android 操作系统是开放的，因此任何人都可以轻松地将应用从一个 Android 设备复制到另一个设备。对知识产权的保护很少。

## 1.2 Android 应用的开发环境

Android 应用的典型推荐开发环境包括以下内容：

- ▸ Java 开发工具包（JDK）



- ▸ Android Studio
- ▸ Android 标准开发工具包（Android SDK）

开发 Android 应用并不要求必须使用 Android Studio，我们可以通过命令行运行代码，或使用其他集成开发环境（如 Eclipse）。然而，Android Studio 是 Google 的官方开发环境，很可能迅速成为行业标准；本书将使用 Android Studio。

要搭建完整的 Android 应用开发环境，我们需要：

- ▸ 下载并安装最新的 Java SDK（如果尚未安装），可在[`www.oracle.com/technetwork/java/javase/downloads/index.html`](http://www.oracle.com/technetwork/java/javase/downloads/index.html)找到。
- ▸ 下载并安装 Android Studio，包括 IDE、SDK 工具和模拟器系统，可在[`developer.android.com/sdk/index.html`](http://developer.android.com/sdk/index.html)找到。

## 1.3 我们的第一个应用：HelloAndroid

让我们创建第一个 Android 应用。

### 1.3.1 骨架应用

打开 Android Studio。首次运行 Android Studio 时，环境会检查是否为最新版本，并在需要时提示下载组件。完成后，点击 Finish（参见图 1.1），我们将看到图 1.2 所示的屏幕。左侧列出了最近的项目；首次使用 Android Studio 时，这里不会有任何项目。要开始一个新项目，请点击“Start a new Android Studio project”。

在图 1.3 所示的对话框中，我们输入项目名称（我们选择`HelloAndroid`）和域名（我们选择`jblearning.com`；如果没有域名，可以选择任意名称）；其他两个字段（包名和项目位置）会自动填充。如果希望更改项目位置，可以编辑该字段。请注意，包名是域名倒序。开发人员通常以域名倒序命名包名；这确保了唯一性。完成后，点击 Next。

下一个对话框（图 1.4）用于指定该项目的最低 SDK；根据我们的应用，这一点可能很重要。例如，如果我们集成广告，可能需要比默认级别更高的 SDK 级别；然而，我们指定的 SDK 级别越新，对应用潜在用户数量的限制就越大。对于这个应用，我们保留默认的 SDK 级别，然后点击 Next。

![](img/9781284093650_CH01_FIGF01.jpg)

图 1.1 下载组件

![](img/9781284093650_CH01_FIGF02.jpg)

图 1.2 欢迎界面

![](img/9781284093650_CH01_FIGF03.jpg)

图 1.3 新建项目对话框

![](img/9781284093650_CH01_FIGF04.jpg)

图 1.4 指定最低 SDK 的对话框

在下一个对话框（图 1.5）中，我们可以从多个模板中选择；模板会创建带有一些预定义用户界面功能的骨架代码；通常，它提供的用户界面与原生应用中的界面类似。对于这个应用，我们选择 Empty Activity 模板——它会创建最简骨架代码。

![](img/9781284093650_CH01_FIGF05.jpg)

图 1.5 选择活动类型的对话框

![](img/9781284093650_CH01_FIGF06.jpg)

图 1.6 文件命名对话框

在下一个对话框（图 1.6）中，我们可以为第一个活动类和布局文件指定各种名称。对于这第一个应用，我们保留默认名称：类名为`MainActivity`，布局文件名为`activity_main`。点击 Finish 后，项目就创建完成了。

项目目录结构以及许多源文件已经创建，我们可以在 Android Studio 开发环境的左侧窗格中看到它们（如图 1.7 所示）。

![](img/9781284093650_CH01_FIGF07.jpg)

图 1.7 IDE 中的应用目录结构

程序会自动生成许多目录和文件。

- ▸ `manifests`目录包含`AndroidManifest.xml`文件，该文件自动生成且可编辑。它指定了该应用使用的资源，例如活动、文件系统、互联网、设备硬件资源等。当用户下载应用时，该文件会告知用户应用使用了哪些资源（例如，是否写入设备文件系统）。
- ▸ `java`目录包含 Java 源文件。随着应用变得复杂，我们可以添加更多 Java 源文件。
- ▸ `res`（`res`代表“资源”）目录包含资源，例如工具文件（用于定义字符串、菜单、布局、颜色、样式）以及图像、声音等。这些资源的 ID 会自动生成在名为`R.java`的文件中。`R.java`不应被修改。
- ▸ 在`res`目录内，`drawable`目录用于存放图像和其他可绘制资源。它可以包含 jpeg、png、gif、用于定义渐变效果的文件等。根据需要，我们可以向此目录添加资源。
- ▸ 在`res`目录内，`mipmap`目录包含应用的图标。根据需要，我们可以向此目录添加资源。
- ▸ 在`res`目录内，`layout`目录包含定义屏幕布局的 XML 文件。目前，它包含`activity_main.xml`文件，这是为我们的空活动自动生成的布局文件。我们可以编辑此文件来定义该应用的图形用户界面（GUI）。
- ▸ 在`res`目录内，`values`目录包含定义各种资源的 XML 文件，例如颜色（在`colors.xml`文件中）、尺寸（在`dimens.xml`文件中）、样式（在`styles.xml`文件中）或字符串（在`strings.xml`文件中）。我们可以编辑这些文件来定义更多的颜色、尺寸、样式或字符串资源。
- ▸ `gradle scripts`目录包含用于构建应用的脚本。

在本章中，我们将详细查看以下文件：`AndroidManifest.xml`、`MainActivity.java`、`dimens.xml`、`strings.xml`、`styles.xml`、`colors.xml`和`activity_main.xml`。我们还会为应用添加一个图标。

### 1.3.2 GUI 预览

Android Studio 的一个不错的功能是，它允许我们在不运行应用的情况下预览屏幕。需要选择一个布局文件才能显示预览。要选择`activity_main.xml`，我们双击该文件名。在菜单中，如果选择 View、Tool Windows、Preview，应用的预览就会显示在环境的右侧，如图 1.8 所示。这样，我们就可以在不运行应用的情况下编辑 GUI 并预览。我们可以通过从菜单中选择（图 1.9）来预览竖屏和横屏两种方向的屏幕。图 1.10 显示了横屏方向的预览。我们还可以通过点击 AppTheme 下拉列表（图 1.11）选择不同的主题来预览应用，并通过点击设备下拉列表（图 1.12）在多种设备之间进行选择。

### 1.3.3 XML 文件：`activity_main.xml`、`colors.xml`、`styles.xml`、`strings.xml`、`dimens.xml`

该应用的 GUI 定义在`activity_main.xml`文件中。注意，我们也可以通过代码来设置 GUI。

要打开`activity_main.xml`，我们点击`res`，然后点击`layout`，再双击`activity_main.xml`。为了查看实际的 XML 代码，我们可能需要点击面板底部的 Text 选项卡。

`Activity_main.xml`（如示例 1.1 所示）是一个可扩展标记语言（XML）文件。Android 开发环境广泛使用 XML，特别是用于定义应用各个屏幕的用户界面，以及定义各种资源，如字符串、尺寸、菜单、样式、形状或渐变效果。

我们可能已经熟悉超文本标记语言（HTML）及其语法。HTML 是 Web 浏览器使用的语言，具有固定的标签和属性集。XML 使用的语法与 HTML 基本相同，但我们可以创建自己的标签和属性。

![](img/9781284093650_CH01_FIGF08.jpg)

图 1.8 环境中的应用预览

![](img/9781284093650_CH01_FIGF09.jpg)

图 1.9 选择预览方向

![](img/9781284093650_CH01_FIGF10.jpg)

图 1.10 横屏方向的应用预览

![](img/9781284093650_CH01_FIGF11.jpg)

图 1.11 选择预览主题（选择 Holo Dark 后）

完整的 XML 文档可以在[`www.w3.org/XML/`](http://www.w3.org/XML/)找到。

接下来，我们将概述 XML 的主要特性。XML 文档由元素组成，每个元素可以有零个或多个属性/值对。元素可以嵌套。元素可以有内容，也可以没有。非空元素以开始标签开头，以结束标签结尾。开始标签和结束标签之间的文本称为元素内容。

虽然实际规范稍微复杂一些，但我们将使用以下简化语法来定义非空 XML 元素：

```xml
<tagName attribute1=”value1” attribute2=”value2” ... >
元素内容
</tagName>
```

以下是两个示例：

```xml
<price>46.00</price>
<app language=”Java” version=”7.0”>Hello Android</app>
```

如果元素没有内容，那么我们可以使用空元素标签，语法如下：

```xml
<tagName attribute1=”value1” attribute2=”value2” ... />
```

以下是两个示例：

```xml
<website name=”twitter”/>
<app language=”Java” version=”7.0”/>
```

![](img/9781284093650_CH01_FIGF12.jpg)

图 1.12 选择预览设备

标签的命名有规则：我们只使用以字母或下划线开头，后跟零个或多个字母、下划线或数字的标签名称。官方对标签名称的规范比上述更复杂，可以在[`www.w3.org/XML/Core/#Publications`](http://www.w3.org/XML/Core/#Publications)找到。

注释使用以下语法：

```xml
<!-- 在此处编写注释 -->
```

文件`activity_main.xml`定义了 GUI 的外观。`RelativeLayout`元素定义了各个图形元素将相对于彼此或它们的父图形容器进行定位和显示。

在`activity_main.xml`文件中，`RelativeLayout`元素使用了第一种语法，并包含属性`android:layout_width`和`android:layout_height`，两者的值均为`match_parent`（第 5–6 行）。这意味着`RelativeLayout`元素将与其父元素一样大，在此示例中父元素是屏幕。它还包含属性`android:paddingBottom`、`android:paddingLeft`、`android:paddingRight`和`android:paddingTop`（第 7–10 行）。`android:paddingBottom`元素的值为`@dimen/activity_vertical_margin`（第 7 行）：这意味着屏幕左侧将有一些内边距，其大小等于位于`res`目录下`values`目录中的`dimens.xml`文件中名为`activity_vertical_margin`的`dimen`元素的值（本例中为 16 px）。

通常，如果在名为`resource_types.xml`的资源文件中定义了一个名为`constant_name`的常量，我们可以使用语法`@resource_type/constant_name`来访问该常量的值。

第 13–16 行定义了一个嵌套在`RelativeLayout`元素内部的`TextView`元素；`TextView`元素是`TextView`类的一个实例，该类封装了一个标签。这个`TextView`元素是一个空元素，因此没有内容；它有三个属性/值对：

- ▸ 属性`android:layout_width`和`android:layout_height`的值为`wrap_content`（第 14 和 15 行）。这意味着`TextView`元素的宽度和高度刚好足以容纳其内容；该元素“包裹”在其内容周围。
- ▸ 属性`android:text`定义了`TextView`内显示的`String`；其值为`Hello World!`。

![](img/ch01exa01.jpg)

示例 1.1 `dimens.xml` 文件

`activity_horizonal_margin`和`activity_vertical_margin`值在`dimens.xml`文件（第 3–4 行）中的两个`dimen`元素内定义，如示例 1.2 所示。它们的值为 16 px。后缀`dp`代表密度像素，这意味着该值与设备无关。如果我们的应用需要根据屏幕尺寸使用不同的值，我们可以在`dimens.xml`文件中定义多个值，每个屏幕尺寸对应一个值。

在`dimens.xml`文件中，定义`dimen`资源的语法为：

![](img/ch01exa02.jpg)

示例 1.2 `dimens.xml` 文件

尝试像示例 1.3 那样修改`dimens.xml`。环境会更新其预览，如图 1.13 所示。

![](img/ch01exa03.jpg)

示例 1.3 修改后的 `dimens.xml` 文件

类似地，值为`HelloAndroid`的`String`（参见图 1.13 中应用的蓝色标题）定义在位于`res`目录下`values`目录中的`strings.xml`文件（示例 1.4）的第 2 行。我们可以在 Java 文件中创建`String`常量，但建议尽可能将`String`常量存储在`strings.xml`文件中。如果以后想要修改一个或多个`String`值，编辑该文件比编辑 Java 代码更容易。

在`strings.xml`文件中，定义`String`资源的语法为：

```xml
<string name=”stringName”>valueOfString</string>
```

![](img/ch01exa04.jpg)

示例 1.4 `strings.xml` 文件

尝试像示例 1.5 那样修改`strings.xml`。环境会更新其预览，如图 1.14 所示。`String` `app_name`在`AndroidManifest.xml`文件中使用，这将在第 1.7 节中解释。

![](img/9781284093650_CH01_FIGF13.jpg)

图 1.13 更新`dimens.xml`文件后环境中应用的预览

![](img/9781284093650_CH01_FIGF14.jpg)

图 1.14 更新`strings.xml`文件后环境中应用的预览

![](img/ch01exa05.jpg)

示例 1.5 修改后的 `strings.xml` 文件

位于`res`目录下`values`目录中的`styles.xml`文件定义了应用中使用的各种样式。示例 1.6 显示了其自动生成的内容。

在`styles.xml`文件中，我们可以通过使用以下语法添加一个`item`元素来修改样式：

```xml
<item name=”styleAttribute”>valueOfItem</item>
```

指定`TextView`内文本大小的样式属性名称为`android:-textSize`。在示例 11.7 中，我们在第 6 行将默认文本大小更改为 40。环境会更新其预览，如图 1.15 所示。

![](img/ch01exa06.jpg)

示例 1.6 `styles.xml` 文件

![](img/ch01exa07.jpg)

示例 1.7 修改后的 `styles.xml` 文件

请注意，`styles.xml`中定义的样式包含三个颜色常量，使用语法`@color/color_name`。这些常量定义在`colors.xml`文件中，如示例 1.8 所示，该文件也位于`res`目录下的`values`目录中。其内容是自动生成的。在`colors.xml`文件中，定义`color`资源的语法为：

```xml
<color name=”colorName”>valueOfColor</color>
```

![](img/ch01exa08.jpg)

示例 1.8 `colors.xml` 文件

![](img/9781284093650_CH01_FIGF15.jpg)

图 1.15 更新`styles.xml`文件后环境中应用的预览

![](img/9781284093650_CH01_FIGF16.jpg)

图 1.16 更新`colors.xml`文件后环境中应用的预览

颜色值使用语法`æRRGGBB`定义，其中`R`、`G`、`B`是十六进制数字，分别代表红色、蓝色和绿色的量。

如果我们将名为`colorPrimary`的颜色值修改为`æFF0000`（纯红色），预览将更新，如图 1.16 所示。

### 1.3.4 `MainActivity` 类

我们应用的入口点是`MainActivity`类，其名称由`Main`和`Activity`组成。它位于`java`目录下的`com.jblearning.helloandroid`包中（如示例 1.9 所示）。



Android 应用的源代码使用 Java 语法。第 1 行是包声明。创建此项目时，我们告诉 Android Studio 将代码放在`com.jblearning.helloandroid`包中。第 3–4 行导入了此类中使用的类。我们需要导入`AppCompatActivity`，因为`MainActivity`扩展了它（第 6 行），从而继承自它。`AppCompatActivity`继承（间接地）自`Activity`类，并在活动屏幕上方包含一个操作栏（图 1.16 中为红色），应用标题显示在其中。

活动是一个提供并控制用户可与之交互的屏幕的组件。一个应用可以由多个活动组成，它们之间可能传递数据。活动在栈（一种后进先出的数据结构）上进行管理。要创建一个活动，我们必须继承`Activity`或其子类，就像自动生成的`MainActivity`骨架代码中所做的那样。当活动启动、停止、恢复或销毁时，系统会自动调用`Activity`类的某些方法。

![](img/ch01exa09.jpg)

示例 1.9 `MainActivity`类

`onCreate`方法（第 8-12 行）在活动启动时自动调用。我们应该重写此方法，并在需要时在该方法内创建活动的组件。在第 10 行，我们通过`AppCompatActivity`调用从`Activity`继承的`onCreate`方法。在第 11 行，我们通过调用`setContentView`方法定义应用的布局，如表 1.1 所示。布局定义在`activity_main.xml`文件中。`setContentView`方法的参数是一个整数，表示定义屏幕布局的布局资源的 ID。资源的 ID 可以在`app/build/generated/source/r/debug/com/jblearning/helloandroid`目录下的`R.java`文件中找到。`R`类包含许多内部类：`anim`、`attr`、`bool`、`color`、`dimen`、`drawable`、`id`、`integer`、`layout`、`menu`、`string`、`style`、`styleable`。每个内部类都是`public`和`static`的，并包含一个或多个`int`常量。每个`int`常量可通过以下语法访问：

```java
R.className.constantName
```

`activity_main`常量（`activity_main.xml`文件的 ID，一个布局资源）定义在`R`类内部的`layout`类中。因此，可以使用`R.layout.activity_main`来引用它。调用`setContentView`并传入一个表示布局 XML 文件的整数参数（本例中为`R.layout.activity_main`）称为“填充 XML”。

| 方法 | 描述 |
| --- | --- |
| `void setContentView( View view )` | 将此 Activity 的内容设置为`view` |
| `void setContentView( int layoutResID )` | 使用 ID 为`layoutResID`的资源设置此 Activity 的内容，该资源将被填充 |

表 1.1 `Activity`类中选定的`setContentView`方法

## 1.4 在模拟器中运行应用

Android Studio 包含一个模拟器，因此我们可以在设备上测试应用之前，先在环境中运行和测试应用。我们首先在模拟器中运行应用。为了使模拟器正常工作，我们可能需要做三件事：

- ▸ 如果需要，在 BIOS 菜单中启用虚拟化扩展（如果它被禁用；注意它可能默认已启用）。启动计算机时，我们需要中断启动过程，访问系统的 BIOS 菜单，并启用虚拟化。如果计算机不支持虚拟化，模拟器很可能无法工作。
- ▸ 如果需要，下载、安装并运行 Intel 硬件加速执行管理器（HAXM）。在我们下载 Android Studio 后，它可能已经存在于计算机上。也可能需要更新。文件名应为`intelhaxm-android.exe`。
- ▸ 关闭并重新启动 Android Studio。

大多数（如果不是全部）较新的计算机都支持虚拟化。

模拟器运行在 Android 虚拟设备（AVD）中。我们可以使用 AVD 管理器创建 AVD。要打开 AVD 管理器，选择“窗口”、“AVD 管理器”，或单击 AVD 管理器图标，如图 1.17 所示。这将打开 AVD 管理器，如图 1.18 所示。要创建新的 AVD，我们单击“+ 创建虚拟设备...”按钮。这将打开一个新面板（图 1.19），允许我们从预制的 AVD 列表中选择。从列表中选择一个并单击“下一步”后，它会显示在一个新面板中（图 1.20）。我们选择所需的版本并单击“下一步”。AVD 的特性会显示出来，如图 1.21 所示。如果需要，我们可以编辑它们；特别是，如果我们想更改 AVD 的分辨率（从而改变模拟器的大小），可以编辑“缩放”属性。单击“完成”后，新的 AVD 已添加，如图 1.22 所示。

![](img/9781284093650_CH01_FIGF17.jpg)

图 1.17 AVD 管理器图标

![](img/9781284093650_CH01_FIGF18.jpg)

图 1.18 首次打开 AVD 管理器

![](img/9781284093650_CH01_FIGF19.jpg)

图 1.19 选择新的 AVD

![](img/9781284093650_CH01_FIGF20.jpg)

图 1.20 选择 AVD 后

![](img/9781284093650_CH01_FIGF21.jpg)

图 1.21 所选 AVD 的特性

![](img/9781284093650_CH01_FIGF22.jpg)

图 1.22 AVD 管理器显示更新后的 AVD 列表

要运行应用，请单击图标栏中的“运行”图标，如图 1.23 所示。

将打开一个对话框（图 1.24），我们从列表中选择要使用的 AVD；然后单击“确定”。我们也可以通过单击“创建新模拟器”按钮访问 AVD 管理器。请注意，如果模拟器已在运行，或者实际设备已连接到计算机，它将显示在“已连接设备”下的面板中。几分钟后，应用应在模拟器中运行。为了节省时间，我们建议只要 Android Studio 打开，就保持模拟器打开。

![](img/9781284093650_CH01_FIGF23.jpg)

图 1.23 运行配置对话框

![](img/9781284093650_CH01_FIGF24.jpg)

图 1.24 单击“运行”图标后的部署目标对话框

![](img/9781284093650_CH01_FIGF25A.jpg) ![](img/9781284093650_CH01_FIGF25B.jpg)

图 1.25 运行 HelloAndroid 应用的模拟器

![](img/9781284093650_CH01_FIGF26.jpg)

图 1.26 模拟器的工具栏，显示旋转工具

图 1.25 显示了在模拟器中运行的应用。默认情况下，模拟器以垂直方向（也称为竖屏）运行。其右侧包含一个工具栏，使我们能够控制其某些功能。特别是，我们可以使用图 1.26 所示的工具旋转模拟器。我们也可以按`Ctrl+F11`将模拟器旋转到水平方向（即横屏）（见图 1.27；注意此截图中未包含工具栏）。`Ctrl+F12`将模拟器恢复为垂直方向。我们可以通过单击模拟器框架顶部的白色部分并拖动来移动模拟器。表 1.2 总结了关于模拟器的有用信息。

Android Studio 一个有趣的新功能是“即时运行”。使用即时运行，我们可以修改应用的某些选定组件（例如`strings.xml`文件），单击“运行”图标，模拟器会自动即时更新应用。即时运行默认启用。如果我们想禁用它，可以选择“文件”、“设置”，然后在“构建、执行、部署”部分中选择“即时运行”，然后进行编辑，如图 1.28 所示。如果我们不想使用即时运行，可以取消选中它，并勾选“代码更改时重新启动活动”。

![](img/9781284093650_CH01_FIGF27.jpg)

图 1.27 以水平方向运行 HelloAndroid 应用的模拟器

| 描述 | 作用 |
| --- | --- |
| 在 BIOS 中启用虚拟化（如有必要） | 使模拟器能够运行 |
| 安装并运行 HAXM 可执行文件（如有必要） | 使模拟器能够运行 |
| `Ctrl+F11` 和`Ctrl+F12` | 旋转模拟器 |
| 工具栏 | 控制模拟器的功能 |

表 1.2 关于模拟器的有用信息

![](img/9781284093650_CH01_FIGF28.jpg)

图 1.28 显示即时运行功能的设置面板

## 1.5 使用 Logcat 调试应用

就像常规的 Java 程序一样，我们可以向控制台发送输出，这对于调试非常有用。为此，我们可以使用表 1.3 中所示的`Log`类的`static`方法之一。`Log`类属于`android.util`包。在开发过程中，这非常有用，可以在测试应用时为我们提供有关各种对象和变量的反馈。如果我们点击 Logcat 选项卡，日志语句的输出将显示在下方面板中（点击屏幕底部的 Android 选项卡以打开该面板），如图 1.29 所示。如果 Logcat 选项卡没有显示，我们应该先以调试模式运行应用，以强制其显示。要以调试模式运行应用，请点击调试按钮（带有 bug 图标的按钮，位于运行按钮的右侧），如图 1.23 所示。在应用的最终版本中，日志语句应被注释掉。

这些方法的主要区别在于其输出的详细程度。从最详细到最不详细，顺序为：`v`、`d`、`i`、`w`、`e`。

Logcat 中可能会有大量输出。我们可以通过使用过滤器来过滤 Logcat 中的输出，使其只显示我们选择的应用输出。要设置过滤器，请点击左下方面板右上角的下拉列表；选择“编辑过滤器配置”（如图 1.30 右侧所示）。在图 1.31 所示的对话框中，为过滤器指定一个标签。我们选择`MainActivity`：这样，它就能识别出该输出是由`MainActivity`类中的某些代码生成的。当使用`Log`类的方法输出数据时，我们将`MainActivity`作为这些方法的第一个参数（标签）。反过来，当我们运行应用时，如果选择名为`MainActivity`的过滤器，如图 1.32 所示，我们就只能看到标记为`MainActivity`的输出。

| 方法 | 描述 |
| --- | --- |
| `static int d( String tag, String msg )` | 此方法发送一条调试消息；`tag`标识日志消息的来源；可用于在 Logcat 中过滤消息。 |
| `static int e( String tag, String msg )` | 此方法发送一条错误消息。 |
| `static int i( String tag, String msg )` | 此方法发送一条信息消息。 |
| `static int v( String tag, String msg )` | 此方法发送一条详细消息。 |
| `static int w( String tag, String msg )` | 此方法发送一条警告消息。 |

表 1.3 `Log`类的部分方法

![](img/9781284093650_CH01_FIGF29.jpg)

图 1.29 下方面板——已选中 Logcat 选项卡和 MainActivity 过滤器

示例 1.10 展示了更新后的`MainActivity`类，其中包含一条反馈输出语句。第 5 行导入了`Log`类。我们在第 8 行声明了一个名为`MA`的常量，用于存储字符串`MainActivity`。第 14 行的输出语句使用`MA`作为其标签，并输出资源`R.layout.activity_main`的值。

![](img/9781284093650_CH01_FIGF30.jpg)

图 1.30 打开 Logcat 过滤器对话框

![](img/9781284093650_CH01_FIGF31.jpg)

图 1.31 设置 Logcat 过滤器

当我们运行应用时，可以在图 1.29 中看到输出语句的结果。如图所示，Logcat 选项卡已被选中（左上角），`MainActivity`过滤器也被选中（右上角）。我们可以验证资源`R.layout.activity_main`的 ID（2130968601）是否与`R.java`文件中找到的值（十六进制数`0x7f040019`）匹配。

![](img/9781284093650_CH01_FIGF32.jpg)

图 1.32 选择 MainActivity 过滤器

![](img/ch01exa10.jpg)

示例 1.10 修改后的`MainActivity`类，HelloAndroid，版本 1

与编程一样，我们可能会遇到编译错误、运行时错误和逻辑错误。默认情况下，Android Studio 会在我们输入时编译代码。它会在代码的右侧边缘用红色小线标记编译错误，用橙色小线标记警告；同时会在错误位置显示红色波浪线。例如，如果我们忘记在第 14 行末尾添加分号，Android Studio 会像图 1.33 所示那样标记错误。如果将鼠标悬停在右侧边缘的红线或红色波浪线上，我们会看到一条或多条建议，帮助我们纠正错误。在这种情况下，我们会看到：

```text
';' expected
```

![](img/9781284093650_CH01_FIGF33.jpg)

图 1.33 Android Studio 标记的编译错误

Android Studio 包含许多功能，可以改善程序员的体验，通过自动生成代码节省时间并防止错误。以下是其中一些功能：

- ▸ 当我们输入双引号时，它会自动添加另一个双引号来闭合；此外，如果我们自己闭合它，它会自动删除多余的双引号。
- ▸ 如果我们使用尚未导入的类，它会为该类添加下划线，并建议通过键入`Alt+Enter`来导入，从而节省我们的时间。
- ▸ 如果我们键入一个对象引用，然后键入一个点，它会建议我们可以调用的对象类的方法，并在我们键入时更新和限制列表。

## 1.6 使用调试器

除了 Logcat，Android Studio 还包含传统的调试工具，例如设置断点、检查变量或表达式的值、逐行单步执行代码、检查对象内存分配、截取屏幕截图和视频。在本节中，我们将学习如何设置断点以及检查变量的值。

要设置断点，我们点击语句的左侧——会出现一个橙色实心圆。图 1.34 显示我们设置了两个断点。

要以调试模式运行应用，我们点击工具栏上的调试图标，如图 1.23 所示。应用运行并在第一个断点处停止。调试器选项卡在屏幕底部的面板中被选中，我们可以看到一些调试信息和工具。在“帧”下，我们可以看到当前正在执行的代码位置。在“变量”下，我们可以检查各个变量的值，例如`MA`，其值为`MainActivity`。要恢复应用，我们点击面板左上角的绿色“恢复”图标，如图 1.35 所示。

![](img/9781284093650_CH01_FIGF34.jpg)

图 1.34 代码中的断点

![](img/9781284093650_CH01_FIGF35.jpg)

图 1.35 在第一个断点处停止后

![](img/9781284093650_CH01_FIGF36.jpg)

图 1.36 代码中的断点

![](img/9781284093650_CH01_FIGF37.jpg)

图 1.37 管理要监视的变量列表

当我们恢复、在断点处停止并多次恢复应用时，应用中各个变量的值会显示在“变量”下。图 1.36 显示此时`count`和`i`的值均为`2`。

如果“变量”下显示的变量太多，而我们只想查看其中几个，我们可以在右下方面板的“监视”下创建一个变量列表。我们点击 + 号向列表中添加变量，点击 - 号从列表中移除变量。图 1.37 显示了将`count`添加到监视变量列表后的值。

## 1.7 在真实设备上测试应用

为了在 Android 设备上测试我们的应用，我们需要：

- ▸ 下载 Android 设备的驱动程序。
- ▸ 将 Android 设备连接到计算机。

Android 设备的驱动程序可以从设备制造商的网站下载。例如，对于三星的 Android 设备，其网站为[`www.samsung.com/us/support/downloads#`](http://www.samsung.com/us/support/downloads#)。

![](img/9781284093650_CH01_FIGF38.jpg)

图 1.38 设备名称和 API 级别

![](img/9781284093650_CH01_FIGF39.jpg)

图 1.39 选择设备对话框

完成上述操作后，Android Studio 会检测到已连接的设备，并在下方面板左上角显示其名称和 API 级别（假设下方面板已打开，即选中了“Android”选项卡），如图 1.38 所示。我们使用的是三星 Galaxy Tab 2 7.0 平板电脑。

点击“运行”或“调试”按钮后，会弹出一个对话框（图 1.39）。该设备会出现在可运行的设备或模拟器列表中。选择该设备并点击“确定”。几秒钟后，应用就会在设备上运行（并安装）。在实际设备上测试应用比使用模拟器更简单、更快捷。图 1.40 展示了应用在平板电脑上运行的情况。请注意，如果我们有输出语句，仍然可以在 Logcat 中看到输出。

![](img/9781284093650_CH01_FIGF40.jpg)

图 1.40 在平板电脑中运行的 HelloAndroid 应用

## 1.8 应用清单与 Gradle 构建系统

### 1.8.1 AndroidManifest.xml 文件：应用图标与设备方向



`AndroidManifest.xml` 文件位于 `manifests` 目录中，它指定了应用所使用的资源，例如活动、文件系统、互联网和硬件资源。用户在 Google Play 下载应用之前，会被告知这些信息。示例 1.11 展示了 `AndroidManifest.xml` 的自动生成版本。其中，它定义了图标（第 7 行）以及应用的标签或标题（第 8 行）。标签内的文本是在 `strings.xml` 中定义的 `app_name` 字符串。

我们应该为应用提供一个启动器图标。这是应用在主屏幕或应用屏幕上的视觉表示。移动设备的启动器图标应为 48 × 48 dp。不同设备可能具有不同的屏幕密度，因此我们可以提供多个启动器图标，每种密度一个。在这样做时，应遵循从中等密度（2）到超高密度（8）之间 2/3/4/6/8 的缩放比例。如果我们只提供一个图标，Android Studio 会使用该图标并根据需要扩展其密度。表 1.4 展示了使用该规则时可能的尺寸示例。如果我们打算发布应用，则应提供一个 512 × 512 的启动器图标用于在 Google Play 中显示。更多信息请访问 [`www.google.com/design/spec/style/icons.html`](https://www.google.com/design/spec/style/icons.html)。图 1.41 展示了在添加了一个名为 `hi.png`（尺寸为 48 × 48）的文件后的 `mipmap` 目录。

![](img/ch01exa11.jpg)

示例 1.11 `AndroidManifest.xml` 文件

要将应用的启动图标设置为 `hi.png`，我们需要在 `AndroidManifest.xml` 文件的 `application` 元素中，将 `android:icon` 属性赋值为字符串 `@mipmap/hi`。`@mipmap/hi` 表达式定义了 `res` 目录下 `mipmap` 目录中名称为 `hi` 的资源（注意，我们不包含扩展名）。示例 1.11 的第 7 行变为：

| 密度 | 中等 | 高 | 超高 | 超超高 | 超超超高 |
| --- | --- | --- | --- | --- | --- |
| 缩放比例 | 2 | 3 | 4 | 6 | 8 |
| 每英寸点数 | 160 dpi | 240 dpi | 320 dpi | 480 dpi | 640 dpi |
| 尺寸 | 48 × 48 px | 72 × 72 px | 96 × 96 px | 144 × 144 px | 192 × 192 px |

表 1.4 启动器图标比例及可能尺寸

![](img/9781284093650_CH01_FIGF41.jpg)

图 1.41 `mipmap` 目录中的 `hi.png` 文件

```xml
android:icon="@mipmap/hi"
```

我们需要考虑的一点是，有些用户会以竖屏（纵向）方向使用应用，而另一些用户则会以横屏（横向）方向使用。应用的默认行为是随着用户旋转设备而旋转屏幕，因此我们当前的应用在两种方向下都能工作。图 1.42 展示了应用在平板电脑中以横屏方向运行的情况。随着应用变得复杂，这会成为一个重要问题。在本书后面，我们将讨论管理方向的替代方案和策略。有时，我们希望应用仅在一种方向下运行，例如竖屏，因此我们不希望应用在用户旋转设备时旋转。在 `activity` 元素内部，我们可以添加 `android:screenOrientation` 属性，并将其值指定为 `portrait` 或 `landscape`。例如，如果我们希望应用仅在竖屏方向下运行，可以添加：

```xml
android:screenOrientation="portrait"
```

请注意，我们可以按活动（activity）来控制应用的行为。在这个应用中只有一个活动，但可能有多个。示例 1.12 展示了更新后的 `AndroidManifest.xml` 文件。如果我们在设备上运行该应用，屏幕不会随着设备旋转而旋转；它会保持竖屏方向。图 1.43 展示了模拟器中的应用图标（位于原生应用之中）。

![](img/ch01exa12.jpg)

示例 1.12 修改后的 `AndroidManifest.xml` 文件

![](img/9781284093650_CH01_FIGF42.jpg)

图 1.42 在平板电脑中以横屏方向运行的 HelloAndroid 应用

![](img/9781284093650_CH01_FIGF43.jpg)

图 1.43 显示应用图标的模拟器屏幕

### 1.8.2 Gradle 构建系统

Android 应用程序包（APK）是用于分发在 Android 操作系统上运行的应用程序的文件格式。文件扩展名为 `.apk`。要创建 `apk` 文件，需要编译项目并将其各个部分打包到 `apk` 文件中。在撰写本文时，`apk` 文件可以在 `projectName/app/build/outputs/apk` 目录中找到。

`Apk` 文件是使用 `Gradle` 构建系统构建的，该系统已集成到 Android Studio 环境中。当我们启动一个应用时，`Gradle` 构建脚本会自动创建。这些脚本可以被修改，以构建需要自定义构建的应用，例如：

- 自定义构建过程。
- 为应用创建多个 `apk`，每个 `apk` 具有不同的功能，使用项目的资源。例如，可以为不同的受众制作不同的版本（付费版与免费版、消费者版与企业版）。

## 章节总结

- Android Studio 是 Android 应用的官方开发环境。
- 除了 JDK 之外，还可以使用 Android SDK 进行开发。
- Android Studio 是免费的，可从 Google 获取。
- Android 开发使用 XML 文件来定义图形用户界面（GUI）、字符串、样式、尺寸等。
- `res` 目录存储了部分应用资源，例如 `layout` 目录中的 `activity_main.xml`，以及 `values` 目录中的 `strings.xml`、`styles.xml`、`colors.xml` 和 `dimens.xml`。
- 布局和 GUI 可以在 XML 文件中定义；默认的起始文件是 `activity_main.xml`。
- 字符串可以在 `strings.xml` 文件中定义。
- 样式可以在 `styles.xml` 文件中定义。
- 尺寸可以在 `dimens.xml` 文件中定义。
- 颜色可以在 `colors.xml` 文件中定义。
- `R.java` 类是自动生成的，用于存储各种应用资源的 ID。
- Android Studio 包含一个预览模式，可以显示布局 XML 文件的 GUI。
- 活动（Activity）是一个组件，它提供一个用户可与之交互的屏幕。
- 一个应用可以由多个活动组成，这些活动之间可以相互传递数据。
- 活动在栈（后进先出数据结构）中进行管理。
- 要创建一个活动，我们需要继承 `Activity` 类或 `Activity` 类的现有子类。
- 当活动启动时，`Activity` 类（入口点）的 `onCreate` 方法会被自动调用。
- 我们通过调用 `setContentView` 方法来为活动指定视图。
- 一个应用包含一个清单文件 `AndroidManifest.xml`，它定义了应用所使用的资源。
- 模拟器使我们能够模拟应用在不同设备上的运行情况。
- 我们可以在模拟器或真实设备上测试应用。
- Instant Run 功能使我们能够修改应用的各个组件，并在模拟器中无需从头重启应用即可运行。
- 当应用准备好安装时，它会被打包成一个扩展名为 `.apk` 的文件，即应用的 `apk` 文件。
- `Gradle` 是 Android 应用的构建系统。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. AVD 代表什么？
   - Android Validator
   - Android Virtual Device
   - Android Valid Device
   - Android Viral device

2. XML 代表什么？
   - eXtended Mega Language
   - eXtended Multi Language
   - eXtensible Markup Language
   - eXtensible Mega Language

3. 判断以下 XML 片段是否有效：
   - `<a>hello</a>`
   - `</b>Hello<b>`
   - `<c digit=”6”></c>`
   - `<d>He there</e>`
   - `<f letter='Z”/>`
   - `<1 digit=”8”>one</1>`
   - `<g digit1=”1” digit2=”2”></g>`
   - `<h><i name=”Chris”></i></h>`
   - `<j><k name=”Jane”></j>`
   - `<l><m name=”Mary”></l></m>`

4. 以下 XML 片段在 `strings.xml` 中定义的字符串名称是什么？

   ```xml
   <string name=”abc”>Hello</string>
   ```

   - `string`
   - `name`
   - `abc`
   - `Hello`

5. 以下 XML 片段在 `strings.xml` 中定义的字符串值是什么？

   ```xml
   <string name=”abc”>Hello</string>
   ```

   - `string`
   - `name`
   - `abc`
   - `Hello`

6. 以下 XML 片段在 `activity_main.xml` 中定义的 `TextView` 组件将显示什么文本？

   ```xml
   <TextView
      android:layout_width=”match_parent”
      android:layout_height=”wrap_content”
      android:text=”@string/hi” />
   ```

   - `@string/hi`
   - `hi`
   - `strings.xml` 中名为 `hi` 的字符串的值
   - `android:text`

7. `AppCompatActivity` 类位于哪个包中？

   - `android.app.Activity`
   - `android.app`
   - `android.Activity`
   - `android.support.v7.app`

8. `AppCompatActivity` 类是 `Activity` 类的子类吗？

   - `true`
   - `false`

### 补全代码

9. 在以下 `activity_main.xml` 的 XML 片段中，添加一行 XML，使文本字段中显示的文本是字符串 `book` 的值（假设字符串 `book` 已在 `strings.xml` 中定义）。

   ```xml
   <TextView
      android:layout_width=”fill_parent”
      android:layout_height=”wrap_content”
   />
   ```

10. 在 `onCreate` 方法中，补全代码，以便设置 `activity_main.xml` 中定义的布局和 GUI。

    ```java
    public void onCreate( Bundle savedInstanceState ){
          super.onCreate(savedInstanceState);
          // 你的代码写在这里
    }
    ```

### 编写一个应用

11. 编写一个显示“I like Android”的应用。

12. 编写一个仅在横屏模式下运行的应用。它在屏幕左上角显示“This is fun!”，且顶部和左侧均无外边距。

# 第二章：模型-视图-控制器、GUI 组件、事件

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

优秀的应用提供有用的功能和易于使用的界面。用户界面由各种图形用户界面（GUI）组件组成，通常等待用户交互。其中一些 GUI 组件允许用户输入，例如点击按钮、从键盘输入数据、从列表中选择项目、滚动滚轮等。这些用户交互被称为事件。当事件发生时，应用处理该事件并更新屏幕；这被称为事件处理。在本章中，我们将学习各种 GUI 组件、它们关联的事件，以及如何处理这些组件上的事件。我们还将学习如何设置这些组件的样式和外观。之后，我们将学习如何使用布局管理器更好地在屏幕上排列这些组件。

## 2.1 模型-视图-控制器架构

之前，我们创建了第一个应用，它包含两个部分：

- `activity_main.xml`，定义了 GUI：这被称为应用的视图部分。
- `MainActivity` 类，它显示 GUI（更一般地说，`Activity` 类管理 GUI）；这被称为应用的控制器部分。

我们的第一个应用只显示了一个标签，因此它没有任何功能；应用的功能被称为模型。

将这三个部分（模型、视图和控制器）分离是一种良好的设计实践。它使应用在后续的设计、编码、维护和修改中更加容易。我们还可以重用应用的某些部分，例如模型，来制作另一个应用。

在本章中，我们将使用模型-视图-控制器架构制作一个简单的小费计算器应用；为此，我们需要编写三个重要文件：

- `TipCalculator.java`：`TipCalculator` 类封装了小费计算器的功能；这个类是应用的模型。
- `activity_main.xml`：这个文件定义了应用的视图。
- `MainActivity.java`：这个类是应用的控制器。

小费计算器的功能由什么组成？我们将模型保持最小化，以便更多地关注视图和控制器。我们的最小模型配置包括账单金额、小费百分比，以及两个计算小费和总账单的方法。视图镜像模型，并包含四个 GUI 组件来显示模型中指定的数据。

控制器是视图和模型之间的中间人。当用户在视图中输入数据时——例如，更改小费百分比——控制器要求模型执行一些计算，然后相应地更新视图。

更一般地，我们可以使用模型-视图-控制器-存储架构。当我们需要持久化数据时，这很有用；我们可以在存储中存储和检索数据。

模型通常是简单的 Java 代码，不包含任何与 GUI 相关的代码。通常，从模型开始是一个好主意。

| 构造方法 | |
| --- | --- |
| `TipCalculator` | `TipCalculator(float newTip, float newBill)` 构造一个 `TipCalculator` 对象 |
| 方法 | |
| 返回值 | 方法名和参数列表 |
| `float` | `getTip()` |
| `float` | `getBill()` |
| `void` | `setTip(float)` |
| `void` | `setBill(float)` |
| `float` | `tipAmount()` |
| `float` | `totalAmount()` |

表 2.1 `TipCalculator` 类的 API

## 2.2 模型

我们启动一个新的 Android Studio 项目，将其命名为 `TipCalculatorV0`，并选择 Empty Activity 模板。

模型封装了小费计算器的功能。模型应该是平台无关的。它的编码方式应使其不仅可用于构建此移动应用或其他移动应用，还可用于桌面应用甚至互联网网站。

对于这个应用，模型很简单，只包含一个封装了小费计算器的类，即 `TipCalculator` 类。它是一个普通的 Java 类。实际上，我们甚至可以在 Android 开发环境之外编写这个类，并在将其引入项目之前进行测试。我们选择将这个类放在项目的 Java 目录下的 `com.jblearning.tipcalculatorv0` 包（和目录）中。我们选中该目录，然后选择 File → New → Java Class，输入类名，点击 OK。类的骨架就出现了。表 2.1 展示了 `TipCalculator` 类的 API。

示例 2.1 展示了类的代码。为了编写 `TipCalculator` 类以及一般的模型，我们不需要了解任何 Android 编程知识。此外，我们可以用一个简单的 Java 程序来测试模型，该程序测试类的所有方法；这留作练习。本例中只有一个类，但通常模型可以包含多个类，并可以放在自己的目录中。这个应用最有用的方法是构造函数（第 7–10 行）、`tipAmount`（第 30–32 行）和 `totalAmount`（第 34–36 行）方法。

## 2.3 GUI 组件

现在我们将注意力转向视图以及 Android 开发环境在设计 GUI 方面的能力。

![](img/ch02exa01.jpg)

示例 2.1 `TipCalculator` 类

在本章中，我们使用 `activity_main.xml` 文件来创建和定义显示在屏幕上的 GUI 组件。我们也可以完全通过代码来定义和操作 GUI 组件，这将在本书后面进行。



GUI 组件是具有图形表示的对象；它们也被称为小部件。术语 `widget` 对于 Android 用户还有另一个含义——它指的是显示在 Android 主屏幕或锁屏上并运行的小型应用，通常显示应用最相关的信息。GUI 组件可以：

- ▸ 显示信息
- ▸ 从用户处收集数据，以及
- ▸ 允许用户与之交互并触发对方法的调用。

Android 提供了大量的类来封装各种 GUI 组件。表 2.2 列出了其中一些。

许多 GUI 组件共享一些功能，并相互继承。图 2.1 总结了其中一些组件的继承层次结构。

`View` 代表了 GUI 组件的基本构建块；`View` 类位于 `android.view` 包中。它占据屏幕上的一个矩形区域，可绘制，并能响应事件。`View` 是按钮、复选框和列表等 GUI 组件的超类。`ViewGroup` 是布局类的超类，也位于 `android.view` 包中；布局是不可见的容器，可以包含其他 `View` 或其他 `ViewGroup`。图 2.1 中显示的大多数其他类，如 `ImageView`、`TextView`、`Button`、`EditText`、`CompoundButton`、`AutoCompleteTextView`、`Checkbox`、`RadioButton`、`Switch` 和 `ToggleButton`，都位于 `android.widget` 包中。`KeyboardView` 位于 `android.inputmethodservice` 包中。

| GUI 组件类型 | 类 | 描述 |
| --- | --- | --- |
| 视图 | `View` | 屏幕上可绘制的矩形区域；可以响应事件 |
| 键盘 | `KeyboardView` | 渲染键盘 |
| 标签 | `TextView` | 显示文本 |
| 文本字段 | `EditText` | 可编辑的文本字段，用户可输入数据 |
| 按钮 | `Button` | 可按下和点击的按钮 |
| 单选按钮 | `RadioButton` | 用户可勾选的二态按钮；在组中使用时，勾选一个单选按钮会自动取消勾选组中的其他单选按钮 |
| 复选框 | `CheckBox` | 用户可勾选或取消勾选的二态按钮 |
| 二态切换按钮 | `ToggleButton` | 可在两个选项之间选择的二态开关按钮 |
| 二态切换按钮 | `Switch` | 类似于 `ToggleButton`；用户也可以在两种状态之间滑动 |

表 2.2 选定的 GUI 组件及其类

![](img/9781284093650_CH02_FIGF01.jpg)

图 2.1 选定 GUI 组件的继承层次结构

## 2.4 `RelativeLayout`、`TextView`、`EditText` 和 `Button`：小费计算器，版本 0

在应用的版本 0 中，我们显示一些 GUI 组件，但不具备任何功能。该版本使用了四个 GUI 组件：两个 `TextView` 用于显示账单和小费百分比的标签，以及两个 `EditText` 用于用户输入账单和小费百分比。在这个版本中，我们不处理任何用户数据，只关心将小部件放置在屏幕上；我们甚至不计算或显示小费金额和总金额。

为了保持简单，我们只允许应用在竖屏方向下工作，这可以在 `AndroidManifest.xml` 文件中指定。我们通过将 `activity` 标签的 `android:screenOrientation` 属性赋值为 `portrait` 来实现，如示例 2.2 的第 13 行所示。

我们编辑 `activity_main.xml` 文件来定义用户界面。如果 GUI 是静态的，并且不会随着用户与应用交互而改变，那么 `activity_main.xml` 是定义它的好方法。如果 GUI 是动态的，并且随着应用运行而改变，那么我们可以通过代码来创建和定义用户界面。例如，如果应用从文件中检索链接列表并显示它们，我们事先不知道会检索到多少链接以及需要显示多少。通常，我们在 `activity_main.xml` 文件中通过 XML 属性和值所能做的，也可以通过编程方式实现。

在编辑小费计算器应用的 `activity_main.xml` 文件之前，让我们先看看创建项目时提供的骨架。`TextView` 元素具有以下两个属性和值：

```xml
android:layout_width="match_parent"
android:layout_height="wrap_content"
```

![](img/ch02exa02.jpg)

示例 2.2 `AndroidManifest.xml` 文件

`android:layout_width` 和 `android:layout_height` 是特殊的属性，可以用常规的 `View` 属性来指定，但由 `View` 的父容器解析。它们属于 `static` 类 `ViewGroup.LayoutParams`，`View` 使用它来告诉父容器它们希望如何布局。`ViewGroup.LayoutParams` 是嵌套在 `ViewGroup` 类内部的 `static` 类。

`ViewGroup.LayoutParams` 类使我们能够指定 `View` 相对于其父容器的宽度和高度。我们可以使用其 `android:layout_width` 和 `android:layout_height` XML 属性来指定 `View` 的宽度和高度，不仅可以使用绝对值，还可以相对于 `View` 的父容器。该类提供了两个常量 `MATCH_PARENT` 和 `WRAP_CONTENT` 来实现此目的，如表 2.3 所示。

我们可以为 `android:layout_width` 和 `android:layout_height` XML 属性分配 `match_parent` 值或 `wrap_content` 值。`match_parent` 值对应于 `ViewGroup.LayoutParams` 类的常量 `MATCH_PARENT`（值为 –1），表示 `View` 应该与其父容器一样大，减去内边距。`wrap_content` 值对应于 `ViewGroup.LayoutParams` 类的常量 `WRAP_CONTENT`（值为 –2），表示 `View` 的尺寸应刚好大到足以容纳其内容，加上内边距。

如果我们查看 `activity_main.xml` 中骨架代码的 `TextView`，会发现我们将 `View` 的宽度和高度相对于其内容的宽度和高度进行了尺寸设置。

| 属性名称 | 描述 |
| --- | --- |
| `android:layout_width` | 设置视图的宽度 |
| `android:layout_height` | 设置视图的高度 |

| 常量 | 值 |
| --- | --- |
| `MATCH_PARENT` | –1 |
| `WRAP_CONTENT` | –2 |

## 表 2.3 `ViewGroup.LayoutParams` 的 XML 属性和常量

我们也可以使用绝对坐标来设置 `View` 的尺寸。如果要指定绝对尺寸，有几种单位可用：`px`（像素）、`dp`（密度无关像素）、`sp`（基于首选字体大小的缩放像素）、`in`（英寸）、`mm`（毫米）。

例如：

```xml
android:layout_width="200dp"
android:layout_height="50dp"
```

然而，应用最终会在许多不同屏幕尺寸的设备上运行。因此，我们建议使用相对定位而非绝对定位。如果选择使用绝对尺寸，我们推荐使用 `dp` 单位，因为它们与安装应用的设备的屏幕密度无关。

此外，每个 GUI 元素都必须同时包含 `android:layout_width` 和 `android:layout_height` 属性。省略其中一个将导致运行时异常；应用会停止并显示以下消息：

```text
Unfortunately, AppName has stopped
```

如图 2.1 所示，`EditText` 和 `Button` 是 `TextView` 的子类，而 `TextView` 本身是 `View` 的子类；因此，这三个类除了拥有自己的属性外，还继承了 `View` 的属性。表 2.4 展示了 `View` 的一些 XML 属性，以及对应的方法和描述。完整列表可参见 `http://www.developer.android.com/reference/android/view/View.html`。

| 属性名称 | 相关方法 | 描述 |
| --- | --- | --- |
| `android:id` | `setId( int )` | 为 `View` 设置 id；之后可通过代码使用该 id 获取 `View` |
| `android:minHeight` | `setMinimumHeight( int )` | 定义 `View` 的最小高度 |
| `android:minWidth` | `setMinimumWidth( int )` | 定义 `View` 的最小宽度 |

## 表 2.4 `View` 的部分 XML 属性和方法

![](img/9781284093650_CH02_FIGF02.jpg)

## 图 2.2 选定的布局管理器类

Android 开发工具包（ADK）提供了布局管理器类，用于在屏幕上排列 GUI 组件；它们是 `ViewGroup` 的子类。图 2.2 展示了其中一些类。

创建空项目时，`activity_main.xml` 中使用的默认布局管理器是 `RelativeLayout`。它允许我们将组件相对于其他组件进行定位。通常，布局管理器类会有一个 `public static` 内部类，通常命名为 `LayoutParams`，其中包含用于定位组件的 XML 属性。如果类名为 `C`，则我们称该内部类为 `C.LayoutParams`。`RelativeLayout` 类有一个名为 `LayoutParams` 的 `public static` 内部类（我们使用 `RelativeLayout.LayoutParams` 来引用它），其中包含许多 XML 属性，允许我们将元素相对于彼此排列，例如位于某个 `View` 下方，或位于另一个 `View` 的右侧。为了引用另一个 `View`，我们可以为该 `View` 设置一个 id，并使用该 id 进行引用。我们也可以相对于父 `View` 来定位一个 `View`，此时无需通过 id 引用父 `View`。表 2.5 列出了其中一些属性。前八个列出的属性（`android:layout_alignLeft` 到 `android:layout_toRightOf`）期望其值为某个 `View` 的 id。最后四个列出的属性期望其值为 `true` 或 `false`。

如果某个值要作为 `View` 的 id，则该 `View` 必须已被赋予一个 id。

Android 框架允许我们使用 `android:id` XML 属性为 `View` 赋予一个整数 id，以便我们引用它，并通过代码使用该 id 获取它。id 必须是资源引用，并使用 `@+` 语法设置，如下所示：

```xml
android:id="@+id/idValue"
```

| XML 属性 | 描述 |
| --- | --- |
| `android:layout_alignLeft` | 当前 View 的左边缘与指定 View 的左边缘对齐 |
| `android:layout_alignRight` | 当前 View 的右边缘与指定 View 的右边缘对齐 |
| `android:layout_alignBottom` | 当前 View 的底边缘与指定 View 的底边缘对齐 |
| `android:layout_alignTop` | 当前 View 的顶边缘与指定 View 的顶边缘对齐 |
| `android:layout_above` | 当前 View 位于指定 View 的上方 |
| `android:layout_below` | 当前 View 位于指定 View 的下方 |
| `android:layout_toLeftOf` | 当前 View 位于指定 View 的左侧 |
| `android:layout_toRightOf` | 当前 View 位于指定 View 的右侧 |
| `android:layout_alignParentLeft` | 如果为 true，当前 View 的左边缘与其父 View 的左边缘对齐 |
| `android:layout_alignParentRight` | 如果为 true，当前 View 的右边缘与其父 View 的右边缘对齐 |
| `android:layout_alignParentBottom` | 如果为 true，当前 View 的底边缘与其父 View 的底边缘对齐 |
| `android:layout_alignParentTop` | 如果为 true，当前 View 的顶边缘与其父 View 的顶边缘对齐 |

## 表 2.5 `RelativeLayout.LayoutParams` 的实用 XML 属性

示例 2.3 展示了版本 0 的 `activity_main.xml` 文件。与骨架应用相比，我们添加了两个 `EditText`（第 21–30 行和第 42–51 行），以及另一个 `TextView` 元素（第 32–40 行）。我们使用两个 `TextView` 元素作为标签，描述两个期望用户输入数据的 `EditText`。我们希望账单的 `TextView` 和 `EditText` 显示在同一水平线上，而小费百分比的 `TextView` 和 `EditText` 显示在下一行。我们不希望这四个 `View` 中的任何一个占据屏幕的全部宽度或高度；因此，所有四个 `View` 的 `android:layout_width` 和 `android:layout_height` 属性都使用了 `wrap_content` 值（第 15–16 行、第 23–24 行、第 34–35 行、第 44–45 行）。我们还指定它们使用字号 28（第 18 行、第 28 行、第 39 行、第 49 行）。

![](img/ch02exa03.jpg)

![](img/ch02exa03a.jpg)

## 示例 2.3 小费计算器应用版本 0 的 `activity_main.xml` 文件

| XML 属性 | 方法 | 描述 |
| --- | --- | --- |
| `android:textSize` | `void setTextSize( int unit, float size )` | 设置文本的大小 |
| `android:hint` | `void setHint( int resource )` | 设置要显示的提示文本 |

## 表 2.6 `TextView` 的 `android:textSize` 和 `android:hint` XML 属性

我们为所有元素都赋予了 id（第 14 行、第 22 行、第 33 行、第 43 行），以便在相对定位时引用它们。我们将第一个 `TextView`（存储账单标签）用作屏幕左上角的锚点元素。在第 17 行，我们为其设置了最小宽度 120 像素；选择该值是为了使我们将要放置在账单标签下方的所有标签文本都能轻松容纳。

在第 25 行，我们指定第一个 `EditText`（用户输入账单的地方）位于账单标签的右侧。在第 26 行，我们指定其底边缘与账单标签的底边缘在同一水平线上。在第 27 行，我们指定其右边缘与其父 `View` 的右边缘对齐，从而使其延伸到屏幕的右边缘。

在第 36 行，我们指定小费百分比的标签位于账单标签（其 id 为 `label_bill`）的下方。在第 37 行和第 38 行，我们指定其左边缘和右边缘与账单标签对齐。

在第 46 行，我们指定第一个 `EditText`（用户输入账单的地方）位于账单标签的右侧。在第 47 行，我们指定其底边缘与账单标签的底边缘在同一水平线上。在第 48 行，我们指定其右边缘与其上方的 `EditText`（其 id 为 `amount_bill`）的右边缘对齐。

我们在第 29 行和第 50 行为两个 `EditText` 分配了提示值；这两个提示值都在 `strings.xml` 文件中定义。表 2.6 展示了 `TextView` 的 `android:textSize` 和 `android:hint` XML 属性，以及对应的方法和描述。由于 `EditText` 是 `TextView` 的子类，因此 `EditText` 继承了这两个属性。默认字体大小较小，因此我们将 `TextView` 和 `EditText` 的字体大小设置为 28。通过指定 `sp` 单位，我们确保字体大小与屏幕密度无关。字体大小直接影响 `TextView` 的大小，因为它们会包裹其内容。如果指定了较大的字体大小，组件可能无法在小屏幕设备上完全显示。在本应用中，暂时不必担心这个问题。我们将在本书后面学习如何解决该问题。

两个 `EditText` 元素还包含一个从 `TextView` 继承的属性 `android:inputType`（第 30 行和第 51 行）；其值定义了该字段允许输入的数据类型。表 2.7 列出了一些可选值。我们希望用户只能为账单输入数字和小数点，因此为第一个 `EditText` 元素（第 30 行）选择了 `numberDecimal`。应用运行时，我们将无法输入除数字或小数点以外的任何字符（实际上最多只能输入一个小数点）。我们希望用户只为小费百分比输入数字，因此为第二个 `EditText` 元素（第 51 行）选择了 `number`。尝试将第 30 行或第 51 行修改为 `textPassword` 并重新运行应用。我们会发现输入的每个字符都被隐藏，并显示为一个小实心圆。

| 属性值 | 描述 |
| --- | --- |
| `text` | 纯文本 |
| `textPassword` | 文本被隐藏；最后一个字符短暂显示 |
| `number` | 仅限数字 |
| `numberDecimal` | 数字和可选的一个小数点 |
| `phone` | 用于输入电话号码 |
| `datetime` | 用于输入日期和时间 |
| `date` | 用于输入日期 |
| `time` | 用于输入时间 |



表 2.7 `TextView` 的 `android:inputType` XML 属性的部分可选值

![](img/ch02exa04.jpg)

示例 2.4 `strings.xml` 文件，小费计算器应用，版本 0

![](img/9781284093650_CH02_FIGF03.jpg)

图 2.3 小费计算器 GUI，版本 0，显示在 Android Studio 环境中

图 2.3 展示了 Android Studio 环境中的当前 GUI。我们可以看到两个 `TextView` 和 `EditText`，包括两个提示：屏幕顶部空间不足，无法正常显示“Enter Bill”。在版本 1 中，我们将修复此问题，添加更多 GUI 元素，并改善外观和体验。

## 2.5 GUI 组件与更多 XML 属性：小费计算器，版本 1

在版本 1 中，我们完成 GUI，添加两个标签和两个 `TextView` 来显示小费金额和总金额，以及一个 `Button`。在版本 2 中，当用户点击 `Button` 时，我们将更新小费和总金额。我们还添加颜色，使 `EditText` 中的文本居中，并在各个元素周围添加外边距以及内部内边距。

表 2.8 展示了更多 XML `View` 属性，以及对应的方法和描述。每个 XML 属性与方法之间可能并非一一对应。例如，单个方法（如 `setPadding`）用于设置多个属性（`paddingBottom`、`paddingLeft`、`paddingRight`、`paddingTop`）的值。内边距属性与 GUI 组件 `内部` 的额外间距有关，即组件边框与其内容之间的间距。如果要在 GUI 组件之间（即 `外部`）添加额外间距，可以使用 `ViewGroup.MarginLayoutParams` 类的外边距属性，如表 2.9 所示。

我们可以为示例 2.3 中的第一个 `TextView` 添加一些内边距和外边距，如下代码序列所示：

```xml
<TextView
  android:id="@+id/label_bill"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_marginTop="70dp"
  android:layout_marginLeft="50dp"
  android:padding="10dp"
  android:minWidth="120dp"
  android:textSize="28sp"
  android:text="@string/label_bill"/>
```

| 属性名称 | 相关方法 | 描述 |
| --- | --- | --- |
| `android:background` | `setBackgroundColor(int)` | 设置 View 的透明度和背景颜色 |
| `android:background` | `setBackgroundResource(int)` | 设置用作 View 背景的 drawable 资源 |
| `android:alpha` | `setAlpha(float)` | 设置 View 的透明度值 |
| `android:paddingBottom` | `setPadding(int, int, int, int)` | 设置 View 底部边缘的内边距（以像素为单位） |
| `android:paddingLeft` | `setPadding(int, int, int, int)` | 设置 View 左侧边缘的内边距（以像素为单位） |
| `android:paddingRight` | `setPadding(int, int, int, int)` | 设置 View 右侧边缘的内边距（以像素为单位） |
| `android:paddingTop` | `setPadding(int, int, int, int)` | 设置 View 顶部边缘的内边距（以像素为单位） |

表 2.8 `View` 的更多选定 XML 属性和方法

| 属性名称 | 相关方法 | 描述 |
| --- | --- | --- |
| `android:layout_marginBottom` | `setMargins(int, int, int, int)` | 在此 View 底部设置额外空间 |
| `android:layout_marginLeft` | `setMargins(int, int, int, int)` | 在此 View 左侧设置额外空间 |
| `android:layout_marginRight` | `setMargins(int, int, int, int)` | 在此 View 右侧设置额外空间 |
| `android:layout_marginTop` | `setMargins(int, int, int, int)` | 在此 View 顶部设置额外空间 |

表 2.9 `ViewGroup.MarginLayoutParams` 的选定 XML 属性和方法

![](img/9781284093650_CH02_FIGF04.jpg)

图 2.4 `TextView` 的外边距和内边距

图 2.4 展示了由此产生的内边距和外边距。账单标签的顶部边缘距离屏幕顶部 70 像素（因为账单标签上方没有 GUI 组件）。其左侧边缘距离屏幕左侧 50 像素（因为账单标签左侧没有 GUI 组件）。文本“Bill”周围有 10 像素的空白空间。

| XML 属性 | 方法 | 描述 |
| --- | --- | --- |
| `android:textColor` | `setTextColor(int)` | 文本颜色 |
| `android:textStyle` | `setTypeface(Typeface)` | 文本样式（粗体、斜体、常规） |
| `android:gravity` | `setGravity(int)` | 此 TextView 内的文本对齐方式 |

表 2.10 `TextView` 的选定 XML 属性

我们还可以设置 `TextView` 的更多文本属性，例如颜色、样式或对齐方式。表 2.10 展示了 `TextView` 的 `android:textColor`、`android:textStyle` 和 `android:gravity` XML 属性。`android:gravity` 属性与文本在 `TextView` 内的对齐方式有关；默认为左对齐。

表 2.11 展示了 `TextView`（或任何继承自 `TextView` 的 GUI 组件）的 `android:textColor` XML 属性值的可能格式。同样适用于 `View` 的 `android:background` XML 属性。更一般地，对于 `View` 的 XML 属性，通常有三种策略来设置其值：

- ▸ 直接指定值
- ▸ 引用资源
- ▸ 引用主题属性

我们将在本章后面讨论主题。在本段中，我们讨论前两种策略。

| 描述 | 格式 | 说明 |
| --- | --- | --- |
| 6 位颜色值 | `"#rrggbb"` | r、g、b 为十六进制数字，分别表示颜色中红、绿、蓝的含量 |
| 透明度和 6 位颜色值 | `#aarrggbb` | a 是表示透明度值的十六进制数字（0 表示透明，f 表示不透明） |
| 3 位颜色值 | `#rgb` | r、g、b 会重复 |
| 透明度和 3 位颜色值 | `#argb` | a、r、g、b 会重复 |
| 引用资源 | `@[+][package:]type:name` | [ ] 表示可选字段 |
| 引用主题属性 | `?[package:][type:]name` |  |

## 表 2.11 用于 `android:textColor` 或 `android:background` 的颜色可能格式

要为文本指定黄色（例如，全红、全绿、无蓝），我们可以通过四种不同的方式直接为 `android:textColor` 属性赋值：

```xml
android:textColor="#FFFF00"
android:textColor="#FFFFFF00"
android:textColor="#FF0"
android:textColor="#FFF0"
```

如果颜色字符串只有三个或四个字符，则每个字符会被重复，以得到等效的六位或八位颜色字符串。如果只有六个字符，则前两个字符指定红色的量，接下来两个字符指定绿色的量，最后两个字符指定蓝色的量。如果有八个字符，则前两个字符指定颜色的不透明度，最后六个字符像之前一样指定红、绿、蓝的各种量。FF 表示完全不透明，00 表示完全透明。如果未指定不透明度（即只有三个或六个字符），则默认为完全不透明。

在 `"FFFFFF00"` 中，前两个 F 表示不透明颜色；00 则表示完全透明颜色。在 `"FFF0"` 中，第一个 F 表示不透明颜色；0 则表示完全透明颜色。

另一种指定颜色的方式是使用如下形式的资源：

```text
"@[+][package:]type:name"
```

我们已经了解到，可以像在 `strings.xml` 文件中那样将字符串资源外部化。我们还可以外部化其他资源，例如：`bool`、`color`、`dimension`（使用标签名 `dimen`）、`id`、`integer`、`integer-array`（使用标签名 `integer-array`）和 `typed array`（使用标签名 `array`）。

语法表达式中的方括号 `[]` 表示该字段是可选的。

为了使用此语法，我们在一个名为 `colors.xml` 的资源文件中外部化一些颜色。文件名并不重要，但最好选择一个有意义的文件名；文件应具有 `.xml` 扩展名，并且必须位于项目的 `res/values/` 目录中，以便 Android 框架能够找到它。虽然不使用 `.xml` 扩展名不会阻止我们的应用运行，但我们建议对这些文件使用 `.xml` 扩展名。

如果我们将 `colors.xml` 放在错误的目录中，例如 `res/layout/` 目录，则会出现编译器错误。

表 2.12 显示了 `res` 目录内支持的目录及其描述。

要指定由新创建的资源文件 `colors.xml` 中名为 `lightGreen` 的字符串定义的颜色，我们编写以下代码：

```xml
android:textColor="@color/lightGreen"
```

在 `colors.xml` 文件中，我们包含了以下代码（示例 2.5 的第 8 行）以定义 `lightGreen`：

```xml
<color name="lightGreen">#40F0</color>
```

| 目录 | 目录内容描述 |
| --- | --- |
| `animator` | 定义属性动画的 XML 文件 |
| `anim` | 定义补间动画的 XML 文件 |
| `color` | 定义颜色状态列表的 XML 文件（例如，可用于为按钮的不同状态指定不同颜色） |
| `drawable` | 定义可绘制资源的位图文件或 XML 文件（在此处放置应用的可绘制资源） |
| `mipmap` | 定义可绘制资源的位图文件或 XML 文件（在此处放置应用的图标） |
| `layout` | 定义 GUI 布局的 XML 文件 |
| `menu` | 定义菜单的 XML 文件 |
| `raw` | 以原始形式保存的文件 |
| `values` | 定义字符串、整数、颜色和其他简单值的 XML 文件 |
| `xml` | 可在运行时通过调用 `Resources.getXML(resourceIdNumber)` 读取的 XML 文件 |

## 表 2.12 `res` 目录内支持的目录列表

![](img/9781284093650_CH02_FIGF05.jpg)

## 示例 2.5 `colors.xml` 文件

`Color` 是资源类型，`lightGreen` 是其名称。文件名 `colors.xml` 虽然推荐使用，但并不重要；我们可以为它选择任何其他名称。我们甚至可以有多个定义颜色的文件。必须使用 `resources` 元素（示例 2.5 的第 2 行）作为 `color` 的父元素。如果使用其他元素，则会收到“无效的开始标签”错误消息。

如果删除 `resources` 的开始和结束标签，则会收到 XML 文档格式不正确的错误消息。XML 文档中的任何错误都会在尝试编译或运行应用时中止构建。

在编译时，`resources` 元素的每个子元素都会被转换为应用资源对象；在 `colors.xml` 中，`resources` 有四个子元素，都是 `color` 元素。然后每个子元素都可以通过其名称在其他文件中引用，例如 `lightGreen`。

示例 2.6 显示了更新后的 `activity_main.xml` 文件。我们从示例 2.3 中删除了第 7 到第 10 行（指定应用 GUI 周围的填充），因为我们重新定义了各个 GUI 元素的边距，不再需要默认填充。

![](img/ch02exa06.jpg) ![](img/ch02exa06a.jpg) ![](img/ch02exa06b.jpg) ![](img/ch02exa06c.jpg)

## 示例 2.6 `activity_main.xml` 文件，小费计算器应用，版本 1

我们将顶部的输入相关元素与底部的计算相关元素用一条红线（第 63–72 行）分隔开。红线是一个 `View` 元素（第 64 行），其高度为 5 像素（第 68 行）。我们使用之前用过的相同定位属性，将五个新元素相对于彼此以及现有的四个元素进行定位：`android:layout_below`、`android:layout_alignLeft`、`android:layout_alignRight` 和 `android:layout_toRightOf`。我们将屏幕左侧的四个 `TextView` 和红线对齐，指定它们都与账单标签对齐（第 43、70、81、106 行）。我们通过使用 `android:layout_marginTop` 属性（第 41、67、78、103、127 行）指定元素之间垂直间距恒定为 20 像素。

我们为所有 `TextView`、`EditText` 和 `Button` 元素添加相同的填充量，即 10 像素（第 15、25、40、53、79、91、104、116、128 行）。在第 13–15 行，我们为账单标签（我们的锚点元素）添加了边距和填充。

我们在第 18、46、84、109 行将左侧四个 `TextView` 的背景设置为浅灰色。我们在第 95 和 120 行将计算后的小费和总金额的背景设置为浅绿色。我们在第 32 和 59 行将两个 `EditText` 元素的文本颜色设置为深蓝色。我们保留了左侧四个 `TextView` 的默认左对齐。我们将右侧的两个 `EditText` 和两个 `TextView` 居中对齐（第 31、58、96、121 行）。如图 2.5 所示，当我们输入时，Android Studio 会建议可能的取值。

在第 129 行，我们将按钮水平居中。此时，按钮不会响应用户点击；我们将在版本 3 中实现该功能。

示例 2.7 显示了更新后的 `strings.xml` 文件。

我们可以在图 2.6 中看到各种组件的大小、颜色、字体大小和字体样式，该图显示了 Android Studio 环境中的 GUI。

![](img/9781284093650_CH02_FIGF05.jpg)

## 图 2.5 Android Studio 环境，显示 `android:gravity` 属性的建议值

![](img/ch02exa07.jpg)

示例 2.7 `strings.xml` 文件，小费计算器应用，版本 1

## 2.6 样式与主题：小费计算器，版本 2

在版本 1 中，许多 GUI 组件具有相同的属性及相同的值。例如，`activity_main.xml` 文件中的九个元素在 `android:layout_width` 和 `android:layout_height` 属性上都使用了 `wrap_content` 值。Android 开发工具包（ADK）允许我们将样式外部化到资源中，以便复用，从而为各种元素应用统一的样式。

![](img/9781284093650_CH02_FIGF06.jpg)

图 2.6 小费计算器 GUI，版本 1，在 Android Studio 中显示

样式的概念类似于 HTML 页面中的 CSS（层叠样式表）。样式是用于指定 `View` 或窗口外观的属性（XML 属性）集合。样式可以指定宽度、高度、内边距、背景颜色、文本颜色、文本大小等属性。然后，我们可以使用样式为一个或多个 `View` 指定 XML 属性的值。样式允许我们将 `View` 的外观与其内容分离。

我们可以在 `res/values` 目录下的 `styles.xml` 文件中定义样式。在该文件中，我们可以定义多个样式，每个样式包含一组 XML 属性和值；每个样式都有一个名称，用于引用它。

定义样式的语法如下：

```xml
<style name="样式名称" [parent="该样式继承的样式"]>
  <item name="属性名称">属性值</item>
  . . .
</style>
```

![](img/9781284093650_CH02_FIGF07.jpg)

图 2.7 `styles.xml` 中定义的样式继承层次结构

一个样式可以继承自另一个样式。继承通过 `parent` 属性定义，且为可选。父样式可以是 Android 原生样式，也可以是用户自定义样式。



通过这种方式定义样式，我们可以构建一个继承层次结构；不仅多个 GUI 元素可以使用同一样式，而且一个样式可以通过继承复用另一个样式的属性。样式还可以覆盖其继承的属性的值。

我们定义了六个样式，如图 2.7 所示。我们为两个 `EditText` 使用了 `InputStyle`：它继承自 `CenteredTextStyle`，而 `CenteredTextStyle` 本身继承自 `TextStyle`，`TextStyle` 又继承自 Android 标准开发工具包（Android SDK）中的现有样式 `TextAppearance`。因此，`EditText` 中的文本将居中显示，大小为 28，颜色为深蓝色。请注意，从 `TextAppearance` 继承的默认文本颜色为黑色，但已被覆盖。两个 `EditText` 的大小将根据其内容而定。

示例 2.8 展示了 `styles.xml` 文件。`TextStyle` 在第 11–16 行定义；它使用语法 `parent="@android:style/父样式名称"` 继承自 Android 原生样式 `TextAppearance`。请注意，每个 `item` 元素的内容（例如 `wrap_content` 或 `28sp`）不包含在双引号内。

在第 18–20 行，`LabelStyle` 使用语法 `parent="父样式名称"` 继承自我们自己的 `TextStyle`。因此，它继承了 `TextStyle` 在第 12–15 行定义的四个属性及其值：`android:layout_width`、`android:layout_height`、`android:textSize` 和 `android:padding`。它还在第 19 行为 `android:background` 属性指定了 `colors.xml` 中定义的浅灰色。因此，任何使用 `LabelStyle` 样式的元素都将具有浅灰色背景、文本周围 10 像素的内边距，文本大小为 28。该元素的大小将根据其内部文本设置。

![](img/ch02exa08.jpg)

示例 2.8 `styles.xml` 文件

在第 22–24 行，`CenteredTextStyle` 也继承自我们自己的 `TextStyle`，指定文本居中。在第 26–28 行，`InputStyle` 继承自 `CenteredTextStyle`，指定文本颜色为 `colors.xml` 中定义的深蓝色。在第 30–32 行，`OutputStyle` 也继承自 `CenteredTextStyle`，指定背景颜色为 `colors.xml` 中定义的浅绿色。最后，在第 34–36 行，`ButtonStyle` 继承自 `TextStyle`，指定背景颜色为 `colors.xml` 中定义的深绿色。

XML 样式文件不仅提供了一个集中定义样式的位置，还使我们的代码更加有条理，更易于维护和修改。通常，我们希望同一类型的 GUI 组件具有相同的样式主题。如果所有 `TextView` 组件都设置为红色，而我们决定将它们改为紫色，那么只需在一个位置更改一行代码即可。我们还可以在许多应用中复用样式。此外，创建和编辑样式文件所需的专业知识与编写 Java 代码所需的专业知识不同。如果应用复杂且由一组开发人员开发，则更容易根据各自的专长将工作分开并分配给团队成员。

在示例 2.9 中，我们使用 `styles.xml` 中定义的样式对 `activity_main.xml` 中的 GUI 元素进行样式设置。结果得到了与版本 1 相同的 GUI。为了对 GUI 组件应用样式，我们使用以下语法：

```xml
style="@style/样式名称"
```

如果写成 `android:style` 而不是 `style`，会导致编译器错误。

在第 11、29、58 和 74 行，我们使用 `LabelStyle` 对屏幕左侧的四个 `TextView` 元素进行样式设置。在第 19 和 38 行，我们使用 `InputStyle` 对两个 `EditText` 元素进行样式设置。在第 67 和 83 行，我们使用 `OutputStyle` 对两个输出 `TextView` 元素进行样式设置。`Button` 元素在第 89 行使用 `ButtonStyle` 进行样式设置。

如果我们修改 `styles.xml` 文件，例如将 `LabelStyle` 的 `android:background` 属性从浅灰色改为其他颜色，那么当我们再次运行应用时，就会看到这一变化。

样式通常应用于一个或多个屏幕。通常，我们希望屏幕中的 `View` 具有相同的外观。或者，我们希望应用中的所有屏幕都具有相同的外观。通过使用样式，我们可以为 Activity 或整个应用赋予主题。

![](img/ch02exa09.jpg) ![](img/ch02exa09a.jpg)

示例 2.9 `activity_main.xml` 文件，小费计算器应用，版本 2

要将样式应用于整个应用，我们在 `AndroidManifest.xml` 文件的 `application` 元素中添加 `android:theme` 属性，语法如下：

```xml
android:theme="@style/样式名称"
```

`AndroidManifest.xml` 骨架中已经包含了使用样式 `AppTheme` 的上述语法。`AppTheme` 已在 `styles.xml` 骨架中声明，我们可以在 `styles.xml` 中编辑 `AppTheme`。我们也可以使用 `styles.xml` 中的样式，并将示例 2.2 的第 10 行修改如下：

```xml
android:theme="@style/LabelStyle"
```

要将样式应用于给定的 Activity，我们在 `AndroidManifest.xml` 文件的 `activity` 元素中添加 `android:theme` 属性，如下所示：

```xml
android:theme="@style/样式名称"
```

例如，我们可以在示例 2.2 的第 12 行和第 13 行之间插入一行，如下所示：

```xml
android:theme="@style/OutputStyle"
```

当前应用中只有一个 Activity，但在更复杂的应用中，可能会有多个 Activity，因此 `AndroidManifest.xml` 文件中可能会有多个 `activity` 元素。每个 Activity 可以单独设置主题。

现在我们已经有了模型和视图，接下来可以编辑控制器，使得当用户输入新的账单金额或小费百分比并点击“计算”按钮时，应用能够计算并显示小费和总金额。

## 2.7 事件与简单事件处理：编写控制器，小费计算器，版本 3

点击按钮被称为事件。在事件发生后执行某些代码（例如更新文本字段的值）被称为处理事件。在 GUI 编程中，事件类型有很多种：点击按钮、勾选复选框、从列表中选择项目、按下按键、点击屏幕、滑动屏幕等等。

在 `activity_main.xml` 文件中，我们可以为 `View` 的 `android:onClick` 属性指定一个方法名：当用户点击该 `View` 时，该方法将被调用。语法如下：

```xml
android:onClick="methodName"
```

该方法应位于控制该 `View` 的 `Activity` 类中，在本例中为 `MainActivity`。`Button` 类继承自 `View`，因此我们可以在 `activity_main.xml` 文件的 `Button` 元素中使用 `android:onClick` 这个 `XML` 属性。如果我们希望用户点击 `Button` 时执行一个名为 `calculate` 的方法，可以这样写：

```xml
android:onClick="calculate"
```

![](img/ch02exa10.jpg)

示例 2.10 `activity_main.xml` 文件中的 `Button` 元素

示例 2.10 展示了 `activity_main.xml` 文件中更新后的部分。

我们应在相应的上下文中编写该方法，通常是在 `Activity` 类中。如果不编写该方法，当用户点击按钮时应用会崩溃。该方法必须具有以下头部：

```java
public void methodName(View v)
```

在方法内部，`View` 参数 `v` 是触发事件的 `View` 的引用。

因此，在 `MainActivity` 类中，我们需要编写 `calculate` 方法，其头部如下：

```java
public void calculate(View v)
```

在该方法内部，我们需要访问 `EditText` 元素以获取用户输入的数据，并访问一些 `TextView` 元素以相应地更新它们。

如果某个 `View` 被赋予了 id，我们可以使用 `Activity` 类（由 `AppCompatActivity` 类继承）的 `findViewById` 方法（如表 2.13 所述）来获取对该 `View` 的引用，调用方式如下：

```java
findViewById(R.id.idValue)
```

现在 `activity_main.xml` 文件已定义，我们可以编写 `MainActivity` 类（如示例 2.11 所示）及其新方法 `calculate`。

`calculate` 方法需要获取两个 `EditText` 组件中输入的金，计算相应的小费和总金额，并相应地更新两个输出 `TextView`。

在第 12 行，我们声明了一个 `TipCalculator` 实例变量 `tipCalc`。通过它，我们可以调用 `TipCalculator` 类的任何方法来执行各种计算。在第 6–8 行，我们导入了 `View`、`TextView` 和 `EditText` 类。`View` 位于 `android.view` 包中；`TextView` 和 `EditText` 位于 `android.widget` 包中。我们需要导入它们，因为在 `calculate` 方法（第 21–51 行）中使用了它们。当 `calculate` 被调用时，`View` 参数是触发事件的 `View` 的引用，在本例中是按钮。我们在第 23 行输出它，仅用于反馈目的。如果我们在没有 `View` 参数的情况下尝试编写 `calculate` 方法，代码可以编译，但当我们运行应用并点击 Calculate 按钮时，会出现运行时异常。

| 类 | 方法 |
| --- | --- |
| `Activity` | `View findViewById(int id)` 查找并返回由 `onCreate` 方法（例如 `activity_main.xml`）中膨胀的 XML 的 `id` 属性标识的 `View` |
| `TextView` | `CharSequence getText()` 返回 `TextView` 小部件中显示的文本 |
| `TextView` | `void setText(CharSequence text)` 设置要在 `TextView` 小部件中显示的文本 |

表 2.13 `Activity` 和 `TextView` 类的有用方法

在第 24–27 行，我们使用从 `Activity` 类继承的 `findViewById` 方法，传入它们的 id `R.id.amount_bill` 和 `R.id.amount_tip_percent`，获取两个 `EditText` 组件的对象引用。由于 `findViewById` 方法返回一个 `View`，我们将其返回值强制转换为 `EditText`。

在第 28–29 行，我们获取用户在两个 `EditText` 中输入的数据，并将这两个值赋给 `billString` 和 `tipString` 字符串；我们使用了 `TextView` 类（由 `EditText` 类继承）的 `getText` 方法（表 2.13）。`getText` 返回一个 `CharSequence`，因此我们额外调用 `CharSequence` 的 `toString` 方法，将从 `EditText` 获取的每个值转换为 `String`。

这两个值是 `String`；我们使用 `Float` 和 `Integer` 类的 `parseFloat` 和 `parseInt` 静态方法将它们转换为 `float` 和 `int` 以便处理。尽管 `parseFloat` 和 `parseInt` 方法（第 37 和 38 行）抛出的异常是非受检异常，但使用 `try` 和 `catch` 块以防止在获取的数据不是有效数字时抛出运行时异常是一种良好实践。在第 39–41 行，我们更新模型：通过调用 `setBill` 和 `setTip` 设置 `tipCalc` 的账单和小费。在第 42–44 行，我们请求模型调用 `tipAmount` 和 `totalAmount` 来计算小费和总金额。在第 45–47 行，我们使用结果更新视图：使用表 2.13 中的 `setText` 方法将格式化后的小费和总金额放入 `TextView` 中。这样，控制器（`MainActivity` 类）从视图收集输入以更新模型，并从模型获取更新后的数据以更新视图。

![](img/ch02exa11.jpg) ![](img/ch02exa11a.jpg)

示例 2.11 小费计算器应用（版本 3）的 `MainActivity` 类

我们永远不应该进入 `catch` 块（第 48–50 行）；实际上，在 `activity_main.xml` 中指定的两个 `EditText` 的 `numberDecimal` 和 `number` 输入类型保证了账单和小费百分比的值将是有效的浮点数和有效的整数。`android:inputType` 的 `numberDecimal` 值只允许用户输入数字和最多一个小数点。`number` 值只允许用户输入数字。然而，即使我们相当确定它们不会发生，捕获潜在错误并验证数据也是一种良好实践。这种做法称为防御性编程。在 `catch` 块内部（第 49 行），我们可以弹出一个警告视图，通知用户输入正确的数据。

在 Logcat 中，我们应该看到类似以下的输出：

```
v = android.support.v7.widget.AppCompatButton{fe17b58
VFED..C.....P.... 280,1063-799,1235}
```

这表明 `View` 参数确实是一个 `Button`（用户点击的唯一按钮；`AppCompatButton` 是一个扩展 `Button` 并支持旧版本特性的类）；`fe17b58` 是一个十六进制数，表示其内存地址。

图 2.8 展示了用户在账单 `EditText` 中输入 154.50、在小费百分比 `EditText` 中输入 18 并点击 Calculate 按钮后，应用在模拟器中运行的情况。默认情况下，当屏幕上至少有一个 `EditText` 时，软键盘会打开。

有人可能认为，对于这个非常简单的应用，我们并不需要一个完整的模型（`TipCalculator` 类）。然而，即使是简单的应用，遵循模型-视图-控制器架构并拥有独立的模型也是一种良好的实践。在应用的生命周期中，它可能会经历多个版本，复杂度不断增加，每个版本都需要新的特性和功能，这些可以轻松添加到模型中并在控制器中使用。例如，我们可能希望将来升级此应用，加入宾客人数，并计算每位宾客的小费和总账单。我们还可以将小费金额和总账单格式化为仅保留两位小数。我们也可能对构建具有相同功能但不同图形用户界面的应用版本感兴趣。此时只需更新视图和控制器，而无需改动模型。

![](img/9781284093650_CH02_FIGF08.jpg)

图 2.8 小费计算器，版本 3，在模拟器中运行

## 2.8 更多事件处理：小费计算器，版本 4

我们的应用现在具备了一些基本功能，但我们应该在用户更改数据时（即用户在键盘上输入的任何时刻）更新小费和总金额，即使没有点击“计算”按钮。实际上，我们甚至不需要“计算”按钮。为了实现这一点，我们需要编辑视图（删除 `activity_main.xml` 文件中的 `Button` 元素）并更改控制器（处理两个 `EditText` 文本的任何变化）；模型无需改动。示例 2.12 展示了更新后的 `activity_main.xml` 文件的结尾部分。它不再包含 `Button` 元素。由于不再使用按钮，我们还可以删除 `strings.xml` 中的 `button_calculate` 字符串、`styles.xml` 中的按钮样式以及 `colors.xml` 中的深绿色颜色元素。

![](img/ch02exa12.jpg)

示例 2.12 `activity_main.xml` 文件，小费计算器应用，版本 4

我们已经知道，点击 `Button` 是一个事件。在 `EditText` 组件内输入，或者更一般地按下按键，也是一个事件。Android 框架为开发者提供了工具，当事件发生或 GUI 组件内某物发生变化时，这些工具会提醒我们。

通常，要捕获并处理事件，我们需要按顺序执行以下步骤：

1. 编写事件处理程序（一个扩展监听器接口的类）。
2. 实例化该类的对象。
3. 将该对象注册到一个或多个 GUI 组件上。

典型的事件处理程序实现了一个监听器接口，这意味着它需要重写该接口的所有 `abstract` 方法。

嵌套在 `View` 类中的 `static OnKeyListener` 接口包含一个方法 `onKey`，当按键事件分派给 `View` 时调用该方法。然而，软件键盘上的按键通常不会触发对此方法的调用。我们希望我们的应用尽可能通用，并且能在具有硬件键盘或软件键盘的移动设备上同样良好地运行。因此，在此应用中我们不使用 `OnKeyListener` 接口。

来自 `android.text` 包的 `TextWatcher` 接口提供了三个方法，当 GUI 组件（`TextView` 或 `TextView` 的子类对象，如 `EditText`）内的文本发生变化时，这些方法会被调用，前提是 `TextWatcher` 对象已注册到该 `TextView` 上。表 2.14 列出了这些方法。与任何接口一样，这三个方法都是 `abstract` 的。

为了让 `TextWatcher` 能够接收到 `TextView` 内文本变化的通知，我们需要执行以下操作：

- 编写一个实现 `TextWatcher` 接口的类（也称为处理程序）。
- 声明并实例化该类的对象。
- 将该对象注册到 `TextView` 上（在此应用中为两个 `EditText`）。

| 方法 | 何时调用该方法？ |
| --- | --- |



| 方法 | 描述 |
|---|---|
| `void afterTextChanged(Editable e)` | 在`e`内部的某处，文本已发生变化 |
| `void beforeTextChanged(CharSequence cs, int start, int count, int after)` | 在`cs`中，从`start`开始的`count`个字符即将被替换为`after`个字符 |
| `void onTextChanged(CharSequence cs, int start, int before, int count)` | 在`cs`中，从`start`开始的`count`个字符刚刚替换了`before`个字符 |

表 2.14 `TextWatcher` 接口的方法

在我们的处理程序类中，我们只对`afterTextChanged`方法感兴趣。我们并不关心有多少字符发生了变化以及变化发生在文本中的哪个位置。我们只关心文本中发生了某些变化。因此，我们将另外两个方法`beforeTextChanged`和`onTextChanged`实现为“什么都不做”的方法。由于我们需要访问两个`EditText`和两个`TextView`，我们选择将处理程序类实现为`MainActivity`的`private`内部类。在编写处理程序时，我们也可以选择将其实现为独立的`public`类。

示例 2.13 展示了`MainActivity`类的完整代码。我们对整体类设计做了一个重要更改。我们为两个`EditText`添加了实例变量（第 14-15 行）。这不是必须的，但如果我们需要在多个地方访问 GUI 组件（注册处理程序时以及处理文本变化时），直接引用它们会很方便。这比每次访问时都使用`findViewById`方法更简单。这些实例变量在第 23-24 行被实例化。

处理程序类在第 57-69 行编写。`afterTextChanged`方法（第 58-60 行）调用了`calculate`方法（第 31-55 行），该方法与之前的`calculate`方法非常相似；注意我们删除了它的`View`参数。

在第 26 行，我们声明并实例化了一个`TextChangeHandler`对象`tch`。在第 27 和 28 行，我们将`tch`注册到两个`EditText`（`billEditText`和`tipEditText`）上。因此，每当用户更改账单或小费百分比时，`afterTextChanged`会自动被调用；这会触发对`calculate`的调用，从而更新模型，然后相应地更新视图。

![](img/ch02exa13.jpg) ![](img/ch02exa13a.jpg)

示例 2.13 小费计算器应用的 `MainActivity` 类，版本 4

运行应用时，当两个`EditText`组件中的任何一个获得焦点并按下任意键后，小费金额都会更新（除非其中一个`EditText`为空；在这种情况下，我们会执行 catch 块内的代码，组件不会更新）。图 2.9 显示了用户在输入账单值 125.59 并开始输入小费百分比后应用运行的情况。用户一输入 2，小费和总金额就会更新。

与我们在示例 2.13 中（第 57-69 行、第 26 行以及第 27-28 行分别对应）编写一个单独的处理程序类、实例化该类的对象并将其注册到一个或多个 GUI 组件上的做法不同，有些开发者喜欢使用匿名对象，并编写如下代码：

```java
tipEditText.addTextChangedListener(new TextWatcher() {
    // 在此处重写 afterTextChanged、beforeTextChanged
    // 和 onTextChanged
});
```

![](img/9781284093650_CH02_FIGF09.jpg)

图 2.9 小费计算器，版本 4，在 Samsung Galaxy Tab 2 7.0 上运行

虽然这段代码乍看起来更紧凑，但我们认为它的可读性和可重用性较差，特别是当我们需要多个处理程序对象或需要将处理程序注册到多个 GUI 组件时。

如果查看此应用的完整代码，我们可以开始看到模型-视图-控制器架构的好处以及由此产生的代码组织方式，如下所示：

- ▸ 模型：`TipCalculator`类
- ▸ 视图：`activity_main.xml`
- ▸ 控制器：`MainActivity`类

随着我们开发的应用程序越来越复杂，`Model-View-Controller`架构的优势将更加明显。

## 章节总结

- 一个合理的应用程序设计涉及使用`Model-View-Controller`架构。
- `Model`是一组封装了应用程序功能的类。
- `View`是图形用户界面（GUI）。
- `Controller`是`Model`和`View`之间的中间人：它从`View`获取一些输入，更新`Model`，要求`Model`执行一些计算，并相应地更新`View`。
- Android 框架提供了多种用于构建 GUI 的组件，例如标签、按钮、文本字段、复选框、单选按钮和列表。
- 我们可以使用`activity_main.xml`文件来设置我们的 GUI，包括设置一些事件。
- 我们可以定义样式并将其应用于视图。
- 我们可以将样式作为主题应用于整个应用程序或某个活动。
- `RelativeLayout`使我们能够根据其他 GUI 组件的位置来定位 GUI 组件。
- 我们可以为`View`分配一个 id，以便稍后使用`Activity`类中的`findViewById`方法通过其 id 检索它。我们还可以在布局 XML 文件中使用组件的 id 来引用它，这在使用了`RelativeLayout`时非常有用。
- 事件驱动编程包括使用交互式组件和事件处理程序来响应用户与这些组件交互所生成的事件。
- 如果我们想要处理点击`View`的操作，可以在 XML 布局文件中为该`View`的`android:onClick`属性指定一个方法名称。然后，我们需要在相应的`Activity`类中将该方法编写为一个接受`View`参数的`void`方法。
- 通常，为了响应用户与组件的交互，我们需要编写一个处理程序类，实例化该类的对象，并将该对象注册到一个或多个组件上。
- 事件处理程序类实现一个监听器接口，并且需要重写其所有`abstract`方法。
- 事件处理程序可以实现为`private`内部类；这使得该类的成员方法可以直接访问其外部类的实例变量。事件处理程序也可以使用匿名对象或作为独立的`public`类来实现。
- 要监听`TextView`内的文本变化，我们可以实现`android.text`包中的`TextWatcher`接口。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. MVC 代表什么？
   - `Model View Code`
   - `Made View Controller`
   - `Model Visual Controller`
   - `Model View Controller`

2. GUI 组件可用于（请勾选所有适用项）：
   - 向用户显示数据
   - 让用户与应用程序交互
   - 让用户输入数据

3. 哪种布局管理器类允许我们相对于其他 GUI 组件来定位 GUI 组件？
   - `LinearLayout`
   - `AbsoluteLayout`
   - `RelativeLayout`
   - `PositionLayout`

4. `View`类位于哪个包中？
   - `javax.swing`
   - `android.widget`
   - `java.util`
   - `android.view`

5. 样式的哪个属性允许你指定一个样式继承自另一个样式？
   - `superclass`
   - `inherits`
   - `parent`
   - `baseStyle`

6. `item`的哪个属性（假设`item`元素嵌套在`style`元素内）允许你指定某些文本的颜色？
   - `android:color`
   - `android:text`
   - `android:colorText`
   - `android:textColor`

7. `application`或`activity`标签的哪个属性允许你为整个应用程序或活动指定主题？
   - `android:style`
   - `android:theme`
   - `android:@style`
   - `android:@theme`

8. 你在`colors.xml`文件中使用颜色 XML 元素定义了一个名为`myColor`的颜色。在`activity_main.xml`文件中，如何指定`EditText`元素的背景颜色将使用`myColor`颜色？
   - `android:background="@color/myColor"`
   - `android:background="@myColor"`
   - `android:background="color/myColor"`
   - `android:backgroundColor="@color/myColor"`

9. `Button`元素的哪个属性允许你指定用户点击`Button`时调用的方法？
   - `android:onPress`
   - `android:onButton`
   - `android:onClick`
   - `android:click`

10. 我们可以使用哪个类来检测`TextView`中的文本是否发生变化？
    - `TextChanger`
    - `TextWatcher`
    - `ViewWatcher`
    - `KeyListener`

### 补全代码

以下内容适用于第 11 至 15 题：

```xml
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
/>
```

11. 添加一行 XML，使显示的文本为名为`book`的字符串的值（在`strings.xml`中定义）。

12. 添加一行 XML，使`TextView`的背景颜色为`red`。

13. 添加一行 XML，使显示的文本在`TextView`元素内居中。

14. 添加一行 XML，使`TextView`在包含该`TextView`元素的`View`内垂直居中。

15. 添加一行 XML，使`TextView`使用在`styles.xml`中定义的名为`myStyle`的样式（使用 XML 元素 style）。

16. 在`colors.xml`中，编写代码定义一个名为`myColor`的颜色，该颜色为`green`。

17. 在`styles.xml`中，定义一个名为`myStyle`的样式，使`paddingBottom`为`10dp`，背景颜色为`red`。

18. 在`MainActivity.java`中，编写代码检索在`activity_main.xml`中定义的、id 为`look`的`TextView`元素，并将其赋值给一个`TextView`对象引用。

19. 我们编写了一个名为`MyWatcher`的类，它实现了`TextWatcher`接口，并声明了该类的对象如下：

    ```java
    MyWatcher mw = new MyWatcher();
    ```

    编写一条语句，将该对象注册到一个名为`myEditText`的`EditText`对象上。

### 编写应用程序

20. 修改本章的应用程序。允许用户输入客人数量，并计算小费和每位客人的总金额。

21. 编写一个执行加法运算的应用程序。它包含三个标签和一个按钮。前两个标签分别显示两个介于 1 到 10 之间的随机整数。当用户点击按钮时，两个整数相加，结果显示在第三个标签中。三个标签应使用相同的样式。按钮应具有红色背景和蓝色文本。所有四个组件应垂直居中。包含一个`Model`。

22. 编写一个执行加法运算的应用程序。它包含两个文本字段、一个标签和一个按钮。用户可以在文本字段中输入两个整数。当用户点击按钮时，两个整数相加，结果显示在标签中。两个文本字段应使用相同的样式。标签和按钮也应使用相同的样式，但与其他样式不同。每种样式至少应有四个属性。所有四个组件应垂直居中。包含一个`Model`。

23. 编写一个模拟交通灯的应用程序。它显示一个标签和一个按钮。标签表示交通灯的当前颜色，可以是红色、绿色或黄色。当用户点击按钮时，标签循环到下一个颜色，模拟交通灯运行。你应该查看`View`类的文档，了解如何以编程方式更改`View`的颜色。两个组件应垂直居中。包含一个`Model`。

24. 编写一个应用，让用户使用 RGB 颜色模型创建颜色。该应用显示三个文本字段和一个标签。我们希望用户在三个文本字段中输入 0 到 255 之间的整数（包含 0 和 255）；如果值为负数，则应转换为 0；如果大于 255，则应转换为 255。文本字段的值代表标签背景色中红色、绿色和蓝色的分量。当用户修改任意文本字段中的数字时，标签的背景色应随之更新。你需要查阅`View`类的文档，了解如何通过编程方式更改`View`的颜色。三个文本字段应具有相同的样式，且至少包含四个属性。所有四个组件应垂直居中。包含一个`Model`。

25. 编写一个应用，检查两个密码是否匹配。该应用包含两个文本字段、一个标签和一个按钮。用户可以在文本字段中输入两个密码，文本字段应具有密码样式。当用户点击按钮时，比较两个密码是否相等，并在标签中显示“THANK YOU”（如果密码匹配）或“PASSWORDS MUST MATCH”（如果密码不匹配）。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。所有四个组件应垂直居中。包含一个`Model`。

26. 编写一个应用，判断电子邮件是否有效。该应用包含一个编辑文本字段、一个标签和一个按钮。用户可以在编辑文本字段中输入其电子邮件。当用户点击按钮时，应用检查输入的电子邮件是否包含 @ 字符。如果包含，标签显示“VALID”，否则显示“INVALID”。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。文本字段和标签应位于同一水平轴上；按钮应位于它们下方并居中。包含一个`Model`。

27. 编写一个应用，评估密码的强度。该应用包含一个文本字段和一个标签；用户可以在其中输入密码。当用户输入时，标签显示“WEAK”或“STRONG”。为简单起见，我们将弱密码定义为八个字符或更少的字符串；强密码定义为九个字符或更多的字符串。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。两个组件应垂直居中。包含一个`Model`。

28. 编写一个应用，要求用户输入一个满足最低强度要求的密码。该应用包含一个文本字段和一个标签。当用户输入密码时，标签显示“VALID”或“INVALID”。在本应用中，我们将有效密码定义为八个字符或更多，且至少包含一个大写字母、一个小写字母和一个数字的字符串。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。两个组件应垂直居中。显示“VALID”或“INVALID”的标签应在用户输入时实时更新。包含一个`Model`。

29. 编写一个应用，记录一餐的卡路里。向用户提供几种食物选择；为每种食物分配一个卡路里数值。用户输入每种食物的份数后，总卡路里数随之更新。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。包含一个`Model`。

30. 编写一个应用，记录一次锻炼过程中消耗的卡路里。向用户提供几种锻炼选择；为每种锻炼分配一个卡路里数值。用户输入每种锻炼的次数后，消耗的总卡路里数随之更新。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。包含一个`Model`。

# 第三章：通过代码编写图形用户界面，布局管理器

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

有时我们想要显示的按钮（或其他组件）数量是动态的——每次运行应用时都可能不同，例如在内容应用中。内容应用是一种从外部来源（如 Facebook 或 Twitter 等网站）获取数据、显示数据并允许用户与之交互的应用。我们无法预先知道会检索到多少数据。也有可能某个应用特别适合某种数据结构，比如井字棋游戏中的 3×3 二维数组。我们可以用九个按钮实现井字棋游戏的图形用户界面部分，并且可以在`activity_main.xml`文件中定义这九个按钮，但通过代码操作一个 3×3 的按钮二维数组更为简便。

在本章中，我们将构建一个井字棋应用，并通过代码创建图形用户界面并处理事件。我们将保留自动生成的`activity_main.xml`文件不变，所有操作均通过代码完成。

## 3.1 模型-视图-控制器架构

尽管我们通过代码而非`activity_main.xml`文件来定义`View`，但我们仍然使用模型-视图-控制器架构。为了定义`View`，我们需要了解其中包含什么内容。这取决于井字棋游戏的定义和玩法；这部分内容封装在`Model`中。因此，我们先定义`Model`。

## 3.2 模型

`Model`由`TicTacToe`类组成，该类封装了井字棋游戏的功能。同样，`Model`独立于任何视觉表示。在本应用中，它实现游戏玩法并强制执行游戏规则。该类的 API 如表 3.1 所示。



示例 3.1 展示了类代码。`TicTacToe` 构造函数（第 8–11 行）在实例化二维数组 `game` 为 3×3 数组后，于第 10 行调用 `resetGame`。拥有独立的 `resetGame` 方法使我们能够在连续进行多局游戏时重用同一个对象。`resetGame`（第 80–85 行）通过将 `game` 中的所有单元格设置为 0 来清空棋盘；同时将 `turn` 设置为 1，以便玩家 1 先手。

方法 `play`（第 13–26 行）首先检查落子是否合法（第 15–16 行）。如果不合法，则返回 0（第 25 行）。如果合法，则在第 17 行更新 `game`，在第 18–21 行更新 `turn`。然后返回 `currentTurn` 的值（第 22 行），该值保存了 `turn` 的旧值（第 14 行）。

方法 `whoWon`（第 28–39 行）检查是否有玩家获胜，如果获胜则返回玩家编号；否则返回 0。我们将该逻辑分解为三个 `protected` 方法：`checkRows`（第 41–47 行）、`checkColumns`（第 49–55 行）和 `checkDiagonals`（第 57–65 行）。该类的客户端没有理由访问这些方法，因此我们将它们声明为 `protected`。

| 实例变量 | 描述 |
| --- | --- |
| `private int[ ][ ] game` | 表示棋盘的 3×3 二维数组 |
| `private int turn` | 1 = 轮到玩家 1 落子；2 = 轮到玩家 2 落子 |

| 构造函数 | 描述 |
| --- | --- |
| `TicTacToe( )` | 构造一个 `TicTacToe` 对象；清空棋盘并将 `turn` 设置为 1，准备开始游戏 |

| 公有方法 | 描述 |
| --- | --- |
| `int play( int row, int column )` | 如果落子合法且棋盘单元格未被占用，则执行落子并返回 `turn` 的旧值 |
| `boolean canStillPlay( )` | 如果棋盘上至少还有一个未被占用的单元格，则返回 `true`；否则返回 `false` |
| `int whoWon( )` | 如果玩家 `i` 获胜则返回 `i`，如果无人获胜则返回 0 |
| `boolean gameOver( )` | 如果游戏结束则返回 `true`，否则返回 `false` |
| `void resetGame( )` | 清空棋盘并将 `turn` 设置为 1 |

表 3.1 `TicTacToe` 类的 API

![](img/ch03exa01.jpg) ![](img/ch03exa01a.jpg) ![](img/ch03exa01b.jpg)

示例 3.1 `TicTacToe` 类

方法 `isGameOver`（第 76–78 行）在游戏结束时（即有人获胜或无人可下）返回 `true`；否则返回 `false`。

## 3.2 以编程方式创建 GUI，TicTacToe，版本 0

在 TicTacToe 应用的版本 0 中，我们使用空活动模板，仅设置 GUI。我们使用一个 3×3 的 `Buttons` 二维数组，以镜像模型（`TicTacToe` 类）中的 3×3 二维数组 `game`。为简单起见，我们首先将视图放在 `Activity` 类内部，因此视图和控制器位于同一个类中。在本章后面，我们将视图与控制器分离，并将它们放在两个不同的类中。

Android 框架提供了称为布局类的类，以帮助我们组织窗口内容。我们已经使用过 `RelativeLayout` 类，它是创建项目时 `activity_main.xml` 中自动使用的默认布局。这些布局类是 `abstract` 类 `ViewGroup` 的子类，而 `ViewGroup` 本身是 `View` 的子类。`ViewGroup` 是一种特殊的 `View`，可以包含其他 `Views`，这些 `Views` 称为其子视图。

表 3.2 展示了一些布局类及其描述。图 3.1 展示了这些类的层次结构。

为了在 3×3 网格中显示九个按钮，我们使用 `GridLayout`。

我们知道，Android 手机和平板电脑有多种类型，它们的屏幕尺寸可能不同。因此，硬编码小部件的尺寸和坐标是不好的做法，因为用户界面在某些 Android 设备上可能看起来不错，但在其他设备上则很差。为保持此示例简单，我们假设用户仅在竖屏模式下玩游戏；因此，我们假设设备的宽度小于其高度。

| 类 | 描述 |
| --- | --- |
| `ViewGroup` | 一个包含其他 `Views` 的 `View`。 |
| `LinearLayout` | 一种将其子视图沿单一方向（水平或垂直）排列的布局。 |
| `GridLayout` | 一种将其子视图放置在矩形网格中的布局。 |
| `FrameLayout` | 一种设计用于在屏幕上划定一个区域以显示单个项目的布局。 |
| `RelativeLayout` | 一种布局，其中 GUI 组件的位置可以相对于彼此或相对于其父级进行描述。 |
| `TableLayout` | 一种将其子视图按行和列排列的布局。 |
| `TableRow` | 一种将其子视图水平排列的布局。`TableRow` 应始终用作 `TableLayout` 的子视图。 |

表 3.2 `ViewGroup` 及其选定的子类

![](img/9781284093650_CH03_FIGF01.jpg)

图 3.1 显示一些布局类的继承层次结构

我们可以通过代码动态获取应用当前运行设备的屏幕宽度和高度。利用这些信息，我们可以调整 GUI 组件的大小，使其适合设备的屏幕，无论设备的品牌和型号如何。在设置视图时，我们执行以下步骤：

- ▸ 获取屏幕宽度
- ▸ 定义并实例化一个具有三行三列的 `GridLayout`
- ▸ 实例化 3×3 的 `Buttons` 数组
- ▸ 将九个 `Buttons` 添加到布局中
- ▸ 将 `GridLayout` 设置为此活动管理的视图的布局管理器

在示例 3.2 中，方法 `buildGuiByCode`（第 19–42 行）实现了上述步骤。

![](img/ch03exa02.jpg)

示例 3.2 `MainActivity` 类，TicTacToe 应用版本 0

| 类或接口 | 包 | 方法和字段 |
| --- | --- | --- |
| `Activity` | `android.app` | `WindowManager getWindowManager( )` |
| `WindowManager` | `android.view` | `Display getDefaultDisplay( )` |
| `Display` | `android.view` | `void getSize( Point )` |
| `Point` | `android.graphics` | `x` 和 `y` 公共实例变量 |

表 3.3 获取屏幕宽度所涉及的资源

在第 10 行，我们声明了实例变量 `buttons`，它是一个 `Buttons` 的二维数组。`Button` 类在第 6 行导入。

在第 20–23 行，我们获取屏幕宽度。在第 21 行，我们声明了一个 `Point` 变量 `size`。`Point` 类（在第 3 行导入）有两个公共实例变量 `x` 和 `y`。

在第 22 行，我们链式调用了三个方法，依次调用 `getWindowManager`、`getDefaultDisplay` 和 `getSize`。`getWindowManager` 来自 `Activity` 类，返回一个封装当前窗口的 `WindowManager` 对象。通过它，我们调用 `WindowManager` 接口的方法 `getDefaultDisplay`；它返回一个 `Display` 对象，该对象封装了当前显示器，并能提供有关其大小和密度的信息。通过它，我们调用 `Display` 类的 `getSize` 方法；`getSize` 是一个 `void` 方法，但接受一个 `Point` 对象引用作为参数。当该方法执行时，它会修改 `Point` 参数对象，并将显示器的宽度和高度赋值给其 `x` 和 `y` 实例变量。在第 23 行，我们获取屏幕宽度（`size.x`），并将其三分之一赋值给变量 `w`。稍后我们使用 `w` 的值来设置 `Buttons` 的尺寸，以便在屏幕上放置三个按钮。表 3.3 总结了获取当前设备屏幕大小所涉及的资源。

在第 25–28 行，我们定义并实例化 `GridLayout` 对象 `gridLayout`。

`GridLayout` 类属于 `android.widget` 包；我们在第 7 行导入它。在第 26 行，我们实例化一个 `GridLayout` 对象，将参数 `this` 传递给 `GridLayout` 构造函数；如表 3.4 所示，`GridLayout` 构造函数接受一个 `Context` 参数。`Context` 是一个接口，封装了关于应用环境的全局信息。如图 3.2 所示，`Activity` 类间接继承自 `Context` 类，因此 `Activity` 对象“是一个” `Context` 对象，`this` 可以用作代表应用环境的 `Context` 对象。在第 27–28 行，我们将 `GridLayout` 的列数和行数设置为 3。

在第 30–37 行，通过循环遍历数组 `buttons` 创建 `Buttons` 并将其添加到布局中。我们首先在第 31 行将 `buttons` 实例化为一个 3×3 的 `Buttons` 二维数组。第 32–37 行的双重循环实例化每个 `Button` 并将其添加到 `gridLayout` 中。第 34 行调用的 `Button` 构造函数接受一个代表应用环境的 `Context` 参数。同样，我们传递 `this`（代表当前 `Context`）作为参数。在调用方法或将其添加到 `View` 之前实例化 GUI 组件非常重要。否则，运行时会出现 `NullPointerException`，应用将停止。在第 35 行，我们使用 `addView` 方法将当前按钮添加到布局中，并指定其宽度和高度等于 `w`。`GridLayout` 类从 `ViewGroup` 继承了 `addView`。

| 构造函数 | 描述 |
| --- | --- |
| `GridLayout( Context context )` | 在由 `context` 定义的应用环境中构造一个 `GridLayout`。 |

| 公共方法 | 描述 |
| --- | --- |
| `setRowCount( int rows )` | 将网格中的行数设置为 `rows`。 |
| `setColumnCount( int cols )` | 将网格中的列数设置为 `cols`。 |
| `addView( View child, int w, int h )` | 从 `ViewGroup` 继承的方法；使用宽度 `w` 和高度 `h` 将 `child` 添加到此 `ViewGroup`。 |

表 3.4 `GridLayout` 构造函数和方法

最后，在第 40 行，我们通过调用 `Activity` 类的 `setContentView` 方法，将此活动管理的视图内容设置为 `gridLayout`。请记住，`GridLayout` 继承自 `ViewGroup`，而 `ViewGroup` 继承自 `View`；因此，`gridLayout`“是一个” `View`。

`buildGuiByCode` 方法在第 16 行被调用，位于 `onCreate` 方法内部，而 `onCreate` 方法在应用启动时自动调用。

![](img/9781284093650_CH03_FIGF02.jpg)

图 3.2 继承层次结构，展示了 `Context` 和 `Activity` 类

为了保持简单，我们只允许应用在竖屏方向下运行。在 `AndroidManifest.xml` 文件中，我们将 `activity` 标签的 `android:screenOrientation` 属性设置为 `portrait`。

图 3.3 展示了应用在模拟器中运行的情况。

至此，我们已经编写了应用的两个重要组件：模型（`TicTacToe` 类）和视图（`MainActivity` 类的 `buildGuiByCode` 方法）。接下来，我们将构建控制器。

![](img/9781284093650_CH03_FIGF03.jpg)

图 3.3 在模拟器中运行的井字棋应用，版本 0

## 3.4 事件处理：井字棋，版本 1

在版本 1 中，我们添加代码来捕获任意按钮的点击事件，识别被点击的按钮，并在被点击的按钮内放置一个 X。此时，我们并不关心游戏玩法或规则执行。这些将在版本 2 中实现。

为了捕获和处理事件，我们需要：

1. 编写一个事件处理器（一个扩展监听器接口的类）。
2. 实例化该类的对象。
3. 将该对象监听器注册到一个或多个 GUI 组件上。

示例 3.3 展示了更新后的 `MainActivity` 类，实现了上述步骤。

我们想要捕获的事件类型决定了我们要实现的监听器接口。`View.OnClickListener` 是我们应该实现的监听器接口，用于捕获和处理 `View` 上的点击事件。由于它定义在 `View` 类内部，导入 `View` 类（第 7 行）会自动导入 `View.OnClickListener`。表 3.5 列出了该接口唯一的 `abstract` 方法 `onClick`。我们的事件处理器类 `ButtonHandler` 实现了 `OnClickListener` 并重写了 `onClick`。`ButtonHandler` 作为一个 `private` 类，在第 53–61 行实现。在第 55 行，我们添加了一条输出语句，用于反馈 `onClick` 方法的 `View` 参数；我们预期它是一个 `Button`。在第 56–59 行，我们遍历 `buttons` 数组，以识别被点击按钮的行和列值。然后我们在第 59 行调用 `update` 方法，传入这些行和列值。

| 方法 | 描述 |
| --- | --- |
| `public abstract void onClick( View v )` | 当 `View` 被点击时调用；参数 `v` 是对该 `View` 的引用。 |

表 3.5 `View.OnClickListener` 接口

`update` 方法在第 48–51 行实现，但在本版本中并没有做太多事情。它输出一些关于被点击按钮的行和列的反馈（用于调试目的），并在其中写入一个 X；这在版本 2 中会有所改变。

我们在第 34 行声明并实例化一个 `ButtonHandler` 对象，并在第 39 行遍历数组时将其注册到 `buttons` 的每个元素上。此外，我们在第 38 行设置了每个按钮的文本大小，使其相对于每个按钮的大小（我们已经相对于屏幕大小进行了设置）。通过这种方式，我们尽量使应用尽可能独立于设备。在尽可能多的不同尺寸的设备上测试应用以验证尺寸和字体大小非常重要。

![](img/ch03exa03.jpg) ![](img/ch03exa03a.jpg)

示例 3.3 `MainActivity` 类，井字棋应用，版本 1

![](img/9781284093650_CH03_FIGF04.jpg)

图 3.4 在模拟器中运行的井字棋应用，版本 1

图 3.4 展示了用户连续点击三个按钮后的应用界面。图 3.5 展示了 Logcat 的部分输出，来自第 55 行和第 49 行的输出语句。它显示用户首先点击了右上角的按钮，然后点击了中间行的左侧按钮，最后点击了底行的中间按钮。图 3.5 还显示了 `onClick` 的三个 `View`（此处为 `Button`）参数的不同内存地址。

![](img/9781284093650_CH03_FIGF05.jpg)

图 3.5 Logcat 的部分输出

现在我们有了一个非常简单的控制器。它由 `onCreate` 和 `update` 方法以及 `MainActivity` 类的 `ButtonHandler` 私有类组成。请注意，在这个应用中，视图和控制器位于同一个类中。在本章后面，我们将它们放在不同的类中，以使代码更具可重用性。下一步是完成控制器的编码，以实现游戏玩法。

## 3.5 集成模型以实现游戏玩法：井字棋，版本 2

我们假设两个用户将在同一设备上相互对战。实现游戏玩法不仅仅意味着在每次轮次中在按钮网格上放置一个 X 或 O。它还意味着执行规则，例如不允许在同一网格位置重复落子，检查是否有玩家获胜，以及指示游戏是否结束。我们的模型 `TicTacToe` 类提供了这些功能。为了实现游戏，我们在 `Activity` 类中添加一个 `TicTacToe` 对象作为实例变量，并根据需要调用 `TicTacToe` 类的方法。游戏在 `update` 方法内部进行，因此我们需要修改它。我们还需要检查游戏是否结束，如果结束，则禁用所有按钮。

示例 3.4 展示了更新后的 `MainActivity` 类。在第 11 行，我们声明了一个 `TicTacToe` 对象 `tttGame`；在第 17 行实例化它。

在 `update` 方法内部（第 48–56 行），我们首先在第 49 行调用 `TicTacToe` 类的 `play` 方法，传入 `tttGame`。我们知道，如果落子合法，它返回玩家编号（1 或 2）；如果不合法，返回 0。如果落子合法且玩家是玩家 1，我们在按钮内写入 X（第 51 行）。如果落子合法且玩家是玩家 2，我们在按钮内写入 O（第 53 行）。如果落子不合法，我们不做任何操作。

当游戏结束时，我们希望禁用所有按钮。在第 58–62 行，`enableButtons` 方法在其参数 `enabled` 为 `true` 时启用所有按钮；如果为 `false`，则禁用所有按钮。我们可以通过调用 `Button` 类的 `setEnabled` 方法，传入参数 `true` 来启用 `Button`，传入 `false` 来禁用它。我们在第 54 行测试游戏是否结束，如果结束，则在第 55 行禁用所有按钮。

![](img/ch03exa04.jpg) ![](img/ch03exa04a.jpg)

示例 3.4 `MainActivity` 类，井字棋应用，版本 2

在版本 3 中，我们将添加一个状态标签，用于提供关于游戏当前状态的反馈。



图 3.6 展示了应用在模拟器中运行的情况。玩家 1 刚刚获胜，按钮已被禁用。

## 3.6 内部类

许多 Android GUI 类都是内部类或内部接口。例如，`OnClickListener` 是 `View` 类的内部接口。布局管理器类具有内部类，用于指定 `View` 子元素在其父布局中的位置。表 3.6 展示了其中一些。类名中使用的点表示法表示一个类是另一个类的内部类。例如，`GridLayout.LayoutParams` 表示 `LayoutParams` 是 `GridLayout` 的内部类。

`LayoutParams` 类都是 `public`、`static` 的内部类。

示例 3.5 展示了一个非常简单的例子，说明如何在一个类 `A` 内部定义一个 `public`、`static` 的内部类 `B`。类 `B` 在第 2–12 行定义。在第 2 行，类头将 `B` 定义为 `public` 和 `static`。它有一个构造函数（第 5–7 行）和一个 `toString` 方法（第 9–11 行）。为方便起见，我们称类 `A.B`，而不是类 `B`（`A` 的内部类）。

![](img/9781284093650_CH03_FIGF06.jpg)

图 3.6 在模拟器中运行的 `TicTacToe` 应用第 2 版——玩家 1 刚刚获胜

| 类 | 描述 |
| --- | --- |
| `ViewGroup.LayoutParams` | `LayoutParams` 类的基类 |
| `GridLayout.LayoutParams` | 与 `GridLayout` 子元素关联的布局信息 |
| `LinearLayout.LayoutParams` | 与 `LinearLayout` 子元素关联的布局信息 |
| `TableLayout.LayoutParams` | 与 `TableLayout` 子元素关联的布局信息 |
| `RelativeLayout.LayoutParams` | 与 `RelativeLayout` 子元素关联的布局信息 |

表 3.6 选定的 `LayoutParams` 类

![](img/ch03exa05.jpg)

示例 3.5 `B` 是类 `A` 的一个 `public, static` 内部类

示例 3.6 展示了一个非常简单的例子，说明如何在另一个类 `Test` 中使用类 `B`。要引用内部类，我们使用以下语法：

```text
OuterClassName.InnerClassName
```

在第 3 行，我们使用此语法声明并实例化 `b`，一个类型为 `A.B` 的对象引用。

![](img/ch03exa06.jpg)

示例 3.6 在另一个类中使用类 `A` 的 `public, static` 内部类 `B`

示例 3.6 的输出为：

```text
number: 20
```

如果 `B` 被声明为 `private` 类，那么我们只能在类 `A` 内部使用 `B`，而不能在外部使用。

如果 `B` 没有被声明为 `static`，那么我们就不能使用 `A.B` 这种语法。

如果类 `A` 的内部类 `C` 被声明为 `public` 但不是 `static`，我们可以按如下方式声明并实例化类 `C` 的对象引用（本例中使用默认构造函数）：

```java
A a = new A( );
A.C c = a.new C( );
```

## 3.7 布局参数：TicTacToe 第 3 版

我们希望通过在屏幕底部显示游戏的当前状态来改进第 2 版，如图 图 3.9 所示。

反馈消息取决于游戏的状态。让我们的模型 `TicTacToe` 类来定义消息是合理的。示例 3.7 展示了 `TicTacToe` 类的 `result` 方法（第 87–94 行）。它返回一个反映游戏状态的 `String`。

![](img/ch03exa07.jpg)

示例 3.7 `TicTacToe` 类的 `result` 方法

第 2 版中使用的 `GridLayout` 非常适合 `TicTacToe` 或任何需要二维 GUI 组件网格的 `View`。有时我们希望使用网格，并且希望灵活地合并网格中的多个单元格，并在其中放置一个组件。`GridLayout` 类允许我们将小部件跨越多个行或列，或同时跨越两者，以实现更自定义的外观和感觉。

在第 3 版中，我们使用一个四行三列的 `GridLayout`。我们将按钮放在前三行，并使用第四行放置一个跨越三列的 `TextView` 来显示游戏状态。

`ViewGroup.LayoutParams` 类允许我们指定一个 `View` 子元素在其父布局中的位置。`GridLayout.LayoutParams` 继承自 `ViewGroup.LayoutParams` 类，我们可以使用它在将 GUI 组件添加到 `GridLayout` 之前设置其布局参数。

一个 `GridLayout.LayoutParams` 对象由两个组件定义：`rowSpec` 和 `columnSpec`，两者都是 `GridLayout.Spec` 类型。`Spec` 被定义为 `GridLayout` 的一个 `public static` 内部类。因此，我们使用 `GridLayout.Spec` 来引用它。`RowSpec` 定义垂直跨度，从行索引开始并指定行数；`columnSpec` 定义水平跨度，从列索引开始并指定列数。因此，通过定义 `rowSpec`（垂直跨度）和 `columnSpec`（水平跨度），我们定义了网格中的一个矩形区域，可以在其中放置一个 `View`。

我们可以使用 `GridLayout.Spec` 类的 `static spec` 方法来创建和定义一个 `GridLayout.Spec` 对象，该对象定义了一个跨度。一旦我们定义了两个 `GridLayout.Spec` 对象，就可以使用它们来定义一个 `GridLayout.LayoutParams` 对象。表 3.7 展示了这些方法。

| `GridLayout` 类的选定方法 |
| --- |
| 1. `public static GridLayout.Spec spec( int start, int size )`<br>   1. 返回一个 `GridLayout.Spec` 对象，其中 `start` 是起始索引，`size` 是大小。<br>2. `public static GridLayout.Spec spec( int start, int size, GridLayout.Alignment alignment )`<br>   1. 返回一个 `GridLayout.Spec` 对象，其中 `start` 是起始索引，`size` 是大小。<br>      `Alignment` 是对齐方式；常见值包括 `GridLayout.TOP`、`GridLayout.BOTTOM`、`GridLayout.LEFT`、`GridLayout.RIGHT`、`GridLayout.CENTER`。 |

| `GridLayout.LayoutParams` 类的构造函数 |
| --- |
| 1. `GridLayout.LayoutParams( Spec rowSpec, Spec columnSpec )`<br>   1. 使用 `rowSpec` 和 `columnSpec` 构造一个 `LayoutParams` 对象。 |

表 3.7 `GridLayout` 和 `GridLayout.LayoutParams` 类的方法

图 3.7 展示了一个 4 × 6 的单元格网格。阴影区域可以定义如下：

- 垂直跨度从索引 1 开始，大小为 2。
- 水平跨度从索引 2 开始，大小为 4。

我们可以为阴影区域定义一个 `GridLayout.LayoutParams` 对象，如下所示：

```java
// 垂直跨度
GridLayout.Spec rowSpec = GridLayout.spec( 1, 2 );
// 水平跨度
GridLayout.Spec columnSpec = GridLayout.spec( 2, 4 );
GridLayout.LayoutParams lp
    = new GridLayout.LayoutParams( rowSpec, columnSpec );
```

注意，如果我们包含以下导入语句，则可以使用 `Spec` 代替 `GridLayout.Spec`：

```java
import android.widget.GridLayout.Spec;
```

以及：

```java
import android.widget.GridLayout;
```

图 3.8 展示了一个 4 × 3 的单元格网格，类似于我们应用中的网格。阴影区域可以定义如下：

- 垂直跨度从索引 3 开始，大小为 1。
- 水平跨度从索引 0 开始，大小为 3。

![](img/9781284093650_CH03_FIGF07.jpg)

图 3.7 一个 4 × 6 网格中的区域，由垂直跨度（`start = 1, size = 2`）和水平跨度（`start = 2, size = 4`）定义

![](img/9781284093650_CH03_FIGF08.jpg)

图 3.8 一个 4 × 3 网格中的区域，由垂直跨度（`start = 3, size = 1`）和水平跨度（`start = 0, size = 3`）定义

我们为阴影区域定义一个 `GridLayout.LayoutParams` 对象，如下所示：

```java
GridLayout.Spec rowSpec = GridLayout.spec( 3, 1 );
GridLayout.Spec columnSpec = GridLayout.spec( 0, 3 );
GridLayout.LayoutParams lp
    = new GridLayout.LayoutParams( rowSpec, columnSpec );
```

我们在示例 3.8 的第 48–53 行使用了与上述类似的代码来定义 `status` 的布局参数。在第 54 行，我们通过调用 `setLayoutParams` 来设置它们。在第 34 行，我们将 `GridLayout` 的行数设置为四，以便将 `status` 放在第四行。在第 57–58 行，我们设置了 `status` 的高度和宽度，使其完全填充由其布局参数定义的网格区域。注意，可以将组件的高度和宽度设置得与其布局参数不同。然后我们可以使用带三个参数的 `spec` 方法来设置组件相对于其定义布局参数的对齐方式。表 3.7 展示了 `spec` 方法第三个参数的一些可能值。

在第 59–62 行，我们分别将 `status` 中的文本居中，将其背景颜色设置为绿色，设置其文本字体大小，并根据 `tttGame` 的状态设置其文本内容。

我们在 `update` 方法的第 77 行和第 79 行添加了代码，以便在游戏结束时更改 `status` 的颜色和文本。

![](img/ch03exa08.jpg) ![](img/ch03exa08a.jpg) ![](img/ch03exa08b.jpg)

示例 3.8 `MainActivity` 类，TicTacToe 应用第 3 版

![](img/9781284093650_CH03_FIGF09.jpg)

图 3.9 井字棋应用，版本 3，在模拟器中运行

图 3.9 展示了应用在模拟器中运行的情况，屏幕底部显示了游戏状态。

## 3.8 警告对话框：井字棋，版本 4

在版本 4 中，我们让玩家在当前游戏结束后能够再玩一局。游戏结束时，我们希望弹出一个对话框，询问用户是否想再玩一次。如果回答是，则可以再玩一局；如果回答否，则退出活动（在本例中即退出应用，因为只有一个活动）。

`AlertDialog.Builder` 类（属于 `android.app` 包）提供了弹出对话框的功能。它为用户提供多个选项，并捕获用户的回答。`AlertDialog.Builder` 类型的对话框最多可以包含三个按钮：否定按钮、中性按钮和肯定按钮。在本应用中，我们只使用其中两个：肯定按钮和否定按钮。通常，这两个按钮对应的是用户的“是”或“否”回答，尽管并非必须如此。表 3.8 展示了 `AlertDialog.Builder` 的构造函数以及该类的其他方法。

**`AlertDialog.Builder` 类的构造函数**

1. `public AlertDialog.Builder( Context context )`
   - 为上下文参数构造一个 `AlertDialog.Builder` 对话框对象。

**`AlertDialog.Builder` 类的方法**

1. `public AlertDialog.Builder setMessage( CharSequence message )`
   - 将显示的消息设置为 `message`；返回此 `AlertDialog.Builder` 对象，允许链式调用。
2. `public AlertDialog.Builder setTitle( CharSequence title )`
   - 将警告框的标题设置为 `title`；返回此 `AlertDialog.Builder` 对象，允许链式调用。
3. `public AlertDialog.Builder setPositiveButton( CharSequence text, DialogInterface.OnClickListener listener )`
   - 设置当用户点击肯定按钮时要调用的监听器；将肯定按钮的文本设置为 `text`。
4. `public AlertDialog.Builder setNegativeButton( CharSequence text, DialogInterface.OnClickListener listener )`
   - 设置当用户点击否定按钮时要调用的监听器；将否定按钮的文本设置为 `text`。
5. `public AlertDialog.Builder setNeutralButton( CharSequence text, DialogInterface.OnClickListener listener )`
   - 设置当用户点击中性按钮时要调用的监听器；将中性按钮的文本设置为 `text`。
6. `public AlertDialog.Builder show( )`
   - 创建并返回一个 `AlertDialog` 框，并显示它。

表 3.8 `AlertDialog.Builder` 类的选定构造函数和方法

示例 3.9 展示了更新后的 `MainActivity` 类。在 `showNewGameDialog` 方法（第 98–106 行）中，我们在第 99 行声明并实例化了一个 `AlertDialog.Builder` 对象 `alert`，传入 `this`（当前 `MainActivity` 对象）。`MainActivity` 继承自 `Activity`，而 `Activity` 继承自 `Context`；因此，`this`“是一个”`Context` 对象。为了显示对话框，我们在第 105 行调用了 `show` 方法。如果不调用 `show` 方法，对话框就不会显示。然而，显示一个没有按钮供用户交互的对话框，会导致出现一个带有标题和消息但无法关闭的对话框。在本应用中，我们想询问用户是否要再玩一局，因此只包含肯定和否定按钮。

中性、肯定或否定按钮可以通过调用 `AlertDialog.Builder` 的 `setPositiveButton`、`setNegativeButton` 和 `setNeutralButton` 方法来添加。这三个方法都接受两个参数。第一个参数是一个 `CharSequence` 或一个表示按钮内显示字符串的 `int` 资源 ID。第二个参数是 `DialogInterface.OnClickListener` 接口类型的对象。

因此，我们需要实现 `DialogInterface.OnClickListener` 接口，以便声明并实例化该类型的对象，并将其作为这三个方法的第二个参数传递。我们将其实现为一个 `private` 类，以便能够访问 `MainActivity` 类的实例变量和方法，特别是对象 `tttGame` 以及将 `Buttons` 和 `TextView` 重置为初始状态的方法。`private` 类 `PlayDialog`（第 117–128 行）实现了 `DialogInterface.OnClickListener`。

![](img/ch03exa09.jpg) ![](img/ch03exa09a.jpg) ![](img/ch03exa09b.jpg)

示例 3.9 `MainActivity` 类，井字棋应用，版本 4

`DialogInterface.OnClickListener` 接口包含一个 `abstract` 方法 `onClick`，我们在第 118–127 行重写了它。`onClick` 方法的第二个参数 `id`（`int` 类型）包含了用户点击了哪个按钮的信息。如果值为 -1，表示用户点击了肯定按钮；如果值为 -2，表示用户点击了否定按钮。

在第 119 行，我们测试 `id` 的值是否为 -1。如果是，我们通过调用 `tttGame` 的 `resetGame` 方法（第 120 行）将 `tttGame` 的实例变量重置为初始值，在第 121 行启用按钮，在第 122 行清除所有按钮的文本，并在第 123–124 行更新 `status` 的背景颜色和文本。`enableButtons` 和 `resetButtons` 方法（分别在第 86–90 行和第 92–96 行）用于启用或禁用九个按钮，以及将它们的文本内容重置为空字符串。如果 `id` 的值为 -2，我们通过调用 `finish` 方法（第 126 行）退出活动。注意，表达式 `this.finish()` 是不正确的，因为此时 `this` 指向当前的 `PlayDialog` 对象（因为我们位于该类内部）。由于我们想用 `MainActivity` 类的当前对象调用 `finish` 方法，因此使用 `MainActivity.this` 来访问它。

图 3.10 展示了游戏结束时的应用状态，状态信息显示玩家 1 获胜，并询问用户是否再玩一局。

## 3.9 分离视图与控制器：井字棋，版本 5



在版本 5 中，我们将视图与控制器分离。这样可以使视图可重用。控制器是视图与模型之间的中间人，因此我们保持视图独立于模型。

在视图中，除了创建视图的代码外，我们还提供了以下方法：

- ▸ 更新视图。
- ▸ 从视图获取用户输入。

这与模型类类似，模型类提供了检索其状态和更新状态的方法。

在控制器中，除了模型的一个实例变量外，我们还添加了视图的一个实例变量。通过它，我们可以调用视图的各种方法来更新视图并从中获取用户输入。

按钮数组和`TextView`状态现在位于视图内部。更新视图意味着更新按钮和`TextView`状态。为此，我们提供了以下方法：

- ▸ 设置特定按钮文本的方法。
- ▸ 设置`TextView status`文本的方法。
- ▸ 设置`TextView status`背景颜色的方法。
- ▸ 将所有按钮文本重置为空字符串的方法（开始新游戏时需要）。
- ▸ 启用或禁用所有按钮的方法（开始新游戏时也需要）。

![](img/9781284093650_CH03_FIGF10.jpg)

图 3.10 井字棋应用，版本 4，在模拟器中运行，显示游戏结束时的警告对话框。

该视图的用户输入是点击其中一个按钮。通常，事件处理在控制器中执行。因此，我们提供了一个方法来检查某个特定按钮是否被点击。

示例 3.10 展示了`ButtonGridAndTextView`类，即该应用第 5 版的视图。在第 4 版中，我们的视图是一个`GridLayout`，因此`ButtonGridAndTextView`类`extends GridLayout`（第 10 行），从而它“是”一个`GridLayout`。我们拥有三个实例变量（第 11–13 行）：

- ▸ `buttons`，一个二维的`Button`数组。
- ▸ `status`，一个`TextView`。
- ▸ `side`，一个`int`，表示`buttons`的行数和列数。

![](img/ch03exa10.jpg) ![](img/ch03exa10a.jpg)

示例 3.10 `ButtonGridAndTextView`类，TicTacToe 应用，第 5 版。

因为我们希望保持视图与模型独立，所以没有使用`TicTacToe`类的`SIDE`常量来确定`buttons`的行数和列数。相反，`side`实例变量存储了该值。构造函数包含一个参数`newSide`，它被赋值给`side`（第 15–16 行和第 18 行）。当从控制器创建视图时，我们可以访问模型，因此我们将传入`TicTacToe`类的`SIDE`常量，以便将其赋值给`side`。`ButtonGridAndTextView`构造函数还包含另外三个参数：一个`Context`、一个`int`和一个`View.OnClickListener`。`Context`参数用于实例化视图的控件（`Button`和`TextView`）。由于`Activity`类继承自`Context`，因此一个`Activity`“是”一个`Context`。所以，当从控制器创建`ButtonGridAndTextView`时，我们可以将`this`作为`Context`参数传入。我们在第 27 行和第 35 行将该`Context`参数传递给`Button`和`TextView`的构造函数。`int`参数表示视图的宽度。通过将宽度作为参数，我们让`Activity`客户端决定视图的尺寸。我们在第 18 行将`newSide`参数赋值给`side`。最后，`View.OnClickListener`参数使我们能够设置事件处理。我们希望由控制器处理事件，但`Button`位于视图中，因此需要在视图中设置事件处理。我们在第 29 行完成此操作。通过测试`newSide`和`width`是否为正数，可以使构造函数代码更加健壮。这留作练习。

在第 30 行和第 49 行，我们将每个`Button`和`TextView`添加到此`ButtonGridAndTextView`中。

`setStatusText`、`setStatusBackgroundColor`、`setButtonText`、`resetButtons`和`enableButtons`方法为视图的客户端（控制器）提供了更新视图的能力。`isButton`方法（第 64–66 行）使视图的客户端（控制器）能够将一个`Button`与由行和列标识的`buttons`数组中的`Button`进行比较。从控制器中，我们将调用该方法来识别被点击的`Button`的行和列。

示例 3.11 展示了更新后的`MainActivity`类。在第 14 行声明了一个`ButtonGridAndTextView`实例变量`tttView`，并在第 24 行实例化。在`onClick`内部（第 40–58 行），我们首先在第 43 行识别哪个按钮被点击，然后根据轮到谁下棋，在第 46 行和第 48 行调用`setButtonText`来更新视图。如果游戏结束（第 49 行），我们通过在第 50 行和第 52 行调用`setStatusBackgroundColor`和`setStatusText`方法来相应地更新视图。我们还在第 51 行禁用了按钮。

![](img/ch03exa11.jpg) ![](img/ch03exa11a.jpg) ![](img/ch03exa11b.jpg)

示例 3.11 `MainActivity`类，TicTacToe 应用，第 5 版。

通过将视图与控制器分离，我们使视图可重用。

## 章节总结

- 要创建 GUI，我们可以使用 XML 或通过编程方式实现。对于某些应用，控件数量是动态的，我们必须通过编程方式实现。对于其他一些应用，虽然可以使用 XML，但通过编程方式可能更方便。
- Android 框架提供了布局管理器来帮助我们组织`View`。
- 布局管理器是`ViewGroup`的子类。
- `addView`方法将一个子`View`添加到`ViewGroup`中。
- 使用`getWindowManager`和`getDefaultDisplay`方法，我们可以获取当前设备显示的特性，特别是其宽度和高度。
- 我们可以使用屏幕尺寸来适当调整 GUI 组件的大小，从而使外观和感觉与设备无关。
- 我们可以实现`View.OnClickListener`接口来处理`View`（例如`Button`）上的点击事件。如果这样做，我们需要实现其`onClick`方法。
- 我们可以为`View`指定布局参数，以便在将`View`添加到其父`ViewGroup`时正确定位。
- `GridLayout`将其子元素放置在矩形网格中。
- `GridLayout`提供了跨多行或多列放置组件的灵活性。
- 我们可以使用`AlertDialog.Builder`类和`DialogInterface.OnClickListener`接口来构建一个警告框。
- 我们可以调用`finish`方法来关闭一个活动。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. 如何导入`View.OnClickListener`（如果我们想使用类似`View.OnClickListener listener;`的代码）？
   - 导入`View`类就足够了。
   - 它是自动导入的。
   - 我们必须导入`View.OnClickListener`；
   - 我们必须导入`OnClickListener`；

2. `View.OnClickListener`的抽象方法名称是什么？
   - `listen`
   - `click`
   - `onClick`
   - `clickListen`

3. 我们使用`ViewGroup`类的哪个方法将子`View`添加到父`View`中？
   - `addChild`
   - `addView`
   - `moreView`
   - `newView`

4. 我们在私有类`Y`中编码，该类编码在公有类`X`内部。如何访问`Y`类的当前对象？
   - `this`
   - `X.this`
   - `Y.this`
   - `this.X`

5. 我们在私有类`Y`中编码，该类编码在公有类`X`内部。如何访问`X`类的当前对象？
   - `this`
   - `X.this`
   - `Y.this`
   - `this.X`

6. 如何获取屏幕尺寸（假设`size`是一个`Point`对象引用）？
   - `getWindowManager().getSize();`
   - `getDefaultDisplay().getSize();`
   - `getWindowManager().getDefaultDisplay().getSize(size);`
   - `getWindowManager().getDefaultDisplay().getSize();`

7. 在代码`GridLayout gridLayout = new GridLayout(this)`中，`this`的数据类型是什么？
   - `GridLayout`
   - `Context`
   - `Grid`
   - `View`

8. 我们使用`GridLayout`类的哪个方法来设置网格的行数？
   - `setRows`
   - `setRowCount`
   - `setCount`
   - `numberOfRows`

9. 我们使用`Activity`类的哪个方法来设置活动的视图？
   - `setLayout`
   - `setContentView`
   - `setView`
   - `view`

10. 在`Activity`类内部，如何实例化一个按钮？
    - `Button b = new Activity();`
    - `Button b = new Button();`
    - `Button b = new Button(this);`
    - `Button b = new Button(Activity);`

11. 视图使用哪个类来告诉其父视图它们希望如何被布局？
    - `Layout`
    - `Params`
    - `ViewParams`
    - `LayoutParams`

12. 我们使用哪个方法来指定`TextView`中文本的对齐方式？
    - `setAlignment`
    - `center`
    - `setGravity`
    - `align`

### 补全代码

13. 将当前屏幕的宽度赋值给变量`width`。

```
// 在此处编写代码
```

14. 以下代码在当前上下文中创建一个`GridLayout`，并将其行数设置为四，列数设置为二。

```
// 在此处编写代码
```

15. 以下代码在当前上下文中创建一个按钮。

```
// 在此处编写代码
```

16. 以下代码在当前上下文中创建一个 5 × 2 的二维按钮数组。

```
// 你的代码写在这里
```

17. 这段代码向已创建的`GridLayout`对象`gl`中添加了一个名为`b`的`Button`对象，并将其宽度和高度均指定为 200 像素。

```
// 你的代码写在这里
```

18. 这段代码为下方的阴影区域定义了一个`GridLayout.LayoutParams`对象。

```
// 你的代码写在这里
```

![](img/9781284093650_CH03_UNNUN01.jpg)

19. 这段代码为下方的阴影区域定义了一个`GridLayout.LayoutParams`对象。

```
// 你的代码写在这里
```

![](img/9781284093650_CH03_UNNUN02.jpg)

20. 这段代码为当前活动设置了一个警告视图。它将标题设置为 HELLO，将消息设置为 HAVE FUN。

```
AlertDialog.Builder alert = new AlertDialog.Builder( this );
// 你的代码从这里开始
PlayDialog pd = new PlayDialog( );
alert.setPositiveButton( ”YES”, pd );
alert.setNegativeButton( ”NO”, pd );
// 并在此处继续，以便显示警告视图
```

21. 这段代码检查被点击的按钮是否名为`b`。如果是，则向 Logcat 输出 YES，否则输出 NO。

```
private class ButtonHandler implements View.OnClickListener {
  public void onClick( View v ){
    // 你的代码写在这里
  }
}
```

### 编写一个应用

22. 编写一个应用，显示一个标签和一个按钮。每次用户点击按钮时，标签在可见与不可见之间切换。不要使用 XML。

23. 编写一个应用，包含三个标签和一个按钮。三个标签代表一个交通信号灯。应用启动时，只有红色背景的标签显示。用户点击按钮时，只有黄色背景的标签显示。再次点击按钮时，只有绿色背景的标签显示。再次点击按钮时，只有红色背景的标签显示……如此循环。不要使用 XML。

24. 编写一个应用，显示一个标签和一个按钮。标签代表交通信号灯的当前颜色，可以是红色、黄色或绿色。用户点击按钮时，标签循环到下一个颜色，模拟交通信号灯运行。不要使用 XML。

25. 编写一个应用，显示一个标签和一个按钮。每次用户点击按钮时，标签向下移动 10 像素。当标签到达屏幕底部时，用户点击按钮后标签不再移动。不要使用 XML。

26. 编写一个应用，显示两个标签和一个按钮。第一个标签显示一个 50 到 100 之间的随机整数。用户点击按钮时，第二个标签移动到其 y 坐标等于第一个标签中显示的整数的位置。不要使用 XML。

27. 编写一个应用，包含一个文本字段、一个标签和一个按钮。用户可以在文本字段中输入其电子邮件。用户点击按钮时，应用检查输入的电子邮件是否包含`@`字符以及`@`字符之后的某个位置有一个点。如果是，标签显示 VALID，否则显示 INVALID。文本字段和标签应各自拥有独立的样式，每个样式至少包含四个属性。包含一个`Model`。不要使用 XML。

28. 编写一个应用，包含一个文本字段和一个标签。用户输入其密码。当用户输入时，标签显示 WEAK 或 STRONG。对于本应用，我们定义弱密码为八个或更少字符，强密码为九个或更多字符。包含一个`Model`。不要使用 XML。

29. 编写一个应用，在网格上显示一个带有黑白棋子的棋盘。你可以用一两个字母表示每个棋子，例如 P 代表兵，Q 代表后，R 代表车，K 代表马，B 代表象，KG 代表王。当用户点击一个马时，将马可以移动到的格子标记为绿色。包含一个`Model`。不要使用 XML。

30. 编写一个应用，显示四个标签和一个按钮。前两个标签代表简化版二十一点游戏中的两张牌，并填充两个 1 到 11（含）之间的随机整数。两者的总和显示在第四个标签内。用户点击按钮时，如果第四个标签中显示的当前总和小于等于 15，则第三个标签填充一个 1 到 11（含）之间的随机数，并且第四个标签内的总和更新为标签一、二、三中三个数字的总和。如果第四个标签中显示的当前总和大于 15，则不执行任何操作。包含一个`Model`。不要使用 XML。

# 第四章：多个活动、活动间传递数据、过渡、持久化数据

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

大多数应用涉及多个屏幕的使用。在本章中，我们将学习如何编写多个活动、如何从一个活动导航到另一个活动并返回、如何在活动之间共享数据、如何设置它们之间的过渡，以及如何保存应用的状态并在用户再次启动应用时恢复它（即如何使数据持久化）。我们将构建一个抵押贷款计算器应用，以此作为学习所有这些概念的载体。

我们将探索两种布局管理器：第一个屏幕使用`TableLayout`，第二个屏幕使用`RelativeLayout`。在第二个屏幕中，我们将探索更多的 GUI 组件：单选按钮，用于显示互斥的选择项。

## 4.1 模型：抵押贷款类

本应用的模型是`Mortgage`类，它封装了一笔抵押贷款。典型的抵押贷款有三个参数：贷款金额、利率和贷款年限。为简化起见，我们假设利率参数为年利率，并按月复利计算；同时假设每月还款额固定。表 4.1 显示了资金流向。M 是我们在时间 0 从银行收到的贷款金额。P 是我们每月向银行支付的还款额，从第 1 个月开始，到第 n*12 个月结束，其中 n 是年数。

如果 r 是年利率，则`mR = r/12`是月利率。所有月还款额按月利率`mR`折现后的现值等于贷款金额`M`。因此，我们得到`M`与`P`、`mR`和`n`之间的如下等式。

![](img/ch04eq001.gif)

设`a = 1/(1 + mR)`；因此，我们有：

![](img/ch04eq002.gif)

| 月份 | 0 | 1 | 2 | 3 | 4 | . . . | . . . | `n*12 — 1` | `n*12` |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|



| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 贷款 | M |   |   |   |   |   |   |   |   |
| 还款 |   | P | P | P | P | . . . |   | P | P |

表 4.1 贷款金额为 M、期限为 n 年、月还款额为 P 的抵押贷款月度现金流

- `M = P((–1 + a + 1 – a ^(n*12 + 1))/(1 – a)) = P(a – a ^(n*12 + 1))/(1 – a)`
  - `M = P a(1 – a ^(n*12))/(1 – a)) = P(1 – a^(n*12))a/(1 – a)`
    - `1 – a = 1 – 1 /(1 + mR) = mR(1 + mR)`

因此，`a/(1 – a) = 1/mR`

于是，`M = P(1 – a ^(n*12))/mR`；我们的月还款额公式为：

`P = mR * M/(1 – a ^(n*12))`，其中 `a = 1/(1+mR)`。

示例 4.1 展示了 `Mortgage` 类，包括它的三个实例变量 `amount`、`years` 和 `rate`（第 9–11 行）、构造方法（第 13–17 行）、修改器（第 19–32 行）以及访问器（第 34–36 行、第 42–44 行和第 46–48 行）。`monthlyPayment` 方法位于第 50–54 行。我们包含了一个 `DecimalFormat` 常量 `MONEY`（第 6–7 行），以便用美元符号和两位小数格式化抵押贷款金额、每月还款额和总还款额。方法 `getFormattedAmount`（第 38–40 行）、`formattedMonthlyPayment`（第 56–58 行）和 `formattedTotalPayment`（第 64–66 行）分别返回 `amount`、每月还款额和总还款额的字符串表示。`DecimalFormat` 类属于 `java.text` 包，在第 3 行被导入。我们选择不为利率提供格式化方法，因为我们希望在应用中显示其精确值。

![](img/ch04exa01a.jpg) ![](img/ch04exa01b.jpg)

示例 4.1 `Mortgage` 类

## 4.2 使用 `TableLayout` 构建前端屏幕 GUI：抵押贷款计算器应用，版本 0

我们为此应用使用空活动模板。该应用的模型-视图-控制器中的视图部分由两个屏幕组成。第一个屏幕显示抵押贷款的特征：金额、年限、利率、每月还款额以及整个贷款期间的总还款额。用户不与此屏幕交互，它是只读的。我们希望将所有信息显示为一个六行两列的表格。对于前五行中的每一行，第一列是描述第二列所显示数据的标签。最后一行是一个按钮，允许用户转到另一个屏幕以更新抵押贷款金额、年限和利率的数据。图 4.1 显示了该应用版本 0 在环境中的预览。

我们使用 `TableLayout` 来管理应用的第一个屏幕。`TableLayout` 将其子元素按行和列排列。它通常包含 `TableRow` 元素，每个元素定义一行。列数最多的行决定了布局的列数。单元格定义为一行中跨越一列或多列的矩形区域。我们也可以使用 `View` 或其子类代替 `TableRow`，此时该 `View` 将跨越整行。`TableLayout` 除了从父类（如 `LinearLayout`、`ViewGroup` 和 `View`）继承的属性外，几乎没有自己的 XML 属性。图 4.2 显示了继承层次结构。

![](img/9781284093650_CH04_FIGF01.jpg)

图 4.1 抵押贷款计算器应用版本 0 的预览

![](img/9781284093650_CH04_FIGF02.jpg)

图 4.2 `TableLayout` 和 `TableRow` 的继承层次结构

我们希望为 `TableLayout` 和 `RelativeLayout` 都使用 16 像素的标准边距。因此，我们修改 `dimens.xml` 文件，创建一个名为 `activity_margin` 的 `dimen` 元素，其值为 `16dp`，如示例 4.2 所示。

![](img/ch04exa02.jpg)

示例 4.2 `dimens.xml` 文件

示例 4.3 展示了 `activity_main.xml` 文件，它使用 `TableLayout` 定义了包含六个 `TableRow` 元素的 GUI。在第 7 行，我们使用之前在 `dimens.xml` 中定义的 `dimen` 元素 `activity_margin`，为 `TableLayout` 指定了 16 像素的边距。前三行定义在第 10–19 行、第 21–30 行和第 32–41 行，显示了抵押贷款参数。每行包含两个 `TextView` 元素；第一个是描述性标签，第二个显示相应数据。对于每个新 `TableRow` 元素中的第一个 `TextView` 元素，我们指定了 10 dip 的内边距（第 15、26、37 行），以将新行中的 GUI 组件与上方元素和屏幕左边缘隔开。我们使用在 `strings.xml` 文件（示例 4.4）中定义的 `Strings`（第 14、18、25、29、36、40 行）为所有这些 `TextView` 元素分配文本。我们在 `strings.xml` 中为抵押贷款参数使用了默认值 $100000、30 年和 3.5%；相应的每月还款额为 $449.04，30 年总还款额为 $161654.66。由于我们打算稍后通过代码更新第二列中 `TextView` 元素内的文本，我们为每个元素分配了一个 id（第 17、28、39 行），以便使用 `findViewById` 方法检索它们。`findViewById` 方法返回一个引用，指向其 id 为该方法参数的 GUI 组件。

![](img/ch04exa03.jpg) ![](img/ch04exa03a.jpg)

示例 4.3 `activity_main.xml` 文件

在第 43–46 行，我们插入了一个高度为 5 像素、颜色为红色的 `View` 元素。这定义了一个细长的红色矩形，横跨屏幕宽度，显示为一条红线。这使我们能够将显示抵押贷款参数的屏幕顶部区域与显示计算数据（即每月还款额和总还款额）的屏幕底部区域分隔开。这些数据显示在接下来的两行中。这两行的 XML 代码与前两行类似，使用了相同的内边距、一些来自 `strings.xml` 的 `Strings` 以及 id。

最后一行显示一个按钮。由于该行只有一个元素，我们在第 73 行使用值为 `center` 的 `android:gravity` 属性将该行居中。我们在第 74 行为该行上方指定了 50 dip 的内边距，以更好地将按钮与上一行分隔开。在第 77 行，我们指定 `modifyData` 作为用户点击按钮时调用的方法。

![](img/ch04exa04.jpg)

示例 4.4 `strings.xml` 文件

我们希望所有元素的字体大小都大于默认字体大小，因此我们在 `styles.xml` 文件（示例 4.5）的第 3 行指定了 22sp 的文本大小。这个字体大小可能在某些 Android 设备上效果良好，而在其他设备上则不然，但我们在此应用中不担心这个问题——我们将在本书后面讨论该主题。第 2 行的 `AppTheme` 样式是在 `AndroidManifest.xml` 文件中指定的应用默认主题。

![](img/ch04exa05.jpg)

示例 4.5 `styles.xml` 文件

为了保持此应用简单，我们只允许应用在竖屏方向运行。因此，在 `AndroidManifest.xml` 文件中，我们向 `activity` 元素添加了一个 `android:screenOrientation` 属性，并将其值设置为 `portrait`。

## 4.3 使用 `RelativeLayout` 构建第二个屏幕 GUI

应用视图部分的第二个组件是第二个屏幕。它允许用户更改三个抵押贷款参数：金额、年限和利率。我们借此机会探索单选按钮，用于选择抵押贷款的年限。

当我们首次创建项目时，它会自动创建一个 `Activity` 类及其 GUI 的 XML 文件（默认名称为 `MainActivity` 和 `activity_main.xml`）。由于我们正在为应用添加第二个屏幕，我们添加另一个 XML 文件 `activity_data.xml` 来定义其 GUI，以及另一个 `Activity` 类 `DataActivity` 来控制它。请确保在 `res/layout` 目录中创建 `activity_data.xml` 文件，并且文件名中不要使用大写字母。如果需要在文件名中分隔名词，我们使用下划线字符。

对于第二个屏幕的 GUI，我们使用 `RelativeLayout` 类，它是 `ViewGroup` 的子类，如图 4.2 所示。它使我们能够相对于其他组件定位组件。

`RelativeLayout` 类有一个名为 `LayoutParams` 的 `public static` 内部类（我们使用 `RelativeLayout.LayoutParams` 来引用它），其中包含许多专门用于将元素彼此相对排列的 XML 属性。这些属性使我们能够将一个 `View` 相对于屏幕上的另一个 `View` 进行定位。为了引用另一个 `View`，我们可以为该 `View` 分配一个 id，并使用该 id 来引用它。我们也可以将一个 `View` 相对于其父 `View` 进行定位，在这种情况下，我们不需要通过 id 来引用父 `View`。其中一些属性列在表 4.2 中。列出的前八个属性（从 `android:layout_alignLeft` 到 `android:layout_toRightOf`）期望其值为某个 `View` 的 id。

例如，在示例 4.6 的第 15 行，我们使用了以下代码：

```xml
android:layout_toRightOf="@+id/label_years"
```

以指定单选按钮组位于 id 为 `label_years` 的 `View` 的右侧。该 `View` 是一个 `TextView`，定义在第 8–12 行，其 id 在第 9 行指定。

在第 18 行，我们使用了以下代码：

```xml
android:layout_alignLeft="@+id/data_rate"
```

以进一步定义单选按钮组的位置。这指定了它与 id 为 `data_rate` 的 `View` 左对齐。该 `View` 是一个 `EditText`，定义在第 67–76 行，其 id 在第 68 行定义。

因此，当我们使用 `RelativeLayout` 时，通常会为许多 `View` 元素分配 id，以便在定义其他 `View` 元素相对于它们的位置时引用它们。

我们可以使用表 4.2 中列出的最后四个属性来将一个 `View` 相对于其父 `View` 进行定位。属性 `android:layout_alignParentLeft` 和 `android:layout_alignParentRight` 涉及垂直对齐，而 `android:layout_alignParentBottom` 和 `android:layout_alignParentTop` 涉及水平对齐。

| XML 属性 | 描述 |
| --- | --- |
| `android:layout_alignLeft` | `View` 的左边缘与指定视图的左边缘对齐。 |
| `android:layout_alignRight` | `View` 的右边缘与指定视图的右边缘对齐。 |
| `android:layout_alignBottom` | `View` 的底边缘与指定视图的底边缘对齐。 |
| `android:layout_alignTop` | `View` 的顶边缘与指定视图的顶边缘对齐。 |
| `android:layout_above` | `View` 位于指定视图的上方。 |
| `android:layout_below` | `View` 位于指定视图的下方。 |
| `android:layout_toLeftOf` | `View` 位于指定视图的左侧。 |
| `android:layout_toRightOf` | `View` 位于指定视图的右侧。 |
| `android:layout_alignParentLeft` | 如果为 true，视图的左边缘与其父视图的左边缘对齐。 |
| `android:layout_alignParentRight` | 如果为 true，视图的右边缘与其父视图的右边缘对齐。 |
| `android:layout_alignParentBottom` | 如果为 true，视图的底边缘与其父视图的底边缘对齐。 |
| `android:layout_alignParentTop` | 如果为 true，视图的顶边缘与其父视图的顶边缘对齐。 |

表 4.2 `RelativeLayout.LayoutParams` 中有用的 XML 属性

![](img/ch04exa06.jpg) ![](img/ch04exa06a.jpg) ![](img/ch04exa06b.jpg)

示例 4.6 `activity_data.xml` 文件

在第 54 行，我们使用了以下代码：

```xml
android:layout_alignParentRight="true"
```

以指定 `EditText` 应与它的父视图（即 `RelativeLayout`）右对齐，而 `RelativeLayout` 本身是一个 `View`，在此情况下它占据了整个屏幕；这意味着 `EditText` 的右边缘应与屏幕的右边缘垂直对齐。

在第 81 行，我们将按钮元素水平居中。在第 82 行，我们指定它应位于 id 为 `data_rate` 的 `View` 下方，并且距离该视图 50dp（第 83 行）。我们还指定当用户点击按钮时，将执行 `goBack` 方法（第 84 行）。

我们将两个 `EditText` 的 `android:inputType` 属性都设置为 `numberDecimal`（第 57 行和第 76 行）。这样，用户只能输入数字，并且最多只能输入一个点（.）字符。

示例 4.7 展示了更新后的 `strings.xml`，在第 16–21 行添加了一些 `String` 变量。这些字符串在 `activity_data.xml` 文件的第 25、30、36、56、75 和 85 行中使用（示例 4.6）。

此时，当我们运行应用时，只能看到第一个屏幕，因为我们还没有办法进入第二个屏幕。不过，我们可以临时修改 `MainActivity.java` 中设置第一个屏幕所用资源的语句，改为显示第二个屏幕。我们在示例 4.8 的第 11–12 行展示了这一点。

![](img/ch04exa07.jpg)

示例 4.7 更新后的 `strings.xml` 文件

![](img/ch04exa08.jpg)

示例 4.8 在 `MainActivity` 类中的修改，将 `activity_main` 替换为 `activity_data`

图 4.3 展示了第二个屏幕在环境中的外观。

## 4.4 连接两个 `Activity`：抵押贷款计算器应用，版本 1

现在我们已经定义并编写了应用的 `Model` 和 `View` 部分，其中有两个 XML 文件定义了两个 `Views`。接下来，我们编写应用的 `Controller` 部分。我们希望能够在创建的两个 `Views` 之间来回导航。为此，我们需要完成以下步骤：

- ▸ 在第一个 `Activity` 类中添加一些代码，以便用户通过交互（本例中为用户点击“修改数据”按钮）进入第二个 `View`。
- ▸ 添加一个新类 `DataActivity`，它继承自 `Activity`，用于管理第二个 `View`。包含相关代码，以便当用户点击“完成”按钮时，可以关闭该 Activity 并返回第一个 `View`。
- ▸ 在 `AndroidManifest.xml` 文件中添加另一个 `activity` 元素（用于第二个 Activity）。

`Intent` 和 `Activity` 类提供了启动新 Activity 和返回上一个 Activity 的功能。`Intent` 类封装了要执行的操作的概念。它通常用于启动一个新的 Activity，也可以用于启动一个服务。

表 4.3 展示了 `Intent` 的一个构造函数。它接受两个参数：`context`（一个 `Context` 参数）和 `cls`（一个 `Class` 参数）。`Cls` 表示此 `Intent` 打算执行的类的类型。在此情况下，它是一个类型应为 `Class` 的参数。`Context` 表示此应用包的上下文。`Activity` 类是 `Context` 的子类，因此一个 `Activity` 对象“是一个” `Context` 对象。通常，如果我们已经在当前应用包中执行一个 Activity，那么当前的 `Activity` 对象（由关键字 `this` 表示）也是一个 `Context` 对象，并用作此构造函数的第一个参数。

| `Intent` 构造函数 |
| --- |
| `Intent(Context context, Class<?> cls)` |
| 构造一个 `Intent`，旨在执行与 `context` 位于同一应用包中的类型 `?`（可能是某个 `Activity` 类）所建模的类。 |

表 4.3 `Intent` 类的构造函数

| `Activity` 类的方法 |
| --- |
| `public void startActivity(Intent intent)` |
| 使用 `intent` 作为启动它的 `Intent` 来启动一个新的 Activity。 |
| `public void finish()` |
| 关闭此 Activity 并将其从栈中弹出；显示前一个 Activity 的屏幕。 |

表 4.4 `Activity` 类的方法



表 4.4 展示了 `Activity` 类的 `startActivity` 和 `finish` 方法。`startActivity` 通常由当前的 `Activity` 对象引用调用，以执行其 `Intent` 参数。

示例 4.9 展示了 `MainActivity` 类，其中第 16–19 行包含了 `modifyData` 方法，该方法指示应用跳转到 `DataActivity`。为此，我们需要做两件事：

* 创建一个指向 `DataActivity` 的 `Intent`
* 执行该 `Intent` 并启动 `DataActivity`

`Intent` 类属于 `android.content` 包。我们在第 3 行导入它。在第 17 行，我们实例化 `myIntent`，将 `this` 和 `DataActivity.class`（其类型为 `Class`）传递给 `Intent` 构造函数。在第 18 行，我们调用 `startActivity` 并传入 `myIntent`，从而启动一个类型为 `DataActivity` 的新活动。

要创建第二个活动，我们创建一个名为 `DataActivity` 的新类，它继承自 `AppCompatActivity`。示例 4.10 展示了 `DataActivity` 类。它有一个与 `MainActivity` 类中类似的 `onCreate` 方法，但在第 11 行使用了资源 `activity_data` 而不是 `activity_main`。当用户点击“完成”按钮时调用的 `goBack` 方法，编码在第 14–16 行。在这个版本中，它只调用 `finish` 方法，该方法会关闭当前活动，将应用返回到与主活动关联的视图。此时，`DataActivity` 类仅允许用户显示其关联的视图，并通过点击“完成”按钮返回第一个视图。

![](img/ch04exa09.jpg)

示例 4.9 抵押贷款计算器应用（版本 1）的 `MainActivity` 类

![](img/ch04exa10.jpg)

示例 4.10 抵押贷款计算器应用（版本 1）的 `DataActivity` 类

当我们向应用添加一个活动时，需要在 `AndroidManifest.xml` 文件中添加相应的 `activity` 元素。示例 4.11 展示了更新后的文件。我们在第 20–23 行指定了第二个 `activity` 元素。

![](img/ch04exa11.jpg)

示例 4.11 `AndroidManifest.xml` 文件

`activity` 标签有许多可能的属性。其中一个重要的属性是 `android:name`：它指定了对应 `Activity` 类的名称。语法如下：

```
android:name=”ActivityClassName”
```

该值必须指定（没有默认值），可以是完全限定类名，例如 `com.jblearning.mortgagev1.MainActivity`。如果值以 `.`（点号）开头（如第 11 行和第 21 行的 `.MainActivity` 和 `.DataActivity`），则该值会附加到 `manifest` 元素的 `package` 属性值（第 2–3 行）后面。

现在我们可以运行应用，并在第一个视图和第二个视图之间来回切换（图 4.1 和图 4.3）。我们还可以在第二个屏幕中编辑贷款金额、利率和年限。但是，此时第一个视图中的值保持不变。这将在版本 2 中改变。

## 4.5 活动的生命周期

一个活动会经历一个生命周期，当活动启动、暂停、停止或关闭时，会自动调用相应的方法。表 4.5 列出了这些方法。

为了说明用户运行应用时哪些方法被调用以及何时被调用，我们在 `MainActivity` 和 `DataActivity` 类中包含了表 4.5 中的所有方法。每个方法都会调用其 `super` 方法，并向 Logcat 输出一些内容。示例 4.12 和示例 4.13 展示了这两个类。请注意，如果不调用 `super` 方法，应用将会崩溃。

为了方便起见，我们在每个类中添加了一个常量（分别在第 10 行和第 9 行），并在每个 Log 语句中使用它。这两个常量具有相同的值 `MainActivity`，即过滤器的名称。我们本可以为 `DataActivity` 类添加第二个过滤器，但在此例中，我们想要检查两个活动中活动生命周期方法的执行顺序。因此，只点击一个过滤器就能同时看到所有输出并按正确顺序排列，这样更方便。

| 方法 | 描述 |
| --- | --- |
| `onCreate(Bundle)` | 当活动被创建时调用；`Bundle` 参数存储活动之前冻结的状态（如果有的话）。 |
| `onStart()` | 在 `onCreate` 之后调用，当活动变为可见时。 |
| `onResume()` | 在 `onStart` 之后调用，当用户开始与活动交互时。 |
| `onPause()` | 当 Android 启动或恢复另一个活动时调用。 |
| `onStop()` | 当活动对用户变为不可见时调用。 |
| `onRestart()` | 当活动即将重新启动时调用。 |
| `onDestroy()` | 当活动结束或因系统内存不足需要释放内存而被系统销毁时调用。 |

表 4.5 `Activity` 类的生命周期方法

![](img/ch04exa12.jpg) ![](img/ch04exa12a.jpg)

示例 4.12 包含生命周期方法的 `MainActivity` 类

![](img/ch04exa13.jpg) ![](img/ch04exa13a.jpg)

示例 4.13 包含生命周期方法的 `DataActivity` 类

一个活动会一直保留在内存中，直到被销毁，此时会调用 `onDestroy` 方法。活动按栈组织——每当启动一个新活动时，它会被放到栈顶。当一个活动被销毁时，它会从栈中弹出。

表 4.6 展示了用户启动应用并在设备上与应用交互时，输出和活动栈的状态。

当应用启动时，起始活动 `MainActivity` 的 `onCreate`、`onStart` 和 `onResume` 方法会按顺序依次调用。当用户触摸“修改数据”按钮时，首先调用 `MainActivity` 的 `onPause` 方法，然后调用 `DataActivity` 类的 `onCreate`、`onStart` 和 `onResume` 方法，接着调用 `MainActivity` 的 `onStop` 方法。`MainActivity` 类的 `onDestroy` 方法不会被调用，因为 `MainActivity` 的实例仍在内存中，并且位于活动栈的底部。此时 `DataActivity` 的实例位于栈顶。当用户触摸“完成”按钮时，首先调用 `DataActivity` 的 `onPause` 方法，然后调用 `MainActivity` 的 `onRestart`、`onStart` 和 `onResume` 方法，接着调用 `DataActivity` 的 `onStop` 和 `onDestroy` 方法。调用 `onDestroy` 表明之前位于栈顶的 `DataActivity` 实例已从栈中弹出，不再存在于内存中。调用 `MainActivity` 的 `onRestart` 方法表明现在位于栈顶（此时栈中唯一的一个）的 `MainActivity` 实例被重新启动。注意，`onCreate` 方法没有被调用，因为 `MainActivity` 实例之前已经创建并仍在内存中。

此时，如果用户只是等待并停止与应用交互，应用会进入后台并变得不可见；当前活动 `MainActivity` 的 `onPause` 和 `onStop` 方法会被调用。然后，当用户触摸电源按钮并滑动屏幕时，随着应用的当前活动进入前台，`MainActivity` 的 `onRestart`、`onStart` 和 `onResume` 方法会被调用。

| 操作 | 输出 | 活动栈 |
| --- | --- | --- |
| 用户启动应用 | 在 `MainActivity` 内部：`onCreate` 在 `MainActivity` 内部：`onStart` 在 `MainActivity` 内部：`onResume` | 主活动 |
| 用户触摸“修改数据”按钮 | 在 `MainActivity` 内部：`onPause` 在 `DataActivity` 内部：`onCreate` 在 `DataActivity` 内部：`onStart` 在 `DataActivity` 内部：`onResume` 在 `MainActivity` 内部：`onStop` | 数据活动 主活动 |
| 用户触摸“完成”按钮 | 在 `DataActivity` 内部：`onPause` 在 `MainActivity` 内部：`onRestart` 在 `MainActivity` 内部：`onStart` 在 `MainActivity` 内部：`onResume` 在 `DataActivity` 内部：`onStop` 在 `DataActivity` 内部：`onDestroy` | 主活动 |
| 用户操作 | 调用的方法 | 活动状态 |
| --- | --- | --- |
| 用户等待片刻，应用进入后台，不再可见 | 在 `MainActivity:onPause` 内 在 `MainActivity:onStop` 内 | 主活动 |
| 用户按下设备的电源键，然后滑动屏幕 | 在 `MainActivity:onRestart` 内 在 `MainActivity:onStart` 内 在 `MainActivity:onResume` 内 | 主活动 |
| 用户按下设备的主页键 | `MainActivity:onPause` `MainActivity:onStop` | 主活动 |
| 用户点击应用图标 | 在 `MainActivity:onRestart` 内 在 `MainActivity:onStart` 内 在 `MainActivity:onResume` 内 | 主活动 |
| 用户按下设备的返回键 | 在 `MainActivity:onPause` 内 在 `MainActivity:onStop` 内 在 `MainActivity:onDestroy` 内 |  |

表 4.6 用户与应用交互时活动栈的输出与状态

然后，如果用户按下主页键，会调用 `onPause` 和 `onStop`。当用户点击屏幕上的应用图标时，应用重新启动，因此会再次调用 `onRestart`、`onStart` 和 `onResume`。

最后，如果用户按下返回键，会调用 `onPause`、`onStop` 和 `onDestroy`，然后退出当前活动。活动栈现在为空，我们退出应用。

## 4.6 在活动之间共享数据：抵押贷款计算器应用，版本 2

在版本 2 中，我们为控制器添加功能，以构建一个功能完整的应用。为此，我们需要能够将用户在第二个视图中输入的值传递给管理第一个视图的活动，以便计算月供和总付款额并显示它们。当我们返回第二个视图再次编辑数值时，需要检索并显示最新的数值，而不是默认值。

有多种方式可以在活动之间传递数据，包括：

* 使用 `Intent` 类的 `putExtra` 方法传递数据。数据必须是原始数据类型或 `String`。
* 在一个 `Activity` 类中声明一个模型类（在本应用中为 `Mortgage` 类）的 `public static` 实例。这样该实例可以被任何其他 `Activity` 类全局访问。
* 将 `Mortgage` 类重写为“单例”类，以便所有 `Activity` 类都能访问并共享同一个对象。
* 将数据写入文件，然后从该文件读取。
* 将数据写入 SQLite 数据库，然后从中读取。

在本应用中，我们希望在两个屏幕之间共享一个 `Mortgage` 对象，而不是共享原始数据类型或 `String`。因此，我们不会使用 `Intent` 的 `putExtra` 方法。在本书后面，我们会展示如何使用 `putExtra` 方法。如果只是想在两个活动之间传递数据，将数据写入文件或 SQLite 数据库就有些大材小用了。

单例类是指只能实例化一个对象的类。我们可以声明该类的多个对象引用，但在实例化后，它们都将指向内存中的同一个对象。因此，活动可以共享同一个对象，从中读取数据并写入数据。我们可以将 `Mortgage` 类重写为单例类，但如果编写其他应用，我们可能希望能够实例化多个 `Mortgage` 对象。因此，我们决定不将 `Mortgage` 类实现为单例。

我们采用第二种策略，这对本应用来说是最简单的。我们在 `MainActivity` 类中声明一个 `public static` 的 `Mortgage` 类型变量，并在 `DataActivity` 类中访问它。在 `MainActivity` 中，我们有以下声明：

```
public static Mortgage mortgage;
```

我们可以在 `DataActivity` 类中使用以下表达式访问它：

```
MainActivity.mortgage
```

这样，同一个 `Mortgage` 对象就可以从两个 `Activity` 类中引用。这正是本应用所需要的：只有一个 `Mortgage` 对象，而不是两个相同的 `Mortgage` 对象。

示例 4.14 展示了更新后的 `MainActivity` 类。我们在第 10 行将 `Mortgage` 变量 `mortgage` 声明为 `public` 和 `static`。它在第 14 行的 `onCreate` 方法中被实例化。

`onStart` 方法（第 18–21 行）在以下情况下自动调用：启动应用时、从数据活动返回时、或者主活动从后台回到前台时。我们希望每次发生这些事件时数据都能更新，因此我们在第 20 行调用 `updateView` 方法。`updateView` 方法（第 23–34 行）使用当前的抵押贷款数据更新五个 `TextView` 元素。我们使用 `findViewById` 方法获取每个 `TextView` 元素，并将返回的 `View` 强制转换为 `TextView`。然后，我们通过 `mortgage` 对象调用 `Mortgage` 类的方法，以使用当前的抵押贷款数据设置每个 `TextView` 元素的文本。例如，在第 31 行，我们设置显示月供的 `TextView` 中的文本。我们通过 `mortgage` 对象调用 `Mortgage` 类的 `formattedMonthlyPayment` 方法来获取月供值。然后，我们使用 `monthlyTV` 调用 `setText` 方法并传入该值。

![](img/ch04exa14.jpg)

示例 4.14 `MainActivity` 类，抵押贷款计算器应用，版本 2

示例 4.15 展示了更新后的 `DataActivity` 类。它增加了两个功能：

* 更新由该活动控制的视图中显示的抵押贷款参数。
* 当用户离开该活动时，更新 `MainActivity` 类的抵押贷款对象。

`updateView` 方法（第 16–30 行）根据 `MainActivity` 类的 `static` 变量 `mortgage` 的三个实例变量的值，更新由该活动控制的视图中的各个元素。它首先在第 17 行获取对 `MainActivity` 类的 `mortgage` 对象的引用。然后，根据 `mortgage` 的 `years` 实例变量的值，在第 18–24 行更新单选按钮的状态。如果该值为 10（第 18 行），则打开 10 年单选按钮（第 20 行）。如果该值为 15（第 21 行），则打开 15 年单选按钮（第 23 行）。否则，不做任何操作，因为 30 年单选按钮的状态在 `activity_data.xml` 文件中被指定为开启。由于三个单选按钮在 `activity_data` 文件中被定义为 `RadioGroup` 元素的一部分，它们是互斥的——打开一个会自动关闭其他两个。我们使用 `findViewById` 方法获取单选按钮。显示贷款金额的 `EditText` 元素在第 27 行更新，显示利率的 `EditText` 元素在第 29 行更新。

![](img/ch04exa15.jpg) ![](img/ch04exa15a.jpg)

示例 4.15 抵押贷款计算器应用的 `DataActivity` 类，版本 2

`goBack` 方法（第 57–60 行）在用户点击“完成”按钮时执行。在用户离开当前活动（第 59 行）并返回主活动之前，我们希望根据用户输入的值更新 `mortgage` 对象的状态。我们在第 58 行调用了 `updateMortgageObject` 方法。与 `updateView` 方法类似，我们在 `updateMortgageObject` 方法（第 32–55 行）内部首先获取对 `mortgage` 对象的引用。然后，我们更新其实例变量 `amount`、`years` 和 `rate` 的值。在第 34–41 行，我们根据三个单选按钮的当前状态更新 `years`。我们调用 `RadioButton` 从 `CompoundButton` 继承的 `isChecked` 方法，以检查单选按钮是开启还是关闭。在第 42 行，我们获取显示抵押金额的 `EditText` 元素的引用，并在第 43 行检索其文本值并将其赋值给 `String` 变量 `amountString`。我们对利率值执行相同操作，并将检索到的值在第 45 行赋值给 `String` 变量 `rateString`。由于 `mortgage` 对象的 `amount` 和 `rate` 实例变量是 `float` 类型，我们需要将这两个 `String` 转换为 `float`。在 `activity_data.xml` 文件中，我们为与两个 `EditText` 关联的 `android:inputType` 属性指定了 `numberDecimal`；因此，我们保证会得到看起来像 `float` 的 `String`。然而，在第 46–54 行将两个 `String` 转换为 `float` 时，我们仍然额外采取了使用 `try` 和 `catch` 块的预防措施。我们在 `catch` 块中为 `amount` 和 `rate` 使用了默认值。

图 4.4 和 图 4.5 显示了用户在第二个屏幕上更新抵押参数后的两个屏幕。

![](img/9781284093650_CH04_FIGF04.jpg)



图 4.4 在模拟器中运行的抵押计算器应用，版本 2（第二个屏幕）

![](img/9781284093650_CH04_FIGF05.jpg)

图 4.5 在模拟器中运行的抵押计算器应用，版本 2（从第二个屏幕返回后的第一个屏幕）

## 4.7 活动之间的过渡：抵押计算器应用，版本 3

我们希望通过在两个屏幕之间添加动画过渡来改进版本 2。

过渡通常是从一个屏幕切换到另一个屏幕时的动画特效：例如，我们可以淡出当前屏幕进入新屏幕，或者淡入以呈现新屏幕，或者通过从左到右（或从右到左）的滑动动作引入屏幕。可以使用两种类型的动画：补间动画和帧动画。补间动画通过定义其起点和终点来定义，中间帧会自动生成。帧动画通过使用从动画开始到结束的一系列不同图像来定义。

在版本 3 中，我们制作了一个从左到右滑动的补间动画，用于从第一个屏幕过渡到第二个屏幕，以及一个淡入和缩放组合的过渡，用于从第二个屏幕返回到第一个屏幕。与布局、`String` 或样式一样，过渡可以定义为 XML 文件中的资源。也可以通过编程方式定义。

在查找资源时，Android 框架会在 `res` 目录内查找。我们在 `res` 目录中创建一个名为 `anim` 的目录，并在其中添加两个 XML 文件：`slide_from_left.xml` 和 `fade_in_and_scale.xml`。图 4.6 显示了目录结构。`R` 代表 `res` 目录，我们使用表达式 `R.anim.fade_in_and_scale` 和 `R.anim.slide_from_left` 来访问这两个资源。Android 框架会自动在 `anim` 类中创建 `fade_in_and_scale` 和 `slide_from_left` 作为 `public static int` 常量，而 `anim` 类本身是 `R` 类的一个 `public static` 内部类。

抽象类 `Animation` 是动画类的根类。它定义了一些 XML 属性，我们可以使用这些属性通过 XML 文件定义动画。它还定义了一些方法，我们可以通过代码定义动画。它有五个直接子类：`AnimationSet`、`AlphaAnimation`、`RotateAnimation`、`ScaleAnimation` 和 `TranslateAnimation`。表 4.7 显示了这五个类及其对应的 XML 元素。`AnimationSet` 可用于定义一组同时运行的动画。我们也可以通过依次使用多个 `AnimationSet` 来顺序运行多个动画。

一个 XML 动画文件必须有一个单一的根元素，例如 `<alpha>`、`<rotate>`、`<translate>`、`<scale>` 或 `<set>`。我们可以使用 `<set>` 元素将其他元素嵌套在其中，并定义多个同时运行的动画。

表 4.8 显示了表 4.7 中 XML 元素的一些选定 XML 属性及其含义。`android:duration` 和 `android:interpolator` 属性是所有动画共有的。`android:interpolator` 属性指定了一个资源，该资源定义了动画的平滑度，特别是其加速或减速。默认是线性速度，即无加速。

![](img/9781284093650_CH04_FIGF06.jpg)

图 4.6 显示过渡 XML 文件的目录结构

| XML 元素 | 类 | 描述 |
| --- | --- | --- |
| `set` | `AnimationSet` | 定义一组（同时的）动画 |
| `alpha` | `AlphaAnimation` | 淡入或淡出动画 |
| `rotate` | `RotateAnimation` | 围绕固定点的旋转动画 |
| `scale` | `ScaleAnimation` | 从固定点开始的缩放动画 |
| `translate` | `TranslateAnimation` | 滑动（水平或垂直）动画 |

表 4.7 选定的动画 XML 元素及其对应的类

在为这些属性赋值时，我们可以使用绝对值或相对值。相对值可以相对于元素本身，使用语法 `value%`，例如 `30%`，或者相对于其父元素，使用语法 `value%p`，例如 `50%p`。

| XML 元素 | XML 属性 | 描述 |
| --- | --- | --- |
|  | `android:duration` | 动画应运行的毫秒数 |
|  | `android:interpolator` | 应用于动画的插值器 |
| `alpha` | `android:fromAlpha` | 起始不透明度值，介于 0.0 和 1.0 之间 |
| `alpha` | `android:toAlpha` | 结束不透明度值，介于 0.0 和 1.0 之间 |
| `rotate` | `android:fromDegrees` | 旋转的起始角度 |
| `rotate` | `android:toDegrees` | 旋转的结束角度 |
| `rotate` | `android:pivotX` | 旋转固定点的 X 坐标 |
| `rotate` | `android:pivotY` | 旋转固定点的 Y 坐标 |
| `scale` | `android:fromXScale` | 起始 X 缩放值，介于 0.0 和 1.0 之间 |
| `scale` | `android:toXScale` | 结束 X 缩放值，介于 0.0 和 1.0 之间 |
| `scale` | `android:fromYScale` | 起始 Y 缩放值，介于 0.0 和 1.0 之间 |
| `scale` | `android:toYScale` | 结束 Y 缩放值，介于 0.0 和 1.0 之间 |
| `scale` | `android:pivotX` | 缩放发生时固定点的 X 坐标 |
| `scale` | `android:pivotY` | 缩放发生时固定点的 Y 坐标 |
| `translate` | `android:fromXDelta` | 平移起点的 X 坐标 |
| `translate` | `android:toXDelta` | 平移终点的 X 坐标 |
| `translate` | `android:fromYDelta` | 平移起点的 Y 坐标 |
| `translate` | `android:toYDelta` | 平移终点的 Y 坐标 |

表 4.8 各种 `Animation` 类的选定 XML 属性

示例 4.16 展示了从屏幕左侧滑入的过渡效果。对于水平滑动过渡，我们使用属性 `android:fromXDelta` 定义起始 x 坐标，使用属性 `android:toXDelta` 定义结束 x 坐标，后者应设为 0。如果屏幕从左向右进入，`android:fromXDelta` 的值应为负数（如果从右向左进入则为正数）。这两个值在第 5 行和第 6 行定义。过渡时间使用属性 `android:duration` 定义，其值以毫秒为单位。第 7 行定义了一个持续 4 秒的过渡。

![](img/ch04exa16.jpg)

示例 4.16 `slide_from_left.xml` 文件

示例 4.17 展示了同时运行的淡入和缩放过渡效果。它们都定义在 `set` 元素内部。

对于淡入动画（第 4–7 行），我们使用 `alpha` 元素，并通过 `android:fromAlpha` 属性定义起始透明度，通过 `android:toAlpha` 属性定义结束透明度。对于完全淡入，起始透明度为 0，结束透明度为 1。它们在第 5 行和第 6 行定义。第 7 行定义了一个持续 3 秒的过渡。

对于缩放动画（第 9–16 行），我们使用 `scale` 元素，并通过 `android:fromXScale`、`android:toXScale`、`android:fromYScale` 和 `android:toYScale` 属性定义起始和结束的 x、y 缩放值。通常我们希望最终缩放为 1。因此，`android:toXScale` 和 `android:toYScale` 的值均为 1.0（第 11 行和第 13 行）。对于完全缩放动画，我们将 `android:fromXScale` 和 `android:fromYScale` 指定为 0.0（第 10 行和第 12 行）。我们将缩放动画的枢轴点定义为中心。`android:pivotX` 和 `android:pivotY` 属性指定该枢轴点的 x 和 y 坐标。如果希望缩放动画从左上角开始并向右下角展开，则将这两个值设为 0.0。如果希望缩放动画从屏幕中心开始并向外展开，则使用相对值并将这两个值设为 50%（第 14 行和第 15 行）。由于两个动画同时运行，我们指定相同的持续时间，即 3 秒（第 16 行），与淡入动画相同。

![](img/ch04exa17.jpg)

示例 4.17 `fade_in_and_scale.xml` 文件

| 方法 | 描述 |
| --- | --- |
| `void overridePendingTransition (int enterAnimResource, int exitAnimResource)` | 参数 `enterAnimResource` 和 `exitAnimResource` 均为资源 ID，分别指定进入新活动（Activity）和退出当前活动时的动画。值为 0 表示无动画。 |

表 4.9 `Activity` 类的 `overridePendingTransition` 方法

继承自 `Activity` 类的 `overridePendingTransition` 方法，如表 4.9 所示，允许我们在从一个活动切换到另一个活动时指定一个或两个过渡效果。该方法应在调用 `startActivity`（启动新活动）或 `finish`（返回上一个活动）之后立即调用。

在 `MainActivity` 类中，`modifyData` 方法（示例 4.18）包含跳转到第二个屏幕的代码。我们在第 39 行调用 `overridePendingTransition`，并将 `slide_from_left` 资源指定为过渡到第二个屏幕的动画。第二个参数值为 `0`，表示从第一个屏幕过渡时不使用任何动画。

![](img/ch04exa18.jpg)

示例 4.18 `MainActivity` 类中的 `modifyData` 方法

在 `DataActivity` 类中，`goBack` 方法（示例 4.19）包含返回第一个屏幕的代码。我们在第 60 行调用 `overridePendingTransition`，并将 `fade_in_and_scale` 资源指定为过渡到第一个屏幕的动画，同时当前屏幕无过渡效果。

示例 4.20 展示了自动生成的 `R.java` 文件的部分内容。在项目中，它位于 `app/build/generated/source/r/debug/com/jblearning/mortgagev3` 目录下。

![](img/ch04exa19.jpg)

示例 4.19 `DataActivity` 类中的 `goBack` 方法

![](img/ch04exa20.jpg)

示例 4.20 `R.java` 文件的选定内容

此文件不应修改。其中包含公共静态类，这些类包含过渡、ID、布局、字符串等常量。

如果运行该应用，我们可以看到跳转到第二个屏幕时向左滑动的过渡效果，以及返回第一个屏幕时的淡入和缩放过渡效果（如图 4.7 所示）。

![](img/9781284093650_CH04_FIGF07.jpg)

图 4.7 处于 `fade_in_and_scale` 过渡过程中的抵押贷款计算器应用，版本 3

## 4.8 处理持久化数据：抵押贷款计算器应用，版本 4

在应用的第 4 版中，我们希望用户选择的数据能够持久化。当用户首次使用应用时，我们显示三个抵押贷款参数（贷款金额、利率和年限）的默认值。但当用户再次使用应用时，我们希望显示用户上次使用应用时使用的值。

为了实现该功能，每次抵押贷款参数发生变化时，我们都会将其写入设备上的一个文件。首次启动应用时，该文件不存在，因此我们使用默认的抵押贷款参数。之后运行应用时，我们从文件中读取抵押贷款参数。虽然我们可以使用 `ContextWrapper` 类的 `openFileOutput` 和 `openFileInput` 方法打开文件进行读写，但使用用户偏好系统来存储和检索持久化数据更为简便。应用的偏好设置被组织为一组键/值对，类似于哈希表。在本应用中，由于有三个抵押贷款值，因此我们有三个键/值对。

| 方法 | 描述 |
| --- | --- |
| `SharedPreferences.Editor putInt(String key, int value)` | 在此 `SharedPreferences.Editor` 中将值与键关联。这些键/值对应通过调用 `commit` 或 `apply` 方法提交。返回此 `SharedPreferences.Editor`，以便可以链式调用方法。 |
| `SharedPreferences.Editor putFloat(String key, float value)` | 在此 `SharedPreferences.Editor` 中将值与键关联。这些键/值对应通过调用 `commit` 或 `apply` 方法提交。返回此 `SharedPreferences.Editor`，以便可以链式调用方法。 |
| `boolean commit()` | 提交此 `SharedPreferences.Editor`（通过 `putDataType` 方法调用）对相应 `SharedPreferences` 对象所做的偏好更改。 |

表 4.10 `SharedPreferences.Editor` 接口的选定方法

`SharedPreferences` 接口包含写入和读取用户偏好的功能。其静态内部接口 `Editor` 使我们能够存储用户偏好。表 4.10 展示了它的一些方法。`putDataType` 方法具有以下通用方法头：

```java
public SharedPreferences.Editor putDataType(String key, DataType value)
```

它在此 `SharedPreferences.Editor` 中将值与键关联。数据类型可以是基本数据类型或 `String`。为了实际写入用户偏好，我们需要调用 `commit` 或 `apply` 方法。假设我们有一个名为 `editor` 的 `SharedPreferences.Editor` 引用，为了将值 10 与键 `rating` 关联，我们编写：

```java
// editor 是一个 SharedPreferences.Editor
editor.putInt("rating", 10);
```

要检索之前写入用户偏好设置的数据，我们使用 `SharedPreferences` 接口的 `getDataType` 方法。表 4.11 展示了其中一些方法。`getDataType` 方法具有以下通用方法头：

```java
public DataType getDataType(String key, DataType defaultValue)
```

返回值是之前写入用户偏好设置时与 `key` 关联的值。如果 `key` 不存在，则返回 `defaultValue`。假设我们有一个名为 `pref` 的 `SharedPreferences` 引用，为了检索之前与键 `rating` 关联并写入偏好设置的值，我们编写：

```java
// pref 是一个 SharedPreferences 对象
int storedRating = pref.getInt("rating", 1);
```

| 方法 | 描述 |
| --- | --- |
| `int getInt(String key, int defaultValue)` | 返回此 `SharedPreferences` 对象中与 `key` 关联的 `int` 值。如果未找到 `key`，则返回 `defaultValue`。 |
| `float getFloat(String key, float defaultValue)` | 返回此 `SharedPreferences` 对象中与 `key` 关联的 `float` 值。如果未找到 `key`，则返回 `defaultValue`。 |

表 4.11 `SharedPreferences` 接口的选定方法

| 方法 | 描述 |
| --- | --- |
| `static SharedPreferences getDefaultSharedPreferences(Context context)` | 返回 `context` 的 `SharedPreferences`。 |

表 4.12 `PreferenceManager` 类的 `getDefaultSharedPreferences` 方法

我们可以使用 `PreferenceManager` 类的 `getDefaultSharedPreferences` static 方法（如表 4.12 所示）来获取一个 `SharedPreferences` 引用。由于 `Activity` 类继承自 `Context`，而我们的 `MainActivity` 和 `DataActivity` 类继承自 `Activity`，因此我们可以将关键字 `this` 作为此方法的参数传递。因此，在 `Activity` 类内部，为了在我们的两个类中获取 `SharedPreferences`，我们可以编写：

```java
SharedPreferences pref =
    PreferenceManager.getDefaultSharedPreferences(this);
```

我们应用的视图组件仍然相同。大部分更改发生在模型层。我们修改 `Mortgage` 类，使其包含一个将抵押数据写入用户偏好设置系统的方法，以及一个从其中读取数据的构造函数。在构成应用控制器部分的 `MainActivity` 和 `DataActivity` 类中，我们使用这些方法从用户偏好设置系统加载或写入抵押参数。



示例 4.21 展示了`Mortgage`类的更新部分。第 5–6 行导入了`SharedPreferences`接口和`PreferenceManager`类。第 11–13 行定义了三个`String`常量，分别保存金额、年限和利率的偏好设置键名。

`setPreferences`方法在第 84–93 行编码。我们包含一个`Context`参数，以便将其传递给`getDefaultSharedPreferences`方法。当我们在`DataActivity`类中使用`Mortgage`对象引用`mortgage`调用`setPreferences`方法时，我们将传递`this`。`Context`类在第 4 行导入。

在第 86–87 行，我们调用`getDefaultSharedPreferences`以获取一个`SharedPreferences`引用。在第 88 行，我们调用`edit`方法并获取一个`SharedPreferences.Editor`引用。利用它，我们在第 89–91 行使用第 11–13 行定义的三个键写入抵押数据。在第 92 行，我们调用`commit`以实际写入偏好设置。

![](img/ch04exa21.jpg)

示例 4.21 `Mortgage`类，抵押计算器应用，版本 4

我们在第 26–33 行添加了一个重载构造函数。在第 30–32 行从偏好设置中读取抵押数据，并调用修改器将读取的三个值赋给`amount`、`years`和`rate`实例变量。如果未找到某个键，我们指定一个适当的默认值。

`MainActivity`类中只需更改一行代码：实例化`mortgage`的语句。我们使用`Mortgage`类的重载构造函数，而不是默认构造函数（示例 4.22 的第 14 行）。参数`this`代表当前的`MainActivity`，因此是一个`Activity`，从而是一个`Context`对象引用。

![](img/ch04exa22.jpg)

示例 4.22 `MainActivity`类中的`onCreate`方法，抵押计算器应用，版本 4

`DataActivity`类中也只需添加一行代码：将`mortgage`中的数据写入此应用的用户偏好设置的语句。我们在`updateMortgageObject`方法的末尾通过调用`setPreferences`方法并传入`mortgage`来实现，再次将`this`作为其参数传递（示例 4.23 的第 51 行）。`updateMortgageObject`方法在用户更新第二个屏幕上的抵押参数后、返回第一个屏幕之前被调用。

![](img/ch04exa23.jpg)

示例 4.23 `DataActivity`类中的`updateMortgageObject`方法，抵押计算器应用，版本 4

从前面的示例可以看出，为此应用实现持久化数据很简单。除了在每个`Activity`类（此应用的两个控制器）中各添加一行代码外，我们在模型层（`Mortgage`类）中编写了两个方法，一个用于写入文件，另一个用于读取文件。两个视图保持不变。简单的更新和改进是模型-视图-控制器架构的优势之一。

当应用写入用户偏好设置时，它会写入设备文件系统。通常，当我们向 Google Play 发布需要与设备交互的应用时，可能需要在`AndroidManifest.xml`文件中包含一个`uses-permission`元素，以便应用正常运行。此外，在有人下载应用之前，会告知他/她该应用会写入设备的文件系统。此类元素的语法如下：

```
<uses-permission android:name="permissionName" />
```

`android:name`属性是权限的名称：其值与应用想要使用设备的某个功能或服务有关，例如相机、联系人列表、读取或发送短信的能力。可以为此属性分配许多值，例如`android.permission.CAMERA`、`android.permission.READ_CONTACTS`、`android.permission.FLASHLIGHT`，或者在此应用的情况下为`android.permission.WRITE_EXTERNAL_STORAGE`。

对于此应用，由于我们要写入设备文件系统，因此需要在`AndroidManifest.xml`的`manifest`元素内包含以下内容（注意：在模拟器中运行应用时不需要这样做）：

```
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

当我们第二次运行应用时，第一次运行时在第二个屏幕上输入的数据现在会显示在第一个屏幕上。应用正在从第一次运行时写入的偏好设置中提取数据。

## 章节总结

*   Android 框架提供了布局来帮助我们组织视图。
*   布局是`ViewGroup`的子类。
*   `TableLayout`将其子元素按行和列排列。
*   `RelativeLayout`将组件相对于其他组件定位。
*   我们可以调用`Activity`类的`startActivity`方法，并传递一个`Intent`参数，以启动该`Intent`对应的新`Activity`。
*   Activity 在栈上进行管理——最近启动的`Activity`位于栈顶。
*   我们可以调用`finish`方法来关闭一个`Activity`。这会将其从栈中弹出，应用返回到上一个`Activity`。
*   `Activity`会经历一个生命周期，当 Activity 启动、暂停、停止或关闭时，会自动调用相应的方法。
*   在两个活动之间传递或共享数据有多种方式，包括：使用`Intent`类的`putExtra`方法、为`Model`使用单例类、或使用表示`Model`的全局变量。
*   活动之间共享数据的一种方式是在一个`Activity`类中声明一个`Model`类的`public static`实例。这样，它就是全局的，可以被任何其他`Activity`类访问。
*   过渡是一种从一个屏幕到另一个屏幕的动画特效。
*   Android 框架提供了用于淡入淡出、缩放、平移和旋转动画的类。动画可以用 XML 文件编写，并放置在`anim`目录中，该目录应放在`res`目录下。
*   `SharedPreferences`接口提供了向文件系统写入和读取首选项的功能。
*   `PreferenceManager`类的`getDefaultSharedPreferences`静态方法返回一个`SharedPreferences`引用。
*   如果应用向文件系统写入数据，我们需要在`AndroidManifest.xml`文件中包含一个`uses-permission`元素。

![](img/common.jpg)

## 练习、问题和项目

### 多项选择题

1.  `TableLayout`类可用于组织各种 GUI 组件
    *   作为行和列的表
    *   作为多行但每行只有一列的表
    *   作为只有一行和多列的表
    *   作为只有一行一列的表

2.  `LinearLayout`和`RelativeLayout`的直接超类是
    *   `View`
    *   `ViewGroup`
    *   `Layout`
    *   `Object`

3.  `TableLayout`和`TableRow`是以下类的直接子类
    *   `LinearLayout`
    *   `ViewGroup`
    *   `RelativeLayout`
    *   `View`

4.  `RelativeLayout`类是组织各种 GUI 组件的一个好选择
    *   为组件提供绝对的 x 和 y 坐标
    *   以便我们相对于其他组件定位组件
    *   作为多行多列的网格
    *   它从来都不是一个好选择

5.  `Intent`类在哪个包中？
    *   `java.intent`
    *   `android.widget`
    *   `android.activity`
    *   `android.content`

6.  在为新活动创建了`Intent`之后，你调用`Activity`类的哪个方法并传入该`Intent`参数以启动新活动？
    *   `startActivity`
    *   `newActivity`
    *   `startIntent`
    *   `newIntent`

7.  当活动即将重新启动时，`Activity`类的哪个方法会被自动调用？
    *   `onCreate`
    *   `onDestroy`
    *   `onRestart`
    *   `onGo`

8.  当活动首次创建时，`Activity`类的哪些方法（以及按什么顺序）会被自动调用？
    *   `onCreate`
    *   `onCreate`、`onStart`和`onResume`（按此顺序）
    *   `onCreate`和`onResume`
    *   `onStart`、`onCreate`和`onResume`（按此顺序）

9.  当活动对用户变为不可见时，`Activity`类的哪个方法会被自动调用？
    *   `onResume`
    *   `onStop`
    *   `onPause`
    *   `onInvisible`

10. 两个活动可以共享相同的数据
    *   不，这是不可能的
    *   可以，但只能通过读写同一个文件来实现
    *   可以，但只能通过读写 SQLite 数据库来实现
    *   可以，例如通过各自访问另一个类中的公共静态实例变量

11. 我们在哪个包中找到`Animation`类？
    *   `android.animation`
    *   `android.view`
    *   `android.view.animation`
    *   `android.animation.view`

12. 哪个不是`Animation`类的子类？
    *   `ScaleAnimation`
    *   `RotateAnimation`
    *   `AlphaAnimation`
    *   `MoveAnimation`

13. 我们使用哪个类来同时播放多个动画？
    *   `AnimationSequence`
    *   `SequenceAnimation`
    *   `SeveralAnimation`
    *   `AnimationSet`

14. 我们使用`PreferenceManager`类的哪个静态方法来获取`SharedPreferences`？
    *   `getPreferences`
    *   `sharedPreferences`
    *   `getDefaultPreferences`
    *   `getDefaultSharedPreferences`

### 补全代码

15. 在`TableLayout`元素内部，以下代码添加一行，该行包含一个`EditText`和一个`TextView`，其 id 分别为`game`和`player`。

    ```
     <TableRow
        android:layout_width=”wrap_content”
        android:layout_height=”wrap_content” >
        <!--Your code goes here -->

    </TableRow>
    ```

16. 以下代码绘制一条 2 像素粗的蓝色线条。

    ```
     <!-- blue line; your code goes here -->
    ```

17. 在`RelativeLayout`元素的`TableRow`内部，以下代码添加一个`EditText`，其 id 为`age`，并位于 id 为`name`的`View`的右侧。

    ```
     <EditText
        android:layout_width=”wrap_content”
       android:layout_height=”wrap_content”
       <!-- Your code goes here -->

       android:inputType=”numberDecimal” />
    ```

18. 在`AndroidManifest.xml`文件中，添加一个类型为`MyActivity`类的`activity`元素。

    ```
     <!-- Your code goes here -->
    ```

19. 在活动中，当用户点击按钮时，方法`goToSecondActivity`执行。编写代码以从`SecondActivity`类启动一个新活动。

    ```
     public void goToSecondActivity( View v ) {
    // Your code goes here

    }
    ```

20. 当用户从另一个活动返回到此活动时，我们希望执行方法`modifyThisActivity`。重写适当的方法并在其中调用`modifyThisActivity`方法。

    ```
     public void modifyThisActivity( ) {
       // this method is already coded
    }
    // Your code goes here
    ```

21. 此 XML 文件定义了一个全缩放过渡的资源，从左上角开始，向右下角扩展，持续 2 秒。

    ```
     <?xml version=”1.0” encoding=”utf-8”?>
    <set xmlns:android=”http://schemas.android.com/apk/res/android”>
      <scale
      android:fromXScale=”0.0”
      android:fromYScale=”0.0”
      <!--Your code goes here -->

    </set>
    ```

22. 此 XML 文件定义了一个过渡的资源，围绕左上角顺时针旋转 180 度，结束于正常位置，持续 5 秒。

    ```
     <?xml version=”1.0” encoding=”utf-8”?>
    <set xmlns:android=”http://schemas.android.com/apk/res/android”>
      <rotate
      <!--Your code goes here -->

    </set>
    ```

23. 以下代码使用键`number`和`hi`将值 45 和"Hello"写入用户首选项。

    ```
     SharedPreferences preferences = PreferenceManager.
    getDefaultSharedPreferences( );
    SharedPreferences.Editor editor = preferences.edit( );
    // Your code goes here
    ```

24. 以下代码从用户首选项中读取与键`grade`关联的整数值和与键`course`关联的字符串值，并将它们分配给两个变量。如果键不存在，则应将默认值 80 和 CS3 分配给这两个变量。

    ```
     SharedPreferences preferences = PreferenceManager.
    getDefaultSharedPreferences();
    SharedPreferences.Editor editor = preferences.edit();
    // Your code goes here
    ```

### 编写一个应用

25. 编写一个使用两个活动的应用：一个活动玩井字棋，另一个活动要求用户选择谁先走（X 或 O）以及 X 和 O 的颜色。包含一个`Model`。包含两个活动之间的过渡。

26. 编写一个使用两个活动的应用：一个活动要求用户给出一个简单数学问题（加法、减法或乘法）的答案，另一个活动要求用户选择算术运算。包含一个`Model`。包含两个活动之间的过渡。

27. 编写一个使用两个活动的应用：一个活动执行摄氏度到华氏度或华氏度到摄氏度的单位转换，另一个活动让用户选择转换方向。包含一个模型。包含两个活动之间的过渡。

28. 编写一个使用两个活动的应用：一个活动执行英里到公里或公里到英里的单位转换，另一个活动让用户选择转换方向。包含一个模型。包含两个活动之间的过渡。

29. 编写一个使用两个活动的应用：一个活动将句子`Hello World`从英语翻译成另一种语言，另一个活动让用户从五种语言中选择一种进行翻译。包含一个模型。包含两个活动之间的过渡。

30. 编写一个使用两个活动的应用：一个活动执行磅到千克或千克到磅的单位转换，另一个活动让用户选择转换方向。包含一个模型。包含两个活动之间的过渡。让用户的选择持久化，以便下次用户运行应用时，他或她之前的选择成为默认值。

31. 编写一个使用两个活动的应用：一个活动执行美元到另一种货币的货币转换，另一个活动让用户从五种货币中选择一种。包含一个模型。包含两个活动之间的过渡。让用户的选择持久化，以便下次用户运行应用时，他或她之前的选择成为默认值。



32. 编写一个使用两个活动的应用：一个活动计算汽车租赁的月付款，另一个活动让用户输入汽车租赁参数——租赁期限（月数）、首付、租赁利率和租赁结束时的汽车价值。包含一个模型。包含两个活动之间的过渡。让用户的选择持久化，以便下次用户运行应用时，他或她之前的选择成为应用启动时的默认值。

33. 编写一个使用两个活动的应用：一个活动使用固定移位（凯撒密码）对用户在文本字段中输入的文本进行加密，另一个活动让用户定义移位值（1 到 25 之间的整数）。如果移位值为 3，则单词 `the` 将被加密为 `wkh`。如果单词是 `zoo`，则加密后的单词是 `crr`。假设只使用从 a 到 z 的小写字母。包含一个模型。包含两个活动之间的过渡。让用户的选择持久化，以便下次用户运行应用时，他或她之前的移位值成为应用启动时的默认值。

# 第五章：菜单，SQLite

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

为了管理持久化数据，我们可以将数据存储在文件或数据库中。在本章中，我们将学习如何使用 SQLite，这是一种轻量级的关系数据库管理系统（RDBMS），适用于 Android 设备。RDBMS 是一种管理关系数据库的软件程序。尽管 SQLite 使用平面文件存储数据，因此与常规 RDBMS 相比在速度上并非最优，但它使我们能够像使用常规 RDBMS 一样组织数据，并使用 SQL 语法。典型的 SQL 操作包括 `insert`、`delete`、`update` 和 `select`。在本章中，我们还将探讨如何使用菜单：每个菜单项对应一个 SQL（`insert`、`delete`、`update`、`select`）操作。为简单起见，我们只允许设备在竖屏方向运行。

## 5.1 菜单和菜单项：糖果店应用，版本 0

当我们使用基本活动模板启动应用时，Android Studio 会生成两个布局 XML 文件和一个菜单 XML 文件：`activity_main.xml`、`content_main.xml` 和 `menu_main.xml`。这与空活动模板不同，后者只生成 `activity_main.xml` 文件。

`activity_main.xml` 文件（如示例 5.1 所示）使用 `CoordinatorLayout` 来排列元素。`CoordinatorLayout` 通常用作应用的顶级容器，以及用于与一个或多个子视图进行特定交互的容器。

它包含三个元素：

- 一个 `AppBarLayout`（第 11–23 行），其内部包含一个 `ToolBar`（第 16–21 行）。这是操作栏，菜单项将放置在此处。
- 由 `content_main.xml`（第 25 行）定义的视图，它是一个包含 `TextView` 的 `RelativeLayout`。
- 一个 `FloatingActionButton`（第 27–33 行），位于右下角，其图标是来自 Android 图标库的标准电子邮件图标。在本应用中，我们不需要此功能，因此删除第 27–33 行。

在 `MainActivity` 类的 `onCreate` 方法中，已有处理用户与浮动操作按钮交互的代码，如示例 5.2 所示。由于本应用不使用浮动操作按钮，我们删除 `MainActivity` 类中的这些代码。

![](img/ch05exa01.jpg)

示例 5.1 使用基本活动模板时自动生成的 `activity_main.xml` 文件

![](img/ch05exa02.jpg)

示例 5.2 使用基本活动模板时 `MainActivity.java` 中生成的部分代码

示例 5.3 显示了 `menu_main.xml` 文件。它定义了一个包含一个菜单项的菜单。菜单项从右侧开始显示在操作栏中。但是，如果我们运行这个骨架应用，不会显示任何菜单项。这是因为唯一的菜单项将属性 `app:showAsAction` 的值设置为 `never`（第 9 行）。

![](img/ch05exa03.jpg)

示例 5.3 自动生成的 `menu_main.xml` 文件

`Menu` 接口（属于 `android.view` 包）封装了一个菜单。菜单由菜单项组成：`MenuItem` 接口封装了一个菜单项。表 5.1 显示了 `MenuItem` 的一些属性和方法。同一个属性可能对应多个方法。一个 `setTitle` 方法接受 `CharSequence` 参数（类似于 `String` 数据类型），而另一个 `setTitle` 方法接受表示资源的 `int` 参数。菜单项可以分配一个 id，以便我们可以在相应的 `Activity` 类中获取对它们的引用。表 5.2 显示了 `MenuItem` 的一些常量，这些常量可以作为 `setShowAsAction` 的参数，以及对应的 `showAsAction` XML 属性值。

我们更新 `menu_main.xml` 文件（如示例 5.4 所示），并包含三个标题分别为添加、删除和更新的菜单项。这三个字符串定义在 `strings.xml` 文件中（如示例 5.5 所示）。我们提供这三个菜单项，以便用户可以向数据库添加糖果、删除糖果或编辑糖果。`android:orderInCategory` 属性使我们能够对菜单项在菜单上的位置进行排序（值最大的项将位于最右侧）。如果不指定该属性的值，菜单项将按从左到右的顺序放置在操作栏中。由于这样已经满足要求，我们删除所有三个菜单项的 `android:orderInCategory` 属性。

| 属性名称 | 相关方法 | 描述 |
| --- | --- | --- |
| `android:title` | `setTitle( int )`、`setTitle(CharSequence )` | 设置菜单项的标题 |
| `app:showAsAction` | `setShowAsAction( int )` | 定义此菜单项在操作栏中的显示方式 |
| `android:icon` | `setIcon( int )`、`setIcon( Drawable )` | 设置菜单项的图标 |

表 5.1 `MenuItem` 的部分 XML 属性和方法

| 常量 | 属性值 | 描述 |
| --- | --- | --- |
| `SHOW_AS_ACTION_NEVER` | `never` | 从不将菜单项显示在操作栏中 |
| `SHOW_AS_ACTION_ALWAYS` | `always` | 始终将菜单项显示在操作栏中 |
| `SHOW_AS_ACTION_IF_ROOM` | `ifRoom` | 如果有空间，则在操作栏中显示该项 |

表 5.2 `MenuItem` 中用作 `setShowAsAction` 参数的选定常量及其对应的 `showAsAction` 属性值

![](img/ch05exa04.jpg)

示例 5.4 `menu_main.xml` 文件，糖果店应用，版本 0

![](img/ch05exa05.jpg)

示例 5.5 `strings.xml` 文件，糖果店应用，版本 0

如果操作栏中要放置的项太多，最右侧的项不会立即显示，但用户仍然可以通过子菜单访问它们。

示例 5.6 展示了编辑后的 `MainActivity` 类。如前所述，我们删除了 `onCreate` 方法中与浮动操作按钮相关的代码。在 `onCreate` 的第 16 行，我们获取了 `activity_main.xml` 中定义的 `Toolbar` 的引用。我们调用 `setSupportActionBar` 方法（第 17 行），如表 5.3 所示，将其设置为该应用的操作栏。

`onCreateOptionsMenu` 方法（第 20–26 行）填充 `menu_main.xml`（第 24 行）以创建菜单，并将该菜单放置在工具栏中。当用户选择菜单项时，会调用 `onOptionsItemSelected` 方法。其参数是一个指向所选菜单项的 `MenuItem` 引用。我们在第 33 行获取其 id，并使用 `switch` 语句将其与 `menu_main.xml` 中定义的各种菜单项的 id 进行比较，并将所选操作输出到 Logcat。表 5.4 展示了与此相关的菜单类和方法。

如果我们选择 `menu_main.xml` 文件，菜单项会在预览窗格中可见，如图 5.1 所示。当我们在模拟器或设备上运行应用时，UPDATE 菜单项可能可见也可能不可见，具体取决于可用空间。如果有未显示的项，则会显示一个 . . .，当用户点击 . . . 时，未显示的项将变为可见。如果我们点击各个菜单项，相应的输出将显示在 Logcat 中。

![](img/ch05exa06.jpg) ![](img/ch05exa06a.jpg)

示例 5.6 `MainActivity` 类，糖果店应用，版本 0

| 方法 | 描述 |
| --- | --- |
| `void setSupportActionBar( Toolbar toolbar )` | 设置工具栏作为此 Activity 的操作栏；工具栏的菜单将填充该 Activity 的选项菜单 |

表 5.3 `AppCompatActivity` 类的 `setSupportActionBar` 方法

| 类或接口 | 方法 | 描述 |
| --- | --- | --- |
| `Activity` | `boolean onCreateOptionsMenu( Menu menu )` | 初始化此 Activity 菜单的内容。必须返回 true 才能显示菜单。 |
| `Activity` | `boolean onOptionsItemSelected( MenuItem menuItem )` | 当用户选择菜单项时调用。 |
| `Activity` | `MenuInflater getMenuInflater( )` | 返回一个 `MenuInflater`。 |
| `MenuInflater` | `void inflate( int menuRes, Menu menu )` | 填充 `menuRes` 资源并创建菜单。 |
| `MenuItem` | `int getItemId( )` | 返回此菜单项的 id。 |

表 5.4 选定的菜单相关方法

![](img/9781284093650_CH05_FIGF01.jpg)

图 5.1 操作栏中显示的菜单，糖果店应用，版本 0

## 5.2 图标项，糖果店应用，版本 1

在版本 1 中，我们使用图标代替 `Strings` 作为菜单项，并为添加菜单项提供一个带有布局的 Activity。要为菜单项包含图标，我们使用表 5.1 中所示的 `android:icon` XML 属性。我们可以使用 Android 库中现有的图标，也可以创建自己的图标。现有图标可以使用以下语法和模式引用：

```text
@android:drawable/name_of_icon
```

对于添加、编辑（更新）和删除，图标资源的名称分别是 `ic_menu_add`、`ic_menu_edit` 和 `ic_menu_delete`。

示例 5.7 展示了更新后的 `menu_main.xml` 文件，在第 7、12 和 17 行添加了 `android:icon` 属性。请注意，尽管图标显示在操作栏中而标题不显示，但我们仍然为这三个项指定了标题（第 6、11、16 行）。实际上，如果用户长按图标，标题会显示出来。这对视障用户非常有帮助。

![](img/ch05exa07.jpg)

示例 5.7 `menu_main.xml` 文件，糖果店应用，版本 1

图 5.2 展示了 Android Studio 环境中的应用预览：三个图标出现在操作栏的右侧。

当用户点击添加图标时，我们希望允许用户向数据库中添加糖果。我们保持简单，数据库只包含一个存储糖果的表：糖果有 id、名称和价格。id 应为整数，从 0 开始，每添加一个糖果自动递增 1。因此，我们的第二个屏幕（用户可以在其中向数据库添加糖果）只包含两个用于用户输入的小部件：一个用于糖果名称，一个用于糖果价格。示例 5.8 展示了其 XML 布局文件 `activity_insert.xml`。

我们使用 `RelativeLayout` 来组织 GUI。两个 `EditText` 的左侧各有一个 `TextView` 元素，用于告知用户输入内容。我们指定用户必须为价格输入浮点数（第 43 行）。我们还添加了两个按钮，一个用于将糖果添加到数据库（第 45–53 行），另一个用于返回第一个 Activity（第 55–62 行）。点击按钮时，分别触发对 `insert` 方法（第 52 行）和 `goBack` 方法（第 61 行）的调用。各个元素都分配了 id，以便我们能够获取它们（对于两个 `editText`）或根据它们的位置定位其他元素。

`activity_insert.xml` 文件中使用的额外 `String` 常量在 `strings.xml` 中定义，如示例 5.9 所示。

我们创建 `InsertActivity` 类来控制第二个屏幕，该屏幕在 `activity_insert.xml` 中定义。在编写代码之前，我们更新 `MainActivity` 类，以便当用户点击添加图标时，启动一个 `InsertActivity`。更新后的 `MainActivity` 类如示例 5.10 所示。唯一的更改在第 33–34 行：当用户点击添加图标时（第 31 行），我们在第 33 行创建一个 `InsertActivity` 的 `Intent`，并在第 34 行启动该 Activity。

![](img/9781284093650_CH05_FIGF02.jpg)

图 5.2 糖果店应用的第一个屏幕，版本 1

![](img/ch05exa08.jpg) ![](img/ch05exa08a.jpg)

示例 5.8 `activity_insert.xml` 文件，糖果店应用，版本 1

![](img/ch05exa09.jpg)

示例 5.9 `strings.xml` 文件，糖果店应用，版本 1

![](img/ch05exa10.jpg) ![](img/ch05exa10a.jpg)

示例 5.10 `MainActivity` 类，糖果店应用，版本 1

示例 5.11 展示了 `InsertActivity` 类。我们填充了 `insert_activity.xml` 文件中定义的 XML 布局（第 11 行），并包含了 `insert` 和 `goBack` 方法。`goBack` 方法（第 28–30 行）在用户点击返回按钮时执行；它将当前 Activity 从 Activity 栈中弹出，使应用返回到上一个 Activity（即第一个屏幕）。在 `insert` 方法（第 14–26 行）中，我们在第 15–19 行获取用户输入，计划使用用户输入在数据库中插入新糖果（第 21 行），并清除两个 `EditText`（第 23–25 行），以防用户想要添加另一个糖果。

![](img/ch05exa11.jpg) ![](img/ch05exa11a.jpg)

示例 5.11 `InsertActivity` 类，糖果店应用，版本 1

最后，我们在 `AndroidManifest.xml` 文件中添加一个 `activity` 元素，如示例 5.12 的第 23–26 行所示。我们还允许两个 Activity 仅在垂直方向运行。

![](img/ch05exa12.jpg) ![](img/ch05exa12a.jpg)

示例 5.12 `AndroidManifest.xml` 文件，糖果店应用，版本 1

最后，在 `styles.xml` 中，我们指定各个视图中的文本大小为 24，如示例 5.13 的第 5 行所示。

![](img/ch05exa13.jpg)

示例 5.13 `styles.xml` 文件，糖果店应用，版本 1

![](img/9781284093650_CH05_FIGF03.jpg)

图 5.3 糖果店应用的添加糖果界面，版本 1

图 5.3 显示了 Android Studio 环境中应用插入界面的预览。

## 5.3 SQLite：创建数据库、表和插入数据：糖果店应用，版本 2

在版本 2 中，我们创建一个数据库，创建一个表来存储糖果，并向该表中插入数据。

SQLite 在 Android 设备上可用，无需设置。它使我们能够像在 SQL 关系数据库中一样组织数据并执行 SQL 命令，尽管数据存储在文本文件中。`android.database.sqlite` 包包含用于管理数据库、执行 SQL 查询、处理结果等的类和接口。

创建 SQLite 表时，我们只能使用以下数据类型：`null`、`integer`、`real`、`text` 和 `blob`。我们使用 `real` 表示 `float` 和 `double`，使用 `text` 表示字符串。SQLite 支持使用 `integer`、`real` 或 `text` 数据类型处理日期和时间。

| 类 | 描述 |
| --- | --- |
| `SQLiteOpenHelper` | 扩展此抽象类以管理数据库及其版本。我们必须重写 `onCreate` 和 `onUpgrade` 方法。 |
| `SQLiteDatabase` | 包含执行 SQL 语句的方法 |
| `Cursor` | 封装由 `select` SQL 查询返回的表。 |

表 5.5 `android.database.sqlite` 包中的选定类

| `id` | `名称` | `价格` |
| --- | --- | --- |
| 1 | 巧克力饼干 | 1.49 |
| 2 | 巧克力软糖 | 1.99 |
| 3 | 核桃巧克力 | 2.99 |

表 5.6 糖果的示例 SQL 表

表 5.5 显示了 `android.database.sqlite` 包中的几个有用类。



我们在`Model`中包含一个与 SQL 表列对应的类。我们打算像表 5.6 那样存储糖果的名称和价格，其中`id`是`int`，`name`是`String`，`price`是`double`。

示例 5.14 中显示的`Candy`类与表 5.6 中的数据类型对应。它是一个简单的 Java 类，包含构造函数、访问器和修改器。我们包含了一个`toString`方法，这对于调试和反馈非常有用。

![](img/ch05exa14.jpg) ![](img/ch05exa14a.jpg)

示例 5.14 `Candy`类，糖果店应用，版本 2

作为`Model`的一部分，我们包含一个包含执行各种基本 SQL 语句方法的类。当执行插入、更新或删除语句时，我们可以使用`SQLiteDatabase`类的`execSQL`方法，如表 5.7 所示。当执行 select 语句时，我们可以使用`SQLiteDatabase`类的`rawQuery`方法来执行，并使用表 5.8 中显示的`Cursor`类的方法来处理结果。

示例 5.15 显示了`DatabaseManager`类，它扩展了`SQLiteOpenHelper`。`SQLiteOpenHelper`类提供了打开、创建或升级数据库的功能。它是一个`abstract`类，有两个`abstract`方法：`onCreate`和`onUpgrade`，我们必须重写它们。如果数据库存在则打开，不存在则创建，并在必要时升级（通过自动调用`onUpgrade`）。第一次调用`getWritableDatabase`时，会自动调用`onCreate`。表 5.9 显示了这些方法。除此之外，我们创建了一个名为`candy`的表，并提供了对该表的插入、删除、更新和选择操作。为了简单起见，我们只包含了插入记录、根据`id`值删除记录、更新记录、选择记录以及选择`candy`表中所有行的方法。我们可以添加更多方法，例如根据糖果名称的值删除或选择记录。

| 方法 | 描述 |
| --- | --- |
| `void execSQL( String sql )` | 执行`sql`，一个不返回数据的 SQL 查询。可用于创建、插入、更新、删除，但不能用于 select 查询。 |
| `Cursor rawQuery( String sql, String [ ] selectionArgs )` | 执行`sql`并返回一个`Cursor`；可以提供`selectionArgs`来匹配查询 where 子句中的问号。 |

表 5.7 `SQLiteDatabase`类的选定方法

| 方法 | 描述 |
| --- | --- |
| `boolean moveToNext( )` | 处理结果时将此`Cursor`移动到下一行。 |
| `DataType getDataType( int column )` | 返回当前行在列索引`column`处的值。`DataType`可以是基本数据类型、`String`或`Blob`。 |

表 5.8 `Cursor`类的选定方法

![](img/ch05exa15.jpg) ![](img/ch05exa15a.jpg) ![](img/ch05exa15b.jpg)

示例 5.15 `DatabaseManager`类，糖果店应用，版本 2

构造函数（第 17-19 行）调用表 5.9 中显示的`super`构造函数。`onCreate`方法（第 21-28 行）在首次创建数据库时自动调用。在其中，我们应该创建所需的表。我们在第 22-25 行定义了一个表示创建`candy`表的 SQL 语句的`String`，并在第 27 行实际创建了该表。请注意，数据库对于使用它的应用是特定的。如果有两个不同的应用，则有两个不同的数据库。

`insert`、`deleteById`和`updateById`方法（第 38-46 行、第 48-55 行、第 57-67 行）共享相同的模式：我们通过调用`SQLiteOpenHelper`类的`getWritableDatabase`获取`SQLiteDatabase`引用，构建 SQL 查询，通过调用`execSQL`方法执行它，然后关闭数据库。

| 方法 | 描述 |
| --- | --- |
| `SQLiteOpenHelper( Context context, String name, SQLiteDatabase.CursorFactory factory, int newVersion )` | 构造函数：创建一个`SQLiteOpenHelper`对象。`Name`是数据库的名称。`Factory`可用于创建`Cursor`对象，使用`null`表示默认。 |
| `abstract void onCreate( SQLiteDatabase db )` | 当数据库首次创建时调用。我们必须实现该方法。 |
| `abstract void onUpgrade( SQLiteDatabase db, int oldVersion, int newVersion )` | 当数据库需要升级时调用。我们必须实现该方法。 |
| `SQLiteDatabase getWritableDatabase( )` | 创建和/或打开一个用于读写的数据库。第一次调用时触发对`onCreate`的调用。返回一个`SQLiteDatabase`引用，我们可以用它来执行 SQL 操作。 |

表 5.9 `SQLiteOpenHelper`类的选定方法

`selectAll`和`selectById`方法（第 69–84 行和第 86–98 行）获取一个`SQLiteDatabase`引用，构建一条 select SQL 查询，通过调用`rawQuery`方法执行它，处理结果，关闭数据库，并返回一个`Candy`对象的`ArrayList`（`selectAll`方法）或一个`Candy`对象（`selectById`方法）。`rawQuery`方法返回一个`Cursor`对象引用。`moveToNext`方法（第 76 行）使`Cursor`对象指向下一行结果，如果已处理完所有行则返回`false`。因此，我们使用`while`循环（第 76–81 行）处理查询返回的所有行。在循环体内，我们为当前行构造一个`Candy`对象（第 77–79 行），并在第 80 行将其添加到`ArrayList candies`中。我们在第 83 行返回`candies`。对于`selectById`方法，我们期望查询返回 0 或 1 行，因为我们是根据表的主键`id`的值进行选择的。因此，我们不需要循环。我们在第 94 行调用`moveToFirst`方法。如果它返回`true`，则查询返回一行。我们在第 95–96 行构建相应的`Candy`对象。我们在第 97 行返回它。

请注意，在调试阶段，我们可以在调用这些方法时使用`try`和`catch`块，因为当 SQL`String`无效时，它们会抛出未检查的`SQLException`。

现在我们的模型已经准备就绪，我们可以在控制器`InsertActivity`类中使用它，以便向数据库中添加糖果，如示例 5.16 所示。我们在第 10 行声明一个`DatabaseManager`类型的实例变量，并在第 14 行实例化它。我们在第 25–33 行插入用户输入的数据。我们在第 28 行创建并实例化一个`Candy`对象，并在第 29 行将其插入糖果表中。我们使用`try`和`catch`块将用户输入的`price`从`String`转换为`double`。请注意，我们并不关心在第 28 行传递给`Candy`构造函数的`id`值，因为`candy`表的`id`列类型为`auto_increment`；`DatabaseManager`的`insert`方法不会使用它插入的`Candy`对象的`id`值。

![](img/ch05exa16.jpg)

示例 5.16 `InsertActivity`类，糖果店应用，版本 2

| 方法 | 描述 |
| --- | --- |
| `static Toast makeText( Context context, CharSequence text, int duration )` | 在指定上下文中创建一个`Toast`，包含文本内容，持续时间由`duration`指定。 |
| `void show( )` | 显示此`Toast`。 |

| 常量 | 值 |
| --- | --- |
| `LENGTH_SHORT` | 0；使用此常量表示`Toast`持续约 3 秒。 |
| `LENGTH_LONG` | 1；使用此常量表示`Toast`持续约 5 秒。 |

表 5.10 `Toast`类的选定方法和常量

我们在第 30 行和第 32 行向用户提供反馈，显示一个`Toast`。`Toast`是一个临时弹出窗口，可用于提供操作的可视反馈。它会在短暂时间后自动消失。`Toast`类位于`android.widget`包中。表 5.10 显示了`Toast`类的方法和常量。要在`Activity`类中创建`Toast`，我们使用`makeText`静态方法，传递`this`（一个`Activity`“是一个”`Context`）、一个`String`（一个`String`“是一个”`CharSequence`）以及`Toast`类的两个常量之一来指定`Toast`的持续时间。然后我们可以通过调用`show`方法来显示`Toast`。以下代码序列说明了这一点。第 30 行和第 32 行将两个方法调用链接起来。

```
Toast toast = Toast.makeText( this, ”Hi”, Toast.LENGTH_SHORT );
toast.show( );
```

最后，我们删除`content_main.xml`文件中的`TextView`元素，以便第一个屏幕不显示“Hello World!”。

当我们运行应用，输入一些数据并点击 ADD 图标时，`Toast`消息会出现。如果我们想检查是否向`candy`表中添加了新行，我们可以调用`DatabaseManager`类的`selectAll`方法，并遍历生成的`Candy`对象`ArrayList`。我们可以在`insert`方法的末尾编写这些语句，并在 Logcat 中检查输出：

```
ArrayList<Candy> candies = dbManager.selectAll( );
for( Candy candy : candies )
  Log.w( ”MainActivity”, ”candy = ” + candy.toString( ) );
```

## 5.4 删除数据：糖果店应用，版本 3

在版本 3 中，我们允许用户从数据库中删除糖果。要实现此功能，我们需要执行以下操作：

- ▸ 创建一个删除活动。
- ▸ 修改`MainActivity`，以便当用户点击 DELETE 图标时，用户进入删除活动。
- ▸ 在`AndroidManifest.xml`中为删除活动添加一个 activity 元素。

我们创建一个名为`DeleteActivity`的新类。我们更新`MainActivity`类的`onOptionsItemSelected`方法（见示例 5.17），以便当用户点击删除图标时（第 36 行），我们为`DeleteActivity`创建一个 intent（第 37 行），然后启动该活动（第 38 行）。

![](img/ch05exa17.jpg)

示例 5.17 `MainActivity`类，糖果店应用，版本 3

示例 5.18 显示了更新后的`AndroidManifest.xml`文件。它在第 28–31 行包含了一个额外的`DeleteActivity`的 activity 元素。

![](img/ch05exa18.jpg)

示例 5.18 `AndroidManifest.xml`文件，糖果店应用，版本 3

示例 5.19 显示了`DeleteActivity`类。如图 5.4 所示，我们希望将所有糖果显示为单选按钮列表。点击单选按钮会删除该糖果并刷新屏幕。当我们从数据库或文件中删除项目时，通常会在实际删除之前通过一个警告框要求用户确认。为了保持此示例简单，这留作练习。

由于`candy`表中的记录数量随时间变化，单选按钮的数量也会变化。因此，我们需要以编程方式创建 GUI。在`onCreate`方法的第 21 行，我们调用`updateView`方法，该方法创建 GUI。我们在第 24–64 行编写`updateView`：我们从`candy`表中检索所有记录，并为每条记录创建一个单选按钮。为此，我们在第 26 行调用`DatabaseManager`类的`selectAll`方法，使用我们在第 20 行实例化的实例变量`dbManager`（第 16 行）。

因为我们不知道有多少糖果，所以屏幕上可能没有足够的空间来显示所有必要的单选按钮。因此，我们将包含所有单选按钮的`RadioGroup`放在一个`ScrollView`内（第 28 行和第 50 行）。这样，如果需要，我们可以滚动浏览单选按钮。

![](img/ch05exa19.jpg) ![](img/ch05exa19a.jpg)

示例 5.19 `DeleteActivity`类，糖果店应用，版本 3

虽然用户可以使用设备的返回按钮返回到上一个活动，但我们添加了一个按钮作为便利（第 40–42 行；我们使用来自`strings.xml`的名为`button_back`的字符串）。我们在第 44–48 行使用一个`View.OnClickListener`类型的匿名对象为按钮设置事件处理。当用户点击该按钮时，当前活动从栈中弹出，我们返回到上一个活动，即第一个屏幕。但是，`ScrollView`不允许在其内部包含多个`ViewGroup`。因此，我们不能将按钮放在`ScrollView`内部。我们将`ScrollView`放在一个`RelativeLayout`内（第 51 行），并将按钮放在`RelativeLayout`的底部（第 53–61 行）。

![](img/9781284093650_CH05_FIGF04.jpg)

图 5.4 糖果店应用的删除屏幕，版本 3

我们在第 29 行创建了`RadioGroup`。在第 30 至 35 行，我们遍历`Candy`对象的`ArrayList`：为每个`Candy`创建一个`RadioButton`（第 31 行），将其文本设置为该`Candy`对象的`String`表示（第 33 行），并在第 34 行将其添加到`RadioGroup`中。在第 32 行，将`RadioButton`的`id`设置为对应`Candy`对象的`id`。这样，当用户选择一个单选按钮时，我们就能访问到正确的`Candy`对象。

在第 36 至 38 行，我们为这组单选按钮设置事件处理。表 5.11 展示了`RadioGroup`类的`setOnCheckedChangeListener`方法，我们用它来处理组内单选按钮的选择。该方法的参数是一个`RadioGroup.OnCheckedChangeListener`。`OnCheckedChangeListener`是`RadioGroup`的一个`public static`内部接口。我们在第 66 至 77 行编写了一个实现`RadioGroup.OnCheckedChangeListener`的`private`类。在第 69 至 70 行，我们从`candy`表中删除选中的糖果。由于我们将`Candy id`赋给了对应的`RadioButton`，因此我们知道`checkedId`参数不仅是所选`RadioButton`的`id`，也是要删除的正确`Candy`的`id`。在第 71 至 72 行，我们使用`Toast`提供一些视觉反馈，表明糖果已被删除。在第 74 至 75 行，我们调用`updateView`来更新单选按钮列表，反映已删除的糖果不再存在于数据库中。

| 方法 | 描述 |
| --- | --- |
| `void setOnCheckedChangeListener( RadioGroup.OnCheckedChangeListener listener )` | 在此`RadioGroup`上注册监听器。当此组中选中的单选按钮发生变化时，会调用`RadioGroup.OnCheckedChangeListener`接口的`onCheckedChange`方法。 |

表 5.11 `RadioGroup`类的选定方法

图 5.4 展示了用户选择删除图标后应用的删除界面。所有糖果都以单选按钮形式显示。点击其中一个会将其删除并刷新屏幕。请注意，版本 3 中的数据库与版本 2 中的数据库不同。因此，如果我们在未插入糖果的情况下运行版本 3，`candy`表为空，点击删除图标时不会显示任何糖果。

## 5.5 更新数据：糖果店应用，版本 4

在版本 4 中，我们允许用户更新数据库中糖果的名称和价格。要实现此功能，我们需要执行以下操作：

- ▸ 创建一个更新活动。
- ▸ 修改`MainActivity`，使得当用户点击更新图标时，用户会跳转到更新活动。
- ▸ 在`AndroidManifest.xml`中为更新活动添加一个活动元素。

这与我们添加删除活动的版本 3 非常相似。我们创建一个名为`UpdateActivity`的新类。我们以与删除活动相同的方式更新`MainActivity`类的`onOptionsItemSelected`方法（见示例 5.20 的第 39–40 行）和`AndroidManifest.xml`文件（见示例 5.21 的第 33–36 行）。

![](img/ch05exa20.jpg)

示例 5.20 `MainActivity`类，糖果店应用，版本 4

![](img/ch05exa21.jpg)



## 示例 5.21

`AndroidManifest.xml`文件，糖果店应用，版本 4

## 示例 5.22

示例 5.22 展示了`UpdateActivity`类。如图 5.5 所示，我们希望显示所有糖果的列表。对于每个糖果，我们在`TextView`中显示其 id，在`EditText`中显示其名称和价格以便编辑，并提供一个按钮来更新数据库中该糖果的名称和价格。与删除活动类似，点击按钮会更新糖果并刷新屏幕。

与删除活动一样，我们需要通过代码创建 GUI，并将`ScrollView`包裹在糖果列表中。为简化此示例，我们不提供返回上一活动的返回按钮。用户可以使用设备的返回按钮返回。我们将组件组织成一个四列的网格：第一列用`TextView`放置 id，第二列和第三列用`EditText`放置名称和价格，第四列放置按钮。与之前一样，`updateView`方法创建 GUI，并在`onCreate`中以及用户更新糖果后调用。

在第 32 至 36 行创建了`ScrollView`和`GridLayout`。在第 38 至 41 行创建了`TextView`、`EditText`和`Button`的数组。

![](img/ch05exa22.jpg) ![](img/ch05exa22a.jpg) ![](img/ch05exa22b.jpg)

示例 5.22 `UpdateActivity`类，糖果店应用，版本 4

![](img/9781284093650_CH05_FIGF05.jpg)

图 5.5 糖果店应用的更新界面，版本 4

我们将屏幕宽度按如下方式分配给四个组件：

- ▸ id 占 10%。
- ▸ 名称占 40%。
- ▸ 价格占 15%。
- ▸ 按钮占 35%。

在第 75 至 83 行将每个组件添加到`GridLayout`时，我们按上述指定宽度分配。在第 44 至 47 行获取屏幕宽度，并将其赋给变量`width`。

在第 51 至 86 行，我们遍历`Candy`对象的`ArrayList`。在第 52 至 55 行为 id 创建`TextView`。在第 57 至 65 行创建`EditText`。在第 64 至 65 行为它们分配唯一的`id`，以便稍后访问它们来获取用户输入的名称和价格。在第 67 至 70 行创建`Button`。我们还为每个`Button`分配唯一的`id`（第 70 行），即对应`Candy`对象的`id`。`View.OnClickListener`接口的`onClick`方法的参数是一个`View`，它是对被点击`View`的引用。这样，我们可以通过获取该`View`的`id`来检索要更新的糖果的 id。在第 72 至 73 行，我们设置事件处理。

我们在第 87 行将网格添加到`ScrollView`，并在第 88 行将`ScrollView`设置为此活动的内容`View`。

图 5.5 展示了更新界面。点击更新按钮会更新对应的糖果并刷新屏幕。用户正在更新核桃巧克力糖果的价格。再次强调，如果我们在未先插入糖果的情况下运行版本 4，`candy`表为空，点击更新图标时不会显示任何糖果。

## 5.6 运行收银机：糖果店应用，版本 5

在版本 5 中，我们允许用户使用第一个屏幕将应用作为收银机运行。我们提供一个按钮网格，每个糖果对应一个按钮。店员可以使用这些按钮计算购买糖果的顾客应付的总金额。每次用户点击一个按钮，我们将对应糖果的价格添加到该顾客的总金额中，并通过`Toast`显示总金额。

当用户点击按钮时，我们需要访问与该按钮关联的糖果的价格。解决该问题的一个简单方法是创建一个新类`CandyButton`，它继承`Button`类并拥有一个`Candy`实例变量。如示例 5.23 所示。我们包含一个`getPrice`方法（第 14–16 行），返回`Candy`实例变量的价格。这样，`CandyButton`“知道”其关联`Candy`的价格。

![](img/ch05exa23.jpg)

示例 5.23 `CandyButton`类，糖果店应用，版本 5

该应用需要为多个客户服务。因此，我们需要一种方法，在当前客户处理完毕后，将运行总计重置为`0`，以便为下一位客户做好准备。一个简单的做法是在菜单中增加一个选项，当用户点击该选项时，将总计重置为`0`。因此，我们在菜单中添加了一个选项，如示例 5.24 的第 5–8 行所示。我们在`strings.xml`文件中添加了一个名为`reset`的`String`，其值为`RESET`（未显示）。我们还添加了自己的图标，存储在`ic_reset.png`文件中，并将其放置在`drawable`目录中。在第 7 行，我们使用表达式`@drawable/ic_reset`来引用该图标。

与删除和更新活动中的做法类似，我们需要将按钮放置在`ScrollView`中，因为每次运行应用时，我们无法预知按钮的数量。一个简单的方法是将`content_main.xml`中的`RelativeLayout`替换为`ScrollView`元素，如示例 5.25 所示。我们为其指定一个 id（第 12 行），以便在`MainActivity`类中获取它。同时，我们移除了`ScrollView`内部的填充。

![](img/ch05exa24.jpg)

示例 5.24 `menu_main.xml`文件，糖果店应用，版本 5

![](img/ch05exa25.jpg)

示例 5.25 `content_main.xml`文件，糖果店应用，版本 5

示例 5.26 展示了更新后的`MainActivity`类。它包含四个实例变量（第 19–22 行）：一个`DatabaseManager`类型的`dbManager`，用于查询数据库以获取糖果；一个`double`类型的`total`，用于跟踪当前客户的运行总计；一个`scrollView`，是对`content_main.xml`中定义的`ScrollView`的引用；以及`buttonWidth`，表示每个按钮的宽度。我们在第 30 行实例化`dbManager`，在第 31 行将`total`初始化为`0.0`，在第 32 行实例化`scrollView`，并在第 33–35 行计算`buttonWidth`。我们希望按钮的宽度为屏幕宽度的一半，因此将屏幕宽度的一半赋值给变量`buttonWidth`。当用户处理完当前客户并点击重置图标（第 104 行）时，我们将运行总计重置为`0.0`（第 105 行），以便应用准备好计算下一位客户的总计。

![](img/ch05exa26.jpg) ![](img/ch05exa26a.jpg) ![](img/ch05exa26b.jpg)

示例 5.26 `MainActivity`类，糖果店应用，版本 5

`updateView`方法（第 44–77 行）创建图形用户界面并设置事件处理。我们在应用启动时的`onCreate`方法中（第 36 行）调用`updateView`，也在用户从添加、删除或更新等次要活动返回时的`onResume`方法中（第 41 行）调用它。实际上，当用户从次要活动返回时，`candy`表的内容可能已经发生变化，因此有必要通过调用`updateView`来更新第一个屏幕。当用户返回到此活动时，`onResume`方法会自动被调用。

`updateView`方法与`UpdateActivity`类中的`updateView`方法有相似之处。用户可能在返回此视图之前添加、删除或更新了一个或多个糖果。因此，在重建`scrollView`之前，我们首先在第 47–48 行移除`scrollView`中的所有按钮。我们动态创建一个按钮网格，每个糖果对应一个按钮。每行包含两个按钮（第 53 行）。我们计算行数，以确保有足够的空间容纳所有按钮（第 52 行）。与删除和更新活动类似，我们将网格放入`ScrollView`中，以便在需要时自动滚动（第 75 行）。

在每个按钮内部，我们显示糖果的名称和价格，各占一行（第 62–65 行）。较长的糖果名称可能需要单独占用两行。我们可以动态设置每个按钮的字体大小，使每个糖果名称都能在一行内显示。这超出了本章的范围，但我们在附录 A 中进行了说明。我们在第 67–68 行设置事件处理。

当用户点击按钮时，会调用`ButtonHandler`类的`onClick`方法（第 113–120 行）。我们更新`total`（第 115 行），并显示一个格式化为货币值的`Toast`（第 116–119 行）。使用`CandyButton`类的好处体现在第 115 行，我们将表示被点击按钮的`View`参数`v`强制转换为`CandyButton`，并调用`getPrice`来获取对应糖果的价格。

图 5.6 展示了所有糖果以及用户选择巧克力曲奇和核桃巧克力后的当前运行总计$4.48。请注意菜单右侧显示的三个垂直点，因为空间不足以容纳所有图标。触摸这三个点会打开一个子菜单，显示缺失的选项。

![](img/9781284093650_CH05_FIGF06.jpg)

图 5.6 运行糖果店应用的收银机，版本 5

## 章节总结

- 我们可以将菜单项放置在操作栏中。
- 菜单项可以是文本或图标。
- 菜单可以在 XML 文件中定义，例如自动生成的`menu_main.xml`，使用`menu`元素内的`item`元素。
- `Activity`类的`onCreateOptionsMenu`方法会在活动启动时自动调用。
- 点击菜单中的某个项会触发对`onOptionsItemSelected`方法的调用。
- 如果我们为每个项指定 id，就可以判断选择了哪个项。
- SQLite 在每个 Android 设备上都可用。
- SQLite 允许我们以关系数据库的方式组织数据，并执行 SQL 查询。
- 为了执行数据库操作，我们扩展`SQLiteOpenHelper`类。
- `SQLiteOpenHelper`的`getWritableDatabase`方法会为当前应用创建或返回一个`SQLiteDatabase`对象。
- `SQLiteDatabase`类包含执行 SQL 查询的方法。
- 要执行插入、更新和删除查询，我们使用`SQLiteDatabase`的`execSQL`方法。
- 要执行选择查询，我们使用`SQLiteDatabase`的`rawQuery`方法。
- `rawQuery`方法返回一个`Cursor`对象，允许我们遍历查询结果。
- 我们可以使用`Toast`类向用户提供临时视觉反馈。
- 使用 SQLite 通常需要以编程方式构建图形用户界面，因为我们无法预先知道界面中会有多少组件。
- 使用 SQLite 还需要使用`ScrollView`，以防屏幕不足以容纳所有组件。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. 使用基本活动模板时自动生成的菜单代码放置在：
   - 整个屏幕
   - 操作栏
   - 屏幕底部

2. 可以在菜单中放置图标：
   - 正确
   - 错误

3. 定义菜单的 XML 文件中通常包含什么？
   - 一个`menu`元素及其内部的`item`元素
   - 一个`item`元素及其内部的`menu`元素
   - 仅`item`元素
   - 仅`menu`元素

4. SQLite 在 Android 设备上可用：
   - 正确，无需特殊安装
   - 否
   - 否，但可以安装

5. 为了管理数据库操作，我们扩展的类名称是什么？
   - `Sqlite`
   - `SQLite`
   - `SQLiteOpenHelper`
   - `DatabaseHelper`

6. 问题 5 中类的`onCreate`方法：
   - 永远不会被调用
   - 每次实例化该类的对象时都会被调用
   - 仅在第一次实例化该类的对象时被调用

7. `SQLiteDatabase`类中用于执行插入、删除或更新 SQL 查询的方法名称是：
   - `execSQL`
   - `sqlExec`
   - `queryExec`
   - `exec`

8. `SQLiteDatabase`类中用于执行选择 SQL 查询的方法名称是：
   - `execSQL`
   - `query`
   - `rawQuery`
   - `sqlExec`

9. 第 8 题中方法的返回类型是：
   - `SQL`
   - `Cursor`
   - `ResultSet`
   - `Result`

### 填写代码

10. 在菜单的`item`元素内部，这行代码使得如果有空间，该项在操作栏中可见。

```xml
<item
  …
/>
```

11. 在菜单的`item`元素内部，这行代码指定该项的标题是定义在`strings.xml`中的字符串`test`的值。

```xml
<item
  …
/>
```

12. 在菜单的`item`元素内部，这行代码指定该项的图标是存储在`drawable`目录中名为`image.png`的文件。

```xml
<item
  …
/>
```

13. 在`AndroidManifest.xml`文件中，添加一个类型为`SecondActivity`类的`activity`元素。

```xml
</activity>
    <!-- 你的代码写在这里 -->

</application>
```

14. 当用户从菜单中选择 id 为`second`的项时，编写代码跳转到另一个类型为`SecondActivity`的活动。否则，不做任何操作。

```java
public boolean onOptionsItemSelected(MenuItem item) {
  // 你的代码写在这里
}
```

15. 编写`MyDBManager`类的类头。在该类中，我们打算创建一个数据库并执行 SQL 操作。

```java
// 你的代码写在这里
```

16. 在继承`SQLiteOpenHelper`的类内部，编写构造函数的代码。我们要创建的数据库名称为`FRIENDS`，版本为 3。

```java
public DatabaseManager(Context context) {
  // 你的代码写在这里
}
```

17. 在继承`SQLiteOpenHelper`的类内部，编写`onCreate`方法的代码。我们要创建表`emails`，定义如下：主键是`email`，字符串类型；还有另外两列`first`和`last`，均为字符串类型。

```java
public void onCreate(SQLiteDatabase db) {
   // 你的代码写在这里
}
```

18. 在继承`SQLiteOpenHelper`的类内部，编写下面`insert`方法的代码。我们要使用下面`insert`方法的三个参数值，向第 17 题中的`emails`表插入一条记录。

```java
public void insert(String email, String first, String last) {
   // 你的代码写在这里
}
```

19. 在继承`SQLiteOpenHelper`的类内部，编写下面`delete`方法的代码。我们要删除第 17 题中`emails`表里`last`值等于该方法参数值的记录。

```java
public void delete(String last) {
   // 你的代码写在这里
}
```

20. 在继承`SQLiteOpenHelper`的类内部，编写下面`update`方法的代码。我们要更新第 17 题中`emails`表里`email`值为`email`的记录。将该记录的`first`和`last`名称改为`first`和`last`。

```java
public void update(String email, String first, String last) {
   // 你的代码写在这里
}
```

### 编写一个应用

21. 修改本章的应用。在更新活动中添加一个返回按钮。

22. 编写一个类似于本章应用的应用，用于管理一组朋友：一个朋友定义为有名字、姓氏和电子邮件地址。朋友应存储在数据库中：可以添加或删除朋友；可以修改他/她的数据。

23. 编写一个类似于本章应用的应用，用于管理一组朋友：一个朋友定义为有名字、姓氏和电子邮件地址。朋友应存储在数据库中：可以添加、更新或删除朋友；可以修改他/她的数据。在第一个屏幕上，应显示所有朋友的列表。

24. 同 22，但增加以下功能：在第一个屏幕上提供一个搜索引擎，用户输入电子邮件；应用搜索数据库，如果该电子邮件存在，则返回对应的名字和姓氏。

25. 同 24，但为搜索引擎文本字段增加自动补全功能：当用户输入时，下拉列表会建议从数据库中检索到的可能匹配的电子邮件。你应该查看`AutoCompleteTextView`来实现此功能。

26. 编写一个进行错误纠正的应用。构建一个包含一个表的数据库。该表有两列：一列存储拼写错误的单词，另一列存储对应的正确单词（例如，`the`是`teh`的正确单词）。该表的内容可以硬编码，并且至少应包含五对单词。应用显示一个`EditText`：当用户输入时，应用根据表的内容纠正拼写错误的单词。

27. 同 26，但增加以下功能：用户可以在表中添加拼写错误和正确单词的对。

28. 同 26，但增加以下功能：用户可以删除和更新拼写错误和正确单词的对。

29. 编写一个问答应用，其中问题和答案存储在数据库的表中。表的内容可以硬编码。



30. 同`29`，但增加以下功能：用户可以在表中添加问题和答案的对。

31. 同`29`，但增加以下功能：用户可以删除和更新问题和答案的对。

32. 编写一个维护存储在数据库中的待办事项列表的应用。用户可以添加项目到列表并删除它们。

33. 同`32`，但增加以下功能：待办事项列表显示在第一个屏幕上。

34. 同`32`，但增加以下功能：对于待办事项列表中的每个项目，我们在数据库中存储一个截止日期。第一个屏幕应显示待办事项列表中的所有项目，并且已过期的项目应显示为红色。

# 第六章：管理设备方向

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

当我们运行一个应用并旋转运行该应用的设备时，图形用户界面（GUI）可能会旋转，也可能不会。有些应用，尤其是游戏，最好只在一种方向下运行，通常是水平方向。但有时，我们希望构建一个在水平和垂直方向都能工作的应用，以便为用户提供更好的体验，并扩大应用的覆盖范围。有些用户可能更喜欢在水平方向运行应用，而另一些用户可能更喜欢在垂直方向运行。默认行为是应用自动旋转。如果我们想阻止应用旋转，需要在`AndroidManifest.xml`的`activity`元素内将`android:screenOrientation`属性的值指定为`portrait`或`landscape`。例如，如果我们希望应用仅在水平方向运行，可以指定如下：

```xml
<activity
  android:screenOrientation="landscape"
```

在本章中，我们希望应用在两个方向都能运行。我们使用空活动模板，这样开始时视图中没有任何内容。

## 6.1 `Configuration`类

`Configuration`类来自`android.content.res`包，封装了设备的配置信息，例如区域设置、输入模式、屏幕尺寸或屏幕方向。本章我们重点关注屏幕方向。表 6.1 展示了该类的一些`public`字段和方法。方向字段可以有两个值，如表 6.2 所示：`ORIENTATION_LANDSCAPE`（常数值为 2）和`ORIENTATION_PORTRAIT`（常数值为 1）。

| 字段或方法 | 描述 |
| --- | --- |
| `public int keyboard` | 设备的键盘。 |
| `public Locale locale` | 用户对区域设置的偏好。 |
| `public int orientation` | 表示屏幕方向的整数值。 |
| `public int screenHeightDp` | 屏幕高度（不包括状态栏），以 dp 单位（密度无关像素）表示。 |
| `public int screenWidthDp` | 屏幕宽度，以 dp 为单位。 |
| `public boolean isLayoutSizeAtLeast(int size)` | 检查设备屏幕是否至少达到指定尺寸。 |

表 6.1 `Configuration`类中选定的`public`字段和方法

| 常量 | 值 |
| --- | --- |
| `ORIENTATION_LANDSCAPE` | 2 |
| `ORIENTATION_PORTRAIT` | 1 |

表 6.2 `Configuration`类`orientation`字段的常量值

| 常量 | 值 |
| --- | --- |
| `SCREENLAYOUT_SIZE_UNDEFINED` | 0 |
| `SCREENLAYOUT_SIZE_SMALL` | 1 |
| `SCREENLAYOUT_SIZE_NORMAL` | 2 |
| `SCREENLAYOUT_SIZE_LARGE` | 3 |
| `SCREENLAYOUT_SIZE_XLARGE` | 4 |

表 6.3 `Configuration`类中与设备屏幕尺寸相关的常量值

| 类 | 方法 |
| --- | --- |
| `Context` | `Resources getResources()` |
| `Resources` | `Configuration getConfiguration()` |

表 6.4 `getResources`和`getConfiguration`方法

`Configuration`类提供了常量，可用作`isLayoutSizeAtLeast`方法的参数（列于表 6.3）。`SCREENLAYOUT_SIZE_SMALL`和`SCREENLAYOUT_SIZE_NORMAL`常量适用于智能手机，而`SCREENLAYOUT_SIZE_LARGE`和`SCREENLAYOUT_SIZE_XLARGE`适用于平板电脑。

利用这些资源，我们可以在应用启动时检测运行应用的设备信息。要使用这些资源，我们需要一个`Configuration`引用。在`Activity`类内部，我们可以从`Context`类（`Activity`继承自该类）调用`getResources`方法，以获取应用包的`Resources`引用。利用该`Resources`引用，我们可以调用`Resources`类的`getConfiguration`方法来获取`Configuration`引用。表 6.4 列出了这两个方法。

因此，在`Activity`类内部，我们可以使用这两个方法来获取`Configuration`对象，如下所示：

```java
Resources resources = getResources();
Configuration config = resources.getConfiguration();
```

我们也可以将这两个方法调用链式连接，如下所示：

```java
Configuration config = getResources().getConfiguration();
```

在示例 6.1 中，我们使用一个修改后的 HelloAndroid 应用来演示如何检索设备信息。在第 18 行，我们获取当前应用环境的`Configuration config`引用。在第 19–20 行，我们以密度无关像素（dp）为单位输出屏幕的高度和宽度。要获得实际尺寸，我们需要将这些值乘以像素密度。注意，`screenHeightDp`存储的是屏幕高度，不包括状态栏。

在第 22–27 行，我们以实际像素为单位检索屏幕尺寸，并输出其宽度和高度。在第 29–32 行，我们检索并输出屏幕的像素密度。附录 A 给出了详细解释。

在第 34–47 行，我们测试屏幕的相对尺寸并输出结果。注意，我们按降序测试相对尺寸。如果先测试“至少”为小屏幕，则结果始终为`true`。在第 49–52 行，我们输出`Configuration`类的两个常量`ORIENTATION_LANDSCAPE`和`ORIENTATION_PORTRAIT`（分别为 2 和 1）。在第 53 行，我们以整数形式输出设备的`orientation`值。在第 54–59 行，我们将该值与前面两个常量进行比较，并输出设备的方向。

![](img/ch06exa01.jpg) ![](img/ch06exa01a.jpg)

示例 6.1 获取运行应用设备的信息

图 6.1 展示了设备屏幕的各个部分。黄色部分是设备的状态栏。它通常包含一些系统和应用通知的图标，包括时钟。红色部分是应用的操作栏，通常左侧显示应用名称，右侧显示可选的菜单项，但具体内容可能因应用而异。蓝色部分是应用的内容视图，即应用内容所在的位置。可见的显示框架由应用的操作栏（红色）和应用内容视图（蓝色）组成。

图 6.2 显示了在 Nexus 5 模拟器上以竖屏方向启动时，示例 6.1 在 Logcat 中的输出。输出确认设备处于竖屏方向，该方向下屏幕尺寸为 568 dp × 360 dp，属于正常尺寸屏幕。方向值为 1，等于竖屏常量。高度尺寸（568 dp）包含操作栏高度，但不包含状态栏高度。逻辑像素密度为 3；568 dp 相当于 1,704 像素（568 × 3），比屏幕高度 1,776 像素少 72 像素。这 72 像素相当于 24 dp，即状态栏的高度。

如果我们旋转模拟器（`Ctrl+F11`），会看到更多输出，这意味着`onCreate`方法再次执行。此外，横屏方向下的屏幕尺寸不同：高度为 336 dp，宽度为 598 dp。竖屏方向下操作栏高度为 56 dp，横屏方向下仅为 48 dp。此外，返回键和主页键在竖屏方向下位于屏幕底部，而在横屏方向下位于屏幕右侧。

如果我们将模拟器保持在横屏方向并重新启动应用，输出显示我们检测到设备处于横屏方向。

如果在 Nexus 4 模拟器中运行该应用，可以看到 Nexus 4 的逻辑像素密度仅为 2，高度和宽度分别为 568 dp 和 384 dp。

![](img/9781284093650_CH06_FIGF01.jpg)

图 6.1 屏幕的视图组件

![](img/9781284093650_CH06_FIGF02.jpg)

图 6.2 示例 6.1 的 Logcat 输出

## 6.2 捕获设备旋转事件

用户可能以某个方向启动应用，但随后旋转设备。如果我们构建的应用需要同时支持两种方向，则必须对代码进行相应设计，使其能够正确响应设备方向的变化。默认情况下，当用户旋转设备时，`Activity`类的`onCreate`方法会被调用。然而，`onCreate`方法通常不仅仅处理方向变化。因此，每次用户旋转设备都执行`onCreate`可能会浪费 CPU 资源。

`Activity`类的`onConfigurationChanged`方法（如表 6.5 所示）会在设备配置发生变化时（例如用户旋转设备）自动调用，前提是我们已在`AndroidManifest.xml`文件中指定了该配置。相应地，`onCreate`方法仅在用户启动应用时调用，而不再在用户旋转设备时调用。`onConfigurationChanged`方法的`newConfig`参数表示设备的最新配置。

在希望收到设备配置变化通知的`activity`元素内部，我们需要添加`android:configChanges`属性，并为其赋予一个或多个适当的值。我们可以使用`|`字符分隔多个值。表 6.6 展示了选定的值。如果我们希望在用户旋转设备时收到通知，则需要将`orientation`赋值给`android:configChanges`。然而，从 API 级别 13 开始，我们还需要添加`screenSize`值。实际上，系统认为当用户旋转设备时屏幕尺寸会发生变化。因此，我们需要为`android:configChanges`属性指定值`orientation|screenSize`，如下所示（注意`orientation`与`|`之间、`|`与`screenSize`之间没有空格）：

```xml
<activity
  android:name=".MainActivity"
  android:configChanges="orientation|screenSize">
```

我们使用另一个修改过的`HelloAndroid`应用，演示在示例 6.2 中，当用户旋转设备时，如何在`onConfigurationChanged`方法内部执行代码。我们可以利用该方法的`newConfig`参数（第 16–28 行）来检测设备当前的方向，并为应用编写相应的更改代码。在这个简单的应用中，我们在第 18–19 行输出屏幕尺寸信息，在第 21–27 行输出方向信息。

| 方法 | 描述 |
| --- | --- |
| `void onConfigurationChanged(Configuration newConfig)` | 当`AndroidManifest.xml`文件中指定的配置之一发生变化时调用。 |

表 6.5 `Activity`类的`onConfigurationChanged`方法

| 属性值 | 含义 |
| --- | --- |
| `orientation` | 用户旋转了设备。 |
| `screenSize` | 屏幕尺寸发生了变化。 |
| `locale` | 语言区域发生了变化（用户选择了新语言）。 |
| `keyboard` | 键盘类型发生了变化。 |
| `fontScale` | 用户选择了新的全局字体大小。 |

表 6.6 `activity`元素的`android:configChanges`属性的部分取值

![](img/ch06exa02.jpg)

示例 6.2 在`onConfigurationChanged`方法中检测配置变化

如果我们从竖屏方向启动应用，在旋转设备（`Ctrl+F11`）到横屏方向之前不会有任何输出。旋转后，会输出图 6.3 的前四行。当我们再次旋转设备（`Ctrl+F12`）回到竖屏方向时，会输出图 6.2 的后四行。可以看到，屏幕的尺寸因设备方向不同而有所差异。

现在我们拥有了在用户旋转设备时检测方向和屏幕尺寸的工具。有多种方法可以向用户显示正确的布局，包括：

- 为每个方向准备一个布局 XML 文件，并在用户旋转设备时加载对应的文件。
- 为两个方向使用同一个布局 XML 文件，并在用户旋转设备时修改某些 GUI 组件的特性。
- 完全通过代码管理布局，并在用户旋转设备时进行适当的修改。

![](img/9781284093650_CH06_FIGF03.jpg)

图 6.3 示例 6.1 的`Logcat`输出

## 6.3 策略 1：每个方向一个布局 XML 文件

我们已经有一个布局 XML 文件`activity_main.xml`，如示例 6.3 所示。我们将其用于竖屏方向：在第 17 行为`TextView`元素添加背景色（绿色），并在第 18 行使用名为`portrait`的`String`修改显示的文本。我们添加另一个布局 XML 文件`activity_main_landscape.xml`，如示例 6.4 所示，用于横屏方向。这次，我们在第 17 行将`TextView`元素的背景色设置为红色，并在第 18 行使用`String` `landscape`显示文本。`portrait`和`landscape`这两个`String`在示例 6.5 的`strings.xml`文件的第 3 行和第 4 行定义。我们还编辑了`styles.xml`文件，如示例 6.6 所示，使文本大小足够大（第 3 行）。

现在资源文件已设置好，我们编写`MainActivity`类。如果设备处于竖屏方向，我们使用`activity_main.xml`文件作为布局；如果设备处于横屏方向，我们使用`activity_main_landscape.xml`文件作为布局。我们不仅需要在`onConfigurationChanged`方法中执行此操作，还必须在`onCreate`方法中执行，以便在应用启动时使用正确的布局文件。实际上，应用启动时设备可能处于横屏或竖屏方向。由于相同的代码会执行两次，我们编写了一个新方法`modifyLayout`（示例 6.7 的第 20–25 行），该方法从`onCreate`（第 12 行）和`onConfigurationChanged`（第 17 行）调用。`modifyLayout`方法测试设备的方向，并为其设置布局，加载相应的 XML 文件。

![](img/ch06exa03.jpg)

示例 6.3 竖屏方向的`activity_main.xml`文件

![](img/ch06exa04.jpg)

示例 6.4 横屏方向的`activity_main_landscape.xml`文件

![](img/ch06exa05.jpg)

示例 6.5 `strings.xml`文件

![](img/ch06exa06.jpg)

示例 6.6 `styles.xml`文件

![](img/ch06exa07.jpg) ![](img/ch06exa07a.jpg)

示例 6.7 使用两个 XML 布局文件管理方向变化

图 6.4 显示了设备处于竖屏方向时在模拟器中运行的应用，图 6.5 显示了我们将设备旋转到横屏方向后的应用。如果我们在`onCreate`和`onConfigurationChanged`中添加输出语句到`Logcat`，我们会看到`onCreate`仅在应用启动时被调用，之后旋转设备时不再调用。相反，`onConfigurationChanged`被调用。如前所述，这是因为我们在`AndroidManifest.xml`文件的`activity`元素中添加了：

```xml
android:configChanges="orientation|screenSize"
```

![](img/9781284093650_CH06_FIGF04.jpg)

图 6.4 应用在模拟器中运行，初始为竖屏方向

![](img/9781284093650_CH06_FIGF05.jpg)

图 6.5 应用在模拟器中运行，旋转到横屏方向后

## 6.4 策略 2：两个方向共用一个布局 XML 文件，通过代码修改布局



现在我们来看另一种根据屏幕方向控制布局的策略。我们只使用一个 XML 布局文件，但根据屏幕方向以编程方式修改其中某些组件的布局参数。

为了更好地说明这一点，我们修改了`activity_main.xml`，如示例 6.8 所示。它在`LinearLayout`（第 2 行）中显示三个按钮（第 10、15 和 21 行）。`LinearLayout`线性地组织元素，根据其`android:orientation`属性的值决定水平或垂直排列。在这个应用中，我们指定元素垂直排列（第 6 行）。

如果无论屏幕方向如何，我们都保持按钮之间的间距恒定（例如 50 像素），那么应用可能在一个方向（例如竖屏）看起来不错，但在另一个方向（例如横屏）看起来很差。相反，我们可以根据方向通过代码设置按钮之间的间距。

为此，我们需要在运行时访问第二个和第三个按钮，因此我们在第 16 行和第 22 行为它们分配了 id。第 13、19 和 25 行使用`strings.xml`文件中定义的`view1`、`view2`和`view3`这三个`String`来指定三个按钮的文本，`strings.xml`文件如示例 6.9 所示。我们使用与示例 6.6 相同的`styles.xml`文件。

![](img/ch06exa08.jpg)

示例 6.8 `activity_main.xml`文件

![](img/ch06exa09.jpg)

示例 6.9 `strings.xml`文件

为了使应用在两个方向上都看起来不错，我们需要在`MainActivity`类中通过代码设置按钮之间的间距。如果设备处于竖屏方向，我们将间距设置为 50 像素；如果设备处于横屏方向，则将间距设置为 25 像素。

示例 6.10 显示了新的`MainActivity`类。这次，我们在`onCreate`方法中加载 XML。和之前一样，`onCreate`和`onConfigurationChanged`都调用`modifyLayout`，该方法设置按钮之间的间距参数。

`modifyLayout`方法（第 25–41 行）在第 26 和 29 行获取第二和第三个按钮，然后在第 27–28 行和第 30–31 行获取它们关联的边距布局参数。

![](img/ch06exa10.jpg) ![](img/ch06exa10a.jpg)

示例 6.10 使用两个 XML 布局文件管理方向变化

Android 框架包含布局参数类，我们可以用它们来设置布局中包含的 GUI 组件的布局参数。这些类的根类是`ViewGroup.LayoutParams`。它有许多专门化的子类，对应于专门的`ViewGroup`，包括`TableLayout.LayoutParams`、`RelativeLayout.LayoutParams`、`LinearLayout.LayoutParams`或`ViewGroup.MarginLayoutParams`。`ViewGroup.MarginLayoutParams`类（`MarginLayoutParams`是`ViewGroup`的一个`public static`内部类）用于设置 GUI 组件的边距。

表 6.7 展示了`ViewGroup.MarginLayoutParams`的一些 XML 属性及其对应的方法。虽然有四个属性，但我们可以通过一个方法`setMargins`来设置它们。

| 属性名称 | 相关方法 |
| --- | --- |
| `android:layout_marginBottom` | `setMargins( int left, int top, int right, int bottom )` |
| `android:layout_marginTop` | `setMargins( int left, int top, int right, int bottom )` |
| `android:layout_marginLeft` | `setMargins( int left, int top, int right, int bottom )` |
| `android:layout_marginRight` | `setMargins( int left, int top, int right, int bottom )` |

表 6.7 `ViewGroup.MarginLayoutParams`的选定 XML 属性及`setMargins`方法

![](img/9781284093650_CH06_FIGF06.jpg)

图 6.6 应用在垂直方向运行时，按钮之间间距为 50 像素

![](img/9781284093650_CH06_FIGF07.jpg)

图 6.7 应用在水平方向运行时，按钮之间间距为 25 像素

我们在第 33 行和第 36–37 行测试方向，并根据方向在第 34–35 行或第 38–39 行设置两个按钮布局参数的上边距。我们使用在第 10–11 行定义的两个常量`SPACING_VERTICAL`和`SPACING_HORIZONTAL`。`MarginLayoutParams`、`params2`和`params3`是对象引用，因此当我们修改它们时，会自动修改与之关联的两个按钮的布局参数。

和之前一样，我们在`AndroidManifest.xml`文件的`activity`元素中添加：

```
android:configChanges="orientation|screenSize"
```

图 6.6 和 6.7 分别展示了设备处于垂直方向和水平方向时，应用在模拟器中运行的情况。

在此示例中，我们硬编码了按钮之间的间距。因此，应用在某些设备上可能看起来效果不佳。在下一个示例中，我们将根据应用运行设备的尺寸动态设置间距。

## 6.5 策略 3：100%通过代码管理布局和方向

在前一个示例中，我们可以在`dimens.xml`文件中设置一些`dimen`元素，以定义多个间距值来适配不同的屏幕尺寸。这种策略对大多数当前设备有效，但可能无法很好地适用于未来设备。

为了获得最大的灵活性并使 GUI 适应任何屏幕尺寸，我们可以完全通过代码控制一切，而不使用任何布局 XML 文件。我们不加载布局 XML 文件，而是调用一个方法以编程方式设置布局。此外，我们调用另一个方法来设置 View 的 GUI 组件的布局参数。

前一个示例的基本原理同样适用于管理方向：每次用户旋转设备时，都会调用`onConfigurationChanged`，进而调用`modifyLayout`。然而，这个应用更复杂，因为我们需要在应用启动时捕获与屏幕尺寸相关的信息，以便根据初始方向正确显示 GUI 组件。

总体而言，我们用一种以编程方式设置 GUI 的方法以及对它的调用来替换布局 XML 文件和`setContentView`的调用。同样，我们使用与示例 6.6 相同的`styles.xml`文件。

我们需要在应用内容视图（即图 6.1 中屏幕的蓝色区域）内显示按钮。我们希望按钮无论设备方向如何都能均匀分布，如图 6.8 所示。

![](img/9781284093650_CH06_FIGF08.jpg)

图 6.8 三个按钮等间距分布

如果`h`是屏幕高度，`a`是按钮之间的间距，`b`是按钮的高度，那么（假设我们使用三个按钮）：

`h = 4 * a + 3 * b`

因此，

`a = (h – 3 * b)/4`

我们可以通过调用尚未显示的 View 的`measure`方法，然后调用其`getMeasuredHeight`方法来测量其尺寸，如表 6.8 所示。如果`button`是一个`Button`引用，我们可以按如下方式获取其高度：

```
button.measure(LayoutParams.WRAP_CONTENT, LayoutParams.WRAP_CONTENT);
int buttonHeight = button.getMeasuredHeight();
```

为了计算`a`（按钮之间的间距），我们需要先计算`h`（应用内容视图的高度）。我们可以按如下方式获取操作栏的高度。一旦获得它，我们就可以轻松计算应用内容视图的高度。附录 A 提供了详细解释。

```
 // 设置操作栏高度的默认值
int actionBarHeight = (int) (pixelDensity * 56);
TypedValue tv = new TypedValue();
if (getTheme().resolveAttribute(android.R.attr.actionBarSize, tv, true))
    actionBarHeight = TypedValue.complexToDimensionPixelSize(
        tv.data,
        getResources().getDisplayMetrics()
    );
```

| 方法 | 说明 |
| --- | --- |
| `public void measure(int widthMeasureSpec, int heightMeasureSpec)` | 这两个参数是由该 View 的父级提供的维度约束信息。 |
| `public int getMeasuredHeight()` | 返回该 View 的测量高度。 |

表 6.8 `View`类的`measure`和`getMeasuredHeight`方法

在示例 6.1 中，我们学习了如何获取减去状态栏后的屏幕高度。因此，要计算内容视图的高度，我们执行以下操作：

```
获取减去状态栏后的屏幕高度：appScreenHeight
获取操作栏的高度：actionBarHeight
内容视图的高度 = appScreenHeight - actionBarHeight
```

示例 6.11 展示了一个简单的应用，其 View 由代码定义，方向变化也由代码管理。如图 6.8 所示，屏幕包含三个按钮，在水平和垂直方向上均垂直等间距分布。

除了三个按钮外，我们还声明了实例变量来存储各种尺寸：操作栏的高度、两种方向下的屏幕高度以及按钮之间的间距。我们还声明了两个`boolean`状态变量`verticalDimensionsSet`和`horizontalDimensionsSet`（第 20 和 24 行），以便只设置一次这些变量，而不是每次设备改变方向时都设置。

其中一些变量被声明为`public`和`static`，以便在必要时可以轻松地从其他 Activity 访问——很可能，如果应用中有其他 Activity，我们将需要在这些 Activity 中访问这些值，原因与在此 Activity 中需要访问它们相同，并且我们不想重写相同的代码来获取它们。

![](img/ch06exa11.jpg) ![](img/ch06exa11a.jpg) ![](img/ch06exa11b.jpg)

示例 6.11 仅通过代码管理方向

`onCreate`方法（第 31–40 行）在第 33 行调用了`setUpGui`。`setUpGui`方法编码在第 70–94 行：它为视图设置布局管理器，创建按钮，并将它们添加到视图中。

为了获取操作栏高度、屏幕尺寸以及计算按钮之间的间距，我们在第 38 行调用了一个单独的方法`checkDimensions`。在第 39 行，我们调用`modifyLayout`，该方法根据设备的方向正确显示按钮。由于我们不知道应用启动时设备处于何种方向，我们在第 37 行将当前配置赋值给变量`config`，并将`config`传递给`checkDimensions`和`modifyLayout`。

在`setUpGui`内部，我们在第 71 行声明并实例化了一个`LinearLayout`类型的`linearLayout`，并在第 72 行将其方向设置为垂直。这意味着其中的按钮是垂直排列的。我们在第 73 行将其重力设置为垂直居中，这意味着其中的按钮在垂直方向上居中。

我们在第 75–77 行实例化了三个按钮，并在第 79–81 行设置了它们各自的文本。我们在第 83–84 行实例化了一个`LayoutParams`对象，并在第 85–87 行使用它为所有三个按钮设置布局参数为`WRAP_CONTENT`。

我们在第 89–91 行将按钮添加到`linearLayout`，并在第 93 行将此活动的内容视图设置为`linearLayout`。`setUpGui`方法没有设置按钮之间的间距，因为该值取决于设备方向。因此，我们希望在调用`onConfigurationChanged`方法时以及应用启动时设置它。

我们编写了一个单独的方法`setLayoutMargins`来实现这一点，位于第 103–114 行。该方法接受一个参数，即两个按钮之间的间距。根据设备的位置，我们在调用该方法时传递不同的参数值。

`checkDimensions`方法（第 42–68 行）获取操作栏高度，并为各种与尺寸相关的实例变量赋值。我们只想执行两次：应用启动时，以及用户首次旋转设备后。因此，在`onConfigurationChanged`内部，只有当`verticalDimensionsSet`或`horizontalDimensionsSet`为`false`时（第 98 行），我们才调用`checkDimensions`。

`checkDimensions`方法获取操作栏的高度，以及两种方向下的屏幕高度。我们将它们赋值给实例变量`actionBarHeight`、`screenHeightInHP`和`screenHeightInVP`。我们还获取按钮的高度（第 52–54 行），并在第 59–60 行和第 64–65 行计算`spacingInHP`和`spacingInVP`的值。

我们在第 50 行输出操作栏高度的值，用于反馈。图 6.9 显示了我们在垂直方向启动应用并旋转设备后的输出。操作栏的高度在垂直方向为 168 像素（56 dp），在水平方向为 144 像素（48 dp）。

在本章前面，我们展示了屏幕高度（不包括状态栏）在垂直方向为 1,704 像素（568 dp × 3），在水平方向为 1,008 像素（336 dp × 3）。因此，对于我们的模拟器，应用内容视图的高度在垂直方向为 1,536 像素（1,704 – 168），在水平方向为 864 像素（1,008 – 144），如图 6.10 和图 6.11 所示。

![](img/9781284093650_CH06_FIGF09.jpg)

图 6.9 示例 6.11 的 Logcat 输出

![](img/9781284093650_CH06_FIGF10.jpg)

图 6.10 Nexus 5 模拟器垂直方向的高度

![](img/9781284093650_CH06_FIGF11.jpg)

图 6.11 Nexus 5 模拟器水平方向的高度

`modifyLayout`方法编码在第 116–121 行，它测试设备的方向（第 117 行和第 119 行），并使用适当的参数（`spacingInHP`或`spacingInVP`）调用`setLayoutMargins`方法（第 118 行和第 120 行）。

`onConfigurationChanged`方法编码在第 96–101 行。如果各个实例变量的值尚未设置（第 98 行），我们调用`checkDimensions`（第 99 行）。这只会发生一次，即用户首次旋转设备时。目前，操作栏高度在两种方向下相同。如果将来发生变化，本示例中的代码将需要修改。在第 100 行，我们调用`modifyLayout`，以便根据设备方向显示按钮。

`setLayoutMargins`方法编码在第 103–114 行。我们首先在第 104–109 行获取三个按钮的`MarginLayoutParams`引用`params1`、`params2`和`params3`。然后我们在第 111–113 行调用`setMargins`，将`spacing`作为其第二个参数传递，以设置每个按钮顶部的 y 坐标。

请记住，`params1`、`params2`和`params3`是对象引用，因此当我们修改它们时，我们实际上是在修改三个按钮的布局参数。

最后，请记住，为了在用户旋转设备时调用`onConfigurationChanged`方法，我们需要在`androidManifest.xml`文件中添加`activity`元素的`android:configChanges`属性：

```
<activity
    android:name=".MainActivity"
    android:configChanges="orientation|screenSize">
```

如果我们运行应用并旋转设备，垂直和水平方向的视图看起来就像图 6.6 和图 6.7 中所示，按钮在两种方向下均匀分布。

在撰写本文时，状态栏的高度在两种方向下均为 24 dp。如有必要，可以通过以下代码获取（附录 A 提供了详细说明）：

```
 // 设置状态栏高度的默认值
int statusBarHeight = (int) (pixelDensity * 24);
// res 是一个 Resources 引用
int resourceId =
    res.getIdentifier("status_bar_height", "dimen", "android");
// res.getIdentifier("android:dimen/status_bar_height", "", "");
if (resourceId != 0) // 找到状态栏高度的资源
    statusBarHeight = res.getDimensionPixelSize(resourceId);
```

## 章节总结

- 可以构建一个在两种方向下都能运行的应用：我们可以使用两个独立的布局 XML 文件，将单个布局 XML 文件与一些代码结合以处理两种方向，或者完全通过编程方式管理布局和方向。
- `Configuration`类包含用于访问设备信息的资源，例如键盘、区域设置、方向、屏幕尺寸等。它还包含一个方法和常量，用于测试当前设备是否至少达到某个尺寸。



- 可以使用`getResources`和`getConfiguration`方法来获取表示当前设备配置的`Configuration`引用。
- 当用户旋转设备时，如果`AndroidManifest.xml`文件的`activity`元素中定义了`android:onChanges`属性，则会自动调用`onConfigurationChanged`方法。
- 为了检测方向变化，`android:onChanges`的值应为`orientation|screenSize`。
- `LayoutParams`类及其子类可用于设置 GUI 组件的各种布局参数。
- 当应用运行时，屏幕通常分为三个部分：顶部的状态栏、操作栏（可能包含除应用名称之外的其他 GUI 组件）以及应用的内容视图。它们各自的高度可以通过编程方式获取。
- 在撰写本文时，状态栏的高度为 24 dp，并且在垂直和水平方向下相同。
- 在撰写本文时，操作栏的高度在垂直方向为 56 dp，在水平方向为 48 dp。
- 附录 A 详细说明了如何获取状态栏和操作栏的高度。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. `Configuration`类位于哪个包中？
   - `android.config`
   - `android.configuration`
   - `android.content`
   - `android.content.res`

2. `getConfiguration`方法位于哪个类中？
   - `Configuration`
   - `Resources`
   - `Activity`
   - `Context`

3. `getResources`方法
   - 可以从`Activity`类中调用，因为`Activity`从`Context`继承了它
   - 不能从`Activity`类中调用
   - 由系统自动调用
   - 由`Configuration`引用调用

4. `ORIENTATION_PORTRAIT`和`ORIENTATION_LANDSCAPE`
   - 是`Resources`类的常量
   - 是`Activity`类的常量
   - 是`Configuration`类的常量
   - 是`View`类的常量

5. 存储设备方向值的`Configuration`类实例变量名是
   - `config`
   - `name`
   - `position`
   - `orientation`

6. `Configuration`类的`screenHeightDp`实例变量存储（以 dp 为单位）
   - 状态栏的高度
   - 整个屏幕的高度，包括状态栏
   - 整个屏幕的高度，不包括状态栏
   - 整个屏幕的高度，不包括状态栏和操作栏

7. 当用户旋转设备时，如果`AndroidManifest.xml`文件正确编码，哪个方法会被自动调用？
   - `onConfigurationChanged`
   - `onRotate`
   - `onChange`
   - `onRotation`

8. 为了让问题 7 中的方法在用户旋转设备时自动调用，需要在`AndroidManifest.xml`文件中设置哪个属性？
   - `android:changes`
   - `android:configChanges`
   - `android:rotate`
   - `android:onRotate`

9. 状态栏的高度
   - 无法通过编程方式获取
   - 可以通过编程方式获取
   - 当前等于 20 像素
   - 在竖屏和横屏方向下总是不同

10. GUI 组件周围的边距
    - 必须在布局 xml 文件中设置——不能通过代码设置
    - 可以使用`View`类的`setMargins`方法设置
    - 可以使用`MarginLayoutParams`类的`setMargins`方法设置
    - 可以使用`Activity`类的`setMargins`方法设置

### 补全代码

11. 编写代码以获取一个`Configuration`引用。

12. 编写代码以获取屏幕的宽度（以像素为单位）。

13. 编写代码以获取屏幕的宽度（以 dp 为单位）。

14. 编写代码以将设备的当前方向输出到 Logcat。

15. 编写代码以测试设备是否具有超大屏幕，并将结果输出到 Logcat。

16. 编写代码以测试设备屏幕是否至少为大屏幕但非超大屏幕，并将结果输出到 Logcat。

17. 编写代码以设置视图：如果设备处于竖屏位置，则从`portrait.xml`加载布局；如果设备处于横屏位置，则从`landscape.xml`加载布局。假设你已经有一个`Configuration`引用。

18. 编写代码以获取操作栏的高度（以像素为单位）。

19. 编写代码以将名为`label`的`TextView`的宽度和高度输出到 Logcat。

```java
/* 假设 TextView label 已被实例化并已添加到视图中 */
// 在此处编写你的代码
```

20. 编写代码以设置按钮的边距：左边距 30 像素，右边距 50 像素。

```java
/* 假设 Button myButton 已被实例化并已添加到视图中 */
MarginLayoutParams params =
  ( MarginLayoutParams ) myButton.getLayoutParams( );
// 在此处编写你的代码
```

### 编写应用

21. 编写一个应用，使用两个布局 XML 文件在竖屏和横屏方向下都能正常工作：该应用要求用户输入加法运算的结果并检查答案。使用 0 到 20 之间的随机整数作为加法的操作数。包含一个`Model`。图形用户界面在两个方向上都应美观。

22. 编写一个应用，在竖屏和横屏方向下都能正常工作。该应用是尼姆游戏的一个变种。两名玩家轮流从一组物体中移除相同的物体。一名玩家每次可以移除一个、两个或三个物体。拿走最后一个物体的玩家输。你可以将当前物体数量存储在`TextView`中，并通过`EditText`获取用户输入。包含一个`Model`。随机生成起始物体数量，为 10 到 20 之间的整数。图形用户界面在两个方向上都应美观。

23. 编写一个应用，使用两个布局 XML 文件在竖屏和横屏方向下都能正常工作。该应用是一个简单的计算器：用户可以点击显示数字 1 到 9 的按钮，点击显示+、-、*的按钮，应用显示结果。包含一个`Model`。图形用户界面在两个方向上都应美观。为一种方向使用一种颜色主题，为另一种方向使用另一种颜色主题。

24. 编写一个应用，使用两个布局 XML 文件在竖屏和横屏方向下都能正常工作。该应用是一个小费计算器：用户可以输入餐厅账单金额、客人数量和小费百分比，应用显示总小费、总金额、每位客人的小费和每位客人的总金额。包含一个`Model`。图形用户界面在两个方向上都应美观。

25. 编写一个应用，在竖屏和横屏方向下都能正常工作。该应用是一个井字棋游戏。包含一个`Model`。图形用户界面在两个方向上都应美观。在一种方向下使用 X 和 O，在另一种方向下使用 A 和 Z。

26. 编写一个应用，在竖屏和横屏方向下都能正常工作。该应用显示一个初始位置的棋盘。包含一个`Model`。图形用户界面在两个方向上都应美观。在一种方向下使用黑色和白色，在另一种方向下使用另外两种颜色。在竖屏位置，将棋盘置于屏幕顶部，使用屏幕的完整宽度。在横屏位置，将棋盘置于屏幕中央，使用屏幕的完整高度。使用字符表示不同的棋子（`K`表示王，`Q`表示后等）。

# 第七章：触摸与滑动

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

许多手机游戏使用屏幕触摸、点击或滑动作为与用户交互的方式。在大多数地图应用中，用户可以通过捏合或张开手指等手势来放大或缩小地图。所有这些都属于事件，并遵循一般事件处理的相同规则：

- 存在一个事件处理类，通常实现一个接口。
- 我们创建该类的一个对象，即监听器。
- 我们将该监听器注册到一个或多个图形用户界面（GUI）组件上。

在本章中，我们将学习如何检测和处理触摸、滑动和点击。我们还将构建一个简单的拼图应用，允许用户通过触摸并拖动拼图块到拼图中的另一个位置来移动它。图 7.1 展示了该拼图，它使用了五个顺序被打乱的`TextView`，需要将它们按正确顺序排列。

![](img/9781284093650_CH07_FIGF01.jpg)

图 7.1 在模拟器中运行的拼图应用（版本 2）

## 7.1 检测触摸事件

在开始制作拼图应用之前，我们先构建一个简单的练习应用，其中包含一个`TextView`。当用户触摸它时，我们会随着用户手指的移动而移动这个`TextView`。我们为此应用使用空活动模板。`View.OnTouchListener`接口是`View`类的一个`public static`内部接口，它提供了一个方法`onTouch`，当用户与屏幕交互时会被调用。当某个事件（例如一个事件）发生时被调用的方法称为回调方法。表 7.1 展示了该方法。

为了使用`View.OnTouchListener`接口处理触摸事件，我们需要：

- 定义一个实现`View.OnTouchListener`并重写`onTouch`方法的类。
- 创建该类的对象。
- 将该对象注册到一个或多个`View`上。

我们可以将该类定义为当前活动类的私有类：

```java
// MainActivity 类内部的私有类
private class TouchHandler implements View.OnTouchListener {
  // TouchHandler 类需要重写 onTouch
  public boolean onTouch( View v, MotionEvent event ) {
    // 在此处处理事件
  }
}
```

为了将`View.OnTouchListener`类型的对象注册到`View`上，我们使用`View`类的`setOnTouchListener`方法，如表 7.2 所示。

```java
// 在 MainActivity 内部，如果我们希望 View v 响应触摸事件
TouchHandler th = new TouchHandler( );
v.setOnTouchListener( th );
```

另一种定义实现`View.OnTouchListener`的新类的方法是让当前的`Activity`类实现`View.OnTouchListener`。这样，`this`就是一个`View.OnTouchListener`对象，我们可以将其注册到一个或多个`View`上。如果`Activity`类是`MainActivity`，我们可以这样写：

```java
// MainActivity 实现了 View.OnTouchListener
public class MainActivity extends Activity implements
             View.OnTouchListener {

// 如果我们希望 View v 响应触摸事件
v.setOnTouchListener( this );

// MainActivity 类需要重写 onTouch
public boolean onTouch( View v, MotionEvent event ) {
  // 在此处处理事件

}
```

| 方法 | 描述 |
| --- | --- |
| `boolean onTouch( View v, MotionEvent event )` | 当触摸事件发生时调用。`v`是事件发生的`View`（假设该监听器已注册在`v`上）。如果此方法返回`true`，则事件被消耗。如果返回`false`，则事件会传播到`View`堆栈中位于`v`下方的`View`。 |

表 7.1 `View.OnTouchListener`接口

| 方法 | 描述 |
| --- | --- |
| `void setOnTouchListener( View.OnTouchListener listener )` | 将监听器注册到此`View`上。当触摸事件发送到此`View`时，将调用监听器的`onTouch`方法。 |

表 7.2 `View`类的`setOnTouchListener`方法

`onTouch`方法的第一个参数是事件发生的`View`，假设监听器已注册在该`View`上。第二个参数是一个`MotionEvent`引用，包含事件的相关信息。当用户触摸屏幕、移动手指然后抬起时，实际上会依次发生一系列事件。`onTouch`方法会被多次调用，每次`event`参数的值都不同。这使我们能够测试`event`参数并相应地处理事件。`MotionEvent`参数`event`包含事件序列中当前事件的信息，甚至可以包含整个序列经过的时间、触摸屏幕的力度等信息。`getAction`方法（在表 7.3 中与其他`MotionEvent`类的方法一起列出）返回一个整数值，用于标识发生的动作类型。我们可以将该值与`MotionEvent`类的动作常量进行比较。因此，在`onTouch`内部，我们可以调用`event.getAction()`，将结果与`MotionEvent`类中对应我们感兴趣事件的常量进行比较，并相应地处理结果。一种好的做法是使用`switch`语句，如下所示（将`SOME_ACTION`和`SOME_OTHER_ACTION`替换为实际的常量，如`ACTION_DOWN`、`ACTION_UP`等）：

```java
public boolean onTouch( View v, MotionEvent event ) {
  int action = event.getAction( );
  switch( action ) {
  case MotionEvent.SOME_ACTION:
    // 发生了某个动作；处理该信息
    break;
  case MotionEvent.SOME_OTHER_ACTION:
    // 发生了另一个动作；处理该信息
    break;
   ...
 }
 ...
}
```

| 方法 | 描述 |
| --- | --- |
| `float getRawX( )` | 返回触摸点在屏幕上的 x 坐标。 |
| `float getRawY( )` | 返回触摸点在屏幕上的 y 坐标。 |
| `float getX( )` | 返回触摸点在其发生的`View`内的 x 坐标。 |
| `float getY( )` | 返回触摸点在其发生的`View`内的 y 坐标。 |
| `int getAction( )` | 返回触摸事件中发生的动作类型。 |

表 7.3 `MotionEvent`类的部分方法

| 常量 | 描述 |
| --- | --- |
| `ACTION_DOWN` | 用户触摸了屏幕。 |
| `ACTION_UP` | 用户停止触摸屏幕。 |
| `ACTION_MOVE` | 用户正在屏幕上移动手指。 |

表 7.4 `MotionEvent`类的部分常量，可与`getAction`方法的返回值进行比较

我们重点关注首次触摸（`ACTION_DOWN`常量）、手指拖动（`ACTION_MOVE`常量）和手指抬起（`ACTION_UP`常量）。在这个第一个示例中，我们只是向 Logcat 输出一些信息，说明正在处理什么动作、对应什么事件以及发生在哪个`View`上。示例 7.1 展示了`MainActivity`类。

我们在第 9-10 行声明`MainActivity`实现了`View.OnTouchListener`接口。在`onCreate`内部，我们在第 17 行使用默认的`content` id 获取活动的内容视图（该 id 默认标识它）。我们在第 18 行输出它，以便将其值与`onTouch`方法的`View`参数的值进行比较。在第 19 行，我们将`this`（一个`View.OnTouchListener`）注册到该内容`View`上。这样，每当用户通过触摸与屏幕交互时，`onTouch`方法就会执行，其`View`参数就是内容`View`。

![](img/ch07exa01.jpg)

示例 7.1 `MainActivity`类，跟踪触摸事件，Touches 应用，版本 0

在`onTouch`方法内部（第 22-36 行），我们首先在第 23 行获取执行的动作。我们使用`switch`结构将其值与`MotionEvent`类的`ACTION_DOWN`、`ACTION_MOVE`和`ACTION_UP`常量进行比较。对于每种情况，我们向 Logcat 输出关于`v`（`View`参数）和`event`（`MotionEvent`参数）的信息。

![](img/9781284093650_CH07_FIGF02.jpg)

图 7.2 来自示例 7.1 的 Logcat 输出

图 7.2 显示了当用户在屏幕上某处进行小幅度滑动时，示例 7.1 在 Logcat 中的输出。我们可以观察到以下几点：

- 该方法首先以`DOWN`动作被调用，然后多次以`MOVE`动作被调用，最后以`UP`动作被调用一次。
- `View`参数`v`始终相同，并且是活动的内容视图。



- ▸ 参数 `event` 包含诸如动作、x 和 y 坐标、时间等信息。我们可以看到，每次在 `MOVE` 动作上调用该方法时，x 和 y 坐标值都不同。它们共同构成一组离散的值，反映了滑动轨迹。请注意，我们并不会获得关于滑动的连续逐像素信息。

## 7.2 处理滑动事件：移动 `TextView`

在第一个示例中，我们在内容 `View` 上注册了触摸监听器。在第二个示例中，我们在屏幕上添加了一个 `TextView`，并在用户触摸它并在屏幕上移动手指时移动它。这次，我们在 `TextView` 上注册了监听器。这说明了 `getX` 和 `getY` 方法，与 `getRawX` 和 `getRawY` 方法之间的区别，如表 7.3 所示。`getX` 和 `getY` 方法返回相对于事件发生的 `View` 的 x 和 y 坐标，该 `View` 是作为第一个参数传递给 `onTouch` 的 `View` `v`。`getRawX` 和 `getRawY` 返回屏幕内的 x 和 y 坐标，包括屏幕装饰（如状态栏和操作栏）。如果我们使用 `getRawX` 和 `getRawY` 方法，并且希望获得相对于内容 `View` 的 x 和 y 坐标，可以在 `onTouch` 内部使用以下代码进行转换：

```java
int [] location = new int[2];
// view 代表活动的 content view
view.getLocationInWindow( location );
float relativeX = event.getRawX( ) - location[0];
float relativeY = event.getRawY( ) - location[1];
```

`View` 类的 `getLocationInWindow` 方法接受一个包含两个 `int` 的数组作为参数，并将其两个值设置为调用该方法的 `View` 在窗口内左上角的 x 和 y 坐标。然后，我们可以从 `getRawX` 和 `getRawY` 返回的值中减去这些值，以获得触摸事件在活动内容视图内的相对 x 和 y 坐标。

相比之下，如果监听器已注册在 `TextView` 上，并且首次触摸发生在 `TextView` 的左上角，那么，`onTouch` 方法的 `View` `v` 参数就是该 `TextView`，并且 `getX` 和 `getY` 方法返回 `0` 和 `0`（或接近该值），而与 `TextView` 在屏幕上的位置无关。

示例 7.2 展示了 `MainActivity` 类。我们通过代码构建 GUI，并在其中包含一个 `TextView`。我们希望根据用户触摸来移动该 `TextView`，因此需要使用绝对坐标。原本用于绝对坐标的 `AbsoluteLayout` 类已被弃用。我们改用 `RelativeLayout` 类。`RelativeLayout` 允许我们将组件相对于彼此定位，或使用绝对坐标定位。每个组件的尺寸和位置可以通过在将其添加到 `RelativeLayout` 时关联一个 `RelativeLayout.LayoutParams` 对象来定义和控制。`TextView` 实例变量 `tv` 在第 12 行声明，其 `RelativeLayout.LayoutParams` 参数 `params` 在第 13 行声明。通过将它们声明为实例变量，我们可以在 `onTouch` 方法内部访问它们。

![](img/ch07exa02.jpg) ![](img/ch07exa02a.jpg)

**示例 7.2** `MainActivity` 类，通过滑动移动 `TextView`，Touches 应用，版本 1

我们在 `buildGuiByCode` 方法（第 24–37 行）中通过代码构建 GUI，该方法在第 21 行被调用。在第 25 行，我们实例化 `tv`，并在第 26 行为其设置红色背景。在第 28 行，我们创建一个 `RelativeLayout`，并在第 34 行将其设置为内容视图。在第 29–31 行，我们定义 `params`，并在第 33 行使用它将 `tv` 添加到相对布局中。在 `onTouch` 方法内部，当我们修改 `params` 并使用 `params` 重置 `tv` 的布局参数时，我们会自动修改 `tv` 的位置。`RelativeLayout.LayoutParams` 是 `ViewGroup.MarginLayoutParams` 的子类，并继承了其与边距相关的字段，如表 7.5 所示。

我们在第 14–17 行添加了更多实例变量，以跟踪 `TextView` 的原始位置以及滑动开始时触摸的位置。我们在 `onTouch` 方法内部使用它们，在用户在屏幕上移动手指时重新计算 `TextView` 的左上角位置。在 `onTouch` 方法内部（第 39–55 行），当用户首次触摸屏幕时（第 43–46 行），我们初始化这四个变量，该触摸由 `DOWN` 动作捕获（第 42 行）。当用户移动手指（`MOVE` 动作，第 48 行）时，我们在第 49–50 行更新 `params` 的 `leftMargin` 和 `topMargin` 参数，并在第 51 行通过调用 `setLayoutParams` 方法（如表 7.6 所示）并传入更新后的 `params` 值来相应更新 `tv` 的位置。当用户将手指从屏幕上抬起时，无需执行任何操作，因此我们在代码中不考虑 `UP` 动作。

| 方法 | 描述 |
| --- | --- |
| `int bottomMargin` | 子视图的底部边距（像素） |
| `int leftMargin` | 子视图的左边距（像素） |
| `int rightMargin` | 子视图的右边距（像素） |
| `int topMargin` | 子视图的顶部边距（像素） |

**表 7.5** `ViewGroup.MarginLayoutParams` 类的 `public` 字段

| 方法 | 描述 |
| --- | --- |
| `void setLayoutParams( ViewGroup.LayoutParams params )` | 设置与此视图关联的布局参数 |

**表 7.6** `View` 类的 `setLayoutParams` 方法

请注意，在此示例中，我们在第 36 行将监听器注册在 `tv` 上，而不是内容视图上。因此，只有当触摸在 `tv` 内部开始时，才会触发对 `onTouch` 的调用；而当触摸在 `tv` 外部开始时，不会触发对 `onTouch` 的调用。

当我们运行这个练习应用时，如果触摸红色矩形并移动手指，红色矩形会随之移动。

## 7.3 模型

现在我们已经了解了触摸事件的工作原理以及如何移动 `TextView`，可以开始构建我们的拼图应用了。如图 7.1 所示，它向用户展示多个需要重新排序的 `TextView`。第一步是设计我们的模型，即 `Puzzle` 类，它包含以下内容：

- ▸ 一个字符串数组 `parts`，以正确顺序存储拼图。
- ▸ 一个方法，返回一个以随机错误顺序存储拼图的字符串数组。
- ▸ 一个方法，检查一个字符串数组是否按正确顺序排列。
- ▸ 一个方法，返回拼图中的碎片数量（即 `parts` 中的元素数量）。

示例 7.3 展示了 `Puzzle` 类。为简单起见，我们在默认构造函数中硬编码了 `parts` 数组的内容（第 10–17 行）。我们可以设想一个更复杂的模型，其构造函数从文件或数据库中读取拼图数据。在这种情况下，在读取数据之前，我们无法知道拼图中的碎片数量。因此，我们在第 47–49 行提供了一个获取拼图碎片数量的访问器 `getNumberOfParts`。这样，无论控制器何时需要知道拼图中有多少碎片，它都可以调用该方法，而不是使用硬编码的常量 `NUMBER_PARTS`。我们还可以在文件或数据库中存储多个拼图，并随机读取一个。在此示例中，我们可以在模型内部更改拼图的碎片数量，而应用仍然可以正常工作。例如，我们可以删除第 15 行和第 16 行，并将 `NUMBER_PARTS` 的值改为 3，应用仍然可以正常运行。

`solved` 方法（第 19–29 行）在其参数数组与 `parts` 内容相同时返回 `true`，否则返回 `false`。`scramble` 方法（第 31–45 行）返回一个 `Strings` 数组，包含拼图的所有元素但顺序不同。为此，我们首先在第 32 行创建一个新数组 `scrambled`，并在第 33–34 行用 `parts` 的元素初始化它。在第 36–43 行，我们使用 `while` 循环就地打乱 `scrambled` 的元素，直到 `scrambled` 的元素顺序与 `parts` 的元素顺序不同。为了测试这一点，我们使用了 `solved` 方法（第 36 行）。

![](img/ch07exa03.jpg)

**示例 7.3** `Puzzle` 类，Puzzle 应用，版本 0

第 37–42 行的 `for` 循环从左到右就地打乱 `scrambled` 的元素，从索引 `0` 开始。在循环的每次迭代中，索引 `0` 到 `i – 1` 之间的元素已经被打乱。当前迭代将索引 `i` 处的元素与 `i` 到 `scrambled.length – 1` 之间的随机索引处的元素交换。在第 38 行，我们生成一个介于 `i` 和 `scrambled.length – 1`（包含）之间的随机索引。然后，我们将该索引处的元素与索引 `i` 处的元素交换（第 39–41 行）。

## 7.4 视图：设置 GUI，Puzzle 应用，版本 0

现在我们了解了触摸事件并有了模型，就可以开始构建一个功能性的拼图应用了。在本节中，我们构建应用的视图部分。为简单起见，我们只允许应用以竖屏方向显示。在 `AndroidManifest.xml` 文件中，我们指定如下：

```xml
<activity
android:screenOrientation=”portrait”
```

在 `styles.xml` 文件中，我们将 `TextViews` 的字体大小设置为 `32`，如下所示：

```xml
<item name=”android:textSize”>32sp</item>
```

拼图的每一块都显示在一个 `TextView` 中。虽然 `Puzzle` 的默认构造函数指定了一个包含五块的拼图，但我们很容易设想另一个构造函数，让用户指定块数，然后从文件或数据库中检索 `Strings`。因此，我们通过代码而不是 XML 文件来定义 `View`，以便它可以容纳可变数量的 `TextViews`。此外，我们将 `View` 放在一个单独的类中，与代表控制器的 `MainActivity` 类分开。

示例 7.4 展示了 `PuzzleView` 类。我们没有扩展 `View` 并在内部用 `RelativeLayout` 管理 `View`，而是直接扩展 `RelativeLayout`。由于 `RelativeLayout` 继承自 `View`，它本身就是一个 `View`，可以分配给 `Activity` 作为其 `View`。我们使用 `RelativeLayout` 类来组织 `TextViews`，因为它可以使用绝对坐标管理其子 `Views`。

我们编写了一个接受四个参数的构造函数，如下所示：

- ▸ `activity`，一个 `Activity` 引用——我们将从 `Activity` 类实例化一个 `PuzzleView`。
- ▸ `width`，一个 `int`，表示屏幕的宽度。
- ▸ `height`，一个 `int`，表示屏幕的高度。
- ▸ `numberOfPieces`，一个 `int`，表示拼图中的块数。

我们通过 `buildGuiByCode` 方法（第 23–41 行）用代码构建整个 GUI，该方法在 `PuzzleView` 构造函数的第 20 行被调用，并将所有构造函数的参数传递给 `buildGuiByCode`。每个组件的尺寸和位置可以通过在将其添加到 `RelativeLayout` 时关联一个 `RelativeLayout.LayoutParams` 对象来定义和控制。我们声明了以下实例变量：

![](img/ch07exa04.jpg)

**示例 7.4** `PuzzleView` 类，Puzzle 应用，版本 0

- ▸ `tvs`，一个 `TextViews` 数组（第 11 行）。每个拼图块对应一个 `TextView`。
- ▸ `params`，一个 `RelativeLayout.LayoutParams` 数组（第 12 行）。
- ▸ `colors`，一个表示颜色的整数值数组（第 13 行）。我们随机生成它们以给 `TextViews` 着色。
- ▸ `labelHeight`，每个 `TextView` 的高度（第 15 行）。

以上三个数组是并行数组。我们使用 `params` 数组来定位和调整 `tvs` 中 `TextViews` 的大小，并使用 `colors` 数组为它们着色。它们在第 25–27 行被实例化。在第 30–40 行，我们遍历数组 `tvs` 中的元素。每个 `TextView` 使用上述三个数组中对应的值进行着色、定位和调整大小。在第 33–34 行，我们生成三个介于 `0` 和 `255`（包含）之间的随机整数，并将它们传递给 `Color` 类的 `rgb` 静态方法，以便为当前 `TextView` 生成随机颜色。注意，我们使用的是 `android.graphics` 包中的 `Color` 类（在第 8 行导入），而不是传统的 `java.awt` 包中的 `Color` 类。

我们希望所有 `TextViews` 具有相同的高度，并将其存储在 `labelHeight` 中。在第 29 行，我们将 `labelHeight` 赋值为 `height` 参数（表示屏幕高度）除以 `numberOfPieces`。在第 36 行，我们使用 `width` 和 `labelHeight` 实例化 `params` 的每个元素。在第 37–38 行，我们设置 `params` 每个元素左上角的坐标。在第 39 行，每个 `TextView` 通过 `ViewGroup` 类（`RelativeLayout` 的直接超类）的 `addView` 方法添加到这个 `PuzzleView` 中，该方法接受一个 `ViewGroup.LayoutParams`（`RelativeLayout.LayoutParams` 的超类）对象作为第二个参数。

`fillGui` 方法（第 43–46 行）提供了用表示拼图打乱后块的 `Strings` 数组填充 `TextViews` 的代码。

示例 7.5 展示了 `MainActivity` 类。它包含两个实例变量：`puzzleView`，一个代表视图的 `PuzzleView` 引用（第 13 行），以及 `puzzle`，一个代表模型的 `Puzzle` 引用（第 14 行）。

`onCreate` 方法（第 16–49 行）在第 18 行实例化 `puzzle`，在第 43–44 行实例化 `puzzleView`。它在第 48 行将此 `Activity` 的内容 `View` 设置为 `puzzleView`。我们在第 20–23 行获取屏幕的高度和宽度。虽然屏幕的宽度也是拼图的宽度，但屏幕的高度包括状态栏和操作栏的高度，这些不应包含在拼图中。在撰写本文时，根据谷歌的设计指南，状态栏的高度为 24 dp，操作栏的高度为 56 dp。因此，我们在第 11–12 行声明了两个常量，定义了状态栏和操作栏高度的默认值。

我们首先在第 29 行和第 36 行将这些默认值乘以像素密度赋值给 `actionBarHeight` 和 `statusBarHeight` 变量，然后再尝试以编程方式获取它们。我们在第 25–27 行通过首先获取一个 `Resources` 引用，然后获取当前设备的 `DisplayMetrics` 引用，再访问其 `density` 字段来获取当前设备的像素密度。`DisplayMetrics` 类包含有关显示器的信息，包括其大小、密度和字体缩放。无法保证操作栏的高度将来不会改变。因此，最好以编程方式获取它。在第 30–34 行，我们尝试获取操作栏的高度，如果成功则将其赋值给 `actionBarHeight`。在第 37–40 行，我们尝试获取状态栏的高度，如果成功则将其赋值给 `statusBarHeight`。附录 A 对此进行了详细解释。

![](img/ch07exa05.jpg)

**示例 7.5** `MainActivity` 类，Puzzle 应用，版本 0

在第 42 行，我们从屏幕高度中减去状态栏和操作栏的高度，以计算拼图的高度。

我们在第 45 行调用 `Puzzle` 的 `scramble` 方法，为谜题生成一个打乱后的 `Strings` 数组，然后将其传递给第 46 行 `PuzzleView` 的 `fillGui` 方法。从模型-视图-控制器的角度来看，控制器在第 45 行要求模型提供一个打乱的 `Strings` 数组，并在第 46 行用该数组更新视图。

此时，还没有事件处理，因此用户无法移动谜题的任何碎片，但应用可以运行并显示未解开的谜题，如图 7.1 所示。

## 7.5 移动碎片，谜题应用，版本 1

现在我们开始构建应用的控制器部分，以赋予应用功能。在版本 1 中，我们允许用户移动谜题的各种碎片（即 `TextViews`）。此时，我们不关心碎片是否摆放正确，也不关心谜题是否已解开。

![](img/9781284093650_CH07_FIGF03.jpg)

**图 7.3** 红色 `View` 在堆叠顺序中高于蓝色 `View`，它部分遮挡了蓝色 `View`

每当用户移动谜题的一个碎片时，我们会将该碎片置于其他碎片之上，以便用户始终能看到它。`Views` 按照堆叠顺序排列在栈中。第一个添加到 `ViewGroup` 的 `View` 位于栈底，最后一个添加的 `View` 位于栈顶。图 7.3 展示了堆叠顺序的概念。红色 `View` 在蓝色 `View` 之后添加，因此在堆叠顺序中更高，并部分遮挡了蓝色 `View`。表 7.7 展示了 `View` 类的 `bringToFront` 方法，我们可以用它来将 `View` 带到栈顶，使其不被同级 `Views` 遮挡。要将名为 `view` 的 `View` 强制置于栈顶，我们调用 `bringToFront` 方法，如下所示：

```java
view.bringToFront( );
```

为了实现上述功能，`MainActivity` 类实现了 `View.OnTouchListener` 接口，并重写了 `onTouch` 方法。此时，`onTouch` 方法的伪代码如下：



如果动作是 `DOWN`
- 存储被触摸的谜题碎片的 `y` 位置
- 存储触摸点的 `y` 位置
- 将该谜题碎片置于堆叠顺序顶部

如果动作是 `MOVE`
- 随着用户手指移动，移动该谜题碎片

| 方法 | 描述 |
| --- | --- |
| `void bringToFront()` | 将此`View`带到栈顶，使其位于所有同级视图之上。 |

表 7.7 `View`类的`bringToFront`方法

上述所有操作都涉及管理`PuzzleView`类中的`TextViews`。因此，我们在`PuzzleView`类中提供执行这些操作的方法，并从`MainActivity`类中调用这些方法。示例 7.6 展示了`MainActivity`类。它实现了`View.OnTouchListener`（第 12–13 行），并在第 54–70 行重写了`onTouch`方法。在第 50 行，`onCreate`方法内部，我们调用`PuzzleView`类的`enableListener`方法，传入`puzzleView`。该方法将`this`监听器（即`MainActivity`）注册到所有`TextViews`上。

在`onTouch`内部，我们首先在第 55 行调用`indexOfTextView`来获取作为触摸事件目标的`TextView`的索引，并在第 56 行获取触摸事件中的动作类型。此时，我们只关心`DOWN`和`MOVE`动作，还不关心`UP`动作。如果是`DOWN`动作（第 58 行），表示用户正在拿起一个谜题碎片并准备移动它。我们调用`updateStartPositions`，传入`puzzleView`（第 59–60 行），以更新被触摸的`TextView`的`y`位置和触摸点的`y`位置（如果动作是`MOVE`，我们需要这两个`y`值来计算`TextView`的新位置）。我们在第 61–62 行将被触摸的`TextView`带到前面。

![](img/ch07exa06.jpg) ![](img/ch07exa06a.jpg)

示例 7.6 `MainActivity`类，谜题应用，版本 1

当用户移动手指时（移动触摸动作，第 64 行），我们调用`moveTextViewVertically`，传入`puzzleView`（第 65–66 行），以便沿着垂直轴跟随用户手指移动被触摸的`TextView`。

示例 7.7 展示了更新后的`PuzzleView`类。它包含了`MainActivity`类中`PuzzleView`实例变量调用的所有方法：`indexOfTextView`、`tvPosition`、`enableListener`、`updateStartPositions`和`moveTextViewVertically`。

`enableListener`方法（第 73–76 行）期望一个`View.OnTouchListener`参数，并将其注册到所有`TextViews`上。当从`MainActivity`调用它时，我们传入`this`，由于`MainActivity` `implements View.OnTouchListener`，因此`this`是一个`View.OnTouchListener`引用。

![](img/ch07exa07.jpg) ![](img/ch07exa07a.jpg)

示例 7.7 `PuzzleView`类，谜题应用，版本 1

![](img/9781284093650_CH07_FIGF04.jpg)

图 7.4 谜题应用，版本 1，用户移动了几个碎片后的界面

为了帮助我们管理`TextViews`的拖动，我们添加了以下实例变量：

- ▸ 一个整型实例变量`startY`（第 17 行），存储正在移动的谜题碎片顶部的`y`坐标。
- ▸ 一个整型实例变量`startTouchY`（第 18 行），存储初始触摸点的`y`坐标。

`indexOfTextView`方法编码在第 51–60 行，返回其`View`参数`tv`在数组`tvs`中的索引。我们期望`tv`是一个`TextView`，但在第 53 行进行了检查。我们遍历`tvs`的元素，将索引`i`处的元素与`tv`进行比较（第 56 行），如果相等则返回`i`（第 57 行）。如果`tv`不是`TextView`或未找到，则返回–1（第 54 行和第 59 行）。

`updateStartPositions`方法编码在第 62–65 行，在触摸动作`DOWN`时被调用。我们在第 63–64 行更新实例变量`startY`和`startTouchY`的值；`startY`存储该碎片对应`TextView`的原始`y`坐标，`startTouchY`存储触摸点在`TextView`内的`y`坐标。在`MOVE`触摸动作时，我们需要这两个值来更新`TextView`的`y`坐标。

`moveTextViewVertically`方法编码在第 67–71 行，根据其第二个参数`y`（表示触摸点的`y`坐标）更新索引为`index`（第一个参数）的`TextView`的布局参数。通过更改`TextView`的布局参数，它会自动移动到这些布局参数定义的新位置。

图 7.4 展示了用户移动了几个碎片后的谜题界面。

## 7.6 解开谜题，谜题应用，版本 2

现在我们继续构建应用的控制器部分，以赋予应用功能。当用户移动一个谜题碎片（即`TextView`）并释放它时，我们会将其位置与它下方的碎片交换。我们判断一个碎片是否位于另一个碎片之上，条件是至少一半的碎片覆盖在另一个碎片上，如图 7.5 所示。绿色碎片超过一半覆盖在蓝色碎片上。如果用户释放它，绿色碎片将占据蓝色碎片的位置，而蓝色碎片将被放置在触摸事件开始时绿色碎片所在的位置。每次移动后，我们检查用户是否已解开谜题。如果已解开，我们禁用触摸事件。

![](img/9781284093650_CH07_FIGF05.jpg)

图 7.5 绿色碎片比红色碎片更靠近蓝色碎片

除了处理`DOWN`和`MOVE`动作外，我们还需要处理`UP`动作，以便交换两个谜题碎片。在`MainActivity`内部，`onTouch`方法的伪代码现在变为：

```
如果动作为 DOWN
  存储所触摸拼图块的 y 位置
  存储触摸点的 y 位置
  存储“空”拼图槽的位置
  将拼图块置于堆叠顺序的顶部
如果动作为 MOVE
  随着用户手指移动而移动拼图块
如果动作为 UP
  将当前拼图块与其下方的拼图块交换
  检查拼图是否完成；如果完成，则禁用监听器
```

为了实现新增功能，我们在`PuzzleView`类中提供了额外的方法，并从`MainActivity`类中调用这些方法。示例 7.8 展示了`MainActivity`类中更新后的`onTouch`方法。

![](img/ch07exa08.jpg)

**示例 7.8** `MainActivity`类中更新后的`onTouch`方法，拼图应用，版本 2

当用户抬起手指（向上触摸动作，第 68 行）时，我们将触摸的`TextView`与当前触摸点下方的`TextView`交换：首先在第 70 行调用`tvPosition`（传入`puzzleView`）以获取触摸`TextView`的新位置索引，然后在第 71 行调用`placeTextViewAtPosition`（传入`puzzleView`）以交换这两个`TextView`。最后，在第 73 行检查用户是否完成了拼图。从模型-视图-控制器的角度来看，控制器从视图获取拼图状态，并请求模型检查这是否是拼图的正确顺序。如果是，控制器通过在第 74 行调用`disableListener`来请求视图禁用触摸事件监听，从而阻止用户移动`TextView`。

示例 7.9 展示了更新后的`PuzzleView`类。它包含了`MainActivity`类中`PuzzleView`实例变量调用的所有以下额外方法：`tvPosition`、`placeTextViewAtPosition`、`disableListener`和`currentSolution`。我们还根据需要更新了`buildGuiByCode`、`fillGui`和`updateStartPositions`方法。

![](img/ch07exa09.jpg) ![](img/ch07exa09a.jpg) ![](img/ch07exa09b.jpg)

**示例 7.9** `PuzzleView`类，拼图应用，版本 2

`disableListener`方法（第 84–87 行）将所有`TextView`的监听器设置为`null`，从而有效禁用触摸监听。

为了帮助我们管理`TextView`的交换，我们添加了以下实例变量：

- ▸ 一个整型实例变量`emptyPosition`（第 19 行），存储“空位置”的`y`位置，即用户当前移动的`TextView`在移动前所在的位置。
- ▸ 一个整型数组实例变量`positions`（第 20 行），存储`tvs`中所有元素的`y`位置。

当用户拿起或释放拼图块时，我们需要评估其在屏幕上的位置。图 7.6 和 7.7 展示了一个可能的起始拼图状态，以及用户交换底部两个拼图块后的第二个拼图状态。图 7.7 展示了`TextView`的位置（右列列出）与其在数组`tvs`中的索引（左列列出）之间的差异：`tvs[4]`位于位置`3`（屏幕底部上方一个位置），`tvs[3]`位于位置`4`（屏幕底部）。因此，`positions[3]`的值为 4（位于位置 3 的`TextView`的索引），`positions[4]`的值为 3（位于位置 4 的`TextView`的索引）。其他`TextView`尚未移动。

`tvPosition`方法（第 89–93 行）返回`tvs`数组中索引为`tvIndex`（方法的参数）的元素的位置（本例中为 0、1、2、3 或 4）。表达式`params[tvIndex].topMargin`返回`TextView`顶部的`y`坐标。我们加上半个`TextView`的高度，然后除以一个`TextView`的高度，以计算其在`PuzzleView`中的位置。

在`updateStartPositions`方法（第 67–71 行）内部，我们在第 70 行更新`emptyPosition`的值。`emptyPosition`实例变量存储被触摸的`TextView`在`PuzzleView`中的位置。我们通过调用`tvPosition`方法并传入该`TextView`的数组索引（第 70 行）来获取它。

![](img/9781284093650_CH07_FIGF06.jpg)

**图 7.6** 拼图的一种可能起始状态

![](img/9781284093650_CH07_FIGF07.jpg)

**图 7.7** 交换 I LOVE 和 JAVA 之后

`placeTextViewAtPosition`方法（第 95–109 行）在用户释放拼图块时被调用。它将拼图块与其下方的块交换。其第一个参数`tvIndex`是用户释放的`TextView`的索引。第二个参数`toPosition`是用户释放并结束触摸事件后该`TextView`将处于的位置。该方法执行三项操作：

- ▸ 将索引为`tvIndex`的`TextView`（TextView A）放置到由`toPosition`标识的新位置。它替换了该位置上的`TextView`（TextView B）。
- ▸ 将 TextView B 放置到 TextView A 的旧位置`emptyPosition`。
- ▸ 更新`positions`数组。

图 7.8 展示了当用户拿起 I LOVE 拼图块并将其移动到 PROGRAMMING 拼图块所在位置时，`TextView`和这些变量的各种状态。在此阶段，用户正在将索引为`4`（`tvIndex`的值）且位置为`3`（`emptyPosition`的值）的`TextView`移动到位置`0`（`toPosition`的值），该位置上有索引为`1`（`positions[toPosition]`的值）的`TextView`。

`tvs`和`params`数组相互对应。在第 98 行，我们将索引为`tvIndex`的`params`数组元素的顶部边距设置为该`tvs`数组元素要移动到的`y`坐标。在第 99 行，我们根据对应的`params`数组元素的值强制重新布局索引为`tvIndex`的`TextView`数组元素，从而将`TextView`放置到其新槽位。在第 101–104 行，我们对原来位于`toPosition`位置的`TextView`元素执行相同操作。它正在移动到`emptyPosition`位置。在第 106–108 行，我们更新`positions`数组以反映这两个`TextView`已被移动。

`positions`数组在第 30 行于`buildGuiByCode`方法中实例化，并在第 52 行于`fillGui`方法中初始化。

![](img/9781284093650_CH07_FIGF08.jpg)

**图 7.8** 将 I LOVE 移动到 PROGRAMMING 位置

![](img/9781284093650_CH07_FIGF09.jpg)

**图 7.9** 拼图应用版本 2，用户完成拼图后

`currentSolution`方法（第 111–118 行）构造并返回一个`String`数组，该数组反映了拼图中`TextView`的当前位置。`positions[i]`的值是位于屏幕位置`i`的`TextView`的索引，如图 7.6 和 7.7 所示。我们使用表达式`tvs[positions[i]].getText()`访问`PuzzleView`中位置`i`处的`TextView`内的文本。由于`getText`方法返回`CharSequence`，我们调用`toString`将返回值转换为`String`。

图 7.9 展示了完成后的拼图。

## 7.7 手势和点击检测与处理

有时我们需要检测确认的单次点击或双击。当系统确认只有一次点击（即未检测到第一次点击后的后续点击）时，该次点击即为确认的单次点击。或者，我们需要检测滑动的速度，以将其赋值给屏幕上物体的速度。`GestureDetector`类及其`static`内部接口`GestureDetector.OnGestureListener`和`GestureDetector.OnDoubleTapListener`提供了处理手势和点击的工具与功能。

- ▸ `GestureDetector.OnGestureListener`接口通过其六个回调方法（列于表 7.8）通知我们手势事件。
- ▸ `GestureDetector.OnDoubleTapListener`接口通过其三个回调方法（列于表 7.9）通知我们双击或确认的单次点击事件。

表 7.10 展示了`GestureDetector`类的一些方法，包括构造函数、`setOnDoubleTapListener`和`onTouchEvent`方法。

| 方法 | 描述 |
| --- | --- |
| `boolean onDown(MotionEvent e)` | 当触摸发生时，在`DOWN`动作时调用。 |
| `boolean onFling(MotionEvent e1, MotionEvent e2, float velocityX, float velocityY)` | 当滑动发生时调用。速度以每秒像素数在两个方向上测量。 |
| `void onLongPress(MotionEvent me)` | 当长按时调用。 |
| `boolean onScroll(MotionEvent e1, MotionEvent e2, float distanceX, float distanceY)` | 当滚动发生时调用。距离是在本次`onScroll`方法调用与上一次调用之间测量的。 |
| `void onShowPress(MotionEvent e)` | 当用户触摸屏幕且未移动或抬起手指时调用。 |
| `boolean onSingleTapUp(MotionEvent e)` | 当触摸发生时，在`UP`动作时调用。 |

表 7.8 `GestureDetector.OnGestureListener`接口的方法

| 方法 | 描述 |
| --- | --- |
| `boolean onDoubleTap(MotionEvent e)` | 当双击发生时，在`DOWN`动作时调用。 |
| `boolean onDoubleTapEvent(MotionEvent e)` | 当双击发生时，在`DOWN`、可能`MOVE`和`UP`动作时调用。 |
| `boolean onSingleTapConfirmed(MotionEvent e)` | 当确认的单次点击发生时（即该单次点击不是双击的第一次点击），在`DOWN`动作时调用。 |

表 7.9 `GestureDetector.OnDoubleTapListener`接口的方法

| 方法 | 描述 |
| --- | --- |
| `GestureDetector(Context context, GestureDetector.OnGestureListener gestureListener)` | 为指定上下文创建一个`GestureDetector`对象，并使用`gestureListener`作为手势事件的监听器。必须从用户界面线程使用此构造函数。 |



| `void setOnDoubleTapListener(GestureDetector.OnDoubleTapListener doubleTapListener)` | 将 `doubleTapListener` 设置为双击及相关手势的监听器。 |
| `boolean onTouchEvent(MotionEvent e)` | 当触摸事件发生时调用；触发对 `GestureDetector.OnGestureListener` 接口相应回调方法的调用。 |

表 7.10 `GestureDetector` 类的部分方法

为了使用 `GestureDetector` 类以及 `GestureDetector.OnDoubleTapListener` 和 `GestureDetector.OnGestureListener` 接口处理触摸事件，我们需要：

* 声明一个 `GestureDetector` 实例变量。
* 定义一个实现 `GestureDetector.OnGestureListener` 和 `GestureDetector.OnDoubleTapListener` 接口并重写其方法的处理类。
* 创建该类的处理对象。
* 实例化 `GestureDetector` 实例变量，并将处理对象作为构造函数的第二个参数传入。
* 将处理对象设置为处理点击事件的监听器（如有必要）。
* 在 `Activity` 类的 `onTouchEvent` 方法内部，使用 `GestureDetector` 实例变量调用 `GestureDetector` 类的 `onTouchEvent` 方法。这将触发触摸事件的分发：根据触摸事件，处理类的相应方法将被自动调用。

我们可以将处理类定义为当前活动类的 `private` 内部类。以下代码序列将实现上述步骤：

```java
// 在 Activity 类内部的 GestureDetector 实例变量
private GestureDetector detector;

// 在 Activity 类的 onCreate 方法内部
GestureAndTapHandler gth = new GestureAndTapHandler();
detector = new GestureDetector(this, gth);
detector.setOnDoubleTapListener(gth);

// 在 Activity 类的 onTouchEvent 方法内部
// event 是 onTouchEvent 方法的 MotionEvent 参数
detector.onTouchEvent(event);

// 在 Activity 类内部的私有类
private class GestureAndTapHandler implements
              GestureDetector.OnGestureListener,
              GestureDetector.OnDoubleTapListener {
    // GestureAndTapHandler 类需要重写所有 9 个方法
}
```

与之前使用 `View.OnTouchListener` 接口类似，另一种方法是让当前 `Activity` 类直接实现 `GestureDetector.OnGestureListener` 和 `GestureDetector.OnDoubleTapListener`，而不是定义一个新类。这样，我们需要在 `Activity` 类内部重写这九个方法，并在上述代码中使用 `this` 代替 `gth`。

`GestureDetector` 类的 `onTouchEvent` 方法充当分发器，根据刚刚发生的事件性质，调用 `GestureDetector.OnGestureListener` 和 `GestureDetector.OnDoubleTapListener` 接口的相应方法。对于某些应用，我们可能只需要在 `onTouchEvent` 方法内部执行代码。对于其他应用，我们可能对捕获双击感兴趣，因此会将代码放在 `onDoubleTapEvent` 方法中。或者，我们可能对捕获滑动的速度感兴趣，因此会将代码放在 `onFling` 方法中。根据我们感兴趣捕获和处理的动作，将代码放在对应的方法中。注意，当我们重写 `onTouchEvent` 时，需要调用 `GestureDetector` 类的 `onTouchEvent` 方法，因为它负责分发事件。

示例 7.10 展示了一个练习应用的 `MainActivity` 类。它在第 10–11 行实现了 `GestureDetector.OnGestureListener` 和 `GestureDetector.OnDoubleTapListener` 接口。我们在第 13 行声明了一个 `GestureDetector` 实例变量 `detector`。在第 17 行实例化它，将 `this` 作为第一个和第二个参数传入。作为第一个参数，`this` 代表应用的上下文（一个 `Activity` 对象“是一个” `Context` 对象）。作为第二个参数，它代表一个 `GestureDetector.OnGestureListener`（`MainActivity` 继承自 `GestureDetector.OnGestureListener`，因此 `this` “是一个” `GestureDetector.OnGestureListener`）。因此，由于 `detector` 在第 23 行调用了它的 `onTouchEvent` 方法，手势事件将根据触摸事件触发对 `MainActivity` 类中实现的六个回调方法中某些方法的调用。在第 18 行，我们将 `this` 设置为 `detector` 注册的点击事件监听器。因此，由于 `detector` 在第 23 行调用了它的 `onTouchEvent` 方法，点击事件将根据触摸事件触发对从 `GestureDetector.OnDoubleTapListener` 继承并在 `MainActivity` 类中实现的三个回调方法中某些方法的调用。

![](img/ch07exa10.jpg) ![](img/ch07exa10a.jpg)

示例 7.10 `MainActivity` 类，Touches 应用，版本 2

`onTouchEvent` 方法编码在第 21–25 行。`detector` 在第 23 行调用自身的 `onTouchEvent` 方法，传入 `MotionEvent event`，从而建立起之前讨论的分发机制。两个监听器接口的所有九个重写方法都会向 Logcat 输出一条反馈语句。

![](img/9781284093650_CH07_FIGF10.jpg)

图 7.10 用户单次点击屏幕时可能的 Logcat 输出，Touches 应用，版本 2

图 7.10 展示了用户在模拟器上单次点击屏幕时，示例 7.10 在 Logcat 中的输出。它显示 `onTouchEvent` 方法依次触发了对 `onDown`、`onSingleTapUp` 和 `onSingleTapConfirmed` 的调用。当 `onSingleTapUp` 被调用时，我们尚不知道这是一个单击事件，因为双击事件也会触发对 `onSingleTapUp` 的调用。因此，如果我们只想基于单击事件执行某些代码，应将代码放在 `onSingleTapConfirmed` 方法中。

![](img/9781284093650_CH07_FIGF11.jpg)

图 7.11 用户双击屏幕时可能的 Logcat 输出，Touches 应用，版本 2

![](img/9781284093650_CH07_FIGF12.jpg)

图 7.12 用户滑动屏幕时可能的 Logcat 输出，Touches 应用，版本 2

图 7.11 展示了用户在模拟器上快速点击屏幕两次（即双击）时，示例 7.10 在 Logcat 中的输出。它显示 `onTouchEvent` 方法触发了对 `onDown`、`onSingleTapUp`、`onDoubleTap`、`onDoubleTapEvent` 的调用，以及再次调用 `onDown` 和 `onDoubleTapEvent`。我们可能会得到略有不同的输出，可能还会额外调用一次 `onTouchEvent` 和 `onDoubleTapEvent`。注意 `onSingleTapConfirmed` 方法没有被调用。如果我们想处理点击事件，可以将代码放在 `onSingleTapUp` 和 `onDoubleTap` 方法中。如果我们想处理双击事件，可以将代码放在 `onDoubleTapEvent` 方法中。注意该方法被调用了两次：一次在 DOWN 动作时，第二次在 UP 动作时。如果在 DOWN 和 UP 动作之间检测到（轻微的）MOVE 动作，它甚至可能被调用三次。

三次点击被解释为一次双击后跟一次单击。四次点击被解释为一次双击后跟另一次双击。

图 7.12 展示了用户滑动屏幕时，示例 7.10 在 Logcat 中的可能输出。`onScroll` 方法在滑动过程中的不同点被多次调用。`onFling` 方法被调用一次，且是最后一次。根据滑动方式的不同，或者如果我们使用模拟器和电脑鼠标，我们可能会得到略有不同的输出。

一旦我们决定了要在哪个方法中执行代码，就可以使用它的一个或多个参数来获取与当前动作相关的值。例如，如果我们想捕获滑动的起点和速度，可以将代码放在 `onFling` 方法中，并像示例 7.11 所示那样获取这些值。

当我们运行修改后的应用并滑动屏幕时，输出结果类似于图 7.13 所示。

![](img/ch07exa11.jpg)

示例 7.11 `MainActivity` 类中扩展的 `onFling` 方法，Touches 应用，版本 3

![](img/9781284093650_CH07_FIGF13.jpg)

图 7.13 用户滑动屏幕时的 Logcat 输出，Touches 应用，版本 3

## 7.8 检测双击，Puzzle 应用，版本 3

`GestureDetector.SimpleOnGestureListener` 是一个便捷类，它实现了 `GestureDetector.OnGestureListener` 和 `GestureDetector.OnDoubleTapListener` 接口，其中的方法均为空操作并返回 `false`。因此，如果我们只对这两个接口中九个方法中的一两个感兴趣，扩展该类比实现其中一个或两个接口更简单。在我们的 Puzzle 应用版本 3 中，我们想要处理双击事件，并在用户双击显示 MOBILE 的 `TextView` 时，将 MOBILE 改为 ANDROID。我们可以忽略其他八个方法，只需在 `onDoubleTapEvent` 方法中编写代码。

我们更新 `Puzzle` 类（我们的模型），并为其添加两个方法：一个返回要更改的单词，另一个返回替换单词。我们尽可能保持这一更改简单，以便更专注于应用的控制器和视图部分。示例 7.12 展示了这两个方法。

![](img/ch07exa12.jpg)

示例 7.12 `Puzzle` 类的 `wordToChange` 和 `replacementWord` 方法，Puzzle 应用，版本 3

为了使用 `GestureDetector.SimpleOnGestureListener` 类，我们可以执行以下步骤：

* 编写一个 `private` 类，扩展 `GestureDetector.SimpleOnGestureListener`，并在该类中重写我们感兴趣的方法。
* 声明并实例化该类的对象，即手势处理器。
* 声明一个 `GestureDetector` 实例变量。在实例化时，将手势处理器作为构造函数的第二个参数传入。
* 如果我们对处理点击事件感兴趣，则调用 `setDoubleTapListener`，传入手势检测器实例变量和手势处理器。
* 在 `Activity` 的子类中重写 `Activity` 类的 `onTouchEvent` 方法。在其中，使用手势检测器实例变量调用 `GestureDetector` 类的 `onTouchEvent` 方法。这将建立触摸事件到手势处理器类相应方法的分发机制。

注意，`MainActivity` 已经扩展了 `AppCompatActivity`，因此无法再扩展 `GestureDetector.SimpleOnGestureListener`。因此，与示例 7.10（其中 `MainActivity` 实现了两个监听器接口）不同，我们需要编写一个单独的类来扩展 `GestureDetector.SimpleOnGestureListener`。

示例 7.13 展示了 `MainActivity` 类的新增部分。`private` 类 `DoubleTapHandler`（编码在第 93–106 行）仅重写了 `onDoubleTapEvent` 方法，因为我们只对处理双击事件感兴趣。在其中，我们获取用户双击的 `TextView` 的索引，检查其标签是否为 MOBILE，如果是，则将其改为 ANDROID。我们首先在第 96 行获取双击在 `PuzzleView` 中的 y 坐标。然后调用 `PuzzleView` 的 `indexOfTextView` 方法（我们将其添加到 `PuzzleView` 类中）来获取双击发生的 `TextView` 的索引（第 99–100 行）。因为需要从双击的 y 坐标中减去状态栏和操作栏的高度，我们在第 19–20 行将 `statusBarHeight` 和 `actionBarHeight` 声明为实例变量。这样，我们就不必计算它们的值两次。

![](img/ch07exa13.jpg)

示例 7.13 `MainActivity` 类的补充内容，Puzzle 应用，版本 3

在第 101–102 行，我们通过调用 `getTextViewText` 方法（也添加到 `PuzzleView` 类中）获取该 `TextView` 中的文本，并测试它是否与 `Puzzle` 类中要更改的单词匹配。如果匹配，则调用 `setTextViewText` 方法（也添加到 `PuzzleView` 类中）将 `TextView` 的文本更改为从 `Puzzle` 类获取的新单词。从模型-视图-控制器的角度来看，控制器要求视图检索 `TextView` 的文本，并将其与从模型获取的要更改的单词进行比较。如果匹配，控制器向模型请求替换单词，并告诉视图将其放入 `TextView` 中（第 103 行）。

在第 57 行，我们声明并实例化了 `dth`，一个 `DoubleTapHandler` 对象。实例变量 `detector`（一个 `GestureDetector`）在第 21 行声明，并在第 58 行实例化。传递给构造函数的第二个参数是 `dth`。这意味着当手势事件发生时，将调用 `GestureDetector.OnGestureListener` 接口中与手势相关的方法，而 `DoubleTapHandler` 类通过 `GestureDetector.SimpleOnGestureListener` 类继承了该接口。然而，在本例中，我们并不关心处理简单的触摸、滑动或快速滑动。我们只关心处理双击。因此，我们在第 59 行调用 `setOnDoubleTapListener` 方法，以便在点击事件发生时调用从 `GestureDetector.OnDoubleTapListener` 接口继承的三个方法。属于 `android.view` 包的 `GestureDetector` 类在第 9 行被导入。

我们在第 88–91 行重写了 `onTouchEvent` 方法。在第 89 行，`detector` 调用了 `GestureDetector` 类的 `onTouchEvent`，该方法设置了将手势和点击事件分派给 `dth` 所属类（即 `DoubleTapHandler`）的方法。因此，当用户在屏幕上双击时，我们会在 `DoubleTapHandler` 类的 `onDoubleTapEvent` 方法内部执行代码。

示例 7.14 展示了添加到 `PuzzleView` 类中的三个方法。在 `indexOfTextView` 方法（第 120–124 行）中，我们将点击的 `y` 坐标除以 `TextView` 的高度，并在第 122 行将其赋值给 `position`。位于 `position` 处的 `TextView` 的索引是 `positions[position]`。我们在第 123 行返回该索引。

在 `getTextViewText` 方法（第 126–129 行）中，我们在第 128 行调用 `toString`，因为 `TextView` 的 `getText` 方法返回一个 `CharSequence`。

![](img/ch07exa14.jpg)

示例 7.14 添加到 `PuzzleView` 类中的三个方法，拼图应用，版本 3

如果我们运行应用，并在解谜后双击 MOBILE，它会变成 ANDROID。注意，如果我们双击 I LOVE、PROGRAMMING、USING 或 JAVA，则不会发生任何变化。`onTouch` 方法（属于 `MainActivity` 类，在示例 7.8 的第 54–78 行展示）返回 `true`。这意味着我们停止传播触摸事件。当我们运行应用时，如果在解谜前双击 MOBILE，则不会发生任何变化，因为 `onDoubleTapEvent` 方法不会执行。一旦谜题被解开，我们禁用对 `TextView` 的监听（在示例 7.8 的第 74 行）。`TextView` 上不再注册触摸监听器，因此触摸事件的目标现在是活动的内容 `View`，并且事件由 `onTouchEvent` 方法分派给 `onDoubleTapEvent` 方法。



如果我们修改`onTouch`方法，使其在示例 7.8 的第 77 行返回`false`，那么`TextView`上的双击事件将传播到内容`View`，即位于触摸目标`View`下方的`View`。在这种情况下，`onDoubleTapEvent`方法将会执行。如果我们双击 MOBILE，它会变成 ANDROID。更一般地，如果`onTouch`方法返回`false`，则触摸事件不仅发生在顶层`View`上，还会传播到该顶层`View`下方的`View`。

图 7.14 展示了用户解谜并双击 MOBILE 后拼图的状态。

![](img/9781284093650_CH07_FIGF14.jpg)

图 7.14 拼图应用，版本 3，用户解谜并双击 MOBILE 后

## 7.9 使应用与设备无关：拼图应用，版本 4

当我们发布应用时，我们不知道它将在什么设备上运行，特别是屏幕的宽度和高度尺寸。在版本 4 中，我们在示例 7.15 中使用了`DynamicFontSizing`类，以便字体大小对于应用运行的设备是最优的。给定一个`TextView`，`setFontSizeToFitInView`静态方法（第 11–32 行）设置`TextView`内的文本字体大小，使其最大化且文本适合一行——它返回该最大字体大小。附录 B 详细解释了`DynamicSizing`类。

![](img/ch07exa15.jpg)

示例 7.15 `DynamicFontSizing`类，拼图应用，版本 4

![](img/ch07exa16.jpg)

示例 7.16 `PuzzleView`类中更新后的`fillGui`方法，拼图应用，版本 4

示例 7.16 展示了更新后的`fillGui`方法，这是`PuzzleView`类中唯一的更改，此外还从`android.util`包中导入了`TypedValue`类。我们在`fillGui`方法中优化了`TextView`的字体大小，因为这是设置它们文本的地方。

我们希望所有`TextView`使用相同的字体大小。然而，每个`TextView`内的文本是不同的。因此，我们计算每个`TextView`调用`setFontSizeToFitInView`返回的最小字体大小。在第 51 行用`MAX_FONT_SIZE`初始化`minFontSize`后，我们在第 59–62 行根据需要更新它。一旦设置了`minFontSize`，我们再次遍历所有`TextView`，并在第 65–67 行用`minFontSize`重置它们的字体大小。此方法执行后，所有`TextView`具有相同的字体大小，并且是使文本内容适合一行的最大字体大小。

在计算每个`TextView`的字体大小之前，我们在第 56 行确保它们的宽度等于屏幕的宽度。我们在第 57 行为每个`TextView`添加一些内边距，以便文本周围有空间。在 Nexus 5 模拟器上运行时，字体大小最终为 46。

图 7.15 展示了在模拟器中运行的拼图应用版本 4。PROGRAMMING 几乎填满了整个`TextView`。

![](img/9781284093650_CH07_FIGF15.jpg)

图 7.15 在模拟器中运行的拼图应用，版本 4

## 章节总结

- 我们可以使用`View.OnTouchListener`接口来捕获和处理触摸事件。
- 要在 GUI 组件上注册`View.OnTouchListener`，我们可以使用`View`类的`setOnTouchListener`方法。
- 当触摸事件发生时，会调用`View.OnTouchListener`接口的`onTouch`回调方法。
- `onTouch`方法包含一个`View`参数，该参数是对发生触摸的`View`的引用。
- `onTouch`方法包含一个`MotionEvent`参数，其中包含当前触摸事件的信息，例如 x 和 y 坐标、事件类型等。
- 如果`onTouch`方法返回`true`，则触摸事件不会传播到当前`View`下方可能具有该触摸事件处理器的`View`。如果返回`false`，则会传播。
- `MotionEvent`类的`getAction`方法返回一个整数值，表示触摸事件中刚刚发生的动作类型。
- `MotionEvent`类包含一些常量来标识触摸事件动作，例如`ACTION_DOWN`、`ACTION_MOVE`或`ACTION_UP`。
- `View`组件使用堆叠顺序显示在`ViewGroup`内部。最先添加的`View`位于堆栈底部，而最后添加的`View`位于堆栈顶部。
- 我们可以使用`bringToFront`方法将`View`带到堆栈顶部，以确保该`View`不会被其他`View`隐藏。
- 我们可以使用`GestureDetector`类及其静态内部接口`GestureDetector.OnGestureListener`和`GestureDetector.OnDoubleTapListener`来捕获和处理手势及点击事件。
- 在活动类的`onTouchEvent`方法内部，期望一个`GestureDetector`对象调用其`onTouchEvent`方法，以将触摸事件分派给实现了`GestureDetector.OnGestureListener`和/或`GestureDetector.OnDoubleTapListener`接口的处理程序类的相应方法。
- `GestureDetector.SimpleOnGestureListener`是一个便捷类，它实现了`GestureDetector.OnGestureListener`和`GestureDetector.OnDoubleTapListener`接口，但方法体为空。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. 我们使用什么方法在组件上注册一个`View.OnTouchListener`？
   - `setOnTouchListener`
   - `addOnTouchListener`
   - `registerOnTouchListener`
   - `isOnTouchListener`

2. 我们使用`MotionEvent`类的哪个方法来获取刚刚发生的动作类型？
   - `action`
   - `getAction`
   - `getEvent`
   - `getTouch`

3. 我们使用什么方法将一个`View`带到堆叠顺序的顶部？
   - `bringToTop`
   - `gotToTop`
   - `bringToFront`
   - `bringChildToTop`

4. 哪个类可用于捕获手势和点击事件？
   - `Gesture`
   - `GestureDetector`
   - `TapDetector`
   - `GestureAndTapDetector`

5. `OnGestureListener`和`OnDoubleTapListener`是
   - `GestureDetector`的私有静态内部类
   - `GestureDetector`的私有静态内部接口
   - `GestureDetector`的公有静态内部接口
   - 独立于`GestureDetector`的类

6. 为了识别触摸事件动作，`MotionEvent`类具有
   - 一个特殊的构造函数
   - 私有实例变量
   - 私有方法
   - 可用于比较动作的常量

7. `GestureDetector`类的哪个方法充当分派器，将事件分派给`OnGestureListener`和`OnDoubleTapListener`的各种方法？
   - `onTouch`
   - `onTouchEvent`
   - `onMotionTouchEvent`
   - `onEvent`

8. `OnGestureListener`和`OnDoubleTapListener`分别有多少个方法？
   - 六个和六个
   - 三个和三个
   - 三个和六个
   - 六个和三个

9. 当继承`OnGestureListener`和`OnDoubleTapListener`时，如果我们只对一两个方法感兴趣，另一种选择是
   - 实现`SimpleOnGestureListener`接口
   - 扩展`SimpleOnGestureListener`类
   - 实现`SimpleOnGestureListener`类
   - 扩展`SimpleOnGestureListener`接口

10. 哪个方法不是`OnDoubleTapListener`的方法？
    - `onSingleTapConfirmed`
    - `onDoubleTapConfirmed`
    - `onDoubleTap`
    - `onDoubleTapEvent`

### 补全代码

11. 编写一个名为`MyActivity`的类的类头，该类继承自`Activity`并实现`View.OnTouchListener`。

12. 我们在`View.OnTouchListener`的`onTouch`方法内编码。如果是 DOWN 动作，将触摸的 x 坐标赋值给变量`x1`。如果是 UP 动作，将触摸的 y 坐标赋值给变量`y2`。

13. 编写代码将一个名为`view`的`View`放置在其所属堆栈的顶部。

14. 我们已经编写了一个名为`MyHandler`的类，它扩展了`View.OnTouchListener`。编写代码以使用该类的对象，以便我们可以监听名为`myView`的`View`内部发生的触摸事件。

15. 编写一个名为`MyActivity`的类的类头，该类继承自`Activity`，并实现`GestureDetector.OnGestureListener`和`GestureDetector.OnDoubleTapListener`。

16. 编写一个继承自`GestureDetector.SimpleOnGestureListener`的私有类。我们只想处理单击事件。每次单击时，我们用随机颜色为名为`myView`的`View`的背景着色。

17. 编写一个继承自`GestureDetector.SimpleOnGestureListener`的私有类。我们想要统计点击次数，并将其累加到一个`Activity`类的实例变量`total`中，该变量已经初始化。每次点击时，`total`增加 1。

以下内容适用于第 18 和 19 题：

- `MyActivity`类扩展了`Activity`并实现了`GestureDetector.OnGestureListener`和`GestureDetector.OnDoubleTapListener`。我们已经声明了一个`GestureDetector`类型的实例变量`d`，如下所示：

```java
private GestureDetector d;
```

18. 我们在`Activity`类的`onCreate`方法内编码。编写代码，使得当前的`Activity`将处理手势和点击事件。

```java
protected void onCreate( Bundle savedInstanceState ){
  super.onCreate( savedInstanceState );
  // 你的代码写在这里
}
```

19. 我们在`Activity`类的`onTouchEvent`方法内编码。编写代码，使得如果有手势事件，它会被分派到`GestureDetector.OnGestureListener`的相应方法。

```java
public boolean onTouchEvent( MotionEvent event ){
  // 你的代码写在这里
}
```

### 编写应用

20. 修改示例 7.13，使得`MainActivity`不实现`View.OnTouchListener`。相反，触摸事件处理程序是一个私有类。

21. 修改示例 7.10，使得`MainActivity`不实现`GestureDetector.OnGestureListener`和`GestureDetector.OnDoubleTapListener`。相反，它们是私有类。

22. 修改示例 7.13，使得当用户双击时，我们重新开始一个新的谜题。

23. 编写一个应用，当用户滑动屏幕时，在一个或多个`TextView`中显示沿每个轴滑动的距离。

24. 编写一个应用，包含两个`TextView`。其中一个有红色背景——当用户在其内部点击时，它变为蓝色；当用户在其内部双击时，它变回红色，以此类推。如果用户在`TextView`外部点击或双击，其颜色不变。另一个`TextView`显示累计的点击次数。

25. 编写一个应用，包含一个具有红色背景的`TextView`——当用户在其内部点击时，它变为不可见；当用户在屏幕任意位置双击时，它再次变为可见。

26. 编写一个应用，使用两种颜色显示棋盘——当用户点击时，颜色变为下一对颜色，以此类推。我们应该包含至少五对颜色，应用循环使用这些颜色。包含一个`Model`。

27. 编写一个应用，包含三个活动——每个活动有一个`TextView`，显示一些标识该活动的文本。对于每个活动，如果用户从右向左滑动屏幕，应用移动到下一个活动（从活动 1 到活动 2，或从活动 2 到活动 3）。如果用户从左向右滑动屏幕，应用返回到上一个活动（从活动 3 到活动 2，或从活动 2 到活动 1）。

28. 编写一个应用，在屏幕中央显示一个`TextView`。用户可以触摸它并将其抛向屏幕边缘（`TextView`应跟随抛掷动作）。如果`x`或`y`方向的速度超过某个阈值（由你确定），则`TextView`在抛掷结束时消失，并在屏幕上的某个随机位置重新出现，以此类推。

29. 编写一个实现拼图游戏的应用：在一个 3×3 的网格上，数字 1 到 8 随机放置在网格内的`TextView`中。通过触摸一个`TextView`，它会移动到相邻的空方格（如果它紧邻空方格）。当数字按顺序排列（第一行 1,2,3，第二行 4,5,6，最后一行 7,8）时，游戏结束，触摸事件被禁用。包含一个`Model`。

30. 编写一个实现以下代数游戏的应用：五个`TextView`显示两个 1 到 9 之间的随机整数、`+`运算符、`=`运算符以及加法结果。当用户双击`+`运算符时，显示结果。当用户双击`+`运算符以外的区域时，两个新的随机数字替换现有的数字。包含一个`Model`。

31. 编写一个使用两个`TextView`实现以下累加器的应用。其中一个显示 1 到 9 之间随机生成的数字，另一个显示当前总数，初始值为 0。当用户触摸第一个`TextView`并将其拖到另一个`TextView`上方然后释放时，该数字被加到总数中，第一个`TextView`返回其原始位置并显示一个新的 1 到 9 之间的随机数字。包含一个`Model`。

32. 编写一个模拟扑克游戏（德州扑克）中公共牌发牌的应用。前三张牌在双击时发出。最后两张牌应在单击时一张一张地发出。滑动操作隐藏牌，以便我们准备开始下一轮。牌由`TextView`表示。包含一个`Model`。

33. 编写一个模拟修改版二十一点游戏的应用。前两张牌在双击时发出。额外的牌仅在单击时（而非双击）一张一张地发出。牌由`TextView`表示。另一个`TextView`显示结果。如果总数超过 17，则应禁用点击，用户获胜。如果总数超过 21，用户失败。包含一个`Model`。

# 第八章：图形、动画、声音与游戏

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

Android 开发框架为我们提供了一组类，用于绘制形状和位图、为这些形状和位图添加动画效果以及播放声音。在本章中，我们将构建一个简单的游戏，用户从大炮向飞过屏幕的鸭子射击。我们将学习如何绘制基本形状（如直线、圆形或矩形）、从文件中绘制位图、播放声音，以及如何捕获和响应触摸事件。我们还将学习如何以指定频率刷新屏幕，以便在屏幕上对对象进行动画处理。

## 8.1 图形

`android.graphics`包包含用于绘制和着色的类。表 8.1 展示了其中一些选定的类。

通常，我们在自定义视图（即`View`类的用户定义子类）上进行绘制。绘制发生在继承自`View`类的`onDraw`方法中。为此，我们可以使用以下模板：

```java
public class CustomView extends View {
  ...
  public void onDraw( Canvas canvas ) {
     super.onDraw( canvas );
     // 根据需要，使用 Paint 对象定义绘制样式和颜色
     // 使用 canvas 调用 Canvas 类的一些绘制方法
  }
...
```

| 类 | 描述 |
| --- | --- |
| `Bitmap` | 封装位图。 |
| `BitmapFactory` | 工厂类，用于从各种来源创建`Bitmap`对象。 |
| `Camera` | 生成可应用于`Canvas`的 3D 变换。 |
| `Canvas` | 绘制形状和位图。 |
| `Color` | 定义用于定义颜色的常量和方法，颜色由整数表示。 |
| `Paint` | 定义绘制的样式和颜色。 |
| `Picture` | 记录绘制调用。 |
| `Point` | 由两个整数坐标定义的点。 |
| `Rect` | 由整数坐标定义的矩形。 |

表 8.1 `android.graphics`包中的选定类



| 方法 | 描述 |
| --- | --- |
| `void setARGB( int a, int r, int g, int b )` | 将此`Paint`对象的 alpha、红色、绿色和蓝色颜色分量设置为值`a`、`r`、`g`和`b`（均在 0 到 255 之间）。 |
| `void setColor( int color )` | 将此`Paint`对象的颜色设置为`color`（包括 alpha 分量）。 |
| `void setStrokeWidth( float width )` | 将此`Paint`对象的描边宽度设置为`width`。 |
| `void setTextSize( float textSize )` | 将此`Paint`对象的文本大小设置为`textSize`。 |
| `void setStyle( Paint.Style style )` | 将此`Paint`对象的样式设置为`style`。`Paint.Style`是一个枚举，其可能值为`STROKE`、`FILL`和`FILL_AND_STROKE`。默认值为`FILL`。 |
| `void setAntiAlias( boolean flag )` | 如果`flag`为 true，则将此`Paint`设置为在绘制形状时使用抗锯齿，默认值为 false。 |

表 8.2 `Paint`类的选定方法

为了指定绘制方式（即定义绘制样式和颜色），我们使用`Paint`类。表 8.2 展示了它的一些方法。

例如，要定义一个`Paint`对象并将其颜色设置为红色、描边宽度设置为`5`像素，我们可以使用以下代码序列：

```java
Paint paint = new Paint( );
paint.setColor( 0xFFFF0000 );
paint.setStrokeWidth( 5.0f );
```

为了进行绘制，我们使用`Canvas`类。它提供了绘制基本形状和先前生成的位图（例如，从包含图片的文件，如 jpeg）的工具。表 8.3 展示了它的一些方法。

假设我们已经声明、实例化并定义了一个名为`paint`的`Paint`对象，以下是在`View`类的`onDraw`方法中绘制一个圆的方法，使其以点`(50, 100)`为中心，半径为`25`。

```java
//   canvas 是 onDraw 方法的 Canvas 参数
canvas.drawCircle( 50, 100, 25, paint );
```

`Paint`的默认样式是绘制形状时填充形状。如果我们不希望形状被填充，可以将`Paint`对象的样式设置为`STROKE`（参见表 8.2），如下所示：

```java
//   paint 是一个 Paint 引用
paint.setStyle( Paint.Style.STROKE );
```

| 方法 | 描述 |
| --- | --- |
| `void drawLine( float startX, float startY, float endX, float endY, Paint paint )` | 使用`paint`中定义的样式和颜色在点(`startX`, `startY`)和(`endX`, `endY`)之间绘制一条直线。 |
| `void drawLines ( float [ ] points, Paint paint )` | 使用`paint`中定义的样式和颜色绘制由`points`定义的直线。每条直线由`points`中连续的四个值定义。 |
| `void drawOval( RectF rect, Paint paint )` | 使用`paint`中定义的样式和颜色在矩形`rect`内绘制一个椭圆。`RectF`与`Rect`类似，但使用浮点数而非整数。 |
| `void drawCircle( float centerX, float centerY, float radius, Paint paint )` | 使用`paint`中定义的样式和颜色绘制一个圆，圆心为点(`centerX`, `centerY`)，半径为`radius`。 |
| `void drawPicture( Picture picture, Rect dst )` | 绘制`picture`并将其拉伸以适合`dst`矩形。 |
| `void drawBitmap( Bitmap bitmap, Rect src, Rect dst, Paint paint )` | 使用`paint`将`bitmap`中的`src`矩形绘制到`dst`矩形内。如果`src`为 null，则绘制整个位图。位图将按`dst`的尺寸绘制。 |
| `void drawRect( Rect rect, Paint paint )` | 使用`paint`中定义的样式和颜色绘制矩形`rect`。 |
| `void drawText( String text, float x, float y, Paint paint )` | 使用`paint`中定义的样式（包括对齐方式）和颜色，从坐标(`x`, `y`)开始绘制`String`文本。 |

表 8.3 `Canvas`类的选定方法

我们还可以使用`Canvas`类从文件中绘制一些图形。如果我们有一个名为`duck.png`的文件，应将该文件放在项目的`drawable`目录中。一旦文件位于`drawable`目录中，它就是一个资源，我们可以使用`R.drawable.nameOfFile`来引用它。在这种情况下，我们可以使用`R.drawable.duck`来引用它。注意，我们不包含文件扩展名。

首先，我们为该文件实例化一个`Bitmap`对象。然后，我们使用`onDraw`方法的`canvas`参数绘制它。要创建一个`Bitmap`，我们可以使用`BitmapFactory`类的众多`static`方法之一。表 8.4 列出了其中一些方法。一旦我们有了`Bitmap`引用，就可以通过`Bitmap`类的各种方法获取或设置其某些特性。表 8.5 列出了其中一些方法。

假设我们在项目的`drawable`目录中有一个名为`duck.jpg`的文件，我们可以使用以下代码将其绘制到自定义`View`中，该`View`位于由以下代码序列定义的矩形内：

```java
//   duck.png 位于 drawable 目录中
Bitmap duck = BitmapFactory.decodeResource( getResources( ),
              R.drawable.duck );
Rect rect = new Rect( 20, 50, 20 + duck.getWidth( ),
            50 + duck.getHeight( ) );
//   canvas 是 onDraw 方法的 Canvas 参数
//   paint 是一个 Paint 对象
canvas.drawBitmap( duck, null, rect, paint );
```

请注意，前面使用的`Rect`构造函数的最后两个参数是矩形的右边缘和下边缘，而不是其宽度和高度。

| 方法 | 描述 |
| --- | --- |
| `static Bitmap decodeResource( Resources res, int id )` | 从包含在`Resources`对象`res`中的`id`资源创建并返回一个`Bitmap`。 |
| `static Bitmap decodeFile( String pathName )` | 从文件路径`pathName`创建并返回一个`Bitmap`。 |
| `static Bitmap decodeStream( InputStream is )` | 读取`is`并从中创建并返回一个`Bitmap`。 |

表 8.4 `BitmapFactory`类的部分方法

| 方法 | 描述 |
| --- | --- |
| `int getWidth( )` | 返回此`Bitmap`的宽度。 |
| `int getHeight( )` | 返回此`Bitmap`的高度。 |
| `int getPixel( int x, int y )` | 返回此`Bitmap`在`(x, y)`坐标处的颜色（以整数形式）；`x`和`y`必须大于或等于 0，且分别小于此`Bitmap`的宽度和高度。 |
| `void setPixel( int x, int y, int color )` | 将此`Bitmap`位于`(x, y)`坐标处的像素颜色设置为`color`。与`getPixel`方法相同的约束条件适用。 |

表 8.5 `Bitmap`类的部分方法

## 8.2 制作自定义视图、绘图、打鸭子应用，版本 0

我们为此应用使用空活动模板。在版本 0 中，我们在屏幕左下角显示大炮，在屏幕右上角显示一只鸭子。与许多游戏一样，为了保持示例简单，我们只允许游戏在水平方向进行。因此，我们在`AndroidManifest.xml`文件的`activity`元素中添加以下内容：

```xml
android:screenOrientation=”landscape”
```

要将 jpeg 或 png 文件导入项目，我们将其复制并粘贴到`drawable`目录中。我们的文件名是`duck.png`。

为了继承`View`类，我们必须提供一个覆盖`View`类构造函数的构造函数，并在其第一条语句中调用`super`构造函数。否则，我们的代码将无法编译。请注意，`View`类不提供默认构造函数。表 8.6 显示了`View`类的一些构造函数和方法。

| 构造函数 | 描述 |
| --- | --- |
| `View( Context context )` | 在通过代码创建`View`时使用此构造函数。 |
| `View( Context context, AttributeSet attrs )` | 在通过填充 xml 资源构造`View`时调用；`attrs`是在 xml 文件中指定的属性。 |
| `View( Context context, AttributeSet attrs, int defStyle )` | 在通过填充 xml 资源构造`View`时调用；`attrs`是在 xml 文件中指定的属性，`defStyle`是应用于所创建`View`的默认样式。 |
| 方法 | 描述 |
| `void onFinishInflate( )` | 在`View`完成从其 xml 资源填充后调用。 |
| `void onAttachedToWindow( )` | 当此`View`附加到其窗口时调用。 |
| `void onMeasure( int widthMeasuredSpec, int heightMeasuredSpec )` | 调用以测量此`View`及其内容，从而确定此`View`的宽度和高度。 |
| `void onSizeChanged( int width, int height, int oldWidth, int oldHeight )` | 当此`View`的大小发生变化时调用。 |
| `void onLayout( boolean changed, int left, int top, int right, int bottom )` | 当此`View`为其子视图分配位置和尺寸时调用。参数与此`View`相对于其父视图的位置有关。 |
| `void onDraw( Canvas canvas )` | 当`View`绘制其内容时调用。 |

表 8.6 `View`类的部分构造函数和方法

当`View`被设置为活动的内容`View`时，`View`类的以下方法会被自动调用，其中一些方法会被多次调用：`onAttachedToWindow`、`onMeasure`、`onSizeChanged`、`onLayout`、`onDraw`；`onFinishInflate`仅在`View`从 xml 文件填充时被调用。如果我们将所有这些方法添加到本示例中，并在其中添加输出语句到 Logcat，则 Logcat 中的输出如下：

```text
Inside   GameView constructor
Inside   onAttachedToWindow
Inside   onMeasure
Inside   onMeasure
Inside   onSizeChanged
Inside   onLayout
Inside   onMeasure
Inside   onLayout
Inside   onDraw
```

示例 8.1 显示了`GameView`类，它继承自`View`。在本章后面，我们预计`onDraw`方法会被频繁调用，因为我们会以高频率重绘屏幕以更新游戏。因此，我们希望避免在`onDraw`内部声明变量，以使代码尽可能高效。在第 12–16 行，我们声明了各种实例变量来存储鸭子的资源：一个用于定义绘制样式和颜色的`Paint`对象、一个用于鸭子的`Bitmap`（`duck`）、一个用于在`View`内绘制鸭子的矩形（`duckRect`），以及屏幕的高度。

构造函数在第 18–31 行编码。我们期望从`Activity`类实例化一个`GameView`对象。因此，构造函数包含两个整数参数，表示该活动中可用的`width`和`height`。我们在第 20 行将`height`参数赋值给实例变量`height`，并在第 21 行初始化`duck`。我们将高度存储在实例变量中，因为我们需要在`onDraw`方法中访问它。在第 23–25 行，我们根据活动传递给构造函数的`width`和`height`值设置`duckRect`的坐标。我们将矩形定位在屏幕的右上角，将其宽度设置为`width`的 1/5，并设置其高度以保持原始鸭子图像的相同比例。因此，我们将`width`–`width`/5 赋值给其左边缘坐标，将`width`赋值给其右边缘坐标。我们希望将鸭子的高度设置为与宽度相同的缩放因子变化。我们可以轻松地按如下方式计算缩放因子：

```text
new duck width = width / 5 = old duck width * scale
```

因此，

```text
scale = width/( 5 * old duck width )
```

执行浮点除法时要小心：我们希望最终才将维度四舍五入为整数，以尽量减少精度损失。

![](img/ch08exa01.jpg)

示例 8.1 `GameView`类，打鸭子应用，版本 0

我们在第 27 行初始化`paint`，在第 28 行将其颜色设置为黑色，在第 29 行将抗锯齿选项设置为`true`，在第 30 行将`paint`的描边宽度设置为`10`。

`onDraw`方法（第 33–43 行）在`onAttachedToWindow`、`onMeasure`、`onSizeChanged`和`onLayout`被调用后也会自动调用。在第 34 行调用其`super`方法后，我们依次在第 35–36 行绘制炮台底座，第 38–39 行绘制炮管，第 41–42 行绘制鸭子。我们使用`Canvas`类的`drawCircle`方法绘制大炮。前两个参数是圆心的 x 和 y 坐标，第三个参数是圆的半径，第四个参数是一个`Paint`对象，用于定义圆的样式和颜色。要绘制一个圆心为`(0, height)`、半径为`50`的圆，我们使用以下语句：

```java
canvas.drawCircle( 0, height, 50, paint );
```

坐标`(0, height)`表示`View`的左下角。`paint`的样式属性用于绘制圆。由于圆心的位置，只有圆的右上四分之一可见。

实际上，我们希望根据`View`的大小来调整半径（上面的 50）。我们使用 10% 的比例。因此，我们在第 36 行使用以下语句绘制炮台底座：

```java
canvas.drawCircle( 0, height, height / 10, paint );
```

注意，由于我们只绘制四分之一圆，也可以改用`drawArc`方法。它的 API 如下：

```java
public void drawArc( RectF oval, float startAngle, float sweepAngle,
                     boolean useCenter, Paint paint )
```

`RectF`类使用浮点坐标封装一个矩形。我们可以使用以下构造函数创建`RectF`：

```java
public RectF( float left, float top, float right, float bottom )
```

`drawArc`的两个角度参数以度为单位：`startAngle`指定起始角度：0 表示三点钟方向。如果`sweepAngle`为正，则弧按顺时针方向绘制，否则按逆时针方向绘制。如果`useCenter`为`true`，则绘制一个扇形，穿过椭圆的中心（如果`RectF`参数是正方形，则穿过圆的中心）。以下是使用`drawArc`绘制炮台底座的方法：

```java
RectF cannonRect = new RectF( - height / 10, height – height / 10,
                              height / 10, height + height / 10 );
canvas.drawArc( cannonRect, 0.0f, -90.0f, true, paint );
```

在第 39 行，我们使用`Canvas`类的`drawLine`方法绘制炮管。前两个参数是线条一端的 x 和 y 坐标，接下来的两个参数是线条另一端的 x 和 y 坐标。第五个参数是一个`Paint`对象，用于定义线条的样式和颜色。如果要绘制一条端点分别为`(0, height)`和`(100, height – 100)`的线条，使其呈 45 度角，我们使用以下语句：



```java
canvas.drawLine( 0, height, 100, height - 100, paint );
```

同样，我们希望根据`View`的大小来调整炮管的长度。我们使用 20% 的比例（注意，20% 的比例是沿 x 轴和 y 轴方向，而炮管呈 45 度角，因此实际更长。炮管的一部分被炮台底座遮挡）。因此，我们在第 39 行使用以下语句绘制炮管：

```java
canvas.drawLine( 0, height, height / 5, height – height / 5,
                 paint );
```

在本章后面，我们将允许用户通过触摸屏幕来改变大炮的角度。

在第 42 行，我们使用`Canvas`类的`drawBitmap`方法之一绘制鸭子。第一个参数是一个`Bitmap`引用，第二个参数定义在位图中绘制的矩形区域，第三个参数定义在`View`上执行绘制的矩形区域，第四个参数是一个`Paint`对象，用于定义所绘制位图的样式和颜色。我们使用以下语句在`duckRect`矩形内绘制整个`Bitmap duck`：

```java
canvas.drawBitmap( duck, null, duckRect, paint );
```

第二个参数值为`null`表示我们正在绘制整个位图。鸭子绘制在第三个参数`duckRect`所表示的矩形内，该矩形在`onLayout`方法中定义。

示例 8.2 展示了`MainActivity`类。为了获得尽可能大的屏幕，我们扩展了`Activity`类，而不是`AppCompatActivity`类。这样，屏幕不包含操作栏，会稍大一些。它没有加载 XML 资源，而是将其内容`View`设置为`GameView`。在第 10 行，我们声明了一个`GameView`实例变量`gameView`。它在第 26 行的`onCreate`中被实例化。我们在第 27 行将活动的内容`View`设置为`gameView`。

我们在第 24–25 行获取屏幕尺寸，以便将其宽度和高度传递给`GameView`构造函数。然而，屏幕高度包括状态栏的高度。因此，我们在第 16–22 行获取它，并在第 26 行从屏幕高度中减去它，然后将结果值传递给`GameView`构造函数。附录 A 更详细地解释了如何获取状态栏和操作栏的高度。

图 8.1 展示了在模拟器中运行的 Duck Hunting Game 应用版本 0。我们为炮台绘制的圆边缘平滑，没有锯齿，这是因为使用了抗锯齿功能。

![](img/ch08exa02.jpg)

示例 8.2 `MainActivity`类，Duck Hunting 应用，版本 0

![](img/9781284093650_CH08_FIGF01.jpg)

图 8.1 Duck Hunting Game 应用，版本 0，在模拟器中运行

## 8.3 模型

在游戏中，屏幕上可能有许多形状和对象，它们移动、变化并发生碰撞。游戏的功能可能相当复杂，将其封装在模型中会更简单、更清晰。我们的模型将反映游戏的状态及其规则。本游戏中有三个对象：大炮、子弹和鸭子。为了保持简单，用户一次只能从大炮发射一颗子弹。如果子弹击中鸭子或飞出屏幕，则用户可以再次射击。因此，屏幕上始终没有子弹或只有一颗子弹。我们可以将游戏状态定义如下：

- ▸ 整体游戏参数：尺寸（宽度和高度）、更新频率
- ▸ 大炮：位置、角度
- ▸ 子弹：是否已发射、尺寸、位置、速度
- ▸ 鸭子：位置、尺寸、速度、是否被击中或飞行中

为了保持简单，鸭子预期从右向左飞行，大炮预期位于屏幕底部。这些约束在`Game`类中强制执行。

我们在`GameView`类中用于绘制目的的值（例如鸭子和炮台的位置以及游戏尺寸）应从模型中获取。

我们还需要一些功能来捕获游戏过程中发生的事件：

- ▸ 开始游戏。
- ▸ 移动鸭子。
- ▸ 移动子弹。
- ▸ 测试鸭子是否在屏幕外。
- ▸ 测试子弹是否在屏幕外。
- ▸ 管理子弹的状态（已发射或未发射）。
- ▸ 测试鸭子是否被击中。

我们将模型封装在`Game`类中，如示例 8.3 所示。我们选择使用大量实例变量（第 8–29 行）而不是常量来存储游戏参数，例如鸭子或子弹的速度。使用实例变量相对于常量的好处是，它们的值可以在用户玩游戏时修改。如果我们想实现不同难度级别的游戏关卡，例如，可以增加鸭子或子弹的速度，或者减小子弹的尺寸。注意，我们有一个用于炮台角度的实例变量，另一个用于子弹角度。当子弹发射后，我们希望用户能够修改炮台角度以进行下一次射击，而不影响已发射子弹的角度。

许多访问器方法是必需的，因为当我们需要重新绘制对应的`View`时，需要访问与所绘制各种对象相关的数据。`setCannon`方法（第 90–102 行）不仅设置了炮台的位置，还设置了子弹在炮台内的初始位置。

从第 137 行到第 199 行，我们编写了各种方法，用于改变游戏状态、移动鸭子、移动子弹、测试鸭子或子弹是否超出屏幕（在此`Model`中即超出狩猎矩形）、将子弹重新装填到初始位置、改变子弹发射角度，以及测试子弹是否击中鸭子。实例变量`duckShot`表示鸭子是否已被击中。方法`duckHit`测试子弹是否击中了鸭子。如果鸭子未被击中，`moveDuck`方法（第 161–169 行）将鸭子从右向左移动。如果鸭子被击中，则将其以五倍飞行速度向下移动。

![](img/ch08exa03.jpg) ![](img/ch08exa03a.jpg) ![](img/ch08exa03b.jpg) ![](img/ch08exa03c.jpg) ![](img/ch08exa03d.jpg)

示例 8.3 `Game`类，打鸭子应用，版本 1

| 方法 | 描述 |
| --- | --- |
| `boolean intersects( int left, int top, int right, int bottom )` | 如果此`Rect`与四个参数定义的矩形相交，则返回`true`，否则返回`false`。此`Rect`不会被修改。 |

表 8.7 `Rect`类中选定的`intersects`方法

为了测试子弹是否击中了鸭子（第 195–199 行的`duckHit`方法），我们将鸭子周围的矩形与子弹周围的矩形进行比较，并测试它们是否相交。我们使用了`Rect`类中的一个`intersects`方法，如表 8.7 所示。如果四个参数定义的矩形与调用该方法的`Rect`引用相交，则返回`true`，否则返回`false`。

## 8.4 动画对象：让鸭子飞行，打鸭子应用，版本 1

现在我们可以使用`Model`让鸭子从右向左飞过屏幕。为此，我们需要以一定的频率重新绘制`View`。当帧率达到每秒 20–30 帧或更高时，人眼会认为物体在连续运动。帧率越高，物体看起来越像连续运动。然而，帧率越高，对 CPU 的要求也越高。如果我们要求 CPU 在过短时间内处理过多任务，运动就会开始变得卡顿，应用质量也会下降。此外，不同设备的 CPU 速度不同，这使问题更加复杂。对于包含大量移动和交互对象的复杂游戏，建议使用 OpenGL（开放图形库）来加速绘图渲染。OpenGL 定义了一个 API，使开发者可以直接与图形处理器交互。游戏开发者通常使用基于 OpenGL 的游戏引擎来开发游戏。高性能游戏编程超出了本书的范围。我们保持游戏简单，以便 CPU 能够处理。

| 方法 | 描述 |
| --- | --- |
| `void schedule( TimerTask task, long delay, long period )` | 安排`task`在`delay`毫秒后开始执行，之后每隔`period`毫秒执行一次。 |
| `void cancel( )` | 取消此`Timer`已安排的任务。 |

表 8.8 `Timer`类中选定的方法

| 方法 | 描述 |
| --- | --- |
| `void run( )` | 按指定频率自动调用；重写此方法并在其中执行任务。 |
| `boolean cancel( )` | 取消此`TimerTask`。 |

表 8.9 `TimerTask`类中选定的方法

`java.util`包中的`Timer`类提供了多个`schedule`和`scheduleAtFixedRate`方法，用于设置一个指定类型的`TimerTask`任务，该任务可以执行一次，也可以按指定频率执行，并在指定延迟后开始。我们还可以取消当前由`Timer`安排的任务。表 8.8 展示了一个`schedule`方法和`cancel`方法。

各种`schedule`和`scheduleAtFixedRate`方法的第一个参数是一个`TimerTask`对象。`TimerTask`类实现了`Runnable`接口，也来自`java.util`包。它是`abstract`的，需要被重写以定义要执行的自定义任务。当我们继承`TimerTask`时，应提供一个构造函数并重写`run`方法。`run`方法会按指定频率自动调用并执行任务。表 8.9 展示了`run`和`cancel`方法。

我们定义了一个`GameTimerTask`类，它继承自`TimerTask`类。在`run`方法内部，我们使用`Model`更新游戏状态。在退出`run`方法之前，我们强制重新绘制`View`，以便用户在屏幕上看到的内容反映当前游戏状态。为此，我们需要在`GameTimerTask`内部持有游戏和`View`的引用。有几种方法可用于重新绘制`View`。表 8.10 列出了其中一些方法。带有四个参数的方法允许我们重新绘制由这四个参数定义的`View`矩形区域。如果我们知道只有部分`View`发生了变化，这可以节省宝贵的 CPU 时间。`View`类的`postInvalidate`方法会自动调用`onDraw`，并且可以从非用户界面线程中调用，这正好符合我们在`GameTimerTask`的`run`方法中执行的情况。因此，在`run`方法的末尾，我们调用`postInvalidate`来重新绘制`View`。

| 方法 | 描述 |
| --- | --- |
| `void invalidate( )` | 通过调用`onDraw`刷新整个`View`。此方法必须从用户界面线程调用。 |
| `void postInvalidate( )` | 通过调用`onDraw`刷新整个`View`。此方法可以从用户界面线程外部调用。 |
| `void invalidate( int top, int left, int right, int bottom )` | 通过调用`onDraw`刷新此`View`内由四个参数定义的矩形区域。此方法必须从用户界面线程调用。 |
| `void postInvalidate( int top, int left, int right, int bottom )` | 通过调用`onDraw`刷新此`View`内由四个参数定义的矩形区域。此方法可以从用户界面线程外部调用。 |

表 8.10 `View`类中强制调用`onDraw`的方法

整体逻辑如下：

```java
// 在 MainActivity 类内部
Timer timer = new Timer( );
// 立即启动任务，每秒运行 10 次（每 100 毫秒）
timer.schedule( new GameTimerTask( this ), 0, 100 );

// 在 GameTimerTask 类的 run 方法内部
// 1 - 使用 Game 引用更新游戏状态
// 2 – 假设 gameView 是 View 的引用，
// 调用 postInvalidate 强制调用 onDraw
gameView.postInvalidate( );

// 在 GameView 的 onDraw 方法内部
// 根据游戏状态绘制炮台、子弹和鸭子
```

总结：

- ▸ `GameTimerTask`类的`run`方法要求`Model`更新游戏状态，然后要求游戏`View`重新绘制自身。
- ▸ `GameView`类的`onDraw`方法根据游戏状态更新`View`。

![](img/ch08exa04.jpg)

示例 8.4 `GameTimerTask`类，打鸭子应用，版本 1

示例 8.4 展示了`GameTimerTask`类。我们在第 3 行导入了`TimerTask`，并在第 5 行让该类`extends`它。我们声明了两个实例变量（第 6–7 行）：`game`（指向游戏的`Game`引用）和`gameView`（指向视图的`GameView`引用）。我们在第 12 行使用`game`启动游戏，并在第 16–18 行的`run`方法内更新游戏状态。我们在第 19 行使用`gameView`调用`postInvalidate()`，以触发对`GameView`的`onDraw`方法的调用。

我们在第 9–13 行提供了一个接受`GameView`参数`view`的构造函数；第 10 行将`view`赋值给`gameView`。我们在第 11 行调用`getGame()`访问器（我们需要将`getGame`方法添加到`GameView`类中），以便将游戏的引用赋值给`game`。我们期望从`GameView`类内部实例化一个`GameTimerTask`对象，并将`this`传递给构造函数。

示例 8.5 展示了`GameView`类。我们不再显示一只简单的鸭子，而是使用从三个透明 PNG 文件创建的三个`Bitmap`，在鸭子飞行时为其制作动画。我们将三个文件`anim_duck0.png`、`anim_duck1.png`和`anim_duck2.png`放入项目的`drawable`目录中。我们打算用这三个文件创建一个四帧动画（0-1-2-1），并将这些可绘制资源存储在数组`TARGETS`中（第 14–15 行）。本例中数组有四个元素，但我们可以轻松添加更多帧来改进鸭子动画。我们现在有一个`Bitmap`数组`ducks`，在第 17 行声明。实例变量`duckFrame`（第 18 行）存储当前在数组`ducks`中的索引。我们用它来访问正确的`Bitmap`，以便在`onDraw`方法中绘制。我们在第 20 行声明了一个`Game`实例变量`game`。通常，我们在控制器（即`MainActivity`类）中包含对模型的引用。在本例中，我们根据模型中的值设置了`onDraw`方法中绘制内容的几个参数（炮座和炮管、鸭子、子弹）。因此，在`GameView`中有一个`Game`引用会很方便，这样我们就可以在`onDraw`方法中访问`Game`各个实例变量的值。

![](img/ch08exa05.jpg) ![](img/ch08exa05a.jpg)

示例 8.5 `GameView`类，打鸭子应用，版本 1

数组`ducks`与数组`TARGETS`对应，在第 24 行实例化，并在第 25–27 行用从`TARGETS`元素生成的`Bitmap`填充。

我们假设所有 PNG 文件具有相同的宽度和高度，并在第 28 行计算缩放因子后，使用第一个文件在第 29–30 行构造一个`Rect`。我们在第 31 行实例化`game`时将该`Rect`传递给`Game`构造函数。我们还希望动态设置鸭子和子弹的速度。实际上，如果屏幕分辨率更高，鸭子和子弹应该移动得更快。如果屏幕宽 1000 像素，那么鸭子速度为每秒 0.03 像素，子弹速度快 10 倍，为每秒 0.3 像素。在第 36 行设置游戏的狩猎矩形后，我们在第 37–38 行调用`setCannon()`来设置大炮的尺寸：我们将大炮定位在狩猎矩形的左下角，并根据视图的大小调整其大小，以尽可能实现设备无关性。

我们希望这个游戏的屏幕刷新率约为每秒 10 次。因此，我们在第 13 行定义了常量`DELTA_TIME`，并为其赋值`100`。我们在第 34 行将该值传递给`game`，并在第 43 行设置炮管的尺寸。

`onDraw`方法编码在第 46–64 行。我们在第 48–50 行绘制大炮，从`game`中获取其中心坐标和半径。我们在第 52–59 行绘制炮管，也从`game`中获取其坐标、尺寸和角度。在第 63 行绘制鸭子的`Bitmap`之前，我们在第 62 行更新`duckFrame`的值，以便访问数组`ducks`中的下一个`Bitmap`。

我们在第 66–68 行为`game`提供了一个访问器。我们在示例 8.6 的`GameTimerTask`内部调用它。

示例 8.6 展示了`MainActivity`类中的编辑。我们在第 30 行实例化一个`Timer`对象，并在第 31–32 行安排一个`GameTimerTask`每秒运行`10`次，立即开始。

![](img/ch08exa06.jpg)

示例 8.6 `MainActivity`类中的编辑，打鸭子应用，版本 1

图 8.2 展示了打鸭子游戏应用版本 1 在模拟器中运行的情况，鸭子正在屏幕中央飞行。请注意，模拟器的性能远低于实际设备，可能无法以指定的帧率绘制鸭子。

![](img/9781284093650_CH08_FIGF02.jpg)

图 8.2 打鸭子游戏应用版本 1 在模拟器中运行

## 8.5 处理触摸事件：移动大炮和射击，打鸭子应用，版本 2

在版本 2 中，我们允许用户通过单次点击或滑动屏幕来移动炮管。无论用户触摸屏幕的哪个位置，我们都将炮管指向该点。我们还通过双击屏幕任意位置来启用射击。但是，我们不希望双击改变炮管的角度。为了实现这一点，我们需要捕获触摸事件，并将其处理为确认的单次点击或滑动（移动炮管），或者处理为双击（射击）。如果是确认的单次点击或滑动，我们获取触摸的 x 和 y 坐标，并在`game`中设置炮管角度的值。炮管的重新绘制应该自动发生，因为我们在`onDraw`方法中绘制炮管时会考虑炮管角度的值。如果是双击，我们调用`game`的`fireBullet()`方法。



实现这一点的最简单方法是在`GameView`类中使用`GestureDetector`，创建一个扩展`GestureDetector.SimpleOnGestureListener`类的`private`类，并重写以下方法：`onSingleTapConfirmed()`、`onScroll()`和`onDoubleTapEvent()`。

通常，事件应该在控制器内部处理。因此，我们将所有与事件相关的代码添加到`MainActivity`类中。示例 8.7 展示了`MainActivity`类的新部分。在第 7 行和第 8 行，我们导入了`GestureDetector`和`MotionEvent`类。在第 14 行声明了一个`GestureDetector`实例变量`detector`。因为我们需要根据用户交互访问和更新模型（改变炮管角度、发射子弹等），所以拥有一个`Game`实例变量（第 15 行的`game`）会很方便。`game`实例变量引用的`Game`对象与`GameView`类的`game`实例变量（第 38 行）相同。

我们在第 49–74 行编写了`private`类`TouchHandler`，它扩展了`GestureDetector.SimpleOnGestureListener`。无论我们在`onSingleTapConfirmed()`还是`onScroll()`方法中执行，我们都希望执行相同的代码，因此我们创建了一个单独的方法`updateCannon()`，并调用它，传递`MouseEvent`参数。在`updateCannon()`内部（第 68–73 行），我们在第 69–70 行计算触摸点相对于大炮中心的 x 和 y 坐标，并在第 71 行使用`Math`类的`atan2()`方法计算角度。然后我们在第 72 行调用`game`的`setCannonAngle()`方法，并传递计算出的角度。为了获取触摸坐标，我们使用`getX()`和`getY()`方法，因为它们返回相对于视图的 x 和 y 坐标，而`getRawX()`和`getRawY()`方法则返回绝对坐标。

在`onCreate`方法中，我们在第 40 行实例化了`detector`，并将第 39 行声明并实例化的`TouchHandler`对象`th`作为其第二个参数传递。接着，在第 41 行调用`setOnDoubleTapListener`方法，传入`th`。因此，假设事件分发已在`onTouchEvent`中设置好，手势和触摸操作会触发`TouchHandler`类中方法的执行。在`onTouchEvent`方法（第 44–47 行）中，我们通过`detector`调用`GestureDetector`类的`onTouchEvent`方法，以便将各种触摸事件分发给`TouchHandler`类的九个方法中的适当方法（其中三个在类内重写，六个继承自`GestureDetector.SimpleOnGestureListener`的空方法）。

![](img/ch08exa07.jpg) ![](img/ch08exa07a.jpg)

示例 8.7 `MainActivity`类，打鸭子应用，版本 2

`GameView`类中唯一的改动是绘制子弹。这是在`onDraw`方法中完成的。示例 8.8 展示了更新后的`onDraw`方法。如果子弹未离开屏幕（第 62 行），我们就在第 63–64 行使用存储在实例变量`game`中的位置和半径绘制它。游戏进行时，子弹的位置每 100 毫秒更新一次。这发生在`GameTimerTask`类的`run`方法中。

示例 8.9 展示了更新后的`GameTimerTask`类。唯一的改动在`run`方法的第 17–20 行。如果子弹离开屏幕（第 17 行），我们将其装填进炮管（第 18 行）。如果子弹在屏幕上，我们检查它是否已被发射（第 19 行）。如果是，我们通过在第 20 行调用`moveBullet`（传入`game`）来更新其位置。在第 23 行调用`postInvalidate`后，`GameView`类的`onDraw`方法会在屏幕上的新位置重新绘制子弹。如果子弹在屏幕上但未被发射，则意味着它仍在炮管内，这种情况下无需更新。

![](img/ch08exa08.jpg)

示例 8.8 `GameView`类的`onDraw`方法，打鸭子应用版本 2

![](img/ch08exa09.jpg) ![](img/ch08exa09a.jpg)

示例 8.9 `GameTimerTask`类，打鸭子应用，版本 2

![](img/9781284093650_CH08_FIGF03.jpg)

图 8.3 打鸭子应用版本 2 在模拟器中运行

图 8.3 展示了打鸭子游戏应用版本 2 在模拟器中运行的情况，此时用户已移动炮管并发射了一颗子弹。

## 8.6 播放声音：射击、碰撞检测、打鸭子应用版本 3

在版本 2 中，子弹击中鸭子时没有任何反应。在版本 3 中，当鸭子被击中时，我们会播放一个小音效，并让鸭子掉落到地面（实际上，我们让鸭子穿过地面）。我们还会在发射子弹时播放音效。

| 方法 | 描述 |
| --- | --- |
| `int load( Context context, int resId, int priority )` | 从由`resId`标识的上下文中加载声音。`priority`参数在撰写本文时未使用。默认使用 1。返回声音 ID。 |
| `int play( int soundId, float leftVolume, float rightVolume, int priority, int loop, float rate )` | 播放声音 ID 为`soundId`的声音。如果`loop`为 0，则播放一次；如果`loop`为–1，则循环播放。`rate`是播放速率，范围 0.5 到 2.0，1.0 为正常播放速率。 |
| `void pause( int soundId )` | 暂停声音 ID 为`soundId`的声音。 |
| `void resume( int soundId )` | 恢复播放声音 ID 为`soundId`的声音。 |

表 8.11 `SoundPool`类的部分方法

`SoundPool`类属于`android.media`包，使我们能够管理和播放声音。我们可以使用其方法：

- ▸ 预加载声音，以便在单次或循环播放时没有延迟。
- ▸ 调整音量和播放速率。
- ▸ 播放、暂停、恢复声音。
- ▸ 同时播放多个声音。

表 8.11 列出了`SoundPool`类的一些选定方法。

`SoundPool`类包含一个`public static`内部类`Builder`，我们可以用它来创建`SoundPool`对象。由于该类是在 API 级别 21 中引入的，我们需要确保模块 gradle 文件中指定的最低 SDK 版本为 21，如示例 8.10 所示。我们首先使用`SoundPool.Builder`的默认构造函数实例化一个`SoundPool.Builder`对象，然后调用`build`方法，该方法返回一个`SoundPool`引用。表 8.12 展示了`SoundPool.Builder`的默认构造函数和`build`方法。

![](img/ch08exa10.jpg)

示例 8.10 `build.gradle`（Module:app）文件的部分内容，最低 SDK 为 21

| 默认构造函数 | 描述 |
| --- | --- |
| `SoundPool.Builder( )` | 构造一个`SoundPool.Builder`对象，此时最多可播放一个流。 |

| 方法 | 描述 |
| --- | --- |
| `SoundPool build( )` | 返回一个`SoundPool`对象引用。 |
| `SoundPool.Builder setMaxStreams ( int maxStreams )` | 设置可同时播放的最大流数量。返回此`SoundPool.Builder`。 |

表 8.12 `SoundPool.Builder`类的默认构造函数和`build`方法

以下序列展示了如何创建`SoundPool`对象。

```java
SoundPool.Builder poolBuilder = new SoundPool.Builder( );
SoundPool pool = poolBuilder.build( );
```

创建`SoundPool`后，下一步是加载声音。就像我们使用布局 XML 文件的 ID 来填充它一样，我们可以使用声音的资源 ID 来加载它。将声音资源放入`res`目录时，通常创建一个名为`raw`的目录，并将声音文件放入其中。在版本 3 中，我们在发射子弹时播放一个音效，在鸭子被击中时播放另一个音效。因此，我们创建`raw`目录，并将`cannon_fire.wav`和`duck_hit.wav`声音文件（通过复制粘贴）添加进去。图 8.4 显示了将`cannon_fire.wav`和`duck_hit.wav`文件放入刚创建的`raw`目录后的目录结构。

在`Activity`类中，我们可以使用`SoundPool`的其中一个`load`方法加载`cannon_fire.wav`，语句如下：

```java
// 加载位于 raw 文件夹中的第一个声音，
// 使用资源 ID
// this, this Activity, “is a” Context
int fireSoundId = pool.load( this, R.raw.cannon_fire, 1 );
```

注意，在指定`raw`目录中的资源时，我们不包含文件名的扩展名。这意味着该目录中不应有两个名称相同但扩展名不同的声音文件。

假设名为`cannon_fire.wav`的声音已加载，并且`load`方法返回了一个整数 ID，我们将其存储在`int`变量`fireSoundId`中。我们可以按如下方式播放一次该声音（我们将`0`指定为`play`的倒数第二个参数）：

```java
// 以正常速度播放 cannon_fire.wav 一次
pool.play( fireSoundId, 1.0f, 1.0f, 1, 0, 1.0f );
```

![](img/9781284093650_CH08_FIGF04.jpg)

图 8.4 `raw`目录中的`cannon_fire.wav`和`duck_hit.wav`文件

如果我们有一个名为`background.wav`的声音已加载，其声音 ID 为`backgroundSoundId`，我们可以按如下方式播放该声音并无限循环（我们将`–1`指定为`play`的倒数第二个参数）：

```java
// 以正常速度播放声音并无限循环
pool.play( backgroundSoundId, 1.0f, 1.0f, 1, -1, 1.0f );
```

我们需要在发射子弹或鸭子被击中时播放声音。发射子弹的代码位于`MainActivity`类中。检查鸭子是否被击中的代码位于`GameTimerTask`类中。因此，在`MainActivity`类中，我们提供一个播放击中音效的方法，以便从`GameTimerTask`类中调用。

示例 8.11 展示了更新后的`MainActivity`类。在第 6 行，我们导入了`SoundPool`类。在第 18–20 行，我们声明了三个实例变量：`pool`（一个`SoundPool`引用）、`fireSoundId`和`hitSoundId`（两个`int`类型，分别存储子弹发射和鸭子被击中时播放的两个声音的 ID）。

![](img/ch08exa11.jpg) ![](img/ch08exa11a.jpg)

示例 8.11 `MainActivity`类，打鸭子应用，版本 3

在第 48–50 行，我们实例化了实例变量`pool`，并使其能够同时播放两个声音，尽管我们并不需要这个特性：两个声音都很短，而且由于我们一次只能发射一颗子弹，发射声和击中声总是会在不同时间播放。

我们在第 51–52 行加载了两个声音，向`load`方法传递了声音资源 ID。`R.raw.cannon_fire`和`R.raw.duck_hit`分别标识了`res`目录下`raw`文件夹中的`cannon_fire.wav`和`duck_hit.wav`文件。

当用户双击时，我们在`TouchHandler`类的`onDoubleTapEvent`方法（第 66–72 行）中执行操作。每当发射子弹时，我们播放`bullet_fire.wav`声音（第 69 行）。

在第 60–62 行，我们编写了`playHitSound`方法。在其中，我们播放一次`duck_hit.wav`声音。该方法不在本类中使用，而是在鸭子被击中时从`GameTimerTask`类中调用。

示例 8.12 展示了`GameTimerTask`类的`run`方法中的更改，这是该类中唯一的更改。当鸭子被击中以及鸭子离开屏幕时，我们更新游戏状态。当鸭子被击中时，我们还播放击中声音。如果鸭子离开屏幕（第 21 行），我们不仅希望让它重新开始飞行（第 23 行），还希望确保其状态为未被击中（第 22 行）。实际上，鸭子有可能在被击中后垂直离开屏幕（此时其状态为已被击中）。

如果鸭子还在屏幕上，我们检查它是否被击中（第 24 行）。如果没有，则无需操作。如果被击中，我们将其状态设置为已击中（第 25 行）。这反过来会影响我们在`Game`类中移动鸭子的方式（垂直从上到下，而不是水平从右到左）。我们还重新加载子弹（第 27 行），并播放击中声音以表示鸭子已被击中。我们在第 26 行通过调用`MainActivity`类的`playHitSound`方法来实现这一点。为了获取`MainActivity`引用，我们使用`gameView`调用`getContext`方法，并将返回的`Context`强制转换为`MainActivity`。

![](img/ch08exa12.jpg)

示例 8.12 `GameTimerTask`类的`run`方法，打鸭子应用，版本 3

![](img/ch08exa13.jpg)

示例 8.13 `GameView`类的更新后的`onDraw`方法，打鸭子应用，版本 3

我们只需要在`GameView`类中做一处更改：在鸭子被击中后正确显示它。如果鸭子被击中，我们停止动画，只显示一帧，即最后一帧（本例中是第一帧；我们可以修改此示例，使用超过四帧来制作鸭子动画，这样显示第一帧才有意义）。因此，`GameView`类中唯一的更改是鸭子的绘制，这发生在`onDraw`方法中，如示例 8.13 所示。

我们在第 68 行检查鸭子是否被击中。如果是，我们在第 69–70 行绘制对应第一帧动画的`Bitmap`。如果鸭子未被击中，我们继续让它飞行，根据`duckFrame`的值绘制`ducks`数组中的当前`Bitmap`（第 72–73 行）。

图 8.5 展示了打鸭子游戏应用版本 3 在模拟器中运行，用户击中鸭子后的画面。

![](img/9781284093650_CH08_FIGF05.jpg)

图 8.5 打鸭子游戏应用版本 3 在模拟器中运行，用户击中鸭子后的画面

## 章节总结

- `android.graphics`包包含许多类，如`Paint`、`Canvas`、`Bitmap`、`BitmapFactory`，我们可以用它们来绘制图形。
- 当我们扩展`View`类时，必须重写`View`类的一个构造函数，并调用`super`构造函数。
- 要在`View`上绘制，我们可以重写`View`类的`onDraw`方法。
- `onDraw`方法有一个`Canvas`类型的参数。我们可以用它来在`View`上绘制形状和位图。
- 我们可以使用`BitmapFactory`类的`decodeResource`方法将文件转换为`Bitmap`。
- `Canvas`类的各种绘制方法接受一个`Paint`参数。我们通过指定该`Paint`参数的相应属性来定义绘制属性，例如颜色和样式。
- 我们可以通过调用`postInvalidate`并传入`View`引用来强制调用`onDraw`。
- 我们可以使用`Timer`类来安排一个任务以指定的频率执行。
- 要定义该任务，我们扩展`TimerTask`类并重写其`run`方法。
- `SoundPool`类可用于管理和播放声音。
- 可以从资源（例如`.wav`声音文件）加载声音。
- `SoundPool`类包含播放、暂停和恢复播放声音的方法。
- `SoundPool`类的`play`方法接受参数来控制声音的播放方式（包括音量和播放速率），可以循环播放或播放一次或多次。

![](img/common.jpg)

## 练习、问题和项目

### 选择题

1. 哪个类用于指定我们要绘制的内容（形状、位图等）？
   - `View`
   - `Paint`
   - `Canvas`
   - `Draw`

2. 哪个类用于定义绘制的方式（样式、颜色等）？
   - `View`
   - `Paint`
   - `Canvas`
   - `Draw`

3. 如果我们想在`View`内部绘制，需要重写哪个方法？
   - `draw`
   - `paint`
   - `onDraw`
   - `onPaint`

4. 我们可以调用`View`类的哪个方法来强制重绘该`View`？
   - `reDraw`
   - `rePaint`
   - `post`
   - `postInvalidate`

5. 哪个类具有可用于创建`Bitmap`对象的静态方法？
   - `Bitmap`
   - `BitmapFactory`
   - `MakeBitmap`



`CreateBitmap`

## 选择题

### 6. 哪个类可用于安排一个任务以指定的频率运行？

- `System`
- `Timer`
- `Task`
- `Schedule`

### 7. 要定义一个将以指定频率运行的任务，我们应该扩展哪个类？

- `Task`
- `TimerTask`
- `TaskTimer`
- `Scheduler`

### 8. 问题 7 中的类的哪个方法应该被重写，以执行计划以指定频率运行的任务？

- `start`
- `task`
- `run`
- `thread`

### 9. 一个 `SoundPool` 对象可以同时播放多少个声音？

- 0
- 仅 1 个
- 0、1 或多个

### 10. 当我们调用 `SoundPool` 类的 `play` 方法时，什么标识了要播放的声音？

- 声音名称
- `SoundPool` 对象
- 声音 ID
- 声音的资源 ID

## 补全代码

### 11

一个名为 `paint` 的 `Paint` 对象已被声明并实例化。修改它，使其颜色为黄色，描边粗细为 20。

### 12

在 `onDraw` 内部，绘制一个实心红色圆，圆心在（100, 200），半径为 50。

### 13

在 `onDraw` 内部，绘制一个绿色空心正方形（内部不填充），位于当前 `View` 的中心，边长为 50。

### 14

在 `onDraw` 内部，从（50, 200）开始绘制蓝色的“HELLO ANDROID”。

### 15

在 `onDraw` 内部，从位于 `drawable` 目录中的图像文件 `my_image.png` 中绘制一个位图到屏幕上的某个位置。

### 16

在某个类中，你有一个名为 `myView` 的实例变量，它是 `View` 的引用。编写代码强制重绘该 `View`。

### 17

我们编写了一个名为 `MyTask` 的类，它继承自 `TimerTask`，并包含了其 `run` 方法。请调度该类的实例，使其每秒运行 50 次，从一秒钟后开始。

### 18

在 `res` 目录下的 `raw` 目录中，有一个名为 `my_sound.wav` 的声音文件。编写代码将其播放一次。

```java
SoundPool.Builder sb = new SoundPool.Builder( );
SoundPool pool = sb.build( );
// 你的代码写在这里
```

## 编写一个应用

### 19

修改本章中的打鸭子应用，使其有两只鸭子，而不是一只。

### 20

修改本章中的打鸭子应用，使得我们不必等到子弹离开屏幕或鸭子被击中才能发射另一颗子弹。

### 21

修改本章中的打鸭子应用，加入一个漂亮的背景（水、太阳、草地等），该背景由至少一张图片和三个形状绘制组成。

### 22

修改本章中的打鸭子应用，使得我们用霰弹枪而不是加农炮射击。霰弹枪会发射出一片子弹，例如三颗。你可以假设这些子弹位于一个圆内，并以相同速度移动。至少有一颗子弹击中鸭子，鸭子才会被击落。

### 23

编写一个应用，显示一个台球（可以使用 1 到 15 中的任意数字）。仅使用形状，不要使用位图。

### 24

编写一个手电筒应用，要求如下：颜色可以从一种颜色（颜色 A）连续变化到另一种颜色（颜色 B）。如果屏幕显示颜色 A，当用户从左向右滑动屏幕时，屏幕从颜色 A 连续变化到颜色 B。当用户从右向左滑动屏幕时，屏幕从颜色 B 连续变化到颜色 A。

### 25

编写一个包含两个活动的应用：第一个活动向用户提供一些可绘制的内容，并附带一些样式或颜色选项；第二个活动负责绘制它们。

### 26

编写一个包含两个活动的应用：第一个活动显示三个按钮，上面显示网站名称（例如 Yahoo!、Google 或 Facebook）。当用户点击其中一个时，第二个活动显示该网站的徽标图形。

### 27

编写一个绘图应用，用户可以通过在两点之间滑动屏幕来绘制两点之间的直线。为用户提供一些绘图选项：从几种颜色中选择，以及选择所画线条的粗细。

### 28

编写一个绘图应用，用户可以通过在屏幕上移动手指来绘制图形（提示：曲线可以由多条直线组成）。为用户提供一些绘图选项：从几种颜色中选择，以及选择所画内容的粗细。

### 29

编写一个应用，在屏幕上显示一个你选择的棋子。用户可以通过触摸它、移动手指并释放来拾起它并将其移动到屏幕上的另一个位置。

### 30

编写一个关于以下游戏的应用：一些敌人从屏幕顶部垂直向下移动。玩家由屏幕底部的一个形状、位图甚至标签表示。用户可以通过触摸并移动手指来移动玩家。我们的目标是避开正在下落的敌人。当敌人移出屏幕时，另一个敌人会从屏幕顶部的随机位置下落。当敌人碰到玩家时游戏结束。包含一个模型（Model）。

### 31

与问题 30 相同，但添加一个声音：当敌人从屏幕顶部开始时播放一个声音，当敌人碰到玩家时播放另一个声音。

### 32

与问题 30 相同，但多个敌人可以同时下落——不是只有一个敌人，而是一个敌人数组。

### 33

编写一个模拟乒乓球游戏的应用。用户可以在屏幕底部移动一个球拍，一个球在屏幕上移动。球碰到屏幕的侧边和上边缘时会反弹。如果球越过球拍，游戏结束。包含一个模型（Model）。

### 34

编写一个类似点唱机的应用，用户可以从至少五个声音中选择一个并播放。为所选声音提供一些选项：仅播放一次或循环播放，不同的播放速率。包含一个模型（Model）。

# 第九章：片段（Fragments）

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

为了支持像平板电脑这样的大屏幕设备，Google 在 API 级别 11 中引入了片段。片段是活动的一部分，可以帮助管理屏幕的一部分。我们可以将片段视为活动中的迷你活动。图 9.1 展示了本章应用第 4 版的屏幕，它被分为三个部分，背景分别为蓝色、红色和绿色。我们可以组织该屏幕，使每个部分都是一个片段。片段是可重用的。它们可以在同一个应用或不同的应用中重复使用。因此，使用片段是可取的。

在本章中，我们演示如何使用和管理片段。我们构建一个玩猜单词游戏（hangman）的应用。我们使用模型-视图-控制器架构，但尽可能简化模型，以便专注于片段的工作原理。此外，我们还讨论如何嵌套布局，使每个片段由单独的布局管理器管理。

## 9.1 模型

模型是 `Hangman` 类，如示例 9.1 所示。它封装了一个游戏，用户必须猜出一个单词中的所有字母，但只有有限的尝试次数。我们将模型保持在最低限度，并将可能的单词数量限制为几个。

我们在第 6 行提供了允许猜测次数的默认值，并在第 7 行提供了一个硬编码单词数组。在第 8 行，实例变量 `word` 存储要猜测的单词。`guessesAllowed` 和 `guessesLeft` 实例变量跟踪允许的猜测次数和用户剩余的猜测次数。最后，`indexesGuessed` 数组跟踪用户到目前为止正确猜出的 `word` 字符串中字母的索引。值为 `true` 表示该索引处的猜测正确。

![](img/9781284093650_CH09_FIGF01.jpg)

图 9.1 猜单词应用第 4 版，水平方向运行

![](img/ch09exa01.jpg) ![](img/ch09exa01a.jpg)

示例 9.1 `Hangman` 类

`Hangman` 构造函数（第 13–23 行）设置了允许猜测次数的值（第 14–17 行）。然后它从数组 `words` 中随机选择一个单词（第 19–21 行），并实例化 `indexesGuessed` 数组。我们可以设想一个更复杂的模型，其中另一个构造函数可以从文件、数据库甚至远程网站中提取可能的单词列表，然后随机选择一个。

我们提供了玩游戏的方法（第 33–43 行）、获取单词完成状态的方法（第 45–53 行）以及检查游戏是否结束的方法（第 55–69 行）。我们还为 `guessesAllowed` 和 `guessesLeft` 提供了访问器（第 25–27 行和第 29–31 行）。

图 9.1 显示了一个实际游戏。在左侧窗格的底部，是用户剩余的猜测次数。在右侧窗格的上部，是用户到目前为止正确猜出的字母，我们提供了一个 `EditText` 来输入下一个字母。在右侧窗格的底部，是游戏的状态或最终结果。

## 9.2 片段

由于片段自 API 级别 11 起就已可用，因此我们在创建应用时需要指定 API 级别 11 或更高（在撰写本文时，默认值为 API 级别 15）。

![](img/9781284093650_CH09_FIGF02.jpg)

图 9.2 `Fragment` 及其选定子类的继承层次结构

片段必须始终嵌入在活动中，尽管片段拥有自己的生命周期方法，但这些方法直接依赖于片段所属父活动的生命周期方法。例如，如果活动被停止或销毁，那么片段也会自动被停止或销毁。一个活动可以包含多个片段，只要活动在运行，这些片段就可以彼此独立地拥有自己的生命周期。片段是可重用的，可以在多个活动中使用。片段可以定义自己的布局，也可以不可见并在后台执行任务。

为了编写我们自定义的片段，我们需要扩展 `Fragment` 类，它是 `Object` 的直接子类。

`Fragment` 类有多个子类，它们封装了特定功能的片段。图 9.2 展示了其中一部分。`DialogFragment` 显示一个对话框窗口，该窗口显示在活动视图的上方。`ListFragment` 显示一个项目列表，并在用户选择其中一项时提供事件处理。`PreferenceFragment` 以列表形式显示偏好设置的层级结构。`WebViewFragment` 显示一个网页。

这些 `Fragment` 类的子类封装了特定的片段功能。例如，当我们想在屏幕的某个部分显示一个用户可交互的项目列表时，`ListFragment` 类非常有用。点击某个项目可能会触发屏幕另一部分中另一个片段内的某些变化。

在本章中，为了更好地理解片段的工作原理，我们将构建自己的 `Fragment` 子类。我们将探讨以下主题：

- 如何仅使用 XML 为活动创建并添加片段。
- 如何使用 XML 和代码为活动创建并添加片段。
- 如何仅使用代码为活动创建并添加片段。
- 片段及其活动如何通信。
- 如何创建并添加一个不可见片段。
- 如何使片段可重用。

## 9.3 使用布局 XML 文件定义片段并将其添加到活动中——Hangman 应用，版本 0

在应用的版本 0 中，我们展示了如何定义和添加片段；我们尚未使用模型，并尽可能保持应用的简单。创建应用时，我们选择了空活动模板。

示例 9.2 展示了 `activity_main.xml` 文件。顶层 `LinearLayout` 元素内部有两个元素：一个 `fragment` 元素（第 9–15 行定义）和一个 `LinearLayout` 元素（第 17–37 行定义）。在第 11 行，我们指定该片段是 `GameControlFragment` 类的一个实例，该类将在本节稍后编写。顶层 `LinearLayout` 元素的 `orientation` 属性为 `horizontal`（第 6 行），因此片段位于屏幕左侧，而 `LinearLayout` 位于屏幕右侧。它们的 `android:layout_weight` 值均为 `1`（第 13 行和第 20 行），因此它们各占屏幕的 50%（= 1/(1+1)），如图 9.1 所示（片段为红色，`LinearLayout` 为蓝色和绿色），并在图 9.3 中进行了说明。`LinearLayout.LayoutParams` 类的 `android:layout_weight` XML 属性使我们能够指定每个 `View` 在其父 `LinearLayout` 中应占用的空间大小。我们在第 14 行和第 21 行将 `fragment` 和 `LinearLayout` 元素的 `android:layout_width` 属性值指定为 `0dp`。这是使用 `android:layout_weight` 属性时的典型做法。`0dp` 值表示我们希望让系统根据 `layout_weight` 属性的值为各个元素分配空间。

![](img/ch09exa02.jpg)

示例 9.2 `activity_main.xml` 文件，Hangman 应用，版本 0

![](img/9781284093650_CH09_FIGF03.jpg)

图 9.3 权重为 1 和 1 时的宽度分布

![](img/9781284093650_CH09_FIGF04.jpg)

图 9.4 权重为 1 和 3 时的宽度分布

如果将 `android:layout_weight` 值改为 1 和 3，则屏幕比例变为 25%（1/(1+3)）和 75%（3/(1+3)），如图 9.4 所示。

在 `LinearLayout` 元素内部，我们在第 23–28 行和第 30–35 行定义了两个 `LinearLayout` 元素。由于该 `LinearLayout` 元素的 `orientation` 为 `vertical`（第 18 行），这两个 `LinearLayout` 元素将分别位于其顶部和底部（在图 9.1 中显示为蓝色和绿色）。它们的 `android:layout_weight` 值均为 `1`（第 27 行和第 34 行），因此它们各占屏幕右侧的 50%（图 9.1 中蓝色和绿色部分的高度相同）。为了更好地可视化它们的位置，我们分别将它们着色为蓝色（第 26 行）和绿色（第 33 行）。在本章稍后，我们将在每个元素中放置一个片段。我们必须为 `fragment` 元素指定一个 id（第 10 行）。如果不这样做，应用将在运行时崩溃。

示例 9.3 展示了 `fragment_game_control.xml` 文件（我们将其放置在布局目录中）。我们使用此布局 XML 文件作为屏幕的左侧面板，该面板由示例 9.2 中的 `fragment` 元素预留。它由一个 `LinearLayout` 管理（其背景为红色（第 5 行））。

![](img/ch09exa03.jpg)

示例 9.3 `fragment_game_control.xml` 文件，Hangman 应用，版本 0

与活动一样，片段也有多个生命周期方法，如表 9.1 所示。表中标记为“a”的方法在片段创建或重新启动时自动调用。标记为“b”的方法在片段变为非活动状态或关闭时自动调用。请注意，所有这些方法都是 `public` 的，这与 `Activity` 类中的生命周期方法（它们是 `protected` 的）相反。当我们想要从布局 XML 文件中填充片段时，必须重写 `onCreateView` 方法来实现。`onCreateView` 方法提供了一个 `LayoutInflater` 参数，使我们能够使用其 `inflate` 方法填充 XML 文件，如表 9.2 所示。其 `ViewGroup` 参数表示片段将要放置的 `ViewGroup`。`Bundle` 参数包含来自片段前一个实例的数据。当片段恢复时，可以读取这些数据。

| 步骤 | 方法 | 调用时机 |
| --- | --- | --- |
| 1a | `void onAttach( Context context )` | 当片段附加到其上下文时。 |
| 2a | `void onCreate( Bundle savedInstanceState )` | 当片段创建时。 |
| 3a | `View onCreateView( LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState )` | 在 `onCreate` 之后；创建并返回与此片段关联的 `View`。 |
| 4a | `void onViewCreated( View view, Bundle savedInstanceState )` | 在 `onCreateView` 之后，但在任何已保存状态恢复到 `View` 之前。 |
| 5a | `void onActivityCreated( Bundle savedInstanceState )` | 当片段的活动已完成执行其自身的 `onCreate` 方法时。 |
| 6a | `void onViewStateRestored( Bundle savedInstanceState )` | 当片段 `View` 层次结构的已保存状态已恢复时（需要 API 级别 17）。 |
| 7a | `void onStart( )` | 当片段对用户可见时。 |
| 8a | `void onResume( )` | 当片段对用户可见，用户可以开始与片段交互时。 |
| 4b | `void onPause( )` | 当活动正在暂停或另一个片段正在修改它时。 |
| 3b | `void onStop( )` | 当片段对用户不再可见时。 |
| 2b | `void onDestroyView( )` | 在 `onStop` 之后；由 `onCreateView` 创建的 `View` 已与此片段分离。 |
| 1b | `void onDestroy( )` | 当片段不再使用时。 |
| 0b | `void onDetach()` | 在片段与其活动分离之前。 |

**表 9-1** `Fragment` 类的生命周期方法

| `View inflate(int resource, ViewGroup root, boolean attachToRoot)` | `Resource` 是要被填充的 XML 资源的 ID。如果 `attachToRoot` 为 `true`，则 `Root` 是可选的 `View`，作为填充布局的父视图。如果 `attachToRoot` 为 `false`，则 `root` 仅用于为 XML 资源中的根视图设置正确的布局参数。 |

**表 9.2** `LayoutInflater` 类中选定的 `inflate` 方法



示例 9.4 展示了`GameControlFragment`类。目前，我们将其保持最小化：它仅在`onCreateView`方法（第 13–18 行）的第 16–17 行填充了`fragment_game_control.xml`文件。我们传递给`inflate`方法的第一个参数是片段的资源 ID`fragment_game_control`。第二个参数是片段所在的容器，即`onCreateView`方法传递的`ViewGroup`类型的`container`。第三个参数是`false`，因为在这种情况下，填充的 XML 文件已经插入到`container`中。指定`true`会创建一个多余的`ViewGroup`层级。

![](img/ch09exa04.jpg)

**示例 9.4**`GameControlFragment`类，Hangman 应用，版本 0

![](img/9781284093650_CH09_FIGF05.jpg)

**图 9.5** Hangman 应用，版本 0，横屏预览

当活动状态恢复时，属于该活动的任何片段都会被重新实例化，并自动调用其默认构造函数。因此，任何片段类都必须有一个默认构造函数（第 10–11 行）。

图 9.5 展示了应用版本 0 在横屏方向下的预览。

我们可以通过在`MainActivity`和`GameControlFragment`类的各个生命周期方法中添加`Log`语句，来检查`Activity`和`Fragment`类的哪些方法会被自动调用以及调用顺序。如果我们将它们添加到这两个类中，当用户启动应用并与应用和设备交互时，我们将看到如图 9.6 所示的输出。它通常显示两件事：

- ▸ 当活动被创建或重新启动时，`Activity`类的方法先执行，然后`Fragment`类的类似方法后执行。
- ▸ 当活动变为非活动状态或被关闭时，`Fragment`类的方法先执行，然后`Activity`类的类似方法后执行。

## 9.4 添加 GUI 组件、样式、字符串和颜色，Hangman 应用版本 1

在应用的版本 1 中，我们用两个 GUI 组件填充屏幕左侧区域（片段），并开始使用模型。

示例 9.5 展示了更新后的`activity_main.xml`文件。我们为屏幕右上角和右下角的`LinearLayout`元素（第 24 行和第 32 行）赋予 ID，以便稍后访问它们来放置片段。我们将硬编码的颜色改为在`colors.xml`文件中定义的颜色（第 27 行和第 35 行），如示例 9.6 所示。

![](img/9781284093650_CH09_FIGF06.jpg)

**图 9.6** 用户与`HangmanV0LifeCycle`应用交互时的输出，包括`Activity`和`Fragment`类的生命周期方法

![](img/ch09exa05.jpg)

**示例 9.5**`activity_main.xml`文件，Hangman 应用，版本 1

![](img/ch09exa06.jpg)

**示例 9.6**`colors.xml`文件，Hangman 应用，版本 1

示例 9.7 展示了更新后的`fragment_game_control.xml`文件。我们在其中放置了两个`LinearLayout`（第 9–14 行，第 16–20 行）：每个都包含一个基本的 GUI 组件（一个按钮和一个标签）。通过在每个布局管理器中放置一个组件，并通过第 9 行和第 16 行的`wrapCenterWeight1`样式为每个布局管理器赋予相同的`android:layout_weight`值`1`，我们使组件均匀分布。`wrapCenterWeight1`样式还设置了`android:layout_width`和`android:layout_height`为`wrap_content`，`android:gravity`为`center`，该样式在`styles.xml`文件中定义（第 11–16 行），如示例 9.9 所示。使用样式简化了布局 XML 文件的编码。

![](img/ch09exa07.jpg)

**示例 9.7**`fragment_game_control.xml`文件，Hangman 应用，版本 1

我们为外部的`LinearLayout`（第 6 行）赋予一个在`colors.xml`中定义的背景颜色。按钮在第 12 行使用`buttonStyle`样式进行样式化，该样式在示例 9.9 的第 31–33 行定义。`ButtonStyle`继承自`textStyle`，后者在示例 9.9 的第 18–23 行定义。

`TextView`元素（第 17–19 行）在第 19 行使用`textStyle`样式进行样式化。`TextView`元素存储用户剩余的猜测次数。我们从模型中检索该值。按钮的文本显示为 PLAY（第 11 行——`strings.xml`文件中`play`字符串的值——示例 9.8 的第 3 行），当用户点击它时触发`play`方法的执行（第 13 行）。

![](img/ch09exa08.jpg)

**示例 9.8**`strings.xml`文件，Hangman 应用，版本 1

![](img/ch09exa09.jpg) ![](img/ch09exa09a.jpg)

**示例 9.9**`styles.xml`文件，Hangman 应用，版本 1

我们将`MainActivity`类（如示例 9.10 所示）保持最小化。它在第 10 行包含一个表示模型的`Hangman`实例变量。由于`onCreate`方法在活动的生命周期中可能被多次调用，我们仅在其之前未被实例化时（即如果为`null`）才实例化它（第 16 行）。我们在第 19 行调用`Hangman`类的`getGuessesLeft`方法，以设置片段中`TextView`的文本。我们在第 18 行使用`findViewById`方法检索该`TextView`。该类还包含`play`方法（第 22–23 行），目前实现为一个空方法（如果不实现它，运行并点击按钮，应用将停止工作）。

![](img/ch09exa10.jpg)

**示例 9.10**`MainActivity`类，Hangman 应用，版本 1

![](img/9781284093650_CH09_FIGF07.jpg)

**图 9.7** Hangman 应用，版本 1，水平方向运行

图 9.7 展示了应用版本 1 在水平方向下的运行情况。

## 9.5 使用布局 XML 文件定义片段并通过代码将片段添加到活动，Hangman 应用版本 2

在版本 2 中，我们在屏幕右上方面板（蓝色背景）中显示片段，展示单词的完成状态，以及一个供用户输入字母的`EditText`。我们在 XML 文件`fragment_game_state.xml`中编码片段，并通过代码创建片段。

此外，为了更好地专注于片段并保持简单，我们仅以水平方向运行应用，方法是在`AndroidManifest.xml`文件的`activity`元素中添加以下行：

```xml
android:screenOrientation="landscape"
```

示例 9.11 展示了`fragment_game_state.xml`文件。它包含一个`TextView`，用于显示单词的完成状态，以及一个`EditText`，用户可以在其中输入字母。我们在第 11 行和第 17 行为这两个元素赋予 ID，以便稍后使用`findViewById`方法检索它们。它们使用`textStyle`和`editTextStyle`进行样式化，这两个样式都在`styles.xml`文件中定义（如示例 9.9 所示）。与左侧面板片段的示例 9.7 类似，我们将每个元素包裹在一个使用`wrapCenterWeight1`样式样式化的`LinearLayout`元素中，以便元素居中并均匀分布。

![](img/ch09exa11.jpg)

### 示例 9.11 `fragment_game_state.xml`文件，猜词游戏应用，版本 2

当用户触摸`Done`键时，我们希望关闭软键盘。为此，我们在第 19 行将继承自`TextView`的`android:imeOptions`属性值设置为`actionDone`。IME 代表输入法编辑器（Input Method Editor），它允许用户输入文本。它不限于键盘——用户也可以通过语音输入文本。属性`android:imeOptions`使我们能够指定要启用的选项。

我们需要在应用启动时显示游戏状态片段。首先需要创建片段并将其添加到活动中，然后设置片段中`TextView`元素内的文本。为此，我们可以调用模型的`currentIncompleteWord`方法。要将片段合并到活动中，需要执行以下步骤：

- 获取此`Activity`的片段管理器引用。
- 创建片段事务。
- 创建片段。
- 让片段事务将片段添加到容器（一个`ViewGroup`）中。
- 提交片段事务。

`FragmentManager` `abstract`类提供了与活动中片段交互的功能。可以通过调用`getFragmentManager`方法（如表 9.3 所示）并传入`Activity`引用来获取当前`Activity`的`FragmentManager`引用。表 9.4 列出了`FragmentManager`类的一些方法。

| 方法 | 描述 |
| --- | --- |
| `FragmentManager getFragmentManager()` | 返回此`Activity`的`FragmentManager`。 |

#### 表 9.3 `Activity`类的`getFragmentManager`方法

| 方法 | 描述 |
| --- | --- |
| `FragmentTransaction beginTransaction()` | 为此片段管理器启动一系列操作。返回一个`FragmentTransaction`。 |
| `Fragment findFragmentById(int id)` | 返回由其 id 标识的`Fragment`。 |
| `Fragment findFragmentByTag(String tag)` | 返回由其标签标识的`Fragment`。 |

#### 表 9.4 `FragmentManager`类的部分方法

因此，我们可以使用以下代码获取当前`Activity`的`FragmentManager`引用：

```java
FragmentManager fragmentManager = getFragmentManager();
```

要为上述`FragmentManager`获取`FragmentTransaction`，我们编写：

```java
FragmentTransaction transaction = fragmentManager.beginTransaction();
```

`FragmentTransaction`类提供了方法（见表 9.5）来执行片段操作，例如向活动添加片段、移除片段、替换片段、隐藏片段、显示片段等。这些方法返回调用它们的`FragmentTransaction`，以便我们可以链式调用方法。还有其他方法，例如定义片段事务执行时的动画或过渡。它是一个`abstract`类，因此我们不能使用构造函数实例化`FragmentTransaction`对象。我们可以使用`FragmentManager`类的`beginTransaction`方法来实例化`FragmentTransaction`对象。

在为某个`Activity`获取名为`transaction`的`FragmentTransaction`后，我们可以使用以下代码将 id 为`game_state`的`GameStateFragment`添加到该`Activity`：

```java
GameStateFragment fragment = new GameStateFragment();
transaction.add(R.id.game_state, fragment);
transaction.commit();
```

在执行片段事务时（例如向活动添加或移除片段），我们可以在调用`commit`方法之前调用`addToBackStack`方法，将其添加到活动的返回栈中。返回栈会跟踪活动中这些片段事务的历史记录，以便用户可以通过按下设备的返回按钮恢复到之前的片段。

| 方法 | 描述 |
| --- | --- |
| `FragmentTransaction add(int containerViewId, Fragment fragment, String tag)` | 向活动添加一个片段。`containerViewId`是片段将放置的容器的资源 id；`fragment`是要添加的片段。`tag`是片段的可选标签名称。之后可以通过片段管理器使用`findFragmentByTag`方法检索添加的片段。返回调用此方法的`FragmentTransaction`引用；因此可以链式调用方法。 |
| `FragmentTransaction add(int containerViewId, Fragment fragment)` | 调用上述方法，`tag`参数为`null`。 |
| `FragmentTransaction add(Fragment fragment, String tag)` | 调用上述方法，资源 id 参数为 0。 |
| `FragmentTransaction hide(Fragment fragment)` | 隐藏片段（即隐藏其`View`）。 |
| `FragmentTransaction show(Fragment fragment)` | 显示片段（即如果之前被隐藏，则显示其`View`——默认情况下片段是显示的）。 |
| `FragmentTransaction remove(Fragment fragment)` | 从活动中移除片段。 |
| `FragmentTransaction replace(int containerViewId, Fragment fragment, String tag)` | 类似于第一个`add`方法，但替换容器中 id 为`containerViewId`的现有片段。 |
| `FragmentTransaction replace(int containerViewId, Fragment fragment)` | 调用上述方法，`tag`参数为`null`。 |
| `int commit()` | 安排提交该片段事务。 |
| `FragmentTransaction addToBackStack(String name)` | 将此事务添加到活动的返回栈中；`name`是可选的，用于存储该返回栈状态的名称。 |

#### 表 9.5 `FragmentTransaction`类的部分方法

示例 9.12 展示了更新后的`MainActivity`类。当应用启动时，`onCreate`方法执行，我们创建片段并将其附加到活动。在第 23 行，我们通过调用`Activity`类的`getFragmentManager`方法获取此活动的片段管理器引用。我们只希望在尚未创建`GameStateFragment`时创建它并添加到活动。在第 24 行使用`findFragmentById`方法，我们检查此活动中是否已存在 id 为`game_state`的片段。如果存在，则不执行任何操作。如果不存在，则在第 25–28 行创建一个并添加到活动。

![](img/ch09exa12.jpg)

### 示例 9.12 `MainActivity`类，猜词游戏应用，版本 2

在第 25 行，使用`FragmentManager`引用，我们获取一个`FragmentTransaction`引用`transaction`。在第 26 行，我们定义并实例化一个`GameStateFragment`引用`fragment`。在第 27 行，我们将`fragment`添加到此`Activity`，将其放置在资源 id 为`game_state`的`ViewGroup`（此处为`LinearLayout`）中。最后，我们在第 28 行提交片段事务。此时，我们仍需要将谜题的文本放入刚刚添加到活动的谜题片段的`TextView`中。为此，我们首先需要访问片段的`View`，并使用`findViewById`方法，传入`TextView`的 id 作为参数。然而，此时片段的`View`为`null`，因此尝试使用它会导致`NullPointerException`，使应用崩溃。因此，我们在`GameStateFragment`类内部执行此操作。因此，在`GameStateFragment`类中，我们需要访问猜词游戏中当前不完整单词的值。为此，我们在`MainActivity`类中提供了`getGame`方法（第 32–34 行）。从`GameStateFragment`类中，我们可以通过调用`getActivity`方法（见表 9.6）来访问活动，该方法继承自`Fragment`类。有了`MainActivity`引用，我们可以通过调用`getGame`访问游戏，然后按如下方式访问不完整单词：

| 方法 | 描述 |
| --- | --- |
| `Activity getActivity()` | 返回此片段所属的活动。 |

#### 表 9.6 `Fragment`类的`getActivity`方法

| `View getView()` | 返回该 fragment 的根`View`。 |



# 表 9.6：`Fragment` 类的 `getActivity` 和 `getView` 方法

```java
MainActivity fragmentActivity = ( MainActivity ) getActivity( );
String currentWord = fragmentActivity.getGame( ).currentIncompleteWord( );
```

示例 9.13 展示了 `GameStateFragment` 类。由于它继承自 `Fragment`，我们在第 12–13 行提供了一个强制性的默认构造函数。我们在第 18–19 行的 `onCreateView` 方法中加载了 `fragment_game_state.xml` 文件。

当 fragment 事务在示例 9.12 的第 28 行提交时，构造函数、`onAttach`、`onCreate`、`onCreateView`、`onActivityCreated` 和 `onStart` 方法会按顺序调用。当 `onStart` 方法（第 22–30 行）执行时，fragment 的 `View` 及其内部的 `TextView` 已经被实例化。因此，我们可以在此时设置 `TextView` 中的文本。

我们在第 24 行使用从 `Fragment` 类继承的 `getView` 方法（如表 9.6 所示）获取 fragment 的 `View` 引用。借助它，我们可以调用 `findViewById` 方法来访问其中已分配 id 的任何 `View`。在第 25–26 行，我们调用该方法，并将 id 为 `state_of_game` 的 `TextView` 赋值给 `gameStateTV`。

我们在第 27 行获取该 fragment 的父 `Activity` 引用，并将其转换为 `MainActivity`。我们链式调用 `getGame` 和 `currentIncompleteWord` 方法，以获取游戏的不完整单词，并在第 28–29 行将结果值赋给 `gameStateTV` 的文本。

![](img/ch09exa13.jpg)

**示例 9.13** `GameStateFragment` 类，Hangman 应用，版本 2

![](img/9781284093650_CH09_FIGF08.jpg)

**图 9.8** Hangman 应用，版本 2，水平方向运行，用户输入字母并点击软键盘上的 Done（或 Check）按钮后

图 9.8 展示了用户在软键盘上输入字母 `U` 并点击 Done 按钮后，应用在模拟器中运行的情况。

## 9.6 通过代码定义和向 Activity 添加 Fragment：Hangman 应用，版本 3

在版本 3 中，我们在屏幕右下方面板（绿色背景）中显示 fragment，该 fragment 在 `TextView` 中显示游戏结果的消息。这次，我们不使用 XML 文件来定义 fragment，而是完全通过代码定义和创建它。

定义 fragment 的图形用户界面（GUI）类似于通过代码定义 `View`，而不是使用 XML 文件。我们在 `GameResultFragment` 类中完成此操作。创建 fragment 与创建游戏状态 fragment 相同。它在 `MainActivity` 类中进行。

示例 9.14 展示了更新后的 `MainActivity` 类。它与示例 9.12 中显示的先前版本非常相似。我们在 id 为 `game_result` 的 `LinearLayout` 中添加了一个 `GameResultFragment`（第 31–36 行）。

在 `GameResultFragment` 类中，我们通过代码定义 fragment。该 fragment 只包含一个 `TextView`。此外，我们需要在游戏结束时访问该 `TextView` 以设置其文本。我们不在创建 `TextView` 时为其分配 id，而是将其声明为实例变量，以便在 `GameResultFragment` 类内部直接引用它（示例 9.15 的第 12 行）。

`onCreateView` 方法（第 14–20 行）在第 17 行调用 `setUpFragmentGui` 方法，以创建该 fragment 的 GUI。它返回其 `super` 方法在第 18–19 行返回的 `View`。`setUpFragmentGui` 方法在第 22–28 行编码。

由于 `onCreateView` 可能在 fragment 的生命周期中被多次调用，因此我们也可以预期 `setUpFragmentGui` 会被多次调用。因此，我们只希望在 `gameResultTV` 为 `null`（第 23 行）时，实例化 `gameResultTV`（第 24 行）并将其添加到作为 fragment 根 `View` 的 `ViewGroup`（第 26 行）中一次。我们在第 25 行将 `gameResultTV` 内的文本居中。

![](img/ch09exa14.jpg)

**示例 9.14** `MainActivity` 类，Hangman 应用，版本 3

![](img/ch09exa15.jpg)

**示例 9.15** `GameResultFragment` 类，Hangman 应用，版本 3

在 `onStart` 方法（第 30–33 行）中，该方法在 `onCreateView` 和 `onActivityCreated` 之后自动调用，我们将 `gameResultTV` 内的文本硬编码为“GOOD LUCK”（第 32 行）。

我们需要将 `GameResultFragment` 的 `TextView` 在其父 `LinearLayout` 中居中。在 `activity_main.xml` 文件中，我们向最后一个 `LinearLayout` 元素（id 为 `game_result`，位于右下方面板）添加以下属性-值对：

```xml
android:gravity="center"
```

![](img/9781284093650_CH09_FIGF09.jpg)

**图 9.9** Hangman 应用，版本 3，水平方向运行

图 9.9 展示了应用在模拟器中运行的情况。现在所有三个 fragment 都已存在：

- 左侧面板（游戏控制）fragment（红色）使用 XML 定义和创建。
- 右上方面板（游戏状态）fragment（蓝色）在 XML 中定义，并通过代码创建。
- 右下方面板（游戏结果）fragment（绿色）通过代码定义和创建。

## 9.7 Fragment 与其 Activity 之间的通信：启用游戏，Hangman 应用，版本 4

我们现在创建了一个包含三个 fragment 的 Activity，这些 fragment 以不同方式定义和创建。在版本 4 中，我们通过处理用户输入的字母并允许用户玩游戏来完成应用。我们还说明了 fragment 在处理事件时如何与其 Activity 通信。

用户在游戏状态 fragment 中输入一个字母，然后点击左侧面板上的 PLAY 按钮，这会触发 `MainActivity` 类中 `play` 方法的执行。为了启用游戏，我们执行以下操作：

- 捕获用户输入的字母。
- 调用 `Hangman` 的 `guess` 方法。
- 更新左侧面板 `TextView` 中剩余的猜测次数。
- 更新右上方面板 `TextView` 中的不完整单词。
- 清空 `EditText`。
- 如果游戏结束，更新右下方面板 `TextView` 中的消息，并清空 `EditText` 中的提示。

示例 9.16 展示了 `play` 方法。我们在第 46 行使用 id 获取 `EditText`，并将其赋值给变量 `input`。在第 47 行，我们获取 `input` 的 `Editable` 引用。如果它不为 `null` 且至少包含一个字符（第 48 行），我们将第一个字符作为用户的输入进行处理。否则，不执行任何操作。

![](img/ch09exa16.jpg)

**示例 9.16** `MainActivity` 类的 `play` 方法，Hangman 应用，版本 4

在第 49–53 行，我们进行游戏并更新剩余的猜测次数。由于我们在 `fragment_game_control.xml` 文件中为显示剩余猜测次数的 `TextView` 分配了 id（`status`），因此我们在第 52 行使用 `findViewById` 方法获取它。我们在第 53 行调用 `game` 的 `getGuessesLeft` 方法以获取剩余猜测次数，并将其显示在 `TextView` 中。

在第 55–62 行，我们更新不完整单词的状态。我们首先在第 56–58 行获取 `GameStateFragment` 的引用，然后在第 59 行获取 fragment 的 `View` 引用。借助它，我们在第 60–61 行调用 `findViewById`，以获取 id 为 `state_of_game` 的 `TextView` 的引用。我们在第 62 行调用 `Hangman` 的 `currentIncompleteWord` 方法来设置该 `TextView` 的文本。在第 64–65 行，我们清空 `EditText`。

然后我们在第 67 行检查游戏是否结束。如果未结束，我们不做任何操作。如果已结束（第 68 行），我们清除 `EditText` 中的提示（第 78–79 行），并告知用户游戏结果。为此，我们需要访问 `GameResultFragment` 内部的 `TextView`；然而，该 `TextView` 没有 id。因此，为了访问它，我们通过 `FragmentManager` 获取包含它的 `GameResultFragment` 的引用（第 69–70 行），并调用 `GameResultFragment` 类的新方法 `setResult`（第 72–76 行）。

示例 9.17 展示了 `GameResultFragment` 类的 `setResult` 方法。该类的其余部分保持不变。它设置了 `gameResultTV` 实例变量的文本。

![](img/ch09exa17.jpg)

**示例 9.17** `GameResultFragment` 类的 `setResult` 方法，猜词游戏应用，版本 4

图 9.1（位于本章开头）展示了游戏进行到某个时刻的应用运行界面。图 9.10 展示了用户获胜后的应用运行界面。之前显示提示或字母的 `TextView` 不再可见，因为其内容为空，且其 `android:layout_width` 和 `android:layout_height` 属性设置为 `wrap_content`。

![](img/9781284093650_CH09_FIGF10.jpg)

**图 9.10** 猜词游戏应用，版本 4，用户获胜后以横向模式运行

## 9.8 使用不可见片段，猜词游戏，应用版本 5

我们还可以使用一个在应用后台执行某些工作、没有任何视觉表示的片段。为此，我们使用 `FragmentTransaction` 类的 `add` 方法，该方法没有 `View` id 参数。如果我们希望稍后能够检索该片段，应提供一个标签名称。

这样的片段可以在用户与应用交互的同时，在应用后台执行某些工作。例如，它可以从文件、数据库、远程 URL 检索数据，或者使用设备的 GPS 获取实时位置数据。

为了演示如何使用这样的片段，我们尽量简化示例。我们的片段是硬编码的，并包含 `warning` 方法。当用户只剩一次猜测机会时，我们会向用户发出警告，并显示 `warning` 方法返回的 `String`。该信息通常来自模型，但为了尽可能简单，我们在此类中将其硬编码。

示例 9.18 展示了 `BackgroundFragment` 类。由于该片段不可见，因此不会调用 `onCreateView` 方法。所以我们没有编写它。在第 10–12 行，我们编写了 `warning` 方法，该方法从 `MainActivity` 类中调用。

![](img/ch09exa18.jpg)

**示例 9.18** `BackgroundFragment` 类，猜词游戏应用，版本 5

示例 9.19 展示了更新后的 `MainActivity` 类的部分内容。我们在 `onCreate` 方法中（第 40–45 行）创建了一个不可见的 `BackgroundFragment`，无需等待用户与应用交互。这种策略可用于需要从外部来源获取数据的应用。

在第 43 行，我们使用 `FragmentTransaction` 类的 `add` 方法，参数为一个 `Fragment` 和一个 `String`。该 `String` 代表片段的标签名称，稍后我们可以通过 `FragmentManager` 类的 `findFragmentByTag` 方法，根据其标签名称 `background` 检索该片段。

我们在 `play` 方法中使用该片段（第 52–99 行）。如果用户只剩一次猜测机会（第 75 行），我们在 `GameResultFragment` 的 `TextView` 中显示警告。我们在第 76–77 行根据标签检索 `BackgroundFragment`，在第 78–79 行根据 id 检索 `GameResultFragment`。然后我们调用 `GameResultFragment` 的 `setResult`，传入通过调用 `BackgroundFragment` 的 `warning` 方法获取的警告（第 81 行）。

![](img/ch09exa19.jpg)

**示例 9.19** `MainActivity` 类，猜词游戏应用，版本 5

图 9.11 展示了应用在模拟器中运行的情况。用户只剩一次猜测机会。

![](img/9781284093650_CH09_FIGF11.jpg)

**图 9.11** 猜词游戏应用，版本 5，以横向模式运行——用户只剩一次猜测机会

## 9.9 使片段可复用，猜词游戏，应用版本 6

应用的版本 5 可以工作，但 `GameStateFragment` 类并非真正可复用。例如，在示例 9.13 的第 27 行，`GameStateFragment` 类内部使用了 `MainActivity` 引用，并在第 28 行调用了 `getGame`，这假设 `MainActivity` 类存在并包含 `getGame` 方法。

示例 9.20 展示了一个更好的实现，使 `GameStateFragment` 类更具可复用性。在片段类内部，我们使用了一个内部接口，命名为 `Callbacks`（第 15–17 行），并将片段类内部所有使用 `MainActivity` 引用的方法调用，通过该接口转移到 `MainActivity` 类中。

在片段类内部，每当我们调用 `MainActivity` 方法时，我们向 `Callbacks` 接口添加一个方法，并从片段类中调用该方法。`MainActivity` 类实现了该接口，因此必须重写该方法。这样，我们有效地将 `MainActivity` 的方法调用从片段类转移到了 `MainActivity` 类中。

![](img/ch09exa20.jpg) ![](img/ch09exa20a.jpg)

**示例 9.20** 可复用的 `GameStateFragment` 类，猜词游戏应用，版本 6

另一个可复用性问题是，`getGame` 方法返回一个 `Hangman` 引用。因此，由于 `getGame` 位于 `GameStateFragment` 类内部的 `Callbacks` 接口中，我们的 `GameStateFragment` 类只能与 `Hangman` 类复用。

为了解决这个问题，我们创建了一个接口，命名为 `WordGame`，并让 `getGame` 返回一个 `WordGame` 引用。`WordGame` 接口只有一个方法 `currentIncompleteWord`。这是必要的，因为我们在 `GameStateFragment` 类内部使用 `getGame` 返回的 `WordGame` 引用来调用该方法。

因此，`GameStateFragment` 类现在可以与任何实现了 `Callbacks` 接口的 Activity 以及任何实现了 `WordGame` 接口的类复用，这两个接口都非常简单且通用。在此应用中，我们修改了 `Hangman`，使其实现 `WordGame`。

以下是 `GameStateFragment` 类中方法转移机制的实现方式。

**之前：在 `GameStateFragment` 内部（旧实现），来自示例 9.13：**

![](img/ch09unexa01.jpg)

**之后：在 `GameStateFragment` 内部（新实现），来自示例 9.20：**

![](img/ch09unexa02.jpg)

第 40 行对 `getGameFromActivity` 的调用，会触发由第 13 行声明并初始化的 `mCallbacks` 实例变量，调用 `Callbacks` 接口（在第 16 行声明）的 `getGame` 方法，该方法将在实现了 `Callbacks` 接口（因此实现了 `getGame`）的类中执行。

在第 19–23 行，我们声明并实例化了 `sDummyCallbacks`，这是一个实现了 `Callbacks` 接口的匿名类对象。该匿名类在第 20–22 行重写了 `getGame` 方法，返回 `null`；`sDummyCallbacks` 在第 13 行被赋值给类型为 `Callbacks` 的实例变量 `mCallbacks`。

`mCallbacks` 实例变量旨在作为此 fragment 所属 activity 的引用。从 `Fragment` 类继承的 `onAttach` 方法在第 44–51 行被重写。当此 fragment 附加到 activity 时，会调用此方法。

此外，当调用该方法时，我们期望其参数 `context` 是实现 `Callbacks` 接口的 `Context` 超类（很可能是 `Activity` 的超类）的实例。如果不是（第 46 行），我们在第 47–48 行抛出 `IllegalStateException`。如果是，则将 `context` 参数类型转换为 `Callbacks` 并赋值给 `mCallbacks`（第 50 行）。



在这个新实现中，没有提及`MainActivity`类，也没有提及`MainActivity`类中名为`getGame`的方法。唯一的要求是，`MainActivity`类或任何与`GameStateFragment`类一起使用的`Activity`类，都实现`Callbacks`接口。这反过来强制`MainActivity`或任何实现`Callbacks`接口的类重写`getGame`方法。请注意，在此示例中，`Callbacks`接口中只有一个方法，但更一般地，可能有多个方法。

从`Fragment`类继承的`onDetach`方法在第 53–56 行被重写。当此 fragment 与其 activity 分离时，会调用该方法。它在第 55 行将默认的`Callbacks`对象`sDummyCallbacks`重新赋值给`mCallbacks`。

示例 9.21 显示了更新后的`MainActivity`类的类头，该类现在实现了`GameStateFragment`的内部接口`Callbacks`。与示例 9.19 相比，没有其他变化：`getGame`方法之前已经实现，现在仍然相同，但它现在重写了`Callbacks`接口的`getGame`方法。

![](img/ch09exa21.jpg)

示例 9.21 `MainActivity`类的类头，Hangman 应用，版本 6

示例 9.22 显示了`WordGame`接口，该接口声明了`currentIncompleteWord`方法（第 4 行）。

![](img/ch09exa22.jpg)

示例 9.22 `WordGame`接口，Hangman 应用，版本 6

示例 9.23 显示了更新后的`Hangman`类的类头，该类现在实现了`WordGame`接口。与示例 9.1 相比，没有其他变化：`currentIncompleteWord`方法之前已经实现，现在仍然相同，但它现在重写了`WordGame`接口的`currentIncompleteWord`方法。

![](img/ch09exa23.jpg)

示例 9.23 `Hangman`类的类头，Hangman 应用，版本 6

请注意，我们将`Callbacks`实现为`GameStateFragment`的内部接口，而将`WordGame`实现为单独的接口。两者都可以实现为内部接口或单独的接口。

## 9.10 改进 GUI：直接处理键盘输入，Hangman，应用版本 7

版本 6 可以工作，但每次都必须单击 PLAY 按钮很烦人。在版本 7 中，当用户关闭键盘时，我们立即启用游戏。我们可以删除 PLAY 按钮，或将其转换为“再玩一局”按钮，你可以在练习中完成。

`EditText`位于游戏状态 fragment 内部，因此版本 7 的事件处理在该 fragment 中进行。`OnEditorActionListener`是`TextView`类的`public static`内部接口，提供了在`EditText`内处理按键事件的功能。表 9.7 列出了其唯一的方法`onEditorAction`。

与往常一样，为了设置事件处理，我们执行以下操作：

1. 编写事件处理程序（一个扩展监听器接口的类）。
2. 实例化该类的对象。
3. 将该对象监听器注册到一个或多个 GUI 组件上。

示例 9.24 显示了更新后的`GameStateFragment`类。在第 79–94 行，我们定义了`private`类`OnEditorHandler`，它实现了`TextView.OnEditorActionListener`接口。它在第 80–93 行重写了其唯一的方法`onEditorAction`。它执行以下操作：

| 方法 | 描述 |
| --- | --- |
| `boolean onEditorAction( TextView view, int keyCode, KeyEvent event )` | `view`是被点击的`TextView`；`keyCode`是标识所按键的整数；`event`是按键事件。 |

表 9.7 `TextView.OnEditorActionListener`接口的`onEditorAction`方法

![](img/ch09exa24.jpg) ![](img/ch09exa24a.jpg)

示例 9.24 `GameStateFragment`类，Hangman 应用，版本 7

- 隐藏键盘（第 82–87 行）。
- 进行游戏（第 89–90 行）。

由于我们在`MainActivity`类中已经有一个`play`方法，我们可以重用其代码。现有的`play`方法接受一个`View`参数，预期是一个`Button`，但该方法实际上并未使用该参数。我们可以调用它并传递`null`，但将`null`传递给另一个类的方法并不是好做法，因为理论上（通常）它可能使用该参数来调用方法。因此，我们在`MainActivity`类中创建了一个额外的`play`方法（参见示例 9.25），该方法不接受参数，并且执行与现有`play`方法完全相同的操作（我们可以将其保留为无操作方法——如果我们选择删除它，还需要删除`fragment_game_control.xml`文件中的`android:onClick`属性）。我们使用与版本 6 相同的策略，通过`Callbacks`接口的`play`方法（在第 20 行声明）将调用转移到`MainActivity`的`play`方法，并通过 fragment 的`play`方法（第 71–73 行）调用它。因此，第 90 行对 fragment 的`play`方法的调用会触发对`Callbacks`的`play`方法的调用。通过这种方式，我们保持了 fragment 类的可重用性（与实现`Callbacks`接口的类一起使用）。

为了通过代码关闭键盘，我们可以使用`InputMethodManager`引用。`InputMethodManager`类管理应用程序与其当前输入法之间的交互。该类没有构造函数，但我们可以通过使用`Activity`引用（由于`Activity`继承自`Context`，因此它是`Context`引用）调用`Context`类的`getSystemService`来获取`InputMethodManager`引用。

`getSystemService`方法具有以下 API：

```
Object getSystemService( String nameOfService )
```

其`String`参数表示一个服务，表 9.8 列出了一些可能的值。根据指定的服务，它返回该服务的管理器对象引用。例如，如果指定`LOCATION_SERVICE`，它将返回一个`LocationManager`引用，我们可以使用它从设备的 GPS 系统收集位置数据。如果指定`WIFI_SERVICE`，它将返回一个`WifiManager`引用，我们可以使用它访问有关设备 Wi-Fi 连接的数据。由于该方法返回一个通用的`Object`，我们需要将返回的对象引用类型转换为预期的类型。我们想要获取一个`InputMethodManager`引用，因此我们传递参数`Context.INPUT_METHOD_SERVICE`，并将结果对象引用转换为`InputMethodManager`，如下所示（如第 83–84 行）：

```
InputMethodManager inputManager = ( InputMethodManager )
getActivity( ).getSystemService( Context.INPUT_METHOD_SERVICE );
```

要关闭键盘，我们使用`InputMethodManager`类的`hideSoftInputFromWindow`方法之一，如表 9.9 所示。第一个参数的类型是`IBinder`，这是一个封装了可远程对象的接口。可远程对象是指可以通过代理在其上下文之外访问的对象。我们需要向`hideSoftInputFromWindow`传递一个`IBinder`引用，该引用代表当前`View`（此处为`EditText`）所附加到的窗口。我们使用当前`Activity`对象调用`Activity`类的`getCurrentFocus`方法，该方法返回当前窗口中拥有焦点的`View`。然后利用该`View`调用`View`类的`getWindowToken`方法，该方法返回一个唯一令牌，用于标识此`View`所附加的窗口。在第 86 行，我们通过以下表达式将这两个方法调用串联起来：

```
getActivity( ).getCurrentFocus( ).getWindowToken( )
```

| 字符串常量 | 字符串值 | `getSystemService`返回类型 |
| --- | --- | --- |
| `POWER_SERVICE` | `power` | `PowerManager` |
| `LOCATION_SERVICE` | `location` | `LocationManager` |
| `WIFI_SERVICE` | `wifi` | `WifiManager` |
| `DOWNLOAD_SERVICE` | `download` | `DownloadManager` |
| `INPUT_METHOD_SERVICE` | `input_method` | `InputMethodManager` |

表 9.8 选定的`String`常量及其值，以及在使用这些常量作为`Context`类的`getSystemService`方法参数时对应的返回类型

| 方法 | 描述 |
| --- | --- |
| `boolean hideSoftInputFromWindow( IBinder token, int flags )` | `token`是发起请求的窗口的令牌，由`View`类的`getWindowToken`方法返回；`flags`指定隐藏软输入时的附加条件。 |

表 9.9 `InputMethodManager`类中选定的`hideSoftInputFromWindow`方法

表 9.10 展示了`InputMethodManager`类中两个可用作`hideSoftInputFromWindow`方法第二个参数的常量。由于用户在尝试输入时会显式打开键盘，因此在这种情况下我们不应使用`HIDE_IMPLICIT_ONLY`常量。我们使用`HIDE_NOT_ALWAYS`，因此第 87 行方法调用的第二个参数为：

```
InputMethodManager.HIDE_NOT_ALWAYS
```

当我们运行应用时，一旦键盘关闭，播放就会立即开始。我们不再需要点击 PLAY 按钮。

| 常量 | 值 | 含义 |
| --- | --- | --- |
| `HIDE_IMPLICIT_ONLY` | 1 | 仅当软输入窗口不是由用户显式打开时才应隐藏。 |
| `HIDE_NOT_ALWAYS` | 2 | 软输入窗口通常应被隐藏，除非它最初是由代码强制打开的。 |

表 9.10 `InputMethodManager`类中选定的`int`常量，用作`hideSoftInputFromWindow`的第二个参数

![](img/ch09exa25.jpg)

示例 9.25 `MainActivity`类中的更改，Hangman 应用，版本 7

## 章节总结

- 片段（Fragment）在 API 级别 11 中被引入，以更好地支持平板电脑等大屏幕设备。
- 片段是活动的一部分，有助于管理屏幕的一部分。我们可以将片段视为活动中的迷你活动。
- 一个活动中可以包含多个片段。
- 片段可以拥有用户界面，也可以仅在活动的后台执行某些工作。
- 片段拥有自己的生命周期方法，但依赖于其所属活动的运行。
- 活动可以使用`getFragmentManager`方法访问其片段管理器，从而访问和管理其片段。
- 片段可以使用`getActivity`方法访问其所属活动。
- 片段可以通过仅使用 XML、仅使用代码或两者结合的方式定义、创建并添加到活动中。
- 在创建片段并将其添加到活动时，我们使用`FragmentTransaction`类。添加片段时，我们可以通过 ID、标签或两者来标识它。
- 片段管理器可以通过 ID 或标签查找片段。
- 片段可以在多个活动中重复使用。
- 片段类的编码应使其可重用，并且不依赖于特定的活动类。我们可以通过在片段类内部使用内部接口来实现这一点。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. 片段是在哪个 API 级别引入的？
   - 2
   - 8
   - 11
   - 13

2. `Fragment`的直接超类是？
   - `Content`
   - `Activity`
   - `Object`
   - `FragmentActivity`

3. 一个活动中可以有多少个片段？
   - 0
   - 仅 1 个
   - 0 个或多个

4. 以下哪个方法不是片段的生命周期方法？
   - `onStart`
   - `onCreate`
   - `onRestart`
   - `onStop`

5. 片段可以使用哪个方法来访问其所属活动？
   - `activity`
   - `getActivity`
   - `getFragment`
   - `findActivity`

6. 活动可以使用哪个类来访问其片段？
   - `FragmentTransaction`
   - `Activity`
   - `FragmentManager`
   - `Manager`

7. `FragmentTransaction`类的哪个方法用于将片段添加到活动？
   - `add`
   - `addFragment`
   - `insert`
   - `insertFragment`

8. 活动可以通过什么方式检索其某个片段？
   - 仅标签
   - 仅 ID
   - 标签或 ID
   - 无法检索

9. 我们可以通过将片段类中由其活动调用的所有方法转移到活动类中，从而使片段类可重用，这通过什么实现？
   - 内部类
   - 接口
   - 不可能实现

### 补全代码

10. 在活动类内部，获取片段管理器。

11. 在活动类内部，添加一个类型为`MyFragment`的片段，并将其放置在一个 ID 为`my_id`的`ViewGroup`元素中。

```
// fm 是一个 FragmentManager 引用
FragmentTransaction transaction = fm.beginTransaction( );
// 你的代码写在这里
```

12. 在活动类内部，添加一个类型为`MyFragment`的片段，并将其放置在一个 ID 为`my_id`的`ViewGroup`元素中。为其指定标签`my_tag`。

```
// fm 是一个 FragmentManager 引用
FragmentTransaction transaction = fm.beginTransaction( );
// 你的代码写在这里
```

13. 在活动类内部，添加一个类型为`MyFragment`且没有用户界面的片段。为其指定标签`my_tag`。

```
// fm 是一个 FragmentManager 引用
FragmentTransaction transaction = fm.beginTransaction( );
// 你的代码写在这里
```

14. 在片段类内部，编写代码，使片段从`my_fragment.xml`文件进行填充。

```
public View onCreateView( LayoutInflater inflater, ViewGroup
      container, Bundle savedInstanceState ) {
  // 你的代码写在这里
}
```

15. 在片段类内部，编写代码以获取该片段所属的活动。假设活动类型为`MyActivity`。

```
// 你的代码写在这里
```

16. 以下片段类不可重用。请修改使其可重用。

```
package com.you.myapp;
import android.app.Fragment;
public class MyFragment extends Fragment {
  public MyFragment( ) {
  }
  public void onStart( ) {
    super.onStart( );
    MyActivity activity = ( MyActivity ) getActivity( );
    activity.update( );
  }
}
// 你的代码写在这里
```

### 编写一个应用

17. 编写一个包含一个活动并使用两个片段的小型应用，如下所示：

![](img/9781284093650_CH09_UNNUN01.jpg)

18. 编写一个包含一个活动并使用三个片段的小型应用，如下所示：



![](img/9781284093650_CH09_UNNUN02.jpg)

## 19. 使用四个片段编写小型应用

编写一个包含一个活动并使用四个片段的小型应用，如下所示：

![](img/9781284093650_CH09_UNNUN03.jpg)

## 20. 使用两个片段实现交通灯

编写一个包含一个`Activity`的应用，使用两个`Fragment`（一个在左，一个在右），具体要求如下：

- 左侧`Fragment`包含一个按钮。
- 右侧`Fragment`包含一个模拟交通灯的标签，初始时为红色。
- 当用户点击按钮时，标签变为绿色。
- 再次点击按钮，标签变为黄色。
- 再次点击按钮，标签变回红色，以此类推。
- 尽管功能简单，但应用应包含一个`Model`。

## 21. 使用多个片段实现动态布局

编写一个包含一个`Activity`的应用，使用多个`Fragment`（一个在上方，一个或多个在下方），具体要求如下：

- 上方`Fragment`占据屏幕的四分之一，包含三个单选按钮，分别显示 1、2 和 3。
- 当用户选择其中一个时，屏幕底部显示对应数量的`Fragment`（每个使用不同颜色）。
- 这些`Fragment`应占据相同的空间。例如，如果用户点击显示 2 的单选按钮，则屏幕底部显示两个高度相等的`Fragment`。

## 22. 使用两个片段实现手电筒

编写一个包含一个`Activity`的应用，使用两个`Fragment`（一个在上方，一个在下方），具体要求如下：

- 应用模拟一个手电筒。
- 上方`Fragment`占据屏幕的 20%，包含一个开关（可使用`Switch`类）。
- 下方`Fragment`占据屏幕的 80%，初始为黑色。
- 当用户打开开关时，下方`Fragment`变为黄色。
- 当用户关闭开关时，下方`Fragment`恢复为黑色。
- 尽管功能简单，但应用应包含一个`Model`。

## 23. 使用两个片段实现调光器

编写一个包含一个`Activity`的应用，使用两个`Fragment`（一个在上方，一个在下方），具体要求如下：

- 应用模拟一个调光器。
- 上方`Fragment`占据屏幕的 20%，包含一个滑块（可使用`SeekBar`类）。
- 下方`Fragment`占据屏幕的 80%，初始为黄色。
- 当用户移动滑块时，黄色逐渐变淡。
- 可假设调光器滑块控制黄色的透明度。
- 尽管功能简单，但应用应包含一个`Model`。

## 24. 使用两个片段实现交通灯

编写一个包含一个`Activity`的应用，使用两个`Fragment`（一个在左，一个在右），具体要求如下：

- 应用模拟一个交通灯。
- 左侧`Fragment`包含一个按钮。
- 右侧`Fragment`包含三个标签，初始时顶部标签为红色，其余标签透明。
- 当用户点击按钮时，顶部标签变为透明，底部标签变为绿色。
- 再次点击按钮，底部标签变为透明，中间标签变为黄色。
- 再次点击按钮，中间标签变为透明，顶部标签变回红色，以此类推。
- 尽管功能简单，但应用应包含一个`Model`。

## 25. 使用两个片段实现井字棋游戏

编写一个包含一个`Activity`的应用，使用两个`Fragment`（一个在上方，一个在下方），具体要求如下：

- 上方`Fragment`占据屏幕的四分之一，包含一个按钮。
- 下方`Fragment`占据屏幕的四分之三。
- 当用户点击按钮时，下方`Fragment`内显示一个井字棋游戏，并允许玩家操作。
- 应用应包含一个井字棋游戏的`Model`。

## 26. 使用两个片段实现猜数字游戏

编写一个包含一个`Activity`的应用，使用两个`Fragment`（一个在上方占据 75% 空间，一个在下方占据 25% 空间），具体要求如下：

- 应用生成一个 1 到 5 之间的随机数，用户需要猜出这个数。
- 下方`Fragment`显示一个`EditText`，提示用户输入数字。
- 上方`Fragment`向用户显示反馈信息（例如“你赢了”或“你输了”）。
- 尽管功能简单，但应用应包含一个`Model`。

## 27. 为猜数字游戏增加不可见片段

编写与练习 26 相同的应用，但增加第三个`Fragment`，该`Fragment`不可见：它提供生成随机数的功能。

## 28. 改进本章示例应用

编写一个改进本章示例应用的应用。在左侧面板中，增加一个包含按钮的`Fragment`，以便用户点击后可以开始另一个游戏。

## 29. 使用文件存储候选单词

编写与练习 28 相同的应用，但增加一个文件，该文件存储大量（1000 个或更多）候选单词。`Hangman`构造函数应从文件中随机选取一个单词。增加一个不可见的`Fragment`来实例化`Hangman`对象，并使用所选单词开始游戏。

# 第十章：使用库及其 API：语音识别与地图

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

Android 框架为应用开发者提供了一些强大的库。在本章中，我们将学习如何使用其中一些库。我们将探索语音识别和地图相关的库。我们将构建一个包含两个`Activity`的简单应用。第一个`Activity`要求用户说出一个地点，并将其与地点列表进行比较。如果匹配成功，第二个`Activity`将显示带有该地点标注的地图。

## 10.1 语音识别

为了测试涉及语音识别的应用，我们需要一台真实的设备——模拟器无法识别语音。此外，某些设备可能不具备语音识别功能，因此我们应检测这一点。

当用户说出一个单词时，语音识别器会返回该单词的可能匹配列表。然后我们可以处理该列表。我们的代码可以限制返回列表的内容，例如，我们可以指定返回项的最大数量、它们的置信度等。

图 10.1 展示了我们的应用版本 0，它使用标准语音识别用户界面在模拟器中运行。

![](img/9781284093650_CH10_FIGF01.jpg)

图 10.1 “显示地图”应用版本 0，在平板中运行，等待用户说话

### `RecognizerIntent`类的部分常量

| 常量 | 描述 |
| --- | --- |
| `ACTION_WEB_SEARCH` | 用于启动一个使用语音进行网络搜索的`Activity`。 |
| `ACTION_RECOGNIZE_SPEECH` | 用于启动一个要求用户说话的`Activity`。 |
| `EXTRA_MAX_RESULTS` | 指定返回结果最大数量的键。 |
| `EXTRA_PROMPT` | 在麦克风旁添加提示文本的键。 |
| `EXTRA_LANGUAGE_MODEL` | 指定语言模型的键。 |
| `LANGUAGE_MODEL_FREE_FORM` | 指定常规语音的值。 |
| `LANGUAGE_MODEL_WEB_SEARCH` | 指定语音用于网络搜索的值。 |
| `EXTRA_RESULTS` | 用于获取结果`ArrayList`的键。 |
| `EXTRA_CONFIDENCE_SCORES` | 用于获取结果置信度数组的键。 |

`RecognizerIntent`类包含一些常量，用于在启动`Intent`时支持语音识别。表 10.1 列出了其中部分常量。它们大多是`String`类型。

要创建语音识别`Intent`，我们使用`ACTION_RECOGNIZE_SPEECH`常量作为`Intent`构造函数的参数，如下所示：

```java
Intent intent = new Intent(RecognizerIntent.ACTION_RECOGNIZE_SPEECH);
```

要创建使用语音输入的网页搜索`Intent`，我们使用`RecognizerIntent`类的`ACTION_WEB_SEARCH`常量作为`Intent`构造函数的参数，如下所示：

```java
Intent searchIntent = new Intent(RecognizerIntent.ACTION_WEB_SEARCH);
```

创建`Intent`后，我们可以通过使用`putExtra`方法向其中添加数据，并使用`RecognizerIntent`类的常量作为这些值的键。例如，如果要显示提示文本，我们使用键`EXTRA_PROMPT`并为其提供一个`String`值，如下所示：

```java
intent.putExtra(RecognizerIntent.EXTRA_PROMPT, "What city?");
```

我们可以使用`EXTRA_LANGUAGE_MODEL`常量作为键，指定`LANGUAGE_MODEL_FREE_FORM`常量的值来告诉系统将说出的话语解释为常规语音，或者指定`LANGUAGE_MODEL_WEB_SEARCH`常量的值来将说出的话语解释为网络搜索词串。

### 用于评估设备是否支持语音识别的有用类和方法

| 类 | 方法 | 描述 |
| --- | --- | --- |
| `Context` | `PackageManager getPackageManager()` | 返回一个`PackageManager`实例。 |
| `PackageManager` | `List queryIntentActivities(Intent intent, int flags)` | 返回一个`ResolveInfo`对象列表，表示能够支持`intent`的活动。`flags`参数可用于限制返回的结果。 |
| `ResolveInfo` |  | 包含描述一个`intent`与`intent`过滤器匹配程度的信息。 |

表 10.2 用于评估设备是否支持语音识别的有用类和方法

并非所有设备都支持语音识别。在构建使用语音识别的应用时，最好检查 Android 设备是否支持它。

我们可以使用`android.content.pm`包中的`PackageManager`类来检索设备上安装的应用包的相关信息，此处是与语音识别相关的信息。`Context`类（`Activity`继承自该类）中的`getPackageManager`方法返回一个`PackageManager`实例。在`Activity`内部，我们可以如下使用它：

```java
PackageManager manager = getPackageManager();
```

使用`PackageManager`引用，我们可以调用`queryIntentActivities`方法（如表 10.2 所示，同时还有`getPackageManager`方法和`ResolveInfo`类）来测试当前设备是否支持某种类型的`intent`。我们将`intent`类型作为该方法的第一个参数，它会返回一个`ResolveInfo`对象列表，每个对象对应设备上支持该`intent`的一个活动。如果该列表不为空，则支持该`intent`类型；如果为空，则不支持。

我们可以使用`RecognizerIntent`的`ACTION_RECOGNIZE_SPEECH`常量来构建一个`Intent`对象，并将该`Intent`作为`queryIntentActivities`方法的第一个参数。我们传递`0`作为第二个参数，这不会对方法返回的结果施加任何限制。因此，我们可以使用以下模式来测试当前设备是否支持语音识别：

```java
Intent intent = new Intent(RecognizerIntent.ACTION_RECOGNIZE_SPEECH);
List<ResolveInfo> list = manager.queryIntentActivities(intent, 0);
if (list.size() > 0) {  // 支持语音识别
    // 让用户说点什么并处理它
} else {
    // 提供用户输入的替代方式
}
```

## 10.2 语音识别部分 A，应用版本 0

在应用版本 0 中，我们只有一个`Activity`：我们让用户说出一个词，并在 Logcat 中提供该词的可能匹配列表。同样，我们选择 Empty Activity 模板。在版本 1 中，当我们向应用添加地图时，这将发生变化。

示例 10.1 展示了`MainActivity`类。它分为三个方法：

- 在`onCreate`方法（第 17–32 行）中，我们设置内容视图并检查是否支持语音识别。如果支持，则调用`listen`方法。如果不支持，则显示一条相应的消息。
- 在`listen`方法（第 34–42 行）中，我们设置语音识别`Activity`。
- 在`onActivityResult`方法（第 44–63 行）中，我们在用户说话后处理设备理解的单词列表。

在第 22 行，我们获取一个`PackageManager`引用。使用它，我们在第 23–24 行调用`queryIntentActivities`，传递一个类型为`RecognizerIntent.ACTION_RECOGNIZE_SPEECH`的`Intent`引用，并将结果列表赋值给`listOfMatches`。

我们在第 25 行测试`listOfMatches`是否包含多于一个元素，这意味着当前设备支持语音识别。如果支持，则在第 26 行调用`listen`。如果不支持，我们在第 28–30 行显示一条临时消息。

我们使用`Toast`类（如表 10.3 所示），这是一个方便的类，用于在屏幕上快速显示一条短暂的消息，同时仍允许用户与当前`Activity`交互。

![](img/ch10exa01.jpg)

示例 10.1 `MainActivity`类，从用户处捕获一个单词，版本 0

### `Toast`类的常量和选定方法

| 常量 | 描述 |
| --- | --- |
| `LENGTH_LONG` | 使用此常量可使`Toast`持续 3.5 秒。 |
| `LENGTH_SHORT` | 使用此常量可使`Toast`持续 2 秒。 |

| 方法 | 描述 |
| --- | --- |
| `static Toast makeText(Context context, CharSequence message, int duration)` | 静态方法，在上下文中创建一个`Toast`，显示`message`持续`duration`秒。 |
| `void show()` | 显示此`Toast`。 |

表 10.3 `Toast`类的常量和选定方法

### `Intent`类的`putExtra`和`get...Extra`方法

| 方法 | 描述 |
| --- | --- |
| `Intent putExtra(String key, DataType value)` | 将`value`存储到此`Intent`中，映射到`key`。 |
| `Intent putExtra(String key, DataType[] values)` | 将数组`values`存储到此`Intent`中，映射到`key`。 |
| `DataType getDateTypeExtra(String key, DataType defaultValue)` | 检索映射到`key`的值。如果没有，则返回`defaultValue`。`DataType`可以是基本数据类型或`String`。 |
| `DataType[] getDateTypeArrayExtra(String key)` | 检索映射到`key`的数组。 |

表 10.4 `Intent`类的`putExtra`和`get...Extra`方法

在`listen`方法内部，第 35–36 行，我们创建并实例化`listenIntent`，一个语音识别`intent`。在第 41 行为其启动`Activity`之前，我们在第 37–40 行通过调用`Intent`类的`putExtra`方法（如表 10.4 所示）为其指定一些属性。

在第 37 行，我们将值`What city?`赋给`EXTRA_PROMPT`键，以便它显示在麦克风旁边的屏幕上。在第 38–39 行，我们通过将键`EXTRA_LANGUAGE_MODEL`的值设置为`LANGUAGE_MODEL_FREE_FORM`来指定预期的语音是常规人类语音。在第 40 行，我们将返回列表中的最大单词数设置为`5`。

我们在第 41 行为`listenIntent`启动`Activity`，并将其与请求代码`1`关联，该值由常量`CITY_REQUEST`（第 15 行）定义。当它完成时，`onActivityResult`方法会自动被调用，其第一个参数的值应为该请求代码的值`1`。

在`listen`方法执行后，用户会看到一个显示麦克风和额外提示（本例中为`What city?`）的用户界面，并有几秒钟的时间说话。之后，代码会在继承自`Activity`类的`onActivityResult`方法中执行。

我们在第 46 行调用了`super`的`onActivityResult`方法，尽管在撰写本文时该方法是一个空操作，但未来可能会改变。在第 47 行，我们测试该方法调用是否对应我们之前的活动请求，并且请求是否成功：通过检查存储在`requestCode`参数中的请求代码值和存储在`resultCode`参数中的结果代码值。

如果它们分别等于`1`（即`CITY_REQUEST`的值）和`RESULT_OK`，那么我们就知道该方法调用是针对正确的活动并且成功了。`RESULT_OK`是`Activity`类的一个常量，其值为`–1`，可用于测试活动的结果代码是否成功。

该方法的第三个参数是一个`Intent`引用。通过它，我们可以检索语音识别过程的结果。我们在第 48–50 行检索语音识别器理解的可能单词列表，并将其赋值给`ArrayList`类型的`returnedWords`。

我们调用`getStringArrayListExtra`方法，传入`data`（方法的`Intent`参数）和`EXTRA_RESULTS`键（如表 10.1 所示），以获取其对应的值（一个`String`类型的`ArrayList`）。我们在第 51–53 行检索语音识别器评估的相应置信度分数数组，并将其赋值给数组`scores`。

在此版本中，我们在第 55–61 行将`returnedWords`的元素及其分数输出到 Logcat。

我们不需要“Hello world!”标签。因此，我们编辑`activity_main.xml`文件并移除`TextView`元素。

我们不应期望设备的语音识别能力完美无缺。有时语音识别器能正确理解，有时则不能。有时我们说出同一个单词，但发音略有不同或带有不同口音，它可能会被理解成不同的内容。

图 10.2 显示了运行应用并说出`Washington`时可能的 Logcat 输出，而图 10.3 显示了运行应用并说出`Paris`时可能的 Logcat 输出。



因此，在处理用户的语音时，考虑这些可能性非常重要。有很多方法可以做到这一点。一种方法是通过在屏幕上写出单词或词组来向用户提供反馈，甚至让设备重复单词或词组以确保设备正确理解。然而，这个过程可能会花费额外时间并让用户感到厌烦。我们也可以处理返回列表中的所有元素，并将它们与我们期望的单词列表进行比较，然后处理第一个匹配的单词。我们在版本 1 中就是这样做的。另一种策略是尝试逐个处理该列表中的元素，直到成功处理一个为止。

![](img/9781284093650_CH10_FIGF02.jpg)

图 10.2 用户说出 Washington 时，示例 10.1 可能的 Logcat 输出

![](img/9781284093650_CH10_FIGF03.jpg)

图 10.3 用户说出`Paris`时，示例 10.1 可能的 Logcat 输出

请注意，如果我们在几秒钟内未能说话，显示麦克风的用户界面就会消失，此时再说话就太晚了。如果我们想给用户更多控制权，可以在用户界面中包含一个按钮，点击该按钮会触发对`listen`方法的调用并再次显示麦克风。

## 10.3 使用 Google Maps 活动模板，应用版本 1

`com.google.android.gms.maps`和`com.google.android.gms.maps.model`包中包含用于显示地图和在其上放置标注的类。根据我们使用的 Android Studio 版本，可能需要通过 SDK 管理器更新 Google Play 服务和 Google APIs。附录 C 展示了这些步骤。

Google Maps 活动模板已经包含了显示地图的骨架代码。此外，它还在`build.gradle`（Module: app）文件中为项目提供了必要的 Google Play 服务库，如附录 C 所示。创建项目时，我们不选择通常使用的 Empty Activity 模板，而是选择 Google Maps Activity 模板（参见图 10.4）。如图 10.5 所示，`Activity`类、布局 XML 文件和应用标题的默认名称分别是`MapsActivity`、`activity_main.xml`和`Map`。

除了常规文件外，`google_maps_api.xml`文件也会自动生成，并位于 values 目录中。示例 10.2 展示了该文件。

![](img/9781284093650_CH10_FIGF04.jpg)

图 10.4 选择 Google Maps Activity 模板

![](img/9781284093650_CH10_FIGF05.jpg)

图 10.5 模板创建的主要文件的名称

![](img/ch10exa02.jpg)

示例 10.2 `google_maps_api.xml`文件，显示地图应用，版本 1

![](img/9781284093650_CH10_FIGF06.jpg)

图 10.6 `google_maps_api.xml`文件的第 18–19 行，密钥部分隐藏

在第 18 行，我们将`YOUR_KEY_HERE`替换为根据附录 C 中的说明从 Google 获取的实际密钥。编辑后，作者的第 18–19 行如图 10.6 所示。

模板自动生成的布局文件名为`activity_maps.xml`，如示例 10.3 所示。通常将地图放置在片段中（第 1 行）。这里使用的片段类型是`SupportMapFragment`（第 2 行），它是`Fragment`类的子类，也是在应用中包含地图的最简单方式。它占据其整个父`View`（第 6–7 行），并有一个 id（第 1 行）。因此，我们可以通过编程方式检索它并更改地图的特性，例如移动地图中心或添加标注。

![](img/ch10exa03.jpg)

示例 10.3 `activity_maps.xml`文件，显示地图应用，版本 1

`AndroidManifest.xml`文件已经包含了两个额外的元素`uses-permission`和`meta-data`，用于从 Google Play 服务检索地图，如示例 10.4 所示。与典型的骨架`AndroidManifest.xml`文件相比，主要添加的内容如下：

- activity 元素类型为`MapsActivity`。
- 有一个`uses-permission`元素，指定应用可以访问当前设备位置。
- 有一个`meta-data`元素，指定关键信息。

要在`AndroidManifest.xml`文件中请求权限，我们使用以下语法：

```xml
<uses-permission android:name="permission_name"/>
```

表 10.5 列出了`Manifest.permission`类的一些`String`常量，我们可以将其用作`permission_name`的值。

![](img/ch10exa04.jpg)

示例 10.4 `AndroidManifest.xml`文件，显示地图应用，版本 1

| 常量 | 描述 |
| --- | --- |
| `INTERNET` | 允许应用访问互联网。 |
| `ACCESS_NETWORK_STATE` | 允许应用访问网络信息。 |
| `WRITE_EXTERNAL_STORAGE` | 允许应用写入外部存储。 |
| `ACCESS_COARSE_LOCATION` | 允许应用访问基于基站和 Wi-Fi 得出的设备大致位置。 |
| `ACCESS_FINE_LOCATION` | 允许应用访问基于 GPS、基站和 Wi-Fi 得出的设备精确位置。 |
| `RECORD_AUDIO` | 允许应用录制音频。 |

表 10.5 `Manifest.permission`类中的选定常量

每个应用必须声明其所需的权限。当用户安装应用时，系统会告知用户该应用所需的所有权限，如果用户不愿意授予这些权限，则可以在此时取消安装。

在第 9–10 行，自动生成的代码包含一个`uses-permission`元素，以便应用能够使用 GPS 获取设备位置。在第 29–31 行，代码包含一个`meta-data`元素，用于指定 Android 地图的键值。在第 33–35 行，代码为我们的`MapsActivity`活动定义了一个`activity`元素。在第 36–40 行，我们指定它是应用启动时第一个启动的活动。

`com.google.android.gms.maps`包为我们提供了显示和修改地图的类。表 10.6 展示了其中一些选定的类。`LatLng`类属于`com.google.android.gms.maps.model`包。

| 类 | 描述 |
| --- | --- |
| `SupportMapFragment` | 包含地图的容器。 |
| `GoogleMap` | 用于管理地图的主类。 |
| `CameraUpdateFactory` | 包含创建`CameraUpdate`对象的静态方法。 |
| `CameraUpdate` | 封装相机移动，例如位置变化或缩放级别变化，或两者兼有。 |
| `LatLng` | 使用纬度和经度封装地球上的一个位置。 |

表 10.6 来自`com.google.android.gms.maps`和`com.google.android.gms.maps.model`包的选定类

| 类或接口 | 方法 | 描述 |
| --- | --- | --- |
| `SupportMapFragment` | `void getMapAsync( OnMapReadyCallback callback )` | 设置回调，当地图准备就绪时，将调用其`mapReady`方法。 |
| `OnMapReadyCallback` | `void onMapReady( GoogleMap map )` | 当地图实例化并准备就绪时调用此方法。需要实现此方法。 |

表 10.7 `SupportMapFragment`类的`getMapSync`方法和`OnMapReadyCallback`接口的`mapReady`方法

`GoogleMap`类是修改地图特征和处理地图事件的核心类。我们的起点是一个`SupportMapFragment`对象，我们可以通过布局中的 ID 检索它，也可以通过编程方式构建它。为了修改该`SupportMapFragment`中包含的地图，我们需要一个指向它的`GoogleMap`引用。我们可以通过调用`SupportMapFragment`类的`getMapAsync`方法来获取该参数，如表 10.7 所示。

`OnMapReadyCallback`接口只包含一个方法`onMapReady`，同样在表 10.7 中展示。`onMapReady`方法接受一个参数，即`GoogleMap`。当该方法被调用时，其`GoogleMap`参数已被实例化，并且保证不为`null`。

以下代码序列将从实现`OnMapReadyCallback`接口的类中名为`fragment`的`SupportMapFragment`获取一个`GoogleMap`引用。

```java
// 假设 fragment 是 SupportMapFragment 的引用
GoogleMap map;
// 假设 this "是一个" OnMapReadyCallback
fragment.getMapAsync( this );
public void onMapReady( GoogleMap googleMap ) {
  map = googleMap;
}
```

为了修改地图，例如其中心点和缩放级别，我们使用`GoogleMap`类的`animateCamera`和`moveCamera`方法，这些方法都接受一个`CameraUpdate`参数。`CameraUpdate`类封装了相机移动。相机显示我们正在查看的地图：如果我们移动相机，地图就会移动。我们还可以使用`GoogleMap`类的`addMarker`、`addCircle`和其他方法向地图添加注释。表 10.8 展示了其中一些方法。

为了创建`CameraUpdate`，我们使用`CameraUpdateFactory`类的`static`方法。表 10.9 展示了其中一些方法。`CameraUpdate`对象包含位置和缩放级别值。缩放级别范围从 2.0 到 21.0。缩放级别 21.0 最接近地球，显示最详细的细节。

| 方法 | 描述 |
| --- | --- |
| `void animateCamera( CameraUpdate update )` | 将相机位置（并修改地图）从当前位置动画移动到`update`。 |
| `void animateCamera( CameraUpdate update, int ms, GoogleMap. CancelableCallback callback )` | 将相机位置（并修改地图）从当前位置动画移动到`update`，耗时`ms`毫秒。如果任务被取消，则调用`callback`的`onCancel`方法。如果任务完成，则调用`callback`的`onFinish`方法。 |
| `void moveCamera( CameraUpdate update )` | 将相机位置（并修改地图）从当前位置移动到`update`，无动画效果。 |
| `void setMapType( int type )` | 设置要显示的地图类型：`GoogleMap`类的常量`MAP_TYPE_NORMAL`、`MAP_TYPE_SATELLITE`、`MAP_TYPE_TERRAIN`、`MAP_TYPE_NONE`和`MAP_TYPE_HYBRID`可用于`type`。 |
| `Marker addMarker( MarkerOptions options )` | 向此地图添加标记并返回该标记；`options`定义标记。 |
| `Circle addCircle( CircleOptions options )` | 向此地图添加圆形并返回该圆形；`options`定义圆形。 |
| `Polygon addPolygon( PolygonOptions options )` | 向此地图添加多边形并返回该多边形；`options`定义多边形。 |
| `void setOnMapClickListener( GoogleMap. OnMapClickListener listener )` | 设置一个回调方法，当用户点击地图时自动调用；`listener`必须是实现`GoogleMap.OnMapClickListener`接口并重写其`onMapClick(LatLng)`方法的类的实例。 |

表 10.8 `GoogleMap`类的选定方法

通常，我们想要更改地图中心的位置。如果我们知道该点的纬度和经度坐标，可以使用`LatLng`类通过以下构造函数创建一个：

```java
LatLng( double latitude, double longitude )
```

因此，如果我们有一个名为`fragment`的`MapFragment`引用，我们可以使用`GoogleMap`类的`moveCamera`方法更改其地图的位置，如下所示：

```java
// someLatitute 和 someLongitude 表示地球上的某个位置
GoogleMap map = fragment.getMap( );
LatLng newCenter = new LatLng( someLatitude, someLongitude );
CameraUpdate update1 = CameraUpdateFactory.newLatLng( newCenter );
map.moveCamera( update1 );
```

| 方法 | 描述 |
| --- | --- |
| `CameraUpdate newLatLng( LatLng location )` | 返回一个将地图移动到`location`的`CameraUpdate`。 |
| `CameraUpdate newLatLngZoom( LatLng location, float zoom )` | 返回一个将地图移动到`location`并设置缩放级别为`zoom`的`CameraUpdate`。 |
| `CameraUpdate zoomIn( )` | 返回一个放大的`CameraUpdate`。 |
| `CameraUpdate zoomOut( )` | 返回一个缩小的`CameraUpdate`。 |
| `CameraUpdate zoomTo( float level )` | 返回一个缩放到缩放级别`level`的`CameraUpdate`。 |

表 10.9 `CameraUpdateFactory`类的选定方法

然后，我们可以使用`GoogleMap`类的`zoomIn`方法进行放大，如下所示：

```java
CameraUpdate update2 = CameraUpdateFactory.zoomIn( );
map.animateCamera( update2 );
```

如果我们想直接缩放到级别 10，可以使用`GoogleMap`类的`zoomTo`方法，如下所示：

```java
CameraUpdate update3 = CameraUpdateFactory.zoomTo( 10.0f );
map.animateCamera( update3 );
```

示例 10.5 展示了`MapsActivity`类。它继承自`FragmentActivity`（第 13 行）和`OnMapReadyCallback`（第 14 行）。与地图相关的类在第 6–11 行导入。此类加载`activity_maps.xml`布局文件，然后在澳大利亚悉尼放置一个标记。

在第 16 行声明了一个`GoogleMap`实例变量`mMap`。`onCreate`方法（第 19–27 行）在第 21 行加载 XML 布局文件，在第 24–25 行检索地图片段，并在第 26 行调用其`getMapSync`方法。

`onMapReady`方法（第 29–48 行）在地图准备就绪时自动调用。我们在第 41 行将其`GoogleMap`参数赋值给`mMap`实例变量。在第 44 行，我们使用澳大利亚悉尼的纬度和经度值创建了一个`LatLng`引用。在第 45–46 行，我们通过链式方法调用和一个匿名`MarkerOptions`对象，在地图上添加了一个标记，其标题为“悉尼标记”。表 10.10 展示了`MarkerOptions`类的构造函数和各种方法。这等价于以下代码序列：

```java
MarkerOptions options = new MarkerOptions( );
options.position( sydney );
options.title( "Marker in Sydney" );
mMap.addMarker( options );
```

![](img/ch10exa05.jpg)

示例 10.5 `MapsActivity`类，显示地图应用，版本 1

| 构造函数 | 描述 |
| --- | --- |
| `MarkerOptions( )` | 构造一个`MarkerOptions`对象。 |

| 方法 | 描述 |
| --- | --- |
| `MarkerOptions position( LatLng latLng )` | 设置此`MarkerOptions`的（纬度，经度）位置。 |
| `MarkerOptions title( String title )` | 设置此`MarkerOptions`的标题。 |
| `MarkerOptions snippet( String snippet )` | 设置此`MarkerOptions`的摘要。 |
| `MarkerOptions icon( BitmapDescriptor icon )` | 设置此`MarkerOptions`的图标。 |

表 10.10 `MarkerOptions`类的选定方法

![](img/9781284093650_CH10_FIGF07.jpg)

图 10.7 显示地图应用，版本 1，在平板电脑中运行



当用户触摸标记时，标题会显示在标注框中。最后，在第 47 行，我们将相机移动到由 `LatLng` 引用 `sydney` 定义的地图位置，从而显示以澳大利亚悉尼为中心的地图。

图 10.7 显示了在平板电脑中运行的应用。它也可以在模拟器中运行，但可能需要更新 Google Play 服务才能实现。

## 10.4 向地图添加注释，应用版本 2

在版本 2 中，我们将地图中心定位在华盛顿特区的白宫，设置缩放级别，添加标记，并在地图中心周围绘制一个圆。项目中受影响的部分只有 `MapsActivity` 类的 `onMapReady` 方法。为此，我们使用表 10.8 中所示的 `addMarker` 和 `addCircle` 方法。

这两个方法类似：`addMarker` 接受一个 `MarkerOptions` 参数，`addCircle` 接受一个 `CircleOptions` 参数。表 10.11 展示了 `CircleOptions` 类的选定方法。

对于两者，我们首先使用默认构造函数实例化一个对象，然后调用相应的方法来定义标记或圆。我们必须指定一个位置，否则运行时将出现异常，应用会停止。两个表中显示的所有方法都返回调用该方法的对象的引用，因此方法调用可以链式进行。

| 构造函数 | 描述 |
| --- | --- |
| `CircleOptions()` | 构造一个 `CircleOptions` 对象。 |

| 方法 | 描述 |
| --- | --- |
| `CircleOptions center(LatLng latLng)` | 设置此 `CircleOptions` 的中心（纬度，经度）位置。 |
| `CircleOptions radius(double meters)` | 设置此 `CircleOptions` 的半径，单位为米。 |
| `CircleOptions strokeColor(int color)` | 设置此 `CircleOptions` 的描边颜色。 |
| `CircleOptions strokeWidth(float width)` | 设置此 `CircleOptions` 的描边宽度，单位为像素。 |

表 10.11 `CircleOptions` 类的选定方法

要向名为 `mMap` 的 `GoogleMap` 添加一个圆，我们可以使用以下代码序列：

```java
LatLng whiteHouse = new LatLng( 38.8977, -77.0366 );
CircleOptions options = new CircleOptions( );
options.center( whiteHouse );
options.radius( 500 );
options.strokeWidth( 10.0f );
options.strokeColor( 0xFFFF0000 );
mMap.addCircle( options );
```

由于前面使用的所有 `CircleOptions` 方法都返回调用它们的 `CircleOptions` 引用，我们可以将所有语句链式合并为一条，如下所示：

```java
map.addCircle( new CircleOptions( ).center( new LatLng( 38.8977,
-77.0366 ) ).radius( 500 ).strokeWidth( 10.0f ).strokeColor(
0xFFFF0000 ) );
```

第一种格式具有清晰的优势。第二种格式更紧凑。网上找到的许多示例都使用第二种格式。

![](img/ch10exa06.jpg)

示例 10.6 `MapsActivity` 类，显示地图应用，版本 2

![](img/9781284093650_CH10_FIGF08.jpg)

图 10.8 带有注释的白宫地图，显示地图应用，版本 2

示例 10.6 展示了更新后的 `MapsActivity` 类。在第 40–44 行，我们在地图上放置了一个标记，指定了其位置、标题和摘要。我们在第 40 行实例化 `MarkerOptions options`，在第 41–43 行设置其属性，并在第 44 行将其添加到地图中。

在第 46–49 行，我们在地图上放置了一个圆，指定了其位置、半径、描边宽度和颜色。我们在第 46–48 行实例化一个 `CircleOptions` 对象，并链式调用 `center`、`radius`、`strokeWidth` 和 `strokeColor` 方法。圆的中心位于白宫位置，半径为 `500` 米，描边宽度为 `10` 像素，颜色为红色。我们在第 49 行将其添加到地图中。虽然我们更喜欢第一种编码风格（即用于标记的那种），但许多开发者使用第二种编码风格，将方法调用链式合并为一条语句。因此，我们应该熟悉这两种风格。

图 10.8 显示了在平板电脑中运行的应用，用户触摸标记后的情况。标题和摘要仅在用户触摸标记时显示。

## 10.5 模型

在版本 3 中，我们在地图活动之前放置了一个语音识别活动：我们期望用户说出几个预定义城市中的一个：华盛顿、巴黎、纽约、罗马和伦敦。我们分析设备理解的单词，并将其与这五个城市进行比较。如果匹配成功，我们显示匹配城市的地图。我们还在地图上放置标记，每个标记附带一个著名景点的描述。我们仍然使用 Google Maps Activity 模板。我们需要修改 `AndroidManifest.xml` 文件，将语音识别活动添加为应用的启动活动，从而指定地图活动不是启动活动。

我们保持模型简单：将（城市，景点）对存储在哈希表中。哈希表是一种将键映射到值的数据结构。例如，我们可以将整数 1 到 12 映射到月份（一月、二月、三月等），并将它们存储在哈希表中。我们也可以将美国各州存储在哈希表中：键是 MD、CA、NJ 等，值是马里兰州、加利福尼亚州、新泽西州等。

在这个应用中，城市（键）是纽约、华盛顿、伦敦、罗马和巴黎。景点（值）是自由女神像、白宫、白金汉宫、罗马斗兽场和埃菲尔铁塔。我们希望将用户说出的单词与模型中的城市进行匹配。如果没有匹配，我们使用华盛顿作为默认城市。

示例 10.7 展示了 `Cities` 类，它封装了我们的模型。在第 11–13 行，我们声明了三个常量来存储字符串 `Washington`、其纬度和经度。在第 8 行，我们声明了一个常量 `CITY_KEY`，用于存储字符串 `city`。当我们从第一个活动转到第二个活动时，我们使用该常量作为语音识别器理解的城市名称的键，该键位于我们用于启动活动的意图中。

在第 9 行，我们声明了常量 `MIN_CONFIDENCE`，并赋予其值 `0.5`。它定义了语音识别器理解的任何单词需要达到的置信度阈值，以便我们将其处理为有效城市。在第 14 行，我们声明了常量 `MESSAGE`。当我们向地图添加标记时，会用到它。

我们在第 16 行声明了唯一的实例变量 `places`，它是一个 `Hashtable`。`Hashtable` 是一个泛型类型，其实际数据类型在声明时指定。`<String, String>` 中的第一个 `String` 是键的数据类型，第二个 `String` 是值的数据类型。

我们在第 18–20 行编写了一个构造函数，它接受一个 `Hashtable` 作为参数并将其赋值给 `places`。在第 43–45 行，`getAttraction` 方法返回 `places` 中映射到给定城市的景点。如果 `places` 中没有该城市，则返回 `null`。

在第 22–41 行，`firstMatchWithMinConfidence` 方法接受一个 `String` 类型的 `ArrayList` 和一个 `float` 数组作为参数。`ArrayList` 表示语音识别器提供的单词列表，`float` 数组存储这些单词的置信度。

我们使用双重循环处理参数：外层循环遍历所有单词（第 29 行），内层循环（第 34 行）检查其中一个单词是否与哈希表 `places` 中的键匹配。我们期望置信度按降序排列。因此，如果当前单词的置信度低于 `MIN_CONFIDENCE`（第 30 行），则剩余的单词也会低于该值，因此我们退出外层循环并在第 40 行返回 `DEFAULT_CITY` 的值。

在内层循环中，我们在第 36 行测试当前单词是否与哈希表 `places` 中列为键的城市匹配。如果匹配，则在第 37 行返回该城市。

如果外层循环处理完毕且未找到置信度可接受的匹配项，则在第 40 行返回 `DEFAULT_CITY` 的值。注意，我们在外层循环（第 29 行）中处理参数 `words`，在内层循环（第 34 行）中处理 `places` 的键，而不是反过来，因为我们期望 `words` 按置信度降序排列。

![](img/ch10exa07.jpg)

示例 10.7 `Cities` 类，Show A Map 应用，版本 2

## 10.6 基于语音输入显示地图，应用版本 3

在第一个活动中，我们要求用户说出一个城市的名称，并使用 `Cities` 类将语音识别器返回的单词列表转换为我们有信心认为用户说出的城市名称。如果没有匹配项，则使用 `Cities` 类中 `DEFAULT_CITY` 常量存储的默认城市。

然后，我们将该信息存储在启动地图活动之前创建的 intent 中。在 `MapsActivity` 类中，我们可以访问该 intent，检索城市名称并显示正确的地图。

我们需要执行以下操作：

* 创建一个要求用户说话的活动。
* 为该活动添加一个 XML 布局文件。
* 用户说话后，跳转到地图活动。
* 根据用户所说的内容，显示正确的地图。
* 编辑 `AndroidManifest.xml`。

我们仍然使用 Google Maps Activity 模板来自动生成代码，特别是 gradle 文件、`AndroidManifest.xml` 文件和 `MapsActivity` 类。当我们添加一个 `MainActivity` 类作为第一个活动时，我们修改 `AndroidManifest.xml` 文件，使 `MainActivity` 成为第一个活动，`MapsActivity` 成为第二个活动。

我们从版本 0 的 `MainActivity` 类及其 `activity_main.xml` 布局文件开始，其中我们删除了 `TextView` 元素和 padding 属性。

示例 10.8 显示了更新后的 `MainActivity` 类。在检索到用户所说的城市后，我们启动第二个活动来显示以该城市为中心的地图。为了分析用户所说的城市，我们使用 `Cities` 类。

我们在第 16 行声明了 `cities`，一个 `Cities` 实例变量；它代表我们的模型。为了方便起见，因为我们需要从 `MapsActivity` 类中访问它，我们将其声明为 `public` 和 `static`。我们在 `onCreate` 方法中的第 22–28 行使用五个城市的列表实例化它。

在 `onActivityResult` 方法的第 63–65 行，我们调用 `cities` 的 `firstMatchWithMinConfidence` 方法来检索用户所说的城市名称，并将其赋值给 `String` 变量 `firstMatch`。在第 68–69 行，我们将 `firstMatch` 放入一个 intent 中，使用 `putExtra` 方法（如表 10.12 所示）启动 `MapsActivity`，并将其映射到键 `city`。我们在第 70–71 行启动该活动。

在 `MapsActivity` 类中，我们需要执行以下操作：

* 访问该活动的原始 intent 并检索存储在 intent 中的城市名称。
* 将该城市名称转换为纬度和经度坐标。
* 将地图的中心设置为该点。

为了检索存储在原始 intent 中的城市名称，我们使用表 10.12 中所示的 `getStringExtra` 方法。

我们需要将城市名称转换为地球上的一个点（纬度，经度），以便显示以该点为中心的地图。更一般地说，将地址转换为一对纬度和经度坐标的过程称为地理编码。相反，从一对纬度和经度坐标转换为地址的过程称为反向地理编码，如表 10.13 所示。

![](img/ch10exa08.jpg)

示例 10.8 `MainActivity` 类，Show A Map 应用，版本 3

| 方法 | 描述 |
| --- | --- |
| `Intent putExtra(String key, String value)` | 将值放入此 `Intent` 中，并将其与 `key` 关联；返回此 `Intent`。 |
| `String getStringExtra(String key)` | 检索并返回使用 `key` 放入此 `Intent` 中的值。 |

表 10.12 `Intent` 类的 `putExtra` 和 `getStringExtra` 方法

`Geocoder` 类提供了地理编码和反向地理编码的方法。表 10.14 列出了它的两个方法：`getFromLocationName`（地理编码方法）和 `getFromLocation`（反向地理编码方法）。它们都返回一个 `Address` 对象的 `List`，按匹配置信度降序排列。对于此应用，我们保持简单，处理该列表中的第一个元素。

`Address` 类属于 `android.location` 包，存储地址信息，包括街道地址、城市、州、邮政编码、国家等，以及纬度和经度。表 10.15 显示了它的 `getLatitude` 和 `getLongitude` 方法。

| 地理编码 | 反向地理编码 |
| --- | --- |
| 地址 → (纬度, 经度) | (纬度, 经度) → 街道地址 |
| 示例：1600 Pennsylvania Avenue, Washington, DC 20500 → (38.8977, -77.0366) | 示例：(38.8977, -77.0366) → 1600 Pennsylvania Avenue, Washington, DC 20500 |

表 10.13 地理编码与反向地理编码

| 构造函数 | 描述 |
| --- | --- |
| `Geocoder(Context context)` | 构造一个 `Geocoder` 对象。 |

| 方法 | 描述 |
| --- | --- |
| `List<Address> getFromLocationName(String address, int maxResults)` | 根据地址返回一个 `Address` 对象列表。该列表最多包含 `maxResults` 个元素，按匹配度降序排列。如果 `address` 为 null，则抛出 `IllegalArgumentException`；如果网络不可用或存在其他 IO 问题，则抛出 `IOException`。 |
| `List<Address> getFromLocation(double latitude, double longitude, int maxResults)` | 根据地球上由纬度和经度定义的点返回一个 `Address` 对象列表。该列表最多包含 `maxResults` 个元素，按匹配度降序排列。如果 `latitude` 或 `longitude` 超出范围，则抛出 `IllegalArgumentException`；如果网络不可用或存在其他 IO 问题，则抛出 `IOException`。 |

表 10.14 `Geocoder` 类的选定方法

| 方法 | 描述 |
| --- | --- |
| `double getLatitude()` | 返回此 `Address` 的纬度（如果当时已知）。 |
| `double getLongitude()` | 返回此 `Address` 的经度（如果当时已知）。 |

表 10.15 `Address` 类的 `getLatitude` 和 `getLongitude` 方法

表 10.15 `Address` 类的选定方法

示例 10.9 展示了从版本 2 更新而来的 `MapsActivity` 类。我们在第 25 行声明了 `city`，一个存储城市名称的 `String` 实例变量。在第 32–36 行，我们检索了存储在用于启动此地图活动的意图中的城市名称。

我们在第 33 行获取了意图的引用，在第 34 行调用 `getStringExtra` 并检索城市名称，将其赋值给 `city`。如果 `city` 为 `null`（第 35 行），我们在第 36 行将其赋值为 `Cities` 类中定义的默认城市。

![](img/ch10exa09.jpg) ![](img/ch10exa09a.jpg)

示例 10.9 `MapsActivity` 类，显示地图应用，版本 3

在 `onMapReady` 方法内部，我们将用户所选城市及其景点定义的地址进行地理编码，转换为经纬度坐标。然后，我们基于这些坐标设置地图，包括一个圆形和一个标记，与版本 2 相同。

在第 49–51 行，我们声明了 `latitude` 和 `longitude` 两个 `double` 变量，用于存储 `city` 的经纬度坐标。我们使用 `Cities` 类的 `DEFAULT_LATITUDE` 和 `DEFAULT_LONGITUDE` 常量中的默认值对它们进行初始化。在第 53–55 行，我们检索城市的景点并将其赋值给 `String attraction`。



我们在第 58 行声明并实例化了一个`Geocoder`对象`coder`。`getFromLocationName`方法会抛出`IOException`（一个受检异常），例如当发生 I/O 问题（如网络相关问题）时。因此，在调用此方法时，我们需要使用`try`（第 59–67 行）和`catch`（第 68–71 行）块。我们在第 61 行将地址定义为景点和城市的拼接。在第 62 行调用`getFromLocationName`方法，传入`address`和`5`以指定我们只需要`5`个或更少的结果，并将返回值赋值给`addresses`。我们在第 63 行测试`addresses`是否为`null`，如果不是，则在第 64 和 65 行将其第一个元素的经纬度数据赋值给`latitude`和`longitude`。如果我们在`catch`块内执行，则表示我们未能获取`city`的经纬度数据，因此我们将`city`重置为默认值。

之后，我们在第 73–78 行将地图中心更新为坐标（`latitude`，`longitude`）的点，并设置缩放级别。我们在第 80–84 行添加标记，在第 86–89 行添加圆形。

我们需要更新`AndroidManifest.xml`文件，以便应用从语音识别活动启动，并包含地图活动。示例 10.10 展示了更新后的`AndroidManifest.xml`文件。在第 34 行，我们将`MainActivity`指定为启动器活动。在第 43–45 行，我们添加了一个`MapsActivity activity`元素。

![](img/ch10exa10.jpg)

示例 10.10 `AndroidManifest.xml`文件，显示地图应用，版本 3

最后，示例 10.11 展示了`activity_main.xml`文件，这是第一个活动的骨架`RelativeLayout`。

图 10.9 展示了我们的应用版本 3 在平板电脑上运行时的第二个屏幕。它显示了用户说出`Paris`后法国巴黎的地图。注意地图中心是埃菲尔铁塔，因为我们将景点名称添加到城市名称中，使得地图中心位于景点位置。

![](img/ch10exa11.jpg)

示例 10.11 `activity_main.xml`文件，显示地图应用，版本 3

![](img/9781284093650_CH10_FIGF09.jpg)

图 10.9 显示地图应用，版本 3，在平板电脑中运行

## 10.7 控制语音输入，应用版本 4

注意，如果我们运行应用且不说话，麦克风会消失，我们就会停留在第一个活动上，现在它是一个空白屏幕。此外，如果我们进入第二个屏幕然后返回第一个屏幕，也会出现空白屏幕。解决此问题的一种方法是无论如何都启动地图活动。如果用户一言不发，麦克风会消失，但`onActivityResult`仍然会执行。我们可以将启动地图活动的代码放在示例 10.8 的`onActivityResult`方法的`if`块之外。显示的地图是默认地图。

解决此问题的另一种方法是添加一个按钮，当点击时触发对`listen`的调用并重新调出麦克风。这给了用户控制的机会，尽管需要额外点击按钮。我们在版本 4 中实现了这一功能。我们编辑`activity_main.xml`，在第一个屏幕上添加一个按钮，并在`MainActivity`类中添加一个方法来处理该点击。

示例 10.12 展示了编辑后的`activity_main.xml`文件。在第 8–14 行，我们定义了一个显示在屏幕顶部的按钮。我们在第 13 行为其指定 id `speak`，并在第 14 行指定用户点击按钮时执行`startSpeaking`方法。

![](img/ch10exa12.jpg)

示例 10.12 `activity_main.xml`文件，包含一个按钮，显示地图应用版本 4

示例 10.13 展示了编辑后的`strings.xml`文件。`click_to_speak`字符串在第 4 行定义。

![](img/ch10exa13.jpg)

示例 10.13 `strings.xml`文件，显示地图应用，版本 4

示例 10.14 展示了编辑后的`MainActivity`类。它在第 20 行包含实例变量`speak`（一个`Button`）。它在第 25 行被赋值为`activity_main.xml`中定义的按钮。如果不支持语音识别，我们在第 42 行禁用该按钮。`startSpeaking`方法在第 49–51 行定义。它在第 50 行调用`listen`。注意，如果我们想设置按钮直接调用`listen`，我们需要为`listen`添加一个`View`参数。当`listen`执行时，我们在第 54 行禁用按钮，并在第 84 行`onActivityResult`执行完毕后重新启用它，这样当我们停留在此屏幕或从地图活动按返回键返回此屏幕时，按钮处于启用状态。

![](img/ch10exa14.jpg) ![](img/ch10exa14a.jpg)

示例 10.14 `MainActivity`类，显示地图应用，版本 4

如果我们再次运行应用，每当第一个屏幕变空白时，我们可以点击按钮重新调出麦克风。

## 10.8 语音识别 B 部分，通过语音一次性移动地图，应用版本 5

我们已经学习了如何使用意图进行语音识别。有些用户可能喜欢通过语音与应用交互，但他们可能会觉得随之而来的用户界面很烦人。特别是，如果我们允许用户反复通过语音提供输入，可能希望在不显示麦克风的情况下进行。

`SpeechRecognizer`类以及`RecognitionListener`接口（均属于`android.speech`包）允许我们在不使用图形用户界面的情况下监听和处理用户语音。但是，我们仍然会有提示音提醒用户应用期望他/她说些什么。在应用的版本 5 中，我们允许用户根据语音输入移动地图：如果用户说出`North`、`South`、`West`或`East`，我们分别将地图中心向北、南、西、东移动。`MainActivity`和`activity_main.xml`没有变化。

为了实现这一点，我们执行以下操作：

- 编辑`AndroidManifest.xml`文件，以便请求音频录制权限。
- 添加功能，将用户说出的单词与可能的方向列表进行比较。
- 在`MapsActivity`类中捕获语音输入并进行处理。

为了添加录制音频的权限，我们编辑`AndroidManifest.xml`文件，如示例 10.15 的第 12–13 行所示。

![](img/ch10exa15.jpg)

示例 10.15 `AndroidManifest.xml`文件，显示地图应用，版本 5

为了方便起见，我们编写了`Directions`类，其中包含`Directions`枚举。我们用它来将用户输入与`Directions`中的各种常量进行比较。虽然我们可以使用`String`常量，但使用`enum`能让我们的代码具有更好的自文档性。示例 10.16 展示了`Directions`类。

![](img/ch10exa16.jpg)

示例 10.16 `Directions`类，Show A Map 应用，版本 5

与之前捕获语音输入时一样，我们会获得一个可能的匹配词列表以及一个并行的置信度分数数组。在这个版本的应用中，我们将该列表与`enum` `Directions`中的常量进行比较，以判断用户是否说出了定义有效方向的词。为此，我们编写了另一个类`MatchingUtility`，如示例 10.17 所示。它包含一个常量`MIN_CONFIDENCE`，用于定义匹配词的最低可接受分数，以及一个方法`firstMatchWithMinConfidence`，用于测试一个词列表是否包含与`enum Directions`中定义的某个常量匹配的`String`。如果匹配，则返回该`String`。`firstMatchWithMinConfidence`方法与之前示例 10.7 中展示的`Cities`类的方法非常相似，区别在于我们将词列表与`enum`列表进行比较，而不是与哈希表中的键列表进行比较。代码的主要区别在于第 18 行我们如何遍历`enum Directions`。通常，要遍历名为`EnumName`的`enum`，我们使用以下`for`循环头：

```java
for (EnumName current : EnumName.values()) {
    // 在此处处理 current
}
```

![](img/ch10exa17.jpg)

示例 10.17 `MatchingUtility`类，Show A Map 应用，版本 5

### 表 10.16 `RecognitionListener`接口的方法

| 方法 | 调用时机 |
| --- | --- |
| `void onReadyForSpeech(Bundle bundle)` | 语音识别器已准备好让用户开始说话。 |
| `void onBeginningOfSpeech()` | 用户开始说话。 |
| `void onEndOfSpeech()` | 用户停止说话。 |
| `void onPartialResults(Bundle bundle)` | 部分结果已就绪。此方法可能被调用 0 次、1 次或多次。 |
| `void onResults(Bundle bundle)` | 结果已就绪。 |
| `void onBufferReceived(byte[] buffer)` | 刚刚接收到更多声音。此方法可能不会被调用。 |
| `void onEvent(int eventType, Bundle bundle)` | 此方法当前未使用。 |
| `void onRmsChanged(float rmsdB)` | 输入声音的音量级别已改变。此方法被频繁调用。 |
| `void onError(int error)` | 发生了识别或网络错误。 |

为了在没有用户界面的情况下捕获语音输入，我们实现了`RecognitionListener`接口。该接口有九个方法需要重写，如表 10.16 所列。

当使用`RecognitionListener`接口处理语音事件时，我们需要执行以下步骤：

- 编写一个实现`RecognitionListener`接口的语音处理类，并重写其所有方法。
- 声明并实例化该语音处理类的一个对象。
- 声明并实例化一个`SpeechRecognizer`对象。
- 将语音处理对象注册到`SpeechRecognizer`对象上。
- 告诉`SpeechRecognizer`对象开始监听。

### 表 10.17 `Bundle`类的选定方法

| 方法 | 描述 |
| --- | --- |
| `ArrayList getStringArrayList(String key)` | 返回与`key`关联的`String`的`ArrayList`，如果没有则返回`null`。 |
| `float[] getFloatArray(String key)` | 返回与`key`关联的`float`数组，如果没有则返回`null`。 |

在平板设备上测试时，`RecognitionListener`接口各个方法的调用顺序（不包括对`onRmsChanged`方法的调用）如下：

```text
onReadyForSpeech, onBeginningOfSpeech, onEndOfSpeech, onResults
```

我们在`onResults`方法中处理用户输入。它的`Bundle`参数使我们能够访问可能的匹配词列表及其对应的置信度分数。表 10.17 列出了我们用来检索可能的匹配词列表及其相关置信度分数的两个`Bundle`类方法。我们使用以下模式：

```java
public void onResults(Bundle results) {
    ArrayList<String> words =
        results.getStringArrayList(SpeechRecognizer.RESULTS_RECOGNITION);
    float[] scores =
        results.getFloatArray(SpeechRecognizer.CONFIDENCE_SCORES);
    // 处理 words 和 scores
```

示例 10.18 展示了`MapsActivity`类中的编辑。在第 27 行，我们声明了`DELTA`，这是一个常量，用于根据用户输入更改地图中心的纬度或经度。在第 31 行，我们声明了一个`SpeechRecognizer`实例变量`recognizer`。

在第 118–168 行，我们编写了`private`类`SpeechListener`，它`implements` `RecognitionListener`。在这个版本的应用中，我们只关心处理结果，因此我们重写了所有方法，除了`onResults`之外都设为空操作，而`onResults`是处理语音结果的方法。我们在第 132–133 行检索可能的匹配词列表，并将其赋值给`ArrayList` `words`。我们在第 134–135 行检索对应的置信度分数数组，并将其赋值给数组`scores`。在第 137–138 行，我们调用`MatchingUtility`类的`firstMatchWithMinConfidence`方法，以检索`words`中第一个与`enum Directions`中某个常量的`String`等效值匹配的元素。我们将其赋值给`String match`。注意，此时`match`可能为`null`。

![](img/ch10exa18.jpg) ![](img/ch10exa18a.jpg)

示例 10.18 `MapsActivity`类，Show A Map 应用，版本 5

根据`match`的值，我们更新地图中心并刷新地图。在第 139 行，我们检索地图的当前中心，并将其赋值给`LatLng`变量`pos`。在第 140 行，我们检索地图的当前缩放级别，并将其赋值给`float`变量`zoomLevel`。我们不打算在此应用中通过代码更改缩放级别，但我们的`updateMap`方法的第二个参数代表缩放级别。如果`match`不为`null`（第 142 行），我们根据`match`的值在第 143–150 行更新`pos`变量。如果`match`匹配枚举常量`NORTH`（第 143 行），我们在第 144 行将`pos`的纬度分量增加`DELTA`，以此类推。注意，为了修改`pos`所引用对象的纬度或经度，我们每次都需要重新实例化一个对象。这是因为`LatLng`类的`latitude`和`longitude`实例变量虽然是`public`的，但却是`final`的。因此，以下代码无法编译：

```java
pos.latitude = pos.latitude + DELTA;
```

一旦`pos`更新完毕，我们在第 152 行调用`updateMap`来重新绘制地图。我们在第 154 行调用`listen`，以允许用户输入更多语音输入；`listen`最初在第 97–98 行地图显示后被调用。

`listen`方法（在第 108–116 行编写）用于设置语音识别。它使用了表 10.18 中列出的`SpeechRecognizer`类的各种方法。它在第 111 行初始化`recognizer`，在第 112 行实例化一个`SpeechListener`对象，并在第 113 行将其注册到`recognizer`上。在第 114–115 行，我们调用`recognizer`的`startListening`方法，并向其传递一个语音识别类型的匿名`intent`。

### 表 10.18 `SpeechRecognizer`类的选定方法

| 方法 | 描述 |
| --- | --- |
| `static SpeechRecognizer createSpeechRecognizer(Context context)` | 静态方法，创建一个`SpeechRecognizer`对象并返回其引用。 |
| `void setRecognitionListener(RecognitionListener listener)` | 设置监听器，该监听器将接收所有回调方法调用。 |
| `void startListening(Intent intent)` | 开始监听语音。 |
| `void stopListening()` | 停止监听语音。 |
| `void destroy()` | 销毁此`SpeechRecognizer`对象。 |

表 10.18 `SpeechRecognizer`类的选定方法

![](img/9781284093650_CH10_FIGF10.jpg)

图 10.10 用户说出`North`后，在平板电脑中运行的“显示地图”应用第 5 版

图 10.10 显示了用户说出`Paris`然后`North`后，在平板电脑中运行的应用。注意，同样地，如果我们在几秒钟内没有说话，`onError`方法会被调用并返回语音超时错误，语音将不再被处理。如果我们想防止这种情况发生，可以添加一些逻辑来检测这种情况，并在发生时重新启动一个新的语音识别器。我们在第 6 版中实现了这一点。

## 10.9 语音识别第三部分：用语音连续移动地图，应用第 6 版

在应用的第 6 版中，我们希望持续监听用户，并在用户指示时不断更新地图，即使用户一段时间不说话。如果发生这种情况，`onError`方法会被调用，语音识别器停止监听，因此我们需要重新启动它。为此，我们在`onError`方法中调用`listen`方法（见示例 10.19 的第 129 行）。这样，我们就可以持续说话来更新地图。

![](img/ch10exa19.jpg)



# 示例 10.19：`MapsActivity` 类的 `onError` 方法，“显示地图”应用第 6 版

## 章节总结

- `RecognizerIntent` 类包含用于支持语音识别的常量，可用于创建意图。
- 要创建语音识别意图，我们使用 `ACTION_RECOGNIZE_SPEECH` 常量作为 `Intent` 构造函数的参数。
- 我们可以使用 `android.content.pm` 包中的 `PackageManager` 类来检索设备上安装的应用程序包的相关信息。
- `Context` 类中的 `getPackageManager` 方法返回一个 `PackageManager` 实例。
- 我们可以使用 `Intent` 类中的 `getStringArrayListExtra` 方法来检索语音识别器可能理解的可能单词列表。
- 我们可以使用 `Intent` 类中的 `getFloatArrayExtra` 方法来检索语音识别器可能理解的可能单词列表的置信度分数数组。
- 地图类不是标准 Android 开发工具包的一部分。如果 Android Studio 不是最新版本，可能需要下载并导入它们。此外，我们需要一个来自 Google 的密钥才能使用地图。
- 由于地图由地图瓦片组成，是从 Google 下载的，因此我们需要在 `AndroidManifest.xml` 文件中指定位置访问权限。
- 地图通常显示在片段（fragment）内。
- `com.google.android.gms.maps` 包包含许多有用的地图相关类，例如 `GoogleMap`、`CameraUpdate`、`CameraUpdateFactory`、`LatLng`、`CircleOptions`、`MarkerOptions` 等。
- `LatLng` 类封装了地球上的一个点，由其纬度和经度定义。
- `SpeechRecognizer` 类以及 `RecognitionListener` 接口（两者都属于 `android.speech` 包）允许我们在不使用图形用户界面的情况下监听和处理用户语音。

![](img/common.jpg)

## 练习、问题与项目

### 多项选择题

1. 我们使用哪个常量来创建语音识别的意图？
   - `ACTION _SPEECH`
   - `RECOGNIZE_SPEECH`
   - `ACTION_RECOGNIZE_SPEECH`
   - `ACTION_RECOGNITION_SPEECH`

2. 哪个类包含用于语音识别的常量？
   - `Activity`
   - `RecognizerIntent`
   - `Intent`
   - `Recognizer`

3. 为了从我们的语音中检索可能识别的单词，我们将问题 2 中类的哪个常量传递给 `Intent` 类的 `getStringArrayListExtra` 方法？
   - `RESULTS`
   - `EXTRA_RESULTS`
   - `RECOGNIZED_WORDS`
   - `WORDS`

4. 为了检索问题 3 中单词的置信度分数，我们将问题 2 中类的哪个常量传递给 `Intent` 类的 `getFloatArrayExtra` 方法？
   - `SCORES`
   - `EXTRA_CONFIDENCE_SCORES`
   - `CONFIDENCE_SCORES`
   - `CONFIDENCE_WORDS`

5. 我们可以使用哪个类来查明当前设备是否支持语音识别？
   - `Manager`
   - `PackageManager`
   - `SpeechRecognition`
   - `Intent`

6. 在 `AndroidManifest.xml` 文件中，我们使用哪个元素来表示此应用需要某些权限，例如访问互联网？
   - `need-permission`
   - `uses-permission`
   - `has-permission`
   - `permission-needed`

7. 我们可以使用哪个类根据点的地址检索该点的纬度和经度？
   - `Geocoder`
   - `Address`
   - `GetLatitudeLongitude`
   - `LatitudeLongitude`

8. `moveCamera` 和 `animateCamera` 方法位于哪个类中？
   - `Camera`
   - `CameraFactory`
   - `CameraUpdate`
   - `GoogleMap`

9. 哪个类封装了由纬度和经度定义的地球上的点？
   - `Point`
   - `EarthPoint`
   - `LatitudeLongitude`
   - `LatLng`

10. 我们可以使用哪些工具在没有用户界面的情况下监听语音？
    - `SpeechRecognizer` 类和 `RecognitionListener` 接口
    - `SpeechRecognizer` 接口和 `RecognitionListener` 类
    - `SpeechRecognizer` 类和 `RecognitionListener` 类
    - `SpeechRecognizer` 接口和 `RecognitionListener` 接口

### 填写代码

11. 编写一条语句来创建用于识别语音的意图。

12. 假设你已经创建了一个名为 `myIntent` 的 `Intent` 引用来识别语音，编写一条语句来启动一个活动（activity）。

13. 你在 `onActivityResult` 方法内执行，编写代码来检索捕获的语音有多少个可能的匹配单词。

```java
protected void onActivityResult( int requestCode, int resultCode,
                                 Intent data ) {
  // your code goes here

}
```

14. 你在 `onActivityResult` 方法内执行，编写代码来计算有多少个可能的匹配单词的置信度至少为 25%。

```java
protected void onActivityResult( int requestCode, int resultCode, 
                                 Intent data )
// your code goes here

}
```

15. 在 `AndroidManifest.xml` 文件中，编写一行代码，使此应用请求访问位置的权限。

16. 地图显示在屏幕上，我们有一个名为 `myMap` 的 `GoogleMap` 引用。编写代码将其缩放级别设置为 7。

17. 地图显示在屏幕上，我们有一个名为 `myMap` 的 `GoogleMap` 引用。编写代码移动地图，使其以纬度 75.6、经度-34.9 的点为中心。

18. 地图显示在屏幕上，我们有一个名为 `myMap` 的 `GoogleMap` 引用。编写代码移动地图，使其以地址 1600 Amphitheatre Parkway, Mountain View, CA 94043 的点为中心。

19. 地图显示在屏幕上，我们有一个名为 `myMap` 的 `GoogleMap` 引用。编写代码显示一个半径为 100 米、以地图中心为圆心的蓝色圆。

20. 地图显示在屏幕上，我们有一个名为 `myMap` 的 `GoogleMap` 引用。编写代码显示一个位于地图中心的标注。如果用户点击它，它会显示“WELCOME”。

21. 地图显示在屏幕上，我们有一个名为 `myMap` 的 `GoogleMap` 引用。使地图移动，使其中心的纬度增加 0.2，经度增加 0.3。

22. 你正在重写 `RecognitionListener` 接口的 `onResults` 方法。如果匹配的单词中有 NEW YORK，则在 Logcat 中输出 USA。

```java
public void onResults( Bundle results ) {
  // 你的代码写在这里

}
```

23. 你正在重写 `RecognitionListener` 接口的 `onResults` 方法。如果至少有一个匹配的单词的置信度达到 25%，则在 Logcat 中输出 YES。

```java
public void onResults( Bundle results ) {
  // 你的代码写在这里

}
```

### 编写一个应用

24. 编写一个应用，以缩放级别 14 显示你所在的城市，并添加两个圆和一个标注来突出显示感兴趣的内容。

25. 编写一个应用，显示你所在的城市，并使用不同于圆形或图钉的方式（例如，使用多边形）来突出显示某个感兴趣的地点（纪念碑、体育场等）。

26. 编写一个应用，要求用户在多个 `TextView` 中输入地址。当用户点击按钮时，应用显示以该地址为中心的地图。

27. 编写一个应用，要求用户在多个 `TextView` 中输入地址。当用户点击按钮时，应用显示以该地址为中心的地图。当用户说出一个数字时，地图会缩放到该级别。如果该数字不是有效级别，地图不发生变化。

28. 编写一个应用，它是一个游戏，运行方式如下：应用生成一个 1 到 10 之间的随机数，用户尝试通过语音输入猜出这个数字。用户有三次猜测机会，应用对每次猜测给出反馈。如果用户猜对或猜错（三次之后），则不允许用户再次说话。

29. 编写一个应用，在屏幕上的随机位置绘制你选择的颜色的圆。圆的半径应从语音输入中获取。

30. 编写一个应用，显示一个 3×3 的井字棋网格。如果用户说 `X`，则在网格的随机位置放置一个 X。如果用户说 `O`，则在网格的随机位置放置一个 O。

31. 编写一个应用，根据语音输入对某个形状或图像进行动画处理。如果用户说 `left`、`right`、`up` 或 `down`，则将该对象向左、右、上或下移动 10 像素。

32. 编写一个应用，它是一个从英语到另一种语言的迷你翻译器。至少包含 10 个翻译器能识别的单词。当用户说出一个英语单词时，应用显示翻译后的单词。

33. 编写一个应用，模拟猜单词游戏（hangman）。用户通过说出字母来一次猜一个字母。用户在使用七个错误字母（用于头、身体、两只手臂、两条腿和一只脚）后失败。

34. 编写一个应用，它是一个数学游戏。应用使用两个 1 到 9 之间的数字生成一个简单的加法算式。用户必须通过语音提交答案，应用检查答案是否正确。

35. 编写一个应用，它是一个数学游戏。首先，我们通过语音询问用户游戏应使用哪种运算：加法或乘法。然后应用使用两个 1 到 9 之间的数字生成一个简单的算式。用户必须通过语音提交答案，应用检查答案是否正确。

36. 编写一个应用，显示一个棋盘。应用启动时，所有方格都是黑白交替的颜色。当用户说出 `C8`（或其他方格）时，该方格变为红色。

37. 编写一个应用，允许用户通过语音玩井字棋游戏。包含一个 `Model`。

# 第十一章：使用 GPS 和定位服务

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

如今许多应用都使用 Android 设备的定位服务。其中一个应用是 Uber，人们用它来寻找付费出行的车辆。该应用使用设备的全球定位系统（GPS）来定位我们的位置，并找到附近已注册的司机。它利用卫星提供位置和时间信息。

## 11.1 访问 Google Play 服务，GPS 应用，版本 0

在这个应用中，我们打算获取设备的位置，向用户询问目的地，并计算到目的地的距离和时间。为了让应用能够使用 GPS 获取设备的位置，它需要访问 Google Play 服务。我们为此应用使用 Empty Activity 模板。在应用的版本 0 中，我们展示如何检查设备是否可以访问 Google Play 服务。我们需要执行以下操作：

- 编辑 `build.gradle` 文件，以便在编译过程中包含 Google Play 服务。
- 编辑 `MainActivity` 类，以便访问 Google Play 服务。

示例 11.1 展示了 `build.gradle`（Module: app）文件。我们对其进行编辑，以使 Google Play 服务库对应用可用（注意有两个 `build.gradle` 文件）。唯一的添加在第 26 行：我们包含了适当版本的 Google Play 服务库。在撰写本文时，该版本为 9.4.0。

![](img/ch11exa01.jpg)

示例 11.1 `build.gradle`（Module: app）文件

编辑 `build.gradle` 文件后，我们应该点击工具栏上的“Sync Project with Gradle Files”图标，如图 11.1 所示。

在 `MainActivity` 类内部，我们执行以下操作：

- 尝试从设备访问 Google Play 服务。
- 如果无法访问且问题可以解决，则尝试解决。否则，退出应用。
- 获取当前位置并显示。

![](img/9781284093650_CH11_FIGF01.jpg)

图 11.1 “Sync Project with Gradle Files”图标

| 方法 | 描述 |
| --- | --- |
| `GoogleApiClient.Builder( Context context )` | 构造一个 `GoogleApiClient` 对象。 |
| `GoogleApiClient.Builder addConnectionCallbacks( GoogleApiClient.ConnectionCallbacks listener )` | 注册监听器以接收连接事件。返回此 `GoogleApiClient.Builder` 引用，以便方法调用可以链式进行。 |
| `GoogleApiClient.Builder addOnConnectionFailedListener( GoogleApiClient.ConnectionFailedListener listener )` | 注册监听器以接收连接失败事件。返回此 `GoogleApiClient.Builder` 引用，以便方法调用可以链式进行。 |
| `GoogleApiClient.Builder addApi( API<? extends Api.ApiOptions.NotRequiredOptions> api )` | 指定 `api` 作为此应用请求的 API。应使用 `LocationServices` 的 API 常量。返回此 `GoogleApiClient.Builder` 引用，以便方法调用可以链式进行。 |
| `GoogleApiClient build( )` | 构建并返回一个用于与 Google API 通信的 `GoogleApiClient` 对象。 |

表 11.1 `GoogleApiClient.Builder` 类的选定方法

`GoogleApiClient` 抽象类（来自 `com.google.android.gms.common.api` 包）是 Google Play 服务的主要入口点。它包含建立和管理与 Google Play 服务连接的功能。由于它是 `abstract` 的，我们不能使用 `new` 运算符实例化该类的对象。它包含一个 `static` 内部类 `Builder`，该类包含用于指定 `GoogleApiClient` 属性的方法以及一个用于创建 `GoogleApiClient` 的 `build` 方法。表 11.1 列出了其中一些方法。除了 `build` 方法外，这些方法都返回调用它们的 `GoogleApiClient.Builder` 引用，以便方法调用可以链式进行。`build` 方法返回一个 `GoogleApiClient` 引用。

`GoogleApiClient` 类包含 `ConnectionCallbacks` 和 `OnConnectionFailedListener` 这两个静态内部接口。`ConnectionCallbacks` 提供了当我们连接或断开 Google 服务时自动调用的回调方法。`OnConnectionFailedListener` 提供了一个在连接尝试失败时自动调用的回调方法。表 11.2 列出了它们。`onConnectionSuspended` 方法的 `int` 参数可以与 `ConnectionCallbacks` 接口的 `CAUSE_SERVICE_DISCONNECTED` 和 `CAUSE_NETWORK_LOST` 常量进行比较，以确定断开连接的原因。

| 接口 | 方法 | 描述 |
| --- | --- | --- |
| `ConnectionCallbacks` | `void onConnected( Bundle connectionHint)` | 在通过使用 `GoogleApiClient` 引用调用 `connect` 方法发起的连接请求成功完成后自动调用。 |
| `ConnectionCallbacks` | `void onConnectionSuspended(int cause)` | 当连接丢失时自动调用。`GoogleApiClient` 对象将自动尝试恢复连接。 |



| `OnConnectionFailedListener` | `void onConnectionFailed(ConnectionResult result)` | 当连接到服务时发生错误时自动调用。 |

表 11.2 `ConnectionCallbacks` 和 `OnConnectionFailedListener` 接口及其方法

因此，假设我们在一个实现了 `ConnectionCallbacks` 和 `OnConnectionFailedListener` 接口的 `Activity` 类中，我们可以使用以下序列实例化一个 `GoogleApiClient` 对象：

```java
// 假设我们在一个 Activity 类中，并且它
// 实现了 ConnectionCallbacks 和 OnConnectionFailedListener
GoogleApiClient.Builder builder = new GoogleApiClient.Builder(this);
builder.addConnectionCallbacks(this);
builder.addOnConnectionFailedListener(this);
builder.addApi(LocationServices.API);
GoogleApiClient gac = builder.build();
```

由于我们在一个 `Activity` 类中，我们可以使用 `this` 作为 `GoogleApiClient.Builder` 构造函数的参数。由于 `Activity` 类实现了这两个接口，我们也可以使用 `this` 作为 `addConnectionCallbacks` 和 `addOnConnectionFailedListener` 的参数。我们使用 `LocationServices` 类的 `API` 常量（如表 11.3 所示）作为 `addApi` 方法的参数。或者，由于这三个方法返回调用它们的 `GoogleApiClient.Builder` 引用，我们可以链式调用方法，如下所示：

```java
GoogleApiClient gac = new GoogleApiClient.Builder(this)
                   .addConnectionCallbacks(this)
                   .addOnConnectionFailedListener(this)
                   .addApi(LocationServices.API).build();
```

| 常量 | 描述 |
| --- | --- |
| `API` | 一个常量，应在构建 `GoogleApiClient` 的过程中传递给 `GoogleApi.Builder` 类的 `addApi` 方法。 |
| `FusedLocationAPI` | 类型为 `FusedLocationProviderAPI` 的静态常量，该接口包含检索设备位置和管理位置更新的方法。 |

表 11.3 `LocationServices` 类的选定字段

| 方法 | 描述 |
| --- | --- |
| `void connect()` | 建立与 Google Play 服务的连接。如果成功，则调用 `ConnectionCallbacks` 的 `onConnected` 方法。如果不成功，则调用 `onConnectionFailed`。 |
| `void disconnect()` | 关闭与 Google Play 服务的连接。 |

表 11.4 `GoogleApiClient` 类的选定方法

一旦我们有了一个 `GoogleApiClient` 引用，并假设其名称为 `gac`，我们可以通过调用 `GoogleApiClient` 的 `connect` 方法（如表 11.4 所示）来尝试建立连接，如下代码所示：

```java
// 假设 gac 是一个 GoogleApiClient 引用
gac.connect();
```

如果连接成功，`ConnectionCallbacks` 接口的 `onConnected` 方法会自动调用。在该方法内部，我们可以检索设备的位置。

如果设备无法连接到 Google Play 服务，则会调用 `onConnectionFailed` 回调方法。我们想检查该问题是否可以解决（例如，设备上可能需要更新 Google Play 服务）。我们可以通过使用 `onConnectionFailed` 的 `ConnectionResult` 参数调用 `hasResolution` 方法来做到这一点。如果该方法返回 `false`，则问题无法解决，我们可以退出应用。如果该方法返回 `true`，则问题可以解决，我们想尝试解决它。我们可以通过调用 `ConnectionResult` 的 `startResolutionForResult` 方法来做到这一点。表 11.5 显示了这两个方法。这需要用户交互。结束后，将调用 `Activity` 类的 `onActivityResult` 方法。在该方法内部，我们可以检查问题是否已解决。如果已解决，我们可以再次尝试连接到 Google Play 服务。

| 方法 | 描述 |
| --- | --- |
| `boolean hasResolution()` | 如果存在可以启动以尝试解决连接问题的解决方案，则返回 `true`。 |
| `void startResolutionForResult(Activity activity, int requestCode)` | 启动一个意图以尝试解决连接问题。这需要用户交互。 |

表 11.5 `ConnectionResult` 类的选定方法

我们可以用以下伪代码实现这一点：

```text
// 在 onConnectionFailed 方法内部
if (问题有可行的解决方案)
  调用 startResolutionForResult 尝试解决
else
  退出应用

// 在 onActivityResult 内部
if (问题已解决)
  再次尝试连接
```

示例 11.2 展示了 `MainActivity` 类。它实现了 `ConnectionCallbacks` 和 `OnConnectionFailedListener` 接口（第 14–15 行）。我们在第 18 行声明了一个 `GoogleApiClient` 实例变量。我们在第 25–28 行实例化它。`onStart` 方法在 `onCreate` 执行后自动调用。如果 `gac` 不为 `null`（第 66 行），我们在第 67 行尝试建立连接。如果成功，这将触发对 `onConnected` 方法的调用（第 31–34 行）。在这个版本中，我们只是向 Logcat 输出一些反馈。如果连接尝试失败，我们会在 `onConnectionFailed` 内部执行（第 41–54 行）。在第 44 行，我们测试该问题是否有可行的解决方案。如果有，我们在第 46 行尝试启动一个活动来解决它。如果不能，我们在显示一个 `Toast` 后退出应用（第 48–51 行）。如果我们成功启动了一个活动来尝试解决连接问题，并且在用户交互之后，应用将在 `onActivityResult` 方法内部恢复执行（第 56–62 行）。如果解决方案成功（第 58 行），我们在第 60 行再次尝试连接到 Google Play 服务。

![](img/ch11exa02.jpg)

示例 11.2 `MainActivity` 类，GPS 应用，版本 0

运行 GPS 应用版本 0 时，Logcat 中的输出显示我们已连接。

## 11.2 使用 GPS 检索我们的位置，GPS 应用，版本 1

在版本 1 中，我们检索设备的位置并将其显示在 `TextView` 中。由于应用访问 GPS，它在模拟器中无法工作，尽管我们可以使用模拟器硬编码经纬度数据。要使用我们当前的位置，我们需要在设备上运行它。因为应用使用了 Google 的位置服务，我们需要在 `AndroidManifest.xml` 文件中指定这一点。因此，我们需要执行以下操作：

- ▸ 在 `AndroidManifest.xml` 文件中，指定我们使用位置服务，并添加关于此应用使用的 Google Play 服务版本的元数据。
- ▸ 在 `MainActivity` 类内部，捕获我们当前的位置并显示它。

示例 11.3 展示了 `AndroidManifest.xml` 文件。在第 5–6 行，我们指定该应用访问设备的近似位置。`Manifest.permission` 类的 `ACCESS_COARSE_LOCATION` 和 `ACCESS_FINE_LOCATION String` 常量可分别用于指定近似位置或精确位置。在第 15–17 行，我们指定该应用使用的 Google Play 服务版本。为简化起见，我们只允许应用在竖屏模式下运行（第 20 行）。

在 `MainActivity` 类中，我们执行以下操作：

- ▸ 与 Google Play 服务建立连接。
- ▸ 获取位置。
- ▸ 显示位置。

`Location` 类属于 `android.location` 包，封装了地球上的一个地理位置。位置通常由其纬度和经度标识。表 11.6 列出了 `Location` 类的一些方法。注意，`Location` 类使用公制系统，通过方法计算的距离以米为单位返回。

`FusedLocationProviderApi` 接口的 `lastLocation` 方法以 `Location` 引用的形式返回设备的当前位置。它接受一个 `GoogleApiClient` 参数，如表 11.7 所示。我们使用此方法获取设备的位置。因此，要调用该方法，我们需要一个 `FusedLocationProviderApi` 引用来调用它，以及一个 `GoogleApiClient` 引用作为其唯一参数传递。如表 11.3 所示，`LocationServices` 类（属于 `com.google.android.gms.location` 包）包含一个名为 `FusedLocationApi` 的 `FusedLocationProviderApi` 常量。因此，假设我们有一个名为 `gac` 的 `GoogleApiClient` 引用，我们可以使用以下序列获取当前位置：

```java
// 假设 gac 是一个 GoogleApiClient 引用
FusedLocationProviderApi flpa = LocationServices.FusedLocationApi;
Location location = flpa.getLastLocation(gac);
```

![](img/ch11exa03.jpg)

示例 11.3 `AndroidManifest.xml` 文件

| 方法 | 描述 |
| --- | --- |
| `double getLatitude()` | 返回此位置的纬度。 |
| `double getLongitude()` | 返回此位置的经度。 |
| `float getAccuracy()` | 返回此位置的精度，单位为米。 |
| `float distanceTo(Location destination)` | 返回此位置与目标位置之间的距离，单位为米。 |

表 11.6 `Location` 类的部分方法

| 方法 | 描述 |
| --- | --- |
| `Location getLastLocation(GoogleApiClient gac)` | 返回最近的位置，如果没有可用位置则返回 `null`。 |

表 11.7 `FusedLocationProviderApi` 接口的 `getLastLocation` 方法

一旦我们获得了当前位置的 `Location` 引用，就可以通过调用 `getLatitude` 和 `getLongitude` 方法来获取该位置的纬度和经度，如下所示：

```java
double latitude = location.getLatitude();
double longitude = location.getLongitude();
```

示例 11.4 展示了 `MainActivity` 类。我们在第 23–24 行声明了两个额外的实例变量：`location`（一个 `Location` 对象，用于存储当前位置）和 `locationTV`（一个 `TextView`，用于显示位置）。在 `onCreate` 中，我们在第 30 行实例化 `TextView`。这假设 `activity_main.xml` 中有一个 `id` 为 `location_tv` 的 `TextView`。在 `onConnected` 方法中，我们在第 52 行调用 `displayLocation` 方法。`displayLocation` 方法（第 38–48 行）在第 39–40 行获取当前设备位置。如果位置不为 `null`（第 41 行），我们获取其纬度和经度，在 `TextView` 中显示它们（第 44 行），并将它们输出到 Logcat（第 45 行）。

![](img/ch11exa04.jpg) ![](img/ch11exa04a.jpg)

示例 11.4 `MainActivity` 类，GPS 应用，版本 1

示例 11.5 展示了 `activity_main.xml` 文件。`TextView` 的 `id` 在第 13 行分配。示例 11.6 展示了 `styles.xml` 文件，其中在第 5 行指定了字体大小为 22。

图 11.2 展示了应用在 Logcat 中的输出，显示了纬度和经度数据。注意，我们必须在一台已连接的设备（具有 GPS）上运行此应用，而不是模拟器。

![](img/ch11exa05.jpg)

示例 11.5 `activity_main.xml` 文件，GPS 应用，版本 1

![](img/ch11exa06.jpg)

示例 11.6 `styles.xml` 文件，GPS 应用，版本 1

![](img/9781284093650_CH11_FIGF02.jpg)

图 11.2 GPS 应用版本 1 的 Logcat 输出

## 11.3 到目的地的距离和时间模型

在版本 2 中，我们要求用户输入目的地的地址，并提供一个按钮来显示到目的地的剩余距离和时间。在构建 GUI 及其控制器之前，我们添加了 `TravelManager` 类，即应用的模型，如示例 11.7 所示。它包含一个 `Location` 实例变量来存储目的地（第 9 行），以及计算从当前位置到目的地位置的距离和剩余时间的方法。为简化应用，我们假设用户以每小时 `55` 英里的速度行驶（第 6 行）。

![](img/ch11exa07.jpg)

示例 11.7 `TravelManager` 类，GPS 应用，版本 2

在 `distanceToDestination` 方法（第 15–21 行）中，我们调用表 11.6 中所示的 `Location` 类的 `distanceTo` 方法，以计算其 `Location` 参数与 `destination` 之间的距离。如果其中一个为 `null`，则返回 `–1`。否则，返回它们之间的距离。`milesToDestination` 方法（第 23–31 行）将该距离转换并返回为表示英里数的 `String`。

`timeToDestination` 方法（第 33–54 行）计算并返回从其 `Location` 参数到目的地所需的时间，假设速度为每小时 `55` 英里。在第 35–36 行，我们计算从其 `Location` 参数到目的地的距离（以米为单位）。在第 37–38 行，我们计算以每小时 `55` 英里的速度行驶该距离所需的时间（以小时为单位，`float` 类型）。然后，我们在第 40–52 行将该值转换为 `String result`，表示小时数和分钟数。注意，如果时间为 `0` 或负数（第 51 行），我们在第 52 行将 `less than a minute left` 赋值给 `result`。

## 11.4 到目的地的距离和时间，GPS 应用，版本 2

我们在 GUI 中包含以下元素，全部居中并垂直排列：

- ▸ 一个 `EditText`，用于用户输入目的地地址。
- ▸ 两个 `TextViews`，用于显示到目的地的距离和时间。
- ▸ 一个 `Button`：当用户点击它时，我们更新两个 `TextViews` 中的距离和时间。

示例 11.8 展示了更新后的 `activity_main.xml` 文件。我们为所有元素赋予 `id`（第 13、18、23、28 行），以便在 `MainActivity` 类中根据需要定位和检索它们。我们希望为所有元素的宽度和高度指定 `WRAP_CONTENT` 值。我们还希望它们之间有 `20` 像素的间距并水平居中。因此，我们在 `styles.xml` 中定义了 `WrappedAndCentered` 样式（示例 11.9 的第 11–16 行），并将其用于所有四个元素（第 15、20、25、32 行）。我们在第 14 行为 `EditText` 指定了一个提示 `Enter destination`，该提示在 `strings.xml` 文件中定义（示例 11.10 的第 3 行）。在第 30 行，我们将按钮内的文本定义为 `String Update`，在示例 11.10 的第 4 行定义。在第 31 行，我们指定当用户点击 `Button` 时调用 `updateTrip` 方法。

![](img/ch11exa08.jpg)

示例 11.8 `activity_main.xml` 文件，GPS 应用，版本 2

在 `MainActivity` 类内部，我们需要进行以下修改：

- ▸ 添加适当的导入语句。
- ▸ 添加一个 `TravelManager` 实例变量，以便访问模型的功能。
- ▸ 为 GUI 中的 `EditText` 和两个 `TextViews` 添加实例变量，并添加一个 `String` 来存储目的地地址。
- ▸ 删除 `displayLocation` 方法：我们不再需要显示当前位置。
- ▸ 添加 `updateTrip` 方法。
- ▸ 删除 `onConnected` 方法的主体：我们希望等待用户输入目的地地址后再执行任何操作。



![](img/ch11exa09.jpg)

示例 11.9 `styles.xml` 文件，GPS 应用，版本 2

![](img/ch11exa10.jpg)

示例 11.10 `strings.xml` 文件，GPS 应用，版本 2

示例 11.11 展示了更新后的 `MainActivity` 类。我们在第 29–33 行声明了额外的五个实例变量。`TravelManager` 和三个 GUI 组件在第 39–42 行的 `onCreate` 方法中实例化。在 `updateTrip` 方法（第 50–79 行）中，我们获取用户输入，必要时更新模型，调用模型的方法计算到目的地的距离和剩余时间，并相应地更新视图。

![](img/ch11exa11.jpg) ![](img/ch11exa11a.jpg)

示例 11.11 `MainActivity` 类，GPS 应用，版本 2

我们首先在第 51 行获取用户输入的目的地地址。如果目的地地址与当前目的地地址不同（第 53 行），则更新当前目的地地址（第 54 行）。然后，我们尝试将其地理编码为 `Location` 对象（第 57–59 行）。地理编码是将街道地址转换为（纬度，经度）坐标的过程。表 11.8 展示了 `Geocoder` 类的一个构造函数和一个 `getFromLocationName` 方法。如果地理编码成功（第 60 行），我们将该 `Location` 赋值给 `TravelManager` 的 `destination` 实例变量。我们通过状态变量 `goodGeocoding` 来跟踪地理编码是否成功。我们在第 52 行将其初始化为 `true`，如果进入第 69 行的 `catch` 块，则将其切换为 `false`。我们在第 73–74 行获取当前位置。如果成功获取当前位置且地理编码成功（第 75 行），则在第 76–77 行更新显示距离和剩余时间的两个 `TextViews`。`manager` 实例变量调用 `milesToDestination` 和 `timeToDestination` 方法，并传入当前位置。

| 方法 | 描述 |
| --- | --- |
| `Geocoder(Context context)` | 构造一个 `Geocoder`。 |
| `List<Address> getFromLocationName(String locationName, int maxResults)` | 返回与 `locationName` 匹配的 `Address` 对象列表。抛出 `IllegalArgumentException` 和 `IOException`。 |

表 11.8 `Geocoder` 类的选定方法

![](img/9781284093650_CH11_FIGF03.jpg)

图 11.3 GPS 应用，版本 2，在平板电脑上运行

图 11.3 展示了用户输入白宫地址并点击更新后，应用在平板电脑上运行的情况。

## 11.5 更新到目的地的距离和时间，GPS 应用，版本 3

在版本 3 中，我们希望自动更新到目的地的距离和剩余时间，而无需点击 `Update` 按钮。我们保留 `Update` 按钮，以便用户需要即时更新时使用。因此，用户界面与版本 2 相同。

`com.google.android.gms.location` 包中的 `LocationListener` 接口提供了一个回调方法 `onLocationChanged`，该方法会根据各种指定参数（如频率和移动距离）自动调用，如表 11.9 所示。这与事件处理非常相似；我们需要执行以下操作：

- ▸ 创建一个实现 `LocationListener` 的私有类，并重写 `onLocationChanged`。
- ▸ 声明并实例化该类的对象。
- ▸ 将该对象注册到融合位置提供器（一个 `FusedLocationProviderApi` 引用）上。

| 方法 | 描述 |
| --- | --- |
| `void onLocationChanged(Location location)` | 根据 `LocationRequest` 的定义自动调用的回调方法；`location` 表示最近的位置。 |

表 11.9 `LocationListener` 类的 `onLocationChanged` 方法

| 方法 | 描述 |
| --- | --- |
| `PendingResult requestLocationUpdates(GoogleApiClient gap, LocationRequest request, LocationListener listener)` | 请求 `listener` 根据 `request` 监听位置更新。 |
| `PendingResult removeLocationUpdates(GoogleApiClient gap, LocationListener listener)` | 停止 `listener` 的位置更新。 |

表 11.10 `FusedLocationProviderApi` 接口的选定方法

或者，我们可以执行以下操作：

- ▸ 让我们的 `Activity` 类实现 `LocationListener`，并重写 `onLocationChanged`。
- ▸ 将 `this` 注册到融合位置提供器（一个 `FusedLocationProviderApi` 引用）上。

我们选择实现第二种策略。表 11.10 展示了 `FusedLocationProviderApi` 接口的一个 `requestLocationUpdates` 方法。它请求其 `LocationListener` 参数根据 `LocationRequest` 参数的定义，通过 `onLocationChanged` 方法提供位置更新。因此，假设我们在一个实现了 `LocationListener` 接口的 `Activity` 类内部，并且已经定义了一个名为 `request` 的 `LocationRequest`，我们可以使用以下代码序列请求位置更新：

```java
// 我们在一个实现了 LocationListener 的 Activity 类内部
// 因此，this "是一个" LocationListener
// gac 是一个 GoogleApiClient 引用
// request 是一个 LocationRequest 引用
FusedLocationProviderApi flpa = LocationServices.FusedLocationApi;
flpa.requestLocationUpdates(gac, request, this);
```

| 方法 | 描述 |
| --- | --- |
| `LocationRequest setInterval(long ms)` | 设置位置更新的间隔（毫秒）。返回此 `LocationRequest`，以便可以链式调用方法。 |
| `LocationRequest setPriority(int priority)` | 设置此请求的优先级。`LocationRequest` 类包含可用作参数的常量（见表 11.12）。返回此 `LocationRequest`，以便可以链式调用方法。 |
| `LocationRequest setSmallestDisplacement(float meters)` | 设置连续更新之间的最小距离。返回此 `LocationRequest`，以便可以链式调用方法。 |

表 11.11 `LocationRequest` 类的选定方法

此时，我们将收到更新，并且 `onLocationChanged` 方法将按照 `LocationRequest` 指定的频率被调用。其 `Location` 参数存储最近的位置，如下所示：

```java
public void onLocationChanged(Location location) {
    // location 是最近的位置
}
```

`LocationRequest` 类提供了定义位置更新请求的功能，通过指定更新频率、精度等参数。

表 11.11 展示了 `LocationRequest` 类中两个最重要的方法。我们使用 `setInterval` 方法来指定位置更新的期望频率，单位为毫秒。位置更新会消耗电量，频繁更新可能会耗尽设备电池。我们使用 `setPriority` 方法来指定期望的精度级别，这实际上是对使用何种来源（GPS 或 Wi-Fi 和基站）的提示。然而，其他因素（例如当前位置、此类来源的可用性以及设备本身）可能会影响返回位置的精度。`LocationRequest` 类的所有 `set` 方法都会返回调用它们的 `LocationRequest` 引用，因此我们可以链式调用方法。如果我们不希望更新（例如，如果移动距离未达到最小值），我们可以使用 `setSmallestDisplacement` 方法，并指定两次连续更新之间的最小距离。例如，在旅行应用中，如果用户因交通堵塞而静止不动，则不需要距离更新。

以下代码序列展示了如何定义 `LocationRequest`：

```java
LocationRequest request = new LocationRequest();
request.setInterval(30000); // 30 秒间隔
request.setPriority(LocationRequest.PRIORITY_HIGH_ACCURACY);
request.setSmallestDisplacement(100); // 最小 100 米
```

表 11.12 展示了 `LocationRequest` 类的常量，我们可以将其用作 `setPriority` 方法的参数。请求的精度越高，电池消耗越大。如果不通过调用 `setPriority` 专门设置优先级，则使用由 `PRIORITY_BALANCED_POWER_ACCURACY` 定义的默认优先级。如果我们构建一个测量到球洞距离的高尔夫应用，我们希望精度达到最近的码或米，因此我们指定最高可能的精度。对于这个旅行应用，默认精度就足够了。

| 常量 | 值 | 描述 |
| --- | --- | --- |
| `PRIORITY_HIGH_ACCURACY` | 100 | 最高可用精度。 |
| `PRIORITY_BALANCED_POWER_ACCURACY` | 102 | 默认值——街区级精度，约 100 米。 |
| `PRIORITY_LOW_POWER` | 104 | 城市级精度，约 10 公里。 |
| `PRIORITY_NO_POWER` | 105 | 最差精度，不消耗电量。 |

表 11.12 `LocationRequest` 类的优先级常量

示例 11.12 展示了 `MainActivity` 类中的更改。我们只希望在成功连接后设置位置更新。因此，我们在 `onConnected` 方法内部执行此操作（第 98–108 行）。我们在第 100–103 行创建并定义了一个 `LocationRequest`。我们添加了对 `setPriority` 和 `setSmallestDisplacement` 的调用以进行说明，但将它们注释掉了。实际上，如果我们在不移动的情况下测试应用，我们不想为位置更新设置最小距离。实际上，我们有可能在 `onConnected` 方法执行过程中断开连接，在这种情况下，当我们尝试设置位置更新时应用会崩溃。因此，我们在设置位置更新（第 105 行）之前测试是否已连接（第 104 行）。如果连接丢失，我们会尝试建立另一个连接（第 107 行）。

在 `onLocationChanged` 方法内部（第 54–59 行），我们在第 58 行调用 `updateTrip`，以更新显示到目的地的距离和剩余时间的两个 `TextView`。作为反馈，我们将关于精度和自动调用 `onLocationChanged` 的时间线的信息输出到 Logcat。表 11.13 展示了 `getAccuracy` 和 `getElapsedRealtimeNanos` 方法。`getElapsedRealtimeNanos` 方法需要 API 级别 17。因此，我们相应地更新 `build.gradle` 文件。

如果应用正在运行并进入后台，我们希望停止请求位置更新。当这种情况发生时，会自动调用 `onPause` 方法（第 92–96 行）。我们在第 95 行通过调用 `removeLocationUpdates` 方法（如表 11.10 所示）来禁用位置更新。当应用回到前台时，会调用 `onStart`，必要时重新连接到 Google Play 服务，并在执行 `onConnected` 时再次请求位置更新。

图 11.4 展示了应用在作者平板电脑上运行时的 Logcat 输出。输出显示 GPS 返回的位置精度可能因测量而异。在此实例中，精度从 30 米到 64.5 米不等。1 纳秒等于 `10^(–9)` 秒。测量的间隔频率始终非常接近指定的 30 秒。它在 30.016 秒（最后一次与倒数第二次测量之间的时间）和 30.034 秒（第三次与第四次测量之间的时间）之间变化。当应用启动时，两个 `TextView` 显示 `0 mile` 和 `seconds left`。如果我们输入一个地址并等待，到该位置的距离和时间会在不到 30 秒内自动更新，无需点击 `Update` 按钮，这表明 `onLocationChanged` 方法已被调用。

![](img/ch11exa12.jpg)

示例 11.12 `MainActivity` 类，GPS 应用，版本 3

| 方法 | 描述 |
| --- | --- |
| `float getAccuracy()` | 返回此位置的精度，单位为米。 |
| `long getElapsedRealtimeNanos()` | 返回自上次启动以来的时间，单位为纳秒。 |

表 11.13 `Location` 类的选定方法

![](img/9781284093650_CH11_FIGF04.jpg)

图 11.4 GPS 应用（版本 3）在平板电脑上运行时的 Logcat 输出

精度也可能取决于设备和位置。在作者家中对平板电脑的进一步测试显示，当使用 `PRIORITY_HIGH_ACCURACY` 设置优先级时（通过取消注释示例 11.12 中的第 102 行），精度从 12 米到 36 米不等。

## 章节总结

- `GoogleApiClient` 类是 Google Play 服务的入口点。
- 如果 Google Play 服务不可用，则有可能通过用户交互使其可用。
- `GoogleApiClient` 的 `Builder` 静态内部类使我们能够构建一个 `GoogleApiClient`。
- 我们可以通过调用 `FusedLocationProviderApi` 接口的 `lastLocation` 方法来获取设备的当前位置。
- `LocationServices` 有一个名为 `FusedLocationApi` 的 `FusedLocationProviderApi` 静态常量字段。
- `Location` 类的 `getLatitude` 和 `getLongitude` 方法返回位置的纬度和经度。
- `Location` 类的 `distanceTo` 方法返回调用它的 `Location` 引用与参数 `Location` 引用之间的距离，单位为米。
- 如果应用访问 Google Play 服务以检索设备位置，我们应在 `AndroidManifest.xml` 文件中添加一个 `uses-permission` 元素，并指定 `ACCESS_COARSE_LOCATION` 或 `ACCESS_FINE_LOCATION`，这两个是 `Manifest.permission` 类的常量。
- `Geocoder` 类提供了将地址转换为 `Location` 对象（即纬度和经度）以及反向转换的方法。
- 我们可以通过实现 `LocationListener` 接口来定期获取位置更新。`LocationListener` 包含一个回调方法 `onLocationChanged`。它接受一个 `Location` 参数，表示设备的当前位置。
- 我们使用 `requestLocationUpdates` 方法在 `FusedLocationProviderApi` 上注册一个 `LocationListener`，并使用 `LocationRequest` 参数定义更新的各种参数。这种注册会触发对 `LocationListener` 的 `onLocationChanged` 方法的自动调用。
- `LocationRequest` 最重要的属性是更新频率和优先级，后者转化为检索到的位置的精度。

![](img/common.jpg)

## 练习、问题和项目

### 多项选择题

1. 如何获取 `GoogleApiClient` 引用？
   - 使用 `GoogleApiClient` 的构造函数
   - 使用 `GoogleApiClient` 的 `getInstance` 方法
   - 创建 `GoogleApiClient.Builder` 并调用 `build` 方法
   - 无法获取

2. `LocationServices` 中 `FusedLocationProviderApi` 常量的名称是什么？
   - `Api`
   - `FusedLocationApi`
   - `FusedApi`
   - `Fused`

3. `Location` 类封装了地球上的一个位置。我们可以使用哪个方法来获取其纬度？
   - `latitude`
   - `getLat`
   - `getLatitude`



* `locationLatitude`

4. `Location` 类的 `distanceTo` 方法返回的距离单位是：

   * 码
   * 米
   * 英里
   * 千米

5. 哪个类包含将地址转换为 `Location` 以及反向转换的方法？

   * `Geocoder`
   * `LocationCoder`
   * `Mapping`
   * `Geography`

6. 如果我们希望以固定间隔获取位置更新，应该实现哪个接口？

   * `Listener`
   * `UpdateListener`
   * `GeoListener`
   * `LocationListener`

7. 问题 6 中接口的 `onLocationChanged` 方法的 `Location` 参数的含义是什么？

   * 它存储一个随机位置
   * 它存储最近的位置
   * 它存储下一个位置
   * 它是 `null`

8. 我们调用 `FusedLocationProviderApi` 接口的 `requestLocationUpdates` 方法来请求定期位置更新。其中两个参数是 `GoogleApiClient` 和 `LocationListener`。第三个参数的类型是什么？

   * `double`
   * `Request`
   * `Time`
   * `LocationRequest`

### 填写代码

9. 声明并实例化一个 `GoogleApiClient`，用于监听连接成功和失败。

10. `Location` 引用 `myLocation` 存储了一个位置。将其精度输出到 Logcat。

11. `String` 地址 `address` 存储了一个地址。将其纬度和经度输出到 Logcat。使用第一个地理编码的 `Address`。

12. `MyActivity` 类希望获取位置更新。编写其类头。

13. 编写 `onLocationChanged` 方法，以便在名为 `MyTV` 的 `TextView` 中显示当前位置的纬度和经度。

14. 构建一个 `LocationRequest`，用于每 100 秒以最高可能精度触发更新。

15. 我们在一个实现了 `LocationListener` 的 `Activity` 类中编码。我们已经实例化了一个名为 `providerApi` 的 `FusedLocationProviderApi`、一个名为 `clientApi` 的 `GoogleClientApi` 和一个名为 `request` 的 `LocationRequest`。编写一条语句，以便在此 `Activity` 类中按照 `request` 的定义获取位置更新。

### 编写一个应用

16. 扩展本章中的应用，使用最后两次位置更新之间的速度（而不是每小时 55 英里）来计算剩余时间。

17. 扩展本章中的应用，使用最后五次位置更新之间的平均速度（而不是每小时 55 英里）来计算剩余时间。如果尚未有五次位置更新，则使用每小时 55 英里。

18. 编写一个应用，从五个位置中识别出离用户最近的位置。这五个位置可以在应用的模型中硬编码。

19. 编写一个应用，识别用户与五个位置之间的距离。这五个位置可以在应用的模型中硬编码。随着用户移动，五个距离应定期更新。应用应允许用户决定更新的频率和位置的精度（优先级）。

20. 编写一个应用，使用户能够从列表中选择一个朋友，检索其地址，并计算该朋友的距离。列表可以存储在文件中，也可以硬编码。包含一个模型。

21. 与 20 相同，但列表不是硬编码的，而是持久化且可扩展的。用户可以添加到列表中。

22. 与 21 相同，但用户还可以从列表中删除和更新朋友的数据。

23. 编写一个 1 洞高尔夫应用。该应用允许用户通过点击按钮来输入果岭中心的位置。该数据应存储在设备上。应用允许用户计算从当前位置到果岭中心位置（之前存储的）的距离。

24. 与 23 相同，但该应用是一个 18 洞高尔夫应用，而不是 1 洞高尔夫应用。

25. 编写一个应用，在设备上存储位置和描述的列表。用户可以为某个位置（用户所在位置）输入描述，并可以点击按钮检索当前位置，然后将描述和位置写入设备存储。该应用还允许用户检索描述和位置的列表并显示它们。

26. 编写一个应用，发送一封电子邮件，并在邮件正文中包含用户位置的纬度和经度。

27. 与 26 相同，但将当前位置转换为地址，并在邮件正文中包含当前地址。

28. 编写一个应用，帮助用户检索其汽车的停车位置。当用户停车时，用户点击一个按钮来存储汽车的位置。如果用户想知道汽车在哪里，应用会显示一个带有两个圆圈的地图，分别显示汽车和用户的位置。

# 第十二章：在应用内使用另一个应用：拍照、灰度处理并发送电子邮件

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

一个应用可以启动另一个应用并处理其结果。应用之间相互通信并使用设备上的其他应用变得越来越常见。例如，我们可能想要访问某个应用的电话簿，或者查找照片或视频。照片应用在智能手机用户中非常流行。它们包括将彩色图片转换为黑白图片、为图片添加边框、将图片发布到社交媒体网站等功能。在本章中，我们将学习如何使用另一个应用：具体来说，我们将学习如何在另一个应用内部使用相机和电子邮件应用。我们将构建一个应用，该应用使用设备的相机应用（至少是其中之一）拍照，处理该图片，然后使用电子邮件应用将其发送给朋友。Android Studio 环境不包含相机，因此我们需要一个实际的设备（手机或平板电脑）来测试本章中的应用。

## 12.1 访问相机应用并拍照，照片应用，版本 0

如果我们想在应用内拍照，有两种选择：

* ▸ 访问相机应用并处理其结果。
* ▸ 使用相机 API 并直接访问相机。

在本章中，我们使用相机应用。在应用的版本 0 中，我们做三件事：

* ▸ 允许用户使用相机应用拍照。
* ▸ 捕获拍摄的图片。
* ▸ 显示图片。

我们可以使用 `PackageManager` 类来收集设备上安装的应用包的信息：我们可以使用 `PackageManager` 引用来检查设备是否有相机、前置摄像头、麦克风、GPS、指南针、陀螺仪、支持蓝牙、支持 Wi-Fi 等。

我们可以通过调用 `PackageManager` 类的 `hasSystemFeature` 方法来测试设备是否具有某个功能，传入与该功能对应的 `PackageManager` 类的常量。如果设备上存在该常量描述的功能，则该方法返回 `true`，否则返回 `false`。`hasSystemFeature` 方法具有以下 API：

```java
public boolean hasSystemFeature( String feature )
```

我们通常使用 `PackageManager` 类的 `String` 常量来代替 `feature` 参数。表 12.1 显示了其中一些 `String` 常量。

| 常量 | 描述 |
| --- | --- |
| `FEATURE_BLUETOOTH` | 用于检查设备是否支持蓝牙。 |
| `FEATURE_CAMERA` | 用于检查设备是否有相机。 |
| `FEATURE_CAMERA_FRONT` | 用于检查设备是否有前置摄像头。 |
| `FEATURE_LOCATION_GPS` | 用于检查设备是否具有 GPS。 |
| `FEATURE_MICROPHONE` | 用于检查设备是否具有麦克风。 |
| `FEATURE_SENSOR_COMPASS` | 用于检查设备是否具有指南针。 |
| `FEATURE_SENSOR_GYROSCOPE` | 用于检查设备是否具有陀螺仪。 |
| `FEATURE_WIFI` | 用于检查设备是否支持 Wi-Fi。 |

表 12.1 `PackageManager` 类的选定常量

我们使用 `Context` 类（由 `Activity` 类继承）的 `getPackageManager` 方法来获取 `PackageManager` 引用。假设我们在 `Activity` 类内部，以下伪代码序列说明了上述过程：

```java
// 在 Activity 类内部
PackageManager manager = getPackageManager( );
if( manager.hasSystemFeature( PackageManager.DESIRED_FEATURE_CONSTANT ) )
  // 所需功能存在；使用它
else
  // 通知用户此应用将无法运行
```

为了运行相机应用，或者更准确地说，“一个”相机应用，我们首先检查设备是否具有相机应用。表 12.1 展示了两个可用于此目的的常量。我们可以通过调用 `PackageManager` 类的 `hasSystemFeature` 方法，并传入 `PackageManager` 类的 `FEATURE_CAMERA` 常量来测试设备是否有相机应用，如下面的代码序列所示：

```java
// 在 Activity 类内部
PackageManager manager = getPackageManager( );
if( manager.hasSystemFeature( PackageManager.FEATURE_CAMERA ) )
  // 相机应用存在；使用它
else
  // 通知用户此应用将无法运行
```

| 方法 | 描述 |
| --- | --- |
| `void startActivityForResult( Intent intent, int requestCode )` | 为 `intent` 启动一个 `Activity`。如果 `requestCode` >= 0，它将作为 `onActivityResult` 方法的第一个参数返回。 |
| `void onActivityResult( int requestCode, int resultCode, Intent data )` | `requestCode` 是提供给 `startActivityForResult` 的请求码。`data` 是由 Activity 返回给调用者的 `Intent`。 |

表 12.2 `Activity` 类的 `startActivityForResult` 和 `onActivityResult` 方法

一旦我们知道设备具有我们想要使用的功能，我们就可以启动一个 Activity 来使用该功能。在这种情况下，我们感兴趣的是拍摄照片并将其显示在屏幕上。通常，如果我们想启动一个 Activity 并希望访问该 Activity 的结果，我们可以使用 `Activity` 类的 `startActivityForResult` 和 `onActivityResult` 方法，两者均显示在表 12.2 中。`onActivityResult` 在由 `startActivityForResult` 的 `Intent` 参数定义的 Activity 执行完毕后执行。

为了创建一个使用设备功能的 `Intent`，我们可以使用以下 `Intent` 构造函数：

```java
public Intent( String action )
```

`String action` 描述了我们想要使用的设备功能。创建 `Intent` 后，我们可以通过调用 `Activity` 类的 `startActivityForResult` 方法为其启动一个 Activity。下面的代码序列说明了如何在应用内启动另一个应用：

```java
// 创建 Intent
Intent otherAppIntent = new Intent( otherAppAppropriateArgument );
// actionCode 是某个整数
startActivityForResult( otherAppIntent, actionCode );
```

要创建一个使用相机应用的 `Intent`，我们将 `MediaStore` 类的 `ACTION_IMAGE_CAPTURE` 常量传递给 `Intent` 构造函数。以下代码序列启动了一个相机应用 Activity：

```java
// 在 Activity 类内部
Intent takePictureIntent = new Intent
( MediaStore.ACTION_IMAGE_CAPTURE );
// actionCode 是某个整数
startActivityForResult( takePictureIntent, actionCode );
```

Activity 执行完毕后，我们在 `Activity` 类的 `onActivityResult` 方法内部执行。其 `Intent` 参数包含了刚刚执行的 `Activity` 的结果，在本例中是一个存储用户刚刚拍摄的照片的 `Bitmap` 对象。下面的代码展示了如何在 `onActivityResult` 方法内将拍摄的照片作为 `Bitmap` 访问。如第一个注释所示，我们应该检查 `requestCode` 的值是否与传递给 `startActivityForResult` 方法的请求码相同，并且 `resultCode` 值反映了 Activity 正常执行。

| 类 | 方法 | 描述 |
| --- | --- | --- |
| `Intent` | `Bundle getExtras( )` | 返回一个 `Bundle` 对象，该对象封装了放置在此 `Intent` 中的映射（键/值对）。 |
| `BaseBundle` | `Object get( String key )` | 返回映射到键的 Object。 |

表 12.3 `Intent` 和 `BaseBundle` 类的 `getExtras` 和 `get` 方法

我们使用表 12.3 中所示的 `getExtras` 方法检索 `Intent` 的 `Bundle` 对象。该 `Bundle` 对象存储了存储在 `Intent` 中的键/值对映射。使用该 `Bundle` 对象，我们调用 `get` 方法（由 `Bundle` 从 `BaseBundle` 类继承，同样显示在表 12.3 中），并传入键 `data` 以检索 `Bitmap`。由于 `get` 方法返回一个 `Object`，而我们期望一个 `Bitmap`，因此需要将返回值类型转换为 `Bitmap`。

```java
protected void onActivityResult( int requestCode,
                                 int resultCode, Intent data ) {
  // 检查请求码是否正确且结果码正常
  Bundle extras = data.getExtras( );
  Bitmap bitmap = ( Bitmap ) extras.get( "data" );
  // 在此处处理 bitmap
}
```

`ImageView` 类（属于 `android.widget` 包）可用于显示图片并缩放。表 12.4 展示了它的一些方法。

| 方法 | 描述 |
| --- | --- |
| `ImageView( Context context )` | 构造一个 `ImageView` 对象。 |
| `void setImageBitmap( Bitmap bitmap )` | 将 `bitmap` 设置为该 `ImageView` 的内容。 |
| `void setImageDrawable( Drawable drawable )` | 将 `drawable` 设置为该 `ImageView` 的内容。 |
| `void setImageResource( int resource )` | 将 `resource` 设置为该 `ImageView` 的内容。 |
| `void setScaleType( ImageView.ScaleType scaleType )` | 将 `scaleType` 设置为该 `ImageView` 的缩放模式。 |

表 12.4 `ImageView` 类的选定方法

在此应用中，当用户使用相机应用拍照时，我们会在应用运行时动态获取图像。拍照后，我们使用 `BaseBundle` 类的 `get` 方法检索 `extras`，然后检索对应的 `Bitmap` 对象。因此，在此应用中，我们使用 `setImageBitmap` 方法将使用相机应用拍摄的照片填充到 `ImageView` 中。如果我们已经有一个名为 `bitmap` 的 `Bitmap` 引用，我们可以使用以下语句将其放入名为 `imageView` 的 `ImageView` 中：

```java
imageView.setImageBitmap( bitmap );
```

我们希望通知潜在用户此应用使用了相机。因此，我们在 `AndroidManifest.xml` 文件的 `manifest` 元素内定义一个 `uses-feature` 元素，如下所示：

```xml
<uses-feature android:name="android.hardware.camera2" />
```

为简单起见，我们只允许此应用以竖屏方向运行，因此我们在 `activity` 元素内添加以下代码：

```xml
android:screenOrientation="portrait"
```

示例 12.1 展示了 `activity_main.xml` 文件。我们使用一个垂直方向的 `LinearLayout`（第 10 行），因为我们打算在应用的其他版本中在视图底部添加元素。在第 13–17 行，我们添加了一个 `ImageView` 元素来存储图片。我们在第 17 行为其指定了 id `picture`，以便可以使用 `findViewById` 方法从 `MainActivity` 类中检索它。

![](img/ch12exa01.jpg)

示例 12.1 `activity_main.xml` 文件，照片应用，版本 0

| 枚举值 | XML 属性值 | 描述 |
| --- | --- | --- |
| `CENTER` | `center` | 将图像在 `ImageView` 内居中，不进行任何缩放。 |



| `CENTER_INSIDE` | `centerInside` | 根据需要缩小图像，使其适合 `ImageView` 内部并居中，同时保持图像的宽高比。 |
| --- | --- | --- |
| `FIT_CENTER` | `fitCenter` | 根据需要缩小或放大图像，使其恰好（至少沿一个轴）适合 `ImageView` 内部并居中，同时保持图像的宽高比。 |

表 12.5 `ImageView.ScaleType` 枚举的选定枚举值及对应的 XML 属性值

`android:scaleType` XML 属性使我们能够指定图片在 `ImageView` 中的缩放和定位方式。`ImageView` 类中的 `ScaleType` 枚举包含可用于缩放和定位图片的值。表 12.5 列出了其中一些可能的值。在第 16 行，我们使用 `fitCenter` 值来完美缩放图片，使其适合并位于 `ImageView` 的中间。在第 6–9 行，我们提供了 `dimens.xml` 文件中定义的一些内边距。

示例 12.2 展示了 `MainActivity` 类。在第 14–15 行，我们声明了两个实例变量 `bitmap` 和 `imageView`，分别是一个 `Bitmap` 和一个 `ImageView`。每当我们想要更改图片时，都需要访问它们，因此直接引用它们会很方便。在 `onCreate` 方法（第 17–32 行）中，我们在第 20 行初始化了 `imageView`。我们在第 22 行获取了一个 `PackageManager` 引用，并在第 23 行测试是否存在相机应用。如果存在，我们在第 24–25 行创建一个使用相机应用的 `Intent`，并在第 26 行启动一个活动，传递存储在 `PHOTO_REQUEST` 常量中的值。如果没有相机应用（第 27 行），我们在第 28–30 行通过 `Toast` 向用户提供快速反馈。

![](img/ch12exa02.jpg) ![](img/ch12exa02a.jpg)

示例 12.2 `MainActivity` 类，照片应用，版本 0

当用户运行应用并拍照时，我们在 `onActivityResult` 方法（第 34–42 行）中执行代码。我们在第 38 行从 `Intent` 参数 `data` 中检索 `Bundle`。由于创建 `Intent` 是为了使用相机应用拍照，我们期望与该意图关联的 `Bundle` 包含一个存储该照片的 `Bitmap`。`Bundle` 类的 `get` 方法在传入字符串 `data` 时返回该 `Bitmap`。我们在第 39 行检索它。在第 40 行，我们将 `imageView` 中的图像设置为该 `Bitmap`。

当我们运行应用时，相机应用启动。图 12.1 显示了用户拍照后的应用界面。图 12.2 显示了用户点击“保存”按钮后的应用界面。图片显示在屏幕上。

![](img/9781284093650_CH12_FIGF01.jpg)

图 12.1 照片应用，版本 0，拍照后

![](img/9781284093650_CH12_FIGF02.jpg)

图 12.2 照片应用，版本 0，点击“保存”后

## 12.2 模型：灰度化图片，照片应用，版本 1

在应用的版本 1 中，我们使用硬编码公式将图片灰度化。此应用的模型是 `BitmapGrayer` 类。它封装了一个 `Bitmap` 和一个可应用于该 `Bitmap` 的灰度化方案。

在 RGB 颜色系统中，有 256 种灰度；灰色具有相同数量的红色、绿色和蓝色。因此，其 RGB 表示形式为（`x`，`x`，`x`），其中 `x` 是 0 到 255 之间的整数。（0，0，0）是黑色，（255，255，255）是白色。

表 12.6 列出了 `android.graphics` 包中 `Color` 类的一些静态方法。我们不应将该类与 `java.awt` 包中的 `Color` 类混淆。

通常，如果我们从彩色图片开始，并希望将其转换为黑白图片，我们需要将图片中每个像素的颜色转换为灰色。有几种公式可用于灰度化图片，我们采用以下策略：

| 方法 | 描述 |
| --- | --- |
| `static int argb( int alpha, int red, int green, int blue )` | 返回由 alpha、红色、绿色和蓝色参数定义的颜色整数值。 |
| `static int alpha( int color )` | 返回颜色的 alpha 分量，值为 0 到 255 之间的整数。 |
| `static int red( int color )` | 返回颜色的红色分量，值为 0 到 255 之间的整数。 |
| `static int green( int color )` | 返回颜色的绿色分量，值为 0 到 255 之间的整数。 |
| `static int blue( int color )` | 返回颜色的蓝色分量，值为 0 到 255 之间的整数。 |

表 12.6 `android.graphics` 包中 `Color` 类的选定方法

- 保持每个像素的 alpha 分量不变。
- 使用像素的红色、绿色和蓝色分量为其生成灰色调。
- 对每个像素使用相同的转换公式生成灰色调。

例如，如果红色、绿色和蓝色是某个像素的红色、绿色和蓝色分量，我们可以应用以下加权平均公式，使得该像素的新颜色为（`x`，`x`，`x`）：

```text
x = red * redCoeff + green * greenCoeff + blue * blueCoeff
```

其中：

```text
redCoeff、greenCoeff 和 blueCoeff 在 0 到 1 之间
```

并且：

```text
redCoeff + greenCoeff + blueCoeff <= 1
```

这保证了 `x` 在 `0` 到 `255` 之间，每个像素的颜色都是灰色调，并且颜色转换过程对图片中的所有像素保持一致。

因此，如果 `color` 是一个表示像素颜色的 `Color` 引用，并且我们希望使用红色、绿色和蓝色的权重分别为 `0.5`、`0.3` 和 `0.2` 来为该像素生成灰色，我们可以使用以下语句生成该灰色：

```java
int shade = ( int ) ( 0.5 * Color.red( color ) + 0.3 * Color.green( color )
                  + 0.2 * Color.blue( color ) );
```

图片可以存储在 `Bitmap` 中。表 12.7 显示了 `Bitmap` 类的一些方法。它们使我们能够遍历 `Bitmap` 对象的所有像素，访问每个像素的颜色并更改它。在此应用中，我们从一张图像开始，获取对应的 `Bitmap`，将颜色更改为灰色调，然后将 `Bitmap` 放回图像中，图像变为黑白。

| 方法 | 描述 |
| --- | --- |
| `int getWidth( )` | 返回此 `Bitmap` 的宽度。 |
| `int getHeight( )` | 返回此 `Bitmap` 的高度。 |
| `int getPixel( int x, int y )` | 返回此 `Bitmap` 中坐标（`x`，`y`）处像素颜色的整数表示。 |
| `void setPixel( int x, int y, int color )` | 将此 `Bitmap` 中坐标（`x`，`y`）处像素的颜色设置为 `color`。 |
| `Bitmap.Config getConfig( )` | 返回此 `Bitmap` 的配置。`Bitmap.Config` 类封装了像素在 `Bitmap` 中的存储方式。 |
| `static Bitmap createBitmap( int w, int h, Bitmap.Config config )` | 返回一个可变的 `Bitmap`，宽度为 `w`，高度为 `h`，并使用 `config` 创建该 `Bitmap`。 |

表 12.7 `Bitmap` 类的选定方法

为了访问名为 `bitmap` 的 `Bitmap` 的每个像素，我们使用以下双重循环：

```java
for ( int i = 0; i < bimap.getWidth( ); i++ ) {
    for ( int j = 0; j < bitmap.getHeight( ); j++ ) {
        int color = bitmap.getPixel( i, j );
        // 在此处处理颜色
    }
}
```

示例 12.3 展示了 `BitmapGrayer` 类。它有四个实例变量（第 7–10 行）：`originalBitmap`（一个 `Bitmap`）以及 `redCoeff`、`greenCoeff`、`blueCoeff`（三个 `float` 值，范围在 `0` 到 `1` 之间）。它们表示在生成 `originalBitmap` 每个像素的灰色调时考虑的红色、绿色和蓝色分量。

三个修改器（第 32–39 行、第 41–48 行和第 50–57 行）强制执行以下约束：

- `redCoeff、greenCoeff 和 blueCoeff 在 0 到 1 之间`
- `redCoeff + greenCoeff + blueCoeff <= 1`

第 32–39 行的 `setRedCoeff` 修改器仅在 `newRedCoeff` 参数介于 `0.0` 和 `1.0` 之间时（第 33 行）更新 `redCoeff`。如果 `newRedCoeff` 的值使得 `greenCoeff`、`blueCoeff` 和 `newRedCoeff` 之和小于等于 `1`（第 34 行），则将 `newRedCoeff` 赋给 `redCoeff`（第 35 行）。否则，将 `redCoeff` 的值设置为使 `greenCoeff`、`blueCoeff` 和 `redCoeff` 之和等于 `1`（第 37 行）。另外两个修改器遵循相同的逻辑。

第 59–75 行编写的 `grayScale` 方法返回一个具有以下特征的 `Bitmap`：

- 其宽度和高度与 `originalBitmap` 相同。
- 其每个像素均为灰色。
- 如果 `red`、`green` 和 `blue` 分别是 `originalBitmap` 中某个像素的红、绿、蓝分量，则返回的 `Bitmap` 中相同 `x`、`y` 坐标处的像素颜色为灰色，且灰度值为 `red * redCoeff + green * greenCoeff + blue * blueCoeff`。

![](img/ch12exa03.jpg) ![](img/ch12exa03a.jpg)

示例 12.3 `BitmapGrayer` 类，照片应用，版本 1

我们在第 60–61 行获取 `originalBitmap` 的宽度和高度。在第 62 行调用 `getConfig` 方法（见表 12.7）获取 `originalBitmap` 的配置。在第 63 行调用 `createBitmap`（见表 12.7）创建 `originalBitmap` 的可变副本 `bitmap`，使用与 `originalBitmap` 相同的宽度、高度和配置。

在第 64–73 行，我们使用双重循环定义 `bitmap` 中每个像素的颜色。在第 66 行获取 `originalBitmap` 中当前像素的颜色。在第 67–69 行计算 `bitmap` 中对应像素的灰度值，在第 70 行用该值创建颜色，并在第 71 行将该颜色赋给该像素。在第 74 行返回 `bitmap`。

示例 12.4 展示了 `MainActivity` 类，版本 1。与版本 0 的唯一区别是我们对 `imageView` 中的图片进行了灰度化处理。我们在第 14 行声明了一个 `BitmapGrayer` 实例变量 `grayer`。在 `onActivityResult` 内部，我们在第 41 行使用 `bitmap` 以及灰度化处理过程中红、绿、蓝系数的三个默认值实例化 `grayer`。注意，在 `onCreate` 方法中实例化 `grayer` 为时过早，因为我们需要先拍摄照片才能获得该照片的 `Bitmap` 对象。在第 42 行，我们调用 `grayer` 的 `grayScale` 方法，并将结果 `Bitmap` 赋给 `bitmap`。

![](img/ch12exa04.jpg)

示例 12.4 `MainActivity` 类，照片应用，版本 1

![](img/9781284093650_CH12_FIGF03.jpg)

图 12.3 照片应用，版本 1，点击保存后显示灰度化图片

图 12.3 展示了用户点击保存按钮后，我们的应用在平板电脑上运行的情况。图片现在变为黑白。

## 12.3 使用 `SeekBars` 定义灰度，照片应用，版本 2

在版本 1 中，生成 `Bitmap` 中每个像素灰度的公式是硬编码的，系数为 `0.34`、`0.33` 和 `0.33`。在版本 2 中，我们允许用户指定公式中的系数。我们在用户界面中包含了三个搜索条（通常也称为滑块）。它们允许用户定义用于计算每个像素灰度的红、绿、蓝系数。

![](img/9781284093650_CH12_FIGF04.jpg)

图 12.4 `SeekBar` 的继承层次结构

`SeekBar` 类属于 `android.widget` 包，封装了一个搜索条。图 12.4 展示了其继承层次结构。

从视觉上看，搜索条包含一个进度条和一个滑块。其默认表示包括一条线（进度条）和一个圆（滑块）。我们可以使用 `SeekBar` 元素在布局 XML 文件中定义搜索条。表 12.8 展示了一些可用于通过 XML 定义搜索条的 XML 属性，以及如果希望通过代码控制搜索条时对应的相应方法。我们可以使用 `android:progress` 属性或通过代码使用 `setProgress` 方法设置搜索条的当前值（称为进度）。其最小值为 `0`，我们可以使用 `android:max` 属性或 `setMax` 方法定义其最大值。

默认情况下，进度条和滑块为浅蓝色。我们可以通过将进度条或滑块替换为 `drawable` 资源（例如来自文件或形状的图像）来自定义搜索条。这可以在 XML 布局文件中或通过编程方式完成。在此应用中，由于每个搜索条代表特定颜色的系数，我们自定义三个搜索条的滑块以反映它们所代表的三种颜色：红色、绿色和蓝色。我们定义了三个 `drawable` 资源，每种颜色一个，并在 `activity_main.xml` 文件中使用它们。

| 类 | XML 属性 | 对应方法 |
| --- | --- | --- |
| `ProgressBar` | `android:progressDrawable` | `void setProgressDrawable ( Drawable drawable )` |
| `ProgressBar` | `android:progress` | `void setProgress ( int progress )` |
| `ProgressBar` | `android:max` | `void setMax ( int max )` |
| `AbsSeekBar` | `android:thumb` | `void setThumb ( Drawable drawable )` |

表 12.8 `ProgressBar` 和 `AbsSeekBar` 的选定 XML 属性及方法

在 `drawable` 目录中，我们创建了三个文件：`red_thumb.xml`、`green_thumb.xml` 和 `blue_thumb.xml`。

示例 12.5 展示了 `red_thumb.xml` 文件。它定义了一个用于红色搜索条滑块的 `shape`。它定义了一个宽度和高度相等的椭圆（第 4–7 行），即一个圆形。在第 8–9 行，我们定义了圆形内部的颜色，纯红色。在第 10–12 行，我们定义了圆形的轮廓厚度（第 11 行）和颜色（第 12 行），也是红色但非完全不透明。

![](img/ch12exa05.jpg)

示例 12.5 `red_thumb.xml` 文件，照片应用，版本 2

`green_thumb.xml` 和 `blue_thumb.xml` 文件类似，分别使用颜色 `#F0F0` 和 `#F00F`，透明度值与 `red_thumb.xml` 文件相同。

要访问名为 `abc.xml` 的 `drawable` 资源，在 XML 布局上下文中使用值 `@drawable/abc`，如果通过编程方式访问资源，则使用表达式 `R.drawable.abc`。

我们需要向 XML 布局文件中添加三个 `SeekBar` 元素。除了它们的 `id` 和滑块外，这些 `SeekBar` 元素完全相同，因此我们使用样式来定义它们的一些属性。我们编辑 `styles.xml` 文件，并为 `SeekBar` 元素添加一个样式元素。示例 12.6 展示了 `styles.xml` 文件。在 `activity_main.xml` 中使用的 `seekBarStyle`（定义在第 11–18 行）用于设置搜索条的样式。它定义了搜索条共有的所有属性。

在第 12 行，我们为使用 `seekBarStyle` 的所有元素分配相同的水平空间，并在第 15 行将它们垂直居中。我们在第 16 行使用 `seekBarStyle` 将任何搜索条初始化为 `progress` 值为 `0`，并在第 17 行赋予其 `max` 值为 `100`。

示例 12.7 展示了 `activity_main.xml` 文件。它将屏幕分为两部分：顶部的 `ImageView`（第 13–18 行）占据屏幕的五分之四（第 14 行），底部的 `LinearLayout`（第 20–39 行）包含屏幕的五分之一（第 22 行），其组件水平排列（第 21 行），并包含三个搜索条（第 26–29 行、第 30–33 行、第 34–37 行）。

我们为每个搜索条赋予一个 `id`（第 27、31、35 行），以便使用 `findViewById` 方法检索它们。在第 28、32 和 36 行，我们通过将三个搜索条的滑块设置为 `red_thumb.xml`、`green_thumb.xml` 和 `blue_thumb.xml` 中定义的形状来自定义它们。在第 29、33 和 37 行，我们使用 `seekBarStyle` 为它们设置样式。

![](img/ch12exa06.jpg)



### 示例 12.6：`styles.xml` 文件，照片应用，版本 2

![](img/ch12exa07.jpg) ![](img/ch12exa07a.jpg)

### 示例 12.7：`activity_main.xml` 文件，照片应用，版本 2

我们期望用户与滑块进行交互，并且需要处理该事件。为此，我们需要实现 `OnSeekBarChangeListener` 接口，它是 `SeekBar` 类的一个 `public static` 内部接口。该接口包含三个方法，如表 12.9 所示。

在本应用中，我们只关心用户交互时每个滑块的值。因此，我们将 `onStartTrackingTouch` 和 `onStopTrackingTouch` 方法重写为空操作的方法，并将事件处理代码放在 `onProgressChanged` 方法中。它的第一个参数 `seekBar` 是用户正在交互的 `SeekBar` 的引用，使我们能够确定用户正在更改灰度化公式中的红色、绿色或蓝色系数。第二个参数 `progress` 存储了 `seekBar` 的进度值：我们用它来设置对应颜色的系数。第三个参数 `fromUser`，如果该方法是由用户交互调用的，则为 `true`；如果是由程序化调用，则为 `false`。

我们希望每个滑块的滑块位置反映其对应系数的实际值。由于灰度化公式的三个系数存在约束，我们不允许用户随意操作滑块。三个系数的总和必须始终为 `1` 或更小。例如，我们不希望红色和绿色滑块都显示 `75%` 的值，因为这意味着红色、绿色和蓝色系数的总和至少为 `1.5`，违反了约束。

因此，我们需要通过代码重置每个滑块的滑块位置，而这又会触发对 `onProgressChanged` 方法的调用。在这种情况下，我们不想处理该调用。

| 方法 | 描述 |
| --- | --- |
| `void onStartTrackingTouch( SeekBar seekBar )` | 当用户开始触摸滑块时调用。 |
| `void onStopTrackingTouch( SeekBar seekBar )` | 当用户停止触摸滑块时调用。 |
| `void onProgressChanged( SeekBar seekBar, int progress, boolean fromUser )` | 当用户移动滑块时持续调用。 |

表 12.9：`SeekBar.OnSeekBarChangeListener` 接口的方法

为了为 `SeekBar` 设置事件处理，我们需要执行以下操作：

- 编写一个实现 `SeekBar.OnSeekBarChangeListener` 接口的 `private` 处理程序类。
- 声明并实例化该类的处理程序对象。
- 将该处理程序注册到 `SeekBar` 组件上。

示例 12.8 展示了 `MainActivity` 类，版本 2。在第 57–82 行，我们编写了 `GrayChangeHandler` 类，它实现了 `SeekBar.OnSeekBarChangeListener` 接口。三个 `SeekBar` 引用 `redBar`、`greenBar` 和 `blueBar` 在第 18 行被定义为实例变量。

在 `onCreate` 方法中，第 25–27 行，我们将 `activity_main.xml` 布局文件中定义的三个 `SeekBar` 分配给这三个实例变量。在第 29 行，我们声明并实例化了一个 `GrayChangeHandler` 对象。在第 30–32 行，我们将其注册为 `redBar`、`greenBar` 和 `blueBar` 的监听器。

在 `onActivityResult` 方法中（第 46–55 行），我们在第 52 行使用默认值 `0`、`0`、`0` 实例化了 `grayer`。在版本 1 中，我们使用硬编码的公式对图片进行灰度化处理。在版本 2 中，我们保持图片原样，保留其颜色，并等待用户与三个滑块交互以对图片进行灰度化处理。

`onProgressChanged` 方法在第 59–75 行编写。我们在第 61 行测试该方法的调用是否由用户交互触发。如果不是（即 `fromUser` 为 `false`），则不执行任何操作。如果是（即 `fromUser` 为 `true`），则测试哪个滑块触发了事件。

如果是红色滑块（第 62 行），我们在第 63 行调用 `setRedCoeff`，并将进度值缩放到 `0` 到 `1` 之间。新的 `redCoeff` 值可能导致三个系数的总和为 `1` 或更小。在这种情况下，我们希望阻止滑块滑块位置超过 `redCoeff` 对应的值（即 `100` 乘以 `redCoeff` 的值）。

无论哪种情况，我们都在第 64 行通过调用 `setProgress` 方法根据 `redCoeff` 的值定位滑块位置。如果滑块是绿色或蓝色滑块，我们分别在 65–67 行和 68–70 行执行相同操作。最后，我们在第 72 行检索由新系数生成的 `Bitmap`，并在第 73 行将图片重置为该 `Bitmap`。

![](img/ch12exa08.jpg) ![](img/ch12exa08a.jpg)

### 示例 12.8：`MainActivity` 类，照片应用，版本 2

图 12.5 展示了用户点击“保存”按钮并与滑块交互后应用运行的情况。

![](img/9781284093650_CH12_FIGF05.jpg)

图 12.5：照片应用，版本 2，点击“保存”并与用户交互后

## 12.4 改进用户界面，照片应用，版本 3

版本 2 为用户提供了自定义灰度化图片公式的能力，但滑块并未提供每个颜色系数值的精确反馈。在版本 3 中，我们在三个 `SeekBar` 组件下方添加了三个 `TextView` 来显示颜色系数。

如果显示小数点后有很多位的数字，会让用户感到烦恼。我们将小数点后的位数限制为两位。为了实现这一点，我们构建了一个工具类 `MathRounding`，其中包含一个 `static` 方法 `keepTwoDigits`，该方法接受一个 `float` 参数，并返回仅保留小数点后两位的相同 `float` 值。

示例 12.9 展示了 `MathRounding` 类。`keepTwoDigits` 方法在第 4–7 行编写，它将参数 `f` 乘以 `100`，并在第 5 行将结果转换为 `int`。然后，它将那个 `int` 转换为 `float`，除以 `100`，并在第 6 行返回结果。我们将 `int` 转换为 `float` 是为了执行浮点除法。

我们可以在 `BitmapGrayer` 类或 `MainActivity` 类中使用此方法。由于我们认为此功能与显示方式相关，而非应用的功能，因此我们在应用的控制器（`MainActivity` 类）中使用该方法，而不是在模型（`BitmapGrayer` 类）中。因此，`BitmapGrayer` 类没有变化。

![](img/ch12exa09.jpg)

### 示例 12.9：`MathRounding` 类，照片应用，版本 3

我们需要在 XML 布局文件中添加三个 `TextView` 元素。除了它们的 id 之外，这些 `TextView` 元素是相同的，因此我们为它们使用一个样式。我们编辑 `styles.xml` 文件，并为 `TextView` 添加一个 `style` 元素。示例 12.10 展示了 `styles.xml` 文件。

![](img/ch12exa10.jpg)

### 示例 12.10：`styles.xml` 文件，照片应用，版本 3

`textStyle` 样式在第 20–28 行定义了用于三个 `TextView` 元素的样式。我们在第 26 行指定字体大小为 `30`，这应该适用于大多数设备，并在第 24 行指定文本居中，在第 25 行将其设为粗体，在第 27 行将其初始化为 `0.0`。

示例 12.11 展示了 `activity_main.xml` 文件。屏幕仍然使用垂直的 `LinearLayout` 组织。现在它包含三个部分：`ImageView`（第 13–18 行）占据屏幕的十分之八（第 14 行），一个 `LinearLayout`（第 20–39 行）占据屏幕的十分之一（第 22 行），以及另一个 `LinearLayout`（第 41–57 行）也占据屏幕的十分之一（第 43 行）。三个 `SeekBar` 元素（第 26–37 行）现在只占据屏幕的十分之一。

![](img/ch12exa11.jpg) ![](img/ch12exa11a.jpg)

## 示例 12.11：`activity_main.xml` 文件，照片应用，版本 3

第 47–55 行定义了三个 `TextView` 元素。我们在第 48、51 和 54 行分别为它们指定了 id，以便在 `MainActivity` 类中使用 `findViewById` 方法访问它们。在第 49、52 和 55 行，通过 `textStyle` 对它们进行了样式设置。

## 示例 12.12：`MainActivity` 类，照片应用，版本 3

示例 12.12 展示了 `MainActivity` 类在版本 3 中的变化。第 11 行导入了 `TextView` 类，第 20 行声明了三个 `TextView` 实例变量 `redText`、`greenText` 和 `blueText`。它们在第 31–33 行的 `onCreate` 方法中完成初始化。

每当用户与某个进度条交互时，我们需要更新对应的 `TextView`。我们在第 71–72 行、第 76–77 行和第 81–82 行中，在根据用户正在交互的进度条的 `progress` 值更新 `grayer` 之后执行此操作。

图 12.6 展示了用户点击“保存”按钮后与进度条交互时应用运行的效果。

![](img/ch12exa12.jpg)

## 示例 12.12：`MainActivity` 类，照片应用，版本 3

![](img/9781284093650_CH12_FIGF06.jpg)

图 12.6：照片应用，版本 3，点击“保存”并与用户交互后

## 12.5 存储图片，照片应用，版本 4

在版本 0、1、2 和 3 中，我们的应用使用相机应用拍照。默认情况下，相机拍摄的任何照片都会存储在相册中。然而，灰度化后的图片在版本 0、1、2 和 3 中并未存储。

在版本 4 中，我们的应用将灰度化后的图片存储在设备上。通常，我们可以将持久化数据存储在内部存储或外部存储中。在 Android 早期，内部存储指非易失性存储器，外部存储指可移动存储介质。

在最近的 Android 设备中，存储空间被划分为两个区域：内部存储和外部存储。我们可以将持久化数据保存在内部或外部存储的文件中。

内部存储始终可用，并且默认情况下，保存在某些内部存储目录中的文件只能由写入它们的应用访问。当用户卸载应用时，位于内部存储中与应用相关的文件会自动删除。

根据设备的不同，外部存储通常可用（尽管不能保证），并且外部存储中的文件可以被任何应用访问。当用户卸载应用时，只有位于 `Context` 类的 `getExternalFilesDir` 方法返回的目录中的外部存储文件才会被自动删除。

表 12.10 总结了内部存储和外部存储之间的一些差异，包括 `Context` 类的方法。

|  | 内部存储 | 外部存储 |
| --- | --- | --- |
| 默认文件访问 | 仅应用可访问。 | 全局可读。 |
| 使用时机 | 当需要限制文件访问时。 | 当不关心限制文件访问时。 |
| 获取目录 | `getFilesDir()` 或 `getCacheDir()` | `getExternalFilesDir(String type)` |
| 清单文件权限 | 无需权限。 | 需要 `WRITE_EXTERNAL_STORAGE` 权限。 |
| 用户卸载应用时 | 应用相关文件被删除。 | 仅当文件位于通过 `getExternalFilesDir` 获取的目录中时才会被删除。 |

**表 12.10**：内部存储、外部存储及 `Context` 类的方法

在版本 4 中，我们将灰度化后的图片保存在外部存储中。为了实现这一功能，我们执行以下操作：

- 在 `activity_main.xml` 布局文件中添加一个按钮。
- 编辑 `MainActivity` 类，使得用户点击按钮时保存图片。
- 创建一个工具类 `StorageUtility`，其中包含一个将 `Bitmap` 写入外部存储文件的方法。

## 示例 12.13：`activity_main.xml` 文件，照片应用，版本 4

示例 12.13 展示了 `activity_main.xml` 文件，版本 4。在第 59–72 行，我们在用户界面中添加了一个按钮。在第 70 行，我们指定当用户点击该按钮时调用 `savePicture` 方法。

我们略微调整了图片占屏幕的比例。在第 14 行，我们将 `ImageView` 元素的 `android:layout_weight` 属性值设置为 `7`，使其占据屏幕的 70%。`SeekBar` 元素仍占 10%（第 22 行），`TextView` 元素仍占 10%（第 43 行），按钮占屏幕的 10%（第 61 行）。

## 示例 12.14：`StorageUtility` 类

示例 12.14 展示了 `StorageUtility` 类。它只包含一个 `static` 方法 `writeToExternalStorage`，位于第 13–62 行：该方法将 `Bitmap` 写入外部存储中的文件，并返回对该文件的引用。

如果过程中出现问题，它会 `throws` 一个 `IOException`。我们返回 `File` 引用而不是 `true` 或 `false`，因为在版本 5 中，当我们将图片通过电子邮件发送给朋友时，需要将该文件作为附件添加。除了 `Bitmap` 参数外，该方法还接受一个 `Activity` 参数，我们用它来访问外部存储的目录。

`Environment` 类是一个工具类，提供对环境变量的访问。它的 `getExternalStorageState` `static` 方法返回一个 `String`，表示设备上外部存储的状态。`getExternalStorageState` 的 API 如下：

```
public static String getExternalStorageState( )
```

![](img/ch12exa13.jpg) ![](img/ch12exa13a.jpg)

## 示例 12.13：`activity_main.xml` 文件，照片应用，版本 4

![](img/ch12exa14.jpg) ![](img/ch12exa14a.jpg)

## 示例 12.14：`StorageUtility` 类

| 常量 | 描述 |
| --- | --- |
| `MEDIA_MOUNTED` | 如果外部存储存在且具有读写权限，`getExternalStorageState` 方法返回该值。 |
| `DIRECTORY_PICTURES` | 目录名称为 Pictures。 |
| `DIRECTORY_DOWNLOADS` | 目录名称为 Download。 |
| `DIRECTORY_MUSIC` | 目录名称为 Music。 |
| `DIRECTORY_MOVIES` | 目录名称为 Movies。 |

**表 12.11**：`Environment` 类的部分常量

如果该 `String` 等于 `Environment` 类的 `MEDIA_MOUNTED` 常量的值（如表 12.11 所示），则表示设备上存在外部存储且具有读写权限。我们可以通过以下代码序列测试是否存在外部存储：

```
String storageState = Environment.getExternalStorageState( );
if( storageState.equals( Environment.MEDIA_MOUNTED ) ) {
  // 存在外部存储
```

我们在第 22–23 行获取存储状态，并在第 26 行测试设备上外部存储是否可用。如果不可用，我们在第 61 行 `throw` 一个 `IOException`。

如果可用，我们在第 27–29 行通过调用 `Context` 类的 `getExternalFilesDir` 方法（`MainActivity` 类通过 `Activity` 类继承该方法）获取外部存储目录的路径。表 12.12 展示了 `getExternalFilesDir` 方法。

在作者的平板电脑上，如果参数为 `null`，返回的目录路径为：

```
/storage/emulated/0/Android/data/com.jblearning.photograyingv4/files
```

如果参数为 `MyGrayedPictures`，返回的目录路径为：

```
/storage/emulated/0/Android/data/com.jblearning.photograyingv4/files/MyGrayedPictures
```

| 方法 | 描述 |
| --- | --- |
| `File getExternalFilesDir( String type )` | 返回应用可放置其文件的外部存储目录的绝对路径。该路径与应用相关。如果 type 不为 null，则会创建一个以 type 值为名称的子目录。 |

**表 12.12**：`Context` 类的 `getExternalFilesDir` 方法

`Environment` 类包含一些常量，可用于目录的标准名称。表 12.11 列出了其中一部分。请注意，我们并非必须使用名为 `Music` 的目录来存储音乐文件，但这样做是一种良好的实践。在第 29 行，我们使用了 `DIRECTORY_PICTURES` 常量，其值为 `Pictures`。



由于`writeToExternalStorage`方法可能被多次调用，我们希望每次调用时都创建一个新文件，而不是覆盖现有文件。我们也不希望要求用户提供文件名，因为这可能会让用户感到厌烦。因此，我们动态生成文件名。由于我们不想覆盖现有文件，我们选择了一种文件命名机制，确保每次都能生成唯一的文件名。一种方法是使用今天的日期和系统时钟。`SystemClock`类的`elapsedRealtime`静态方法（如表 12.13 所示）返回自上次启动以来的毫秒数。我们将其与今天的日期结合以生成文件名。用户几乎不可能在同一个毫秒内修改一个滑块并点击“保存图片”按钮。因此，我们的命名策略保证了每次生成的文件名都是唯一的。我们在第 30–33 行生成该唯一文件名。在第 35–36 行，我们使用该文件名在外部存储目录中创建一个文件。

我们在第 37 行获取该文件所在目录的可用空间大小，并在第 38 行使用`Bitmap`类的`getByteCount`方法（如表 12.14 所示）获取将位图写入该文件所需的字节数。我们在第 39 行测试目录中是否有足够的空间来容纳所需的字节数（乘以`1.5`以确保安全）。如果没有，我们在第 57–58 行`throw`一个`IOException`。如果有，我们尝试在第 42 行打开该文件进行写入，并在第 43–45 行尝试将`bitmap`写入其中。如果由于某种原因失败，我们将执行`catch`块中的代码，并在第 53 行`throw`一个`IOException`。由于`FileOutputStream`构造函数可能抛出多个异常，我们在第 52 行捕获一个通用的`Exception`以简化处理。

为了将`Bitmap bitmap`写入文件，我们使用了`Bitmap`类的`compress`方法，如表 12.14 所示。`compress`方法的第一个参数是文件压缩格式。`Bitmap.CompressFormat`枚举包含一些常量，可用于指定此类格式，如表 12.15 所列。`compress`方法的第二个参数是压缩质量。某些压缩算法（例如 PNG 格式的算法）是无损的，会忽略该参数的值。`compress`方法的第三个参数是输出流。如果我们要写入文件，可以使用`FileOutputStream`引用，因为`FileOutputStream`是`OutputStream`的子类。在第 45 行，我们指定了`PNG`格式和压缩质量级别`100`（尽管在此处无关紧要）。

| 方法 | 描述 |
| --- | --- |
| `static long elapsedRealtime()` | 返回自上次启动以来的时间（以毫秒为单位），包括休眠时间。 |

表 12.13 `SystemClock`类的`elapsedRealtime`方法

| 方法 | 描述 |
| --- | --- |
| `public final int getByteCount()` | 返回存储此 Bitmap 所需的最小字节数。 |
| `public boolean compress(Bitmap.Compress.Format format, int quality, OutputStream stream)` | 使用指定的格式`format`和由`quality`指定的压缩质量（`quality`介于 0（最小尺寸）和 100（最高质量）之间），将 Bitmap 的压缩版本写入`stream`。某些格式（如无损的 PNG）会忽略`quality`的值。 |

表 12.14 `Bitmap`类的`getByteCount`和`compress`方法

| 常量 | 描述 |
| --- | --- |
| `JPEG` | JPEG 格式 |
| `PNG` | PNG 格式 |
| `WEBP` | WebP 格式 |

表 12.15 `Bitmap.CompressFormat`枚举的常量

在第 46 行关闭文件后，我们在第 47 行测试`compress`方法是否返回了`true`（即`Bitmap`已正确写入文件）。如果是，我们在第 48 行返回`file`，否则在第 50–51 行`throw`一个`IOException`。

示例 12.15 展示了`MainActivity`类的第 4 版。当用户点击“保存图片”按钮时，会调用`savePicture`方法（第 65–74 行）。在第 68 行，我们调用`writeToExternalStorage`方法，传入`this`和`bitmap`。我们没有使用返回的`File`引用，因此没有捕获它。用户可以多次更改灰度参数并保存多张灰度图片。由于我们使用唯一名称命名文件，因此可以保存任意数量的图片。

由于应用会写入外部存储，因此必须通知潜在用户，并在`AndroidManifest.xml`文件的`manifest`元素内包含一个`uses-permission`元素，如下所示：

```xml
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

![](img/ch12exa15.jpg)

示例 12.15 `MainActivity`类，照片应用，第 4 版

图 12.7 展示了用户与滑块交互后应用运行的情况。“保存图片”按钮使用户能够保存灰度图片。

当我们运行应用并保存图片时，应用会给出`Toast`反馈。我们还可以打开应用存储图片的目录（位于设备的外部存储中）并查找我们的文件。图 12.8 展示了在依次点击左侧窗格中的`My Files`原生应用、`storage`、`emulated`、`0`、`Android`和`data`，导航到`data`目录后的平板电脑截图。接着，我们点击`com.jblearning.photograyingv4`目录（右侧顶部），然后点击`files`和`Pictures`。我们的图片现在可见。

如果我们将示例 12.14 中的第 28–29 行改为：

```java
File dir = activity.getExternalFilesDir("MyPix");
```

然后重新运行应用，并导航到`Pictures`目录旁边的`MyPix`目录，`MyPix`将包含应用生成的新灰度图片。

![](img/9781284093650_CH12_FIGF07.jpg)

图 12.7 照片应用第 4 版，在点击“保存”并与用户交互后

![](img/9781284093650_CH12_FIGF08.jpg)

图 12.8 导航查找存储的灰度图片时的平板电脑截图

## 12.6 使用电子邮件应用：将灰度图片发送给朋友，照片应用，第 5 版

现在我们已经知道如何将图片保存到文件，我们可以将该文件作为电子邮件的附件使用。在第 5 版中，我们将按钮内的文本“保存图片”替换为“发送图片”，并允许用户分享图片或将其作为附件通过电子邮件发送给朋友。

我们修改`activity_main.xml`文件中按钮的代码，如示例 12.16 所示。

示例 12.17 展示了`MainActivity`类的`sendEmail`方法（第 67–87 行）和新的`import`语句（第 6 行和第 15 行）。`sendEmail`方法替换了示例 12.16（照片应用第 4 版）中的`savePicture`方法。

在第 70 行，我们将`bitmap`写入外部存储，并返回`File`引用`file`。在第 71 行，我们调用`Uri`类的`fromFile`方法（如表 12.16 所示），并为`file`创建一个`Uri`引用`uri`。我们需要一个`Uri`引用来将文件附加到电子邮件中。`Uri`类来自`android.net`包，不要与`java.net`包中的`URI`类混淆，它封装了一个统一资源标识符（URI）。

![](img/ch12exa16.jpg)

示例 12.16 `activity_main.xml`文件，照片应用，第 5 版

![](img/ch12exa17.jpg)

### 示例 12.17 `MainActivity`类，照片应用，版本 5

| 方法 | 描述 |
| --- | --- |
| `static Uri fromFile( File file )` | 从文件创建并返回一个`Uri`；对除`/`以外的字符进行编码。 |

### 表 12.16 `Uri`类的`fromFile`静态方法

在第 72–79 行，我们使用表 12.17 中所示的`Intent`类常量创建并定义了一个用于发送数据的`Intent`。在第 72 行，我们使用`ACTION_SEND`常量创建了一个用于发送数据的`Intent`。在第 73 行，我们使用表 12.18 中所示的`setType`方法设置了`Intent`的多用途互联网邮件扩展（MIME）数据类型。我们在第 76–77 行定义了一个主题行，将其映射到`EXTRA_SUBJECT`的值。我们在第 79 行将`uri`作为附加数据添加到`Intent`中，并将其映射到`EXTRA_STREAM`的值：这意味着当我们发送数据时，`file`所代表的文件将成为附件。我们添加并注释掉了第 74–75 行和第 78 行。它们展示了如何使用`EXTRA_EMAIL`和`EXTRA_TEXT`常量添加收件人列表和邮件正文文本。对于此应用，最好让用户在邮件应用打开时自行填写空白内容。

| 常量 | 描述 |
| --- | --- |
| `ACTION_SEND` | 用于创建一个`Intent`以向某人发送数据。 |
| `EXTRA_EMAIL` | 用于指定电子邮件地址列表。 |
| `EXTRA_STREAM` | 与`ACTION_SEND`一起使用，指定一个包含与`Intent`关联的数据流的`URI`。 |
| `EXTRA_SUBJECT` | 用于指定消息中的主题行。 |
| `EXTRA_TEXT` | 与`ACTION_SEND`一起使用，定义要发送的文本。 |

### 表 12.17 `Intent`类的部分常量

| 方法 | 描述 |
| --- | --- |
| `Intent setType( String type )` | 设置此`Intent`的 MIME 数据类型；返回此`Intent`，以便可以链式调用方法。 |
| `Intent putExtra( String name, dataType value )` | 向此`Intent`添加数据。`name`是数据的键，`value`是数据。有多个`putExtra`方法，支持不同的数据类型。它返回此`Intent`，以便可以链式调用方法。 |
| `static Intent createChooser( Intent target, CharSequence title )` | 创建一个操作选择器`Intent`，以便用户可以通过用户界面在多个活动之间进行选择。`title`是用户界面的标题。 |

### 表 12.18 `Intent`类的`setType`和`createChooser`方法

在第 81–82 行，我们调用了表 12.18 中所示的`Intent`类的`createChooser`方法，并调用`startActivity`，传入返回的`Intent`引用。`createChooser`方法返回一个`Intent`引用，当我们用它启动一个活动时，用户会看到与`Intent`匹配的应用选择列表。由于我们使用`SEND_ACTION`常量创建了原始的`Intent`，因此会向用户展示能够发送数据的应用，例如`email`、`gmail`和其他应用。

图 12.9 显示了用户与滑块交互后我们的应用运行情况。“发送图片”按钮使用户能够保存并发送灰度图片。

图 12.10 显示了用户点击“发送图片”按钮后我们的应用运行情况。所有与发送数据意图匹配的可用应用都会显示出来。

![](img/9781284093650_CH12_FIGF09.jpg)

### 图 12.9 照片应用，版本 5，用户与滑块交互后

![](img/9781284093650_CH12_FIGF10.jpg)

### 图 12.10 照片应用，版本 5，用户点击“发送图片”后

![](img/9781284093650_CH12_FIGF11.jpg)

### 图 12.11 照片应用，版本 5，选择邮件应用后

图 12.11 显示了用户选择邮件后我们的应用运行情况。我们现在位于邮件应用内部，可以像编辑任何邮件一样进行编辑。

## 章节总结

- 一个应用可以使用另一个应用。
- 为了使用某个功能或另一个应用，我们在`AndroidManifest.xml`文件中包含一个`uses-feature`元素。
- `PackageManager`类的`hasSystemFeature`方法使我们能够检查 Android 设备上是否安装了某个功能或应用。
- 我们可以使用`Intent`类的`ACTION_IMAGE_CAPTURE`常量来打开相机应用。
- 我们可以使用`ImageView`类作为容器来显示图片。
- `Bitmap`类封装了基于 PNG 或 JPEG 等格式存储的图像。
- 如果图片存储在`Bitmap`中，我们可以访问图片中每个像素的颜色。
- `SeekBar`类（来自`android.widget`包）封装了一个滑块。
- 我们可以通过实现`SeekBar.OnSeekBarChangeListener`接口来捕获和处理`SeekBar`事件。
- 为了存储持久化数据，Android 设备始终具有内部存储，并且通常（但不总是）具有外部存储。
- `Context`类提供了可用于检索外部存储目录路径的方法。
- 为了写入外部存储，必须在`AndroidManifest.xml`文件中包含一个`uses-permission`元素。
- 我们可以使用`Bitmap`类的`compress`方法将`Bitmap`写入文件。
- `Uri`类的`fromFile`方法将`File`转换为`Uri`。
- 我们可以使用`Intent`类的`ACTION_SEND`常量创建一个`Intent`，以使用现有的邮件应用发送电子邮件。
- 我们可以使用`Intent`类的`createChooser`静态方法来显示与给定`Intent`匹配的多个可能应用。

![](img/common.jpg)

## 练习、问题与项目

### 多项选择题

1. 我们可以使用`PackageManager`类的哪个方法来检查 Android 设备上是否安装了某个应用？
   - `isInstalled`
   - `isAppInstalled`
   - `hasSystemFeature`
   - `hasFeature`

2. 我们可以使用`MediaStore`类的哪个常量来创建一个使用相机应用的`Intent`？
   - `ACTION_CAMERA`
   - `IMAGE_CAPTURE`
   - `ACTION_ CAPTURE`
   - `ACTION_IMAGE_CAPTURE`

3. 我们可以使用哪个类作为图片的容器？
   - `PictureView`
   - `ImageView`
   - `BitmapView`
   - `CameraView`

4. 问题 3 中类的哪个方法用于将`Bitmap`对象放入容器中？
   - `setBitmap`
   - `setImage`
   - `setImageBitmap`
   - `putBitmap`

5. 我们使用哪个键来检索存储在相机应用`Intent`的附加数据`Bundle`中的`Bitmap`？
   - `camera`
   - `picture`
   - `data`
   - `bitmap`

6. 我们使用`Bitmap`类的哪个方法来检索像素的颜色？
   - `getPixel`
   - `getColor`
   - `getPixelColor`
   - `getPoint`

7. 我们使用`Bitmap`类的哪个方法来修改像素的颜色？
   - `setPixel`
   - `setColor`
   - `setPixelColor`
   - `setPoint`

8. 问题 7 中的方法接受多少个参数？
   - 0
   - 1
   - 2
   - 3

9. 封装滑块的类名是什么？
   - `Slider`
   - `Bar`
   - `SeekBar`
   - `SliderView`

10. Android 设备上的存储类型有哪些？
    - 内部存储和外部存储
    - 仅内部存储
    - 仅外部存储
    - Android 设备上没有存储

11. `Context`类的哪个方法返回外部存储目录的绝对路径？
    - `getExternalPath`
    - `getInternalPath`
    - `getExternalFiles`
    - `getExternalFilesDir`

12. 我们可以使用`Bitmap`类的哪个方法将`Bitmap`写入文件？
    - `writeToFile`



- `compress`
- `write`
- `format`

## 13. 选择题

### 13.1 `Uri` 静态方法

我们使用 `Uri` 类的哪个静态方法从文件创建 `Uri`？

- `fromFile`
- 构造函数
- `createFromFile`
- `createUriFromFile`

### 13.2 `Intent` 常量

我们使用 `Intent` 类的哪个常量来创建用于发送数据的 `Intent`？

- `ACTION_SEND`
- `DATA_SEND`
- `EMAIL_SEND`
- `SEND`

## 补全代码

### 15. 检查相机应用

编写一段代码，输出到 `Logcat`，指示设备上是否有可用的相机应用。

### 16. 在 `ImageView` 中显示 `Bitmap`

编写代码，将名为 `myBitmap` 的 `Bitmap` 放入名为 `myImageView` 的 `ImageView` 中。

### 17. 将像素更改为红色

编写代码，将名为 `myBitmap` 的 `Bitmap` 中的所有像素更改为红色。

### 18. 将像素更改为灰色

编写代码，将名为 `myBitmap` 的 `Bitmap` 中的所有像素更改为灰色。灰度分别使用红色、绿色和蓝色的以下系数定义：0.5、0.2、0.3。

### 19. 检查外部存储

编写代码，根据当前设备是否有可用的外部存储，输出到 `Logcat` 的 `EXTERNAL STORAGE` 或 `NO EXTERNAL STORAGE`。

### 20. 输出 `Bitmap` 的字节数

编写代码，输出到 `Logcat` 名为 `myBitmap` 的 `Bitmap` 中的字节数。

### 21. 将 `Bitmap` 写入 JPEG 文件

编写代码，将名为 `myBitmap` 的 `Bitmap` 以 JPEG 格式写入文件，压缩质量级别为 50。

```java
// 假设 file 是一个之前已正确定义的 File 对象引用
try {
  FileOutputStream fos = new FileOutputStream(file);
  // 你的代码写在这里
}
catch (Exception e) {
}
```

### 22. 发送带附件的电子邮件

编写代码，创建一个 `Intent`，向 `mike@yahoo.com` 发送一封主题为 `HELLO`、内容为 `SEE PICTURE ATTACHED` 的电子邮件。将存储在名为 `myFile` 的 `File` 对象中的文件作为附件。

## 编写一个应用

### 23. 消除照片中的红色分量

编写一个应用，允许用户拍照、显示照片，并有一个按钮用于消除照片所有像素中的红色分量。包含一个 `Model`。

### 24. 消除照片中的指定颜色分量

编写一个应用，允许用户拍照、显示照片，并有三个单选按钮，用于消除照片所有像素中的红色、绿色或蓝色分量。包含一个 `Model`。

### 25. 显示照片的镜像

编写一个应用，允许用户拍照、显示照片，并有一个按钮让用户将照片变为其镜像（照片的左右两侧互换）。如果用户点击按钮两次，应用再次显示原始照片。包含一个 `Model`。

### 26. 为照片添加边框

编写一个应用，允许用户拍照、显示照片，并有一个按钮让用户在照片内显示一个边框（由你选择）。你可以用颜色和像素厚度来定义边框。包含一个 `Model`。

### 27. 发送带边框照片的电子邮件

与 26 相同，但增加一个按钮，用于发送带有边框照片的电子邮件。包含一个 `Model`。

### 28. 使用多种颜色的边框

编写一个应用，允许用户拍照、显示照片，并有一个按钮让用户在照片周围显示一个边框，边框可以有多种颜色（至少有三个单选按钮用于选择这些颜色）。包含一个 `Model`。

### 29. 循环显示两张照片

编写一个应用，允许用户拍摄两张照片，并在同一个 `ImageView` 容器中像动画 GIF 一样显示：照片 1 显示一秒，然后照片 2 显示一秒，然后照片 1 再显示一秒，如此循环。

### 30. 发送两张照片

与 29 相同，但增加一个按钮，用于通过电子邮件发送这两张照片。

### 31. 在照片上添加文本

编写一个应用，允许用户拍照、显示照片，并在照片上添加一些你选择的文本。你可以使用 `Canvas` 和 `Paint` 类，特别是接受 `Bitmap` 作为参数的 `Canvas` 构造函数。

### 32. 在照片上添加气泡和文本

与 31 相同，但增加一个气泡（你可以硬编码气泡的绘制）。文本放在气泡内部。

### 33. 添加晕影效果

编写一个应用，允许用户拍照、显示照片，并添加晕影效果。晕影效果是指图像边缘饱和度的降低。包含一个 `Model`。

# 第十三章：XML 与内容应用

![章节开篇图片](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

智能手机和平板电脑都内置了浏览器，用户可以通过它上网。然而，在小屏幕上显示常规网页可能会让人感到信息过载。内容应用是指那些从网站中精选内容进行展示的应用，使得信息量可控，用户体验更佳。这类内容应用在许多网站上都有，尤其是社交媒体网站和新闻网站。

通常，网站会提供频繁更新、格式一致的信息，供外部世界（尤其是应用开发者）使用。其中一种格式化的信息称为简易信息聚合（RSS）订阅源。典型的 RSS 订阅源不仅采用 XML 格式，而且通常使用通用元素，如 `item`、`title`、`link`、`description` 或 `pubDate`。为了为特定网站构建内容应用，我们需要了解该网站 RSS 订阅源的格式，并且需要能够解析该网站暴露的 XML 文件，以便显示其内容。

## 13.1 解析 XML、DOM 和 SAX 解析器、Web 内容应用（版本 0）

一个 XML 文档通常附带一个文档类型声明（DTD）文档：它包含了 XML 文档应遵循的规则。例如，它可以指定一个 `rss` 元素可以包含 0 个或多个 `item` 元素。它可以指定一个 `item` 元素必须恰好包含一个 `title` 元素和一个 `link` 元素。它还可以指定 `title` 元素必须包含纯文本。

在本章中，我们只关注 XML 本身，不考虑 DTD。我们假设我们解析的任何 XML 文档都是格式良好的，并且符合其 DTD 的规则。

解析 XML 文档有两种类型的解析器：

- DOM 解析器
- SAX 解析器

文档对象模型（DOM）解析器将 XML 文件转换为树。一旦 XML 被转换为树，我们就可以遍历树来修改元素、添加元素、删除元素或搜索元素或值。这与浏览器处理 HTML 文档的方式类似：它构建一棵树，一旦该树数据结构在内存中，就可以使用 JavaScript 访问、搜索或修改它。

如果我们将 XML 文档用作数据库的替代品，并且需要访问和修改该数据库，那么使用 DOM 解析器是一个不错的选择。但对于内容应用来说，情况通常并非如此。内容应用通常将 XML 文档转换为列表，并允许用户与列表交互。通常，该列表包含指向 URL 的链接。

为了将 XML 文档转换为列表，我们使用简单 API for XML（SAX）解析器。SAX 解析器在读取 XML 文档时构建一个列表。该列表的元素是对象。通常认为 SAX 解析器比 DOM 解析器更快。

例如，假设我们要解析示例 13.1 中显示的 XML 文档。

![示例 13.1](img/ch13exa01.jpg)

示例 13.1 一个简单的 XML 文档

DOM 解析器会将那个 XML 文档转换为类似于图 13.1 所示的树。实际上，树中的分支比图 13.1 显示的要多一些，因为元素之间的空字符串也是树的分支。

除了将 XML 文档视为树之外，我们也可以将其视为包含三个项目的列表。在这个文档中，每个项目都有一个标题和一个链接。我们可以编写一个 `Item` 类，包含两个 `String` 实例变量 `title` 和 `link`。SAX 解析器会将那个 XML 文档转换为包含三个元素的项目列表，如图 13.2 所示。

![图 13.1](img/9781284093650_CH13_FIGF01.jpg)

图 13.1 示例 13.1 中 XML 文档的树结构

![图 13.2](img/9781284093650_CH13_FIGF02.jpg)

图 13.2 示例 13.1 中 XML 文档的项目列表

| 接口 | 接收通知的类型 | 方法名称 |
| --- | --- | --- |
| `EntityResolver` | 与实体相关的事件 | `resolveEntity` |
| `DTDHandler` | 与 DTD 相关的事件 | `notationDcl`、`unparsedEntityDcl` |
| `ContentHandler` | 与逻辑相关的事件 | `startDocument`、`endDocument`、`startElement`、`endElement`、`characters` 以及其他方法 |
| `ErrorHandler` | 错误和警告 | `error`、`fatalError`、`warning` |

表 13.1 `EntityResolver`、`DTDHandler`、`ContentHandler` 和 `ErrorHandler` 接口

在应用的第 0 版中，我们专注于使用 SAX 解析器进行 XML 解析的过程。我们使用现有的 SAX 解析器来解析示例 13.1 中的 XML 文档，并将解析过程中各个步骤的反馈输出到 `Logcat`。

为此，我们构建了两个类：

- `SAXHandler` 类处理 XML 文档的各种元素，例如开始标签、结束标签以及标签之间的文本，这些元素由 SAX 解析器依次遇到。
- `MainActivity` 类。

我们将在 `res` 目录中创建一个 `raw` 目录，并将包含示例 13.1 中 XML 文档的 `test.xml` 文件放入其中。在本章稍后部分，我们将从 URL 动态读取 XML 文档。目前，我们尚未创建 `Item` 类。这将在第 1 版中完成。

`DefaultHandler` 类是 SAX 级别 2 事件处理器的基类。`DefaultHandler` 类实现了四个接口：`EntityResolver`、`DTDHandler`、`ContentHandler` 和 `ErrorHandler`。它将这些接口继承的所有方法实现为空操作（do-nothing）方法。表 13.1 展示了这四个接口及其方法。

使用 SAX 解析器解析 XML 文件时，可能会发生许多事件：例如，每当解析器遇到开始标签、结束标签或文本时，都会触发一个事件。`DefaultHandler` 类包含多个方法，这些方法在解析文档并发生事件时自动被调用。表 13.2 展示了其中一些方法。

例如，当解析器遇到开始标签时，会调用 `startElement` 方法；遇到结束标签时，会调用 `endElement` 方法；遇到文本时，会调用 `characters` 方法。这些方法被实现为空操作。为了处理这些事件，我们需要继承 `DefaultHandler` 类并重写我们感兴趣的方法。

XML 文档可以包含实体引用。实体引用使用特殊语法 `&nameOfTheEntity;`。例如，`&quot;` 是表示双引号（"）的实体引用，`&lt;` 表示小于号（<），`&amp;` 表示与符号（&）。这些是几个预定义实体引用中的一部分。我们还可以在 DTD 中添加用户定义的实体引用。为简单起见，我们假设本章中解析的 XML 文档不包含实体引用。

| 方法 | 描述 |
| --- | --- |
| `void startElement(String uri, String localName, String startElement, Attributes attributes)` | 当解析器遇到开始标签时调用；`uri` 是命名空间 URI，`localName` 是其本地名称；`startElement` 是开始标签的名称；`attributes` 包含在 `startElement` 标签内找到的（名称，值）对列表。 |
| `void endElement(String uri, String localName, String endElement)` | 当解析器遇到结束标签时调用。 |
| `void characters(char[] ch, int start, int length)` | 当解析器遇到字符数据时调用；`ch` 存储字符，`start` 是起始索引，`length` 是从 `ch` 中读取的字符数。 |

表 13.2 `DefaultHandler` 类的部分方法

| 方法 | 描述 |
| --- | --- |
| `void parse(InputStream is, DefaultHandler dh)` | 解析 XML 输入流 `is` 的内容，并使用 `dh` 处理事件。 |
| `void parse(File f, DefaultHandler dh)` | 解析 XML 文件 `f` 的内容，并使用 `dh` 处理事件。 |
| `void parse(String uri, DefaultHandler dh)` | 解析位于 `uri` 的 XML 文件的内容，并使用 `dh` 处理事件。 |

表 13.3 `SAXParser` 类的部分 `parse` 方法

要解析 XML 文档，我们调用 `SAXParser` 类的某个 `parse` 方法。表 13.3 列出了其中一些方法。它们指定了一个 `DefaultHandler` 参数，用于处理解析过程中遇到的事件。当我们重写 `DefaultHandler` 类时，需要重写其方法，以便在这些方法内部构建我们的项目列表。

示例 13.2 展示了我们的 `SAXHandler` 类（第 0 版）。我们重写了 `startElement`、`endElement` 和 `characters` 方法，这些方法都会抛出 `SAXException`。在这些方法内部，我们输出它们某些参数的值。与 SAX 相关的类位于 `org.xml.sax` 和 `org.xml.sax.helpers` 包中。这些类在第 3-5 行被导入。

如表 13.1 所示，`DefaultHandler` 类包含其他方法，例如 `error` 或 `fatalError`，这些方法在遇到 XML 文档中的错误时被调用。为简单起见，我们假设 XML 和 DTD 文档中没有任何类型的错误，因此我们不处理 XML 错误。

![示例 13.2](img/ch13exa02.jpg)

示例 13.2 `SAXHandler` 类，第 0 版

| 方法 | 描述 |
| --- | --- |
| `SAXParserFactory newInstance()` | 静态方法，创建并返回一个 `SAXParserFactory`。 |
| `SAXParser newSAXParser()` | 创建并返回一个 `SAXParser`。 |

表 13.4 `SAXParserFactory` 类的部分方法

`SAXParser` 类是 `abstract` 的，因此我们无法从中实例化对象。`SAXParserFactory` 类也是 `abstract` 的，它提供了创建 `SAXParser` 对象的方法。表 13.4 列出了其中的两个方法。`static` 的 `newInstance` 方法创建一个 `SAXParserFactory` 对象并返回其引用，而 `newSAXParser` 方法创建一个 `SAXParser` 对象并返回其引用。

| 方法 | 描述 |
| --- | --- |
| `InputStream openRawResource(int id)` | 打开并返回一个 `InputStream`，用于读取 ID 为 `id` 的资源的数据。 |

表 13.5 `Resources` 类的 `openRawResource` 方法

要创建 `SAXParser` 对象，我们可以使用以下序列：

```java
SAXParserFactory factory = SAXParserFactory.newInstance();
SAXParser saxParser = factory.newSAXParser();
```

在第 0 版中，我们将硬编码的 XML 文档存储在位于 `res` 目录的 `raw` 子目录中的文件中。因此，如果我们的文件名是 `test.xml`，我们可以使用资源 `R.raw.test` 来访问它。我们可以将该资源转换为输入流，并使用表 13.3 中列出的第一个 `parse` 方法。

`Context` 类的 `getResources` 方法（由 `Activity` 类继承）返回一个指向我们应用程序包的 `Resources` 引用。利用该 `Resources` 引用，我们可以调用表 13.5 中列出的 `openRawResource` 方法，以打开并获取一个 `InputStream` 引用，从而读取该资源中的数据。

我们可以链式调用 `getResources` 和 `openRawResource` 方法来打开一个输入流，从文件 `test.xml` 中读取数据，如下所示：

```java
InputStream is = getResources().openRawResource(R.raw.test);
```

为了解析一个名为 `is` 的 `InputStream`（其中包含 XML 文档），使用名为 `saxParser` 的 `SAXParser`，并利用名为 `handler` 的 `DefaultHandler` 引用来处理事件，我们按如下方式调用 `parse` 方法：

```java
saxParser.parse(is, handler);
```

示例 13.3 展示了 `MainActivity` 类。`SAXParser` 和 `SAXParserFactory` 类都属于 `javax.xml.parsers` 包，在第 7-8 行被导入。我们使用的各种方法可能会抛出许多异常：

> `newSAXParser` 抛出 `ParserConfigurationException` 和 `SAXException`。

> `openRawResource` 抛出 `Resources.NotFoundException`。

> `parse` 抛出 `IllegalArgumentException`、`IOException` 和 `SAXException`。



这些异常中有些是受检异常，有些是非受检异常。为简单起见，我们在第 14–20 行使用一个 `try` 块，并在第 20 行捕获一个通用的 `Exception`。在 `try` 块内部，我们在第 15–16 行创建一个 `SAXParser`，在第 17 行声明并实例化一个名为 `handler` 的 `SAXHandler`。我们在第 18 行打开一个输入流，读取位于 `res` 目录下 `raw` 目录中的 `test.xml` 文件数据，并在第 19 行使用 `handler` 开始解析该输入流。解析过程会触发对 `SAXHandler` 从 `DefaultHandler` 继承的各种方法的多次调用，特别是我们在示例 13.2 中重写的三个方法。

![](img/ch13exa03.jpg)

示例 13.3 `MainActivity` 类，版本 0

图 13.3 显示了运行应用时 `Logcat` 中的输出。我们观察到以下内容：

- ▸ 每当遇到开始标签时，我们会在 `startElement` 方法内执行，并且 `startElement` 参数的值就是该标签的名称。
- ▸ 每当遇到结束标签时，我们会在 `endElement` 方法内执行，并且 `endElement` 参数的值就是该标签的名称。
- ▸ 在同一元素的开始标签和结束标签之间，我们会在 `characters` 方法内执行，数组 `ch` 存储了开始标签和结束标签之间的字符（也称为元素内容）。
- ▸ 在一个元素的结束标签和另一个元素的开始标签之间，我们会在 `characters` 方法内执行，但文本仅包含空白字符。

![](img/9781284093650_CH13_FIGF03.jpg)

图 13.3 Web Content 应用的 `Logcat` 输出，版本 0

## 13.2 将 XML 解析为列表，Web Content 应用，版本 1

在版本 1 中，我们解析 `test.xml` 文件并将其转换为列表。我们将 `Item` 类编码为模型的一部分。`Item` 类封装了 XML 文档中的一个条目：它有两个 `String` 实例变量，`title` 和 `link`。在 `SAXHandler` 类中，我们构建一个 `Item` 对象的 `ArrayList`，以反映我们在 XML 文档中找到的内容。

示例 13.4 展示了 `Item` 类。它包含第 7–10 行的重载构造函数、第 12–13 行的修改器以及第 14–15 行的访问器。我们在第 16 行添加了一个 `toString` 方法，主要用于检查解析的正确性。

![](img/ch13exa04.jpg)

示例 13.4 `Item` 类，Web Content 应用，版本 1

在示例 13.5 所示的 `SAXHandler` 类（版本 1）中，我们构建了一个 `Item` 对象的 `ArrayList`。当调用 `startElement` 方法时，如果标签是 `item`，我们需要实例化一个新的 `Item` 对象。如果标签是 `title` 或 `link`，那么我们在 `characters` 方法中读取的文本就是当前 `Item` 对象的 `title` 或 `link` 实例变量的值。当调用 `endElement` 方法时，如果标签是 `item`，我们就完成了当前 `Item` 对象的处理，需要将其添加到列表中。

我们需要小心，在 `characters` 方法中处理正确的数据。在 XML 文档中，标签之间通常存在空白字符，例如在结束标签和开始标签之间。我们必须小心不要处理它们。我们想要处理的字符数据位于开始标签和对应的结束标签之间。因此，我们使用一个状态变量 `validText` 来评估我们在 `characters` 中处理的字符数据是否是我们想要处理的数据。当我们遇到开始标签时，将 `validText` 设置为 `true`。当我们遇到结束标签时，将 `validText` 设置为 `false`。只有当 `validText` 为 `true` 时，我们才在 `characters` 方法中处理字符数据。

![](img/ch13exa05.jpg)

示例 13.5 `SAXHandler` 类，Web Content 应用，版本 1

我们在第 9–12 行声明了四个实例变量：

- ▸ `validText`，一个 `boolean` 状态变量。如果其值为 `true`，我们在 `characters` 方法中处理字符数据，否则不处理。
- ▸ `element`，一个 `String`，存储当前元素（在此示例中为 `xml`、`rss`、`item`、`title` 或 `link`）。
- ▸ `currentItem`，一个 `Item`，存储当前的 `Item` 对象。
- ▸ `items`，一个 `ArrayList`，存储我们构建的 `Item` 对象列表。

构造函数（第 14–17 行）在第 15 行将 `validText` 初始化为 `false`，并在第 16 行实例化 `items`。我们在第 19 行编写了一个 `items` 的访问器，以便外部类可以访问它。

在 `startElement` 方法（第 21–28 行）中，我们在第 24 行将 `validText` 设置为 `true`，并在第 25 行将开始标签内的文本 `startElement` 赋值给 `element`。如果开始标签等于 `item`（第 26 行），我们实例化一个新的 `Item` 对象，并将其引用赋值给 `currentItem`（第 27 行）。

如果开始标签后面跟着结束标签，接下来会调用 `characters` 方法。如果 `currentItem` 不为 `null` 且 `validText` 为 `true`，并且 `element` 的值是 `title` 或 `link`（第 39 行和第 41 行），则我们正处于构建当前 `Item` 对象的过程中。如果 `element` 等于 `title` 或 `link`，我们将当前 `Item` 对象的 `title` 或 `link` 实例变量的值设置为读取到的字符（第 40 行和第 42 行）。

在调用 `startElement` 和 `characters` 方法之后，会调用 `endElement` 方法（第 30–35 行）。我们在第 32 行将 `false` 赋值给 `validText`。这样，在结束标签之后、开始标签之前找到的任何文本都不会被 `characters` 方法处理。如果 `element` 的值是 `item`（第 33 行），我们就完成了当前 `Item` 对象的处理，并将其添加到 `items` 中（第 34 行）。

示例 13.6 展示了 `MainActivity` 类，版本 1。在第 22 行，我们检索解析后的条目列表，并将其赋值给 `ArrayList` `items`。在第 23–24 行，我们遍历该列表并将其输出到 `Logcat`，以检查解析的正确性。

图 13.4 显示了运行应用（版本 1）时 `Logcat` 中的输出。我们可以检查到 `ArrayList` `items` 包含了 `test.xml` 文件中列出的三个 `Item` 对象。

![](img/ch13exa06.jpg)

示例 13.6 `MainActivity` 类，Web Content 应用，版本 1

![](img/9781284093650_CH13_FIGF04.jpg)

图 13.4 Web Content 应用的 `Logcat` 输出，版本 1

## 13.3 解析远程 XML 文档，Web Content 应用，版本 2

在版本 2 中，我们解析来自远程网站的 XML 文档。我们不再从 `test.xml` 文件读取数据，而是从 Jones & Bartlett Learning 的计算机科学博客的 RSS feed 中拉取数据。URL 是 [`www.blogs.jblearning.com/computer-science/feed/`](http://www.blogs.jblearning.com/computer-science/feed/)。我们访问互联网，打开该 URL，并读取该 URL 处的数据。从 Android 3.0 开始，Android 不允许应用在其主线程中打开 URL。线程是在现有进程中执行的一段代码序列。现有进程通常被称为主线程。对于 Android 应用，它也被称为用户界面线程。同一个进程中可以有多个线程同时执行。线程可以共享资源，例如内存。

当我们启动应用时，代码在主线程中执行，因此我们需要在另一个线程中打开该 URL。此外，我们需要在尝试用数据填充列表之前，确保后台线程中的 XML 解析已完成，因为列表使用的是后台线程读取的数据。`android.os` 包中的 `AsyncTask` 类允许我们执行后台操作，然后访问主线程以传递其结果。它设计用于执行短任务（持续几秒或更短），不应用于启动长时间运行的线程。`AsyncTask` 是 `abstract` 的，因此我们必须创建其子类并实例化子类对象才能使用它。附录 D 详细解释了 `AsyncTask`，并包含一个使用 `AsyncTask` 的非常简单的应用。

我们创建 `ParseTask` 类，它是 `AsyncTask` 的子类，用于解析来自远程服务器的 RSS 源。我们执行以下步骤：

- 创建 `ParseTask`，它是 `AsyncTask` 的子类。
- 重写 `doInBackground` 方法，使其解析我们感兴趣的 XML 文档。
- 在 `ParseTask` 内部，包含一个实例变量，该变量是对启动任务的 Activity 的引用。这使我们能够从 `ParseTask` 调用 Activity 类的方法。
- 重写 `onPostExecute` 方法，并调用 Activity 类的方法，用刚完成的任务结果更新 Activity。
- 在 Activity 内部，创建并实例化一个 `ParseTask` 对象。
- 将对此 Activity 的引用传递给 `ParseTask` 对象。
- 调用 `AsyncTask` 的 `execute` 方法，传入一个 URL，以开始执行任务。

`AsyncTask` 类使用了三个泛型类型，在扩展它时必须指定。子类的类头如下：

```java
AccessModifier ClassName extends AsyncTask<Params, Progress, Result>
```

其中 `Params`、`Progress` 和 `Result` 是实际类名的占位符，含义如下：

- `Params` 是调用 `execute` 方法时传递给 `AsyncTask` 的数组的数据类型。
- `Progress` 是任务在后台执行时用于进度单位的数据类型。如果选择报告进度，该数据类型通常是 `Integer` 或 `Long`。
- `Result` 是任务执行完成后返回的值的数据类型。

在此应用中，我们希望将 `Strings` 数组（表示 URL）作为 `execute` 方法的参数传递，我们不关心报告进度，任务返回一个 `Item` 对象的 `ArrayList`。因此，我们使用以下类头：

```java
public ParseTask extends AsyncTask<String, Void, ArrayList<Item>>
```

| 方法 | 描述 |
| --- | --- |
| `AsyncTask execute( Params... params )` | `params` 表示类型为 `Params`（泛型类型）的值数组。 |
| `Result doInBackground( Params... params )` | `params` 是调用 `execute` 时传递给它的参数。 |
| `void onPostExecute( Result result )` | 在 `doInBackground` 完成后自动调用。`Result` 是 `doInBackground` 返回的值。 |

表 13.6 `AsyncTask` 类的选定方法

为了使用 `AsyncTask` 类启动任务，我们执行以下操作：

- 创建 `AsyncTask` 的子类。
- 声明并实例化该子类的对象。
- 使用该对象调用 `execute` 方法启动任务。

当我们使用 `ParseTask` 引用调用 `execute` 方法后，`doInBackground` 方法执行，其参数与传递给 `execute` 的参数相同。其返回值成为 `onPostExecute` 的参数，`onPostExecute` 在 `doInBackground` 完成后自动调用。表 13.6 显示了这三个方法。`execute` 和 `doInBackground` 的方法头表明它们都接受可变数量的参数。

当我们调用 `execute` 方法时，`AsyncTask` 类的以下方法按此顺序执行：`onPreExecute`、`doInBackground` 和 `onPostExecute`。

在任务执行之前，如果我们想执行一些初始化，可以将代码放在 `onPreExecute` 方法中。我们将要执行的任务的代码放在 `doInBackground` 方法中。该方法是 `abstract` 的，必须重写。自动传递给 `doInBackground` 方法的参数与调用 `execute` 方法时传递给它的参数相同。在 `doInBackground` 内部，当任务执行时，如果我们想向主线程报告进度，可以调用 `publishProgress` 方法。这反过来会触发对 `onProgressUpdate` 方法的调用，我们可以重写该方法：例如，可以在用户界面线程中更新进度条。当 `doInBackground` 方法执行完毕后，会调用 `onPostExecute` 方法。我们可以重写它，用刚完成的任务结果更新用户界面。自动传递给 `onPostExecute` 方法的参数是 `doInBackground` 方法返回的值。

总结数据流：传递给 `execute` 的参数被传递给 `doInBackground`，而 `doInBackground` 的返回值被作为 `onPostExecute` 的参数传递。

在我们的 `ParseTask` 类中，Params 数据类型是 `String`，Result 数据类型是 `ArrayList`。因此，`doInBackground` 方法具有以下方法头：

```java
protected ArrayList<Item> doInBackground( String... urls )
```

![](img/ch13exa07.jpg)

示例 13.7 `ParseTask` 类，Web 内容应用，版本 2

示例 13.7 展示了 `ParseTask` 类。在类头（第 9 行）中，我们指定 `String` 作为 `Params` 数据类型，`Void` 作为 `Progress` 数据类型（因为在此应用中我们不报告进度），`ArrayList` 作为 `Result` 数据类型。

在第 10 行，我们声明了 `activity` 实例变量，它是对 `MainActivity` 的引用。构造函数（第 12–14 行）接受一个 `MainActivity` 参数并将其赋值给 `activity`。当我们在 `MainActivity` 类中调用该构造函数时，我们传递 `this` 作为参数。

我们在第 16–27 行重写了 `doInBackground` 方法。方法头指定它返回一个 `Item` 对象的 `ArrayList`（`Result` 数据类型），并接受 `Strings` 作为参数（`Params` 数据类型）。

解析 XML 的代码与示例 13.6 基本相同，不同之处在于我们在第 21 行使用了 `parse` 方法，其第一个参数是表示 URL 的 `String`，而不是之前的 `InputStream`。我们期望只向该方法传递一个参数，因此我们只处理第一个参数，通过表达式 `urls[0]` 访问。我们不期望此时 `urls` 为 `null`，但即使如此，我们在第 23 行捕获了该异常。在第 22 行，我们返回解析 XML 文档时生成的 `Item` 对象的 `ArrayList`。

我们在第 29–31 行重写了 `onPostExecute` 方法。当 `doInBackground` 方法执行完毕后自动调用该方法时，其参数 `returnedItems` 的值是 `doInBackground` 返回的 `Item` 对象的 `ArrayList`。我们使用 `activity` 实例变量调用 `MainActivity` 类的 `displayList` 方法，在第 30 行传递 `returnedItems`。在 `MainActivity` 类内部，我们需要编写 `displayList` 方法。

由于我们的应用访问互联网，我们需要在 `AndroidManifest.xml` 文件的 `manifest` 元素内添加适当的权限代码，如下所示：

```xml
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
```

示例 13.8 展示了 `MainActivity` 类。我们在第 9–10 行声明了一个名为 `URL` 的 `String` 常量，用于存储 RSS 订阅源的 URL。在第 15 行，我们声明并实例化了一个 `ParseTask` 对象，并在第 16 行调用 `execute` 方法，传入 `URL`。由于 `execute` 方法接受可变数量的参数，我们可以传入 0 个、1 个或多个参数。或者，我们也可以传入一个只包含一个元素 `URL` 的 `String` 数组，如下所示：

```java
task.execute(new String[ ] { URL } );
```

![](img/ch13exa08.jpg)

示例 13.8 `MainActivity` 类，Web 内容应用，版本 2

![](img/9781284093650_CH13_FIGF05.jpg)

图 13.5 Web Content 应用版本 2 的 `Logcat` 输出

在第 19–24 行，我们编写了 `displayList` 方法。此时，它会将参数 `items` 的内容输出到 `Logcat`。`Items` 可能为 `null`，因此我们在第 20 行 `for` 循环之前对其进行了检查。



请注意，当我们使用`AsyncTask`时，代码的执行顺序很重要。在第 16 行调用`execute`之后，如果第 16 行之后还有语句，执行将继续在`onCreate`方法内进行。在这种情况下，这些语句与`ParseTask`类内部执行的语句之间会出现交错执行。如果我们试图在`onCreate`方法中第 16 行之后立即检索`Item`对象的`ArrayList`，它很可能是`null`。处理任务结果的正确方式是在`onPostExecute`方法内部进行。

图 13.5 展示了运行应用版本 2 时 Logcat 中的部分输出。请注意，这是一个实时博客，因此内容可能每天变化，可能与图中的输出不匹配。

## 13.4 在`ListView`中显示结果，Web 内容应用，版本 3

在版本 0、1 和 2 中，我们没有用户界面。在版本 3 中，我们在屏幕上显示从 XML 文档中检索到的所有标题列表。

为了保持示例简单，我们只允许应用在竖屏模式下运行。因此，我们在`AndroidManifest.xml`文件的`activity`元素中添加以下内容：

```
android:screenOrientation="portrait"
```

为了在屏幕上以列表形式显示标题，我们在`activity_main.xml`文件中使用了一个`ListView`元素。`ListView`包含任意数量的`String`。我们在定义`ListView`时无需指定元素数量。因此，我们可以动态构建一个`Item`对象的`ArrayList`，并通过编程方式将相应的标题列表放入`ListView`中。

示例 13.9 展示了`activity_main.xml`文件，版本 3。我们将骨架文件中显示`Hello World!`的`TextView`替换为第 12–16 行的`ListView`元素。我们在第 12 行为其指定了一个`id`，以便通过代码使用`findViewById`方法访问它并填充数据。我们在第 15–16 行使用了`android:divider`和`android:dividerHeight`属性，在显示的项目之间添加一条红色、`2`像素粗的分隔线。

![](img/ch13exa09.jpg)

示例 13.9 `activity_main.xml`文件，Web 内容应用，版本 3

示例 13.10 展示了`ParseTask`类，版本 3。在第 24–25 行，我们将示例 13.7 第 24 行中输出到 Logcat 的语句替换为一条`Toast`语句。连同第 4 行导入`Toast`的语句，这是仅有的改动。

示例 13.11 展示了`MainActivity`类，版本 3。我们在第 13 行包含了一个`ListView`实例变量`listView`。

在`displayList`方法（第 23–36 行）中，我们用`ArrayList items`中的所有标题填充`listView`。我们在第 25–28 行生成了`titles`，一个包含`items`中标题的`String`类型的`ArrayList`。在第 30–31 行，我们创建了一个包含`titles`的`ArrayAdapter`。我们使用了表 13.7 中列出的构造函数，传入了三个参数。第一个参数是`this`，即当前活动的引用（`Activity`继承自`Context`）。第二个参数是`android.R.layout.simple_list_item_1`，这是`R.layout`类的一个常量。它是一个简单的布局，可用于显示一些文本。第三个参数是`titles`，它是一个`ArrayList`，因此也是一个`List`。

![](img/ch13exa10.jpg)

示例 13.10 `ParseTask`类，Web 内容应用，版本 3

![](img/ch13exa11.jpg) ![](img/ch13exa11a.jpg)

示例 13.11 `MainActivity`类，Web 内容应用，版本 3

| 构造函数 | 描述 |
| --- | --- |
| `ArrayAdapter(Context context, int textViewResourceId, List<T> objects)` | `Context`是当前上下文；`textViewResourceId`是包含`TextView`的布局资源的`id`；`objects`是类型为`T`的对象列表。 |

表 13-7 `ArrayAdapter`类的选定构造函数

我们在第 18 行使用其`id`检索在`activity_main.xml`中定义的`ListView`，并将其赋值给`listView`。在第 32 行，我们调用`ListView`类的`setAdapter`方法（如表 13.8 所示），将标题列表设置为`listView`中显示的列表。`adapter`引用实际上是一个`ArrayAdapter`，因此也是一个`ListAdapter`，因为`ArrayAdapter`继承自`ListAdapter`接口。`ListAdapter`是`ListView`与其数据列表之间的桥梁。

| 方法 | 描述 |
| --- | --- |
| `void setAdapter(ListAdapter adapter)` | 将此`ListView`的`ListAdapter`设置为`adapter`；`adapter`存储支持此`ListView`的数据列表，并为数据列表中的每个项目生成一个`View`。 |

表 13.8 `ListView`类的`setAdapter`方法

此时，我们没有设置任何列表事件处理；我们将在版本 4 中进行。如果`items`为`null`，我们在第 34–35 行显示一条`Toast`。

图 13.6 展示了在模拟器中运行的应用版本 3。

![](img/9781284093650_CH13_FIGF06.jpg)

图 13.6 在模拟器中运行的 Web 内容应用版本 3

## 13.5 在应用内打开网页浏览器，Web 内容应用，版本 4

在版本 4 中，我们在用户从列表中选择的 URL 处打开浏览器。为此，我们执行以下操作：

- 当用户从列表中选择一个项目时实现事件处理。
- 检索与该项目关联的链接。
- 在链接包含的 URL 处打开浏览器。

在版本 3 中，我们的列表显示了通过解析 XML 文档生成的`Item`对象的`ArrayList`的标题。在版本 4 中，我们实际上需要访问链接值。为了检索给定`Item`对象的链接，我们向`MainActivity`类添加一个实例变量，该变量表示`Item`对象的列表。当用户从列表中选择一个项目时，我们检索其索引，从`ArrayList`中检索该索引处的`Item`对象，并检索该`Item`的`link`实例变量的值。

示例 13.12 展示了`MainActivity`类，版本 4。在第 18 行，我们声明了`listItems`实例变量，它是一个`Item`对象的`ArrayList`。在`displayList`内部，第 29 行，我们将参数`items`赋值给`listItems`。

![](img/ch13exa12.jpg) ![](img/ch13exa12a.jpg)

示例 13.12 `MainActivity`类，Web 内容应用，版本 4

`OnItemClickListener`是`AdapterView`类的一个`public`内部接口。它包含一个`abstract`回调方法`onItemClick`。当用户从与`AdapterView`关联的列表中选择一个项目时，如果有一个`OnItemClickListener`对象正在监听该列表上的事件，该方法会自动被调用。表 13.9 展示了`onItemClick`方法。

为了实现列表事件处理，我们执行以下操作：

- 我们在第 47–56 行编写了一个扩展`OnItemClickListener`的`private`处理程序类，并在第 49–55 行重写了其唯一的`abstract`方法`onItemClick`。
- 我们在第 40 行声明并实例化了该类的一个对象。
- 我们在第 41 行将该处理程序注册到`ListView`上，以便它监听列表事件。

| 方法 | 描述 |
| --- | --- |
| `void onItemClick(AdapterView<?> parent, View view, int position, long id)` | 当列表中的某个项被选中时调用此方法：`parent`是`AdapterView`；`view`是`AdapterView`中被选中的视图；`position`是视图在`AdapterView`中的位置；`id`是被选中项的行索引。 |

表 13.9 `OnItemClickListener`接口

| 方法 | 描述 |
| --- | --- |
| `static Uri parse(String uriString)` | 创建一个解析`uriString`并返回其引用的`Uri`对象。 |

表 13.10 `Uri`类的`parse`方法

`onItemClick`方法的参数`position`存储了用户所选中的项在列表中的索引。我们在第 51 行用它来检索`listItems`中该索引处的`Item`对象。在第 52 行，我们使用`Uri`类的`static parse`方法（如表 13.10 所示）创建一个`Uri`对象，该对象包含该`Item`对象的`link`实例变量中存储的`String`。在第 53 行，我们创建一个`Intent`来在该`Uri`处打开网页浏览器。我们将`Intent`类的`ACTION_VIEW`常量和`Uri`对象传递给`Intent`构造函数。在第 54 行，我们使用该`Intent`启动一个新的活动。由于该活动是打开浏览器，因此没有与该活动关联的布局文件和类。

图 13.7 展示了用户从列表中选择一个项后，在模拟器中运行的应用（版本 4）。如果我们点击模拟器的返回按钮，就会返回到链接列表，该列表随后成为活动栈顶部的活动。

![](img/9781284093650_CH13_FIGF07.jpg)

图 13.7 用户从列表中选择一个项后，在模拟器中运行的 Web Content 应用（版本 4）

## 章节总结

- XML 解析器有两种类型：DOM 和 SAX。
- DOM 解析器将 XML 文档转换为树结构。SAX 解析器顺序读取 XML 文档并报告其发现的内容。我们可以用它来将 XML 文档转换为对象列表。
- 我们可以使用`SAXParserFactory`类来获取`SAXParser`引用。
- `SAXParser`类包含多个解析 XML 文档的方法。
- 我们可以扩展`DefaultHandler`类，使用 SAX 解析器解析 XML 文档。
- `DefaultHandler`类包含回调方法，这些方法在解析 XML 文档时自动被调用。例如，当解析器遇到开始标签时，会调用`startElement`方法。
- Android 的最新版本不允许我们在应用的主线程上打开 URL。我们需要在单独的线程上执行此操作。
- 我们可以扩展`AsyncTask`类来提供线程功能。
- 调用`AsyncTask`类的`execute`方法会依次触发其`preExecute`、`doInBackground`和`postExecute`方法的执行。
- 传递给`execute`的参数会依次传递给`doInBackground`，而`doInBackground`的返回值则作为`postExecute`的参数传递。
- 为了从应用访问互联网，我们需要在`AndroidManifest.xml`文件中为其包含一个`uses-permission`元素。
- 我们可以使用`ListView`来显示项目列表。
- 要对`ListView`执行事件处理，我们可以实现`AdapterView`类的`OnItemClickListener`内部接口，并重写其`onItemClick`方法。
- `Uri`类封装了统一资源标识符。
- 我们可以使用`Intent`类的`ACTION_VIEW`常量和`Uri`对象创建一个意图来打开浏览器。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. DOM 代表什么？
   - 直接对象模型
   - 文档对象模型
   - 文档导向模型
   - 直接导向模型

2. SAX 代表什么？
   - 超级适配器 XML
   - 简单 API 扩展
   - 用于 XML 的简单 API
   - 用于 XML 的简单 Android

3. 当解析器遇到开始标签时，会调用`DefaultHandler`类的哪个方法？
   - `startElement`
   - `startTag`
   - `start`
   - `tag`

4. 当解析器遇到结束标签时，会调用`DefaultHandler`类的哪个方法？
   - `endElement`
   - `endTag`
   - `end`
   - `tag`

5. 当解析器遇到字符数据时，会调用`DefaultHandler`类的哪个方法？
   - `data`
   - `characterData`
   - `foundCharacters`
   - `characters`

6. 我们调用`AsyncTask`类的哪个方法来启动任务？
   - `start`
   - `run`
   - `execute`
   - `startTask`

7. 问题 6 中方法的参数会成为哪个方法的参数？
   - `preExecute`
   - `doInBackground`
   - `postExecute`
   - `publishProgress`

8. `doInBackground`方法的返回值会成为哪个方法的参数？
   - `preExecute`
   - `doInBackground`
   - `postExecute`
   - `publishProgress`

9. 我们可以使用`Intent`类的哪个常量来创建打开浏览器的意图？
   - `ACTION_BROWSER`
   - `ACTION_VIEW`
   - `WEB_VIEW`
   - `WEB_BROWSER`

### 补全代码

10. 以下代码开始解析位于`res`目录下`raw`目录中的名为`myFile.xml`的文件，使用`DefaultHandler` `myHandler`（假设`SAXHandler`扩展了`DefaultHandler`）。

```java
SAXParserFactory factory = SAXParserFactory.newInstance( );
SAXParser saxParser = factory.newSAXParser( );
SAXHandler myHandler = new SAXHandler( );
// 你的代码写在这里
```

11. 在`DefaultHandler`类的`characters`方法内部，将解析器读取的字符赋值给一个名为`myString`的`String`。

```java
public void characters( char ch [ ], int start, int length )
     throws SAXException {
 String myString;
 // 你的代码写在这里
}
```

12. 我们正在编写一个名为`MyTask`的类，它扩展了`AsyncTask`。我们期望向`execute`方法传递一个`Integer`数组，并期望`doInBackground`方法返回一个`Double`的`ArrayList`。我们不关心报告进度。请写出`MyTask`的类头。

13. 我们正在编写一个名为`MyTask2`的类，它扩展了`AsyncTask`。我们期望向`execute`方法传递一个`Double`，并期望`doInBackground`方法返回一个`String`。我们希望将进度报告为`Integer`。请写出`MyTask2`的类头。

14. 我们已经编写了一个名为`MyTask`的类，它扩展了`AsyncTask`。`doInBackground`接受可变数量的`Integer`作为参数。开始执行任务，传递一个或多个值。

```java
// 我们在一个活动类内部
MyTask myTask = new MyTask( this );
// 你的代码写在这里（仅一条语句）？
```

15. 编写一个私有类，实现`OnItemClickListener`接口，并将其方法重写为空方法。

16. 在一个活动内部，编写代码在[`www.google.com`](http://www.google.com)处打开浏览器。

### 编写应用

17. 编写一个类似于本章中的应用：使用不同的 URL，并显示发布日期以及标题。

18. 编写一个类似于本章中的应用：使用不同的 URL，并仅显示最近 30 天内发布的标题。

19. 编写一个类似于本章中的应用：使用不同的 URL，并添加一个文本字段，让用户指定他们希望数据有多新。例如，如果用户输入 45，则仅显示发布日期在最近 45 天内的结果。

20. 编写一个类似于本章中应用的应用程序：使用不同的 URL，并添加一个带有文本字段的前端活动，让用户指定搜索词，以便显示的标题包含该搜索词。

21. 编写一个应用程序，在`ListView`中向用户展示一个你选择的网站列表。当用户点击其中一个时，浏览器会打开该网站。



# 第十四章：制作一个 Android 小部件

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

应用小部件，也称为小部件，是嵌入在其他应用（称为小部件宿主）中的小型应用。主屏幕和锁屏就是小部件宿主的例子。我们也可以实现自己的小部件宿主，但这超出了本章的范围。小部件可以接收定期更新并相应地更新其视图。自动定期更新的最小频率是 30 分钟。许多 Android 设备都预装了原生小部件。一个众所周知且常见的小部件是来自`www.accuweather.com`的天气应用小部件。在本章中，我们将创建一个小部件，用于显示用户在安装小部件时指定的位置的当前温度。

## 14.1 制作小部件的步骤：温度小部件，版本 0

为了创建一个小部件，我们首先使用空活动模板创建一个标准的 Android 应用程序项目。虽然我们可以重用（并修改）`activity_main.xml`文件，但我们选择在布局目录中为小部件创建一个新的布局文件。我们将其命名为`widget_layout.xml`。

`android.appwidget`包中包含使我们能够创建和管理小部件的类。表 14.1 列出了其中一些类。

为了创建小部件，我们需要执行以下操作：

- ▸ 在`AndroidManifest.xml`文件的`application`元素内添加一个`receiver`元素。
- ▸ 在`res/xml`目录下的可扩展标记语言（XML）资源中定义一个`AppWidgetProviderInfo`对象。
- ▸ 在`res/layout`目录下的 XML 文件中定义一个小部件布局。
- ▸ 扩展`AppWidgetProvider`类或`BroadcastReceiver`类。

在版本 0 中，我们创建一个非常简单的小部件，显示一个硬编码的字符串。

| 类 | 描述 |
| --- | --- |
| `AppWidgerProvider` | 一个便利类，我们可以扩展它来实现小部件提供程序。这个类包含小部件的生命周期方法，我们可以重写这些方法。 |
| `AppWidgetProviderInfo` | 描述小部件提供程序中的元数据，例如图标、最小宽度和高度、更新频率等。 |
| `AppWidgetManager` | 管理小部件提供程序和小部件。 |

表 14.1 `android.appwidget`包中的选定类

首先，我们更新`AndroidManifest.xml`文件。我们在`AndroidManifest.xml`文件的`application`元素内包含一个`receiver`元素，使用以下模式：

```xml
<receiver android:name="AppWidgetProviderClassName">
  <intent-filter>
    <action android:name="android.appwidget.action.APPWIDGET_UPDATE" />
  </intent-filter>
  <meta-data android:name="android.appwidget.provider"
             android:resource="@xml/name_of_widget_info_file" />
</receiver>
```

在这个例子中，`TemperatureProvider`是我们扩展`AppWidgetProvider`的类的名称，而`widget_info.xml`是位于`res`目录的`xml`目录中的文件名称，该文件包含小部件信息，例如大小和更新频率。

示例 14.1 显示了`AndroidManifest.xml`文件。在第 12–22 行，`receiver`元素替换了默认的`activity`元素。第 12 行`receiver`元素内的`android:name`属性是必需的。它的值是扩展`AppWidgetProvider`的类的名称。`intent-filter`元素内的`action`元素（第 14–15 行）是必需的，并且必须有一个`android:name`属性，其值等同于`AppWidgetManager`类的`ACTION_APPWIDGET_UPDATE`常量。这意味着这个小部件会按照小部件信息 XML 文件中指定的频率接收更新广播。第 18–20 行的`meta-data`元素通过其`android:name`和`android:resource`属性（两者都是必需的）指定了`AppWidgetProviderInfo`信息：

![](img/ch14exa01.jpg)

示例 14.1 `AndroidManifest.xml`文件

- ▸ `android:name`属性指定了元数据名称：值`android.appwidget.provider`用于将元数据标识为`AppWidgetProviderInfo`类型（第 19 行）。
- ▸ `android:resource`属性指定了包含`AppWidgetProviderInfo`信息的 XML 文件的资源位置和名称（第 20 行）。

示例 14.2 显示了`widget_info.xml`文件。它在 XML 资源中定义了一个`AppWidgetProviderInfo`对象。表 14.2 显示了`AppWidgetProviderInfo`类的一些`public`实例变量和相应的 XML 属性。

![](img/ch14exa02.jpg)

示例 14.2 `widget_info.xml`文件

`res`目录默认不包含`xml`目录，因此我们需要创建它。由于我们在示例 14.1 的`AndroidManifest.xml`文件中指定了`widget_info`作为定义`AppWidgetProviderInfo`对象的 XML 文件的名称，因此我们在`xml`目录中添加了一个名为`widget_info.xml`的 XML 文件。该文件必须包含一个单独的`appwidget-provider`元素。它在示例 14.2 的第 2–8 行中定义。在第 4 行，我们指定了位于`res/layout`目录中的`widget_layout.xml`作为小部件的布局资源。在第 5–6 行，我们将其最小高度和宽度设置为`50`和`200`像素。这些将是小部件创建并添加到宿主时的宽度和高度。Android 主屏幕被组织成一个单元格网格，小部件（和图标）可以放置在其中。网格可能因设备而异。

例如，手机可能是 4 × 4，平板电脑可能是 8 × 7。小部件所需的水平或垂直单元格数量分别是容纳`minWidth`或`minHeight`像素所需的最小单元格数量。表 14.3 显示了 Google 的建议。例如，如果我们有一个小部件，其`minWidth`值为`200`，`minHeight`值为`70`，那么它的图形表示将被分配一个 2 × 4 的单元格矩形：`200`密度像素需要 4 个垂直单元格，`70`密度像素需要 2 个水平单元格。

| 公共实例变量 | XML 属性 | 描述 |
| --- | --- | --- |
| `int minWidth` | `android:minWidth` | 小部件添加到宿主时的宽度，以 dp 为单位。 |
| `int minHeight` | `android:minHeight` | 小部件添加到宿主时的高度，以 dp 为单位。 |
| `int minResizeWidth` | `android:minResizeWidth` | 小部件可以调整大小的最小宽度，以 dp 为单位。 |
| `int minResizeHeight` | `android:minResizeHeight` | 小部件可以调整大小的最小高度，以 dp 为单位。 |
| `int updatePeriodMillis` | `android:updatePeriodMillis` | 小部件的更新频率，以毫秒为单位。最小频率为 30 分钟。 |
| `int widgetCategory` | `android:widgetCategory` | 指定此小部件是否可以显示在主屏幕、锁屏（Keyguard）或两者上。 |

表 14.2 `AppWidgetProviderInfo`类的选定`public`实例变量和 XML 属性

| 每个维度的单元格数 | 小部件最大维度（密度像素 dp） |
| --- | --- |
| n | `70 * n – 30` |
| 1 | 40 |
| 2 | 110 |
| 3 | 180 |
| 4 | 250 |

表 14.3 单元格数与小部件每个维度大小的关系

在第 7 行，我们将更新频率设置为`1800000`毫秒，即`30`分钟。这是小部件可以自动更新的最小频率。但是，我们可以通过在小部件上设置一些事件处理（例如，用户触摸小部件）来通过代码触发小部件更新。我们将在版本 2 中实现这一点。

示例 14.2 在第 4 行指定了小部件的布局定义在`widget_layout.xml`文件中。虽然小部件通常尺寸较小且 GUI 简单，但小部件也可以拥有复杂的 GUI，不过存在一些限制。表 14.4 列出了小部件可以使用的视图和布局管理器。

| 视图 | `AnalogClock`、`Button`、`Chronometer`、`ImageButton`、`ImageView`、`ProgressBar`、`TextView`、`ViewFlipper`、`ListView`、`GridView`、`StackView`、`AdapterViewFlipper` |
| --- | --- |
| 布局管理器 | `FrameLayout`、`LinearLayout`、`RelativeLayout`、`GridLayout` |

表 14-4 小部件中可使用的视图和布局管理器

示例 14.3 展示了`widget_layout.xml`文件。它采用`LinearLayout`（第 2 行）组织，仅包含一个`TextView`（第 7–12 行），该版本使用字符串资源`city_and_temp`（第 11 行）显示了一些硬编码文本；`city_and_temp`在`strings.xml`中定义如下：

```xml
<string name="city_and_temp">New York, NY\n75\u00B0F</string>
```

它使用 Unicode 字符`\u00B0`来编码度数符号（°）。在`strings.xml`中，我们将`app_name`字符串的值从`TemperatureWidgetV0`改为`TemperatureV0`。

![](img/ch14exa03.jpg)

示例 14.3 `widget_layout.xml`文件

现在，我们创建一个继承自`AppWidgetProvider`的类。如示例 14.1 的`AndroidManifest.xml`文件中所指定，我们将其命名为`TemperatureProvider`。表 14.5 展示了`AppWidgetProvider`类的一些生命周期方法。第 2 列中的常量来自`AppWidgetManager`类。至少，我们需要重写`onUpdate`方法以显示小部件。`onUpdate`方法提供了三个参数：

- ▸ 一个`Context`引用，指向运行此`AppWidgetProvider`的上下文。
- ▸ 一个`AppWidgetManager`：它使我们能够更新当前类型的一个或多个小部件。
- ▸ 一个小部件 ID 数组：需要更新的该提供者的小部件的 ID。

| 方法 | 广播类型（或 Intent 的动作值） | 描述 |
| --- | --- | --- |
| `void onUpdate(Context context, AppWidgetManager manager, int [ ] appWidgetIds)` | `ACTION_APPWIDGET_UPDATE` | 当此小部件首次运行以及更新时（按`updatePeriodMillis`定义的频率）调用。 |
| `void onAppWidgetOptionsChanged(Context context, AppWidgetManager manager, int appWidgetId, Bundle newOptions)` | `ACTION_APPWIDGET_OPTIONS_CHANGED` | 当此小部件调整大小时调用。 |
| `void onEnabled()` | `ACTION_APPWIDGET_ENABLED` | 当该类型的第一个小部件添加到主屏幕时调用。 |
| `void onDeleted()` | `ACTION_APPWIDGET_DELETED` | 当该类型的小部件从主屏幕删除时调用。 |
| `void onDisabled()` | `ACTION_APPWIDGET_DISABLED` | 当该类型的最后一个小部件从主屏幕删除时调用。 |
| `void onReceive(Context context, Intent intent)` | 在小部件配置之前以及配置活动完成后，自动在`onUpdate`方法之前调用。 | 重写此方法以将调用分派给此类的其他方法。 |

表 14-5 `AppWidgetProvider`类的选定方法

可能安装了该类的多个小部件。这就是为什么我们引用一个小部件 ID 数组而不是单个小部件 ID。例如，如果此小部件可根据某个位置进行自定义，那么我们可以有一个显示纽约州纽约市温度的小部件，以及另一个显示加利福尼亚州帕洛阿尔托温度的小部件。

在`onUpdate`方法内部，我们遍历所有类型为`TemperatureProvider`的小部件 ID，并使用`AppWidgetManager`参数更新它们。

请注意，我们可以选择仅通过使用`onUpdate`方法的`appWidgetIds`参数来更新需要更新的小部件。

表 14.6 展示了`AppWidgetManager`类的一些方法。

`RemoteViews`类（来自`android.widget`包）描述了一个可显示的视图层次结构。它可以从 XML 资源中展开。它还包含可以管理视图层次结构内容的方法。表 14.7 展示了`RemoteViews`类的一个构造函数。

| 方法 | 描述 |
| --- | --- |
| `int [ ] getAppWidgetIds(ComponentName provider)` | 返回此`AppWidgetProvider`提供者类型的小部件的小部件 ID 列表。 |
| `void updateAppWidget(int appWidgetId, RemoteViews views)` | 将`views`设置为 ID 为`appWidgetId`的小部件的`RemoteViews`。 |

表 14.6 `AppWidgetManager`类的选定方法

| 构造函数 | 描述 |
| --- | --- |
| `RemoteViews(String packageName, int layoutResourceId)` | 从名为`packageName`的包中由`layoutResourceId`标识的资源创建并返回一个`RemoteViews`。 |

表 14.7 `RemoteViews`类的选定方法

示例 14.4 展示了`TemperatureProvider`类。`onUpdate`方法位于第 9–17 行。在第 13–14 行，我们为`widget_layout.xml`文件中定义的布局实例化了一个`RemoteViews`对象。`appWidgetIds`参数存储了需要更新的小部件的小部件 ID。在第 15–16 行，我们使用`appWidgetManager`参数遍历所有这些 ID。

![](img/ch14exa04.jpg)

示例 14.4 `TemperatureProvider`类

![](img/9781284093650_CH14_FIGF01.jpg)

图 14.1 模拟器中的应用图标，包括小部件预览图标

![](img/9781284093650_CH14_FIGF02.jpg)

图 14.2 模拟器中的小部件列表

如果设备上安装了同一提供者类的多个小部件，它们很可能是在不同时间安装的。在示例 14.4 中，我们只更新那些需要更新的小部件。我们也可以更新所有小部件，无论哪些需要更新，以便它们保持同步。我们将在本章后面部分进行此操作。

我们可以在模拟器中测试小部件。如果我们点击应用图标，然后点击小部件预览图标（见图 14.1），再点击小部件（见图 14.2），就可以看到小部件的预览（见图 14.3）。

![](img/9781284093650_CH14_FIGF03.jpg)

图 14.3 模拟器中`TemperatureWidgetV0`小部件的预览

![](img/9781284093650_CH14_FIGF04.jpg)

图 14.4 长按后平板电脑显示的菜单

在平板电脑等设备上运行示例 14.4 后，我们需要在平板电脑上安装小部件。为此，我们执行以下操作：

- ▸ 长按屏幕以调出图 14.4 所示的菜单（也可以点击应用图标）。
- ▸ 选择“应用和小部件”，然后点击屏幕顶部的“小部件”选项卡。根据设备上已安装的小部件数量，我们可能需要滑动屏幕才能找到显示小部件的屏幕，如图 14.5 所示。
- ▸ 要安装它，我们按住它并将其移动到所需位置。松开后，小部件即开始运行。

图 14.6 显示了在主屏幕上运行的小部件。请注意，我们可以重复此操作，在主屏幕上安装同一提供者类的第二个小部件。

![](img/9781284093650_CH14_FIGF05.jpg)

图 14.5 平板电脑显示`TemperatureWidget`版本 0 小部件



![](img/9781284093650_CH14_FIGF06.jpg)

图 14.6 在平板电脑主屏幕上运行的`TemperatureWidgetV0`小部件

## 14.2 为小部件设置样式，温度小部件，版本 1

在版本 1 中，我们对小部件进行样式设计，使其看起来更像我们习惯的小部件，但尚未改进其功能。我们通过两种方式对其进行样式设计：

* 为其添加背景。
* 对显示文本的`TextView`进行样式设计。

为了定义背景，我们在 `drawable` 目录中创建一个 XML 文件，并定义一个矩形形状（第 3 行），如示例 14.5 所示。在第 5 行，我们指定矩形的每个角都带有半径为 `10` 的圆角。在第 7–9 行，我们指定矩形的描边：其宽度为 `2` 像素（第 8 行），颜色为海沫绿（第 9 行）。在第 11–14 行，我们指定一个渐变来填充矩形。其起始颜色为象牙白（第 12 行），结束颜色为蓝绿色（第 13 行），并具有两种不同的不透明度级别。这是一个线性渐变，以 `45` 度角从左到右渐变（第 14 行）。

![](img/ch14exa05.jpg)

示例 14.5 `widget_shape.xml`文件

Google 建议在小部件边界矩形的边缘与小部件框架之间留出外边距，并在小部件框架内部留出一些内边距，如图 14.7 所示。红色外部矩形是小部件的边界矩形（或边界框）。蓝色矩形是小部件的框架。小部件内容，特别是`Views`，位于黑色矩形内部。

![](img/9781284093650_CH14_FIGF07.jpg)

图 14.7 小部件的边距和内边距

示例 14.6 展示了更新后的`widget_layout.xml`文件。`widget_layout.xml`文件使用`LinearLayout`元素定义了小部件的布局。在第 7 行，我们将值`@drawable/widget_shape`赋给`android:background` XML 属性，以指定`LinearLayout`元素的背景由`widget_shape.xml`文件定义。我们在第 6 行将外边距设置为 `5` 像素。在第 14 行，我们将`TextView`元素内的文本水平和垂直居中。我们在第 15 行将内边距设置为 `5` 像素。由于我们需要在版本 2 及以后通过代码访问`TextView`，我们在第 10 行为其指定了一个 id。

图 14.8 展示了我们的小部件（版本 1）在平板电脑上与版本 0 的小部件一起运行的情况。

![](img/ch14exa06.jpg)

示例 14.6 `widget_layout.xml`文件

![](img/9781284093650_CH14_FIGF08.jpg)

图 14.8 平板电脑主屏幕中的版本 0 和版本 1 小部件

## 14.3 更新小部件中的数据——温度小部件，版本 2

在版本 2 中，我们使小部件动态化：我们从设备动态获取日期和时间，并将其显示在小部件内部。为了实现此功能，我们执行以下操作：

* 通过代码获取日期和时间，并构建一个包含它的`String`。
* 使用该`String`更新小部件内部的`TextView`。

`java.util`包中的`Date`类使我们能够动态获取日期和时间。`java.text`包中的`DateFormat`类使我们能够将该日期和时间格式化为`String`。

`RemoteViews`类包含一些方法，使我们能够像在应用程序中管理`Views`一样管理小部件内部的`Views`。表 14.8 展示了`RemoteViews`类的一些方法，以及它们在常规应用程序中的等效方法和类。`RemoteViews`的方法包含一个额外的参数，用于标识作为方法调用主体的`View`。该参数通常是`View`的 id。

例如，如果我们的小部件的布局 XML 文件是`widget_layout.xml`，并且它包含一个 id 为`display`的`TextView`，我们可以将该`TextView`的文本设置为`Hello Widget`，颜色设置为`green`，大小设置为`32`，如下所示：

```java
RemoteViews remoteViews = new RemoteViews( context.getPackageName( ),
                                           R.layout.widget_layout );
remoteViews.setTextViewText( R.id.display, "Hello Widget");
remoteViews.setTextColor( R.id.display, Color.parseColor("#00FF00"));
remoteViews.setTextViewTextSize( R.id.display, TypedValue.COMPLEX_UNIT_SP, 32.0f );
```

| `RemoteViews`的方法 | 等效方法 | 所属类 |
| --- | --- | --- |
| `void addView( int viewId, RemoteViews nestedView )` | `void addView( View child )` | `ViewGroup` |
| `void setTextViewText( int viewId, CharSequence text )` | `void setText( CharSequence text )` | `TextView` |
| `void setTextViewTextSize( int viewId, int units, float size )` | `void setTextSize( int units, float size )` | `TextView` |
| `void setTextColor( int viewId, int color )` | `void setTextColor( int color )` | `TextView` |

表 14.8 `RemoteViews`类的选定方法及其等效方法（及其所属类）

![](img/ch14exa07.jpg)

示例 14.7 `TemperatureProvider`类，应用程序版本 2

示例 14.7 展示了更新后的`TemperatureProvider`类。在第 9–10 行，我们导入了`DateFormat`和`Date`类。在第 17 行，我们获取了今天日期的引用`dateToday`。在第 18 行，我们将其格式化为更简单的`String` `today`，去掉了星期几和时区。在第 19 行，我们获取了一个`Resources`引用，以便将`city_and_temp`字符串资源转换为`String`（第 21 行）。`Resources`在第 6 行导入。在第 20–21 行，我们将`today`和我们的默认城市、州及温度拼接成`String` `displayString`。在第 25 行，我们将 id 为`display`的`TextView`中的文本设置为`displayString`。

图 14.9 展示了我们的小部件（版本 2）在平板电脑上与版本 0 和版本 1 的小部件一起运行的情况。

![](img/9781284093650_CH14_FIGF09.jpg)

图 14.9 平板电脑主屏幕中运行的版本 0、1 和 2 小部件

## 14.4 通过点击更新小部件中的数据——温度小部件，版本 3

小部件可以按指定频率自动更新。最低频率为 30 分钟。通常，用户不想等待 30 分钟，而是希望强制立即更新。在版本 3 中，我们实现了该功能。我们设置事件处理，以便通过点击小部件，小部件调用`onUpdate`方法并自行更新。

`RemoteViews`的`setOnClickPendingIntent`方法（如表 14.9 所示）使我们能够指定一个已创建为待定意图的意图，当用户点击由 id 标识的`RemoteViews`层次结构中的`View`时，该意图将被启动。

`PendingIntent`类封装了待定意图的概念。待定意图包含一个意图以及当该意图启动时要执行的操作。可以使用`PendingIntent`类的`getBroadcast`静态方法（如表 14.10 所示）结合其某些常量（如表 14.11 所示）来创建`PendingIntent`。

| 方法 | 描述 |
| --- | --- |
| `void setOnClickPendingIntent( int viewId, PendingIntent pendingIntent )` | 当用户点击 id 为`viewId`的`View`时，启动`pendingIntent`。 |

表 14.9 `RemoteViews`类的`setOnClickPendingIntent`方法

| 方法 | 描述 |
| --- | --- |
| `static PendingIntent getBroadcast( Context context, int requestCode, Intent intent, int flags )` | 在`Context` `context`中创建并返回一个`PendingIntent`；`requestCode`当前未使用（默认使用`0`）；`intent`是要广播的`Intent`；`flags`可以是`FLAG_...`常量之一。 |

表 14.10 `PendingIntent`类的`getBroadcast`方法

| 常量 | 描述和用途 |
| --- | --- |
| `FLAG_UPDATE_CURRENT` | 如果待定意图已存在，则重用，但其附加数据将被新意图的附加数据替换。 |
| `FLAG_ONE_SHOT` | 待定意图只能使用一次。 |
| `FLAG_CANCEL_CURRENT` | 如果存在待定意图，则在生成新的意图之前取消当前的意图。 |

表 14.11 `PendingIntent`类的部分常量

示例 14.8 展示了更新后的`TemperatureProvider`类。在第 29–33 行，我们创建了类型为`TemperatureProvider`的`Intent` `intent`（第 30 行），设置其动作以更新由`TemperatureProvider`类定义的小部件（第 31 行），并将小部件 ID 数组作为附加数据放入其中（第 32–33 行）。当该意图被启动时，会触发对`TemperatureProvider`的`onUpdate`方法的调用。

在第 35–36 行，我们使用`intent`创建了一个`PendingIntent`（`PendingIntent`类在第 3 行被导入），并指定重用当前意图且仅更新附加数据。附加数据包含小部件 ID 数组，而我们在设备上可能会删除现有小部件或安装更多`TemperatureProvider`类型的小部件。因此，小部件 ID 列表可能会变化。在第 37 行，我们指定点击 ID 为`display`的`View`将触发待定意图的启动。

![](img/ch14exa08.jpg)

示例 14.8 `TemperatureProvider`类，应用版本 3

图 14.10 展示了我们的小部件（版本 3）在平板电脑上运行的情况（左侧从上往下第二个），旁边是版本 0、1 和 2 的小部件。如果我们触摸版本 3 的小部件，数据和时间会更新，而版本 0、1 和 2 的数据是静态的。

![](img/9781284093650_CH14_FIGF10.jpg)

图 14.10 在平板电脑主屏幕上运行的版本 0、1、2 和 3 的小部件

## 14.5 从远程源检索温度数据，温度小部件，版本 4

在版本 4 中，我们显示从远程源检索到的实时温度数据。为此，我们需要执行以下操作：

- 确定提供所需数据的远程源。
- 确定要传递哪些数据以及如何将其传递给远程源。
- 理解远程源返回的数据及其格式。
- 从远程源检索数据：
  - 连接到远程源。
  - 将远程源的数据读取到适当的数据结构中。
- 解析该数据结构，以便检索所需的数据。
- 在小部件（或应用）中显示所需数据。

天气数据由气象站收集。在美国，大约有 2000 个气象站，每个气象站都有一个 ID 和与之关联的地理数据，例如地址、纬度、经度等。美国国家气象局（NWS）提供了大量免费的天气数据。为了获取特定位置的天气数据，我们首先从 NWS 检索该位置附近的气象站列表，计算从该位置到每个气象站的距离，选择最近的气象站，然后从该气象站读取数据。

除了 NWS，还有许多可用的天气数据源：有些是免费的，有些不是；有些需要密钥才能访问，有些则不需要。它们可能接受一种或多种输入类型，例如邮政编码、城市或经纬度坐标，并使用不同的数据格式，例如 XML 或 JavaScript 对象表示法（JSON），这是一种轻量级的数据格式化方式。JSON 通常用于格式化在互联网上服务器和客户端之间传输的数据，因为它不像 XML 那样繁琐，并且易于解析。

JSON 字符串可以包含两种数据结构：

- 表示哈希表的对象。
- 数组。

对象用花括号（{}）括起来，由逗号（,）分隔的名称/值对列表组成。冒号（:）分隔名称和值。值可以是双引号括起来的字符串、数字、true、false、null、对象或数组（即这两种数据结构可以嵌套）。数组是用方括号（[]）括起来的逗号分隔的值列表。

以下是一些有效的 JSON 字符串示例：

```json
{ "name": "mike", "age": 22 }
{ "states": { "MD": "Maryland", "CA": "California", "TX": "Texas" } }
[ "Chicago", "New York", "Palo Alto" ]
{ "countries": [ "USA", "Mexico", "China" ] }
```

在本应用中，我们使用 openweathermap.org 作为天气数据源。获取密钥非常容易，并且对于有限使用是免费的。该 URL 接受简单的输入，例如城市、国家字符串，其输出是一个 JSON 字符串。查询该站点的一种可能的 URL 格式是：

`http://api.openweathermap.org/data/2.5/weather?q=city,country&appid=your_key`

密钥是一个由十六进制数字组成的长字符串，例如：

`8f4fc1b7ccx025gga22ac2db344a3hj8z`

该 URL 也接受美国州名代替国家。问号字符（`?`）后面的字符串（本例中为 `q=city,country&appid=key`）称为查询字符串。

例如，我们可以使用：

```text
http://api.openweathermap.org/data/2.5/weather?q=London,UK&appid=YOUR_KEY
http://api.openweathermap.org/data/2.5/weather?q=New York,NY&appid=YOUR_KEY
http://api.openweathermap.org/data/2.5/weather?q=Baltimore,MD&appid=YOUR_KEY
```

如果我们打开浏览器并将这三个示例中的第一个（使用实际密钥）粘贴到 URL 字段中，浏览器将显示图 14.11 中所示的 JSON 字符串。

![](img/9781284093650_CH14_FIGF11.jpg)

图 14.11 来自 openweathermap.org 的伦敦（英国）的 JSON 字符串

| 开尔文 | 摄氏度 | 华氏度 |
| --- | --- | --- |
| K | C = K – 273.15 | F = ( C * 9/5) + 32 |
| 273.15 | 0 | 32 |
| 298.15 | 25 | 77 |

表 14.12 开尔文、摄氏度和华氏度之间的温度转换

返回的信息比我们这个小部件实际需要的要多。我们保持小部件简单，只显示当前温度。图 14.11 显示温度为 `283.09`，即字段 `temp` 的值。温度以开尔文度为单位。表 14.12 显示了各种温标之间的转换公式。

当我们构建一个模型来解析这样的 JSON 字符串时，我们注意到我们的模型依赖于接收到的数据的格式。虽然数据源不太可能频繁更改其数据格式，但最好订阅数据源的通知，以便能够尽快编辑我们的代码以适应数据及其格式的任何变化。`org.json` 包中的`JSONObject`类包含解析 JSON 字符串的方法。表 14.13 展示了其中一些方法。

在图 14.11 中，映射到`coord`的值是一个`JSONObject`。映射到`weather`的值是一个`JSONArray`。映射到`name`的值是一个字符串`London`。表 14.13 中的构造函数和方法会抛出`JSONException`。这是一个受检异常，因此在调用这些方法时必须使用`try`和`catch`块。假设我们已经使用图 14.11 中所示的 JSON 字符串创建了一个名为`jsonObject`的`JSONObject`，我们可以按如下方式检索这些值：

```java
// `jsonObject` 是从图 14.11 中的字符串创建的 `JSONObject`
try {
  JSONObject coordJSONObject = jsonObject.getJSONObject( "coord" );
  JSONArray weatherJSONArray = jsonObject.getJSONArray( "weather" );
  String city = jsonObject.getString( "name" );
} catch( JSONException jsonE ) {
  // 在此处处理异常
}
```

| 构造函数和方法 | 描述 |
| --- | --- |



为`json`创建一个`JSONObject`对象。

| 方法 | 描述 |
|---|---|
| `JSONObject getJSONObject(String name)` | 如果存在由`name`映射的`JSONObject`，则返回该`JSONObject`。 |
| `JSONArray getJSONArray(String name)` | 如果存在且为`JSONArray`，则返回按名称映射的`JSONArray`。 |
| `int getInt(String name)` | 如果存在且可以转换为`int`，则返回按名称映射的`int`值。 |
| `double getDouble(String name)` | 如果存在且可以转换为`double`，则返回按名称映射的`double`值。 |
| `String getString(String name)` | 如果存在，则返回按名称映射的`String`值。 |

## 表 14-13 `JSONObject` 类的部分方法

为了从图 14.11 的 JSON 字符串中检索当前温度，我们可以使用以下代码序列：

```java
// jsonObject 是从图 14.11 的字符串创建的 JSONObject
try {
  JSONObject mainJSONObject = jsonObject.getJSONObject("main");
  double temperature = mainJSONObject.getDouble("temp");
  // 在此处处理温度
} catch(JSONException jsonE) {
  // 在此处处理异常
}
```

示例 14.9 展示了`TemperatureParser`类，它是我们此应用模型的一部分。其主要功能是从 JSON 字符串中提取温度数据。构造函数（第 13–18 行）实例化了唯一的实例变量`jsonObject`，调用`JSONObject`构造函数并传入其`String`参数。`getTemperatureK`方法（第 20–27 行）返回与键`main`关联的 JSON 对象中键`temp`对应的值。请注意，我们在第 24 行捕获了一个通用的`Exception`而不是`JSONException`，因为`jsonObject`可能为`null`。当实例化`TemperatureParsing`对象时，如果传递给构造函数的参数无法转换为`JSONObject`，则`jsonObject`为`null`。对`null`引用调用`getJSONObject`方法会导致`NullPointerException`。通过捕获通用的`Exception`，我们可以捕获`NullPointerException`或`JSONException`。如果此时发生异常，我们在第 25 行使用默认值 25 摄氏度。`getTemperatureC`（第 29–31 行）和`getTemperatureF`（第 33–35 行）方法分别返回四舍五入为整数的摄氏度和华氏度温度。

![](img/ch14exa09.jpg)

### 示例 14.9 `TemperatureParser` 类，应用版本 4

除了`TemperatureParser`类，我们在模型中还包含一个用于从远程位置读取数据的类`RemoteDataReader`。该类是一个工具类，用于从由两个`String`定义的远程位置读取数据：一个基础 URL 和一个查询字符串。

为了从远程位置读取数据，我们执行以下操作：

*   ▸ 连接到远程位置。
*   ▸ 从该远程位置获取输入流。
*   ▸ 将该输入流读取到`String`中。

| 类 | 构造函数或方法 | 描述 |
|---|---|---|
| `URL` | `URL(String url)` | 为 url 创建一个`URL`。 |
| `URL` | `URLConnection openConnection()` | 创建并返回一个与此`URL`关联的`URLConnection`。 |
| `URLConnection` | `InputStream getInputStream()` | 返回一个从此`URLConnection`读取数据的`InputStream`。 |
| `URLConnection` | `void setDoInput(boolean doInputFlag)` | 如果我们想要读取，则使用参数`true`调用此方法；如果不想要读取，则使用`false`（默认值为`true`）。 |
| `URLConnection` | `void setDoOutput(boolean doOutputFlag)` | 如果我们想要写入，则使用参数`true`调用此方法；如果不想要写入，则使用`false`（默认值为`false`）。 |
| `HttpURLConnection`（继承自`URLConnection`） | `void setRequestMethod(String method)` | 将此请求的方法设置为 method——通常为`GET`或`POST`。默认值为`GET`。 |
| `HttpURLConnection`（继承自`URLConnection`） | `void disconnect()` | 断开与此`HttpURLConnection`的 URL 所在服务器的连接。 |
| `InputStream` | `void close()` | 关闭此`InputStream`并释放与其关联的内存资源。 |
| `InputStreamReader`（继承自`Reader`） | `InputStreamReader(InputStream is)` | 构造一个用于从输入流 is 读取数据的`InputStreamReader`。 |
| `BufferedReader` | `BufferedReader(Reader r)` | 构造一个`BufferedReader`，并使用缓冲以实现更高效的读取。 |
| `BufferedReader` | `String readLine()` | 读取并返回一行文本。 |
| `BufferedReader` | `void close()` | 关闭输入流并释放与其关联的内存资源。 |

## 表 14-14 用于从远程位置读取数据的部分类和方法

表 14.14 展示了我们执行这些步骤所使用的各种类和方法。`HttpURLConnection`是`URLConnection`的子类，增加了对 HTTP 协议的支持。`InputStreamReader`是`Reader`的子类，因此`InputStreamReader`引用可以用作`BufferedReader`构造函数的参数。

示例 14.10 展示了`RemoteDataReader`类。第 12 行声明的实例变量`urlString`表示一个完整的 URL。构造函数（第 14–25 行）构造`urlString`，将其四个`String`参数拼接起来：第二个参数是一个查询字符串，可能包含被视为不安全且需要编码的字符（例如空格或逗号`,`）。第三个和第四个参数可能为`null`，如果从该 URL 读取数据不需要密钥的话。我们在第 18 行将第二个参数编码为 URL 标准，然后将其拼接到`baseUrl`。如果第三个和第四个参数不为`null`（第 19 行），我们添加`&`字符，对其进行编码，并将它们拼接起来以形成完整的 URL。我们期望第二个`String`参数表示小部件版本 5 中的用户输入，因此我们希望确保特殊字符（特别是我们几乎肯定能从用户输入中得到的空格字符）被编码。

![](img/ch14exa10.jpg) ![](img/ch14exa10a.jpg)

### 示例 14.10 `RemoteDataReader` 类，应用版本 4

`getData`方法（第 27–53 行）从`urlString`表示的 URL 位置读取数据并返回。我们在第 29–32 行打开一个连接，并在第 34–37 行创建一个`BufferedReader`对象，用于读取该 URL 位置的数据。我们在第 40 行初始化`dataRead`（一个累积读取数据的`String`），并在第 41 行进行预读。我们在第 42–45 行使用`while`循环将数据读入`dataRead`，并在第 49 行返回。我们在第 50 行捕获整个过程中可能发生的任何异常，如果发生异常，则在第 51 行返回空`String`。

我们已经完成了此版本的模型。现在需要编辑小部件的控制器，即`TemperatureProvider`类。对于此版本的小部件，我们连接到互联网并从远程服务器检索一些数据。因此，我们在`AndroidManifest.xml`文件的`manifest`元素内包含两个`uses-permission`元素，如下所示：

```xml
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
```

由于我们要访问互联网，因此需要在单独的线程上执行此操作。我们创建`TemperatureTask`类，它是`AsyncTask`类的子类，以便从远程服务器读取温度。附录 D 详细解释了`AsyncTask`。`AsyncTask`类使用了三个泛型类型，我们在扩展它时必须指定这些类型。子类的类头如下：

```java
AccessModifier ClassName extends AsyncTask<Params, Progress, Result>
```

| 方法 | 描述 |
|---|---|
| `AsyncTask execute(Params... params)` | params 表示类型为`Params`（一个泛型类型）的值数组。 |
| `Result doInBackground(Params... params)` | params 是调用`execute`时传递给它的参数。 |
| `void onPostExecute(Result result)` | 在`doInBackground`完成后自动调用；result 是`doInBackground`返回的值。 |

## 表 14-15 `AsyncTask` 类的部分方法

其中`Params`、`Progress`和`Result`是实际类名的占位符，含义如下：

*   ▸ `Params`是当我们调用`AsyncTask`的`execute`方法时，传递给该方法的数组的数据类型。
*   ▸ `Progress`是任务在后台执行时，用于进度单位的数据类型。如果我们选择报告进度，该数据类型通常是`Integer`或`Long`。
*   ▸ `Result`是任务执行完成后返回的值的数据类型。

我们期望数据检索速度很快，因此不打算向用户提供任何进度反馈。任务的输入是一个 URL 字符串，输出是从远程服务器检索到的`String`。因此，`TemperatureTask`的类头如下：

```java
public class TemperatureTask extends AsyncTask<String, Void, String>
```

当我们通过`TemperatureTask`引用调用`execute`方法后，`doInBackground`方法会执行，其参数与传递给`execute`的参数相同。它的返回值成为`onPostExecute`的参数，`onPostExecute`会在`doInBackground`完成后自动调用。表 14.15 展示了这三个方法。`execute`和`doInBackground`的方法头表明它们都接受可变数量的参数。

我们期望实例化一个`TemperatureTask`对象，并在`TemperatureProvider`类的`onCreate`方法中调用其`execute`方法。`doInBackground`方法执行后，其返回值成为`postExecute`方法的参数。因此，我们需要在`postExecute`方法内部更新小部件。然而，为了更新小部件，我们需要使用`onCreate`方法的参数。为了在`onPostExecute`内部访问这些参数，我们将它们传递给`TemperatureTask`的构造函数，并赋值给`TemperatureTask`类的实例变量。然后，从`postExecute`方法中，我们可以调用`TemperatureProvider`类的一个方法，并将这些引用传递给该方法，以便它能够更新小部件。请注意，为了调用`TemperatureProvider`类的方法，我们需要一个`TemperatureProvider`对象的引用，我们也可以将其传递给`TemperatureTask`的构造函数，并赋值给一个实例变量。

示例 14.11 展示了`TemperatureTask`类。我们在第 9–11 行声明了三个实例变量，以匹配`TemperatureProvider`的`onCreate`方法的三个参数。我们还在第 8 行声明了一个`TemperatureProvider`实例变量，以便用它调用`TemperatureProvider`类的方法。第 13–21 行的构造函数将四个参数引用赋值给这四个实例变量。我们将从`TemperatureProvider`类的`onCreate`方法中调用它，第一个参数使用`this`，另外三个参数使用`onCreate`方法的三个参数。

![](img/ch14exa11.jpg)

示例 14.11 `TemperatureTask` 类，应用版本 4

第 23–30 行编写了`doInBackground`方法，该方法在`execute`方法被调用后自动调用，并接收与传递给`execute`相同的参数。它在第 32–33 行实例化一个`RemoteDataReader`对象，并将该 URL 位置的数据读取到名为`json`的`String`中（第 34 行），然后返回该字符串。

第 38–42 行的`postExecute`方法在第 39 行使用其`String`参数（由`doInBackground`方法返回的`String`）实例化一个`TemperatureParser`对象。它检索华氏温度值，并在第 40–41 行调用`TemperatureProvider`类的`updateWidget`方法，传递温度值以及三个实例变量（这些变量是对`onCreate`方法三个参数的引用）。

示例 14.12 展示了`TemperatureProvider`类。我们在第 14–16 行包含了常量`DEGREE`和`STARTING_URL`。我们没有为城市值使用资源，而是在第 19 行声明了一个名为`city`的实例变量。在版本 5 中，当允许用户修改它时，我们将需要它。我们在第 17 行和第 20 行声明了一个键名常量和键值实例变量。请注意，出于隐私和安全原因，我们将键值替换为`YOUR KEY HERE`。

![](img/ch14exa12.jpg) ![](img/ch14exa12a.jpg)

示例 14.12 `TemperatureProvider` 类，应用版本 4

`onUpdate`方法（第 22–30 行）在第 27–28 行实例化一个`TemperatureTask`对象，并在第 29 行调用其`execute`方法。`execute`的四个参数会自动传递给`TemperatureTask`类的`doInBackground`方法。

`updateWidget`方法位于第 32–56 行。它由`TemperatureTask`类的`postExecute`调用，第一个参数是检索到的温度，另外三个参数是`onUpdate`的参数。它在第 34–37 行构建要显示的`String`，包括温度。其余代码与版本 3 的`onUpdate`方法中的代码相同。

| 模型 | `RemoteDataReader.java`、`TemperatureParser.java` |
| 视图 | `widget_layout.xml` |
| 控制器 | `TemperatureProvider.java`、`TemperatureTask.java` |

表 14.16 模型-视图-控制器类与文件，版本 4

![](img/9781284093650_CH14_FIGF12.jpg)

图 14.12 版本 0、1、2、3 和 4 的小部件在平板电脑主屏幕中运行

表 14.16 展示了我们小部件版本 4 的各个组件：模型由`RemoteDataReader`和`TemperatureParser`类组成，这两个类在其他项目中也可重用。`widget_layout.xml`文件是视图。`TemperatureProvider`和`TemperatureTask`类构成控制器。

图 14.12 展示了我们的小部件版本 4 在平板电脑中运行（左侧从上往下第三个），旁边是版本 0、1、2 和 3 的小部件。请注意，温度显示的是实时数据（77°F），而不是像之前版本那样硬编码的值。

## 14.6 使用 Activity 自定义小部件，温度小部件，版本 5



在版本 4 中，位置被硬编码为纽约州纽约市。在版本 5 中，我们允许用户指定要显示当前温度的位置。当用户安装小部件时，他可以设置城市和州，或者城市和国家。通过这种方式，我们允许用户配置小部件。我们可以通过向项目添加一个`activity`来实现这一点。该`activity`首先运行并收集用户输入。我们使用用户输入（在本例中是城市和州，或城市和国家）来设置小部件提供程序的适当参数。在这种情况下，我们在`TemperatureProvider`类中设置`city`变量的值。

为了配置小部件，我们按如下方式修改项目：

- ▸ 在`AndroidManifest.xml`文件中添加一个`activity`元素。
- ▸ 为收集用户输入的`activity`创建一个布局 XML 文件。
- ▸ 在`AppWidgetProviderInfo` XML 文件中添加一个`android:configure`属性。
- ▸ 为`activity`创建一个类。
- ▸ 提供一种机制，将数据从`activity`传递到`TemperatureProvider`类。
- ▸ 根据需要更新`TemperatureProvider`类。

示例 14.13 展示了更新后的`AndroidManifest.xml`文件。在第 16–21 行，我们在`application`元素内部、`receiver`元素（用于小部件）之前添加了一个`activity`元素。在第 16 行，我们将`.TemperatureWidgetConfigure`指定为`activity`元素的`android:name`属性的值。这意味着我们继承`Activity`类的类名为`TemperatureWidgetConfigure`。前面的点（`.`）表示它位于当前包中。在第 18–19 行，我们通过将`AppWidgetManager`类的`ACTION_APPWIDGET_CONFIGURE`常量（参见表 14.17）的值赋给`activity`元素的`intent-filter`元素的`action`元素的`android:name`属性，来指定该活动的意图动作为配置小部件。小部件宿主（此处为主屏幕）会使用`ACTION_APPWIDGET_CONFIGURE`动作启动该活动，因此我们需要在清单文件中进行指定。

![](img/ch14exa13.jpg) ![](img/ch14exa13a.jpg)

**示例 14.13** `AndroidManifest.xml`文件，应用版本 5

| 常量 | 描述 |
| --- | --- |
| `ACTION_APPWIDGET_CONFIGURE` | 发送以启动在`AppWidgetProviderInfo`元数据中指定的活动的动作。 |
| `EXTRA_APPWIDGET_ID` | 使用此常量从意图的附加数据中检索小部件 ID。 |
| `INVALID_APPWIDGET_ID` | 值为 0，`AppWidgetManager`永远不会将其作为有效的小部件 ID 返回。 |

**表 14.17** `AppWidgetManager`类的选定常量

我们在布局目录中创建的`widget_config.xml`文件定义了配置小部件的活动的布局。用户界面包括一个用于输入数据的文本字段和一个用于处理输入数据的按钮。示例 14.14 展示了`widget_config.xml`文件。在第 6–10 行，我们编写了一个`TextView`元素，告知用户要做什么。`EditText`元素在第 11–15 行定义，并在第 12 行赋予 ID `city_input`，以便我们可以通过代码使用`findViewById`方法检索它。按钮在第 16–21 行定义。在第 20 行，我们指定`configure`作为用户点击按钮时执行的方法。

![](img/ch14exa14.jpg)

**示例 14.14** `widget_config.xml`文件，应用版本 5

必须在`AppWidgetProviderInfo` XML 文件中使用`android:configure`属性声明该活动。因此，我们更新了`widget_info.xml`文件，如示例 14.15 所示。在第 8–9 行，我们将`com.jblearning.temperaturewidgetv5`包中的`TemperatureWidgetConfigure`类指定为`appwidget-provider`元素的`android:configure`属性的值。

![](img/ch14exa15.jpg)

**示例 14.15** `widget_info.xml`文件，应用版本 5

接下来，我们创建`TemperatureWidgetConfigure`，即配置小部件的活动类。为了在活动中配置小部件，我们需要执行以下操作：

- ▸ 根据需要获取用户输入。
- ▸ 获取小部件 ID。
- ▸ 更新小部件。
- ▸ 创建返回意图。
- ▸ 将用户输入数据传递给`AppWidgetProvider`类。
- ▸ 退出活动。

当我们使用配置活动来自定义小部件时，活动有责任首先更新小部件。此外，配置活动应返回一个结果，该结果应包含启动该活动的意图所传递的小部件 ID。

示例 14.16 展示了`TemperatureWidgetConfigure`类。在第 15 行，我们将结果设置为`Activity`类的`RESULT_CANCELED`常量的值，如表 14.18 所示。当结果设置为`RESULT_CANCELED`时，如果用户未完成配置活动，则不会安装小部件。

![](img/ch14exa16.jpg) ![](img/ch14exa16a.jpg)

**示例 14.16** `TemperatureWidgetConfigure`类，应用版本 5

| 常量 | 描述 |
| --- | --- |
| `RESULT_CANCELED` | 0：表示活动已被取消。 |
| `RESULT_OK` | –1：表示活动成功结束。 |

**表 14.18** `Activity`类的常量

在第 20–22 行，我们检索用户输入。要将简单数据从一个活动传递到另一个活动，我们通常使用`Intent`类的`putExtra`和`getExtra`方法。然而，`AppWidgetProvider`类没有关联的意图，因此我们无法在此处使用该策略。此外，`AppWidgetProvider`类的默认构造函数会自动调用，并将实例变量重新初始化为其默认值。因此，将小部件数据存储在实例变量中并不实用，因为其值会随时间变化。在版本 4 中，我们使用了`TemperatureProvider`类的实例变量`city`（在示例 14.12 的第 19 行声明）来存储城市和州（或国家），尽管在该版本中它被硬编码为`New York, NY`。在版本 5 中，我们通过将其指定为`public`和`static`来使该变量成为全局变量，以便我们可以从`TemperatureWidgetConfigure`类访问和修改它。这是一种非常简单且方便的方式，可以将数据从活动类传递到小部件提供程序类。在第 24–25 行，我们访问`TemperatureProvider`类的`public static`变量`city`，并用用户输入的值更新它。

在第 27–34 行，我们从传入的意图中检索小部件 ID。我们在第 30 行将其默认值设置为`0`（表 14.17 中所示的`INVALID_APPWIDGET_ID`常量的值）。在第 31 行，我们测试传入意图的`Bundle`中是否存储了某些数据。如果有，我们在第 32–34 行尝试检索小部件 ID。如果`Bundle extras`包含一个键条目，其值等于`AppWidgetManager`类的`EXTRA_APPWIDGET_ID`常量（见表 14.17）的值，则该键映射到小部件 ID 值，并通过调用`getInt`返回该小部件 ID 值。如果没有，则调用`getInt`返回第二个参数，即`INVALID_APPWIDGET_ID`的值（即`0`）。

我们在第 36 行测试小部件 ID 值是否有效。如果有效，我们在第 37–43 行更新小部件，在第 45–46 行创建返回意图，在第 48–49 行将小部件 ID 放入其中，并在第 50 行将结果设置为`RESULT_OK`的值。之后，或者如果小部件 ID 值无效，我们在第 53–54 行终止活动。

示例 14.17 展示了`TemperatureProvider`类。在第 19 行，我们将`city`变量的访问修饰符从`private`更改为`public`和`static`，以便我们可以在`TemperatureWidgetConfigure`类中修改其值（参见示例 14.16 的第 25 行）。

![](img/ch14exa17.jpg) ![](img/ch14exa17a.jpg) ![](img/ch14exa17b.jpg)

**示例 14.17** `TemperatureProvider`类，应用版本 5

| 事件与方法调用序列 | 小部件 ID | 方法调用 |
| --- | --- | --- |
| 安装小部件 | | |
| `TemperatureProvider:onReceive` | 无效 | 自动 |
| `TemperatureProvider:onUpdate` | | 自动 |
| `TemperatureWidgetConfigure:onCreate` | | 自动 |
| 输入城市和州，点击配置小部件 | | |
| `TemperatureWidgetConfigure:configure` | 有效 | 事件处理 |
| `TemperatureProvider:onReceive` | 有效 | 自动 |
| `TemperatureProvider:onUpdate` | | 由`onReceive`调用 |

**表 14.19** 安装小部件时的方法调用序列，版本 5

`AppWidgetProvider`类的`onReceive`方法会在`TemperatureWidgetConfigure`活动结束后自动调用。该方法编码在第 58–70 行。在第 62–64 行，我们使用其`Intent`参数来获取应用小部件 ID。如果该 ID 有效（第 66 行），我们通过在第 68 行调用`onUpdate`方法来更新小部件。TABLE 14.19 展示了方法调用的顺序及其性质。

TABLE 14.20 展示了我们小部件版本 5 的模型、视图和控制器状态。与版本 4 相比，模型未发生变化。我们在视图中添加了`widget_config.xml`文件，用于定义配置小部件的活动布局，并在控制器中添加了`TemperatureWidgetConfigure`类，修改了`TemperatureProvider`类。

FIGURE 14.13 展示了用户在小部件版本 5 配置过程中设置城市和州的操作。FIGURE 14.14 展示了我们的小部件版本 5 在平板电脑上运行，旁边是版本 0、1、2、3 和 4 的小部件。版本 5 小部件（加利福尼亚州旧金山）的城市和州与其他版本不同，并且像版本 4 一样显示实时数据。

| 模型 | `RemoteDataReader.java`、`TemperatureParser.java` |
| --- | --- |
| 视图 | `widget_layout.xml`、`widget_config.xml` |
| 控制器 | `TemperatureProvider.java`、`TemperatureTask.java`、`TemperatureWidgetConfigure.java` |

**表 14.20** 模型-视图-控制器类与文件，版本 5

![](img/9781284093650_CH14_FIGF13.jpg)

**图 14.13** 安装小部件时的配置界面，版本 5

![](img/9781284093650_CH14_FIGF14.jpg)

**图 14.14** 版本 0、1、2、3、4 和 5 的小部件在平板电脑主屏幕上运行

## 14.7 在锁屏上托管小部件，温度小部件，版本 6

自 Android 4.2 起，也可以将小部件托管在锁屏（也称为 Keyguard）上。我们通过在小部件信息文件的`appwidget-provider`元素中为`android:widgetCategory`属性赋值`keyguard`来启用锁屏上的小部件托管，如下所示：

| 常量 | 描述 |
| --- | --- |
| `WIDGET_CATEGORY_HOME_SCREEN` | 值为 1。小部件可显示在主屏幕上。 |
| `WIDGET_CATEGORY_KEYGUARD` | 值为 2。小部件可显示在锁屏上。 |

**表 14.21** `AppWidgetProviderInfo`类的选定常量

```xml
android:widgetCategory="keyguard"
```

我们根据是否允许锁屏、主屏幕或两者作为小部件的可能托管屏幕，为`android:widgetCategory`属性赋值`keyguard`、`home_screen`或`keyguard | home_screen`。如果未指定，小部件的默认托管屏幕为主屏幕。这些值对应于`AppWidgetProviderInfo`类中的`WIDGET_CATEGORY_KEYGUARD`和`WIDGET_CATEGORY_HOME_SCREEN`常量，如表 14.21 所示。

示例 14.18 展示了更新后的`widget_info.xml`文件。在第 8 行，我们指定小部件可以托管在主屏幕或锁屏上。

![](img/ch14exa18.jpg)

**示例 14.18** `widget_info.xml`文件，应用版本 6

可以设计一个小部件，使其在锁屏上的外观与主屏幕上的外观不同。为此，我们为小部件在锁屏上托管时创建一个不同的 XML 布局文件。我们还需要在`AppWidgetProviderInfo` XML 文件中指定该文件的名称。如果锁屏的 XML 布局文件名为`widget_layout_keyguard.xml`，则在`AppWidgetProviderInfo` XML 文件的`appwidget-provider`元素中添加以下属性/值对。

| 常量与方法 | 描述 |
| --- | --- |
| `OPTION_APPWIDGET_HOST_CATEGORY` | 一个字符串常量，用作检索小部件托管类别（存储为额外数据）的键。 |
| `Bundle getAppWidgetOptions(int widgetId)` | 返回存储小部件（ID 为`widgetId`）额外数据的`Bundle`。 |

**表 14.22** `AppWidgetManager`类的`OPTION_APPWIDGET_HOST_CATEGORY`常量和`getAppWidgetOptions`方法

| 方法 | 描述 |
| --- | --- |
| `int getInt(String key)` | 返回与`key`关联的整数值，如果没有则返回 0。 |

**表 14.23** `BaseBundle`类的`getInt`方法，由`Bundle`继承

```xml
android:initialKeyguardLayout="@layout/widget_layout_keyguard"
```

在`AppWidgetProvider`类内部，我们可以测试小部件托管屏幕是主屏幕还是锁屏。托管信息存储在与小部件关联的`Bundle`中。在`AppWidgetProvider`类的`onUpdate`方法中，我们有一个`AppWidgetManager`引用作为该方法的参数。我们可以通过调用`AppWidgetManager`类的`getAppWidgetOptions`方法（参见表 14.22）来检索该`Bundle`，并将小部件 ID 作为其唯一参数。有了`Bundle`引用，我们可以调用`getInt`方法（如表 14.23 所示），传入`AppWidgetManager`类的`OPTION_APPWIDGET_HOST_CATEGORY`常量（参见表 14.22），并将小部件托管类别作为`int`值检索出来。然后，我们可以将该整数值与`AppWidgetProviderInfo`类（参见表 14.21）的`WIDGET_CATEGORY_HOME_SCREEN`和`WIDGET_CATEGORY_KEYGUARD`常量（值分别为 1 和 2）进行比较，以测试小部件所在的托管屏幕。

我们可以使用以下序列来测试托管屏幕是主屏幕还是锁屏。

```java
Bundle bundle = appWidgetManager.getAppWidgetOptions(widgetId);
int host =
  bundle.getInt(AppWidgetManager.OPTION_APPWIDGET_HOST_CATEGORY, -1);
if (host == AppWidgetProviderInfo.WIDGET_CATEGORY_KEYGUARD) {
  // 锁屏托管代码
} else if (host == AppWidgetProviderInfo.WIDGET_CATEGORY_HOME_SCREEN) {
  // 主屏幕托管代码
}
```

设计一个在锁屏上外观和行为不同的小部件留作练习。

## 章节总结

- 应用小部件（也称为小部件）是嵌入在其他应用（称为应用小部件托管程序）中的小型应用。
- 主屏幕和锁屏是应用小部件托管程序的示例。
- 要创建小部件，我们可以扩展`AppWidgetProvider`类并重写其`onUpdate`方法。
- 小部件信息文件位于`res`目录的`xml`目录中，定义了一个`appwidget-provider`元素，用于指定小部件的特性，如大小和更新频率。
- 并非所有`View`和布局管理器类都可以在小部件内部使用。



小部件可以使用可绘制资源作为其背景。

小部件可以按一定频率自动更新其显示。最小频率为 30 分钟。

我们可以通过用户与小部件的交互（例如点击）来更新小部件。

可以动态更新小部件显示的数据。这些数据可以从本地或远程源获取。

小部件可以在安装时通过添加一个捕获用户输入的活动来让用户自定义。

我们不仅可以将小部件安装到主屏幕上，还可以将其安装到锁屏上。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. 我们重写 `AppWidgetProvider` 的哪个方法来更新小部件？
   - `update`
   - `onUpdate`
   - `widgetUpdate`
   - `broadcast`

2. 问题 1 中方法的第三个参数是：
   - `Context` 引用
   - `AppWidgetManager` 引用
   - 一个小部件 ID
   - 一个小部件 ID 数组

3. 我们使用哪个类来管理小部件内部的 `View` 层次结构？
   - `Views`
   - `View`
   - `RemoteViews`
   - `Remotes`

4. 我们在小部件信息 XML 文件中定义哪个元素？
   - `appwidget`
   - `appwidget-provider`
   - `provider`
   - `widget-info`

5. 小部件 ID 的数据类型是：
   - `char`
   - `String`
   - `int`
   - `AppWidgetInfo`

6. 小部件自动更新的最小频率是：
   - 1 秒
   - 30 秒
   - 60 秒
   - 30 分钟

7. 我们可以允许通过用户交互来更新小部件：
   - 不可以，这是不可能的
   - 可以，例如通过点击它
   - 可以，但只能每 60 秒一次
   - 可以，但只能每 30 分钟一次

8. 小部件显示的数据：
   - 不能更改
   - 可以更改，但只能使用设备内部存储的数据
   - 可以更改，通过从外部源检索数据
   - 只能每 30 分钟更改一次

9. 如何在安装时自定义小部件？
   - 这是不可能的
   - 我们可以在那时运行一个活动，捕获并使用用户输入来自定义小部件
   - 我们使用 `android.widget` 包中的 `CustomizeWidget` 类
   - 我们使用 `android.widget` 包中的 `SpecializeWidget` 类

10. 小部件的主屏幕有哪些例子？
    - 小部件没有所谓的主屏幕
    - 主屏幕，且只有主屏幕
    - 锁屏，且只有锁屏
    - 主屏幕和锁屏

### 填写代码

11. 编写代码，使小部件的更新频率为 1 小时。

```xml
<?xml version="1.0" encoding="utf-8"?>
<appwidget-provider
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:initialLayout="@layout/widget_layout"
    android:minHeight="40dp"
    android:minWidth="180dp"
    <!-- 你的代码写在这里 -->

</appwidget-provider>
```

12. 在 `AppWidgetProvider` 类的 `onUpdate` 方法中，更新该 `AppWidgetProvider` 类类型的所有小部件。

```java
public void onUpdate ( Context context,
       AppWidgetManager appWidgetManager, int[ ] appWidgetIds ) {
  super.onUpdate( context, appWidgetManager, appWidgetIds );
  RemoteViews views = new RemoteViews( context.getPackageName( ),
                                       R.layout.widget_layout );
  // 你的代码写在这里

}
```

13. 编写代码，将 ID 为 `my_view` 的 `TextView` 中的文本设置为 `HELLO WIDGET`。

```java
RemoteViews remoteViews = new RemoteViews( context.getPackageName( ),
                                           R.layout.widget_layout );
// 你的代码写在这里
```

14. 在 `MyProvider` 类的 `onUpdate` 方法中，编写代码，使得每次用户点击小部件内 ID 为 `my_view` 的 `View` 时更新小部件。

```java
RemoteViews remoteViews = new RemoteViews( context.getPackageName( ),
                                           R.layout.widget_layout );
// widgetId 是当前小部件的 ID
Intent intent = new Intent( context, MyProvider.class );
intent.setAction( AppWidgetManager.ACTION_APPWIDGET_UPDATE );
intent.putExtra( AppWidgetManager.EXTRA_APPWIDGET_IDS, appWidgetIds );
// 你的代码写在这里

appWidgetManager.updateAppWidget( widgetId, remoteViews );
```

15. 考虑以下名为 `json` 的 JSON 字符串。编写代码以检索国家（例如 Italy）的值。

```json
{"coord":{"lon":12.495800018311,"lat":41.903049468994},"sys":{"country":
"Italy","sunrise":1374033016,"sunset":1374086531 } };

// 你的代码写在这里
```

16. 编写代码，使小部件由一个名为 `MyActivity` 且位于 `com.xyz.q16` 包中的活动进行配置。

```xml
<?xml version="1.0" encoding="utf-8"?>
<appwidget-provider
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:initialLayout="@layout/widget_layout"
    android:minHeight="40dp"
    android:minWidth="180dp"
    <!-- 你的代码写在这里 -->

</appwidget-provider>
```

17. 在配置活动中，编写代码将 `current_widget_id`（一个小部件 ID）作为额外数据放入 `Intent` `resultIntent` 中。

```java
// 应用小部件 ID 是 widget_id
Intent resultIntent = new Intent( );
// 你的代码写在这里
```

18. 编写代码，使小部件可以安装在主屏幕或锁屏上。

```xml
<?xml version="1.0" encoding="utf-8"?>
<appwidget-provider
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:initialLayout="@layout/widget_layout"
    android:minHeight="40dp"
    android:minWidth="180dp"
    <!-- 你的代码写在这里 -->

</appwidget-provider>
```

### 编写一个小部件

19. 修改本章示例的第 4 版，使其显示与温度不同的内容，例如湿度水平。

20. 修改本章示例的第 4 版，使其显示两条数据（而不是一条），并且与温度不同，例如气压和湿度水平。

21. 修改本章示例的第 5 版，使其显示两个城市（而不是一个）的温度。

22. 修改本章示例的第 5 版，使其显示两个城市（而不是一个）的数据，并且这些数据应与温度不同，例如湿度水平。

23. 修改本章示例的第 5 版，使用户可以自定义温度的显示方式，而不是位置。用户可以在摄氏度和华氏度之间选择。

24. 修改本章示例的第 5 版，使用户可以自定义小部件的背景颜色，而不是位置。

25. 创建一个小部件，从你选择的远程源拉取数据。

26. 创建一个小部件，从你选择的远程源拉取数据，并且可由用户自定义。

27. 修改本章示例的第 5 版，使数据从 NWS 拉取。使用本章第 14.5 节开头描述的策略。

# 第十五章：应用内广告

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

构建应用时的一个重要问题是如何实现盈利。由于市面上有如此多的应用，大多数人会首先尝试免费应用（如果可能的话）。Android SDK 为开发者提供了在应用内包含广告的能力，并利用 Google 的广告资源在运行时上传广告。

## 15.1 视图、秒表应用，第 0 版

我们想要构建一个秒表应用，使用户能够启动时钟、停止、重置、重新启动等。在第 0 版中，我们只构建 GUI，在底部预留一个广告横幅的空间。图 15.1 显示了该应用的第 3 版在模拟器中运行的情况。屏幕分为三个部分：

- 顶部是时钟。
- 中间是一个开始/停止切换按钮和一个重置按钮。
- 底部是广告横幅。

![](img/9781284093650_CH15_FIGF01.jpg)

图 15.1 秒表应用，第 3 版

对于两个圆形按钮，我们使用了三个可绘制对象，如示例 15.1、15.2 和 15.3 所示。我们将它们放在 `drawable` 目录中。对于开始/停止按钮，我们将在 `start_button.xml` 和 `stop_button.xml` 之间切换按钮的背景。开始按钮有一个绿色圆形轮廓，停止按钮有一个红色圆形轮廓（示例 15.1 和 15.2 的第 6 行）。重置按钮有一个灰色圆形轮廓（示例 15.3 的第 6 行）。

![](img/ch15exa01.jpg)

示例 15.1 秒表应用版本 0 的 `start_button.xml` 文件

![](img/ch15exa02.jpg)

示例 15.2 秒表应用版本 0 的 `stop_button.xml` 文件

![](img/ch15exa03.jpg)

示例 15.3 秒表应用版本 0 的 `reset_button.xml` 文件

为了显示秒表，我们使用 `Chronometer`。`Chronometer` 类继承自 `TextView`，封装了运行时钟的功能。我们想要设置 `Chronometer` 的样式，因此在 `styles.xml` 文件的第 11–15 行编写了 `textViewStyle` 样式，如示例 15.4 所示。

![](img/ch15exa04.jpg)

示例 15.4 秒表应用版本 0 的 `styles.xml` 文件

示例 15.5 展示了 `activity_main.xml` 文件，组织了图形用户界面。一个垂直（第 10 行）的 `LinearLayout`（第 2 行）将屏幕分为三个部分：

- 一个 `Chronometer`（第 13–18 行）。
- 一个水平（第 21 行）的 `LinearLayout`（第 20–59 行），包含开始/停止和重置按钮。
- 另一个 `LinearLayout`（第 61–67 行），作为广告横幅的占位符（我们稍后会按照 Google 的建议将这个 `LinearLayout` 改为片段）。

![](img/ch15exa05.jpg) ![](img/ch15exa05a.jpg)

示例 15.5 秒表应用版本 0 的 `activity_main.xml` 文件

我们将屏幕的 4/9（权重 4 – 第 14 行）分配给 `Chronometer` 元素，4/9（权重 4 – 第 22 行）分配给按钮，1/9（权重 1 – 第 63 行）分配给底部的 `LinearLayout`。我们在第 17 行给 `Chronometer` 分配了一个 id，因为我们需要从 `MainActivity` 类中访问它。我们在第 18 行设置了它的样式。

屏幕中间的水平 `LinearLayout` 包含两个 `LinearLayout`（第 27–41 行和第 43–57 行），每个包含一个按钮（第 33–40 行和第 49–56 行）。每个按钮的直径为 150 像素（第 35–36 行和第 51–52 行），文本大小为 36。虽然硬编码尺寸值通常不是好做法，但这里为了保持示例简单而这样做。此外，这些尺寸相当小，预期能在任何设备上工作。在第 39 行和第 55 行，我们将每个按钮的背景设置为其对应的可绘制资源。点击开始/停止按钮将触发对 `startStop` 方法的调用（第 40 行），点击重置按钮将触发对 `reset` 方法的调用（第 56 行）。

在这个版本中，我们将底部的 `LinearLayout` 设置为浅灰色（第 66 行），以便可视化广告横幅将放置的位置。

我们向 `MainActivity` 类添加了空操作的 `startStop` 和 `reset` 方法（示例 15.6），这样当用户点击任一按钮时应用不会崩溃。

图 15.2 展示了环境中秒表版本 0 的预览。

![](img/ch15exa06.jpg)

示例 15.6 秒表应用版本 0 的 `MainActivity` 类

![](img/9781284093650_CH15_FIGF02.jpg)

图 15.2 秒表应用版本 0 的预览

## 15.2 控制器：运行秒表应用，版本 1

在版本 1 中，我们将编写 `startStop` 和 `reset` 方法，使应用具备功能。为此，我们使用 `Chronometer` 类的功能，它代表了此应用的模型：`Chronometer` 类的 `start`、`stop` 和 `setBase` 方法（如表 15.1 所示）使我们能够启动、停止和重置 `Chronometer`。

`setBase` 的参数 `base` 通常使用 `SystemClock` 类的 `elapsedRealtime` 方法设置。其 API 为：

```java
public static long elapsedRealtime( )
```

`elapsedRealtime` 方法返回自上次启动以来的毫秒数，包括休眠时间。

| 方法 | 描述 |
| --- | --- |
| `void start( )` | 开始计数（或重新开始计数）。 |
| `void stop( )` | 停止计数。 |
| `void setBase( long base )` | 设置计数的参考时间。 |

表 15.1 `Chronometer` 类的选定方法

示例 15.7 展示了更新后的 `MainActivity` 类。由于开始/停止按钮在两个状态之间切换，我们使用一个 `boolean` 实例变量 `started`（第 12 行）来跟踪该状态。由于我们需要在两个方法中访问 `Chronometer`，我们为其添加了一个实例变量 `chrono`（第 11 行）。在 `onCreate` 方法中，我们在第 18 行使用 `findViewbyId` 方法实例化它。

![](img/ch15exa07.jpg) ![](img/ch15exa07a.jpg)

示例 15.7 秒表应用版本 1 的 `MainActivity` 类

`startStop` 方法编写在第 21–34 行。如果 `Chronometer` 已经启动（第 23 行），那么开始/停止按钮处于“已启动”状态，我们执行以下操作：

- 停止 `Chronometer`：我们在第 24 行通过调用 `chrono` 的 `stop` 方法来实现。
- 将 `started` 设为 `false`（第 25 行），以指定按钮现在处于“已停止”状态。
- 将按钮的文本改为 START（第 26 行）。
- 将按钮的背景切换为 `start_button.xml` 中定义的可绘制资源（第 27 行）。

否则（第 28 行），`Chronometer` 尚未启动或已停止，按钮处于“启动”状态，我们执行以下操作：

- 启动 `Chronometer`：我们在第 29 行通过调用 `chrono` 的 `start` 方法来实现。
- 将 `started` 设为 `true`（第 30 行），以指定按钮现在处于“已启动”状态。



* ▸ 将按钮的文本改为 `STOP`（第 31 行）。
* ▸ 将按钮的背景切换为 `stop_button.xml` 中定义的可绘制资源（第 32 行）。

`reset` 方法（第 36–39 行）通过调用 `setBase` 方法，传入当前时间的毫秒数，将 `chrono` 重置为 `00:00`。因此，当我们在时间 `t` 调用 `reset` 时，`00:00` 被视为时间 `t`。

![](img/9781284093650_CH15_FIGF03.jpg)

图 15.3 秒表应用版本 1

图 15.3 展示了在模拟器中运行的秒表版本 1。时钟正在运行，开始/停止按钮有一个红色圆形轮廓，并显示 `STOP`。

## 15.3 改进秒表应用，版本 2

版本 1 有一个问题：如果我们停止时钟然后稍后重新启动，它不会从停止的地方重新开始。实际上，当我们停止 `Chronometer` 时，它仍在后台运行。在版本 2 中，我们修复了这个问题，使得当我们在时间 `t` 停止 `Chronometer` 时，它会在时间 `t` 重新开始。

为了实现这一点，当我们启动或重新启动 `Chronometer` 时，我们需要从 `elapsedRealtime` 方法返回的值中减去自停止 `Chronometer` 以来经过的时间。我们不在控制器 `MainActivity` 类中执行此操作，而是创建一个工具类 `ClockUtility`，如示例 15.8 所示。此应用的模型现在由 `Chronometer` 和 `ClockUtility` 类组成。此外，`ClockUtility` 类的功能可以在其他应用中重用。

`ClockUtility` 包含一个 `static` 方法 `milliseconds`：它将一个格式类似于 `Chronometer` 内显示的字符串转换为等效的毫秒数。`clock` 字符串（第 10 行）的格式预期为 `hh:mm:ss` 或 `mm:ss`，其中 `hh` 表示小时数（00 到 23），`mm` 表示分钟数（00 到 59），`ss` 表示秒数（00 到 59）。为了将 `clock` 字符串转换为毫秒数，我们使用 `Integer` 类的 `parseInt` 方法，该方法会抛出 `NumberFormatException`。虽然这不是强制性的，因为 `NumberFormatException` 是非检查异常，但我们更倾向于使用 `try` 和 `catch` 块（第 15–26 行）。

![](img/ch15exa08.jpg)

示例 15.8 秒表应用版本 2 的 `ClockUtility` 类

我们在第 12 行将 `clock` 转换为数组。如果该数组中有三个元素（第 16 行），则毫秒数等于 `hh * 60 * 60 * 1000 + mm * 60 * 1000 + ss * 1000`（第 17–19 行）。如果该数组中有两个元素（第 20 行），则毫秒数等于 `mm * 60 * 1000 + ss * 1000`（第 21–22 行）。如果 `clock` 格式不正确，该方法返回 `0`。

示例 15.9 展示了更新后的 `MainActivity` 类。在 `startStop` 方法中，如果我们重新启动 `Chronometer`（第 29–33 行），我们首先通过调用 `resetChrono` 方法将其重置为之前停止的位置（第 29 行）。在 `resetChrono` 中（第 42–46 行），我们在第 43–44 行将 `chrono` 的当前值转换为毫秒数。在第 45 行，我们将其基准（即起始值）重置为它停止时的值。表 15.2 展示了当用户点击 START，然后当 `chrono` 显示 `10:00` 时点击 STOP，再点击 START 时，`elapsedRealtime` 和 `milliseconds` 方法可能返回的值。

![](img/ch15exa09.jpg) ![](img/ch15exa09a.jpg)

示例 15.9 `MainActivity` 类，秒表应用，版本 2

| 操作 | `Chrono` | 时间 | `elapsedRealtime` 返回的值 | `milliseconds` 返回的值 |
| --- | --- | --- | --- | --- |
| 开始 | 00:00 | t1 | 695064 | 0 |
| 停止 | 00:10 | t2 | 705777 | 10000 |
| 开始 | 00:10 | t3 | 859134 | 10000 |

表 15.2 假设执行 START、STOP、START 序列时 `elapsedRealtime` 和 `milliseconds` 返回的值

现在，当我们运行应用时，我们可以停止 `Chronometer`，它将从停止的位置重新开始。例如，如果我们在停止时 `Chronometer` 显示 `00:15`，并且我们等待 10 秒后再点击开始/停止按钮，`Chronometer` 将从 `00:15` 重新开始，而不是 `00:25`。

## 15.4 放置广告，秒表应用，版本 3

在版本 3 中，我们在屏幕底部放置了一个广告。`com.google.android.gms.ads` 包提供了一组用于显示和管理广告的类。表 15.3 展示了其中一些类。

| 类 | 描述 |
| --- | --- |
| `AdView` | `View` 的子类，用于显示广告横幅。 |
| `AdSize` | 封装横幅广告的大小。 |
| `AdRequest` | 封装一组营销特征，如位置、生日、关键词等，以便广告可以针对与应用相关的人口统计信息。 |

表 15.3 `com.google.android.gms.ads` 包中的选定类

然而，`com.google.android.gms.ads` 包不是标准 Android SDK 的一部分，而是 Google Play 服务的一部分。因此，为了使用它，我们编辑 `build.gradle` 文件，如示例 15.10 所示。由于我们编辑了 `build.gradle` 文件，我们需要同步项目。

![](img/ch15exa10.jpg)

示例 15.10 编辑后的 `build.gradle` 文件

我们编辑 `activity_main.xml` 文件，并为放置广告的最后一个 `LinearLayout` 指定一个 ID，如示例 15.11 第 60 行所示。由于我们无法完全控制将要投放的广告的大小，我们希望屏幕宽度最大化。因此，我们删除示例 15.5 的第 7 行和第 8 行，这样整个 `LinearLayout` 就没有左右内边距了。

![](img/ch15exa11.jpg)

示例 15.11 `activity_main.xml` 文件的结尾

`AdSize` 类封装了横幅广告的大小。它提供了与各种行业标准尺寸匹配的常量，以及使宽度和高度相对于设备宽度和高度的常量。表 15.4 展示了其中一些常量。我们可以使用 `FULL_WIDTH` 和 `AUTO_HEIGHT` 常量通过 `AdSize` 构造函数创建 `AdSize` 对象，而使用其他常量（如 `SMART_BANNER`）来指定预制的 `AdSize` 对象。

`AdView` 类包含创建和管理横幅广告的方法。它的直接超类是 `ViewGroup`，而 `ViewGroup` 本身是 `View` 的子类。因此，`AdView` 继承自 `View`。表 15.5 展示了 `AdView` 类的一些方法。

在将广告加载到 `AdView` 之前，我们必须设置 `AdView` 的大小和广告单元 ID。否则，当我们尝试加载广告时，会抛出（未检查的）`IllegalStateException`。为了从 Google 获取广告单元 ID，我们必须是注册的 Android 开发者。开发者通过广告单元 ID 来产生广告收入等。广告单元 ID 是一个 `String`，我们可以从 AdMob（Google 用于管理广告的平台）获取，网址如下：

```text
https://support.google.com/admob/v2/answer/3052638
```

AdMob 广告单元 ID 的格式如下：

```text
ca-app-pub-XXXXXXXXXXXXXXXX/NNNNNNNNNN.
```

对于未注册但想测试包含 `AdView` 的应用的开发者，Google 提供了一个测试广告单元 ID。我们将其包含在 `strings.xml` 文件中，如示例 15.12 所示（第 3–4 行）。实际上，我们在版本 3 中没有使用该 `String`，但在版本 4 和版本 5 中会使用。

![](img/ch15exa12.jpg)

示例 15.12 `strings.xml` 文件，秒表应用，版本 3

以下代码序列展示了创建 `AdView`、设置其大小和广告单元 ID 的过程，假设我们在 `Activity` 类中：

```java
// 创建横幅广告；假设这是一个 Activity 引用
AdView adView = new AdView(this);
// 设置广告大小
adView.setAdSize(AdSize.SMART_BANNER);
// 设置广告单元 ID；使用 Google 的默认字符串
String adUnitId = "ca-app-pub-3940256099942544/6300978111";
adView.setAdUnitId(adUnitId);
```

| 方法 | 描述 |
| --- | --- |
| `public AdRequest.Builder()` | 默认构造函数。 |
| `public AdRequest.Builder addKeyword(String keyword)` | 添加用于定向的关键词，可多次调用以添加多个关键词。 |
| `public AdRequest.Builder setGender(int gender)` | 设置用户的性别以进行定向。 |
| `public AdRequest.Builder setBirthday(Date birthday)` | 设置用户的生日以进行定向。 |
| `public AdRequest.Builder setLocation(Location location)` | 设置用户的位置以进行定向。 |
| `public AdRequest.Builder addTestDevice(String deviceId)` | 设置设备以接收测试广告而非真实广告。使用 `AdRequest` 类中的常量 `DEVICE_ID_EMULATOR` 来使用模拟器。 |
| `public AdRequest build()` | 构造并返回一个包含此 `AdRequest.Builder` 指定属性的 `AdRequest`。 |

表 15.6 `AdRequest.Builder` 类的选定方法

一旦我们创建了 `AdView`，设置了其尺寸和广告单元 ID，就需要创建一个广告请求并将其加载到 `AdView` 中。`AdRequest` 类封装了广告请求的概念。它包含一个 `static` 内部类 `Builder`，我们可以用它来设置 `AdRequest` 的特性。表 15.6 展示了 `AdRequest.Builder` 类的一些方法。`addKeyword` 允许我们添加与应用程序相关的关键词（每次方法调用添加一个），以便广告能更精准地定位到典型应用用户。`setGender` 方法允许我们将广告定位到女性、男性或两者。`AdRequest` 类提供了三个 `int` 常量：`GENDER_FEMALE`、`GENDER_MALE` 和 `GENDER_UNKNOWN`，我们可以将它们用作该方法的参数。我们可以使用 `setLocation` 方法基于位置来定位广告。应用程序可以访问 GPS，动态获取用户的位置，并将其包含在广告请求中，以便 Google 服务能够利用该位置更好地选择和定位广告。所有这些方法都返回调用它们的 `AdRequest.Builder` 引用，以便可以链式调用方法。一旦设置了广告请求的所有特性，我们就可以使用 `build` 方法创建一个 `AdRequest` 对象。

下面展示了一段创建 `AdRequest` 并将其加载到 `AdView` 的代码序列：

![](img/9781284093650_CH15_FIGF04.jpg)

图 15.4 Logcat 输出显示设备 ID

```java
// 创建 AdRequest
AdRequest adRequest = adRequestBuilder.build();
// 加载广告
adView.loadAd(adRequest);
```

如果我们想使用模拟器测试应用，需要在调用 `build` 创建 `AdRequest` 之前添加这一行：

```java
adRequestBuilder.addTestDevice(AdRequest.DEVICE_ID_EMULATOR);
```

如果我们是一名注册开发者，并且已经从 Google 获取了有效的广告单元 ID，可以在调用 `build` 之前添加这一行来创建用于测试的 `AdRequest`。在应用的最终版本中，提交到 Google Play 之前，我们应该删除或注释掉这一行。

我们可以获取用于测试应用的设备的设备 ID（一个 32 位十六进制字符串）。通过查看在已连接设备上运行应用时的 Logcat 输出来获取。对于作者的设备，Logcat 输出如下，也显示在图 15.4 中（如果在 Logcat 中找不到，请使用 Ads 标签过滤消息，如下所示）：

```text
Use AdRequest.Builder.addTestDevice("DE4?????????????????7A") to
get test ads on this device.
```

因此，对于作者的设备，我们可以包含以下代码在平板电脑上测试应用（出于安全和隐私原因，图 15.4 中的设备 ID 被部分隐藏，下面用 `?` 字符填充）。

```java
String deviceId = "DE4?????????????????7A";
adRequestBuilder.addTestDevice(deviceId);
```

![](img/ch15exa13.jpg) ![](img/ch15exa13a.jpg)

示例 15.13 `MainActivity` 类，秒表应用，版本 3

示例 15.13 展示了更新后的 `MainActivity` 类，其中包括创建 `AdView`，然后创建 `AdRequest`，并加载广告。唯一的修改在 `onCreate` 方法的第 25–48 行。在第 25–30 行，我们创建了一个 `AdView`，并使用 `SMART_BANNER` 设置其尺寸，使用 Google 提供的默认广告单元 ID 设置广告单元 ID。在第 32–41 行，我们创建并定义了一个 `AdRequest`。投放的广告将定位对 `fitness` 和 `workout` 感兴趣的用户（第 36–37 行）。如果在模拟器上运行应用，我们要求发送测试广告而非真实广告（第 38–39 行）。在第 41 行，我们使用 `AdRequest.Builder` 引用 `adRequestBuilder` 调用 `build` 来创建 `AdRequest`。在第 43–45 行，我们获取 ID 为 `ad_view` 的 `LinearLayout`，并将 `AdView` 放入其中。在第 47–48 行，我们在 `AdView` 中加载符合 `adRequest` 的广告。

需要在 `AndroidManifest.xml` 文件中添加三项内容，如示例 15.14 所示。一个 `uses-permission` 元素用于访问互联网（第 5–6 行），一个必需的 `meta-data` 元素用于使用 Google 服务（第 15–17 行），以及另一个 `activity` 元素，如第 29–32 行所示。注意，第 30 行和第 31 行在 `AndroidManifest.xml` 文件中应合并为一行。

本章开头的图 15.1 展示了正在运行的秒表应用版本 3，包括屏幕底部的横幅广告。如果我们是一名注册开发者，并且正在使用自己的应用单元 ID，则不应为了测试目的点击真实广告：这样做违反 Google 政策。如果我们想测试横幅广告的功能，则应使用测试广告，可以通过以下方式获取：

* ▸ 使用 Google 提供的测试广告单元 ID；或者
* ▸ 通过 `AdRequest.Builder.addTestDevice` 请求测试广告。

![](img/ch15exa14.jpg)

示例 15.14 `AndroidManifest.xml` 文件，秒表应用，版本 3

## 15.5 将广告放置在 Fragment 中，秒表应用，版本 4

Google 建议使用 Fragment 来放置 `AdView`。这样做的一个好处是 Fragment 的 XML 布局文件可以在其他应用中重复使用。在版本 4 中，我们将 `AdView` 放置在 Fragment 内部，而不是 `LinearLayout` 中。从版本 3 升级到版本 4 涉及以下步骤：

* ▸ 为 Fragment 创建一个 XML 布局文件。
* ▸ 将 `activity_main.xml` 文件中的最后一个 `LinearLayout` 替换为 Fragment。
* ▸ 编写 Fragment 类。
* ▸ 更新 `MainActivity` 类。

示例 15.15 展示了 Fragment 的 XML 布局文件。我们将 `AdView` 元素（第 7–15 行）放置在 `RelativeLayout` 元素（第 2 行）内部。我们在第 8 行为 `AdView` 指定了一个 ID，以便在 Fragment 类中使用 `findViewById` 方法获取它。我们在第 13–14 行指定了 `AdView` 的尺寸和广告单元 ID。在第 11–12 行，我们将 `AdView` 在 `RelativeLayout` 中水平和垂直居中。

![](img/ch15exa15.jpg)

示例 15.15 `fragment_ad.xml` 文件，秒表应用，版本 4



示例 15.16 展示了更新后的 `activity_main.xml` 文件：我们将最后一个 `LinearLayout` 元素替换为 `fragment` 元素（第 59–64 行）。我们在第 60 行为其指定了一个 ID，并在第 61 行指定它是 `AdFragment` 类的一个实例。虽然在此应用中我们没有使用它的 ID，但如果不为 Fragment 指定 ID 或标签，应用在运行时将会崩溃。

![](img/ch15exa16.jpg) ![](img/ch15exa16a.jpg)

示例 15.16 `activity_main.xml` 文件，秒表应用，版本 4

示例 15.17 展示了我们的 Fragment 类，我们将其命名为 `AdFragment`。在 `onCreateView` 方法中，我们在第 15 行加载了 `fragment_ad.xml` 文件。在 `onActivityCreated` 方法中，我们使用其 ID 获取 Fragment 中指定的 `AdView`（第 21–22 行），构建一个 `AdRequest`（第 23–31 行），并将其加载到 `AdView` 中（第 32–33 行）。

![](img/ch15exa17.jpg) ![](img/ch15exa17a.jpg)

示例 15.17 `AdFragment` 类，秒表应用，版本 4

由于所有与横幅广告相关的代码都在 `AdFragment` 类中，因此 `MainActivity` 类与版本 2 中的相同。

## 15.6 管理 `AdView` 的生命周期，秒表应用，版本 5

`AdView` 类包含生命周期方法，如表 15.7 所示，这样当应用进入后台或退出时，我们可以避免不必要的处理。在 Fragment 类内部，`onPause`、`onResume` 和 `onDestroy` 生命周期方法会随着父 Activity 进入后台、前台或退出而自动调用。因此，我们可以从 Fragment 的生命周期方法中调用 `AdView` 的生命周期方法。

示例 15.18 展示了我们应用第 5 版中更新后的 `AdFragment` 类。所有其他类和文件保持不变。由于我们需要从 `onPause`（第 38–42 行）、`onResume`（第 44–48 行）和 `onDestroy`（第 50–54 行）中访问 `AdView`，我们将 `AdView` 设为实例变量（第 12 行），以便能够直接引用它。在这三个方法内部，我们暂停、恢复或销毁 `AdView`，并调用 `super` 方法。注意，在 `onPause` 和 `onDestroy` 内部，我们先 `pause` 或 `destroy` `AdView`，再调用 `super` 方法：我们希望在暂停或销毁片段本身之前，先暂停 `AdView` 的处理或销毁片段内的 `AdView`。在 `onResume` 内部，我们先调用 `super` 方法，再通过实例变量 `adView` 调用 `resume`：我们希望在恢复 `AdView`（位于片段内部）的处理之前，先恢复片段的处理。

| 方法 | 描述 |
| --- | --- |
| `public void pause()` | 暂停与此 `AdView` 相关的任何额外处理。 |
| `public void resume()` | 在调用 `pause` 后，恢复与此 `AdView` 相关的处理。 |
| `public void destroy()` | 销毁此 `AdView`。 |

`1package com.jblearning.stopwatchv5;`

表 15.7 `AdView` 类的生命周期方法

![](img/ch15exa18.jpg) ![](img/ch15exa18a.jpg)

示例 15.18 `AdFragment` 类，秒表应用，第 5 版

注意，`AdFragment` 并非直接可复用，因为此广告请求的性别和关键词是特定于该应用的。我们可以将广告请求构建器设为实例变量，并在 `AdFragment` 内部提供设置这些参数的方法。这留作练习。

## 章节总结

- `Chronometer` 类封装了一个秒表。
- `SystemClock` 类的 `static` 方法 `elapsedRealtime` 返回自上次启动以来的时间（以毫秒为单位），包括休眠时间。
- `com.google.android.gms.ads` 包提供了一组用于显示广告和管理广告的类。
- `com.google.android.gms.ads` 包是 Google Play 服务的一部分。要使用它，我们需要相应地编辑 `build.gradle` 文件。
- `AdView` 类继承自 `View`，封装了一个可以显示广告横幅的 `View`。
- `AdSize` 类封装了横幅广告的尺寸。它包含了各种行业标准横幅尺寸的常量。
- `AdRequest.Builder` 类提供了定义数据（如性别、位置和关键词）的方法，这些数据使广告能够针对特定人群。
- `AdRequest.Builder` 类的 `build` 方法返回一个 `AdRequest` 引用。
- 我们可以使用以下广告单元 ID 进行测试：`ca-app-pub-3940256099942544/6300978111`
- 在 `AdView` 调用 `loadAd` 方法加载广告之前，我们必须设置 `AdView` 的尺寸和广告单元 ID。
- 根据 Google 的建议，我们可以使用片段来放置横幅广告。
- 包含 Google 广告需要在 `AndroidManifest.xml` 文件中添加三项内容：
  - 需要 `INTERNET` 权限，因为任何显示 Google 广告的应用都会使用互联网。
  - 还需要一个 `meta-data` 元素，表明使用了 Google Play 服务。
  - 需要为 `AdActivity` 添加一个额外的 `activity` 元素。

![](img/common.jpg)

## 练习、问题与项目

### 选择题

1. `com.google.android.gms.ads` 包是 Google Play 服务的一部分。
   - 正确
   - 错误

2. 哪个类不在 `com.google.android.gms.ads` 包中？
   - `AdView`
   - `AdBuilder`
   - `AdSize`
   - `AdRequest`

3. `Builder` 类是哪个类的内部静态类？
   - `AdView`
   - `AdRequest`
   - `AdSize`
   - `AdListener`

4. 我们可以使用什么方法来确保在测试期间只收到测试广告，而不是真实广告？
   - `addTest`
   - `addDevice`
   - `addTestDevice`
   - `addEmulator`

5. 如果我们不是 Android 开发者，因此无法从 Google 获取广告单元 ID，我们就无法测试包含横幅广告的应用。
   - 正确
   - 错误：我们可以使用 Google 提供的默认广告单元 ID

6. 哪个方法不是可以指定广告请求目标人群的方法之一？
   - `setLocation`
   - `setBirthday`
   - `setGender`
   - `setKeyword`

7. 当 `AdView` 的尺寸或广告单元 ID 未设置时，`loadAd` 方法会抛出什么异常？
   - `IOException`
   - `IllegalStateException`
   - `LoadException`
   - `AdViewException`

8. 对于使用横幅广告的应用，哪个元素不是我们需要在 `AndroidManifest.xml` 文件中包含的？
   - `activity`
   - `uses-permission`
   - `meta-data`
   - `uses-storage`

### 补全代码

9. 在 `Activity` 类内部，创建一个 `AdView` 并设置其尺寸，使其符合 IAB 排行榜广告尺寸（你需要查看 `AdSize` 类来获取该尺寸）。

10. 在 `Activity` 类内部，创建一个 `AdView` 并将其广告单元 ID 设置为 Google 提供的用于测试的默认字符串。

11. 创建一个简单的 `AdRequest`，以便我们使用测试广告而不是真实广告。

12. 创建一个针对男性的 `AdRequest`，使用关键词 `game` 和 `video`。

13. 创建一个针对女性的 `AdRequest`，使用生日为 2000 年 1 月 1 日。

14. 创建一个 `AdRequest`，考虑到我们将在模拟器中测试应用，并且我们只想要测试广告，而不是真实广告。

15. 假设 `AdView` `myAdView` 已创建，其尺寸和广告单元 ID 已设置，并且 `AdRequest` `myRequest` 已构建，将广告加载到 `myAdView` 中。

16. 在 `AndroidManifest.xml` 中，为包含横幅广告的应用编写与权限相关的元素。

17. 在 `AndroidManifest.xml` 中，为包含横幅广告的应用编写额外的 `activity` 元素。

18. 在 `AndroidManifest.xml` 中，为包含横幅广告的应用编写与元数据相关的元素。

### 编写应用

19. 制作一个简单的闪光灯应用，底部带有横幅广告。闪光灯是一个黄色的 `View`，占据除横幅广告外的整个屏幕。

20. 制作一个闪光灯应用，顶部带有横幅广告。闪光灯是一个黄色的 `View`，占据除横幅广告和 `SeekBar` 外的整个屏幕。黄色的 `View` 可调光，你应该使用 `SeekBar` 来实现。包含一个模型。

21. 制作一个你选择的应用（应具有某些功能），其中横幅广告的显示由事件触发，例如用户点击按钮。

22. 制作一个你选择的应用（应具有某些功能），其中横幅广告在用户运行应用时有 50% 的概率显示。

23. 制作一个你选择的应用（应具有某些功能），带有横幅广告。该应用应包含某种形式的用户输入（可以是 `EditText`，或者一些可供选择的列表）。你需要将用户输入用作广告请求的关键词。

24. 修改秒表应用第 5 版，使 `AdFragment` 类完全可复用（即，它不应设置特定的性别和关键词）。将广告的自定义限制为性别和关键词。

# 第十六章：安全与加密

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

## 引言

对于每个计算机用户，尤其是移动设备用户来说，安全是一个非常重要的问题。有价值的数据（如信用卡号）如果未得到妥善保护，可能会被盗取。保护数据的一种方法是加密。随着技术的发展，计算机变得越来越强大，曾经被认为坚固安全的加密算法可能会变弱。在选择加密算法时，明智的做法是检查它在使用时是否仍然安全。在本章中，我们将学习各种加密算法以及如何使用它们来加密数据。

## 16.1 对称加密与非对称加密

加密通常涉及使用特定的算法和密钥来加密消息。密钥通常是一串字符。在密码学中，为了测试加密算法的强度，我们通常假设算法已知，并评估找到其关联密钥的难度。因此，除了理解加密算法的工作原理外，了解如何为该算法生成密钥也很重要。

加密系统可以是单向或双向的。单向意味着一旦我们加密了某些内容，就无法解密。单向加密系统可用于加密密码。用户名和加密密码通常存储在服务器上的数据库中。用户从远程位置连接到该服务器并登录。明文密码仅由各个用户知晓，且永远不会存储在服务器上。由于加密过程发生在服务器端而非客户端，因此本章不讨论单向加密。

双向加密系统可以是对称的或非对称的。对称加密意味着用于加密明文消息的密钥与用于解密密文消息的密钥相同：只有一个密钥。这意味着消息的发送方和接收方都需要拥有该密钥。这反过来意味着至少有一人必须将密钥交给另一人。由于该密钥是保密的，因此挑战在于以安全的方式分发该密钥，确保没有其他人能够访问它。如果涉及超过两人，挑战会更大。人们可以决定每次发送消息时使用不同的密钥，以降低密钥被第三方窃取的风险。与往常一样，实用性和安全性之间存在权衡。

非对称加密意味着用于加密明文消息的密钥与用于解密密文消息的密钥不同：有两个密钥。其中一种系统是 `RSA`，以其三位发明者 Rivest、Shamir 和 Adleman 命名。在 `RSA` 系统中，每个人拥有一对密钥：一个公钥（公开）和一个私钥（秘密）。例如，如果 Alice 和 Bob 是该系统的两个用户，Alice 可以向 Bob 发送消息，使用 Bob 的公钥加密消息，如下所示：

```
encryptedMessage1 = rsa(publicKeyBob, message1)
```

Alice 知道 Bob 的公钥，因为它是公开的。由于该消息是使用 Bob 的公钥加密的，因此只能使用 Bob 的私钥解密。由于 Bob 的私钥是私密且保密的，只有 Bob 知道它。因此，只有 Bob 可以解密该消息。Bob 按如下方式解密消息：

```
decryptedMessage1 = rsa(privateKeyBob, encryptedMessage1)
```

Bob 可以回复 Alice，使用 Alice 的公钥加密消息，如下所示：

```
encryptedMessage2 = rsa(publicKeyAlice, message2)
```

Bob 知道 Alice 的公钥，因为它是公开的。由于该消息是使用 Alice 的公钥加密的，因此只能使用 Alice 的私钥解密。由于 Alice 的私钥是私密且保密的，只有 Alice 知道它。因此，只有 Alice 可以解密该消息。Alice 按如下方式解密消息：

```
decryptedMessage2 = rsa(privateKeyAlice, encryptedMessage2)
```

`RSA` 依赖于这样一个事实：找出一个非常大的合数的因子非常困难。合数是两个素数的乘积。例如，143 等于 13 乘以 11，是一个合数。`RSA` 的底层数学基础包括群论和模代数。

## 16.2 对称加密：模型（`AES`）、加密应用，版本 0

在版本 0 中，我们通过一个简单的应用来探索对称加密。我们还将研究密钥分发问题。我们构建一个使用对称加密对文本进行加密和解密的模型，并对其进行测试。Android 库中有许多对称加密算法。我们使用高级加密标准（`AES`）。我们可以通过调用 `Security` 类的 `getProviders` 方法，然后遍历所有提供者，来访问设备上可用的加密算法列表。这超出了本章的范围。

`javax.crypto` 包包含封装密码学概念的类和接口，例如 `Cipher`、`KeyGenerator` 和 `SecretKey`。`Cipher` 类提供了对加密和解密算法实现的访问。它的所有方法都是 `final` 的（即我们不能覆盖它们）。表 16.1 显示了 `Cipher` 类的一些选定方法。`Cipher` 没有 `public` 构造函数。我们使用其 `getInstance` 静态方法来获取对 `Cipher` 对象的引用。`getInstance` 方法的参数是一个表示加密算法名称的 `String`，例如 `AES`。`doFinal` 方法将字节数组加密或解密为另一个字节数组。在调用 `doFinal` 之前，我们应该调用 `init` 方法来指定三件事：

- `doFinal` 是加密还是解密（操作模式）。
- 加密/解密密钥。
- 一个随机性元素。

| 方法 | 描述 |
| --- | --- |
| `public static Cipher getInstance(String transformation)` | 返回一个用于 `transformation`（加密算法名称）的 `Cipher`。抛出 `NoSuchAlgorithmException` 和 `NoSuchPaddingException`。 |
| `public byte[] doFinal(byte[] input)` | 加密 `input` 和其他先前缓冲的字节，并返回结果加密字节。抛出 `IllegalBlockSizeException`、`BadPaddingException` 和 `IllegalStateException`。 |
| `public void init(int opMode, Key key, SecureRandom random)` | 使用操作模式 `opMode`、`key` 以及作为随机性源的 `random` 初始化此 `Cipher`。抛出 `InvalidKeyException` 和 `IllegalParameterException`。 |

表 16.1 `Cipher` 类的选定方法

| 方法 | 描述 |
| --- | --- |
| `public SecureRandom()` | 使用默认算法构造一个 `SecureRandom` 对象。我们可以用它生成伪随机数。 |

表 16.2 `SecureRandom` 类的选定构造函数

| 方法 | 描述 |
| --- | --- |
| `public static KeyGenerator getInstance(String algorithm)` | 返回一个 `KeyGenerator`，它可以为名为 `algorithm` 的加密算法生成密钥。抛出 `NoSuchAlgorithmException` 和 `NullPointerException`。 |
| `public void init(int keySize)` | 为此 `KeyGenerator` 初始化一个大小为 `keySize` 位的密钥。 |
| `public SecretKey generateKey()` | 返回此 `KeyGenerator` 的 `SecretKey` 引用。 |

表 16.3 `KeyGenerator` 类的选定方法



我们可以使用 `Cipher` 类的 `ENCRYPT_MODE` 和 `DECRYPT_MODE` 常量来指定模式（加密或解密）。`Key` 是一个接口，因此无法实例化。`SecretKey` 类实现了 `Key` 接口，并封装了对称加密算法的密钥。因此，我们可以将其用于 `init` 的第二个参数。

第三个参数的类型是 `SecureRandom`。`SecureRandom` 类封装了生成加密安全伪随机数的能力。我们可以使用 `SecureRandom` 类的默认构造函数实例化一个 `SecureRandom` 对象，该类是 `Random` 的子类，如表 16.2 所示。我们可以使用 `KeyGenerator` 类（如表 16.3 所示）来创建一个 `SecretKey`。`KeyGenerator` 没有 `public` 构造函数。我们使用 `getInstance` 静态方法来获取一个 `KeyGenerator` 对象的引用。`getInstance` 方法的参数是一个 `String`，表示加密算法的名称，例如 `AES`。`generateKey` 方法返回一个类型为 `SecretKey` 的密钥。在调用 `generateKey` 之前，我们应该调用 `init` 方法来指定密钥的位数大小。

我们首先编写一个类（属于我们的 Model 部分），用于封装使用 `AES` 算法加密和解密 `String` 的能力。示例 16.1 展示了 `AESEncryption` 类。我们可以用它来生成一个密钥，也可以使用任何密钥执行加密和解密操作。它有一个默认构造函数、两个用于 `secretKey` 实例变量的访问器，以及 `crypt` 方法，我们可以用该方法加密或解密一个 `String`。为了加密或解密一个 `String`，我们需要一个 `SecretKey`、一个 `Cipher` 和一个 `SecureRandom` 引用。因此，我们声明了这三个类型的实例变量（`secretKey`、`cipher` 和 `rand`）（第 11–13 行），以便在 `crypt` 方法中访问它们。在构造函数内部（第 15–24 行），我们在第 17 行实例化 `cipher`，在第 18 行实例化 `rand`。我们在第 19 行为 `AES` 算法实例化一个 `KeyGenerator` 对象，在第 20 行用 256 位的密钥大小初始化它，并在第 21 行用它实例化 `secretKey`。我们在第 22 行捕获 `NoSuchAlgorithmException` 或 `NoSuchPaddingException`。

![](img/ch16exa01.jpg) ![](img/ch16exa01a.jpg)

**示例 16.1** 加密应用第 0 版的 `AESEncryption` 类

我们为算法的密钥 `secretKey` 提供了两个访问器。第一个 `getSecretKey`（第 38–40 行）返回 `secretKey`。第二个 `getKeyBytes`（第 42–44 行）将 `secretKey` 表示为字节数组并返回。通常，我们需要将密钥分发给远程用户。如果我们想以电子方式分发密钥，可以通过安全连接将字节数组发送给用户，使用 `getKeyBytes` 方法获取密钥的字节数组表示。我们也可以在发送时对密钥进行加密。在 `getKeyBytes` 内部，我们调用了 `SecretKey` 的 `getEncoded` 方法，该方法继承自 `Key` 接口，如表 16.4 所示。

我们可以使用 `crypt` 方法（第 26–36 行）使用给定的密钥加密或解密一个 `String`。它的第一个参数指定是加密还是解密。如果要加密，我们将 `Cipher.ENCRYPT_MODE` 作为第一个参数传入。如果要解密，则传入 `Cipher.DECRYPT_MODE`。第三个参数表示一个加密密钥。在这个例子中，我们传入的是这个 `AESEncryption` 对象的密钥。我们使用 `opMode` 指定的模式以及密钥参数 `key` 和 `rand` 来初始化 `cipher`（第 28 行）。`doFinal` 方法接受一个字节数组参数，因此我们在第 29 行将 `String` 参数转换为字节数组。我们使用 `ISO-8859-1` 编码标准将字节数组转换为 `String`：`ISO-8859-1` 是通过 HTTP 协议以 MIME 类型传输文档的默认编码标准；它在 `String` 和字节数组之间提供了一对一的映射。在第 30 行，我们调用 `doFinal` 将该字节数组加密为另一个字节数组，并在第 31 行将该字节数组转换为 `String`。我们在第 32 行返回该 `String`。我们在第 33 行捕获所有可能的 `Exceptions`，如果发生 `Exception`，则在第 34 行返回 `null`。

| 方法 | 描述 |
| --- | --- |
| `byte[] getEncoded()` | 返回此 `Key` 的编码形式，以字节数组表示。 |

表 16.4 `Key` 接口的 `getEncoded` 方法

在 `MainActivity` 类中（如示例 16.2 所示），我们使用 `AESEncryption` 类来加密一个 `String`，并将其加密版本解密回原始 `String`。我们还测试了将密钥转换为字节数组、从该字节数组重建密钥，以及重建的密钥与原始密钥匹配。这就是我们以电子方式分发密钥时发生的操作类型。在第 20 行，我们实例化 `aes`，一个 `AESEncryption` 实例变量。我们在第 25–26 行加密 `String original`，并在第 27 行将加密后的 `String` 输出到 Logcat。我们在第 28–29 行解密加密后的 `String`，并在第 30 行将结果输出到 Logcat，如图 16.1 所示，该结果与我们最初使用的 `String` 相同。

![](img/ch16exa02.jpg) ![](img/ch16exa02a.jpg)

**示例 16.2** 加密应用第 0 版的 `MainActivity` 类

在第 32–45 行，我们模拟分发密钥，并检查接收到的密钥是否与发送的密钥匹配。我们从 `aes` 的密钥开始，在第 32–33 行将其转换为字节数组。在第 34–36 行，我们将该字节数组作为对象和对应的 `String` 输出。然后，我们假设该字节数组被发送给用户，并在第 38–39 行用它重建一个密钥。我们在第 40–41 行检索该重建密钥对应的字节数组。最后，在第 42–45 行，我们将该字节数组作为对象和对应的 `String` 输出。

![](img/9781284093650_CH16_FIGF01.jpg)

图 16.1 加密应用第 0 版的 Logcat 输出

图 16.1 显示了 Logcat 中的输出。我们可以看到两件事：两个字节数组的内存地址不同，但它们的值相同。因此，这个例子表明，我们可以通过传输字节来将密钥从一个用户传输到另一个用户。

## 16.3 对称加密：添加视图，加密应用第 1 版

在第 1 版中，我们添加了一个用户界面，使用户能够输入一个 `String`。我们提供了一个按钮来加密该 `String` 并解密加密后的字符串，从而恢复原始 `String`。

示例 16.3 展示了 `activity_main.xml` 文件。我们使用 `RelativeLayout` 来组织各个元素。我们还引用了 `styles.xml` 和 `strings.xml` 文件中定义的样式和字符串。`styles.xml` 文件使用了我们在 `colors.xml` 文件中定义的颜色。示例 16.4、16.5 和 16.6 展示了这三个文件。`activity_main.xml` 文件包含左侧的三个 `TextViews`，用作 `EditText`（第 20–26 行）的标签，以及右侧的两个 `TextViews`（第 37–42 行和第 53–58 行）。我们为这三个元素赋予了 id（第 21、38、54 行），以便在 `MainActivity` 类中使用 `findViewById` 方法检索它们。当用户在 `EditText` 中输入内容并点击按钮（第 60–66 行）时，`encryptAndDecryptAES` 方法会执行（第 66 行）。我们相应地更新右侧的两个 `TextViews`，显示加密后的 `String` 以及解密加密 `String` 的结果。

![](img/ch16exa03.jpg) ![](img/ch16exa03a.jpg)

**示例 16.3** 加密应用第 1 版的 `activity_main.xml` 文件

![](img/ch16exa04.jpg)

**示例 16.4** 加密应用第 1 版的 `strings.xml` 文件

![](img/ch16exa05.jpg)

**示例 16.5** 加密应用第 1 版的 `colors.xml` 文件

![](img/ch16exa06.jpg) ![](img/ch16exa06a.jpg)

**示例 16.6** 加密应用第 1 版的 `styles.xml` 文件

示例 16.7 展示了 `MainActivity` 类。在 `encryptAndDecryptAES` 方法（第 21–34 行）中，我们获取用户输入并更新屏幕右侧的两个 `TextView`。我们在第 22、26–27 和 29–30 行获取对 `EditText` 和两个 `TextView` 的引用。在第 23 行，我们获取用户输入。在第 24–25 行，我们对其进行加密。在第 28 行，我们将结果放入屏幕中间右侧的 `TextView` 中。我们在第 31–32 行解密加密后的 `String`，并在第 33 行将结果放入另一个 `TextView` 中。

![](img/ch16exa07.jpg) ![](img/ch16exa07a.jpg)

**示例 16.7** 加密应用第 1 版的 `MainActivity` 类

图 16.2 展示了用户在输入 `Android is fun` 并点击按钮后，应用在模拟器中的运行情况。

![](img/9781284093650_CH16_FIGF02.jpg)

图 16.2 加密应用第 1 版在模拟器中运行

## 16.4 非对称加密：向模型添加 RSA——加密应用第 2 版

在第 2 版中，我们向模型添加了 RSA 加密，并在 `MainActivity` 类中进行了测试。我们可以使用示例 16.8 中所示的 `RSAEncryption` 类来生成一组私钥和公钥，并使用任意密钥执行加密和解密。此设计与 `AESEncryption` 类类似。我们在第 11–13 行声明了三个实例变量：`cipher`（一个 `Cipher` 引用）以及两个密钥——`privateKey` 和 `publicKey`。构造函数（第 15–25 行）在第 17 行实例化 `cipher`，并在第 18–22 行生成两个密钥。

![](img/ch16exa08.jpg) ![](img/ch16exa08a.jpg)

**示例 16.8** 加密应用第 2 版的 `RSAEncryption` 类

`KeyPairGenerator` 类具有生成 `KeyPair` 的方法，`KeyPair` 封装了一对密钥（一个私钥和一个公钥）。表 16.5 展示了这两个类的方法。`KeyPairGenerator` 类是 `abstract` 的，无法实例化。不过，我们可以使用其 `getInstance` 静态方法获取对 `KeyPairGenerator` 的引用（第 18 行）。`getInstance` 方法接受一个 `String` 参数，该参数表示 `KeyPairGenerator` 用于生成 `KeyPair` 的算法。`genKeyPair` 方法（在第 20 行调用）返回一个 `KeyPair`：我们可以使用 `KeyPair` 类的 `getPrivate` 和 `getPublic` 方法（第 21 和 22 行）检索这两个密钥。`getPrivate` 和 `getPublic` 方法分别返回 `PrivateKey` 和 `PublicKey`。这两个接口都继承自 `Key` 接口。因此，我们可以将它们的返回值赋给 `privateKey` 和 `publicKey` 实例变量（第 21 和 22 行）。我们在第 27–29 行和第 31–33 行为这两个密钥提供了访问器。我们还为这两个密钥的字节数组表示提供了访问器，以便它们可以以电子方式传输。我们可以将公钥传输到中心位置（可能位于服务器上），以便其他用户可以检索它。如果我们提供生成密钥的客户端软件，则无需将私钥传输给每个用户，因此泄露一个或多个私钥的风险要低得多。如果必须以安全方式将私钥传输给特定用户，我们可以使用像 `AES` 这样的算法对其进行加密。

| 类 | 方法 | 描述 |
| --- | --- | --- |
| `KeyPairGenerator` | `public static KeyPairGenerator getInstance( String algorithm )` | 返回一个使用指定算法的 `KeyPairGenerator`。 |
| `KeyPairGenerator` | `initialize( int keySize )` | 使用 `keySize`（以位为单位）初始化此 `KeyPairGenerator`。 |
| `KeyPairGenerator` | `KeyPair genKeyPair( )` | 生成并返回一个新的 `KeyPair`。 |
| `KeyPair` | `PrivateKey getPrivate( )` | 返回此 `KeyPair` 的私钥。 |
| `KeyPair` | `PublicKey getPublic( )` | 返回此 `KeyPair` 的公钥。 |

表 16.5 `KeyPair` 和 `KeyPairGenerator` 类的选定方法

`crypt` 方法（第 43–53 行）与 `AESEncryption` 类的 `crypt` 方法相同，只是它使用 `RSA` 的 `Cipher` 引用而不是 `AES`。

示例 16.9 中所示的 `MainActivity` 类演示了如何使用 `RSAEncryption` 类。由于 `RSA` 加密算法是非对称的，我们执行了两个测试。我们在第 15 行声明了一个 `RSAEncryption` 实例变量，并在第 21 行实例化它。我们首先使用公钥加密并使用私钥解密（第 24–32 行），然后使用私钥加密并使用公钥解密（第 34–42 行）。图 16.3 显示，在这两种情况下，我们在连续加密和解密后都得到了原始的 `String`。两个加密后的 `String` 表明加密不是对称的。如图所示，加密后的 `String` 比显示的要长得多。

![](img/ch16exa09.jpg) ![](img/ch16exa09a.jpg)

**示例 16.9** 加密应用第 2 版的 `MainActivity` 类

![](img/9781284093650_CH16_FIGF03.jpg)

图 16.3 加密应用第 2 版的 Logcat 输出

## 16.5 对称与非对称加密：修改视图——加密应用第 3 版

在第 3 版中，我们向用户展示了三个按钮：第一个按钮触发 `AES` 加密和解密（与之前相同），另外两个按钮触发 `RSA` 加密和解密，使用我们可用的两种场景：

- 一种使用私钥加密，使用公钥解密。
- 另一种使用公钥加密，使用私钥解密。

我们修改了 `activity_main.xml` 文件（视图），并添加了两个按钮。这两个按钮在示例 16.10 的第 67–74 行和第 76–83 行中编码。我们为 AES 按钮指定了一个 id（第 60 行），以便我们可以相对于它定位两个新按钮。此外，由于我们现在有三个按钮，AES 按钮不再居中。因为 `RSA` 加密产生的 `String` 比 `AES` 加密大得多，我们在第一行和第二行组件之间指定了比之前更大的边距（第 30 行）。

我们还在 `strings.xml` 中定义了 `button_rsa1` 和 `button_rsa2` 字符串。

![](img/ch16exa10.jpg) ![](img/ch16exa10a.jpg) ![](img/ch16exa10b.jpg)

**示例 16.10** 加密应用第 3 版的 `activity_main.xml` 文件

示例 16.11 展示了更新后的 `MainActivity` 类。由于我们需要在三个不同的方法中访问 GUI 组件，我们在第 14–16 行为它们添加了三个实例变量。我们在第 24–26 行使用 `findViewById` 方法实例化它们。请注意，在检索它们之前设置内容 `View`（第 23 行）非常重要。否则，它们将为 `null`，并且应用最终会在运行时崩溃。`encryptAndDecryptRSA1` 和 `encryptAndDecryptRSA2` 方法与 `encryptAndDecryptAES` 方法非常相似。`encryptAndDecryptRSA1` 方法使用私钥加密（第 46–47 行）并使用公钥解密（第 49–50 行）。`encryptAndDecryptRSA2` 方法使用公钥加密（第 56–57 行）并使用私钥解密（第 59–60 行）。

![](img/ch16exa11.jpg) ![](img/ch16exa11a.jpg)

**示例 16.11** 加密应用第 3 版的 `MainActivity` 类

![](img/9781284093650_CH16_FIGF04.jpg)

图 16.4 用户点击 RSA 1 后的加密应用第 3 版

![](img/9781284093650_CH16_FIGF05.jpg)

图 16.5 用户点击 RSA 2 后的加密应用第 3 版

图 16.4 和 16.5 展示了用户在输入 `Android is fun` 并分别点击 RSA 1 按钮和 RSA 2 按钮后的应用界面。

## 章节总结



加密算法可以是单向的（加密后无法解密）、对称的（加密和解密使用相同的密钥）或非对称的（加密和解密使用不同的密钥）。

- `javax.crypto` 包提供了封装各种密码学概念和功能的接口和类。
- 我们可以使用 `KeyGenerator` 类为对称加密算法生成密钥。
- 我们可以使用 `KeyPairGenerator` 类为非对称加密算法生成一对密钥。
- 封装密钥的类提供了将密钥对象转换为字节数组以及从字节数组重建密钥的方法。这样，我们就可以通过电子方式传输密钥。密钥分发是一个重要问题。
- 我们可以使用 `SecureRandom` 类生成加密安全的伪随机数。
- `Cipher` 类提供了对加密和解密算法实现的访问。
- `Cipher` 类的 `doFinal` 方法将一个字节数组加密或解密为另一个字节数组。
- 我们可以使用 `ISO-8859-1` 编码标准将字节数组转换为 `String`，反之亦然。它在 `String` 和字节数组之间提供了一对一的映射。
- 在调用 `doFinal` 方法进行加密或解密之前，我们调用 `init` 来指定模式（加密或解密）、密钥，并设置一个随机性元素。

![](img/common.jpg)

## 练习、问题和项目

### 选择题

1. 非对称加密算法使用相同的密钥进行加密和解密。
   - 正确
   - 错误

2. 我们在哪个包中找到封装密码学概念和功能的接口和类？
   - `java.crypto`
   - `javax.crypto`
   - `android.crypto`
   - `android.algorithm`

3. 我们可以使用哪个类为 `RSA` 算法生成私钥及其对应的公钥？
   - `Key`
   - `KeyGenerator`
   - `KeyPairGenerator`
   - `SecretKey`

4. 提供各种加密和解密算法实现的类叫什么？
   - `Crypt`
   - `Encrypt`
   - `RSA`
   - `Cipher`

5. 问题 4 中类的 `doFinal` 方法将：
   - 字节数组转换为 `String`
   - `String` 转换为字节数组
   - `String` 转换为 `String`
   - 字节数组转换为字节数组

6. 问题 4 中类的 `init` 方法的第一个参数是一个 `int`。如果要加密，我们可以使用哪个值？
   - `Cipher.ENCRYPT_MODE`
   - `Cipher.ENCRYPT`
   - `Cipher.DECRYPT`
   - `Cipher.DECRYPT_MODE`

7. 问题 4 中类的 `init` 方法的第一个参数是一个 `int`。如果要解密，我们可以使用哪个值？
   - `Cipher.ENCRYPT_MODE`
   - `Cipher.ENCRYPT`
   - `Cipher.DECRYPT`
   - `Cipher.DECRYPT_MODE`

### 补全代码

8. 编写代码，为 `AES` 算法声明并实例化一个 `Cipher` 对象。
9. 编写代码，为 `RSA` 算法声明并实例化一个 `Cipher` 对象。
10. 编写代码，为 `AES` 算法声明并实例化一个 `KeyGenerator` 对象。
11. 编写代码，为 `RSA` 算法声明并实例化一个 `KeyPairGenerator` 对象。
12. 变量 `keyPair` 是一个 `KeyPairGenerator` 引用，并且已经为 `RSA` 算法实例化。编写代码以获取其私钥的字节数组。
13. 变量 `keyPair` 是一个 `KeyPairGenerator` 引用，并且已经为 `RSA` 算法实例化。编写代码以获取其公钥的字节数组。
14. 一个名为 `s` 的 `String` 已被初始化。编写代码，使用 `ISO-8859-1` 编码标准将其转换为字节数组。
15. 一个字节数组已用某些值初始化。编写代码，使用 `ISO-8859-1` 编码标准将其转换为 `String`。
16. 一个名为 `myCipher` 的 `Cipher` 引用已被声明并实例化。密钥 `myKey` 也已被声明并实例化。编写代码以初始化 `myCipher`，使其准备好使用 `myKey` 加密某些内容。
17. 一个名为 `myCipher` 的 `Cipher` 引用已被声明、实例化，并已使用某个密钥初始化为加密模式。编写代码以加密字节数组 `myBytes`。将结果赋值给你选择的变量。

### 编写应用程序

18. 编写一个类似于本章版本 1 的应用程序。选择一种不同于 `AES` 的加密算法。
19. 编写一个类似于本章版本 1 的应用程序。改用第二个参数为 `Certificate` 的 `init` 方法。
20. 编写一个发送电子邮件的应用程序。使用 `AES` 加密电子邮件正文。
21. 编写一个使用 `RSA` 的应用程序，要求用户输入一个句子。一个按钮使用用户 1 的私钥和用户 2 的公钥加密该句子，并在 `TextView` 中显示结果（用户 2 知道该句子来自用户 1 后可以解密）。另一个按钮将结果解密回原始句子，并在另一个 `TextView` 中显示。
22. 制作一个应用程序，使用凯撒密码（字母表中的每个字母都移动固定数量：例如，如果偏移量为 3，则 a 变为 d，b 变为 e，等等）加密用户输入。
23. 查看 `java.security` 包中的 `Security` 类。制作一个应用程序，使用该类检索 Android 设备支持的所有加密算法。

## 附录 A：动态获取状态栏和操作栏的高度

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

如果我们以编程方式定义 `View`，通常需要获取内容视图的高度，即屏幕总高度减去状态栏和操作栏的高度。

图 A.1 显示了设备屏幕的各个部分。设备的**状态栏**以黄色显示：它通常包含一些系统和应用程序通知的图标，包括时钟。红色部分是应用程序的**操作栏**，通常左上角显示应用程序名称，右侧显示菜单，但具体取决于应用程序。应用程序内容 `View` 以蓝色显示。这是应用程序内容所在的位置。可见显示帧由应用程序的操作栏（红色）和应用程序内容 `View`（蓝色）组成。

在撰写本文时，根据 Google 的设计指南，状态栏的高度为 24 dp，操作栏的高度为 56 dp。这些数字以密度无关像素给出，因此要计算实际像素数，我们需要将它们乘以设备的逻辑像素密度。无法保证状态栏和操作栏的高度将来不会改变。因此，最好以编程方式获取它们。

以下代码序列显示了如何获取设备的逻辑像素密度。

```java
Resources res = getResources( );
DisplayMetrics metrics = res.getDisplayMetrics( );
float pixelDensity = metrics.density;
```

![](img/9781284093650_APPA_FIGF01.jpg)

图 A.1 屏幕的 `View` 组件

我们首先通过调用 `Activity` 类从 `ContextWrapper` 类继承的 `getResources` 方法获得一个 `Resources` 引用。我们可以使用 `Resources` 类来访问应用的资源。利用 `Resources` 引用 `res`，我们调用 `getDisplayMetrics` 方法来获取设备的 `DisplayMetrics` 引用。`DisplayMetrics` 类包含有关显示器的信息，包括其大小、密度和字体缩放。`DisplayMetrics` 类的 `density` 字段存储设备的逻辑像素密度。表 A.1 展示了 `ContextWrapper` 类的 `getResources` 方法、`Resources` 类的 `getDisplayMetrics` 方法以及 `DisplayMetrics` 类的 `density` 字段。

| 类 | 方法或字段 | 描述 |
| --- | --- | --- |
| `ContextWrapper` | `Resources getResources( )` | 返回此应用包的 `Resources` 引用。 |
| `Resources` | `DisplayMetrics getDisplayMetrics( )` | 返回此 `Resources` 对象的显示度量。 |
| `DisplayMetrics` | `density` | 密度无关像素单位的缩放因子。 |

表 A.1 `getResources`、`getDisplayMetrics` 方法以及 `DisplayMetrics` 的 `density` 字段

一旦我们获得了设备的密度，就可以为操作栏高度和状态栏高度分配默认值，如下所示：

```java
int actionBarHeight = ( int ) ( pixelDensity * 56 );
int statusBarHeight = ( int ) ( pixelDensity * 24 );
```

现在我们已经有了操作栏高度的默认值，可以尝试使用以下序列动态检索其值。如果不成功，则使用操作栏默认值。

```java
//   set default value for action bar height
int actionBarHeight = ( int ) ( pixelDensity * 56 );
TypedValue tv = new TypedValue( );
if( getTheme( ).resolveAttribute( android.R.attr.actionBarSize, tv, true ) )
  actionBarHeight = TypedValue.complexToDimensionPixelSize( tv.data,
                         getResources( ).getDisplayMetrics( ) );
```

操作栏的高度是应用主题的一部分。`getTheme` 方法（如表 A.2 所示）由 `Activity` 从 `ContextThemeWrapper` 继承而来，返回与当前 `Context` 关联的 `Theme`。`Theme` 是 `Resources` 类的内部类：它存储特定主题的属性值。`Theme` 类的 `resolveAttribute` 方法（如表 A.3 所示）检查某个属性是否存在于主题中。如果存在，则返回 `true` 并将属性值赋给其 `TypedValue` 参数（第二个参数）。操作栏高度的资源 ID 是 `android.R.attr.actionBarSize`。我们声明并实例化一个 `TypedValue` 引用 `tv`，目的是将其作为第二个参数传递给 `resolveAttribute` 方法。如果该方法返回 `true`，则将其值赋给 `actionBarHeight`。我们使用 `TypedValue` 类的 `complexToDimensionPixelSize` 静态方法（如表 A.4 所示）将 `tv` 内部的数据 `tv.data` 转换为表示像素数的整数。如果输出 `tv` 的类型 `tv.type`，可以看到其值为 5，即 `TypedValue` 类的 `TYPE_DIMENSION` 常量的值。

| 成员 | 描述 |
| --- | --- |
| `Resources.Theme getTheme( )` | 返回与当前 `Context` 关联的 `Theme`。 |

表 A.2 `ContextThemeWrapper` 类的 `getTheme` 方法

| 成员 | 描述 |
| --- | --- |
| `boolean resolveAttribute( int resourceId, TypedValue outValue, boolean resolveRefs )` | 如果属性 `resourceId` 存在于该 `Theme` 中，则返回 `true`。如果存在，则将其值赋给 `outValue`；`resolveRefs` 用于确定属性的资源类型。 |

表 A.3 `Resources.Theme` 类的 `resolveAttribute` 方法

| 成员 | 描述 |
| --- | --- |
| `public int data` | 此 `TypedValue` 中的数据。 |
| `public int type` | 此 `TypedValue` 中数据的类型。 |
| `static int complexToDimensionPixelSize( int data, DisplayMetrics metrics )` | 使用 `metrics` 作为显示度量，返回与 `data` 对应的像素数。`data` 的类型必须是 `TYPE_DIMENSION`（值为 5）。 |

表 A.4 `TypedValue` 类的资源

要动态检索状态栏高度的值，我们使用以下序列。如果不成功，则使用状态栏默认值。

```java
// set default value for status bar height
int statusBarHeight = ( int ) ( pixelDensity * 24 );
// res is a Resources reference
int resourceId =
    res.getIdentifier( "status_bar_height", "dimen", "android" );
// res.getIdentifier( "android:dimen/status_bar_height", "", "" );
if( resourceId != 0 ) // found resource for status bar height
  statusBarHeight = res.getDimensionPixelSize( resourceId );
```

我们可以通过调用 `Resources` 类的 `getIdentifier` 方法（如表 A.5 所示）来获取给定名称和资源类型的资源 ID。如果返回的值不为 `0`，则表示成功检索到。然后我们可以通过调用 `Resources` 的 `getDimensionPixelSize` 方法并传入该 ID 值来获取其尺寸。表 A.5 也展示了该方法。

| 成员 | 描述 |
| --- | --- |
| `int getIdentifier( String name, String type, String package )` | 返回名为 `name` 的资源的资源 ID；`type` 指定资源的类型（color、dimen 等），`package` 是资源所在的包。如果 `name` 中包含了 `type` 和 `package`（即类似于“package:type/resourceName”的字符串），则这两个参数可选。如果未找到，则返回 `0`。 |
| `int getDimensionPixelSize( int id )` | 返回 ID 为 `id` 的资源的像素数。 |

表 A.5 `Resources` 类的 `getIdentifier` 和 `getDimensionPixelSize` 方法

示例 A.1 展示了一个简单应用的 `MainActivity` 类，该应用检索状态栏和操作栏的高度。

![](img/App_A_exa01.jpg) ![](img/App_A_exa01a.jpg)

示例 A.1 `MainActivity` 类，展示如何检索当前设备的状态栏和操作栏高度

图 A.2 展示了示例 A.1 在 Nexus 5 模拟器上运行时的输出。检索到的操作栏高度为 168，等于 3（像素密度）乘以 56（Google 给出的操作栏高度，单位为 dp）。检索到的状态栏高度为 72，等于 3（像素密度）乘以 24（Google 给出的状态栏高度，单位为 dp）。

![](img/9781284093650_APPA_FIGF02.jpg)

图 A.2 示例 A.1 在 Nexus 5 模拟器上的输出

![](img/9781284093650_APPA_FIGF03.jpg)

图 A.3 示例 A.1 在 Nexus 4 模拟器上的输出

图 A.3 展示了示例 A.1 在 Nexus 4 模拟器上运行时的输出。检索到的操作栏高度为 112，等于 2（像素密度）乘以 56（Google 给出的操作栏高度，单位为 dp）。检索到的状态栏高度为 48，等于 2（像素密度）乘以 24（Google 给出的状态栏高度，单位为 dp）。我们可以验证资源 ID 与 Nexus 5 模拟器相同。

## 附录 B：动态设置 `TextView` 的字体大小

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

在构建应用时，`TextView` 内部的字体大小调整是一个常见问题。由于应用将在具有各种屏幕尺寸的许多设备上运行，如果对所有设备使用相同的字体大小，在某些设备上可能会显得不协调。有多种方法可以设置 `TextView` 内部的字体大小，以使文本适配良好。我们将探讨如何设置字体大小，使文本恰好在一行内显示且字体大小最大。我们假设 `TextView` 内部没有内边距。

我们构建一个工具类 `DynamicSizing`，其中包含一个静态方法，其工作方式如下：

它设置 `TextView` 中字体的大小，使得文本恰好占一行，并且字体大小达到最大。

该功能的另一种实现方式是继承 `TextView`，并将前面提到的方法定义为非 `static` 方法。



计算最佳字体的一种策略是从一个非常大的字体开始，例如大小为 200，然后每次减少 1 个字号，直到文本在`TextView`内需要两行或更多行才能容纳为止，如下面的伪代码所示：

```
字体大小 = 200
while (文本需要 2 行或更多行才能容纳在 TextView 内) {
  字体大小减 1
}
```

我们可以使用`TextView`类的`getLineCount()`方法（见表 B.1）来获取文本在`TextView`内所占的行数。动态调整`View`或其属性大小时出现的一个问题是，需要访问`View`的属性，例如宽度、高度或文本所占的行数。如果`View`尚未显示，则`getWidth()`、`getHeight()`和`getLineCount()`方法都会返回`0`。

我们可以调用`View`类的`measure()`方法（见表 B.1）来获取`TextView`内文本的宽度、高度和行数。如果先调用`measure()`，那么调用`getLineCount()`将返回文本在`TextView`内实际占用的行数。要在调用`measure()`后获取宽度和高度信息，应调用`getMeasuredWidth()`和`getMeasuredHeight()`方法。

`measure()`方法接受两个`int`参数，指定`View`的父视图对其施加或未施加的大小约束类型。表 B.2 显示了`MeasureSpec`类的三个常量，我们可以用它们来指定这两个参数的值。

| 类 | 方法 | 描述 |
| --- | --- | --- |
| `View` | `int getWidth()` | 返回 View 的宽度（像素），如果尚未显示则返回 0。 |
| `View` | `int getHeight()` | 返回 View 的高度（像素），如果尚未显示则返回 0。 |
| `View` | `void measure(int widthMeasureSpec, int heightMeasureSpec)` | 如果我们想获取 View 的大小则调用此方法；`widthMeasureSpec` 和 `heightMeasureSpec` 表示父 View 施加的水平和垂直要求。 |
| `View` | `int getMeasuredWidth()` | 返回通过调用 `measure` 测量得到的 View 宽度（像素）。 |
| `View` | `int getMeasuredHeight()` | 返回通过调用 `measure` 测量得到的 View 高度（像素）。 |
| `View` | `ViewParent getParent()` | 返回此 View 的父视图。 |
| `TextView` | `int getLineCount()` | 返回 TextView 内文本的行数，如果 TextView 尚未显示则返回 0。 |
| `TextView` | `void setTextSize(int unit, float size)` | 将 TextView 内文本的大小设置为 size 单位。 |
| `TextView` | `void setWidth(int w)` | 将 TextView 的宽度设置为 w 像素。 |
| `TextView` | `void setHeight(int h)` | 将 TextView 的高度设置为 h 像素。 |

表 B.1 `View`和`TextView`类的部分方法

示例 B.1 展示了我们的`DynamicSizing`工具类。我们在第 8 行声明了常量`MAX_FONT_SIZE`，等于`200`。我们将其用作字体的起始大小，然后每次减少`1`以找到正确的值，使文本恰好占一行。我们还声明了另一个常量`MIN_FONT_SIZE`，其值设置为`1`（第 9 行），并将此值用作`TextView`的最小字体大小。

第 11–32 行的`setFontSizeToFitInView()`方法接受一个`TextView`参数`tv`，并修改其字体大小。它返回修改后的字体大小。我们在第 18 行将`MAX_FONT_SIZE`的值赋给变量`fontSize`，并在第 19 行将`tv`的字体大小设置为`fontSize`。

我们使用`TypedValue`类中的整数常量`COMPLEX_UNIT_SP`作为`TextView`类的`setTextSize()`方法的第一个参数来指定单位。这意味着单位是缩放像素。表 B.3 显示了`TypedValue`类的几个常量。

| 常量 | 描述 |
| --- | --- |
| `UNSPECIFIED` | 父视图未对子 View 施加任何约束。 |
| `EXACTLY` | 父视图已确定子 View 的确切大小。 |
| `AT_MOST` | 父视图已确定子 View 的最大大小。 |

表 B.2 `MeasureSpec`类的常量

![](img/App_B_exa01.jpg)

示例 B.1 `DynamicSizing`工具类

| 常量 | 描述 |
| --- | --- |
| `COMPLEX_UNIT_IN` | 以英寸为单位的值。 |
| `COMPLEX_UNIT_PX` | 以原始像素为单位的值。 |
| `COMPLEX_UNIT_SP` | 以缩放像素为单位的值。 |

表 B.3 `TypedValue`类的常量

在第 21 行通过调用`getLineCount()`获取文本行数之前，我们在第 20 行调用了`measure()`，这样`getLineCount()`就不会返回`0`。如果它没有返回 0，我们在第 23–28 行循环，直到存储在变量`lines`中的行数等于`1`或字体大小降到`2`。

如果由于某种原因（例如文本非常长），字体大小达到`2`，我们就退出循环。这种情况不太可能发生，但良好的防御性编程实践可以防止意外情况。如果进入循环且字体大小大于`2`，则意味着行数大于`1`，因此需要减小字体大小。

我们在第 24 行将`fontSize`减`1`，在第 25 行重置`tv`的字体大小以反映这一点，在第 26 行调用`measure()`重置测量值，并在第 27 行更新`lines`。由于循环内字体大小减小，要么`lines`的值会达到`1`，要么`fontSize`的值会达到`2`。

退出循环后，我们在第 29 行将`tv`的字体大小重置为`fontSize – 1`，以确保文本在`tv`内恰好占一行。我们在第 31 行返回`fontSize`。请注意，我们没有考虑`TextView`内的任何内边距。

我们现在构建一个简单的应用，并编辑`activity_main.xml`文件和`MainActivity`类来测试`DynamicSizing`类的`setFontSizeToFitInView()`方法。

示例 B.2 展示了`activity_main.xml`文件。我们在第 15 行为`TextView`指定了一个 id，以便在`MainActivity`类中获取其引用，从而修改其宽度、文本以及文本的字体大小。我们在第 16 行将`TextView`的背景设置为黄色，以便可视化其边界。

示例 B.3 展示了`MainActivity`类。在第 13–14 行，我们获取了`TextView`。在第 15–17 行，我们设置了它的宽度和文本。在第 18–19 行，我们设置了它的字体大小，使其内部的文本恰好占一行。我们不需要`setFontSizeToFitInView()`的返回值，因此将调用`setFontSizeToFitInView()`作为独立语句。

![](img/App_B_exa02.jpg)

示例 B.2 `activity_main.xml`文件

![](img/App_B_exa03.jpg)

示例 B.3 `MainActivity`类

![](img/9781284093650_APPB_FIGF01.jpg)

图 B.1 在模拟器中运行的测试应用

图 B.1 展示了在模拟器中运行的应用。尝试更改`TextView`的文本（例如改为 PRO 或 PROGRAM）和/或宽度（例如改为 300），然后再次测试应用。字体大小会相应调整。

## 附录 C：如何下载和安装 Google Play 服务，使用地图

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

Android 标准开发工具包（Android SDK）并不包含我们开发所需的所有包和类。例如，地图和广告相关的类可能不包含在内。但是，我们可以通过 Android SDK 管理器下载并安装它们。表 C.1 显示了可能需要执行的额外步骤。

步骤 1 和 2 与开发环境相关，我们只需执行一次。步骤 3、4 和 5 与项目相关，每个项目都需要执行。

| 步骤 | 描述 |
| --- | --- |
| 1 | 下载并安装 Google Play 服务（如果尚未安装）。 |
| 2 | 下载并安装 Google API（如果尚未安装）。 |
| 3 | 更新 `build.gradle`（Module: app）文件（如果尚未更新——这取决于我们使用的 Android 模板）。 |
| 4 | 对于使用 Google Maps 的应用，从 Google 获取密钥（如果尚未获取）。 |
| 5 | 将适当的元素添加到 `AndroidManifest.xml` 文件中（如果尚未添加——这取决于我们使用的 Android 模板）。 |

表 C.1 使用 Google Play 服务的步骤

### 步骤 1（执行一次，如有需要可定期执行）：安装 Google Play 服务

选择 Tools，选择 Android，选择 SDK Manager（或点击 SDK Manager 图标），选择 SDK Tools 选项卡。查找 Google Play 服务。如果显示 `Not installed`，勾选其复选框，然后点击 Install `x` Packages（`x` 可能大于 1，具体取决于当前开发环境的版本）。接受许可条款并点击 Install。根据下载和安装的文件数量，这可能需要几秒到几分钟。在图 C.1 中，我们可以看到 Google Play 服务已安装。

### 步骤 2（执行一次，如有需要可定期执行）：如有必要，安装 Google API

我们所需的库可能已在步骤 1 中安装，也可能没有。例如，Google Maps Android API Version 2 是 Google Play Services SDK 的一部分。它可能已在步骤 1 中安装（默认可能已勾选，并与 Google Play 服务一同安装）。如果没有，我们必须安装它才能使用地图。

重新打开 SDK Manager（选择 Tools，选择 Android，选择 SDK Manager）。选择 Android SDK，然后选择 SDK Platforms 选项卡。选择最新的 Android 目录（作者撰写本文时为 Android 6.0 API 23），然后点击面板右下角的 Show Package Details 按钮。

在图 C.2 中，我们可以看到 Google API 已安装，但有可用更新。如果 Google API 显示 `Not installed`，我们需要选择它，然后点击 Install packages。如果有可用更新，我们应该更新。我们也可以通过从 Help 菜单中选择 Check for Update... 并按照指示进行更新。这可能需要几分钟。

![](img/9781284093650_APPC_FIGF01.jpg)

图 C.1 安装 Google Play 服务之前的 Android SDK 管理器

![](img/9781284093650_APPC_FIGF02.jpg)

图 C.2 Android SDK 管理器：Google API 已安装，且有可用更新

### 步骤 3（每个项目执行一次）：使 Google Play 服务库对应用可用

为此，我们需要修改 `build.gradle` 文件（有两个这样的文件，我们需要编辑模块对应的那个）。示例 C.1 显示了编辑后的文件。唯一的添加在第 27 行：我们需要包含适当版本的 Google Play 服务库。此示例显示的是版本 9.4.0。

每当我们修改 gradle 文件时，都应该同步项目。我们可以通过点击同步图标来完成。图 C.3 显示了同步图标。完成此步骤后，项目应能正确编译。

请注意，如果我们在创建新项目时使用现有的 Android 模板（例如 Google Maps Activity 模板），则 `build.gradle` 文件已包含第 27 行。

### 步骤 4（仅执行一次）：为了使用 Google 地图，从 Google 获取密钥

要从 Google 获取可用于开发的密钥，我们需要执行以下操作：

1. 获取调试证书指纹。
2. 在 Google APIs Console 中注册一个项目，并将 Maps API 添加为该项目的服务。
3. 请求并获取密钥。

![](img/App_C_exa01.jpg)

示例 C.1 编辑后的 `build.gradle`（Module: app）文件

![](img/9781284093650_APPC_FIGF03.jpg)

图 C.3 同步图标

当我们要将应用发布到 Google Play 时，需要获取发布证书指纹而不是调试证书指纹，过程类似。但为此，我们需要成为 Google Play 的注册开发者。

> 要获取调试证书指纹，请在命令行中执行以下操作：
>
> 对于 Linux 或 Unix 系统：
>
> ```bash
> keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android
> ```
>
> 对于 Windows 系统：
>
> ```bash
> keytool -list -v -keystore "C:\Users\your_user_name\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android
> ```
>
> 对于作者的计算机，命令为：
>
> ```bash
> keytool -list -v -keystore "C:\Users\Herve\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android
> ```

如果系统无法识别 `keytool` 命令，我们可以将其所在目录添加到路径中，或者从 `keytool` 所在目录内运行该命令。`keytool` 的可执行文件 `keytool.exe` 应位于 Java jdk 目录的 `bin` 目录内。在作者的计算机上，`keytool.exe` 位于`C:\Program Files\Java\jdk1.8.0_60\bin`目录中。

在 Windows 中，我们应该会看到类似图 C.4 所示的输出（注意作者已将证书指纹和密钥标识符替换为随机值）。指纹是 SHA1 后面出现的由冒号分隔的 20 个两位十六进制数字序列。

![](img/9781284093650_APPC_FIGF04.jpg)

图 C.4 运行 `keytool` 时的可能输出

指纹证书是唯一的，并提供了一种识别应用的方法。这使得 Google 能够在 Google Play 中跟踪应用，以及跟踪我们的应用对地图资源的使用情况。

现在，我们需要前往 Google APIs Console 注册一个项目。在撰写本文时，URL 为：

```text
https://console.developers.google.com/
```

如果我们已经注册了一个项目，该项目会显示在网页上。否则，点击 Create project。为我们的项目输入一个名称，然后点击 Create。接着，选择 Use Google APIs。

在可用服务列表中，找到 Google Maps Android API，如图 C.5 所示，然后点击它。接下来，点击 Enable API，如图 C.6 所示。此时，除非我们之前已经做过，否则系统会要求我们输入凭据。

![](img/9781284093650_APPC_FIGF05.jpg)

图 C.5 在 Google Play 服务中查找 Google Maps Android API

![](img/9781284093650_APPC_FIGF06.jpg)

图 C.6 启用 Google Maps Android API

![](img/9781284093650_APPC_FIGF07.jpg)

图 C.7 选择 API Manager

接下来，我们需要获取一个密钥。在左上角，点击 Google Developers Console 旁边的三条水平线。从菜单中选择 API Manager（见图 C.7）。然后选择 Credentials。从 New Credentials 菜单中，选择 API key（见图 C.8），然后选择 Android key。

此时，我们应该输入应用的包名以及图 C.4 中的 SHA-1 指纹，如图 C.9 所示。注意，我们在图中隐藏了作者的指纹。然后点击 Create，密钥就会显示出来。

密钥取决于指纹证书和应用包，因此我们建议为每个应用获取不同的密钥，但这不是必须的。

### 步骤 5（每个项目执行一次）：将适当的权限添加到 `AndroidManifest.xml` 文件中

根据应用的不同，我们需要按如下方式编辑 `AndroidManifest.xml` 文件：

- ▸ 使用 `permission` 元素列出权限。
- ▸ 使用 `uses-permission` 元素列出使用权限。

![](img/9781284093650_APPC_FIGF08.jpg)

图 C.8 从“新凭据”菜单中选择 API 密钥

![](img/9781284093650_APPC_FIGF09.jpg)

图 C.9 输入包名和 SHA-1 指纹



* ▸ 使用`uses-feature`元素列出使用的功能。
* ▸ 如果应用使用 Google Maps，则使用`meta-data`元素指定访问地图数据的密钥名称和值。
* ▸ 如果应用使用 Google Maps，则使用`uses-library`元素列出 Google Maps 库。

如果我们使用 Google Maps Activity 模板，其中一些内容可能已自动包含在`AndroidManifest.xml`中。

## 附录 D：AsyncTask 类

![](img/chapopener.jpg)

章节开篇图片：© Fon_nongkran/Shutterstock

`Thread`是在现有进程内执行的一段代码序列。现有进程通常称为主线程。对于 Android 应用，它也称为用户界面线程。同一进程内可以执行多个线程，并且线程可以共享资源（如内存）。

当我们启动应用时，代码在主线程中执行。有时，我们需要启动另一个线程。例如，我们可能需要从远程位置检索数据。此外，我们可能需要该其他线程在我们使用其数据并将其放入 GUI 组件之前完成。`android.os`包中的`AsyncTask`类允许我们执行后台操作，然后访问主线程以传达其结果。它旨在执行持续时间几秒或更短的短任务，不应用于启动长时间运行的线程。`AsyncTask`是`abstract`的，因此我们必须子类化它并实例化子类的对象才能使用它。

`AsyncTask`类使用了三个泛型类型，我们在扩展它时必须指定这些类型。子类头部的语法如下：

```java
AccessModifier ClassName extends AsyncTask<Params, Progress, Result>
```

其中`Params`、`Progress`和`Result`是实际类名的占位符，含义如下：

* ▸ `Params`是当我们调用`AsyncTask`的`execute`方法时传递给它的数组的数据类型。
* ▸ `Progress`是任务在后台执行时用于进度单位的数据类型。如果我们选择报告进度，该数据类型通常是`Integer`或`Long`。
* ▸ `Result`是任务执行后返回的值的数据类型。

我们可能对使用其中某些类型不感兴趣。如果对某个类型不感兴趣，则使用`Void`。例如，假设我们的类名为`TestTask`，并且我们将一个`Integers`数组作为`execute`方法的参数传递。再假设我们不关心报告进度，并且任务返回一个`String`。那么，我们使用以下类头部：

`public TestTask extends AsyncTask<Integer, Void, String>`

为了使用`AsyncTask`类启动任务，我们执行以下操作：

* ▸ 创建`AsyncTask`的子类。
* ▸ 声明并实例化该子类的对象。
* ▸ 使用该对象调用`execute`方法以启动任务。

`execute`方法是`public`和`final`的。`AsyncTask`包含一些可以由子类重写的`protected`方法。表 D.1 列出了`AsyncTask`类的一些方法。如前所述，`Params`、`Progress`和`Result`是实际类名的占位符。

参数列表中数据类型后的三个点语法表示该方法接受可变数量的参数，也称为可变参数。可变参数必须位于参数列表的最后一个参数位置。使用可变数量的参数的方法头部语法如下：

`AccessModifyer returnType methodName( someParameterList, DataType... variableNames )`

| 方法 | 描述 |
| --- | --- |
| `AsyncTask execute( Params... params )` | `Public`和`final`；`params`表示类型为`Params`（一个泛型类型）的值数组；返回此`AsyncTask`实例。 |
| `void onPreExecute( )` | `Protected`。在我们调用`execute`之后、`doInBackground`开始之前自动调用。 |
| `Result doInBackground( Params... params )` | `Protected`。我们需要重写的`Abstract`方法以执行任务；`params`是我们在调用`execute`时传递给它的参数。 |
| `void publishProgress( Progress... values )` | `Protected`和`final`。调用该方法会触发对`onProgressUpdate`的调用。 |
| `void onProgressUpdate( Progress... values )` | `Protected`。如果我们调用`publishProgress`，则自动调用。 |
| `void onPostExecute( Result result )` | `Protected`。在`doInBackground`完成后自动调用；`result`是`doInBackground`返回的值。 |

表 D.1 `AsyncTask`类的选定方法

注意，数据类型和三个点之间没有空格。`execute`、`doInBackground`、`publishProgress`和`onProgressUpdate`方法接受可变数量的参数。

例如，假设我们定义了一个名为`Item`的类，我们可以使用以下方法头部重写`doInBackground`方法：

`protected ArrayList<Item> doInBackground( Integer... numbers )`

当调用接受可变数量参数的方法时，我们可以不传递参数、传递单个参数、多个参数或一个参数数组。例如，要调用一个具有上述方法头部的`doInBackground`方法（使用名为`task`的`AsyncTask`引用），我们可以通过四种不同的方式实现：

```java
// #1：不传递参数
task.execute( );
// #2：仅传递 1 个参数
task.execute( 7 );
// #3：传递多个参数
task.execute( 6, 8, 15 );
// #4：传递一个参数数组
int [ ] values = { 10, 20, 30, 40, 50 };
task.execute( values );
```

当我们调用`execute`方法时，`AsyncTask`类的以下方法按此顺序执行：`onPreExecute`、`doInBackground`和`onPostExecute`。

在任务执行之前，如果我们想执行一些初始化，可以将该代码放在`onPreExecute`方法中。我们将要执行的任务代码放在`doInBackground`方法中。该方法是`abstract`的，必须重写。自动传递给`doInBackground`方法的参数与我们在调用`execute`时传递给它的参数相同。在`doInBackground`内部，当任务执行时，如果我们想向主线程报告进度，可以调用`publishProgress`方法。这反过来会触发对`onProgressUpdate`方法的调用，我们可以重写该方法：例如，我们可以在用户界面线程中更新进度条。当`doInBackground`方法执行完毕时，`onPostExecute`方法会自动调用。我们可以重写它以使用刚刚完成的任务的结果更新用户界面。自动传递给`onPostExecute`方法的参数是`doInBackground`方法返回的值。

总结数据流：我们传递给`execute`的参数会自动传递给`doInBackground`，而`doInBackground`的返回值会自动作为`onPostExecute`的参数传递。

在`onPostExecute`方法内部，我们很可能想要更新用户界面线程的活动。基本上有两种方法可以做到这一点：

* ▸ 我们可以将`AsyncTask`的子类编码为执行该任务的活动类的`private`内部类。在这种情况下，我们可以从`onPostExecute`方法内部调用活动类的方法。
* ▸ 我们可以将`AsyncTask`的子类编写为一个独立的`public`类。在这种情况下，我们需要一个对执行任务的 Activity 类的引用，以便能够从`onPostExecute`方法内部调用该 Activity 类的方法。

我们展示第二种解决方案的示例（即，我们编写一个独立的`AsyncTask`的`public`子类）。它说明了如何将一个`Activity`引用从一个类传递到另一个类。我们执行以下步骤：

* ▸ 我们创建`TestTask`，它是`AsyncTask`的一个子类。
* ▸ 我们重写`doInBackground`方法，使其执行我们感兴趣的任务。
* ▸ 在`TestTask`内部，我们包含一个实例变量，该变量是对启动任务的`Activity`的引用。这使我们能够从`TestTask`调用`Activity`类的方法。
* ▸ 我们重写`onPostExecute`方法，并调用`Activity`类的一个或多个方法，以使用刚刚完成的任务的结果更新 Activity。
* ▸ 在`Activity`类内部，我们创建并实例化一个`TestTask`对象。
* ▸ 我们将对此`Activity`的引用传递给`TestTask`对象。
* ▸ 我们调用`AsyncTask`的`execute`方法，传入适当的输入数据（例如，如果需要从远程网站检索数据，则传入 URL），以开始执行任务。

我们现在构建一个非常简单的应用程序，以说明如何使用`AsyncTask`类。我们使用 Empty Activity 模板。示例 D.1 展示了`TestTask`类。在类头（第 6 行）中，我们将`Integer`指定为`Params`数据类型，将`Void`指定为`Progress`数据类型（我们在此不关心报告进度），并将`String`指定为`Result`数据类型。

![](img/App_D_exa01.jpg)

示例 D.1 `TestTask`类

在第 7 行，我们声明了`activity`实例变量，它是对`MainActivity`的引用。构造函数（第 9–12 行）接受一个`MainActivity`参数并将其赋值给`activity`。当我们从`MainActivity`类调用`TestTask`构造函数时，我们将`this`作为参数传递。

我们在第 14–17 行重写了`doInBackground`方法。方法头指定它返回一个`String`（`Result`数据类型），并接受`Integers`作为参数（`Params`数据类型）。在这个简单的示例中，这些参数从未被使用，因此无关紧要。

我们在第 19–22 行重写了`onPostExecute`方法。当`doInBackground`方法执行完毕后自动调用该方法时，其参数`message`的值是`doInBackground`返回的`String`。我们使用`activity`实例变量调用`MainActivity`类的`updateView`方法，并在第 21 行传递`message`。我们需要添加到`MainActivity`类中的`updateView`方法，预期会根据其参数的值更新`View`。

在所有方法内部，我们添加了一条输出语句（第 10、15、20 行），以便能够追踪所有方法被调用的顺序。

示例 D.2 展示了`MainActivity`类。在第 16 行，我们声明并实例化了一个`TestTask`对象，并在第 18 行调用`execute`方法，传递`1`。在这个简单的示例中，我们传递的参数从未被使用，因此无关紧要。然而，其数据类型必须与`TestTask`类的`doInBackground`方法的参数数据类型匹配。由于`execute`方法接受可变数量的参数，我们可以传递 0 个、1 个或多个参数。我们本可以传递一个只包含一个元素`1`的`Integers`数组，如下所示：

```java
task.execute( new Integer[ ] { 1 } );
```

![](img/App_D_exa02.jpg)

示例 D.2 `MainActivity`类

在第 22–26 行，我们编写了`updateView`方法。此时，它向 Logcat 输出一些反馈，并在第 25 行更新`TextView`中的文本。

请注意，当我们使用`AsyncTask`时，代码的顺序很重要。在第 18 行调用`execute`之后，如果第 18 行之后还有语句，执行将继续在`onCreate`方法内进行。在这种情况下，这些语句与在`TestTask`类内部执行的语句之间将存在交错执行。如果我们试图在调用`execute`之后立即检索任务生成的一个或多个值（即使任务生成的值位于`TestTask`类内部，也很容易将它们写成另一个类的`public` `static`数据，并从`MainActivity`类读取该`public` `static`数据），在本示例中即在`onCreate`方法内部，那么该值或这些值很可能是`null`。处理任务生成值的正确方法是在`onPostExecute`方法内部进行。

示例 D.3 展示了`activity_main.xml`文件。我们在第 16 行为`TextView`添加了一个 id，并在第 17 行将字体大小设置为 32，以便在屏幕上看得更清楚。

示例 D.3 `activity_main.xml`文件

![](img/App_D_exa03.jpg)

图 D.1 展示了运行时的 Logcat 输出，特别是执行顺序。它显示`MainActivity`类第 19 行的 Logcat 输出语句在`TestTask`类的`doInBackground`方法执行之前执行。这个非常简单的模拟证实了处理任务生成值的正确方法是在`onPostExecute`方法内部进行。图 D.2 展示了`TextView`中的文本已从`Hello World!`更改为`Changed using AsyncTask`。

![](img/9781284093650_APPD_FIGF01.jpg)

图 D.1 示例 D.2 的 Logcat 输出

![](img/9781284093650_APPD_FIGF02.jpg)

图 D.2 在模拟器中运行的应用程序

## 索引

注意：页码后跟 b、f 或 t 分别表示方框、图形或表格中的内容。

### A

* `AbsoluteLayout`类，256
* `abstract`类，155，314，354
* 操作栏，高度
  * 检索，643–648
* `actionBarHeight`变量，263
* 活动（Activities）
  * 生命周期，145–150
  * 输出和状态，用户与应用交互时的堆栈，149t
  * 在活动之间共享数据，150–154
  * 活动之间的转换，155–161
* `Activity`类，141，223，224，227，251，252，279，280，303，306，326，345，346，436，515
  * 常量，574t
  * `getCurrentFocus`方法，375
  * `getFragmentManager`方法，354t
  * 生命周期方法，145b，347f
  * 方法，142t
  * `onActivityResult`方法，437，440，466，466t
  * `onConfigurationChanged`方法，227，227t
  * `onTouchEvent`方法，285
* `overridePendingTransition`方法，159t
* `startActivityForResult`方法，466, 466t
* 有用的方法，71t
* `activity`元素，227, 232, 242, 302
* `android:configChanges`属性，227, 227t
* `activity_data.xml`文件，137–139b
* `activity_insert.xml`文件，182–183b
* `activity_main_landscape.xml`文件，229, 230b
* `activity_main.xml`文件，8, 11, 12b, 40, 44, 69, 70, 132, 133–134b, 174, 175b, 229, 233b, 479, 491, 540, 600, 652, 653b
  * `button`元素，70b
  * 加密应用
    * 版本 1，625–626b
    * 版本 3，634–636b
  * GPS 应用
    * 版本 1，445b
    * 版本 2，448b
  * 猜词游戏应用
    * 版本 0，342b
    * 版本 1，348b
  * 照片应用
    * 版本 0，468b
    * 版本 2，480–481b
    * 版本 3，487–488b
    * 版本 4，492–493b
    * 版本 5，500b
  * 用于竖屏方向，230b
  * 显示地图应用



* 版本 3，413–414、414b
* 版本 4，415b

* 秒表应用
  * 版本 0，590–591b
  * 版本 4，608–609b

* 小费计算器应用
  * 版本 0，49b
  * 版本 1，58–61b
  * 版本 2，67–68b
  * 版本 4，75b

* 网页内容应用
  * 版本 3，527b

* `activity_maps.xml` 文件，393b
* `AdapterView` 类，532
* `add` 方法，365
  * `FragmentTransaction` 类的，365
* `addApi` 方法，436
* `addConnectionCallbacks`，436
* `addOnConnectionFailed Listener` 接口，436
* `Address` 类，409t
* `addToBackStack` 方法，354
* `addView` 方法，263
* `AdFragment` 类，609–610b、611–612b
* `AdRequest.Builder` 类，602、602t
* `AdSize` 类，横幅广告，600、600t
* 高级加密标准（AES）模型，619
* 广告，599
* `AdView` 类，600–601、601t、610、611t、612
* `AESEncryption` 类，621–622b、630、632
* `afterTextChanged` 方法，76
* 警告对话框，110–115
* `AlertDialog.Builder` 类，110、111t
* Android 应用程序包（APK），34
* Android 应用，2
  * 开发环境，3
* Android 开发框架，298
* Android 开发工具包（ADK），47、62–63、64
* Android 设备，在其上测试应用，28–30
* Android 框架，235
* Android 市场，2
* Android 操作系统，2
* Android 手机，2
* Android 标准开发工具包（Android SDK），3、655、656
* Android Studio，3、18、27
  * 编译器错误标记，26b
* Android Studio 环境，181
* Android 虚拟设备（AVD）管理器，18–21
* `android.appwidget` 包，540、540t
* `android:background` XML，55、65
* `android:configChanges` 属性，227、228、242
  * `activity` 元素的，227、227t
  * `onConfigurationChanged` 方法，228b
* `android.content.pm` 包，386
* `android.content.res` 包，222
* `android.database.sqlite` 包，188、189t
* `android.graphics` 包，263、298、298t、471–472、472t
* `android:imeOptions` 属性，353
* `android:inputType`，73
* `android:layout_weight` XML 属性
  * `LinearLayout` 的，343
* `android:layout_width` 属性，343
* `android.location` 包，440
* `AndroidManifest.xml` 文件，7、30、31b、44、45b、144b、186–187b、198b、203b、222、227、232、242、261、302、352、393–394b、412–413b、418b、440、541b、570–571b、605–606b
* `android.media` 包，325
* `android:orientation` 属性，233
* `android.os` 包，522
* `android:screen Orientation`，222
* `android:textColor` XML，55、56
* `android:theme`，69
* `android.view` 包，287
* 动画，155
  * XML 元素及对应类，156t
* `Animation` 类，选定的 XML 属性，157t
* API 级别 11、340
* 应用微件宿主，540
* 应用微件，540
  * 外边距和内边距，550f
  * 模型-视图-控制器类，569t、578t
  * 每维度的单元格数与尺寸，542、543t
  * 在平板电脑中运行，551f、554f、556f、569f、578f
  * 方法调用顺序，577t
  * 视图与布局管理器，543、544t
* `AppBarLayout`，174
* `AppCompatActivity`，285、306
* Apple，2
* `AppTheme`，69
* `AppWidgetManager` 类，542、545、546t、571t、580t
* `AppWidgetProvider` 类，544、545t
* `AppWidgetProviderInfo` 类，542、543t、579t
* `ArrayAdapter` 类，529–530
* 非对称加密，618
* `AsyncTask` 类，522、523t
  * `Params`、`Progress` 和 `Result`，522
  * 其 `ParseTask` 类，522

### B

* `BackgroundFragment` 类，365b
* `beforeTextChanged` 方法，76
* `beginTransaction` 方法，354
* BIOS 菜单，18
* `Bitmap` 类，303、318、319、472–473、473t、496
  * 其 `getByteCount` 方法，496、497t
  * 其方法，300、301t
* `Bitmap` 引用，306
* `BitmapFactory` 类，其方法，300、301t
* `BitmapGrayer` 类，473–475、485–486
* BlackBerry，2
* `blue_thumb.xml` 文件，479
* `boolean` 状态变量，241
* `View` 类的 `bringToFront` 方法，265、265t
* `build` 方法
  * `SoundPool.Builder` 类的 `build` 方法，默认构造函数与，326、326t
* `build.gradle` (Module:app) 文件，325、434、599、658
* `buildGuiByCode` 方法，93b、95、258、261、276
* `Bundle` 类，345、421、421t、467、467t
* `Button` 类，46、53、69、73、75、94、237
* `ButtonGridAndTextView` 类，116、117–118b、119
* `ButtonHandler` 类，97、213
* `ButtonStyle`，66、350

### C

* `calculate` 方法，70、76
* 回调方法，251
* `Callbacks` 接口，367、369、370
* 相机应用（照片应用），在平板电脑中运行
  * 版本 0，470、471f
  * 版本 1，477、477f
  * 版本 2，485f
  * 版本 3，490f
  * 版本 4，498、499f
  * 版本 5，502–503、502f、503f
* `CameraUpdateFactory` 类，396、398t
* `cancel` 方法，314
* `Candy` 类，189–190b
* 糖果店应用
  * 版本 0，174–180
  * 版本 1，180–188
  * 版本 2，188–196
  * 版本 3，197–202
* 版本 4，202–207
* 版本 5，208–213
* `CandyButton` 类，208、213
* `Canvas` 类，305、306
  * 方法，299、300t
* 收银机，运行，208–213
* `CenteredTextStyle`，64、65、66
* `checkDimensions` 方法，241、242
* `Chronometer` 类，589
  * `elapsedRealtime` 方法，593、596
  * `setBase` 方法，593、594t
  * `start` 方法，593、594t、595
  * `stop` 方法，593、594t、595
* `CircleOptions` 类，400、401t
* `Cities` 类，404
  * 显示地图应用，版本 2，405b
* 类头
  * `Hangman` 类的，371b
  * `MainActivity` 类的，370b
* `ClockUtility` 类，秒表应用，596–597
* `Color` 类，263
* `colors.xml` 文件，15b、16、56、57b、349b、627b
* `columnSpec`，105
* `com.google.android.gms.ads` 包，598–599、599t
* `com.google.android.gms.maps` 包，395t
* `com.google.android.gms.maps.model` 包，395t
* `commit` 方法，354
* `compress` 方法，照片应用，496–497、497t
* `Configuration` 类，222–226
* `Configuration config` 引用，224、224–225b
* `Configuration` 引用，223
* `ConnectionCallbacks` 接口，435、436t、437
* `ConnectionResult` 方法，437–438、438t
  * `hasResolution` 方法，437
  * `onConnectionFailed` 方法，437
  * `startResolutionForResult` 方法，437
* 常量值
  * `Configuration` 类的，与设备屏幕尺寸相关，223t
  * `Configuration` 类的方向字段的，223t
* `content`，253
* `content_main.xml` 文件，174、209b
* `ContentHandler` 接口，512t
* `Context` 类，223、386、386t
  * `getSystemService` 方法，375t
* `ContextThemeWrapper` 类，644、645t
* `ContextWrapper` 类，643、644t
* 控制器，40、115
* `CoordinatorLayout`，174
* CSS（层叠样式表），63
* `currentIncompleteWord` 方法，353、371
* `currentSolution` 方法，277
* `Cursor` 类，191t
* 自定义视图（创建），317

### D

* 数据
  * 删除，197–202
  * 处理持久化，161–166
  * 更新，202–207
* `DataActivity` 类，142、145、148、159、163
  * `goBack` 方法，160b
  * 带有生命周期方法，147–148b
  * 抵押贷款计算器应用的
    * 版本 1，143b
    * 版本 2，152–153b
  * `updateMortgageObject` 方法，165b
* `DatabaseManager`，210、190、191–193b
* 调试
  * 使用 Logcat 调试应用，24–27
* 调试器
  * 断点，27–28
  * 使用，27–28
* `DefaultHandler` 类，512–513、513t
  * `ContentHandler` 接口，512t
  * `DTDHandler` 接口，512t
  * `EntityResolver` 接口，512t
  * `ErrorHandler` 接口，512t
* 防御性编程，73
* `DeleteActivity` 类，197、198、199–200b
* `DELTA_TIME` 常量，318
* `density` 字段，263
* 设备方向，管理，222
  * `Configuration` 类，222–226
  * 设备旋转事件，捕获，227–229
  * 一个布局 XML 文件
    * 两种方向，233–236
    * 每种方向一个，229–232
    * 仅通过代码控制方向，236–243
* 设备旋转事件，捕获，227–229
* `DialogFragment`，341
* `DialogInterface.OnClickListener`，111、115
* `dimens.xml` 文件，13b、132b
* `Directions` 类，418–419
* `disableListener` 方法，272、275
* `displayList` 方法，527
* `DisplayMetrics` 类，263、644、644t
* 距离与时间到达目的地模型，GPS 应用，445–447
  * `distanceToDestination` 方法，447
  * `timeToDestination` 方法，447
  * `TravelManager` 类，用于，445–447
* `distanceToDestination` 方法，GPS 应用，447
* 文档对象模型（DOM）解析器，510–511
* 文档类型声明（DTD）文档，510
* DOM 解析器。参见文档对象模型（DOM）解析器
* `Done` 键，353
* 双击，检测，284–288
* `DoubleTapHandler` 对象，287
* `DOWN` 动作方法，255、258、270、283
* `drawable` 目录，300、302
* `drawArc` 方法，305
* `drawBitmap` 方法，306
* `drawCircle` 方法，305
* 绘制位图，302
* 绘制形状，302
* `DTDHandler` 接口，512t
* 打鸭子应用
  * 版本 0，302–313
  * 版本 1，313–319
  * 版本 2，320–324
  * 版本 3，324–332
* `duckHit` 方法，313
* `duckRect`，303
* `duckShot`，313
* `DynamicFontSizing` 类，289b
* `DynamicSizing` 类，289、649、650、651

### E

* `EditText`，44、46、48、50、53、64、66、70、71、73、75、78、181、371
* `elapsedRealtime` 方法，593、596、598t
* 元素内容，10
* 电子邮件（发送），499
* 空活动模板，251、302、341、434
* 模拟器，在内部运行应用，18–23
  * 加密应用
    * 版本 1，629f
    * 版本 3，638f
  * GPS 应用，版本 2，453f
  * 横屏方向，22、23f
  * 竖屏方向，22、22f
  * 显示地图应用
    * 版本 0，384f
    * 版本 1，400f
    * 版本 2，403f
  * 测试应用，654f
  * 井字游戏应用，版本 0，96f
  * 关于的有用信息，23t
  * 垂直和水平位置，232f、236f
  * 网页内容应用
    * 版本 3，530f



* 版本 4，533f

    * 在模拟器中运行的小部件，547–549f

* `enableListener` 方法，266，268

* 加密应用

    * 非对称

        * 将 RSA 添加到模型，版本 2，630–634

    * 修改视图，版本 3，634–638

    * 对称

        * 添加视图，版本 1，625–629

        * AES 模型，版本 0，619–625

* `EntityResolver` 接口，512t

* `Environment` 类，495–496

* `ErrorHandler` 接口，512t

* 事件处理，96–100

* `Event` 参数，252，254

* 事件，40，69

* 扩展 `View` 类，317

* `extends`，314

* 可扩展标记语言（XML），8，10

    * 文档，510–511

        * 解析为列表，518–521

        * 和内容应用，509–533

        * 使用 DOM 和 SAX 解析器解析，510–517

        * 转换为项目列表，511，511f

        * 解析远程 XML 文档，521–526

        * 在 `ListView` 中显示结果，526–530

        * 转换为树，511，511f

        * 在应用内打开网页浏览器，531–533

    * 非空 XML 元素，10

    * 标签命名规则，11

* 外部存储，照片应用，490–491，491t

### F

* `fade_in_and_scale.xml` 文件，158b，161f

* `fillGui` 方法，263，265，276，290

* `findFragmentById` 方法，356

* `findFragmentByTag` 方法，365

* `findViewById` 方法，152、352、357

* `fireBullet` 方法，320

* `FloatingActionButton`，174

* `for` 循环，261

* `Fragment` 类，341、346

    * `getActivity` 和 `getView`

        * 的方法，357t

    * 的生命周期方法，344、347f

* `fragment_ad.xml` 文件，607b

* `fragment_game_control.xml` 文件

    * Hangman 应用

        * 版本 0，343b

        * 版本 1，349b

* `fragment_game_state.xml` 文件，353b

* `FragmentManager abstract` 类，353

* `FragmentManager` 类，353

    * 的方法，354t

* `FragmentManager` 引用，356

* 片段（fragments），338、340–341

* `FragmentTransaction` 类，354

    * `add` 方法，365

    * 的方法，355t

* `FragmentTransaction` 引用，356

* 帧动画（frame animation），155

* `FusedLocationProviderApi` 接口，440、442t、454t

    * `lastLocation` 方法，440

### G

* `Game` 类，309–313b

* `GameControlFragment` 类，342、345、346

    * Hangman 应用，版本 0，345b

* `GameResultFragment` 类，359

    * Hangman 应用

        * 版本 3，361b

        * 版本 4，364b

* `GameStateFragment` 类，357、369、370

    * Hangman 应用

        * 版本 2，358b

        * 版本 6，367–368b

        * 版本 7，372–373b

* `GameTimerTask` 类，314、316、319、322、327

    * 打鸭子（Duck Hunting）应用

        * 版本 1，316b

        * 版本 2，323–324b

        * 版本 3，330b

    * `run` 方法，315、330b

* `GameView` 类，303、308、316、320、322

    * 打鸭子（Duck Hunting）应用

        * 版本 0，304

        * 版本 1，317–318

        * 版本 2，323

        * 版本 3，331

* `GameView` 对象，303

* `Geocoder` 类，408、409t、452、452t

    * `getFromLocationName` 方法，452

* 地理编码（geocoding），408、409t

* 手势（gesture），277–284

* `GestureDetector` 类，278、279、279t、280、285、287、320

* `GestureDetector.OnDoubleTapListener`，278、278t、279、280、282、284

* `GestureDetector.OnGestureListener`，278、278t、279、280、284、287

* `GestureDetector.SimpleOnGestureListener` 类，284、285、287、320

* `getAction` 方法，252、253t

* `getActivity` 方法，357

    * `Fragment` 类的方法，357t

* `getConfiguration` 方法，223、223t

* `getContext` 方法，331

* `getCurrentFocus` 方法，`Activity` 类的方法，375

* `PreferenceManager` 类的 `getDefaultSharedPreference` 方法，163b

* `getElapsedRealtimeNanos` 方法，456

* `getEncoded` 方法，622、622t

* `getExternalFilesDir` 方法，495、495t

* `getFragmentManager` 方法，353、355

    * `Activity` 类的方法，354t

* `getGame` 方法，357、370

* `getGuessesLeft` 方法，351

* `getLocationInWindow` 方法，256

* `getMeasuredHeight` 方法，237

    * `view` 类的方法，237、237t

* `getNumberOfParts`，259

* `getRawX` 方法，256、320

* `getRawY` 方法，256、320

* `getResources` 方法，223、223t、643–644、643t

* `getSystemService` 方法，`Context` 类的方法，375t

* `getText` 方法，71、277

* `getView` 方法，`Fragment` 类的方法，357t

* `getX` 方法，256、320

* `getY` 方法，256、320

* `goBack` 方法，154

    * 在 `DataActivity` 类中，160b

* Google，2

* Google Maps

    * 活动模板，391–400、391–392f

* `android API`，启用，660f

* 来自“新凭据”菜单的 `API key`，662f

* `API manager`，选择，661f

* 添加适当的权限，661–663

* 在 Google Play 服务中查找，660f

* 来自 Google 的密钥，657–661，659f

* Google Play 服务，2–3

    * 访问，434–440

    * Google API，安装，656–657，657f

    * 安装，656，656f

    * 应用可用的库，657，658f

    * 使用步骤，655t

* `google_maps_api.xml` 文件，392–393b

* `GoogleApiClient abstract` 类，435

* `GoogleApiClient` 类，437，437t

* `GoogleApiClient.Builder` 类，435，435t

* `GoogleMap` 类，396，397t

    * `OnMapReadyCallback` 接口，396t

    * `SupportMapFragment` 类，396t

* GPS（全球定位系统）应用，434–459

    * 版本 0，434–440

    * 版本 1，440–445

    * 版本 2，447–453

    * 版本 3，453–458

    * Gradle 构建系统，34

* 图形用户界面（GUI），222，359，447，588

    * 组件，41–44，237

        * 类和，43t

        * 所选组件的继承层次结构，44f

        * XML 属性和，53–62

* 图形，298–301

* `green_thumb.xml` 文件，479

* `GridLayout` 类，94，96，105，106t，116

    * 构造函数和方法，95t

* `GridLayout.LayoutParams` 对象，105，106t，107

* `GridLayout.Spec` 类，105，106

* `guessesAllowed` 实例变量，338

* `guessesLeft` 实例变量，338

* GUI。参见图形用户界面

### H

* 处理器，75，76

* 处理事件，40，69

* 处理触摸事件，320–324

* Hangman 应用

    * 添加 GUI 组件、样式、字符串和颜色，版本 1，346–352

    * 片段与其活动之间的通信，版本 4，362–364

    * 片段，定义和添加

        * 版本 0，341–346

        * 版本 2，352–359

        * 版本 3，359–362

    * GUI 改进，版本 7，371–376

    * 使用不可见片段，版本 5，365–367

    * 制作可复用片段，版本 6，367–371

* `Hangman` 类，338，339–340b

    * 类的头部，Hangman 应用，版本 6，371b

* `Hangman` 构造函数，340

* HangmanV0LifeCycle 应用，347f

* `height` 参数，263，303

* HelloAndroid，3

    * 模拟器运行，22f

    * GUI 预览，8

    * `MainActivity` 类，16–18，17b

    * 骨架应用，3–8

    * XML 文件，8–16

* `hideSoftInputFromWindow` 方法，374，375，376t

    * 属于 `InputMethodManager` 类，375t

* `hi.png` 文件，31–32

* `horizontalDimensionsSet`，241

* 超文本标记语言（HTML），8

### I

* `IBinder` 引用，374

* 图标项，180–188

* `ImageView` 类，467–468，467t，469，469t

* `indexesGuessed` 数组，338，340

* `indexOfTextView` 方法，266，270，285，287

* `inflate` 方法，345

    * 属于 `LayoutInflater` 类，345

* 膨胀 XML，18

* 继承层次结构

    * 对于 `Fragment`，341

    * 对于 `SeekBar` 类，478f

    * 对于选定的 GUI 组件，44f

    * 显示布局类，92f

    * 对于 `TableLayout`，132

    * 对于 `TableRow` 元素，132

* 内部类，102–104

* 输入法编辑器，353

* `InputMethodManager` 类，375，376t

    * 其 `hideSoftInputFromWindow` 方法，375t

* `InputMethodManager` 引用，374

* `InputStyle`，64、65、66

* `InsertActivity` 类，185、194

    * 糖果店应用

        * 版本 1，185–186b

        * 版本 2，195b

* 实例变量，241

* `Instant Run`，22、23f

* 英特尔硬件加速执行管理器（HAXM），18

* `Intent` 类，141、389、389t、408t、467、467t、501t

    * 构造函数，142t

* 内部存储，照片应用，490–491、491t

* `intersects` 方法

    * 属于 `Rect` 类，313、313t

* `ints` 参数，256

* iOS，2

* `isLayoutSizeAtLeast` 方法，223

* `Item` 类，518

### J

* Java 开发工具包（JDK），3

* `java` 目录，7

* JavaScript 对象表示法（JSON），558、559f

* `java.util` 包，314

* `javax.crypto` 包，619

    * `Cipher`，619、620t

    * `KeyGenerator`，619、620t

    * `SecretKey`，619、620t

* `JSONObject` 类，559、560t

### K

* `keyguard`，578–579

* `KeyPair` 类，631t

* `KeyPairGenerator` 类，631t

### L

* `labelHeight` 参数，263

* `LabelStyle`，64、66

* `landscape Strings`，229

* 启动器图标，用于应用，30–31

* 布局管理器类，47

* 布局参数，105–110

* 布局 XML 文件，236–237

* `LayoutInflater` 参数，345

* `LayoutParams` 类，47、102、103t、343

* `LayoutParams` 对象，256

* `leftMargin` 参数，258

* 生命周期方法

    * 属于 `activity` 类，347f

    * 属于 `fragment` 类，344、347f

* `LinearLayout`，233、241、342、343

    * `android:layout_weight` XML 属性，343

    * 占位符，592

* `LinearLayout.LayoutParams` 类，235

* `ListFragment`，341

* `ListView` 类，529–530

    * `setAdapter` 方法，530t

* `load` 方法，326

* `Location` 类，440、441t、457t

* `Location` 引用，440、442

* `LocationListener` 接口，453、454t

* `LocationRequest` 类，455、455t

    * 优先级常量，456t

* `LocationServices` 类，436、437t

* `Log` 类，24、24t、25

* Logcat 输出

    * 加密应用

        * 版本 0，624–625、624f

        * 版本 2，634f

    * GPS 应用

        * 版本 0，440

        * 版本 1，444、445f

        * 版本 3，456、458f

    * 秒表应用，603f

    * 网页内容应用

        * 版本 0，516、517f

        * 版本 1，520、521f

        * 版本 2，526f

* Logcat 选项卡，使用其调试应用，24–27

### M



- `MainActivity` 类，6、16–18、17b、25、40、70、73、100、111、142、145、148、159、163、174、229、234、252–254、261、306、318、320、327、346、355、357、359、367、369、370、434、440、447、456
  - 糖果店应用
    - 版本 0，178–179b
    - 版本 1，184–185b
    - 版本 3，197b
    - 版本 4，203b
    - 版本 5，210–212b
  - 打鸭子应用
    - 版本 0，307b
    - 版本 1，319b
    - 版本 2，321–322b
    - 版本 3，328–329b
- 编辑内容，将`activity_main`替换为`activity_data`，140b
- 加密应用
  - 版本 0，623–624b
  - 版本 1，628–629b
  - 版本 2，632–633b
  - 版本 3，636–637b
- GPS 应用
  - 版本 0，438–439b
  - 版本 1，442–444b
  - 版本 2，450–452b
  - 版本 3，457b
- 猜词游戏应用
  - 版本 1，351b
  - 版本 2，356b
  - 版本 3，360b
  - 版本 4，363b
  - 版本 5，366b
  - 版本 6，370b
  - 版本 7，376b
- HelloAndroid，版本 1，26b
- 包含生命周期方法，146–147b
- `MainActivity`类中的`modifyData`方法，159b
- 抵押贷款计算器应用
  - 版本 1，143b
  - 版本 2，151b
- `onCreate`方法，165b
- 照片应用
  - 版本 0，469–470b
  - 版本 1，475–476b
  - 版本 2，483–484b
  - 版本 3，488–489b
  - 版本 4，497–498b
  - 版本 5，499，500b
- `playHitSound`方法，330
- 拼图应用
  - 版本 0，264
  - 版本 1，266–267b
  - 版本 3，286b
- 显示地图应用
  - 版本 3，406，407–408b
  - 版本 4，416–417b
- 状态栏和操作栏高度，获取，646–647b
- 秒表应用
  - 版本 0，592b
  - 版本 1，594–595b
  - 版本 2，597–598b
  - 版本 3，604–605b
- 文本视图，设置字体大小，653b
- 井字游戏应用
  - 版本 0，93b
  - 版本 1，97–98b
  - 版本 2，101–102b
  - 版本 3，107–109b
  - 版本 4，112–114b
  - 版本 5，119–121b
- 小费计算器应用
  - 版本 3，71–72b
  - 版本 4，77–78b
- 触摸应用
  - 版本 0，254b
  - 版本 1，257–258b
  - 版本 2，281–282b
- 语音识别应用
  - 版本 0，387–388b
- 网页内容应用
  - 版本 0，515–516b
  - 版本 1，520–521b
  - 版本 2，525b
  - 版本 3，528–529b
  - 版本 4，531–532b
- `MainActivity.java`，内部生成的代码，175b
- `Manifest.permission`类，393，395t
- `MapsActivity`类
  - 版本 1，398–399b
  - 版本 2，402b
  - 版本 3，409–411b
  - 版本 5，421–423b
- 地图（显示），391
- `MarginLayoutParams`引用，242
- `MarkerOptions`类，398，400t
- `match_parent`值，45
- `MatchingUtility`类，419
- `MathRounding`类，485，486b
- `mCallbacks`实例变量，370
- `measure`方法，237
  - `view`类的`measure`方法，237，237t
- `MeasureSpec`类，650，651t
- `menu_main.xml`文件，176b，177b
  - 糖果店应用
    - 版本 1，181b
    - 版本 5，209
- `MenuItem`接口，176
  - 选中的常量，177t
  - 选中的 XML 属性和方法，176t
- 模型，40，41，88–91，259–261，308–313，338–340
- 模型-视图-控制器，287
  - 架构，40–41，88，338
- 修改后的`AndroidManifest.xml`文件，32，33b
- 修改后的`dimens.xml`文件，13b
- 修改后的 HelloAndroid 应用，224
- 修改后的`MainActivity`类，26b
- 修改后的`string.xml`文件，14b
- 修改后的`styles.xml`文件，15b
- `MainActivity`类中的`modifyData`方法，159b
- `modifyLayout`方法，229，234，237，241，242
- 抵押贷款计算器应用
  - 版本 0，131–135
  - 版本 1，140–145
  - 版本 2，150–154
  - 版本 3，155–161
  - 版本 4，161–166
- `Mortgage`类，128–129，129–130b
  - 其月度现金流，128t
  - 抵押贷款计算器应用，版本 4，164b
- `MotionEvent`，252，253t，254，282，320
- `MouseEvent`，320
- `MOVE`动作方法，255，256，270，283
- `moveDuck`方法，313
- `moveTextViewVertically`方法，270

### N

- 国家气象局（NWS），558
- `newConfig`参数，227
- Nexus 5 模拟器，242，242f，647–648f
- 非空 XML 元素，10
- `null`值，306
- `NullPointerException`，95，357
- `NUMBER_PARTS`，259

### O

- `onClick`方法，97，115
- `onConfigurationChanged`方法，227–229，228b，232，234，237，241，242
  - 属于`Activity`类，227，227t
- `OnConnectionFailedListener`接口，435，436t，437
- `onCreate`方法，17，227，229，232，234，241，253，263，266，320，351，355，365
- `onCreateOptionsMenu`方法，178
- `onCreateView`方法，345，359，361
- `onDetach`方法，370
- `OnDouble-TapListener`接口，287
- `onDoubleTap`方法，283
- `onDoubleTapEvent`方法，280，283–285，288，330
- `onDraw`方法，299，300，303，305，315，316，318，319，320，322，331
  - 属于`GameView`类，打鸭子应用版本 2，323
- 一个 XML 布局文件，233
  - 两种方向，233–236
  - 每种方向一个，229–232
- `onEditorAction`方法
  - 属于`TextView.`
    - `OnEditorActionListener`接口，371，371t
- `onError`方法，425–426
- `onFling`方法，280，283–284
- `OnItemClickListener`接口，532，533t
- `onLayout`方法，306
- `onLocationChanged`方法，456
- `onOptionsItemSelected`方法，178
- `onPause`方法，456
- `onScroll`方法，283，320
- `OnSeekBarChangeListener`接口，481–482，481t
- `onSingleTapConfirmed`方法，283，320
- `onSingleTapUp`方法，283
- `onStart`方法，361
- `onTextChanged`方法，76
- `onTouch`方法，251–254，256，258，265，266，270，271
- `onTouchEvent`方法，278–280，282，283，287，288，320
  - 属于`Activity`类，285
- `OnTouchListener`接口，253
- OpenGL，314
- `org.xml.sax`包，513
- `org.xml.sax.helpers`包，513
- 仅通过代码管理方向，238–240
- `orientation`作为
  - `android:configChanges`值，228
- `ORIENTATION_LANDSCAPE`常量，222，223t，224
- `ORIENTATION_PORTRAIT`常量，222，224
- `OutputStyle`，66
- `Activity`类的`overridePendingTransition`方法，159t

### P

- `PackageManager`类，386，386t，464，465t
- `Paint`类的方法，299，299t
- `Paint`对象，303
- `params`，258
- `parent`样式，64
- `parseFloat`，71
- `parseInt`方法，71
- `ParseTask`类，523–525，527，528
- `PendingIntent`类，554–555，555t
- 持久化数据（使用本地数据库），188
- 持久化数据（使用偏好设置），161
- Photo 应用，464
  - 相机应用，访问，版本 0，464–471
  - 电子邮件应用，使用，版本 5，499–503
  - 图片灰度化，版本 1，471–477
  - 改进用户界面，版本 3，485–490
  - 使用`SeekBars`实现灰度渐变，版本 2，477–485
  - 存储图片，版本 4，490–499
- `placeTextViewAtPosition`方法，276
- `play`方法，352，362
  - 属于`MainActivity`类，Hangman 应用，版本 4，363
- `playHitSound`方法，330
  - 属于`MainActivity`类，330
- `portrait`，229
- `postInvalidate`方法，315
- `PreferenceFragment`，341
- `private`类，279，285，320
- 伪代码，265
- `public`字段和方法，222，222t，345
- `public static`内部类，47
- `public static`内部接口，251
- Puzzle 应用，250，250f，251
  - 版本 0，261–265
  - 版本 1，265–270
  - 版本 2，270–277
  - 版本 3，284–288
  - 版本 4，289–291
- `Puzzle`类，259，260，285
- `PuzzleView`类，261–263b，266，268–269b
  - 其`fillGui`方法，290
  - Puzzle 应用，版本 2，272–274b
- `PuzzleView`构造函数，261

### R

- `RadioGroup`类，201
  - 其选中的方法，202t
- `rawQuery`方法，194
- `R.drawable.nameOfFile`，300
- Really Simple Syndication (RSS) 源，510
- `RecognitionListener`接口，418，420t
- `RecognizerIntent`类，其常量，385，385t
- `Rect`类
  - 其`intersects`方法，313，313t
- `Rect`构造函数，301
- `RectF`类，305
- `red_thumb.xml`文件，479
- 关系数据库管理系统 (RDBMS)，174
- `RelativeLayout`类，11，12，47，91，181，256，258
  - 用于第二屏幕 GUI，135–140
- `RelativeLayout.LayoutParams`，235，256，263
  - 其有用的 XML 属性，137t
- 可远程对象，374
- `RemoteDataReader`类，561，563–564b
  - 从远程位置读取数据，562t
- `RemoteViews`类，546，546t，552，552t
  - 其`setOnClickPendingIntent`方法，554，555t
- `removeLocationUpdates`方法，456
- `res`目录，7，8
  - 其内部支持的子目录，57t
- `reset_button.xml`文件，589
- `ResolveInfo`类，386，386t
- `Resources`类，223，643，644t
  - `getDimensionPixelSize`方法，646t
  - `getIdentifier`方法，646t
  - 其`openRawResource`方法，515，515t
- `Resources`引用，223，263
- `Resources.Theme`类
  - 其`resolveAttribute`方法，645t
- 可复用的`GameStateFragment`类
  - Hangman 应用，版本 6，367–368b
- 反向地理编码，408，409t
- `rgb static`方法，263
- `R.java`文件，选中的内容，160b
- 旋转设备，227
- `rowSpec`，105
- RSA 加密，630
- `RSAEncryption`类，630–631
- RSS。参见 Really Simple Syndication 源
- `run`方法，314，316，322
  - 属于`GameTimerTask`类，315，330

### S

- SAX 解析器。参见 Simple API for XML (SAX) 解析器
- `SAXHandler`类，514b，518–520，519b
- `SAXParser`类，513–514，513t
- `SAXParser Factory`类，514，514t
- `scale`变量，303
- `schedule`方法，314
- `scheduleAtFixedRate`方法，314
- `scramble`方法，259, 261
- 屏幕
  - 设备的，643, 643f
  - 的视图组件，226, 226f
- `screenHeightDp`存储，224
- `SCREENLAYOUT_SIZE_LARGE`，223
- `SCREENLAYOUT_SIZE_NORMAL`常量，223



*   `SCREENLAYOUT_SIZE_SMALL` 常量，223
*   `SCREENLAYOUT_SIZE_XLARGE`，223
*   `screenSize` 值，228
*   `ScrollView`，200–201, 213
*   `SeekBar` 类，478
    *   `AbsSeekBar`，478t
    *   的继承层次结构，478f
    *   `ProgressBar`，478t
    *   XML 属性，478t
*   `selectById` 方法，194
*   选定的菜单相关方法，179t
*   `sendEmail` 方法，499
*   发送电子邮件，499
*   分离方法，241
*   `setCannon` 方法，308, 318
*   `setCannonAngle` 方法，320
*   `setContentView` 方法，17, 17t, 237
*   `setDoubleTapListener`，285
*   `setEnabled` 方法，100
*   `setFontSizeToFitInView` 静态方法，289
*   `setInterval` 方法，455
*   `setLayoutMargins` 方法，242
*   `setLayoutParams` 方法，258
    *   属于 `View` 类，259t
*   `setMargins` 方法，235t
*   `setNegativeButton`，111
*   `setNeutralButton`，111
*   `setOnTouchListener` 方法
    *   属于 `View` 类，251, 252t
*   `setOnDoubleTapListener` 方法，278, 287, 320
*   `setPadding`，53
*   `setPositiveButton`，111
*   `setPriority` 方法，455–456
*   `setResult` 方法
    *   属于 `GameResultFragment` 类，Hangman 应用，版本 4，364
*   `setShowAsAction`，177t
*   `setSmallestDisplacement` 方法，456
*   `setSupportActionBar` 属于 `AppCompatActivity` 类，179t
*   `setTitle` 方法，176
*   `setUpFragmentGui` 方法，359
*   `setUpGui` 方法，241
*   `SharedPreference` 接口，选定的方法，163t
*   `SharedPreference.Editor` 接口，选定的方法，162t
*   共享数据（在活动之间），150
*   Show A Map 应用，在平板电脑内运行的部分输出，99, 100b
    *   版本 0，384f
    *   版本 1，400f
    *   版本 2，403f
    *   版本 3，414f
    *   版本 5，425f
*   `ShowAsAction` 属性，177t
*   用于 XML 的简单 API (SAX) 解析器，510–511
*   单次点击，277
*   单例类，150
*   `slide_from_left.xml` 文件，158b
*   智能手机，1
    *   定义，2
    *   操作系统与，2–3
*   `solved` 方法，259
*   声音，播放，324–332
*   `SoundPool` 类，325
    *   的方法，325, 325t
*   `SoundPool.Builder`，325
    *   的默认构造函数和 `build` 方法，326, 326t
*   `SPACING_HORIZONTAL` 常量，236
*   `SPACING_VERTICAL` 常量，236
*   `Spec`，105
*   `SpeechRecognizer` 类，418, 424, 424t
*   SQL 语法，174
*   糖果的 SQL 表，189t
*   SQLite，174, 188–196
*   `SQLiteDatabase` 类，190, 191t
*   `SQLiteOpenHelper` 类，190
    *   选定的方法，194t
*   堆叠顺序，265
*   `start_button.xml` 文件，589
*   `static` 方法，300
*   `static onKeyListener` 接口，75
*   状态栏
    *   的高度，获取，643–648
*   `statusBarHeight` 变量，263
*   `stop_button.xml` 文件，589
*   Stopwatch 应用，588, 588f
    *   改进，版本 2，596–598
    *   管理 `AdView` 的生命周期，版本 5，610–612
    *   放置广告
        *   在屏幕底部，版本 3，598–606
        *   在片段中，版本 4，607–610
    *   运行，版本 1，593–595, 595f
    *   视图，版本 0，588–593, 593f
*   `StorageUtility` 类，491, 493–494
*   `String landscape`，229
*   `String MainActivity`，25
*   `String word`，340
*   `Strings`，259, 261, 263, 277, 365, 374
*   `strings.xml` 文件，13b，14b，51–52，52b，62b，135b，177b，184b，229，231b，234b，350b，415b，449b，601b，627b
*   样式
    *   定义语法，63–64
    *   与主题，62–69
*   `styles.xml` 文件，15b，65b，135b，187b，231b，350–351b，445b，449b，480b，486b，590b，627–628b
*   `super` 构造函数，302
*   `super` 方法，305
*   滑动事件，处理，256–259
*   `switch` 构造，254
*   `switch` 语句，252
*   Symbian，2
*   对称加密，618
*   `SystemClock` 类
    *   `elapsedRealtime` 静态方法，496，496t

### T

*   `TableLayout`
    *   用于前屏幕 GUI，131–135
    *   继承层次结构，132
*   `TableLayout.LayoutParams` 类，235
*   `TableRow` 元素，131
    *   继承层次结构，132
*   点击检测，277–284
*   温度标度，之间的转换公式，559，559t
*   温度小部件应用
    *   自定义，版本 5，570–578
    *   托管，版本 6，578–580
    *   制作步骤，版本 0，540–549
    *   样式设计，版本 1，549–551
    *   来自远程源的温度数据，版本 4，557–569
    *   更新数据
        *   版本 2，552–554
        *   版本 3，554–557
*   `TemperatureParser` 类
    *   应用版本 4，560，561b
*   `TemperatureProvider` 类，541，546b，570
    *   应用版本 2，553b
    *   应用版本 3，555–556b
    *   应用版本 4，567–568b
    *   应用版本 5，575–577b
*   `TemperatureTask` 类，565，565t，567b
*   `TemperatureWidgetConfigure` 类，573–574b
*   `TextAppearance`，64
*   `TextStyle`，64，66
*   `TextView`，12，44–45，46，48，50，61，66，70，115，181，229，250，251，256–259，261，263，266，275，350，453，649，650t
    *   `android:hint`，50t
    *   `android:inputType` XML 属性，51t
    *   `android:textSize`，50t
    *   拖动，270
    *   字体大小，设置，649–654
    *   移动，256–259
    *   选定的 XML 属性，55t
    *   有用的方法，71t
*   `TextView.OnEditorActionListener` 接口
    *   `onEditorAction` 方法，371，371t
*   `TextWatcher` 接口，75，76t
*   `this`，251，253，280
*   线程
    *   主线程，522
    *   用户界面线程，522
*   `TicTacToe` 应用
    *   版本 0，91–96
    *   版本 1，96–100
    *   版本 2，100–102
    *   版本 3，105–110
    *   版本 4，110–115
    *   版本 5，115–121
*   `TicTacToe`，88–91b，118，100
    *   API，88，89t
*   `Timer` 类，314
    *   方法，314t
*   `TimerTask` 类，314
    *   方法，314t
*   `timeToDestination` 方法，GPS 应用，447
*   小费计算器应用
    *   版本 0，44–52
    *   版本 1，53–62
    *   版本 2，62–69
    *   版本 3，69–74
    *   版本 4，74–79
*   `tipCalc`，70
*   `TipCalculator` 类，40，41t，42b，70，73
*   `Toast` 类，387，389t
    *   选定的方法和常量，196t
*   `topMargin` 参数，258
*   触摸事件，检测，251–256
*   `TouchHandler` 类，320，330
*   过渡（活动之间），155
*   `TravelManager` 类，445，446–447b
*   `tvPosition` 方法，275，276
*   `tv.RelativeLayout.LayoutParams`，258
*   补间动画，155
*   两个 XML 布局文件，使用它们管理方向变化，231–232b，234–235b
*   `TypedValue` 类，645t，652，652t

### U

*   `UP` 动作方法，255，258，270，283
*   `Update` 方法，97
*   `UpdateActivity` 类，202，204，213
    *   Candy Store 应用，版本 4，204–206b
*   `updateCannon`，320
*   更新后的 `onDraw` 方法
    *   属于 `GameView` 类，Duck Hunting 应用，版本 3，331b
*   更新后的 `strings.xml` 文件，140b
*   `updateMortgageObject` 方法，154
*   `updateStartPositions` 方法，270，275
*   `updateView` 方法，152，213
*   `Uri` 类，499，501t，533，533t
*   用户自定义的 `View`，317

### V

*   `verticalDimensionsSet`，241
*   `View` 和 `Controller`，拆分，115–121
*   `view` 类，40，43，47，251，252，254，256，298，302，303，649，650t
    *   它的 `bringToFront` 方法，265，265t
    *   它的构造函数，302t
    *   它的 `measure` 和 `getMeasuredHeight` 方法，237，237t
    *   它的方法，302t，315t
    *   它的 `setLayoutParams` 方法，259t
    *   它的 `setOnTouchListener` 方法，251，252t
*   `ViewGroup`，43，47，91，95，235，263，265，345
    *   选定的子类，92t
*   `ViewGroup.LayoutParams`，263，45，46b，105，235
*   `ViewGroup.MarginLayoutParams` 类，235，258，258t
    *   它的 XML 属性，235，235t
*   `View.OnClickListener`，96–97，119
*   `View.OnTouchListener`，251，251t，252，254，265，266，268，280
*   语音识别应用，384–386
    *   用于映射的注解，版本 2，400–405
    *   Google Maps 活动模板，版本 1，391–400
    *   基于语音输入的地图，版本 3，406–414
    *   移动地图
        *   通过语音连续移动，版本 6，425–426
        *   通过语音单次移动，版本 5，418–425
    *   语音输入，版本 4，414，418
    *   版本 0，387–391

### W

*   `warning` 方法，365
*   Web Content 应用，510
    *   版本 0，510–517
    *   版本 1，518–521
    *   版本 2，521–526
    *   版本 3，526–530
    *   版本 4，531–533
*   `WebViewFragment`，341
*   `widget_config.xml` 文件，571，572b
*   `widget_info.xml` 文件，542b，572b，579b
*   `widget_layout.xml` 文件，544b，550，551b
*   `widget_shape.xml` 文件，550b
*   小部件，42–43。参见 应用小部件
*   Windows，2
*   `word` 实例变量，338
*   `WordGame` 接口，370
*   `wrapCenterWeight1` 样式，349

### X

*   XML，510
*   XML 解析，510
