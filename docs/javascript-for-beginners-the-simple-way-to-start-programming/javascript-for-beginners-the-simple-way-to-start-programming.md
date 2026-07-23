# Javascript 初学者指南：简单的编程入门方法











# 引言

Javascript 是一种客户端编程语言，其处理引擎嵌入在 Internet Explorer、Netscape、Firefox 等浏览器中。这使得处理引擎在浏览时能够读取和解释包含 javascript 代码的网页。

Javascript 首次出现于 1995 年，尽管当时它被称为 Livescript。这个名字后来被改为 javascript。

Javascript 的发明是为了为 HTML 页面添加更多令人兴奋的功能。HTML 本身是非常枯燥的，除了显示网页之外什么也做。相反，Javascript 编程可以提供许多令人兴奋的功能，如执行计算、允许用户与网页交互、执行表单验证、操作网页上的元素、提供出色的视觉效果、实现动态功能等。

所有这些功能都为网站用户提供了增强的体验。因为 javascript 是一种客户端语言，所有这些功能都可以在无需频繁引用服务器的情况下实时可用。这防止了时间延迟并增加了用户的满意度。

让我们仔细看看使用 javascript 编程可以做的伟大的事情：

### 执行计算

Javascript 可用于从简单到高级的数学计算。如果您希望用户通过输入某些需要某种计算的信息并根据结果显示相关内容来与您的网站交互，这将特别有用。例如，如果用户在网站上输入所需的贷款金额，javascript 可以计算还款并显示相应的结果。此外，javascript 还可以告知日期和时间、记录活动时间并执行复杂的日期时间计算。

### 用户交互

网页上的 javascript 可以通过事件接收用户的交互并执行特定功能。一些最流行的事件包括：

- onblur
- onchange
- onclick
- ondblclick
- onfocus
- onkeydown
- onkeypress
- onkeyup
- onload
- onmousedown
- onmousemove
- onmouseout
- onmouseover
- onmouseup
- onselect
- onsubmit

### 执行表单验证

Javascript 可以验证和检查用户输入，以确定其是否符合某些要求。例如，您可以检查某个字段是否为空、电子邮件地址格式是否正确、邮政编码格式是否正确等。

在大多数情况下，如果您的网站访问者犯了错误，警框可以向其显示适当的错误信息。

### 操作网页上的元素

Javascript 允许用户通过上述事件在与用户交互时更改网页的内容或样式。例如，悬停在某些文本上可以使图像出现，提交按钮上的文本可以在提交时发生变化等。

### 提供视觉效果

Javascript 有许多方法为网页提供视觉效果，这是其他服务器端编程语言无法提供的。这一个典型的例子是一些华丽的图像悬停按钮。

### 实现动态功能

Javascript 配合 AJAX（异步 JavaScript 和 XML）可以用于创建动态应用程序。其中一个示例是在不刷新页的情况下向网页上加载动态内容。

# 第一章

## 什么是 JavaScript？

我们中的许多人经常看到屏幕上弹出一个窗口，说我们需要运行 Java 或更新 JavaScript。大多数人对这两者之间感到困惑，并好奇 Java 和 JavaScript 之间的区别。

### JavaScript 的目的是什么？

JavaScript 通常用于创建交互式网页。JavaScript 将运行在访问者的系统上，您不需要在所访问的网站上持续下载它。因此，整个用户体验将更快、更流畅。如果您是网站的访问者，您会注意到 JavaScript 通常用于创建测验和投票以及其他鼓励交互的内容。使用该程序的主要目的是在网站和访问者之间创建交互，这种交互不仅限于访问网站。

### JavaScript 与 Java 有什么区别？

Java 是一种用于创建需要在虚拟机或浏览器中运行的应用程序的计算机语言。它允许程序员使用英语而不是常用的数字代码。JavaScript 是一种面向对象的编程语言代码，可以在浏览器中运行。

### 运行 JavaScript 需要什么？

如果您使用 IE、Firefox 或 Chrome 等主流浏览器，您不需要特殊工具即可运行 JavaScript。所有这些浏览器都内置了该支持。但是，只有当您的用户拥有支持 JavaScript 并启用了 JavaScript 的浏览器时才能工作。如果是这样，当有人访问网站时，JavaScript 就会自动运行。

人们不需要接受任何培训来运行 JavaScript。这些代码是预先写好的，并作为插件轻松可用。如果用户的浏览器支持 JavaScript 并启用了它，JavaScript 就会自动运行。

### 编写 JavaScript 需要什么？

编写 JavaScript 不需要特殊的代码。因为它是解释型语言。可以使用记事本或任何类似的纯文本编辑器创建该语言。

### 设计师可以使用 HTML 替代 JavaScript 吗？

HTML 不能替代 JavaScript。这两种编程语言完全不同，具有不同的功能、特性和能力。HTML 是一种标记语言，旨在创建静态网页内容，而 JavaScript 是一种可以执行动态任务的编程语言。它可以在网站的不同页面上反复使用。这可以通过将其外部化并放在单独的文件中并将 JavaScript 文件链接到 HTML 代码中来实现。

特定的页面。因此，通过在每个页面上添加正确的标签，可以将 JavaScript 添加到许多页面中。

## 静态与动态

JavaScript 的功能比 HTML 更强大，因为 HTML 是静态的，而 JavaScript 是动态的，这意味着它可以对查看者的操作做出反应，例如点击或在对象上滚动鼠标。JavaScript 通常被称为“行为”（behaviors）。一个行为由观众的“事件”（event）和程序的响应或“动作”（action）组成。你可以编写程序在观众点击时触发某种行为，也可以编写程序在观众双击时触发——这就是所谓的“事件”。当“事件”发生时，程序会通过显示某些内容（如下拉菜单）或执行某些操作（如播放声音）来做出响应。通过 JavaScript，你的网站是“动态的”，因为它能对观众点击的普通超链接做出响应！

## 客户端编程对比 服务端编程

JavaScript 是一种“客户端”编程语言。客户端意味着程序代码会与网页的其他代码（通常是 HTML）一起发送到你的计算机；然后，你的浏览器会读取代码并执行其指令。在许多带有 JavaScript 的网站上，你可以通过进入浏览器的“编辑 -> 查看源代码”直接与 HTML 一起查看编程代码。你通常可以判断代码中是否包含 JavaScript，因为 `head` 标签中会有一个显示 `language="JavaScript"` 的标签。这是查看某些运行脚本的好方法。（有些网站会隐藏它们的 JavaScript 代码。）

## JavaScript 与浏览器

JavaScript 经常用于执行简单的编程任务，因为网页查看者可以在电脑上关闭 JavaScript，这意味着当他们查看你的网站时，你所有复杂的编程工作都无法运行。出于安全考虑，可能会关闭 JavaScript，有些浏览器的默认设置禁用了 JavaScript。相反，我们使用 JavaScript 来增强网页的功能。例如，如果你完全依赖 JavaScript 来验证在线表单，就会留有安全漏洞。如果观众的 JavaScript 被关闭，它将绕过你的验证。因此，你可能还会使用“服务端”编程语言来双检输入。

较新的浏览器通常拥有较版本的 JavaScript，这意味着有更多的编程选项。一些旧浏览器无法读取 JavaScript，或者只能读取有限数量的 JavaScript。启用 JavaScript 的浏览器可以读取某些版本的 JavaScript。

## JavaScript 在网页设计中的优缺点

这部分讨论了在网站设计中使用 JavaScript 的优点和缺点。它指出了 JavaScript 作为基于 Web 的编程语言的领域，同时也描述了使用它实际上可能会损害网站性能的情况。

首先，JavaScript 是一种基于浏览器的编程语言，它实际上在客户端运行。这意味着你用 JavaScript 编写的任何代码都会随你的网页一起交付，而你编写的脚本实际上运行在用户的浏览器内部，而不是直接运行在提供网页的服务器上。在某些情况下，JavaScript 是实现网页设计整洁功能的极佳解决方案，但在某些情况下，使用 JavaScript 可能会损害你网站的性能。

## 网页设计中的 JavaScript - 优点

JavaScript 是在客户端实现表单验证的极佳解决方案。这意味着如果用户忘记在表单中输入姓名（例如），JavaScript 验证函数可以弹出一个消息让他们知道漏掉了内容。这比使用服务端验证程序来处理错误要好得多，因为服务器不需要进行任何额外的处理。可以编写一个 asp 或 php 程序来实现相同的任务，但 JavaScript 会在表单从一开始没有正确完成之前就不允许其提交，这是一种要稳健得多的解决方案！

JavaScript 另一个表现优色的领域是创建动态效果，例如滚鼠标悬停图像和脚本幻灯片，这些功能的使用已变得非常普遍。因为 JavaScript 运行在客户端浏览器内部，它可以用于在服务器发送页面后更改屏幕的外观。这允许它创建一些非常令人印象深刻的动态图像效果。

## 网页设计中的 JavaScript - 缺点

使用 JavaScript 的主要缺点之一是它倾向于使网页严重臃肿。如果你将其用于任何稍微有趣的功能，JavaScript 代码可能会迅速累积到数百或数千行代码。尽管如此，大段 JavaScript 代码的问题可以通过将 JavaScript 代码存储在具有 `.js` 扩展的单独 JavaScript 源文件中来轻松解决。这清理了你的网页代码，因为 JavaScript 代码与 HTML 页面本身分开存储，留下了更整洁、更易读的网页。

由于 JavaScript 有网页臃肿的倾向，它对你网站的搜索引擎友好性可能非常不利。这是因为当搜索引擎访问你的网站并寻找优质内容和关键词以确定你页面的主题时，它最不想看到的就是几百行 JavaScript 代码。同样，这个问题可以通过将 JavaScript 代码整齐地存储在带有 `.js` 扩展的脚本文件中，并在 HTML 文档中链接到该文件来轻松解决。

JavaScript 是一种功能丰富且实用的浏览器脚本，如果使用得当，可以实现一些很棒的效果并提高用户的体验。它的使用也有缺点，即它倾向于使网页臃肿。要记住的关键点是在外部脚本文件中使用 JavaScript 代码来兼顾两者。这样，代码就与你的内容分离，你就可以获得 JavaScript 功能的所有好处，而不会产生相关代码臃肿的负面影响。

## JavaScript 的好处

对于初学者来说，JavaScript 和 HTML 这些词只是他/她可能听过的术语。假设这些初学者正在阅读这一部分，让我们从这些词的定义开始吧。HTML 代表超文本标记语言（HyperText Markup Language），它是“用于结构化网页的标签，以便浏览器可以显示它”。

同时，JavaScript 是“一种常用于为网页添加交互脚本语言”。

基本上，HTML 标签创建你放入页面中的内容，而 JavaScript 允许你操作这些内容。

那么，在 HTML 代码中使用 JavaScript 有什么好处？

1. JavaScript 将改进视觉显示。正如前面提到的，如果网页只有纯 HTML，它将只是一页文本。你将无法移动物体，也无法进入下一页。

2. JavaScript 将允许许多页面效果 JavaScript 允许的一些效果：

- 页面停留时间
- 弹出窗口和提示
- 折叠文本
- 页面超时
- 颜色变化和淡变
- 字体大小变化和淡变
- 终极淡变
- 嵌入音频
- 打印页面/元素
- 滚动横幅
- 飞行文字
- 新闻滚动
- 自动弹出
- 图像切换
- 切换按钮

3. JavaScript 将增加用户交互性 添加的特殊效果将网页更具交互性。你网站的用户会想要在网站内继续探索。

4. JavaScript 将提供用户插件的无缝集成 JavaScript 不仅提供了 HTML 对象的访问，还提供了对浏览器和平台特定对象（如浏览器插件 Adobe Acrobat、Media Player）的访问。



# 第二章

## JAVASCRIPT 与其他编码语言的区别

## JQUERY 与 JAVASCRIPT 的区别

作为一种极其受欢迎的客户端脚本语言，JavaScript 不再需要额外介绍。除了作为网页浏览器的一部分外，JavaScript 还可以控制网页浏览器、实现用户交互、促进异步通信，并向用户交付定制化内容。因此，大多数 Web 开发者使用 JavaScript 来减少构建大型或复杂网站所需的时间精力。Web 开发者还可以选择使用几个 JavaScript 框架来实现并加速 Web 开发。

jQuery 是一个广泛使用的跨平台 JavaScript 库。尽管是开源的，但 jQuery 非常易用、快速且简洁。jQuery 提供的 API 在主流网页浏览器中无缝运行。此外，功能丰富的 JavaScript 库让 Web 开发者更容易操作 HTML 文档、处理事件、创建动画、选择 DOM 元素以及构建 AJAX 应用。同时，jQuery 还可以利用 JavaScript 库的优势创建各种插件。

因此，现代 Web 开发者可以选择独立或并行使用 JavaScript 和 jQuery。然而，对于程序员来说，理解 JavaScript 和 jQuery 之间的一些主要区别也很重要。

## JAVASCRIPT 与 JQUERY 的四个重要区别

### 1. 编程语言与库

作为一种动态编程语言，JavaScript 支持面向对象、结构化、函数式和命令式编程风格。一类函数和动态类型也使 JavaScript 被基于基于原型的脚本语言。另一方面，jQuery 是一个 JavaScript 库。

框架让开发者更容易完成许多常见任务，如 HTML 文档操作、事件处理、动画、DOM 元素选择和 AJAX 应用开发。

### 2. 脚本时间

当 Web 开发者决定使用原生 JavaScript 时，他必须编写额外的代码来完成若干任务。他还需要在调试和修复浏览器兼容性问题上花费额外的时间和精力。但 jQuery 允许开发者利用现有的脚本。因此，他们可以使用 jQuery 中现有的脚本完成许多任务，而无需编写长行代码。因此，jQuery 让 Web 程序员更容易节省构建现代网站和互联网应用程序所需的时间精力。

### 3. 客户端脚本的简化

作为一种客户端脚本语言，JavaScript 让开发者更容易实现用户交互并向用户交付定制化内容。但开发者必须编写长行代码才能用原生 JavaScript 写 Web 应用。因此，Web 开发者经常使用 JavaScript 开发框架来简单快速地完成脚本功能。作为一个跨平台的 JavaScript 库，jQuery 带有执行常用脚本功能的特性。因此，开发者可以使用该库来简化 HTML 的客户端脚本。框架提供的插件、组件和 UI 帮助 Web 程序员大幅缩短开发时间。

### 4. 性能

JavaScript 和 jQuery 在最新的网页浏览器和计算机上运行都相当快。但 JavaScript 和 jQuery 的速度都会受到旧版网页器的的影响。由于 JavaScript 访问 DOM 比 jQuery 快，程序员可以轻松地减少与库相关的开销。然而，jQuery 通过独立于网页浏览器的功能，让开发者更容易构建高性能的网站和互联网应用程序。

总而言之，JavaScript 是一种动态且功能丰富的编程语言，而 jQuery 是一个 JavaScript 代码库。

精通 JavaScript 的开发者可以轻松地使用 jQuery 完成各种任务，而无需编写长行代码。然而，即使不精通这种流行的客户端脚本语言，他们仍然可以使用 jQuery。这就是为什么；开发者需要根据项目的特定需求选择 JavaScript 或 jQuery。

## 什么是超文本标记语言 (HTML)？

HTML 是网页浏览器用于动态格式化网页的格式化语言。它最初演变自标准通用标记语言 (SGML)，遵循了出版行业使用的许多标记规范。HTML 本身并不是一种编程语言，而是一种标记语言；它的初衷从未为了控制文档布局的所有方面，而是为了格式化页面内容。它使用的语法是使用尖括号包裹由关键词标识的标签，例如 `<title>`，这些标签可以组合起来来控制页面在浏览器窗口中的显示方式。早期的一个障碍是 20 世纪 90 代的不同浏览器以不同的方式解释这些代码。万维网联盟 (W3C) 的形成是为了引入某种程度的标准。

## W3C

W3C 为网页设计师制作了需要遵循的“建议”，其 Web 可访问性倡议（Web Accessibility Initiative）为让所有人（而不只是使用图形浏览器的人）访问网页提供了指南。它推荐了多种规范以确保 HTML 和 XHTML 之间易于迁移。

## XHTML

万维网的问题之一是有时很难找到你要的内容，因此 W3C 引入了 XML 作为部分解决方案。XHTML 是一种独立的语言，它是 HTML 4 和可扩展标记语言 (XML) 的结合。HTML 的语法允许许多 XHTML 不具备快捷方法，最明显的区别之一是在 XHTML 中所有标签必须闭合。

## 浏览器

过去几年发生的一个进展是通过使用层叠样式表 (CSS) 实现内容与布局的分离。不同的浏览器显示内容的方式仍然不同，当你在修复一个异常却遇到另一个异常时，这可能是令人恼火的。完全符合标准仍然是一个梦想，尽管浏览器差异之间的差距已大幅缩小。新兴技术的浏览器（如 Apple 的 iPad）带来了新的挫败；它不支持 Flash，但 Apple 的 Safari 浏览器（被 Google 适配为他们的 Chrome 浏览器）是第一个完全支持 HTML5 视频标准的浏览器之一。遗憾的是，不同浏览器更新渲染引擎的速度不同，浏览器用户更新软件的速度更不可预测，有些根本不更新。

## CSS

W3C 开发了如 CSS 和 XSL 等样式语言来帮助标准化呈现。层叠样式表 (CSS) 为 HTML 页面提供了一种简单的方法，允许设计师控制视觉和听觉特征；例如字体、边距、行间距、边框、颜色、层等。启发性的设计师 Shea 和 Holzschlag 创建了 CSS Zen Garden —— 一个致力于展示功能性、实用 CSS 的网站，而不是只有 2% 浏览用户可见的尖端技巧。

## JAVA IDE 比较：NETBEANS 与 ECLIPSE

与其他通用型编程语言不同，Java 被开发者广泛用于构建桌面、Web 和移动应用程序。但开发者经常寻找智能的集成开发环境 (IDE)、框架和工具，以便高效快速地编写 Java 应用程序。开发者可以进一步快速编写代码和


通过一系列 Java IDE 可以高效地工作。NetBeans 和 Eclipse 都是非常流行的 Java IDE。

尽管 NetBeans 是开源的，但它仍然是 Java 平台的官方 IDE。NetBeans 提供的功能和工具允许开发者使用 Java 8 构建各种桌面、Web 和移动端应用程序。除了 Java 之外，该 IDE 进一步支持多种技术 - HTML、CSS、JavaScript、PHP 和 C/C++。NetBeans 提供的编辑器、分析器和转换器进一步让程序员能够更容易将他们的遗留应用程序升级到最新的 Java 版本。

Eclipse 是用 Java 编写的，其设计具有简化 Java 应用开发的特性。开发者可以使用各种插件轻松地扩展 IDE。他们还可以通过使用特定的插件，将 Java 与其他流行的编程语言（包括 Ruby、Perl、PHP、Scala 和 Groovy）集成来开发应用程序。此外，Eclipse 也是一个开源 IDE，并受到活跃社区的支持。因此，对于开发者来说，根据关键特性和功能比较 NetBeans 和 Eclipse 是至关重要的。

## 了解 NETBEANS 和 ECLIPSE 之间的重要差异

### Java 8 支持
Java 8 版本带了许多新功能和增强，包括 lambda 表达式、新的日期/时间 API 以及集成的 Nashorn JavaScript 引擎。因此，许多开发者倾向于在 Java 8 中编写应用程序，以利用 Java 8 的新特性。

NetBeans 是官方 Java IDE，完全支持 Java SE8。另一方面，Eclipse 通过 Eclipse Java 编译器 (ECJ) 实现了新的 Java 8 语言增强。开发者必须遵循一系列步骤才能充分利用 Java 8 提供的新语言特性。

### Java 8 迁移
Oracle 建议 Java 开发者使用 NetBeans。因此，NetBeans 在最新 Java 版本发布后几乎立即就能提供支持。此外，它还提供了一系列工具，让开发者更容易地将其遗留应用程序迁移到最新的 Java 版本。开发者可以使用 NetBeans 提供的代码编辑器、分析器和转换器，快速平稳地将他们的应用程序迁移到 Java8。但 Eclipse 没有提供任何健壮的工具来简化 Java 8 迁移。

### 插件数量
在插件类别，Eclipse 优于 NetBeans。许多开发者选择 Eclipse，通过利用其提供的插件轻松地为应用程序添加功能。然而，开发者通常需要为 Eclipse 使用多个第三方插件。这些第三方插件的质量和性能各不相同。另一方面，NetBeans 允许用户使用一组稳定且高质量的插件。

### 用户界面
NetBeans 的用户界面基于 Swing 设计，而 Eclipse 的用户界面基于 SWT 设计的。Swing 是一个 Java 原生轻量级工具包，而 SWT 是用于系统底层工具的 Java 工具。许多开发者发现 NetBeans 的用户界面比 Eclipse 的界面更简单、更友好。NetBeans 简单的用户界面进一步让初学者更容易学习和使用该 IDE，而无需花费额外的时间精力。Java 程序员则需要花费额外的时间精力高效地使用 Eclipse 工作。

### 配置
NetBeans 带有多个内置开箱即用（out-of-box）功能。这些开箱即用功能使用户能够快速配置 IDE 并无延迟地完成基础编程任务。但 Eclipse 没有许多开箱即用的功能。用户必须安装并配置 Eclipse 插件才能完成常见任务并高效地构建应用程序。这些插件让初学者很难在短时间内配置和使用 IDE。

### 与其他编程语言协作
这两个 Java IDE 都允许开发者与其他流行的技术和编程语言协作。NetBeans 除了 Java 之外还支持 HTML、CSS、JavaScript、PHP 和 C/C++。同样，Eclipse 允许程序员将 Java 与多种流行的编程语言集成，包括 Python、Perl、PHP、Groovy 和 Scala。但 NetBeans 被设计为基于工具的 DE，允许程序员通过特定项目与其他技术协作。因此，Java 开发者发现使用 NetBeans 与其他编程语言工作更加容易。

### 对 Maven 的支持
NetBeans 和 Eclipse 都支持 Maven - 一种常用的项目管理工具。Maven 提供的完整构建生命周期框架让程序员更容易自动化整个构建基础。但许多程序员发现使用 NetBeans 时处理 Maven 更容易。他们可以直接在 NetBeans 内部运行 Maven 目标。同样，他们可以使用控制台直接在 NetBeans 中查看 Maven 命令的输出。NetBeans 进一步让用户更新 Maven 依赖、启动 Maven 构建和创建新的 Maven 项目变得更容易。

### Android 应用开发
Java 语言广泛用于开发 Android 移动应用 - Android 是全球市场最大的移动平台。各种网站发布的统计数据显示，大多数 Android 应用开发者倾向于 Eclipse 而非 NetBeans。除了简单快速之外，Eclipse 还提供了一个标准的 UI 工具包 Swing，它可以无缝集成到 Android 应用程序中。此外，Eclipse SDK 提供的各种插件让开发者更容易构建健壮的 Android 应用，而无需花费额外的时间精力。然而，NetBeans 也提供了若干功能和工具来简化 Android 开发。

### 源代码格式化
这两个 Java IDE 都具有自动格式化 Java 编写应用程序源代码的能力。但许多程序员发现 Eclipse 提供的 Java 代码格式化器比 NetBeans 提供的格式化选项更高效。在使用 Eclipse 时，程序员可以通过快捷键 C-S-F 直接调用 Java 代码格式化器。因此，他们可以以灵活高效的方式格式化 Java 代码。

总的来说，NetBeans 和 Eclipse 都是开源且跨平台的 Java IDE。但 Eclipse 受到 IBM 支持，而 NetBeans 受到 Oracle 支持。每个 IDE 都提供了多项创新功能和工具，以简化并加速 Java 开发。但开发者必须根据特定需求评估每个 IDE 的优缺点。

## JAVASCRIPT 与 AJAX

JavaScript 是一种客户端脚本语言。当你打开网页时，浏览器首先从服务器下载必要的文件以正确显示页面。这些必要的文件包括 HTML、CSS、图像、视频以及 JavaScript 文件。下载完成后，浏览器显示页面并运行与其关联的脚本。

在 AJAX 技术中，通过 JavaScript 向服务器发送用户输入和其他数据。JavaScript 创建 XMLHttpRequest 连接服务器，向其提交数据并请求响应。当响应返回时，触发一个 JavaScript 事件，并执行与事件相关的函数。因此，在 AJAX 技术中，JavaScript 仅用于在客户端和服务器之间传输数据，而主程序在服务器端执行（使用 PHP 或任何服务器端语言）。由于 JavaScript 从客户端计算机运行，其执行时间非常短，几乎是瞬时的。观众也可以在不连接服务器的情况下运行 JavaScript。但在 AJAX 中，观众必须连接服务器。这里的执行时间要长得多，取决于网络连接速度、服务器硬件以及客户端与服务器之间传输的字节数。



JavaScript 仅用于某些对数据安全不是重要考虑的特定应用程序，而 Ajax 技术的应用范围是无限的。

# 集成 JAVASCRIPT 和 ORACLE FOR

任何在 JavaScript 中编写的代码都将与你的网页以及在用户浏览器中运行的脚本一起交付，而不是直接运行在提供网页的服务器上。因此，整个用户体验将变得更加流畅和快速。

这种编程语言通常用于创建网站与访问者之间的交互，并开发一种不仅限于访问网站的参与度。JS 也用于嵌入式硬件控制和服务器。

这就是为什么这种语言被认为是强大的原因。JavaScript 被认为是一种丰富且实用的基于器的脚本，因为它不需要安装；它直接内置在网络浏览器中！

你可能经常看到“JavaScript”和“网络浏览器”一起使用，但“JavaScript”和“Oracle Forms”又是什么？

## Oracle Forms 应用

让我们简单聊聊 Oracle Forms。

Forms 是一个强大的开发和运行环境，已用于为组织构建关键任务应用程序。

企业通过将 Oracle Forms 以及其他遗留应用程序与 JavaScript 集成可以受益匪浅。这种集成有助于企业和组织将各种应用程序统一到一个桌面应用中，通过简化业务流程、消除冗余数据输入和降低维护成本来提高准确性和效率。

想象将 Forms 操作简化为自动化的任务序列！

当 Oracle 引入 Java 导入器以及 Java 6i 版本时，它使得调用 Java 中的类成为可能，并允许 Forms 调用 Web 服务。

毫无疑问，技术的这些改进帮助 Oracle Forms 摆脱了相对隔离的状态。在引入 itg 之前，Forms 无法运行任何功能，除非用户的操作触发了它们。

## JavaScript 和 Oracle Forms

但通过 JavaScript 和 Oracle Forms 的集成，一套新的功能减轻了 Forms 开发人员的压力。Oracle Forms 现在处于即使在没有用户触发的情况下也能反应的位置。它们现在不仅与客户端 JavaScript 交互；还可以根据高级队列（Advanced Queuing）消息进行交互。

运行所有应用程序的表 applet 现在可以通过 JavaScript 与周围的其他网站通信。Web 开发人员现在可以将他们的表单嵌入 HTML 页面中。你的 Forms 应用程序现在可以通过 JavaScript 集成与 Google Maps、电子商务平台等现代 API 进行交互。

由于新的市场压力，让更多遗留应用使用 JavaScript 已已成为必要。JavaScript 能够增强遗留应用程序前端提供的交互性，这有助于提高用户友好性和有效性，同时帮助企业跟上最新的以 Web 为核心的市场趋势。

# 第三章

## JAVASCRIPT 中的核心工具

作为一种简单且多功能的客户端脚本语言，JavaScript 让 Web 程序员更容易让网站和互联网应用程序更加用户友好和具有交互性。JavaScript 代码在用户的计算机上执行。因此，开发者可以使用 JavaScript 为网站访问者提供更好的用户体验，而不会给 Web 服务器带来任何额外压力。然而，Web 开发人员仍然需要使用各种 JavaScript 工具来优化网站性能，而无需编写长长的代码。

2015 年 Web 开发人员必须使用的七种**核心 JAVASCRIPT 工具**

- 1. Meteor

Meteor 让 Web 开发人员更容易在超简单的环境中创建现代网站和互联网应用。该框架的设计特性使 Web 应用程序开发变得简单、方便和快速。目前，Meteor 支持 Linux 和 Mac OS X。然而，Meteor 社区已提供多种选项，让 Windows 用户可以使用该框架。社区提供的插件也让程序员更容易在不编写额外代码的情况下优化网站的功能和性能。

- 2. Epoch

如今，互联网应用程序广泛使用图表以一种令人印象深刻且引人注目的方式向用户展示信息。Epoch 让 Web 开发人员更容易在他们的应用程序中扩展和采用各种图表。目前，Epoch 有五种实时图表，如面积图、折线图、饼图、柱状图和散点图。这些漂亮且高性能的图表可以使用 CSS 查询引擎进一步自定义。

- 3. Hitch

Hitch 是一个小型 JavaScript polyfill 引擎，可以轻松包含在任何网页中。Web 开发人员可以使用 HTML 和 CSS 的扩展。它通过使 CSS 选择器更具表达力，让程序员保持 HTML 代码清洁。Hitch 让程序员更容易决定所需的功能，而无需担心最终用户使用的网络浏览器。

- 4. Radio app

Radi 帮助 Web 程序员为现代网站和互联网应用创建视频、动画和实时图形。它带有功能，允许开发者使用 HTML5 特性创建各种内容。HTML5。

- 5. JSHint

Web 开发人员仍然需要使用各种 JavaScript 工具来优化网站性能，而无需编写长长的代码。

- 6. 交互地图

为了提供本地化体验，现在大多数网站都使用动画。

- 7. JavaScript 响应式扩展 (RxJS)

现代网站需要高度。

## 如何在你的浏览器中启用（和禁用）JAVASCRIPT

今天，大多数网站都需要一些（或大量）JavaScript，如果你禁用了 JavaScript，那么在你喜欢的网站上不太可能获得很大成功。

当然，有些时候你只想直接处理网站的功能，如果是这样，禁用 JavaScript 可能是你倾向于做的事。幸运的是，无论你是启用还是禁用 JavaScript，都可以在所有浏览器的同一个位置轻松地完成。

## 在 INTERNET EXPLORER 中启用或禁用 JAVASCRIPT

Internet Explorer 有有一项很好的功能，可以简单地更改设置，其中包含 JavaScript 选项。

- 1. 在 IE9 窗口中，点击右上角的设置菜单（它看起来像一个齿轮）。一旦设置菜单出现，选择底部的“Internet 选项”。

- 2. Internet 选项菜单会出现。在此菜单中，点击“安全”选项卡标题。安全选项卡将打开。

- 3. 在安全设置底部的框中，有一个“自定义级别”按钮。点击该按钮以打开更多安全功能。

- 4. 在自定义安全设置框内，向下滚动直到找到列出“脚本”的区域。由于选项是按区域字母顺序排列的，该区域位于列表末尾。

系统可能会提示您确认更改，如果出现该框，请在其中选择“是”。

当返回“设置”框时，最后点击一次“确定”以完成对系统的更改。如果您刚刚开启了 JavaScript 设置，您应该能够刷新正在操作的网页，并看到脚本正常运行。相反，如果您刚刚禁用了 JavaScript，那么在刷新页面时，预计您的网页将会失去功能。

## 在 FIREFOX 中启用或禁用 JavaScript

在 Firefox 中禁用或启用 JavaScript 同样简单。要更改 Firefox 内部的 JavaScript 设置，请先点击屏幕左上角的 Firefox 按钮。

- 1. 打开 Firefox 菜单后，选择“选项 (Options)”，然后再次选择“选项 (Options)。（如果您启用了菜单栏，将不会看到巨大的橙色 Firefox 按钮。相反，请点击“工具 (Tools)”然后“选项 (Options)”。）

- 2. 在选项菜单中，您会看到各种选择的选项卡。打开“内容 (Content)”选项卡，然后查找与 JavaScript 相关的选择。

- 3. 在 Firefox 选项的“内容”部分，“启用 JavaScript (Enable JavaScript)”文字旁边有一个复选框。勾选该框以启用 JavaScript 让其在浏览器中运行，或根据需要取消勾选以关闭 JavaScript。

- 1. 在适当勾选或取消勾选后，点击“确定 (OK)”关闭选项菜单。

刷新您的网页。如果您勾选了启用 JavaScript，页面现在将正常工作。如果您取消勾选了框（实际上禁用了 JavaScript），您正在查看的可能会可能会某些功能，并可能无法正常运行。要重新开启 JavaScript，只需重新访问选项菜单并再次勾选该框即可。

## 在 GOOGLE CHROME 中启用或禁用 JavaScript

由于 Chrome 是一个极简浏览器，启用或禁用 JavaScript 只需要找到正确的菜单选项并对设置进行快速更改。要为此，您首先需要识别代表菜单的符号。

- 1. 在 Chrome 窗口的右上角，寻找一个像三条水平线的符号。点击此按钮将出现菜单列表。点击列表底部的“设置 (Settings)”。

- 2. 打开设置菜单后，滚动到底部并打开“显示高级设置 (Show Advanced Settings)”。寻找名为“隐私 (Privacy)”的类别。在该下方，有一个“内容设置 (Content Settings)”按钮。点击“内容设置”框将出现一个新窗口。

- 3. 在出现的窗口中，您将看到可以操作的选项列表。寻找 JavaScript 设置。

- 4. 一旦找到 JavaScript 设置，您就有两个选择。要在 Chrome 中启用 JavaScript，只需点击显示“允许网站运行 JavaScript (Allow all sites to run JavaScript)”的地方。如果您不想启用 JavaScript，则可以通过点击“不允许任何网站运行 JavaScript (Do not allow any sites to run JavaScript)”的选项来禁用它。

在 Chrome 中无需点击“确定”或“保存”，因为您的选项会自动保存到浏览器中。事实上，您可以通过刷新正在查看的网站来立即测试您的新更改。如果页面丢失所有横幅和功能，则 JavaScript 可能已被禁用。如果页面运行正常，但在在此之前一直不正常，说明您已重新启用了 JavaScript。

# 第四章

## JavaScript 编程语言的强大特性

在网页开发者和上网用户社区中，JavaScript 作为浏览器的客户端脚本语言非常受欢迎。在任何 Web 应用中，JavaScript 可用于实现简单的功能（如图像悬停），以及使用 ajax 发起异步请求。几年前当 Flash 还不流行时，JavaScript 被广泛用于为网页添加精美效果，现在仍被用于同样的目的。让我们来看看该语言的一些特性。

- 1. 浏览器支持：要访问 Flash 内容，您需要在浏览器中安装 Flash 插件。但要使用 JavaScript，您完全不需要任何插件。这是因为所有浏览器都接受 JavaScript 作为脚本语言并为其提供集成支持。您需要做的就是妥善处理某些依赖于客户端浏览器 DOM（文档对象模型）的任务。

- 2. 既可用于客户端也可用于服务器端：由于 JavaScript 可以访问浏览器的文档对象模型，您实际上可以在运行时更改网页的结构。由于此，JavaScript 可用于为网页添加不同的效果。另一方面，JavaScript 也可以在服务器端使用。例如，在流行的开源企业内容管理系统 Alfresco 中，JavaScript 用于创建网络脚本（webscripts）。这使得为 Alfresco 添加自定义任务变得非常简单。

- 1. 浏览器支持：要访问 Flash 内容，您需要在浏览器中安装 Flash 插件。但要使用 JavaScript，您完全不需要任何插件。这是因为所有浏览器都接受 JavaScript 作为脚本语言并为其提供集成支持。您需要做的的就是妥善处理某些依赖于客户端浏览器 DOM（文档对象模型）的任务。

- 2. 既可用于客户端也可用于服务器端：由于 JavaScript 可以访问浏览器的文档对象模型，您实际上可以在运行时更改网页的结构。由于此，JavaScript 可用于为网页添加不同的效果。另一方面，JavaScript 也可以在服务器端使用。例如，在流行的开源企业内容管理系统 Alfresco 中，JavaScript 用于创建网络脚本（webscripts）。这使得为 Alfresco 添加自定义任务变得非常简单。



优点：拥有强大的社区和深远的影响。

缺点：基于字符串的奇特继承模型。控制器与视图过于接近，且缺乏绑定。即使它的名字听起来也十分通用。

### 8. Google Web Toolkit:

GWT 是一个真正的客户端工具包，不仅仅是一个框架。它将 Java 编译为 JavaScript，同时支持标准 Java 库的子集。它曾被 Google 内部用于 Wave。

- 优点：功能丰富的框架，社区强大。它拥有稳健的基于 Java 的组件继承模型。非常适合大型客户端应用。

- 缺点：Java 显然已经从列表中移除，并启动了如 DART 等计划。Java 在客户端的抽象显得有些生硬。

### 9. Google Closure:

Google Closure 不仅仅是一个工具包和简单的 JavaScript 框架。它包含一个编译器和一个优化器。

- 优点：主要的 Google 应用都使用了 Google Closure。它配备了一个简单的基于组件的 UI 组合系统。

- 缺点：缺乏 UI 绑定支持。

### 10. Ember.js:

Ember.js 以前被称为 SproutCore 2.0，旨在将 SproutCore 2.0 的核心功能提取到更适合 Web 的紧凑模块化框架中。

- 优点：真正丰富的模板系统，具有组合的视图和 U 绑定。

- 缺点：非常新，且缺乏大量文档支持。

### 1. Angular.js:

这个优秀的框架，由……创建，包含了有趣的设计选择。

- 优点：设计非常好，具有模板作用域和控制器设计方面的长。它拥有一个依赖注入系统。它还提供了丰富的 UI 绑定语法支持，以方便过滤和转换值。

- 缺点：代码库有些臃肿，视图也不够模块化。

### 2. Batman.js:

Batman.js 由 Shopify 开发，类似于 Knockout 和 Angular。它具有健壮的 UI 绑定系统，基于 HTML 属性。它使用地道的 CoffeeScript 编写。与 Node.js 紧密集成，还提供了自己的（并非必要的）Node.js 服务器。

- 优点：提供了整洁的代码库，并在绑定、持久化和路由方面采用了简单的方法。

- 缺点：由于它基于 Knockout，在处理嵌套组件时，它与 Knockout 和 Angular 具有相同的缺点。

简单来说，Ember.js 是唯一提供开发者所需一切的框架。尽管它存在细微的性能问题，但它交付了卓越的代码库。凭借强大的社区，这个框架应该是你的列表首选。

# 第五章

## 开始学习语言

在开始学习新语言之前，你对 HTML 和主体区域有基本的了解，并掌握一些用于添加图像、插入链接、在超文本语言中创建段落的简单语句。用于编写 JavaScript 的软件是基础文本编辑器。Windows 用户可以使用 Notepad 或 Notepad++，Mac 用户可以使用 TextEdit 或 TextWrangler。代码需要网络浏览器（首选 Mozilla Firefox 或 Google Chrome）来成功编译和运行。

### 入门教程

一个在 JavaScript 中打印自定义消息的简单程序，如下所示：

```html
<html>
<head>
<title>JavaScript example</title>
<script language="JavaScript">
document.write("My First JavaScript Program!");
</script>
</head>
```

```html
<body> Hello World! </body>
```

```html
</html>
```

在上述代码中使用 `<!--` 和 `-->` 可以确保代码不会被不支持 JavaScript 的旧版本浏览器显示。这确保了页面在不支持的浏览器上不会发生故障。

就像任何其他 HTML 文件一样，你只需要将上述代码复制粘贴到你的记事本文档中，然后将其保存为“.html” 扩展名。保存完成后，只需右键点击文件并选择“打开方式”。在这里，选择网络浏览器（可用 Mozilla Firefox）。代码将自动执行，结果将显示在浏览器窗口中。

### 注意事项

- JavaScript 代码大部分放在 html 的 "head" 部分，你甚至可以在 "body" 区域使用它们。

- JavaScript 代码通常以标签 `<script language="JavaScript">` 开始，以 `</script>` 结束。

- JavaScript 总是被嵌入到 HTML 代码中，永远无法独立存在。

## 警告消息框

如果你想为网站添加自定义的警告消息框，可以使用 JavaScript 轻松实现。添加自定义警告框的代码如下。

```html
</body>
```

```html
<script>
```

```html
window.alert("My First JavaScript Program!");
</script>
</body>
```

同样，你还可以添加其他警报，例如：

## 确认

window.alert("Are you sure you want to exit?");

## 提示

window.alert("User field cannot be left.");

### 在 JavaScript 中编写的另一种方式

正则表达式 (RegExp) 非常有用且强大。……JavaScript。如果你对……感到沮丧

到目前为止，我们指定的字母范围 [A-Z] 和数字范围 [0-9]。在正则表达式中编写范围有多种方法。你可以指定范围 [abc] 来匹配 a 或 b 或 c。你也可以指定范围 [^abc] 来匹配任何不是 a、b 或 c 的内容。

## 2. 原型型 JavaScript

如果 JavaScript 也有类似的功能，那该有多好啊。惊讶的是，许多开发者并没有意识到 JavaScript 也是一种原型型编程语言。这意味着你可以创建自己的 JavaScript 弱类型对象，并将其嵌入自己的函数以及属性。

是这样吗？是的。让我来详细解释一下。我们都熟悉我们喜爱的 String 对象（字符串对象）。假设我声明了如下一个变量：

```javascript
var someString = new String();
```

现在，我可以使用 `someString` 这个 `String` 类型对象所暴露的丰富方法。

例如

someString.length 将给我该对象中存在的字符数量。

我们可以看到，JavaScript 本质上已经托管了许多对象，这些对象通过实例渲染不同的方法和属性。

掌握了这些知识，让我们尝试弄清楚我如何创建一个自己的类似于 String 对象的对象。

我们的场景是创建一个员工对象，该对象暴露以下属性：

```javascript
mp.name;
mp.age;
mp.skills;
```

要创建一个像这样的对象，我们必须使用以下语法。

```javascript
function Employee(name,age,skills){
  this.name = name;
  this.age = (isNaN(parseInt(item))?0:age;
  this.skills = skills;
}
```

我如何像这样轻松地实例化一个 `Employee` 类型的对象

```javascript
function testEmployee(){
  var myEmployee.prototype.status = null;
  var emp = new myEmployee("Joe",25,"average");
  emp.status="fired";
  var emp2 = new myEmployee("Mary",25,"good");
  emp2.status="detained";
  alert(emp.name + " is " + emp.status + " because he is " + emp2.skills);
  alert("Hi " + emp2.name + " you are in, because you are " + emp2.skills);
}
```

"prototype" 允许我扩展员工对象显示额外的字段 "status"。所以你会发现，当你有一个现有的对象并想要扩展它以渲染其他功能时，这非常有用。

当你运行此示例时，你会看到一个弹窗，显示消息 "Joe is fired because he is average" 和 "Hi Mary you are in because you are good"

# 第六章

## JavaScript 错误

对于大多数计算机用户来说，JavaScript 是一种奇怪的 PC 术语。除了 PC 专业人员程序员外，大多数人对它一知甚少。本质上，JavaScript 是一种 Web 开发语言，最常用于网站。JavaScript 因其易于使用的特性而在非程序员中非常受欢迎，它还允许脚本访问其他应用程序中的对象。

然而，JavaScript 错误也相当常见，很大程度上是因为许多业余爱好者在使用它编写 Web 程序。但糟糕的是，它也可以用于编写广告软件和间谍软件，这些软件会进入你的电脑，通常在你没有察觉的情况下，从而阻塞注册表。这反过来会减慢电脑速度，甚至可能导致其崩溃，我们都知道这意味着多大的头疼问题。

常见的 JavaScript 错误如下：

- 浏览器中未启用 JavaScript。
- 网页包含 JavaScript 编程错误。
- 浏览器不支持 JavaScript 技术。

我们可以做什么来处理这些问题？当然，你可以选择向 Web 管理员报告问题，并提供你收到的 JavaScript 错误消息的所有细节，但你有一个更简单的替代方案。只需清理你的 Windows 注册表，看着问题消失即可。

对于不知道的人来说，Windows 注册表是一个巨大的数据库，你在系统上使用的所有程序（包括 Windows 本身）都存储了大量数据。因此，每当你更改控制面板设置、文件关联、系统策略或安装新软件时，更改就会反映在注册表中。所以注册表实际上监控着你系统的行为，除非你定期使用注册表清理工具保持注册表干净，否则你无法避免 JavaScript 错误消息。

## 不同类型的 JavaScript 错误

在浏览网页时遇到 JavaScript 错误可能会令人烦恼，因为你会经历冻结和崩溃，这会干扰你平静的浏览。那么我们最初为什么会遇到错误呢？JavaScript 成了网站，所以当我们遇到 JavaScript 错误时，可能是某个网页中的 JavaScript 代码出了问题。

所以你必须熟悉两种类型的 JavaScript 错误：

- 1. 语法错误。意味着代码中存在拼写错误或可能缺少字符，导致了错误的发生。此错误在页面加载时出现。
- 2. 运行时错误。发生在未找到指定对象或脚本无法完成指令时。此错误在受影响的代码运行时出现。

错误消息以小图标的形式出现，你可以点击它进一步检查错误消息。那么你如何修复 JavaScript 错误呢？

问题可能出现在你的浏览器上，因为不同的浏览器对你访问的每个网站反应不同，所以尝试切换到不同的互联网浏览器。

如果无效，访问 Java 网站 java.com 进行测试检查 Java 安装是否正常。寻找跳动的公爵（dancing duke）。如果你能看到它，说明它运行正常。

如果你没有看到跳动的公爵，说明 Java 安装未正常。对于 Internet Explorer 用户，通过转工具、Internet 选项、安全来启用 Java。



# 第七章

## 必须掌握的核心编程语言

我们经常从希望进入 IT 行业的人那里听到的最常见的问题之一：“我需要了解哪些编程语言？”显然，这是一个复杂的问题，答案取决于你想要进入哪个领域。然而，已经在 IT 行业的人知道，你所拥有的最大技能就是成为一个**全才****。得益于对多种编程语言的广泛了解，准备充分的员工只需经过极少的培训就能在不同的计算机编程工作之间切换。

正因如此，这个问题的快速答案是：“学会的语言越多越好。”当然，如果我们花时间去学习每一种编程语言，我们实际上永远无法获得收入！这份列表涵盖了试图进入 IT 行业的人应该掌握的最核心的计算机编程语言。

### 1. HTML、CSS 和 JavaScript

这三种不同的语言被列在一起，是因为它们构成了绝大多数网站代码。由于互联网现在已成为全球通信的主要手段，网页设计和开发领域将永远存在。HTML、CSS 和 JavaScript 在许多方面都是相似的，但它们在改进网站功能方面各自侧重。

HTML 代表超文本标记语言（Hyper Text Markup Language），是网站的基础语言。HTML 用于在网页上插入图像、链接、基础格式和内容。它是最容易学习的编程语言之一，通常也是职业 IT 人士学习的第一门语言。

CSS 是 HTML 的自然扩展，为网站引入了更多功能。CSS，级联样式表（Cascading Style Sheets），通过让单个网页调用独立的代码来确定页面上的元素，允许创建具有固定格式的复杂网站。这使得代码更加简洁，并实现了布局与内容的分。

JavaScript 允许网页进行客户端交互，并被设计为与 HTML 和 CSS 无缝融合。文本框、按钮和弹出窗口都是 JavaScript 的功能。

### 2. Java

Java 在许多方面与 JavaScript 相似，但实际上它们之间没有关系。它是一种面向对象的语言，有许多用途，设计得既直观又稳定。Java 的通用性和广泛应用使其对开发者非常有用，几乎找不到一个对它了如指掌的成功程序员。

Java 常见于网络 Applet，在那里它可以运行比 JavaScript 更高级的 GUI。许多在线游戏通过 Java 运行。它并不是特别快速或强大的语言，但它几乎可以完成任何事情，并且在不同的机器和操作系统之间几乎通用。因此，它是每位 IT 工作者都应该知道的编程语言。

### 3. C 和 C++

这两种语言是今天仍被广泛使用的经典。C 语言于 20 世纪 70 年开发，用于系统编程。然而，由于其高效性和通用性，它很快在消费级软件中也流行起来。

C++ 设计于 1983 年作为 C 语言的扩展。它现在是最流行的编程语言之一，可以用于几乎所有的应用程序。作为在使用的开发最完善、最强大的编程语言之一，了解它对 IT 工作者来说是关重要的。如果你只能学习一种语言，请学习 C++。

### 4. PHP

PHP 是一种服务器端语言，允许创建交互式网页。它被设计为使用标签，因此与网页的基础 HTML 集成。这听起来与 JavaScript 相似，但关键区别在于 JavaScript 仅在客户端运行。在许多情况下，通过服务器进行交互是理想的，而这正是 PHP 发放异彩的地方。PHP 与 Java 配合良好，使得在代码中调用 Java 方法变得更容易。

结合与许多类型数据库的兼容性，很容易看出为什么 PHP 应该出现在每个程序员的武器库中。

# 第八章

## 如何学习编程语言

上述语言通常足够在 IT 行业起步，但你可能还会遇到其他几种语言。Ruby、Perl 和 Python 都在高级项目中被广泛使用，所以如果你有时间，它们非常值得研究。而且，特定的任务可能需要现有的众多编程语言中的任何一种。

一名专业 IT 工作者需要掌握的语言数量可能会让人望而生畏。并不是每个人都有时间或金钱接受正规教育，而网络上的免费资源往往难以遵循、不准确或不完整。不要让自己在这个竞争激烈的行业中落后。今天就开始温习你的编程语言吧！

# 结论

JavaScript 基本上是由网景（Netscape）公司创建的一种编程语言。这种语言在最近几个月获得了相当大的关注，因为它允许 Web 开发人员修改浏览器行为以及网站内容，而这是使用传统的 HTML 工具甚至 CSS 无法实现的。在页面上使用 JavaScript 使开发者能够控制页面对用户特定操作的反应和行为、检查文档元素、在提交之前验证表单选项、为页面添加日期和时间，甚至嵌入简单的微游戏。一旦你掌握了 OOP（面向对象编程）概念的基础知识，这门语言就很容易学习和理解了。
