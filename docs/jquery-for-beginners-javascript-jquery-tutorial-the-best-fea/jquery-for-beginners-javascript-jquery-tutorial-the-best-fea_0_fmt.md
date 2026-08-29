
# 初学者指南：jQuery 教程与最佳特性

## 引言

在异步 JavaScript 和 XML (`AJAX`) 出现之前，网页数据处理方式较为传统：信息字段接收数据，通过点击提交按钮收集，随后页面带 `POST` 或 `GET` 参数重新加载。对于未采用 AJAX 的开发者，这在某些场景下仍是可行方案。但越来越多的人转向异步开发模式，得益于 jQuery，这变得前所未有的简单。

AJAX 允许开发者在无需重新加载页面或页面特定部分的情况下处理输入信息。起步需下载 `jQuery` 库并在网站 `<head>` 部分引用，或直接引用 Google 托管的免费 `jQuery` 库（始终保持最新稳定版）。建议定期检查更新并更新引用。

准备就绪后，我们创建一个包含姓名和电话号码的基础通讯录。页面需两个 `div`：一个包含表单结构，另一个显示已保存的数据。

### 表单结构

姓名：<br>
电话：

结构就位后，引入 jQuery 核心概念：`$(document).ready()` 函数。该函数内的代码将在 DOM 构建完成后、页面内容完全加载前立即执行。请参考下方注释代码：

```javascript
$(document).ready(function() {
    // 加载目前保存在数据库中的数据
    $('#addressData').load('phoneNumbers.php');

    $('#submitMe').click(function() {
        // 当用户点击提交按钮时执行的函数
        var enteredName = $('#name').val();
        var enteredPhone = $('#phone').val();

        $('#addressData').load('phoneNumbers.php?name=' + enteredName + '&number=' + enteredPhone, function() {
            // 在请求成功执行后执行的函数
            alert('加载完成。');
        });
    });
});
```

在 `phoneNumbers.php` 中，需检查 `GET` 参数是否已设置。若已设置并提交，执行数据库 `INSERT` 操作，再 `SELECT` 信息并显示；若未设置，仅 `SELECT` 显示。

核心逻辑如下：

- 文档就绪时，从 `phoneNumbers.php` 加载数据库号码并输出至 `addressData` `div`。
- 用户点击提交按钮时，将表单信息发送至 `phoneNumbers.php`。
- PHP 脚本执行数据库插入并返回最新信息。
- 信息加载至 `addressData` `div`。
- 请求完成后，弹窗提示成功。

这实现了表单提交时仅重新加载单个 `div` 而非整个页面。文档可能有其他实现方式，此处为教学手动编写。

## 创建你的第一个 jQuery 插件

### 为什么要创建 jQuery 插件

有时需在代码中复用通用功能：可能需要一个函数访问 `jQuery` 选择器并对其执行特定操作；或将项目中的工具函数高效迁移至其他项目。编写插件是最佳选择。jQuery 跨平台、易学、易用，且拥有大量实用插件。

但现有插件可能无法完美匹配需求，或体积过大仅需部分功能。解决方案是自行编写。这听起来复杂实则简单。本教程将介绍编写基础插件的方法，包含选项配置与回调执行。

### 设置

可下载本教程完整项目。我们将制作一个简单的手风琴插件。在网站 `"js"` 目录下创建 `js` 文件，按惯例命名为 `"jquery.simpleaccordion.js"`（以 `"jquery."` 开头加插件名）。

需在基础 HTML 页面 (`index.html`) 中引入插件文件与 `jQuery` 库。推荐从 Google CDN 引入 `jQuery`：全球分发节点带来更快响应，且用户访问时可能已缓存。

### jQuery 插件结构

jQuery 提供开发插件所需工具。为遵循 JavaScript 良好实践，确保代码在局部作用域内。基础框架如下：

```javascript
(function($) {
    $.fn.simpleAccordion = function() {
        // 基础手风琴插件代码
    };
}(jQuery));
```

准备就绪，开始编码。

## 为插件添加功能

jQuery 允许使用任意选择器。插件需处理多种组件类型，利用 `this` 关键字遍历每个组件应用功能，无需关心具体类型。

## 准备 HTML 部分 - 构建折叠面板

构建手风琴需如下 HTML 结构：

### 标题 1

Cras dolor elit, porttitor air conditioning diam bibendum, eleifend aliquam erat.

### 标题 2

Donec blandit risus nec est tristique interdum.

### 标题 3

Fusce sit amet arcu id justo malesuada faucibus.

### 标题 4

Aliquam tincidunt lobortis sem at porttitor.

基础结构包含四个标题及对应内容区。插件将把此 HTML 转换为可交互的手风琴，用户可展开/折叠区域。初始外观如下：

为美观添加基础样式：

```css
.accordion {
  width: 600px;
  border: 1px solid #ccc;
  border-bottom: none;
}
.accordion dt, .accordion dd {
  border-bottom: 1px solid #ccc;
  margin: 0px;
}
.accordion dt {
  background: rgba(193, 221, 252, 0.24);
  cursor: pointer;
  padding: 8px 4px;
  font-size: 14px;
  font-weight: bold;
}
.accordion dd {
  padding: 12px 8px;
}
```

应用样式后手风琴结构如下：

## jQuery 部分 - 让它运行起来！

修改 JS 文件添加核心功能代码：

```javascript
(function($) {
  $.fn.simpleAccordion = function(options) {
    return this.each(function() {
      var dts = $(this).children('dt');
      dts.click(accordionClick);
      dts.each(reset);
    });

    function accordionClick() {
      $(this).siblings('dt').each(hide);
      $(this).next().slideDown('fast');
      return false;
    }

    function hide() {
      $(this).next().slideUp('fast');
    }

    function reset() {
      $(this).next().hide();
    }
  };
})(jQuery);
```

代码解析：首先理解 jQuery 是扩展 JavaScript 的库。创建插件本质上是在扩展 jQuery 库，而 jQuery 扩展了 JavaScript。深入理解需掌握 JavaScript 原型属性，虽未直接使用，但 jQuery 的 `fn` 属性是原生 `prototype` 的别名，后台利用原型机制。简单说，通过 `fn` 扩展插件。

### 插件选项配置

插件可接受选项参数。相比传多个参数，使用 `options` 对象传递多属性是 jQuery 标准做法。最佳实践是用 `defaults` 对象设置默认值。`defaults` 与 `options` 均为纯对象，包含允许传递的属性。添加选项演示：

传入 `open` 选项控制手风琴初始化时首个面板是否展开。

```javascript
(function($) {
  $.fn.simpleAccordion = function(options) {
    var settings = $.extend({}, {open: false}, options);
    return this.each(function() {
      var dts = $(this).children('dt');
      dts.click(accordionClick);
      dts.each(reset);
      if(settings.open)
        $(this).children('dt:first-child').next().show();
    });

    function accordionClick() {
      $(this).siblings('dt').each(hide);
      $(this).next().slideDown('fast');
      return false;
    }

    function hide() {
      $(this).next().slideUp('fast');
    }

    function reset() {
      $(this).next().hide();
    }
  };
})(jQuery);
```

注意：默认值 `open: false` 意味着无选项传入时首个面板折叠。`$.extend` 合并对象：合并目标对象 `{}`、默认值 `{open: false}` 和用户传入的 `options`。

## jQuery 效果优于 Flash 动画的优势

jQuery 是为网页添加精美动画的优秀工具。Flash 动画曾广泛存在，但存在未解之痛点，jQuery 更好地解决了这些问题。虽非所有 Flash 动画可由 jQuery 实现，但持续进步与新插件推动开发者以 jQuery 替代 Flash。以下是 jQuery 效果相比 Flash 的优势：

### 1. 加载速度更快

执行 jQuery 效果无需额外插件。99% 浏览器支持 JavaScript，完整的 JS 引擎即可运行 jQuery。无额外插件加载，速度远超 Flash。Flash 需外部插件，若浏览器缺失特定版本，插件会在动画开始前加载，导致 Flash 整个生命周期耗时更长。

### 2. 高级效果制作更容易

Flash 高级效果需深厚的 ActionScript（Flash 脚本技术）知识。反之，jQuery 高级效果制作极简。官网提供大量尖端插件，即使初级工程师也能高效下载应用于 Web 应用。

### 3. 移动端表现更优

jQuery 比 Flash 更现代，适应性更强。许多主流移动框架不支持 Flash 动画，而 jQuery 在各类移动框架和浏览器中无缝运行。

# jQuery 插件生态

jQuery 插件数量庞大且持续更新。插件是提供核心 `jQuery` 库额外功能的库文件。分类下有海量插件，开发者可按需筛选。插件持续更新以适配操作系统和浏览器新进展。

## jQuery JavaScript 教程

`jQuery` 是广泛使用的 `JavaScript` 库，简化网站结构化开发。设计师偏爱 `jQuery` 而非原生 `JavaScript`，因其先进特性与简易性。实现同等功能，`jQuery` 代码量远少于 `JavaScript`（专家估计 1 行顶 20 行）。

`jQuery` 用于：选择页面元素、创建排版布局、通过修改外观/样式/可见性/文本/HTML 控制元素。体积小、执行快。还能将客户端脚本从 HTML 标记中分离。区别于其他 JS 库，`jQuery` 内置大量功能。灵活性是亮点，兼容 `Internet Explorer`、`Mozilla Firefox`、`Safari` 等不同内核浏览器，免去为每个浏览器编写单独代码的麻烦。

`jQuery` 消除重复造轮子，处理事件、执行动画、无痛引入 `Ajax` 支持。特效出色：简单代码实现切换、淡入淡出、滑动等。

学习 `jQuery` 趣味且易上手，尤其对熟悉 `JavaScript` 者。网上有海量在线教程，结构清晰、分类详尽、附带示例、语法参考，部分提供“尝试一下”在线运行功能。

## jQuery 的最佳特性

历久弥新的 `jQuery` 将 `JavaScript` 代码推向新高度。用过 `JavaScript` 者大多熟知 `jQuery`。典型用户包括 Google、Facebook、Twitter。

## 什么造就了 jQuery

`jQuery` 让 `JavaScript` 编写更快、代码更少。核心优势：少代码实现灵活应用。`JavaScript` 是 `jQuery` 的基石（`jQuery` 由 `JavaScript` 编写）。`jQuery` 代码有两种形式：压缩版（生产环境）和未压缩版（开发调试）。

## 免费下载

`jQuery` 开源免费，插件库同样免费可用。

## jQuery 的典型应用场景

动画、数据库查询、幻灯片等。

- **制作动画**：滑动、淡入淡出效果。
- **制作幻灯片**：图片轮播是最著名特性之一。
- **下拉菜单**：带动画的级联下拉菜单。
- **DOM 操作**：简单脚本包含、修改、删除页面内容。
- **MySQL 查询**：无需刷新页面发送 `MySQL` 查询（配合后端 AJAX 实现）。
- **表单验证**：客户端表单验证。
- **交互简化**：创建直观用户界面。

## 兼容性运行

`JavaScript` 长期面临浏览器兼容性问题，`jQuery` 成功率更高。`jQuery` 不改变 `JavaScript` 本质，但让其更好用、更普及。

# 针对浏览器 JavaScript 问题的排查指南

修复 `JavaScript` 错误不难，但定位根因常需侦探般排查。多种因素导致错误，需逐步识别并修复。

### 如何启用活动脚本修复 JavaScript 错误

浏览网页时需确保启用活动脚本、`ActiveX 控件` 和 `Java` 小程序，这些是 `JavaScript` 正常运行的关键。若遇困难，请按以下步骤启用：

**Internet Explorer 8 (Windows)**

- 选择“工具”菜单。
- 点击“Internet 选项”。
- 选择“安全”选项卡。
- 点击“自定义级别”。
- 勾选“启用活动脚本”复选框。

**Mozilla Firefox 3.5 (Windows)**

- 菜单栏选择“工具”。
- 点击“选项”。
- 选择“内容”标签页。
- 勾选“启用 JavaScript”复选框。
- 点击确定。关闭 Firefox 重新打开。

### 禁用烦人的错误警告

若错误警告频繁骚扰但浏览器运行正常，可禁用 JS 错误通知。某些警告会导致死机或干扰功能。在 `Internet Explorer` 中操作：

**Internet Explorer 8 (Windows)**

- 选择“工具”菜单。
- 点击“Internet 选项”。
- 选择“高级”选项卡。
- 取消勾选“对每个脚本错误显示通知”复选框。
- 关闭浏览器重新打开。

若网页包含大量 JS 错误，建议用其他浏览器测试。应始终用不同浏览器交叉验证。若多浏览器均报错，基本可判定网页本身是错误源。

### 尝试运行注册表清理程序快速修复

若无法消除 JS 错误，可使用注册表清理工具。其扫描整个注册表并快速修复无效项。

掌握修复 JS 问题的方法，提升浏览器性能表现。

# 如何解决 `javascript:void(0)` 问题

许多用户点击链接时遇此问题，浏览器状态栏显示错误代码导致链接失效。这是页面加载 JS 遇阻时偶尔显示的错误消息。触发场景多样，根因各异，了解潜在原因对解决至关重要。

### 1. 弹出窗口拦截器

拦截器阻止 JS 执行的同时拦截广告弹窗。解决：调整拦截器设置或暂时禁用；或更换拦截器、查阅评测确认是否为罪魁祸首。

### 2. 网络代理服务器

代理服务器故障或拦截内容。解决：不使用代理、或换用不干扰下载的代理；检查代理与网页内容兼容性。

### 3. 不当的 JavaScript 编写

错误的 JS 代码导致报错。解决：通知网站管理员重写 JS。

### 4. JavaScript 被禁用

浏览器中 JS 被禁用。启用方法：
- **IE**：工具 > Internet 选项 > 安全 > 自定义级别 > 脚本 > 启用。
- **Firefox**：工具 > 选项 > 内容 > 勾选“启用 JavaScript”。

### 5. 浏览器升级

浏览器 JS 引擎损坏，需修复或升级浏览器。

### 根治 `javascript:void(0)` 的简单方法

因 `javascript:void(0)` 导致某些浏览器异常渲染页面，且当链接无 `href` URL 时常触发此表达式（浏览器不知如何响应）。解决：使用 `return false;` 阻止默认行为。

操作步骤（在文本编辑器中打开文件）：

1. 查找 `javascript:void(0)` 引用。
2. 将链接中的 `#` 替换为实际 URL 或 `#`。
3. 在 `onclick` 表达式中添加 `return false;`，使链接引用变为：`<a href="#" onclick="callFunction(); return false;">链接</a>`。
4. 将 `callFunction()` 替换为实际函数名。
5. 保存并关闭文件。
