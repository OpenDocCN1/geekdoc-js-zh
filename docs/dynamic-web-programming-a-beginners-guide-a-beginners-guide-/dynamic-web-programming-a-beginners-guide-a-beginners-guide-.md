#  Dynamic Web Programming 入门指南




已于 2020 年 10 月 23 日取消

## 关于作者

**Marty Matthews** 自早期大型机时代起，便以程序员和软件公司高管等不同身份从事计算机相关工作。因此，他对如何最有效地使用计算机有着深刻的见解，并将此应用于撰写或参与撰写了 70 余部著作，涵盖桌面和网页出版、Microsoft Office 以及 Microsoft 操作系统等领域。近期的著作包括 *FrontPage 2003 QuickSteps*；*FrontPage 2003: The Complete Reference*；*Microsoft Office 2007 QuickSteps*；以及 *Windows 7 QuickSteps*。Marty 与妻子 Carole 住在普吉特海湾的一个小岛上。

**John Cronan** 拥有超过 30 年的计算机行业经验，并已连续 17 年从事计算机相关书籍的撰写和编辑工作。他近期的著作包括 *Build an eBay Business QuickSteps, Second Edition*；*Microsoft Office Excel 2007 QuickSteps*；以及 *Microsoft Office Access 2007 QuickSteps*。John 与妻子 Faye（以及猫咪 Little Buddy）住在华盛顿州埃弗里特。


> 献给我们生活中的调味剂：
> Carole 和 Faye


## 致谢

许多人帮助促成了这本书的完成，其中包括：

**Greg Kettell**，技术编辑，纠正了许多错误，并为本书增色不少。谢谢，Greg！

**Joya Anthony**，策划协调人，让我们保持正轨。谢谢，Joya！

**Jan Jue**，文字编辑，将我们不成熟的尝试转化为可读的文字，与她工作总是令人愉快。谢谢，Jan！

**Smita Rajan**，项目经理，协调各方，推动手稿变成书籍。谢谢，Smita！

**Janet Walden**，编辑主管，为本书做了最后的润色。谢谢，Janet！

**Roger Stewart**，编辑总监，他对我们和这本书的信任使其成为可能。谢谢，Roger！

## 简介

人们通常从在页面上放置文本和图形开始构建网站，并逐步进行多个层次的格式化和布局。然而，所有这些都是*静态*内容，可以使用常见的文本编辑和排版程序创建。创建*动态*页面，即内容随用户事件而变化，需要编程以及可能使用数据库。

*Dynamic Web Programming: A Beginner's Guide*采用实践方法，带你从构建高级静态网页到创建包含各种动态元素的页面。为此，书中介绍、探索并演示了五种最常用的网页编程语言（X/HTML、CSS、JavaScript、PHP 和 MySQL），通过创建常见的动态网页元素来展示其应用。

本书假定你具有一定的静态网页制作经验，并希望为页面添加动态内容。为了为所有读者建立共同基础，本书首先快速回顾如何使用 HTML（超文本标记语言）创建静态网页，然后介绍 XML（可扩展标记语言）提供的更严格的规范和良好实践来实现 XHTML（可扩展 HTML）。接着，本书将带你了解如何使用 CSS（层叠样式表）和模板在一系列网页中应用共同的特性和格式。

*《动态Web编程：初学者指南》* 从JavaScript的概述开始讨论动态元素，以及如何使用JavaScript实现客户端元素，如鼠标悬停时更换图片、弹出窗口、将光标定位到表单中以及验证表单输入。接下来，我们概述了PHP，以及如何使用它实现服务器端元素，例如使用Cookie和服务器变量对用户进行身份验证。最后，本书将介绍MySQL以及如何将其与PHP结合使用来存储、选择和更新网页上的信息。

*《动态Web编程：初学者指南》* 是一本以解决方案为导向的书籍，围绕一系列详细示例组织而成，这些示例展示了常见动态Web元素的全部功能。本书旨在供你直接作为模板使用，用于构建包含动态内容的网页，包括全面使用MySQL/PHP数据库。

## 代码清单在线获取

本书中的所有代码清单，包括完整的用户身份验证和班级注册系统，均可从 www.mhprofessional.com/computingdownload 或 www.matthewstechnology.com/ 下载。

## 本书使用的约定

*《动态Web编程：初学者指南》* 使用了几种约定，以便于你阅读本书：

- **粗体** 用于标题、代码清单中的关键字以及屏幕上需要操作的词语，例如"...然后点击**运行**"。
- *斜体* 用于正在定义或需要特别强调的单词或短语。
- `等宽字体` 用于代码片段和代码清单。
- **粗体小写字母** 用于键盘上的按键，如 **ENTER** 和 **SHIFT**。
- 当你需要输入命令时，会指示你 *按* 相应的键。如果需要输入文本或数字，会指示你 *键入* 它们。

# 第一部分

## 准备工作

### 设置你的工作站

尽管本书的重点是使用JavaScript、PHP和MySQL进行动态Web编程，但重要的是我们需要在HTML、CSS以及创建动态Web页面所需的编程工具方面拥有共同的基础。因此，本书的这一部分致力于建立这一基础。在本部分简介中，我们将讨论创建和测试动态Web页面所需的工具。在第1章中，我们将回顾HTML和XHTML，而第2章将涵盖CSS。

当你开始进行动态Web编程时，你将进行大量的编码工作，并希望获得尽可能多的支持来生成干净、无错误的代码。你不仅需要像静态Web页面那样测试代码的外观，还需要测试其运行情况，而且不仅要在一种浏览器上测试，还要在多种浏览器上测试。因此，你需要一个文本编辑器，或者其更高级的形式——一种集成了更多功能的开发工具，用来编写代码。该工具不仅要支持HTML，还要支持JavaScript和PHP。你还需要在自己的计算机上运行一个支持所有语言（特别是PHP和MySQL）的测试服务器环境。最后，你需要能够访问几种流行的浏览器。

> **注意**
> 本书面向Microsoft Windows、Windows XP、Windows Vista或Windows 7用户编写。虽然本书中的大部分讨论也适用于Mac和Linux用户，但本节专门针对Windows。Mac和Linux有自己的一套编辑器、服务器和浏览器。

### 选择开发工具

动态Web编程最重要的工具是一个功能强大的文本编辑器或开发工具，它能辅助你编写代码，而不是试图替你完成编码。市面上有许多此类工具，从免费附带在Windows中的记事本（Windows Notepad），它允许你输入代码并保存为文件，到Adobe Dreamweaver（售价399美元），它在一个准所见即所得（WYSIWYG，即看到的就是得到的）环境中为你创建动态Web代码。如下所示的Windows记事本，在紧急情况下或许可以用来输入少量代码，但当你看到免费可下载编辑器所提供的功能和支持水平后，你会把Windows记事本扔进软件垃圾桶。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_20_0.png)

> **注意**
> 有人可能会告诉你，Microsoft Word可以从你在文字处理器中排版的文本和图形生成HTML文件。虽然这是事实，但生成的代码既不太高效，也不易于修改或定制。此外，Word不提供任何Web编程支持。因此，我们强烈建议不要使用Word进行网站开发。

#### 功能齐全的开发套件

与Windows记事本处于光谱另一端的是Adobe Dreamweaver（参见图P1-1）和Microsoft Expression Web（Microsoft售价299美元，用于替代FrontPage的产品）。这两者提供的功能远不止编辑器，旨在与Adobe或Microsoft提供的其他工具集成使用。除了价格因素（你可以在Amazon和其他地方获得折扣）之外，这些套件存在两个主要问题，使我们无法推荐使用它们：

- **所见非所得** 网页的显示效果取决于所使用的浏览器。这两个套件试图向你展示最终显示页面的样子，但其结果可能与实际显示有显著差异，并可能导致你以不同于其他方式来布局页面。
- **难以管理且效率低下的代码** 由所见即所得页面布局生成的代码，尤其是动态Web功能的代码，非常复杂、低效，且难以修改和定制。如果你想在Dreamweaver创建了PHP代码的页面上自行编写任何PHP代码，这将极其困难。

#### 强大的替代方案

在Windows记事本和Adobe Dreamweaver之间的广阔光谱中，有许多值得关注的Web开发工具，它们提供的功能远超Windows记事本，而且可以免费下载或成本相对较低。你可以在多个网站上找到Web开发套件的比较，包括 http://sixrevisions.com/tools/the-15-most-popular-text-editors-for-developers/ （该网站上有许多关于Web开发的有用文章）和 http://en.wikipedia.org/wiki/Comparison_of_html_editors。

在评估Web开发工具时，你可能希望考虑所选工具中多项功能的可用性。其中包括：

- **代码辅助** 在你输入代码时提供上下文相关的辅助，如图所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_21_1.png)

- **代码补全** 自动为你输入的开始标签提供结束标签。
- **代码高亮** 为代码的各个部分提供颜色编码，以便于你轻松识别。
- **代码验证** 检查你的代码，并告诉你是否发现了不正确的内容。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_22_0.png)

- **浏览器视图** 在开发工具中以浏览器的形式显示你的代码效果。
- **大纲视图** 提供代码的大纲，如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_22_1.png)

- **行号** 为每一行代码编号，以便你能快速找到错误消息中提到的行。
- **查找和替换** 允许在一次操作中更改同一项目的多个实例。
- **宏功能** 允许录制一组步骤，以便可以重复执行。
- **多文件打开** 允许你同时打开多个代码页面，以便在它们之间进行比较和复制代码。
- **多语言支持** 提供对多种编程语言的支持，如HTML、CSS、JavaScript、PHP、MySQL和Ajax。对于本书，前五种最为重要。
- **文件管理** 在开发工具内部提供Windows资源管理器的功能。
- **FTP传输** 允许你将网页和应用程序上传和下载到托管服务器。
- **版本控制** 提供跟踪网站版本的能力：哪些版本在服务器上，开发计算机上哪个版本是最新的，哪些版本是归档副本。



**图 P1-2** Aptana Studio 是一款功能全面的开发工具，免费且拥有良好的技术支持。

**Aptana Studio**，如**图 P1-2**所示，是我们选择的 Web 开发工具，本书中将出现许多它的截图。Aptana Studio 是一个完全集成的开发环境（IDE），将文本编辑与网页的可视化浏览器显示相结合，同时提供多种工具来帮助您编写整洁的代码。Aptana 具备前文提到的大多数功能（插图均来自 Aptana），它是免费的，并且拥有庞大的用户社区及其创建者的支持。对我个人而言，Aptana 尤其重要的是能够为本书讨论的所有语言（以及 Ajax 和 Ruby on Rails）提供代码辅助、代码补全和代码着色或语法高亮功能。Aptana 还可以在其窗口中打开浏览器窗格（参见**图 P1-3**），以及进行代码验证和文件管理。您可以从 www.aptana.com 免费下载 Aptana Studio。您还可以购买专业版，但就本书的内容而言，免费版本（Community Edition）已完全够用。

### 选择测试服务器

静态网页以及部分使用 JavaScript 的动态网页完全在浏览器中显示和运行，称为*客户端*应用程序。测试这些页面所需的只是一个浏览器。使用*服务器端*功能的动态网页在服务器而非客户端浏览器中运行，例如用 PHP 和 MySQL 编写的网页，如果您想在开发计算机上测试这些页面，则需要安装服务器。两种流行的本地 Web 服务器替代方案是 Microsoft Internet Information Server (IIS) 和 Apache。IIS 包含在某些版本的 Windows 中，尤其是 Windows Server 2003 和 2008，因此您可能已经拥有它。Apache 可以免费下载，它是名为 *XAMPP*（*X* 代表跨平台，包含 Apache、MySQL、PHP 和 Perl 的服务器）的集成包的一部分，该包同时包含 PHP 和 MySQL。

由于 XAMPP 包含了您所需的所有服务器和开发工具，并且可供所有使用 Windows XP、Vista 或 Windows 7 的用户轻松获取，本书假设您将使用它，并建议您在需要时立即下载和安装。

> 注意
> 虽然 XAMPP 有 Mac OS X 版本，但您可能想要研究一下 MAMP（Macintosh servers for Apache, MySQL, and PHP），网址为 www.mamp.info/en/download.html。MAMP 通常被认为在 Mac 上优于 XAMPP。

#### 获取和安装 XAMPP

XAMPP 使用标准的 Windows 安装程序技术来下载和安装 Apache、PHP 和 MySQL：

1. 在您想要安装测试服务器的计算机上，打开网站 www.apachefriends.org/en/xampp-windows.html。向下滚动到大约第二页的底部，在最新版本的 Windows 版 XAMPP 下，点击**Installer**。跳过广告页面，您将被带到下载站点，在那里，根据您的 Windows 版本，下载将自动开始；或者您可能需要右键点击浏览器顶部的消息，然后点击**Download File**。

2. 点击**Run**直接运行，或点击**Save**将文件保存到您的磁盘（我们的偏好，以防出现问题时无需重新下载）。

3. 下载完成后，您可以点击**Run**或**Go to Folder**。如果您进入文件夹，双击 **xampp-win32-1-7-1-installer.exe**（根据您执行此操作的时间，最后两位数字可能有所不同），如果您开启了用户账户控制（UAC），点击**Yes**允许程序运行，然后点击**Run**。

4. 选择您要使用的语言，然后点击**OK**。如果您使用的是 Vista 或 Windows 7，可能会提示您需要关闭 UAC，并建议保持关闭状态。再次点击**OK**，然后点击**Next**。

5. 选择目标位置（建议使用 C:\xampp），然后点击**Next**。点击**Install**。安装将开始。

6. 安装完成后，点击**Finish**，然后点击**Yes**打开 XAMPP 控制面板。

7. 点击 Apache 和 MySQL 对面的**Start**以启动这两项服务，然后点击**Close**（右上角的 X）关闭控制面板。

8. 要检查 XAMPP 是否正在运行，请打开 Web 浏览器（Internet Explorer 或 Firefox），在地址栏中输入 localhost。XAMPP 应该会打开。选择您要使用的语言，XAMPP 将在您的浏览器中打开，如**图 P1-4**所示。

**图 P1-4** XAMPP 提供 Apache Web 服务器、PHP 编程环境和 MySQL 关系数据库程序等。

#### 测试浏览器

大多数个人计算机用户使用以下四种浏览器之一访问 Web：随 Windows XP 附带的 Microsoft Internet Explorer 6 (IE 6)；随 Windows Vista 附带的 Microsoft Internet Explorer 7 (IE 7)；将随 Windows 7 附带的 Internet Explorer 8 (IE 8)；以及可免费下载的 Mozilla Firefox。在本书撰写之时（2009 年 5 月），来自 www.w3schools.com 的浏览器用户分布为：Firefox 占 47.7%；IE 8 占 5.2%；IE 7 占 21.3%；IE 6 占 14.5%；Google Chrome 占 5.5%；其他（主要是 Safari 和 Opera）占 5.2%。

您可以从 Microsoft 网站为 Windows XP 下载 Internet Explorer 7，网址为 www.microsoft.com/windows/downloads/。点击**Windows Internet Explorer | Windows Internet Explorer 7 for Windows XP**。

同一网页（www.microsoft.com/windows/downloads/）有 IE 8 的链接；点击**Download Now**。如果您想要 Vista 版本，再次点击**Download Now**。如果您想要 XP 版本，点击**Other Locales and Versions**。无论哪种情况，请按照出现的说明操作。

> 注意
> 一台计算机上只能安装一个版本的 Internet Explorer。

> 提示
> 您无法在 Vista 上安装 IE 6，但可以使用 Internet Explorer Application Compatibility VPC Images，它允许您在 Windows XP 或 Windows Vista 上测试 IE 6、IE 7 和 IE 8 上的网页。您可以从 www.microsoft.com/downloads/en/details.aspx 下载此工具，并搜索"IE App Compat VHD"。您还必须下载并运行最新版本的 Virtual PC，可在与 IE App Compat VHD 相同的页面找到。

# 第 1 章

## XHTML 和 HTML 回顾

## 关键技能与概念

- 理解 X/HTML
- 回顾基本 HTML 标签
- 设置段落样式
- 应用字符样式
- 显示特殊字符
- 使用图像和图像映射
- 添加超链接和书签
- 创建表单和表格

HTML（超文本标记语言）是 Web 的基础编程语言，为所有网页提供骨架。您可以在页面中添加 JavaScript 和 PHP，但围绕这些代码的结构是 HTML。虽然 HTML 为网页提供了关键的基础设施，但它也已经存在了一段时间；它未能跟上新网站的需求，尤其是智能手机和 PDA（个人数字助理）上的网站。因此，创建了两种补充技术：

- **CSS（层叠样式表）**的开发旨在大幅增强网页的布局和格式化。CSS 在第 2 章中介绍。
- **XML（可扩展标记语言）**是一种*元*语言，即用于开发其他语言的语言，可以在其中定义标记标签以及许多其他元素。使用 XML，HTML 被重写，从而创建了 XHTML（可扩展 HTML）。XHTML 在本章中进一步讨论，并在整本书中使用。

本书的第一部分提供了基于 XHTML 和 CSS 的坚实且最新的基础，您可以在此基础上使用 JavaScript、PHP 和 MySQL 构建动态网站。在本书中 wherever applicable，CSS 和 XHTML 将替代等效的 HTML。



HTML、XML、XHTML 和 CSS 均由万维网联盟（W3C——www.w3c.org/)制定的推荐标准控制。截至本文撰写之时，最新的推荐标准为 CSS 2（2008年4月11日）、XML 1.1 第二版（2004年2月4日，2006年8月16日修订）、XHTML 1.0 第二版（2000年1月26日，2002年8月1日修订）以及 HTML 4.01（1999年12月24日）。可以看出，HTML 已经相当古老，而 XHTML 也并不年轻。更新的标准正在制定中（HTML 5 的工作草案于2008年6月10日发布），但进程非常缓慢，部分原因是该联盟规模庞大，包括了大多数活跃在网络上的组织、学者和个人。

> **注意**
为了确保您的网站能在尽可能多的浏览器中正常显示，请仅使用 HTML、CSS 和 XHTML 的推荐标准。

### XHTML 与 HTML

请记住，XHTML 只是以 XML 形式书写的 HTML。它是在一套更标准化的规则下书写的 HTML，因此浏览器更容易解读您的意图。这减少了 HTML 书写方式上的灵活性或宽松度，但也意味着浏览器软件可以更简单。后者在将浏览器适配到智能手机或 PDA 时非常重要。此外，纯 HTML 可能会在脚本中造成一些严重问题，例如标签不匹配和缺少闭合标签。

那么，既然 HTML 如此古老和局限，为什么还要讨论它呢？首先，因为 XHTML 只是带有规则集的 HTML。其次，数十亿的网页使用 HTML 编写，数百万的人知道如何使用它。而且，它易于使用，这是网络飞速发展的重要原因之一。因此，牢固掌握 HTML 仍然非常重要；您只需要按照 XHTML 规则来使用它，并忽略那些已被 CSS 取代的旧格式和布局标签。本书假定您希望这样做，示例也反映了这一点。

#### XHTML 规则

XHTML 规则全部涉及 HTML 的*书写方式*，而非*书写内容*。XHTML 使用与 HTML 相同的标签、属性和值（请参阅本章后面的"HTML 回顾"）。区别在于*语法*，即代码各部分组合在一起的方式。一般而言，**XHTML** 只是更严格的 HTML 形式。

- 必须包含完整的标题标签集、DOCTYPE、html、head 和 body。如果使用 Aptana 及其标准模板（如下所示），这将自动完成。

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
        <title>Untitled Document</title>
    </head>
    <body>
    </body>
</html>
```

- 所有开始标签必须有闭合标签。同样，Aptana 会为您填充闭合标签。

- 所有标签、属性和预定义属性值必须为小写。

- 所有属性值必须用引号括起来。

- 所有属性值必须明确声明，不能假定，即使它们与属性相同。

- 必须先闭合内层标签，再闭合外层标签。

所有这些规则只是对 HTML 原始定义的严格解释，并且合乎常理。Aptana 帮助您遵循这些规则，而且养成习惯并不难。当您这样做时，您能更有把握地确保代码能被广泛的浏览器正确支持。

#### 已弃用的 HTML 标签

随着 CSS 的日益使用和普及，许多格式和布局标签已被标记为从推荐的 HTML 标准中移除。这些标签称为*已弃用标签*，意思是它们已不受青睐。目前 W3C 的已弃用标签包括：

- **applet**（Java 小程序）
- **basefont**（字体特性）
- **center**（居中对齐的 `div`）
- **dir**（目录列表）
- **font**（字体更改）
- **frame**（创建框架）
- **frameset**（定义框架集）
- **iframe**（创建浮动框架）
- **isindex**（单行提示）
- **menu**（菜单列表）
- **noframe**（框架的替代方案）
- **s**（删除线样式）
- **strike**（删除线文本）
- **u**（下划线样式）

> **注意**
与框架相关的标签并未被 W3C 正式弃用，但不被鼓励，因为框架页面可能会干扰搜索引擎。

除了这些标签，一些可接受标签的属性也已被弃用。这些包括

- align（左对齐、右对齐、居中）
- alink、link、vlink（链接颜色）
- background（背景图像）
- bgcolor（背景颜色）
- compact（减少中间间距）
- target（指定框架）
- text（文本颜色）
- type（类型样式）

实现 XHTML 有三个级别：严格（strict）、过渡（transitional）和框架集（frameset）。该级别在网页的 DOCTYPE 行中标识，如前面 Aptana 模板所示。"严格"意味着您已遵循所有 XHTML 规则，且未使用任何已弃用或与框架相关的标签。"过渡"意味着您已遵循规则，但希望使用一些已弃用的标签。"框架集"意味着您已遵循规则，但希望使用与框架相关的标签。本书假定您希望使用严格的 XHTML 级别，且不讨论任何已弃用的标签。

> **注意**
尽管 Web 有标准机构（W3C），但遵守其标准是自愿的。因此，您不能指望所有 Web 浏览器都以相同方式解读您的 HTML 代码。一些差异相对较小，而另一些则不然。在发布之前，最好在主流浏览器（IE 6、IE 7 和 Firefox）中测试您的工作。

### HTML 回顾

HTML 是一系列标签，用于标识网页中的元素。*标签或标记标签* 由尖括号（<>）括起的标签名称组成，通常成对出现。标签放置在您想要标识的元素（通常是文本）的开头和结尾；结束标签的名称前加有斜杠。例如，

`<title>这是一个标题</title>`

使用 Title 标签标识将放置在浏览器窗口标题栏中的文本。在 XHTML 中，标签应使用小写。标签围绕文本放置以标识它及其处理方式。

> **注意**
本章不会提供详尽的 HTML 覆盖，也不会涵盖每个 HTML 标签的每个细微差别。这两个领域在 Web 上都有详尽的覆盖，特别是 www.w3c.org。

除了标签名称外，标签还可以包含一个或多个*属性*来特惠标签的功能。例如，如果您想在网页上显示图像，可以使用此标签：

`<img src="rodie.jpg" />`

**img** 标签的*属性*是 **src**，而 **src** 属性的*值*是 **rodie.jpg**。

> **注意**
在本章的列表和 HTML 示例中，标签以粗体显示，而属性及其值则不是。此外，续行相对于其父行缩进。这些约定仅用于可读性。Aptana 默认会对 HTML 进行颜色编码和缩进以提高可读性。深红色用于标签，鲜红色用于属性名称，蓝色用于属性值，黑色用于纯文本。您可以通过点击 **Windows | Preferences** 并选择 **Aptana | Editors | HTML | Colors** 来更改 Aptana 使用的颜色。

#### 使用基本标签

所有网页都必须包含一组基本标签。这些标签将文档标识为 HTML 或 XHTML 文档，并标识文档的主要部分。在 XHTML 中，这些标签必须包含在网页中以符合标准。基本标签由 Aptana 模板自动放置在页面上，如清单 1-1 所示，并在表 1-1 中与其属性一起描述。

> **提示**
本书中的列表以及本书其余部分的列表均可在线获取，网址为 www.matthewstechnology.com/。请参阅本书的引言以了解如何最好地访问在线列表。

##### 清单 1-1  基本标签集

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
    <head>
    <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
    <title>Untitled Document</title>
    </head>
    <body>
    
    </body>
</html>
```

| 标签或属性 | 说明 |
| --- | --- |
| <!DOCTYPE ...> | 标识文档遵循给定的 HTML 或 XHTML 版本。 |
| <html> </html> | 标识中间的内容为 HTML。 |
| <head> </head> | 包含标题和文档标识信息。<title> 标签在 <head> 标签中是必需的。 |
| <title> </title> | 标识将放置在浏览器标题栏中的标题。 |
| <meta ...> | 为元素分配内容，该内容可由服务器或浏览器使用，且无法在其他方面通过 HTML 分配；在清单 1-1 中，"Content-Type" 被分配给 http-equiv 并放置在 <head> 标签内。 |
| content | 标识有关页面的信息。 |
| http-equiv | 标识 meta 标签的使用方式。 |
| name | 提供可供搜索引擎使用的信息。 |
| <body> </body> | 指定显示给用户的页面部分，并定义整体页面属性。 |

表 1-1  基本 HTML 标签集



 **注意**

在本章的标签和属性表格中，标签用其尖括号表示，属性则从左侧缩进。

#### 设置段落样式

段落样式包括基本段落定义和标题；换行；项目符号列表、编号列表和定义列表；预格式化段落；注释；以及水平线或横线。除非使用预格式化样式，否则 HTML 会忽略普通的行尾、一个以上的多余空格和制表符。除非使用段落标签，否则行只是简单地换行以适应分配给它们的空间。列表 1-2 展示了段落样式的示例。此列表与列表 1-1 中的标签结合，生成了图 1-1 中所示的网页。段落样式在表 1-2 中描述。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_35_0.png)

**图 1-1** 将列表 1-2 放置于列表 1-1 的 Body 标签之间所产生的网页列表

```
Listing 1-2  Example of using paragraph style tags

<h2>This is a 2nd-level heading</h2>
<p>This is the first line of a paragraph which ends with a line break.<br />
This is the second line of a paragraph.</p>
<hr>
<ul>
  <li>This is item 1 in a bulleted (unordered) list</li>
  <li>This is item 2 in a bulleted list</li>
</ul>
<ol>
  <li>This is item 1 in a numbered (ordered) list</li>
  <li>This is item 2 in a numbered list</li>
</ol>
<!-- This is a comment, it is ignored by a browser and not displayed -->
<pre>This line will be reproduced with
  all its spaces, tabs, and line endings.</pre>
<address>This text will be italicized</address>
```

| 标签或属性 | 说明 |
|---|---|
| `<p>` `</p>` | 标识段落的开始和结束 |
| `<hn>` `</hn>` | 标识六种标题样式之一（*n* = 1 到 6） |
| `<br />` | 强制换行，类似于在 Microsoft Word 中按 SHIFT+ENTER |
| `<hr>` | 创建水平横线 |
| `<ol>` `</ol>` | 包含有序（编号）列表 |
| `<ul>` `</ul>` | 包含无序（项目符号）列表 |
| `<li>` `</li>` | 标识编号或项目符号列表中的项目 |
| `<dl>` `</dl>` | 包含定义列表 |
| `<dt>` `</dt>` | 标识待定义的术语，显示在窗口左侧 |
| `<dd>` `</dd>` | 标识紧随其前的术语的定义，从左侧缩进 |
| `<address>` `</address>` | 标识一段斜体文本 |
| `<blockquote>` `</blockquote>` | 标识一段左右两侧都缩进的段落，类似于引文的格式 |
| `cite` | 标识 `<blockquote>` 的 URL |
| `<!-- -->` | 标识浏览器将忽略且不显示的注释 |

表 1-2 段落样式 HTML 标签（*续*）

| 标签或属性 | 说明 |
|---|---|
| `<div>` `</div>` | 标识页面的一个分区 |
| `class` | 标识用于应用样式的 div 类 |
| `id` | 附加一个名称用于链接 |
| `<pre>` `</pre>` | 标识预格式化文本，其中所有空格、制表符和行尾都保留 |

表 1-2 段落样式 HTML 标签（续）

> **注意**
您可以嵌套列表，并获得自动缩进效果。

#### 应用字符样式

字符样式决定一个或多个字符的外观或行为方式，分为两种形式。*逻辑*字符样式由浏览器定义，可以以浏览器设定的任何方式显示。*物理*字符样式有严格的定义，在所有浏览器中都将相同。字符样式标签的示例见列表 1-3，而图 1-2 展示了 Microsoft Internet Explorer 7 和 Mozilla Firefox 3 如何显示它们。请注意其中的差异之少。表 1-3 描述了大多数字符样式。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_37_0.png)

图 1-2 Microsoft Internet Explorer 7 和 Mozilla Firefox 3 中显示的字符样式标签

# 第 1 章：XHTML 和 HTML 复习

**注意**
图 1-2 证明了浏览器会忽略行尾，除非它们被 `<p>`、`<br>` 或其他段落样式标记。

##### 列表 1-3 字符样式标签使用示例

```
<b>This text is bold</b>
This text is normal size, <big>this is larger</big>
This text is normal size, <small>this is smaller</small>
<code>This is normally fixed-width font</code>
<em>This text is normally italic</em>
<i>This text is italic</i>
<strong>This text is normally bold</strong>
```

**注意**
字符样式和格式曾经有一些已弃用的标签，例如 `font`、`strike` 和 `u`。

| 标签 | 说明 |
| :--- | :--- |
| `<b>` `</b>` | 将粗体物理字符样式应用于所包含的字符 |
| `<big>` `</big>` | 使所包含的字符增大一号 |
| `<cite>` `</cite>` | 将引用逻辑字符样式应用于所包含的字符；通常为斜体 |
| `<code>` `</code>` | 将代码逻辑字符样式应用于所包含的字符；通常为等宽字体 |
| `<dfn>` `</dfn>` | 将定义逻辑字符样式应用于所包含的字符；通常为斜体 |
| `<em>` `</ em>` | 将强调逻辑字符样式应用于所包含的字符；通常为斜体 |
| `<i>` `</i>` | 将斜体物理字符样式应用于所包含的字符 |
| `<kbd>` `</kbd>` | 将键盘逻辑字符样式应用于所包含的字符；通常为等宽字体 |
| `<samp>` `</samp>` | 将示例逻辑字符样式应用于所包含的字符；通常为等宽字体 |
| `<small>` `</small>` | 使所包含的字符减小一号 |
| `<strong>` `</strong>` | 将强强调逻辑字符样式应用于所包含的字符；通常为粗体 |
| `<sub>` `</sub>` | 将下标物理字符样式应用于所包含的字符 |
| `<sup>` `</sup>` | 将上标物理字符样式应用于所包含的字符 |
| `<tt>` `</tt>` | 将打字机文本物理字符样式应用于所包含的字符；等宽字体 |

表 1-3 字符样式 HTML 标签

#### 显示特殊字符

HTML 将小于号、大于号和 & 符号定义为具有特殊含义，因此它们不能作为普通文本使用。要正常使用这些字符，请按如下方式替换：

| 要显示 | 输入 |
| --- | --- |
| 小于号（<） | `&lt;` 或 `&#60;` |
| 大于号（>） | `&gt;` 或 `&#62;` |
| & 符号（&） | `&amp;` 或 `&#38;` |

键盘上可以输入的所有其他字符将按原样显示。此外，HTML 还定义了许多其他字符，可以通过在需要显示该字符的位置输入*转义序列*来显示。转义序列可以采用数字或文本格式，如前面提到的三个特殊字符所示。无论哪种情况，转义序列都以 & 符号（&）开头，以分号（;）结尾。在数字格式中，& 符号后跟一个数字符号（#）和一个代表该字符的数字。所有字符，无论是否在键盘上，都可以用数字转义序列表示。文本格式仅针对部分字符定义，排除了键盘上的大多数字符。两种格式的其他示例见表 1-4。

## **注意**

与 HTML 的其他部分不同，转义序列是区分大小写的——例如，不能使用 `&LT;` 来表示小于号。

| 字符 | 名称 | 数字序列 | 文本序列 |
| --- | --- | --- | --- |
| … | 水平省略号 | `&#133;` | `&hellip;` |
| • | 项目符号 | `&#149;` | `&bull;` |
| ™ | 商标 | `&#153;` | `&trade;` |
| © | 版权 | `&#169;` | `&copy;` |
| Æ | AE 连字 | `&#198;` | `ampersand;AElig;` |
| Ä | A 变音符 | `&#228;` | `&auml;` |
| É | E 尖音符 | `&#233;` | `&eacute;` |
| Õ | O 波浪号 | `&#245;` | `&otilde;` |

**表 1-4** 字符转义序列示例

提示

欲获取完整的字符转义序列列表，请打开
www.w3c.org/markup/html-spec/html-spec_13.html。

#### 使用图像和图像映射

图像是通过图像（`<img />`）标签添加到网页中的，该标签指定了图像的路径和文件名，以及一些属性，如大小、定位、边距和边框。其中一个属性 ismap 标识该图像附有图像映射。图像映射是服务器使用的一个单独的 MAP 文件，用于将图像的区域与 URL 关联起来。要使用 ismap，必须将图像标签包含在锚点标签中（参见下一节"添加超链接和书签"）。列表 1-4 中给出了几个示例，并在图 1-3 中展示。表 1-5 描述了许多图像属性。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_40_0.png)

图 1-3 列表 1-4 中图像标签的使用示例



 清单 1-4 中的 `&nbsp;`（也可以是 `&#160;`）是不间断空格，用于在此处或配合 Paragraph 标签添加空间，以创建 HTML 会保留的空白行（段落）。

##### 清单 1-4 使用 Image 标签的示例

```
<p><img src="hibiscus.jpg" alt="A picture of a hibiscus" width="166" height="190" /> 这是一张芙蓉花的图片...</p>
<p>&nbsp;</p>
<p><img src="undercon.gif" alt="Under Construction" width="40" height="38" />
这是"正在建设中"符号...</p>
```

指定 `height` 和 `width` 可以加快加载速度，因为浏览器可以快速为图像绘制占位符，让文本在图像绘制的同时继续加载。如果没有这些尺寸，文本的加载必须等待图像绘制完成后才能确定剩余文本的位置。当前浏览器如果只给定一个尺寸（`height` 或 `width`），会根据图像当前的纵横比自动缩放另一个尺寸。

#### 添加超链接和书签

超链接提供了点击对象并将浏览器显示内容（`焦点`）转移到与该对象关联的地址的能力。HTML 使用 Anchor 标签（`<a></a>`）实现超链接，该标签指定其包含的文本或图形是一个超链接、书签或两者兼有。如果该标签是 `超链接` 且其内容被选中，则焦点会转移到当前页面或网站的另一个位置，或者另一个网站。如果该标签是 `书签`，则另一个 Anchor 标签可以引用它，并将焦点转移到该位置。

如上所述使用的图像是假设整个图像都是超链接。图像也可以被分割成多个区域，每个区域都是一个链接或 `热点`。要将图像分割成多个链接，需要使用通过 Map 标签实现的 `图像映射`。Map 标签包含 Area 标签，用于定义图像特定区域的形状及其指向的链接。

清单 1-5 提供了一些 Anchor、Map 和 Area 标签的示例，如图 1-4 所示。表 1-6 描述了这些标签及其属性。

| 属性 | 说明 |
| --- | --- |
| alt | 标识当鼠标指针放在图像上时显示的替代文本，或图像无法显示时显示的文本 |
| height | 指定图像的高度，以像素为单位 |
| ismap | 指定服务器端图像映射 |
| src | 标识图像的路径、文件名或 URL |
| usemap | 指定客户端图像映射 |
| width | 指定图像的宽度，以像素为单位 |

##### 表 1-5 Image 标签属性

> **注意**
> 图 1-4 中的手指指向标记为 "screen" 的热点，如窗口底部所示（".../Listing 1-5.html#screen"）。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_42_0.png)

图 1-4 清单 1-5 中定义的超链接和书签，包括一个热点链接。（Lenovo IdeaCentre K220 台式电脑，照片由 Lenovo 提供，已获授权使用。）

##### 清单 1-5 超链接和书签示例

```
<p>这是指向<a href="default.html">首页</a>的链接。</p>
<p><a name="This ">This </a>是一个书签。</p>
<p>这个<a href="#This ">链接</a>会带你到该书签。</p>
<p><map name="ComputerMap">
  <area shape="polygon" coords="163, 121, 197, 145, 91, 183, 55,
    157" href="#keyboard">
  <area shape="polygon" coords="6, 90, 147, 87, 148, 115, 46, 145,
    2, 124" href="#processor">
  <area shape="rect" coords="30, 6, 124, 70" href="#screen"></map>
  <a href="computer.map" />
  <img align="bottom" src="Lenovo K220.jpg" width="200" ismap
    usemap="#computermap" height="186" /></a></p>
```

## 注意

Area 标签的 shape 属性可以省略，此时将假定默认为矩形。

| 标签或属性 | 说明 |
| --- | --- |
| `<a> </a>` | 指定超链接的定义 |
| accesskey | 指定链接的快捷键 |
| href | 标识目标 URL，可以是书签、页面或网站 |
| name | 标识此位置的书签 |
| tabindex | 标识该链接在 Tab 键顺序中的位置 |
| `<map> </map>` | 指定图像映射的定义 |
| name | 标识图像映射的名称 |
| `<area> </area>` | 指定一个图像区域的定义 |
| accesskey | 指定链接的快捷键 |
| coords | 标识所定义形状的坐标，使用图像像素中各点的 x 和 y 位置 |
| href | 标识焦点转移到的书签或 URL |
| nohref | 指示给定区域不执行任何操作 |
| shape | 指定所定义形状的类型，可以是 circ、circle、poly、polygon、rect 或 rectangle |
| tabindex | 标识该链接在 Tab 键顺序中的位置 |

##### 表 1-6 Anchor、Map 和 Area 标签及其属性

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_44_0.png)

图 1-5 由清单 1-6 创建的表单

#### 定义表单

HTML 中的表单由其包含的输入字段定义。每个输入字段由其类型、名称以及可能的默认值定义。有多种字段类型，你可以在其周围包装文本和格式，以定义几乎任何你想要的表单。一个示例显示在清单 1-6 中，并在图 1-5 中展示。表 1-7 描述了与表单相关的标签和属性。

```
清单 1_xx 表单示例

<h1>这是一个表单</h1>
<form action="saveresults" METHOD="post">
  姓名：&nbsp; &nbsp; <input type="text" size="50" maxlength="256"
    name="name"><br />
  地址：<input type="text" size="50" maxlength="256"
    name="address"><br /><br />
  发送数据？是 <input type="radio" name="Send" value="Yes">
    否 <input type="radio" name="Send" value="No">&nbsp; &nbsp;
  用于什么类型的产品？<select name="Product" multiple
    size="1">
    <option selected value="Laptop">笔记本电脑
    <option value="Desktop">台式机
  </select><br />
```

```
勾选是否为会员 <input type="checkbox" name="Member"
    Value="true">
<br /><br />
<input type="submit" value="发送"> <input type="reset"
    value="重置">
</form>
```

| 标签或属性 | 说明 |
| --- | --- |
| `<form>` `</form>` | 指定表单的定义 |
| action | 指定提交时处理表单的 URL |
| method | 指定表单发送到服务器的方式：get 将数据作为 URL 的一部分传输；post 只在处理代码查询时传输数据，更安全 |
| `<input>` | 标识一个输入字段 |
| accesskey | 指定字段的快捷键 |
| checked | 如果 type=checkbox 或 radio，确定默认情况下是否选中（true）或未选中（false） |
| disabled | 指定该字段不能使用 |
| maxlength | 指定在文本字段中可以输入的最大字符数 |
| name | 指定字段的名称 |
| readonly | 指定字段内容不能更改 |
| size | 指定文本字段的宽度（以字符为单位），或文本区域的宽度和高度（以字符和行数为单位） |
| src | 如果 type=image，指定图像的 URL |
| tabindex | 标识该字段在 Tab 键顺序中的位置 |
| type | 指定字段类型为 checkbox、hidden、image、password、radio、reset、submit、text 或 textarea |
| value | 指定字段的默认值 |
| `<select>` `</select>` | 指定下拉菜单的定义 |
| disabled | 指定该定义不能使用 |
| multiple | 指定可以在菜单中选择多个项目 |
| name | 指定菜单的名称 |
| size | 指定菜单的高度 |

## **表 1-7** 表单标签和属性

标识菜单中的一项

指定该选项不能使用

指定选项的标签

指定该选项为默认选项

指定选项被选中时的值

| 标签或属性 | 说明 |
| --- | --- |
| `<option>` | 标识菜单中的一项 |
| disabled | 指定该选项不能使用 |
| label | 指定选项的标签 |
| selected | 指定该选项为默认选项 |
| value | 指定选项被选中时的值 |

#### 创建表格

HTML 提供了非常丰富的标签集来定义表格、单元格、边框和其他属性。尽管最初的 HTML 表格规范已经很丰富，但 Microsoft 和 Netscape 都对其进行了许多扩展。由于这些扩展在两家公司之间并不一致，因此需要谨慎使用。清单 1-7 提供了创建图 1-6 所示简单表格的 HTML 示例。表 1-8 显示了主要的表格标签及其属性。

##### 清单 1-7 表格示例

```
<h2>一个新表格</h2>
<table border="2" cellpadding="3" cellspacing="4" width="100%" >
  <caption>这是表格标题</caption>
  <tr valign="bottom">
    <th align="left" width="25%">单元格 1，表头</th>
    <td colspan="2" width="25%">单元格 2，此单元格跨两列</td>
    <td width="10%">单元格 3</td>
    <td width="10%">单元格 4</td>
  </tr>
  <tr>
    <td width="25%">单元格 5，25%</td>
    <td width="25%">单元格 6，25%</td>
    <td width="25%">单元格 7，25%</td>
    <td width="10%">10%</td>
  </tr>
  <tr>
    <td rowspan="2" width="25%">单元格 9/13，这些单元格已合并</td>
    <td width="25%">单元格 10</td>
    <td width="25%">单元格 11</td>
    <td width="10%">单元格 12</td>
  </tr>
</table>
```



 ```
<tr>
    <td width="25%">Cell 14</td>
    <td width="25%">Cell 15</td>
    <td width="10%">Cell 16</td>
</tr>
</table>
```

## 提示

并没有规定`<tr>` `</tr>`标签必须分开在不同行，如清单1-7所示，但这样做会使区分行（`<tr>` `</tr>`）和单元格（`<td>` `</td>`）变得容易得多。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_47_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_47_1.png)

图1-6 使用清单1-7创建的表格。注意IE 7和Firefox 3之间的一些差异。

第1章：XHTML与HTML复习

31

| 标签或属性 | 说明 |
|---|---|
| `<table>` `</table>` | 指定表格的定义 |
| border | 指定表格中所有单元格周围边框的大小，单位为像素 |
| cellspacing | 指定单元格之间的间距，单位为像素；未指定时默认值为0 |
| cellpadding | 指定单元格壁与其内容之间各方向的间距，单位为像素；未指定时默认值为0 |
| frame | 指定表格的哪些外边框显示——void（无）、above（仅顶部）、below（仅底部）、hsides（水平边）、vsides（垂直边）、lhs（左侧）、rhs（右侧）、box或border（全部） |
| rules | 指定表格的哪些内边框显示——none、basic（标题、主体和页脚部分之间的水平线）、rows、cols、all |
| summary | 指定表格的用途 |
| width | 指定表格的宽度，可以是特定像素数或窗口的百分比 |
| `<tr>` `</tr>` | 标识表格中单个单元格行 |
| align | 指定此行中单元格的文本在单元格内左对齐、居中或右对齐 |
| valign | 指定行中的文本可以与单元格的顶部、居中、基线或底部对齐；如果未指定，文本默认居中对齐 |
| `<td>` `</td>` | 标识表格中的单个数据单元格（`<td>`）或表头单元格（`<th>`） |
| `<th>` `</th>` | |
| align | 指定此单元格中的文本在单元格内左对齐、居中或右对齐 |
| colspan | 指定单元格的跨列数 |
| rowspan | 指定单元格的跨行数 |
| nowrap | 指定表格中的文本不能换行以适应较小的单元格，强制单元格放大 |
| `<caption>` `</caption>` | 标识表格的标题 |
| `<col>` `</col>` | 标识列组 |
| align | 指定列组的水平对齐方式，左对齐、居中或右对齐 |
| span | 指定列组中的列数 |
| valign | 指定列组的垂直对齐方式，顶部或底部 |
| width | 指定列宽 |

表1-8 表格标签和属性

#### HTML编写资源

网上有许多关于HTML编写的优秀资源。以下是一些最重要的资源列表。其中一些文档按照互联网标准来看已经相当古老（数年之久），但基本信息仍然有效。重要的是要理解，HTML已经成为一种成熟的网络语言。尽管如此，对这些文档提供的HTML的扎实理解，将为你进行动态网页编程打下坚实的基础。

**提示**

没有border属性的表格将没有边框，但会占用与边框为1时相同的空间。因此，指定边框为零（0）将占用更少的空间。

**注意**

网址变化非常快。虽然本书付印时已尽力确保以下网址正确，但等到本书到达书店时，有些网址可能已经改变。如果你在使用某个网址时遇到问题，请从右向左逐段删除由斜杠分隔的片段，直到可以正常访问。微软的网站比任何其他网站变化都快，所以如果他们的某个网址无法使用，请不要惊讶。最好的解决方法是访问**www.microsoft.com/**，然后逐步导航。

以下是在线可用的资源列表：

- W3C的Dave Raggett撰写的"Getting Started with HTML"、"More Advanced Features"和"Adding a Touch of Style"提供了对HTML和CSS的基础理解，来自制定标准的组织。最后更新于2005年5月24日。"Getting Started"文档包含指向其他两篇的链接，可在**www.w3c.org/Markup/Guide/Overview.html**获取。
- **W3 Schools**是HTML、XHTML、CSS、JavaScript和PHP的主要资源。它免费提供了所有主题的教程、参考资料、示例和论坛。你可以访问**www.w3schools.com/**。
- **HTML Goodies**在**www.htmlgoodies.com/**提供了良好的HTML入门指南以及许多HTML、CSS、JavaScript和PHP的高级资源。
- **HTML Code Tutorial**在**www.htmltutorial.com/**提供教程、论坛和其他资源。
- James "Eric" Tilton撰写的"Composing Good HTML"（最后更新于1998年7月13日）。可在**www.ology.org/tilt/cgh/**获取。
- VisiBone提供的免费在线速查表"HTML Tags"，位于**html-tags.info**。
- Tim Berners-Lee（万维网的创始人）撰写的"Style Guide for Online Hypertext"。最后更新于1995年5月。可在**www.w3.org/Provider/Style/**获取。
- Alan Richmond（NASA GSFC）撰写的"A Basic HTML Style Guide"。最后更新于2001年7月11日。可在**heasarc.gsfc.nasa.gov/docs/heasarc/Style_Guide/styleguide.html**获取。

网上还有许多其他关于Web和HTML编写的优秀书籍，包括：

- *HTML and XHTML: The Complete Reference, Fourth Edition* by Thomas A. Powell (McGraw-Hill/Professional, 2003).
- *Web Design: The Complete Reference, Second Edition* by Thomas A. Powell (McGraw-Hill/Professional, 2002).
- *HTML, XHTML, and CSS QuickSteps, Second Edition* by Guy Hart-Davis (McGraw-Hill/Professional, 2009).

## 商业地产税收抵免

计算机科学研究论文

#### HTML和Web资源

W3C HTML验证服务是一个极其有用的工具。它确保你的标记符合当前的HTML标准。还有一个CSS验证器可用，它允许你输入URL甚至直接输入CSS代码；如果你在点击"submit"时遇到困难，尝试按住control键的同时按下enter键，这将提交表单，这是从文本框中学到的一个小窍门。这个文本框经常回答关于浏览器之间渲染差异的问题。此外，W3C常见问题页面虽然不是详尽的，但仍然是有用的HTML常见问题列表，它还描述了HTML版本之间的关系。

ROSS nived是一个很棒的资源，还有一些其他有价值的资源。如果你在网站上遇到HTML或CSS问题，它是一个很好的资源。它还包含许多指向其他资源的有用链接，包括关于电子邮件、如何发送电子邮件等的资源，还有许多维护不正确的信息等等。现在，这些中哪些在网上听起来有用...

对于某些HTML元素，另一个有趣且有选择性的HTML和CSS资源指南可用。该网站最后更新于5月14日。另一个非常有用的页面是页面，这是资源指南的最初草稿。这也可以在URL获得，以及HTML、XHTML、CSS、JavaScript和ASP的对象。它设计和功能涵盖所有主题，免费提供。你也可以在同一网站地址使用ITIL入门指南和许多其他Web资源，以及获取最新产品信息的其他资源。

# 第2章

## 使用CSS进行样式设计

## 关键技能与概念

- 附加CSS
- 理解CSS规则
- 选择要格式化的内容
- 应用CSS概念
- 使用文本属性
- 实现页面属性
- 使用CSS进行布局

使用XHTML可以构建网页的结构，但如果你遵循XHTML的严格定义，不使用任何已弃用的HTML标签，就无法让页面看起来很好，而且在不同浏览器中可能看起来不同。让页面在多种浏览器中始终保持良好的外观是CSS（层叠样式表）的工作。CSS是一组规则，用于指定网页的颜色、字体和布局。今天，它不仅是格式化网页的主要方式，也是最有效的方式。

在本章中，我们将了解CSS规则的结构、如何将样式表添加到网页、规则如何应用、更常见的规则有哪些，以及它们的使用示例。

> **注意**
> 为简化本章的讨论，以下几个术语使用其通用含义。其中包括：
> **页面**或"网页"是Web设计师放置要显示元素的原始区域或"画布"。
> **浏览器**是任何能够渲染页面以便阅读的软件。
> **屏幕**是任何能够显示页面的设备，包括手持设备和打印机。
```



 # 创建 CSS

CSS 就是嵌入在 XHTML 或 HTML（以下统称为 X/HTML）页面中的几行文本（规则），或者更常见的情况是放在单独的 CSS 文件中，在那里它可以应用于多个 X/HTML 页面。CSS 设计得非常紧凑，具有许多避免冗长的特性，如清单 2-1 所示。

```
清单 2-1  CSS 示例

body {
    background:yellow;
    color:red;
    font: 12pt Arial;
}
h1, h2 {
    color:blue;
    font: 24pt "Comic Sans MS";
}
```

在清单 2-1 所示的 CSS 中，应用此 CSS 的网页上的 X/HTML `<body>` 标签被分配了黄色背景、红色文本和 12 磅 Arial 字体。此外，`<h1>` 和 `<h2>` 标题标签都被分配了蓝色文本和 24 磅 Comic Sans 字体。这也展示了 CSS 的层叠特性：body 的属性被分配给页面上的各个元素，但 h1 和 h2 元素除外，它们有自己的属性分配。

### 附加 CSS

CSS 可以通过以下两种主要方式之一或同时附加到 X/HTML 页面或文件：

- 使用 `<style>` 标签**嵌入**到 X/HTML 文件中。
- 使用 `<link>` 标签**链接**为外部 CSS 文件。

清单 2-2 展示了如何使用 `<style>` 标签。注意 CSS 是嵌入在 `<style>` 标签中的。清单 2-3 展示了 `<link>` 标签。这两个标签都只出现在 X/HTML 文档的 `<head>` 部分，但如果有需要，可以有多个 `<link>` 标签。图 2-1 显示了这两种附加 CSS 的方法产生完全相同的效果（颜色方面需要您发挥一下想象力，但正如所述），而表 2-1 显示了这些标签及其属性。

## 38 动态 Web 编程：初学者指南

![图 2-1](img/1c438577fbcf9eaf55830d0e11ca0b3a_55_0.png)

**图 2-1**  链接和嵌入的样式表产生相同的效果，但链接的样式表可以用于多个页面。

#### 清单 2-2  带有 `<style>` 标签的 X/HTML 页面

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
<title>清单 2-2</title>
<style type="text/css">
```

```
body {
    background:yellow;
    color:red;
    font: 12pt Arial;
}
h1, h2 {
    color:blue;
    font: 24pt "Comic Sans MS";
}
```

```
</style>
</head>
<body>
    <h1>This heading should be<br />24-point Comic Sans, in blue.</h1>
    <p>
        This normal paragraph text should be 12-point Arial, in red.<br />
        The page background should be in yellow.
    </p>
</body>
</html>
```

| 标签或属性 | 说明 |
| --- | --- |
| `<style> </style>` | 允许在 X/HTML 文档中嵌入 CSS 规则。 |
| type | 指定样式表内容类型，通常为 text/css。必须提供此属性。 |
| media | 指定样式的预期媒介。默认值为 screen。 |
| `<link />` | 将外部 CSS 附加到 X/HTML 文档。 |
| rel | 指定 X/HTML 文档与样式表之间的关系。最常见的是 stylesheet，但也可以是 alternate，以指定带有名称的替代样式表。 |
| href | 指定样式表的 URL 或文件名。 |
| type | 指定样式表内容类型，通常为 text/css。必须提供此属性。 |
| media | 指定样式的预期媒介。默认值为 screen；另一种替代值为 printer。 |
| title | 指定替代样式表的名称。 |

表 2-1  Style 和 Link 标签

#### 清单 2-3  带有 `<link>` 标签的 X/HTML 页面

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
    <head>
    <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
        <title>清单 2-3</title>
        <link rel="stylesheet" type="text/css" href="listing 2-1.css" />
    </head>
    <body>
        <h1>This heading should be<br />24-point Comic Sans, in blue.</h1>
        <p>
            This normal paragraph text should be 12-point Arial, in red.<br />
            The page background should be in yellow.
        </p>
    </body>
</html>
```

## 提示

在较早的代码示例中，您可能会看到在 `<style>` 标签内放置 `<!-- -->` 注释标签来包围所有样式，以防止它们在旧浏览器中显示。虽然这种方法有效，但现在很少有人使用旧浏览器，而且这种使用注释标签的做法不符合 XHTML 规范。

### CSS 规则

最简单的 CSS 规则是一行包含三个组成部分的文本：选择器、属性和值。例如：

![CSS 规则图示](img/1c438577fbcf9eaf55830d0e11ca0b3a_57_0.png)

其中*选择器*是 **body**，*属性*是 background，*值*是 yellow。属性和值之间用冒号分隔，它们一起构成*声明*，并用花括号（`{}`）括起来。一个单独的选择器可以有多个属性/值对，如清单 2-1 所示，它们之间用分号分隔。如果只有一个属性/值对，或者对于最后一个属性/值对，分号不是必需的，但为了保持一致性和培养良好习惯，建议使用分号。

CSS 规则区分大小写，必须使用小写。您可以添加任意数量的空格、制表符和换行符，使 CSS 易于阅读。建议您将规则展开，以便轻松查看哪些规则正在影响网页的各个部分。

您可以通过添加注释来帮助自己记住在样式表中所做的操作，或向他人说明，这些注释可以在规则完成后的同一行添加，也可以在单独的一行添加。为此，将文本注释用 /* */ 括起来，如下所示：

```
body { background : yellow; } /* 将背景设置为黄色 */
```

#### 选择器的类型

CSS 规则中的选择器部分标识了将受该规则影响的网页元素。您可以有覆盖整个页面的选择器，例如 **body**，或单个类型的标签，例如 **h1**，如您在清单 2-1 和 2-2 中所见。您还可以有标识页面部分的选择器，或仅某些特定标签，例如某些 **h1**。因此，选择器可以是标签名称、由类修改的标签名称、ID、属性、事件或其上下文，或由标签标识的元素部分。

##### 类和 ID 选择器

您可以为大多数标签添加类名和/或 ID，以仅标识您希望受样式影响的那些标签，方法是将类或 ID 添加到选择器中。类通过在选择器的标签名称后添加句点（.）和类名来添加。ID 通过在选择器的标签名称后添加井号（#）和 ID 来添加。例如，清单 2-4 和图 2-2 展示了格式化特定类别的段落和具有 ID 的特定标题所需的选择器，而未如此标识的标题和段落则以不同方式格式化。

![图 2-2](img/1c438577fbcf9eaf55830d0e11ca0b3a_58_0.png)

**图 2-2**  ID 和 class 属性让您可以为特定元素设置样式。

**注意**

在清单 2-4 以及本章剩余的清单中，`<!DOCTYPE>` 和 `<meta>` 标签以及 `<html>` 属性已被省略，以保持简洁。

###### 清单 2-4  类和 ID 选择器

```
<html>
    <head>
        <title>清单 2-4</title>
        <style type="text/css">
            h1 {font : 24pt "Arial Black";  }
            p { font : 14pt "Times New Roman"; }
            h1.big { font : 36pt "Eras Bold ITC"; }
            p#special { font : 16pt "Gill Sans MT Condensed"; }
        </style>
    </head>
    <body>
        <h1>This is a normal heading.</h1>
        <p>This is a normal paragraph.</p><br />
        <h1 class="big">This is the "big" heading.</h1>
        <p id="special">This is the "special" paragraph.</p>
    </body>
</html>
```

## 提示

CSS 选择器可以仅为类或 ID，带有其标识符（`.` 或 `#`）且不带标签名称。例如，`.legal { font : 16pt "Franklin Gothic Book"; }` 将应用于所有带有 `legal` 类的标签。虽然您也可以对 ID 执行相同操作（`#note { font : 16pt "Franklin Gothic Book"; }`），但在 X/HTML 文档中，只有一个元素可以具有特定的 ID。

##### 其他选择器

最常用的选择器是标签名称，后面跟着带有类或 ID 的标签名称。但是，还有另外五种类型的选择器使用事件、属性、上下文、位置或组来标识要设置样式的内容：

- 事件考虑影响标签的交互事件，通常与 `<a>`（锚点）标签中的超链接一起使用。例如：
  
  `a:link { color : green; }`



如果链接未被访问过，则将其显示为绿色。共有五种可能的事件可以设置样式；所有这些事件都紧接在标签之后，前面有一个冒号（:）：

- **link**，用于未被单击过的超链接
- **visited**，用于已被单击过的超链接
- **active**，用于正在被单击过程中的元素
- **hover**，用于鼠标所指位置的元素
- **focus**，用于已选中但未被激活的元素，如使用 TAB 键选中的情况

- 标签的**属性**，属性用方括号（`[ ]`）括起来。例如：
`input[readonly]  { background : gray; }`
将为具有 `readonly` 属性的表单字段应用灰色背景。你还可以仅对那些具有特定属性值的标签设置样式。例如：
`table[border="2"]  { border-color : blue; }`
将仅把 `border="2"` 属性的表格边框设置为蓝色。此外，如果标签的属性值是多个值列表中的一项，可以这样设置样式：
`area[coords~="147"]  { background-color : yellow; }`
这将为坐标之一为 147 的 area 元素添加黄色背景。最后，如果标签的属性值是值列表中的第一个值，可以这样设置样式：
`area[coords|="60"]  { background-color : fuchsia; }`
这将为第一个坐标为 60 的 area 元素添加紫红色背景。

- 标签的**上下文**考虑的是标签相对于另一个标签的位置关系，有三种可能（见清单 2-5）：

+ **后代**选择器，要设置样式的标签称为*后代*标签，它位于另一个称为*祖先*标签的任何位置内部，包括嵌套在第三个标签内。作为选择器，后代标签跟在祖先标签之后，中间用空格分隔。例如：
`div em { font-family : "Comic Sans MS" }`
将使 `<div>` 内的任何 `<em>` 内容显示为 Comic Sans，如下所示：

> • This line is ***FUNNY!***
> • This line is ***FUNNIER!!***

###### 清单 2-5 上下文修饰选择器示例

```
<html>
    <head>
        <title>Listing 2-5</title>
        <style type="text/css">
            div em { font-family : "Comic Sans MS"; }
        </style>
    </head>
    <body>
        <div>
            <ul>
                <li>This line is <em>FUNNY!</em></li>
                <li>This line is <em>FUNNIER!!</em></li>
            </ul>
        </div>
    </body>
</html>
```

- **子元素**选择器，要设置样式的标签（称为*子*标签）直接包含在其*父*标签内。它不能在第三个标签内。作为选择器，子标签跟在父标签之后，中间用 >（大于号）分隔。例如：

  `ul > li { font-family : "Comic Sans MS" }`

  将使两个 `<li>` 的内容都显示为 Comic Sans，如下所示：

  - This line is *FUNNY!*
  - This line is *FUNNIER!!*

- **首个子元素**选择器，要设置样式的标签是一个子标签，并且紧跟在其*父*标签之后。作为选择器，`:first-child` 跟在父标签之后。例如：

  `ul :first-child { font-family : "Comic Sans MS" }`

  将使第一个 `<li>` 的内容显示为 Comic Sans，如下所示：

  - This line is *FUNNY!*
  - This line is FUNNIER!!

- **相邻兄弟**选择器，要设置样式的标签紧接在其*兄弟*标签之后，且两者处于同一层级。作为选择器，要设置样式的标签跟在兄弟标签之后，中间用加号（+）分隔。例如：

  `li + li { font-family : "Comic Sans MS" }`

将使第二个 `<li>` 的内容显示为 Comic Sans，如下所示：

- This line is *FUNNY!*
- This line is ***FUNNIER!!***

元素内的**位置**，可以设置元素的*首字母*或*首行*样式。例如：

```
p:first-letter { font : 18pt "Copperplate Gothic Bold" }
```

将使 `<p>` 标签内的首字母变为 18pt Copperplate Gothic Bold，如下所示，每个段落都在单独的 `<p> </p>` 标签中。

> Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.

Now we are engaged in a great civil war, testing whether that nation, or any nation so conceived and so dedicated, can long endure. We are met on a great battle-field of that war. We have come to dedicate a

具有相同声明的**标签组**可以列为共同的选择器，用逗号分隔。例如：

```
h1, h2, h3 { font-family : "Copperplate Gothic Bold" }
```

将设置前三个标题级别使用 Copperplate Gothic Bold 字体。

## 提示

你可以组合多种指定选择器的方法，以精细控制要设置样式的内容。例如：

```
p#first span { font : 18pt "Copperplate Gothic Bold" ; }
```

将使具有 first ID 的 `<p>` 标签的后代 `<span>` 标签中的文本变为 18pt Copperplate Gothic Bold。

#### CSS 属性和值

你可以在 CSS 规则中使用的属性和值多种多样，但大致可分为三组：文本属性、页面属性和布局属性，每组都将在本章后面的各自章节中讨论。要理解和恰当使用这些属性和值，首先需要对 CSS 所基于的基本概念有一个初步了解。

### CSS 概念

CSS 有七个基本概念：层叠和继承、页面布局的盒子模型和视觉模型、元素定位、度量单位、颜色的使用、文本和字体，以及表格和列表。文本和字体与文本属性一起讨论。盒子模型和视觉模型页面布局，以及定位和表格列表，与布局属性一起讨论。其余内容在此讨论。

#### 层叠和继承

在 CSS 中，每个属性都必须有一个值。该值可以是具体的、计算得出的或继承而来的。要得出最终使用的实际值，浏览器必须经过三组过程。第一个是*层叠*，它确定各种因素在影响最终属性值时的优先顺序。第二个是*继承*，它考虑为当前元素的父元素确定的值的影响。第三个过程是最终值的*计算*。

##### 层叠顺序

在层叠顺序中，值由在给定层次结构中被认为最重要的影响因素决定。对于 CSS，层叠优先顺序按升序排列（1 为最不重要，5 为最重要）：

1. 浏览器或查看软件的约定和设置。
2. 网页的用户或查看者所做的默认设置。
3. 导入或链接的样式表属性值。
4. 嵌入式样式表属性值。
5. 页面被查看时用户或查看者所做的设置。

换句话说，浏览器从自身设置开始，这些设置可能被用户更改，首先被外部样式表替换，然后被嵌入式样式表替换，最后由用户在查看程序中进行调整。

如果你希望某个特定样式覆盖层叠中原本会发生的情况，可以为该样式添加 `!important` 声明，它将会这样做。此类声明的示例是

```
h1 { font : 24pt "Arial Black" !important ; }
```

##### 继承

通过继承，元素的值可以由文档树中较早的元素的值来确定。例如，清单 2-6 展示了一个简单的网页及其文档树，如 Aptana 的大纲视图所示，如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_64_0.png)

**清单 2-6** 文档树示例

```
<html>
    <head>
        <title>Listing 2-6</title>
        <style type="text/css">
            div.main { font : 12pt "Bodoni MT"; }
            em { font : 14pt "Script MT Bold"; }
        </style>
    </head>
    <body>
        <div class="main">
            <h1>The main heading.</h1>
            <p>The first paragraph.</p>
            <p>The second, <em>yes, second</em> paragraph.</p>
        </div>
    </body>
</html>
```

在此文档树中，与大多数情况一样，`<body>` 是树的根，第一个子元素是 `<div class="main">`，它又有三个子元素 `<h1>`、`<p>` 和 `<p>`。第二个 `<p>` 有一个子元素 `<em>`。如果没有样式表，或者用户没有在其浏览器中更改设置，浏览器中的默认样式设置将基于层叠贯穿整个树。当引入一个为 `<div class="main">` 设置字体样式的样式表时，该样式将流向其子元素及其子元素的子元素，除非被另一个样式中断。这就是继承的基本原理。如下所示，为 `<div class="main">` 设置的字体出现在 `<h1>` 和两个 `<p>` 中，除了 `<em>` 标签内的文本，因为它有自己的样式。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_64_1.png)



继承适用于那些允许继承的属性，例如 `font`。在本章后面几节的列表中，你会看到标有"Inherited?"（是否可继承？）的列，其中显示了可以继承的属性。如果你希望某个通常不可继承的属性被继承，可以为该元素创建一个样式，并将其值设为 `inherit`。

#### 计量单位

CSS 中的水平和垂直测量值用于许多属性，包括 `border-width`、`font`、`line-height`、`margin` 和 `text-indent`。水平和垂直测量单位可以分为两种形式：相对于其他度量，以及绝对度量。

*相对*单位将当前元素缩放到元素的字号大小、元素的字体"x 高度"（小写字母 x 的大小），或相对于输出设备的分辨率。相对计量单位包括：

- `em`，将元素缩放到其字号大小。`1em` 与字体大小相同，或等于 100%。因此 `1.4em` 是字号的 140%，`.6em` 是字号大小的 60%。
- `ex`，将元素缩放到其"x 高度"，类似于 `em`，`1ex` 与"x 高度"大小相同，或等于当前字体字母"x"大小的 100%。默认情况下，`1ex` 被认为等同于 `.5em`。
- `px` 或像素，将元素缩放到显示分辨率。在 96dpi（每英寸点数）的电脑屏幕上，在约一臂远（约 28 英寸）的距离观看时，1px 约为 0.01 英寸或 0.26 毫米，略小于一个点（`pt`，见下一条列表），点为 0.01389 英寸。

# 注意

当 `em` 用于字体时，它相对于父元素的字号或其百分比。

绝对计量单位是以下任一单位中的特定测量值：

- `cm`，厘米，0.3937 英寸
- `in`，英寸，2.54 厘米
- `mm`，毫米，0.1 厘米，0.03937 英寸
- `pc`，派卡，1/6 英寸，12 点
- `pt`，点，1/72 英寸，1/12 派卡

**提示**

当你使用绝对单位时，应该非常确定显示设备的尺寸。随着手持设备越来越普及，使用相对单位变得更加重要。

代码清单 2-7 和图 2-3 展示了各种计量单位的应用示例。

##### 代码清单 2-7 计量单位

```
<html>
    <head>
        <title>Listing 2-7</title>
        <style type="text/css">
            body {
                margin : .5in ;
                font : 14px "Arial";
            }
            h1 {
                font : 2em "Arial Black"; /* twice the body font */
                line-height : 1.5em ; /* 150% of font or 36 points */
                margin : -.32cm ; /* outdented about a third of the margin */
            }
            p {
                margin : 25mm ; /* about twice the body margin */
                font : 1.1em; /* 110% of the body font*/
                border : .25ex dashed; /* 25% of the font's x-height */
            }
        </style>
    </head>
    <body>
        <h1>This is approximately a 20pt heading that is outdented.</h1>
        <p>
            This a paragraph with approximately 11pt type, indented and
            with a dashed border.
        </p>
    </body>
</html>
```

这是一个大约 20pt 的突出标题。

这是一个大约 11pt 的段落，带有缩进和虚线边框。

图 2-3 基于 Web 的文档使用相对计量单位会更好地缩放。

#### 颜色的使用

在 CSS 中，你可以使用 `background-color` 属性为页面背景添加颜色，或者为三种前景元素之一添加颜色：使用 `color` 属性为文本；使用 `border-color` 属性为边框；使用 `outline-color` 属性为轮廓。这些属性中的每一个的值都是一个特定的颜色标识符，此外对于 `border-` 和 `outline-color`，你还可以选择 `transparent`（透明）。

颜色标识符可以是颜色名称，也可以是使用 RGB（红、绿、蓝）颜色规范的数值表示。颜色名称可以是经典颜色名称之一：`aqua`、`black`、`blue`、`fuchsia`、`gray`、`green`、`lime`、`maroon`、`navy`、`olive`、`orange`、`purple`、`red`、`silver`、`teal`、`white` 或 `yellow`，也可以是大多数浏览器中实现的 140 多种扩展颜色名称之一，这些名称展示在 [www.w3.org/TR/css3-color/](http://www.w3.org/TR/css3-color/)。

RGB 颜色可以用四种方式指定（以下示例用于将段落文本设为青色）：

- 作为前面带 `#` 的六位十六进制（hex）数，例如：
  `p.cyan { color: #00ffff }`。
- 作为前面带 `#` 的三位十六进制数，例如：
  `p.cyan { color: #0ff }`。
  三位十六进制数仅在通常由两位表示的三种颜色各有两个相同字符时才有效。三位数字通过将每个原始数字翻倍扩展为六位。
- 作为三个百分比，用逗号分隔，括在括号中，前面加 `rgb`，其中十六进制 00 为 0%，十六进制 FF 为 100%，例如：
  `p.cyan { color: rgb(0%,100%,100%) }`。
- 作为三个十进制数，用逗号分隔，括在括号中，前面加 `rgb`，其中十六进制 00 为 0，十六进制 FF 为 255，例如：
  `p.cyan { color: rgb(0,255,255) }`。

用于表示红、绿或蓝颜色分量的两位十六进制数可以有 256 个值（范围从十进制的 0 到 255 或十六进制的 00 到 FF）。三种颜色或六个十六进制数字的组合，共允许超过 1600 万种颜色，相比之下命名颜色只有 140 种。颜色范围从十进制 `0,0,0` 或十六进制 `#000000` 的黑色（没有任何颜色）到十进制 `255,255,255` 或十六进制 `#ffffff` 的白色（所有颜色的总和）。红色是 `255,0,0` 或 `#ff0000`，酸橙绿（不是绿色）是 `0,255,0` 或 `#00ff00`，蓝色是 `0,0,255` 或 `#0000ff`。

**提示**

十进制和十六进制记数法之间转换的一种简便方法是使用科学模式的 Windows 计算器。从**开始 | 所有程序 | 附件 | 计算器**打开计算器，然后选择**查看 | 科学型**。单击 **Hex** 或 **Dec** 选项，输入十六进制或十进制数字，然后单击相反的选项（**Hex** 或 **Dec**）。

过去，Web 上关于颜色的任何讨论都集中在 Web 安全调色板——216 种能在几乎任何显示器上 correctly 显示的颜色。最早的浏览器只有 16 种命名颜色的原因之一是许多系统不支持超过 16 种颜色。如今，这种情况与 Web 相关的其他一切一样，已经大不相同。此时，坚持一个已被先进技术淘汰的标准几乎没有意义。这并不意味着命名颜色在适合应用时不应该使用，只是坚持这一标准的重要性已大大降低。

除了前面提到的 W3C 颜色图表外，互联网上还有许多可用的颜色图表。搜索"Internet Color Chart"（互联网颜色图表）。其中最好、也是我们的最爱之一，是 http://html-color-codes.com，由 VisiBone 的 Bob Stein 制作（www.visibone.com，该网站还有许多其他图表和指南，其中一些在本书中有所提及）。

#### 文本属性

CSS 提供了多种属性和值来方便文本的样式设置，如表 2-2 所示，并在本章的许多代码清单、图和插图中展示。文本样式有两个主要组成部分：字体和字体特征的应用，以及文本的对齐和间距。

#### 字体的应用

字体应用的关键在于浏览器向用户呈现网页设计师指定的字体，且字号、字重、变体和样式正确。大多数浏览器都有一种算法，可以在指定的字体及其属性不可用时选择替代字体。W3C 在 http://w3.org/TR/CSS21/fonts.html 提供了这种替代的模型。作为设计师，你可以做几件事来协助这一进程：选择常见字体、添加替代字体，以及添加通用字体。

例如，如果你想将 Garamond 指定为页面主要部分的字体族，可以使用以下规则：

```
div.main { font-family : "Garamond", "Palatino Linotype", "Times", serif }
```

字体按从左到右的优先级顺序列出，因此如果 Garamond 可用则优先使用，只有当所有三种命名字体都找不到时才会使用通用 serif 字体。



 52 动态网页编程：初学者指南

| 属性 | 允许值 | 继承？ |
|---|---|---|
| color | 文本颜色。详见本章前面的"颜色的使用"。 | 是 |
| font | 字体大小和字体系列的组合，但可包含 font-variant、-weight、-style 和 line-height，这些必须加斜杠（/）前缀。 | 是 |
| font-family | 一个或多个用引号括起来、以逗号分隔的字体名称，以及可选的通用字体类型（serif、sans-serif、cursive、fantasy 和 monospace）作为指定字体不可用时后备。 | 是 |
| font-size | 绝对值（xx-small、x-small、small、medium、large、x-large、xx-large）；特定数值及单位；相对大小（larger、smaller）；或百分比（120%）。 | 是 |
| font-style | normal、italic、oblique。 | 是 |
| font-variant | normal、small-caps。 | 是 |
| font-weight | normal、bold、b、bolder、lighter、100-900。 | 是 |
| letter-spacing | normal 或指定字母间距增加值及单位。 | 是 |
| line-height | normal 或指定高度及单位；乘以字体大小的数值；或乘以字体大小的百分比。 | 是 |
| text-align | left、right、center、justify。 | 是 |
| text-decoration | none、underline、overline、line-through、blink。 | 否 |
| text-indent | 指定首行文本缩进量及单位。 | 是 |
| text-transform | capitalize、uppercase、lowercase、none。 | 是 |
| vertical-align | 相对于包含该文本的行进行文本对齐：baseline、sub（下标）、super（上标）、top、text-top、middle、bottom、text-bottom、正或负百分比，或相对于基线的特定量。默认值为 baseline。 | 否 |
| white-space | normal（折叠空白并允许所有换行）、pre（防止折叠空白并允许部分换行）、nowrap（折叠空白并忽略换行）、pre-wrap（防止折叠空白并允许所有换行）、pre-line（折叠空白并允许部分换行）。 | 是 |
| word-spacing | normal 或指定词间距增加值及单位。 | 是 |

**表 2-2** 文本属性

---

## 注意

如果字体名称不包含空格或特殊字符，则无需加引号。不过，将所有字体名称都加上引号是个好习惯。

使用各种字体属性时需牢记以下要点：

- `font-style` 的值为 `italic` 时会同时选择斜体和倾斜字体名称，而值为 `oblique` 时仅选择倾斜字体名称。
- `font-weight` 的数字值（如 200 和 600）是名称，你*不能*在它们之间插值，例如使用 "250"。值 400 等同于 `normal`，700 等同于 `bold`。名称中包含 "light" 的字体为 300，"book"、"regular" 和 "roman" 均为 normal 或 400，"medium" 或 "demi" 为 500，"heavy" 为 800，"black" 为 900。
- `font` 属性允许你将其他五种字体属性的值与 `line-height` 合并为一个属性，如清单 2-8 所示，第一条规则中列出的各个属性在最后合并为一个。在 `font` 属性中，必须包含字体大小和字体系列，且大小必须位于系列之前。你可以包含零到三个其他字体属性，它们之间的顺序不限，但必须全部位于字体大小之前。行高必须位于大小和系列之间，组合时必须加斜杠前缀。

**清单 2-8** 相同的规则

```
p {
  font-style : italic;
  font-variant : small-caps;
  font-weight : 800; /* 比 "bold" 粗 25% */
  font-size : 16px;
  line-height : 1.5em;
  font-family : "Garamond", "Palatino Linotype", "Times", serif;
}
p { font : italic small-caps 800 16px /1.5em "Garamond"; }
```

#### 文本对齐

文本对齐属性相当直观易懂，但有几个不那么明显的特性需要注意：

- text-indent 属性仅适用于文本块的第一行，可以为负值以将文本行向左移动，如下所示以及清单 2-9 所示，但如果没有边距来容纳外凸的文本，它将被截断。

> 八十七年前，我们的先辈们在这个大陆上建立了一个新国家，它孕育于自由之中，奉行一切人生来平等的原则。

**清单 2-9** 使用 text-indent

```
<html>
    <head>
        <title>Listing 2-9</title>
        <style>
            p#first {
                margin : .5in ;
                text-indent : -.25in ;
            }
            p#first span { font : 18pt "Copperplate Gothic Bold" ; }
        </style>
    </head>
    <body>
        <p id="first">
            <span>Four score and seven years ago</span> our fathers brought
forth on this continent, a new nation, conceived in Liberty, and dedicated
to the proposition that all men are created equal.
        </p>
    </body>
</html>
```

- text-align : justify 使用的算法因浏览器而异，因此可能产生不同结果，并可能与包含词间距和字母间距的规则冲突。
- text-decoration 属性应用于元素内的文本，包括字符、单词和句子之间的空白，使用与元素指定的文本颜色相同。
- text-decoration 属性的 blink 值是可选值，在 IE 6、IE 7 和 IE 8 中无效，在 Firefox 3.0 和 3.5 中有效。
- `letter-spacing` 和 `word-spacing` 属性值是字符、单词和句子之间正常间距的附加值。当使用这些属性更改间距时，`text-align : justify` 值无法进一步调整间距以实现文本行的两端对齐。
- `vertical-align` 属性将文本相对于其所在文本行（称为*行框*）进行对齐。它*不*对段落或其他包含块进行垂直对齐。
- `white-space` 属性决定浏览器如何处理文本行首行尾的空格。空格、制表符和回车都被视为"空白"，使用 `normal`、`nowrap` 和 `pre-line` 值时会被清除，但使用 `pre` 和 `pre-wrap` 值时不会。

**注意**

在适用的情况下，除非另有规定，大多数属性默认值为适当的 `auto`、`normal`、`medium` 或 `none`。

#### 页面属性

页面属性如表 2-3 所示，与 `<body>` 标签一起使用时应用于整个页面，但也可以使用 `<div>`、`<h1...`、`<p>`、`<table>` 以及定义页面上空间的其他元素应用于页面的特定部分。

| 属性 | 允许值 | 继承？ |
|---|---|---|
| `background` | `background-attachment`、`background-color`、`background-image`、`background-position`、`background-repeat` 的任意组合。 | 否 |
| `background-attachment` | 相对于浏览器的 `scroll` 或 `fixed`，默认值为 `scroll`。 | 否 |
| `background-color` | 颜色（详见本章前面的"颜色的使用"）或 `transparent`，默认值为 `transparent`。 | 否 |
| `background-image` | 图像文件名或 URL，或 `none`。 | 否 |
| `background-position` | 水平百分比或绝对距离、`left`、`center` 或 `right`，和/或垂直百分比或绝对距离、`top`、`center` 或 `bottom`。默认值为 0%、0%，即左上角。 | 否 |
| `background-repeat` | `repeat`（水平和垂直）、`no-repeat`、`repeat-x`（水平）或 `repeat-y`（垂直），默认值为 `repeat`。 | 否 |
| `border`；`border-top`、`-right`、`-left`、`-bottom` | `border-width`、`border-style` 和 `border-top-color` 的任意组合。 | 否 |

**表 2-3** 页面属性*（续）*



 | 属性 | 允许值 | 继承？ |
| --- | --- | --- |
| border-color; border-top-color -right-, -left-, -bottom- | 特定颜色（参见本章前面的"色彩的使用"）或 transparent，默认值为 transparent。 | 否 |
| border-style; border-top-style -right-, -left-, -bottom- | 最多四个值（每边一个），包括 dashed、dotted、double、groove、hidden、inset、outset、ridge 和 none。默认值为 none。 | 否 |
| border-width; border-top-width, -right-, -left-, -bottom- | 最多四个值（每边一个），包括 thin、medium、thick 或特定单位的数值。默认值为 medium。 | 否 |
| cursor | 光标类型：auto、crosshair、default、pointer、move（四向箭头）、text（I 形光标）、wait（沙漏）、progress（旋转沙滩球）；或移动光标的一边，其中边由 n-resize（北边）、ne-resize（东北边）、e-resize、se-resize、s-resize、sw-resize、w-resize 和 nw-resize 指定；或用作光标的图像文件名。 | 是 |
| orphans | 页面底部必须保留的最小行数。默认值为 2。 | 是 |
| outline | outline-color、outline-style 和 outline-width 的任意组合。 | 否 |
| outline-color | 特定颜色（参见本章前面的"色彩的使用"）或 invert（元素颜色的反色），默认值为 invert。 | 否 |
| outline-style | 最多四个值（每边一个），包括 dashed、dotted、double、groove、inset、outset、ridge 和 none。 | 否 |
| outline-width | 最多四个值（每边一个），包括 thin、medium、thick 或特定单位的数值。 | 否 |
| overflow | visible（内容溢出盒子）、hidden（内容在盒子边缘裁剪）、scroll（添加滚动条以查看内容）、auto（通常与 scroll 相同）。 | 否 |
| page-break-after page-break-before | auto（既不强制也不禁止分页）、always（在盒子前/后强制分页）、avoid（禁止在盒子前/后分页）、left（强制一个或两个分页以使页面成为左手偶数页）、right（强制一个或两个分页以使页面成为右手奇数页）。 | 否 |
| page-break-inside | auto（既不强制也不禁止分页）、avoid（禁止在盒子前/后分页）。 | 是 |
| widows | 页面顶部必须保留的最小行数。默认值为 2。 | 是 |

表 2-3 页面属性（续）

## 注意

虽然可以将许多页面属性应用于 `<html>` 标签，但其效果几乎总是与应用于 `<body>` 标签相同。

使用页面属性时需要注意以下事项（参见清单 2-10 和图 2-4 了解背景和边框属性的应用示例）：

- background 属性可以是颜色、图像或两者兼有。如果两者都有，在图像生成之前会显示颜色。颜色也会透过图像的任何透明区域显示出来。背景覆盖其应用元素的内容、内边距和边框。

- 背景、颜色或图像位于屏幕上元素堆叠的"底部"（离观看者最远），可能被其他元素覆盖。这可以通过本章后面"布局属性"中讨论的 `z-index` 属性来控制。

- 如果将 background 属性与例如 `<p>` 标签一起使用，你需要在 `<p>` 周围添加一些内边距，以便背景稍微延伸到文本之外。

- 如果使用图像作为背景，通常希望使用小图像以便快速下载。要让图像覆盖整个元素，可能需要重复显示，这是 `background-repeat` 属性的默认值，因此无需额外声明。

- 如果希望单个图像在页面上水平和垂直居中，需要使用 `no-repeat` 值，但只需要一个 `center` 值。

- 使用 border 属性生成的边框放置在元素内容加上任何添加的内边距的外侧，但在外边距的内侧。参见本章后面"布局属性"中的"页面布局的盒模型和视觉模型"。

- 与 background 属性类似，如果添加边框，你需要在 `<p>` 和其他内容区域周围添加一些内边距，以使边框稍微位于文本之外。

- 对于 `border-style` 和 `border-width` 属性，如果有一个值，则应用于所有边；如果有两个值，第一个指上下边，第二个指左右边；如果有三个值，第一个是上边，第二个是左右边，第三个是底边；如果有四个值，顺序为上、右、下、左。

outline 属性在对象上方绘制线条，而不是像边框那样在外侧，因此线条不占用空间。它们采用对象的形状，可能是非矩形的，例如按钮。outline 在所有边上都是相同的。

orphan 和 widow 属性仅在第一页没有足够的空间容纳文本块时才被考虑。此外，如果没有足够的文本来同时满足 orphan 和 widow 属性，并且第一页没有足够的空间容纳整个文本块，那么整个文本块将被移到第二页。

三个分页属性控制分页是否可以在元素块（如段落、图像或表格）之前、之后或内部发生。默认情况是允许但不强制所有三个分页。如果允许分页，那么 widow 和 orphan 属性控制如何进行分页。

![图 2-4 如果使用背景图像，请确保文本在其上可读。](img/1c438577fbcf9eaf55830d0e11ca0b3a_75_0.png)

##### 清单 2-10 页面属性

```html
<html>
    <head>
        <title>Listing 2-10</title>
        <style type="text/css">
            body {
                background : #dcdcdc url(alincoln-transparent.jpg)
                no-repeat center;
            }
            h1, h2 {font-family : "Copperplate Gothic Bold"; }
            h1 { font-size : 24pt; }
            h2 { font-size : 20pt; }
            p {
                font : 14pt "Bodoni MT";
                padding : .5em;
            }
            p:first-letter  { font : 18pt "Copperplate Gothic Bold" ; }
            p#one { border : thin double blue}
            p#two { border : .1em dashed red}
        </style>
    </head>
    <body>
        <h1>Abraham Lincoln</h1>
        <h2>Gettysburg Address</h2>
        <p id="one">
            Four score and seven years ago our fathers brought forth on ...
        </p>
        <p id="two">
            Now we are engaged in a great civil war, testing whether that ...
        </p>
    </body>
</html>
```

#### 布局属性

虽然 CSS 通常被认为用于格式化和样式化网页，但它在页面布局方面同样有用。借助 CSS 的布局属性（见表 2-4），你可以通过多种不同方式在页面上定位元素：你可以确定元素如何相互交互、它们之间的间距、列表和表格的形成方式，以及页面的特征和行为。正如本章前面提到的，几个基本概念对于布局属性很重要，包括盒模型和视觉模型、定位以及表格和列表。

| 属性 | 允许值 | 继承？ |
| --- | --- | --- |
| border-collapse | 表格的 collapse 或 separate，默认值为 separate。 | 是 |
| border-spacing | 表格和单元格边框之间的一个或两个绝对距离。一个值同时指定水平和垂直距离。两个值时，第一个是水平距离，第二个是垂直距离。默认值为 0。 | 是 |
| bottom, left, top, right | 以特定单位表示的元素边与其包含块分离的距离、包含块高度（bottom 或 top）或宽度（left 或 right）的百分比，或 auto。 | 否 |
| caption-side | top（将标题定位在表格上方）、bottom，默认值为 top。 |  |
| clear | 当前盒子的上边框放置在另一个浮动盒子的 both、left 或 right 边框下方，或 none。 | 否 |
| clip | auto（元素不被裁剪），或 rect (top, right, bottom, left)，其中 top、right、bottom 和 left 是以特定单位表示的距离，用逗号分隔，表示绝对定位元素的边从其左上角裁剪或偏移的距离（可为负值）。 | 否 |
| display | block（将元素显示为独立块）、inline（将元素显示在另一个元素的块内）、inline-block（将元素显示为另一个元素块内的独立块）、list-item（将一组元素显示为父块及其内联子元素）、run-in（将元素显示为与另一个独立块相邻的独立块）、table、inline-table、table-element（将元素显示为表格或表格元素，独立或内联）、none（使元素及其后代对布局无影响）。 | 否 |
| float | 将块盒子定位在其他元素的左侧或右侧，最接近包含盒子的左侧或右侧，或 none。 | 否 |
| height, width | 以特定单位表示的元素高度或宽度、包含块高度或宽度的百分比，或 auto。不包括内边距、边框和外边距。 | 否 |
| list-style | 按顺序设置 list-style-type、list-style-position 和/或 list-style-image 的任意属性。 | 是 |
| list-style-image | 用作列表项标记的图像文件名，或 none。替换 list-style-type 标记。 | 是 |
| list-style-position | 将列表项标记定位在列表项框内部或外部（如悬挂缩进），默认值为 outside。 | 是 |

##### 表 2-4 布局属性



 | 属性 | 允许值 | 继承性 |
|----------|---------------|-----------|
| list-style-type | 将列表项标记指定为 disc、circle、square、decimal、decimal-leading-zero、lower-roman、upper-roman、lower-alpha、upper-alpha、lower-greek 或 none。 | 是 |
| margin; margin-top, -right, -left, -bottom | 元素边距与其包含块之间的特定距离，可使用任意测量单位；包含块高度的百分比（bottom 或 top）或宽度的百分比（left 或 right）；或 auto。默认值为 0。如果只有一个值，则应用于所有边。如果有两个值，第一个指上下，第二个指左右。如果有三个值，第一个是上边，第二个是左右两侧，第三个是下边。如果有四个值，顺序为上、右、下、左。 | 否 |
| max-height max-width min-height min-width | 元素高度或宽度的特定最小或最大长度，可使用任意测量单位；包含块高度或宽度的百分比；或 none。 | 否 |
| padding; padding-top, -right, -left, -bottom | 元素边与其包含块之间的特定距离，可使用任意测量单位；包含块高度的百分比（bottom 或 top）或宽度的百分比（left 或 right）；或 auto。默认值为 0。如果只有一个值，则应用于所有边。如果有两个值，第一个指上下，第二个指左右。如果有三个值，第一个是上边，第二个是左右两侧，第三个是下边。如果有四个值，顺序为上、右、下、左。 | 否 |
| position | absolute（元素从正常文档流中移除，根据 top、right、bottom、left 属性相对于包含块的左上角进行定位和大小调整）、fixed（元素按 absolute 值定位，但在页面滚动时固定在该位置）、relative（元素的位置相对于其正常位置进行偏移，正常位置由正常文档流决定，使用 top、right、bottom、left 属性）和 static（正常的元素，以正常文档流方式呈现，为默认值）。 | 否 |
| table-layout | fixed（使用指定的表格、列、单元格和边框宽度）或 auto（反映表格中的数据，不需要特定宽度）。 | 否 |
| visibility | visible（元素可见）、hidden（元素不可见，但影响布局）、collapse（在表格中，折叠行和/或列；其他情况下与 hidden 相同）。 | 是 |
| z-index | 一个整数，表示从屏幕视角的堆叠层级，用户看到的是"最上层"，即最高的堆叠层级；或 auto。 | 否 |

##### 表 2-4 布局属性（续）

#### 页面布局的盒模型与视觉模型

从最简单的意义上讲，网页是一系列盒子套着盒子，旁边有其他盒子，上方和下方还有更多盒子。网页布局的过程可以被认为是将盒子调整大小并排列，使它们都按你想要的顺序排列，就像这样：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_79_0.png)

网页上的元素属于以下两类之一：

- **块级元素** 占据屏幕上特定的、独立的区域，并生成一个包含其后代元素的包含块。这称为*块级盒子*，或简称为"块盒子"。块级元素包括 `<body>`、`<div>`、`<h1...>` 和 `<p>`。

**内联级元素** 不占据屏幕上的独立区域，默认情况下也不形成独立的块。内联级元素位于块级元素创建的块内部（与之内联）。内联级元素包括 `<em>`、`<cite>` 和 `<kbd>`。为了布局的目的，内联级元素可以被认为是包含在一个"内联盒子"中。

`display` 属性可以使块级元素变为内联级，也可以使内联级元素变为块级。

块级元素不仅有一个不可见的盒子包含它们，而且该盒子还可能被最多三个额外的与元素关联的盒子所包含：

- **内边距（Padding）**，内容区域与边框之间的区域。
- **边框（Border）**，通常可见的围绕内边距的线条或装饰。
- **外边距（Margin）**，边框与其包含块（如页面或父块）之间的区域。

块级元素的总大小是内容、内边距、边框和外边距的总和，如下图所示。如果内边距、边框和外边距都为 0（默认值），则内容直接紧挨着其包含块。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_80_0.png)

当网页在屏幕或其他设备上渲染时，它按特定顺序流动，后面的元素既可以影响也可以被前面的元素影响。当每个元素进入时，它会生成零个、一个或多个盒子。这些盒子在屏幕上的显示方式以及对其他盒子的影响称为*视觉格式化模型*，或简称为"视觉模型"。视觉模型的组成部分影响最终页面在屏幕上的呈现效果，包括：

- **视口（Viewpoint）**，用户看到的区域；我们称之为*屏幕*。它可能比设计者的页面或画布大或小，浏览器和设计者都需要考虑这一点。

**包含块** 是由层级更高的元素创建的块，可以是父元素或祖先元素，它包含当前元素，而当前元素本身又可能作为其子代后代的包含块。例如，如下图所示，`<body>` 元素包含一个 `<div>` 元素，`<div>` 元素又包含 `<h1>` 和 `<p>` 元素。`<body>` 元素的包含块以子元素或后代元素的形式容纳其他三个元素。`<h1>` 和 `<p>` 元素同时位于 `<div>` 和 `<body>` 元素的包含块中，这两个元素分别是它们的父元素和祖先元素。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_81_0.png)

**盒子生成** 发生在元素流入页面时。根据元素的类型和 display 属性，元素生成一个*块盒子*（显示在页面的独立区域中）或一个*内联盒子*（显示在另一个元素的块盒子内部）。在下面的示例中，`<p>` 标签生成一个块盒子，其中包含 `<span>` 内联盒子。

```
<p> <span>Four score and seven years ago</span> our fathers brought...</p>
```

**插入盒子（Run-in box）**，使用 `display` 属性的 `run-in` 值创建，允许块级元素与同级（同一层级）的块级元素共享同一个块。例如，一个标题可以流入后面的段落，如清单 2-11 所示，结果如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_81_1.png)

```
Listing 2-11  Run-in example

<html>
    <head>
        <title>Listing 2-11</title>
        <style type="text/css">
            h4 { display : run-in; }
        </style>
    </head>
    <body>
        <h4>The first heading.</h4>
        <p>The first paragraph into which the first heading is run-in.</p>
        <h4>The second heading.</h4>
        <p>The second paragraph into which the second heading is run-in.</p>
    </body>
</html>
```

**注意**
清单 2-11 仅在 IE 8（随 Windows 7 附带）中产生如上所示的期望结果。在 IE 7、Firefox 3.0 和 3.5 中，`run-in` 值不起作用，产生的结果如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_82_0.png)

#### 定位

定位决定了元素盒子在流入页面时如何相对于彼此调整大小和对齐。定位使用五种方法之一来完成，这些方法由 `position`、`top`、`right`、`bottom`、`left`、`float`、`clear` 和 `z-index` 属性决定。五种定位方法如下：

- **正常文档流** 是元素及其盒子流入页面的默认流程，所有定位属性都设置为其默认值或初始值；特别是 `position` 设置为 `static`，这会抵消其他定位属性。



 - **相对定位**（relative positioning）以正常流为起点，然后通过 `top`、`right`、`bottom` 和 `left` 属性的值，将元素的盒子相对于其"正常"位置进行偏移。跟随在相对定位盒子后面的盒子，其定位方式就像该盒子处于正常定位状态一样。
- **浮动定位**（float positioning）同样以正常流为起点，然后将元素的盒子向左或向右偏移，最多偏移到包含盒允许的极限位置。
- **绝对定位**（absolute positioning）通过 `top`、`right`、`bottom` 和 `left` 属性的值，确定元素相对于包含块边缘的位置，并可能确定其大小。绝对定位的元素不会影响其他元素的布局，其外边距也不会与其他外边距折叠。
- **固定定位**（fixed positioning）与绝对定位相同，此外，当页面滚动时，该元素会保持在屏幕上的固定位置（其原始位置）。

**正常流**（Normal Flow）在正常流中，块级盒子从页面顶部开始依次流向页面，垂直方向上一个接一个地排列，间距由它们的外边距决定。块级盒子的左边缘紧靠包含块的左边缘。内联盒子从左上角开始流向页面，在包含块中水平向右排列，到达右边缘后向下移动，开始另一组水平排列的盒子。这样一组横跨包含块宽度的内联盒子称为*行盒*（line box）。一组内联盒子可以在行盒内使用 `vertical-align` 属性进行水平对齐，使用 `text-align` 属性进行垂直对齐。

**浮动定位** 浮动定位允许你将块级盒子从其正常流的垂直位置中抽取出来，并将其附加到包含块的左侧或右侧。一旦附加后，浮动块会允许其他块位于其未附加的一侧。这是实现多列布局的主要且推荐的方式。尽管如此，这并不总是最简单的方法。本章后面讨论的表格，如果你的唯一受众是 1024×786 像素的电脑屏幕，那么表格可以确保信息在页面上的确定位置。浮动块的优点在于它具有灵活性，可以在许多不同的显示设备上呈现良好的效果，*前提*是你能确保所有部分都按照你的意愿"浮动"到正确的位置。

在代码清单 2-12 中，你可以看到用于创建常见的三列页面（带有页眉和页脚块）的 CSS 和相关 XHTML，如图 2-5 所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_84_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_84_1.png)

**图 2-5** 多列布局最灵活的方式是使用浮动块来实现。

##### 代码清单 2-12 浮动列——CSS

```
body {
    width : 600px;
    margin : 0;
    padding : 0;
}
div, h1, h2, p {
    margin : 0;
    padding : 0;
}
h2 {font : 600 24px "Futura" ; }
p  {font : 16px "Arial", "Helvetica", sans-serif ; }
div#header {
    top : 0px;
    left : 0px;
    height : 80px;
    margin : 5px;
    border : thin solid;
    padding : 5px;
}
h1#title {
    font : italic small-caps 600 36px /1.5em "Futura" ;
    text-align : center;
}
div#left {
    float : left;
    width : 15%;
    margin : 5px;
    border : thin solid;
    padding : 5px;
}
div#main {
    position : relative ;
    float : left;
    width : 58%;
    margin : 5px;
    border : thin solid;
    padding : 5px;
}
```

```
div#right
{
	position : relative ;
	float : right;
	width : 15%;
	margin : 5px;
	border : thin solid;
	padding : 5px;
}
```

```
div#footer
{
	clear: both ;
	margin : 5px;
	border : thin solid;
	padding : 5px;
}
```

##### 浮动列——HTML

```
<html>
	<head>
		<title>Listing 2-12</title>
		<link rel="stylesheet" type="text/css" href="Listing 2-12.css" />
	</head>
	<body>
		<div id="header">
			<h1 id="title">Page Header</h1>
		</div>
	广汽传祺
		<div id="left">
			<h2> Left Column </h2>
			<p> This can be used for navigation.</p>
		</div>
		<div id="main">
			<h2> Center Column </h2>
			<p> This can be used for the body.</p>
		</div>
		<div id="right">
			<h2> Right Column </h2>
			<p> This can be used for advertising.</p>
		</div>
		<div id="footer">
			<h2> Page Footer </h2>
			<p> This can be used for contact information.</p>
		</div>
	</body>
</html>
```

在代码清单 2-12 的 CSS 部分中，很多内容都是显而易见的，但有几个地方需要注意：

- 左列向左浮动、右列向右浮动是合理的，但你可能猜不到*中间列也需要向左浮动*。如果不这样做，右列就不知道它可以紧挨在中间列旁边，而中间列会向左偏移，就像这样：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_87_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_87_1.png)

> **注意**
此代码沦为 IE 6 "浮动 bug" 的受害者，该 bug 会使开始一行的 `float: left` 块的左边距加倍。这会使其他所有元素向右偏移，因此右盒在 IE 6 中仍然会被推下去。可以通过向 `div#left` 添加 `display: inline` 样式来修复此问题。更多信息，请参见 www.positioniseverything.net/explorer/doubled-margin.html。

如果你给两个外侧列各分配 15% 的空间，你应该可以给中间列分配 70% 并使其全部容纳。但如果你这样做，你会发现它并不合适，如下所示。正如你在清单中看到的，中间列必须减少到 58% 才能容纳。原因是 `height` 和 `width` 属性设置的是*内容高度或宽度，不包括内边距、边框和外边距*，这些必须添加到高度或宽度值中。通过查看绝对数值而非百分比，你可以最好地理解这一点（尽管使用百分比是首选，因为它们更灵活）。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_88_0.png)

- body 宽度 = 600 像素。
- 左列和右列，两者均为：外边距 = 5 像素 × 2，边框 = 2 像素（在 IE 7、Firefox 中为 1 像素）× 2，内边距 = 5 像素 × 2，每列额外增加 24 像素，加上 90 像素的内容宽度，总计 114 像素。
- 中间列也有 24 像素的外边距、边框和内边距。
- 如果从 600 像素的 body 宽度中减去两列以及中间额外的 24 像素，中间列的内容剩余 348 像素，即 58%。

你会注意到，在代码清单 2-12 的 CSS 部分顶部，我们将所有基本元素的内边距和外边距归零。原因是所有浏览器都会为这些元素设置默认值（并且不同浏览器的应用方式不同）。当你设置自己的值时，它会与浏览器设置的值相加，使元素看起来与你想要的效果不同。下图展示了未对基本元素进行归零时，三列浮动示例的外观。将此图与图 2-5 进行比较，后者包含了对元素的归零处理：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_89_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_89_1.png)

> 注意
IE 8 在未对基本元素进行归零的情况下显示三列浮动示例时，与 Firefox 3.0.5 显示方式相同，而不是 IE 7 的方式。

#### 表格和列表

表格和列表是用于处理表格化信息的强大 X/HTML 元素集合。表格也可以用于网页布局，但这是不推荐的，因为它提供的灵活性有限，而且难以维护。表格将网页的某个区域或整个页面划分为行和列，在两者相交处创建*单元格*。*列表*是一组缩进的条目，可以自动编号，或者在每行开头带有一个小图像，称为*项目符号*。如第 1 章所示，有一组广泛的 X/HTML 标签用于制作表格和列表，但同样也有大量的 CSS 属性和值可以应用于表格和列表的格式设置与布局。

> 注意
`display` 属性中的表格值（`table`、`table-row`、`table-row-group`、`table-column`、`table-column-group`、`table-cell`、`table-caption`、`table-header-group`、`table-footer-group`）用于创建表格元素，是针对 X/HTML 之外的语言（如 XML）设计的，这些语言没有定义表格元素。在 X/HTML 中，此功能由表格标签执行，并且这些 display 属性应用于 X/HTML 表格元素时会被忽略。

**表格布局与格式设置** 表格的格式设置是应用于各种表格元素的总和，基于一个可被视为一组层次的分层结构。为了使格式设置（例如边框或背景）对查看者可见，它必须应用于顶层，或者其上方的层必须是透明的（这是默认值）。从顶层（最接近查看者）到底层的层次依次为：

1. 单元格（`<td>` 或 `<th>`）
2. 行（`<tr>`）
3. 行组（`<tbody>`）
4. 列（`<col>`）
5. 列组（`<colgroup>`）
6. 表格（`<table>`）



 ## 提示

你可以在 Firefox 中看到显示网页时所使用的所有默认样式，因为它使用 CSS 文件来完成这项工作。在 Windows 计算机上，你可以在 c:\program files\mozilla firefox\res\html.css 路径找到这个 CSS 文件。

清单 2-13 是一个对其应用了多种样式的简单表格。看看样式应用如何影响表格：

1.  从仅包含表格且没有任何样式或格式开始，只保留各元素的默认样式，你会得到如下所示的表格。注意表头行如何是**粗体**且居中对齐，而表体行则是正常粗细且左对齐。此外，没有任何边框。
2.  给 `<table>` 标签添加背景、宽度和边框属性，你会得到如下所示的表格。（在 IE 6 到 IE 8 中，边框比 Firefox 中更浅。）
3.  给 `<thead>` 标签添加背景。这个背景会覆盖表格背景，除了单元格边框所在的位置。

| 零件名称 | 年度成本 | 维修工时 |
| :--- | :--- | :--- |
| Gauge | $425 | 12 |
| Switch | $158 | 8 |
| Control | $218 | 10 |

| 零件名称 | 年度成本 | 维修工时 |
| :--- | :--- | :--- |
| Gauge | $425 | 12 |
| Switch | $158 | 8 |
| Control | $218 | 10 |

| 零件名称 | 年度成本 | 维修工时 |
| :--- | :--- | :--- |
| Gauge | $425 | 12 |
| Switch | $158 | 8 |
| Control | $218 | 10 |

4.  添加 `<table>` 标签属性 cellspacing="0" 来消除单元格之间的间隙。同时，给 `<colgroup id="part">` 设置与表头相同的背景，并给单元格类 `<td class="name">` 设置 font-weight : bold。

| 零件名称 | 年度成本 | 维修工时 |
| :--- | :--- | :--- |
| Gauge | $425 | 12 |
| Switch | $158 | 8 |
| Control | $218 | 10 |

5.  最后，美化标题的格式，在其下方添加一些内边距，在表头下方添加底部边框，将数字右对齐并在右侧添加一些内边距使其不会紧贴单元格右边缘，同时将零件名称也右对齐，同样在右侧添加一些内边距。结果如下所示——与未格式化的表格相比，变化相当明显。

| 零件名称 | 年度成本 | 维修工时 |
| :--- | :--- | :--- |
| Gauge | $425 | 12 |
| Switch | $158 | 8 |
| Control | $218 | 10 |

## **注意**

表格分组元素（如 `<thead>` 和 `<colgroup>`）对其可使用的样式属性有限制。例如，如果将底部边框添加到 `<thead>`，它不会显示；而字体加粗对 `<colgroup>` 不起作用。

## **清单 2-13** 表格示例

```
<html>
  <head>
    <title>Listing 2-13</title>
    <style type="text/css">
      table {
        background : #dcdcdc;
        border : thin solid;
        width : 240px;
      }
      thead, #part { background : #fffacd; }
      .name {
          font-weight : bold;
          text-align : right;
          padding-right : 12px;
      }
      caption {
          font : bold 14px "arial";
          padding-bottom : 5px;
      }
      .line { border-bottom : medium solid #00008b }
      .data {
          text-align : right;
          padding-right : 12px;
      }
    </style>
  </head>
  <body>
    <table cellspacing="0">
      <caption>UR 771 Part Cost</caption>
      <colgroup id="part" />
      <colgroup span="2" id="costs" />
      <thead>
        <tr>
          <th>
            Name
          </th>
          <th>
            Annual
          </th>
          <th>
            Hours
          </th>
        </tr>
        <tr>
          <th class="line">
            of Part
          </th>
          <th class="line">
            Cost
          </th>
          <th class="line">
            to Repair
          </th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="name">
            Gauge
          </td>
          <td class="data">
            $425
          </td>
          <td class="data">
            12
          </td>
        </tr>
        <tr>
          <td class="name">
            Switch
          </td>
          <td class="data">
            $158
          </td>
          <td class="data">
            8
          </td>
        </tr>
        <tr>
          <td class="name">
            Control
          </td>
          <td class="data">
            $218
          </td>
          <td class="data">
            10
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

## **列表样式设置**

X/HTML 包含多种显示列表的方式，包括有序（编号）列表、无序（项目符号）列表和定义（缩进）列表。CSS 还添加了多个用于样式设置、定位以及替换标记符（每个列表项开头的数字、字母或项目符号）的属性。清单 2-14 生成一个列表的列表——一个定义列表，其中先包含一个无序列表，然后是一个有序列表。图 2-6 展示了这些列表在没有 CSS 或 HTML 样式时的样子。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_95_0.png)

图 2-6  没有任何样式或 CSS 的初始列表

###### 清单 2-14 列表的列表

```
<html>
    <head>
        <title>Listing 2-14</title>
        <style type="text/css">
            body { background : #dcdcdc; }
            dl {
                background : #fafad2;
                padding : 5px;
            }
            dt { font : bold 12pt arial; }
            ul { list-style-type : square; }
            ol { list-style-type : lower-alpha; }
        </style>
    </head>
    <body>
        <h2>Repair of RB 111 Controller </h2>
        <dl>
            <dt> Tools and Parts Needed </dt>
            <dd>
                <ul>
                    <li>RB 111 Test Bench </li>
                    <li>1492 Tester </li>
                    <li>XYZ 215 Circuit Board </li>
                    <li>DR 32 Display</li>
                    <li>DR 96 Keyboard </li>
                </ul>
            </dd>
            <dt> Test and Repair Procedure </dt>
            <dd>
                <ol>
                    <li>Plug the controller into the tester. </li>
                    <li>Run the first 7 tests set out in the manual. </li>
                    <li>If indicated, replace the circuit board. </li>
                    <li>Run the next 5 tests. </li>
                    <li>If indicated, replace the display. </li>
                </ol>
            </dd>
            <dt> Additional Steps </dt>
            <dd> Test the keyboard and replace as needed. </dd>
        </dl>
    </body>
</html>
```

在基本 X/HTML 代码中，为 **body** 和 **dl** 元素添加对比背景色的 CSS 样式；为 **dl** 添加内边距使文字不会紧贴背景边缘；设置 **dt** 元素的格式使其更像标题；然后将 **ul** 的标记符改为方块，将 **ol** 的标记符改为小写字母。结果如图 2-7 所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_96_0.png)

图 2-7  应用简单 CSS 样式的列表的列表

并非所有属性和值都在所有浏览器中起作用，例如在 IE 6 中，你需要在你认为会访问页面的浏览器中测试代码。

以下是关于使用 CSS 列表属性的一些说明：

- 如果你给列表项应用背景，当标记符位置设置为 "outside" 时，标记符不会共享该背景（它是透明的）。
- 如果你同时使用 `list-style-image` 和 `list-style-type` 属性，将使用 `list-style-image`。
- 可用的编号和字母系统类型如下：
  - decimal: 1, 2,...9
  - decimal-leading-zero: 01, 02,...99
  - lower-roman: i, ii, iii, iv...
  - upper-roman: I, II, III, IV...
  - lower-latin 或 lower-alpha: a, b, c,...z
  - upper-latin 或 upper-alpha: A, B, C,...Z
  - lower-greek: α, β, γ,...ω
- HTML 和 CSS 规范并未说明当列表用完一个字母表时会发生什么，因此对于长列表，你应该使用数字编号。

访问 W3C (www.w3.org/style/css/) 获取 CSS 的最新最详细说明，并使用 W3C CSS 验证器 (jigsaw.w3.org/css-validator) 测试你的 CSS 代码。

# 第二部分
## 添加 JavaScript 动态元素

本书第一部分通过 XHTML 和 CSS 的应用介绍了布局和一致样式设置的要素。第二部分介绍 JavaScript，这是一种可用于为网页创建动态元素的编程语言。第 3 章描述 JavaScript 使用的各种组件，然后第 4 章和第 5 章展示如何使用 JavaScript 在网页上创建多种动态元素。本部分前言提供有关编程和 JavaScript 的通用信息。

## 注意

JavaScript 和 PHP（第三部分介绍）之间有许多相似之处。为了提供一致的外观和格式，两部分之间存在一些重复内容。

### 理解编程与 JavaScript

尽管名称暗示了其他含义，JavaScript 实际上是一种为 Web 计算设计的编程语言。它为新手提供了一个学习编程机制和要素的机会，而无需使用更强大、更冗长的语言所需的某些开销。JavaScript 与 Java 没有直接联系，只是它们都来自 Sun Microsystems 并共享一些通用语法和关键字。

## 注意

JavaScript 主要被视为网页的编程工具，但它也被用于多种计算工具中，例如 Adobe Acrobat 和 Adobe Reader 对 PDF 文件中 JavaScript 的支持。

### 深入探究 JavaScript

编程语言简单地说就是一套称为*语法*的规则，用于规范你如何使用语言的各个元素与计算机通信。JavaScript 使用一种称为*OOP*（面向对象编程）的模型。你有*对象*（例如，窗口），对象具有*属性*（例如，长度）和*方法*，即对象可以执行的动作（例如打开），同时响应*事件*，即对对象执行的动作（例如点击）。一旦你熟悉了基本术语和语法，JavaScript 编程就只是编写一组顺序的*命令*或*语句*供计算机及其软件理解并执行。（第 3 章详细描述了 JavaScript 的元素和语法。）计算机与用户之间的这种交互发生的方式和位置，正是 JavaScript（和其他脚本语言）与传统语言（如 C 或 Java）的区别所在。



 ## 注意

许多程序员对 JavaScript 采用面向对象编程模型这一说法嗤之以鼻。我们将讨论留给纯粹的学者，但就 JavaScript 入门而言，该模型已足够接近，有助于解释这门语言的工作原理。

#### 编译型语言与解释型语言

尽管人们往往容易忘记，但有必要记住：计算机执行我们要求的众多复杂任务的能力，完全取决于数十亿个硅基电子开关是打开（1）还是关闭（0）。为了让我们摆脱二进制生活的繁琐，我们使用编程语言，它们以某种书面和口头语言的形式书写，然后被翻译成计算机能够理解的形式。用于创建应用程序的编程语言（例如，作为 Microsoft Word 核心的 Word.exe 文件）需要特殊软件来编写代码，然后必须通过*编译器*才能变为计算机可读取的格式。编译器是一种检查代码错误并将编写的代码转换为计算机代码的软件。虽然这种方法可以实现非常复杂的计算，但需要时间和资源来完成。

相比之下，JavaScript 被称为*解释型*语言，这意味着它的代码是即时运行的，无需编译。只需要一个文本编辑器来创建包含代码的文件，以及一个提供代码底层解释的网页浏览器（这与创建和显示 XHTML 页面的要求相同，本书第一部分有所描述；或与创建 PHP 页面的要求相同，第三部分有所描述）。虽然像 JavaScript 这样的解释型代码通常不如编译型代码高效或快速，但对于创建动态网页所使用的任务类型来说，其性能已经足够好，而且易于编辑和嵌入页面的优点足以弥补其不足。此外，编译型代码往往是特定平台的（Windows 与 Mac 之分），而解释型 JavaScript 则不是。

#### 客户端计算与服务器端计算

顾名思义，客户端和服务器端计算指的是编程代码执行的位置。对于 PHP 之类的服务器端编程，用户网页的请求被发送到托管的 Web 服务器，执行后结果再返回到用户浏览器中的网页。虽然拥有服务器及其可用的网络化资源和数据库提供了几乎无限的信息访问和计算能力，但这需要信息在客户端和服务器之间来回传输。此外，其服务由其他用户共享，因此存在延迟的可能性。客户端计算在用户的计算机上执行代码，使服务器能够执行更多密集型任务，并为用户提供更快的体验。（许多 Web 应用程序同时使用服务器端和客户端计算来分担 workload，并利用各自的优势。）JavaScript 是一种客户端程序，能够实现更快的代码执行和更即时的用户响应反馈。

#### JavaScript 简介

JavaScript 由 Sun Microsystems 和 Netscape 团队于 20 世纪 90 年代中期创建，旨在提供比 Netscape 浏览器中先前使用的客户端编译型 Java 语言更简化的 Web 编程方式。随着时间的推移，JavaScript 经历了版本更新（截至 2009 年春季的最新版本是 1.8）和配套产品（JScript 是 Microsoft Internet Explorer 的版本）的演变。源自 Netscape 的 Mozilla Firefox 应该能为您的代码提供最准确的解释。所有这些说明，与处理网页一样，您需要使用最新的浏览器（它们将包含各自最新的 JavaScript 版本），并使用不同的流行浏览器（Firefox、IE 和 Apple 的 Safari）测试您的作品，以确保代码按设计运行。

#### JavaScript 所需工具

要有效地使用 JavaScript，您需要一个支持 JavaScript 脚本编写和测试的开发环境。您需要以下工具：

- **JavaScript 脚本编写**，在编写脚本时提供代码辅助和验证。
- **JavaScript 脚本测试**，在您的开发计算机上进行。
- 浏览器中的**开发支持**，以帮助调试。

本书第一部分引言介绍并推荐了可以下载的这些工具包，包括：

- **Aptana Studio**，一个集成开发环境，默认提供对 HTML、CSS 和 JavaScript 的强大编写功能。
- **XAMPP**，Apache Web 服务器、MySQL 数据库服务器和 PHP 服务器的组合，运行在您的计算机上，模拟将网站上传到商业 Web 主机后看到的效果。
- **IE 6、IE 7 和 Firefox** 浏览器，都需要用来测试和调试您的脚本。由于很大比例的网页浏览人群在使用这些浏览器，因此在所有浏览器中测试您的网页非常重要。本书撰写时，IE 8 正处于最终测试阶段，也是您用于测试的强有力候选。它可用于 Windows XP 和 Windows Vista，以及最新版本 Windows 7。除了在这些浏览器上简单测试页面外，我们还推荐 Firefox 可用的 Web 开发者工具栏。

如果您尚未安装 Aptana Studio、XAMPP、IE 6、IE 7、Firefox 和 Firefox Web 开发者工具栏，请返回第一部分引言，按照说明下载并安装它们。本书剩余章节的讨论建议使用这些工具。

#### JavaScript 简介

JavaScript 是一种编程语言，是万维网的核心技术之一，与 HTML 和 CSS 并列。截至 2023 年，98% 的网站在客户端使用 JavaScript 来实现网页行为，通常会集成第三方库。

- JavaScript 实现交互式网页，是 Web 应用程序的重要组成部分。
- 它最初由 Brendan Eich 于 1995 年创建。
- JavaScript 符合 ECMAScript 规范。

#### JavaScript 所需工具

要开始 JavaScript 开发，您需要一个文本编辑器和一个网页浏览器。一些流行的选择包括：

- **编辑器：** Visual Studio Code、Sublime Text、Atom 或 Notepad++
- **浏览器：** Chrome、Firefox、Safari 或 Edge
- **版本控制：** Git 和 GitHub 用于代码管理

要在浏览器之外运行 JavaScript，您可以使用 Node.js，它允许您在计算机上执行 JavaScript 代码。

| 类别 | 描述 |
|----------|-------------|
| 前端 | 在浏览器中运行，处理用户界面 |
| 后端 | 在服务器上运行（Node.js），处理数据和逻辑 |
| 全栈 | 前端和后端开发的结合 |

# 第3章
JavaScript 基础

## 关键技能与概念

- 在 X/HTML 页面中使用 JavaScript
- JavaScript 基础入门
- 编写和测试 JavaScript
- 使用变量、常量和运算符
- 融入语句和表达式
- 构建函数和对象
- 应用条件语句

第3章讨论 JavaScript 使用的基本结构，以及 JavaScript 如何与 HTML 代码页面结合。本章介绍变量、运算符和函数，并展示其使用示例。if/else 语句及其控制条件与 for、while 和 do 循环一起演示。本章还回顾对象，包括其组成元素：属性、方法和事件处理程序。您将看到它们更常见用途的示例。

## JavaScript 介绍

任何语言的元素只有在根据一组规则和给定格式协同工作时，才能以可理解的形式共同运作。本节描述 JavaScript 中使用的基本技术和约定，帮助您入门，并提供捷径和建议，使处理脚本更加轻松高效。

### 在 X/HTML 页面中使用 JavaScript

您可以通过两种方式在 X/HTML 页面上使用 JavaScript 代码：直接放在使用它的 X/HTML 页面上，或放在单独的文件中。为单一用途编写的脚本最直接的方式是直接在受影响的页面上编写（本书主要使用这种方式）。随着您对 JavaScript 越来越熟悉并开发更高级的用途，您会发现将较长的脚本保存到单独的 JS 页面中，可以使网页更简洁，并且能够在网站的多个页面上使用相同的代码。



 > **说明**
> 术语*code*（代码）和*script*（脚本）可以互换使用，用于描述 X/HTML 页面中 `<script>` 标签内以及独立 JS 文件中的各种 JavaScript 语言元素。

#### 直接在 X/HTML 页面中输入 JavaScript

开始编写 JavaScript 的最简单方法是直接在 X/HTML 页面的 JavaScript 标签集 `<script></script>` 中输入脚本。`<script>` 标签放置在页面的 `<head>` 或 `<body>` 部分。通常，直接向页面输出内容的代码放在 `<body>` 部分的 X/HTML 中。放置在 `<head>` 部分的脚本一般由 `<body>` 部分其他位置的代码调用。清单 3-1 展示了这两种技术的使用。

**清单 3-1 脚本放置示例**

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
        <title>Listing 3-1</title>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            //The bgColor property of the document object is set to
            //Dodger Blue;
            document.bgColor="dodgerblue"
            //]]>
        </script>
    </head>
    <body>
        <script language="javascript" type="text/javascript">
        //<![CDATA[
            //The document.bgColor property is used to display the
            //hexadecimal of the background color set in the header;
            document.write("The hexadecimal value of Dodger Blue
            is "+ document.bgColor)
        //]]>
        </script>
    </body>
</html>
```

## 动态网页编程：初学者指南

> **说明**
> 清单 3-1 的目的是提供示例，展示脚本如何放置并在页面的头部和主体中有效使用。Firefox 对头部的代码存在问题，因为它出现在 `<body>` 标签之前，却又引用了该标签。由于 `<body>` 标签尚未定义，JavaScript 返回 #ffffff，即白色。IE 6–8 对此处理正常。此外，`document.bgColor` 已被视为过时并弃用。此处使用它是为了得到一个简单的示例。

#### 使用 JavaScript 文件

随着脚本变得越来越复杂，并且你在网站中发现代码的重复使用时，可以通过将大部分代码外包到带有 .js 文件扩展名的独立文本文件中，来减小 X/HTML 页面的体积并重用相同的代码。当你想要在页面中使用 JS 文件中的代码时（例如，myjavascript.js），可以通过向 `<script>` 标签添加属性来请求其执行，例如 `<script type = "text/javascript" src = myjavascript.js>`。

### JavaScript 基础

在开始尝试创建脚本之前，你需要熟悉 JavaScript 语法的几个一般方面。

#### 为脚本添加注释

JavaScript 允许你以两种方式向脚本添加注释：

- 以 `//` 开头的单行注释
  `//这是一条注释`
- 用 `/* */` 包裹的多行注释
  `/* 这是一条可以跨越多行的注释。 */`

> **提示**
> 强烈建议你为脚本添加注释，以帮助理解和调试工作。

#### 编码规范

在规范方面，JavaScript 相当宽松。以下是最常见的规范：

- JavaScript 包含一些区分大小写的元素。JavaScript 命令和变量名区分大小写。例如，如果你将 `person` 定义为变量名，稍后使用 **Person**，JavaScript 不会将第二个实例识别为原始变量。最好的经验法则是全部使用小写。当使用其他来源的 JavaScript 元素（如对象、属性、方法和事件处理程序）时，请使用书中、网页上或其他示例中引用的大小写。

- JavaScript 中的每条*语句*（或命令）通常以分号结尾。（语句是语法完整且正确以执行任务的代码行。）虽然不要求这样做，但这样可以防止错误、使调试更容易，并让你养成在其他坚持使用的语言中这样做的习惯（例如，第三部分中描述的 PHP）。

- 你可以将脚本封装在标签中，将其标识为字符数据，以免脚本被错误解释。主要担忧是较旧的浏览器无法识别 JavaScript 并返回错误。为了保护代码免受可能的问题（至少这类问题），请将脚本包含在 HTML 注释 `<!-- //-->` 中。展望未来，更大的担忧是 X/HTML 验证器会认为脚本中的某些内容在其管辖范围内并产生错误。为避免这种情况，占位符建议你的脚本以 `//<![CDATA[` 开头，以 `//]]>` 结尾。本书的 JavaScript 示例中显示了此标记，并包含在创建包含 JavaScript 的新 HTML 页面的建议模板中。

- 文本，即字母和数字的任意组合，也称为*字符串*，需要用引号括起来，单引号（`' '`）或双引号（`" "`）均可——它们在使用上的区别将在后面的说明中解释。引号必须以相同的成对形式出现。

- 合法的数字，可以带有小数点，不需要用引号括起来。

- 多个参数用逗号（,）分隔。

- 大多数函数要求其参数用括号括起来。

#### 特殊字符和转义序列

你可能想知道，既然引号用于标识字符串，那么如何显示作为字符串一部分要在 X/HTML 页面上显示的引号。为此，JavaScript 使用反斜杠（\），即所谓的*转义序列*，它告诉 JavaScript 不要将后面的字符作为脚本语法的一部分，而是将其视为*字面量*或文本字符串的一部分。例如：

```
document.write("My name is \"Marty\"");
```

*Marty* 两侧的双引号如果没有用反斜杠"转义"，就会产生错误。

另一种理解方式是，你想要添加一个字面量字符，在这种情况下是双引号。在这种用法中，我们通常说正在添加 JavaScript *特殊字符*。实际上，转义序列和特殊字符共享相同的代码并实现相同的结果。两者之间的唯一区别在于你是说杯子半满还是半空。

JavaScript 赋予特殊用途或作为转义序列使用的大多数字符都带有反斜杠前缀。以下是一些更常见的转义序列 / 特殊字符：

- \" 产生双引号。
- \' 产生单引号。
- \\ 产生反斜杠。
- \b 产生退格。
- \r 产生回车。
- \n 产生换行。
- \t 产生制表符。

> **说明**
> 虽然可以用单引号或双引号来括住字符串，但在某些情况下，其中一种更为可取。用单引号括住字符串时，可以在字符串中使用字面量的双引号而无需反斜杠，如下所示。不过，使用单引号时，除 \' 或 \\ 以外的转义序列会显示反斜杠而不执行其功能。使用双引号时，所有转义序列都有效。

```
document.write('My name is "Marty"');
```

#### 避免使用保留字

有些被称为*保留字*或*关键字*的词语（见表 3-1），不应于在 JavaScript 中命名元素，因为它们是语言的一部分，对 JavaScript 解释器具有特殊含义。

| abstract | boolean | break | byte | case |
| --- | --- | --- | --- | --- |
| catch | char |_revision_needed_ | const | continue |
| debugger | default | delete | do | double |
| else | enum | export | extends | false |
| final | finally | float | for | function |
| goto | if | implements | import | in |
| instanceof | int | interface | label | long |
| native | new | null | package | private |
| protected | public | return | short | static |
| super | switch | synchronized | this | throw |
| throws | transient | true | try | typeof |
| var | void | volatile | while | with |

**表 3-1** JavaScript 保留字

### 编写和测试 JavaScript

作为解释型语言，JavaScript 不需要任何辅助软件（如软件开发工具包，即 SDK）来编写、检查错误或测试。你可以使用任何用于编写 X/HTML 的文本编辑器开始编写 JavaScript；不过，我们强烈建议使用第一部分简介中介绍的 Aptana Studio。为了简化 JavaScript 工作，我们进一步建议你创建一个基本模板来开始任何脚本项目。

#### 在 Aptana 中修改默认 HTML 页面

当你在 Aptana 中创建新的 HTML 文件时，它会添加必需的 HTML 头部数据和标签以在浏览器中显示页面。通过一些简单的修改，你可以修改这个默认文件以包含 X/HTML 文档类型（以确保文件符合未来的 Web 规范），并添加 `<script>` 标签、属性和可选注释以容纳 JavaScript（本章前面已描述）。要在 Aptana 中修改默认 HTML 文件，请执行以下操作：

> **提示**
> 要在 Aptana 中创建不包含 `<script>` 标签的 X/HTML 文件（在修改默认新 HTML 页面文本之后），只需在 Aptana 编辑器中删除添加的文本即可。



 **1. 打开 Aptana Studio**（有关安装 Aptana Studio 的信息，请参阅第 1 章）。

**2. 单击菜单栏中的 shrift File**，然后单击 **New | Untitled HTML File**。

**3.** 在 Aptana 编辑器（右窗格）中，按如下所示和清单 3-2 修改文本。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_111_0.png)

**4.** 选择修改后的文本，然后按 **CTRL-C** 将文本复制到剪贴板。

**5. 单击 Window**，然后单击 **Preferences**。

**6.** 在 Preferences 对话框中，单击 Aptana 旁边的加号以展开其列表。

**7. 展开 Editors**，然后单击 **HTML**。

**8.** 在 HTML 窗格中，在窗格底部附近的 **Initial HTML File Contents** 下，选择默认文本，然后按 **CTRL-V** 将修改后的文本粘贴到其位置，如图 3-1 所示。

**9. 单击 Apply**，然后单击 **OK** 关闭 Preferences 对话框。

第 3 章：JavaScript 基础 95

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_112_0.png)

图 3-1 更改在 Aptana 中创建的新 X/HTML 页的默认代码，以添加支持 XML 和 JavaScript 的标签。

##### 清单 3-2 更改后的 Aptana 页面默认 X/HTML 代码

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
    <head>
        <meta http-equiv="Content-Type" content="text/html;
        charset=iso-8859-1">
        <title>Untitled Document</title>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            //]]>
        </script>
    </head>
    <body>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            //]]>
        </script>
    </body>
</html>
```

#### 测试你的工作

正如本部分简介中提到的，由于浏览器在解释 X/HTML 和脚本的某些方面存在差异，因此使用主流浏览器测试你的工作以确定这些差异是否影响你的意图非常重要。清单 3-3 中显示的 JavaScript 代码示例在两个主流浏览器中显示的对话框略有不同（见图 3-2）。在这种情况下，差异是轻微的，仅涉及外观，无需担心。然而，情况并非总是如此。此时请勿担心清单 3-3 中代码的外观或你对其缺乏理解。本章的其余部分以及接下来的两章将阐明一切。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_113_0.png)

##### 图 3-2 Firefox（左）和 IE（右）使用相似但略有不同的解释来显示消息框。

> 本章其余部分显示的清单已省略网页中的一些默认 X/HTML 代码（例如 DOCTYPE 声明），以提供更简洁的示例。

##### 清单 3-3 浏览器差异示例

```
<html>
    <head>
        <title>Listing 3-3</title>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            // This code produces the classic Hello World! message
            box window.alert("Hello, World!");
            //]]>
        </script>
    </head>
    <body>
    </body>
</html>
```

### JavaScript 的组成部分

正如口语包含名词、动词、副词、形容词和其他词性元素一样，编程语言也有自己的一组组成部分。在本部分中，我们将介绍 JavaScript 的更常见元素，为第 4 章和第 5 章构建工作脚本奠定基础。在本节中，我们将探讨 JavaScript 的信息类型、变量、运算符、语句和函数。在下一部分中，我们将探讨作为控制结构的语句。

> 与任何语言一样，JavaScript 在语言的每个部分都包含许多元素，远非此处所能涵盖。要查看完整的列表，请访问 www.javascriptkit.com/jsref/ 或 www.webreference.com/javascript/reference/core_ref/contents.html。

#### 变量和常量

JavaScript 中使用的信息（或数据）分为两类。无论哪种情况，它都由你指定的名称及其数据类别或*数据类型*定义。

- **变量**是在脚本执行期间不同时刻可以包含不同值的项目，以关键字 `var` 开头，后跟您指定的名称。
- **常量**在脚本执行期间包含相同的值。

## *提示*

> 变量在脚本执行期间的不同时间可能具有不同的值，而常量在整个执行期间具有单个值。

##### 数据类型

JavaScript 通常会根据数据在脚本中的上下文来识别您使用的数据类型，从而避免您需要指定特定类型。但是，在 JavaScript 误解您的意图的情况下，了解可用的数据类型及其一些特性会很有帮助。表 3-2 显示了更常见的数据类型。

- 布尔值 `FALSE` 等同于整数 0、浮点数 0.0、空字符串或字符串 "0"、零元素数组或 NULL。其他一切都是 TRUE。
- 整数默认为十进制（基数为 10）数字。要使其成为八进制（基数为 8），请在前面加 0（零）。要使其成为十六进制（基数为 16），请在前面加 0x。
- 非常大的整数（大于 2,147,483,647）被视为浮点数。
- 如果将两个整数相除，除非这些数字可以整除，否则您将得到浮点数。
- 由于类似三分之一的分数的无限进展，浮点数在最后一位数字上并不精确。因此，您不应该比较两个浮点数是否相等。
- 包含紧接左引号的数字（整数或浮点数）的字符串可以用作数字。例如，"18.2" 和 "4 cars" 都可以用作数字，而 "his 4 cars" 则不能。

| 数据类型/子类型 | 名称 | 描述 | 示例 |
| --- | --- | --- | --- |
| 布尔值 | bool | 要么是 TRUE 要么是 FALSE，不区分大小写，但通常为大写 | TRUE, FALSE |
| 数值/浮点数 | float | 带小数点的分数；可能为负数，可能使用科学记数法 | 7.34, -21.89, 2.31e3 |
| 数值/整数 | int | 不带小数点的整数；可能为负数 | 43, 928, -4 |
| 数值/Null | null | 没有任何值 | NULL |
| 字符串 | string | 用单引号或双引号括起来的一系列字符（256 个字母、数字和特殊字符之一） | "Mike", 'Seattle', "1495 W. 18th St" |
| 未定义 | | 已命名但未分配值的变量 | |

表 3-2 JavaScript 数据类型

## 注意

在本书中，仅用于讨论目的而使用了两种额外的伪类型："mixed" 用于任何其他类型的组合，"numbers" 用于整数和浮点数的组合。

##### 命名约定

您为变量或常量（或 JavaScript 中的任何其他标签）指定的名称区分大小写（请参阅本章前面的"JavaScript 基础知识"），可以以字母 a-z（或 A-Z，但不推荐）或下划线（_）开头，可以是任意长度，并且可以包含字母、数字、下划线和西欧字母表中的字符。虽然您可能会发现某些特殊字符是允许的，但最佳做法是不要使用它们。不允许使用空格。

一个好的做法是让变量和常量名称更具自描述性，并在此过程中避免与预定义名称发生任何冲突的可能性。例如，如果您正在收集购买者的姓名和地址，您可能会倾向于使用 name、street 和 city。虽然这些名称没有什么问题，但最好养成使用复合名称的习惯，这些名称更具描述性，并且避免使用常见名称，例如 buyer_name、buyer_street 和 buyer_city。键入这些名称可能需要多花几秒钟，但它们不会与其他名称混淆。此外，大多数程序员都非常擅长剪切和粘贴以减少打字量。



 ## 提示

如果你在程序中查找一个问题或错误时遇到了困难，请检查你为变量和常量分配的名称；尝试更改任何可能与预定义或保留名称冲突的名称，例如将 **name** 改为 **buyer_name**，或将 **private** 改为 **my_own**。

#### 运算符

创建变量或常量后，你将希望通过赋值、计算或比较来为其赋予值。JavaScript 定义了多种类型的运算符来完成这些操作，如表 3-3 所示。

| 类型运算符 | 名称 | 示例 | 说明 |
|---|---|---|---|
| **算术** | | | 对两个操作数执行算术计算，操作数可以是变量、数字或一个数字和一个变量。 |
| + | 加法 | `a + b` | 两个操作数相加。 |
| - | 减法 | `a - b` | 返回两个操作数的差。 |
| * | 乘法 | `a * b` | 两个操作数相乘。 |
| / | 除法 | `a / b` | 两个操作数相除。 |
| -- | 递减 | `--a`<br>`a--` | 从a中减去1并返回a。<br>返回a，然后从a中减去1。 |
| ++ | 递增 | `++a`<br>`a++` | 给a加1并返回a。<br>返回a，然后给a加1。 |
| % | 取模 | `a % b` | 返回除法运算的余数。 |
| = | 一元取反 | `=a` | 将负数转换为正数，或将正数转换为负数。 |
| **赋值** | | | 用一个值替换另一个值。 |
| = | 赋值 | `a = 7` | a被设置为7。 |
| += | 加并赋值 | `a += 2` | a增加2并赋值为新值。 |
| -= | 减并赋值 | `a -= 2` | a减少2并赋值为新值。 |
| *= | 乘并赋值 | `a *= 2` | a乘以2并赋值为新值。 |
| /= | 除并赋值 | `a /= 2` | a除以2并赋值为新值。 |
| %= | 取模并赋值 | `a %= 2` | a除以2并将余数赋值。 |

表 3-3 JavaScript 运算符

| 类型运算符 | 名称 | 示例 | 说明 |
|---|---|---|---|
| **位运算** | | | 逻辑运算用于打开或关闭整数中的特定位。 |
| & | 与 | `a & b` | a和b中都设置的位被设置。 |
| \| | 或 | `a \| b` | a或b中设置的位被设置。 |
| ^ | 异或 | `a ^ b` | a或b中设置的位但不包括两者都被设置的位被设置。 |
| ~ | 非 | `~a` | a中设置的位不被设置。 |
| << | 左移 | `a << b` | 将a中的位向左移动b步（每步相当于乘以2）。 |
| >> | 右移 | `a >> b` | 将a中的位向右移动b步（每步相当于除以2）。 |
| **比较** | | | 比较两个值并返回 TRUE 或 FALSE。 |
| == | 等于 | `a == b` | 如果a等于b，则为TRUE。 |
| === | 全等 | `a === b` | 如果a与b全等，则为TRUE。 |
| != | 不等于 | `a != b` | 如果a不等于b，则为TRUE。 |
| !== | 不全等 | `a !== b` | 如果a与b不全等，则为TRUE。 |
| < | 小于 | `a < b` | 如果a小于b，则为TRUE。 |
| > | 大于 | `a > b` | 如果a大于b，则为TRUE。 |
| <= | 小于或等于 | `a <= b` | 如果a小于或等于b，则为TRUE。 |
| >= | 大于或等于 | `a >= b` | 如果a大于或等于b，则为TRUE。 |
| **逻辑** | | | 逻辑运算。 |
| && | 与 | `a && b` | 如果a和b都为TRUE，则为TRUE。 |
| \|\| | 或 | `a \|\| b` | 如果a或b任一为TRUE，则为TRUE。 |
| ! | 非 | `!a` | 如果a不为TRUE，则为TRUE。 |
| **其他** | | | |
| ?: | 条件 | `Condition ? value : value` | 一个if-then-else语句，条件设置在?的左侧，值分别放在:的两侧。 |
| delete | 删除 | `delete window2` | 删除一个对象、属性或数组元素。 |

表 3-3 JavaScript 运算符（续）

## 注意

条件运算符，也称为"三元运算符"，将在本章后面的"控制结构"部分讨论。

如果在一个表达式中组合多个运算符，优先级顺序如下，从高到低依次为：++, --, !, delete, *, /, %, +, -, ., <<, >>, <, hosp<=, >, >=, ==, !=, ===, !==, &, ^, |, &&, ||, ?:, =, +=, -=, *=, /=, &=, and, xor, or。你可以使用括号来改变优先级顺序。关于JavaScript运算符的其他说明：

- 当算术运算符(+)用于组合文本时（例如 window.alert ("Marty" + "Matthews") 在对话框中显示 "Marty Matthews"），或将文本与数字组合时（例如 window.alert (1234 + "Broadway, " + "Anytown") 显示 "1234 Broadway, Anytown"），该操作称为连接。

- 取模运算(%)不会产生百分比；相反，它给出余数，即整除后剩余的部分。

- 等号(=)并不意味着"相等"，它意味着"赋值"或"替换"。

- 要比较两个变量，你可以使用相等(==)或全等(===)。区别在于 == 测试两个值是否相等，与值的类型无关，而 === 测试两个值不仅值相等，而且类型相同。

- 如果 a = "2" 且 b = 2.0，它们不是全等的，因为一个是字符串，另一个是浮点数，但它们的值是相等的。

清单 3-4 展示了 JavaScript 变量和运算符的使用示例。此脚本返回的结果如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_119_0.png)

##### 清单 3-4 变量和运算符示例

```
<html>
    <head>
        <title>Listing 3-4</title>
    </head>
    <body>
        <h1>Example of Variables and Operators</h1>
        <script language="javascript" type= "text/javascript">
            //<![CDATA [
            //Math
            var a = 2;
            var b = 5;
            document.write("Add ", a, " and ", b, " to get ",
                a+b, "<br>");
            document.write("Multiply ", a, " by ", b, " to get ",
                a*b, "<br>");
            document.write("Divide ", a, " by ", b, " to get ",
                a/b, "<br>");
            document.write("Modulus ", a, " by ", b, " to get ",
                a%b, "<br>");
            //Assign, Increment and Concatenate
            var a = 7;
            document.write("Increment ", a, " by 2 to get ", a+=2,
                "<br>");
            document.write("Increment ", a, " by 1 to get ", ++a,
                "<br>");
            first_name = "Mary "; last_name = "Smith";
            document.write("Concatenate ", first_name, " and ",
                last_name, " to get ", first_name + last_name,
                "<br>");
            //Comparison
            a = "2"; b = 2.0; c = 4; d = a == b; e = a === b;
            document.write("Test if ", a, " and ", b,
                " are equal: ", a==b, "<br>");
            document.write("Test if ", a, " and ", b,
                " are identical: ", a===b, "<br>");
            document.write("Test if ", a, " is less than or equal
                to ", c, ": ", a<=c, "<br>");
            //Logical
            document.write("Test if ", d, " and ", e, " are TRUE: ",
                d&&e, "<br>");
            document.write("Test if ", d, " or ", e, " are TRUE: ",
                d||e, "<br>");
            //]]>
        </script>
    </body>
</html>
```

#### 语句和表达式

JavaScript 脚本包含注释或语句。*语句*是一行代码，其语法完整且正确以执行一项任务，通常是位于分号以及 JavaScript 开标签和闭标签之间的任何内容。通常语句是以分号结尾的单行代码，但你可以在一行中有多个语句，也可以有跨越多行的语句。语句包含一个或多个表达式。

*表达式*是任何具有值的东西。*值*是可以赋给变量的任何东西，因此值可以是任何数据类型：整数、浮点数、字符串或布尔值。虽然 NULL 数据类型表示没有值，但在此讨论中它仍被视为一个值。

表达式可以包含表达式，换句话说，表达式是构建块，可用于构建其他表达式。例如，a = 2 包含三个表达式：2、a 和 a = 2。

#### 函数

函数是一段脚本（一个*代码片段*），它执行某些操作并可以在更大的脚本中反复调用。全局函数已经存在，而你自己编写的是用户自定义函数。有些函数要求你向它们传递值或*参数*，函数使用这些参数向你返回一个值。其他函数在调用时简单地返回一个值。

##### 全局函数

与其他语言和程序（如 PHP 或 Microsoft Excel）不同，JavaScript 没有大量的内部全局函数来执行非*对象特定*的日常任务。另一方面，JavaScript 包含一整套*方法*，它们是与对象相关的函数调用。（方法和对象将在本章后面描述。）这样，你可以使用 JavaScript 方法实现与使用其他语言和程序中的内部函数基本相同的结果。表 3-4 列出了 JavaScript 更常用的全局函数。

### 注意

构造函数用于创建对象。该函数不是一个特定的全局函数，而是使用用户函数的标准语法来构造对象的一种方式，包括命名对象、声明其参数，并将参数值分配给对象的属性。



 | 函数 | 说明 |
| --- | --- |
| escape( ) | 返回字符串的十六进制编码 |
| eval( ) | 计算一个 JavaScript 代码字符串，不引用特定对象 |
| isFinite( ) | 计算参数以确定它是否为有限数字 |
| isNaN( ) | 计算参数以确定它是否为非数字（NaN） |
| parseFloat( ) | 解析字符串参数并返回浮点数 |
| parseInt( ) | 解析字符串参数并返回整数 |
| unescape( ) | 返回十六进制编码对应的 ASCII 字符串 |

表 3-4 全局函数

##### 用户自定义函数

编写 JavaScript 脚本时，你经常会发现想要重复使用相同的代码。你可以简单地将代码复制到所有需要使用它的地方，但如果你想修改那段代码，就必须在复制的所有地方都进行修改。解决方案是创建一个包含你想要重复的代码的函数，然后在需要使用它的地方直接调用该函数。函数还能让你将代码分段或隔离，从而更易于调试和维护。

使用函数还有一个更重要的原因。到目前为止，本章中的所有 JavaScript 代码都旨在页面加载时运行。但如果你不希望这样，可以创建一个函数，将其放在 X/HTML 头部，这样它就不会运行，直到被调用。

与预定义或全局函数一样，用户定义的（以下简称"用户"）函数可以可选地接收传递给它们的参数，并在执行后返回一个值。一旦用户函数被定义，它就会被调用，也就是说脚本中的某个语句请求该函数执行它被设计来执行的操作。函数本身可以执行你能用 JavaScript 做的任何事情，使用 JavaScript 的所有特性，包括调用其他函数，甚至调用自身来创建递归函数（这不应超过 100 次，否则可能会发生错误）。

用户函数使用 function 关键字按以下形式定义：

```
function name(argument1, argument2,...)
{
    [any JavaScript statements];
    return returnValue;
}
```

**注意**

无参数函数通过提供*名称*和一组空括号来定义，例如：

function calrate()

你给函数指定的名称使用与变量、常量和其他标签相同的命名规则。它区分大小写，可以以字母 *a–z* 或 *A–Z* 或下划线（_）开头，可以是任意长度，并且可以包含字母、数字、下划线和西欧字母表中的字符。

清单 3-5 展示了用户函数的一个示例，其结果如下所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_123_0.png)

**清单 3-5** 用户自定义函数

```
<html>
    <head>
        <title>Listing 3-5</title>
    </head>
    <body>
        <h1>User-Defined Function</h1>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            function tokm(miles)
            {
                var km = miles * 1.6;
                return km;
            }
            document.write("<b>Directions:</b><br>");
            document.write("From the highway turn right,<br>");
            " ("go 2.4 miles or " + tokm(2.4) + " km, turn left<br>");
```

```
document.write("go 1.3 miles or " + tokm(1.3) +
  " km, turn right<br>");
document.write("go 1.9 miles or " + tokm(1.9) + " km,
  you're there.<br>");
//]]>
</script>
</body>
</html>
```

#### 对象

如第二部分介绍中所述，JavaScript 是一种基于对象的编程语言。对象是网页的可视元素，如窗口、按钮、复选框和日期。对象也可以是更抽象的元素，如数学计算和数组。你可能会发现 JavaScript 中的预定义对象足以满足你的基本编程工作需求，但你也可以创建自己的对象。更有趣的是，对象可以有子对象，这开始类似于构成网页的元素之间的家族树层次结构。

# 提示

JavaScript 有数十种预定义对象，许多对象都有多个属性和方法，数量太多无法在此书中一一列举。我们建议你获取列出对象及其组成的在线和硬拷贝参考图表。我发现有用的参考资料有 www.javascriptkit.com 以及 Thomas Powell 和 Fritz Schneider 所著、McGraw-Hill/Professional 于 2004 年出版的《JavaScript: The Complete Reference》。

预定义对象由关键字名称标识，自定义对象则使用与本章前面描述的变量命名规则相同的规则赋予唯一名称。你可以在网页中拥有某个对象的多个实例。以 window 对象为例。网页中的每个窗口或框架都有唯一的名称标识，并通过其特征或属性、它能做的事情（称为方法）以及影响它的用户事件（例如鼠标点击）来进一步定义。对象与其组成部分之间的关系通过点语法显示，即对象名称与其组成部分之间用句点分隔。在本章开头（参见清单 3-3），你曾看到将 alert 方法应用于 window 对象以产生警告对话框（Hello World!）：

```
window.alert("Hello, World!");
```

其中 window 是预定义对象，alert 是显示警告消息框的方法，而 "Hello, World!" 是在消息框中显示文本的方法值。

本章到目前为止你看到的另一个点语法示例是常用于将脚本结果显示到浏览器的语句：

```
document.write("From the highway turn right,<br>");
```

##### 自定义对象

你可以创建自己的对象，例如商店网站上出售的家具物品。你可以使用以下两种方法之一来创建对象：

- 使用**构造函数**先创建对象的结构，然后使用 new 关键字创建对象的实例。
- 使用**对象初始化器**在一个语句中命名对象并分配属性值。

使用构造函数时，你先命名一个对象，然后将其参数值分配给对象的属性。例如：

```
function furniture()
{
this.era=era
this.wood=wood
}
```

**注意**

JavaScript 关键字 this 的含义是"此对象"，即参数被分配给*此*正在被定义的对象。

接下来，你必须使用关键字 new 将对象的实例创建为变量，并为其赋值。例如：

```
var buffet = new furniture("Eastlake", "Oak");
```

对象初始化器方法可以达到相同的结果，但方式更为简洁，直接创建对象实例：

```
buffet = {era: "Eastlake", wood: "Oak"}
```

###### 属性

对象具有属性，使你能够描述对象，区分同一对象的不同变体，以及根据需要自定义对象。例如，你可以通过外部高度和宽度尺寸（`outerHeight`/`outerWidth`）以及内部或显示区域尺寸（`innerHeight`/`innerWidth`）来修改窗口。某些对象有多个属性（如窗口），而另一些则很少（字符串对象只有一个属性，`length`）。此外，不同类型的对象可以具有相同的属性（但它们不太可能在那些属性值上做共享）。

属性通过点语句语法应用于对象，形式为 `objectname.propertyname="value"`；清单 3-6 展示了使用 JavaScript 的属性的两种用法。首先，在 head 部分，使用颜色名称设置网页的背景颜色。然后，在页面的 body 部分，调用背景颜色并返回其十六进制代码。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_126_0.png)

## 清单 3-6 属性示例

```
<html>
    <head>
        <title>Listing 3-6</title>
        <script language="javascript" type= "text/javascript">
            //<![CDATA [
            document.bgColor="yellow"
            //]]>
        </script>
    </head>
```



 ```
<body>
    <h1>Properties give life to objects</h1>
    <script language="javascript" type="text/javascript">
        //<![CDATA[
        document.write("The hexadecimal value of the yellow background color is " + document.bgColor);
        //]]>
    </script>
</body>
</html>
```

##### 方法

对象可以执行的动作称为*方法*。在很多情况下，你可以将方法视为对象预先定义好的函数。例如，要返回三的平方根，你可以使用 math 对象的平方根方法。使用点语法，形式如下：`math.sqrt(3)`。在前面关于对象的章节中，使用 `alert()` 方法显示消息框也是使用方法来触发对象动作的另一个例子。与属性一样，不同的对象和对象类型共享许多相同的方法。

> **提示**

由于对象的属性和方法都以 `object.method` 或 `object.property` 的形式书写，那么如何区分它们呢？与属性相关的值是通过等号来设置的，并将值用引号括起来（`document.bgColor="dodgerblue"`）。方法中使用的值则用括号括起来（`Math.sqrt(3)`）。

##### 事件处理器

JavaScript 允许你通过使用预定义的*事件处理器*，轻松利用用户在你的网页上执行的事件或*触发器*，例如鼠标点击和页面打开。事件处理器识别正在发生的事件，然后执行一个或多个任务，从而在网页和用户之间添加了一层易于编码的交互性。例如，当用户将鼠标指针悬停在按钮上时，会打开一个警告对话框，警告点击该按钮的后果（单击动作由第二个事件处理器定向到另一个动作）。第4章提供了多个使用事件处理器来活跃网页的例子。

表 3-5 列出了 JavaScript 事件处理器及其执行相应任务所需的触发器。

| Event Handler | Event Trigger |
| --- | --- |
| onAbort | An image's loading is interrupted. |
| onBlur | Focus is removed from an element. |
| onChange | Contents of a form are changed. |
| onClick | An element is single-clicked. |
| onDblClick | An element is double-clicked. |
| onDragDrop | An object is dragged-and-dropped into a window. |
| onError | An error occurs when loading a web page or picture. |
| onFocus | The user places the focus on an element. |
| onKeyDown | The user presses a defined key. |
| onKeyPress | The user presses and holds down a defined key. |
| onKeyUp | The user releases a defined pressed key. |
| onLoad | A web page completes loading in a browser. |
| onMouseDown | The user presses a mouse button. |
| onMouseMove | The user moves the mouse pointer. |
| onMouseOut | The user moves the mouse pointer from a link. |
| onMouseOver | The user moves the mouse pointer to a link. |
| onMouseUp | The user releases a mouse button. |
| onMove | A window or frame is moved. |
| onOpen | A web page opens in a browser. |
| onReset | A form is reset. |
| onResize | A window or frame is resized. |
| onSelect | A field in a form is selected. |
| onSubmit | A user submits a form. |
| onUnload | A user opens another web page. |

**表 3-5** JavaScript 事件处理器

### 控制结构

简单的脚本从第一条语句执行到最后一条语句，不会中断或改变方向。通常你会希望询问脚本应该走这条路还是那条路，或者返回去重新执行某段特定的代码。这就是控制结构的目的，包括 **if/else** 语句；**while**、**do-while** 和 **for** 语句；以及 **switch** 语句等。

#### If/Else 语句

if/else 语句是 JavaScript 中主要的决策结构。它允许你指定：如果某个表达式为 TRUE，则执行一组语句，否则执行另一组语句。其形式如下：

```
if (conditional expression) {
    statements executed if TRUE;
}
else {
    statements executed if FALSE;
}
```

else 语句是可选的，只有当你想在条件表达式为 FALSE 时执行其他操作而不是继续执行脚本时才需要。此外，你可以嵌套 if/else 语句，如下所示：

```
if (outer conditional expression) {
    statements executed if first conditional is TRUE;
    if (inner/nested conditional expression){
        statements executed if second conditional is TRUE;
    }
    else {
        statements executed if second conditional is FALSE;
    }
}
else {
    statements executed if first conditional is FALSE;
}
```

在所有情况下，条件表达式必须产生布尔值 TRUE 或 FALSE（1 或 0）。如果一个变量仅仅存在，即它已被定义且包含的内容不是 NULL、FALSE 或 0，那么它就是 TRUE。

> **提示**

如果你将变量定义为包含 NULL、TRUE 或 FALSE 等常量，你必须记住*不要*将常量放在引号中。

许多条件表达式是比较运算，测试两个元素是否相等、大于或小于。记住，当你在 JavaScript 中测试相等性时，必须使用双等号（==），而不是单个等号，后者表示赋值。

清单 3-7 展示了几个 if/else 语句的例子，结果如下所示。后面的章节中还会展示更多例子。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_130_0.png)

##### 清单 3-7 If/Else 语句

```
<html>
    <head>
        <title>Listing 3-7</title>
    </head>
    <body>
        <h1>If/Else Examples</h1>
        <script language="javascript" type= "text/javascript">
            //<![CDATA [
            //if the variable "a" is declared, return True/write
            //True; else return False/write False. Since no variable
            //"a" declared, expect False;
            if (a){
            document.write("True <br>");
            }
            else {
                document.write("False <br>");
            }
            //If the variable "a" is declared, return True/write
            //True; else return False/write False. Since variable
            //"a" is declared, expect True;
            var a = "Something";
            if (a){
```

```
document.write("True <br>");
}
else {
    document.write("False <br>");
}
//If variable "state" equals "WA", return True/write
  "Pacific Northwest;" else return False/write Somewhere
  Else. Since variable "a" equals "CA", expect False;
var state="CA";
if (state=="WA"){
    document.write("Pacific Northwest <br>");
}
else {
    document.write("Somewhere Else <br>");
}
//]]>
</script>
  </body>
</html>
```

#### 三元运算符

在 JavaScript 脚本中进行 if/else 决策的简写方法是使用三元运算符（? :），其中 ? 替换 if 测试并跟在条件表达式之后，: 替换 else。例如，(a==3) ? "True" : "False";

#### While 和 Do-While 语句

while 和 do-while 语句是循环结构，允许你重复执行一段代码，直到条件表达式不再为 TRUE。while 语句是这类语句的基础，形式如下：

```
while (conditional expression) {
    statements executed while TRUE;
}
```

do-while 语句与 while 语句类似，区别在于条件表达式在语句末尾而不是开头，这使得即使 while 语句为 FALSE，do 部分也会执行。do-while 语句的形式如下：

```
do {
    statements executed while TRUE;
}
while (conditional expression);
```

最常见的条件表达式是将计数器与某个结束值进行比较——换句话说，初始化一个计数器，然后循环执行一些语句，每次循环递增计数器，直到计数器超过结束值。清单 3-8 展示了 while 和 do-while 的这种例子，结果如下所示。你可以看到 while 语句一直运行到计数器结束。在 do-while 语句的情况下，do 语句为 TRUE 并执行一次，但 while 语句为 FALSE，不循环，也不执行 write 语句。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_132_0.png)

##### 清单 3-8 While 和 do-while 示例

```
<html>
    <head>
        <title>Listing 3-8</title>
    </head>
    <body>
        <h1>While Example</h1>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            var i = 1;
```



 ```
while (i <= 10) {
    document.write("Guess how many times this
    While loop will repeat?<br>");
    i += 1;
}
//]]>
</script>
<h1>Do-While 示例</h1>
<script language="javascript" type="text/javascript">
//<![CDATA [
var i = 10;
do {
document.write("Guess how many times this Do While loop
  repeats?<br>")
i += 1;
} while (i < 11);
//]]>
</script>
</body>
</html>
```

#### For 语句

for 语句是另一种额外的循环结构。for 语句与其他语言中的对应结构类似，将计数器的初始化、条件限制和增量都放在紧跟 for 之后的一系列表达式中。for 语句采用以下形式：

```
for (initializing expression; conditional expression; incrementing
expression)
    {
    statements executed while TRUE;
    }
```

在其基本形式中，for 表达式可能是 for (i = 1; i <= 5; i++)，其中 i++ 在使用 i 之后将其递增。如果这些表达式中的任何一个在脚本的其他地方处理，它们可以在 for 表达式中留空，其最小形式为 for ( ; ; )。

清单 3-9 展示了 for 语句的示例，结果如下所示。for 语句的使用方式与 while 非常相似。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_134_0.png)

##### 清单 3-9 For 示例

```
<html>
    <head>
        <title>Listing 3-9</title>
    </head>
    <body>
        <h1>For Example</h1>
        <script language="javascript" type="text/javascript">
            //<![CDATA[
            for (i=1; i <= 10; i++) {
                document.write("I bet you know how many times this will repeat!<br>")
            }
            //]]>
        </script>
    </body>
</html>
```

#### Switch 语句

switch 语句类似于一系列 if/else 语句。switch 语句用于将单个变量与多个不同的值进行比较，并根据不同的值执行不同的操作。switch 还使用三个额外的关键字：case、break 和 default，其形式如下：

```
switch (avariable) {
    case "1" :
        statements executed while TRUE;
        break;
    case "2" :
        statements executed while TRUE;
        break;
    case "3" :
        statements executed while TRUE;
        break;
    default :
        statements executed when all cases are FALSE;
}
```

switch 语句中的每个 case 表达式将 switch 变量与 case 值进行比较，case 值可以是字符串。如果相等，则执行 case 表达式后面的语句，然后 break 表达式将脚本的流程发送到 switch 结束花括号后的第一条语句。如果没有任何 case 表达式成功，则执行 default 表达式后面的语句，脚本流程退出 switch 语句。清单 3-10 演示了这是如何工作的，并提供了以下结果：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_135_0.png)

##### 清单 3-10 Switch 语句示例

```
<html>
    <head>
        <title>Listing 3-10</title>
    </head>
    <body>
        <h1>Switch Statement Example</h1>
        <p><b>The Computer Wizard!</b></p>
        <p>Ask a Yes/No question and click Refresh.</p>
        <script language="javascript" type="text/javascript">
            //<![CDATA [
            var randNum = Math.ceil(8*Math.random())
            switch (randNum) {
                case 1 :
                    document.write("Definitely Yes!");
                    break;
                case 2 :
                    document.write("Probably Yes!");
                    break;
                case 3 :
                    document.write("Definitely Maybe!");
                    break;
                case 4 :
                    document.write("Probably No!");
                    break;
                case 5 :
                    document.write("Definitely No!");
                    break;
                default :
                    document.write(randNum,"<br>");
                    document.write("Computer Malfunction, Try Again");
            }
            //]]>
        </script>
    </body>
</html>
```

在后续章节中，你将了解如何将 JavaScript 的众多部分组合成一个真正有用的脚本，例如在网页之间或会话之间传递数据，在服务器上读写文件，或验证用户身份。

一本关于 JavaScript 的优秀书籍是 *JavaScript: A Beginners Guide, Third Edition*，由 John Pollock 撰写，McGraw-Hill/Professional 于 2009 年出版。

## # 最终项目 - 第一部分

**简介**

**数据处理**

- 步骤 1：数据清洗与预处理
- 步骤 2：探索性数据分析
- 步骤 3：模型训练
- 步骤 4：评估与优化

在本项目中，我们将探索不同的数据预处理技术及其对模型性能的影响。目标是_compare_各种方法，并为我们的特定数据集确定最有效的方法。通过遵循这些步骤，我们旨在开发一个可靠的流程，以便在未来应用于类似的问题。

# 第四章

## 响应事件

## 关键技能与概念

- 在代码中放置事件处理器
- 理解事件处理器的语法和用法
- 在页面打开/关闭时显示消息
- 放置和移除焦点
- 调整窗口大小
- 使用 `onclick`、`ondblclick` 和数组
- 移动鼠标指针以触发事件
- 使用键盘事件处理器

正如在第三章中介绍的那样，事件是 Web 用户执行的影响网页或网页上元素的操作。

第四章研究了可能发生在网页上的各种事件类型、JavaScript 事件处理器如何响应它们，并演示了多个使用示例。本章围绕事件处理器使用的四个基本类别进行组织：

- **窗口**事件处理器处理用户对整个网页进行的打开、关闭、调整和移动等事件。
- **鼠标**事件处理器处理鼠标指针的操作，例如单击或双击元素，或将鼠标指针移入或移出元素。
- **键盘**事件处理器响应键盘上的按键操作。
- **表单**事件处理器响应用户在数据收集表单中的操作，例如选择表单元素、重置表单中的值，或将表单提交给接收者或数据库（在第五章中介绍）。

> 注意

本章中列出的并非每个事件处理器都被充分描述或演示。许多事件处理器非常相似，详细描述它们的使用将是重复的。

### 事件处理器简介

当浏览器将某件事解释为发生时，它会调用或触发一个 JavaScript 对象，称为*事件处理器*，来执行某个操作（有关 JavaScript 事件处理器的列表，请参见第三章）。例如，当你将鼠标指针移到链接或图像上时，你经常会看到一个弹出消息，告知你有关该链接或图像的性质。在这种情况下，将鼠标指针放在链接上的*事件***触发**（或激发）onmouseover *事件处理器*来显示消息。当你将鼠标指针从链接或图像上移开时，通常会触发 onmouseout 事件处理器来关闭消息。

如果你有使用 X/HTML 事件处理器的经验，你可能会疑惑为什么不能继续使用它们。你可以这样做，但 JavaScript 事件处理器相对于其 X/HTML 同类相比，最大的优点是它们可以调用其他 JavaScript 代码，如函数，从而为你的网页开辟了更广泛的交互性。X/HTML 事件处理器仅限于其属性的值。下一节描述了 X/HTML 和 JavaScript 处理事件的方式之间的这种相互关系。

#### 在代码中放置事件处理器

事件处理器是 JavaScript 的一个独特功能，因为它们可以在通常用于封装脚本的 `<script>` 标签之外使用。

你可以将 JavaScript 事件处理器作为属性添加到多个 X/HTML 标签中。哪些标签可用取决于特定的事件处理器。例如，窗口类型的事件处理器 onload 可以与 `<body>`、`<frame>`、`<frameset>`、`<iframe>`、`<img>`、`<link>` 和 `<script>` 标签一起使用，而点击类型的事件处理器如 onclick 则与数十个标签兼容。然而，大多数常见用法发生在 `<body>`、`<form>` 和 `<link>` 标签内。这种用法的一个例子是

```
<body onload="window.alert('Welcome to Past Times Antiques')\">
```

它将 JavaScript onload 事件处理器作为属性添加到 X/HTML `<body>` 标签中。

#### 理解事件处理器的语法和用法

事件处理器以如下形式添加到 X/HTML 标签中：

```
<X/HTML tagname eventhandlername="JavaScript Statement; JavaScript
Statement; ...;">
```



当将 JavaScript 用作属性时，你需要用双引号将 JavaScript 代码括起来。双引号内的文本字符串（例如警告消息框的消息文本）则使用单引号标识。

其中：

- **<** 标识 X/HTML 标签的开始
- **X/HTML 标签名** 是与事件处理程序关联的可用标签之一
- **eventhandlername** 是你正在使用的事件处理程序
- **=** 将 JavaScript 语句分配给事件发生时触发
- **"** 开头双引号开始 JavaScript 代码
- **;** 结束每个 JavaScript 语句，分隔多个语句
- **"** 结尾双引号完成 JavaScript 代码
- **>** 标识 X/HTML 标签的结束

如你所见，你可以在一个参数中将多个 JavaScript 语句串联在一起，用分号分隔。虽然这对于短语句和仅使用一次的语句来说是可以接受的，但更高效（且优雅）的方法是创建一个包含这些语句的函数，然后在网页主体中按需调用该函数。

### 使用窗口事件处理程序

在本节中，我们将使用与网页本身相关的一些事件处理程序，即窗口事件。表 4-1 列出了相关的事件处理程序。

| 事件处理程序 | 事件触发条件 |
| --- | --- |
| onabort | 图像加载中断。 |
| onblur | 焦点从元素上移开。 |
| onerror | 加载网页或图片时发生错误。 |
| onfocus | 用户将焦点放在某个元素上。 |
| onload | 网页完成加载到浏览器。 |
| onmove | 窗口或框架被移动。 |
| onresize | 窗口或框架被调整大小。 |
| onunload | 用户打开另一个网页。 |

#### 页面打开/关闭时显示消息

事件处理程序非常常见的用途是在用户首次打开网页或离开页面时显示消息。

##### onload 事件处理程序

例如，假设你正在建立一个涉及动物虐待问题的网站，并且你有一些图片可能会冒犯到某些人。是的，你可以使用标题——————————

使用上一节中描述的语法，清单 4-1 展示了使用 onload 事件处理程序创建警告/公告消息框的代码。图 4-1 在商业风格的网页上显示了该消息框。

**注意**

在第 3 章中，我们展示了在网页的 <head> 部分中将 `alert()` 方法包含在 JavaScript 语句中的示例。你可能会想知道这种用法与在 <body> 中使用 onload 事件处理程序有什么区别。关键在于控制消息框出现的时间。在前一种用法中，消息框会立即显示，在页面元素完成显示之前（这个过程非常快，以至于某些页面元素如文本可以在消息框出现之前加载）。而在 onload 事件处理程序的情况下，你可以确保所有页面元素（包括图片和其他媒体）都会在消息框出现之前显示，这或许能让用户更好地理解消息框的性质。

**清单 4-1 onload 示例**

```
<html>
  <head>
    <title>Listing 4-1</title>
  </head>
  <body onload="window.alert('The next hematology class is
scheduled for March 24th');"
  </body>
</html>
```

126 Dynamic Web Programming: A Beginner's Guide

图 4-1 使用 onload 事件处理程序在页面加载完所有元素后显示消息框。

##### onunload 事件处理程序

正如 onload 事件处理程序可用于欢迎用户或向其提供公告一样，你也可以通过在用户尝试以任何方法离开页面时显示消息框来提供某种告别：点击链接、使用"文件"|"打开"、关闭浏览器窗口等。此处展示了 onunload 事件处理程序的使用示例，代码显示在清单 4-2 中。（请注意清单中 alert 方法属性内使用了 `\'` 转义序列来显示单词"don't"中的单引号。）

## 第 4 章：响应事件

**清单 4-2 onunload 示例**

```
<html>
	<head>
		<title>Listing 4-2</title>
	</head>
	<body onunload="window.alert('And please, don\'t forget to contact your representative regarding this important legislation');">
	</body>
</html>
```

**注意**

你很容易过度使用 onunload 事件处理程序，从而惹恼许多网页浏览者。试想一下，当你的心眼已经在想象下一个网页冲浪页面的显示时，一切突然停止，你必须"杀死"这个 &^%$ 消息框才能继续。谨慎使用，否则你可能会疏远那些你试图赢得青睐的用户。

#### 放置和移除焦点

*焦点*是程序员用来描述哪个窗口或窗口中的哪个元素获得你注意力的一个花哨词汇。例如，就窗口而言，活动窗口具有焦点，而非活动窗口则没有焦点（在图 4-1 中，消息框具有焦点）。也就是说，它们是*模糊的*（另一个程序员术语，尽管焦点并非字面意义上的模糊）。另一个例子体现在数据输入表单中，准备接受用户输入的表单元素具有焦点。用户可以通过点击或使用 Tab 键切换到不同的窗口或网页元素来转移焦点，而你和其他网页程序员也可以通过使用脚本或其他编码方法来以编程方式实现。

**提示**

编程术语可以非常具体和合乎逻辑，有时也可能相当模糊和口语化。要从元素中移除焦点，即模糊它，并不意味着元素变得不可见或无法阅读，只是需要一些额外的操作（如鼠标点击）才能接受用户输入。

##### onfocus 事件处理程序

为了解如何在脚本中使用 onfocus 事件处理程序，此示例首先在 <head> 部分创建一个函数来产生我们想要的结果。然后在 <body> 部分，将调用函数的代码添加到 onfocus 事件处理程序中，这样焦点的变化就会触发我们想要的结果。清单 4-3 展示了当用户将焦点移到表单中的文本框时（表单在第 5 章中有更详细的介绍），更改其背景色的代码，如下所示。

**注意**

焦点可以通过编程方式应用于某个元素，本章后面的示例中将展示这一点。

**清单 4-3 onfocus 示例**

```
<html>
    <head>
        <title>Listing 4-3</title>
        <script language="javascript" type= "text/javascript">
//<![CDATA[
function chgTextColor(i){
document.getElementById(i).style.background="lightblue";
}
//]]>
</script>
</head>
<body>
<h2>To change an element's background color, move the focus
to it:</h2>
<form>
Occupation: <input type="text" onfocus="chgTextColor(this.id);"
id="occupation">
</form>
</body>
</html>
```

##### onblur 事件处理程序

onblur 事件处理程序在焦点从元素上移开时触发，当你想提醒用户对具有焦点的元素应该做些什么，或者想就某个元素向用户提出问题时，它会派上用场。在清单 4-4 中，我们采用之前看到的 onfocus 示例，添加第二个文本框以便从原始文本框更改焦点（通过点击文本框或按 Tab 键），然后创建一个用户必须处理才能继续的消息框，如下所示：

**清单 4-4 onblur 示例**

```
<html>
    <head>
        <title>Listing 4-4</title>
        <script language="javascript" type= "text/javascript">
            //<![CDATA[
            function chgTextColor(i){
                document.getElementById(i).style.background="lightblue";
            }
            //]]>
        </script>
    </head>
    <body>
        <h2>To get a user's attention when leaving a page element:</h2>
        <ol>
            <li>Click the <b>Occupation</b> text box and type an entry.</li>
            <li>Change focus to the <b>Duration</b> text box by clicking it or pressing TAB.</li>
        </ol>
        <form>
            <b>Occupation:</b> <input type="text" onfocus="chgTextColor(this.id);"
            id="occupation" onblur="window.alert('Hey, what did you think the color is for in the text box?');">
            <b>Duration:</b> <input type="text" onfocus="chgTextColor(this.id);"
            id="duration">
        </form>
    </body>
</html>
```

#### 调整窗口大小

onresize 事件处理程序在网页窗口被调整大小时触发并执行 JavaScript 代码。有时（在某些浏览器中，这些时候可能比其他浏览器更常发生）网页上的内容在网页窗口本身被调整大小时不会随之调整。为了让浏览器识别这一变化，你可以使用 onresize 事件处理程序强制刷新或重新加载页面。清单 4-5 展示了如何做到这一点。图 4-2 显示了显示快速刷新指示的状态栏。



 ## 清单 4-5  onresize 示例

```
<html>
    <head>
        <title>Listing 4-5</title>
    </head>
    <body onresize="window.location.href=window.location.href;">
        <h2>To reload the web page, resize the window:</h2>
        <table border="1" width="100%">
            <tr>
                <td width="41%" height="21">I am really stretching this table out in order to try and force a resize</td>
                <td width="59%" height="21">I am really stretching this table out in order to try and force a resize</td>
            </tr>
            <tr>
                <td width="41%" height="21">I am really stretching this table out in order to try and force a resize</td>
                <td width="59%" height="21">I am really stretching this table out in order to try and force a resize</td>
            </tr>
        </table>
    </body>
</html>
```

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_148_0.png)

图 4-2  状态栏中的绿色条表示页面调整大小时的快速刷新。

### 使用鼠标和键盘事件处理器

最常用的事件处理器是与用户鼠标操作和键盘输入相关的组。鼠标事件包括用户将鼠标指针简单移动、移入和移出链接、按下鼠标按钮产生单击或双击，以及按下和释放鼠标按钮等操作。表 4-2 列出了相关的事件处理器。（键盘事件将在本章后面讨论。）

在接下来的几节中，我们使用了一些鼠标事件处理器来展示它们如何在你的代码中使用。

#### 处理 onclick、ondblclick 和数组

虽然网页上的任何元素都可以响应用户的点击，但没有什么比按钮更常见的了。在第一个示例中，除了 onclick 事件处理器外，我们还添加了一些其他脚本元素以使事情更有趣。首先，设置了一个数组来*异常*地处理多个变量。接下来，创建了一个函数，在调用时显示消息。最后，将 onclick 事件处理器附加到屏幕元素上以触发操作。

##### 介绍数组

数组是一种 JavaScript 对象，允许你存储类似的变量，按数字索引，以便在脚本稍后使用。通过为值分配数字，不仅可以减少想要使用它们时的输入（一次编写，多次使用），而且还可以使用其他脚本功能（如循环）来进一步提高效率。数组的创建来自于我们创建变量和函数的方式的变形，形式如下：

```
var arrayname=new Array()
```

其中 arrayname 是你提供的唯一名称，使用标准的 JavaScript 变量和对象命名语法，而 **var**、**new** 和 **Array**() 是脚本关键字，将即将添加的变量分配到一个新数组。

你可以在创建数组时（通常在 `<head>` 部分）或之后脚本中的任何位置将变量（或参数）分配给数组。要在创建数组后分配变量，请按以下形式列出：

```
var arrayname=new Array(3)
arrayname[0]="variablename0";
arrayname[1]="variablename1";
arrayname[2]="variablename2";
```

在这种情况下，我们知道此数组将有三个参数，因此我们将数组设置为仅包含三个参数，即 **new Array(3)**。稍后在我们的脚本中，我们可以继续按原始列表的顺序添加参数，或者只需添加一行带有赋值的代码即可。或者，我们可以创建没有参数的数组，即 **new Array()**，并在需要时添加变量。作为对象，数组具有属性和方法，使它们成为脚本工具箱中非常有用的工具。

| 事件处理器 | 事件触发 |
| --- | --- |
| onclick | 元素被单击。 |
| ondblclick | 元素被双击。 |
| ondragdrop | 对象被拖放进入窗口。 |
| onmousedown | 用户按下鼠标按钮。 |
| onmousemove | 用户移动鼠标指针。 |
| onmouseout | 用户将鼠标指针从链接上移开。 |
| onmouseover | 用户将鼠标指针移到链接上。 |
| onmouseup | 用户释放鼠标按钮。 |

### 注意

数组是高效的数据存储机制，但如果使用不当，很容易失去效率。当你运行带有 100 参数数组的脚本时，100 字节的数据被放入内存堆栈中。如果你创建了一个 100 参数的数组，但 inadvertently 将最后一个参数的索引设置为 500——例如，`DogsInKennel[500] = "lassie";`——你刚刚创建了一个 500 参数的数组，在堆栈中占用了 400 个未使用的字节。因此，请确保你的索引数字是按顺序分配的。

##### 将脚本组合起来

在清单 4-6 的 `<head>` 部分中，定义了 `logic_list` 数组并用三个变量填充。定义了 `callalert` 函数，其中包含一个在被调用时显示消息框的语句。在主体中，创建了三个按钮（如下所示），它们使用 onclick 事件处理器调用 callalert 函数，并传入 logic_list 数组中的三个变量。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_151_0.png)

###### 清单 4-6  onclick 和数组示例

```
<html>
	<head>
		<title>Listing 4-6</title>
		<script language="javascript" type= "text/javascript">
			//<![CDATA[
			var logic_list= new Array(2)
			logic_list[0]="Boy, do I need a European vacation";
			logic_list[1]="If only I had the money";
			logic_list[2]="Therefore, I need to keep working to earn
				enough money for my European vacation"
			function callalert (logic_list){
				window.alert(logic_list);
			}
			//]]>
		</script>
	</head>
	<body>
		<h2>Circular logic</h2>
		<p>Click here for a solution... <input
		type="button" onclick=callalert(logic_list[0])>
		that has a small problem... <input type="button"
		onclick=callalert(logic_list[1])>
		that seems to have a solution <input type="button"
		onclick=callalert(logic_list[2])></p>
	</body>
</html>
```

#### 添加 ondblclick 事件处理器

如你所料，ondblclick 事件处理器的功能与 onclick 事件处理器完全相同，只是它需要用户多花一点力气（第二次点击！）。清单 4-7 展示了使用 ondblclick 事件处理器的示例，该示例触发一个显示一些文本的按钮。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_152_0.png)

##### 清单 4-7  ondblclick 示例

```
<html>
    <head>
        <title>Listing 4-7</title>
    </head>
    <body>
        <h2>Click the button below to see if you won a prize! (If
            a single click doesn't work, try a double-click.)</h2>
        <input type="button" ondblclick="document.write('<h2>
            Congratulations, you won!!! An ex-prince from
            Nigeria will contact you with details on how to
            claim your prize!</h2>')"
    </body>
</html>
```

### 提示

另外两个事件处理器响应鼠标点击，即 onmousedown 和 onmouseup。根据你期望用户执行的操作，这些事件处理器通常可以提供比 onclick 和 ondblclick 更少出错的结果。例如，考虑用户点击链接或按钮，但在释放鼠标按钮之前将鼠标指针移开目标的情况。（请记住点击的定义；也就是说，点击涉及按下和释放鼠标按钮。）如果你使用 onclick 事件处理器，触发器将不会触发。如果你使用 onmousedown 事件处理器，触发器将在初始按下时触发，无论按钮释放时鼠标指针在哪里。

#### 移动鼠标指针触发事件

与点击类型的事件处理器类似，有一些处理器在鼠标指针移入或移出元素时工作。最常见的是 onmouseover 和 onmouseout 的组合，它们可以用于各种目的，但最著名的是在悬停效果（rollover）中，当鼠标指针进入和离开图像时，切换几乎相同的图像，以产生动画效果，如下所示。清单 4-8 展示了在锚点标签（`<a href`）中包含这两个事件处理器的代码，以创建指向图像的链接。要创建此脚本，你需要两个具有相同尺寸的图片，因为当鼠标指针移入和移出图像时，一个会被另一个替换。代码包括以下细节：

- `<a href="http://www.someLinkToPictures.com"` 包含开始标签，如果用户点击而不是简单地将鼠标指针移入/移出图片，则创建指向图像的链接。
- `onmouseover="document.swan.src='../Art/swan-onmouseover.jpg'"` 当名为 "swan" 的图像被鼠标悬停事件触发时，显示 src 路径中的图像。
- `onmouseout="document.swan.src='../Art/swan-onmouseout.jpg'">` 当名为 "swan" 的图像被鼠标移出事件触发时（鼠标必须移出图片），显示 src 路径中的图像。
- `<img name="swan" border="0" width="307" height="230" alt="Dutch Swan" src="../Art/swan-onmouseout.jpg"></a>` 定义初始出现在页面上的图像。



第四章：响应事件 137

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_154_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_154_1.png)

Before

After

> **注意**
>
> 为使清单 4-8 和 4-9 中的代码示例有意义，我们使用了计算机上的图形文件。如果你想复制这些示例，请在适用的 src 属性中替换为你所选文件的 URL 或路径。在测试这些清单时，独立浏览器（Firefox 或 IE）比 Aptana 效果更好。

**清单 4-8** onmouseover 和 onmouseout 示例

```
<html>
  <head>
    <title>Listing 4-8</title>
  </head>
  <body>
    <a href="http://www.someLinkToPictures.com"
        onmouseover="document.swan.src='../Art/swan-onmouseover.jpg'"
        onmouseout="document.swan.src='../Art/swan-onmouseout.jpg'">
      <img name="swan" border="0" width="307" height="230" alt="Dutch Swan"
        src="../Art/swan-onmouseout.jpg"></a>
  </body>
</html>
```

注意

使用翻转效果来增强脚本交互性的方法有多种变体。清单 4-8 中显示的示例其实只是你能做的起点。网络上充满了你可以合法模仿的示例，以找到能实现你特定想要达到的效果的那个。

#### 使用键盘事件处理程序

除了接收来自鼠标的用户输入外，你还可以基于键盘按键操作来触发事件，如表 4-3 所列。这些事件中的大多数与在线数据录入表单相关，将在第五章中更详细地描述。在本章中，使用 `onkeyup` 事件处理程序来演示键盘事件处理程序。结合第三章的代码示例、本章前面的事件处理程序以及两个函数，按键释放事件被用来向用户触发随机消息。

清单 4-9 中的 `<body>` 部分除了包含一些叙述性 X/HTML 外，还执行三个操作：

- `<body onload="setfocus()">` 在触发 `onload` 事件处理程序时触发 `setfocus` 函数。
- `<input id="text1" type="text" onkeyup="presskey()">` 创建名为 `text1` 的文本框，并在用户释放按下的键时触发 `presskey` 函数。

`<head>` 部分定义了这两个函数：

- **function** `setfocus()` 封装了一个语句，当页面加载时将焦点设置到文本框（在框的左端放置闪烁的插入点，使其准备好输入）。

| 事件处理程序 | 事件触发条件 |
| :--- | :--- |
| `onkeydown` | 用户按下定义的键。 |
| `onkeypress` | 用户按下并按住定义的键。 |
| `onkeyup` | 用户释放按下的定义的键。 |

表 4-3 键盘事件处理程序

- **function** `presskey()` 封装了第三章演示的 `switch` 语句，用于在警告消息框中随机显示评论。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_156_0.png)

##### 清单 4-9 onkeyup 示例

```
<html>
    <head>
        <title>Listing 4-9</title>
        <script language="javascript" type="text/javascript">
        //<![CDATA[
        function setfocus(){
            document.all.text1.focus();
        }
        var randNum = Math.ceil(8*Math.random())
        function presskey(){
            switch (randNum) {
                case 1:
                    window.alert("Hey dude, can you press a little softer, please?");
                    break;
                case 2:
                    window.alert("Ouch, take it easy, bub");
                    break;
                case 3:
                    window.alert("C'mon, type like you mean it!");
                    break;
```

```
                case 4:
                    window.alert("Is that all you got?");
                    break;
                case 5:
                    window.alert("Try pressing in the middle of the key");
                    break;
                default:
                    window.alert("Where did you learn to spell?");
            }
        }
        //]]>
        </script>
    </head>
    <body onload="setfocus()">
        <h2>A little joke to play on your friends the next time they ask you to create a form:</h2>
        <ol>
            <li>Start typing a word in the text box below</li>
            <li>After closing the alert, refresh your screen by clicking Refresh Active Preview <img src="../art/refresh.gif"> at the bottom of the Aptana editor area. DO NOT PRESS F5. </li>
            <li>Continue until you've had enough.</li>
        </ol>
        <input id="text1" type="text" onkeyup="presskey()">
    </body>
</html>
```

## 注意

还有一些其他事件处理程序专注于表单中的操作。第五章专门讨论在表单中使用 JavaScript，其中许多事件处理程序在表 4-4 中列出，并将在该章中演示。

| 事件处理程序 | 事件触发条件 |
|---|---|
| onsubmit | 用户提交表单。 |
| onselect | 选中表单中的字段。 |
| onreset | 重置表单。 |
| onchange | 更改表单内容。 |

表 4-4 表单事件处理程序

# 第五章

## 处理与验证表单

## 关键技能与概念

- 理解表单
- 使用 X/HTML 创建表单
- 在网页上命名表单
- 使用表单的属性和方法
- 使用表单元素的属性和方法
- 理解验证
- 使用密码验证
- 创建菜单栏
- 正则表达式简介

表单是信息从用户流向网页的网络机制。它们收集信息，供网站使用。JavaScript 为表单添加自动化功能，以响应用户输入的内容。

第五章讨论表单的创建和使用、它们的方法和属性、如何验证表单中的信息，以及如何基于表单中的 JavaScript 导航元素在网站中进行导航。

### 回顾表单

本节提供关于表单以及如何使用 X/HTML 创建表单的简要入门知识。

## 注意

> 如需更全面地了解如何使用 X/HTML 创建和显示表单以及使用 CSS 进行样式设置，请参阅 Guy Hart-Davis 所著、McGraw-Hill/Professional 于 2009 年出版的《HTML, XHTML, and CSS QuickSteps, Second Edition》。

#### 理解表单

表单，就像其实纸质形式一样，是页面上包含子元素以允许用户输入信息的区域，图 5-1 显示了示例。用户

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_160_0.png)

被给予要填写的框、要选择的选项和要作的选择。在线表单相比纸质表单有若干优势：

- 在线表单易于修改且成本低廉（无需因为添加了新项目而跑到复印店去再印 1000 份订单）。
- 输入元素可以被构建以强制用户规范，即数据可以被验证是否存在（无空白字段）、是否达到一定长度（例如，信用卡和社会保障号码），或是否满足其他特定标准。
- 数据以数字形式提供，可直接输入数据库，无需手写信息数据录入所固有的时间、成本和不准确性。

创建表单有三条基本原则：保持简洁、保持简短，并清楚告知用户应该做什么（正如一位退休的海军朋友所说，使其"水手也能懂"）。

设计表单时，先在纸上草拟你的想法会有所帮助。（当然，如果你只是在将现有纸质表单数字化，那么这项任务已经完成。）首先，问自己你想从用户那里获得什么类型的信息，例如，联系信息、账户信息或订购信息。这个问题的答案将决定你需要问什么问题。例如，在征求联系信息时，询问姓名（以及格式，如全名或姓、名）、职称、地址、电子邮件地址和电话号码。确保你的文本标签清楚地向用户传达你想要什么，如图 5-1 所示。此外，查看网络上其他人用于类似目的的表单，看看是否有你需要考虑添加的字段。

接下来，考虑哪些表单元素最适合你正在收集的信息类型。每个表单元素，如表 5-1 所述，针对特定目的而设计，

| 表单元素 | JavaScript 对象名称 | 用途 |
|---|---|---|
| Button | button | 将用户引导至另一个 URL |
| Check box | checkbox | 获取是unnies/否类型的响应；可用于非互斥分组 |
| Fieldset | NA | 允许你在可见的带框区域中显示其他表单元素，可选带标题（非脚本元素） |
| Hidden field | hidden | 创建对用户不可见的字段；通常用于为服务器提交内容建立索引 |
| Password field | password | 创建显示星号（*）以屏蔽输入字符的文本框 |
| Radio (option) button | radio | 在互斥分组内获取是/否类型的响应 |
| Reset button | reset | 将表单恢复为默认设置 |
| Select box | select | 创建下拉列表框的基础设施 |
| Submit button | submit | 将表单中输入的数据发送到数据库或电子邮件地址等目的地 |
| Text area | textarea | 允许输入大量文本，通常仅受浏览器限制；适用于段落、博客和文章 |
| Text box | text | 允许较短的单行文本输入；默认通常为 20 个字符 |

表 5-1 表单元素



 ## 第5章：处理和验证表单

除了`fieldset`之外，还都有与之关联的 JavaScript 对象，允许你进行验证，这些 JavaScript 对象大多在本章后续部分使用。

最后，审查表单的整体外观和布局。将相似类型的信息归类在一起，如果你需要提供中间叙述或图片，或者觉得用户需要休息一下，可以考虑将较长的表单拆分成多个表单。（如本章稍后所示，在单个网页上设置多个表单非常容易。）

#### 使用 X/HTML 创建表单

表单，你可能已经知道，是使用两部分模型构建的。首先，你使用 X/HTML 来创建表单及其元素并将它们放置在网页上。如果你熟悉在网页上创建静态内容，这应该是你熟悉的领域。第二个阶段，即活动阶段，涉及使用 JavaScript 来访问你的表单，并通过函数和其他脚本让它们执行某些操作。

表单是通过将其元素包含在`<form></form>`标签内来创建的，从而有效地创建一个表单对象。你还可以选择使用`<fieldset></fieldset>`标签集将表单划分为可见的离散部分。清单 5-1 创建了一个使用多个表单元素的基本表单，如下所示。接下来的部分将向你展示如何在表单中使用脚本来激活它们。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_162_0.png)

##### 清单 5-1 表单示例

```
<html>
    <head>
        <title>Listing 5-1 Sample Form</title>
    </head>
    <body>
        <h2>Acme Securities</h2>
        <form name="menu" action="mailto:teacher64@isp.com">
            <fieldset>
                <legend>Request for Investment Information</legend>
                Name: <input type="text" size="24">
                Address: <input type="text"><br>
                Telephone: <input type="text">
                Email: &nbsp;&nbsp;&nbsp;&nbsp; <input type="text"><br>
                Married: Yes <input type="checkbox"> No <input type="checkbox"><p></p>
                Describe your anticipated retirement lifestyle:<br>
                <textarea name="report" rows="15" cols="50"></textarea>
                <br>Choose the investment products in which you are interested<br>
                <select name="investments" onchange="window.location=document.menu.investments.options[document.menu.investments.selectedIndex].value;">
                    <option selected value="">Investments</option>
                    <option value="stocks.html">Equities</option>
                    <option value="bonds.html">Bonds</option>
                    <option value="cds.html">CDs</option>
                </select>
                <select name="insurance" onchange="window.location=document.menu.insurance.options[document.menu.insurance.selectedIndex].value;">
                    <option selected value="">Insurance</option>
                    <option value="term.html">Term </option>
                    <option value="whole.html">Whole Life</option>
                    <option value="annuities.html">Annuities</option>
                </select>
            </fieldset>
        </form>
        <input type="submit" value="Submit Information">
        <input type="reset" value="Reset Form">
    </body>
</html>
```

### 在表单中使用 JavaScript

如上一节所述，表单对象是从`<form>`标签集创建的。要将 JavaScript 属性和方法应用于表单及其元素，必须建立一种命名约定来标识脚本语句应用于哪个表单和元素。在本节中，你将首先看到如何标识表单，然后了解它们的属性，以及与表单元素相关的属性和方法。

#### 在网页上命名表单

表单可以通过两种方式之一来标识。两种约定中更直接的一种，也是这里描述的一种，就是简单地命名表单（另一种方法在下一节中详细介绍，利用表单对象的`length`属性）。通过命名表单，你可以创建表单对象的实例。

**注意**

命名表单的缺点是，你不能使用`document.forms.length`属性来标识表单，因此无法使用表单数组来遍历表单中的每个元素。这种限制通常被能够快速知道哪个表单是哪个而无需计算特定表单索引号的便利性所抵消。当然，如果你只处理几个表单，两种方法都可以。

命名表单允许你通过唯一且有意义的名称访问网页上的表单。要为表单命名，请将 name 属性添加到`<form>`标签中，如以下语法所示：

```
<form name="formname">
```

要从脚本中的语句调用表单，请使用以下方法：

```
document.formname
```

清单 5-2 使用表单对象的`length`属性来计算表单中元素的数量（`length`属性在本章后面描述，并在其他示例和清单中使用）。注意在`<body>`部分开头的表单命名方式，以及它在`alert`语句中的调用方式，为消息框中的文本提供信息。使用 X/HTML`<input>`标签集添加了几个表单元素，如下所示。这些以及类似的元素将是我们稍后在本章中添加脚本命令的基础。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_164_0.png)

##### 清单 5-2 命名和调用表单示例

```
<html>
  <head>
    <title>Listing 5-2 Naming and Calling Forms</title>
  </head>
  <body>
    <form name="count_elements">
      Last name: <input type="text">
      First name: <input type="text"><br>
      US Citizen: Yes <input type="checkbox">
      No <input type="checkbox"><br>
      <input type="submit"><input type="reset">
    </form>
    <script language="javascript" type="text/javascript">
      //<![CDATA[
      window.alert("Do you think "+document.count_elements.length+"
        form elements on this page are enough to demonstrate this
        point?")
      //]]>
    </script>
  </body>
</html>
```

#### 表单属性和方法

表 5-2 列出了与表单对象相关的属性和方法。虽然大多数表单属性只包含与`<form>`标签中的属性相关的值（类似于上一节中描述的 name 属性），但有一些提供了更有意义的操作。这些属性以及一些表单方法将在本节中讨论。

##### action 属性

`<form>`的`action`属性指示浏览器将提交的表单数据发送到目的地，通常是 URL，服务器端的 CGI 或 PHP 处理脚本会将数据附加到数据库中。或者，表单数据可以定向到处理数据的 JavaScript 函数，或者发送到电子邮件地址。`action`属性允许你调用这些值，这里有一个示例并在清单 5-3 中编码。在该清单中，脚本有一个`write`语句，包含一个带有连接字面文本值和点语法的参数：

```
"+document.mailto.action);
```

其中`document`表示文档对象，`mailto`是表单对象名称，`action`是返回`<form>` action 属性中值的表单属性。

| JavaScript Element | Type | Description |
|---|---|---|
中文翻译表格如下：

| JavaScript 元素 | 类型 | 说明 |
|---|---|---|
| action | 属性 | 指定 CGI（通用网关接口）或 PHP 脚本的目标；值对应于`<form>` action 属性 |
| elements[] | 属性 | 指定用于访问表单中元素的数组 |
| encoding | 属性 | 指定表单中使用的编码类型；值对应于`<form>` type 属性 |
| length | 属性 | 指定表单中元素的数量；值对应于相关元素数组的长度 |
| method | 属性 | 指定提交表单时使用的方法类型；值对应于`<form>` method 属性 |
| name | 属性 | 指定表单的名称；值对应于`<form>` name 属性 |
| target | 属性 | 指定 CGI 或 PHP 输出定向到的窗口；值对应于`<form>` target 属性 |
| reset() | 方法 | 在表单中显示一个按钮，当用户单击时，将表单元素中的输入重置为默认值 |
| submit() | 方法 | 在表单中显示一个按钮，当用户单击时，将表单值发送到特定脚本 |

表 5-2 表单属性和方法

![](img/1c438577fbcf9eaf55830d0e0.3a_166_0.png)



 > 注意
在 action 属性中使用 mailto:时，用户的电子邮件客户端会打开一个新的消息表单，其中填充了表单数据。用户必须点击“发送”才能发送邮件数据。这些数据不会被保存或处理以纳入数据库或电子表格。

###### 代码清单 5-3 action 属性示例

```
<html>
    <head>
        <title>Listing 5-3 Action Property</title>
    </head>
    <body>
        <form name="mailto" method="post" enctype="text/plain" action="mailto:teacher64@isp.com">
            <fieldset>
                <legend>Vacaciones de la Primavera</legend>
                Name: <input type="text">
                Email: <input type="text" name="email_address"><br>
                Describe what you did during your spring break, in Spanish, por favor!:<br>
                <textarea name="report" rows="15" cols="50"></textarea><br>
            </fieldset>
            <input type="submit">
            <input type="reset">
        </form>
        <script language="javascript" type="text/javascript">
        //<![CDATA[
        document.write("Note: Upon clicking Submit Query you are sending your report to me at: "+document.mailto.action);
        //]]>
        </script>
    </body>
</html>
```

##### forms 数组

在本章前面，我们提到了一种除为每个表单命名之外来标识和访问表单的方法。虽然它实际上并不是表单对象的属性，但其行为方式大体相同。使用 **forms** 数组，网页上的每个表单按顺序编号，从 0 开始（有关数组的更详细说明，请参阅第 4 章）。例如，要访问页面上的第三个表单，可使用语法 `document.forms[2]`。代码清单 5-4 演示了这种用法，其中包含了表单对象的 **length** 属性。

如前所示，**length** 属性返回的值对应该表单中表单元素的数量。此示例包含三个表单，每个表单的元素数量不同。第一个表单名为 alpha（使用 name 表单属性），后两个表单未命名。在脚本中，三条 `write` 语句展示了如何使用 **forms** 数组表示法来访问表单，以及为它们命名。此外，您可以通过表单名称或其 **forms** 数组位置来访问表单，如第一条和第三条 `write` 语句所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_168_0.png)

###### 代码清单 5-4 forms 数组示例

```
<html>
	<head>
		<title>Listing 5-4 Forms Array</title>
	</head>
	<body>
		<form name="alpha">
			<fieldset>
				<legend>Hi, I'm the first form and I am called
				Alpha</legend>
				Name: <input type="text">
				Address: <input type="text"><br>
				Telephone: <input type="text">
				Email: <input type="text">
			</fieldset>
		</form>
<p>
<form>
    <fieldset>
        <legend>Hi, I'm the second form and I don't have a name</legend>
        Product Name: <input type="text">
        Model: <input type="text"><br>
        Model Number: <input type="text">
        Serialopic: <input type="text"><br>
        <input type="submit">
        <input type="reset">
    </fieldset>
</form>
<p>
<form>
    <fieldset>
        <legend>Hi, I'm the third form and I don't rate a name, either</legend>
        Are you currently employed: Yes: <input type="checkbox">
        No: <input type="checkbox"><br>
        <input type="submit">
    </fieldset>
</form>
<p>
<script language="javascript" type="text/javascript">
//<![CDATA[
document.write("In the form named Alpha, there are "+document.alpha.length+" elements.<br>");
document.write("In the second form, there are "+document.forms[1].length+" elements.<br>");
document.write("In the third form, there are "+document.forms[0].length+" elements. Oops, that's the results for the Alpha form. Actually, there are "+document.forms[2].length+" elements in the third form.");
//]]>
</script>
</body>
</html>
```

##### elements[] 属性

在表单中，每个元素可以通过名称来引用（如同表单一样，如前所述），或者通过其在 **elements[]** 数组中的位置来引用（也类似于 **forms**）。**elements[]** 数组是 **forms[]** 数组的属性。标识和访问表单元素的两种方式具有以下形式（编号从 0 开始）：

- `document.forms[0].elements[2]`，其中引用了页面上第一个表单中的第三个元素。
- `document.third_form.second_element`，其中引用了第三个表单中的第二个元素，表单和元素都已命名。

要使用 JavaScript 有意义地处理表单元素，需要使用其相关属性和方法。这些将在下一节中描述。

##### reset() 和 submit() 方法

**reset()** 和 **submit()** 方法允许您以编程方式执行“重置”和“提交”表单元素按钮的操作，即将表单清除为其默认值，以及将表单值提交到指定目的地。代码清单 5-5 和图 5-2 展示了如何通过使用 **onblur** 事件处理程序，在从表单元素移除了焦点时提交表单，从而无需用户手动执行该操作。（**reset()** 方法以类似方式工作。）提前透露一下下一节的内容，此示例使用了 `textarea` 元素的 **form** 属性，结合 **text** 关键字来标识该元素所属的表单。这种结构（`onblur="this.form.submit()"`）是为表单命名然后在脚本属性中通过名称引用它的替代方法（`onblur="document.myformname.submit()"`）。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_170_0.png)

图 5-2 表单可以通过事件处理程序操作（如点击）来提交。

> **注意**
使用 **reset()** 方法或“重置”表单元素按钮都会将表单重置为其默认值。如果要完全清除表单（包括默认值），则需要添加额外的脚本，单独标识每个元素并将其恢复到清除状态。

###### 代码清单 5-5 submit() 示例

```
<html>
    <head>
        <title>Listing 5-5 Submit Method</title>
    </head>
    <body>
        <h2>To see how this exercise works, type a few words in the
        text area, and
        then click somewhere else on the page or press TAB.</h2>
        <form action="http://www.matthewstechnology.com/essay.php">
            <fieldset>
                <legend>No second chances when filling out this essay!</legend>
                Write in the space provided a concise summary of Chapter 2:
                <textarea rows=20 cols=40 onblur="this.form.submit()"></textarea><br>
            </fieldset>
            <input type="submit" value="Click here or move the focus anywhere
            outside of the text box">
        </form>
    </body>
</html>
```

#### 处理表单元素属性和方法

在本章前面，表 5-1 列出了表单包含的表单元素。这里，表 5-3 列出了适用于每个表单元素的几个属性和方法。如您所见，这些属性/方法中有许多是多个元素共享的。

下一节提供了如何使用其中一些属性和方法与表单元素配合以实现特定结果的示例。许多未展示的属性/方法与正在演示的属性/方法行为非常相似。

##### defaultValue 属性

在文本框和文本区域中，您可以为用户显示一个默认值。如果他们更改了该值，然后决定返回到默认值，他们可能会尝试重置整个表单，这虽然有效，但会清除他们可能已输入的任何其他内容。更巧妙的处理方式是创建一种仅将元素返回其默认值的方法。代码清单 5-6 展示了创建一个函数的代码，该函数在点击“返回默认国籍”按钮时将文本框的值返回其默认值。**onclick** 事件处理程序在 `<body>` 部分进行调用。您可以亲自尝试一下，如图 5-3 所示。

| 属性/方法 | 适用元素 | 描述 |
|---|---|---|
| checked | 复选框、单选按钮 | 指示复选框是否被选中（true）或未被选中（false） |
| defaultChecked | 复选框、单选按钮 | 指示复选框是否默认被选中（true） |
| defaultValue | 文本区域、文本框 | 指示文本区域或文本框中的默认值 |
| form | 所有 | 返回父表单的名称 |
| name | 所有 | 设置或返回元素的名称 |
| options[] | 选择框 | 为选项列表中的选项提供数组 |
| selectedIndex | 选择框 | 指示选项列表中所选选项的索引值 |
| type | 所有 | 返回元素的类型值；例如，复选框的类型值为 checkbox |
| value | 除选择框外的所有 | 设置指定元素的值 |
| blur() | 除隐藏字段外的所有 | 从元素中移除焦点 |
| click() | 除隐藏字段、选择框、文本区域和文本框外的所有 | 对元素执行点击事件 |
| focus() | 除隐藏字段外的所有 | 将焦点置于元素上 |
| select() | 文本区域、文本框 | 选择文本区域或文本框 |

表 5-3 表单元素属性和方法

###### 代码清单 5-6 defaultValue 属性示例

```
<html>
  <head>
    <title>Listing 5-6 defaultValue Property</title>
    <script language="javascript" type="text/javascript">
      <![CDATA[
      function default_cit() {
        document.contact.citizen.value = document.contact.citizen
          .defaultValue;
      }
      //]]>
    </script>
  </head>
```



 ```
<body>
    <form name="contact">
        <fieldset>
            <legend>Personal Information</legend>
            Name: <input type="text" name="fullname">
            Email: <input type="text" name="email"><br>
            Citizenship: <input type="text" name="citizen"
            value="United States">
            <input type="button" value="Return to Default Citizenship"
            onclick="default_cit();">
        </fieldset>
        <input type="submit" value="Submit Personal Info">
        <input type="reset">
    </form>
</body>
</html>
```

图 5-3 你可以使用 defaultValue 属性重置某个字段，而无需重置整个表单。

##### options[] 和 value 属性

如表 5-3 所述，options[] 属性是一个数组，为下拉选择框中的所有选项提供索引，类似于下面所示的示例。使用数组索引约定（记住，编号从 0 开始，并随选项的列出顺序依次递增），你可以引用任何一个选项。在清单 5-7 中，value 属性用于访问由两个索引数组选项所引用的值，然后将其写入页面。选项列表如下所示。

###### 清单 5-7  options[] 属性示例

```
<html>
    <head>
        <title>Listing 5-7 options[] Property</title>
    </head>
    <body>
        <form name="languageform">
            <fieldset>
                <legend>Foreign Language Experience</legend>
                Do you speak a language other than English?
                Yes <input type="checkbox" name="languageyes">
                No <input type="checkbox" name="languageno"><br>
                If yes, which language do you speak best?
                <select name="languages">
                    <option selected value="Spanish">Spanish</option>
                    <option value="French">French</option>
                    <option value="Russian">Russian</option>
                    <option value="Italian">Italian</option>
                    <option value="Japanese">Japanese</option>
                    <option value="Arabic">Arabic</option>
                </select>
            </fieldset>
<input type="submit">
<input type="reset">
</form>
<p>
<script language="javascript" type="text/javascript">
//<![CDATA[
document.write("Note: If you speak both "
    +document.languageform.languages.options[2].value+"
and " +document.languageform.languages.options[5]
+value+" contact us immediately!");
//]]>
</script>
</body>
</html>
```

##### Focus 和 Blur 方法

focus() 和 blur() 方法执行的操作与第 4 章中描述的同名事件处理器相同；也就是说，focus() 通过用户鼠标点击或 Tab 键操作将焦点设置到某个字段，而 blur() 则从元素中移除焦点。两者之间的主要区别在于各自在脚本中激活的方式不同。你只需将方法包含在脚本语句的层级点语法中，类似于本章前面描述的属性。清单 5-8 中所示的示例将这两种方法用作 onclick 事件处理器的属性，产生如下所示的表单。

> **提示** 在表单中使用 focus() 方法的一个便捷方式是，在验证脚本将用户返回到某个元素以更正其输入后，将焦点放置到该表单元素中（即将光标置于该元素内）。JavaScript 验证将在下一节中更详细地描述。

###### 清单 5-8 focus() 和 blur() 方法

```
<html>
    <head>
        <title>Listing 5-8 focus() and blur() Methods</title>
    </head>
    <body>
        <form name="focusandblur">
            <fieldset>
                <legend>Focus and Blur Demonstration</legend>
                <p>Use the included buttons to learn about focus:</p>
                <input type="text" name="demo" size="20"><p>
                <input type="button" name="focus" value="Set Focus"
                    onclick="document.focusandblur.demo.focus();" />
                <input type="button" name="blur" value="Remove Focus
                    (Blur)"
                    onclick="document.focusandblur.demo.blur();" />
                <p>
            </fieldset>
        </form>
    </body>
</html>
```

### 验证表单

本章前面回顾了表单的基本功能和布局，随后的几个部分展示了如何使用 JavaScript 让表单执行某些操作。到目前为止，尚缺少的一个方面是使用 JavaScript 处理表单最常见的方式之一。本节讨论表单验证，并演示可以在表单中使用验证的各种方式。

#### 理解验证

验证是一种检查表单中用户输入是否正确的花哨说法。由于大多数输入通常都会包含在数据库中以供进一步处理或数据挖掘，因此确保 incoming 数据准确且格式正确至关重要（这有助于避免 GIGO 情况；即，垃圾进，垃圾出）。那么，是否要进行数据验证，实际上不是问题（答案是肯定的），真正的问题在于**在哪里**进行验证。提交的数据通常会被发送到服务器上运行的 CGI 或 PHP 脚本，这些脚本当然有能力处理验证任务。然而，这需要额外的计算资源，并且还要往返浏览器，这可能会降低对用户的响应速度。一种更快的处理方式是在本地执行验证，即在用户计算机上配合 Web 浏览器进行验证。

## 160 Dynamic Web Programming: A Beginner's Guide

> **注意**
并非每个浏览器都支持 JavaScript，因此客户端验证最终可能无法执行。随着时间的推移，旧版浏览器逐渐被淘汰，这个问题变得不那么相关了。然而，网络安全专家建议在客户端和服务器端都进行验证，以解决此问题及其他安全问题。客户端验证用于处理大多数常见的用户输入错误，而服务器端则具有更强大的验证功能，以防止针对性的黑客攻击。

在大多数情况下，客户端验证可以很简单，比如验证表单元素是否未留空、检查必需字符是否存在，或者访问外部数据库进行安全确认。需要验证的数据类型多种多样，因此也许发现可用功能和编码方法的最佳途径，就是留意 Web 上其他人在他们自己的表单和脚本中所做的工作。

#### 使用密码验证

客户端验证的最佳示例之一是确保用户提供的基本信息正确无误。你可以通过让用户输入两次密码来检查他们是否输入了自己认为正确的字符。（实际的密码验证以确定其是否存储在数据库中，则在服务器端处理）。清单 5-9 乍一看似乎是一个过于复杂的脚本，尤其是对于此处所示的极少输出而言，但如果将其分解为与验证脚本工作方式相关的各个部分以及可以执行验证的不同方式，它就会变得相当温和。

##### 清单 5-9 验证示例

```
<html>
  <head>
    <title>Listing 5-9 Validation</title>
    <script language="javascript" type="text/javascript">
    //<!CDATA[
      var minlength=8;
      function validateform(){
        if (document.passwordform.fullname.value=="") {
          window.alert("Please provide your full name");
```

# 第 5 章：处理和验证表单

```
document.passwordform.fullname.focus();
return false;
}
if (document.passwordform.pwd1.value==""){
window.alert("Please enter a password");
document.passwordform.pwd1.focus();
return false;
}
if (document.passwordform.pwd1.value.length < minlength){
window.alert("The password must be at least
"+minlength+" characters long");
document.passwordform.pwd1.focus();
return false;
}
if (document.passwordform.pwd1.value !=
document.passwordform.pwd2.value){
window.alert("Your two password entries are not the
same");
document.passwordform.pwd1.focus();
document.passwordform.pwd1.select();
return false
}
else {
window.alert("Thank you for submitting correct
data");
return true;
}
}
//]]>
</script>
</head>
<body>
<form name="passwordform" onsubmit="return validateform()"
action="http://myserver.com/cgi-bin/formresults.com">
<fieldset>
<legend>Validation Example</legend>
Name: <input type="text" name="fullname" size="30"><br>
Enter password: &nbsp<input type="password"
name="pwd1"><br>
Confirm password: <input type="password" name="pwd2"><br>
</fieldset>
<p>
<input type="submit" value="Submit Validated Form">
<input type="reset">
</form>
</body>
</html>
```



 ## 使用 onsubmit 事件处理程序

清单 5-9 中的 `<body>` 部分看起来与本章其他示例中的大致相同，生成了如下所示的基本简短表单。此构造中唯一有趣的方面在于 `onsubmit` 属性中的参数，即 `onsubmit="return validateform()"`。这种构造是验证工作原理的关键要素。

当用户点击"Submit Validated Form"按钮时，并非像前面的示例那样直接将表单值发送到 `action` 属性中指定的服务器，而是 `<form>` 标签集中的 `onsubmit` 事件处理程序拦截请求，调用 `validateform()` 函数（将在下一节中描述），并使用 `return` 关键字查看该函数返回 **true** 还是 **false**。如果返回 **true**，则将值发送到服务器；如果返回 **false**，则不发送任何数据。

### 剖析该函数

`validateform()` 函数由多个 `if` 语句组成，这些语句对文本框和两个密码框执行验证检查。如果 `if` 语句的条件为真，代码将继续不间断地运行。如果条件为假，则会向用户显示一个警告消息框，告知存在问题。

清单 5-9 中的前两个 `if` 语句几乎完全相同，只是检查以确保"Name"文本框和第一个密码框不为空。如果其中任何一个为空，则会显示一个警告（如下所示），向 `<body>` 部分中的 `onsubmit` 事件处理程序返回 **false**，并且不发送任何表单数据。

```
if (document.passwordform.fullname.value==""){
    window.alert("Please provide your full name");
    document.passwordform.fullname.focus();
    return false;
}
```

> **注意**
>
> 如果你希望脚本在 Firefox 中工作，请务必使用完全限定的表单字段名称——`document.passwordform.fullname`，而不仅仅是 `passwordform.fullname`。IE 可以使用简化名称，但 Firefox 不行。

如果显示了警告，请注意当用户关闭消息框时，焦点会返回到受影响的元素。

在第三个 **if** 语句中，将用户输入的密码长度与 `minlength` 变量中指定的长度进行比较。如果小于该值，则会显示警告，向 `<body>` 部分中的 `onsubmit` 事件处理程序返回 **false**，并且不发送任何表单数据。

```
if (document.passwordform.pwd1.value.length < minlength){
    window.alert("The password must be at least "+minlength+"
    characters long");
    document.passwordform.pwd1.focus();
    return false;
}
```

在第四个也是最后一个 **if** 语句中，比较两个密码框的值，以确保输入的密码与在确认框中输入的密码相同。与其他 **if** 语句一样，**false** 会生成警告，而 **true** 则继续执行脚本。

```
if (document.passwordform.pwd1.value !=
    document.passwordform.pwd2.value){
    window.alert("Your two password entries are not the same");
    document.passwordform.pwd1.focus();
    document.passwordform.pwd1.select();
    return false
}
```

> **提示**
>
> 如果你只是比较两个密码（`passwordform.pwd1 != passwordform.pwd2`）而不是它们的值，那么即使两个密码相同，也可能无法获得相等的结果，因为变量的其他属性（例如长度）可能不同。

函数中的最后操作由 **else** 和最后的 **return** 语句处理。当所有 **if** 语句都返回 **true** 时，代码处理到达 **else** 语句，该语句显示一个确认警告，向用户表明一切正常。当确认警告后，函数返回 **true**，该值被 **onsubmit** 事件处理程序接收，最终为表单数据发送到 **action** 属性中指定的 URL 开了绿灯。

```
else {
    window.alert("Thank you for submitting correct data");
    return true;
}
```

虽然这是一个有点长的示例，但相对于你可以执行的所有验证检查来说，这真的只是冰山一角。例如，除了这里检查的内容之外，你还可以通过验证是否包含大写字母、数字和特殊字符来检查密码是否为"强"密码。或者，对于电子邮件文本框，你可以检查用户是否同时包含了 @ 字符和句点（有关此示例，请参见第 9 章）。使用清单 5-9 中示例的变体，你可以构建自己的验证器来检查对表单重要的参数。

### 使用表单附加功能

表单可以用于多种用途，而 JavaScript 是使其发挥功能的关键组成部分。除了验证数据之外，脚本还可以用于计算贷款服务网页上的还款和摊销（研究 Math 对象及其属性和方法，以获取在表单中引入计算的工具）。此外，许多表单元素还可以一药二用，作为创建按钮和链接栏替代方案的方式。

本节提供了一个示例，展示如何使用 select 表单元素构建下拉列表来创建一个菜单，将用户导向网站中的其他页面，并介绍在表单中使用正则表达式。

#### 创建菜单栏

按钮栏和链接栏（如此处所示）传统上被用于允许用户在网站中导航。如果你有包含多个子类别的信息类别，你可以在下拉列表中组织链接，以整合所有这些选项。清单 5-10 提供了一个菜单栏的开始部分，该菜单栏采用了前面讨论过的几种脚本元素和技术。

##### 清单 5-10 下拉菜单示例

```
<html>
  <head>
    <title>Listing 5-10 Drop-Down Menu</title>
  </head>
  <body>
    <form name="menu">
      <fieldset>
        <legend>Acme Securities Products and Services</legend>
        <select name="investments" onchange="window.location=document.menu.investments.options[document.menu.investments.selectedIndex].value;">
          <!-- Code continues off screen -->
```

```
<option selected value="">Investments</option>
<option value="stocks.html">Equities</option>
<option value="bonds.html">Bonds</option>
<option value="cds.html">CDs</option>
</select>
<select name="insurance" onchange="window.location=document.menu.insurance.options[document.menu.insurance.selectedIndex].value;">
<option selected value="">Insurance</option>
<option value="term.html">Term </option>
<option value="whole.html">Whole Life</option>
<option value="annuities.html">Annuities</option>
</fieldset>
</form>
</body>
</html>
```

菜单栏的结构是一个包含两个 select 表单元素框的表单，其组成在本章前面已经描述过（你可以轻松添加更多 select 框来增大菜单栏的尺寸）。实现这一点的关键是捕获用户对选项的选择，并将选项的值（你希望用户被引导到的 HTML 页面）传递给事件处理程序的 window.location 属性，该属性会显示页面。

乍一看，使用 onclick 事件处理程序似乎很合理，但我们需要另一种选择，因为如果用户点击选中的值选项，我们不希望发生任何操作，而在此示例中它不是真正的选项，而是充当选项列表的类别标题。为解决此问题，使用了 onchange 事件处理程序，如下所示：

```
onchange="window.location=document.menu.investments.options[document.menu.investments.selectedIndex].value;"
```

在 window.location 属性中，每个 select 框的 options[] 数组的 selectedIndex 属性保存用户选择的索引项的值。

属性的最后一个组成部分 value 是所选选项的值，在本例中是你希望显示的网页或 URL。

这段代码中另一个有趣的方面出现在选中的值选项中：

```
<option selected value="">Insurance</option>
```

为确保选中的值是一个充当类别标题的死链接，我们为其赋予一个空值。



 ## 正则表达式简介

即便 JavaScript 已经充满了诸如关键字、对象、属性和方法之类的术语，但还有一种完整的语法世界在等着你去探索，那就是正则表达式（通常缩写为 regex 或 RegExp）。它们与前三章展示的标准表达式不同。正则表达式是一种简写约定，允许你使用文本字符串来定义字符模式，让你能把多行代码浓缩为一行。它们是检测、验证和格式化文本字符串的强大工具。

> **注意**
> 
> 对于正在学习 JavaScript 的人来说，深入探索正则表达式超出了本书的范围。这里的目的是让你了解它的存在，并能够识别它是什么。

JavaScript 解释器将正则表达式视为一个对象（具有自己的属性和方法），其形式如下：

```
re = /somepattern/;
```

其中 re 是一个变量名，用于表示由正斜杠内的正则表达式特殊字符所表示的值。一个简单的正则表达式示例，用于匹配由四个字符组成的序列号文本字符串，该序列号以一个字母开头，后跟三个数字：

```
/^\b[a-d]\d\d\d\b$/
```

其中

- `/ /` 表示一个正则表达式
- `^` 表示整个文本字符串的开头
- `\b` 表示单词边界（在此示例中并非真正需要，因为我们只有一个单词）
- `[a-d]` 匹配范围内的任意字符
- `\d` 匹配任意数字 0–9（与使用 `[0-9]` 相同）
- `$` 表示整个文本字符串的结尾

因此，在使用示例表达式的验证文本框中，*A306* 和 *c598* 将被接受，但 *1902*、*C3456* 和 *D45c* 不符合条件（*1902* 不是以 *a* 到 *d* 之间的字母开头，*C3456* 有五个字符长，而 *D45c* 在末尾包含了一个字母而不是数字）。

正则表达式将是你 JavaScript 学习过程中的自然进阶，需要多学习一些，但它提供了一种更精简的方式来创建越来越复杂的脚本。将这个概念更进一步，你可以通过使用流行的编程语言 PHP 来编写页面，从而为你的网页增添更多功能和灵活性。第 6 章将向你介绍 PHP 和 Web 编程的服务器端。

## 用 PHP 锻炼服务器

在本书的第二部分，你看到了 JavaScript 如何通过运行在客户端浏览器中的脚本激活动态 Web 元素。在第三部分，你将看到运行在服务器上的 PHP 如何提供另一层次的自动化，包括动态处理信息和决定用户接下来看到什么。

> **注意**
> 
> 尽管 JavaScript 和 PHP 有许多相似之处，但本书的这一部分是在不涉及 JavaScript 部分的情况下编写的，因此你不需要来回翻阅。同时，你可能会发现两个部分之间存在一些重复。

第 6 章讨论了 PHP 使用的基本构造以及 PHP 如何与 X/HTML 脚本绑定。变量、运算符、表达式和函数都有描述，并展示了它们的使用示例。`if-else` 和 `switch` 语句以及控制它们的条件，连同 `for`、`while` 和 `do` 循环一起进行了演示。

第 7 章回顾并演示了 PHP 的文件处理能力，描述了如何使用 PHP 文件处理来设置用户登录表单、针对文件验证登录信息，以及建立可以控制对网站受限页面访问的会话变量。还讨论了在网页之间传递数据，以及如何使用 URL、会话变量和 cookie 来实现这一点。Cookie 也在如何用于为特定用户定制页面的方面进行了讨论。

在这第三部分的开篇中，我们将提供一些关于 PHP 的背景知识，并讨论你应该运行哪些工具来处理 PHP。

### 关于 PHP

PHP 是一种用于开发动态网页的脚本语言。PHP 运行在 Web 服务器中，是*解释型*的，这意味着开发人员编写的原始人类可读脚本，每次使用时都会被转换为计算机指令。这与 C 和 Java（不是 JavaScript）等语言形成对比，后者是*编译型*的而非解释型的，意味着原始脚本会作为一次性过程转换为计算机指令，并以转换后的形式存储，因此在使用时可以立即执行，无需等待解释。虽然像 PHP 这样的解释型语言可能稍慢一些，但它们可以在使用前立即更改，这赋予了它们很大的灵活性，并使开发变得更加容易——在接下来四章的学习过程中，你会体会到这一点。

PHP 诞生于 1994 年，当时 Rasmus 为了帮助他给自己的*个人主页*添加一些动态元素而开发了它，因此得名 PHP。从那时起，它像野火一样蔓延开来，因为它功能强大且易于使用，与 HTML 集成良好，并且支持多种数据库，重要的是 MySQL。Rasmus 还将其置于公共领域，这意味着它不仅免费使用，而且任何有技能的人都可以增强它。因此，许多人参与了它的开发。如今它已发展到第五次主要修订版（PHP 5），期间有许多次修订（在撰写本文时，最新的稳定版本是 PHP 5.2.8，PHP 5.3 即将推出，PHP 6 正在开发中）。PHP 现在已经是一种完全成熟的专业脚本语言，你可以从其网站 http://www.php.net 看出。它在世界各地拥有大量的用户组（对于获取帮助很有价值——参见 PHP 网站查找你所在地区的用户组），庞大的指导和文档委员会，以及许多从事开发工作的开发人员，其中大多数是志愿者。它现在还有一个听起来更正式的，虽然是递归的，名称——"PHP：Hypertext Preprocessor"（PHP：超文本预处理器）。虽然无法获得准确的数字，但已有数百万网页使用它开发，许多专业的 Web 开发人员认为，PHP 和 MySQL 是为任何规模的网站添加数据库的最佳方式。

### PHP 所需工具

要有效地使用 PHP，你需要一个支持 PHP 脚本编写和测试的开发环境。你需要以下工具：

- **PHP 脚本编写**，在编写脚本时提供代码辅助和验证
- **在你开发计算机上的 PHP 脚本测试**
- **浏览器中的开发支持**，以帮助调试

第一部分介绍中描述并推荐了可以下载的此类工具包，包括：

- **Aptana Studio**，一个集成开发环境（IDE），默认提供对 HTML、CSS 和 JavaScript 的强大编写支持，并通过附加组件或插件支持 PHP。PHP 插件将在这里讨论。
- **XAMPP** 是 Apache Web 服务器、PHP 和 Perl 服务器以及 MySQL 数据库服务器的组合，它们都运行在你的计算机上，并模拟你将网站上传到商业 Web 主机时会看到的情况。
- **IE 6、IE 7 和 Firefox** 浏览器都是测试和调试脚本所需要的。由于很大比例的 Web 浏览人群在使用这些浏览器，因此在所有这些浏览器中测试你的网页非常重要。IE 8 在撰写本文时处于最终测试阶段，也是你用于测试的有力候选。它适用于 Windows XP 和 Windows Vista，以及 Windows 7。除了在这些浏览器上简单试用你的页面外，我们还推荐适用于 Firefox 的 Web 开发者工具栏。

如果你还没有 Aptana Studio、XAMPP、IE 6、IE 7、Firefox 和 Firefox Web 开发者工具栏，请返回第一部分介绍，按照说明下载并安装它们。本书剩余章节的讨论建议使用它们。

#### 在 Aptana 中添加 PHP

Aptana Studio 在最初下载时不包含对 PHP 的支持。幸运的是，Aptana 组织提供了一个优秀的免费 PHP 插件，它内置了用于在 Aptana Studio 中预览脚本的 PHP 服务器，以及完整的 PHP 代码辅助和格式化功能，还有一个 PHP 调试器。要下载并安装 Aptana PHP 插件：

1. 像往常一样启动 Aptana Studio；如果 **My Aptana** 未打开，请点击 **Help | Aptana Help | My Aptana**。
2. 在 My Aptana 中，点击 **Plugins**。在 Platform 标签页中，在 Aptana PHP 下，点击 **Get It**。
3. 在 Select The Features To Install 下，点击 **Site Providing Aptana PHP** 的复选框，然后点击 **Next**。
4. 点击 **I Accept The Terms**，然后点击 **Next**。最后点击 **Finish**。下载将开始。这可能需要几分钟时间。
5. 下载完成后，点击 **Install All**。安装完成后，点击 **Yes** 重新启动 Aptana Studio。

#### 在 Aptana 中设置 PHP

通过查看 Aptana 并无法明显看出 PHP 已安装，而且如果你点击 **File | New**，你将看不到 "Untitled PHP File"，除非已在你的 Aptana Studio 中打开了 PHP 项目。接下来执行此操作，让 Aptana 为本书的其余部分做好准备。

1. 在桌面上运行的 Aptana Studio 中，点击 **File | New | Project** 打开 New Project 对话框。
2. 在 New Project 对话框中，打开 **Aptana Projects**，点击 **PHP Project**，然后点击 **Next**。将同时创建项目和一个新文件 index.php。



 ## 第六章
PHP基础

### 核心技能与概念

- 在X/HTML中使用PHP
- PHP的编写与测试
- PHP基础入门
- 使用变量、常量与运算符
- 融入语句与表达式
- 创建函数
- 应用条件语句

PHP提供服务器端编程，使Web开发者能够访问托管网站的服务器及其上存储和/或运行的所有内容。其中包括存储在该服务器或其他服务器上的其他网页、购物车与计费等Web应用程序，以及用于收集和显示信息的数据库。PHP还可以访问服务器的文件系统，因此可以独立于数据库读写信息。*最重要的是*，PHP可用于构建发送到客户端的网页，从而根据客户端用户进行页面定制，例如显示特定语言或适合用户的安全级别。

本章将介绍PHP，如何将其与X/HTML集成，以及如何在不使用Aptana的情况下在您的计算机上进行编写和测试。随后本章将回顾语句、变量、运算符和函数，并展示其使用示例。最后，本章将以探索条件语句及其使用语句作结，同样附带示例。

## PHP简介

PHP是在网页中告知服务器您需要执行某些操作的一种方式。它可能是打开另一个网页、写入文件，或从数据库提取信息。无论是什么，在X/HTML页面中，开发者决定了他或她需要从服务器获取某些内容。这就是PHP的任务暴露在X/HTML页面中。因此，第一个问题是如何将PHP放入X/HTML页面，第二个问题是放入后能做什么。

### 将PHP与X/HTML集成

Aptana在第三部分导论中创建的默认PHP文件具有.php扩展名和单行PHP脚本：

```
<?php phpinfo(); ?>
```

**.php扩展名**告诉服务器该文件需要通过PHP解释器处理。`<?php ... ?>`告诉PHP解释器需要处理中间的内容，并将PHP脚本行替换为发送给浏览器的X/HTML代码，以便与服务器交互。因此，PHP的前两条规则是：

- PHP文件必须具有**.php**扩展名。
- PHP脚本必须被`<?php ... ?>`包围。

> **注意**
> 在某些情况下，您可以使用`<? ... ?>`而不包含`php`，但除非您是为内部网等受控环境开发，我们强烈建议您包含`php`，以确保脚本在所有环境中都能工作，并简单地提醒或提示查看脚本的人他们正在查看PHP。

根据这两条规则，您可以将PHP脚本放在X/HTML文件的任何位置。例如，清单6-1展示了前述PHP行放在X/HTML页面的主体中，并以.php扩展名保存。结果如图6-1所示。

> **注意**
> 图6-1展示了Firefox如何使用XAMPP（包含最新PHP服务器）显示X/HTML和PHP页面。这与Aptana显示PHP的方式略有不同，正如您在第三部分开篇所见。

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
    <title>Listing 6-1</title>
  </head>
```

## 动态Web编程：初学者指南

```
<body>
    <h1>This is an Example of PHP Embedded in X/HTML</h1>
    <p>The PHP code displays information about the PHP server.</p>
    <?php
        phpinfo();
    ?>
</body>
</html>
```

> **注意**
> 本章剩余的清单将不再包含<!DOCTYPE>和<meta>语句，以及<html>属性，以使清单更加紧凑。

### PHP的编写与测试

当您使用本书讨论的工具编写和测试PHP脚本时，您需要与Aptana一起进行编写和部分测试，并使用XAMPP中的Apache和PHP服务器以及多个浏览器进行额外的测试。要做到这一点，您需要打开Aptana PHP项目，让XAMPP能够看到它，并在项目中创建和存储PHP文件。这就是在第三部分导论中"在Aptana中设置PHP"部分所做的操作。以下是进入下一步并将PHP语句放入X/HTML页面的方法：

1. 在Aptana中点击**文件**|**新建**|**HTML文件**。在新建HTML对话框中，容器应显示您在第三部分导论中创建的项目；建议使用"Examples"。如果没有显示，点击**浏览**，选择您的项目，然后点击**完成**。

2. 在`<body>`标签之间输入清单6-1所示的语句。

3. 点击**文件**|**另存为**，输入带有.php扩展名的名称，如"Listing 6-1.php"，然后点击**确定**。

4. 点击Aptana中的某个浏览器，您应该能看到X/HTML标题和段落，以及由`phpinfo()`函数生成的PHP服务器信息。

5. 点击桌面上的**XAMPP图标**打开XAMPP控制面板。为Apache和MySQL都点击**启动**。当两个模块都显示"运行中"且启动按钮变为停止按钮时，点击**关闭**。

6. 打开浏览器（IE或Firefox）；在地址栏中输入**localhost/Listing-6-1.php**；然后按**回车键**。您应该看到图6-1所示的图像。

## 动态Web编程：初学者指南

如果您在第4步和第6步中未看到正确结果，则Aptana PHP插件或XAMPP的安装未正确完成，或者项目和文件的设置不正确。

如果在Aptana中有效而在浏览器中无效，请确保XAMPP按第5步所述运行。如果是，请查看地址栏中的内容。如果是"http://localhost/Listing 6-1.php"，则使用Windows资源管理器查看文件是否在c:\xampp\htdocs\Listing 6-1.php中（注意，Apache服务器区分大小写）。它可能在htdocs内的其他文件夹中。如果是，请在浏览器地址栏中添加该路径。

如果在浏览器中能看到显示而在Aptana中不能，则要么是插件未工作，更可能是您未正确设置项目。最好的解决方法是完全重新操作。回到第三部分导论，重新执行"在Aptana中设置PHP"下的指示。如果您认为Aptana PHP插件未工作，请返回尝试重新安装。如果已安装，Aptana会告知您。

*非常重要的是*，在进入本章后续内容之前，请确保Aptana Studio、Aptana PHP插件和XAMPP，以及两三个IE浏览器和Firefox，都能正常运行。您需要能够边学边测试您的工作。

> **提示**
> Aptana、Apache Friends和PHP都有论坛和用户组，您可以联系他们以获取解决问题的帮助。

### PHP基础

PHP有几个基本功能，既赋予其强大能力，又使其更易于使用。这些功能包括在脚本中的任何位置显示信息、以多种方式添加注释，以及一组有用的编码约定。

#### 显示信息

在调试脚本时，在脚本使用过程中显示注释或变量通常很有帮助。PHP为您提供两种方法来实现这一点，即`echo()`和`print()`函数，它们非常相似，在许多用途上是相同的。清单6-2展示了两种函数，其产生的效果如图所示。



 # 第六章：PHP 基础

##### 示例 6-2 print/echo 示例

```
<html>
    <head>
        <title>示例 6-2</title>
    </head>
    <body>
        <h1>展示 Print 和 Echo 函数</h1>
        <?php
            print "这是由 Print 生成的 <br />";
            echo "这是由 Echo 生成的";
        ?>
    </body>
</html>
```

print 和 echo 虽然被称为"函数"并包含在函数列表中，但它们与大多数函数不同：它们的参数不需要用括号括起来，不过你也可以选择使用括号。如果参数不是数字，则引号是必须的，但你可以选择使用单引号或双引号。

由于引号内的信息会被发送到浏览器进行处理，因此你可以在其中包含 X/HTML 标签，它们会被当作 X/HTML 代码行中的一样处理。示例 6-2 中的 `<br />` 就展示了这一点。这也意味着你可以在一组引号内将文本放在多行上。

print 和 echo 之间只有两个显著区别。print 在处理时会返回一个值（1），因此你可以测试它是否执行成功（本章后面会解释）。echo 不会这样做，但 echo 可以接受多个用逗号分隔的参数，而 print 只能接受一个参数。

print 和 echo 的各种使用方法如示例 6-3 所示，结果如下所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_198_0.png)

##### 示例 6-3 更多 print 和 echo 示例

```
<body> <h1>更多 Print 和 Echo 示例</h1>
<?php
    print "这是带双引号的 Print <br />";
    echo "这是带双引号的 Echo <br />";
    print '这是带单引号的 Print <br />';
    echo '这是带单引号的 Echo <br />';
    print ("这是带括号的 Print <br />");
    echo ("这是带括号的 Echo <br />");
    print "Print 参数 1<br />"; #第二个会导致错误
    echo "Echo 参数 1 ", "Echo 参数 2<br />";
    print 1234567890 ; //不带引号
    echo "<br />" , 987654321 , "<br />";
    print "这是第一行,<br />
           这是第二行, <br />
           这是第三行。";
    /* echo 和 print 基本上
       在只有一个参数时相同。 */
?>
</body>
```

> **注意**
> 在示例 6-3 中，不带引号输出数字时，`echo` 的数字不能以零开头，因为 PHP 会将其解释为八进制（以 8 为基数）数字，而八进制数字不能包含"9"，所以整个数字会被计算为"0"。

#### 注释脚本

PHP 允许你用三种方式在脚本中添加注释，如示例 6-3 所示：

- 以 # 开头的单行注释
- 以 // 开头的单行注释
- 用 /*  */ 包裹的多行注释

> **提示**
> 强烈建议你为脚本添加大量注释，以便将来更容易处理。

#### 编码规范

PHP 在规范方面相当宽松。不过在前三个示例中，你可能已经注意到几条应该添加到 PHP 规则中的约定：

- 每条 PHP 语句应以分号（`;`）结尾。唯一的例外是关闭标签 `?>` 之前的最后一条语句，它可以有分号，但不是必须的。
- 参数中的文本，即字母和数字的任意组合，也称为*字符串*，需要用引号括起来，可以是单引号（`' '`）或双引号（`" "`）。（本节后文的注释中会解释一些差异。）引号必须成对使用。
- 有效的数字，可以包含小数点，不需要用引号括起来。
- 多个参数用逗号（`, `）分隔。
- 大多数函数要求它们的参数用括号括起来。

> **提示**
> 当你调试脚本并收到"语法错误"的消息时，请检查前一行末尾是否缺少分号。这通常是问题所在。

你可能会有疑问：既然引号用于标识字符串，那么如何显示字符串中要打印或回显的引号呢？为此，PHP 使用反斜杠（`\`），这被称为*转义序列*，如下所示：

```
print "我的名字是 \"Marty\"";
```

PHP 赋予特殊用途的大多数字符都可以通过在其前面加上反斜杠来作为字面字符使用。此外，PHP 还定义了几个转义序列。以下是一些更常见的转义序列：

- `\"` 产生双引号。
- `\'` 产生单引号。
- `\\` 产生反斜杠。
- `\$` 产生美元符号。
- `\r` 产生回车符。
- `\n` 产生换行符。
- `\t` 产生制表符。

虽然单引号或双引号都可以用来括住字符串，但在某些情况下，某一种会更合适。用单引号括住字符串时，你可以在字符串中直接使用双引号字面量而无需反斜杠，如下所示。不过，使用单引号时，除 `\'` 或 `\\` 之外的转义序列会显示反斜杠而不会执行其功能。使用双引号时，所有转义序列都能正常工作。

```
print '我的名字是 "Marty"';
```

### PHP 的组成部分

PHP 虽然与 C 或 Java 相比是一种相对简单的语言，但仍然非常复杂，正如你对 PHP 这种全面的语言所期望的那样。在本节中，我们将剖析 PHP 并探索 PHP 的信息类型、语句、变量、运算符和函数。在下一部分中，我们将探讨控制结构、类和对象。

与任何语言一样，语言的每个部分都有大量元素，远非此处能够涵盖。要查看完整列表，请访问 http://www.php.net/manual/en/langref.php。

#### 信息类型

PHP 对正在处理的信息类型不如其他语言敏感，通常你不需要指定数据类型，如整数或字符串。PHP 会根据你使用它的上下文自动确定。不过，你仍然应该牢记正在处理的类型。可能的数据类型如表 6-1 所示。本章后文将对这些类型进行更详细的讨论，包括如何设置、取消设置类型，以及如何与变量和数组一起使用。

表 6-1 中的所有示例，除 NULL 外，也都是数组。有关数据类型的其他说明包括：

- 布尔值 FALSE 等同于整数 0、浮点数 0.0、空字符串或字符串 "0"、零元素数组，或 NULL。其他一切皆为 TRUE。
- 整数默认为十进制（以 10 为基数）数字。要使数字为八进制（以 8 为基数），在其前面加 0（零），例如 02 或 06。要使数字为十六进制（以 16 为基数），在其前面加 0x，例如 0x4 或 0x8。
- 非常大的整数（大于 2,147,483,647）被视为浮点数。

| 数据类型 | 名称 | 描述 | 示例 |
|---|---|---|---|
| 数组 | arr | 两个或多个数据组成的集合，可以是逗号分隔列表中前六种数据类型中的任意一种 | 98101, 'WA', 'Seattle', '123 E 3rd' |
| 布尔值 | bool | 为 "TRUE" 或 "FALSE"；不区分大小写，但通常用大写 | TRUE, FALSE |
| 浮点数 | float | 带小数点的分数；可以为负数，可以使用科学记数法 | 7.34, -21.89, 2.31e3 |
| 整数 | int | 不带小数点的整数；可以为负数 | 43, 928, -4 |
| 空值 | null | 没有任何值 | NULL |
| 字符串 | string | 一系列字符（256 个字母、数字和特殊字符之一），用单引号或双引号括起来 | "Mike", 'Seattle', "1495 W. 18th St" |
| 对象 | object | 被重复调用的脚本 | |
| 资源 | resource | 对外部元素的引用；通常与 MySQL 一起使用 | |

**表 6-1** PHP 数据类型

- 如果你将两个整数相除，除非数字能被整除，否则会得到一个浮点数。
- 由于像三分之一这样的分数会无限延续，浮点数在最后一位数字上并不精确。因此，你不应该比较两个浮点数是否相等。
- 紧跟在左引号后面的数字字符串（无论是整数还是浮点数）可以用来作为数字。例如，"18.2" 和 "4 cars" 都可以用作数字，而 "his 4 cars" 则不能。
- 数组中的特定值通过*键*来标识，键可以是整数、求值为整数的字符串、浮点数的截断整数部分、求值为整数 1 的布尔值 TRUE，或求值为整数 0 的 FALSE。

> **注意**
> 在本书中，与 PHP 手册一样，另外两种伪类型仅用于讨论："mixed" 用于前六种类型中任意一种的组合，"numbers" 类型用于整数和浮点数的组合。



 ## 变量与常量

编写 PHP 脚本时，你需要为正在处理的项目命名，以便反复引用它们。常见的可命名项目有两种类型：

- **变量**，指在脚本执行期间可以包含不同值的项目，以美元符号（$）开头，后跟你给定的名称。
- **常量**，指在脚本执行期间保持相同值的项目，按照惯例，其名称全部为大写。例如，NULL 就是一个常量。

你给变量或常量（或 PHP 中的任何其他标识符）命名的名称是区分大小写的，可以以字母 *a-z* 或 *A-Z* 或下划线（_）开头，可以是任意长度，并且可以包含字母、数字、下划线以及西欧字母表中的字符。虽然某些特殊字符可能被允许使用，但最佳实践是不使用它们。

表 6-2 列出了 PHP 中具有特定含义、不应用于变量、常量或其他标识符的关键词。

PHP 中有大量预定义常量，用于各种用途，例如真常量（M_PI = 3.1415926535898 和 M_E = 2.718281828459）、与特定函数一起使用的常量（与排序函数一起使用的 SORT_NUMERIC 和 SORT_STRING）、用于定义的常量（与日历一起使用的 CAL_GREGORIAN 和 CAL_JULIAN），以及用于格式化的常量（与日期函数一起使用的 DATE_ATOM 和 DATE_RFC822）。你可以在每个主要预定义函数部分的 PHP 手册函数参考中找到预定义常量的列表，网址为 http://www.php.net/manual/en/funcref.php。

表 6-2 PHP 关键词

| abstract | and | array | as | bool | break |
| --- | --- | --- | --- | --- | --- |
| case | catch | class | clone | const | continue |
| declare | default | do | echo | else | elseif |
| enddeclare | endfor | endforeach | endif | endswitch | endwhile |
| extends | false | final | float | for | foreach |
| function | global | goto | if | implements | int |
| interface | instanceof | namespace | new | null | object |
| or | print | private | protected | public | static |
| string | switch | throw | try | true | use |
| var | while | xor |  |  |  |

一个良好的实践是使变量和常量名称更具自描述性，同时避免与预定义名称产生任何冲突。例如，如果你要收集买家的姓名和地址，可能会倾向于使用 $name、$street 和 $city。虽然这些名称没有问题，但更好的做法是养成使用复合名称的习惯，既更具描述性，又避免使用常见名称，例如 $buyer_name、$buyer_street 和 $buyer_city。输入这些名称可能需要多花几秒钟，但它们不会与类似的名称混淆。此外，大多数程序员都非常擅长剪切和粘贴以减少打字量。

> **提示**

如果你在程序中难以找到 bug，请查看你为变量和常量分配的名称，并尝试更改任何可能与其他名称冲突的名称，例如将 $name 改为 $buyer_name。

#### 运算符

创建了变量或常量后，你会想要为其赋值。PHP 定义了多种类型的运算符来完成此操作，如表 6-3 所示。

> **注意**

另一组比较运算符，称为"三元运算符"，将在本章稍后的"控制结构"部分讨论。

如果在单个表达式中组合多个运算符，优先级顺序如下，从高到低或先执行依次为：++、--、!、~、@、*、/、%、+、-、.、<<、>>、<、<=、>、>=、<>、==、!=、===、!==、&、^、|、&&、||、=、+=、-=、=、and、xor、or。

你可以使用括号来改变优先级顺序。关于 PHP 运算符的其他说明如下：

- 取模（%）不是给出第一个数占第二个数的百分比；而是给出余数，即整除后剩余的部分。
- 等号（=）不表示"等于"，它表示"赋值"或"替换"。对于比较，例如"a 等于 b"，应使用双等号（==）。
- 如果 $a = 2 且 $b = 2.0，它们不是完全相同的，因为一个是整数，另一个是浮点数。

| 运算符类型 | 名称 | 示例 | 说明 |
| --- | --- | --- | --- |
| **算术** | | | 执行算术运算 |
| + | 加 | $a + $b | 和 |
| - | 减 | $a - $b | 差 |
| * | 乘 | $a * $b | 积 |
| / | 除 | $a / $b | 商 |
| % | 取模 | $a % $b | 余数 |
| **赋值** | | | 用一个值替换另一个值 |
| = | 赋值 | $a = 7; | 将 $a 设为 7 |
| += | 递增 | $a = 7;<br>$a += 2;<br>返回 9 | 将 $a 增加 2 |
| .= | 连接 | $a = "Joe ";<br>$a .= "Blow";<br>返回 "Joe Blow" | 将字符串添加到现有字符串 |
| []= | 追加 | $array [] = $something | 将 $something 追加到数组末尾 |
| **位运算** | | | 开启或关闭整数中的特定位 |
| & | 与 | $a & $b | 设置 $a 和 $b 中都有的位 |
| \| | 或 | $a \| $b | 设置 $a 或 $b 中有的位 |
| ^ | 异或 | $a ^ $b | 设置 $a 或 $b 中有的位，但不同时设置 |
| ~ | 非 | ~$a | 不设置 $a 中的位 |
| << | 左移 | $a << $b | 将 $a 的位向左移动 $b 步（每步乘以 2） |
| >> | 右移 | $a >> $b | 将 $a 的位向右移动 $b 步（每步除以 2） |
| **比较** | | | 比较两个值 |
| == | 等于 | $a == $b | 如果 $a 等于 $b 则返回 TRUE |
| === | 全等 | $a === $b | 如果 $a 与 $b 全等则返回 TRUE |
| != 或 <> | 不等于 | $a != $b 或<br>$a <> $b | 如果 $a 不等于 $b 则返回 TRUE |
| !== | 不全等 | $a !== $b | 如果 $a 与 $b 不全等则返回 TRUE |
| < | 小于 | $a < $b | 如果 $a 小于 $b 则返回 TRUE |
| > | 大于 | $a > $b | 如果 $a 大于 $b 则返回 TRUE |

| 运算符类型 | 名称 | 示例 | 说明 |
| --- | --- | --- | --- |
| <= | 小于或等于 | $a <= $b | 如果 $a 小于或等于 $b 则返回 TRUE |
| >= | 大于或等于 | $a >= $b | 如果 $a 大于或等于 $b 则返回 TRUE |
| **递增** | | | 将值改变 1 |
| ++ | 递增 | ++$a $a++ | 将 $a 加 1 并返回 $a 返回 $a，然后将 $a 加 1 |
| -- | 递减 | --$a $a-- | 将 $a 减 1 并返回 $a 返回 $a，然后将 $a 减 1 |
| **逻辑** | | | 逻辑结果 |
| and && | 与 | $a and $b | 如果 $a 和 $b 都为 TRUE 则返回 TRUE |
| or \|\| | 或 | $a or $b | 如果 $a 或 $b 为 TRUE 则返回 TRUE |
| xor | 异或 | $a xor $b | 如果 $a 或 $b 为 TRUE，但非两者都为 TRUE 则返回 TRUE |
| ! | 非 | !$a | 如果 $a 不为 TRUE 则返回 TRUE |
| **其他** | | | |
| @ | 错误抑制 | @my_function() | 禁用表达式中的错误显示 |
| ` ` | 执行 | ` date ` | 执行反引号内的内容（这些不是单引号），类似 DOS 命令 |

表 6-3 PHP 运算符（续）

清单 6-4 展示了 PHP 变量和运算符的使用示例。此脚本返回的结果显示在接下来的插图页面中。

> **注意**

以下脚本中的变量名，例如 $a 或 $b，在使用 echo 或 print 显示时会被替换为变量中包含的值，除非你通过在变量前添加反斜杠（\）来转义它们（将它们视为字面字符）。这在双引号内以及任何引号外都适用，称为插值。如果使用单引号括起变量名，则显示名称而非内容。

##### 清单 6-4 变量和运算符示例

```
<html>
    <head>
        <title>Listing 6-4</title>
    </head>
    <body>
        <h1>Example of Variables and Operators</h1>
        <?php
        //Math
        $a = 2; $b = 5;
        echo "Add $a and $b to get ", $a + $b, "<br />";
        echo "Multiply $a by $b to get ", $a * $b, "<br />";
        echo "Divide $a by $b to get ", $a / $b, "<br />";
        echo "Modulus $a by $b to get ", $a % $b, "<br />";
        //Increment and Concatenate
        $a = 7;
        echo "Increment $a by 2 to get ", $a += 2, "<br />";
        echo "Increment $a by 1 to get ", ++$a, "<br />";
        $first_name = "Mary "; $last_name = "Smith";
        echo "Concatenate $first_name and $last_name to get ",
            $first_name . $last_name, "<br />";
        //Comparison
        $a = "2"; $b = 2.0; $c = 4; $d = $a == $b; $e = $a === $b;
        echo "Test if $a and $b are equal (True = 1)  ", $a == $b,
            "<br />";
        echo "Test if $a and $b are identical (True = 1)  ",
            $a === $b, "<br />";
```



 ```
echo "Test if $a is less than or equal to $c (True = 1)  ",
    $a <= $c, "<br />";
//Logical
echo "Test if \$d and \$e are TRUE (True = 1)  ", $d and $e,
    "<br />";
echo "Test if \$d or \$e are TRUE (True = 1)  ", $d or $e,
    "<br />";
//Execute
echo `date` ;
?>
</body>
</html>
```

#### 语句与表达式

PHP 脚本包含注释或语句。语句是指位于分号之间或 PHP 开始和结束标签之间的任何内容。通常，语句是结束于分号的单行代码，但您可以在单行上包含多个语句，也可以有跨越多行的语句。大多数语句包含一个或多个表达式，但也有一些仅为单个关键字，例如 **break** 或 **else**。

表达式是指具有值或计算结果为值的任何内容。值是可以赋值给变量的任何内容，因此值可以是任何数据类型：整数、浮点数、字符串、布尔值、数组或对象。虽然 NULL 数据类型表示无值，但在此讨论中它仍被视为一个值。

表达式可以包含表达式，换句话说，表达式是作为构建块来构建其他表达式的。例如，`$a = 2` 包含三个表达式：`2`、`$a` 和 `$a = 2`。

#### 函数

函数是一段执行某项操作的脚本，可以在更大的脚本中反复调用。一些内部函数已经存在，还有一些是用户自定义的函数。有些函数需要*参数*，即传递给函数的值，函数使用它们来计算返回值。其他函数则在被调用时直接返回值。

##### 内部函数

您可以使用大量内部或预定义的 PHP 函数来完成许多不同的任务。要探索完整的 PHP 函数集，请参阅在线 PHP 手册函数参考：http://www.php.net/manual/en/funcoref.php。

以下各节介绍了一些在特定类别中使用频率较高的内部函数作为示例。再次说明，这些只是可用函数中的一小部分。

**数组函数** 数组函数提供了多种处理数组的方式。表 6-4 展示了其中几个函数，清单 6-5 演示了它们的使用。

###### 清单 6-5 数组函数示例

```
<html>
    <head>
        <title>Listing 6-5</title>
    </head>
    <body>
        <h1>Examples of Array Functions</h1>
        <?php
            $nameEntry = array(
                "name" => "Jon Doe", "email" => "jon@zxy.com",
                "phone" => "x456", );
            echo "Number of elements is: ", count($nameEntry), "<br />";
            print_r($nameEntry);
            $output = print_r($nameEntry, true);
            echo "<br /> Output is: ", $output, "<bresian";
            echo "Name is: ", $nameEntry [name], "<br />";
            echo "Email is: ", $nameEntry [email], "<br />";
            echo "Phone is: ", $nameEntry [phone], "<br />";
        ?>
    </body>
</html>
```

###### 表 6-4 几个数组函数

| 函数 | 描述 | 说明 |
| :--- | :--- | :--- |
| array () | 构建一个参数数组 | 参数是一系列由逗号分隔的 key => value 语句。键可以是整数或字符串。值可以是任何类型。 |
| count () | 计算数组中的元素数量 | 参数为数组名称；元素即为键/值对的数量。 |
| print_r () | 以可读形式打印变量（包括数组） | 参数为变量（或数组）名称。如果可选的第二个参数 = TRUE，则变量或数组的内容将被返回供另一个变量使用，而不是被打印出来。 |

**日期/时间函数** 日期和时间函数提供对运行脚本的服务器当前日期和时间的访问和操作。表 6-5 展示了其中几个函数，清单 6-6 演示了它们的使用，如下所示：

###### 表 6-5 几个日期和时间函数

| 函数 | 描述 | 说明 |
| :--- | :--- | :--- |
| date () | 格式化的日期和时间字符串 | 需要一个格式字符串，如果不需要本地时间，还可以选择性地提供一个时间戳 |
| getdate () | 日期和时间组成的数组 | 如果不需要本地时间，可以接受可选的时间戳 |
| time () | 当前 "Unix" 时间戳 | 返回自 1970-1-1 00:00:00 GMT 到当前服务器时刻的秒数 |

###### 清单 6-6 日期和时间函数示例

```
<html>
    <head>
        <title>Listaing 6-6</title>
    </head>
    <body>
        <h1>Date and Time Examples</h1>
        <?php
            echo date(DATE_RFC822), "<br />";
            $date_format = "l, F jS, Y";
            echo date($date_format), "<br />";
            echo date("l, F jS, Y"), "<br />";
            print_r(getdate());
            $date_array = getdate();
            echo "<br />Today is: ", $date_array[weekday],
                ", ", $date_array[month], " ", $date_array[mday],
                ", ", $date_array[year], "<br />";
            echo "Today's timestamp is: ", time(), "<br />";
                //Seconds since 1-1-1970
            $twoweeks = (14 * 24 * 60 * 60);
                //seconds in 2 weeks
            $twoweeksFrNow = time() + $twoweeks;
            echo "Two weeks from today is: ",
                date("l, F jS, Y", $twoweeksFrNow), "<br />";
        ?>
    </body>
</html>
```

> **提示**
> date() 函数的所有格式化代码，如清单 6-6 中使用的那些，可在 http://www.php.net/manual/en/function.date.php 查看。

**数学函数** 数学函数允许您执行数学运算。表 6-6 展示了其中一些函数，清单 6-7 演示了它们的使用。

###### 表 6-6 几个数学函数

| 函数 | 描述 | 说明 |
| :--- | :--- | :--- |
| dechex() | 将十进制整数转换为十六进制数 | 返回表示十六进制数的字符串。 |
| exp() | 计算 e 的幂 | 返回 e 的浮点数次幂的浮点数。 |
| log() | 计算自然对数 | 返回浮点数的对数的浮点数。可选参数可以指定除默认的 e 以外的底数。 |
| rand() | 生成随机数 | 无参数时生成 0 到 32,768 之间的整数。可选地，可以指定最小和最大整数，用逗号分隔。 |
| round() | 将数字四舍五入到指定的小数位数 | 对浮点数进行算术四舍五入后返回浮点数。可选地，可以指定精度或小数位数。 |

###### 清单 6-7 数学函数示例

```
<html>
<head>
    <title>Listing 6-7</title>
</head>
<body>
    <h1>Examples of Math Functions</h1>
    <?php
        echo "The hex equivalent of 1492 is: ", dechex(1492), "<br />";
        echo "The power of e to 214 is: ", exp(214), "<br />";
        echo "The logarithm of 55.86 is: ", log(55.86), "<br />";
        echo "A random number between 11 & 99 is: ", rand(11,99), "<br />";
        echo "567.12534 rounded to two places is: ", round(567.12534, 2), "<br />";
    ?>
</body>
</html>
```

**字符串函数** 字符串函数允许您处理字符串。您已经见过两个字符串函数，echo() 和 print()。表 6-7 展示了其他几个函数，清单 6-8 演示了它们的使用，如下所示

> **注意**
> count_chars() 函数有五种模式（0 到 4）。模式 0 到 2 是返回计数的数组：模式 0 返回所有 255 个字符的计数；模式 1 返回所有存在字符的计数；模式 2 返回所有不存在字符的计数。模式 3 和 4 是字符串：模式 3 列出所有存在的唯一字符；模式 4 列出所有不存在的字符。

| 函数 | 描述 | 说明 |
| :--- | :--- | :--- |
| count_chars() | 统计字符串中字符出现的次数 | 参数为字符串和可选的模式，该模式决定返回数组还是字符串，以及要计数的内容。参见上面的注释。 |
| implode() 或 join() | 将数组元素连接形成字符串 | 参数为数组和可选的连接字符，默认为空格，放置在元素之间。 |
| is_string() | 确定值是否为字符串 | 参数为变量，如果该变量是字符串则返回 TRUE。 |
| ltrim() | 通过移除左侧空白和指定字符形成的字符串 | 参数为字符串和可选的要移除的字符列表。未指定列表时，移除空格、制表符、回车符、换行符和垂直制表符。 |
| number_format() | 通过用小数点和千位分隔符格式化数字形成的字符串 | 浮点数格式化为可选的整数位小数位数（1、2 或 4，不是 3）。可选地，可以指定小数点和千位分隔符字符。 |
| str_split() | 将字符串拆分为数组元素 | 参数为字符串和可选的每个元素中的字符数，默认为 1。 |
| strval() | 将数字变量转换为字符串 | 参数必须是整数或浮点数。 |



 ## 代码清单 6-8 字符串函数示例

```html
<html>
    <head>
        <title>Listing 6-8</title>
    </head>
    <body>
        <h1>Examples of String Functions</h1>
        <?php
            $textString = "Now is the time!";
            $textArray = count_chars($textString, 1);
            print_r($textArray);
            $nameEntry = array(
                "name" => "Jon Doe", "email" => "jon@zxy.com",
                "phone" => "x456",
            );
            echo "<br />", implode(" ",$nameEntry), "<br />";
            $aLongString = "         Now is the time";
            echo ltrim($aLongString), "<br />";
            echo "The formatting of 543216789.6386 is: ",
                number_format(543216789.6386, 2), "<r />";
            print_r(str_split(543216789.6386, 3)) ;
            echo "<br />", $newString, "  is a string? (True = 1) ",
                is_string($newString) , "<br />";
        ?>
    </body>
</html>
```

> **注意**
>
> 在本章后面的"控制结构"一节中，你会看到 `count_chars()` 更好的显示效果。

##### 用户自定义函数

编写 PHP 脚本时，你经常会发现想要重复使用相同的代码。你可以简单地将代码复制到所有需要使用的地方，但如果你想修改这段代码，就必须在复制过的所有地方都进行修改。解决这个问题的方法是创建一个包含你想要重复使用的代码的函数，然后在需要使用的地方调用该函数即可。函数还能让你将代码分段或隔离，使其更易于调试和维护。

使用函数还有更重要的原因。到目前为止，本章中所有 PHP 代码都是在页面加载时运行或执行的，但*在*页面显示之后执行，这与某些 JavaScript 在页面显示*之前*执行形成对比。如果你不想在页面加载时执行 PHP 脚本，可以创建一个函数，将其放在 X/HTML 头部之上，这样它在被调用之前不会运行。

与预定义或内部函数一样，用户自定义函数（以下简称为"用户函数"）可以有选择地接收传递给它们的参数，并在执行后返回一个值。一旦用户函数被定义，就可以像内部函数一样被*调用*或使用。函数本身可以使用 PHP 的所有特性执行任何操作，包括调用其他函数，甚至调用自身来创建递归函数。（你需要限制递归函数，确保它们不会无限递归，否则会产生错误。一个好的经验法则是将递归限制在不超过 100 次。）

用户函数使用 **function** 和 **return** 关键字按以下形式定义：

```
function name($argument1, $argument2,...)
{
    [any PHP statements];
    return $returnValue;
}
```

函数名称的命名规则与变量、常量和其他标签相同。它区分大小写，可以以字母 *a–z* 或 *A–Z* 或下划线 (_) 开头，可以是任意长度，并且可以包含字母、数字、下划线和西欧字母表中的字符。

代码清单 6-9 展示了用户函数的一个示例，其结果如下所示。本章及后续章节中还会展示更多示例。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_215_0.png)

###### 代码清单 6-9 用户自定义函数

```html
<html>
<head>
<title>Listing 6-9</title>
</head>
<body>
<h1>User-Defined Function</h1>
<?php
function tokm($miles)
{
    $km = $miles * 1.6;
    return $km ;
}

echo "<b>Directions:</b>", "<br />", "From the highway
    turn right,"
    , "<br />",
    "go 2.4 miles or ", tokm(2.4), " km, turn left", "<br />",
    "go 1.3 miles or ", tokm(1.3), " km, turn right", "<br />",
    "go .9 miles or ", tokm(.9), " km, you're there.", "<br />";
?>
</body>
</html>
```

### 控制结构

本章到目前为止的脚本都是从第一条语句到最后一条语句不间断或不变向地执行，除了代码清单 6-9 中重复的函数调用。通常你会想要判断脚本应该走这条路还是那条路，或者返回去重新执行某段代码。这就是控制结构的目的，包括 if/else 语句；while、do-while 和 for 语句；以及 switch 语句等。

#### if/else 语句

if/else 语句是 PHP 中主要的决策构造。它允许你指定：如果某个表达式为 TRUE，则执行一组语句，否则执行另一组语句。其形式如下：

```
if (conditional expression) {
    statements executed if TRUE;
}
```

```
else {
    statements executed if FALSE;
}
```

else 语句组是可选的，只有当条件表达式为 FALSE 时你想执行其他操作时才需要。此外，你还可以使用 elseif 嵌套 if/else 语句，如下所示：

```
if (conditional expression) {
    statements executed if TRUE;
}
elseif (second conditional expression) {
    statements executed if second conditional is TRUE;
}
else {
    statements executed if second conditional is FALSE;
}
```

在所有情况下，条件表达式必须结果为布尔值 TRUE 或 FALSE（1 或 0）。如果某个变量只是存在——即，它被定义为包含除 NULL、FALSE 或 0 之外的某个值——那么它就是 TRUE。

> **提示**
>
> 如果你将变量定义为包含 NULL、TRUE 或 FALSE 等常量，必须记住*不要*将其放在引号中。

许多条件表达式都是比较，测试两个元素是否相等、大于或小于。记住，在 PHP 中测试相等性时，必须使用双等号 (==)，而不是单等号，后者表示赋值。

代码清单 6-10 展示了 if/else 语句的几个示例，其结果如下所示。后续章节中还会展示更多示例。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_217_0.png)

##### 代码清单 6-10 if/else 语句

```html
<html>
<head>
    <title>Listing 6-10</title>
</head>
<body>
    <h1>If/Else Examples</h1>
    <?php
    if ($a) {
        echo "True", "<br />";
    }
    else {
        echo "False", "<br />";
    }
    $a = "Something";
    if ($a) {
        echo "True", "<br />";
    }
    else {
        echo "False", "<br />";
    }
    $state = "CA";
    if ($state == "WA" ) {
        echo "Pacific Northwest", "<br />";
    }
    elseif ($state == "OR") {
        echo "Pacific Northwest", "<br />";
    }
    else {
        echo "Somewhere Else", "<br />";
    }
    ?>
</body>
</html>
```

#### 三元运算符

在 PHP 脚本中进行 if/else 决策的简写方法是使用三元运算符 (?:)，其中 ? 替代 if 测试并跟在条件表达式之后，而 : 替代 else。以下语句产生与其后所示的 if 语句相同的结果。

```
echo ($a) ? "True" : "False", "<br />";
if ($a) {
    echo "True", "<br />";
}
else {
    echo "False", "<br />";
}
```

不建议将多个 `if` 语句像使用 `elseif` 那样用三元运算符连接，因为 PHP 对此行为未定义。

> **提示**
>
> 如果你想使用多个三元运算符，请使用括号。

#### while 和 do-while 语句

`while` 和 `do-while` 语句是循环构造，允许你重复执行一段代码，直到条件表达式不再为 TRUE。`while` 语句是这组语句的基础，采用以下两种形式之一：

```
while (conditional expression) {
    statements executed while TRUE;
}
```

```
while (conditional expression) :
    statements executed while TRUE;
endwhile;
```

`do-while` 语句与 `while` 语句类似，区别在于条件表达式在语句末尾而不是开头。`do-while` 语句的形式如下：

```
do {
    statements executed while TRUE;
}
while (conditional expression);
```

最常见的条件表达式是将计数器与某个结束值进行比较。换句话说，初始化一个计数器，然后循环执行一些语句，每次循环递增计数器，直到计数器超过结束值。代码清单 6-11 展示了 `while` 和 `do-while` 的示例，结果如下所示。你可以看到，在这种情况下 `while` 和 `do-while` 没有区别。

> **注意**
>
> `do-while` 中的代码保证至少执行一次，因为条件在第一次执行后才检查。如果条件立即计算为 false，`while` 语句可能一次都不会执行。



 清单 6-11 while 和 do-while 示例

```
<html>
    <head>
        <title>Listing 6-11</title>
    </head>
    <body>
        <h1>While and Do-While Examples</h1>
        <?php
            echo "<b>Partial Character Set with While</b><br />";
            $i = 33;
            while ($i <= 41) {
                echo "Character # ", $i , " is ", chr($i);
                echo "&nbsp; &nbsp; &nbsp; Character # ", $i + 1 ,
                    " is ", chr($i + 1);
                echo "&nbsp; &nbsp; &nbsp; Character # ", $i + 2 ,
                    " is ", chr($i + 2), "<br />";
                $i = $i + 3;
            }
            echo "<br /> <br /> <b>Partial Character Set with Do-While</b><br />";
            $i = 33;
            do {
                echo "Character # ", $i , " is ", chr($i);
                echo "&nbsp; &nbsp; &nbsp; Character # ", $i + 1 ,
                    " is ", chr($i + 1);
                echo "&nbsp; &nbsp; &nbsp; Character # ", $i + 2 ,
                    " is ", chr($i + 2), "<br />";
                $i = $i + 3;
            }
            while ($i <= 41);
        ?>
    </body>
</html>
```

#### for 和 foreach 语句

for 和 foreach 语句是额外的循环结构。for 语句与其他语言中的对应结构类似，将计数器的初始化、条件限制和递增都放在 for 后面的一系列表达式中。for 语句可以采用以下两种形式之一：

```
for (initializing expression; conditional expression; incrementing expression)
    {
        statements executed while TRUE;
    }
```

```
for (initializing expression; conditional expression; incrementing expression):
    statements executed while TRUE;
endfor;
```

在其基本形式中，for 表达式可能是 for ($i = 1; $i <= 5; $i++)，其中 $i++ 在使用 $i 后对其进行递增。如果其中任何表达式在脚本的其他地方已处理，则可以在 for 表达式中将它们留空，其最小形式为 for ( ; ; )。

foreach 语句用于遍历数组，不能用于任何其他类型的变量。它可以显示数组中每个元素的值，或者 alternatively 显示数组中每个元素的键和值。因此，它具有以下两种形式之一：

```
foreach ($array as $value) {
        statements executed for each element;
    }
```

```
foreach ($array as $key => $value) {
        statements executed for each element;
    }
```

当你开始执行 foreach 语句时，数组指针会自动重置到第一个元素。当你结束执行 foreach 语句时，数组指针停留在最后一个元素上，其值仍由 $value 包含。你可以使用 unset($value) 来移除它，并使用 reset($array) 来重置数组指针。

清单 6-12 展示了 for 和 foreach 语句的示例，结果如下所示。for 语句可以以非常类似于 while 的方式使用。foreach 语句使 count_char 数组的显示更加易读（与清单 6-8 比较）。

**清单 6-12** for 和 foreach 示例

```
<html>
    <head>
        <title>Listing 6-12</title>
    </head>
    <body>
        <h1>For and Foreach Examples</h1>
        <?php
            echo "<b>Partial Character Set with For</b><br />";
            for ($i = 33; $i <= 35; $i++) {
                echo "Character # ", $i , " is ", chr($i), "<br />";
            }
            echo "<br /> <br /> <b>Count_Chars with Foreach</b><br />";
            $textString = "Now is the time!";
            $textArray = count_chars($textString, 1);
            foreach ($textArray as $key => $val) {
                echo "The character \"", chr($key) , "\" occurs ",
                    $val, " times. <br />";
            }
        ?>
    </body>
</html>
```

#### switch 语句

switch 语句类似于一系列 if/elseif 语句。switch 语句用于将单个变量与多个不同的值进行比较，并根据值执行不同的操作。switch 还使用三个额外的关键字：case、break 和 default，形式如下：

```
switch ($avariable) {
    case 1:
        statements executed while TRUE;
        break;
    case 2:
        statements executed while TRUE;
        break;
    case 3:
        statements executed while TRUE;
        break;
    default:
        statements executed while all are FALSE;
}
```

switch 语句中的每个 case 表达式将 switch 变量与 case 值进行比较，case 值可以是字符串；如果相等，则执行 case 表达式后面的语句，然后 break 表达式将脚本的流程发送到 switch 结束大括号后的第一个语句。如果所有 case 表达式都不成功，则执行 default 表达式后面的语句，脚本的流程退出 switch 语句。清单 6-13 演示了这是如何工作的，提供了以下结果：

清单 6-13 switch 语句示例

```
<html>
    <head>
        <title>Listing 6-13</title>
    </head>
    <body>
        <h1>Switch Statement Example</h1>
        <p><b>The Computer Wizard!</b></p>
        <p>Ask a Yes/No question and click Refresh.</p>
        <?php
        $randNum = rand(1,5);
        switch ($randNum) {
        case 1:
            echo "Definitely Yes!";
            break;
        case 2:
            echo "Probably Yes!";
            break;
        case 3:
            echo "Definitely Maybe!";
            break;
        case 4:
            echo "Probably No!";
            break;
        case 5:
            echo "Definitely No!";
            break;
        default:
            echo $randNum, "<br />"; //Display the number
            echo "Computer Malfunction, Try Again";
        }
        ?>
    </body>
</html>
```

在接下来的章节中，你将看到如何将 PHP 的众多部分组合成一个实际有用的脚本，例如在网页之间或会话之间传递数据，或者在服务器上读写文件以创建留言簿，或者验证用户身份。

除了在线 PHP 手册之外，还有两本关于 PHP 的优秀书籍：*PHP: The Complete Reference*，由 Steven Holzner 撰写，McGraw-Hill/Professional 2008 年出版；以及 *How to Do Everything with PHP & MySQL*，由 Vikram Vaswani 撰写，McGraw-Hill/Professional 2005 年出版。

# 第 7 章

## 单独使用 PHP

## 关键技能与概念

- 理解基本文件函数
- 考虑额外的文件函数
- 使用会话变量
- 添加 Cookie
- 建立服务器变量
- 完成索引脚本
- 构建注册脚本
- 创建登录脚本
- 建立站点页面

PHP 通常被认为仅仅是与 MySQL 数据库工作的机制。然而，它是一种功能齐全的编程语言，不仅具有你在第 6 章中看到的所有功能，还包括强大的文件处理工具、浏览器信息功能以及创建和使用 cookie 与会话变量的技术。本章探讨了 PHP 的这些强大功能，并在此过程中描述了如何使用 PHP 文件管理来设置用户登录表单、验证登录信息、确定浏览器类型以及建立可以保护对网站访问的会话变量。还讨论了使用会话变量和 cookie 在网页之间传递数据。

> **提示**
> 将 PHP 手册和 PHP 函数参考添加为浏览器的书签或收藏夹是很有用的，这样你可以快速查阅它们。手册位于 http://www.php.net/manual/en/，函数参考位于 http://www.php.net/manual/en/funcref.php。

### PHP 文件和目录管理

服务器端编程的主要优势之一是你可以在服务器的存储设备上读写信息。PHP 拥有一组广泛的函数，不仅可以让你读写文件，还可以更改文件属性；复制、移动和删除



文件；操作目录；等等。在本节中，我们将讨论并简要演示一些更重要的文件函数。在本章的最后一大节中，我们将展示如何使用文件命令创建用户认证系统。

#### 基本文件函数

基本的 PHP 文件处理包含以下要素：

- 使用 `fopen()` 函数在 PHP 与文件之间建立文件连接，或称为*文件指针*（也叫“句柄”）。
- 使用 `fwrite()` 函数将数据字符串写入已打开的文件。
- 使用 `fread()` 函数从已打开的文件中读取一定数量的字节到字符串中。
- 使用 `fclose()` 函数终止文件指针。

表 7-1 提供了有关这些基本文件函数的更多信息，清单 7-1 简要演示了这些函数的使用方法。

> **提示**
如果你将文件指针变量命名为 `$fp`，它将与 Aptana 建议的文件函数所需的文件指针参数相匹配。

| 函数 | 说明 | 解释与参数 |
|---|---|---|
| `fclose()` | 终止文件指针 | 唯一的参数是使用 `fopen()` 创建的文件指针。成功关闭则返回 `TRUE`，否则返回 `FALSE`。 |
| `fopen()` | 连接文件并创建文件指针 | 必需的参数是带有路径和文件名的字符串，以及带有模式的字符串（模式列表见表 7-2）。返回可用于其他文件函数的文件指针，或返回 `FALSE`。 |
| `fread()` | 将一定数量的字节读入字符串 | 必需的参数是使用 `fopen()` 创建的文件指针，以及要读取的字节数。返回包含读取数据的字符串，或返回 `FALSE`。 |
| `fwrite()` | 将字符串写入文件 | 必需的参数是使用 `fopen()` 创建的文件指针，以及要写入的字符串。可选地，可以添加要写入的字节数。返回写入的字节数，或返回 `FALSE`。 |
| `rewind()` | 将文件指针重置到文件开头 | 唯一的参数是使用 `fopen()` 创建的文件指针。如果成功则返回 `TRUE`，否则返回 `FALSE`。 |

表 7-1 基本文件函数

| 模式 | 说明 |
|---|---|
| `a` | 只写，从文件末尾开始或创建新文件，将新信息追加到文件中先前存在的内容之后。 |
| `a+` | 读写，从文件末尾开始或创建新文件，将新信息追加到文件中先前存在的内容之后。 |
| `r` | 只读，从文件开头开始。 |
| `r+` | 读写，从文件开头开始。 |
| `w` | 只写，删除任何文件内容后或创建新文件。 |
| `w+` | 读写，删除任何文件内容后或创建新文件。 |
| `x` | 创建新文件并只写，从文件开头开始。如果文件存在则返回 `FALSE`。 |
| `x+` | 创建新文件并读写，从文件开头开始。如果文件存在则返回 `FALSE`。 |

表 7-2 `fopen()` 模式

图 7-1 证明了清单 7-1 中的脚本确实有效，提供了以下在线响应：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_229_0.png)

> **注意**
只有当你多次运行脚本时，才会在前图所示的文件中看到多行。`fopen` 的 `a+` 参数使其能够发生这种情况。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_230_0.png)

图 7-1 在每行末尾放置 `\r\n`（回车、换行）会使文件显示为单独的行，而不是一个连续的文本字符串。它也可以用来每次读取一行。

##### 清单 7-1 基本文件函数

```html
<html>
    <head>
        <title>Listing 7-1</title>
    </head>
    <body>
        <h1>Basic File Functions</h1>
        <?php
        echo "<br />", "Create or Open the file.", "<br />";
        $fp = fopen("newfile.txt", "a+");
        if ($fp){
            echo "newfile.txt created.", "<br />";
        }
        else {
            echo "newfile.txt cannot be opened.", "<br />";
        }
        echo "<br />", "Write the file.", "<br />";
        $bytes = fwrite ($fp, "Now is the time for all good men and women
            to come to the aid of their country. \r\n");
        if ($bytes){
            echo $bytes, " byte written.", "<br />";
        }
        else {
            echo "File not written.", "<br />";
        }
        echo "<br />", "Rewind and read the file.", "<br />";
        rewind($fp);
        $data = fread ($fp, $bytes);
        if ($data){
            echo $data, "<br />";
        }
        else {
            echo "File not read.", "<br />";
        }
        echo "<br />", "Close the file.", "<br />";
        if (fclose ($fp)) {
            echo "newfile.txt closed", "<br />";
        }
        ?>
```

```
else {
    echo "newfile.txt not closed.", "<br />";
}
?>
</body>
</html>
```

> **提示**
随着脚本变得越来越长，压缩代码变得非常诱人，例如将 `if` 语句放在一行且不缩进。问题在于这样的代码变得难以目视检查，因此容易出现问题。

#### 附加文件函数

虽然 `fread()` 和 `fwrite()` 功能非常强大，正如你所见，PHP 还提供了许多其他方式来读写服务器存储设备上的数据。`fread()` 和 `fwrite()` 都旨在将文件的部分内容读取到字符串中或从字符串写入。PHP 还可以读取到数组、逐个字符读取、逐行读取，以及使用表 7-3 中描述的函数在文件内移动，这些在清单 7-2 中演示，结果如图 7-2 所示。

> **警告**
`fseek()` 可以将文件指针移动到文件末尾之外，因此你可能需要对此进行测试，并使用带有 `SEEK_END` 常量的负字节数。

| 函数 | 说明 | 解释与参数 |
| :--- | :--- | :--- |
| `feof()` | 确定指针是否在文件末尾（EOF） | 唯一的参数是使用 `fopen()` 创建的文件指针。如果到达 EOF 则返回 `TRUE`，否则返回 `FALSE`。 |
| `fgetc()` | 从打开的文件中读取单个字符 | 唯一的参数是使用 `fopen()` 创建的文件指针。返回包含读取字符的字符串，如果到达 EOF 则返回 `FALSE`。 |
| `fgets()` | 从打开的文件中读取由 `\n` 指定的一行 | 必需的参数是使用 `fopen()` 创建的文件指针，可选地，可以指定要读取的字节数。返回包含读取数据的字符串，或返回 `FALSE`。 |
| `file()` | 将整个文件读入数组，每个元素都是由 `\n` 指定的一行 | 必需的参数是带有路径和文件名的字符串。默认以二进制数据读取，但你可以使用 `FILE_TEXT` 常量作为第二个参数来更改。 |
| `filesize()` | 确定文件的大小 | 唯一的参数是带有路径和文件名的字符串。返回文件大小（以字节为单位），或返回 `FALSE`。 |

表 7-3 附加文件函数

| 函数 | 说明 | 解释与参数 |
| :--- | :--- | :--- |
| `fseek()` | 移动打开文件的文件指针 | 必需的参数是使用 `fopen()` 创建的文件指针，以及移动指针的字节数。默认从文件开头移动，但添加 `SEEK_CUR` 常量作为第三个参数会将字节数加到当前位置，而使用 `SEEK_END` 常量作为第三个参数会将字节数加到 EOF。成功返回 0，否则返回 -1。 |
| `ftell()` | 提供打开文件的文件指针的当前位置 | 唯一的参数是使用 `fopen()` 创建的文件指针。返回从文件开头算起的字节数（整数），或返回 `FALSE`。 |

表 7-3 附加文件函数（续）

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_232_0.png)

图 7-2 PHP 为你提供了多种阅读和浏览文件的方式。



 # **注意**

清单 7-2 使用了清单 7-1 创建的 newfile.txt 文件，在该脚本运行五次之后，会生成五行内容，每行 82 个字符或 bytes，共计 410 bytes。

# **清单 7-2** 额外的文件函数

```
<html>
<head>
    <title>Listing 7-2</title>
</head>
<body>
    <h1>Additional File Functions</h1>
    <?php
    $file = "newfile.txt";
    echo "<br />", "Open the file.", "<br />";
    $fp = fopen($file, "r");
    if ($fp){
        echo "newfile.txt opened.", "<br />";
    }
    else {
        echo "newfile.txt cannot be opened.", "<br />";
    }
    echo "<br />", "Get the file size.", "<br />";
    $bytes = filesize ($file);
    if ($bytes){
        echo "The file size is ", $bytes, " bytes.", "<br />";
    }
    else {
        echo "File size not available.", "<br />";
    }
    echo "<br />", "Check for EOF and rewind if needed.", "<br />";
    if (feof($fp)){
        rewind($fp);
        echo "Returned to the beginning of the file.", "<br />";
    }
    else {
        echo "Not at the end of the file.", "<br />";
    }
    echo "<br />", "Read 10 characters and skip 10 characters.", "<br />";
    echo "File pointer at ", ftell($fp), " bytes.", "<br />";
    while (ftell($fp) < 42) {
        while ($i < 11) {
            $char = fgetc ($fp);
            echo $char ;
            $i++ ;
        }
        $i = 0;
        echo "<br />";
        echo "File pointer at ", ftell($fp), " bytes.", "<br />";
        fseek($fp, 10, SEEK_CUR);
        echo "Now file pointer at ", ftell($fp), " bytes.", "<br />";
    }
```

```
echo "<br />", "Read a line.", "<br />";
rewind($fp);
$data = fgets ($fp);
if ($data) {
    echo $data, "<br />";
}
else {
    echo "File not read.", "<br />";
}
echo "<br />", "Read to an array.", "<br />";
$textArray = file($file);
foreach ($textArray as $line => $text) {
    echo "Line ", $line, " ", $text, "<br />";
}
echo "<br />", "Close the file.", "<br />";
if (fclose ($fp)) {
    echo "newfile.txt closed", "<br />";
}
else {
    echo "newfile.txt not closed.", "<br />";
}
?>
</body>
</html>
```

# **提示**

> 正如清单 7-2 所示，在调试脚本时，插入多个 echo 来显示正在发生的情况，并将特定部分注释掉，直到找出问题所在，这是非常有帮助的。在脚本的最终版本中，这些 echo 可以变成注释。

PHP 文件函数比本节和上一节提到的要多得多，提供了全面的文件操作能力。要查看完整的文件函数集不时，请访问 http://www.php.net/manual/en/ref.filesystem.php。

### Cookie、Session 和服务器变量

网页在使用时会使用变量来临时存储信息。不过，你可能希望收集并存储来自用户、正在运行的脚本以及服务器的信息，并在当前会话期间的其他页面或多个会话中使用这些信息。在本节中，我们将讨论创建和使用会话变量、cookie 和服务器变量来实现收集和存储的功能。首先从表 7-4 中比较这三个对象开始。

| 对象 | 创建方式 | 访问方式 | 存储位置 | 持续时间 |
| :--- | :--- | :--- | :--- | :--- |
| 会话变量 | `$_SESSION` | `$_SESSION` | 服务器 | 会话期间或更短 |
| Cookie | `setcookie()` | `$_COOKIE` | 客户端 | 直到过期 |
| 服务器变量 | 自动 | `$_SERVER` | 服务器 | 无限制 |

# 表 7-4 外部变量比较

会话变量、cookie 和服务器变量都是 PHP 预定义或内置的变量，被称为 *superglobals*（超全局变量），因为它们在整个网站的域内所包含的任意页面上都可用。此处使用的 superglobals 是 `$_SESSION`、`$_COOKIE` 和 `$_SERVER`。它们的用法将在以下章节中解释。本书中讨论的所有 superglobals 都以 `$_` 开头，并且在这里以及许多其他参考资料中，都显示为全部大写，尽管这不是必需的。你还会在本书后面看到其他 superglobals。

Superglobals 是 *associative arrays*（关联数组），即键（key）或数组索引为字符串而非整数的数组。通常 *key* 是元素名称，而 *value* 是元素值。例如：`$_SESSION["name"] = $name;`，其中 `["name"]` 是数组元素的 *key*，而 `$name` 的内容是其 *value*。一些 superglobal 数组（如 `$_SESSION` 和 `$_COOKIE`）允许你定义键，而另一些（如 `$_SERVER`）则具有预定义的键。你将在接下来的章节中看到相关示例。

> 在输入关联数组的键字符串时，可以不使用引号。然而，这是一个不好的做法，因为 PHP 将带引号的字符串与不带引号的字符串视为不同的实体，所以很容易混淆两者，从而在脚本中创建一个难以发现的错误。

#### 会话变量

会话变量允许你在用户与网站的单次 *session*（会话）期间，跨多个页面收集和使用信息。要定义会话，必须使用 `session_start()` 函数启动它，该函数必须位于发送给客户端的所有其他代码之前，包括 `<html>` 和 `<head>`。然后你可以将信息存储在 `$_SESSION` 数组中。如果你转到另一个页面，并再次使用 `session_start()` 函数启动它，就可以检索 `$_SESSION` 数组中的信息。清单 7-3a 和清单 7-3b 演示了这一点，结果如下所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_236_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_236_1.png)

# **提示**

按照“会话变量”中所述测试会话变量时，使用 http://localhost/ 配合 Apache 服务器可能无法工作。请改用 http://127.0.0.1/，这样应该可以正常工作。

# **清单 7-3a** 创建会话变量

```
<?php
session_start()
?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">
<html>
	<head>
		<title>Listing 7-3a</title>
	</head>
	<body>
		<h1>Session Variables, Page 1</h1>
		<?php
			$name = "Joe";
			$amount = "$14.92";
			echo "Store session variables:", "<br />";
				$_SESSION["name"] = $name;
				$_SESSION["amount"] = $amount;
				$_SESSION["time"]  = time();
			echo "Name is: ", $_SESSION["name"], "<br />";
			echo "Amount is: ", $_SESSION["amount"], "<br />";
			echo "Time is: ", date('Y m d H:i:s', $_SESSION["time"]), "<br />";
		?>
	</body>
</html>
```

# **清单 7-3b** 使用会话变量

```
<?php
    session_start()
?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">
<html>
    <head>
        <title>Listing 7-3b</title>
    </head>
    <body>
        <h1>Session Variables, Page 2</h1>
        <?php
            echo "Read session variables:", "<br />";
            echo "Name is: ", $_SESSION["name"], "<br />";
            echo "Amount is: ", $_SESSION["amount"], "<br />";
            echo "Time is: ", date('Y m d H:i:s', $_SESSION["time"]), "<br />";
        ?>
    </body>
</html>
```

> **注意**
会话变量的生命周期有限，由服务器上 `php.ini` 文件中的 `session.cache_expire` 值设置。根据用途，可以设置为从几分钟到数小时，以分钟为增量。默认值为 180 分钟，即三小时。

#### Cookie

Cookie 在客户端计算机上存储信息。一旦 cookie 被存储（或 *set*），创建它的同一网站（实际上是同一 *domain*）在下次连接到客户端时将自动收到该信息。这使得网站能够识别返回ICE返回的客户端。Cookie 使用 `setcookie()` 函数创建，并通过 `$_COOKIE` 超全局变量访问。

> **注意**
出于安全考虑，许多人不允许在他们的计算机上存储 cookie。

##### 使用 setcookie()

你可以使用 `setcookie()` 函数创建和存储 cookie，该函数必须放在脚本中任何其他输出之前，包括 `<html>` 和 `<head>` 标签。其形式如下：



 ```
setcookie(name [,value [,expire [,path [,domain [,secure [,httponly]]]]])
```

`name` 参数是唯一必需的，其余参数均为可选，且如果其右侧没有参数，则可以留空。如果你想跳过某个参数并输入其右侧的参数，请使用空字符串（""）填充，但 `$expire` 除外，它需要 `(0)`。各参数的含义如下：

- **name** 是 cookie 的名称，可以是使用大小写字母、数字和下划线的任何标签。
- **value** 是你希望随 cookie 存储的信息，以字符串形式表示。
- **expire** 是从 1970/1/1 起算，你希望 cookie 过期的时间（以秒为单位）。你可以使用 `time()` 函数来创建这个时间，该函数会返回从 1970/1/1 到当前时刻的秒数，然后加上你希望 cookie 保持活跃的秒数。例如，`time()+(60*60*24*10)` 可以让 cookie 从当前时间起保持活跃十天。默认值为 0，表示 cookie 将在会话结束时过期。
- **path** 是服务器上 cookie 可用的路径。如果路径设置为 "/"，整个域都可以访问该 cookie。
- **domain** 是 cookie 可用的域。如果你希望 cookie 对所有子域可用，请在域名前加一个句点。例如，`.somedomain.com`。
- **secure**，如果设置为 TRUE，则表示 cookie 仅应通过 HTTPS 等安全连接发送。默认值为 FALSE。
- **httponly**，如果设置为 TRUE，则表示 cookie 仅应通过 HTTP 协议访问。默认值为 FALSE。

`value` 参数可以是任何可以放入字符串的内容，例如姓名或金额。如果你想在 cookie 中存储多个独立的信息片段，你需要使用多个 cookie 来实现。不过，从 SUPPORT 和 服务器的角度来看，你可以将从一个站点发送给一个客户端的一组 cookie 视为一个数组。在客户端，它们被存储为独立的信息片段，但在 PHP 中，你可以将它们作为单个数组的元素来访问。本章后面的 Listing 7-4 将提供一个示例。

> **注意**
Cookie 可被间谍软件应用程序查看，因此请勿使用 cookie 存储用户名、密码和账号等敏感信息。

##### 使用 $_COOKIE

设置 cookie 后，下次设置该 cookie 的域重新与客户端连接时，客户端会自动将 cookie 信息返回给服务器，并存储在 $_COOKIE 超全局数组中。你必须关闭设置 cookie 时与客户端的连接，并重新打开连接后，$_COOKIE 才会包含该信息。

Listing 7-4a 演示了一个名为 "MatTech" 的网站如何存储客户的名字、上次订单日期以及所购商品类型，这些 cookie 在 90 天内不会过期，且在设置 cookie 的整个域内可用。Listing 7-4b 演示了如何接收和显示这些信息，如下所示：

###### Listing 7-4a 设置 cookie

```
<?php
    //Set cookies for name, date, and type of purchase
    $name = "Joe";
    $date = time();
    $type = "iPods";
    $expire = time()+(60*60*24*90);
    setcookie("MatTech[name]", $name, $expire, "/");
    setcookie("MatTech[date]", $date, $expire, "/");
    setcookie("MatTech[type]", $type, $expire, "/");
?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">
<html>
	<head>
		<title>Listing 7-4a</title>
	</head>
	<body>
		<h1>Setting Cookies, Page 1</h1>
		<?php
			echo "Cookies set for:", "<br />";
			echo "Name: ", $name, "<br />";
			echo "Date: ", date('m d Y', $date), "<br />";
			echo "Type: ", $type, "<br />";
		?>
	</body>
</html>
```

###### Listing 7-4b 显示 cookie

```
<html>
	<head>
		<title>Listing 7-4b</title>
	</head>
	<body>
		<h1>Displaying Cookies, Page 2</h1>
		<?php
			if (isset ($_COOKIE["MatTech"])) {   //Check if there
				echo "Hello ", $_COOKIE["MatTech"][name], "! <br />";
				echo "Thanks for your order on ", date('M d Y', $_COOKIE["MatTech"][date]), ". <br />";
				echo "Check out our ", $_COOKIE["MatTech"][type], ". <br />";
			}
		?>
	</body>
</html>
```

> **提示**
要删除或取消设置 cookie，请设置一个同名的新 cookie，值为 ""，日期为当前日期之前的时间，例如 time()-3600。如果设置了一组 cookie 数组，则必须全部删除。Listing 7-4c 展示了删除 Listing 7-4 中设置的 cookie 所需的代码。

###### Listing 7-4c 删除 cookie

```
<?php
    //Delete cookies for name, date, and type of purchase
    $expire = time()-(60*60);
    setcookie("MatTech[name]", "", $expire, "/");
    setcookie("MatTech[date]", "", $expire, "/");
    setcookie("MatTech[type]", "", $expire, "/");
?>
```

#### 服务器变量

服务器变量提供有关服务器、运行其上的软件、产生请求的当前脚本以及客户端及其软件的信息。与客户端通信的服务器产生这些信息，并将其存储在超全局数组 $_SERVER 中。每个 Web 服务器产生的数组元素集略有不同，这些元素由其关联键定义。Listing 7-5 是一个用于在你的服务器上显示 $_SERVER 数组元素的简短脚本。图 7-3 显示了在我的计算机上使用 XAMPP 的 Apache 服务器生成的服务器变量，而图 7-4 显示了使用 Aptana 内置服务器生成的一些变量，该服务器仅用于调试目的，因此有更多变量。

##### Listing 7-5 服务器变量生成器

```
<html>
    <head>
        <title>Listing 7-5</title>
    </head>
    <body>
        <h1>Exploring Server Variables</h1>
        <?php
        foreach ($_SERVER as $key => $value) {
            echo "<b> $key &nbsp : &nbsp </b> $value ", "<br />";
        };
        ?>
    </body>
</html>
```

#### 探索服务器变量

```
HTTP_HOST : localhost
HTTP_USER_AGENT : Mozilla/5.0 (Windows; U; Windows NT 6.0; en-US; rv:1.9.0.7) Gecko/2009021910 Firefox/3.0.7
HTTP_ACCEPT : text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
HTTP_ACCEPT_LANGUAGE : en-us,en;q=0.5
HTTP_ACCEPT_ENCODING : gzip,deflate
HTTP_ACCEPT_CHARSET : ISO-8859-1,utf-8;q=0.7,*;q=0.7
HTTP_KEEP_ALIVE : 300
HTTP_CONNECTION : keep-alive
HTTP_COOKIE : MarTech[name]=Joe; MarTech[date]=1236211638; MarTech[type]=Pods
PATH : C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Program Files\Microsoft SQL Server\90\Tools\binn\;C:\Program Files\UltraEdit
SystemRoot : C:\Windows
COMSPEC : C:\Windows\system32\cmd.exe
PATHEXT : .COM; .EXE; .BAT; .CMD; .VBS; .VBE; .JS; .JSE; .WSF; .WSH; .MSC
WINDIR : C:\Windows
SERVER_SIGNATURE : Apache/2.2.11 (Win32) DAV/2 mod_ssl/2.2.11 OpenSSL/0.9.8i mod_autoindex_color PHP/5.2.8 Server at localhost Port 80

SERVER_SOFTWARE : Apache/2.2.11 (Win32) DAV/2 mod_ssl/2.2.11 OpenSSL/0.9.8i mod_autoindex_color PHP/5.2.8
SERVER_NAME : localhost
SERVER_ADDR : 127.0.0.1
SERVER_PORT : 80
REMOTE_ADDR : 127.0.0.1
DOCUMENT_ROOT : C:/xampp/htdocs
SERVER_ADMIN : admin@localhost
SCRIPT_FILENAME : C:/xampp/htdocs/Chap07/Listing 7-5.php
REMOTE_PORT : 51633
GATEWAY_INTERFACE : CGI/1.1
SERVER_PROTOCOL : HTTP/1.1
REQUEST_METHOD : GET
QUERY_STRING :
REQUEST_URI : /Chap07/Listing%207-5.php
SCRIPT_NAME : /Chap07/Listing 7-5.php
PHP_SELF : /Chap07/Listing 7-5.php
REQUEST_TIME : 1236287095
argv : Array
argc : 0
```

**图 7-3** XAMPP Apache Web 服务器生成的服务器变量

**图 7-4** Aptana 内置 Web 服务器生成的服务器变量

要查看和使用服务器变量，请使用 $_SERVER 和特定的键。由于大多数键的值是一个很长且不同的字符串，你不希望检查是否相等，而是检查字符串是否包含特定的词。Listing 7-6 展示了如何检查正在使用的浏览器是否为 Firefox，以下分别是使用 Internet Explorer、Firefox 和 Google Chrome 的结果：

##### Listing 7-6 检查浏览器类型

```
<html>
    <head>
        <title>Listing 7-6</title>
    </head>
    <body>
        <h1>Checking for Browser Type</h1>
        <?php
        if(strpos($_SERVER[HTTP_USER_AGENT], "MSIE")) {
            echo "The browser is Internet Explorer. <br />";
        }
```



 228 动态 Web 编程入门指南

```
elseif (strpos($_SERVER["HTTP_USER_AGENT"], "Firefox")) {
    echo "The browser is Firefox. <br />";
}
else {
    echo "A different browser is being used. <br />";
}
?>
</body>
</html>
```

> **注意**
> 清单 7-6 无法识别 Aptana 内置 Firefox 浏览器中的 Firefox，因为其字符串中不包含该单词。此外，IE 和 Firefox 的字符串中都包含 "Mozilla" 一词。

清单 7-6 中使用的 `strpos()` 函数功能强大且有趣。其既定用途是在一个字符串中查找另一个字符串首次出现的位置。不过，它最常用的用途是简单地判断一个字符串是否存在于另一个字符串中，如清单 7-6 和清单 7-11 中所示。PHP 手册将其比喻为"大海捞针"。

> **提示**
> 要查看完整的服务器变量集合及其含义，请访问 http://www.php.net/manual/en/reserved.variables.server.php。

### 用户认证

用户认证允许你限制谁可以访问网站。它要求所有用户注册网站，提供姓名、唯一 ID（通常是电子邮件地址）和密码。这些信息存储在磁盘文件中，ID 和密码经过加密，以防止被滥用。用户已注册的事实（而非其 ID 和密码）会存放在用户计算机上的 cookie 中，这样他/她就无需再次注册。希望进入网站的用户需要输入其 ID 和密码，这些信息经过加密后与注册用户文件中的加密值进行比较。如果 ID 和密码与文件中的条目正确匹配，用户就被允许进入网站。用户已通过认证的事实（而非其 ID 和密码）存储在会话变量中，这样用户就可以自由地在网站各页面之间移动，无需重新输入信息。

图 7-5 展示了执行用户认证功能的系统流程图。它包括四个区域的六个脚本：

- **初始网站** index.php 脚本，检查用户是否拥有 cookie。
- **注册区域** 包含两个脚本，一个供用户输入其信息，另一个用于加密用户信息、将其写入磁盘，并创建和设置 cookie。
- **登录区域** 包含两个脚本，一个供用户输入其信息，另一个用于加密用户信息、与磁盘信息进行比较，并创建和设置会话变量。
- **常规网站页面**，检查会话变量是否存在。

以下将分节逐一讨论这些内容。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_246_0.png)

> **警告**
> 
> 此用户认证系统*仅*用于演示目的，*并非*旨在作为保护网站访问的完全安全流程。它也不适用于大量用户，因为每次使用时整个用户磁盘文件都会被读入内存。仅将其作为 PHP 代码示例，或作为你自己系统的起点。*使用此系统的任何风险由你自己承担。*

在接下来的几章中，你将了解如何将数据库用于文件，这将极大地帮助用户认证系统并支持大量用户。

#### 索引脚本

当网站加载时，自动打开而无需特别请求的脚本就是索引脚本，这里是 index.php。因此，用户认证系统将使用该脚本启动认证。如果网站中的任何其他脚本被打开，该脚本将检查用户是否已登录，如果没有，则将用户引导至登录页面。如果脚本上带有保护代码，用户将无法进入网站上的任何脚本。

index.php 脚本（参见清单 7-7）包含一系列非常简单的 PHP 语句，询问用户是否拥有该网站的 cookie。（示例脚本使用 Matthews Technology 作为网站名称，缩写为 "MatTech"。实际使用此代码时，你可能需要更改该名称。）如果用户拥有之前访问该网站并在最近 180 天内注册的 cookie，则会创建一个会话变量，包含其姓名、当前日期和一个用于登录的重试变量。然后用户被引导至 signin.php 脚本。如果用户没有 cookie，他/她将被发送到 register.php 脚本。

index.php 脚本有几个独特之处：

- 该脚本是纯 PHP 代码，没有 X/HTML 代码，且不向用户显示任何内容。你会看到在该系统中我们多次这样做。

- 脚本使用 `isset()` 函数来确定 cookie 是否存在。请记住，如果某个域已在用户计算机上设置了 cookie，那么下次用户连接到该服务器时，它会自动返回给该域的服务器。

- `header("Location:... ")` 函数用于通过 HTML 标头通知服务器发送另一个脚本，从而将执行转移到另一个 Web 脚本。此函数*必须*在发送任何其他输出给用户之前执行，例如 echo 语句或 `<html>` 或 `<head>` 元素。

> **提示**
>
> 开始时可以使用大量 echo 语句来辅助调试，并使用 XHTML
> `<a href=...>`（锚点）元素代替 PHP header 语句，因为 header
> 不能在任何输出之后使用，例如 echo 语句。

**清单 7-7** index.php

```
<?php
    session_start();
    //Check if user has a cookie.
    if (isset ($_COOKIE["MatTech"])) {
        //If so, set session and go to sign in.
        $_SESSION["name"] = $_COOKIE["MatTech"]["name"];
        $_SESSION["retry"] = 0;
        $_SESSION["time"] = time();
        header( "Location: signin.php");
    }
    else {
        //If not, go to registration.
        header( "Location: register.php");
    }
?>
```

#### 注册脚本

如前所述，注册脚本有两个：register.php 处理用户输入，enterName.php 负责处理。可以在一个脚本中完成所有这些操作，如你在某些 PHP/MySQL 示例中将看到的那样，但两个脚本的解决方案为这个过程提供了清晰的介绍。

##### 输入表单

register.php 脚本（参见清单 7-8）是一个包含表单表格，有三个字段：姓名、用户 ID 和密码，如图 7-6 所示。当用户填写完表单（其内容放入 $_POST 超全局数组）并点击 **Register** 后，表单操作将执行转移到 enterName.php 脚本。

> **提示**
>
> 可以使用带有 Body (onload) 事件的 JavaScript 自动跳转到第一个表单字段。

###### 清单 7-8 register.php

```
<!--User enters name, ID, and password.-->
<html>
    <head>
        <title>Listing 7-8 Registration Page</title>
    </head>
    <body>
        <div>
            <img src="MatTech.gif" alt="Matthews Technology" />
        </div>
        <div id="form">
            <!-- Go to enterName.php after clicking Register -->
            <form action="enterName.php" method="post" id="registerForm">
            <table width="150" border="1" cellspacing="3" cellpadding="5" >
                <tr height= 50>
                    <th colspan= "2" valign="middle" >
                        <p id="head">Welcome to Matthews Technology!</p>
                        <p id="body">Please enter your Name,<br />User ID, and Password</p>
                    </th>
                </tr>
                <tr>
                    <td width="40">
                        <p class="label">Name:</p>
                    </td>
                    <td width="100">
                        <input type="text" name="name" value="" size="60" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <p class="label">User ID:</p>
                    </td>
                    <td>
                        <input type="text" name="userid" value="" size="60" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <p class="label">Password:</p>
                    </td>
                    <td>
                        <input type="password" name="passwd" value="" size="20" />
                    </td>
                </tr>
            </table>
                <input type="submit" name="submit" value="Register" />
            </form>
        </div>
    </body>
</html>
```



 **图 7-6** 注册表单可以使用 CSS 来美化一下。

##### 加密并保存到磁盘

`enterName.php` 脚本如清单 7-9 所示，是第二个纯 PHP 脚本。它获取注册时输入的名称，并通过 `$_POST` 超全局变量传递给该脚本。该名称与当前时间和过期时间结合，用于创建并设置用户计算机上的 cookie。用户在注册时输入的用户 ID 和密码被组合起来，然后使用 SHA1（安全哈希算法 1）进行加密，实现 160 位加密。接着，当前时间、用户名称以及加密后的 ID 和密码被放入一个数组中，并使用 `file_put_contents()` 函数将该数组写入磁盘（因为它允许将数组追加到现有的磁盘文件）。然后系统执行返回到 `index.php`。

###### 清单 7-9 enterName.php

```
<?php
/* Cookie is written. Then the user id
 * and password are encrypted and that and
 * the name are written to disk. */

//Information for cookie, expires in 6 months.
$name = $_POST['name'] ;
$date = time() ;
$expire = time()+(60*60*24*180);

//Set cookie.
setcookie("MatTech[name]", $name, $expire, "/");
setcookie("MatTech[date]", $date, $expire, "/");

//Combine userid and password and encrypt it.
$userPasswd = $_POST['userid'] . $_POST['passwd'];
$encryptid_pw = sha1($userPasswd);

//Build an array of data and write it to disk.
$entry = array( 'index' => time(),
                'name' => $name,
                'encrypt' => $encryptid_pw,
              );
if (!$byteswrite = file_put_contents('namelist.txt',
   $entry, FILE_APPEND)) {
    echo "<br />File not written.<br />";
}

//Return to Index.php.
header( "Location: index.php");
?>
```

#### 登录脚本

同样，两个登录脚本 `signin.php` 和 `verify.php` 可以合并为一个脚本，但为了本练习的清晰起见，将它们分开。

##### 登录

一旦用户的计算机上有了 cookie，用户就会直接进入 `signin.php`。这同样是一个表格内的表单，如图 7-7 和清单 7-10 所示，它使用 `$_POST` 超全局变量，通过表单操作将用户 ID 和密码传递给 `verify.php`，当用户点击**登录**时触发。

> **注意**
>
> 如果不注册，则不应该进入 `signin.php`，但添加了"未注册？点击这里！"以便您可以在不删除 cookie 的情况下返回到 `register.php`。

动态 Web 编程：入门指南

![图 7-7 用户 ID 和密码通过互联网未加密传输是一个重大安全漏洞。使用 HTTPS 执行此操作会有所帮助。]

###### 清单 7-10 signin.php

```
<!-- User enters id and password. -->
<html>
  <head>
    <title>Listing 7-10 Sign-In</title>
  </head>
  <body>
    <div>
      <img src="MatTech.gif" alt="Matthews Technology" />
    </div>
    <div id="form">
      <!-- Display the sign-in form. After filling in, go to verify script. -->
      <form action="verify.php" method="post" id="signinForm">
        <table width="100" border="1" cellspacing="3" cellpadding="5" >
          <tr height= 50>
            <th colspan= "2" valign="middle" >
              <p id="head">Welcome Back!</p>
              <p id="body">Please enter your<br />User ID and Password</p>
              <p id="body">Not registered? <a href="register.php">Click here!</a></p>
            </th>
          </tr>
<tr>
    <td width="50">
        <p class="label">User ID:</p>
    </td>
    <td width="120">
        <input type="text" name="userid" value="" size="60" />
    </td>
</tr>
<tr>
    <td>
        <p class="label">Password:</p>
    </td>
    <td>
        <input type="password" name="passwd" value="" size="20" />
    </td>
</tr>
</table>
<input type="submit" name="submit" value="Sign In" />
</form>
</div>
</body>
</html>
```

##### 验证输入

`verify.php` 脚本如清单 7-11 所示，使用 `file_get_contents()` 函数将整个 `namelist.txt` 文件读入 `$namelist` 字符串。然后它将登录时输入的用户 ID 和密码组合起来并加密该组合。接着使用 `strpos()` 函数检查加密后的组合是否包含在 `$namelist` 中。如果加密信息存在，则更新会话变量，并将执行转移到站点脚本。如果加密信息在磁盘文件中未找到，则 `$retry` 变量递增，并检查是否大于 3。如果是，则执行转移到 `register.php`；否则，将 `$retry` 变量存储在 `$_SESSION` 变量中，并将执行转移到 `signin.php`。

###### 清单 7-11 verify.php

```
<?php
    session_start();

    // Verify user's id and password, and create session.

        //Read the name list file.
        if(!$namelist = file_get_contents('namelist.txt')) {
            echo "<br />File not read.<br />";
        }

//Combine the user ID and password and encrypt it.
$userPasswd = $_POST['userid'] . $_POST['passwd'];
$testentry = sha1($userPasswd);

//Determine if the encrypted user ID and password are in file.
if(strpos($namelist, $testentry)){

    //If there, reset the session and enter site.
    $_SESSION["retry"] = "admit";
    $_SESSION["time"] = time();
   哈姆( "Location: enterSite.php");
}
else {
    //If not, add to Session Retry and test > 3
    $retry = $_SESSION["retry"];
    $retry++;
    if ($retry > 3) {
        //If greater than 3 go to register.
        header( "Location: register.php");
    }
    else {
        //If less than 3, reset Session Retry and go to Sign in
        $_SESSION["retry"] = $retry;
        header( "Location: signin.php");
    }
}
?>
```

#### 站点页面

每个常规站点页面上的代码片段（见清单 7-12）检查 `$_SESSION["retry"]` 是否存在且等于 `"admit"`。如果是，则向用户问好，执行流程进入常规页面。否则，执行返回到 `index.php`，用户必须证明她有 cookie，否则她将不得不注册，无论哪种情况她都必须登录。

> **提示**
>
> 与其在每个常规站点页面上包含清单 7-12 中的 PHP 代码片段，不如将该 PHP 片段保存为其自己的文件；然后在每个站点页面的第一行插入 `<?php require_once(enterSite.php); ?>`。`require` 和 `require_once` 函数的一个特性是，页面上其余的脚本在被引用代码成功执行之前不会执行。如果出现致命错误，它会停止执行。这与 `include` 和 `include_once` 函数形成对比，后两者不会停止其余脚本的执行。`_once` 防止该片段被加载多次。

**清单 7-12  enterSite.php**

```
<?php
    session_start();
//Having successfully signed in...
    //Check to see if session variable present and is "admit"
    if (isset($_SESSION["retry"]) && $_SESSION["retry"] == "admit") {
        //If so, continue.
        echo "Hello ", $_SESSION["name"], "!<br />";
    }
    else {
        //If not, return to the site Index page.
        header( "Location: index.php");
    }
?>
```

可以做很多事情来增强这个系统。第一件事可能是让收集用户 ID 和密码的部分使用 HTTPS，从而保护该传输的安全。第二件事是使用 CSS 让数据收集表单看起来更美观。另外两个我们将在第 9 章中讨论的领域是更好地处理错误消息，例如从磁盘读写错误返回的消息，以及处理用户试图在表单中输入不寻常字符和其他内容（如粘贴图片）的情况。

# 第四部分

使用 MySQL 和 PHP 驱动数据库

在第 7 章中，您了解了如何使用 PHP 读写磁盘文件进行用户身份验证。虽然这种方法可行，但它有限制，因为您必须将整个文件读入内存，并在那里搜索以执行所需操作。在第四部分中，您将看到 MySQL，一个成熟的关系型数据库管理系统（RDBMS），如何大大增强读取、写入、维护、更改、搜索和重新排列存储在计算机文件中的信息的过程。它是使网站动态化的第三大主要工具，虽然网站需要 HTML 和 PHP 以及 MySQL，但在数据处理方面，MySQL 承担了繁重的工作。

第 8 章讨论 MySQL 的基础知识以及它如何与 PHP 一起使用。它首先介绍关系型数据库、SQL（结构化查询语言）以及使用数据库的基础知识。然后描述如何通过 Internet 或 Intranet 使用 phpMyAdmin 创建、更改和管理 MySQL 数据库。最后，讨论用于操作 MySQL 数据库的 PHP 函数，并举例说明它们的使用方法。

第 9 章回顾并演示 PHP 和 MySQL 的数据库处理功能，通过数据录入、验证、存储和检索的示例，还演示了如何搜索或查询数据库、更新和删除记录，以及在网页上格式化和显示数据库信息。

在本第四部分的开篇中，我们将提供一些关于 MySQL 的背景信息，并讨论您应该运行哪些工具来与 PHP 和 MySQL 一起工作。

## 关于 MySQL

MySQL 是一个关系型数据库管理系统，使用结构化查询语言来存储、处理和检索互联网上的信息。MySQL 被称为"世界上最受欢迎的开源数据库"，有数百万个网站在使用它。MySQL 是一种 Web 资源，与 PHP 一样运行在 Web 服务器上。MySQL 旨在处理大容量、多用户的数据库访问。维基百科称，MySQL 被多个高流量网站使用，包括 Flickr、Facebook、维基百科、Google、Nokia 和 YouTube。由于其易用性、速度和可靠性，MySQL 对小型站点也非常适用，这解释了它的广泛应用。

> **注意**
>
> 此处讨论的 GNU 通用公共许可证是为瑞典 GNU 操作系统开发的免费软件示范许可证。"GNU"不是首字母缩写词，而是一种类似羚羊的动物的名字。

MySQL 最初于 1995 年由 MySQL AB 开发并发布，该公司是一家瑞典公司，现为 Sun Microsystems 的子公司。MySQL AB 在专有许可证之外，还以 GNU 通用公共许可证（GPL）提供该程序。GPL 规定

任何使用 MySQL 的系统都必须按照类似的许可协议进行分发。正是这种安排使得 MySQL 能够随 XAMPP 一起提供。在撰写本文时（2009 年春季），XAMPP 包含 MySQL 5.1.30。MySQL AB/Sun Microsystems 提供 MySQL Community Server，可以免费下载，但安装、集成和管理需要相当的专业知识。它还提供 MySQL Enterprise，附带许多工具和技术支持，使工作变得更加轻松，但需要付费。XAMPP 使使用 MySQL 变得相对简单，是启动项目的好方法。MySQL AB 目前提供 5.1.32 版本，以及用于开发和测试的 6.1 alpha 版本。在所有情况下，MySQL 都是一个成熟、功能齐全的专业 RDBMS，这可以从其网站 http://www.mysql.com 看出。许多专业的 Web 开发人员认为，PHP 和 MySQL 是为任何规模的网站添加数据库的最佳方式。

### MySQL 所需工具

要有效地使用 MySQL，您需要具备本书前面各章节介绍中描述的相同工具。第 I 部分介绍中描述并推荐了一些可以下载的软件包来完成这项工作，包括：

- **Aptana Studio**，一个集成开发环境，默认可为 HTML、CSS 和 JavaScript 提供强大的创作功能，通过附加组件或插件，还可以支持 PHP。
- **XAMPP** 是 Apache Web 服务器、MySQL 数据库服务器以及 Perl 和 PHP 服务器的组合，它们都在您的计算机上运行，并模拟您将网站上传到具有这些服务器的商业 Web 主机时看到的情况。
- **IE 6**、**IE 7** 和 **Firefox** 浏览器都是测试和调试脚本所必需的。由于绝大多数网络浏览人群使用这些浏览器，因此在所有浏览器中尝试您的网页非常重要。在撰写本文时，IE 8 正在进行最终测试，也是您用于测试的强力候选者。它适用于 Windows XP 和 Windows Vista，以及 Windows 7。

如果您还没有 Aptana Studio、XAMPP、IE 6、IE 7 和 Firefox，请返回第 I 部分介绍，按照说明下载并安装它们。本书剩余章节的讨论都需要它们。

> **提示**
> 本章和下一章需要运行 XAMPP，并且至少有一个浏览器打开到 http://localhost/xampp。如果您桌面上有 XAMPP 图标，请双击它。否则点击**开始 | 所有程序 | Apache Friends | XAMPP | XAMPP 控制面板**。在 XAMPP 控制面板中，点击 Apache 对应的**启动**，并点击 MySQL 对应的**启动**，如下图所示。

# 动态 Web 编程：初学者指南

打开浏览器，在地址栏中输入 `http://localhost/xampp`，然后点击左侧的**状态**。前五项服务应该已激活，如图 P4-1 所示。

> **提示**
> 如果您在 `http://localhost/` 上查看网站时遇到问题，请尝试 `http://127.0.0.1/`。

本书的这一部分也严重依赖 PHP 的基础知识，如本书第 III 部分所述。如果您不具备这些知识，强烈建议您返回该部分，在开始第 IV 部分之前先熟悉 PHP。

**图 P4-1** "Localhost" 是运行在您计算机上的 Apache Web 服务器，它提供对 MySQL 的访问。

# 第 8 章

## MySQL 基础

## 关键技能与概念

- 理解 RDBMS
- 理解 SQL
- 使用 MySQL
- 打开和探索 phpMyAdmin
- 在 phpMyAdmin 中创建和使用数据库
- 操作数据库
- 获取数据库信息
- 管理数据库
- 结合使用 PHP MySQL 函数

MySQL 赋予网站快速高效地存储、检索和处理大量信息的能力。这使得网站能够展示大量待售商品目录、提供对大量档案信息的访问和搜索能力，或注册和服务大量个人，例如组织的成员。

本章将介绍关系数据库、SQL（结构化查询语言）以及直接使用 MySQL 的基础知识。然后介绍如何通过 Internet 或 Intranet 使用 phpMyAdmin 创建、更改和管理 MySQL 数据库。最后，讨论用于操作 MySQL 数据库的 PHP 函数，并举例说明它们的使用方法。

### 关系数据库与 SQL

作为 RDBMS，MySQL 处于数据库引擎的顶级行列，通过实现 SQL，它成为这些产品中最复杂的产品之一。该组中的其他产品包括 Oracle、IBM 的 DB2 和 Microsoft 的 SQL Server。要充分理解 MySQL 及其强大功能，理解 RDBMS 和 SQL 非常重要。

**图 8-1** 数据库是带有记录和字段的表。

#### 理解 RDBMS

数据库最简单的形式是信息*表*，如图 8-1 中显示的 Excel 书籍列表所示。每本书的条目是表中的一行，称为*记录*。书籍条目中的每条信息，例如标题或作者，是表中的一列，称为*字段*。

图 8-1 中的表称为*平面文件*，数据库中的所有信息都在单个表中。注意到有几本书具有相同的作者、相同的出版商或相同的类别。如果这些字段被制作成包含附加信息的独立表，将简化 Books 表，提供更多信息，并节省存储空间。（在此数据库中节省量非常小，但如果您有一个大型数据库，节省量将是可观的。）生成的四个表如图 8-2 所示，形成一个*关系数据库*。

在关系数据库中，重复的信息片段存储在单独的表中，并通过它们的*键*或索引相互关联，键是分配给表中每条记录的唯一值。在它所索引的表中，键称为*主键*。当该键在另一个表中使用时，称为*外键*。例如，在 Authors 表中，Aid（作者 ID）是主键，但在 Books 表中，Aid 是外键，将 Authors 表与 Books 表关联起来。Books 数据库中的完整关系集如下所示。

| BkID | 书名 | Aid | Pid | 价格 | Cid |
|------|------|-----|-----|------|-----|
| 3 | 2010 | 3 | 3 | 3.95 | 1 |
| 5 | A Thief of Time | 5 | 5 | 4.95 | 3 |
| 7 | Hornet Flight | 4 | 4 | 7.99 | 2 |
| 4 | Lie Down with Lions | 4 | 4 | 4.95 | 3 |
| 9 | Mission of Honor | 2 | 2 | 7.99 | 2 |
| 1 | Nightfall | 1 | 1 | 5.99 | 1 |
| 2 | Patriot Games | 2 | 2 | 4.95 | 2 |
| 6 | The Fly on the Wall | 5 | 5 | 4.95 | 3 |
| 8 | The Innocent Man | 6 | 6 | 7.99 | 2 |

| Aid | 姓氏 | 名字 |
|-----|------|------|
| 1 | Asimov | Isaac |
| 2 | Clancy | Tom |
| 3 | Clarke | Arthur |
| 4 | Follett | Ken |
| 5 | Hillerman | Tony |
| 6 | Grisham | John |

| Pid | 出版商 | 地址 | 城市 |
|-----|--------|------|------|
| 1 | Bantam | 666 5th Ave | New York |
| 2 | Berkley | 200 Madison | New York |
| 3 | Ballantine | 201 E 50th | New York |
| 4 | Signet | 375 Hudson | New York |
| 5 | Harper | 10 E 53rd | New York |
| 6 | Dell | 666 5th Ave | New York |

| Cid | 类别 | 区域 |
|-----|------|------|
| 1 | Sci. Fic. | F-14 |
| 2 | Thriller | G-10 |
| 3 | Mystery | E-9 |

**图 8-2** 关系数据库将重复信息放入单独的表中。

将具有重复值的字段取出并放入其自己的表中的过程称为*规范化*。它不仅减少了数据库占用的空间，还显著增强了数据库的可维护性。如果没有规范化，如果要更改字段中的值，就必须更改数据库中该值的所有出现位置。有了规范化，您只需更改单个出现位置。

#### 理解 SQL

SQL，即结构化查询语言，是使用类似口语的语句与数据库进行交互的有效手段。SQL 最初由 IBM 开发，此后成为国际标准，被许多 RDBMS 使用。SQL 被设计为一种结构化的声明性查询语言，用于关系数据库。SQL 语句通常以声明性关键字开头，例如 **CREATE**、**DELETE**、**INSERT**、**OPEN**、**SELECT** 和 **UPDATE**。然后跟一个或多个子句，以一个或多个以下关键字开头：**FROM**、**GROUP BY**、**HAVING**、**JOIN**、**ORDER BY** 和 **WHERE**。例如，使用前面定义的 Books 数据库和表：

```
SELECT * FROM books WHERE price > 5.00 ORDER BY books.title;
```

将从 Books 表中选择 Price 大于 $5.00 的所有记录（星号），并按 Book Title 对结果列表进行排序。清单 8-1 显示了额外的 SQL 语句示例，这些语句构建了包含五个字段的 Books 表，其中三个是可变

字符字符串的最大长度可以是 255 或 60 个字符。BkID 字段是一个整数，必须有值（NOT NULL），并且是该表的主键。随后向表中插入了六本书的数据。在前五条记录中，每个字段都有值，因此没有指定字段名。对于第六本书，缺少两个字段，因此必须指定存在的字段。然后更新表以修改第 3 本书的价格，并修改第 5 本书的标题以纠正拼写错误。最后从表中删除第 6 本书。

##### 清单 8-1 SQL 语句示例

```
CREATE TABLE books (
    bkid int NOT NULL PRIMARY KEY,
    title varchar(255),
    author varchar(60),
    publisher varchar(60),
    price decimal(10,2));
INSERT INTO books VALUES
    (1, 'Nightfall', 'Asimov', 'Bantam', 5.99);
INSERT INTO books VALUES
    (2, 'Patriot Games', 'Clancy', 'Berkley', 4.95);
INSERT INTO books VALUES
    (3, '2010', 'Clarke', 'Ballantine', 3.95);
INSERT INTO books VALUES
    (4, 'Lie Down with Lions', 'Follett', 'Signet', 4.95);
INSERT INTO books VALUES
    (5, 'A Thief of Time', 'Hillerman', 'Harper', 4.95);
INSERT INTO books (bkid,title,price) VALUES
    (6, 'The Innocent Man',7.99);
UPDATE books SET price=5.99 WHERE bkid = 3;
UPDATE books SET title='A Thief of Time' WHERE bkid = 5;
DELETE FROM books WHERE bkid = 6;
```

当然，还有许多其他的 SQL 关键字和从句，以及各种数据类型和函数。不过，本书的目的是探讨如何在 PHP 中使用 MySQL。虽然 MySQL 与 SQL 紧密相关，但两者存在一些差异，因此我们将以这个简短的介绍结束对 SQL 的讲解。

### 使用 MySQL

MySQL 服务器可以通过多种方式使用。这里我们将介绍三种方式：直接通过 MySQL 命令行客户端；通过 phpMyAdmin 用户界面在线使用；以及通过 PHP 编程方式使用。在本节中，我们将简要介绍命令行客户端；在下一主要章节中，我们将探讨 phpMyAdmin；再之后的章节中，我们将深入讲解如何使用 PHP 操作 MySQL。

MySQL 命令行客户端主要用于确认 MySQL 是否已安装并在计算机上运行，以及对数据库进行一些快速维护。数据库的主要设置和维护通过 phpMyAdmin 完成，而数据库的常规使用则通过编程方式完成，在本书中即使用 PHP。

#### 启动 MySQL 命令行客户端

安装 XAMPP 时，MySQL 命令行客户端会被放置在计算机上，位于 c:/xampp/mysql/bin 文件夹中。如果它尚未运行，请启动 XAMPP，然后按照以下说明加载并试用 MySQL：

1. 如果桌面上有 XAMPP 图标，请双击它。否则点击**开始 | 所有程序 | Apache Friends | XAMPP | XAMPP 控制面板**。

2. 在 XAMPP 控制面板中，点击 Apache 对面的**启动**，并点击 MySQL 对面的**启动**，如第四部分引言中所示。

3. 通过点击**开始 | 计算机**（Windows XP 中为"我的电脑"）打开 Windows 资源管理器。

4. 通过双击 **c:** 驱动器，向下滚动并打开 **xampp | mysql | bin**，切换到 c:/xampp/mysql/bin 文件夹。

5. 通过双击 **mysql.exe** 打开 MySQL 命令行客户端窗口，如图 8-3 所示。

6. 在 **mysql>** 提示符下输入

select version(), current_date;

然后按 **ENTER**。您的命令窗口应如下所示：

**图 8-3** XAMPP 提供了一整套 Web 开发软件，包括完整版的 MySQL。

**7.** 如果您能够按照上述说明操作并获得所示结果，则 MySQL 已正确安装并运行。如果不能，您需要重新检查安装过程，并可能参考这些说明来查找错误所在。

**8.** 如果您要直接进入下一节，请直接进行。否则输入 `exit`，然后按 ENTER。

> **注意**
>
> 某些较早版本的 XAMPP 安装在 Program Files 文件夹中，因此 mysql.exe 的路径将是 c:/program files/xampp/mysql/bin。

#### 在命令行上构建表

构建一部分 Books 表，对其执行查询，然后将其删除，请按照以下说明操作（结果如图 8-4 所示）：

1. 如果您已退出命令行窗口，请使用前面说明中的必要步骤重新打开它。

**图 8-4** MySQL 命令行客户端有点繁琐，可能不是您操作 MySQL 的首选。

2. 要将 Books 表附加到现有数据库，请在 `mysql>` 提示符下输入以查看可用的数据库：

`SHOW DATABASES;`

然后按 **ENTER**。

3. 要使用 Test 数据库，在 `mysql>` 提示符下输入

`USE test;`

然后按 **ENTER**。

4. 要开始创建新表，在 `mysql>` 提示符下输入

```
CREATE TABLE books (
    bkid int NOT NULL PRIMARY KEY,
    title varchar(255),
    author varchar(60));
```

然后按 **ENTER**。这段代码可以在一行中输入，或者使用 **SHIFTьк**（换行）分成多行，如这里所示。

5. 在 `mysql>` 提示符下输入以下内容，将图书添加到数据库中

```
INSERT INTO books VALUES
      (1, 'Nightfall', 'Asimov');
```

然后按 ENTER。同样，这可以是一行或两行。

6. 继续添加图书，在 `mysql>` 提示符下输入

```
INSERT INTO books VALUES
      (2, 'Patriot Games', 'Clancy');
```

然后按 ENTER。

7. 在 `mysql>` 提示符下输入

```
INSERT INTO books VALUES
      (3, '2010', 'Clarke');
```

然后按 ENTER。

8. 列出数据库中的图书，按标题排序。在 `mysql>` 提示符下输入

```
SELECT * FROM books ORDER BY title;
```

然后按 ENTER。

9. 删除表。在 `mysql>` 提示符下输入

```
DROP TABLE books;
```

然后按 ENTER。

10. 关闭 MySQL 命令行客户端。在 `mysql>` 提示符下输入

```
exit;
```

然后按 ENTER。

> **提示**
>
> MySQL 命令行客户端是进行小型、快速数据库修复；小型一次性查询；以及测试 MySQL 命令响应方式的良好工具。

### 使用 phpMyAdmin

phpMyAdmin 是一个用于操作 MySQL 数据库的在线图形用户界面，使用 PHP 编写。它是 XAMPP 附带的程序之一。phpMyAdmin 的主要用途是Initializer设置将通过 PHP 编程使用的数据库及其表，以及对数据库进行偶尔维护。它并非用于数据库的日常使用，日常使用通过 PHP 或其他程序完成。

在本节中，我们将探索 phpMyAdmin，查看其安全性及如何更改，创建带表的数据库，并查看数据库规范的详细信息，包括各种数据类型。

#### 打开并探索 phpMyAdmin

按照以下步骤打开并探索 phpMyAdmin：

1. 如果尚未运行，请打开 XAMPP 控制面板并启动 Apache 和 MySQL，如本章前面所述。

2. 打开浏览器，在地址栏中输入 http://localhost/xampp/，然后按 ENTER。

3. 在左列中点击 **phpMyAdmin**，它将打开如图 8-5 所示。

图 8-5 所示的 phpMyAdmin 窗口在左侧列出了内置数据库，括号中为表的数量。右侧是各种设置、当前 MySQL、Apache、PHP 和 phpMyAdmin 的版本，以及 phpMyAdmin 的文档。中间可以创建新数据库和更改界面。顶部有十个选项卡，提供关于现有 MySQL 数据库的更多详细信息，以及更改设置的功能，在 SQL 选项卡中，您可以执行 MySQL 命令行客户端中的所有操作。

在窗口底部，您会看到一个警告，phpMyAdmin 的默认设置没有为默认用户名"root"设置密码。这意味着任何知道用户名"root"的人（很多人都知道）都可以访问您的数据库并随意操作。在 localhost（或 127.0.0.1）上自己计算机上工作时，风险不大，但当您将网站上传到商业主机时，将用户名设置为非"root"并使用强密码就变得至关重要。下一节将向您展示如何操作。

#### 设置权限

您可以通过 phpMyAdmin 的"权限"选项卡设置和更改密码，添加和删除用户——前提是您有执行这些操作的权限，root 用户就有（这也是要为 root 设置密码的另一个原因，即使是在您自己的计算机上）。现在来做：

1. 从 phpMyAdmin 主页（如图 8-5 所示；如果不在那里，点击选项卡上方的 **服务器:localhost**），点击 **权限** 选项卡。用户概览打开，如图 8-6 所示。

您可以看到 root 用户已设置（至少在我的情况下）用于 localhost 和 127.0.0.1，两种情况下都没有设置密码，并且拥有所有权限，包括授予他人权限的能力。

2. 点击列出的第一个 root 用户右侧的 **编辑权限** 图标。详细信息权限页面的顶部打开。在这里您可以看到可以设置的完整权限列表。

3. 向下滚动直到看到"更改密码"，然后点击密码对面的文本框。



 254 Dynamic Web Programming: A Beginner's Guide

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_271_0.png)

图 8-6 MySQL 内置了全面的安全系统。

4. 输入您要使用的密码（为了获得最高强度，请将密码设置为六到八个字符，并包含大写和小写字母、数字以及至少一个特殊字符的组合）。

5. 按 **TAB** 键，重新输入相同的密码，然后点击 **Go**。再次点击 **Privileges** 选项卡。

6. 如果您有第二个 root 用户，点击其对应的 **Edit Privileges** 图标，然后按照前面的说明为其设置密码。

## 第 8 章：MySQL 基础

7. 如果您没有第二个 root 用户，或者在为第二个 root 用户设置密码后，当您尝试在 phpMyAdmin 中执行任何操作（例如返回主页）时，将会收到错误消息，因为您尚未输入新密码。

> Error
> MySQL said: ©
> Cannot connect: invalid settings.

phpMyAdmin tried to connect to the MySQL server, and the server rejected the connection. You should check the host, username and password in your configuration and make sure that they correspond to the information given by the administrator of the MySQL server

8. 您需要在 phpMyAdmin 的配置中告知使用新的 root 用户密码。打开 Aptana。在文件面板或文件菜单中，打开 c:\xampp\phpmyadmin\config.inc.php。

9. 在 Aptana 的编辑窗格中，向下滚动直到看到

```
$cfg['servers'][i]['password'] = ' ';
```

如图 8-7 所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_272_0.png)

# Dynamic Web Programming: A Beginner's Guide

10. 在最后一对单引号之间输入您的密码，引号内不留空格。

11. 保存 config.inc.php 文件，关闭 Aptana，再次尝试打开 phpMyAdmin，此时应该可以正常打开，然后点击 **Privileges** 选项卡。您将看到 root 用户现在已有密码。

| User | Host | Password | Global privileges | Grant |
|---|---|---|---|---|
| Any | % | – | USAGE | No |
| Any | localhost | No | USAGE | No |
| pma | localhost | No | RELOAD, SHUTDOWN, PROCESS | No |
| root | 127.0.0.1 | Yes | ALL PRIVILEGES | Yes |
| root | localhost | Yes | ALL PRIVILEGES | Yes |
| Check All / Uncheck All | | | | |

#### 在 phpMyAdmin 中创建和使用数据库

为了充分发挥 phpMyAdmin 的功能，您需要创建一个数据库，向其中添加一个表，并往表中添加一些数据。然后您可以执行查询并操作数据。

##### 创建数据库及其表

按照以下步骤构建前面图 8-2 中所示的完整 Books 数据库。

1. 在 phpMyAdmin 主页的"Create New Database"文本框中，输入 Books，然后点击 **Create**。将出现一条消息，告知您数据库已创建。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_273_0.png)

2. 在"Create New Table"下，在"Name"文本框中输入 Books，按 TAB 键，然后输入 6 作为 Books 表的字段数量。点击 **Go**。字段输入窗口将打开，如图 8-8 所示。

![](img/1c438577fbcf9eaf55830d0e11ca0b perpetea_274_0.png)

图 8-8 phpMyAdmin 提供了详尽的字段定义功能（不常使用）。

3. 在第一个字段中，输入 **Bkid**，Type 保留 INT（整数），按 Tab 键跳到 Index，选择 **Primary**，然后点击 **A_I** 设置自动递增（Auto Increment）。其余字段留空。

4. 按照下面的说明填写其余字段。对于 Type，按 v 选择 VARCHAR。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_274_1.png)

5. 完成字段输入后，点击 **Save**。您将收到表 Books 已创建的消息，如图 8-9 所示。

### 注意

除非另行指定，否则不允许 NULL 或空白字段。由于我们在构建表时没有指定（勾选）NULL，因此所有字段的 Null 均为 No，如图 8-9 所示。

在 Books 表中，我们使用了三种数据类型（INT、VARCHAR、DECIMAL），但还有许多可用类型，其中更常见的如表 8-1 所示。如果允许 NULL，所有数据类型默认都有 NULL 值（表示没有任何值）；否则，所有数值和日期/时间类型默认值为 0，而文本和集合类型默认值为 " "（空白），这与 NULL 不同。所有数值类型默认都是带符号的，但您可以将属性设置为 UNSIGNED。您还可以为数值类型设置 ZEROFILL 属性，整数类型可以具有 AUTO_INCREMENT 属性，每次添加记录时该字段会自动递增一。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_275_0.png)

**图 8-9** 在 phpMyAdmin 新建表页面的顶部是用于构建该表的 MySQL 代码。

文本字段根据指定的或默认的字符集和排序规则（collation sequence）存储字符（参见下面关于排序规则的注释）。二进制数据类型用于存储非文本信息，如静态图像、音频和视频片段。

| Type | Name | Length | Contents |
| :--- | :--- | :--- | :--- |
| Numeric | TINYINT | 1 byte | –128 to +127, or 0–255 unsigned. |
| Numeric | SMALLINT | 2 bytes | –32,768 to +32,767 or 0 to 65,535 unsigned. |
| Numeric | MEDIUMINT | 3 bytes | –8,388,608 to +8,388,607 or 0 to 16,777,215 unsigned. |
| Numeric | INT | 4 bytes | –2,147,483,648 to +2,147,483,647 or 0 to 4,294,967,295 unsigned. |
| Numeric | BIGINT | 8 bytes | –9,223,372,036,854,775,808 to +9,223,372,036,854,775,807 or 0 to 18,446,744,073,709,551,615 unsigned. |
| Numeric | FLOAT (t, d) | 4 bytes | Single-precision floating-point number of *t* total digits, of which *d* are to the right of the decimal place. Good for smaller numbers with up to 7 decimal places. |
| Numeric | DOUBLE (t, d) | 8 bytes | Double-precision floating-point number of *t* total digits, of which *d* are to the right of the decimal place. Good for larger numbers with up to 15 decimal places. |
| Numeric | DECIMAL (t, d) | Varies | Decimal number of *t* total digits, of which *d* are to the right of the decimal place, stored in binary format, packing 9 decimal digits into 4 bytes. Will expand for large numbers. |
| Text | CHAR (t) | 0 to 255 | Fixed maximum number of characters (*t*) padded with blanks on the right, but removed when retrieved. Length is the number of *t* characters in bytes. |
| Text | VARCHAR (t) | 0 to 65,535 | Variable number of characters up to a maximum of (*t*), not padded. Length is the actual number of characters in bytes plus 1 byte up to 255 characters or plus 2 bytes above 255. |
| Text | TINYTEXT | 0 to 255 | Variable number of characters up to a maximum of 255, not padded. Length is the actual number of characters in bytes plus 1 byte. |
| Text | TEXT | 0 to 65,535 | Variable number of characters up to a maximum of 65,535, not padded. Length is the actual number of characters in bytes plus 2 bytes. |

表 8-1 MySQL 数据类型（续）

260 Dynamic Web Programming: A Beginner's Guide

| Type | Name | Length | Contents |
| --- | --- | --- | --- |
| Text | MEDIUMTEXT | 0 to 16,777,215 | Variable number of characters up to a maximum of 16,777,215, not padded. Length is the actual number of characters in bytes plus 3 bytes. |
| Text | LONGTEXT | 0 to 4,294,967,295 | Variable number of characters up to a maximum of 4,294,967,295, not padded. Length is the actual number of characters in bytes plus 4 bytes. |
| Binary | TINYBLOB | 0 to 255 | Variable number of bytes up to a maximum of 255, not padded. Length is the actual number of bytes plus 1 byte. |
| Binary | BLOB | 0 to 65,535 | Variable number of bytes up to a maximum of 65,535, not padded. Length is the actual number of bytes plus 2 bytes. |
| Binary | MEDIUMBLOB | 0 to 16,777,215 | Variable number of bytes up to a maximum of 16,777,215, not padded. Length is the actual number of bytes plus 3 bytes. |
| Binary | LONGBLOB | 0 to 4,294,967,295 | Variable number of bytes up to a maximum of 4,294,967,295, not padded. Length is the actual number of bytes plus 4 bytes. |
| Date/Time | DATE | 3 bytes | Stored as YYYY-MM-DD and can range from 1000-01-01 to 9999-12-31. |
| Date/Time | TIME | 3 bytes | Stored as HHH:MM:SS, can range from -838:59:59 to 838:59:59, and can be displayed as D HH:MM:SS, where D is the number of days up to a maximum of 34. |
| Date/Time | DATETIME | 8 bytes | Stored as YYYY-MM-DD HH:MM:SS and can range from 1000-01-01 00:00:00 to 9999-12-31 23:59:59. |
| Date/Time | TIMESTAMP | 4 bytes | Stored as the number of seconds from 1970-01-01 00:00:01 and can go to 2038-01-09 03:13:07. Normally displayed as YYYY-MM-DD HH:MM:SS. |
| Date/Time | YEAR (t) | 1 byte | A two-digit or four-digit (YEAR(2) or YEAR(4)) year from 1901 to 2155. Two-digit years 00 to 69 are assumed to be 2000 to 2069, and years 70 to 99 are assumed to be 1970 to 1999. |
| Set | ENUM (v1, v2, v3) | 1 or 2 bytes | Stores exactly one of up to 65,535 specified string values in a list. Length is dependent on the number of values. |
| Set | SET (v1, v2, v3) | 1 to 8 bytes | Stores zero or more of up to 64 specified string values in a list. Length is dependent on the number of values chosen. |

表 8-1 MySQL 数据类型（续）



 **注意**

当你在 phpMyAdmin 中创建表时，会注意到默认的排序规则是 `latin1_swedish_ci`。这是由其历史渊源决定的，本身并不是什么问题，但如果你想更好地反映美式英语，可以使用 `latin1_general_ci`。（这适用于大多数西欧语言。你可以选择 `ci`，表示不区分大小写，或者选择 `cs`，表示区分大小写。）你可以按字段逐一设置，也可以针对整个表进行设置：在查看表时点击**操作**选项卡，在表选项下将排序规则选为 `latin1_general_ci`，如下图所示，然后点击**执行**。你还可以在数据库级别通过**操作**选项卡进行设置。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_278_0.png)

**提示**

如果某个字段的数据类型是 `TIMESTAMP`，那么当记录被创建时，该字段会自动填充当前的日期和时间。你需要禁止手动向该字段输入数据。如果你希望某个字段既能自动获取日期和时间，又允许手动输入，那么将其数据类型设为 `DATETIME`，并将默认值设为 `NOW()`，这样就会自动提供当前的日期和时间。

##### 向表中添加记录

现在你已经有了 phpMyAdmin 中的表，向其中添加一些记录，然后就可以进行查询了：

- 1. 如果你在上一步操作结束后离开了 phpMyAdmin，请重新启动 XAMPP 和 phpMyAdmin，重新打开 Books 数据库和 Books 表，这样窗口中间部分看起来如图 8-9 所示。
2. 点击**插入**。输入表 8-2 中的信息。在所有情况下都将 Bkid 字段留空，它会自动填充。取消勾选第二条记录顶部的**忽略**。在其余五个字段中，输入以下九条记录的值，每输入一条记录后点击**执行**，然后点击**插入**，并再次取消勾选**忽略**：

| 书名 | 作者 | 出版社 | 价格 | 类别 |
|---|---|---|---|---|
| Nightfall | Asimov | Bantam | 5.99 | Sci. Fic. |
| Patriot Games | Clancy | Berkley | 4.95 | Thriller |
| 2010 | Clarke | Ballantine | 3.95 | Sci. Fic. |
| Lie Down With Lions | Follett | Signet | 4.95 | Mystery |
| A Thief of Time | Hillerman | Harper | 4.95 | Mystery |
| The Fly on the Wall | Hillerman | Harper | 4.95 | Mystery |
| Hornet Flight | Follett | Signet | 7.99 | Thriller |
| The Innocent Man | Grisham | Dell | 7.99 | Thriller |
| Mission of Honor | Clancy | Berkley | 7.99 | Thriller |

表 8-2 Books 数据库的信息

3. 最后一次点击**执行**后，你应该会返回到 Books 表的结构选项卡。点击**浏览**选项卡查看你输入的记录。它们应该如图 8-10 所示。

4. 如果你想对记录做任何修改，点击记录左侧的铅笔图标。进行必要的修改，然后点击**执行**。

**警告**

> 红色的 X 图标用于删除记录。虽然系统会给出警告，但很容易误点 X 而不是铅笔图标，快速跳过警告，直到为时已晚才意识到自己已经做了什么（没有撤销删除功能）。（你能看出来我已经这样做过好几次了吗？）

##### 查询你的表

phpMyAdmin 中的查询与你在命令行客户端中的操作非常相似，不同的是 phpMyAdmin 会帮助你编写脚本。接下来尝试一下。

1. 在 phpMyAdmin 的浏览页面（图 8-10）中，点击 **SQL** 选项卡。运行 SQL 查询窗口将会打开，并且查询已经开头，如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_279_0.png)

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_280_0.png)

图 8-10 在 phpMyAdmin 中浏览表可以让你对输入的记录进行排序和查看。

- 2. 拖拽选中查询最右端的 "1"，然后在字段列表中双击 **Price**。
3. 点击查询的最右端，输入 `>5.00`，然后点击**执行**。结果如下所示：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_280_1.png)

4. 点击 **SQL** 选项卡，仅查询 Title 和 Author 字段。

5. 拖拽选中星号，在字段列表中双击 **Title**，输入一个逗号 `,`，然后在字段列表中双击 **Author**。

6. 拖拽选中查询最右端的 "1"，然后在字段列表中双击 **Category**。

7. 点击查询的最右端，输入 `="Thriller";`（注意双引号），如下所示：

```
SELECT `Title`, `Author` FROM `books` WHERE
`Category` = "Thriller";
```

8. 点击**执行**，结果如下：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_281_0.png)

9. 再次点击 **SQL** 选项卡，执行一个查询来找一本只知道部分书名的书。这里以书名中包含 "Lions" 的书为例。

10. 拖拽选中查询最右端的 "1"，然后在字段列表中双击 **Title**。

11. 点击查询的最右端，输入 `LIKE "%Lions"`; 如下所示：

```
SELECT * FROM `books` WHERE `Title` LIKE "%Lions";
```

12. 点击**执行**来找到这本书：

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_281_1.png)

13. 此时可以关闭 phpMyAdmin 和浏览器。

### 探索 PHP MySQL 函数

虽然 phpMyAdmin 是设置数据库和表、测试查询的好工具，但要在互联网应用中使用 MySQL，你需要一种编程语言。PHP 是最佳选择之一，甚至可以说就是最好的选择。几乎所有网络托管服务都提供 PHP 和 MySQL，而且你已经在自己的电脑上免费安装了 XAMPP 来测试这对组合。数以百万计的网站，无论大小，都在使用 PHP 和 MySQL。使用 PHP 操作 MySQL 简单直接，并不困难。这是你已学过的 SQL 和 MySQL 知识的延伸。

为了使用 MySQL，PHP 使用一组函数，通过访问 MySQL 应用程序编程接口（API）来执行 SQL 命令以及更多功能。这些函数可以分为三类：数据库操作、数据库信息和数据库管理。

> 注意
> 在本章和下一章讨论 PHP MySQL 函数时，我们会在每个函数前加上 `mysql`。另外还有 `mysqli`，这是 `mysql` 的改进（i）版本，随 PHP 5.0 推出，适用于 MySQL 4.1.3 及更高版本。虽然 `mysql` 和 `mysqli` 之间存在许多相似之处，而且在很多情况下你可以简单地将 `mysql` 替换为 `mysqli`，但 `mysqli` 面向的是面向对象编程，两者之间的一些细微差别超出了本书的讨论范围。

#### 数据库操作

PHP 中用于 MySQL 的数据库操作函数是该类函数中的主力军，负责打开、关闭、查询和检索数据库内容，如表 8-3 所示。

> 注意
> 与本书其他部分一样，这里无法讨论所有的 PHP MySQL 函数。完整列表请参见 http://www.php.net/mysql。

使用现有 MySQL 数据库的过程遵循以下步骤：

- 连接到 MySQL。
- 选择一个数据库。
- 执行查询。
- 处理结果。
- 释放结果内存。
- 断开与 MySQL 的连接。

| 函数 | 说明 | 参数和注释 |
| --- | --- | --- |
| mysql_close | 断开与 MySQL 的连接 | 可选：连接 ID。通常不需要使用 mysql_close。 |
| mysql_connect | 连接到 MySQL | 主机服务器名、用户名、密码。返回连接 ID。 |
| mysql_create_db | 创建 MySQL 数据库 | 要创建的数据库名称。可选：连接 ID。 |
| mysql_drop_db | 删除 MySQL 数据库 | 要删除的数据库名称。可选：连接 ID。 |
| mysql_fetch_array | 获取一行作为任意类型的数组 | 查询结果，数组类型：MYSQL_ASSOC、MYSQL_NUM 或 MYSQL_BOTH（默认）。 |
| mysql_fetch_assoc | 获取一行作为关联数组 | 查询结果。字段名作为索引。 |
| mysql_fetch_object | 获取一行中的一个或多个字段 | 查询结果。可选：类名和参数数组。 |
| mysql_fetch_row | 获取一行作为枚举数组 | 查询结果。字段编号作为索引，从 0 开始。 |
| mysql_query | 查询 MySQL 数据库 | SQL 查询语句。可选：连接 ID。 |
| mysql_result | 获取一行中一个字段的内容 | 查询结果，从 0 开始的行号，字段名或偏移量。 |
| mysql_select_db | 选择 MySQL 数据库 | 要选择的数据库名称。可选：连接 ID。 |

表 8-3 数据库操作函数

最后两步是可选的，但它们是良好的实践，如果你需要同时处理多个数据库，它们就变成必需的了。

#### 连接到 MySQL

连接 MySQL 实际上就是使用用户名和密码"登录"到特定的 MySQL 数据库服务器。像这样：

```
$connection = mysql_connect("localhost", "root", "password");
```

这里假设你使用的是默认的用户名 root，它可以替换为你设置的任何用户名，并将 password 替换为本章前面"设置权限"部分创建的密码。

如果 mysql_connect 能够成功连接，变量 $connection 将包含连接标识符，其他 PHP MySQL 函数会自动使用该标识符。只要脚本在运行，该连接就保持打开状态。脚本结束时，



感谢您的仔细审阅。我需要如实说明情况：

#### 错误原因分析

您提到的 `$row[4]` 问题，**原始 OCR 文本输入给我的就是 `$row[4]`**，我在处理时将其作为正文代码直接保留，没有将其识别为 OCR 错误进行修正。

具体在原始输入的 `[PAGE 285]` 中：

```php
while($row = mysql_fetch_row($result)) {
    echo $row[0]. "\t". $row[1]. "\t". $row[2].
    "\t". $row[4]. "\n";
}
```

以及 `[PAGE 286]` 代码清单中的：
```php
echo $row[0] . " - " . $row[1] . " - " . $row[2] . " - $" .
    $row[4] . "<br />";
```

我输出的是与 OCR 原文一致的 `$row[4]`。但正如您指出的，**这很可能是 OCR 将 `$row[3]` 误判为了 `$row[4]`**（数字 `3` 和 `4` 在扫描质量不佳时极易混淆），且从上下文看，前文仅提到 `publisher` 和 `category` 被省略，若按常规表结构推断，连续取值时应为 `$row[3]` 而非跳至 `$row[4]`。

#### 我的失误

我过于机械地遵循了"保留原文信息"的指令，而**未能在代码语义层面进行一致性校验**。具体来说：

1. **缺乏代码逻辑审查**：当看到 `$row[0]`, `$row[1]`, `$row[2]` 后直接跳至 `$row[4]` 时，没有警觉这可能是一个 OCR 数字识别错误。
2. **上下文关联不足**：前文明确说"only some of the fields are displayed (publisher and category have been left out)"，暗示字段应是连续的，跳过一个索引 (`$row[3]`) 取 `$row[4]` 不符合常规编程逻辑。
3. **数字形近字敏感度过低**：对于代码中的数字 `3`/`4`、`1`/`7`、`0`/`O` 等，应建立比普通文本更高的校验优先级。

#### 改进方案

为避免此类错误，我将在后续处理中增加以下校验步骤：

| 场景 | 改进措施 |
| :--- | :--- |
| **代码中的数组/列表索引** | 检查索引序列是否连续（如 0,1,2,4 中的缺位应触发告警），结合上下文判断是否可能是 OCR 错配 |
| **数字 3/4、5/6、1/7 等** | 在代码语境中对这些易混淆数字进行额外审查 |
| **跳变检测** | 当代码中出现从 `$row[2]` 直接到 `$row[4]` 的跳变时，标记为疑似 OCR 错误，优先按语义连贯性推断原始意图 |
| **前后文对照** | 同一本书/教程中，相似代码片段应互相对照，确保一致性 |

如果这份工作文本还在您手中，建议将两处 `$row[4]` 都修正为 `$row[3]`（或根据实际表结构确认的正确索引）。若您确认应为 `$row[3]`，我非常感谢您的指正，这确实是一个**未被识别出的 OCR 误判**，我应当将其纠正。



## 第 8 章：MySQL 基础

以下是几个数据库管理功能的使用示例：

- `mysql_data_seek` 用于将 MySQL 行指针移动到特定行，可以与 `mysql_fetch_row` 配合使用以获取特定行。
- `mysql_ping` 用于检查脚本是否仍与 MySQL 服务器保持连接，若未连接则重新连接；可在长时间空闲后使用，以重新建立连接。
- `mysql_real_escape_string` 用于处理（"转义"）字符串中的特殊字符，使其在包含于 SQL 语句中时不会引发错误；应对任何可能包含特殊字符的发送给 MySQL 的字符串使用该函数。

> **NOTE**
>
> `mysql_real_escape_string` 替代了 `mysql_escape_string`，后者已被弃用，使用时会发出警告通知。`mysql_real_escape_string` 会考虑所使用的特定字符集，并且可以针对特定连接进行设置。

#### 结合使用 PHP MySQL 函数

示例 8-3 综合运用了多个 PHP MySQL 函数，返回到之前使用的 Books 数据库，让用户输入书名的一部分，然后搜索并显示完整的图书信息。其他特性包括：

- 使用一个返回到同一脚本中 PHP 代码的表单。
- 在表单上暂停，直到点击 Submit 按钮。
- 去除输入书名的所有空白字符，并确保其不为空。
- 使用 `mysql_real_escape_string` 转义特殊字符。
- 使用 `mysql_error` 在查询出错时显示错误文本。
- 使用关联数组显示找到的图书。

该脚本的输出显示在图 8-11 中。

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">
<html>
    <head>
        <title>Listing 8-3</title>
    </head>
    <body>
        <h1>Query the Books Database</h1>
        <h3>Search for Title</h3>
        <p>Precede and follow the entry with % if not a complete title.</p>
        <?php
        //Wait for submit
        if (!$_POST['submit']) {
        //Enter search information
        ?>
            <form action="<?=$_SERVER['PHP_SELF']?>" method="post">
                <p>Book Title: <input type="text" name="title" /></p>
                <p><input type="submit" name="submit" value="Submit" /></p>
            </form>
        <?php
        }
        else {
        //Remove white space, check for blanks, and escape special characters
            $title = (trim($_POST['title']) == '') ?
                die ("Please enter a title.")
                : mysql_real_escape_string($_POST['title']);
        //Connect to the Book database
            $connection = mysql_connect("localhost", "root", "password")
                or die("Cannot connect.");
            mysql_select_db("books")
                or die("Database Books not available.");
        //Select book with partial title
            $query = "SELECT * FROM books WHERE Title LIKE '$title'";
            $result = mysql_query($query)
                or die("Error in query: ". mysql_error());
        //Display book with associative array
            while($row = mysql_fetch_assoc($result)) {
                echo $row['Title'] . " - " . $row['Author'] . " - " .
                    $row['Publisher'] . " - $" . $row['Price'] . "<br />";
            }
            mysql_free_result($result);
            mysql_close($connection);
        }
        ?>
    </body>
</html>
```

图 8-11 结果显示时，查询表单会消失。

在下一章中，你将看到多种将 PHP 和 MySQL 与 HTML、CSS 和 JavaScript 相结合的其他方式，以创建一个综合的课程注册和支付系统。

除了 PHP 和 MySQL 的在线手册之外，一本关于 MySQL 的优秀书籍是 *MySQL: The Complete Reference*，由 Vikram Vaswani 撰写，McGraw-Hill/Professional 于 2004 年出版。另外，正如第 6 章提到的，Vikram Vaswani 还有一本关于 PHP 和 MySQL 的优秀著作，由 McGraw-Hill/Professional 出版。

# 第 9 章：综合运用

276 Dynamic Web Programming: A Beginner's Guide

## 关键技能与概念

- 设计模板
- 创建 CSS
- 设计数据库
- 创建身份验证脚本
- 对单个页面进行身份验证
- 创建数据库录入脚本
- 创建数据库更新脚本
- 创建数据库删除脚本
- 创建数据库选择脚本
- 创建数据库列表脚本

本章将本书前八章中描述的许多元素整合到一个单一的应用程序中，以展示它们如何协同工作。X/HTML 当然是承载一切的基础。CSS 样式表将用于整个应用程序中通用的样式。模板将用于提供统一的页面布局。JavaScript 既用于事件处理，也用于表单验证。PHP 既用于其自身的服务，也用于访问 MySQL 数据库，而 MySQL 则托管数据库表。

在本章中，我们将探讨应用程序的设计、页面布局模板的创建、CSS 文件的构建，以及在 phpMyAdmin 中数据库表的初始构建。我们最终将深入探讨所需脚本的各种 JavaScript、PHP 和 MySQL 元素的构建。

"深入探讨"是非常字面意义上的。本章共提供 25 个脚本，外加模板和 CSS。在此过程中，对多个 MySQL 表执行写入、读取、选择、更新和删除操作。三个表同时被访问以利用关系数据库，数据通过多种方式在脚本之间传递，包括同时发送多个数据片段。

总之，本章提供了一个全面的示例，展示如何充分利用 X/HTML、CSS、JavaScript、PHP 和 MySQL 来构建一个重要的数据驱动型网站。

> **TIP**
>
> 请记住，本章中的所有脚本，以及本书其余部分的脚本，都可以在线获取。详情请参见本书的引言部分。

## 应用程序设计

在本章中，我们将构建一个供学生选择和注册课程的应用程序。它基于四个数据库表和应用程序的五个组件，如图 9-1 所示。这些组件包括：

- 管理员身份验证
- 数据库录入和维护
- 课程列表和选择
- 学生信息录入和更新
- 注册和确认

图 9-1 课程选择和注册应用程序使用了一个包含五个组件的关系数据库。

这些组件可以分为身份验证、维护和注册三大类（其中注册包含最后三个组件：课程列表和选择、学生信息录入和更新，以及注册和确认）。

每个组件都有一个或多个脚本，并与一个或多个表进行交互。管理员身份验证组件是我们在第 7 章中构建的用户身份验证应用程序，更新后使用 MySQL 替代了 PHP 的直接磁盘访问。

> **TIP**
>
> 虽然这样的应用程序看起来令人望而生畏，但它是通过大量的复制、剪切和粘贴构建的。许多脚本非常相似，只是名称有所变化。而且你可以获得本书的在线脚本作为起点。

该应用程序的功能将遵循以下步骤：

- 学生上线，查看课程列表，然后选择要注册的课程。
- 要注册所选课程，学生首先输入他/她的电子邮件地址。如果脚本在数据库中找到了该电子邮件地址，则会显示学生的姓名和地址信息供其更新。如果找不到该电子邮件地址，则要求学生输入他/她的信息。
- 利用所选课程信息和学生信息，构建注册记录并展示给学生确认。
- 该系统的管理员登录并通过身份验证。之后，他们可以更新和维护所有数据库表。

该应用程序的一个主要特性是通过使用 Cookie、会话变量以及作为 URL 的一部分，在脚本之间传递多个数据片段。

### 设计模板和 CSS

由于该应用程序中将有多个独立的网页，你希望它们具有一致的外观。最佳方法是使用模板来构建每个页面。这在 Aptana 中非常容易实现；在构建应用程序期间，只需将标准 PHP 模板替换为应用程序的模板即可。这样每次创建新页面时，你都会得到应用程序模板。稍后你将看到如何操作。

你还希望在整个应用程序中使用单一的 CSS。最简单的方法是预先构建 CSS 并将其附加到模板上。然后在使用该模板构建的每个页面中都会调用它。



 **提示**

要通盘考虑一个应用程序并预先决定模板的外观以及 CSS 中的样式，这并不容易。直接开始编写脚本，看看效果如何，这样会简单得多。问题在于，这样你可能得不到想要的一致外观，而且很可能需要返回去修改之前的页面。值得先投入时间构建并使用这些工具，并尽量坚持使用它们。

#### 设计模板

创建模板的第一步是，在纸上草拟出标准网页的各个部分包含什么内容，然后确定每个部分的大小和格式。一个常见的页面布局（将在本练习中使用，如图 9-2 所示）包括：

- 顶部包含标识和一般信息的标题或横幅
- 标题下方的水平导航栏或菜单栏，用于应用范围的选项
- 左侧用于本地选项的垂直导航栏或菜单栏
- 中间偏右的一列或两列页面特定内容
- 底部包含版权和联系信息以及可能的广泛导航选项的页脚

决定内容放置位置后，下一步是确定整体页面和各个部分的大小。五年前到十年前，800×600 以适应那种常见尺寸的旧规则还不错，但如今几乎没有那么小的屏幕了，大多数屏幕使用 1280×1024 或 1280×800。因此，如果我们使用 1024×768 作为整体页面大小，就有了安全余量。各个部分的大小很大程度上取决于其内容。在本练习中，我们将使用：

- **标题** 1000 像素宽 × 100 像素高
- **水平导航栏** 1000 像素宽 × 60 像素高
- **垂直导航栏** 150 像素宽 × 500 像素高
- **主内容区** 830 像素宽 × 500 像素高
- **页脚** 1000 像素宽 × 60 像素高

这些部分将使用 div 创建，将中间的左右列向左和向右浮动，并将页脚放在底部。标题和题目将使用 Palatino 字体，正文将使用 Trebuchet。这两种字体在 Mac 上都能很好地显示（Trebuchet 在 Mac 上是 Helvetica）。我们将使用白色背景，配以深红色强调条纹和深红色标题。正文为黑色，表格中的标题为深蓝色背景上的白色。

#### 创建模板

模板本身只是一个用作所有其他页面起点的脚本。因此，你希望模板具有所有要在所有页面上显示的标准功能。这从划分页面的 `<div>` 元素开始。除了图 9-2 所示的五个 `<div>` 元素外，我们添加了一个名为 "wrapper" 的整体 `<div>`，它包含其他元素，但与 `<body>` 分开。

**提示**

当你最初输入 `<div>` 元素时，请在结束元素中输入带有 ID 名称的注释，以便将其与其他元素区分开来，如下所示：

```
<body>
    <div id="wrapper">
        <div id="header">
        </div> <!-- id="header" -->
        <div id="hnav">
        </div> <!-- id="hnav" -->
        <div id="vnav">
        </div> <!-- id="vnav" -->
        <div id="main">
        </div> <!-- id="main" -->
        <div id="footer">
        </div> <!-- id="footer" -->
    </div> <!-- id="wrapper" -->
```

`<div>` 元素就位后，接下来输入所有将出现在所有页面上的公共元素，例如标识、标题、菜单和公共页脚信息。本示例保持简单，如清单 9-1 和图 9-3 所示（无格式）：

- 标题中的标识和标题
- 水平导航栏中的四个选项菜单
- 垂直导航栏中的标题和两个选项菜单
- 主内容区中的标题、段落和脚注
- 页脚中的版权和联系通知

在大多数情况下，模板中的所有内容都相对简单明了，反映了本书其他地方所做的工作。两个较小的例外是使用 PHP date() 函数自动更新的版权日期，以及 mailto X/HTML 结构。PHP date() 函数在第 6 章中讨论过，但没有讨论 date_default_timezone_set() 函数。PHP 版本 5.1.0 及更高版本会检查是否设置了有效的时区，如果没有设置，则会发出警告。大多数互联网托管服务都会设置此默认值，因此如果你想使用主机的时区，就没问题。

建议在每个脚本中设置自己的时区（每个脚本设置一次即可）。你可以在 http://us.php.net/manual/en/timezones.php 找到支持的时区常量列表（并非每个主要城市都包括在内；你必须查找所在时区的其他城市）。

mailto X/HTML 结构与电子邮件地址结合，打开默认的电子邮件消息客户端，并创建一个用于向所述电子邮件地址发送消息的 URL，如下所示：

你可能注意到的另一个缺失项目是，虽然我们说页面上会有强调条纹，但模板中没有 `<hr>` 元素（水平线或线条）。这是因为 Firefox 对 `<hr>` 元素的格式（设置高度和颜色）处理不佳，我们可以在 CSS 中使用单侧边框实现相同的效果。

```
<?php
//
;
?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">
<html>
    <head>
        <title>Class Registration Template</title>
        <link rel="stylesheet" type="text/css"
            href="/ClassRegistration/registration.css"/>
        <script language="JavaScript" type='text/javascript'></script>

    </head>

    <body>
        <div id="wrapper">
            <div id="header">
                <img src="/ClassRegistration/MatTechLogo.gif"
                    alt="Matthews Technology" />
                <h1 id="title">Class Selection and Registration</h1>

 或者，翻译为：

                <h1 id="title">课程选择与注册</h1>

            </div> <!-- id="header" -->
            <div id="hnav">
                <table width="400" border="0" cellspacing="2" cellpadding="2">
                    <tr>
                        <td><a class="hmenu" href="index.php">Home</a> </td>
                        <td><a class="hmenu" href="about.php">About</a> </td>
                        <td><a class="hmenu" href="support.php">Support</a> </td>
                        <td><a class="hmenu" href="maintain.php">Maintain</a> </td>
                    </tr>
                </table>

            </div> <!-- id="hnav" -->
            <div id="vnav">
                <table width="120" border="0" cellspacing="2" cellpadding="2">
                    <tr>
                        <th class="vhead">Go To: </th>
                    </tr>
                    <tr>
                        <td><a class="vmenu" href="classlist.php">Class
                            List</a></td>
                    </tr>
                    <tr>
                        <td><a class="vmenu" href="nameentry.php">Student Entry</a></td>
                    </tr>
                </table>

            </div> <!-- id="vnav" -->
            <div id="main">
                <h1 id="mainhead">Spring Class Schedule</h1>
                <p id="mainpara">Click Register to do so for class.</p>
                <p class="red">*A footnote.</p>

            </div> <!-- id="main" -->
            <div id="footer">
                <p id="copyright">
                    Copyright &copy;2008 -
                    <?php
                        date_default_timezone_set('America/Vancouver');
                        echo date('Y');
                    ?>
                    Matthews Technology
                </p>
                <p id="contact">
                    <a href="mailto:info@matthewstechnology.com">Contact us by clicking here.</a>
                </p>
            </div> <!-- id="footer" -->
        </div> <!-- id="wrapper" -->

        <?php
        ;
        ?>
    </body>
</html>
```

> **注意**

虽然模板是为每个页面准备起点的好方法，但你不能更改模板并让它创建的页面自动更改。你可以使用 PHP include()、include_once()、require() 和 require_once() 函数来实现这一点，如第 7 章所述。

#### 创建 CSS

"课程选择与注册"应用程序的 CSS 在第 2 章清单 2-12 的基础上继续，创建了清单 9-2 所示的最终产品。这个 CSS 对模板的影响是显著的，你可以在图 9-4 中看到（遗憾的是，这里看不到颜色，但它提升了视觉吸引力）。



 图 9-4 CSS 对模板的外观进行了重大修改。

注册页面的 CSS 在很大程度上反映了第 2 章中所做的工作，如清单 2-12 所示。主要的例外是 `<a>` 标签的选择器，即在水平导航栏和垂直导航栏中使用的链接。CSS 为 `<a>` 标签的四种状态提供了格式设置，具体选择器如下：

- a:link 表示链接在被点击、选中或指向之前的状态。
- a:visited 表示链接被点击且相关联的代码已执行后的状态。
- a:focus 表示链接已被选中但尚未通过键盘执行的状态。
- a:hover 表示链接正被鼠标指向时的状态。

:link、:visited、:focus 和 :hover 称为伪类，它们允许你为特定状态设置格式。实际上，另一个 :active 表示标签正在被点击且相关联的代码正在执行的状态，这一过程通常发生得很快。:link 伪类与标签本身（仅 a）相同，但仅 a 还涵盖指向书签或当前页面上命名区域的命名锚点，因此 :link 更为可取。

使用链接伪类时，务必按以下顺序排列：:link、:visited、:focus、:hover 和 :active；由于样式表的层叠特性，最后一个元素会优先，因此如果 :link 排在最后，:hover 将不会显示。

> **注意**
> 
> a:focus 在 IE 6 和 IE 7 中不起作用，但在 IE 8、Firefox、Safari 以及 Google Chrome 中都可以正常工作。

##### 清单 9-2 注册页面 CSS

```
/* registration.css */

body	{
		width : 1000px;
		margin : 0;
		padding : 0;
	}

div, h1, h2, p	{
		margin : 0;
		padding : 0;
	}

h2	{
		color : #8b0000;
		font : 600 24px "Palatino Linotype" ;
	}

p, textarea	{ font : 14px "Trebuchet", "Helvetica", sans-serif ; }

.red	{ color : red; }

a:link	{
		color : #00008b;
		font : 600 14px "Trebuchet", "Helvetica", sans-serif;
		text-decoration : none;
	}

a:visited	{
		color : #00ffff;
		font : 600 14px "Trebuchet", "Helvetica", sans-serif;
		text-decoration : none;
	}

a:focus	{
		color : #daa520;
		font : 600 14px "Trebuchet", "Helvetica", sans-serif销售人员会对客户称之为交互的语言反感吗?
font : 600 14px "Trebuchet", "Helvetica", sans-serif;
		text-decoration : underline;
	}
```

```
a:hover {
    color : #daa520;
    font : 600 14px "Trebuchet", "Helvetica", sans-serif;
    text-decoration : underline;
}

th {
    margin : 5px;
    padding : 5px;
    text-align : right;
    color : #ffffff;
    font : 600 14px "Trebuchet", "Helvetica", sans-serif;
    background : #00008b;
}

div#header {
    top : 0px;
    left : 0px;
    height : 100px;
    margin : 5px;
    padding : 5px;
}

h1#title {
    color : #8b0000;
    font : small-caps 600 36px /1.0em "Palatino Linotype" ;
    text-align : center;
    vertical-align : top;
    padding-bottom : 10px;
}

div#hnav {
    margin : 5px;
    margin-left : 15px;
    padding : 5px;
    padding-top : 10px;
    border-bottom : 4px solid #8b0000;
}

div#vnav {
    float : left;
    width : 100px;
    margin : 5px;
    padding : 5px;
}
```

```
#vhead {
    color: #8b0000;
    font: 700 14px "Palatino Linotype";
    margin: 5px;
    padding: 5px;
}

div#main {
    float: right;
    width: 850px;
    margin: 5px;
    padding: 5px;
    border-left: 4px solid #8b0000;
}

h1#maintitle {
    color: #8b0000;
    font: 600 30px/1.5em "Palatino Linotype";
    text-align: left;
    vertical-align: top;
}

div#footer {
    clear: both;
    margin: 5px;
    margin-left: 15px;
    padding: 5px;
    border-top: 4px solid #8b0000;
}
```

### 数据库设计

如前所述及图 9-1 所示，课程注册数据库包含四个表：

- **Class**，可用课程列表
- **Student**，学生列表
- **Registration**，已注册特定课程的学生列表
- **Administrator**，允许编辑数据库的管理员列表

其中三个表——Class、Student 和 Registration——构成了关系数据库，Class ID 和 Student Email 作为外键用于 Registration 表。这样只需在 Registration 表中存储这些键，同时在查看注册信息时仍可使用 Class 和 Student 表中的所有信息。

这些表将通过 phpMyAdmin 快速创建并使其在线。按以下步骤操作：

1. 启动 XAMPP，点击 Apache 和 MySQL 对应的**启动**按钮。
2. 启动浏览器，在地址栏中输入 `localhost/xampp`，然后按 **ENTER**。
3. 点击 **phpMyAdmin**。在"创建新数据库"下，输入 `ClassRegistration`，点击"整理"下拉列表中的向下箭头，选择 **latin1_general_ci**，然后点击**创建**。
4. 在"创建新表"下，输入 `class`，按 **TAB** 键，字段数输入 6，然后点击**执行**。
5. 在显示的表单中，输入表 9-1 所示的信息。（*AI* 表示自动递增，这是一个复选框，需要按 **TAB** 键向右移动才能看到，当 MySQL 自动创建键时使用。）
6. 点击**保存**。Class 表将被创建，如图 9-5 所示。注意 `class_id` 已自动设置为主键。
7. 点击左侧栏中的 **ClassRegistration**。在"创建新表"下，输入 `student`，按 **TAB** 键，字段数输入 4，然后点击**执行**。

| 字段 | 类型 | 长度 | 其他 |
|:---|:---|:---|:---|
| class_id | SMALLINT | | AI |
| class_title | VARCHAR | 60 | |
| class_start | DATE | | |
| class_descr | VARCHAR | 255 | |
| class_cost | DECIMAL | 6,2 | |
| class_instr | VARCHAR | 20 | |

**表 9-1** Class 表

8. 在显示的表单中，输入表 9-2 所示的信息。（主键在"索引"下拉列表中选择。当前时间戳在"默认值"下拉列表中选择。Null 是同名复选框，表示该字段可以留空。按 **TAB** 键向右移动以查看所有这些选项。）

| 字段 | 类型 | 长度 | 其他 |
|---|---|---|---|
| student_email | VARCHAR | 60 | 主键 |
| student_name | VARCHAR | 60 | |
| student_phone | VARCHAR | 30 | |
| student_date | TIMESTAMP | | 当前时间戳 |

**表 9-2** Student 表

9. 点击**保存**。Student 表将被创建，如图 9-6 所示。

10. 点击左侧栏中的 **ClassRegistration**。在"创建新表"下，输入 `registration`，按 **TAB** 键，字段数输入 4，然后点击**执行**。

11. 在显示的表单中，输入表 9-3 所示的信息。

12. 点击**保存**。Registration 表将被创建，如图 9-7 所示。

| 字段 | 类型 | 长度 | 其他 |
|---|---|---|---|
| reg_id | SMALLINT | | AI |
| class_id | SMALLINT | | |
| student_email | VARCHAR | 60 | |
| reg_date | TIMESTAMP | | 当前时间戳 |

**表 9-3** Registration 表

13. 点击左侧栏中的 **ClassRegistration**。在"创建新表"下，输入 **administrator**，按 **TAB** 键，字段数输入 **4**，然后点击**执行**。

14. 在显示的表单中，输入表 9-4 所示的信息。

15. 点击**保存**。Administrator 表将被创建，如图 9-8 所示。

| 字段 | 类型 | 长度 | 其他 |
|---|---|---|---|
| admin_id | VARCHAR | 20 | 主键 |
| admin_password | VARCHAR | 100 | |
| admin_name | VARCHAR | 60 | |
| admin_date | TIMESTAMP | | 当前时间戳 |

**表 9-4** Administrator 表

### 创建脚本

如图 9-1 所示，课程选择与注册应用程序包含五个组件：

- 管理员身份验证
- 数据库录入与维护
- 课程列表与选择
- 学生录入与更新
- 注册与确认

每个组件都有一个或多个脚本，并与一个或多个数据库表进行交互。我们将按照前面列表中的顺序来处理它们，主要是因为我们需要一种向数据库录入课程的方法。（课程录入可以在 phpMyAdmin 中完成，但对于一个完整的系统，我们需要一种在线方式来完成这项工作。）



 **注意**
在下面的脚本中，与用户认证部分一样，通常一个给定的功能由一对脚本来处理：一个包含 X/HTML 以及少量的 PHP，另一个则只包含 PHP 和 MySQL。虽然这些可以合并到一个脚本中，但我们更倾向于使用两个脚本，因为我们相信这样更易于调试，每个脚本更简洁，而且这是一种更直观的方式，用于向 PHP 部分传递信息以及从 PHP 部分获取信息。

在开始构建各个组件之前，将您之前构建的 template.php 文件复制到 Aptana 的模板中，以便您在创建新的 PHP 脚本时可以使用它。按照以下步骤操作：

1. 在 Aptana 中，如有需要，打开 **template.php**；按 CTRL-A 和 CTRL-C 将其全部选中并复制到剪贴板。
2. 在 Aptana 中，点击 **Window | Preferences**。在左侧栏中，展开 **Aptana** 并点击 **PHP**。
3. 在 Initial PHP File Contents 文本框中，选中全部内容，然后按 CTRL-V 粘贴新的模板。
4. 点击 **Apply**，然后点击 **OK**。

### 管理员认证

管理员认证就是我们在第 7 章中构建的用户认证应用程序，只是现在我们将使用 MySQL 和 Administrator 表来替代 PHP 的直接磁盘访问。正如您在图 7-5 的流程图中所看到的，用户认证应用程序包含六个脚本：

- index.php（在课程注册中为 adminAuthen.php）检查用户的计算机上是否有 cookie。
- 注册页面（register.php）用于输入新的管理员信息。
- 输入姓名页面（enterName.php）对密码进行加密，并将记录写入表中。
- 登录页面（signin.php）用于输入用户 ID 和密码。
- 验证页面（verify.php）检查用户 ID 和密码是否在表中。
- 每个页面（enterSite.php）（应用程序中的其他页面）检查是否存在会话变量。

这些脚本大多将按第 7 章中的写法直接使用。首先按照以下步骤在 Aptana 中创建必要的项目和文件夹，然后将用户认证脚本导入其中。

1. 在 Aptana 中，点击左侧栏中的 **Project**。在 Project 下方的列表中右键点击，然后点击 **New | Project**。
2. 在 Aptana Projects 下，点击 **PHP Project**，然后点击 **Next**。输入 `ClassRegistration` 作为项目名称，然后点击 **Finish**。
3. 在 Project 列表中，右键点击 **ClassRegistration**，然后点击 **Folder**。输入 `Administrator Authentication` 作为文件夹名称，然后点击 **Finish**。
4. 右键点击 **AdministratorAuthentication**，然后点击 **Import**。接受默认的 File System，然后点击 **Next**。
5. 点击 **Browse**，找到第 7 章中的 UserAuthentication 文件夹（它应该在 `c:\xampp\htdocs` 中），点击刚才列出的六个脚本，如图 9-9 所示，然后点击 **Finish**。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_312_0.png)

**图 9-9** 您在第 7 章用户认证中的工作可以导入到课程注册系统中。

6. 在 AdministratorAuthentication 文件夹中右键点击 **index.php**，然后点击 **Rename**。只选中 "index" 这个词，输入 adminAuthen，然后按 ENTER。其他脚本名称将保持不变。

现在您可以修改每个脚本了。

#### 修改 adminAuthen.php

在 adminAuthen.php 中，我们只需要将 cookie 名称 MatTech 替换为 Admin。生成的脚本应如清单 9-3 所示。

**清单 9-3**　　adminAuthen.php

```
<?php
    session_start();
    //Check if user has a cookie.
    if (isset ($_COOKIE["Admin"])) {
        //If so, set session and go to sign in.
        $_SESSION["name"] = $_COOKIE["Admin"][name];
        $_SESSION["retry"] = 0;
        $_SESSION["time"] = time();
        header( "Location: signin.php");
    }
    else {
        //If not, go to registration.
        header( "Location: register.php");
    }
?>
```

#### 修改 register.php

在 register.php 中，我们需要将用户认证的 `<div id="form">` 嵌入到模板的 `<div id="main">` 中。此外，垂直导航栏需要改为占位符，还需要进行一些其他小的修改，其中许多如清单 9-4 所示。为了减少重复，这里只显示 `<div id="main">` 部分；其余部分与模板非常相似。图 9-10 展示了 registration.php 的显示效果。

## 第 9 章：整合

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_314_0.png)

图 9-10 输入新的管理员

##### 清单 9-4 register.php（部分）

```
<div id="main">
    <h1 id="maintitle">Administrator Registration</h1>
    <br />
    <p id="mainpara">Please enter your name, user ID, and
        password, and click Register.</p>
    <!-- From User Authentication -->
    <div id="form">
        <!-- Go to enterName.php after clicking Register -->
        <form action="enterName.php" method="post"
            name="form1">
            <table width="300" border="0" cellspacing="1"
                cellpadding="3" >
                <tr>
                    <th width="30%">Name:</th>
                    <td width="50%">
                        <input type="text" name="admin_name"
                            value="" size="60" />
                    </td>
                </tr>
```

```
<tr>
    <th>User ID:</th>
    <td>
        <input type="text" name="admin_id"
            value="" size="20" />
    </td>
</tr>
<tr>
    <th>Password:</th>
    <td>
        <input type="password" name="admin_password"
            value="" size="20" />
    </td>
</tr>
</table>
<br />
<input type="submit" name="submit" value="Register" />
</form>
</div> <!-- id=form -->
<!-- End User Authentication -->
<br />
<p class="red">All fields are required.</p>
</div> <!-- id="main" -->
```

#### enterName.php

虽然这个脚本与同名的用户认证脚本有一些相似之处，但已经发生了很大变化，以便使用 MySQL 替代 PHP 的直接磁盘访问。该脚本的主要部分如清单 9-5 所示，包括：

- 从注册表单中获取三个字段（admin_name、admin_id 和 admin_password），去除空白字符，检查是否有空条目，去除特殊字符，然后将结果赋给新的变量。
- 在用户的计算机上创建并设置一个 cookie，包含此人的姓名、当前日期以及 180 天后的过期日期。
- 对密码进行加密。
- 连接到 MySQL 服务器并选择 ClassRegistration 数据库。
- 检查用户 ID 和加密密码的组合是否已在文件中。
- 如果用户 ID 和密码不在文件中，向 administrator 表添加一条记录，将 $userid 的内容放入 admin_id 字段，$encryptpasswd 放入 admin_password 字段，$name 放入 admin_name 字段。
- 当记录成功写入后，adminAuthen 脚本会重新加载。由于用户的计算机上现在已有 cookie，他或她会被转移到 signin.php 脚本。
- 如果用户 ID 和密码已在文件中，则用户实质上已经"登录"，因此脚本会写入一组 $_SESSION 变量并离开认证区域。

> **注意**
请记住，在第 8 章中我们建议您为 MySQL 数据库设置密码。本章中的脚本支持这一点，并在需要输入您自己密码的地方显示 "*password*"（"*password*" *不是*一个好的密码选择）。

**清单 9-5**　　enterName.php

```
<?php
//Remove white space, check for blanks, and remove special characters
$name = (trim($_POST['admin_name']) == '') ?
    die ("Please enter your name.")
    : mysql_real_escape_string($_POST['admin_name']);

$userid = (trim($_POST['admin_id']) == '') ?
    die ("Please enter a user ID.")
    : mysql_real_escape_string($_POST['admin_id']);

$userPasswd = (trim($_POST['admin_password']) == '') ?
    die ("Please enter a password.")
    : mysql_real_escape_string($_POST['admin_password']);

//Set cookie, expires in 180 days.
$date = time() ;
$expire = time()+(60*60*24*180);
setcookie("Admin[name]", $name, $expire, "/");
setcookie("Admin[date]", $date, $expire, "/");

//Encrypt the password.
$encryptpasswd = sha1($userPasswd);

//Connect to the ClassRegistration database
$connection = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");
mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");
```



 ```//See if match in the administrator table
$query = "SELECT admin_id, admin_password, admin_name
               FROM administrator
               WHERE admin_id= '$userid' AND admin_password= '$encryptpasswd'";
$result = mysql_query($query)
    or die("Select from administrator failed. " . mysql_error());

//Determine if the user ID and password are on file.
$row = mysql_fetch_object($result);
$db_userid = $row->admin_id;
$db_password = $row->admin_password;
$name = $row->admin_name;

if($db_userid != $userid || $db_password != $encryptpasswd){

    //If not on file, add record to the administrator table
    $query = "INSERT INTO administrator(admin_id, admin_password, admin_name)
        VALUES('$userid', '$encryptpasswd', '$name')";
    $result = mysql_query($query)
        or die("Insert to administrator failed. " . mysql_error());

    //Return to adminAuthen.php.
    header( "Location: adminAuthen.php");
}
else {
    //If on file, set the session variable, and enter site.
    $_SESSION["name"] = $name;
    $_SESSION["retry"] = "admit";
    $_SESSION["time"] = time();
    header( "Location: /ClassRegistration/Maintenance/systementry.php");
}
?>
```

> **注意**
> 由于 SQL 的一个特殊性，所有非数值类型的值都必须用单引号括起来，包括字符串*和*变量。

#### signin.php

与 register.php 的做法类似，对于 signin.php，我们需要将用户认证的 `<div id="form">` 嵌入到模板的 `<div id="main">` 中。同样，垂直导航栏只是一个占位符，并做了其他一些小改动。清单 9-6 只显示了该脚本的 `<div id="main">` 部分；其余部分与模板非常相似。图 9-11 展示了 signin.php 的显示效果。

![图 9-11 管理员登录](img/1c438577fbcf9eaf55830d0e11ca0b3a_318_0.png)

##### 清单 9-6 signin.php（部分）

```
<div id="main">
    <h1 id="maintitle">Administrator Sign In</h1>
    <br />
<?php
    $retry = $_SESSION["retry"];
    if($retry < 1 ){
?>
    <p id="mainpara">Please enter your user ID and password, and
    click Sign In.</p>
<?php
    }
    else {
?>
    <p class="red">Please RE-enter your user ID and password, and
    click Sign In.</p>
<?php
    }
?>
    <!-- From User Authentication -->
    <div id="form">
        <!-- Display the sign-in form. After filling in, go to verify page. -->
        <form action="verify.php" method="post" id="signinForm">
```

```
<table width="200" border="0" cellspacing="3" cellpadding="5" >
    <tr>
        <th width="60">User ID:</th>
        <td width="120">
            <input type="text" name="userid" value="" size="60" />
        </td>
    </tr>
    <tr>
        <th>Password:</th>
        < PerspectiveImage>
            <input type="password" name="passwd" value="" size="20" />
        </td>
    </tr>
</table>
<input type="submit" name="submit" value="Sign In" />
</form>
</div>  <!-- id="form" -->
```

> **说明**
> 插入到脚本这部分开头的 PHP 代码调用了一个 `$_SESSION` 变量，因此需要在脚本最顶部使用 `session_start()` 函数，这在模板中已有体现。

#### verify.php

verify.php 脚本与 enterName.php 非常相似。从 signin.php 传入的 userid 和 passwd 会被清理，密码会被加密，然后将其与用户 ID 和数据库中的内容进行比对。如果匹配，会话变量会被更新，焦点会转移到第一个站点页面。如果不匹配，用户在 signin.php 中会有三次尝试机会，之后会被发送到 register.php 重新注册。清单 9-7 展示了该脚本。

> **提示**
> 如果未找到所查找的项目，SELECT 查询的结果不是 FALSE，查询也不会失败。必须单独将找到的内容与所查找的内容进行比较，以确定结果。这在 verify.php 中有演示。

##### 清单 9-7 verify.php

```
//Remove white space, check for blanks, and remove special characters
$userid = (trim($_POST['userid']) == '') ?
    die ("Please enter a user ID.")
    : mysql_real_escape_string($_POST['userid']);
```

```
$userpasswd = (trim($_POST['passwd']) == '') ?
    die ("Please enter a password.")
    :  mysql_real_escape_string($_POST['passwd']);

//Encrypt the password.
$encryptpasswd = sha1($userpasswd);

//Connect to the ClassRegistration database
$connection = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");
mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");

//See if match in the administrator table
$query = "SELECT admin_id, admin_password, admin_name
          FROM administrator
          WHERE admin_id= '$userid' AND admin_password= '$encryptpasswd'";
$result = mysql_query($query)
    or die("Select from administrator failed. " . mysql_error());

//Determine if the user ID and password are on file.
$row = mysql_fetch_object($result);
    $db_userid = $row->admin_id;
    $db_password = $row->admin_password;
    $name = $row->admin_name;

if($db_userid != $userid || $db_password != $encryptpasswd){
    //If not, add to Session Retry and test > 3
    $retry = $_SESSION["retry"];
    $retry++;
    if ($retry > 3) {
    //If greater than 3 go to register.
    header( "Location: register.php");
    }
    else {
    //If less than 3, update Session Retry and go to Sign in.
    $_SESSION["retry"] = $retry;
    header( "Location: signin.php");
    }
    }
else {
    //If on file, reset the session, and enter site.
    $_SESSION["name"] = $name;
    $_SESSION["retry"] = "admit";
    $_SESSION["time"] = time();
    header( "Location: enterSite.php");
}
?>
```

#### enterSite.php

enterSite.php 是一段可以放在站点每个页面上的代码，或者使用 PHP 的 `require_once()` 函数在每个页面上引入的代码片段。我们将在以下脚本中演示这两种用法。当这段代码在此应用中作为独立脚本时，它被称为"doorway.php"。该代码片段检查 `$_SESSION` 变量 retry 是否已设置且包含 admit。如果是，则检索用户名以便在脚本中使用（在实际使用中，echo 语句会从代码片段中移除，并放在脚本的其他位置）。如果不是，则加载 adminAuthen.php 脚本。

##### 清单 9-8 enterSite.php（doorway.php）

```
<?php
session_start();
//Check to see if session retry is "admit."
if (isset($_SESSION["retry"])&& $_SESSION["retry"] == "admit") {
    //If so, continue.
    echo "Hello ", $_SESSION["name"], "!<br />";
}
else {
    header( "Location: adminAuthen.php");
}
?>
```

### 数据库录入与维护

数据库录入与维护组件用于录入、更新和删除数据库中的信息。四个表都需要它，但在这个练习中，我们将为 Class 表执行此操作，以便向其中添加一些课程。在此过程中，它将演示 MySQL 的 INSERT、UPDATE 和 DELETE 功能。数据库录入与维护有三个子组件，每个子组件有一个或多个脚本：

- 系统入口
- 新课程录入
- 课程更新和删除

#### 系统入口

systemEntry.php 是数据库录入与维护的起点，允许你选择要执行的操作，然后引导你前往相应页面。它是管理员授权发送你到达的脚本，也是你完成此组件中的任何其他操作后返回的脚本。它没有数据库元素，PHP 代码也很少，如图 9-12 所示。

![图 9-12 systementry.php](img/1c438577fbcf9eaf55830d0e11ca0b3a_322_0.png)

首先创建一个新的基于我们在此构建的模板的 PHP 脚本，剪切并粘贴 enterSite.php 代码片段，修改中间部分和垂直菜单为这里所示的内容，并修改 verify.php 使其指向此脚本而不是 enterSite.php。清单 9-9 展示了来自 enterSite.php 代码片段的脚本开头的 PHP 代码，以及脚本的 vnav 和 main 部分。脚本的其余部分直接来自模板。

##### 清单 9-9 systementry.php

```
<?php
session_start();

//Check to see if session retry is session retry is "admit."
if (isset($_SESSION["retry"])&& $_SESSION["retry"] == "admit") {
    //If so, continue.
    $name = $_SESSION["name"];
}
```



 ```
else {
    header( "Location: adminAuthen.php");
}
?>
<div id="vnav">
    <table width="120" border="0" cellspacing="2" cellpadding="2">
        <tr>
            <td id="vhead">Go To: </td>
        </tr>
        <tr>
            <td><a href="classentry.php">Enter New Classes</a> </td>
        </tr>
        <tr>
            <td><a href="classupdate.php">Update & Delete Classes</a>
            </td>
        </tr>
    </table>
</div> <!-- id="vnav" -->
<div id="main">
    <h1 id="maintitle">Database Entry and Maintenance</h1>
    <br />
    <p id="mainpara">Hello
<?php
    echo $name;
?>
    </p>
    <br />
    <p id="mainpara">Please choose the task you want to<br />
    perform from the menu on the left.</p>
    <!-- <p class="red">*A footnote.</p> -->
</div> <!-- id="main" -->
```

#### 课程录入

课程录入从 classentry.php 开始，该文件首先使用模板，然后添加用于输入新课程的表单、用于将光标定位到第一个字段的 JavaScript，最后调用 addclass.php 将课程添加到数据库。addclass.php 与前面介绍的 enterName.php 非常相似，而且更简单，因为它不需要 cookie 和加密元素。图 9-13 显示了课程录入期间的界面，清单 9-10 展示了 classentry.php，清单 9-11 展示了 addclass.php。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_324_0.png)

**图 9-13** 有了模板、CSS 样式表，以及另一个可以从中获取部分代码的页面，构建新页面就相对简单了。

classentry.php 的大部分内容如清单 9-10 所示，这样你可以看到脚本早期部分的变化。页脚部分被省略了，因为它没有变化。

**清单 9-10 classentry.php**

```
<?php
require_once "doorway.php" ;
?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">
<html>
  <head>
    <title>Class Database Entry</title>
    <link rel= "stylesheet" type= "text/css" href= "/ClassRegistration/registration.css"/>
    <script language="JavaScript" type= "text/javascript"></script>
  </head>
```

```
<!-- Put cursor in the first field -->
<body onload="document.form1.class_title.focus();">
    <div id="wrapper">
        <div id="header">
            <img src="/ClassRegistration/MatTechLogo.gif"
                 alt="Matthews Technology" />
            <h1 id="title">Class Selection and Registration</h1>

        </div> <!-- id="header" -->
        <div id="hnav">
            <table width="400" border="0" cellspacing="2" cellpadding="2">
                <tr>
                    <td><a href="../index.php">Home</a> </td>
                    <td><a href="../about.php">About</a> </td>
                    <td><a href="../support.php">Support</a> </td>
                    <td><a href="..adminAuthen.php">Maintain</a> </td>
                </tr>
            </table>

        </div> <!-- id="hnav" -->
        <div id="vnav">
            <table width="120" border="0" cellspacing="2" cellpadding="2">
                <tr>
                    <td id="vhead">Go To: </td>
                </tr>
                <tr>
                    <td><a href="systementry.php">System Entry</a> </td>
                </tr>
                <tr>
                    <td><a href="classlist.php">Class Update & Delete</a></td>
                </tr>
            </table>

        </div> <!-- id="vnav" -->
        <div id="main">
            <h1 id="maintitle">Class Database Entry</h1>
            <p id="mainpara">Enter class information and click Add.</p>

            <!-- Class Entry form -->
            <form action="addclass.php" method="post" name="form1">
                <table width="600px" border="0" cellspacing="1" cellpadding="3">
                    <tr>
                        <th width="18%">Class Title:</th>
                        <td width="60%">
                            <input type="text" name="class_title" value=""
                                   size="60" />
                        </td>
                    </tr>
                    <tr>
                        <th>Class Start Date:<span class="red">*</span></th>
                        <td>
                            <input type="text" name="class_start" value=""
                                   size="60" />
                        </td>
---
120	                    </tr>
```

```
<tr>
	<th>Class Description:</th>
	<td>
		<textarea name="class_descr" cols="60"
			rows="4"></textarea>
	</td>
</tr>
<tr>
	<th>Class Cost:</th>
	<td>
		<input type="text" name="class_cost" value=""
			size="20" />
	</td>
</tr>
<tr>
	<th>Class Instructor:</th>
	<td>
		<input type="text" name="class_instr" value=""
			size="20" />
	</td>
</tr>
</table>
<p><input type="submit" value="Add" /></p>
</form>
```

<p class="red">All fields required.<br />
*Enter date fields as YYYYMMDD.</p>
</div> <!-- id="main" -->

**Listing 9-11 addclass.php**

```
<?php
//Remove white space, check for blanks, and remove special characters
$title = (trim($_POST['class_title']) == '') ?
	die ("Please enter the class title.")
	: mysql_real_escape_string($_POST['class_title']);

$start = (trim($_POST['class_start']) == '') ?
	die ("Please enter a start date.")
	: mysql_real_escape_string($_POST['class_start']);

$descr = (trim($_POST['class_descr']) == '') ?
	die ("Please enter a description.")
	: mysql_real_escape_string($_POST['class_descr']);

$cost = (trim($_POST['class_cost']) == '') ?
	die ("Please enter a class cost.")
	: mysql_real_escape_string($_POST['class_cost']);
```

```
$instr = (trim($_POST['class_instr']) == '') ?
    die ("Please enter an instructor.")
    :  mysql_real_escape_string($_POST['class_instr']);

//Connect to the ClassRegistration database
$connection = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");

mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");

//Add record to the class table
$query = "INSERT INTO class(class_title, class_start, class_descr,
    class_cost, class_instr)
    VALUES('$title', '$start', '$descr', '$cost', '$instr')";
$result = mysql_query($query)
    or die("Insert to class failed. " . mysql_error());

//Return to classentry.php.
    header( "Location: classentry.php");
```

#### Class Update and Delete

The class update and delete function has three subelements:

- Displaying the list of classes and letting the user select one to update or delete
- Displaying and updating the class selected
- Displaying and deleting the class selected

These three elements have in total five scripts, as discussed next.

#### Display the Class List

To update or delete a class, you must first have a list of classes from which to choose the one you want to update or delete. That is the function of classlist.php. This script begins with a PHP/MySQL section using SELECT to get all the records from the class table and ordering them by the class start date. The first record or row in the database table is then picked up and sent to an X/HTML table, which proceeds to loop through the remaining rows using a PHP do-while loop and displaying each as a row in the X/HTML table. Finally, each row of the table has two links, one for updating that particular record, and the other for deleting it. Figure 9-14 shows what the class list looks like on the screen, and Listing 9-14 shows the PHP and <div id= "main"> segments of the script to perform this function.

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_328_0.png)

**Figure 9-14** The class list lets you not only see the classes, but also choose to update or delete classes.

**NOTE**

The class_id used to get the correct record from the class table is passed to both classupdate.php and classdelete.php scripts in the link URL that loads them.

##### Listing 9-12 classlist.php

```
<?php
require_once "doorway.php" ;

//Connect to the ClassRegistration database
  $connection = mysql_connect("localhost", "root", "password")
```

```
or die("Cannot connect to MySQL.");
mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");

//Get records from the class table
$query = "SELECT * From class ORDER BY class_start";
$result = mysql_query($query)
    or die("Select from class failed. " . mysql_error());

//Get first class (row)from class table
$classrow = mysql_fetch_assoc($result);

?>

<div id="main">
    <h1 id="maintitle">Class List</h1>
    <p id="mainpara">Choose to Update or Delete a class.</p>

    <!-- Class List -->
    <table width="850" border="1" frame="void" rules="all"
    cellspacing="1" cellpadding="2">
        <!-- Display the column headings -->
        <tr>
            <th class="list" width="40">Class ID</th>
            <th class="list" width="110">Class Title</th>
            <th class="list" width="60">Class Start</th>
            <th class="list" width="400">Class Description</th>
            <th class="list" width="50">Class Cost</th>
            <th class="list" width="50">Class Instructor</th>
            <th class="list" width="50">&nbsp</th>
            <th class="th class="list" width="40">&nbsp</th>
        </tr>

        <!-- Loop through and display the classes (first class
        retrieved above). -->
        <?php do {  ?>

        <tr>
            <td align="center"><?php echo $classrow ['class_id']; ?></td>
            <td><?php echo $classrow ['class_title']; ?></td>
            <td align="center"><?php echo date('m/d/y',
                strtotime($classrow ['class_start'])); ?></td>
            <td><?php echo $classrow ['class_descr']; ?> &nbsp </td>
            <td align="right"><?php echo number_format($classrow
                ['class_cost'],0,'.',','); ?> &nbsp</td>
            <td><?php echo $classrow ['class_instr']; ?></td>
            <td><a href="classupdate.php?recordID=<?php echo
                $classrow ['class_id']; ?>">Update</a></td>
            <td><a href="classdelete.php?recordID=<?php echo
                $classrow ['class_id']; ?>">Delete</a></td>
        </tr>
        <?php } while ( $classrow = mysql_fetch_assoc($result) ); ?>
        </table>

    <p class="red">&nbsp</p>
</div> <!-- id="main" -->
```



第 9 章：综合运用 313

#### 更新课程

更新课程是输入新课程和显示现有课程的结合。它使用类似于输入新记录的输入表单，但会通过 PHP 生成的数组提供待更新课程的当前字段值。该课程通过课程列表传递的 `class_id` 以及 MySQL SELECT 语句来查找。在屏幕上完成所需的更改后，将调用 `updateclass.php` 脚本，使用 MySQL UPDATE 将数据库表中的记录替换。`class_id` 再次通过 URL 传递给 `updateclass.php`，而其他字段则通过表单的 POST 方法传输。图 9-15 展示了课程更新界面，而列表 15 和 16 分别展示了 `classupdate.php` 和 `updateclass.php` 的部分代码。

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_330_0.png)

**图 9-15** 课程列表和课程更新界面及脚本非常相似。

314 动态 Web 编程：初学者指南

##### 列表 9-13 classupdate.php

```
<?php
    require_once "doorway.php" ;

//Get Class ID from classlist.php
    $classid = ($_GET['recordID']);

//Connect to the ClassRegistration database
    $connection = mysql_connect("localhost", "root", "password")
        or die("Cannot connect to MySQL.");
    mysql_select_db("classregistration")
        or die("Database ClassRegistration not available.");

//Get records from the class table
    $query = "SELECT * From class WHERE class_id = $classid";
    $result = mysql_query($query)
        or die("Select from class failed. " . mysql_error());

//Get class (row)from database
    $classrow = mysql_fetch_assoc($result);

?>
<div id="main">
    <h1 id="maintitle">Class Database Update</h1>
    <p id="mainpara">Make the desired changes and click Update.</p>

    <!-- Class Entry form -->
    <form action="updateclass.php?recordID=<?php echo $classrow ['class_id']; ?>" method="post" name="form1">
        <table width="600px" border="0" cellspacing="1" cellpadding="3">
            <tr>
                <th width="18%">Class ID:</th>
                <td width="60%" ><?php echo $classrow ['class_id']; ?></td>
            </tr>
            <tr>
                <th>Class Title:</th>
                <td>
                    <input type="text" name="class_title" value="<?php
echo $classrow ['class_title']; ?>" size="60" />
                </td>
            </tr>
            <tr>
                <th>Class Start Date:<span class="red">*</span></th>
                <td>
                    <input type="text" name="class_start" value="<?php
echo $classrow ['class_start']; ?>" size="60" />
                </td>
            </tr>
            <tr>
                <th>Class Description:</th>
                <td>
                    <textarea name="class_descr" cols="60" rows="4"><?php
                    echo $classrow ['class_descr']; ?></textarea>
                    </td>
                </tr>
                <tr>
                    <th>Class Cost:</th>
                    <td>
                        <input type="text" name="class_cost" value="<?php echo
                        $classrow ['class_cost']; ?>&nbsp" size="20" />
                    </td>
                </tr>
                <tr>
                    <th>Class Instructor:</th>
                    <td>
                        <input type="text" name="class_instr" value="<?php
                        echo $classrow ['class_instr']; ?>" size="20" />
                    </td>
                </tr>
            </table>
            <p><input type="submit" value="Update" /></p>
        </form>

        <p class="red">All fields required.<br />
                *Enter date fields as YYYYMMDD.</p>

    </div> <!-- id="main" -->
```

```
<?php
//Get Class ID from classupdate.php
    $classid = ($_GET['recordID']);

//Remove white space, check for blank, and remove special characters
    $title =  (trim($_POST['class_title']) == '') ?
        die ("Please enter the class title.")
    :  mysql_real_escape_string($_POST['class_title']);

    $start = (trim($_POST['class_start']) == '') ?
        die ("Please enter a start date.")
        :  mysql_real_escape_string($_POST['class_start']);

    $descr = (trim($_POST['class_descr']) == '') ?
        die ("Please enter a description.")
        :  mysql_real_escape_string($_POST['class_descr']);

    $cost = (trim($_POST['class_cost']) == '') ?
        die ("Please enter the class cost.")
        :  mysql_real_escape_string($_POST['class_cost']);

    $instr = (trim($_POST['class_instr']) == '') ?
        die ("Please enter the instructor.")
        :  mysql_real_escape_string($_POST['class_instr']);
```

```
//Connect to the ClassRegistration database
$connection = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");

mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");

//Update the record on the class table
$query = "UPDATE class SET class_title='$title', class_start='$start',
    class_descr='$descr', class_cost='$cost', class_instr='$instr'
    WHERE class_id='$classid' ";
$result = mysql_query($query)
    or die("Update class failed. " . mysql_error());

//Return to classlist.php.
    header( "Location: classlist.php");
?>
```

#### 删除课程

classdelete.php 包含许多与 classupdate.php 相同的元素。脚本开头的 PHP 代码完全相同，在下面的列表中不再重复。它只是获取将要删除的课程或记录。该记录以类似 classupdate.php 的表格形式呈现，但此处信息仅列出且无法更改。虽然没有输入字段，但 X/HTML 表格位于一个表单中，以便将信息传递给 deleteclass.php，该文件使用 MySQL 的 DELETE 执行实际删除操作。图 9-16 展示了屏幕上的 classdelete.php，而列表 15 和 16 分别展示了 classdelete.php 和 deleteclass.php 的部分代码。

##### 列表 9-15 classdelete.php

```
<div id="main">
    <h1 id="maintitle">Class Delete</h1>
    <p class="red"><b>If you are sure you want to delete this class,
        click Delete.</b></p>

    <!-- Class Entry form -->
    <form action="deleteclass.php?recordID=<?php echo $classrow
        ['class_id']; ?>" method="post" name="form1">
    <table width="600px" border="0" cellspacing="1" cellpadding="3">
        <tr>
            <th width="18%">Class ID:</th>
            <td width="60%"><?php echo $classrow ['class_id']; ?></td>
        </tr>
        <tr>
            <th>Class Title:</th>
            <td><?php echo $classrow ['class_title']; ?></td>
        </tr>
```

```
<tr>
    <th>Class Start Date:</th>
    <td><?php echo date('m/d/y', strtotime($classrow['class_start'])); ?></td>
</tr>
<tr>
    <th>Class Description:</th>
    <td><?php echo $classrow['class_descr']; ?></td>
</tr>
<tr>
    <th>Class Cost:</th>
    <td>$<?php echo number_format($classrow['class_cost'], 0, '.', ','); ?>&nbsp</td>
</tr>
<tr>
    <th>Class Instructor:</th>
    <td><?php echo $classrow['class_instr']; ?></td>
</tr>
</table>
<p class="red"><input type="submit" value="Delete" /></p>
</form>

<p class="red">&nbsp</p>

</div><!-- id="main" -->
```

###### 列表 9-16 deleteclass.php

```
<?php
//Get Class ID from classupdate.php
$classid = ($_GET['recordID']);

//Connect to the ClassRegistration database
$connection = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");
mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");

//Delete a record from the class table
$query = "DELETE FROM class WHERE class_id='$classid' ";
$result = mysql_query($query)
    or die("Delete class failed. " . mysql_error());

//Return to classlist.php.
header("Location: classlist.php");
?>
```

第 9 章：综合运用 317

![](img/1c438577fbcf9eaf55830d0e11ca0b3a_335_0.png)

图 9-16 classdelete.php 正在获取用户想要删除记录的确认。

### 课程注册

与身份验证和维护流程相比，并经历了这些流程之后，课程注册过程相对简单。注册共有六个步骤，如图 9-17 所示，每一步都有一个或两个脚本。

#### 课程列表与选择

课程列表脚本 classes.php 与用于更新和删除课程的 classlist.php 几乎完全相同。主要区别是更新和删除链接已被注册链接取代，末尾调用的脚本不同，并且一些标题有所更改。它甚至不值得单独列出新列表；参见列表 9-12。屏幕上的显示也非常相似，如图 9-18 所示。

#### 学生电子邮件输入

学生电子邮件输入脚本会将所选课程一并带入，要求学生输入其电子邮件地址，以确定他们之前是否已注册过课程。



 # 第9章：综合应用

图 9-17 选择和注册课程所需的步骤

| 课程编号 | 课程名称 | 课程开始时间 | 课程描述 | 课程费用 | 课程讲师 |
|---|---|---|---|---|---|
| 4 | 使用 PHP 锻炼服务器 | 01/18/10 | 使用 PHP 锻炼服务器通过提供该语言概述、描述其使用的各种组件，以及 PHP 如何用于处理和配合服务器，动态处理网页信息，来介绍 PHP | $750 | Alice Bailey |
| 6 | 使用 PHP 访问 MySQL 数据库 | 02/01/10 | 使用 PHP 访问 MySQL 数据库描述如何将 PHP 与 MySQL 结合使用来创建和处理（或查询）MySQL 数据库，包括从 HTML 表单获取信息并存储到数据库中，以及显示、更新和删除数据库信息 | $1,000 | Marty Matthews |
| 1 | 网站入门 | 02/14/10 | 本课程为初学者提供开始构建网站所需的基础知识。它向学生介绍 Web，然后深入讲解 HTML，以及如何编写 HTML 标签来创建网页 | $500 | John Staley |
| 2 | meatballs_style_guide.md | 03/15/10 | 为网页添加样式涵盖良好设计的要素、是什么让网页具有吸引力，以及如何创建和使用层叠样式表（CSS）来为整个网站添加一致的样式 | $650 | Bess Pretty |
| 9 | 高级 JavaScript | 03/22/10 | 高级 JavaScript 讨论如何创建和使用表单、其方法和属性，以及如何使用 JavaScript 验证信息、从表单获取信息，并在网站中执行导航 | $1,000 | John Cronan |
| 5 | 使用 MySQL 构建数据库 | 04/05/10 | 使用 MySQL 构建数据库介绍 SQL（结构化查询语言）作为 MySQL 的基础，并讨论该语言的基本特性以及这些特性在 MySQL 中的实现方式 | $750 | George Maynard |

图 9-18 用于注册的课程列表与用于更新和删除的课程列表非常相似。

如果是这样，它们将被传递给 stuupdate.php 脚本，在那里他们可以根据需要更新自己的学生记录。否则，他们将被发送到 stuentry.php，在那里他们可以填写注册信息。此过程使用了三个脚本：

- **emailentry.php**，用于输入电子邮件地址及其确认的表单，显示学生正在注册的课程，部分如清单 9-17 所示。图 9-19 显示了电子邮件输入在屏幕上的样子。
- **emailvalid.js**，一个 JavaScript 表单验证脚本，检查是否已输入电子邮件地址及其确认，两者是否都是有效的地址，以及它们是否相同，如清单 9-18 所示。以下是产生的三条消息：

图 9-19 电子邮件输入携带课程信息。

用于检查电子邮件地址是否已在档的 checkemail.php，如清单 9-19 所示。学生的电子邮件地址与学生表中的电子邮件地址进行比较，如果找到匹配项，则加载 stuupdate.php；否则加载 stuentry.php。在这两种情况下，课程 ID 和学生电子邮件地址都会传递给下一个脚本。

# 注意

来自 emailentry.php 的以下三行代码包含两种不同的将 classid 传递给 checkemail.php 的方式。第一种方式使用 URL，与之前在几个维护脚本中的做法相同；第二种使用隐藏字段和 post。只需要一种方式。checkemail.php 将使用第二种方式，以与获取电子邮件地址相同的方式获取 classid。onsubmit 语句调用 JavaScript 验证函数。

```
<form action="checkemail.php?recordID=<?php echo $classid ?>" method="post"
  onsubmit="return validate_form(this)" name="form1">
  <input type="hidden" name="classid" value="<?php echo $classid; ?>"/>
```

##### 清单 9-17 emailentry.php

```
<div id="main">
    <h1 id="maintitle">Student Registration</h1>
    <p id="mainpara">To register for this class, please enter your
       e-mail addressGuests two and click Continue.</p>
    
    <!-- From Class List -->
    <table width="850" border="1" frame="void" rules="all" 
       cellspacing="1" cellpadding="2">
       <!-- Display the column headings -->
       <tr>
          <th class="list" width="40">Class ID</th>
          <th class="list" width="150">Class Title</th>
          <th class="list" width="60">Class Start</th>
          <th class="list" width="450">Class Description</th>
          <th class="list" width="50">Class Cost</th>
          <th class="list" width="50">Class Instructor</th>
       </tr>
       
       <!-- Display the selected class. -->
       <tr>
          <td align="center"><?php echo $classrow ['class_id']; ?></td>
          <td><?php echo $classrow ['class_title']; ?></td>
          <td align="center"><?php echo date('m/d/y',strtotime($classrow
             ['class_start'])); ?></td>
          <td><?php echo $classrow ['class_descr']; ?> &nbsp </td>
          <td align="right">$<?php echo number_format($classrow
             ['class_cost'],0,'.',','); ?>&nbsp;</td>
          <td><?php echo $classrow ['class_instr']; ?></td>
       </tr>
    </table>
```

```
<p>&nbsp</p>
<p>&nbsp</p>
<div id="form">
<!-- Display the e-mail entry form. After filling in, go
    to check e-mail page. -->
<form action="checkemail.php" method="post"
    onsubmit="return validate_form(this)" name="form1">
    <input type="hidden" name="classid" value="<?php echo
        $classid; ?>"/>
    <table width="200" border="0" cellspacing="3" cellpadding="5">
        <tr>
            <th width="100">E-mail Address:</th>
            <td width="80">
                <input type="text" name="email" value="" size="40" />
            </td>
        </tr>
        <tr>
            <th width="100">Confirm E-mail:</th>
            <td width="80">
                <input type="text" name="conemail" value="" size="40" />
            </td>
        </tr>
    </table>
    <input type="submit" name="submit" value="Continue" />
</form>
</div> <!-- id="form" -->

<!-- Begin from template -->
<br />
<p class="red">All fields are required.</p>
</div> <!-- id="main" -->
```

##### 清单 9-18 emailvalid.js

```
// JavaScript Document
function validate_required(field,alerttxt)
{
  with (field)
  {
  if (value==null||value=="")
    {alert(alerttxt);return false}
  else {return true}
  }
}

function validate_email(field,alerttxt)
{
    with (field)
    {
    apos=value.indexOf("@")
```

```
dotpos=value.lastIndexOf(".")
if (apos<1||dotpos-apos<2)
    {alert(alerttxt);return false}
else {return true}
}

function validate_equal(field1,field2,alerttxt)
{
    if (field1.value==field2.value)
        {return true}
    else {alert(alerttxt);return false}
}

function validate_form(thisform)
{
    with (thisform)
    {
    if (validate_required(email,"Please enter an e-mail address.")==false)
        {email.focus();return false}
    if (validate_email(email,"Please enter a valid e-mail address.")==false)
        {email.focus();return false}
    if (validate_required(conemail,"Please confirm your e-mail address.")==false)
        {conemail.focus();return false}
    if (validate_email(conemail,"Please enter a valid e-mail address.")==false)
        {conemail.focus();return false}
    if (validate_equal(email,conemail,"The two e-mail addresses are not the same.")==false) {conemail.focus();return false}
    if (email && conemail)
        form1.submit
    }
}
```

##### 清单 9-19 checkemail.php

```
<?php
//Remove white space, check for blank, and remove special characters
$classid = (trim($_POST['classid']) == '') ?
    die ("Please enter a class ID.")
    : mysql_real_escape_string($_POST['classid']);

$email = (trim($_POST['email']) == '') ?
    die ("Please enter your e-mail address.")
    : mysql_real_escape_string($_POST['email']);

//Connect to the ClassRegistration database
$connection = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");
mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");

//See if match in the administrator table
$query = "SELECT student_email
```



 ```
FROM student
WHERE student_email= '$email';
$result = mysql_query($query)
    or die("Select from student failed. " . mysql_error());

//Determine if the student e-mail is on file.
$row = mysql_fetch_object($result);
$db_email = $row->student_email;

if($db_email != $email ){

    //If not, go to new student entry with the classid and the e-mail
    header( "Location: stuentry.php?classid=$classid&email=$email");
}
else {

    //If on file, go to student update, with the classid and the e-mail.
    header( "Location: stuupdate.php?classid=$classid&email=$email");
?>
```

#### 新生录入

新生录入脚本（stuentry.php，见清单 9-20）从 checkemail.php 接收课程 ID 和学生电子邮件地址。课程 ID 用于显示将要注册的课程。学生需要输入他或她的姓名和电话号码（实际应用中可能有更多字段），如图 9-20 所示，然后点击“继续”，页面将跳转至 enterstu.php，同时携带课程 ID、电子邮件地址以及姓名和电话号码。

##### 清单 9-20 stuentry.php

```
<?php
//Get Class ID from checkemail.php
    $classid = ($_GET['classid']);
//Get e-mail address from checkemail.php
    $email = ($_GET['email']);

//Connect to the ClassRegistration database
    $connection = mysql_connect("localhost", "root", "password")
        or die("Cannot connect to MySQL.");
    mysql_select_db("classregistration")
        or die("Database ClassRegistration not available.");

//Get records from the class table
    $query = "SELECT * FROM class WHERE class_id = $classid";
    $result = mysql_query($query)
        or die("Select from class failed. " . mysql_error());
```

图 9-20 学生注册继续显示课程信息，以便学生确认自己正在注册的课程。

```
//Get class (row) from class table
    $classrow = mysql_fetch_assoc($result);
?>
  <div id="main">
    <h1 id="maintitle">Student Registration</h1>
    <br />
    <p id="mainpara">To register for this class, please enter
      your name and phone, and click Continue.</p>

    <!-- From Class List -->
    <table width="850" border="1" frame="void" rules="all"
      cellspacing="1" cellpadding="2">
      <!-- Display the column headings -->
      <tr>
        <th class="list" width="40">Class ID</th>
        <th class="list" width="150">Class Title</th>
        <th class="list" width="60">Class Start</th>
        <th class="list" width="450">Class Description</th>
        <th class="list" width="50">Class Cost</th>
        <th class="list" width="50">Class Instructor</th>
      </tr>

      <!-- Display the selected class. -->
      <tr>
```

```
<td align="center"><?php echo $classrow ['class_id']; ?></td>
<td><?php echo $classrow ['class_title']; ?></td>
<td align="center"><?php echo date('m/d/y',strtotime($classrow
['class_start'])); ?></td>
<td><?php echo $classrow ['class_descr']; ?> &nbsp </td>
<td align="right">$<?php echo number_format($classrow
['class_cost'],0,'.',','); ?>&nbsp</td>
<td><?php echo $classrow ['class_instr']; ?></td>
</tr>
</table>
<p>&nbsp</p> <!-- Inserts two blank lines -->
<p>&nbsp</p>

<div id="form">
<!-- Go to enterstu.php after clicking Continue -->
<form action="enterstu.php?classid=<?php echo $classid
?>&email=<?php echo $email ?>" method="post" name="form1">
<table width="300" border="0" cellspacing="1" cellpadding="3" >
<tr>
<th width="30%">Student Name:</th>
<td width="50%">
<input type="text" name="stu_name" value=""
size="60" />
</td>
</tr>
<tr>
<th>Phone Number:</th>
<td>
<input type="text" name="phone" value=""
size="20" />
</td>
</tr>
</table>
<br />
<input type="submit" name="submit" value="Continue" />
</form>
</div> <!-- id=form -->
```

enterstu.php（见清单 9-21）从 stuentry.php 接收课程 ID 以及学生的电子邮件地址、姓名和电话号码。它将后三项写入 student 表，然后加载 confirm.php，并将课程 ID 和电子邮件地址传递给它。

##### 清单 9-21 enterstu.php

```
<?php
//Get Class ID from checkemail.php
  $classid = ($_GET['classid']);

//Get e-mail address from checkemail.php
  $email = ($_GET['email']);

//Remove white space, check for blank, and remove special characters
  $name = (trim($_POST['stu_name']) == '') ?
    die ("Please enter your name.")
```

```
: mysql_real_escape_string($_POST['stu_name']);

$phone = (trim($_POST['phone']) == '') ?
    die ("Please enter your phone number.")
    : mysql_real_escape_string($_POST['phone']);

//Connect to the ClassRegistration database
    $connection = mysql_connect("localhost", "root", "password")
        or die("Cannot connect to MySQL.");
    mysql_select_db("classregistration")
        or die("Database ClassRegistration not available.");

//Add record to the student table
    $query = "INSERT INTO student (student_email, student_name, student_phone)
        VALUES('$email', '$name', '$phone')";
    $result = mysql_query($query)
        or die("Insert to student failed. " . mysql_error());

//Go to confirm.php with class id and e-mail.
    header( "Location: confirm.php?classid=$classid&email=$email");
?>
```

#### 现有学生更新

学生更新（stuupdate.php，见清单 9-22）在显示学生数据库记录的同时保持课程信息的显示，并允许学生修改姓名和电话号码字段，如图 9-21 所示。学生无法修改电子邮件地址，因为它是记录的主键（虽然可以实现，但会使问题复杂化——需要删除原记录并录入新记录），而注册日期由系统提供。学生完成更新并点击“继续”后，将跳转至 updatestu.php，并携带本页面的信息。

##### 清单 9-22 stuupdate.php

```
<?php
//Get Class ID from checkemail.php
    $classid = ($_GET['classid']);

//Get email address from checkemail.php
    $email = ($_GET['email']);

//Connect to the ClassRegistration database
    $connection = mysql_connect("localhost", "root", "password")
        or die("Cannot connect to MySQL.");
    mysql_select_db("classregistration")
        or die("Database ClassRegistration not available.");

//Get record from the class table
    $query = "SELECT * FROM class WHERE class_id = $classid";
    $result = mysql_query($query)
        or die("Select from class failed. " . mysql_error());
```

图 9-21 学生更新允许更改学生输入的字段。

```
//Get class (row) from class table
$classrow = mysql_fetch_assoc($result);

//Get record from the student table
$query1 = "SELECT * FROM student WHERE student_email = '$email'";
$result1 = mysql_query($query1)
    or die("Select from student failed. " . mysql_error());

//Get student (row) from student table
$sturow = mysql_fetch_assoc($result1);
?>
<div id="main">
    <h1 id="maintitle">Student Database Update</h1>
    <p id="mainpara">Make any desired changes and click Continue.</p>
    
    <!-- From Class List -->
    <table width="850" border="1" frame="void" rules="all"
        cellspacing="1" cellpadding="2">
    <!-- Display the column headings -->
    <tr>
        <th class="list" width="40">Class ID</th>
        <th class="list" width="150">Class Title</th>
        <th class="list" width="60">Class Start</th>
```

```
<th class="list" width="450">Class Description</th>
<th class="list" width="50">Class Cost</th>
<th class="list" width="50">Class Instructor</th>
</tr>

<!-- Display the selected class. -->
<tr>
    <td align="center"><?php echo $classrow ['class_id']; ?></td>
    <td><?php echo $classrow ['class_title']; ?></td>
    <td align="center"><?php echo
        date('m/d/y',strtotime($classrow ['class_start'])); ?></td>
    <td><?php echo $classrow ['class_descr']; ?> &nbsp </td>
    <td align="right">$<?php echo
        number_format($classrow ['class_cost'],0,'.',','); ?>&nbsp</td>
    <td><?php echo $classrow ['class_instr']; ?></td>
</tr>
</table>
<p>&nbsp</p> <!-- Inserts two blank lines -->
<p>&nbsp</p>
<!-- Begin Student Update -->
<div id="form">
    <!-- Go to updatestu.php after clicking Continue -->
    <form action="updatestu.php?classid=<?php echo $classid
        ?>&email=<?php echo $email ?>" method="post" name="form1">
        <table width="300" border="0" cellspacing="1" cellpadding="3" >
            <tr>
                <th width="30%">Student E-mail:</th>
                <td width="50%"><?php echo $sturow ['student_email']; ?></td>
            </tr>
            <tr>
                <th>Student Name:</th>
                <td>
                    <input type="text" name="stu_name" value="<?php echo
                        $sturow ['student_name']; ?>" size="60" />
                </td>
            </tr>
            <tr>
                <th>Phone Number:</th>
                <td>
                    <input type="text" name="phone" value="<?php echo
                        $sturow ['student_phone']; ?>" size="20" />
                </td>
            </tr>
            <tr>
                <th width="30%">Date Entered:</th>
                <td width="50%"><?php echo $sturow ['student_date']; ?></td>
            </tr>
        </table>
        <br />
        <input type="submit" name="submit" value="Continue" />
    </form>
</div> <!-- id=form -->
<p class="red">All fields required.</p>
</div> <!-- id="main" -->
```



updatestu.php（见清单 9-23）从 stuupdate.php 接收班级 ID 以及学生的电子邮件地址、姓名和电话。它将后三项更新到 student 表中，然后加载 confirm.php，并向其传递班级 ID 和电子邮件地址。

##### 清单 9-23 updatestu.php

```
<?php
//Get Class ID from stuupdate.php
   $classid = ($_GET['classid']);

//Get email address from stuupdate.php
   $email = (($_GET['email']);

//Remove white space, check for blank, and remove special characters
   $name = (trim($_POST['stu_name']) == '') ?
      die ("Please enter your name.")
      : mysql_real_escape_string($_POST['stu_name']);

   $phone = (trim($_POST['phone']) == '') ?
      die ("Please enter your phone number.")
      : mysql_real_escape_string($_POST['phone']);

//Connect to the ClassRegistration database
   $connection = mysql_connect("localhost", "root", "password")
      or die("Cannot connect to MySQL.");
   mysql_select_db("classregistration")
      or die("Database ClassRegistration not available.");

//Update a record on the student table
   $query = "UPDATE student SET student_name='$name', student_phone='$phone'
      WHERE student_email='$email'";
   $result = mysql_query($query)
      or die("Insert to student failed. " . mysql_error());

//Go to confirm.php with class id and e-mail.
   header("Location: confirm.php?classid=$classid&email=$email");
?>
```

#### 注册与确认

最终的注册确认页面 confirm.php（如清单 9-24 所示），从 stuentry.php 或 stuupdate.php 接收班级 ID 和电子邮件地址。它使用这些信息从数据库中检索并显示班级和学生的记录。学生被要求确认这些信息，如图 9-22 所示。当他们点击"确认"时，会加载 sendemail.php，并向其传递班级 ID 和电子邮件地址。

##### 清单 9-24 confirm.php

```
<?php
//Get Class ID from enterstu.php
  $classid = ($_GET['classid']);

//Get e-mail address from enterstu.php
  $email = ($_GET['email']);

//Connect to the ClassRegistration database
  $connection = mysql_connect("localhost", "root", "password")
      or die("Cannot connect to MySQL.");
  mysql_select_db("classregistration")
      or die("Database ClassRegistration not available.");

//Get record from the class table
  $query = "SELECT * FROM class WHERE class_id = $classid";
  $result = mysql_query($query)
      or die("Select from class failed. " . mysql_error());
```

Chapter 9: Putting It All Together

331

**MATTHEWS TECHNOLOGY**
Integrating Innovation!

CLASS SELECTION AND REGISTRATION

Go To:

**Registration Confirmation**

To complete registration, please review the class and student information.
If OK, click Confirm, otherwise use one of the options on the left.
You will be sent an email confirmation.

| Class ID | Class Title | Class Start | Class Description | Class Cost | Class Instructor |
|----------|-------------|-------------|-------------------|------------|------------------|
| 6 | Accessing MySQL Databases with PHP | 02/01/10 | Discusses how PHP is used with MySQL to create and access, or query, a MySQL database including taking information from HTML forms and storing it in the database, and displaying, updating, and deleting database information. | $1,000 | Marty Matthews |

| Email Address | Student Name | Phone Number | Registration Date |
|---------------|------------|--------------|-------------------|
| jm@web.com | Judy Mann | 987-654-3210 | 04/13/09 |

[Confirm]

Copyright © 2008 - 2009 Matthews Technology
Contact us by clicking here.

**图 9-22** 学生还有一次机会进行修改，然后注册被确认。

## 332 Dynamic Web Programming: A Beginner's Guide

```
//Get class (row) from class table
  $classrow = mysql_fetch_assoc($result);

//Get record from the student table
  $query1 = "SELECT * FROM student WHERE student_email = '$email'";
  $result1 = mysql_query($query1)
     or die("Select from student failed. " . mysql_error());

//Get student (row) from student table
  $sturow = mysql_fetch_assoc($result1);

?>
```

```
<div id="main">
  <h1 id="maintitle">Registration Confirmation</h1>
  <br />
  <p id="mainpara">To complete registration, please review
    the class and student information.<br />
    If OK, click Confirm, otherwise use one of the
    options on the left.<br />
    You will be sent an e-mail confirmation.</p>

  <!-- From Class List -->
  <table width="850" border="1" frame="void" rules="all"
     cellspacing="1" cellpadding="2">
     <!-- Display the column headings -->
     <tr>
        <th class="list" width="40">Class ID</th>
        <th class="list" width="150">Class Title</th>
        <th class="list" width="60">Class Start</th>
        <th class="list" width="450">Class Description</th>
        <th class="list" width="50">Class Cost</th>
        <th class="list" width="50">Class Instructor</th>
     </tr>

     <!-- Display the selected class. -->
     <tr>
        <td align="center"><?php echo $classrow ['class_id']; ?></td>
        <td><?php echo $classrow ['class_title']; ?></td>
        <td align="center"><?php echo
           date('m/d/y',strtotime($classrow ['class_start'])); ?></td>
        <td><?php echo $classrow ['class_descr']; ?>&nbsp </td>
        <td align="right">$<?php echo number_format($classrow
           ['class_cost'],0,'.',','); ?>&nbsp</td>
        <td><?php echo $classrow ['class_instr']; ?></td>
     </tr>
  </table>
  <p>&nbsp</p> <!-- Inserts two blank lines -->
  <p>&nbsp</p>

  <div id="form">
     <!-- Go to enterstu.php after clicking Continue -->
     <form action="sendemail.php?classid=<?php echo
        $classid ?>&email=<?php echo $email ?>"
        method="post" name="form1">
     <table width="300" border="0" cellspacing="1" cellpadding="3" >
     <!-- Display the column headings -->
```

```
<tr>
    <th class="list" width="40">E-mail Address</th>
    <th class="list" width="150">Student Name</th>
    <th class="list" width="60">Phone Number</th>
    <th class="list" width="450">Registration Date</th>
</tr>

<!-- Display the selected class. -->
<tr>
    <td align="center"><?php echo $sturow ['student_email']; ?></td>
    <td><?php echo $sturow ['student_name']; ?></td>
    <td><?php echo $sturow ['student_phone']; ?> &nbsp </td>
    <td align="center"><?php echo date('m/d/y',strtotime($sturow ['student_date'])); ?></td>
</tr>
</table>
<br />
<input type="submit" name="confirm" value="Confirm" />
</form>
</div> <!-- id=form -->
<br />
<p class="red">&nbsp</p>
</div> <!-- id="main" -->
```

sendemail.php 是我们让关系数据库大显身手的地方。班级 ID 和电子邮件地址用于构建一条新记录，并将其写入 register 表。然后使用 mysql_insert_id 获取在生成新注册记录时自动生成的注册 ID（$regid）。接着，使用班级 ID、电子邮件地址和注册 ID 分别从 class、student 和 registration 表中检索记录。这些信息随后用于准备并发送注册确认的电子邮件。电子邮件消息使用 $msg_client 的长串联接（.=）来构成消息正文。

##### 清单 9-25 sendemail.php

```
<?php
//Get Class ID from confirm.php
    $classid = ($_GET['classid']);

//Get e-mail address from confirm.php
    $email = ($_GET['email']);

//Connect to the ClassRegistration database
    $connection = mysql_connect("localhost", "root", "password")
        or die("Cannot connect to MySQL.");
    mysql_select_db("classregistration")
        or die("Database ClassRegistration not available.");
```

```
//Add record to the registration table
$query = "INSERT INTO registration(class_id, student_email)
    VALUES('$classid', '$email')";
$result = mysql_query($query)
    or die("Insert to registration failed. " . mysql_error());

//Get the registration ID generated by insert.
$regid = mysql_insert_id();

//Get record from the class table
$query1 = "SELECT * FROM class WHERE class_id = '$classid'";
$result1 = mysql_query($query1)
    or die("Select from class failed. " . mysql_error());

//Get selected class (row) from class table
$classrow = mysql_fetch_assoc($result1);

//Get record from the student table
$query2 = "SELECT * FROM student WHERE student_email = '$email'";
$result2 = mysql_query($query2)
    or die("Select from student failed. " . mysql_error());

//Get student (row) from student table
$sturow = mysql_fetch_assoc($result2);

//Get record from the registration table
$query3 = "SELECT * FROM registration WHERE reg_id = '$regid'";
$result3 = mysql_query($query3)
    or die("Select from registration failed. " . mysql_error());

//Get registration (row) from registration table
$regrow = mysql_fetch_assoc($result3);

//Confirmation E-mail
$to_client = $sturow['student_name'] . ' <'.$sturow['student_email'].'>';
$sub_client = 'Class Registration';
$msg_client = 'Thank you for your class registration. Here is the
    necessary information:'."\n\n";
$msg_client .= 'Registration number: '.$regrow['reg_id']."\n";
$msg_client .= 'Class ID: '. $classid . "\n";
$msg_client .= 'Class Title: '.$sturow['class_title']."\n";
$msg_client .= 'Class Start Date: '.$sturow['class_start']."\n";
$msg_client .= 'Class Cost: '. "$" . $sturow['class_cost']."\n";
$msg_client .= 'Registration date: '.$regrow['reg_date']."\n";
$msg_client .= "\n\n";
```



 ```
$msg_client .= 'Your E-mail Address: '.$sturow['email_address']."\n";
$msg_client .= 'Your Name: '.$sturow['student_name']."\n";
$msg_client .= 'Your Phone: '.$sturow['student_phone']."\n\n";
$msg_client .= 'Please contact us to arrange payment at:'."\n";
$msg_client .= 'info@matthewstechnology.com'."\n";
$msg_client .= "\n\n";
$msg_client .= 'Thanks again,'."\n\n";
$msg_client .= 'Matthews Technology'."\n\n";
$addl_headers_client = 'From: Matthews Technology
    <info@matthewstechnology.com>'."\n\n";

mail($to_client,$sub_client,$msg_client,$addl_headers_client);
?>
    <div id="main">
        <h1 id="maintitle">Class Database Update</h1>
        <p id="mainpara">Thank you for completing class registration!<br />
            Please click Complete.</p>

        <div id="form">
            <!-- Go to classes.php after clicking Complete -->
            <form action="classes.php" method="post" name="form1">
                <input type="submit" name="submit" value="Complete" />
            </form>
        </div> <!-- id=form -->
        <p class="red">&nbsp;</p>

    </div> <!-- id="main" -->
```

类似"课程选择与注册"这样的应用程序总是可以扩展和改进的。在构建过程中你会做出一些决策，而完成之后，你又会重新考虑，在大多数情况下不会超过15秒，就想着回去进行大规模重写。这个应用程序中可以更改的一些地方包括：

- 将数据库连接代码（如下所示）放在一个单独的脚本中，并通过`require_once`在其他脚本中引入。这段代码在每个使用数据库的脚本中都是一样的。这还有助于提高安全性，因为用户名和密码只需要放在一个位置，而不是每个脚本中都有。大多数互联网托管服务都有办法隐藏这样的脚本。

```
//Connect to the ClassRegistration database
$connection正值 = mysql_connect("localhost", "root", "password")
    or die("Cannot connect to MySQL.");
mysql_select_db("classregistration")
    or die("Database ClassRegistration not available.");
```

- 扩展数据库录入和维护组件，使其包含学生和注册表的维护。这只需复制课程表的脚本并更改表名即可。
- 扩展学生表及其支持脚本，添加额外的学生字段，如地址、城市、州和邮政编码。
- 添加支付系统——使用PayPal让这变得非常简单。通过PayPal，你可以接受信用卡、借记卡以及银行转账，只需使用简单的X/HTML链接或购物车即可。访问他们的网站http://www.paypal.com；点击**企业**，然后在"需要接受信用卡吗？"下点击**在您的网站上**。

我相信你还能想到许多其他可以对这个应用程序进行的更改。关键是，现在你已经拥有了进行这些更改的工具，以及许多获取额外工具的资源的链接。你能用这些工具做什么，只受你的想象力的限制。

## 索引

### 数字

- 216 色（Web 安全调色板），51

### 符号

# （井号），与类选择符一起使用，41–42

# 注释，在 PHP 中包含，182。*另见* 注释

$ （美元符号）

- 在 PHP 中使用，186–187
- 在正则表达式中使用，167

% （取模）运算符

- 在 JavaScript 中使用，102
- 在 PHP 中使用，187

() （括号）

- 在 PHP 中使用，187
- 与三元运算符一起使用，202

+ * （星号），在 SQL 中使用，246

+ . （句点），与类选择符一起使用，41–42

+ / （斜杠），与标签一起使用，16

+ // 正则表达式，167

// 注释。*另见* 注释

- 在 PHP 中包含，182
- 在 JavaScript 中使用，90

/\* \*/ 注释。*另见* 注释

- 在 PHP 中包含，182
- 在 JavaScript 中使用，90
- 与注释一起使用，41

: （冒号），与事件选择符一起使用，43

; （分号）

- 在 JavaScript 中使用，91
- 与 PHP 脚本一起使用，183

? : （三元运算符）

- 在 JavaScript 中使用，114
- 在 PHP 中使用，201–202

\ （反斜杠）

- 在 JavaScript 中产生，92
- 在 JavaScript 中使用，91–92
- 在 PHP 中使用，183–184、189

+ \\' 转义序列，与 alert 一起使用，126–127

+ \\r\\n，在 PHP 中使用，213

+ \^，在正则表达式中使用，167

\_ （下划线）

- 在 JavaScript 中使用，99
- 与用户自定义函数一起使用，198

+ {} （花括号），与 CSS 规则一起使用，40

+ <\!-- --> 注释，使用，19、40

+ <\!-- //--> 注释，在 JavaScript 中使用，91

+ <> （尖括号），与标签一起使用，16

= （等号）运算符

- 在 JavaScript 中使用，102
- 在 PHP 中使用，187

== （相等运算符）

- 在 JavaScript 中使用，102、112
- 在 PHP 中使用，187、200

" （双引号）

- 在 JavaScript 中产生，92
- 在 JavaScript 中使用，91–92
- 在 PHP 中使用，183–184、189
- 与字体名称一起使用，51、53
- 与 JavaScript 属性一起使用，124
- 与字符串一起使用，92

' （单引号）

- 在 JavaScript 中产生，92
- 在 PHP 中使用，183–184、189
- 在 phpMyAdmin 中使用，256
- 与非数字属性一起使用，300
- 与字符串一起使用，92

, （逗号）

- 在 JavaScript 中使用，91
- 在 PHP 中使用，183

### A

<a href> 元素，与 index.php 一起使用，231

<a></a> 标签组，使用，24、285。*另见* 锚点标签

+ 绝对单位，在 CSS 中使用，48–49

action 属性

- 在其中使用 mailto:，149–150
- 与 JavaScript 表单一起使用，148–150

[a-d]，在正则表达式中使用，167

+ addclass.php 脚本，309–310

<address></address> 标签组，19

相邻选择符，示例，44–45

管理员认证脚本。**另见** 课程选择与注册应用程序

- adminAuthen.php，296
- enterName.php，298–300
- enterSite.php，303–304
- register.php，296–298
- signin.php，300–302
- verify.php，302–303

Administrator 表示例，292–293

Adobe Dreamweaver，替代方案，3–6

a:focus，使用，285–286

alert 消息框，使用，125

alert() 方法，使用，107、110、125

align 废弃属性，15

alink 废弃属性，15

alt 属性，描述，25

锚点标签。*另见* <a></a> 标签组

- 示例，24、26
- 与超链接一起使用，24

Apache

- 下载，8
- 使用 XAMPP 安装，8–9

应用程序设计

- 创建 CSS，284–288
- 创建模板，281–284
- 概述，277–278
- 模板的设计，279–280

Aptana PHP 项目，打开，179–180

Aptana Studio

- 向其添加 PHP，172
- 在其中更改 HTML 颜色，16
- 其中的颜色编码标签，16
- 在其中创建文件夹，295
- 在其中创建项目，295
- 在其中创建 X/HTML 文件，93
- 特性，6–7
- 修改其中的默认 HTML 页面，93–96
- 在其中设置 PHP，172–174
- 包含的标签，14
- 对 HTML 的处理，16
- 与 MySQL 一起使用，241
- 与 PHP 一起使用，171

Area 标签，示例，24、26

<area></area> 标签组，描述，26

算术运算符

- 在 JavaScript 中使用，100
- 在 PHP 中使用，188

arr 数据类型，在 PHP 中使用，185

array() 函数，在 PHP 中使用，193

数组函数，在 PHP 中使用，192–193

数组索引，与表单一起使用，157

数组指针，与 foreach 语句一起使用，204

数组值，在 PHP 中标识为键，185

数组。*另见* 表单数组

- 将变量赋值给，133
- PHP 中的数据类型，185
- 作为数据存储机制，133
- 定义和填充，133–135
- 效率，133
- 在 JavaScript 中使用，108
- 与鼠标事件一起使用，132–133

赋值运算符

- 在 JavaScript 中使用，100
- 在 PHP 中使用，188

关联数组，超全局变量作为，218

星号 (*)，在 SQL 中使用，246

属性选择符，示例，43

属性

- 类的属性，41–42
- 废弃属性，15
- <form> 和 </form> 的属性，28
- ID 的属性，41–42
- Image 标签的属性，25
- input 的属性，28
- <input> 的属性，28
- <link /> 和 <style> 标签的属性，39
- <option> 的属性，29
- <select> 和 </select> 的属性，28
- Table 标签的属性，31
- 将 JavaScript 用作属性，124

创作资源，32–33

### B

+ \b，在正则表达式中使用，167

<b></b> 标签组，21

background 废弃属性，15

背景图片，使用，58

背景页面属性，在 CSS 中使用，55、57

反斜杠 (\\)

- 在 JavaScript 中产生，92
- 在 JavaScript 中使用，91–92
- 在 PHP 中使用，183–184、189

退格，在 JavaScript 中产生，92

bgcolor 废弃属性，15

<big></big> 标签组，21

BIGINT 数据类型，在 MySQL 中使用，259

二进制数据类型，在 MySQL 中使用，259、260

位运算符

- 在 JavaScript 中使用，101
- 在 PHP 中使用，188

黑色，十六进制数，50

BLOB 数据类型，在 MySQL 中使用，260

块级框，定义，62–63

<blockquote></blockquote> 标签组，19

蓝色，十六进制数，50

blur() 方法，与表单一起使用，155、158–159

body 属性，在 CSS 中赋值，37

<body></body> 标签组，17

<body> 部分

- 键盘事件处理程序，138
- 在其中命名表单，147
- 与 onfocus 一起使用，128

<body> 标签

- 示例，37
- 与事件处理程序一起使用，123

粗体物理字符，应用，21

书签

- 定义，26
- 作为标签，24

Books 数据库

- 信息，261–262
- 查询，269

Books 表。*另见* 表

- 附加到数据库，250–251
- 数据类型，258
- 字段，245–247
- 键，245

bool 数据类型

- 在 JavaScript 中使用，99
- 在 PHP 中使用，185

布尔数据类型

- 在 JavaScript 中使用，99、112
- 在 PHP 中使用，185

布尔 FALSE 数据类型

- 在 JavaScript 中使用，98–99、112
- 在 PHP 中使用，184–185

布尔 TRUE 数据类型，112

border 属性

- 省略，32
- 在 CSS 中使用，55–57、60

bottom 布局属性，在 CSS 中使用，60

页面布局的盒模型

- 块级元素，62
- 内联级元素，63
- 内边距、边框和外边距，63

<br /> 标签，19

尖括号 (<>，与标签一起使用，16

break 关键字，与 switch 语句一起使用，118、206

浏览器类型，在 PHP 中检查，227–228

浏览器。*另见* Firefox；Internet Explorer (IE)

- 使用率统计差异，97
- CSS 的处理过程，46–48
- 术语，36
- 测试，10
- 测试工作，96–97

bug，在程序中查找，187

项目符号（无序）列表，标签，19

按钮栏，为表单创建，164–166

button 对象，包含在表单上，144

按钮，包含在表单上，144

### C

+ 计算器，在科学模式下使用，51

callalert 函数，定义，133–135

<caption></caption> 标签组，31

caption-side 布局属性，在 CSS 中使用，60

回车，在 JavaScript 中产生，92

级联，覆盖，46

CSS 的级联顺序，46

层叠样式表 (CSS)

- 附加，37–40
- 创建，284–288
- 定义，37
- 示例，37
- 其中的浮动列，68–69
- 水平度量，48–49
- 链接与嵌入，37–38
- 相对单位，48
- 在其中使用伪类，285
- 垂直度量，48–49
```


...


- “浮点错误”，71
- 浮点数据类型
  - 在JavaScript中的使用，99
  - 在PHP中的使用，185
- FLOAT数据类型，在MySQL中的使用，259
- 浮动布局属性，在CSS中的使用，60
- 浮动列
  - 在CSS中，68–69
  - 在HTML中，69
- 浮点数，在JavaScript中的比较，98
- 焦点
  - 定义，127–128
  - 从元素中移除，158–159
  - 设置到字段，158–159
  - 使用onfocus事件处理器，128–129
- focus()方法，与表单一起使用，155, 158–159
- font已弃用标签，15
- font属性来源，使用，53
- 字体大小，按比例缩放元素，48
- font-*文本属性，其值，52
- 字体，在CSS中应用，51–53
- font-weight，其数值，53
- fopen() PHP文件函数
  - 描述，211
  - 模式，212
- for语句
  - 在JavaScript中的使用，116–117
  - 在PHP中的使用，204–205
- foreach语句
  - 在PHP中的使用，204–205
- 外键，在数据库中的使用，245
- 表单元格方法
  - blur()，158–159
  - focus()，158–159
- 表单元格属性
  - defaultValue，154–156
  - options[]，157–158
  - value，157–158
- 表单元素
  - 使用<input>属性添加，147–148
  - 可用性，144
- 表单事件处理器，122
- 表单扩展
  - 菜单栏，164–166
  - 正则表达式，167–168
- form属性，与表单一起使用，155
- 表单验证
  - 概述，159–160
  - 使用onsubmit事件处理器，162
  - 与密码一起使用，160–161
  - validateForm()函数，162–164
- <form></form>标签集
  - 描述，28
  - 使用，145
  - 与其一起使用事件处理器，123
- 表单。另请参阅JavaScript表单
  - 访问，150–152
  - 使用X/HTML创建，145–146
  - 定义，142–143
  - 定义，27–29
  - 设计考虑，144
  - 示例，27–28, 146
  - 完全限定的字段名称，163
  - 识别，150–152
  - 命名和调用示例，148
  - 在线与纸质，143
  - 重置字段，155–156
  - 审查，145
  - 创建规则，144
  - 两部分模型，145
  - 使用数组索引，157
- forms数组，与JavaScript表单一起使用，150–152。另请参阅数组
- frame已弃用标签，15
- 与框架相关的标签，建议，15
- frameset已弃用标签，15
- fread() PHP文件函数，描述，211, 214
- FrontPage，替代品，3
- fseek() PHP文件函数，描述，214–215
- ftell() PHP文件函数，描述，215
- 完全限定的表单字段名称，使用，163
- function关键字，在PHP中的使用，198
- 函数。另请参阅PHP MySQL函数
  - 无参数定义，106
  - 命名，106
- JavaScript中的函数
  - 全局，104–105
  - 用户定义，105–107
- PHP中的函数。另请参阅PHP脚本语言
  - 数组，192–193
  - 日期和时间，193–194
  - 内部，191–192
  - 数学，194–195
  - 字符串，195–197
  - 用户定义，197–199
- fwrite() PHP文件函数，描述，211, 214

### G

- Getdate()函数，在PHP中的使用，193–194
- 全局函数，在JavaScript中的使用，104–105
- GNU通用公共许可证，240
- Google Chrome使用统计，10
- GPL（通用公共许可证），240–241
- 组选择器，示例，45

### H

- <h1>和<h2>标签，示例，37
- <head>部分，与onfocus一起使用，128
- <head></head>标签集，17
- header()函数，与index.php脚本一起使用，230
- 标题，识别，19
- 高度和宽度，指定，24
- height属性，描述，25
- 高度布局属性，在CSS中的使用，60
- Hello World!警报对话框，107
- 十六进制表示法，转换，51
- 隐藏字段，包含在表单中，144
- 隐藏对象，包含在表单中，144
- `<hn></hn>`标签集，19
- 水平线，创建，19
- 热点
  - 定义，26
  - 说明，24
- `<hr>`元素，在模板中缺失，283
- HTML（超文本标记语言），12。另请参阅X/HTML页面
  - 创作资源，32–33
  - 其中的浮动列，68–69
  - 标签放置，16
  - 与XHTML对比，13–15
- HTML页面，在Aptana中修改，93–96
- HTML标签。另请参阅标签
  - 属性，16
  - 已弃用，14–15
  - 放置，16
  - 使用，17
- `<html>`属性，在PHP中的使用，177–178
- `<html></html>`标签集，17
- http-equiv属性，17
- 超链接
  - 定义，26
  - 使用Anchor标签实现，24
- `<i></i>`标签集，21
- id属性，20
- ID选择器
  - 示例，42
  - 在CSS中的使用，41–42
- IE（Internet Explorer）使用统计，10。另请参阅浏览器
- IE 6和7
  - 与MySQL一起使用，241
  - 与PHP一起使用，171
- IE 7和IE 8，下载，10
- IE应用程序兼容性VPC映像，10
- if语句，与表单一起使用，162–164
- if/else语句
  - 在JavaScript中的使用，112–114
  - 在PHP中的使用，199–201
- iframe已弃用标签，15
- IIS（Internet Information Server），7
- 图像标签
  - 属性，25
  - 示例，24
- 图像
  - 分解为部分，24
  - 其中的热点，24
  - 加速加载，24
- img标签，使用，16
- implode()函数，在PHP中的使用，196
- !important声明，在CSS中的使用，46
- in测量单位，在CSS中的使用，48
- include()函数，237, 284
- 递增运算符，在PHP中的使用，189
- 缩进段落，识别，19
- 索引，在数据库中的使用，245
- index.php脚本，使用，230–231
- 继承，应用于CSS，47–48
- `<input>`标签
  - 描述，28
  - 与表单一起使用，147–148
- INSERT SQL语句，示例，247
- int数据类型
  - 在JavaScript中的使用，99
  - 在PHP中的使用，185
- INT数据类型，在MySQL中的使用，259
- 整数，在PHP中的处理，184–185
- Internet Explorer（IE）使用统计，10。另请参阅浏览器
- 插值，在PHP中的使用，189
- 解释型编程语言，83
- 解释型与编译型语言，170
- is_string()函数，在PHP中的使用，196
- isFinite()函数，在JavaScript中的使用，105
- isindex已弃用标签，15
- ismap属性
  - 描述，25
  - 使用，23
- isNaN()函数，在JavaScript中的使用，105
- isset()函数，与index.php脚本一起使用，230
- 斜体物理字符，应用，21
- italic值，与font-style一起使用，53
- 斜体文本，识别，19
- JavaScript表单。另请参阅表单
  - action属性，148–150
  - elements[]属性，152–153
  - forms数组，150–152
  - 识别，147
  - 在网页上命名，147–148
  - 属性和方法，149
  - reset()方法，153–154
  - submit()方法，153–154
- JavaScript对象。另请参阅JavaScript中的对象
- JavaScript编程语言
  - 事件处理器的优势，123
  - 算术运算符，100, 102
  - 赋值运算符，100
  - 用于验证的可用性，160
  - 避免保留字，92–93
  - 位运算符，101
  - 编码约定，90–91
  - 在其中组合运算符，102–103
  - 注释脚本，90
  - 比较浮点数，98
  - 比较变量，102
  - 比较运算符，101
  - 条件表达式，112
  - 构造函数，104
  - 控制结构，111
  - 创建，84
  - 自定义对象，108
  - 数据类型，98–99
  - do-while语句，114–116
  - 直接输入，89
  - 等号（=），102
  - 转义序列，91–92
  - 事件处理器，110–111
  - 表达式，104
  - for语句，116–117
  - 函数，104–107
  - 全局函数，104–105
  - if/else语句，112–114
  - 作为解释型语言，83
  - 语言元素，97
  - 逻辑运算符，101
  - 方法，104, 110
  - 修改默认HTML页面，93–96
  - 模（%）运算符，102
  - 命名约定，99–100
  - 对象，107–108
  - 运算符，100–103
  - 运算符示例，103
  - 运算符优先顺序，102
  - 概述，82–84
  - 属性，109–110
  - 脚本放置示例，89
  - 分隔参数，91
  - 特殊字符，91–92
  - 语句，104
  - 字符串，91
  - switch语句，118–119
  - 三元运算符，114
  - 测试，96–97
  - 测试相等性，112
  - this关键字，108
  - 所需工具，84–85
  - 故障排除，100
  - 用户定义函数，105–107
  - 使用<!-- //-->注释，91
  - 作为属性使用，124
  - 与运算符一起使用括号，102
  - 在其中使用正则表达式，167–168
  - 在其中使用相同代码，105
  - 变量示例，103
  - while语句，114–116
- join()函数，在PHP中的使用，196
- JS文件，在其中使用代码，90

### K

- <kbd></kbd>标签集，21
- 键盘事件处理器，122, 138–140
- 键
  - 在数据库中，245
  - 与超全局变量一起使用，218
- SQL中的关键字，246

### L

- 布局属性，在CSS中的使用，59–61
- 左布局属性，在CSS中的使用，60
- length属性
  - 用于命名表单，147
  - 与forms数组一起使用，150–152
  - 与JavaScript表单一起使用，149
- Lerdorf, Rasmus, 170
- letter文本属性，其值，52
- <li></li>标签集，19
- 换行，强制，19
- 行尾，忽略，21
- 换行符，在JavaScript中产生，92
- line-height文本属性
  - 示例，53
  - 其值，52
- <link />标签，描述，39
- 链接栏，为表单创建，164–166
- link已弃用属性，15
- link伪类，使用，285
- <link>标签
  - 示例，37, 40
  - 与其一起使用事件处理器，123
- Linux与Mac和Windows用户，2
- 列表项，应用背景，80
- 列表属性，使用，80
- 列表
  - 字母系统，80
  - 示例，78–79
  - 嵌套列表，78–79
  - 编号系统，80
  - 样式化，77–80
  - 与表格对比，73
- list-style-*布局属性，在CSS中的使用，60–61
- 图像的加载，加速，24



### M

- location 选择器，示例，45
- 在 PHP 中使用 `log()` 函数，195
- 逻辑运算符
  - 在 JavaScript 中使用，101
  - 在 PHP 中使用，189
- 在 MySQL 中使用 `LONGBLOB` 数据类型，260
- 在 MySQL 中使用 `LONGTEXT` 数据类型，260
- 循环结构
  - `for` 语句，116–117
  - `while` 和 do-while 语句，114–116
- 在 PHP 中使用 `ltrim()` 函数，196

- Mac 与 Linux 和 Windows 用户的对比，2
- `mailto` 结构
  - 在 action 属性中使用，149–150
  - 与模板一起使用，281–282
- MAMP 网站，8
- Map 标签
  - 内容，24
  - 示例，24、26
- `<map></map>` 标签，描述，26
- 在 CSS 中使用 `margin-*` 布局属性，61
- 标记标签。*参见* tags
- 在 PHP 中使用 math 函数，194–195
- 在 CSS 中使用 `max-*` 布局属性，61
- 在 MySQL 中使用 `MEDIUMBLOB` 数据类型，260
- 在 MySQL 中使用 `MEDIUMINT` 数据类型，259
- 在 MySQL 中使用 `MEDIUMTEXT` 数据类型，260
- 在 PHP MySQL 中释放内存，268
- 为表单创建菜单栏，164–166
- menu 已弃用标签，15
- 消息
  - 使用 `onunload` 事件处理程序创建，126–127
  - 为关闭的页面显示，125–127
  - 为打开的页面显示，125–127
- `<meta>` 标签
  - 描述，17
  - 在 PHP 中使用，177–178
- 使用 JavaScript 表单的 method 属性，149
- 方法
  - 与属性区分，110
  - 在 JavaScript 中使用，104
- Microsoft Expression Web，3
- 关于 Microsoft Word 的提示，3
- 在 CSS 中使用 `min-*` 布局属性，61
- 在 CSS 中使用 mm 单位，48
- 使用模态对话框，125
- 取模 (%) 运算符
  - 在 JavaScript 中使用，102
  - 在 PHP 中使用，187

- 鼠标点击的事件处理程序，136
- 鼠标事件
  - 解释，122
  - `ondblclick`，135
  - 与数组一起使用，132–133
- 用鼠标指针触发事件，136–138
- Mozilla Firefox。*参见* Firefox
- MySQL。*参见* PHP MySQL functions; SQL (Structured Query Language)
  - 在命令行上构建表，249–251
  - 命令行客户端，248–249
  - 连接到 MySQL，266–267
  - 数据类型，259–260
  - 包含在 XAMPP 中，7
  - 使用 XAMPP 安装，8–9
  - 概述，240–241
  - 安全系统，253–254
  - 所需工具，241–242
- `mysql` 和 `mysqli`，265
- 在 PHP 中使用 MySQL 数据库，265–266

### N

- name 属性
  - 描述，17
  - 与表单一起使用，155
  - 与 JavaScript 表单一起使用，149
- `&nbsp;`，解释，23–24
- `noframes` 已弃用标签，15
- 包含不间断空格，23–24
- 规范化字段，246
- 使用记事本，2
- `null` 数据类型
  - 在 JavaScript 中使用，99
  - 在 PHP 中使用，185
- NULL 与空白 (`""`) 值，258
- 在 PHP 中使用 `number_format()` 函数，196
- 编号（有序）列表的标签，19
- 数值数据类型
  - 在 JavaScript 中使用，99
  - 在 MySQL 中使用，259
  - 在 phpMyAdmin 中使用，258

### O

- 在 PHP 中使用 `object` 数据类型，185
- 在 JavaScript 中使用对象初始化器，108
- JavaScript 中的对象
  - 应用属性，109–110
  - 自定义对象，108
  - 预定义对象，107
  - 属性与方法，110

- 在 PHP 中表示八进制数，184
- `<ol></ol>` 标签组，19
- on* 事件处理程序
  - 用于表单，140
  - 用于键盘，138
  - 用于鼠标，132
  - 在 JavaScript 中使用，111
  - 用于窗口，124
- 使用 onblur 事件处理程序，129–130
- 使用 onchange 事件处理程序处理下拉菜单，166
- onclick 和数组示例，134–135
- onclick 事件处理程序
  - 与 blur() 方法一起使用，158–159
  - 与 focus() 方法一起使用，158–159
  - 与 defaultValue 属性一起使用，155–156
- 添加 ondblclick 事件处理程序，135
- 使用 onfocus 事件处理程序，128–129
- onkeyup 示例，139–140
- onmousedown 事件，解释，136
- onmouseout 示例，137
- onmouseover 示例，137
- onmouseup 事件，解释，136
- 使用 onresize 事件处理程序，130–131
- 在验证中使用 onsubmit 事件处理程序，162
- 使用 onunload 事件处理程序，126–127
- Opera 使用统计，10
- 运算符
  - 在 JavaScript 中组合，102–103
  - PHP 中的示例，190–191
  - 在 PHP 中使用，187–191
- `<option>` 标签，描述，29
- 使用 options[] 属性处理表单，155、157–158
- 有序（编号）列表的标签，19
- 在 CSS 中使用 orphans 页面属性，56、58
- 在 CSS 中使用 outline-* 页面属性，56、58
- 在 CSS 中使用 overflow 页面属性，56

### P

- `<p></p>` 标签组，19
- 为边框添加 padding，57
- padding 框，解释，63
- 在 CSS 中使用 padding-* 布局属性，61
- 页面布局
  - 盒模型，62–65
  - 视觉模型，62–65
- 页面属性
  - 示例，59
  - 在 CSS 中使用，55–58
- 页面术语，36
- 在 CSS 中使用 page-break-* 页面属性，56、58

- 设置段落样式，18–20
- 括号 (())
  - 在 PHP 中使用，187
  - 与三元运算符一起使用，202
- 在 JavaScript 中使用 parseFloat() 函数，105
- 在 JavaScript 中使用 parseInt() 函数，105
- 在表单中包含密码字段，144
- 在表单中包含 password 对象，144
- 密码
  - 在 phpMyAdmin 中更改，253–256
  - 比较表单密码，163
  - 在 phpMyAdmin 中设置，253–256
  - 使用密码验证，160–164
- 在 CSS 中使用 pc 单位，48
- 句点 (.), 与类选择器一起使用，41–42
- `<?php ... ?>`，解释，177
- PHP 控制结构
  - do-while 语句，202–203
  - for 语句，204–205
  - foreach 语句，204–205
  - if/else 语句，199–201
  - switch 语句，206–207
  - 三元运算符，201–202
  - while 语句，202–203
- .php 扩展名，解释，177
- PHP 文件函数，211–217
- 在单独行上显示 PHP 文件，213
- 访问 PHP 手册，210
- PHP MySQL 函数，269。*参见* functions; MySQL
  - 组合使用，272–274
  - 完成查询，268
  - 连接到 MySQL，266–267
  - 数据库管理，271–272
  - 数据库信息，270–271
  - 数据库操作，265–266
  - 释放内存，268
  - 执行查询，268
  - 处理结果，268
  - 查询 Books 数据库，269
  - 选择数据库，267
- PHP 运算符
  - 算术运算符，188
  - 赋值运算符，188
  - 位运算符，188
  - 比较运算符，188–189
  - 增量运算符，189
  - 逻辑运算符，189
- PHP 脚本语言。*参见* functions in PHP
  - 添加到 Aptana，172
  - 数组值作为键，185
  - Boolean FALSE 数据类型，184–185
  - 检查浏览器类型，227–228
  - 编码约定，183–184
  - 注释脚本，182
  - 常量，186–187
  - cookie，217、220–224
  - 数据类型，184–185
  - 调试程序，187
  - 调试脚本，180
  - 显示信息，180–182
  - PHP 中的双等号 (==)，187
  - echo() 函数，180–182
  - PHP 中的等号 (=) 运算符，187
  - PHP 中的转义序列，183
  - 转义变量名，189
  - 示例，177–178
  - 表达式，191
  - 包含在 XAMPP 中，7
  - 信息类型，184–185
  - 使用 XAMPP 安装，8–9
  - PHP 中的整数，184–185
  - 与 X/HTML 集成，177–178
  - 关键字，186
  - 将数字设为八进制，184
  - "mixed" 伪类型，185
  - PHP 中的取模 (%) 运算符，187
  - "numbers" 伪类型，185
  - PHP 中的优先级顺序，187
  - 概述，170–171、176–177
  - print() 函数，180–182
  - 规则，177
  - 服务器变量，224–228
  - 会话变量，218–220
  - 在 Aptana 中设置，172–174
  - 语句，191
  - 测试相等性，200
  - 所需工具，171–172
  - PHP 中字符串的处理，183
  - 使用 MySQL 数据库，265–266
  - 在 PHP 中使用括号 (())，187
  - 变量，186–187
  - 编写和测试，179–180

- 默认排序规则，261
- 删除记录，262
- 打开和浏览，252–253
- 概述，251–252
- 查询表，262–264
- 红色 X 图标，262
- 设置权限，253–256
- 文本字段，259
- 使用字段定义，256–257

- absolute（绝对定位），66
- fixed（固定定位），66
- float（浮动定位），66–72
- normal flow（正常流），65–66
- relative（相对定位），66

PHP 脚本，关闭代码，214。*参见* scripts

PHP 用户认证。*参见* User Authentication scripts

- enterName.php 脚本，233–234
- enterSite.php，237–238
- index.php 脚本，230–231
- 概述，228–230
- register.php 脚本，231–234
- signin.php 脚本，234–236
- 站点页面，237–238
- 系统流程图，228–229
- verify.php 脚本，236–237

phpMyAdmin GUI

- 向表中添加记录，261–262
- 浏览表，262–263
- 构建表，289–293
- 创建数据库，256–261
- 创建表，256–261

`<pre></pre>` 标签组，20

主键，数据库中的，245

print() 函数

- 示例，181–182
- 在 PHP 中使用，180

print_r() 函数，在 PHP 中使用，193

权限，在 phpMyAdmin 中设置，253–256

编程语言，类型，83

属性

- 与方法区分，110
- 在 JavaScript 中使用，109–110

伪类，在 CSS 中使用，285

pt 单位，在 CSS 中使用，48

px（像素）单位，在 CSS 中使用，48

### Q

在 PHP MySQL 中执行查询，268

引号。*参见* 双引号 ("); 单引号 (')

### R

在表单中包含单选按钮，144

在表单中包含 radio 对象，144

在 PHP 中使用 rand() 函数，195

RDBMS（关系数据库管理系统），245–246。*参见* MySQL

记录

- 在 phpMyAdmin 中向表添加记录，261–262
- 数据库中的，245
- 在 phpMyAdmin 中删除，262

红色，十六进制数，50

刷新窗口，130–131

regex，与表单一起使用，167–168



### R

- RegExp，在表单中使用，167–168
- register.php 脚本
  - 修改，296–298
  - 使用，231–233
- 注册 CSS
  - 其中的 `<a>` 标签，285
  - 示例，286–288
- 注册表示例，291–292
- 正则表达式，在表单中使用，167–168
- 相对单位，在 CSS 中使用，48–49
- require() 函数，237，284
- require_once，使用，303，307，311，314，335
- 保留字，在 JavaScript 中避免使用，92–93
- 重置按钮，在表单上包含，144
- reset() 方法
  - 在表单中使用，153–154
  - 在 JavaScript 表单中使用，149，153–154
- reset 对象，在表单上包含，144
- resource 数据类型，在 PHP 中使用，185
- $result 变量，在 PHP MySQL 中使用，268
- return 语句
  - 表单中的示例，164
  - 在 PHP 中使用，198
- rewind() PHP 文件函数，描述，211
- RGB 颜色，指定，50
- right 布局属性，在 CSS 中使用，60
- root 用户，设置密码，253–254
- round() 函数，在 PHP 中使用，195
- run-in 值
  - 示例，65
#line 62	col 1
  - 与 display 属性一起使用，64

### S

- s 已弃用标签，15
- Safari 使用统计，10
- `<samp></samp>` 标签集，21
- 科学模式，在计算器中使用，51
- 屏幕，术语，36
- 脚本与代码，89
- `<script>` 标签，与 JavaScript 一起使用，89
- 脚本。参见 PHP 脚本
  - addclass.php，309–310
  - adminAuthen.php，296
  - checkemail.php，323–324
  - classdelete.php，316–317
  - classentry.php，307–309
  - classlist.php，311–312
  - classupdate.php，314–315
  - 在 PHP 中添加注释，182–183
  - confirm.php，331–333
  - 在 PHP 中调试，180
  - deleteclass.php，317
  - emailentry.php，321–322
  - emailvalid.js，322–323
  - enterName.php，298–300
  - enterSite.php，303–304
  - enterstu.php，326–327
  - register.php，296–298
  - sendemail.php，333–335
  - 在脚本中设置时区，282
  - signin.php，300–302
  - stuentry.php，324–326
  - stuupdate.php，327–329
  - systementry.php，304–306
  - updateclass.php，315–316
  - updatestu.php，330
  - verify.php，302–303

- 选择框，在表单上包含，144
- select() 方法，在表单中使用，155
- select 对象，在表单上包含，144
- `<select></select>` 标签集，28
- selectedIndex 属性，在表单中使用，155
- 选择器类型
  - 相邻，44–45
  - 属性，43
  - 子元素，44
  - 类和 ID，41–42
  - 上下文，43–44
  - 事件，42–43
  - 第一个子元素，44
  - 组，45
  - 位置，45
- 选择器，指定，45

- 分号 (;)
  - 在 JavaScript 中使用，91
  - 在 PHP 脚本中使用，183
- sendemail.php 脚本，333–335
- $_SERVER 超全局数组，224
- 服务器变量。参见变量
  - 与 cookie 对比，218
  - 生成，224–226
  - 与会话变量对比，218
  - 在 PHP 中使用，218–220，224–228
- 服务器端与客户端计算，83–84
- 服务器端特性，使用，6–7
- 会话变量。参见变量
  - 与 cookie 对比，218
  - 与服务器变量对比，218
  - 在 PHP 中使用，218–220
- session_start() 函数，使用，300
- SET 数据类型，在 MySQL 中使用，260
- Set 数据类型，在 MySQL 中使用，260
- setcookie() 函数
  - 其中的 name 参数，221
  - 在 PHP 中使用，220–221
  - 其中的 value 参数，221
- shape 属性，省略，26
- signin.php 脚本，300–302
- signin.php 脚本，使用，234–236
- 单引号 (')
  - 在 JavaScript 中产生，92
  - 在 PHP 中使用，183–184，189
  - 在 phpMyAdmin 中使用，256
  - 与非数字值一起使用，300
  - 与字符串一起使用，92
- 站点模板示例，283–284
- 斜杠 (/)，与标签一起使用，16
- `<small></small>` 标签集，21
- SMALLINT 数据类型，在 MySQL 中使用，259
- 空格，使用 `&nbsp;` 添加，23–24
- 特殊字符
  - 显示，21–22
  - 在 JavaScript 中使用，91–92
- SQL（结构化查询语言），246–247，300。参见 MySQL
- SQL 语句，示例，247。参见语句
- src 属性
  - 描述，25
  - 与 `<img>` 标签一起使用，16
- 语句。参见 SQL 语句
  - 在 JavaScript 中的处理，91
  - 在 JavaScript 中使用，104
  - 在 PHP 中使用，191
- Stein, Bob，51
- str_split() 函数，在 PHP 中使用，196
- XHTML 的严格级别，使用，15
- `<strike>` 已弃用标签，15
- string 数据类型
  - 在 JavaScript 中使用，99
  - 在 PHP 中使用，185
- 字符串函数，在 PHP 中使用，195–197
- 字符串
  - 在 PHP 中作为数字，185
  - 在 PHP 中的处理，183–184
  - 使用引号，92
  - 在 PHP 中验证，228
- `<strong></strong>` 标签集，21
- strpos() 函数，在 PHP 中使用，228，236
- 结构化查询语言 (SQL)，246–247，300
- Strval() 函数，在 PHP 中使用，196
- Student 表示例，290–291
- stuentry.php 脚本，324–326
- stuupdate.php 脚本，327–329
- `<style></style>` 标签集
  - 描述，39
  - 示例，37–39
- `<sub></sub>` 标签集，21
- 提交按钮，在表单上包含，144
- submit() 方法
  - 在表单中使用，153–154
  - 在 JavaScript 表单中使用，149，153–154
- submit 对象，在表单上包含，144
- `<sup></sup>` 标签集，21

- 超全局变量，在 PHP 中使用，218
- switch 语句
  - 使用的关键字，206
  - 在 JavaScript 中使用，118–119
  - 在 PHP 中使用，206–207
- systementry.php 脚本，304–306

### T

- 制表符，在 JavaScript 中产生，92
- 表格背景，覆盖，74
- 表格格式，层次结构，73
- 表格分组元素，使用，75
- `<table></table>` 标签集，31
- table-layout 属性，在 CSS 中使用，61
- 表格。参见 Books 表
  - 添加记录到，261–262
  - 应用样式到，74–75
  - 附加到数据库，250
  - 在 phpMyAdmin 中构建，289–293
  - 在 MySQL 命令行上构建，248–251
  - 创建，29–32，289–293
  - 在 phpMyAdmin 中创建，256–261
  - 在数据库中，245–246
  - 示例，29–30，75–77
  - 与列表对比，73
  - 在 phpMyAdmin 中查询，262–264
- 标签。参见 HTML 标签
  - 添加事件处理程序到，123
  - 书签，24
  - for，38–39
  - 作为超链接，24
- target 已弃用属性，15
- target 属性，与 JavaScript 表单一起使用，149
- `<td></td>` 标签集，31
- template.php 文件，复制，294
- 模板
  - 创建，281–284
  - 设计，279–280
- 三元运算符 (?:)
  - 在 JavaScript 中使用，114
  - 在 PHP 中使用，201–202
- Test 数据库，使用，250
- 测试服务器，选择，6–9
- 文本，在 CSS 中对齐，54–55
- 文本区域
  - 在其中显示默认值，154–156
  - 在表单上包含，144
- 文本框
  - 在其中显示默认值，154–156
  - 在表单上包含，144
- TEXT 数据类型，在 MySQL 中使用，259
- Text 数据类型，在 MySQL 中使用，259–260
- `<u>text</u>` 已弃用属性，15
- 文本编辑器，选择，2–6
- text 对象，在表单上包含，144
- 文本属性，表格，52
- textarea 对象，在表单上包含，144
- text-indent 属性，在 CSS 中使用，54
- `<th></th>` 标签集，31
- this 关键字
  - 在 JavaScript 中使用，108
  - 与表单一起使用，153
- this.form，使用，153–154
- TIME 数据类型，在 MySQL 中使用，260
- time() 函数，在 PHP 中使用，193–194
- 时区，在脚本中设置，282
- TIMESTAMP 数据类型，在 MySQL 中使用，260–261
- TINYBLOB 数据类型，在 MySQL 中使用，260
- TINYINT 数据类型，在 MySQL 中使用，259
- TINYTEXT 数据类型，在 MySQL 中使用，259
- title 标签，示例，16
- `<title></title>` 标签集，17
- top 布局属性，在 CSS 中使用，60
- `<tr></tr>` 标签集
  - 描述，31
  - 分隔，30
- 触发器。参见事件
  - 表单事件处理程序的，140
  - 键盘事件处理程序的，138
  - 与事件处理程序一起使用，110–111
  - 窗口事件的，124
- TRUE 布尔值，112
- true，为 validate() 表单返回，163–164
- `<tt></tt>` 标签集，21
- type 已弃用属性，15
- type 属性，与表单一起使用，155
- 打字机文本样式，应用，21

### U

- u 已弃用标签，15
- `<ul></ul>` 标签集，19
- undefined 数据类型，在 JavaScript 中使用，99
- 下划线 (_)
  - 在 JavaScript 中使用，99
  - 与用户定义函数一起使用，198
- unescape() 函数，在 JavaScript 中使用，105
- 度量单位，在 CSS 中使用，48–49
- 无序（项目符号）列表，标签，19
- UPDATE SQL 语句，示例，247
- updateclass.php 脚本，315–316
- updatestu.php 脚本，330
- URL，为 blockquote 标识，19
- usemap 属性，描述，25
- 用户认证脚本，导入，295–296。参见 PHP 用户认证
- 用户定义函数
  - 在 JavaScript 中使用，105–107
  - 在 PHP 中使用，197–199

### V

- validateForm() 函数，使用，162–164
- 验证表单。参见表单验证
- value 属性，与表单一起使用，155，157–158
- 值，与变量比较，118
- VARCHAR 数据类型，在 MySQL 中使用，259
- 变量名，在 PHP 中转义，189
- 变量。参见服务器变量；会话变量
  - 赋值给数组，133
  - 在 JavaScript 中比较，102
  - 与值比较，118
  - PHP 中的示例，190–191
  - 在 JavaScript 中使用，98–100
  - 在 PHP 中使用，186–187
- verify.php 脚本，236–237，302–303
- vertical-align 属性
  - 在 CSS 中使用，55
  - 值，52
- visibility 布局属性，在 CSS 中使用，61
- VisiBone，51
- Vista，下载 IE，10
- 页面布局的可视化模型
  - 框生成，64
  - 包含块，64
  - run-in 框，64
  - 视口，63
- vlink 已弃用属性，15

### W

- W3C 标准，合规性，16
- W3C 网站，13
- Web 开发工具
  - 选择，2–6
  - 特性，4–6
- Web 页面
  - 块级元素，62
  - 显示，3
  - 关闭时显示消息，125–127
  - 打开时显示消息，125–127
  - 元素，62–63
  - 行内级元素，63
  - 在其上命名 JavaScript 表单，147–148
  - 重新加载，130–131
  - 术语，36
- Web 安全色板（216 色），51
- Web 服务器，替代方案，7
- 网站
  - Apache 下载，8
  - 创作资源，32–33
  - 颜色图表，51
  - CSS 颜色名称，50
  - CSS（层叠样式表），80



 date() function codes for PHP, 194
- development packages, 4
- Firefox, 10
- font substitutions, 51
- IE 7 for Windows XP, 10
- JavaScript language elements, 97
- MAMP, 8
- PHP, 171
- PHP elements, 183
- PHP file functions, 217
- PHP functions, 191
- PHP manual, 210
- PHP MySQL functions, 265
- PHP server variables, 228
- server variables in PHP, 228
- W3C, 13
- World Wide Web Consortium, 13

- World Wide Web Consortium, 13
- write statements, using with forms, 148, 151
- WYSIWYG page layout, 3

### X

- XAMPP
  - features of, 7
  - getting and installing, 8–9
  - MySQL 5.1.30 in, 241
  - using with MySQL, 241, 248
  - using with PHP, 171
  - verifying running of, 9
  - version for Mac OS X, 8
- x-height, scaling elements to, 48
- X/HTML
  - frameset implementation, 15
  - versus HTML, 13
  - integrating PHP with, 177–178
  - rules, 13–14
  - strict implementation, 15
  - transitional implementation, 15
- X/HTML 1.0 second edition, 13
- X/HTML files, creating in Aptana, 93
- X/HTML pages. See also HTML (Hypertext Markup Language)
  - attaching CSS to, 37–40
  - with <link> tag, 40
  - with <style> tag, 38–39
- X/HTML tags. See tags
- XML (Extensible Markup Language), 12
- XML 1.1, recommendation of, 13

- while statements
  - using in JavaScript, 114–116
  - using in PHP, 202–203
- White, hexadecimal numbers for, 50
- white-space property
  - using in CSS, 55
  - values for, 52
- widows page property, using in CSS, 56, 58
- width and height, specifying, 24
- width attribute, described, 25
- width layout properties, using in CSS, 60
- window events, 122. See also event handlers
  - onblur, 129–130
  - onfocus, 128–129
  - onload, 125–126
  - onunload, 126–127
  - placing focus, 127–128
  - removing focus, 127–128
  - triggers, 124
- windows
  - blurred, 127–128
  - focus of, 127–128
  - refreshing, 130–131
  - resizing, 130–131
- Windows Notepad, 2–3
- Windows versus Linux and Mac users, 2
- Windows Vista, downloading IE for, 10
- Word, advisory about, 3
- word-spacing text property, values for, 52

### Y

- YEAR data type, using in MySQL, 260

### Z

- z-index layout property, using in CSS, 61

## Take Your Web Design Skills to the Next Level!

Master XHTML, CSS, JavaScript, PHP, and MySQL with ease. *Dynamic Web Programming: A Beginner's Guide* shows you everything you need to know to program web pages that respond to user input. Create rollover events and pop-ups, and validate forms, with JavaScript. Use PHP for cookies, server variables, page transitions, and user authentication. Store, supply, and vary website content with MySQL. This hands-on guide includes JavaScript, PHP, and MySQL scripts that allow you to build a comprehensive relational database application. Download these scripts plus their template and CSS for free from www.mhprofessional.com/computingdownload or www.matthewstechnology.com

## Essential Skills—Made Easy

- Strengthen your knowledge of HTML, XHTML, and CSS
- Add dynamic elements to your web pages with JavaScript, PHP, and MySQL
- Enhance your site with user authentication, form validation, information interchange, and web automation
- Add extensive database capability with PHP and MySQL and create relational database applications

**Marty Matthews** is the author or co-author of more than 70 books, including the bestselling *Windows Vista QuickSteps* and *Microsoft Office FrontPage 2003: The Complete Reference*. He has more than ten years of experience working with dynamic web technologies.

**John Cronan** has been working with computers for more than 30 years. His books include *Microsoft Office Excel 2007 QuickSteps*, *Build an eBay Business QuickSteps*, and others.

Learn more. Do more.
MHPROFESSIONAL.COM

Programming

Cover Design: Jeff Weeks
