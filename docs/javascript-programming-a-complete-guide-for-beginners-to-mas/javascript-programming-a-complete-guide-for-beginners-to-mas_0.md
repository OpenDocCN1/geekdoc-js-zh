
# JavaScript 编程：初学者指南，掌握 JavaScript 编程语言并成为专家

![](img/cover0008.jpeg)

# 1. JavaScript 简介

JavaScript 是一种客户端脚本语言，嵌入在 Internet Explorer、Netscape、Firefox 等浏览器中。它首次创建于 1995 年，尽管它的名字后来改为 JavaScript。发明 JavaScript 是为了为 HTML 添加交互功能。它允许开发者与网页元素交互、执行计算、验证表单等。

## 18. 如何使用 JavaScript 获取用户输入

在上述代码中使用 `<!--` 和 `-->` 确保代码不会被缺乏 JavaScript 支持的旧版本浏览器显示。

## 19. 结论

与任何其他 HTML 文件一样，你只需要将上述代码复制粘贴到你的记事本文档中，然后以 ".html" 扩展名保存。保存完成后，只需右键点击该文件，并选择“打开方式”。在这里，选择一个网页浏览器（如果可用，选择 Mozilla Firefox）。代码将自动执行，结果将在浏览器窗口中显示。

### 注意事项

- JavaScript 代码大部分放置在 html 的 "head" 部分，但你也可以在 "body" 区域使用它们。
- JavaScript 代码通常以标签 `<script language="JavaScript">` 开始，以 `</script>` 结束。
- JavaScript 总是被嵌入到 HTML 代码中，永远不能孤立存在。

### 警报消息框

如果你想为网站添加自定义的警报消息框，可以使用 JavaScript 非常轻松地实现。添加自定义警报框的代码如下：

```html
<body>
<script>
window.alert("This is JavaScript Alert Box!")
</script>
</body>
```

同样，你可能还会添加其他警报，例如：

1. 确认操作
   `window.confirm("Are you sure you want to exit from this site?")`

2. 提示操作
   `window.prompt("User name field cannot be left blank.")`

让我们仔细观察使用 JavaScript 编程可以实现的奇妙功能：

### 执行计算

JavaScript 可用于从简单到高级的数学计算。如果你希望用户通过输入某些需要计算的信息来与网站交互，并根据该结果显示相关内容，那么这将非常有用。例如，如果用户在网站上输入所需的贷款金额，javascript 可以计算贷款还款并显示适当的结果。此外，javascript 还可以告知日期时间、活动计时并执行复杂的日期时间计算。

### 用户交互

网页上的 JavaScript 可以接收用户的交互并以此执行某些功能。一些最流行的事件包括：

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
- `onSubmit`

### 执行表单验证

JavaScript 可以验证和检查用户输入，以确定其是否符合特定要求。例如，你可以检查某个字段是否留空、电子邮件地址格式是否正确、邮政编码格式是否正确等。在大多数情况下，如果访客犯了错误，警报可以向其显示错误消息。

### 操作网页上的元素

JavaScript 允许用户在触发事件交互时更改网页内容。例如，鼠标悬停在某些文本上可以显示图像，提交按钮上的文字可以更改 `onSubmit` 等。

### 提供视觉效果

JavaScript 有一种原生方式为网页提供视觉效果，这是其他服务器端语言无法提供的。这方面的示例可能是华丽的图片轮播。

### 启用动态功能

JavaScript 结合 AJAX（异步 JavaScript 和 XML）可用于创建动态应用程序。其示例是在不刷新页面的情况下加载网页的动态内容。

### JavaScript 能处理大型企业应用吗？

根据 W3Techs 发布的统计，超过 91% 的网站使用 JavaScript 作为客户端编程语言。还有许多程序员使用 JavaScript 同时编写客户端和服务器端代码。然而，开发者必须依赖如 `Node.js` 等框架来将 JavaScript 用于服务器端。JavaScript 可以有效处理处理大型且复杂的企业应用。

### 为什么 JavaScript 可以有效处理？企业应用的简化

程序员可以轻松地开发复杂的企业应用。JavaScript 库让程序员更容易简化项目组成。Shadow DOM 使得网页浏览器使用 `div` 等常用标签交付文档。除了单独的 JavaScript 框架外，shadow 还会进一步促进内容之间的通信。因此， JavaScript 将帮助程序员有效地维护和管理他们的项目组成。

### 响应式网页设计

许多调查强调，现在有许多人在移动设备上访问网站。同样，实施自备设备（BYOD）的组织数量也日益增加。因此，企业需要确保应用程序在不同设备上提供优质的用户体验。作为一种现代网站设计，响应式网页帮助企业使其基于 Web 的交付在各种设备上提供优质的用户体验。但响应式网页设计强调了 HTML5、JavaScript 和 CSS3 等技术的使用。

### 同构应用开发

许多企业选择同构 JavaScript 开发，以创建在许多设备上提供更丰富用户体验的 Web 应用。程序员也发现更容易管理、更新和维护同构 JavaScript 应用。这种开发模型要求程序员使用 JavaScript 编写客户端和服务器端代码。由于整个代码库都是使用单一编程语言开发的，开发者可以更容易管理和更新，而无需花费额外的时间精力。

### 译器简化 JavaScript 编程

JavaScript 最初被设计为 浏览器的客户端脚本语言。因此，它缺乏现代编程语言（如 Java 或 C#）的一些高级功能。但开发者仍然可以使用许多译器来简化 JavaScript。这些工具包括 `TypeScript` 和 `Babel`。这些工具让 JavaScript 能够有效处理动态应用程序。

### 许多 JavaScript 框架

这些框架中有些健壮且功能完备，另一些则非常简单。程序员可以使用 `Angular` 和 `Ember` 等大型框架为企业应用添加动态特性。同时，他们也可以选择 `React` 等轻量级库来完成特定任务。此外，他们还可以使用 `NPM` 等专用工具来安装和管理企业使用的 JavaScript 库。

在 Web 开发者和冲浪社区中，JavaScript 作为 Web 浏览器的客户端脚本语言非常流行。在任何 Web 应用程序中，JavaScript 都可以用于实现图像悬停等简单功能，还可以使用 `ajax` 向服务器发送异步请求。几年前，当 Flash 尚未流行时，JavaScript 已被广泛用于为网页添加精美的效果，并且现在仍被用于此目的。让我们来看看这种语言的一些特性。

1. **浏览器支持**：为了评估 Flash 内容，你需要在浏览器中安装 Flash 插件。但要使用 JavaScript，你完全不需要使用任何插件。这是因为所有浏览器都接受 JavaScript 作为它们的脚本语言，并对其提供了集成支持。你只需要妥善处理一些依赖于不同浏览器 `DOM`（文档对象模型）的任务即可。

2. **既可以用于客户端，也可以用于服务器端**：由于 JavaScript 可以访问浏览器的文档对象模型，你实际上可以在运行时更改页面的结构。得益，JavaScript 可以用于为网页添加不同的效果。另一方面，JavaScript 也可以在服务器端使用。例如，在 `Alfresco` 这一流行的开源企业内容管理系统中，JavaScript 被用于创建 Webscripts。这使得为 `alfresco` 添加自定义任务变得非常简单。

3. **函数式编程语言**：在 JavaScript 中，函数可以像其他数据类型一样赋值给变量。不仅如此，函数还可以接受另一个函数作为参数，也可以返回一个函数。你也可以匿名函数。显然，这赋予了你以函数式编程风格编写代码的能力。

4. **对对象的支持**：JavaScript 是一种面向对象的语言。然而，JavaScript 处理对象和继承的方式与 `Java` 等传统的面向对象编程语言略有不同。因此，JavaScript 在保持易于学习和使用的同时，支持了大多数面向对象的概念。

这些都是让 JavaScript 能够处理简单及复杂任务的特性。正因如此，JavaScript 长期以来一直是最流行的编程语言。对于想要学习计算机编程的人来说，它也是一门很好的语言，因为它支持面向和函数式概念，而使用它，你只需要一个浏览器和一个文本编辑器。

# 如何消除 Internet Explorer JavaScript 警告

JavaScript 是互联网页面的标准编程语言。JavaScript 错误是页面编程代码中的漏洞（bug）。

在互联网的早期，网页仅限于使用超文本标记语言（HTML）。HTML 是所有浏览器用于显示网页的通用标准。HTML 处理字体样式、链接和图片等内容，这在初已经足够，但人们对网页有了更高的要求。

他们使用了一种为 JavaScript 开发的编程语言，即使是非程序员也能用它增强自己的网站。这种语言本身已经变得复杂，现在已成为一种像 HTML 一样被所有浏览器支持的标准。

JavaScript 的设计并不是为了运行极快，而是为了增强网页。随着互联网的演变，网页背后的编程变得越来越复杂，往往定义了 JavaScript 的限制。所有的编程工作都转移到了服务器端，而不是全部下载。

运行中的 JavaScript 目前被网站用于驱动用户界面。虽然现代网站与服务器通信以获取数据，但速度可能很慢。如果服务器出现问题，用户界面的响应能力至关重要，界面通常用 JavaScript 编写并在你的计算机上运行，而复杂的代码则在服务器上运行。

像任何语言一样，JavaScript 会有漏洞，有时会导致程序失败。幸运的是，当 JavaScript 失败时，页面仍然运行。

## 消除 Internet Explorer JavaScript 警告

你遇到的大多数 JavaScript 错误都是由于单个网页的失败。通常这些错误是：虽然你丢失了一些功能，但它们对你的计算机没有危险。然而，Internet Explorer 默认会弹出一个警告。这会阻止你在页面上进行任何操作，并可能令人厌恼。如果你是一个查看代码的程序员，这对你是没用的。

要消除对话框，请按照以下步骤操作：

1. 在 Internet Explorer 中，从菜单选择 `Internet Options`。
2. 点击 `Advanced`（高级）选项卡。
3. 根据你使用的版本，你需要设置（勾选其中两个）：
   - `Disable debugging (Internet Explorer)`
   - `Disable script (Other)`
   - `Display a notification about error`（显示关于错误的通知）
4. 点击 OK 按钮。

这应该会停止对话框的显示。如果你开始遇到网页问题，可能是浏览器的问题，而不是网页的问题，你可能需要重新安装 Internet Explorer。

## 关于 JavaScript 的错误

对于大多数计算机用户来说，JavaScript 是件新事物。除了 PC 专业人士，大多数人对它知之甚。本质上，JavaScript 是一种最用于网站的 Web 开发语言。JavaScript 因其友好的特性在非程序员中广受欢迎，它还允许访问嵌入其他应用程序中的对象。

然而，JavaScript 错误也相当常见，很大原因是许多业余爱好者使用它编写开发程序。但糟糕的是，它也可以被用来编写广告软件和间谍软件，这些软件会进入你的计算机（往往在你毫无察觉的情况下），从而堵塞注册表。这反过来会减慢你的计算机速度并可能导致其崩溃，我们都知道这意味着多大的头疼。

1. 浏览器中未启用 JavaScript。
2. 网页包含 JavaScript 编程错误。
3. 浏览器不支持 JavaScript 技术。

我们可以做什么来处理这些问题？当然，你可以选择向网站管理员报告问题，并提供你收到的所有 JavaScript 错误消息的细节，但你有一个更简单的替代方案。只需清理 Windows 注册表，看着问题消失即可。

对于不了解此的人来说，Windows 注册表是一个巨大的内部数据库，你在系统上使用的所有程序（包括 Windows 本身）都在其中存储了大量数据。因此，每当你更改控制面板设置、文件关联、系统或安装新软件时，更改都会反映在注册表中。

对于某些网站构建者来说，遇到 JavaScript 错误可能是毁灭性的。这是一个常见的错误，但即使是简单的错误也会破坏网站效果，并让终端用户感到困惑和沮丧。这反过来也可能导致构建者损失资金并失去业务。

## 禁用 Firefox 浏览器的错误警告

帮助打破弹出错误警告循环的一种方法是手动更改启用或禁用警告弹窗的选项。要为 Mozilla Firefox 用户禁用这些警告，请执行以下操作：

1. 选择页面顶部的“工具 (Tool)”选项卡。
2. 点击“选项 (Options)”并在框顶部选择“内容 (Content)”选项卡。
3. 通过取消勾选“启用 JavaScript (Enable JavaScript)”复选框来禁用警告。

这将阻止警告在上网时干扰你。然而，即使禁用了警告，并不意味着错误已彻底消失。

### 尝试使用不同的网络浏览器

不同的浏览器对不同网站的反应不同。一个浏览器可能会遇到错误，而另一个则不会。如果错误仍然在浏览器中出现，请尝试使用别人的账户甚至别人的电脑。如果在使用别人的 PC 时错误停止了，那么可能是时候清理你的 PC 注册表了。

## 从 Internet Explorer 中删除临时 Internet 文件

你的浏览器会创建你访问过的地方副本并将其存储在临时文件中。这些文件的堆积会在系统中产生错误，需要定期清理。对于 Internet Explorer 用户，请执行以下操作：

1. 选择位于页面顶部的“工具 (Tools)”选项卡。
2. 选择“常规 (General)”选项卡。
3. 在“临时 Internet 文件 (Temporary Internet Files)”下选择“设置 (Settings)”。
4. 点击“删除文件 (Delete Files)”并按“确定”。
5. 点击“删除 Cookie (Delete Cookies)”并按“确定”。
6. 同时，在“历史记录 (History)”下选择“清除历史记录 (Clear History)”。
7. 选择“是”，然后点击“确定”。

### 维护你的 PC 注册表

如果 JavaScript 错误仍然存在，请使用注册表清理程序修复。持续使用 PC 会使其损坏，不断的信息流可能会阻塞你的注册表，减慢电脑速度。这些错误可能是由故障或损坏的注册表引起的。Optimize-Your-PC 可以为你提供先进的注册表清理技术。它将扫描、诊断并修复你的 JavaScript 错误，为你留下一个高度优化的 PC。

## 在 Dreamweaver 8 中添加 JavaScript

JavaScript 允许你在 Web 页面上添加交互元素并在上面执行脚本函数。在 Dreamweaver 8 中添加 JavaScript 并不困难，不需要你了解 JavaScript 编程。

在 Dreamweaver 8 中，JavaScript 是一种“行为 (behavior)”，通过行为面板 (Behaviours panel) 进行控制。当你向 Dreamweaver 8 中使用的 Web 页面添加 JavaScript 时，会用到行为面板。

要打开行为面板，选择 `Windows > Behaviours`。选择 `+` 按钮激活下拉菜单。“添加行为 (Add Behaviours)”下拉菜单包含大约二十种常见的 JavaScript 控制的函数，你可以将这些函数添加到 Dreamweaver 页面中。常见函数如检查浏览器类型和修订版本、检查插件、显示弹出消息、验证表单或转到 URL 等，都是你可能添加的 JavaScript 行为示例。

“添加行为”菜单中的每个行为都有一个对话框，允许你指定在遇到特定触发器时应该执行的操作。触发器是网站访问者可能执行的操作，例如点击链接、向表单输入数据或鼠标悬停在页面特定位置。

如果你从访问者那里收集信息，你会发现“验证表单 (Validate Form)”非常实用。用于验证访问者输入的数据符合正确格式的“验证表单”行为包含有效数据。一旦配置好该行为，点击确定。

如果你要添加的行为不在内置行为中，你可以选择 `获取更多 (Get More)`。这会将带你进入 Dreamweaver 网站。注意：并非所有行为都是免费的，但当你访问该网站时，你会发现添加新行为很容易的。你也可以更改已添加到 Dreamweaver 8 的行为。要修改现有的行为，找到你想要编辑的行为。选择它，它将出现在行为面板中“添加行为”按钮下方的列表中。从现在起，你可以修改事件发生的顺序，更改触发操作的事件或删除该行为。

根据统计，目前超过 89% 的网站使用 JavaScript 作为一种客户端语言。作为一种跨平台且轻量级的脚本语言，JavaScript 使得程序员能够更容易地构建出适用于各种浏览器和设备的响应式网站和 Web 应用程序。它被程序员广泛用于浏览器控制、用户交互和异步通信等重要任务。此外，程序员还可以选择通过 `Node.js` 和类似的运行时环境将 JavaScript 作为服务端脚本语言。同时，他们可以使用各种框架来减少构建应用程序所需的时间和精力。它还可以与 HTML 和 CSS 一起用于创建 Web 应用程序和游戏。你始终可以考虑使用 JavaScript 作为动态客户端语言来构建大型 Web 应用程序。

## 主流浏览器支持 JavaScript 的优势

JavaScript 支持大多数常用的网络浏览器，包括 Firefox、Chrome、Internet Explorer、Safari 和 Opera。它也得到了实现了 JavaScript 的新浏览器的支持。因此，用户无论选择何种浏览器，都可以使用 JavaScript 访问 Web 应用程序。由于某些原因脚本语言被禁用，他们还可以通过启用它来访问网站的所有功能。

### 无需使用任何特定工具

JavaScript 是一种解释型编程语言。因此，你可以轻松编写代码而不使用任何特定工具或程序。你只需打开记事本并开始编写 JavaScript 代码即可。此外，你还可以选择许多编辑器来识别代码中的错误。编辑器会对脚本进行着色或重新格式化，使用户更容易识别错误。

### 重用代码的选项

你只需通过将代码放在单独的文件中，就可以跨多个页面进一步复用 JavaScript 代码。将代码放在单独的文件后，你必须以 .js 扩展保存文件。可以通过页面 HTML 代码中的 `<script>` 标签将该文件链接到多个 Web 页面。此选项允许你在为网站部分添加相同功能时避免编写额外的代码。

### 许多库和框架

你可以使用几个框架来减少构建应用程序所需的时间和精力。许多程序员倾向于使用动态 JavaScript 框架，如 `AngularJS`、`Backbone`、`Ember` 和 `React`。然而，你仍然可以根据特定需求从长长的列表中进行选择。例如，可以使用 `DHTMLX`、`Bootstrap`、`jQuery UI`、`DojoWidgets` 或 `AngularJS` 等小组件进行 GUI 开发。

### 相对快速

如前所述，JavaScript 是一种客户端脚本语言。因此，代码在用户的系统上执行。由于代码是在不与服务器交互的情况下执行的，处理过程以较快的[速度]完成。更快的处理使得 Web 应用能够通过提供更丰富的浏览体验来让用户保持参与。

### 从服务器交付更新的响应数据

JavaScript 进一步使用 `XMLHttpRequest` API 进行数据检索。该 API 向 Web 服务器发送 HTTP 或 HTTPS 请求，并在脚本中加载服务器发送的响应。脚本可以根据从服务器收到的响应数据轻松更新当前网页，而无需重新加载新网页。因此，您可以在无需完全重新加载网页的情况下向用户提供更新的信息，从而提升 Web 应用的性能。

### 扩展网站功能

JavaScript 让您能够在不付出额外精力的情况下扩展 Web 应用的功能。您可以使用这种脚本语言在屏幕上创建视觉效果、计算数据并让网页更具交互性。JavaScript 还进一步允许您通过第三方脚本来扩展网站功能。这种灵活性使得您更容易在使用任何额外插件或工具的情况下为 Web 应用添加开箱即用的功能。

### 减轻服务器负载

服务器端脚本语言要求 Web 服务器在向用户发送响应之前处理用户请求。因此，尽管用户拥有高速连接，该过程仍需要额外的时间。但 JavaScript 代码在用户的机器上处理，不与 Web 浏览器交互。因此，Web 服务器的压力和负载大大减轻，同时用户可以获得快速响应。在构建大型网站时，您可以使用 JavaScript 为用户提供更快的响应，而不会给服务器带来压力。

### 优化本地缓存

JavaScript 可以配合 HTML5 一起使用，使用户在没有活动连接的情况下访问网站。这些技术在本地缓存数据方面非常有效，并在连接恢复之前保持 Web 应用的响应能力。您甚至可以使用 `localStorage` 等工具来跟踪对对象的更改，并在网络连接后将更改上传到 Web 服务器。这一选项使 Web 应用能够像 App 一样运行。

### 与其他 Web 技术协作

如前所述，JavaScript 开发者可以将其作为客户端和服务器端脚本语言。同时，您还可以选择将 JavaScript 作为客户端技术，与 `PHP`、`Perl` 和 `Java` 等广泛使用的 Web 技术一起使用。该脚本语言还广泛配合 HTML5 和 CSS 使用，用于开发可以使用同一代码库在各种设备上访问的响应式网站。

然而，在用 JavaScript 构建大型网站和应用程序时，必须记住它的一些主要缺点。由于 JavaScript 代码在 Web 浏览器上执行，它容易受到各种安全攻击。此外，由于各个浏览器的解释方式不同，代码会变得不可预测。包括 Google 在内的主流搜索引擎爬虫无法完全、充分地理解用 JavaScript 编写的客户端代码。因此，使用过多 JavaScript 的 Web 应用的搜索引擎排名和可见性将受到影响。但您仍然可以配合 HTML5 和 CSS 等其他流行的 Web 技术使用 JavaScript，创建可在多个设备、操作系统和浏览器上访问的健壮应用程序。

### 为什么公司要雇佣 JavaScript 开发者？

公司最近越来越重视雇佣 JavaScript 开发者。企业现在正花费大量的资金、时间和精力来招聘优秀的人才，特别是年轻和新入场的人才，主要是因为他们的专业质量，以及因为他们与最新的技术和开发趋势保持同步。有许多原因导致现代企业在 JavaScript 开发者身上投入资金。

企业青赖这些人员的首要原因是他们的教育背景。大多数候选人拥有软件工程、计算机科学、信息技术和其他与业务相关的学士学位。然而，公司更看重经验而非学位，那是另一个问题。

企业投入资金是因为对软件开发有坚实的理解。此外，他们拥有客户端和服务器端编程技能的强大事实。这不仅对 JavaScript 重要，对平台同样重要。此外，在特质方面，他们具有很强的分析能力，并拥有与团队其他人同步工作所需的心理素质。这本身就足以让公司雇佣他们。

除了所有这些问题，了解他们的职责并拥有优秀的眼光将大不相同。大多数 JavaScript 开发程序都是专门为用于网站和计算机系统的 Web 而设计和开发的。开发后，必须对程序进行适当评估。优秀的开发者还将具备评估这些编程脚本的知识，因此公司雇佣他们是为了降低成本，因为程序员既可以开发也能评估脚本。他们还擅长对语言进行大量测试，以确保在交付给客户之前其运行正常。他们还确保脚本完全没有 Bug。这些专业人士，尤其是新人，对最新的 Java 虚拟机或 `JVM` 语言有广泛知识，这有助于他们更快地完成任务。他们还擅长构建让语言变得更简单的应用程序。归结底，这为公司节省了大量资金。公司的关键是寻找参与软件开发社区的最优秀工程师，这样他们就能与最新技术保持同步，并在概念创造方面保持新鲜。这是为了确保企业能从投入到 JavaScript 开发者身上的投资中获得最大的回报，而他们是业务发展的支柱。专家不仅熟练且经验丰富，而且精通其他语言，如 `C++`、`.NET`、`Python` 等。他们拥有完美的技能，这一事实在开发中得到了体现。

### JavaScript 在何处

#### `<script>` 标签

在 HTML 中，JavaScript 代码必须插入 `<script>` 和 `</script>` 标签之间。

```html
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```

旧的 JavaScript 示例可能会使用 `type` 属性：

```html
<script type="text/javascript">
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```

`type` 属性不是必須。JavaScript 是 HTML 中的默认脚本语言。

#### `<head>` 或 `<body>` 中的 JavaScript

你可以在 HTML 文档中放置任意数量的脚本。

脚本可以放置在 HTML 页面的 `<body>` 部分、`<head>` 部分，或者两者都放置。

##### `<head>` 中的 JavaScript

在此示例中，一个 JavaScript 函数被放置在 HTML 页面的 `<head>` 部分。当点击按钮时，该函数会被调用（执行）：

###### 示例

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

##### `<body>` 中的 JavaScript

在此示例中，一个 JavaScript 函数被放置在 HTML 页面的 `<body>` 部分。当点击按钮时，该函数会被调用（执行）：

###### 示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>A Web Page</h1>
<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</body>
</html>
```

#### 外部 JavaScript

外部文件：`myScript.js`

```javascript
function myFunction() {
    document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

当同一段代码在多个不同的网页中用时，外部脚本非常实用。JavaScript 文件的扩展名为 `.js`。要使用外部脚本，将脚本文件名放在 `<script>` 标签的 `src` 属性中：

###### 示例

```html
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

你可以根据意愿将外部脚本引用放置在 `<head>` 或 `<body>` 中。脚本的行为将就像它恰好位于 `<script>` 标签所在的位置。外部脚本不能包含 `<script>` 标签。

##### 外部 JavaScript 的优势

将脚本放置在外部文件中具有某些优点：

- 它将 HTML 和代码分离
- 它让 HTML 和 JavaScript 更于阅读和维护
- 缓存的 JavaScript 文件可以加快页面加载

向一个页面添加多个脚本文件 - 使用多个 `<script>` 标签：

###### 示例

```html
<script src="myScript1.js"></script>
<script src="myScript2.js"></script>
```

##### 外部引用

外部脚本可以使用完整 URL 或相对于当前网页的路径进行引用。此示例使用完整 URL 链接到脚本：

```html
<script src="https://www.w3schools.com/js/myScript1.js"></script>
```

这链接到位于当前页面所在文件夹中的脚本：

```html
<script src="myScript.js"></script>
```

## JavaScript 输出

JavaScript 可以以不同的方式“显示”数据：

- 使用 `window.alert()` 写入警框。
- 使用 `document.write()` 写入 HTML 输出。
- 使用 `innerHTML` 写入 HTML 元素。
- 使用 `console.log()` 写入浏览器控制台。

### 使用 `window.alert()`

你可以使用警告框来显示数据：

```html
<!DOCTYPE html>
<html>
<body>
<h1>First Web Page</h1>
<p>First paragraph.</p>
<script>
window.alert(5 + 6);
</script>
</body>
</html>
```

### 使用 `document.write()`

为了测试目的，使用 `document.write()` 是方便的：

```html
<!DOCTYPE html>
<html>
<body>
<h1>First Web Page</h1>
<p>First paragraph.</p>
<script>
document.write(5 + 6);
</script>
</body>
</html>
```

在 HTML 完全加载后使用 `document.write()`，将删除现有的 HTML：

```html
<!DOCTYPE html>
<html>
<body>
<h1>First Web Page</h1>
<p>First paragraph.</p>
<button onclick="document.write(5 + 6)">Try it</button>
</body>
</html>
```

### 使用 `innerHTML`

要访问 HTML 元素，JavaScript 可以使用 `document.getElementById(id)` 方法。`id` 属性定义 HTML 元素。`innerHTML` 属性定义 HTML 内容：

###### 示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>First Web Page</h1>
<p>First Paragraph</p>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 5 + 6;
</script>
</body>
</html>
```

要在 HTML 中“显示数据”（在大多数情况下），你将设置 `innerHTML` 属性的值。

### 使用 `console.log()`

在你的浏览器中，你可以使用 `console.log()` 方法显示数据：

###### 示例

```html
<!DOCTYPE html>
<html>
<body>
<h1>First Web Page</h1>
<p>First paragraph.</p>
<script>
console.log(5 + 6);
</script>
</body>
</html>
```

## JavaScript 语法

JavaScript 语法是构建 JavaScript 构造的规则集。

### JavaScript 程序

计算机程序是的一份供计算机“执行”的“指令”列表。在编程语言中，这些程序指令被称为语句。JavaScript 是一种编程语言。JavaScript 语句用分号隔开：

###### 示例

```javascript
var x, y;
x = 5;
y = x + y;
```

在 HTML 中，JavaScript 程序由浏览器执行。

### JavaScript 语句

JavaScript 语句由：值、表达式、关键字和注释组成。

### JavaScript 值

JavaScript 定义了两种类型的值：固定值和变量值。固定值被称为字面量。变量值就是变量。

### JavaScript 字面量

编写固定值的最重要规则是：

- 数字用小数形式写：`10.5`, `100`
- 字符串是文本，写在双引号或单引号内：`"John Doe"`, `'John'`

### JavaScript 变量

在编程语言中，变量用于存储数据。JavaScript 使用 `var` 来声明变量。赋值运算符用于为变量赋值。在此示例中，`x` 被为一个变量。然后，给 `x` 赋值为 6：

```javascript
var x;
x = 6;
```

### JavaScript 运算符

JavaScript 使用赋值运算符 `=` 为变量赋值：

```javascript
var x, y;
x = 5;
y = 6;
```

JavaScript 使用算术运算符（`+`,`-`,`*`,`/`）计算值。

### JavaScript 表达式

表达式是值、变量和运算符的组合，它计算出一个值。这种组合被称为求值。例如，`5 * 10` 求值为 `50`。表达式也可以包含变量值：`x * 10`。值可以是各种类型，如数字和字符串。例如，`"John" + " " + "Doe"` 求值为 `"John Doe"`。

### JavaScript 关键字

JavaScript 关键字用于标识要执行的操作。`var` 关键字告诉浏览器创建变量：

```javascript
var x, y;
x = 5 + 6;
y = x * 10;
```

### JavaScript 注释

并不是所有的 JavaScript 语句都会“执行”。双斜杠 `//` 之后以及 `/* */` 之间的代码被视为注释。注释会被忽略，不会被执行：

```javascript
var x = 5; // 我将被执行
// var x = 6 我将不会执行
```

## JavaScript 标识符

标识符是名称。在 JavaScript 中，标识符用于命名变量（以及关键字、函数和标签）。大多数编程语言的命名规则相似。在 JavaScript 中，标识符的第一个字符必须是字母、下划线（`_`）或美元符号（`$`）。后续字符可以是字母、数字、下划线或美元符号。数字不允许作为第一个字符。这样 JavaScript 就可以轻松区分标识符和数字。

### JavaScript 是大小写敏感

所有的 JavaScript 标识符区分大小写。`lastName` 和 `lastname` 是两个不同的变量：

```javascript
var lastname, lastName;
lastName = "Doe";
lastname = "Person";
```

### JavaScript 与驼峰命名法

历史上，程序员使用三种方法将多个单词合并为一个变量名：

- **连字符**：`first-name`, `last-name`, `master-card`, `inter-city`。JavaScript 不允许连字符。它被保留用于减法。
- **下划线**：`first_name`, `last_name`, `master_card`, `inter_city`.
- **驼峰命名法 (Camel Case)**：`FirstName`, `LastName`, `MasterCard`, `InterCity`.
- **小驼峰命名 (camelCase)**：JavaScript 程序员倾向于使用首字母小写的驼峰命名：`firstName`, `lastName`, `masterCard`, `interCity`.

### JavaScript 字符集

JavaScript 使用 Unicode 字符集。Unicode 涵盖了（几乎）世界上所有的字符、标点和符号。

### JavaScript 语句

此语句告诉浏览器在 `id="demo"` 的 HTML 元素中写入 "Hello Dolly."：

###### 示例

```javascript
document.getElementById("demo").innerHTML = "Hello Dolly.";
```

### JavaScript 程序

大多数 JavaScript 程序都包含许多 JavaScript 语句。这些语句按照编写顺序逐个执行。在这个示例中，`x`、`y` 和 `z` 被赋予了值，最后显示了 `z`：

###### 示例

```javascript
var x, y, z;
x = 5;
y = 6;
z = x + y;
document.getElementById("demo").innerHTML = z;
```

JavaScript 程序（以及 JavaScript 语句）通常被称为 JavaScript 代码。

### 分号 ;

分号用于分隔 JavaScript 语句。在每条可执行语句末尾添加分号：

```javascript
var a, b, c;
a = 5;
b = 6;
c = a + b;
```

用分号分隔时，允许在一行中使用多个语句：

`a = 5; b = 6; c = a + b;`

在 Web 上，你可能会看到没有分号的示例。语句结尾不强制要求分号，但强烈建议这样做。

### JavaScript 空格

JavaScript 会忽略多个空格。你可以在脚本中添加空格来提高其可读性。以下行是等价的：

```javascript
var person = "Hge";
var person="Huge";
```

良好的做法是在运算符（`= + - * /`）周围放置空格：

```javascript
var x = y + z;
```

### JavaScript 行长度与换行

为了获得最佳的可读性，程序员通常喜欢避免代码行超过 80 个字符。如果一个 JavaScript 语句无法在一行内，最佳断行位置是运算符之后：

###### 示例

```javascript
document.getElementById("demo").innerHTML =
"Hello Dolly.";
```

### JavaScript 代码块

JavaScript 语句可以组合在位于大括号 `{...}` 内部的代码块中。代码块的目的是定义要一起执行的语句。你可以在 JavaScript 函数中发现语句被分组在块中的情况：

###### 示例

```javascript
function myFunction() {
    document.getElementById("demo1").innerHTML = "Hello Dolly.";
    document.getElementById("demo2").innerHTML = "How are you?";
}
```

### JavaScript 关键字

JavaScript 语句通常以关键字开头，以标识要执行的 JavaScript 操作。以下是你在本教程中将学习的一些关键字列表：

| 关键字 | 描述 |
| :--- | :--- |
| `break` | 终止 switch 或循环 |
| `continue` | 跳出循环并从顶部开始 |
| `debugger` | 停止 JavaScript 的执行，并（如果可用）进行调试 |
| `do ... while` | 执行代码块，并在条件为真时重复该块 |
| `function` | 定义函数 |
| `if ... else` | 标记一个取决于条件的语句块 |
| `return` | 退出函数 |
| `switch` | 标记不同情况的语句块 |
| `try` | 错误处理 |

### JavaScript 注释

JavaScript 注释可以解释 JavaScript 并提高其可读性。JavaScript 注释还用于在测试时防止执行。

#### 单行注释

单行注释以 `//` 开头。`//` 到行尾之间的任何文本都会被忽略（不会被执行）。此示例在每行代码之前使用单行注释：

```javascript
// 修改标题
document.getElementById("myH").innerHTML = "First Page";
// 修改段落
document.getElementById("myP").innerHTML = "first paragraph.";
```

此示例在每行的末尾使用单行注释来解释代码：

```javascript
var x = 5; // 声明 x，并赋值赋值为 5
var y = x + 2; // 声明 y，并赋值为 x + 2
```

#### 多行注释

多行注释以 `/*` 开头，以 `*/` 结尾。`/*` 和 `*/` 之间的任何文本会被 JavaScript 忽略。此示例使用多行注释（注释块）来解释代码：

```javascript
/*
下面的代码将更改
我的页面中 id = "myH" 的标题
以及 id = "myP" 的段落：
*/
document.getElementById("myH").innerHTML = "First Page";
document.getElementById("myP").innerHTML = "first paragraph.";
```

#### 使用注释防止执行

使用注释防止代码执行适用于测试。在代码行前添加 `//` 可以将该代码行从可执行行变为注释。此示例使用 `//` 防止执行其中一行代码：

此示例使用注释块防止多行代码执行：

```javascript
/*
document.getElementById("myH").innerHTML = "First Page";
document.getElementById("myP").innerHTML = "first paragraph.";
*/
```

### JavaScript 变量

JavaScript 变量是存储数据值的容器。在这个示例中，`x`、`y` 和 `z` 是变量：

```javascript
var x = 5;
var y = 6;
z = x + y;
```

从示例中，你可以预期：

* `x` 存储 5
* `y` 存储 6
* `z` 存储 11

### JavaScript 命名

JavaScript 变量标识符规定：

* 名称必须以字母开头
* 名称也可以也可以以 `$` 或 `_` 开头
* 不能使用保留字作为名称
* 名称对大小写敏感

### 赋值运算符

在 JavaScript 中，等号 `=` 是“赋值”运算符，而不是“相等”运算符。这与代数不同。以下内容在代数中没有意义：`x = x + 5`。但在 JavaScript 中，它是意义的：它将 `x + 5` 的值赋值给 `x`。（它计算 `x + 5` 的值并将结果放入 `x` 中）。

“等于”运算符在 JavaScript 中写为 `==`。

### JavaScript 数据类型

JavaScript 变量可以持有像 100 这样的数字和像 "John Doe" 这样的文本值。JavaScript 可以处理许多类型的数据，但目前只需考虑数字和字符串。

字符串写在双引号或单引号内。数字不带引号。如果你把数字放在引号中，它将被视为文本字符串。

```javascript
var pi = 3.14;
var person = "John Doe";
var answer = 'Yes I am!';
```

声明后，变量没有值。（技术上讲，它的值为 `undefined`）

要给变量赋值，请使用等号：

```javascript
carName = "Volvo";
```

你也可以在声明变量时同时给它赋值：

```javascript
var carName = "Volvo";
```

在下面的示例中，我们创建了一个名为 `carName` 的变量，并给它赋值为 "Volvo"。然后，我们在一个 `id="demo"` 的 HTML 段落中“输出”该值：

###### 示例

```html
<p id="demo"></p>
<script>
var carName = "Volvo";
document.getElementById("demo").innerHTML = carName;
</script>
```

## 一条语句，多个变量

你可以在一个语句中声明多个变量。以 `var` 开始该语句，并用逗号分隔变量：

```javascript
var person = "John Doe", carName = "Volvo", price = 200;
```

声明可以跨越多行：

```javascript
var person = "John Doe",
carName = "Volvo",
price = 200;
```

## 值为 undefined

在计算机程序中，变量通常在声明时不赋值。该值可以是必须计算的内容，也可以是以后提供的的内容，例如用户输入。

未赋值时声明的变量，其值为 `undefined`。在执行此语句后，变量 `carName` 的值为 `undefined`：

###### 示例

```javascript
var carName;
```

## 重新声明 JavaScript 变量

如果你重新声明一个 JavaScript 变量，它不会丢失原来的值。在执行这些语句后，变量 `carName` 仍然是 "Volvo"

###### 示例

```javascript
var carName = "Volvo";
var carName;
```

## JavaScript 算术

与代数一样，你可以对 JavaScript 变量进行算术运算，使用 `=` 和 `+` 等运算符：

###### 示例

```javascript
var x = 5 + 2 + 3;
```

你也可以相加字符串，但字符串会被拼接：

###### 示例

```javascript
var x = "John" + " " + "Doe";
```

再尝试这个：

###### 示例

```javascript
var x = "5" + 2 + 3;
```

### JavaScript 运算符

### 给变量赋值并求相加

```javascript
var x = 5;         // 将 5 赋值给 x
var y = 2;         // 将 2 赋值给 y
var z = x + y;     // 将 7 赋值给 z (x + y)
```

赋值运算符 (`=`) 为变量赋值。

### 赋值

```javascript
var x = 10;
```

### 加法

```javascript
var x = 5;
var y = 2;
var z = x + y;
```

乘法运算符 (`*`) 用于数字相乘。

### 乘法

```javascript
var x = 5;
var y = 2;
var z = x * y;
```

### 算术运算符

算术运算符用于执行数字算术运算：

| 运算符 | 描述 |
| :--- | :--- |
| `+` | 加法 |
| `-` | 减法 |
| `*` | 乘法 |
| `/` | 除法 |
| `%` | 取模 |
| `++` | 自增 |
| `--` | 自减 |

复合加赋值运算符 (`+=`) 为变量增加一个值。

### 赋值

```javascript
var x = 10;
x += 5;
```

赋值运算符在 JS 赋值图表中会有详细描述。

## JavaScript 字符串运算符

`+` 运算符也可以用于添加（拼接）字符串。

###### 示例

`+=` 赋值运算符也可以用于添加（拼接）字符串：

```javascript
txt1 = "What a very ";
txt1 += "nice day";
```

`txt1` 的结果将是：`What a very nice day`

用于字符串时，`+` 运算符被称为拼接运算符。

### 字符串与数字

相加两个数字将返回和，但相加一个数字和一个字符串将返回字符串：

###### 示例

```javascript
x = 5 + 5;
y = "5" + 5;
z = "Hello" + 5;
```

`x`、`y` 和 `z` 的结果将是：

- `10`
- `55`
- `Hello5`

如果你相加一个数字和一个字符串，结果将是字符串！

## JavaScript 比较运算符

| 运算符 | 描述 |
| :--- | :--- |
| `==` | 等于 |
| `===` | 值相等且类型相等 |
| `!=` | 不等于 |
| `!==` | 值不等或类型不相等 |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |
| `?` | 三元运算符 |

## JavaScript 逻辑运算符

| 运算符 | 描述 |
| :--- | :--- |
| `&&` | 逻辑与 |
| `||` | 逻辑或 |
| `!` | 逻辑非 |

## JavaScript 类型运算符

| 运算符 | 描述 |
| :--- | :--- |
| `typeof` | 返回变量的类型 |
| `instanceof` | 如果对象是某个类型的实例，则返回 true |

## Java 和 JavaScript

程序员面临的一个常见问题是混淆 Java 和 JavaScript。虽然这两种语言有相似之处，但它们是完全不同的物，且用于不同的应用。

Java 是一种由 Sun Microsystems 开发的通用编程语言，其特点是“编写一次，到处运行”。Java 代码在虚拟机内部执行，因此可以发布 Java 应用，而开发者无需担心它们可能运行在不同架构和系统。相反，JavaScript 是一种脚本语言。它仅用于网页。当网络浏览器加载页面时，它会执行其中的 JavaScript。代码可以改变网页的外观和行为。例如，JavaScript 代码可以用于创建下拉菜单。

然而，你仍然需要学习一些关于数据类型的知识，因为如果不指定你想要存储什么类型的信息，将会产生一些副作用。

无论如何，该信息仍然有一个变量名。这里有一个练习题，它可以：

1. 从提示框中收集信息，
2. 将其放入变量中，
3. 进行计算，并且
4. 通过警告框（alert）返回答案。

将以下代码添加到新网页中：

```javascript
var SquareThis = prompt("Enter a number you would like to square.");
var Answer;
Answer = SquareThis * SquareThis;
alert(Answer);
```

## 这段代码中的基础编程技能

1. 当你进行任何类型的编程时，你必须考虑计算机需要识别和保留哪些信息。然后，你创建变量来存储这些信息。在这个例子中，我们需要存储两部分信息：1) 将要平方的数字，2) 答案。
2. 你通过命名 `var`、空格和变量名来告诉 JavaScript 你想让存储信息。
3. 该脚本的第一行承担了三项任务：1) 它告诉 JavaScript 为变量 `SquareThis` 留出内存空间，2) 它使用预定义的函数提示用户输入一个数字，3) 它获取用户在提示框中输入的任何内容并将其放入 `SquareThis` 的内存空间中。
4. 注意，`prompt` 函数需要一个参数，就像 `alert()` 一样。注意参数位于 " " 中，这意味着该参数是一个字符串（String）数据类型。
5. 现在脚本需要一个变量来存放答案。这是通过 `var Answer;` 完成的。
6. 现在一切都就绪可以进行数学计算了：`Answer = SquareThis * SquareThis;`。告诉计算机执行什么数学运算的部分运算符。主要的运算符有 `+`、`-`、`*`、`/`（加、减、乘、除）。还有许多其他运算符。平方是任何数字乘以自身；因此这个公式将 `SquareThis` 乘以 `SquareThis`。
7. 程序得出了答案，但它需要告诉用户。我们再次使用一个警告框。
8. 现在更改公式以执行其他操作。尝试再添加另一个变量和另一个 `alert()` 来询问另一个数字（或多个）。

以下是一些供你实验的运算符：

| 运算符 | JavaScript 数学功能 |
| :--- | :--- |
| `+` | 两个数字相加 |
| `-` | 两个数字相减 |
| `/` | 两个数字相除 |
| `++` | 数字自加 1（只需要一个变量） |
| `--` | 数字自减 1（只需要一个变量） |

## 结论

HTML 可能不能用来替代 JavaScript。这两种编程语言完全不同，具有不同的功能、特性和能力。HTML 是一种标记语言，设计用于创建静态网页内容；而 JavaScript 是一种可以执行动态任务的编程语言。它可以反复用于网站的不同页面上。这可以通过将其外部化并放在单独的文件中，并将 JavaScript 文件链接到特定页面的 HTML 代码来实现。因此，通过在每个页面上添加正确的标签，可以将 JavaScript 添加到许多页面。

并不是每个拥有业务的人都精通 JavaScript 或知道如何使用它。由于 JavaScript 可以为网站增加许多方面的特性，使用它创建网站只会对你的网站有益。因此，如果你能聘请专业的网页设计公司来帮助你使用 JavaScript 构建网站，将始终非常有帮助。专业设计师团队可以与你坐在一起，理解你的业务，并考虑到你所有的业务需求来设计网站。

© Brian Draper
