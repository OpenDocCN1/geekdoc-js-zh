# 初学者指南 JQUERY：JavaScript：jQuery 教程：jQuery 的最佳特性：JavaScript, PHP, CSS, HTML




## 引言

在异步 JavaScript 和 XML (`AJAX`) 宇宙出现之前，在网页上处理创建的方式有些不寻常。信息字段接收数据，数据通常通过点击提交按钮进行收集，随后，你的页面会通过真实的 `POST` 或 `GET` 参数进行重新加载。对于那些尚未加入真实 AJAX 临时潮流的人来说——这确实可能是你以后会用上的一种方法。对于某些能力来说，这在目前可能是一个非凡的决定。无论如何，越来越多的人正在接受一种非并发的方式来处理他们的开发实践。得益于 JQuery 这个奇迹，这从未像现在这样来得简单。

AJAX 允许 Web 开发者处理输入信息，而无需重新加载页面、重新加载页面的特定部分，等等。要开始使用，你需要下载 `JQuery` 库并在你网站的 `<head>` 部分中引用它。这非常简单。另一种方法是直接引用 Google 提供的免费 `JQuery` 库——它们始终保持着最新的稳定版本。定期查询更新并更新你的内容引用。

当你准备好这些代码后，你就准备好开始使用 `JQuery` 库了。我们来创建一个包含名称和电话号码的超基础地址录吧。你在这里直接需要两个 `div`，一个包含结构，另一个包含我们目前保存的所有名称和电话号码。

### 标题：
电话：

好了，既然结构在位置内，这是一个引入一些 JQuery 的绝佳机会。该业务的主要收获是理解真实的 `$(document).ready()` 函数。设置在真实函数内的所有代码将在 DOM 构建完成后、但在页面内容通常被加载之前立即被堆栈（执行）。请查看下方的注释代码并尝试理解它。

```javascript
$(document).ready(function() {
    // 加载目前保存在数据库中的数据
    $('#addressData').load('phoneNumbers.php');

    $('#submitMe').click(function() {
        // 当客户端点击提交按钮时执行的函数
        var enteredName = $('#name').val();
        var enteredPhone = $('#phone').val();

        $('#addressData').load('phoneNumbers.php?name=' + enteredName + '&number=' + enteredPhone, function() {
            // 在请求成功执行后执行的函数
            alert('加载完成。');
        });
```

在你的 `phone numbers.PHP` 文件中，你应该检查 `GET` 参数是否已设置。如果它们已设置并提交，则在你的数据库中执行 `INSERT`，然后从数据库中 `SELECT` 你的电脑信息并显示。如果没有设置，只需在数据库中 `SELECT` 你的信息并显示。

通俗逻辑如下：
- 当文档可以编写时，从 `phoneNumbers.PHP` 加载数据库中保存的号码并将其输出放在 `address data` `div` 中。
- 当个人点击提交按钮时，将字段信息发送到 `phone numbers.PHP`。
- PHP 内容将执行数据库插入并在添加后返回新鲜出炉的信息。
- 这些细节被堆叠到 `address data` `div` 中。
- 请求完成后，显示一个警告框告诉顾客请求已成功。

你现在拥有的是在提交排序时简单重新加载单个 `div` 的基本案例，而不是期望重新加载整个页面。你会发现这部分特定文档的其他方法，但为了学习，我是手动编写的。

## 创建你的第一个 JQuery 插件

### 为什么要创建一个 jQuery 模块

偶尔，在你的代码中提供一些通用的功能是有帮助的。你可能需要一个单一函数，它可以访问一个 `jQuery` 选择器并在该选择器上执行特定操作。或者相反，你可能在其中一个任务中编写了一个工具函数，现在你需要能够将其有效地移动到不同的任务中。无论如何，编写一个模块都是你的最佳选择。`jquery` 是不可错的。它是跨平台的、易于学习的，并让你非常容易使用界面。它还带有许多实用的模块，可以完成你想要的任何事情。

然而，偶尔仅仅有很多是不够的，想象一种你找不到适合你要求的完美模块的情况。或者，可能存在一个模块，但它太大了，而你只需要它的部分。方案可能是亲力而编写自己的东西。毕竟，这听起来比实际的要复杂。这个简短的练习将介绍编写基础模块的方法，包括一些选项，甚至执行一个回调。

### 设置

你可以下载此练习的完整项目。我们将制作一个简单的手风琴（accordion）模块。我们来创建一个 `js` 记录并将其放在网站的 `"js"` 目录中。所有 `js` 模块文档的习惯做法是以 `"jquery speck"` 开头，后面跟着真实的模块名，所以我们将命名为 `"jquery.simpleaccordion.js"`。

- 我们网站注册中 js 目录下的模块文档

现在我们必须将我们的模块文档与 `jQuery` 库一起包含到我们的基础 HTML 页面(`index.html`) 中。从 Google 正地引入 `jQuery` 库是最佳实践，因为它们在全球范围内分布，而不是你的单个工作区域：对于大多数人意味着更快的响应时间。从 Google 包含 `jQuery` 的另一个优势是，当客人访问你的网站时，他们现在已经在本地作用域中拥有 `jQuery` 内容。

### jQuery 插件结构

jQuery 提供了所有必要的工具帮助你开发我们的模块。尽管如此，为了保持 JavaScript 的良好实践，我们应该确保一切都在本地作用域内。我们从 jQuery 模块的基本框架开始：

```javascript
(function($) {
    $.fn.simpleAccordion = function() {
        // ：基础手风琴模块的代码
    }
}(jQuery));
```





既然所有的部分都已就绪，让我们开始动手吧！

## 为我们的插件添加功能

jQuery 的惊人之处在于它允许你使用任何需要的选择器。在任何情况下，你应该记住，我们的模块可以管理几种不同的组件类型。利用 `this` 关键字允许我们的插件通过遍历每个组件来应用相关功能，而无需关注组件类型。

## 准备 HTML 部分 -构建折叠面板

由于我们正在构建一个折叠面板，我们需要为它准备 HTML 结构，如下：

### 标题 1
Cras dolor elit, porttitor air conditioning diam bibendum, eleifend aliquam erat.

### 标题 2
Donec blandit risus nec est tristique interdum.

### 标题 3
Fusce sit amet arcu id justo malesuada faucibus.

### 标题 4
Aliquam tincidunt lobortis sem at porttitor.

这是一个基础的折叠面板结构，包含四个标题和它们各自的内容区域。因此，我们的想法是让模块将这段 HTML 代码转换为实用的折叠面板，用户可以在其中展开和折叠不同的区域。在进一步通知之前，它的外观应该是这样的：

为了美观起，我们应该包含一些简单的样式。代码如下：

```css
.accordion {
  width: 600px;
  outskirt: 1px strong #ccc;
  outskirt base: none;
}
.accordion dt,.accordion dd {
  outskirt base: 1px strong #ccc;
  edge: 0px;
}
.accordion dt {
  foundation: rgba(193, 221, 252, 0.24);
  cursor: pointer;
  cushioning: 8px 4px; text dimension: 14px;
  textual style weight: strong;
}
.accordion dd {
  cushioning: 12px 8px;
}
```

现在我们的折叠面板结构应该像这样：

## jQuery 部分 - 让它运行起来！

为了给模块添加实用性，我们将修改 JS 并包含以下代码：

```javascript
(function($) {
  $.fn.simpleAccordion = function(options) {
    return this.each(function() {
      var dts = $(this).children('dt');
      dts.click(accordionClick); dts.each(reset);
    });

    function accordionClick() {
      $(this).siblings('dt').each(hide);
      $(this).next().slideDown('fast');
      return bogus;
    }

    function stow away() {
      $(this).next().slideUp('fast');
    }

    function reset() {
      $(this).next().hide();
    }
  }
})(jQuery);
```

现在让我们来说过一下这段代码在做什么。首先，你必须理解 jQuery 是一个扩展 JavaScript 语言的库。在创建任何 jQuery 模块时，你基本上是在扩展 jQuery 库，而 jQuery 正在扩展 JavaScript。真正理解你的模块如何扩展 jQuery 库需要对 JavaScript 的模型属性有深入理解。尽管没有被直接使用，但 JavaScript 模型属性是通过 jQuery 属性 `fn` 在后台使用的，`fn` 是本地 JavaScript 模型属性的 jQuery 别名。

简单来说，你通过利用 `fn` 从 jQuery 扩展了你的模块。

### "你的模块名称"

此外，我们可以为模块添加选项。一个 jQuery 模块可以包含默认值和选项。选项是你传递给模块的参数。与发送几个参数相比，使用 `choices` 对象可以发送多个属性，这是 jQuery 的标准做法。在模块中允许选项时，最佳实践是使用 `defaults` 对象设置默认选项。就像 `choices` 一样，`defaults` 是一个严格的对象，它应该包含你允许传递给模块的属性。我们应该快速为我们的模块添加几个选项，以展示这是有多简单。

我们将传递一个边界选项，以便在折叠面板首次折叠时让其主区域打开。

```javascript
(function($) {
  $.fn.simpleAccordion = function(options) {
    var state = $.extend({}, {open: false}, choices);
    return this.each(function() {
      var dts = $(this).children('dt');
      dts.click(accordionClick); dts.each(reset);
      if(state.open)
        $(this).children('dt:firstchild').next().show();
    });

    function accordionClick() {
      $(this).siblings('dt').each(hide);
      $(this).next().slideDown('fast');
      return bogus;
    }

    function cover up() {
      $(this).next().slideUp('fast');
    }

    function reset() {
      $(this).next().hide();
    }
  }
})(jQuery);
```

你可能注意到，我们使用了 `open: false` 的默认估计，所以如果没有传递任何选项，模块将预期在首次折叠时折叠面板是关闭的。当模块获取选项时，你可以依赖 `$.extend` 方法来进行实际合并。`$.extend` 方法的作用是合并至少两个项目。

## jQuery 效果优于 Flash 动画的优势

jQuery 是一种非常棒的编程工具，可以为网页添加精美的动画。jQuery 已经存在很久了。使用 Flash 的活动出现在大量网站中。然而，Flash 在方面存在一些今天尚未解决的问题。这些问题通过 jQuery 得到了更好的解决。并不是所有 Flash 能实现的动画都能通过 jQuery 实现，但持续的进展和新模块已经激励了开发者用 jQuery 效果替换许多 Flash 效果。让我们来聊 jQuery 效果相比 Flash 的优势。

### 1. jQuery 效果的加载速度比 Flash 制作的更快
执行 jQuery 效果不需要额外的模块。99% 的程序都支持 JavaScript。一个完美的 JavaScript 程序就足够执行 jQuery 了。由于不包含额外的模块，jQuery 效果的加载速度比 Flash 快得多。请记住，Flash 需要外部模块才能执行。如果程序没有正确形式的 Flash 模块来执行特定活动，那么模块将在动画开始之前堆栈。这使得整个 Flash 的运行生命周期低于 jQuery。

### 2. 进的 jQuery 效果制作并不困难
要使用 jQuery 制作高级的效果，开发者必须在 Action 内容方面拥有深厚的知识（Action 是 Flash 使用的脚本技术）。相反，制作高级的 jQuery 效果非常简单。jQuery 官网提供了许多尖端模块。事实上，即使是初级软件工程师也可以在 Web 应用中有效地下载并使用它们。

### 3. jQuery 移动效果优于 Flash 制作
jQuery 比 Flash 更现代。因此，与 Flash 相比，jQuery 具有更好的适应性。实际上，许多著名的移动框架尚未支持 Flash 动画。而 jQuery 在各种移动框架和程序中都能无缝执行。





# jQuery 模块

jQuery 模块数量丰富，并且在不断更新。jQuery 模块是库文档，提供了可以添加到到核心 `jQuery` 库的额外功能。在插件分类下有许多模块。软件工程师可以查阅并选择一个完全符合其需求的模块。此外，这些模块会不断更新，以适应操作系统和程序开发的新进展。

## jQuery Javascript 教程

`jQuery` 是一个被广泛使用的 `Javascript` 库，因为它让网站的结构化变得简单。用迷人的颜色和格式设计网站是一件很有趣的事。设计师们倾向于使用 `jQuery` 而不是 `Javascript`，因为它具有许多先进特性，而且利用 `jQuery` 创建网页或应用程序非常简单。`jQuery` 的代码量比 `javascript` 少得多。专家们认为，在 `jQuery` 中用一行代码就能实现的结果，在 `Javascript` 中可能需要 20 行。

`jQuery` 可用于选择页面组件，创建组件的排列布局，通过更改它们的外观、样式、可见性、文本，甚至是它们的 `HTML` 来控制组件的排列布局。`jQuery` 并不大，执行其结果需要一些投入。它还被用于将客户端内容从 `HTML` 标记中分离。与其他 `javascript` 库完全不同，`jQuery` 包含了许多可以使用的功能。灵活性是 `jQuery` 的优秀特性之一，它可以很好地用于各种程序，如 `Internet Explorer`、`Mozilla Firefox` 或 `Safari`。由于这些每个程序的工作方式都不相同，我们有时被迫为每个程序编写单独的代码。

`jQuery` 消除了任务重复的困难性。它还可以用于处理事件、执行动画，并毫无复杂地将 `Ajax` 支持引入 Web 应用程序。同样，利用 `jQuery` 可以提供的特效是非常出的。人们可以使用简单的代码实现切换、模糊、响应。

学习 `jQuery` 既有趣又简单，因为内容易于理解。特别是对于熟悉 `Javascript` 的人来说，发现学习 `jQuery` 将轻而易举。网上有无数在线教程可以学习 `jQuery`。许多地方以易于理解的结构提供 `jQuery` 教程，并可以附带模型。它们为每个特性、功能等提供了完美安排的语法结构，分类在不同的分类下，使用户户立即看到内容。没有多少教程还带有“尝试一下”选项，除了通过模型理解外，它还允许用户尝试检查特效或结果。

## jQuery 的最佳特性

历久弥新的 `jQuery`。`jQuery` 将 `JavaScript` 代码提升到了前所未有的水平。如果你使用 `JavaScript`，你可能已经很熟悉 `jQuery`。卓越的模型包括 Google 指南、`Facebook` 和 `Twitter`。

## 是什么造了 jQuery

有了 `jQuery` 在你身边，它会让 `JavaScript` 部分更快，使用更少的代码。最受欢迎的元素是使用更少代码创建应用程序的灵活性。`JavaScript` 是 `jQuery` 的生产者，因为 `jQuery` 是用 `JavaScript` 写的。`jQuery` 代码有两种完全不同的类型：压缩记录和压缩文档。

## 允许下载

`JQuery` 开放下载并免费使用。你的库模块同样可用。

## jQuery 的理想选择

以下是一些你可以使用 `jQuery` 完成的任务。动画、数据库查询和幻灯片是其中的结果。
- **制作动画**：你可以制作滑动效果和模糊效果。
- **制作幻灯片**：创建图像或图片幻灯片是最著名的特性之一。
- **下拉菜单**：创建带有动画的级联下拉菜单的灵活性。
- **DOM 操作**：你可以使用基本内容包含、更改请求或删除网页上的内容。
- **MySQL 查询**：你可以在无需刷新页面的情况下向数据库发送 `MySQL` 问题。
- **结构验证**：你可以将其用于你的结构验证。
- **简化**：为你的网站客户创建直观的界面是有趣且令人兴奋的。

## 运行

`JavaScript` 在 Web 程序兼容性上一直存在问题，但 `jQuery` 有更高的成功率。`JQuery` 永远不会以任何形式改变 `JavaScript`，但它会变得更加有用，并且对设计师来说变得更加普通。

## 针对你的浏览器 JavaScript 问题启动调查

修复 `JavaScript` 问题并不困难，但有时很难确定问题的根源。各种问题都会导致 `JavaScript` 问题，因此你需要完成一些侦探工作来识别罪魁祸首并修复错误。

### 活动脚本如何修复 JavaScript 错误

浏览网页时始终开启活动脚本。你还需要确保启用了 `ActiveX 控件` 和 `Java` 小程序。这些关键选项对于 `JavaScript` 正常工作至关重要。如果你在使用 `JavaScript` 时遇到困难，那么你必须确保已启用动态脚本。这里是步骤：

**Web Explorer 8 (Windows)**
- 选择“工具”菜单。
- 点击“Web 选项”。
- 选择“安全”。
- 选择“自定义级别”。
- 勾选“启用活动脚本”旁边的复框。

**Mozilla Firefox 3.5 (Windows)**
- 从菜单栏选择“工具”。
- 点击“备选项”。
- 选择名为“内容”的标签页。
- 勾选“启用 JavaScript”旁边的框。
- 点击确定。关闭 Mozilla，然后重新打开。

字体 破坏心情的错误警告

如果烦人的警告不断骚扰你，但你的程序完全运行正常，那么你可能只需要禁用 JavaScript 错误警告。某些错误警告会导致你的电脑死机。它们还会干扰程序的实用性。在 `Internet Explorer` 中实现这一点非常简单。遵循以下方法：

**Web Explorer 8 (Windows)**
- 选择“工具”菜单。
- 点击“Web 选项”。
- 选择“高级”。
- 取消选择“对每个脚本错误显示通知”旁边的框框
- 关闭 Mozilla，然后重新打开。

如果一个网页看起来包含大量的 JavaScript 错误，那么它值得用另一个程序测试该网页。实际上，你应该始终使用不同的程序测试 JavaScript 错误。如果两个程序经历了类似的错误，那么几乎可以网页本身是 JavaScript 错误的来源。

### 为了快速解决，运行注册表清理程序

如果你无法摆脱这些 JavaScript 错误，请使用注册表清理程序。清理程序通过过滤你的整个错误库来工作。它随后迅速解决每个未创建的错误。




为了断开并修复这些错误，请熟悉修复你的 JavaScript 问题的方法，以便改进你程序的展示效果。

# 如何解决 JavaScript Void(0) 问题

许多网页客户端在尝试点击连接时遇到此问题，并在程序状态栏上看到此错误代码，导致连接无法正常工作。这是一种在处理网页页面加载 JavaScript 遇到问题时，在浏览器中偶尔显示的错误消息。尽管此错误消息会在不同的事件中触发，但对于不同的客户端，真实原因可能是多种，因此了解此错误消息背后的最潜在原因对于解决这些问题至关重要。

### 1. 弹出窗口拦截器
此错误消息的一个重要原因是弹出窗口拦截器阻止了 JavaScript，同时阻止了在不同位置以广告形式打开的窗口。解决这个问题包括根据你的需求更改弹出窗口拦截器的设置，并以此禁用拦截器。你甚至可以下载另一个弹出窗口拦截程序，或者阅读弹出窗口拦截器的产品评论，以评估它们是否确实导致了这些错误消息。

### 2. 网络代理服务器
网络代理服务器（用于访问不同的受限网站）的崩溃也会同时阻塞不同的内容。可以通过不使用代理服务器本身，或者使用功能更强且不会干预内容下载的代理服务器来避免此问题。同样，检查代理服务器与不同网页及内容的兼容性。

### 3. 不恰的 JavaScript
编写不当的 JavaScript 也可能导致此错误消息。解决方法是将此错误告知网站管理员，让他们重写 JavaScript。

### 4. JavaScript 被禁用
JavaScript 可能在你的程序中被禁用，应该将其启用。要在 `IE` 中启用，请转到工具菜单下网络选项中的安全选项的“脚本”选项卡；要在 `Firefox` 中启用，请转到工具菜单并在网页设置中启用 JavaScript 选项。

### 5. 浏览器升级
网页浏览器使用 JavaScript 时有时也会损坏，这需要更换或基本升级你的互联网浏览器。

有一种简单的方法可以让你从根本上真正避免 `javascript: void(0)` 错误消息，因为我们知道 `javascript: void(0)` 会导致某些程序异常地显示你的网站页面，而且当连接没有附加 URL 时，经常发生 `javascript: void(0)` 表达式，程序不知道如何响应并恢复错误消息。因此，请使用 `return false;` 语句让程序不要查找 URL。

尝试在任何文字处理程序中打开报告：
1. 在记录中找到 `javascript: void(0)` 引用。
2. 将连接中的 `#` 替换为标点 `.`。
3. 在表达式中添加 `return false` 语句，使连接引用显示为链接。
4. 将 `call function()` 替换为你的函数名；
5. 最后保存并关闭文档。

MALINA PRONTO
