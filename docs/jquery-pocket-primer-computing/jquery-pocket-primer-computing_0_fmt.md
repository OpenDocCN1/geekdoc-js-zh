
# Jquery 入门指南

```xml
<embed src="OEBPS/cover.xml">
```

![image](img/publisher.jpg)

我们所有的书目都在 authorcloudware.com 和其他数字供应商提供数字格式版本。可以通过联系 info@merclearning.com 获取本书目的的配套文件（图表和代码列表）。MERCURY LEARNING AND INFORMATION 对购买者的唯一义务是根据缺陷材料或工艺缺陷更换光盘，而不是基于产品的操作或功能。

我想将这本书献给我的父母——愿这能给他们的生活带来快乐和幸福。

```html
<script src="http://ajax.googleapis.com/ajax/libs/jqueryui/1.10.1/jquery-ui.min.js"></script>
```

你必须使用第二个 `<script>` 元素，因为第一个 `<script>` 元素无法正常工作。列表 1 显示了当你启动 HTML 页面并尝试拖放任何图像时，Web 检查器中的输出。

![image](img/fig1.jpg)

***图 1*** Web 检查器中来自 jQuery 迁移插件的错误消息。

如果你启动 HTML 页面并发现“晦涩”的错误消息，请检查 `jQuery` 网站获取基于 CDN 的 JavaScript 和 CSS 文件的最新版本并相应更新你的网页。如果这不能解决问题，请进行 Google 搜索，看看是否能找到该错误的解决方案链接。

## 关于技术编辑

Richard Clark, M.A. (@rdclark) 是一位丰富的软件开发人员和 Kaazing Corporation 的讲师。他曾在苹果和惠尔特公司任教，编写过沉浸式模拟程序，为财富 100 强企业开发了多个高性能 Web 应用，并发布了 Apple iOS 应用。作为国际会议上受欢的演讲者，他对利用移动、连接、实时应用程序来帮助人们更好地生活、工作和娱乐有浓厚兴趣。在空余时间，Richard 为非营利组织进行 Web 开发，打理种满加州本土植物的花园，并为家庭和慈善活动烹饪。

# 第 1 章：jQuery 概念

本章将向你介绍 `jQuery` 并提供使用 `jQuery` API 操作 HTML5 Web 页面中元素的示例。`jQuery` 是一个极其流行的基于 JavaScript 的开源工具包，它在 JavaScript 之上提供了一层抽象。此外，`jQuery` 支持多个浏览器，简化了你 HTML Web 页面中的代码。

`jQuery` 首页提供了源代码下载链接，以及文档、开发者资源和其他有用链接：

*[`jquery.org`](http://jquery.org)*

`jQuery` 是一个开源 JavaScript 工具包，让你能够编写跨浏览器和跨平台的 JavaScript 代码来管理 HTML Web 页面中的元素，这包括查找、创建、更新和删除元素，还包括元素属性，以及添加或移除元素样式属性的能力。

`jQuery` 的一些重要且实特性（不分特定顺序）包括其对跨浏览器代码的支持、第三方 `jQuery` 插件、主题化组件、事件处理、AJAX 支持以及简单的 DOM 遍历。

## 使用 jQuery 在页面中查找元素

一个关键点是，`$` 前缀是 `jQuery` 的简写形式。这意味着以下两行代码是等价的：

```javascript
var pElements1 = $("p");
var pElements2 = jQuery("p");
```

第三种选择是使用 `window.jQuery`，但这种用法不如使用 `$` 常见。

## 带有 jQuery 的“Hello World”网页

本节中的示例查找了单个 `<p>` 元素并更改其文本。稍后你还将看到操作多个 `<p>` 元素的修改后的代码。

列表 1.1 显示了 `HelloWorld1.html` 的内容，展示了如何为包含单个 `<p>` 元素的 HTML 页面添加 jQuery 功能。

![image](img/note.jpg) *列表 1.1 包含 console.log()，它在 WebKit 浏览器中可用，但在其他浏览器中可能需要某些类型的插件或扩展才能使用。*

***列表 1.1 HelloWorld1.html***

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>Hello World</title>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
</head>
<body>
  <p id="Steve">Hello World From a Paragraph</p>
  <script>
    $(document).ready(function(){
      // get the 'id' value
      var pId = $("p").attr("id");
      // get the text in the <p> element
      var pText = $("p").text();
      console.log(pId+" says "+pText);
      // update the text in the <p> element
      $("p").text("Goodbye World From a Paragraph");
      pText = $("p").text();
      console.log(pId+" says "+pText);
    });
  </script>
</body>
</html>
```

列表 1.1 使用此代码片段引用两个 jQuery 文件：

```html
<script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
<script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
```

重要：HTML `<body>` 元素中的第一个 HTML `<script>` 元素以此行开始：

```javascript
$(document).ready(function(){
  // do something here
});
```

前面的结构确保了 DOM 已加载到内存中，因此可以安全访问和操作 DOM 元素。

记住，你可以使用 `$` 符号表示 jQuery，并可以使用 jQuery 的 `attr()` 函数获取 HTML 元素（例如 `<p>` 元素）的属性值。例如，你可以按照以下方式获取 HTML `<p>` 元素的 `id` 属性值：

`var pId   = $("p").attr('id');`

你可以使用 jQuery 的 `text()` 函数获取 HTML `<p>` 元素中的文本字符串，如下：

```javascript
// get the text in the <p> element
var pText = $("p").text();
console.log (pId+' says '+pText);
```

最后，你可以使用相同的 `text()` 函数来更新 HTML `<p>` 元素中的文本，如下：

```javascript
// update the text in the <p> element
$("p").text("Goodbye World From a Paragraph");
```

在列表 1.1 中启动文件，并打开基于 WebKit 的浏览器中可用的检查器（Inspector）。接下来，选择“检查元素”（Inspect Element），并点击网页底部的“>>”符号以查看列表 1.1 中两个 `console.log()` 语句的输出。请记住，使用 Web 检查器的具体步骤在 Chrome 和 Safari 中不同，该顺序可能在这两个浏览器的未来版本中发生变化。

如果你还不知道，你可以使用 Chrome Web 检查器查看变量的内容，这对于调试非常有帮助。你可以尝试 Chrome Web 检查器的功能，还可以阅读有关这一优秀工具的在线教程。

## 使用 jQuery 查询和修改 DOM

本节将向你展示如何使用各种 jQuery 修饰符，这些修饰符可以非常方便地查找和更新 HTML5 网页中的元素。代码示例之所以短，是因为它们只说明了一个或两个选择符，但你可以组合它们来执行非常复杂的 DOM 遍历和对 DOM 元素进行上下文相关的修改。

本节代码示例中讨论的一些选择器包括 `:first`、`:last`、`:even` 和 `:odd`。选择器的部分列表包括 `:eq()`、`:lt()`、`:gt()`、`:has()`、`:contains()` 和 `:eq()`。

### 使用 :first 和 :last 选择符查找和修改元素

本节中的示例向你展示了如何使用 jQuery 的 `:first` 和 `:last` 选择符来操作 HTML 元素中的文本。

列表 1.2 显示 `JQModifyElements1.html` 的内容，说明了如何切换两个 `<p>` 元素的内容。

***列表 1.2 JQModifyElements1.html***

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery and Modifying Elements</title>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
</head>
<body>
  <p style="color:red" id="Steve">Hello From Paragraph One</p>
  <p style="color:blue" id="Dave">Goodbye From Paragraph Two</p>
  <script>
    $(document).ready(function(){
      // get information in first paragraph:
      var pId1   = $("p:first").attr('id');
      var pText1 = $("p:first").text();
      // get information in last paragraph:
      var pId2   = $("p:last").attr('id');
      var pText2 = $("p:last").text();
      $("p:first").html(pText2);
      $("p:last").html(pText1);
      //$("p:first").text(pText2);
      //$("p:last").text(pText1);
    });
  </script>
</body>
</html>
```

列表 1.2 使用此代码片段引用两个 jQuery 文件：（由于上所述，为了简洁省略）

`var pId1   = $("p:first").attr('id');`
`var pText1 = $("p:first").text();`
`var pId2   = $("p:last").attr('id');`
`var pText2 = $("p:last").text();`
`$("p:first").html(pText2);`
`$("p:last").html(pText1);`
`$("p").text("Goodbye World From a Paragraph");`
`$("#myInput").val()`
`$("#myInput").text("new value");`

图 1.1 显示了 `JQModifyElements1.html` 的结果。

![image](img/fig1.jpg)

***图 1.1***

下一节将向你展示如何使用 jQuery 选择符 `:even()` 和 `:odd()`。

### 使用 :eq, :lt 和 :gt 选择符查找元素

有许多 jQuery 函数可以执行复杂的操作。本节包含一些实用的代码片段，说明了部分：

`$('p:eq(3)').text('index equals three');`
`$('p:gt(3)').text('index is greater than three');`
`$('p:lt(3)').text('index is less than three');`

### jQuery 中的属性与属性





关于属性和元素的额外信息请此处：

- [`developer.mozilla.org/en-US/docs/DOM/element`](https://developer.mozilla.org/en-US/docs/DOM/element)
- [`stackoverflow.com/questions/5874652/prop-vs-attr`](http://stackoverflow.com/questions/5874652/prop-vs-attr)

jQuery 为属性提供了 `.prop()` 方法，为属性提供了 jQuery `.attr()` 方法。遗憾的是，jQuery 文档对 `.prop()` 方法和 `.attr()` 方法的描述是完全相同的：

“获取匹配元素集合中第一个元素的属性值，或为每个匹配元元素设置一个或多个属性。”

然而，好消息在以下述述中：

“为了保持向后兼容 [sic]，jQuery 1.6.1+ 中的 `.attr()` 方法将为您检索并更新该属性，因此不需要将布尔属性的代码更改为 `.prop()`。”

最安全的方法是对原始值（如布尔值或单值字符串）使用 jQuery 的 `.attr()` 方法，并对多值字符串（如“style”）使用 jQuery 的 `.prop()` 方法。考虑到这一点，下一节将向你展示如何在 jQuery 中处理属性。

### 查找和设置元素属性

你已经看到过如何使用各种 jQuery 函数来操作元素，以及如何查找属性值。本节包含了更新元素属性的示例。

以下代码段获取元素 `src` 属性的值：

```javascript
var $source = $("img").attr("src");
```

下一段代码显示了如何设置一个属性的值：

```javascript
$("img").attr("src", "/images/MyHouse.jpg");
```

以下代码段显示了如何在一个命令中设置多个属性（为了方便起分行显示）：

```javascript
$("img").attr({
    src: "/images/MyHouse.jpg",
    title: "House",
    alt: "House"
});
```

前一个代码段将属性 `src`、`title` 和 `alt` 的值设置为它们各自的值。

注意，jQuery `attr()` 方法的语法与 jQuery `css()` 方法非常相似，因此当你理解其中一个函数时，也会理解另一个。

### 使用自定属性

HTML5 支持自定义属性，前提是属性名称以字符串 `data-` 开头，后跟属性名称。虽然你现在可能不需要使用自定义属性，但 jQuery Mobile 高度依赖自定义属性，因此此功能非常有用。

你可以使用 jQuery 的 `.data()` 方法获取自定义属性的值。例如，假设你的 HTML 页面包含以下代码段：

```html
<div data-role="page" data-value="99" data-status="new"></div>
```

你可以按照以下方式获取这些自定义属性的值：

`$("div").data("role")` 返回值 page
`$("div").data("value")` 返回值 99
`$("div").data("status")` 返回值 true

你将在 jQuery Mobile 代码示例中看到更多操作自定义数据属性的示例，如果你真的很有野心，可以在 jQuery Mobile 源码中找到更多示例。

### 使用 jQuery 移除元素

正如你可能猜到的，jQuery 除了允许你查找和修改 HTML 页面中的元素外，还能移除元素。列表 1.3 包含了 HTML 页面 `JQRemovingElements1.html` 的，说明了如何通过 jQuery 移除元素。

**列表 1.3 JQRemovingElements1.html**

```html
<script>
  $(document).ready(function(){
    // 移除 <p> 元素 Dave
    $("#Dave").remove();
    // 移除 <p> 元素 Michelle
    $("div1").remove("#Michelle");
    // 移除包含 "Goodbye" 的 <p> 元素
    $("p").filter(":contains('Goodbye')").remove();
  });
</script>
```

列表 1.3 包含三行移除元素的代码，第一行所示（第二行类似）：

```javascript
// 移除 <p> 元素 Dave
$("#Dave").remove();
```

虽然前一个代码段的操作正如你预期的那样，但下面的代码段展示了 jQuery 的真实威力，它使用 jQuery 的 `filter()` 方法查找并移除所有包含字符串 Goodbye 的 HTML `<p>` 元素：

```javascript
$("p").filter(":contains('Goodbye')").remove();
```

将上述单行 jQuery 代码的简单直观性，与实现相同功能所需的相应 JavaScript 代码进行对比。

![image](img/fig1.2.jpg)

**图 1.2** 在 iPad3 上使用 jQuery 移除元素。

图 1.2 显示了从运行在 iPad3 上的 iOS 应用拍摄的竖屏截图中渲染 `RemovingElements1.html` 的结果。

### 创建 DOM 元素

jQuery 提供了 `clone()` 方法和 `append()` 方法来创建新的 DOM 元素。`clone()` 方法创建一个元素的真实副本。相反，`append()` 方法在指定的元素上操作。列表 1.4 显示了 `JQCreatingElements1.html` 的内容，说明了如何使用这两个 jQuery 方法在 HTML 页面中创建新元素。

**列表 1.4 JQCreatingElements1.html**

```html
<!DOCTYPE html>
<html lang="en">
<body>
  <script>
    $(document).ready(function(){
      // 将 Dave 元素的副本添加到 #div2：
      $("#Dave").clone().css({color:"#000"}).appendTo("#div2");
      // 将另一个 Dave 元素的副本添加到 #div2：
      $("#Dave").clone().css({color:"#000"})
      .appendTo("#div2");
      // 将 Dave 移动到 #div4 的末尾：
      $("#Dave").appendTo("#div4");
      // 在所有 'div' 元素之前添加 Dave：
      $("#Dave").clone().prependTo("div");
    });
  </script>
</body>
</html>
```

列表 1.3 引入了 `clone()` 方法，其示例所示：

```javascript
$("#Dave").clone().css({color:"#000"}).appendTo("#div2");
```

上述代码段的目的显而易见，你甚至可以从左到右读取它：克隆 id 为 Dave 的元素，将其颜色设置为黑色，并将此副本添加到 id 为 div 的元素中。

1.3 中的另一个新功能是 jQuery 的 `prependTo()` 函数，它将元素插入到指定元素之前（而不是之后），所示：

```javascript
$("#Dave").prependTo("div");
```

记住的另一个点：`clone(true)` 还会传播元素的事件处理器。还有其他插入 DOM 元素的 jQuery 方法，其中一些将在后面的章节描述。

图 1.3 显示了从运行在 iPad3 上的 iOS 应用拍摄的横屏截图中渲染 `JQCreatingElements1.html` 的结果。

![image](img/fig1.3.jpg)

**图 1.3** 在 iPad3 上使用 jQuery 创建元素。

### jQuery append() 和 appendTo() 方法

jQuery 文档对这两个方法提供了简洁明了的解释：

“`.append()` 和 `.appendTo()` 方法执行相同的任务。主要的区别在于语法——具体来说是内容和目标的位置。对于 `.append()`，方法之前的选择器表达式是插入内容的容器。另一方面，对于 `.appendTo()`，内容位于方法之前（无论是作为选择器表达式还是即时创建的标记），并被插入目标容器中。”

也许这个非正式的解释可以澄清这种差异：

`{select-something-here}.append(and-append-stuff-from-here)`
`{specify-stuff-here}.appendTo(and-append-that-stuff-here)`





本章包含了使用这些方法的代码示例，以便你能够记住这两个 jQuery 方法之间的区别。

## 实用的 jQuery 代码块

本节包含了一组代码片段，允许你执行条件逻辑，然后执行你的自定义代码。本节中的代码示例非常直观，并且注释解释了它们的用途。

检查 jQuery 是否已加载：

```javascript
if (typeof jQuery == 'undefined') {
   // jQuery 未加载
}
```

检查元素是否存在：

```javascript
if ( $('#myElement').length > 0 ) {
   // 元素存在
}
```

注意，前一个代码片段中的 `>` 符号在“真值（truthy）”风格的编程中通常会被省略，但在代码中保持显式写法是比较好的。

检查空元素：

```javascript
$('*').each(function() {
    if ($(this).text() == "") {
        //在此处执行某些操作
    }   
});
```

根据 `<div>` 元素的内容返回 true 或 false：

```javascript
var emptyTest = $('#myDiv').is(':empty');
```

确定复选框是否勾选（返回 true/false）：

```javascript
$('#checkBox').attr('checked');
```

查找所有已选的复选框：

```javascript
$('input[type=checkbox]:checked');
```

禁用/启用按钮元素的输入框：

```javascript
$("#submit-button").attr("disabled", true);
```

从按钮元素中移除属性：

```javascript
$("#submit-button").removeAttr("disabled");
```

上述代码片段让你了解了检查各种条件的紧凑方式。随着你对 jQuery 越来越熟练，你将开发出属于自己的有用代码片段。

现在，让我们来看另一类重要的 jQuery 函数，它们允许你在 DOM 之间进行导航，其中一些内容将在下一节中讨论。

## 在 jQuery 中处理点击事件

jQuery 支持各种类型的事件和用户手势，你可以将它们“绑定”到（你编写的）自定�代码上，每当这些事件或手势发生时，代码就会执行。在 jQuery Mobile 中可以检测并绑定的事件将在 jQuery Mobile 章节中讨论。

`click()` 函数允许你使用以下语法处理点击事件：

```javascript
$("#button1").click(function() {
      // 执行某些操作
});
```

处理事件有多种技术，这里展示了推荐的技巧：

```javascript
$("#button1").on("click"), function() {
      // 执行某些操作
}
```

`dblclick()` 函数允许你处理双击事件，其语法示例在此：

```javascript
    $("#button2").dblclick(function() {
      // 执行某些操作
    }
```

顺便提到，`focus()` 函数为选定的元素提供焦点。虽然这里没有涵盖，但你可以通过查阅在线文档获取更多信息。

列表 1.5 显示了 `JQClickDivs1.html` 的大部分内容，它说明了如何检测点击事件，然后更新此 HTML5 Web 页面中两个 `<div>` 元素的内容。

***列表 1.5 JQClickDivs1.html***

```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="utf-8" />
   <title>使用 jQuery 检测点击事件</title>
   <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
   <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
</head>
<body>
   <div id="div1">第一个 div 元素 </div>
   <div id="div2">第二个 div 元素 </div>
   <script>
    var click1=0, click2=0, total=0;
    $(document).ready(function() {
        $("#div1").click(function() {
          ++click1;
          ++total;
          $(this).text("Clicked: "+click1+" total: "+total);
          $("#div2").text("Clicked: "+click2+" total: "+total);
      });
      $("#div2").click(function() {
          ++click2;
          ++total;
          $(this).text("Clicked: "+click2+" total: "+total);
          $("#div1").text("Clicked: "+click1+" total: "+total);
      });
    });
  </script>
</body>
</html>
```

列表 1.5 引用了所需的 jQuery 文件，紧接着是一些 CSS 样式定义以及两个 HTML `<div>` 元素。这里显示了为第一个 HTML `<div>` 元素添加点击事件监听器的代码（对于第二个 HTML `<div>` 元素使用了类似的 jQuery 代码）：

```javascript
$("#div1").click(function() {
      ++click1;
      ++total;
      $(this).text("Clicked: "+click1+" total: "+total);
      $("#div2").text("Clicked: "+click2+" total: "+total);
});
```

每当用户点击上述 HTML `<div>` 元素时，它的点击计数和总点击计数都会加 1，并且两个 HTML `<div>` 元素的文本都会更新为对应单个 `<div>` 元素的点击次数以及总和。

## jQuery 函数链式调用 (#toc.html_toc-h1-0005)

你已经看到过 jQuery 命令链式调用的示例，可能在 Java 中也用过链式命令（特别是使用 JAXB 时），如下：

```
myList().getFirstElem().getCustomer().setFirstName("Dave");
```

jQuery 链式调用支持比上述代码段更复杂的操作。默认情况下，jQuery 会引用链中的第一个元素，但你可以更改默认行为。例如，你可以指示 jQuery 使用 `.parent()` 方法引用当前元素，执行某些操作，然后使用 jQuery 的 `.end()` 方法再次引用链中的第一个元素。

这里有一个很好的示例，说明了上一段落中讨论的信息：

[`blog.pengoworks.com/index.cfm/2007/10/26/jQuery-Understanding-the-chain`](http://blog.pengoworks.com/index.cfm/2007/10/26/jQuery-Understanding-the-chain)

请记住以下几点事项：在更改方法链中的默认行为时要格外小心，因为实际行为可能并不是你代码中预期的行为。此外，确保对此类代码进行清晰说明，以免困扰那些比你对 jQuery 了解少的人。

## 使用 jQuery 获取加速度计值 (#toc.html_toc-h1-0006)

本节的示例说明了你如何使用 jQuery 获取移动设备的加速度计值。

![image](img/cd.jpg)列表 1.6 显示了 `JQAccelerometer1.html` 的内容，它展示了当移动设备在任何方向发生加速时，如何显示加速度计的数值。CSS 样式表 `JQAccelerometer1.css` 包含了此处未显示的简单选择器，但你可以在 CD 上找到完整的列表。

***列表 1.6 JQAccelerometer1.html***

```html
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="utf-8">
 <title>jQuery and Accelerometer</title>
   <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
   <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
   <script>
     var colorX = "", colorY = "", colorZ = "";
     var intx = 0, inty = 0, intz = 0;
     var colors = ['#f00', '#ff0', '#00f'];
     $('document').ready(function(){
       $(window).bind("devicotion", function(e){
         var accelEvent = e.originalEvent,
             acceler = accelEvent.accelerationIncludingGravity,
             x = acceler.x, y = acceler.y, z = acceler.z;
       if(x < 0)      { intx = 0; }
       else if(x < 1) { intx = 1; }
       else             { intx = 2; }
       if(y < 0)      { inty = 0; }
       else if(y < 1) { inty = 1; }
       else             { inty = 2; }
       if(z < 0)      { intz = 0; }
       else if(z < 1) { intz = 1; }
       else             { intz = 2; }
       colorX = colors[x];
       colorY = colors[y];
       colorZ = colors[z];
       $("#valueX").css("backgroundColor", colorX);
       $("#valueY").css("backgroundColor", colorY);
       $("#valueZ").css("backgroundColor", colorZ);
       $("#valueX").html("<p>Acceleration x: <b>" + x + "</body></p>");
       $("#valueY").html("<p>Acceleration y: <b>" + x + "</body></p>");
       $("#valueZ").html("<p>Acceleration z: <b>" + x + "</body></p>");
       });
     });
   </script>
</head>
<body>
  <h2>Accelerometer Values</h2>
  <div id="outer">
   <div id="valueX"></div
   <div id="valueY"></div
   <div id="valueZ"></div>
  </div>
</body>
</html>
```

列表 1.6 中的代码获取移动设备三个方向（相互相互垂直）的加速度计值，然后执行一些算术计算，以计算出整数值作为颜色值数组的索引。在确定每个方向的颜色后，相关的 `div` 元素将更新为相应的颜色。

在将 `window` 对象绑定到 `devicotion` 事件后，我们可以使用事件对象（在此情况下称为 `e`）来获取加速度对象的 JavaScript 引用（称为 `acceler`）。然后我们可以提取三个不同轴的当前值，如下：

```javascript
$('document').ready(function(){
  $(window).bind("devicotion", function(e){
    var accelEvent = e.originalEvent,
        acceler = accelEvent.accelerationIncludingGravity,
        x = acceler.x, y = acceler.y, z = acceler.z;
  });
});
```

为了简单起见，颜色数组仅包含三种颜色，以下代码计算 0 到 2 之间的数字，以确定方向的颜色：

```javascript
if(x < 0)      { intx = 0; }
else if(x < 1) { intx = 1; }
else             { intx = 2; }
```

x 方向的颜色计算如下：

```javascript
colorX = colors[x];
```

与 x 方向相关的 `div` 元素将更新为相应的背景颜色：

```javascript
$("#valueX").css("backgroundColor", colorX);
```

最后，使用以下代码显示 x 方向的当前值：

```javascript
$("#valueX").html("<p>Acceleration x: <b>" + x + "</body></p>");
```

y 方向和 z 方向的相应值以类似的方式计算。

图 1.5 显示了列表 1.5 中 HTML 页面的渲染结果，这是从运行 Asus 平板上的 Android 应用截取的横屏截图。

![image](img/fig1.5.jpg)

***图 1.5***在 Asus 平板上的加速度计

## 总结 (#toc.html_h1-0007)

本章介绍了 jQuery，并提供了代码示例展示了如何使用 jQuery 函数操作 HTML 页面。你通过示例了解了如何：

* 创建一个基于 jQuery 的 HTML5 页面
* 使用 `:first` 和 `:last` 选择器查找元素
* 使用 `:even` 和 `:odd` 选择器查找元素
* 使用 `:eq`、`:lt` 和 `:gt` 选择器查找元素
* 通过类或 ID 查找元素
* 获取/设置属性
* 查找表单元素及其属性
* 用于查找元素的 CSS3 表达式
* 删除 DOM 元素
* 创建 DOM 元素
* 处理事件
* 使用 `click()` 函数
* jQuery 函数链式调用
* 使用 jQuery 获取加速度计

## CSS3 支持与 CSS3 属性的浏览器前缀

在我们深入研究 CSS3 细节之前，关于为 HTML 页面定义基于 CSS3 的选择器，有两个需要了解的重要细节。首先，你需要了解不同浏览器中可用的 CSS3 功能。确定 CSS3 功能浏览器支持的最佳网站之一是：

*[`caniuse.com/`](http://caniuse.com/)

上述链接包含了关于 IE、Firefox、Safari、Chrome、Opera 以及若干移动浏览器的 CSS3 支持情况的表格化信息。

另一个检查 CSS3 功能支持的非常有用的工具是 Enhance.js。它通过测试浏览器来确定它们是否支持某一组核心的 CSS 和 JavaScript 属性，然后为那些满足测试的浏览器提供相应的功能。你可以在这里下载 Enhance.js：

*[`github.com/filamentgroup/EnhanceJS`](https://github.com/filamentgroup/EnhanceJS)

第三个实用工具是 Modernizr，它用于检查各种浏览器中与 HTML5 功能的功能，其主页在此处：

*[`www.modernizr.com/`](http://www.modernizr.com/)

在某个时刻，你会在 HTML5 Web 页中使用 JavaScript（事实上，你可能已经在使用了），而 Modernizr 提供了一种编程方式来检查不同浏览器中的许多 HTML5 和 CSS3 功能。

为了使用 Modernizr，请在 Web 页面的 `<head>` 元素包含以下代码段：

```
<script src="modernizr.min.js" type="text/javascript"></script>
```

导航到 Modernizr 主页，你可以在那里阅读有关该功能检测集的文档、教程和详细信息。

你需要了解的第二个细节是，许多 CSS3 属性目前需要浏览器特定的前缀才能正常工作。该前缀适用于各个浏览器的“进行中”特性，而最终规范将舍弃浏览器特定的前缀。`-ie-`、`-moz-` 和 `-o-` 分别对应 Internet Explorer、Firefox 和 Opera。请注意，Opera 也支持 `-webkit-` 前缀，其他浏览器也可能这样做（请查看各自的网站以获取更新）。

作为示例，下面的代码块展示了这些前缀的示例：

```
-ie-webkit-border-radius: 8px;
-moz-webkit-border-radius: 8px;
-o-webkit-border-radius: 8px;
border-radius: 8px;
```

在你的 CSS 选择器中，在“通用”属性之前指定带有浏览器特定前缀的属性，通用属性在浏览器特定属性未被选中时作为默认选择。书中的 CSS3 代码示例包含 WebKit 特有的前缀，这有助于我们保持 CSS 样式表的大小易于管理。如果你需要能够在多个浏览器（包括当前版本以及旧版本）运行的 CSS 样式表，基本上有两种方案。一种方案是手动添加带有所有所需浏览器特定前缀的 CSS3 代码，这可能非常麻烦且容易出错。另一种方案是使用 CSS 工具包或框架（将在下一章讨论），它们可以通过编程方式生成包含所有浏览器特定前缀的 CSS3 代码。

最后，这里有一份带有浏览器前缀的 CSS 属性详细列表：

*[`peter.sh/experiments/vendor-prefixed-css-property-overview/`](http://peter.sh/experiments/vendor-prefixed-css-property-overview/)

这里有一份无前缀 CSS 属性的详细列表：

*[`www.blooberry.com/indexdot/css/propindex/all.htm`](http://www.blooberry.com/indexdot/css/propindex/all.htm)

## CSS3 功能快速概览

CSS3 采用模块化方法，涉及多个子规范，以扩展现有的 CSS2 功能并支持新功能。因此，CSS3 在逻辑上可以分为以下几类：

*   背景/边框
*   颜色
*   媒体查询
*   多列布局
*   选择器

通过 CSS3，你可以创建带有圏角和阴影效果的框；使用线性渐变和径向渐变创建丰富的图形效果；检测竖屏和横屏；使用媒体查询选择器检测移动设备类型；以及生成多列文本渲染和格式。

此外，CSS3 还允许你使用伪类（在下一节描述）定义复杂的选择规则、`:first-child`、`:last-type` 以及基于属性的模式匹配。

## CSS3 伪类与属性选择

本节简要包含了伪类的示例，随后展示了如何根据属性中的字符串来选择元素。

记住，CSS 中的 `class` 属性提供了一种为一组元素标记的方法，例如下面的代码段：

```
<p class="details">
```

另一方面，伪类允许你通过元素拥有的某些特征引用任意组。例如，下面的代码段选取每个 `<section>` 元素中的段落：

```
section:p:first-of-type
```

CSS3 支持极其丰富的伪类集，包括 `nth-child()` 以及它的一些语义“变体”，如 `nth-of-type()`、`nth-first-of-type()`、`nth-last-of-type()` 和 `nth-last-child()`。

CSS3 还支持布尔选择器（也是伪类），例如 `empty`、`enabled`、`disabled` 和 `checked`，这些表单元素非常有用。另一个伪类是 `not()`，它返回不符合选择标准的元素。

尽管本节关注 `:nth-child()` 伪类，但你将熟悉各种其他的 CSS3 伪类。

### CSS3 伪类

CSS3 `:nth-child()` 伪类既强大又实用，其格式如下：

```
:nth-child(在此处插入关键字或线性表达式)
```

下面的列表提供了使用 `nth-child()` 伪类的各种示例，用以匹配 HTML `<div>` 元素子元素的不同子（该元素也可以被其他 HTML 元素替换）：

*   `div:nth-child(1)`：匹配第一个子元素
*   `div:nth-child(2)`：匹配第二个子元素
*   `div:nth-child(:even)`：匹配偶数子元素
*   `div:nth-child(:odd)`：匹配奇数子元素

`nth-child()` 伪类的有趣且强大之处在于它支持形如 `an+b` 的线性表达式，其中 `a` 是正整数，而 `b` 是非负整数，如下所示（使用一个 HTML5 的 `<div>` 元素）：

*   `div:nth-child(3n)`：匹配从位置 0 开始的每第三个子元素
*   `div:nth-child(3n+1)`：匹配从位置 1 开始的每第三个子元素
*   `div:nth-child(3n+2)`：匹配从位置 2 开始的每第三个子元素

另一个非常有用的伪类涉及 `:hover`，它可以轻松创建美观的视觉效果。以下 CSS3 `:hover` 伪类的示例展示了当用户用鼠标悬停在关联元素上时，改变 `id` 属性值为 `text1` 的元素的字体大小：

```css
#text1:hover {
  font-size: 12pt;
}
```

## CSS3 属性选择

你可以指定 CSS3 选择器来选择 HTML 元素，还可以使用各种正则表达式根据 HTML 元素属性的值来选择 HTML 元素。例如，以下选择器选择 `src` 属性以文本字符串 `Laurie` 开头的 `img` 元素，并将所选 `img` 元素的 `width` 属性和 `height` 属性设置为 `100px`：

```css
img[src^="Laurie"] {
  width: 100px; height: 100px;
}
```

当你想要根据图片的名称（Laurie, Shelly, Steve 等）为图片设置不同的尺寸时，上述 CSS3 选择器非常有用。以下 HTML `<img>` 元素不匹配前述的选择器：

```html
<img src="3Laurie" width="200" height="200" />
<img src="3Laurrie" width="200" height="200" />
```

CSS3 使用元字符 `^`、`$` 和 `*`（后跟 `=` 符号）来匹配文本字符串的起始、终止或任意位置。如果你熟悉 Unix 实用程序 `grep` 和 `sed` 以及 `vi`编辑器，那么这些元字符对你来说非常熟悉。然而，CSS3 对元字符的使用施加了限制：它们只能在属性匹配的上下文中使用（使用方括号）。

以下选择器选择 `src` 属性以文本字符串 `jpeg` 结尾的 HTML `img` 元素，并将所选 `img` 元素的 `width` 属性和 `height` 属性设置为 `150px`：

```css
img[src$="jpeg"] {
  width: 150px; height: 150px;
}
```

当你想要根据图片的类型（jpg, png, jpeg 等）为图片设置不同的尺寸时，上述 CSS3 选择器非常有用。

以下选择器选择 `src` 属性包含文本字符串 `baby` 任意出现的 HTML `img` 元素，并将所选 HTML `img` 元素的 `width` 属性和 `height` 属性设置为 `200px`：

```css
img[src*="baby"] {
  width: 200px; height: 200px;
}
```

当你想要根据图片的“分类”（mybaby, yourbaby, babygirl, babyboy 等）为图片设置不同的尺寸时，上述 CSS3 选择器非常有用。

如果你想了解更多关于可以在 CSS3 选择器中使用的模式（及其描述），可以在此处查看详尽的列表：

*http://www.w3.org/TR/css3-selectors*

本章的第一部分到此结束，下一节将深入探讨 CSS3 面向图形的效果，例如圆角和阴影效果。

## CSS3 阴影效果和圆角

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圆角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

### 使用 RGB 和 HSL 指定颜色

在我们深入研究 CSS3 有趣的功能之前，你需要知道如何表示颜色。一种方法是使用 `(R, G, B)` 三元组，它们代表颜色的红、绿、蓝分量。例如，三元组 `(255, 0, 0)`、`(255, 255, 0)` 和 `(0, 0, 255)` 分别代表红色、黄色和蓝色。指定颜色的其他方法包括：十六进制三元组 `(F, 0, 0)` 和 `(FF, 0, 0)`；十进制三元组 `(100%, 0%, 0)` 或字符串 `#F00`。你也可以使用 `(R, G, B, A)`，其中第四个分量指定透明度，这是一个 0（透明）到 1（不透明）之间的小数。

然而，还有颜色的 HSL（色相、饱和度和亮度）表示法，其中第一个分量是 0 到 360 之间的角度（0 度是北），另外两个分量是 0 到 100 之间的百分比。例如，`(0, 100%, 50%)`、`(120, 100%, 50%)` 和 `(240, 100%, 50%)` 分别代表红色、绿色和蓝色。第一个分量 `(R, G, B, A)` 中的第四个分量指定透明度，这是一个 0（透明）到 1（不透明）之间的小数。

#### CSS3 阴影效果

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圆角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

### 使用 RGB 和 HSL 指定颜色

在我们深入研究 CSS3 有趣的功能之前，你需要知道如何表示颜色。一种方法是使用 `(R, G, B)` 三元组，它们代表颜色的红、绿、蓝分量。例如，三元组 `(255, 0, 0)`、`(255, 255, 0)` 和 `(0, 0, 255)` 分别代表红色、黄色和蓝色。指定颜色的其他方法包括：十六进制三元组 `(F, 0, 0)` 和 `(FF, 0, 0)`；十进制三元组 `(100%, 0%, 0)` 或字符串 `#F00`。你也可以使用 `(R, G, B, A)`，其中第四个分量指定透明度，这是一个 0（透明）到 1（不透明）之间的小数。

然而，还有颜色的 HSL（色相、饱和度和亮度）表示法，其中第一个分量是 0 到 360 之间的角度（0 度是北），另外两个分量是 0 到 100 之间的百分比。例如，`(0, 100%, 50%)`、`(120, 100%, 50%)` 和 `(240, 100%, 50%)` 分别代表红色、绿色和蓝色。第一个分量 `(R, G, B, A)` 中的第四个分量指定透明度，这是一个 0（透明）到 1（不透明）之间的小数。

### CSS3 阴影与文本

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圆角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

#### CSS3 阴影效果

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圏角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

#### CSS3 阴影效果

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圆角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

#### CSS3 阴影效果

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圆角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

#### CSS3 阴影效果

CSS3 阴影效果对于创建生动的视觉效果非常有用。你可以将阴影效果应用于文本以及矩形区域。CSS3 还能让你轻松渲染带有圆角的矩形，因此你不需要 `JPG` 文件即可创建这种效果。

#### CSS3 阴影效果

CSS 阴影效果可以使页面更具吸引力。

#### Listing 2.1 Shadow.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CSS Shadow</title>
</head>
<body>
  <div id="text1">One Shadow</div>
  <div id="text2">Two Shadow</div>
  <div id="text3">Three Shadow</div>
  <div id="text4">Four Shadow</div>
  <div id="text5">Five Shadow</div>
  <div id="text6">Six Shadow</div>
</body>
</html>
```

#### Listing 2.2 Shadow.css
```css
#text1 {
  font-size: 24pt;
  text-shadow: 2px 4px 5px #00f;
}
#text2 {
  font-size: 32pt;
  text-shadow: 0px 1px 6px #000, 4px 5px #f00;
}
...
```

*(注：由于提供的原始文本中存在大量重复的段落和不完整的代码片段，译文已根据“不要重复输出原文”的原则，对逻辑内容进行了整合和去重，并翻译了核心技术说明。)*

```css
text-shadow: 2px 4px 5px #f00;
  -webkit-transform: rotate(-170deg);
}
/* 'transform' 稍后解释 */
#text1:hover, #text2:hover, #text3:hover,
#text4:hover, #text5:hover, #text6:hover {
  -webkit-transform : scale(2) rotate(-45deg);
  transform : scale(2) rotate(-45deg);
}
```

Listing 2.2 中的第一个选择器指定了 24 的 `font-size`，并使用 `text-shadow` 渲染具有蓝色背景的文本（由十六进制值 `#00f` 表示）。`text-shadow` 属性指指定了从左到右的阴影 x 坐标、y 坐标、模糊半径和颜色。第二个选择器指定了 32 的 `font-size` 和红色阴影背景（`#f00`）。第三个选择器通过在 `text-shadow` 属性中指定多个组件创建了更丰富的视觉效果，这些组件是通过对不同组件的不同值进行实验而选择的。

最后的 CSS3 选择器会在用户悬停在六个文本字符串之一上时创建一个动画效果，动画的细节将在本章稍后部分介绍。

图 2.1 显示了 CSS 样式表 `TextShadow1.css` 中的选择器与 HTML 页面 `TextShadow1.html` 中的 HTML `<div>` 元素匹配的结果。该横屏截图取自 Nexus S 4G (Android ICS) 智能手机上的 Android 应用（基于 Listing 2.1 和 Listing 2.2 中的代码）。

![image](img/fig2.1.jpg)

**图 2.1** CSS3 文本阴影效果。

## CSS3 与外阴效果 (#toc.html_toc-h2-0015)

你也可以对包含文本字符串的框应用阴影效果，这在吸引用户注意网页特定部分方面非常有效。然而，关于过度使用的相同警告也适用于外阴。

![image](img/cd.jpg) 此处未显示 HTML 页面 `BoxShadow1.html` 和 `BoxShadow1.css`，但它们可以在 CD 中找到。它们共同渲染出外阴效果。

关键属性是 `box-shadow` 属性，如下所示（此处用**粗体**显示了 Mozilla、WebKit 以及不带前缀的属性）：

```css
#box1 {
  position:relative;top:10px;
  width: 50%;
  height: 30px;
  font-size: 20px;
  -moz-box-shadow: 10px 10px 5px #800;
  -webkit-box-shadow: 10px 10px 5px #800;
  box-shadow: 10px 10px 5px #800;
}
```

图 2.2 显示了带有 Android ICS 的 Nexus S 4G 的横屏截图（基于 `BoxShadow1.html` 和 `BoxShadow1.css` 中的代码）。

![image](img/fig2.2.jpg)

**图 2.2** 带有 Android ICS 的 Sprint Nexus 上的 CSS3 外阴效果。

## CSS3 与圆角 (#toc.html_toc-h2-0016)

Web 开发者长期等待 CSS 中的圆角功能，而 CSS3 能够非常轻松地渲染带有圆角的框。Listing 2.3 显示了 HTML 页面 `RoundedCorners1.html` 的内容，该页面在圆角框中渲染文本字符串，Listing 2.4 显示了 CSS 文件 `RoundedCorners1.css`。

### 列表 2.3 RoundedCorners1.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example</title>
  <link href="RoundedCorners1.css" rel="stylesheet" type="text/css">
</head>
<body>
  <div id="outer">
    <a href="#" class="anchor">矩形内的文本</a>
  </div>
  <div id="text1">带有阴影效果的文本第一行</div>
  <div id="text2">带有阴影效果的文本第二行</div>
</body>
</html>
```

列表 2.3 包含了对 CSS 样式表 `RoundedCorners1.css` 的引用，该样式表包含三个 CSS 选择器，分别匹配 `id` 值为 `anchor`、`text1` 和 `text2` 的元素。在 `RoundedCorners1.css` 中定义的 CSS 选择器创建了视觉效果，正如你将看到的，悬停伪类选择允许你创建动画。

### 列表 2.4 RoundedCorners1.css
```css
a.anchor:hover {
  background: #00F;
}
a.anchor {
  /* 其他样式... */
}
```

```css
{
  font-size: 32px;
  background-image: -webkit-gradient(linear, 100% 0%, 0% 100%, from(#fff), to(#ff0));
  background-image: -gradient(linear, 100% 0%, 0% 100%, from(#fff), to(#ff0));
  -webkit-border-radius: 4px;
  border-radius: 4px;
}
#line3 {
  width: 50%;
  font-size: 32px;
  background-image: -webkit-gradient(linear, 0% 0%, 0% 100%, from(#f00), to(#00f));
  background-image: -gradient(linear, 0% 0%, 0% 100%, from(#f00), to(#00f));
  -webkit-border-radius: 4px;
  border-radius: 4px;
}
#line4 {
  width: 50%;
  font-size: 32px;
  background-image: -webkit-gradient(linear, 100% 0%, 0% 100%, from(#f00), to(#00f));
  background-image: -gradient(linear, 100% 0%, 0% 100%, from(#f00), to(#00f));
  -webkit-border-radius: 4px;
  border-radius: 4px;
}
#outline {
  font-size: 2.0em;
  font-weight: bold;
  color: #fff;
  text-shadow: 1px 1px 1px rgba(0,0,0,0.5);
}
h3 {
  width: 50%;
  position: relative;
  margin-top: 0;
  font-size: 32px;
  font-family: helvetica, ariel;
}
h3 a {
  position: relative;
  color: red;
  text-decoration: none;
  -webkit-mask-image: -webkit-gradient(linear, left top, left bottom, from(rgba(0,0,0,1)), color-stop(50%, rgba(0,0,0,0.5)), to(rgba(0,0,0,0)));
}
h3:after {
  content: "This is a Line of Gradient Text";
  color: blue;
}
```

列表 2.6 中的第一个选择器指定了文本的 `font-size` 为 32，`border-radius` 为 4（渲染出圆角），以及一个从白色到蓝色的线性渐变，如下所示：

```css
#line1 {
  width: 50%;
  font-size: 32px;
  background-image: -webkit-gradient(linear, 0% 0%, 0% 100%, from(#fff), to(#f00));
  background-image: -gradient(linear, 0% 0%, 0% 100%, from(#fff), to(#f00));
  -webkit-border-radius: 4px;
  border-radius: 4px;
}
```

如你所见，第一个选择器包含两个带有 `-webkit-` 前缀的属性和两个没有该前缀的标准属性。由于 列表 2.6 中的后续选择器与第一个选择器相似，我们在此不再讨论它们的内容。下一个选择器通过将文本渲染为白色并带有细阴影，创建一个带有漂亮阴影的文本轮廓，如下所示：

```css
color: #fff;
text-shadow: 1px 1px 1px rgba(0,0,0,0.5);
```

列表 2.6 的最后部分包含了影响 `h3` 元素及其嵌入的 `a` 元素渲染的三个选择器。`h3` 选择器指定宽度和字体大小；`a` 选择器指定线性渐变；`h3:after` 选择器指定在 HTML5 `h3` 元素之后显示的文本字符串“This is a Line of Gradient Text”。（*注意*：你可以使用 `h3:before` 来在 HTML5 `h3` 元素之前指定文本字符串。）还指定了其他属性，但这些是选择器主要的属性。

图 2.4 显示了 CSS 样式 `LinearGradient1.css` 中的选择器与 HTML 页面 `LinearGradient1.html` 匹配的结果，截图来自运行带有 Android ICS 的 Asus Prime 平板的横屏模式。

### 径向渐变

CSS3 径向渐变比 CSS3 线性渐变更复杂，但你可以用它们创建更复杂的渐变效果。基于 `Webkit` 的浏览器支持以下语法来定义径向渐变：

*   一个起点
*   起始半径
*   一个终点
*   结束半径
*   使用 `from()` 指定起始颜色
*   零或多个颜色停止
*   使用 `to()` 指定结束颜色

![image](img/fig2.4.jpg)
**图 2.4** 带有 Android ICS 的 Asus Prime 10 平上的 CSS3 线性渐变效果。

注意，径向渐变的语法与线性渐变的语法相似，但你还指定了起始半径和结束半径。

![image](img/cd.jpg) HTML5 网页 `RadialGradient1.html` 和 CSS 样式表 `RadialGradient1.css` 未在此处显示，但完整的列表可以在 CD 上找到。HTML5 代码中的核心涉及此代码块：

```html
<div id="outer">
  <div id="radial3">Text3</div>
  <div id="radial2">Text2</div>
  <div id="radial4">Text4</div>
  <div id="radial1">Text1</div>
</div>
```

CSS 样式表 `RadialGradient1.css` 包含了五个 CSS 选择器，用以匹配五个 HTML `div` 元素，其中一个选择器在此处所示：

```css
#radial1 {
  background: -webkit-gradient(
    radial, 500 40%, 0, 301 25%, 360, from(red),
    color-stop(0.05, orange), color-stop(0.4, yellow),
    color-stop(0.6, green), color-stop(0.8, blue),
    to(#fff)
  );
}
```

`#radial1` 选择器包含一个使用 `-webkit-` 前缀定义径向渐变的 `background` 属性，它指定了：
*   起点 (500, 40%)
*   起始半径 0
*   终点 (301, 25%)
*   结束半径 360
*   起始颜色红色
*   结束颜色白色 (#fff)

其他选择器的语法与第一个选择器相同，但生成的径向渐变显著不同。通过指定不同的起点和终点，以及指定大于结束半径的起始半径，你可以创建这些（其他的）效果。

图 2.5 显示了 CSS 样式表 `RadialGradient1.css` 中的选择器与 HTML 页面 `RadialGradient1.html` 匹配的结果，截图来自 Android 平板的横屏模式。

![image](img/fig2.5.jpg)

```css
img.scaled {
  -webkit-box-shadow: 10px 10px 5px #800;
  box-shadow: 10px 10px 5px #800;
}
img.scaled:hover {
  -webkit-transform : scale(2);
  transform : scale(2);
}
```

Listing 2.8 中的 `img` 选择器指定了一个过渡属性，该属性使用 `ease` 函数在一秒的间隔内应用变换效果，如下所示：

```css
transition: transform 1.0s ease;
```

接下来，选择器 `img.scaled` 指定了 `box-shadow` 属性，它创建了一个红色的阴影效果（你之前在本章中已经见过它），如下所示：

```css
img.scaled {
  -webkit-box-shadow: 10px 10px 5px #800;
  box-shadow: 10px 10px 5px #800;
}
```

最后，选择器 `img.scaled:hover` 指定了一个变换属性，该属性使用 `scale()` 函数，当用户用鼠标悬停在任何 `<img>` 元素上时，会将关联 JPG 文件的大小放大一倍，如下所示：

```css
transform : scale(2);
```

由于 `img` 选择器指定了使用 `ease` 函数的一秒间隔，因此缩放效果将持续一秒。可以尝试不同的 CSS3 `scale()` 函数取值，以及时间间隔的不同值，以创建适合你需求的动画效果。

另一个需要记住的点是，你可以同时进行水平和垂直缩放：

```css
img {
  -webkit-transition: -webkit-transform 1.0s ease;
  transition: transform 1.0s ease;
}
img.mystyle:hover {
  -webkit-transform : scaleX(1.5) scaleY(0.5);
  transform : scaleX(1.5) scaleY(0.5);
}
```

图 2.6 显示了 CSS 样式表 `Scale1.css` 中的选择器与 HTML 页面 `Scale1.html` 匹配的结果。该横屏截图取自运行在带有 Android ICS 的 Nexus S 4G 智能手机上的 Android 应用（基于 Listing 2.7 和 Listing 2.8 中的代码）。

## 旋转变换](#toc.html_toc-h2-0019)

CSS3 transform 属性允许你指定 `rotate()` 函数来创建缩放效果，其语法格式如下：

```css
rotate(someValue);
```

你可以将 `someValue` 替换为任何数字。当 `someValue` 为正数时，旋转为顺时针方向；当 `someValue` 为负数时，旋转为逆时针方向；当 `someValue` 为零时，则没有旋转效果。在所有情况下，旋转效果的初始位置都是正水平轴。

![image](img/fig2.6.jpg)

***图 2.6*** 基于 CSS3 的 JPG 文件缩放效果。

![image](img/cd.jpg) CD 上的 HTML5 页面 `Rotate1.html` 和 CSS 样式表 `Rotate1.css` Illust 明了如何创建旋转效果，其一个示例所示：

```css
img.imageL:hover {
  -webkit-transform : scale(2) rotate(-45deg);
  transform : scale(2) rotate(-45deg);
}
```

`img` 选择器指定了一个过渡属性，该属性使用 `ease` 定时函数在一秒的间隔内创建一个动画效果，如下所示：

```css
transition: transform 1.0s ease;
```

CSS3 transform 属性允许你指定 `skew()` 函数来创建倾斜效果，其语法格式如下：

```css
skew(xAngle, yAngle);
```

你可以将 `xAngle` 和 `yAngle` 替换为任何数字。当 `xAngle` 和 `yAngle` 为正数时，倾斜效果为顺时针方向；当 `xAngle` 和 `yAngle` 为负数时，倾斜效果为逆时针方向；当 `xAngle` 和 `yAngle` 为零时，则没有倾斜效果。在所有情况下，倾斜效果的初始位置都是正水平轴。

![image](img/cd.jpg) HTML5 页面 `Skew1.html` 和 CSS 样式表 `Skew1.css` 位于 CD 上，它们说明了如何创建倾斜效果。该 CSS 样式表包含 `img` 选择器，该选择器指定了一个过渡属性，进而使用 `ease` 定时函数在一秒的间隔内创建一个动画效果，如下所示：

```css
transition: transform 1.0s ease;
```

还有四个选择器 `img.skewed1`、`img.skewed2`、`img.skewed3` 和 `img.skewed4` 分别创建深浅不一的红、黄、绿、蓝背景投影效果（这些在之前的代码示例中都见过）。

选择器 `img.skewed1:hover` 指定了一个变换属性，当用户用鼠标悬停在第一个 `<img>` 元素上时，会执行倾斜效果，如下所示：

```css
transform : scale(2) skew(-10deg, -30deg);
```

另外三个 CSS3 选择器也使用了 CSS 函数 `skew()` 和 `scale()` 的组合来创建不同的视觉效果。注意，第四个悬停选择器还将透明度（opacity）属性设置为 0.5，这与该选择器中的其他效果并行发生。

图 2.7 显示了 CSS 样式表 Skew1.css 中的选择器与 HTML 页面 Skew1.html 匹配的结果。该横屏截图取自运行在 Nexus S 4G 智能手机上的 Android 应用。

![image](img/fig2.7)

***图 2.7*** 基于 CSS3 的缩放效果。

CSS3 transform 属性允许你指定 `translate()` 函数来创建元素的水平和垂直位移，其语法格式如下：

```css
translate(xDirection, yDirection);
```

位移是相对于原点的，即屏幕的左上角。因此，`xDirection` 和 `yDirection` 的正值会产生向右和向下的偏移，而 `xDirection` 和 `yDirection` 的负值则产生向左和向上的偏移。

![image](img/cd.jpg) CD 上的 HTML5 页面 `Translate1.html` 和 CSS 样式表 `Translate1.css` 说明了如何对 JPG 文件应用位移效果。

```css
img.trans2:hover {
  -webkit-transform : scale(0.5) translate(-50px, -50px);
  transform : scale(0.5) translate(-50px, -50px);
}
```

该 CSS 样式表包含 `img` 选择器，该选择器指定了一个使用 `ease` 定时函数在一秒间隔内的过渡效果，如下所示：

```css
transition: transform 1.0s ease;
```



四个选择器 `img.trans1`、`img.trans2`、`img.trans3` 和 `img.trans4` 分别创建红、黄、绿、蓝深色的背景投影效果，正如你在前一节中看到的那样。

选择器 `img.trans1:hover` 指定了一个变换属性，当用户用鼠标悬停在第一个 `<img>` 元素上时，会执行缩放效果和位移效果，如下所示。

图 2.8 显示了 CSS 样式表 Translate1.css 中的选择器与 HTML 页面 Translate1.html 匹配的结果。该横屏截图取自带有 Android ICS 的 Nexus S 4G 智能手机上的 Android 应用。

![image](img/fig2.8.jpg)

***图 2.8*** 基于 CSS3 的 JPG 文件缩放和位移效果。

## CSS3 媒体查询

CSS3 媒体查询是非常用的逻辑表达式，允许检测具有不同物理属性和方向的移动应用程序。例如，通过 CSS3 媒体查询，你可以更改应用程序的尺寸和布局，使其在智能手机和平板上都能正确显示。

你可以使用 CSS3 媒体查询确定设备的以下特征：

*   浏览器窗口宽度和高度
*   设备宽度和高度
*   方向（横屏或竖屏）
*   比例
*   设备比例
*   分辨率

CSS3 媒体查询是布尔表达式，包含一个或多个“简单项”（使用 and 或 or 连接），这些项评估结果为真或假。

例如，以下 `link` 元素仅当设备为屏幕且设备最大宽度为 `480px` 时才会加载 CSS 样式表 `mystuff.css`：

```html
<link rel="stylesheet" type="text/css" media="screen and (max-device-width: 480px)" href="mystuff.css"/>
```

上述 `link` 包含一个 `media` 属性，它指定了两个部分：媒体类型为 `screen`，以及一个指定 `max-device-width` 值为 `480px` 的查询。CSS3 媒体查询中 `media` 的支持值包括 `braille, embossed, handheld, print, projection, screen, speech, tty` 和 `tv`。

下一个 CSS3 媒体查询检查了媒体类型、设备最大宽度以及设备的分辨率：

```css
@media screen and (max-device-width: 480px) and (resolution: 160dpi) {
  #innerDiv {
    float: none;
  }
}
```

如果上述代码段中的 CSS3 媒体查询求值为为真，则嵌套的 CSS 选择器将匹配 `id` 属性值为 `innerDiv` 的 HTML 元素，并且任何最大屏幕宽度为 `480px` 的设备上，其 `float` 属性将被设置为 `none`。如你所示，可以创建包含非平凡逻辑的紧凑 CSS3 媒体查询，这显然非常有用，因为 CSS3 没有像其他编程语言那样的 `if/then/else` 结构。

![image](img/cd.jpg) CD 额外代码示例

CSS 样式表 `CSS3MediaQuery1.css` 和 HTML5 网页 `CSS3MediaQuery1.html` 阐明了如何使用媒体查询在用户旋转移动设备时更改两幅图像的大小。

![image](img/cd.jpg) 你可以使用简单的 JavaScript 代码检测移动设备方向的变化，因此你并不“被迫”使用 CSS3 媒体查询。CD 上的 HTML5 网页 `CSS3OrientationJS1.html` 阐明了如何使用标准 JavaScript 在用户旋转移动设备时更改两幅图像的大小。

本质上，该代码使用变量 `window.orientation` 的值来检测移动设备的四种不同方向。在每种情况下，都会使用以下类型的代码更新 JPG 文件的尺寸：

```javascript
document.getElementById("img1").style.width = "120px";
document.getElementById("img1").style.height = "300px";
```

尽管这是一个非常简单的例子，但希望这段代码能让你体会 CSS3 媒体查询的能力。

## 总结

本章向你展示了如何创建图形效果、阴影效果以及如何在 CSS3 中使用变换（transforms）。你学习了如何创建可以应用于 HTML 元素的动画效果，并看到了如何定义 CSS3 选择器来执行以下操作：

*   渲染圆矩
*   为文本和 2D 形状创建阴影效果
*   创建线性和径向渐变
*   使用 `translate()`、`rotate()`、`skew()` 和 `scale()` 方法
*   创建基于 CSS3 的动画效果

## 第 3 章

### 使用 JQUERY 和 CSS3 实现动画效果

本章向你展示了如何创建动画效果并为用户提供交互的 HTML5 网页。你将看到一组创建各种动画效果的 `jQuery` 函数，你可以轻松地将它们整合到你的 HTML5 网页中。这个内容广泛的章节旨在为你提供许多动画效果，以及一系列代码示例和代码片段，你可以将它们整合到你的其他 HTML5 网页中。

本章的第一部分向你展示了如何使用 `jQuery` 通过设置 CSS3 选择器的属性值来操作元素的属性，并提供了使用 `animate` 和 `effect` 创建动画效果的示例。你将看到创建基于滑动的和淡入淡出的（`fadeIn`, `fadeOut`, `fadeTo`）动画效果的代码示例。本节还阐明了如何结合 `jQuery` 和 CSS3 `keyframes` 创建 2D 动画效果。

本章的第二部分阐明了如何创建一个“跟随鼠标”的 HTML5 网页，该网页使用 CSS3 用于视觉效果，并使用 `jQuery` 更新渐变填充矩形的位置。记住，书中章节中的 CSS3 示例专门针对基于 WebKit 的浏览器，但你可以修改代码示例以包含特定厂商的前缀，以便代码示例可以在其他浏览器中运行。本章的最后一个示例说明了如何使用 `jQuery` 插件通过 `jQuery` 渲染 `SVG`。

注意，本章涵盖了 `jQuery` 动画效果，第七章包含了某些使用 `jQuery Mobile` 的对应动画效果，这两个章节都包含了基于 CSS3 的动画效果。由于空间限制，本章仅涵盖了 `jQuery` 可用的部分功能。你可以通过在线 `jQuery` 文档或搜索额外的教程和文章来了解更多 `jQuery` 动画。

## 在 jQuery 中处理 CSS3 选择器

本节包含代码示例，阐明了如何使用 `jQuery` 通过操作 CSS 类程序化地创建视觉效果，例如圆角、渐变和阴影效果。

### jQuery 中的基础动画效果

本节包含代码片段而非完整的列表，这些代码片段阐明了如何使用 `hide()` 和 `show()` 创建动画，以及如何设置动画速度。请记住本节仅涵盖了可用功能集的一部分。务必阅读在线文档以了解其他功能。

`hide()` 和 `show()` 函数允许你更改 HTML 页面中元素的可见性。例如，以下代码在用户点击第一个按钮时隐藏第二个按钮；当用户双击第一个按钮时，第二个按钮变为可见：

```javascript
$("#myButton1").click(function() {
  $("#myButton2").hide();
});
$("#myButton1").dblclick(function() {
  $("#myButton2").show();
});
```

`toggle` 函数可以处理同一个事件的两次或多次发生。例如，以下代码处理一个元素上的一次、两次或三次点击事件：

```javascript
$("#myDiv1").toggle(
  function() {
    $("myText").text("First click");
  },
  function() {
    $("#myText").text("Second click");
  },
  function() {
    $("#myText").text("Third click");
  }
);
```

另外两个实用的 `jQuery` 方法是 `removeClass()` 和 `addClass()`，它们分别移除或添加 CSS 类，示例在此：

```javascript
$("#myDiv1").toggle(
  function() {
    $("myText").addClass("shiny");
  },
  function() {
    $("#myText").addClass("dark");
  }
);
```

`addClass()` 方法添加 CSS 类，而 `toggleClass()` 方法则“切换” CSS 类；即：如果类不存在则添加它，如果已经包含则移除它。其他相关的 `jQuery` 方法包括使用淡入淡出效果的 `fadeClass()` 和创建滑动效果的 `slideClass()`。

## 使用回调函数

许多 `jQuery` 函数（包括 `hide()`、`show()`、`toggle()` 和滑动相关的函数）允许你指定一个回调函数，该函数将在指定的操作完成后执行。例如，你可以定义以下代码块：

```javascript
$("#myButton1").click(function() {
  $("#myButton2").hide('slow',
);
function callback() {
  // do something else
});
});
```

当用户点击 id 为 `myButton1` 的元素时，上一个代码块会缓慢隐藏 id 为 `myButton2` 的元素，在动画完成后，将执行 `callback` 函数中的代码。

本书包含了基于 WebKit 的代码示例，但如果你决定在 IE 中使用上一个代码块，请记住在 IE 中在回调函数中使用命名函数（named functions）时存在一个 bug。下文提供了有关命名函数的有用信息：

[`kangax.github.com/nfe`](http://kangax.github.com/nfe)

# jQuery 渐入和滑动动画效果

jQuery 与淡入（fade）和滑动（slide）相关的效果很容易创建，如果你定义得当，它们可以在你的 Web 页面中创建非常佳的视觉效果。

以下示例结合了 jQuery 的 `.fadeIn()` 和 `.fadeOut()` 函数，还向你展示了如何链式调用这些函数以便创建多个动画效果。

## fadeIn(), fadeOut(), 和 fadeToggle() 函数

这三个 jQuery 函数 `.fadeIn()`、`.fadeOut()` 和 `.fadeToggle()` 方法可以指定三个参数，其语法所示：

`jQuery(list-of-elements).fadeIn(speed);`
`jQuery(list-of-elements).fadeOut(speed);`
`jquery(list-of-elements).fadeTo(speed);`

下方的代码块说明了如何使用这三个 jQuery 函数：

```javascript
$("#something").click(function() {
  $(this).fadeIn('slow');
});
$("#something").click(function() {
  $(this).fadeOut('slow');
});
$("#something").click(function() {
  $(this).fadeTo('slow', .65);
});
```

`Listing 3.1` 显示了 `FadeInOut.html` 的内容，并插插了如何在 jQuery 中执行简单和链式的淡入效果。

### 列表 3.1 FadeInOut.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery 渐入相关效果</title>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
</head>
<body>
  <div>
    <div> <p>Hello World from jQuery (悬停在我身上)</p> </div>
    <div> <p>Goodbye World from jQuery (悬停在我身上)</p> </div>
    <div>
      <input type="button" id="button1" value="Hide Me" />
    </div>
  </div>
  <script>
    $(document).ready(function(){
      var para = $("div > p");
      para.each(function(){
        var p = $(this);
        p.append('<span style="color:red;font-size:18px"'+'>'>这段文字在悬停时会淡出</span>');
      });
      para.hover(function() {
        // 你可以使用 'slow' 或 'fast'
        //$(this).find("span").fadeIn("slow");
        $(this).find("span").fadeIn(3000).fadeOut("fast").fadeIn("slow");
      }, function() {
        //$(this).find("span").hide();
        $(this).find("span").fadeOut(2000).fadeIn("slow").fadeOut("fast").fadeIn(2000).fadeOut("slow");
      });
      $("#button1").click(function() {
        $(this).fadeOut(50, function() {
          //$(this).remove();
        });
      });
    });
  </script>
</body>
</html>
```

`Listing 3.1` 以两个 HTML `<div>` 元素和一个 HTML `<button>` 元素开始，随后是用于对 HTML `<p>` 元素应用渐入相关效果的 jQuery 代码。第一个需要注意的是 JavaScript 变量 `para`，它存储了指向 `<div>` 元素子元素的 HTML `<p>` 元素的引用，如下所示：

```javascript
$(document).ready(function(){
  var para = $("div > p");
  // 省省略代码
}
```

下一个代码块为 `para` 变量中引用的 HTML `<p>` 元素动态添加一个 HTML `<span>` 元素：

```javascript
para.each(function(){
  var p = $(this);
  p.append('<span style="color:red;font-size:18px"'>这段文字在悬停时会淡出</span>');
});
```

当用户悬停在任何 HTML `<p>` 元素上时，jQuery 代码使用 jQuery 方法链式调用为 HTML `<p>` 元素创建多个渐入相关效果。示例所示：

```javascript
$(this).find("span").fadeOut(2000).fadeIn("slow").fadeOut("fast").fadeIn(2000).fadeOut("slow");
```

你可以使用 jQuery 方法对当前获取焦点元素以外的元素应用效果。例如，如果你想在悬停事件期间隐藏一个兄弟元素，你可以这样做：

`$(this).next().fade();`

下一节将向你展示如何使用 jQuery 滑动相关函数来创建滑动动画效果。

# jQuery 滑动相关函数

jQuery 的 `slideUp()`、`slideDown()` 和 `slideToggle()` 方法可以指定三个参数，它们的语法如下：

`jQuery(elements).slideUp([speed], [easing], [callback]);`
`jQuery(elements).slideDown([speed], [easing], [callback]);`
`jQuery(elements).slideToggle([speed], [easing], [callback]);`

`milliseconds` 值指定动画效果的持续时间，`callback` 是在动画完成后执行的可选 JavaScript 函数。

`Listing 3.2` 显示了 `SlideUpDown.html` 的内容，并说明如何在 jQuery 中执行简单和链式的滑动效果。

### 列表 3.2 QSlideUpDown.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery 滑动相关效果</title>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
</head>
<body>
  <div>
    <div> <p>Hello World from jQuery (悬停在我身上)</p> </div>
    <div> <p>Goodbye World from jQuery (悬停在我身上)</p> </div>
    <div>
      <input type="button" id="button1" value="Click to Slide Up and Hide Me" />
    </div>
  </div>
  <script>
    $(document).ready(function(){
      var para = $("div > p");
      para.each(function(){
        var p = $(this);
        p.append('<span style="color:red;font-size:18px"'>这段文字在悬停时会滑动</span>');
      });
      para.hover(function() {
        // 你可以使用 'slow' 或 'fast'
        //$(this).find("span").slideDown("slow");
        $(this).find("span").slideDown(3000).slideUp("fast").slideDown("slow");
      }, function() {
        //$(this).find("span").hide();
        $(this).find("span").slideUp(2000).slideDown("slow").slideUp("fast").slideDown(2000).slideUp("slow");
      });
      $("#button1").click(function() {
        $(this).slideUp(2000, function() {
          //$(this).remove();
        });
      });
    });
  </script>
</body>
</html>
```

`Listing 3.2` 与 `Listing 3.1` 类似，不同的是使用了滑动相关的 jQuery 方法代替渐入相关的 jQuery 方法，且该代码示例的描述类似于 `Listing 3.1` 的描述。

需要记住的一点是，对于具有 CSS 内边距（padding）、外边距（margin）属性或未设置固定宽度的元素，滑动效果并不总是按预期工作（可能会出现某些抖动）。请尝试这些场景，看看结果行为是否符合你的预期，或者对你的 Web 页面来说是可以接受的。

## jQuery 中的缓动函数

jQuery 支持一组被称为“缓动”（easing）函数，这些函数提供了不同类型的动画效果。通俗来说，缓动函数使用某种方程作为动画效果的路径。例如，你可以使用线性方程来创建恒速运动的动画。你也可以使用二次方程（二阶多项式，其通用形式为 `a*x*x+b*x+c`）来创建具有加速度的动画效果，或用于二次贝塞尔曲线，并使用三次方程用于三次贝塞尔曲线。

jQuery 还为动画提供了缓动函数，其动画速度在缓动函数的不同位置更加复杂（慢、快、慢）。在 particular 开始搜索 jQuery 插件之前，探索现有的 jQuery 缓动函数是非常值得的，其中一些：`linear`、`easeInQuad`、`easeOutQuad`、`easeInCubic`、`easeOutCubic`、`easeInOutCubic`、`easeInSine`、`easeOutSine`、`easeInOutSine`、`easeInElastic`、`easeOutElastic` 和 `easeInOutElastic`。

你可以找到许多提供 jQuery 缓动函数大量演示的链接，包括这里显示的：

- [`jqueryui.com/demos/effect/easing.html`](http://jqueryui.com/demos/effect/easing.html)

此外，还有许多 jQuery 插件可用于自定义动画相关的缓动函数，或者如果你找不到符合你需求的插件，也可以创建自己的 jQuery 插件。

## 的 jQuery .animate() 方法

jQuery `animate()` 方法可以接受四个参数，它们看起来如下：

```javascript
jQuery(elements).animate([properties],
                      [milliseconds],
                      [easing-function],
                      [complete-function]);
```

`properties` 参数包含要动画的属性列表，`milliseconds` 参数指定动画效果的持续时间。`easing-function` 参数指定上一节讨论的缓动函数之一，而 `complete-function` 参数指定在动画效果完成后执行的 JavaScript 回调函数。

![image](img/cd.jpg) CD 上的 HTML5 页面 `JQAnimate1.html` 阐释了如何使用 jQuery `animate()` 函数在两个 PNG 文件上创建动画效果。

此 HTML5 页面包含两个 PNG ，以及针对两个 HTML `<button>` 元素的 jQuery 点击处理程序。每当用户点击左侧按钮时，jQuery 代码会在五秒间隔内将 PNG 的透明度从 1.0 降低到 0.25，将图像向右移动 50 个单位，并增加高度 100 个单位，所示：

```javascript
$('#text1').animate({
    opacity: 0.25,
    left: '+=50',
    height: '+=100'
}, 5000, function() {
    // 动画完成（执行其他操作）
});
```

每当用户点击第二个按钮时，jQuery 代码会对右侧图像文件执行类似的动画效果。运行 `Listing 3.2` 中的代码并点击按钮以查看动画效果。

你可以在 HTML5 页面 `JQAnimate2.html` 中看到 `Listing 3.2` 中动画效果的变体，以及 `JQAnimate2.html` 页面中的顺序动画和并行动画效果，这两者在 CD 上均可用。

![image](img/cd.jpg) 你可以通过更改 HTML 元素的不同 CSS 属性，使用 jQuery `animate()` 函数创建其他有趣的视觉效果。例如，以下代码块为作为 HTML `<ul>` 元素部分的列表项创建一个“摇晃”效果：

```javascript
$('#mylist li').hover(function() {
  $(this).animate({paddingLeft: '+=15px'}, 200);
}, function() {
  $(this).animate({paddingLeft: '-=15px'}, 200);
});
```

你还可以创建线性和摇摆动画效果，所示：

```javascript
$('p:first').toggle(function() {
  $(this).animate({'height':'+=150px'}, 1000, 'linear');
}, function() {
  $(this).animate({'height':'-=150px'}, 1000, 'swing');
});
```

## 使用 .animate() 函数自定义 CSS 动画

你可以使用 jQuery 动画许多 CSS 属性，包括 `border-width`、`bottom`、`font-size`、`height`、`margin`、`opacity`、`padding`、`right`、`top`、`width` 和 `word-spacing`。此外，你可以使用 `slow`、`fast` 或代表毫秒的整数值指定持续时间。

以下代码动画化 HTML `<div>` 元素的 `width` 和 `height` 属性，使其最终值将将为 500 和 300：

```javascript
$("#myDiv").click(function() {
  $(this).animate({width:'500px', height: '300px'});
});
```

在前面的 jQuery 代码中，如果初始值小于 `500px`，则宽度将增加到 `500px`；否则宽度将减到 `500px`（高度也是如此）。

### 基于 CSS3 的动画效果

本节说明了你可以用 CSS3 创建的各种动画效果，代码示例使用了 CSS3 `@keyframes` 规则和 2D 变换。

### 使用 CSS 关键帧和 2D 变换的动画

Listing 3.3 显示了 `QButtonAnimation1.html` 的内容，并说明了如何创建由 `hover` 伪类触发的按钮相关动画。

列表 3.3 包含一个 HTML `<style>` 元素，其中包含一个 CSS3 keyframes 定义（你也可以将其移动到单独 CSS 样式表中），随后是两个类型为按钮的 HTML `<input>` 元素，这两个元素都在 列表 3.3 中的 `<script>` 元素中定义了点击事件处理程序。

当用户点击任何一个按钮时，CSS3 keyframes 定义就会应用到该按钮上。这反过来通过 `translate()`、`rotate()` 和 `skew()` 函数的组合，为相关选择器指定的时段（无论是 2 秒还是 4 秒）创建动画效果。此外，点击处理程序还创建了一个持续 500 毫秒的淡出效果。

当你在浏览器中启动 HTML Web 页面 `JQButtonAnimation1.html` 时，每当你悬停在任一个按钮上，都会看到动画效果。

## 使用 CSS3 和 jQuery 进行 2D 变换

本节中的代码示例向你展示了如何使用 jQuery 的 `css()` 函数基于用户触发的事件，直接对元素应用 CSS 变换。

列表 3.4 显示了 `JQTransforms2D1.css` 的内容，该文件包含应用于 HTML5 Web 页面 `JQTransforms2D1.html` 的 CSS3 选择器，该页面见于 列表 3.4。

### 列表 3.4 JQTransforms2D1.css

```css
#outer {
  position: absolute;
  left: 50px;
  top: 150px;
}
#inner1 {
  float: left;
  background-color:#F00;
  width: 200px;
  height:150px;
}
#inner2 {
  float: left;
  background-color:#FF0;
  width: 200px;
  height:150px;
}
#inner3 {
  float: left;
  background-color:#00F;
  width: 200px;
  height:150px;
}
```

列表 3.4 非常直观：为 列表 3.5 中定义的三个 HTML `<div>` 元素指定了宽度和高度等属性。

### 列表 3.5 JQTransforms2D1.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery 变换效果</title>
  <link href="Transforms1.css" rel="stylesheet" type="text/css">
  <script src="http://code.jquery.com/jquery-2.0.0b1.js">
  </script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js">
  </script>
</head>
<body>
  <h1>点击任何一个矩形内部：</h1>
  <div id="outer">
    <div id="inner1"></div>
    <div id="inner2"></div>
    <div id="inner3"></</div>>
  </div>
  <script>
    $(document).ready(function() {
      $("#inner1").click(function() {
        $("div").css({height: '300px',
          'webkit-transform': 'scale(0.5, 0.5) skew(-10deg, 20deg)'
        });
      });
      $("#inner2").click(function() {
        $("div").css({height: '200px',
          width: '250px',
          'webkit-transform': 'scale(0.5, 0.8) rotate(-45deg)'
        });
      });
      $("#inner3").click(function() {
        $("div").css({height: '100px',
          width: '250px',
          'webkit-transform': 'skew(-10deg, 10deg) rotate(-45deg)'
        });
      });
    });
  </script>
</body>
</html>
```

列表 3.5 为三个 HTML `<div>` 元素定义了点击事件的处理程序，所有处理程序都调用了 `css()` 函数来更新接收点击的 `<div>` 元素的属性。例如，第一个 HTML `<div>` 元素的更新如下：

`$("div").css({height: '300px', 'webkit-transform': 'scale(0.5, 0.5) skew(-10deg, 20deg)'});`

如你所见，高度属属性设置为 300px，并且当用户点击 `<div>` 元素时，应用了变换。请记住，你可以将 列表 3.5 中点击处理程序所引用的 CSS 代码移动到单独的样式表中。这使得在单个文件中维护 CSS 代码变得更加容易，你还可以在多个 HTML 页面中引用同一个样式表。

除了 CSS3 2D 动画效果外，你显然还可以创建 3D 动画效果。通过尝试 列表 3.5 中的代码，并添加来自以下来源的 3D 效果：`http://code.google.com/p/`，你可以对 第 2 章 进行实验。图 3.1 在浏览器中显示 `JQTransforms2D1.html`。列表 3.4 和 列表 3.5 涉及到鼠标相关功能以及如何通过编程方式处理事件。列表 3.6 在下一节展示了如何使用 jQuery 和 CSS3 在 HTML5 页面中根据鼠标当前位置渲染 `<div>` 元素。

## jQuery 跟随鼠标示例

本节中的代码示例通过展示如何通过编程方式创建 `<div>` 元素并将其添加到 DOM 中，扩展了前节介绍的功能。列表 3.6 显示了 `JQFollowMouse.html` 在 MacBook 上的内容。

### 列表 3.6 JQFollowMouse.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>跟随鼠</title>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
</head>
<body>
  <div></div>
  <script>
    // 关于前一个 <div> 的注释
    $(document).ready(function() {
      var rectWidth = 20;
      var rectHeight = 20;
      var moveCount = 0;
      var insertNode = true;
      var currColor = "";
      var rectColors = Array('#ff00', '#ffff0', '#00ff', '#00ff');
      var newNode;
      $(document).mousemove(function(e) {
        ++moveCount;
        // 用户正在移动鼠标吗？
        if (insertNode == true) {
          // 在当前位置创建一个矩形
          newNode = $('<div id=newNode>').css({
            'position':'absolute',
            'background-color':'#ff0000',
            'width':rectWidth+'px',
            'height':rectHeight+'px',
            top: e.pageY,
            left: e.pageX
          });
          // 使用此代码将矩形添加到正文
          $("div").append(newNode);
          // 使用此代码不将矩形添加到正文
          //$(document.body).append(newNode);
          insertNode = false;
        } else {
          currColor = rectColors[moveCount % rectColors.length];
          $('div').each(function() {
            $(this).css({
              top: e.pageY,
              left: e.pageX,
              'background-color': currColor
            });
          });
        }
      });
    });
  </script>
</body>
</html>
```

Listing 3.6 初始化了一些 JavaScript 变量，然后使用 jQuery 的 `css()` 方法动态创建一个 HTML `<div>` 元素，该元素的左上角坐标与 `mousemove` 事件发生点的坐标相同，从而创建了一个跟随鼠标的效果。需要注意的关�点是，事件对象（在此代码示例中称为 `e`）允许我们访问当前移动位置的坐标。我们可以使用属性 `e.pageX` 和 `e.pageY` 分别设置 CSS 属性 `left` 和 `top`。

同样请注意在 Listing 3.6 中，HTML `<body>` 元素之后紧跟着一个空的 HTML `<div>` 元素。需要这个元素是因为众，在脚本之后添加的 UI 元素在某些旧版浏览器中会消失。解决方案是包含这个空 `<div>` 元素，然后向该元素添加内容。

## 使用 jQuery 处理其他事件

你已经见过了说明如何使用 jQuery 处理各种事件的代码示例。jQuery 为鼠标相关事件提供了广泛支持，并像接下来的两节描述的那样，支持键盘事件。

### 处理鼠标事件

jQuery 支持以下你可能熟悉的常用鼠标事件：`mousedown`、`mouseenter`、`mouseleave`、`mousemove`、`mouseout`、`mouseover` 和 `mouseup`。你可以使用以下 jQuery 代码结构在 jQuery 中检测这些鼠标事件：

```javascript
$("#myInput").mousedown(function() {
  // do something
});
$("#myInput").mouseenter(function() {
  // do something
});
$("#myInput").mouseleave(function() {
  // do something
});
$("#myInput").mousemove(function() {
  // do something
});
$("#myInput").mouseout(function() {
  // do something
});
$("#myInput").mouseover(function() {
  // do something
});
$("#myInput").mouseup(function() {
  // do something
});
```

你可以将所需的任何代码片段包含在 HTML 页面中，然后添加处理逻辑以提供预期的功能。

### 处理键盘事件

你也可以在 jQuery 中检测 `keypress`、`keyup` 和 `keydown` 事件。例如，这段代码在用户点击大写“Z”键时显示一个警报：

```javascript
$("#myInput").keypress(function(e) {
  if (e.which == 90) alert ('Z was typed.');
});
```

你可以检查其他按键事件，记住大写 `A` 的十进制是 65（十六进制 41），小写 `a` 是十进制 97（十六进制 61），小写 `z` 是十进制 122（十六进制 7A）。

你还可以添加许多其他效果，包括本章之前代码示例中提供的动画效果。

![image](img/cd.jpg) ## CD 额外代码示例

HTML5 页面 `JQSlideShow1.html` 阐述了如何使用 jQuery 创建包含 JPG 图像的幻灯片，它使用以下代码块来确定下一个 HTML `<img>` 元素（当到达最右侧的图像时，它会循环到列表的第一张图像），并添加 `show` 属性，如下：

```javascript
next = curr.next().length ? curr.next() :
       curr.parent().children(':first');
next.addClass("show");
```

![image](img/cd.jpg) CD 上的 HTML5 页面 `JQSketchSolid1.html` 阐述了如何使用 jQuery 和 CSS3 在 HTML5 页面中创建一个基础的素描程序。

Figure 3.2 在 MacBook 的 Chrome 浏览器中显示 `JQSketchSolid1.html`。

![image](img/fig3.2.jpg)

*图 3.2 在 MacBook 的 Chrome 浏览器中使用 jQuery 绘图。*

用于 3D 动画的 jQuery 插件 `rotate3di` 允许对 HTML 内容以及其他视觉效果进行动画处理，其主页在这里：

*[`www.zachstronaut.com/projects/rotate3di/`](http://www.zachstronaut.com/projects/rotate3di/)*

![image](img/cd.jpg) 你还可以将 jQuery 与 SVG 结合，而不是动态创建使用 CSS3 选择器样式的 `<div>` 元素。随附的 CD 包含 HTML5 页面 `JQArchDoubleEllipse1Rotate1.html`，它介绍了如何将 jQuery 与 SVG 结合。然而，这段代码与之前的代码示例相似，因此其内容在本书中省略。

![image](img/cd.jpg) CD 上的 HTML5 页面 `JQBouncingBalls1.html` 阐述了如何在 jQuery HTML5 页面中渲染一组垂直跳跃的球。Figure 3.3 显示了在带有 Android ICS 的 Asus Prime 平板上渲染此 HTML5 页面的结果。

![image](img/fig3.3.jpg)

*图 3.3 带有 Android ICS 的 Asus Prime 平板上的跳球。*

jQuery 插件 `PFold` 提供了一种良好的折叠效果，可以在此处下载：

*[`tympanus.net/Development/PFold/`](http://tympanus.net/Development/PFold/)*

## 动画：比较 CSS3 与 jQuery

HTML5 页面 `JQSlideShow1.html` 阐述了如何使用 jQuery 创建包含 JPG 图像的幻灯片，它使用以下代码块来确定下一个 HTML `<img>` 元素（当到达最右侧的图像时，它会循环到列表的第一张图像），并添加 `show` 属性，如下：

```javascript
next = curr.next().length ? curr.next() :
       curr.parent().children(':first');
next.addClass("show");
```

用于 3D 动画的 jQuery 插件 `rotate3di` 允许对 HTML 内容以及其他视觉效果进行动画处理，其主页在这里：

*[`www.zachstronaut.com/projects/rotate3di/`](http://www.zachstronaut.com/projects/rotate3di/)*

第一个链接是 Christian Heilmann 写的的一篇文章，包含了五个性能相关的建议：

*[`christianmann.com/2013/01/25/five-things-you-can-do-to-make-html5-perform-better/`](http://christianmann.com/2013/01/25/five-things-you-can-do-to-make-html5-perform-better/)*

第二个链接提供了性能基准（它与 Christian 的其中一个略有不同）：

*[`blog.tumult.com/2013/02/28/transform-translate-top-left/`](http://blog.tumult.com/2013/02/28/transform-translate-top-left/)*

第三个链接是 Opera 网站上一篇文章，比较了 CSS3 和 jQuery 的性能：

“CSS3 遥遥胜出。性能上的巨大差异是因为浏览器的 CSS 处理器是用 C++ 编写的，原生代码执行非常快，而 jQuery (JavaScript) 是一种解释型语言，在就将发生什么事件方面，浏览器无法提前预判。”

上述引言来自以下网站：

http://dev.opera.com/articles/view/css3-vs-jquery-animations/#comments

上述网站还说明了以下内容：

“尽管上面的结果表明你应该使用 CSS3 进行动画，但请记住我们在文章早些时候讨论的优缺点。你需要考虑到很大比例的人仍然在使用 Internet Explorer 7 和 8，因此如果你的动画绝对需要在这些旧浏览器中正常工作，就应该使用 jQuery。”

## 总结

本章介绍了 jQuery 图形和动画效果，并提供了说明如何使用 jQuery 函数创建简单动画效果的代码示例。特别是，你学习了如何执行以下操作：

-   jQuery 中的基础动画
-   jQuery 中的 Effect 操作
-   jQuery 中的滚动效果
-   使用 CSS3 选择器
-   使用 `css()` 函数设置属性
-   切换 CSS 属性
-   创建圆角
-   创建阴影效果
-   设置线性径向渐变
-   处理图像
-   `hide()` 和 `show()` 函数
-   使用回调函数
-   `fadeIn()`、`fadeOut()` 和 `fadeTo()` 方法
-   设置速度
-   切换 `hide()` 和 `show()`
-   jQuery 淡入淡出和滑动效果
-   `fadeIn()` 和 `fadeOut()` 函数
-   `jQuery` 的 `slideUp()` 和 `slideDown()` 函数
-   `jQuery` 中的缓动函数
-   使用 `animate()` 自定义 CSS 动画
-   创建图片幻灯片
-   基于 CSS3 的动画效果
-   使用 CSS3 的简单滑动效果
-   使用 CSS3 更新多个属性
-   使用 CSS 的滑动效果
-   使用 CSS3 keyFrames 和 2D 变换的动画效果
-   使用 CSS3 和 `jQuery` 进行 2D 变换
-   使用 CSS3 和 `jQuery` 进行 3D 变换
-   使用 `jQuery` 的鼠标跟随示例
-   你的第一个绘画程序

下一章将为你介绍各种 `jQuery UI` 控件，以及展示如何在 HTML5 页面中渲染某些 `jQuery UI` 控件的代码示例。

# jQuery UI 控件

本章将为你介绍各种 `jQuery UI` 控件，以及展示如何在 HTML5 页面中渲染某些 `jQuery UI` 控件的代码示例。使用这些 UI 控件的理由很简单：它们不需要像编写 way 自定 UI 控件那样花费大量精力，你也不需要维护这些控件的代码。此外，这些 UI 控件在多种浏览器上运行良好。

你将看到使用 `jQuery` 渲染折叠面板、按钮、组合框、日期选择器、进度条、滑动条和标签页的示例。此外，你将学习如何通过处理涉及 `jQuery UI` 控件的用户触发事件。通过查阅 `jQuery` 首页，你可以了解更多可用 UI 控件。

本章中的 `jQuery UI` 控件按字母顺序排列，因此你可以随时跳转阅读，以阅读你感兴趣的 UI 控件。虽然 `jQuery` 文档中提供了这些 UI 控件的信息，但这是一本入门级书籍，因此，在一个方便的地方列出 UI 控件列表，比直接告诉你“去读文档”要恰当得多。在读完本章后，你将能够更好地理解章节末尾冗长的代码示例。该示例展示了一个包含各种 `jQuery UI` 控件的 HTML5 页面，其方式反映了某种真实的场景。

本章还包含了处理用户点击事件的代码示例，这些事件会触发定义在同一 HTML5 页面其他地方（有时是图形化的）元素的更新。这种方法可以让你轻松理解如何实现事件相关的功能，希望你能够将本章中的代码示例调整到你的特定需求。

需要记住的一点是，本章中的 HTML5 页面同时包含 HTML 标记和 `jQuery` 代码。对于较长的网页，将 `jQuery` 代码放在单独的文件中正如我们处理 CSS 样式表那样）更有意义。然而，本章中的几乎每个网页都很短（在 1 页到 1.5 页之间），因此为了方便，将代码保持在单个文件中。

第二点涉及如何编写自己的 `jQuery` 插件，这超出了本书的范围。如果你找不到任何满足需求的现有 `jQuery` 插件，可以在网上找到教你如何编写 `jQuery` 插件的教程。

## 在章中使用 jQuery 2.0

以下代码示例在 `jQuery` 1.5 中运行正常，但在 `jQuery` 2.0.0 中无法正常工作：

*   `JQUIProgressBar1.html`（未显示进度条）
*   `JQUISlider1.html`（未显示滑动条）
*   `JQUISliderColors1.html`（未显示滑动条）
*   `JQUIThemes1.html`（使用 GitHub 上提供的插件）

请记住，未来的 `jQuery` 版本无疑将解决这些问题以及你在使用 `jQuery` 的 HTML 网页中可能遇到的其他不一致问题。

## 折叠面板效果

`jQuery UI` 支持折叠面板（accordion）控件，它包含一个或多个“文件夹”，只有在点击特定文件夹时才会显示内容。

示例 4.1 展示了 HTML5 页面 `JQUIAccordion1.html`，展示了如何渲染折叠面板控件。

### 4.1 JQUIAccordion1.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery Accordion</title>
  <link href="JQUIAccordion1.css" rel="stylesheet" type="text/css">
  <link type="text/css" href="css/themename/jquery-ui-1.8.14.custom.css" />
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/ui/1.10.1/jquery-ui.js"></script>
  <link href="JQUIAccordion1.css" rel="stylesheet" type="text/css">
</head>
<body>
  <div id="accordion">
    <h3><a href="#">Section 1</a></h3>
    <div>
      <p> This is the first section of the accordion. </p>
    </div>
    <h3><a href="#">Section 2</a></h3>
    <div>
      <p> This is the second section of the accordion. </p>
      <ul>
        <li>List item one</li>
        <li>List item two</li>
        <li>List item three</li>
      </ul>
    </div>
    <h3><a href="#">Section 3</a></h3>
    <div>
      <p> This is the section of the third accordion. </p>
    </div>
    <h3><a href="#">Section 4</a></h3>
    <div>
      <p> This is the section of the fourth accordion. </p>
      <div id="outer">
        <div id="inner1"></div>
        <div id="inner2"></div>
        <div id="inner3"></div>
      </div>
    </div>
  </div>
  <script>
    $(function() {
      $("#accordion").accordion();
    });
  </script>
</body>
</html>
```

启动列表 4.1 中的 HTML5 页面，并点击渲染后的手风琴控件中的每个“文件夹”，这将显示当前选中文件夹的内容，并隐藏该手风琴中其他文件夹的内容。

图 4.1 显示了在列表 4.1 中`JQUIAccordion1.html`的渲染结果，该截图是从一个运行在 Android ICS 的 Nexus S 4G  Android 应用程序拍摄的横屏模式。

## 按钮

按钮

按钮在 页面中显然非常重要，特别是对于提交表单数据而言，而 jQuery 为按钮相关功能提供了大量的支持。你可以定义 CSS 选择器为 HTML 按钮应用任何你需要的样式效果，包括渐变和阴影效果。

列表 4.3 显示了 HTML5 页面 `JQUIButtons1.html` 的内容，它说明了如何在 HTML 页面中渲染按钮。CSS 样式表 `JQUIButtons1.css` 被省略，因为它的内容与列表 4.2 相同。

### 列表 4.3 JQUIButtons1.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery Buttons</title>
  <link href="JQUIButtons1.css" rel="stylesheet" type="text/css">
  <link type="text/css" rel="Stylesheet" href="css/themename/jquery-ui-1.8.14.custom.css" />
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/ui/1.10.1/jquery-ui.js"></script>
</head>
<body>
  <div id="outer">
    <div class="buttons">
      <button>A regular button</button>
      <input type="submit" value="A submit button">
      <a href="#">An anchor button</a>
    </div>
    <div id="inner1"></div>
    <div id="inner2"></div>
    <div id="inner3"></div>
  </div>
  <script>
    $(function() {
      $( "input:submit, a, button", ".buttons" ).button();
    });
  </script>
  <script>
    $(document).ready(function() {
      var divColors = new Array('#000', '#F0F', '#F00', '#0F0', '#00F', '#0FF');
      var clickCount = 0;
      var color1 = "";
      $("button").click(function() {
        ++clickCount;
        color1 = divColors[(clickCount) % divColors.length];
        $("#inner1").css({background: color1});
      });
      $("input").click(function() {
        ++clickCount;
        color1 = divColors[(clickCount) % divColors.length];
        $("#inner2").css({background: color1});
      });
      $("a").click(function() {
        ++clickCount;
        color1 = divColors[(clickCount) % divColors.length];
        $("#inner3").css({background: color1});
      });
    });
  </script>
</body>
</html>
```

列表 4.3 包含一个 `<script>` 元素，它通过一行代码将 `button()` 方法应用于三个 HTML 元素，并将它们转换为 jQuery 按钮，如此片段所示：

```javascript
$("input:submit, a, button", ".buttons").button();
```

注意，`.buttons` 类（用于样式化包含 HTML 按钮和锚点的 `<div>` 元素）在前面的代码片段中也被指定了。这个额外的类在代码中是多余的，但它向你展示了指定一组想要转换为 jQuery 按钮的 HTML 元素的灵活性。

接下来的代码块渲染了三个 `<div>` 元素，其颜色是在关联样式表中定义的对应选择器中指定的。启动列表 4.3 中的 HTML 页面，当你点击顶行的按钮（包括锚点链接）时，矩形会改变。例如，由于以下代码的作用，每当用户点击按钮时颜色就会改变：

```javascript
$("button").click(function() {
  ++clickCount;
  color1 = divColors[(clickCount) % divColors.length];
  $("#inner1").css({background: color1});
});
```

在前面的事件处理器中，颜色是从 JavaScript 数组 `divColors` 中选择的。图 4.2 显示了列表 4.3 中`JButtons.html`的渲染结果，该截图是从 iPad 拍摄的横屏模式。

![image](img/fig4.2.jpg)
图 4.2 iPad 上的按钮

## 复选框和单选按钮

复选框和单选按钮

jQuery 允许为复选框和单选按钮添加事件处理器，以便你可以确定哪些被选中了。列表 4.4 显示了 `JCheckboxRadio1.html` 的内容，它说明了如何在 HTML 页面中渲染一个复选框和一组单选按钮。CSS 样式表 `JCheckboxRadio1.css` 被省略，因为它的内容与列表 4.2 相同。

### 列表 4.4 JCheckboxRadio1.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>Checkbox and Radio Buttons</title>
  <link href="JCheckboxRadio1.css" rel="stylesheet" type="text/css">
  <link type="text/css" href="css/themename/jquery-ui-1.8.14.custom.css" />
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/ui/1.10.1/jquery-ui.js"></script>
  <style>
    #CheckBoxRadioInfo, #CheckBoxRadio2 {
      font-size: 20px;
      top: 10px;
      width: 50%;
      height: 50px;
    }
  </style>
</head>
<body>
  <div id="outer">
    <div>
      <fieldset id="CheckBoxRadioInfo">
        <label for="checkbox1">Check Something:</label>
        <input type="checkbox" name="checkbox1" id="checkbox1">
        <input type="radio" name="radio" value="radio1" checked="checked">
        <input type="radio" name="radio" value="radio2">
        <input type="radio" name="radio" value="radio3">
      </fieldset>
    </div>
    <div>
      <fieldset id="CheckBoxRadio2">
        <label for="checkbox1">You Clicked:</label>
        <input type="checkbox" name="checkbox1" id="checkbox1">
        <input type="radio" name="radio" value="radio1" checked="checked">
        <input type="radio" name="radio" value="radio2">
        <input type="radio" name="radio" value="radio3">
      </fieldset>
    </div>
  </div>
  <script>
    $(document).ready(function() {
      var divColors = new Array('#000', '#F0F', '#F00', '#0F0', '#00F', '#0FF');
      var clickCount = 0;
      var color1 = "";
      $("button").click(function() {
        ++clickCount;
        color1 = divColors[(clickCount) % divColors.length];
        $("#inner1").css({background: color1});
      });
      $("input").click(function() {
        ++clickCount;
        color1 = divColors[(clickCount) % divColors.length];
        $("#inner2").css({background: color1});
      });
      $("a").click(function() {
        ++clickCount;
        color1 = divColors[(clickCount) % divColors.length];
        $("#inner3").css({background: color1});
      });
    });
  </script>
</body>
</html>
```

图 4.3 MacBook 上 Chrome 浏览器中的复选框/按钮。

## 组合框 (Combo Boxes)

jQuery 支持 HTML 组合框，你可以为其绑定事件处理器以检测与这些 HTML 元素相关的事件。

列表 4.5 显示了 `JQUIComboBox1.html` 的内容，展示了如何在 HTML 网页中渲染组合框，以及当用户在组合框中选择不同的值时执行一段代码块。

### 列表 4.5 JQUIComboBox1.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>jQuery ComboBox</title>
  <link type="text/css" href="css/themename/jquery-ui-1.8.14.custom.css" />
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/ui/1.10.1/jquery-ui.js"></script>
  <style>
    #ComboBoxInfo {
      position: relative;
      font-size: 20px;
      top: 10px;
      width: 50%;
      height: 50px;
    }
  </style>
</head>
<body>
  <div id="outer">
    <div>
      <fieldset id="ComboBoxInfo">
        <label for="ComboBox"><strong>我的组合框：</strong></label>
        <select id="ComboBox">
          <option value="1">值 1</option>
          <option value="2">值 2</option>
          <option value="3">值 3</option>
          <optgroup label="Group1">
            <option value="4">值 4</option>
            <option value="5">值 5</option>
            <option value="6">值 6</option>
          </optgroup>
        </select>
        <label for="selected1"><strong>你选择了：</strong></label>
        <input id="selected1" type="text" value="">
      </fieldset>
    </div>
  </div>
  <script>
    $(document).ready(function() {
      $("#ComboBox").change(function() {
        // 显示选中的值
        $("#selected1").val(
          $("#ComboBox option:selected").text());
      });
    });
  </script>
</body>
</html>
```

列表 4.5 非常直观：第一部分引用了所需的 jQuery 文件，紧接着是一个 HTML `<style>` 元素，然后是组合框中项目的的定义。

每当用户更改组合框中选中的项目时，这段代码块就会执行：

```javascript
$("#ComboBox").change(function() {
  // 显示选中的值
  $("#selected1").val(
    $("#ComboBox option:selected").text());
});
```

图 4.4 显示了在 Chrome 浏览器中渲染列表 4.5 中 `JQUIComboBox.html` 的结果。

![Figure 4.4](img/fig4.4.jpg) MacBook 上 Chrome 浏览器中的组合框。

## 日期选择器 (Date Pickers)

jQuery 支持“日期选择器”，允许你设置过去、现在和未来的日期，并能够以相关上下文的方式修改这些日期。

列表 4.6 显示了 HTML5 页面 `JDatePicker.html` 的内容，展示了如何在 HTML 页面中渲染日期选择器组件。省略了 CSS 表表 `JDatePicker.css`，因为它的内容与列表 4.2 相同。

### 列表 4.6 JDatePicker.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>日期选择器</title>
  <script src="http://code.jquery.com/jquery-ui-1.8.4.min.js"></script>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/ui/1.10.1/jquery-ui.js"></script>
  <style>
    #input1, #input2, #input3 {
      width: 150px;
      height: 50px;
      float: left;
    }
  </style>
</head>
<body>
  <div id="outer">
    <div id="input1">
      上周：
      <input type="text" name="date" id="date1" />
    </div>
    <div id="input2">
      今天的日期：
      <input type="text" name="date" id="date2" />
    </div>
    <div id="input3">
      未来的日期：
      <input type="text" name="date" id="date3" />
    </div>
  </div>
  <script>
    $(document).ready(function() {
      // 设置日期为上周
      var defaultDate1 = $("#date1").datepicker("option", "defaultDate");
      $("#date1").datepicker( "option", "defaultDate", -7 );
      // 设置日期为今天
      var defaultDate2 = $("#date1").datepicker("option", "defaultDate");
      $("#date2").datepicker("option", "defaultDate", +0 );
      // 设置日期为未来
      var futureDate = "07/07/2017";
      $("#date3").datepicker("setDate",futureDate);
    });
  </script>
</body>
</html>
```

图 4.5 显示了在 Chrome 浏览器中渲染列表 4.6 中 `JDatePicker.html` 的结果。

![Figure 4.5](img/fig4.5.jpg) MacBook 上 Chrome 浏览器中的日期选择器。

## 进度条 (Progress Bars)

你可以使用 jQuery 轻松创建和更新进度条。列表 4.7 显示了 `JProgressBar.html` 的内容，并了如何在 HTML 页面中渲染进度条。

### 列表 4.7 JProgressBar.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>进度条</title>
  <link rel="stylesheet" type="text/css" href="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8/base/jquery-ui.css"/>
  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/ui/1.10.1/jquery-ui.js"></script>
  <style>
    #progressBar1 {
      width: 30%;
    }
  </style>
</head>
<body>
  <div id="outer">
    <div id="progressBar1">
      进度条：
      <div id="progressBar1"> </div>
    </div>
    <div id="value1">
      进度条值：
      <input id="text1" type="text" value="0" />
    </div>
    <div id="newValue">
      设置新值：
      <input id="newVal" type="text" value="0" />
    </div>
  </div>
  <script>
    $(document).ready(function() {
      $("#progressBar1").progressbar({ value: 40 });
      $("#text1").val($("#progressBar1").progressbar("value"));
      $("#newValue").bind("change", function() {
        var newVal = $("#newVal").val();
      });
    });
  </script>
</body>
</html>
```



进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```
if (condVar > someVal) {console.log("xxx")}
```



Jade 还支持注释（单行和多行）、条件逻辑、“case”语句、过滤器和迭代。

作为一个更具体的示例，列表 6.1 显示了 `layout.jade` 的内容，它生成了一个非常基础的 HTML5 页面。

**列表 6.1 layout.jade**

```jade
doctype 5

html

  head

    title= title

    link(rel='stylesheet', href='/css/style.css')

    script(src='/js/jquery-1.8.2.min.js')

    script(src='/js/client.js')

    script(src='/js/templates.js')

  body  

    block content
```

如你在列表 6.1 中所示，Jade 使用简单的语法来定义 CSS 样式表链接以及定义 HTML `<script>` 元素。

此外，Jade 允许你扩展模板的内容并使用条件逻辑。列表 6.2 根据 `user.id`（在其他地方定义）是否存在来扩展 `layout.jade` 的内容。

**列表 6.2 index.jade**

```jade
extends layout

block content

  h1= title

  - if (user.id)

    p Hello #{user.name}, and welcome to #{title}

    p

      a(href='/managebooks') My Book List

    p

      a(href='/logout') Logout

    #bookhistory

  - else

    div

      a(href='/login') Login with password

    div

      a(href='/register') Register
```

如你所见，列表 6.2 的第一部分（以“if”开头）显示了欢迎消息和一个链接，当前登录的用户可以通过那里查看书籍列表。列表 6.2 的第二部分（以“else”开头）显示了一个带有登录页链接的 `<div>` 元素以及另一个用于注册页的 `<div>` 元素。

### 使用 Jade 的最小 NodeJS 代码示例

本节展示了如何创建一个微型的 NodeJS 应用程序，它使用了三个文件（放在 views 子目录下）和一个 JavaScript 文件：

- `views/index.jade`
- `views/layout.jade`
- `views/navigation.jade`
- `server.js`

以下是 `index.jade` 的内容：

```jade
h1

a(href='http://www.google.com/') Google Page
```

以下是 `layout.jade` 的内容：

```jade
doctype5

html(lang='en')

  head

    title= title

  body!= body
```

以下是 `navigation.jade` 的内容：

```jade
div#navigation

  a(href='/') home
```

列表 6.3 显示了 `server.js` 的内容，它引用了本节中的三个 Jade 文件。

**列表 6.3 server.js**

```javascript
var express = require('express');

var app = express.createServer();

app.configure(function () {

  app.set('views', __dirname + '/views');

  app.set('view engine', 'jade');

});

app.get('/', function(req, res) {

  res.render('index.jade', { pageTitle: 'Jade Example', layout: false });

});

app.listen(9000);
```

虽然我们还没有涵盖 Node 代码，但你可以看到代码创建了一个应用程序，设置了一些配置，然后渲染由 view 子目录下基于 Jade 的模板定义的 HTML 页面。更详细一点，列表 6.3 从创建一个名为 `app` 的基于 express 的应用程序开始。接下来，代码指定了当前目录的 views 子目录（由内置变量 `__dirname` 指定），并将 Jade 配置为“视图引擎”。下一部分代码指定了对 GET 请求要做什么，如下：

```javascript
app.get('/', function(req, res) {

  res.render('index.jade', { pageTitle: 'Jade Example', layout: false });

});
```

此前的代码通过返回 `index.jade`（在 views 子目录下）的内容来渲染响应，该内容是一个带有指向 Google 首页链接的 HTML 页面。最后一行代码监听 localhost 的 9000 端口。你必须通过 `cd` 进入该目录来启动此 Node 应用程序。

### 其他模板解决方案

有许多可用的其他模板解决方案，一些更流行的列在这里：

- Mustache.js
- Handlebars.js
- Dust.js
- jQuery.tmpl 插件
- Underscore Micro-templating
- PURE

你可以在网上找到如何使用上述模板引擎的链接和教程。

## MongoDB

MongoDB 是一种流行的 NoSQL 数据库，其主页在此：

[`www.mongodb.org/`](http://www.mongodb.org/)

开始使用 MongoDB 的地方是：

[`mongolab.com/home`](https://mongolab.com/home)

在此网站下载并安装 MongoDB：

[`www.mongodb.org/downloads`](http://www.mongodb.org/downloads)

安装 MongoDB 后，你可以通过在另一个 shell 中输入 `mongo` 来启动交互会话，允许允许从命令行管理 schema 并执行类 CRUD 操作（CRUD 代表创建、读取、更新和删除，四个关键数据库操作）。

例如，下面的命令序列向你展示如何在 users schema 中插入新用户（该 schema 在本章后面的 Mongoose 部分定义）。

```bash
mongo

> use db

switched to db db

> users = db.users

db.users

> users.find();

> users.insert({firstName:'a', lastName:'b'});

> users.find()

{
  "_id" : ObjectId("509425f82685d84f9c41c858"),
  "firstName": "a",
  "lastName": "b"
}
```

查阅文档可以获取有关在 MongoDB shell 中执行的命令的更多细节。

## NodeJS

NodeJS 是一种执行 JavaScript 的流行的服务器技术。你可以从其主页下载并安装 NodeJS：

[`nodejs.org/`](http://nodejs.org/)

![image](img/cd.jpg) 本节将仅描述基本信息以及你为了配合 CD 上示例应用程序中使用的 NodeJS 服务器而所需的模块。

在你的机器上安装 NodeJS 之后，请使用以下命令安装 `express` 和 `mongoose`：

```bash
npm install express
npm install mongoose
```

为了向你展示可以在不使用模板引擎（如 `Jade`）的情况下使用 NodeJS，列表 6.4 显示了 `HelloWorld.js` 的内容，当用户在浏览器中导航到 `localhost:5000` 时，该文件会显示文本字符串“Hello World”。

**列表 6.4 HelloWorld.js**

```javascript
//创建一个应用服务器

var express = require("express");

var app = express();

//向客户端发送 'Hello World' 

app.get('/', function(req, res) {

    res.send('Hello World');

});

app.listen(5000);
```

按照如下方式从命令行启动应用程序：

```bash
node HelloWorld.js
```

启动浏览器并导航到 URL [`localhost:5000`](http://localhost:5000)。你将看到文本字符串“Hello World.”

现在你已经看到了如何启动简单的 NodeJS 应用程序（带有和不带模板的），你已经准备好创建一个使用 Mongoose 和 MongoDB 的 NodeJS 应用程序，这是本章下一节的主题。

# Mongoose (#toc.html_toc-h1-0063)

Mongoose 是一个用于 MongoDB 的 ORM（用 NodeJS 编写），它允许你在 MongoDB 数据库中定义模式（schemas），它的主页在这里：

[`mongoosejs.com/index.html`](http://mongoosejs.com/index.html)

使用 npm 包管理器安装 Mongoose，如下：

```bash
npm install mongoose
```

接下来的章节将向你展示如何通过 Mongoose 连接到 MongoDB 实例，随后是一个创建模式、创建模式实例、然后修改并将这些实例保存到 MongoDB 数据库的示例。

## 通过 Mongoose 连接到 MongoDB (#toc.html_toc-h2-0046)

你可以使用 `mongoose.connect()` 方法连接到 MongoDB。以下命令是连接到在默认端口（27017）运行的本地 `myapp` 数据库所需的最小值：

```javascript
mongoose.connect('mongodb://localhost/myapp');
```

你可以根据你的环境在 `uri` 中指定额外的参数：

```javascript
mongoose.connect('mongodb://username:password@host:port/database');
```

请参考文档获取连接 MongoDB 数据库的更多选项。

## 在 Mongoose 中创建模式 (#toc.html_toc-h2-0047)

Mongoose 中允许的 `SchemaTypes` 有：`String`、`Number`、`Date`、`Buffer`、`Boolean`、`Mixed`、`ObjectId` 和 `Array`。

首先，我们需要定义两个引用 mongoose 和 MongoDB 数据库的变量：

```javascript
var mongoose = require('mongoose'),

    db = mongoose.createConnection('localhost', 'test');
```

现在让我们在 Mongoose 中创建一个简单的 `Person` 模式：

```javascript
var personSchema = new mongoose.Schema({

    id:         Schema.Types.ObjectId,

    firstName: String,

    lastName:  String

})
```

我们可以为我们的 `Person` 模式添加方法，如下所示：

```javascript
personSchema.methods.pname = function () {

  var fullname = this.firstname+" "+this.lastname;

  console.log(fullname);

}
```

接下来，我们按照如下方式将 `Person` 模式编译为 `Model`：

```javascript
var Person = db.model('Person', personSchema);
```

注意，模型（model）只是一个允许我们构建文档的类。在这个示例中，文档是一个 `Person` 对象。

让我们创建两个 `Person` 对象：

```javascript
var p1 = new Person({ firstName: 'John', lastname: 'Smith' })

var p2 = new Person({ firstName: 'Jane', lastname: 'Jones' })
```

最后，我们可以按照如下方式将对象保存到 MongoDB：

```javascript
p1.save(function (error) {

    if (error) {

        console.log("error saving p1");

    }

});

p2.save(function (error) {

    if (error) {

        console.log("error saving p2");

    }

});
```

你可以在 Mongoose 模式中指定其他属性，例如索引、setter 和 getter。例如，下面的代码块向你展示如何通过几个额外的属性扩展 `User` 模式的定义：

```javascript
mongoose.model('User', {

  properties: ['first, 'last'],

  cast:      {age: Number},

  indexes:   ['first', 'last'],

  setters:   {first: function(){} },

  getters:    {full_name: function(){} },

  methods:   {save: function() }

});
```

## SPA 代码示例 (#toc.html_toc-h2-0048)

SPA 代码示例创建了三个 Mongoose 模式来表示用户、书籍以及用户对书籍的评论。

`userSchema` 包含了用户的信息以及每个用户读过的书籍列表。这里存在一对多的关系（每个用户可以读多本书），如下所示：

```javascript
var userSchema = new mongoose.Schema({

  firstName: String,

  lastName: String,

  books: [Object]

});
```

`bookSchema` 包含了书籍的信息以及对该书籍的评论列表。这里存在一对多的关系（每本书可以有多条评论），如下所示：

```javascript
var bookSchema = new mongoose.Schema({

  title: String,

  author: String,

  comments: [Object]

});
```

`commentSchema` 包含了用户对书籍的评论。它引用了一个用户和一条书籍，如下所示：

```javascript
var commentSchema = new mongoose.Schema({

  user: Schema.Types.ObjectId,

  book: Schema.Types.ObjectId,

  text: String

});
```

```javascript
, app = express.createServer()

, mongoose = require('mongoose')

, db = mongoose.createConnection('localhost', 'test');

/* models */

mongoose.connect('mongodb://127.0.0.1/sampledb');

var Schema = mongoose.Schema

  , ObjectId = Schema.ObjectID;

// 在 Mongoose 章节之前声明的 schemas

var userSchema = ...

var bookSchema = ...

var commentSchema = ...

var Book    = db.model('Book', bookSchema);

var User     = db.model('User', userSchema);

var Comment = db.model('Comment', commentSchema);

// 一本新书，一个新用户，以及关于

// 新用户对新书的评论：

var b1 = new Book({bookAuthor:  'Oswald Campesato',

                   bookTitle:   'HTML5 Canvas and CSS3 Graphics',

                   bookPubDate: '07/30/2012'

                   });

var u1 = new User({firstName:  'John', lastname: 'Smith'});

var c1 = new Comment(

         {userid: u1, bookid: b1, comment: "Great book!"});

// 将用户 u1 添加到读过这本书的用户列表（在 b1 中）:

b1.users.push(u1);

// 将书籍 b1 添加到用户 u1 读过的书籍列表（在 u1 中）:

u1.books.push(b1);

//显示书籍

app.get('/showbooks', function(req,res){

  console.log("finding books");

    Book.find({}, function(error, data){

      res.json(data);

    });

});

//显示用户

app.get('/showusers', function(req,res){

  console.log("finding users");

    User.find({}, function(error, data){

      res.json(data);

    });

});

// 添加用户的示例 URL：

//http://localhost:3003/adduser/tom/smith

app.get('/adduser/:first/:last/:username', function(req, res){

  console.log("adding user");

  var user_data = {

        first_name: req.params.first

    , last_name: req.params.last

    , username: req.params.username

  };

  var user = new User(user_data);

  user.save( function(error, data){

    if(error){

        res.json(error);

    }

    else{

        res.json(data);

    }

  });

});

app.listen(3003);

console.log("listening on port %d", app.address().port);
```

Listing 6.5 整合了你在本章早些看到的许多代码片段。还存在代码块，允许你通过从 URL 中提取相关信息来添加新用户，然后构建以下保存到数据库的结构：

```javascript
// 添加用户的示例 URL：

//http://localhost:3003/adduser/tom/smith

app.get('/adduser/:first/:last/:username', function(req, res){

  var user_data = {

        first_name: req.params.first

    , last_name: req.params.last

    , username: req.params.username

  };

  var user = new User(user_data);

  user.save( function(error, data){

    if(error){

        res.json(error);

    }

    else{

        res.json(data);

    }

  });

});
```

jQuery Mobile 本质上是 jQuery 插件和组件的集合，允许你编写可以在多个平台上运行的移动 Web 应用。你已经知道 jQuery 专注于桌面 Web 应用程序；相比之下，jQuery Mobile（包含 CSS 样式表和 JavaScript 库）是为移动设备设计的。然而，jQuery Mobile 依赖“基础”jQuery 库，在 Web 页面引用 jQuery Mobile 库之前，必须先引用 jQuery。此外，jQuery Mobile 使用了 HTML5 和 CSS3 功能（如过渡和动画）以及用于导航的小型图标。

jQuery Mobile 依赖于带有 `data-` 前缀的自定属性。如果你不知道，自定义属性是 HTML5 中引入的新特性，并且始终具有此类前缀。这种对自定义数据属性的支持为 HTML5 标记提供了某些 XML 中可用的功能。这使得代码能够处理自定义标签及其值，同时通过验证。

一个简单的 jQuery Mobile 页面具有以下结构：

*   一个带有 `data-role="header"` 属性的可选 `<div>` 元素
*   一个带有 `data-role="content"` 属性的强制 `<div>` 元素
*   一个带有 `data-role="footer"` 属性的可选 `<div>` 元素

在初始化期间，jQuery Mobile 会预处理 Web 页面并插入额外的标记、CSS 类和处理器。你将在本章稍后的“Hello World”代码示例中 jQuery Mobile 如何修改 Web 页面的示例。

在编写 jQuery Mobile Web 页面时，有几个需要注意的重要细节。首先，jQuery Mobile 提供了以下页面相关的事件，你可以在 jQuery Mobile 页面的生命周期内程序化地调用：`pageInit()`、`pageCreate()`、`pageShow()` 和 `pageHide()`。其次，jQuery Mobile 支持处理用户手势的自定义事件，如滑动、点击、长按和设备方向变化。第三，jQuery Mobile 使用主题来定制移动应用程序的外观，并结合渐进式增强（在第 1 章）中简要讨论），使你的移动应用程序运行在各种支持 Web 的设备上。

另一个需要记住的关键点是 jQuery 使用了这种结构：

```javascript
$(document).ready() {

  // do something here

}
```

另一方面，jQuery Mobile 使用这种结构：

```javascript
$(selector).live('pageinit', (function(event){

  // do something here

}));
```

注意它们的重点不同：jQuery 在 Web 页面加载后发送事件，而 jQuery Mobile 在页面（或页面视图）初始化时发送事件。

## jQuery Mobile 中的核心功能和组件 (#toc.html_toc-h2-0049)

如果你已经阅读了之前涵盖 jQuery 的章节，你已经获取了大量关于 jQuery 特性的知识。这些知识出于另一个原因有用：jQuery Mobile 使用 jQuery 作为基础，在你的 HTML5 Web 页面中，jQuery 库必须始终于 jQuery Mobile 库。

jQuery Mobile 提供了许多实用的功能，将简化创建移动应用程序的过程。这里列出 jQuery Mobile 的功能：

*   兼容主要的移动平台（Android、iOS 等）
*   使用 HTML5 标记
*   采用渐进式增强方法
*   提供紧凑的工具包（压缩后约 12K）
*   支持插件和主题
*   支持基于触摸和鼠标的用户手势
*   支持 WAI-ARIA

此外，jQuery Mobile 支持以下组件（以及此处未列出的其他）：

*   按钮
*   表单元素
*   列表视视图
*   页面和对话框
*   工具栏

书中的 jQuery 代码示例使用简单的命名约定：包含 jQuery 代码的 HTML5 Web 页面名称以“JQ”开头，包含 jQuery Mobile 的 HTML5 页面名称以字母“JQM”开头。记住，此命名约定仅适用于本书。

## 最小 jQuery Mobile Web 页面 (#toc.html_toc-h1-0067)

列表 7.1 显示了 `JQMHelloWorld1.html` 的内容，它说明了在桌面浏览器、平板电脑或智能手机上渲染时，如何在 HTML5 Web 页面中显示“Hello World”消息。

**列表 7.1 JQMHelloWorld1.html**

```html
<!DOCTYPE html>

<html lang="en">

  <head>

    <meta charset="utf-8" />

    <title>Hello World from jQuery Mobile</title>

    <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />

    <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>

    <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>

    <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>

  </head>

  <body>

    <div data-role="page">

      <div data-role="header">

        <h2>This is the Header</h2>

      </div>

      <div data-role="content">

        <p>Hello World from a Simple jQuery Mobile Page</p>

      </div>

      <div data-role="footer">

        <h2>This is the Footer</h2>

      </div>

    </div>

  </body>

</html>
```

列表 7.1 结构直观易懂：它由一个单一页面视图（一个带有 `data-role="page"` 属性的 HTML `<div>` 元素）组成，其中包含三个 `<div>` 元素：分别页眉部分、内容部分和页脚部分。

图 7.1 显示了在运行 Android ICS 的 Asus Prime 平板电脑上通过横屏模式截屏渲染列表 7.1 中 HTML Web 页面的结果。

对比图 7.1 与图 7.2，后者显示了在运行 Android ICS 的 Sprint Nexus 4G 智能手机上横屏运行的示例 jQuery Mobile 应用程序，使用的是与图 7.1 相同的二进制文件。注意页眉和页脚是如何延伸到屏幕宽度的。

图 7.1 显示了在运行 Android ICS 的 Asus Prime 平板电脑上通过横屏模式截屏渲染列表 7.1 中 HTML Web 页面的结果。

图 7.2 显示了在运行 Android ICS 的 Sprint Nexus 4G 智能手机上横屏运行的示例 jQuery Mobile 应用程序，使用的是与图 7.1 相同的二进制文件。注意页眉和页脚是如何延伸到屏幕宽度的。

现在在基于 Webkit 的浏览器中启动列表 7.1，并对比你在图 7.1 和图 7.2 中看到的内容。

你之前已经学过 jQuery Mobile 如何使用额外的标签和 CSS 类增强移动 Web 页面。jQuery Mobile 在列表 7.1 的 HTML5 Web 页面中“注入”了各种 CSS 类（属于 jQuery Mobile 的）。通常情况下，你不需要担心这些细节；但如果你需要更深入地理解这些细节，可以深入研究 jQuery Mobile 的源码。光盘上的 HTML5 页面 `JQMHelloWorld1Enhanced.html` 展示了 jQuery 如何“增强”HTML5 Web 页面 `HelloWorld1.html` 的内容。

正如你在之前的代码示例所示，jQuery Mobile 中的每个页面视图都由一个带有 `data-role="page"` 属性的 HTML `<div>` 元素定义，并包含一个可选的头部（header）、一个必需的内容元素（content）和一个可选的页脚（footer）。

页面之间的导航非常简单：只需在 jQuery Mobile 应用中为带有 `data-role="content"` 属性的 `<div>` 元素添加链接即可，如下：

```html
<div data-role="content">

  <p>A second page view<a href="#home">Home</a>a></p>

</div>
```

当用户点击链接时会发生页面视图之间的切换，jQuery Mobile 会自动处理切换所需的细节。本章节后面将提供一个包含多个页面视视图的 jQuery Mobile Web 页面的完整示例（以及如何在页面视图之间导航）。

## jQuery Mobile 自定义属性

jQuery Mobile 使用 `data-role` 属性来识别“页面视图”（本质上是一个屏幕）的不同部分，其支持的一些值包括 `page`、`header`、`content` 和 `footer`。`data-role` 属性也用于增强 HTML 元素。例如，如果你在无序列表的 HTML `<ul>` 标签中指定属性 `data-role="listview"`，那么 jQuery Mobile 将进行必要的增强（如插入标记、添加 CSS 类和暴露监听器），使你能够像处理小部件一样处理无序列表。

另一个示例是，你可以通过向块级 HTML5 `<nav>` 元素添加属性 `data-role="navbar"` 来创建一个导航栏，关联列表项（封装在 HTML5 `<nav>` 元素中）中的文本字符串将作为导航栏中的标签元素显示。

`data-transition` 属性指定切换页面视图或显示对话框时的切换效果。由于这些切换基于 CSS3，因此它们仅在支持 CSS3 的浏览器（如基于 WebKit 的浏览器）中有效。`data-transition` 属性的允许值为 `fade`、`flip`、`pop`、`slide`、`slidedown` 和 `slideup`。

其他一些自定义 jQuery Mobile 属性包括 `data-backbtn`、`data-divider`、`data-direction`、`data-icon`、`data-inline`、`data-position`、`data-rel` 和 `data-url`。

## jQuery Mobile 页面切换

jQuery Mobile 提供了页面切换（以及事件和 `ui` 对象），你可以在绑定到任何页面切换的自定义代码块中引用它们。请记住，“页面”可以是一个独立的 HTML Web 页，也可以是当前加载的 HTML Web 页内部的 HTML `<div>` 元素。

以下是页面初始化期间发生的页面事件序列：

- `pagebeforecreate`: 首先触发
- `pagecreate`: 在 DOM 填充后触发
- `pageinit`: 在初始化完成后触发
- `pagebeforeshow`: 在切换到“目标”页面前触发
- `pageshow`: 在切换到“目标”页面后触发

每当用户点击一个导航到首次首次加载的页面的链接时，会发生以下事件序列：

- `pagebeforehide`: 在切换前在“离开”页面上触发
- `pagebeforeshow`: 在切换前在“目标”页面上触发
- `pagehide`: 在切换后在“离开”页面上触发
- `pageshow`: 在切换后在“目标”页面上触发

每当使用 AJAX 加载新页面时，会发生以下事件序列：

- `pagebeforeload`: 在进行 AJAX 调用之前
- `pageload`: 在 AJAX 调用完成后触发
- `pageloadfailed`: 如果 AJAX 调用失败则触发

在页面切换期间，`ui.nextPage` 被赋值为切换的目标页面，如果没有下一个页面则赋值为空的 jQuery 对象。同样，`ui.prevPage` 被赋值为切换前的当前页面，如果没有上一个页面则赋值为空 jQuery 对象。

jQuery Mobile 内部功能使用基于 AJAX 的异步方法调用，因此它区分了页面加载事件与页面显示和隐藏事件。当文件以同步方式加载到浏览器时会发生页面加载事件，可以使用 `jQuery(document).ready()` 方法以及其他初始化事件。注意，在某些情况下，你可以显式指定同步而非异步方法调用，但本章未讨论此功能（如果需要更多细节，请查看在线 jQuery Mobile 文档）。

正如你将在本章后面看到的，单个 HTML Web 页可能包含多个 jQuery Mobile 页面视图，用户可以多次在这些页面视图之间导航。这些切换不会触发页面加载事件；jQuery Mobile 提供了一组在每次页面切换发生时发生的事件。

由于页面隐藏和显示事件在每次页面切换时都会触发，请确保你不要多次绑定事件处理程序，可以先检查事件处理程序是否已绑定（如果是则什么都不做），或者在重新绑定到给定事件之前清除之前的绑定。

列表 7.2 显示了 `JQMPageEvents1.html` 的内容，说明了页面事件执行的序列。

**列表 7.2 JQMPageEvents1.html**

```html
<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="utf-8">

  <title>JQuery Mobile Page Events</title>

  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.min.css">

  <script src="http://code.jquery.com/jquery-1.6.4/jquery.min.js"></script>

  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile.min.js"></script>

</head>

<body>

  <div data-role="page" id="page1">

    <div data-role="header">

      <h3>jQuery Mobile Page Events</h3>

    </div>

    <div data-role="content">

      <p>A second page view<a href="#home">Home</a>a></p>

    </div>

    <div data-role="footer">

      <h3>Footer</h3>

    </div>

  </div>

  <script>

    $(page1).live("pagebeforecreate", function() {

      console.log("pagebeforecreate");

    });

    $(page1).live("pagecreate", function() {

      console.log("pagecreate");

    });

    $(page1).live("pageinit", function() {

      console.log("pageinit");

    });

    $(page1).live("pagebeforehide", function() {

      console.log("pagebeforehide");

    });

    $(page1).live("pagebeforeshow", function() {

      console.log("pagebeforeshow");

    });

    $(page1).live("pagehide", function() {

      console.log("pagehide");

    });

    $(page1).live("pageshow", function() {

      console.log("pageshow");

    });

  </script>

</body>

</html>
```

接下来，jQuery Mobile 会搜索带有 `data-` 属性的子元素，并为它们添加主题类、适当的 ARIA 角色，并在必要时为第一页之外的所有页面页头添加返回按钮。

最后，jQuery Mobile 会增强按钮、控制组和表单控件，并对工具栏进行任何必要的调整。

因此，jQuery Mobile 代表你执行了大量工作，这意味着你无需受这些繁琐且低级细节的困扰，可以专注于你的移动应用程序的功能。

还有更多好消息：当用户在移动应用程序的不同页面之间导航时，jQuery Mobile 会自动处理页面过渡和返回按钮。jQuery Mobile 还通过执行异步获取（使用 `AJAX`）处理外部页面，并将该外部页面集成到当前文档中（如果未找到外部页面，将显示错误消息）。外部页面整合到当前文档中带有 `data-role="page"` 属性的第一个元素中（同时忽略该页的所有内容）。

注意，如果 jQuery Mobile 无法找到 Web 页面或该页面不包含 `data-role="page"` 属性的元素，它将显示错误消息。确保外部 Web 页面中的 `id` 值与当前 Web 页面中的 `id` 值不同。

顺便说，你可以通过两种方式覆盖默认的页面加载：在链接上指定目标属性（如 `_blank`），或者在链接上指定 `rel="external"` 属性。

# mobileinit 事件

jQuery Mobile 在执行后立即在 `document` 对象上触发 `mobileinit` 事件，因此你可以绑定到它并覆盖任何默认配置。

例如，假设你需要防止 jQuery Mobile 在整个移动应用程序中特定类型的 HTML 元素应用样式规则。以下代码块阻止了 jQuery Mobile 将其样式规则（全局范围内）应用于 HTML `<input>` 和 `<textarea>` 元素：

```javascript
$(document).bind('mobileinit',function () {

    $.mobile.page.prototype.options.keepNative = "input,textarea";

});
```

注意，`data-role="none"` 属性的作用与上述代码块相同，区别在于它仅应用于包含该属性的特定元素。

## jQuery Mobile 选项与自定义

jQuery Mobile 为各种对象提供了选项和方法，包括 `.mobile`、`.mobile.path` 和 `.mobile.history`。你有许多可以为移动应用程配置的选项，我们将在本节中介绍其中几个。一个明显有用的方法是 jQuery Mobile 的 `pageLoading()` 方法，它可以显示和隐藏 jQuery Mobile 的加载对话框。你使用布尔值 `true` 调用此方法来隐藏对话框，并在不带参数调用此方法来显示对话框，所示：

```javascript
// 显示页面加载对话框

$.mobile.pageLoading();

// 隐藏加载对话框

$.mobile.pageLoading(true);
```

你还可以自定义“加载消息”以及过渡效果的类型，所示：

```javascript
$.mobile.loadingMessage = "wait a few moments ";

$.mobile.defaultPageTransition = "pop";
```

实现与前两行相同功能的另一种方法所示：

```javascript
$.extent($.mobile, {

    "loadingMessage" = "wait a few moments",

    "defaultPageTransition" = "pop"

});
```

事实上，你可以按照以下方式使用自己的初始化配置 jQuery Mobile：1) 创建一个在 jQuery Mobile 加载之前加载的脚本，2) 为 `mobileinit` 事件绑定事件处理程序。

如果你想了解更多关于 jQuery Mobile 自定义初始化、选项和方法的信息，请阅读 jQuery 文档以深入了解如何使用它们。

# 页面导航与切换页面

当用户在你的移动 Web 应用程序导航时，jQuery Mobile 也会更新 `location.hash` 对象，包含每个页面视图的唯一 URL（由带有 `data-role="page"` 属性的元素定义）。jQuery Mobile 将每个页面的 URL 存储在分配给页面“容器”元素的 `data-url` 属性中。

jQuery Mobile �还提供了一系列方法，允许你通过程序处理页面更改和滚动。这些方法之一是 `changePage()`，其语法如下：

```javascript
changePage(to, transition, back, changeHash);
```

`to` 参数是一个指定元素 `id` 或文件名（以及许多其他选项）的字符串，它是目标页面的引用。`transition` 参数是应用程序进入目标页面时创建的过渡效果名称。`back` 参数是一个布尔值，指定过渡是否为反向。最后，`changeHash` 参数是一个布尔值，指定是否更新 `location.hash` 对象。

`changePage()` 方法允许你创建更复杂的页面过渡效果。例如，以下代码段在用户点击 `.back-btn` 时跳转到页面 `#first`，并使用反向的“flip”效果且不更新位置 hash：

```javascript
$(".back-btn").bind("click", function () {

    changePage("#first", "flip", true, false);

});
```

jQuery Mobile 还提供了 `silentScroll()` 方法，带有一个单整数值来指定目标。当调用此方法时，滚动监听器不会被触发。例如，以下代码将滚动到 200：

```javascript
$.mobile.silentScroll(200);
```

## jqdata() 选择器

在第 1 章中，你学习了 `data()` 方法。jQuery Mobile 提供了一个名为 `jqdata()` 的相应方法，它是选择自定义属性的自定义选择器。例如，在 jQuery 中，你可以使用此代码选择 Web 页面中包含 `data-` 属性的所有元素：

```javascript
$("[data']")
```

你可以使用 `jqdata()` 选择相同的元素集合，所示：

```javascript
(":jqdata()")
```

注意，`jqdata()` 选择器通过为字符串指定一个值（默认为空）来为你自动处理命名空间，避免标签冲突。

这种方法比创建一个具有多个 HTML5 页面的移动应用程序更高效。尽管 HTML5 Web 页面的初始下载时间可能更长，当用户导航到页的不同部分时，没有额外的 Internet 。

列表 7.3 显示了 `JQMMultiPageViews1.html` 的内容，说明了如何在单个 HTML5 Web 页面中的内部页面视图之间导航。

```html
LISTING 7.3: JMMultiPageViews1.html

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8" />

  <title>jQuery Mobile: Page Views</title>

  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />

  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>

  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>

  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>

</head>

<body>

<div data-role="page" id="first">

  <h1>First Page</h1>

  <a href="#second" class="btn">Go to Second Page</a>

</div>

<div data-role="page" id="second">

  <h1>Second Page</h1>

  <a href="#first" class="btn back-btn">Go to First Page</a>

</div>

</body>

</html>
```

```html
<div data-role="page" id="home">

  <div data-role="header"><h1>首页页头</h1></div>

  <div data-role="content">

    <p>这是主页的内容</p>

    <p><a href="#about">点击此处获取更多信息</a></p>

  </div>

  <div data-role="footer"><h1>首页页脚</h1></div>

</div>

<div data-role="page" id="about">

  <div data-role="header"><h1>关于此页的页头</h1></div>

  <div data-role="content">

    <p>第二个视图（目前就是全部）</p>

    <a href="#home">点击此处或点击“返回”按钮回到首页</a>

  </div>

  <div data-role="footer"><h1>关于此页的页脚</h1></div>

</div>

</body>

</html>
```

[列表 7.3 包含了两个页面视图，正如 HTML `<div>` 元素所指定的，其 `id` 属性值为 `home` 和 `about`（在列表 7.3 中以**粗体**显示）。当用户导航到第二个页面视图时，此代码段将返回第一个页面视图：

```html
<a href="#home">点击此处或点击“返回”按钮回到首页</a>
```

jQuery Mobile 应用中的页面视图（或屏幕）是顶层同级元素，每个元素都包含 `data-role="page"` 属性（因此页面不能嵌套）。

jQuery Mobile 框架会在每个页面视图上自动生成返回按钮和主页按钮，但你可以通过指定 `data-backbtn="false"` 属性来抑制返回按钮，如下：

```html
<div data-role="header" data-backbtn="false">

  <h1>页头</h1>

</div>
```

图 7.4 显示了在列表 7.3 中的 HTML Web 页面在运行 Android ICS 的 Sprint Nexus S 4G 上的横屏截图中的渲染结果。

![image](img/fig7.4.jpg)

**图 7.4** 在运行 Android ICS 的 Sprint Nexus S 4G 多页应用。

当你点击 Web 页面上的链接时，应用程序将导航到第二个屏幕，其代码定义也包含在列表 7.3 中。

## 在页面视图中定位页头和页脚 (#toc.html_toc-h1-0072)

jQuery Mobile 可以通过三种方式动态定位页头和页脚工具栏：

- **标准 (Standard)**：工具栏根据文档流呈现，随着用户滚动数据，会进入和离开视口。这是默认设置。
- **固定 (Fixed)**：页头和页脚将出现在视口的顶部和底部，并在用户滚动时时保持在那里。点击屏幕将导致它们返回到文档流中的常规位置。
- **全屏 (Fullscreen)**：页头和页脚将出现在视口内，并在用户滚动时保持显示，无论用户处于内容的哪个位置。点击屏幕将隐藏它们。本质上，页头和页脚从文档流中移除，并始终动态定位在视口的顶部和底部。

在 `<header>` 或 `<footer>` 标签中包含 `data-position="fixed"` 属性可以创建固定页头和页脚，如列表 7.4 所示，该列表显示了 `JQMFixed1.html` 的内容。

**列表 7.4 JQMFixed1.html**

```html
<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="utf-8" />

  <title>jQueryMobile 中的固定页头和页脚</title>

  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.1.1.0.min.css" />

  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>

  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>

  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>

</head>

<body>

  <div id="page1" data-role="page">

    <header data-role="header" data-position="fixed">

      <h1>jQuery Mobile</h1>

    </header>

    <div class="content" data-role="content">

      <h3>内容区域。</h3>

    </div>

    <footer data-role="footer" data-position="fixed">

      <h3>固定页脚</h3>

    </footer>

  </div>

</body>

</html>
```

列表 7.4 包含了 HTML 标记和单个页面视图，该视图还为页头和页脚指定了 `data-position="fixed"` 属性。

你也可以通过在 `data-role="page"` 元素中包含 `data-position="fixed"` 属性以及 `fullscreen="true"` 属性来创建全屏页头或页脚，如下：

```html
<section id="page1" data-role="page">

  <header data-role="header" data-position="fixed">

    <h1>jQuery Mobile</h1>

  </header>

  <div class="content" data-role="content">

    <h3>内容区域。</h3>

  </div>

  <footer data-role="footer" data-position="fixed">

    <h3>固定页脚</h3>

  </footer>

</section>
```

<p><a href="#about">关于此页</a></p>

图 7.5 显示了列表 7.5 中的 HTML 页面在 MacBook 上的渲染结果。

![image](img/fig7.5.jpg)

**图 7.5** MacBook 上的固定页头/页脚。

jQuery Mobile 按钮元素或类型为 `submit`、`reset`、`button` 或 `image` 的输入元素不需要 `data-role="button"` 属性，因为 jQuery Mobile 会自动将这些元素视为基于链接的按钮。

虽然原始的基于表单按钮没有显示，但它仍然包含在 HTML 标记中。当链接按钮上发生点击事件时，对应的原始表单按钮也会发生相应的点击事件。

## 按钮组与列网格

jQuery Mobile 允许你通过定义一个指定了 `data-role="controlgroup"` 属性的容器 HTML `<div>`元素并包含一个或多个按钮元素，将一组按钮（或复选框或单选按钮）渲染为一个区块。包含的按钮的默认渲染方式是水平的（一行），你可以通过指定 `data-type="vertical"` 属性将按钮渲染为垂直组。

jQuery Mobile 会渲染按钮，移除按钮之间的间距（以及外阴投影），并对第一个和最后一个按钮进行“圆角”处理，以创建类似组的效果。下面的代码块展示了如何指定一个水平按钮组：

```html
<div data-role="controlgroup">

  <a href="index1.html" data-role="button">One</a>

  <a href="index2.html" data-role="button">Two</a>

  <a href="index3.html" data-role="button">Three</a>

</div>
```

需要记住的一点：如果按钮数量超过屏幕宽度，按钮将“换行”到额外的行。[Listing 7.5] 展示了你如何渲染水平按钮组和垂直按钮组。

jQuery Mobile 框架允许你通过一种名为 `ui-grid` 的区块样式类约定来渲染 CSS 列。你可以通过使用类值 `ui-grid-a`、`ui-grid-b`、`ui-grid-c` 和 `ui-grid-d` 分别渲染两列、三列、四列和五列布局。下面的代码块说明了如何渲染两列布局：

```html
<div class="ui-grid-a">

  <div class="ui-block-a">Block 1 and text inside will wrap</div></div>

  <div class="ui-block-b">Block 2 and text inside will wrap</div></div>

</div>
```

注意下方代码块中显示三列布局时的区别：

```html
<div class="ui-grid-b">

  <div class="ui-block-a">Block 1 and text inside will wrap</div></div>

  <div class="ui-block-b">Block 2 and text inside will wrap</div></div>

  <div class="ui-block-c">Block 3 and text inside will wrap</div></div>

</div>
```

你可以在这里找到更多细节和代码示例：

[`jquerymobile.com/demos/1.0b1/#/demos/1.0/docs/content/content-grids.html`](http://jquerymobile.com/demos/1.0b1/#/demos/1.0/docs/content/content-grids.html)

## 使用主题渲染按钮

jQuery Mobile 拥有完善的主题系统，涉及标记为“a”到“e”的主题，用于控制按钮的样式化方式。当链接添加到容器中时，jQuery Mobile 会为其分配一个与其父元素主题匹配的主题“色块”字母。例如，放置在主题为“a”（默认主题下为黑色）的内容容器中的按钮，会自动被分配按钮主题“a”（默认主题下为炭灰色）。

这里显示了一个按钮主题示例：

```html
<div data-role="footer" class="ui-bar">

  <a href="left.html" data-icon="arrow-l" data-role="button" data-theme="a">Left</a>

</div>
```

[Listing 7.5] 显示了 `JQMButtons1.html` 的内容，它阐述了如何水平和垂直渲染按钮、如何应用不同的主题以及如何指定自定义 CSS 选择器。

### 列表 7.5 JQMButtons1.html

```html
<!DOCTYPE html>

<html lang="en">

  <head>

    <meta charset="utf-8" />

    <title>Multiple Buttons and Themes in jQuery Mobile</title>

    <link rel="stylesheet" href="CSS3Background1.css" />

    <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />

    <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>

    <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>

    <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>

  </head>

  <body>

    <div id="page1" data-role="page">

      <div data-role="header">

        <!-- 此按钮出现在左侧 -->

        <a href="abc.html" data-icon="arrow-l" data-theme="b">Index</a>

        <h1>Rendering Buttons in Mobile</h1>

        <!-- 此按钮出现在右侧 -->

        <a href="def.html" data-icon="plus" data-theme="e">Add</a>

      </div>

      <div class="content" data-role="content">

        <div data-role="controlgroup" data-type="horizontal">

          <a href="index1.html" data-role="button">One</a>

          <a href="index2.html" data-role="button">Two</a>

          <a href="index3.html" data-role="button">Three</a>

          <a href="index4.html" data-role="button">Four</a>

          <a href="index5.html" data-role="button">Five</a>

        </div>

        <a href="index6.html" class="shadow" data-role="button">Vertical1</a>

        <a href="index7.html" class="shadow" data-role="button">Vertical2</a>

        <a href="index8.html" class="shadow" data-role="button">Vertical3</a>

        <div data-role="controlgroup">

          <a href="index6.html" data-role="button">Vertical1</a>

          <a href="index7.html" data-role="button">Vertical2</a>

          <a href="index8.html" data-role="button">Vertical3</a>

        </div>

        <div>

          <a href="index9.html" data-role="button" id="cancel" data-inline="true">Cancel</a>

          <a href="index10.html" data-role="button" id="submit" data-inline="true" data-theme="b">Save</a>

        </div>

      </div>

      <div data-role="footer" class="ui-bar">

        <!-- 显示四个键 -->

        <a href="left.html" data-icon="arrow-l" data-theme="a">Left</a>

        <a href="up.html" data-icon="arrow-u" data-theme="b">Up</a>

        <a href="down.html" data-icon="arrow-d" data-theme="c">Down</a

        <a href="right.html" data-icon="arrow-r" data-theme="e">Right</a>

      </div>

    </div>

  </body>

</html>
```

列表 7.5 中底部的四个 HTML `<a>` 元素渲染了四个方向箭头，因为它们具有 `data-icon` 属性，且值分别设置为 `arrow-l`、`arrow-u`、`arrow-d` 和 `arrow-r`。此外，这四个 HTML `<a>` 元素为 `data-theme` 属性指定了不同的值，并根据每个预定义的 jQuery Mobile 主题的视觉显示进行渲染。

请注意，列表 7.6](#ch07.html_lst7.6) 中的 HTML `<a>` 元素引用的 HTML 页面并未为此移动应用程序定义。因此，当用户点击这些链接时，将看到错误消息。

### 列表 7.6 CSS3Background1.css

```css
#cancel, #submit, .shadow {

  background-color:white;

  background-image:

    -webkit-radial-gradient(red 4px, transparent 18px),

    -webkit-repeating-radial-gradient(red 2px,  green 4px,

                               yellow 8px, blue 12px,

                                     transparent 28px,

                                     green 20px, red 24px,

                                     transparent 28px,

                                     transparent 32px),

    -webkit-repeating-radial-gradient(red 2px,  green 4px,

                                     yellow 8px, blue 12px,

                                     transparent 28px,

                                     green 20px, red 24px,

                                     transparent 28px,

                                     transparent 32px);

  background-size: 50px 60px, 70px 80px;

  background-position: 0 0;

  -webkit-box-shadow:  30px 30px 30px #400;

}
```

列表 7.6 包含了你在 第 2 章 中熟悉的定义。如果你需要复习，可以参考该章节中的相关部分。

图 7.6 显示了在带有 Android 的 Nexus 设备上渲染列表 7.5](#ch07.html_lst7.5) 中 HTML 页面的结果。

![图 7.6](img/fig7.jpg) Nexus 设备上的按钮。

如你所示，jQuery mobile 中有很多与样式相关的选项，因此关于 jQuery Mobile 按钮的总结可能有所帮助：
* 带有 `data-role="button"` 属性的锚点链接将被渲染为按钮。
* 任何 `type` 为 `button`、`submit` 或 `image` 的 `input` 元素都被分配类 `ui-btn` 并显示为按钮。
* 添加 `data-icon` 属性可以创建带有图标的按钮。
* 添加 `data-pos` 属性可以图标的位置。
* 指定 `data-inline="true"` 可使渲染的按钮宽度仅与其文本等宽。
* `data-role="group"` 在 `<div>` 元素中垂直（或水平）分组。
* `data-theme="e"` 属性是五个主题（从“a”到“e”）中的第五个。

### jQuery Mobile 中的列表视图

jQuery Mobile 支持列表视图（在移动应用程序中非常常见）以及多种变体，包括列表按钮、嵌套列表视图和列表拆分按钮。jQuery Mobile 可以通过对列表应用 `data-role="listview"` 属性来增强有序列表和无序列表。嵌入 `<a>` 标签内部的列表元素响应用户手势，如列表 7.7](#ch07.html_lst7.7)所示，该列表显示了 jQuery Mobile 页面 ListView.html 的内容。

### 列表 7.7 ListView.html

```html
<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="utf-8" />

  <title>List Views in jQuery Mobile</title>

  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />

  <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>

  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>

  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>

</head>

<body>

  <div data-role="page">

    <div data-role="header"><h2>This is the Header</h2></div>

    <div data-role="content">

      <h3>Simple Unordered List Example</h3>

      <ul data-role="listview">

        <li><a href="#">Unordered Item 1</a></li>

        <li><a href="#">Unordered Item 2</a></li>

        <li><a href="#">Unordered Item 3</a></li>

      </ul>

      <h3>Simple Ordered List Example</h3>

      <ol data-role="listview">

        <li><a href="#">Ordered Item 1</a></li>

        <li><a href="#">Ordered Item 2</a></li>

        <li><a href="#">Ordered Item 3</a></li>

      </ol>

    </div>

    <div data-role="footer"></div>

  </div>

</body>

</html>
```

每当你点击任何链接时，你都会看到一条错误消息。

图 7.6 显示了在带有 Android 的 Nexus 设备上渲染列表 7.5](#ch07.html_lst7.5) 中 HTML 页面的结果。

![图 7.6](img/fig7.jpg) Nexus 设备上的按钮。

列表 7.7 显示了 jQuery Mobile 页面 ListView.html 的内容。

jQuery Mobile 支持列表视图（在移动应用程序中非常常见）以及多种变体，包括列表按钮、嵌套列表视图和列表拆分按钮。jQuery Mobile 可以通过对列表应用 `data-role="listview"` 属性来增强有序列表和无序列表。嵌入 `<a>` 标签内部的列表元素响应用户手势，如列表 7.7](#ch07.html_lst7.7)所示，该列表显示了 jQuery Mobile 页面 ListView.html 的内容。

导航栏通常包含一组按钮，允许用户在页面之间导航。jQuery Mobile 允许你在页页头、页脚或内容区域包含导航栏。

要指定导航栏，请对块级元素（如 `<nav>` 元素）应用 `data-role="navigation"`。导航元素内的锚点标签将被格式化为按钮组。jQuery Mobile 将自动处理按钮的激活和非激活状态，如 HTML5 页面 NavigationBar.html 所示。

jQuery Mobile 允许你显示和隐藏菜列表，你还可以使用过渡效果在菜单列表显示或隐藏时创建动画效果。HTML5 页面 Menu.html 阐述了如何创建一个滑动菜单。

jQuery Mobile 使用 AJAX 进行表单提交，并将尝试将服务器响应集成到应用程序 DOM 中，提供预期的过渡效果。如果你希望防止 jQuery Mobile 使用 AJAX 处理表单，请对 `form` 标签应用 `data-ajax="false"` 属性。

```html
<head>

  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>

  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>

</head>

<<body>

  <script>

    var xmlData = "", count = 0;

    $("#page1").live('pageinit', (function(event){

      $.ajax({

        url: 'http://localhost:9000/sample.xml',

        dataType: 'xml',

        success: function(data) {

          $(data)

            .find('svg')

            .children()

            .each(function() {

              var node = $(this);

              var x      = node.attr('x');

              var y      = node.attr('y');

              var width  = node.attr('width');

              var height = node.attr('height');

              var stroke = node.attr('stroke');

              var fill   = node.attr('fill');

              // 其他处理在此...

              ++count;

              console.log("element: "+node);

            });

          console.log("element count: "+count);

        },

        error: function() {

          alert('未找到数据');

        }

      })

    })

    );

  </script>

  <div id="page1" data-role="page">

    <div data-role="header">页眉</div>

    <div data-role="content">

      <p>来自 jQuery Mobile 的 Hello World</p>

    </div>

    <div data-role="footer">页脚</div>

  </div>

</</body>

</html>
```

示例 7.8 包含了 HTML 标记和一次 jQuery Mobile AJAX 调用，该调用会在此网页加载到浏览器后执行。随后，代码将处理 XML 文档 `sample.xml`（显示在 示例 7.9 中）中 `<svg>` 元素的所有子元素，如下：

```javascript
var node = $(this);

var x      = node.attr('x');

var y      = node.attr('y');

var width  = node.attr('width');

var height = node.attr('height');

var stroke = node.attr('stroke');

var fill   = node.attr('fill');

```

为了说明起，这段代码假设 示例 7.9 中的 XML 文档 `sample.xml` 包含上述代码指定的属性的 XML 元素。

**示例 7.9 sample.xml**
```xml
<?xml version='1.0' encoding='iso-8859-1'

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="100%" height="100%">

  <rect x="50" y="10" width="100" height="200" stroke="blue" fill="red" />

  <rect x="200" y="10" width="100" height="200" stroke="blue" fill="green" />

  <rect x="350" y="10" width="100" height="200" stroke="blue" fill="blue" />

</svg>



将 示例 7.8 和 7.9 中的文件放在同一目录下，并启动一个在端口 `9000` 上提供服务的 Web 服务器。在笔记本电脑或桌机的 Chrome 浏览器中打开 示例 7.8 中的 HTML 页面，打开 Chrome 开发者工具，并检查 Chrome 控制台的内容。你将看到类似图 7.8](#ch07.html_fig7.8) 的内容，它显示了 MacBook 上 Chrome 浏览器中 Chrome 开发者工具的内容。

![图 7.8](img/fig7.jpg) # jQuery Mobile 与地理定位

在第 5 章中，你学习了如何获取用户的地理定位信息。在本节中，你将看到如何使用 jQuery Mobile 来获取地理定位。示例 7.10 显示了 `JQMGeoLocation.html` 的内容，说明了如何在 HTML5 页面中获取地理定位。

**示例 7.10 JQMGeoLocation.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>JQuery Geolocation</title>
  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />
  <script src="http://code.jquery.com/jquery-2.0.0.js"></script>
  <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
  <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>
  <!-- google maps API -->
  <script src="http://maps.google.com/maps/js?sensor=false"></script>
  <style>
    #theMap, #theCoords {
      font-size: 16px;
      height: 200px;
      width: 400px;
    }
  </style>
  <script>
    function findUserLocation() {
      // 指定 'success' 和 'fail' JavaScript 函数
      navigator.geolocation.getCurrentPosition(successCallback, errorCallback);
    }
    function successCallback(position) {
      var latitude = position.coords.latitude;
      var longitude = position.coords.longitude;
      var latlong = new google.maps.LatLng(latitude, longitude);
      var myOptions = {
        zoom: 14,
        center: latlong,
        mapTypeId: google.maps.MapTypeId.ROADMAP
      };
      // 使用 Google Maps 显示当前位置
      var map = new google.maps.Map(document.getElementById("theMap"), myOptions);
      /*
      var marker = new google.maps.Marker({
        position: initialLocation,
        map: map,
        title: "I Am Here!"
      });
      */
      // 在控制台中显示位置详情
      positionDetails(position);
    }
    function errorCallback(error) {
      if(error.code == error.PERMISSION_DENIED) {
        console.log("错误：你必须允许地理定位访问");
      } else if(error.code == error.PERMISSION_UNAVAILABLE) {
        console.log("错误：地理定位不可用");
      } else if(error.code == error.TIMEOUT) {
        console.log("错误：超时");
      }
    }
    function positionDetails(pos) {
      var positionStr =
        "纬度:"+ pos.coords.latitude +"<br>" +
        "经度:"+ pos.coords.longitude +"<br>" +
        "精度:"+ pos.coords.accuracy +"<br>" +
        "高度:"+ pos.coords.altitude +"<br>" +
        "高度精度:"+ pos.coords.altitudeAccuracy +"<br>" +
        "方向:"+ pos.coords.heading +"<br>" +
        "速度:"+ pos.coords.speed;
      $("#theCoords").html(positionStr);
      console.log(positionStr);
    }
  </script>
</head>
<body>
  <div data-role="page" id="page1">
    <div data-role="header"><h3>JQuery Geolocation</h3></div>
    <div data-role="content" id="content">
      <div id="theMap"></div>
      <form id="geoLocationForm">
        <input type="button" id="geobutton" value="点击查找我的位置">
      </form>
      <div id="theCoords"></div>
    </div>
    <div data-role="footer"><h3>页脚</h3></div>
  </div>
  <script>
    $("#page1").live('pageinit', (function(event){
      $("#geobutton").bind("vmousedown",function(event, ui){
        findUserLocation();
      });
    }));
  </script>
</body>
</html>
```

在本章中，你学习了 jQuery Mobile 的各种功能，并并通过代码示例了解了如何处理事件、创建具有多个视图的 Web 页面以及如何使用 HTML 组件创建表单。你还学习了如何使用 CSS3 阴影和渐变效果（你在第 3 章中学习过）为 jQuery Mobile Web 页面中的按钮样式。你学习了如何在使用 jQuery Mobile 的 HTML 页面中实现以下操作：

* 渲染按钮
* 显示简单和嵌套列表
* 渲染滑动菜单
* 使用 AJAX 使用 jQuery Mobile
* 结合定位使用 jQuery Mobile

# 第 8 章

## jQuery Mobile 中的用户手势与动画效果

本章包含许多代码示例，演示了如何处理用户手势以及如何在 jQuery Mobile 中创建动画效果。幸运的是，jQuery Mobile 为用户手势触发了事件，例如 `orientationchange`、`scrollstart`、`scrollstop`、`swipe`、`swipeleft`、`swiperight`、`tap` 和 `taphold`。本章的第一部分向你展示了如何处理其中的一些用户手势。你还将看到代码示例，展示如何在 jQuery 中创建与滑动相关和淡入相关的动画效果。本节最后最后简要讨论了 jQuery Mobile 虚拟鼠标事件，当你需要在 HTML Web 页面中处理鼠标相关事件以及触摸相关事件时，它可以简化你的代码。

本章的第二部分向你展示了如何使用 jQuery Mobile 创建 CSS3 2D/3D 动画效果。一个代码示例使用 jQuery Mobile 创建了 3D 立方效果。此外，光盘中还有渲染“跳动球”的示例，展示了如何获取移动设备的加速度值并在 jQuery Mobile Web 页面中显示实时值。

![image](img/cd.jpg) 回想你在第 2 章中学习了如何创建 CSS3 2D 和 3D 效果，在第 3 章中学习了如何在 HTML5 Web 页面中将这些效果结合 jQuery。在本章中，你将看到如何使用 jQuery Mobile 创建一些相应的效果。

### 在 jQuery Mobile 中处理用户手势和事件

jQuery Mobile 为用户手势触发了一系列事件，例如 `orientationchange`、`scrollstart`、`scrollstop`、`swipe`、`swipeleft`、`swiperight`、`tap` 和 `taphold`。

如果你需要处理许多用户手势，可以考虑使用 jQuery 插件而不是编写自己的代码。目前有各种插件可用，接下来的章节将简要讨论其中两个插件。

当你想在 HTML Web 页面上检测用户手势时，你可以使用 jQuery 的 `.on("click")` 方法编写自定义 jQuery 代码来处理这些手势。请复阅第 1 章中关于在 jQuery 1.7 及以后版本中弃用的 jQuery 事件相关方法的章节，以及推荐的处理事件的 jQuery 方法。

你可能已经知道，当用户点击某个元素时，会发生 `tap` 事件，而当用户触摸某个元素并保持接触一秒钟时，会发生 `taphold` 事件。你可以通过以下代码段在 jQuery Mobile 中绑定 `tap` 事件和 `taphold` 事件：

```javascript
$("body").bind("tap", function () {
  console.log("Tap Event on the body Element");
  return false;
});
$("body").bind("taphold", function () {
  console.log("Tap Hold Event on the body Element");
  return false;
});
```

jQuery 事件处理程序内部的 `return false` 语句等同于在 jQuery 事件对象上调用 `e.preventDefault()`（防止默认事件发生）以及 `e.stopPropagation()`（防止事件“冒泡”），该对象是作为参数传递给 JavaScript 函数的（本例中未提供）。请记住，非 jQuery 事件处理程序中的 `return false` 语句并阻止已发生事件的“冒泡”行为。

当在一秒的时间间隔内以 `30px`（或更大）的速度进行水平拖动时，会发生 `swipe` 事件。当 `swipe` 事件分别向左或向右移动时，会发生 `swipeleft` 和 `swiperight` 事件。

代码列表 8.1 显示了 `JQMSwipeEvents1.html` 的内容，说明了如何在 jQuery Mobile 中处理点击事件以及左滑和右滑事件。

***代码列表 8.1  JQMSwipe-TapEvents1.html***
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Swipe and Tap Events in jQuery Mobile</title>
    <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.css" />
    <script src="http://code.jquery.com/jquery-2.0.0b1.js"></script>
    <script src="http://code.jquery.com/jquery-migrate-1.1.0.js"></script>
    <script src="http://code.jquery.com/mobile/1.1.0/jquery.mobile-1.1.0.min.js"></script>
  </head>
  <body>
    <div data-role="page" id="page1">
      <div data-role="header"><h3>Header</h3></div>
      <div data-role="content">
        <img id="sample1" src="Sample1.png" width="150" height="150" />
        <img id="sample2" src="Sample2.png" width="150" height="150" />
        <img id="sample3" src="Sample3.png" width="150" height="150" />
        <div id="sample1">Left:</div>
        <div id="sample2">Middle:</div>
        <div id="sample3">Right:</div>
      </div>
      <div data-role="footer"><h3>Footer</h3></div>
    </div>
    <script>
      <!-- jQuery 事件处理代码从这里开始 -->
      $(page1).live('pageinit',function(event){
        $("body").bind("tap", function () {
          console.log("Tap Event on the body Element");
          return false;
        });
        $("body").bind("taphold", function () {
          console.log("Tap Hold Event on the body Element");
          return false;
        });
      });
    </script>
  </body>
</html>
```

处理用户手势的语法使用了 `jQuery.bind` 方法。例如，你可以使用以下代码段通过 `jGestures` 插件绑定滑动手势：

```javascript
jQuery('#swipe').bind('swipeone',eventHandler);
```

另一个处理各种用户手势的 jQuery Mobile 插件在这里：

[`github.com/eightmedia/hammer.js`](https://github.com/eightmedia/hammer.js)

这个 JavaScript 工具包包含了一系列良好的示例，这些示例说明了如何处理用户手势。由于市面上有许多用于处理用户手势的 jQuery Mobile 插件，建议在互联网上搜索以寻找这些插件，然后对它们进行评估，以确定哪些插件最符合你的需求。

## jQuery Mobile 中的滚动事件

jQuery Mobile 支持以下自定义事件：`orientationchange`（通过更改设备方向，无论是垂直还是水平触发）、`scrollstart`（在滚动开始时触发）和 `scrollstop`（在滚动结束时触发）。你可以像处理其他 jQuery 事件一样，使用 `live()` 或 `bind()` 来绑定这些事件，这些方法在 jQuery 1.7 版本之前的用法在第 6 章中有所讨论。此外，当你的 jQuery Mobile 代码绑定到 `orientationchange` 事件时，回调函数可以指定第二个参数，该参数包含一个等于 `portrait`（竖屏）或 `landscape`（横屏）的方向属性。

![image](img/cd.jpg) CD 上的 HTML5 页面 `JQMScrollEvents1.html` 演示了如何在 jQuery Mobile 中处理滚动事件，其逻辑如下：

```html
<script>
  $("#page1").live('pageinit', (function(event,ui){
    var eventsElement = $('#events');
    $(window).bind('scrollstart', function () {
      console.log('Scroll start');
      $('.ui-body-c').css('background', 'green');
      eventsElement.append('<li><a href="">Start Scroll</a></li>>');
      //eventsElement.listview('refresh');
      eventsElement.listview();
    });
    $(window).bind('scrollstop', function () {
      console.log('Scroll stop');
      $('.ui-body-c').css('background', 'red');
      eventsElement.append('<li><a href="">Stop Scroll</a></li>');
      //eventsElement.listview('refresh');
      eventsElement.listview();
    });
    $(window).bind('orientationchange', function () {
      console.log('Orientationchange change');
      $('.ui-body-c').css('background', 'red');
      eventsElement.append('<li><a href="">Orientation</a></li>');
      //eventsElement.listview('refresh');
      eventsElement.listview();
    });
  });
</script>
```

## 竖屏模式与横屏模式

除了检测移动设备的方向外，你可能还需要在方向改变时更改用于样式 Web 页面元素的 CSS 类。

![image](img/cd.jpg) CD 上的 HTML5 页面 `JQMOrientation1.html` 演示了如何根据移动设备方向轻松地更改与 HTML 元素相关的 CSS 类。关键逻辑包含在此代码块中：

```javascript
$("#page1").live('pageinit', (function(event,ui){
  $(window).bind ('orientationchange', function (e) {
    console.log("new orientation: "+e.orientation);
    $("#content").removeClass('portrait landscape')
    .addClass (e.orientation ? 'landscape' : 'portrait');
  });
}));
```

注意，`orientationchange` 事件绑定到 `window` 对象。在当前示例中，竖屏模式下背景颜色设置为红色，宽度设置为 320px；而横屏模式下背景颜色设置为蓝色，宽度设置为 480px。

另一个需要注意的是，`window.orientation` 在竖屏模式下的值为 0，在横屏模式下值为 -90 或 90。

另一种方法是在你的 HTML 页面中使用以下类型的代码：

```css
@media all and (orientation: portrait) { body {background-color: red} }
```

```html
<link rel="stylesheet" media="all and (orientation: landscape)" href="landscape.css" />
```

图 8.2 显示了在运行 Android ICS 的 Asus Prime 平板电脑上拍摄的横屏图中渲染 `JQMOrientation1.html` 的结果。

![image](img/fig8.2.jpg)

***图 8.2*** 在运行 Android ICS 的 Asus Prime 平板电脑上检测方向。

## 使用 jQuery Mobile 使用动画效果

你可以使用 jQuery Mobile 创建各种基于 jQuery 的动画效果，包括淡入效果、滑动效果和自定�动画。创建动画效果的方法（jQuery 和 jQuery Mobile 共有）包括：`animation()`、`clearQueue()`、`delay()`、`dequeue()`、`fadeIn()`、`fadeOut()`、`fadeTo()`、`fadeToggle()`、`hide()`、`queue()`、`show()`、`slideDown()`、`slideToggle()`、`slideUp()`、`stop()` 和 `toggle()`。

本节包含代码示例，说明了如何在 jQuery Mobile 中创建其中一些动画效果。

### 与淡入相关的方法

jQuery 的 `.fadeIn()` 和 `.fadeOut()` 方法为创建简单动画提供了方便的方法。

![image](img/cd.jpg) CD 上的 HTML5 页面 `JQMFadeInOut1.html` 演示了如何在 jQuery Mobile 页面中使用 jQuery 的 `.fadeIn()` 和 `.fadeOut()` 方法，其主逻辑如下：

```html
<body
  <div data-role="page" id="page1">
    <div id="header" data-role="header">
      <h3>头部文本</h3>
    </div>
    <div id="content" data-role="content">
      <p>来自 jQuery 的 Hello World</p>
      <p>来自 jQuery 的 Goodbye World</p>
      <p>点击此文本可切换此段落。</p>
    </div>
    <div data-role="footer">
      <h3>页脚</h3>
    </div>
  </div>
  <script>
    $("#page1").live('pageinit', (function(event,ui){
      // ... 淡入/淡出的逻辑 ...
    });
  </script>
</body>
```

每当用户点击右侧的图片时，第一张图片会缓慢显示：

```javascript
// display first <img> when users click on the last <img>
$("img:last").click(function () {
    $("img:first").fadeIn("slow");
});
```

你可以使用类似的代码块来捕捉其他 HTML 元素的事件。在这个示例中，我们也可以使用此片段获取所有的 `<p>` 元素：

```javascript
var para = $("p");
```

然而，在 `JQMFadeInOut1.html` 中，我们使用 `$("p:first")` 和 `$("p:last")` 引用第一个最后一个 HTML `<p>` 元素，然后执行类似的淡入效果。

图 8.3 显示了在 MacBook 的 Chrome 浏览器上横屏渲染 `JQMFadeInOut1.html` 的结果。

![image](img/fig8.3.jpg)

**图 8.3** MacBook 上 Chrome 浏览器上的淡入效果。

## 幻灯片相关的 jQuery 方法

正如你所推的，jQuery 的 `.slideUp()` 和 `.slideDown()` 方法为 jQuery Mobile 提供了滑动功能。

![image](img/cd.jpg) CD 中的 HTML5 页面 `JQMSlideUpDown1.html` 展示了如何在 jQuery Mobile Web 页面中使用 jQuery `.slideUp()` 和 `.slideDown()` 方法，这里显示了部分代码：

```html
<body
    <div data-role="page" id="page1">
        <div data-role="header"><h3>Header</h3></div>
        <div data-role="content">
            <p>Click me or one of the Rectangles:</p>
            <div name="first" id="first">First</div>
            <div id="second">Second</div>
            <div id="third">Third</div>
            <div id="fourth">Fourth</div>
        </div>
        <div data-role="footer"><h3>Footer</h3></div>
    </div>
    <script>
        $("#page1").live('pageinit', (function(event,ui) {
            $("#page1").click(function() {
                if ($("div:first").is(":hidden")) {
                    $("div").show("slow");
                } else {
                    $("div[name='first']").slideUp(2000);
                }
                $("div[name='first']").css({background:'#00f'})
                    .show(2000).hide(2000).slideDown(2000);
            })
        }))
    </script>
</body>
```

HTML5 页面 `JQMSlideUpDown1.html` 包含一个 `<style>` 元素，它使用 CSS 对四个矩形应用了某些样式，随后是一个处理页面视图中任何位置点击事件的代码块：

```javascript
$("#page1").click(function() {
    // handle a click event on the page
});
```

jQuery Mobile 代码的核心由一行代码组成，它使用方法链创建一个多部分动画效果，每当用户点击矩形时，该效果会：1) 将背景颜色变为红色，2) 执行为期 2 秒的“显示”和“隐藏”动画效果，随后是 3) 持续 2 秒的“滑动”效果，如下所示：

```javascript
$("div[name='first']").css({background:'#00f'})
    .show(2000).hide(2000).slideDown(2000);
```

图 8.4 显示了在带有 Android ICS 的 Asus Prime 平板上横屏渲染 `JQMSlideUpDown1.html` 的结果。

![image](img/fig8.4.jpg)

**图 8.4** 带有 Android ICS 的 Asus Prime 平板上的淡入效果。

## jQuery Mobile 与过渡效果

jQuery Mobile 使用基于 WebKit 的 CSS3 变换来实现页面过渡，基于 WebKit 的浏览器目前对 CSS3 变换提供了最好的支持（其他浏览器正在提高支持水平）。由于基于 WebKit 的浏览器使用硬件加速，CSS 动画效果在移动设备以及笔记本电脑和桌面上看起来非常平滑。

你通过应用 `data-transition` 属性来指定过渡效果，其七种支持的值为：

*   fade：简单地在之前的内容之上淡入页面或对话框
*   flip：动画页面翻页效果，将当前视图旋转出，并让反面的另一侧视图进来
*   pop：页面从屏幕中心弹入视视图
*   slide：从左侧或右侧滑入，将之前的内容推开
*   slidedown：从顶部向下滑动，覆盖当前内容上方
*   slideup：向上滑动到顶部，显示下方的后续内容

jQuery Mobile 还提供了 `animationComplete` 事件，这在你添加或移除应用 CSS 过渡的类后非常有用。

代码列表 8.2 显示了 `JQMTransition1.html` 的内容，说明了如何在 jQuery Mobile 页面中使用 `slidedown` 和 `flip` 过渡。

**代码列表 8.2 JQMTransition1.html**
```html
<body
    <div data-role="page" id="first">
        <div data-role="header"><h2>This the first page</h2></div>
        <div data-role="content">
            <p><a href="#second" data-transition="slidedown">Go to Page Two</a></p>
        </div>
        <div data-role="footer"><h2>This the first footer</h2></div>
    </div
    <div data-role="page" id="second">
        <div data-role="header"><h2>This the second page</h2></div>
        <div data-role="content">
            <p><a href="#first" data-transition="flip" data-direction="reverse">Go to Page #1 via 'flip' and reverse</a></p>
        </div>
        <div data-role="footer"><h2>This the second footer</h2></div>
    </div>
</body>
```

代码列表 8.2 包含了 jQuery Mobile 页面的代码。当你点击第一个页面视视图中的链接时，你将看到由第一页内容 `<div>`（其 `id` 属性为 first）中的以下片段创建的滑动效果：

```html
<a href="#second" data-transition="slidedown">Go to Page Two
```

第二个页面视视图显示以下文本：You saw a slidedown effect Go to Page #1 via ‘flip’。当你点击之前的链接时，你将看到由第二个页面内容 `<div>`（其 `id` 属性为 second）中的以下片段创建的翻页效果：

```html
<a href="#first" data-transition="flip" data-direction="reverse">
```

注意，jQuery Mobile 将尝试在使用自动返回按钮或隐藏对话框时使用反向过渡。这个简单的示例说明了在不同页面视视图之间导航时可以创建的一些页面效果。你可以尝试许多过渡效果，以找到适合你要求的效果。

图 8.5 显示了在 MacBook 的 Chrome 浏览器上横屏渲染 代码列表 8.2 中 `JQMTransition1.html` 的结果。

![image](img/fig8.5.jpg)

**图 8.5** MacBook 上 Chrome 浏览器上的过渡效果。

## jQuery Mobile 与 CSS3 动画效果

回 jQuery Mobile 使用基于 WebKit 的 CSS3 变换来实现页面过渡。WebKit 浏览器使用硬件加速，使得 CSS 动画效果在移动设备、笔记本电脑和桌面上看起来都很平滑。

代码列表 8.3 显示了 `JQMJender1.html` 的内容，说明了如何在 jQuery Mobile 页面中结合 JPG 文件使用 `slideDown()` 和 `slideUp()`。

**代码列表 8.3 JQMRender1.html**
```html
<body
    <div data-role="page" id="page1">
        <div data-role="content">
            <img id="sample1" src="Sample1.png" width="200" height="200">
            <img id="sample2" src="Sample2.png" width="200" height="200">
            <p>
                <a id="button1" href="#" data-role="button">Click Me To Display The Right Image</a>
                <a id="button2" href="#" data-role="button">Click Me To Shrink The Right Image</a>
            </p>
        </div>
    </div
    <script>
        $("#page1").live('pageinit', (function(event,ui) {
            $("#sample2").hover(function() {
                $(this).slideUp(800);
            })
            $("#sample2").hover(function() {
                $(this).css({'position':'relative',
                             'width':'200px',
                             'height':'200px'
                            });
            });
        });
        $("#button1").click(function() {
            $("#sample2").slideDown(800);
        });
        $("#button2").click(function() {
            $("#sample2").css({'position':'relative',
                               'width':'100px',
                               'height':'100px'
                              });
        });
    </script>
</body
```

Listing 8.3 渲染了两个图像并包含两个绑定到点击事件的按钮。视觉效果取决于点击按钮的顺序。当用户点击第二个按钮（“点击缩小右侧图像”）时，使用以下代码块将最右侧的图像从初始的 200x200 尺寸缩小到 100x100：

```javascript
$("#button2").click(function() {
  $("#sample2").css({'position':'relative',
      'width':'100px',
      'height':'100px'
  });
});
```

如你所见，前面的代码块使用 jQuery 的 `css()` 函数来修改右侧图像的宽度和高度，这意味着没有过渡效果。

接下来，如果用户悬停在右侧的图像（现在已缩小）上，由于以下代码块，图像将带有过渡效果缩小并消失：

```javascript
$("#sample2").hover(function() {
    $(this).slideUp(800);
});
```

现在，如果用户点击第一个按钮（“点击显示右侧图像”），由于以下代码，第二个图像将（再次使用过渡效果）以原始尺寸重新出现：

```javascript
$("#button1").click(function() {
    $("#sample2").slideDown(800);
});
```

这些代码说明了编写 jQuery 代码来创建良好的图像动画效果是多么简单。此外，你可以将 jQuery 动画效果与 jQuery 的 `css()` 函数结合。例如，你可以使用 `css()` 函数在用户点击图像时渲染具有背景径向渐变效果的图像，或者更新图像（或元素）的任何其他 CSS 属性。

因此，你可以对 jQuery 动画、CSS 以及 CSS3 图形和动画的知识，通过简单紧凑的 jQuery 代码来创建有趣的效果。

![image](img/fig8.6.jpg) ***图 8.6*** 在 MacBook 的 Chrome 浏览器上带有动画效果的调整 JPG。

Figure 8.6 显示了在 MacBook 的 Chrome 浏览器上横屏模式渲染 Listing 8.3 中 `JQMRenderJPG1.html` 的结果。

# jQuery Mobile 虚拟鼠标事件 #toc.html_toc-h1-0081

jQuery Mobile 提供了一组“虚拟”鼠标事件来处理鼠标和触摸事件。这些事件非常有用，因为每个事件都处理鼠标事件及其相应的触摸事件，这可以减少 Web 页面中需要编写的代码。此外，虚拟鼠标事件支持同一个 Web 页面上的桌面和移动样式交互。

jQuery Mobile 中的虚拟鼠标事件名称以字母“v”（代表 virtual）开头，随后是鼠标事件的通用或标准名称。例如，`vmousedown` 虚拟事件“传递”了 `mousedown` 事件以及 `touchstart` 事件。虚拟鼠标事件列表（及其对应的触摸相关和鼠标相关事件）所示：

- `vclick` (touchend 或鼠标点击事件)
- `vmousecancel` (触摸或鼠标 mousecancel 事件)
- `vmousedown` (touchstart 或 mousedown 事件)
- `vmousemove` (touchmove 或 mousemove 事件)
- `vmouseover` (触摸或 mouseover 事件)
- `vmouseup` (touchend 或 mouseup 事件)

请记住：在支持触摸的设备上，`vclick` 事件在 `vmouseup` 事件之后触发；然而，`vmouseup` 在 `vmousedown` 之前触发，而 `vmousedown` 在 `vclick` 之前触发，正如你预期的那样。此外，事件对象包含坐标信息的 `pageX`,`pageY`,`screenX`,`screenY`,`clientX` 和 `clientY`，你将在后续示例中看到。

![image](img/cd.jpg) CD 中的 HTML5 Web 页面 `QM2DAnimationGrad4Reflect1.html` 和 CSS 样式表 `QM2DAnimationGrad4Reflect1.css` 展示了如何在 jQuery Mobile 中创建 CSS3 2D 动画。

```html
LISTING 8.4 QM2DAnimationGrad4Reflect1.html
<body>
  <div data-role="page">
    <div data-role="content">
      <div id="outer">
        <div id="radial3">Text3</div>
        <div id="radial2">Text2</div>
        <div id="radial4">Text4</div>
        <div id="radial1">Text1</div>
      </div>
    </div>
  </div>
</body>
```

Listing 8.4 非常直截易懂：jQuery 代码包含了四个 `div` 元素，这些元素在关联的样式表中有相应的 CSS 选择器。这四个 CSS 选择器定义了径向渐变（在 CD 的附带样式表中定义），它们与 第 2 章 中的 CSS3 示例非常。（如果你需要复习，请阅读相关章节）。需要注意的关键点是，尽管代码示例中的视觉效果并不是新的，但这段代码演示了你如何轻松地将 jQuery 代码与 CSS3 2D/3D 图形和动画效果相结合。

![image](img/fig8.7.jpg) ***图 8.7*** iPad 上的 CSS3 2D 效果。Figure 8.7 在 iPad 上横屏模式渲染 `QM2DAnimationGrad4Reflect1.html`。

![image](img/fig8.8.jpg) ***图 8.8*** 带有 Android 的 Asus 平板上的 CSS3 3D 效果。CD 中的 HTML5 Web 页面 `QM3DRotate3GradOpacity4Reflect1.html` 创建 CSS3D 动画效果。Figure 8.8 在带有 Android 的 Asus 平板上横屏模式显示 `QM3DRotate3GradOpacity4Reflect1.html`。

CD 中的 HTML5 Web 页面 `QMSS3AnimTap.html` 展示了如何检测用户点击事件，然后创建 CSS3D 动画效果。Figure 8.9 显示了在带有 Android 的 Asus 平板浏览器中横屏模式启动该 Web 页面的结果。

![image](img/fig8.9.jpg) ***图 8.9*** 带有 Android 的 Asus 平板上的 CSS3D 点击动画。

在本章前面，你已经学习了 jQuery Mobile 鼠标事件。CD 中的 Web 页面 `QMSetchSolidDOM1.html` 展示了如何捕获用户手势来动态创建并将新的 `div` 元素追加到 `id` 属性值为 `content` 的 `div` 元素中，创建一个“涂鸦”程序。

```javascript
LISTING 8.5 QMSetchSolidDOM1.html
<body>
  <script>
    $("#page1").live('pageinit', (function(event,ui){
      var insertNode = false;
      var newNode;
      // mouse-down means insertNode:
      $("#content").bind('vmousedown', function() {
        console.log("start");
        insertNode = true;
      });
      // mouse-up means no insertNode:
      $("#content").bind('vmouseup', function() {
        console.log("stop");
        insertNode = false;
      });
      $("#content").bind('vmousemove', function(e) {
        // are users are moving their mouse?
        if(insertNode == true) {
          console.log("move");
          // create a rectangle at the current position
          newNode = $('<div>').css({
            'position':'absolute',
            'background-color':'#ff0000',
            'width':'8px',
            'height':'8px',
            top: e.pageY,
            left: e.pageX
          });
          //append the rectangle to the content <div>
          $("#content").append(newNode);
        }
      });
    });
  </script>
</body>
```

Listing 8.5 包含了 jQuery Mobile 代码，绑定了 `vmousedown`、`vmouseup` 和 `vmousemove` 虚拟事件。该代码使用前两个虚拟鼠标事件来判断 `vmousemove` 事件是否伴随着 `vmousedown` 事件；如果后者为真，则会在程序化在用户鼠当前位置创建一个新的 HTML `<div>` 元素，并将其插入 DOM 中。

Figure 8.10 显示了 MacBook 上 Chrome 浏览器横屏模式下的 `JQMSketchSolidDynamicDOM1.html`。

![image](img/fig8.10.jpg)

图 8.10：在 MacBook 的 Chrome 浏览器上的绘图效果。

![image](img/cd.jpg) 在之前的章节中，你已经学习了如何使用 CSS3 创建 HTML5 Web 页面来创建一个 3D 立方体，当用户将鼠标悬停在立方体的三个面中的任意一个上时，这些面会移动。CD 上的 HTML5 Web 页面 `JQM3DCube1.html` 演示了如何使用 CSS3 渲染一个 3D 立方体。

### LISTING 8.6 JQM3DCube1.html
```html
<<body>
    <div data-role="page" id="page1">
      <div data-role="header">
        <h3>Tap on the Cube Faces:</h3>
      </div>
      <div data-role="content">
        <div id="outer">
          <div id="top">Text1</div>
          <div id="left">Text2</div>
          <div id="right">Text3</div>
        </div>
      </div>
      <div data-role="footer"><h3>Footer</h3></div>
    </div>
    <script>
      $("#page1").live('pageinit', (function(event,ui){ }));
    </script>
</</body>
```

Listing 8.6 包含了 jQuery Mobile 代码，其中包含三个 HTML `<div>` 元素的定义，这些元素用作立方体左侧、顶部和右侧面的占位符，以及一段极短的 jQuery Mobile 代码片段，如下所示：

```javascript
<script>
  $("#page1").live('pageinit', (function(event,ui){ }));
</script>
```

此代码示例中所有的实际“动作”发生在 CSS3 样式表 `JQM3DCube1.css` 中，其部分内容在 Listing 8.7 中。

### LISTING 8.7 JQM3DCube1.css
```css
/* animation effects */
#right:hover {
  -webkit-transition: -webkit-transform 3.0s ease;
  transition: transform 3.0s ease;
  -webkit-transform : scale(1.2) skew(-10deg, -30deg) rotate(-45deg);
  transform : scale(1.2) skew(-10deg, -30deg) rotate(-45deg);
}
#left:hover {
  -webkit-transition: -webkit-transform 2.0s ease;
  transition: transform 2.0s ease;
  -webkit-transform : scale(0.8) skew(-10deg, -30deg) rotate(-45deg);
  transform : scale(0.8) skew(-10deg, -30deg) rotate(-45deg);
}
#top:hover {
  -webkit-transition: -webkit-transform 2.0s ease;
  transition: transform 2.0s ease;
  -webkit-transform : scale(0.5) skew(-20deg, -30deg) rotate(45deg);
  transform : scale(0.5) skew(-20deg, -30deg) rotate(45deg);
}
// details omitted for brevity
```

Listing 8.7 中的 CSS3 选择器取自 第 2 章 中的一个代码示例，该示例也演示了如何使用 CSS3 选择器渲染立方体，你可以回顾该代码示例的详细细节。在这个示例中，每当用户点击或悬停在 3D 立方体的其中一个面上时，CSS3 选择器就会应用各种 3D 动画效果。

Figure 8.11 显示了带有 Android ICS 的 Asus Prime 平板上横屏模式下的 `JQM3DCube1.html`。

![image](img/fig8.11.jpg)

图 8.11：带有 Android ICS 的 Asus Prime 平板上的 jQuery Mobile 和 CSS3。

## CD 额外代码示例

CD 包含了其他几个使用类似 jQuery Mobile 技术的代码示例。你可以将这些技术作为“构建块”，可能还可以结合你自己的技术，来创建更复杂的视觉效果。

![image](img/cd.jpg) 代码示例主要是为了趣味，你可以通过动态修改额外的 CSS 属性来实验，并创建其他有趣的效果。

你可以通过多种方式在 jQuery Mobile 应用中创建翻页效果，在本节中，你将看到如何使用 jQuery 插件 `Turn.js`，其主页地址如下：

*[`www.turnjs.com`](http://www.turnjs.com)*

此代码示例包含了许多处理 jQuery Mobile 虚拟事件以及用户手势和键盘事件的示例。由于空间限制，我们无法讨论该代码示例的所有细节，但非常值得花时间仔细阅读代码以学习有用的技术。

![image](img/cd.jpg) CD 上的 HTML5 Web 页面 `JQMPageTurn1.html` 展示了如何使用 `Turn.js` 在 jQuery Mobile 应用中模拟翻页效果。

## jQuery 加速度计数值](#toc.html_toc-h1-0083)

![image](img/cd.jpg) CD 上的 HTML5 Web 页面 `JQMAccelerometer1.html` 展示了设备在任何方向发生加速时如何显示加速度值。

## 总结

本章介绍了 jQuery Mobile 中的动画效果，并查看了演示各种效果的代码示例。你学习了如何在 jQuery Mobile 中实现以下功能：

*   点击和滑动事件
*   滚动事件
*   识别竖屏还是横屏
*   淡入淡出动画效果
*   滑动动画效果
*   过渡效果
*   使用 CSS3 进行动画
*   虚拟鼠标事件

# 第 9 章 (#toc.html_toc-9)

## HTML5 CANVAS 简介](#toc.html_toc-9)

本章概述了 HTML5 Canvas，这是一种允许你编写直接在 Web 页面部分绘制图形的程序的技术。HTML5 Canvas 支持多种 API 来渲染 2D 形状以及各种图形效果。虽然网上有很多关于 Canvas 和 CSS3 的教程（你可以通过快速搜索确认），但很少有教程同时提供 HTML5 Canvas 和 CSS3 效果的代码示例。

还有一点需要记住：`HTML5 Canvas` 对 `jQuery` 或 `jQuery Mobile` 没有任何形式的“依赖”。如果有必要，你可以创建包含 `HTML5 Canvas` 的混合 HTML5 移动应用，可以结合工具包（如 `PhoneGap`），也可以不需要工具包。

## 什么是 HTML5 Canvas？

几年前，Canvas 在 OS X 中作为一种组件工具包出现。在 Canvas 在 `Safari` 浏览器中可用后，它成为了 Web 的一种规范。现在，它通常被称为 `HTML5 Canvas`。

`HTML5 Canvas` 和 `SVG` 都允许你通过 `JavaScript` 在浏览器中编程渲染图形。然而，`HTML5 Canvas` 使用的是“立即模式”（immediate mode），这是一种写完即忘的渲染方法。因此，如果你想在 `HTML5 Canvas` 中编写一个绘画程序，并且想提供“撤销”功能，那么你必须通过程序跟踪用户在屏幕上绘制的所有内容。另一方面，`SVG` 使用的是“保留模式”（retained mode），它涉及一个 `DOM`（文档对象模型）结构，用于跟踪渲染对象以及它们之间的关系。

如果你打算编写大量使用图形效果的 HTML Web 页面，你可能需要理解 `HTML5 Canvas` 和 `SVG` 在性能方面的差异。你可以自由地仅使用其中一种技术，也可以创建包含 `HTML5 Canvas`、`SVG` 和 `CSS3` 混合的 HTML Web 页面。性能相关的信息可以帮助你决定如何编写你的 HTML Web 页面。

虽然本章没有深入探讨上述观点，但你可以在这里找到关于 `HTML5 Canvas` 某些特性/优势的良好概述：

[`thinkvitamin.com/code/how-to-draw-with-html-5-canvas/`](http://thinkvitamin.com/code/how-to-draw-with-html-5-canvas/)

顺便一下，如果你在 `Internet Explorer 8` 中需要 `HTML5 Canvas` 支持，可以使用 `ExplorerCanvas`，这是一个开源项目，可以在这里：

[`code.google.com/p/explorercanvas/`](http://code.google.com/p/explorercanvas/)

你只需要在 HTML Web 页面中包含以下代码段，即可使用上述代码项目：

```
<!-- [if IE lt 8]><script src="excanvas.js"></script><![endif]-->
```

## HTML5 Canvas 与 SVG

一个需要考虑的点是何时使用 `HTML5 Canvas` 而不是 `SVG` 等技术更具优势。以下简短列表包含了你在进行此类分析时需要考虑的一些特性：

*   原生支持与插件浏览器支持
*   不同浏览器对 `SVG` 的支持程度
*   动画支持
*   对过滤器的支持（仅限 SVG）
*   对类 HTML 组件的内置支持
*   第三方支持

大多数现代浏览器都对 `SVG` 提供不同程度的内置支持，Adobe 的 `SVG` 查看器可以与微软的 `Internet Explorer` 配合使用。如果你需要基于过滤器的视觉效果，那么 `SVG` 提供了非常丰富（可能是最好的）的功能。如果你需要对 HTML 控件的内置支持，像 `Wijmo` 等框架可能是你需求的良好解决方案。另一个需要考虑的点是 Adobe 不再支持它的 `SVG` 查看器了。这是一个重大的决定，因为 Adobe 的 `SVG` 查看器多年来一直一直是 SVG 查看器的事实上的标准。尽管 `Firefox` 和 `Opera` 在支持 `SVG` 方面取得了显著进展，并且两者都在增强对 `SVG` 的支持，但它们仍然缺乏 Adobe `SVG` 查看器的功能支持。因此，你需要权衡最重要的因素，以做出符合你项目需求的决策。

有一篇包含示例和图表、比较 `HTML5 Canvas` 和 `SVG` 使用的优秀文章，可以在这里：

[`blogs.msdn.com/b/ie/archive/2011/04/22/thoughts-on-when-to-use-canvas-and-svg.aspx`](http://blogs.msdn.com/b/ie/archive/2011/04/22/thoughts-on-when-to-use-canvas-and-svg.aspx)

## HTML5 Canvas 坐标系

回想你高中的时光，那时你学过笛卡尔坐标系通过一对数字（通常写为 (x,y)）识别欧几里得平面上的任意点。第一个数字代表水平值，第二个数字代表垂直值。水平轴标记为 `x-axis`，`x-axis` 上的正值位于垂直轴的右侧（即向右）。垂直轴标记为 `y-axis`，`y-axis` 上的正值位于水平轴上方。原点是 `x-axis` 和 `y-axis` 的交点。

`HTML5 Canvas` 坐标系中的情况几乎相同。`x-axis` 是水平的，正方向向右。`y-axis` 是垂直的，但正方向向下，这与典型数学教科书中大多数图的方向相反。在 `HTML5 Canvas` 坐标系中，原点是屏幕的左上角（而不是左下角），测量单位是像素。当本书出版时，最大的可见显示器为 2880×1800，无疑未来会有更大的显示器。

![image](img/fig9.1.jpg)

***图 9.1***在 HTML5 Canvas 中渲染的四个点。

作为一个简单的说明，[图 9.1] 显示了 HTML `<canvas>` 元素中的四个点。

如果你从原点（屏幕的左上角）开始向右移动 50 像素，然后向下移动 50 像素，你将到达 [图 9.1] 中的左上点。接下来，如果你从原点开始向右移动 200 像素并向下移动 50 像素，你将到达 [Listing 9.1] 中的右上点。同样，第二“行”中的两个点坐标为 (50,100) 和 (200,100)。注意，第一行的两个点的 y 坐标值相同，这是合理的，因为它们距离 Web 页面顶部的距离相同；第二行的两个点也是如此。同样，左侧“列”的两个点具有相同的 x 坐标，因为它们距离 Web 页面左侧的距离相同。

现在你已经理解了 HTML5 Canvas 坐标系，让我们来看看 [Listing 9.1] 内容，它显示了一个最小的 HTML5 Web 页面，准备好渲染基于 HTML5 Canvas 的图形。书书中每个基于 Canvas 的代码示例都使用 [Listing 9.1] 中显示的代码（或某些变体）。注意，如果你在浏览器会话中启动此代码，你将只看到一个空白屏幕。

***Listing 9.1 Canvas1.html***
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Canvas Drawing Rectangles</title>
  <script><!--
    window.addEventListener('load', function () {
      // Get the canvas element
      var elem = document.getElementById('myCanvas');
      if (!elem || !elem.getContext) {
        return;
      }
      // Get the canvas 2d context
      var context = elem.getContext('2d');
      if (!context) {
        return;
      }
      // Insert your custom Canvas code here
    });
  // --></script>
</head>
<body>
  <canvas id="myCanvas" width="300" height="300">
    No support for Canvas.
  </canvas>
</body>
</html>
```

[Listing 9.1] 包含一个 HTML `<head>` 元素，用于检查 Web 页面 HTML `<body>` 元素内部是否存在 HTML `<canvas>` 元素，然后从 HTML `<canvas>` 元素获取 2D 上下文。如果你跳过 [Listing 9.1] 中的各种条件语句，有两行代码使我们获取变量 `context` 的引用，该变量代表一个可绘制表面：

```javascript
var elem = document.getElementById('myCanvas');
var context = elem.getContext('2d');
```

如果你将示例 9.1 运行在不支持 HTML5 Canvas 的浏览器中，屏幕将显示文本消息“No support for Canvas.（不支持 Canvas）”。

由于在加载事件期间执行了一个匿名 JavaScript 函数，每当你启动该网页时，都会执行以下代码段：

```html
<script><!--
window.addEventListener('load', function () {
  // 在此处执行某些操作
});
// --></script>
```

现在你已经了解了渲染基于 Canvas 的 2D 形状的底层代码，可以专注于实际绘制某些 2D 形状的代码了，从下一节的示例开始。

# 线段、矩形、圆形和阴影效果 (#toc.html_toc-h1-0086)

本节包含各种代码示例，用于阐述如何在 HTML5 Canvas 中渲染 2D 形状。本节引入了许多概念，因此在深入研究代码示例之前，让我们先看看本节中用到的一些 HTML5 Canvas API。第 2 章 包含一个描述指定颜色多种方式的章节，该章节的内容与本章中的代码示例相关（如果你需要，现在可以快速回顾其内容）。

HTML5 Canvas 提供了用于渲�矩形的 `fillRect()` 方法，它需要四个参数：矩形的左上角顶点（由其 `x` 坐坐标和 `y` 坐标定义）、矩形的宽度以及目标矩形的高度。`Canvas fill()` API 如下：

```javascript
context.fillRect(x, y, width, height);
```

HTML5 Canvas 允许你通过指定线段两个端点的 `(x,y)` 坐标来渲染线段。本节代码示例中用到的两个新 API 是 `moveTo()` 和 `lineTo()`，它们的形式如下：

```javascript
context.moveTo(x1, y1);
context.lineTo(x2, y2);
```

前面的代码段代表两个端点由点 `(x1, y1)` 和 `(x2, y2)` 指定的段。请注意，你也可以使用以下代码段渲染相同的线段：

```javascript
context.moveTo(x2, y2);
context.lineTo(x1, y1);
```

阴影效果提供了比非阴影效果更丰富的视觉体验，是对者的改进。你通过为三个与阴影相关的属性赋值来创建阴影效果，这些属性控制底层阴影的大小以及阴影的“模糊”程度，如下所示：

```javascript
context.shadowOffsetX = shadowX;
context.shadowOffsetY = shadowY;
context.shadowBlur = 4;
```

你还可以为 `shadowColor`（它是绘图上下文的属性）分配 `(R,G,B)` 或 `(R,G,B,A)` 值，如下所示：

```javascript
context.shadowColor = "rgba(0,0,64,1.0)";
```

示例 9.2 中的 HTML5 网页 `RandRectanglesShadow.html`（为了起见省略了代码部分）使用了这种技术来渲染一组带有阴影效果的随机生成矩形。

**示例 9.2 RandRectanglesShadow.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Canvas Random Rectangles With Shadow Effects</title>
  <link href="CSS3Background2.css" rel="stylesheet" type="text/css">
  <script><!--
    window.addEventListener('load', function() {
      redrawCanvas = function() {
        // 在绘制新一组矩形之前清除画布
        context.clearRect(0, 0, elem.width, elem.height);
        for(var r=0; r<rectCount; r++) {
          basePointX = canWidth*Math.random();
          basePointY = canHeight*Math.random();
          // 根据奇偶数点击计数使用不同的 (R,G,B,A)
          // 值交替阴影效果
          if(clickCount % 2 == 0) {
            context.shadowColor = "rgba(0,0,64,1.0)";
          } else {
            context.shadowColor = "rgba(64,0,0,1.0)";
          }
          // 指定底层阴影效果的大小以及
          // "模糊"程度的代码
          context.shadowOffsetX = shadowX;
          context.shadowOffsetY = shadowY;
          context.shadowBlur = 4;
          context.lineWidth = 1;
          // 渲染一个彩色矩形
          colorIndex = Math.floor(basePointX)%fillStyles.length;
          context.fillStyle = fillStyles[colorIndex];
          context.fillRect(basePointX, basePointY, rectWidth, rectHeight);
          ++clickCount;
        }
      }
      // 渲染一组随机矩形
      redrawCanvas();
    });
  // --></script>
</head>
<body>
  <canvas id="myCanvas" width="800" height="350">No support for Canvas</canvas>
</body>
</html>
```

## HTML5 Canvas 线性渐变

HTML5 Canvas 提供了两种主要的颜色渐变（类似于 SVG 和 CSS3）：*线性渐变*和*径向渐变*。

线性颜色渐变可以进一步细分为三种：水平线性渐变、垂直线性渐变和对角线线性渐变。因此，HTML5 Canvas 提供的颜色渐变使你能够创建愉悦的视觉效果。

线性渐变通过 `ColorStop` 元素定义，每个元素包含一个小数（在 0 到 1 之间）和一个表示颜色的十六进制值。例如，如果你定义一个初始颜色为 `#FF0000`（红色的十六进制值）且结束颜色为 `#000000`（黑色的十六进制值）的线性渐变，那么生成的颜色渐变将（线性地）从红色过渡到黑色。线性渐变让你能够创建生动且有趣的颜色组合，它们有三种形式：水平、垂直和对角线。注意，书中“线性渐变”和“线性颜色渐变”是互换使用的。

### 水平、垂直和对角线线性渐变

正如你在本章引言中所学到的，HTML5 Canvas 支持 `createLinearGradient()` 方法，你可以用它通过编程方式创建线性渐变。其语法如下：

```
context.createLinearGradient(startX, startY, endX, endY);
```

![image](img/cd.jpg) [Listing 9.4] 中的 HTML5 页面 `LGradRectangles1.html` 展示了如何渲染一组具有水平、垂直和对角线线性渐变的矩形。[Listing 9.3] 引用了 CSS3 样式 `HoverAnimation1.css`，该样式每当用户用鼠标悬停在该 HTML5 `<canvas>` 元素上时，会将基于 CSS3 关键帧的 2D 动画应用到该元素。[Listing 9.4] 也引用了 CSS3 样式 `HoverAnimation2.css`，其工作方式类似。然而，该样式表对 [Listing 9.3] 中的第二个 HTML5 `<canvas>` 元素应用了 CSS3 3D 动画效果。由于这些 CSS 样式表中的动画技术已在第 2 章讨论过，我们将在本章中省略它们，但完整的源代码可以在 CD 上找到。

### LISTING 9.3 LGradRectangles1.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Canvas Linear Gradient Rectangles</title>
  <link href="HoverAnimation1.css" rel="stylesheet" type="text/css">
  <link href="HoverAnimation2.css" rel="stylesheet" type="text/css">
  <script>
    window.addEventListener('load', function () {
      redrawCanvas = function() {
        // 在绘制新一组矩形之前清空画布
        //context.clearRect(0, 0, elem.width, elem.height);
        //context2.clearRect(0, 0, elem.width, elem.height);
        // 左上角矩形：水平线性渐变
        currentX = basePointX;
        currentY = basePointY;
        gradient1 = context.createLinearGradient(
                                            currentX,
                                            currentY,
                                            currentX+rectWidth,
                                            currentY+0*rectHeight);
        gradient1.addColorStop(0, '#f00');
        gradient1.addColorStop(1, '#00f');
        context.fillStyle = gradient1;
        context.fillRect(currentX, currentY,
                         rectWidth, rectHeight);
        // 右上矩形：垂直线性渐变
        // 为了简洁省略了相似代码
        // 在第二个 <canvas> 元素中
        // 渲染左下方的矩形
        // 左下角矩形：对角线线性渐变
        // 为了简洁省略了相似代码
        // 右下角矩形：对角线线性渐变
        // 为了简洁省略了相似代码
        ++clickCount;
        basePointX += 4;
        basePointY += 2;
      } // 线性渐变
      redrawCanvas();
    }, false);
  </script>
</head>
<body>
  <div>
    <canvas id="myCanvas" width="600" height="250"></canvas>
  </div>
  <div>
    <canvas id="myCanvas2" width="600" height="250"></canvas>
  </div>
  <div>
    <input type="button" onclick="redrawCanvas();" value="Redraw Rectangles" />
  </div>
</body>
</html>
```

[Listing 9.3] 渲染线性渐变。通过 `addColorStop()` 方法的三次或四次调用，线性渐变可以实现不同的颜色组合。尝试不同的颜色停止值，看看它们如何影响渲染的矩形。

![image](img/fig9.3)

***图 9.3*** Nexus 7 线性渐变

### 径向渐变

径向颜色渐变是第二种 HTML5 颜色渐变。你可以通过 `createRadialGradient()` 方法定义径向渐变，使用 `addColorStop()` 方法添加颜色值。其语法（不包含 `addColorStop()` 方法）如下：

```
context.createRadialGradient(startCenterX, startCenterY, startRadius, endCenterX, endRadius);
```

*径向*颜色渐变可以与向池塘中丢石头产生的波纹效应相比，每个“波纹”都有按渐变变化的颜色。每个波纹对应一个颜色停止元素。例如，如果你定义一个起始颜色为 `#FF0000`（红色）且结束颜色为 `#000000`（黑色）的径向渐变，那么生成的颜色渐变将（径向地）从红色过渡到黑色。径向渐变也可以包含多个起始/停止组合。需要注意的是，径向渐变按*线性*方式改变颜色，但渲的颜色是以组扩展圆形绘制的。注意，“径向渐变”和“径向颜色渐变”在书中是互换使用的。

![image](img/cd.jpg) HTML5 页面 `RGradRectangles1.html` 使用线性和径向渐变在 HTML5 `<canvas>` 元素中渲染线段、矩形和圆形，可以在 CD 上找到。

```javascript
gradient1 = context.createRadialGradient(
                                            currentX,
                                            currentY,
                                            0,
```



currentX+rectWidth,

currentY+rectHeight);

gradient1.addColorStop(0, '#f00');

gradient1.addColorStop(1, '#00f');

context.fillStyle = gradient1;

context.fillRect(currentX, currentY,

                 rectWidth, rectHeight);

```

`RGradRectangles1.html` 与 Listing 9.3 类似，但使用的是径向渐变（而不是线性渐变），通过调用 `addColorStop()` 方法向径向渐变添加四个“颜色停止值”。

![image](img/fig9.4.jpg)

***图 9.4*** iPad3 上的径向渐变矩形

图 9.4 显示了在 iPad3 上横屏模式下，基于 `RGradRectangles1.html` 的一组带有径向渐变的矩形。

## HTML5 Canvas 变换与状态保存

HTML5 Canvas 允许你通过以下方法对 2D 形状和文本字符串进行旋转、缩放、倾斜或平移（水平和/或垂直位移）：

- `rotate(x,y)`
- `scale(x,y)`
- `transform(x1,y1,x2,y2,x3,y3)`
- `translate(x,y)`

需要注意的是，你必须在 HTML5 Web 页面中实际渲染图形形状*之前*，指定你想要应用的变换（以及设置属性值）。

以下代码段说明了你可以在上述 Canvas 方法中使用的示例值，其中 `context` 是引用 HTML5 `<canvas>` 元素上下文的 JavaScript 变量：

```javascript

context.rotate(30*Math.PI/180);

context.scale(0.8, 0.4);

context.translate(100, 200);

context.transform(1, 0, 0.5, 1, 0, 0);

```

上述代码块中的 `rotate()` 方法引用了 JavaScript 常量 `Math.PI`，其值代表 PI 弧度。如果你忘记了，PI 弧度等于 180 度，因此 `2*PI` 弧度是 360 度，`PI/2` 弧度是 90 度。因此，`Math.PI/6` 弧度（或 `30*Math.PI/180`）等于 30 度。你不需要了解更多弧度的知识，但如果你想阅读提供额外示例教程，可以自行搜索。

HTML5 Canvas 中的两个额外 API 是 `save()` 和 `restore()`，它们允许你保存画布当前的状态，进行更改，然后恢复画布的原始状态。`save()` 方法将当前状态“推入”栈中，而 `restore()` 方法从栈中“弹出”最近一次的状态。

你可以在应用本节列出的任何变换之后，也可以在指定阴影相关属性（等）的值之后，保存（并稍后恢复）画布状态。你可以在画布状态上多次调用 `save()` 和 `restore()` 方法，这使得这两个方法对于游戏相关的 Web 页面非常有用。我们不会在本章的任何代码示例中使用这两个方法，但你可以通过网络搜索阅读教程并找到代码示例。

![image](img/cd.jpg) CD 中的 HTML5 Web 页面 `JQMCanvasTransforms1.html` 展示了如何将四个 HTML5 Canvas 变换应用于文本字符串。

## jCanvas：一个用于 HTML5 Canvas 的 jQuery 插件

jCanvas jQuery 插件允许你使用 jQuery 语法来指定在 HTML5 `<canvas>` 元素中渲染的 2D 形状。它的主页在这里：

*[http://calebevans.me/projects/jcanvas/]*

CD 中的 HTML5 Web 页面 `JCanvasSamples1.html` 展示了如何使用 `jCanvas` 渲染几个 2D 形状。

![image](img/fig9.5.jpg)

***图 9.5*** iPad3 上的 jQuery jCanvas 插件。

图 9.5 显示了在 iPad3 上横屏模式渲染 `JCanvasSamples1.html` 的结果。

你也可以将 jQuery Mobile 与 HTML5 Canvas 使用，如下一节的代码示例所示。

## 结合 CSS3 和 jQuery Mobile 的 HTML5 Canvas

到现在，我们希望你已经理解如何在 HTML5 Canvas 中渲染 2D 形状。本节包含一个代码示例，向你展示如何结合 jQuery Mobile、HTML5 Canvas 以及当用户点击此网页中 HTML5 `<canvas>` 元素内部时动态创建 HTML `<div>` 元素。

记住，尽管图形效果并不一定是你需要的，但此代码示例确实说明了如何在 jQuery Mobile 中处理元素的动态创建以及点击事件（其处理方式与 jQuery 中的点击事件不同）。

列表 9.4 显示了 HTML5 Web 页面 `JQMCanvas1.html` 的内容，列表 9.5 显示了 CSS 样式表 `JQMCanvas1.css`，其 CSS3 选择器匹配 HTML5 Web 页面 `JQMCanvas1.html` 中的元素。

***列表 9.4 JQMCanvas1.html***

```html

<!DOCTYPE html>

<html lang="en">

  <head>

    <meta charset="utf-8">

    <title>JQueryMobile and Canvas Graphics</title>

    <link rel="stylesheet" href="JQMCanvas1.css" />

    <link rel="stylesheet"

      href="http://code.jquery.com/mobile/1.1.0/

                              jquery.mobile-1.1.0.min.css" />

    <script src="http://code.jquery.com/jquery-2.0.0b1.js">

    </script>

    <script

      src="http://code.jquery.com/jquery-migrate-1.1.0.js">

    </script>

    <script

src="http://code.jquery.com/mobile/1.1.0/

                              jquery.mobile-1.1.0.min.js">

    </script>

    <script>

      var tapCount = 0;

      var xCoord = 0, yCoord = 0;

      var rectWidth = 20, rectHeight = 20;

      var rectColors = Array('#ff0', '#0f', '#0f');

      var elem, context;

      var gradient1 = '-webkit-gradient(radial, 25%, 50%, 20%, from(red), color-stop(0.05, orange), color-stop(0.4, yellow), color-stop(0.6, red), color-stop(0.9, blue), to(#fff))

      var gradient2 = '-webkit-gradient(radial, 25%, 50%, 20%, from(blue), color-stop(0.05, orange), color-stop(0.4, red), color-stop(0.6, black), color-stop(0.9, blue), to(#f0))

      var gradient3 = '-webkit-gradient(radial, 25%, 50%, 20%, from(blue), color-stop(0.05, yellow), color-stop(0.4, green), color-stop(0.6, red), color-stop(0.9, blue), to(#fff))

      var gradient4 = '-webkit-gradient(radial, 25%, 50%, 20%, from(blue), color-stop(0.05, yellow), color-stop(0.2, green), color-stop(0.6, blue), color-stop(0.8, red), to(#fff))

      var currentBG;

      $("#page1").live('pageinit', (function(event){

        // 获取画布元素

        elem = document.getElementById('MyCanvas');

        if (!elem || !elem.getContext) {

          return;

        }

        // 获取画布 2d 环境

        context = elem.getContext('2d');

        if (!context) {

          return;

        }

        // 用户点击了 MyCanvas...

        $("#MyCanvas").live('vmousedown',function(event) {

          xCoord = 0.40*(event.clientX)*window.devicePixelRatio;

          yCoord = 0.40*(event.clientY)*window.devicePixelRatio;

          context.fillStyle = rectColors[++tapCount%rectColors.length];

          context.fillRect(xCoord, yCoord, rectWidth, rectHeight);

          $("#MyCanvas").hide("slow");

        });

        // 这让 MyCanvas 可见

        $("#tapInside").live('tap',function(event) {

          $("#MyCanvas").show("slow");

        });

        $("#CanvasParent").live('vmousedown',function(event) {

          if(tapCount % 4 == 0) {

            currentBG = gradient1;

          } else if(tapCount % 4 == 1) {

            currentBG = gradient2;

          } else if(tapCount % 4 == 2) {

            currentBG = gradient3;

          } else {

            currentBG = gradient4;

          }

          newNode = $('<div').css({

            'position':'absolute',

            'background': currentBG,

            'width':rectWidth+'px',

            'height':rectHeight+'px',

            'top': event.clientY,

            'left': event.clientX

          });

          //将新矩形附加到 CanvasParent

          $("#CanvasParent").append(newNode);

        }

      })

    );

    </script>

    <style>

      #tapInside { color: #f00; }

      #MyCanvas  { width: 80%; height: 30%; }

    </style>

  </head>

  </body>

```



<div id="tapInside">
  <p>点击红色矩形内部隐藏，点击此处显示：</p>
</</div>
<div id="CanvasParent" name="CanvasParent">
  <canvas name="MyCanvas" id="MyCanvas" style="background:#f00;width=80%;height=200px"></canvas>
  <div id="outer">
    <div id="radial3">Text3</div>
    <div id="radial2">Text2</div>
    <div id="radial4">Text4</div>
    <div id="radial1">Text1</div>
  </div>
  <!-- jQuery toggle-handling code -->
  <script>
    $(document).ready(function() {
      $("#outer").toggle(function(){
        $("#radial1").show("slow");
        $("#radial2").hide("slow");
        $("#radial3").hide("slow");
        $("#radial4").show("slow");
      },function(){
        $("#radial1").hide("slow");
        $("#radial2").show("slow");
        $("#radial3").show("slow");
        $("#radial4").hide("slow");
      });
    });
  </script>
</</div>
<div data-role="footer">
  <h3>JQuery Mobile 与 Canvas 图形</h3>
</div>
</div>
</body>

请注意 Listing 9.4.live('vmousedown',function(event) {
  xCoord = 0.40*(event.clientX)*window.devicePixelRatio;
  yCoord = 0.40*(event.clientY)*window.devicePixelRatio;
  context.fillStyle = rectColors[++tapCount%rectColors.length];
  context.fillRect(xCoord, yCoord, rectWidth, rectHeight);
  $("#MyCanvas").hide("slow");
});
```

请记住，你必须使用 `vmousedown` 事件，因为 jQuery Mobile 中的点击事件不会为你提供点击位置的坐标。你还需要在计算点击位置时使用 `window.devicePixelRatio` 的值。

当用户点击 id 为 `tapInside` 的 `<canvas>` 元素时，隐藏的 `<canvas>` 元素将再次显示，同时带有之前通过 `fillRect()` 方法渲染的所有矩形。

当用户点击 id 为 `CanvasParent` 的 `<canvas>` 元素时，代码首先使用条件逻辑来确定选择哪个径向渐变并将其赋值给 JavaScript 变量 `currentBG`。

接下来，会在点击事件的位置动态创建一个新的 HTML `<div>` 元素并将其追加到 `CanvasParent` 元素中，如下：

```
newNode = $('<div>').css({'position':'absolute',
  'background': currentBG,
  'width':'35px',
  'height':'35px',
  top: event.pageY,
```

`newNode = $('<div>').css({'position':'absolute', 'background': currentBG, 'width':'35px', 'height':'35px', top: event.pageY});`

`$("#CanvasParent").append(newNode);`

注意，在前面的代码中 `position` 被设置为 `absolute`，这意味着这个 `<div>` 元素将会被保留。最后，当用户点击任何一个 `<div>` 元素时，代码将使它们消失。

![image](img/cd.jpg) HTML5 页面 `LRGradQCBezier1.html` 展示了如何渲染带有线性渐变着色的二次贝塞尔曲线以及带有径向渐变的三次贝塞尔曲线。光盘中提供了两个 CSS 样式表 `CSS3Background4.css` 和 `HoverAnimation1.css`。

HTML5 页面 `LRGradQCBezier1.html` 中定义的三次贝塞尔曲线是根据几个计算点使用六个颜色停止点通过径向渐变渲染的，如下：

```
context.bezierCurveTo(
    currentX+3*multiplier*rectWidth,
    currentY+2*multiplier*rectHeight,
    currentX+2*multiplier*rectWidth,
    currentY-multiplier*rectHeight,
    currentX+100, currentY+300);
```

尝试贝塞尔曲线中控制点的不同值，你可能会发现创建悦目视觉效果的其他方法。列表 9.6 的下一部分使用五个颜色停止点的线性渐变渲染了二次贝塞尔曲线。

请注意，每当用户点击“重绘（redraw）”按钮时，都会根据用户每次点击“重绘”按钮时增加的变量 `clickCount` 的值绘制另一条三次和二次贝塞尔曲线。新曲线叠加在之前的曲线上，从而营造出良好的视觉效果。然而，如果你想在渲染另一对贝塞尔曲线之前刷新 HTML5 `<canvas>` 元素，只需取消下方代码段中第二行的注释：

```
// clear the canvas before drawing new set of rectangles
//context.clearRect(0, 0, elem.width, elem.height);
```

![image](img/fig9.7.jpg)

**图 9.7** iPad3 渐变贝塞尔曲线。

图 9.7 在 iPad3 的横屏模式下渲染了 `LRGradQCBezier1.html` 中定义的二次和三次贝塞尔曲线。

HTML5 Canvas 支持渲染 JPG 文件，你也可以对 HTML5 `<canvas>` 元素应用 CSS 选择器。光盘包含 HTML5 Web 页面 `Image1.html` 和 `Image1.css`，其选择器匹配 HTML5 `<canvas>` 元素。

顺便提一下，HTML5 Canvas 还支持 `clip()` 方法，允许你以各种方式“裁剪” JPG 文件。此外，你还可以执行合成效果，甚至操作 JPG 文件的单个像素。可以在互联网上搜索描述这些效果技术细节的文章。

HTML5 Canvas 提供了 `createPattern(image, type)` 方法，允许你根据模式类型渲染一组图像，其取值可以是 `repeat`、`repeat-x`、`repeat-y` 和 `no-repeat`。语的示例（以及使用方法）如下：

```
var pattern = canvas.createPattern(img,"repeat");
canvas.fillStyle = pattern;
canvas.fillRect(0,0,500,300);
```

![image](img/cd.jpg) 光盘上的 HTML5 Web 页面 `RepeatingImage1.html` 阐述了如何在 HTML5 `<canvas>` 元素上重复 JPG 图片。

图 9.8 在 MacBook 的 Chrome 浏览器上横屏模式显示了 `RepeatingImage1.html`。

![image](img/fig9.8.jpg)

**图 9.8** MacBook Chrome 浏览器上的重复 JPG。

### 其他 HTML5 Canvas 工具包 (#toc.html_toc-h1-0093)

有几个非常好的 JavaScript 工具包可以在 HTML5 Canvas 之上提供抽象层，包括 `Easel.js`、`Fabric.js` 和 `Paper.js`。

除了在这些工具包各自主页上提供的代码示例外，你可能喜欢以下开源项目的内容，它使用 `Easel.js` 创建图形代码示例：

http://code.google.com/p/easeljs-graphics

### 总结 (#toc.html_toc-h1-0094)

本章介�了 HTML5 Canvas，并展示了使用 HTML5 `<canvas>` 元素创建 2D 形状的示例。你还学习了如何将 HTML5 Canvas 与 jQuery 自定义代码结合，以便使用 Canvas 的 2D 形状操作 HTML5 Web 页面。特别是，你学习了如何在 HTML5 Canvas 中实现以下操作：

* 渲染线段、矩形和圆形

* 创建线性和径向渐变

* 创建贝塞尔曲线

* 显示 JPG 文件

* 使用 `jCanvas`（一个用于 jQuery 插件）

* 将 HTML5 Canvas 与 CSS3 结合

* 将 HTML5 Canvas 与 jQuery Mobile 结合

# 第 10 章 (#toc.html_toc-10)

### 使用 PHONEGAP 开发 HTML5 移动端应用 (#toc.html_toc-10)

本章向你展示了如何为 Android 和 iOS 创建基于 HTML5 的混合移动应用程序。章中的代码示例包含了 HTML5 以及 HTML5、CSS3 和 SVG 的各种组合。

正如你很快会发现的，基于 Android 的示例比基于 iOS 的示例要多。代码示例的移动平台选择纯粹出于风格考虑。然而，每个基于 Android 的代码示例都有对应的 iOS 版本，反之亦然。

本章的第一部分概述了如何使用“手动”方法而不是 PhoneGap 等工具包来开发移移动应用程序。该节的代码示例使用了你在之前章节中见过的代码，并向你展示了如何创建基于 Android 的移动应用程序。如果你心心勃勃，可以为所有示例创建 iOS 版本！

本章的第二部分包含了基于 Android 的示例，展示了如何将原生 Android 应用与 CSS3、SVG 和 HTML5 Canvas 结合。该节包含一个渲染支持鼠标的折线图示例，每当用户点击折线图下方的按钮时，其值就可以更新。请记住，代码示例后的讨论进展得很快，因为 HTML Web 页面包含简单的标记，CSS3 选择器包含你以前见过的代码，并且讨论了 SVG 形状。

本章的第三部分快速概述了 Apache Cordova（以前称为 PhoneGap），这是一种流行的跨平台移动应用开发工具包。2011 年，Adobe 收了创建 PhoneGap 的公司 Nitobi，不久后 Adobe 开源了 PhoneGap。该节解释了 PhoneGap 能做什么，以及你可以配合 PhoneGap 使用的一些工具包。你将学习如何创建一个基于 PhoneGap 的渲染 CSS3 动画效果的 Android 应用。你可以将此应用部署到支持 Android ICS 或更高版本的 Android 移动设备。

本章的最后部分讨论了如何使用 Xcode 的 PhoneGap 插件创建 iOS 混合移动应用。正如你在本章看到的，PhoneGap 允许你使用 HTML、CSS 和 JavaScript 创建移动应用。你可以将这些应用部署到多个平台，包括 Android、iOS、BlackBerry 和 Windows Mobile。你还可以创建结合 PhoneGap 和 Sencha Touch（另一个流行的框架）的移动应用。然而，由于空间限制，本章未讨论 Sencha Touch。

如果你不熟悉本章提到的任何移动平台，你仍然可以完成本章中的示例，因为它们由基于 HTML5 的代码组成。在移动平台上创建基于 HTML5 的移动应用的步骤顺序本质上独立于实际代码。

如果你对 Android 并不熟悉，可以阅读本书的附录，其中包含了本章代码示例中 Android 特有概念的简要概述。每当你遇到不清楚的 Android 概念时，都可以参考相应的章节。

本节的代码示例向你展示如何在 Android 应用程序中启动 HTML5 Web 页面（该页面还引用了 CSS3 样式表）。核心思想包含三个步骤：

1. 修改 Android `Activity` 类以实例化一个 Android `WebView` 类，以及一些与 JavaScript 相关的设置。

2. 引用 Android 项目 `assets/www` 子目录下的 HTML5 Web 页面。

3. 将 HTML5 Web 页面、CSS 样式表和 JavaScript 文件复制到 Android 项目的 `assets/www` 子目录中。

在步骤 3 中，你可能会创建一个分级目录集，其中包含相同类型（HTML、CSS 或 JavaScript）的文件，这与你在 Web 应用程序中组织文件的方式非常相似。

现在启动 Eclipse 并创建一个名为 `AndroidCSS3` 的 Android 项目。确保你选择的是 Android 3.1 或更高版本，这对于渲染基于 CSS3 的效果是必要的。

创建项目后，让我们来看包含此 Android 移动应用程序自定义代码的四个文件。Listing 10.1、10.2 和 10.3 分别显示了项目文件 `main.xml`、`AndroidCSS3.html` 和 `AndroidCSS3Activity.java` 的内容。

### 列表 10.1 main.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent">
  <WebView android:id="@+id/webview"
          android:layout_width="fill_parent"
          android:layout_height="fill_parent">
  </WebView>
</LinearLayout>
```

列表 10.1 指定了一个 `LinearLayout`，它包含一个 Android `WebView`，该 WebView 将占据移动设备的整个屏幕。这是我们想要看到的效果，因为 Android 默认浏览器是在 Android `WebView` 中渲染的。

### 列表 10.2 AndroidCSS3.html

```html
<!doctype html>
<head>
  <title>CSS 渐变示例</title>
  <link href="AndroidCSS3.css" rel="stylesheet">
</head>
<body>
  <div id="outer">
    <div id="radial1">Text1</div>
    <div id="radial2">Text2</div>
    <div id="radial3">Text3</div>
    <div id="radial4">Text4</div>
  </div>
</body>
</html>
``` （等待，已更正）

列表 10.2 是一个简单的 HTML Web 页面，它引用了 CSS 样式表 `AndroidCSS3.css`（在光盘上可用），以及一个 HTML `div` 元素（其 `id` 属性值为 `outer`），作为另外四个 HTML `div` 元素的“容器”。

![image](img/cd.jpg) CSS 样式表 `AndroidCSS3.css` 包含一个用于为 `id` 值为 `outer` 的 HTML `div` 元素设置样式的 CSS 选择器，随后是四个选择器器 `11``22`````` `radial4` 列表 10.2 中对应的 HTML `div` 元素。这些选择器的内容应该非常熟悉（你可以回顾前面的章节中关于 CSS3 渐变的材料），因此我们在本节中不再涵盖它们的内容。

### 列表 10.3: AndroidCSS3Activity.java

```java

package com.iquarkt.css3;

import android.app.Activity;

import android.os.Bundle;

import android.webkit.WebChromeClient;

import android.webkit.WebSettings;

import android.webkit.WebView;

import android.webkit.WebClient;

public class AndroidCSS3Activity extends Activity

{

    /** 当 activity 首次创建时调用。 */

    @Override

    public void onCreate(Bundle savedInstanceState)

    {   

      super.onCreate(savedInstanceState);

      setContentView(R.layout.main);

      // 获取声明的 WebView 持有器的引用

      WebView webview = (WebView) this.findViewById(R.id.webview);

      // 获取设置

      WebSettings webSettings = webview.getSettings();

      // 启用 JavaScript 用于交互

      webSettings.setJavaScriptEnabled(true);

      // 使缩放控件可见

      webSettings.setBuiltInZoomControls(true);

      // 允许触摸选择/取消选择数据系列

      webview.requestFocusFromTouch();

      // 设置客户端

      webview.setWebViewClient(new WebViewClient());

      webview.setWebChromeClient(new WebChromeClient());

      // 加载 URL

      webview.loadUrl("file:///android_asset/AndroidCSS3.html");

    }

}

```

![image](img/fig10.1.jpg) **图 10.1** 带有 Android ICS 的 Asus Prime 平板上基于 CSS3 的 3D 立体。

Listing 10.3 定义了一个扩展标准 Android `Activity` 类的 Java 类 `AndroidCSS3Activity`。该类包含 `onCreate()` 方法，该方法“指向”XML 文档 `main.xml`（在 Listing 10.2 中显示），以便我们可以通过 `R.id.webview` 获取其 `WebView` 子元素的引用（这是 Listing 10.2 中 `WebView` 元素的引用），所示：

```

WebView webview = (WebView) this.findViewById(R.id.webview);

```

接下来，`WebSettings` 类的 `webSettings` 实例允许我们设置各种属性，如 Listing 10.4 代码中的注释行所示。

最后一行代码加载了 HTML Web 页面 `AndroidCSS3.html`（位于 `assets/www` 子目录）的内容，所示：

```java

webview.loadUrl("file:///android_asset/AndroidCSS3.html");

```

Figure 10.1 显示了带有 Android ICS 的 Asus Prime 平板上基于 CSS3 的 Android 应用程序。

## SVG 与 Android 应用

本节的示例向你展示如何创建一个 Android 移动应用程序，用于渲染嵌入 HTML5 Web 页面中的 SVG 代码。现在启动 Eclipse 并创建一个名为 `AndroidSVG1` 的 Android 项目，确保选择的是 Android 3.1 或更高版本，这对于渲染 SVG 元素是必要的。

上一节的示例包含四个自定文件，而本节中的 Android/SVG 示例包含两个文件：Listing 10.4 中的 HTML 页面 `AndroidSVG1.html` 和光盘上提供的 Java 类 `AndroidSVG1Activity`。

![image](img/cd.jpg) **列表 10.4 AndroidSVG1.html**

```html

<!doctype html>

<html>

<head>

  <title>HTML5 SVG</title>

</head>

<body>

  <h1>HTML5 SVG</h1>

  <svg>

    <ellipse cx="300" cy="50" rx="80" ry="40" fill="red" stroke="black" stroke-width="3" />

    <line x1="100" y1="20" x2="300" y2="350" stroke="black" stroke-width="8" />

    <path d="M0,0 C200,150 400,300 20,250" fill="none" stroke="red" stroke-width="4" />

    <path d="M200,150 C0,0 400,300 20,250" fill="none" stroke="blue" stroke-width="12" />

  </svg>

</body>

</html>

```




图 10.2 显示了在运行 Android ICS 的 Asus Prime 平板上基于 SVG 的 Android 应用。

![image](img/fig10.2.jpg)

***图 10.2*** 在运行 Android ICS 的 Asus Prime 平板上基于 SVG 的 Android 应用。

# HTML5 Canvas 与 Android 应用(#toc.html_toc-h1-0097)

除了渲染基于 CSS3 的效果和 SVG 文档外，你可以在 Android 应用中渲染基于 Canvas 的 2D 形状。启动 Eclipse 并创建一个名为 `AndroidCanvas1` 的 Android 项目。确保你选择了 Android 3.1 或更高版本，这是渲染 SVG 元素必需的。

本节中的示例包含一个名为 `AndroidCanvas1.html` 的自定义文件，该文件显示在列表 10.5 中。

***列表 10.5 AndroidCanvas1.html***

```html

<!DOCTYPE html>

<html lang="en">

<head>

 <meta charset="utf-8" />

 <title>HTML5 Canvas Example</title>

<script>

 function draw() {

   var basePointX  = 10;

   var basePointY  = 80;

   var currentX    = 0;

   var currentY    = 0;

   var startAngle  = 0;

   var endAngle    = 0;

   var radius      = 120;

   var lineLength  = 200;

   var lineWidth    = 1;

   var lineCount   = 200;

   var lineColor  = "";

   var hexArray    = new Array('0','1','2','3','4','5','6','7','8','9','a','b','c','d','e','f');

   var can = document.getElementById('canvas1');

   var ctx = can.getContext('2d');

   // render a text string...

   ctx.font = "bold 26px helvetica, arial, sans-serif";

   ctx.shadowColor = "#333333";

   ctx.shadowOffsetX = 2;

   ctx.shadowOffsetY = 2;

   ctx.shadowBlur = 2;

   ctx.fillStyle = 'red';

   ctx.fillText("HTML5 Canvas/Android", 0, 30);

   for(var r=0; r<lineCount; r++) {

       currentX = basePointX+r;

       currentY = basePointY+r;

       startAngle = (360-r/2)*Math.PI/180;

       endAngle   = (360+r/2)*Math.PI/180;

       // render the first line segment...

       lineColor = '#' + hexArray[r%16] + '00';

       ctx.strokeStyle = lineColor;

       ctx.lineWidth   = lineWidth;

       ctx.beginPath();

       ctx.moveTo(currentX, currentY+2*r);

       ctx.lineTo(currentX+lineLength, currentY+2*r);

       ctx.closePath();

       ctx.stroke();

       ctx.fill();

       // render the second line segment...

       lineColor = '#' + '0' + hexArray[r%16] + '0';

       ctx.beginPath();

       ctx.moveTo(currentX, currentY);

       ctx.lineTo(currentX+lineLength, currentY);

       ctx.closePath();

       ctx.stroke();

       ctx.fill();

       // render the arc...

       lineColor = '#' + '00'+ hexArray[(2*r)%16];

       ctx.beginPath();

       ctx.fillStyle = lineColor;

       ctx.moveTo(currentX, currentY);

       ctx.arc(currentX, currentY, radius, startAngle, endAngle, false);

       ctx.closePath();

       ctx.stroke();

       ctx.fill();

   }

 }

</script>

</head>

<body onload="draw()">

  <canvas id="canvas1" width="300px" height="200px"></canvas>

</</body>

</html>

```

列表 10.5 包含了一些模板化的 HTML 标记和一个 JavaScript 函数 `draw()`，该函数会在 页面加载到 Android 浏览器时执行。`draw()` 函数包含 JavaScript 代码，用于将一组线和弧绘制到 HTML5 `<canvas>` 元素中，该元素的 `id` 属性值为 `canvas1`。你可以查看这些代码。

![image](img/fig10.2.jpg)

***图 10.2*** 在运行 Android ICS 的 Asus Prime 平板上基于 SVG 的 Android 应用。

图 10.2 显示了在运行 Android ICS 的 Asus Prime 平板上基于 SVG 的 Android 应用。




HTML 页面 `index.html` 位于项目的 `assets/www` 子目录中，其内容如列表 10.7 所示。

### 列表 10.7 index.html

```html

<!DOCTYPE HTML>

<html

  <head>

    <meta name="viewport" content="width=320; user-scalable=no" />

    <meta http-equiv="Content-type" content="text/html; charset=utf-8">

    <title>PhoneGap</title>

    <link rel="stylesheet" href="master.css" type="text/css" media="screen" title="no title" charset="utf-8">

    <script src="phonegap-1.0.0.js"></script>

    <script src="main.js"></script>

  </head>

  <body onload="init();" id="stage" class="theme">

    <h1>Welcome to PhoneGap!</h1>

    <h2>此文件位于 assets/www/index.html</h2>

    <div id="info">

      <h4>Platform: <span id="platform"> &nbsp;</span, Version: <span id="version">&nbsp;</span></h4>

      <h4>UUID: <span id="uuid"> &nbsp;</span, Name: <span id="name">&nbsp;</span></h4>

      <h4>Width: <span id="width"> &nbsp;</span, Height: <span id="height">&nbsp;</span>, Color Depth: <span id="colorDepth"></</span></h4>

    </div>

    <dl id="accel-data">

      <dt>X:</dt><dd id="x">&nbsp;</dd>

      <dt>Y:</dt><dd id="y">&nbsp;</dd>

      <dt>Z:</dt><dd id="z">&nbsp;</dd>

    </dl>

    <a href="#" class="btn large" onclick="toggleAccel();">切换加速度计</a>

    <a href="#" class="btn large" onclick="getLocation();">获取位置</a>

    <a href="tel://411" class="btn large">拨打 411</a>

    <a href="#" class="btn large" onclick="beep();">蜂鸣</a>

    <a href="#" class="btn large" onclick="vibrate();">震动</a>

    <a href="#" class="btn large" onclick="show_pic();">获取照片</a>

    <a href="#" class="btn large" onclick="get_contacts();">获取手机联系人</a>

    <a href="#" class="btn large" onclick="check_network();">检查网络</a>

    <div id="viewport" class="viewport" style="display: none;">

      <img style="width:60px;height:60px" id="test_img" src="" />

    </div>

  </body>

</html>

```

列表 10.7 的第一部分包含一个 `<script>` 元素，它包含了 JavaScript 文件 `phonegap.js`，该文件定义了构成 PhoneGap 核心功能的函数。

列表 10.7 的第二部分显示了锚元素，这些元素允许你测试手机与媒体相关的功能：加速度计、地理位置、通话、蜂鸣、震动效果以及在手机或平板电脑上拍照。

列表 10.8 显示了 `main.js` 文件的内容，它包含了支持 HTML5 页面的选部分 JavaScript 代码。

### 列表 10.8 main.js

```javascript

var deviceInfo = function() {

  document.getElementById("platform").innerHTML = device.platform;

  document.getElementById("version").innerHTML = device.version;

  document.getElementById("uuid").innerHTML = device.uuid;

  document.getElementById("name").innerHTML = device.name;

  document.getElementById("width").innerHTML = device.width;

  document.getElementById("height").innerHTML = device.height;

  document.getElementById("colorDepth").innerHTML = device.colorDepth;

};

function dump_pic(data) {

  var viewport = document.getElementById('viewport');

  viewport.style.display = "";

  viewport.style.position = "absolute";

  viewport.style.top = "10px";

  viewport.style.left = "10px";

  document.getElementById("test_img").src = "data:image/jpeg;base64," + data;

}

function fail(msg) {

  alert(msg);

}

function show_pic() {

  navigator.camera.getPicture(dump_pic, fail, {

    quality: 50

  });

}

```




注意，如果你正在使用 `Xcode 4.3.1`，则你需要手动将生成的 `www` 子目录拷贝到当前 `Xcode` 应用程序的项目根目录中。当你正确完成这一步骤后，在模拟器或你的 iOS 设备上启动移动应用程序时，将不再看到错误信息。

CSS 表格 `ThreeDCube1.css` 与第 2 章 中的 CSS 文件 `3DCube1.css` 相同，因此我们在此不再显示其内容。列表 10.9 显示了 HTML 页面 `ThreeDCube1.html` 的内容，该页面与 Xcode 中通过 PhoneGap 插件生成的 HTML 页面 `index.html` 相同。

### 列表 10.9 index.html

```html

<!DOCTYPE html>

<html>

<head>

  <title>CSS 3D Cube Example</title>

  <link href="ThreeDCube1.css" rel="stylesheet" type="text/css">

  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no;" />

  <meta charset="utf-8">

  <!-- iPad/iPhone specific css below, add after your main css >

  <link rel="stylesheet" media="only screen and (max-device-width: 1024px)" href="ipad.css" type="text/css" />

  <link rel="stylesheet" media="only screen and (max-device-width: 480px)" href="iphone.css" type="text/css" />

  -->

  <!-- If your application is targeting iOS BEFORE 4.0 you MUST put json2.js from http://www.JSON.org/json2.js into your www directory and include it here -->

  <script src="phonegap-1.3.0.js"></script>

  <script type="text/javascript">

    // If you want to prevent dragging, uncomment this section

    /*

    function preventBehavior(e)

    {

      e.preventDefault();

    };

    document.addEventListener("touchmove", preventBehavior, false);

    */

    function onBodyLoad()

    {

      document.addEventListener("deviceready", onDeviceReady, false);

    }

    function onDeviceReady()

    {

      // do your thing!

      //navigator.notification.alert("PhoneGap is working")

    }

  </script>

</head>

<body onload="onBodyLoad()">

  <div id="outer">

    <div id="top">Text1</div>

    <div id="left">Text2</div>

    <div id="right">Text3</div>

  </div>

</body>

</html>

```

列表 10.9 是将来自第 2 章 的 HTML 页面 `3DCube1.html`（它本质上是一组 HTML `<div>` 元素）与你在 Xcode 中使用 PhoneGap 插件创建移动应用程序时自动生成的 HTML 页面 `index.html` 结合而的结果。

现在，在 Xcode 模拟器或你的移动设备上运行此移动应用程序，你将看到一个与图 10.5 类似的图形图像。

![image](img/fig10.5.jpg)

**图 10.5** iPad3 上的 CSS3 立方体。

在本章中创建其他 iOS 移动应用程序的过程与前一个 iOS 移动应用程序的过程相同，因此没有需要包含额外的示例。然而，值得你花时间创建额外的 iOS 移动应用程序，这会增加你的熟练程度，可能还会激励你学习 Xcode 的其他功能。

光上的额外代码样本

![image](img/cd.jpg) 虽然 Android 没有内置渲染图表和图形的支持，但你可以使用基于 Canvas 的代码创建它们，这些代码与上一节中的代码非常相似。

![image](img/cd.jpg) 启动 Eclipse 并创建一个名为 `AndroidCanvasMultiLine2` 的 Android 项目，确保你选择了 Android 3.1 或更高版本。光盘上的 HTML5 页面 `AndroidCanvasMultiLine2.html` 包含了使用 HTML5 Canvas 渲染多折线图的 JavaScript 代码。

图 10.6 显示了在带有 Android ICS 的 Nexus S 4G 上基于 Canvas 的多折线图 Android 应用程序。

![image](img/fig10.6.jpg)

**图 10.6** 带有 Android ICS 的 Nexus S 4G 上基于 Canvas 的多折线图 Android 应用程序。





# CSS3 Keyframes 和 2D 变换, 54

# jQuery 的 `.animate()` 方法, 52–54

# 使用 CSS 动画, 53–54

# jQuery 渐入与滑动, 47–52

# `fadeIn()`, `fadeOut()` 和 `fadeToggle()` 函数, 48–50

# jQuery 滑动相关函数, 50–52

# jQuery 中的缓动函数, 52

# 使用 jQuery Mobile, 171–174

# 渐入相关方法, 171–173

# jQuery 滑动相关方法, 173–174

# Apache Cordova, 209

## `Attribute`, 1, 7

## B
# Backbone Boilerplate, 115

# BackboneJS, 112–115

# 简要介绍, 112–115

# 变, 115–116

# 按钮, 71–73

## C
# 复选框与单选桂, 74–76

# `click()` 函数, 12

# 集合, 113

# 组合框, 76–78

# CR (“候选人推荐”）状态, 88

# 创建“爆炸”特效, 84

# CRUD, 123

# CSS3, 21–44

# 2D 变换, 37–42

# 旋转, 39–42

# 光盘中的额外代码示例, 43–44

# 渐变, 32

# 线性, 32–35

# 径向, 35–37

# 媒体查询, 42–42

# CSS3 特性快速览, 23

# 伪类与属性选择, 23–26

# 阴影特效与圆角, 26–32

# 盒子阴影特效, 30

# 圆角, 30–32

# 使用 RGB 和 HSL 指定颜色, 26–29

# 文本阴影特效与, 26

# CSS3 属性的支持与浏览器特定前缀, 22–23

# `css()`, 8

# CSS 盒模型, 21

# 立立方贝塞尔曲线, 52, 205

## D
# 日期选择, 78–80

# DAP (设备 API) 工作组, 92

# 检测横屏与竖屏模式, 23

# `divColors`, 73

# DOM (文档对象模型)结构, 186

## E
# Eclipse 插件, 225

# Enhance.js, 22

# EmberJS, 116–117

## H
# `hide()` 和 `show()` 函数, 46

# HTML5 Canvas?, 186–207

# 卡卡尔坐标系, 187–189

# 使用 CSS3 和 jQuery Mobile, 198–204

# 线性颜色渐变, 193–196

# 对角线, 193

# 水平, 193

# 垂直, 193

# 线段、矩形、圆形与阴影特效, 189–193

# 径向颜色渐变, 196–197

# SVG 与, 187

# 工具包, 207

# 变换与状态保存, 197–198

# HTML5 相关技术, 87–108

# 跨域资源共享 (CORS), 91–92

# 检测在线与离线状态, 108

# HTML5 拖放 (DnD), 98–99

# HTML5 History APIs, 106

# HTML5 离线应用, 107

# jQuery 与 HTML5 拖放, 99–101

# jQuery 与 HTML5 API, 104–106

# jQuery 与 HTML5 本地存储, 101–103

# HTML5 本地存储的库, 103–104

# 电池 API, 92

# W3C 阶段, 88

# W3C 地理位置, 89–91

# 使用 `getCurrentPosition()` 获取用户位置, 90

# 使用 `watchPosition()` 跟踪用户位置, 90–91

# W3C 候选状态 (CR), 92

# W3C 推荐 (REC), 89

# 使用, 221

# XMLHttpRequest  2 (XHR), 92–98

# 使用 XMLHttpRequest 2 (XHR), 97–98

# 使用 jQuery 调用 AJAX, 95–96

# 不使用 jQuery 调用 AJAX, 93–94

## I
# iOS 移动应用, 225

## J
# `Canvas`, 185, 198

# Jade, 119–123

# 极简 NodeJS 代码, 121–123

# 代码示例, 120–121

# 模板解决方案, 123

# JAXB, 15

# JavaScript 工具包, 1

# jQuery, 1

# 使用 jQuery 获取加速度计数值, 16–19, 184

# 使用 jQuery 跟随鼠标示例, 60–61

# jQuery 链式函数, 15–16

# 在网页中查找元素, 1–4

# “Hello World” 网页, 2–4

# 在 jQuery 中处理点击事件, 12–14

# 在 jQuery 1.7 及之后中处理事件, 14–15

# 使用 jQuery 处理其他事件, 61–62

# 键盘事件, 62

# 鼠标事件, 62

# 使用 jQuery 查询和修改 DOM, 4–12

# 创建 DOM 元素, 9–10

# `:eq`, `:lt`, 和 `:gt` 选择器, 6

# 查找和设置元素属性, 7–8

# `:first` 和 `:last` 选择器, 4–6

# jQuery 中的属性与属性, 7

# jQuery 的 `append()` 和 `appendTo()` 方法, 10–11

# 处理自定属性, 8

# 有用的 jQuery 代码块, 8–9

# 使用 jQuery 移除元素, 11–12

# 在 CSS3 选择器中工作, 46

# jQuery Mobile, 135–163, 165–170, 174–183

# 极简 jQuery Mobile 网页, 136–138





# 使用 CSS3 的动画效果，176–178

# 地理定位，160–163

# 处理用户手势与事件，165–170
# 竖屏模式与横屏模式，170
# 滚动事件，169
# 用于检测用户手势的两个 jQuery 插件，168
# jQuery Mobile 中的列表视图，156–161
# AJAX 与，158–161
# 在一个 HTML5 页面中实现多个页面视图，146–147
# jQuery 与 jQuery Mobile 之间的更多差异，138–144
# 与 CSS 相关的页面初始化，143
# 自定义属性，139
# 页面过渡，140–142
# 页面视图，139
# `mobileinit` 事件，143–144
# 选项与自定义，144
# ...的概述，135–136
# 关键功能与组件，136
# 页面导航与切换页面，144–145
# `jqmData()` 自定义选择器，145
# 在页面视图中定位页眉和页脚，148–149
# 过渡效果，174–176
# 虚拟鼠标事件，179–183
# 在...中使用按钮，150–156
# 作为锚点链接的导航按钮，150–151
# 按钮组与列网格，151
# 使用主题渲染按钮，152–156
# jQuery UI 控件，67–85

## L
LC（最后调用）状态，88

## M
方法链，2
模型 (Model)，112
更改, 113
Modernizr，22
MongoDB，123–124
Mongoose，125–131
一个 SPA 代码示例，127–131
通过 Mongoose 连接到 MongoDB，125
在 Mongoose 中创建 Schema，125–126

## N
Nexus S 4G，224
NodeJS，124–125

## P
PhoneGap，217–222
在 iOS 上使用 CSS3 立方体，222
使用 PhoneGap 插件创建 Android 应用，218–221
它是如何工作的？217–218
插件，225
与...一起，221
进度条，80–82
属性 (Property)，7
PR（建议案）状态，88

## Q
二次贝塞尔曲线，52, 205

## R
REC（建议）状态，88
rotate()，27
路由器 (Router)，114

## S
同源策略，91
scale()，39
滚动事件，169
单页应用 (SPA)，109–131
一个极简的 SPA，119
什么是 SPA？109
用于 SPA 的客户端技术，111
在 SPA 中生成网页，111
在 SPA 中处理模型相关事件，111
MVC 和 MV* 模式，110–111
现代网络架构，110
skew()，40
滑块，67
slideUp(), slideDown(), 和 slideToggle() 方法，50

## T
点击与滑动事件，168
主题滚器 (Theme Roller)，84
ThreeDCube1，225
translate() 方法，41
Twitter Bootstrap，117–119

## V
视图 (View)，113

## W
WD（工作草案）文档，88
写完忘的方法，186

## X
Xcode，224


```
