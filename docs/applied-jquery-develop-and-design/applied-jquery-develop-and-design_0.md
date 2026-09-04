
# jQuery 应用：开发与设计

## 致谢

没有许多人的支持和理解，这样的项目是不可能完成的，而我在开始写书之旅时并未真正理解这一点。说“谢谢”远远不够，但我希望你们都能明白我有多么感激你们！

即使生活的搅拌机在我们周围轰鸣，康妮·凯、凯特琳、布列塔尼、扎克、卡拉和摩根给予我的爱与支持超乎想象。我爱你们！

致丽贝卡·古利克，感谢你信任我，帮助我实现梦想！

致安妮·玛丽·沃克，你的温和坚定、指导和微妙的幽默感，我无法用言语表达。我永远感激你！

致杰西·卡斯特罗，感谢你让我走在正道上。你的洞察力、技术能力和鼓励让我惊叹不已！

致拉里·厄尔曼，感谢你像福特·普里弗克特之于亚瑟·登特一样，引导我穿越银河系！我的毛巾一直放在桌上！

致弗朗西斯·戈弗斯，知道只需一个电话或一封邮件就能联系到你，我生活中的曲折变得更容易忍受。最好的朋友莫过于此！

致那些日复一日与我共事的开发团队伙伴们，感谢你们让我成为更好的程序员和更好的人！你们愿意在我身边指导我、教我新东西，这份情谊无比珍贵。

致`jQuery`社区，你们是一群了不起的人，我很荣幸能与你们共享电子世界！

## 引言

作为网页设计师，你不得不竭尽全力尽快吸引网络浏览者的注意力，然后让他们留在你的网站上吸收内容。除了你提供的产品、服务或信息之外，网站还必须具有视觉吸引力，并提供刺激（且有价值）的交互。`jQuery`库是为你的网站蛋糕增添糖霜的主要原料。如果运用得当，`jQuery`的效果将说服访客和应用用户点击浏览并品尝你的所有内容。

诀窍在于学习如何有效地将`jQuery`与其他标记和语言结合起来。你必须掌握广泛领域的知识，比如`HTML`（超文本标记语言）和`CSS`（层叠样式表），才能知道如何恰当地混合适量的`jQuery`。本书的目标是让你掌握将`HTML`、`CSS`和`jQuery`这些要素结合在一起的知识，从而为你的网站和应用创建引人入胜的交互性。

在整本书中，我还会向你展示如何使用`PHP`（一种流行的服务器端脚本语言）和`MySQL`（一种关系数据库产品）来增强你的整体开发能力，并为你的应用注入强大动力。这两种技术都很容易迁移到其他`Web`开发语言中。

### 什么是 jQuery？

`jQuery`由 John Resig 于 2006 年发布，它作为一种使用`JavaScript`与`HTML`和`CSS`交互的新方式迅速获得了流行和支持。`jQuery`的简单选择器模仿了`CSS`选择器，使得这个库对设计师和开发者来说既熟悉又易于学习。`jQuery`库通过在后端处理大多数浏览器兼容性问题，消除了`Web`开发者在尝试跨多种浏览器创建交互式网站时所遭受的担忧。

除了这两个特性之外，`jQuery`还使用了简化的语法。下面的例子展示了如何使用`jQuery`根据元素的`id`属性来选择它：

```javascript
$('#foo');
```

与老式`JavaScript`中的相同示例相比，`jQuery`选择器要简短得多：

```javascript
document.getElementByID('foo');
```

难怪`Web`开发社区会拥抱`jQuery`“写得更少，做得更多”的口号。将`jQuery`的简洁性与它支持复杂动画和实现惊人效果的能力相结合，你就得到了一个灵活且功能强大的`JavaScript`库，它能够让你为网站访客提供出色的交互体验。

### 本书面向的读者

本书面向初级到中级的`Web`开发者，但无论你作为设计师或开发者处于哪个阶段，都不影响阅读。你应该能在本书中找到一些示例，帮助你用`jQuery`让网页和应用变得生动起来。如果你具备`HTML`、`CSS`、`JavaScript`和`jQuery`的基础知识会有所帮助，但并非必需，因为示例都是完整且可直接使用的。

### 我所使用的工具

在撰写本书时，`jQuery 1.5`已经发布，并且本书中的所有示例都使用了该版本。你可以从[`www.jquery.com`](http://www.jquery.com)下载它。它也可以在本书的网站[`www.appliedjquery.com`](http://www.appliedjquery.com)上找到。

`HTML`、`CSS`和`JavaScript`文件都是纯文本文件，你可以在任何纯文本编辑器中创建和编辑它们。

所有示例均在 Firefox 3 和 Internet Explorer 8 中测试过，偶尔也在 Safari 和 Google Chrome 中查看。

### 代码在哪里获取

本书的所有代码示例都可以从 Applied jQuery 网站[`www.appliedjquery.com/downloads`](http://www.appliedjquery.com/downloads)获取。在那里你可以下载一个包含所有示例、图形和其他所需附件的 Zip 文件。

示例在 Zip 文件中按章节排列，并包含所有必要的`jQuery`文件，以便示例开箱即用。

不过，尽管所有文件都可以下载，我还是鼓励你在阅读本书的过程中亲自输入每个示例。动手实践将帮助你理解所有技术如何协同工作，并加深你对这些概念的记忆。

### 让我们开始吧

是时候让你直接投入并开始学习如何使用`jQuery`了。在第一章中，我将为你提供一些好的规则和工具，帮助你朝着正确的方向前进，用`jQuery`为你的`Web`开发工作增色添彩。

## 欢迎使用 jQuery

### 欢迎使用 jQuery

`jQuery`是当今最流行的`JavaScript`库之一，因为它让你能够快速轻松地构建`JavaScript`网页和`Web`应用，用一行代码就能完成原本需要几十行`JavaScript`代码才能完成的工作。

准备好一台电脑和下面列出的几个工具，然后深入阅读接下来的六个章节。

#### jQuery

`jQuery`可以免费下载和使用，它以一个单独的`.js`文件形式存在，你从网页中链接该文件，然后你的代码通过调用各种`jQuery`函数来访问这个库。前往`jquery.com`下载`jQuery`库。

![图片](img/jquery_icon.jpg)

#### jQuery UI

接下来，你需要从`jQueryUI.com`下载`jQuery UI`库。这将为你提供一些核心交互插件以及许多 UI 小部件，我将在本书后面讨论它们。

![图片](img/jqueryui_icon.jpg)

#### 文本编辑器

你将进行一些脚本编写，所以请准备一个好的文本编辑器。Windows 用户通常选择 Microsoft Notepad 或 Notepad++，而 Mac 用户则经常依赖 Bare Bones Software 的 BBEdit。

![图片](img/bbedit_icon.jpg)

#### 浏览器

很可能你已经安装了一个符合标准的浏览器。流行的选择包括最新版本的 Microsoft Internet Explorer、Mozilla Firefox、Apple Safari、Google Chrome 和 Opera。

![图片](img/chrome_icon.jpg)

#### 故障排查工具

我严重依赖 Firebug Web 开发工具进行故障排查。前往[`getfirebug.com`](http://getfirebug.com)获取一个针对你浏览器的版本。它是 100% 免费且开源的，当出现问题时，你会庆幸已经安装了它。

![图片](img/firebug_icon.jpg)

#### 测试环境

不要使用实际的托管网站来测试你的`jQuery`作品，而是使用你自己计算机上的本地测试环境。我使用 XAMPP，你可以从[`apachefriends.org`](http://apachefriends.org)下载它。

![图片](img/xampp_icon.jpg)

## 1. 初识 jQuery

使用语义化标记和诸如层叠样式表（`CSS`）与`JavaScript`等非侵入式技术的丰富交互式网站，正成为`Web`开发的事实标准。设计师和开发者正在寻找新的、更好的方式来让他们的作品生动起来，而像`jQuery`这样的库使得这一目标易于实现。

为了正确开始使用`jQuery`，你需要配备合适的工具和概念。因此，我为你收集了这些工具，并帮助你学习如何使用它们。

本章将让你牢固掌握`jQuery`的基础知识以及使`jQuery`使用起来简单明了的工具。此外，还包含一些充分利用`jQuery`的技巧。但首先要做的是；让我们从一个“Hello World”示例开始，采用`jQuery`风格。

### 让 jQuery 工作起来

`jQuery`库的强大之处在于它能够与你网页中已经熟悉的元素进行交互。通过使用简单的选择器概念，可以轻松地将网页中的标记标签、类声明和属性信息与`jQuery`连接起来。

`jQuery`选择器会将一个元素或一组元素封装成一个对象。一旦创建了`jQuery`对象，你就可以有效地对该对象应用大量`jQuery`方法，以创建动画、与服务器收发信息或执行对象操作。

任何一本编程书，如果没有“Hello World!”示例，那就不算完整。为了展示`jQuery`选择器的强大和灵活性，我们来创建一个“Hello World!”示例。

---

#### 注意

Hello World 代码是本书网站下载中唯一没有提供的代码示例。原因是我认为你自己亲手输入这段代码非常重要。示例中也包含了注释。

---

1. 首先建立`HTML`页面的基本标记：

   ```html
   <!DOCTYPE>
   <html lang="en">
       <head>
           <meta charset="utf-8" />
           <title>Hello World - jQuery 风格</title>
   ```

2. 确保包含`jQuery`源文件。没有这个文件，任何`jQuery`代码都无法运行：

   ```html
           <script type="text/javascript"
           ![Image](img/ccc.jpg) src="jquery-1.5.min.js"></script>
   ```

3. 打开一个`script`标签，为`jQuery`代码在页面中提供一个位置：

   ```html
           <script type="text/javascript">
   ```

4. 你创建的`jQuery`函数需要在网页加载完所有元素后才能运行。为此，你需要将`jQuery`代码包裹在一个*文档就绪*函数中。顾名思义，当 Web 文档就绪时，包裹在该函数中的代码就可以运行了：

   ```javascript
           $(document).ready(function() {
   ```

5. 创建第一个选择器。这个选择器将获取页面中`id`属性等于`first`的标记元素。所有`id`属性在`jQuery`（和`CSS`）中都是通过在`id`属性包含的信息前加上井号（`#`）来选择的。你将在选择器后面通过链式调用`jQuery`的`html`方法。该方法会将标记`<h1>Hello World!</h1>`放入选中的元素中：

   ```javascript
               /* 向第一个 div 写入 'Hello World!' */
               $('#first').html('<h1>Hello World!</h1>');
   ```

   *链式调用*是用来描述将一个或多个方法应用于`jQuery`对象的术语。链式调用为你提供了多种可能性，可以组合方法，为网站访问者创建独特的交互效果。

6. 在本示例中，你将创建另一个方法，用于连接（或*绑定*）一个事件处理程序到选择器上，以创建一个动作。事件处理程序将接受一个动作，并对其他选中的元素执行额外的`jQuery`函数。首先，将`jQuery`的`click`处理程序绑定到`id`为`link`的元素上：

   ```javascript
               $('#link').click(function() {
   ```

   `click`方法暴露了一个处理函数，允许你构建一系列将由`click`方法触发的动作。

7. 为`id`为`greeting`的元素设置一个选择器，并对其应用`html`方法：

   ```javascript
                   $('#greeting').html('<h1>Hello Again!</h1>');
   ```

8. 用正确的花括号、方括号和`script`标签关闭`jQuery`代码：

   ```javascript
               });
           });
           </script>
   ```

   在创建`jQuery`代码时，要特别注意花括号和方括号。每个开括号或开大括号都必须有对应的闭括号或闭大括号，这一点至关重要。

9. 完成标记的`head`部分，并打开网页的`body`：

   ```html
       </head>
       <body>
   ```

10. 创建一个`id`为`first`的`HTML div`。你之前创建的初始`jQuery`选择器将与此元素交互，添加在`div`标签之间指定的`HTML`标记：

    ```html
            <div id="first"></div>
    ```

11. 创建另一个`id`为`second`的`HTML div`。你没有为这个元素编写任何选择器；它只是用作其他元素的容器：

    ```html
            <div id="second">
    ```

12. 创建一个锚点标签，并赋予它`id`为`link`。你之前编写的`jQuery`代码将处理用户点击该链接时的操作：

    ```html
                <a href="#" id="link">点击我！</a><br />
    ```

13. 创建一个`id`为`greeting`的`span`元素。当链接被点击时，`greeting`的选择器会将你在`span`标签之间指定的`HTML`标记应用进去：

    ```html
            <span id="greeting"></span>
    ```

14. 通过正确关闭标记标签来完成页面：

    ```html
            </div>
        </body>
    </html>
    ```

15. 图 1.1。页面加载时显示“Hello World!”消息，点击链接时显示“Hello Again!”消息。

    ![Image](img/01-01.jpg)

    将文件保存为`hello_world.html`，并在 Web 浏览器中加载。如果你输入得足够仔细，你将看到一个与图 1.1 完全相同的网页。

这个示例只是让你初步了解如何将`jQuery`连接到网页中的元素，以提供信息和交互性。该示例还演示了如何使用`jQuery`向网页添加元素。

要有效地使用`jQuery`，你需要了解如何处理网页中的所有元素，以及它们是如何组合成一个文档的。

一个文档？

完全正确：网页是旨在 Web 浏览器中显示的文档。由于网页是文档，它们遵循一些与纸质文档相同的规则，而这些规则由主文档——文档对象模型（`DOM`）提供。

### 使用 DOM

图 1.2。使用 Firefox 的 Firebug 检查`DOM`。

![Image](img/01-02.jpg)

所有网页的核心是一个`API`（应用程序编程接口），它描述了页面上的所有内容。这就是`DOM`。`DOM`为页面上的每个元素提供信息，包括与元素关联的样式。`DOM`中的信息以树状结构存储。

有几种`DOM`检查器应用程序，既可以作为独立应用程序，也可以作为许多流行 Web 浏览器的插件使用。图 1.2 显示了 Firebug 中可用的`DOM`检查器。

图 1.3。列表中元素之间关系的轮廓。

![Image](img/01-03.jpg)

`DOM API`允许像`JavaScript`这样的语言和像`jQuery`这样的库与网页中的元素进行交互。你可以使用像`jQuery`这样的库在`DOM`树中上下移动，以定位、添加、删除和修改元素。由于你将使用`jQuery`与`DOM`交互，包括从中添加和删除元素，因此你需要熟悉`DOM`的构造方式。你不需要成为`DOM`专家，但你应该对`DOM`有足够的了解，以便在使用`jQuery`操作它时能够识别发生了什么。

当你开始使用`jQuery`的父级和子级类型选择器时，了解`DOM`变得至关重要。你必须理解`DOM`中元素之间的关系，才能有效地操作这些元素。考虑以下`HTML`标记：

```html
<div id="information">
    <ul>
        <li><a href="foo.html"><img src="bar.jpg" /></a></li>
        <li><a href="glorp.html"><img src="murkle.jpg" /></a></li>
    </ul>
</div>
```

要知道如何在`DOM`树中上下移动，你必须知道元素之间的关系是什么。图 1.3 显示了这些关系是如何定义的。

---

#### 换行和注释

由于`JavaScript`允许你通过换行继续代码，`jQuery`也是如此。这意味着你可以将链式调用的`jQuery`方法分散到多行。将较长的链式调用分散到多行可以使`jQuery`方法在视觉上更容易跟踪和调试。你经常会看到类似以下示例的`jQuery`链式调用：



```javascript
var nextImage = $('img[src="bar.jpg"]') // 定义起始点

    .closest('li') // 向上遍历到最近的列表项

    .next() // 移动到下一个列表项

    .find('img') // 在下一个列表项中找到图片标签

    .attr('src'); // 获取找到的图片的 src 属性

    ![Image](img/ccc.jpg) 图片标签
```

我无论如何强调代码注释的重要性都不为过。虽然出于篇幅考虑，本书中不会对大量代码进行注释，但你可以期待在网站上的代码示例中看到大量注释。我个人的风格是：当注释简短时，在行末使用双斜杠；当需要更详细的描述时，则使用较大的注释块（以`/*`开头，以`*/`结尾）。

```javascript
// 这是一个短注释

/* 这个注释可以跨越多行，并且可以非常详细

![Image](img/ccc.jpg) 描述性 */
```

---

掌握了这些知识，你就可以遍历这个列表的 DOM 元素了。假设你知道第一个列表项中的图片源，你可以轻松地获取列表中第二张图片的`src`属性，如下所示：

```javascript
var nextImage = $('img[src="bar.jpg"]') // 定义起始点

    .closest('li') // 向上遍历到最近的列表项

    .next() // 移动到下一个列表项

    .find('img') // 在下一个列表项中找到图片标签

    .attr('src'); // 获取找到的图片的 src 属性

    ![Image](img/ccc.jpg) 图片标签
```

变量`nextImage`现在包含值`murkle.jpg`。

### 学习一些 jQuery 技巧

随着我不断使用和学习 jQuery 库，我积累了一些好的经验法则，包括精确指定 jQuery 选择器、缓存选择器以及打包代码以提高效率。这里提供的这些技巧以及其他技巧将使你的代码更高效，为你提供一些好用的工具，并缩短开发时间。

#### 精确选择元素

为了找到你想要操作的元素，jQuery 需要遍历 DOM 树。根据页面的长度和复杂度，DOM 可能相当庞大。使用粗糙的选择器会降低性能并导致挫败感。

jQuery 从右向左读取选择器，所以如果你有一个像这样的选择器：

```javascript
$("div ul li a");
```

jQuery 会先收集所有锚点，然后判断它们是否在列表项内，再找出列表项是否包含在无序列表中，而该无序列表又包含在`<div>`中。

呼！最好给这一组中的某个元素添加一个 class 或 id 属性，这样你就可以更直接地识别所涉及的一个或多个元素。例如，这一组中的锚点标签可能是导航元素，并赋予一个`navigation`类（`<a href="nav1.html" class="navigation">`）。这样你就可以将选择器缩短为`$(".navigation")`。额外的好处是，该元素在 CSS 中也能更容易地被引用和设置样式！

---

**提示**

感谢非常支持我们的 jQuery 社区，本节中的技巧来自他们。你可以通过参与 jQuery 论坛（[`forum.jquery.com`](http://forum.jquery.com)）学到很多东西。论坛参与者总是乐于帮助你解决 jQuery 和 JavaScript 问题。

---

#### 快速完成 DOM 遍历

有时，你可能需要升级一个由他人开发的、规划不佳的旧网站或应用程序。上一节中提到的选择器`$("div ul li a")`可能需要反复使用才能达到你试图用 jQuery 实现的效果。如果是这样，你应该缓存该选择器，这样你只需要为该选择器遍历一次 DOM：

```javascript
var myNavLinks = $("div ul li a"); // 执行遍历并

![Image](img/ccc.jpg) 存储它

$(myNavLinks) // 新的选择器无需再次遍历

![Image](img/ccc.jpg) DOM 树
```

当你想要操作数十甚至数百个表格行和单元格时，缓存就成了一种宝贵的性能工具。

#### 使用 Firebug 进行故障排除

Firebug 几乎适用于所有浏览器，是调试和分析 JavaScript 的领先工具。它绝对应该出现在你的 Web 开发工具箱中。

Firebug 允许你执行多项任务，包括“实时”观察代码，看看当事件在网页上触发时代码的行为。例如，在**图 1.4**中，一个链接被点击了。如果你仔细看，可以看到几行 HTML 被黄色高亮显示。这些行就是受点击链接影响的 HTML 部分。

Firebug 最方便的功能之一是能够准确识别 JavaScript（以及 jQuery）错误，让你能够快速排查和纠正问题。

我将在本书中多次使用 Firebug 的一些功能。要讨论和演示 Firebug 的所有功能，恐怕需要一整本书！

---

**提示**

Firebug 可从[`getfirebug.com`](http://getfirebug.com)免费下载。

---

图 1.4 使用 Firebug，你可以检查 jQuery 的动作。

![图片](img/01-04.jpg)

#### 打包你的代码

在编写代码时，使用大量空白和注释是有帮助的。但所有注释和空白都会占用空间，因此当你准备将代码投入生产环境时，最好将其打包。你可能已经注意到，官方 jQuery 网站以及插件开发者都提供了两个版本的脚本：普通版和压缩版。压缩版去掉了大部分空白和注释。这确保了你的网站能够更高效地交付。

有多种工具可用于打包代码。我最喜欢的一个是 Google 提供的免费工具——Google Closure Compiler（[`code.google.com/closure/compiler`](http://code.google.com/closure/compiler)）。Google 的 Closure Compiler 提供了一种快速压缩代码的方法，并具有一些额外优势，比如检查非法 JavaScript。

为了好玩，让我们打包文件`spritenav.js`中的一些代码，你将在本书后面用到它。包含空白和注释的代码如下所示：

```javascript
/*

 * 名称: SpriteNav(jQuery)

 * 作者: Jay Blanchard

 * 日期: 2011-01-10

 * 业务规则:    <如果适用>

 *

 * 修订版本:    a20110110jb

 * 状态:       开放

 * 用法:       从 Web 界面页面调用

 *

 * 修订历史

 *

 * a20110110jb   - 创建 CSS 和 XHTML 用于初始测试布局

 */

$(document).ready(function() {

$(function() {

    /* 设置初始值 */

    $("#spriteNav span").css("opacity", "0");

    $("#spriteNav span.selected").css("opacity", "1");

    /* 如何悬停？让我数数... */

    $("#spriteNav span").hover(function() {

        if($(this).attr("class").length == 0) {

            $(this).stop().animate({

                opacity: 1

            }, 75); // 鼠标移入结束

        } else {

            $(this).css("opacity", "1"); // 鼠标移入结束

        }; // 结束 if

    }, function(){

        if($(this).attr("class").length == 0) {

            $(this).stop().animate({

                opacity: 0

        }, 250); // 鼠标移出结束

    } else {

        $(this).css("opacity", "1"); // 鼠标移出结束

    }; // 结束 if

}); // 结束 hover 函数

    /* 点击我！点击我！ */

        $("#spriteNav span").click(function() {

            /* 我们点击了，所以从所有元素中移除 selected 类 */

            $("#spriteNav span").removeClass("selected");

            /* 然后将其添加到被点击的元素上 */

            $(this).addClass("selected");

            /* 然后淡出之前选中的元素 */

            /* 精确指定要淡出的元素 */

            $("#spriteNav span:not(.selected)").stop().animate({

                opacity: 0
```

```javascript
            }, 500);

        }); // 结束点击函数

    }); // 结束函数

}); // 结束文档就绪函数
```

图 1.5 打包前后的代码，同时显示了 Closure 编译器遇到的警告和错误。

![图片](img/01-05.jpg)

在**图 1.5**中，你可以看到打包前后代码的并排对比。使用 Google Closure 编译器打包代码后，它变成：

```javascript
$(document).ready(function(){$(function(){$("#spriteNav span").css

![Image](img/ccc.jpg) ("opacity","0");$("#spriteNav span.selected").css("opacity",

![Image](img/ccc.jpg) "1");$("#spriteNav span").hover(function(){if($(this).attr

![Image](img/ccc.jpg) ("class").length==0){$(this).stop().animate({opacity:1},75)}

![Image](img/ccc.jpg) else{$(this).css("opacity","1")}},function(){if($(this).

![Image](img/ccc.jpg) attr("class").length==0){$(this).stop().animate({opacity:0},

![Image](img/ccc.jpg) 250)}else{$(this).css("opacity","1")}});$("#spriteNav span").

![Image](img/ccc.jpg) click(function(){$("#spriteNav span").removeClass("selected");

![Image](img/ccc.jpg) $(this).addClass("selected");$("#spriteNav span:not(.selected)").

![Image](img/ccc.jpg) stop().animate({opacity:0},500)})})});
```

代码缩减到原始大小的 40%（原始 1360 字节；压缩后 567 字节），非常紧凑。

虽然这是一个很好的例子，展示了压缩 jQuery 代码所能获得的收益，但实际上你并不需要压缩小文件。如果你使用多个小文件，最好将它们合并后再进行压缩处理。如果你打算压缩文件，请务必保留一份用于编辑的副本，其中保留所有空白和注释，然后在准备用于生产网站或应用程序时再进行压缩。

#### 使用 RETURN FALSE

任何做过 JavaScript 编程（包括使用 jQuery 编程）的人，都遇到过`return false;`。大多数情况下，很多人都用错了。让我们看一个例子，一个 HTML 锚标签链接：

```html
<div><a href="inc/content.html">点击这里！</a></div>
```

通常，你可能会应用类似下面的 jQuery 代码来处理锚标签：

```javascript
$("div a").click(function() {

    var link = $(this).attr("href");

    $("#content").load(link);

    return false;

});
```

在这个例子中，你希望能够点击链接，但链接不执行其正常行为；你只想让链接中的内容加载到`id`为`content`的元素中。于是，你在函数中插入了`return false;`。它起作用了！但你真的知道它是如何工作的吗？

因为`return false`工作得很好，你可能没有意识到它以后会给你带来麻烦。`return false`函数首先调用`preventDefault();`，然后调用`stopPropogation()`。`stopPropogation()`函数会阻止`click`事件在 DOM 中冒泡，这可能会阻止你以后添加的祖先元素上的后续`click`事件。当你看似完美的代码无法按你的要求执行，且没有任何错误提示时，你会感到非常困惑。

大多数情况下，你应该使用的是`preventDefault()`，如下面高亮显示的代码所示：

```javascript
$("div a").click(function(e) {

    var link = $(this).attr("href");

    $("#content").load(link);

    e.preventDefault();

});
```

花几分钟时间熟悉其他相关函数`stopPropogation()`和`stopImmediatePropogation()`，因为你可能会发现它们非常有用且能揭示问题！

#### 摆弄 jQuery 代码

多年来我见过的最有用、最酷的工具之一是一个名为 jsFiddle 的 Web 应用程序（[`jsFiddle.net`](http://jsFiddle.net)）。由 Piotr Zalewa 开发，作为“Web 开发者的游乐场”，jsFiddle 是一个很棒的网站，你可以在其中结合 HTML 和 CSS，并用 jQuery 对代码进行实验（**图 1.6**）。该工具支持多个不同版本的 jQuery，是一个极好的故障排除工具。

使用 jsFiddle 网站是与其它开发者分享代码进行讨论、故障排除或炫耀的好方法。该网站还允许你在实验中包含最新的 jQuery UI（用户界面）代码。

图 1.6 使用 jsFiddle，你可以测试 jQuery 代码片段。

![图片](img/01-06.jpg)

### 将 jQuery 与其他代码结合

在本书中，你将使用多种技术来让你的 Web 应用程序生动起来。首先，你将使用 HTML、CSS 和 JavaScript，然后混合使用 PHP 和 MySQL 来支持进一步的交互。

#### 从 HTML 开始

HTML 是你用来启动所有网页的基础。最新版本的 HTML（HTML5）的使用正在增加，本书中的示例在适当的地方使用了它。由于 HTML5 仍在开发中，浏览器支持有限。我建议在使用 HTML5 时进行大量的跨浏览器测试。

jQuery 可以轻松选择 HTML DOM 元素。例如，如果你有一个表单输入元素：

```html
<input name="username" type="text" size="48" />
```

你可以使用 jQuery 选择器`$('input[name="username"]')`与该元素进行交互。

#### 使用 CSS 设计网页样式

CSS 可能是一个棘手的领域，因为不同的浏览器对 CSS 提供的属性支持程度不同。仍然需要进行跨浏览器测试，以确保在一个浏览器中显示的内容也能在另一个浏览器中显示。理解这一点非常重要：你的网站在不同浏览器中看起来不完全一样是可以接受的。

jQuery 将支持最新、最强大的 CSS 版本（CSS3）及其所有属性，但请确保在多个浏览器中进行测试，因为这是确定你所看到的内容是否可接受的唯一方法。

#### 使用 PHP 和 MySQL

作为 Web 上最流行的服务器端语言之一，PHP 在你每天使用和了解的技术上留下了印记。对于本书中的示例和项目，你将使用 PHP 不仅支持对服务器的异步数据请求（AJAX），而且还能通过 jQuery 缩短开发时间。

你将把 PHP 与 MySQL 数据库结合起来，以支持和增强你的 jQuery 项目。

请记住，你可以使用任何数量的语言和数据库产品与 jQuery 结合，正如我在本书中将要介绍的那样——选择完全取决于你。

### 渐进增强

2003 年，Steve Champeon 在德克萨斯州奥斯汀非常流行的 SXSW 互动会议上发表演讲时，创造了术语*渐进增强*。这个概念几乎与一些早期的 JavaScript 库同时出现。

渐进增强的过程是：首先开发你的标记，然后为标记添加样式（CSS），最后通过 JavaScript 引入增强的交互。

在 Web 开发的“美好旧时光”里，设计师和编码人员被一种称为*优雅降级*的范式所束缚。每个人都使用最新技术为最新浏览器设计网站，然后通过插入 hack 或移除 JavaScript 功能来“修复”页面，以便它们能够优雅地降级，并在较旧、功能较弱的浏览器或用户禁用 JavaScript 的情况下仍可使用。开发者试图使用 JavaScript 进行浏览器检测，以便在每个可用的浏览器中提供炫酷的交互。这既繁琐又令人沮丧。Steve Champeon 的概念改变了这一切。



有一种更好的方式来描述渐进增强。在 2008 年发表于 A List Apart 网站的文章《理解渐进增强》（[www.alistapart.com/articles/understandingprogressiveenhancement](http://www.alistapart.com/articles/understandingprogressiveenhancement)）中，Aaron Gustafson 描绘了我最喜欢的关于渐进增强的比喻，他写道：“如果你是个糖果爱好者，可以把它想象成一颗花生 M&M 巧克力豆：从你的内容花生开始，用丰富的、语义化的(X)HTML 进行标记。然后给这颗花生裹上一层浓郁丝滑的 CSS。最后，加上 JavaScript 作为硬糖外壳，制成一颗美味可口的糖果（并且防止它在手中融化）。”

让我们快速看一个渐进增强的例子。以下是`1-1.html`的一部分（可在代码下载中找到，地址为[www.appliedjquery.com](http://www.appliedjquery.com)的`chap1/1-1.html`文件夹）：

```
<body>
    <div id="header"><h2>渐进增强示例</h2></div>
    <div id="clear"></div>
    <div id="leftContent">
        <a href="1-2.html" id="anchor" >新内容</a><br />
        <a href="http://www.google.com" rel="external">Google</a>
    </div>
    <div id="rightContent"></div>
</body>
```

图 1.7 仅使用 HTML 和 CSS 的基本渐进增强页面。

![Image](img/01-07.jpg)

图 1.8 点击`1-2.html`中的“新内容”链接后的结果。

![Image](img/01-08.jpg)

标记非常标准。添加一些基本的 CSS 后，就会得到**图 1.7**中显示的效果。

我还为第二个页面`1-2.html`生成了 HTML 和 CSS，它位于`chap1/1-2.html`文件夹中。如果你点击“新内容”链接，该页面将正常加载（**图 1.8**）。除了为此示例添加了一些内容外，唯一的变化在于 CSS，它使内容显示在焦橙色框中：

```
#rightContent {
    width: 75%;
    margin-left: 20px;
    padding-top: 10px;  
    padding-left: 10px;  
    background-color: #FFCC66;
    vertical-align: top;
    float: left;
}
```

网站运行完美，尽管略显单调。现在让我们在不改动任何现有标记的情况下，添加一点 jQuery。

**1.** 在`1-1.html`的`<head>`部分添加一个标签来引入 jQuery 库：

```
<head>
    <meta http-equiv="Content-Type" content="text/html;
    ![Image](img/ccc.jpg) charset=ISO-8859-1" />
    <title>渐进增强示例 1-1</title>
    <script type="text/javascript" src="../inc/jQuery/8
jquery-1.5.min.js"></script>
```

**2.** 同样在`<head>`标签内添加一个代码块（尽管并非必须，后续示例中你会看到）：

```
<script type="text/javascript">
$(document).ready(function(e) {
    $("#anchor").click(function() {
        $("#rightContent").load("1-2.html #rightContent > p");
        e.preventDefault();
    });
});
</script>
```

基本上，这段代码指定了：*每当点击标识为 anchor 的元素时，将`1-2.html`文件中`rightContent`区域的段落加载到`1-1.html`文件的内容区域中*。

图 1.9 来自第二个页面的内容出现，没有令人分心的背景颜色。

![Image](img/01-09.jpg)

现在当你点击“新内容”链接时，页面不会重新加载，内容会按预期显示，没有难看的背景颜色（**图 1.9**）。

在不使用内联 JavaScript 标签的情况下添加 jQuery，被称为*非侵入式 JavaScript*，并且遵循渐进增强的原则。无需更改任何 HTML 标签，如果 JavaScript 被禁用，页面仍能按设计继续工作。不再需要在 HTML 标签中嵌入 JavaScript 调用！

此外，这里的 CSS 也是非侵入式的。HTML 标签中没有样式属性，但 jQuery 确实为你提供了动态改变样式的能力，通过添加和移除类以及直接操作页面上每个元素的 CSS。在本书中，你将频繁使用这些函数。

### 规划设计与交互

任何好的 Web 应用程序都始于纸上，也许是一些基本的草图。到本书结束时，你将能够使用 jQuery 极大地增强你的网站，因此规划尤为重要。你不想在没有计划的情况下随意将 jQuery 代码扔进网页，否则很快就会导致交互过载。屏幕上会有太多页面元素发生变化和移动，虽然能吸引访问者的注意力，但并非以你期望的方式。

创建故事板是规划如何引导访问者浏览网站的好方法。绘制故事板不需要任何特殊技能。你可以使用便签、草图、流程图，甚至 UML（统一建模语言）来展示潜在交互的行为以及页面之间的连接。一定要多问“如果……会怎样”。如果查看者点击这里会怎样？如果鼠标滚动到页面的这个区域会怎样？如果总额超过 100 美元会怎样？如果你把旋转的、带火焰的 logo 放在页面正中央会怎样？

提出诸如此类的问题并创建网站的基本布局，将让你了解访问者如何看待你的网页并与它们交互。同时，它也会给你一些想法，让你能够构建更多为网站增加价值的 jQuery 小部件。

### 总结

在本章中，你了解了 jQuery JavaScript 库，学习了如何编写正确的 jQuery 语法，以及 jQuery 选择器如何与 CSS 选择器类似。你学习了 jQuery 如何与 DOM 交互，以及如何使用 jQuery 遍历 DOM。你掌握了 Firebug、jsFiddle 和 Google Closure Compiler 等工具的知识，这些工具可以帮助你排查问题、测试并使 jQuery 脚本准备好用于实时网站和应用程序。最后，你学习了如何使用渐进增强技术将 jQuery 与 HTML、CSS 和其他语言结合，使所有代码和脚本保持模块化，便于维护，并让使用功能较弱浏览器的访问者也能有限地使用你的内容。

现在你已经掌握了一些好工具并理解了 jQuery 的基础知识，是时候深入实践了。要了解 jQuery 如何与浏览器及与浏览器相关的事件交互，只需翻到下一页！

## 2. 处理事件

jQuery 的核心能力在于它与各种浏览器和物理事件交互的能力，包括鼠标移动、表单交互和键盘事件。你可以使用 jQuery 控制这些事件，为网站访问者提供更丰富的交互体验。

通过将鼠标点击或按键等事件绑定到文本、链接、图像和其他 DOM 元素，你可以触发从动画到 AJAX 的无数函数。函数可以组合起来创建复杂的连锁反应，这是一件非常酷的事情。

在本章中，我将向你展示如何在创建一个名为“摄影师交流”的虚构网站时，控制许多此类事件。你将组合这些事件来创建效果，让网站观众为之瞩目。其他事件则非常微妙，将为你的 Web 应用程序增添风味。

### 使用“摄影师交流”网站

图 2.1 “摄影师交流”的首页。文本用作占位符，供你后续开发使用。

![Image](img/02-01.jpg)

您将设计摄影师交流网站，让摄影师能够展示他们的照片和技巧。用户将能够上传照片并编辑这些照片的信息。此外，用户还可以提交关于摄影的文章。访客将能够使用不同的条件搜索网站。网站首页将展示精选的照片和摄影师的文章。**图 2.1** 展示了准备编辑的网站基本布局。

---

注意

本书中的所有代码均可从本书网站 [www.appliedjquery.com/download](http://www.appliedjquery.com/download) 下载。

---

### 让导航更优雅

如果您想将渐进增强的原则（如第 1 章所述）应用到您的网站，您需要让导航尽可能优雅。最简单的方法是完整地构建链接，就好像您的访客无法使用 JavaScript（以及 jQuery）一样。

打开 `chap2/2-1.php` 文件。您会看到一个包含三个链接的无序 HTML 列表：

```
<a href="search.php" rel="searchWindow" class="modal"

![Image](img/ccc.jpg) id="search"><span>Search</span></a>

<a href="register.php" rel="registerWindow" class="modal"

![Image](img/ccc.jpg) id="register"><span>Register</span></a>

<a href="login.php" rel="loginWindow" class="modal"

![Image](img/ccc.jpg) id="login"><span>Login</span></a>
```

每个链接在没有 JavaScript 的情况下也能正常工作。点击任意链接都会将相应的页面加载到浏览器中。

---

注意

为了节省本书的时间和篇幅，我没有创建额外的网页。每个模态窗口的内容（包含在 `1-1.php` 中）可以放在单独的页面中，如果您担心用户无法使用 JavaScript 的话。

---

这组链接将用于在浏览器中调用模态窗口。

#### 创建并调用模态窗口

模态窗口是用户与网站和应用程序交互的一种巧妙方式。它们通过将内容“置于”当前网页之上来提供平滑的过渡，可以向用户提供信息，也可以通过表单或确认对话框接收用户的信息。一旦模态窗口关闭，用户将返回到之前在浏览器中查看的相同内容。

每个模态窗口用于在网站上执行特定操作：搜索、注册或登录。您无需对链接的 HTML 进行任何修改；只需添加适当的 jQuery 即可。

**1.** 创建一个 jQuery 语句，选择所有具有 `modal` 类的锚标签：

```
$('a.modal').click(function() {
```

现在，您已将 `click` 事件的控制权交给了 jQuery，或者将 jQuery 的 `click` 事件绑定到了锚标签上。这种绑定允许 jQuery 处理 `click` 事件以及分配给该事件的任何函数。

函数的其余部分决定打开哪个模态窗口、将窗口放置在哪里以及如何关闭模态窗口。此外，该函数还会在整个网站上放置一个半透明的“遮罩”，使模态窗口更加突出。您可以在 `chap2/inc/jqpe.js` 文件中找到完整代码，位于注释 `/* modal windows */` 部分。

**2.** 将当前点击项的 `rel` 属性值存储在一个变量中，该变量将在函数后面使用：

```
        var modalID = $(this).attr('rel');
```

**3.** 淡入您选择的模态窗口，并添加一个允许您关闭模态窗口的链接。使用图形元素（`close_button.png`）使关闭按钮看起来更美观：

```
    $('#' + modalID).fadeIn().prepend('<a href="#"

    ![Image](img/ccc.jpg) class="close"><img src="grfx/close_button.png"

    ![Image](img/ccc.jpg) class="close_button" title="Close Window"alt=

    ![Image](img/ccc.jpg) "Close" /></a>');
```

在文件 `chap2/inc/modal.css` 中，为每个模态窗口定义了外边距和内边距。要使它们在屏幕上居中，您需要考虑内边距和外边距产生的额外空间，以便应用正确的偏移量。在这种情况下，每个模态窗口周围有 20 像素的外边距和 20 像素的内边距。这意味着您必须将高度和宽度增加 80 像素。设置好高度和宽度后，再除以 2 即可得到正确的边距。

**4.** 将计算出的水平和垂直边距值分别赋给变量 `modalMarginTop` 和 `modalMarginLeft`：

```
    var modalMarginTop = ($('#' + modalID).height() + 80) / 2;

    var modalMarginLeft = ($('#' + modalID).width() + 80) / 2;
```

图 2.2\. 模态窗口框，包括内边距和外边距。模态窗口的左上角最初位于窗口高度和宽度的 50% 处。使用负数设置上边距和左边距可将模态框移动到浏览器窗口的中心。

![Image](img/02-02.jpg)

**5.** 现在将边距信息添加到模态窗口的 CSS 中以使其居中：

```
    $('#' + modalID).css({

        'margin-top' : -modalMarginTop,

        'margin-left' : -modalMarginLeft

    });
```

**图 2.2** 展示了模态框的模型，以及需要将其向浏览器窗口的顶部和左侧偏移多少才能居中。

如果您不计算框的中心位置，框的左上角将位于浏览器窗口的中心，如**图 2.3**所示。

图 2.3\. 未计算框中心位置的模态框。模态框的左上角位于浏览器窗口高度和宽度的 50% 处，即 (0, 0)。

![Image](img/02-03.jpg)

---

动画评估

在创建模态窗口时，您使用 jQuery 方法 `fadeIn()` 调用了第一个动画。jQuery 有许多内置的动画方法，包括 `fadeIn` 和 `slideDown`，以及允许您创建自定义动画的 `animate` 方法。

什么是动画？

在 jQuery 中，动画是将元素从一个 CSS 状态平滑地移动到另一个 CSS 状态的行为。动画只能应用于具有数值属性的 CSS 规则。jQuery 使用一组算法来计算从一个状态开始到另一个状态结束的每个点。一个简单的例子是不透明度。

如果一个元素不可见，其不透明度为 0。要使元素完全可见，您将其不透明度设置为 1。根据分配给过渡的时间长度，jQuery 将计算所需的离散步骤，使元素看起来淡入（或淡出），将不透明度从 0 移动到 1，反之亦然。

jQuery 还支持队列，以便您可以组合动画来创建复杂的移动和变化。

jQuery 用户界面（UI）扩展了 jQuery 的基本动画事件，并添加了几个额外的效果方法，包括颜色动画。

---

图 2.4\. 用于注册的模态窗口已打开，并正确居中，带有半透明背景。

![Image](img/02-04.jpg)

##### 创建半透明背景

打开模态窗口的最后一步是创建半透明背景。这个遮罩实际上是一个半透明的 `div`，您仍然可以通过它看到网站。这是一个非常酷的效果，有助于用户理解他们仍然在您的网站上，但注意力应该集中在为他们高亮显示的内容上。您将在网站的其他小部件中使用类似版本的半透明 `div`。

**1.** 向 `body` 追加一个新的 `div` 来创建遮罩：

```
    $('body').append('<div id="modalShade"></div>');
```

**2.** 将半透明背景动画化为部分不透明度，使其变得有些透明：

```
    $('#modalShade').css('opacity', 0.7).fadeIn();
```

**3.** 使用 `return false;` 方法关闭 `click` 函数，以防止链接尝试在浏览器中加载另一个页面。

```
    return false;
});
```

完成后，jQuery 代码会在浏览器窗口中央打开模态窗口，并带有阴影背景，使用户能够看到其下方的网页（**图 2.4**）。

---

### 使用 live( ) 和 delegate( ) 控制未来元素

jQuery 提供了两种方法用于将事件绑定到当前或未来创建的元素上：`live` 和 `delegate`。这两种方法都能省去你在动态添加新元素时额外绑定新事件的工作。两者主要区别在于：`live` 不支持 DOM 遍历，而 `delegate` 支持将事件绑定到特定的 DOM 元素。

要使用 `live`，你必须在选择器之后立即使用它来绑定事件，就像你在关闭模态窗口的代码中所做的那样：

```
$('a.close, #modalShade').live('click', function() {...
```

另一方面，`delegate` 可以这样使用：

```
$('ul#myList').delegate('li', 'click', function() {...
```

这会将 `click` 事件绑定到当前及未来的每个列表项 `(<li>`) 上。如果你向无序列表追加更多列表项，它们都将绑定 `click` 函数。

---

现在不必担心处理表单信息或处理这些信息。我将在第 3 章“让表单更生动”和第 4 章“高效使用 AJAX”中介绍表单处理。

#### 关闭模态窗口

用户必须能够关闭窗口并移除遮罩，因此你需要为用户提供返回网站的方法。

**1.** 通过将关闭图形和模态遮罩绑定到 jQuery 的 `click` 方法来启动关闭函数：

```
$('a.close, #modalShade').live('click', function() {
```



这两个元素最初都不存在于 DOM 中（关于 DOM 的简要讨论请参见第 1 章），因此你必须使用特殊的 jQuery 函数 `live` 将 `click` 绑定到这些元素上。

**2.** 通过获取 `a.close` 的 `parent` 的 `id` 来确定要关闭哪个模态窗口：

```javascript
var thisModalID = $('a.close').parent().attr('id');
```

**3.** 现在淡出模态窗口和遮罩。淡出完成后，使用 `fadeOut` 提供的回调函数移除包含遮罩的 `div` 以及预先附加到模态窗口的链接：

```javascript
$('#modalShade, #'+thisModalID).fadeOut(function() {
    $('#modalShade, a.close').remove();
});
return false;
});
```

简单来说，回调是一段可执行的代码块，作为参数传递给另一个函数。回调中的代码块会在原始函数完成后执行。你向 `fadeOut` 函数发出了一个回调，如下所示：

```javascript
$('#modalShade, #'+thisModalID).fadeOut(function() {
    $('#modalShade, a.close').remove();
});
```

淡出完成后，才会发出回调，从 DOM 中移除 `#modal-Shade` 和 `a.close` 元素。

以这种方式组合多个 jQuery 方法，使得点击链接成为一个相当强大的事件。你能将 `click` 事件或其他事件绑定到非链接元素上吗？当然可以，而且你已经做到了。再看下面这一行：

```javascript
$('a.close, #modalShade').live('click', function() {
```

高亮的值是包含遮罩的 `div` 的 `id`，它也被绑定到了 `live click` 函数上。这允许用户点击遮罩上的任意位置来淡出模态窗口并执行函数中的其他操作。在使用 jQuery 时，绑定到非链接类型的元素是很常见的。

### 将事件绑定到其他元素

jQuery 让你能够灵活地将事件绑定到 DOM 中可用的任何元素。这使你能够创建高度交互的用户界面。创建真正有趣且直观的用户体验比以往任何时候都更容易，因为你不再将用户局限于点击网站上的链接或按钮。

摄影师交流网站需要一种展示会员照片的方式。一个简单的图片轮播将提供展示会员才华的绝佳方法，同时让你作为开发者能够发挥创意。

#### 构建图片轮播

现在让我们为网站添加一个简单版本的图片轮播。

轮播的概念非常简单，基于一个缩略图的无序列表。你可以在 `chap2/2-2.php` 中看到添加到网站的列表：

```html
<div id="carouselContainer">
    <div id="carouselOuter">
        <div id="scrollLeft"><img src="photos/arrowLeft.jpg" /></div>
        <div id="carouselInner">
            <ul id="carouselUL">
            <li><img class="carThumb" src="photos/thumb_ka1.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka2.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka3.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka4.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka11.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka12.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka13.jpg" /></li>
            <li><img class="carThumb" src="photos/thumb_ka14.jpg" /></li>
            </ul>
        </div>
        <div id="scrollRight"><img src="photos/arrowRight.jpg" /></div>
    </div>
</div>
```

现在你有了图片列表，需要添加以下轮播功能：

- 自动滚动。
- 当鼠标光标悬停在轮播的任何部分时，滚动停止。
- 当鼠标光标未悬停在轮播的任何部分时，滚动继续。
- 当鼠标光标悬停在缩略图上时，高亮该图片。
- 控制手动滚动。
- 点击缩略图时显示该图片的更大版本。

在开始添加这些功能之前，你需要使用 CSS 创建轮播的容器。我们先来介绍这个。

##### 设置轮播 CSS

为了使轮播效果良好，它必须有一个稳固的容器。容器将由 CSS 和你之前创建的标记共同定义。

**1.** 设置 `#carouselInner` 规则，使得一次只显示一定数量的缩略图：

```css
#carouselInner {
    float: left;
    width: 510px;
    overflow: hidden;
    background: #000000;
}
```

`#carouselInner` 规则设置了一个 510 像素的可视区域。任何超出此规则所分配元素的内容都将不可见。510 像素区域是通过三个缩略图的宽度（每个 160 像素）加上每个缩略图 10 像素计算得出的。额外的像素用于每个图片周围的填充。

**2.** 创建一个左边距，使得两张图片可以隐藏在轮播的左侧。设置这个边距是 `#carouselUL` 规则中最重要的部分。在轮播左侧保留两张图片可以确保滚动平滑进行。确保整个轮播足够宽，以容纳你计划显示的缩略图数量。在本例中，`#carouselUL` 设计为最多容纳 50 个缩略图：

```css
#carouselUL {
    position: relative;
    list-style-type: none;
    left: -340px;
    margin: 0px;
    padding: 0px;
    width: 8500px;
    padding-bottom: 10px;
}
```

**3.** 现在设置列表项的高度和宽度：

```css
#carouselUL li{
    float: left;
    width: 160px;
    height: 128px;
    padding: 0px;
    background: #000000;
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 5px;
    margin-right: 5px;
    text-align: center;
}
```

图 2.5。旋转木马中可见与不可见的部分。你还可以看到图片如何移动以实现“无限”旋转。当最后一张缩略图显示后，缩略图将从列表开头重新开始。

![Image](img/02-05.jpg)

**图 2.5** 展示了列表项将如何移动。当旋转木马向左滚动时，第一个列表项在不可见状态下被移动到列表末尾。当旋转木马向右滚动时，则发生相反的情况（最后一个列表项被移动到第一个位置）。用户会感觉图片在旋转木马上不停地循环转动。

定义好样式信息后，你就可以开始使用 jQuery 为旋转木马添加功能了。

---

> **注意**
>
> 旋转木马的 CSS（`chap4/css/carousel.css`）内容远不止这些，但大部分是装饰性的，或者为用于手动控制旋转木马的箭头预留空间。此外，还定义了用于显示大图的模态窗口的样式信息。

---

##### 添加自动滚动

现在可以开始为旋转木马添加定义好的功能了。首先创建一个自动滚动旋转木马的函数。创建一个名为 `carousel.js` 的文件，并将其保存在 `chap2/inc` 文件夹中。

**1.** 使用 `function` 关键字创建函数，并命名为 `autoCarousel`。然后将变量 `itemWidth` 设置为旋转木马中一个列表项的宽度，并加上 10 以留出内边距空间：

```javascript
function autoCarousel() {
    var itemWidth = $('#carouselUL li').outerWidth() + 10;
```

**2.** 确定旋转木马需要向左移动的距离。回想一下，CSS 的左边距最初设置为 -340，因此 `moveFactor` 将为 -510。将计算结果赋值给变量 `moveFactor`：

```javascript
var moveFactor = parseInt($('#carouselUL').css('left'))
    - itemWidth;
```

**3.** 现在真正有趣的部分开始了！将 `animate` 方法绑定到由 `#carouselUL` 标识的无序列表上。然后将图片列表向左移动，使图片的左边距与 `moveFactor` 相同。添加 `slow` 持续时间和 `linear` 缓动过渡，以便更精确地控制动画：

```javascript
$('#carouselUL').animate(
    {'left' : moveFactor}, 'slow', 'linear',
    function(){
```

**4.** 将第一个列表项移动到列表末尾，即最后一个列表项之后。这行代码包含在动画的回调函数中，是实现无限旋转木马的秘诀：

```javascript
$("#carouselUL li:last").after($("#carouselUL li:first"));
```

通过移动列表项并整体改变 HTML 列表的顺序，可以使图片看起来在旋转木马上不断循环。

---

> **提示**
>
> 在 jQuery 中，缓动（Easing）用于控制动画在不同时间点的移动速度。jQuery 包含两种默认缓动方法：`linear` 和 `swing`。`Linear` 使动画从 A 点到 B 点匀速移动，速度不变。`Swing` 使动画开始时缓慢，接近中点时加快，到达终点时再减慢。这两种缓动方法都有助于使动画更平滑，减少卡顿感。你可以使用 George Smith 的 jQuery Easing 插件创建一些酷炫的效果。该插件提供了数十种额外的缓动类型，可用于你的 jQuery 应用程序。该插件可从 GSGD 网站获取：[`gsgd.co.uk/sandbox/jquery/easing`](http://gsgd.co.uk/sandbox/jquery/easing)。

---

**5.** 通过将左边距重置为原始值并关闭所有括号和大括号来结束函数：

```javascript
$('#carouselUL').css({'left' : '-340px'});
});
};
```

如果不重置左边距，旋转木马会继续向左滚动，最终图片将移出视野。

**6.** 将 `autoCarousel` 函数放入 `setInterval` 函数中调用。通过将 `setInterval` 方法赋值给一个变量来为其指定标识符。将间隔设置为 2000 毫秒（2 秒）：

```javascript
var moveCarousel = setInterval(autoCarousel, 2000);
```

现在你可以加载页面了。你会看到旋转木马自动启动，并在每次动画之间暂停 2 秒。

**7.** 使用下一行代码使所有缩略图和箭头图形呈现淡出效果：

```javascript
$('.carThumb, #scrollLeft, #scrollRight').css({opacity: 0.5});
```

在创建 `hover` 函数时，你将利用这种设置为淡出状态的不透明度。

##### 添加悬停函数

你将把 `hover` 函数绑定到由类 `carThumb` 标识的缩略图以及包含用于手动控制滚动箭头的 `div` 元素上。`hover` 函数需要执行三个操作：

- 当鼠标光标悬停在旋转木马的任何部分时，停止滚动。
- 当鼠标光标悬停在缩略图上时，高亮显示该图片。
- 当鼠标光标未悬停在旋转木马的任何部分时，继续滚动。

图 2.6。鼠标光标悬停在旋转木马中的一张图片上。图片已淡出至完全不透明，旋转木马已停止滚动。

![Image](img/02-06.jpg)

**1.** 将 `hover` 函数绑定到类 `carThumb` 以及 `id` 为 `scrollLeft` 和 `scrollRight` 的元素上：

```javascript
$('.carThumb, #scrollLeft, #scrollRight').hover(function() {
```

`hover` 函数包含两部分，一部分用于 `mouseover`，一部分用于 `mouseout`。jQuery 的 `hover` 方法将这两部分功能结合在一起，提供了极大的灵活性。

**2.** 将 jQuery 的 `stop` 和 `animate` 方法绑定到由 `$(this)` 表示的元素上，用于函数的 `mouseover` 部分。`stop` 确保当你移开鼠标或执行其他操作时，当前动画会立即停止。如果没有 `stop`，动画会继续排队并运行，这对于 `hover` 函数来说是不可取的：

```javascript
$(this).stop().animate({
    opacity: 1
}, 75);
```

该动画使图片在极短时间（75 毫秒）内淡出至完全不透明。这实现了图片高亮的效果，满足了其中一个要求。在**图 2.6**中，光标悬停在一张缩略图上，使其看起来比相邻的缩略图更亮。

**3.** 通过清除 `setInterval` 函数来停止旋转木马的滚动动画。通过将标识符 `moveCarousel` 传递给 `clearInterval` 函数来指定要清除的间隔：

```javascript
clearInterval(moveCarousel);
```

**4.** 在 `hover` 函数的 `mouseout` 部分添加淡入图片的代码：

```javascript
}, function() {
    $(this).stop().animate({
        opacity: 0.5
    }, 250);
```

jQuery `hover` 函数的 `mouseout` 部分反转了不透明度的淡出效果，并且速度更慢（250 毫秒），只是为了视觉效果。请注意，你没有在 `hover` 函数的任何一侧应用缓动。缓动在这里也可以工作，但从不透明到完全不透明或半透明的移动时间非常短，大多数缓动方法几乎无法察觉。

**5.** 通过在 `hover` 函数 `mouseout` 部分的最后一行调用 `setInterval` 函数来重新启动旋转木马的自动滚动：

```javascript
moveCarousel = setInterval(autoCarousel, 2000);
});
```

旋转木马的需求很快就得到了满足。接下来，你将让网站访问者能够手动控制旋转木马的滚动。

##### 控制手动滚动

网站访问者需要能够手动滚动轮播，以便查找特定图片。添加手动控制相当简单，尽管轮播的移动方向可能与点击的图片看起来相反。换句话说，点击右箭头会使轮播向左移动，点击左箭头则使轮播向右移动。

手动控制的部分功能已在自动滚动函数 `autoCarousel` 中完成（以下高亮代码）。你只需将代码包装在一个函数中，该函数将 `click` 函数绑定到标识为 `scrollRight` 的元素上：

```javascript
$('#scrollRight').click(function(){

    var itemWidth = $('#carouselUL li').outerWidth() + 10;

    var moveFactor = parseInt($('#carouselUL').css('left')) - itemWidth;

    $('#carouselUL').animate(
        {'left' : moveFactor}, 'slow', 'linear', function(){

        $("#carouselUL li:last").after($("#carouselUL li:first"));

        $('#carouselUL').css({'left' : '-340px'});

    });

});
```

如果你观察得非常仔细，你会注意到这个 `click` 事件绑定到了一个指向右方的箭头图片上，但轮播却向左移动。如前所述，这些函数的移动方向可能看起来有些反直觉，但这是有充分理由的。

网站访问者已经被他们一生中大部分时间所执行的动作所条件化。其中最显著的一个动作是翻书或翻报纸。这个动作要求你抓住右侧的页面部分并将其向左移动。这种移动会按照你期望的方式揭示新内容，这看起来非常自然。轮播也是如此。点击右侧会使轮播向左移动，感觉非常自然。你可以通过对函数做一些修改来测试这一点。

向右移动轮播只需要做几处修改。

**1.** 复制用于设置点击右箭头时手动控制的函数，并将新复制的代码粘贴到该函数下方。



**2.** 将函数的第一行改为将`click`函数绑定到`scrollLeft`选择器：

```javascript
$('#scrollLeft').click(function(){
```

**3.** 将分配给`moveFactor`变量的计算改为加上`itemWidth`而不是减去它：

```javascript
var itemWidth = $('#carouselUL li').outerWidth() + 10;

var moveFactor = parseInt($('#carouselUL').css('left')) + itemWidth;
```

轮播移动的距离与之前相同；只是移动方向不同。这种方向差异是通过将移动从左侧 -340 像素动画到左侧 -170 像素来实现的（向左动画时，轮播从左侧 -340 像素移动到左侧 -510 像素）。

**4.** 创建将`animate`方法绑定到轮播的函数：

```javascript
$('#carouselUL').animate(
    {'left' : moveFactor}, 'slow', 'linear', function(){
```

**5.** 将最后一个列表项移动到第一个列表项之前：

```javascript
$("#carouselUL li:first").before($("#carouselUL li:last"));
```

这一移动与之前重新排序图片列表的操作相反，如果用户继续手动选择`scrollLeft`选项，则会使轮播在相反方向上实现“无限”滚动。

**6.** 使用最后一行代码将左边距重置到原始位置，以完成轮播手动控制的要求：

```javascript
$('#carouselUL').css({'left' : '-340px'});

});

});
```

图 2.7. 轮播标准左边距（左侧 -340 像素）与临时设置以支持动画的边距之间的关系。

![Image](img/02-07.jpg)

为了理解移动，**图 2.7** 展示了轮播的正常左边距为 -340 像素。该边距会根据轮播`click`函数的需要临时向右或向左移动。这为动画方法提供了一个“目标”位置。

---

> 注意
>
> 包含箭头的容器的样式规则位于`chap2/css/carousel.css`中。

---

你需要再添加一个要求来完成轮播，这是一个重要的要求（请原谅这个双关语）。轮播需要一种显示更大图片的方法。

### 放大查看大图

当网站访问者发现他们想仔细查看的缩略图时，你不想让他们只是眯着眼睛看缩略图并试图想象它们是大图。通过应用一些 CSS 和 jQuery，可以轻松让用户通过点击缩略图来查看更大的图片。

**1.** 使用类似于创建带有表单元素的模态窗口的技术，在`chap2/2-2.php`中关闭`body`标签之前创建一个`div`：

```html
<div id="photoModal" class="photoModal"></div>
```

**2.** 将`photoModal`的样式规则添加到`chap2/css/carousel.css`：

```css
.photoModal {
    display: none;
    background: #FFFFFF;
    color: #000000;
    border: 20px solid #FFFFFF;
    float: left;
    font-size: 1.2em;
    position: fixed;
    width: auto;
    height: auto;
    top: 50%;
    left: 50%;
    z-index: 200;
}
```

在规则中包含`height`和`width`属性（高亮部分）非常重要，因为这些属性确保加载到`div`中的图片能正确填充该`div`，并支持将图片在浏览器窗口中居中的计算。

接下来，你将向之前创建的文件`chap2/inc/carousel.js`中添加处理大图的额外函数。第一个添加的函数应是将所有大图加载到具有`photoHolder`类的隐藏`div`中。以这种方式加载图片是必要的，因为 jQuery 无法测量尚未加载的元素的高度和宽度。如果没有测量尚未在 DOM 中的元素的能力，则在点击缩略图时加载每张图片可能会产生不稳定的结果。

**1.** 将具有`carThumb`类的缩略图绑定到`each`方法以开始该函数：

```javascript
$('.carThumb').each(function(){
```

**2.** 根据缩略图的源提取图片的路径和名称信息。例如，第一行将`photos/thumb_ka1.jpg`赋值给变量`photoInfo`：

```javascript
var photoInfo = $(this).attr("src");
```

**3.** 在斜杠处拆分缩略图路径信息：

```javascript
var photoPathArr = photoInfo.split('/');
```

拆分会创建一个名为`photoPathArr`的数组。该数组包含两条信息：`photoPathArr[0]`中的`photos`和`photoPathArr[1]`中的`thumb_ka1.jpg`。

**4.** 将斜杠连接到`photos`（包含在`photoPathArr[0]`中）。需要斜杠来正确表示图片的路径：

```javascript
var photoPath = photoPathArr[0]+'/';
```

**5.** 再次执行拆分以获取全尺寸图片的实际名称：

```javascript
var photoInfoArr = photoInfo.split('_');
```

全尺寸图片的名称将包含在`photoInfoArr[1]`中。

**6.** 重新组合这两部分以提供全尺寸图片的路径，例如`photos/ka1.jpg`：

```javascript
var photoSrc = photoPath+photoInfoArr[1];
```

请注意，像刚才那样操作文本在 jQuery（以及其他编程语言）中经常发生。事实上，稍后在此函数中将`click`事件绑定到缩略图时，你会看到类似的文本操作。随着你技能的增长，你将能够编写快速处理此类文本操作的函数，更重要的是，作为可重用的代码片段。

**7.** 通过使用`$('<img/>')`选择器创建新图片，并将图片绑定到`load`函数：

```javascript
$('<img/>').load(function(){
```

**8.** 将一个`div`追加到 HTML 文档的`body`中，以容纳全尺寸图片：

```javascript
$('body').append('<div class="photoHolder"><a href="'+photoSrc+'"</div>');
```

**9.** 将分配给类`photoHolder`的每个元素的 CSS `display`属性设置为`none`。这是为了确保每个新添加的元素对网站访问者不可见：

```javascript
$('.photoHolder').css('display','none');
```

**10.** 为新的`$('<img/>')`提供其源信息：

```javascript
}).attr('src', photoSrc);
```

当`each`函数遍历无序图片列表时，每个全尺寸图片将被放置到其对应的元素中，并对用户隐藏。

对于将绑定到缩略图的`click`函数，你将执行与图片加载函数相同的文本操作步骤。这些步骤被重复执行，因为`load`和`click`函数彼此独立，无法访问对方的变量。

**1.** 将具有`carThumb`类的元素绑定到 jQuery 的`click`方法：

```javascript
$('.carThumb').click(function() {
```

**2.** 执行文本操作步骤以获取路径和全尺寸图片名称：

```javascript
var photoInfo = $(this).attr("src");
var photoPathArr = photoInfo.split('/');
var photoPath = photoPathArr[0]+'/';
var photoInfoArr = photoInfo.split('_');
```

**3.** 为全尺寸照片创建一个图片标签：

```javascript
var photoImgTag = '<img src="'+photoPath+photoInfoArr[1]+'" id="currentPhoto" />';
```

**4.** 从缩略图的`rel`属性中获取要使用的模态窗口名称：

```javascript
var modalID = $(this).attr('rel');
```

**5.** 将图片标签放入模态窗口：

```javascript
$('#' + modalID).html(photoImgTag);
```

**6.** 对`photoModal`应用淡入效果，使其在浏览器窗口中显示。此外，在模态窗口中附加一个允许访问者关闭窗口的按钮：

```javascript
$('#' + modalID).fadeIn('slow', 'swing').append('<div class="photoNote"><a href="#" class="closePhoto"><img src="grfx/photoClose.jpg" class="closeX" title="Close Photo" alt="Close" /></a></div>');
```

**7.** 将 HTML `body`的当前高度加载到变量`bodyHeight`中：

```javascript
var bodyHeight = $('body').height();
$('#currentPhoto').css('height', (bodyHeight - 200));
```

然后使用`bodyHeight`变量设置放大图片的总高度。这样做可以将放大后的图片保持在浏览器窗口的边界内，防止网站访问者需要上下滚动才能看到完整图片。应用于放大图片的高度比浏览器窗口的总高度少 200 像素，这还能为图片留出美观的边框。

---

> 提示
>
> 仔细命名项目，使其信息可重复使用，从而缩短代码并编写更高效的函数。在这种情况下，在照片名称前加上“thumb_”前缀，将为你提供创建正确路径以检索全尺寸图片所需的所有信息。用于上传照片的函数（参见第 3 章）将为你命名缩略图和全尺寸图片。

---

图 2.8. 最终效果。一张缩略图照片的更大版本已加载到浏览器窗口中，供所有人欣赏。

![Image](img/02-08.jpg)

**8.** 使用与之前居中模态窗口相同的计算方式，将当前模态窗口居中：

```javascript
var modalMarginTop = ($('#' + modalID).height() + 40) / 2;
var modalMarginLeft = ($('#' + modalID).width() + 40) / 2;
$('#' + modalID).css({
    'margin-top' : -modalMarginTop,
    'margin-left' : -modalMarginLeft
});
```

**9.** 通过添加半透明遮罩层到背景，使照片突出显示，从而关闭函数：

```javascript
$('body').append('<div id="carouselShade"></div>');
$('#carouselShade').css('opacity', 0.7).fadeIn();
return false;
```

现在，点击缩略图会显示一张更大的照片，并居中显示在浏览器窗口中（**图 2.8**）。

图 2.9. 主导航精灵相当基础，但你可以通过该技术获得惊人的效果。

![Image](img/02-09.jpg)

关闭包含照片的模态窗口的函数与“创建和调用模态窗口”一节中创建的函数相同。

将事件绑定到元素是让 Web 应用程序生动起来的激动人心的工具。结合 jQuery 事件（如`click`、`hover`、`fade`和`animate`）的能力，为网站访问者创造高度交互的体验提供了丰富的机会。

其中一个最流行的交互机会源于老式游戏设计——使用精灵。

#### 创建基于精灵的导航

电子游戏在过去大约 30 年里一直风靡一时，任何玩过早期版本游戏（如《马里奥兄弟》或《塞尔达传说》）的人，都玩过以精灵作为动画基础的游戏。

简单来说，*精灵*是一种描述多个项目的图形，每个项目位于图形中的特定位置。精灵中的每个项目都可以通过其相对于精灵中某个点的位置来访问。通常，精灵的左上角（通常描述为 0, 0）是用于引用每个项目相对位置的点。

CSS 布局对于基于精灵的导航的成功至关重要。样式表规则包含了精灵中所有项目的位置信息。**图 2.9**显示了摄影师交流网站上使用的精灵。该精灵由六个项目组成，分为两行，每行三个项目。行和列仅用于保持精灵中项目的组织；元素可以放置在精灵中的任何位置。该精灵将用于弹出网站的多个模态对话框窗口。

`mainNav.jpg`精灵（位于网站代码的`chap2/grfx`文件夹中）分为两类。第一类包含处于自然状态（无悬停）的项目。第二类（第二行项目）是显示用户用鼠标光标悬停在其上的组。

图 2.10. 精灵`mainNav.jpg`的测量尺寸。该精灵按行和列排列，使得识别精灵元素非常容易。

![Image](img/02-10.jpg)

确定精灵的测量尺寸至关重要。你将在 CSS 中使用这些测量信息来定义项目的位置。获取每列的宽度（例如，搜索列）和每行的高度。**图 2.10**展示了导航精灵的测量尺寸。

请注意，列的宽度可能不同；行的高度在行与行之间是一致的，并且必须一致才能使动画效果正常工作。

---

> 注意
>
> 在用于页面侧面（垂直）导航的精灵中，列宽必须在列与列之间保持一致，但高度可以不同。

---

##### 定义标记

导航的 HTML 标记非常简单，由`chap2/2-2.php`中的一个无序 HTML 列表组成。每个列表项包含一个锚点标签和一个`span`标签：

```html
<ul id="spriteNav">
    <li><a href="search.php" rel="searchWindow" class="modal" id="search"><span>Search</span></a></li>
    <li><a href="register.php" rel="registerWindow" class="modal" id="register"><span>Register</span></a></li>
    <li><a href="login.php" rel="loginWindow" class="modal" id="login"><span>Login</span></a></li>
</ul>
```

尽管标记语言极其简单，但 CSS 却要复杂得多，不过并不难懂。样式表中必须描述每个图像的状态，这些状态还包括每个图像的位置信息。

### 为精灵图创建 CSS

现在让我们深入探讨 CSS（`chap2/css/spritenav.css`）。样式表首先进行基本的清理工作。

**1.** 在`spriteNav`规则中定义精灵图的高度：

```css
#spriteNav {
    height: 30px;
    list-style: none;
    margin: 0;
    padding: 0;
}
```

**2.** 将每个列表项设置为左浮动，使它们并排显示：

```css
#spriteNav li {
    float: left;
}
```

**3.** 为列表项中的锚点标签定义背景图像：

```css
#spriteNav li a {
    background: url(../grfx/mainNav.jpg) no-repeat;
    display: block;
    height: 30px;
    position: relative;
}
```

**4.** 现在为嵌套在每个列表项锚点标签中的`span`标签定义背景图像：

```css
#spriteNav li a span {
    background: url(../grfx/mainNav.jpg) no-repeat;
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    height: 30px;
    width: 100%;
}
```

精灵图被设置为锚点链接和`span`元素的背景图像。这是整个高亮效果在从一个精灵图淡入到另一个时的工作原理的基础：

每一列项目都必须有宽度和位置。位置通过`x`和`y`坐标定义。由于处理的是第一行项目，每个项目的 y 轴均为 0。每个项目的 x 轴定义为鼠标光标当前悬停项目之前所有项目的总宽度。

再看一下图 2.10。在精灵图中，顶行的“搜索”项目的起始坐标为 x 轴 0，y 轴 0。“搜索”宽度为 100 像素，因此“注册”项目的 y 轴仍为 0，但 x 轴为 -100 像素。“注册”项目宽度为 115 像素，因此“登录”项目的 x 轴值为“搜索”宽度加上“注册”宽度，即 -215 像素。

**1.** 定义每个列表元素的`width`和`background-position`：



#spriteNav li a#search {
    width: 100px;
}
#spriteNav li a#register {
    width: 110px;
    background-position: -100px 0px;
}
#spriteNav li a#login {
    width: 90px;
    background-position: -215px 0px;
}

位置，位置，还是位置！

示例中的精灵图组织得非常有序，通过行和列以逻辑方式定义和容纳项目。然而，这种组织程度并非必需。

你可以将项目放置在精灵图中的任何位置。你只需要知道每个项目相对于坐标 `(0,0)` 的偏移量即可。有了这些信息，你就可以创建 CSS 规则来处理位置细节。

掌握了这些知识，你就可以为各种用途设置精灵图，有时甚至可以将许多小项目合并到一个大精灵图中。包含多个项目的大精灵图可以节省带宽，既体现在下载大小上，也体现在减少获取多个小图像所需的服务器请求数量上。

**2.** 现在定义每个 `span` 元素的 `background-position`：

```
#spriteNav li a#search span {
    background-position: 0px -30px;
}
#spriteNav li a#register span {
    background-position: -100px -30px;
}
#spriteNav li a#login span {
    background-position: -215px -30px;
}
```

为什么要使用负数？想象每个列表元素是一个盒子，盒子的左上角由坐标 `(0,0)` 定义。为了让精灵图的每个项目与其列表项的左边缘对齐，精灵图项目必须向左偏移相应的像素数。

对于第二行的精灵图项目，精灵图不仅向左偏移，还以类似方式向上偏移所需的量。

现在 CSS 已正确定义，你可以将注意力转向创建 jQuery 来为精灵图的变换添加动画效果。

### 添加 jQuery 动画

你可以仅使用 HTML 和 CSS 来实现从一个精灵图项目到另一个的即时切换，但这有什么乐趣呢？是时候添加一些 jQuery 来为精灵图的过渡提供平滑的动画效果了。

**1.** 创建函数，首先确保 `spriteNav` 的 `span` 元素设置为默认状态：

```
$(function() {
    $("#spriteNav span").css("opacity", "0");
    $("#spriteNav span").text('');
```

注意，通过将 `span` 元素的不透明度降低到 0 使其不可见。`span` 元素包含精灵图项目，当鼠标光标悬停在 `span` 上时，这些项目将显示出来。

**2.** 将 `span` 元素绑定到 jQuery 的 `hover` 方法，并设置函数的 `mouseover` 和 `mouseout` 部分：

```
    $("#spriteNav span").hover(function() {
        $(this).stop().animate({
            opacity: 1
        }, 100);
    }, function(){
        $(this).stop().animate({
            opacity: 0
        }, 500);
    });
});
```

图 2.11 通过精灵图不透明度的动画，`span` 元素获得了完全可见性。

![Image](img/02-11.jpg)

你之前已经见过作为轮播图需求一部分的悬停效果。这里的区别在于，`hover` 方法淡入由 `#spriteNav span` 描述的精灵图部分。在正常情况下，`span` 是完全透明的，让你可以看到由 `#spriteNav li` 描述的精灵图项目。当鼠标光标进入 `span` 的空间时，精灵图元素的不透明度被动画化为完全可见。图 2.11 展示了悬停效果，但我鼓励你将代码加载到浏览器中，以充分欣赏动画效果。

在第 6 章“创建应用程序界面”中，我将向你展示如何使用精灵图创建更复杂的交互和动画。

### 总结

本章充满了基于将网页元素绑定到事件（如 `click` 或 `hover`）的操作。一旦绑定到事件，jQuery 就可以基于这些事件执行任意数量的方法，包括动画或向 DOM 追加新元素。你从使用单个事件平滑地过渡到组合事件和方法来创建小部件，例如模态窗口、无限图像轮播图和基于精灵图的交互式导航。

本章为你使用和组合事件提供了坚实的基础，但还有许多其他事件值得探索。让我们在探索可用于表单的事件的同时，将你的 jQuery 开发技能提升到新的水平。

## 3. 让表单更生动

访问你网站的用户不仅限于与点击和悬停等基本事件进行交互。你可能希望让用户通过填空式表单提供信息。作为准确数据的守护者，你希望确保用户通过引导他们完成表单填写过程（验证）来提供适当的信息。作为设计师，你希望表单直观且易于使用。作为开发者，你希望利用 jQuery 提供的工具和事件来帮助你的内部数据守护者和设计师创建有效、高质量的表单。

在本章中，你将使用为摄影师交流网站开发的表单，并添加 jQuery 的表单事件，以在验证用户提供的数据的同时增强用户交互。

### 利用表单事件

乍一看，jQuery 为表单方法公开的五个事件（`blur`、`change`、`select`、`focus` 和 `submit`）似乎相当少。虽然列表很短，但将这些方法与其他 jQuery 函数结合使用将产生广泛的功能。

为了引导访客，你需要给他们一些提示（或明确的指引），告诉他们你期望他们下一步做什么。为了避免网站用户只是假设自己应该往表单里输入信息，你可以直接将焦点放在他们应该首先填写的表单元素上。

### 聚焦表单输入

最简短实用的 jQuery 方法之一是 `focus` 函数。使用这个 jQuery 方法，你可以将光标直接放在你希望用户填写的表单元素中。

要使用 `focus` 函数，了解 HTML 元素的 `tabindex` 属性会很有帮助，这些元素包括锚标签、表单元素和按钮。`tabindex` 定义了这些元素基于计算机键盘上 Tab 键被点击时的选中顺序（从具有 `tabindex` 值的最低编号项开始）。你可以像这样在每个元素中手动设置 `tabindex` 值：

```
<input type="text" name="penewuser" size="24" tabindex="0" />
```

在许多情况下，每个页面只有一个表单，这样你就可以使用该函数的最简短形式：

```
$('input[tabindex="0"]').focus();
```

选择器会选择 `tabindex` 为 0 的表单输入，并将光标放在该字段中。

这很简单，但如果有多个表单呢？Photographer's Exchange 网站的 `chap3/3-1.php` 就是这种情况。用户最常使用的三个表单包含在网站主页面中的隐藏元素中。通常情况下，第一个 `tabindex` 很可能是第一个表单中的第一个输入。那么，如何将光标放入当前显示的表单的第一个输入中呢？

打开 `jqpe.js`，找到注释 `/* focus on the first form element */`。接下来的几行包含一个函数，你将用它来识别在模态窗口中打开的任何表单中的第一个输入项。

图 3.1\. 用户点击登录元素后，jQuery 定位到第一个 HTML 输入元素 `object`。

![Image](img/03-01.jpg)

该函数的开场动作是查找所有可见的表单输入，并开始遍历它们：

```
$(':input:visible').each(function(i,e){
```

由于表单最初将其 CSS `display` 属性设置为 `none`，因此只会遍历当前可见的表单元素。当模态窗口打开时，表单变为可见。

`each` 方法包含几个额外的变量：一个用于标识正在处理的表单元素，另一个是迭代器或计数器，从 0 开始。如果你设置一个每次循环时触发的警告（`alert(i+' '+e);`），它会显示计数器和表单输入对象。图 3.1 显示了该警告。

函数中唯一的一行代码为每个可见表单元素的 `tabindex` 属性赋值，从 1000 开始：

```
    $(e).attr(1000, i);
});
```

`tabindex` 值设置得足够高，以避免与网页中可能存在的其他 `tabindex` 值冲突。当你对表单应用 `focus` 方法时，光标将落在当前显示的表单的第一个元素中。

一旦可见表单正确分配了 `tabindex` 值，你就可以使用 `focus` 方法将光标放在第一个输入字段中：

```
$('input[tabindex="1000"]').focus();
```

你在这里使用的 `focus` 方法实际上会将光标放在某个元素上。你还可以在用户通过 Tab 键切换到某个元素或通过鼠标点击选中该元素时触发一个事件。

现在你已经掌握了焦点，让我们来处理一些更具挑战性的事情：使用 jQuery 验证电子邮件地址。

### 验证电子邮件地址

在你喜欢的文本编辑器中打开 `chap3/3-1.php`，找到 `id` 为 `registerForm` 的 `div`。在该表单中，你会找到一行描述电子邮件地址输入的 HTML：

```
<label class="label" for="email">Email: </label><input type="text"
![Image](img/ccc.jpg) name="email" id="email" size="48" /><span class="error">please
![Image](img/ccc.jpg) enter a valid email address</span><br />
```

HTML 错误 `span` 通常通过 CSS 规则（`chap3/css/modal.css`）隐藏：

```
.error {
    display: none;
    color: #FF0000;
    font-size: 0.7em;
    margin: 0px 0px 0px 5px;
}
```

如果执行基本的电子邮件验证时出现错误，错误 `span` 将通过 jQuery 函数更改其显示属性来显示，该函数用于测试表单中输入的电子邮件地址。

基本的表单验证不使用 AJAX（我将在第 4 章“有效使用 AJAX”中向你展示如何使用 AJAX 验证某些表单元素）。开始使用 jQuery 电子邮件验证：

1. 打开 `chap3/inc/jqpe.js` 文件。你将在文档就绪函数包装器的结束括号之前开始创建此函数。

### 征服正则表达式

你会发现有很多方法可以使用正则表达式来测试和验证输入到表单中并在函数中使用的数据。深入讨论正则表达式超出了本书的范围，因此我将推荐一些查找和学习正则表达式的好资源：

- [`www.webreference.com/js/column5`](http://www.webreference.com/js/column5) 提供了一个有效的教程，重点介绍如何在 JavaScript 中使用正则表达式。

- [`developer.mozilla.org/en/Core_JavaScript_1.5_Guide/Regular_Expressions`](https://developer.mozilla.org/en/Core_JavaScript_1.5_Guide/Regular_Expressions) 是用于 Web 浏览器的 JavaScript 正则表达式的权威指南。

- [`regexpal.com`](http://regexpal.com) 提供了一个在线工具，通过提供视觉线索帮助你正确编写正则表达式。输入一个测试字符串，然后编写正则表达式来匹配该字符串。

2. 将 `blur` 方法绑定到电子邮件输入：

```
$('#email').blur(function() {
```

当通过 Tab 键或点击离开输入元素时，会触发 `blur` 方法，导致输入失去焦点。

当失去焦点发生时，你需要采用一种方法来验证电子邮件。最强大的验证方法之一是使用一种称为*正则表达式*的编程结构。我现在就能听到恐惧的尖叫声！尖叫声！哭喊声！

然而，一旦你理解了正则表达式，就没什么好害怕的了。正则表达式是一种灵活的文本字符串匹配方式，非常适合执行验证电子邮件地址所需的匹配。这里使用的正则表达式很容易分解。

3. 插入用于匹配大多数电子邮件地址的正则表达式，并将其存储在变量 `regexEmail` 中：

```
    var regexEmail = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+
    ![Image](img/ccc.jpg) \.[a-zA-Z]{2,4}$/;
```

正则表达式的第一部分 `/^[a-zA-Z0-9._-]+` 表示要匹配的内容应以字母数字字符开头，并且字母字符可以是大写或小写。也允许使用句点、下划线和连字符。`+` 号表示此语句应匹配前面的字符一次或多次。

在初始字符之后，必须有一个 `@` 符号，也称为 *at*。

在 *at* 符号之后，允许另一组字母数字字符 `[a-zA-Z0-9.-]+`，以及仅限句点和连字符。接下来，应该有一个句点 `\.` 来分隔域名和子域名。

正则表达式以 `[a-zA-Z]{2,4}$` 结尾。这表示要匹配的项的最后一部分必须只有字母，长度可以是 2 到 4 个字符。这对于匹配当前可用的 Web 域名非常合适。

4. 将表单输入元素的值放入变量 `inputEmail` 中：

```
    var inputEmail = $(this).val();
```

5. 现在，让我们使用 JavaScript 的 `test` 方法，将输入到表单中的值与正则表达式进行测试：

```
var resultEmail = regexEmail.test(inputEmail);
```

`test` 方法在电子邮件地址有效时返回 `true`，无效时返回 `false`。这样你就可以使用条件测试来判断是否应该显示错误消息。

**6.** 创建一个条件语句，利用正则表达式测试的结果来决定是否向用户显示错误消息：

```
if(!resultEmail){
```

图 3.2. 用户在姓名中留了一个空格。这与用于验证电子邮件地址的正则表达式匹配时无效。

![Image](img/03-02.jpg)

这里的感叹号本质上表示：*如果变量的条件不成立，则测试失败*。

**7.** 如果测试失败，通过更改其 CSS `display` 属性，在此元素（`#email`）旁边显示错误：

```
$(this).next('.error').css('display', 'inline');
```

**8.** 如果测试成功（无论是用户首次输入信息，还是用户返回并更正信息），将错误的 CSS `display` 属性设置为不显示：

```
} else {
    $(this).next('.error').css('display', 'none');
}
```

**9.** 用正确的花括号和方括号关闭 jQuery 电子邮件验证函数：

```
});
```

当输入格式不正确的电子邮件时，在 `blur` 事件发生时显示错误 `span`，使焦点离开电子邮件输入区域。结果如 **图 3.2** 所示。

如果你仔细查看 `chap3/3-1.php` 中的代码，会发现有多个 `span` 元素被分配了 `error` 类。为什么当出现错误时，所有这些 `span` 不会都变得可见？答案在于函数条件语句中使用的方法。再看这一行：

```
$(this).next('.error').css('display', 'inline');
```

关键在于 `.next()` 方法。jQuery 对象 `$(this)` 表示 `id` 为 `#email` 的对象。`#email` 的一个兄弟元素是 `#error`。如果你按层级方式编写 HTML，可以更清楚地看到这种关系：

```
<form name="register" id="registerForm" action="inc/peregister.php"
method="post">
    /* 其他表单元素 */
    <label class="label" for="email">Email: </label>
    <input type="text" name="email" id="email" size="48" />
    <span class="error">please enter a valid email address</span>
    /* 更多表单元素 */
</form>
```

每个高亮显示的元素都是 `form` 元素的子元素，并且与标记中同一层级的所有元素互为兄弟元素。`#email` 的下一个兄弟元素正是代码中紧随其后的错误 `span`。使用 `next` 方法只会更改这个错误 `span` 的属性，使其变得可见。

现在，让我们将表单的 `change` 方法与 `next` 方法结合起来，在表单密码字段填写完毕后关闭错误提示。

#### 确保输入完整

确保表单字段在提交前不为空，是表单输入验证最基本的方法。有几种方法可以创建函数来确保 HTML 表单中的字段已填写。你可以使用正则表达式强制用户使用特定字符，或者确保密码满足最小长度要求。

图 3.3. 用户被警告不要将密码字段留空。

![Image](img/03-03.jpg)

对于摄影师交流网站，唯一的要求是密码字段不能留空。警告会在表单加载时显示，如 **图 3.3** 所示。

**1.** 打开 `chap3/inc/jqpe.js`，首先在文档就绪包装器的结束括号之前创建函数：

```
$(function() {
```

**2.** 获取 `id` 为 `penewpass` 的表单元素中包含的值的长度。将该长度存储在一个名为 `passwordLength` 的变量中：



```javascript
var passwordLength = $('#penewpass').val().length;
```

**3.** 代码中的第一项测试密码字段值的长度。如果长度为零，则显示警告：

```javascript
if(passwordLength == 0){
    $('#penewpass').next('.error').css('display',
    'inline');
```

**4.** 设置 jQuery 代码以监听密码输入字段中发生的 `change` 事件。如果发生更改，CSS 方法将错误的 `display` 设置为 `none`，从而使警告消息消失：

```javascript
$('#penewpass').change(function() {
    $(this).next('.error').css('display', 'none');
});
```

**5.** 正确关闭函数的括号和大括号：

```javascript
}
});
```

尽管你执行了大量客户端数据验证，但始终应该通过删除表单中用户提供的可能有害的语法甚至代码语句，在数据到达服务器时对其进行适当的清理。接下来，当用户能够向摄影师交流网站上传图片时，我们来看看其中一些清理技术。

### 处理上传

图 3.4. 文件上传表单，网站用户一次最多可以上传五张图片。

![Image](img/03-04.jpg)

你可能已经知道，不能使用 AJAX 上传文件。阻止像 AJAX 这样的客户端技术执行文件上传，可以堵住一个潜在的重大安全漏洞。

那么，如何允许用户向你的网站上传文件呢？在本节中，你将学习一种使用 HTML `iframe` 元素和 PHP 进行文件上传的可靠（且安全）的方法，同时保持你期望从 jQuery 获得的流畅交互性。

为了使上传过程有效且安全，你将结合 jQuery 和 PHP。确保用户上传正确的文件是首要任务。你将使用的上传表单位于文件 `chap3/3-4.php` 中，如**图 3.4**所示。

#### 执行客户端验证

由于该网站面向摄影师，文件上传将限制为 *JPG、JPEG*（联合图像专家组）和 *PNG*（便携式网络图形）。这些文件类型特别适合数码摄影。如果用户选择了其他文件类型，上传表单需要提示用户。HTML 包含一个隐藏的错误 `span`，当选择的文件类型不正确时会显示：

```html
<label class="label" for="pUpload1">Select File: </label><input
type="file" name="pUpload[]" id="pUpload1" value="" size="48"
/><span class="error">extension must be jpg, jpeg or png</span>
```

这与之前表单中应用的错误消息类似。将捕获错误的 jQuery 代码放在一个名为 `pePhotoUp.js` 的文件中，该文件将保存在 `chap3/inc` 文件夹中。

**1.** 通过选择上传表单的输入并将它们绑定到 `each` 方法来启动函数：

```javascript
$('input[name*="pUpload"]').each(function(){
```

这里使用的选择器称为*属性选择器*。属性选择器允许你指定一个或多个属性及其各自的值来过滤一组元素。这里选择器包装了所有名称以 `pUpload` 开头的输入。

**2.** 将输入绑定到 `change` 方法，以便捕获输入字段中的任何更改来触发函数的其余部分：

```javascript
$(this).change(function(){
```

**3.** 设置一个正则表达式来测试正确的文件扩展名文本。然后函数将获取更改后的输入的值，并针对该正则表达式测试该值：

```javascript
var regexPhotoExt = /\.(jpg|jpeg|png)$/i;
var photoName = $(this).val();
var resultPhoto = regexPhotoExt.test(photoName);
```

让我们剖析一下这里使用的正则表达式。从右向左看，`i` 表示测试不区分大小写。美元符号（`$`）确保测试针对的是被测试字符串的结尾。表达式的核心部分 `(jpg|jpeg|png)` 是一个包含三个可接受文件扩展名的字符串数组。句点（由反斜杠转义）表示成功的测试字符串将以句点开头。文件扩展名 `.jpg`、`.jpeg` 或 `.png` 将通过测试。

图 3.5 如果用户选择了不合适的文件扩展名，将会看到的错误消息。

![Image](img/03-05.jpg)

**4.** 创建条件检查，用于显示或隐藏错误消息：

```javascript
if(!resultPhoto){
    $(this).next('.error').css('display', 'inline');
} else {
    $(this).next('.error').css('display', 'none');
}
});
```

如果用户选择的文件扩展名与正则表达式数组中的某个值不匹配，则会显示错误，如图 3.5 所示。

---

> **注意**
>
> 提醒一句：向用户提供视觉提示实际上并不能阻止文件被上传！

---

如果设计师和开发者只需在网站访问者试图做他们不希望的事情时提供一条警告消息，那么他们的工作就会轻松很多。但现实是，你还必须在信息到达服务器时对其进行验证，因为有些访问者可能会尝试提交可能危害服务器的数据或上传文件，甚至更糟的是，将带有病毒的文件传播给其他网站访问者。接下来你将学习如何验证这些信息。

#### 开发服务器端验证

在摄影师交流网站中，服务器端验证由文件上传过程中的几行 PHP 代码处理。让我们先单独看看这些代码，了解验证是如何执行的，然后再创建图像上传功能。

在摄影师交流网站的 `chap3/inc` 文件夹中找到 `photoUpload.php` 文件并打开它。该文件包含几个不同的函数，但本节的重点是用于验证上传文件的代码。

---

> **注意**
>
> 本书中的所有服务器端处理都将使用 PHP 代码，但你可以轻松地用任何语言复制这些功能。

---

找到注释 `/* set up the file for validation */`。该注释后面的几行代码是确保上传的文件符合预期（即图像文件）的关键。

PHP 为上传的文件设置了一个临时文件名。PHP 使用这个临时名称来引用该文件，直到上传完成。文件的真实名称也是可用的。这两个名称被保存到变量中，以便于使用：

```php
$tmpName = $_FILES["pUpload"]["tmp_name"][$key];
$photoName = $_FILES["pUpload"]["name"][$key];
```

在下一行中，你会看到一个熟悉的内容。这段代码是用于客户端验证的正则表达式；之所以使用它，是因为你应该始终验证用户提供的数据，而且 jQuery 并没有阻止用户点击“上传”按钮，即使选择了不正确的文件类型：

```php
$regexFileExt = "/\.(jpg|jpeg|png)$/i";
```

PHP 函数 `preg_match` 提供了与 JavaScript 的 `test` 方法相同的测试能力：

```php
if(preg_match($regexFileExt, $photoName)){
```

这种测试级别对某些开发者来说可能已经足够，但你确实希望更安全。在 PHP 中添加额外测试层的一种方法是使用一个函数来读取文件的前几个字节，以确定文件的实际类型。这个函数就是 `exif_imagetype`。

`exif_imagetype` 函数可以返回十多种不同的常量，例如测试有效时返回 `IMAGETYPE_JPEG`。在摄影师交流网站上，用户只允许使用两种不同的文件类型（从二进制角度看，`jpg` 和 `jpeg` 是相同的），因此将两个常量放入一个数组中，用于测试：

```php
$arrEXIFType = array(IMAGETYPE_JPEG, IMAGETYPE_PNG);
```

---

> **提示**
>
> 如果你使用 PHP，请确保你的 PHP 版本包含 EXIF（可交换图像信息）扩展。你需要该扩展才能使用 EXIF 函数。

---

临时文件 `$tmpName` 由函数 `exif_imagetype` 进行测试。然后 PHP 函数检查返回的常量是否在数组 `$arrEXIFType` 中。如果常量与数组中的某个值匹配，则允许继续上传文件：

```php
if(in_array(exif_imagetype($tmpName), $arrEXIFType)){
    // 执行文件上传
```

现在文件可以被正确验证了，是时候将注意力转向实际执行上传了。

---

> **注意**
>
> 当测试失败时，`exif_imagetype` 返回常量 `FALSE`。

---

图 3.6 正常文件上传的路径从一个网页开始，在上传处理完成后结束于另一个网页。

![Image](img/03-06.jpg)

#### 上传文件

由于 AJAX 不能用于上传文件，你将学习如何运用一些 jQuery 魔法，使应用程序能够将文件从用户的计算机移动到网站的服务器上。

通常，上传表单会直接调用处理文件上传的脚本。一旦服务器处理完上传，就会加载另一个网页。图 3.6 展示了该过程如何从浏览器中的表单开始。表单将数据发送到服务器上的脚本（本例中为 PHP 上传脚本）进行处理，然后将用户重定向到一个新的网页。

图 3.7 此屏幕揭示了 jQuery 上传过程背后的魔法。一个 `iframe` 被临时创建，用于容纳文件上传处理脚本。

![Image](img/03-07.jpg)

新的上传函数使用一个临时且隐藏的 HTML `iframe`，该 `iframe` 由 jQuery 函数动态创建。从典型的文件上传表单开始，jQuery 过程随后打开 `iframe`（为清晰起见，如图 3.7 所示），PHP 上传脚本被定向到该 `iframe` 中。当上传脚本完成后，`iframe` 会被 jQuery 过程移除，并显示一个模态窗口，告知用户过程已完成。

##### 编写上传脚本

整个文件上传过程需要两部分：在服务器端处理上传文件的 PHP 代码，以及在客户端由 Web 浏览器使用的 jQuery 代码。你将首先创建客户端 jQuery 代码。

**1.** 打开你在其中创建了客户端文件扩展名验证的 jQuery 文件 `chap3/inc/pePhotoUp.js`。在文件扩展名验证函数的结束括号之后立即开始上传函数。将 jQuery 的 `submit` 方法绑定到上传表单：

```javascript
$(function(){
    $('#uploadForm').submit(function(){
```

**2.** 设置一个 `iframe` 并将其附加到网页的 `body` 中。将 `iframe` 的 `display` 属性设置为 `none`；用户永远不会看到它：

```javascript
var iframeName = ('iframeUpload');
var iframeTemp = $('<iframe name="'+iframeName+'"
src="about:blank" />');
iframeTemp.css('display', 'none');
$('body').append(iframeTemp);
```

现在 `iframe` 已准备好使用，`submit` 函数提供了正确的属性，将 PHP 上传脚本定向到该 `iframe`。这就是上传发生的地方。

**3.** 为 `submit` 函数设置要传递给 `iframe` 的属性：

```javascript
$(this).attr({
    action: 'inc/photoUpload.php',
    method: 'post',
    enctype: 'multipart/form-data',
    encoding: 'multipart/form-data',
    target: iframeName
});
```

现在图像文件已上传到服务器。

让我们为文件上传过程的客户端部分画上句号。你需要让用户知道过程已完成，并执行一些清理工作：清除表单并移除 `iframe`。

### 创建回调风格的功能

jQuery 上传脚本的最后一部分被放入一个短暂的（1 秒）`setTimeout` 函数中。这个超时时间（你可以自行调整时长）允许几个函数依次执行，而不会给网站访客带来突兀的过渡效果。

**1.** 创建 `setTimeout` 函数：

```javascript
setTimeout(function(){
```

**2.** 移除临时的 `iframe`，因为它不再需要：

```javascript
iframeTemp.remove();
```

**3.** 创建一个小型函数，用于确定 `input` 字段中文本的长度。长度信息将被存入 `inputLength` 变量，供文件上传函数后续使用：

```javascript
inputLength = 0;
$('input[name*="pUpload"]').each(function() {
    inputLength += $(this).val().length;
});
```

你不希望在“上传”按钮被意外点击且 `input` 字段中没有数据时显示确认弹窗。为了防止意外确认，需要进行一次检查，确保 `inputLength` 大于零。

**4.** 打开一个条件语句，检查 `inputLength` 变量的值：

```javascript
if(0 < inputLength){
```

图 3.8 访客收到过程已完成的确认信息。

![Image](img/03-08.jpg)

**5.** 如果 `inputLength` 大于零，则在页面主体中追加一个包含确认信息的 `div`：

```javascript
$('body').append('<div id="ty" class="thankyouModal">
<h3>感谢您！上传已完成...</h3></div>');
```

**6.** 为了确保弹窗显示在浏览器窗口中央，获取该 `div` 的高度和宽度，然后加上额外的外边距和内边距宽度。此技术曾在第 2 章中用于居中弹窗和轮播图片：

```javascript
var modalMarginTop = ($('#ty').height() + 60) / 2;
var modalMarginLeft = ($('#ty').width() + 60) / 2;
$('#ty').css({
    'margin-top' : -modalMarginTop,
    'margin-left' : -modalMarginLeft
});
```

**7.** 淡入确认消息（**图 3.8**），让用户知道过程已完成：

```javascript
$('.thankyouModal').fadeIn('slow', function(){
```

**8.** 清空 `input` 字段，使表单恢复干净，可供再次使用：

```javascript
$('input[name*="pUpload"]').val('');
```

---

> **注意**
>
> 文件上传表单中提供给用户的消息仅确认过程已完成。它既不确认文件已发送到服务器，也不报告错误。有许多方法可以使此过程更加健壮。例如，你可以修改脚本以提供错误消息，或使用 AJAX 轮询文件应存放的目录。

---

**9.** 缓慢淡出确认消息，给网站访客一种视觉上的动作感：

```javascript
$(this).fadeOut(1500, function() {
```

**10.** 从 DOM 中移除确认弹窗：

```javascript
$(this).remove();
```

**11.** 确保条件语句的所有花括号和圆括号都正确匹配并闭合：

```javascript
});
});
};
```

`setTimeout` 函数的时间（毫秒，1000 毫秒等于 1 秒）放在函数关闭之前，随后是剩余的闭合花括号、圆括号和分号：

```javascript
}, 1000);});});});
```

---

> **提示**
>
> 一个好的集成开发环境（IDE）编辑器会内置括号匹配功能。

---

何时才能将照片正确显示为全尺寸图像和缩略图？让我们转向处理上传文件的 PHP 脚本 `chap3/inc/photoUpload.php`。

### 处理上传的文件

PHP 照片上传脚本所做的远不止上传文件并验证它们以确保用户不会向你的服务器发送恶意文件。该脚本将全尺寸照片放入正确的目录，创建适当大小的缩略图，并将与上传文件对应的数据存入数据库。

**1.** 创建到 MySQL 数据库的连接：

```php
if(!$dbc = mysql_connect('localhost', 'username', 'password')){
    echo mysql_error() . "\n";
    exit();
}
```

---

> **注意**
>
> 你需要根据你的安装配置，使用特定的服务器、用户名和密码信息来建立此连接。本应用所需的各种表的设置脚本位于代码下载的 `chap3/sql` 目录中，可从 [www.appliedjquery.com](http://www.appliedjquery.com) 获取。

---

**2.** 你将把所有照片和缩略图存储在一个名为（我绞尽脑汁想出来的）`photos` 的目录中。该目录的路径是 `chap3/photos/`。将该路径赋值给 `$photoPath` 变量：

```php
$photoPath = "../photos/";
```

**3.** 开始一个循环，上传每个图像文件，并检查是否存在任何类型的上传错误。有错误的文件将被忽略，但我强烈建议你研究处理错误并将信息反馈给用户的方法：

```php
foreach($_FILES["pUpload"]["error"] as $key => $error) {
    if ($error == UPLOAD_ERR_OK) {
```



## 4. 添加验证代码

添加下一段代码，即本章前面解释过的验证代码：

```php
$tmpName = $_FILES["pUpload"]["tmp_name"][$key];
$photoName = $_FILES["pUpload"]["name"][$key];
$regexFileExt = "/\.(jpg|jpeg|png)$/i";
if (preg_match($regexFileExt, $photoName)) {
    $arrEXIFType = array(IMAGETYPE_JPEG, IMAGETYPE_PNG);
    if (in_array(exif_imagetype($tmpName), $arrEXIFType)) {
```

## 5. 移动照片

将照片的提议路径与实际引用图像文件的名称拼接起来，然后将新图像移动到服务器上的永久目录文件中：

```php
$newPhoto = $photoPath . $photoName;
move_uploaded_file($tmpName, $newPhoto);
```

至此，图像已上传、验证、命名并移动。

## 6. 创建缩略图路径和名称

将全尺寸图像转换为缩略图，以便在轮播和页面中使用，让用户能够编辑照片信息。首先为缩略图创建路径和名称：

```php
$newPhotoThumbnail =
$photoPath . 'thumb_' . $photoName;
```

## 7. 调用 `createThumbnail` 函数

调用`createThumbnail`函数（你将在本章后面的“创建缩略图”部分创建该函数），并向函数传递适当的参数——全尺寸照片的名称、将要创建的缩略图名称以及缩略图的最大宽度和高度：

```php
createThumbnail(
    $newPhoto,
    $newPhotoThumbnail,
    160,
    128
);
}
}
```

在讨论缩略图创建函数之前，让我们先完成脚本的这一部分，将数据保存到数据库。

### 保存图像数据

使用该网站的摄影师希望保存并与其他访客分享照片信息。如果你已经运行了 SQL 脚本来设置照片的数据库表，该表允许存储每张照片的一些基本信息：图像名称、缩略图名称、上传照片的用户名以及照片备注。

在上传过程中，有三个信息片段可以立即用于填充该表。

> **注意**
>
> 此时用户名实际上还不可用，因为注册和登录尚未完成。这些功能将在第 4 章“高效使用 AJAX”中完成。完成该章节后，你需要修改 SQL 代码以适配新增内容。

用于插入图片信息的 SQL 查询被分成多行，以提高可读性并在必要时便于故障排查。查询信息应放在`chap3/inc/photoUpload.php`中的文件上传处理函数之后。

1. 声明插入语句以及数据库和表名：

    ```php
    $photoInsert = "INSERT INTO `photoex`.`pephoto` ";
    ```

2. 声明数据将插入的数据库表中的列名：

    ```php
    $photoInsert .= "(`imgName`,`imgThumb`,`username`) ";
    ```

3. 将上传过程中的每个值插入表中：

    ```php
    $photoInsert .= "VALUES(";
    $photoInsert .= "'" . $photoName . "', ";
    $photoInsert .= "'thumb_" . $photoName . "', ";
    $photoInsert .= "'' ";
    $photoInsert .= ")";
    ```

4. 结束查询并调用 PHP 的`mysql_query`函数执行查询：

    ```php
    if (!($peInsert = mysql_query($photoInsert, $dbc))) {
    ```

    如果查询出错，会在屏幕上打印出几个变量，以便你快速有效地排查问题。在正常情况下，你不希望向用户透露这些信息。相反，你应该给用户一个有意义的错误消息，并记录错误变量的结果，以便在后台作为调试过程的一部分进行检查。

5. 设置 PHP 变量，以便在数据库插入出现问题时为你提供故障排查信息：

    ```php
    echo $photoInsert;
    echo mysql_error();
    echo mysql_errno();
    exit();
    ```

6. 用适当的闭合括号结束 PHP 文件上传函数：

    ```php
    }
    }
    }
    ```

照片安全上传且数据记录到数据库后，网站进展顺利。你还需要做的另一项工作是确保正确创建缩略图，以便它们能在网站之前包含的轮播中正常工作。缩略图在需要时也会以表格形式显示。

### 创建缩略图

在第 2 章中，你创建了一个无限轮播来显示图片缩略图。要从所有上传的图片中创建缩略图，你将使用此处描述的 PHP 函数。

配置轮播时，你确定每张使用的图片宽度不能超过 160 像素，高度不能超过 128 像素。你需要将这些信息连同其他几个参数一起传递给函数。你将在文件上传函数中使用这行代码来调用缩略图创建方法：

`createThumbnail($newPhoto, $newPhotoThumbnail, 160, 128);`

图 3.9 比较全尺寸原图与其更小的缩略图。

![Image](img/03-09.jpg)

以下参数被传递给函数：

- 变量`$newPhoto`中的新照片名称。
- 变量`$newPhotoThumbnail`中你希望缩略图拥有的名称。
- 缩略图的最大宽度（像素）。
- 缩略图的最大高度（像素）。

请记住，该函数可以创建任何尺寸的缩略图；你只需更改最后两个参数即可。正如你将看到的，该函数会根据需要计算宽度或高度，以确保缩略图按比例缩放。图 3.9 显示了通过该过程创建的缩略图，以及它与原图相比如何保持比例。

让我们深入探讨并在`chap3/inc/photoUpload.php`中创建 PHP 函数，该函数将从你的图片生成缩略图。

1. 首先声明函数及其参数：

    ```php
    function createThumbnail($name, $filename, $newWidth, $newHeight) {
    ```

2. 通过拆分变量将图片名称放入数组。使用示例中的图片名称`cameras.jpg`，用`explode`方法创建一个包含两个条目`cameras`和`jpg`的数组（`$arrPhotoName`）。使用下一行将`jpg`放入变量`$fileExtPosition`：

    ```php
    $arrPhotoName = explode('.', $name);
    $fileExtPosition = count($arrPhotoName) - 1;
    ```

    PHP 的`explode`方法接受两个参数：分隔符和要拆分的项目。此处的分隔符是句点。

3. 根据图片类型（基于文件扩展名），调用相应的 PHP 函数以正确格式创建工作图像。将使用此工作图像代替原始图像。使用图像的副本有助于确保不会破坏或损坏原始图像：

    ```php
    if (preg_match('/(jpg|jpeg)/i', $arrPhotoName[$fileExtPosition])) {
        $workingImg = imagecreatefromjpeg($name);
    } elseif (preg_match('/(png)/i', $arrPhotoName[$fileExtPosition])) {
        $workingImg = imagecreatefrompng($name);
    }
    ```

    注意再次使用了正则表达式。你现在应该已经习惯它们了。

> **提示**
>
> 此函数中用于操作图像的 PHP 函数由 GD 库提供，这只是 PHP 可用的图像操作库之一。如果你想使用此处使用的图像操作函数，请确保你的 PHP 版本已编译 GD 库。

4. 现在可以开始这个函数真正有趣的部分了。首先需要获取工作图像的宽度和高度。以下计算将确定缩略图的新高度和宽度：

    ```php
    $oldX = imagesx($workingImg); // 宽度
    $oldY = imagesy($workingImg); // 高度
    ```

5. 如果工作图像的宽度大于高度，则将宽度设置为 160 像素，并计算使高度成比例的像素数：

    ```php
    if ($oldX > $oldY) {
        $thumbW = $newWidth;
        $thumbH = ($oldY * $newWidth) / $oldX;
    }
    ```

6. 如果工作图像的高度大于宽度，则将缩略图的高度设置为 128 像素，并计算使宽度成比例的像素数：

    ```php
    if ($oldX < $oldY) {
        $thumbW = ($oldX * $newHeight) / $oldY;
        $thumbH = $newHeight;
    }
    ```

7. 对于正方形图像，可以将高度和宽度设置为轮播中使用的最大高度：

    ```php
    if ($oldX == $oldY) {
        $thumbW = $newHeight;
        $thumbH = $newHeight;
    }
    ```

8. 使用 PHP 的`ImageCreateTrueColor`函数，并将新确定的缩略图宽度和高度传递给它：

    ```php
    $newThumbnail = ImageCreateTrueColor($thumbW, $thumbH);
    ```

    缩略图现已创建。

> **注意**
>
> 缩略图创建函数是为简单起见而设计的。该函数对于通常在轮播最大尺寸范围内的图片效果良好。当图片宽度和高度值接近但尚未成为正方形时，这些简单的算法将无法使缩略图保持在轮播设计的最大高度和宽度范围内。解决方法是查看计算出的缩略图高度和宽度，如果任一测量值超出范围，则再次调整高度或宽度。

9. 重新采样图像以保持缩略图质量；你将使用 PHP 的`imagecopyresampled`来实现。你需要为此函数提供多个参数才能使其正常工作：

    - 目标图像资源（`$newThumbnail`）。
    - 源图像资源（`$workingImage`）。
    - 目标点的`x`和`y`坐标。这告诉重采样函数从目标图像上的哪个点开始工作。在本例中，它是图像的左上角。
    - 源点的`x`和`y`坐标。这告诉重采样函数在源图像中从哪个点开始工作。它从左上角开始。
    - 目标宽度和高度。
    - 源宽度和高度。

    ```php
    imagecopyresampled(
        $newThumbnail,
        $workingImg,
        0,
        0,
        0,
        0,
        $thumbW,
        $thumbH,
        $oldX,
        $oldY
    );
    ```

10. 重采样完成后，将图像输出到适当的位置，从而将其移动到网站文件结构中的永久位置。如果图像是`png`，则使用 PHP 的`imagepng`执行此操作；否则，使用`imagejpeg`：

    ```php
    if (preg_match("/(png)/i", $arrPhotoName[$fileExtPosition])) {
        imagepng($newThumbnail, $filename);
    } else {
        imagejpeg($newThumbnail, $filename);
    }
    ```

11. 销毁资源以释放服务器上的内存：

    ```php
    imagedestroy($newThumbnail);
    imagedestroy($workingImg);
    }
    ```

缩略图创建完成！通过将 jQuery 上传过程与 PHP 结合，你创建了一种有效的方式，允许用户将文件上传到你的网站。同时，你掌握了操作文件以满足需求并保护服务器免受损害的技术。

现在花点时间上传一些图片，并对一些表单功能进行修改，以便更好地理解这一切是如何协同工作的。在此过程中，思考如何修改和改进此功能，以便在你的表单中使用。

### 总结

在本章中，你牢固掌握了处理表单及表单中数据的方法。你了解了诸如使用正则表达式在 jQuery 中验证数据而无需往返服务器的方法。在此过程中，你学到了几种向表单用户提供有意义用户消息的方式。你还学会了如何使用 jQuery（无需 AJAX）通过隐藏的 iframe 元素将文件上传到服务器，以及确认允许用户上传的文件类型的方法。

正当你以为可以安全地离开表单领域时，接下来你将学习如何使用 jQuery 的 AJAX 方法。在第 4 章中，将深入介绍 jQuery 的 AJAX 函数，为你提供改进和增强表单的方法，并通过动态平滑加载内容来改善用户体验。卷起袖子开始吧！

## 4. 高效使用 AJAX

AJAX 是多年来进入 Web 开发领域最热门的技术组合之一，它能够将新内容加载到现有的 DOM 结构中，从而推动了交互式 Web 设计的蓬勃发展。

jQuery 通过为基本 AJAX 方法提供几种简写方法，简化了 AJAX 的使用。对于大多数开发者和设计师来说，这些简写方法就足以满足需求。本章重点介绍 jQuery 的 AJAX 简写方法`post`、`get`和`load`。jQuery 还提供了强大的功能集，包括回调函数，供希望自定义 AJAX 调用以提供更丰富交互体验的开发者使用。我将向你展示如何使用 jQuery 的多个 AJAX 功能来增强网站和应用程序。让我们从完成你在第 3 章中开始的表单验证开始。

### 使用 AJAX 进行验证

简单来说，AJAX（异步 JavaScript 和 XML）允许你使用 JavaScript 异步地向服务器发送和接收信息，而无需页面重定向或刷新。你可以使用 AJAX 获取信息并更新用户当前正在查看的网页。可以对后台运行的数据库发出复杂请求。

当新用户注册使用网站时，他们需要拥有唯一的用户名。他们的用户名将与其他信息（如上传的照片或撰写的文章）相关联。它将是允许他们更新所提交照片信息的关键。

首先，请确保通过在数据库上运行 SQL 文件`chap4/sql/peuser.sql`来设置网站数据库。在 MySQL 或任何其他数据库平台上运行此脚本将创建网站数据库、该数据库的用户以及用于存储网站访问者注册信息的表。然后，你可以开始构建 PHP 文件，该文件将响应 AJAX 函数请求的操作。

#### 构建 PHP 注册和验证文件

希望分享图片并可能撰写摄影文章的摄影师需要一种方式向网站注册信息，以便他们能够登录并访问非注册用户无法使用的网站功能。

你可以为此创建一种对用户来说非常流畅的交互。借助 jQuery 的 AJAX 功能，你可以避免页面重新加载或重定向到其他页面（图 4.1）。AJAX 引擎会将请求发送到服务器上的 PHP 脚本，而不会中断用户体验。

使用 PHP 和 jQuery，你将创建支持注册交互的函数。

1. 打开一个新文本文件，并将其保存为`chap4/inc/peRegister.php`。

> **注意**
>
> 如果你希望使用下载中提供的 PHP 文件，请随意跳到“设置 jQuery 验证和注册函数”部分。请务必编辑 PHP 文件，使用正确的用户名、密码和主机名来匹配你在数据库服务器上设置的数据库连接。

图 4.1. 典型 HTTP 请求与 jQuery AJAX 方法使用的 XMLHttpRequest 之间的区别。

![Image](img/04-01.jpg)

2. 为 PHP 函数设置数据库连接，包括在无法建立连接时返回错误的方法：

    ```php
    if (!$dbc = mysql_connect('servername', 'username', 'password')) {
        echo mysql_error() . "\n";
        exit();
    }
    ```

此 PHP 文件中包含三个操作：一个用于完成注册，一个用于验证用户名，还有一个方法允许注册用户登录。将根据 AJAX 函数中使用的表单名称调用相应的函数。

3. 使用 PHP 的`switch`方法确定提交的是哪个表单，并为注册表单设置第一个`case`：

    ```php
    switch ($_POST['formName']) {
        case 'register':
    ```

4. 检查用户名和密码是否已设置：

    ```php
    if (isset($_POST['penewuser']) &&
        isset($_POST['penewpass'])) {
    ```

5. 如果用户名和密码已设置，则使用表单中的数据完成一条 SQL 语句，将新用户的信息插入数据库：

    ```php
    $peuserInsert = "INSERT INTO `photoex`.`peuser` ";
    $peuserInsert .= "(`username`, `userpass`,
    `userfirst`, `userlast`, `useremail`";
    ```

6. 由于用户在注册时可以选择多个摄影兴趣，因此必须设置一个循环来处理注册表单中选中的复选框：

    ```php
    if (isset($_POST['interests'])) {
    ```

7. 此处使用的循环计算所选兴趣的数量，并正确格式化 SQL 语句以命名这些兴趣。在正确的位置插入逗号，并用右括号关闭初始语句：



```php
$peuserInsert .= ",";
for($i = 0; $i < count($_POST['interests']); $i++){
    if($i == (count($_POST['interests']) - 1)){
        $peuserInsert .= "`".$_POST['interests'][$i]."`";
    } else {
        $peuserInsert .= "`".$_POST['interests'][$i]."`, ";
    }
}
```

```php
$peuserInsert .=")";
```

**8.** 将注册表单中的值按正确顺序放入 SQL 语句：

```php
$peuserInsert .= "VALUES (";
$peuserInsert .= "'".$_POST['penewuser']."', ";
$peuserInsert .= "'".$_POST['penewpass']."', ";
$peuserInsert .= "'".$_POST['pefirstname']."', ";
$peuserInsert .= "'".$_POST['pelastname']."', ";
$peuserInsert .= "'".$_POST['email']."' ";
```

**9.** 插入正确的值，包括遍历表单中选择的任何兴趣，并为这些兴趣插入值“yes”：

```php
if(isset($_POST['interests'])){
    $peuserInsert .= ",";
    for($i = 0; $i < count($_POST['interests']); $i++){
        if($i == (count($_POST['interests']) - 1)){
            $peuserInsert .= "'yes'";
        } else {
            $peuserInsert .= "'yes', ";
        }
    }
}
```

**10.** 正确关闭 SQL 语句：

```php
$peuserInsert .=")";
```

如果你打印出变量`$peuserInsert`中包含的最终 SQL 语句，它看起来会像这样：

```sql
INSERT INTO `photoex`.`peuser`(`username`, `userpass`,
`userfirst`, `userlast`, `useremail`,`landscape`,
`astronomy`,`wildlife`) VALUES ('Bob.Johnson','ph0t0man',
'Bob','Johnson','photoman@gmail.com','yes','yes','yes','yes')
```

**11.** 使用 PHP 函数`mysql_query`将数据插入数据库，用户即完成注册：

```php
if(!($peuInsert = mysql_query($peuserInsert, $dbc))){
    echo mysql_errno();
    exit();
}
```

### 检查用户名的可用性

由于新用户通常会先填写用户名，密码和用户名尚未设置，因此将调用`else`语句。以下是检查用户名是否存在于数据库中的 PHP 代码。

**1.** 创建一个 SQL 查询，从用户数据库中选择注册表单中输入的用户名：

```php
} else {
    $peCheckUser = "SELECT `username` ";
    $peCheckUser .= "FROM `photoex`.`peuser` ";
    $peCheckUser .= "WHERE `username` = '".$_POST['penewuser']."' ";
    if(!($peuCheck = mysql_query($peCheckUser, $dbc))){
        echo mysql_errno();
        exit();
    }
```

如果用户在注册表单中输入的名称已存在于数据库中，查询将返回行数 1。如果名称不在数据库中，行数为 0。

**2.** 将查询返回的行数赋值给变量：

```php
$userCount = mysql_num_rows($peuCheck);
```

**3.** 输出计数值，供 AJAX 函数返回，以便 jQuery 判断用户是否应在注册表单中输入新用户名：

```php
echo $userCount;
}
```

**4.** 完成注册表单的`case`语句：

```php
break;
```

### 创建用户登录的 PHP 代码

注册后，用户可以登录网站并开始上传照片和撰写文章。让我们完成 PHP 文件的登录部分。

**1.** 为登录代码设置`case`语句：

```php
case 'login':
```

**2.** 检查用户名和密码是否已设置：

```php
if(isset($_POST['pename']) && isset($_POST['pepass'])){
```

**3.** 如果已设置，向数据库发送包含用户名和密码信息的查询：

```php
$peLoginQ = "SELECT `username`, `userpass` ";
$peLoginQ .= "FROM `photoex`.`peuser` ";
$peLoginQ .= "WHERE `username` = '".$_POST['pename']."' ";
$peLoginQ .= "AND `userpass` = '".$_POST['pepass']."' ";
if(!($peLogin = mysql_query($peLoginQ, $dbc))){
    echo mysql_errno();
    exit();
}
```

---

> **注意**
>
> 在将数据提交到数据库之前，务必严格检查用户输入表单的数据，确保数据已被清理。

---

图 4.2 用户可点击的复选框，用于记住登录状态。用户无需再次登录，直到与此操作关联的 cookie 过期或从计算机中删除。

![Image](img/04-02.jpg)

**4.** 将变量`$loginCount`设置为数据库查询返回的行数。如果用户名和密码正确，该值将为 1：

```php
$loginCount = mysql_num_rows($peLogin);
```

接下来，根据用户的偏好设置 cookie。Cookie 是放置在访问者计算机上的一个小文件，包含与特定网站相关的信息。如果用户希望在此计算机上被记住，可以选择**图 4.2**中显示的复选框。

**5.** 如果登录尝试成功，确定应存储在 cookie 中的信息：

```php
if(1 == $loginCount){
```

**6.** 如果选中了“记住我”复选框，则设置一个包含用户名的 cookie，其过期时间为当前日期起一年后：

```php
if(isset($_POST['remember'])){
    $peCookieValue = $_POST['pename'];
    $peCookieExpire = time()+(60*60*24*365);
    $domain = ($_SERVER['HTTP_HOST'] != 'localhost') ? $_SERVER['HTTP_HOST'] : false;
```

`time()`函数的计算将过期日期设置为当前日期起一年后，以秒表示，即 31,536,000 秒。对于任何旨在记住用户的 cookie 来说，一年通常是足够的时间。`$domain`变量中的信息确保 cookie 在`localhost`以及任何其他有效域名上都能正常工作。

**7.** 创建 cookie 并输出`$loginCount`供 AJAX 使用：

```php
setcookie('photoex', $peCookieValue, $peCookieExpire, '/', $domain, false);
echo $loginCount;
```

**8.** 如果用户未选择记住选项，则设置一个在浏览器关闭时过期的 cookie：

```php
} else {
    $peCookieValue = $_POST['pename'];
    $peCookieExpire = 0;
    $domain = ($_SERVER['HTTP_HOST'] != 'localhost') ? $_SERVER['HTTP_HOST'] : false;
    setcookie('photoex', $peCookieValue, $peCookieExpire, '/', $domain, false);
    echo $loginCount;
}
```

**9.** 如果用户名和密码未设置，则输出登录计数。该值应为 0：

```php
} else {
    echo $loginCount;
}
}
break;
```

---

> **注意**
>
> 有关 PHP 以及如何有效使用 MySQL 的更多信息，请参阅 Larry Ullman 的著作《PHP 6 and MySQL 5 for Dynamic Web Sites: Visual QuickPro Guide》（Peachpit, 2008）。

---

PHP 文件准备就绪后，接下来构建 jQuery AJAX 函数。

#### 设置 jQuery 验证和注册函数

检查新用户名应尽可能对注册者无缝。表单应在提交前向用户提供即时反馈，并提示他们修改信息。用户名的表单输入元素（位于`chap4/4-1.php`）将绑定到`blur`方法：

```html
<label class="labelLong" for="penewuser">请选择一个用户名：</label>
<input type="text" name="penewuser" id="penewuser" size="24" />
<span class="error">名称已被占用，请重新选择 another</span>
```

![Image](img/04-03.jpg)

**1.** 将用户名的表单输入绑定到 jQuery 的`blur`方法：

```javascript
$('#penewuser').blur(function() {
```

**2.** 将用户名的值捕获到`newName`变量中：

```javascript
var newName = $(this).val();
```

接下来，你将使用`post`方法进行验证。

**1.** 调用`post`方法，传入 PHP 脚本的 URL、表示正在填写的表单名称的数据以及`newName`变量：

```javascript
$.post('inc/peRegister.php', {
    formName: 'register',
    penewuser: newName
```

请注意，`post`方法传递的数据是`name: value`对的形式。在发送原始数据时，每个对中的值都会被引号括起来。像`newName`这样的变量不需要引号。

调用`inc/peRegister.php`脚本的结果将自动存储在`data`变量中，供后续处理。

**2.** 为`post`函数定义回调函数，并将`data`变量传递给该函数，以便处理结果：

```javascript
}, function(data){
```

PHP 函数仅返回基于查询的行数，该查询用于检查用户名是否存在于数据库中。

**3.** 设置一个变量来保存`data`变量中返回的信息：

```javascript
var usernameCount = data;
```

**4.** 创建一个条件语句，根据 AJAX 方法返回的数据显示或隐藏错误消息。你会认出这个条件语句的大部分内容，因为它与第 3 章中传递验证错误消息的方式类似：

```javascript
if(1 == usernameCount){
    $('#penewuser').next('.error').css('display', 'inline');
} else {
    $('#penewuser').next('.error').css('display', 'none');
}
```

图 4.3 用户名 FrankFarklestein 已被其他人使用。谁知道竟然有两个？

![Image](img/04-03.jpg)

**5.** 通过指定你期望服务器端函数返回的数据类型来关闭`post`函数：

```javascript
}, 'html');
});
```

如果 PHP 函数返回 1，则会显示错误`span`，如**图 4.3**所示。

注册函数需要提交用户数据，或者在提交仍有错误时通知用户。如果有错误，需要提示用户修正注册信息。

**1.** 通过将注册表单绑定到`submit`方法来启动注册函数：

```javascript
$('#registerForm').submit(function(e) {
```

变量`e`保存了事件对象的信息，在本例中是提交事件。

**2.** 由于你将使用 AJAX 提交表单，你不希望提交事件按正常方式执行。要阻止这种情况发生，你需要将事件设置为`preventDefault`：

```javascript
e.preventDefault();
```

图 4.4 模态提示，告知用户需要修正注册信息。在背景中可以看到用户名已被占用；必须更改。

![Image](img/04-04.jpg)

**3.** 序列化表单数据。序列化会创建一个带有标准 URL 编码表示法的文本字符串。对于大多数表单，这种表示法采用`key=value`对的形式：

```javascript
var formData = $(this).serialize();
```

**4.** 现在，你可以通过提供要提交的 URL 和序列化的表单数据，并设置回调函数来调用 jQuery AJAX `post`方法：

```javascript
$.post('inc/peRegister.php', formData, function(data) {
```

如果添加用户的查询成功，PHP 代码将返回 0。否则，它将返回一个更大的数字，表示无法添加用户。

**5.** 将 AJAX 函数返回的信息存储在`mysqlErrorNum`变量中：

```javascript
var mysqlErrorNum = data;
```

如果返回了错误，你需要向用户提供一个提示，让他们知道需要修正信息。该信息将像之前一样显示在模态窗口中。**图 4.4**显示了你接下来要设置的模态窗口。

**6.** 测试变量`mysqlErrorNum`的值，以设置条件语句：

```javascript
if(mysqlErrorNum > 0){
```

**7.** 如果`mysqlErrorNum`大于 0，则在网页的 body 中追加一个模态窗口：



```javascript
$('body').append('<div id="re" class="errorModal"><h3>There is an error with your registration</h3><p>Please correct your information and re-submit...</div>');
```

**8.** 像之前一样计算并应用新模态窗口的外边距：

```javascript
var modalMarginTop = ($('#re').height() + 60) / 2;
var modalMarginLeft = ($('#re').width() + 60) / 2;
$('#re').css({
    'margin-top' : -modalMarginTop,
    'margin-left' : -modalMarginLeft
});
```

**9.** 添加使模态窗口淡入的代码：

```javascript
$('#re').fadeIn().prepend('<a href="#" class="close_error"><img src="grfx/close_button.png" class="close_button" title="Close Window" alt="Close" /></a>');
```

**10.** 提供一种关闭包含错误警告的模态窗口的方法：

```javascript
$('a.close_error').live('click', function() {
    $('#re').fadeOut(function() {
        $('a.close_error, #re').remove();
    });
});
```

**11.** 如果没有返回错误，则淡出注册窗口并清除表单：

```javascript
} else {
    $('#registerWindow, #modalShade').fadeOut(function() {
        $('#registerForm input[input*="pe"]').val('');
    });
}
```

**12.** 通过提供你期望 PHP 函数返回的数据类型来关闭 `post` 方法：

```javascript
}, 'html');
});
```

## 用户登录

在验证过程中，你需要做的最后一步是让用户能够登录到他们的账户。

登录函数的 jQuery 代码几乎与注册函数相同，因此我将完整呈现：

```javascript
$('#loginForm').submit(function(e){
    e.preventDefault();
    var formData = $(this).serialize();
    $.post('inc/peRegister.php', formData, function(data) {
        var returnValue = data;
        if(1 == returnValue){
            $('#loginWindow, #modalShade').fadeOut(function() {
                $('#loginForm input[name*="pe"]').val('');
                window.location = "4-2.php";
            });
        } else {
            $('body').append('<div id="li" class="errorModal"><h3>There is an error with your login</h3><p>Please try again...</div>');
            var modalMarginTop = ($('#li').height() + 60) / 2;
            var modalMarginLeft = ($('#li').width() + 60) / 2;
            $('#li').css({
                'margin-top' : -modalMarginTop,
                'margin-left' : -modalMarginLeft
            });
            $('#li').fadeIn().prepend('<a href="#" class="close_error"><img src="grfx/close_button.png" class="close_button" title="Close Window" alt="Close" /></a>');
            $('a.close_error').live('click', function() {
                $('#li').fadeOut(function() {
                    $('a.close_error, #li').remove();
                });
            });
        }
    }, 'html');
});
```

图 4.5 登录成功后显示用户的账户页面。

![Image](img/04-05.jpg)

如果登录成功，浏览器将加载`chap4/4-2.php`（**图 4.5**），即用户的账户页面。

现在你已经熟悉了基本的 jQuery AJAX，接下来我们将学习如何使用 jQuery AJAX 函数来更新浏览器中的内容。

## 使用 AJAX 更新内容

在许多情况下，你会希望使用各种 jQuery AJAX 函数来更新可见的网站内容。有些内容更新可能基于当前用户的信息，另一些则可能基于任何用户发起的请求，例如网站访客执行的搜索信息。

让我们来看一些使用 jQuery 的 AJAX 方法更新内容的技术。

### 基于当前用户获取内容

即使你只开发过很短时间的网站，也很可能知道 URL 中的查询字符串。除非网站开发者使用了隐藏字符串的方法，否则你可能见过类似这样的内容：

`http://www.website.com/?user=me&date=today`

问号之后的所有内容都是查询字符串，可以在向服务器发送 GET 请求时使用。每个项都以`name=value`对的形式设置，可以轻松地被 jQuery 和 PHP 等脚本语言解析。

> **注意：** 大多数表单使用 POST 方法向服务器请求数据，但 URL 仅限于 GET 方法。大多数 Web 开发者遵循这样的规则：仅在检索数据时使用 GET，在向服务器发送数据以触发服务器端更改时使用 POST。

GET 请求不仅限于 URL。你可以将 GET 用作表单方法或 AJAX 中的方法。jQuery 提供了一个简写方法调用来向服务器发起此类请求，方便起见，它被称为`get`。

1. 打开`chap4/4-2.php`，设置一个`get`函数，将当前用户的图片检索到 Web 浏览器中。与其将 jQuery 代码存储在另一个文件中并包含进来，不如使用一种略有不同的技术，这种技术在使用小型 jQuery 脚本时非常有用。

2. 找到闭合的`</body>`标签。就在该标签之前，将设置 jQuery AJAX `get`方法来检索用户的图片。首先插入 script 标签：

   ```html
   <script type="text/javascript">
   ```

3. 确保文档（当前网页的 DOM 信息）完全加载后，打开函数：

   ```javascript
   $(document).ready(function() {
   ```

4. 确保从数据库获取正确信息的第一个关键步骤是，将登录时设置的 cookie 值赋给一个 jQuery 可以使用的变量。cookie 中的信息是用户名：

   ```javascript
   var cookieUser = '<?php echo $_COOKIE['photoex'];?>';
   ```

5. 如前所述，`get`方法依赖于`name=value`对来正常工作。确保`get`请求将 cookie 数据作为`name=value`对发送到服务器：

   ```javascript
   $.get('inc/userPhoto.php', {photoUser: cookieUser},
   function(data){
   ```

6. 将返回的信息加载到`id`为`myPhotos`的`div`中：

   ```javascript
   $('#myPhotos').html(data);
   ```

7. 关闭`get`函数，并指定 PHP 脚本预期返回的数据类型。关闭后，设置闭合的`</script>`标签（`</body>`标签仅作参考）：

   ```javascript
   }, 'html');
   });
   </script>
   ```

   ```html
   </body>
   ```

8. 在从数据库获取照片之前，你需要创建照片表。因此，运行代码下载中`chap4/sql`文件夹内的`pephoto.sql`文件。该 SQL 文件还会为`chap4/photos`文件夹中的照片插入默认数据。

   在 PHP 文件`chap4/inc/userPhoto.php`中，SQL 查询使用了`photoUser`变量中包含的信息：

   ```php
   $getImg = "SELECT `imgName`,`imgThumb` ";
   $getImg .= "FROM `photoex`.`pephoto` ";
   $getImg .= "WHERE `username` = '".$_GET['photoUser']."' ";
   ```

   图 4.6：用户的照片以表格形式呈现。

   ![Image](img/04-06.jpg)

   用户的照片被检索出来并放入一个表格中供查看。结果如**图 4.6**所示。

将用户数据与`get`方法结合使用，对于需要显示用户特有数据的页面非常有效。那么，对于非用户特有的内容呢？`get`方法有一个很酷的小兄弟，叫做`load`。

### 基于请求加载内容

在 jQuery AJAX 简写方法中，`load`是从服务器检索信息最简单、最容易的方法。当你想要调用不需要像`get`或`post`方法那样传递数据的新信息时，它特别有用。`load`的语法也非常简洁：

```javascript
$('a[href="writeNew"]').click(function(e){
    e.preventDefault();
    $('#newArticle').load('inc/userWrite.php');
});
```

图 4.7：表单已加载到页面中，以便用户撰写新文章。

![Image](img/04-07.jpg)

点击“撰写”链接（**图 4.7**）会调用`load`函数，导致`chap4/inc/userWrite.php`被加载到`id`为`newArticle`的`div`中。

`load`还提供了另一个非常酷的功能：你可以用它只加载其他页面的部分内容。例如，要加载另一个页面中`id`为`part1`的`div`，语法如下：

```javascript
$('#newArticle').load('inc/anotherPage.html #part1');
```

能够加载页面部分内容，可以为你提供极大的设计和组织灵活性。

> **注意：** 在第 6 章“创建应用程序界面”中，你将看到一个示例，其中多个小部件包含在一个文件中，该文件将根据需要由`load`调用以完成界面。

并非每个网站都能使用 jQuery 提供的所有 AJAX 功能，因此我们在此将暂时放下 Photographer's Exchange 网站。我们将开发独立的示例来演示 jQuery AJAX 库中其他一些可用的功能和事件。

### 动态加载脚本

在某些情况下，你需要在网页和应用程序中一次性加载 JavaScript 或 jQuery 脚本。jQuery 提供了一个专门的 AJAX 简写方法来实现这一点，即`getScript`。

在这个示例中，你将使用`chap3/dvdCollection`中包含的代码，这是一个小型个人网站，旨在作为你拥有的所有 DVD 和蓝光光盘的目录。

有时你会想知道自己有多少张 DVD 和蓝光光盘，但每次使用网站时都加载执行计数并显示结果的脚本并不必要。jQuery 的`getScript`方法是加载不常用脚本的完美解决方案。

1. 创建一个名为`dvdcount.js`的脚本，并将其放在 DVD 收藏网站的`inc`目录中。这是`getScript`在被调用时将加载的脚本。

2. 包含文档就绪功能：

   ```javascript
   $(document).ready(function(){
   ```

3. 每部电影都包含在一个`class`为`dvd`的`div`中。将这些`div`的数量赋给变量`totalCount`：

   ```javascript
   var totalCount = $('.dvd').length;
   ```

4. 使用 jQuery 的`:contains`选择器来帮助统计收藏中光盘的类型。`:contains`选择器非常适合查找包含特定字符串的元素。这里用它来查找`h3`元素中的文本“DVD”或“Blu-ray”：

   ```javascript
   var dvdCount = $('h3:contains("DVD")').length;
   var brCount = $('h3:contains("Blu-ray")').length;
   ```

5. 设置模态窗口以向用户显示信息。这与第 2 章和第 3 章中使用的技术相同，因此我不再详细说明每个步骤：

   ```javascript
   var movieModal = '<div class="movieModal">Total Movies: '+totalCount+'<br />DVD: '+dvdCount+'<br />Blu-ray: '+brCount+'</div>';
   $('body').append(movieModal);
   ```

```javascript
var modalMarginTop = ($('.movieModal').height() + 40) / 2;
var modalMarginLeft = ($('.movieModal').width() + 40) / 2;
$('.movieModal').css({
    'margin-top' : -modalMarginTop,
    'margin-left' : -modalMarginLeft
});
```

模态框只会短暂弹出，然后淡出：

```javascript
$('.movieModal').fadeIn('slow', function(){
    $(this).fadeOut(2500, function() {
        $(this).remove();
    });
});
```

DVD 目录网站的主页面是`chap4/dvdCollection/4-5.php`。我们花点时间来设置它。

1. 输入页头信息：

   ```html
   <!DOCTYPE html>
   <html lang="en">
       <head>
           <meta charset="utf-8">
           <title>DVD 收藏目录</title>
           <link rel="stylesheet" href="css/dvd.css" type="text/css" />
   ```

2. 包含 jQuery 文件，以便所有交互都能正常运行：

   ```html
           <script type="text/javascript"
           src="inc/jquery-1.5.min.js"></script>
       </head>
   ```

3. 接下来设置 body：

   ```html
       <body>
       <h2>DVD 收藏目录</h2>
       <div class="menuContainer">
   ```

4. 仔细设置菜单部分，因为你会用这些元素来调用其他脚本：

   ```html
           <ul class="menu">
               <li id="add">添加</li>
               <li id="summary">摘要</li>
           </ul>
       </div>
       <br />
   ```

5. 设置用于容纳页面内容的 div：

   ```html
       <div class="content"></div>
   ```



## 6. 创建包含 jQuery 脚本的部分

这些脚本用于将信息加载到页面中，以及加载`chap4/dvdCollection/inc/getdvd.php`的函数。PHP 由 jQuery 的`load`方法调用，以获取 DVD 收藏的信息：

```html
<script type="text/javascript">
    $(document).ready(function(){
        $('.content').load('inc/getdvd.php');
```

图 4.8 点击“摘要”元素会加载并运行`dvdcount.js`脚本。

![Image](img/04-08.jpg)

## 7. 绑定`click`方法

将`click`方法绑定到`id`为`summary`的列表项上。这将调用`getScript`来运行之前创建的 jQuery 脚本`dvdcount.js`：

```javascript
        $('#summary').click(function() {
            $.getScript('inc/dvdcount.js');
        });
    });    
</script>
```

## 8. 关闭 HTML

```html
</body>
</html>
```

点击网页上的“摘要”元素会加载并运行`dvdcount.js`脚本，显示包含计数的模态窗口（图 4.8）。然后模态窗口会慢慢淡出。

你会发现，在许多情况下，动态加载和运行脚本可以增强你的网站和应用程序。

接下来，你将把注意力转向 jQuery 的许多 AJAX 扩展功能，并学习如何实际应用它们。

## 使用 jQuery 的 AJAX 扩展功能

除了简写方法之外，jQuery 还提供了许多有用的方法和辅助工具，让你能够高效地使用 AJAX。这些方法从底层接口到全局事件处理程序，只要应用得当，都能让你的程序和网站更高效。

让我们从底层接口开始，看看这些扩展功能。

### 使用底层接口

jQuery 的底层 AJAX 接口提供了最详细的 AJAX 函数实现方式。这种详细程度使得底层接口非常灵活，但由于所有可用的选项，也增加了额外的复杂性。

应对大量选项带来的复杂性的一种方法是使用一个方法来设置不经常更改的选项。看看最简单的底层接口`ajaxSetup`：

```javascript
$.ajaxSetup({
    url: ajaxProcessing.php,
    type: 'POST'
});
```

`ajaxSetup`方法允许你提供将用于每个 AJAX 请求的选项。你可以使用`ajaxSetup`设置所有可用的 AJAX 选项（超过 25 个！）。如果你需要重复向同一个 URL 发送 AJAX 请求，或者每次请求都使用相同的密码，这会非常方便。在许多情况下，开发者会将所有服务器端 AJAX 处理程序放在服务器上的同一个文件中。使用`ajaxSetup`可以缩短他们的 AJAX 调用，包括简写方法。根据当前的`ajaxSetup`示例，你的`post`方法可以这样配置：

```javascript
$.post({ data: formData });
```

你只需要向`post`函数提供要由`ajaxProcessing.php`处理的数据。使用`ajaxSetup`方法的一个优点是，你可以在单个 AJAX 调用中覆盖任何`ajaxSetup`选项。

你最常见到的底层接口是直接的`ajax`方法。它是简写方法所包装的函数，也是所有 jQuery AJAX 调用的核心。`ajax`方法能够接受所有可用于 jQuery AJAX 请求的选项。理解底层 AJAX 方法的最佳方式可能是将其与你之前使用的某个简写方法进行比较。下面是你用来检查用户名是否可用的`post`方法：

```javascript
$.post('inc/peRegister.php', {
    formName: 'register',
    penewuser: newName
}, function(data){
    var usernameCount = data;
    if(1 == usernameCount){
        $('#penewuser').next('.error').css('display', 'inline');
    } else {
        $('#penewuser').next('.error').css('display', 'none');
    }
}, 'html');
```

下面是使用 jQuery 底层`ajax`方法的相同请求：

```javascript
$.ajax({
    type: 'POST',
    url: 'inc/peRegister.php',
    data: 'formName=register&penewuser='+newName+'',
    success: function(data){
        var usernameCount = data;
        if(1 == usernameCount){
            $('#penewuser').next('.error').css('display', 'inline');
        } else {
            $('#penewuser').next('.error').css('display', 'none');
        }
    },
    dataType: 'html'
});
```

差异相当明显，例如声明 AJAX 应该使用的方法将信息传递给服务器（`type: 'POST'`），指定原始数据的格式（`data: 'formName=register&penewuser= '+newName+'`），以及确保成功方法被隐式定义（`success: function(data){...`）。

浏览 jQuery 的`ajax` API 文档[`api.jquery.com/jQuery.ajax`](http://api.jquery.com/jQuery.ajax)，查看所有可用于此方法的选项。

既然你可以向服务器发送信息并从服务器端进程接收信息，那么你需要确保用户知道正在发生 AJAX 操作。jQuery 提供了几个辅助函数，让你可以轻松做到这一点。

### 在 AJAX 调用前后触发事件

在许多情况下，你的 jQuery AJAX 函数会执行得非常快，以至于用户可能甚至不知道他们的操作已经达到了预期效果。在其他情况下，AJAX 过程可能很长，需要用户等待结果。jQuery 提供了四种方法让你可以随时通知用户：`ajaxStart`、`ajaxSend`、`ajaxComplete`和`ajaxStop`。

理解这四个函数的顺序很重要。在任何给定事件中，你可以调用任意数量的 AJAX 进程。因此，你可能不仅想知道第一个 AJAX 函数何时开始，还想知道每个后续 AJAX 方法何时被调用和完成。然后你可能需要记录所有 AJAX 调用都已完成。如果你将 jQuery AJAX 事件想象成图 4.9 中的项目堆栈，你就会看到 jQuery AJAX 引擎如何定义事件及其调用的顺序。

图 4.9 初始的 jQuery 事件由开发者堆叠起来，然后由 jQuery 的 AJAX 引擎排序和处理。

![Image](img/04-09.jpg)

让我们仔细看看如何通过在使用 DVD 收藏目录进行数据和文件提交事件时为用户提供视觉提示，来使用`ajaxStart`和`ajaxStop`方法。

1. 打开`chap4/4-6.php`。

在`4-6.php`中，你会看到一个表单（下一页的图 4.10），该表单接受用户输入并提供上传文件的方法。这种组合并不罕见，但需要你在编写 PHP 和 jQuery 处理数据传输和文件上传时格外小心。

图 4.10．用户填写以将电影添加到个人数据库的表单。

![Image](img/04-10.jpg)

两个 PHP 脚本将处理表单中提供的数据：一个用于电影封面图片上传（记住，这不是真正的 AJAX），另一个用于表单中的数据输入。

### PHP 脚本：文件上传

2. 创建一个名为`chap4/dvdCollection/inc/dvdcover.php`的文件，首先设置图片上传。

3. 设置封面图片的路径：

```php
$coverPath = "../cover_art/";
```

4. 确保文件正确提交且没有错误：

```php
if ($_FILES["movieCover"]["error"] == UPLOAD_ERR_OK) {
```

5. 设置变量以保存上传文件的信息（这与你在第 3 章中用于文件上传的技术相同）：

```php
$tmpName = $_FILES["movieCover"]["tmp_name"];
$coverName = $_FILES["movieCover"]["name"];
```

6. 创建用于检查上传文件扩展名的正则表达式：

```php
$regexFileExt = "/\.(jpg|jpeg|png)$/i";
```

7. 测试文件扩展名，看是否与正则表达式允许的扩展名匹配：

```php
if(preg_match($regexFileExt, $coverName)){
```

8. 通过检查文件的前几个字节，再次确认文件确实是正确的类型：

```php
$arrEXIFType = array(IMAGETYPE_JPEG, IMAGETYPE_PNG);
if(in_array(exif_imagetype($tmpName), $arrEXIFType)){
```

9. 设置文件的新名称和路径，并将其放入变量`$newCover`中：

```php
$newCover = $coverPath.$coverName;
```

10. 将正确命名的文件移动到其永久目录：

```php
move_uploaded_file($tmpName, $newCover);
```

现在你已经完成了文件上传的 PHP 脚本，可以创建将由 jQuery AJAX`post`方法调用的 PHP 脚本，以更新数据库。

### PHP 脚本：`postdvd.php`

1. 创建一个名为`postdvd.php`的文件，并将其存储在`chap4/dvdCollection/inc`文件夹中。

`postdvd.php`只包含两个操作：一个用于连接数据库，另一个用于运行执行数据库更新的查询。

2. 首先设置数据库连接（确保使用你为数据库设置的用户名和密码）：

```php
if(!$dbc = mysql_connect('localhost', 'username', 'password')){
    echo mysql_error() . "\n";
    exit();
}
```

3. 引入一个小的睡眠计时器来减慢进程。这将允许将要创建的 jQuery 函数中的`ajaxStart`显示动画加载图形（通常，数据库操作非常快——快到用户可能没有意识到发生了什么。）：

```php
sleep(2);
```

4. 创建 SQL 查询，该查询将接受来自 AJAX`post`方法的值，以更新数据库：

```php
$insertMovie = "INSERT INTO `dvdcollection`.`dvd` ";
$insertMovie .= "(`name`,`genre`,`format`,`description`,
![Image](img/ccc.jpg) `cover`) ";
$insertMovie .= "VALUES(";
$insertMovie .= "'".$_POST['movieName']."',";
$insertMovie .= "'".$_POST['movieGenre']."',";
$insertMovie .= "'".$_POST['movieFormat']."',";
$insertMovie .= "'".$_POST['movieDescription']."',";
$insertMovie .= "'cover_art/".$_POST['movieCover']."' ";
$insertMovie .= ")";
```

---

> **注意**
>
> 确保在你的数据库平台上运行 SQL 脚本`chap4/dvdCollection/sql/create_collection_table.sql`，以设置并填充 DVD 收藏的表。

---

5. 调用`mysql_query`函数来运行 SQL 查询：

```php
if(!($movieInfo = mysql_query($insertMovie, $dbc))){
    echo mysql_error();
    echo mysql_errno();
    exit();
}
```

完成 PHP 脚本后，你现在可以将注意力转向 jQuery 函数。所有 jQuery 函数都将放入文件`inc/movieUp.js`中。

### jQuery 函数

1. 通过定义`ajaxStart`方法开始文件：

```javascript
$('body').ajaxStart(function(){
```

一旦发出 AJAX 请求，就会调用`ajaxStart`函数。该方法可以绑定到 DOM 中可用的任何元素，这里绑定到`body`元素。你可以在`ajaxStart`方法中定义任何你想要的过程。

2. 对于此文件和数据的上传，创建一个模态弹出窗口，为用户提供视觉提示，表明正在发生某些操作：

```javascript
var waitingModal = '<div class="waitingModal">
![Image](img/ccc.jpg) <img src="grfx/loading.gif" border="0" /></div>';
$('body').append(waitingModal);
var modalMarginTop = ($('.waitingModal').height() + 40) / 2;
var modalMarginLeft = ($('.waitingModal').width() + 40) / 2;
$('.waitingModal').css({
    'margin-top' : -modalMarginTop,
    'margin-left' : -modalMarginLeft
});
$('.waitingModal').fadeIn('slow');
```

创建模态窗口的技术与你之前在本书中使用过的技术相同。

3. 将`ajaxStop`方法绑定到`body`元素（记住，像`ajaxStart`和`ajaxStop`这样的方法可以绑定到任何元素）。当 AJAX 请求完成时，你将清除表单并从视图中移除模态窗口，以便用户知道过程已结束：

```javascript
$('body').ajaxStop(function(){
```

4. 清除表单元素，以便用户可以使用表单添加另一部电影。就像使用`ajaxStart`一样，你可以在`ajaxStop`函数中定义任何过程：

```javascript
$('#addMovie input[name*="movie"]').val('');
$('#addMovie textarea').val('');
```

在选择要清除的表单元素时，请确保 jQuery 选择器非常具体。例如，仅使用`$('#addMovie input')`也会清除表单的按钮，这会让用户感到困惑。

5. 淡出模态指示器并将其从 DOM 中移除。这是`ajaxStop`方法中定义过程的最后一部分：

```javascript
$('.waitingModal').fadeOut('slow', function(){
    $(this).remove();
});
```

6. 通过将表单`addMovie`绑定到`submit`方法来开始表单处理程序：

```javascript
$('#addMovie').submit(function(){
```

7. 使用第 3 章中定义的`iframe`方法上传图片：

```javascript
var iframeName = ('iframeUpload');
var iframeTemp = $('<iframe name="'+iframeName+'"
![Image](img/ccc.jpg) src="about:blank" />');
iframeTemp.css('display', 'none');
$('body').append(iframeTemp);
$(this).attr({                    
    action: 'inc/dvdcover.php',
    method: 'post',
    enctype: 'multipart/form-data',
    encoding: 'multipart/form-data',
    target: iframeName
});
```

图 4.11．`ajaxStart`方法已调用等待指示器。

![Image](img/04-11.jpg)

8. 图片上传完成后，从 DOM 中移除`iframe`：

```javascript
setTimeout(function(){
    iframeTemp.remove();
}, 1000);
```

9. 准备要在`post`方法中使用的数据。由于`textarea`中的信息无法使用常规的 jQuery 方法序列化，因此创建一个文本字符串，通过将信息设置为*name=value*对，使`textarea`值看起来像是被序列化了一样：



```javascript
var coverData = '&movieCover=' +
![Image](img/ccc.jpg) $('input[name="movieCover"]').val();
```

**10.** 序列化表单的其余数据：

```javascript
var formData = $(this).serialize();
```

**11.** 表单数据经过`serialize`函数处理后，将两个字符串连接到`uploadData`变量中：

```javascript
var uploadData = formData + coverData;
```

**12.** 调用 jQuery AJAX 简写方法`post`上传数据：

```javascript
$.post('inc/postdvd.php', uploadData);
});
```

当电影数据表单提交时，jQuery AJAX 引擎会检测到过程中发生了`post`操作，从而触发`ajaxStart`方法。**图 4.11** 展示了由`ajaxStart`调用的模态加载指示器。

一旦`post`过程完成，`ajaxStop`方法被触发，导致模态等待指示器淡出。

现在你已经学会了处理 AJAX 调用及其返回的数据，接下来需要学习如何处理 Web 上增长最快的数据类型之一——JSON。

---

### 提示

如果你需要动画图形来向用户指示后台正在发生某些操作，请查看[www.ajaxload.info](http://www.ajaxload.info)。在那里你可以生成多种不同颜色的动画图形。

---

## 使用 JSON

JSON（JavaScript 对象表示法）已成为一种流行且轻量级的方式，用于在互联网上传输各种用途的数据包。在许多方面，JSON 比 XML 更受欢迎，因为它能快速高效地传递数据。JSON 数据可以轻松地与 jQuery AJAX 简写方法配合使用，该方法专门设计用于处理 JSON 数据类型，即`getJSON`。

那么 JSON 到底是什么？

要理解 JSON，你需要先了解 JavaScript 的对象字面量表示法。对象字面量表示法是一种显式创建对象的方式，也是设置 JavaScript 对象最健壮的方法。以下是一个示例：

```javascript
var person = {
    name: "Jay",
    occupation: "developer",
    stats: ["blonde", "blue", "fair"],
    walk: function () {
        alert(this.name + 'is walking');
    }
};
```

`person`对象被字面定义为名称-值对，包括一个嵌套数组（`stats`）和一个使对象行走的方法。这是一种非常简洁的描述对象的方式。

以下命令与`person`对象交互：

```javascript
person.walk(); // 弹出 'Jay is walking'

alert(person.stats[1]); // 弹出 'blue'
```

JSON 是对象字面量表示法的一个子集，本质上是描述对象的名称-值对。一个 JSON 数组可以包含多个对象。成功使用 JSON 的关键是确保其格式正确。JSON 必须具有匹配数量的开闭方括号和花括号（括号顺序必须正确）；名称-值对中的名称和值必须正确引用；并且每个名称-值对之间必须用逗号分隔。

为了说明这一点，请看`person`对象的 JSON：

```javascript
var myJSONobject = {
    "person": [{
        "name": "Jay",
        "occupation": "developer",
        "stats": [{
            "hair": "blonde",
            "eyes": "blue",
            "skin": "fair"
        }]
    }]
};
```

需要注意的是，JSON 对象不包含任何可执行的方法或函数。JSON 特意将这些排除在表示法之外，因为 JSON 仅作为传输数据的载体。

### 设置 JSON 请求

自互联网诞生以来，Twitter 无疑已成为最受欢迎的社交媒体之一。Twitter 提供了一个 API，供那些希望将 Twitter 功能扩展到自己的网页和应用程序的人使用。Twitter API 最流行的用途之一是在个人网站和博客中包含最近的推文。

利用 API 可以简单也可以复杂，完全取决于你的需求。让我们构建一个简单的小部件，获取你最近的十条推文并嵌入到网页中。

推文数据以 JSONP 格式从 Twitter 返回。JSONP 被称为“带填充的 JSON”。在正常情况下，你无法向请求来源域之外的域发出 AJAX 请求（下一页的**图 4.12**）。JSONP 依赖于 JavaScript 的一个特性：`<script>`元素允许进行跨域请求。

**图 4.12.** 进行跨域请求的唯一方法是使用 JSONP。

![Image](img/04-12.jpg)

为了实现这一点，JSON 必须在一个函数中返回。使用之前创建的 JSON 对象，JSONP 看起来像这样：

```javascript
myJSONfunction({
    "person": [{
        "name": "Jay",
        "occupation": "developer",
        "stats": [{
            "hair": "blonde",
            "eyes": "blue",
            "skin": "fair"
        }]
    }]
});
```

如果现在看起来像乱码，别担心；当你逐步构建从 Twitter 获取 JSON 数据的函数时，一切都会变得清晰。

让我们从头开始构建整个文件，包括 CSS。

**1.** 在`chap4`文件夹中创建一个名为`4-7.php`的文件。

**2.** 设置`DOCTYPE`并包含基本的`head`、`title`和字符集声明：

```html
<!DOCTYPE html>
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
        <title>Twitter 小部件</title>
```

**3.** 提供将要使用的 jQuery 源文件的引用。确保路径正确；本例中路径为`inc/jquery-1.5.2.min.js`：

```html
<script type="text/javascript" src="inc/jquery-1.5.min.js"></script>
```

**4.** 为 Twitter 小部件创建样式信息：

```html
<style type="text/css">
    body {
        background-color: #FFFFCC;
    }

    #tw {
        position: relative;
        width: 350px;
        left: 50%;
        margin-left: -175px;
    }

    .tweet {
        font-family: "Lucida Grande", "Arial Unicode MS", sans-serif;
        width: 350px;
        background-color: #99FFCC;
        padding: 5px;
        border-right: 2px solid #66CC99;
        border-bottom: 3px solid #66CC99;
        margin-bottom: 2px;
    }
</style>
```

**5.** 关闭页面的`head`部分：

```html
</head>
```

小部件的`body`部分非常简单：添加一个`id`为`tw`的`div`，推文将被追加到其中：

```html
<body>
    <div id="tw"></div>
```

获取推文的 jQuery 脚本非常简短，但需要你注意细节。我们将使名称和话题标签可点击，使其具有与 Twitter 网站上相同的功能。推文中包含的任何链接也将可点击，并打开一个新的浏览器窗口显示信息。

**1.** 通过打开`script`标签并插入文档就绪函数来启动 jQuery 函数：

```javascript
<script type="text/javascript">
    $(document).ready(function() {
```

**2.** 创建访问 Twitter 的 URL 并将其存储在变量`twitterURL`中：

```javascript
var twitterURL = 'http://twitter.com/statuses/user_timeline.json?screen_name=YOUR_TWITTER_USER_NAME&count=10&callback=?';
```

请务必将`YOUR_TWITTER_USER_NAME`替换为你实际的 Twitter 用户名。确保 URL 格式正确，包含查询字符串（名称=值对），这一点非常重要，因为`getJSON`将在请求中使用这些参数。向 Twitter 发送三个选项：你的 Twitter`screen_name`、要返回的推文数量`count`，以及最重要的`callback`。正是`callback`选项让 Twitter 知道你期望返回的数据是 JSONP。

**3.** 一旦 URL 形成，通过发送 URL 并定义`getJSON`的回调选项来打开`getJSON`请求方法：

```javascript
$.getJSON(twitterURL, function(data) {
```

---

### 注意

查询字符串的回调选项与`getJSON`请求的回调不同。

---

**4.** 此时 JSONP 已从 Twitter 返回。设置一个循环遍历函数中包含的数据。将数据视为名为`item`的数组的成员：

```javascript
$.each(data, function(i, item) {
```

**5.** 将推文包含在一个名称-值对中，名称为`text`。将此项目赋值给变量`tweetText`：

```javascript
var tweetText = item.text;
```

**6.** 使用正则表达式定位推文中的 URL、@ 标签和井号（#）标签，以便对每个标签进行适当处理。首先查找 URL：

```javascript
tweetText = tweetText.replace(
    /http:\/\/\S+/g,
    '<a href="$&" target="_blank">$&</a>'
);
```

正则表达式`/http:\/\/\S+/g`匹配以`http://`开头、以空格结尾的文本，这通常表示一个 URL。`/g`（全局）表示匹配`tweetText`字符串中的所有 URL。通过将 URL 替换为包含 URL 作为`href`和链接文本的锚标签，将 URL 转换为链接。在 JavaScript 中，`$&`属性包含正则表达式最后匹配的项目。由于 URL 是最后匹配的项目，因此可以使用`$&`属性将其替换到锚标签中。

**7.** Twitter 在用户名前加上@符号。因此，搜索`tweetText`中以@符号开头的单词：

```javascript
tweetText = tweetText.replace(
    /(@)(\w+)/g,
    ' $1<a href="http://twitter.com/$2" target="_blank">$2</a>'
);
```

这里，正则表达式`/(@)(\w+)/g`表示所有以@符号开头的单词都被替换为适当的锚标签，以便为用户推文打开浏览器窗口。`$1`和`$2`包含每个括号中匹配的信息，用于在替换文本中包含这些匹配项。

**8.** 现在将注意力转向井号标签，并使用类似于替换@符号的技术：

```javascript
tweetText = tweetText.replace(
    /(#)(\w+)/g,
    ' $1<a href="http://search.twitter.com/search?q=%23$2" target="_blank">$2</a>'
);
```

**9.** 一旦`tweetText`被完全处理以插入所有锚标签，将其放入一个`div`中。然后将新的`div`追加到作为页面原始内容一部分而设置的现有`div`（`id="tw"`）中：

```javascript
$("#tw").append('<div class="tweet">' + tweetText + '</div>');
```

**10.** 关闭页面的 jQuery 函数和 HTML 标签：

```html
});
});
});
</script>
</body>
</html>
```

**图 4.13.** Twitter 小部件检索你最近发布的几条推文。

![Image](img/04-13.jpg)

**11.** 将页面上传到服务器，并在浏览器中加载页面。你应该会看到**图 4.13**中所示的结果。

由于客户端和服务器之间（包括不受你控制的服务器）有大量数据来回传输，因此担心你和网站访问者在 AJAX 请求中发送的信息的安全性是很自然的。接下来我们来解决这些问题。

## 保护 AJAX 请求

网站和应用程序的一个棘手问题是，用户可能会无意或故意通过你的网站提交可能对数据库和服务器造成损害的数据。尽可能采取措施防止输入和传输错误或格式错误的数据非常重要。

其中一些步骤已经介绍过，包括使用正则表达式引导用户输入正确类型的数据，以及确保为每个网站访问者唯一设置 cookie。正如一位年长且更有智慧的导师对我说的：“用这种方式锁门只能阻止诚实的人翻越栅栏。”

即使表单字段中使用了正则表达式，你仍然无法阻止数据的传输，因为表单仍然可以提交。那么，你可以采取哪些措施来防止用户提交潜在有害的数据呢？

- 通过“灰显”表单上的提交按钮来阻止表单提交，直到每个表单字段的所有正则表达式规则都满足为止。
- 使用 cookie 根据注册信息唯一标识用户（更准确地说，是用户的计算机），并在传输用户提供的数据期间对照数据库检查 cookie 数据。
- 在后端处理过程中清理用户提供的数据，确保数据不包含有害的语句或字符。
- 通过安全连接（HTTPS [超文本传输协议安全]）传输数据，以防止外部人员“嗅探”进出 Web 浏览器的信息。

---

### 注意

有关 HTTPS 的更多信息，请访问电子前哨基金会的网站：[www.eff.org/https-everywhere](http://www.eff.org/https-everywhere)。

---

这些技术应相互结合使用，为用户和网站所有者提供最安全的体验。让我们逐步了解其中一些技术。

### 阻止表单提交

让我们回到摄影师交流网站，对包含注册表单的 HTML 文件以及支持该表单的 jQuery 脚本进行一些更改。

**1.** 打开`chap4/4-2.php`，找到脚本中包含 jQuery 脚本的部分。你会在`head`标签之间找到这些包含声明。

**2.** 将以下高亮行更改为指向更新后的`jqpe.js`文件：

```html
<script type="text/javascript" src="inc/jquery-1.5.min.js"></script>
<script type="text/javascript" src="inc/jquery.ez-bg-resize.js"></script>
<script type="text/javascript" src="inc/spritenav.js"></script>
<script type="text/javascript" src="inc/carousel.js"></script>
<script type="text/javascript" src="inc/jqpe.js"></script>
<script type="text/javascript" src="inc/peAjax.js"></script>
```

更改后，该行将如下所示：

```html
<script type="text/javascript" src="inc/jqpeUpdated.js"></script>
```

**3.** 将文件另存为`chap4/4-8.php`。

**4.** 打开`chap4/inc/jqpe.js`并将其另存为`chap4/inc/jqpeUpdated.js`。添加错误计数函数的代码。首先初始化`$submitErrors`变量：

```javascript
var submitErrors = 0;
```



**5.** 声明一个名为`errorCount`的函数：

```javascript
function errorCount(errors) {
```

**6.** 将参数变量`errors`设置为等于`submitErrors`变量：

```javascript
    errors = submitErrors;
```

**7.** 如果错误计数为零，则希望启用提交按钮。因此，从按钮中移除`disabled`属性。使用 jQuery 属性选择器选择正确的按钮：

```javascript
    if(0 == errors){
        $('input[type="submit"][value="Register"]').
        removeAttr('disabled');
```

**8.** 如果错误计数不为零，则提交按钮将被禁用。使用相同的选择器语法，向按钮添加`disabled`属性：

```javascript
    } else {
        $('input[type="submit"][value="Register"]').
        attr('disabled','disabled');
    }
```

**9.** 关闭函数：

```javascript
}
```

函数就位后，你需要对之前创建的密码和电子邮件验证函数进行一些更改。

**1.** 在`jqpeUpdated.js`中找到以注释`/*make sure password is not blank */`开头的密码验证函数。插入此处高亮显示的两行新代码：

```javascript
/* 确保密码不为空 */
    $(function() {
        var passwordLength = $('#penewpass').val().length;
        if(passwordLength == 0){
            $('#penewpass').next('.error').css('display',
            'inline');
            errorCount(submitErrors++);
```

```javascript
$('#penewpass').change(function() {
    $(this).next('.error').css('display', 'none');
    errorCount(submitErrors--);
});
```

如果密码为空（长度为零），则调用`errorCount`函数，并将`submitErrors`变量增加 1。

`errorCount(submitErrors++);`

输入密码后，错误被清除，错误计数可以通过递减`submitErrors`来减少：

`errorCount(submitErrors--);`

**2.** 找到电子邮件验证函数。它以注释`/* validate e-mail address in register form */`开头。在以下高亮指示的位置添加对`errorCount`函数的相同调用：

```javascript
/* validate e-mail address in register form */
$(function(){
    var emailLength = $('#email').val().length;
    if(emailLength == 0){
        $('#email').next('.error').css('display',
        'inline');
        errorCount(submitErrors++);
        $('#email').change(function() {
        var regexEmail = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+
        \.[a-zA-Z]{2,4}$/;
        var inputEmail = $(this).val();
        var resultEmail = regexEmail.test(inputEmail);
        if(resultEmail){
            $(this).next('.error').css('display', 'none');
            errorCount(submitErrors--);
               }
    });
}
});
```

图 4.14. 注册按钮呈灰色显示。在所有错误清除之前，用户无法使用该按钮。

![Image](img/04-14.jpg)

当页面首次加载时，`submitErrors`会被递增两次——每个验证函数各一次。表单填写前的总错误计数为 2。由于`submitErrors`的值为 2，提交按钮被禁用，如**图 4.14**所示。

当每个函数清除其错误后，`submitErrors`变量递减，直到最终达到零。当`submitErrors`的值为零时，`errorCount`函数会移除提交按钮的禁用属性，表单即可正常提交。

此技术可应用于任何需要验证的表单字段，但仅凭此还不足以阻止恶意用户试图攻击你的网站。让我们看看另一种可以添加到网站应用程序模型中的技术，即为每个用户提供 cookie。

### 使用 COOKIE 识别用户

给用户 cookie 听起来很愉快。但实际上，这意味着你想识别用户，以确保他们有权使用你网站上的表单和数据。你不应该做的是将敏感信息放入 cookie 中。Cookie 可能被窃取、读取和利用。

就个人而言，我不太喜欢“记住我 cookie”，因为 cookie 过期的时间越长，潜在恶意用户就有更多时间获取并利用 cookie 中的信息。我更希望当用户关闭浏览器时 cookie 就过期。这样可以减少有人登录用户计算机并访问相同站点以获取信息，或将 cookie 复制到其他位置的机会。

那么应该在 cookie 中存储什么？一种非常有效的技术是在 cookie 中存储一个唯一的令牌，该令牌可以在用户当前会话期间与用户匹配。让我们修改 Photographer's Exchange 的登录过程，在用户的数据库记录中存储一个令牌。每次用户登录网站时，令牌都会更改，并且你将使用该令牌根据需要检索用户的其他数据。

**1.** 打开`chap4/inc/peRegister.php`，找到以注释`/* if the login is good */`开头的部分。你将插入新代码，以创建令牌并将其保存到新创建的数据库列中。

**2.** 需要添加的第一行代码创建一个唯一值用于令牌化。将`$_POST['pename']`中包含的用户名与 PHP 的`time`函数生成的时间戳拼接起来。PHP 的`time`函数返回自 1970 年 1 月 1 日以来的秒数。将其存储在变量`$tokenValue`中，如下面的高亮行所示：

```php
/* if the login is good */
if(1 == $loginCount){
    if(isset($_POST['remember'])){
    $tokenValue = $_POST['pename'].time("now");
```

**3.** 通过使用 MD5（消息摘要算法）哈希对`$tokenValue`进行哈希处理，修改要存储在`$peCookieValue`中的信息：

```php
    $peCookieValue = hash('md5', $tokenValue);
    $peCookieExpire = time()+(60*60*24*365);
    $domain = ($_SERVER['HTTP_HOST'] != 'localhost') ?
    $_SERVER['HTTP_HOST'] : false;
    setcookie('photoex', $peCookieValue, $peCookieExpire, '/',
    $domain, false);
    echo $loginCount;
} else {
```

MD5 哈希算法是一种加密哈希，它接受一个字符串并将其转换为 32 位十六进制数。这个十六进制数通常非常唯一，并且通过将`time`函数与用户名结合使用，使其更加唯一。

**4.** 在未设置“记住我”值的代码部分进行相同的修改：

```php
    $tokenValue = $_POST['pename'].time("now");
    $peCookieValue = hash('md5', $tokenValue);
    $peCookieExpire = 0;
    $domain = ($_SERVER['HTTP_HOST'] != 'localhost') ?
    $_SERVER['HTTP_HOST'] : false;
    setcookie('photoex', $peCookieValue, $peCookieExpire, '/',
    $domain, false);
    echo $loginCount;
```

**5.** 添加用于使用新值更新数据库的代码：

```php
    $updateUser = "UPDATE `photoex`.`peuser` ";
    $updateUser .= "SET `token` = '".$peCookieValue."' ";
    $updateUser .= "WHERE `username` = '".$_POST['pename']."' ";
    if(!($updateData = mysql_query($updateUser, $dbc))){
        echo mysql_errno();
        exit();
    }
```

图 4.15. cookie 的内容被圈出，潜在的 cookie 窃贼被挫败！

![Image](img/04-15.jpg)

**6.** 打开`chap4/4-8.php`，使用已知的有效用户名和密码登录网站。Cookie 将使用令牌设置，令牌信息将存储在数据库中。你可以使用浏览器的内置 cookie 查看器（对于**图 4.15**，我在 Firefox 浏览器中使用了“工具 > 页面信息 > 安全 > 查看 Cookie”）来检查存储在 cookie 中的值。

使用令牌的值，你可以检索有关用户的所需信息，以便将数据输入表单或显示相应的照片。接下来，让我们看看如何清理用户提供的数据。

### 清理用户提供的数据

为确保用户提供的数据到达服务器后安全无虞，你可以采取的额外步骤是使用客户端脚本语言来确保数据得到安全可靠的处理。

一个不太友善的访问者可能会访问你的网站，并复制你可见的网页和功能。一旦复制，就可以修改你的 jQuery 脚本，移除你为数据设置的一些控制（例如正则表达式）。你的第一道防线是在服务器端脚本中复制这些控制。

**1.** 以电子邮件验证为例，打开`peRegister.php`（`chap4/inc/peRegister.php`）进行修改。

**2.** 找到以注释`/* if the registration form has a valid username & password insert the data */`开头的代码部分，并提供以下正则表达式：

```php
$regexEmail = '/^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/';
```

这与 jQuery 函数中用于验证注册表单中电子邮件地址的正则表达式相同。

**3.** 使用 PHP 的`preg_match`函数测试提交的值是否匹配正则表达式：

```php
preg_match($regexEmail, $_POST['email'], $match);
```

**4.** 测试结果（匹配则为 1，不匹配则为 0）被存入`preg_match`函数中声明的变量`$match`中。利用此结果修改`$_POST['email']`变量：

```php
if(1 == $match){
    $_POST['email'] = $_POST['email'];
} else {
    $_POST['email'] = 'E-MAIL ADDRESS NOT VALID';
}
```

来自`$_POST['email']`变量的数据被用于将数据插入数据库的 SQL 查询中。

许多语言（如 PHP）都包含专门用于数据清洗的函数。我们来看两个 PHP 函数，它们可以在数据进入数据库之前对其进行清理：`htmlspecialchars()`和`mysql_real_escape_string()`。

清理以 HTML 格式提交的信息，只需将数据包裹在 PHP 的`htmlspecialchars`函数中即可。给定如下表单：

```html
<form name="search" action="inc/search.php" method="post">
    <label class="label" for="pesearch">Search For: </label>
    <input type="text" name="pesearch" id="pesearch" size="64" /><br />
    <label class="label">&nbsp;</label>
    <input type="submit" value="Search" />
    <input type="reset" value="Clear" />
</form>
```

PHP 的`htmlspecialchars`函数会替换某些字符，并返回：

```text
&lt;form name=&quot;search&quot; action=&quot;inc/search.php&quot;
method=&quot;post&quot;&gt;&lt;label class=&quot;label&quot;
for=&quot;pesearch&quot;&gt;Search For: &lt;/label&gt;&lt;input
type=&quot;text&quot; name=&quot;pesearch&quot;
id=&quot;pesearch&quot; size=&quot;64&quot; /&gt;&lt;br
/&gt;&lt;label class=&quot;label&quot;&gt;&amp;nbsp;&lt;
/label&gt;&lt;input type=&quot;submit&quot;
value=&quot;Search&quot; /&gt;&lt;input type=&quot;reset&quot;
/&gt;&lt;/form&gt;
```

以下字符已被更改：

- 与号（&）变为`&amp;`
- 双引号（"）变为`&quot;`
- 单引号（'）变为`&#039;`
- 小于号（<）变为`&lt;`
- 大于号（>）变为`&gt;`

使用 PHP 的`htmlspecialchars`函数可以让用户提供的 HTML 数据在网站和数据库中更安全地使用。PHP 也提供了一个反向函数`htmlspecialchars_decode()`。

同样简单的是，使用 PHP 的`mysql_real_escape_string`函数可以防止可能的 SQL 注入攻击。该函数通过转义任何字符串中的特定字符来工作。恶意访问者可能会尝试在表单字段中输入 SQL 查询，希望它被执行。请看下面的例子，访问者试图通过更改数据库管理员密码来获取数据库的管理员权限。黑客还假设了一些常见词汇来尝试确定表名：

```sql
UPDATE `user` SET `pwd`='gotcha!' WHERE `uid`='' OR `uid` LIKE
'%admin%'; --
```

如果这个 SQL 查询被输入到用户名字段中，你可以通过使用`mysql_real_escape_string`来阻止它运行：

```php
$_POST['username'] = mysql_real_escape_string($_POST['username']);
```

这将`$_POST['username']`的值设置为：

```sql
UPDATE `user` SET `pwd`=\'gotcha!\' WHERE `uid`=\'\' or `uid` like
\'%admin%\'; --
```

由于查询被正确处理且特定字符被转义，它会被插入数据库而不会造成任何危害。

另一种可以使用的技术是保护客户端和服务器之间数据传输的安全。接下来我们重点讨论这一点。

### 安全传输数据

另一个可以考虑的选项是为你的网站或应用程序获取安全证书，然后将网站置于 HTTPS 安全协议中。这非常有用，因为潜在攻击者无法轻易读取客户端和服务器之间传输的数据，但成本可能较高。



所有网站数据都根据安全证书提供的密钥进行加密。网站信息通过安全套接层（SSL）来回传输。SSL 是一种用于 Web 的加密通信协议。一旦数据到达传输的任一端，它就会被正确解密以供使用。如果你使用过 URL 以`https://`开头的网站，或者在浏览器中看到过锁形图标，那么你就使用过以这种方式保护的网站。许多金融机构和商业网站都使用 HTTPS 来确保数据安全传输。

---

### 提示

你可以在电子前哨基金会的网站[`www.eff.org/https-everywhere`](http://www.eff.org/https-everywhere)上了解更多关于 HTTPS 和 SSL 的信息。

---

## 总结

在本章中，你学习了如何将 jQuery AJAX 的简写方法（如`.get()`、`.post()`和`.load()`）与服务器端脚本结合，为 HTML 表单增加响应性。本章还介绍了从服务器获取响应的方法，你可以用 jQuery 处理这些响应，以更改页面内容或向网站访问者提供有意义的消息。

你还了解了 jQuery 底层 AJAX 方法，这些方法用于与 Web 服务器进行更复杂的交互。最后，你学习了 JavaScript 对象表示法（JSON），以及如何使用 jQuery 的 JSON 方法从 Twitter 或 Flickr 等服务中检索数据，用于你将构建的网站。

如果你对 jQuery 小部件的初次体验意犹未尽，那么你很幸运！第 5 章，“应用 jQuery 小部件”，将探讨各种形状和大小的部件，包括 jQuery UI 项目中的几个。除了 jQuery UI 项目中的部件，你还将学习如何使用他人开发的插件，以及如何创建（并发布）自己的插件与他人分享。继续阅读吧，麦克达夫！

# 5. 应用 jQuery 小部件

jQuery 非常容易通过功能进行扩展，以至于 jQuery 设计者和开发者已经编写了数百个扩展（插件），从极其简单实用到极其复杂专业。

jQuery UI（用户界面）库是一组用于交互、小部件和视觉效果的核心插件，它作为 jQuery 的一个独立分支持续开发。使用 jQuery UI 库将使你的编程生活更加轻松，并为你提供有效向网站和应用程序添加高级功能的工具。

在本章中，你将学习 jQuery UI 中一些非常有用的部件，以及由设计师和开发者社区推广的一些最有效和最酷的插件。此外，我将引导你完成创建自己插件的步骤。

## 使用 jQuery UI 小部件

图 5.1 可用于配置与 jQuery UI 小部件一起使用的自定义样式表的 ThemeRoller 选项的一部分。

![Image](img/05-01.jpg)

jQuery UI 是一个完整的库包，用于让交互式小部件变得生动。*小部件*是一个独立的包或工具，为你的 Web 界面添加特定功能——例如选项卡或可从中选择日期的日历。

---

### 注意

小部件是 jQuery UI 的组件，而插件是开发者创建和维护的小部件的术语。

---

作为额外奖励，你可以从 jQuery UI 网站图库（[`www.jqueryui.com`](http://www.jqueryui.com)）下载预配置的样式（包含图片和图标）。你也可以使用 jQuery UI 的 ThemeRoller 自定义 CSS，如**图 5.1**所示。

### 自定义 jQuery UI

jQuery UI ThemeRoller（可在[`jqueryui.com/themeroller`](http://jqueryui.com/themeroller)获取）允许你设置样式表的 CSS 规则，该样式表将与 jQuery UI 库一同下载。在 ThemeRoller 中设置的 CSS 规则用于为 jQuery UI 小部件提供所需的信息，使其能够与你的网站视觉上融为一体。

图 5.2. 当信息输入到 ThemeRoller 小部件时，jQuery UI ThemeRoller 会更改元素的样式。

![Image](img/05-02.jpg)

一旦你为网站或应用程序选定了调色板，就可以轻松地将该调色板和样式信息转移到 jQuery UI ThemeRoller（图 5.2）。你可以为字体设置、颜色以及构成 jQuery UI 小部件的许多单独元素提供规则。当你在 ThemeRoller 中更改每个样式规则时，ThemeRoller 页面上的元素会自动更新，以便你立即看到这些更改的结果。

设置完所有样式信息后，你需要下载自定义主题。单击“Download theme”按钮时，你可以选择要包含在下载中的 jQuery UI 小部件。你可以选择的一些小部件包括：

- `Accordion`。提供一个带有滑动内容区域的小部件，旨在固定空间中提供大量内容。
- `Autocomplete`。尝试根据用户输入预测单词或短语。
- `Dialog`。为开发者提供一种创建交互式对话框的方式。
- `Tabs`。提供一种将内容容器转换为类似选项卡式文件夹界面的方式。

图 5.3. jQuery 文件的位置以及它们在 HTML 文件中的引用方式。

![Image](img/05-03.jpg)

请务必花时间阅读并熟悉 jQuery UI 网站提供的所有小部件。

现在，下载 jQuery UI 库中包含的所有小部件。将来，你可以只选择特定项目所需的小部件。一旦你按照自己的喜好配置了 CSS 主题，请单击“Download”。你的自定义 jQuery UI 包将以 ZIP 格式的压缩归档文件形式呈现。将归档文件保存到你的硬盘上。

接下来，让我们看看如何将 jQuery UI 库包含到你的 HTML 文件中。

### 在 HTML 文件中引用 jQuery UI 文件

当归档文件安全地保存在硬盘上后，你可以解压文件。需要注意的是，jQuery UI 库包含许多网站不需要的额外文件，因此不要将它们传输到你的 Web 服务器。图 5.3 展示了如何为最基本的网站组织文件；高亮显示的是你需要从 jQuery UI 下载中获取的文件。

对于本章将要开发的网站所使用的 jQuery UI 版本，我复制了 jQuery UI 库下载中的`images`目录（及其中的所有内容）以及 jQuery UI CSS 文件`jquery-ui-1.8.12.custom.css`，然后将它们粘贴到`chap5/css/ui`文件夹中。jQuery UI JavaScript 文件`jquery-ui-1.8.12.custom.min.js`被复制并粘贴到`chap5/inc/jQuery`文件夹中。这将使 jQuery UI 库文件可供网站使用。

然后，在将使用 jQuery UI 小部件的 HTML 文件中正确引用这些 jQuery UI 文件。让我们一步一步来，创建一个基础文件，随着本章的推进，将在此基础上添加内容。

1. 创建一个名为`5-0.php`的文件，并将其保存在`chap5`文件夹中。

2. 为网站创建基本的 HTML 布局：

```html
<!DOCTYPE html>
<html>
```

3. 创建开头的`head`标签，并包含基本的字符类型和页面`title`：

```html
<head>
    <meta http-equiv="Content-Type"
    ![Image](img/ccc.jpg) content="text/html; charset=UTF-8" />
    <title>The Lodge at Mystic Forrest</title>
```

4. 首先引用网站的 CSS 和 jQuery UI CSS 文件：

```html
<link type="text/css" rel="stylesheet"
![Image](img/ccc.jpg) href="css/lamf.css" />
<link type="text/css" rel="stylesheet"
![Image](img/ccc.jpg) href="css/ui/jquery-ui-1.8.12.custom.css" />
```

5. 加载 jQuery 和 jQuery UI 源文件（注意顺序；必须先加载基本的 jQuery 源文件）：

```html
<script type="text/javascript" src="inc/jQuery/jquery
![Image](img/ccc.jpg) -1.5.min.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/jquery-ui-1.8.12.custom.min.js">
![Image](img/ccc.jpg) </script>
```

6. 提供一组`script`标签和文档就绪包装器。你将在该包装器中包含其他 jQuery 调用：

```javascript
<script type="text/javascript">
$(document).ready(function() {
});
</script>
```

7. 提供其余标签以完成基本的 HTML 布局。

```html
</head>
<body>
</body>
</html>
```

有了 jQuery UI 后，你就可以开始添加 jQuery UI 为你的网站提供的一些酷炫小部件了。

### 包含 jQuery UI 小部件

jQuery UI 小部件设计精良且易于配置。事实上，这些小部件设计得如此出色，以至于在某些情况下，你几乎不需要编写 jQuery 代码来应用于你的界面。通常，你只需调用小部件并添加网站所需的选项即可。

在使用 jQuery UI 小部件时，应用正确的 HTML 标记更为重要。一个很好的例子是当你决定构建一个选项卡式界面时。那么，接下来你就将这样做。

### 创建选项卡式界面

向网站访问者呈现内容或多部分表单的最简单方法之一是使用选项卡式界面。人们对文件文件夹的选项卡概念很熟悉，因此使用选项卡浏览网站显得非常自然。多年来，Web 设计师一直使用复杂的 CSS 和 JavaScript 来创建选项卡式界面。jQuery UI Tabs 小部件消除了复杂性，并为创建选项卡式界面添加了一些极其灵活的功能。

1. 打开基础文件`chap5/5-0.php`，并将其另存为`chap5/5-1.php`，以设置选项卡式界面的标记。在`body`标签中添加一个用于页眉的`div`：

```html
<body>
    <div id="header"></div>
```

2. 为页面的内容区域设置一个`div`：

```html
<div id="content">
```

选项卡由无序列表定义。重要的是，锚点标签前面要有一个井号（高亮显示），因为链接将用于引用稍后添加的任何`div`：

```html
<div id="contentTabs">
    <ul>
        <li><a href="#welcome">Welcome to the
        ![Image](img/ccc.jpg) lodge...</a></li>
        <li><a href="#play">Play with us...</a></li>
        <li><a href="#stay">Stay with us...</a></li>
    </ul>
```

3. 为每个选项卡设置一个`div`，并确保每个`div`的`id`与之前无序列表中锚点标签内输入的文本匹配：

```html
<div id="welcome">
    <h2>Mystic Forrest welcomes you...</h2>
</div>
<div id="play">
    <h2>Things to do...</h2>
</div>
<div id="stay">
    <h2>Make a reservation...</h2>
</div>
```

你可以在每个`div`中放置几乎任何你想要的内容，正如你将在网站中添加其他 jQuery UI 小部件时看到的那样。

4. 关闭`div`标签：

```html
</div>
</div>
</body>
```

剩下要做的就是添加一点 jQuery，将你的标记转换为选项卡。

图 5.4. 添加 jQuery UI Tabs 小部件前后的浏览器窗口。

![Image](img/05-04.jpg)

5. 在标记的 head 部分，在文档就绪包装器中添加高亮显示的代码：

```javascript
<script type="text/javascript">
$(document).ready(function() {

    $('#contentTabs').tabs();

});
</script>
```

jQuery UI 负责处理标记和浏览器事件的 CSS 操作，将普通的无序列表转换为选项卡界面（**图 5.4**）。只需遵循几个简单的步骤，jQuery UI 库就能省去数小时的复杂繁琐工作。

就是这样。一行 jQuery 代码加上适当的支持文件和标记，就能将普通的网站转变为交互式杰作，这一切都归功于 jQuery UI 包。

Tabs 小部件提供了许多选项，包括通过 AJAX 加载内容的能力。设置好适当的选项后，你甚至可以让网站访问者根据自己的偏好重新排列选项卡的顺序。

接下来，我们通过为用户提供在表单中选择日期的方法来增添趣味。

## 为表单添加日历

与其依赖网站访问者正确输入日期，或者编写复杂的算法来解析访问者输入的日期，不如使用一个工具让用户能够选择他们需要在表单中输入的日期，这样会简单得多。jQuery UI 正好提供了这样一个工具——`Datepicker`。

让我们在你正在处理的网站的“与我们同住”选项卡中添加一个简单的表单。该表单仅收集足够的信息，以便网站所有者能够回复访问者关于其小旅馆可能的预订请求。

**1.** 将刚刚完成的文件`chap5/5-1.php`另存为`chap5/5-2.php`。

**2.** 找到`id`为`stay`的`div`。插入以下简单表单的标记：

```html
<form name="reservationForm" method="post">

    <label class="formLabel" for="arrivalDate">到达日期：

    ![Image](img/ccc.jpg) </label><input type="text" id="arrivalDate" /><br />

    <label class="formLabel" for="departureDate">离开

    ![Image](img/ccc.jpg) 日期：</label><input type="text" id="departureDate"

    ![Image](img/ccc.jpg) /><br />

    <label class="formLabel" for="visitorName">访客姓名：

    ![Image](img/ccc.jpg) </label><input type="text" id="visitorName" /><br />

    <label class="formLabel" for="phoneArea">电话号码：

    ![Image](img/ccc.jpg) </label>

    <input type="text" id="phoneArea" size="3" />

    <input type="text" id="phoneExchange" size="3" />

    <input type="text" id="phoneNumber" size="4" />

    <br />

    <label class="formLabel">&nbsp;</label><button

    ![Image](img/ccc.jpg) type="submit">请求预订</button><br />

    <label class="formLabel">&nbsp;</label><button

    ![Image](img/ccc.jpg) type="reset">重置表单</button><br />

</form>
```

处理两个日期（`arrivalDate`和`departureDate`）的 jQuery 代码比选项卡的 jQuery 代码稍微复杂一些。由于旅馆老板只希望人们查询今天或未来的日期，你需要设置`Datepicker`的`minDate`选项。然后，你需要使用`Datepicker`的`onSelect`选项来设置离开日历，使得只有到达日期之后的日期可供选择。

**3.** 通过将`Datepicker`绑定到`id`为`arrivalDate`的表单元素来启动`Datepicker`函数：

```javascript
$('#arrivalDate').datepicker({
```

在许多情况下，选项以对象的形式传递给 jQuery UI 小部件以及你将在后面学习的插件。正如你在第 4 章中学到的，JavaScript 对象以对象字面量表示法指定，即名称:值对。

**4.** 你不希望用户能够选择过去的日期。因此，将`minDate`选项设置为 0，以将最早可选日期设为今天（**图 5.5**）：

```javascript
minDate: 0,
```



一旦选择了到达日期，你可以使用`Datepicker`的`onSelect`选项创建一个晚于到达日期的日期值。网站所有者不希望访客能够选择早于到达日期的离开日期。

**5.** 打开`onSelect`选项，并将所选日期传递给`dateText`变量：

```javascript
onSelect: function(dateText) {
```

**6.** 通过使用 JavaScript 的`Date`函数将`dateText`变量转换为实际日期，开始计算合适的离开日期：

```javascript
var depart = new Date(dateText);
```

**7.** 将`depart`变量中包含的日期设置为比当前值（恰好是到达日期，尽管名称如此）大一天：

```javascript
depart.setDate(depart.getDate()+1);
```

图 5.5. 用户无法点击早于今天的日期，此处假设今天是 2011 年 7 月 19 日。

![Image](img/05-05.jpg)

图 5.6.`Datepicker`的最小离开日期比到达日期大一天。

![Image](img/05-06.jpg)

**8.** 将`datepicker`绑定到`id`为`departureDate`的表单输入元素，并将`minDate`选项设置为新的潜在离开日期：

```javascript
        $('#departureDate').datepicker({

            minDate: depart

        });
```

**9.** 用适当的大括号和圆括号关闭函数：

```javascript
    }

});
```

完成后，离开日期被设置为到达日期之后一天的最小日期（**图 5.6**）。

与其他 jQuery UI 小部件一样，`Datepicker`提供了大量用于自定义小部件的选项，包括动画、一次显示多个月份的能力，以及通过选择适当的语言将日历本地化到特定区域的功能。

将`Datepicker`添加到表单并配置好你想要的选项后，你可以使用 AJAX 提交表单。接下来我们设置这一点，并使用 jQuery UI 的`Dialog`小部件让网站访问者有机会确认他们的提交。

### 与访客建立“对话框”

你可以与网站或应用程序的用户建立的交互部分以对话框的形式提供。你可以使用对话框来通知或警告用户。你也可以使用它们来收集用户的额外信息，即使这些信息只是简单的表单提交确认。

jQuery UI 的`Dialog`小部件非常灵活，并提供了许多自定义选项。让我们设置一个对话框来确认预订请求的提交。即使是一个简单的对话框，也需要几个部分：包括 HTML、PHP 和 jQuery。为了提供交互，你将依次设置每个部分，首先从 HTML 开始。

**1.** 打开`chap5/5-2.php`并将其另存为`chap5/5-3.php`。

**2.** 在 HTML 的结束 body 标签之前，添加以下标记行以建立对话框的标记：

```html
<div id="dialog" title="验证提交">

    <p>您确定要查询这些日期吗？</p>

</div>
```

由于这是一个简单的确认对话框，HTML 非常简单。`div`标签中的`title`属性将用作对话框的标题，而`div`的内容将用于对话框的主体。

**3.** 在你的数据库包上运行 SQL 文件`chap5/sql/lodge.sql`（可在代码下载中找到），以设置数据库并创建用于保存预订请求的表。

现在 HTML 标记已完成，数据库表也已建立，你可以将注意力转向创建用于处理预订查询的 PHP 代码。

**4.** 创建`chap5/inc/reserve.php`并设置与数据库的连接。确保使用正确的用户名和密码进行数据库连接：

```php
if(!$dbc = mysql_connect('localhost', 'username', 'password')){

    echo '连接数据库时出错('.mysql_errno().')：

    ![Image](img/ccc.jpg) '.mysql_error() . "\n";

    exit();

}
```

**5.** 为进程添加一个`sleep`函数。`sleep`函数会使程序在执行下一行代码前暂停指定的时间（添加`sleep`语句的必要性将在“使用进度条通知用户”一节中明确）。将其设置为 2 秒：

```php
sleep(2);
```

**6.** 创建用于将 AJAX POST 请求中的信息插入`reserverequests`表的 SQL 语句：

```php
$reserveIN = "INSERT INTO `lamf`.`reserverequests` ";
$reserveIN .= "(`arrival`, `departure`, `guest`, `phone`) ";
$reserveIN .= "VALUES (";
$reserveIN .= "'".mysql_real_escape_string($_POST
![Image](img/ccc.jpg) ['arrivalDate'])."', ";
$reserveIN .= "'".mysql_real_escape_string($_POST
![Image](img/ccc.jpg) ['departureDate'])."', ";
$reserveIN .= "'".mysql_real_escape_string($_POST
![Image](img/ccc.jpg) ['visitorName'])."', ";
$reserveIN .= "'".mysql_real_escape_string($_POST
![Image](img/ccc.jpg) ['phoneArea']).'-'.mysql_real_escape_string($_POST
![Image](img/ccc.jpg) ['phoneExchange']).'-'.mysql_real_escape_string($_POST
![Image](img/ccc.jpg) ['phoneNumber'])."' ";
$reserveIN .= ")";
```

**7.** 在数据库上执行 SQL 语句并报告任何错误：

```php
if(!($reservation = mysql_query($reserveIN, $dbc))){
    echo mysql_errno();
    exit();
}
```

对于此表单，AJAX 进程不需要也不期望从数据库返回任何内容，因此除了可能发生的错误外，查询不会返回任何信息。至此 PHP 部分完成，接下来可以继续处理 jQuery 脚本。

jQuery 脚本包含两个函数：一个绑定到表单的“提交”按钮，用于调用`dialog`函数；另一个是`dialog`函数本身。

**1.** 打开`chap5/5-3.php`，找到 HTML 头部中的文档就绪函数。

**2.** 通过为预订表单绑定一个`submit`方法来启动对话框进程：

```javascript
$('#reservationForm').submit(function(e){
```

**3.** 对之前在本练习中创建的 HTML 标记调用 jQuery UI Dialog 的`open`方法：

```javascript
    $('#dialog').dialog('open');
```

**4.** 对提交事件应用`preventDefault`方法，并关闭函数：

```javascript
    e.preventDefault();
});
```

**5.** 为了在本网站中使用，再添加一个绑定到之前 HTML 中创建的`div`元素的`dialog`方法：

```javascript
$('#dialog').dialog({
```

**6.** 首先添加`autoOpen`选项。通过将此选项设置为`false`，可以防止对话框在调用`open`方法之前打开：

```javascript
    autoOpen: false,
```

**7.** 设置对话框的宽度：

```javascript
    width: 325,
```

**8.** 如果你希望对话框具有模态窗口的属性（一个半透明背景，透过它可以看到其他内容，但有助于用户专注于当前交互），则将`modal`选项设置为`true`：

```javascript
    modal: true,
```

**9.** 将`resizable`选项设置为`false`。在此场景下使用的对话框无需可调整大小：

```javascript
    resizable: false,
```

接下来，你需要为对话框创建按钮。在对话框中，向用户显示问题：“您确定要查询这些日期吗？”可能的答案是“是”或“否”。每个按钮将触发各自的函数。

**10.** 创建第一个按钮，即“是”按钮：

```javascript
    buttons: {
        "YES": function() {
```

**11.** jQuery UI Dialog 按钮具有可用的回调函数。因此，在回调中，对表单进行`serialize`序列化，并使用 jQuery 的 AJAX`post`方法将序列化后的数据发送到你之前创建的 PHP 处理脚本`chap5/inc/reserve.php`：

```javascript
            var formData = $('#reservationForm').serialize();
            $.post('inc/reserve.php', formData);
```

由于`post`方法没有返回数据，因此 AJAX 函数没有分配回调。

**12.** 清空表单中的文本输入框，让用户知道已经发生了某些操作：

```javascript
            $('#reservationForm input[type="text"]').val('');
```

图 5.7 jQuery UI 对话框被设置为一个确认交互界面。

![Image](img/05-07.jpg)

**13.** 在点击“是”按钮并执行 AJAX 调用后，对对话框调用`dialog close`方法：

```javascript
            $(this).dialog("close");
```

**14.** 对于对话框上的“否”按钮，不需要任何功能，因此直接关闭对话框：

```javascript
        }, "NO": function() {
            $(this).dialog("close");
        }
```

**15.** 添加`dialog`函数的闭合括号：

```javascript
    }
});
```

**16.** 导航到“与我们同住”选项卡，填写表单，然后点击“提交”。jQuery UI Dialog 小部件弹出，并提供提交日期的选项（图 5.7）。

jQuery UI Dialog 小部件提供的交互效果很好，但可能会让用户疑惑是否发生了任何操作。数据突然从表单中消失，对话框也消失了。如果用户能看到并感知到某个操作正在进行，他们可能会更安心。而这正是 jQuery UI Progressbar 的完美用武之地！

### 使用进度条通知用户

使用 jQuery UI Progressbar 小部件为用户提供进程正在进行的视觉提示，可以简单也可以复杂，完全取决于你的需求。在某些情况下，你只需显示一个动画进度条，向用户指示某个操作正在发生。在其他情况下，你可以设置与 jQuery UI Progressbar 小部件的复杂交互，使其能够接收来自某些操作的增量信息，然后利用这些信息将进度条从左向右移动。

AJAX 请求不会返回执行这种移动所需的增量信息，因为 AJAX 请求是异步的。你可以猜测增量值（不推荐），也可以寻找其他方式来使用 jQuery UI Progressbar 小部件达到预期效果。

> **注意：** AJAX 通常直到 XMLHttpRequest 完成时才会向浏览器返回任何信息（请参阅第 4 章）。你可以强制浏览器通过 AJAX 请求返回增量信息，但这是一个非常复杂的过程，在某些情况下可能会导致用户浏览器“锁定”，直到请求完成。

使用 jQuery UI Progressbar 小部件的一种方法是让它显示一个动画图像来表示操作。这就是你将在这里使用的方法。

你将使用之前学到的技术，在模态窗口中显示 jQuery UI Progressbar。一旦收到提交日期信息的确认，进度条将在`ajaxStart`函数中被调用。AJAX 请求完成后，进度条将淡出并消失。

**1.** 要配置 jQuery UI Progressbar 和模态窗口的 CSS，请打开`chap5/css/lamf.css`并插入`shade`属性：

```css
#progressShade {
```

**2.** 通过将`display`属性设置为`none`来初始隐藏遮罩层：

```css
    display: none;
```

**3.** 设置遮罩层的颜色和`position`：

```css
    background: #323232;
    position: fixed;
    left: 0;
    top: 0;
```

**4.** 配置遮罩层的`height`、`width`以及`z-index`：

```css
    width: 100%;
    height: 100%;
    z-index: 100;
}
```

**5.** 为容纳 jQuery UI Progressbar 小部件的元素设置 CSS 规则：

```css
#progressbar {
```

**6.** 在需要之前隐藏进度条：

```css
    display: none;
```

**7.** 配置`position`、`height`和`width`：

```css
    position: fixed;
    height: 12px;
    width: 200px;
```

**8.** 设置正确的`margin`和位置数据，使 jQuery UI Progressbar 小部件在浏览器窗口中居中：

```css
    margin: auto;
    top: 50%;
    left: 50%;
```

**9.** 将`z-index`设置为足够高的数字，以确保它出现在所有其他元素的上方：

```css
    z-index: 200;
}
```

现在你需要准备 jQuery 来显示 jQuery UI 进度条小部件。

**1.** 将`chap5/5-3.php`的副本另存为`chap5/5-4.php`。

**2.** 将`ajaxStart`绑定到 body：

```javascript
$('body').ajaxStart(function() {
```

**3.** 使用本书前面演示的用于设置模态窗口的相同技术，将模态窗口代码添加到`ajaxStart`函数中：

```javascript
    $('body').append('<div id="progressbar"></div>
    ![Image](img/ccc.jpg) <div id="progressShade"></div>');
    var modalMarginTop = ($('#progressbar').height()) / 2;
    var modalMarginLeft = ($('#progressbar').width()) / 2;
    $('#progressbar').css({
        'margin-top' : -modalMarginTop,
        'margin-left' : -modalMarginLeft
    });
    $('#progressShade').css('opacity', '0.4');
```

**4.** 在`ajaxStart`函数中调用 jQuery UI 进度条小部件：

```javascript
    $("#progressbar").progressbar({
```

**5.** 将进度条的`value`选项初始化为 100。这意味着进度条将在网页上占据的空间中从左到右完全展开：

```javascript
        value: 100
    });
```

**6.** 淡入带有动画图像的进度条，给人一种正在执行操作的视觉效果：

```javascript
    $('#progressbar, #progressShade').fadeIn(250);
});
```

图 5.8 jQuery UI 进度条小部件向用户指示进程正在运行。

![Image](img/05-08.jpg)

**7.** 在 AJAX 请求完成后的`ajaxStop`函数中移除 jQuery UI 进度条小部件：

```javascript
$('body').ajaxStop(function() {
    $('#progressbar, #progressShade').fadeOut(400, function(){
        $('#progressbar, #progressShade').remove();
    });
});
```

在正常情况下，驱动 jQuery UI 进度条小部件在网站中显示和消失的 AJAX 请求和响应循环会非常快，以至于进度条几乎来不及出现就会淡出。这就是在“与访客建立‘对话框’”一节中将`sleep`函数放入 PHP 文件的原因。`sleep`函数为请求增加了一点时间，从而延长了进度条在屏幕上的显示时间。**图 5.8**展示了进度条的实际效果。

以 jQuery UI 进度条小部件的方式为用户提供视觉线索，是保持网站访客参与度的宝贵方法。Web 应用程序的用户喜欢知道他们对自己与应用程序的交互有一定程度的控制。

另一种可以用来保持用户参与度的方法是 jQuery UI 自动完成小部件。接下来我们看看如何使用这个小部件。

#### 自动完成字段

用户将信息输入表单并点击按钮等待结果的盲目搜索在今天的互联网上几乎已成为历史。许多网站，包括像 Google 这样的大型网站，都选择根据用户在输入字段中输入的内容立即提供建议。

jQuery UI 自动完成小部件让你能够轻松实现即时建议功能。接下来我们将把这个小部件添加到网站中。



1. 打开 `chap5/5-4.php` 并将其副本另存为 `chap5/5-5.php`。找到第二个选项卡的 HTML 标记。该标记位于 `id` 为 `play` 的 `div` 中。

2. 设置支持 jQuery UI 自动完成小部件所需的唯一标记，即一个表单输入框：

```html
<div id="play">
    <h2>要做的事...</h2>
    <div id="widget">
        <label for="attractions">景点：</label>
        <input type="text" id="attractions" size="32" />
    </div>
```

3. 设置一个 `div` 来存放搜索结果：

```html
    <div id="attractionInfo"></div>
</div>
```

你将在单独的文件 `chap5/inc/jQuery/attractions.js` 中创建自动完成小部件的 jQuery 脚本。

4. 确保在 `5-5.php` 的 head 部分包含以下行来引用该文件：

```html
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/attractions.js"></script>
```

5. 要配置 jQuery 脚本文件 `chap5/inc/jQuery/attractions.js`，请构建一个景点数组：

```javascript
$(function(){
    var attractions = [
        "Admiral Nimitz Museum - Fredericksburg",
        "Aquarena Springs Nature Center - San Marcos",
        "Canyon Lake - Sattler",
        "Dinosaur Flats - Startzville",
        "Enchanted Rock - Fredericksburg",
        "Gruene Hall - New Braunfels",
        "Guadalupe River State Park - Spring Branch",
        "Live Oak Disc Golf Course - Live Oak",
        "Longhorn Caverns - Boerne",
        "Lost Maples State Park - Vanderpool",
        "National Museum of the Pacific War - Fredericksburg",
        "Wonder World - San Marcos"
    ];
```

6. 将 `autocomplete` 方法绑定到之前创建的输入文本框：

```javascript
    $('#attractions').autocomplete({
```

7. 为自动完成小部件提供数据源的引用，用于执行向用户呈现即时建议的任务。此处的数据源是已完成的数组，名为 `attractions`：

```javascript
        source: attractions,
```

8. 将 `ui.item` 中返回的选中项文本放入变量 `selectedAttraction`：

```javascript
        select: function(event, ui) {
            var selectedAttraction = ui.item.value;
```

图 5.9 当用户开始输入搜索词时，自动完成功能会返回建议的搜索词。

![Image](img/05-09.jpg)

9. 使用 JavaScript 的 `split` 方法将 `selectedAttraction` 变量拆分为数组。数组的第一个单词 `arrayAttractName` 用于标识 `chap5/inc/attractionInfo.php` 中将要检索的元素：

```javascript
            var arrayAttractionName =
            ![Image](img/ccc.jpg) selectedAttraction.split(' ');
```

10. 将景点信息加载到 `id` 为 `attractionInfo` 的元素中：

```javascript
            $('#attractionInfo').load('inc/attractionInfo.php
            ![Image](img/ccc.jpg) #'+arrayAttractionName[0]);
        }
    });
});
```

jQuery UI 自动完成小部件的演进过程如**图 5.9**所示。

jQuery UI 库的核心小部件确实在一个小巧且易于使用的包中提供了大量额外功能。然而，这些小部件只是冰山一角，作为设计师或开发者，你还可以通过 jQuery 为 Web 应用程序添加更多交互功能。

让我们继续研究其他开发者（就像你一样）提供的、可以添加到网站中的小部件。

---

**注意**

包含景点信息的文件 `chap5/inc/attractionInfo.php` 仅为了演示目的而创建了几个景点。

### 使用 jQuery 插件

如前所述，开发社区通过添加并持续添加数百个插件来拥抱和扩展 jQuery。社区成员将这些插件提供给社区中的其他设计师和开发者，用于他们自己的网站和应用程序，并且这些插件通常免费，无需支付任何费用或版税。

jQuery 团队认可这一努力，并在其网站 [`plugins.jquery.com`](http://plugins.jquery.com) 上专门开辟了空间来展示这些插件。在该网站上，你可以找到从 AJAX 到小部件等各类插件的列表。

由于可用插件数量庞大，从中筛选出一些最有用的插件是一项相当棘手的任务。最终，我选择了几个你可以快速轻松地应用于 Web 应用程序和网站的插件：

- **Tablesorter.** 让你能够为任何普通 HTML 表格添加排序功能。
- **TinyTips.** 一个工具提示生成器，允许你为几乎任何元素添加更多信息。
- **gMap.** 让与谷歌地图 API 的交互变得简单直接，并提供丰富的选项，使您能够通过地图向网站访客传递大量信息。
- **jqPlot.** 一个强大的插件，让您能够以图表和图形形式向访客呈现复杂数据。

---

**注意**

提供插件的开发者们投入了大量心血和时间，使他们的产品易于使用，并且免费提供给网站设计师和开发者社区。为了支持这些开发者以及他们插件的持续发展，我鼓励您向这些帮助简化您我工作的人捐款。（许多插件网站上都设有捐款链接。）

#### 用插件增强您的应用

在开发网站和应用程序时，您会反复使用某些工具来实现特定效果或提供特定类型的内容。以下章节讨论的 jQuery 插件正好满足这一需求。除了方便地访问特定类型的内容外，这些 jQuery 插件使用简单，并能为您向网站访客呈现的内容增加价值。

计算机用户一直很欣赏的一项功能是能够按一列或多列对数据表进行排序。表格排序有助于用户理解数据，并为他们提供挖掘数据趋势的方法。

您可以通过添加 jQuery Tablesorter 插件，将此功能扩展到您的网页表格中。

##### 对表格记录进行排序

Christian Bach 的 Tablesorter 插件（可从 [`tablesorter.com/docs`](http://tablesorter.com/docs) 获取）是为任何 HTML 表格添加排序功能的最有效插件。那么，让我们将其整合到旅馆网站中。

在旅馆示例中，业主希望查看并回复所有预订请求。由于这些请求的日期可能不按顺序，业主需要能够对记录进行排序，并优先回复即将到来的请求。

**1.** 打开 `chap5/5-5.php` 并将其另存为 `chap5/5-6.php`。

**2.** 开始编写 PHP 代码以获取预订请求列表，从数据库连接开始（确保使用您为数据库设置的用户名和密码）：

```php
<?php

if(!$dbc = mysql_connect('localhost', username, 'password')){

    echo mysql_error() . "\n";

    exit();

}
```

**3.** 添加一个非常简单的查询来从表中获取数据：

```php
$getRequests = "SELECT `arrival`,`departure`,`guest`,`phone` ";
$getRequests .= "FROM `lamf`.`reserverequests` ";
$getRequests .= "WHERE `response` = '' ";
if(!($requests = mysql_query($getRequests, $dbc))){
    echo mysql_errno();
    exit();
}
?>
```

PHP 将从数据库中检索所有预订请求记录。

**4.** 创建页面的 HTML 部分，包括 Tablesorter CSS 文件。确保在基本 jQuery 文件之后引入 Tablesorter 插件脚本：

```html
<!DOCTYPE html>
<html>
    <head>
    <meta http-equiv="Content-Type" content="text/html;
    ![Image](img/ccc.jpg) charset=UTF-8" />
    <title>The Lodge at Mystic Forrest</title>
        <link type="text/css" rel="stylesheet"
        ![Image](img/ccc.jpg) href="css/lamf.css" />
        <link type="text/css" rel="stylesheet"
        ![Image](img/ccc.jpg) href="css/ui/jquery-ui-1.8.12.custom.css" />
        <link type="text/css" rel="stylesheet"
        ![Image](img/ccc.jpg) href="css/tablesorter/style.css" />
        <script type="text/javascript" src="inc/jQuery/jquery
        ![Image](img/ccc.jpg) -1.5.min.js"></script>
        <script type="text/javascript"
        ![Image](img/ccc.jpg) src="inc/jQuery/jquery-ui-1.8.12.custom.min.js">
        ![Image](img/ccc.jpg) </script>
        <script type="text/javascript"
        ![Image](img/ccc.jpg) src="inc/jQuery/jquery.tablesorter.min.js">
        ![Image](img/ccc.jpg) </script>
```

**5.** 将 `tablesorter` 方法绑定到 `id` 为 `requests` 的表格上：

```html
        <script type="text/javascript">
        $(document).ready(function() {
            $('#requests').tablesorter({
```

jQuery Tablesorter 插件有许多可用选项，但这里只调用了一个。表格中的“已回复”列不需要排序。列从左到右计数，从零开始；“已回复”列是第四列。

**6.** 将“已回复”列的 `sorter` 属性设置为 `false`：

```javascript
                headers: {4:{sorter: false}}
            });
```

**7.** 关闭脚本：

```javascript
        });
        </script>
    </head>
```

该函数现已准备就绪。

**8.** 创建 HTML 标记的主体。在 HTML 中调用 PHP 脚本来设置要排序的表格：

```html
    <body>
        <div id="header"></div>
        <div id="content">
        <h2>预订请求</h2>
```

**9.** 在 PHP 部分创建一个条件检查，以测试表中是否有数据；如果没有，PHP 代码将返回一条消息，说明没有可用数据，这样用户就不会认为应用程序可能存在问题：

```php
        <?php
        if(0 != mysql_num_rows($requests)){
```

**10.** 如果有数据，则开始输出 HTML 表格。确保表格的 `id` 为 `requests`（在本例中，`tablesorter` 方法绑定到该 id），并为其指定 `class` 为 `tablesorter` 以启用 CSS 样式：

```php
            echo '<table id="requests" class="tablesorter">';
```

**11.** jQuery Tablesorter 插件要求表格同时具有格式正确的 `thead` 部分和 `tbody` 部分。使用正确的列名设置 `thead` 部分：

```php
            echo '<thead>';
            echo '<tr><th>到达日期</th><th>离开
            ![Image](img/ccc.jpg) 日期</th><th>客人姓名</th><th>客人
            ![Image](img/ccc.jpg) 电话</th><th>已回复</th></tr>';
            echo '</thead>';
```

**12.** 将注意力转向 `tbody` 部分。设置 PHP 循环遍历所有记录，并将信息放入相应的表格单元格中：

```php
            echo '<tbody>';
            while($pendingRequest =
            ![Image](img/ccc.jpg) mysql_fetch_array($requests)){
                echo '<tr class="even">';
                echo '<td>'.$pendingRequest['arrival'].
                ![Image](img/ccc.jpg) '</td>';
                echo '<td>'.$pendingRequest['departure'].
                ![Image](img/ccc.jpg) '</td>';
                echo '<td>'.$pendingRequest['guest'].'</td>';
                echo '<td>'.$pendingRequest['phone'].'</td>';
                echo '<td><input type="checkbox"
                ![Image](img/ccc.jpg) name="response[]" /></td>';
                echo '</tr>';
            }
```

**13.** 关闭 `tbody` 部分和 `table`：

```php
            echo '</tbody>';
            echo '</table>';
```

**14.** 如果查询未返回任何数据，则向用户提供一条消息：

```php
        } else {
            echo '<p>没有待处理的预订
            ![Image](img/ccc.jpg) 请求</p>';
        }
?>
```

**15.** 将剩余的 HTML 标签放置到位。**图 5.10** 显示了完成的表格：

```html
        </div>
    </body>
</html>
```

记录按照它们输入数据库的顺序排序。

在此表格中，四列（到达日期、离开日期、客人姓名和客人电话）是可排序的。**图 5.11** 显示了单击“到达日期”表头时发生的排序操作。

---

**注意**

我特意省略了用户如何通过选中“已回复”列中的复选框来从表格中移除记录。一个好的练习是为复选框添加 jQuery `change` 事件，并使用 jQuery 的 AJAX 功能将该记录标记为已回复。这样用户只需查看他们需要回复的记录。

---

无论你的表格多么简单或复杂，Tablesorter 插件都会提供许多选项，确保网站用户能够随心所欲地对数据进行排序。

另一种提供额外信息的方式是，当鼠标悬停在 HTML 页面中的某个元素上时，显示工具提示。让我们为网站添加一个工具提示插件，以提供关于选项卡的更多信息。

图 5.10. 刚加载的表格，数据未排序。

![图片](img/05-10.jpg)

图 5.11. 第一列按到达日期从最早到最晚排序。

![图片](img/05-11.jpg)



图 5.12. TinyTip 提供了关于旅馆网站上某个选项卡的更多信息。

![图片](img/05-12.jpg)

### 提供简短信息

工具提示，例如图 5.12 中所示，是一种向网站访问者提供关于网页上链接或词语的额外信息的好方法。

jQuery TinyTips 插件（可从 [`www.mikemerritt.me/blog/jquery-plugin-tinytips-1-1`](http://www.mikemerritt.me/blog/jquery-plugin-tinytips-1-1) 获取，作者为 Mike Merritt）是一个小巧、易用且极其灵活的插件，它允许你在弹出式工具提示中显示图片和文本。让我们试试吧！

1. 打开 `chap5/5-6.php` 并将其另存为 `chap5/5-7.php`。在 head 部分插入 TinyTips CSS 和 jQuery 脚本文件的源引用（已高亮显示）：

```html
<link type="text/css" rel="stylesheet" href="css/lamf.css" />

<link type="text/css" rel="stylesheet"
      href="css/ui/jquery-ui-1.8.12.custom.css" />

<link type="text/css" rel="stylesheet"
      href="css/tinyTips/tinyTips.css" />

<script type="text/javascript"
        src="inc/jQuery/jquery-1.5.min.js"></script>

<script type="text/javascript"
        src="inc/jQuery/jquery-ui-1.8.12.custom.min.js"></script>

<script type="text/javascript"
        src="inc/jQuery/attractions.js"></script>

<script type="text/javascript"
        src="inc/jQuery/jquery.tinyTips.js"></script>
```

2. 找到 `head` 标签之间的 `$(document).ready(function() {...` 代码段，并包含以下 jQuery 代码来设置 TinyTips：

```javascript
$('a.tinyTip').tinyTips('yellow', 'title');
```

你将带有 `class` 为 `tinyTip` 的锚标签绑定到 `tinyTips` 方法。`tinyTips` 方法中的属性（按顺序）是：要使用的 CSS 样式，以及将在工具提示中显示的元素属性。

3. 要在旅馆网站的多个选项卡上创建 TinyTips，请包含 `tinyTip` 类，并为选项卡的 HTML 标记添加 title 属性：

```html
<ul>
    <li><a href="#welcome" title="欢迎来到神秘森林">
        欢迎来到旅馆...</a></li>
    <li><a href="#play" class="tinyTip" title="查找当地景点">
        和我们一起玩...</a></li>
    <li><a href="#stay" class="tinyTip" title="提交预订请求">
        和我们一起住...</a></li>
</ul>
```

请务必访问 TinyTips 插件网站，了解其他选项以及在网站和应用程序中使用 TinyTips 的方法。

在为旅馆网站访问者添加更多信息的同时，为他们提供地图信息也是合理的，许多商业网站都这样做。由于在网站上展示地图数据非常流行，Google 提供了一个 API，你可以用它来与地图应用进行交互。下一个 jQuery 插件 gMap 为你提供了在网站中轻松有效地使用 Google Maps API 所需的工具。

### 将业务放在地图上

使用 Google Maps API 显示各种类型地图的网站数量惊人。网站使用地图来提供路线指引、突出显示所有位置，甚至指导玩家进行实时互动游戏。

只有一个问题：Google Maps API 使用起来可能很棘手，尤其是当设计师只想包含一张地图来显示零售商或服务的位置时。

Cedric Kastner 通过他的 Google 地图 jQuery 插件（他称之为 gMap，可从 [`gmap.nurtext.de`](http://gmap.nurtext.de) 下载）消除了这种复杂性。使用 gMap 的唯一要求（除了在标记中包含正确的文件外）是你拥有一个 Google 帐户，以便注册 Google Maps API 密钥。你可以在 [`code.google.com/intl/en-US/apis/maps/signup.html`](http://code.google.com/intl/en-US/apis/maps/signup.html) 注册密钥。

让我们把旅馆的位置放在地图上。

1. 将 `chap5/5-7.php` 另存为 `chap5/5-8.php`。确保在 `chap5/5-8.php` 的 head 部分包含 gMap 插件源文件，就像之前处理其他插件文件一样。

2. 在 head 部分使用你的 Google Maps API 密钥包含以下脚本引用（将其添加到 gMap 脚本引用之前）：

```html
<script type="text/javascript"
        src="http://maps.google.com/maps?file=api&amp;v=2&amp;
        key=在此处输入你的 API 密钥"></script>
```

3. 在你的 CSS 文件 `chap5/css/lamf.css` 中添加以下样式规则和属性。这些属性将用于定义地图的容器：

```css
#lodgeMap {
    position: relative;
```

4. 为用于容纳地图的元素定义高度和宽度：

```css
    width: 700px;
    height: 450px;
```

5. 将容纳地图的元素在屏幕上居中：

```css
    margin-left: -350px;
    left: 50%;
}
```

6. 在 HTML 文件 `chap5/5-8.php` 的 `head` 部分的文档就绪包装器中添加 gMap 插件的 jQuery 代码。将 gMap 插件绑定到将容纳地图的元素：

```html
<script type="text/javascript">
    $(document).ready(function(){
        $('#lodgeMap').gMap({
```

7. 设置你的 gMap 选项。在特定的纬度和经度放置一个标记：

```javascript
            markers: [{
                latitude: 29.871266,
                longitude: -98.237708
            }],
```

8. 将地图类型和缩放级别传递给 gMap 插件：

```html
            maptype: G_PHYSICAL_MAP,
            zoom: 12
        });
    });
</script>
```

图 5.13. gMap 插件创建的标记显示了旅馆在一个岛屿上的位置。

![图片](img/05-13.jpg)

`maptype: G_PHYSICAL_MAP` 选项提供了地图的地形视图（图 5.13）。

9. 在 HTML 正文中的某个位置添加用于容纳地图的元素：

```html
<div id="lodgeMap"></div>
```

10. 加载页面。

jQuery gMap 插件显示的地图以输入的位置为中心，并带有标记，缩放级别足以向用户提供一些地形细节。同样，请务必查看 gMap 网站，了解此处未演示的更多选项。

使用 jQuery 插件在地图上绘制点和在图表中绘制信息都很容易。为了使数据报告更直观，通常希望以条形图、饼图或沿着绘图线和趋势线的形式以图形方式呈现信息。下一个插件 jqPlot 提供了一个全面的库，用于为 Web 应用程序用户提供这些类型的图表。

图 5.14. 使用 jqPlot 设置每月预订请求的水平条形图。

![图片](img/05-14.jpg)

### 绘制和图表化数据

到目前为止，这些插件使用起来都相当简单。Chris Leonello 的 jqPlot 插件（可从 [`www.jqplot.com`](http://www.jqplot.com) 获取）在简洁性上也不例外。不同之处在于，它提供了大量选项，供你创建和定制多种类型的图形和图表。这种灵活性是有代价的：使用该插件时，你必须非常细致地设置显示和数据细节。

在本例中，你将创建一个柱状图（图 5.14），向旅馆老板展示每月通过网站收到的预订请求数量。你将把图表添加到旅馆老板查看待处理预订请求的页面上。

首先修改网站的 CSS 文件来开始练习。

1. 打开 `chap5/css/lamf.css`，为 CSS 选择器 `requestChart` 添加高度和宽度属性。该选择器将连接到 HTML 中显示图表的元素：

```css
#requestChart {
    width: 800px;
    height: 350px;
}
```

为了从数据库中检索数据并正确格式化数据以供 jQuery jqPlot 插件使用，必须非常仔细地编写 PHP 代码。jqPlot 期望以 JavaScript 对象表示法（JSON）的形式成对提供标签（以数值索引值的形式）和要绘制的值：

```json
[0,1],[0,2],[0,3],[0,4],[6,5],[2,6],[3,7],[0,8],[1,9],[0,10],
[0,11],[1,12]
```

每对中的第一个数字表示要绘制的值。第二个值是绘图索引（在本例中对应一年中的月份）。

---

**提示**

许多 jQuery 插件使用 JSON 格式的数据，因为它是 JavaScript 对象字面量表示法的子集。这有助于保持不同插件之间的表示法一致，并帮助开发者避免学习不同的格式来向插件传递信息。

---

对 MySQL 数据库的 PHP 请求将使用之前创建的同一连接；让我们看看你将添加到页面 PHP 部分的代码。

2. 将 `chap5/5-8.php` 另存为 `chap5/5-9.php`。这是你将添加额外 PHP 和 jQuery 代码以显示柱状图的文件。

3. 在 `5-9.php` 的 PHP 部分中，在数据库查询完成后立即声明一个变量，用于保存来自数据库的绘图数据：

```php
$ra = '';
```

4. 创建一个名为 `requestArray` 的数组，用于索引数据库请求：

```php
$requestArray = array(1,2,3,4,5,6,7,8,9,10,11,12);
```

5. 遍历 `$requestArray`，并根据 `$requestArray` 开始向数据库发起请求：

```php
for($i = 0; $i < count($requestArray); $i++){
    $getReservationsByMonth = "SELECT count(*) as reqCount
    FROM `lamf`.`reserverequests` WHERE SUBSTRING
    (`arrival`, 1, 2) = ".$requestArray[$i];
```

6. 运行查询。查询会返回任何发生的错误：

```php
        if(!($requestsMonth =
        mysql_query($getReservationsByMonth, $dbc))){
            echo mysql_errno();
            exit();
        }
```

7. 为了确保 JSON 数组字符串格式正确，在每对方括号值之间插入逗号。如果 `$i` 的值小于 11（十二月），则插入逗号（高亮部分）：

```php
        if($i < 11){
            $ra .= ''. mysql_result($requestsMonth, 0)
            .','. ($i+1) . '],';
```

PHP 的 `mysql_result` 从查询 `$requestsMonth` 中返回第一个项目（给定月份的请求计数）。由于 `$requestArray` 的索引实际上比月份的实际数值索引小 1（记住 PHP 数组索引从 0 开始），因此你将该值加 1，以确保月份正确对应。

8. 如果月份是十二月（`$i == 11`），则消除在该对后面加逗号的可能性：

```php
        } else {
            $ra .= ''. mysql_result($requestsMonth, 0)
            .','. ($i+1) . ']';
        }
}
```

现在 PHP 输出了正确的数据格式，你可以将注意力集中在插入正确的文件上，这些文件需要在 HTML 的 head 部分引用。jqPlot 插件有几个可选的附加组件，根据你期望显示的图表，你可能需要包含其中任意数量的附加组件。

9. 确保引用了 jqPlot 的 CSS 样式表：

```html
<link type="text/css" rel="stylesheet"
      href="css/jqPlot/jquery.jqplot.css" />
```

10. 对于柱状图，需要几个 jqPlot 附加组件。第一个附加组件对于微软的 Internet Explorer 9 不是必需的，但对于早期版本的 Internet Explorer 是必需的。该附加组件在 CSS 条件注释中调用（所有附加组件都包含在 jqPlot 的基础文件之后）：

```html
<script type="text/javascript"
        src="inc/jQuery/jquery.jqplot.min.js"></script>

<!--[if lt IE 9]><script type="text/javascript"
        src="inc/jQuery/excanvas.min.js"></script><![endif]-->
```

11. 对于柱状图以及图表轴上会使用文本的图表，你必须引用 `jqplot.barRenderer.min.js` 和 `jqplot.categoryAxisRenderer.min.js` 文件：

```html
<script type="text/javascript"
        src="inc/jQuery/jqplot.barRenderer.min.js"></script>

<script type="text/javascript"
        src="inc/jQuery/jqplot.categoryAxisRenderer.min.js">
</script>
```

12. 编写 jQuery 代码来显示图表。启用 jqPlot 的附加组件：

```javascript
$.jqplot.config.enablePlugins = true;
```

13. 从 PHP 函数中获取数据，并将其插入 JavaScript 变量 `line1` 中：

```javascript
line1 = [<?php echo $ra; ?>];
```

14. 调用 `jqplot` 函数。将该函数绑定到显示图表的元素上，并提供变量 `line1` 中包含的数据：

```javascript
$.jqplot('requestChart', [line1], {
```

图 5.15. 边距为零会导致每个柱形填满可用空间，可能使图表难以阅读。

![图片](img/05-15.jpg)

15. 将 `$.jqplot.BarRenderer` 附加组件声明为 `seriesDefaults` 选项的一部分。这样做是为了显示柱状图：

```javascript
            seriesDefaults: {
                renderer: $.jqplot.BarRenderer,
```

现在 jqPlot 知道了将使用的图表渲染器附加组件。

16. 设置渲染器的选项：`barDirection` 为水平方向，`barMargin` 为 10：

```javascript
                rendererOptions: {
                    barDirection: 'horizontal',
                    barMargin: 5
                }
            },
```



`barMargin` 选项设置柱形之间的间距。图 5.15 显示了边距为零的柱形；重叠效果不佳。

接下来，你将设置图表每个轴的详细信息，从 y 轴开始。y 轴将显示月份名称。

**17.** 设置 y 轴的渲染器：

```
axes: {
    yaxis: {
        renderer: $.jqplot.CategoryAxisRenderer,
```

**18.** 提供 `ticks` 选项的信息，在本例中是月份的名称：

```
ticks: ['一月', '二月', '三月',
    '四月', '五月', '六月', '七月',
    '八月', '九月', '十月',
    '十一月', '十二月']

},
```

图 5.16\. 每个刻度递增 10，图表 x 轴最大值为 100。

![Image](img/05-16.jpg)

**19.** 提供图表 x 轴的信息。旅馆老板认为他每月通过网站会收到大约 100 个请求。将 x 轴配置为从最小 0 个请求开始，最大 100 个请求：

`xaxis: {min: 0, max: 100, numberTicks:11}`

**20.** 在 x 轴上指定 11 个刻度，以显示十个均匀分布的柱形（图 5.16）。

如果你需要创建复杂的仪表板——显示各种类型的图表和图形——来报告企业中的各项指标，并且希望高效地完成，那么你无需再寻找其他工具，`jqPlot` jQuery 插件就是最佳选择。凭借其丰富的图表类型和众多可用选项，你一定能找到展示数据的完美元素。

有数百个非常实用的插件可用于你的网站和 Web 应用程序。然而，还有另一类 jQuery 插件，它们可能不那么实用，但用起来很有趣。接下来我们看看其中一些。

#### 让你的网站更炫酷

对于某些 jQuery 插件而言，实用与酷炫之间的界限很模糊。在互联网上搜索，你会发现许多处于技术前沿的 jQuery 插件。这类插件可能提供先进的动画技术，但并非在所有浏览器上都能正常工作，或者进行密集的数据操作，导致浏览器运行不畅。其中一些高级插件并不适合日常使用，而且许多前沿插件仍处于实验阶段，稳定性较差。

本节中你将使用的插件都是一流的，质量足够高，可以日复一日地用于你的网站。与大多数 jQuery 插件一样，它们很容易集成到你的设计中。

首先介绍一种向旅馆网站访客提供天气信息的方法。

图 5.17\. 旅馆当前的天气状况。

![Image](img/05-17.jpg)

##### 预测天气

`zWeatherFeed` jQuery 插件（[www.zazar.net/developers/zweatherfeed](http://www.zazar.net/developers/zweatherfeed)）可以非常轻松地将 Yahoo 的天气信息包含到你的网站中（图 5.17）。让我们将 `zWeatherFeed` jQuery 插件添加到旅馆网站中。

**1.** 打开 `chap5/5-7.php` 并将其另存为 `chap5/5-10.php`。在 `chap5/5-10.php` 的 head 部分包含对 `zWeatherFeed` CSS 和 jQuery 脚本的引用（高亮部分）：

```
<link type="text/css" rel="stylesheet" href="css/lamf.css" />
<link type="text/css" rel="stylesheet"
      href="css/ui/jquery-ui-1.8.12.custom.css" />
<link type="text/css" rel="stylesheet"
      href="css/tinyTips/tinyTips.css" />
<link type="text/css" rel="stylesheet"
      href="css/weatherfeed/jquery.zweatherfeed.css" />
<script type="text/javascript" src="inc/jQuery/jquery-1.5.min.js"></script>
<script type="text/javascript"
        src="inc/jQuery/jquery-ui-1.8.12.custom.min.js"></script>
<script type="text/javascript"
        src="inc/jQuery/attractions.js"></script>
<script type="text/javascript"
        src="inc/jQuery/jquery.tinyTips.js"></script>
<script type="text/javascript"
        src="inc/jQuery/jquery.zweatherfeed.min.js"></script>
```

**2.** 在 jQuery 代码的文档就绪函数部分包含以下 jQuery 脚本：

```
$('#weather').weatherfeed(
    ['USTX0207'],
    {unit: 'f'}
);
```

该代码将 `weatherfeed` 方法绑定到一个 `id` 为 `weather` 的元素上，例如 `<div id="weather"></div>`。这里包含的 `weatherfeed` 方法选项包括 RSS（简易信息聚合）位置代码以及你希望使用的度量单位，此处为华氏度。

要获取 RSS 位置代码，请访问 [`weather.yahoo.com`](http://weather.yahoo.com) 并输入位置信息。如图 5.18 所示，将鼠标悬停在 RSS 图标上，即可在浏览器状态栏中看到 URL。你可以在该 URL 中找到位置代码，然后将其放入你的 jQuery `weatherfeed` 函数中。

---

注意

请务必阅读并理解 Yahoo 关于天气信息的使用条款。

---

图 5.18\. 查找 RSS 位置代码。

![Image](img/05-18.jpg)

由于你正在向网站访客提供更多关于旅馆的信息，很可能你还想展示一些旅馆及周边地区的照片。一种有趣的方式是使用一个插件，让访客能够放大并更仔细地查看照片细节。

##### 放大查看图片

许多购物和摄影网站上流行一种效果，允许用户将鼠标悬停在图片上并放大查看。Raff Cecco 的 `Cloud Zoom` 插件（可在 [www.professorcloud.com/mainsite/cloud-zoom.htm](http://www.professorcloud.com/mainsite/cloud-zoom.htm) 获取）是用 jQuery 实现这一效果的完美工具。

**1.** 打开 `chap5/5-0.php` 并将其另存为 `chap5/5-11.php`。

**2.** 在 HTML 文件的 `head` 部分包含对 `Cloud Zoom` CSS 文件和 jQuery 文件的引用（高亮部分）：

```
<link rel="stylesheet" href="css/primary.css" type="text/css" />
<link rel="stylesheet" href="css/cloudZoom/cloud-zoom.css"
      type="text/css" />
<script type="text/javascript" src="inc/jQuery/jquery-1.5.min.js"></script>
<script type="text/javascript"
        src="inc/jQuery/cloud-zoom.1.0.2.min.js"></script>
```

**3.** 设置一个容器来放置照片：

```
<div class="bigPhoto">
```

**4.** 添加引用大图和小图的锚点标签和图片标签：

```
<a href='images/lodge_hummingbirds.jpg' class='cloud-zoom'
   id='zoom1' rel="position: 'inside', smoothMove: 4,
   adjustX: -1, adjustY:-4">
    <img src="images/lodge_hummingbirds_small.jpg" alt=''
         title="Hummingbirds at the Lodge" border="0" />
</a>
```

这个插件的一个巧妙之处在于，你无需在页面中添加任何 jQuery 代码。`Cloud Zoom` 插件的所有选项（高亮部分）都在锚点标签的 `rel` 属性中指定。

**5.** 关闭放置照片的容器：

```
</div>
```

**6.** 通过向 `chap5/css/lamf.css` 添加 CSS 规则来居中照片容器：

```
.bigPhoto {
    position: relative;
    width: 800px;
    margin: auto;
}
```

图 5.19\. 大图被调用到原始图片所在的空间中。移动光标可以让用户更仔细地查看图片的各个部分。

![Image](img/05-19.jpg)

缩放效果（图 5.19）是通过使用两张图片副本实现的：一张正常显示的小图和一张由 `Cloud Zoom` 插件调用的大图。大图（此处为 `images/lodge_hummingbirds.jpg`）在锚点标签中引用，而缩略图（`images/lodge_hummingbirds_small.jpg`）则包含在图片标签中。

为此 `Cloud Zoom` 实例指定的选项包括 `position: 'inside'`，它告诉 `Cloud Zoom` 插件在缩略图内部显示放大的图像。选项 `smoothMove: 4` 设置了一种光标缓动方法，使放大图片的移动具有流畅效果。选项 `adjustX: -1` 和 `adjustY:-4` 用于微调放大图像相对于缩略图的位置。

jQuery `Cloud Zoom` 插件还有许多其他选项，当你在网站中使用该插件时，这些选项将为你提供极大的创作灵活性。

在网站和应用程序中处理图像的另一种方法是添加一个随浏览器大小调整的背景图像。接下来我们看看这个。

图 5.20\. 一个渐变填充的背景图像，非常适合作为网站或应用程序的底层。

![Image](img/05-20.jpg)

##### 使用浏览器调整背景图片大小

多年来，网页设计师和开发者一直在寻找改善网站背景显示效果的方法。缩放背景图片一直是个难题，尤其是当你预见到浏览器窗口大小可能会改变时。jQuery `Easy Background Resize` 插件解决了这个问题。事实上，你会发现你会想方设法在所有网站和应用中使用背景图片。

背景调整插件结合你的一张图片，可以为你的网站和应用带来微妙（如图 5.20 中的渐变背景）或强烈的视觉效果。它无疑是你能添加到网站中最巧妙的插件之一。

该插件由 J.P. Given 开发，jQuery `Easy Background Resize`（可在 [`johnpatrickgiven.com/jquery/background-resize`](http://johnpatrickgiven.com/jquery/background-resize) 获取）允许你在网站上放置背景图片，并使该背景图片随浏览器一起调整大小。

让我们将这个插件添加到旅馆网站中。

**1.** 打开 `chap5/5-10.php` 并将其另存为 `chap5/5-13.php`。

图 5.21\. 渐变背景已应用于网站主体。当浏览器调整大小时，渐变会按需扩展和收缩。

![Image](img/05-21.jpg)

**2.** 在 HTML 文件的 head 部分插入包含该插件的代码行：

```
<script type="text/javascript" src="inc/jQuery/jquery.ez-bg-resize.js"></script>
```

**3.** 将 `ezBgResize` 方法绑定到 HTML 的 `body` 标签，并指定要用作背景的图片路径：

```
$("body").ezBgResize({
    img : "grfx/lodge_gradient_background.jpg"
});
```

**4.** 将页面加载到浏览器中（图 5.21）并调整大小以查看效果。就这么简单！

图 5.22\. 使用蜂鸟图片作为背景的旅馆网站视图。这展示了在图片之上叠加其他图形和网页元素是多么容易。

![Image](img/05-22.jpg)

一旦你看到 jQuery `Easy Resize` 插件的实际效果，你无疑会想出许多创造性的方法将其应用到你的网站和应用中。例如，图 5.22 显示渐变背景已被之前使用的蜂鸟图片所取代。

现在你已经让背景变得更加生动，你可以在前景中添加一个小插件来吸引眼球。

图 5.23\. 页面卷角效果。

![Image](img/05-23.jpg)

##### 与一个好网站一起“卷”起来

当前旅馆网站的设计并不够新潮。旅馆老板希望在不影响现有网站的情况下，让访问者知道新网站设计即将推出。

本质上，你将“翻页”到一个新网站。一个支持翻页概念的 jQuery 插件（图 5.23）是 jQuery `Sexy Curls` 插件。卷页“背后”显示的信息是对即将到来的新网站的预览。

Elliot Kember 的 `Sexy Curls` jQuery 插件（可在 [`elliottkember.com/sexy_curls.html`](http://elliottkember.com/sexy_curls.html) 获取）是创建页面卷角效果的理想插件。现在让我们将其包含到网站中。

**1.** 创建 `chap5/5-13.php` 的副本并另存为 `chap5/5-14.php`。确保所需的 CSS 和 jQuery 文件已包含在 `chap5/5-14.php` 的 head 部分：

```
<link type="text/css" rel="stylesheet" href="css/lamf.css" />
<link type="text/css" rel="stylesheet" href="css/ui/jquery-ui-1.8.12.custom.css" />
<link type="text/css" rel="stylesheet" href="css/tinyTips/tinyTips.css" />
<link type="text/css" rel="stylesheet" href="css/turn/turn.css" />
<link type="text/css" rel="stylesheet" href="css/weatherfeed/jquery.zweatherfeed.css" />
<script type="text/javascript" src="inc/jQuery/jquery-1.5.min.js"></script>
<script type="text/javascript" src="inc/jQuery/jquery-ui-1.8.12.custom.min.js"></script>
<script type="text/javascript" src="inc/jQuery/attractions.js"></script>
<script type="text/javascript" src="inc/jQuery/jquery.tinyTips.js"></script>
<script type="text/javascript" src="inc/jQuery/turn.js"></script>
<script type="text/javascript" src="inc/jQuery/jquery.zweatherfeed.min.js"></script>
```

页面卷角图片存储在 `turn.css` 文件所在的同一文件夹中，即 `chap5/css/turn`。

**2.** 在结束 `body` 标签之前添加包含“隐藏”信息的图片标签：

```
<img id="foldGraphic" src="grfx/lodge_new.jpg">
```

**3.** 在文档就绪包装器中添加 jQuery 代码，将 `fold` 方法绑定到将显示在页面卷角后面的元素：

```
$('#foldGraphic').fold();
```

在这个例子中，绑定到 `fold` 方法的元素是一张图片。

jQuery `Sexy Curls` 插件是我遇到的少数几个需要开发者打开插件（位于 `chap5/inc/jQuery/turn.js` 文件夹中）来设置选项的插件之一。



**4.** 打开插件，找到以注释 `//default awesomeness.` 开头的代码部分（Kember 先生很有幽默感！）。接下来的几行是你可以为插件设置的选项。在这个例子中，设置的选项包括用于翻页的图片位置、起始和最大尺寸：

```js
turnImage: 'css/turn/fold.png', // 三角形翻页图片
maxHeight: 450, // 最大高度。显而易见。
startingWidth: 40, // 起始宽度和高度
startingHeight: 40, // （这些应该用驼峰命名法，哎呀。）
```

此外，`autoCurl` 函数被设置为 `true`，这样当你鼠标悬停在小卷角图片上时，效果就会运行：

```js
autoCurl: true // 如果设置为 true，则鼠标悬停/移出时卷角会卷起/展开。
```

**5.** 将页面加载到你的 Web 浏览器中，测试卷角效果。

现在你已经安装并配置了许多插件，你可能想尝试开发自己的插件。在下一节中，我将向你展示如何布局基础知识，以便你可以制作自己的 jQuery 插件。

### 打造你自己的插件

创建自己的插件可以非常有成就感，而且并不难。让我们编写一个非常基础的插件，并将其应用到旅馆网站中。

**1.** 创建一个名为 `jquery.colorText.js` 的文件，并将其保存在 `chap5/inc/jQuery` 文件夹中。通过声明一个函数来开始编写插件：

```js
(function($){
```

为了确保你可以在插件中继续使用熟悉的美元符号，并防止插件与其他 JavaScript 库冲突，插件框架将 `jQuery` 映射到美元符号。`jQuery` 到自执行函数的映射发生在插件的最后一行 `(jQuery)`。这将创建一个称为*闭包*的自执行函数。

---

> **注意**

> 闭包可能难以理解，但归根结底，它是在函数返回后保持函数的局部变量存活。如果你有兴趣了解更多关于闭包的知识，互联网上有大量关于闭包的信息。

---

**2.** 向 jQuery 的 `fn`（称为 *effin*）对象添加一个新的函数属性。该属性的名称将是你的插件名称。对于 `colorText` 插件，用户将能够向函数传递选项，因此将其声明为函数的参数：

```js
    $.fn.colorText = function(options) {
```

**3.** 为你允许用户为 `colorText` 插件声明的每个选项设置默认值：

```js
        var defaults = {

        'color'            : '#000000',

        'backgroundColor'  : '#FFFFFF'

    };
```

当用户将 `colorText` 元素绑定到某个元素时，可以通过传递一个 JavaScript 对象字面量来扩展默认设置。jQuery 用于合并默认选项与传递的对象字面量的方法是 `extend` 方法。

`extend` 方法的第一个参数被称为目标对象。目标对象是在调用 `extend` 时将被修改的对象。

**4.** 在这种情况下，保持目标对象为空，以便保留 `defaults` 和 `options` 的属性。将 `extend` 方法赋值给 `opt` 变量：

```js
    var opt = $.extend({}, defaults, options);
```

**5.** 为了让插件能够与其他 jQuery 方法链式调用，返回 `this` 对象，同时继续使用插件中的方法对其进行操作：

```js
    return this.each(function(){

        $this = $(this);
```

**6.** 插入 `colorText` 插件将对绑定到该插件的元素执行的操作。在本例中，修改 CSS（这并非世界上最聪明的插件）以设置绑定到插件的元素的文本颜色和背景颜色：

```js
        $this.css({
```

**7.** 由于默认设置和可选设置已通过 `extend` 方法合并，你可以从存储在 `opt` 中的对象字面量中检索每个属性的值，如下所示：

```js
            'color': opt.color,

            'backgroundColor': opt.backgroundColor

        });

    });

  };
```

**8.** 用正确的括号关闭简单的 `colorText` 插件，然后将 jQuery 对象传递给插件：

```js
})(jQuery);
```

现在插件已准备就绪，可以使用了。

**1.** 复制 `chap5/5-14.php` 并将其保存为 `chap5/5-15.php`。

图 5.24 将 `colorText` 插件应用于 HTML 页面中元素的结果。

![Image](img/05-24.jpg)

**2.** 插入引用 `colorText` 插件源的脚本标签，就像你处理所有其他插件一样：

```html
<script type="text/javascript"

![Image](img/ccc.jpg) src="inc/jQuery/jquery.colorText.js"></script>
```

**3.** 将 `colorText` 插件绑定到 `h2` 元素。为 `color` 和 `backgroundColor` 属性插入不同的值，以了解插件的工作方式：

```js
$('h2').colorText({

    'color': '#FFCC33',

    'backgroundColor': '#006600'

});
```

`h2` 元素是小木屋网站每个选项卡中的标题元素。将 `5-15.php` 加载到浏览器中，查看 **图 5.24** 中显示的结果。

这个 `colorText` 插件是一个简单的示例，展示了如何构建 jQuery 插件。你可以将这些基本原则应用于任何你想在 jQuery 中创建的插件。现在，你已经将多个 jQuery 小部件和插件整合到了小木屋网站中，你已经学会了如何开始创建自己的 jQuery 代码来分享。

### 总结

本章充满了 jQuery 小部件（来自官方 jQuery UI 库），你可以使用它们来增强访问者与网站的交互。这些小部件包括日期选择器、进度条和对话框。你只需包含 jQuery UI 库文件，并通常用一两行脚本调用每个小部件，即可在网页和应用程序中使用它们。

接下来，你的视野扩展到了被称为 jQuery 插件的全球小部件农场。来自全球各地的开发者开发并维护他们自己的 jQuery 库扩展，提供从表格排序器和工具提示到图片缩放器和图表绘制器等交互式小部件。

最后，你学习了如何为 jQuery 库创建自己的扩展，并获得了一个模板，你可以用它来支持自己的插件库，这些插件可以保留或与世界分享。

在下一章中，你将应用本书到目前为止学到的所有技能和工具，创建一个类似于软件而非网站的 Web 应用程序界面。让我们继续前进吧！

## 6. 创建应用程序界面

jQuery 库通过提供擅长支持协同作用的方法和函数，使创建强大、交互式的 Web 应用程序界面变得更加容易，这些协同作用可以将枯燥、无生气的 Web 应用程序界面转变为功能丰富、以用户为中心的强大工具，帮助你创建直观且有趣的 Web 应用程序界面。

在本章中，你将学习如何应用前几章学到的技术，以及其他的 jQuery、HTML 和 CSS 技术，为基于 Web 的应用程序界面打下坚实的基础。你将首先详细地了解基本的标记和样式信息，并在界面开发过程中逐步添加内容。在此过程中，你将学习使用精灵图和 AJAX 为界面注入活力的高级技术。

### 建立基础

图 6.1 Web 应用程序界面的基本布局。

![Image](img/06-01.jpg)

对于任何 Web 应用程序，你需要完成的第一步是确定应用程序的需求，然后定义数据模型。一旦这些完成，你就可以开始为应用程序所需的每个用户界面定义布局。

在设计布局时，必须始终牢记 Web 应用程序的用户。导航项必须逻辑分组，内容必须一致。用户应该能够依靠直觉轻松找到元素。例如，你可能在界面顶部有一个主导航组件。当点击主项时，会加载反映用户初始选择的次级导航。这些选择必须对用户有意义，同时支持应用程序所需的操作。

一旦确定了布局，你就可以建立一些基础的 HTML 标记和 CSS。本章将要构建的界面非常基础：主导航位于浏览器窗口顶部，次级导航位于窗口左侧，主要内容显示在右侧的大区域中（**图 6.1**）。

通过在浏览器窗口中提供一个页脚区域，可以显示额外的目的驱动内容，从而完成基本布局。

此布局的主要目标是保持每个元素在浏览器中可见，以避免滚动。必要时允许滚动，但仅限于包含的内容超出该元素显示范围的容器内。

有了布局计划，接下来你将开始创建项目的基础标记。

#### 创建 HTML

HTML 标记构成了界面其余部分的基础。你将定义用于容纳内容和导航元素的容器，这些容器将通过 CSS 和 jQuery 得到增强。

在定义了基本的 HTML 标记之后，除了添加额外的 jQuery 和 CSS 函数声明外，你不需要对其进行太多修改。与之前的标记布局一致，应用程序界面的 HTML 将非常简单。让我们开始吧。

**1.** 创建一个名为 `6-1.php` 的文件，并将其保存在 `chap6` 文件夹中。以 DOCTYPE 声明（此处为 HTML5 声明）打开 HTML：

```html
<!DOCTYPE html>

<html>

    <head>

        <meta http-equiv="Content-Type" content="text/html;

        ![Image](img/ccc.jpg) charset=UTF-8" />
```

**2.** 应用无缓存指令，以防止缓存应用程序的内容。对于 Web 应用程序，最好不缓存任何数据（保存在临时存储中）：

```html
<meta http-equiv="pragma" content="no-cache" />
```

`<meta http-equiv="cache-control"` ![Image](img/ccc.jpg) `content="no-cache" />`

**3.** 声明应用程序的标题：

```html
<title>jQuery Application Interface</title>
```

**4.** 创建 CSS 和 jQuery/JavaScript 文件的声明，首先从你将创建的样式表开始：

```html
<link rel="stylesheet" href="css/interface.css"
![Image](img/ccc.jpg) type="text/css" />

<link type="text/css" rel="stylesheet"
![Image](img/ccc.jpg) href="css/ui/jquery-ui-1.8.12.custom.css" />

<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/jquery-1.5.min.js"></script>

<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/jquery-ui-1.8.12.custom.min.
![Image](img/ccc.jpg) js"></script>

</head>
```

标准 jQuery 文件以及 jQuery UI 的 CSS 和 JavaScript 文件都已包含在基础标记中，因此你无需担心后续添加它们。

**5.** 添加将容纳应用程序界面导航和内容的元素：

```html
<body>
    <div id="mainNavBar"></div>
    <div id="content1">
        <div id="contentArea1">
            <!-- nav items -->
        </div>
    </div>
    <div id="content2">
        <div id="contentArea2">
            <!-- content items -->
        </div>
    </div>
    <div id="footer"></div>
</body>
</html>
```

HTML 主体中包含的标记非常简单且易于阅读。每个元素都清晰声明，注释使标记易于理解。

接下来，你将为基础 HTML 标记添加一些样式。

### 应用 CSS

应用程序界面的样式表定义了用于显示内容的区域的属性。你需要清晰地描述这些区域，以便 CSS 能够有效地应用于你的标记。

让我们先设置基本的 CSS 属性，并添加一些额外的属性，为每个区域添加边框以提供视觉引导。设计完成后，你可以移除这些边框。

**1.** 在你的文本编辑器中创建一个名为 `interface.css` 的文件，将其保存在 `chap6/css` 文件夹中，然后建立整体布局：

```css
body, html {
    height:100%;
    margin: 0px auto;
    overflow-y: hidden ! important;
    overflow-x: auto ! important;  
}
```

---

> **注意**

> CSS 属性 `! important` 始终应用于标记，无论其他任何 CSS 条目是否试图覆盖该属性。CSS 是从上到下读取的，标记为 `! important` 的 CSS 属性无论出现在 CSS 文档中的哪个位置，都将始终被应用。

---

```css
body  {
    margin: 0px;
    font-family: Tahoma, Arial, Helvetica, sans-serif;
    font-size: 11px;
    background-color: #000000;
}
```

这里建立的 CSS 规则确保文档主体与浏览器窗口允许的高度一致，并将所有外边距设置为 0。所有溢出内容将被隐藏，界面文档主体上不会出现滚动条。最后，使用十六进制表示法将背景声明为黑色。

**2.** 将 `:focus` 伪选择器设置为无轮廓，这将防止在可点击项周围出现轮廓：

```css
:focus {
    outline: 0;
}
```

---

> **注意**

> 这里需要提醒一下：在公共网站上，你绝不应该关闭 `:focus` 元素上的轮廓，因为该元素有助于提高网页的可访问性。如果你的 Web 应用程序需要让使用屏幕阅读器的人能够访问，你应该从 CSS 文档中省略这条 `:focus` CSS 规则。

---

**3.** 设置二级导航的容器。有两个部分：外部容器和内部容器。先声明外部容器：

```css
#content1 {
    width: 20%;
    height: 80%;
    background-color: transparent;
    vertical-align: bottom;
    float: left;
    margin: 5px 5px 0px 10px;
    position: relative;
    bottom: 0px;
}

#contentArea1 {
    position: relative;
    padding: 10px;
}
```

外部容器 `#content1` 设计用于容纳将出现在界面左侧的导航项。由于应用程序界面设计为流式布局（所有元素随屏幕调整大小以保持比例），因此使用百分比来配置高度和宽度。

**4.** 构建用于容纳主内容的 CSS，使用一个外部容器：

```css
#content2 {
    position: relative;
    width: 77%;
    height: 80%;  
    background-color: transparent;
    vertical-align: top;
    float: left;
    margin: 5px 5px 0px 0px;
}
```

**5.** 创建主内容区域的内部容器，并将 `overflow` 属性设置为 `auto`。当内容长度超过外部容器允许的范围时，内部容器将出现滚动条：

```css
#contentArea2 {
    position: relative;
    padding: 10px;
    overflow: auto;
}
```

**6.** 声明主导航区域的空间，包括将用作导航背景的图像：

```css
#mainNavBar {
    height: 75px;
    background-image: url('../grfx/large_gray_gradient.png');
    background-repeat: repeat-x;
    padding: 0px 0px 0px 25px;
}
```

**7.** 为页脚部分创建规则和属性：

```css
#footer {
    position: absolute;
    bottom: 0px;
    height: 75px;
    width: 99%;
    margin: 5px 5px 0px 5px;
}
```

页脚与浏览器窗口底部对齐，这样稍后你在本章中创建的窗口调整大小功能就可以考虑到页脚元素所占据的已知固定空间。

图 6.2 主导航和二级导航区域以及内容和页脚区域已创建完毕，可供修改。

![Image](img/06-02.jpg)

**8.** 创建 CSS 样式表的最后一部分，其中包含用于在界面开发过程中提供视觉引导的边框规则：



```css
#content1, #content2, #footer {
    border: 1px dashed #FFFF00;
}

#contentArea1, #contentArea2 {
    border: 1px dashed #00FF00;
}
```

界面完成后，你可以移除这些规则。

基础 CSS 并不复杂，但它是实现应用程序界面所需的布局和交互性所必需的。

有了基本的 CSS 和 HTML 后，你可以将`chap6/6-1.php`加载到浏览器中（图 6.2）。你应该会看到应用程序界面每个主要区域的黄色边框（外部容器）和绿色边框（内部容器）。

请注意，某些导航和内容区域略有重叠。你将在下一节添加 jQuery 调整大小函数时纠正这种重叠。

### 使界面可调整大小

对于应用程序界面来说，每个元素不仅在浏览器打开时，而且在用户决定调整浏览器窗口大小时，都处于正确的位置并具有正确的大小，这一点非常重要。使用 jQuery 的`resize`方法可以让你完成这个微妙但重要的任务。

为了确保浏览器窗口初始打开时元素具有正确的大小，你需要知道窗口打开后的总高度。然后你可以将适当的高度应用于内容容器元素。

在本练习中，你将创建 jQuery 函数，根据浏览器窗口打开时的大小自动为所有容器元素应用适当的高度。然后，你将创建当用户更改浏览器窗口大小时调整容器元素大小的 jQuery 函数。

1. 创建一个名为`interface.js`的新文件，并将其保存在`chap6/inc/jQuery`文件夹中。然后创建文档就绪包装函数：

```javascript
$(document).ready(function() {
```

2. 使用 jQuery 的`height`方法获取浏览器窗口的高度，并将该信息存入名为`windowHeight`的变量中：

```javascript
    var windowHeight = $(window).height();
```

3. 设置两个内容外部容器和两个内容内部容器的高度。外部容器的高度需要考虑`mainNavBar`元素（75 像素）加上`footer`元素（75 像素）的高度。再额外增加 25 像素作为内边距：

```javascript
    $("#content1").height(windowHeight - 175 + "px");
    $("#contentArea1").height(windowHeight - 205 + "px");
    $("#content2").height(windowHeight - 175 + "px");
    $("#contentArea2").height(windowHeight - 205 + "px");
```

确保内部容器`contentArea1`和`contentArea2`的总高度设置正确，使其保持在外部容器内部，方法是从内部容器的高度中再减去 30 像素。

接下来，你将创建一个 jQuery`resize`函数，以确保当浏览器窗口大小改变时，内容区域能够随之调整大小。用于在浏览器打开时设置内容容器大小的相同函数，也会在调整大小事件中使用。

4. 将浏览器窗口绑定到 jQuery 的`resize`函数：

```javascript
    $(window).resize(function() {
```

5. 复制并粘贴之前用于设置内容容器高度的函数，然后用适当的括号关闭`resize`函数：

```javascript
        var windowHeight = $(window).height();
        $("#content1").height(windowHeight - 175 + "px");
        $("#contentArea1").height(windowHeight - 205 + "px");
        $("#content2").height(windowHeight - 175 + "px");
        $("#contentArea2").height(windowHeight - 205 + "px");
    });
```

6. 关闭文档就绪函数：

```javascript
});
```

现在，你已准备好将`interface.js`包含到 HTML 声明中。

7. 复制`chap6/6-1.php`，另存为`chap6/6-2.php`，并在 HTML 的 head 部分添加一个 script 标签，以调用`chap6/inc/jQuery/interface.js`的源文件：

```html
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/interface.js"></script>
```

图 6.3 展示了在应用处理内容区域大小的 jQuery 函数之前，内容区域与页脚元素重叠的情况。

![Image](img/06-03.jpg)

8. 在浏览器窗口中打开`chap6/6-2.php`。你会看到内容区域不再与页脚部分重叠（图 6.3）。调整浏览器窗口大小，观察内容区域是否正确调整大小。

基本布局已完成，可以进一步开发为你的 Web 应用程序界面。让我们通过引入一个强大的精灵元素作为应用程序的主要导航来开始开发。

---

注意

如果你将浏览器窗口调整得非常小，以至于实际上无法使用，内容区域将再次开始相互重叠，因为在浏览器分配的空间内没有它们可放置的位置。

---

### 改进应用程序界面

图 6.4 展示了将在 Web 应用程序界面中使用的精灵。

![Image](img/06-04.jpg)

在 Web 应用程序界面的基本框架建立之后，你可以开始应用 jQuery 函数和小部件，为应用程序用户创造丰富的交互体验。

你将应用在前几章中学到的一些技术，包括处理事件和使用 jQuery UI 小部件。这些技术和小部件将为你的应用程序提供直观的用户交互，同时利用 jQuery 库提供的效率，使你的应用程序能够流畅运行。

首先，让我们采用你在第 2 章中学到的简单精灵导航技术，并提升该技术的能力，使其在 Web 软件应用程序中以不同但更有效的方式运行。

#### 创建更好的精灵

你在第 2 章中使用的精灵交互相当简单：将鼠标悬停在一个元素上，它就会改变；将光标移开，它就会恢复为正常外观。对于本章中创建的 Web 应用程序界面，交互需要稍微复杂一些。精灵不仅需要反映悬停状态，还需要反映用户选择在应用程序中工作的区域的第三种状态（选中状态）。

因此，你需要配置一个包含三行的精灵图像（图 6.4）。你可以在下载文件的`chap6/grfx/main_nav.png`中找到此图像。

当鼠标光标悬停在精灵中的某个项目上时，图标将变为黄色，然后当光标移开该图标时，图标会逐渐变回灰色。这与之前创建的精灵发生的动作相同。不同之处在于，选中的项目在光标悬停时不会改变，而点击的精灵项目将获得选中状态，图标变为白色。

要使精灵按你期望的方式做出反应，有两个关键方面：CSS 和 jQuery。在准备好 CSS 和 jQuery 代码后，你将把精灵添加到 HTML 中。让我们先创建 CSS。

##### 为精灵设置样式

使精灵正常工作关键在于在页面中为精灵容器设置样式，并确保精灵的每个元素都在 CSS 中定义。

1. 在文件夹`chap6/css/spritenav`中创建一个名为`spritenav.css`的 CSS 文件，并设置第一个属性，该属性将设置精灵的高度。该规则还将包含一个属性，用于移除将用于精灵的无序列表的默认样式：

```css
   #spriteNav {
      height: 75px;
      list-style: none;
      margin: 0;
      padding: 0;
   }
```

2. 确保所有列表项向左浮动，以便它们能够并排排列：

```css
   #spriteNav li {
      float: left;
   }
```

3. 为精灵容器内的锚点标签设置样式。锚点标签的背景图像是定义精灵的图形：

```css
   #spriteNav li a {
      background: url(../../grfx/main_nav.png) no-repeat;
      display: block;
      height: 75px;
      position: relative;
   }
```

4. 添加精灵的`span`元素的样式。`span`元素是精灵中的图像项，当光标悬停在元素上时会出现。`span`的背景图像与锚点元素使用的精灵图形相同，即`chap6/grfx/main_nav.jpg`：

```css
   #spriteNav li a span {
      background: url(../../grfx/main_nav.png) no-repeat;
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      height: 75px;
      width: 100%;
   }
```

5. 为每个项目设置起始基础`width`和`background-position`。精灵中的每个导航项目都必须有起始宽度和位置。由于起始位置是精灵的顶行，每个项目的`y`坐标为`0px`。所有精灵项目的宽度均为 100 像素：

```css
   #spriteNav li a#users {
      width: 100px;
   }
   #spriteNav li a#notes {
      width: 100px;
      background-position: -100px 0px;
   }
   #spriteNav li a#stats {
      width: 100px;
      background-position: -200px 0px;
   }
   #spriteNav li a#processes {
      width: 100px;
      background-position: -300px 0px;
   }
   #spriteNav li a#security {
      width: 100px;
      background-position: -400px 0px;
   }
```

6. 添加下一组样式规则，以定义`span`元素的精灵项目位置。`span`元素提供悬停效果。精灵项目位于精灵的第二行，因此这些项目的`y`坐标必须为`-75px`：

```css
   #spriteNav li a#users span {
      background-position: 0px -75px;
   }
```

```css
   #spriteNav li a#notes span {
      background-position: -100px -75px;
   }
   #spriteNav li a#stats span {
      background-position: -200px -75px;
   }
   #spriteNav li a#processes span {
      background-position: -300px -75px;
   }
   #spriteNav li a#security span {
      background-position: -400px -75px;
   }
```

7. 准备精灵图的最后一行——即当某个项目被选中时显示的图像——其`y`坐标为`-150px`：

```css
   #spriteNav li a#users span.selected {
       background-position: 0px -150px;
   }
   #spriteNav li a#notes span.selected {
       background-position: -100px -150px;
   }
   #spriteNav li a#stats span.selected {
       background-position: -200px -150px;
   }
   #spriteNav li a#processes span.selected {
       background-position: -300px -150px;
   }
   #spriteNav li a#security span.selected {
       background-position: -400px -150px;
       text-decoration: none;
   }
```

基于精灵图的导航样式现已完成。接下来，你需要将注意力转向 jQuery，它将为精灵图增添亮点。

##### 创建精灵图交互

精灵图的 jQuery 代码由两个函数定义，一个用于处理悬停操作，另一个用于处理点击或选中的精灵图项目。

1. 在文件夹`chap6/inc/jQuery`中创建一个名为`spreitenav.js`的文件，并建立文档就绪函数：

```javascript
$(document).ready(function() {
```

2. 将`hover`函数和`click`函数包装到一个单一的函数调用中，使它们相互关联：

```javascript
$(function() {
```

这一步并非必须，但在代码组织方面会带来极大的好处。

3. 为`span`和`span selected`元素的可见性设置默认值：

```javascript
$("#spriteNav span").css("opacity", "0");
$("#spriteNav span.selected").css("opacity", "1");
```

4. 开始编写`hover`函数，将`hover`方法绑定到`#spritenav span`元素：

```javascript
$("#spriteNav span").hover(function() {
```

5. 创建一个条件判断，测试当前悬停的`span`元素是否定义了 CSS 类属性。如果没有定义 CSS 类，则应用 jQuery 动画，淡入该元素的黄色精灵图项目：

```javascript
if($(this).attr("class").length == 0) {
    $(this).stop().animate({
        opacity: 1
    }, 75);
```

6. 如果鼠标光标所在的元素附加了 CSS 类，则将该元素的不透明度设置为 1，使其完全可见：

```javascript
} else {
    $(this).css("opacity", "1"); // 结束鼠标进入
};
```

`hover`方法的`mouseover`部分现已完全定义，接下来将进入`hover`事件的`mouseout`部分。

7. 如果元素没有附加 CSS 类，则将淡出时间设置为 250 毫秒，使淡出持续时间稍长：

```javascript
}, function(){
    if($(this).attr("class").length == 0) {
        $(this).stop().animate({
            opacity: 0
        }, 250);
```

8. 如果元素附加了类，则无论鼠标光标位置如何，都保持项目完全可见。该类表示该项目是当前选中的元素：

```javascript
} else {
    $(this).css("opacity", "1"); // 结束鼠标离开
};
```

9. 使用正确的结束括号和花括号关闭`hover`方法：

```javascript
}); // 结束 hover 函数
```

10. 开始定义`click`函数，将 jQuery 的`click`方法绑定到`#spritenav span`元素：

```javascript
$("#spriteNav span").click(function() {
```

11. 首先从所有`#spritenav`元素中移除选中的类，使当前元素成为唯一选中的元素：

```javascript
$("#spriteNav span").removeClass("selected");
```

12. 使用 jQuery 的`addClass`方法将`selected`类添加到该元素：

```javascript
$(this).addClass("selected");
```

13. 将所有没有`selected`类的`#spritenav`元素淡化为灰色状态：

```javascript
$("#spriteNav span:not(.selected)").stop().animate({
    opacity: 0
}, 0);
```

这会将之前选中的项目恢复为灰色（即未选中或悬停状态）。

14. 添加适当的结束括号和花括号：

```javascript
        });
    });
});
```

现在 CSS 和 jQuery 已就位，为精灵图提供了功能，剩下的工作就是添加标记，将精灵图放入应用程序界面。

##### 将精灵图添加到界面

你已经做了大量准备工作，现在可以开始向 Web 应用程序界面添加功能了。你可以依靠之前构建的 HTML 标记和 CSS 作为指导，将新元素放入 Web 应用程序界面。

1. 复制`chap6/6-2.php`，并将其保存到`chap6`文件夹中，命名为`6-3.php`。

2. 添加声明，将`spritenav.css`和`spritenav.js`链接到新文件 HTML 标记的 head 部分，如下所示：



```html
<link rel="stylesheet" href="css/interface.css"
![Image](img/ccc.jpg) type="text/css" />
<link rel="stylesheet" href="css/spritenav/spritenav.css"
![Image](img/ccc.jpg) type="text/css" />
<link type="text/css" rel="stylesheet" href="css/ui/jquery-ui
![Image](img/ccc.jpg) -1.8.12.custom.css" />
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/jquery-1.5.min.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/jquery-ui-1.8.12.custom.min.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/interface.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/spritenav.js"></script>
```

图 6.5. 当鼠标光标悬停在“进程”项目上时，“用户”为选中项目。

![Image](img/06-05.jpg)

**3.** 找到`id`为`mainNavBar`的`div`元素，并将无序列表放置在该元素内：

```html
<div id="mainNavBar">
    <ul id="spriteNav">
```

**4.** 设置一个默认元素具有`selected`类，如下所示（可选）：

```html
<li><a id="users"><span class="selected"></span></a></li>
```

**5.** 确保每个精灵图项目都有一个列表元素：

```html
<li><a id="notes"><span></span></a></li>
<li><a id="stats"><span></span></a></li>
<li><a id="processes"><span></span></a></li>
<li><a id="security"><span></span></a></li>
</ul>
</div>
```

精灵图导航已完成，可以测试了。

**6.** 在浏览器中加载`chap6/6-3.php`以查看导航（**图 6.5**）。

应用程序界面随着主导航的建立开始成形。你不再需要修改在`chap6/6-3.php`中定义的基本布局。从此刻起，所有更改都在文件（CSS 和 jQuery 文件）中进行，这些文件将从其他文件加载内容到界面中。

接下来，你将学习如何让主导航加载次级导航项和主要内容。

图 6.6. 点击任意一个标题，内容将以手风琴效果展开，根据需要上下滑动内容和标题。

![Image](img/06-06.jpg)

#### 使用 AJAX 加载内容

使用 jQuery 选择器可以轻松定位 Web 应用程序界面的内容区域。一旦定位了某个区域，就可以使用 jQuery 的 AJAX 方法之一将外部内容调用到界面中。

你可以加载到这些内容区域的内容没有限制。你创建的内容，以及 jQuery 插件和 jQuery UI 小部件，都可以包含到应用程序界面中。

你可以同时将内容加载到多个区域。例如，通过一次`click`事件，你可以在将内容加载到主要内容区域的同时，将内容加载到辅助导航区域。

我们先来看一种将 jQuery UI 折叠面板（Accordion）组件加载到导航区域的技术。

### 包含 jQuery UI 组件

一种在有限空间内显示大量内容的流行组件是 jQuery UI 折叠面板（Accordion）组件。折叠面板占用固定空间，通过点击面板的标题可以滑动显示内容窗口。**图 6.6**展示了一个包含三个部分的 jQuery UI 折叠面板，并显示了内容 C 部分的内容。

你将使用 jQuery UI 折叠面板组件来辅助导航。让我们先准备这个组件，然后添加从主导航调用该组件的代码，以便打开折叠面板。

**1.** 在`chap6/inc/nav`中创建一个名为`users.php`的新页面。此文件夹将用于存储所有辅助导航文件。

**2.** 添加以下 jQuery 代码，将 jQuery UI 的`accordion`方法绑定到`id`为`accordion`的元素上：

```html
<script type="text/javascript">
    $(document).ready(function() {
        $('#accordion').accordion();
    });
</script>
```

**3.** 创建用于容纳`accordion`元素的`div`：

```html
<div id="accordion">
```

**4.** 为折叠面板的每个部分添加标题和内容。注意，标题包含在标题（`h3`）标签中：

```html
    <h3><a href="#">管理用户</a></h3>
    <div>
        <ul>
            <li><a href="#" id="addUser">添加用户</a></li>
            <li><a href="#" id="addUser">编辑用户</a></li>
        </ul>
    </div>
    <h3><a href="#">管理角色</a></h3>
    <div>
        <ul>
            <li><a href="#" id="addUser">添加角色</a></li>
            <li><a href="#" id="addUser">编辑角色</a></li>
        </ul>
    </div>
```

**5.** 添加最后一个折叠面板部分，并关闭`accordion`元素：

```html
    <h3><a href="#">管理群组</a></h3>
    <div>
        <ul>
            <li><a href="#" id="addUser">添加群组</a></li>
            <li><a href="#" id="addUser">编辑群组</a></li>
        </ul>
    </div>
</div>
```

jQuery UI 库（包括库自带的 CSS）负责处理创建折叠面板和管理动画的细节；剩下的工作就是添加 jQuery 代码，将折叠面板加载到界面中。

与其创建一个新文件来编写将项目加载到应用程序界面的 jQuery 代码，不如将代码添加到之前创建的脚本文件`chap6/inc/jQuery/interface.js`中。

**1.** 打开`interface.js`文件，并准备在之前放入文件的窗口`resize`函数之后添加代码。

**2.** 在第一行，将`click`函数绑定到包含在`#spritenav`列表项锚点标签中的主导航元素上：

```javascript
$('#spriteNav li a').click(function(){
```

**3.** 获取被点击项的`id`属性值，并将其放入变量`clicked`中：

```javascript
    var clicked = $(this).attr('id');
```

如果你在命名文件时足够聪明，就可以利用属性值（如上一行代码中的`id`属性）来创建适用于多种事件的单一函数。在本例中，要加载的导航文件名为`users.php`。这意味着文件名与被点击项关联得很好。

图 6.7. jQuery UI 折叠面板组件已准备好作为 Web 应用程序界面的辅助导航元素。

![Image](img/06-07.jpg)

**4.** 创建一个名为`loadNav`的变量，用于保存要加载的文件名和路径。注意，变量`clicked`用于补全路径文本：

```javascript
    var loadNav = 'inc/nav/' + clicked + '.php';
```

**5.** 使用 jQuery AJAX 的简写方法`load`将折叠面板加载到`contentArea1`中，完成该函数：

```javascript
    $('#contentArea1').load(loadNav);
});
```

**图 6.7**展示了你的辛勤工作成果。jQuery UI 折叠面板组件已加载到辅助导航区域，并准备就绪。

需要注意的是，你无需修改主界面，因为 jQuery UI 脚本文件和 CSS 已经包含在内。此外，将 UI 组件绑定在其使用文件中的技术是避免复杂脚本文件的最佳方式。

在加载的文件中会使用额外的 jQuery 代码，因为这是组织应用程序的更好方式。将 jQuery 代码隔离在各自需要的文件中，有助于将函数模块化，以便在调用它们的地方使用，而不是将所有函数始终加载到界面中。这样可以减少加载时间，并且更容易追踪代码中的问题。应用程序界面也更容易扩展，因为新代码可以放入扩展应用程序的模块中。

### 同时加载多个项目

使用 jQuery，可以轻松扩展函数，使其能够同时处理多个事件。为了演示这一能力，你将创建一个小的表单，该表单将在 jQuery UI 折叠面板组件加载到 Web 应用程序界面的辅助导航区域的同时，加载到主要内容区域。

**1.** 创建一个名为`users_search.php`的表单，并将其保存在`chap6/inc/content`文件夹中。

**2.** 添加一个小表单的 HTML 标记：

```html
<form action="#" method="post" id="search_form">
    <fieldset>
        <label>名字</label><input type="text"
        ![Image](img/ccc.jpg) name="first_name" id="first_name" /><br />
        <label>姓氏</label><input type="text"
        ![Image](img/ccc.jpg) name="last_name" id="last_name" /><br />
        <label></label><input type="submit" name="search"
        ![Image](img/ccc.jpg) id="search" value="搜索" /><br />
    </fieldset>
</form>
```

**3.** 扩展上一节（`chap6/inc/jQuery/interface.js`）中定义的`click`函数，添加两行代码：一行定义要加载的路径和文件名，另一行用于应用于新文件的`load`方法：

```javascript
$('#spriteNav li a').click(function(){
    var clicked = $(this).attr('id');
    var loadNav = 'inc/nav/' + clicked + '.php';
    var loadContent = 'inc/content/' + clicked + '_search.php';
    $('#contentArea1').load(loadNav);
    $("#contentArea2").load(loadContent);
});
```

图 6.8. 多个项目已由`load`方法处理，并放置到 Web 应用程序界面的不同部分。

![Image](img/06-08.jpg)

**图 6.8**显示了点击主导航区域中*用户*图标的结果。表单被加载到主要内容区域，而 jQuery UI 折叠面板组件出现在辅助导航区域。

可以想象，只要规划得当并保持代码组织有序，从不同来源将内容加载到 Web 应用程序界面的内容区域并不复杂。即使是大量内容，也能轻松显示在界面中。

### 处理大量内容

当你有包含多个部分的表单或扩展到数百行的表格数据时，最好将这些信息保持在 Web 应用程序界面内显示，而无需滚动整个窗口内容。滚动整个窗口会使导航元素和标识内容的标题移出视野，可能会让用户感到困惑，或者至少导致用户上下滚动以辨别数据的某些信息。任何相关的页脚都不会立即可见，用户可能永远不会向下滚动足够远以获取该元素的信息。

这并不是说你不应该构建会导致整个内容窗口滚动的界面。如果你确实在某个设计元素中允许这样做，就需要确保无论用户滚动到何处，都能有一种方式来识别内容和数据。大多数设计师会通过在内容旁边紧邻放置内容标识，或者每隔几行重复表格的列标题来实现这一点。

你为 Web 应用程序界面构建的 CSS 提供了恰当的结构，既能保持内容的可用性，又不会失去显示主要和次要导航区域以及页脚（如果包含任何内容）的能力。

下载包中提供了一个名为`users_add.php`的大表单，你可以用它来测试你的界面。该表单位于`chap6/inc/content`文件夹中，并包含一些 jQuery 函数，包括 jQuery UI Tabs 小部件。

要将表单加载到内容区域，你需要修改之前在`chap6/inc/nav`中创建的`users.php`文件。

**1.** 打开`users.php`文件，并添加以下（高亮显示的）jQuery 代码：

```javascript
$(document).ready(function() {

    $('#accordion').accordion();

    $('#addUser').click(function(event) {

        event.preventDefault();

        $('#contentArea2').load('inc/content/users_add.php');

    });

});
```

由`addUser`标识的元素被绑定到 jQuery 的`click`方法，以将表单`inc/content/users_add.php`加载到`contentArea2`中。

图 6.9. 加载到 Web 应用程序界面中的表单。

![Image](img/06-09.jpg)

**2.** 在浏览器中重新加载`6-4.php`，并点击*Users*图标。

**3.** 当 jQuery UI Accordion 小部件加载后，你可以点击*Add User*。带选项卡的表单应出现在内容区域中（**图 6.9**）。

图 6.10. 由于内容超出了其所定位屏幕区域的大小，滚动条会自动出现。

![Image](img/06-10.jpg)

通常超出浏览器窗口底部的内容现在被限制在内容区域的边界内。该界面区域在需要时会获得一个滚动条。**图 6.10**显示了当点击 Security 选项卡时，由于该选项卡包含的内容量较大，滚动条出现的情况。

现在你已经配置好了基本的 Web 应用程序界面，并且能够轻松地将内容加载到各个区域，接下来让我们看看一些能够增强 Web 应用程序界面的附加功能。

图 6.11. Mozilla Firefox 浏览器中的标准上下文菜单。在大多数基于 Web 的应用程序中，这些选项作用不大。

![Image](img/06-11.jpg)

#### 配置附加增强功能

由于你正在构建一个 Web 应用程序，你需要关注用户如何与你的应用程序交互。他们是否使用了鼠标右键功能？他们是否点击了后退按钮而不是使用导航元素？你是否想限制或修改用户访问浏览器内置功能的能力？有了这些问题的答案，你可以应用一些 jQuery 技术来实现这些增强功能。

##### 禁用右键上下文菜单

通过鼠标右键激活的上下文菜单（**图 6.11**）中的许多操作项在基于 Web 的应用程序中并不适用。因此，你可以选择禁用用户右键点击时出现的上下文菜单。使用 jQuery，你只需应用一小段代码即可实现。

打开你之前创建的 jQuery 脚本文件`interface.js`（位于`chap6/inc/jQuery`中），并在文档就绪包装函数的结束括号之前插入以下代码：

```javascript
$(document).bind("contextmenu",function(e){

    e.preventDefault();

});
```

这段 jQuery 代码将`contextmenu`事件绑定到文档，然后对上下文菜单应用`preventDefault`处理程序。这将阻止右键点击时弹出上下文菜单。

你可能已经猜到，还有一些 jQuery 上下文菜单插件可用。这些插件允许你为 Web 应用程序创建自定义上下文菜单。请查看我最喜欢的 jQuery 上下文菜单插件：[`abeautifulsite.net/blog/2008/09/jquery-context-menu-plugin`](http://abeautifulsite.net/blog/2008/09/jquery-context-menu-plugin)。让我们为其中一个界面元素添加一个自定义上下文菜单。

**1.** 打开`chap6/inc/jQuery`文件夹中的`interface.js`，并将你之前创建的用于禁用右键上下文菜单的代码用注释括起来：

```javascript
/*$(document).bind("contextmenu",function(e){

    e.preventDefault();

});*/
```

添加注释后，你可以保存文件。现在右键功能再次可用；自定义上下文菜单需要用到它。



**2.** 打开`6-3.php`，并将其另存为`chap6`文件夹中的`6-4.php`。你也可以将代码添加到`6-3.php`中，但为了保持一致性（以及备份原始工作），复制一份是更稳妥的做法。

**3.** 将 jQuery Context Menu CSS 和 jQuery 文件的源引用添加到`chap6/6-4.php`的 head 部分（高亮显示）：

```html
<link rel="stylesheet" href="css/interface.css"
![Image](img/ccc.jpg) type="text/css" />
<link rel="stylesheet" href="css/spritenav/spritenav.css"
![Image](img/ccc.jpg) type="text/css" />
<link type="text/css" rel="stylesheet"
![Image](img/ccc.jpg) href="css/ui/jquery-ui-1.8.12.custom.css" />
<link type="text/css" rel="stylesheet"
![Image](img/ccc.jpg) href="css/contextmenu/jquery.contextMenu.css" />
<script type="text/javascript" src="inc/jQuery/jquery
![Image](img/ccc.jpg) -1.5.min.js"></script>
<script type="text/javascript" src="inc/jQuery/jquery-ui
![Image](img/ccc.jpg) -1.8.12.custom.min.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/interface.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/spritenav.js"></script>
<script type="text/javascript"
![Image](img/ccc.jpg) src="inc/jQuery/jquery.ContextMenu.js"></script>
```

---

> **注意**
>
> jQuery Context Menu 插件附带一个名为`images`的文件夹。将这个文件夹放在与`jquery.contextMenu.css`文件相同的文件夹中非常重要。

---

**4.** 创建一个名为`notes.php`的文件，并将其保存在`chap6/inc/nav`文件夹中。

**5.** 将 jQuery UI Accordion 小部件的 jQuery 代码添加到`notes.php`文件中：

```javascript
<script type="text/javascript">

    $(document).ready(function() {

        $('#accordion').accordion();
```

**6.** 将`click`方法绑定到`addNotes`元素：

```javascript
        $('#addNotes').click(function(event) {

            event.preventDefault();
```

**7.** 定义 jQuery AJAX 加载函数以检索正确的文件，然后关闭文件的脚本部分：

```javascript
            $('#contentArea2').load('inc/content/notes_add.php');

        });

    });

</script>
```

**8.** 构建导航手风琴的 HTML 标记：

```html
<div id="accordion">

    <h3><a href="#">管理笔记</a></h3>

    <div>

        <ul>

            <li><a href="#" id="addNotes">添加笔记</a></li>

            <li>编辑笔记</li>

        </ul>

    </div>

</div>
```

由于你在`interface.js`中构建了基于精灵的可靠导航函数，现在你可以在浏览器中加载`chap6/6-4.php`，并点击 Notes 使`note.php`出现在界面的左侧内容区域。完成这一步后，你就可以着手创建内容，以展示 jQuery Context Menu 插件。

**1.** 在`chap6/inc/content`文件夹中创建一个名为`notes_add.php`的文件。

**2.** 输入 jQuery 代码，将`contextMenu`绑定到`noteBody`元素：

**3.** 将`id notesContext`分配给 jQuery Context Menu 插件的`menu`选项，然后关闭脚本标签：

```javascript
<script type="text/javascript">
    $(document).ready(function() {
        $("#noteBody").contextMenu({
            menu: 'notesContext'
        });
    });
</script>
```

**4.** 为`notes_add.php`的内容创建一个 HTML 表单：

```html
<form action="#" method="post" id="search_form">
    <fieldset>
        <label>笔记标题</label><input type="text"
        ![Image](img/ccc.jpg) name="noteTitle" id="noteTitle" size="64" /><br />
        <label>内容</label><textarea name="noteBody"
        ![Image](img/ccc.jpg) id="noteBody" cols="64" rows="16"></textarea>
        <label></label><input type="submit" name="saveNote"
        ![Image](img/ccc.jpg) id="saveNote" value="保存笔记" /><br />
    </fieldset>
</form>
```

**5.** 构建一个无序 HTML 列表，用于包含要在自定义上下文菜单中显示的每个项目：

```html
<ul id="notesContext" class="contextMenu">
    <li class="edit">
        <a href="#edit">编辑</a>
    </li>
    <li class="cut separator">
        <a href="#cut">剪切</a>
    </li>
    <li class="copy">
        <a href="#copy">复制</a>
    </li>
    <li class="paste">
        <a href="#paste">粘贴</a>
    </li>
    <li class="delete">
        <a href="#delete">删除</a>
    </li>
    <li class="quit separator">
        <a href="#quit">退出</a>
    </li>
</ul>
```

**6.** 在 Web 浏览器中重新加载`chap6/6-4.php`，然后点击“笔记”以加载“管理笔记”菜单。

**7.** 点击“添加笔记”，即可在主内容区域看到笔记界面。

图 6.12. 新的 jQuery 自定义上下文菜单小部件显示在 Web 应用程序界面上。

![Image](img/06-12.jpg)

由于您已将自定义上下文菜单绑定到`noteBody`元素，现在可以在界面的文本区域内右键单击，以查看自定义上下文菜单（图 6.12）。

由于 jQuery 自定义上下文菜单基于基本的无序 HTML 列表构建，因此您可以轻松地将功能绑定到列表中的所有元素。jQuery 自定义上下文菜单的 CSS 易于理解，并且可以轻松扩展，添加额外的图标以支持您想要添加到菜单中的任何操作。您可以声明自定义上下文菜单并将其分配给任何界面。

比上下文菜单更令人头疼的问题是经常令人困扰的“后退”按钮。处理“后退”按钮以及随之而来的浏览器历史记录，是开发 Web 应用程序界面的一个重要因素。

### 处理后退按钮

如果您想成为创建 Web 应用程序的专家，就必须考虑浏览器的“后退”按钮以及浏览器管理历史记录的方式。“后退”按钮是 Web 浏览器的一项无法禁用的功能，因此最好在规划 Web 应用程序时，就考虑好如何处理浏览器历史记录以及用户将如何操作“后退”按钮。

与其从头开始处理“后退”按钮，不如直接使用一个 jQuery 插件——由开发者“牛仔”Ben Alman 编写的“后退按钮与查询（BBQ）库”。该插件可在[`benalman.com/projects/jquery-bbq-plugin`](http://benalman.com/projects/jquery-bbq-plugin)获取，它是一个小巧但非常有效的插件，允许您在 Web 应用程序中控制浏览器历史记录。jQuery BBQ 插件还允许您为 Web 应用程序中的“页面”设置书签（如果您选择启用该功能）。

由于 BBQ 插件的灵活性，它为开发者提供了多种选项，用于引导用户浏览 Web 应用程序的历史记录。jQuery BBQ 插件将使您能够管理页面上多个小部件的历史记录（例如，您可以同时控制用于导航的手风琴和用于数据输入的选项卡界面的历史记录）。更重要的是，当正确使用 BBQ 插件时，它允许您在 Web 应用程序界面中保留“后退”按钮的启用状态。

由于应用 jQuery BBQ 插件的方法有很多，我鼓励您访问 Ben 的网站，阅读文档并查看示例。然后下载该插件，构建一些小规模的示例，以了解插件的工作方式以及 BBQ 提供的选项。一旦您完成了这些，就可以将 jQuery BBQ 插件应用到一些更大的 Web 应用程序界面项目中了。

在开发 Web 应用程序界面时，您需要处理的最后一项内容是向应用程序的用户提供有用的提示。

### 提供上下文帮助

当您设计复杂的 Web 应用程序界面时，应该为用户提供文档（无论是印刷版还是在线版）。文档旨在引导他们完成使用应用程序的过程。您经常会听到人们抱怨：“我不需要看说明书！”然后用户仅凭直觉就开始使用应用程序。

图 6.13. 将鼠标悬停在 Web 应用程序界面的元素上，会显示一个上下文帮助框。

![Image](img/06-13.jpg)

作为 Web 应用程序开发者，当应用程序可能不像用户（或您）想象的那么直观时，您可以向使用应用程序的访问者提供优雅的提示。为此，您可以提供上下文帮助。

上下文帮助功能会在用户将鼠标光标悬停在已分配特定类和属性的元素上时，提供更多信息（图 6.13）。上下文帮助窗口仅在鼠标光标停留在元素上时出现，以避免因信息过多和弹出窗口过多而让用户感到困扰。

要设置上下文帮助功能，您需要先设置 CSS。打开您之前创建的 CSS 文件`interface.css`，它位于`chap6/css`文件夹中。在文件末尾添加以下两条 CSS 规则：

```css
.contextHelp {
    cursor: help;
    position: relative;
}

.contextHelpWrapper {
    width: 175px;
    padding: 10px;
    border: 4px solid #0066CC;
    background-color: #FFFFCC;
    color: #000000;
    position: absolute;
    top: 20px;
    display: none;
    font-weight: bold;
    font-size: 9pt;
    z-index: 10000;
}
```

CSS 规则将光标更改为帮助样式，以提醒用户某个元素提供了上下文帮助，并设置了上下文帮助框的样式。

接下来，让我们创建支持上下文帮助界面的 jQuery 函数。

**1.** 打开您之前在`chap6/inc/jQuery`文件夹中创建的`interface.js`文件，以添加上下文帮助函数。

**2.** 使用`delegate`方法将`mouseover`和`mouseout`事件附加到`contextHelp`类选择器：

```javascript
$('body').delegate('.contextHelp', 'mouseover mouseout',
![Image](img/ccc.jpg) function(event){
```

这里使用`delegate`方法是为了确保上下文帮助函数对所有具有正确类的元素都可用，即使这些元素尚未存在于 DOM 中。例如，当您通过单击链接加载一个具有`contextHelp`类的界面元素时，`delegate`方法会确保该元素被附加到上下文帮助函数上。

**3.** 测试是否发生了`mouseover`事件：

```javascript
    if(event.type == 'mouseover'){
```

**4.** 从元素中获取`title`信息，并将其存储在变量`this.helpText`中：

```javascript
        this.helpText = $(this).attr('title');
```

**5.** 向当前元素追加一个`div`，该`div`的`class`为`contextHelp`：

```javascript
        $(this).append('<div class="contextHelpWrapper">' +
        ![Image](img/ccc.jpg) this.helpText + '</div>');
```

该`div`用于包含来自`title`属性的文本。这些文本是将会显示给用户的上下文帮助信息。

**6.** 移除`title`属性以阻止默认行为：

```javascript
$(this).removeAttr('title');
```

在正常情况下，浏览器会将`title`属性显示为一个小工具提示。

**7.** 将具有`class`为`contextHelp`的元素的`width`存入变量`helpWidth`：

```javascript
var helpWidth = $(this).width();
```

宽度信息将用于设置上下文帮助相对于当前元素的显示位置。

**8.** 应用 CSS，根据变量`helpWidth`定义上下文帮助框的左边缘：

```javascript
$('.contextHelpWrapper').css({left:helpWidth-25});
```

**9.** 创建一个函数来容纳上下文帮助元素的`fadeIn`方法：

```javascript
function helpDisplay() {
    $('.contextHelpWrapper').fadeIn(400);
}
```

`helpDisplay`函数将被 JavaScript 的`setTimeout`方法使用，以延迟上下文帮助元素的出现。

**10.** 设置`setTimeout`方法，调用`helpDisplay`函数并将可见性延迟 1250 毫秒：

```javascript
setTimeout(helpDisplay, 1250);
```

**11.** 测试`mouseout`方法是否已被调用：

```javascript
} else if (event.type == 'mouseout') {
```

**12.** 将`title`属性恢复到`contextHelp`元素，以便可以再次使用：

```javascript
$(this).attr('title', this.helpText);
```

**13.** 使用 jQuery 的`fadeOut`方法使上下文帮助元素消失：

```javascript
$('.contextHelpWrapper').fadeOut(100);
```

**14.** 移除上下文帮助框，并用正确的花括号和方括号关闭函数：

```javascript
$('.contextHelpWrapper').remove();
};
```

要使用上下文帮助功能，你需要将`contextHelp`类与`title`属性一起应用于任何你想要显示帮助提示的元素。请看以下两个标记示例：

```html
<label class="contextHelp" title="Make sure to use a strong

![Image](img/ccc.jpg) password">Password</label>
```

```html
<a href="#" class="contextHelp" title="Add, edit and manage

![Image](img/ccc.jpg) application users">
```

图 6.14。上下文帮助功能附加到一个表单元素上，以提示用户提供强密码。

![Image](img/06-14.jpg)

`class`属性是 jQuery 函数的钩子，而`title`属性包含将显示给用户的文本（**图 6.14**）。

你可以调整上下文帮助框的位置和延迟时间，以适应你的喜好，并在你的 Web 应用程序和网站中使用。

### 总结

Web 应用程序界面为你提供了许多额外的 jQuery 技术，可以应用于你的网站和基于 Web 的应用程序。你还可以应用本书前面提供的工具，为你的客户在使用你的应用程序和网站时创建令人兴奋的交互性。



在本章中，你学习了如何将所有 jQuery 知识组合成一个包，以满足高度交互式 Web 应用程序的需求。你应用了 jQuery UI 小部件和开发者插件，以及手工制作的 jQuery 脚本，创建了一个有吸引力且实用的 Web 应用程序模板。

请务必访问本书的网站[`www.appliedjquery.com`](http://www.appliedjquery.com)，获取更多示例、文章、插件以及关于 *Applied jQuery* 的更多内容。

---

> **注意**
>
> 你可以为 Web 应用程序界面创建更多的函数和接口。使用本章提供的基础，尝试 jQuery 事件、小部件和插件。这个界面远未完成，这将为你提供许多机会来应用所学知识，并进一步了解 jQuery 的精彩世界。

---

## 索引

### 符号

`$`（美元符号），与插件一起使用，200

`)`（圆括号），用于关闭代码，4

`//`（双斜杠），用于注释，8

`/*`（斜杠星号），用于注释，8

`}`（花括号），用于关闭代码，4

### A

Accordion 小部件

特性，149

使用，226–229

账户页面，显示，107

操作，使用 Firebug 检查，11

`addClass` 方法，与精灵图一起使用，223

`addMovie` 表单，绑定到`submit`方法，124

AJAX（异步 JavaScript 和 XML），92。*另见* JavaScript

处理大量内容，231–234

包含 jQuery UI 小部件，226–229

加载多个项目，230–231

AJAX 调用，触发事件，118–125

AJAX 内容更新

基于请求，110–111

基于用户，108–110

加载脚本，112–116

AJAX 附加功能

`ajaxSetup` 低级接口，116

JSON（JavaScript 对象表示法），126–133

低级接口，116–117

触发事件，118–126

`ajax` 方法，使用，117–118

AJAX 方法

`getScript`，112–116

HTTP 请求，93

`load`，110–111

`post`，103

XMLHttpRequest，93

AJAX 请求

清理用户提供的数据，141–144

用于识别用户的 Cookie，139–141

与 JSONP AJAX 请求对比，128

MD5 哈希，139–140

防止表单提交，135–138

提供选项，116

安全性，134

安全传输数据，144

AJAX 验证

`post` 函数的回调，101

复选框，94

PHP 函数的连接，93

Cookie 设置，98–100

`data` 变量，101

`else` 语句，96–97

错误消息，101–102

插入用户信息，94

用户登录，105–107

模态窗口，104

`mysql_query` PHP 函数，96

`mysqlErrorNum` 变量，103–104

`newName` 变量，101

密码，94

用于用户登录的 PHP，97–100

PHP 注册，92–100

PHP 的`switch`方法，93–94

注册表单，94–95

注册函数，102–105

SQL 语句，94–95

用户名，94

用户名和`blur`方法，100

用户名可用性，96–97

验证`post`方法，100–102

验证文件，92–100

验证函数，100–102

`ajaxSetup` 低级接口，116

`ajaxStart` 方法

调用等待指示器，125

使用，119–121，123

`ajaxStop` 方法

绑定，123

使用，119–121

Alman, Ben，241

锚点标签，创建，4

动画图形网站，125

动画

添加到基于精灵图的导航，55–56

缓动，38

动画方法

不可见元素，30

为模态窗口调用，30

可见元素，30

应用程序界面

添加精灵图，224–225

返回按钮，241

内容区域，206

上下文帮助，241–246

CSS（层叠样式表），209–214

禁用右键上下文菜单，235–240

页脚，206

HTML（超文本标记语言），207–208

改进精灵图，217–221

布局，206–207

使用 AJAX 加载内容，226–234

导航项，206

主导航，206

`resize` 方法，214–216

次导航，206

精灵图交互，221–224

异步 JavaScript 和 XML（AJAX），92。*另请参阅* JavaScript

处理内容量，231–234

包含 jQuery UI 小部件，226–229

加载多个项目，230–231

属性选择器，与上传一起使用，70

自动完成小部件

`div` 标签，167

功能，149，167

表单输入框，167

脚本文件，168

`selectedAttraction` 变量，169

### B

巴赫，克里斯蒂安，172

返回按钮

处理，241

和查询（BBQ）库，241

背景颜色，移除，22

背景图像

渐变填充，194

调整大小，194–196

条形图

创建，183–188

显示，186–187

BBEdit，xii

BBQ（返回按钮和查询）库，241

蓝光光盘示例

`::contains` 选择器，112

加载脚本，112–116

模态窗口，112–113

`blur` 方法

绑定到电子邮件输入，62

与用户名一起使用，100

花括号（`}`），用于关闭代码，4

浏览器，xiii

### C

缓存选择器，10

日历，添加到表单，155–157

回调，与模态窗口一起使用，33

`cameras.jpg` 图像，使用，85

轮播。*另请参阅* 图像轮播

`carousel` 文件，创建，37

层叠样式表（CSS）

应用于应用程序界面，209–214

边框规则，213

`:focus` 伪选择器，211

页脚部分，212

用于图像轮播，35–37

重要属性，209

内部容器，212

导航区域，212–213

外部容器，210–211

用于进度条小部件，163

用于精灵图，52–54

使用 CSS 样式化网页，18

切科，拉夫，191

链式方法，展开，8。*另请参阅* 方法

链式调用，解释，3

尚皮翁，史蒂夫，19

图表数据，183–188

Chrome 浏览器，xiii

`click` 事件，与模态窗口一起使用，27–28

`click` 方法

精灵图交互，222

在 DVD 目录中使用，115

客户端验证，执行，68–71

Closure Compiler

下载，11

打包和解包代码，11–14

Cloud Zoom 插件

居中照片，192

下载，191

选项，193

照片容器，192

缩放效果，193

代码。*另请参阅* jQuery 代码

关闭，4

打包，11–15

共享，16

`colorText` 插件，声明，200–202

注释和换行，8

`::contains` 选择器，使用，112

内容，处理量，231–234

上下文菜单

禁用，235–240

`id notesContext`，238

笔记界面，239

`notes_add.php` 文件，238

`notes.php` 文件，237

插件，236

无序 HTML 列表，239

上下文帮助

`class` 属性，246

CSS（层叠样式表），242–243

`delegate` 方法，243

`div`，244

`fadeIn` 方法，244

`fadeOut` 方法，245

`helpDisplay` 函数，244–245

`mouseout` 事件，243

`mouseout` 方法，245

`mouseover` 事件，243

提供，241–246

`setTimeout` 方法，244–245

`title` 信息，244–246

使用，245–246

Cookie

赋值，109

“记住我”值，140

为用户登录设置，98–100

`time()` 函数，99

与 MD5 哈希一起使用，139–140

用于识别用户，139–141

封面艺术，为 DVD 创建，120

CSS（层叠样式表）

应用于应用程序界面，209–214

边框规则，213

`:focus` 伪选择器，211

页脚部分，212

用于图像轮播，35–37

和 HTML，19–22

重要属性，209

内部容器，212

导航区域，212–213

外部容器，210–211

用于进度条小部件，163

用于精灵图，52–54

使用 CSS 样式化网页，18

CSS 状态，从...移动元素，30

自定义上下文菜单小部件，240

### D

仪表板，创建，188

数据

清理，142

安全传输，144

`Datepicker` 函数，使用，156–157

日期，添加到表单，155–157

使用 Firebug 调试，xiii，10

`delegate` 方法

使用，32

与上下文帮助一起使用，243

设计，规划，23

对话框，设置宽度，161

对话框小部件

`autoOpen` 选项，160

按钮，161

`close` 方法，162

`dialog` 函数，160，162

功能，149，158–162

模态选项，161

否按钮，162

`preventDefault` 方法，160

`reserverequest` 表，159

`resizable` 选项，161

`sleep` 函数，159

“请稍候”标签，162

提交按钮，160

是按钮，161

`div` 标签，创建，4

美元符号（`$`），与插件一起使用，200

DOM（文档对象模型）

API（应用程序编程接口），7

检查，5–6

检查器应用程序，6

树状结构，6–7

DOM 树，遍历，7–10

双斜杠（`//`），与注释一起使用，8

DVD 目录

绑定`click`方法，115

`load` 方法，114

主页面，113–115

Summary 元素，115

DVD 收藏目录，封面图，120

DVD 示例。*另请参阅* `postdvd.php` 文件

`::contains` 选择器，112

加载脚本，112–116

模态窗口，112–113

`dvdcount.js` 脚本

加载，115

设置，112

`dvdcover.php` 文件，创建，120

### E

`each` 方法，与表单一起使用，61

缓动方法

线性，38

摇摆，38

Easing 插件，下载，38

Easy Background Resize 插件

添加到旅馆网站，194–196

下载，194–196

特性，194

图片路径，195

电子前哨基金会网站，144

元素，选择，9

AJAX 验证中的`else`语句，96–97

电子邮件地址

绑定`blur`方法，62

隐藏的错误 span，62

`inputEmail` 变量，64

`.next()` 方法，66

带有错误的`span`元素，66

测试方法，64–65

在表单中验证，62–66

电子邮件验证

执行，141–142

更新，137–138

AJAX 验证的错误消息，101–102

错误，捕获上传错误，69–71

事件处理程序，绑定，3

事件。*另请参阅* submit 事件

绑定到元素，32，34

用于表单方法，60

为 AJAX 调用触发，118–125

`exif_imagetype` 函数，使用，73

可扩展标记语言（XML），与 JavaScript 对象表示法（JSON）对比，126

### F

`fadeIn()` 方法，与模态窗口一起使用，30

字段，自动完成，167–170

文件扩展名

正则表达式，120–121

上传测试，70

文件上传。*参见* 上传

Firebug

下载，xiii，10

检查操作，11

特性，10

处理程序功能，10

使用其进行故障排除，10

Firefox 浏览器，xiii

`fn` 对象，与插件一起使用，200

`focus` 函数

`tabindex` 属性，60

与表单一起使用，60–62

`:focus` 伪选择器，与 CSS 一起使用，211

表单数据，序列化，103，125

表单元素，清除，124

表单字段，避免空白，66–68

表单输入

用于添加电影，120

客户端验证，68

完成，66–68

光标位置，61–62

`each` 方法，61

`focus` 函数，60–62

查找，61

正则表达式，63–65

表单方法，事件，60

表单提交

电子邮件验证，137–138

`errorCount` 函数，135–136

`errors` 参数变量，136

递增`submitErrors`，138

密码验证，136–137

阻止，135–138

`$submitErrors` 变量，135

表单

添加日历，155–157

添加日期，155–157

`users_add.php`，232

`users_search.php`，230

验证电子邮件地址，62–66

论坛，参与，9

函数。*参见* 方法

### G

`get` 方法

关闭，109

使用，108–110

`getJSON` 请求方法，与推文一起使用，131

`getScript` 方法，使用，112–116

Given, J.P.，194

gMap 插件

居中地图，182

下载，180

特性，171，180

加载页面，182

地图类型，181

绘制点，182

属性，180

设置选项，181

样式规则，180

缩放级别，181

Google Maps API，流行度，180

优雅降级，19

GSGD 网站，38

Gustafson, Aaron，19

### H

“Hello World”示例

锚点标签，4

绑定事件处理程序，3

链式调用，3

完成，5

文档就绪函数，3

头部区域，4

HTML `div`，4

HTML 标记，2

jQuery 源文件，2

脚本标签，2

选择器，3

span 元素，4

`hello_world.html` 文件，保存，5

`hover` 函数

图片轮播，39–41

精灵交互，222

HTML（超文本标记语言）

为应用程序界面创建，207–209

与 CSS，19–22

无序列表，239

HTML `div`，创建，4

HTML 文件，在其中引用 jQuery UI 文件，150–152

HTML 表单，为`notes_add.php`创建，238

HTML 列表，无序，27

HTML 标记，为基于精灵的导航定义，51

HTMLDOM 元素，选择，18

`htmlspecialchars()` 函数，使用，142–143

HTTPS 安全协议，考虑，144

### I

`iframe` 方法

从 DOM 中移除，125

使用其上传图片，124

与上传一起使用，75

图片轮播

`animate` 方法，40

`autoCarousel` 函数，37，39

自动滚动，37–39

缩略图的`bodyHeight`变量，48

构建，34

`carThumb` 类，45

居中模态窗口，49

控制手动滚动，41–44

CSS（层叠样式表），35–37

缓动动画，38

放大缩略图，44–50

特性，35

`function` 关键字，37

列表项高度，36

hover functions（悬停功能），39–41

invisible portions（不可见部分），37

left margin for CSS（CSS 左外边距），36

list items（列表项），37

modal window for thumbnail（缩略图的模态窗口），48

mouse cursor（鼠标光标），40

moving（移动），38

moving list items（移动列表项），38

moving to right（向右移动），42–44

naming items（命名项），48

`photoModal` style rule（`photoModal` 样式规则），45

`photoPathArr` array（`photoPathArr` 数组），46

resetting left margin（重置左外边距），39

restarting automatic scrolling（重新启动自动滚动），41

`scrollRight` element（`scrollRight` 元素），42

`setInterval` function（`setInterval` 函数），39

splitting thumbnail path info（拆分缩略图路径信息），46

`stop` method（`stop` 方法），40

stopping scrolling animation（停止滚动动画），41

visible portions（可见部分），37

width of list items（列表项宽度），36

zooming in on larger images（放大查看大图），44–50

`! important` CSS property（`! important` CSS 属性），209

images, uploading with `iframe` method（使用`iframe`方法上传图片），124

`inc/movieUp.js` file（`inc/movieUp.js` 文件）。*另请参阅* movies

`ajaxStart` method（`ajaxStart` 方法），123

beginning form handler（开始表单处理程序），124



绑定`ajaxStop`方法，123

清除表单元素，124

表单处理程序，124

模态弹出窗口，123

`post`方法，125

移除模态指示器，124

序列化表单数据，125

启动，123

上传数据，125

上传图片，124

交互规划，23

`interface.css`文件

上下文帮助，242–243

创建，209

`interface.js`文件

上下文帮助，243

创建，214

打开，228，235

Internet Explorer 浏览器，xiii

### J

JavaScript。*另请参阅* AJAX（异步 JavaScript 和 XML）

对象字面量表示法，126

`test`方法，72

非侵入式，22

JavaScript Object Notation (JSON)（JavaScript 对象表示法）

数组，126

`name:value`对，126–127

人员对象，127

要求，126

在函数中返回，128

与 XML 对比，126

设置 JavaScript 对象，126

jqPlot 插件

`$requestArray`，183–184

`barMargin`选项，187

CSS 样式表，186

仪表盘，188

下载，183

特性，171

`$.jqplot.BarRenderer`附加组件，187

JSON 数组字符串，185

外边距，187

`mysql_result`，185

渲染器，187

`requestArray`，184

`requestChart`选择器，183

`ticks`选项，187–188

图表 x 轴，188

jQuery 代码。*另请参阅* code

关闭，4

与其他代码结合，18

jsFiddle 工具，16

测试代码片段，17

jQuery 上下文菜单插件，Images 文件夹，236

jQuery 自定义上下文菜单小部件，240

参与 jQuery 论坛，9

jQuery 库

下载，xii

在渐进增强中包含，21

jQuery 插件

后退按钮与查询 (BBQ) 库，241

Cloud Zoom，191–193

`colorText`，200–202

上下文菜单，236

创建，200–202

Easy Background Resize，194–196

`fn`对象，200

gMap，171，180–182

jqPlot，171，183–188

返回`this`对象，201

Sexy Curls，197–199

结构化，202

Tablesorter，171–178

TinyTips，171，178–181

工具提示，178–181

使用 $（美元符号），200

与小部件对比，148

zWeatherFeedjQuery，189–191

jQuery UI

自定义，148–150

下载，xii

在 HTML 中引用文件，150–152

网站，148

jQuery UI 小部件

Accordion（手风琴），149，226–229

Autocomplete（自动完成），149

表单日历，155–157

Custom Context Menu（自定义上下文菜单），240

`Datepicker`函数，156–157

访客“对话框”，158–162

Dialog（对话框），149

设计，152

字段自动完成，167–170

日期的`onSelect`选项，156

与插件对比，148

Progressbar（进度条），163–167

选项卡界面，152–155

Tabs（选项卡），149

ThemeRoller，148

创建`jquery.colorText.js`文件，200

下载 jsFiddle 工具，16

JSON (JavaScript Object Notation)（JSON（JavaScript 对象表示法））

数组，126

`name:value`对，126–127

人员对象，127

要求，126

在函数中返回，128

与 XML 对比，126

JSON 示例

`DOCTYPE`设置，129

Twitter 小部件的样式信息，129–130

设置 JSON 请求，127–133

JSONP 格式

跨域请求，128

与推文数据一起使用，127

### K

Kastner, Cedric（Cedric Kastner），180

Kember, Elliott（Elliott Kember），198

### L

Leonello, Chris（Chris Leonello），183

在渐进增强中包含库，21

换行与注释，8

使用`live`方法，32

`load`方法

调用，111

语法，110

使用，110–111

与 DVD 目录一起使用，114

与多个项目一起使用，230–231

lodge 网站

Easy Background Resize 插件，194–196

页面卷曲效果，197–199

排序表格记录，189–190

zWeatherFeed 插件，189–191

为登录创建 PHP，97–100

创建登录函数，105–107

### M

`mainNav.jpg`精灵图

类别，50

尺寸，51

使用 MD5 哈希与 cookie，139–140

Merritt, Mike（Mike Merritt），178

将方法应用于对象，3。*另请参阅* chained methods

模态窗口

用于 AJAX 验证，104

动画，30

回调，33

调用，27–30

居中，31

缩略图居中，49

`click`事件，27–28，32–33

关闭，28，32–33

创建，27–30，123

确定关闭时机，33

`fadeIn()`方法，30

`fadeOut`函数，33

外边距，28–29

打开，31

内边距，28–29

弹出窗口，123

`rel`属性，28

阴影背景，31–32

与脚本一起使用，112–113

电影。*另请参阅* `inc/movieUp.js`文件

表单，120

包含在光盘中，112

使用 mySQL，18

连接到 mySQL 数据库，80

`mysql_query`函数

运行，122

用于验证，96

使用`mysql_real_escape_string()`函数，142–144

将`mysql_result`与 jqPlot 插件一起使用，185

`mysqlErrorNum`变量，103–104

### N

`name:value`对

为推文创建，131

解析，108

与 get 方法一起使用，109

命名约定，48

导航

使其优雅，27–33

模态窗口，27–30

基于精灵的，50–56

`newName`变量，与`post`方法一起使用，101

`.next()`方法，与表单一起使用，66

`notes_add.php`文件

创建，238

HTML 表单，238

`notes.php`文件，为上下文菜单创建，237

记事本，xii

Notepad++，xii

### O

对象字面量表示法，解释，126

对象，应用方法到，3

Opera 浏览器，xiii

### P

页面重定向，避免，92

页面重新加载，避免，92

页面。*参见* 网页

圆括号 ()))，用于关闭代码，4

密码

检查 AJAX 验证，94

检查用户登录，97–98

提示输入，246

密码字段，避免空白，67–68

密码验证，更新，136–137

`pephoto.sql`文件，运行，109

`pePhotoUp.js`文件，保存，70

`peRegister.php`文件，打开，141

照片表，创建，109–110

摄影师交流网站。*另请参阅* 网站

账户页面，107

客户端验证，69–71

用于识别用户的 Cookie，139–141

电子邮件验证，137–138

`errorCount`函数，135–136

`errors`参数变量，136

文件类型，73

文件上传表单，69

表单输入，61

表单，60

首页，26

递增`submitErrors`，138

密码字段，67–68

密码验证，136–137

阻止表单提交，135–138

检索图片，108–110

保存图像数据，82–83

服务器端验证，72–73

精灵，50

`$submitErrors`变量，135

上传函数，75–76

照片

检索，108–110

放大，191–193

`photoUpload.php`文件，定位，72

`photoUservariable`变量的内容，109–110

PHP

`createThumbnail()`函数，85

`explode`方法，85

`imagecopyresampledto`函数，87

`ImageCreateTrueColor`函数，87

`mysql_query`函数，96

照片上传脚本，80

`preg_match`函数，72

资源，100

用于验证的`switch`方法，93–94

测试能力，72–73

上传故障排除信息，83

用于用户登录，97–100

使用，18

在服务器端验证中使用，72

PHP 函数

用于数据清理，142–144

`htmlspecialchars()`，142–143

`mysql_real_escape_string()`，142–144

PHP 注册，为验证构建，92–100

图片

检索，108–110

放大，191–193

规划设计，23

绘制数据，183–188

插件

后退按钮和查询 (BBQ) 库，241

Cloud Zoom，191–193

`colorText`，200–202

上下文菜单，236

创建，200–202

Easy Background Resize，194–196

`fn`对象，200

gMap，171，180–182

jqPlot，171，183–188

返回`this`对象，201

Sexy Curls，197–199

结构化，202

Tablesorter，171–178

TinyTips，171，178–181

工具提示，178–181

与 $（美元符号）一起使用，200

与小部件对比，148

zWeatherFeedjQuery，189–191

`post`方法

回调，101

关闭，102

`GET`方法，108

调用，103

与`ajaxSetup`一起使用，116–118

与`inc/movieUp.js`文件一起使用，125

验证，100–102

`postdvd.php`文件。*另请参阅* DVD 示例

创建，121

数据库连接，121

数据库更新，122

运行 SQL 查询，122

睡眠计时器，122

`preventDefault`设置，与提交事件一起使用，102–103

进度条小部件

调用，165

CSS（层叠样式表），163

CSS 规则，164

显示，165–166

淡入，165

特性，163

隐藏，164

移除，166

设置外边距，164

阴影，163–164

用于关闭代码，163

z-index，164

渐进增强

应用原则，27

示例，19–22

解释，19

HTML 和 CSS，20

包含 jQuery 库，21

### Q

查询字符串，识别，108

### R

注册函数

`preventDefault`设置，102–103

序列化表单数据，103

设置提交事件，102–103

启动，102

注册窗口，淡出，105

正则表达式

用于文件扩展名，70，120–121

与表单一起使用，63–65

与缩略图一起使用，85

与推文一起使用，131–132

`return false;`

锚点标签，15

遇到，15

`preventDefault();`调用，15–16

`stopPropagation()`，15

右键上下文菜单，禁用，235–240

### S

Safari 浏览器，xiii

`script`标签，用于关闭代码，4

脚本。*另请参阅* 服务器端脚本



`::contains` 选择器，112

动态加载，112–116

模态窗口，112–113

用于推文，130–133

安全套接层（SSL），144

安全证书，考虑，144

安全协议，HTTPS，144

选择器

将事件处理程序绑定到，3

缓存，10

`::contains`，112

创建，3

读取，9

`requestChart`，183

序列化表单数据，103

服务器，从中检索信息，110–111

服务器端脚本，保护，141–142。*另请参阅* 脚本

服务器端验证

为表单开发，72–73

`exif_imagetype` 函数，73

Sexy Curls 插件，使用，198–199

站点。*请参阅* 网站

斜杠星号（`/*`），与注释一起使用，8

`sleep` 函数，与 Dialog 小部件一起使用，159

睡眠定时器，为`postdvd.php`创建，122

Smith, George，38

`span` 元素，4

精灵交互

`addClass` 方法，223

`click` 函数，222–223

创建，221–224

`hover` 函数，222

`hover` 事件中的`mouseout`部分，222–223

`span` 元素，222

`span selected` 元素，222

基于精灵的导航

动画，55–56

背景图像，52–53

`background` 位置，53

列位置，53

列宽，53

创建，50–56

CSS 布局，50

定义标记，51

悬停效果，56

项目布局，54

`mainNav.jpg` 精灵，50–51

`span background-position`，53

`span` 元素，55–56

`spriteNav` 规则，52

精灵，52–54

`width` 位置，53

x 轴和 y 轴，53

创建`spritenav.css`文件，218

`spritenav.js` 文件

创建，221

打包，11–14

解包，14

精灵

添加到应用程序界面，223

锚点标签，218

`background-position`，219–220

`base width`，219

CSS（层叠样式表），218–221

图像，221

`span` 元素，219–220

用途，54

SSL（安全套接层），144

“Stay with us” 标签，导航到，162

故事板，使用，23

样式，使用 ThemeRoller 小部件应用，149

提交事件，设置，102–103。*另请参阅* 事件

`submit` 方法，将`addMovie`表单绑定到，124

`submitErrors`，递增，138

`$submitErrors` 变量，初始化，135

SXSW Interactive 会议，19

### T

选项卡式界面

创建，152–155

`div` 标签，152–153

无序列表，153

`tabindex` 属性，与`focus`函数一起使用，60

表记录，排序，172–177

Tablesorter 插件

到达日期，177

列，176

条件检查，174

特性，171

HTML 标记，174

HTML 部分，173

HTML 表格输出，175

请求`id`，174

`sorter` 属性，174

排序记录，176–177

`tbody` 部分，175

测试数据，174

`thead` 部分，175

未排序数据，177

使用，172–177

Tabs 小部件，特性，149–155

文本编辑器，xii

ThemeRoller 小部件

使用它选择样式，149

下载，148

`this` 对象，为插件返回，201

缩略图

`createThumbnail()` 函数，85

为上传创建，83–88

高度和宽度，86

命名，48

`time()` 函数，与 cookie 一起使用，99

超时，为上传设置，77–79

TinyTips 插件

在选项卡上创建，179

下载，178

特性，171

设置，179

源代码参考，178–179

工具提示。*请参阅* TinyTips 插件

推文数据，以 JSONP 格式返回，127

推文

包含在`name:value`对中，131

`getJSON` 请求方法，131

哈希标签，132

正则表达式，131–132

脚本，130–133

搜索`@`前缀，132

`tweetText`，在其中插入锚点标签，132

Twitter，创建 URL 访问，130–131

Twitter API，流行度，127

Twitter 小部件

主体部分，130

功能，133

样式信息，129–130

### U

Ullman, Larry，100

非侵入式 JavaScript，22

无序 HTML 列表

创建，239

示例，27

上传的文件

开始循环，80

连接到 mySQL 数据库，80

`createThumbnail` 函数，81

处理，80–81

验证代码，81

上传

属性选择器，70

回调式功能，77–79

清除输入字段，79

客户端 jQuery，76

客户端验证，69–71

创建缩略图，83–88

文件类型的错误 span，69–71

淡入确认消息，78

淡出确认消息，79

文件类型，69–70

`iframe`，75–76

`inputLength` 变量，77–78

插入图像信息，82–83

模态窗口，78

执行，74–75

PHP 代码，75

PHP 故障排除信息，83

移除确认模态框，79

保存图像数据，82–83

脚本编写，76–77

服务器端验证，72–73

`setTimeout` 函数，77–79

SQL 查询，82

缩略图，83–88

用户登录，创建 PHP 代码，97–100

用户名，使用中，102–103

用户

通过 Cookie 识别，139–141

使用进度条通知，163–167

加载`users_add.php`表单，232

创建`users_search.php`表单，230

创建`users.php`页面，227

用户提供的数据，清理，141–144

### V

验证。*参见* AJAX 验证；客户端验证；电子邮件验证；密码验证；服务器端验证

访客，建立“对话框”，158–162

### W

等待指示器，调用，125

天气，预测，189–191

Web 应用程序界面。*参见* 应用程序界面

Web 页面

卷曲效果，198–199

特性，5

加载部分内容，111

使用 CSS 设置样式，18

Web 站点。*另请参阅* 摄影师交流网站

动画图形，125

Cloud Zoom 插件，191

Easing 插件，38

Easy Background Resize 插件，194–196

电子前哨基金会，144

Firebug 下载，xiii, 10

gMap 插件，180

Google Closure Compiler，11

GSGD，38

jqPlot 插件，183

jQuery UI，148

jsFiddle 工具，16

正则表达式，63

Tablesorter 插件，172

ThemeRoller，148

TinyTips 插件，178

zWeatherFeedjQuery 插件，189

小部件

手风琴，149, 226–229

自动完成，149

表单日历，155–157

自定义上下文菜单，240

`Datepicker` 函数，156–157

访客“对话框”，158–162

对话框，149

设计，152

字段自动完成，167–170

日期的`onSelect`选项，156

与插件对比，148

进度条，163–167

选项卡界面，152–155

选项卡，149

ThemeRoller，148

### X

XAMPP，xiii

XML（可扩展标记语言），与 JavaScript 对象表示法（JSON）对比，126

### Z

zWeatherFeedjQuery 插件

添加到旅馆网站，189–190

下载，189

RSS 位置代码，190–191
