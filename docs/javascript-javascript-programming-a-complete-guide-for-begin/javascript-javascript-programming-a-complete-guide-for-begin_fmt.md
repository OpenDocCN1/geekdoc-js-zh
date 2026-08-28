
# JavaScript 编程：初学者掌握并成为 JavaScript 编程语言专家完整指南

**作者：Brian Draper**

## JavaScript 编程简介

JavaScript 是一种客户端编程语言，其处理引擎嵌入在 Internet Explorer、Netscape、Firefox 等网络浏览器中。这使得处理引擎在浏览时能够读取和解释包含 JavaScript 代码的网页。

JavaScript 首次于 1995 年出现，尽管当时它被称为 Livescript。这个名字后来被更改为 JavaScript。

JavaScript 的发明是为了为 HTML 页面添加更多令人兴奋的功能。HTML 本身相当无聊，除了制作网页之外它做不了什么。相比之下，JavaScript 编程可以提供许多令人兴奋的功能，如计算、允许用户与网页交互、执行验证、操作网页上的元素、提供出色的视觉效果、启用动态功能等。

所有这些功能都为网站用户提供了增强的用户体验。因为 JavaScript 是一种客户端语言，所有这些功能都可以实时可用，而无需浏览器一直引用服务器。这防止了时间延迟并增加了用户的满意度。

JavaScript 基本上是由 Netscape 公司创建的一门语言。该语言在最近几个月里获得了相当大的流行，因为它允许 Web 开发人员修改浏览器行为以及网站内容，而这些是使用传统的 HTML 工具甚至 CSS 无法完全实现的。在网页上使用 JavaScript 使得开发者能够控制其页面如何对用户的特定操作做出反应和行为、检查页面上显示的文档元素、在提交之前验证表单选项、检查原生浏览器详情、为特定操作设置 Cookie、为页面添加日期时间，甚至在网站中嵌入简单的微游戏。一旦你有了 OOP（面向对象编程）概念和 HTML 的基础知识，这门语言很容易学习和理解。

## 需要的软件和知识

在开始学习新语言之前，你必须对 HTML 的 head 和 body 区域有基本的了解，并掌握一些用于添加图像、插入超链接、在文本语言中创建段落的简单语句。你可以用于开始 JavaScript 之旅的软件是基础文本编辑器。Windows 用户可以使用 Notepad 或 Notepad++，Mac 用户可以使用 TextEdit 或 TextWrangler。代码需要一个网络浏览器（首选 Firefox 或 Google Chrome）才能成功编译和运行。

## 入门之旅

一个在 JavaScript 中打印自定义消息的简单程序看起来如下：

```html
<html>
<head>
<title>JavaScript example</title>
<script language="JavaScript">
<!--
document.write("My First JavaScript!");
-->
</script>
</head>
<body> Hello World! </body>
</html>
```

在上述代码中使用 `<!--` 和 `-->` 确保代码不会被不支持的旧版本浏览器显示。这确保了页面在不支持的浏览器上不会发生故障。

与其他任何 HTML 文件一样，你只需要将上述代码粘贴到 Notepad 中，然后以 `.html` 扩展名保存。保存完成后，只需右键点击文件并选择“打开方式”。从这里选择一个网络浏览器（如果有 Mozilla Firefox）。代码将独立运行，结果显示在浏览器窗口中。

## 注意事项

JavaScript 代码大多位于 HTML 的 `head` 部分，但你也可以在 `body` 区域使用它们。

JavaScript 代码通常以标签 `<script language="JavaScript">` 开始并以 `</script>` 结束。

JavaScript 代码始终嵌入 HTML 代码中，不能独立存在。

## 警告框

如果你想为网站添加自定义警告框，可以使用 JavaScript 非常方便地实现。添加警告框的代码如下：

```html
<body>
<script>
window.alert("This is JavaScript Alert Box!")
</script>
</body>
```

同样，你可以添加其他警告，例如：

1. 确认操作

`window.confirm("确定要离开此网站吗？")`

2. 提示操作

`window.prompt("用户名字段留空。")`

让我们更深入地查看使用 JavaScript 编程可以实现的各种功能：

## 执行计算

JavaScript 可用于执行从简单到高级的数学计算。如果你希望用户通过输入某些需要进行计算的信息与你的网站进行交互，并根据结果显示相关内容，这就会尤为有用。例如，如果用户在网站上输入了所需的贷款金额，JavaScript 可以计算贷款还款并显示适当的结果。此外，JavaScript 还可以显示日期和时间、为某些活动计时并执行复杂的日期计算。

## 用户交互

网页上的 JavaScript 可以接收用户的交互，并通过事件执行特定功能。一些最受欢迎的事件包括：

- `onblur`
- `onchange`
- `onclick`
- `ondblclick`
- `onfocus`
- `onkeydown`
- `onkeypress`
- `onkeyup`
- `onload`
- `onmousedown`
- `onmousemove`
- `onmouseout`
- `onmouseover`
- `onmouseup`
- `onselect`
- `onsubmit`

## 执行表单验证

JavaScript 可以验证和检查用户输入，以确定其是否符合某些要求。例如，你可以检查某个字段是否为空、电子邮件地址格式是否正确、邮政编码格式是否正确等。在大多数情况下，如果网站访问者犯了错误，可以通过警告（`alert`）向他们显示适当的错误信息。

## 操作网页上的元素

JavaScript 允许通过上述事件，在用户交互时更改网页的内容或样式。例如，悬停在某些文本上可以使图像出现，提交按钮上的文字可以在提交时发生变化等。

## 提供视觉效果

JavaScript 拥有许多方法为网页提供视觉效果，而其他服务器端编程语言无法做到。一个典型的例子可能是一些酷的图像悬停按钮。

## 启用动态功能

JavaScript 同 AJAX（异步 JavaScript 和 XML）可用于创建动态应用程序。其中一个示例是在不刷新页面的情况下向网页加载动态内容。

## JavaScript 可以处理大型企业应用吗？

根据 W3Techs.com 发布的最新使用统计，超过 91% 的网站使用 JavaScript 作为客户端编程语言。还有许多程序员倾向于使用 JavaScript 同时编写客户端和服务器端代码。然而，开发者必须依赖 Node.js 等框架来使用 JavaScript 进行服务器端开发。JavaScript 可以有效处理大型且复杂的企业应用。

### 为什么 JavaScript 可以有效处理复杂的企业应用？

简化复杂企业应用的组合

程序员可以通过简化其组合来轻松加速复杂企业应用的开发。JavaScript 库通过创建 Shadow DOM 边界，让程序员更容易简化复杂业务应用的组合。Shadow DOM 使网络浏览器可以使用常用的 HTML 标签（如 `div`、`select` 和 `input`）生成并交付文档。除了解单个 JavaScript 框架的组件，Shadow DOM 将进一步促进组件之间的无缝通信。因此，JavaScript 将通过简化组合帮助程序员有效地进行维护和管理。

### 响应式网页设计

许多调查强调，现在很大比例的人在移动设备上访问网站。同样，实施“自带设备”（BYOD）政策的组织数量也在增加。因此，企业需要确保企业应用在不同设备上提供优质的用户体验。作为一种现代网站设计技术，响应式网页设计帮助企业使其 Web 端应用在各种设备上提供优质的用户体验。但响应式网页设计强调对 HTML5、JavaScript 和 CSS3 等开放技术的使用。

### 同构应用开发

许多企业现在选择同构 JavaScript 开发，以创建在许多设备上提供丰富用户体验的 Web 应用。程序员也发现更容易管理、更新和维护同构 JavaScript 应用。这种开发模型要求程序员使用 JavaScript 编写客户端和服务器端代码。由于整个代码库都是使用单一编程语言开发的，开发者更容易进行管理和更新，而无需投入额外的时间精力。

### 转译器简化 JavaScript 编程

JavaScript 最初被设计为 Web 浏览器的客户端脚本语言。因此，它缺乏 Java 或 C# 等现代编程语言提供的一些高级功能。但开发者仍然可以使用许多转译器来简化 JavaScript 编程。用户也可以从 CoffeeScript、TypeScript、DukeScript 和 Vaadin 中选择。这些工具通过复杂的工作流让程序员更容易为企业应用添加功能。这些转译器进一步使 JavaScript 在处理各种现代企业应用方面变得有效。

### 许多 JavaScript 框架的可用性

这些 JavaScript 框架有些强大且功能完全，另一些则简单。程序员可以使用 Angular 和 Ember 等大型框架快速为企业应用添加功能。同时，他们也可以选择使用 React 等轻量级库来高效完成特定任务。此外，可以使用 Node.js 等专用工具将 JavaScript 作为服务器端编程语言。同时，他们可以使用 NPM 等工具流畅有效地安装和管理企业应用使用的 JavaScript 库。

总体而言，企业有选择使用 JavaScript 开发企业应用的前后端。通过部署全栈开发者使用 JavaScript 编写客户端和服务器端代码，可以进一步缩短开发时间和成本。然而，程序员将需要各种 JavaScript 库、工具和框架来更高效地工作。

## JavaScript 编程语言的四个强大特性

在 Web 开发者和冲浪者社区中，JavaScript 作为浏览器的客户端脚本语言非常受欢迎。在任何 Web 应用中，JavaScript 都可实现图像悬停等简单功能，并可以使用 AJAX 向服务器发送异步请求。几年前，当 Flash 还不流行时，JavaScript 被广泛用于为网页添加精美效果，现在仍被用于此目的。让我们来看看这种语言的某些特性。

1. 浏览器支持：要访问 Flash 内容，你需要在浏览器中安装 Flash 插件。但要使用 JavaScript，你完全不需要任何插件。这是因为所有浏览器都接受 JavaScript 作为它们的脚本语言，并对其提供了集成支持。你只需要处理一些依赖于不同浏览器 DOM（文档对象模型）的任务即可。

2. 既可以在客户端使用，也可以在服务器端使用：JavaScript 可以访问浏览器的文档对象模型，你实际上可以在运行时更改网页的结构。因此，JavaScript 可以用于为网页添加不同的效果。另一方面，JavaScript 也可以在服务器端使用。例如，在 Alfresco 这种流行的开源企业内容管理系统中，JavaScript 用于创建 Webscripts。这使得为 Alfresco 添加自定义任务变得非常简单。

3. 函数式编程语言：在 JavaScript 中，函数可以像任何其他数据类型一样赋值给变量。不仅如此，函数还可以接受另一个函数作为参数，还可以返回一个函数。你也可以拥有没有名字的函数。显然，这赋予了你以函数式编程风格编码的能力。

4. 对对象的支持：JavaScript 是一种面向对象的语言。然而，JavaScript 处理对象和继承的方式与 Java 等传统的面向对象编程语言略有不同。由于这一点，JavaScript 在保持易于学习和使用的同时，支持了大多数面向对象的概念。

这些是让 JavaScript 能够处理简单及复杂任务的一些特性。正因如此，JavaScript 长期以来一直是最流行的编程语言。对于想要学习计算机编程的人来说，它也是一种很好的语言，因为它支持面向对象和函数概念，而且要使用它，你只需要一个浏览器和一个文本编辑器。

## 如何消除 Internet Explorer 上的 JavaScript 警告

JavaScript 是互联网上网页的标准编程语言。

JavaScript 错误是页面编程代码中的漏洞（bug）。

在互联网诞生初期，网页仅限于使用超文本标记语言（HTML）。HTML 是所有浏览器用于显示网页的标准。

HTML 处理链接和图片等内容，这在起初已经足够了，但人们希望在网页上实现更多功能。

Netscape 使用了一种专为 JavaScript 开发的简单编程语言，使得即使是非程序员也能通过更复杂的功能来增强他们的网站。这种语言本身已变得越来越复杂，现在成为了一项像 HTML 一样被所有网络浏览器支持的标准。

JavaScript 的设计并不是为了运行极其复杂的程序；它是为了网页的简单增强而设计的。随着互联网的演变，网页背后的编程变得越来越复杂，经常挑战 JavaScript 的局限。为了缓解这个问题，部分编程工作被交给了服务器处理，而不是尝试全部下载到你的计算机上。

JavaScript 在本地运行，目前被网站大量用于驱动其用户界面。尽管许多现代网站通过与服务器通信获取数据，但这种通信可能会缓慢甚至完全失败。如果服务器出现问题，用户界面保持响应至关重要，因此界面通常用 JavaScript 编写并在你的计算机本地运行，而更复杂的代码则运行在服务器上。

与任何编程语言一样，JavaScript 会有漏洞，有时这些漏洞会导致程序故障。幸运的是，与桌面程序不同，当 JavaScript 程序故障时，页面的其余部分通常仍正常运行。

### 消除 Internet Explorer JavaScript 警告对话框

你遇到的大多数 JavaScript 错误由于单个网页故障。通常这些错误是无害的：虽然你可能会丢失某些功能，但它们对你的计算机没有危险。

然而，Internet Explorer 默认会弹出警告对话框。此警告会阻止你在页面上进行任何操作，并可能令人感到恼怒。如果你是一个程序员，查看代码可能很有趣，但对我们其他人来说，这并没有什么用。

要消除该对话框，请遵循以下步骤：

1. 在 Internet Explorer 中，从“工具”菜单选择“Internet 选项”。
2. 点击“高级”选项卡。
3. 根据你的版本，可能会有三个需要设置的复选框（其中两个勾选，一个不勾选）：
   - 勾选：禁用脚本调试 (Internet Explorer)
   - 勾选：禁用脚本调试 (其他)
   - 取消勾选：显示有关每个脚本错误的通知
4. 点击“确定”按钮。

这应该停止警告对话框的显示。如果你在许多网页上开始遇到问题，可能是你的浏览器有问题，而不是网页，你可能需要重新安装 Internet Explorer。

## 关于 JavaScript 的错误

对于大多数计算机用户来说，JavaScript 是一个陌生的电脑术语。除了电脑专业人士和程序员外，大多数人对其知之甚少。本质上，JavaScript 是一种最常用于网站的 Web 开发语言。它因用户友好的特性而在非程序员中很受欢迎，同时还允许脚本访问嵌入其他应用程序中的对象。

然而，JavaScript 错误也相当常见，很大程度上是因为许多初学者使用它编写 Web 开发程序。但糟糕的事情是它也可以被用于编写广告软件和间谍软件，这些软件会进入你的计算机（通常是在你毫无察觉的情况下），从而阻塞注册表。这反过来会减慢你计算机的速度，甚至可能导致崩溃，我们都知道这意味着多么大的令人头疼。

常见的 JavaScript 错误如下：

1. 浏览器未启用 JavaScript。
2. 网页包含 JavaScript 编程错误。
3. 浏览器不支持 JavaScript 技术。

我们可以如何处理这些问题？当然，你可以选择告知网站管理员问题并提供你收到的 JavaScript 错误消息的所有细节，但你有一个更简单的替代方案：清理你的 Windows 注册表并观察问题的消失。

对于不知情的人来说，注册表是你使用的所有程序中的一个巨大的数据库，包括系统策略、文件关联或安装新软件。除非定期清理注册表，否则你无法避免 JavaScript 错误消息。

### 你可以用来移除 JavaScript 错误的简单技巧

许多网站构建者依赖 JavaScript 使其网站具有功能性。下拉菜单、图像切换和链接到其他网站等功能都是通过 JavaScript 完成的。当错误弹出时，意味着代码中某些地方不对。

### 让 JavaScript 错误在你的网站上运行可能会导致损失

对于某些网站构建者来说，遇到 JavaScript 错误可能是毁灭性的。这是一种常见的错误，但即使是简单的错误也会破坏网站的结果，并让最终用户感到困惑和沮丧。这反过来也会导致构建者损失资金并失去业务。

### 禁用 Firefox 浏览器的错误警告

帮助打破弹出警告不断循环的方法是手动更改启用或禁用弹出的选项。要禁用 Firefox 用户的警告，请执行以下操作：

1. 选择页面顶部的“工具”选项卡
2. 点击“选项”并选择框顶部的“内容”选项卡
3. 通过取消勾选“启用 JavaScript”框来禁用警告

这将阻止警告在你在上网时干扰你。然而，尽管禁用了警告，并不意味着错误彻底消失了。

### 尝试使用不同的网络浏览器

不同的浏览器对不同网站的反应不同。一个浏览器可能会遇到错误，另一个则不会。如果错误通过其他浏览器仍然发生，请尝试使用他人的账户甚至他人的计算机。如果在使用他人的 PC 时错误停止了，那么可能是时候关注清理你 PC 的注册表了。

### 从 Internet Explorer 中删除临时 Internet 文件

你的网络浏览器会创建你访问过的副本并存储在临时文件中。这些文件的积累会导致系统产生错误，需要定期清理。对于 Internet Explorer 用户，请执行以下操作：

1. 选择页面顶部的“工具”选项卡
2. 选择“常规”选项卡
3. 在“临时 Internet 文件”下选择“设置”
4. 点击“删除文件”并按“确定”
5. 点击“删除 Cookie”并按“确定”
6. 同时，在“历史”下选择“清除历史”
7. 选择“是”，然后点击“确定”

### 维护您的 PC 注册表

如果 JavaScript 错误仍然存在，请使用注册表清理程序修复。长期使用电脑会导致损坏，不断的信息流可能会阻塞注册表，从而降低电脑速度。这些错误可能是由故障或损坏的注册表引起的。

Optimize-Your-PC 可以为您提供先进的注册表清理技术。它将扫描、诊断并修复您的 JavaScript 错误，留下一个高度优化的电脑。

## 在 Dreamweaver 8 中添加 JavaScript

JavaScript 允许您向页面添加交互元素，并在网页上执行脚本函数。在 Dreamweaver 8 中添加 JavaScript 并不困难，不需要了解 JavaScript 编程。

在 Dreamweaver 8 中，JavaScript 是一种“行为”（behavior），通过行为面板（Behaviours panel）控制。当您在 Dreamweaver 8 中为网页添加 JavaScript 时，将使用行为面板。

要打开行为面板，选择 Windows > 行为（Behaviours）。选择 + 按钮激活下拉菜单。“添加行为”（Add Behaviours）下拉菜单包含约十二种常用的 JavaScript 控制函数，您可以将它们添加到 Dreamweaver 的页面中。常见的函数如检查浏览器类型和版本、检查插件、显示弹出消息、验证表单或跳转到 URL 都是您可以添加的 JavaScript 行为示例。

“添加行为”菜单中的每个行为都有一个对话框，允许您指定遇到特定触发器（trigger）时发生的操作。触发器是网站访问者可能执行的操作，例如点击链接、在表单中输入数据或鼠标悬停在页面上的特定位置。

如果您从访问者收集输入的信息，会发现“验证表单”（Validate Form）行为非常有用。验证表单行为可以验证访问者输入的数据格式是否正确或仅包含有效数据。妥善配置行为后，点击确定。

如果您想添加的行为不是内置的 JavaScript 行为，可以选择“获取更多行为”（Get More Behaviours）。此选项将带您访问 Macromedia Dreamweaver Exchange 网站。在这里，您可以找到下载的用户创建的 JavaScript 行为。需要注意的是：此处的行为并非都是免费的，但您会发现访问该网站时为 Dreamweaver 界面添加新行为是非常简单的。

您还可以更改已添加到 Dreamweaver 8 的行为。要修改现有行为，请在代码视图（Code View）中找到您想要编辑的行为。选择它，它将出现在行为面板中“添加行为”按钮下方的列表中。从现在起，您可以修改事件发生的顺序、更改触发操作的事件或直接删除该行为。

## JavaScript 构建大型 Web 应用的效果如何？

根据 w3techs.com 上发布的最新统计数据，目前超过 89% 的网站使用 JavaScript 作为客户端编程语言。作为一种跨平台且轻量级的编程语言，JavaScript 使得程序员更容易构建响应式网站和 Web 应用，这些应用可以与流行的网络浏览器、操作系统和设备无缝协作。它还被程序员广泛用于网络浏览器的一部分，以完成浏览器控制、用户交互和异步通信等重要任务。

此外，程序员还可以通过 Node.js 和类似的运行时环境将 JavaScript 作为服务器端脚本语言。同时，他们还可以使用各种开源框架来减少构建 JavaScript 应用所需的时间和精力。它还可以与 HTML5 和 CSS 一起用于创建应用程序和游戏。因此，您可以始终考虑将 JavaScript 作为动态客户端编程语言来构建大型 Web 应用。

### 使用 JavaScript 进行大型 Web 应用开发的优势

#### 主流网络浏览器支持

大多数广泛使用的网络浏览器（包括 Firefox、Chrome、Internet Explorer、Safari 和 Opera）都支持 JavaScript。实现 JavaScript 的新型浏览器也支持。因此，无论用户选择何种浏览器，都可以使用 JavaScript 访问 Web 应用。如果脚本语言由于某些原因被禁用，用户也可以通过启用它访问网站的所有功能。

#### 无需使用任何特定工具

JavaScript 是一种解释型编程语言。因此，您可以轻松编写代码而无需使用任何特定工具或程序。您只需打开记事本并开始编写 JavaScript 代码。此外，您可以使用许多编辑器来识别代码中的错误。编辑器会对脚本进行着色或重新格式化，以便用户识别错误。

#### 代码复用选项

通过简单将代码放置在单独的文件，您可以在多个页面之间进一步复用 JavaScript 代码。将代码放置在页面后，该选项允许您在链接到相同功能的同时避免编写额外的代码。

#### 许多库和框架

您可以使用多种框架来减少构建 JavaScript 应用所需的时间和精力。许多程序员更倾向于使用 AngularJS、Ember 和 React 等动态框架。然而，您仍然可以根据特定需求从长列表中进行选择。例如，您可以使用 Handlebars、Mustache。

#### 相对更快

如前所述，JavaScript 是一种客户端脚本语言。因此，代码在用户的系统上执行。由于代码执行时无需与服务器交互，处理速度相对更快。更快的处理使 Web 应用能够通过提供丰富的体验来留住用户。

#### 从服务器交付更新的响应数据

JavaScript 进一步使用 `XMLHttpRequest` API 进行数据检索。该 API 向 Web 服务器发送 HTTP 或 HTTPS 请求，并将服务器发送的响应加载到脚本中。脚本可以根据从服务器收到的响应轻松更新当前网页。因此，可以通过向用户提供更新信息而无需重新加载网页，从而提高 Web 应用的性能。

#### 扩展网站功能

JavaScript 让您更容易在不付出额外精力的情况下扩展 Web 应用的功能。您可以使用脚本语言在屏幕上创建视觉效果、计算数据并让网页更具交互性。JavaScript 进一步允许您使用第三方脚本扩展网站功能。这种灵活性让您更容易在不使用任何额外插件或工具的情况下为 Web 应用添加开箱功能。

#### 减少服务器负载

服务器端脚本语言需要 Web 服务器在发送响应之前处理用户请求。因此，尽管用户拥有高速互联网连接，该过程仍需要额外的时间。但 JavaScript 代码在用户的机器上处理，不与网络浏览器交互。因此，Web 服务器的压力和负载大大减轻，同时用户可以获得快速响应。在构建大型网站时，可以使用 JavaScript 为用户提供更快的响应，而不会给服务器带来过大负担。

#### 优化本地缓存

JavaScript 可以配合 HTML5 一起使用，使用户在没有活动互联网连接的情况下也能访问网站。这些技术在本地缓存数据方面有效，并在互联网连接恢复之前保持 Web 应用的响应能力。您甚至可以使用 Kendo UI DataSource 等工具来跟踪本地对对象的更改，并在网络连接恢复后将更改上传到 Web 服务器。该选项允许您让 Web 应用程序像移动应用程序一样工作。

#### 与其他 Web 技术配合

如前所述，TypeScript 开发者可以将其作为客户端脚本语言也可以作为服务端脚本语言。同时，你也可以选择 JavaScript 作为客户端技术，并与 PHP、Perl 和 Java 等广泛使用的 Web 技术配合使用。该脚本语言也常与 HTML5 和 CSS 一起用于开发响应式网站，通过同一套代码库即可在各种设备上访问。

然而，在使用 JavaScript 构建大型网站和 Web 应用时，你必须记住它的某些主要缺点。由于 JavaScript 代码在网络浏览器中执行，因此它容易受到各种安全攻击。此外，由于不同浏览器对代码的解释方式不同，代码会变得不可预测。

包括 Google 在内的主要搜索引擎机器人无法完全、充分地理解 JavaScript 编写的客户端代码。因此，使用过多 JavaScript 的 Web 应用其搜索引擎排名和可见性受到影响。但你仍然可以将 JavaScript 与 HTML5 和 CSS 等其他流行的 Web 技术结合，创建可在多个设备、系统和浏览器上访问的健壮 Web 应用。

## 为什么公司要招聘 JavaScript 开发者？

企业越来越重视招聘 JavaScript 开发者。如今正投入大量的资金、时间和精力来招聘人才，特别是年轻和应届的毕业生，主要是为了他们的专业素质，以及他们契合最新的技术和开发趋势。

现在，有许多原因导致现代企业将资金投入到 JavaScript 开发者身上。

企业青睐这些开发者的首要原因是他们的教育背景。大多数候选人拥有软件工程、计算机科学、信息技术以及与公司经营业务领域相关的学士学位。

然而，某些企业更看重经验，而不是他们所拥有的学位。尽管这是完全另一个问题。

企业投入资金是因为这些专业人士对软件开发生命周期有深入的理解。此外，他们拥有强大的概念——这一事实增强了他们在客户端和服务端语言方面的编程技能。这至关重要，因为并不是每个项目或客户都只需要 JavaScript，还需要辅助的编程平台。此外，当涉及到个人特质时，这些专业人士具有极强的分析能力和故障排除专长——这在软件开发中非常有用。而且，他们具备了与团队中其他人同步工作所需的心理素质。这本身就足以成为公司招聘他们的理由。

除了这些问题之外，了解他们的职责并拥有卓越的职业眼光也会带来不同。大多数 JavaScript 开发程序都是专门为 Web 端以及通常用于网站和计算机系统的不同服务器应用程序而设计和开发的。

开发完成后，必须对程序进行适当评估。一个优秀的开发者还具备评估这些编程脚本的专业知识，因此公司雇用他们是为了降低成本，因为程序员既可以开发也可以评估脚本。他们还擅长对语言进行广泛测试，以确保其在交付给客户之前运行正常。他们还确保脚本完全没有错误。

这些专业人士（尤其是应届毕业生）对最新的 Java 虚拟机 (JVM) 语言有丰富的知识，这有助于他们更快地完成任务。他们还擅长构建使语言更简单的应用程序。这最终为公司节省了大量资金。

公司的关键在于寻找参与软件开发社区的最优秀工程师，这样他们才能跟上最新技术并在概念创造方面保持新鲜。这是为了确保企业从对业务发展支柱——JavaScript 开发者的投入获得最大的回报。

专家不仅技术高、经验丰富，还精通其他语言，如 C、C++、.NET、Python、Joomla 等。他们拥有完美的技能。因此，尽管考虑到当今的通胀，招聘此类专业人士非常有成本效益，但公司仍然对其争相，因为这从短期和长期来看都是值得的。然而，为了节省成本，公司越来越倾向于聘请海外专业人士，而不是雇佣全职个人。这些专业人士提供维护以及其他辅助服务，无需额外费用，这有助于公司在很大程度上降低成本。

## JavaScript 的位置

### `<script>` 标签

在 HTML 中，JavaScript 代码必须插入在 `<script>` 和 `</script>` 标签之间。

示例

```html
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```

旧的 JavaScript 示例可能使用 `type` 属性：`<script type="text/javascript">`。

`type` 属性不是必须的。JavaScript 是 HTML 的默认脚本语言。

### `<head>` 或 `<body>` 中的 JavaScript

你可以在 HTML 文档中放置任意数量的脚本。

脚本可以放置在 HTML 页面的 `<body>` 部分、`<head>` 部分，或者两者都放。

#### `<head>` 中的 JavaScript

在此示例中，JavaScript 函数被放置在 HTML 页面的 `<head>` 部分。

当点击按钮时调用（触发）该函数：

示例

```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>
<h1>A Web Page</h1>
<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>
</body>
</html>
```

#### `<body>` 中的 JavaScript

在此示例中，JavaScript 函数被放置在 HTML 页面的 `<body>` 部分。

当点击按钮时调用（触发）该函数：

示例

```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>
<h1>A Web Page</h1>
<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>
</body>
</html>
```

```html
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
```

## 外部 JavaScript

外部文件：`myFunction.js`

```javascript
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

当同一代码在多个网页中使用时，外部脚本是非常实用的。

JavaScript 文件的扩展名为 `.js`。

要使用外部脚本，将脚本文件名放在 `<script>` 标签的 `src`（源）属性中：

示例

```html
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

### 外部 JavaScript 的优势

将脚本放在外部文件中具有某些优势：

- 分离了 HTML 和代码
- 使 HTML 和 JavaScript 更易于阅读和维护
- 缓存的 JavaScript 文件可以加快页面加载

要向一个页面添加多个脚本文件——使用多个 `<script>` 标签：

示例

```html
<script src="myScript1.js"></script>
<script src="myScript2.js"></script>
```

### 外部引用

外部脚本可以使用完整 URL 或相对于当前页面的路径引用。

此示例使用完整 URL 链接到脚本：

示例

```html
<script src="http://www.w3schools.com/js/myScript1.js"></script>
```

此示例链接到与当前页面相同文件夹下的脚本：

示例

```html
<script src="myScript1.js"></script>
```

## JavaScript 输出

JavaScript 可以通过不同的方式“显示”数据：

- 使用 `window.alert()` 写入警告框。
- 使用 `document.write()` 写入 HTML 输出中。
- 使用 `innerHTML` 写入 HTML 元素中。
- 使用 `console.log()` 写入浏览器控制台。

### 使用 `window.alert()`

你可以使用警告框来显示数据：

示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p>My first paragraph.</p>
<script>
window.alert(5 + 6);
</script>
</body>
</html>
```

### 使用 `document.write()`

为了测试之目的，使用 `document.write()` 是方便的：

示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p>My first paragraph.</p>
<script>
document.write(5 + 6);
</script>
</body>
</html>
```

在 HTML 文档完全加载后使用 `document.write()`，将删除所有现有的 HTML：

示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p>My first paragraph.</p>
<button onclick="document.write(5 + 6)">Try it</button>
</body>
</html>
```

### 使用 `innerHTML`

要访问 HTML 元素，JavaScript 可以使用 `document.getElementById(id)` 方法。

`id` 属性定义 HTML 元素。`innerHTML` 属性定义 HTML 内容：

示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p>My First Paragraph</p>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 5 + 6;
</script>
</body>
</html>
```

要在 HTML 中“显示数据”，（在大多数情况下），你将设置 `innerHTML` 属性的值。

### 使用 `console.log()`

在你的浏览器中，你可以使用 `console.log()` 方法来显示数据。

示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
My first paragraph.
<script>
console.log(5 + 6);
</script>
</body>
</html>
```

## JavaScript 语法

JavaScript 语法是构建 JavaScript 程序的规则集。

### JavaScript 程序

计算机程序是供计算机“执行”的一系列“指令”列表。

在编程语言中，这些程序指令被称为语句。

JavaScript 是一种编程语言。

JavaScript 语句用分号隔开：

示例

```javascript
var x, y, z;
x = 5;
y = 6;
z = x + y;
```

在 HTML 中，JavaScript 程序由 Web 浏览器执行。

### JavaScript 语句

JavaScript 语句由以下部分组成：

值、操作符、表达式、关键字和注释。

### JavaScript 值

JavaScript 语法定义了两种值：固定值和变量值。

固定值被称为字面量（literals）。变量值被称为变量。

### JavaScript 字面量

编写固定值最重要的规则是：

数字可以带或不带小数写：

```javascript
10.50
```

```javascript
1001
```

字符串是文本，写在双引号或单引号内：

```javascript
"John Doe"
```

```javascript
'John Doe'
```

### JavaScript 变量

在编程语言中，变量用于存储数据值。

JavaScript 使用 `var` 关键字来声明变量。

使用等号给变量赋值。

在示例中，`x` 被定义为一个变量。然后，给 `x` 赋值（给定）值 6：

```javascript
var x;
```

```javascript
x = 6;
```

### JavaScript 操作符

JavaScript 使用赋值运算符（`=`）给变量赋值：

```javascript
var x, y;
x = 5;
y = 6;
```

JavaScript 使用算术操作符（`+` `-` `*` `/`）计算值：

### JavaScript 表达式

表达式是值、变量和操作符的组合，计算出一个值。

计算过程被称为求值（evaluation）。

例如，`5 * 10` 的求值结果为 50：

```javascript
5 * 10
```

表达式也可以包含变量值：

```javascript
x * 10
```

值可以是各种类型，例如数字和字符串。

例如，`"John" + " " + "Doe"` 的求值结果为 `"John Doe"`：

```javascript
"John" + " " + "Doe"
```

### JavaScript 关键字

JavaScript 关键字用于标识要执行的操作。

`var` 关键字告诉浏览器创建变量：

```javascript
var x, y;
x = 5 + 6;
y = x * 10;
```

### JavaScript 注释

并不是所有的 JavaScript 语句都会被“执行”。

双斜杠 `//` 以及 `/*` 和 `*/` 之间的代码被视为注释。

注释会被忽略，不会被执行：

```javascript
var x = 5; // I will be executed
// var x = 6; I will NOT be executed
```

你将在后面的章节中学习更多关于注释的知识。

### JavaScript 标识符

标识符是名称。

在 JavaScript 中，标识符必须是字母、下划线 (`_`) 或美元符号 (`$`)。

### JavaScript 区分大小写

所有标识符都区分大小写。

```javascript
var lastname = "Doe";
var LastName = "Doe";
```

### JavaScript 与驼峰命名法

从历史上，程序员使用三种方法将单词组合为一个：

- 连字符：`first-name`
- 下划线：`first_name`
- 驼峰命名法：`firstName`

### JavaScript 字符集

JavaScript 使用 Unicode 字符集。Unicode 涵盖（几乎）世界上所有的字符、标点和符号。

### JavaScript 语句

该语句告诉浏览器在 `id="demo"` 的 HTML 元素内部写入 `"Hello Dolly"`：

示例

```javascript
document.getElementById("demo").innerHTML = "Hello Dolly";
```

### JavaScript 程序

大多数 JavaScript 程序包含许多语句。

语句按照编写顺序逐个执行。

在此例中，`x`、`y` 和 `z` 被赋予了值，最后显示了 `z`：

示例

```javascript
var x, y, z;
x = 5;
y = 6;
z = x + y;
document.getElementById("demo").innerHTML = z;
```

### 分号

分号隔开 JavaScript 语句。

在每个可执行语句末尾添加分号：

```javascript
var a, b, c;
a = 5;
b = 6;
c = a + b;
```

当用分号隔开时，允许在一行中写多个语句：

```javascript
a = 5; b = 6; c = a + b;
```

在网页上，你可能会看到没有分号的示例。

语句结尾不需要加分号，但强烈建议加上。

### JavaScript 空格

JavaScript 忽略多个空格。你可以在脚本中添加空格以提高其可读性。

以下行是等价的：

```javascript
var person = "Hege";
var person="Hege";
```

良好的做法是在操作符周围放置空格。

```javascript
var x = y + z;
```

### JavaScript 行长度

为了最佳的可读性，程序员通常喜欢避免代码行超过 80 个字符。

如果一条 JavaScript 语句无法一行写完，最佳折行位置是在操作符之后：

示例

```javascript
document.getElementById("demo").innerHTML = 
"Hello Dolly";
```

### JavaScript 代码块

JavaScript 语句可以组合在花括号 `{...}` 中的代码块中。

代码块的作用是定义一起执行的语句。

你可能会找到语句在块中分组的一个地方是在 JavaScript 函数中：

示例

```javascript
function myFunction() {
    document.getElementById("demo1").innerHTML = "Hello Dolly";
    document.getElementById("demo2").innerHTML = "How are you?";
}
```

## JavaScript 关键字

JavaScript 语句通常以关键字开头，用于标识要执行的 JavaScript 操作。

以下是本教程中你将学习的一些关键字列表：

| 关键字 | 说明 |
| --- | --- |
| `break` | 终止 switch 或循环 |
| `continue` | 跳出循环并从顶部重新开始 |
| `debugger` | 停止 JavaScript 的执行，并调用（如果可用）调试函数 |
| `do ... while` | 执行一个语句块，并在条件为真时重复该块 |
| `for` | 标记一个要执行的语句块，只要条件为真 |
| `function` | 声明一个函数 |
| `if ... else` | 根据条件标记一个要执行的语句块并退出函数 |
| `switch` | 根据不同的情况标记一个要执行的语句块 |
| `try ... catch` | 对语句块实现错误处理 |
| `var` | 声明变量 |

## JavaScript 注释

JavaScript 注释可以解释 JavaScript 代码，并使其更具可读性。

JavaScript 注释还可以用于在测试备用代码时防止执行。

### 单行注释

单行注释以 `//` 开头。

`//` 和行尾之间的任何文本都将被 JavaScript 忽略（不会执行）。

此示例在每行代码之前使用一个单行注释：

示例

```javascript
// 修改标题：
document.getElementById("myH").innerHTML = "My First Page";
// 修改段落：
document.getElementById("myP").innerHTML = "My first paragraph."
```

此示例在每行的末尾使用单行注释来解释代码：

示例

```javascript
var x = 5; // 声明 x，给它赋值为 5
var y = x + 2; // 声明 y，给它赋值为 x + 2
```

### 多行注释

多行注释以 `/*` 开头并以 `*/` 结束。

`/*` 和 `*/` 之间的任何文本都将被 JavaScript 忽略。

此示例使用多行注释（注释块）来解释代码：

示例

```javascript
/*
下面的代码将更改
我的网页中 id 为 "myH" 的标题
以及 id 为 "myP" 的段落：
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

### 使用注释防止执行

使用注释防止代码执行适用于代码测试。

在代码行前添加 `//` 会将该代码行从可执行行变为注释。

此示例使用 `//` 防止其中一行代码的执行：

示例

```javascript
//document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

此示例使用注释块防止多行代码的执行：

示例

```javascript
/*
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
*/
```

## JavaScript 变量

JavaScript 变量是存储数据值的容器。

在示例中，`x`、`y` 和 `z` 都是变量：

示例

```javascript
var x = 5;
var y = 6;
var z = x + y;
```

从上面的示例中，你可以预期：

- `x` 存储值 5
- `y` 存储值 6
- `z` 存储值 11

### 类似于代数

在示例中，`price1`、`price2` 和 `total` 是变量：

示例

```javascript
var price1 = 5;
var price2 = 6;
var total = price1 + price2;
```

在编程中，就像在代数中一样，我们使用变量（如 `price1`）来持有值。

在编程中，就像在代数中一样，我们在表达式中使用变量（`total = price1 + price2`）。

从上面的示例中，你可以计算出总值为 11。

### JavaScript 标识符

所有的 JavaScript 变量必须用唯一的名称标识。

这些唯一的名称被称为标识符。

标识符可以是短名称（如 `x` 和 `y`），也可以是描述性的名称（`age`、`sum`、`totalVolume`）。

构造变量名称（唯一标识符）的通用规则是：

- 名称可以包含字母、数字、下划线和美元符号。
- 名称必须以字母开头。
- 名称也可以以 `$` 和 `_` 开头（但我们不会在本教程中使用它们）。
- 名称区分大小写（`y` 和 `Y` 是不同的变量）。
- 预留字（如 JavaScript 关键字）不能作为名称。

JavaScript 标识符是区分大小写的。

### 赋值运算符

在 JavaScript 中，等号 (`=`) 是一个“赋值”运算符，而不是“等于”运算符。

这与代数不同。以下内容在代数中是没有意义的：

```javascript
x = x + 5
```

但在 JavaScript 中，它是完全有意义的：它将 `x + 5` 的值赋值给 `x`。

（它计算 `x + 5` 的值并将结果放入 `x` 中。`x` 的值增加了 5。）

“等于”运算符在 JavaScript 中写为 `==`。

## JavaScript 数据类型

JavaScript 变量可以持有诸如 100 这样的数字和像 `"John Doe"` 这样的文本值。

在编程中，文本值被称为文本字符串。

JavaScript 可以处理许多类型的数据，但现在只需考虑数字和字符串。

字符串写在双引号或单引号内。数字则不加引号。

如果你将一个数字放在引号内，它将被视为文本字符串。

示例

```javascript
var pi = 3.14;
var person = "John Doe";
```

### JavaScript 运算符

| 运算符 | 描述 |
| --- | --- |
| `+` | 加法 |
| `-` | 减法 |
| `*` | 乘法 |
| `/` | 除法 |
| `%` | 取模 |
| `**` | 幂 |
| `++` | 递增 |
| `--` | 递减 |
| `==` | 等于 |
| `===` | 严格相等 |
| `!=` | 不等于 |
| `!==` | 严格不相等 |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |
| `&&` | 逻辑与 |
| `||` | 逻辑或 |
| `!` | 逻辑非 |
| `=` | 赋值运算符 |
| `+=` | 加赋值 |
| `-=` | 减赋值 |
| `*=` | 乘法赋值 |
| `/=` | 除法赋值 |
| `%=` | 取模赋值 |
| `**=` | 幂赋值 |
| `<<=` | 左移赋值 |
| `>>=` | 右移赋值 |
| `>>>=` | 无符号右移赋值 |
| `&=` | 位与赋值 |
| `|=` | 位或赋值 |
| `^=` | 位异或赋值 |

### JavaScript 算术运算

与代数一样，你可以对 JavaScript 变量进行算术运算，使用 `=` 和 `+` 等运算符：

示例

```javascript
var x = 5 + 2 + 3;
```

## JavaScript 数据类型

JavaScript 变量支持多种数据类型：

| 类型 | 描述 |
| --- | --- |
| `number` | 数字 |
| `string` | 字符串 |
| `boolean` | 布尔值 |
| `undefined` | 未定义 |
| `null` | 空值 |
| `symbol` | 符号 |
| `bigint` | 大整型 |
| `object` | 对象 |
| `function` | 函数 |

## JavaScript 比较运算符

比较运算符用于比较两个值：

| 运算符 | 描述 |
| --- | --- |
| `==` | 等于 |
| `===` | 严格相等 |
| `!=` | 不等于 |
| `!==` | 严格不相等 |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |

## JavaScript 逻辑运算符

逻辑运算符用于执行逻辑操作：

| 运算符 | 描述 |
| --- | --- |
| `&&` | 逻辑与 |
| `||` | 逻辑或 |
| `!` | 逻辑非 |

### JavaScript 赋值运算符

赋值运算符用于向变量赋值：

| 运算符 | 描述 |
| --- | --- |
| `=` | 赋值 |
| `+=` | 加赋值 |
| `-=` | 减赋值 |
| `*=` | 乘法赋值 |
| `/=` | 除法赋值 |
| `%=` | 取模赋值 |
| `**=` | 幂赋值 |
| `<<=` | 左移赋值 |
| `>>=` | 右移赋值 |
| `>>>=` | 无符号右移赋值 |
| `&=` | 位与赋值 |
| `|=` | 位或赋值 |
| `^=` | 位异或赋值 |

### JavaScript 位运算符

位运算符用于对位进行操作：

| 运算符 | 描述 |
| --- | --- |
| `&` | 位与 |
| `|` | 位或 |
| `^` | 位异或 |
| `~` | 位取反 |
| `<<` | 左移 |
| `>>` | 右移 |
| `>>>` | 无符号右移 |

### JavaScript 三元运算符

JavaScript 只有一个三元运算符：

| 运算符 | 描述 |
| --- | --- |
| `? :` | 条件运算符 |

### JavaScript 表达式运算符

表达式运算符用于计算一个值：

| 运算符 | 描述 |
| --- | --- |
| `+` | 加法 |
| `-` | 减法 |
| `*` | 乘法 |
| `/` | 除法 |
| `%` | 取模 |
| `**` | 幂 |
| `++` | 递增 |
| `--` | 递减 |
| `==` | 等于 |
| `===` | 严格相等 |
| `!=` | 不等于 |
| `!==` | 严格不相等 |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |
| `&&` | 逻辑与 |
| `||` | 逻辑或 |
| `!` | 逻辑非 |
| `=` | 赋值 |
| `+=` | 加赋值 |
| `-=` | 减赋值 |
| `*=` | 乘法赋值 |
| `/=` | 除法赋值 |
| `%=` | 取模赋值 |
| `**=` | 幂赋值 |
| `<<=` | 左移赋值 |
| `>>=` | 右移赋值 |
| `>>>=` | 无符号右移赋值 |
| `&=` | 位与赋值 |
| `|=` | 位或赋值 |
| `^=` | 位异或赋值 |
| `&` | 位与 |
| `|` | 位或 |
| `^` | 位异或 |
| `~` | 位取反 |
| `<<` | 左移 |
| `>>` | 右移 |
| `>>>` | 无符号右移 |



## 使用变量

```
var x = 5;
var y = 6;
var z = x + y;
```

从上面的示例中，你可以预期：

- `x`存储值 5
- `y`存储值 6
- `z`存储值 11

### 类似于代数

在示例中，`price1`、`price2`和`total`是变量：

示例

```
var price1 = 5;
var price2 = 6;
var total = price1 + price2;
```

在编程中，就像在代数中一样，我们使用变量（如`price1`）来持有值。

在编程中，就像在代数中一样，我们在表达式中使用变量（`total = price1 + price2`）。

从上面的示例中，你可以计算出总值为 11。

### JavaScript 标识符

所有的 JavaScript 变量必须用唯一的名称标识。

这些唯一的名称被称为标识符。

标识符可以是短名称（如`x`和`y`），也可以是描述性的名称（`age`、`sum`、`totalVolume`）。

构造变量名称（唯一标识符）的通用规则是：

- 名称可以包含字母、数字、下划线和美元符号。
- 名称必须以字母开头。
- 名称也可以以`$`和`_`开头（但我们不会在本教程中使用它们）。
- 名称区分大小写（`y`和`Y`是不同的变量）。
- 预留字（如 JavaScript 关键字）不能作为名称。

JavaScript 标识符是区分大小写的。

### 赋值运算符

在 JavaScript 中，等号（`=`）是一个“赋值”运算符，而不是“等于”运算符。

这与代数不同。以下内容在代数中是没有意义的：

```
x = x + 5
```

但在 JavaScript 中，它是完全有意义的：它将`x + 5`的值赋值给`x`。

（它计算`x + 5`的值并将结果放入`x`中。`x`的值增加了 5。）

“等于”运算符在 JavaScript 中写为`==`。

## JavaScript 数据类型

JavaScript 变量可以持有诸如 100 这样的数字和像`"John Doe"`这样的文本值。

在编程中，文本值被称为文本字符串。

JavaScript 可以处理许多类型的数据，但现在只需考虑数字和字符串。

字符串写在双引号或单引号内。数字则不加引号。

如果你将一个数字放在引号内，它将被视为文本字符串。

示例

```
var pi = 3.14;
var person = "John Doe";
```

- 减法
- 乘法
- 除法
- 取模运算
- `++`递增
- `--`递减

赋值运算符（`+=`）用于给变量增加一个值。

```
Assignment
x = 10;
x += 5;
```

赋值运算符在 JS 赋值章节中会有详细的描述。

## JavaScript 字符串运算符

`+`运算符也可以用于连接（拼接）字符串。

### 示例

`+=`赋值运算符也可以用于连接（拼接）字符串。

```
Example
txt1 = "What a very ";
txt1 += "nice day";
// txt1 的结果将是:
```

What a very nice day

当用于字符串时，`+`运算符被称为拼接运算符。

### 相加字符串和数字

相加两个数字将返回和，但相加一个数字和一个字符串将返回一个字符串：

### 示例

```
x = 5 + 5;
y = "Hello" + 5;
z = "Hello" + 5;
```

`x`、`y`和`z`的结果将是：

```
10
55
Hello5
```

如果你将一个数字和一个字符串相加，结果将是一个字符串！

## JavaScript 比较运算符

| 运算符 | 描述 |
| :--- | :--- |
| `==` | 值相等且类型相等 |
| `!=` | 不相等 |
| `!=` | 值不等或类型不相等 |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |
| `?` | 三元运算符 |

## JavaScript 逻辑运算符

| 运算符 | 描述 |
| :--- | :--- |
| `&&` | 逻辑与 |
| `\|\|` | 逻辑或 |
| `!` | 逻辑非 |

## JavaScript 类型运算符

| 运算符 | 描述 |
| :--- | :--- |
| `typeof` | 返回变量的类型 |
| `instanceof` | 如果对象是对象类型的实例，则返回 true |

## Java 和 JavaScript：并不一样

程序员面临的一个常见问题是混淆 Java 和 JavaScript 这两种编程语言。虽然这两种语言有相似之处，但它们是完全不同的东西，通常用于不同的应用程序。

Java 是由 Sun Microsystems 开发的一种通用编程语言，旨在让程序员实现“一次编写，随处运行”。Java 代码在虚拟机内部执行，因此 Java 应用程序可以发布，而无需开发者担心应用程序可能运行的不同架构和操作系统。

相反，JavaScript 是一种脚本语言。它的用途是在网页内部的。当网页浏览器加载页面时，它会执行其中的 JavaScript 代码。这些代码可以更改网页的外观和操作方式。例如，JavaScript 代码可以创建一个在鼠标悬停时展开的下拉菜单，或者创建一个显示图片会定期变化的图像图库。

这种差异在两种语言的库中最为明显。Java 拥有一个巨大的标准库，该库在 Java 标准中已经标准化。这允许 Java 程序员在编写代码时使用各种工具。JavaScript 的标准库要小得多，通常与处理网页中的 HTML 代码有关。

进一步让这两种语言产生混淆的是，Java 还可以以 Java applet 的形式用于网页中。这是网页的一个小部分，Java 代码在其中运行并在浏览器窗口中显示。Java applet 通常用于在浏览器中创建更高级的内容，例如游戏。JavaScript 的功能远不足以创建一个复杂的游戏，因此使用了 Java。

这就是 Java 的平台无关优势大用武场。只要网页浏览器安装了 Java 插件（大多数浏览器都有），无论使用哪种网页浏览器，代码的运行都是相同的。这不能适用于 JavaScript，因为它在不同的网页浏览器中的实现方式往往不同，需要各种兼容性补丁。

尽管两者都可以作为 Web 语言，但对于追求 Web 的程序员来说，学习 JavaScript 要重要得多。JavaScript 的简单性也意味着它运行速度快，因此网页上添加的小功能不会被 Java 虚拟机拖慢。这就是为什么 Java 不再被广泛用于 Web 的原因：因为它太慢了。Java applet 需要加载巨大的 Java 插件，对于大型 Web 项目之外的所有项目都是大材小用，特别是当像 HTML5 这样灵活的工具在 Web 上变得越来越广泛使用时。

Java 和 JavaScript 是两种不同的编程语言。它们都有自己的用途，但它们不能互相替代。

## 如何使用 JavaScript 获取用户输入并在计算中使用该输入

变量的使用是所有编程语言的关键。你可能还记得高中代数课上的`x`和`y`。在编程中，变量的意义比仅仅是未知值的概念要大得多。在编程中，变量被用作特定信息存储区域的名称。然后你可以使用变量名来调用存储在那里的任何内容。如果你丢弃旧内容并在存储区域中放入新内容，变量就会指向新内容。

某些编程语言必须提前知道你打算存储什么。它们喜欢提前规划你正在租用多大的存储区域。告诉这些语言你打算存储什么意味着你必须声明数据类型。这些类型的编程语言被称为强类型语言。其他语言（如 JavaScript）则完全不在乎你存储什么。

它们在你将数据发送到存储区域时才决定需要多大的空间。这就是为什么 JavaScript 比某些编程语言学起来简单的原因之一。

然而，你仍然需要学习一些数据类型的知识，因为不告诉想要存储什么类型会有一些副作用。在任何情况下，信息仍然有一个变量名。这里有一个练习，可以：

- 从提示框收集信息
- 将其放入变量中
- 进行计算
- 在警告框中返回答案

将此代码添加到新的网页中

```
var SquareThis = prompt("输入一个你想要平方的数字。");
var Answer;
Answer = SquareThis * SquareThis;
alert(Answer);
```

## 此代码中的基础编程技能

1. 当你进行任何编程时，你必须思考计算机需要持有哪些信息。然后你创建变量来持有这些信息。在这个例子中，我们需要持有两个信息：1) 将被平方的数字，2) 答案。

2. 你通过命名`var`、空格和变量名告诉 JavaScript 你想存储信息。

3. 此脚本的第一行执行了三项任务：1) 它告诉 JavaScript 为变量`SquareThis`留出内存空间，2) 使用预写的函数提示用户输入数字，3) 它获取用户在提示框中输入的任何内容并将其放入`SquareThis`的内存空间中。

4. 注意提示函数像`alert()`一样需要一个参数。同样注意参数在`""`中，这意味着参数是字符串类型。

5. 现在脚本需要一个变量来存放答案。这是通过`var Answer;`实现的。

6. 现在已准备好进行数学计算：`Answer = SquareThis * SquareThis;`告诉计算机执行什么样的数学运算被称为运算符。主要的运算符有`+`、`*`、`/`（加、乘、除）。还有许多其他运算符。平方是任何数字乘以自身，所以这个公式将`SquareThis`乘以自身。

7. 程序有了答案，但它需要告诉用户。我们再次使用一个警告框。

8. 现在更改公式执行其他操作。尝试添加另一个变量和另一个`alert()`来请求另一个数字（或多个）。

## 以下是一些供你实验的运算符：

| 运算符 | JavaScript 数学函数 |
| :--- | :--- |
| `+` | 加两个数字 |
| `-` | 减两个数字 |
| `/` | 除两个数字 |
| `++` | 数字加 1（只需要一个变量） |
| `--` | 数字减 1（只需要一个变量） |

## 结论

HTML 不能用来替代 JavaScript。这两种编程语言完全不同，具有不同的功能、特性和能力。HTML 是一种标记语言，旨在为创建静态网页内容而设计；而 JavaScript 是一种可以执行动态任务的编程语言。它可以在网站的不同页面上反复使用。这可以通过将其外部化并放置在单独的文件，并将 JavaScript 文件链接到特定页面的 HTML 代码中来实现。因此，通过在每个页面上添加正确的标签，可以将 JavaScript 添加到许多页面中。

并不是每个拥有业务的人都精通 JavaScript 或知道如何使用它。使用它来创建网站只会对你的网站有益，因为 JavaScript 可以为网站增添许多方面的特性。因此，如果你能聘请一家专业的网页设计公司来帮助你使用 JavaScript 构建网站，那将大有帮助。专业设计师团队可以与你坐在一起，理解你的业务，并在考虑到你所有业务需求的情况下来设计网站。

© Brian Draper
