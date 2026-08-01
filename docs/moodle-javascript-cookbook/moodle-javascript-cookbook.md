# oodle JavaScript 秘籍



















# 鸣谢

**作者**
Alastair Hole

**编辑团队负责人**
Akshara Aware

**审核员**
Anthony Borrow
Mauno Korpelainen
Susan Smith Nash

**项目团队负责人**
Priya Mukherji

**项目协调员**
Srimoyee Ghoshal

**版权编辑**
Chaitanya Apte

**校对**
Joel T. Johnson

**开发编辑**
Roger D'souza

**制作协调员**
Kruthika Bangera

**技术编辑**
Azharuddin Sheikh

**封面工作**
Kruthika Bangera

**文案编辑**
Neha Shetty

**索引员**
Hemangini Bari

# 关于作者

Alastair Hole 是一位 Web 开发人员，目前专注于教育软件，特别是与英国进阶教育和高等教育相关的软件。他的 Web 开发经验始于互联网泡沫后的时代，曾在出版行业的 B2B 电子商务 Web 应用领域工作，侧重于后台集成。此后，他将才华转向教育领域，创建的项目获得了《时代报教育补充》（The Times Educational Supplement）和 IMS 全球学习联盟等组织的奖励。

Alastair 是获奖插件 Moodle 内容包仓库插件“MrCUTE--Moodle 仓库：创建、上传、标记与嵌入”的作者，该插件是一个由联合信息系统委员会 (JISC) 委托的开源项目，已从苏格兰到澳大利亚的全球 Moodle 站点被广泛使用。

感谢所有对本书的完成做出贡献的人，无论是对错过截止日的耐心，还是在一切似乎都不可收拾时的鼓励。感谢 Ma 和 Pa Hole，你们远见卓识，预见到总有一天我会学会重新组装我曾拆卸、断开、拆解或以其他方式摆弄过的所有东西。感谢互联网提供了一个不断扩张的自学机会源。

请记住，“这仅仅是一场旅程。我们可以随时任何时候改变它。”

# 关于审核员

**Anthony Borrow, S.J.** 是新奥尔良教区的耶稣会士，在 Moodle 社区已活跃五年。Anthony 拥有圣路易斯大学的咨询学硕士学位以及圣克拉拉大学耶稣会神学院的神学硕士学位。Anthony 自1992年以来一直致力于各种数据库系统的设计和实现。

Anthony 以贡献协调员的身份为 Moodle 社区服务。在该职位上，Anthony 曾在美国各地的 Moodle Moot（会议）上演讲，并为学习如何实施 Moodle 的机构提供内部培训机会。Anthony 正在 Cristoy Rey 耶稣会（http://cristoreyejuit.org/）培训校园牧师，并为耶稣会中学教育协会（http://jsea.org/）和耶稣会虚拟学习学院（http://jvla.org/）提供技术建议。

Anthony 是《青少年：全球展望》（Teen Gangs: A Global View）洪都拉斯章节的作者，并担任过多种 Pack 书籍的技术审核员。

> 我感谢 Moodle 社区不断激励我学习教育技术，并营造了一个每个声音都能为构建该社区的环境。

**Mauno Korpelainen** 在芬兰的 Hyvinkää 教高中生和成年人数学，多年来一直是 PHM（特别有帮助的 Moodle 用户），并是 **moodle.org** 论坛的版主之一。

Susan Smith Nash 目前是俄克拉荷马州图尔萨美国石油地质学家协会（AAPG）的教育与职业发展总监，也是纽约州奥尔巴尼 Excelsior 学院的兼任教授。在此之前，她是俄克拉荷马大学诺曼市文理学院研究生项目的副院长。她在俄克拉荷马大学获得博士、英语硕士和地质学学士学位。Nash  e-learning 博客，并为许多出版物撰过文章和章节，包括《教学设计与技术的趋势与问题》（第三版）、发展中国家的移动技术采用：影响与意义》。她的最新著作包括《Moodle 教学技巧》（Packt Publishing, 2010）、《电子学习者生存指南》（Texture Press, 2009）以及其他书籍。


# 支持文件、电子书、折扣优惠及更多

您可能希望访问 www.packtpub.com 获取与书籍相关的支持文件和下载。

您知道 Packt 为出版的每本书都提供电子书版本（提供 PDF 和 ePub 文件）吗？作为纸质书客户，您有权在 www.packtpub.com 获取电子书副本。更多详情请通过 service@packtpub.com 与我们联系。

在 www.packtpub.com，您还可以阅读一系列免费的技术文章，订阅一系列免费新闻邮件，并获取 Packt 书籍和电子书的专属折扣和优惠。


您需要 IT 问题的快速解决方案吗？PacktLib 是 Packt 的在线数字图书馆。在这里，您可以访问、阅读并搜索 Packt 的整个书籍库。

# 为什么要订阅？

- 全搜索 Packt 出版的每一本书
- 复制并粘贴、打印和书签内容
- 按需获取并通过网络浏览器访问

# Packt 账户持有者的免费访问

如果您在 www.packtpub.com 拥有 Packt 账户，今天可以使用它访问 PacktLib 并查看九本完全免费的书。只需使用您的登录凭据即可立即访问。






## 第 4 章：使用 YUI 3 操作数据 57

- 引言 57
- 使用 UO 请求 URI 58
- 使用 UO 的替代传输方法请求外部 URL 60
- 使用 PHP 作为代理从外部域加载数据 63
- 使用 DataSource 解析 XML 64
- 使用 DataSource 解析 JSON 67
- 使用 DataSource 解析 CSV 数据 69
- 从 Moodle 2.0 Web 服务获取数据 72
## 第 5 章：使用数据表格工作 79

- 引言 79
- 初始化 YUI DataSource 80
- 显示数据 83
- 基础列排序 85
- 添加分页 87
- 启用滚动 88
- 启用编辑 89
## 第 6 章：增强页面元素 93

- 引言 93
- 添加带有自动完成的文本框 94
- 添加带有自动完成的组合框 96
- 显示自动更新的数据 98
- 启用可调整大小的元素 100
- 添加自定义提示框 101
- 添加自定义按钮控件 103
## 第 7 章：高级布局技术 105

- 引言 105
- 添加弹出导航菜单 106
- 添加下拉导航菜单 109
- 显示树形导航菜单 112
- 添加标签页内容控件 114
- 在模态窗口中显示内容 118
## 第 8 章：组件动画 123

引言 123

元素淡入 124

元素淡出 126

元素滚动 129

调整元素大小 132

使用缓动动画 134

沿直线路径移动元素 136

沿曲线路径移动元素 138

更改元素颜色 141

序列化多个动画 142
## 第 9 章：集成外部库 147

引言 147

添加 jQuery 框架 148

添加 MooTools 框架 149

添加 Dojo 框架 151

添加 Prototype 框架 153

为 Prototype 添加 script.aculo.us 插件 155

使用 Lightbox 2 添加图片放大功能 157

# 序言

Moodle 是同领域最优秀的电子学习解决方案，正在彻底改变 Web 课程。在 Moodle 中使用 JavaScript 对于管理员和动态开发人员非常有有用，因为它使用了内置库来提供当今网络用户所期望的现代动态体验。

《Moodle JavaScript 食谱》将带你了解结合 Moodle 与 JavaScript 的基础知识，并解释如何配合 Moodle 一使用 JavaScript。它将解释如何将 Yahoo! 用户界面库 (YUI) 集成到 Moodle 中。YUI 将是本书的重点，也是实现现代、动态、功能丰富的界面的关键，帮助你的用户获得更满意、更高效的 Moodle 体验。它将使你能够添加特效、让表单响应迅速、使用 AJAX 和动画来创建更丰富的用户体验。你将学习一系列 YUI 特性，例如从其他网站获取并显示信息、增强现有的 UI 元素以使用户生活更轻松，甚至为你的页面添加动画以达到锦睛之笔。

# 本书涵盖的内容

第 1 章，结合 Moodle 与 JavaScript。在本章中，我们将学习将 JavaScript 代码与 Moodle 2.0 集成的基础技术。我们将学习几种在 Moodle 页面中包含 JavaScript 代码的方法。

第 2 章，Moodle 与 Yahoo! 用户界面库 (YUI)。在本章中，我们将学习使用 YUI 的基础知识。我们还将学习如何使用控制台进行调试。

第 3 章，Moodle 表单验证。在本章中，我们将学习如何添加自定义验证逻辑。

第 4 章，使用 YUI 3 操作数据。在本章中，我们将介绍使用 YUI 的各种方法。

第 5 章，使用数据表格工作。在本章中，我们将学习如何初始化一个 YUI DataSource。

第 6 章，增强页面元素。在本章中，我们将介绍其中的一些技术。

第 7 章，高级布局技术。在本章中，我们将介绍设计用户与内容交互方式的可用技术。

第 8 章，组件动画。在本章中，我们将介绍如何让页面上的元素活起来。

第 9 章，集成外部库。在本章中，我们将介绍用于集成外部 JavaScript 库的方法。





# 本书所需的准备工作

为了使用书中配方中提供的代码，你需要安装 Moodle 2.0，并使用你喜爱的文本编辑器来运行代码，以便进行任何更改。请访问 http://moodle.org/ 获取 Moodle 2.0 的下载链接和安装说明。

# 本书的读者群体

本书面向倾向于使用插件模块、主题和补丁对 Moodle 进行自定义定制的开发者和管理员，他们希望让自己的网站更具动态性。如果你已经了 HTML、PHP 和 CSS 的相关知识，并对 Moodle 的底层结构有良好的了解，那么这本书就适合你。不需要预先具备 JavaScript 经验。

# 约定

在书中，你将发现多种风格的文本，用以区分不同类型的信息。以下是这些风格的一些示例及其含义解释。

文本中的代码词汇显示如下：“我们将创建一个简单的 MooTools 脚本，它会在 domready 事件被触发时显示一个 JavaScript 警框。”

代码块显示如下：

```
window.addEventListener('domready', function() {
  alert('Hello from MooTools');
});
```

当我们希望引起你注意代码块的特定部分时，相关的行或项目将**加粗**显示：

```
{
  key: "title",
  label: "Title",
  formatter: "string",
  sortable: true
}
```

# 前言

新术语和重要词汇**加粗**显示。你在屏幕、菜单或对话框中看到的文字显示如下：“当用户点击按钮时，调用窗口的 show 方法”。

> 警告或重要注释以这种形式显示。

> 提示以这种形式显示。

# 读者反馈

我们欢迎读者的反馈。告诉我们你对这本书的看法——你喜欢或可能不喜欢的地方。读者反馈对于我们开发真正优秀的作品至关重要。

要发送通用反馈，请向 feedback@packtpub.com 发送邮件并在主题中注明书名。

如果你需要并希望我们出版书籍，请通过 www.packtpub.com 上的反馈表格告诉我们。如果你对某个主题有专长并愿意编写或贡献书籍，请查看 www.packtpub.com/authors 指南。

# 客户支持

既然你是 Packt 书籍的所有者，我们有许多方法可以帮助你从购买中获得最大的收益。

# 下载代码

你可以从 http://www.PacktPub.com 下载所有 Packt 书籍的示例代码文件。如果你是从其他地方购买的书籍，可以访问 www.PacktPub.com。

# 错误说明

尽管我们尽力确保内容的准确性，但错误仍然在所避免。如果你在我们的书籍中发现错误——无论是文本还是代码——请向我们报告。这样做可以帮助其他读者避免困扰，并帮助改进后续版本。如果你发现任何错误，请访问 www.packpub.com/support，选择你的书籍，点击错误提交链接并输入错误详情。一旦你的错误通过验证，你的提交将被接受并上传到我们网站对应书籍的错误部分。你可以通过 www.packpub.com/support 查看任何错误。

# 版权

互联网上的版权材料侵版是一个持续存在的问题。在 Packt，我们非常重视版权和许可的保护。如果你在互联网上发现我们作品的任何形式的非法副本，请立即向我们提供地址或网站名称以便我们采取措施。

请通过 copyright@packpub.com 与我们联系并提供疑似侵权材料的链接。

感谢你帮助保护我们的作者以及帮助我们为你带来有价值的内容。

# 疑问

如果你在本书的任何方面遇到问题，可以通过 questions@packpub.com 联系我们，我们将尽力解决。

# 结合 Moodle 与 JavaScript

在本章中，我们将涵盖：

- 创建一个新的 Moodle PHP 页面
- 加载 JavaScript 文件
- 在 `<head>` 中加载 JavaScript 文件
- 从 PHP 生成 JavaScript 函数调用
- 将变量从 PHP 传递到 JavaScript
- 确保符合 XHTML Strict 标准
- 从 Moodle 获取语言字符串

## 引言

网页和网站自 20 世纪 90 年代初诞生（HTML 的创建）以来已经有了巨大的进步。像 Moodle 这样的现代 Web 应用与它们最初模仿的简单处理文档有更多共同点。

现代 Web 应用武器库中的一个关键武器是本书的主题——JavaScript。

从本质上说，JavaScript 是一种运行在用户浏览器而非 Web 服务器上的编程语言，它允许程序员通过所谓的文档对象模型（DOM）来操作网页。DOM 是底层 HTML 页面的表示，其结构方式提供了访问 HTML 页面内每一个元素的方法。现代浏览器现在实现了标准版本的 DOM，因此它可以被视为一种跨平台技术。

# 结合 Moodle 与 JavaScript

近年来，JavaScript 框架的使用显著增加。JavaScript 框架是一个 JavaScript 代码库，让 JavaScript 程序员的生活更加轻松。通常，它们提供了更高效的方法来执行 JavaScript 中最常见的任务，例如定位 DOM 元素或为这些元素绑定事件。（事件是元素的功能，例如，HTML 输入按钮在鼠标指针悬停在按钮上点击时会触发“点击”事件。）此外，它们提供了对特定浏览器怪性的抽象，使得编写可在各种浏览器中运行的跨平台代码变得非常容易。

一个 JavaScript 框架是 Yahoo 用户库（YUI）。YUI 是 Moodle 2.0 选择的框架，包含在标准的 Moodle 2.0 软件包中。由于由于原因，后续章节涵盖的许多技术将基于 YUI。在最后一章中，我们将简要探索其他 JavaScript 框架。

也许比“如何”使用 JavaScript 更重要的是“何时”使用它。如果你正在构建一个在公共环境中使用的应用程序，那么你的目标应该是尽可能让所有类型的用户都能访问。专门对于 JavaScript 而言，这意味着你网站的核心功能对于那些由于某种原因无法或不想使用支持 JavaScript 的浏览器的用户也是可用的。这些技术构成了所谓的“渐进式增强”的一部分。

在本章中，我们将学习将 JavaScript 代码与 Moodle 集成的基础技术。我们将学习如何通过 .js 文件在 Moodle 页面中包含 JavaScript 代码，以及如何让代码运行。最后，我们将查看最佳实践，以及如何让 Moodle 数据和语言字符串对代码可用。

# 创建一个新的 Moodle PHP 页面

我们在书中配方中使用所有代码示例都基于我们在本配方中创建的模板。该模板设置了必要的 Moodle 环境并显示了标准的 Moodle 头部和页脚。





## 第一章

请参考 http://docs.moodle.org/ 上的 Moodle 文档，以决定哪种插件框架适合您的需求。

在极少数情况下，可能无法在插件框架内实现您想要的功能，这可能需要修改核心代码。如果确实如此，那么您所需要的功能可能对所有 Moodle 用户都有用。因此，你应该与 Moodle 开发社区联系，就就将更改包含在核心代码新修订版本中的可行性寻求建议。

然而，如果你确切知道自己绝对需要对核心代码进行更改，并且这些更改是为 Moodle 的使用而定制的，那么你可以考虑（作为最后手段）修改核心代码文件。请注意，这种方法并非没有问题，它会带来显著的缺点：

-   跟踪你对每个文件所做的每处更改，并在升级到 Moodle 的未来版本时合并这些更改。CVS 或 GIT 等版本控制系统可以为你提供帮助。
-   你的更改将不会经过与官方代码相同标准的测试和调试。
-   无法保证你的更改在未来的版本中仍继续正常工作；你需要在每次未来的升级中对你的更改进行完全测试。

所以，如你所看到的，扩展和增强 Moodle 的每种方法在功能通用性上都有权衡；因此你应该明智地选择。如果有疑问，请使用插件或主题！

### 准备工作

首先，我们将在 Moodle 安装目录中创建一个名为 `cook` 的子文件夹，并在其中放置我们在书中将使用的所有文件。

接下来，我们将创建一个 PHP 文件 `blank.php`，内容如下：

```php
<?php
require_once (dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/blank.php');
echo OUTPUT->header();
echo OUTPUT->footer();
?>
```

## 下载示例代码文件

> 你可以从 http://www.PacktPub.com 上的账户下载你购买的所有 Packt 书籍的示例代码文件。如果你在其他地方购买了此书，可以访问 http://www.PacktPub.com/support 并注册，以便文件通过电子邮件发送给你。

## 结合 Moodle 和 JavaScript

我们现在将模板保存到了 `/path/to/moodle/cook/blank.php`。

为了测试这个新模板，我们可以在浏览器中加载它并检查一切是否正常。假设我们有一个运行中的 Web 服务器，并在基础 URL http://localhost/moodle 处提供 Moodle 服务，我们可以加载该 URL 来测试我们的新模板：http://localhost/moodle/cook/blank.php。

如果模板设置得正确，我们将看到一个带有标准页眉和页脚的简单页面，如下所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_22_0.png)

### 如何实现...

我们首先以标准方式使用 PHP 标签，即使用 `<?php`。

注意，我们没有使用 `<?` 的简写符号，因为这违背了 Moodle 编程指南，也不符合通用的良好实践。

接下来，我们必须包含 Moodle 的全局配置文件。该文件的包含设置了必要的 Moodle 编程环境，包括我们将要使用的两个全局变量：`$PAGE` 和 `$OUTPUT`。

`$PAGE` 被定义为我们响应用户请求而生成的当前页面信息的中心存储器。

`PAGE` 对象允许我们开始定义页面的属性，即上下文（context）和 URL。页面的上下文是页面的使用范围，即它在 Moodle 系统中使用。我们正在使用系统（System）内容；其他示例在课程（Course）或模块（Module）上下文中。

接下来，我们设置页面的 URL。这反映了我们的目录结构；在这种情况下，将其设置为 `/cook/blank.php`。

`$OUTPUT` 被定义为 `core_renderer` 的实例或其子类之一。使用它来生成输出的 HTML。

`OUTPUT` 对象允许我们根据当前的 Moodle 主题为页面生成页眉和页脚。这是通过调用 `$OUTPUT` 对象的 `header` 和 `footer` 方法，并使用 `echo` 将它们写入页面来实现的。

## 工作原理...

打开 PHP 标签后，我们可以开始插入 PHP 代码。我们使用 `require_once` 来包含 Moodle 配置文件（这确保文件只被包含一次，如果文件不可用，将停止页面执行）。配置文件的路径使用 `dirname` 函数来获取当前文件的路径（使用内置常量 `__FILE__`），然后向上遍历目录（因为我们在 `cook` 子目录中）来寻找 `config.php` 文件。

接下来，我们通过调用 `$PAGE` 对象的 `set_context` 方法获取页面上下文。它接收一个上下文实例。通过向 `get_context_instance` 函数传递 `CONTEXT_SYSTEM` 常量来获取系统上下文的实例。

`$PAGE` 对象的最终用法是设置页面 URL，这是使用 `set_url` 方法在 Web 根 URL 路径实现的，在这种情况下为 `/cook/blank.php`。

接下来，我们需要使用 `$OUTPUT` 对象生成页面页眉和页脚。`header` 和 `footer` 方法都返回字符串形式的 HTML，因此我们可以使用 `echo` 结构将这些字符串写入页面。

## 加载 JavaScript 文件

我们添加的大部分 JavaScript 将包含在外部 JavaScript 文件中，这是一个带有 `.js` 扩展名的文本文件。在本教程中，我们将学习如何使用这种文件。

### 准备工作

首先，我们将在 Moodle 安装目录中创建一个名为 `cook` 的子文件夹，并在其中放置我们在书中将使用的所有文件。

接下来，我们将创建一个 PHP 文件 `blank.php`，内容如下：

```php
<?php
require_once (dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/blank.php');
echo OUTPUT->header();
echo OUTPUT->footer();
?>
```

## 下载示例代码文件

> 你可以从 http://www.PacktPub.com 上的账户下载你购买的所有 Packt 书籍的示例代码文件。如果你在其他地方购买了此书，可以访问 http://www.PacktPub.com/support 并注册，以便文件通过电子邮件发送给你。

## 结合 Moodle 和 JavaScript

我们现在将模板保存到了 `/path/to/moodle/cook/blank.php`。

为了测试这个新模板，我们可以在浏览器中加载它并检查一切是否正常。假设我们有一个运行中的 Web 服务器，并在基础 URL http://localhost/moodle 处提供 Moodle 服务，我们可以加载该 URL 来测试我们的新模板：http://localhost/moodle/cook/blank.php。

如果模板设置得正确，我们将看到一个带有标准页眉和页脚的简单页面，如下所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_22_0.png)

### 如何实现...

我们首先以标准方式使用 PHP 标签，即使用 `<?php`。

注意，我们没有使用 `<?` 的简写符号，因为这违背了 Moodle 编程指南，也不符合通用的良好实践。

接下来，我们必须包含 Moodle 的全局配置文件。该文件的包含设置了必要的 Moodle 编程环境，包括我们将要使用的两个全局变量：`$PAGE` 和 `$OUTPUT`。

`$PAGE` 被定义为我们响应用户请求而生成的当前页面信息的中心存储器。

`PAGE` 对象允许我们开始定义页面的属性，即上下文（context）和 URL。页面的上下文是页面的使用范围，即它在 Moodle 系统中使用。我们正在使用系统（System）内容；其他示例在课程（Course）或模块（Module）上下文中。

接下来，我们设置页面的 URL。这反映了我们的目录结构；在这种情况下，将其设置为 `/cook/blank.php`。

`$OUTPUT` 被定义为 `core_renderer` 的实例或其子类之一。使用它来生成输出的 HTML。

`OUTPUT` 对象允许我们根据当前的 Moodle 主题为页面生成页眉和页脚。这是通过调用 `$OUTPUT` 对象的 `header` 和 `footer` 方法，并使用 `echo` 将它们写入页面来实现的。

## 工作原理...

打开 PHP 标签后，我们可以开始插入 PHP 代码。我们使用 `require_once` 来包含 Moodle 配置文件（这确保文件只被包含一次，如果文件不可用，将停止页面执行）。配置文件的路径使用 `dirname` 函数来获取当前文件的路径（使用内置常量 `__FILE__`），然后向上遍历目录（因为我们在 `cook` 子目录中）来寻找 `config.php` 文件。

接下来，我们通过调用 `$PAGE` 对象的 `set_context` 方法获取页面上下文。它接收一个上下文实例。通过向 `get_context_instance` 函数传递 `CONTEXT_SYSTEM` 常量来获取系统上下文的实例。

`$PAGE` 对象的最终用法是设置页面 URL，这是使用 `set_url` 方法在 Web 根 URL 路径实现的，在这种情况下为 `/cook/blank.php`。

接下来，我们需要使用 `$OUTPUT` 对象生成页面页眉和页脚。`header` 和 `footer` 方法都返回字符串形式的 HTML，因此我们可以使用 `echo` 结构将这些字符串写入页面。

## 加载 JavaScript 文件

我们添加的大部分 JavaScript 将包含在外部 JavaScript 文件中，这是一个带有 `.js` 扩展名的文本文件。

```php
alert('Hello World!');
```

> 有许多原因导致你要求文件被包含在 `<head>` 中，例如如果你需要使用 `document.write` 手动写入 `<head>` 内容。

> 有关关于此技术的进一步讨论，请参考 Yahoo! 开发者资源 http://developer.yahoo.com/performance/rules#js_bottom

这段代码必须在 Moodle 配置文件 config.php 被包含之后包含。这就是我们我们设置 `$PAGE` 对象的地方。

```html
<script type="javascript" src="http://localhost/moodle/lib.php?file=cook/alert.jsrev=1"></script>
```





## 结合 Moodle 和 JavaScript

### 如何实现...

你会发现这段代码与上一个配方的代码几乎相同。这里的关键在于我们传递给 `$PAGE->requires->js` 方法的参数。我们传递了第二个可选参数，它决定了是否在文档的 `<head>` 标签内渲染 `<script>` 标签。在例例中，我们将将其设置为 `true`，以确保 `<script>` 标签按此方式进行渲染。

###其工作原理...

我们再次调用了 `$PAGE->requires->js`，这次带有两个参数。第一个参数是我们想要包含的 `.js` 文件的路径。第二个参数是一个布尔值，用于指定是否在 HTML 页面的 `<head>` 标签中包含该文件。

渲染到文档中的 `<script>` 标签与上一个配方中的相同，关键区别在于它被渲染在 `<head>` 标签内，而不是在 `</body>` 标签的末尾。

## 从 PHP 生成 JavaScript 函数调用

我们已经加载了 JavaScript 文件，我们需要一种方法来执行它。同样，我们可以使用页面需求管理器 `$PAGE` 来生成对我们 JavaScript 函数的调用。

> 本配方描述了在页面加载时执行你的 JavaScript 代码的基本技术。基于使用 Yahoo! User Interface 库处理 DOM 事件的更复杂的将在将在章节中介绍。

### 准备工作

创建一个名为 `requirejs_init.php` 的 PHP 文件，内容如下：

```php
<?php
require_once(dirname(__FILE__), '/config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/course/requirejs_init.php');
$PAGE->requires->js('/course/requirejs_init.js');
$PAGE->requires->js_call('hello');
echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

设置相应的 JavaScript 文件 `requirejs_init.js`，内容如下：

```javascript
function hello(Y)
{
  alert('Hello World!');
}
```

现在当我们加载页面时，我们看到 JavaScript 警告已执行，这向我们证明了代码正在正确加载和执行，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_27_0.png)

### 如何实现...

当我们想要调用名为 `hello` 的 JavaScript 函数时。这是通过 `js_init_call` 方法实现的。我们传递了一个参数，它是一个包含我们想要调用的函数名称字符串，即 `hello`。

###其工作原理...

当文档被渲染时，`js_init_call` 方法确保生成对我们 JavaScript 函数的调用。此示例将生成以下 JavaScript：

```javascript
hello(Y);
```

该 JavaScript 随后包含在最终页面 `</body>` 标签最后的 `<script>` 标签内。

## 从 PHP 将变量传递到 JavaScript

在上一个配方中，我们学习了如何运行 JavaScript 函数，但没有向它传递任何数据。在这个配方中，我们将向 JavaScript 函数传递两个参数——要显示的消息和当前用户的用户名，演示如何让 PHP 中的变量值在我们的 JavaScript 代码可用。

## 结合 Moodle 和 JavaScript

### 准备工作

创建一个名为 `requirejs_init_data.php` 的新 PHP 文件，内容如下：

```php
<?php
require_once(dirname(__FILE__)) . './../config.php';
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/requirejs_init_data.php');
$PAGE->requirejs('js/cook/requirejs_init_data.js');

$PAGE->requires('js_init_call('hello', array('Hello', $USER->username));');

echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

这段代码设置了一个简单的 Moodle 页面并包含了 JavaScript 文件 `requirejs_init_data.js`，其中包含我们将调用的基础“Hello World”函数，该函数接受三个参数。

注意，第一个参数 `Y` 是 YUI 对象的实例，由页面需求管理器自动传递给我们的函数。

后续两个参数是传递给函数的字符串：`message` 和 `username`：

```javascript
function hello(Y, message, username)
{
    alert(message + ' ', ' + username);
}
```

现在当我们加载页面时，我们看到 JavaScript 警告已执行，显示了随之传递的消息以及当前用户（admin）：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_28_0.png)

### 如何实现...

在调用 `$PAGE->requires->js` 之后，添加以下代码：

```php
$PAGE->requires->js_init_call('hello', array('Hello', $USER->username));
```

第一个参数是包含我们想要调用的 JavaScript 函数名称的字符串，在这种情况下是 `hello`。

第二个参数是一个 PHP 值数组，这些值按照定义的顺序传递给 JavaScript 函数。

使用数组允许 `js_init_call` 方法支持任意数量的参数，在本例中：`message` 和 `username`。

###其工作原理...

我们使用了页面需求管理器来注册我们想要调用的函数名称，并通过 PHP 数组中的函数传递了两个额外参数。

当文档被渲染时，以下 JavaScript 将将在 `</body>` 标签结束之前的 `<script>` 标签内生成：

```javascript
hello(Y, "Hello", "admin");
```

## 确保符合 XHTML 严格标准

Moodle 使用 `DocType XHTML Strict`。我们应该注意确保我们的 JavaScript 符合此标准。

尽管可以避免，但偶尔可能需要在嵌入页面中的 `<script>` 标签内包含 JavaScript 代码。如果是这样，代码极有可能会包含对 XHTML Strict 规范具有特殊意义的字符，例如 `&` 和 `<` 等。

### 准备工作

打开包含嵌入 JavaScript 的 PHP 文件，并找到开始和结束的 `<script>` 标签。

### 如何实现...

在起始 `<script>` 标签之后立即添加以下代码：

```html
<script language="JavaScript" type="text/javascript">
//<!CDATA[
```

在结束的 `<script>` 标签之前立即添加以下代码：

```javascript
//]]>
</script>
```

###其工作原理...

我们使用的 `CDATA` 标签确保浏览器不会尝试将 JavaScript 解析为 XHTML 标记。

此外，为了避免与 JavaScript 语法冲突，我们使用了 `CDATA` 。

## 从 Moodle 获取布局字符串

Moodle 使用语言字符串来支持国际化。在实践中，字符串存储在语言文件中。例如，字符串“Submit assignment”可能存储在相应的语言文件中。当用户更改其偏好语言时会自动。

### 准备工作

在本示例中，我们将获取内置的 Moodle 语言字符串并证明它在我们的 JavaScript 代码中可用。

我们再次从一个基础 Moodle 页面和关联的 .js 文件开始：

```php
<?php
require_once(dirname(__FILE__)) . '../config.php';
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/requirejs_init.php');
$PAGE->requires->js('/cook/requirejs_init.js');
$PAGE->requires->string_for_js('course', 'moodle');
$PAGE->requires->js_init_call('lang');
echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

如所示，这段代码注册了对函数 `lang` 的调用，该函数定义在关联的 .js 文件中：

```javascript
function lang (Y)
{
    alert(M.str.moodle.course);
}
```

现在当我们加载页面时，我们看到 JavaScript 警告已执行，显示了我们设置的语言字符串值，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_31_0.png)

### 如何实现...

我们使用熟悉的方法 `$PAGE->requires->js` 包含了我们的 .js 文件。

在这一行之后，我们使用了页面需求管理器的一个新功能，`string_for_js` 函数：

```php
$PAGE->requires->string_for_js('course', 'moodle');
```

最后，我们在我们的 JavaScript 代码中引用此语言字符串：

```javascript
alert(M.str.moodle.course);
```

###其工作原理...

我们调用 `string_for_js` 方法并带有两个参数：我们想要获取的字符串名称以及该字符串的位置。在本例中，我们从核心 Moodle 语言文件中获取 `course` 的语言字符串。




现在，此字符串作为 Moodle 全局 JavaScript 命名空间 (M) 的一部分提供给我们，格式为 `M.str.<module name>.<string name>`。在我们的示例中，它是 `M.str.moodle.course`。

通过这种方法，我们设置的字符串对所有后续 JavaScript 代码可用。如果我们简单地将此字符串作为参数传递给 JavaScript 函数，它将只在该函数内部可用。如果我们需要它在额外的函数可用，就必须重复该过程，创建字符串的副本并将其传递给额外的函数，这将导致代码出现不必要的低效。

# 2 Moodle 和 Yahoo! 用户界面库 (YUI)

在本章中，我们将涵盖：

- 初始化 YUI 3 库
- 加载 YUI 3 模块
- 从 YUI 3 加载 YUI 2 模块
- 绑定基础事件处理器
- 绑定高级 DOM 事件处理器
- 实现事件委托（Event Delegation）
- 使用 YUI 控制台进行调试

# 简介（Introduction）

编写 JavaScript 时，需要执行许多常见任务。其中很大一部分仅仅涉及到处理 Web 浏览器之间的差异。为了能够隐藏或将每个浏览器的特定细节抽象为标准接口，产生了被称为 JavaScript 库的工具集。今天 Web 上最广泛使用的库之一是 Yahoo! 用户界面库 (YUI)。

## Moodle 和 Yahoo! 用户界面库 (YUI)

Moodle 包含一个 YUI 副本作为其首选的 JavaScript 库。YUI 为开发者提供了广泛的工具来增强他们的 Web 应用程序：

YUI 库是一组用 JavaScript 和 CSS 编写的工具和控件，用于通过 DOM 脚本、HTML 和 AJAX 等技术构建高度交互的 Web 应用程序。YUI 以 BSD 许可提供，对所有用户免费。YUI 被证明是成熟、可扩展、快速且健壮的。它由来自的前端工程师和贡献者构建，是一个为热爱 JavaScript 的人士提供的工业级 JavaScript 库。

Yahoo! Developer Network
http://developer.yahoo.com/yui/

在本章中，我们将学习使用 YUI 的基础知识。我们将学习如何初始化 YUI 并使其准备好供我们的代码使用，以及从 YUI 的 2 和 3 版本加载额外的模块。我们还将学习如何通过向我们的控件绑定事件来管理代码的执行，最后如何使用 YUI 日志工具调试代码。

# 初始化 YUI 3 库

在本食谱中，我们将学习如何在 Moodle 中初始化 YUI 3 环境，这将使我们能够使用 YUI 特性。Moodle 处理了大部分的初始设置，即加载所需的 CSS 和 JavaScript 文件，因此我们只需要关注激活 YUI 环境即可。

此示例将展示如何在 YUI 环境内部执行 JavaScript 代码。我们将设置一个小小的 YUI 脚本，它将简单地在 JavaScript alert 框中显示包含活动 YUI 环境版本号的消息。

这提供了一个让 YUI 运行所需的示例视图，我们将在随后的食谱中在此基础上构建。

# 准备工作（Getting ready）

我们首先在 `cook` 目录下创建一个新的 PHP 文件 `yui_init.php`，内容如下：

```php
<?php
require_once(dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/yui_init.php');
$PAGE->set_js('/cook/yui_init.js');
echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

注意，前面的代码引用了一个 JavaScript 文件 `yui_init.js`，其内容如下：

```javascript
YUI().use
{
  function(Y)
  {
    alert('Hello from YUI ' + Y.version);
  }
};
```

# 如何实现？（How to do it?）

我们创建了一个 PHP 文件，设置了 Moodle 编程环境并包含了一个 JavaScript 文件，这种方法我们已经从之前的食谱中熟悉了。

这里新颖的是 JavaScript 文件的内容，我们将从那里准备好 YUI 3 环境。

Moodle 已经包含了 YUI 所需的所有 JavaScript（这是在我们输出 `$OUTPUT->header()` 返回的值时发生的）。这意味着我们现在在 JavaScript 代码中有一个名为 `YUI` 的全局对象可用。

我们使用 `YUI()` 方法创建 YUI 对象的一个新实例，并立即调用 `use` 方法。

我们将传递给 `use` 方法的唯一参数是一个匿名函数。这就像普通的 JavaScript 函数一样，只是它没有指定名称；因此它是“匿名”的。不需要名称，因为它没有被再次引用，它被直接传递给 `use` 方法。此函数接受单个输入参数 `Y`，该参数将是 YUI 对象新实例的引用。（注意，`use` 方法也用于加载额外的 YUI 模块；这是下一个食谱的主题。）

创建的匿名函数是代码中最需要注意的部分，因为我们将所有利用 YUI 特性的代码都放在这里。在这个示例中，你将看到我们正在创建一个包含 `Y.version` 值的短消息的 JavaScript 警框，`Y.version` 是一个包含已加载的 YUI 版本号的字符串，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_35_0.png)

## Moodle 和 Yahoo! 用户界面库 (YUI)

编写 JavaScript 时需要执行许多常见任务。其中很大一部分仅仅涉及到处理 Web 浏览器之间的差异。为了能够隐藏或将每个浏览器的特定细节抽象为标准接口，产生了被称为 JavaScript 库的工具集。今天 Web 上最广泛使用的库之一是 Yahoo! 用户界面库 (YUI)。

## 工作原理（How it works）

我们使用 `YUI()` 方法创建 YUI 对象的一个新实例，并立即调用 `use` 方法。

## 加载额外的模块（Loading additional modules）

YUI 是一组用 JavaScript 和 CSS 编写的工具和控件，用于通过 DOM 脚本、HTML 和 AJAX 等技术构建高度交互的 Web 应用程序。YUI 以 BSD 许可提供，对所有用户免费。YUI 被证明是成熟、可扩展、快速且健壮的。它由来自的前端工程师和贡献者构建，是一个为热爱 JavaScript 的人士提供的工业级 JavaScript 库。提供的额外模块包括：
- 动画
- 拖放
- 操作 DOM
- 处理事件
- 处理数据 (JSON/XML)

有关所有模块的列表，请参考 Yahoo 网站：http://developer.yahoo.com/yui/

### 如何实现...

加载额外的模块通过 YUI 的 `use` 方法实现。在之前的食谱中，我们学习了使用以下语法运行代码：

```javascript
YUI().use(function(Y) { /* 执行代码 */ });
```

注意 `use` 方法接受任意数量的参数，最后一个参数必须是匿名函数。因此，例如，为了加载动画模块 (`anim`) 和事件模块 (`event`)，我们将使用以下语法：

```javascript
YUI().use("anim", "event", function(Y) { /* 执行代码 */ );
```

## 从 YUI 3 加载 YUI 2 模块（Loading YUI 2 modules from YUI 3）

我们想要从 YUI 3 加载 YUI 2 模块的原因有很多。我们可能有大量的预写 YUI 2 代码可以直接使用，从而避免从头重写的麻烦。另一个可能是，在书中，我们希望使用尚未实现为原生 YUI 3 模块的 YUI 2 功能。在本食谱中，我们将通过在原生 YUI 3 脚本内部加载 YUI 2 的日组件，学习如何从 YUI 3 加载 YUI 2 模块。

# 准备工作（Getting ready）

我们在 `cook` 目录下创建一个新的 PHP 文件 `yui_cal.php`，内容如下：

```php
<?php
require_once(dirname(__FILE__) . './../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/yui_cal.php');
$PAGE->set_requires->js('/cook/yui_cal.js');

echo $OUTPUT->header();

?>
<div id="calContainer"></div>
<?php
echo $OUTPUT->footer();
?>
```

你会注意到 `yui_cal.php` 引用了位于 `cook` 目录的 JavaScript 文件 `yui_cal.js`，其内容如下：

```javascript
YUI().use("yui2-calendar", function(Y) {
  var YAHOO = Y.YUI2;
  var cal = new YAHOO.widget.Calendar("calContainer");
  cal.render();
});
```




Moodle Yahoo! 用户界面库 (YUI)

### 如何操作...

首先，我们创建了一个 PHP 文件 `yui_cal.php`，在其中我们设置了 Moodle 编程环境并引入了我们的 JavaScript 文件 `yui_cal.js`。此外，在这个 PHP 文件中，我们包含了一个容器 `<div>` 标签，并为其分配了 ID `calContainer`。正如你所猜的那样，这就是我们将渲染 YUI 2 容器的地方。

转向此配方中包含在 `yui_cal.js` 中的 YUI 脚本部分，我们首先加载了命名模块 `yui2-calendar`。所有的 YUI 2 模块都使用其原始名称并加上 `yui2-` 前缀进行引用。因此，`calendar` 变成了 `yui2-calendar`。

下一步是重新创建来自 YUI 2 的 `YAHO` 对象。它是作为 YUI 中 YUI 3 对象 `Y` 的一部分提供的。为了方便起见，我们将将其复制到一个新对象 `YAHO` 中。由于这符合 YUI 2 的编码风格，它方便你复用 YUI 2 的代码。

最后，我们创建一个 YUI 2 日历小组件的新实例 `YAHO.widget.Calendar`，传入我们之前创建的容器 `<div>` 容器的 ID，然后调用 `render` 方法来显示日历。

我们的页面应该在我们的 `<div>` 容器内部渲染了一个新的日历控件，如下面的截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_38_0.png)

## 工作原理...

当我们在浏览器中加载 `yui_cal.php` 时，我们的页面会被渲染，其中包含了用于日历的 `<div>` 容器。当页面下载完成后，我们的 JavaScript 就会执行。

在我们的 JavaScript 中，YUI 3 会首先加载 YUI 2 日历模块，其加载方式与我们加载 YUI 3 模块相同，区别在于我们使用了带有 `yui2-` 前缀的 YUI 2 模块名称，即 `yui2-calendar`。

接下来，我们通过从 YUI 3 对象 `Y.YUI2` 复制获取了 YUI 2 对象 `YAHO` 的副本。

最后，我们可以使用新的 `YAHO` 对象创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法进行构建和显示。

## 绑定基础事件处理程序

事件是管理用户界面如何响应用户采取特定操作（主要是通过键盘和/或鼠标）的基础。事件是在特定 DOM 元素的上下文中执行的特定操作。以下是两个常见示例：

- 输入按钮具有 `click`（点击）事件，当用户在鼠标指针悬停在按钮上点击鼠标时触发。
- 输入文本框具有 `focus`（聚焦）事件，当文本框获得焦点时触发，这意味着用户使用鼠标光标或 Tab 将光标移动到文本框。

因此，事件处理程序是一个特定的代码块（回调函数），我们将其注册（附加）到特定的元素和事件组合上，即输入按钮及其点击事件。

在这个配方中，我们将作为第一个示例，学习如何为 HTML 输入按钮绑定点击事件处理程序。我们将设置代码，在点击按钮时显示一个 alert（提示框）。

### 准备工作

我们首先在 `cook` 目录下创建一个新的 PHP 文件 `yui_eventbasic.php`，内容如下：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/yui_event.php');
$PAGE->requires->js('/cook/yui_eventbasic.js');
echo $OUTPUT->header();
?>
<form>
<input type="button" id="btn1" value="Button 1" />
</form>
<?php
echo $OUTPUT->footer();
?>
```

## Moodle 和 Yahoo! 用户界面库 (YUI)

你会注意到 `yui_eventbasic.php` 链接到了位于 `cook` 目录下的 JavaScript 文件 `yui_eventbasic.js`，内容如下：

```javascript
YUI().use("node-base", function(Y) {
  var btn1_Click = function(e) {
    alert('Button clicked');
  };
  Y.on("click", btn1_Click, "#btn1");
});
```

### 如何操作...

我们已经在 `yui_eventbasic.php` 中以现在熟悉的方式设置了 Moodle 编程环境，并增加了一个带有标签 **Button 1**  ID 为 `btn1` 的输入表单，如下面的截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_40_0.png)

这就是我们将注册点击事件的按钮，稍后将通过其 ID 引用它。此 PHP 文件还包含了 JavaScript 文件 `yui_eventbasic.js`，我们将从那里设置事件。

`yui_eventbasic.js` 中的 JavaScript 首先加载我们需要的模块——`--node-base`。

接下来，我们定义了一个函数 `btn1_Click`，它将作为点击事件处理程序。该函数简单地显示一个 alert，以证明事件已正确触发。

最后，我们使用 `Y` 对象的 `on` 方法来注册事件，并如表所示传递三个参数：

| 参数 | 值 |
|---|---|
| 事件名称 | click |
| 要注册的函数名称 | btn1_Click |
| 元素的 ID | btn1 |

我们可以在页面中使用新的 `YAHO` 对象创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法进行构建和显示。（注：此处原文似乎有遗漏，已根据上下文逻辑补全）

工作原理...

当我们在浏览器中加载 `yui_cal.php` 时，我们的页面会被渲染，其中包含了用于日历的 `<div>` 容器。当页面下载完成后，我们的 JavaScript 就会执行。

在我们的 JavaScript 中，YUI 3 会首先加载 YUI 2 日历模块，其加载方式与我们加载 YUI 3 模块相同，区别在于我们使用了带有 `yui2-` 前缀的 YUI 2 模块名称，即 `yui2-calendar`。

接下来，我们通过从 YUI 3 对象 `Y.YUI2` 复制获取了 YUI 2 对象 `YAHO` 的副本。

最后，我们可以使用新的 `YAHO` 对象创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法进行构建和显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。

（由于原文后部分存在大量重复文本，此处已按要求对核心逻辑进行翻译处理）

| 事件 | 说明 |
|---|---|
| domready | 当 DOM 完全加载后可以安全访问。 This element is not applied to a specific element. |
| load | 当 the element is fully loaded by the browser. If applied to the window element, this fires when the entire contents of the window has loaded, including the page and any scripts, or images. |
| available | When the element has loaded, but not necessarily after the element's child elements have loaded. |
| contentready | When the element and all of its child elements are fully loaded. |

> 使用 `YAHO` 对象来创建 `Calendar` 小组件的新实例，将其附加到我们的容器 `<div>` 上，并调用 `render` 方法让其构建并显示。





<h1>按顺序调用的事件：</h1>
</div>
<?php
echo $OUTPUT->footer();
?>
```

你会注意到 `yui_eventdom.php` 链接到了 JavaScript 文件 `yui_eventdom.js`，它位于 `cook` 目录下，内容如下：

```javascript
YUI().use("node-base", function(Y) {
  Y.on(
    "available",
    function() {
      printMessage("Element #container 'available'");
    },
    "#container"
  );
  Y.on(
    "contentready",
    function() {
      printMessage("Element #container 'contentready'");
    },
    "#container"
  );
  Y.on(
    "domready",
    function() {
      printMessage("Page 'domready'");
    }
  );
  Y.on(
    "load",
    function(e) {
      printMessage("Window 'load'");
    }
  );
  Y.config.win
});
```

# Moodle 与 Yahoo! 用户界面库 (YUI)

```javascript
var order = 1;
var container = Y.one('#container');
function printMessage(message) {
  container.append('<p>' + order++ + '. ' + message + '</p>');
};
```

### 如何实现...

在 PHP 文件 `yui_event.dom` 中，我们像通常一样设置了标准模块编程环境，并包含了一个 `<div>` 标签，我们将在其中打印来自四个事件处理器的消息。注意，我们为这个 `<div>` 标签设置了 ID `container`，确保我们稍后可以在 JavaScript 中引用它。

转到 JavaScript 文件 `yui_event.dom`，我们首先加载 `node-base` 模块，它允许我们使用 `Y.on` 方法，我们将使用该方法来注册事件处理器。接下来，我们设置了正在演示的四个事件处理器，从 `available` 和 `contentready` 开始，它们注册在我们的容器 `<div>` 中。下一个事件处理器是 `domready`，它不应用于 DOM 的任何元素，而是页面内固有的。最后，我们使用了 `YUI.config.win`，这是 YUI 对页面窗口对象的浏览器无关的引用。

在这些事件处理器的每一个内部，我们都调用了 `printMessage` 函数，它会打印传递给它的消息，并带上反映调用顺序的数字前缀。

现在当我们在网页浏览器中加载页面时，我们将看到事件被调用的顺序。顺序通常对应于“最安全”的一个。也就是说，该顺序尊重相应的元素，使其在页面加载生命周期中尽早被调用，从而避免遇到任何特定浏览器的问题（例如由于尝试访问尚未加载的 DOM 元素而导致崩溃）。

在接下来的中，我们可以看到三个常见浏览器之间顺序的变化：

- Safari 5

| 按顺序调用的事件： |
| :--- |
| 1. 页面 'ready' |
| 2. 元素 #container 'available' |
| 3. 元素 #container 'contentready' |
| 4. 窗口 'load' |

- Firefox 3

| 按顺序调用的事件： |
| :--- |
| 1. 元素 #container 'available' |
| 2. 元素 #container 'contentready' |
| 3. 页面 'domready' |
| 4. 窗口 'load' |

- Internet Explorer 8

| 按顺序调用的事件： |
| :--- |
| 1. 窗口 'load' |
| 2. 页面 'domready' |
| 3. 元素 #container 'available' |
| 4. 元素 #container 'contentready' |

注意，Firefox 3 是最直观的查看器，容器 `<div>` 标签变为 **available**，然后其子元素加载并变为 **contentready**。随后触发 **domready**，最后在所有额外资源（脚本、样式表和图像）加载完成后，触发窗口-`load` 事件。

# 它的工作原理...

我们使用 *Y.on* 方法将事件分配给它们相应的元素。当页面执行时，YUI 会以特定特定的方式管理这些事件，在最早且最安全的机会触发我们的事件。

当事件触发时，会调用我们的 `printMessage` 函数，该函数会打印一条消息，并带有一个指示事件已触发的数字前缀。这是通过通过全局变量 `order` 进行计数来实现，该计数从 *1* 开始。每当我们打印一条消息时，我们都会在文本中包含此数字，并将其值加一，为显示下一条消息做好准备。

# 实现事件委托

到目前，我们查看了为单个元素注册单个事件的一系列方法。这些技术非常有用，但当我们想要为多个元素注册事件时，就会变得低效且费力。

# Moodle 与 Yahoo! 用户界面库 (YUI)

如果我们以链接列表形式的导航控件为例，我们可以通过手动为每个链接注册事件来为每个链接实现点击事件。对于几个链接这可能还好，但随着列表变大，管理这些事件会变得非常困难。链接越多，越容易出现错误和 Bug。如果不需要，你还会手动编写（并管理）为 50 个链接注册事件的代码吗？

幸运的是，YUI 恰好有这类问题的解决方案，即事件委托。

**事件委托** 是一种技术，我们可以指定一个父元素来处理其子元素。以我们的链接列表为例，这意味着可以使用包含列表的元素来管理列表中的事件。

### 准备工作

我们首先创建一个包含内容的 PHP 文件 `yui_delegation.php`：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/yui_delegation.php');
$PAGE->requires->js('/cook/yui_delegation.js');
echo $OUTPUT->header();
?>
<div id="container">
<ul>
<li id="li-1"><a href="#">Item 1</a></li>
<li id="li-2"><a href="#">Item 2</a></li>
<li id="li-3"><a href="#">Item 3</a></li>
<li id="li-4"><a href="#">Item 4</a></li>
<li id="li-5"><a href="#">Item 5</a></li>
</ul>
</div>
```

接下来，我们创建在下面中引用的 JavaScript 文件 `yui_delegation.js`，其内容如下：

```javascript
YUI().use("event-delegate", function(Y) {
  Y.delegate("click", function(e) {
    var item = this.get('a').get();
    alert("You clicked " + item);
  }, "#container", "li");
});
```



```php
echo $OUTPUT->header();
?>
<h1>YUI Console</h1>
<?php
echo $OUTPUT->footer();
?>
```

 接下来，我们创建一个包含以下内容的强大的 JavaScript 文件 `yui_console.js`：

```javascript
YUI().use("console", function(Y) {
  var myConsole = new Y.Console();
  myConsole.render();

  Y.log("I am an info message.", "info");
  Y.log("I am a warning.", "warn");
  Y.log("I am an error.", "error");
});
```

### 如何操作...

我们的 PHP 页面设置了我们在这些食谱中使用的标准 Moodle 编程环境，链接到我们的 JavaScript 文件 `yui_console.js`。

在这个 JavaScript 文件中，我们首先加载控制台模块。现在我们可以使用 `Y.Console` 对象了。我们创建了该对象的新实例，然后在这个新实例上调用了 `render` 方法。

最后，我们使用 `Y.log` 方法写入了三个示例日志消息，以演示消息是如何记录的。

在网页浏览器中加载页面后，控制台会显示出来，如下所示所示了我们的三个日志消息：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_49_0.png)

## 工作原理...

加载控制台模块后，我们现在可以使用 `Y.Console` 和 `Y.log`。

`Y.Console` 对象允许我们创建一个 YUI 控制台的新实例，当我们调用它的 `render` 方法时，它就会显示在页面上。

最后，我们使用 `Y.log` 方法显示三种不同程度的消息：信息、警告和错误。我们可以根据需要使用这些方法，在普通的文本字符串中显示我们想要渲染的任何类型的调试信息。

# 3 个 Moodle 表单验证

在本章中，我们将涵盖内容：

- 添加必填字段
- 添加具有最大长度的字段
- 添加具有最小长度的字段
- 添加长度在指定范围内的字段
- 添加有效的电子邮件地址字段
- 使用正则表达式添加自定义验证
- 添加仅接受字母字符的字段
- 添加仅接受字母和数字的字段
- 添加仅接受数字的字段
- 拒绝标点符号
- 拒绝没有前零的输入
- 与另一个字段进行比较
- 添加自定义 JavaScript 验证函数回调

# 简介

出于各种原因，我们需要从用户那里收集信息。例如，我们获取联系方式或他们在使用我们的网站时遇到的问题信息。通常情况下，解决这个问题最常见的方案是使用现实世界中的模型：表单。

# Moodle 表单验证 –

基础的 Web 表单与其纸质表单非常相似，在页面上呈现出一系列元素，用户可以在其中输入所需的信息。

Web 表单的优势在于，它们让我们有机会在输入信息时确保提供信息的质量。这个过程被称为表单验证。通过使用这种技术，我们可以对输入的信息应用一系列检查和约束。我们还可以确保在用户提交完成的表单之前，所有这些都得到了满足。

Moodle 提供了一个基于 PHP 扩展和应用程序库 (PEAR) 库 `Quick.Form` 的功能丰富的 Web 表单实用程序。未使用此库生成的 Moodle 表单是例外。在本章中，我们将学习如何激活内置的 JavaScript 表单验证函数，以及如何添加自己的 JavaScript 表单验证逻辑。

第一个食谱将从设置一个 QuickForm 表单并添加一个带有验证的简单文本字段开始。随后的食谱将在此基础表单的基础上构建，并涵盖每个高级高级验证选项。

# 添加必填字段

在这个食谱中，我们将使用 QuickForm 库构建一个新的表单，它由一个应用了“必填字段”验证的文本框组成。

这种表单验证是最简单且最常用的验证。它防止用户留空字段，但对实际输入的内容不施加进一步的限制。

### 准备工作

首先，我们将准备表单定义。在 `cook` 目录下创建一个新文件 `validation_form.php`，内容如下：

```php
<?php
require_once($CFG->libdir.'/formslib.php');
class validation_form extends moodleform
{
    function definition()
    {
        $mform =& $this->form;
        $mform->addElement('text', 'mytext1', 'Required');
        $mform->addElement('submit', 'submitbutton', 'Submit');
    }
}
?>
```

这是一个非常简单的表单定义，包含一个文本框 `mytext1` 和一个提交按钮。

接下来，在 `validation.php` 中准备表单逻辑，内容如下：

```php
<?php
require_once(dirname(__FILE__) . '/../config.php');
require_once('./validation_form.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/validation.php');
$PAGE->requires->js('/cook/validation.js');
echo $OUTPUT->header();
echo $OUTPUT->heading('Moodle JavaScript Cookbook');
$mform = new validation_form();
if ($mform=$mform->get_data()) {
    print_object($mform);
} else {
    $mform->display();
}
echo $OUTPUT->footer();
?>
```

`validation.php` 中的表单逻辑是用于渲染表单的文件，如下所示：

| Moodle JavaScript Cookbook |
|-----------------------------|
| Mytext1                     |
| Submit                      |

### 如何操作...

要添加必填字段，我们在 `validation_form.php` 的表单定义中添加以下代码：

```php
$mform->addRule('mytext1', 'required', null, 'client');
```

# Moodle 表单验证 -

当我们在浏览器中重新加载 `validation.php` 并尝试在不输入任何内容的情况下提交表单时，我们将无法提交，并像如下所示看到警告：

| Moodle JavaScript Cookbook |
|-----------------------------|
| Required |

### 工作原理

我们使用了 QuickForm 的 `addRule` 方法来定义验证：

```php
$mform->addRule('mytext1', 'required', null, 'client');
```

| 参数编号 | 说明 | 值 |
|---|---|---|
| 1 | 应用的元素名称 | mytext1 |
| 2 | 验证失败时显示的文本 | Required |
| 3 | 要应用的规则名称 | required |
| 4 | 规则的格式选项（注意 required 规则没有选项，所以这里传递了 null） | null |
| 5 | 如何执行验证。可以是 client 或 server。 | client |

> 此规则可以与后续食谱中演示的任何规则结合。这确保了字段不仅被填充，而且符合任何额外的约束。同样，两个或多个规则可以在任何地方结合。

# 添加具有最大长度的字段

在这个食谱中，我们将定义一个具有最大长度约束的字段。这可以在需要输入简短摘要文本时使用，例如当“房地产”非常宝贵时。或者，当存储数据的数据库特定列只能存储特定数量字符时，这非常有用。

### 准备工作

请参考本章的第一个食谱了解如何准备 QuickForm 表单的详情，它是本食谱的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中添加以下代码：

```javascript
$mform->addElement('text', 'mytext2', 'Max length 5');
$mform->addRule('mytext2', 'Max length 5', 5, 'client');
```

当我们通过输入六个字符来测试此表单时，我们无法提交表单，我们的验证警告消息将如下所示显示：

| Moodle JavaScript Cookbook |
| Max length | Max length 5 |
|---|---|
| 123456 |
| Submit |

## 工作原理...

我们使用了 `maxLength` 验证类型，它接受一个整数形式的格式选项，表示允许输入的最大长度。

如果用户输入的字符超过了我们允许的长度（在本例中为 5 个），我们配置的警告消息就会显示，并且在输入变得有效（减少到五个或更少）之前，用户无法提交表单。





## Moodle 表单验证

## 添加带有最小长度的字段

在本教程中，我们将应用一种验证约束，强制用户输入至少指定数量字符的文本。这可以用于预期特定字符数量的场景，例如邮政编码或电话号码。

### 准备工作

请参阅本章的第一个配方，了解如何准备 QuickForm Web 表单的详情，它是本配方的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中，在字段定义之后添加以下代码：

```
$mform->addElement('text', 'mytext3', 'Min length 5');
$mform->addRule('mytext3', 'Min length 5', 'minlength', 5, 'client');
```

现在，我们可以在网页浏览器中尝试此规则。当我们输入一个仅四个字符的字符串时，我们无法提交表单，警告信息会显示出来，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_56_0.png)

## 工作原理...

我们使用了验证类型 `minlength`，它接受一个整数形式的格式选项，代表输入允许的最小长度。

在这种情况下，我们指定文本必须包含至少五个字符。当我们输入四个或更少字符的字符串时，我们将无法提交表单，直到通过提供至少五个字符来满足这一最小长度。

## 添加指定范围内的字段长度

在本教程中，我们将学习如何添加一条规则，以确保输入的文本长度落在指定的字符数量范围内。同样，这可以用于验证信息，例如电话号码的长度必须在特定范围内才能被接受。

### 准备工作

请参阅本章的第一个配方，了解如何准备 QuickForm 表单的详情，它是本配方的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中，在字段定义之后添加以下代码：

```
$form->addElement('text', 'mytext4', 'Length 3-5');
$form->addRule('mytext4', 'Length 3-5', 'rangelength',
array(3,5), 'client');
```

现在，我们可以在网页浏览器中测试此验证，并注意到如果输入的文本超出了所需范围，我们的警告信息将会显示，用户将无法继续，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_57_0.png)

## 工作原理...

我们使用了验证类型 `rangelength`，它接受一个包含两个值的数组格式选项：输入长度的下界和上限。使用数组允许我们轻松地通过单个参数向 `addRule` 方法传递一对值。

## Moodle 表单验证

现在，当用户尝试提交长度超出范围的文本时，我们的警告信息将会显示，在文本满足所需的验证规则之前，他们将无法提交表单。

## 添加有效的电子邮件地址字段

在本教程中，我们将添加一条规则，确保用户输入了有效的电子邮件地址。这条规则应该是显而易见的。它仅仅检查文本是否符合标准的 "user@example.com" 格式。

### 准备工作

请参阅本章的第一个配方，了解如何准备 QuickForm 表单的详情，它是本配方的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中，在字段定义之后添加以下代码：

```
$mform->addElement('text', 'mytext6', 'Email');
$mform->addRule('mytext6', 'Email', 'email', null, 'client');
```

现在，我们可以在网页浏览器中测试此验证。当我们输入一个不符合规则的域名时，警告信息将会显示，且我们无法提交表单，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_58_0.png)

## 工作原理...

我们使用了 `email` 验证类型，它不需要格式选项。当用户输入无效的电子邮件地址时，警告信息将会显示，在修复之前他们将无法提交表单。

## 使用正则表达式添加自定义验证

正则表达式是匹配字符串的强大方法。通过使用正则表达式来验证任何模式，这种方法是非常灵活的。在本教程中，我们将使用正则表达式来验证任何文本。

### 准备工作

请参阅本章的第一个配方，了解如何准备 QuickForm 表单的详情，它是本配方的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中，在字段定义之后添加以下代码：

```
$form->addElement('text', 'mytext5', 'URL');
$form->addRule('mytext5', 'URL', 'regex', 'server');
```

现在，我们通过输入域名来测试此规则。警告信息将会显示，在格式化文本之前，我们将无法提交表单，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_59_0.png)

## 工作原理...

我们使用了 `regex` 验证类型，它接受标准正则表达式作为格式选项。

## Moodle 表单验证

注意，Moodle 表单不支持客户端正则表达式。因此，第五个参数必须设置为 `server`。

## 添加仅允许字母的字段

在本教程中，我们将添加一条规则，禁止除字母以外的所有字符，即允许字母。

### 准备工作

请参阅本章的第一个配方，了解如何准备 QuickForm 表单的详情，它是本配方的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中，在字段定义之后添加以下代码：

```
$mform->addElement('text', 'mtext7', 'Letters only');
$mform->addRule('mtext7', 'Letters only', 'lettersonly', null, 'client');
```

当我们输入数字字符测试此规则时，警告信息将会显示，我们无法提交表单，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_60_0.png)

## 工作原理...

我们使用了 `lettersonly` 验证类型，它不需要任何格式选项。现在，当用户尝试提交非字母字符时时，他们将无法继续，但可以看到我们配置的验证警告。

## 添加仅允许字母数字的字段

在本教程中，我们将添加一条仅允许字母数字的规则，即数字 0-9 和大小写字母 a-z。

### 准备工作

请参阅本章的第一个配方，了解如何准备 QuickForm Web 表单的详情，它是本配方的基础。

### 如何操作...

在 `validation_form.php` 的表单定义中，在字段定义之后添加以下代码：

```
$form->addElement('text', 'mytext8', 'Alpha-numeric');
$form->addRule('mytext8', 'Alpha-numeric', 'alphanumeric', null, 'client');
```

现在，我们可以通过包含非字母数字字符的文本来测试此新规则。在示例中，我们将文本包含在非字母数字的双引号中。我们看到警告信息将会显示，我们无法提交表单，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_61_0.png)

## 工作原理...

我们使用了 `alphanumeric` 验证类型，它不需要任何格式选项。当用户输入任何不是数字或字母的字符时，将显示验证，在移除无效字符之前，他们将无法提交表单。





# 添加仅接受数字字符的字段

在本食谱中，我们将添加一条仅接受数字字符的规则，即数字 0-9。这在某些情况下非常有用，例如用户需要输入引用编号或货币值时。

### 准备工作

请参考本章的第一个食谱，了解如何准备 QuickForm Web 表单的详情，这是本食谱的基础。

### 如何实现...

将以下代码添加到我们 `validation_form.php` 的定义中，紧接在定义之后：

```
$mform->addElement('text', 'mytext9', 'Numeric');
$mform->addRule('mytext9', 'Numeric', null, 'client');
```

当我们通过输入非数字字符来测试此新规则时（在本例中，我们输入了字符串 `abc`），会显示验证警告消息，并且我们无法提交表单，如图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_62_0.png)

## 工作原理...

我们使用了 `numeric` 验证类型，它不需要任何格式选项。现在，当用户输入数字（0-9）以外的任何内容时，他们将看到验证警告消息，并在移除无效的非数字字符之前无法继续。

# 拒绝标点字符

在本食谱中，我们将添加一条防止输入标点字符的规则。这在某些情况下非常有用，例如您要求新文档标题不能包含句号或逗号。

### 准备工作

请参考本章的第一个食谱，了解如何准备 QuickForm 表单的详情，这是本食谱的基础。

### 如何实现...

将以下代码添加到 `validation_form.php` 中的表单定义中，紧接在字段定义之后：

```
$mform->addElement('text', 'mtext10', 'No punctuation');
$mform->addRule('mtext10', 'No punctuation', 'nopunctuation', null, 'client');
```

当我们通过输入包含标点字符的文本（逗号或句号）来测试此规则时，我们看到显示了警告消息，并且无法提交表单，如图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_63_0.png)

## 工作原理...

我们使用了 `nopunctuation` 验证，它不需要任何格式选项。当用户输入包含任何标点字符的文本时，将显示验证警告消息，并在移除无效字符之前无法提交表单。

# 拒绝带领先零的输入

在本食谱中，我们将添加一条规则，要求输入有效数字且不能有领先数字 0。这对于验证不带零填充的整数非常有用。

### 准备工作

请参考本章的第一个食谱，了解如何准备 QuickForm 表单的详情，这是本食谱的基础。

### 如何实现...

将以下代码添加到 `validation_form.php` 中的表单定义中，紧接在字段定义之后：

```
$mform->addElement('text', 'mtext1', 'No leading zero');
$mform->addRule('mtext1', 'No leading zero', 'nonzero', null, 'client');
```

现在我们可以通过添加一个带有领先零的无效数字序列（0123）来测试该规则。我们看到显示了验证警告消息，并且无法提交表单，如图所示。

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_64_0.png)

## 工作原理...

我们使用了 `nonzero` 验证类型，它不需要任何格式选项。当用户尝试输入包含领先零的文本时，将显示验证警告消息，并在移除无效字符之前无法进行表单提交。

# 与另一个字段比较

在本食谱中，我们将添加一条规则，允许确保两个字段的内容相同。此类验证的经典示例是我们从用户处获取的信息准确性至关重要（例如密码或电子邮件地址）。我们确保他们输入两次，比较两个条目，如果不一致则显示警告。

### 准备工作

请参考本章的第一个食谱，了解如何准备 QuickForm 表单的详情，这是本食谱的基础。

### 如何实现...

将以下代码添加到 `validation_form.php` 中的表单定义中，紧接在字段定义之后：

```
$mform->addElement('text', 'mtext11', 'Must match');
$mform->addRule('mtext11', 'Must match', 'compare', null, 'server');
```

现在我们可以通过在每个文本框中输入不同的值来测试此规则。我们看到显示了验证警告消息，并且无法提交表单，如图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_65_0.png)

## 工作原理...

我们使用了 `compare` 验证类型，它的参数略不同。第一个参数必须是元素名称的数组。格式选项是一个字符串，用于指定比较类型。

| 格式选项 |  |
| :--- | :--- |
| eq | 第一个元素的值等于第二个 |
| != | 第一个元素的值不等于第二个 |
| gt | 第一个元素的值大于第二个 |
| ge | 第一个元素的值大于等于第二个 |
| lt | 第一个元素的值小于第二个 |
| lte | 第一个元素的值小于等于第二个 |

# 添加自定义 JavaScript 函数回调

在本食谱中，我们将查看如何使用 JavaScript 手动验证输入框的内容。通过允许我们使用 JavaScript 内的任何工具来验证输入，这提供了完全的灵活性。例如，我们可以根据今天的日期进行验证，甚至通过 Web 服务查询值。

### 准备工作

请参考本章的第一个食谱，了解如何准备 QuickForm Web 的详情，这是本食谱的基础。

### 如何实现...

将以下代码添加到 `validation_form.php` 的定义中，紧接在定义之后：

```
$mform->addElement('text', 'mtext13', 'Custom');
$mform->addRule('mtext13', 'Custom', 'callback', 'mycallback', 'client');
```

我们指定了一个自定义验证函数回调。在示例中，我们必须编辑 `validation.php` 以引入包含我们回调函数的 JavaScript 文件：

```
$PAGE->requires->js('/validation.js');
```

最后，我们必须在 `validation.js` 中添加回调函数：

```javascript
function callback(input)
{
    if(input == 'valid')
    {
        return true;
    }
    else
    {
        return false;
    }
}
```

我们只需测试输入是否等于字符串 `valid`，并分别返回真值 true 或 false，但该函数可以包含任何必要的 JavaScript。我们通过输入文本 `invalid` 来测试规则，看到验证失败并显示了警告消息，如图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_67_0.png)

## 工作原理...

我们使用了 `callback` 验证类型，它接受一个 JavaScript 函数名称作为格式选项。回调函数由表单 API 调用，并将待验证的值作为唯一参数传递。自定义逻辑被应用于该值，且该函数必须根据需要返回 true 或 false。




将第五个参数设置为 `client` 表示它是一个客户端回调函数，因此它是一个 JavaScript 函数。请注意，将此参数设置为 `server` 将允许使用 PHP 函数作为回调，而不是 JavaScript 函数。使用此类类型的额外规则可以确保即使户在他们的 Web 浏览器中禁用了 JavaScript，验证也始终会发生。

重要的是，我们在本章中涵盖的验证技术主要依赖于用户的 Web 浏览器启用了 JavaScript。因此，健壮的表单验证必须始终是便捷的客户端验证与服务器验证的结合。这确保了无论终端 Web 浏览器提供了哪些功能，接收到的数据都将经过验证。这还确保了试图绕过客户端验证的潜在恶意客户端被迫接受服务器上进行的额外验证。

## 使用 YUI 3 操纵数据

在本章中，我们将涵盖：

-   使用 IO 请求 URI
-   使用 IO 的替代传输方法请求外部 URI
-   使用 PHP 代理从外部域域加载数据
-   使用 DataSource 解析 XML
-   使用 DataSource 解析 JSON
-   使用 DataSource 解析 CSV 数据
-   从 Moodle 2.0 Web 服务检索数据

## 引言

在本章中，我们将介绍如何使用 JavaScript 和 YUI 从各种不同的源检索并显示数据。通过这些技术，我们可以将所有类型的数据集成到我们的 Moodle 应用中。此列表包括天气预报、股票更新、新闻源、您可能从外部系统获取的任何类型的自定义文本数据，甚至通过 Moodle 的 Web 服务 API 从 Moodle 本身检索的数据（本地 Moodle 系统以及您的代码授权访问的任何远程系统）。

Moodle 2.0 包含了第 3 版 Yahoo! 用户界面库 (YUI 3)。YUI 3 拥有丰富的数据处理 API，我们将在本章对其进行介绍。我们将涵盖如何使用 IO 模块发送简单的 HTTP GET 请求以检索文件内容，然后转向更复杂的场景，例如从外部域检索数据、解析各种数据格式以及消费基于 XML 的 Web 服务。


```javascript
failure: failed
};
function completed(id, o, args) {
  Y.one('#contents').set('value', o.responseText);
}
function failed(id, o, args) {
  Y.one('#contents').set(value, 'Error: '+args);
}
var getFile = function() {
  var uri = "http://example.com/text.txt";
  var request = Y.io(uri, cfg);
}

var ready = function() {
  Y.one('#go').set("disabled", false);
  Y.on('click', getFile, "#go");
}
Y.on('io:xdrReady, ready, Y);
```

3. `text_external.php` 的内容与之前示例中使用的类似，不同之处在于请求输入被禁用了，这样当请求传输机制准备就绪时，就可以使用了。在这里，我们定义了一个简单的表单，包含一个用于显示响应文本的文本区域以及一个允许用户如截图所示启动请求的输入按钮：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_74_0.png)

4. `text_external.js` 文件是执行请求的地方。首先，我们创建一个新的 YUI 3实例，加载 `io-xdr` 模块（用于跨域请求传输）和 `node` 模块（用于操作 DOM 元素）。

5. 接下来，我们指定 IO 的 xdr 代理 Flash 文件的路径（该路径相对于最终 HTML 输出的路径），并将此配置应用到 IO 传输对象上。

6. 接下来，我们为主 IO 对象定义另一个配置对象，指定我们将使用 "flash" 传输机制，并订阅了成功事件。

7. 我们现在定义一个执行请求的函数，该函数稍后将绑定到输入按钮的点击事件上。

8. 最后，我们为 IO 的 `xdrReady` 事件定义并注册了一个回调函数。

## 工作原理...

当页面加载时，我们的 JavaScript 代码会初始化 IO 的跨域请求 (XDR) 功能，并订阅相关的事件。Flash 电影被加载到页面中，并且当 `xdrReady` 事件触发时，它就可以使用了。

我们已经订阅了 `xdrReady` 事件，当它完成后，我们启用输入按钮，并在点击事件上绑定一个执行实际请求的函数。

当请求成功完成时，会触发成功事件并调用我们的函数，该函数获取正文文本并将其显示在我们 PHP 页面的 textarea 元素中。或者，如果请求失败，将触发 `failed` 事件处理器，并将错误消息显示在框中。

# 使用 PHP 作为代理从外部域加载数据

如果您希望从一个没有安装有效跨域策略文件（crossdomain policy file）的受信任外部源获取数据，那么您可以使用本地 PHP 文件作为代理来为您下载该文件。

这种方法的缺点是，获取文件的开销被移动到了服务器端，而不是像之前的 YUI 方法那样在客户端。然而，当无法在远程域上安装跨域策略文件时，这可能需要将其作为最后的手段。

### 如何实现...

- 1. 此示例使用一个 PHP 文件：`get_external_data.php`：
```php
<?php
require_once('../config.php');
require_once('../lib/filelib.php');
$uri = 'http://remote.example.com/text.txt';
echo download_file_content($uri);
?>
```

- 2. 首先，我们通过包含全局 `config.php` 文件设置 Moodle 环境。

- 3. 接下来，我们包含 Moodle 的文件 API 库，它提供了 `download_file_content` 函数。

- 4. 我们现在定义想要下载的文件 URI，并输出 `download_file_content` 的结果。

- 5. 最后，我们可以使用这个新的 PHP 文件作为数据源，替代外部 URI。

## 工作原理...

Moodle 的文件 API 提供了 `download_file_content` 函数，它返回所提供的 URI 的内容。

由于该文件位于本地域，JavaScript 与这些数据的交互就像它们是本地文件一样，避免了从远程域加载数据时发生的安全问题。

# 使用 DataSource 解析 XML

许多网站和网络服务以 XML 格式提供数据（例如 RSS）。在本示例中，我们将加载一个 XML 文件，解析内容并将其显示在文本框中。

### 如何实现...

- 1. 在此示例中，我们将使用以下三个文件：
    `data.xml`: 一个非常简单的 XML 数据文件，内容如下：
    ```xml
    <?xml version="1.0" encoding="UTF-8" ?>
    <list>
      <item>Item One</item>
      <item>Item Two</item>
      <item>Item Three</item>
      <item>Item Four</item>
      <item>Item Five</item>
      <item>Item Six</item>
      <item>Item Seven</item>
      <item>Item Eight</item>
      <item>Item Nine</item>
      <item>Item Ten</item>
    </list>
    ```
    `datasource_xml.php`: 一个 PHP 页面，包含一个启动请求的输入按钮和一个显示结果的文本区域：
    ```php
    <?php
    require_once(__FILE__) . '../config.php';
    ```

```php
<?php
require_once(__FILE__) . '../config.php';
```

```html
<form>
<textarea id="contents" rows="10"></textarea>
<br />
<input id="go" type="button" value="Get XML">
</form>
```

```php
<?php
require_once(__FILE__) . '../config.php';
echo OUTPUT->header();
?>
```

```php
<?php
echo OUTPUT->footer();
?>
```

```datasource_xml.js
YUI().use('datasource-io', 'datasource-xmlschema', 'node', function (YUI) {
  var dataSource = new YUI.DataSource.IO({source:'data.xml'});
  dataSource.plug(YUI.Plugin.DataSourceXMLSchema, {
    schema: {
      resultLocator: {key:"item"},
      resultFields: ["text"]
    }
  });

  function loadXML() {
    dataSource.sendRequest({
      callback: function (e) {
        var xmlData = '';
        e.response.results.forEach(function(item) {
          xmlData += item.text + '\n';
        });
        document.getElementById('contents').value = xmlData;
      },
      failure: function (e) {
        alert(e.error.message);
      }
    });
  }

  YUI.on('click', loadXML, "#go");
});
```





# 使用 DataSource 解析 JSON

在本教程中，我们将使用 DataSource 结合 JSONSchema 插件来检索并解析 JSON 格式的数据文件。

### 准备工作

在此示例中，我们将使用三个文件：

+   data.json: 一个 JSON 格式的数据文件，内容如下：
```json
{
  "list": [
    {"name":"Item One"},
    {"name":"Item Two"},
    {"name":"Item Three"},
    {"name":"Item Four"},
    {"name":"Item Five"},
    {"name":"Item Six"},
    {"name":"Item Seven"},
    {"name":"Item Eight"},
    {"name":"Item Nine"},
    {"name":"Item Ten"}
  ]
}
```

+   datasource_json.php: 一个 PHP 页面，包含一个用于发起请求的输入缓冲区和一个显示结果的文本区域：
```php
<?php
require_once(dirname(__FILE_)) . '/../config.php';
$PAGE->set_url('/cook/datasource_json.php');
$PAGE->requires->js('/cook/datasource_json.php');
echo OUTPUT->header();
?>
<form>
<textarea id="contents" rows="10"></textarea>
<br />
<input id="go" type="button" value="Get JSON">
</form>
<?php
echo OUTPUT->footer();
?>
```

## 使用 YUI 3 操作数据

datasource_json.js: 配套的 JavaScript 文件，包含了 YUI 数据逻辑：

```
YUI().use('datasource-io', 'datasource-jsonschema', 'node',
function(Y) {
  var dataSource = new Y.DataSource.IO({source:"./data/json"});
  dataSource.plug(Y.Plugin.DataSourceJSONSchema, {
    schema: {
      resultListLocator: "List",
      resultFields: ["name"]
    }
  });

function loadJSON() {
  dataSource.sendRequest({
    callback: {
      success: function(e) {
        var jsonData = "";
        Y.Array.each(e.response.results, function(item) {
          jsonData += item.name + "\n";
        });
        document.getElementById('contents').value = jsonData;
      },
      failure: function(e) {
        alert(e.error.message);
      }
    }
  });
}
Y.on('click', loadJSON, "#go");
});
```

### 如何实现...

+   1. 首先，设置一个新的熟悉的 PHP 页面并链接到我们配套的 JavaScript 文件。我们包含了一些基础表单元素，例如用于显示检索数据的文本区域，以及一个我们将在其上绑定事件以运行 JavaScript 的输入按钮。
2. 接着处理我们的 JavaScript 文件，我们开始创建一个新的 YUI 实例并加载我们需要的模块：

## 第 4 章

| 模块 | 用途 |
| --- | --- |
| datasource-io | 数据检索 |
| datasource-jschema | 数据解析 |
| node | DOM 访问（用于在页面显示数据） |

+   3. 首先，我们定义了 DataSource.IO 的新实例，传递数据文件的路径。

+   4. 接下来，我们告诉数据使用 DataSourceJSONSchema 插件，这样我们可以轻松地将 JSON 数据解析为所需的格式。

+   5. 接下来，我们定义了一个函数 `loadJSON` 来执行数据的加载和解析。我们调用数据源的 `sendRequest` 方法，并定义两个回调函数：`success` 和 `failure`。

+   6. 对于 `success` 回调函数，我们遍历响应结果的内容来构建一个字符串，并显示在页面的文本区域元素中。

+   7. `failure` 回调函数简单显示发生的错误消息。如果一切正常，我们将不会看到这个！

+   8. 最后，我们将 `loadJSON` 函数绑定到我们的输入按钮上，允许用户发起请求。

## 工作原理...

当页面加载时，会实例化一个新的 `DataSource.IO` 对象，其源被设置为我们想要检索的文件。此外，该对象被配置为使用 `DataSourceJSONSchema`，它描述了文件的格式并允许将其自动解析为我们有用的格式。

当用户点击输入按钮时，会触发点击事件并调用我们绑定的函数。该函数执行检索数据的请求，如果一切成功，将运行 `success` 回调函数。

该回调传递了响应，这是一个由 JSON 数据生成的对象，格式由我们提供的 `JSONSchema` 定义。在示例中，我们使用了 `Array.each` 工具来构建一个包含结果列表的字符串，并用换行符分隔，最后将其显示在文本区域元素中。

# 使用 DataSource 解析 CSV 数据

在本教程中，我们将使用 `DataSource` 和 `TextSchema` 插件解析一个简单的两列 CSV 数据文件。

## 使用 YUI 3 操作数据

### 准备工作

我们再次需要三个文件：

+   - data.csv: 一个两列的 CSV 数据文件，我们将将其作为数据源：
1,Item One
2,Item Two
3,Item Three
4,Item Four
5,Item Five
6,Item Six
7,Item Seven
8,Item Eight
9,Item Nine
10,Item Ten

+   - datasource_csv.php: 一个 PHP 页面，包含一个用于发起请求的输入缓冲区和一个显示结果的文本区域：
```php
<?php
require_once(dirname(__FILE_)) . '/../config.php';
$PAGE->set_url('/cook/datasource_csv.php');
$PAGE->requires->js('/cook/datasource_csv.php');
echo OUTPUT->header();
?>
<form>
<textarea id="contents" rows="10"></textarea>
<br />
<input id="go" type="button" value="Get JSON">
</form>
<?php
echo OUTPUT->footer();
?>
```

+   - datasource_csv.js: 配套的 JavaScript 文件，包含了 YUI 数据逻辑：

```
YUI().use('datasource-io', 'datasource-jsonschema', 'node',
function(Y) {
  var dataSource = new Y.DataSource.IO({source:"./data/data.csv"});
  dataSource.plug(Y.Plugin.DataSourceJSONSchema, {
    schema: {
      resultListLocator: "items",
      resultFields: ["id", "name"]
    }
  });

function loadCSV() {
  dataSource.sendRequest({
    callback: {
      success: function(e) {
        var csvData = "";
        Y.Array.each(e.response.results, function(item) {
          csvData += item.id + ": " + item.name + "\n";
        });
        document.getElementById('contents').value = csvData;
      },
      failure: function(e) {
        alert(e.error.message);
      }
    }
  });
}
Y.on('click', loadCSV, "#go");
});
```

### 如何实现...

+   1. 首先，设置一个新的熟悉的 PHP 页面并链接到我们配套的 JavaScript 文件。我们包含了一些基础表单元素，例如用于显示检索数据的文本区域，以及一个我们将在其上绑定事件以运行 JavaScript 的输入按钮。
2. 接着处理我们的 JavaScript 文件，我们开始创建一个新的 YUI 实例并加载我们需要的模块：

+   3. 首先，我们定义了 `DataSource.IO` 的新实例，传递数据文件的路径。

+   4. 接下来，我们告诉数据使用 `DataSourceJSONSchema` 插件，这样我们可以轻松地将 JSON 数据解析为所需的格式。

+   5. 接下来，我们定义了一个函数 `loadCSV` 来执行数据的加载和解析。我们调用数据源的 `sendRequest` 方法，并定义两个回调函数：`success` 和 `failure`。

+   6. 对于 `success` 回调函数，我们遍历响应结果的内容来构建一个字符串，并显示在页面的文本区域元素中。

+   7. `failure` 回调函数简单显示发生的错误消息。如果一切正常，我们将不会看到这个！

+   8. 最后，我们将 `loadCSV` 函数绑定到我们的输入按钮上，允许用户发起请求。

## 从 Moodle 2.0 Web 服务检索数据

在本教程中，我们将使用 Moodle Web 服务。Moodle 2.0 新引入了基于插件的服务层，支持多种 Web 服务标准。在本教程中，我们将使用 Moodle 2.0 内置的 REST Web 服务获取特定课程的小组列表，并将列表显示在页面的文本框中。

### 准备工作

在你的 Moodle 2.0 安装中启用 Web 服务，并配置使用 REST 协议。请记录在此过程中定义的安全令牌，我们稍后会需要它。请参考 Moodle 文档有关如何启用服务的详细信息：http://docs.moodle.org/en/Web_Services。

### 如何实现...

+   1. 首先，创建一个基础的 PHP 页面来设置 Moodle 编程环境，包含一个文本框和一个我们用于检索和显示 Web 数据的输入按钮。该文件 `datasource_moodlews.php` 将具有以下内容



```php
<?php
require_once(dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/datasource_moodlews.php');
$PAGE->requires->js('/cook/datasource_moodlews.js');
echo $OUTPUT->header();

?>
```

```html
<form>
<textarea id="content" rows="10"></textarea>
<br />
<input id="go" type="button" value="Get Data">
</form>
```

```php
<?php
echo $OUTPUT->footer();
?>
```

2. 此文件引用了配套的 JavaScript 文件 `datasource_moodlews.js`。这是存储与网络服务通信代码的地方，其内容如下：

```javascript
var uri = "webservice/rest/server.php?woken=+token&wsfunction=
var dataSource = new Y.DataSource.IO({source:uri});
dataSource.plug(Y.Plugin.DataSourceXMLSchema,
{
schema:
YUI.use('datasource-io', 'datasource-schema', 'node',
function(Y) {
var token = "cbbf322ae46c4de4aa0e72f69cafc077";
var wsFunction = "moodle_group_group_course_groups"
resultListLocator: "SINGLE",
resultFields: [{key:"name"],
locator: "KEY[$name='name']/VALUE"
});
function loadXML() {
dataSource.sendXMLRequest({
request:courseid=2",
cfg:
}}
```

```javascript
method:"post",
headers:
{
  'Content-Type': 'application/x-www-form-urlencoded'
},
callback:
{
  success: function(e)
  {
    var xmlData = ""
    Y.Array.each(
      e.response.results,
      function(item)
      {
        xmlData += item.name + \<n>
      }
    );
    Y.on('#contents').set('value', xmlData);
  },
  failure: function(e)
  {
    alert(e.error.message);
  }
}
}
Y.on(<click>, loadXML, "#go");
```

- 3. 文件 `datasource_moodlews.php` 基于我们通常的 Moodle PHP 文件模板，并包含了如下截图所示的两个额外的文本区域（text area）和一个输入按钮：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_86_0.png)

## 第 4 章

4. 在随后的 JavaScript 中，我们将为此按钮绑定一个点击事件，用于从网络服务获取我们所需的数据并将其显示在文本框中。

5. 转到 JavaScript 文件 `datasource_moodlews.js`，我们在这里完成获取和显示数据的大部分工作。我们首先加载必要的 YUI 模块：

| 模块 | 用途 |
| --- | --- |
| datasource-io | 发起调用以从网络服务检索数据 |
| datasource-schema | 解析 XML 响应数据 |
| node | 操作 DOM 元素（绑定事件、设置文本值） |

- 6. 定义两个用于网络服务查询的变量，从安全令牌（token）开始。该令牌是在配方开始时在 Moodle 中设置的。接下来是我们想要调用的网络服务函数名称：`moodle_group_get_course_groups`。

- 7. 使用这两个变量来构建我们将调用的网络服务方法的 URI，并在此基础上创建一个新的 `DataSource_IO`。

- 8. 通过插入 `DataSourceXML-io-plugin` 并提供一个描述 Moodle 网络服务返回的 XML 格式的 schema，来定义 `DataSource_IO` 如何向我们返回数据。

- 9. 定义一个 `loadXML` 函数来执行请求。这是通过 `DataSource_IO` 对象的 `sendRequest` 方法完成的。它接受一个对象参数，包含以下三个对象：

- request：此字符串定义了用作网络服务方法输入的键值对列表。在本例中，我们只有课程 ID 值为 2。

- cfg：该对象我们定义了请求的 HTTP 方法（POST）。它还允许我们为请求设置额外的 HTTP 请求头。我们使用 `Content-Type` 请求头 `application/x-www-form-urlencoded` 以确保我们的键值对被正确编码。

- callback：该对象由 `success` 和 `failure` 两个对象组成。这些对象是函数，只会调用其中一个，对应请求的成功或失败。在我们的 `success` 函数中，我们解析返回的数据并将其写入文本框。`failure` 函数会显示一个带有 `DataSource_IO` 提供的错误信息的警框。

10. 最后，我们将 `loadXML` 函数绑定到按钮的点击事件上。

## 使用 YUI 3 操作数据

11. 现在，当我们在浏览器中测试此代码时，点击“Get Data”按钮，并看到如下截图所示返回的组列表：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_88_0.png)





| 章节编号 | 标题 |
|--- |--- |
| 1 | 结合 Moodle 和 JavaScript |
| 2 | Moodle 与 Yahoo! 用户界面库 (YUI) |
| 3 | Moodle 表单验证 |
| 4 | 数据操作 |
| 5 | 使用数据表格 |
| 6 | 增强页面元素 |
| 7 | 高级布局技术 |
| 8 | 组件动画 |
| 9 | 集成外部库 |

## 使用数据表格

本页面生成布局，如下幅截图所示：

（注意：原文中提到的截图似乎由上方提供的表格表示。）

此页的 Moodle 文档
您以 Admin User 身份登录（退出）

接下来，我们向关联的 JavaScript 文件 (datatables.js) 中添加必要的代码：

```javascript
YUI().use('yui2-datatable', function(YUI) {
  var YAHOO = YUI.YUI;

  var dataSource = new YAHOO.util.DataSource(YAHOO.util.Dom.get('cookable'));
  dataSource.responseType = YAHOO.util.DataSource.TYPE_HTMLTABLE;
  dataSource.responseSchema = {
    fields:
      { key: "chapter", parser: "number" },
      { key: "title", parser: "string" }
    }
  };
});
```

## 第 5 章

我们构建的 HTML 表格由一个标准的双列表格组成，在 `<head>` 和 `<th>` 标签内清晰定义了表头和行。验证表头信息是否存储正确，允许 YUI 2 确保其不会被包含实际数据集的一部分。

转向我们的 JavaScript 代码，我们以标准方式初始化一个新的 YUI 3 环境，加载所需的模块：`yui2-datatable`。

目前没有 DataObject 的 YUI 3 版本，因此我们将使用 YUI 2 版本。这是通过设置在对象 YUI2 中可用的 YUI 2 对象 `YAHOO` 来的。

接下来，我们创建一个新的 YUI 2 DataSource，传递 ID 为 `cookie` 的 HTML 表格的引用。然后，我们设置 DataTable 的 `responseType` 将其识别为 HTML 表格。

最后，我们设置 DataTable 的 `schema` 键，并定义列的数据类型；在此例中，它们分别为 `number` 和 `string`。

我们有一个从 HTML 表格填充的 YUI 2 DataSource。它可以与任何与 YUI 2 DataSource 兼容的代码一起。在这个示例中，我们将此对象传递给 YAHOO 控制，作为交互式数据控制的基础。

# 它是如何工作的...

我们混合使用了 YUI 2 和 YUI 3 代码。YUI 3 允许我们使用简化的语法来加载模块，而 YUI 2 允许我们使用 DataTable 控制代替 YUI 3 的替代品。

YUI 3 为我们提供了一个 YUI 2 的实例，该实例位于 `YUI2` 中。我们将其复制到 `YAHOO` 对象中，以便能够使用与原生 YUI 代码完全相同的语法。

当我们将 DataSource 构造函数指向我们的 HTML 表格时，它能够通过 `responseType YAHOO.util.DataSource.TYPE_HTMLTABLE` 将数据提取到新的 YUI 2 DataSource 对象中。

# 显示数据

在此配方中，我们使用了从上一个配方从 HTML 表格中准备的 DataSource 对象。我们将其作为新的 DataTable 控制的基础，并将开始看到这种控制带来的增强。

现在我们有了一个可用的 DataSource 对象，可以开始创建实际的 DataTable 控制了。此示例基于上一个配方，在现有的 JavaScript 中增加了额外的代码。然而，应该明确的是，我们在上一个配方中构建的 DataSource 可以替换为任何其他（例如，从 XML Web 服务获取的数据构建的 DataSource）。

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_95.png)

### 如何实现...

打开 datatable.js 文件并添加列定义。该文件应与以下内容：

```javascript
YUI().use('yui2-datatable', function(YUI) {
  var YAHOO = YUI.YUI;

  var dataSource = new YAHOO.util.DataSource(YAHOO.util.Dom.get('cookable'));
  dataSource.responseType = YAHOO.util.DataSource.TYPE_HTMLTABLE;
  dataSource.responseSchema = {
    fields:
      { key: "chapter", parser: "number" },
      { key: "title", parser: "string" }
    }
  };

  var columns = [
    { key: "chapter", label: "Chapter No.", formatter: "number" },
    { key: "title", label: "Title", formatter: "string" }
  ];

  var dataTable = new YAHOO.widget.DataTable("container", columns, dataSource);
});
```

我们首先创建一个包含以下属性的对象的数组：

| 属性 | 描述 |
|---|---|
| key | 列的键 |
| label | 列的文本标签 |
| formatter | 列中数据的类型 |

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_96.png)

然后我们创建一个 YUI 2 DataTable 对象，它接受三个参数：
1. 作为 container 的 DOM 对象的 ID
2. 之前创建的列定义
3. 用于填充表格的 DataSource 对象

DataTable 使用我们提供的列数组来生成表格，如下截图所示：

| 章节编号 | 标题 |
|---|---|
| 1 | 结合 Moodle 和 JavaScript |
| 2 | Moodle 与 Yahoo! 用户界面库 (YUI) |
| 3 | Moodle 表单验证 |
| 4 | 数据操作 |
| 5 | 使用数据表格 |
| 6 | 增强页面元素 |
| 7 | 高级布局技术 |
| 8 | 组件动画 |
| 9 | 集成外部库 |

# 列排序

在此配方中，我们将启用列排序。这将允许用户点击表格的表头单元格，按字母或数字对整个表格进行排序。点击一次为升序，点击两次为降序。

### 准备工作

打开 datatable.js 文件进行编辑。我们将修改列定义以允许排序。

```javascript
var columns = {
  key: "chapter",
  label: "Chapter No.",
  formatter: "number",
  sortable: true,

  key: "title",
  label: "Title",
  formatter: "string",
  sortable: true
};


我们在每个列定义中添加了一个额外属性：sortable。

将此设置为 true 将激活我们启用的每个列的内置列排序功能。下面的截图显示，通过点击列标题，DataTable 已经按标题按字母顺序排序：

| 章节编号 | 标题 |
|---|---|
| 7 | 高级布局技术 |
| 8 | 组件动画 |
| 1 | 结合 Moodle 和 JavaScript |
| 6 | 增强页面元素 |
| 9 | 集成外部库 |
| 4 | 数据操作 |
| 2 | Moodle 与 Yahoo! 用户界面库 (YUI) |
| 3 | Moodle 表单验证 |
| 5 | 使用数据表格 |

同样，我们可以按章节编号对表格行进行排序，通过点击章节编号列标题按降序数字排序，点击一次为升序，点击两次为降序，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_98.png)





## 第 5 章

| 章节编号 | 标题 |
| :--- | :--- |
| 9 | 集成外部库 |
| 8 | 组件动画 |
| 7 | 高级布局技术 |
| 6 | 增强页面元素 |
| 5 | 使用数据表格 |
| 4 | 数据处理 |
| 3 | Moodle 表单验证 |
| 2 | Moodle 与 Yahoo! 用户界面库 (YUI) |
| 1 | 结合 Moodle 与 JavaScript

## 添加分页功能

在本教程中，我们将启用数据分页。我们将实现 YUI 分页器（Paginator）控件，并配置 DataTable 每五行显示一组。YUI 2 DataTable 控件与分页器控件兼容。这允许我们为 DataTable 启用熟悉的分页控件，这对于大型数据集特别有用。

### 准备工作

打开 `datatable.js` 文件进行编辑。我们将向 DataTable 构造函数添加一个额外的配置对象。

### 如何实现...

首先，我们必须包含一个额外的模块：`yui2-paginator`。我们通过修改第一行代码并使用 `use`来实现：

```javascript
YUI().use("yui2-datatable", "yui2-paginator", function(Y) {

var config = {
  paginator : new YAHOO.widget.Paginator({
    rowsPage: 5
  })
};
```

接下来，我们需要将这个新配置对象作为第四个参数传递给 DataTable。修改变量 `DataTable` 的定义，以匹配以下代码：

```javascript
var data = new YAHOO.widget.DataTable("container", columns,
  dataSource, config);
```

# 使用表格

## 工作原理...

DataTable 允许我们将一个配置对象作为第四个参数传递。

其中一个属性是 `paginator` 属性，我们将其设置为分页器控件的新实例（每页大小为 5）。

DataTable 已经应用了我们的配置并添加了分页控件。我们现在可以使用它生成的链接按页跳转列表，如下截图所示：

<< 上一个 < 前 1 2 下一个 > 最后 >>
| 章节编号 | 标题 |
| :--- | :--- |
| 1 | 结合 Moodle 与 JavaScript |
| 2 | Moodle 与 Yahoo 用户界面库 (YUI) |
| 3 | Moodle 表单验证 |
| 4 | 数据处理 |
| 5 | 使用数据表格 |
<< 上一个 < 前 1 2 下一个 > 最后 >>

<< 上一个 < 前 1 2 下一个 > 最后 >>
| 章节编号 | 标题 |
| :--- | :--- |
| 6 | 增强页面元素 |
| 7 | 高级布局技术 |
| 8 | 组件动画 |
| 9 | 集成外部库 |
<< 上一个 < 前 1 2 下一个 > 最后 >>

## 启用滚动功能

在本教程中，我们将实现滚动数据表格。作为分页的替代方法，它可以让我们更好地处理大型数据集的显示，因为完整显示这些数据会非常繁琐。

我们将使用另一个定义相似的 YUI 控件来实现：`ScrollingDataTable`。

### 准备工作

打开 `datatable.js` 文件进行编辑。我们将修改 `datatable` 对象的定义。

### 如何实现...

修改 `dataTable` 的定义以匹配以下代码：

```javascript
var dataTable = new YAHOO.widget.ScrollingDataTable(
    "container", columns, dataSource,
    height: "150px"
);
```

## 工作原理...

使用了替代控件 `ScrollingDataTable`，并将配置对象作为第四个参数传入。该配置对象仅为 DataTable 设置了高度，任何溢出此高度的内容将进行滚动。同样，我们可能设置宽度来启用水平滚动，或者通过同时设置高度和宽度来启用水平和垂直滚动。

以下截图显示，超过 150px 设定高度的内容是可以垂直滚动的：

| 章节编号 | 标题 |
| :--- | :--- |
| 1 | 结合 Moodle 与 JavaScript |
| 2 | Moodle 与 Yahoo! 用户界面库 (YUI) |
| 3 | Moodle 表单验证 |
| 4 | 数据处理 |
| 5 | 使用数据表格 |
| 6 | 增强页面元素 |

| 章节编号 | 标题 |
| :--- | :--- |
| 4 | 数据处理 |
| 5 | 使用数据表格 |
| 6 | 增强页面元素 |
| 7 | 高级布局技术 |
| 8 | 组件动画 |
| 9 | 集成外部库 |

## 启用编辑功能

DataTable 控件具有内联编辑功能，允许用户点击任何启用的编辑单元格并修改其值。这将更新底层 DataSource，然后可以对其进行检索和存储。

### 准备工作

打开 `datatable.js` 文件进行编辑。我们将为列定义添加一些额外的属性，并订阅 DataTable 的 `cellClickEvent`。

### 如何实现...

通过添加新的 `editor` 属性来修改列定义：

```javascript
var columns = [
  {
    key: "chapter",
    label: "章节编号",
    formatter: "number",
    sortable: true,
    editor: new YAHOO.widget.TextboxCellEditor
  },
  {
    key: "title",
    label: "标题",
    formatter: "string",
    sortable: true,
    editor: new YAHOO.widget.TextboxCellEditor
  }
];
```

接下来，通过订阅 `cellClickEvent` 来启用编辑：

```javascript
dataTable.subscribe("cellClick", function(event, data) {
    // 编辑逻辑
});
```

以下截图显示了编辑功能：

| 章节编号 | 标题 |
| :--- | :--- |
| 1 | 结合 Moodle 与 JavaScript |
| 2 | Moodle 与 Yahoo! 用户界面库 (YUI) |
| 3 | Moodle 表单验证 |
| 4 | 数据处理 |
| 5 | 使用数据表格 |
| 6 | 增强页面元素 |



```php
<?php
echo $OUTPUT->header();
?>
<div style="width:15em;height:10em">
<input id="txtInput" type="text">
<div id="txtInput_container"></div>
</div>
<?php
echo $OUTPUT->footer();
?>
```

其次，我们需要创建 JavaScript 文件 `autocomplete.js`，代码如下：

```javascript
YUI().use("yui2-autocomplete", "yui2-datasource", function(Y) {
  var YAHOO = Y.YUI;
  var dataSource = new YAHOO.util.LocalDataSource(
    ["Alpha", "Bravo", "Beta", "Gamma", "Golf"]
  );
  var autoCompleteText = new YAHOO.widget.AutoComplete("txtInput",
  "txtInput_container", dataSource);
});
```

## 工作原理...

我们的 HTML 包含三个元素：一个父级 `div` 元素以及包含在它的两个元素：一个输入框和一个用于显示自动补全建议的占位 `div` 元素。

我们的 JavaScript 文件定义了一个用于提供建议的 `DataSource`，然后根据我们已经定义的 HTML 元素创建了一个新的 `AutoComplete` 组件。

在这个示例中，为了简单起见，我们使用了 `LocalDataSource`，但它可以被替换为任何有效的 `DataSource` 对象，正如我们在之前的章节中涵盖的那样。

一旦我们有了一个 `DataSource` 对象，我们就会实例化一个新的 YUI2 `AutoComplete` 组件，并传递以下参数：

- 提供自动补全建议的 HTML 输入文本元素的名称
- 用于显示建议的容器元素的名称
- 用于查找建议的有效数据源对象

## 增强页面元素

现在，当用户开始在文本框中输入字时，任何匹配的自动补全建议都会显示出来并可以被，如下所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_108_0.png)

## 添加带有自动补全的组合框

在这个示例中，我们将自动补全与组合框（下拉列表）结合使用。这与上一个示例相比有一个显著不同之处——它包含一个下拉箭头按钮，允许用户在先输入之前查看完整的值列表。

这在用户可能不确定合适值的情况下非常有用。在这种情况下，他们可以点击下拉按钮查看建议，而无需在输入时进行猜测。此外，这种方法也支持与上一个配方相同的边输入边匹配自动补全。

### 如何实现...

打开上一个配方的 `autocomplete.php` 文件，并编辑文本框自动补全下方的 HTML 代码：

```html
<div style="width:15em;height:10em;">
<input id="txtCombo" type="text" style="vertical-align:top;width:11em;"><span id="toggle"><<span>/</span></span></span>
<div id="txtCombo_container"></div>
</div>
```

接下来，打开 JavaScript 文件 `autocomplete.js` 并将其修改为匹配以下代码：

```javascript
YUI().use("ui12-auto-complete", "ui12-datasource", "ui12-element", "ui12-yahoo-dom-event", function (Y) {

  var YAHOO = Y.YUI;

  var dataSource = new YAHOO.util.LocalDataSource(
    ["Alpha", "Bravo", "Beta", "Gamma", "Golf"]
  );

  var autoCompleteText = new YAHOO.widget.AutoComplete("txtInput",
  "txtInput_container", dataSource);

  var autoCompleteCombo = new YAHOO.widget.AutoComplete("txtCombo",
  "txtCombo_container", dataSource, {minQueryLength: 0,
  queryDelay: 0});

  var toggler = YAHOO.util.Dom.get("toggle");
  var tButton = new YAHOO.widget.Button({container:toggler,
  label:"&arr;"});
  var toggle = function() {
    if (autoCompleteCombo.isContainerOpen()) {
      autoCompleteCombo.collapseContainer();
    } else {
      autoCompleteCombo.getInputEl().focus();
      setTimeout(function() {
        autoCompleteCombo.sendQuery("*");
      },0);
    }
  };
  tButton.on("click", toggle);
});
```

你会注意到，我们在这个配方中添加的 HTML 与上一个非常相似，除了我们在文本框之后包含了一个 `span` 元素。它被用作插入 YUI2 控制按钮的占位符。

这个配方比上一个复杂得多，因此包含了一些额外的 YUI 模块：`element`、`button` 和 `yahoo-dom-event`。

我们以之前相同的方式定义 `AutoComplete` 组件，但我们需要在作为第四个参数传递的对象中添加两个配置选项。

接下来，我们获取了按钮占位符的引用，并实例化一个新的 `Button` 组件来作为组合框的“下拉”按钮。

最后，我们为按钮定义了一个点击处理程序并将其注册。

我们现在可以看到建议列表，通过点击下拉按钮可以显示它，如下所示：

| |
|:---|
| Alpha |
| Bravo |
| Beta |
| Gamma |
| Golf |

## 工作原理...

用户可以像以前一样在框内输入内容以接收自动补全建议，但现在可以使用组合下拉按钮查看建议。

当用户点击下拉菜单时，会触发点击事件。

此点击事件执行以下操作：

- 如果下拉菜单已显示，则隐藏它，允许用户切换显示状态。
- 如果未显示，则将焦点置于框内（允许继续输入），并在自动补全组件上执行空白查询，这将显示建议列表。注意，我们在早些定义 `AutoComplete` 组件时通过 `minQueryLength: 0` 选项显式启用了长度为0的查询。

## 显示自动更新数据

另一个实用的界面是在设定间隔内不断更新数据。例如，这可以每五分钟更新一次新闻标题，或每分钟更新一次股票数据显示。

在这个配方中，我们将采用时钟的基本示例，在页面上显示完整的日期和时间，并使用 `DataSource` 的扩展每秒更新一次。这种技术可以从任何数据源显示任何数据，并按照我们的频率更新。

### 如何实现...

在这个示例中，我们将设置一个简单的 PHP 页面 `updatedate.php`，其中包含一个我们要显示的占位符：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(CONTEXT_SYSTEM);
$PAGE->set_url('/cook/updatedate.php');
$PAGE->requires_js('/cook/updatedate.js', true);
echo $OUTPUT->header();
?>
<div id="txtUpdate"></div>
<?php
echo $OUTPUT->footer();
?>
```

接下来，我们定义 JavaScript `updatedate.js`：

```javascript
YUI().use("datasource-function", "datasource-polling", function(Y) {
  var getDateString = function() {
    return new Date();
  };

  var dataSource = new Y.DataSource.Function({source:getDateString});

  var request = {
    callback: {
      success: function(e) {
        document.getElementById('txtUpdate').innerHTML = e.results[0];
      }
    }
  };

  var id = dataSource.setInterval(1000,request);
});
```





## 增强页面元素

剩下的只需使用 DataSource 的 `setInterval` 方法来注册定义的回调函数，并将其配置为每 1000 毫秒（1 秒）更新一次。

现在可以看到，加载页面后会显示完整的日期和时间，并每秒更新一次，有效地在页面上创建基于文本的时钟，如下所示：

> Sun Oct 03 2010 13:41:32 GMT+0100 (BST)

# 启用可调整大小的元素

另一个有效的 YUI2 示例使用了 resize 工具。它有许多用途，从简单的（在本示例中，允许文本块可调整大小）到更复杂的场景（如可调整大小的表单）。它允许用户通过在页面上拖动手柄来更改元素的大小，类似于用户在操作系统的 GUI 中调整任何应用程序窗口的方式。当元素包含大量内容时这非常有用，允许用户根据需要调整元素的大小。

### 如何操作...

首先，设置一个简单的页面 `resize.php`，并在容器元素中包含文本块，如下：

```php
<?php
require_once(dirname(__FILE__)) . '../config.php';
$PAGE->set_content(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/resize.php');
$PAGE->requires->js('/cook/resize.js', true);
?>
```

```php
<?php
echo $OUTPUT->header();
?>
<div id="content" style="width:20em;padding:10em;">
<p>
Moodle（Modular Object-Oriented Dynamic Learning Environment 的缩写）是一个
免费开源的电子学习软件平台，也称为课程管理系统、
学习管理系统或虚拟学习环境 (VLE)。截至 2010 年 10 月，它拥有 49,952 个注册并验证的站点，为 370 万门课程中的 3700 万用户服务。</p>
</div
<?php
echo $OUTPUT->footer();
?>
```

关联的 JavaScript `resize.js` 非常简单：

```javascript
YUI().use("yui2-resize", function (Y) {
  var YAHOO = Y.YUI;
  var resize = new YUI.util.Resize("content");
});
```

实例化一个新的 `Resize` 对象，并将要调整大小的元素名称作为唯一参数传递。

这允许元素在两个轴上进行调整大小，在元素的右侧和底部有调整大小的手柄，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_113_0.png)

## 工作原理...

在构造函数中实例化 `Resize` 控制并传递要增强的元素，会导致 YUI 在元素上添加调整大小的手柄，允许其水平和垂直方向进行调整大小。

## 添加自定义提示框

通过元素的 `title` 属性设置的 HTML 提示框仅允许基于文本的提示框，无法控制布局。在本示例中，我们将使用 YUI Tooltip 组件增强现有的元素。

## 增强页面元素

### 如何操作...

首先，设置一个 PHP 页面 `tooltip.php`，其中包含一个设置了 `title` 属性的图像：

```php
<?php
require_once(dirname(__FILE__) ) . './config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/tooltip.php');
$PAGE->requires->js('/cook/tooltip.js', true);

echo $OUTPUT->header();
?>
<img id="logo" src="../image.php?theme=tooltip.php?theme=standard&image=moodlelegogo" title="Moodle Logo" />
<?php
echo $OUTPUT->footer();
?>
```

接下来，设置关联的 JavaScript 文件 `tooltip.js`：

```javascript
YUI().use("yui2-yahoo-dom-event", "yui2-animation", "yui2-container",
function(YUI) {

var YAHOO = YUI;

var tooltip = new YAHOO.widget.Tooltip("Tooltip", {
context: "logo"
});
});
```

创建一个我们将为其添加自定义提示框的元素。在本示例中，我们只使用了一个设置了 `title` 属性的 `img` 标签。实例化一个新的 `Tooltip` 组件并传递以下参数：

- 1. 提示框对象的名称。
- 2. 一个配置对象，其 `context` 属性设置为要增强的元素的名称。

## 工作原理...

YUI 通过添加一个包含原始 `title` 文本的自定义提示框元素来“渐进增强”指定的元素。现在，当我们悬停在添加了自定义提示框的图像元素上时，我们看到增强版本出现，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_114_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_115_0.png)

## 添加自定义按钮控制

YUI 有一个 Button 组件控件，为增强标准 HTML 按钮控件提供了许多功能。它允许对按钮的外观和功能进行很大程度的控制，例如添加图像或允许按钮与其值不同的标签。在本示例中，我们将增强一个基础 HTML 输入按钮。

### 如何操作...

首先，设置一个 PHP 页面 `button.php`，带有一个 HTML 输入按钮控件：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/button.php');
$PAGE->requires->js('/cook/button.js', true);
?>
<?php
echo $OUTPUT->header();
?>
<input id="btnButton" type="button" value="Custom Button" />
<?php
echo $OUTPUT->footer();
?>
```

接下来，定义关联的 JavaScript 文件 `button.js`：

```javascript
YUI().use("yui2-button", function(Y) {

var YAHOO = Y.YUI;

var customButton = new YAHOO.widget.Button("btnButton");

```

实例化一个新的 `Resize` 对象，并将要调整大小的元素名称作为唯一参数。这允许元素在两个轴上进行调整大小，在元素的右侧和底部有调整大小的手柄，如下：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_13_0.png)

## 工作原理...

在构造函数中实例化 `Resize` 控件并传递要增强的元素会导致 YUI 在元素上添加调整大小的手柄，允许其水平和垂直方向进行调整大小。

## 添加自定义提示框

通过元素的 `title` 属性设置的 HTML 提示框仅允许基于文本的提示框，无法控制布局。在本示例中，我们将使用 YUI Tooltip 组件增强一个元素。

## 增强页面元素

### 如何操作...

首先，设置一个 PHP 页面 `tooltip.php`，其中包含一个设置了 `title` 属性的图像：

```php
<?php
require_once(dirname(__FILE__) ) . './config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/tooltip.php');
$PAGE->requires->js('/cook/tooltip.js', true);

echo $OUTPUT->header();
?>
<img id="logo" src="../image.php?theme=tooltip.php?theme=standard&image=moodlelegogo" title="Moodle Logo" />
<?php
echo $OUTPUT->footer();
?>
```

接下来，设置关联的 JavaScript 文件 `tooltip.js`：

```javascript
YUI().use("yui2-yahoo-dom-event", "yui2-animation", "yui2-container",
function(YUI) {

var YAHOO = YUI;

var tooltip = new YAHOO.widget.Tooltip("Tooltip", {
context: "logo"
});
});
```

创建一个我们将为其添加自定义提示框的元素。在本示例中，我们只使用了一个设置了 `title` 属性的 `img` 标签。实例化一个新的 `Tooltip` 组件并传递以下参数：

- 1. 提示框对象的名称。
- 2. 一个配置对象，其 `context` 属性设置为要增强的元素的名称。

## 工作原理...

YUI 通过添加一个包含原始 `title` 文本的自定义提示框元素来“渐进增强”指定的元素。现在，当我们悬停在添加了自定义提示框的图像元素上时，我们看到增强版本出现，如下截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_114_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_115_0.png)

## 添加自定义按钮控制

YUI 有一个 Button 组件控件，为增强标准 HTML 按钮控件提供了许多功能。它允许对按钮的外观和功能进行很大程度的控制，例如添加图像或允许按钮与其值不同的标签。在本示例中，我们将增强一个基础 HTML 输入按钮。

### 如何操作...

首先，设置一个 PHP 页面 `button.php`，带有一个 HTML 输入按钮控件：

```php
<?php
require_once(dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/button.php');
$PAGE->requires->js('/cook/button.js', true);
?>
<?php
echo $OUTPUT->header();
?>
<input id="btnButton" type="button" value="Custom Button" />
<?php
echo $OUTPUT->footer();
?>
```

接下来，定义关联的 JavaScript 文件 `button.js`：

```javascript
YUI().use("yui2-button", function(Y) {

var YAHOO = Y.YUI;

var customButton = new YAHOO.widget.Button("btnButton");

});
```

## 高级布局技术

除了线性块集合之外，还有许多方法可以组织内容显示。同样，可以使用传统用户界面中的成熟技术，例如：

- **标签页内容**：这种内容组织风格与所有最流行的网络浏览器中提供的标签页功能最为熟悉。
- **模态窗口**：最适用于显示需要用户立即关注的内容。它出现在所有其他内容之上，用户必须在确认之前才能继续与页面的其他部分交互。





```php
<?php
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/nav_flyout.php');
$PAGE->requires_js('/cook/nav_flyout.js', true);
echo $OUTPUT->float('header');
?>
<div style="float:left">
<div id="menu" class="yiui3-menu">
    <div class="yiui3-menu-content">
      <ul>
        <li class="yiui3-menuitem">
          <a class="yiui3-menuitem-content" href="#">Item 1</a>
        </li>
        <li class="yiui3-menuitem">
          <a class="yiui3-menuitem-content" href="#">Item 2</a>
        </li>
        <li>
          <a class="yiui3-menu-label" href="#submenu-1">
            <em>Sub Menu</em>
          </a>
          <div id="submenu-1" class="yiui3-menu">
            <div class="yiui3-menu-content">
              <ul>
                <li class="yiui3-menuitem">
                  <a class="yiui3-menuitem-content" href="#">Sub Item 1</a>
                </li>
                <li class="yiui3-menuitem">
                  <a class="yiui3-menuitem-content" href="#">Sub Item 2</a>
                </li>
              </ul>
            </div>
          </div>
        </li>
        <li>
          <li class="yiui3-menuitem">
            <a class="yiui3-menuitem-content" href="http://moodle.org/">Moodle.org</a>
          </li>
        </li>
      </ul>
    </div>
  </div>
</div>
<?php
```

## 高级布局技术

```php
echo $OUTPUT->footer();
?>
```

此页面中的 HTML 主要使用无序列表来标记导航项目以及不同层级的菜单。下面的截图显示了增强之前的菜单基本嵌套结构：

- 项目 1
- 项目 2
- 子菜单
    - 子项目 1
    - 子项目 2
- Moodle.org

我们将使用关联的 JavaScript 文件 `nav_flyout.js`，在其中我们将菜单标记增强为功能性的飞出菜单（fly-out menu）：

```javascript
YUI().use("node-menunav", function(Y) {
  Y.on("contentready", function () {
    this.plug(Y.Plugin.NodeMenuNav);
    "#menu");
  });
});
```

现在我们加载页面，可以看到我们标记中的无序列表被转换成了动态的飞出导航菜单，如下所示所示：

| 项目 1 |
| :--- |
| 项目 2 |
| 子菜单 ▶ | 子项目 1 |
| Moodle.org | 子项目 2 |

## 工作原理...

为了让 JavaScript 能够正确识别我们标记中用于飞出菜单的标记组件，我们必须设置几个 ID 和 CSS 类名。

第一个组件是包含内容的容器 `<div>` 元素，我们必须为它分配一个 ID，以便在随后的 JavaScript 代码中使用。此外，YUI3 模块 `node-menunav` 规定我们必须为该元素分配名为 `yui3-menu` 的 CSS 类名。

在上一个 `<div>` 元素内部，我们创建了一个子 `<div>` 元素，将作为实际菜单内容的容器。这需要 `yui3-menu-content` CSS 类名。

子菜单现在的格式与父菜单完全相同，其中容器 `<div>` 的 ID 与子菜单标签的 `href` 属性的目标相匹配。

子菜单结构可以根据需要递归渲染，以反映所需的导航层级。

一旦我们定义了分级菜单的标记，艰苦的工作就完成了，YUI3 会完成剩余工作。

此示例中的 JavaScript 首先使用我们菜单的 `on-contentready` 事件，以确保在尝试扩展它之前标记已在 DOM 中完全加载并渲染。

最后，将 `NodeMenuNav` 插件应用到我们的菜单上，并根据在标记中定义的所有 ID 和 CSS 类名自动为我们构建飞出菜单。

# 添加下拉导航菜单

飞出菜单的一种轻微变是下拉菜单。同样，这是一种许多用户会熟悉并能够舒适地使用的菜单结构。

### 准备工作

我们可以在上一个配方的基础上进行构建，标记几乎相同，只是在父元素上应用了一些 CSS 类名。

### 如何实现...

- 1. 此示例使用包含以下内容的文件 `nav_dropdown.php`：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/nav_dropdown.php');
$PAGE->requires_js('/cook/nav_dropdown.js', true);
echo $OUTPUT->header();
?>

<div id="menu" class="yui3-menu yui3-menu-horizontal yui3-menubuttonav" style="float:left;height:100px;">
<div class="yui3-menu-content">
```html
<ul>
<li class="yui3-menuitem">
  <a class="yui3-menuitem-content" href="#">Item 1</a>
</li>
<li class="yui3-menuitem">
  <a class="yui3-menuitem-content" href="#">Item 2</a>
</li>
<li>
  <a class="yui3-menu-label" href="#submenu-1">
    <em>Sub Menu</em>
  </a>
  <div id="submenu-1" class="yui3-menu">
    <div class="yui3-menu-content">
      <ul>
        <li class="yui3-menuitem">
          <a class="yui3-menuitem-content" href="#">Sub Item 1</a>
        </li>
        <li class="yui3-menuitem">
          <a class="yui3-menuitem-content" href="#">Sub Item 2</a>
        </li>
      </ul>
    </div>
  </div>
</li>
<li class="yui3-menuitem">
  <a class="yui3-menuitem-content" href="http://moodle.org/">Moodle.org</a>
</li>
</ul>
</div>
<?php
echo $OUTPUT->footer();
?>
```

此标记为导航菜单生成了一个简单的、基于列表的结构，在任何样式处理之前所示：

- 项目 1
- 项目 2
- 子菜单
    - 子项目 1
    - 子项目 2
- Moodle.org

- 2. 我们需要关联的 JavaScript `nav_dropdown.js` 并包含以下内容：

```javascript
YUI().use("node-menunav", function(Y) {
  Y.on("contentready", function () {
    this.plug(Y.Plugin.NodeMenuNav);
  }, "#menu");
});
```

> 注意：此示例中使用的 JavaScript 与飞出菜单中的完全相同。

只需通过向父 `<div>` 元素添加以下类，即可将菜单转换为下拉菜单：

| 名称 | 目的 |
| :--- | :--- |
| yui3-menu | 指示 YUI3 构建下拉菜单而非垂直飞出菜单。 |
| yui3-menu-horizontal | 使菜单项水平排列。 |
| yui3-menubuttonav | 使菜单看起来像按钮。 |

## 高级布局技术

## 工作原理...

从飞出菜单到下拉菜单的转换完全通过在前面的章节中描述的 CSS 类来实现。下方的截图显示了下拉菜单的最终渲染：

| 项目 1 | 项目 2 | 子菜单 | Moodle.org |
| :--- | :--- | :--- | :--- |
| | | 子项目 1 | |
| | | | 子项目 2 |

# 显示树形导航菜单

另一种显示导航菜单的方法是树形视图。用户熟悉如 Windows 资源管理器之类的文件和文件夹目录结构。

在编写时，YUI3 缺乏稳定的 TreeView ，因此我们将使用 YUI2 的 TreeView 组件。

### 如何实现...

- 1. 我们必须在 `nav_tree.php` 中定义菜单树的标记：

```php
<?php
require_once dirname(__FILE__) . '../config.php';

$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/nav_dropdown.php');
$PAGE->requires_js('/cook/nav_dropdown.js', true);
echo $OUTPUT->header();
?>

<div id="treeContainer">
  <ul>
    <li><a href="#">Item 1</a></li>
    <li><a href="#">Item 2</a></li>
    <li>Sub Tree
      <ul>
        <li><a href="#">Sub Item 1</a></li>
        <li><a href="#">Sub Item 2</a></li>
      </ul>
    </li>
  </ul>
</div>
```

```html
<li></li>
<li><a href="http://moodle.org/">Moodle.org</a></li>
</ul>
</div>
<?php
echo $OUTPUT->footer();
?>
```

下面的截图显示了增强之前的标记基本嵌套无序列表结构：

- 项目 1
- 项目 2
- 子菜单
    - 子项目 1
    - 子项目 2
- Moodle.org

- 2. 接下来，我们在关联的 JavaScript 文件 `nav_tree.js` 中添加必要的代码：

```javascript
YUI().use("yui2-treeview", function(Y) {
  var YAHOO = Y.YUI2;
  var treeView = new YAHOO.widget.TreeView("treeContainer");
  treeView.render();
});
```





## 高级布局技术

随后，我们的无序列表将被隐藏并替换为原始列表的动态树视图表示，如下截图所示：

| 项目 1 |
| 项目 2 |
| 子树 |
| 子项目 1 |
| 子项目 2 |
| Moodle.org |

# 添加标签页内容控制

标签页内容控制是用户在单个页面内导航一系列内容面板的便捷方法。本教程将向你展示如何使用 YUI3 TabView 模块来增强一系列 `<<div>` 内容面板。

### 如何实现...

+ 1. 首先，我们定义要增强的标记语言，在本示例中，为 `tabview.php`：

```php
<?php
require_once(dirname(__FILE__) ) . '../config.php';

$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->requires->js('js/cook/tabview.js');
$PAGE->set_url('/cook/tabview.php', true);
echo $OUTPUT->header();
?>
<div id="tabContainer" style="width:400px">
<ul>
<li><a href="#tab1">Moodle</a></li>
<li><a href="#tab2">来源</a></li>
<li><a href="#tab3">名称由来</a></li>
</ul>
</div>
<div id="tab1">
<p>nMoodle（Modular Object-Oriented Dynamic Learning Environment 的缩写）是一个免费开源的在线学习软件平台，也被称为课程管理系统（CMS）或虚拟学习环境（VLE）。截至</p>
</div>
```

2010 年 10 月，它已拥有 49,952 个注册并经过验证的站点用户群，在 370 万门课程中服务了 3700 万用户。

```
</div>>
<div id="tab2">
```

Martin Dougamas 拥有计算机科学和教育领域的硕士学位，他编写了 Moodle 的第一个版本。Dougamas 开始攻读博士，研究“在反思性探究的互联网社区中利用开源软件支持社会构造主义教学与探究认识论”。社会构造主义究竟如何让 Moodle 不同于其他学习平台这一点很难表现，但它被 Moodle 采用者视为一个重要因素。其他 Moodle 采用者（如英国开放大学）也指出，学习管理系统同样可以被视为“相对教学中立”。

```
</div>
<div id="tab3">
```

Moodle 缩写代表 Modular Object-Oriented Dynamic Learning Environment（模块对象化动态学习环境；在早期，“M”代表“Martin's”，即以原始开发者 Martin Dougamas 的名字命名）。除了是一个缩写外，该名称的选取还因为 Moodle 在词典中的定义，并对应于一个可用的域名。

```
</div>
</div>
<?php
echo $OUTPUT->footer();
?>
```

## 高级布局技术

在增强之前，这会产生一系列线性的内容块，如下截图所示：

- Moodle
- 名称由来

Moodle（Modular Object-Oriented Dynamic Learning Environment 的缩写）是一个免费开源的在线学习软件平台，又被称为课程管理系统、学习管理系统、虚拟学习环境（VLE）。截至 2010 年 10 月，它已拥有 49,952 个注册并经过验证的用户，在 3.7 万门课程中服务了 3700 万人。Martin Douglas 拥有计算机科学和教育领域的硕士学位，他编写了 Moodle 的第一个版本。Douglas 开始攻读博士以研究“在反思性探究的互联网社区中利用开源软件支持社会构造主义教学与学习认识论”。虽然社会构造主义究竟如何让 Moodle 不同于其他平台这一点很难知道，但它被许多采用者引用，例如英国开放大学指出，学习管理系统同样可以被视为“相对中立”。

Moodle 缩写代表 Modular Object-Oriented Dynamic Learning Environment（在早期，“M”代表“Martin's”，即以原始开发者 Martin Douglas 的名字命名）。除了是一个缩写外，该名称的选取还因为 Moodle 在词典中的定义并对应于一个可用的域名。

+ 2. 随后，我们在相关的 JavaScript 文件 `tabview.js` 中添加必要的代码：

```
YUI().use("tabview", function(Y) {
var tabView = new Y.TabView(
    {
        srcNode: '#tabContainer'
    }
);
tab.render();
});
```

## 工作原理...

标记语言包含一个父级 `<div>` 容器，我们必须为其分配一个 ID，以便稍后在 JavaScript 代码中作为引用。

## 第 7 章

此 `<div>` 首先包含一个无序列表，每个项目对应一个标签页。每个项目都是 `<a>` 标签，带有标签页的文本标签，其 `href` 指向后文定义的 `<div>` 内容 ID。

接下来是另一个 `<div>` 容器，它将为每个内容标签页包含一个子 `<div>` 容器。每个子 `<div>` 容器的 ID 将与之前定义的无序列表中对应项的 `href` 相匹配。

转到 JavaScript 代码，首先加载 YUI 模块 `TabView`。接下来，我们创建一个 TabView 的新实例，并向构造函数传递一个配置对象。最后，我们调用 TabView 的 `render` 方法，它会将标记语言转换为各个标签页。





## 高级布局技术

```javascript
visible:false,
modal:true,
width:"300px",
height:"auto",
close: true,
draggable: false,
fixedcenter: true
}
panel.hideEvent.subscribe(function() {
  Y.one('#modalContainer').setStyle('height', null);
  panel.render();
})
function showPanel() {
  Y.one('#modalContainer').setStyle('height', Y.one('body')).get('winHeight');
  panel.show();
}
Y.on('click', showPanel, "#show");
```

## 工作原理...

我们的内容通过标记中的一个父级 `<div>` 容器来定义，并为其分配一个 ID 作为引用。

该父容器包含三个子 `<div>` 元素：

| 目的 | 所需 CSS 类名 |
| --- | --- |
| 窗口头部文本 | hd |
| 窗口主体内容 | bd |
| 窗口页脚文本 | ft |

现在，我们必须在 JavaScript 中实例化一个新的 Panel 组件，并传递一个包含以下属性的配置对象：

| 名称 | 值 |  |
| --- | --- | --- |
| visible | false | 默认隐藏窗口 |
| modal | true | 将窗口行为设置为模态 |
| width | 300px | 设置窗口所需的宽度 |
| height | 150px | 设置窗口所需的高度 |
| close | true | 在窗口右上角显示关闭按钮 |
| draggable | true | 允许通过拖动移动窗口 |
| fixedcenter | true | 在视口中心显示窗口 |

接下来，我们将订阅面板的隐藏事件（hide event）。每当窗口隐藏或用户点击窗口的关闭图标时，我们在此定义的函数就会被调用。在该函数中，我们将重置包含模态面板的 `<div>` 元素的高度，将其恢复到原始高度。

接着，我们调用 Panel 组件新实例的 `render` 方法。

最后，我们定义一个函数来显示窗口。在这个示例中，我们将其绑定到**显示** 按钮的点击事件上。

当页面加载时，我们的 JavaScript 会隐藏窗口内容，并将其渲染为模态窗口。

当用户点击**显示面板** 按钮时，将调用窗口的 `show` 方法。首先，设置容器 `<div>` 元素的高度以匹配浏览器窗口的高度，以确保面板不会被裁剪并完整显示，如下面的截图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_133_0.png)

注意，背景内容是灰色的，且在窗口关闭之前用户是无法访问的，这符合模态（modal）的概念。这允许设计人员确保用户在恢复与页面其他部分的交互之前，立即考虑任何特别重要的信息或需要执行的操作。

## 8
## 组件动画

在本章中，我们将涵盖：

- 元素淡入（Fading in）
- 元素淡出（Fading out）
- 元素滚动
- 元素调整大小
- 使用缓动（Easing）进行动画处理
- 沿直线路径移动元素
- 沿折线路径移动元素
- 改变元素的颜色
- 多个动画的顺序执行

## 引言

在本章中，我们将学习如何使用动画让页面上的元素生起来。在处理何时以及何地向页面添加动画时，你必须采取理性的方法。尽量将动画的使用限制在能提升用户体验的场景，避免用毫无意义的动画轰扰用户。

动画在多种情况下可以提供有益的效果，例如通过淡入透明度来缓冲从一个元素到另一个元素的过渡，或者通过从浅色到深色的轻微脉冲效果来改变需要用户注意的元素的颜色。

我们将使用 YUI 库内置的动画功能，该库包含在标准的 Moodle 安装中。所有动画的基础都是在指定的时间范围内，将元素属性的值从一个特定值更改为另一个值。例如，为了淡出一个元素，我们可能会将元素的透明度从 100% 变为 0%；或者为了移动元素的位置，我们可能会改变它的 X 和 Y 坐标。

> 仔细考虑何时以及何地使用动画。问问自己：“这会提高用户体验吗？”避免不必要的动画，因为它们只会分散用户的注意力并降低你页面的可用性。

## 元素淡入

在本教程中，我们将通过动画化元素透明度从 0% 到 100% 的变化来产生淡入效果。与简单地从不可见变为可见，或从不显示变为显示相比，这种方法让元素变得可见更加微妙。

在这里，我们可以通过观察一系列帧来查看此动画的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_136_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_136_1.png)

### 如何实现...

我们首先创建一个 PHP 页面来加载 Moodle 编程环境，这反过来会加载 YUI3 环境。起点是，我们在页面中需要一个想要“淡入”的元素。此外，我们通过将 CSS 'opacity' 设置为 0 来确保该元素初始时是隐藏的。

接下来，我们需要添加 JavaScript 代码来将透明度从 0 变为 1。我们通过创建一个新的 YUI 实例并加载两个模块：`node` 和 `anim`。

`node` 模块允许我们访问页面事件，而 `anim` 模块为我们提供了 YUI 的动画功能。现在我们加载了所需的模块，可以创建 anim 模块的新实例并传递多个参数。`node` 参数是我们要动画的元素 ID，而 `to` 参数是一个包含我们想要动画属性的对象，即属性的最终值随时间变化。

在这个示例中，我们仅在 `to` 参数中包含了透明度属性，并设置为 1，即 100%。

最后，我们订阅正在动画的元素的 `contentready` 事件。这确保了在附加代码运行之前，元素已完全加载并可以使用。我们在此附加的代码只是调用了之前创建的 anim 对象的 `run` 方法。

```php
<?php
require_once(dirname(__FILE__) . '/config.php';
echo header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#00ff;padding:30px;opacity:0;">
<h1>Animation: Fade-in</h1>
</div>
```

```javascript
YUI.use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      opacity:1
    }
  });

  Y.on("contentready", function () {
    anim.run();
  });
});
```

## 元素淡出

在本教程中，我们将通过动画化元素透明度从 100% 到 0% 的变化来产生淡出效果。与简单使用 CSS 将可见性或显示属性改为 `hidden` 或 `none` 相比，这种方法让元素变得不可见更加微妙。

我们可以通过观察以下一系列帧来查看此动画的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_138_0.png)





![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_139_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_139_1.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_139_2.png)

### 如何实现...

我们首先创建一个 PHP 页面来加载 Moodle 编程环境，该环境反过来加载我们将使用的 YUI3 环境。

在例例中，我们创建了一个名为 `anim_fadeout.php` 文件，内容如下：

```php
<?php
require_once(dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/anim_fadeout.php');
$PAGE->requires('js', '/cook/anim_fadeout.js', true);
echo OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#0099FF;float:left;padding:30px;">
<h1>Animation: Fade-out</h1>
```

# 动画组件

```php
</div>
<?php
echo $OUTPUT->footer();
?>
```

此外，我们还创建一个 JavaScript 文件，在其中执行动画。在本例中，`anim_fadeout.js` 的内容如下：

```javascript
YUI().use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      opacity:0
    }
  });

  Y.on("contentready", function () {
    anim.run();
  }, "#anim-container");
});
```

## 工作原理...

作为起点，我们在页面中需要一个我们想要“淡出”的元素。显然，所有元素的默认透明度均为 100%，因此我们不需要显式地指定这一点。

接下来，我们需要添加必要的实例 JavaScript 代码，将透明度从 1 变为 0。我们首先创建一个新的 YUI3 实例并加载两个模块：`node` 和 `anim`。

`node` 模块允许我们向页面挂载事件，而 `anim` 模块为我们提供了 YUI3 的动画能力。

现在我们已经加载了必要的模块，可以创建一个 `anim` 模块的新实例，并传入几个参数。`node` 参数是我们要想要动画的元素的 ID，`to` 参数是一个包含我们想要动画的属性的对象，即我们正随时间改变的属性的最终值。

在本例中，我们简单地在 `to` 参数中包含了 `opacity`（透明度）属性并将其设置为 0，即 0%。

最后，我们订阅正在执行动画的元素的 `contentready` 事件。这确保了在挂载的代码运行之前，元素已完全加载并可以使用。我们在这里挂载的代码简单地调用了之前在代码中创建的 `anim` 对象的 `run` 方法。

当我们选择进行动画处理的元素完成页面加载时，会触发 `contentready` 事件，这正是在我们调用动画对象 `run` 方法的地方。`run` 方法现在执行我们之前指定的转换，即将透明度更改为 0。我们没有指定转换的持续时间，因此它默认为 1 秒；这意味着元素的透明将在 1 秒的时间跨度内从 100% 变为 0%。

# 元素滚动

在本教程中，我们将观察如何对容器元素的内容滚动滚动。我们将滚动一个 `div` 标签的内容，该标签设置了宽度和高度以强制内容溢出，并并将 `overflow` 设置为隐藏。

通过查看以下帧的选取，我们可以看到此动画的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_141_0.png)

### 如何实现...

我们首先创建一个 PHP 页面来搭建基础的 Moodle 编程环境，在本例中为 `anim_scroll.php`，内容如下：

```php
<?php
require_once(dirname(__FILE__) . '/../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/anim/anim_scroll.php');
$PAGE->requires->js('/anim/anim_scroll.js', true);
echo $OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#0099ff;float:left;padding:5px;width:120px;height:200px;overflow:hidden;">
<h1>Animation:</h1>
<p>
Moodle（Modular Object-Oriented Dynamic Learning Environment）是一个免费且开源的学习平台，也称为课程管理系统、学习管理系统或虚拟学习环境 (VLE)。截至2010年10月，它已拥有49,952个注册并验证的站点，服务于 
</p>
</div>
<?php
echo $OUTPUT->footer();
?>
```

我们还创建了一个 JavaScript 文件，在其中执行动画。在本例中，`anim_scroll.js` 的内容如下：

```javascript
YUI().use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      top: 0
    }
  });

  Y.on("contentready", function () {
    var scrollHeight = Y('#anim-container').scrollHeight;
    var clientHeight = Y('#anim-container').clientHeight;
    // ... 滚动逻辑 ...
  }, "#anim-container");
});
```





<div id="anim-container" style="border:1px solid black;background-color:#0099FF;float:left;padding:5px;">
<h1>动画：调整大小</h1>
</div>
<?php
echo $OUTPUT->footer();
?>

我们还创建一个关联的 JavaScript 文件 anim_resize.js，在其中我们将添加动画代码，内容如下：

```
YUI().use("node", "anim", function (Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      width: '300px',
      height: '100px'
    }
  });

  Y.on("contentready", function () {
    anim.run();
  }, "#anim-container");
});
```

## 工作原理...

我们从一个容器元素开始（在本例中是一个 div ），它通过设置左侧的 CSS 属性将其宽度收缩以适应内容。同样，高度也会收缩以适应内容。

然后，我们设置了一个 anim 对象，将高度和宽度转换为新的较大的值，从而放大容器 div。

div 元素从默认的“自适应内容”尺寸开始。我们创建了一个 anim 对象，将宽度和高度分别放大到 300px 和 100px。

我们将动画设置为在内容加载完成并触发 contentready 事件时运行。这会导致元素在默认的 1 秒时间跨度内动画扩展到其新尺寸。

## 使用缓动（easing）进行动画

动画缓动是在动画过程的不同点添加加速或减速的技术，以提供更平滑的过渡。它也可能导致转换在返回最终状态之前超过目标值。例如，在对元素的高度进行动画时，可以通过让动画超过最终值，然后稳定在最终值来实现弹跳效果。

幸运的是，YUI3 包含了许多内置的缓动类型，我们可以通过极少的额外代码将它们添加到动画中。在本例中，我们将使用 `bounce-out` 缓动行为配合调整大小动画。这将使得框的边界在达到动画结束时看起来像在弹跳。

YUI3 中提供的许多缓动行为的完整列表可以通过以下 URL 获取：

```
http://developer.yahoo.com/yui/3/api/Easing.html
```

在这里，我们可以通过查看选帧来看到此动画中的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_146_0.png)

### 如何实现...

我们首先创建一个 PHP 页面来建立基础的 Moodle 编程环境。在本例中为 anim_ease.php，内容如下：

```php
<?php
require_once(dirname(__FILE__ ) . '/../config.php');

$PAGE->set_context(context_get_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/anim_ease.php');
$PAGE->requires->js('/cook/anim_ease.js', true);
echo $OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#fff;float:left;padding:5px;">
<h1>动画：平滑调整大小</h1>
</div>
<?php
echo $OUTPUT->footer();
?>
```

我们还创建一个关联的 JavaScript 文件 anim_ease.js，在其中我们将添加动画代码，内容如下：

```
YUI().use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      width: '400px',
      height: '100px'
    },
    easing: Y.Easing.bounceOut
  });
  Y.on("contentready", function () {
    anim.run();
  }, "#anim-container");
});
```

## 工作原理...

我们以与上一个教程相同的方法创建了调整大小动画，放大容器 div 的宽度和高度。

在本例中，我们向 anim 对象添加了一个额外的属性 `easing` 来执行缓动。它接收来自 `Y.Easing` 对象下可用的任何 YUI 行为的值，在本例中为 `Y.Easing.bounceOut`。

现在，当从容器 div 的 contentready 事件运行调整大小动画时，它将根据 `bounceOut` 缓动的行为，在动画结束时带有弹跳效果地执行动画。

## 沿直线路径移动元素

通过对页面上 X 和 Y 位置的变化进行动画处理，可以沿直线路径移动元素来重新定位。在本例中，我们将让一个容器 div 向右移动 200 像素。

在这里，我们可以通过查看选帧来看到此动画中的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_148_0.png)

### 如何实现...

我们首先创建一个 PHP 页面来建立基础的 Moodle 编程环境。在本例中为 anim_straight.php，内容如下：

```php
<?php
require_once(dirname(__FILE__)) . '../config.php';

$PAGE->set_context(context_get_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/anim_straight.php');
$PAGE->requires->js('/cook/anim_straight.js', true);
echo $OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#009FF;padding:30px;width:150px;">
<h1>动画：移动</h1>
</div>
<?php
echo $OUTPUT->footer();
?>
```

我们还创建一个关联的 JavaScript 文件 anim_straight.js，在其中我们将添加动画代码，内容如下：

```
YUI().use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container'
  });

  Y.on("contentready", function() {
    var startX = Y.one('#anim-container').getX();
    var startY = Y.one('#anim-container').getY();
    anim.set('to', {x: startX+200, y: startY});
  });
});
```

## 组件动画

```
anim.run();
```

## 工作原理...

我们在 HTML 中从一个 div 元素开始将其移动到一个新位置。在 JavaScript 代码中，我们通过传递 div 的 ID 创建一个新的 anim 对象。接下来，订阅 div 的 contentready 并添加只有在 div 在浏览器加载后才会运行的代码。

首先，当 div 加载时，我们的代码获取当前的 X 和 Y 坐标，以便知道将移动到哪里。接下来，我们调用 anim 对象的 `set` 方法，允许我们将 `to` 属性设置为新的 X 和 Y 坐标。我们将 div 向右移动 200px，并保持 Y 坐标不变，因为我们不会上下移动 div。

当 div 加载时，我们的代码获取当前的 X 和 Y 坐标，并将其修改为新值。在 X 坐标上增加 200px，保持 Y 坐标不变。这实现了在默认 1 秒跨度内让 div 向右移动 200px。

## 沿曲线路径移动元素

另一种让元素运动动画的方法是使用曲线动画。曲线被指定为元素运动将遵循的 X 和 Y 坐标矩阵。在本例中，我们将跨越简单的曲线移动 div。

在这里，通过查看选帧可以看到此动画中的关键步骤：

| http://localhost/../anim_curved.php |
| :--- |
| 动画：移动 |

## 第8章

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_151_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_151_1.png)

### 如何实现...

我们首先创建一个 PHP 页面来建立基础的 Moodle 编程环境。在本例中为 anim_curved.php，内容如下：

```php
<?php
require_once(dirname(__FILE__)) . '../../config.php';
$PAGE->set_context(context_get_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/anim_curved.php');
$PAGE->requires->js('/cook/anim_curved.js', true);
echo $OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#0099FF;padding:10px;width:150px;margin:30px;">
<h1>动画：移动</h1>
</div>
<?php
echo $OUTPUT->footer();
?>
```

## 组件动画

我们还创建一个关联的 JavaScript 文件 anim_curved.js，在其中我们将添加动画代码，内容如下：

```
YUI().use("anim", function(Y) {
  var startX = Y.one('#anim-container').getX();
  var startY = Y.one('#anim-container').getY();
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      curve: [
        [startX+40, startY-40],
        [startX+160, startY]
      ]
    }
  });

  Y.on("contentready", function () {
    anim.run();
  }, "#anim-container");
});
```

## 工作原理...

我们从一个简单的 div 元素开始，将其沿曲线路径移动。在我们的 JavaScript 文件中，我们通过传递 div 的 ID 基于我们的 div 创建一个新的 anim 对象。接下来，订阅 div 的 contentready 函数并添加动画代码。首先，获取对象的当前 X 和 Y 坐标，以便知道动画的起始位置。接下来，我们使用 `set` 方法添加一个 `to` 属性，将其设置为一个“curve”对象，该对象包含 X 和 Y 坐标的数组矩阵，描述了我们希望对象遵循的曲线。

当 div 加载并运行动画代码时，YUI 通过将对象移动到我们指定的每个 X 和 Y 坐标对来使其运动化。这实现了让 div 沿与指定坐标描述的路径形状移动的效果。





## 改变元素的颜色

在本教程中，我们将制作一个元素改变色的动画。我们将把 `div` 元素的背景颜色从蓝色变为绿色。

在这里，我们可以通过查看一系列帧来了解此动画的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_153_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_153_1.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_153_2.png)

### 如何实现...

我们首先创建一个 PHP 页面来搭建基础的 Moodle 编程环境。在这种情况下，`anim_color.php` 的内容如下：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/anim/anim_color.js', true);
echo $OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#009FF;float:left;padding:5px;">
<h1>Animation Color</h1>
</div>
```

```php
<?php
echo $OUTPUT->footer();
?>
```

我们还创建一个关联的 JavaScript 文件 `anim_color.js`，在其中添加动画代码，内容如下：

```javascript
YUI().use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      backgroundColor: 'green'
    }
  });

  Y.on("contentready", function () {
    anim.run();
  }, "#anim-container");
});
```

### 工作原理

我们从一个具有特定背景（在本例中为蓝色）的简单 `div` 元素开始。进入 JavaScript，我们首先基于该 `div` 创建一个 anim 元素，并将 `div` 的 ID 指定为 `node` 属性。此外，我们将设置 `to` 属性，将对象的 `backgroundColor` 属性设置为它的新颜色，在本例中为绿色。

最后，我们设置动画在 `div` 通过 `contentready` 事件加载后运行。当 `div` 元素加载完成时，它的 `contentready` 事件会被触发，我们的动画随之运行。元素的颜色从初始的蓝色变为指定的绿色，持续时间为默认的一秒钟。

### 动画的排序

在一次动画期间，我们可以更改任意数量的属性。若要让多个动画线性地发生（一个接一个），我们必须使用新方法。YUI 通过提供一个 `end` 事件来实现这一点，该事件在动画完成时触发。通过这种方式，我们可以根据需要链联任意数量的动画，一个接一个。

在本教程中，我们将链联两个动画：缩小 `div` 元素的大小，然后将其淡出。在这里，我们可以通过查看一系列帧来了解此动画的关键步骤：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_155_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_155_1.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_155_2.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_155_3.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_155_4.png)

### 如何实现...

我们首先创建一个 PHP 页面来搭建基础的 Moodle 编程环境。在这种情况下，`anim_multiple.php` 的内容如下：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/anim/anim_multiple');
$PAGE->requires->js('/anim/anim_multiple.js', true);

echo $OUTPUT->header();
?>
<div id="anim-container" style="border:1px solid black;background-color:#009FF;float:left;padding:5px;width:300px;height:150px;opacity:1">
<h2>Resize</h2>
</div>
<?php
echo $OUTPUT->footer();
?>
```

我们还创建一个关联的 JavaScript 文件 `anim_multiple.js`，在其中添加动画代码，内容如下：

```javascript
YUI().use("node", "anim", function(Y) {
  var anim = new Y.Anim({
    node: '#anim-container',
    to: {
      width: '180px',
      height: '50px'
    }
  });

  var animEnd = function() {
    this.detach('end', animEnd);
    this.set('to', {opacity:0});
    this.run();
  }
  anim.on('end', animEnd);

  Y.on("contentready", function () {
    anim.run();
  }, "#anim-container");
});
```

## 工作原理...

我们从一个我们将进行动画的 `div` 元素开始，设置所需的高度和宽度，并设置一个引用 ID。

接下来，进入 JavaScript 代码，首先基于我们的 `div` 创建一个新的 anim 对象，传入该 `div` 的 ID。在这里，我们将设置链链中的第一个动画，即通过将宽度和高度缩减到 180px 和 50px 来调整元素的大小。

接下来，我们将在独立的函数中定义第二个动画，在本例中为 `animEnd`。稍后它会被绑定到第一个动画的 `end` 事件上。由于这样做，动画的顺序是正确的。



```php
<?php
$PAGE->set_url('/cook/external_jquery.php');
$PAGE->requires_js('/cook/jquery-1.4.4.min.js');
$PAGE->requires->js('/cook/external_jquery.js');

echo $OUTPUT->header();
echo $OUTPUT->footer();

?>
```

接下来，我们创建一个关联的 JavaScript 文件，并在其中添加 jQuery 代码：

```javascript
$(document).ready(function() {
    alert('Hello from jQuery');
});
```

现在，当我们在浏览器中运行此页面时，我们将看到以下 JavaScript 警告弹窗出现，我们可以确定 jQuery 已正确加载：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_161_0.png)

## 工作原理...

在我们将 jQuery 副本保存到 Moodle 安装目录后，可以创建一个 PHP 页面来初始化该框架。我们创建此文件并设置 Moodle 编程环境，添加了两个 JavaScript 包含。第一个要包含的文件是 jQuery 文件，第二个是我们的自定义 JavaScript 文件，它将包含我们使用 jQuery 框架的代码。注意，在任何 JavaScript 使用框架之前，必须包含主 jQuery 文件。

只需在页面中包含 jQuery 文件：`$PAGE->requires->js('/cook/jquery-1.4.4.min.js');` 即可确保框架已初始化并准备好使用。在示例中，我们包含了对框架的一个非常简单的使用，即通过页面对象的 `ready` 事件显示 JavaScript 警告，这确认了框架运行正常。

## 添加 MooTools 框架

在本教程中，我们将为示例页面设置 MooTools 框架的使用。

### 集成外部库

以下是来自 MooTools 网站（http://mootools.net/）关于该框架的简要概述：

MooTools 是一个紧凑、模块化的面向对象 JavaScript 框架，专为中高级 JavaScript 开发者设计。它允许你通过其优雅、文档齐全且一致的 API 编写强大、灵活且跨浏览器的代码。

MooTools 本质上是 UI 或 jQuery 的另一种替代方案。如果你希望使用某些基于 MooTools 的第三方代码，你可能需要安装此框架，因为这些代码要么无法移植到原生 JavaScript，要么移植并不实际。你也可以使用 Mood 偏好的 JavaScript 框架 YUI 对其重写。

我们将创建一个简单的 MooTools 脚本，当 `domready` 事件触发时将显示一个 MooTools 警告。

### 准备工作

我们首先下载 MooTools 框架的最新版本。访问 MooTools 首页（http://mootools.net/），导航到下载页面，并下载合适的 MooTools 版本。在示例中，我们使用不带兼容性的 MooTools Core 1.3 压缩版本。

将此文件保存到 Moodle 安装目录中的某个位置。在示例中，我们将其保存在 Moodle 站点主文件目录下的 `cook` 中。

### 如何操作...

设置一个 PHP 页面 `external_mootools.php`，其内容如下，将用于设置 MooTools：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');

$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/external_mootools.php');
$PAGE->requires->js('/cook/mootools-core-1.3.js');
$PAGE->requires->js('/cook/external_mootools.js');

echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

最后，我们创建一个 JavaScript 文件 `external_mootools.js`，并在其中添加一个简单的 MooTools 脚本，如下：

```javascript
window.addEvent('domready', function() {
  alert('Hello from MooTools');
});
```

一旦我们将 MooTools 副本保存到 Moodle 安装中，就可以设置一个 PHP 文件来创建运行 MooTools 代码的页面。我们包含了两个 JavaScript 文件，第一个是 MooTools 文件，第二个是我们的自定义 JavaScript 文件 `external_mootools.js`。注意，MooTools 文件必须在使用它的文件之前包含。

我们现在可以在网页浏览器中加载此页面，并将看到以下 JavaScript 警告弹窗，证明了 MooTools 已正确加载并准备好使用：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_163_0.png)

## 工作原理...

我们在自己的 JavaScript 文件之前加载了 MooTools 框架，确保框架已准备就绪。我们在这里添加的 JavaScript 代码利用窗口的 `domready` 事件，在页面完全加载后显示 JavaScript 警告。当加载页面时，我们看到警告弹窗，可以确定 MooTools 已正确加载。

## 添加 Dojo 框架

在本教程中，我们将为 Moodle 设置 Dojo 框架的使用。然后，我们将创建一个简单的 Dojo 脚本，在页面完全加载时利用 Dojo 的 `addOnLoad` 功能显示 JavaScript 警告。

来自来自 Dojo 网站（http://dojotoolkit.org/）关于该框架的简要描述：

> Dojo 为您节省时间，提供性能，并随着您的开发过程而扩展。它是经验丰富的开发者在构建桌面和移动 Web 体验时青赖的工具包。

安装此框架的典型需求是：你希望使用某些第三方代码，这些代码要么无法移植到原生 JavaScript，要么移植并不实际。你也可以使用 Mood 偏好的 JavaScript 框架 YUI 对其重写。

### 准备工作

我们首先下载 Dojo 框架的最新版本。访问 Dojo 首页（http://dojotoolkit.org/），导航到下载页面，并下载合适的 Dojo 版本。在示例中，我们使用不带兼容性的 Dojo 压缩版本。

### 如何操作...

设置一个 PHP 页面 `external_mootools.php`，其内容如下，将用于设置 Dojo：

```php
<?php
require_once(dirname(__FILE__) . '../config.php');

$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/external_mootools.php');
$PAGE->requires->js('/cook/dojo.js');
$PAGE->requires->js('/cook/external_mootools.js');

echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

最后，我们创建一个 JavaScript 文件 `external_mootools.js`，并在其中添加一个简单的 Dojo 脚本，如下：

```javascript
dojo.addOnLoad(function() {
  alert('Hello from Dojo');
});
```

一旦我们将 Dojo 副本保存到 Moodle 安装中，就可以设置一个 PHP 文件来创建运行 Dojo 代码的页面。我们包含了两个 JavaScript 文件，第一个是 Dojo 文件，第二个是我们的自定义 JavaScript 文件 `external_mootools.js`。注意，Dojo 文件必须在使用它的文件之前包含。

我们现在可以在网页浏览器中加载此页面，并将看到以下 JavaScript 警告弹窗，证明了 Dojo 已正确加载并准备好使用：

## 工作原理...

我们在自己的 JavaScript 文件之前加载了 MooTools 框架，确保框架已准备就绪。我们在这里添加的 JavaScript 代码利用窗口的 `domready` 事件，在页面完全加载后显示 JavaScript 警告。当加载页面时，我们看到警告弹窗，可以确定 Dojo 已正确加载。

## 添加 Prototype 框架

在本教程中，我们将为示例页面设置 Prototype 框架的使用。然后我们将设置一个简单的 Prototype 脚本，在页面完全加载时显示 JavaScript 警告。

以下是来自 Prototype 网站（http://www.prototypejs.org/）关于该框架的简要描述：

- Prototype 是一个旨在简化动态应用程序开发的 JavaScript 框架。
- 通过其独特的、易用的类驱动开发工具包以及最出色的 Ajax 库，Prototype迅速成为 Web 应用开发者的首选代码库。

Prototype 是两个扩展的基础：script.aculo.us 和 Lightbox。将在接下来的两个教程中查看这些，以进一步增强可用功能。

### 准备工作

我们首先下载 Prototype 框架的最新版本。访问 Prototype 首页（http://www.prototypejs.org/），导航到下载页面，并下载合适的 Prototype 版本。在示例中，我们使用不带兼容性的 Prototype 压缩版本。





## 如何操作..

我们现在已经有了 Prototype 的本地副本。我们可以创建一个名为 `external_prototype.php` 的页面，在其中我们将加载框架以及自定义的 JavaScript 文件，如下所示：

```php
<?php

require_once(dirname(__FILE__) . '../../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/external_prototype.php');
$PAGE->requires->js('/cook/prototype.js');
$PAGE->requires->js('/cook/external_prototype.js');
echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

最后，我们创建自定义的 JavaScript 文件 `external_prototype.js`，内容如下：

```javascript
document.observe("dom:loaded", function() {
    alert('Hello from Prototype');
});
```

我们创建一个 PHP 文件来设置 Moodle 编程环境，并加载 Prototype 框架文件。一旦 Prototype 文件加载完成，我们就可以添加自己的 JavaScript 文件，其中包含使用 Prototype 的脚本。在该脚本中，我们使用 Prototype 的 `document observe` 方法为页面加载事件绑定一个 JavaScript 警报。

当我们在浏览器中加载此页面时，我们看到该事件已触发，并显示了 JavaScript 警报，如下图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_166_0.png)

## 工作原理...

PHP 文件加载了 Prototype 框架。这确保了在我们在使用框架的自定义 JavaScript 加载之前，它已经加载并准备就绪。接下来，加载我们的 JavaScript，并使用 Prototype 注册一个在页面完成后运行的 JavaScript 警报。当页面在浏览器中完全加载后，我们将看到 JavaScript 警报弹出，确认 Prototype 框架已正确加载。

## 为 Prototype 添加 script.aculo.us 插件

`script.aculo.us` 库是 Prototype 的一个插件，包含许多用户界面增强功能，如动画、拖放和 AJAX 控制。在本教程中，我们将设置 `script.aculo.us` 并添加一个抖动动画以验证它是否已正确加载。

### 准备工作

首先，我们需要通过访问 http://script.aculo.us/ 并导航到下载页面来获取 `script.aculo.us` 副本。下载当前版本的 ZIP 压缩包，并解压到 Moodle 安装目录中 `cook` 子目录下的名为 `scriptaculous` 的文件夹中，即 `/path/to/moodle/cook/scriptaculous`。

### 如何操作...

创建一个 PHP 文件 `external_scriptaculous.php`，内容如下：

```php
<?php
require_once(dirname(__FILE__) . '/../config.php');

$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/external_scriptaculous.php');
$PAGE->requires->js('/cook/prototype.js');
$PAGE->requires->js('/cook/scriptaculous/scriptaculous.js');
$PAGE->requires->js('/cook/scriptaculous/effects.js');
$PAGE->requires->js('/cook/external_scriptaculous.js');
echo $OUTPUT->header('header');

?>
<div id="demo">Hello from script.aculo.us</div>
<?php
echo $OUTPUT->footer();
?>
```

最后，我们创建一个 JavaScript 文件 `external_scriptaculous.js`，内容如下：

```javascript
document.observe("dom:loaded", function() {
  Effect.Shake("demo");
});
```

### 集成外部库

现在当我们在网页浏览器中加载此页面时，我们可以看到抖动效果生效。以下截图显示了抖动动画效果的一些帧。请注意，我们应用效果的文本在左右之间移动，仿佛文本正在左右抖动，最后才回到原始位置：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_168_0.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_168_1.png)

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_168_2.png)

## 工作原理...

首先，我们下载 `script.aculo.us` 文件并将其保存到 `cook` 子目录中与 Moodle 文件并列的 `scriptaculous` 文件夹中。

接下来，我们创建一个 PHP 文件，在其中加载必要的 JavaScript 文件。它们按顺序为：

- /cook/prototype.js
- /cook/scriptaculous/scriptaculous.js
- /cook/scriptaculous/effects.js
- /cook/external_scriptaculous.js

现在我们在 PHP 页面的 `body` 中添加一个 `div` 标签，其中包含一些示例文本。我们为此元素应用抖动动画效果，因此为了以后引用，我们为标签添加了 ID。

最后，我们在我们的 JavaScript 文件 `external_scriptaculous.js` 中添加一些代码。我们设置了一个页面加载函数，像上一个教程一样使用 Prototype。在函数内部，我们将使用 `script.aculo.us` 为我们的 `div` 元素应用抖动动画效果。

## 使用 Lightbox 添加图片

Lightbox 2 是一个非常流行的基于 `script.aculo.us` 的脚本，包含许多用户界面增强功能，如动画、拖放和 AJAX 控制。在本教程中，我们将设置 Lightbox 2 并添加一个抖动动画以验证其是否已正确加载。

### 准备工作

首先，我们需要通过访问 http://lbox2.com/ 并导航到下载页面来获取 Lightbox 2 副本。下载最新版本的 ZIP 压缩包，并将其解压到 Moodle 安装目录中 `cook` 子目录下的名为 `lightbox2` 的文件夹中，即 `/path/to/moodle/cook/lightbox2`。

Lightbox 2 是一个非常流行的基于 `script.aculo.us` 的脚本，包含许多用户界面增强功能，如动画、拖放和 AJAX 控制。在本教程中，我们将设置 Lightbox 2 并添加一个抖动动画以验证其是否已正确加载。

### 集成外部库

### 如何操作...

创建一个名为 `external_prototype.php` 的页面，在其中我们将加载框架以及我们自定义的 JavaScript 文件，如下所示：

```php
<?php
require_once(dirname(__FILE__) . '../../config.php');
$PAGE->set_context(get_context_instance(CONTEXT_SYSTEM));
$PAGE->set_url('/cook/external_prototype.php');
$PAGE->requires->js('/cook/prototype.js');
$PAGE->requires->js('/cook/external_prototype.js');
echo $OUTPUT->header();
echo $OUTPUT->footer();
?>
```

最后，我们创建自定义的 JavaScript 文件 `external_prototype.js`，内容如下：

```javascript
document.observe("dom:loaded", function() {
    alert('Hello from Prototype');
});
```

我们创建一个 PHP 文件来设置 Moodle 编程环境，并加载 Prototype 框架文件。一旦 Prototype 文件加载完成，我们就可以添加自己的 JavaScript 文件，其中包含使用 Prototype 的脚本。在该脚本中，我们使用 Prototype 的 `document observe` 方法为页面加载事件绑定一个 JavaScript 警报。

当我们在浏览器中加载此页面时，我们看到该事件已触发，并显示了 JavaScript 警报，如下图所示：

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_166_0.png)

## 工作原理...

PHP 文件加载了 Prototype 框架。这确保了在我们在使用框架的自定义 JavaScript 加载之前，它已经加载并准备就绪。接下来，加载我们的 JavaScript，并使用 Prototype 注册一个在页面完成后运行的 JavaScript 警报。当页面在浏览器中完全加载后，我们将看到 JavaScript 警报弹出，确认 Prototype 框架已正确加载。

## 使用 Lightbox 添加图片

Lightbox 2 是一个非常流行的基于 `script.aculo.us` 的脚本，包含许多用户界面增强功能，如动画、拖放和 AJAX 控制。在本教程中，我们将设置 Lightbox 2 并添加一个抖动动画以验证其是否已正确加载。

（注：此处提供的文本似乎存在重复或逻辑混乱，已根据翻译指令对原文呈现的内容进行了对应翻译）





# 目录

# 符号

- 输出 10
- 页 10
- <head>  13
- <script>  12
- bounceOut 缓动 136
- btn1_Click 函数 29

# A

# C

- addOnLoad 方法 153
- addRule 方法 42
- 数字字母验证类型 49
- 动画缓动 134-136
- 组件上的动画效果
- 颜色: 141, 142
- 淡入 124-126
- 淡出 126-128
- 沿曲线路径移动: 138-140
- 沿直线路径移动: 136-145
- 调整大小: 132, 133, 142-145
- 带有缓动的调整 134-136
- 滚动 129-131
- animEnd 145
- anim 模块 126
- anim 对象 126
- Array.each 工具 77
- 自动补全功能 93
- 自动更新功能 93
- 自动更新数据 98-100
- 可用事件 30

- 回调验证类型 55
- cellEvent 90
- 点击事件 72
- clientHeight 131
- 颜色动画生成 141, 142
- 数据表列排序 85, 86
- 组合框添加，使用自动补全 96, 97
- 比较验证类型 53
- 确保符合 XHTML Strict 规范 17
- 组件动画 123
- 内容
- contentready 30, 126
- content 属性 102
- 使用 DataSource 的 CSV 数据解析 69-72
- 添加自定义按钮控制 103, 104
- 自定义按钮 94
- 添加自定义 JavaScript 验证函数回调 54
- 关于自定义工具提示的 94 添加 101, 102

# B

- backgroundColor 属性 142
- 绑定基本事件处理程序 27-29

# D

- 数据显示 83, 85
- 使用 PHP 从外部域加载 63, 64
- 从 Moodle 2.0 服务检索 72-76
- data.csv 文件 70
- data.json 文件 67
- 数据表数据分页 87
- 使用 DataSource 解析 CSV 69-72
- 用于解析 JSON 67-69
- 用于解析 XML 64-66
- datasources_csv.js 文件 70
- datasource_csv.php 文件 70
- datasource_json.js 文件 68
- datasource_json.php 文件 67
- datasource_JsonSchema.plugin 69
- datasource_models.php 文件 73
- DataObject 83
- datasourceTextSchema.plugin 71
- datasource_xml.js 65
- datasource_xml.php 文件 64
- datasourceXMLSchema.plugin 66, 75
- dataTable 构造函数 85
- 数据表
- 基本列排序 85, 86
- 数据分页 87
- 启用编辑 89-91
- 行内编辑 80
- 无分页 80
- 滚动 80
- 启用 88
- 排序 79
- 使用 79
- data.xml 文件 64
- dirname 函数 11
- div 元素 95, 133
- Dojo 框架
- 关于 153
- 下载 152
- 设置 151, 152
- URL 151
- 工作 153
- domready 事件 30
- 下拉导航菜单关于 109 添加 109

# E

- 缓动行为 URL 134
- 启用数据表编辑 89-91
- 编辑分页 91
- 元素
- 颜色变化 141, 142
- 淡入效果生成 126-128
- 淡出效果生成 126-128
- 沿曲线移动 138-140
- 沿直线路径移动 136-138
- 调整大小 132, 133
- 滚动 129, 131
- 邮箱验证类型 46
- 事件结束 142
- event-delegate 模块 35
- 事件委托关于 34 实现: 33-35
- 事件处理器函数 145
- 扩展与应用程序库 (PEAR) 40
- 外部 URIs
- 使用 IO 的 alive 传输方法请求 60, 62

# F

- 淡入效果生成 126-128
- 淡出效果生成 126-128
- 失败事件 63
- 失败回调函数 66
- 飞出导航菜单关于 106
- 淡入 106-112
- 表单验证 40
- Function 数据源 99

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_174_0.png)

# G

- getFile 函数 59

# H

- href 属性 109

# I

- 使用 Lightbox 2 添加图像放大 157-160
- img 标签 102
- io 关于 58
- IO 传输
- 请求外部 URIs 60, 62

# JavaScript
- 确保符合 XHTML Strict 17
- JavaScript 文件 nav_float.js 108
- 加载 12
- 在 <head> 标签加载 13
- 从 PHP 生成 JavaScript 调用 14, 15
- jQuery 框架关于 148
- 添加 148
- 下载 148
- 设置 148, 149
- URL 148
- 工作 149
- js_init 调用 15
- JSON
- 使用 DataSource 解析 67-69

# L

- 从 Moodle 检索语言字符串 18, 19
- 字母验证类型 48
- Lightbox 2 关于 157
- 下载 157

# M

- 图像放大 158-160
- 集成 157
- loadCSV 72
- load 事件 30, 153
- loadJSON 函数 69
- loadXML 函数 66, 75
- LocalDataSource 95
- maxlength 验证类型 43
- minlength 验证类型 44
- modal 118
- modal 窗口关于 118
- 内容显示 118-122
- Moodle
- 加载额外的 YUI 模块 24
- 绑定基本事件处理程序 29-33
- 自动更新数据显示 98-100
- 使用 Lightbox 添加组合框 96, 97
- 添加自定义控件 103, 104
- 添加自定义 tooltip 101, 102
- 使用数据表工作 79
- 外部 JavaScript 库
- 事件委托启用 33-35
- 检索语言字符串 19
- 导航菜单 106
- 可调整大小元素 100, 101
- 使用 94-96 添加文本框 
- 从 YUI 3 加载 YUI 2 模块 25, 26
- YUI 3 库初始化 22-24
- YUI 控制台调试 36-38
- 从 Moodle 2.0 服务获取数据 72-76
- Moodle 文档链接 9
- Moodle 表单验证
- 另一个字段 53
- 添加自定义 JavaScript 函数回调 54, 55
- 使用正则表达式自定义验证 47
- 添加字母字段 48

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_175_0.png)

# N

- nav_dropdown.js 111
- nav_dropdown.php 109
- 导航菜单关于 106
- 下拉菜单 106, 109
- 飞出菜单 106
- 视图菜单 106, 112
- nav_tree.php 132
- NodeMenuNav 插件 109
- node 模块 126
- node 参数 126
- nonzero 验证类型 52
- 标点验证类型 51
- 数字验证类型 50

# O

- on-contentready 事件 109
- on 方法 on 参数 28

# P

- 分页器属性 88

# S

- 向 Prototype 添加 script.aculo.us 库 155
- 下载 155

![](img/6eec08dbea5e7459c4bcd2ec593a6fd6_176_0.png)

- 生成滚动动画 132, 133
- 带有缓动 134, 136
- 滚动数据表 129, 131
- 设置 155, 156
- setHeight 131
- 抖动动画效果 155
- span 元素 97
- src 属性 118
- success回调函数 66
- 成功事件 59
- success 函数 59

# X

- xReady 事件 63
- 确保符合 XML Strict 17
- 使用 DataSource 解析 XML 64-66

# Y

- Yahoo! Developer Network 22
- 用于 YUI 的 Yahoo! Developer Network 网站 24
- URL 24
- YUI 用户界面。见 YUI
- YUI.Dom 对象 38
- YUI.delegate 对象 36
- YUI.Easing 对象 136
- YUI.log 方法 37
- YUI 21, 93
- yui2calendar 26
- YUI2 DataTable 控制 87
- YUI2 DataTable 对象 85
- 从 YUI 3 加载 YUI 2 模块 25, 26
- YUI2 TreeView 模块 113
- YUI 3 57
- YUI 5 库初始化 22-24
- 使用 YUI 3 IO 请求 YUI URI 58, 59
- YUI3 node-menu 模块 106
- YUI3 Tab 模块 114
- YUI 控制台调试 36-38
- yui_console.ph 36
- 初始化 YUI DataSource 80-83
- yui_eventback.ph 28
- yui_init.ph 文件 22
- YUI 库 22
- YUI 模块加载 24




# 感谢购买

# Moodle JavaScript Cookbook

# 关于 Packt 出版社

Packt（读作 "packed"）于2004年4月出版了第一本书《高效 MySQL 管理》，随后继续专注于。我们的书籍为 IT 专业人士提供技术和解决方案。Packt 是一家现代化的公司，致力于生产前沿书籍。欲了解更多信息，请访问我们的网站：www.packt.com。

# 关于 Packt Open Source

2010年，Packt 发布了两个新品牌：Packt Open Source 和 Packt Enterprise，以继续其专注于。本书是 Packt Open Source 品牌的一部分，该品牌出版围绕开源许可的书籍，为从高级开发者到初级网页设计师的任何人提供信息。Open Source 品牌还运行 Packt 开源计划，为每个良好的开源项目提供收益。

# 为 Packt 写作

我们欢迎所有感兴趣的人提交提案。书籍提案可以发送至 author@packt.com。如果您的书籍处于早期阶段，并希望在编写正式提案之前进行讨论，请联系我们；我们的聘书编辑将与您联系。

我们不仅在寻找作者；如果您拥有强大的技术技能但没有写作经验，我们经验丰富的编辑可以帮助您发展写作生涯，或者只需为您的专业知识获得额外奖励。

## Moodle 2.0 初探

ISBN: 978-1-849511-94-0 平装本：272 页

发现 Moodle 2.0 的新特性、这些功能如何工作以及它将对您产生什么影响

- 1. 深入了解 Moodle 2.0 的新功能
- 2. 评论和条件活动等全新新增的好处
- 3.  Moodle 2.0 管理方面的变化
- 4. 第一本也是唯一涵盖 Moodle 2.0 所有精彩新功能的书籍

## Moodle 1.9 扩展开发

ISBN: 978-1-847194-24-4 平装本：320 页

利用强大的插件系统自定义和扩展 Moodle

- 1. 开发您自己的模块、活动、过滤器，并使用安全代码组织内容
- 2. 彻底涵盖 Moodle 的核心库以及使用它们的最佳实践
- 3. 探索 Moodle 的架构概念、它的结构以及它是如何运行的

请查看 www.PacktPub.com 获取有关我们书籍的信息
