
# PHP 精选：面向对象的 PHP 解决方案卷 1

![](img/80d007a3dc499b219e99d11695c2c366_0_0.png)

![](img/80d007a3dc499b219e99d11695c2c366_0_1.png)

作者：Harry Fuecks

这部分《PHP 选集：面向对象的 PHP 解决方案》第一卷的节选包含了内容摘要、作者及 SitePoint 信息、目录、序言、书中 3 章内容以及全部 4 个附录。

您还应该收到一个单独的文件，其中包含《PHP 选集：面向对象的 PHP 解决方案》的节选。

我们希望这些《PHP 选集：面向对象的 PHP 解决方案》第二卷的信息对您有所帮助。

更多信息请访问 `sitepoint.com`

Harry Fuecks

作者 Harry Fuecks

![](img/80d007a3dc499b219e99d11695c2c366_5_0.png)

## 关于作者

Harry 是一位技术作家、程序员和系统工程师。他自 1994 年起就开始从事企业 IT 工作，拥有物理学学学位。他首次在 1999 年接触 PHP 是为了构建一个小型内网。如今，他是一个企业外网的主开发人员，PHP 在交付许多后台系统方面发挥着重要作用。

在业余时间，为 SitePoint 编写技术文章并运行 `phpPatterns` (`http://www.phppatterns.com/`)，这是一个探索 PHP 应用设计的网站。

他来自英国，现住在瑞士。今年 5 月，Harry 成了一个漂亮女儿的父亲，这让他整天（甚至深夜）都很忙

## 关于技术编辑

作为 SitePoint 的技术总监，Kevin Yank 监督其所有的技术出版物——书籍、文章、时事和博客。他为 SitePoint 写过关于 PHP、XML、.NET、Java、JavaScript 和 CSS 等技术的 50 多篇文章，最广为人知的是为 SitePoint 出版的《使用 PHP & MySQL 构建自己的数据库驱动网站》一书。Kevin 现在住在澳大利亚墨尔本。在空闲时间，他喜欢驾驶轻型飞机和学习即兴表演的艺术。加油，你这大红大火！

## 关于 SitePoint

SitePoint 专注于为 Web 专业人士出版有趣、实用且易于理解的内容。访问 `http://www.sitepoint.com/` 访问我们的书籍、时事通讯、文章和社区论坛。

献 Natalie 和 Masha

### 1. PHP 基础

### 2. 面向对象 PHP

## PHP 选集

### 3. PHP 与 MySQL

点击此处订购《PHP 选集》第一卷和第二卷，可享 75 折优惠！

### 4. 文件

### 5. 文本处理

## PHP 精选

### 6. 日期与时间

- 我如何在 MySQL 中存储日期？

### 7. 图像

### 8. 电子邮件

### 9. 网页元素

### 10. 错误处理

## PHP 选集

安装 PEAR

PEAR 软件包管理器

手动安装包

- 索引

## 前言

PHP 的伟大之处之一在于其充满活力且活跃的社区。开发者拥有许多在线交流聚集点，包括 [SitePoint 论坛][1](`http://www.sitepointforums.com/`)，开发者在那里聚在一起，帮助彼此解决每天面临的问题，从 PHP 工作的基本知识，到解决如“我如何验证表单？”之类的设计问题。作为获取帮助的一种，这些社区是非常出色的——它们充满了你使项目成功所需的各种关键碎片。然而，将所有这些知识整合成适用于你特定情况的解决方案可能是一个难题。通常，社区成员会假设他人也具有某种程度的知识；你可能经常花费大量的时间从各种帖子、线程和用户处（每个人的编程风格都不同）收集代码段，以获得完整的全貌。

与其他 PHP 书籍的不同之处在于，它摒弃了教程风格，转而关注如何以最小的努力实现实际目标。在某种程度上，你应该能够以或或“即插即用”的方式使用这里提供的许多解决方案，而无需从头到尾读完。

尽管如此，在这些讨论中贯穿着一个“隐藏目标”。除了解决方案，本书还向你介绍了一些可以节省精力的技术，帮助你缩短完成以及后期维护 Web 端 PHP 应用程序的时间。

尽管 PHP 最初被视为过程化编程语言，但近年来，PHP 证明其作为开发面向对象解决方案的语言已日益成功。2003 年 1 月 PHP 应用和扩展库[2](`http://pear.php.net/`)（PEAR）的开放进一步加强了这一点，它为全球 PHP 开发者经常遇到的架构问题（如 Web 表单生成和验证）提供了日益增多的的可重用且维护良好的解决方案集。

[1] `http://www.sitepointforums.com/`

[2] `http://pear.php.net/`

面向对象的范式似乎让许多 PHP 开发者感到恐惧，并且通常被视为所有 PHP 大师的“禁区”。本书将向你展示的是，你不需要计算机科学学位就可以利用如今 PHP 中丰富的类库。在本书提供的解决方案的开发过程中，只要可能，我都利用了一些我个人认为好用的免费库，这些库为我节省了数小时的开发时间。使用他人开发的类通常与使用 PHP 提供的任何内置函数一样简单。

本书对利用可重用组件构建你的 PHP Web 应用程序的强调，反映了与许多 PHP 相关书籍关注点的又一次偏。尽管你还没有发现关于面向对象设计的广泛讨论，但通过读完《PHP 选集：面向对象的 PHP解决方案》第一卷和第二卷，通过渗透的过程，可以帮助你将 PHP 编码技能提升到新水平，指引你构建经受住时间考验的应用。

《PHP 选集：面向对象的 PHP解决方案》第一卷将为你提供在操作 PHP 引擎时所需的信心的要要素，包括一个关于使用 PHP 进行面向对象编程的快速入门指南（第 2 章）。在完成这些准备后，本书将介绍适用于所有基于 PHP 的 Web 应用程序的解决方案，你可能已经了解它们的要要素，但尚未完全掌握。

### 谁应该读这本书？

如果你已经开始尝试 PHP（涉足水），可能读过 Kevin Yank 的《使用 PHP & MySQL 构建你自己的数据库网站》（SitePoint, ISBN-0-9579218-1-0）并完成了你的第一或两个 PHP 项目，那么这本书适合你。

具有更丰富 PHP 经验的读者可能希望跳到《PHP 选集：面向对象的 PHP解决方案》第二卷，学习如何使用 PHP 的一些更高级的功能，并在需要解释更基础的概念时回看《PHP 选集：面向对象的 PHP解决方案》第一卷。

### 本书中涵盖了什么？

以下是你在本卷的每个章节中可以找到的内容：

#### 第 1 章：PHP 基础

本章总结了你为了在 PHP 中快速上手所需的所有要素，从如何使用手册、理解 PHP 错误信息到`include`是如何工作的。还有一些关于编写可移植代码的提示，我们将查看主要的 PHP 配置。

#### 第 2 章：面向对象 PHP

第二章包含了对 PHP 类语法的概述，以及一个解释了面向对象范式的关键元素如何应用于 PHP 的入门。这是阅读本选集后续章节的必要准备。

#### 第 3 章：PHP 与 MySQL

本章为你提供了 MySQL（PHP 最喜爱的数据库）的所有要素。我们从基础开始，涵盖了如何避免 SQL 注入攻击等重要话题。然后我们深入探讨许多不为人知的主题，例如 MySQL 全文检索功能、如何修复表和备份数据库，以及如何使用 `PEAR::DB_DataObject` 避免编写 SQL。本章还作为设计用于连接和查询 MySQL 数据库的类的“案例研究”。

#### 第 4 章：文件

本章是 PHP 中处理文件的生存指南。在这里，我们将涵盖从访问本地文件系统到使用 PHP 的 FTP 客户端从网络获取文件的所有内容。我们将学习如何 `PEAR::Archive_Tar` 创建你自己的压缩包。

#### 第 5 章：文本处理

本章涵盖了处理网站内容的要要素。我们将讨论你可以舍弃的字符串函数，以及用于验证和过滤用户提交内容的专业方法。我们将查看你如何实现一个 BBCode 系统，并理解防止跨脚本攻击涉及的实际操作问题。

#### 第 6 章：日期与时间

在这里，你将学习如何在数据库中存储日期，以及如何使用 PHP 的日期函数。我们将处理处理不同时区的细微差别，并实现一个在线日历。我们将看到在没有命令行访问的情况下，在网站上运行批作业是多么简单，以及如何进行简单的脚本性能测量。

序言

#### 第 7 章：图像

本章探索了缩略图的创建，以及如何在你的网站上为图像“水印”。我们还将讨论如何防止其他网站的盗链（热链），并使用 JpGraph 生成一些专业的图表和图形。

#### 第 8 章：电子邮件

在本章中，我们将专门处理电子邮件相关的解决方案，向你展示如何利用 PHP 充分利用电子邮件。我们将学习使用 PHP Mailer 成功发送 HTML 电子邮件和附件，并使用 PHP 轻松处理发送到你的 Web 服务器的邮件。

#### 第 9 章：网页元素

本章涵盖了网页和导航的核心要素，例如使用`PEAR::HTML_Table`创建表格，以及结果集的实现。我们将讨论使用`PEAR::HTML_QuickForm`开发表单，深入探讨文件上传的处理以及导航菜单的构建。我们还将查看一些可以使用 Apache 的技巧来生成搜索引擎友好的 URL。

#### 第 10 章：错误处理

在这个内容丰富的章节中，你将了解 PHP 的报告机制、如何利用 PHP 的自定义错误处理功能，以及如何优雅地处理错误。

### 本书网站

支持本书的网站位于 `http://sitepoint.com/books/phpant/`，你将可以通过以下功能：

#### 代码存档

随着学习的进行，你会注意到很多处对代码存档的引用。这是一个可以下载的 ZIP 压缩包，包含了书中展示的所有示例的完整代码。

除了 PHP 脚本本身，存档中还包含许多共享库，它们被封装在`SPLIT`目录中。为了让依赖这些库的脚本能够按预期工作，你需要将此目录添加到 PHP 的`include_path`中（有关`include_path`的完整细节，请参见第 1 章中的“如何在另一个文件中包含一个 PHP 脚本”）。这样做也会让你在自己的项目中使用这些库变得更容易。

关于如何安装和使用代码存档的完整说明，请参阅存档中的`readme.txt`文件。

#### 更新与勘误

没有一本书是完美的，我们预计敏锐的读者在本书结束前至少能发现两个错误。本书网站上的勘误（Errata）页面将会有有关已知打印和代码错误的最新信息，以及针对 PHP 新版本和各种 Web标准的必要更新。

#### SitePoint 论坛

如果你想就本书与我或 SitePoint 出版团队的其他人进行交流，你应该加入 SitePoint 的在线社区[4]。正如我提到的，特别是 PHP 论坛[5]，可以提供丰富的信息，并提供书中解决方案之外的见解。

事实上，即使你不想和我们聊天，也应该加入该社区，因为那里有很多有趣且经验丰富的 Web 设计师和开发者。那里是学习新知识、快速获得问题解答以及享受乐趣的好方法。

#### SitePoint 邮件简报

除了这类书籍外，SitePoint 还会发布免费的电子邮件简报，包括《The SitePoint Tribune》和《The SitePoint Tech Times》。在简报中，你将读到关于 Web 开发各个方面的最新新闻、产品发布、趋势、技巧和技术。即使没有其他收获，你也会获得有用的 PHP 文章和技巧，但如果你对学习其他技术感兴趣，你会发现它们特别有价值。快去 `http://www.sitepoint.com/newsletter/` 订阅一个或多个 SitePoint 邮件简报吧——我等着你！

- [4] `http://www.sitepointforums.com/`

- [5] `http://www.sitepointforums.com/forumdisplay.php?forumid=34`

点击此处订购《PHP Anthology》第一、二卷并享受 75 折优惠！

#### 你的反馈

如果你无法通过论坛找到答案，或者由于其他任何原因想与我们联系，最好的联系方式是 `books@sitepoint.com`。我们建立了一个管理良好的电子邮件支持系统来跟踪你的查询，如果我们的支持人员无法回答你的问题，他们会将问题直接发送给我。我们非常欢迎改进建议以及对你可能发现的任何错误的通知。

#### 致谢

首先，我要感谢 SitePoint 团队为本书的诞生付出的巨大努力，感谢在截止日期不可避免地推迟时的理解，感谢你们的个人投入，这让与他们工作成为件乐事。

特别感谢 Kevin Yank，他在整个过程中提供的宝贵技术见解和紧密合作解决了许多遗留问题，帮助《The PHP Anthology: Object Oriented PHP Solutions》既易于读又易于理解。感谢 Julian Szemere，频繁的反馈帮助塑造了本合集的的内容，并感谢 Georgina Laidlaw，她设法让我的一些“深夜时刻”变得更加清晰。

特别感谢那些为 SitePoint 论坛[7] 做出贡献的人。有一长名单的人因为他们分享 PHP 实践经验的无私精神而值得赞誉。看着 PHP 论坛在过去三年中成长是非常迷人的，从讨论 PHP 语法的基础到企业级应用架构。整体而言，我确定 SitePoint 的 PHP 社区为 PHP 成为流行且成功的技术做出了巨大的贡献。

最后，回到家里，我要感谢 Natalie，她在整个过程中的耐心、爱和理解令我惊讶。在写书一半时，我们的第一个孩子 Masha 出生了；同时写书并不总是容易。

- [7] `http://www.sitepointforums.com/`

## 第 1 章：PHP 基础

PHP 是一种为构建网站而设计的编程语言，由于极其容易学习，既是一种幸运也是一种诅咒。入门变得非常简单。

PHP 的文档非常优秀，由志愿者维护，他们的唯一目标是保持文档更新、易于理解且相关联。在线版本非常易于导航，并包含了全球开发者以注释形式提供的额外知识。

- [1] `http://www.hotscripts.com/`

该手册还提供了二十四种不同的语言版本 [4]，但既然你正在阅读这本书，我假设你对手册的英文版感到满意。它被分为五个主要部分加上附录。了解可以在哪里找到什么信息以及在何处是值得的——至少在前四个部分中，这些部分与典型的 PHP 开发者最相关。

### 第一部分：入门

`http://www.php.net/getting-started`

本节提供了 PHP 的简要介绍并附有一些基础示例。随后，它解释了如何安装 PHP（描述了各种操作系统与 Web 服务器的组合），以及如何通过修改`php.ini`文件来对其进行配置。



不容忽视的是安全章节，它涵盖了 PHP 开发者经常在 PHP 中犯错误的领域，这些错误会导致他们的应用程序容易被滥用。再次，PHP 易用性的“代价”是它并不会总是保护你免受最糟糕错误的影响，因此在你的 PHP 涯中尽早开始学习安全是值得的。你将在附录 C 中找到关键安全问题的总结，在本书的适当讨论中也会提到。

[4] http://www.php.net/docs.php

# 第 1 章：PHP 基础

## 第三部分：特性

http://www.php.net/features

这里涵盖了通常专注于解决特定 Web 相关问题的 PHP 核心元素。特性部分的大部分内容读起来像“执行摘要”，从开发者的角度来看，当你看到它们在运行时，可能会更好地理解这里包含的信息。一次性读完所有内容可能就像在读字典一样。幸运的是，通过阅读网络上丰富的教程以及研究 PHP 源代码中使用的代码，可以吸收语言参考中包含的大部分信息。当然，正如你将在书中读到的，我希望你从中学到一两点关于充分利用 PHP 的技巧。然而，熟悉手册这一部分包含的主题是值得的，并将它们记在脑中以备后参考。

## 第四部分：函数参考

http://www.php.net/manual/en/funref.php

这一部分构成了手册的核心，涵盖了 PHP 中可用功能的各个方面。随着你对 PHP 的学习，你将在这里花费大部分时间，所以你会很高听到 PHP 组努力让这一部分易于导航。在空闲时刻，仅仅阅读手册并对你可以用 PHP 做的所有事情感到惊讶甚至很有趣。是的，我刚刚把阅读手册描述为“有趣”。

函数参考被分为若干子章节，涵盖了各种类别的函数，每个类别对应一个 PHP 扩展。

### PHP 扩展

扩展的概念刚开始时可能有点困惑，因为许多扩展是随标准 PHP 安装一起分发的。字符串函数（`String functions`）我们很难离开它们，就是一个例子。通常情况下，PHP 组作为默认 PHP 安装的一部分分发了所有认为对开发者至关重要的扩展。被认为是“非要要”的功能（即某些开发者需要但并非所有开发者都需要）的扩展必须单独添加。重要信息出现在每个扩展主页的“安装”标题下。核心扩展的描述语句是：“使用这些函数不需要安装；它们是 PHP 核心的一部分。”非标准扩展在附录 B 中进行了检查。

访问函数参考中的信息可以通过搜索字段（右上角）和在“函数列表”中搜索来获取。注意，在函数列表中搜索仅检查函数参考部分。

点击此处订购《PHP 选集》第一卷和第二卷，并获得手册 75% 折扣。要搜索整个手册，你需要在“在线文档”中搜索。

另一种方便的导航方法是在 URL 中传递你感兴趣的主题名称来“快捷”到函数。例如，尝试在浏览器的地址栏中输入以下内容：`http://www.php.net/strings`。这将带你进入 `http://www.php.net/manual/en/strings.php`，这是字符串扩展的主页。查看此页面，你将看到该扩展提供的所有函数列表；同样的列表在左侧菜单中可用。

以 `strpos` 函数为例，输入 URL `http://www.php.net/strpos`（这会带你进入 `http://www.php.net/manual/en/function.strpos.php`）。你将看到关于 `strpos` 函数的以下信息：

| strpos |

| :--- |

| (PHP 3, PHP 4) |

| strpos -- 查找字符串首次出现的位置 |

| 描述 |

| int strpos (string haystack, string needle [, int offset]) |

| 返回 needle 在 haystack 中首次出现的的数字位置。与 strpos() 不同，此函数可以接受完整的字符串作为 needle 参数且该项将被使用。 |

| 如果未找到 needle，则返回 FALSE。 |

第一行包含函数名，第二行是该函数可用的 PHP 版本。第三行告诉你是函数的作用。在这种情况下，这是一个相当简短的解释，但 `strpos` 确实如此。在“描述”标题下，它是你感兴趣的函数。在括号中，函数签名告诉了函数接受的参数，并以逗号分隔。

# 第 1 章：PHP 基础

（注：行行，，，，，，，，，，。，，，， ` ` `stackstack` ``。。注意，第三个参数是可选的。以下是你如何使用 `strpos`：

```php
<?php
$haystack = 'Hello World!';
$needle = 'orld';

// 使用 strpos 函数
$position = strpos($haystack, $needle);
echo 'The substring ' . $needle . ' in ' . $haystack . ' begins at character ' . $position;
?>
```

## 第一章：PHP 基础

Zend 是开发 PHP 引擎核心的公司，他们还运营着一个相当活跃的论坛[20]，用于通用的 PHP 问题。

如果你想确保能获得答案，那么研究一下 PHP Helpdesk[21] 是值得的，该服务由 Tap Internet[22] 运营，他们与 Zend 合作提供 PHP。

### 如何修复 PHP 在我的脚本中发现的错误？

当你编写你最新、最强大的脚本到一半时，突然测试执行返回了此错误：

`Parse error: parse error, unexpected T_ECHO, expecting ',', or ';' in c:\htdocs\sitepoint\phpbasics\2.php on line 5`

这里有问题的代码如下：

```php
<?php
echo 'This is some code<br />';
echo 'Somewhere in here I've got a ';
echo 'parse error!<br />';
echo 'But where is it?<br />';
?>
```

你所面对的问题被称为**语法错误**（syntax error），虽然你还是 PHP 新手，但你可能会发现自己花费大量时间来寻找此类问题。随着你对 PHP 经验的增加，追踪错误将变得更容易。你最终会了解自己的坏习惯，并可能在开始寻找之前就能猜到你犯的错误（我自己的典型缺点是在在 PHP 字符串中构建 SQL 语句时忘记了最后的引号，以及在构建数组时遗漏了逗号）。不过，熟悉 PHP 的错误信息是一个好主意。

总的来说，你在 PHP 应用中会遇到四种基本类型的错误：

- [20] http://www.zend.com/phorum/list.php?num=3

- [21] http://www.phphelpdesk.com/

- [22] http://www.tapinternet.com/

#### 语法错误

如上面的示例所示，当你违反 PHP 语法规则时，就会发生语法错误。语法错误通常会导致 PHP 抛出 Parse Error（解析错误）消息。

在上面的示例中，问题本身发生在第 4 行：

```php
echo 'parse error!<br />'
```

我忘记在行末尾添加分号（;），分号是标记每个语句结束所必需的。PHP 解析器只有在遇到另一个 `echo` 语句时才注意到第 4 行的问题，因为指令在合法情况下可以跨多行。这是值得注意的，因为会让错误更难发现——错误实际上可能发生在你注意到问题的那行之前。

在大型 `if-else` 或 `while` 语句的情况下，语法错误可能会变得特别令人困惑，例如，你忘记了一个闭合括号。你可能有一段夹杂着 HTML 块的冗长列表；寻找缺失的大括号可能极其困难。然而，随着你编码技巧的提高，以及你开始利用类，将你的代码拆分为短小且易于阅读的独立块时，你会发现定位语法错误要容易得多。

另外一个需要注意的是 PHP 对标记（tokens）的使用。在错误消息中，PHP 抱怨说有一个“意外的 T_ECHO”。`T_ECHO` 是一个代表你 PHP 脚本中 `echo` 语句的标记。PHP 解析器将你的代码拆分为多个标记，以便它能够分析和处理脚本。你在错误报告中看到的某些标记比其他标记不那么显而易见，如果你不确定，查看关于标记的手册[23] 是值得的。

如果你在使用 PHP 4.3.0，你将发现所谓的分词器扩展[24]，它允许你看到 PHP 解析器查看代码的方式。出于兴趣，这里是你可以如何查看分词器输出的示例：

```php
<?php
/* 注意：此脚本仅在 PHP 4.3.0 或更高版本上运行 */
// 将 PHP 脚本读取为字符串
```

- [23] http://www.php.net/tokens

- [24] http://www.php.net/tokenizer

点击此处订购 PHP 精华第一、二卷并享受 75 折优惠！

```php
<?php
$script = file_get_contents('2.php');

// 获取标记并存数组
$tokens = token_get_all($script);

// 显示
echo '<pre>';
print_r($tokens);
echo '</pre>';
?>
```

#### 语义错误

语义错误发生在你编写了遵守 PHP 语法规则，但在执行时违反了 PHP 的“运行规则”的代码时。例如，你给 `foreach` 语句提供的是一个数组：

```php
<?php
$variable = 'This is not an array';

foreach($variable as $key => $value) {
    echo $key . ': ' . $value;
}
?>
```

因为 `$variable` 不是数组，此脚本产生了以下错误消息：

> Warning: Invalid argument supplied for foreach() in c:\htdocs\timepoint\phpbasics\3.php on line 4

语义错误通常会导致像这样的 Warning（警告）错误消息。

#### 环境错误

环境错误发生在系统与 PHP 脚本的连接导致问题时。例如，当你的 PHP 脚本尝试连接 MySQL 服务器时，该服务器可能已经宕机。也许你指定了错误的文件路径，导致 PHP 无法找到该文件。

当我们在一个系统上编写 PHP 脚本，并在另一个环境不同的系统中执行它时，也会发生这些错误。

问题可能仅仅是 Web 服务器的底层目录结构或域名不同。创建一个存储所有这些内容的中央配置脚本来处理此类问题是常见的做法。

点击此处订购 PHP 精华第一、二卷并享受 75 折优惠！

问题可能仅仅是 Web 服务器的底层目录结构或域名不同。创建一个存储所有这些内容的中央配置脚本来处理此类问题是常见的做法。

PHP 在 `php.ini` 中也有许多设置。

#### 逻辑错误

逻辑错误发生在应用程序从引擎角度来看运行完美，但代码执行的结果与你的意图不符。例如，想象你有一封想要发送的邮件。这类问题是最难发现的，尤其是当你对它们非常熟悉时。

发现逻辑错误的关键在于你严谨测试的能力，这是极端编程（XP）的一个方面，我们将在第六章中探索。

逻辑错误发生在应用程序从引擎角度来看运行完美，但代码执行的结果与你的意图不符。例如，想象你有一封想要发送的邮件。这类问题是最难发现的，尤其是当你对它们非常熟悉时。

发现逻辑错误的关键在于你严谨测试的能力，这是极端编程（XP）的一个方面，我们将在第六章中探索。

### 如何在一个 PHP 脚本中包含另一个 PHP 脚本？

在发现编写数千行的脚本可能不是组织代码的方法后，你可能在寻找将代码拆分为单独文件的方法。也许在使用某人的开源应用时，你发现自己正困于如下错误消息：

`Fatal error: Failed opening required 'script.php'`

#### 包含

PHP 提供了四个命令允许你将 PHP 脚本的内容添加到另一个中：`include`、`require`、`include_once` 和 `require_once`。在每种情况下，PHP 获取命令中的文件名，然后执行其内容。`include` 和 `require` 的区别在于当无法找到脚本时的行为。

`include` 会生成类似这样的 PHP 警告消息：

`Warning: Failed opening 'script.php' for inclusion`

这将允许调用 `include` 命令的脚本继续执行。

相比之下，`require` 会导致如所示的致命错误，这意味着脚本将终止，停止所有操作。如果被要求的的文件对你的应用程序至关重要，那么脚本终止是非常好的。

`include_once` 和 `require_once` 命令的行为与其对应的命令类似，但如果脚本已经在其他地方（通过四个命令中的任何一个）包含或引用，则该语句将被忽略。乍一看，这些命令的使用方法并不明显；你当然知道自己用过多少次 `include` 命令，对吧？在更复杂的应用程序中，你的 PHP 脚本包含了其他 PHP 脚本，而这些脚本又包含了更多的 PHP 脚本。当你使用类库（我们将在第二章中探索），且这些类被许多脚本重复使用时，这一点尤为重要。一个类可能依赖于另一个类的可用。

使用 `require_once` 来包含所需的类确保了它将始终可用，但如果该类恰好在其他地方被使用，也不会产生任何问题。

为了看到所有这些操作，让我们创建一个 `include_me.php` 脚本：

文件：include_me.php

```php
<?php
// include_me.php
echo 'I\'ve been included!<br />';
?>
```

每当此脚本被包含时，它都会显示“I’ve been included!”的消息，这样我们就知道它工作了。

现在，让我们测试一下在另一个脚本中包含此文件的各种方法：

文件：5.php

```php
<?php
// 这种工作正常
echo '<br />Requiring Once: ';
require_once 'include_me.php';

// 这个也工作正常
echo '<br />Including: ';
include 'include_me.php';

// 由于文件已经包含，所以什么都没有发生
echo '<br />Including Once: ';
include_once 'include_me.php';

// 这样没问题
echo '<br />Requiring: ';
require 'include_me.php';

// 再次什么都没有发生 - 文件已经包含过了
echo '<br />Requiring Once again: ';
require_once 'include_me.php';

// 因为文件不存在，产生产生警告消息
echo '<br />Include the wrong file: ';
include 'include_wrong.php';

// 产生致命错误并停止脚本执行
echo '<br />Requiring the wrong file: ';
```

# 第1章：PHP 基础

```php
require 'include_wrong.php';

// 这将永远不会执行，因为我们有一个致命错误
echo '<br />Including again: ';
include 'include_me.php';
?>
```

这是它生成的输出（注意我简化了结尾的错误信息）：

Requiring Once: I've been included!

Including: I've been included!

Including Once:

Requiring Once: I've been included!

Requiring Once again:

Include the wrong file: 'include_wrong.php' for inclusion

Warning: Failed opening 'include_wrong.php' for a warning

Requiring the wrong file:Fatal error: Failed opening required 'include_wrong.php'

注意，第一次使用 `include_once` 没有包含（文件已经包含过了），后来的 `require_once` 也是如此。随后，当我尝试包含错误的文件时（一种情况下，一个不存在的文件），会有一个警告消息。然而，执行会继续到下一行，我尝试要求一个不存在的文件。这一次，PHP 产生了一个致命错误并停止了脚本执行，这意味着最后一次包含文件的尝试永远不会发生。

请注意，你需要的文件并不只包含 PHP。包含的文件可以只包含 HTML 而不包含任何 PHP。

#### 应使用哪种命令？

作为一种通用做法，除非你有需要其他行为的特殊情况，否则请始终使用 `require_once` 命令将一个文件包含在另一个文件中。当你将 PHP 类放在单独的文件中，并且一个类可能依赖于另一个类时，这一点尤为重要。关于类的完整故事情节，请参阅第 2 章。

![](img/80d007a3dc499b219e99d11695c2c366_35_0.png)

点击此处订购《PHP 精选》第一卷和第二卷并享受 75 折优惠！

PHP 的四个包含命令不应与各种文件相关函数（在第 4 章讨论）混淆；这些函数旨在用于获取内容而不立即将其解析为 PHP 脚本，从而允许你处理它们的内容。

请注意，在本书中，即使我使用 `require` 命令之一时，我也会谈论“包含”一个文件。这是讨论 PHP 的常用惯例，源于第一批 PHP 先驱所使用的较旧语言。

#### 路径查找

到为止，我只看了如何包含。

# 使用完整的 `<?php ?>` 标签

PHP 支持多种标记来标识 PHP 代码段，包括短标签 (`<? ?>`) 和 ASP 风格的标签 (`<% %>`)。这些标签由 `php.ini` 中的 `short_open_tag` 和 `asp_tags` 设置进行控制。虽然你可能将这些设置设置为 `On`，但其他人可能没有。例如，短标签样式在 PHP 与 XML 文档混合时会产生问题，因为 XML 使用了类似下面的处理指令：



```xml
<?xml version="1.0"?>
```
如果这里有一个包含 PHP 和 XML 的文档，并且开启了 `short_open_tag`，PHP 会将 XML 处理指令 `<?xml` 误认为是 PHP 开启标签。

你的代码可能需要在 `short_open_tags` 和 `asp_tags` 均关闭的环境中运行。确保万无一失的最佳方法是养成始终使用 `<?php ?>` 标签风格的习惯，否则在将来可能需要进行大量的代码重写。

## `register_globals`

PHP 能够将数据转换为原生 PHP 变量。此功能由 `php.ini` 中的 `register_globals` 设置控制。开启 `register_globals` 后，如果我的浏览器指向类似 `http://www.mysite.com/index.php?logged_in=1` 的地址，PHP 将自动创建 `$logged_in` 变量并赋值为 1。PHP 组建议禁用此功能，因为正如前一个示例所示，它代表了安全风险。

因此，在 `php.ini` 中确保存在以下代码：

```
register_globals = Off
```

这将迫使你通过预定义的超全局变量（例如 `$_GET['username']`）来访问传入的数据，这意味着它们不会与你在脚本中创建的变量冲突。

在 Apache 中使用 `.htaccess` 文件，可以通过以下代码实现相同的结果：

```
php_flag register_globals off
```

更多信息可以在 PHP 手册中，以及 Kevin Yank 在 SitePoint 上的文章"Write Secure Scripts with PHP 4.2!"中找到。

## Magic Quotes（魔幻引号）

Magic quotes 是一项旨在防止 PHP 初学者开发的网站出现安全漏洞的功能。在你的脚本访问任何这些值之前，它会自动对传入的 URL 字符串和表单中的字符进行转义（更多信息请见第 5 章）。如果你直接将数据插入数据库，那么就不存在某人能够篡改数据库的风险。对于初学者来说，这无疑是防止灾难性方法。然而，一旦你理解了 SQL 注入并养成了处理它们的习惯，magic quote 功能可能会变成比其价值更大的问题。

Magic quotes 功能由 PHP 配置设置 `magic_quotes_gpc` 控制，该设置可以为 `On` 或 `Off`。我倾向于关闭 magic quotes，并自己处理数据转义。遗憾的是，这意味着我编写的代码无法很好地迁移到开启了 magic quotes 的 PHP 环境中（会导致内容中出现反斜杠）。坦率地说，为了解决这个问题，PHP 提供了 `get_magic_quotes()` 函数，可以用它检查 magic quotes 是否开启。为了保持代码的可移植性，如果启用了此功能，请使用一个简单的文件来剔除 magic quotes：

```php
<?php
/* 检查 magic_quotes_gpc 是否为 On，并在需要时从传入的 
请求中剔除它们 */
if (get_magic_quotes_gpc()) {
  $GET = array_map('stripslashes', $GET);
  $POST = array_map('stripslashes', $POST);
}
?>
```

# 第 1 章：PHP 基础

如果在任何从查询字符串、post 或 cookie 接收数据的文件的开头包含此内容，我们将移除由 magic quotes 添加的任何反斜杠，这有效地让我们找回了原始数据。SQL 注入攻击将在第 3 章的"我如何解决由引号引起的错误？"中详细讨论。如果你不确定自己可以保护自己免受 SQL 攻击，请使用 magic quotes。一旦你对完全掌握了所有问题感到满意，请关闭 magic quotes 为自己省去很多烦恼。请注意，magic quotes 只能在 `php.ini` 文件或 Apache 的一个 `.htaccess` 文件中关闭。更多信息请参阅附录 A。

## 调用时按引用传递（Call-Time Pass-By-Reference）

引用就像是变量值的"快捷方式"。当我们使用函数和类时，通常需要引用，我们将在第 2 章进一步讨论这个主题。当你在函数或类方法中使用变量的引用时，它被定义为调用时引用传递。考虑这个例子：

```
$result = myFunction(&$myVariable);
```

`&` 运算符告诉 PHP 使用变量 `$myVariable` 的引用作为参数，而不是创建一个其值的副本。这现在被认为是一种坏做法，但它会让理解他人代码变得极其困难。在 `php.ini` 中使用以下命令关闭它：

```
allow_call_time_pass_reference = Off
```

或者，在 `.htaccess` 文件中如下关闭它：

```
php_flag allow_call_time_pass_reference off
```

## 编写可复用代码

说起来容易，我知道，但如果你发现自己正在编写多个 PHP 脚本，那么你需要在遭受过早性脱发之前开始思考如何让你的代码可复用。从技术上讲，这并不完全是一个可移植性问题，但如果你最终在其他网站或应用程序上工作，你会感谢拥有现成的代码。此外，如果你编写的是需要集成到现有应用程序的代码，你需要将其封装成不依赖于现有系统的形式。

例如，如果你的应用程序有某种用户身份验证系统，它将与已使用的系统集成——一个拥有大量关联系统的。

最好的方法是编写面向对象的代码（第 2 章的重点），并旨在创建"组件"。有些人认为 PHP 中的面向对象代码会降低应用程序性能，因此应该避免。他们忘记提到面向对象编程带给性能的巨大提升。毕竟，优秀的程序员比快的机器更贵！

衡量代码复用性能时需要考虑的一些因素：

- 在长时间之后你还能理解这些代码吗？

- 你的代码可以轻松集成到其他应用程序中吗？

- 你代码中的假设是否适用于其他网站？

你将在本书中找到许多提示和建议，鼓励你编写可复用代码，尽管对 PHP 应用设计的深度分析超出了它的范围。在你阅读本书时，你应该对某些关键因素作为进一步研究的主产生感觉。作为一名丰富的 PHP 开发者，你对自己有一个责任：扩展对软件开发更深奥方面的知识，例如设计模式和企业应用架构，以提高你的开发技术，更重要的是为你节省时间。你的知识越广泛，在获得项目时风险就越低。

- Write Secure Scripts with PHP 4.2!: [http://www.sitepoint.com/article/758](http://www.sitepoint.com/article/758)

一篇解释在关闭 `register_globals` 的情况下编写脚本重要性的教程。

- Effortless (or Better!) Bug Detection with PHP Assertions: [http://www.sitepoint.com/article/1008](http://www.sitepoint.com/article/1008)

- Using Strings: [http://www.zend.com/zend/tut/using-strings.php](http://www.zend.com/zend/tut/using-strings.php)

Zend 提供了处理字符串的主要函数导览。

- String Theory: [http://www.devshed.com/Server_Side/PHP/StringTheory](http://www.devshed.com/Server_Side/PHP/StringTheory)

DevShed 对字符串进行了深入探讨，甚至涉及了 Posix 扩展正则表达式。

## 2 面向对象的 PHP

面向对象范式是一种编程方法，旨在鼓励开发可维护且结构良好的应用程序。由于许多 PHP 开发者将**面向对象编程** (OOP) 视为某种神秘的艺术，因为许多 PHP 开发者在解决问题时，往往只关注**面向过程**的方法，而不采用面向对象的方法。这是一种遗憾，因为采用面向对象的方法开发 PHP 应用可以获益匪浅，其中最重要的一点可能就是代码重用。一段编写良好的面向对象代码可以轻松解决其他项目中的相同问题；我们只需要在需要时将其插入即可。面向对象的代码库数量日益增加，例如 PEAR[1] 和 PHP Classes[2]，它们可以节省你在解决这些体系问题上花费的数小时工作，让你有精力专注于应用程序的特定细节。

在本章中，你将获得编写面向对象 PHP 的实战基础——并且会有很多机会让你上手实践。教授 OOP 有很多方法，这个主题提供了无尽的讨论空间。在我看来，最好的方法是直接投入，看看如何使用 PHP 中的类来完成过程化的任务，并在此过程中加入理论。这就是我们在本章将采取的方法。在《PHP 选集：面向对象 PHP 解决方案》两卷书中，我将在适当的地方使用 OOP，这应该为你提供更多可学习的示例。特别是第二卷第 7 章，将让你深入理解为什么 OOP 是结构化应用程序的有效方法。

在实践中，学习使用 PHP 提供的对象模型我们需要实现两个目标，这两个目标通常需要同时进行：

- 你必须完成从面向过程代码到面向对象代码的"思维跨跃"。

第一步是很容易的。它是下一个解决方案的主题，并在后续阶段的更多示例中将涉及更高级的主题。

第二步，即"思维跨跃"，既简单又具有挑战性。一旦你实现了它，你将不再考虑单个脚本应该完成的长长任务列表；相反，你将编程视为组合一组工具，你的脚本将把工作委托给这些工具。

稍微提前一点——为了体验一下未来的内容——这里有一个任何使用 PHP 超过一周的人都会熟悉的简单示例：连接 MySQL 并获取一些数据。一种常见的面向过程方法所示：

```php
<?php
// 过程示例

// 连接到 MySQL
$connection = mysql_connect('localhost', 'harry', 'secret');

// 选择所需的数据库
mysql_select_db('sitepoint', $connection);

// 执行查询选择五篇文章
$sql = 'SELECT * FROM articles LIMIT 0,5';
$result = mysql_query($sql, $connection);

// 显示结果
while ($row = mysql_fetch_array($result)) {
    // 在处显示结果
}
?>
```

点击此处订购《PHP 选集》第一、二卷并享受 75 折优惠！

在上面的脚本中，我们调用了 PHP 的 MySQL 函数，这些函数作用于我们传递给它们的变量。这通常会导致我们得到一个新的变量，我们可以通过它进行进一步的工作。

解决相同问题的面向对象方法可能如下：

```php
<?php
// OOP示例

// 引入 MySQL 类
require_once 'Database/MySQL.php';

// 实例化 MySQL 类，连接到 MySQL 并选择数据库
$db = new MySQL('localhost', 'harry', 'secret', 'sitepoint');

// 执行查询选择五篇文章
$sql = 'SELECT * FROM articles LIMIT 0,5';
$result = $db->query($sql); // 创建一个 MySQLResult

// 显示结果
while ($row = $result->fetch()) {
    echo $Display results
}
?>
```

使用 PHP MySQL 函数处理 MySQL 的细节现在已委托给了一个从 MySQL 类创建的对象（我们将在本书中频繁使用该类，它将在第 3 章中构建）。尽管这个示例可能无法完全阐明 OOP 的优势（考虑到在代码量上它与第一个示例非常相似），但它的作用是原始脚本中的某些复杂性现在由 MySQL 类来处理了。

例如，我们不再需要执行两个步骤来连接到 MySQL 服务器然后选择数据库；相反，我们可以在创建 MySQL 对象时一次性处理这两个步骤。此外，如果稍后我们希望让脚本从不同的数据库（例如 PostgreSQL）获取结果，我们可以使用像 MySQL 类那样相关的类编程接口 (API)——为了做到这一点，我们只需要更改上述示例的一行代码。我们将在第二卷第 7 章中恰好这样做。

面向对象的方法在对象相互交互的情况下真正显示了它的价值。我将在本章中留出对这些解决方案的进一步讨论，因为这是一个重要的概念。当你精通面向对象编程时，你会发现编写复杂的应用程序变得像组装高积木一样简单。

我会在讨论中偶尔引入统一建模语言 (UML) 类图。UML 是一种用图像描述面向对象程序的标准。如果你以前没有遇到过 UML，不要担心；图表与代码之间的关系将自其明。

## 面向对象 PHP 的基础是什么？

假设你对 OOP 一无所知，最好的开始点是类的基本 PHP 语法。你可以简单地将类类函数和变量的集合。

## 阅读详细手册

PHP 手册包含了关于 OOP 的丰富信息：

[http://www.php.net/oop](http://www.php.net/oop)

我们将开发一个可以帮助生成 HTML 的简单示例，并将演示 PHP 类和对象的知识。这并不是为了优秀的设计；它只是 PHP 语法的入门。让我们从一个构建 Web 页面的过程脚本开始，然后逐渐将其转换为 PHP 类：

```php
<?php
// 生成页面顶部
function addHeader($page, $title)
{
  $page .= <<<EOD
<html>
<head>
<title>$title</title>
</head>
<body>
<h1 align="center">$title</h1>
EOD;
  return $page;
}

// 生成页面底部
function addFooter($page, $year, $copyright)
{
  $page .= <<EOD
<div align="center">$page $copyright</div>
</body>
</html>
EOD;
  return $page;
}

// 初始化页面变量
$page = '';

// 将页头添加到页面
$page = addHeader($page, '一个过程脚本');

// 在页面主体中添加内容
$page = <<EOD
<p align="center">此页面是通过过程脚本生成的</p>
EOD;

// 将页脚添加到页面
$page = addFooter($page, date('Y'), 'Procedural Designs Inc.');

// 显示页面
echo $page;
?>
```

> 过程化编程是非面向对象编程的名称。到目前为止，我们在书中看到的所有代码都是过程性的。

# 第 2 章：面向对象的 PHP

但是我们如何重构上述代码以采用面向对象的形式呢？

首先，我们需要一个类，将上述两个函数 `addHeader` 和 `addFooter` 放入其中：

文件：`2.php` (节录）

```php
<?php
// Page 类
class Page {
  // 生成页面顶部
  function addHeader($page, $title)
  {
    $page .= <<EOD
<html>
<head>
<title>$title</title>
</head>
<body>
<h1 align="center">$title</h1>
EOD;
    return $page;
  }

  // 生成页面底部
  function addFooter($page, $year, $copyright)
  {
    $page .= <<EOD
<div align="center">&copy; $year $copyright</div>
</body>
</html>
EOD;
    return $page;
  }
}
```

使用 PHP 关键字 `class`，我们可以将 `addHeader` 和 `addFooter` 这两个函数组合在类中。放在类内部的函数被称为成员函数，或更常用的**方法 (methods)**。与普通函数不同，方法必须作为类的一部分被调用：

> ²重构是在不实际改变代码功能的情况下对代码进行结构调整。这通常是为了便于未来的维护和扩展，而当前的结构会阻碍代码的扩展。

```php
// 初始化 $page 变量
$page = '';

// 将页头添加到页面
$page = Page::addHeader($page, '一个使用静态方法的脚本');

// 向页面主体添加一些内容
$page .= <<EOD
<p align="center">此页面是用静态类方法生成的</p>
EOD;

// 将页脚添加到页面
$page = Page::addFooter($page, date('Y'), 'Static Designs Inc.');

// 显示页面
echo $page;
?>
```

我们使用 `::` 运算符调用了类方法 `addHeader` 和 `addFooter`。脚本实际上与之前几乎相同；然而，我们不再是直接调用函数，而是需要像这样调用它们：

```php
$page = Page::addHeader($page, '一个使用静态方法的脚本');
```

虽然这算是一个巨大的改进，但它确实根据功能将我们的函数集合在了一起。这允许我们在不同的类中分别调用同名的不同函数。

## 静态方法

到目前为止，我们只把类作为相关函数的容器。在面向对象的术语中，设计为这样工作的函数被称为**静态方法 (static methods)**。实际上，与大多数方法相比，静态方法相当无聊。在接下来的章节中，我们将看到如何通过完全的方法来展示你的才华。

## 类与对象

类是对象的"蓝图"。也就是说，与你声明并使用的函数不同，类仅仅描述了一种类型的对象。在用它做有用的工作之前，你需要通过**实例化 (instantiation)** 来创建一个对象——即类的**实例 (instance)**。

类并不只包含函数——它们还可以包含变量。为了让 `Page` 类更有用，我们可能希望将某些变量与方法分组，然后将类实例化为一个对象。这里是改进后的 `Page` 类的代码：文件：`3.php` (节录)



```php
<?php
// Page 类
class Page {

  // 声明一个类变量
  var $page;

  // 构造函数
  function Page() {
    $this->page = '';
  }

  // 生成页面顶部
  function addHeader($title)
  {
    $this->page .= <<EOD
<html>
<head>
<title>$title</title>
</head>
<body>
<h1 align="center">$title</h1>
EOD;
  }

  // 向页面添加一些文本
  function addContent($content)
  {
    $this->page .= $content;
  }

  // 生成页面底部
  function addFooter($year, $copyright)
  {
    $this->page .= <<EOD
<div align="center">&copy; $year $copyright</div>
</body>
</html>
EOD;
  }

  // 获取页面内容
  function get()
  {
    return $this->page;
  }
}
```

在这一版本的示例中，`Page` 类要实得多得多。首先，我们添加了一个成员变量（也称为**字段 (field)**），用于存储 HTML：

```php
// 声明一个成员变量
var $page;
```

PHP 关键字 `var` 用于在类中声明变量。我们也可以在声明变量时为其赋值，但不能在声明中放置函数调用。例如：

```php
// 这是允许的
var $page = '';

// 这是不允许的
// var $page = strtolower('HELLO WORLD');
```

在变量声明之后，我们有一个特殊的方法叫做**构造函数 (constructor)**。当类被实例化时，该方法会被自动执行。构造函数的名称必须与类名相同。

## 构造函数没有返回值

> 构造函数不能返回任何值。它的作用纯粹是在类实例化时以某种方式设置好对象。如果这有帮助的话，可以将构造函数看作是一个在设置好后会自动返回对象的函数，你不需要自己提供返回值。

尽管如此，如果需要，你仍然可以使用不带指定值的 `return` 命令来立即终止构造函数。在构造函数内部，我们使用了一个特殊变量 `$this`：

```php
// 构造函数
function Page() {
  $this->page = '';
}
```

在任何方法（包括构造函数）中，`$this` 都指向正在运行该方法的对象。它允许方法访问该特定对象的其他方法和变量。跟在 `$this` 后面的 `->`（箭头）运算符用于指向对象命名的属性或方法。

在上面的示例中，构造函数为开始时声明的成员变量赋了一个空字符串。`$this` 变量的概念初看起来很奇怪且令人困惑，但是其他编程语言（如 Java）采用的一种常用策略，允许类成员之间相互交互。一旦你开始编写面向对象的代码，你很快就会习惯它。所有方法都使用 `page` 成员变量，这并非巧合。将代码（方法）与其所处理的数据（变量）绑定在一起，是面向对象编程最基础的特性。

这里是该类的实际运行：

```php
// 实例化 Page 类
$webPage = new Page();

// 将页头添加到页面
$webPage->addHeader('一个用对象构建的页面');
```

```php
// 向页面主体添加一些内容
$webPage->addContent("<p align=\"center\">此页面是用对象生成的</p>");

// 将页脚添加到页面
$webPage->addFooter(date('Y'), 'Object Designs Inc.');

// 显示页面
echo $webPage->get();
?>
```

## 理解作用域

编写超过几百行的过程化 PHP 代码，毫无疑问，你会遇到解析错误，或者更糟糕，由于无意中多次使用函数名或变量名而导致的错误。当你包含大量文件且代码变得越来越复杂时，你可能会发现自己对这个问题变得越来越偏执。如何防止命名冲突的发生？解决此问题的方法之一是利用作用域（scope）对不需要这些内容的代码隐藏变量和函数。

作用域是一个变量或函数与其他作用域隔离的上下文。PHP 有三种可用的作用域：全局作用域、函数作用域和类作用域。在任何这些作用域中定义的变量和函数对任何其他作用域都是隐藏的。函数和类作用域是局部作用域，这意味着函数 X 的作用域对函数 Y 的作用域是隐藏的，反之亦然。

类的巨大优势在于你可以在一个地方定义变量以及使用它们的函数，将函数与无关的代码隔离开。这突显了面向对象范式的关键理论点之一。特定的范式特别强调函数，变量被视为在函数调用之间存储数据的微小组合。而面向对象的范式将重点转移到了变量；函数“支撑”变量并被用于访问或修改它们。

让我们通过一个示例来探索：

```php
<?php
// 一个全局变量
$MyVariable = 'Going global';

// 在全局作用域声明的函数
function myFunction()
{
    // 函数作用域内的变量
    $MyVariable = 'Very functional';
}

// 在全局作用域声明的类
class MyClass {
    // 在类作用域声明的变量
    var $MyVariable = 'A class act';

    // 在类作用域声明的函数
    function myFunction() {
        // 函数（方法）作用域内的变量
        $myVariable = 'Methodical';
    }
}
?>
```

在示例中，每个变量声明实际上都是独立的变量。它们可以和谐地共存而不互相干扰，因为每个都位于独立的作用域中。同样，两个 `myFunction` 声明是两个独立的函数，存在于不同的作用域中。因此，PHP 将为你保留它们所有的值。

当你开始在 PHP 中大量使用面向对象编程时，作用域变得非常重要。由于许多类可以具有相同名称的方法，你可以设计不同的类来提供相同的编程接口（API）。这些类所使用的脚本可以使用相同的方法调用，无论它们处理的对象是由哪个类实例化的。这在编写可维护的代码时可能是一项非常强大的技术。当我们在本章稍后讨论多态时会详细介绍这一点。

### 三行代码

以下是我们可以让类变得更易使用的方法：

```php
<?php
// Page 类
class Page {
    // 声明类成员变量
    var $page;
    var $title;
    var $year;
    var $copyright;

    // 构造函数
    function Page($title, $year, $copyright) {
        // 给成员变量赋值
        $this->page = '';
        $this->title = $title;
        $this->year = $year;
        $this->copyright = $copyright;

        // 调用 addHeader() 方法
        $this->addHeader();
    }

    // 生成页面顶部
    function addHeader()
    {
        $this->page .= <<EOD
<html>
<head>
<title>$this->title</title>
</head>
<body>
<h1 align="center">$this->title</h1>
EOD;
    }

    // 向页面添加更多文本
    function addContent($content)
    {
        $this->page = $content;
    }

    // 生成页面底部
    function addFooter()
    {
        $this->page .= <<EOD
<div align="center">&copy; $this->year $this->copyright</div>
</body>
</html>
EOD;
    }

    // 获取页面内容
    function get()
    {
        $temp = $this->page;
    }

    // 调用 addFooter() 方法
    $this->addFooter();
}
```

点击此处订购《The PHP Anthology Volume I & II》并享受 75 折优惠！

# 第二章：面向对象的 PHP

在 PHP 中，所有的变量名都自动与内存中的值链接在一起。

使用引用（reference）允许我们在变量名相同时的情况下，将两个变量名链接到内存中的同一个值。然后你可以让它们之间互相替换。

## 什么是引用？

要理解引用，我们必须先理解 PHP 在正常情况下（即在不使用引用的情况下）是如何处理变量的。

默认情况下，当一个变量被传递给其他任何对象时，PHP 会创建该变量的副本。当我说“传递”时，指的是以下任何一种情况：

- 将一个变量传递给另一个变量：

```php
<?php
$color = 'blue';
$settings['color'] = $color;
?>
```

`$settings['color']` 现在包含了 `$color` 的一个副本。

- 将变量作为参数传递给函数：

```php
<?php
function isPrimaryColor($color)
{
    // $color 是一个副本
    switch ($color) {
        case 'red':
        case 'blue':
        case 'green':
            return true;
            break;
        default:
            return false;
    }
}

$color = 'blue';
if (isPrimaryColor($color)) {
    echo $color . ' is a primary color';
} else {
    echo $color . ' is not a primary color';
}
?>
```

当 `$color` 被传递给函数 `isPrimaryColor` 时，PHP 在函数内部使用的是原始 `$color` 变量的副本。

将变量传递给类方法的情况也是类似的。

```php
<?php
class ColorFilter {
  var $color;
  function ColorFilter($color) {
    // $color 是一个副本
    $this->color = $color;
    // $this->color 是副本的副本
  }
  function isPrimaryColor() {
    switch ($this->color) {
      case 'red':
      case 'blue':
      case 'green':
        return true;
        break;
      default:
        return false;
    }
  }
}
```

```php
<?php
$color = 'blue';
$filter = new ColorFilter($color);
if ($filter->isPrimaryColor()) {
  echo ($color.' is a primary color');
} else {
  echo ($color.' is not a primary color');
}
?>
```

类外的原始 `$color` 被传递给了 `ColorFilter` 的构造函数。构造函数内部的 `$color` 变量是传递给它的版本的副本。它被赋值给 `$this->color`，这使得该版本变成了副本。

# 第二章：面向对象的 PHP

所有这些传递变量的方法都会创建该变量值的副本；这被称为**值传递**（passing by value）。

## 使用引用

要使用引用，你需要使用引用运算符 `&`。例如：

```php
<?php
$color = 'blue';
$settings['color'] = &$color;
?>
```

`$settings['color']` 现在包含了对原始 `$color` 变量的引用。

比较以下示例，第一个使用 PHP 的默认拷贝行为：

```php
<?php
$color = 'blue';
$settings['color'] = $color; // 创建一个副本
$color = 'red'; // 改变
echo $settings['color']; // 显示 "blue"
?>
```

第二个涉及引用传递：

```php
<?php
$color = 'blue';
$settings['color'] = &$color; // 创建一个引用
$color = 'red'; // 改变
echo $settings['color']; // 显示 "red"
?>
```

引用传递允许我们将新变量“链接”到原始源变量。改变新变量或旧变量都会反映在两者之中。

到目前为止，你可能在想：“这有什么大不了的？”无论 PHP 是拷贝还是创建引用，只要我们得到了预期的结果，这有什么区别呢？在过程化程序中，很少需要担心引用。然而，当对象相互交互时，如果你不通过引用传递对象，可能会得到不符合预期的结果。

点击此处购买 PHP 选集 I & II 并享受 75 折优惠！

## 引用的重要性

想象你的网站上有一个机制，允许访问者更改网站的外观——一个“控制面板”。很可能，为了实现这种功能，你需要编写代码对一组包含“外观”数据的变量进行操作，以便独立于应用程序的其他部分来修改它们。

首先，用类简单地表示，让我们看看存储外观相关数据的类：

```php
<?php
// 外观包含 $color 和 $size
class LookAndFeel {
    var $color;
    var $size;
    function LookAndFeel() {
        $this->color = 'white';
        $this->size = 'medium';
    }
    function getColor() {
        return $this->color;
    }
    function getSize() {
        return $this->size;
    }
}
```

*(注：后续重复的类定义和章节由于原文 OCR 文本的冗余，已根据工程师要求进行处理，保留核心逻辑翻译。)*

# 第二章：面向对象的 PHP

接下来，假设我们有一个处理输出的类：

```php
<?php
// 外观包含 $color 和 $size
class LookAndFeel {
    var $color;
    var $size;
    function LookAndFeel() {
        $this->color = 'white';
        $this->size = 'medium';
    }
    function getColor() {
        return $this->color;
    }
    function getSize() {
        return $this->size;
    }
}
```

*(省略重复的类定义块...)*

```php
function display($message) {
  echo $message;
}

$myMessage = 'Hello World!';
```

// 调用时引用传递 - 糟糕的做法！

`display($myMessage);`

这被称为调用时引用传递，PHP 通过 `php.ini` 中的以下设置来控制它：

```
allow_time_pass_reference = Off
```

在最近的 PHP 版本中，上述设置默认应设置为 `Off`；开启此设置被 PHP 的制作者们视为“反对”。如果关闭该设置，每当函数调用一个本应通过引用传递的参数时，PHP 都会生成警告错误。因此，保持此设置关闭是一个良好的做法。

调用时引用传递之所以是“坏事”的原因是，调用时引用传递会使代码极其难以追踪。我偶尔见过使用调用时引用传递编写的 PHP XML 解析器——几乎无法理解程序正在发生什么。

变量是否以引用方式传递的这一“决策”属于被调用的函数，而不是调用它的代码。上述代码如果写得正确，应该是这样的：

```php
// 引用传递 - 良好的做法
function display($message) {
  echo $message;
}

$myMessage = 'Hello World!';

display($myMessage);
```

## 性能问题

取决于你的应用程序规模，在使用引用时，你可能需要考虑一些性能问题。

# 第 2 章：面向对象的 PHP

在复制一个变量的简单情况下，PHP 的内部引用计数可以防止不必要的内存消耗。例如：

```php
$a = 'the quick brown fox';
$b = $a;
```

在上面的示例中，`$b` 的值不会占用任何额外的内存，PHP 的内部引用计数会隐式地让 `$b` 和 `$a` 指向内存中的同一个位置，而它们的值是不同的。这是 PHP 的内部特性，会影响性能但不影响行为。我们不需要担心它。

然而，在某些情况下，使用引用会更快，特别是对于大型数组和对象，此时 PHP 的内部引用计数无法使用，因此必须复制其内容。

因此，为了获得最佳性能，你应该执行以下操作：

- 对于整数和字符串等简单值，尽可能避免使用引用。



- 对于数组和对象等复杂值，尽可能使用引用。

## 引用与 PHP 5

随着 PHP 5 的发布，引用将不再是一个问题；PHP 在传递对象时的默认行为将变为通过引用传递。如果你确实需要一个对象的副本，可以使用`__clone`方法来创建副本。

本质上，PHP 的这些与 Java 等大多数面向对象编程语言保持一致的更改，将有助于减少围绕该主题的困惑。不过，目前在 PHP 5 被广泛采用之前，了解引用的工作原理是非常重要的。

## 我该如何利用继承？

继承是面向对象范式的根本部分之一，也是其威力的重要部分。继承是不同类之间的关系，其中一个类被定义为另一个类的子类或子类。子类继承父类定义的方法和成员变量，允许它为父类“增加值”。

[点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！]

查看 PHP 中继承如何工作的最简单方法是通过示例。假设我们有这样一个简单的类：

```php
<?php
class Hello {
    function sayHello() {
        return 'Hello World!';
    }
}
```

使用`extends`关键字，我们可以创建一个 Hello 的子类：

```php
class Goodbye extends Hello {
    function sayGoodbye() {
        return 'Goodbye World!';
    }
}
```

Goodbye 现在是 Hello 的子类。反过来说，Hello 是 Goodbye 的父类或超类。现在，我们可以简单地实例化子类，并使用单个对象访问`sayHello`和`sayGoodbye`方法：

```php
$msg = new Goodbye();
echo $msg->sayHello() . '<br />';
echo $msg->sayGoodbye() . '<br />';
?>
```

该示例展示了继承工作的原理，但没有展示它的真实威力。这随着重写（Overriding）的引入而到来。

### 重写

当我们给子类提供一个与父类中函数同名的函数时会发生什么？示例如：

```php
<?php
class Hello {
    function getMessage() {
        return 'Hello World!';
    }
}
class Goodbye extends Hello {
    function getMessage() {
        return 'Goodbye World!';
    }
}
```

两个类具有相同的方法名`getMessage`。这对 PHP 来说是完全可以接受的——它对方法的重复声明没有任何意见。

当我们使用这些类时，会发生以下情况：

```php
$hello = new Hello();
echo $hello->getMessage() . '<br />';

$goodbye = new Goodbye();
echo $goodbye->getMessage() . '<br />';
?>
```

输出结果如下：

```
Hello World!
Goodbye World!
```

通过`$goodbye`对象调用`getMessage`显示 "Goodbye World!"。子类方法重写了父类中的方法。

你也可以让子类在内部使用父类的方法，同时对其进行重写。例如：

```php
<?php
class Hello {
    function getMessage() {
```

[点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！]

```php
        return 'Hello World!';
    }
}
class Goodbye extends Hello {
    function getMessage() {
        $parentMsg = parent::getMessage();
        return $parentMsg . '<br />';
    }
}
```

```php
$goodbye = new Goodbye();
$goodbye->getMessage();
```

使用`parent`关键字，我们可以访问父方法。注意上述代码实现了相同的结果。

### PHP 不会级联构造函数

大多数面向对象的语言（如 Java）会在运行子类的覆盖构造函数之前自动运行父类的构造函数——这是 PHP 没有的功能。

如果你在子类中创建构造函数，请注意你正在重写父类的构造函数，如果你仍然希望父类处理初始化，则必须显式调用它。

重写成员变量的方法与方法相同，尽管你可能不会频繁使用这一功能。

### 继承实战

现在你对 PHP 中如何使用继承有了大致了解，是时候看一个可以让你更好地理解如何应用继承的示例了。

下面的示例实现了一个网页的简单导航系统，生成出现在页面顶部的 HTML。通过让一个类继承另一个类，可以在需要时为页面添加“面包屑”导航。

文件：`12.php`（节选）

```php
<?php
/**
 * 网页的标准头部
 */
class StandardHeader {
    /**
     * 头部存储在这里
     */
    var $header = '';

    /**
     * 构造函数，接收页面标题
     */
    function StandardHeader($title) {
        $html = <<EOD
<head>
<title>$title</title>
</head>
<body>
<h1>$title</h1>
</body>
EOD;
        $this->setHeader($html);
    }

    /**
     * 向头部添加内容的通用方法
     */
    function setHeader($string) {
        if (empty($this->header)) {
            $this->header .= $string;
        } else {
            $this->header = $string;
        }
    }
    
    function getHeader() {
        return $this->header;
    }
}
```

```php
/**
 * 获取页头
 */
function getHeader() {
    return $this->header;
}
```

现在，子类`CategoryHeader`为其父类增加了额外功能，在生成的 HTML 中添加了“面包屑”链接。我们不需要重新创建`setHeader`和`getHeader`方法，因为在实例化`CategoryHeader`时，这些方法已经从`StandardHeader`继承了。

```php
/**
 * 处理分类的子类，构建面包屑菜单
 */
class CategoryHeader extends StandardHeader {
    /**
     * 构造函数，接收名称和页面的基础 URL
     */
    function CategoryHeader($category, $baseUrl) {
        // 调用父类构造函数
        parent::StandardHeader($category);

        // 构建面包屑
        $html = <<EOD
<p><a href="$baseUrl">Home</a></a><a href="$baseUrl?category=$category">$category</a></a></p>
EOD;
        // 调用父类 setter 方法
        $this->setHeader($html);
    }
```

现在让我们来使用这两个类吧：

```php
// 设置基础 URL
$baseUrl = '12.php';

// 一个有效分类的数组
```

```php
$categories = array('PHP', 'MySQL', 'CSS');

// 检查是否正在查看一个有效分类
if (isset($_GET['category']) &&
in_array($_GET['category'], $categories)) {

  // 实例化子类
  $header = new CategoryHeader($_GET['category'], $baseUrl);
} else {

  // 否则是首页。实例化父类
  $header = new StandardHeader('Home');
}

// 显示页头
echo $header->getHeader();
?>
<h2>Categories</h2>
<p><a href="?php echo $baseUrl;?category=PHP">PHP</a></p>
<p><a href="?php echo $baseUrl;?category=MySQL">MySQL</a></p>
<p><a href="?php echo $baseUrl;?category=CSS">CSS</a></p>
</body>
</html>
```

你可以看到，控制主体会寻找`$_GET['category']`变量。如果它存在，就会创建一个`CategoryHeader`实例，显示导航以允许用户找到返回首页的路。但如果它不存在，则会创建一个父类`StandardHeader`实例，这适用于用户查看首页时（因此不需要面包屑来返回首页）。

换句话说，继承允许我们添加所需的额外功能，而无需重现父类中已有的逻辑；现有的方法和逻辑可以通过子子类进行复用。

继承提供了一种强大的机制，可以创建出模块化的类来解决特定问题，同时确保无论我们处理的是哪个具体的对象，共享的方法和变量都可以被使用。

# 避免深层次的继承结构

作为一个通用的准则，当使用继承来构建类层次结构时，深度不要超过两代。

![](img/80d007a3dc499b219e99d11695c2c366_76_0.png)

# 第 2 章：面向对象的 PHP

这样做通常是设计不佳的标志，即错过了类之间以不同方式交互的机会（参见下一个解决方案）。在实践中，类层次超过两代通常会导致各种调试问题，并使代码难以维护。例如，可能很难跟踪你在层次结构高层使用的变量名。

## 对象之间如何交互？

除了继承之外，对象之间还有其他交互方式；例如，一个对象使用另一个对象。在许多方面，这种交互比继承更重要，这正是面向对象范式展现其实力的地方。

一个对象可以使用其他对象的方法有两种：**聚合（aggregation）和组合（composition）。**

### 聚合 (Aggregation)

当一个对象“临时借用”另一个对象时，就会发生聚合。第二个对象通常会被传递给第一个对象的成员函数。随后第一个对象就可以调用第二个对象的方法，允许它将第二个对象中存储的功能用于自己的目的。

聚合的一个常见示例涉及数据库连接类。想象你将一个数据库连接类传递给另一个类，然后该类使用该数据库连接类来执行查询。执行查询的类**聚合**了数据库连接类。

这里有一个使用 MySQL 类的简单示例，我们将在第 3 章创建它：

```php
<?php
// 引入 MySQL 数据库连接类
require_once 'Database/MySQL.php';

// 聚合 MySQL 类的类
class Articles {
    var $db;
    var $result;
    // 接收 MySQL 类的实例

    function Articles(&$db) {
        // 将对象赋值给本地成员变量
        $this->db = &$db;
        $this->readArticles();
    }

    function readArticles() {
        // 使用 MySQL 类执行查询
        $sql = "SELECT * FROM articles LIMIT 0,5";
        $this->result = $this->db->query($sql);
    }

    function fetch() {
        return $this->result->fetch();
    }
}

// 创建 MySQL 类的实例
$db = &new MySQL('localhost', 'harryf', 'secret', 'sitepoint');

// 创建 Article 类的实例，传递 MySQL 对象
$articles = &new Articles($db);

while ($row = $articles->fetch()) {
    echo '<pre>';
    print_r($row);
    echo '</pre>';
}
```

你可以看到，控制主体会寻找`$_GET['category']`变量。如果它存在，就会创建一个`CategoryHeader`实例，显示导航以允许用户找到返回首页的路。但如果它不存在，则会创建一个父类`StandardHeader`实例，这适用于用户查看首页时（因此不需要面包屑来返回首页）。

换句话说，继承允许我们添加所需的额外功能，而无需重现父类中已有的逻辑；现有的方法和逻辑可以通过子子类进行复用。

继承提供了一种强大的机制，可以创建出模块化的类来解决特定问题，同时确保无论我们处理的是哪个具体的对象，共享的方法和变量都可以被使用。

# 第 2 章：面向对象的 PHP

| Articles |
| :--- |
| $db |
| $result |
| 接收 MySQL 类的实例 |
| (string) |
| 共享的方法和变量都可以 |
| 无论我们处理的是哪个具体的对象。 |

| Articles |
| :--- |
| $db |
| $result |
| +readArticles() |
| +fetch() |

### 聚合 (Aggregation)

当一个对象“临时借用”另一个对象时，就会发生聚合。第二个对象通常会被传递给第一个对象的成员函数。随后第一个对象就可以调用第二个对象的方法，允许它将第二个对象中存储的功能用于自己的目的。

聚合的一个常见示例涉及数据库连接类。想象你将一个数据库连接类传递给另一个类，然后该类使用该数据库连接类来执行查询。执行查询的类**聚合**了数据库连接类。

这里有一个使用 MySQL 类的简单示例，我们将在第 3 章创建它：

```php
<?php
// 引入 MySQL 数据库连接类
require_once 'Database/MySQL.php';

// 聚合 MySQL 类的类
class Articles {
    var $db;
    var $result;
    // 接收 MySQL 类的实例

    function Articles(&$db) {
        // 将对象赋值给本地成员变量
        $this->db = &$db;
        $this->readArticles();
    }

    function readArticles() {
        // 使用 MySQL 类执行查询
        $sql = "SELECT * FROM articles LIMIT 0,5";
        $this->result = $this->db->query($sql);
    }

    function fetch() {
        return $this->result->fetch();
    }
}

// 创建 MySQL 类的实例
$db = &new MySQL('localhost', 'harryf', 'secret', 'sitepoint');

// 创建 Article 类的实例，传递 MySQL 对象
$articles = &new Articles($db);

while ($row = $articles->fetch()) {
    echo '<pre>';
    print_r($row);
    echo '</pre>';
}
```

你可以看到，控制主体会寻找`$_GET['category']`变量。如果它存在，就会创建一个`CategoryHeader`实例，显示导航以允许用户找到返回首页的路。但如果它不存在，则会创建一个父类`StandardHeader`实例，这适用于用户查看首页时（因此不需要面包屑来返回首页）。

### 组合 (Composition)

当一个对象“完全拥有”另一个对象时，就会发生组合。也就是说，第一个对象负责创建第二个对象。在很多情况下，这种情况下是非常有用的，尽管通常，组合用于可能只有一个类需要使用 Session 的情况。

来自第二卷第 1 章的一个例子是`Auth`类，它组合了`Session`类，在构造函数中创建它：

```php
class Auth {
    ...
    /**
     * Session 类实例
     * @var Session
     */
    var $session;

    function Auth($dbConn, $redirect, $md5 = true)
    {
        $this->dbConn = &$dbConn;
        $this->redirect = $redirect;
        $this->md5 = $md5;
        $this->session = &new Session();
        $this->checkAddress();
        $this->login();
    }
}
```

因为`Auth`类需要读写会话变量，并且应用程序中只有少数不相关的类可能也需要 Session，所以让它创建自己的 Session 是合理的。

点击此处订购 PHP Anthology Volume I & II 并享受 25% 折扣！

# 第 2 章：面向对象的 PHP



# 多态

面向对象编程的另一个强大方面是多态——不同类共享同一个接口的能力。

接口由一个或多个方法组成，允许你为了特定目的使用某个类。例如，你可以有两个数据库连接类——一个用于 MySQL，另一个用于 PostgreSQL。只要它们提供一个 `query` 方法，你就可以交替使用它们在不同的数据库上运行查询。`query` 方法就是这两个类共享的简单接口。

共享相同接口的类通常继承自父类，该父类提供了公共方法。同样，通过示例来理解是最好的。

首先，我们定义了一个抽象基类 `Message`，它提供了公共方法 `get()`。在 `Message` 类之下，我们定义了具体类，这些类创建特定的消息。

"抽象（abstract）"和"具体（concrete）"术语指的是类的用法，特别是指一个类是否被设计为直接使用。抽象类是所有子类都将共享某些功能或结构，但并不打算被直接使用的类；它有一个或多个不执行任何用处的空方法。换句话说，你不应该从抽象类创建对象。具体类是抽象类的子类，你可以从中创建对象。某些语言（如 Java）在语言语法中提供了对抽象类的支持——PHP 4 则没有。尽管如此，在设计应用程序时你仍然可以使用抽象类的概念，不过你可能考虑添加文档告诉告诉代码的其他开发者该类是抽象的。

```php
<?php
class Message {
    var $message;
    function setMessage($message) {
        $this->message = $message;
    }
    function getMessage() {
        return $this->message;
    }
}
```

文件：`14.php` (节录)

[点击此处订购 The PHP Anthology Volume I & II 并享受 75 折优惠！]()

```php
class PoliteMessage extends Message {
  function PoliteMessage()
  {
    $this->setMessage('How are you today?');
  }
}

class TerseMessage extends Message {
  function TerseMessage()
  {
    $this->setMessage('Howzit?');
  }
}

class RudeMessage extends Message {
  function RudeMessage()
  {
    $this->setMessage('You look like ** today!');
  }
}
```

我们定义了 `MessageReader` 类，它通过构造函数接收一个 `Message` 对象的数组。

文件：`14.php` (节录)

```php
class MessageReader {
  var $messages;
  function MessageReader(&$messages) {
    $this->messages = &$messages;
    $this->readMessages();
  }
  function readMessages() {
    foreach ($this->messages as $message) {
      echo $message->getMessage() . '<br />';
    }
  }
}
```

这里需要注意的重要点是，对于 `MessageReader` 而言，"消息对象"是任何从 `Message` 类或其任一子类实例的对象。你看到了吗，在 `readMessages` 方法内部调用了 `getMessage` 方法？这段代码适用于任何具有 `getMessage` 方法的对象——包括 `Message` 的任何子类。

现在，为了证明这一点，让我们使用我们的三个子类随机创建一些 `Message` 对象：

文件：`14.php` (节录)

```php
$classNames = array('PoliteMessage', 'TerseMessage', 'RudeMessage');
$messages = array();
srand((int((float)microtime()) * 1000000)); // 准备随机洗牌
for ($s=0; $s<10; $s++) {
  shuffle($classNames);
  $messages[] = new $classNames[0]();
}
$messageReader = new MessageReader($messages);
?>
```

通过创建 `$classNames` 并反复洗牌，我们可以获取数组的第一个元素并用它创建一个新对象：

```php
$messages[] = new $classNames[0]();
```

这是一个变量函数的示例。表达式`$classNames[0]`被求值为要调用的构造函数名称（`PoliteMessage`、`TerseMessage` 或 `RudeMessage`）。

最后，`$messages` 数组包含了随机选择的消息，并在实例化时传递给 `MessageReader` 的构造函数。

这是一个示例结果：

```
You look like ** today!
Howzit?
How are you today?
How are you today?
How are you today?
You look like ** today!
How are you today?
How are you today?
Howzit?
How are you today?
```

每次我们执行脚本时，列表都是不同的。

由于所有具体类都共享相同的 `getMessage` 函数（即它们实现了接口），`MessageReader` 类能够提取数据，而无需知道它处理的是哪种类型的消息。一组相关类交替工作的能力被称为多态，如图 2.4 所示的 UML 图。

### 图 2.4. 多态

| MessageReader | Message |
| :--- | :--- |
| -messages : array | -message : string |
| -readMessages(): void | +getMessage() : string |
| | #setMessage(in message : string) : void |

一旦你意识到它的价值，面向对象编程的这个方面将非常强大。例如，你可能有一个代表 HTML 标签的对象集合。

## 基础连接

以下是最简单形式的 MySQL 数据库连接：

```php
<?php
$host = 'localhost'; // MySQL 服务器主机名
$dbUser = 'harryry'; // MySQL 用户名
$dbPass = 'secret'; // 用户密码
$dbName = 'sitepoint'; // 数据库名称

// 连接 MySQL 服务器
if ($dbConn = mysql_connect($host, $dbUser, $dbPass)) {
    die('无法连接到服务器');
}

// 选择数据库
if (!mysql_select_db($dbName, $dbConn)) {
    die('无法选择数据库');
}
// 连接成功！
// ... 在此处使用 MySQL 的某些代码

// 完成后关闭连接
mysql_close($dbConn);
?>
```

需要记住，MySQL 是一个独立的服务器程序，就像 Apache 一样。这两个服务器可能运行在同一台物理计算机上（因此在上面的示例中我们`$host = 'localhost';`），也可以将 MySQL 连接到远程计算机，例如`$host = 'anothercomputer.com';`。更有趣的是，MySQL 还有自己的端口号，默认是 3306。PHP 假设 3306 是你需要使用的端口，如果使用不同的端口，只需设置`$host = 'anothercomputer.com:4321';`。

另一个概念上的障碍在于理解：单个 MySQL 服务器可以提供许多数据库的访问，这就是为什么在连接服务器后，你需要在 PHP 中选择你的数据库。

回到上面的代码，有几点需要注意。首先，我将连接 MySQL 所需的值放在了变量中。这让我们的工作变得更简单；通常会将此类信息存储在每个 PHP 脚本都会包含的单独文件中，这样就可以一次性更改多个脚本。稍后我们将查看可以采用的让生活更轻松的进一步技巧。

## 第 3 章：PHP 与 MySQL

`mysql_connect` 函数负责连接 MySQL 服务器的工作。它返回的值要么是一个链接标识（PHP 提供的用于标识连接的值），要么是 `FALSE`（连接失败）。

```php
if (!$dbConn = mysql_connect($host, $dbUser, $dbPass)) {
    die('无法连接到服务器');
}
```

这条语句提问："我是否成功连接到了 MySQL 服务器？"如果没有成功，它将使用 `die` 终止脚本。

接下来，我们将使用相同的语句技术通过 `mysql_select_db` 选择我们需要的数据库：

```php
if (!mysql_select_db($dbName, $dbConn)) {
```

注意，我们将链接标识符变量作为第二个参数传递给 `mysql_select_db`。虽然我们通常不会这样做（该参数是可选的），但当一个复杂脚本处理多个数据库连接时，这种方法可以帮助 PHP 知道你指的是哪一个。

最后，我们使用 `mysql_close` 断开与服务器的连接：

```php
mysql_close($dbConn);
```

这发生在脚本底部，在我们运行了一些使用该连接的 PHP 代码之后。关闭连接通常是可选的——PHP 在脚本结束后会自动关闭任何连接。

> 使用 `mysql_pconnect` 的连接是不同的。该函数建立到数据库的持久连接，供多个 PHP 脚本重用。使用持久连接会让你的脚本运行更快，因为 PHP 不再每次都要重新连接，但速度是有代价的：如果你的网站运行在共享服务器上，持久连接可能会垄断连接，导致其他网站有时无法连接。在这种环境中，通常会避免使用 `mysql_pconnect`，或者配置 MySQL 让连接在停止操作时立即终止，并设置较短的连接超时值。

点击此处订购《The PHP Anthology Volume I & II》并享受 75 折优惠！

## 可重用代码

你刚刚看到了连接 MySQL 最简单的方法。然而，将上述代码"封装"在函数或类中通常很有用，这样它可以被重用。

作为一个函数，我们可以拥有：

```php
<?php
function connectToDb($host, $dbUser, $dbPass, $dbName) {
  // 连接 MySQL 服务器
  if (!@mysql_connect($host, $dbUser, $dbPass)) {
    return false;
  }

  // 选择数据库
  if (!@mysql_select_db($dbName)) {
    return false;
  }

  return $dbConn;
}

$host = 'localhost'; // MySQL 服务器主机名
$dbUser = 'harry'; // MySQL 用户名
$dbPass = 'secret'; // 用户密码
$dbName = 'sitepoint'; // 数据库名称

$dbConn = &connectToDb($host, $dbUser, $dbPass, $dbName);
?>
```

这把连接 MySQL 和选择数据库的过程简化为了单行（如果你算上 `include` 语句，它指向包含 `connectToDb` 函数的单独文件）：

`$dbConn = &connectToDb($host, $dbUser, $dbPass, $dbName);`

注意我们使用了引用操作符 `&`。这个运算符及其作用在第 2 章中详细介绍过。

## 第 3 章：PHP 与 MySQL

### 偷懒一点：编写良好的代码

科学家现在已经明确证明，PHP 知识与空闲时间成反比，但与脱发成正比。防止这些影响的唯一方法尽早学习编写可扩展、可维护且可重用的代码。在 PHP 中利用类和面向对象是向正确方向迈出的一步。作为一名 PHP 开发者，偷懒是一种美德。

进一步，我们可以将这段代码封装在一个类中：

文件：`Database/MySQL.php`（位于 SPLIB 中）（节选）

```php
/**
 * MySQL 数据库连接类
 *
 * @access public
 * @package SPLIB
 */
class MySQL {

    /**
     * MySQL 服务器主机名
     *
     * @access private
     * @var string
     */
    var $host;

    /**
     * MySQL 用户名
     *
     * @access private
     * @var string
     */
    var $dbUser;

    /**
     * MySQL 用户密码
     *
     * @access private
     * @var string
     */
    var $dbPass;

    /**
     * 数据库名称
     *
     * @access private
     * @var string
     */
    var $dbName;

}
```

### 我如何从表中获取数据？

在这里使用类的目的是为了练习使用 PHP 的对象模型来处理常见任务。如果你是 PHP 面向对象编程的新手，在这个阶段最需要记住的一点是：你不需要理解类中发现的所有代码，就可以在你的代码中使用它。

我们将在整本书中使用这个类以及其他类，用来说明面向对象编程如何允许代码复用，并在开发应用程序时节省时间。

## 我如何从表中获取数据？

连接到数据库当然是好事。但如果我们无法从从中获取任何内容，它又有什么用呢？

从 MySQL 获取数据有多种方法，但最常用的可能是结合 `mysql_query` 使用 `mysql_fetch_array`。

我们只需要在"我如何访问 MySQL 数据库？"中看到的 `connectToDb` 函数中添加一点内容，就可以从该表中获取数据：

```php
// Connect to MySQL
$dbConn = &connectToDb($host, $dbUser, $dbPass, $dbName);

// 查询所有文章的 SQL
$sql = "SELECT * FROM articles ORDER BY title";

// 执行查询，标识连接
$queryResource = mysql_query($sql, $dbConn);

// 一次从 MySQL 获取行数据
while ($row = mysql_fetch_array($queryResource, MYSQL_ASSOC)) {
    echo 'Title: ' . $row['title'] . ' <br />';
    echo 'Author: ' . $row['author'] . ' <br />';
    echo 'Body: ' . $row['body'] . ' <br />';
}
```

文件: `4.php`

本质上，获取数据有三个步骤：

1. 首先，将必要的 SQL 查询语句放在字符串中

> 如果你不熟悉结构化查询语言 (SQL)，我将在本章中介绍基础知识。如需更完整的教程，请参阅《Build Your Own Website Driven Using PHP & MySQL, 2nd Edition》(ISBN 0-9579218-0)。

点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！

## 第 3 章：PHP 和 MySQL

```php
$sql = "SELECT * FROM articles ORDER BY title";
```

将它保持在单独变量中非常方便，因为当我们开始编写复杂的查询并出现问题时，我们可以通过这一单行代码双检我们的查询：

```php
echo $sql;
```

2. 接下来，告诉 MySQL 执行查询：

```php
$queryResource = mysql_query($sql, $dbConn);
```

这起初可能会让人困惑。当你告诉 MySQL 执行查询时，它并不会立即给你结果。它将结果保存在内存中，直到你告诉它要做什么。PHP 使用资源标识符来跟踪结果，这就是你从 `mysql_query` 函数获取的返回值。在上面的代码中，我们将标识符存储在 `$queryResource` 中。

3. 最后，使用 `mysql_fetch_array` 从结果集中一次获取行数据：

```php
while ($row = mysql_fetch_array($queryResource, MYSQL_ASSOC))
```



这将结果集的每一行都放在变量`$row`中。这些行中的每一行都将由一个数组表示。通过在`mysql_fetch_array`使用额外的参数`MYSQL_ASSOC`，我们告诉函数返回一个数组，其中其键（keys）与表中的列名对应。如果你省略了`MYSQL_ASSOC`参数，每个列将以数字索引出现一次（例如`$row[0]`、`$row[1]`等），并以字符串索引出现一次（例如`$row['title']`、`$row['author']`等）。虽然这通常不会引起问题，但指定你想要的数组类型将稍微提高速度。

如上所示，使用循环处理结果集的每一行是一种常用方法。循环实际上是在说：“从 MySQL 获取行，直到我无法获取更多数据为止”，而循环体会在获取每一行时对其进行处理。

## 大规模查询的前台缓冲（Foreground Buffering）

对于大型查询（即产生大型结果集的查询），你可以通过告诉 PHP 不要缓冲查询结果来大幅提高性能。当查询被缓冲时，整个结果在从 MySQL 获取并存储在内存中之前，你的脚本才会被继续执行。

点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！

## 使用类获取数据

另一方面，无缓冲查询（unbuffered query）允许 MySQL 保留结果，直到你一次一次地请求它们（例如使用`mysql_fetch_array`）。这不仅允许你的脚本在 MySQL 执行查询时继续运行，还节省了 PHP 在内存中存储所有行的开销：

PHP 允许你通过`mysql_unbuffered_query`执行无缓冲查询：

```php
$QueryResource = mysql_unbuffered_query($sql, $dbConn);
```

当然，凡事皆有代价——对于无缓冲查询，你不能再使用`mysql_num_rows`函数来计算行数。显然，由于 PHP 不保留完整结果集的副本，它无法计算它自己的行数！你必须在执行另一个查询之前，从 MySQL 获取结果集中的所有行。

虽然存在其他用于查询结果现有行和单元格的函数（如`mysql_fetch_object`和`mysql_result`），但你仅用`mysql_fetch_array`就能实现相同的功能，这种一致性可能有助于保持代码的简单。

现在你已经掌握了获取现有行和单元格的基础知识，让我们来看看这个`MySQLResult`类。

## 如何在我的数据库中添加或修改数据？

最好是结合`trigger_error`函数使用（该函数将在第10章中详细讨论），该函数允许你控制错误消息的输出。让我们修改一下之前看到的基础连接代码：

文件：6.php（节选）

```php
// 连接到 MySQL 服务器

if (!$dbConn = mysql_connect($host, $dbUser, $dbPass)) {
    trigger_error('Could not connect to server: ' . mysql_error());
}
```

```php
// 选择数据库

if (!mysql_select_db($dbName)) {
    trigger_error('Could not select database: ' . mysql_error());
}
```

同样的方法也可以用于查询：

文件：6.php（节选）

```php
// 查询所有文章的查询

$sql = "SELECT * FROM articles ORDER BY title";
```

```php
// 执行查询并标识连接

if (!$queryResource = mysql_query($sql, $dbConn)) {
    trigger_error('Query error ' . mysql_error() . ': SQL: ' . $sql);
}
```

返回完整的查询本身是一个好主意，正如我们在上面的示例中所示，特别是使用 PHP 变量构建它时。这让你能够精确看到执行了什么查询，如果有必要，可以直接在 MySQL 中执行它以确定具体错误出在哪里。

上面讨论的 MySQL 类在遇到问题时会自动使用`mysql_error`和`trigger_error`。

## 如何在我的数据库中添加或修改数据？

能够从数据库中获取数据只是开始，但你最初如何将数据放入那里呢？

点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！

# 第三章：PHP 和 MySQL

再次，PHP 的答案是简单的：使用`mysql_query`函数结合 SQL 命令`INSERT`和`UPDATE`。`INSERT`用于在表中创建新行，而`UPDATE`用于修改现有的行。

### 插入行

使用本章开头定义的`articles`表，一个简单的`INSERT`如下所示：

```php
// 插入数据的查询

$sql = "INSERT INTO

    articles

    SET

        title = '$title',

        body = '$body',

        author = '$Author';

// 执行查询并标识连接

if (!$QueryResource = mysql_query($sql, $dbConn)) {
    trigger_error('Query error ' . mysql_error() . ' SQL: ' . $sql);
}
```

### 更新行

在可以使用`UPDATE`查询之前，你需要确定要更新表中的哪几行。在这个示例中，我使用了`SELECT`来获取标题为“如何插入数据”的文章的唯一`article_id`值：

```php
// 选择文章的查询

$sql = 'SELECT article_id FROM articles

WHERE title = 'How to insert data';

if (!$QueryResource = mysql_query($sql, $dbConn)) {
    trigger_error('Query error ' . mysql_error() . ' SQL: ' . $sql);
}

// 从结果中获取单行

$row = mysql_fetch_array($QueryResource, MYSQL_ASSOC);

// 一个新标题

$title = 'How to update data';
```

```php
$sql = "UPDATE articles

SET title='$title'

WHERE article_id=' . $row['article_id'] . '";
```

```php
if (!$queryResource = mysqli($sql, $dbConn)) {
    trigger_error('Query error ' . $mysql_error() . ': SQL: ' . $sql);
}
```

在上面的示例中，我们使用`SELECT`查询来找到想要更新的行的 ID。

在实际的 Web 应用程序中，`UPDATE`可能发生在依赖 Web 浏览器输入的页面上，例如在用户使用 HTML 表单输入值（s）之后。这些数据中的字符串可能包含单引号，这会破坏 SQL 并影响安全。鉴于此，请确保阅读了“如何解决由引号/单引号引起的数据库错误？”，它涵盖了 SQL 注入攻击。

![](img/80d007a3dc499b219e99d11695c2c366_102_0.png)

### 注意全局更新

使用`UPDATE`时要小心，记得使用`WHERE`子句指示更改哪些行。

例如，考虑此查询：

```sql
UPDATE articles SET title = 'How NOT to update data'
```

这将更新表中的每一行！

### 另一个类操作

使用“如何从表中获取数据?”中最后提到的 MySQL 类，我们可以在无需任何进一步修改的情况下执行`INSERT`和`UPDATE`查询。使用类重复上述示例，我们可以先这样`INSERT`：

```php
// 连接到 MySQL

$db = &new MySQL($host, $dbUser, $dbPass, $dbName);

$title = 'How to insert data';

$body = 'This is the body of the article';
```

点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！

# 第三章：PHP 和 MySQL

```php
$author = 'HarryF';

// 插入数据的查询

$sql = 'INSERT INTO articles

SET

title = '$title',

body = '$body',

author = '$author';

$db->query($sql);

if ($db->isError()) {
    echo 'INSERT successful';
} else {
    echo 'INSERT failed';
}
```

我们可以如下进行`UPDATE`：

```php
$db = &new MySQL($host, $dbUser, $dbPass, $dbName);

// 选择文章的查询

$sql = 'SELECT article_id FROM articles

WHERE title='How to insert data';

$result = $db->query($sql);

$row = $result->fetch();

// 一个新标题

$title = 'How to update data';

$sql = "UPDATE articles

SET

title=''. $title.'. '

WHERE

article_id=' '.$row['article_id'] . ''";

$db->query($sql);

if (!$db->isError()) {
    echo 'UPDATE successful';
} else {
    echo 'UPDATE failed';
}
```

文件：10.php（节选）

82

点击此处订购《PHP Anthology Volume I & II》并享受 75 折优惠！

## 如何解决由引号/单引号引起的数据库错误？

考虑以下内容：

```sql
INSERT INTO articles SET title='PHP';
```

### 转义

解决方案是通过添加反斜杠来转义单引号。例如，以下有效：

```sql
INSERT INTO articles SET title='PHP\'s';
```

### 反斜杠与 ANSI SQL 标准

注意使用反斜杠作为转义字符并不是 ANSI SQL。如果你只使用 MySQL 数据库，反斜杠可能是接受的，但在另一个数据库上运行相同的语句可能会失败。根据 ANSI SQL，我们应该用另一个单引号来转义单引号：

```sql
INSERT INTO articles SET title='PHP''s';
```

> 令我不断惊讶的是，许多设计专业的网站未能正确处理转义！请留意你自己的网站中意外的反斜杠。参考第1章关于如何在你的网站上最好避免此问题的建议。

接下来，我们来看 PHP 的`addslashes`。应用于任何字符串时，`addslashes`将使用反斜杠对单引号、双引号、反斜杠和空字符进行转义。这使其成为查询转义字符串的有效手段。

如果使用了魔引号（magic quotes），当然，你不能使用`addslashes`，否则字符会被转义两次！为了解决这个冲突，你可以使用`get_magic_quotes_gpc`函数检查是否启用了魔引号，如果启用则返回 TRUE，如果未启用则返回 FALSE。你可以如下所示将此测试封装在一个函数中：

```php
<?php

function safeAddSlashes($string)
{
    if (get_magic_quotes_gpc()) {
        return $string;
    } else {
        return addslashes($string);
    }
}

?>
```

第三种方法与`addslashes`非常类似，使用的是`mysql_escape_string`或`mysql_real_escape_string`函数（后者在 PHP 4.3.0 中引入）。这些函数使用底层的 MySQL C++ API（由 MySQL 开发者提供，而非 PHP 开发者）来对特殊字符进行转义。

这些函数转义空字符、换行符、回车符、反斜杠、单引号、双引号和结束符。从 PHP 4.3.0 开始，这两个函数都使用了 PHP 与 MySQL 连接时使用的当前字符集。因此，在最新的 PHP 版本中，这两个函数没有区别，如果你的服务器是最新的，可以自由使用其中较短的`mysql_escape_string`。

由于这种方法是 MySQL 内置的字符串转义机制，我推荐使用它而不是`addslashes`或`magic_quotes_gpc`。当然，如果你想让你的 SQL 良好迁移到其他数据库，你可能想要将该函数“隐藏”在类方法中，这样在移动到不同的数据库时，就可以更换整个类（包括转义机制）。

# 第三章：PHP 与 MySQL

再次，如果你没有通过其他方式处理魔引号问题，你必须检查`magic_quotes_gpc`是否开启：

```php
<?php

function safeEscapeString($string)
{
    if (get_magic_quotes_gpc()) {
        return $string;
    } else {
        return mysql_real_escape_string($string);
    }
}

?>
```

书中的脚本使用了第 1 章引入并包含在代码存档中的`MagicQuotes/strip_quotes.php`文件，以便在启用了魔引号的服务器上有效地切换魔引号，因此后续的解决方案将自由使用`mysql_real_escape_string`。如果你认为自己对手动转义引号和其他特殊字符有信心，我鼓励你在自己的脚本中也这样做。

# SQL 注入攻击

SQL 注入发生于攻击者利用你网站上合法的用户输入机制发送 SQL 代码，而你毫无防备的脚本会将这些代码传递给数据库执行。黄金法则：在让数据接触数据库之前，对所有来自外部源的数据进行转义。该规则不仅适用于`INSERT`和`UPDATE`查询，也适用于`SELECT`。

许多 PHP 开发者由于 MySQL 的局限性免受 SQL 注入的影响，每次调用`mysql_query()`只允许执行单个 SQL 语句。在其他数据库上，SQL 注入的影响可能是灾难性的，因为攻击者可以发送第二个查询，例如删除整个表的内容。然而，使用 MySQL 时问题仍然可能发生，如下代码所示：

```php
$sql = "SELECT * FROM users WHERE username='" . $_POST['username'] . "' AND password='" . $_POST['password'] . "'";

echo 'Query: ' . $sql . '<br/>';

$rows = mysql_num_rows($result);

if ($rows > 0) {
    echo 'You are logged in!<br />';
} else {
    echo 'You are not allowed here!<br />';
}
```

```html
<form method="post" action="<?php echo $_SERVER['PHP_SELF']; ?>">
<input type="text" name="username" /><br />
<input type="text" name="password" /><br />
<input type="submit" />
</form>
```

聪明的攻击者只需在表单的密码字段中输入以下内容：

`' OR username LIKE '%'`

假设你的服务器上禁用了魔引号，且你没有采取其他措施来防止它，这个巧妙的操作改变了查询的含义：

```sql
SELECT * FROM users
WHERE username='' AND password=''' OR username LIKE '%'
```

修改后的查询将选择用户表中的所有记录！当脚本检查是否有用户匹配提供的用户名和密码组合时，它将看到这个巨大的结果集并授予访问网站的权限：

可以通过以下方法防止这种情况：

```php
$sql = "SELECT * FROM users
WHERE username='' . safeEscapeString($_POST['username']) . ''
AND password='' . safeEscapeString($_POST['password']) . ''";
```

在某些情况下，取决于具体情况，这可能是必要的。但如果你看重你的睡眠，请记住那个黄金法则：对所有来自外部源的数据进行转义。

## 我该如何创建灵活的 SQL 语句？

SQL 是一种操作数据的强大语言。使用 PHP，我们可以根据变量构建 SQL 语句，这对于按单列对表进行排序或跨多个页面显示大型结果非常有用。

# 第三章：PHP 与 MySQL



再次，如果你没有通过其他方式处理魔引号问题，你必须检查`magic_quotes_gpc`是否开启：

```php
<?php
function safeEscapeString($string) {
    if (get_magic_quotes_gpc()) {
        return $string;
    } else {
        return mysql_real_escape_string($string);
    }
}
?>
```

书中的脚本使用了第 1 章引入并包含在代码存档中的`MagicQuotes/strip_quotes.php`文件，以便在启用了魔引号的服务器上有效地切换魔引号，因此后续的解决方案将自由使用`mysql_real_escape_string`。如果你认为自己对手动转义引号和其他特殊字符有信心，我鼓励你在自己的脚本中也这样做。

# SQL 注入攻击

SQL 注入发生于攻击者利用你网站上合法的用户输入机制发送 SQL 代码，而你毫无防备的脚本会将这些代码传递给数据库执行。黄金法则：在让数据接触数据库之前，对所有来自外部源的数据进行转义。该规则不仅适用于`INSERT`和`UPDATE`查询，也适用于`SELECT`。

许多 PHP 开发者由于 MySQL 的局限性免受 SQL 注入的影响，每次调用`mysql_query()`只允许执行单个 SQL 语句。在其他数据库上，SQL 注入的影响可能是灾难性的，因为攻击者可以发送第二个查询，例如删除整个表的内容。然而，使用 MySQL 时问题仍然可能发生，如下代码所示：

```php
$sql = "SELECT * FROM users WHERE username='" . $_POST['username'] . "' AND password='" . $_POST['password'] . "'";
echo 'Query: ' . $sql . '<br/>';
```

点击此处购买《The PHP Anthology Volume 1 & II》并获得 75 折优惠！

```php
$rows = mysql_num_rows($result);

if ($rows > 0) {
    echo 'You are logged in!<br />';
} else {
    echo 'You are not allowed here!<br />';
}
```

```php
<form method="post" action="<?php echo $_SERVER['PHP_SELF']; ?>">

<input type="text" name="username" /><br />

<input type="text" name="password" /><br />

<input type="submit" />

</form>
```

聪明的攻击者只需在表单的密码字段中输入以下内容：

```
' OR username LIKE '%'
```

假设你的服务器上禁用了魔引号，且你没有采取其他措施来防止它，这个巧妙的操作改变了查询的含义：

```sql
SELECT * FROM users

WHERE username='' AND password=''' OR username LIKE '%'
```

修改后的查询将选择用户表中的所有记录！当脚本检查是否有用户匹配提供的用户名和密码组合时，它将看到这个巨大的结果集并授予访问网站的权限。

可以通过以下方法防止这种情况：

```php
$sql = "SELECT * FROM users

WHERE username='' . safeEscapeString($_POST['username']) . ''

AND password='' . safeEscapeString($_POST['password']) . ''";
```

在某些情况下，取决于具体情况，这可能是必要的。但如果你看重你的睡眠，请记住那个黄金法则：对所有来自外部源的数据进行转义。

# 我该如何创建灵活的 SQL ？

SQL 是一种操作数据的强大语言。使用 PHP，我们可以根据变量构建 SQL 语句，这对于按单列对表进行排序或跨多个页面显示大型结果非常有用。

# 第三章：PHP 与 MySQL

再次，如果你没有通过其他方式处理魔引号问题，你必须检查`magic_quotes_gpc`是否开启：

```php
<?php

function safeEscapeString($string) {

    if (get_magic_quotes_gpc()) {

        return $string;

    } else {

        return mysql_real_escape_string($string);

    }

}

?>
```

书中的脚本使用了第 1 章引入并包含在代码存档中的`MagicQuotes/strip_quotes.php`文件，以便在启用了魔引号的服务器上有效地切换魔引号，因此后续的解决方案将自由使用`mysql_real_escape_string`。如果你认为自己对手动转义引号和其他特殊字符有信心，我鼓励你在自己的脚本中也这样做。

# SQL 注入攻击

SQL 注入发生于攻击者利用你网站上合法的用户输入机制发送 SQL 代码，而你毫无防备的脚本会将这些代码传递给数据库执行。黄金法则：在让数据接触数据库之前，对所有来自外部源的数据进行转义。该规则不仅适用于`INSERT`和`UPDATE`查询，也适用于`SELECT`。

许多 PHP 开发者由于 MySQL 的局限性免受 SQL 注入的影响，每次调用`mysql_query()`只允许执行单个 SQL 语句。在其他数据库上，SQL 注入的影响可能是灾难性的，因为攻击者可以发送第二个查询，例如删除整个表的内容。

## 第 3 章：PHP 与 MySQL

（我该如何从表中获取数据呢？）以下代码演示了`mysql_num_rows`的用法：

文件：12.php（节录）

```php
// 查询所有文章的语句

$sql = "SELECT * FROM articles ORDER BY title";

// 执行查询，标识连接

$queryResource = mysql_query($sql, $dbConn);

// 获取选定的行数

$numRows = mysql_num_rows($queryResource);

echo $numRows . ' rows<br/>';

// 一次从 MySQL 获取一行数据

while ($row = mysql_fetch_array($queryResource, MYSQL_ASSOC)) {

    echo 'Title: ' . $row['title'] . ' < br/>';

    echo 'Author: ' . $row['author'] . ' < br/>';

    echo 'Body: ' . $row['body'] . ' < br/>';

}
```

在上面的示例中，`mysql_num_rows`函数接收一个结果资源标识符并返回该结果中的行数。

请注意，相关函数`mysql_num_fields`可用于查找选取了多少列。当你使用像`SELECT * FROM`类的查询，但不知道选取了多少列时，这非常有用。

### 使用 MySQL 统计行数

另一种方法是在查询中使用 MySQL 的`COUNT`函数。这要求你执行两次查询——一个用于统计行数，另一个用于实际获取结果——这在性能上会让你产生少许的开销。

以下是你可以使用 MySQL`COUNT`函数的方法：

文件：13.php（节录）

```php
// 查询所有文章的语句

$sql = "SELECT COUNT(*) AS numrows FROM articles";

// 统计返回行数的查询

$queryResource = mysql_query($sql, $dbConn);

$row = mysql_fetch_array($queryResource, MYSQL_ASSOC);

echo $row['numrows'] . ' rows selected<br />';

// 查询所有文章的语句

$sql = "SELECT * FROM articles ORDER BY title";

// 执行查询，标识连接

$queryResource = mysql_query($sql, $dbConn);

// 一次从 MySQL 获取一行数据

while ($row = mysql_fetch_array($queryResource, MYSQL_ASSOC)) {

  echo 'Title: ' . $row['title'] . '<br />';

  echo 'Author: ' . $row['author'] . '<br />';

  echo 'Body: ' . $row['body'] . '<br />';

}
```

注意我们使用了别名来放置`COUNT`函数的结果吗？

```sql
SELECT COUNT(*) AS numrows FROM articles
```

我们这样做是为了稍后可以使用`$row['numrows']`来识别行数。另一种替代方案是省略别名：

```sql
SELECT COUNT(*) FROM articles
```

这将要求我们通过`$row['COUNT(*)']`访问信息，这可能会让代码读起来很困惑。

当我们使用`COUNT`函数时，动态构建查询就变得重要了，正如"如何创建灵活的 SQL 语句？"所示。你需要确保你的`COUNT`查询包含了与"真实"查询中使用的相同的`WHERE`或`LIMIT`子句。例如，如果我们实际用于获取数据的查询是：

```sql
SELECT * FROM articles WHERE author='HarryF'
```

在 PHP 中，我们可能想要像这样的代码：

```php
// 定义可重用的 SQL "块"

$table = " FROM articles";

$where = " WHERE author='HarryF'";

$order  = " ORDER BY title";

// 统计返回行数的查询

$sql = "SELECT COUNT(*) as numrows" . $table . $where;

// 执行查询，标识连接

$queryResource = mysql_query($sql, $dbConn);

$row = mysql_fetch_array($queryResource, MYSQL_ASSOC);

echo $row['numrows'] . " rows selected<br />";

// 获取行的查询

$sql = "SELECT " . $table . $where . $order;

// 执行查询，标识连接

$queryResource = mysql_query($sql, $dbConn);

// 一次从 MySQL 获取一行数据

while ($row = mysql_fetch_array($queryResource, MYSQL_ASSOC)) {

    echo 'Title: ' . $row['title'] . '<br />';

    echo 'Author: ' . $row['author'] . '<br />';

    echo 'Body: ' . $row['body'] . '<br />';

}
```

### 使用类进行行计数

让我们再次看看我们在本节中开发的类。我们可以通过向`MySQLResult`类引入以下方法，增加查找选定行数的功能：

文件：Database/MySQL.php（在 SPLIB 中）节录

```php
/**

 * 返回选定的行数

 * @return int

 * @access public

 */

function size() {

    return mysql_num_rows($this->query);

}
```

以下是使用方法：

```php
// 连接到 MySQL

$db = &new MySQL($host, $dbUser, $dbPass, $dbName);
```

文件：15.php（节录）

[点击此处订购 PHP Anthology Volume I & II 并享受 75 折优惠！]

```php
// 选择所有行

$sql = "SELECT * FROM articles WHERE author='HarryF'";

$result = $db->query($sql);

echo $result->size() . " rows";
```

### 受影响的行数

查找`UPDATE`或`DELETE`语句影响的行数也是可能的。`mysql_affected_rows`函数返回受最后一个查询影响的行数。你可以这样使用：

```php
// 更新某些行

$sql = "UPDATE articles SET title='New Title' WHERE author='HarryF'";

$queryResource = mysql_query($sql, $dbConn);

$affected = mysql_affected_rows($queryResource);

echo $affected . " affected";
```

### 插入 ID

当你处理`AUTO_INCREMENT`列时，通常需要获取新插入行的 ID。`mysql_insertid`函数提供了这些信息。你可以这样使用：

```php
// 插入新行

$sql = "INSERT INTO articles (title, body, author) VALUES ('How to use mysql_insertid()', 'This is an example', 'HarryF')";

$queryResource = mysql_query($sql, $dbConn);

$insertID = mysql_insertid($queryResource);

echo 'The row has ID: ' . $insertID;
```

### 类插入 ID

要在`MySQLResult`类中使用此功能，请添加以下方法：

```php
/**

 * 返回最后插入行的 ID

 * @return int

 * @access public

 */

function insertID() {

    return mysql_insertid($this->dbConn);

}
```

正如你可能猜想到的，这个方法非常直接：

```php
//  MySQL 类

require_once 'Database/MySQL.php';

$host = 'localhost'; // MySQL 服务器主机

$dbUser = 'harry'; // MySQL 用户名

$dbPass = 'secret'; // 用户密码

$dbName = 'sitepoint'; // 数据库名

$db = &new MySQL($host, $dbUser, $dbPass, $dbName);

// 插入新行

$sql="INSERT INTO articles (title, body, author) VALUES ('How to use mysql_insertid()', 'This is an example', 'HarryF')";

$result = $db->query($sql);

echo 'The row as ID: ' . $result->insertID();
```

## 如何搜索我的表？

有些人就是非常急躁；与其浏览你提供的网站导航系统，他们现在就想要信息！因此，像你我这样的 PHP 开发者需要实现搜索功能，为访问者提供寻找所需信息的捷径。在以 HTML 文件形式存储所有内容的时代，这可能是个大问题，但现在你使用数据库进行搜索，搜索变得简单多了。

### 你所 LIKE

最基础的搜索形式是针对单列并使用`LIKE`操作符：

```sql
SELECT * FROM articles WHERE title LIKE 'How %'
```

`%`是一个通配符。上面的语句将选取所有标题以"How"开头的文章。MySQL 还支持 POSIX 正则表达式

## 第3 章：PHP 与 MySQL

表达式（与 PHP 的`ereg`函数相同）。使用`RLIKE`操作符，我们可以通过正则表达式对列进行比较：

```sql
SELECT * FROM articles WHERE title RLIKE '^How '
```

上述语句还选取了所有标题以"How"开头并跟有空格的文章。

通过一些努力，这些操作符提供了探索数据所需的所有内容。但当需要对多个列执行搜索时，上述方法就会变成一种负担。例如：

```sql
SELECT * FROM articles

WHERE title LIKE '%how%' OR body LIKE '%how%'
```



对于较大的表，这可能需要你编写一些非常复杂且不愉快的查询语句。

## 全文检索（FULLTEXT Searches）

MySQL 提供了一种可以替你完成大部分工作的替代方案——全文索引（FULLTEXT index）。数据库中的索引非常像书的索引；它们提供了一种从组织良好的列表中快速定位数据库中的信息的手段。全文索引允许你搜索特定的单词。

全文索引是从 MySQL 3.23 版本引入的。当时的实现相当有限，但对于基础搜索仍然很有用，这也是我将在这里演示的。在 MySQL 4.0.1 中，此功能扩展到了完整的布尔搜索机制，使你能够构建类似于 Google 高级搜索功能的功能。全文索引还允许每个结果带有一个“相关性”值返回。例如，多个单词搜索的结果可以根据每个结果与用户特定搜索的匹配程度来显示。

要利用全文索引，你首先需要指示 MySQL 开始对你想要搜索的列建立索引：

```sql
ALTER TABLE articles FULLTEXT art_search (title, body, author);
```

一旦完成此操作，你需要向 MySQL 插入一条新记录（或修改现有记录）来构建索引。你还需要数据库中至少三条记录才能进行全文搜索，因为非布尔搜索仅在搜索字符串出现在表中少于 50% 的行中时才会返回结果（如果表中只有两行，而你的搜索匹配了其中一行，那就是 50%）。

最后需要注意的一点是，全文搜索只会匹配超过三个字母的搜索；索引机制会忽略三个字符或更少的单词，以避免构建一个巨大的索引。这就像书的索引；你会惊讶地发现书的索引中 “the” 这个单词到底出现在哪些页！

这是一个基础的全文检索示例：

```sql
SELECT *
FROM articles
WHERE MATCH (title, body, author) AGAINST ('MySQL');
```

此搜索将返回所有标题、正文或作者包含 “MySQL” 单词的行。

全文索引的另一个用途是在返回每个示例相关性的搜索中。

文件：`19.php`（节）

```php
// 选择所有行但显示相关性
$sql = "SELECT
    MATCH (title, body, author)
    AGAINST
    ('The PHP Anthology Released Long Word Matching')
    AS
    score
FROM
    articles
ORDER BY score DESC";
```

```php
// 运行查询，识别连接
$queryResource = mysql_query($sql, $dbConn);

// 从 MySQL 逐行获取结果
while ($row = mysql_fetch_array($queryResource, MYSQL_ASSOC)) {
    echo 'Title: ' . $row['title'] . '<br />';
    echo 'Author: ' . $row['author'] . '<br />';
    echo 'Body: ' . $row['body'] . '<br />';
    echo 'Score: ' . $row['score'] . '<br />';
}
```

别名 `score` 包含一个标识该行与搜索相关性的值。该值不是百分比，而是一个衡量标准：0 表示完全没有匹配。单个单词会产生 1 左右的值。匹配的单词越多，数字越大，因此几个单词匹配排名将产生 13 左右的相关性评分。MySQL 的相关性算法是为大表设计的，数据越多，相关性值就越有用。

总的来说，MySQL 的全文检索功能提供了一种易于实现并能提供有用结果的机制。

## 如何备份我的数据库？

数据库越大，备份其包含的数据就越令人紧张。如果你的服务器崩溃且一切都丢失了怎么办？坦率地说，MySQL 提供了两种替代方案：像 `mysqldump` 这样的命令行工具，以及用于备份表的查询语法。

以下是如何使用 `mysqldump` 从命令行导出数据库内容：

```bash
mysqldump -uharry -psecret sitepoint > sitepoint.sql
```

此命令将以用户 “harry”（`-uharry`）的身份通过密码 “secret” 登录 MySQL，并将 `sitepoint` 数据库的内容输出到名为 `sitepoint.sql` 的文件中。`sitepoint.sql` 的内容将是一系列可以在 MySQL 上运行的查询语句，也许可以使用 `mysql` 工具从命令行执行反向操作：

```bash
mysql -uharry -psecret sitepoint < sitepoint.sql
```

使用 PHP 函数 `system()`，你可以在 PHP 脚本中执行上述命令（这需要你已登录并能够从命令行执行 PHP 脚本）。以下类将所有内容整合到一个方便的 PHP 类中：

```php
<?php

class MySQLDump
{
    /**
     * 要执行的命令
     *
     * @private
     * @var string
     */
    var $cmd;

    /**
     * MySQLDump 构造函数
     *
     * @param string $dbUser MySQL 用户
     * @param string $dbPass 密码
     * @param string $dbName 数据库名称
     * @param string $dest 路径
     * @param string $zip 用于压缩的工具
     */
    public function __construct($dbUser, $dbPass, $dbName, $dest, $zip = 'gz')
    {
        $zip_util = array('gz' => 'gzip', 'bz2' => 'bzip2');

        if (array_key_exists($zip, $zip_util)) {
            $fname = $dbName . '.' . date('w') . '.sql' . ($zip == 'gz' ? '' : '.' . $zip);
            $this->cmd = 'mysqldump -u' . $dbUser . ' -p' . $dbPass . ' ' . $dbName . ' > ' . $dest . '$fname';
        } else {
            // 处理无效的 zip 类型
        }
    }

    /**
     * 执行生成的命令
     *
     * @access public
     * @return void
     */
    public function backup()
    {
        system($this->cmd, $error);

        if ($error) {
            trigger_error('备份失败：' . $error);
        }
    }
}

// 使用示例：
$dbUser = 'harry';
$dbPass = 'secret';
$dbName = 'sitepoint';
$dest = '/home/harry/backups/';
$zip = 'bz2';

$mysqlDump = new MySQLDump($dbUser, $dbPass, $dbName, $dest, $zip);
$mysqlDump->backup();

?>
```

## 如何备份我的数据库？

每周覆盖上周的备份。这应该提供足够的备份，给你留出一周的时间来发现任何严重问题，而不需要过多的磁盘空间来存储文件。

使用 ZIP 工具是可选的。如果变量 `$zip` 的值不是 `gz` 或 `bz2`，则不会进行压缩，尽管对于大型数据库来说，使用压缩工具来最大限度地减少磁盘空间显然是一个好主意。

此类旨在与 `crontab` 工具配合使用，`crontab` 是 Unix 的一个功能，允许你定期（例如，每天）执行脚本。

MySQL 提供了 `BACKUP TABLE` 和 `RESTORE TABLE` SQL 语句，允许你将表的内容复制到系统中的另一个位置。使用 `mysql` 工具，通过这种方式备份的表将保留其原始格式（不是人类可读的），但这种机制不需要访问命令行工具，因此可以通过 Web 页面执行。

这些语句的通用语法如下：

```sql
BACKUP TABLE tbl_name[, tbl_name ...]
TO /path/to/backup/directory/

RESTORE TABLE tbl_name[, tbl_name ...]
FROM /path/to/backup/directory/
```

注意，在 Windows 系统上，最好使用正斜杠指定路径（例如 `C:/backups`）。

通过将这些语句与 MySQL 提供的一些“内省”语句结合，我们可以使用在本章构建的 MySQL 类来备份数据库。首先，我们需要获取数据库中的表列表，这通过 `SHOW TABLES` 查询语法可以快速实现。

文件：`21.php`（节）

```php
<?php

// 引入 MySQL 类
require_once 'Database/MySQL.php';

$host = 'localhost'; // MySQL 服务器主机名
$dbUser = 'harry'; // MySQL 用户名
$dbPass = 'secret'; // 用户密码
$dbName = 'sitepoint'; // 数据库名称
```

点击此处订购 PHP Anthology Volume I & II 并享受 75 折优惠！

## 第 3 章：PHP 和 MySQL

```php
$db = &new MySQL($host, $dbUser, $dbPass, $dbName);

// 显示数据库中表的查询
$sql = "SHOW TABLES FROM sitepoint";

// 执行查询
$result = $db->query($sql);
```

我们还存储了此查询返回的行数，以帮助我们格式化将用于 `BACKUP` 查询的字符串。

文件：`21.php`（节）

```php
// 获取找到表数量
$numTables = $result->size();
```

接下来，我们遍历结果，构建一个用于备份的表逗号分隔列表。

文件：`21.php`（节）

```php
// 构建表名字符串
$tables = '';
$i = 1;

while ($table = $result->fetch()) {
    $tables .= $table['Tables_in_sitepoint'];

    if ($i < $numTables) {
        $tables .= ', ';
    }

    $i++;
}
```

最后，我们使用 `BACKUP TABLE` 查询语法将表复制到我们选择的目录（当然，执行此查询的脚本需要该目录的写入权限）：

文件：`21.php`（节）

```php
// 构建备份查询
$sql = "BACKUP TABLE $tables TO '/home/harryf/backup";

// 执行查询
$db->query($sql);

if (!$db->isError()) {
    echo 'Backup succeeded';
} else {
    echo 'Backup failed';
}
```

点击此处订购 PHP Anthology Volume I & II 并享受 75 折优惠！

## 如何修复损坏的表？

虽然不应该发生，但存储在 MySQL 中的数据偶尔会损坏。在某些（罕见）情况下可能会发生这种情况；Windows 特别容易受到影响，因为它没有像 Unix 系统那样健壮的文件锁定机制。在重负载下，`INSERT` 和 `UPDATE` 查询与 `SELECT` 查询一样，也可能遭受偶尔损坏。你正在使用 MyISAM 表类型（除非另有指定，否则你将使用这种类型），这是一个好消息；通常情况下，你应该能够恢复损坏表中的所有数据。

注意，这里提供的信息仅供需要帮助时的快速参考。非常值得阅读关于[灾难预防与恢复][2]的 MySQL 手册，这样你就能确切知道自己在做什么。

MySQL 提供了两个处理损坏表的重要工具，并为那些可以访问 MySQL 命令行的用户提供了实用的 SQL 语法。

首先，可以从命令行运行 `error` 工具，让你大致了解 MySQL 错误代码的含义。该工具可以在 MySQL 安装的 `bin` 子目录下找到。例如，输入 `error 145` 将告诉你：

```text
145 = 表被标记为崩溃并应修复
```

从命令行中，你可以使用 `myisamchk` 工具检查数据库文件本身：

```bash
myisamchk /path/to/mysql/data/table_name
```

使用 `myisamchk` 修复损坏的表，语法如下：

```bash
myisamchk -r /path/to/mysql/data/table_name
```

使用 SQL，你也可以通过此类查询检查并修复表：

```sql
CHECK TABLE articles;
```

以及：

```sql
REPAIR TABLE articles;
```

> [2]: http://www.mysql.com/doc/en/Disaster

有了这些，你准备好处理损坏的表了。MySQL 提供了两个处理损坏表的重要工具，并为那些可以访问 MySQL 命令行的用户提供了实用的 SQL 语法。

首先，可以从命令行运行 `error` 工具，让你大致了解 MySQL 错误代码的含义。该工具可以在 MySQL 安装的 `bin` 子目录下找到。例如，输入 `error 145` 将告诉你：

```text
145 = 表被标记为崩溃并应修复
```

从命令行中，你可以使用 `myisamchk` 工具检查数据库文件本身：

```bash
myisamchk /path/to/mysql/data/table_name
```

使用 `myisamchk` 修复损坏的表，语法如下：

```bash
myisamchk -r /path/to/mysql/data/table_name
```

使用 SQL，你也可以通过此类查询检查并修复表：

```sql
CHECK TABLE articles;
```

## 我真的需要写 SQL 吗？

开始使用 DBObject 的第一步是指向你的数据库并告诉它生成类。DataObject 会利用 MySQL 的内省自动生成，并为每个表生成一个类。

上述文件遵循 `.php` 的某些格式规则。最重要的是第一行，这是一个 `PEAR::DB DSN` 字符串，定义了连接数据库的变量。该文件既用于生成 DataObject 类，也用于执行查询。

准备就绪，我们可以使用此脚本（必须从命令行运行）来生成类。

文件：`22.php`

```php
<?php

// 构建 DataObjects 类
$_SERVER['argv'][1] = 'db_dataobject.ini';
```

## 第 3 章：PHP 和 MySQL

```php
require_once 'DB/DataObject/createTables.php';
?>
```

此脚本会自动创建访问数据库所需的类文件。以下是一个为文章（articles）开发的示例。

文件：`ExampleApps/DataObject/Articles.php`（位于 SPLIB 中）

```php
<?php

/**
 * articles 表定义
 */
require_once 'DB/DataObject.php';

class DataObject_Articles extends DB_DataObject
{
    ###START_AUTOCODE

    /* 以下代码为自动生成，请勿删除上方标签 */
    var $_table = 'articles'; // 表名
    var $article_id; // int(1) not_null primary_key auto_increment
    var $title; // string(255) not_null multiple_key
    var $intro; // blob(65535) not_null blob
    var $body; // blob(65535) not_null blob
    var $author; // string(255) not_null
    var $published; // string(1) not_null enum

    /* ZE2 兼容性技巧 */
    function clone()
    {
        return $this;
    }

    /* 获取 */
    function getStatic($k, $v = NULL)
    {
        return DB_DataObject::staticGet('DataObject_Articles', $k, $v);
    }

    /* 以上代码为自动生成，请勿删除下方标签 */
    ###END_AUTOCODE
}

?>
```

现在让我们使用这个类来访问 `articles` 表。

文件：`23.php`

```php
<?php

// 引入 DataObjects_Articles 类
```

点击此处订《The PHP Anthology Volume I & II》并享受 75 折优惠！

## 我真的需要写 SQL 吗？

```php
require_once 'ExampleApps/DataObject/Articles.php';

// 解析数据库 ini 文件
```



`$dbconfig = parse_ini_file('db_dataobject.ini', true);`

// 加载数据库设置

// （注意 PEAR 类由 `Articles.php` 加载）

```
foreach ($dbconfig as $class => $values) {

    $options = &PEAR::staticProperty($class, 'options');

    $options = $values;

}
```

// 实例化 `DataObject_Articles` 类

```
$articles = new DataObject_Articles();
```

// 为 `Author` 列分配一个使用的值

```
$articles->author = 'Kevin Yank';
```

// 执行查询

```
$articles->find();
```

```
echo 'Kevin has written the following articles:<br />';

// 遍历文章
while ($articles->Fetch()) {
    echo ' - ' . $articles->title . ' , published : ' . date('j M Y', $articles->published) . ' <br />';
}
```

首先，SQL 呢？完全没有——太棒了！`parse_ini_file` 函数由 PHP 提供（详情请见第 4 章），用于从我们的 `db_dataobject` 配置文件中获取变量。`fetch` 循环在我们实例化 `DataObject_Articles` 时，为 `DB_DataObject` 提供了所需的变量。通过为 `$articles` 对象的 `author` 属性赋值，我们为 `DataObjectArticles` 在查询数据库时准备了一个 `WHERE` 条件。查询实际上是通过调用 `find` 方法执行的（完整细节请参 `DB_DataObject` 文档），该方法转而执行了以下查询：

```sql
SELECT FROM articles WHERE author = 'Kevin Yank'
```

为了遍历结果，我们使用 `fetch` 方法。当它被调用时，`fetch` 用当前结果填充 `$articles` 对象的属性。

这允许我们再次通过属性名访问它们，例如通过 `$articles->title`。

还提供了其他方法来使查询更复杂，例如 `whereAdd` 方法：

```php
// 实例化 DataObject_Articles 类

$articles = new DataObject_Articles();

// 为 'Author' 列分配一个用于搜索的值

$articles->author = 'Kevin Yank'

// 添加 where 子句

$articles->whereAdd('published > ' . mktime(0, 0, 0, 5, 1, 2002));

// 执行查询

$articles->find();
```

这允许我们向 `WHERE` 子句中添加额外的条件：

```sql
SELECT * FROM articles

WHERE published > 1020204000 AND articles.author = 'Kevin Yank'
```



还有其他方法，如果这些方法不能满足你的需求，可以使用`query`方法执行手动编写的查询。请注意，如果你发现自己需要使用`query`方法，那么创建一个生成的`DataObject`类可能是一个好主意，并将查询封装在一个描述准确的有用方法名中。

`DB_DataObject`还能有效地处理表连接（table joins），虽然比上面的示例稍微详细一些，但与手动编写复杂的连接相比，它非常节省时间。

对`DB_DataObject`的简要介绍到此结束，但本节让你体验了它能为你做什么。巨大的优势是，使用 SQL 查询数据库要轻松得多且不易出错。此外，通过在单个类中集中对特定表的访问，有助于简化处理表结构的变化。

# 扩展阅读

- *Beginning MySQL: http://www.devshed.com/Server_Side/MySQL/Intro/*

点击此处订购《The PHP Anthology Volume 1 & II》并享受 75 折优惠！

# 关键安全与移植性设置

表 A.1 显示了与 PHP 脚本的安全性和移植性相关的最重要的 PHP 设置。

## 附录 A：PHP 配置

### 表 A.1. 关键安全与移植性设置

| 设置 | 备注 |
| --- | --- |
| `register_globals` (默认: off) | 从传入的 HTTP 请求变量（如 GET 和 POST）自动创建全局变量。出于安全和移植性考虑，强烈建议关闭此选项。更多详情请参见 http://www.php.net/register_globals。 |
| `magic_quotes_gpc` (default: off) | 自动用反斜杠转义 HTTP 请求变量中的引号，有助于防止 SQL 注入攻击。如果你知道自己在做什么，通常最好关闭此功能，并在插入数据库时自行处理这些转义工作，因为该功能可能会给你带来很多问题，而且它还会引入性能开销。请参阅第 1 章获取有关如何让你的脚本兼容此功能的信息。 |
| `call_time_pass_reference` (default: off) | 允许在调用时使用变量引用（例如`htmlentities($string)`）。为了保持代码整洁易于理解并确保移植性，请保持此功能关闭状态。 |
| `short_open_tag` (default: on) | 允许仅用`<?`而不是更长的`<?php`来启动 PHP 块。还允许使用`<=?`写表达式，这与`<?php echo`相同。虽然方便，但这些快捷方式不符合 XML 标准，并且当 PHP 处理器遇到如`<?xml version="1.0"?`这样的 XML 处理指令时可能会混乱。许多人都关闭了`short_open_tag`，因此为了最大的移植性，请在开发期间避免使用快捷方式并关闭此功能。 |
| `asp_tags` (default: off) | 允许使用 ASP 样式的标签`< ... %>`作为 PHP 和开放标签`<?php ... ?>`的替代方案。很少有人使用它，因此为了最大的移植性，最好避免使用它们，并在开发期间关闭此功能。 |

点击此处订购《PHP Anthology》第 1 和 2 卷并享受 75 折优惠！

| 设置 | 备注 |
| --- | --- |
| `error_reporting` (default: E_ALL & -E_NOTICE) | 开发时，为了获得最大的移植性，最好将其设置为`E_ALL`，这样 PHP 会通知你某些情况，例如你的代码依赖的某个`$_GET`变量已初始化。这会迫使你编写更安全且错误更少的代码，同时也确保你的代码在服务器上运行顺畅。 |
| `display_errors` (default: on) | 决定 PHP 是否向 Web 浏览器发送错误消息。在生产环境中运行应用程序，通常最好关闭此项，转而使用 PHP 的日志机制将错误捕获到文件中（例如）。 |
| `open_basedir` (default: not set) | 允许你将所有 PHP 文件操作限制在给定的目录及其之下。这是一个很好的主意，可以防止用于显示文件内容的脚本被用于访问服务器其他地方的敏感文件。 |
| `allow_url_fopen` (default: on) | 允许为函数`fopen`指定远程文件位置（例如`fopen('http://www.sitepoint.com/','r')`）。这是一个实用的工具，但对于编写得糟糕的脚本来说，也存在潜在的安全风险。如果你知道不需要它，请将其关闭。 |

### 包含与执行设置

表 A.2 显示了与包含（includes）以及你的 PHP 脚本运行状况相关的最重要的 PHP 设置。

### 表 A.2. 包含与执行设置

| 设置 | 备注 |
| --- | --- |
| `include_path` (default: '.') | 允许你在使用包含相关的命令时，指定 PHP 应该搜索的相对路径和绝对路径。确保你至少指定了当前目录（`.`），否则大多数第三方脚本将无法工作。在 Unix 系统上，目录列表用冒号（`;`）分隔，而在 Windows 上，分隔符是分号（`:`）。 |
| `auto_prepend_file` (default: not set) | PHP 将在执行任何请求脚本之前执行文件（文件）。这对于执行全站操作（如安全、日志、定义错误处理程序、移除 magic quotes 功能添加的反斜杠等）非常有用。对于你自己使用的应用程序很有用，但不适用于打算分发的代码。无法通过 `.htaccess` 文件修改 `php.ini` 设置的用户无法使用此类代码。分隔符与 `include_path` 设置相同。 |
| `auto_append_file` (default: not set) | `auto_prepend_file`的孪生节点，在请求脚本之后执行。 |
| `max_execution_time` (default: 30) | 指定在 Web 服务器上运行的 PHP 脚本允许的最大执行时间（秒）。通常，最好保持默认值，并使用`set_time_limit`函数根据每个脚本来扩展限制。值`0`表示取消对脚本执行时间的任何限制。 |
| `memory_limit` (default: 8M) | PHP 在运行时可用的内存量。通常，默认值就足够了；但在处理非常大的 XML 文档或处理图像时，你可能需要增加它。此值越大，脚本实际使用的内存就越多，服务器上运行的其他应用程序所可用的内存就越少。 |

### 错误相关设置

表 A.3 显示了与 PHP 处理错误方式相关的最重要的 PHP 设置，除了 A.1 中描述的`display_errors`和`error_reporting`。

### 表 A.3. 错误相关设置

| 设置 | 备注 |
| --- | --- |
| `post_max_size` (default: 8M) | PHP 通过 HTTP POST 接受的最大数据量（例如上传图片的表单）。 |
| `log_errors` (default: off) | 结合`error_log`（下文），允许将错误记录到文件中。对于关闭了向访问者显示错误的站点有用。 |
| `error_log` (default: not set) | 开启`log_errors`时记录错误的文件。 |
| `ignore_repeated_errors` (default: off) | 使用此项后，如果同一脚本的同一行发生相同的错误，则每次脚本执行只会报告一次。有助于防止循环中发生的错误产生巨大的日志文件。 |
| `ignore_repeated_seconds` (default: 30) | 与`ignore_repeated_errors`类似，在这种情况下它抑制整个 PHP 脚本期间相同类型的重复错误。 |
| `report_memleaks` (default: on) | 确保开启此项，特别是当你使用实验性版本或非稳定版 PHP 时，否则一旦内存耗尽可用空间可能会导致服务器崩溃。`error_reporting`必须设置为报告警告，此设置才能生效。 |

### 其他设置

表 A.4 显示了你在 PHP 配置中应该注意的其他重要设置。

### 表 A.4. 其他设置

| 设置 | 备注 |
| --- | --- |
| `session.save_path` (default: /tmp) | 如果在 Windows 系统上文件存储会话，你需要修改此设置以便 PHP 可以写入会话文件的可用目录。 |
| `session.use_cookies` (default: 1) | 使用 cookie 在客户端存储会话 ID，而不是将会话 ID 放在 URL 中（这带来的风险更大）。 |
| `extension_dir` (default: './') | 编译好的 PHP 扩展所在的路径。在 Windows 系统上，它可能像这样：`extension_dir = C:\php-4.3.2\extensions\` |
| `extension` | 仅限 Windows 系统，用于标识所有应该加载的扩展。指定的扩展应位于`extension_dir`路径（上文）。例如：`extension = php_xslt.dll` |

# 附录 B：主机选择清单

PHP，更广泛地说，Linux、Apache、MySQL 和 PHP/Perl/Python 的 LAMP 组合通过数以千计的 Web 主机提供，价格非常低廉。你可以轻松获得每月不到 10 美元、就能满足你 90% 需求的优质 Web 托管。尽管如此，并非所有的 PHP 安装都是同等的，它们在很大程度上取决于`php.ini`中定义的配置设置，以及主机商为你安装的扩展。此外，还有许多与你对环境的控制程度有关的通用问题，如果你不想以后遇到大麻烦，这些问题是非常关重要的。

以下是在支付托管服务费用之前应该调查的关键问题总结。联系潜在的提供商，让他们针对这些问题的每一点给出回复。随后，向其他了解或使用过该服务的人征求意见。在许多在线论坛中，你可以找到能够提供建议的人。但请注意，“知情者”与“无知者”的比例是严重向无知倾斜的；要挖掘技术细节，以便能够验证所给答案是否确实是有据可的。

我在这里提供的一些观点可能看起来有些极端，但一旦你经历过几次，你可能希望花钱买到价值，而不是在周六早上修理主机商在周五晚上为你制造的问题。

## 通用问题

- **要求 Linux 和 Apache (1.3)**：从性能和可靠性的角度来看，这是最好的。避免使用 Apache 2.x（它与 PHP 的配合并不完全稳定）。询问 Linux 发行版的细节。虽然 Red Hat 和 Suse 很流行，但你可能会发现使用 Debian（或者更好的，Rocky Linux）的主机对自己的工作更了如。

- **主机是否为你提供服务器的 SSH 访问权限？**

SSH 为你提供了服务器的安全连接，可以从 Linux 命令行执行任务或使用 SCP（安全复制）传输文件。避免任何允许你使用 telnet 的主机（这是通过互联网连接服务器的一种根本上不安全的方法）。对于 Windows 用户，Putty|WinSCP[2] 提供了使用 SSH 连接的安全文件传输机制。噢，千万不要用 ftp 传输文件——它的安全性和 telnet 一样。

- **主机是转销商还是他们自己维护服务器？**

如果你需要基础技术层面的帮助（例如，如果你自认为是新手），转销商可以提供巨大的价值，但他们对服务器的控制权限通常和你一样。“直接找源头”意味着当系统出现问题时，你不需要面对延迟，因为你面对的是维护服务器的人。缺点是，他们往往倾向于“宽容新手”，所以你可能会得到答案——但不是你能够听懂的答案。

- **主机在多大程度上对服务器进行了“过载”？**

许多 Web 托管公司在服务器上创建的账户超过了系统指定的最大数量。最好的指标是`uptime`命令（你需要访问权限）；它将告诉你服务器在 1、5 和 15 分钟内的负载平均值。理想情况下，服务器的负载平均值永远不应高于 1。显然，问题没有那么简单，但一旦你看到服务器的平均值超过 5，你就会开始发现你的基于 PHP 的应用程序出现明显的延迟。

- **主机商对于从命令行运行脚本和程序的策略是什么？**

MySQLDump 是一个备份数据库非常实用的工具，但如果你无法运行它，那也是很妙的。有些主机会自动杀死执行时间超过给定时间的命令行应用程序。

- **主机是否提供对 cron 的访问（允许你调度批处理作业的 Unix 工具）？**

如果是，请确保主机允许执行命令行脚本。有些主机实现的 cron 使得它通过 Web URL 执行脚本。如果相关脚本使用 MySQLDump 应用程序备份数据库，这样做就毫无用处——因为通过 Apache 执行的 PHP 脚本通常以用户身份运行，该用户将不具备完成任务所需的正确权限。

[1] http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
[2] winscp.sourceforge.net/

## PHP 相关问题

- **你是否可以在实际分配给你的服务器上看到`phpinfo`的输出？**

有些主机可能声称这是一个安全风险，但专家级主机知道，通过隐蔽来实现安全并不能替代真正的安全。对于那些懂业务并正确设置了 Linux、Apache 和防火墙的主机商来说，`phpinfo`提供的信息并不是安全风险。`phpinfo`告诉你的的是确认事实的最佳方法。

- **PHP 是否作为 Apache 模块安装（而不是 CGI 版本）？**

这提供了许多更好的性能。

- **Apache 设置`AllowOverride`是否被设置为 Options 或 All？**

这将允许你通过 `.htaccess` 文件修改`php.ini`设置。

- **PHP 是否禁用了安全模式（Safe Mode）？**

`php.ini`中的`safe_mode`选项在某种程度上是为了让 PHP 安全，防止用户执行某些任务或使用对安全敏感的函数。如果你在 PHP 中进行任何严肃的工作，安全模式将是一个巨大的麻烦。

- **检查你主机的升级策略。**

询问主机在执行升级前你会得到多少警告。检查他们是否为你提供他们所使用的`php.ini`文件副本。

- **向主机索要已扩展列表。**

- **PHP 是否可以在命令行中使用？**

如果不能，你可能需要要求访问 Perl 或 Python。

# 附录 C：安全清单

鉴于在线 PHP 应用对所有人开放，在开发过程中，安全应该是关注的问题之一，甚至是首要考虑。在某种程度上，PHP 应用开发的简易性也是其最大的弱点之一；对于那些没有意识到可能危险的新手来说，部署一个安全性像瑞士奶酪一样的应用程序是非常容易的。

确保你了解相关信息，如有任何疑问，请询问。开放 Web 应用安全项目 (OWASP)[1] 是一个专注于提高 Web 安全意识的社区，是信息的绝佳来源。永远不要从 Web 浏览器中获取任何信任。浏览器完全在你的控制之外，伪造如 HTTP referrer 等值非常容易。在表单中隐藏一个字段也很容易。

更重要的是，在处理表单时（例如），务必仔细验证数据。使用“拒绝所有，允许少量”的策略。例如，如果注册表单有一个用户名字段，只允许字母和可能可能的数字 0-9，而不是简单地拒绝特定字符。使用正则表达式将数据限制为你精确所需的内容。像 `PEAR::QuickForm` 这样的包（如你在第 9 章中看到的）提供了验证表单的内置机制，并在很大程度上帮助涵盖你可能忽略的弱点。

此外，在涉及包含文件时，要警惕这类逻辑：

```
include($_GET['page']);
```

确保你检查 `$_GET['page']` 的值是否在你代码设计包含的文件列表中。

[1] http://www.owasp.org/

## 附录 C：安全检查清单

```
$pages = array(

  'news.php', 'downloads.php', 'links.php'

);

if (in_array($_GET['page'], $pages)) {

    include $_GET['page'];

} else {

    include 'not_found.php';

}
```

如果没有此类检查，攻击者很容易使用类似下面的代码来执行其他 PHP 脚本——即你没有编写的脚本。

- **越坏的访问控制**

如果你不知道自己在做什么，该表单的基本逻辑很容易出错。例如，开发者经常使用如下逻辑在数据库中对用户名/密码组合进行比对：

```
if ($numRows != 0) {

  // 允许访问 ...

}
```




这意味着，如果用户在数据库中找到了多个匹配的项，就允许他们进入。如果你的网站存在类似命令注入漏洞等安全孔洞（见下文），这可能会为攻击者提供比你预期的多得多的权限。在认为自己考虑到位的情况下很容易出错，但实际上，该逻辑可以被轻易绕过。通常情况下，尽可能使用第三方库，如`PEAR::Auth`[2]和`PEAR::LiveUser`[3]，同时调查一些 Web 框架，如`SimpleTest`[4]，它们提供了从浏览器角度测试你网站的能力。

- 会话和 Cookie 漏洞

注意会话劫持（session hijacking）。在需要安全身份验证的站点（例如电子商务网站），请使用 SSL 为浏览器提供服务，以确保对话经过加密，且没有人在窃听。如果你通过 URL 传递会话 ID（基于 WML 的站点将这样做），请确保不要将会话 ID 放在指向远程站点的 URL 中。此外，将访问引导远程站点时，通过中间脚本进行转发，并剥离掉任何包含会话 ID 的 HTTP Referer 信息。

[2] http://pear.php.net/package/Auth
[3] http://pear.php.net/package/LiveUser
[4] http://www.lastcraft.com/simple_test.php

### 顶级安全漏洞

通常，使用 Cookie 处理会话更好。如果你在编写自己的基于 Cookie 的身份验证，请仅在 Cookie 中存储识别 ID，而不是存储用户名和密码。

### 跨站脚本 (XSS)

通过使用网站提供的合法机制，攻击者可能会在你的网站上发布内容，例如 JavaScript，导致其他用户交出他们的会话 ID，从而允许攻击者劫持他们的会话。不那么严重但同样尴尬的是，仅仅发布 HTML 来“扰乱”你页面的布局，例如过早关闭标签。使用“少即是多”的方法，或者更好的是采用一种如 BBCode（第 5 章）的独立标记语言，同时消除`strip_tags`和`htmlentities`等 HTML PHP 函数。如果你真的想允许发布 HTML，请考虑基于`PEAR::XML_HTMLSax`[5]构建过滤器（见第二卷，第 2 章）。

### 命令注入

命令注入发生在攻击者能够影响 PHP 与外部系统（如文件系统或数据库）交互的方式时。SQL 注入就是一个例子，发生在攻击者使用表单或 URL 修改数据库查询时。这在第 3 章中详细讨论过。底线是：在使用从用户那里接收的所有数据之前，对其进行转义。

### 错误处理

经验攻击者能够从你的错误消息中获取大量关于系统的重要信息。虽然这属于“安全隐晦性”范畴（这不能替代真正安全的应用程序），但对于运行中的站点，指示 PHP 将错误消息记录到文件中而不是显示在浏览器是一个很好的做法。详情见附录 A。

### 加密使用不当

首先，涉及加密时，不要自己编写实现。记住，如果是一个用于解码的算法，那么其他人（除你之外）也能够解码它。记住，严格来说，MD5 不是加密算法（即你无法通过解密 MD5 字符串来获取原始数据）；它是一种消息摘要算法。但如果你在通过 PHP 的`md5()`函数使用时不解密该值，这允许你比较两段数据的加密版本（例如存储的密码和用户输入的密码），从而避免了处理可能被攻击者解密的加密值时带来的风险。

[5] http://pear.php.net/package/XML_HTMLSax

### 管理缺陷

允许攻击者获得与你对网站相同的访问权限显然是坏事。避免 FTP 和 telnet，分别改用 SCP/SFTP 和 SSH。Linux 发行版通常预装了所需的客户端工具。对于 Windows，可以使用 `putty`[6] 进行 SSH 访问，使用 `WinSCP`[7] 进行 SCP/SFTP。FTP 和 telnet 会让你的网络暴露于嗅探。确保你的主机提供的任何 Web 管理工具仅通过 SSL 连接运行。如果你正在使用第三方软件（如 `phpBB`），请立即更改默认管理员密码，并关注潜在的安全漏洞。

### 配置与补丁

在安装 PHP 时，`php.ini-recommended` 配置文件是最佳起点，可以确保你正确配置了程序包。

如果你使用托管公司，他们应该为你处理大部分问题，例如在漏洞公布时对软件进行修补。尽管如此，自己保持更新也是值得的，可以使用 `Security Focus`[8] 和 `DMOZ`[9] 列出的其他网站。

更多信息请访问 `PHP Advisory`[10]，尽管遗憾的是该网站已不再维护。

[6] http://www.chiark.greenend.uk/~sgatham/putty/
[7] http://winscp.sourceforge.net/eng/
[8] http://www.securityfocus.com/incidents/
[9] http://dmoz.org/Computers/Mailing_Lists/
[10] http://www.phpadvisory.com/

## 附录 D：使用 PEAR

`PEAR`[1]（PHP扩展与应用程序库）是 `Stig Bakken` 的结晶，并受到了 Perl 的 `CPAN`[2] 的启发。

作为一个项目，它构思于 1999 年，并在 2003 年 1 月发布了第一个稳定版本。它有两个目标：首先，它提供了解决架构问题的 PHP 类，我们在书中已经看到。其次，在 `PECL`（PHP扩展代码）下，PEAR 为扩展提供了仓库。PEAR 最初旨在存储边缘的非标准扩展，但后来已演变为未包含核心扩展的默认仓库。在这里，我将专注于 PEAR 提供的类。

提交和维护 PEAR 仓库的都是志愿者。最初 PEAR 的第一个稳定版本数量一直在增长，并受到了整个 PHP 社区的更多关注，PHP 本身的标准方面仍有很多工作要做。如果你感到困惑，一个很好的起点是 `PHPKitchen` 的 `PEAR` 教程[3]。尽管如此，PEAR 在减少开发 PHP 应用所需的工作提供了显著价值。

但 PEAR 对你有意义吗？考虑到 `PEAR::SOAP` 在第二卷第 2 章中涵盖的功能，尝试自己编写 SOAP 实现后再编写使用它的应用程序代码显然是浪费时间。浏览包列表[4]，你会发现 PEAR 提供了许多按主题分类的类，帮助你避免重复造轮子。理解 PEAR 的重点是架构是很重要的。在其他类中，PEAR 不是脚本；你不会在那里找到应用程序；相反，你会发现可以在许多应用程序中使用的代码。同样，PEAR 开发者社区尽力维护和支持该库，相比于通过 `SourceForge`[5] 提供的项目，后者通常是个人的。

[1] http://pear.php.net/
[2] http://www.cpan.org/
[3] http://www.phpkitchen.com/staticpages/index.php?page=200304120420962
[4] http://pear.php.net/packages.php
[5] http://www.sourceforge.net/

---

## 附录 D：使用 PEAR

一旦相关人员投入时间工作，这些努力就会停止。否则，在整个库中都强调要保持某种程度的标准化。例如，所有的错误处理都应该使用 `PEAR::Error` 完成，并且代码应该使用 `PHPDoc` 标准进行文档化，这意味着如果你能在 PEAR 网站上找到 `PHPDocument`[6]（第二卷，第 6 章），你就应该能够使用它提取 API 文档。

请注意：与 Java 类库相比，包与 PEAR 之间的集成程度很少很低。这意味着在某些情况下，你将面临是使用 `PEAR::HTMLForm` 的验证功能，还是使用 `PEAR::Validate`，或者两者都用的决策。在开始之前花时间研究哪种适合你的开发是一个明智的选择，而不是直接跳进去并将 PEAR 用于应用程序的关键部分，结果后来发现它并不是解决该问题的最佳选择。

一个需要明确的重要点是，提到“PEAR”实际上可以指两个意思：整个仓库，或者 PEAR 前端（也称为包管理器），它提供了安装和升级 PEAR 包的工具。

请注意，并不是要求你使用 PEAR 管理器来安装 PEAR 包。如果你需要，可以从 PEAR 网站直接下载并手动将其提取到你的 PHP include 路径中。确保你检查了网站上列出的依赖项（这是其他包所要求的），并意识到大多数包隐式需要 PEAR “base” 包[7] 来执行错误处理等任务。

### 安装 PEAR

如今，PEAR 的基础由 PHP 分发版本身提供，但 Web 托管商通常用其默认的 PEAR 安装让客户失望，因此知道如何从零开始这样做是值得的。该过程在 Unix 和 Windows 系统之间略有不同。

第一步是确保你可以通过命令行运行 PHP 脚本。只要输入 PHP 二进制文件的完整路径，这总是可以的。对于 Unix 系统，你使用以下命令：

```
/usr/local/bin/php /home/username/scripts/my_script.php
```

对于 Windows，你将使用类似的内容：

```
c:\php\cli\php.exe c:\scripts\my_script.php
```

注意，在上面的 Windows 路径中，我们使用了 PHP 安装中 `cli`（命令行界面）子目录的可执行文件，这与 Apache 处理网页时使用的略有不同。自 4.3.0 以来，Windows 二进制发行版将 `cli` 版本的 PHP 可执行文件放在此目录。

不过，通过对系统环境变量进行一些更改，可以让 PHP 在命令行变得更容易使用。要进行深入讨论，请参见 `PHPBuilder`[9] 上的“用 PHP 脚本替换 Perl 脚本”[8]。

接下来，将浏览器指向 http://pear.php.net/go-pear，你将在那里看到一个 PHP 脚本。该脚本用于安装 PEAR 包管理器——你安装所有其他 PEAR 包所需的基础。将此下载到你的电脑（文件，另存为）并命名为 `go-pear.php`。从这里开始，你有许多选择。

将 `go-pear.php` 存储在服务器文档根目录的任何地方都将允许你作为网页运行该脚本。这种行为仍然是实验性的，尽管无法保证它一定能正常工作。如果你使用这种方法，请确保该脚本不是公开的！

更好的方法是通过命令行执行 `go-pear.php` 脚本，例如：

```
/usr/local/bin/php /home/username/pear/go-pear.php
```

或者，在 Windows 上：

```
c:\php\cli c:\pear\go-pear.php
```

这将启动一个交互式命令行界面，它将询问你关于希望如何设置“安装前缀”的问题——安装前缀是安装 PEAR（以及你安装的任何包）的目录，被称为 `$prefix`，而 `$php_dir` 是你 PHP 安装的路径（除非你另有指定，否则 `go-pear.php` 默认将与 PEAR 相关的文档放在那里）。Windows 用户知晓

[8] http://www.phpbuilder.com/columns/jayesh20021111.php3
[9] http://www.phpbuilder.com/

更改安装前缀会弹出一个 Windows “浏览”对话框，通过你可以指定所需的目录。

一旦安装选项符合你的要求，`go-pear.php` 脚本将连接到 PEAR 网站，并下载设置管理器所需的所有包（它还会询问你是否需要额外的包，这些包非常值得拥有）。包将安装在你指定的作为安装前缀的目录的子目录 `pear` 中（因此，在上面的示例中，你将得到 `c:\pear/home/username/pear/pear`）。

最后，如果你登录，`go-pear.php` 安装程序将尝试修改你 `php.ini` 中的 `include_path`。要手动执行此操作，假设你使用上述目录，你需要指定：

```
include_path = ":/home/username/pear/pear"
```

对于 Windows 用户，路径是：

```
include_path = "c:\pear"
```

最后，为了从命令行使用 PEAR 命令，你需要设置系统路径。在 Windows 上通过系统控制面板（高级选项卡，点击环境变量），并将 `c:\pear` 添加到 `PATH` 变量。

在 Unix 系统上，在 `.profile` 中添加以下内容：

```
export PATH=$PATH:pear
```

### PEAR 包管理器

假设你正确设置了 PEAR，现在可以使用包管理器的命令行界面来安装包。例如，从命令行输入：

```
pear install HTML_Common
```

这将从 PEAR 网站安装 `HTML_Common` 包。命令行中的包名与网站上相同。

PEAR 包管理器使用 `XML_RPC` 与 PEAR 网站通信。如果你位于代理服务器或防火墙后，你需要告诉 PEAR 代理服务器的域名：

```
pear config-set http_proxy.your-isp.com
```

在后期取消该变量，只需使用：

```
pear config-set http_proxy ""
```

现在将 `QuickForm` 添加到已安装的 PEAR 包，你只需要输入：

```
pear install HTML_QuickForm
```

如果在安装后发布了另一个版本的 `QuickForm`，可以使用以下命令升级：

```
pear upgrade HTML_QuickForm
```

如果由于某些原因，你以后决定不再需要 `QuickForm`，可以使用以下命令将其删除：

```
pear uninstall HTML_QuickForm
```

要查看所有 PEAR 命令列表，只需输入 `pear`。

现在，如果你不喜欢命令行，PEAR 还有一个（实验性的）基于 Web 的前端（还有一个 PHP-GTK 前端，但这超出了讨论范围）。要使用它，你首先需要从命令行安装它。

---

## 附录 D：使用 PEAR

（注意，如果你通过 Web 服务器执行了 `go-pear.php`，则也安装了 Web 端前端）。输入以下命令：

```
pear install Net UserAgent_Detect
pear install Pager
pear install HTML_Template_IT
pear install PEAR_Frontend_Web
```

请注意前三个包是 `PEAR_Frontend_Web` 必需的。完成后，你可以使用以下简单脚本从 Web 服务器上启动前端：

```php
<?php
// 如果未设置包含路径，则此项可选
# ini_set('include_path', 'c:\htdocs\PEAR');
require_once 'PEAR.php';
// 对于 Windows 用户
# $user_config = 'c:\windows\pear.ini';
// 对于 Unix 用户
$user_config = '/home/username/pear/pear/PEAR/pear.conf';
$useHTML = TRUE; // 旧版浏览器请关闭
require_once 'PEAR/WebInstaller.php';
?>



### 手动安装包

可以手动安装包（尽管这涉及更多工作），但在这样做时，务必仔细观察包含路径（include paths）。首先，创建一个作为你安装的所有 PEAR 类基础的目录。该目录必须在你的包含路径中。接下来，安装主 PEAR 包[11]——下载最新稳定版本并将其解压到你创建的目录，使得`PEAR.php`位于该目录的根目录下。

安装更多包可以以大致相同的方式完成，但你需要小心解压到哪个目录。例如，查看`PEAR::DB`，主文件`DB.php`与`PEAR.php`文件并列位于 PEAR 类目录下，而其他与`PEAR::DB`相关的文件则位于子目录。最好的检查方法是查看每个 PEAR 包附带的`package.xml`文件。

> [11] http://pear.php.net/package/PEAR

该文件包含一个名为`filelist`的元素，列出了包中包含的所有文件以及它们应该安装的位置。对于每个文件，检查`baseinstalldir`属性，如果指定了该属性，它会告诉文件相对于 PEAR 类根目录应该放置的位置。`name`属性指定了相对于`baseinstalldir`（如果没有`baseinstalldir`属性，则直接相对于 PEAR 类根目录）的每个文件应放置的路径和文件名。

# 索引

本索引涵盖了《PHP 精要：面向对象的 PHP 解决方案》的两卷。另一卷中的页码引用以数字和*斜体*开头（例如，123 指第一卷的第 23 页）。

- alpha 通道混合 (alpha blending), 223
- 备用内容类型 (alternative content types), II-169
- Apache, 308, 310
- API 文档, II-xiii, II-283 生成, II-291 读取, II-287
- SQL 语句中的单引号转义（参见魔术引号 magic quotes）（参见 SQL 语句中的引号 quotes in SQL statements）
- 应用程序编程接口 (APIs), 25, 35, 78
- 应用程序编程接口 (APIs)

## 符号

- `$FILES`数组, 280
- `GLOBALS`数组, II-91
- `$this`变量, 31, 37, II-97
- `%` (通配符), 95
- `&` (引用)运算符, 42, 69, II-124 (参见引用 references)
- `->` (箭头)运算符, 32
- `=` (字符串拼接)运算符, II-309
- 前向代理文件 (forward files), 248
- `htacces`文件, 16, 18, 20, 118, 128, 204, 311, 322, II-72, II-81, II-229
- `::`运算符, 29
- `=` (赋值)运算符, II-309
- `@` (错误抑制)运算符, 163, 322, 224
- `@doc`标签, II-285, II-293
- `__clone_method`, 448
- 应用程序, 314
- 归档 (参见压缩文件)
- 参数, 5
- 数组 指针, II-324
- 数组, 256
- 转换为字符串, 151
- 从字符串创建, 150
- 字符串作为数组, 152
- ASP 标签 (`%%`), 18
- `asp_tags`指令, 18
- 认证 (参见访问控制)
- 认证标头 (参见 HTTP 认证)
- 自动登录, II-232
- 抽象类, 60, II-84
- 验收, II-298
- 访问控制, II-1, II-13, II-21 (参见方法 methods) (参见权限 permissions)
- 安全问题, II-1, II-24
- 相接列表模型, 288
- 聚合, 56, 59
- 别名 (参见 SELECT 查询)
- `allow_call_time_pass_reference`指令, 20, 47,
- 自动备份 MySQL, 98
- 自动备份 TABLE 查询, 101, 102
- `auto_append_file`指令, 204
- `AUTO_INCREMENT`列, 94
- `auto_prepend_file`指令, 203, II-72, II-260
- 自动化测试 (参见单元测试 unit testing)
- AWStats, II-225
- 备份 MySQL 数据库
- 坏词过滤器 (坏词 bad words)
- 条形图 (参见图表 graphs)
- base64 编码, II-6
- BBCode, 153
- Windows 中的二进制文件读取, 321
- 位运算, 321
- 黑盒测试, II-299
- 面包屑 (参见面包屑导航 crumb navigation)
- 缓冲查询 (参见未缓冲查询)
- 缓冲 (参见输出缓冲 output buffering)
- bzip2, 100
- 分块缓冲 (参见输出缓冲 chunked buffering)
- 类声明, 28
- 类作用域 (参见 scope)
- 类, 25, 26, 29, 154 (参见类中的输出 output in classes)
- 点击路径分析, II-223, II-225, II-238
- 代码归档, II-xii, II-vii
- 代码懒加载包含, II-275
- 引号, II-276
- 引用, II-276
- SQL 查询, II-275
- 集合, II-323
- 组合, 58, 59, II-158
- 压缩文件
- 缓存, 202, 293, II-156, II-175, II-241 (参见模板 template)
- 分块, II-248, II-255
- 客户端, II-242, II-262
- 下载, II-244
- 函数调用, II-260
- 防止, II-243
- 安全问题, II-256
- 服务端, II-242, II-247, II-254
- Web 服务, II-260
- 日历, 190
- 每日计划, 198
- 月中的天数, 195
- 年中的月份, 194
- 调用时引用传递, 20, 47
- 回调函数, 326, II-87, II-90, II-93
- 级联构造函数, 52
- 过滤坏词, 157
- 图表 (参见图表 graphs)
- CHECK TABLE 查询, 103
- 子类, 48 (参见 PEAR, `PEAR::Archive_Tar`)
- 创建, 138
- 提取, 139
- 具体类, 60
- 条件 GET, II-264
- 配置信息, 17
- 存储文件, 127
- 常量, II-13, II-28
- 构造函数, 31
- 上下文菜单, 292, 297
- Cookie, II-5, II-214, II-32
- 会话 sessions, II-32
- 损坏数据库，修复 MySQL
- COUNT, 205, 206
- cronab, 110
- 跨站脚本 (XSS) 攻击, 148, 153, 158
- 自定义错误处理器, 159
- 自定义页面, 333
- 自定义标签, II-285, II-293
- 自定义方法, 52
- 自定义字符串, II-28
- 自定义 for, II-23
- 自定义 in, II-27
- 自定义 de, II-30
- 自定义 as, II-31
- 自定义 a, II-32
- 自定义 de, II-34
- 自定义 a, II-35
- 自定义 de, II-37
- 自定义 de, II-38
- 自定义 a, II-39
- 自定义 de, II-40
- 自定义 a, II-41
- 自定义 de, II-42
- 自定义 a, II-43
- 自定义 de, II-44
- 自定义 a, II-45
- 自定义 de, II-46
- 自定义 a, II-47
- 自定义 de, II-48
- 自定义 a, II-49
- 自定义 de, II-50
- 自定义 a, II-51
- 自定义 de, II-52
- 自定义 a, II-53
- 自定义 de, II-54
- 自定义 a, II-55
- 自定义 de, II-56
- 自定义 a, II-57
- 自定义 de, II-58
- 自定义 a, II-59
- 自定义 de, II-60
- 自定义 a, II-61
- 自定义 de, II-62
- 自定义 a, II-63
- 自定义 de, II-64
- 自定义 a, II-65
- 自定义 de, II-66
- 自定义 a, II-67
- 自定义 de, II-68
- 自定义 a, II-69
- 自定义 de, II-70
- 自定义 a, II-71
- 自定义 de, II-72
- 自定义 a, II-73
- 自定义 de, II-74
- 自定义 a, II-75
- 自定义 de, II-76
- 自定义 a, II-77
- 自定义 de, II-78
- 自定义 a, II-79
- 自定义 de, II-80
- 自定义 a, II-81
- 自定义 de, II-82
- 自定义 a, II-83
- 自定义 de, II-84
- 自定义 a, II-85
- 自定义 de, II-86
- 自定义 a, II-87
- 自定义 de, II-88
- 自定义 a, II-89
- 自定义 de, II-90
- 自定义 a, II-91
- 自定义 de, II-92
- 自定义 a, II-93
- 自定义 de, II-94
- 自定义 a, II-95
- 自定义 de, II-96
- 自定义 a, II-97
- 自定义 de, II-98
- 自定义 a, II-99
- 自定义 de, II-100
- 自定义 a, II-101
- 自定义 de, II-102
- 自定义 a, II-103
- 自定义 de, II-104
- 自定义 a, II-105
- 自定义 de, II-106
- 自定义 a, II-107
- 自定义 de, II-108
- 自定义 a, II-109
- 自定义 de, II-110
- 自定义 a, II-111
- 自定义 de, II-112
- 自定义 a, II-113
- 自定义 de, II-114
- 自定义 a, II-115
- 自定义 de, II-116
- 自定义 a, II-117
- 自定义 de, II-118
- 自定义 a, II-119
- 自定义 de, II-120
- 自定义 a, II-121
- 自定义 de, II-122
- 自定义 a, II-123
- 自定义 de, II-124
- 自定义 a, II-125
- 自定义 de, II-126
- 自定义 a, II-127
- 自定义 de, II-128
- 自定义 a, II-129
- 自定义 de, II-130
- 自定义 a, II-131
- 自定义 de, II-132
- 自定义 a, II-133
- 自定义 de, II-134
- 自定义 a, II-135
- 自定义 de, II-136
- 自定义 a, II-137
- 自定义 de, II-138
- 自定义 a, II-139
- 自定义 de, II-140
- 自定义 a, II-141
- 自定义 de, II-142
- 自定义 a, II-143
- 自定义 de, II-144
- 自定义 a, II-145
- 自定义 de, II-146
- 自定义 a, II-147
- 自定义 de, II-148
- 自定义 a, II-149
- 自定义 de, II-150
- 自定义 a, II-151
- 自定义 de, II-152
- 自定义 a, II-153
- 自定义 de, II-154
- 自定义 a, II-155
- 自定义 de, II-156
- 自定义 a, II-157
- 自定义 de, II-158
- 自定义 a, II-159
- 自定义 de, II-160
- 自定义 a, II-161
- 自定义 de, II-162
- 自定义 a, II-163
- 自定义 de, II-164
- 自定义 a, II-165
- 自定义 de, II-166
- 自定义 a, II-167
- 自定义 de, II-168
- 自定义 a, II-169
- 自定义 de, II-170
- 自定义 a, II-171
- 自定义 de, II-172
- 自定义 a, II-173
- 自定义 de, II-174
- 自定义 a, II-175
- 自定义 de, II-176
- 自定义 a, II-177
- 自定义 de, II-178
- 自定义 a, II-179
- 自定义 de, II-180
- 自定义 a, II-181
- 自定义 de, II-182
- 自定义 a, II-183
- 自定义 de, II-184
- 自定义 a, II-185
- 自定义 de, II-186
- 自定义 a, II-187
- 自定义 de, II-188
- 自定义 a, II-189
- 自定义 de, II-190
- 自定义 a, II-191
- 自定义 de, II-192
- 自定义 a, II-193
- 自定义 de, II-194
- 自定义 a, II-195
- 自定义 de, II-196
- 自定义 a, II-197
- 自定义 de, II-198
- 自定义 a, II-199
- 自定义 de, II-200
- 自定义 a, II-201
- 自定义 de, II-202
- 自定义 a, II-203
- 自定义 de, II-204
- 自定义 a, II-205
- 自定义 de, II-206
- 自定义 a, II-207
- 自定义 de, II-208
- 自定义 a, II-209
- 自定义 de, II-210
- 自定义 a, II-211
- 自定义 de, II-212
- 自定义 a, II-213
- 自定义 de, II-214
- 自定义 a, II-215
- 自定义 de, II-216
- 自定义 a, II-217
- 自定义 de, II-218
- 自定义 a, II-219
- 自定义 de, II-220
- 自定义 a, II-221
- 自定义 de, II-222
- 自定义 a, II-223
- 自定义 de, II-224
- 自定义 a, II-225
- 自定义 de, II-226
- 自定义 a, II-227
- 自定义 de, II-228
- 自定义 a, II-229
- 自定义 de, II-230
- 自定义 a, II-231
- 自定义 de, II-232
- 自定义 a, II-233
- 自定义 de, II-234
- 自定义 a, II-235
- 自定义 de, II-236
- 自定义 a, II-237
- 自定义 de, II-238
- 自定义 a, II-239
- 自定义 de, II-240
- 自定义 a, II-241
- 自定义 de, II-242
- 自定义 a, II-243
- 自定义 de, II-244
- 自定义 a, II-245
- 自定义 de, II-246
- 自定义 a, II-247
- 自定义 de, II-248
- 自定义 a, II-249
- 自定义 de, II-250
- 自定义 a, II-251
- 自定义 de, II-252
- 自定义 a, II-253
- 自定义 de, II-254
- 自定义 a, II-255
- 自定义 de, II-256
- 自定义 a, II-257
- 自定义 de, II-258
- 自定义 a, II-259
- 自定义 de, II-260
- 自定义 a, II-261
- 自定义 de, II-262
- 自定义 a, II-263
- 自定义 de, II-264
- 自定义 a, II-265
- 自定义 de, II-266
- 自定义 a, II-267
- 自定义 de, II-268
- 自定义 a, II-269
- 自定义 de, II-270
- 自定义 a, II-271
- 自定义 de, II-272
- 自定义 a, II-273
- 自定义 de, II-274
- 自定义 a, II-275
- 自定义 de, II-276
- 自定义 a, II-277
- 自定义 de, II-278
- 自定义 a, II-279
- 自定义 de, II-280
- 自定义 a, II-281
- 自定义 de, II-282
- 自定义 a, II-283
- 自定义 de, II-284
- 自定义 a, II-285
- 自定义 de, II-286
- 自定义 a, II-287
- 自定义 de, II-288
- 自定义 a, II-289
- 自定义 de, II-290
- 自定义 a, II-291
- 自定义 de, II-292
- 自定义 a, II-293
- 自定义 de, II-294
- 自定义 a, II-295
- 自定义 de, II-296
- 自定义 a, II-297
- 自定义 de, II-298
- 自定义 a, II-299
- 自定义 de, II-300
- 自定义 a, II-301
- 自定义 de, II-302
- 自定义 a, II-303
- 自定义 de, II-304
- 自定义 a, II-305
- 自定义 de, II-306
- 自定义 a, II-307
- 自定义 de, II-308
- 自定义 a, II-309
- 自定义 de, II-310
- 自定义 a, II-311
- 自定义 de, II-312
- 自定义 a, II-313
- 自定义 de, II-314
- 自定义 a, II-315
- 自定义 de, II-316
- 自定义 a, II-317
- 自定义 de, II-318
- 自定义 a, II-319
- 自定义 de, II-320
- 自定义 a, II-321
- 自定义 de, II-322
- 自定义 a, II-323
- 自定义 de, II-324
- 自定义 a, II-325
- 自定义 de, II-326
- 自定义 a, II-327
- 自定义 de, II-328
- 自定义 a, II-329
- 自定义 de, II-330
- 自定义 a, II-331
- 自定义 de, II-332
- 自定义 a, II-333
- 自定义 de, II-334

FTP（参见文件传输协议 (FTP)）HTTP 身份验证, II-3, II-5,
全文搜索, 96, II-280 II-6

函数引用, 4
函数作用域（参见 scope）
函数
（另参见参数）
（另参见 PHP 函数）
（另参见返回值）
签名, 5, II-286
HTTP 请求头, 135, 288, II-175, II-215,
II-242, II-243, II-262
以及输出缓冲, II-246
授权, II-6
缓存控制 (`cache-control`), II-243, II-263
内容处置 (`content-disposition`), 136, II-244
内容长度, 136
内容类型, 130, 217, II-201
`etag`, II-263

# G

- GD 图像库, 209, 225
GET（参见 HTTP 请求方法）
GIF 文件
- 客户端问题, 210
- `global`关键字, 275
- 全局作用域（参见 scope）
- 全局变量（参见超全局变量）
- 图形, 225
- 柱状图, 226
- 饼图, 228
- 灰盒测试, II-299
- 组（参见用户组）
- gzip, 100
- GZIP 文件（参见压缩文件）
过期 (`expires`), II-243, II-264
- `if-modified`, II-263, II-264, II-266
- `last-modified`, II-175, II-243, II-263, II-264, II-266
- `location`, II-20, II-234
- `pragma`, II-243
- `referrer`, II-10
- 何时, II-7
- `www-authenticate`, II-5
- HTTP 请求头, II-4
- HTTP 请求方法, II-268, II-163
- HTTP 响应处理器, II-4, II-9
- `httpd.conf`, 312
- hylink URL 编码, 143

# I

- HAWAWK, II-208, II-289
HDML, II-208
heredoc 语法, 27
分层数据, 288, 289
分层菜单（参见树形菜单）
HTML
- 转换为 PDF, II-177
- 于邮件中（参见 email, HTML）
- 解析, II-81, II-177
HTML 标签
- 替换为 BBCode, 153
- 从文本中剥离, 147, 163
HTML2FO, II-200
- `if`语句, 9, 688, 277, II-132, II-148, II-195, II-271, II-282, II-334
- `ignore_repeated_errors`设备, 333, 383
图像
- 获取尺寸, 212
- 获取类型, 214
- 文本叠加, II-240
- 基于调色板的, 213
- 防止“热链” (hot linking), 230
- 重采样, 213
- 调整大小, 213
- 按缩放, 214
- 真彩, 213
- 水水印, 223
- `include`, 12, 15, 69（另参见 require）
包含文件（参见 includes）
`include_once`, 12, 14（另参见 `_once`）
`include_path`方向, 16, II-171
索引, 12, 15, 27（参见代码优化, 懒加载包含）（另参见 `include_path`）
- 跨目录, 15
- 入站邮件（参见 email, receiving）
- 索引（参见数据库索引）
继承, 48, 52, 190, 264, II-84
- 深层结构, 55
- `.ini`文件（参见在文件中存储配置信息）
- INSERT 查询, 80, 81, 96
- 影响行数, 93
- 获取新 ID, 94
- 实例（参见实例化）
- 实例化, 30
- 接口, 60, II-353（另参见应用程序接口 (APIs)）
- 懒获取, II-69
- LIKE 运算符, 95
- LIMIT 子句, 89, 91, 259, II-280
换行符
- 在 HTML 中保留, 146
- 链接标识符, II-68
- 链接 URL（参见 URL 编码）
HttpHeaders, II-262
- 日志错误（参见 logging）
- 逻辑错误, 11, 319
- 查找表, II-61

# M

- 魔法引用 (magic quotes), 19, 84, 269, II-17,（另参见 SQL 语句中的 quotes）
- `magic_quotes_pc`设备, 19, 84, 85,（另参见魔法引用）
- 邮件列表（参见 email, mailing lists）
- 最大上传大小, 280
- MD5 摘要, II-16
- 成员函数（参见方法）
- 成员变量, 31
- 访问控制, II-286
- 元标签, II-242, II-243
- 过期 (`expires`), II-243
- 问题, II-243
- 方法, 28（另参见静态方法）
- 访问控制, II-286
- 访问成员变量, 32
- 调用其他方法, 37
- 签名, II-286
- IP 地址, II-24, II-224,
- 迭代器, 296, II-98, II-108, II-323, II-338
- JavaScript, II-10
- 图形库, 225
- 语言过滤器（参见 bad words）
- 分层设计（参见 N-Tier design）
- MIME（参见 Multipurpose Mail Extensions）
- 模拟对象, II-306
- `mod_rewrite`, 231, 312,
- Mozilla, II-79, II-215
- Multipurpose Mail Extensions (MIME), 210
- 类型, 211, 215, 216, 239, 284（参见 `application/mozilla.xml`）
- `image/bmp`, 211
- `image/jpeg`, 211
- `image/png`, 211
- `image/xml+svg`, 211
- `text/html`, 211
- `new`关键字, 33
- 新行（参见 line breaks）
- 通知, 321, 323, 324, 325
- 后缀, 188
- SOAP, II-157

# O

- 面向对象编程, 21, 23, II-31
- 对象, 25, 29
- 性能问题, II-271
- 代码优化, II-269
- for 循环, II-274
- ORDER BY 子句, 256
- 输出缓冲, 333, II-245, II-247, 248（另参见 caching, chunked）
- 嵌套, II-254
- 类中的输出, 33
- 覆盖, 50
- 调用重写的方法, 55
- MySQL, 17, 24, 66, 66, 78, 290, II-2, II-254, II-279, II-343（另参见 unbuffered queries）
- 备份（参见 backing up MySQL）
- 连接, 67, 69
- 显示数据, 255
- 获取数据, 73, 75
- 插入数据行, 80
- 存储日期, 172
- 更新数据行, 80
MySQL 列类型
DATE, 174
DATETIME, 174
TIME, 174
MySQL 函数
COUNT, 90, 260
DATE_FORMAT, 178
UTC_TIMESTAMP, 178
MySQL 手册, 103
MySQL 时间戳, 174, 177
`mysqldump`, 98, 100, 101

# N

- N-Tier 设计, II-iii, II-200, II-277
- 命名空间（参见 XML namespaces）
- 导航系统, 288
- 嵌套缓冲区（参见 output buffering, nested）
- 嵌套集合 (nested sets), 288

# P

- 数据包错误 (packet sinners), II-1
- 分页结果, 259
- 参数（参见 arguments）
- 父类, 49
- 调用类的方法, 51
- 父类关键字, 51
- 解析错误, 9
- 引用传递, 42（另参见 references）
- 按值传递, 42
- 密码
- 修改, II-55
- 生成, II-51
- 获取, II-66
- 暂停脚本执行, 247, II-24
PDF（参见便携文档格式 (PDF)）
PEAR, ix, 16, 23, 253（另参见 phpOpenTracker）
`Auth_HTTP`, II-8
`PEAR::Archive_Tar`, 138
`PEAR::Cache`, II-261
`PEAR::Cache_Lite`, II-156, II-254, II-27, II-259, II-260, II-264
`PEAR::DB`, 89, 105, II-262, II-280, II-343
`PEAR::DB_DataObject`, 89, 104
`PEAR::Error`, 331
`PEAR::File`, 118, 119
`PEAR::HTML_Quick`, 249, II-22, II-26, II-37, II-48, II-55,
`PEAR::HTML_Table`, 201, 255
`PEAR::Tree`, 304
`PEAR::Mail_Mime`, 247, 249
`PEAR::mailparse`, 249
`PEAR::NET_FTP`, II-133
`PEAR::Pager_Sliding`, II-263
`PEAR::PHP`, II-301
`PEAR::SOAP`, II-157
`PEAR::Tree`, II-288
`PEAR::Validate`, II-159
`PEAR::XML`, II-102
`PEAR::XML_pdf`, II-200
`PEAR::XML_Sax`, II-81
`PEAR::XML_html`, II-177
`PEAR::XML_dom`, II-102
`PEAR::XML_Filters`, II-187
`PEAR::XML_Tree`, II-238

# 索引

- 和 IIS, 203
- `rawurdecode`, 144
- `rawurlencode`, 144
- `readdr`, 123
- `readfile`, 115, II-17, 227
- `session_register`, II-11
- `session_start`, II-7, II-9, II-11, II-246
- `session_unregister`, II-11
- `set_cookie`, II-246
- `set_error_handler`, 326, 328
- `set_time_limit`, 132, 207, 247
- `sleep`, 24, II-24
- `printf`, 152
- `str_replace`, 150
- `strip_tags`, 118, 147, 153, 156, 163, 167, II-210
- `striplashes`, 19, 84
- `strpos`, 5, 149
- `strtime`, 266
- `substr`, 122
- `system`, 98, 138
- `time`, 176, 202, 203
- `trigger_error`, 79, 320, 324, 325, II-97
- `trim`, 151
- `urldecode`, 144
- `urldecodeencode`, 144
- `warning`, 324
- `wordarray`, 149
- `xml_parse_into_struct`, II-87, II-88
- `xml_parser_create`, II-87
- `xml_parser_free`, II-88
- `xml_parser_set_option`, II-87
- `xml_set_character_handler`, II-93
- `xml_element_handler`, II-93
- `xml_element_object`, II-97, II-101
- `xslt_create`, II-137
- `xslt_errno`, II-130
- `xslt_error`, II-137
- `xslt_process`, II-137

- PHP 许可证, 154
- PHP 手手册, 2
- 搜索, 4
- 快捷键, 5
- PHP 源代码
    - 在线显示, 125
    - 安全问题, 125
    - `php.ini`, 33, 11, 16, 18, 20, 47, 80, 105, 125, 228, 203, 204, 205, 226, 227, 238, 280, 321, 332, II-72, II-81, II-82, II-260
- PHPDoc, II-284
- PHPDocument, 160
- phpDocument, II-293
- PHPMailer, 238, 243, 245, II-26, II-48, II-287
- phpOpenTracker, II-221, II-227, II-234
- API, II-231
- 安装, II-228
- 搜索引擎插件, II-236
- PHPSESSID 变量, II-214
- PHPSiff, II-222
- PHPUnit, II-300
- 饼图（参见图表，饼图）
- PNG（参见便携网络图形 (PNG)）
- 点, II-172
- 多态, 35, 60, 63
- 可携式文档格式 (PDF), II-69
    - 来自 HTML, II-177
    - 生成, II-176, II-196
    - 页面, II-173
    - 渲染, II-169
- 便携网络图形 (PNG), 210
- 可移植 PHP 代码, 16
- POST（参见 HTTP 请求方法）
- `post_max_size`指令, 280
- PostgreSQL, 66, 78, II-343
- 打印语句, II-245
- 私有方法, 39

点击此处订购《PHP Anthology》第一卷和第二卷并享受 75 折优惠！

- 过程化编程, 23
- 处理指令（参见 XML 处理指令）
- 代理服务器, II-224
- 伪 cron, 205
    - （参见 cron）
- 公有方法, 39
    - （也参见 `include_once`）
- 保留字符, 144
- 资源标识符, 74
- RESTORE TABLE 查询, 101
- 结果分页器（参见分页结果）
- 返回命令
    - 在构造函数中, 31
    - 返回值, 5
    - 构造函数返回, 31
    - 可用代码, 20, 23
- 丰富客户端, II-215
- RLIKE 运算符, 96
- 机器人（参见矢量统计，不包括搜索引擎）
- RSS, II-79, II-85, II-102
    - 聚合, II-122
    - 生成, II-114
    - 验证, II-122
- RTFM, 2
    - （也参见手册）

# Q

- QuickForm（参见 PEAR, `PEAR:HTMLForm`）
- 引号（参见代码优化，引号）
- SQL 语句中的引号, 84

# R

- ROS PDF, II-270
- 原始数据, II-226
- RDF（参见 RSS）
- 领域, II-6
- 重定向, II-20
    - （也参见 HTTP 头部，位置）
- 重构, 28
- 引用计数, 48
- 引用, 20, 39, II-276
    - （也参见引用传递）
- 使用 PHP 优化性能, 47
- 从函数/方法转换, 46
- 到新对象, 46
- `register_globals`指令, 18, II-11, II-18
- 注册用户（参见注册）
- 正则表达式, 153, 158, II-44, II-340
- REPAIR TABLE 查询, 103
- 修复数据库, 103
- `require`, 12
- `require_once`, 12, 14, 17, II-276, II-283
    - （也参见 include）

# S

- SAX（参见 API for XML）
- 矢量图形 (SVG), II-169, II-200
- 使用 PHP 渲染, II-205
- 范围, 34
- 脚本执行时间（参见计时）
- 搜索引擎友好, 307
- 搜索引擎查询, II-236
- 搜索并替换字符串, 149
- 搜索 MySQL 数据库, 95
- 安全套层 (SSL), II-1
- 安全, 3
- SELECT 查询, 80
- 返回行计数, 89, 92
- 使用 PHP, 89
- 优化, II-275
- 搜索, 95
- 排序结果, 256
- 语义错误, 10, 319
- `sendmail`, 237
- session 变量, II-45
- `session.save_path`指令, II-10, II-72
- sessions, II-8, II-11, II-12, II-55, II-154, II-214
    - （也参见自定义处理器）
    - （也参见在线跟踪）
- 在多个服务器, II-280
- 安全问题, II-9, 57
- 在 MySQL 中存储, II-71, II-73
- 与 cookies, II-232
- 短标签 (`<?`), II-18, 81
- `short_open_tag`指令, 18, 201
- Simple API for XML (SAX), II-63, II-82, II-87, II-88, II-110, II-177
- Simple Mail Transfer Protocol (SMTP), 237
- SQL 注入攻击, 275
- SQL 注入攻击, 19, 20, 81, 86, II-144
- 独立 PHP 脚本, 249
- 标准输入, 249
- 静态方法, 29, 159
- stdClass, II-100
- 字符串函数, 149
    - （也参见 PHP 函数）
- 字符串
    - 转换为数组, 150
    - 从数组创建, 151
    - 视为数组, 152
    - 修剪空白， 151
    - 写入格式化值到 152
- 结构化查询语言 (SQL), 73, II-134
    - （也参见 DELETE 查询）
    - （也参见 INSERT 查询）
    - （也参见 SQL 语句中的引号）
    - （也参见 SELECT 查询）
    - （也参见 UPDATE 查询）
    - （也参见 SQL 查询中的变量）
- 自动生成, 104
- 从 XML 生成, II-138
- 解决问题, 78
- 子类（参见子类）
- 超类（参见父类）
- 全局变量, 18
- SVG（参见矢量图形 (SVG)）
- `switch`语句, 88, 256, 327, II-58, II-60, II-89, II-130, II-322, II-334
- 语法错误, 9
- 语法高亮（参见 PHP 源代码，在线显示）
- 系统集成测试, II-298
- 对象访问协议（参见 SOAP）
- SimpleTest, II-301
- 隐藏页码, 263
- SMTP（参见 Simple Mail Transfer Protocol (SMTP))
- SOAP, II-xiii, II-141, II-150, II-226
    - （也参见 WSDL）
    - （也参见 XML-RPC）
    - 构建客户端, II-152, II-164
    - 构建服务器, II-157
    - 与 XML-RPC, II-142
- 源代码（参见 PHP 源代码）
- 特殊字符, 144, 145, 156
    - （也参见保留字符）
    - （也参见不安全字符）
- 蜘蛛（参见访问统计，不包括搜索引擎）

# T

- 表关系, 66, 94
- 表
    - 交替行, PHP, 257
    - 使用 PHP 生成, 255
- TAR 文件（参见压缩文件）
- 模板缓存, II-245
- 文本内容
    - 在 HTML 文档中, 143
    - 缩略图创建, 211, 214
    - 时间限制（参见执行限制）
    - 时区, 202
    - 时间戳, 172
    - （也参见 Unix 时间戳）
    - 计时 PHP 脚本, 204
- 分词器扩展, 99
- 标记 (tokens), 1
- 树, 289, 301
- `try-catch`语句, 320
- 用户组, II-61
- 用户注册, II-25, II-37
- 提交的数据, 159, II-335
- `var`命令, 1
- 变量, 40
    - （也参见值传递）
- 输出格式化, 152
- 在 SQL 查询中, 87
- 视图, 315, II-231
- 退出链接, II-234
- 收集, II-225
- 日志, II-226
- 报告, II-238
- 返回访问者, II-232
- 统一建模语言 (UML), 26, 38, 59, 63, 190, II-84, II-322, II-340, II-351
- 从 II-293 生成
- 单元测试, 11, II-xii, II-298, II-300
- Unix 时间戳, 173, 175, II-186
- 生成, 176
- 在 MySQL 中存储, II-174
- 不安全字符, 144
- UPDATE 查询, 81
- 影响行数, 93
- WHERE 子句, 81
- `upload_max_files`指令, 280
- URL 编码, 144
- URL 重写（参见 `mod_rewrite`）
- URLs（参见搜索引擎友好）
- 设计, 314
- 用户代理字符串, II-223

# W

- WAP（参见 Web Application Protocol (WAP))
- 警告, 320, 324, 325
- 水印, 223
- Web 错误, II-230
- Web 服务, II-xii, II-79, II-141, II-150, II-202
- 缓存, II-260
- 消费, II-150
- 部署, II-150
- 安全问题, II-165
- Web 服务描述语言（参见 WSDL）, II-238
- WHERE 子句, 89, 91, II-275
- `while`语句, 9, 74, 117, 193, 257, II-212, II-248, II-326, II-328
- 白盒测试, II-299
- 空格
- 修剪, 151
- XP（参见极捷编程）
- XPath, II-81, II-123, II-128, II-134, II-139
- 谓词, II-136
- XQuery, II-134
- XSL 格式化对象 (XSL-FO), II-200
- XLT, II-79, II-135, II-138
- 错误处理, II-139
- XSS（参见跨站脚本攻击 (XSS)）
- XUL（参见 XML 用户界面语言 (XUL))
- 无线应用协议 (WAP), II-205
- 无线标记语言 (WML), II-135, II-169, II-205, II-279, II-289
    - （也参见 HAHA）
- 卡片, II-206
- 生成, II-208
- 使用 Opera 查看, II-205
- WML（参见无线标记语言 (WML))
- 自动换行（参见文本文本）
- 包装, 149
- WSDL, II-142, II-150, II-157, II-160
- 编辑器, II-151

# Z

- ZIP 文件（参见压缩文件）

# X

- Xdebug（参见 PHP 扩展, Xdebug）
- XML, 17, 18, 290, II-79, II-205, II-238
    - （也参见 XPath）
    - （也参见 XSLT）
- 转换为 SQL, II-138
- 生成, II-80, II-111, II-112
- XML 实体引用, II-93
- XML 命名空间, II-81, II-127
- 默认命名空间, II-127
- XML 处理指令, 18, II-81, II-93, II-201
- XML Schema, II-81, II-142
- XML 用户界面语言 (XUL), II-169, II-215
- XML-RPC, II-xiii, II-141
    - （也参见 SOAP）
    - 构建客户端, II-152, II-164
    - 构建服务器, II-157
    - 与 XML-RPC, II-142

# 接下来？

如果你喜欢《The PHP Anthology：面向对象的 PHP 解决方案》中的这些章节，为什么不自己订购一本呢？

在《The PHP Anthology：面向对象的 PHP 解决方案》第一卷的剩余内容中，你将学习如何基于面向对象的软件设计原则，通过实际解决方案将 PHP 的基础功能（如文件和文本处理、图像生成和电子邮件）发挥到极致。你还将获得代码库下载权限，这样你就可以尝试所有的示例而无需重新输入！

以下是在第一卷中你将学习使用 PHP 实现的部分功能：

- 通过 FTP 上传和下载文件
- 创建压缩 ZIP/TAR 文件
- 实现敏感词过滤
- 构建在线日历
- 创建缩略图
- 显示图表和折线图
- 处理入站邮件
- 创建“搜索引擎友好”的 URL
- 实现自定义错误处理程序
- 以及更多更多内容……

千万不要忘记《The PHP Anthology：面向对象的 PHP 解决方案》第二卷！它涵盖了 PHP 的复杂应用，包括 XML 处理、PDF 文件等替代内容类型、网站统计、单元测试、设计模式等许多精彩内容！

立即订购，让它直接送到家门口！
