
# JavaScript 和 PHP 用户数据收集与分析实战

## 前言

任何 Web 应用程序的驱动力都是应用程序的用户和创建应用程序的开发者。然而，在开发过程中，用户的利益和需求往往会被搁置，转而关注开发者认为他们需要什么。这种开发风格通常导致复杂的用户界面、糟糕的设计选择和信息过载。

为了缓解这种情况，在开发过程中，应将用户与应用程序的日常交互及其整体意见视为重中之重。本书旨在提供收集和分析数据所需的工具和知识，无论数据的格式或来源如何。

本书将可从用户那里收集的数据类型划分为一条分界线。主动数据被定义为通过向用户提供表达对某个功能或主题的意见和感受的方式来收集的数据。这些解决方案通常在网站上以评分系统、反馈框和用户调查的形式出现。与此相对，被动数据被定义为在后台收集的、无需用户直接交互的数据。这种数据的形式包括浏览器指纹、IP 地址、地理位置数据、页面停留时间以及与应用程序交互期间的鼠标位置。

随着云存储解决方案的出现，保留的数据比以前更多了。销售数据、交易日志和用户调查都成为数据分析的来源。数据可以来自许多不同的来源，其中一些可能在应用程序开发之前就已经存在。重点在于收集这些数据并将其整理成可用于分析的格式。

收集到这些数据后，分析过程就可以开始了。对于每种不同的数据类型——例如，数字或文本——可以生成统计和可视化图表。本书为从数据中创建有意义的洞察和可视化提供了基础，这些洞察和可视化既符合业务需求，也符合开发人员需求。

与任何新技术一样，新解决方案面临的常见问题是如何将其集成到现有系统或实现中。为便于开发，本书中的每个示例均独立开发，以便于轻松集成。我们着重于技术的多样性，以提供对可用技术的全面理解。

本书描述了完整的开发生命周期，概述了如何收集、分析数据，并向项目的关键利益相关者报告。

## 作者

**凯尔·戈斯林**

都柏林理工大学

爱尔兰，都柏林

**马库斯·霍夫曼**

都柏林理工大学

爱尔兰，都柏林

## 致谢

我要感谢阿曼达的持续支持，无论家中或室外天气如何，她都允许我躲在办公室里写作和审稿。你的意见和感受对我来说比任何其他事情都更重要。我还要感谢我的父母泰德和克莱尔，他们对一切学术事务都给予了坚定不移的支持。追求知识和冒险总是得到鼓励，因为即使多次失败，最终的回报总是更好。我还要感谢我的兄弟达拉赫，当沮丧或写作瓶颈出现时，他始终是耐心的倾听者。

我还要感谢都柏林理工大学布兰查斯敦校区信息学系主任丹尼尔·麦克威尼，感谢他的支持和鼓励。想法总能得到指导和反思。我不能忘记我的同事彼得·亚历山大、塔拉·坎贝尔、简·汉拉蒂以及 A57 办公室的所有其他人，感谢他们的持续支持和鼓励。分享经验总是更美好。我还要感谢菲利普·卡瓦纳对本书的技术审阅。

本书融合了许多源于在都柏林理工大学布兰查斯敦校区教学中的想法和概念。我要感谢我的学生们，他们是学术界的命脉。

> — 凯尔·戈斯林

## 图目录

- 1.1 在 `Google Chrome` 中查看开发者控制台。7
- 1.2 在开发者控制台中禁用缓存。8
- 2.1 是和否二元选项。16
- 2.2 显示所选单选按钮值的警报框。16
- 2.3 否选项展开，允许用户以文本格式扩展他们的回答。21
- 2.4 星级评分示例。23
- 2.5 带有预设评分的星级评分。28
- 2.6 已完成的响应表单。37
- 2.7 表单提交后显示给用户的 `Bootstrap` 模态框。38
- 3.1 从 `cookie` 中检索值。41
- 3.2 设置和获取 `JSON` 值。43
- 3.3 遍历 `JSON` 值。45
- 3.4 使用自定义 `JavaScript` 函数添加的 `JSON`。47
- 3.5 回显到 Web 浏览器的唯一会话 ID。48
- 3.6 从存储在会话中的数组输出到浏览器的文本。49
- 3.7 `jQuery File Upload` 插件的文件夹结构。51
- 3.8 `jQuery File Upload` 插件的默认布局。51
- 3.9 `Google` 表单示例。54
- 3.10 `Google` 表单导出选项。54
- 3.11 `Google` 表单下载 `CSV` 响应。55
- 3.12 示例 `Google` 表单 `CSV` 文件。55
- 3.13 输出到浏览器的 `CSV` 文件内容。57
- 3.14 从文本文件中读取并输出到浏览器的三行独立文本。58
- 3.15 `JSON` 格式的 IP 地址。59
- 3.16 呈现给用户的是/否选项。63
- 3.17 用户选择是或否后显示的消息。64
- 3.18 打印到控制台的用户代理。66
- 3.19 `user_agent.php` — 使用 `PHP` 检索的用户代理。66
- 3.20 示例地理信息。69
- 3.21 在浏览器中以 `JSON` 格式显示的地理信息。70
- 3.22 与 IP 地址关联的当前位置打印到控制台。71
- 3.23 四秒后输出到控制台。72
- 3.24 用户在 `div` 标签上花费的秒数。74
- 3.25 用户导航离开当前页面时打印到控制台的消息。76
- 3.26 记录到数据库表的示例计时。80
- 3.27 调用 `PHP REFERRER` 变量的输出。81
- 3.28 新项目的示例 `composer.json` 内容。83
- 3.29 `Composer` 库安装控制台输出。83
- 3.30 `Twitter API` 搜索结果。86
- 4.1 登录页面的自定义仪表板。93
- 4.2 已完成的仪表板注册页面。103
- 4.3 注册成功时显示的 `Bootstrap` 模态框。104
- 4.4 `Charts.js` 的下载选项列表。105
- 4.5 `Chart.js` `zip` 文件的内容。105
- 4.6 `Chart.js` 文件夹的内容。106
- 4.7 包含工作示例列表的 `index.html`。106
- 4.8 显示每个分数计数的条形图。111
- 4.9 用于二元数据的双列条形图。116
- 4.10 包含示例数据源和配置选项的数据库表。119
- 4.11 示例 `Bootstrap` 仪表板。119
- 4.12 带导航栏的 `Bootstrap` 默认仪表板。123
- 4.13 选择活动模态框，包含两个可用活动。129
- 4.14 查看活动列表，其中一个活动元素被选中。130
- 4.15 添加了两个可视化的示例仪表板。139
- 4.16 允许用户创建新活动的两个文本字段。143
- 4.17 添加新活动元素并选择数据源的过程。150
- 5.1 使用 `JavaScript` 进行停用词移除前后的对比。156
- 5.2 `stopwords.php` — 使用 `PHP` 进行停用词移除前后的对比。158
- 5.3 示例评论记录。160
- 5.4 查看红旗菜单选项。163
- 5.5 选择日期和 CID 模态框。163
- 5.6 `jQuery` 日期选择器。164
- 5.7 每条评论输出时，红旗术语会高亮显示。167
- 5.8 N=2 的示例 n-gram 输出。170
- 5.9 在反馈记录中搜索单词“staff”的结果。173
- 5.10 调用词干提取算法后的结果。174
- 5.11 `BigHugeLabs.com` API 密钥创建过程。175
- 5.12 `BigHugeLabs.com` 示例 `REST URL`。176
- 5.13 通过 `GET` 请求调用 `Big Huge Labs API` 返回的示例同义词。178
- 5.14 单个文档中每个术语的示例 `TF-IDF` 输出。185
- 5.15 情感分析过程的结果。187
- 6.1 未移除停用词的示例词云。191
- 6.2 使用词频动态生成词云的输出。
- 6.3 完成的基于树的结构，句子根节点作为父节点。
- 6.4 两个关键词和一个日期的 `Vis.js` 图形输出。
- 6.5 显示一周内七天正面和负面反馈的时间图。
- 7.1 时间段分析控件。
- 7.2 选择分析过程的开始时间。
- 7.3 选择感兴趣的开始时间。
- 7.4 两小时窗口内正面和负面反馈的时间段分析。
- 7.5 实时反馈评分报告折线图。
- 7.6 正面和负面反馈的日历视图。单元格的阴影表示记录数量。
- 7.7 鼠标悬停显示给定日期的记录数量。
- 7.8 使用 `jQueryUI` 日期选择器选择日历日期。
- 7.9 显示单日 24 小时的热图。
- 7.10 显示给定时间段反馈记录数量的工具提示。
- 8.1 显示众数和该众数记录总数的输出。
- 8.2 给定列的平均值结果。
- 8.3 示例标准差结果。
- 8.4 计算百分比差异。
- 9.1 在 `PDF` 文件中呈现的统计数据。
- 9.2 `cron-job.org` 网站。
- 9.3 在 `cron-job.org` 上创建示例 `cron` 任务。
- 9.4 为 `cron` 任务创建示例计划。
- 9.5 正在通过 `composer` 安装 `SendGrid API`。
- 9.6 `Amazon Lightsail` 仪表板。
- 9.7 选择 `Lightsail` 镜像类型和蓝图。
- 9.8 选择 `Lightsail` 实例类型。
- 9.9 为 `Lightsail` 实例提供名称。
- 9.10 处于挂起状态的 `Lightsail` 实例。
- 9.11 正在运行的 `Lightsail` 实例。
- 9.12 `Lightsail` 集成控制台。
- 9.13 创建或下载现有密钥的选项。
- 9.14 `FileZilla` 主页。
- 9.15 `FileZilla` 新连接窗口。
- 9.16 `Amazon Lightsail` 实例上的文件和文件夹列表。
- 9.17 在 `FileZilla` 中选择要上传到实例的文件。
- 9.18 在 Web 浏览器中查看的示例应用程序。

## 表格目录

- 5.1 当 `N=2` 时的 n-gram 示例 — 168
- 5.2 当 `N=3` 时的 n-gram 示例 — 168
- 5.3 词频示例记录 — 179
- 5.4 词频得分示例 — 181
- 5.5 词频—逆文档频率示例记录 — 181
- 7.1 `MySQL` 数据库的时间和日期数据类型 — 222

## 1.1 绪论

理解用户的需求和要求是任何企业的主要驱动力之一。采集的数据可以洞察用户对某项功能或主题的看法，以及他们在日常工作中的行为方式。这些数据可以通过向用户提出简单问题，允许用户从预定义列表中选择选项，或输入自己的基于文本的回答来直接收集。

尽管可以直接询问用户的意见，但也可以使用其他方法来收集数据。数据可以通过 Web 应用程序间接收集，监测用户与应用程序的交互和行为。收集到的数据可以被处理以生成有意义的统计信息和可视化结果，提供对用户兴趣和需求的概览以及深入分析。

每种不同的数据类型，例如数值数据和文本数据，都有识别重要性和相关性的方法。定量和定性分析方法都可以用来提取这些洞察。在本书中，我们将探索用于数据收集、提取和分析的不同方法。本书旨在描述许多不同的方法，以期尽可能多地捕获数据用于分析。

为了提供完整的解决方案，我们将探索在云服务器上开发和部署开发出的解决方案的过程，包括报告生成和交付等附加功能。本书强调技术的多样性，向你展示许多不同的数据收集和分析替代方案，为你提供开发成熟解决方案所需的工具。

## 1.2 本书受众

本书面向具有一定 `JavaScript` 和 `PHP` 基础知识的 Web 应用程序开发人员。本书在这些基础知识之上构建，并提供完整的工作示例，可以轻松部署到现有的 Web 应用程序中。

本书并非面向不具备这些技能的人，但关于收集数据和生成洞察的知识对于理解可用工具和方法仍然很有价值，前提是你有开发人员来实现这些解决方案。

## 1.3 使用技术

在本书中，各章节使用的技术之间存在明显的区别。在客户端，即用户的 Web 浏览器中，将使用 `HTML` 和 `JavaScript`。在服务器端，使用 `PHP 7.4` 版本¹ 运行在 `Apache 2.4` 版本 Web 服务器² 上，来进行大部分的数据处理，例如将信息存储在数据库中以及计算统计信息。

使用 `JavaScript` 是因为它能够在不将用户重定向到多个不同页面的情况下操纵和呈现数据。利用收集到的数据，将使用 `JavaScript` 和 `HTML/CSS` 库创建可视化效果。由于 `JavaScript` 是一种由各 Web 浏览器供应商实现的基于浏览器的编程语言，每个浏览器在解释方式上可能存在细微差异。为了规避跨浏览器兼容性问题，我们将尽可能利用 `JavaScript` 库。本书中使用的主要 `JavaScript` 库是 `jQuery 3.5`。³

`jQuery` 提供了纯 `JavaScript` 的所有功能，但所有跨浏览器问题都已得到彻底测试。任何 `JavaScript` 新手搜索代码时，往往会找到特定于浏览器的 `JavaScript` 代码，并将其视为正确的解决方案。但可能在一个浏览器中正确运行的代码，在另一个浏览器中可能无法运行。让开发人员沮丧的是，即使是同一浏览器的不同版本，在运行示例代码时也可能会导致问题。因此，我们将广泛使用库来加快开发进程。

为了辅助可视化过程，我们将探讨基于 `JavaScript` 的库，例如 `D3.js`、`Charts.js` 和 `Google Charts`，因为它们提供高质量的交互式可视化。本书强调使用库的多样性，以提供不同代码库的学习体验。

由于所有收集到的数据都需要被检索用于分析，我们将探讨不同的数据来源。这方面的例子包括利用逗号分隔值（`CSV`）文件、简单文本文件、`JSON` 文件和数据库表。在本书中，我们将使用的核心数据库是 `MySQL 8` 社区版⁴，因为它免费、使用广泛，并且能与 `PHP` 集成。

尽管存在许多不同的 Web 浏览器，但本书中示例的开发过程使用的是 `Google Chrome 80`。⁵

## 1.4 数据变体

在本节中，我们将开始分解两种可以从用户那里收集数据的方法。第一种方法是主动数据收集，即直接询问用户以提供答案或判断。第二种方法是被动数据收集，即所有的数据都在后台收集，无需用户干预。后者的例子包括通过监听浏览器环境来收集数据。当用户浏览 Web 应用程序时，数据可以被记录并保存，供将来检索。

数据可以有结构化和非结构化的格式。结构化数据的一个例子是数据库表，其中包含用户评级的一到十之间的兴趣程度。这种数据唯一可能的变化就是提供给用户的范围内的数字。这种结构化数据的另一个组成部分是处理速度，由于数据已经是期望的格式，因此几乎不需要处理。要从中获得洞察，可以使用总数量、总和和平均值等简单指标。

结构化数据与非结构化数据形成对比，后者可能存储在任意数量的不同位置，例如文本文件、`CSV` 文件或数据库表。这种形式的数据本质上没有结构。这增加了数据处理的复杂性，因为它不仅仅是简单的计算或表中的预定义列。要从中提取含义，必须执行额外的处理，例如识别相关性和重要性。

处理之后，可以执行额外的步骤来识别各个数据片段之间的关系。这方面的例子包括使用图表来可视化这些关系。随着在应用程序交互过程中数据量的增长，可以对数据进行过滤，以便聚焦于关键趋势。

### 1.4.1 主动数据

主动数据是指由用户直接提供的任何数据。这些数据可以通过询问用户对某个主题的看法来收集，也可以是针对问题的简短“是”或“否”回答。通常来说，用户没有时间去提供大量信息，详细说明他们对某个特定页面或主题的看法。这常常导致开发人员考虑提出问题的最佳时机或方式。

主动数据的缺点是，与用户交互存在成本。在任何流程的末尾，许多用户根本不想留下任何形式的数据，并认为这个过程很烦人。主动数据的例子包括：

- 在社交媒体界面上，用户分享或“点赞”某个网站特定页面的次数。
- 为网站上的产品留下评分。
- 回答调查问卷中的问题。
- 在网站上设置自定义选项。

### 1.4.2 被动数据

被动数据是在应用程序后台收集的、无需任何用户干预的数据。尽管用户正在浏览内容并选择不同的感兴趣的文章，但在任何时候都不会正式要求用户提供关于他们正在查看内容的输入。被动数据收集方法包括通过监听浏览器环境来收集数据。当用户浏览 Web 应用程序时，数据可以被记录并保存，供将来检索。

数据可以有结构化和非结构化的格式。结构化数据的一个例子是数据库表，其中包含用户评级的一到十之间的兴趣程度。这种数据唯一可能的变化就是提供给用户的范围内的数字。这种结构化数据的另一个组成部分是处理速度，由于数据已经是期望的格式，因此几乎不需要处理。要从中获得洞察，可以使用总数量、总和和平均值等简单指标。

结构化数据与非结构化数据形成对比，后者可能存储在任意数量的不同位置，例如文本文件、`CSV` 文件或数据库表。这种形式的数据本质上没有结构。这增加了数据处理的复杂性，因为它不仅仅是简单的计算或表中的预定义列。要从中提取含义，必须执行额外的处理，例如识别相关性和重要性。

处理之后，可以执行额外的步骤来识别各个数据片段之间的关系。这方面的例子包括使用图表来可视化这些关系。随着在应用程序交互过程中数据量的增长，可以对数据进行过滤，以便聚焦于关键趋势。

被动数据的例子包括：

- 用户在某个特定页面集合（这些页面彼此直接相关）中花费的时间。
- 用户的人口统计信息。
- 用户与应用程序交互时的点击次数。
- 应用程序生成的日志文件。
- 用户的地理位置/IP 地址。
- 应用程序的使用模式。

## 1.5 你需要什么

由于本书的重点是 Web 应用程序的开发，因此需要完整的服务器栈。本书通篇使用的三大主要技术包括：带有 `PHP` 模块的 `Apache` Web 服务器和 `MySQL` 数据库。对于新手开发者，建议使用预打包的解决方案，例如 `XAMPP`⁶，这是一个为 Web 开发者提供的预配置解决方案，无需费力安装和配置各个独立组件即可使用所有这些服务。`XAMPP` 目前可用于 Microsoft Windows、Apple Mac 和 Linux 发行版。

`XAMPP` 的替代方案包括 `MAMP`⁷、`EasyPHP`⁸ 和 `AMPPS`⁹ 等工具。

为了帮助开发过程，本书通篇使用 `JavaScript` 库。为了避免为每个不同的示例下载所需的 `JavaScript` 文件，并确保使用最新的可用代码库，我们尽可能使用内容分发网络（`CDN`）。这些可以在每个示例的开头几行中看到。



由于大多数 PHP 库都有预打包版本，我们将使用命令行应用程序 `composer`。这是一个 PHP 依赖管理工具。Composer 可以从 [https://getcomposer.org/download](https://getcomposer.org/download) 下载。在安装 `composer` 的过程中，它会要求指向 `php.exe` 文件的位置。如果你使用的是本地 Web 服务器，这通常安装在自动检测到的 `php/` 文件夹内。安装完 `composer` 后：

^6 [https://www.apachefriends.org](https://www.apachefriends.org)

^7 [https://www.mamp.info/en](https://www.mamp.info/en)

^8 [https://www.easyphp.org](https://www.easyphp.org)

^9 [https://www.ampps.com](https://www.ampps.com)

打开命令提示符并导航到你项目的根文件夹。之后，执行 `composer init` 命令以开始创建 `composer.json` 文件。

Composer 与其他工具不同，它不是在系统范围内工作的，而是专注于在每个项目的基础上工作。每个单独的项目都会有一组指定的库，这些库定义在 `composer.json` 文件内部。这是一个人类可读的文件，包含给定 PHP 项目的不同需求列表，采用 JSON 格式。

一个例子是定义了对 `PHPinsight` 包的引用以及该包的版本号的 composer 文件。要添加到项目的其他 PHP 包可以在 https://packagist.org 找到。下面是 `composer.json` 文件中 JSON 的示例。

```json
{
    "require" : {
        "jwhennessey/phpinsight": ">=2.0.9"
    }
}
```

在将 `composer.json` 添加到项目文件夹后，可以使用 composer 来管理额外的包。通过打开命令提示符并导航到 `composer.json` 所在的项目根目录，可以向 composer 发出 `install` 命令。执行此操作后，将解析 JSON 文件的内容，并下载和安装所有指定的依赖项到项目中。

```bash
composer install
```

如果我们想向项目添加新的依赖项，可以使用 `require` 命令：

```bash
composer require jwhennessey/phpinsight
```

这一过程极大地改进了构成项目的不同包的手动安装过程。

## 1.6 开发环境

在本书的编写过程中，重点放在了客户端编程语言 JavaScript 上。在使用 JavaScript 时，代码中一个很小的问题可能会迅速波及到其他部分，导致一连串的错误。为了帮助 JavaScript 的调试过程，应经常使用 `console.log()` 函数。只要将该函数放在 JavaScript `script` 标签内，就可以从网页中的任何位置调用它。示例代码 1 展示了一个简单网页调用此函数的示例。

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Hello World</title>
    </head>
    <body>
        <p>Hello World!</p>

        <script>
            console.log("Hello world!");
        </script>
    </body>
</html>
```

### 示例代码 1：包含嵌入式 JavaScript 的 HTML 文档示例

要在 Google Chrome 中访问此控制台日志，可以一起按下 `Ctrl+Shift+I` 键来查看开发者工具，如图 1.1 所示。

![](img/ed4cb7e1be98f0adec0546edd14f6223_31_0.png)

### 图 1.1：在 Google Chrome 中查看开发者控制台

此控制台提供有关 JavaScript 代码中遇到的错误信息，以及错误发生在哪一行的信息。单独的 JavaScript 变量、对象和字符串可以传递给 `console.log()` 函数。为了帮助调试过程，可以在一段 JavaScript 代码运行之前和之后调用该函数进行打印。这使我们能够轻松查看代码是否按预期运行。

由于使用本地 Web 服务器是为了模拟商业服务器的行为以用于开发目的，有时会实现一些不需要的功能。其中一个例子是打开本地网页时浏览器执行的网站缓存。由于在开发过程中会对应用程序进行更改，浏览器通常不会渲染最新版本的代码，而是选择返回缓存版本。为了防止这种情况，开发者工具允许我们禁用此缓存功能。

通过进入 Google Chrome 开发者工具中的 `Network` 选项卡，可以在开发期间勾选 `disable cache` 选项，如图 1.2 所示。

![](img/ed4cb7e1be98f0adec0546edd14f6223_32_0.png)

### 图 1.2：在开发者控制台中禁用缓存

## 1.7 代码示例

本书包含许多可以在你的本地 Apache/PHP/MySQL 服务器上运行的 JavaScript/HTML 和 PHP 代码示例。为了帮助开发，完整的示例可以从本书的官方网站 [https://www.kylegoslin.ie/applied](https://www.kylegoslin.ie/applied) 下载。对于需要使用数据库的示例，SQL `create` 和 `insert` 语句也可获得。这些应在本地运行示例之前添加到你的数据库中。

这些示例只需很少的修改即可运行。通常，数据库的访问详细信息可能是原始代码唯一需要的修改。重点是开发可以独立运行而非作为更大框架一部分的代码示例。这为将这些示例放入现有应用程序提供了机会。

尽管安全是 Web 应用程序开发的重要组成部分，但它不是本书的重点。因此，如果任何示例用于实时环境，应采取额外的谨慎措施来实施正确的安全机制。

## 1.8 本书大纲

在本节中，简要介绍本书的结构。

第 1 章eresting.

on any given day, a linked graph is described. As data is often collected at different times, a time-series analysis approach is described for positive and negative feedback records.

第 7 章：基于时间的反馈分析——介绍了数据的时间组成部分，以及如何利用它进行数据分割。

由于时间是一个持续进行的实体，文中描述了一种基于时间段分析和可视化的方法，允许查看各个时间窗口。实时反馈分析领域适用于数据收集过程正在积极进行的情况。为了在单一可视化中查看更大的数据集，文中描述了为给定年份创建正负反馈日历的过程。为了以较小的规模查看大数据集，文中描述了查看自定义颜色编码反馈热力图的过程。

对于任何类型的数据，都可以推导出统计信息。在第 8 章：反馈统计与概览中，描述了统计学基础并附有完整示例。由于处理大型数据集通常非常耗时，文中描述了使用代表性样本的过程。随后描述了计算百分比差的过程，inae 大多数生成的统计信息都可以表示为百分比。

最后，在第 9 章：托管、报告与分发中，描述了基于 PHP 生成 PDF 报告的过程。由于许多数据处理任务都是每天执行的，文中描述了针对本地和外部服务的任务调度过程。为了向关键利益相关者提供生成的报告，文中描述了集成云端电子邮件服务的过程。最后，当完整的应用程序开发完成后，文中描述了在 Amazon Lightsail 上托管 PHP/JavaScript 应用程序的过程。

## 1.9 本章小结

本章介绍了运行本书示例所需的工具和环境。描述了被动数据和主动数据的概念，指出数据不一定需要直接从用户处收集。可以采用间接方法，例如记录与应用程序的交互、识别相关数据源（如现有文件和社交媒体流）来收集数据以供分析。在第 2 章中，将描述通过主动方法收集数据的过程，以开始数据收集、分析和可视化的循环。

# 主动数据收集

## 2.1 引言

在本章中，我们将描述直接从用户处收集数据的过程。这通过使用简单的二元选择、基于文本的内容和星级评分来实现。这些数据被归类为主动数据，因为用户需要参与数据收集过程。然而，直接从用户处收集数据可能很困难，因为用户通常不愿意为此投入时间。我们试图使用户数据收集过程尽可能简单且不引人注目。

## 2.2 二元数据收集

许多现代 Web 应用程序为用户提供简单的数据收集机制，形式为二元选择。通常，这是回答问题的结果。一个简单的 `是` 或 `否` 输入字段可以快速收集用户的意见，且只需最少努力。这些机制故意限制用户可以拥有的选项和交互数量。此数据的提交过程也可以是自动的，以防止用户选择选项后因忘记点击提交按钮而遗漏数据。

为了帮助未来的分析过程，此示例应用程序中的每个页面都被视为独立的文章。每篇文章都有一个唯一的 `ID`，以区分不同的文章。

## 示例 1：二元数据收集

此示例包含三个核心文件和一个库：

- `create.sql` — 用于创建 `yesno` 数据库表。
- `binary.html` — 主要的 HTML/JavaScript 二元数据收集界面。
- `ajax.php` — 用于接收数据并将其存储在 MySQL 数据库中。
- jQuery — 用于向 `ajax.php` 页面执行 JavaScript POST 请求。

### 示例代码：create.sql

在创建用户界面之前，首先需要创建一个新的 MySQL 数据库表，命名为 `yesno`，如示例代码 2 所示。该表包含四个不同的属性，其中两个在插入新记录时自动生成。第一个是 `ID` 列，它是自增的并作为主键。每次在数据库中创建新记录时，`ID` 将增加 1。这对于在未来唯一标识记录非常有用。第二列命名为 `mytime`。每次创建新记录时，服务器上的当前时间戳将与该记录一起记录。第三列和第四列将根据用户正在查看的文章以及所作的选择而变化。

由于 `articleid` 是数字，其数据类型将设置为 `int`。然而，`result` 列包含字符串 `Yes` 或 `No`。为了容纳此内容，`result` 列的数据类型设置为 `varchar`。

```sql
CREATE TABLE `yesno` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `mytime` TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP ,
    `articleid` INT,
    `result` VARCHAR (10),
    PRIMARY KEY (`id`)
);
```

示例代码 2：create.sql — `yesno` 数据库表 SQL。

### 示例代码：binary.html

在示例代码 3 中，第 1 行首先添加了对 jQuery<sup>1</sup> 内容分发网络（CDN）的引用。第 4 行和第 6 行添加了两个单选按钮以及一个简单的 `div` 标签，使表单可被 uniquely identifiable。

[1](https://code.jquery.com)

JavaScript 将负责监听对表单所做的更改，并将数据传递给 Web 服务器以保存在数据库表中。在示例代码中，两个单选按钮具有相同的 `name` 属性。这样做是因为它们都属于同一组，防止同时被选中。

第 10 行添加了一个 jQuery `click()` 监听器。它监听对单选按钮的点击。在识别单选按钮时，将 `input:radio` 值传递给 jQuery 选择器，指定我们感兴趣的是 `name` 属性定义为 `answer` 的单选按钮。当任一单选按钮被点击时，`click` 函数内的 JavaScript 将被触发。在此函数内部的第 11 行，我们可以使用关键字 `this`，它代表刚刚被点击的单选按钮。使用它，我们可以调用 `val()` 函数，该函数将返回所选单选按钮的值。

之后在第 12 行，调用了一个名为 `saveAnswer()` 的自定义 JavaScript 函数。调用时，用户当前选择的值将传递给此函数。第 15 行的 `saveAnswer()` 函数接收一个参数，即用户选择的值。在此函数内部，第 16 行添加了一个 jQuery POST，用于将 `answer` 变量发送到名为 `ajax.php` 的服务器端页面，以将数据保存到数据库表。在 jQuery POST 中，第一个参数是 `ajax.php`。这是对将处理数据库交互的页面的引用。添加了一个自定义 `type` 参数，以便我们可以通过唯一标识发送到页面的不同类型的请求，将同一 `ajax.php` 页面用于多种不同目的。

`type` 变量设置为 `yesno`。接下来，我们将传递用于标识数据来源页面的 `articleid`。`articleid` 设置为 1221。传递的最后一个参数名为 `result`。此变量的值来自传递给 `saveAnswer()` 函数的用户选择，即 `answer`。第 18 行添加了一个 `done()` 函数。当所有处理完成且数据已发送到数据库时，将调用此函数。第 19 行添加了一个简单的 `alert()` 函数，在用户提交数据后告诉他们 `"Thank you!"`。

14 ■ 使用 JavaScript 和 PHP 应用用户数据收集与分析

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js"
 crossorigin="anonymous">
</script>
<div id="binaryfeedback">
    您对本服务满意吗？
    <input type="radio" name="answer" value="Yes"> 是
    <input type="radio" name="answer" value="No"> 否
</div>
<script>
$( "input:radio[name=answer]" ).click(function() {
    var val = $(this).val();
    saveAnswer(val);
});

function saveAnswer(answer){
    $.post( "ajax.php", { type: "yesno", articleid: "1221",
      result: answer })
    .done(function( data ) {
        alert('感谢！'+data);
    });
}
</script>
```

样例代码 3：binary.html —— 向用户展示“是/否”选项。

### 示例代码：ajax.php

在样例代码 4 中，创建了标题为 `ajax.php` 的新 PHP 页面。此附加页面永远不会被用户直接打开；它通过 jQuery `POST` 函数动态调用。每当数据被保存时使用 PHP 数据对象（PDO）保存到数据库表中。在第 2 行，引用 `POST` 变量以提取来自 JavaScript 请求传递的值。在第 3 行，使用简单的 `if` 语句检查 `type` 变量包含的值。如果类型设置为 `yesno`，则在第 4 行调用 `yesNoLog()` PHP 函数。在 `if` 语句之后，第 6 行添加 `yesNoLog()` 函数的定义。

在第 7 和第 8 行的 PHP 函数主体中，创建两个变量以捕获从 jQuery `POST` 请求发送过来的值。重要的是要确保 `POST` 中的变量名与之前使用 JavaScript `POST` 发送的变量匹配。在本例中，从 `POST` extracts `articleid` 和 `result`。收集变量后，可以建立数据库连接。数据库交互在执行于第 9 行开始的 try-catch 语句中进行。`host`、`dbname`、`user` 和 `pass` 变量定义在第 10 到 13 行。

这些变量反映了正在使用的 MySQL 数据库。在第 14 行，创建一个新的 PHP PDO。在第 16 行，创建简单的 SQL `INSERT` 语句。在语句末尾插入两个问号。这是占位符，用于存放将要追加的变量。

我们从 `POST` 捕获的两个变量通过 `bindParam()` 函数在第 19 和 20 行传递给 SQL 语句。这是将变量安全地传递给数据库的方法，不会引起任何安全问题，因为变量会进行清理。由于 `articleid` 是整数，添加的参数类型设置为 `PARAM_INT`。正在添加的 `result` 的类型设置为 `PARAM_STR`。

此过程的最后一步是运行 SQL 语句。在第 21 行，调用 `execute()` 函数。在第 22 行添加 catch 以完成 try-catch 块。如果在连接数据库或运行代码时出现任何错误，`catch` 块将运行，并调用 `getMessage()` 函数以获取错误消息。



```php
<?php
$type = $_POST['type'];
if ($type == 'yesno') {
    yesNoLog();
}
function yesNoLog() {
    $articleid = $_POST['articleid'];
    $result = $_POST['result'];
    try {
        $host = 'localhost';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
        $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $password);
        $sql = "INSERT INTO `yesno` (`articleid`, `result`) VALUES
            (?, ?);";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $articleid, PDO::PARAM_INT);
        $sth->bindParam(2, $result, PDO::PARAM_STR);
        $sth->execute();
    } catch (PDOException $e) {
        echo $e->getMessage();
    }
}
```

样例代码 4：`ajax.php`——将二元选择日志记录到`yesno`数据库表中。

### 输出

图 2.1 显示了这些单选按钮的输出，伴随着一个小问题，例如“您对本服务满意吗？”

您对本服务满意吗？○ 是 ○ 否

图 2.1：是/否二元选项。

在图 2.2 中，显示了数据在数据库表中记录后呈现给用户的警报框。

![](img/ed4cb7e1be98f0adec0546edd14f6223_40_0.png)

图 2.2：显示所选单选按钮值的警报框。

## 2.3 基于文本的数据收集

可以在基本二元数据收集过程中添加进一步的改进，以包含一个仅在用户选择“否”选项时出现的额外文本字段。虽然文本需要额外的处理来量化并收集见解，但它仍然很有用，因为可以从这些数据中得出许多衍生统计信息。

### 示例 2：提供收集文本的选项

本例由三个核心文件和一个库组成：

1. `create.sql`——此文件用于创建`whyanswerlog`数据库表。此表有一个额外的列用于存储文本。
2. `binary.html`——主要的 HTML/JavaScript 二元数据收集接口，并带有额外的文本字段。
3. `ajax.php`——用于接收数据并将其存储到 MySQL 数据库表中。
4. `jQuery`——用于添加点击处理程序并向`ajax.php`页面执行 JavaScript POST。

### 示例代码：`create.sql`

要存储文本，需要一个额外的数据库表。在样例代码 5 中，将`result`列设置为 500 个字符，以允许基于文本的回答。

```sql
CREATE TABLE `whyanswerlog` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `mytime` TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `articleid` INT,
    `result` VARCHAR(500),
    PRIMARY KEY (`id`)
);
```

样例代码 5：`whyanswerlog`数据库表的 SQL。

### 示例代码：`binary.html`

在样例代码 6 中，第 5 行添加了一个 `div` 标签，用于容纳用户阐述选择“否”原因的文本区域。第 11 行添加了一个简单的提交按钮以触发保存过程。提交按钮具有`onclick`设置，用于调用`saveWhyAnswer()` JavaScript 函数。

在第 14 行，为单选按钮添加了`click()`处理程序。在第 19 行，添加了一个简单的`if`语句，用于检查用户是否点击了“否”。如果是，我们将调用`findOutWhy()`函数，该函数将在第 20 行触发打开用户输入字段的输入框。

在第 31 行，添加了名为`findOutWhy()`的函数。在此函数内的第 32 行，调用了 jQuery `show()`函数，其 jQuery 选择器引用`explainwhy` `div`标签。

当用户点击提交按钮时，如第 34 行所示，会调用`saveWhyAnswer()`函数。在此函数的第 35 行，使用`getElementById()`函数收集用户输入的文本，该函数引用`whyanswer`文本区域。在第 36 行，调用类似于之前例子的 POST 函数。在第 39 行，使用简单的`alert()`语句向用户显示文本“感谢您的评论！”。

在第 42 行，页面加载完成后，使用`document ready`函数的简写版本。这确保了页面已加载，并且页面上的所有不同元素都准备就绪。一旦页面完全加载，jQuery 将使用`hide()`函数（第 43 行）隐藏我们刚刚创建的 `div`，直到用户选择“否”选项。

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js"
  crossorigin="anonymous"></script>
<input type="radio" name="answer" value="Yes"> Yes <br>
<input type="radio" name="answer" value="No"> No<br>
<div id="explainwhy">
    Sorry to hear you were not happy,<br>
    Would you like to say why?<br>
    <textarea id="whyanswer" rows="5" cols="50">
    </textarea>
    <br>
    <button onclick="saveWhyAnswer()">Submit</button>
</div>
<script>
$("input:radio[name=answer]").click(function() {
    var val = $(this).val();
    saveAnswer(val);

    if (val == 'No') {
        findOutWhy();
    }
});

function saveAnswer(answer) {
    $.post("ajax.php", {
        type: "yesno",
        articleid: "1221",
        result: answer
    }).done(function(data) {
        alert('Thank you!');
    });
}

function findOutWhy() {
    $("#explainwhy").show();
}

function saveWhyAnswer() {
    var answer = document.getElementById('whyanswer').value;
```

## 2.4 星级评分

星级评分功能允许我们以一个定义好的量表范围，从用户那里以最少的人机交互方式收集意见。星级评分通常让用户在一到五星的范围内进行评价。这种方法非常不具侵入性，因为用户不需要点击额外的提交按钮即可将结果发送到服务器。

评分系统主要有两种类型：一种允许用户以星级评级的形式提供反馈；另一种则显示之前的用户评分。本章末尾将讨论以星级形式收集统计信息并向用户展示的过程。由于像亚马逊（Amazon）和易贝（eBay）这样的网站上广泛使用星级评分，许多供应商提供了免费且开源的星级评分解决方案。这些实现方案各自具备不同程度的功能和处理用户输入的能力。评分方法的整体外观和感觉是决定使用哪种实现方案的主要因素。在本示例中，我们将考察`RateYo!²`星级评分包。

### 示例 3：星级评分

此示例包含一个文件和两个库：

1. `rating.html`——为用户提供星级评分界面。
2. `jQuery`——该库用于访问 jQuery 选择器。
3. `RateYo!`——用于提供星级评分界面。

² <https://rateyo.fundoocode.ninja>

### 示例代码：`rating.html`

在代码片段 8 中，包含了三个引用。第一个是在第 1 行对 jQuery 的引用，第二个是在第 3 行对 CSS 文件的引用，最后一个是在第 6 行对 RateYo JavaScript 文件的引用。文件包含之后，在第 9 行包含了一个 `div` 标签，它将被转换为星级评分系统。`div`标签的`ID`设置为`rateYo`。在第 11 行，添加了`document ready`函数的简写形式。

jQuery 选择器用于在第 12 行选择`rateYo` `div`标签。在这个`div`上调用`rateYo()`函数。在此内部，第 13 行的`onSet`接收一个当星星被点击时调用的函数引用。在本例中，第 14 行添加了一个简单的 alert 语句，以向用户指示他们选择的评分。用户进行的评分通过`rating`变量可用。

```html
<script src="https://code.jquery.com/jquery-3.1.0.min.js"
        crossorigin="anonymous"></script>
<link rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/rateYo/2.2.0/
      jquery.rateyo.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/rateYo/2.2.0/
      jquery.rateyo.min.js">
</script>
<div id="rateYo"></div>
<script>
$(function() {
    $("#rateYo").rateYo({
        onSet: function(rating, rateYoInstance) {
            alert("Rating is set to: " + rating);
        }
    });
});
</script>
```

代码片段 8：`rating.html`——星级评分界面。

### 输出

图 2.4 展示了加载时星级评分的外观示例。

![](img/ed4cb7e1be98f0adec0546edd14f6223_47_0.png)

图 2.4：星级评分示例。

### 示例 4：保存星级评分

在用户点击星星后，页面上唯一变化的是星星的状态。没有数据被存储在稍后可检索的数据库表中。

此示例包含三个文件和两个库：

1. `create.sql`——用于创建`starratinglog`数据库表。
2. `rating.html`——为用户提供可选的评分星星。
3. `ajax.php`——此页面接收评分并将其存储在数据库表中。
4. `jQuery`——添加以执行对`ajax.php`页面的 JavaScript POST 请求。
5. `RateYo!`——用于提供星级评分界面。

### 示例代码：`create.sql`

为了存储数据，需要一个新的数据库表，如代码片段 9 所示。该表包含一个唯一且自动递增的`ID`字段。接着是`mytime`，它保存记录创建时的时间戳。`articleid`列用于保存用户正在查看的文章的引用。用户输入的结果放置在`result`列中。由于用户不能选择半星，因此该列的数据类型设置为`int`。

```sql
CREATE TABLE starratinglog (
    `id` INT NOT NULL AUTO_INCREMENT,
    `mytime` TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `articleid` INT,
    `result` INT,
    PRIMARY KEY (`id`)
);
```

代码片段 9：示例`starratinglog`表 SQL。

### 示例代码：`rating.html`

在代码片段 10 的第 14 行调用了`saveRating()`函数，该函数接受一个名为`rating`的单个参数，其中包含用户选择的评分。在第 18 行，定义了该函数。在此函数中，第 19 行执行了对 jQuery POST 函数的调用。正在执行的请求`type`标题为`starrating`。正在查看的`articleid`设置为`1221`，`userrating`设置为`rating`，这是在选中星星时动态设置的。在第 22 行，添加了`alert()`调用，以便在选中评分时向用户展示文本`Thank you for your rating!`。

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js"
        crossorigin="anonymous"></script>
<link rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/rateYo/2.2.0/
      jquery.rateyo.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/rateYo/2.2.0/
      jquery.rateyo.min.js">
</script>
<div id="rateYo"></div>
<script>
$(function() {
    $("#rateYo").rateYo({
        onSet: function(rating, rateYoInstance) {
            saveRating(rating);
        }
    });
});

function saveRating(rating) {
    $.post("ajax.php", {
        type: "starrating",
        articleid: "1221",
        userrating: rating
    }).done(function(data) {
        alert('Thank you for your rating!');
    });
}
</script>
```

代码片段 10：`rating.html`——带有`saveRating()`函数的星级评分。

### 示例代码：`ajax.php`

添加了一个名为`ajax.php`的第二个页面，负责处理 AJAX 请求。它接收 POST 数据并将星级评分存储在数据库中。

```php
<?php
$type = $_POST['type'];
if ($type == 'starrating') {
    saveStarRating();
}

function saveStarRating() {
    $articleid = $_POST['articleid'];
    $rating = $_POST['userrating'];
    try {
        $host = 'localhost';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
        $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
        $sql = "INSERT INTO `starratinglog` (`articleid`, `result`) VALUES (?, ?);";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $articleid, PDO::PARAM_INT);
        $sth->bindParam(2, $rating, PDO::PARAM_INT);
        $sth->execute();
    } catch (PDOException $e) {
        echo $e;
    }
}
?>
```

代码片段 11：`ajax.php`——将星级评分保存到数据库的 PHP 页面。

### 输出

图 2.5 展示了选择三颗星星的结果。

![](img/ed4cb7e1be98f0adec0546edd14f6223_48_0.png)

图 2.5：选中并保存星级评分。

在本章中，我们探讨了从用户那里收集输入的几种不同方法。我们首先从一个简单的 yes/no 选择开始。然后，我们转向文本区域，允许用户输入解释其选择的评论。接下来，我们研究了星级评分，允许用户在定义的量表上提供反馈。每种方法都可以以非侵入性的方式收集用户的反馈。



该请求。在示例代码 11 的第 2 行，`type` 变量首先从 `POST` 中获取。在第 3 行执行检查，以确定发送的请求 `type` 是否等于 `starrating`。如果是，则调用第 4 行的 PHP 函数 `starRatingLog()`。在位于第 7 行和第 8 行的 `starRatingLog()` 函数内部，从 PHP `POST` 中提取 `articleid` 和 `userrating`，并将其放入本地变量中。

在第 14 行，建立数据库连接以将记录插入到 `starratinglog` 数据库表中。由于该表的前两列是自动生成的，因此 `insert` 语句仅需 `articleid` 和 `result`。在第 16 行的语句内部，两个问号占据了将要放置值的位置。`bindParam()` 函数在第 19 行和第 20 行被使用，在执行业务之前将值置入语句中。

```php
<?php
$type = $_POST['type'];
if($type == 'starrating'){
    starRatingLog();
}

function starRatingLog(){
    $articleid = $_POST['articleid'];
    $result = $_POST['userrating'];
    try {
        $host = 'localhost';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
        $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,
          $pass);
        $sql = "INSERT INTO `starratinglog` (`articleid`, `result`)
          VALUES (?, ?);";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $articleid, PDO::PARAM_INT);
        $sth->bindParam(2, $result, PDO::PARAM_INT);
        $sth->execute();
    } catch(PDOException $e) {echo $e;}
}
?>
```

**示例代码 11**：ajax.php — 将星级评级保存到 `starratinglog` 数据库表。

### 示例 5：检索星级评级

由于星级评级可用于收集用户意见，其反面则是显示平均星级评级。这是通过收集用户 previously 保存的评级来实现的。虽然数据库表将包含来自网站各处大量不同星级评级的数据，但我们必须确保仅获取当前正在考虑的该文章所需的评级。

本示例包含两个文件和两个库：

1. `star.php` — 此文件向用户提供可选择的评级星星，并显示预设评级。
2. `ajax.php` — 此页面接收新评级并将其存储到数据库表中。
3. `jQuery` — 用于执行 JavaScript `GET` 请求。

当首次设置评级流程时，我们为网站上实施的每个不同的星级评级分配了唯一的 `ID`。在本示例中，`articleid` 是包含单个星级评级实例所有信息的变量。

首先，我们将查看用于检索平均值的 SQL 查询。在本示例中，我们将使用名为 `avg()` 的 SQL 函数，它将返回给定 `articleid` 所有记录的平均值。在此 SQL 查询的右侧，添加了额外的 `WHERE` 子句，以限定记录集合，仅返回我们要关心的当前文章的平评率。

```sql
SELECT AVG(result) FROM starratinglog WHERE articleid ='1221';
```

### 示例代码：star.php

在示例代码 12 的第 13 行，使用 jQuery 向 `ajax.php` 页面执行 `GET` 请求。发送的 `type` 被设置为 `getrating`。为了确保返回单个星级评级的结果，传递了包含我们要关注的文章 `ID` 的 `articleid` 变量。在第 14 行，当 jQuery 函数返回后，调用 `done()` 函数，返回一个名为 `data` 的变量，其中包含将从 `ajax.php` 页面检索到的平均星级评级。在第 16 行，将 `data` 变量设置为 `rating` 变量的值，该变量决定了将突出显示多少颗星星。

```html
1  <script src="https://code.jquery.com/jquery-3.5.1.min.js"
2      crossorigin="anonymous">
3  </script>
4  <link rel="stylesheet"
5      href="https://cdnjs.cloudflare.com/ajax/libs/rateYo/2.2.0/
6      jquery.rateyo.min.css">
7  <script src="https://cdnjs.cloudflare.com/ajax/libs/rateYo/2.2.0/
8      jquery.rateyo.min.js">
9  </script>
10 <link rel="stylesheet" href="jquery.rateyo.css"/>
11 <div id="rateYo"></div>
12 <script>
13 $.get( "ajax.php", { type: "getrating", articleid: 1221})
14     .done(function( data ) {
15     $("#rateYo").rateYo({
16         rating:data,
17         onSet: function (rating, rateYoInstance) {
18     }
19     });
20 });
21 </script>
```

**示例代码 12**：star.php — 使用 `GET` 请求检索平均星级评级。

### 示例代码：ajax.php

示例代码 13 显示了 `ajax.php` 页面。在第 2 行，`type` 变量首先从 PHP `GET` 请求中接收。在第 3 行，使用 `if statement` 检查 `type` 是否等于 `getrating`。如果是，则调用位于第 4 行的 `getRating()` 函数。

在第 6 行，定义 `getRating()` 函数。在该函数内部的第 13 行，创建到数据库的连接。在第 15 行，添加用于检索平均评级的 SQL 语句。文章 `ID` 留作问号。使用 `bindParam()` 在第 18 行传入通过 jQuery `GET` 请求传递给该页面的 `articleid`。该查询运行后，在第 21 行，将返回单个结果。该结果放置在返回数组位置 0 的 `res` 变量中。使用 PHP `round()` 函数去除尾随小数，仅返回整数。

```php
<?php
$type = $_GET['type'];
if($type == 'getrating'){
    getRating();
}

function getRating(){
    $articleid = $_GET['articleid'];
    try {
        $host = 'localhost';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
        $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,
         $pass);
        $sql = "SELECT AVG(result) FROM starratinglog WHERE
         articleid=?";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $articleid, PDO::PARAM_INT);
        $sth->execute();
        $res = $sth->fetch();
        echo round($res[0]);
    } catch(PDOException $e) {echo $e;}
}
?>
```

**示例代码 13**：ajax.php — 检索平均星级评级并将其打印为页面输出。

### 输出

图 2.5 显示了一个带预设评级的示例。虽然数据库表中存在多条记录，但获得的平均星级评级为 3 星。

![](img/ed4cb7e1be98f0adec0546edd14f6223_52_0.png)

**图 2.5**：带预设评级的星级评级。

## 2.5 自定义响应表单

在本节中，我们将回顾创建完整响应表单的流程。此表单可用于提示用户以不同格式输入较长的数据。虽然可以向用户展示选项，但不能保证用户会全部填写。为此，在表单中添加了自定义验证，在提交表单之前提示用户为每个字段输入值。

为了辅助表单布局，使用 Bootstrap。Bootstrap 为表单提供了默认的视觉风格。除此之外，还将使用 Bootstrap 模态框在表单提交后向用户显示消息。

### 示例 6：带 JavaScript 验证的自定义响应表单

本示例包含三个文件和两个库：

1. `create.sql` — 此文件用于创建 `servicerating` 数据库表。
2. `form.html` — 此文件包含创建表单的主要 HTML 和 JavaScript 代码，以及 jQuery 和 Bootstrap 的引用。
3. `saveForm.php` — 接收来自表单的数据，并使用 PHP PDO 将其保存到数据库表中。
4. Bootstrap — 用于美化自定义表单，并添加创建模态框的功能。
5. jQuery — 用于向 `ajax.php` 页面执行 JavaScript POST 请求。

### 示例代码：create.sql

为了将该数据存储到数据库中，创建了一个名为 `servicerating` 的新表。该表包含用户输入每个表单项的属性。对于基于文本的数据使用 `varchar` 数据类型，对于数值数据使用 `int` 数据类型。为了唯一标识每个单独的记录，添加了一个 `ID` 列，并进行 `auto-incremented`（自动递增）设置，并将其设为 `primary key`（主键）。

```sql
CREATE TABLE `servicerating` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `email` VARCHAR(100),
    `fullName` VARCHAR(100),
    `serviceRating` INT,
    `foodRating` INT,
    `atmosRating` INT,
    `comments` VARCHAR(500),
    PRIMARY KEY (`id`)
);
```

示例代码 14：`servicerating` 数据库表 SQL。

### 示例代码：form.html

示例代码 15 概述了用于收集完整反馈的 HTML 表单。第 1 行首先添加了对 jQuery 的引用。第 4 行包含了 Bootstrap 的 CSS，随后第 8 行是 Bootstrap 所需的额外 JavaScript。第 12 行创建了一个 `div` 标签，它用作占位符，用于显示在表单字段留空时生成的错误消息。第 14 行添加了一个表单标签，其 `class` 属性设置为 `w-25`，这告诉浏览器使用 25% 的可用空间来显示表单组件。`p-2` 用于设置表单的内边距。

在 `form` 标签内部，可以添加各个表单元素。在此过程中，为各个表单元素提供唯一的 ID 非常重要。为了在用户填写表单时提供帮助，在第 16 行添加了单独的 `label` 标签。`for` 属性允许我们指定该标签所对应的表单元素。`aria-describedby` 用于指定一段将在表单元素下方显示的文本。

为了给用户提供一系列可供选择的选项，在第 35 至 42 行添加了一个 HTML `select` 元素。用户可以在一到五之间进行选择。`select` 元素的默认值是列表中的第一个选项。在此示例中，第一个选项留空。这在验证过程中很有用，因为如果未选择任何值，可以抛出错误。这也防止了表单在提交时带有默认值。

主动数据收集 ■ 31

```html
1 <script
2   src="https://code.jquery.com/jquery-3.5.1.min.js"
3   crossorigin="anonymous"></script>
4 <link rel="stylesheet"
5       href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/
6       bootstrap.min.css"
7   crossorigin="anonymous">
8 <script
9   src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/
10   bootstrap.min.js" crossorigin="anonymous"></script>

12 <div id="error_message">
13 </div>
14 <form class="w-25 p-2">
15 <div class="form-group">
16   <label for="emailAddress">E-mail address</label>
17   <input type="text" class="form-control" id="emailAddress"
18     aria-describedby="emailHelp"
19     placeholder="Enter email">
20   <small id="emailHelp"
21     class="form-text text-muted">We'll never share your email
22     with anyone else.
23   </small>
24 </div>
25 <div class="form-group">
26   <label for="fullName">Full name</label>
27   <input type="text" class="form-control" id="fullName"
28     aria-describedby="nameHelp" placeholder="Enter full name">
29   <small id="nameHelp"
30     class="form-text text-muted">Please enter your full name.
31   </small>
32 </div>
33 <div class="form-group">
34   <label for="serviceRating">How would you rate our service?</label>
35   <select class="form-control" id="serviceRating">
36     <option></option>
37     <option value="1">1</option>
38     <option value="2">2</option>
39     <option value="3">3</option>
40     <option value="4">4</option>
41     <option value="5">5</option>
42   </select>
43 </div>
44 <div class="form-group">
45   <label for="foodRating">How would you rate our food?</label>
```

32 ■ 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

```html
        </label>
        <select class="form-control" id="foodRating">
            <option></option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
        </select>
    </div>
```

示例代码 15：form.html — 完整的 Bootstrap 反馈表单（第 1 部分）。

在示例代码 16 中，第 74 行向表单添加了一个提交按钮。为了使表单更具交互性，当表单提交时，将打开一个 Bootstrap 模态框。第 77 行，模态框开始，其 `ID` 设置为 `success`。`div` 标签的 `role` 设置为 `dialog`。这将在表单提交期间用于打开此模态框。第 91 行向模态框添加了一个关闭按钮，允许用户关闭消息。



```html
<div class="form-group">
    <label for="atmosRating">How was the atmosphere in the restaurant?</label>
    <select class="form-control" id="atmosRating">
        <option></option>
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
        <option value="5">5</option>
    </select>
</div>
<div class="form-group">
    <label for="comments">Please tell us about your experience</label>
    <textarea class="form-control" id="comments" rows="3">
    </textarea>
</div>
<button type="submit" id="submit" class="btn btn-primary">Submit</button>
</form>
<div class="modal" id="success" tabindex="-1" role="dialog">
```

```html
<div class="modal-dialog" role="document">
    <div class="modal-content">
        <div class="modal-header">
            <h5 class="modal-title">Success!</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                <span aria-hidden="true">&times;</span>
            </button>
        </div>
        <div class="modal-body">
            <p>Thank you for the feedback.</p>
        </div>
        <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        </div>
    </div>
</div>
```

## 示例代码 16：`form.html` — 完整的 Bootstrap 反馈表单（第 2 部分）

旧的 Web 表单通过在`form`标签上附加`action`和`method`属性来使用它。由于我们使用纯 JavaScript，我们将使用 jQuery 来处理表单提交过程。在示例代码 17 的第 3 行，当点击提交按钮时，会调用`preventDefault()`函数。此函数用于抑制`form`标签重定向到不同页面的默认行为。之后，在第 4 行添加了一个新的变量`error`来存储表单的错误消息（如果有的话）。

在第 6—29 行，使用 jQuery 选择器来选择每个单独的表单元素。`val()`函数用于从元素中提取值。可以使用一个简单的`if`语句来检查表单字段中的值是否为空。如果为空，则使用`+=`语法将错误消息追加到`error`变量。

第 31 行，在错误检查完成后，可以使用一个`if`语句来检查`error`变量是否包含错误消息。如果存在错误消息，则使用`html()`函数将收集在`error`变量中的错误消息添加到`error_message div`中。如果表单有效，则在第 33 行执行 jQuery`POST`操作，将输入保存到数据库。

## 34 ■ 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

`post()`函数接受键值对，其中第一个变量（例如`email`）被传递，其值设置为变量`email`的值。赋予此变量的名称与将在`saveForm.php`页面上捕获的变量名直接相关。当表单执行`POST`操作时，第 37 行将触发`done()`。在此函数内部，jQuery 选择器用于在第 39 行选择`success`模态框。调用`modal()`函数使其对用户可见。

如果表单无效，在第 43 行，使用 jQuery 选择器选择`error_message` div 标签。`div`标签的 HTML 内容被设置为`error`变量的内容。

```javascript
1 <script>
2 $( "#submit" ).click(function(event) {
3     event.preventDefault();
4     var error = '';
5 
6     var email = $("#emailAddress").val();
7     if(email == ""){
8         error += 'Please enter your e-mail address<br>';
9     }
10     var fullName = $("#fullName").val();
11     if(fullName == ""){
12         error += 'Please enter your full name<br>';
13     }
14     var serviceRating = $("#serviceRating").val();
15     if(serviceRating == ""){
16         error += 'Please rate the service<br>';
17     }
18     var foodRating = $("#foodRating").val();
19     if(foodRating == ""){
20         error += 'Please rate the food<br>';
21     }
22     var atmosRating = $("#atmosRating").val();
23     if(atmosRating == ""){
24         error += 'Please rate the atmosphere<br>';
25     }
26     var comments = $("#comments").val();
27     if(atmosRating == ""){
28         error += 'Please add a comment<br>';
29     }
30 
31     if(error === ""){
32         // if the form if valid
33         $.post( "saveForm.php", { type: "register", email:email,
```

## 示例代码：`saveForm.php`

**样本代码 18**概述了将表单数据保存到数据库表中的 PHP 脚本。该页面标题为`saveForm.php`。在第 2 行，首先从`$_POST`变量中提取`type`变量。如果`POST`中包含术语`register`，则会在第 4 行调用`registerNewUser()`函数。在该函数的内部，利用 JavaScript`POST`提交的每个使用`$_POST`的变量均会从 PHP`$_POST`提取出来，并放置到局部变量中（第 7–12 行）。

在收集完所有变量后，从第 13 行开始添加`try-catch`机制。（在此过程中）数据库调用在第 8 行执行。在第 40 行的 PHP 变量`sql`包含要插入到`servicerating`表中的原始 SQL 语句。其中包含了数据库中每个单独列的引用，随后跟随六个问号（`?`），这些被视为占位符，用于使用第 26–31 行中绑定的变量的`bindParam()`函数。

在 SQL 已准备完毕且变量已通过附加后，可以在第 45 行执行对`execute()`函数的调用来插入记录到数据库中。

```php
<?php
$type = $_POST['type'];
if($type == 'register'){
    registerNewUser();
}
function registerNewUser(){
    $email =           $_POST['email'];
    $fullName =       $_POST['fullName'];
    $serviceRating = $_POST['serviceRating'];
    $foodRating =     $_POST['foodRating'];
    $atmosRating =    $_POST['atmosRating'];
    $comments =       $_POST['comments'];
    try {
        $host = 'localhost';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DACO';
        $DBH = new PDO("mysql:host=$host;dbname=$dbname",
            $user, $pass);

        $sql = "INSERT INTO `servicerating` (`email`, `fullName`,
                                       `serviceRating`, `foodRating`,
                                       `atmosRating`, `comments`)
                                       VALUES (?,?,?,?,?,?);";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $email, PDO::PARAM_STR);
        $sth->bindParam(2, $fullName, PDO::PARAM_STR);
        $sth->bindParam(3, $serviceRating, PDO::PARAM_INT);
        $sth->bindParam(4, $foodRating, PDO::PARAM_INT);
        $sth->bindParam(5, $atmosRating, PDO::PARAM_INT);
        $sth->bindParam(6, $comments, PDO::PARAM_STR);
        $sth->execute();
    } catch(PDOException $e) {echo $e;}
}
?>
```

**样本代码 18：**`saveForm.php`——用于将表单数据保存到数据库表的 PHP。

## 输出

在图 **2.6** 中，可以看到完成的布局表单。**图 45** 概述了用户在提交表格后显示给用户的模态框。

**邮箱地址**

*输入 email*

我们绝不会与任何人分享您的电子邮件。

**完整姓名**

*填写全名*

请输入您的全名。

**您如何评价我们的服务？**

**您对食物有多满意？**

**餐厅的氛围如何？**

*请告诉我们您的经历*

**提交按钮**

> **图 2.6：**已完成的响应表单。

## 48 ■ 使用 JavaScript 和 PHP 收集和分析用户数据的应用

![](img/ed4cb7e1be98f0adec0546edd14f6223_62_0.png)

*图 4.6：提交表格后显示给用户的 Bootstrap 模态框。*

## 2.6 总结

本章提供了通过二进制选项、星级评分和具有客户端验证的自定义表单提示用户直接收集活跃数据的示例。虽然来自用户的原始数据质量非常高，但在大规模数量上收集这些数据的过程可能会很困难。

为了在不进行直接交互的情况下更多地了解用户的数据，可以使用被动集合机制。[第 3 章](#chapter-3)概述了这些方法。

### 被动数据采集

被动数据是指无需与用户互动即可在后台收集的数据。这对于从用户处获取广泛的洞察力非常有用（例如：他们来自何处、他们的兴趣以及目前用来访问应用程序的环境）。

在本章中，我们探讨了识别不同数据来源和数据格式的过程；通过自定义解决方案和第三方工具探索了从这些用户中提取有意义的见解的方法过程。

#### 3.1 引言

虽然可以存储用户与 Web 应用的所有交互记录，但并非所有这些都可能对分析有用。为了防止出现重复数据的情况，一种简单方法是将数据仅存储在预定义操作的结果之后。**可触发数据存储的操作包括：**

- 多次查看特定产品；
- 浏览属于相似类别的产品；
- 购买特定产品。

在评估要存储哪些数据时，应考虑用户与给定产品或分类之间的连接有多具体。例如：一位用户在书籍集合中搜索后决定购买玩具。**虽然**购买一本书将被认为是一个具体的联系（即他们执行了我们想要的操作），应该对此类更强调此类联系。（注：此处原文逻辑似乎有误，“As buying a book would be considered a concrete connection... greater emphasis should be put on this connection”应理解为“如果用户搜索书籍但最终购买了玩具，那么购买本书这一行为才是‘具体连接’；若只浏览相似主题的图书则不同。”）

与之相反的情况是：也许该浏览器只是在浏览所有主题相似的书籍。如果能向用户提供关于同一主题的候选书籍进行分析的结果可能对未来销售很有益。**这些是如何推断出来的将在后续章节中进行探讨**。

无论数据来源如何，大多数数据都有一个共同的组成部分：时间维度的元素；例如，**记录时间的数据长度**可以被视为与正在进行的分析过程相关。

#### 3.2 Cookie 和会话

在 Web 开发的早期阶段，`Cookies`被用作存储一小段用户浏览器信息的默认方法。随着网络的发展，这种使用 Cookie 的方法很快就被过时而转向使用服务器端`Sessions`来存储更多数据的能力。虽然`Sessions`已在 Web 应用开发中司空见惯，但 Cookie 并未被淘汰。例如：当 PHP 创建新的服务器端会话时，此过程中会在用户的浏览器内保存一个 cookie 以识别其当前关联的会话。典型的服务器端`Session`可能仅持续 30—60 分钟；但在用户浏览器中存储的 Cookie 可以存在得久得多。

然而，Cookies 可靠性会受到质疑：注重隐私的用户通常会阻止应用程序在其网页浏览器中存放 Cookies。当用户删除他们的浏览器历史记录时，这通常包括网站留下的 cookies。此时，用户与该服务器上特定数据集之间的关联就被破坏了。

#### 示例 1：客户端 cookie——简单的设置和获取

Cookies 是一种简单的方法来存储用户在 Web 浏览器的数据。此数据在客户端上保存而不对服务器造成开销。为了帮助处理与 Cookie 的交互过程，使用了`js-cookie`库[^sup-4]。要包含这些功能，需要使用内容分发网络（CDN）来提供当前版本的 JavaScript 文件。`Cookies`类可用来设置和检索 Cookie 信息。

> 1. https://github.com/js-cookie/js-cookie

#### 示例代码：`cookies.html`

在样本代码 35 中，第 42 行的`set()`函数接受两个参数：第一个名为`name`（即我们访问值的键），后面是第二个名叫`John`的参数表示该值。Cookie 创建完成后，可以使用第 37 行上的`get()`函数来获取给定 Cookie 名称的值。此值被放置到局部变量`name`中；第 40 行的`name`变量被输出至浏览器控制台中显示：

```html
<script src="https://cdn.jsdelivr.net/npm/js-cookie@2/src/
    js.cookie.min.js"></script>
<script>
 Cookies.set('name', 'john');  
 var name = Cookies.get('name'); 
console.log(name);
</script>
```

**SAMPLE CODE 1：**`cookies.html`——单个 Cookie 值的设置和获取。

#### 输出

若要访问 Google Chrome 的开发者控制台，可按住`Ctrl+Shift`并按下`J`键。**图 3.2**所示为一个从 cookie 中检索到的单个变量被打印到控制台的输出结果。



![](img/ed4cb7e1be98f0adec0546edd14f6223_65_0.png)

**图：** 正在从 Cookie 中提取的值。

[^sup-4]: https://github.com/js-cookie/js-cookie

可以对 `set()` 函数进行修改，以包含 Cookie 的过期天数。在此示例中，Cookie 将持续七天。

```javascript
Cookies.set('name', 'value', { expires: 7 });
```

也可以将 Cookie 的可见域传递给 `set()` 函数。

```javascript
Cookies.set('name', 'value', { domain: 'site.com' });
```

要删除此 Cookie，需要提供 Cookie 的 `name`（名称）和 `domain`（域）。这种方法可以防止意外删除错误的 Cookie。

```javascript
Cookies.remove('name', { domain: 'site.com' });
```

### 示例 2：客户端 Cookie —— JSON 内容

虽然可以为每条需要存储的不同信息创建不同的 Cookie，但 Cookies 库提供了存储 JSON 内容的能力。这在需要存储多个变量时特别有用。

### 示例代码：cookies_json.html

在示例代码 2 中，第 6 行创建了一个名为 `info` 的 JSON 对象，其中包含一个名为 `pageOfInterest` 的变量，其值设置为 `homeware`。

一旦 JSON 内容被存储在 Cookie 中，第 7 行调用了 `getJSON()` 函数，按名称返回 JSON 对象。调用 `getJSON()` 的结果存储在一个名为 `json` 的局部变量中。可以使用标准的点对象表示法从对象中提取感兴趣的属性。在第 8 行，从 `json` 对象中选择了 `pageOfInterest` 属性，并使用标准点表示法（例如 `json` 后跟属性名）将其打印到控制台。

```html
1 <script src="https://cdn.jsdelivr.net/npm/js-cookie@2/src/js.cookie.min.js"></script>
2 <script>
3     Cookies.set('info', { pageOfInterest: 'homeware' });
4     var json = Cookies.getJSON('info');
5     console.log(json.pageOfInterest);
6 </script>
```

示例代码 2：cookies_json.html —— 设置和获取 JSON 内容。

### 输出

图 3.2 展示了正在检索并打印到开发者控制台的 JSON 内容。

![](img/ed4cb7e1be98f0adec0546edd14f6223_67_0.png)

图 3.2：设置和获取 JSON 值。

### 示例 3：客户端 Cookie —— 迭代 JSON

前面的示例在 JSON 字符串中存储了一个属性。在下面的示例 JSON 中，它包含两个 `pageOfInterest` 属性，用于存储用户正在查看的内容类型的引用。

```json
1 [{
2         "pageOfInterest": "homeware"
3 },
4 {
5         "pageOfInterest": "cooking"
6 }
7 ]
```

### 示例代码：iterate.html

此示例包含一个文件和两个库：

1. `iterate.html` —— 此文件设置 JSON 内容，然后对其进行迭代。
2. Cookies 库 —— 用于与 Cookie 交互。
3. jQuery —— 用于迭代 JSON 内容。

在示例代码 3 中，第 1 行引入了 Cookie 库。第 3 行，为了处理此 JSON，以 CDN 引用的形式包含了 JavaScript jQuery[^2] 库。第 7 行，Cookies 的 `set()` 函数用于存储 JSON 内容。JSON 存储后，第 9 行可以使用 `getJSON()` 函数检索它，该函数接受一个值，用于标识要检索的 Cookie 名称。此 JSON 在第 10 行传递给 jQuery 的 `each()` 函数。这使我们能够迭代 JSON 内容。

在函数的每次迭代中，可以使用名为 `this` 的引用来指向当前正在处理的对象。可以使用点表示法一次访问一个 `pageOfInterest` 属性，并将其打印到浏览器控制台。

```html
1 <script src="https://cdn.jsdelivr.net/npm/js-cookie@2/src/
2     js.cookie.min.js"></script>
3 <script src="https://code.jquery.com/jquery-3.5.1.min.js">
4     </script>
5 <script>
6 // Storing and retrieving JSON
7 Cookies.set('info', [{"pageOfInterest": "homeware"},
8         {"pageOfInterest": "cooking"}]);
9 var json = Cookies.getJSON('info');
10 jQuery.each(json, function() {
11     console.log(this.pageOfInterest);
12 });
13 </script>
```

示例代码 3：iterate.html —— 设置和获取可迭代的 JSON 内容。

[^2]: https://jquery.com

### 输出

图 3.3 展示了从 JSON 中检索并迭代后打印到浏览器控制台的值。

![](img/ed4cb7e1be98f0adec0546edd14f6223_69_0.png)

图 3.3：迭代 JSON 值。

### 示例 4：客户端 Cookie —— 自定义追加函数

从 Cookie 中读取 JSON 后，它将被转换为 JavaScript 对象。在应用程序的任何阶段，如果我们想用额外的 JavaScript 数据更新此 JSON，可以使用 `push()` 函数追加到 JSON。

此示例包含一个文件和两个库：

1. `appending.html` —— 此文件使用自定义函数设置 JSON 内容。
2. Cookies 库 —— 用于与 Cookie 交互。
3. jQuery —— 用于迭代 JSON 内容。

### 示例代码：appending.html

在示例代码 4 中，第 8 行在 `info` 变量中设置 JSON，然后在第 10 行从同名的 Cookie 中读取。`json` 变量可用作将来添加内容的存储位置。

第 12 行添加了一个名为 `addItem()` 的函数。第 13 行向该函数添加了 `push()` 函数，允许通过函数调用将新对象追加到 JSON 中。这种方法有助于模块化推送过程，允许在存储数据前根据需要对其进行额外的安全检查。要向 JSON 追加数据，在第 16 行调用 `addItem()` 函数，并传递一个要存储的字符串。在此示例中，追加了单词 baking。

第 18 行使用 jQuery 的 `each()` 函数迭代完整的 JSON 对象，将三个值打印到浏览器控制台。

```html
<script src="https://cdn.jsdelivr.net/npm/js-cookie@2/src/js.cookie.min.js"></script>

<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>

<script>
// Storing and retrieving JSON
Cookies.set('info', [{"pageOfInterest": "homeware"}, {"pageOfInterest": "cooking"}]);
var json = Cookies.getJSON('info');
// Using a function to add to JSON
function addItem(item){
  json.push({"pageOfInterest": item});
}
// call the function
addItem("baking");
// view all
jQuery.each(json, function() {
  console.log(this.pageOfInterest);
});
</script>
```

示例代码 4：appending.html —— 用于向现有 JSON 对象添加 JSON 内容的自定义函数。

### 输出

图 3.4 展示了调用自定义 `addItem()` 函数后的输出。

在使用 JavaScript 时，对变量所做的所有修改在页面刷新或用户导航到不同页面时都会丢失。因此，应实现定期保存过程，不仅将内容添加到浏览器中的对象，还要添加到 Cookie 中以实现持久化。

![](img/ed4cb7e1be98f0adec0546edd14f6223_71_0.png)

图 3.4：使用自定义 JavaScript 函数添加的 JSON。

### 示例 5：服务器端会话 —— 存储变量

作为在用户网络浏览器中存储信息的后续方案，可以使用服务器端 PHP 会话。此会话包含两个元素：一个留在用户网络浏览器中的小 Cookie，其中包含正在使用的 PHP 会话的 `ID` 号；以及服务器上与该 `ID` 对应的存储数据。在每个网页的开头，都会调用 `session_start()` 函数。如果会话存在，它将恢复；如果会话不存在，则开始一个新会话。创建会话后，我们可以通过创建新的会话变量简单地将数据存储在会话中。

### 示例代码：session.php

在示例代码 5 中，存储在会话中的变量标题是 `samplevariable`，如第 3 行所示。附加到此变量的值设置为 `Sample Value`。第 4 行检索唯一的会话 `ID` 并将其放置在一个局部变量中。此变量在第 5 行打印到浏览器。

```php
1 <?php
2 session_start();
3 $_SESSION['samplevariable'] = 'Sample Value';
4 $id = session_id();
5 echo $id;
6 ?>
```

示例代码 5：session.php —— 在 PHP 会话中设置单个字符串变量。

### 输出

图 3.5 展示了已生成并输出到 Web 浏览器的唯一会话 ID。

`9geckbbatmsb3gnlf9oqdd7l5o`

**图 3.5：** 唯一会话 ID 显示在 Web 浏览器中。

## 示例 6：服务器端会话——存储数组

会话也可用于保存较大量的数据。一个简单的例子是包含三个值的数组。存储在数组中的值不需要是相同的数据类型。

### 示例代码：session_arrays.php

在示例代码 6 中，第 3 行创建了一个名为 `myArray` 的数组，包含三个值。在第 4 行，通过将该数组的引用赋值给会话变量 `$contactinfo`，将数据存入了该会话变量。在第 5 行，从会话中获取了 `contactinfo` 变量的值。由于该引用包含一个数组，在获取值时必须提供目标元素的位置编号。`contactinfo` 会话数组的第一个元素存储在位置 `[0]`。

```php
<?php
session_start();
$myArray = array("John Smith", 18, "8222555");
$_SESSION['contactinfo'] = $myArray;
echo $_SESSION['contactinfo'][0];
?>
```

**示例代码 6：** session_arrays.php — 在 PHP 会话中设置数组。

### 输出

在下方图 3.6 中，由于访问了数组的位置 `[0]`，`John Smith` 这个名字将被打印在 Web 浏览器中。

`John Smith`

**图 3.6：** 从存储在会话中的数组输出到浏览器的文本。

存储在 PHP 会话中的所有数据仅在服务器管理员定义的时间段内存在，例如 30、60、90 分钟等。因此，如果我们希望让这些数据持久保存更长时间，就必须使用数据库或静态文件。会话通常用于存储已登录系统的用户信息。当用户退出系统时，相应的会话将被销毁。这可以通过调用 `session_destroy()` 函数来完成，如示例代码 7 第 6 行所示。

```php
<?php
1 session_start();
2 $myArray = array("John Smith", 18, "8222555");
3 $_SESSION['contactinfo'] = $myArray;
4 echo $_SESSION['contactinfo'][0];
5 session_destroy();
6 ?>
```

**示例代码 7：** session_destroy.php — 使用后销毁 PHP 会话。（为清晰起见修正了标题）

## 3.3 从文件中读取

我们之前描述的所有数据收集解决方案都围绕在线应用程序。在许多情况下，数据是使用未集成到现有应用程序中的其他工具收集的。例如，数据可能是使用文本文件、电子表格或允许将数据导出为通用格式（如逗号分隔值文件）的应用程序手动收集的。在接下来的章节中，我们将探讨这些不同的格式，并描述如何提取数据以供利用。

### 示例 7：将文件上传到 Web 服务器

本示例使用一个库：

1. jQuery File Upload 插件 —— 此库用于为文件上传过程提供现代化的外观和体验。

将文件上传到 Web 服务器需要两个组件。第一个组件是用户界面上传工具，第二个是服务器端代码，用于接收文件并将其放置到服务器上所需的位置。将文件上传到 Web 服务器的过程可以使用非常简单的 HTML 和少量的服务器端 PHP 代码来完成。然而，这个过程无法向用户提供有关上传状态的任何额外信息，也无法提供现代 Web 应用程序中预期的上传器外观和体验。

在这个示例中，我们将使用众多 HTML/JavaScript 文件上传库之一以及服务器端 PHP 代码。本示例使用了 jQuery File Upload 插件[^3]。从网站下载源代码 zip 文件并解压后，可以看到如图 3.7 所示的文件夹结构。

可以在该文件夹的根目录中找到一个名为 `index.html` 的文件，如图 3.8 所示。它提供了上传工具功能的最小示例。

尽管显示了额外的功能，但可以修改此演示，移除本示例不需要的元素。由于 `index.html` 页面负责提供用户文件上传体验的流程，所有额外的处理都在服务器端使用 PHP 执行。在 `/server/php/` 文件夹内，可以找到一个名为 `UploadHandler.php` 的文件。此文件包含文件上传过程的所有配置，允许我们指定文件存储位置以及对文件上传过程施加的限制。由于此文件较大，为简洁起见，此处不提供完整内容。

### 示例代码：UploadHandler.php

此示例中描述的完整代码可在示例代码中查看。在 `UploadHandler.php` 文件的第 104 行，可以看到对上传过程中允许的原始文件格式的引用。这些最初设置为允许上传图像格式。

[^3]: https://blueimp.github.io/jQuery-File-Upload

```php
'accept_file_types' => '/\.(gif|jpe?g|png)$/i',
```

由于我们处理的是文本文件和 CSV 文件，我们将用所需的文件扩展名替换这些。

```php
'accept_file_types' => '/\.(txt|csv)$/i',
```

当文件成功上传到服务器时，它会被放置在 `/server/php/files` 文件夹内。出于安全原因，在此文件夹内使用 `.htaccess` 文件来防止用户在 Web 浏览器中执行这些文件，例如，当用户上传 PHP 文件时，他们将无法在服务器端运行该 PHP 文件。通过手动将文件名（例如 `server/php/test.csv`）输入到 Web 浏览器中，将无法检索到该文件。

在此文件中，我们可以看到文件默认上传的路径。它指向用于引用当前文件上传目录的 `$SCRIPT_FILENAME`，后跟文件文件夹。`$upload_url` 引用的是文件的 URL。

```php
'upload_dir' => dirname($this->get_server_var('SCRIPT_FILENAME')).'/files/',
'upload_url' => $this->get_full_url().'/files/',
```

为了提高安全性，建议将上传的文件放置到非 Web 可访问的目录中。要将文件放入 Web 服务器的 `E:/sample/` 文件夹，我们可以简单地对 `$upload_dir` 变量进行如下修改。

```php
'upload_dir' => 'E:/sample/',
```

如果文件已存在于服务器上，系统会自动为其分配不同的名称。然而，为了提供唯一的文件名，可以对位于同一文件夹第 1143 行的 `$handleFileUpload()` 函数进行轻微修改。在示例代码 8 中，MD5 哈希函数被传递了一个引用来获取当前日期。

这是通过调用 `$date()` 函数获取的。`Y-m-d H:i:s:u` 指定了日期的格式。其后是一个句点和一个对扩展名变量的引用。此扩展名变量使用 PHP 的 `$pathinfo()` 函数检索原始文件扩展名。



```php
$extension = pathinfo($name, PATHINFO_EXTENSION);
$file->name = md5(date('Y-m-d H:i:s:u')) . '.' . $extension;
```

**示例代码 8**：修改`UploadHandler.php`文件，以基于 MD5 算法提供唯一文件名。（修正了函数/文件名的拼写）。

将文件上传到 Web 服务器时，文件夹权限常常会引起问题。上传文件的文件夹，例如`/files/`，需要具有允许 PHP 写入的权限。在共享主机环境中工作时，如果看到与权限相关的错误，可能需要审查权限设置。添加像`777`这样的文件夹权限总是被视为不良做法。应在文件夹上设置最少的必要权限，以允许文件上传，但又不能完全开放，以免被恶意用户滥用。

## 示例 8：来自 Google 表单的 CSV 文件

CSV 文件被广泛使用，因为它们允许以简单的格式存储数据，例如，文件中的一行对应一条单独的记录，而文件中不同的列对应那条记录的不同数据片段。使用逗号来分隔列。CSV 文件以纯文本形式存储，不需要任何特殊的库或工具来读取内容。因此，它们已成为广泛使用的数据存储格式。

一个例子是在线数据收集工具，如 Google 表单$^{[[https://www.google.com/forms/about](图 3.9)]}$`[[1]]`和 SurveyMonkey$^{[[https://www.surveymonkey.com](图 3.9)^\wedge]}$。这两种工具都提供了将收集到的所有数据下载为简单 CSV 文件的功能。在**图 3.9**中展示了一个简单的 Google 表单，其中包含一个允许用户输入电子邮件地址的字段和另一个允许用户选择“是”或“否”的字段。虽然这是一个简单的例子，但可以轻松扩展以包含额外的自定义字段。

在 Google 表单的“响应”选项卡下，右上角显示了三个点，如**[[图 3.10]]**所示，提供了可以对表单数据执行的操作列表。

在**[[图 3.11]]**中，选择了“下载响应”选项以导出使用当前表单收集的数据。在此示例中，有一条单独的响应被添加到了表单中。从此界面导出的文件不是简单的 CSV 文件，而是压缩的 Zip 文件，其中包含 CSV 文件。这在数据提取过程中增加了一个额外的处理步骤，因为文件必须先解压。

54 ■ 使用 JavaScript 和 PHP 的应用用户数据收集与分析

图 3.9：Google 表单示例。

图 3.10：Google 表单导出选项。

### 输出

图 3.12 展示了使用 Google 表单收集数据生成的 CSV 文件示例。该文件包含两条独立记录。文件的第一行是列名。在本例中，列名是表单中每个问题的文本。其下方是两行独立的数据。文件中每一列都使用逗号分隔，因此该文件格式被称为逗号分隔值（CSV）。为了方便用户分析，每一行的第一列包含一个唯一的日期/时间戳，随后是每个问题的单独数据。

![图 3.11：Google 表单下载 CSV 回复。](img/ed4cb7e1be98f0adec0546edd14f6223_79_0.png)

```csv
"Timestamp","Are you happy with our service?","How likely are you to return to our site?"
"2019/07/25 6:32:04 pm CET","Yes","10"
"2019/07/25 6:32:09 pm CET","No","5"
```

图 3.12：Google 表单 CSV 文件示例。

### 示例 9：从 CSV 文件读取

虽然这只是 CSV 文件的一个非常小的示例，但无论使用多少条记录，处理过程都是相同的。由于使用逗号分隔每一行，并使用引号标注每个值，因此它可以轻松地被 PHP 脚本处理。

### 示例代码：`read_csv.php`

示例代码 9 开始处理 CSV 文件，在第 2 行调用`fopen()`函数。该 PHP 文件假设要读取的 CSV 文件位于 Web 服务器上 PHP 脚本的旁边。否则，必须输入 CSV 文件的完整路径。`r`标志表示我们希望从文件中读取。`fopen()`调用被放在一个简单的`if`语句中，以确保可以建立到文件的连接。这是通过检查文件引用不等于`false`来实现的。

在第 3 行，建立连接后，使用`while`循环来迭代文件中的每一行。调用`fgetcsv()`函数。该函数接受一个我们要读取 CSV 内容的文件的引用，后跟`1000`，表示文件中一行的最大长度。其后是文件的分隔符。分隔符是用来分割文件中单独列的标记的名称。由于我们处理的是 CSV 文件，因此将使用简单的逗号作为分隔符。

与上一个示例中的`if`语句类似，`while`循环有一个保护机制，确保当返回的值等于`FALSE`时停止从文件读取。

对于`while`循环的每次迭代，在第 4 行，使用`echo`语句打印包含一行完整数据的`data`变量的内容。传递一个键来标识我们想要显示的该行中的单独列。在 PHP 中使用句点将每个单独的字符串连接成一个完整的字符串，然后回显到浏览器。由于我们要输出到网页，因此必须使用 HTML 标签来换行。在第 7 行，文件处理完毕后，关闭对文件的引用。

```php
1 <?php
2 if (($file = fopen("data.csv", "r")) !== FALSE) {
3     while (($data = fgetcsv($file, 1000, ",")) !== FALSE) {
4         echo $data[0] . " --- " . $data[1] . " --- " . $data[2] .
5              '<br>';
6     }
7 fclose($file);
8 }
9 ?>
```

示例代码 9：`read_csv.php`——使用 PHP 读取 CSV 文件。

### 输出

图 3.13 展示了 PHP 从 CSV 文件读取并将内容输出到浏览器的结果。在此输出中，打印存储在位置 0 的第一列。其后是该行的位置 1 和位置 2。

### 示例 10：从文本文件读取

从文本文件读取与从 CSV 文件读取非常相似。CSV 文件与纯文本文件的主要区别可能是缺乏格式。文本文件中的每一行都被视为一条单独的记录。该记录不再进一步细分为单独的列。

### 示例代码：`read_text.php`

在示例代码 10 中，首先在第 2 行创建了一个`if`语句。这是为了确保可以建立到文本文件的连接。如果找不到文件，则将返回`FALSE`。否则，可以开始从文件中读取单独行的过程。

在第 3 行，使用`while`循环来迭代文件中的每一行。使用`feof()`函数检查文件结束字符。如果未找到，则循环将继续迭代每一行。其开头的`!`用于表示不是文件结尾，则继续循环。在此`while`循环内部，创建了一个单独的`line`变量。该变量的内容在第 4 行使用`fgets()`函数读取。该函数用于从文件指针获取一行。该函数被传递已打开文件的引用。在第 5 行，使用简单的`echo`语句将该行打印到浏览器。其后是一个`br`标签，用于在浏览器中换行。在第 7 行，调用`fclose()`函数来关闭对文件的引用。

```php
<?php
if (( $file = fopen("textfile.txt", "r")) != FALSE) {
while ( !feof($file)) {
    $line = fgets($file);
    echo $line . '<br>';
}
fclose($file);
}
```

示例代码 10：`read_text.php`——使用 PHP 从纯文本文件读取并打印到 Web 浏览器。

---

Timestamp --- Are you happy with our service? --- How likely are you to return to our site?

2019/07/25 6:32:04 pm CET --- Yes --- 10

2019/07/25 6:32:09 pm CET --- No --- 5

图 3.13：CSV 文件内容输出到浏览器。

### 输出

图 3.14 展示了从文本文件读取并输出内容到浏览器的三行内容。由于使用了`br`标签进行换行，因此文本文件中的每一行都以相同的格式在浏览器中输出。

图 3.14：从文本文件读取的三行单独内容输出到浏览器。

## 3.4 用户 IP 地址

用户的 IP 地址可以提供大量关于用户及其访问应用程序所用环境的知识。IP 地址也可以被视为识别单个用户的独特方式。

虽然可以使用 IP 地址来确定哪些用户经常访问您的网站，但还需要记住，大多数互联网服务提供商（ISP）并不会为所有用户提供固定 IP 地址。通常，当用户重新连接到互联网时，他们会获得一个新的 IP 地址。大型公司也是如此，公司内部有许多不同的用户都在同一个网络上工作。他们内部可能都有不同的 IP 地址，但对外他们都使用相同的 IP 地址。

虽然这是识别一般用户群的有用方法，但不应将其作为区分网站用户的唯一方法。用户的 IP 地址对开发人员来说仍然有用，可以收集一些关于单个用户或用户群的基本信息。

获取用户 IP 地址主要有两种方法，第一种是使用服务器端编程语言来访问 IP，第二种是使用实现此功能的服务。使用服务的好处是所有工作都是自动执行的，并且可以使用 JavaScript 轻松访问 IP 地址。

### 示例 11：用户 IP 地址——Web 浏览器 URL 调用

在本示例中，我们将使用 IPify。这是众多第三方服务之一，为开发人员提供检索用户 IP 地址的能力。

### 示例代码

此方法基于对单个 URL 的`GET`请求。当调用此 URL 时，会显示用户的 IP 地址。当使用 Web 浏览器打开 URL`https://api.ipify.org?format=json`时，将返回一个简单的 JSON 文档。

### 输出

图 3.15 展示了在 Web 浏览器中输入 URL 时返回的 JSON 文档。该文档包含一个简单的键值对，其中`ip`是键，值是用户的 IP 地址。

```json
{"ip":"193.1.39.1"}
```

图 3.15：JSON 格式的 IP 地址。

## 示例 12：用户 IP 地址——JavaScript `GET`请求

在上一个示例中，IP 地址是通过在 Web 浏览器中输入 URL 时执行的`GET`请求返回的。要自动执行相同的过程，可以使用 JavaScript`GET`请求。

此示例包含一个文件和一个库：

- jQuery——用于执行到服务的`GET`请求。
- ipify.org——该服务接受`GET`请求并返回用户的 IP 地址。

### 示例代码：`get_ip.php`

示例代码 11 描述了将此功能集成到应用程序中的过程。在第 1 行，包含 jQuery。在第 4 行，添加了用于包裹发往 Web 服务的`getJSON()`请求的文档`ready`函数的快捷方法。

另外还有一个名为`format`的附加参数通过 URL 传递。该参数用于告诉 Web 服务我们希望以哪种格式获取响应。

在本示例中，我们传递了`format`参数并将其设置为`JSON`。此调用将返回包含访客 IP 地址的 JSON 结构化文档。

在第 5 行，一旦向服务发出调用，IP 地址将存储在一个名为`ip`的本地变量中。

此变量的一个简单用途是：在从用户收集数据的过程中，可以在数据库内部放置一个附加列，用于存储用户的 IP 地址以及收集到的数据。

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js">
    </script>
<script>
$(function() {
    $.getJSON("https://api.ipify.org?format=json",
        function(json) {
            var ip = json.ip;
            console.log(ip);
        }
    );
});
</script>
```

**示例代码 11：**`get_ip.php`——使用第三方服务获取用户的 IP 地址。

### 示例 13：用户 IP 地址——用户“是/否”选择和 IP 地址

本示例包含三个文件和一个库：

1. `create.sql`——用于创建`yesnolog`数据库表。
2. `yesno_ip.html`——此文件向用户提供“是/否”选项，并收集其 IP 地址。
3. `ajax.php`——此文件接收结果及 IP 地址，并将数据保存到数据库表中。
4. jQuery——用于检索 JSON，并使用 jQuery 选择器访问元素。

**被动数据收集 ■ 61**

### 示例代码：`create.sql`

```sql
1 CREATE TABLE `yesnolog` (
2     `id` INT(11) NOT NULL AUTO_INCREMENT,
3     `articleid` INT(11) NOT NULL DEFAULT '0',
4     `result` INT(11) NOT NULL DEFAULT '0',
5     `ipadd` VARCHAR(50) NOT NULL DEFAULT '0',
6         PRIMARY KEY (`id`)
7 );
```

**示例代码 12：**`create.sql`——创建`yesnolog`表。

### 示例代码：`yesno_ip.html`

在示例代码 13 中，使用 HTML 单选按钮向用户展示“是/否”选项。在第 1 行，包含对 jQuery CDN 的引用。随后是第 3 行和第 4 行分别对应的两个输入字段，一个用于“是”，一个用于“否”。

第三个是`result`，它用于存储用户选择“是”或“否”选项的结果。传递的最后一个变量是`ip`，其中包含来自全局变量的值，该值是通过向 Web 服务进行初始调用而收集到的 IP 地址。

在执行 POST 之后，在第 23 行调用了`.done()`函数，该函数包含一个简单的`alert`语句以通知用户。

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js">
	</script>
<input type="radio" name="answer" value="Yes"> Yes  <br>
<input type="radio" name="answer" value="No">  No   <br>
<script>
$( "input:radio[name=answer]" ).click(function() {
	var val = $(this).val();
	saveAnswer(val);
});
var ip = '';
$(function() {
	$.getJSON("https://api.ipify.org?format=json",
	function(json) {
		ip = json.ip;
	}
	);

});
var ip = 0;
function saveAnswer(answer){
	$.post( "ajax.php", { type: "yesno", articleid: "1221",
		result: answer, ip:ip })
	.done(function( data ) {
		alert('Thank you!');
	});
}
</script>
```

**示例代码 13：**`yesno_ip.html`——向用户展示用于收集其 IP 地址的“是/否”选项。

### 输出

图 3.16 展示了向用户呈现的“是/否”单选按钮。

![](img/ed4cb7e1be98f0adec0546edd14f6223_87_0.png)

图 3.16：向用户展示的“是/否”选项。

### 示例代码：`ajax.php`

为了处理数据，添加了第二个名为`ajax.php`的页面。在该页面顶部第 2 行显示了（修正为显示）`type`变量。

使用一个简单的`if`语句将发出的请求导向第 3 行的正确函数。在第 4 行调用了名为`yesNoLog()`的 PHP 函数。在此函数的第 7—9 行内，从使用 JavaScript 发送的 PHP`POST`中提取三个变量。每个变量都被放置在本地 PHP 变量中。

在收集数据之后，在第 10 行添加了一个`try-catch`语句。在此内部，在第 15 行创建了到数据库的连接。使用连接，在第 16 行创建一个带有问号的新的`INSERT`语句以占位符对应值。为了将值与添加的问号进行匹配，在第 20、21 和 22 行调用了`bindParam()`函数。最后，在第 23 行调用了`execute()`函数。如果在数据库 INSERT 期间发生错误，在第 24 行添加了`catch`以捕获任何错误消息并显示给浏览器。

```php
1 <?php
2 $type = $_POST['type'];
3 if($type == 'yesno'){
4 yesNoLog();
5 }
6 function yesNoLog(){
7 $articleid = $_POST['articleid'];
8 $result = $_POST['result'];
9 $ip = $_POST['ip'];
10 try {
11 $host = 'localhost';
```

64 ■ 应用用户数据收集和分析：使用 JavaScript 和 PHP



```php
12 $dbname = 'bookexamples';
13 $user = 'sampleuser';
14 $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
15 $DBH = new PDO("mysql:host=$host;dbname=$dbname",
16     $user, $pass);
17 $sql = "INSERT INTO `yesnolog` (`articleid`,
18     `result`, `ipadd`) VALUES (?, ?, ?);";
19 $sth = $DBH->prepare($sql);
20 $sth->bindParam(1, $articleid, PDO::PARAM_INT);
21 $sth->bindParam(2, $result, PDO::PARAM_STR);
22 $sth->bindParam(3, $ip, PDO::PARAM_STR);
23 $sth->execute();
24 } catch(PDOException $e) {echo $e;}
25 }
26 ?>
```

**示例代码 14：**`ajax.php`——将单选按钮选择和 IP 地址保存到数据库表。

### 输出

图 3.17 显示了用户点击“是”或“否”后显示的结果消息。由于插入数据库记录的过程是通过 JavaScript 完成的，因此没有输出可见给用户。

![](img/ed4cb7e1be98f0adec0546edd14f6223_88_0.png)

图 3.17：选择“是”或“否”后显示给用户的消息。

## 3.5 查找用户代理（FINDING THE USER AGENT）

随着智能手机和其他设备的出现，市面上有许多不同的网络浏览器。在网站开发期间，重要的是要确保网站已在使用不同版本的浏览器进行了彻底测试。尽管一个网站在一个环境中可查看并不意味着它适用于所有环境。通常用于增强用户体验的许多工具，例如 JavaScript，在不同的浏览器中经常表现出不寻常的行为。

### 示例 14：查找用户代理

本示例由两个文件和一个库组成：

1. `user_agent.html`——此文件用于通过 JavaScript 获取用户的 IP 地址。
2. `user_agent.php`——此文件用于通过 PHP 获取用户的 IP 地址。
3. `jQuery`——此库用于使用 JavaScript 获取用户的 IP 地址。

获取更多信息的一种方法是使用用户代理（`user agent`）。目前存在多种不同的库，允许开发人员在应用程序中集成用户代理识别。`jQuery` 库提供有用的函数来辅助此开发过程。

**示例代码：**`user_agent.html`

在示例代码 15 中，第 1 行使用 `script` 标签首先在 PHP 脚本中包含 `jQuery` 库。在第 4 行，获取了用户代理。在第 5 行，可以使用简单的 `console.log()` 查看 `UserAgent` 变量。

```html
1 <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
2 <script>
3   var agent = navigator.userAgent;
4   console.log(agent);
5 </script>
```

**示例代码 15：**`user_agent.html`——使用 `jQuery` 检索用户代理。

### 输出

图 3.18 提供了一个用户代理打印到浏览器控制台的示例。

![](img/ed4cb7e1be98f0adec0546edd14f6223_90_0.png)

图 3.18：打印到控制台的 `user agent`（用户代理）。

### 示例代码：`user_agent.php`

使用 PHP 代码检查用户代理是 JavaScript 的另一种方法。示例代码 16 显示了向包含对 `HTTP_USER_AGENT` 引用的 `$_SERVER` 数组进行简单调用的调用。

```php
<?php
echo $_SERVER['HTTP_USER_AGENT'];
?>
```

**示例代码 16：**`user_agent.php`——使用 PHP 检索用户代理。

### 输出

图 3.19 显示了 PHP 用户代理变量的示例。

`Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/71.0.3578.98 Safari/537.36`

图 3.19：`user_agent.php`——使用 PHP 检索用户代理。

## 3.6 用户地理位置

任何在互联网上构建和部署的应用程序，通常不仅仅服务于一小部分用户。互联网的全球性为未来业务带来了机遇，这些机遇在网站初始开发阶段可能被忽视了。识别应用程序的目标受众通常非常有趣，因为尽管你服务的是一个特定群体，但可能会发现来自其他地理区域的用户流量访问了你的应用。

网络上存在许多不同的服务，用于收集当前查看页面的用户信息。当通过在谷歌地图上输入经纬度进行检查时，会发现我们获取的并非用户的精确位置，而通常是用户所在位置的大致信息。尽管人们认为 IP 地址是唯一标识符，但 IP 地址并没有可供第三方服务查询的物理地址。

## 示例 15：`geolocation-db.com`

为辅助开发过程，可以使用 `geolocation-db.com` API。该 API 允许通过 GET 请求将单个 IP 地址传递给服务。服务会返回一个 JSON 结构的文档，其中包含与该 IP 地址相关的地理位置信息。

本示例包含一个文件和两个库：

1. `geo.html`——此文件用于调用服务。
2. `jQuery`——用于选择单个 `span` 标签并更新其值。
3. `geolocation-db.com`——该服务基于单个 IP 地址提供地理信息。

### 示例代码：`geo.html`

在示例代码 17 中，第 1 行首先调用并引入了 `jQuery`。第 3 至 8 行使用单独的 `span` 标签作为从 API 检索的变量的占位符。`span` 标签最初创建时不需要值。一个重要的元素是每个 `span` 标签的唯一 ID。

添加 `span` 标签后，下一步是在第 10 行向 `geolocation-db.com` 的 URL 发起 AJAX 调用。这里没有使用 JSON，而是使用了 JSONP。这是 JSON 但带有填充（padding）。这与传统请求不同，因为跨域调用不是问题。

调用成功后，会有一个名为 `location` 的对象可用。该对象包含用户的国家、州、城市、纬度和经度。此外，用户的 IP 地址也可用。这些属性可以通过访问对象 `location`，后跟一个点号，再跟上感兴趣的变量名来获取。

在第 15 至 20 行，使用 `jQuery` 选择器选中之前创建的每个 `span` 标签。对选择器调用 `.html()` 函数，将 `span` 标签的值更新为 `location` 对象中当前选定变量的值，例如 `country_name`。

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js">
    </script>
<div>Country: <span id="country"></span></div>
<div>State: <span id="state"></span></div>
<div>City: <span id="city"></span></div>
<div>Latitude: <span id="latitude"></span></div>
<div>Longitude: <span id="longitude"></span></div>
<div>IP: <span id="ipv4"></span></div>
<script>
$.ajax({
    url: "http://geolocation-db.com/jsonp",
    jsonpCallback: "callback",
    dataType: "jsonp",
    success: function(location) {
        $('#country').html(location.country_name);
        $('#state').html(location.state);
        $('#city').html(location.city);
        $('#latitude').html(location.latitude);
        $('#longitude').html(location.longitude);
        $('#ipv4').html(location.IPv4);
    }
});
</script>
```

示例代码 17：`geo.html`——检索用户位置信息。

### 输出

图 3.20 展示了收集到并显示在 `span` 标签中的地理位置信息示例。

![](img/ed4cb7e1be98f0adec0546edd14f6223_93_0.png)

图 3.20：地理位置信息示例。

## 示例 16：`ipstack.com`

另一个能够从用户 IP 地址收集信息的服务是 `IpStack`。⁸ 与之前允许匿名 API 调用的服务不同，此服务要求用户提供有效的 API 密钥。此密钥用作项目唯一标识符，通常与计费相关，当请求数量超过免费基础套餐时会触发。

本示例包含一个文件和两个库：

1. `geo.html`——此页面用于向 `ipstack.com` 网络服务发起请求。
2. `jQuery`——此库用于向 `ipstack.com` 发起 AJAX 请求。
3. `ipstack.com`——提供关于给定 IP 地址信息的网络服务。

当从服务收到免费的 API 密钥后，可以将其添加到 URL 中，例如：`http://api.ipstack.com/193.1.39.1?access_key=XXXXXXXXXXXXXXX`，其中 X 用唯一的 API 密钥替换。添加到此 URL 的 IP 地址可以是我们希望探索的任何 IP 地址。如果在浏览器中打开此 URL，将输出一个 JSON 文档。

### 输出

图 3.21 展示了调用 `ipstack.com` 网络服务后的输出。尽管难以阅读，但它是一个有效的 JSON 文档。

```json
{"ip":"193.1.39.1","type":"ipv4","continent_code":"EU","continent_name":"Europe","country_code":"IE","country_name":"Ireland","region_code":"L","region_name":"Leinster","city":"Blanchardstown","zip":"D15","latitude":53.3881,"longitude":-6.3756,"location":{ ... }}
```

图 3.21：浏览器中以 JSON 格式显示的地理信息。

### 示例代码：`geo.html`

在示例代码 18 中，第 1 行引用了 `jQuery` CDN。第 4 行和第 5 行创建了两个变量，一个包含我们希望查找更多信息的 IP 地址，另一个包含我们 `ipstack.com` 账户的唯一 API 密钥。

第 6 行执行了一个 `jQuery` AJAX 调用到 API URL。将 IP 地址和访问密钥变量添加进去，创建完整的调用 URL。使用 JSONP 作为调用方法以允许跨源请求。

请求完成后，会调用 `success` 属性旁边的函数。该函数包含一个名为 `json` 的单独对象引用，其中包含服务器的响应。在此对象内部的第 11 行，引用了 `location`。在这个 `location` 对象内部，可以调用单个属性，例如 `capital`。这些属性及其错误代码的完整列表可在官方文档中找到。⁹

```html
1 <script src="https://code.jquery.com/jquery-3.5.1.min.js">
2     </script>
3 <script>
4 var ip = '193.1.39.1'
5 var access_key = '34dd357a733f2142f58b1bada9f9f394';
6 $.ajax({
7     url: 'http://api.ipstack.com/' + ip + '?access_key=' + access_key,
8     dataType: 'jsonp',
9 });
```

⁹ <https://ipstack.com/documentation>

```html
success: function(json) {
    console.log(json.location.capital);
}
});
</script>
```

示例代码 18：`geo.html`——向 `ipstack.com` 网络服务发起 AJAX 请求。

### 输出

`Dublin`

图 3.22：与该 IP 地址关联的当前位置被打印到控制台。

## 3.7 页面停留时间

衡量用户与 Web 应用程序交互的一个简单但有效的方法是记录用户在页面或页面各部分停留的时间。本示例使用 `TimeMe.js`¹⁰ 库。该库可从 <https://github.com/jasonzissman/TimeMe.js> 下载。下载 ZIP 文件后应解压，以访问 `timeme.js` JavaScript 文件。

## 示例 17：`TimeMe.js` 实现

`TimeMe.js` API 提供了一系列工具，允许开发者识别用户在网页上花费的时间。如果用户切换到不同的选项卡、最小化窗口，或停止键盘或鼠标交互，计时器将停止。

本示例包含一个库和一个文件：

1. `time.php`——此页面包含 `TimeMe.js` 库的一个实例。
2. `TimeMe.js`——此库提供了记录用户与网页交互时间的能力。可从其网站¹¹ 获取。

¹⁰ <http://timemejs.com>

¹¹ <https://github.com/jasonzissman/TimeMe.js/>

### 代码示例：`time.php`

在示例代码 19 的第 1 行，添加了包含主库的 `timeme.js` 文件的引用。在第 3 行，执行了计时器的初始化。在初始化代码（第 4 行）内部，添加了一个简单的引用名称，以唯一标识使用计时器的页面。在第 5 行，添加了超时时间段，例如，计时器在一段时间空闲后应该停止的时间。

为了辅助未来的数据分析，在第 7 行添加了一个触发器，用于在一段时间后执行。在此示例中，触发器设置为 4 秒。

```html
1 <script src="timeme.js"></script>
2 <script type="text/javascript">
3     TimeMe.initialize({
4         currentPageName: "my-home-page", // current page
5         idleTimeoutInSeconds: 3 // seconds
6     });
7     TimeMe.callAfterTimeElapsedInSeconds(4, function() {
8         console.log("The user has been using the page for
9             4 seconds!");
10    });
11 </script>
```

示例代码 19：`time.php`——带有 elapsed time（经过时间）的计时器示例。

### 输出

如图 3.23 所示，当经过 4 秒后，输出被打印到控制台。

该用户已在页面上使用了 4 秒！

图 3.23：四秒后控制台输出。

通过识别经过时间何时发生，如果需要在特定时间间隔内，可以检索当前页面的数据（如输入字段的值）并将其存储在数据库中。这通常是一个有用的过程，因为用户可以填写表单或搜索字段，但可能不完成按下提交按钮的过程。在这种情况下，如果没有计时器触发日志记录过程，数据将会丢失。

## 3.8 跟踪各个 `div` 标签

Web 应用程序的每个区域通常被分解为各个 `div` 标签。应用程序的每个不同区域可能代表一个关键功能，例如，特定的 `div` 标签专门用于内容，而另一个 `div` 标签被指定为搜索功能。

### 示例 18：使用 `TimeMe.js` 跟踪 `div` 标签

此示例包含一个库和一个文件：

1. `time.php`——此页面包含 `TimeMe.js` 库的一个实例。
2. `TimeMe.js`——此库记录用户与网页的交互。

与前面的示例类似，要使用 `TimeMe.js`，必须下载 `TimeMe.js` JavaScript 文件并将其放置在当前脚本旁边。

### 代码示例：`time.php`

在示例代码 20 的第 8 行，可以使用主计时跟踪工具的一个变体来关注单个感兴趣区域花费的时间。在此示例中，使用了 `trackTimeOnElement` 函数，并专注于 `area-of-interest-1` `div` 标签。在第 9 行，使用 `setInterval()` 函数每 100 毫秒重复执行内部代码。

在第 10 行，创建了一个名为 `timeSpentOnElement` 的新变量，其值设置为在 `textarea-of-interest-time-1` `span` 标签上花费的时间。在第 12 行，使用 `document.getElementById()` 函数检索 `area-of-interest-time-1` 并设置内容为元素上花费的时间。调用 `timeSpentOnElement.toFixed()` 函数并传入值 5。这表示在打印时间时应包含多少位小数。



```html
<script src="timeme.js"></script>
<script type="text/javascript">
    TimeMe.initialize({
        currentPageName: "my-home-page", // current page
        idleTimeoutInSeconds: 5, // stop recording time due to
        inactivity
    });
    window.onload = function(){
        TimeMe.trackTimeOnElement('area-of-interest-1');
        setInterval(function(){
        var timeSpentOnElement =
            TimeMe.getTimeOnElementInSeconds
            ('area-of-interest-1');
        document.getElementById('area-of-interest-time-1').
            textContent = timeSpentOnElement.toFixed(5);
        }, 100);
    }
</script>
<div class="area-of-interest" id="area-of-interest-1">
    Interact with this element<br/><br/>
    Interaction: <span id="area-of-interest-time-1"></span>
    seconds.
</div>
```

示例代码 20：`time.php` — 记录在单个 `div` 标签上花费的时间量。

### 输出

图 3.24 显示了 Web 浏览器中的输出，描述了用户在各个 `div` 标签上花费的时间量。

![](img/ed4cb7e1be98f0adec0546edd14f6223_98_0.png)

图 3.24：用户在 `div` 标签上花费的秒数。

虽然实时查看用户在某页面特定部分花费的时间很有用，但为了未来的分析，将这些信息存储在数据库中也是有用的。在此操作之前，为了模块化代码，首先创建一个自定义函数，该函数在用户离开当前页面时触发。

### 示例 19：在卸载时调用自定义函数

为此，我们将创建一个自定义函数，该函数将在用户离开当前页面时被调用。页面上所有活动的计时器都将停止，并收集值并将其存储在数据库表中。如果用户移动到应用程序内的内部页面，或手动输入不同网站的 URL，此函数将被触发。

### 代码示例：`time.php`

在示例代码 21 中，首先在第 2 行将 JavaScript `addEventListener` 绑定到 `window`。添加的事件类型名为 `beforeunload`。每当用户尝试导航到不同页面时，都会触发此事件。在此函数（第 3 行）中，调用了一个名为 `timingDataStore()` 的自定义函数。函数定义包含在第 8 行。在事件监听器（第 4 行）中，返回类型设置为 `undefined`。这确保在页面重定向时不会提示用户。

```javascript
<script>
window.addEventListener('beforeunload', function (e) {
    timingDataStore();
    return undefined
});

// Customer logging function
function timingDataStore(){
    console.log("goodbye...")
}
</script>
```

示例代码 21：`time.php` — 当用户离开页面时调用 JavaScript 函数。

### 输出

[图 3.25](#) 显示了当用户离开当前页面时打印到控制台的输出。要查看此消息，在 Google 开发者控制台中，点击右侧的齿轮，然后点击 `Preserve log`（保留日志）选项。

```text
goodbye...
```

**图 3.25：** 当用户离开当前页面时打印到控制台的文本。

### 示例 20：保存到数据库表

在前面的示例中，虽然我们可以知道用户何时离开了页面，但没有将任何计时记录在数据库表中。在此示例中，描述了将记录保存到数据库表的过程。

此示例包含三个文件和两个库：

1. `timinglog.sql` — `timinglog` 创建表的 SQL。
2. `timing.php` — 收集来自浏览器的计时日志。
3. `ajax.php` — 用于接收计时数据并将其存储在数据库表中。
4. jQuery — 用于向 `ajax.php` 页面执行 JavaScript `POST` 请求。
5. `TimeMe.js` — 用于记录用户与应用程序之间的计时。

### 代码示例：`timinglog.sql`

示例代码 22 概述了名为 `timinglog` 的数据库表的 SQL，这是必需的。这包含一个 `ID` 列来标识每条记录，以及一个自动添加的时间戳列，名为 `timelogged`。`user` 字段可以包含任何额外的信息来以用户名、`ID` 或 IP 地址的形式标识用户。`pageID` 列用于持有应用程序中任何给定页面的唯一 `ID`。

为了辅助未来的检索，添加了两个示例键值对属性。在此示例的情况下，`att1` 将是页面上花费的总时间，如果需要，`att2` 可用于其他变量。

`timing1` 和 `timing2` 列用于存储为每个记录的值。

```sql
CREATE TABLE `timinglog` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `timelogged` TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `user` VARCHAR(50),
    `pageID` VARCHAR(50),
    `att1` VARCHAR(50),
    `timing1` VARCHAR(50),
    `att2` VARCHAR(50),
    `timing2` VARCHAR(50),
    PRIMARY KEY (`id`)
);
```

示例代码 22：`timinglog` 数据库表。

### 代码示例：`timing.php`

在示例代码 23 的第 1 行，包含了对 jQuery CDN 的引用。在第 5 行，添加了对本地 `TimeMe.js` 库的引用。在第 9 行，为当前正在运行代码的页面赋予一个唯一的名称。这将在稍后用于识别记录来自何处。在第 12 行，添加了事件监听器，该监听器将在用户离开当前页面时触发。在第 13 行，包含了对 `timingDataStore()` 函数的核心调用。在第 17 行，添加了 `timingDataStore()` 函数的定义。为了找出用户在当前页面上花费了多长时间，在第 18 行调用了 `getTimeOnCurrentPageInSeconds()` 函数。

在此函数进一步进展之前，在第 20 行调用了 `console.log()` 以将信息输出到 Web 浏览器的开发者控制台。这确保我们正确收集时间，因此可以排除 `TimeMe.js` 库的任何问题。在收集数据并触发事件后，表明用户已离开当前页面。在第 23 行对 `ajax.php` 页面执行 AJAX 请求以将数据存储到数据库表中。在此过程中，我们先收集时间，然后对数据处理页面执行 AJAX `POST` 请求。

此页面的名称为 `ajax.php`。`POST` 请求首先包含我们要发送的请求 `type`。在此情况下，我们发送 `timelog` 作为值，后跟 `key-pair`（键值对）属性。其中第一个是 `pageTitle`，其值设置为 `TimeMe.js` 页面 `ID`。接下来是两个属性，第一个是用户在页面停留的总时长，第二个是为将来可能需要而预留的额外键值对占位符。虽然本示例仅展示了两个属性，但可以扩展为同时发送多个属性和值。

在第 28 行，当执行 POST 请求后，会调用 `.done()` 函数的回调，向用户显示 `Bye!` 文本。

```javascript
1 <script
2   src="https://code.jquery.com/jquery-3.5.1.min.js"
3   integrity="sha256-9/aliU8dGd2tb6OSuzixeV4y/faTqgFtohetphbbj0="
4   crossorigin="anonymous"></script>
5 <script src="timeme.js"></script>
6 <script type="text/javascript">
7   // Initialize library and start tracking time
8   TimeMe.initialize({
9     currentPageName: "my-home-page", // current page
10    idle utilizeTimeoutInSeconds: 3 // seconds
11  });
12  window.addEventListener('beforeunload', function (e) {
13    timingDataStore();
14    return undefined;
15  });
16  // Custome logging function
17  function timingDataStore(){
18    var timeSpentOnPage = TimeMe.getTimeOnCurrentPageInSeconds();

20    console.log('Time on Page:' + timeSpentOnPage);

22    // Send data to the server here
23    $.post( "ajax.php", { type: "timelog", pageTitle:
24        TimeMe.currentPageName,
25                              att1name: 'totaltime', att1:
26                                  timeSpentOnPage,
27                              att2name: 'interest', att2: '0' })
28    .done(function( data ) {
29      alert("Bye!");
30    });
31 }
32 </script>
```

### 代码示例 23：`timing.php` —— 调用 `timingDataStore()` 函数进行 AJAX `POST` 请求以存入数据库。

### 代码示例：`ajax.php`

在服务器端，我们有一个名为 `ajax.php` 的页面。该页面的第一步是通过获取第 2 行的 `type` 变量来解析我们发送的请求类型。在本示例中，JavaScript 发送的值为 `timelog`，因此我们将在第 3 行使用简单的 `if` 语句检查 `type` 变量，并在第 4 行调用 PHP 的 `timeRecordLog()` 函数。在第 6 行的 `timeRecordLog()` 函数内部，我们首先从执行的 `POST` 请求中提取每条数据。这些数据包括 `pageTitle`、`attribute 1` —— 名称和值，以及 `attribute 2` —— 名称和值，如第 7–11 行所示。

在第 19 行，使用 PDO 对象建立与 MySQL 数据库的连接。第 21 行添加 `INSERT` 语句。对于每个参数，在语句的右侧放置一个问号。这些参数通过第 25–29 行的 `bindParam()` 函数填充。此过程的最后一步是在第 30 行使用 `execute()` 执行 SQL 语句，将数据 `INSERT` 到数据库中。`try catch` 语句始终包围着数据库连接，因为如果在连接过程或 `INSERT` 语句期间出现问题，catch 将处理错误，防止脚本崩溃。

```php
1 <?php
2 $type = $_POST['type'];
3 if($type == 'timelog'){
4     timeRecordLog();
5 }
6 function timeRecordLog(){
7     $pageID = $_POST['pageTitle'];
8     $att1name = $_POST['att1name'];
9     $att1time = $_POST['att1'];
10    $att2name = $_POST['att2name'];
11    $att2time = $_POST['att2'];
12
13    try {

15        $host = 'localhost:3306';
16        $dbname = 'bookexamples';
17        $user = 'sampleuser';
18        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
19        $DBH = new PDO("mysql:host=$host;dbname=$dbname",
20            $user, $pass);
21        $sql = "INSERT INTO `timinglog` (`pageID`, `att1`, `timing1`,
22            `att2`, `timing2`)
23        VALUES (?,?,?,?,?);"
24        $sth = $DBH->prepare($sql);
25        $sth->bindParam(1, $pageID, PDO::PARAM_STR);
26        $sth->bindParam(2, $att1name, PDO::PARAM_STR);
27        $sth->bindParam(3, $att1time, PDO::PARAM_STR);
28        $sth->bindParam(4, $att2name, PDO::PARAM_STR);
29        $sth->bindParam(5, $att2time, PDO::PARAM_STR);
30        $sth->execute();
31    } catch(PDOException $e) {echo $e;}
32}
```

### 代码示例 24：`ajax.php` —— 将计时器值记录到 `timinglog` 数据库表中。

图 3.26 展示了当用户离开当前页面时，记录到数据库中的五次计时结果。我们可以看到 `timing1` 列包含了在页面上花费的总时长。

| id | timelogged | user | pageID | att1 | timing1 | att2 | timing2 |
|---|------------|------|--------|------|---------|------|---------|
| 1 | 2020-06-23 12:04:59 | 0 | my-home-page | totaltime | 2.073 | interest | 0 |
| 2 | 2020-06-23 12:06:07 | 0 | my-home-page | totaltime | 3.148 | interest | 0 |
| 3 | 2020-06-23 12:27:38 | 0 | my-home-page | totaltime | 2.352 | interest | 0 |
| 4 | 2020-06-23 12:27:44 | 0 | my-home-page | totaltime | 2.073 | interest | 0 |
| 5 | 2020-06-23 12:27:50 | 0 | my-home-page | totaltime | 3.256 | interest | 0 |

### 图 3.26：记录到数据库表中的示例计时数据。

## 3.10 用户来源

### 示例 21：使用 `HTTP_REFERER` 变量

另一种收集数据的方法是利用 PHP 库中存在的函数。其中最著名的是 `HTTP_REFERER` 变量。该变量允许你查明用户是从应用程序中的哪个页面来到当前页面的。

### 示例代码：`ref.php`

为了收集数据，首先添加 PHP 起始标签，然后在第 2 行使用 `HTTP_REFERER` 变量。添加简单的 `echo` 语句将值输出到浏览器。然而，有时该变量可能未被设置，导致脚本显示警告消息。为防止这种情况，示例代码可以包裹在 PHP 的 `isset()` 函数中，在输出之前检查该变量是否存在。

```php
1 <?php
2 if(isset($_SERVER['HTTP_REFERER'])){
3     echo $_SERVER['HTTP_REFERER'];
4 }
5 ?>
```

### 代码示例 25：`ref.php` —— 将 PHP `HTTP_REFERER` 输出到网页浏览器。

### 输出

**图 3.27** 展示了从一个页面导航到另一个页面后的输出结果。列出的页面是用户Previously viewed page。

![调用 PHP REFERRER 变量的输出结果](img/ed4cb7e1be98f0adec0546edd14f6223_105_0.png)

### 图 3.27：调用 PHP REFERRER 变量的输出结果。

## 3.11 社交媒体内容采集



社交媒体为数据分析师提供了对用户实时意见变化的额外洞察。Facebook 和 Twitter 等社交媒体平台允许用户输入他们的想法，并添加额外的关键标识符，如话题标签（hashtags）和 @ 提及（@ mentions），这些可以用来识别他们正在提及的公司以及他们对这些公司的情感态度。在本节中，我们将探讨创建一个工具来抓取特定 Twitter 页面内容的过程。

在选择用于分析的社交媒体数据源时，必须首先解决的障碍是查看内容是否需要身份验证。社交媒体网站的许多不同组成部分都可以公开访问，无需登录。其他来源，如 Facebook 群组，可能设置为私密，需要用户账户登录并被接受加入群组后，才能开始提取过程。

### 示例 23：基于 Twitter 库的订阅源提取

本示例需要一个文件和一个库：

1. `twitteroauth` —— 这是用于与 Twitter API 交互的主要库。
2. `twitter_auth.php` —— 这是将使用库执行 API 请求的示例应用程序。

在本节中，介绍了使用众多可用库之一与 Twitter API 集成的方法。在本节中，我们将回顾 `twitteroauth` 库。

要在本地服务器上安装此库，我们将使用 `composer`。[^13] 从命令提示符，使用 `cd` 命令进入项目所在的文件夹。

进入文件夹后，我们可以开始初始化 `composer` 的过程。这是通过运行 `composer init` 命令完成的。运行此命令后，需要输入项目名称、项目描述、项目目录类型、许可证和项目作者。必须定义项目的稳定性。在本示例中，我们将其设置为 `dev`。

最后，定义开发依赖项。在本示例中，我们可以选择 `no`。在此过程结束时，系统将要求你确认将在项目文件夹中创建的 `composer.json` 文件内容。图 3.28 展示了一个示例 `composer.json` 文件。

创建 `composer.json` 文件后，我们可以开始添加所需的其他库。为此，在项目文件夹根目录的命令提示符中输入以下命令。

```bash
composer require abraham/twitteroauth
```

此过程将开始下载并将库安装到项目中，如图 3.29 所示。

[^12]: https://github.com/abraham/twitteroauth
[^13]: https://getcomposer.org

![](img/ed4cb7e1be98f0adec0546edd14f6223_107_0.png)

## 图 3.28：新项目的 `composer.json` 示例内容

```text
Using version dev-master for abraham/twitteroauth
./composer.json has been updated
Loading composer repositories with package information
Updating dependencies (including require-dev)
Package operations: 1 install, 0 updates, 0 removals
  - Installing abraham/twitteroauth (dev-master 9350ad1): Cloning 9350ad14d5 from cache
Writing lock file
Generating autoload files
```

## 图 3.29：Composer 库安装控制台输出

要访问 Twitter API，需要创建多个不同的 Web 端点。每个不同的端点都是一个独立的 URL，接受各种不同的参数。由于 Twitter API 是商业工具，提供了不同的套餐计划，例如标准版（Standard）和高级版（Premium）。在本例中，我们将使用标准版计划。我们将重点关注的 API 组件是搜索 API（Search API），可以在 API 文档中找到相关信息。[14]

在开始与 API 交互之前，需要一个 Twitter 账户。此外，还必须向 Twitter 注册一个新的应用程序，说明该应用程序的用途。要注册此应用程序，可以使用 Twitter 网页上的应用控制台（app console）。[15]在该页面上，可以看到创建应用（Create an app）的选项。

[14]: https://developer.twitter.com/en/docs/tweets/search/api-reference/get-search-tweets
[15]: https://developer.twitter.com/en/apps

84 ■ Applied User Data Collection and Analysis Using JavaScript and PHP

在此过程中，会添加关于应用程序的基本信息。此过程中添加的关键要素是回调 URL。该回调 URL 的目的是允许 Twitter OAuth 流程将验证信息发送回我们服务器上的页面。

应用程序注册完成后，可以查看为该应用程序创建的密钥（keys）和令牌（tokens）。这些对于应用程序来说是唯一的，可以作为 Twitter 服务器识别该项目的标识符。这些令牌将被添加到代码中，以协助完成认证过程。

标准搜索 API 有一些限制。这些限制包括：用户在 15 分钟内只能执行 180 次请求，而应用程序在 15 分钟内可以执行 450 次请求。¹⁶

## 示例代码：`twitter_auth.php`

库安装完成后，我们可以开始创建一个新的 PHP 文件，用于与该库进行交互。添加到该文件的第一行是我们所用 PHP 库的自动加载，如示例代码 26 第 2 行所示。

库导入项目后，我们可以在第 4-7 行添加消费者密钥（consumer key）、消费者密钥（consumer secret key）和应用程序的回调（callback）URL。这为我们提供了与服务器认证所需的信息。认证完成后会调用回调，并向我们提供验证状态信息。

我们可以创建库的一个新实例，连同我们的唯一凭证。完成此操作后，我们将在第 8 行调用 `oauth()` 函数访问 Twitter API，以接收一个唯一的请求令牌，该令牌将随我们未来向 API 发出的所有请求一起发送。

唯一访问令牌生成后，我们可以开始向服务器发出请求。在本例中，我们将在第 12 行向搜索 API 发出请求。向服务器执行一个 `GET` 请求，传递我们希望使用的 API 功能的名称。API 的每个不同组件都会有不同的可用参数集合。这些参数使我们能够微调返回给我们的结果。在下面的示例中，我们通过传递查询参数 `q` 并将其值设置为 `Dublin` 来搜索推文。

¹⁶https://developer.twitter.com/en/docs/tweets/search/api-reference/get-search-tweets.html

更有趣的可用参数之一是 `result_type`。这使我们能够指定应返回哪种类型的结果。这些结果类型包括：`mixed`（混合），提供热门和实时响应；`recent`（最近），仅显示最近的结果；以及 `popular`（热门），仅返回最热门的结果。要添加此参数，只需添加一个简单的逗号即可。

`results` 变量将包含来自服务器的完整响应。在第 15 行，要遍历结果，可以使用 `for each` 语句。该语句接收 `results` 对象，后跟对 `statuses` 的引用。我们可以遍历每条单独的推文，并提取所需的属性。在本例中，我们提取推文创建的时间和推文包含的文本。

```php
1 <?php
2 require_once 'vendor/autoload.php';
3 use Abraham\TwitterOAuth\TwitterOAuth;
4 define('CONSUMER_KEY', '1wUmYQ6c2GQFh7j7CIYhyaJ6R');
5 define('CONSUMER_SECRET', 'yPHBqqT9o1lppggiscj0yAjutRclS6s');
6 define('OAUTH_CALLBACK', 'https://www.kylegoslin.ie/test.php');
7 $connection = new TwitterOAuth(CONSUMER_KEY, CONSUMER_SECRET);
8 $request_token = $connection->oauth('oauth/request_token',
9                             array('oauth_callback' => OAUTH_CALLBACK));
10 $results = $connection->get("search/tweets",
11                            ["q" => "Dublin",
12                            "result_type"=> "popular"]);
13 foreach($results->statuses as $tweet){
14     echo $tweet->created_at . '-'. $tweet->text . '<br>';
15 }
```

示例代码 26：`twitter_auth.php` — Twitter 库访问及遍历推文

### 输出

图 3.30 显示了调用 Twitter 搜索 API 的示例输出。在这些结果中，首先打印日期，后跟一个短横线，然后是来自单条推文的文本。

```text
Mon Nov 04 19:27:08 +0000 2019-Dublin, we can't wait to experience the energy of tonight with you. https://t.co/Hny0TOZIFa

Sun Nov 03 19:08:16 +0000 2019-Cheers Dublin ❤️ https://t.co/5z8JyWkYQb

Mon Nov 04 15:26:21 +0000 2019-#RIPGayByrne - so supportive of Irish artists. He came to see my first solo show in Dublin for no other reason than… https://t.co/hx9uyYiHOC

Mon Nov 04 13:12:07 +0000 2019-👤 INSTORE ALBUM SIGNINGS 📍 Manchester, Birmingham, Belfast and Dublin. To gain entry, you MUST purchase a copy of… https://t.co/SD5L6biphJ

Mon Nov 04 15:43:45 +0000 2019-Such sad news. #GayByrne brought wisdom, mischief & deep curiosity into my Dublin home as a child. His… https://t.co/AMkfSrX6fL

Mon Nov 04 18:30:31 +0000 2019-A boil water notice has been issued for a second time for people living in parts of counties Dublin, Kildare and Me… https://t.co/mrkpwpel5k

Mon Nov 04 20:47:27 +0000 2019-Paris, Rome and Dublin didn't even make the top ten. Time to get a long weekend booked. 🍸🍸 https://t.co/bs7qaEJrlp

Mon Nov 04 19:25:58 +0000 2019-Fans in a frenzy as Christina Aguilera stops into Dublin pub before 3Arena gig https://t.co/gevVentalX

Mon Nov 04 15:25:51 +0000 2019-Follow a behind the scenes account from the road over on https://t.co/RvV5p7vUkn - the first two tour blogs are fro… https://t.co/CodZb7MUjB

Mon Nov 04 17:00:30 +0000 2019-Brussels is the youngest capital city in the EU, followed by Paris and Dublin. In contrast, Lisbon is the capital c… https://t.co/31eh2alWJf

Mon Nov 04 17:29:15 +0000 2019-To be in with a chance of winning a pair of tickets to our Irish premiere screening of #LastChristmasMovie and fest… https://t.co/LVxknJSqXj

Mon Nov 04 14:47:56 +0000 2019-Very sad news from Dublin. A legend - the legend - of Irish broadcasting is no more #GayByrne https://t.co/kYCnQLEIN7

Sun Nov 03 19:39:39 +0000 2019-New mural of Lizzo in Dublin 🎨 https://t.co/ZAg6Rmlf6wT
```

## 图 3.30：Twitter API 搜索结果

## 3.12 小结

本章介绍了利用从用户兴趣领域和本地浏览器环境收集的被动数据的概念，无需直接的用户干预。探讨了以 Cookies 和 Sessions 形式的简单数据源，这些包含用户和应用程序留下的短期数据。为了进一步提取洞察，使用了额外的服务来查找用户的地理位置和 IP 地址。随后探讨了服务器端 PHP 以识别用户的来源。然后描述了用户在感兴趣领域花费的时间。为了持久化数据，探讨了将数据保存到数据库表的过程。

以认证 API 调用方式收集数据的替代数据源也得到了探讨，因为许多用户向 Twitter 等服务提供了丰富的知识。接下来的第 4 章将描述创建自定义仪表板的过程，以帮助发现洞察和监控响应。

# 自定义仪表板

第 3 章之前概述了可实施以收集被动数据的机制。在本章中，被动和主动数据源成为数据分析过程的核心焦点。引入活动作为区分数据集的主要方法。这些步骤是使用自定义仪表板执行的，提供对可视化工具和感兴趣的数据源的轻松访问。

## 4.1 引言

在处理数据时，关键组成部分是从任何设备或环境收集数据并以此为有意义的方式向数据分析师提供此数据的能力。（本章）将回顾创建自定义仪表板的流程，该仪表板为数据的收集和 analysed 提供工作空间。可以认为该仪表板是分析师审查数据和启动新数据采集过程的主要门户。

该仪表板包括用户登录门户，允许用户识别系统以及注册页面供新用户激活。用户在登录到系统后，核心仪表板允许用户选择已实施的分析工具和可视化内容。（为了）aid the development process（使用）Bootstrap[^1]作为视觉组件布局期间的核心库。

[^1]: https://getbootstrap.com

## 4.2 用户登录

### 示例 1：用户登录页面

本例由六个文件组成：

1. `create_dashboard.sql` — 此文件用于创建在登录和注册期间使用的数据库表（`dashboard_accounts`）。
2. `bootstrap.js` — 核心 Bootstrap JavaScript 文件。可从其网站[^2]下载。
3. `bootstap.min.css` — 核心 Bootstrap CSS 文件。（可）从 Bootstrap 网站获取。
4. `jquery.min.js` — jQuery 库的压缩版本。可在他们的网站[^3]获得。
5. `index.php` — 此文件是登录过程的主用户界面。使用 Bootstrap 为此页面进行主题设计。
6. `login.php` — 动态使用 jQuery 调用此页面，并通过验证存储在数据库中的凭据来传递和验证用户名和密码哈希值。

[^2]: https://getbootstrap.com/docs/4.0/getting-started/download/
[^3]: https://jquery.com/download/

### 示例代码：`create_dashboard.sql`

要开始登录过程，将创建名为 `dashboard_accounts` 包含账户的数据库表。（如）Sample Code 1所示。该表包含一个自增主键列（ID）。该表中的两个核心列是用户名和密码列。（在）处理密码时，总是记得永远不要以明文形式将密码存储在数据库中。如果发生对数据库的非授权访问，攻击者可能在其他系统上使用相同（的用户名和）密码组合。存储密码的 `哈希` 格式是一种常见做法。哈希是通过传递给返回固定长度字母数字字符串的哈希算法的过程。（然而），如果未实施其他安全措施（如添加 `salt` 盐），则有可能对哈希进行逆向操作以获取原始密码。

```sql
CREATE TABLE `dashboard_accounts` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `username` VARCHAR(100),
    `password` VARCHAR(100),
    `email` VARCHAR(100),
    PRIMARY KEY (`id`)
);
```

样本代码 1：系统的主 `dashboard_accounts` 表。

### 示例代码：`index.php`



用户登录页面是用户访问仪表板之前看到的第一个页面。本节描述完整的登录页面布局。此页面的整体布局基于 Bootstrap。示例代码 2 从第 4 行开始引用 `jQuery`[^4] 库。该引用包含在内，是因为后续将使用它收集用户输入的用户名和密码以进行验证。第 5 行添加了 `Popper`[^5]。这是 Bootstrap 库中的工具提示定位引擎，用于气泡和下拉菜单。为了使用此功能，在第 8 行添加了核心 Bootstrap 库。

[^4]: https://jquery.com/

[^5]: https://popper.js.org/

登录页面的样式保持非常简单。在第 10–16 行，输入字段被设置为延伸至可用空间的宽度。通过添加内边距（`padding`），将文本从输入字段的左侧移开。`margin` 设置为 `8px`，`display` 设置为 `inline-block`。输入字段使用细的 `1px` 实线浅灰色边框。

在第 17–25 行，添加了主登录按钮的样式。颜色设置为白色，`padding` 和 `margin` 设置为特定值。由于这是一枚按钮，当用户将鼠标指针置于其上时，光标将变为 `pointer`。第 27 行设置了鼠标悬停时的效果：按钮的透明度将从初始值 `1.0` 变为 `0.8`。

第 30 行添加了主可见区域 `viewport`。这有助于缩放用户将看到的内容，初始缩放比设置为 `1`。Bootstrap[^6] 提供了更多此类颜色。第 34 行添加了 `div` 标签以包含页面主体中的内容，并将 `class` 设置为 `container`。第 35 行添加了其中的导航栏（`nav`）。该导航栏具有 `bg-light` 颜色和圆角边缘。可以从 Bootstrap 网站获得更多关于这些颜色的信息[^6]。

第 36 行添加了单个链接，其 `class` 设置为 `navbar-brand`。这是标题的主要焦点。`href` 指向 `index.php` 页面，其可见文本设置为 `Feedback Dashboard`。

[^6]: https://getBootstrap.com/docs/4.3/utilities/colors

第 38 行添加了 `main` 标签，并将 `role` 设置为 `main`。其中添加了一个 `class` 设置为 `jumbotron` 的 `div` 标签（第 39 行），为主内容显示提供空间。

在 `Jumbotron` 内，第 40 行添加了带有 `mx-auto` 类的 `div` 标签，允许我们将组件居中。第 42 行添加了简单文本，以指导用户输入用户名和密码。`form` 标签包裹两个 `input` 字段，并将其 `id` 设置为 `login`（第 43 行）。这两个 HTML 输入字段位于第 45 行和第 47 行，并在此前使用 CSS 进行样式设计。此 `ID` 将稍后用于附加事件监听器，以处理表单提交过程。

第 49 行添加了单个 `span` 标签，其 `id` 为 `message`，用作错误消息的默认显示位置，例如表单值不正确时出现的错误，如错误的用户名或密码。

```html
<head>
<link rel="stylesheet" href="Bootstrap.min.css" crossorigin="anonymous">
<script src="jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.3/umd/popper.min.js"
        crossorigin="anonymous"></script>
<script src="Bootstrap.js" crossorigin="anonymous"></script>
<style>
input[type=text], input[type=password] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc,
}
button {
background-color: grey;
color: white;
padding: 14px 20px;
margin: 8px 0:
border: none;
cursor: pointer;
width. 100%;
}
button:hover{
    opacity: Qg,
    
</style> 
<meta name="viewport" content = "width=device-width, initial-scale=1, shrink-to-fit=no">

</head> 
<body > 


<div class="container "> <nav claaa ="navbar na bar-expand-lg navbar light bg-light rounded '>


a class ="nabar-brand"hrefindexphp">Feedback Dashboard"</a></nav><main role = main "div class ="jumbotron".div"class ="mx-auto”style width 30px"h1 login",p,Please enter your username and password tologin."formid=login"<label>

<username</b>Username<b>
<label>Password</label"input type="password"id=password/> <button"type = "submit">Login. span id=message/span/form/divdiv/main>/body
```

示例代码 2：`index.html` — 使用 Bootstrap 创建的仪表板登录页面。

在示例代码 3 中，登录页面的核心功能使用 JavaScript 执行。第一个组件是附加到 `login` 表单上的表单提交监听器（第 58 行）。不同于需要刷新页面的传统表单 `POST`，这里使用 JavaScript 执行表单提交。

第 59 行在表单提交时防止页面发生任何重定向。执行完此操作后，在第 60 行和第 61 行使用 jQuery 选择器分别选择 `username` 和 `password`。`val()` 函数用于从字段中提取值。这些值被放入两个本地变量 `un` 和 `pw` 中。

为了验证输入的详细信息是否正确，第 62 行调用 jQuery 的 `POST` 函数，将 `username` 和 `password` 变量发送到名为 `login.php` 的第二个 PHP 页面。发送到此页面的请求 `type` 被描述为 `login`。这使得单个 PHP 页面可以在将来被重新用于其他任务。

一旦调用 PHP 页面，第 64 行返回 `data` 变量。如果登录凭据正确，该变量将包含一个名为 `success` 的标志。第 67 行将 Web 浏览器的位置重定向到 `dashboard.php` 页面。

如果用户名或密码不正确，第 70 行使用 `span` 标签保存错误消息。这是通过将字符串传递给可在 `span` 标签上调用的 `text()` 函数来完成的。为了帮助调试，在第 68 行和第 72 行添加了两个 `console.log()` 函数。

```javascript
<script>

$( "#login" ).submit(function( event ) {

    event.preventDefault();

    var un = $("#username").val();

    var pw = $("#password").val();

    $.post( "login.php", { type:"login", username: un, password:

      pw })

         .done(function( data ) {

              alert(data);

              if(data == 'success'){

                $(location).attr("href", "dashboard.php");

                console.log('success');

              } else {

                $('#message').text('Login failed, please check

                  your username and password.');

                console.log('failed');

              }

         });

});

</script>
```

> 示例代码 3：`index.html` — 成功登录时重定向到正确页面的 JavaScript 表单监听器。

### 输出

图 4.1 显示了完成的仪表板登录页面。

![](img/ed4cb7e1be98f0adec0546edd14f6223_117_0.png)

图 4.1：登录页面的自定义仪表板。

## 示例代码：`login.php`

为了验证登录详细信息，使用 `login.php` 页面。当在登录页面上执行 JavaScript 表单提交时，`username` 和 `password` 通过 `POST` 发送。

在示例代码 4 中，在开始学习登录过程之前，首先在第 3 行检查 `type` 参数，以查看正在发出的请求类型。当 `type` 设置为 `login` 时，调用 `login()` 函数。

在第 7 行和第 8 行的 `login()` 函数内部，首先从 `POST` 中提取 `username` 和 `password`，并将其放入本地变量中。随后建立与本地数据库的简单连接，以获取所提供 `username` 的记录。在 SQL 中附加了 `LIMIT 1` 子句，以仅从数据库返回一条记录。这在第 16 行中显示，其中 `username` 保留为问号，并在第 19 行使用 `bindParam()` 函数添加 `username`。语句在第 20 行执行。

在返回的记录中，`password` 使用 `bcrypt` 算法进行哈希处理。[^7] 在用户注册过程中，从用户那里收集的密码被传递给密码哈希函数，该函数将返回一个 60 字符的哈希字符串并存储在数据库中。密码 `MySamplePassword` 的字符串示例为 `$2y$10$tLUrTdYnI3B/dsyBtg.lJtDXxEKndyxu5LmRvjwHCSArNpEO`。

可以添加 `Salt`（盐值），这是在注册期间添加到用户密码中的一小段附加文本。此盐值将防止在不同系统上的两个密码之间直接匹配，因为盐值不同。因此，每次生成的哈希将不会相同。

由于我们在密码上使用哈希算法，无法在密码哈希和存储在数据库中的哈希之间进行直接比较。必须在第 22 行调用 `password_verify()` 函数，该函数接受两个参数。第一个是用户输入的原始密码，第二个是从数据库返回的记录中位置 2 返回的哈希值。

当登录成功时，第 25 行启动会话，第 26 行将用户记录中的 `ID` 存储在会话变量 `ID` 中，然后在第 27 行将用户名存储在 `username` 变量中。当登录成功时，单词 `success` 被返回给执行 `POST` 的 JavaScript 函数。这触发调用 `login.php` 页面的原始 JavaScript 重定向到主 `dashboard.php` 页面。

如果密码无效，则触发 `else` 语句，并将文本 `Password is not valid` 返回给用户。

```php
<?php

$type = $_POST['type'];

if($type == 'login'){

    login();

}

function login(){

    $username = $_POST['username'];

    $password = $_POST['password'];

    try {

        $host = 'localhost';

        $dbname = 'bookexamples';

        $user = 'sampleuser';

        $pass = '3C9038A509BE6145A-agent-3B4568AD918BC3DAC0';

}

$DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,

	$pass);

$sql = "SELECT * FROM dashboard_accounts WHERE username

=? LIMIT 1";

$sth = $DBH->prepare($sql);

$sth->bindParam(1, $username, PDO::PARAM_STR);

$sth->execute();

$res = $sth->fetch();

$result = password_verify ($password,$res[2]);

if($result){

	echo 'success';

session_start();

$_SESSION['id'] = $res[0];

$_SESSION['username'] = $res[1];

$_SESSION['valid'] = True;

} else {

	echo 'Password is not valid'

}
```

示例代码 4：`login.php` — 接受用户输入的用户名和密码进行验证。

## 4.3 用户注册

本节将审阅在系统中创建新用户帐户的过程。其界面类似于登录过程。

### 示例 2：用户注册页面

首先，创建名为 `register.php` 的新文件。该文件将为用户提供输入字段，以输入其用户名、电子邮件和密码。此示例包含两个文件和三个库：

1. `bootstrap.js` — 核心 Bootstrap JavaScript 文件，可从其网站获取。
2. `bootstop.min.css` — 核心 Bootstrap CSS 文件，可在 Bootstrap 网站上获取。
3. `jquery.min.js` — jQuery 库的压缩版本，可在其网站上获取<sup>9</sup>。
4. `register.php` — 仪表板的主要注册页面。
5. `ajax.php` — 用于通过 jQuery `POST` 接收注册详细信息并将其保存到数据库。

> 8 https://getbootstrap.com/docs/4.0/getting-started/download/

## 示例代码：`register.php`

示例代码 5 显示了标题为 `register.php` 的注册页面 HTML。该页面将包含用于布局页面的 Bootstrap HTML，以及用于触发注册过程的 JavaScript。

在此文件顶部的第 2 行，包含了对 Bootstrap CSS 文件的引用。随后在第 3 行包含了对 jQuery 库的引用。在第 5 行包含了对 `Popper.js` 的引用，因为它是 Bootstrap 的依赖项。在第 9 行包含了核心 Bootstrap JavaScript 文件。在第 10 行添加了 `meta` 标签作为注册页面的主视口。

随后添加了注册页面的主要样式。输入字段获得最多的样式：在第 13–19 行，将宽度设置为可用空间的 100%。添加 `padding` 和 `margin` 以水平对齐输入字段中的文本。在第 17 行将显示方法设置为 `inline-block`。在第 18 行添加了 `1px` 的浅灰色简单边框。

注册按钮也有少量样式。主要可见的变化是第 26 行的光标。当鼠标放在注册按钮上时，光标变为指针。在第 30 行，当鼠标悬停时，按钮的不透明度从初始的 `1.0` 更改为 `0.8`。

第 35 行添加了 `div` 标签，并将类设置为 `container`。其中添加了导航栏标签，主题设置为 `bg-light`，并在第 36 行设置圆角。

添加导航栏后，下一步是添加页面的主要内容，以允许用户输入其详细信息。第 40 行添加了 `main` 标签作为所有内容的包装器。其中，第 41 行添加了类设置为 `jumbotron` 的 `div` 标签。此组件允许轻松缩放。在其中，第 42 行添加了另一个类设置为 `mx-auto` 的 `div` 标签，将内容自动水平拉伸。随后添加了两段简单文本。

> <sup>9</sup> https://jquery.com/download/

## 示例代码 5：`register.html` —— 用户注册页面 HTML 部分 1

第 45 行添加了一个 `form` 标签，作为该表单的唯一识别方式。

在第 46–53 行，添加了四个输入字段，以收集用户的用户名、电子邮件地址和密码。还添加了第二个输入字段，允许用户确认其密码。密码字段的 ID 分别为 `password1` 和 `password2`，以便后续比较时简单引用。

一个重要的元素是每个元素关联的 `ID` 属性，因为这些属性将在后续使用 JavaScript 处理表单时使用。添加了 `Label` 标签，允许在每个输入字段前指定一段简单文本。为允许开始注册，在第 54 行添加了一个 `submit` 按钮。在第 55 行添加了一个简单的 `span` 标签，标题为 `message`，用作验证过程中可能出现的错误消息的占位符。当页面首次加载时，此 `span` 标签将没有任何值。

```html
1 <head>

2 <link rel="stylesheet" href="Bootstrap.min.css" crossorigin=

3 "anonymous">

4 <script src="jquery.min.js"></script>
```



```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.3/umd/popper.min.js"
        crossorigin="anonymous">
</script>

<script src="Bootstrap.js" crossorigin="anonymous"></script>

<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

<style>
input[type=text], input[type=password] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
}

button {
    background-color: grey;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    cursor: pointer;
    width: 100%;
}

button:hover {
    opacity: 0.8;
}
</style>
</head>

<body>
<div class="container">
    <nav class="navbar navbar-expand-lg navbar-light bg-light rounded">
        <a class="navbar-brand" href="#">Feedback Dashboard</a>
    </nav>

    <main role="main">
        <div class="jumbotron">
            <div class="mx-auto" style="width:300px">
                <h1>Register</h1>
                <p>Register for a new account</p>

                <form id="register">
                    <label><b>Username</b></label>
                    <input type="text" id="username"/>

                    <label><b>E-mail Address</b></label>
                    <input type="text" id="email"/>

                    <label><b>Password</b></label>
                    <input type="password" id="password1"/>

                    <label><b>Repeat Password</b></label>
                    <input type="password" id="password2"/>

                    <button type="submit">Register</button>
                    <span id="message"></span>
                </form>
            </div>
        </div>
    </main>
</div>
```

## 98 应用 JavaScript 和 PHP 进行用户数据收集与分析

### 示例代码 6：`register.html` —— 用户注册页面 HTML 部分 2

在示例代码 6 中，显示了一个自定义模态框。该模态框在应用程序启动时隐藏，仅在新的用户记录成功插入数据库后才可见。在第 61 行，为模态框提供的唯一 ID 设置为`nowRegistered`。在第 66 行，模态框的标题设置为 Success。在第 74–75 行，可以看到用户可见的主要文本。在第 79 行，添加了一个指向包含原始登录页面的`index.php`页面的`href`链接。

```html
<div class="modal" id="nowRegistered" tabindex="-1" role="dialog">
    <div class="modal-dialog" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" style="width:100%">Success</h5>
                <button type="button" class="close" data-dismiss="modal"
                        aria-label="Close"
                        style="width:100px">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>

            <div class="modal-body">
                <p>You are now registered.</p>
                <p>Click to login!</a></p>
            </div>

            <div class="modal-footer">
                <a href="index.php" class="btn btn-primary"
                   role="button">Login!</a>
            </div>
        </div>
    </div>
</div>
```

### 示例代码 7：`register.html` —— JavaScript 注册页面验证部分 3

HTML 组件添加完成后，需要进行表单验证。示例代码 7 概述了此验证过程。为了在提交表单时提供最佳用户体验，将抑制页面的自然重定向过程。为此，我们首先在第 86 行使用 jQuery 选择器选中`register`表单，并添加一个提交处理函数。每当表单提交时，都会调用此函数。

在此函数内部，在第 87 行添加了一个名为`valid`的变量。它用作标志，表示在进一步处理（例如将数据发送到数据库）之前，表单字段是否有效。第二个组件是在第 88 行调用`event.preventDefault()`。这将阻止页面的默认重定向过程。

在第 90 行，使用 jQuery 选择器选中用户名字段。使用`val()`函数提取其值。在第 91 行，检查`un`变量是否为空。如果`username`字段中未输入任何内容，则输入字段将为空，从而允许`if`语句执行。在此`if`语句内部，在第 109 行再次使用 jQuery 选择器选中之前创建的`message` span 标签，并追加消息`Username blank`，后跟一个 HTML `br`标签。这样做是因为`message` span 标签包含一个长字符串，在发生错误时将直接打印到用户的浏览器中。通过添加换行符，每个错误消息将在单独的行上可见。

除了这些基本检查外，第 102 行的`password1`值和第 103 行的`password2`值需要相互比较，且必须匹配。这是为了防止输入密码时的人为错误。在第 108 行，可以使用一个简单的`if`语句，在两个值之间使用`!=`来标识它们是否不相等，从而显示错误消息。

```javascript
<script>
$( "#register" ).submit(function( event ) {
    var valid = true;
    event.preventDefault();

    // Username
    var un = $("#username").val();
    if (un == "") {
        $('#message').append('Username blank.<br>');
        valid = false;
    }

    // Email
    var email = $("#email").val();
    if (email == "") {
        $('#message').append('E-mail blank. <br>');
        valid = false;
    }

    // Password
    var pw1 = $("#password1").val();
    var pw2 = $("#password2").val();

    if (pw1 == "" || pw2 == "") {
        $('#message').append('Password blank.<br>');
        valid = false;
    }

    if (pw1 != pw2) {
        $('#message').append('Sorry your passwords do not match.<br>');
        valid = false;
    }

    // If valid, then perform the post request
    if (valid == true) {
        $.post("ajax.php", {
            type: "register",
            username: un,
            password: pw1,
            email: email
        })
        .done(function(data) {
            if (data == 'registered') {
                // Show modal
                $("#nowRegistered").modal();
            } else {
                $('#message').text('Sorry registration failed.');
            }
        });
    }
});
</script>
```

在注册过程的任何阶段，如果任何字段不正确，`valid`变量将被设置为 false。这用于跟踪表单字段，并查看提交过程是否可以继续到下一部分。在我们执行 POST 操作之前，第 114 行使用了一个`if`语句来确保`valid`变量等于 true。之后，在第 115 行，执行 jQuery POST 到`ajax.php`页面。用户名、密码和电子邮件被发送到第二个页面。当第二个页面成功执行 INSERT 操作时，将通过在第 120 行调用`modal()`函数来显示 Bootstrap 模态框，否则将在第 123 行再次使用消息 span 标签来显示此错误消息。

### 示例代码 8：`ajax.php`

在示例代码 8 中，可以看到名为`ajax.php`的页面，该页面负责向数据库插入新记录。在该页面顶部的第 2 行，接收到`type`变量。在第 3 行，如果`type`变量等于 register，则调用自定义的`registerNewUser()`函数。

在`registerNewUser()`函数内部的第 7 行，通过 POST 发送的三个变量被设置到本地变量`username`、`password`和`email`中（第 7–9 行）。`password`变量被传递到第 10 行的 PHP `password_hash()`函数。该函数接受两个参数。第一个是用户提供的密码，第二个是我们要生成的哈希类型。在本示例中，我们使用`bcrypt`算法。重要的是要记住，用户的密码永远不应该以纯文本形式存储在数据库中。

在第 18 行，构建了一个简单的 SQL `INSERT`语句，插入到包含名为`dashboard_accounts`的表的数据库中。指定了我们要插入的三个列，后跟`VALUES`关键字和三个问号。这三个问号用作未命名占位符。值不直接放入 SQL 中，因为这不安全。这三个值通过第 22–24 行的`bindParam()`函数绑定到语句上。每个开头的数字表示插入的位置。后跟我们要添加的值，以及与之大致关联的数据类型。由于`username`、`password`和`email`都是字符串，因此每个都使用`PARAM_STR`作为数据类型。

```php
<?php

$type = $_POST['type'];

if ($type == 'register') {
    registerNewUser();
}

function registerNewUser() {
    $username = $_POST['username'];
    $password = $_POST['password'];
    $email = $_POST['email'];

    $hashed_password = password_hash($password, PASSWORD_BCRYPT);

    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO(
            "mysql:host=$host;dbname=$dbname",
            $user,
            $pass
        );

        $sql = "INSERT INTO `dashboard_accounts` (`username`, `password`, `email`)
                VALUES (?,?,?)";

        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $username, PDO::PARAM_STR);
        $sth->bindParam(2, $hashed_password, PDO::PARAM_STR);
        $sth->bindParam(3, $email, PDO::PARAM_STR);
        $sth->execute();

        echo 'registered';
    } catch (PDOException $e) {
        echo 'failed' . $e;
    }
}

?>
```



## 示例代码 8：`ajax.php` — 注册新用户功能

当 `INSERT` 成功运行时，术语 `registered` 将返回到浏览器。此结果将返回到 `register.php` 页面上的 JavaScript 调用者，触发 Bootstrap 模态框打开。如果在注册过程中发生任何错误，将触发 `PDOException`。错误信息将被抑制，并返回单词 `failed`。

### 输出

[图 4.2](#) 显示了完成的注册页面。[图 4.3](#) 描述了用户成功注册后向他们展示的模态框。该模态框为用户提供了一个链接，将他们带回登录页面。

![](img/ed4cb7e1be98f0adec0546edd14f6223_127_0.png)

**图 4.2：** 完成的仪表板注册页面。

![](img/ed4cb7e1be98f0adec0546edd14f6223_128_0.png)

**图 4.3：** 注册成功时显示的 Bootstrap 模态框。

## 4.4 多列柱状图

在前面的示例中，重点放在创建仪表板以实现用户的注册和登录。一旦登录系统，收集到的数据将以图表格式呈现给用户。在这些示例中，`Charts.js` 用作主要的客户端图表渲染库。

### 示例 3：多列柱状图

此示例包含两个文件和两个库：

- `feedbackformrecords.sql` — 这会创建用于保存可视化样本数据的数据库表。
- `chart1.php` — 这是主要的可视化页面。
- `Chart.bundle.js` — 用于渲染柱状图。
- `utils.js` — `Chart.js` 的一个组件。

首先，我们需要从官方仓库下载 `Chart.js` 的副本。[10] 在项目的 GitHub 仓库中，有多种变体可供选择。这些变体的可用性在于，有时开发者可能只想要源代码，而其他时候，他们可能想要用于部署应用程序的代码的压缩（或精简）版本。在我们的案例中，我们想要代码以及示例集合来展示功能。这将使我们能够在上下文中查看现有的图表样本。对于此示例，我们下载 `Chart.js.zip` 文件，如图 4.4 所示。

> [10] https://github.com/chartjs/Chart.js/releases/tag/v3.0.0-alpha

![](img/ed4cb7e1be98f0adec054供应链1be98f0adec0546edd14f6223_129_0.png)

**图 4.4：** `Charts.js` 的下载选项列表。

zip 文件下载完成后，解压 zip 文件的内容，并将整个 `Chart.js` 文件夹放入 Web 服务器的 `htdocs` 中以方便使用。访问示例时，可以通过在 Web 浏览器中输入 `http://localhost`，然后导航到 `Chart.js` 文件夹来完成。在 `Chart.js` 文件夹内部，有许多不同的 JavaScript 文件，另外还有一个名为 `samples` 的文件夹，如图 4.5 所示。JavaScript 文件将放在我们即将创建的图表旁边，以使图表功能对我们可用。

![](img/ed4cb7e1be98f0adec0546edd14f6223_129_1.png)

**图 4.5：** `Chart.js` zip 文件的内容。

在图 4.6 所示的 `samples` 文件夹中，有一个名为 `index.html` 的文件。当通过 Web 浏览器打开此文件时，如图 4.7 所示，可以选择完整的运行示例。与处理较小的代码片段不同，在生成图表时，有许多不同的元素是图表正确运行所必需的。创建自定义图表时，最佳实践是从使用样本数据的样本图表开始。这确保了样本图表在用于替代数据或参数时只需进行最少的修改。

![](img/ed4cb7e1be98f0adec0546edd14f6223_130_0.png)

**图 4.6：** `Chart.js` 文件夹的内容。

![](img/ed4cb7e1be98f0adec0546edd14f6223_130_1.png)

**图 4.7：** 包含工作示例列表的 `index.html`。

## 示例代码：`feedbackformrecords.sql`

在生成图表之前，首先设置一个新的数据库表。在示例代码 9 中，可以看到一个示例数据库表。`FeedbackFormId` 包含一个整数，用于标识数据来自哪个表单。`FeedbackElementID` 是第二个属性，用于进一步精确确定用户使用了什么组件，例如输入字段或点击了按钮。为了记录用户一到十之间的评分，添加了一个名为 `Score` 的属性。这将包含用户给出的数字评分。

```sql
CREATE TABLE `feedbackformrecords` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `FeedbackFormId` INT,
    `FeedbackElementID` INT,
    `Score` INT,
    first [],
    PRIMARY KEY (`id`)
);
```

示例代码 9：带有评分属性的样本反馈记录。

## 示例代码：`chart1.php`

示例代码 10 从第 5 行开始，引用包含渲染图表核心 JavaScript 的 `Chart.bundle.js` 文件。之后在第 6 行，引用了包含绘制图表额外工具的 `utils.js` 文件。此图表是一个 `Chart.js` 演示，附加了 PHP 以收集要渲染的数据。

在第 16 和 17 行，添加了一个 `ID` 设置为 `container` 的 `div` 和一个 `ID` 设置为 `canvas` 的 `canvas`。`canvas` 是绘图操作将进行的地方，而 `container` 是整个柱状图的单一可识别 `div` 标签。`container` `div` 标签的宽度可以根据应用程序需求进行更改。在下面的代码中，`container` `div` 占据了页面宽度的 50%。

在此代码之后，在第 20 行包含了颜色辅助工具。在第 21 行，创建了用于保存图表数据的主要对象。在此内部第 22 行，创建了 `labels` 属性。这是将在柱状图水平轴上显示的不同名称的数组。

在第 24 行，创建了 `datasets` 数组。此数组包含每个标签将出现的值。此柱状图期望数组内为逗号分隔的值。样本数据点数组如下：

`data [6, 40, 10, 11, 12, 1, 90, 9, 3, 10]`。

该数组中的第一个元素 `6`，将对应柱状图上“Score 1”标签的数值。

由于直接将值硬编码到柱状图中无法实现动态化，我们将改为在第 31 行调用一个 PHP 函数来替换 `data[]` 数组内部的值。该函数将动态调用数据库以返回这些值。此 PHP 函数接受单个参数，即我们要绘制的记录 ID。在本示例中，传入的是 `1`。

```html
1   <!doctype html>
2   <html>
3   <head>
4       <title>Bar Chart</title>
5       <script src="Chart.bundle.js"></script>
6       <script src="utils.js"></script>
7       <style>
8           canvas {
9               -moz-user-select: none;
10              -webkit-user-select: none;
11              -ms-user-select: none;
12              }
13          </style>
14          </head>
15          <body>
16          <div id="container" style="width: 50%"> 
17            <canvas id="canvas"></canvas>
18          </div>
19          <script>
20          var color = Chart.helpers.color;
21          var barChartData = {
22              labels: ["Score 1", "Score 2", "Score 3", "Score 4", "Score 5",
23                     "Score 6", "Score 7", "Score 8", "Score 9", "Score 10"],
24              datasets: [{
25                  label: 'Customer Satisfaction',
26                  backgroundColor: color(window.chartColors.blue).alpha(0.5).
27                 rgbString(),
28                  borderColor: window.chartColors.blue,
29                  borderWidth: 1,
30                  data: [
31                  <?php getSatisfactionScores(1); ?>
32                  ]
33              }]
34          };
35 window.onload = function() {
    var ctx = document.getElementById("canvas").getContext("2d");
    window.myBar = new Chart(ctx, {
        type: 'bar',
        data: barChartData,
        options: {
            responsive: true,
            legend: {
                position: 'top',
            },
            title: {
                display: true,
                text: 'Customer Satisfaction'
            }
        }
    });
};
</script>
</body>
</html>
```

示例代码 10：`chart1.php` — 简易 `Chart.js` 柱状图第一部分。

如“示例代码 11”所示，在第 57 行的 `getSatisfactionScores()` 函数中，我们接收了 `formID`，并将其以无名占位符的形式传递给数据库查询。在第 65 行，`SELECT` 语句将收集唯一的 `score`（即 1-10），随后是每个 `score` 的计数 `count`。这是通过调用 SQL `count()` 函数并传递 `score` 列来实现的。

问号（`?`）用于标记将要放置 `formID` 值的位置。该数值是通过第 69 行的 `bindParam()` 功能传递给该位置的。一旦查询运行完毕，将返回十个结果。使用位于第 73 行的 `foreach()` 语句遍历这些结果，并打印出 `score` 标签及其关联的 `count` 数量。这是通过在第 84 行对当前行的位置 1 运行 `echo` 语法来实现的（如第 11 行所示）。

```php
56 <?php
function getSatisfactionScores($formID){
    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
67      $user = 'sampleuser';
82      $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
63      $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,
64          $pass);
85      $sql = "SELECT score, count(score) FROM
66                              feedbackformrecords
67                              WHERE FeedbackFormId = ? GROUP BY score";
68      $sth = $DBH->prepare($sql);
69      $sth->bindParam(1, $formID, PDO::PARAM_INT);
0       $sth->execute();
71      $res = $sth->fetchAll();

3       foreach ($res as $row){
4           echo $row[1] . ', ';
53      }
6   } catch(PDOException $e) {echo $e;}
77 }
8 ?>
```




## 示例代码 11：`chart1.php` — 简易 Chart.js 柱状图第二部分

最终生成的柱状图如图 4.8 所示。由于该柱状图直接从数据库拉取数据，不依赖于静态文件，因此每当用户将新数据提交到数据库中时，只要重新加载图表，即可看到结果数据。

## 4.5 二进制条形图（Binary Bar Chart）

最简单的一种数据类型是二元反馈（binary feedback）。在这种方式中，会提出问题，并将答案以“1”（代表“是”）和“0”（代表“否”）的形式存储起来。通常用户会被问及问题，然后通过勾选复选框或点击单选按钮来作答。

与前面展示范围在 1 到 10 之间数据的示例不同，这类数据只有两种变化。虽然这可能看起来有限，但它是在收集关于特定问题的准确信息（例如以下问题）的唯一方法：

- 后产量是否超过 50k？
- 你是否已婚？
- 你有孩子吗？

### 自定义仪表板

![自定义仪表板](img/ed4cb7e1be98f0adec054eed_iiiii.png)

这些问题可以附带明确的“是”或“否”答案。在绘制这类数据时，会同时显示“是”和“否”两个数据集的收集情况。这有助于从数据中快速获得见解，例如检查是否有四分之三的人表示“是”，那么可能会有四分之一的人回答“否”。

### 示例 4：二元条形图

1. `survey.sql` — 该文件包含创建调查数据库表的 SQL。
2. `chart2.php` — 此文件包含主要的可视化内容。
3. `Chart.bundle.js` — 这提供了柱状图的能力。
4. `utils.js` — 一个由 Chart.js 使用的附加文件。

#### 示例代码：`survey.sql`

示例代码展示了名为 `survey` 的样本数据库表。像以前的示例一样，添加了 `id` 用作主键并且自动递增。每当完成一次新调查时，数据将输入到该表中。

然而，可能存在关于谁何时填写调查的其他描述性数据，但本例中将不包含这些数据。`FeedbackFormId` 列引用附加到此数据的反馈活动（feedback campaign），以及四个额外的数据列：`married`、`haskids`、`ownscar` 和 `makesover50k`。

```sql
CREATE TABLE `survey` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `FeedbackFormId` INT,
    `married` INT,
    `haskids` INT,
    `ownscar` INT,
    `makesover50k` INT,
    PRIMARY KEY (`id`)
);
```

示例代码 12：示例调查数据库表 SQL。

### 示例代码：`chart2.php`

在示例代码 3 的第 8—9 行，导入允许我们创建柱状图的附加 JavaScript 文件。在第 37 行，`container` `div` 标签被添加到页面中，用于容纳新的图表。

三个不同的数组已设置好以保存图表的数据。第 21 行，名为 `lab` 的数组将被用于存储将要添加至列表的每个标签。在第 28 行，添加了 `data1`，负责存储所有的 0 数据（例如“否”）。

在数组设置好之后，还需要在 JavaScript 中填充数据。为此，第 41 行调用了一个名为 `getData()` 的自定义 PHP 函数。该函数接收希望添加到图表中的列名。

第 29 行将要添加的“否”柱状图颜色设置为红色。随后，第 74 行所示的当前行中使用 `echo` 语句。第 36 行，通过向画布传递名为 `ctx` 的引用来初始化图表。第 48 行将数据传递到图表中。

```html
<!doctype html>
<html>
<head>
    <title>Bar Chart</title>
    <script src="Chart.bundle.js"></script>
    <script src="utils.js"></script>
    <style>
        * {
            -moz-user-select: none;
            -webkit-user-select: none;
            -ms-user-select: none;
        }
    </style>
</head>
<body>
    <div id="container" style="width: 100%;">
        <canvas id="canvas"></canvas>
    </div>

    <script>
        var color = Chart.helpers.color;
        var lab = new Array();
        var data1 = [];
        var data2 = [];

        <?php getData('married'); ?>

        var barChartData = {
            labels: lab,
            datasets: [{
                label: 'No',
                backgroundColor: color(window.chartColors.red).alpha(0.5).rgbString(),
                borderColor: window.chartColors.red,
                borderWidth: 1,
                data: data1
            }, {
                label: 'Yes',
                backgroundColor: color(window.chartColors.blue).alpha(0.5).rgbString(),
                borderColor: window.chartColors.blue,
                borderWidth: 1,
                data: data2
            }]
        };

        window.onload = function() {
            var ctx = document.getElementById('canvas').getContext('2d');

            window.myBar = new Chart(ctx, {
                type: 'bar',
                data: barChartData,
                options: {
                    responsive: true,
                    legend: {
                        position: 'top'
                    },
                    title: {
                        display: true,
                        text: 'Chart.js 柱状图'
                    }
                }
            });
        };
    </script>
</body>
</html>
```

## 示例代码 13：`chart2.php` — 示例二进制数据柱状图

在示例代码 14 中，这个柱状图生成过程的核心是一个自定义的 PHP 函数，用于收集数据。该函数从第 64 行开始，是一个简单的函数定义，传入一个名为 `column` 的变量。这是我们希望从中收集数据的数据库列名。

在该函数内部，第 70 行首先建立与数据库的连接，第 72 行创建 SQL 语句。在此查询中，`SELECT` 语句选择传入函数的列。然后使用 SQL 的 `count()` 函数来统计指定列的记录数。这使得该函数可以用于返回数据库表中任何列的信息。

第 80 行使用 `foreach` 语句来遍历从数据库返回的每一行。查询运行后，将返回一组已统计的记录。在数据被图表使用之前，第 83 行和第 86 行使用 PHP 的 `echo` 在页面上放置修改后的 JavaScript 代码，用于“是”记录的计数（如果查看的是“1”条记录），或者在处理“否”记录计数时输出“0”。这些 `echo` 语句生成了图表读取的 JavaScript 数组值。

```php
<?php

function getData($column)
{
    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO(
            "mysql:host=$host;dbname=$dbname",
            $user,
            $pass
        );

        $sql = "SELECT $column, count($column) FROM survey WHERE
                FeedbackFormId = 1
                GROUP BY $column";

        $sth = $DBH->prepare($sql);
        $sth->execute();
        $res = $sth->fetchAll();

        // 添加标签
        echo 'lab.push("' . $column . '");';

        foreach ($res as $row) {
            // 如果是 0，则添加到第一列
            if ($row[0] == 0) {
                echo "data1.push('" . $row[1] . "');";
            }
            // 如果是 1，则添加到第二列
            else if ($row[0] == 1) {
                echo "data2.push('" . $row[1] . "');";
            }
        }
    } catch (PDOException $e) {
        echo $e;
    }
}

?>
```

示例代码 14：`chart2.php` — 按名称检索单列记录的 PHP 示例。

### 输出

在图 4.9 中，我们可以看到调用 `getData()` 函数收集 `married` 列的值的结果。两列分别包含“是”的计数和“否”的计数。

## 4.6 动态仪表盘

虽然我们已经研究了如何收集数据并将结果放入单独的数据库表中，但这并非一个完整的解决方案。在接下来的章节中，我们将介绍“活动”的概念。每个活动被认为是一个完整的数据收集和分析解决方案，将呈现在一个仪表盘上。

### 示例 5：基础仪表盘

为了查看数据，设计了一个仪表盘，允许用户动态选择不同的数据源并渲染可视化效果。此示例包含 Bootstrap、Popper.js、jQuery 和 jQueryUI。

1. `camps.sql` — 包含用于存储单个活动数据的 `dashboard_camps` 表和 `dashboard_camp_elements` 表。
2. `dashboard1.php` — 使用 Bootstrap 样式的示例仪表盘。
3. Bootstrap — 用于提供仪表盘布局的 JavaScript 和 CSS。
4. `dashboard.css` — 包含用于仪表盘布局的额外 CSS。
5. Popper.js — 用作 Bootstrap 的工具提示定位引擎。
6. jQuery/jQueryUI — 此库用于提供模态框，并通过 jQuery 选择器选择单个标签。

#### 示例代码：`camps.sql`

在开始编辑仪表盘的 HTML 之前，需要创建一个名为 `dashboard_camps` 的新数据库表，如示例代码 15 所示。该表将作为系统中存储单个活动的主要位置。每个活动将包含其首次创建的日期，以及用于向用户描述活动的简要说明。用于标识单个活动的核心标识符是 `campid`。与其他字段不同，`campid` 不是自动递增的，因为可能已经创建了遗留的标签和 ID。如果没有创建，可以为每个唯一的活动使用一个简单的整数。

```sql
CREATE TABLE `dashboard_camps` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `datemade` DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `campname` VARCHAR(100),
    `campid` INT,
    PRIMARY KEY (`id`)
);
```

示例代码 15：`dashboard_camps` 数据库表示例。

每个单独的活动可以包含多个不同的活动元素，例如，存储在数据库表 X 的 Y 列中的整数形式的总销售数据。由于数据可能不存储在数据库中，因此用于存储这些数据源的方法应保持灵活。为此，创建了第二个名为 `dashboard_camp_elements` 的数据库表。

该表将包含单个活动可能拥有的所有数据源信息。该表由一个名为 `id` 的唯一主键组成，随后是链接到前一个表中 `campID` 的 `campID`。`description` 列用于向用户简要描述该元素的用途。

`datatype` 列用于定义数据类型，例如 `int`、`string`、`boolean` 等。这是开发人员在后续步骤中使用此数据时的标志。最后一列名为 `datasource`，包含对可视化元素存储位置的引用，例如 MySQL 数据库表或已上传到服务器的 CSV 文件。

`options` 列用于保存应从数据源检索的列的特定数据。最后一列是 `chart`，包含与数据源关联的图表类型描述，例如柱状图或折线图。虽然这两个示例用于仪表盘，但可以轻松添加其他图表类型。

```sql
CREATE TABLE `dashboard_camp_elements` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `campID` INT,
    `desc` VARCHAR(500),
    `datatype` VARCHAR(100),
    `datasource` VARCHAR(100),
    `options` VARCHAR(500),
    `chart` VARCHAR(50),
    PRIMARY KEY (`id`)
);
```





### 输出

图 4.10 描述了一个包含每个属性值的示例数据库表。

要创建仪表盘，Bootstrap 提供了一个可用于基本配置的示例仪表盘布局。图 4.11 展示了 Bootstrap 主题的一个示例，其中只做了非常少量的修改以移除不必要的链接和数据。该示例可以在`https://getBootstrap.com/docs/4.0/examples`在线查看。

**图 4.10**：包含示例数据源和配置选项的数据库表。

**图 4.11**：示例 Bootstrap 仪表盘。

### 示例代码：`dashboard1.php`

在示例代码 16 中，创建了一个名为`dashboard1.php`的新文件。这将是用户登录系统后的主门户。在页面顶部的第 4-8 行的`head`标签内，添加了默认标签，包括页面的`viewport`、`description`、`author`和`title`。随后是第 9 行用于核心 Bootstrap 主题的 CSS。第 12 行还添加了一个名为`dashboard.css`的自定义 CSS 文件，可以根据任何应用主题进行修改。第 12-15 行包含了`jQuery`、`Popper.js`、`Bootstrap`和`jQueryUI`。

库导入后，仪表盘的`header`包含在第 20 行。该标题包含一个`nav`标签，其`class`设置为`navbar`，包括固定在页面顶部的`navbar-dark`主题。

第 22 行包含一个`class`设置为`navbar-brand`的链接，这是对页面主要文本的引用。在此示例中，使用`Dashboard`作为标题。第 23 行添加了一个`div`标签，其`class`设置为`collapse navbar-collapse`。这向导航栏添加了一个可用作下拉菜单的附加项。在此示例中，用于显示`Home`这个词。第 26 行在`href`标签中放置了指向主页或仪表盘起始页的链接。

在第 28 行，添加了一个标题为`Campaign`的导航栏项，它将用作活动的根目录。该项在第 32-34 行包含三个选项：`Add New Visualization`、`Build New Campaign`和`Add Campaign Elements`。由于这些项都是`Campaign`导航栏项的子项，每个项的`class`都被设置为`dropdown-item`。当每个项被点击时，将打开三个独立的模态框。为了触发此过程，每个项都被赋予一个唯一的`href`值。

在第 38 行和第 41 行，添加了两个额外的链接，分别用于自定义的`Text Analysis`功能和将在后续章节中添加的`View Red Flags`功能。

```html
<!doctype html>

<html lang="en">

    <head>

        <meta charset="utf-8">

        <meta name="viewport" content="width=device-width,

            initial-scale=1, shrink-to-fit=no">

        <meta name="description" content="">

        <meta name="author" content="">

        <title>Dashboard</title>

        <link rel="stylesheet" href="Bootstrap.min.css">

        <link rel="stylesheet"

            href="https://code.jquery.com/ui/1.12.1/themes/base/

        jquery-ui.css">

        <link href="dashboard.css" rel="stylesheet">

        <script src="jquery-3.1.0.min.js"></script>

        <script src="popper.min.js"></script>

        <script src="Bootstrap.min.js"></script>

        <script

            src="https://code.jquery.com/ui/1.12.1/jquery-ui.js">

        </script>

    </head>

    <body>

        <header>

            <nav class="navbar navbar-expand-md navbar-dark

                fixed-top bg-dark">

                <a class="navbar-brand" href="#">Dashboard</a>

                <div class="collapse navbar-collapse"

                    id="navbarsExampleDefault">

                    <ul class="navbar-nav mr-auto">

                        <li class="nav-item active">

                            <a class="nav-link" href="#">Home <span

                                class="sr-only">(current)</span></a>

                        </li>

                        <li class="nav-item dropdown">

                            <a class="nav-link dropdown-toggle"

                              href="#" id="dropdown01"

                              data-toggle="dropdown"

                              aria-haspopup="true"

                              aria-expanded="false">Campaign</a>

                            <div class="dropdown-menu"

                              aria-labelledby="dropdown01">

                              <a class="dropdown-item" id="addViz"

                                href="#addAtt" data-toggle="modal"

                                >Add New Visualization</a>

                              <a class="dropdown-item"

                                href="#buildCamp"

                                data-toggle="modal" >Build New

                                Campaign</a>

                              <a class="dropdown-item"

                                href="#addElements"

                                data-toggle="modal" >Add Campaign

                                Elements</a>

                            </div>

                        </li>

                        <li class="nav-item dropdown">

                            <a class="nav-link dropdown-toggle"

                              href="#" id="dropdown01"

                              data-toggle="dropdown"

                              aria-haspopup="true"

                              aria-expanded="false">Text

                              Analysis</a>

                            <div class="dropdown-menu"

                              aria-labelledby="dropdown02">

                              <a class="dropdown-item"

                                href="#selectRanges"

                                data-toggle="modal" >View Red

                                Flags</a>

                            </div>

                        </li>

                    </ul>

                </div>

            </nav>

        </header>
```

示例代码 16：`dashboard1.php` — 简单 Bootstrap 仪表板 — 第 1 部分。

要添加额外选项，在第 48 行，添加了一个额外的`div`，其`class`设置为`container-fluid`。其中，添加了一个`nav`标签，其`class`设置为`small`，主题为`light`。在第 53 行和第 58 行，以两个`li`标签的形式添加了两个选项，其`class`设置为`nav-item`。虽然目前未使用，但可以在此处设置`href`。

在示例代码 17 中，添加了一个名为`main`的标签，它代表仪表板的中心区域。在此标签内部，第 66 行添加了一个`div`标签，其`ID`设置为`output`。当创建可视化内容时，它们将被追加到这个`div`标签中。

```html
<div class="container-fluid">

    <div class="row">

        <nav class="col-sm-3 col-md-2 d-none d-sm-block bg-light

         sidebar">

          <ul class="nav nav-pills flex-column">

            <li class="nav-item">

              <a class="nav-link active" href="#">Overview

              <span class="sr-only">(current)</span>

              </a>

            </li>

            <li class="nav-item">

               <a class="nav-link" href="#">Export</a>

            </li>

          </ul>

        </nav>

        <main role="main" class="col-sm-9 ml-sm-auto col-md-10

         pt-3">

        <h1>Dashboard</h1>

        <div id="output">

        </div>

        <section class="row text-center placeholders">

        </section>

    </div>

</div>
```

示例代码 17：`dashboard1.php` — 简单 Bootstrap 仪表板 — 第 2 部分。

### 输出

图 4.12 展示了带有自定义导航栏的仪表板。

![](img/ed4cb7e1be98f0adec0546edd14f6223_147_0.png)

图 4.12：带有导航栏的 Bootstrap 默认仪表板。

## 示例 4.1：选择活动元素

当点击仪表板上的 Campaign 菜单，然后点击`Add New Visualization`时，需要一个模态框来向用户展示活动列表和活动属性。

本示例包含 Bootstrap、Popper.js、jQuery 和 jqeUI。

- `dashboard2.php` — 这是对原始仪表板的修改，用于向用户展示活动选项。
- `ajax.php` — 此文件用于从数据库中检索活动元素和数据。
- `Bootstrap` — JavaScript 和 CSS 用于提供仪表板的布局。
- `dashboard.css` — 包含仪表板布局的额外 CSS。
- `Popper.js` — 用作 Bootstrap 的工具提示定位引擎。

### 示例代码：`dashboard2.php`

在示例代码 18 中，为了创建模态框，在第 2 行添加了一个`div`标签，其`class`设置为`modal fade`。此模态框通过设置为`addAtt`的`ID`进行唯一标识。默认情况下，该模态框在页面上是隐藏的，直到用户打开它。该标签的`role`设置为`dialog`。`aria-labelledby`设置为`addAtt`，这类似于创建一个名称来将标签链接到`div`。在此`div`内部，第 4 行添加了第二个`div`，其`class`设置为`modal-dialog`。其中包含第 6 行的`div`标签，其`class`设置为`modal-header`，显示在模态框的顶部。在此标题中，第 7 行添加了一个`title`，文本为`Select Campaign`。第 8 行，在模态框的右侧使用了一个`button`标签，为用户提供在需要时关闭模态框的选项。

在模态框的主体中，第 14 行添加了一个行，其中包含一个`div`标签，其`class`设置为`col-4`（第 15 行）。其中，第 16 行添加了一个`list-group`用于结构化。之后，第 19 行添加了第二个`div`，其`class`设置为`col-8`，为内容显示提供更宽的窗口。第 20 行再次添加了一个`list-group`用于结构化。在第 27 行和第 28 行，向模态框末尾添加了两个按钮。第一个是`Close`按钮，允许用户关闭模态框，随后是`Add Visualization`按钮。当点击此按钮时，所选元素用作调用`addViz()` JavaScript 函数的起点，该函数负责将可视化添加到仪表板。此模态框中未指定任何内容。活动列表和活动属性列表稍后使用 JavaScript 添加。

```html
<!-- Select Campaign Modal -->

<div class="modal fade" id="addAtt" tabindex="-1" role="dialog"

     aria-labelledby="addAtt" aria-hidden="true">

  <div class="modal-dialog" role="document">

    <div class="modal-content">

      <div class="modal-header">

        <h5 class="modal-title" id="addAtt">Select Campaign</h5>

        <button type="button" class="close" data-dismiss="modal"

                aria-label="Close">

          <span aria-hidden="true">&times;</span>

       </button>

     </div>

     <div class="modal-body">

       <!--- List of camps-->

       <div class="row">

         <div class="col-4">
```




```html
<div class="list-group" id="list-tab-camp"
  role="tablist">
</div>
</div>
<div class="col-8">
  <div class="list-group" id="list-tab-att"
    role="tablist">
    点击活动以查看属性
  </div>
</div>
</div>
</div>
<div class="modal-footer">
  <button type="button" class="btn btn-secondary"
    data-dismiss="modal">关闭</button>
  <button onclick="addViz()" type="button" class="btn
    btn-primary">添加可视化效果</button>
</div>
</div>
</div>
</div>
</div>
```

示例代码 18：`dashboard2.php` — 活动列表模态框。

在**示例代码 19**的第 35 行，jQuery 选择器被用于选中 `ID` 设置为 `addViz` 的菜单项。当点击该按钮时，系统在第 36 行向页面执行 jQuery `POST` 操作以访问 `ajax.php` 页。`posttype（请求类型）` 参数被设置并传送到该页面为 `getcamp`。此函数会在第 37 行返回一个题为 `data` 的变量，其中包含用 HTML 标记的活动列表。在第 37 行，选中了名为 `list-tab-camp` 的元素并使用由 jQuery `html()` 函数配合传递回来的 `data` 变量来设置其内容。

当点击每个活动时，都可以获取用于可视化的元素列表。为了执行此操作（第 41-42 行），在 `ID` 为 `list-tab-camp` 的 `div` 标签上绑定了监听器；例如，当用户点击其中一个活动触发 `shown.bs.tab` 事件时，该函数就会被调用。在第 43 行中定义了一个名为 `data` 的变量用于存储选中选项卡元素的 HTML 内容。在第 44 行，使用该变量的 `cid` 属性值（通过 jQuery `attr()` 函数获取）来提取活动的 `ID`；在本例中即为 `cid`。

为了检索构成特定活动的各个元素列表，第 45 行向位于 `ajax.php` 的页面发起一次 `POST` 请求，并将 `getformfields` 作为请求类型参数传递以筛选出相关数据（即返回针对给定活动所需的属性）。同时也会传入该单个活动的 `cid`。在第 46-47 行中，当函数执行完毕后，结果会在一个函数字符串内通过标题为 `data` 的变量被获取并使用 jQuery `html()` 功能添加至名为 `list-tab-att` 的元素之中。

```javascript
<script>
  // Add list of camp elements to the modal

  $("#addViz").click(function() {
    console.log("Called add viz");

    $.post("ajax.php", { type: "getcamp" })
      .done(function(data) {
        $("#list-tab-camp").html(data);
      });
  });

  $('div[id="list-tab-camp"]').on("shown.bs.tab", function(e) {
    var data = e.target; // HTML of just selected tab
    var cid = $(data).attr("cid"); // get the ID

    // get list of attributes for campaign
    $.post("ajax.php", {
      type: "getformfields",
      cid: cid
    }).done(function(data) {
      $("#list-tab-att").html(data);
    });
  });
</script>
```

示例代码 19：`dashboard2.php` — JavaScript，用于在仪表板模态框中列出活动。

***示例代码片段***：**`ajax.php`**

为了检索活动和活动的属性列表，需要修改 **`ajax.php`** 页面。**示例代码 20** 的第 3 行中，如果 `type` 设置为 `getcamp`，则会调用第 4 行中的 PHP 函数 `getCamp()` 以返回活动列表；随后又增加了类型为 `getformfields` 属性的设置（见第 6-7 行），用于根据 `cid` 检索活动的属性。

在活动模态框首次打开时，系统会从仪表板数据库 `dashboard.camps` 表格中获取活动列表。需要关注的主要信息有：`campid` 以及该 `campaigne`（即对应记录的行）。在进行 `foreach` 语句的每一次迭代过程中（第 23 行附近），均会创建一个新 `href` 链接；同时在该对象上设置类为 `list-group-item list-group-item-action`。还会在目标元素上加入自定义属性，以便协助对基本活动数据的进一步移动处理，例如 `cid` 等。随后将“列表名”（`list-camp`）设置为活动的 ID 值并将第 24 行上的 `data-toggle` 属性设定为一个数组；对于用户而言显示出的文本内容为：`campid` 加上单个虚号后，再加上从该行中提取的 `campname`。

针对已在模态框中选定的各项活动，系统会向 **`ajax.php`** 页面发送 AJAX 请求并调用其内部的 `getFormFields()` 函数进行处理获取结果。

```php
<?php

$type = $_POST['type']; // 接收前端传来的类型参数

if ($type == 'getcamp') { // 判断是否为活动列表请求模式
    getCamp(); // 如果是则执行相关逻辑；否则...
} else if ($type == 'getformfields') { // 如果类型为获取表单字段信息
} else {
    throw new Exception('未定义该类型参数或者为空！');
    return;
}

function getCamp()
{
    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO(
            "mysql:host=$host;dbname=$dbname",
            $user,
            $pass
        );

        // 定义数据库连接对象，并指定对应的操作符参数集
        // $sql = "select campid, campanme from dashboard_camps";

        # 获取当前需要查询的数据集合结果记录
        $sth = $DBH->prepare($sql)->execute();
        $res = $sth->fetchAll();

        foreach ($res as $row) {
            echo '<a class="list-group-item list-group-item-action cid="' .
                $id . '" id="_camp-' . $id . '"' .
                ' data-toggle="tab" href="#camp-' . $id .
                '" role="tab" aria-controls="_cid-">' .
                $row['campanme'] .
                '</a>';
        }
    } catch (PDOException $e) {
        echo $e;
    }
}
```

**示例代码 20：**`ajax.php` — 获取活动列表——第一部分

128 ■ 利用 JavaScript 和 PHP 实现的用户数据收集和分析应用实例

在**示例代码 21**的第 37 行中定义了函数；而该函数的主要职责是返回组成单个元素的属性描述信息。这些内容包含：文本型说明（基于原始定义）、正在处理的 `dataType`、信息来源等相关介绍资料，例如它是 CSV 文件还是 SQL 数据库导出等数据源类型，以及用于在仪表板上渲染数据时所使用的图表形式等等。

同时还需要注意：在第 38 行中存储了已接收到该请求参数中的 `cid` 属性值并将其放入局部变量当中进行临时保管；随后再于第 46-50 行处添加相应的 SQL 代码以选择对应的活动元素集合——因为其中包含一个问号作为占位符号，代表动态传递过来的 `campID` 属性，以便后续使用 `bindParam()` 函数对其进行追加绑定处理（参见后面部分）并在第 49 行完成这一操作。此外还在第 53 行添加了一个用于循环遍历结果数据的 `foreach` 语句；然后在每轮迭代的过程中分别提取出包括 ID、描述信息在内的重要指标数据并将其存放在单独的局部变量之中加以保留或稍作预处理后再进行下一步的工作流程处理（即获取各类所需属性相关信息），并将它们整合成一个完整的 HTML 链接结构返回给前端界面展示给用户浏览查看使用等用途。

```php
// return a list of form fields
// for a given cid
function getFormFields()
{
    var $cid = $_POST['cid']; // 获取外部传递进来的具体活动编号信息

    try {
        // 建立与本地 MySQL 数据库服务器之间的连接通道，并设置相关参数配置...
        // localhost:3306
        // bookexamples
        // sampleuser, password=3C9038A509BE6145AAD6827B4568AD918BC3DAC0

        PDO("mysql:host=$host;dbname=$dbname", $u, $p);

        // 编写一条选择操作语句，从指定表中查询所有符合条件的记录集
        // （即当前活动的所有子要素信息）
        select * from dashboard_camp_elements where campID=?

        prepare($sql)->execute();
        $res = fetchAll();

        foreach ($res as $row) {
            $id = $row['id'];
            $desc = $row['desc'];
            $dtype = $row['datatype'];
            $src = $row['datasource'];
            $chte = chart[$row['chart']]; // 读取并赋值当前行的图表类型参数

            // 输出每一个个体属性的具体描述说明（即按钮名称），
            // 以便用户点击选择时能够正确对应显示出来。
            echo '<a char="." datasource=' . $src .
                ' elementid=' . $id . ' elementtitle=' . $desc .
                ' cid=... class="list-group-item list-group-item-action"
                id="_camp-e" data-toggle="tab" href="#" role="tab"
                aria-controls="_campe">' .
                $desc . '-' . $dataType . '-source:' . $src .
                '</a>';
        }
    } catch (PDOException $e) {
        echo $e;
    }
}
```

示例代码 21：`ajax.php` — 获取表单字段列表——第二部分

图 4.13 展示了“选择活动”模态框界面。此窗口左侧列出当前系统支持的活跃项目清单，当用户选定某一项工作时，右侧便会自动加载并显示与其相关联的内容属性集合信息；这些资料涵盖了关于元素描述、数据结构格式以及数据来源等多个方面的详细内容说明资料，以供查阅参考使用等目的需要！

![图 4.13 选择活动模态框界面](img/ed4cb7e1be98f0adec0546edd14f6223_153_0.png)

### 示例 7：添加可视化

当点击活动模态框中的任何活动元素时，它们会变成蓝色，表示已选中。要基于此选定的活动元素添加可视化图表，点击“添加可视化”按钮时会调用 `addViz()` 函数。本示例包含四个文件：

1. `dashboard3.php` —— 此文件包含原始的仪表板 HTML/JavaScript，并额外添加了用于添加可视化的函数。
2. `data_processor.php` —— 此文件包含 PHP 代码，根据所选数据源访问数据库或文件。
3. `line.php` —— 此文件包含生成 Chart.js 折线图的 HTML/JavaScript。
4. `barchart.php` —— 此文件包含生成 Chart.js 柱状图的 HTML/JavaScript。

在示例代码 22 中，描述了位于 `dashboard3.php` 文件底部的 `script` 标签内的 `addViz()` 函数。在第 2 行，执行了一个简单的 `console.log()` 以指示我们该函数已被正确调用。在第 3-6 行，搜索 `list-tab-att` 项目，其中状态被设置为 `a.active`，表示已选中。对于选定的活动元素，提取了 `elementID`、`chart`、`datasource` 和 `elementtitle`。这些在生成期间被放置在各个项目中。

在第 11 行，进行检查以确定所需的图表类型。如果类型等于 `barchart`，则使用 jQuery 选择器选取 `output` `div` 标签并附加一个新的 `div` 标签。该 `div` 标签的内容通过动态调用 `load()` 函数获取 `bar.php` 页面，并传入 `source`、`ID` 和 `title` 变量。在第 16 行，对折线图重复了相同的过程。

```javascript
function addViz() {
  console.log("add viz called");

  var elementid = $("#list-tab-att a.active")
    .attr("elementid");
  var chartType = $("#list-tab-att a.active")
    .attr("chart");
  var dataSource = $("#list-tab-att a.active")
    .attr("datasource");
  var vizTitle = $("#list-tab-att a.active")
    .attr("elementtitle");

  if (chartType == "barchart") {
    $("#output").append(
      $("<div>").load(
        "bar.php?source=" + dataSource +
        "&id=" + elementid +
        "&title=" + escape(vizTitle)
      )
    );
  } else if (chartType == "linechart") {
    $("#output").append(
      $("<div>").load(
        "line.php?source=" + dataSource +
        "&id=" + elementid +
        "&title=" + escape(vizTitle)
      )
    );
  }
}
```

**示例代码 23：**`data_processor.php` — 根据数据源类型从数据源获取数据。

### 示例代码：`data_processor.php`

Both the `barchart.php` and `line.php` file require use of a file titled `data_processor.php`. This file is used as the main method of gathering data from different data sources.



在示例代码 23 中，第 2 行定义了`getData()`函数，该函数接受用于绘制图表的元素的`ID`和引用当前数据存储位置的`sourceType`。在第 3 行，如果源类型是 MySQL 数据库，则向数据库发出查询。通过在第 11 行调用`getDataSourceOptions()`函数并传入要可视化的元素的`ID`来收集查询。对于返回的每一行，值为`row[0]`，调用`push()`函数并将第 16 行的术语添加到 JavaScript `lab`数组中，该值被添加到 X 值。在第 17 行，用于修改条形高度的要显示的`Y`值从`row[1]`收集并推送到`data1` JavaScript 数组。

在第 23 行，如果`sourceType`变量设置为`csv`，则在第 24 行调用`getDataSourceOptions`。此函数接受要绘制图的元素的`ID`。将绘制的数据必须遵循与`X`和`Y`相同的结构。其中`X`是标签，`Y`是要绘制的值。在将 CSV 添加到系统的过程中，定义了两个列，然后描述文件名。在数据库表中，这些值的形式为`filename.csv, 1, 2`，其中 1 是 CSV 文件中要绘制的`X`列，2 是`Y`列。

为了拆分为处理的值，在第 25 行调用`explode()`函数，接受一个分隔符以及要处理的字符串。在此示例中，分隔符为逗号。在第 27 行调用`fgetcsv()`以打开文件连接并收集内容。由于该文件是 CSV，这里再次指定分隔符为逗号。图表的`label`存储在与`lab` JavaScript 数组中的变量中。

这些值从包含 CSV 文件中各个列的`data`变量中提取。在第 30 和 31 行，提供了对`col1`和`col2`的引用，以识别感兴趣的两个列并提取其值。第一个是标签，第二个是与标签关联的值。使用包含 JavaScript 的`echo`语句将这些值打印出来，用于添加到`lab`和`data1` JavaScript 数组。JavaScript `push()`函数用于将值添加到相应的数组中。

```
<?php
function getData($id, $sourceType){
    if($sourceType =='mysql'){
        try {
            $host = 'localhost:3306';
            $dbname = 'bookexamples';
            $user = 'sampleuser';
            $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DACO';
            $DBH = new PDO("mysql:host=$host;dbname=$dbname",
             $user, $pass);
            $sql = getDataSourceOptions($id);
            $sth = $DBH->prepare($sql);
            $sth->execute();
            $res = $sth->fetchAll();
            foreach ($res as $row){
                echo " lab.push('".$row[0]."');";
                echo " data1.push('".$row[1]."');";
            }

        } catch(PDOException $e) {echo $e;}

    }
    else if($sourceType =='csv'){
        $dataSourceOptions = getDataSourceOptions($id);
        $op = explode(',',$dataSourceOptions);
        if (($file = fopen('samplefiles/'.$op[0], "r")) !== FALSE)
            {while (($data = fgetcsv($file, 1000, ",")) !== FALSE)
                {$col1 = $op[1];
                    $col2 = $op[2];
                    echo " lab.push('".$data[$col1]."');";
                    echo " data1.push('".$data[$col2]."');";
                }
            fclose($file);
        }
    }

}
function getDataSourceOptions($id){
    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DACO';
        $DBH = new PDO("mysql:host=$host;dbname=$dbname",
        $user, $pass);
        $sql = "SELECT options FROM dashboard_camp_elements
             WHERE id = ?";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $id, PDO::PARAM_INT);
        $sth->execute();
        $res = $sth->fetch();
            return $res[0];
        } catch(PDOException $e) {echo $e;}
    }
}
```

### 示例代码：line.php

创建一个名为`line.php`的文件以可视化折线图。在第 2 行，包含`data_processor.php`文件，如前所述将提供数据源访问权限。在第 11 和 12 行，包含了 Charts.js 所需的两个 JavaScript 文件。这两个文件必须在当前目录中。在第 14–18 行，设置`canvas`不允许选区。在第 22 行，添加一个`div`，用于存储可视化内容。在第 27 行，生成一个随机数字并放入标题为`uniqueID`的局部变量中。这用作图的 ID。在第 28 和 30 行，将 ID 设置为`container`和 canvas。在第 36 行，调用 PHP 函数`getData()`以描述的内容中的函数。ID 和`sourceType`传递给该函数。

在第 38 行，添加包含要渲染的图表类型的`config`变量。`labels`设置为生成的`lab`数组。在`datasets`数组的第 43 行内，将图的数据设置为生成的`data1`数组。

```
<?php
include('data_processor.php');
$id = $_GET['id'];
$title = $_GET['title'];
$sourceType = $_GET['source'];
?>
<!doctype html>
<html>
<head>
    <title>Line Chart</title>
    <script src="Chart.bundle.js"></script>
```

 <script src="utils.js"></script>

<style>

    canvas{

        -moz-user-select: none;

        -webkit-user-select: none;

        -ms-user-select: none;

    }

</style>

</head>

<body>

<div id="container" style="width:50%"; class="ui-widget-content">

    <canvas id="canvas"></canvas>

</div>

<script>

    var uniqueID = Math.floor((Math.random() * 1000) + 1);

    document.getElementById("container").setAttribute("id", "container"+uniqueID);

    document.getElementById("canvas").setAttribute("id", "canvas"+uniqueID);

    var lab = new Array();

    var data1 = new Array();

<?php

    // Get the data for the graph

    getData($id,$sourceType);

?>

    var config = {

        type: 'line',

        data: {

            labels: lab,

            datasets: [{

                label: "",

                backgroundColor: window.chartColors.red,

                borderColor: window.chartColors.red,

                data: data1,

                fill: false,

            }]

        },

SAMPLE CODE 24：line.php —在添加可视化时使用——第 1 部分。

在第 25 个示例代码中，第 84 行将图表引用`ctx`和`config`传递给`create`以创建新的图表对象。在第 85 和第 86 行，调用`draggable()`和`resizable()`函数于`container`上，允许其在屏幕上移动。这些函数是作为原始仪表板的一部分添加的 jQueryUI 库中的组件。

```
options: {
    responsive: true,
    title:{
        display:true,
        text: unescape('<?php echo $title;?>')
    },
    tooltips: {
        mode: 'index',
        intersect: false,
    },
    hover: {
        mode: 'nearest',
        intersect: true
    },
    scales: {
        xAxes: [{
            display: true,
            scaleLabel: {
                display: true,
                labelString: 'Month'
            }
        }],
        yAxes: [{
            display: true,
            scaleLabel: {
                display: true,
                labelString: 'Value'
            }
        }]
    }
}
};
var ctx = document.getElementById("canvas"+uniqueID).
getContext("2d");
window.myLine = new Chart(ctx, config);
$("#container"+uniqueID).resizable();
$("#container"+uniqueID).draggable();
</script>
</body>
</html>
```

SAMPLE CODE 25：line.php —在添加可视化时使用——第 2 部分。

### 示例代码：bar.php

在第 26 和 27 个样本代码中，可以看到`bar.php`文件。该文件的 JavaScript 与`line.php`文件的完全相同。唯一需要进行的修改是在第 52 行，将类型设置为`bar`。

```
<?php
include('data_processor.php');
$id = $_GET['id'];
$title = $_GET['title'];
$sourceType = $_GET['source'];
?>
<!doctype html>
<html>
<head>
<script src="Chart.bundle.js"></script>
<script src="utils.js"></script>
<style>
canvas {
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
}
</style>
</head>
<body>
<div id="container" style="width:50%"; class="ui-widget-content">
    <canvas id="canvas"></canvas>
</div>
<script>
var uniqueID = Math.floor((Math.random() * 1000) + 1);
document.getElementById("container").setAttribute("id",
    "container"+uniqueID);
document.getElementById("canvas").setAttribute("id",
    "canvas"+uniqueID);
var color = Chart.helpers.color;
var lab = new Array();
var data1 = new Array();
<?php
// Get the data for the graph
getData($id, $sourceType);
?>
var barChartData = {
    labels: lab,
    datasets: [{

```

```:
label: '',
backgroundColor: color(window.chartColors.red).
alpha(0.5).rgbString(),
borderColor: window.chartColors.red,
borderWidth: 1,
data: data1
}]

};
var ctx = document.getElementById("canvas"+uniqueID).
getContext("2d");
window.myBar = new Chart(ctx, {
    type: 'bar',
    data: barChartData,

SAMPLE CODE 26：bar.php —在添加可视化时使用——第 1 部分。

```

options: {

    responsive: true,

    scales: {

        yAxes: [{

            ticks: {

                beginAtZero: true

            }

        }]

    },

    legend: {

        display:false,

    },

    title: {

        display: true,

        text: unescape('<?php echo $title;?>')

    }

}

});

$("#container"+uniqueID).resizable();

$("#container"+uniqueID).draggable();

</script>

</body>

</html>



### SAMPLE CODE 27：bar.php——在添加可视化时使用——第 2 部分

#### 输出

**图 4.15**概述了包含两种不同可视化的最终仪表板。第一个是条形图，第二个是折线图。由于图表的设置是动态的，因此只需进行最小的修改即可添加进一步的图表类型。

#### 仪表板

![](img/ed4cb7e1be98f0adec0546edd14f6223_163_0.png)

**图 4.15：**包含两个已添加可视化的示例仪表板。

### 示例 8：添加新活动

每个可视化构件的基础是活动。要向系统中添加新的活动，在*活动*下拉菜单中有一个标题为 *Build New Campaign*（构建新活动）的菜单项可供选择。选择此项时，会创建一个新的模态框，允许用户输入活动的唯一`ID`号，随后是描述语。为此，首先创建一个全新的模态框。

本示例包含两个文件：

1. `dashboard4.php`——这是原始仪表板，带有额外的 Bootstrap 模态框。
2. `ajax.php`——此文件用于动态向数据库插入新活动。

### 示例代码：dashboard4.php

在第 28 个样本代码中，第 2 行添加了一个`div`标签，其`ID`设为`buildCamp`。在第 9 行，将模态框的标题设置为 *Create new campaign*（创建新活动）。在第 21 和 22 行，添加了两个输入字段，其`ID`分别设为`newcid`和`newdesc`。在第 28 行添加了一个关闭按钮，随后在第 30 行添加了另一个负责触发向数据库中添加活动的按钮。该按钮的`ID`被设置为`addNewCamp`。

```html
<!-- Build new camp modal -->

<div class="modal fade" id="buildCamp" tabindex="-1"
  role="dialog"
  aria-labelledby="buildCamp"
  aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="buildCamp">Create new Campaign</h5>
        <button type="button" class="close" data-dismiss="modal"
          aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <!--- List of camps-->
        <div class="row">
          <div class="col-5">
            <div class="list-group" id="list-tab-camp" role="tablist">
              Campaign ID <input type="text" id="newcid"><br>
              Description <input type="text" id="newdesc"><br>
            </div>
          </div>
        </div>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary"
          data-dismiss="modal">Close</button>
        <button id="addNewCamp" type="button" class="btn btn-primary"
          data-dismiss="modal">Add New Campaign</button>
      </div>
    </div>
  </div>
</div>
```

```html
<div>
<!-- END NEW CAMP MODAL -->
```

### SAMPLE CODE 28：dashboard4.php——附加添加新活动模态框

在第 29 个样本代码中，第 3 行将 jQuery 监听器绑定到`addNewCamp`按钮上。在第 5 和第 6 行，当点击该按钮时，使用 jQuery 选择器从模态框中提取`newcid`和`newdesc`的值。在第 7 行，将这些变量`POST`发送到名为`ajax.php`且标题为`type=addnewcamp`的页面。调用`ajax.php`页面后，使用一个简单的`alert()`输出响应结果。

```javascript
<script>

// example 3 changes

$("#addNewCamp").click(function() {
    alert("called");

    var newcid = $("#newcid").val();
    var newdesc = $("#newdesc").val();

    $.post("ajax.php", {
        type: "addnewcamp",
        newcid: newcid,
        newdesc: newdesc
    })
    .done(function(data) {
        alert(data);
    });
});

</script>
```

### SAMPLE CODE 29：dashboard4.php——添加新活动按钮点击监听器

### 示例代码：ajax.php

样本代码 30 概述了`ajax.php`页面。在第 1 行，首先捕获类型。在第 2 行，如果`type`等于`addnewcamp`，则调用`addNewCamp()`函数。在第 6 和第 7 行，从`POST`中首次提取新`ID`和描述语并将其放入局部变量中。在第 13 行创建数据库的新连接。第 15 行创建的 SQL `INSERT`语句放置两个问号以占位符表示值。通过调用`bindParam()`函数分别在 lines 18 and 19 绑定这些值。在第 20 行执行`INSERT`语句。

142 ■ 使用 JavaScript 和 PHP 进行用户数据采集与分析

```php
$type = $_POST['type'];

if ($type == 'addnewcamp') {
    addNewCamp();
}

function addNewCamp() {
    $newcid = $_POST['newcid'];
    $newdesc = $_POST['newdesc'];

    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO(
            "mysql:host=$host;dbname=$dbname",
            $user,
            $pass
        );

        $sql = "INSERT INTO `dashboard_camps` (`campname`,
            `campid`) VALUES (?,?);";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $newdesc, PDO::PARAM_STR);
        $sth->bindParam(2, $newcid, PDO::PARAM_INT);
        $sth->execute();

        echo 'Added';
    } catch (PDOException $e) {
        echo 'failed' . $e;
    }
}
```

示例代码 30：`ajax.php`——添加新活动 PHP。

#### 输出

图 4.16 显示了点击 *添加新活动* 后的输出。

### 示例 9：添加新活动元素

向用户显示的最复杂的模态框是设计用于允许用户指定新活动元素的模态框。活动元素是活动中的一个独立字段。此示例由三个文件组成：

1. `dashboard5.php`——原始的仪表板，带有一个用于添加活动元素的新模态框。
2. `ajax.php`——此文件负责将新活动元素记录插入数据库。
3. `listOfFiles.php`——此文件用于检索可用作数据源的文件列表。

![](img/ed4cb7e1be98f0adec0546edd14f6223_167_0.png)

**图 4.16：**两个文本字段，允许用户创建新活动。

### 示例代码：dashboard.php

在示例代码 31 中，第 2 行创建了一个新的`div`标签。此`div`的`ID`设置为`addElements`。`role`设置为`dialog`。

在第 19 行，添加了一个输入字段，允许用户输入活动`ID`。在第 21 行，添加了另一个输入字段，允许用户输入列名。由于数据可以是任何格式，在第 24 行，添加了一个`select`字段，允许用户指定内容是整数、文本还是小数。在第 30 行，添加了另一个字段，允许用户确定内容是来自 CSV 文件还是 MySQL 数据库。

在第 35 行，添加了一个`select`，允许用户选择希望在仪表板上显示条形图还是折线图。添加了一个标题为`dataSourceOptions`的`div`。当此模态框加载时，此`div`标签中不显示任何内容。当用户选择 MySQL 时，此`div`中将显示一个文本区域。当用户选择 CSV 时，则会显示一个文件列表供选择。

# 使用 JavaScript 和 PHP 进行用户数据采集与分析

```html
<!-- ADD NEW CAMP ELEMENT -->

<div class="modal fade" id="addElements" tabindex="1"
  role="dialog"
  aria-labelledby="addElements"
  aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content" style="width:900px">
      <div class="modal-header">
        <h5 class="modal-title" id="addElements">创建新活动元素</h5>
        <button type="button" class="close" data-dismiss="modal"
          aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <div class="container">
          <div class="row">
            <div class="col-sm">
              <b>活动 ID</b><br>
              <input type="text" id="addElementCid"><br>

              <b>自定义列名</b><br>
              <input type="text" id="addElementCol"><br>

              <b>数据类型</b><br>
              <select id="addElementDataType">
                <option>int</option>
                <option>text</option>
                <option>decimal</option>
              </select><br>

              <b>数据源</b><br>
              <select id="addElementSource">
                <option value="csv">CSV 文件</option>
                <option value="mysql">MySQL 列</option>
              </select><br>

              <b>图表类型</b><br>
              <select id="chartType">
                <option value="barchart">条形图 (X 和 y)</option>
                <option value="linechart">折线图 (X 和 Y)</option>
              </select><br>
            </div>

            <div class="col-sm">
              <b>选择数据源</b><br>
              <div id="dataSourceOptions" style="width:300px;
                height:200px; overflow: auto">
              </div>
              <div id="dataSourceAdditional"></div>
            </div>
          </div>
        </div>
      </div>

      <div class="modal-footer">
        <button type="button" class="btn btn-secondary"
          data-dismiss="modal">关闭</button>
        <button id="addNewCampElement" type="button"
          class="btn btn-primary"
          data-dismiss="modal">添加新元素</button>
      </div>
    </div>
  </div>
</div>
```

示例代码 31：`dashboard5.php`——添加新活动元素模态框。

示例代码 32 描述了用于跟踪用户正在添加的数据源的 Javascript。在第 65 行，当在表单上选择源（例如 CSV 或 MySQL）时，将触发`on()`函数。在第 66 行，如果选定的源等于`mysql`，则在第 67 行，将选择`dataSourceOptions` div 标签，并将其内容更新为一个示例 SQL 查询。在第 71 行，如果选择了 CSV，则会选择`dataSourceOptions` div 标签，并将其内容设置为加载`listOfFiles.php`文件的输出。此 PHP 文件用于列出目录的内容。



```javascript
$('#addElementSource').on('change', function() {
    if (this.value === 'mysql') {
        $('#dataSourceOptions').html(
            '<textarea rows="6" cols="35" id="querybox">select Score, count(Score) from feedbackformrecords where FeedbackFormId=1 and FeedbackElementID = 1 group by Score;</textarea>'
        );
        $('#dataSourceAdditional').html('');
    } else if (this.value == 'csv') {
        $('#dataSourceOptions').load('listOfFiles.php');
        $('#dataSourceAdditional').html(
            '列 X: <input type="text" id="selectedColX" size="2"/>' +
            '列 Y: <input type="text" id="selectedColY" size="2"/><br>'
        );
    } else if (this.value == 'textfile') {
        $('#dataSourceOptions').load('listOfFiles.php');
        $('#dataSourceAdditional').html('');
    }
});
```

示例代码 32：`dashboard5.php` — 更新 `dataSourceOptions` div 标签的 JavaScript。

在示例代码 33 中，第 83 行，如果点击 ID 设置为 `addNewCampElement` 的按钮，将运行以下代码。第 84–87 行，从输入字段和选择框中收集值。第 91 行，收集选定的数据源类型。

由于每个不同的数据源具有不同的字段组合，因此添加了一个名为 `optionString` 的字符串。这用于保存访问指定数据源的配置。对于 CSV 类型的数据源，第 96–99 行收集定义的列。这些被设置到 `optionsString` 变量中，用逗号分隔。对于 MySQL 数据类型，第 104 行收集 `querybox` 的值并直接放入 `optionsString`。

收集完值后，第 109 行对 `ajax.php` 页面执行 `POST`。发送的请求 `type` 设置为 `addElementToCamp`。收集的每个属性都被发送。当此函数完成时，第 116 行显示一个包含 `ajax.php` 页面输出的 `alert()` 语句。

```javascript
$('#addNewCampElement').click(function() {
    var addElementCid = $('#addElementCid').val();
    var addElementCol = $('#addElementCol').val();
    var dataType = $('#addElementDataType').val();
    var chartType = $('#chartType').val();
    var optionsString = '';

    // 获取数据源类型
    var dataSourceType = $('#addElementSource :selected').val();

    if (dataSourceType == 'csv') {
        // 选择 CSV 特定选项
        // 文件名
        var selectedFile = $('#file:checked').val();

        // 关注的列
        var selColX = $('#selectedColX').val();
        var selColY = $('#selectedColY').val();

        optionsString = selectedFile + ',' + selColX + ',' + selColY;
    } else if (dataSourceType == 'mysql') {
        var queryBoxContent = $('#querybox').val();
        optionsString = queryBoxContent;
    }

    $.post('ajax.php', {
        type: 'addElementToCamp',
        cid: addElementCid,
        customName: addElementCol,
        dataType: dataType,
        dataSourceType: dataSourceType,
        options: optionsString,
        chart: chartType
    }).done(function(data) {
        alert(data);
    });
});
```

示例代码 33：`dashboard5.php` — JavaScript 点击触发新活动的保存。

## 示例代码：`listOfFiles.php`

为了向用户列出可用的 CSV 文件，对一个名为 `listOfFiles.php` 的页面发起了 AJAX 调用。在该页面内部，使用了 `opendir()` 函数的引用来打开位于 PHP 脚本旁边的 `samplefiles` 文件夹。实际上，只要文件夹路径正确，该文件夹可以放置在任何位置。要找出当前工作目录，只需调用 `echo getcwd();`，即可打印出确切的目录路径，辅助调试过程。

在文件夹内，使用 while 循环遍历每个单独的文件。添加了一个简单的 if 语句，以确保条目或单个文件不包含句点或两个句点，这可能表示父文件夹。对于每个单独的文件，添加了一个类型设置为 radio 的 input 字段。字段的 ID 设置为 `file`。最关键的元素是存储文件名内部引用的 `value`。

在本例中，`value` 被设置为来自 `entry` 变量的值。`entry` 变量再次被打印给用户查看，后面跟着一个简单的 `br` 标签以换行。列出所有文件后，必须使用 `closedir()` 函数关闭与目录的连接。在示例代码 34 中，可以看到 `listOfFiles.php` 的完整代码。

```php
<?php

if ($handle = opendir('samplefiles')) {
    while (false !== ($entry = readdir($handle))) {
        if ($entry != "." && $entry != "..") {
            echo '<input type="radio" id="file" name="file" value="' . $entry . '">' . $entry . '<br>';
        }
    }
}

closedir($handle);

?>
```

示例代码 34：`listOfFiles.php` — 从 `samplefiles` 文件夹检索文件列表。

## 示例代码：`ajax.php`

示例代码 35 概述了 `ajax.php` 页面。在第 2 行，首先访问 `type` 变量并将其放入局部变量中。在第 3 行，如果变量等于 `addElementToCamp`，则在第 4 行调用 `addElementToCamp()` 函数。第 7–12 行，从 POST 中提取每个变量并放入局部变量。在第 20 行，建立新的数据库连接。在第 23 行，创建 INSERT 语句，使用问号作为值的占位符。在第 28–33 行，使用 `bindParam()` 函数将每个值添加到语句中。在第 34 行，最终执行该语句。

```php
<?php

$type = $_POST['type'];

if ($type == 'addElementToCamp') {
    addElementToCamp();
}

function addElementToCamp()
{
    $cid = $_POST['cid'];
    $customName = $_POST['customName'];
    $dataType = $_POST['dataType'];
    $dataSourceType = $_POST['dataSourceType'];
    $options = $_POST['options'];
    $chart = $_POST['chart'];

    try {
        $host = 'localhost:3306';
        $dbname = 'bookexamples';
        $user = 'sampleuser';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO(
            "mysql:host=$host;dbname=$dbname",
            $user,
            $pass
        );

        $sql = "INSERT INTO `dashboard_camp_elements` (
                    `campID`,
                    `desc`,
                    `datatype`,
                    `datasource`,
                    `options`,
                    `chart`
                ) VALUES (?,?,?,?,?,?);";

        $sth = $DBH->prepare($sql);

        $sth->bindParam(1, $cid, PDO::PARAM_STR);
        $sth->bindParam(2, $customName, PDO::PARAM_STR);
        $sth->bindParam(3, $dataType, PDO::PARAM_STR);
        $sth->bindParam(4, $dataSourceType, PDO::PARAM_STR);
        $sth->bindParam(5, $options, PDO::PARAM_STR);
        $sth->bindParam(6, $chart, PDO::PARAM_STR);

        $sth->execute();

        echo 'New Element Added';
    } catch (PDOException $e) {
        echo 'failed' . $e;
    }
}

?>
```




### 示例代码 35：`ajax.php` — 向现有活动添加元素

#### 输出

图 4.17 概述了数据源选择过程。在其右侧，当选择 MySQL 或 CSV 时，数据源选项变得可见。在本例中，已选择 CSV，并在模态框的右侧返回文件列表。然后将输入活动 `ID`，接着是唯一元素的名称。输入 X 列以表示感兴趣的行，输入 Y 以为从所选 CSV 文件中指示感兴趣的列。可以设置感兴趣列的数据类型，以及我们希望创建的图表类型。

![](img/ed4cb7e1be98f0adec0546edd14f6223_174_0.png)

图 4.17：添加新活动元素和选择数据源的过程。

## 4.7 总结

本章描述了创建登录页面、注册页面和仪表板的过程。该仪表板作为以图表形式添加数据可视化的起点。由于数据有多种格式，因此探讨了创建动态图表的过程。虽然可视化对于探索数据很有用，但通常需要额外的处理才能对数据有更深入的了解。

在[第 5 章](Chapter 5)中，探讨了处理文本的过程，概述了删除无关术语和处理相关术语的方法。

# 第 5 章：处理文本

## 5.1 引言

从用户那里收集数据时，有时预定义的答案集合不适合用户表达自己的需求。当这种情况发生时，为用户提供一个可以输入其文本反馈的文本字段可能很有用。然而，基于文本的反馈存在限制，因为典型的分析指标（如计算数据库列的总和）无法执行。

要从文本中获取洞察，需要额外的处理来识别文本或术语的相关性和重要性。本章将回顾可以对文本执行的处理方法以及识别价值和相关性的指标。

## 5.2 自然语言处理

自然语言处理（NLP）领域可以追溯到 1950 年代早期。由于文本是我们主要的交流形式之一，利用文本的软件自然成为研究人员感兴趣的领域。原始形式的文本通常需要进一步处理，以浓缩和提取有意义的见解。

在商业环境中，分析师希望用户在描述所遇到的问题时尽可能具体。然而，用户在描述问题时经常使用错误的关键词或术语。除此之外，与数字数据不同，基于文本的数据可能有不同的形式。示例包括：

- 单个单词或单个句子；
- 脱离上下文的大段文本；
- 对服务或产品没有真正反映的不利反馈。

与其他数据格式不同，句子中的标点和顺序会影响含义。以下句子中的一个例子：`I really hated how well the people at the front desk treated me. I am shocked!` 当对这个句子进行简单分析时，对于像 `hate` 这样的负面词汇，其周围的词语 `I really hated` 可能被视为针对前台员工的负面内容。然而，当保留句子的完整上下文时，我们可以看到这是一句真诚的赞美。

在接下来的每一节中，我们将处理可能包含单个单词、单个句子或多个不同句子的文本。由于这些文本是由不同用户输入的，因此不能对数据的格式、内容或质量做任何假设。一些用户可能选择使用正确的标点符号，而其他用户可能只创建长句。这些不确定性增加了处理文本的难度。

## 5.3 停用词

用户输入的单条文本包含两种主要类型的术语：

1. 对于理解用户所说的有用处的术语；
2. 用于将句子连接在一起的术语。

停用词被认为是句子中的粘合剂，停用词的示例包括：`as`、`the`、`it`、`on`、`which` 和 `that`。这些术语中的每一个都没有向我们描述任何特定的东西。如果这些术语从文本中删除，阅读文本的人仍然会理解用户想要说什么。另一个例子是句子 `to be or not to be`，每个术语都可以被视为停用词。

在分析过程中，这些术语通常在进行任何进一步处理之前从文本中删除。然而，没有官方的停用词列表。单词的长度并不一定意味着它是一个停用词。然而，停用词通常是一个或两个字符长。

当术语至关重要时，停用词常常会引发问题。一个例子是乐队名称 `The Who`。当停用词被移除时，例如术语 `The`，我们将剩下乐队名称 `Who`。这同样适用于乐队名称 `Take That`，两个术语可以被视为停用词。这进一步强化了为什么没有官方停用词列表的原因。

MySQL 的 InnoDB<sup>1</sup> 存储引擎默认包含 36 个不同的词作为停用词。

Python NLTK 库的英文停用词列表包含 127 个词。<sup>2</sup>

词汇的多样性以及应用特定停用词的需求，常常导致我们需要建立自己的停用词集合。随着任务的变化，可以向此词集合中添加或删除词语。

当我们查看一个词汇集合时，通常需要考虑文本的大小写情况。

- 一个例子是，当你的停用词列表中包含单词 `the`，但我们句子中的单词是首字母大写的 `The`，我们通常会发现需要在文本处理期间将文本转换为小写，以避免遗漏该词。

文本处理阶段需要考虑的另一个因素是处理应在何处进行。

我们可以选择使用像 `PHP` 这样的服务器端语言执行这些操作，将负担放在服务器上，或者我们可以选择使用像 JavaScript 这样的客户端语言，将负担放在用户的网络浏览器上。

反馈的另一个有趣元素是文本中使用脏话。

脏话通常不会给数据增添任何价值，但我们常常可以选择从文本中删除这些脏话（为了分析师）。众所周知，有很多常见的脏话，但通常随着人们在方法或侮辱性语言上变得更有创造力，脏话列表也会不断扩展。

与停用词类似，没有官方的脏话列表。然而，我们可以选择使用不同地点获取脏话列表。

- <https://www.cs.cmu.edu/~biglou/resources/bad-words.txt>
- <https://en.wikipedia.org/wiki/English_swear_words>

众所周知，有很多常见的脏话。

- <https://www.cs.cmu.edu/~biglou/resources/bad-words.txt>

由于脏话通常可以被描绘成积极或消极的含义，它们可能与将其从文本中删除的任务无关。如果它们确实出现，这是个人试图表达对服务体验的严重不满。

- <https://www.cs.cmu.edu/~biglou/resources/bad-words.txt>
- <https://en.wiktionary.org/wiki/Category:English_swear_words>

由于脏话通常可以被描绘成积极或消极的含义，它们可能与将其从文本中删除的任务无关。如果它们确实出现，这是个人试图表达对服务体验的严重不满。

- <https://en.wiktionary.org/wiki/Category:English_swear_words>

由于脏话通常可以被描绘成积极或消极的含义，它们可能与将其从文本中删除的任务无关。如果它们确实出现，这是个人试图表达对服务体验的严重不满。

- <https://en.wiktionary.org/wiki/Category:English_swear_words>

由于脏话通常可以被描绘成积极或消极的含义，它们可能与将其从文本中删除的任务无关。如果它们确实出现，这是个人试图表达对服务体验的严重不满。

- <https://en.wiktionary.org/wiki/Category:English_swear_words>

由于脏话通常可以被描绘成积极或消极的含义，它们可能与将其从文本中删除的任务无关。如果它们确实出现，这是个人试图表达对服务体验的严重不满。

- 由于脏话通常可以被描绘成积极或消极的含义，它们可能与将其从文本中删除的任务无关。如果它们确实出现，这是个人试图表达对服务体验的严重不满。

- 人们经常用积极或消极的情绪来表达自己的感受，这是很常见的事情。

### 示例 1：JavaScript 停用词函数

由于停用词可以在客户端和服务器端被移除，本节我们将描述一种基于 JavaScript 的方法。

#### 示例代码：`stopwords.html`

在示例代码 1 中，第 3 行首先包含了对 jQuery 内容分发网络（CDN）的引用。这将在稍后用于选择页面上的 `div` 标签。在第 7 行，创建了一个名为 `sampleSentence` 的变量，其中包含一个包含停用词的句子。在第 8 行，创建了一个名为 `stripStopWords()` 的新函数。此函数接受一个名为 `input` 的单一变量。此变量处于未处理状态。

在此函数内部的第 9 行，添加了一个占位符变量，该变量将用作清理后数据的位置，因为停用词将从原始 `input` 中移除。在第 10 行，创建了一个 JavaScript 数组，其中包含每个 MySQL 停用词作为数组的独立元素。之后在第 15 行，传入函数的 `input` 变量根据单词之间的空格进行分割，并放入一个名为 `termArray` 的数组中。

一旦我们将每个独立的词放入 `termArray`，我们就开始检测输入中是否存在停用词的过程。这是通过使用 `for` 循环遍历词数组中的每个词来完成的。`for` 循环的每次迭代在第 17 行，从 `termArray` 的位置 `i` 中取出一个词。这个变量 `i` 引用数组中的当前位置。该词被取出并放入一个名为 `currentTerm` 的临时变量中。

在第 18 行，使用一个简单的 `if` 语句来检查我们当前处理的词是否可以在停用词列表中找到。这是通过使用 JavaScript 数组的 `indexOf()` 函数来完成的。如果返回一个正数，则标识该词存在；如果返回负数，则意味着该词不存在。

如果该词不存在，在第 20 行，`currentTerm` 被追加到 `cleaned` 变量上。记住在追加当前词之前添加一个空格很重要。否则，所有词将连在一起。在此函数的最后，在第 24 行，添加了一个简单的 `return` 语句，以将清理后的字符串返回给函数调用者。

在页面底部的第 27–32 行，为了在 Web 浏览器中提供输出，创建了两个 `div` 标签，一个包含 `ID` `output1`，另一个包含 `ID output2`。为了测试第 33 行的函数，我们首先将使用 jQuery 选择器选择 ID 为 `output1` 的 `div` 标签，并以原始形式追加变量 `sampleSentence`。完成此操作后，在第 35 行，我们将创建一个名为 `cleaned` 的变量，该变量用于存储调用传入 `sampleSentence` 变量的 `stripStopWords()` 函数后的结果。

一旦 `cleaned` 变量有了结果，输出将在第 36 行追加到第二个 ID 设置为 `output2` 的 `div` 标签上。

```html
<head>
    <script
        src="http://code.jquery.com/jquery-3.5.1.min.js"
        crossorigin="anonymous"></script>
</head>

<script>
var sampleSentence = "what a great night I loved the food";

function stripStopWords(input) {
    var cleaned = '';

    var stopwords = [
        "a", "about", "an", "are", "as", "at", "be", "by",
        "com", "de", "en",
        "for", "from", "how", "i", "in", "is", "it", "la", "of",
        "on", "or", "that", "the", "this", "to", "was", "what",
        "when", "where", "who", "will", "with", "und", "the", "www"
    ];

    var termArray = input.split(" ");

    for (i = 0; i < termArray.length; i++) {
        var currentTerm = termArray[i];

        if (stopwords.indexOf(currentTerm) >= 0) {
        } else {
            cleaned += " " + currentTerm;
        }
    }

    return cleaned;
}
</script>

<div id="output1">
    <b>Before Filter:</b>
</div>

<div id="output2">
    <bafter filter:="" b="">
</div>

<script>
$('#output1').append(sampleSentence);

var cleaned = stripStopWords(sampleSentence);

$('#output2').append(cleaned);
</script>
```

示例代码 1：`stopwords.html` — JavaScript 停用词函数。

#### 输出

执行上述操作后，在 Web 浏览器中我们可以看到原始字符串以及处理后的字符串，如图 5.1 所示。

**过滤前：** what a great night i loved the food

**过滤后：** great night loved food

在“过滤后”的结果中，我们仍然保留了反馈核心的原始描述性词语，但那些对描述没有附加价值的词语已被移除。在每一个阶段，如果有一些我们不希望出现在输出中的词语，只需将这些自定义停用词添加到原始停用词数组中即可。

### 示例 2：PHP 停用词函数

除了基于客户端的过滤方式外，我们还可以在服务器端使用 PHP 执行相同的操作，因为记录通常是通过 PHP 从数据库中检索的，这为我们提供了执行此清理操作的良好机会。

#### 示例代码：`stopwords.php`

在示例代码中，创建了一个新的 PHP 页面。在第 2 行，创建了一个名为 `stripStopWords()` 的新函数。该函数接受一个名为 `input` 的单一参数，其中包含要处理的文本。

```php
1 <?php

2 function stripStopWords($input) {
3     $cleaned = '';
4     $stopwords = array(
5         "a", "about", "an", "are", "as", "at", "be",
6         "by", "com", "de", "en", "for", "from", "how", "I",
7         "in", "is", "it", "la", "of", "on", "or", "that",
8         "the", "this", "to", "was", "what", "when", "where",
9         "who", "will", "with", "und", "the", "www"
10    );

11    $inputArray = explode(' ', strtolower($input));

12    foreach ($inputArray as $inputword) {
13        $isStopWord = False;

14        foreach ($stopwords as $word) {
15            if ($inputword == $word) {
16                $isStopWord = True;
17            }
18        }

19        if ($isStopWord == False) {
20            $cleaned .= ' ' . $inputword;
21        }
22    }

23    return $cleaned;
24 }

25 $input = 'I am really happy with the service';
26 echo 'Input:' . $input . '<br>';
27 $result = stripStopWords($input);
28 echo 'Result: ' . $result;
```

示例代码 2：`stopwords.php` — PHP 停用词函数。

#### 输出

图 5.2 展示了使用 PHP 进行停用词移除后的输入和输出。

```text
Input: I am really happy with the service

Result: am really happy service
```

图 5.2：`stopwords.php` — 使用 PHP 进行停用词移除前后的对比。

## 5.4 红旗词监控

与停用词类似，红旗词可以被视为文本中需要重点关注的词语。红旗词可能是一些很少被提及的词语，但当它们出现时，应当被识别出来。在处理大量文本集合时，这种方法非常有用，因为庞大的数据量会使得逐篇阅读单条文本变得困难。

### 示例 3：红旗词仪表板选项

本示例包含四个文件和两个库：

1. `reflag.comments.sql` — 这是包含示例评论的数据库表的创建代码。
2. `reflagterms.sql` — 这是包含被识别为红旗词列表的数据库表。
3. `dashboard.php` — 带有额外红旗词模态框的原始仪表板。
4. `redFlags.php` — 通过 jQuery 动态调用的附加文件，用于渲染带有高亮红旗词的被选记录。
5. jQuery — 用于选择页面上的元素并执行 AJAX POST 请求。
6. jQueryUI — 用于提供交互式日期选择器。

红旗词可能是引起企业关注的词语。在流程开始之前，我们将创建一个示例词语集合，这些词语被我们视为红旗词。本示例中使用的词语包括 `staff` 和 `breakfast`。

#### 示例代码：`redflag_comments.sql`

首先，我们将创建一个名为 `redflags_comments` 的简单表，如示例代码 3 所示，用于存放我们的测试数据。该表包含一个唯一的 `ID` 列，以及一个名为 `mytime` 的列，用于记录评论提交的时间。添加了一个 `comment` 列来存储反馈过程中从用户收集的文本。另外添加了一个名为 `cid` 的列，用于存储此特定活动的 ID 编号。




```sql
CREATE TABLE `redflag_comments` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `mytime` DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `comments` TEXT,
  `cid` INT,
  PRIMARY KEY (`id`)
);
```

示例代码 3：`redflag_comments` 表的 SQL。

由于每个不同的活动可能有一组不同的被视为红旗词的术语，因此创建了如示例代码 6 所示的名为`redflagterms`的表。每个单独的词语与活动 ID 一起作为一行存储在该表的`cid`列中。

```sql
CREATE TABLE `redflagterms` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `term` VARCHAR(50),
  `cid` INT,
  PRIMARY KEY (`id`)
);
```

示例代码 4：`redflagterms` 表。

为了提供一个可运行的示例，该数据库表将填充如图 5.3 所示的示例数据。

|  | timestamp | comments | cid |
|---|---|---|---|
| 1 | 2018-08-05 10:24:29 | The staff are horrible here, I am really not hap... | 1 |
| 2 | 2019-08-05 10:24:51 | The staff have been great, I am really not hap... | 1 |
| 3 | 2019-08-05 10:25:09 | I was five minutes late and they said i can not ... | 1 |
| 4 | 2019-08-05 10:25:37 | The breakfast was great. | 1 |
| 5 | 2019-08-05 10:25:43 | More coffee is needed at breakfast time. How ... | 1 |
| 6 | 2019-08-05 21:09:23 | breakfast was good but the staff are great | 1 |

图 5.3：示例评论记录。

## 示例代码：`dashboard.php`

在第四章描述的仪表板基础上，添加了额外的 HTML 和 JavaScript 以包含显示文本中红旗词的新选项。在示例代码 5 中，为了向用户展示选项，创建了一个 Bootstrap 模态框。在第 2 行，模态框的 ID 设置为`selectRanges`。在第 15 行，添加了一个`class`设置为`modal-body`的`div`标签。这是放置内容的主要位置。在该标签中，我们将为用户提供两个不同的 jQueryUI 日期选择器，允许用户为分析过程选择日期范围。在第 16、21 和 26 行，添加了`div`标签以创建单独的行。在第 17 行，文本“Start Date:”被添加到`class`设置为`col`的`div`标签内。在第 18 和 23 行，添加了输入字段，这些字段将使用 jQueryUI 转换为日期选择器。在第 28 行添加了第三个字段，允许用户输入感兴趣的 CID。在第 35 行添加了“Show Red Flags”按钮。`onclick`属性设置为调用稍后描述的`showRedFlags()` JavaScript 函数。

```html
<!---- Red Flag Modal -->

<div class="modal fade" id="selectRanges" tabindex="-1"
  role="dialog" aria-labelledby="selectRanges"
  aria-hidden="true">

  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="addAtt">Select Date Ranges</h5>
        <button type="button" class="close" data-dismiss="modal"
          aria-label="Close">
```

# 164 ■ 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

### 输出

在仪表板上，当点击名为“Text Analysis”的项目时，会出现一个标题为“View Red Flags”的菜单，如图 5.4 所示。图 5.5 展示了模态框的布局。当用户点击任意一个输入框时，日期选择器将变得可见，如图 5.6 所示。它们选择的值将被填入输入字段。

![](img/ed4cb7e1be98f0adec0546edd14f6223_187_0.png)

图 5.4：查看红旗标记菜单选项。

![](img/ed4cb7e1be98f0adec0546edd14f6223_187_1.png)

图 5.5：选择日期和 CID 的模态框。

### 示例代码：`redFlags.php`

这个过程的核心位于`redFlags.php`页面。在示例代码 7 中，该页面顶部的第 2—4 行，从 GET 请求中获取开始日期、结束日期和 CID。第 5 行输出一个新的`div`标签到页面。第 6 行将开始日期、结束日期和 CID 回显到页面。第 9 行调用`getData()`函数，该函数负责收集数据。

`getData()`函数在第 12 行定义。在此函数内部，第 19 行建立与数据库的连接。第 21 行添加了针对`redflag_comments`表的`SELECT`语句。评论根据用户指定的两个日期之间的时间戳进行筛选。CID 用于对单个指定活动的记录进行最终聚合。

第 31 行调用`getRedFlags()`函数，以获取单个活动的特定红旗标记列表。对于从数据库返回的每条评论，第 34 行使用`explode()`函数根据评论中每个术语之间的空格进行分割。每个单独的术语被转换为小写。

第 39 行添加了一个名为`output`的 PHP 变量，该变量将随着每条评论的迭代而被追加内容。第 37 行，将来自评论的单个`inputWord`与`redFlags`数组进行比较。这是通过使用 PHP 的`in_array()`函数完成的，该函数检查给定术语是否存在于提供的数组中。

第 39 行，如果当前分析的术语存在于`redFlags`数组中，则使用少量 CSS 样式将该术语的颜色设置为红色。如果不存在，则直接将其追加到字符串中。最终结果使用 PHP 的`echo`打印到浏览器。

```php
<?php

$start = $_GET['start'];
$end = $_GET['end'];
$cid = $_GET['cid'];

echo '<div id="redflags">';
echo '<b>Start:</b> ' . $start . ' - <b>End date:</b> ' . $end .
     ' - <b>CID:</b> ' . $cid . '<br>';
echo '<hr>';

getData();

echo '</div>';

function getData()
{
    global $start, $end, $cid;

    try {
        $host = 'localhost:3306';
        $dbname = 'test';
        $user = 'root';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);

        $sql = "SELECT * FROM redflag_comments WHERE mytime
                BETWEEN ?
                AND ? AND cid = ?";

        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $start, PDO::PARAM_STR);
        $sth->bindParam(2, $end, PDO::PARAM_STR);
        $sth->bindParam(3, $cid, PDO::PARAM_INT);
        $sth->execute();

        $res = $sth->fetchAll();

        // 从数据库获取红旗标记列表
        $redFlags = getRedFlags($cid);

        foreach ($res as $row) {
            $comment = $row[2];
            $inputArray = explode(' ', strtolower($comment));
            $output = '';

            foreach ($inputArray as $inputWord) {
                $isFlag = in_array($inputWord, $redFlags);

                if ($isFlag) {
                    $output .= '<span style="color:red">' .
                               $inputWord . '</span> ';
                } else {
                    $output .= ' ' . $inputWord;
                }
            }

            echo $output . '<br>';
        }
    } catch (PDOException $e) {
        echo $e;
    }
}
```

示例代码 7：`redFlags.php` — 识别红旗标记术语 - 第 1 部分。

在示例代码 8 中，为了获取每个活动的唯一红旗标记列表，创建了一个自定义的`getRedFlags()`函数，该函数接受一个参数，即 CID。在该函数顶部，第 45 行添加了一个名为`flags`的数组。第 51 行执行数据库连接。

第 53 行创建了一个`SELECT`语句，用于从`redflagterms`表中选择数据。结果通过返回仅 CID 等于提供给函数的值的记录进行筛选。对于每个术语，第 59 行将它们追加到`flags`数组中，该数组在第 63 行返回，并用作分析每条评论时的红旗标记源。

```php
function getRedFlags($cid)
{
    $flags = array();

    try {
        // 创建数据库连接
        $host = 'localhost:3306';
        $dbname = 'test';
        $user = 'root';
        $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

        $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);

        $sql = "SELECT term FROM redflagterms WHERE cid = ?";
        $sth = $DBH->prepare($sql);
        $sth->bindParam(1, $cid, PDO::PARAM_STR);
        $sth->execute();

        $res = $sth->fetchAll();

        foreach ($res as $row) {
            array_push($flags, $row[0]);
        }
    } catch (PDOException $e) {
        echo $e;
    }

    return $flags;
}
```

示例代码 8：`redFlags.php` — 检索红旗标记术语列表 - 第 2 部分。

## 仪表盘

开始：2018-01-08 - 结束日期：2020-01-01 - CID：1

这里的员工非常糟糕，我真的很不开心。

员工表现一直很好，但我不喜欢泳池。

我迟到了五分钟，他们说我不能吃早餐。

早餐很棒。

早餐时间需要更多的咖啡。没有它我怎么能工作？

早餐不错，但员工很优秀。

**图 5.7**：每个评论输出时，警示性术语被高亮显示。

### 输出

在**图 5.7**中，可以看到存储在数据库中的一系列评论。每个警示性术语都以红色高亮显示。用户选择的开始日期和结束日期也已显示，活动 ID 显示为 CID。

## 5.5 N-Gram

在处理基于文本的数据时，一个常见的做法是创建 n-grams。在此过程介绍之前，我们将首先对文档结构进行概述。文档 D 由 P 个独立段落组成。每个段落可包含 S 个独立句子，每个句子包含 W 个单词。每个独立句子包含来自`$W_0...W_y$`的词。

尽管文档可以被视为独立术语的集合，但这些术语周围的上下文可以提供有价值的见解，说明术语是如何被使用的。考虑到句子 *I was shocked, the service was great!*，如果对该句子进行词频分析：

|  |
|---|
| - 员工 |
| - 员工是 |
| - 是糟糕的 |
| - 这里糟糕 |
| - 这里我 |
| - 我 |
| - 真的很 |
| - 真的很不 |
| - 不高兴 |

|  |
|---|
| - 员工是 |
| - 员工很糟糕 |
| - 糟糕在这里 |
| - 这里在我 |
| - 我在真的 |
| - 我真的很不 |
| - 真的很不高兴 |

每个术语的权重将为 1，因为每个术语仅出现一次。如果在不考虑上下文的情况下提取这些术语，术语`shocked`将被视为负面术语，因为没有提供额外上下文。

为此，可以生成 n-grams。N-Gram 接收一个包含`$W_0...W_y$`术语的句子`$S$`作为输入。N-Gram 算法采用参数`$N$`，识别单个序列中应包含的术语数量。在 N-Gram 处理过程中，不同的`$N$`值会产生截然不同的结果。二元组（Bi-grams）是指当`$N`设置为 2 时。对于句子 *The staff are horrible here I am really not happy*，表 5.1 显示了当`$N = 2$`时的输出。

三元组（Tri-grams）是指当`$N = 3$`时。与之前的示例不同，三元组包含大量的上下文信息。表 5.2 显示了当`$N = 3$`时的输出。

### 示例 4：生成 n-grams

在数据分析过程中使用 N-Gram 的优势是保留了术语周围的额外上下文。这在记录数量超过人工审查过程时尤其有用。

### 代码示例：`ngram.php`

代码示例 9 描述了一种简单的 N-Gram 方法。第 2 行的`sentence`变量存储待处理的句子。为了将句子分解为独立标记，第 3 行使用了`explode()`函数。该函数接受带有两个引号且中间有一个空格的内容。这是分隔符，用作拆分句子时依据的 token。传递的第二个变量是包含文本的`sentence`变量。

由于我们将处理任意数量的 n-gram，第 4 行添加了一个名为`gram`的变量。对于`$N = 2`的句子 *This is a sample sentence*，`gram`变量将首先包含词项`The`，接着是一个空格，然后添加第二个词项`staff`。由于要添加的 n-gram 数量等于 2，则打印`gram`变量，并清除该变量，以便在下一次迭代中重用。

这段代码包含两个循环，第一个在第 6 行循环遍历每个独立术语，而第二个在第 8 行的循环上针对单个术语添加`$Y`数量的 n-grams。第 9 行使用了一个名为`counter`的小内部变量，用于跟踪已添加的 n-gram 数量。当计数器等于期望的标记数量时，向浏览器打印`gram`变量，随后是一个`br`标签以换行。该变量被清除，然后在第 14 行使用`break`语句终止循环。这将允许外部循环继续进行到下一个术语。此代码可以通过修改`n`变量来用于任何数量的 n-gram 序列。

```php
<?php

$sentence = 'The staff are horrible here';
$tokens = explode(' ', $sentence);
$gram = '';
$n = 2;

for ($x = 0; $x <= sizeof($tokens) - 1; $x++) {
    $counter = 0;

    for ($y = $x; $y <= sizeof($tokens) - 1; $y++) {
        $counter++;
        $gram .= ' ' . $tokens[$y];

        if ($counter == $n) {
            echo $gram . '<br>';
            $gram = '';
            break;
        }
    }
}
```



## 代码示例 9：`ngram.php` — PHP N-Gram 算法

### 输出

图 5.8 展示了句子 *The staff are horrible here* 的 N-Gram 输出，其中 `N=2`。

![img/ed4cb7e1be98f0adec0546edd14f6223_194_0.png](img/ed4cb7e1be98f0adec0546edd14f6223_194_0.png)

**图 5.8：** `N=2` 时的样本 N-Gram 输出。

## 5.6 句子补全

在处理大量用户评论时，常常可以观察到特定一起使用的词汇之间存在重叠。在以下评论中可以见到单词 *staff* 的示例：

1. The staff are great.
2. I had fun. The staff made the experience even better.
3. Good food, but the staff were nasty.

这三条评论都描述了客户对员工的感受，然而最后一条是负面评论。这在分析中很有益，因为关于某个主题的评论（例如员工）可能会引发调查的开始，以查看为何留下了那一条特定的负面反馈。

然而，提出的问题是该如何看待这些数据。关于员工的少量信息可能隐藏在一个较大的段落或文本主体中。使用句子补全可以极大地增强文本分析，在出现感兴趣的术语之前修剪掉不相关的文本，只留下相关文本。这是通过首先开始于单个术语或一组被视为句子词干（stem）的术语来实现的。

### 示例 5：句子补全

此示例包含两个文件：

1. `create.sql` — 此文件用于创建 `feedback_wild` 数据库表。
2. `completion.php` — 此文件提供了句子补全的示例。

### 代码示例：`create.sql`

首先，代码示例 10 以名为 `feedback_wild` 的简单 SQL 表开始。该表包含一个名为 `feedback` 的列，用于保存句子补全过程的样本记录。

```sql
1 CREATE TABLE IF NOT EXISTS `feedback_wild` (
2     `id` INT NOT NULL AUTO_INCREMENT,
3     `mytime` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP,
4     `feedback` text,
5     PRIMARY KEY (`id`)
6 );
```

**代码示例 10：** `feedback_wild` 数据库表。

### 代码示例：`completion.php`

在代码示例 11 中，第 7 行首先建立与数据库的连接。第 9 行添加了一个名为 `rootWords` 的变量。该变量包含感兴趣的术语。在此示例中，我们要搜索单词 *staff*。

在第 10 行，创建了 SQL 片段。在 `rootWords` 变量开头和结尾添加百分号（表示通配符），并放入一个名为 `likeString` 的新变量中。

百分号表示该术语可以在反馈记录的任何位置找到，例如开头、结尾或句子中间。

在第 11 行，创建了一个 SQL 查询，`LIKE` 的值使用问号占位符。在查询中使用了一个无名占位符，显示为问号。

在第 13 行调用 `execute()` 函数期间，准备好的 `rootWords` 变量以 `likeString` 的形式传递。

一旦查询执行完毕，在第 14 行，使用一个 `while` 循环来遍历已识别的记录。第 15 行，将 `feedback` 列中存储的文本数据放入名为 `record` 的局部变量中。之后在第 16 行，使用 `strpos()` 函数来定位术语 *staff* 首次出现的索引位置。

在第 17 行，调用了 `substr()` 函数。该函数接受三个参数。第一个是包含我们要处理的文本的变量。第二个是我们希望开始处理的起始索引。最后，第三个参数是我们希望停止处理的索引号。在此示例中，该索引被设置为使用 `strlen()` 函数找到的 `record` 变量的长度。`substr()` 的结果通过一个简单的 `echo` 语句打印到浏览器。

```php
<?php

try {
    $host = '127.0.0.1:3306';
    $dbname = 'test';
    $user = 'root';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);

    $rootWords = 'staff';
    $likeString = '%' . $rootWords . '%';

    $stmt = $DBH->prepare("SELECT * FROM feedback_wild WHERE
        feedback LIKE ?");

    $stmt->execute([$likeString]);

    while ($row = $stmt->fetch(PDO::FETCH_ASSOC)) {
        $record = $row['feedback'];
        $start = strpos($record, "staff");
        echo substr($record, $start, strlen($record)) . '<br>';
    }
} catch (PDOException $e) {
    echo $e;
}
```

**示例代码 11：** `completion.php` — 针对术语 *staff* 的句子补全。

### 输出

图 5.9 展示了在句子开头和中间找到术语 *staff* 的示例。所有位于关注术语之前的文本都被忽略，只留下关注术语及其后的句子其余部分。

```text
staff are horrible here, I am really not happy.
staff have been great, I am really not happy about the pool.
staff are great
```

**图 5.9：** 在反馈记录中搜索单词 *staff* 的结果。

## 5.7 词干提取

在处理术语时，根据单词的用法不同，它们常常会有不同的后缀。以术语 *house* 为例，如果它在句子中使用，常见的变体有 *Houses*、*House* 和 *Housing*。然而，问题在于如果进行任何计算，例如统计单词出现的次数，通常会漏掉该术语的其他变体。

### 示例 6：词干提取

为了防止这种情况发生，在处理文本集合时可以进行 *词干提取*。这是将术语还原为词干的过程。在词干提取时可以采用许多不同的方法。词干提取工具的一个例子是 Porter Stemmer。在本示例中，我们将使用该算法的一个 PHP 实现。³

本示例包含两个文件：

- `stemming.php` — Porter 词干提取用法的一个示例实例。
- `PorterStemmer` — 词干提取算法的一个实例。

### 示例代码：`stemming.php`

在示例代码 12 中，第 2 行首先将库添加到当前页面。要进行词干提取的单词被放入第 3 行的 `word` 变量中。该变量在第 4 行被传递给 `Stem` 函数。该函数返回词干并打印到页面上。术语 Houses、House 和 Housing 的词干提取过程均已完成。HTML `br` 标签用于将输出分隔到单独的行。

```php
<?php

require('PorterStemmer.php');

$word = 'Houses';
$stem = PorterStemmer::Stem($word);
echo $stem . '<br>';

$word = 'House';
$stem = PorterStemmer::Stem($word);
echo $stem . '<br>';

$word = 'Housing';
$stem = PorterStemmer::Stem($word);
echo $stem . '<br>';
```

**示例代码 12：** `stemming.php` — 对三个术语使用 Porter Stemmer。

### 输出

图 5.10 显示了词干提取过程的输出。尽管向词干提取算法传递了三个不同的单词，但每次调用后都返回了相同的词干。这种方法有助于我们识别出这三个术语都是相关的。

```text
Hous
Hous
Hous
```

**图 5.10：** 调用词干提取算法后的结果。

## 5.8 同义词

在审查反馈记录时，可以很快发现两个评论永远不会包含相似的短语或术语集合。这可能会给任何需要在术语之间进行匹配的反馈处理带来困难。例如，当一条记录中使用术语 *chef* 而另一条记录中使用术语 *cook* 时就会出现这种情况。通过开发一个识别这些同义词的函数，为分析过程增加了另一个维度。

### 示例 7：BigHugeLabs.com API

在本示例中，我们将概述使用 BigHugeLabs.com API 获取给定术语同义词的过程。此过程的第一步是获取访问该服务的 API 密钥。他们目前每天提供 500 次免费请求。可以支付少量费用进行额外的服务调用。要获取此密钥，首先需要创建一个账户。图 5.11 描述了注册密钥所需的参数。添加应用程序的简要描述，然后是请求将来自的 URL。由于这是一个测试应用程序，URL 添加了 *localhost*。

### 获取 API 密钥

描述您的应用程序。

请尽可能详细。如果您是为应用程序请求密钥的用户，请提及该应用程序。

test application

网站/应用商店 URL

localhost

**图 5.11：** BigHugeLabs.com API 密钥创建过程。

密钥创建完成后，会显示示例 REST URL。每个 URL 都将唯一的 API 密钥连同单个关注单词传递给服务。每个 API URL 的区别在于返回响应的格式。图 5.12 显示了可用的选项，包括纯文本、XML 或 JSON。

### 输出

在示例代码 13 中，构建了 API URL。传递的第一个参数是唯一的 API 访问密钥。术语 *dad* 作为关注术语传递给 API。为了辅助处理结果，URL 末尾附加了 `/json`，以便以 JSON 格式检索结果。

176 ■ 应用 JavaScript 和 PHP 进行用户数据收集与分析

```text
示例 REST URL

纯文本

https://words.bighugelabs.com/api/2/0c7cc83b387027012538b959c8576cfb/word/

XML

https://words.bighugelabs.com/api/2/0c7cc83b387027012538b959c8576cfb/word/xml

JSON

https://words.bighugelabs.com/api/2/0c7cc83b387027012538b959c8576cfb/word/json

序列化 PHP

https://words.bighugelabs.com/api/2/0c7cc83b387027012538b959c8576cfb/word/php
```

**图 5.12：** BigHugeLabs.com 示例 REST URL。

```text
https://words.bighugelabs.com/api/2/0c7cc83b387027012538b959c8576cfb/dad/json
```

**示例代码 13：** 传递术语 *dad* 的完整 API 调用。

示例代码 14 显示了包含术语 *dad* 同义词的结果集。

```json
{
  "noun": {
    "syn": [
      "dada",
      "daddy",
      "pa",
      "papa",
      "pappa",
      "pop",
      "begetter",
      "father",
      "male parent"
    ]
  }
}
```

**示例代码 14：** 返回的术语 *dad* 的同义词。

在计算包含术语 *dad* 的反馈记录数量时，如果发现任何同义词，可以包含额外的记录。尽管这是分析过程中一个有用的工具，但也确实存在一些问题。一个例子是 *dad* 的同义词 *pop*。由于在处理文本时通常会移除上下文，因此很难确定这是指一个人的 *dad* 还是指 *soda*（汽水）的同义词 *pop*。

### 示例 8：PHP 向 Big Huge Lab 的 API 发起请求

为了从 PHP 访问 REST API，我们可以使用 `file_get_contents()` 函数。这允许我们传递 API 的 URL，该 URL 包含一个名为 `term` 的变量，其中包含关注的术语。

### 示例代码：`syn.php`

在示例代码 15 中，第 2 行首先定义了关注的术语。在本示例中，我们搜索术语 *dad* 的同义词。第 3 行调用了 PHP 的 `file_get_contents()` 函数。该函数将向提供的 URL 发起一个 `GET` 请求。变量 `term` 的值被替换到字符串中。输出的页面内容被放入名为 `result` 的局部变量中。

该服务将返回 JSON 内容。第 5 行，为了处理 JSON，将结果传递给 `json_decode()` 函数。传递了 `true` 参数以确保结果以关联数组的形式返回。第 6 行，在 `decoded` 变量被填充后，我们可以传递一个键来从数组中选择结果。`noun` 是父级结果。在其中，可以访问 `syn` 集合。

一旦我们访问了 `syn` 结果，第 7 行使用一个 `foreach` 语句来遍历每个单独的同义词。当在 Web 浏览器中查看结果时，添加了一个简单的 `br` 标签，将每个结果换行到新行。

```php
<?php

$term = 'dad';

$result = file_get_contents(
    "https://words.bighugelabs.com/api/2/"
    . "0c7cc83b387027012538b959c8576cfb/$term/json"
);

$decoded = json_decode($result, true);

$syn = $decoded['noun']['syn'];

foreach ($syn as $item) {
    echo $item . '<br>';
}
```

**示例代码 15：** `syn.php` — 使用 PHP 调用 BigHugeLabs API。

图 5.13 展示了将术语 *dad* 传递给 Big Huge Lab 同义词 API 后的输出结果。

![](img/ed4cb7e1be98f0adec0546edd14f6223_202_0.png)

**图 5.13：** 通过 `GET` 请求调用 Big Huge Labs API 返回的同义词示例。

## 5.9 术语加权

在前面的示例中，文本从数据库中收集，并直接对文本执行不同的任务，而无需任何额外处理。这种方法的一个问题是解决方案的可扩展性。当处理少量记录时，搜索文本的过程可以轻松执行并获取洞察。然而，当分析数百或数千条记录时，任何数据应用都会迅速变得困难，因为不相关的文本可能在结果中变得突出。因此，可以应用额外的度量标准来识别文本的重要性。

### 示例 9：词频

一个可用于辅助分析过程的简单方法是为单个术语应用权重。最简单的方法是计算每个单独词语在所有记录中被发现的次数。在本例中，我们将考虑表 5.3 中显示的五个单独记录。

**表 5.3：** 用于词频的示例记录。

| ID | 反馈 |
|:--:|:---|
| 1 | 我对邮寄收到的产品非常满意。但是，包裹的包装处理得很糟糕。 |
| 2 | 我对我收到的产品非常满意。将来我会再次光顾。 |
| 3 | 这家公司的客户服务存在很多问题。我会把我的业务转移到别处。这是一次糟糕的体验。 |
| 4 | 我再也不会回来了。前台的人对我态度恶劣。 |
| 5 | 这是一家很棒的公司，我永远不会去别处。 |

### 示例代码：`tf.php`

为了计算每个单词的词频，需要计算每个术语在所有记录中的总计数。

在示例代码 16 中，第 2—6 行将单个记录作为字符串添加。在第 8 行，创建了一个数组，用作字符串的主要存储位置。在第 9—13 行，每个单独的字符串被添加到数组中。在第 14 行，创建了一个新数组，用于存放所有单独的术语。在第 15 行，使用一个简单的 `foreach` 语句遍历所有记录。对于每个单独的记录，在第 17 行，句号和逗号从字符串中被移除并替换为空格。在第 18 行，调用 `explode()` 函数，在每次遇到空格时将单个字符串分解为单独的术语。

在第 20 行，每个单独的术语被添加到 `allWords` 数组中。最后在第 24 行，调用 `array_count_values()` 函数，该函数将计算数组中每个术语的总出现次数。该输出使用 `print_r()` 函数打印到浏览器。

```php
<?php

$doc1 = 'I was very happy with the product that I got in the
 mail. However, the package was handled badly.';

$doc2 = 'I am very happy with the product that I got. I will
 come back again in the future.';

$doc3 = 'There was a number of issues with the customer service
 of this company. I will take my business somewhere else. It
 was a bad experience.';

$doc4 = 'I will never return. I was treated badly by the man on
 the front desk.';
```



```php
$doc5 = 'This is a great company, I will never go elsewhere.';

$documents = array();

array_push($documents, $doc1);
array_push($documents, $doc2);
array_push($documents, $doc3);
array_push($documents, $doc4);
array_push($documents, $doc5);

$allWords = array();

foreach($documents as $doc){
    echo '----------document----------<br>';

    $cleaned = strtr($doc, array('.' => '', ',' => ''));

    $terms = explode(' ', $cleaned);

    foreach($terms as $term){
        array_push($allWords, $term);
    }
}

print_r(array_count_values($allWords));
```

示例代码16：`tf.php` — 使用PHP进行词频计算的示例。

### 输出

在本例中，术语`badly`在记录1中出现一次，在记录4中出现一次。因此，术语`badly`的词频将被设置为二。

在处理这些记录时，如果计算单词`I`的出现次数，其值将被赋为9。这样做的问题很容易看出，因为从这个单词中几乎无法获取任何洞察。原始词频对于计算重要性而言可被视为朴素的。在表5.4中，可以看到所有词频分数大于一的单词列表。除了此表顶部的停用词外，还可以看到诸如`badly`、`never`和`happy`等有趣的术语。

### 示例10：词频——逆文档频率

原始词频的一个改进是词频——逆文档频率（TF-IDF）。这种术语加权方案基于以下假设：在所有文档中频繁出现的术语应获得较低的分数，而独特的、不常出现的术语应获得较高的分数。这种加权方案可被视为对上一节传统词频计算中停用词问题的直接解决方案。表5.5描述了用于分析的两条示例记录。

**表5.5：用于词频——逆文档频率的示例记录**

| ID | 反馈 |
|---|---|
| 1 | 我对邮寄收到的产品非常满意。但是，包裹的包装处理得很糟糕。 |
| 2 | 我对我收到的产品非常满意。将来我会再次光顾。 |

术语`mail`的TF-IDF分数通过首先计算词频（tf）然后计算逆文档频率（idf）来计算。`mail`在文档1的19个术语中出现一次。方程的第一部分如公式5.1所示。

$$tf(mail, d1) = \frac{1}{19} = 0.05 \quad\quad (5.1)$$

在文档2中，术语`mail`的词频为0（文档中共有18个单词），如公式5.2所示。

$$tf(mail, d2) = \frac{0}{18} = 0.0$$

然后计算术语`mail`的逆文档频率，这考虑了该单词在所有文档`D`中出现的次数。在本例中，两篇文档中有一篇包含术语`mail`。结果转换为以10为底的对数，如公式5.3所示。

$$idf(mail, D) = log(\frac{2}{1}) = 0.301$$

一旦计算了词频，并且计算了逆文档频率，方程的两个组成部分就可以结合形成TF-IDF分数。对于文档1，TF-IDF通过将术语`mail`的`tf`分数乘以`idf`分数来计算，如公式5.4所示。

$$tfidf(mail, d1, d) = 0.05 \times 0.301 = 0.0158$$

然后可以计算文档2的TF-IDF，如公式5.5所示。

$$tfidf(mail, d2, d) = 0.0 \times 0.301 = 0$$

得到的TF-IDF分数对于不太常见的单词更高，提供了对所使用术语更深入的洞察。这种方法自然地从结果中移除了常见的停用词，因为它们经常出现在文档中。

### 示例代码：`tfidf.php`

示例17概述了一个PHP TF-IDF算法示例。在该示例的顶部，第2和3行添加了两个带有原始标点的简单反馈记录。在第5行，创建了一个名为`documents`的数组，用于存放TF-IDF计算过程中将考虑的所有文档。在第6和7行，使用`array_push()`函数将两个文档添加到数组中。

在第8行，第一个`foreach`语句用于遍历所有文档。在第10行，使用`echo`语句将文档打印到浏览器。添加一个换行符（`<br>`标签）以标识我们在Web浏览器中当前正在处理的文档。在第11行，使用`strtr()`函数将任何出现的句号或逗号替换为空格，并将结果放入`$cleaned`变量中。在第12行，将`$cleaned`传递给`explode()`函数，该函数接受分隔符以分割字符串。在本例中，传递一个空格，后跟对`$cleaned`变量的引用。这将在`$terms`数组中留下一组单独的术语。

在第13行，简单调用`count()`函数以了解数组的长度，即我们正在处理多少个术语。启动第二个内部`foreach`语句以遍历文档中的每个单独术语。使用`substr_count()`函数来识别该术语在文档中出现的次数。将正在考虑的术语、`$length`和`$count`打印到浏览器以辅助调试。`$tf`通过取`$count`并将其除以`$length`来计算。

在第21行，通过取包含正在分析的术语的文档数量除以总文档数的对数来计算`$idf`。将10传递给`log`函数以返回以10为底的对数答案。最后，在第23行，通过取`$tf`值并将其乘以`$idf`值来生成最终的TF-IDF分数。在第24行，使用简单的`echo`将分数打印到浏览器。

为了辅助算法，在第27行可以看到`$countInDocs()`函数的主体。该函数接受一个单独的术语并计算包含该术语的文档数量。在该函数的末尾，在第35行添加了一个`return`语句以返回计数。

```php
<?php

$doc1 = 'I was very happy with the product that I got in the
mail. However, the package was handled badly.';

$doc2 = 'I am very happy with the product that I got. I will come back again in the future.';

$documents = array();

array_push($documents, $doc1);
array_push($documents, $doc2);

foreach($documents as $doc){
    echo '-------------document-------------<br>';

    $cleaned = strtr($doc, array('.' => ' ', ',' => ' '));

    $terms = explode(' ', $cleaned);

    $len = count($terms);

    foreach($terms as $term){
        $count = substr_count($doc, $term);
        echo ' term: ' . $term;
        echo ' count: ' . $count;
        echo ' length: ' . $len;

        $tf = $count / $len;
        echo ' - TF: ' . $tf;

        $idf = log((count($documents) / countInDocs($term)), 10);
        echo ' IDF: ' . $idf;

        $score = $tf * $idf;
        echo ' - TF-IDF: ' . $score . '<br>';
    }
}

function countInDocs($term){
    global $documents;

    $count = 0;

    foreach($documents as $doc){
        if(substr_count($doc, $term) > 0){
            $count = $count + 1;
        }
    }

    return $count;
}
```

示例代码17：`tfidf.php` —— PHP TF-IDF 算法示例。

### 输出

图5.14展示了TF-IDF算法分析第一个文档时的输出结果。为了调试，所有计算中都添加了`echo`语句。在此输出中，我们可以看到两个文档中都存在的常见词获得了较低的TF-IDF分数。独特词汇则具有更高的TF-IDF分数。

## 5.10 情感分析

在处理文本时，还有一个额外的机会可以收集文本的整体`情感`。文本的情感是将一条记录分类为`正面`、`负面`或`中性`情感类别之一。传统的统计指标如1-10分范围可以让我们轻松判断用户对服务是否满意。然而，处理文本则稍微困难一些，因为句子中的词汇如果使用了特定关键词，很容易被认为是正面的。但这些词可能与负面回应相关联。

### 示例：情感分析

同义词是指与其他词汇含义相同的词。例如`happy`这个词，其同义词包括`cheerful`、`content`、`delighted`、`elated`和`joyful`。如果一条反馈记录中包含`delighted`这个词，我们希望将这条记录标记为具有正面情感。与其手动进行同义词检测，不如使用情感分析工具。

本示例包含一个文件和一个库：

1. `sentiment.php` —— 本页面展示了情感分析工具的使用示例。
2. `PHPinsight` —— 该库为我们提供了运行情感分析过程的能力。

### 示例代码：`sentiment.php`

要在PHP中执行情感分析，我们将使用`PHPInsight`包。该包可从<https://packagist.org/packages/jwhennessey/phpinsight>获取。我们将使用`composer`来安装，而不是手动下载文件再尝试集成到项目中。

## 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

从项目根目录的命令提示符中，我们将执行以下命令：

```bash
composer require jwhennessey/phpinsight
```

示例代码18：PHPInsight的`composer require`示例。

在示例代码19中，第2行使用了一个`pre`标签来格式化生成的输出。第3行添加了一个数组，其中包含情感分析过程将对其运行的句子。可以向此数组中添加额外的句子以进行分析。第8行添加了对`vendor`文件夹的引用，该文件夹包含PHPInsight。`autoload.php`用于从库中拉取情感分析过程所需的功能。第10行使用了一个简单的`foreach`语句来遍历数组中的每个单独字符串。第12行使用`score()`函数来获取情感分数。第13行使用`categorise()`函数来输出主导结果，例如，每个句子的`positive`、`negative`或`neutral`。

```php
1 <?php

2 echo "<pre>";

3 $strings = array(
4     1 => 'I am very happy with the staff',
5     2 => 'I did not like the staff they are unhelpful',
6     3 => 'The food was bad',
7 );

8 require_once('vendor/autoload.php');

9 $sentiment = new \PHPInsight\Sentiment();

10 foreach ($strings as $string) {
11     // calculations:
12     $scores = $sentiment->score($string);
13     $class = $sentiment->categorise($string);

14     // output:
15     echo "String: $string\n";
16     echo "Dominant: $class, scores: ";
17     print_r($scores);
18     echo "\n";
19 }
```

示例代码19：`sentiment.php` —— 使用PHPInsight库收集文本的情感。

```text
String: I am very happy with the staff

Dominant: pos, scores: Array

(
    [pos] => 0.5
    [neg] => 0.25
    [neu] => 0.25
)

String: I did not like the staff they are unhelpful

Dominant: neg, scores: Array

(
    [neg] => 0.5
    [pos] => 0.25
    [neu] => 0.25
)

String: The food was bad

Dominant: neg, scores: Array

(
    [neg] => 0.5
    [pos] => 0.25
    [neu] => 0.25
)
```

图5.15：情感分析过程的结果。

### 输出

图5.15展示了情感分析过程的输出示例。显示了三个不同的分数范围，介于0.0到1.0之间。这些显示了每个句子的正面、负面和中性分数。还可以看到主导分数，它表明了所有三个类别中的最高值。

## 5.11 小结

本章描述了处理文本时可能遇到的问题。与数值不同，文本需要额外的处理来去除无关词汇，并重新聚焦于相关词汇。本章描述了文本处理的实际组成部分，包括停用词去除、红旗词识别、n-gram生成、词干提取和同义词检测。

由于文本可以有任何长度，保持对相关词汇的关注可能很困难。为了帮助这一过程，本章讨论了诸如词频（TF）和词频-逆文档频率（TF-IDF）等指标。为了进一步分析文本，本章还描述了情感分析，可以识别文本的正面、负面和中性分数。

第6章概述了可用于创建文本动态交互式可视化的库。

# 文本可视化

## 6.1 引言

处理少量文本时，识别数据集中的模式和感兴趣记录可能很容易。然而，数据集越大，分析过程就越困难。本章描述了各种可以轻松纳入项目以增强数据探索过程的文本可视化方法。对于这些可视化，将使用基于JavaScript的库，如D3.js<sup>1</sup>、Charts.js<sup>2</sup>和HighCharts<sup>3</sup>。

## 6.2 词云

### 示例1：词云

最简捷但最具洞察力的可视化之一便是词云。它使用户能够快速查看大段文本中的关键词汇。句子被分词为单独的词汇，其中词频用于决定最终可视化中单个单词的大小。在本示例中，我们将使用可从[https://github.com/timdream/wordcloud2.js](https://github.com/timdream/wordcloud2.js)获取的`wordcloud2.js`插件。尽管文档中概述的步骤描述了使用node的npm安装库的过程，但我们将查看手动安装和设置过程，因为所需的设置非常少。

此示例需要两个文件：

1. `wordcloud.html` —— 包含运行示例的主要HTML和JavaScript代码。
2. `wordcloud2.js` —— 生成可视化效果所需的核心JavaScript库。

### 示例代码：`wordcloud.html`

此过程的第一步是下载`wordcloud2.js`文件，该文件可在<https://github.com/timdream/wordcloud2.js>找到。此单个文件夹包含了创建词云所需的所有工具。下载后，我们将创建一个新的HTML文件用于容纳词云。在示例代码1中，第1行首先添加了对JavaScript文件的引用，接着在第3行有一个单独的`canvas` HTML标签，用于容纳生成的词云。此标签被赋予了一个唯一的`ID`，将在下一步中使用。

第6行创建了一个简单的JavaScript数组，该数组接收要在词云中显示的术语列表以及每个术语在词云中应显示的大小。在此示例中，未移除停用词。第8行创建了一个`WordCloud`实例。选择了之前创建的`canvas`元素的引用，并将术语列表传递给词云。

```html
<script src="wordcloud2.js">
</script>
<canvas id="my_canvas">
</canvas>
<script>
var list = [['this', 40], ['is', 20], ['my', 60], ['sample', 20],
['chart', 60]];
WordCloud(document.getElementById('my_canvas'), { list: list });
</script>
```

示例代码1：`wordcloud.html` — 用于生成自定义词云的示例代码。

添加到词云中的每个术语都以不同的颜色表示。术语的大小由数组中设置的变量决定。尽管这提供了一个可工作的词云示例，但它并未动态接收文本字符串，也没有对文本执行任何计算来确定每个术语的出现次数。

![](img/ed4cb7e1be98f0adec0546edd14f6223_215_0.png)

图6.1：未移除停用词的示例词云。

### 示例2：动态词云



此示例词云建立在前一个示例的基础上。术语和大小不再是硬编码的，而是根据输入字符串动态生成。此示例需要两个文件：

1. `wordcloud2.html` —— 包含运行示例的主要 HTML 和 JavaScript 代码。
2. `wordcloud2.js` —— 应用程序所需的核心 JavaScript 库。

### 示例代码：wordcloud2.html

示例代码 2 从第 1 行开始引用了驱动此可视化的 `wordcloud2.js` 文件。第 3 行添加了一个 `canvas` 标签，它将作为可视化的位置。此处需要保留的重要元素是设置为 `my_canvas` 的 `ID`。为 `canvas` 设置了 `高度` 和 `宽度`。

第 6 行添加了一个名为 `text_string` 的变量，它包含将用于可视化呈现的数据。第 7 行添加了第二个名为 `common` 的字符串，用于容纳一组常见术语（例如，用逗号分隔的停用词）。这将作为一个过滤器，在渲染之前应用于可视化。由于文本可能以多种不同格式出现，并使用不同的标点符号分隔术语，因此在第 8 行的 `split()` 函数中使用了正则表达式模式应用于 `text_string`。在这种情况下，如果遇到空格、句点或逗号，则会在此标记处进行分割。

第 9 行和第 10 行创建了两个数组。第一个用于存储术语，第二个用于存储术语的计数。下一个过程是统计 `split()` 函数运行后生成的 `tokens` 数组中每个术语的出现次数。

第 11 行使用 `for` 循环遍历 `tokens` 数组中的每个元素，范围从 0 到 `tokens` 数组的长度。当此循环运行时，将从 `tokens` 数组中取出一个单独的标记，并强制转换为小写以减少重复。对每个术语调用 `trim()` 函数以去除空格。

在 `for` 循环体中，第 14 行对于每个单独的术语，使用 `indexOf()` 函数检查 `words` 数组中是否存在当前分析的术语。如果该术语确实存在，则在第 16 行将该术语推入 `words` 数组。第 17 行将值 1 推入 `wordsCount` 数组。

如果该术语不存在于数组中，则运行第 19 行的 `else` 语句。为了找到该词的存储位置，使用了该单独术语的 `indexOf()` 函数，它将返回该术语在数组中的位置，并存储在 `index` 变量中。这直接传入第 21 行的 `wordsCount` 数组以检索当前值。第 22 行将当前值加一，并设置到 `wordsCount` 数组的 `index` 位置。

第 25–31 行，使用一个简单的 `for` 循环遍历这些术语及其关联的值，并将它们打印到浏览器控制台以辅助调试。第 33 行创建了一个名为 `list` 的新数组，该数组将传递给可视化。为了填充此数组，一个 `for` 循环遍历 `words` 数组中收集的每个单独术语。在每次迭代中，第 35 行收集位置 `i` 处的 `words` 值，第 36 行收集位置 `i` 处的 `wordsCount` 值。两个值都放入局部变量中。

第 38 行使用 `\S` 模式指定，对于任何非空格字符，该单独术语将被推送到 `list` 数组上。同时还执行了一项检查，以确保该术语不出现在 `common` 字符串中，这表示它是一个停用词。第 39 行，该术语及其值（例如，术语在可视化中的大小）是该术语的计数乘以 20。

最后，第 42 行选择了 `ID` 设置为 `my_canvas` 的 `canvas`，并将 `list` 数组传递给它进行渲染。

## 文本可视化 ■ 193

```javascript
1 <script src="wordcloud2.js">
2 </script>
3 <canvas id="my_canvas" style="width:400px; height:300px">
4 </canvas>
5 <script>
6 var text_string = "I was very happy with the product that I got
    in the mail. However, the package was handled badly. I am
    very happy with the product that I got. I will come back
    again in the future. There was a number of issues with the
    customer service of this company. I will take my business
    somewhere else. It was a bad experience. I will never
    return. I was treated badly by the man on the front desk.
    This is a great company, I will never go elsewhere.";
7 var common = "i, you, me, is, was, of, a, with, that, in";
8 var tokens = text_string.split(/[ ,]+/);
9 var words = new Array();
10 var wordsCount = new Array()
11 for (var i = 0; i < tokens.length; i++) {
12   var term = tokens[i].toLowerCase().trim();
13   console.log(term);
14   if(words.indexOf(term) == -1){
15     console.log("does not exist");
16     words.push(term);
17     wordsCount.push(1);
18  /*** */
  ***//
```

```javascript
list.push([term,count*20]);
    }
  }
}
WordCloud(document.getElementById('my_canvas'), { list: list }
  );
</script>
```

示例代码 2：`wordcloud2.html` — 具有动态数据源的示例词云。

### 输出

图 6.2 显示了基于术语频率动态创建的词云的输出。

![](img/ed4cb7e1be98f0adec0546edd14f6223_218_0.png)

图 6.2：使用术语频率动态生成词云的输出。

尽管此可视化可以一目了然地提供对数据的深刻见解，但数据集越大，可视化过程就越困难。应在可视化过程开始之前考虑移除停用词，因为它们很容易占据内容的大部分。第二个需要考虑的是使用一个度量标准为感兴趣的各个术语分配权重。

## 6.3 可折叠树形布局

### 示例 3：树形布局

在处理基于文本的反馈时，经常会出现多条不同的反馈记录包含相似句子但结尾不同的情况。以下反馈记录就是一个例子：

- The food was good but I did not like the service.
- I did not like how the chairs were dirty.
- Why was there no chicken today? I did not like how the table was not cleaned.
- The food was great but I did not like the attitude of the server.

每个句子都包含相似的词组 `"did not like"`。虽然这是一个简短示例，但如果我们对包含这三个词的大量记录集合进行排序，就可以更深入地了解这些词组的上下文。可折叠树形布局允许我们在页面上水平创建基于树的结构。在树的根部，我们可以放置一段通用文本，每个分支可以包含 N 个不同的子节点，而这些子节点又可以拥有 N 个子节点。使用可折叠树形布局的优点在于，我们可以轻松隐藏树上的不同分支，从而专注于感兴趣的区域。

本示例包含三个文件：

1. `create.sql` — 用于创建所需的 `feedback_tree` 表的 SQL。
2. `tree.html` — 核心可视化示例。
3. `generateJSON.php` — 一个简单的 PHP 脚本，用于从数据库表中检索记录并将其转换为 JSON 格式。
4. `D3.js` — 用作渲染图表的主要库。
5. `jQuery` — 用于执行 JavaScript GET 请求。

### 示例代码：create.sql

对于本示例，如示例代码 3 所示，使用了一个简单的数据库表，其中包含一个唯一 `ID` 列、一个记录创建时自动插入的时间戳列，以及一个 `comment` 列，用于存储基于文本的反馈。

```sql
CREATE TABLE IF NOT EXISTS `feedback_tree` (
    `id` int NOT NULL AUTO_INCREMENT,
    `mytime` timestamp NULL DEFAULT CURRENT_TIMESTAMP,
    `comments` text,
    PRIMARY KEY (`id`)
);
CSI_SEVERITY.ERROR
```

**示例代码 3：** `Feedback_tree` 数据库表。

可折叠树形可视化由单个 JSON 文档构建而成。每个单独的节点通过 `name` 属性定义，后跟要显示的文本。在以下示例的 JSON 中，树的根节点是 `did not like`。该节点有四个子节点。

```json
{
  "name": "did not like",
  "children": [
    {
      "name": "the service"
    },
    {
      "name": "how the chairs were dirty"
    },
    {
      "name": "how the table was not cleaned"
    },
    {
      "name": "the attitude of the server"
    }
  ]
}
```

JSON 文档需要完全有效才能被渲染。这在开发过程中可能是一个困难的过程。然而，JSON 不需要像上面的示例那样被分隔开。为了帮助在开发过程中编辑 JSON，在线 JSON 格式化工具可以根据需要结构化或压缩 JSON。一个例子可以在 <https://jsonformatter.org/json-editor> 找到。

### 示例代码：tree.html

在示例代码 4 中，第 4–18 行引用了可视化所使用的 CSS 样式。第 21 行引用了 `D3.js` 的包含。第 22 行包含了 `jQuery`。`jQuery` 允许我们动态调用将生成可视化 JSON 内容的 PHP 页面。为了帮助我们识别代码加载过程中的进度，第 28 行添加了一个简单的 `console.log()`，说明我们即将调用服务器端来生成 JSON 内容。

在第 29 行，发起了一个 `jQuery` `GET` 请求，负责调用 `generateJSON.php` 页面。此次调用的结果将可在 `data` 变量中使用。然而，返回给我们的内容虽然有效的 JSON，但并未以 JSON 格式存储。在第 31 行，为了将字符串转换为 JSON 格式，我们可以使用 `JSON.parse()` 函数，该函数接收一个包含字符串的变量并将其转换为对象。这些 JSON 对象存储在 `treeData` 变量中，在第 32 行传递给 `generateTree()` 函数，该函数负责渲染树。为简洁起见，此函数的代码被省略，但可以在本书附带的在线示例中找到。

```html
<!DOCTYPE html>
<meta charset="UTF-8">
<style>
.node circle {
  fill: #fff;
  stroke: steelblue;
  stroke-width: 3px;
}

.node text {
  font: 12px sans-serif;
}

.link {
  fill: none;
  stroke: #ccc;
  stroke-width: 2px;
}
</style>

<!-- load the d3.js library -->
<script src="https://d3js.org/d3.v4.min.js"></script>

<script
    src="https://code.jquery.com/jquery-3.5.1.js"
    integrity="sha256-WpOOhJOqMqqyKL9FccASB900KwACQJpFTUBLTYOVvVU="
    crossorigin="anonymous"></script>

<body>
<script>
console.log("Calling the generateJSON.php page");
$.get( "generateJSON.php", function( data ) {
    console.log(data);
    treeData = JSON.parse(data);
    generateTree(treeData);
});
</script>
</body>
```

**示例代码 4：** `tree.html` — 检索要用 `D3` 绘制图表的数据。

### 示例代码：generateJSON.php

`generateJSON.php` 页面负责连接 MySQL 数据库，收集与执行的查询相关的记录，然后将其格式化为 JSON 结构。从数据库收集记录过程的核心是宽松匹配的 SQL 查询。在本示例中，使用了 `LIKE` 语句，并在感兴趣的文本前后加上 `%`。这表明相关词组可能出现在反馈记录的开头、中间或结尾。然而，需要进行额外的处理来移除记录开头的文本，因为它不是必需的。

在示例代码 5 中，第 7 行添加了一个名为 `rawtext` 的变量。该变量包含被视为所有我们感兴趣文本的词干的文本。第 8 行建立了与数据库的连接。第 10 行创建了一个名为 `params` 的新数组，它接收单个 `rawtext` 变量，并在变量开头和末尾加上百分号。第 11 行创建了 SQL 查询。

第 15 行，JSON 内容的开始部分首先在名为 `header` 的变量中创建。创建了一个包含要附加到内容末尾的 JSON 的 `footer` 变量。第 22 行添加了一个名为 `body` 的变量，将用作生成 JSON 的主要容器。

第 23 行，使用简单的 `foreach` 来遍历数据库结果。对于每个单独的结果，数据首先在第 24 行放入 `record` 变量中。第 25 行，通过使用 `strpos()` 函数来找到感兴趣文本的起始点，该函数接收两个参数。第一个是原始的 `record` 变量，第二个是感兴趣的文本，即 `rawtext` 变量的形式。该函数将返回一个整数，指示从何处开始提取过程。

第 27 行，`body` 变量被构建起来。这以 JSON 内容开始，并输入一个子字符串，该子字符串通过调用 `substr()` 函数并传递完整的 `record` 变量，后跟 `start` 位置加上 `rawtext` 变量的长度来获得。这将剥离感兴趣词组前面的任何附加文本。最后在第 32 行，先打印 `header`，接着是第 33 行的 `body`，最后是第 34 行的 `footer` JSON 内容。这三个组件共同构成一个有效的 JSON 文档。

```php
<?php
try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
    $rawtext = 'did not like';
    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
    
    $params = array("%$rawtext%");
    $sql = " SELECT * FROM feedback_tree WHERE comments LIKE ?";
    $sth = $DBH->prepare($sql);
    $sth->execute($params);
    $res = $sth->fetchAll();
    $header = '
        {
        "name": "did not like",
        "children": [';
    $footer = '
        ]
    }';
    $body = '';
    foreach ($res as $row){
        $record = $row[2];
        $start = strpos($record, $rawtext);
    
        $body .= '
        {"name": "'.substr($record, $start + strlen($rawtext)).'"}';
        $body .= ',';
    }
    $body = rtrim($body, ',');
    echo $header.$body.$footer;
} catch (PDOException $e) {
    echo "Error: " . $e->getMessage();
}
?>
```

## 示例代码 5：generateJSON.php ——动态构建 JSON 文档

```json
{
    "name":"' . substr($record, $start+strlen($rawtext)). '"
},';
```

### 输出

图 6.3 显示了在网页浏览器中运行的完整树形结构。左边，我们有句子主干，右边，我们有所有包含原始主干的注释。

## 6.4 关注术语节点图

### 示例 4：术语节点图



在审查来自用户的基于文本的反馈时，经常存在反馈记录之间的连接，这些连接在查看单独的记录时可能无法察觉。这种联系的一个例子可以在以下五个不同的记录中看到，这些记录可能由不同的用户留下：

- 这里的员工很糟糕，我真的很不高兴。
- 员工一直很棒，但我对游泳池真的不高兴。
- 我晚了五分钟，他们说我不许享用早餐。
- 早餐很棒。
- 早餐时间需要更多的咖啡。没有它我怎么能工作呢？

虽然这是一个非常简单的例子，我们可以看到有两次对`员工`的引用，以及三次对`早餐`的不同引用。在本节中，我们将概述识别受我们关注的术语的过程，这些术语是我们可能在记录中看到过的（例如`早餐`和`员工`），并将这些术语用作连接不同反馈记录的节点和基于边的图。

本示例由六个文件组成：

1. `create.sql`——创建用于`nodetree`表的 SQL。
2. `graph.php`——这允许用户输入感兴趣的术语和日期。
3. `getRecords.php`——该文件从数据库检索记录。
4. `Viz.js`——此库用于向图添加节点。
5. `jQueryUI`——此库添加了交互式日期选择器的功能。
6. `jQuery`——这用于选择页面上的元素。

### 示例代码：`create.sql`

To begin, we will start with a basic table structure that will hold the feedback records, as shown in Sample Code 6. This table titled `nodetree` contains three columns, a unique `ID` column, a timestamp column, and a feedback column that will contain the text that the user has entered.

```sql
CREATE TABLE `nodetree` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `mytime` DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `feedback` TEXT,
    PRIMARY KEY (`id`)
);
```

样本代码 6：节点树数据库表。

对于此示例，我们将使用可以从以下 GitHub 页面下载的 Vis.js 库：<https://github.com/visjs/vis-network>。我们将对要绘图的记录使用两种不同的过滤标准。第一种是存储在`YYYY-MM-DD`格式的日期，以及在特定日期上搜索的一组用逗号分隔的术语。我们搜索的两个术语是`早餐`和`员工`。

### 示例代码：`getRecords.php`

此过程的第一步是创建一个允许我们选择数据库中的记录以供可视化的 PHP 页面。在样本代码 7 中，`date`和`terms`变量在第 2 和第 3 行接收。第 9 行建立了与数据库的连接。第 10 行使用了`explode()`函数将术语根据逗号分开。第 11 行创建了一个名为`whereClause`的变量，用作 SQL`WHERE`子句的占位符。对于每个术语，在第 13 行添加了额外的`WHERE`子句以搜索与用户输入的术语相似的术语。在语句末尾添加了一个`OR`运算符，允许附加其他`WHERE`子句。当`foreach`循环结束时，在第 15 行使用`substr()`函数从`whereClause`变量中删除最后一个`OR`语句，因为 SQL 不能以有效的 SQL 语句结尾作为`OR`。

第 16 行，`date`被输入到一个新数组中，存储在标题为`params`的局部变量中。SQL 语句的主体添加到第 17 行，搜索`notetree`表中时间戳大于提供日期的记录。`WHERE`子句附加到此 SQL 查询。第 19 行，查询最终执行。第 21 行，对于返回的每个记录，收集该行中位置 2 的列并将其放入`record`变量中。这是输出到页面的反馈文本。

```php
<?php
$date = $_GET['date'];
$terms = $_GET['terms'];
try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
    $words = explode(',',$terms);
    $whereClause = '';
    foreach( $words as $word) {
        $whereClause .= ' feedback LIKE "%' . $word . '%" OR';
    }
    $whereClause = substr($whereClause, 0, -2);
    $params = array($date);
    $sql = "SELECT * FROM nodetree WHERE timestamp > ? AND " . $whereClause;
    $sth = $DBH->prepare($sql);
    $sth->execute($params);
    $res = $sth->fetchAll();
    foreach ($res as $row){
        $record = $row[2];
        echo $record . '<br>';
    }
} catch(PDOException $e) {echo $e;}
```

样本代码 7：`getRecords.php`——使用`WHERE`子句获取记录。

### 示例代码：`graph.php`

创建了一个第二个页面，标题为`graph.php`。这是主界面，允许用户选择日期并输入感兴趣的术语。

在样本代码 8 中，在此文件顶部引用了 jQueryUI CSS（用于辅助弹出日期选择器）。第 3 行引用了 jQuery。第 4 行包含 jQueryUI 所需的 JavaScript。第 6 和第 7 行包含了`vis-network.min.js`文件和`vis-network-min.css`文件。这两个文件可以在 Vis.js 源代码的根目录下的`dist`文件夹中找到。第 10–15 行使用 CSS 定义标题为`mynetwork`的`div`标签的高度、宽度、边框和背景。

文档页面的主体包含两个输入框。第一个位于第 22 行，`ID`设置为`datepicker`，允许用户从 jQueryUI 日期选择器工具中选择感兴趣的日期。第二个输入框在第 24 行添加，`ID`设置为`terms`，允许用户输入感兴趣的术语。用户可以输入单个术语或多个用逗号分隔的术语。第 25 行添加了按钮，`ID`设置为`generate`，点击时生成图。第 26 行添加了一个带有标题为`mynetwork`的`div`标签，这是可视化的主要占位符。

```html
<link rel="stylesheet"
    href="http://code.jquery.com/ui/1.12.1/themes/base/
    jquery-ui.css">
<script src="https://code.jquery.com/jquery-1.12.4.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js">
</script>
<script type="text/javascript"
    src="vis-network.min.js"></script>
<link href="vis-network.min.css" rel="stylesheet"
    type="text/css" />
<head>
<style type="text/css">
#mynetwork {
    width: 1000px;
    height: 1000px;
    border: 1px solid lightgray;
    background:#d1d1d1;
}
p {
max-width:600px;
}
</style>
</head>
<body>
    <p>Date of interest: <input type="text" id="datepicker"
    value="2019-08-05"></p>
    Please enter terms of interest
    <input type="text" value="breakfast" size="30" id="terms">
    <button id="generate">Generate graph</button>
    <div id="mynetwork"></div>
</body>
```

样本代码 8：`graph.php`——提供感兴趣的日期和术语——第 1 部分。

HTML 组件创建之后，下一步是实施将用于生成图的 JavaScript。

在样本代码 9 中，在`script`标签内，第 29 和第 30 行创建了两个数据集。第一个用于存储图的节点，第二个用于存储图的边。边是将在每个不同节点之间创建的连接。第 31 行创建了一个名为`nodeId`的变量，用作存储每个节点唯一 ID 的参考点。每当向图添加新节点时，此变量将递增。

为了开始图的生成过程，在第 32 行生成了一个点击（`click()`）处理器添加到生成按钮上。图的生成将添加到此点击处理器内部。第 33 和第 34 行使用 jQuery 选择器选择术语和日期输入框。`val()`函数将从输入字段中提取值。第 35 行，向之前创建的`getRecords.php`页面发起 GET 请求。在第 36 和第 37 行传递两个变量给此页面，即术语和日期。从临时用于存储值的变量中获取值`t`和`d`。

此 GET 请求在第 39 行有一个`done()`函数，返回数据变量。这将返回数据库中选中的行。要在执行任何处理之前查看这些记录，可以添加`console.log(data)`以帮助调试。

使用此数据变量，在第 40 行，根据`getRecords.php`页面每行末尾附加的`br`标签将每个单独记录分开。此`br`标签用作标识将下一行与上一行区分开的标记。在调用`split()`函数之后，`feedbackRecords`变量将包含一个数组，每一行对应数组中的一个独立位置。

为了确定用户输入的术语数量，第 42 行基于每个术语之间的逗号对`t`变量进行拆分。这些术语被放入`termsSplit`数组变量中。第 44 行添加了一个`for`循环，以遍历用户输入的每个术语。对于每个单独的术语，第 45 行调用`trim()`函数以删除术语周围的所有额外空白。然后在第 47 行调用`generateGraphForTerm()`函数。该函数接受一个术语作为参数。这是为每个术语生成图的核心部分。

在第 51 行可以看到`generateGraphForTerm()`函数。在第 52 行，创建了一个名为`connections`的新数组，它将用于存储节点之间的边。创建了一个包含当前`nodeId`的父节点。这将作为所有生成节点的参考点。对于术语`staff`，任何包含该术语的记录都将链接回这个父节点。

为了创建父节点，在第 54 行调用`nodes`数据集并调用`add()`函数。它接收节点的唯一定义 ID 和标签（包含节点将显示的文本）。在这种情况下，对于父节点，第 56 行的文本将来自`singleT`变量，即用户输入的一个单独术语。然后添加字体大小和颜色。此过程中的一个关键要素是在创建新节点时递增`nodeId`变量，如第 63 行所示。这将允许图中的每个节点拥有唯一的 ID。

在为每个单独术语生成根节点之后，需要为每个已返回的记录创建节点。为此，第 65 行添加了一个`for`循环，以遍历包含单独反馈记录的`feedbackRecords`数组。为了辅助调试过程，第 66 行添加了一个`console.log()`函数，用于打印出我们当前正在处理的`nodeId`。

创建了两个变量来监控单独记录的处理。第一个变量是第 67 行的`termCount`记录，用于存储用户输入的术语中出现在我们正在处理的记录中的数量。

在第 69 行，在处理每个记录时，使用内部`for`循环来遍历用户输入的每个术语。这些术语存储在`termsSplit`数组中。`indexOf()`函数在第 71 行的`if`语句中被调用，并传递用户输入的一个术语。如果反馈记录包含该术语，则该函数将返回大于 -1 的数字。当我们找到该术语时，第 72 行递增`termCount`。

对于添加到图中的每个单独记录，如果在记录中找到用户输入的一个术语，它被视为普通记录。在这种情况下，默认字体颜色为`黑色`。如果找到所有术语，则记录的颜色变为`红色`。在内部`for`循环运行之后，在第 77 行进行检查，看`termCount`是否小于用户输入的术语数量。如果是这种情况，则通过将第 78 行的`normalRecord`布尔变量设置为`true`将记录识别为普通记录。

```javascript
<script>
var nodes = new vis.DataSet();
var edges = new vis.DataSet();
var nodeId = 1; // unique Node ID for each.
$('#generate').click(function() {
	var t = $('#terms').val();
	var d = $('#datepicker').val();
	$.get("getRecords.php", {
		terms: t,
		date: d
	})
	.done(function(data) {
	var feedbackRecords = data.split('<br>');
	// count number of terms entered by the user
	var termsSplit = t.split(',');
	// for each individual term entered by the user
	for (var i = 0; i < termsSplit.length; i++) {
		var singleTerm = termsSplit[i].trim();
		console.log("running graph for " + singleTerm);
		generateGraphForTerm(singleTerm);
	}
}
// main function for generating a graph for
// a specific term
function generateGraphForTerm(singleT) {
	var connections = new Array();
	var parentNode = nodeId;
	nodes.add({
		id: nodeId,
		label: singleT,
		font: {
			size: 16,
			color: 'black',
			face: 'arial'
		}
	});
	nodeId++;
	// for each row in the data set we are working with.
	for (var i = 0; i < feedbackRecords.length; i++) {
		console.log("NodeID " + nodeId);
		var termCount = 0;
		var normalRecord = false;
		for (var y = 0; y < termsSplit.length; y++) {
			console.log("looking in" + feedbackRecords[i]);
			if (feedbackRecords[i].indexOf(termsSplit[y]) > -1) {
				termCount++;
				console.log("found occurrence for " + termsSplit[y]);
			}
		}
		console.log("term count " + termCount);
		if (termCount < termsSplit.length) {
			normalRecord = true;
		}
	}
```

示例代码 9：`graph.php`——识别感兴趣的术语——第二部分。

在示例代码 10 中，第 80 行，如果`normalRecord`设置为`true`，并且我们正在处理的记录确实包含感兴趣的术语，则将新节点添加到`nodes`数据集中。类似于如何为父记录添加记录，第 82 行调用`add()`函数。添加了唯一的`nodeId`和`label`。为了可视化第 84 行上的完整记录，节点的`label`设置为`feedbackRecords[i]`，其中`i`是我们正在遍历的数组的当前位置。由于这是一个普通记录，字体颜色在第 87 行设置为`黑色`。

在第 92 行，此过程的最后一步是将刚刚创建的节点推送到`connections`数组中，以便稍后连接边。在第 95 行，在新节点创建后递增`nodeId`同样至关重要，以防止图中出现重复的节点 ID。

在第 97 行，如果用户输入的所有术语都出现在反馈记录中，则使用相同的过程将节点添加到图中。所做的唯一修改是使用`else`而不是添加`if`语句，因为这只有在`normalRecord`变量等于`false`时才会运行。在这种情况下，字体颜色在第 102 行更改为`红色`，以与其他记录区分开来。



在为每个单独术语创建父节点以及子节点（例如，单独的反馈记录节点）之后，必须执行创建边的过程。边是出现在节点之间的连接。第 112 行使用一个`for循环`来遍历所有已存储的连接。这个`connections`数组包含了在前一步骤中添加的所有节点的 ID 列表。

在第 113 行，对于每个单独的连接，节点计数器变量用于从`connections`数组中选择节点`ID`。这将从 0 开始并递增到`connections`数组的长度。对于`connection`数组中存储的每个节点`ID`，它们首先放入一个名为`leftNode`的临时变量中。第 115 行，使用`edges`数据集并在数据集上调用`add()`函数，以在当前拥有的`leftNode`和之前创建的`parentNode`之间建立连接。这个父节点将仅包含一个术语，例如`staff`，而`leftNode`将包含包含术语`staff`的完整文本反馈记录。

```javascript
80 if (normalRecord == true) {
81     if (feedbackRecords[i].indexOf(singleT) > -1) {
82         nodes.add({
83             id: nodeId,
84             label: feedbackRecords[i],
85             font: {
86                 size: 11,
87                 color: 'black',
88                 face: 'arial'
89             }
90         });
91         console.log(nodeId + feedbackRecords[i]);
92         connections.push(nodeId);
93     }
94
95     nodeId++;
96 } else {
97     nodes.add({
98         id: nodeId,
99         label: feedbackRecords[i],
100        font: {
101            size: 11,
102            color: 'red',
```

## 示例代码 10：graph.php — 创建边 — 第 3 部分

在示例代码 11 中，该过程的最后一步是在网页上初始化图表。这通过在第 122 行使用`getElementById()`选择器来选择先前创建的`ID`为`mynetwork`的`div`标签。此引用被放入一个名为`container`的变量中。`data`被创建，它包含对第 124 和 125 行已构建的`nodes`和`edges`数据集的引用。

在此之后，指定图表的选项。在第 129 和 130 行，指定了大小为 10 的点形状。三个引用`container`、`data`和`options`在第 133 行传递给`vis.Network()`构造函数。这将基于我们提供的数据创建一个图表。最初用于生成图表过程的点击处理函数被关闭。

要初始化 jQueryUI 日期选择器，在第 137 行使用 jQuery 选择器来选择`datepicker`输入框。调用`datepicker()`函数。由于数据库中的日期以`YYYY-MM-DD`格式存储，可以在日期选择器上设置一个额外选项以使用此格式，如第 138 行所示。如果不执行此步骤，日期和月份将会颠倒。

```javascript
    // create a network
    var container = document.getElementById('mynetwork');
    var data = {
        nodes: nodes,
        edges: edges
    };
    var options = {
        nodes: {
            shape: 'dot',
            size: 10
        }
    };
    var network = new vis.Network(container, data, options);
});
});
$(function() {
    $("#datepicker").datepicker();
    $("#datepicker").datepicker("option", "dateFormat",
        'yy-mm-dd');
});
</script>
```

## 示例代码 11：graph.php — 创建 jQueryUI 日期选择器 — 第 4 部分

### 输出

图 6.4 提供了所选日期 2019-08-05 以及关键词`breakfast`和`staff`的输出示例。在此示例中，我们可以看到用户输入的关键词成为包含该术语的所有记录的父节点。每当一条记录包含用户输入的所有术语时，记录的颜色将变为红色以作额外强调。

## 6.5 使用正负评论图表进行时间序列分析

在本节中，我们将概述创建时间序列图的过程。这些图表侧重于时间元素，允许在数天或数周内查看数据。这种数据分析方法使我们能够查看营销活动或功能实施对用户的影响。为此，我们将在一周的每一天绘制发生的正向和负向反馈。此示例包含四个组件：

1. `create.sql` — 这包含`pastime`表的创建 SQL，该表包含评论分数。
2. `time.php` — 用于从数据库检索记录，是主要的可视化页面。
3. `Chart.js` — 这是用于生成图表的主要库。
4. `moment.js` — 一个基于 JavaScript 的库，用于处理时间戳。

### 示例 5：正向和负向评论

图表生成过程分为两个部分。用于从数据库收集相关记录的 PHP 组件，以及用于创建可视化的 HTML/JavaScript 组件。在此示例中，创建了一个名为`time.php`的文件。PHP 代码将放在文件顶部，随后是 JavaScript 和 HTML。

#### 示例代码：create.sql

在开始构建图表之前，需要一个数据库表。在此示例中，我们将创建一个名为`pastime`的表。此表包含一个唯一的`ID`列，它是主键，并且在输入新记录时自动递增。`mytime`列将在保存新记录时从系统检索当前时间戳。`feedbacktext`是文本类型，允许用户输入他们的反馈。此示例中最重要的列是`score`列，我们将用于存储 1 到 10 之间的评分。由于范围较小，可以使用`TINYINT`数据类型。

```sql
CREATE TABLE `pastime` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `mytime` TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
  `feedbacktext` TEXT,
  `score` TINYINT,
  PRIMARY KEY (`id`)
);
```

#### 示例代码：time.php

在示例代码 12 中，用于生成图表记录的 PHP 组件分为四个不同的部分。第一个是第 7 行与 MySQL 数据库的连接。此数据库将用于检索正向反馈记录和负向反馈记录。在第 10 行，定义了一个名为`getNumberOfPositive()`的新函数，它接受一个日期形式的参数。在第 11 行，引用了数据库对象。在第 12 行，日期被传递到 PHP`explode()`函数中，该函数将根据日、月和年之间的空格将日期分开。每个部分将作为数组元素存储在`date`数组中。

通过引用位置 0 的`date`对象访问年份，并存储在`justYear`变量中。在第 14 行，创建了一个 SQL 查询。这使用 SQL`count()`函数对`score`列返回的记录数进行计数。在 SQL 语句末尾添加了一个`WHERE`子句，以指定年份类似于`justYear`变量中的年份。除此之外，为了将记录分类为正向，还添加了一个额外的`AND`运算符，以确保分数必须大于 5。在第 18 行，返回包含正向记录总数的记录结果。

此过程在第 20 行的`getNumberOfNegative()`函数中再次重复。唯一的修改是在第 24 行，`score`必须小于或等于 5。

为了检索要可视化的日期列表，在第 33 行添加了一个新的 SQL 查询。使用`distinct`关键字去除重复日期。在第 40 行，对于每个单独的日期，存储日期的位置 0 的行被放入`labels`变量中。通过在第 42 行调用`getNumberOfPositive()`函数来检索该日期的正向分数，后跟一个逗号以分隔结果和下一个要生成的结果。在第 45-47 行，通过调用`getNumberOfNegative()`函数对负向分数重复相同的过程。通过向 PHP`substr()`函数传递 -1，使用 PHP`substr()`函数从`labels`、`positive`和`negative`变量中移除尾部冒号。

```php
<?php
try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';
    $DBH = new PDO("mysql:host=$host;dbname=$dbname",$user,
        $pass);
} catch(PDOException $e){echo $e;}

function getNumberOfPositive($date) {
    global $DBH;
    $date = explode(' ', $date);
    $justYear = $date[0];
    $sql = "SELECT COUNT(score) as CORE FROM pastime WHERE TIMESTAMP LIKE '$justYear%' and score > 5";
    $sth = $DBH->prepare($sql);
    $date = ' '.$date[0].'';
    $justYear = $DBH->query($sql)->fetchAll();
    return $justYear;
}

function getNumberOfNegative($date) {
    global $DBH;
    $justYear = $date[0][0];
    $sql = "SELECT COUNT(score) as CORE FROM pastime WHERE TIMESTAMP LIKE '$justYear%' and score <= 5";
    $sth = $DBH->prepare($sql);
    $sth->execute();
    return $sth->fetchAll();
}

$stmt = $DBH->query('SELECT DISTINCT CAST(mytime AS DATE) as mydate FROM pastime');
$labels = '';
$positive = '';
$negative = '';

foreach ($stmt as $row) {
    $labels .= $row[0].',';
    $positive .= getNumberOfPositive($row[0]).',';
    $negative .= getNumberOfNegative($row[0]).',';
}

$labels = substr($labels, 0, -1);
$positive = substr($positive, 0, -1);
$negative = substr($negative, 0, -1);
?>
```

#### 示例代码 13：time.php — 初始页面设置 — 第 1 部分

在示例代码 14 中，存储图表所有配置的`config`对象在第 85 行添加。第 86 行指定了将生成的图表类型。在此例中，我们将生成一个折线图。第 87 行定义了图表的数据。这将包含图表的标签和数据。第 88 行的标签，在此例中，是已收集反馈的各个日期。为辅助图表生成过程，标签是使用 PHP 生成的。这些标签存储在`labels` PHP 变量中，并用逗号分隔。

将要表示的数据集由一个月中的各个日期组成，每个日期包含正面和负面反馈记录的计数。为便于实现，第 92 行的`datasets`变量包含标签，该标签将用于显示第一个数据集，在此例中，即正面反馈。该数据的背景颜色在第 94 行设置为`red`。此红色取自之前定义的`chartColors`。图表的数据在第 98 行定义。这些值将在第 99 行使用 PHP 动态添加。

添加了第二个数据集。这是通过首先在第 102 行指定我们希望显示的标签，然后指定我们希望用于表示该数据集的颜色来完成的。第 103 行设置为`blue`。`fill`属性允许我们定义是否希望用颜色填充折线下的区域。为保持此图表清晰，我们将此设置为`false`。与正面反馈类似，此数据集的数据来自第 108 行 PHP 变量输出的`negative`变量。

在第 113 行，可以指定图表的附加选项。先设置标题，然后是数据图上将出现的坐标轴。第 119 行，`xAxes`被定义为`time`。`display`设置为`true`，`label`设置为值`Date`。定义了图表的`yAxes`。此过程的最后一步是生成图表。第 135 行使用`window.onload()`函数来触发此过程。当窗口加载时，使用`getElementById()`选择器选择`canvas`。调用`getContext()`函数并设置为`2d`。最后，在第 137 行，`window.myLine`被设置为一个新的`Chart`，其中`ctx`变量作为上下文传入，`config`变量包含图表的配置。

### 图 (c)

> **图 (c)：** 显示了图表生成过程的最终输出。图表中添加了两条线，分别表示正面反馈计数和负面反馈计数。
>
> 图表底部显示的日期代表时间线。
>
> **图 (a)：** 显示一周内七天正面和负面反馈的时间图表。

#### HTML 页面

```html
<!doctype html>
<html>
<head>
<title>正面和负面反馈</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.18.1/moment.min.js"></script>
<script src="https://www.Chart.js.org/dist/2.8.0/Chart.min.js"></script>
<script src="https://code.jquery.com/jquery-1.12.4.js"></script>
<style>
canvas {
-moz-user-select: none;
-webkit-user-select: none;
-ms-user-select: none;
}
</style>
</head>
<body>
<div style="width:75%;">
    <canvas id="canvas"></canvas>
</div>
</body>
</html>
<script>
window.chartColors = {
red: 'rgb(255, 99, 132)',
orange: 'rgb(255, 159, 64)',
yellow: 'rgb(255, 205, 86)',
green: 'rgb(75, 192, 192)',
blue: 'rgb(54, 162, 235)',
purple: 'rgb(153, 102, 255)',
grey: 'rgb(201, 203, 207)'
};
</script>
```

## 总结

> 本章概述了处理文本时可以进行的可视化操作。介绍了词云作为一种快速查看文本集合中最常用术语的方法。由于文本以句子和段落等结构化格式呈现，随后探索了基于树的结构，概述了如何使用单个术语的根进行连接。

任何反馈记录的一个重要因素是其留下时间。随后探讨了基于特定日期正面和负面反馈记录数量的折线图，为数值数据提供了快速统计概览。

接下来，第 7 章将详细探讨数据的时间组成部分。




# 第七章 基于时间的反馈分析

## 7.1 引言

在收集反馈数据时，通常会添加时间戳。这些时间戳可用于从数据中获取额外的洞察。特定时间范围内的反馈记录可以表明当前业务运营中存在的问题，或在特定过去时间出现的问题。如果查看记录集合时没有时间维度，这些洞察可能会丢失。

在本章中，将探讨数据的时序特性。

## 7.2 收集时间线和数据库数据类型

在向用户收集反馈时，MySQL 提供了多种不同的日期和时间型数据类型。表 7.1 概述了这些数据类型。可以根据时间/日期是在数据收集过程中以编程方式创建的，还是在将数据提交到数据库的过程中自动创建的，来进行划分。

### 示例 1：日期和时间

在 PHP 中，我们可以使用`date()`函数返回当前日期戳。可以向该函数传递不同的参数，以不同的格式返回日期。示例代码 1 概述了获取年、月、日的过程。`Y`参数返回四位数的年份，例如 2021；`m`参数返回两位数的月份，例如 08；最后`d`参数返回两位数的日期，例如 12。

¹ http://php.net/manual/en/function.date.php

**表 7.1：MySQL 日期和时间的数据库数据类型**

| 数据类型 | 描述 |
| :--- | :--- |
| `DATE` | 日期以 YYYY-MM-DD 格式存储，范围从 1000-01-01 到 9999-12-31。 |
| `TIME` | HH:MM:SS 格式，范围从 -838:59:59 到 838:59:59。可用六位精度微秒作为尾数小数。 |
| `YEAR` | 从 1901 到 2155 的年份。可以整数或字符串格式赋值。可使用 1 至 99 之间的整数，这些整数将转换为四位字符表示。 |
| `DATETIME` | 自动生成的字段，格式为 YYYY-MM-DD HH:MM:SS。 |
| `TIMESTAMP` | 自动生成的字段，范围从 1970-01-01 00:00:01 UTC 到 2038-01-19 03:14:07 UTC。MySQL 将当前时区转换为 UTC 格式进行存储，并在检索过程中转换回当前时间。 |

```php
<?php

echo "Today is " . date("Y-m-d") . "<br>";

?>
```

**示例代码 1：** 使用 PHP 检索日期。

存储时间的另一种方法是使用 Epoch 格式。这种格式是自 Unix 纪元（即 1970 年 1 月 1 日 00:00:00 GMT）以来经过的秒数。在存储这种格式时，不需要标准的日期/时间数据类型。示例代码 2 概述了以 Epoch 格式检索时间的过程。

```php
<?php

$date = new DateTime();

echo $date->getTimestamp();

?>
```

**示例代码 2：** 返回当前 Epoch 时间。

使用基于 Epoch 的格式的优点是可以轻松地对时间戳进行计算。例如，对于 Epoch 时间戳 1540470653，我们可以通过简单地将三小时转换为秒来添加三小时，如公式 7.1 所示。

$$60 \, 秒 \times 60 \, 分钟 \times 3 \, 小时 = 10800$$ (7.1)

可以对原始 Epoch 时间进行简单的加法运算，得到新的 Epoch 时间，如公式 7.2 所示。

$$1540470653 + 10800 = 1540481453$$ (7.2)

## 7.3 时间段分析和可视化

在查看反馈时，根据我们希望与数据的距离远近，有多种不同的选项可供选择。在这个示例中，我们将描述为给定时间段生成正面和负面反馈图表的过程。在这个示例中，我们将一天作为最大的查看时间量。在这一天中，我们将重点关注每个不同小时的正面和负面反馈记录数量。这种方法使我们能够更近距离地查看可能收到的正面或负面反馈，并查看反馈记录的确切时间。

### 示例 2：时间段分析

此示例包含三个文件和五个库：

1. `create.sql` — 该文件概述了`exampleexample`表的创建 SQL。
2. `timesegment.php` — 其中包含允许用户选择感兴趣的日期和时间以及时间段大小的控件。
3. `getTimeRecords.php` — 该文件从数据库中检索感兴趣的记录。
4. `Chart.js` — 用于绘制正面和负面反馈图表。
5. `Moment.js` — 该库用于在 JavaScript 中处理时间戳。
6. `jQuery` — 用于执行 JavaScript POST 请求。
7. `jQueryUI` — 提供交互式日期选择工具。
8. `timepicker.co` — 提供交互式时间选择工具。

### 示例代码：`create.sql`

示例代码 3 概述了数据库表的结构。创建新记录时，时间戳记录在`mytime`列中。反馈分数存储在`score`列中。

```sql
CREATE TABLE `timeanalysis` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `mytime` TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `score` INT,
    PRIMARY KEY (`id`)
);
```

**示例代码 3：** 创建`timeanalysis`数据库表的 SQL。

### 示例代码：`timesegment.php`

此过程的第一步是创建一个新的 PHP 页面，标题为`timesegment.php`，用于容纳用户选择的 HTML 选项和可视化的 JavaScript。对于将要使用的每个 JavaScript 库，将使用内容分发网络（CDN），以消除下载并将每个单独的库存放到项目文件夹中的需要。

在示例代码 4 中，第 5–15 行包含了 CDN 引用。其中包括用于在 JavaScript 中处理时间戳的 Moment.js。该库可从 https://momentjs.com/ 获取。Chart.js 用于主要的绘图过程。在此示例中，我们将使用带有两个轴的折线图。为了操作 HTML 文档并利用 DOM 对象选择器，将使用 jQuery。为了向用户提供交互式日历，使用了 jQueryUI 库以及 jQueryUI CSS 文件。日历小部件可从 https://jqueryui.com/datepicker/ 获取。为了选择时间窗口，使用了基于 jQuery 的时间选择器，可从 https://timepicker.co/ 获取。时间选择器还使用了一个 CSS 文件进行样式设置，该文件也一并包含。

与之前的示例类似，在第 17-21 行，`canvas`标签被操作以防止用户在 Firefox、Chrome 和 Internet Explorer 中进行选择。

在第 25 和 26 行，添加了两个输入字段。第一个用于向用户呈现日期值，第二个用于向用户显示所选的时间。默认情况下，小部件将不会出现，直到用户点击输入字段。要将这些常规`input`字段转换为小部件，需要使用额外的 JavaScript，这部分稍后在本节中展示。这里有两个重要的元素：每个字段的 ID。第一个`input`字段的 ID 为`datepicker`，第二个的 ID 为`timepicker`。

由于此可视化的主要目标是利用时间，在第 28 行添加了一个 HTML `select`字段。该字段的`ID`设置为`minutes`。初始增量为 15 分钟，直到小时标记。然后以小时为单位进行增量。小时由附加在数字后的附加`h`表示。这将在数据收集期间用于将选定的小时转换为分钟。指定时间窗口后，在第 57 行添加了一个`button`，用于触发可视化过程。该按钮的`ID`设置为`loadData`。

在第 58 行，添加了一个`div`标签，宽度为可用空间的 75%。在此`div`标签内，添加了一个`canvas`标签，这是可视化的核心。其`ID`设置为`canvas`。

```html
<!doctype html>
<html>
<head>
<title>Time Segment Analysis</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.18.1/moment.min.js"></script>
<script src="https://www.chartjs.org/dist/2.8.0/Chart.min.js"></script>
<script src="https://code.jquery.com/jquery-1.12.4.js"></script>
<link rel="stylesheet" href="//code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
```

## 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

```html
<link rel="stylesheet"
   href="https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.js"></script>
<style>
    canvas {
        -moz-user-select: none;
        -webkit-user-select: none;
        -ms-user-select: none;
    }
</style>
</head>
<body>

Date: <input type="text" id="datepicker">
Time From: <input type="text" id="timepicker">
Time Window

<select id="minutes">
    <option value="15">15 Minutes</option>
    <option value="30">30 Minutes</option>
    <option value="45">45 Minutes</option>
    <option value="1h">1 Hour</option>
    <option value="2h">2 Hours</option>
    <option value="3h">3 Hours</option>
    <option value="4h">4 Hours</option>
    <option value="5h">5 Hours</option>
    <option value="6h">6 Hours</option>
    <option value="7h">7 Hours</option>
    <option value="8h">8 Hours</option>
    <option value="9h">9 Hours</option>
    <option value="10h">10 Hours</option>
    <option value="11h">11 Hours</option>
    <option value="12h">12 Hours</option>
    <option value="13h">13 Hours</option>
    <option value="14h">14 Hours</option>
    <option value="15h">15 Hours</option>
    <option value="16h">16 Hours</option>
    <option value="17h">17 Hours</option>
    <option value="18h">18 Hours</option>
    <option value="19h">19 Hours</option>
    <option value="20h">20 Hours</option>
    <option value="21h">21 Hours</option>
    <option value="22h">22 Hours</option>
    <option value="23h">23 Hours</option>
    <option value="24h">24 Hours</option>
</select>
```

```html
<button id="loadData">Load Data</button>

<div style="width:75%;">
    <canvas id="canvas"></canvas>
</div>
```

**示例代码 4：** `timesegment.php`—第一部分。

### 输出

图 7.1 展示了 HTML 的最终输出。

![图 7.1：时间分段分析控件。](img/ed4cb7e1be98f0adec0546edd14f6223_251_0.png)

> 图 7.1：时间分段分析控件。

图 7.2 展示了在单击日期输入字段后显示的 jQueryUI 日历小部件。

![图 7.2：选择分析过程的开始时间。](img/ed4cb7e1be98f0adec0546edd14f6223_251_1.png)

> 图 7.2：选择分析过程的开始时间。

图 7.3 展示了用于选择感兴趣的时间起点的时间输入器小部件的使用示例。

日期：[ ]

时间从：上午 1:00 | 时间窗口：15 分钟 | 加载数据

![图 7.3：选择感兴趣的时间起点。](img/ed4cb7e1be98f0adec0546edd14f6223_252_0.png)

> 图 7.3：选择感兴趣的时间起点。

在样本代码 5 中，第 63 行创建了`window.chartColors`。这指定了一组颜色的 RGB 值。在此图表中，将使用红色和绿色。当页面加载时，第 72 行调用`function()`。内部，在第 73 行使用 jQuery 选择器来选择`datepicker`输入字段。我们使用的日期格式作为参数指定。在此示例中，我们将传递`yy-mm-dd`，这将提供诸如`2020-08-28`之类的日期。选择器再次用于在第 74 行选择`timepicker input`字段。时间格式传为`h:mm p`。这将提供输出如 10:00am。第 76 行的间隔指定添加时间之间的间隔。在此示例中，我们在每个当前时间之间使用 15 分钟间隔。默认时间在第 77 行指定为 1:00am。第 79 行，下拉框设置为`true`，提供下拉菜单以允许用户选择日期。第 80 行，滚动条设置为`true`，提供视觉滚动条。

在第 83 行，使用 jQuery 选择器选择`loadData`按钮，将`click()`处理程序附加到之前创建的按钮上。当按钮被点击时，会调用`generateNewGraph()`函数负责完整的图表生成过程。第 86 行，创建了这个新函数。当此函数被调用并从数据库检索正向和负向反馈并将其绘制在单独的线上时。

在此函数内，在第 87 行将 Chart.helpers.color 的引用存储在名为`color`的变量中。图表的配置在第 88 行创建并存储在`config`变量中。在此配置中，第一个参数是生成的图表类型，在本例中值设置为`line`。第 91 行的`data`变量包含`datasets`数组。

该数组包含两个不同的数据集。第一个存储在该数组的位置 0，即负反馈分数。在第 93 行使用之前定义的`chartColours`选择颜色红色。此颜色使用`rgbToString()`函数转换为 RGB 字符串。边框颜色也定义为红色。第 96 行，`fill`属性允许我们在图表中线条下方着色。由于可能存在大量反馈记录，为避免过度填充图表，将其设置为`false`。第 87 行的`data`变量是一个在首次初始化时留空的数组。这将在稍后步骤中输入。

从第 100 行开始，定义第二个数据集。该数据集存储在数组的位置 1。该数据集用于存储正向反馈。此过程与上一步相同，唯一的改动是在第 103 行将线条颜色设置为绿色。

```javascript
window.chartColors = {
    red: 'rgb(255, 99, 132)',
    orange: 'rgb(255, 159, 64)',
    yellow: 'rgb(255, 205, 86)',
    green: 'rgb(75, 192, 192)',
    blue: 'rgb(54, 162, 235)',
    purple: 'rgb(153, 102, 255)',
    grey: 'rgb(201, 203, 207)'
};

$(function() {
    $("#datepicker").datepicker({dateFormat: "yy-mm-dd"});
    $('#timepicker').timepicker({
        timeFormat: 'h:mm p',
        interval: 15,
        defaultTime: '1:00am',
        startTime: '1:00am',
        dropdown: true,
        scrollbar: true
    });
});
```




```javascript
82 });

83 $("#loadData").click(function() {

84     generateNewChart();

85 });

```

```javascript
86 function generateNewChart(){

87     var color = Chart.helpers.color;

88     var config = {

89         type: 'line',

90         data: {

91             datasets: [{

92                 label: 'Negative Feedback Score',

93                 backgroundColor: color(window.chartColors.red).alpha(0.5).rgbString(),

94                 borderColor: window.chartColors.red,

95                 fill: false,

96                 data: []

97             },

98             {

99                 label: 'Positive Feedback Score',

100                backgroundColor: color(window.chartColors.green).alpha(0.5).rgbString(),

101                borderColor: window.chartColors.green,

102                fill: false,

103                data: []

104            }

105            ]

106        },

```

### 示例代码 5：`timesegment.php`——基本图表配置——第二部分

在示例代码 6 中，定义了图表的选项。在此示例中，我们在第 111 行将图表设置为响应式。这允许当用户与鼠标交互时图表移动，当图表上有比可用空间更多的数据时。`title` 设置为 `true` 以显示可见性，并且 `title` 的文本在第 114 行设置。

在第 116 行，用于图表的 `scales` 被用来定义图表的 X 和 Y 轴。X 在图表上水平显示。第 122 行，`labelString` 设置为 `Time stamp` 以向用户显示我们正在处理时间。图表的刻度标记（即每条记录的独立标记）在第 127 行的 `fontColor` 设置为 `#000000`，即黑色。第 131 行，用于图表的 Y 轴用来显示垂直显示在图表左侧上的文本 `Feedback Score`。

```javascript
110   options: {

111       responsive: true,

112       title: {

113           display: true,

114           text: 'Time Segment Analysis'

115       },

116       scales: {

117           xAxes: [{

118               type: 'time',

119               display: true,

120               scaleLabel: {

121                   display: true,

122                   labelString: 'Time stamp'

123               },

124               ticks: {

125                   major: {

126

127                       fontColor: '#000000'

128                   }

129               }

130           }],

131           yAxes: [{

132               display: true,

133               scaleLabel: {

134                   display: true,

135                   labelString: 'Feedback Score'

136               }

137           }]

138       }

139   }

140 };

```

### 示例代码 6：`timesegment.php`——添加 X 和 Y 轴——第三部分

在示例代码 7 中，一旦配置创建完成，就可以定义主图表。在第 141 行创建一个标题为 `ctx` 的单变量，它作为对之前在图表中定义的 `canvas` 标签的引用点。图表的上下文设置为 `2d`，即二维。第 142 行，`window.myLine` 变量被设置为 `Chart()` 对象的新实例，该对象接受两个参数，以 `ctx` 引用形式的 `context` 和第 88 行的 `config` 变量。由于用户界面提供用户选择日期的能力，需要获取用户输入的时间值以及他们希望查看的时间窗口，因此这些值必须被检索。

## 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

其中第一个是 `日期` 变量。由于数据存储在一个简单的 HTML `input` 字段中，可以使用 jQuery 选择器通过之前设置为 `datepicker` 的 ID 来选择该元素，如第 145 行所示。然后，`val()` 函数从所选字段中提取出值。

用户输入的时间也存储在一个简单的文本 `input` 字段中，但由于时间格式可能各不相同，因此使用 JavaScript 库 `moment` 来处理时间。

在第 147 行，此过程的第一步是创建一个对 `moment` 库的新调用。在此调用中传递了两个参数。第一个是输入的原始时间格式。这是通过使用 jQuery 选择器选择输入字段，并使用 `.val()` 函数提取原始值来获取的。传递的第二个参数是时间戳的原始格式。在本例中，为 `h:mm A`，它接收原始日期格式，例如 `1:00 AM`。这会被格式化为 `HH:mm`，即时间的 24 小时制变体，例如 `01:00`。

有关这些模式的更多信息，可以在 `moment.js` 网站上找到。

> https://momentjs.com/docs/#/manipulating/

返回的结果将是日期后跟一个反馈分数的格式。返回的每条记录使用逗号分隔。因此，为了处理每条记录，在第 159 行调用了 `split()` 函数，传递一个逗号作为分隔符。此过程的结果是一个存储在 `result` 变量中的记录数组。在第 160 行，使用 `forEach()` 函数进行简单迭代，这使我们能够访问集合中的每个单独的 `record`。这是我们分配给单个记录的变量名。

返回的记录必须分成四个部分：数组的 0 位置是 `年`、`日` 和 `月`，1 位置是 `时间`，3 位置是 `反馈分数`。要执行此操作，在第 161 行调用了 `split()` 函数，传递一个空格作为分隔符。

要将数据添加到图表数据集，在第 162 行引用了 `config.data.datasets[0]`。这指向在 `config` 变量中创建的原始数组。数据集的 0 位置仅用于负面反馈记录。要将新数据添加到图表的数据集数组中，调用了 `push()` 函数。它接受两个参数：`x` 值和 `y` 值。第一个是单个 `date[0]`，即日期，后跟 1 位置，即记录被记录的时间。Y 轴值是存储在数组 2 位置的介于 1 和 10 之间的反馈分数。

在循环迭代完成后，在第 167 行调用 `window.myLine.update()` 函数来渲染对图表所做的更改。

```javascript
141   var ctx = document.getElementById('canvas').getContext('2d');

142   window.myLine = new Chart(ctx, config);

143

144   // get values entered by the user

145   var date = $('#datepicker').val();

146   console.log($('#timepicker').val())

147   var time = moment($('#timepicker').val(), ["h:mm A"]).format("HH:mm");

148   console.log("time new" + time);

149

150   var minutes = $('#minutes').val();

151

152   if(minutes.indexOf('h') > -1){

153       minutes = minutes.replace('h', '');

154       minutes = minutes * 60;

155   }

156   // get negative records

```

### 示例代码 7：`timesegment.php`——将记录追加到数据集——第 4 部分

在示例代码 8 中，为了收集正面反馈记录，代码是相同的，唯一的更改是第 170 行的 `type` 参数设置为 `positive`，以及第 175 行对正面数据集记录的引用，该引用位于数据集数组的 1 位置。同样，通过在第 180 行调用 `window.myLine.update()` 函数来更新图表。

在添加了用于渲染图表的主函数之后，在第 183 行添加了一个名为 `newDate()` 的第二个函数。它接收来自数据库的时间戳，并将其格式化为年、月、日格式，后跟小时、分钟和秒。这将返回数据库中存储为 `2020-08-26 10:22:01` 的时间戳。

```javascript
169  // get positive records

170 $.get("getTimeRecords.php", { type: "positive", dstart: date,

171     tstart: time, minutes:minutes} )

172     .done(function(data) {

173         var result = data.split(',');

174         result.forEach((record) => {

175             var single = record.split(' ');

176             config.data.datasets[1].data.push({

177                 x: newDate(single[0]+single[1]),

178                 y: single[2],

179             });

180         });

181         window.myLine.update();

182 }); // end of GET

```

```javascript
function newDate(stamp) {

    return moment(stamp, "YYYY-MM-DD HH:mm:ss");

}

</script>

```

### 示例代码 8：`timesegment.php`——执行 `GET` 请求——第 5 部分

**示例代码：`getTimeRecords.php`**

为了从数据库中检索记录用于图表生成过程，创建了第二个名为 `getTimeRecords.php` 的 PHP 页面。在示例代码 9 中，第 2 行使用 `GET` 函数检索请求的反馈 `类型`，例如 `positive` 或 `negative`。这存储在 `type` 变量中。第 3～9 行建立了与数据库的连接。

第 10 行使用一个简单的 `if` 语句来检查 `type` 变量是设置为 `positive` 还是 `negative`。根据该值，在第 11 行或第 14 行调用 `getRecords()` 函数，该函数接收 `type`。这使我们能够为正面和负面记录重用相同的代码体。第 16 行声明了 `getRecords()` 函数，它接受单个参数 `sort`，该参数将包含值 `positive` 或 `negative`。

在此函数内，第 18、19 和 20 行检索通过 JavaScript `GET` 传递的每个参数。这些包括感兴趣的日期、感兴趣的时间以及所需时间窗口的大小（以分钟为单位）。创建一个名为 `start` 的新变量，将日期和时间用单个空格连接在一起。第 22 行，将此日期传递给 `DateTime` PHP 对象的新实例。此 `DateTime` 允许我们创建时间的偏移量，例如，感兴趣时间之后的分钟数。执行此过程是为了导出感兴趣的结束时间，该时间将用于我们的 SQL 查询。第 24 行，`modify()` 函数接收偏移量，即我们希望更改原始时间戳的分钟数。此结束时间存储在第 25 行的 `end` 变量中。调用 `format()` 函数将日期和时间格式化为从数据库检索所需的格式。

由于此函数用于正面和负面反馈，因此使用简单的 `if` 语句生成一段 SQL，该 SQL 将被添加到 SQL 查询中。这从第 26 行创建一个名为 `params` 的数组开始，该数组包含感兴趣的开始和结束时间。如果传递给函数的 `sort` 变量是正数，则在第 29 行将 `scoreSort` 变量设置为 `score >= 5`。当该变量设置为负数时，则在第 32 行将 `scoreSort` 设置为 `score < 5`。

## 基于时间的反馈分析

在第 34 行，SQL 查询被构建以从 `timeanalysis` 表中选择 `mytime` 和 `score` 列。过滤是通过添加一个 `WHERE` 子句实现的，该子句定义我们感兴趣的是时间戳大于或等于？（即 `params` 数组中的第一个值）且时间戳小于或等于？（即数组中的第二个参数，例如结束时间）的记录。还追加了一个 `AND`。然后追加了用于 `scoreSort` 的 SQL。过程中的最后一步是 `ORDER BY`，它表明我们希望按时间戳对记录进行排序。

在第 36 行，调用 `execute()` 函数，传入参数，随后调用 `fetchAll()` 函数以返回所有记录。

过程中的最后一步是生成 `output` 变量。该变量是基于从数据库检索到的内容构建的。对于数据库中的每一行，在第 40 行，输出被追加以包括 `row[0]`，其中包含时间戳后跟一个空格，随后是 `row[1]`，其中包含分数。每行完成时添加冒号，该冒号用作返回给前面定义的 JavaScript `GET` 请求的记录之间的分隔符。

生成的输出在第 42 行通过调用 `substr()` 函数进行处理，该函数接受两个参数：起始索引（设置为 0）和结束索引（设置为 -1 以从 `output` 变量中移除最后的分号）。

所有数据都输出到页面，返回到 `timesegment.php` 页面上的原始 JavaScript `GET` 请求以供绘图。

```php
<?php

$type = $_GET['type'];

try {

    $host = 'localhost:3306';

    $dbname = 'bookexamples';

    $user = 'sampleuser';

    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);

} catch(PDOException $e) {echo $e;}

if($type=='positive'){

    getRecords('positive');

}

else if($type=='negative'){

    getRecords('negative');

}

function getRecords($sort){

```

## 基于时间的反馈分析 237

```php
    global $DBH;

    $dateStart = $_GET['dstart'];

    $timeStart = $_GET['tstart'];

    $minutes = $_GET['minutes'];

    $start = $dateStart . ' ' . $timeStart;

    $dt = new DateTime($start);

    $offSet = $minutes;

    $dt->modify("+{$offSet} minutes");

    $end= $dt->format('Y-m-d H:m');

    $params = array($start, $end);

    $scoreSort = '';

    if($sort == 'positive'){

         $scoreSort = 'score >= 5';

    }

    else if($sort == 'negative'){

         $scoreSort = 'score < 5';

    }

    $sql = "SELECT timestamp, score FROM timeanalysis  where

         TIMESTAMP >= ? AND TIMESTAMP <= ? AND $scoreSort ORDER

         BY timestamp";
```



```php
$sth = $DBH->prepare($sql);

$sth->execute($params);

$res = $sth->fetchAll();

$output = '';

foreach ($res as $row) {
    $output .= $row[0] . ' ' . $row[1] . ',';
}

echo substr($output, 0, -1);
```

**示例代码 9：** 根据时间戳和分数检索正面和负面反馈。

## 输出

图 7.4：两小时窗口内正面和负面反馈的时间分段分析。可以看到，正面记录显示为绿色，负面反馈记录显示为红色。

在处理来自客户的反馈时，反馈留下的时间可能很重要。考虑一组正在与 Web 应用程序交互并试图下订单的用户，而该网站开始出现故障。这很快会给企业带来问题。在这种情况下，反馈留下的时间可能非常重要。关注负面反馈而不是正面反馈将是主要的兴趣领域。

在本节中，我们将概述在实时环境中查看来自客户的反馈的过程。这种情况的一个例子是当用户留下低于特定阈值的反馈时，例如在 1 到 10 的尺度上低于 5。将使用 Smoothie Charts JavaScript 库进行图表生成过程。此图表与之前的图表不同，它将随着用户在实时的反馈继续从右向左跨屏幕移动。它可以被视为一条移动折线图（Moving line graph）。该库可从[平滑图表](http://smoothiecharts.org/)获取。

### 示例 3：实时图表分析

此示例由三个文件和两个库组成：

1. `create.sql` — 此文件包含创建*实时*表的 SQL，用于存储反馈记录。
2. `realtime.php` — 此文件用于渲染图表。
3. `recordFetch.php` — 此文件用于从数据库检索反馈记录。
4. Smoothie Charts — 这是用于渲染图表的主要 JavaScript 库。
5. jQuery — 该库用于执行 JavaScript GET 请求。

### 示例代码：`create.sql`

在样本代码 10 中，数据库表包含一个唯一的 ID 列作为主键并自动递增。添加了一个 DATETIME 列，在创建记录时会自动设置当前时间戳。最后添加了一个 score 列，用于存储用户输入的分数。在此示例中，我们将处理 1 到 10 之间的分数。

```sql
CREATE TABLE `realtime` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `datetime` DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
    `score` TINYINT,
    PRIMARY KEY (`id`)
);
```

**示例代码 10：** 样本实时数据库表。

### 示例代码：`realtime.php`

在样本代码 11 中，显示了一个名为 `realtime.php` 的新文件。在此文件的顶部，我们将包含两个 JavaScript 库。第一个是在第 5 行对 `smoothie.js` 文件的引用，它位于与 PHP 页面相同的文件夹中。在第 6 行，对 jQuery CDN 进行了引用，这将允许我们使用 JavaScript GET 函数。

完成头部之后，可以添加文档的主体。一个简单的 `h1` 标签用于在第 9 行在页面顶部添加文本。这后跟一个 `canvas` 标签，位于第 10 行。该标签的 ID 设置为 `mycanvas`。Canvas 的高度和宽度属性分别设置为 500 和 500。这是持有图表的主要容器。

图表生成过程的核心基于额外添加的 JavaScript 库。为了开始此过程，首先在第 13 行添加了一个脚本标签。这后跟对当前日期的引用，可以使用第 15 行的 `new Date()` 函数检索。该函数本身将返回一个完整的字符串，参考用户所在的时区。由于这可能与我们数据库中存储的数据不相关，包含日期的变量需要进一步处理。

在第 16 和 17 行，创建了两个名为 `date` 和 `time` 的变量。对之前检索到的 `now` 变量调用了 `getFullYear()`、`getMonth()` 和 `getDate()` 函数。在这些提取之后，还可以调用以提取小时、分钟和秒。此方法的好处是我们可以添加日期和时间之间所需的分隔符。在这种情况下，日期组件之间使用破折号，时间之间使用冒号。在第 18 行，`date` 和 `time` 变量都被追加到一起并放入 `currentTime` 变量中。

收集时间后，需要在新的一行添加到图表上。这是通过调用第 19 行的 `TimeSeries()` 对象完成的。该引用被放置在 `line1` 变量中。由于数据库表中存在大量记录，每个都有自己唯一的 ID，因此在第 20 行创建一个名为 `currentIdProcessed` 的变量。这将用作记录已添加到图表的 ID 的存储设施，确保没有带有此 ID 或更低的记录将添加到图表上。仅可视化新记录，坚持实时主题。

在第 22 行，使用 `setInterval()` 函数创建循环，以便在添加新记录时移动图表。在此代码的非常末尾，添加了 2000 作为迭代之间要添加的毫秒数。可以更改它以使更新更频繁或不那么频繁。在这种情况下，2000 将在更新之间提供两秒延迟。

对于 `setInterval()` 函数的每次调用，在第 23 行都会调用 jQuery GET 函数来调用 `recordFetch.php` 页面，该页面是图表的主要信息来源。与此调用一起传递了两条数据：`time` 变量，设置为系统的当前时间；以及 `currentRecord` 变量，设置为存储从数据库检索的最新记录的 ID 的 `currentIdProcessed` 变量的值。当调用 `recordFetch.php` 页面时，数据将以第 24 行的 `data` 变量中的单字符串形式返回。当记录被返回时，`done()` 函数将在第 24 行触发。

在此函数内部，`data` 变量可用。此变量包含一个字符串，其中包含检索到的记录的 ID 和分数，这是由用户留下的值。该值使用单个破折号进行分隔。在第 25 行，一个简单的 `if` 语句用于检查 `data` 变量是否包含数据。如果包含，则开始处理 `data` 变量。为了在第 26 行处理它，对 `data` 变量调用了 `split()` 函数。破折号用作分隔符来分割记录。此过程的结果是一个名为 `result` 的数组。

分割过程完成后，在第 27 行，使用 `new Date().getTime()` 生成一个新的时间戳，该函数返回纪元格式的时间。紧随其后的是 `result[1]`，其中包含用户输入的反馈分数。此数据被附加到 `line1` 对象中。

在第 28 行，一个简单的 `console.log()` 用于在控制台中打印出已附加到图表的 ID 和分数，以供调试过程使用。在第 29 行，存储在数组 `result[0]` 中的当前记录的 ID 被设置为 `currentIdProcessed` 变量的当前值。这将在循环的未来迭代中使用，以防止再次调用同一记录。

在第 33 行创建了一个新的 SmoothieChart，其引用存储在 `smoothie` 变量中。可以设置图表的颜色和样式。在此示例中，`strokeStyle` 使用 RGB 数字设置，后跟 `fillStyle` 和 `lineWidth`。`millisPerLine` 设置为 250，这是背景中显示的网格之间的间隔。显示的垂直部分数设置为 6。在第 34 行，调用了 `addTimeSeries()` 函数，该函数接收对 `line1` 对象的引用。设置了 `strokeStyle`、`fillStyle` 和 `lineWidth`。在第 35 行，此过程的最后一步是将 smoothie 图表设置为流式传输到之前创建的 `canvas` 标签，其 ID 设置为 `mycanvas`。我们将 2000 设置为此过程的间隔。

```html
<!DOCTYPE html>
<html>
<head>
    <title>Negative Feedback Real-time view</title>
    <script type="text/javascript" src="smoothie.js"></script>
    <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
</head>
<body>
    <h1>Negative Feedback Real-time view</h1>
    <canvas id="mycanvas" width="500" height="400"></canvas>
</body>
</html>
```

```javascript
<script type="text/javascript">
// get the current date and time

var now = new Date();
var date = now.getFullYear() + '-' + (now.getMonth() + 1) + '-' + now.getDate();
var time = now.getHours() + ":" + now.getMinutes() + ":" + now.getSeconds();
var currentTime = date + ' ' + time;
var line1 = new TimeSeries();
var currentIdProcessed = '';

// start the updating loop

setInterval(function() {
    $.get("recordFetch.php", {
        time: currentTime,
        currentRecord: currentIdProcessed
    }).done(function(data) {
        if (!(data.length == 1)) {
            var result = data.split('-');
            line1.append(new Date().getTime(), result[1]);
            console.log("adding new record" + result[0] + " " + result[1]);
            currentIdProcessed = result[0];
        }
    });
}, 2000);

var smoothie = new SmoothieChart({
    grid: {
        strokeStyle: 'rgb(125, 0, 0)',
        fillStyle: 'rgb(60, 0, 0)',
        lineWidth: 1,
        millisPerLine: 250,
        verticalSections: 6
    },
    labels: {
        fontSize: 16
    }
});

smoothie.addTimeSeries(line1, {
    strokeStyle: 'rgb(255, 0, 0)',
    fillStyle: '',
    lineWidth: 3
});

smoothie.streamTo(document.getElementById("mycanvas"), 2000);
</script>
```

**示例代码 11：** `realtime.php` — 随着记录添加到数据库而实时更新的图表。

### 示例代码：`recordFetch.php`

创建了第二个页面，该页面负责从名为 `recordFetch.php` 的数据库中检索记录。在示例代码 12 中，`currentRecord` 变量在第 2 行从 `GET` 中获取。紧随其后的是第 3 行的 `date` 变量，该变量包含相关记录的时间戳。为了允许此示例在测试期间用于静态记录集合，`date` 记录可以替换为包含反馈记录集合的静态日期。在第 9 行，创建了与 MySQL 数据库的连接。

要从数据库中检索记录，在第 11 行创建了一个名为 `params` 的数组，该数组包含最后检索到的记录的 ID 和感兴趣的日期。在第 12 行，创建了一个 `SELECT` 语句。此语句包含一个 WHERE 子句，该子句仅返回大于所提供 ID 的 ID。这些结果按日期排序，日期大于或等于所提供的日期。问号用于替换字符串中的变量作为未命名的占位符。设置了第二个排序顺序，即 ID 列升序。添加了 LIMIT 1 以仅返回单条记录。该语句和参数在第 13 行使用 `prepare()` 函数组合在一起，随后在第 14 行调用了 `execute()` 函数。

在第 15 行，记录被获取并放入名为 `res` 的局部变量中。在第 16 行，以图表将处理的格式生成最终输出。此格式是存储在 `res` 变量中的数据库行的第 0 列，即行的 ID，后跟一个破折号，再后跟分数，该分数存储在 `res` 数据库行的位置 2。

```php
<?php

$id = $_GET['currentRecord'];

$date = '2019-8-18 20:36:18'; // only used for static example

try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = 'SCDASAO9BSOEt4SAADBaZIBABBOADSIIBCSDACO';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
} catch (PDOException $e) {
    echo $e;
}

$parms = array($id, $date);

$sql = "SELECT * FROM realtime WHERE Id=? AND datatime >= ? ORDER BY id ASC LIMIT 1";

$sth = $DBH->prepare($sql);

$sth->execute($parms);

$res = $sth->fetch();

echo $res[0] . '-' . $res[2];

?>
```

示例代码 12：`recordFetch.php` — 从实时数据库表中检索记录。

## 负面反馈实时视图

![实时反馈分数报告折线图。](img/ed4cb7e1be98f0adec0546edd14f6223_268_0.png)

图 7.5：实时反馈分数报告折线图。

**输出**

图 7.5 显示了最终的图表。在此图中，最大和最小分数将存储在图表的右侧。每 2 秒，图表将更新更多数据。

## 7.5 正面与负面反馈日历

查看反馈分数时，查看整个一年可能是一个有益的过程，因为它提供了反馈逐日记录的上下文。在本节中，我们将概述使用 Google Charts 生成基于 JavaScript 的图表的过程。这些图表为绘图提供了简单的最小实现，所需开销很小。日历的完整 API 可在[https://developers.google.com/chart/interactive/docs/gallery/calendar](https://developers.google.com/chart/interactive/docs/gallery/calendar)找到。由于这些是基于日历的图表，将在同一页面中添加两个不同的图表，一个图表用于一年的正面反馈，第二个图表显示同一年的负面反馈。

### 示例 4：反馈日历

此示例包含三个文件和两个库：

1. `create.sql` — 这包含创建 `calendar` 数据库表的 SQL。
2. `calendar.php` — 这包含用于可视化的主 JavaScript。
3. `calendarGetRecords.php` — 这检索要在日历上绘制的记录。
4. Google Charts — 此库包含可视化过程中使用的主要日历。
5. jQuery — 这用于执行到 `calendarGetRecords.php` 页面的 JavaScript `GET` 请求。

### 示例代码：`create.sql`

在我们开始可视化记录之前，需要一些正面和负面反馈记录用于一系列日历日期。将创建一个 MySQL 表，其中包含记录的 ID、时间戳、用户输入的反馈文本以及用户给出的 1 到 10 之间的分数。

```sql
CREATE TABLE `calendar` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `timestamp` TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
    `feedbacktext` TEXT,
    `score` TINYINT,
    PRIMARY KEY (`id`)
);
```




## 示例代码：`calendar.php`

我们将创建一个新的 PHP 页面，标题为`calendar.php`。在示例代码 13 中，第 3 行添加了一个内容分发网络以引入 jQuery。第 4 行引入了 Google Charts 的 JavaScript 加载器。第 6 行调用了 Google Chart 的`load()`函数。该函数接受两个参数：`current`，指定我们希望使用当前版本的 API；以及`packages`，引用可使用的不同类型的图表。在本例中，我们加载的是`calendar`包。

当图表准备好后，第 7 行和第 8 行调用`setOnLoadCallback()`函数，该函数接受一个指向我们想要用于生成图表的函数的引用。在本示例中，我们调用的函数是`drawPositiveChart()`函数和`drawNegativeChart()`函数。第 9 行添加了`drawPositiveChart()`函数，用于图表生成过程。在该函数内部，第 10 行创建一个新的`DataTable`对象，包含所有正面和负面评价。第 11 行调用`dataTable.addColumn()`函数，允许我们添加可视化所需的列。在本示例中，我们添加了一列用于日期，另一列用于反馈数量，当鼠标悬停在图表上时将显示该数量。

第 13 行注释掉了一条记录样本结构，以供将来参考。图表首次加载时，此处不添加任何数据。第 17 行创建一个新的`chart`对象，引用稍后将要添加的`calendar_positive`元素。第 19 行创建一个`options`对象，允许我们指定图表的`title`（标题）和`height`（高度）。

添加列之后，开始向图表添加数据。添加到图表的每一行都是一个新`Date`对象，包含我们要绘制信息的年份、月份和日期。后跟一个可正可负的单独数字，当鼠标光标放置在该单元格上时将显示该数字。该数字将从白色渐变到深蓝色，具体取决于添加的数值。数值越高，单元格的蓝色越深。

第 23 行，向`calendarGetRecords.php`页面发起一个 jQuery `GET`请求以获取要绘制的数据。传递了一个`type`参数，表明我们想检索`positive`（正面）反馈记录。第 24 行，当结果返回时，`data`变量变为可用。这包含将绘制到图表上的记录。

在`done()`内部（第 24 行），第 25 行添加了一个简单的`console.log()`以查看返回的数据，帮助调试。第 26 行，`data`变量根据用于分隔每个日期的逗号进行拆分，结果放入`singleDates`数组中。

`data`变量中返回的结果包含用破折号分隔的日期和分数（针对单个值），以及记录之间用逗号分隔的，例如，`2019-02-11-3`表示日期`2019-02-11`，后接分数`3`。后续记录以逗号作为唯一的分隔符，例如，`2019-02-11-3,2019-02-24-11,2019-03-24-9,2019-06-19-25`。

第 27 行，使用`for`循环遍历每个日期。对于第 28 行的每个单独日期，调用`split()`函数根据年份、月份、日期和反馈总数之间的破折号来拆分日期。为了帮助调试，第 29 行添加了另一个`console.log()`。正在查看的`singleDate`的每个组成部分都可以通过数组索引 0 到 3 来访问。

最后，为了将新数据添加到图表上，第 30 行调用`dataTable.addRow()`函数。该函数接受一个日期对象，后跟一个表示当天记录总数的数字。创建一个新的日期，并添加`oneDate[0]`作为年份，`oneDate[1]`作为月份，`oneDate[2]`作为日期。日期对象结束，并使用逗号将附加的分数与`oneDate`数组中位置 3 的元素分隔开。

由于该数字最初返回的表示形式是字符串，因此使用`Number()`函数将其转换为数字。在将行添加到图表并且`for`循环完成最终迭代之后，第 32 行调用`chart.draw()`函数，该函数接受刚刚填充的`dataTable`，后跟`options`数组。

```html
<html>

<head>

<script
src="https://code.jquery.com/jquery-3.4.1.min.js"></script>

<script type="text/javascript"
src="https://www.gstatic.com/charts/loader.js"></script>

<script type="text/javascript">

google.charts.load("current", {packages:["calendar"]});
google.charts.setOnLoadCallback(drawPositiveChart);
google.charts.setOnLoadCallback(drawNegativeChart);

function drawPositiveChart() {

var dataTable = new google.visualization.DataTable();

dataTable.addColumn({ type: 'date', id: 'Date' });
dataTable.addColumn({ type: 'number', id: 'Feedback Count'
});

dataTable.addRows([

    // Sample records that can be added to the chart.
    //[ new Date(2019, 3, 13), 2 ],

]);

var chart = new
  google.visualization.Calendar(document.getElementById
("calendar_positive"));

var options = {
    title: "Positive Feedback Analysis",
    height: 350,
};

$.get( "calendarGetRecords.php", { type: "positive"} )
    .done(function( data ) {
        console.log(data);
        var singleDates = data.split(',');
        for(var i=0; i< singleDates.length; i++){
            var oneDate = singleDates[i].split('-');
            console.log(oneDate[0], oneDate[1], oneDate[2],
                oneDate[3]);
            dataTable.addRow( [ new Date(oneDate[0],
                oneDate[1], oneDate[2]), Number(oneDate[3])
                ]  );
        }
        chart.draw(dataTable, options);
});

}

```

示例代码 13：`calendar.php` —— 初始图表设置和 `GET` 请求 —— 第 1 部分。

在示例代码 14 中，负面反馈图表的生成过程相同，仅有小幅变动。向`calendarGetRecords.php`页面发起的`GET`请求在第 50 行传递了`type`变量，其值设置为`negative`。

该过程的最后一步是创建 HTML 页面的主体。第 64 行添加`body`标签，其中创建了一个带有唯一 ID `calendar_positive`的`div`标签（第 65 行）。使用`style`属性设置可视化的宽度和高度。对第二个 ID 设置为`calendar_negative`的`div`重复相同的过程（第 67 行）。

```javascript
function drawNegativeChart() {

    var dataTable = new google.visualization.DataTable();

    dataTable.addColumn({ type: 'date', id: 'Date' });
    dataTable.addColumn({ type: 'number', id: 'Feedback Count'
    });

    dataTable.addRows([
      // first sample records that can be hardcoded.
      //[ new Date(2019, 3, 13), 2 ],
    ]);

    var chart = new
    google.visualization.Calendar(document.getElementById('calendar_negative'));

    var options = {
      title: "Negative Feedback Analysis",
      height: 350,
    };

    $.get("calendarGetRecords.php", { type: "negative"} )
      .done(function( data ) {
        console.log(data);
        var singleDates = data.split(',');
        for(var i=0; i< singleDates.length; i++){
          var oneDate = singleDates[i].split('-');
          console.log(oneDate[0], oneDate[1], oneDate[2],
            oneDate[3]);
          dataTable.addRow([ new Date(oneDate[0],
            oneDate[1], oneDate[2]), Number(oneDate[3])
          ]);
        }
        chart.draw(dataTable, options);
      });
}
</script>

</head>

<body>

  <div id="calendar_positive" style="width: 700px; height: 200px;"></div>

  <hr>

  <div id="calendar_negative" style="width: 700px; height: 200px;"></div>

</body>

</html>
```

示例代码 14：`calendar.php` —— 为负面图表收集数据 —— 第 2 部分。

## 示例代码：`calendarGetRecords.php`

为了通过`GET`请求从数据库获取数据，创建了第二个名为`calendarGetRecords.php`的 PHP 页面。在示例代码 15 中，该页面从第 2 行的`$type`变量开始，该变量用于获取发送到页面的请求类型。在本图表中，可用的两种数据类型是正向和负向反馈分数。第 10-15 行根据`type`变量的值，调用相应函数：使用`getPositiveRecords()`函数获取正向反馈，或使用`getNegativeRecords()`函数获取负向反馈。

在`getPositiveRecords()`函数内部，第 17 行添加了关键字`global`以引用数据库连接`$DBH`。第 18 行构建了 SQL 查询，用于从数据库中检索所有正向反馈记录。此查询从数据库中选择时间戳并将其转换为日期，然后将该列引用为`date`。执行`count(score)`来计算被引用为`score`列的分数记录数量。这些操作在日历数据库表上执行，条件是分数大于 5。添加了`GROUP BY`语句，根据时间戳列对记录进行分组。这种方法允许数据库返回每个存储反馈的唯一日期的总分数。

第 19 行调用了`prepare()`函数，随后是`execute()`函数。第 21 行调用了`fetchAll()`函数，该函数将从数据库返回所有相关记录。第 22 行的一个名为`$output`的变量用作占位符，用于在每次循环迭代时累积记录。

在此示例中，`$row[0]`表示 YYYY-MM-DD 格式的日期，后跟一个连字符，再后跟`$row[1]`，其中包含该给定日期的记录总数。为每个单独记录添加一个逗号作为分隔符。这一点很重要，因为前面描述的 JavaScript `GET`函数在处理过程中使用此分隔符来拆分日期。此过程的最后一步是使用第 26 行的`substr()`函数，该函数接受`$output`变量、起始位置（例如 0）和结束位置（例如 -1），这将去除完整输出的最后一个逗号。此输出使用`echo`语句打印，当被调用时，将把内容返回给`GET` JavaScript 函数。

负向反馈记录的处理过程与正向反馈记录非常相似。唯一需要修改的地方是`WHERE`子句。关注的分数是那些小于或等于 5 的分数。

```php
<?php

$type = $_GET['type'];

try {

    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);

} catch(PDOException $e) {
    echo $e;
}

if($type=='positive'){
    getPositiveRecords();
} else if($type=='negative'){
    getNegativeRecords();
}

function getPositiveRecords(){

    global $DBH;

    $sql = "SELECT DATE(TIMESTAMP) AS date,COUNT(score) AS score FROM calendar WHERE score > 5 GROUP BY DATE(TIMESTAMP)";

    $sth = $DBH->prepare($sql);
    $sth->execute();

    $res = $sth->fetchAll();
    $output = '';

    foreach ($res as $row){
        $output .= $row[0] . '-' . $row[1] . ',';
    }

    echo substr($output, 0, -1);
}

function getNegativeRecords(){

    global $DBH;

    $sql = "SELECT DATE(TIMESTAMP) AS date,COUNT(score) AS score FROM calendar WHERE score <= 5 GROUP BY DATE(TIMESTAMP)";

    $sth = $DBH->prepare($sql);
    $sth->execute();

    $res = $sth->fetchAll();
    $output = '';

    foreach ($res as $row){
        $output .= $row[0] . '-' . $row[1] . ',';
    }
}
```

250 应用用户数据收集与分析：使用 JavaScript 和 PHP




## 输出

图 7.6 显示了绘图过程的最终输出。图表展示了两个图表，顶部图表是正向反馈记录，底部图表是负向反馈记录。在屏幕的右上角，我们可以看到颜色深浅索引。颜色越浅，记录越少。颜色越深，反馈记录越多。

![图 7.6](img/ed4cb7e1be98f0adec0546edd14f6223_276_0.png)

**图 7**：正向和负向反馈的日历视图。单元格的深浅表示记录数量。

在`图 7`中，我们可以看到，当鼠标悬停在日历上时，会提供该日期的反馈记录总数。

### 反馈热力图

在分析反馈时，反馈留下的时间通常会出现模式。日历代表用户可以选择的单个日历日。对于选定的一天，每个小时将表示为一个独立的块。在每个小时块内，它进一步细分为五分钟的窗口。

对于每个单独的时间窗口，将计算收集到的反馈记录总数。这些块将根据找到的记录数量着色。较浅的颜色将用于标识较少的记录数量，较深的颜色将用于标识较高的记录计数。

这种基于颜色的方法可以一目了然地提供反馈留下的时间段的详细信息。对于每个不同的时间段，可以使用光标动态显示该时间段的总数。通过使用这种基于光标的方法，默认情况下添加到图表的数据总量是最小的，并且在需要时可以提供额外的数据。

### 示例 5：热力图

此示例包含两个文件和两个库：

1. `heat.php` - 这是用于显示可视化的主 PHP 页面。
2. `getRecords.php` — 此页面负责从数据库中收集记录。
3. `jQuery` — 用于对`getRecords.php`页面执行`GET`请求。
4. `jQueryUI` — 用于添加自定义日期选择器小部件。

### 示例代码：`heat.php`

为了开始此图表，创建了一个名为`heat.php`的新 PHP 文件。在示例代码 16 中，第 3 行包含了 jQuery 的内容分发网络（CDN）。第 4 行添加了 jQueryUI CDN。随后是第 5 行对 jQueryUI 使用的 CSS 文件的引用。

第 7 行添加了一个新的`style`标签，首先用于设置页面的`font`。在此示例中，我们使用`arial`字体。第 11 行创建了 CSS 类`colorRow`。此类用于更改将显示的每个单独时间片段的布局。首先设置`height`，然后是`width`。`left`边距设置为`35px`，以在首先打印的时间和旁边将显示的彩色行之间提供空间。单独行的背景颜色默认设置为红色。这将根据给定时间发现的反馈量更改为较浅的阴影。

第 19 行创建了一个新的`variable`标签，标题为`step`。此变量用作颜色编码过程的核心。对于给定的反馈记录集合（例如 20 条单独记录），对于上午 09:00 到 09:05 之间的给定五分钟窗口，可能只有 12 条反馈记录。对于稍后的时间，例如上午 10:30 到 10:35，可能收集了两条记录。收集反馈记录的其他每个时间可能落在这些时间之外（例如，其他六条记录）。在这种情况下，当天给定时间段的最大可能计数为 12 条记录。为了将其从浅色到深色进行颜色编码，将使用红色表示最大值（12），而较浅的红色阴影将用于表示较低的值（例如 2）。可能的最小记录数为零，这将是图表所需的最浅颜色。

为了计算这个，`step`变量通过取给定日期的最大记录数除以 10 来计算。这允许在图表上表示十种不同的阴影。不是直接更改颜色，而是将更改红色的`opacity`。这允许轻松操作任何基础颜色，使其范围从最浅的 0.0 到最深的 1.0。

![](img/ed4cb7e1be98f0adec0546edd14f6223_277_0.png)

**图 7.7**：鼠标悬停显示给定日期的记录数量。

在第 22 行，使用了一个简单的`span`标签来为图表添加标题。紧接着在第 23 行，有一个`input`输入框，其`ID`设置为`datepicker`。这个`input`输入框稍后将进行修改，以便使用 jQueryUI 日历作为日期选择机制。在第 24 行，添加了一个`button`按钮，用于触发图表生成过程。该按钮的`ID`设置为`viewChart`，稍后将为其附加一个`click()`事件处理程序。

在第 26 行，创建了一个`script`标签，并调用了`on load`函数。当页面加载时，第 27 行将 HTML`input`输入框转换为 jQuery UI 日期选择器。可以添加所需的日期格式。在此示例中，我们将日期格式设置为`yy-mm-dd`，这使我们能够以`2020-09-02`这样的格式来表示日期。在第 30 行，添加了一个`div`标签，其`ID`设置为`chart`。这用于容纳将要生成的主图表。

```html
<html>

<head>

<script
    src="https://code.jquery.com/jquery-3.4.1.min.js"></script>

<script src="http://code.jquery.com/ui/1.12.1/jquery-ui.min.js">
    </script>

<link rel="stylesheet" type="text/css"
    href="http://code.jquery.com/ui/1.12.1/themes/base/
    jquery-ui.css">

"><?记得fenxi.BiFunction，

<style>

*{
    font-family: arial;
}

.colorRow {
    height:13px;
    width:50px;
    margin-left: 35px;
    background-color:red;
}

</style>

</head>

<script>

var step = 0;

</script>

<span style="font-size:16pt">Feedback Heat Map </span>

<p>Date: <input type="text" id="datepicker">
<button id="viewChart">View Chart</button></p>

<script>

$( function() {

$( "#datepicker" ).datepicker({dateFormat: "yy-mm-dd"});

  } );

</script>

<div id="chart">
</div>

</html>
```

**示例代码 16：**`heat.php`—初始页面设置—第 1 部分。

在示例代码 17 中，第 34 行使用 jQuery 选择器来选择`viewChart`按钮。为此按钮附加了一个`click()`事件处理程序。在此点击处理程序内部，启动图表生成过程。在第 35 行，使用 jQuery 选择器来选择`datepicker`输入字段，并使用`val()`函数提取其值。这被放入一个名为`date`的变量中。要使此过程正确工作，用户输入的日期必须与存储在数据库中的时间戳相匹配，这是必不可少的。

在第 36 行，向第二个名为`getData.php`的页面发出单个`GET`请求，以从数据库中检索记录。此页面接受一个名为`selectedDate`的参数，其值设置为用户输入并存储在`date`变量中的值。当第 37 行的`GET`调用完成时，将调用`done()`函数。其结果是一个名为`data`的单一变量，其中包含 HTML 以及每个将要显示的时间段记录。在第 38 行，使用 jQuery 选择器选择`ID`设置为`chart`的`div`标签，将`data`设置到`chart div`标签中。`html()`函数将 HTML 内容作为输入设置到`div`中。在将 HTML 添加到图表之后，它仍然没有正确的颜色编码。为此，启动第二个过程，为每个添加的`div`标签添加额外的 CSS 样式。

每个小时有十二个独立的时间段。为了正确地为这些记录着色，使用了三个变量。第一个变量是第 40 行的`start`，用于存储颜色编码的起始数字；第 41 行的`end`变量存储颜色编码范围的结束值。

一个例子是计数值在 1 到 10 之间的时间段。第一次搜索将查找 0 到 1 之间的记录，例如集合中最低计数。下一次搜索将在 1 到 2 之间，依此类推。这使我们能够以递增的方式处理记录。第 42 行的文本`op`变量用于存储正在处理的`div`的当前不透明度。我们使用的最低值是 0.1，用于表示记录数较少的时间段。

在通过`GET`请求返回 PHP 页面的数据记录中包含 24 个不同的`div`标签，代表一天，每个标签包含 12 个时间段。每个单独的时间段都将 CSS`class`设置为`colorRow`，这使我们能够对整个文档执行筛选，以选择具有此类的所有`div`标签。

对于 1 小时时间块中的每个单独时间段，使用`console.log()`函数添加了一个简单的调试输出。为单个时间段着色的起点从`start`变量设置为 0 开始，因为可能存在记录为零的时间段。`end`位置设置为`step`的值，如前所述，这是集合中记录的最大计数除以 10。`op`设置为 0.1，而`score`（例如，给定时间段内记录的计数数量）从第 48 行的`div`标签属性`score`中提取，该属性在执行`GET`请求生成 HTML 时已添加。

在第 49 行，添加了一个`for`循环来遍历可用范围，例如 0 到 1、1 到 2、2 到 3 等。为了辅助此过程，在第 50 行添加了一个`console.log()`，输出当前正在处理的分数以及此时`start`和`end`变量的值。在第 51 行，在迭代过程中，如果我们发现的分数大于或等于`start`变量，或者小于等于`end`变量，则添加颜色编码。

在第 52 行，添加了一个简单的`console.log()`来将单词`found`输出到控制台以辅助调试。在第 53 和 54 行，对正在处理的`div`标签调用`css()`函数，将颜色更新为`red`，并将`opacity`设置为变量`op`的当前值。在更新`div`之后，调用`break;`以退出`for`循环。

在第 57 和 58 行，如果记录不在第一个`start`和`end`范围内，则将`start`变量更新为`end`的值，并将`end`变量更新为`end+step`。`op`变量也会更新，额外增加 0.1，使得`div`的不透明度随着`for`循环的迭代而变暗。在第 65 行，为了帮助用户分析记录，将 jQueryUI 工具提示添加到整个文档中。

当第 66 行将属性`track`设置为`true`时，工具提示会根据鼠标当前所在位置进行更新。此工具提示从 PHP 生成的单个`div`标签的`title`属性中获取值。

```javascript
<script>

$("#viewChart").click(function() {

    var date = $('#datepicker').val();

    $.get("getData.php", { selectedDate: date })
        .done(function(data) {

        $("#chart").html(data);

        // ------ add color style

        var start = 0;

        var end = 0;

        var score = 0;

        $(".colorRow").filter(function() {

            console.log("processing new record......");

            start = 0;

            end = step;

            op = 0.1;

            var score = $(this).attr("score");

            for(var i=0; i < 10; i++){

                console.log("checking if "+score+" is between" +
                    start + " and " + (end) + " op is..." + op);

                if(score >= start && score <= end ){

                    console.log("found");

                    $(this).css('background-color', 'red');

                    $(this).css("opacity", op);

                    break;

                }

                start = end;

                end = end + step;

                op = op + 0.1;

            }

        }); // end .done()

    }); // end .click()

    $( function() {

        $(document).tooltip({

            track: true

        });

    });

</script>
```

**示例代码 17：**`heat.php`—动态修改单元格颜色—第 2 部分。

### 示例代码：`getData.php`

## 基于时间的反馈分析 ■ 259

为了驱动此图表，创建了一个名为`getData.php`的 PHP 页面。在示例代码 18 中，第 7 行首先建立了与数据库的连接。在第 9 行，创建了一个名为`totalRecords`的变量，用于存储我们在给定时间处理的记录总数。在第 10 行，启动了一个`div`标签，其`style`设置为`overflow: hidden`，这使我们能够将`div`标签并排放置。其`width`设置为`900px`，可以根据所需布局进行更改。

在第 11 行，通过运行从 0 到 24 的`for`循环来启动生成过程的核心。每个数字代表给定日历天中的一天。在循环过程中，第 12 行调用`getBlockForHour()`函数，该函数生成包含 12 个时间段的单个小时（每个时间段 5 分钟）。在此过程中不执行颜色编码，因为这是在客户端完成的。此组件纯粹是为了收集给定日期的记录，并计算一天中每个时间段的总数。在第 16 行，创建了一个名为`step`的 JavaScript 变量，将返回到客户端。其值设置为稍后设置的`max`除以 10，表示将有 10 个颜色范围。在第 17 行，定义了`getBlockForHour()`函数。这负责生成给定日期的 24 小时块。在第 18 行，添加了一个名为`output`的变量。这充当将要返回的所有内容的占位符。

在第 20 行，`output`以单个`class`设置为`oneRow`的`div`标签开始。在`style`属性内部设置为`float:left`，宽度定义为`100px`。这一行将包含一个时间戳，例如 0:00，后面跟着一个彩色条。时间在`span`标签中添加，这使我们能够将`font-size`设置为`11pt`。`span`标签的内容是传递给函数的`hour`变量，后跟`:00`。在第 23 行，创建了`hourStamp`变量。在第 24—28 行，如果我们当前处理的小时小于 10，例如如果小时只有一位数，则在其前面添加 0。在第 30 行，启动了一个`for`循环来获取给定小时的 12 个时间段。每个时间段代表五分钟的时间窗口。

对于每个小时，首先在第 31 行调用`getScore()`函数，该函数将计算给定时间窗口留下的记录总数。此函数被传递`hourStamp`变量，后跟我们正在查看的`minutes`变量。此函数将返回一个整数，如果该时间段未找到记录则为 0，如果找到记录则大于 0。

此结果存储在第 31 行的`score`变量中。在第 32 行，生成时间段 HTML 的主体。一个新的`div`

## 基于 JavaScript 和 PHP 的实际用户数据收集与分析 ■ 260

创建了一个宽度为 500 且`overflow`设置为`hidden`的`div`标签。这允许该`div`标签内的内容向左浮动。在第 33 行，这个`div`内部包含一个 50px 的小`div`，其第 34 行又包含一个`span`标签，该标签的字号设置为 10pt，用于表示将为用户打印的时间。添加`hourStamp`，后跟一个冒号，再后跟分钟戳。然后关闭`span`标签和`div`标签。

之后，在第 36 行，创建了一个新的`div`，其`class`设置为`colorRow`。这是用户将看到的代表时间段的主要颜色编码条。`div`标签的`title`属性被设置为返回的分数。这个`title`属性被 jQueryUI 工具提示使用，以便在鼠标悬停时获取给定时间段的分数。`score`属性被设置为返回的分数。这个`score`属性在客户端进行颜色编码处理时使用。在第 39 行，`minutes`变量增加五分钟，以便在`for`循环再次迭代之前进入下一个时间段。在第 40 行，如果`minutes`变量小于 10，则在变量开头添加一个单独的 0，以改善时间戳的外观。在添加完所有 24 个小时后，每个小时包含 12 个五分钟的时间窗口，然后一个最终的关闭`div`标签被追加到`output`变量。`output`变量在第 45 行返回。

```php
1 <?php

2 try {

3     $host = 'localhost:3306';

4     $dbname = 'bookexamples';

5     $user = 'sampleuser';

6     $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

7     $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,

8         $pass);

9 } catch(PDOException $e) {echo $e;}
```



```php
$totalRecords = 0;

echo '<div style="overflow: hidden; width:900px">';

for($h=0; $h<24; $h++){
    echo getBlockForhour($h);
}

echo '</div>';

// 在生成图表之前更新 `step` 变量
echo '<script> step = ' . ($max / 10) .'; </script>';

function getBlockForhour($hour){
    $output = '';
    $minutes = '00';

    $output .='<div class="oneRow" style="float:left; width:100px">';

    $output .= '<span style="font-size:11pt;">' . $hour . ':00</span>';

    $hourStamp = '';

    if($hour < 10){
        $hourStamp = '0' . $hour ;
    } else{
        $hourStamp = $hour;
    }

    for($i=1; $i<13; $i++){
        $score = getScore($hourStamp, $minutes);
        $output .= '<div style="width:300px; overflow: hidden;">'
                <div style="width:40px; float: left">
                <span style="font-size:10pt"> '. $hourStamp.':'
        . $minutes . ' </span>
                </div>
                <div class="colorRow" id="colorRow"
        title="'.$score.' Feedback records" score="'.$score.'">
                </div>
                </div>';
        $minutes += 5;

        if($minutes < 10){
            $minutes = '0' . $minutes;
        }
    }

    $output .= '</div>';
    return $output;
}
```

示例代码 18：`getData.php` — 生成一小时的 HTML 块 — 第 1 部分。

为了计算给定时间段的分数，使用了`getScore()`函数，如示例代码 19 所示。此函数接受两个参数：`hourStamp`，后跟`minuteStamp`。在第 48 行，引用了`max`和`min`变量，因为它们在分数收集过程中可能会改变。在第 49 行，提供的`endTime`被设置为当前分钟戳 + 4 分钟，创建一个 5 分钟的时间窗口。例如，对于时间戳 17:30，我们感兴趣检索记录的时间段是在 17:30 到 17:35 之间。在第 50 行，感兴趣的日期存储在一个局部变量中。SQL 查询在第 51 行定义。在此查询中，使用`SELECT`语句计算所有`score`记录并将其作为`score`处理。这消除了处理名为`count(score)`的列的需要。选择了`feedbackheat`表，并添加了一个`WHERE`子句，声明感兴趣的记录在 ? 和 ? 之间，这些是当前感兴趣`start`和`end`时间戳的未命名占位符。

在第 52-54 行，创建了`stDate`和`finish`变量。`stDate`是用户输入的当前日历日期，后跟一个空格，后跟小时戳、冒号、分钟戳、冒号和 00 秒。这是为了匹配数据库中存储记录的格式。`finish`时间戳是当前日历日期后跟相同的`hourStamp`，后跟一个冒号，后跟`endTime`变量，后跟一个冒号和 59 秒。如前所述，我们将分钟变量增加 4 分钟，秒数用于标识我们想要从 0:00 到 4:59 秒之间的所有记录。

为了收集结果，在第 57 行调用了`fetch()`函数。结果存储在`res`变量中。在第 58 和 59 行，引用了`totalRecords`，因为它存储了找到的记录总数的引用。此变量被更新以包含`res[0]`，其中包含当前时间段中的记录总数。

在第 62-67 行，引用了`max`和`min`变量。如果返回的结果大于`max`，则存储新的分数。如果结果小于当前的`min`，则也存储它。在此过程结束时，最终的`result`变量将返回给调用`getScore()`函数的调用者，如前所述。

```php
function getScore($hourStamp, $minuteStamp){
    global $DBH, $max, $min;

    $endTime = $minuteStamp+4;
    $date = $_GET['selectedDate'];

    $sql = "SELECT COUNT(score) AS score  FROM feedbackheat
           WHERE TIMESTAMP BETWEEN ? AND ?";

    $stDate = $date . " " . "$hourStamp:$minuteStamp:00";
    $finish = "$date $hourStamp:$endTime" . ":59";
    $params = array($stDate, $finish);

    $sth = $DBH->prepare($sql);
    $sth->execute($params);

    $res = $sth->fetch();

    global $totalRecords;
    $totalRecords = $totalRecords + $res[0];

    $result = $res[0];

    global $max, $min;

    if($result > $max){
        $max = $result;
    }

    if($result < $min){
        $min = $result;
    }

    return $result;
}
?>
```

示例代码 19：`getData.php` — 查找分数 — 第 2 部分。

### 输出

图 7.8 显示了日期输入框被点击且 jQueryUI 日期选择器变得可见的示例。选择日期后，必须点击*查看图表*按钮。

# 反馈热力图

![](img/ed4cb7e1be98f0adec0546edd14f6223_287_0.png)

图 7.8：使用 jQueryUI 日期选择器选择日历日期。

图 7.9 显示了最终生成的图表。对于一天中从 0:00 到 23:59 的每个小时，都显示了五分钟的时间窗口。对于每个五分钟的时间窗口，颜色*红色*的*透明度*根据已添加的记录数量而变浅或变深。这提供了一种查看给定一天中最受欢迎反馈时间的简单方法。

## 264 ■ 使用 JavaScript 和 PHP 进行实际用户数据收集与分析

# 反馈热力图

日期：2019-09-02 [查看图表]

![](img/ed4cb7e1be98f0adec0546edd14f6223_288_0.png)

图 7.9：显示单日 24 小时的热力图。

图 7.10 显示了当光标放在单个时间段上时显示的工具提示。该时间段的值从时间段`div`标签的`score`属性中提取。

![](img/ed4cb7e1be98f0adec0546edd14f6223_289_0.png)

图 7.10：显示给定时间段反馈记录数量的工具提示。

## 7.7 总结

本章描述了处理数据的时间维度。首先，描述了一种时间分段分析方法。这种方法允许用户选择他们感兴趣的特定时间段来绘制较小数量的数据。然后描述了实时反馈分析领域，因为反馈发生时通常需要进行监控。此方法侧重于在图表上绘制正面和负面反馈。

为了提供更全面的数据视图，描述了一种正面与负面反馈日历方法。该方法绘制了整年的正面反馈和负面反馈。每个都给出了自己的图表，使用颜色编码概述了每天收到的记录数量。最后，描述了一个 24 小时自定义热力图，它将一整天分解为更小的小时，然后进一步分解为五分钟的时间槽。这种方法允许分析师查看一天中反馈记录留下的趋势时间。

第 8 章概述了可以从数字和基于文本的数据中收集的统计数据。

# Taylor & Francis

Taylor & Francis Group

`http://taylorandfrancis.com`

# 第 8 章

## 反馈统计与概览

## 8.1 引言

在处理大规模数据集合时，统计分析在理解数据方面起着至关重要的作用，并能提供否则可能会被忽视的关键洞察。

本章描述了可应用于大型数据集的各种任务，以便为数据分析师提供一目了然的洞察。其中许多方法可以与图表集成，以进一步协助呈现统计信息，从而实现快速高效的分析。

## 8.2 基础统计

要处理基础统计，将使用一个名为`statistics`的数据库表。对于`score1`、`score2`和`score3`列，可以输入 1 到 5 之间的值。

**示例代码**：`create.sql`

该表包含一个唯一的`ID`列、三个独立的分数字段，以及一个`mytime`字段，该字段在记录创建时自动设置为当前时间。

```sql
CREATE TABLE `statistics` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `score1` TINYINT,
    `score2` TINYINT,
    `score3` TINYINT,
    `mytime` DATETIME NULL DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (`id`)
)
```

### 示例 1：计算众数

在处理大量反馈记录时，我们通常希望看到出现频率最高的反馈分数是多少。这被称为*众数*。众数的一个简单示例如示例代码 1 中的 10 个反馈分数所示。

1, 2, 2, 5, 6, 7, 7, 7, 7, 10

**示例代码 1：用于众数计算的示例值。**

由此可以看出，用户输入的最频繁的反馈分数是 7。对于这个数据集，*众数*定义为 7。

### 示例代码：`getMode.php`

要获取更大数据集（例如 1000 条记录）的众数，将创建一个新的 PHP 页面，名为`getMode.php`。在示例代码 2 中，该文件顶部的第 7 行建立了与数据库的连接。第 9 行创建了一个名为`getMode()`的新 PHP 函数。第 10 行引用了数据库连接。虽然可以使用 PHP 计算众数，但为了减轻 PHP 服务器的负担，此计算交由数据库完成。第 11 行添加了用于计算众数的 SQL 查询。首先选择`score1`列，然后是`score1`列的*计数*。这被表示为`scoreCount`变量以供后续参考。

对`score1`列执行`GROUP BY`以将所有相似的值分组。添加了`ORDER BY`按`scoreCount`列对结果排序，因为这将使出现次数最多的分数成为结果集中的第一条记录。由于我们只关心众数，而不关心其他记录，因此在末尾附加了`LIMIT 1`以仅返回单条记录。

在第 12 和 13 行，运行了`prepare()`和`execute()`函数。由于只需要一条记录，可以在第 14 行执行一次对`fetch()`函数的调用。此次调用的结果作为数组放入`res`变量中。数组的第 0 位包含众数，第 1 位包含`score1`的计数。第 17 行执行了一个简单的`return`以将这些值返回给调用者。

在第 19 行，使用简单的`echo`输出文本，然后调用`getMode()`函数以获取值。

```php
<?php

try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DACO';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
} catch(PDOException $e) {
    echo $e;
}

function getMode(){
    global $DBH;

    $sql = 'SELECT score1, COUNT(score1) AS scoreCount FROM
        statistics GROUP BY score1 ORDER BY scoreCount DESC
        LIMIT 1';

    $sth = $DBH->prepare($sql);
    $sth->execute();

    $res = $sth->fetch();
    $mode = $res[0];
    $count = $res[1];

    return $mode . ' with count ' . $count;
}

echo 'The mode is: ' . getMode();
```

**示例代码 2：`getMode.php` — 返回众数。**

### 输出

图 8.1 展示了包含两列的最终结果，一列是众数（例如 9），另一列显示所选分数的计数（例如 116）。

```text
The mode is: 9 with count 116
```

**图 8.1：显示众数及其记录总数的输出结果。**

### 示例 2：计算平均值/均值

给定列的平均分数可以通过调用 SQL `AVG()`函数轻松找到，该函数接受单个列名作为参数。与前面的示例一样，数据库负责处理，从而减轻了 Web 服务器的负担。

### 示例代码：`getAverage.php`

在示例代码 3 中，第 7 行首先建立了与数据库的连接。第 9 行定义了`getAverageScore()`函数。该函数接受一个参数，即我们希望计算平均值的列的名称。第 11 行定义了 SQL。调用了 SQL `avg()`函数并传入了`column`参数。为了从结果列标题中移除`avg()`文本，该列被表示为`average`。

在第 12 和 13 行，调用了`prepare()`和`execute()`函数。第 14 行，由于只会返回一个变量，可以使用`fetch()`函数。第 15 行，这被放入一个名为`avg`的局部变量中，并在第 16 行返回给函数调用者。要调用此函数，在第 18 行使用 echo 语句打印一小段前导文本，然后调用`getAverageScore()`函数，该函数接受感兴趣的列的名称。

```php
<?php

try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
} catch(PDOException $e) {
    echo $e;
}

function getAverageScore($columnName){
    global $DBH;

    $sql = "SELECT AVG($columnName) AS average FROM statistics";

    $sth = $DBH->prepare($sql);
    $sth->execute();

    $res = $sth->fetch();
    $avg= $res[0];

    return $avg;
}

echo 'The averages for score1 is ' . getAverageScore('score1');
```




## 示例代码 3：`getAvg.php` — 计算列的平均值

### 输出

调用此函数计算给定列的结果如图 8.2 所示。

**`score1` 的平均值是 5.4410**

**图 8.2：给定列的平均值结果。**

## 示例 3：计算标准差

在审查反馈记录集合时，一个易于推导的有用统计量是标准差，通常表示为 $\sigma$（西格玛）。标准差是一种用于识别给定数值与均值之间距离的方法。例如反馈分数 1、2、2 和 5。观察这四个数字，我们可以轻易看出数字 2 出现了两次。这组数据的均值是 2.5。其计算如公式 8.1 所示，将四个数字相加后除以四。

$$
\frac{1 + 2 + 2 + 5}{4} = 2.5 \quad (8.1)
$$

观察最后一个反馈分数 5，我们可以看出它远高于其他反馈分数。标准差有助于识别我们所关注的分数与均值的距离。如果我们单独看反馈分数 5，在 1 到 5 的评分尺度上它似乎是正面的。然而，当同时查看标准差时，它会告诉我们 5 实际上与分数的真实代表相距甚远。

对于每个单独的分数，我们用该值减去均值并对结果求平方。每个结果相加后除以数据集中的分数数量，如公式 8.2 所示。

$$
\frac{(1-2.5)^2+(2-2.5)^2+(2-2.5)^2+(5-2.5)^2}{4-1} = \frac{9}{4} \quad (8.2)
$$

然后我们得到 2.25，如公式 8.3 所示。

$$
\frac{9}{3} = 2.25 \quad (8.3)
$$

最后，求得 2.25 的平方根，如公式 8.4 所示。

### 示例代码：`create.sql`

此示例使用一个名为 `smallset` 的简单数据库表。该表包含一个自增的 `ID` 列，以及一个 `score` 列，用于存储 1 到 5 之间的样本分数值。

```sql
CREATE TABLE `smallset` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `score` INT,
    PRIMARY KEY (`id`)
)
```

最终结果为 1.5，定义为该组分数的总标准差。

$$
\sqrt{2.25} = 1.5 \quad (8.4)
$$

本示例包含两个文件：

1. `create.sql` — 该文件用于创建 `smallset` 数据库表。
2. `getStdDev.php` — 该文件从数据库中检索标准差。

### 示例代码：`getStdDev.php`

使用 MySQL 数据库时，可以轻松使用 `std()` 函数计算标准差。该函数接收一个参数，即我们希望计算其标准差的列名。

在示例代码 4 中，第 7 行创建了一个新的数据库连接。第 9 行定义了 `calculateStdDev()` 函数。在该函数内部，第 11 行添加了 SQL 语句。在 `SELECT` 之后添加了名为 `std()` 的函数，并传入目标列的名称。第 14 行，由于只会返回单条记录，因此调用了数据库的 `fetch()` 方法。此调用的结果被放入 `res` 变量中。提取位置 0 的 `res` 值，并将其放入名为 `stdev` 的局部变量中，该变量在第 16 行返回给函数调用者。

第 18 行使用简单的 `echo` 输出前导文本，然后调用 `calculateStdDev()` 函数。

```php
<?php 

try {
    $host = 'localhost:3306';
    $dbname = 'bookexamples';
    $user = 'sampleuser';
    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user, $pass);
} catch(PDOException $e) {
    echo $e;
}

function calculateStdDev() {
    global $DBH;

    $sql = 'SELECT STD(score) AS sd FROM smallset;';
    $sth = $DBH->prepare($sql);
    $sth->execute();

    $res = $sth->fetch();
    $stdev = $res[0];

    return $stdev;
}

echo 'The standard deviation is ' . calculateStdDev();
```

**示例代码 4：`getStdDev.php` — 计算标准差。**

### 输出

图 8.3 展示了 SQL 查询的结果，将标准差打印到浏览器中。

```text
The standard deviation is 1.5000
```

**图 8.3：示例标准差结果。**

## 8.3 使用样本

反馈记录集合越大，从中获取洞察的过程就越困难。在我们之前描述的每个示例中，我们处理的都是相对较小的样本，例如 100 条记录。当处理超过此规模的数据集时，就无法再快速浏览反馈的整体趋势。抽样是使用一个较小的、但能准确代表整体数据集的数据子集的过程。在本节中，我们将回顾常见的抽样方法。

例如，有一个包含 50,000 条反馈记录的集合。数据中可能存在某种模式，例如有 20,000 条记录的反馈分数低于 10 分制中的 5 分。与其处理全部 50,000 条记录来识别这一点，如果使用正确的抽样方法，我们可以用更少的记录找到大致相同的答案。

这种方法减轻了应用程序在信息检索和处理方面的需求压力。收集的总样本量不需要有固定值，但结果的准确性将帮助确定一个合适的值。

*简单随机抽样*是一种非常简单的收集样本的方法。在此方法中，对于包含 1000 条记录的样本集，随机抽取 `n` 个样本，例如 100 条记录。在这种方法下，任何记录被选中并包含在抽取的样本集中的机会是均等的。

*分层抽样*是一种首先将记录集合（例如 1000 条单独的反馈记录）按特征（如记录采集日期）进行划分的方法。第一个*层*将包含 `N` 条记录，第二个*层*也将包含 `N` 条记录。这种方法会继续将集合划分为更小的子集。然后从这些子集中，执行简单随机抽样以从每个子集中收集 `N` 条反馈记录。这种方法很有用，因为它提供了一种逻辑方式来分离每个反馈集合，并确保每个集合（在本例中，即一周中的每一天）在最终样本集中得到准确代表。

*系统抽样*是一种抽样方法，它不随机选择反馈分数用于样本，而是采取一种更系统化的方法。在一个包含 100 条单独反馈记录的集合中，使用一个名为 `K` 的变量，其值设为 1。由于 `K=1`，数据集中的第一条记录被添加到样本中。此后，变量递增，将五加到变量 `K` 上，此时 `K` 等于 6。递增之后，数据集中的第 6 行记录被添加到样本中。

这种方法的缺点是，如果数据集使用了某种排序，例如 70/100 条记录是在周一添加的，30/100 条记录是在周二添加的，那么很容易看出样本集会对周一产生偏向，因为它包含了更大比例的记录。

## 8.4 百分比差异

从数据集合中获取概览是了解用户的重要一步。百分比通常被用作一种向用户传递信息的简单方式，而用户几乎不需要付出额外的努力。像 25% 这样的统计数据可以轻松传达，无论使用的是何种样本量或有多少反馈记录可用。在本节中，我们将回顾如何计算两个日历日期之间的百分比差异。

### 示例 4：计算百分比差异

此示例包含三个文件和三个库：

1. `create.sql` — 包含名为 `diffcalc` 的示例表的创建代码。
2. `diff.php` — 提供给用户的主要用户界面。
3. `getDiff.php` — 该文件收集记录并计算差异。
4. `jQuery` — 引入此库以执行 JavaScript `GET` 请求。
5. `jQueryUI` — 此文件为用户提供交互式的日期选择器以选择日期。
6. `popper.js` — 为 Bootstrap 提供定位引擎。

要计算两个分数之间的百分比差异，可以使用公式 8.5。其中 $V_1$ 是第一个值，$V_2$ 是第二个值。

$$
\frac{|V_1 - V_2|}{[\frac{V_1+V_2}{2}]} \times 100
$$

示例代码 `create.sql`（示例代码 5）展示了一个简单的数据库表，用于存储反馈分数以及反馈提交的日期。该表包含一个唯一的 `ID` 列、三个 `score` 字段和一个 `datestamp`。

## 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

```sql
CREATE TABLE `diffcalc` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `score1` TINYINT,
    `score2` TINYINT,
    `score3` TINYINT,
    `datestamp` DATE,
    PRIMARY KEY (`id`)
);
```

**示例代码 5：示例 `diffcalc` 表。**

### 示例代码：`diff.php`

创建一个名为 `diff.php` 的新页面。在示例代码 6 中，第 3 行首先引用了 jQuery 内容分发网络（CDN）。接着在第 4 行引用 jQueryUI JavaScript 文件，第 5 行引用关联的 CSS 文件。jQueryUI 将用于创建交互式日期选择器。表格的样式将使用 Bootstrap。Bootstrap 的依赖项包括 `popper.js`，它在第 8 行被引入。在第 10-13 行，包含了 Bootstrap.js 并引用了 Bootstrap CSS 文件。第 15 行对 `thead tr` 标签进行了一些小的 CSS 修改。这将把第一行的背景设置为黑色，文字设置为白色。

第 22 行添加了一个 `div` 标签，其 `class` 设置为 `container`。这是用于容纳我们表格的容器。添加了参数 `sm` 以标识我们需要一个小尺寸的容器。在此容器内，第 23 行添加了一个输入框，其 `ID` 设置为 `datepicker`。紧接其下，第 24 行添加了一个单独的 `button`，其 `ID` 设置为 `viewData`。这是负责生成表格的主要按钮。

为辅助布局，第 25 行添加了一个 HTML `table`，其 `class` 设置为 `table table-striped`。这将使表格中的奇偶行具有不同的阴影效果。在内部，第 27 行添加了一个表格 `row`，包含四列。第一列是日期，接着是记录计数，然后是该列添加的所有反馈记录的分数总和，以及百分比差异。第 34 行创建了一个名为 `tbody` 的新标签，其 `ID` 设置为 `content`。这是用于存放选定日期并点击 `viewData` 按钮后生成的 HTML 的主要占位符。

## 反馈统计与概览

在第 40 行，为了触发内容生成过程，使用了 jQuery 选择器为 `viewData` 按钮附加一个 `click()` 处理程序。当按钮被点击时，jQuery 的点击处理程序将被触发。其中，在第 41 行，使用 jQuery 选择器选中了存放日期的 `datepicker input` 字段。`val()` 函数被用于提取该值并将其放入一个名为 `dateSelected` 的临时变量中。

在我们获取到所选日期后，第 42 行执行了一个 jQuery `GET` 请求到负责生成内容的 `getDiff.php` 页面。传递了一个名为 `date` 的参数，其值被设置为 `dateSelected` 变量。当请求完成后，在第 43 行调用了 `done()` 函数。第 44 行，使用 jQuery 选择器选中 `content div` 标签，并使用 `html('')` 函数（不带任何额外参数）将其内容设置为空。如果不执行此步骤，后续对 `getDiff.php` 页面的请求将会把内容追加到当前表格中。

在第 45 行，调用了 `append()` 函数，该函数接收一个参数 `data`，其中包含了从 `getDiff.php` 页面接收到的完整 HTML。

在 `diff.php` 页面的末尾，第 49 行，使用 jQuery 选择器选中 `datepicker input` 字段，并将其转换为 jQueryUI 的交互式日期选择器。`dateFormat` 参数以 `yy-mm-dd` 的形式传递给 `datepicker()` 函数。这将把用户选择的日期格式化为类似 `2020-09-01` 的形式。

```html
<html>
<head>
<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="http://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" type="text/css"
  href="http://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<script
  src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
<link rel="stylesheet"
  href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
<script
  src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
```

使用 JavaScript 和 PHP 进行应用用户数据收集与分析

```html
<style>
thead tr {
    background-color: #000000;
    color: #FFFFFF;
}
</style>
</head>

<body>
<div class="container sm">
<p>查看起始周：<input type="text" id="datepicker">
<button id="viewData">查看数据</button></p>

<table class="table table-striped">
    <thead style="">
        <tr>
            <th scope="col">日期</th>
            <th scope="col">记录数</th>
            <th scope="col">分数总和</th>
            <th scope="col">百分比差异</th>
        </tr>
    </thead>
    <tbody id="content">
    </tbody>
</table>
</div>
</body>

<script>
$( "#viewData" ).click(function() {
    var dateSelected = $( "#datepicker" ).val();

    $.get( "getDiff.php", { date: dateSelected} )
        .done(function( data ) {
            $( "#content" ).html('');
            $( "#content" ).append(data);
        });
})

$( function() {
    $( "#datepicker" ).datepicker({dateFormat: "yy-mm-dd"});
} );
</script>
```




## 示例代码 6：`diff.php` —— 允许用户选择一周的主用户界面

### 示例代码：`getDiff.php`

创建了一个名为`getDiff.php`的页面。此页面是数据检索和计算过程的核心。在示例代码 7 中，第 2 行检索了一个名为`date`的`GET`变量。这个日期是用户在上一页通过 jQuery `GET`操作选择并传递给页面的。该日期存储在一个名为`startDate`的变量中。这将用作所有后续计算的起始点。对于任何给定的日期，该算法将查看起始日期与接下来的七个日历日之间的差异。如果日期跨越到下一个月，月份将自动调整。在获取日期后，第 8 行建立了到数据库的连接。

在第 10 行，创建了核心的`calculateDiffFromDate()`函数，它接收一个名为`basedate`的参数，函数将基于此参数进行操作。

函数内部，第 12 行创建了一个名为`output`的变量。这将用作所有生成的 HTML 的主要占位符。第 14 行，调用了`getDateRecords()`函数，并将当前关注的日期`baseDate`传递给它。

调用`getDateRecords()`函数的结果是三个值：`count`、`sum`和`difference`。每个值之间用冒号分隔。第 15 行，调用`explode()`函数，将`resBase`变量基于冒号分割成数组格式，以便提取这三个值。

在第 16–22 行，`output`变量被追加内容，以包含第一个 HTML 行。此行将包含`baseDate`，后跟字符串`Start`，用作视觉指示，告诉用户这是所有其他统计信息将由此衍生出的日期。记录数通过调用`r[0]`添加，总和通过调用`r[1]`添加。第 23 行，为了计算初始日历日之后每一天的差异，首先调用`strtotime()`函数将日历日期转换为可访问的格式。第 24 行的`for`循环用于遍历这七天。

为了找到下一个日历日期，第 25 行调用`date()`函数，将日期格式化为`Y-m-d`格式。调用了`strtotime()`函数，允许我们传入想要从原始日期戳偏移的天数。此循环第一次运行时，原始日历日期将偏移 +1 天，然后是 +2 天，依此类推。找到下一个日历日期后，第 26 行调用了`getDataRecords()`函数，该函数负责从数据库中收集记录。如果没有可用数据，此函数将返回 0。

如果该日期有可用数据，第 28 和 29 行分别对`resBase`变量和`res2`变量调用`explode()`函数，并将结果放入相应的局部变量中，例如，n1 代表第一天，n2 代表第二天。每个变量都包含三个由冒号分隔的数据项。

280 ■ 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

这三个数据项包括记录总数、反馈总和以及日历日期，例如，100:301:2020-09-02。对于 n1 和 n2 数组，在第 30–35 行，每个值都被提取并放入局部变量中。

第 36 行，计算过程可以开始。通过将 count1 除以 sum1（记录的总和）来计算，得到 v1。重复相同的过程得到 v2 的值。该公式在第 38 行分解为分子，第 39 行分解为分母。

第 40 行，通过将分子结果除以分母来计算最终结果。此结果乘以 100 得到百分比差异。第 41 行调用`round()`函数将结果四舍五入到 2 位小数。在第 43–45 行，如果数据库中给定日期没有记录，则将 count、sum 和 diff 变量设置为 0。第 47 行，将输出追加内容，包含这三个变量的值作为新的表格行。第 55 行，将输出打印到屏幕以返回给客户端。

```php
<?php

$startDate = $_GET['date'];

try {

    $host = 'localhost:3306';

    $dbname = 'bookexamples';

    $user = 'sampleuser';

    $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

    $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,

      $pass);

} catch(PDOException $e) {echo $e;}

function calculateDiffFromDate($baseDate){

    global $DBH;

    $output = '';

    // 获取起始记录的数据

    $resBase = getDateRecords($baseDate);

    $r = explode(':', $resBase);

    $output .= '

    <tr>

        <th scope="row"> '.$baseDate.' [起始]</th>

        <td>'.$r[0].'</td>

        <td>'.$r[1].'</td>

        <td>0</td>

    </tr>';
```

```php
23  $timestamp = strtotime($baseDate);

24  for($d = 1; $d < 8; $d++){

25      $nextDate =  date('Y-m-d', strtotime('+'.$d.' day',

26          $timestamp));

27      $res2 = getDateRecords($nextDate);

28      if($res2 != 0){

29          $r1 = explode(':', $resBase);

30          $r2 = explode(':', $res2);

31          $count1 = $r1[0];

32          $sum1 = $r1[1];

33          $viewingDate1 = $r1[2];

34          $count2 = $r2[0];

35          $sum2 = $r2[1];

36          $viewingDate2 = $r2[2];

37          $v1 = $count1 / $sum1;

38          $v2 = $count2 / $sum2;

39          $top = $v1 - $v2;

40          $bottom = ($v1 + $v2) / 2;

41          $re = ($top / $bottom) * 100;

42          $diff = round($re,2);

43      } else {

44          $count2 = 0;

45          $sum2 = 0;

46          $diff = 0;

47      }

48      $output .= '

49          <tr>

50              <th scope="row">'.$nextDate.'</th>

51              <td>'.$count2.'</td>

52              <td>'.$sum2.'</td>

53              <td>'.$diff.'%</td>

54          </tr>';

55  }

56  echo $output;
```

示例代码 7：`getDiff.php` — 第一部分。

从数据库检索记录的流程是通过调用`getDateRecords()`函数来完成的，该函数接收一个单历日期。在示例代码 8 的第 57 行定义了此函数。

在第 59 行，向`count()`函数发出 SQL 查询以计算记录数量。此结果在结果集中表示为`count`。找到标题为`score1`的列中所有记录的总和，并在最终结果中表示为`sum`。还包含`timestamp`以辅助追踪数据来源。使用简单的`WHERE`子句根据感兴趣的日期缩小结果集范围。使用问号作为日期的占位符。

在第 60 行，创建了一个名为`params`的新数组，将`date`变量作为输入。在第 62 行，调用`execute()`函数。在第 64–66 行，将`count`、`sum`和`date`放置在局部变量中。如果在第 67 行没有返回记录，则返回 0 给函数调用者。如果有记录，则将`count`、`sum`和`date`用冒号（`:`）连接在一起。在第 73 行，调用`calculateDiffFromDate()`函数并传入起始日期。这是为了触发检索流程。

```php
57  function getDateRecords($date){

58      global $DBH;

59      $sql = "SELECT COUNT(score1) AS COUNT, SUM(score1) AS SUM, datestamp FROM diffcalc WHERE datestamp = ?";

60      $params = array($date);

61      $sth = $DBH->prepare($sql);

62      $sth->execute($params);

63      $res = $sth->fetch();

64      $count= $res[0];

65      $sum = $res[1];

66      $date = $res[2];

67      if($count == '0'){

68          return 0;

69      } else {

70          return $count . ':' . $sum . ':' . $date;

71      }

72  }

73  calculateDiffFromDate($startDate);

74

75  ?>
```

示例代码 8：`getDiff.php` — 第二部分。

### 输出

[图 8.4](#) 显示了在日历中选择一天并点击`View Data`按钮后的结果。表格中的所有内容由`getDiff.php`页面动态生成，并通过 jQuery `GET`请求进行调用。

![](img/ed4cb7e1be98f0adec0546edd14f6223_307_0.png)

## 8.5 总结

随着数据集合规模的扩大，手动分析变得困难。本章概述了可用于分析大型数据集合的常见统计方法。由于许多统计方法可以通过使用 PHP 或现有的数据库函数来实现，因此我们探索了这两种选项。

下一章[第 9 章](#)概述了为数据集合和分析流程开发专用托管解决方案的过程。重点放在数据分析的报告组件以及将发现分发给项目的主要利益相关者上。

![](img/ed4cb7e1be98f0adec0546edd14f6223_308_0.png)

泰勒&法朗西斯

泰勒&法朗西斯集团

`http://taylorandfrancis.com`

# 第 9 章：托管、报告与分发

## 9.1 简介

及时采取行动以获取数据是满足客户需求的关键。在本章中，描述了生成和分发报告的不同方法。描述了报告生成过程的内容和频率，概述了调度、自动报告创建和交付的核心组件。

此外，本章还探讨了亚马逊云平台作为托管前几章中讨论解决方案的一种方法。

## 9.2 报告生成

任何分析的关键组成部分都是生成可由不同数量的人员访问的输出。虽然一些用户可能能够登录 Web 应用程序并查看生成的图表和统计数据，但并非所有用户都是如此。拥有一份格式简单的文档（如 PDF），可以轻松分发给同事，这仍然是普遍的做法。在本章中，我们将查看基于任何给定内容生成 PDF 文件的过程。所有用于生成 PDF 文件的功能都在服务器端使用 PHP 执行。

有许多不同的 PDF 生成库可用于 PHP，但其中一种工具 TCPDF 已经经受了时间的考验。TCPDF 可从 `https://tcpdf.org` 获取。TCPDF 允许您基于 HTML/CSS 生成 PDF，并还具有包含图形的能力。这使我们能够快速将任何现有的可视化和统计信息转换为基于 PDF 的格式。

### 示例 1：生成 PDF

本示例由三个文件和一个库组成：

1. `create.sql` — 包含创建`smallset`和`statistics`表所需的 SQL。
2. `custom.php` — 这是生成 PDF 文件的主代码。
3. `figure1.png` — 这是将包含在 PDF 中的示例图形。
4. `TCPDF` — 此库用于生成 PDF。

### 示例代码：`create.sql`

首先创建`smallset`表。该表包含一个`ID`列和一个用于存储各种分数的`score`列。然后创建`statistics`表，该表包含一个`ID`列和三个`score`列。

```sql
CREATE TABLE `smallset` (

    `id` INT NOT NULL AUTO_INCREMENT,

    `score` INT,

    PRIMARY KEY (`id`)

);

CREATE TABLE `statistics` (

    `id` INT NOT NULL AUTO_INCREMENT,

    `score1` TINYINT,

    `score2` TINYINT,

    `score3` TINYINT,

    `mytime` DATETIME NULL DEFAULT CURRENT_TIMESTAMP,

    PRIMARY KEY (`id`)

);
```

示例代码 1：`create.sql` — 用于创建`smallset`和`statistics`数据库表的 SQL。

### 示例代码：`TCPDF`

要使用 TCPDF，必须先从官方存储库下载。¹ 您将有一个选项，将存储库的内容下载为单个 zip 文件。下载此 zip 文件后，将`TCPDF-master`文件夹的内容解压到您本地 Web 服务器的`htdocs`文件夹根目录。默认情况下，要使`examples`文件夹中的示例运行无需额外配置。

### 示例代码：`custom.php`

此页面由两个核心组件组成：第一个是用于从前一章收集统计信息并将其用于 PDF 的函数。第二个专注于将添加到 PDF 的总体布局和内容。在示例代码 2 中，第 1–39 行可以看到 PHP 函数用于计算众数、平均值和标准差，如第 8 章所述。每次调用函数时，每个函数将返回一个单一值。

```php
1 <?php

2 try {

3   $host = 'localhost:3306';

4   $dbname = 'bookexamples';

5   $user = 'sampleuser';

6   $pass = '3C9038A509BE6145AAD6827B4568AD918BC3DAC0';

7 

8   $DBH = new PDO("mysql:host=$host;dbname=$dbname", $user,

9   → $pass);

10 } catch(PDOException $e) {echo $e;}

11 function getMode(){

12   global $DBH;

13   $sql = 'SELECT score1, COUNT(score1) AS COUNT FROM

14   → statistics GROUP BY score1 ORDER BY count DESC LIMIT 1';

15   $sth = $DBH->prepare($sql);

16   $sth->execute();

17   $res = $sth->fetch();

18   $mode=$res[0];

19   $count = $res[1];

20   return $mode . ' with count ' . $count;

21 }
```

¹ `https://github.com/tecnickcom/tcpdf`

## 使用 JavaScript 和 PHP 进行应用型用户数据收集与分析

```php
function getAverageScore($columnName){

    global $DBH;

    $sql = "SELECT AVG($columnName) AS average FROM statistics";

    $sth = $DBH->prepare($sql);

    $params = array($columnName);

    $sth->execute($params);

    $res = $sth->fetch();

    $avg= $res[0];

    return $avg;

}

function calculateStdDev(){

    global $DBH;

    $sql = 'SELECT STD(score) AS sd FROM smallset;';

    $sth = $DBH->prepare($sql);

    $sth->execute();

    $res = $sth->fetch();

    $stdev=$res[0];

    return $stdev;

}
```




## 示例代码 2：`custom.php` — 收集统计数据 — 第 1 部分

在示例代码 3 中，第 41 行调用并包含了`tcpdf_include.php`页面，用于在我们的项目中引入 TCPDF 库。第 43 行创建了一个新的 PDF 对象。`PDF_PAGE_ORIENTATION` 的值设置为`P`，表示我们使用纵向模式。`PDF_UNIT` 的默认度量单位是毫米。`PDF_PAGE_FORMAT` 默认设置为 A4。然后设置页面的编码为 UTF-8。在第 45–49 行，基本的作者和标题信息被设置到 PDF 中。第 51 行设置了等宽字体。

第 53 行设置了 PDF 文件的边距。这些当前设置为默认值，但可以手动更改。第 54 行设置了 PDF 的基本页眉信息。`PDF_HEADER_LOGO` 包含对 TCPDF 徽标的引用。随后是`PDF_HEADER_LOGO_WIDTH`，指示徽标的宽度。接着是两个可以修改的字符串。为了添加颜色，添加了两个包含 RGB 值的数组。

第 55 和 56 行设置了页眉和页脚的边距。第 58 行将 PDF 设置为自动分页。第 60 行设置了默认的`PDF_IMAGE_SCALE_RATIO`，即 1.25。第 62 到 67 行设置了默认字体。

PDF 生成过程的核心从第 69 行开始，此时调用`AddPage()`函数。这是我们将要添加内容的空白画布。在第 71–73 行，调用之前创建的函数。每个函数返回的结果被放入局部变量中。第 77–83 行添加了一个名为`HTML`的新变量。不是直接将字符串添加到变量中，而是添加了`EOD`标签，允许输入任何文本。在打印之前，空格将被移除。我们收集的三个变量被放入此块中，并附带一些额外的文本。最后，添加另一个`EOD`标签。可以将 HTML 添加到此标签中，而不会引起引号相关的问题。

第 84 行添加了一张图表图像。这个名为`graph.png`的文件被添加到名为`stats`的文件夹中。10 表示距左侧的位置，80 表示距页面顶部的位置。170 是图片的宽度，80 是高度。可以嵌入链接，使用户能够跳转到感兴趣的页面。

第 85 行调用`writeHTMLCell()`函数，该函数接收包含我们要显示内容的`html`参数。该函数的参数包括：宽度、高度、X 位置、Y 位置、HTML、边框、线条、填充、重置页眉、对齐方式和自动填充。

第 87 行指定了文件将要放置的文件夹以及文件的名称。当将该页面用作界面时，可以设置参数`I`，在浏览器中渲染 PDF。当需要以文件形式获取 PDF 时，可以将其更改为`F`，它将被输出到所需的文件夹中。

```php
// Include the main TCPDF library (search for installation path).

require_once('tcpdf_include.php'); // create new PDF document

$pdf = new TCPDF(PDF_PAGE_ORIENTATION, PDF_UNIT, PDF_PAGE_FORMAT, true, 'UTF-8', false); // set document information

$pdf->SetCreator(PDF_CREATOR);

$pdf->SetAuthor("Kyle Goslin");

$pdf->SetTitle('Sample PDF');

$pdf->SetSubject('How to use TCPDF');

$pdf->SetKeywords('TCPDF, PDF, example, test, guide'); // set default monospaced font

$pdf->SetDefaultMonospacedFont(PDF_FONT_MONOSPACED); // set margins

$pdf->SetMargins(PDF_MARGIN_LEFT, PDF_MARGIN_TOP, PDF_MARGIN_RIGHT);

| 54 | $pdf->SetHeaderData(PDF_HEADER_LOGO, PDF_HEADER_LOGO_WIDTH,    |
| --- | --- |
|'Custom Sample Statistics', '', array(0, 0, 0),|
| → array(0, 0, 0));;

| 55 | $pdf->SetHeaderMargin(PDF_MARGIN_HEADER);
| 56 | $pdf->SetFooterMargin(PDF_MARGIN_FOOTER);
| 57 | // set auto page breaks
| 58 | $pdf->SetAutoPageBreak(TRUE, PDF_MARGIN_BOTTOM);
| 59 | // set image scale factor
| 60 | $pdf->setImageScale(PDF_IMAGE_SCALE_RATIO);
| 61 | // set default font subsetting mode
| 62 | $pdf->setFontSubsetting(true);
| 63 | // Set font
| 64 | // dejavusans is a UTF-8 Unicode font, if you only need to
| 65 | // print standard ASCII chars, you can use core fonts like
| 66 | // helvetica or times to reduce file size.
| 67 | $pdf->SetFont('dejavusans', '', 14, '', true);
| 68 | // Add a page
| 69 | $pdf->AddPage();
| 70 | // Gather the data
| 71 | $mode = 'The mode is: ' . getMode();
| 72 | $average = 'The averages for score1 is: ' . getAverageScore('score1');
| 73 | $stdev = 'The standard deviation of the database table is: ' . calculateStdDev();
| 74 |
| 75 |
| 76 | // Set some content to print
| 77 | $html = <<<<EOD
| 78 | Welcome to the statistics page!
| 79 | <p>
| 80 | $mode <br>
| 81 | $average <br>
| 82 | $stdev<br>
| 83 | EOD;
| 84 | $pdf->Image('stats/graph.png', 10, 80, 170, 80, 'PNG', 'http://www.tcpdf.org', '', true, 150, '', false, false);
| 85 | $pdf->writeHTMLCell(0, 0, '', '', $html, 0, 1, 0, true, '', true);
| 86 | // Close and output PDF document
| 87 | $pdf->Output(__DIR__ . '/stats/report.pdf', 'I');
```

## 示例代码 3：`custom.php` — 使用 PHP 生成 PDF — 第 2 部分

### 输出

图 9.1 展示了完成的 PDF 文件，可以在 Web 浏览器中查看或保存到外部文件中。

![](img/ed4cb7e1be98f0adec0546edd14f6223_315_0.png)

**图 9.1：** 在 PDF 文件中呈现的统计数据。

## 9.3 Cron 与任务调度

报告的一个重要方面是在固定时间将数据传递给业务利益相关者。有些时间报告可能最有用，例如，周五早上 8 点开会前，或者周一早上 9 点。

Cron，是*chronological*（按时间顺序的）的缩写，是一个旨在特定时间、日期或内部状态变化结果时执行操作的应用程序，例如运行程序或调用 URL。它是 Linux/Unix 操作系统家族中的命令行实用工具。然而，这个名称已被用作任何执行基于时间或日期操作的应用程序的通用名称。在 Windows 操作系统中，存在一个类似的应用程序，称为*任务计划程序*。该应用程序具有图形用户界面，以辅助调度过程。

在本章中，PDF 报告生成是通过在 Web 浏览器中调用 PHP 页面来完成的。虽然结果直接显示给用户，但这不是必须的。可以使用`cron`实用工具来调用 URL 以生成所需的 PDF。

要使`cron`实用工具正常工作，托管它们的主机操作系统必须保持持续运行。如果操作系统曾经关闭，所有的`cron`作业都将无法执行。因此，`cron`作业的创建方式存在区别，要么在服务器本地创建，要么在外部其他人的服务器上创建。在指定时间执行的单个任务称为`cron job`（cron 作业）。

### 示例 2：本地 cron 作业

当可以直接访问操作系统时，可以创建 cron 作业。访问服务器操作系统的优势在于，可以以程序或脚本的形式运行单个文件。由 cron 执行的各个作业存储在`crontab`（`cron table`的缩写）中。要编辑 cron 作业，我们在终端中键入以下命令：

```bash
crontab -e
```

在 cron 表中，我们可以指定希望作业运行的具体时间和日期，以及希望执行的任务。在示例代码 4 中，可以看到添加到 cron 表中一行的选项顺序。可以使用星号`*`形式的通配符来指定所有值。间隔可以定义为`/15`的形式表示每 15 分钟，或`/20`表示每 20 天。

| 选项 | 描述 | 范围/详情 |
| --- | --- | --- |
| MIN | 分钟 | 0-60 |
| HOUR | 小时 [24 小时制] | 0-23 |
| MDAY | 每月日期 | 1-31 |
| MON | 月份 | 1-12 |
| DOW | 星期几 | 0-6 |
| COMMAND | 要运行的程序或脚本 | — |

### 示例代码 4：cron 选项列表

## 示例代码 5：示例 cron 任务 — 每 15 分钟执行一次

示例代码 5 展示了一个完整 cron 任务的示例，该任务被设计为每 15 分钟调用一次`myscript.sh`。在此脚本内，会执行对 PDF 生成器的实际调用。脚本路径，例如`/home/user1/`，可以替换为我们希望运行的脚本路径。

```bash
* /15 * * * /home/user1/myscript.sh
```

## 示例代码 6：示例 cron 任务 — 每周日凌晨 4 点执行

示例代码 6 展示了每周日凌晨 4 点调用`myscript.sh`文件的模式。

```bash
0 4 * * sun /home/user1/myscript.sh
```

## 示例代码 7：捕获 cron 输出

示例代码 7 概述了如何捕获 cron 任务的输出。由于我们调用的脚本会打印文本，如果成功，此文本将显示在`output.log`文件中。

```bash
0 4 * * sun /home/user1/myscript.sh > /home/user1/output.log
```

## 示例代码 8：`myscript.sh` — 执行`GET`请求的 bash 脚本示例

示例代码 8 展示了`myscript.sh`文件的示例。当运行此脚本时，在第 2 行，将输出一段文本。在第 3 行，使用`wget`工具向`custom.php`文件发起一个 HTTP `GET`请求，该文件在第 9.2 节中已描述，用于生成 PDF。在`custom.php`中主要需要考虑的是，将输出标志设置为`F`以确保创建一个文件，而不是仅在浏览器中显示。

```bash
1   #!/bin/bash
2   echo "cron running.."
3   wget http://localhost/custom.php
```

在处理 cron 模式时，为了辅助此过程，有许多在线的 cron 任务模式生成器工具可用，例如`https://crontab-generator.org`、`https://crontab.guru`和`http://www.cronmaker.com`。

### 示例 3：外部 cron 任务

在共享主机解决方案上，cron 工具可能无法访问。在这些情况下，可以利用外部 cron 服务。使用外部 cron 工具的缺点是，它们只能访问 Web 服务器上公开的页面。所有位于服务器上但不在 Apache 服务器`htdocs`目录中的脚本和文件都将不可用。然而，使用外部服务的优点在于其服务正常运行时间通常很高，并且许多都提供了易于使用的界面，而不是手动输入 cron 任务模式。

许多不同的公司提供具有附加功能的 Web cron 工具，例如当 cron 任务执行失败时，可以向服务器管理员发送警报。其中一个例子是`cron-job.org`，如图 9.2 所示。

![cron-job.org 网站。](img/ed4cb7e1be98f0adec0546edd14f6223_318_0.png)

图 9.2：cron-job.org 网站。

**图 9.3**展示了创建新 cron 任务的过程。首先为任务指定一个标题。随后是将要调用的可通过 Web 访问的 URL。在此示例中，我们调用的是`http://www.domain.com/scriptToCall.php`页面。此 PHP 页面可以为我们执行任务，例如生成 PDF、删除文件或发送自动化电子邮件。

![为 cron 任务创建示例计划。](img/ed4cb7e1be98f0adec0546edd14f6223_320_0.png)

图 9.4：为 cron 任务创建示例计划。

在示例代码 9.4 中，输入这些详细信息后，可以指定 cron 的计划。在此站点上，可以看到一个带有直观选项的简单用户界面。提供了通知选项，以便在 cron 任务未能运行时通知您。这很有用，因为它通常表明您试图运行的服务器或任务存在问题。

## 9.4 云电子邮件服务集成

由于 cron 为我们提供了在指定时间间隔执行操作的能力，这可以轻松用于日常任务，例如报告分发。分发内容的一个简单方法是使用电子邮件。尽管电子邮件在商业环境中每天都在使用，但成功向用户发送电子邮件的过程一直存在持续性问题。

电子邮件的问题源于其最初设计的方式。对于电子邮件的发送方式或发送数量没有任何限制。因此，许多电子邮件托管提供商会快速将电子邮件标记为垃圾邮件或恶意邮件。这可能是由于发件人的 IP 地址以前被用作垃圾邮件发送，或者所发送电子邮件的质量所致。许多以前托管内部电子邮件解决方案的部门已经开始使用电子邮件托管提供商来传递邮件。这可以被视为一种稳健的方法，因为电子邮件提供商将处理确保发件人地址不被标记为垃圾邮件或恶意邮件的过程。

296 ■ 使用 JavaScript 和 PHP 进行应用用户数据收集与分析

### 示例 4：发送电子邮件

一个成功的电子邮件托管解决方案是 SendGrid。² 要使用此 API，必须执行两个步骤。第一步是从 SendGrid 网站获取一个唯一的 API 密钥。此密钥用于在计费时区分一个账户与另一个账户。第二步是验证将要使用的电子邮件地址。在此过程中，在注册过程完成后，一封来自 SendGrid.com 网站的电子邮件将被发送到所需发送地址的收件箱。此步骤确保电子邮件的发送者确实是所有者。在您拥有域名的情况下，SendGrid 提供了验证域名的功能。这是通过在您域名的 DNS 记录中添加键值对来证明真实性而完成的。³

要将此解决方案集成到现有的 Web 应用程序中，可以使用`composer`来安装 SendGrid 库。在 Web 服务器的`htdocs`文件夹中，创建一个名为`composer.json`的新文件。在此文件中，可以添加 SendGrid API 所需的 JSON，如示例代码 9 所示。

```json
{
  "require": {
    "sendgrid/sendgrid": "~7"
  }
}
```

示例代码 9：SendGrid `composer.json`内容。

添加此内容后，在命令提示符下运行以下`install`命令：

```bash
composer install
```

示例代码 10：安装依赖项。

### 输出

在图 9.5 中，可以看到使用`composer`自动安装 SendGrid 的过程。

```text
Loading composer repositories with package information

Updating dependencies (including require-dev)

Package operations: 3 installs, 0 updates, 0 removals

  - Installing starkbank/ecdsa (0.0.4): Downloading (100%)

  - Installing sendgrid/php-http-client (3.11.0): Downloading (100%)

  - Installing sendgrid/sendgrid (7.8.1): Downloading (100%)

Writing lock file

Generating autoload files
```




图 9.5：SendGrid API 正在被 composer 安装。

### 示例代码：`sendmail.php`

可以在安装 SendGrid 库的同一文件夹中创建一个名为 `sendmail.php` 的新文件。在示例代码 11 中，第 2 行引用了 SendGrid 库的 `autoload.php`。第 3 行创建了 `mail` 对象的一个新实例，并将其放入名为 `email` 的局部变量中。第 4 行设置了 `from` 地址。此地址必须是在注册服务时使用的电子邮件地址，因为 SendGrid 会发送一封验证邮件。第 5 行设置了电子邮件的 `subject`。第 6 行设置了 `to`，指明我们将电子邮件发送给谁。

在第 7 和第 8 行，调用了 `addContent()` 函数向电子邮件追加内容。此函数接受两个参数，第一个描述正在发送的内容类型，第二个包含要发送的内容。第 11 行以字符串格式附加了 API 密钥。此密钥对于您的用户账户是唯一的，必须包含在内。发送电子邮件的过程在第 12–19 行执行。一个 `try-catch` 包围了电子邮件发送过程，首先尝试发送电子邮件，如果失败，则捕获错误。可以访问响应的状态码、头部和正文，以识别发送电子邮件时是否存在问题。通常，如果 API 密钥或电子邮件发送地址出现问题，可以在这里看到。

```php
<?php

require 'vendor/autoload.php'; // 如果您使用 Composer（推荐）

$email = new \SendGrid\Mail\Mail();

$email->setFrom("johnsmith@gmail.com", "Example User");

$email->setSubject("Sending with SendGrid is Fun");

$email->addTo("johnsmith@gmail.com", "Example User");

$email->addContent("text/plain", "and easy to do anywhere, even with PHP");

$email->addContent(
    "text/html",
    "<strong>and easy to do anywhere, even with PHP</strong>"
);

$sendgrid = new \SendGrid('YOUR_API_KEY');

try {
    $response = $sendgrid->send($email);

    print $response->statusCode() . "\n";

    print_r($response->headers());

    print $response->body() . "\n";
} catch (Exception $e) {
    echo 'Caught exception: ' . $e->getMessage() . "\n";
}
```

示例代码 11：`sendmail.php` — 使用 SendGrid 发送电子邮件。

---

² https://www.sendgrid.com  
³ https://app.sendgrid.com/settings/sender_auth/domain/create

## 示例 5：带附件的 SendGrid 邮件

对原始的邮件发送过程可以进行一个简单的修改，以包含附件，例如 PDF 文件。我们将创建一个名为 `sendmail_attach.php` 的新文件，其中包含原始邮件代码，以及发送附件的小幅修改。

### 示例代码：`sendmail_attach.php`

在示例代码 12 的第 11 行，调用了 PHP 函数 `file_get_contents()` 来检索名为 `samplefile.pdf` 的文件内容，该文件与 PHP 文件位于同一文件夹中。使用 `base64_encode()` 函数将文件内容编码为 base64 格式，将其转换为可通过电子邮件发送的格式。在第 12 行，调用了 `addAttachment()` 函数，该函数接受编码后文件的引用、文件格式、文件名，并最终将其标识为附件。

```php
<?php

require 'vendor/autoload.php'; // If you're using Composer

$email = new \SendGrid\Mail\Mail();

$email->setFrom("kylegoslin@gmail.com", "Example User");

$email->setSubject("Sending with SendGrid is Fun");

$email->addTo("kylegoslin@gmail.com", "Example User");

$email->addContent("text/plain", "and easy to do anywhere, even with PHP");

$email->addContent(
    "text/html",
    "<strong>and easy to do anywhere, even with PHP</strong>"
);

$file_encoded =
    base64_encode(file_get_contents('samplefile.pdf'));

$email->addAttachment(
    $file_encoded,
    "application/pdf",
    "samplefile.pdf",
    "attachment"
);

$sendgrid = new \SendGrid('YOUR_API_KEY');

try {
    $response = $sendgrid->send($email);

    print $response->statusCode() . "\n";

    print_r($response->headers());

    print $response->body() . "\n";
} catch (Exception $e) {
    echo 'Caught exception: ' . $e->getMessage() . "\n";
}
```



示例代码12：`sendmail_attach.php` — 发送带附件的电子邮件。

## 9.5 托管PHP/JavaScript应用程序

在过去几年里，Web应用程序托管的格局已从受限的共享托管环境转变为基于云的托管，这种方式对资源的承诺较少。云托管的进一步发展是实现了轻量级的云托管解决方案，消除了配置完整操作系统和服务器的需要。其中一种解决方案是Amazon AWS Lightsail。⁴

本节将描述将在本书中开发的解决方案托管到Amazon Lightsail上的过程。使用Lightsail的主要优势包括服务器部署的速度、管理的简便性以及运行服务的每月总体成本（撰写本文时为3.50美元）。开始之前，需要一个Amazon AWS账户，可在AWS主页上创建。⁵ 创建新账户后，我们可以前往AWS的Lightsail部分。⁶

### 示例6：创建Lightsail实例

在Lightsail仪表板上，我们首先可以看到任何正在运行的实例。*实例*是已创建的单个托管解决方案。在[图9.6]中，可以看到一个现有实例。在此仪表板的右侧，点击*创建实例*以开始。

在[图9.7]中，存在一个选项来选择我们希望启动的实例类型。典型的选项分界线是选择基于Linux的映像还是基于Microsoft Windows的映像。由于Linux映像运行成本更低，我们将选择它。接下来，选择映像的*蓝图*。这是在创建映像时预加载到映像上的软件的名称。由于我们使用的是PHP和MySQL，因此选择*LAMP (PHP 7)*。

---

⁴ https://aws.amazon.com/lightsail
⁵ https://aws.amazon.com
⁶ https://lightsail.aws.amazon.com/ls/webapp/home/instances

### 下午好！

- 实例
- 数据库
- 网络
- 存储
- 快照

按日期排序

图9.6：Amazon Lightsail仪表板。

### 选择您的实例映像

**选择平台**

- Linux/Unix
- Microsoft Windows

**选择蓝图**

- 应用程序 + 操作系统
- 仅操作系统

- WordPress 5.4.2
- WordPress多站点 5.4.2
- LAMP (PHP 7) 7.4.7
- Node.js 12.18.3
- Joomla 3.9.19
- Magento 2.3.5-1
- MEAN 4.2.8-7
- Drupal 9.0.1

图9.7：选择Lightsail映像类型和蓝图。

下一个选择侧重于我们希望添加的整体RAM、CPU大小和硬盘空间。为了在应用程序的初始测试期间保持最低成本，在图9.8中，选择了3.50美元的选项。如果应用程序需要额外资源，可以随时更改此选项。此基础实例配备512MB RAM、1个vCPU、20GB固态硬盘和1TB传统存储。我们正在查看的选项基于价格。在内存、处理、存储或数据传输很重要的场景中，提供了自定义选项。

![](img/ed4cb7e1be98f0adec0546edd14f6223_326_0.png)

在图9.9中，我们可以为实例提供一个名称。当同时使用多个不同的实例以及组织月度账单上出现的名称时，这特别有用。

创建您的第一个实例后，该实例不会直接可用。它首先进入*待处理*状态，如图9.10所示。在此期间，您将无法使用该实例或创建任何远程连接。此过程通常持续不到五分钟。

一旦实例完成初始化过程，就可以访问了。要连接到实例，可以通过点击控制台图标打开控制台，如图9.11所示。这是一个完整的控制台，复制了在传统本地操作系统上看到的内容。控制台下方是您的实例的唯一IP地址。

### 识别您的实例

您的Lightsail资源必须具有唯一的名称。

标签选项
使用标签在Lightsail控制台中筛选和组织您的资源。键值标签也可用于组织您的账单并控制对您资源的访问。了解有关标签的更多信息。

图9.9：为Lightsail实例提供名称。

![](img/ed4cb7e1be98f0adec0546edd14f6223_327_0.png)

图9.10：处于待处理状态的Lightsail实例。

![](img/ed4cb7e1be98f0adec0546edd14f6223_327_1.png)

图9.11：运行中的Lightsail实例。

可以直接输入到Web浏览器中，将显示一个简单的默认HTML页面。

在图9.12中，可以看到实例的控制台。要查看当前所在的文件夹，可以使用`ls`命令。执行此命令后，我们可以看到有一个`htdocs`文件夹，它作为Web应用程序的根文件夹。这类似于本地Apache Web服务器上的`htdocs`。

![](img/ed4cb7e1be98f0adec0546edd14f6223_328_0.png)

图9.12：Lightsail集成控制台。

### 示例7：将文件上传到实例

尽管我们现在拥有控制台访问权限来运行任何我们希望的命令，但此时的主要愿望是上传本书中描述的示例PHP/JavaScript示例。为此，我们首先需要获取访问密钥，该密钥将在进行外部连接时用于对服务器进行身份验证。为此，仪表板的账户部分提供了一个密钥管理部分。⁷ 在[图9.13](#)中，我们可以看到尚未添加自定义密钥。我们可以使用默认密钥，而不是创建自定义密钥。这只需点击实例托管区域旁边的*下载*即可完成。此私钥将具有`.pem`扩展名，应存储在安全的地方。

要连接到服务器并传输文件，我们将使用安全文件传输协议（SFTP）。最常用的工具是FileZilla客户端。⁸ FileZilla是一个免费且开源的工具，支持多种文件传输格式。要获取FileZilla，只需点击如[图9.14](#)所示的*下载客户端*选项。下载完成后，应将其安装在您的系统上。

---

⁷ https://lightsail.aws.amazon.com/ls/webapp/account/keys
⁸ https://filezilla-project.org

### 管理您的 SSH 密钥？

请选择默认密钥，创建新密钥或将现有公钥上传到拥有资源的 AWS 区域。

每个 AWS 区域可存储最多 100 个密钥。

![](img/ed4cb7e1be98f0adec0546edd14f6223_329_0.png)

图 9.13：创建或下载现有密钥的选项。

![](img/ed4cb7e1be98f0adec0546edd14f6223_329_1.png)

图 9.14：FileZilla 主页。

在图 9.15 中，安装 FileZilla 后，我们现在可以开始创建连接的过程。首先选择“新建站点”选项。在协议部分，应选择 SFTP。主机是您在 Lightsail 仪表盘的控制台按钮下可以找到您的唯一实例的 IP 地址。登录类型设置为密钥文件（Key file），因为它将使用之前下载的`.pem`文件。此实例类型的默认用户名为`bitnami`。在密钥文件选项旁边，

![](img/ed4cb7e1be98f0adec0546edd14f6223_330_0.png)

托管、报告和分发 ■ 307

![](img/ed4cb7e1be98f0adec0546edd14f6223_331_0.png)

![](img/ed4cb7e1be98f0adec0546edd14f6223_331_1.png)

图 9.17：在 FileZilla 中选中用于上传到实例的文件。

# 使用 JavaScript 和 PHP 应用用户数据收集与分析

![](img/ed4cb7e1be98f0adec0546edd14f6223_332_0.png)

图 9.18：在 Web 浏览器中查看的示例应用程序。

## 9.6 总结

本章通过描述任何 Web 应用的基本组件结束了数据分析过程。已描述了报告生成，这是一种使用 PHP 快速生成 PDF 报告的简单方法。为了提供同步的报告方式，针对本地和外部 cron 源均描述了 cron 和任务调度。随着电子邮件投递管理已成为全职工作，已描述了基于云的电子邮件服务的基础知识作为内部电子邮件托管的替代解决方案。

最后，为了采取本书中描述的解决方案并提供切实的应用程序，描述了一种使用 Amazon Lightsail 的轻量级云 Web 应用托管解决方案。

# 索引

注意：文本中的斜体表示图表，粗体指示表格。

- **A**
  - 主动数据收集，3–4, 11
    - 二进制数据收集，11–16
      - `ajax.php`, 12–16
      - `binary.html`, 12–14
      - `create.sql`, 11–12
      - `jQuery`, 14, 12
    - 自定义响应表单，29–38
      - `Bootstrap`, 29
      - `create.sql`, 29–30
      - `form.html`, 29–35
      - `jQuery`, 29
      - `saveForm.php`, 29, 35–38
    - 星级评分，21–28
      - `ajax.php`, 24–28
      - `create.sql`, 21, 23
      - `jQuery`, 26
      - RateYo! 星级评分包，21
      - `rating.html`, 21–24
      - 检索，26–28
      - `star.php`, 26–27
    - 基于文本的数据收集，16–21
      - `ajax.php`, 17, 19–21
      - `binary.html`, 16–19
      - `create.sql`, 16–17
      - `jQuery`, 17
- `AddAtt`, 124
- `AddAttachment()` 函数，299
- `AddContent()` 函数，298
- `AddElementToCamp`, 146, 148
- `AddEventListener`, 75
- `Add()` 函数，206, 208–209
- `AddItem()` 函数，45–46
- `Addnewcamp`, 141
- Add new campaign, 142–150
- `AddNewCamp()` 函数，140–141
- `AddPage()` 函数，288–289
- `AddTimeSeries()` 函数，241
- Add Visualization 选项，130–139
- `AddViz()` 函数，124–125, 131
- Add Vizualization, 124
- `Ajax.php`
  - 二进制数据收集，12, 14–16
  - 活动，139, 141–143, 148
  - 数据库表，79–80
  - 页面，141
  - 选择活动元素，123–129
  - 星级评分，24–28
  - 基于文本的数据收集，17, 19–21
  - 用户 IP 地址，63–64
  - 用户注册页面，96, 101–103
- `Alert()` 函数，13, 24
- `Alert()` 语句，18, 146
- **亚马逊**
  - AWS Lightsail, 300
  - 云平台，285
- Lightsail, 308
- AMPPS, 5
- Apache Web 服务器，2, 5
- `Append()` 函数，277
- Apple Mac, 5
- `Aria-describedby`, 30
- `Aria-labelledby`, 124
- `Array count values()` 函数，179
- `Array push()` 函数，182
- `Articleid` 列，23
- `Autoload.php`, 186
- `Avg()` 函数，269-270

- **B**
- `Barchart.php`, 130, 132
- `Bar.php`, 137-139
- `Base64 encode()` 函数，299
- Basic dashboard, 116-123
- `Bcrypt` 算法，94, 102
- `Beforeunload`, 75
- `B-g-light` 颜色，90
- BigHugeLabs.com API, 175-177
- Binary bar chart, 110-115
- Binary data collection, 11-16
  - `ajax.php`, 12, 14-16
  - `binary.html`, 12-14
  - `create.sql`, 11-12
  - `jQuery`, 14, 12
- Binary feedback, 110
- `Binary.html`
  - 二进制数据收集，12-14
  - 基于文本的数据收集，16-19
- `bindParam()` 函数，15, 19, 25, 27, 63, 79, 93, 102, 109, 141, 148
- `Bitnami`, 305
- Blueprint for image, 300
- Bootstrap, 87, 89, 117-118, 123
  - 自定义响应表单，29
  - 仪表板，119
  - `form.html`, feedback, 32-33
  - JavaScript 文件，96
  - 库，89
  - modal, 38, 160
  - 网站，90
- `Bootstrap.js`, 88, 95
- 基于浏览器的网站缓存，7

- **C**
- `CalculateDiffFromDate()` 函数，279, 281
- `CalculateStdDev()` 函数，272
- `CalendarGetRecords.php`, 245-246, 250
- `Calendar.php`, 245-246, 248
- Campaigns, 87, 115, 120, 139-142
  - 元素，142-150
  - 选择元素，123-130
- `CampID`, 117-118
- `Camps.sql`, 116-119
- `Canvas`, 107
- `Canvas` 标签，225, 231
- `Categorise()` 函数，186
- `Chart`, 131
- `Chart.bundle.js`, 104, 107, 111
- `ChartColors`, 217
- `Chart.draw()` 函数，247
- `Chart.helpers.color`, 229
- `Chart.js`, 104, 106, 212, 223
- `Chart.js.zip` 文件，105
- `Chart()` 对象，231
- `Chart1.php`, 104, 107
- `Chart2.php`, 111-112, 114-115
- `Charts.js`, 3
- `Click()` 处理器，17, 205, 255, 277
- 基于客户端的过滤器，156
- 客户端 Cookie; *参见* 服务器端会话
  - 自定义附加函数，45–47
  - 遍历 JSON，43–45
  - JSON 内容，42–43
  - 简单设置和获取，40–42
- `Closedir()` 函数，148
- 基于云的电子邮件服务，308
- 云电子邮件服务集成，295–300
- 导航栏折叠 (`navbar-collapse`), 119
- 可折叠树形布局，195–200
  - 基于文本的反馈，195–200
- 颜色编码流程，254
- 颜色阴影索引，252
- 命令行
  - 应用程序 Composer, 5–6
  - 实用程序，291
- 逗号分隔值 (CSV) 文件，3, 49
- `Completion.php`, 171
- Composer, 5–6, 82
- `Composer init` 命令，82
- `Composer.json`, 6, 82–83, 83
- `Config.data.datasets[0]`, 233
- `Connections array`, 209
- `Console.log()` 函数，6–7, 65, 77, 92, 131, 197, 206, 241, 246, 257
- `Contactinfo`, 48
- `Container div` 标签，107
- 内容分发网络 (CDN), 5, 12, 40–41, 154, 215, 224, 254, 276
- Cookies and sessions
  - 客户端 Cookie, 40–47
  - `cookies.html`, 41
  - 删除，42
  - 开发者控制台，41
  - 可靠性，40
  - 服务器端会话，47–49
- `Cookies.html`, 41–42
- `Cookies json.html`, 42–43
- `Cookies set()` 函数，44
- `Count()` 函数，109, 114, 183, 213, 281
- `CountInDocs()` 函数，183
- `Create dashboard.sql`, 88–89
- Create new campaign, 140
- `Create.sql`, 61, 171, 195–196, 201–202, 213, 223, 238–239, 245, 267, 272
  - 二进制数据收集，11–12
  - 自定义响应表单，29–30
  - PDF 生成，286–287
  - 百分比差异，275
  - 星级评分，21, 23
  - 基于文本的数据收集，16–17
- Cron
  - 任务，292, 294–295
  - 表，292
  - 和任务调度，291–295
- `Crontab -e`, 292
- CSV 文件，55
  - 来自 Google Forms, 53–55
  - 从文件中读取，55–56
- Current Epoch time, 222
- `CurrentIdProcessed` 变量，241
- `CurrentTerm`, 154
- `CurrentTime`, 240
- 自定义仪表板，87
  - 二进制条形图，110–115
  - 动态仪表板，115–150
  - 多列条形图，104–110
  - 用户登录，88–95, 93
  - 用户注册，95–104
- 自定义响应表单，29–38
  - Bootstrap, 29
  - `create.sql`, 29–30
  - `form.html`, 29–35
  - jQuery, 29
  - `saveForm.php`, 29, 35–38

- **D**
- `Dashboard_accounts`, 88, 102
- Dashboard camp elements, 120
- `Dashboard.css`, 117
- 数据收集，66
  - DATE, 159
- Data, 119
- 数据表，275
- 数据库表，118, 196
- Date selection control, 231
- `Date()` 函数，93, 197, 240, 277
- `Db data.sql`, 245
- `Dbname`, 5
- DELETE request, 230
- Developer console, 41
- `Diffcalc` table, 276
- `Diff.php`, 275
- Div tags, 107
- Document class, 298
- Document ready, 117, 183, 196, 215
- DOM (elements), 6, 30, 124, 131, 196, 247
- `Done()`, 132
- Double/decimal value, 11
- Download the JSON, 124
- `Draw()` 函数，229
- Dynamic dashboard, 115-150

- **E**
- `Echo getcwd()`, 148
- Edit element modal, 148
- `Element`, 141, 147
- Element with form, 45
- Email, 2, 38
  - distribution, 290
  - hosting, 295
  - services, 285, 295
- Email library, 296
- Encoding parameter, 54
- Epoch time, 93, 197, 222, 228, 275
- Error callback, 42
- Error handling, 299-300
- Event listeners, 75, 255
- `Exception`, 299

- **F**
- Facebook, 81
- `Fclose()` 函数，57
- Feedback
  - dashboard, 90
  - tree database table, 196
- `FeedbackElementID`, 107
- `FeedbackFormId`, 107, 112
- `Feedback form records.sql`, 104, 107
- Feedback heat map, 252–265
- `FeedbackRecords`, 206
- `FeedbackRecords[i]`, 208
- Feedback statistics, 267
  - basic statistics, 267–273
  - percentage difference, 275–283
  - working with samples, 263–274
- `Feedbacktext`, 213
- `Feof()` 函数，57
- `FetchAll()` 函数，250
- `Fgetcsv()` 函数，56, 132
- `Fgets()` 函数，57
- `File get contents()`, 299
- `File get contents()` 函数，177
- FileZilla, 305–306, 306–307
- `FindOutWhy()` 函数，17
- `Fopen()` 函数，55
- `ForEach()` 函数，233
- Foreach statement, 183
- `Foreach()` 语句，109
- `Format()` 函数，235
- `Form.html`
  - Bootstrap feedback, 32–33
  - custom JavaScript form validation, 35
  - custom response form, 29–35
- `FormID`, 109
- `Function()` 函数，228

- **G**
- `GenerateGraphForTerm()` 函数，206
- `GenerateJSON.php`, 195, 200
- `GenerateTree()` 函数，197
- Geographical information, 69
- `Geo.html`, 67–71
- Geolocation-db.com, 67–69
- `GetAverageScore()` 函数，270
- `GetBlockForHour()` 函数，259
- `Getcamp`, 125
- `GetContext()` 函数，217
- `GetData()` 函数，112, 115, 132, 134, 163
- `GetData.php`, 256, 258–263
- `GetDataRecords()` 函数，281
- `GetDataSourceOptions()` 函数，132
- `GetDate()` functions, 240
- `GetDateRecords()` 函数，279
- `GetDiff.php`, 275, 277–278, 281
- `GetElementById()` 函数，17, 210
- `GetElementById()` selector, 217
- `Getformfields`, 125
- `GetFullYear()`, 240
- `Get()` 函数，41
- `Get ip.php`, 59
- `getJSON()` 函数，42, 44
- `getJSON()` request, 60
- `GetMessage()` 函数，15
- `GetMode()` 函数，268
- `GetMode.php`, 268–269
- `GetMonth()`, 240
- `GetNegativeRecords()` 函数，250
- `GetNumberOfNegative()` 函数，214
- `GetNumberOfPositive()` 函数，214

# 314 ■ 索引

## A
`GetPositiveRecords()` 函数，250
`In array()` 函数，164
`GetRating()` 函数，27
`Index.html`，50，106
`GetRecords()` 函数，235
`IndexOf()` 函数，154，192，206
`GetRecords.php`，201–203，205，254
`Index.php`，88–92
内部电子邮件托管，308
`GetRedFlags()` 函数，164，166
行内块级元素，96
`GetSatisfactionScores()` 函数，109
InnoDB 存储引擎，153
`InputArray`，157
`GetScore()` 函数，259
INSERT 语句，15，63，79，103
`GetStdDev.php`，272-273
互联网服务提供商 (ISPs)，58
`GetTimeOnCurrentPageInSeconds()` 函数，77
逆文档频率，180–184
`GetTimeRecords.php`，223，232，235
IPify，59
GitHub 仓库，104
`Ipstack.com`，69–71
Google Charts，3，245
`Isset()` 函数，81
Google Chrome，3
`IsStopWord`，157
Google Forms，53
`Iterate.html`，44–45
CSV 文件，54
csv 响应，55
导出选项，54
示例，54
Google Map，67
`Graph.php`，201，204-211

## H
`Handle file upload()` 函数，52
哈希，88
`Heat.php`，253–256
`HourStamp`，260
`Href` 标签，119
HTML，2
`Html()` 函数，33，68，125，256，277
HTTP REFERER 变量，80–81

## I
File Upload 演示，51
`ID output1`，154
`ID output2`，154

## J
JavaScript，2，6–7
代码，2
GET 请求，59–60
jQuery 库，44
库，2-3，5
POST，12-13
script 标签，7
停用词函数，154–156
基于 JavaScript 的库，189，215
jQuery，14，50，89，158，195，201，224，239，245，254，275
二进制数据收集，12
CDN，61
`click()` 监听器，13
自定义响应表单，29
日期选择器，164
jQueryUI，117，123
POST，14
星级评分，26
基于文本的数据收集，17
版本 3.5.3，2
卸载时的自定义函数，75–76
数据库表，保存到，76–80
`Jquery.min.js`，88，96
`Json decode()` 函数，177
JSON 内容，3，42–43
自定义 JavaScript 函数，47
`getJSON()` 函数，42
迭代值，43–45
JavaScript jQuery 库，44
设置和获取 JSON 值，43
JSON 格式化工具，197
JSONP，70
`JSON.parse()` 函数，197
`JSON.php`，198
Jumbotron，90，96
JQueryUI，158，201，224，254，275–276
日历部件，227
Js-cookie 库，40

## L
LAMP (PHP 7)，300
Lightsail 镜像，301
Lightsail 实例，300–304，303–304
LIMIT 1 子句，93
`Line.php`，130，132，134–137
Linux 发行版，5
`List-group`，124
`ListOfFiles.php`，143，145，147–148
`List-tab-att` 项，131
`List-tab-camp` 元素，125
`LoadData`，225，228
`Load()` 函数，246
记录时间，75–80

## M
MAMP，5
外边距，89，96
`Message span` 标签，100
Microsoft Windows，5
模态对话框，124
`Modal()` 函数，34，101
`Modal-header`，124
`Modify()` 函数，235
Moment.js，212，223
多列柱状图，104–110
`MyArray`，48
`Mycanvas`，239
MySQL 8 社区版数据库，3
MySQL 数据库，5，12，198
时间和日期的数据类型，222
表，118
`Mytime`，23

## N
自然语言处理 (NLP)，151–152
导航栏，90
`Navbar-brand`，90
`Navbar-dark` 主题，119
`NewDate()` 函数，234，239
`New Date().getTime()`，241
N-grams，167–168
生成 n-grams，168–170
`NodeId`，206
`Nodetree`，202
节点树数据库表，202
`NormalRecord`，208
布尔变量，207
变量，209
`Number()` 函数，247

## O
`Oauth()` 函数，84
`OptionString`，146
`Output div` 标签，131

## P
内边距，89，96
`PageID` 列，76
`PageOfInterest`，43
`PARAM_INT`，15
`PARAM_STR`，102，15
`ParentNode`，209
被动数据收集，3-5，39-40
Cookie 和会话
客户端 Cookie，40-47
服务端会话，47-49
div 标签，跟踪单个，73-74
使用 TimeMe.js，73-74
记录时间，75-80
卸载时的自定义函数，75-76
数据库表，保存到，76-80
从文件读取，49-58
CSV 文件，55-56
来自 Google Forms 的 CSV 文件，53-55
文本文件，56-58
上传文件到 Web 服务器，50-53
社交媒体内容，81-86
密码，88，92
`Password1`，97，100
`Password2`，97，100
`Password hash()` 函数，102
`Password verify()` 函数，94
`Pathinfo()` 函数，52
PDF 生成
`create.sql`，286-287
使用 PHP，290-291
`PDF_HEADER_LOGO`，288
`PDF_HEADER_LOGO_WIDTH`，288
`PDF_IMAGE_SCALE_RATIO`，288
`PDF_PAGE_FORMAT`，288
`PDF_PAGE_ORIENTATION`，288
百分比差异，275-283
PHP，2
对 Big Huge Lab 的 API 的 API 请求，177-178
JAVASCRIPT 应用，300
lightsail 实例，300–304
上传文件到实例，304–308
停用词函数，156–158
PHP 数据对象 (PDO)，14
PHPinsight，185
PHPinsight 包，6
指针，89
Popper，89
`Popper.js`，96，117，123，275
PorterStemmer，173
正面与负面反馈日历，244–252
`Post()` 函数，12–14，34
`Prepare()` 函数，268，270
`PreventDefault()` 函数，33，91
`Print r()` 函数，179
`Push()` 函数，45，132，233
Python NLTK 库，153

## Q
`Querybox`，146

## R
`RateYo()` 函数，22
RateYo! 星级评分包，21–22
`Rating.html`
星级评分，21–24
`Rawtext`，198
`Read text.php`，57
实时环境，238
实时反馈
分析，237–244
分数报告折线图，244
`Realtime.php`，238–242
`RecordFetch.php`，239，242–243
`Redflag comments.sql`，158–159
红旗监控，158
仪表盘选项，158–167
`RedFlags` 数组，164
`RedFlags.php`，158，163–164，167
`Redflagterms.sql`，158
`Redflagterms` 表，160
`Ref.php`，80
`RegisterNewUser()` 函数，35，101
`Register.php`，95–101
`Remove()` 函数，162
`Replace()` 函数，231
报告生成，285–286
及交付，1
PDF 生成，286–291
`Resizable()` 函数，135
响应表单，37
`RgbtoString()` 函数，229
`RootWords` 变量，171
`Round()` 函数，27

## S
`SampleSentence`，155
示例词频得分，181
示例值，47
抽样，273–274
`SaveAnswer()` 函数，13，61
`SaveForm.php`
自定义响应表单，29，35–38
`SaveRating()` 函数，24
`SaveWhyAnswer()` 函数，17
`SaveWhyAnswer()` JavaScript 函数，17
`ScoreCount` 列，268
`Score()` 函数，186
`Script` 标签，131，205
安全文件传输协议 (SFTP)，304
选择活动元素，123-130
选择活动，129
`SelectedDate`，76
SendGrid 库，90
带附件的 SendGrid 邮件，299
`Sendmail attach.php`，299
句子补全，165-173
情感分析，184-187
`Serpent.php`，111
服务端 PHP，86
服务端会话，48；另请参见客户端 Cookie
存储数组，15-16
存储变量，16
`Servicerating`
数据库表，29-30
表，33
`Session arrays.php`，48-49
`Session destroy()` 函数，16
`Session destroy.php`，16
`Session.php`，15-16
`Session start()` 函数，49
`Set()` 函数，11-12
`SetInterval()` 函数，60
`SetOnLoadCallback()` 函数，19
`Show()` 函数，17
`ShowRedFlags()` 函数，162-163，167
简单随机抽样，274
简单文本文件，56-58
`SingleDates` 数组，26
`SingleT` 变量，103
Smoothie Charts，229
社交媒体内容，基于 Twitter 库的 Feed 提取，82-86
固态硬盘，1
`SourceType` 变量，35
`Span` 标签，97
`Split()` 函数，191，192，193，194
SQL `avg()` 函数，268
SQL INSERT 语句，15
`Star.php`
星级评分，35-37
星级评分数据库表，28，29
`StarRatingLog()` 函数，35
星级评分，11-14
`ajax.php`，26-28
`create.sql`，15
示例，26
界面，22
jQuery，25
RateYo! 星级评分包，21-22
`rating.html`，11-14
检索，26-28
`.php`，19-23
`Std()` 函数，27
`Stemming.php`，172-174
停用词，156-158
JavaScript 停用词
PHP 停用词函数，156-158
`Stopwords.html`，156-158
`Stopwords.php`，154-158
分层抽样，274
`StripStopWords()` 函数，157-158
`Strlen()` 函数，176
`StrokeStyle`，141
`Strpos()` 函数，177-178
`Strtotime()` 函数，279
`Strtr()` 函数，23
结构化数据，29
`Substr count()` 函数，183
`Substr()` 函数，177，178，204
`Substr()` PHP 函数，219
SurveyMonkey，5
`Survey.sql`，111-112

# 索引

## S

- 同义词，174–175
  - BigHugeLabs.com API，175–177
  - 对 Big Huge Lab's API 的 PHP API 请求，177–178
- 系统抽样，274

## T

- 任务调度器，292
- TCPDF，285，287–291
- TCPDF-master 文件夹，287
- `TermArray`，154
- `TermCount`，207
- `TermCount` 记录，206
- 词频-逆文档频率 (TF-IDF)，180–184，188
- 词频 (TF)，178–180，188
- 关键词节点图，200–211
- `TermsSplit` 数组，206
- 词权重，178
  - 逆文档频率，180–184
  - 词频，178–180
- 文本，151
  - 分析，120，162
  - 文件，56–58
  - 自然语言处理，151–152
  - N-gram，167–168
    - 生成 N-gram，168–170
  - 红旗监控，158
    - 仪表板选项，158–167
  - 句子补全，170–173
  - 情感分析，184–187
  - 停用词，152–153
    - JavaScript 停用词函数，154–156
    - PHP 停用词函数，156–158
- 基于文本的数据，16–21，151
  - `ajax.php`，17，19–21
  - `binary.html`，16–19
  - `create.sql`，16–17
  - `jQuery`，17
- `Text()` 函数，92
- `Text_string`，191
- `Tfidf.php`，182
- `Tf.php`，179
- TIME，222
- `Timeanalysis` 数据库，224
- 基于时间的反馈，221
  - 反馈热图，252–265
  - 正面与负面反馈日历，244–252
  - 实时反馈分析，237–244
  - 时间线与数据库数据类型，221
    - 日期与时间，221–223
    - 时间段分析与可视化，223–237
- TimeMe.js，73–74
  - 实现，71–72
  - 库，71
- `Time.php`，72–76，212–213，216
- `Timepicker`，225
- Timepicker.co，224
- `TimeRecordLog()` 函数，79
- 时间段分析与可视化，223–237，265
- `Timesegment.php`，223–224，230，234–236
- `TimeSeries()` 函数，240
- `TimeSpentOnElement.toFixed()` 函数，73
- 带有正面与负面评论图表的时间序列分析，211–219
- TIMESTAMP，222
- `TimingDataStore()` 函数，75，77
- `Timinglog.sql`，76–77
- `Timing.php`，77–80
- 工具提示定位引擎，89
- `TrackTimeOnElement` 函数，73
- 基于树的结构，201
- 基于树的可视化，196
- `TreeData` 变量，197
- `Tree.html`，195
- Tri-grams，168
- `Trim()` 函数，192，206
- `Try-catch` 语句，15，19
- Twitter，81
  - `auth.php`，82，84
  - 基于库的 Feed 提取，82–86
  - OAuth 流程，84
- `Twitteroauth` 库，82

## U

- Unix 时间戳，222
- `UploadHandler.php`，50–53
- 上传文件
  - 到实例，304–308
  - 到 Web 服务器，50–53
- 上传 URL 引用，52
- 用户
  - `agent.html`，65–66
  - `agent.php`，66
  - 地理位置，67–71
    - geolocation-db.com，67–69
    - ipstack.com，69–71
  - IP 地址，58–64
  - JavaScript GET 请求，59–60
  - JSON 格式，59
  - 用户是/否选择与 IP 地址，60–64
  - Web 浏览器 URL，59
  - 登录
    - 密码，88，92
    - 用户名，88，92
  - 注册，95–105
  - 用户名，88，92
  - 变量，94
  - 是/否选择与 IP 地址，60–64
- `Utils.js`，104，111

## V

- `Val()` 函数，13，33，61，92，99，205，231–232，256
- `Varchar` 数据，29
- `ViewChart`，255
- `ViewData`，276
- View Red Flags，120，162
- Vis.js 图，212
- `Vis.Network()` 构造函数，210
- `Vis-network-min.css` 文件，204
- `Vis-network.min.js` 文件，204
- 可视化，2，122，130–139，189，194，204
- `Viz.js`，201

## W

- Web 应用程序，5
- Web 浏览器，40
  - URL，59
- Web 服务器，上传文件到，50–53
- `WhyAnswer()` 函数，19
- `Whyanswerlog` 数据库，16–17
- `Window.chartColors`，228
- `Window.myLine.update()` 函数，233–234
- `Window.myLine` 变量，231
- `Window.onload()` 函数，217
- 词云，189–194
  - `Wordcloud.html`，190
  - `Wordcloud2.html`，191，194
  - `Wordcloud2.js`，189–191
  - `WordsCount` 数组，192
  - 词干提取，173–174
- `WriteHTMLCell()` 函数，289

## X

- XAMPP，5

## Y

- YEAR，222
- `Yesno` 数据库表，11–12
- `Yesno ip.html`，61
- `YesNoLog()` PHP 函数，14，63

## Z

- Zip 文件，53–54
