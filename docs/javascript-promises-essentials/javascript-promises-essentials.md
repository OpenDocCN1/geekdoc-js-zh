# Javascript Promises 入门指南
















# 序言

《JavaScript Promises Essentials》是一本关于 promises 新概念的实用指南。它提供了一个单一资源，取代了目前关于该主题的所有零散信息。它详细介绍了这一将增强我们在 JavaScript 中进行异步编程方式的新标准。本书对 Promises API 及其特性以及如何在 JavaScript 编程中使用它进行了简明的解释。它涵盖了 JavaScript promises 的核心内容，触及了你在新学习过程中最重要的细节，并针对该主题的不同方面提供了一些非常有用的提示。

Promises 在很大程度上是一个编程概念，它提供了一种流程，允许开发者安排对尚不存在的数据和值进行执行的工作，并允许他们在未来的某个不确定点（异步地）处理这些值。它还提供了一种处理与异步 API 通信的抽象。目前，JavaScript 中可以通过回调、定时器和事件来实现异步调用，但它们都有局限性。Promises 解决了实际开发中的头疼问题，与传统方法相比，允许开发者以更原生的方式处理 JavaScript 的异步操作。此外，promises 在同步功能和异步函数之间提供了直接的对应关系，特别是在错误处理方面。已经有一些库开始使用 promises 并现在提供了健壮的 promises 实现。你可以在 Web 的许多库中找到 promises，也可以通过与 Node.js 和 WinRT 交互找到。学习 promise 实现的细节将帮助你避免异步 JavaScript 世界中出现的许多问题，并构建出更好的 JavaScript API。

# 本书涵盖的内容

第 1 章“JavaScript Promises – 我为什么需要关注它？”，介绍了 JavaScript 异步编程的世界以及 promises 在该世界中的重要性。

第 2 章“Promise API 及其兼容性”将带你了解 Promises API 的更多细节。我们还将学习当前浏览器对 promises 标准的支持情况，并查看市场上实现 promises 和类 promise 特性的 JavaScript 库。

第 3 章“Promises 链式”向你展示 promises 如何允许异步操作的链式调用以及这实现了什么。本章还涵盖了如何队列异步操作。

第 4 章“错误处理”涵盖了 JavaScript 中的异常和错误处理。本章还将解释 promises 如何让错误处理变得更简单更好。

第 5 章“WinJS 中的 Promises”探索了 WinJS.Promise 对象的所有内容以及它如何在 Windows 应用开发中使用。

第 6 章“整合所有内容 – Promises 实战”向你展示 promises 的实战，以及在整合目前所学内容的场景中如何以及在何时使用 promises。

# 本书需要的工具

为了实现你将在书中学习的内容，你只需要一个 HTML 和 JavaScript 编辑器。你可以从以下选项中选择：

- Microsoft Visual Studio Express 2013 for Web：它提供了功能全标记和代码编辑器。
- WebMatrix：这是运行示例代码的另一种选择。这是一个免费、轻量、云连接的网络开发工具，利用了最新的标准和流行的 JavaScript 库。
- jsF：这是一个在线 Web 编辑器，允许你编写 HTML 和 JavaScript 代码并直接在浏览器中运行。

# 本书的读者

本书适用于所有参与 JavaScript 编程的开发者，无论是在 Web 开发中，还是在使用大量异步 API 的 Node.js 和 WinRT 技术。此外，它也适用于对 JavaScript 异步编程以及能提升体验的新标准感兴趣的开发者。简而言之，本书适合所有人。

# 约定

在书中，你将发现许多区分不同类型信息的样式。以下是这些样式的示例及其含义。

文本中的代码、数据库名、文件名、扩展名、路径名、虚拟 URL、用户输入显示如下：“我们可以通过 `addEventListener()` 实现。”

代码块显示为：

```javascript
var testDiv = document.getElementById("testDiv");
testDiv.addEventListener("click", function() {
  // 所以 testDiv 被点击了，现在
  alert("I'm here!");
});
```

**新词和重要单词加粗显示。**屏幕上、菜单或对话框中的词汇显示为：“请命名应用程序，并点击确定。”


![](img/04c7981ae2601bc5401805f632a22d49_6_1.png)

# 读者反馈

我们欢迎读者的反馈。让我们对这本书的看法——你喜欢或可能不喜欢的地方。读者反馈对于我们开发真正受益的书至关重要。

发送通用反馈，只需发送邮件到 feedback@packpub.com，并在邮件主题中注明书名。

如果你在某个领域拥有专长并兴趣编写或贡献书籍，请参阅我们 www.packpub.com 上的作者指南。

# 客户支持

现在你是 Packt 书籍的主人，我们有很多方法帮助你从购买中获得最大收益。

# 勘误

尽管我们努力确保内容的准确性，但错误仍然会发生。如果你在我们的书籍中发现错误——可能是文本或代码中的错误——我们将非常感谢你告诉我们。这样做可以避免其他读者感到沮扰，并帮助我们改进书中后续的版本。如果你发现任何勘误，请访问 http://www.packpub.com/submit-errata 进行报告，选择你的书籍，点击勘误提交表链接并输入勘误详情。一旦你的勘误通过验证，提交将被接受，勘误将上传到我们的网站，或添加到该标题下 Errata 部分的现有勘误列表中。你可以通过 http://www.packpub.com/support 查看任何现有勘误。





### JavaScript Promises – 我为什么需要关注它？

JavaScript 的流行程度从未像现在这样。这种曾经（也许对某些人来说现在依然如此）由于其名称而最受误解的编程语言，现在已处于最流行编程语言的前列。此外，世界上几乎每台个人电脑都至少在使用或安装了一个 JavaScript 解释器。JavaScript 流行程度的不断增加完全归功于它作为 Web 脚本语言的角色。它在这一领域的成功——JavaScript 设计用于在 Netscape Navigator 中运行——使其成为几乎所有浏览器的标准配置，但 JavaScript 已经成长并成熟，现在已扩展到许多与 Web 无关的领域。在第一章中，我们将简要介绍以下内容：

- JavaScript 中的异步编程
- 开发者在处理异步操作的传统方法中面临的问题
- JavaScript Promises 简介
- 为什么在与常见的异步处理方式进行比较时，我们应该关注 Promise

## JavaScript 中的异步编程

谈到 JavaScript 中的异步编程时，有两点需要讨论：Web 和编程语言。浏览器代表的 Web 环境与桌面环境不同，这反映在我们在为每个环境编写程序和代码的方式上。与桌面环境相反，浏览器为所有需要访问用户界面的操作（在 HTML 术语中是 DOM）提供单线程。这种单线程模型对可能访问和修改 UI 元素的应用代码产生了负面影响，因为它将代码的执行限制在同一个线程中。因此，我们会有阻塞函数和线程，它们基本上会阻塞 UI 直到该线程执行完毕。这就是为什么在 Web 开发中，充分利用器的任何异步能力是至关重要的。

让我们回顾一下历史以获取更多背景。过去，网站由 HTML 页面组成，每个用户都需要从服务器加载整个网页。这给开发者带来了很多问题，特别是当编写编写会影响页面的服务器端代码时。此外，它还导致了糟糕的用户体验。对用户操作或 HTML 表单更改的响应是通过向表单所在的页面发送 HTTP POST 请求完成的；这导致服务器使用刚刚收到的信息刷新页面。这整个过程和模型都是低效的，因为在缓慢的互联网环境下，这会导致页面的所有内容丢失。浏览器随后重新加载网页并重新发送所有内容，即使只有部分信息发生了变化；这消耗了过多的带宽并给服务器增加了额外负载。后来，在行业内不同方的大量努力下，异步 Web 技术开始出现，以帮助解决这一局限性。该领域的一个著名成员是异步 JavaScript 和 XML (AJAX)，这是一组在客户端用于创建异步方式通信的 Web 应用的技术。AJAX 技术允许 Web 应用以异步方式从服务器发送数据和检索数据，而不会干扰当前页面的 UI 和行为；基本上不需要重新加载整个页面。实现这一点的核心 API 是 `XMLHttpRequest` API。

随着 Web 技术和浏览器的进步，JavaScript 作为 Web 脚本语言变得更加突出，它允许开发者访问 DOM 并动态地显示以及与网页上呈现的内容进行交互。然而，JavaScript 本质上也是单线程的，这意味着在任何给定时刻，两行脚本不能同时运行；相反，JavaScript 语句是按行执行的。同样，在浏览器中，JavaScript 与浏览器执行的一系列其他工作负载共享一个线程，从绘制和更新样式到处理用户操作。其中一个活动将决定执行顺序。

当 JavaScript 起初开始时，它旨在编写简短、快速运行的代码。主要的应用程序逻辑和计算都在服务器端完成。自从 Web 加载内容的方式从重新加载整个页面变为客户端加载后，异步开发者极度依赖 JavaScript 进行 Web 开发。现在，我们可以看到用 JavaScript 编写完整的应用程序逻辑，并且许多库蓬勃发展以帮助开发者完成工作。

在 Web 开发中，我们有三个主要组件：

- HTML 和 CSS
- 文对象模型 (DOM)
- JavaScript

还有一个在 AJAX 中起关键作用的组件：

- XMLHttpRequest API

简而言之，HTML 和 CSS 用于网页的呈现和布局。DOM 用于动态显示和交互。XHR 用于向服务器发送 HTTP/HTTPS 请求并将数据传回脚本。最后，JavaScript 允许将这些技术结合在一起，以创建美观、响应式的 Web 应用。

为了解决多线程的局限性，开发者严重依赖事件和回调，因为这是应用程序暴露异步编程的方式。在基于事件的 API 中，处理程序被注册到指定的对象，并在事件触发时调用。浏览器通常会在不同的线程中执行操作，并在适当的情况下在主线程中调用。

## JavaScript Promises – 我为什么关注它？

可以使用 `addEventListener()` 方法来实现这种基于事件的技术。该方法简单地在其调的对象上注册一个监听器。事件目标对象可以是 HTML 中的一个元素、文档本身或任何其他支持事件的对象（如 XHR）。下面的代码展示了使用 HTML 和 JavaScript 的简单事件监听器。

HTML 部分如下：

```
<div id='testDiv' style="width:100px; height:100px; background-color:red"></div>
```

JavaScript 部分如下：

```javascript
var testDiv = document.getElementById("testDiv");
testDiv.addEventListener("click", function() {
  // 所以 testDiv 对象被点击了，现在我们可以做一些事情
  alert("我在这里！");
});
```

在 HTML 部分，我们在 DOM 中定义了一个带有 `testDiv` ID 的 div 元素。在 JavaScript 部分，我们在第一行代码中获取该 div 元素并赋值给变量。然后，我们在它上添加事件监听器，并将其传递给点击事件，随后跟一个匿名函数（没有名字函数）作为监听函数。该函数将在稍后元素被点击时被调用。

> 如果你在 HTML 标记包含 div 元素之前添加这段 JavaScript 代码，它将报错。因为在代码执行时元素尚未创建，代码将找不到可以调用 `addEventListener` 的目标对象。





# 第一章

如果你是 JavaScript 的初学者，看到函数被作为参数传递可能会觉得有些陌生，但别担心；当你把它们看作对象时，一切都会变得简单。

某些浏览器 API（如 HTML5 Geolocation）是根据设计被调用的。我将在示例中使用自定义的 `getCurrentMethod` 来使用回调函数。代码看起来如下：

```
navigator.geolocation.getCurrentPosition(function(position) {
 alert('I am here, Latitude: ' + position.coords.latitude + ' ' +
  '/ Longitude: ' + position.coords.longitude);
});
```

在上一个示例中，我们简单地调用了 `getCurrentPosition` 方法并传递了一个匿名函数，该函数反过来调用了 `alert` 方法，该方法将带有我们请求的结果被回调。这允许浏览器同步或异步地执行此代码；因此，在获取位置时代码不会阻塞浏览器。

在这种情况下，我们使用了内置的浏览器 API，但我们也可以通过异步的方式暴露其基本 API 来让我们的应用程序支持异步。这些 API 涉及到 I/O 操作或密集型计算，这些可能花费大量时间。

例如，在回调场景中，获取某些数据的最简单代码如下：

```
getData(function(myData) {
 alert('Houston, we have : ' + myData);
});
```

在之前的 JavaScript 代码中，我们仅仅是定义了一个 `getData` 函数，它接受一个回调函数作为参数，该函数反过来执行一个 `alert` 来显示我们应该获取的数据。这实际上强制应用程序 UI 代码必须做好异步准备；因此，在代码获取数据时，UI 不会被阻塞。

让我们将其与非回调场景进行比较；代码看起来如下：

```
// 错误：这将在获取数据时导致 UI 冻结
var myData = getData();
alert("Houston, we have : " + myData);
```

## JavaScript Promise (Promises) – 我为什么需要关注它？

在之前的示例中，JavaScript 代码将逐行运行，即使第一行代码没有完成，下一行代码也会运行。这种 API 设计会导致代码 UI 阻塞，因为它会冻结 UI 直到获取数据为止。此外，如果 `getData()` 函数的执行恰好需要一些时间（例如，从互联网获取数据），整体体验对用户来说将非常糟糕，因为 UI 必须等待其执行完成。

此外，在之前的回调函数示例中，我们将匿名函数作为包含函数的参数传递。这是使用回调函数的常见模式。另一种使用回调函数的方法是声明一个命名函数并将函数名作为参数传递。在下面的示例中，我们将使用命名函数。我们将创建一个接受字符串参数并在 `alert` 中显示它的通用函数。我们将其命名为 `popup`。然后，我们将创建另一个函数并调用 `getContent()`；它接受两个参数：一个字符串对象和一个回调函数。最后，我们将调用 `getContent` 函数，并在第一个参数传递一个字符串值，并在第二个参数传递 `popup` 回调。运行脚本，结果将是一个包含第一个字符串参数中值的 alert。以下是该代码的示例：

```
// 显示 alert 的通用函数
function popup(message) {
  alert(message);
}
// 一个接受两个参数的函数，最后一个是回调函数
function getContent(content, callback) {
  callback(content); //调用回调函数
}
getContent("JavaScript is awesome!", popup);
```

正如我们在上一个示例中看到的，我们能够向回调函数传递参数，归根结底，它在执行时就是一个普通函数。我们可以将包含函数的任何变量作为参数传递给回调函数，甚至可以传递代码其他部分的全局变量。

总结一下，JavaScript 回调函数是强大的，对 Web 开发环境做出了巨大贡献，从而允许开发者进行异步 JavaScript 编程。

## 我为什么应该关注 Promise？

Promise 与这一切之间有什么关系呢？嗯，让我们从定义 Promise 开始。

一个 Promise 代表异步操作的最终结果。

- [Promises/A+ 规范，http://promisesplus.com/

因此，一个 Promise 对象代表一个可能尚未可用的值，但它将在未来的某个点被解析（resolved）。

Promise 有状态，在任何时间点，可以是以下状态之一：

- **Pending (等待中)**：Promise 的值尚未确定，它的状态将转移到已完成（fulfilled）或已拒绝（rejected）。
- **Fulfilled (已完成)**：Promise 成功完成，现在有一个必须不能改变的值。此外，它不得从已完成状态转换到任何其他状态。
- **Rejected (已拒绝)**：Promise 从一个失败的操作返回，并且必须有一个失败原因。该原因不能改变，且 Promise 不得从该状态转换到任何其他状态。

Promise 只能从 `pending` 状态移动到 `fulfilled` 状态，或从 `pending` 状态移动到 `rejected` 状态。然而，一旦 Promise 被完成或拒绝，它就不能转换到任何其他状态，且它的值不能改变，因为它是不可变的。

> Promise 的不可变特性非常重要。它有助于避免监听器产生非预期的副作用（这可能会导致行为的意外变化），反而在可以在不影响调用者函数的情况下将 Promise 传递给其他函数。

从 API 的角度来看，Promise 被定义为一个对象，其属性的值是一个函数。Promise 对象有一个主要的 `then` 方法，返回一个新对象。它的语法如下：

```
then(onFulfilled, onRejected);
```

以下两个参数基本上是回调函数，它们将在 Promise 完成时被调用：

- **onFulfilled**：该参数在 Promise 已完成时调用
- **onRejected**：该参数在 Promise 失败时调用

### JavaScript Promises – 我为什么需要关注它？

请记住，两个参数都是可选的。此外，非函数的参数值将被忽略，因此在执行它们之前检查参数是否为函数可能是一个良好的习惯。

> 值得注意的是，当你研究 Promise 时，可能会遇到两种定义/规范：一种基于 Promises/A+，另一种是基于 CommonJS 的旧版 Promises/ A。虽然 Promises/A+ 基于这些概念并提出了 then API，但 A 的实现在多个方面与 Promises/A 有不同，我们将在第二章看到。

方法返回的新 Promise 在指定的 `onFulfilled` 或 `onRejected` 回调完成后被解析。该实现反映了一个简单的概念：当 Promise 被完成时，它有一个值；当它被拒绝时，它有一个原因。

以下是使用 Promise 的简单示例：

```
promise.then(function (value) {
  var result = JSON.parse(data).value;
}, function (reason) {
  alert(error.message);
}
});
```

回调处理程序的返回值作为返回 Promise 的解析值，这使得 Promise 操作可以链式。因此，我们将得到类似的内容：

```
$getJSON('example.json').then(JSON.parse).then(function(response) {
  alert("Hello There: ", response);
});
```





### 我不能直接用回调函数吗？

回调函数非常简单！我们传递一个函数，它会在未来的某个点被调用，然后我们就可以执行异步操作。此外，回调函数是轻量级的，因为我们不需要添加额外的库。将函数作为高阶对象已经是 JavaScript 编程语言内置的特性；因此，我们不需要额外的代码即可使用它。

然而，如果不加小心，JavaScript 中的异步编程可能会迅速变得复杂，回调函数尤其如此。当回调函数嵌套在长行代码中时，往往变得难以维护和调试。此外，在回调中使用匿名内联函数会使得阅读调用栈变得非常枯燥。而且，在调试时，从深层嵌套的回调中抛出的异常可能无法正确传播到调用链中启动回调的函数，这使得很难确定错误发生的确切位置。此外，构建基于回调的代码结构是非常困难的，因为它们会像雪球一样滚出杂乱的代码。我们最终会在更大的规模上得到类似下面代码示例的内容：

```javascript
function readJSON(filename, callback) {
  fs.readFile(filename, function (err, result) {
    if (err) return callback(err);
    try {
      result = JSON.parse(result, function (err, result) {
        fun.readAsync(result, function (err, result) {
          alert("I'm inside this loop now");
        });
        alert("I'm here now");
      });
    } catch (ex) {
      return callback(ex);
    }
    callback(null, result);
  });
}
```

上一个示例中的代码是深层嵌套代码片段，有时被称为“地狱之渊”。这种代码在增长时，会让阅读、结构化、维护和调试成为一项艰巨的任务。


### JavaScript Promises – 我为什么需要关注它？

相反，Promises 提供了一种用于管理与异步 API 交互的抽象，与使用回调和事件处理器相比，它为 JavaScript 中的异步编程提供了一种更具管理力的方法。我们可以将 Promise 看作一种异步编程的模式。

简单来说，Promise 模式将允许异步编程从广泛使用的“延续传递风格”（continuation-passing style）转变为返回值的风格，这个值被称为 Promise，它将代表该特定操作的最终结果。

它允许你将代码：

```javascript
call1(function (value1) {
  call2(value1, function(value2) {
    call3(value2, function(value3) {
      call4(value3, function(value4) {
        // 执行一些代码
      });
    });
  });
});
```

变为：

```javascript
Promise.asyncCall(promisedStep1)
.then(promisedStep2)
.then(promisedStep3)
.then(promisedStep4)
.then(function (value4) {
  // 执行一些代码
});
```

如果我们列出让 Promise 更易于使用的属性，它们如下：

- 使用更整洁的方法签名，因此更易阅读
- 它允许我们在单个 Promise 上附加多个回调函数
- 它允许将值和错误沿链传递并冒泡到调用者函数
- 它允许 Promise 的链式调用

我们可以观察到，Promise 通过返回值为同步能力带来了函数式组合，并通过向异步函数抛出异常带来了错误冒泡。这些都是我们在同步世界中认为理所当然的能力。

下面的示例（虚拟）代码展示了使用回调来组合相互通信的异步函数与使用 Promise 实现相同目的之间的区别。

以下是回调的示例：

```javascript
$("#testInput").click(function () {
  firstCallback(function (param) {
    getValues(param, function (result) {
      alert(result);
    });
  });
});
```

以下是将上述回调函数转换为返回 Promise 的函数的代码示例，这些函数可以相互链式：

```javascript
$("#testInput").clickPromise() // 返回 promise 的函数
  .then(firstCallback)
  .then(getValues)
  .then(alert);
```

正如我们所看到的，与传统的回调方法相比，Promise 允许的扁平化链式代码更更容易阅读，最终也更容易维护。

## 总结

JavaScript 中的回调函数允许我们通过异步处理事件（即用户输入）来获得响应迅速的用户界面，而不会阻塞应用程序的其他部分。Promise 是一种允许异步编程标准化的模式，使开发者能够编写出更具读性和可维护性的异步代码。

在下一章中，我们将查看支持 Promise 的浏览器及其与 jQuery 的兼容性。你还将学习支持类似 Promise 功能的库。

## 2: Promise API 及其兼容性

Promise 对于 JavaScript 世界来说还很新，但变通方法已经存在一段时间了。正如我们在上一章中看到的，处理 JavaScript 异步编程的方法，无论是通过事件还是回调。你还学习了为什么 Promise 与实现此目的传统技术有所不同。

接下来，我们将深入介绍 Promise API 的细节。你还将学习当前浏览器对 Promise 标准的支持，并查看实现 Promise 及类 Promise 功能的 JavaScript 库。在本章中，我们将涵盖以下主题：

- Promise API 及其细节
- 浏览器兼容性
- Promise 实现
- 具有类 Promise 功能的库

### Promise API 及其兼容性

### 了解 API

在本书中，我们将处理和使用根据 [Promises/A+](https://promises.com/) 定义的。Promises/A+ 组织产生 Promises/A+ 规范旨在将最初的 Promises/A 规范扩展为更清晰、更充分的版本。该提案引用自其网站：

> Promises/A+ 是基于 CommonJS Promises/A 提案中的概念和 API 的。

> - [differences from promises/a](https://promises.com/differences-from-promises-a)

这些差异存在三个层面：缺失、新增和澄清。在缺失层面，Promises/A+ 从原始规范中删除了以下功能：

- 进度处理：该功能包括一个在操作进行中（未成功也未拒绝）的回调函数。它的删除是因为实现者得出，在实践中这些功能被证明规范不足，目前 Promise 社区对其行为尚未达成共识。
- 交互式 promise：这是之前 Promises/A 提案中的扩展功能，基本上为 promise 支持两个额外函数；`get(propertyName)` 从此 promise 的目标请求属性，`call(functionName, arg1, arg2, ...)` 在 promise 的目标上调用给的方法/函数。在新的 A+ 规范中，该功能以及 call 和 get 函数被认为在实现互操作 promise 所需的基础 API 范围内。
- promise== resultPromise：这是旧提案中的一个要求，规定 promise 的结果不应等于 promise 本身，例如 `var resultPromise = promise.then(onFulfilled, onRejected);` 事实上，只要实现满足所有要求，任何实现都允许 `resultPromise === promise`。

在新增层面，Promises/A+ 规范对现有 Promises/A 提案增加了以下功能和要求：

在 `onFulfilled` 或 `onRejected` 返回 then 的行为规范，包括解析过程的细节。
- 传递给 `onRejected` 处理器的原因，它必须是该情况下抛出的异常。





# 第 2 章

- onFulfilled 和 onRejected 处理器都必须被异步调用。
- onFulfilled 和 onRejected 处理器都必须是函数。

当在同一个 promise 上连续调用 `then` 方法时，实现是根据对 onFulfilled 和 onRejected 调用的精确顺序来构建的。通俗地说，这意味着如果对同一个 promise 多次调用 `then` 方法（例如 `promise.then().then()`），那么在这些 `then` 调用中使用的所有 onFulfilled 处理器必须按照原始调用 `then` 的顺序执行。因此，第一个 `then` 函数中的 onFulfilled 回调将执行，然后是第二个 `then` 中的 onFulfilled 回调，依此类推。这种情况同样适用于场景中 onRejected 回调的执行。这复杂吗？也许下面的例子可以解释它：

```javascript
var p = [[promise]];
p.then();
p.then();
```

前面的代码与以下行代码不同：
`promise.then().then();`

区别在于 `promise.then()` 可能会返回不同的 promise。

最后，在分类级别上，Promises/A+ 提案提供了与 Promises/A 不同的命名，因为新规范的作者希望反映已在许多 promise 实现中传播的词汇。变化包括：

- promise 状态被称为 pending（待定）、fulfilled（已完成）和 rejected（已拒绝），取代了 unfilled、fulfilled 和 failed
- 当 promise 被 fulfilled 时，该 promise 拥有一个值；同样，当 promise 被 rejected 时，它拥有一个原因

`then` 方法是 API 中的核心角色。正如我们在上一节中看到的，如果一个对象没有 `then` 方法来获取和访问其当前或最终的值或原因，则不被视为 promise。该方法接受两个参数，这两个参数需要是函数，如下所示：

```javascript
promise.then(onFulfilled, onRejected);
```

让我们深入研究 `then` 的细节及其参数的规范，并考虑之前简单 `then` 方法的代码示例：

- 参数 onFulfilled 和 onRejected 均是可选的。
- 两个参数都必须是函数；否则必须被忽略。

### Promise API 及其兼容性

- 在同一个调用中，两个参数都不能被调用多次。
- onFulfilled 参数必须在 promise 被 fulfilled 后才被调用，并将 promise 的值作为其第一个参数。
- onRejected 参数必须在 promise 被 rejected 后才被调用，并将 promise 拒绝的原因作为其第一个参数。
- onFulfilled 和 onRejected 参数不能作为 `this` 值传递；如果你在 JavaScript 代码中应用严格模式，这在处理器中将被处理为 `undefined`；在非严格模式下，它将处理视为 JavaScript 代码中的全局对象。
- `then` 方法可以在同一个 promise 上被调用多次。
- 当 promise 被 fulfilled 时，所有 onFulfilled 处理器必须按照它们原始调用 `then` 的顺序执行。同样的规则也适用于 onRejected 回调。
- `then` 方法必须返回一个 promise，如下：
  `promiseReturned = promise.then(onFulfilled, onRejected);`
- 如果 onFulfilled 或 onRejected 返回一个值 `x`，则必须调用 promise 解决程序来解析值 `x`，如下代码所示：
  `promiseReturned = promise.then(onFulfilled, onRejected); [Resolve](promiseReturned, x).`
- 如果 onFulfilled 或 onRejected 处理器抛出异常 `e`，`promiseReturned` 必须被拒绝，并以 `e` 作为拒绝或失败的原因。
- 如果 onFulfilled 不是函数且 promise 被 fulfilled，`promiseReturned` 必须以相同的值被 fulfilled。
- 如果 onRejected 不是函数且 promise 被 rejected，`promiseReturned` 必须以相同的原因被拒绝。

之前的列表是 Promises/A+ 标准中定义并指定的 promise 和 `then` 方法的详细规范。我们在上一个列表中提到的 promise 解决程序，但我们并不知道它是什么。嗯，promise 解决程序基本上是一个抽象操作，它接受一个 promise 和一个值作为参数，指示如下：

```
[[Resolve](promise, x)]
```

如果 `x` 是 thenable（可通），即它是一个定义了 `then` 方法的对象或函数，那么 resolve 方法将强制 promise 假设处于 `x` 的状态，前提是 `x` 的行为至少有点像一个 promise。否则，它将用值 `x` 履行 promise。

# 第 2 章

promise 解决程序处理 thenables 的技术允许不同的实现之间能够可靠地相互工作，只要 promise 暴露了符合 Promises/A+ 标准的 `then` 方法即可。此外，它还允许将非标准实现与具有合理 `then` 方法的实现相整合。

> Promise 解决程序（PRP）不是公共 API。它旨在描述一个重要的、但抽象且内部/私有的过程，这里的“过程”仅指“算法”，而不是具体的 JavaScript 函数。特定的 promise 实现可以根据其认为最合适的方式进行实现。
> - Brian Cavalier, Promises/A+ 共同编辑解释

promise 解决程序允许我们拥有 `promise.resolve` 的正确实现。同时，保证 `then` 的正确实现也是必要的。你可能会发现 promise 解决程序没有没有，，因为它是一个抽象过程，可以由特定 promise 实现作者认为的任何方式进行实现。在这里，结果留给实现者，只要它实现了目标，即将 promise 置于与 `x` 相同的状态。因此从概念上讲，它影响了 promise 上的状态转换。

虽然 promise 过程的实现取决于实现者，但它也有一些我们应该遵守的规则。这些规则如下：

1. 如果 `x` 是 thenable，即它是一个定义了 `then` 方法的对象或函数，resolve 方法将强制 promise 假设处于 `x` 的状态，前提是 `x` 的行为至少有点像一个 promise。否则，它将用值 `x` 履行 promise。
2. 如果 `x` 是一个 promise，promise 必须保持 pending 状态直到它被 fulfilled 或 rejected：
   - 如果 x 被 fulfilled，promise 应以相同的值被 fulfilled
   - 如果 x 被 rejected，promise 应以相同的原因被拒绝
3. 如果 `x` 是对象或函数，且不是 promise，则实现应该调用 `x.then`。

### Promise API 及其兼容性

- 如果获取 `x.then` 属性最终抛出异常，promise 应以 `e` 为原因被拒绝。
- 如果 `then` 是函数，用 `this` 的值调用它。第一个参数应该是 `resolvePromise`，第二个参数应该是 `rejectPromise`。
- 如果 `then` 不符合函数定义，直接用 `x` 履行 promise。
- 4. 如果 `x` 既不是对象也不是函数，promise 应被履行 `x`。

让我们看看第三条规则。我们看到，如果 `then` 是函数，第一个参数应该是 `resolvePromise`，第二个参数应该是 `rejectPromise`，此时适用以下规则：

1. 如果/当 `resolvePromise` 被带值 `z` 调用时，实现必须运行 [Resolve](promise, z)。
2. 如果/当 `rejectPromise` 被带原因 `j` 调用时，实现必须以原因 `j` 拒绝 promise。
3. 如果处理器 `resolvePromise` 和 `rejectPromise` 都被调用，或者在同一个参数被多次调用的情况下，第一个调用具有优先权，任何其他后续调用均被忽略。
4. 如果调用 `then` 导致抛出异常 `e`，我们有两种情况：
   - 如果 `resolvePromise` 或 `rejectPromise` 处理器已经被调用，我们应该忽略 `then`
   - 如果没有，实现应以 `e` 作为返回的原因拒绝 promise。




此外，承诺解析程序（promise resolution procedure）即使在面对不合规（且略有危险）的 thenables 时，也能确保正确性。一个例子是使用 `resolve` 函数将 jQuery 版本的 promise（它不符合 A+ 标准）转换为一个真正的简单且符合标准的 promise。以下代码说明了该实现：

```javascript
// 一个返回 jquery promise 的 ajax 调用
var jQueryPromise = $.ajax('/sample.json');
// 修复它并将其转换为符合标准的 promise
var standardPromise = Promise.resolve(jQueryPromise);
```

归根结底，Promises/A+ 的核心目标是提供一个最少、最简单的规范，以便在存在风险的情况下，也能允许不同 promise 实现之间进行可靠的互操作。

> Just为了消除可能产生的任何困惑，承诺解析程序与某些实现在公共 API 中提供的 `promise.resolve` 方法并不相同。

为了符合 Promises/A+ 标准的核心目标，Promises/A+ 组织创建了一个合规性测试套件，用于测试 promise 库或 API 实现是否符合 Promises/A+ 规范。合规测试可以在 https://github.com/promises-aplus/promises-tests 找到，其目的是为实现是否满足要求并符合标准提供更具体的指导和证据。

### 浏览器支持与兼容性

JavaScript 与浏览器紧密耦合，promise 也是也是如此，因为 promise 在之前的 ECMAScript 版本中并不是标准，而它们将成为新的 ECMAScript 6 发布版本的一部分；因此它们不会在所有浏览器中都得到支持。此外，promise 可以被实现，我们将见证许多库提供类似 promise 的功能或暴露 promise 的能力。在本章的剩余部分中，我们将涵盖这两个在处理 promise 时至关重要的要点。

### Promise API 及其兼容性

### 检查浏览器兼容性

与任何客户端技术一样，JavaScript 显式地开发用于在结合 HTML 页的 Web 浏览器中使用。它利用浏览器来完成工作，这就是为什么它是一门脚本语言。一旦脚本被发送到浏览器，就由浏览器来对其进行处理。这里存在很强的依赖关系；因此，浏览器兼容性至关重要。

某些浏览器中已经有了 promise 的实现；在编写本书时，有一小部分浏览器支持 promise，如下由 Kangax 提供的 ECMAScript 6 兼容性表：

| 特性名称 | IE 10 | IE 11 | FF 24 | FF 25 | FF 27-28 | FF 29 | FF 30 | FF 31 | CH 30 | CH 33 | CH 34 | CH 35 | SF 6 | SF 7 | WK | OP 12 | OP 15 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Promise | No | No | No | No | Yes | Yes | Yes | Yes | Yes | Yes | Yes | No | No | Yes | No | No |

数据来源：http://kangax.github.io/compat-table/es6/#Promise

> > 兼容性表中的缩写：
> IE 代表 Internet Explorer，FF 代表 Firefox，CH 代表 Chrome，Safari 代表 Webkit，OP 代表 Opera。

正如我们在上一个表中看到的，Firefox 的最后三个版本（截至版本 29）和 Chrome（截至版本 32）默认启用了 promise。不用担心，因为有一个 polyfill（垫补程序）可以为不支持 promise 的浏览器添加 promise 功能。

> > Polyfill 是由 Remy Sharp 创造的新术语，并在 Web 社区中流行起来。它代表一段代码，交付了我们期望浏览器原生提供的技术和行为。我们可以将其看作计算中的一个补丁。

这个 polyfill 发挥了魔法并为我们提供了 promise 支持，可以从此链接下载：https://www.promisejs.org/polyfills/promise-4.0.0.js。它基本上为那些没有原生实现 promise 的浏览器添加了 promise 支持。它也可以用于为 Node.js 提供 promise 支持。以下代码示例显示了如何包含它：

```html
<script src="https://www.promisejs.org/polyfills/promise-4.0.0.js"></script>
```

## 第2章

我们展示 ECMAScript 6 兼容性表是因为 promise 是 ECMAScript 6 规范的一部分，该规范将 promise 作为一种原生语言特性提供，且其实现基于 Promises/A+ 提案。

### 具有类似 promise 功能的库

promise 的概念对于 Web 开发和 JavaScript 世界来说并不新鲜。开发者可能通过库以非标准化的方式在 JavaScript 中遇到或使用过 promise。这些库是 promise 概念的实现；其中一些是合规实现并已开始采用 promise 模式，而许多并不是。此外，这些库中的某些并不符合 Promises/A+ 标准，这在我们选择项目中使用何种 JavaScript 库时是一个非常重要的要求。


以下是一些完全符合 Promises/A+ 规范的库列表，因此我可以保留地推荐它们：

- **Q.js**: 由 Kris Kowal 和 Domenic Denicola 开发，包含一个功能齐全的 promise 库，包含了 Node.js 的适配器和对进度处理程序的支持。可以在 `https://github.com/kriskowal/q` 下载。
- **RSVP.js**: 由 Yehuda Katz 开发，提供了一个非常轻量级的 promise 库。可以从 https://github.com/tildeio/rspv 下载。
- **when.js**: 由 Brian Cavalier 开发，它提供了中间件库并扩展了进度和取消的功能。可以从 https://github.com/cujojs/when 下载。

此外，我们还有 `then` (https://github.com/then)`，它是符合 Promises/A+ 规范的实现，并在 promise 成功或被拒绝时提供进度处理等功能。

## 总结

正如我们所看到的，promise 的概念并不新鲜，在 JavaScript 中已经通过不同的库实现存在了很久，无论它们是符合标准的还是其他的。然而，现在，所有这些努力都汇聚成了 Promises/A+ 社区规范，大多数库都遵循该规范。因此，我们通过在下一个 ECMAScript 版本中包含的标准 Promise 类在 JavaScript 中获得了对 promise 的原生支持，允许 Web API 为其异步操作返回 promise。此外，我们深入探讨了 promise API 和 `then` 方法，并了解了新标准的当前浏览器兼容性。最后，我们简要介绍了一些实现 promise 并符合 Promises/A+ 规范的库。

在接下来的章节中，我们将重点介绍 promise 的链式调用（chaining）以及如何使用 `then` 方法来实现它以启用多个异步操作。




# 3 Promise 链式调用

Promise 最重要的特性之一是能够链式调用并管理一系列异步操作。在上一章节中，我们已经学习了 Promise API 的细节以及它的工作原理；特别是，我们看到了 `then` 方法是如何工作的。我们还学习了 Promise 对当前浏览器的兼容性，以及实现和扩展 JavaScript Promise 的库。在本章中，我们将涵盖以下主题：

- 链式调用在异步 JavaScript 中是如何产生的
- 使用 Promise 实现链式调用
- 从“回调地狱”转换为组织良好的 Promise 链

## 前所未有的链式调用

正如我们在前两个章节中学到的，Promise 倾向于将同步编程的强大功能引入异步函数。Promise 的这种能力包含了同步函数的两个关键特征：

- 返回值的函数
- 抛出异常的函数

这些特征的意义在于，它们可以用于将一个函数的返回值直接传递给另一个函数——而且不仅仅一次；这可以转化为将这些函数按顺序链联的能力，其中链中元素之间的绑定关系是每个操作的 Promise 返回值。现在，第二个特征的含义非常重要，因为抛出异常允许我们主要检测过程是否失败；其次，它允许我们通过链中处理 `catch` 的任何函数捕获这些异常，帮助我们避免在这些链函数中间丢失异常。

那么，这如何转化到异步世界呢？

## Promise 链式调用

首先，在异步世界中，人们不能简单地返回值，因为这些值尚未及时准备好。同样，我们也不能抛出异常，基本上是因为没有人来捕获这些出的异常。因此，机智多角的开发者尝试通过回归嵌套回调来解决这个问题。这允许他们将带有返回值的函数链起来，但是以牺牲维护性、可读性以及额外的代码行为代价的。当代码增加且嵌套回调增长时，当需要编辑或出现错误时，代码变得越来越难以维护和调试。此外，嵌套回调对可读性有不利影响，开发者需要折叠和展开分支来跟踪代码，判断回调函数的开始和结束。

此外，在这些嵌套回调中捕获错误非常困难，需要开发者手动将错误沿回调链向上传递。这种异步编程中的痛苦经历是出名的，被称为“回调地狱”；它通常导致类似于下面演示的代码：

```javascript
function shout(shoutTxt, callbackFunc) {
  alert(shoutTxt);
  callbackFunc("b");
}

shout('First Shout!', function (a) {
  if (a == "a") {
    alert("hey, there is an error!");
  }
  else {
    shout('Shout Again!', function (a) {
      shout('Third shout!', function (a) {
        a = "c";
        if (a == "c") {
          shout('I am inside the third shout!',
            function (a) {
              alert("hey, I can " + a.toString());
            });
        }
        else {
          shout('I am still inside the third shout!',
            function (a) {
              alert("Alright I am tired");
            });
        }
      });
    });
  }
});
```

# 第 3 章

在上一个例子中，你会注意到在看起来像金字塔的代码中，到处都是函数和 `}}};`，请注意我们甚至没有包含错误处理代码。上一个例子在小规模上描述了回调地狱的样子。我们还可以观察到嵌套回调（这在 JavaScript 编程中非常盛行）如何不受控制地增长成交织且难以维护的代码。想象一下在更复杂的场景下代码会是什么样的。

尽管如此，开发者可以实施一些补救措施，使嵌套回调更具可读性和维护性。这些措施包括在回调参数中使用命名函数代替匿名函数。另一种解决方案是将代码拆分成更块，将执行特定任务的代码放在单独的模块中，然后将该模块插入到应用程序代码的其他地方。然而，这些措施更多是权宜之计而非标准做法；此外，权宜措施不足以完全解决异步操作链的概念。

另一方面，Promise 提供了我们在同步编程中的函数组合，或者说与 JavaScript 中的异步编程相比的一种开箱即用的方式。

为什么呢？因为规范规定 Promise 必须提供 `then` 方法。不仅如此，规范还要求函数（或任何具有合规实现的函数）应该返回一个 Promise。返回的 Promise 包含一个值（如果已完成）或一个异常（如果被拒绝）。因此，`then` 可以使用返回的 Promise 与另一个函数组合成一个链，其中第一个操作的结果被传递给下一个操作，依此类推。此外，这可以在任何时间被拒绝操作中断，拒绝操作可以由链中任何声明了异常处理代码的操作处理；换句话说，错误将通过该链自动冒泡。

> 一些爱好者认为这种 Promise 链式调用是新标准中最好的部分。

在 JavaScript 编程中，当我们需要执行多个异步操作场景时，链式调用非常重要。这些场景包括一个操作依赖于上一个操作结果的情况。此外，我们可能遇到第一个操作在返回结果并传递给下一个操作之前需要处理某些代码的情况。记住，这一切应该在不阻塞其他线程（尤其是 UI 线程）的情况下发生。在这里，我们需要一种简单的标准机制来链接这些异步操作，而这正是 Promise 提供的。

## Promise 链式调用

提到链式调用时，只要 `then` 返回 Promise，链就可以达到我们想要的深度。但需要注意的是，如果我们进行像 `promise.then(onFilled)` 这样的调用，`onFilled` 函数只能在 Promise 运行结束后被调用，并将 Promise 的值作为其第一个参数。因此，如果我们在第一个 `then` 内部返回一个简单值并将其链到另一个，下一个 `then` 将用上一个 `then` 返回的简单值被调用。如果我们在第一个 `then` 中返回一个 Promise，随后的 `then` 将必须等待返回的 Promise，并且只有在 Promise 履行或完成后才会被调用。

让我们来看实际操作。以下是一个演示链式 Promise 的非常基础示例代码：

```javascript
var promiseObj = function (time) {
  return new Promise(function (resolve) {
    setTimeout(resolve, time);
  });
}

promiseObj(3000).then(function () {
  alert('promise 1');
}).then(function () {
  alert('another promise');
});
```

该脚本非常直观，你可以在任何开发环境环境中编写它，甚至可以在 JSfiddle.net 等在线代码编辑器中编写。首先，我们通过定义 `promiseObj` 对象创建一个 Promise。这个对象是一个函数，每次接受一个参数并返回一个新的 Promise。

> 记住，正如我们在第 2 节“Promise API 及其兼容性”中学到的，并不是所有浏览器都支持 Promise。要这样做，你需要在兼容的浏览器在 JSiddle 上运行或测试代码。返回本章检查兼容的浏览器。





## 第3章

代码的第二部分是链式的地方。我们首先调用刚刚创建的 `promiseObj`；由于它会返回一个 promise，我们可以在上面调用 `then`。
根据定义，`promiseObj` 接收一个 `time` 参数（单位为毫秒），并传递给 `setTimeout` 函数。在这里，我们传递了 3000（3秒），并在内部我们简单地调用了一个 `alert()` 函数，它将如如下截图所示在屏幕上弹出：

```javascript
var promiseObj = function(time) {
  return new Promise(function(resolve) {
    setTimeout(resolve, time);
  });
};
promiseObj(3000,function () {
  alert('promise 1');
}).then(function () {
  alert('another promise');
});
```

现在，由于 `then` 返回一个 promise，我们可以对其链式另一个 `then`；这将在 promise 解决后执行，并而执行一个 `alert()` 函数。虽然上一个例子非常基础，但它说明了我们如何轻松地通过 promise 链组合异步操作。

让我们把之前看到的嵌套回调示例转换为 promise 链。为了说明目的，我将添加一个 HTML 元素 `div`，并在 promise 的传播向其中填充内容。

HTML 部分如下：

```html
<div id="log"></div>
```

JavaScript 部分如下：

```javascript
var log = document.getElementById('log');
var shout = new Promise(function (resolve) {
  log.insertAdjacentHTML('beforeend', 
  '<small>Promise started </small><br>');
  window.setTimeout(
    function () {
      resolve('First Shout!'); // fulfill the promise !
    }, 2000);
  );
});
```

```javascript
shout.then(function (val) {
  log.insertAdjacentHTML(
    'beforeend', val + ' (<small>Promise fulfilled</small><br/>');
  var newVal = 'Shout Again!';
  return newVal;
}).then(function (val) {
  log.insertAdjacentHTML('beforeend', val + ' ( <small>Promise fulfilled</small><br/>');
  var newVal2 = 'Third shout, you\'re out!';
  return newVal2;
}).then(function (val) {
  log.insertAdjacentHTML('beforeend', val + ' ( <small>Promise fulfilled</small><br/>');
  return val;
});
```

在 HTML 中，我们只有一个空的 ID 为 `log` 的 `div` 元素。在 JavaScript 中，我们首先声明一个名为 `log` 的变量来持有该 `div` 元素。我们构建了一个新的 promise 并将其赋值给变量 `shout`。在该 promise 对象内部，我们添加了内容以强调我们刚刚开始了 promise。我们在这里承诺的是等待 2 秒（2000 毫秒）后的 `shoutText` 字符串。我们再次使用了 `window.setTimeout` 函数来模拟一个需要时间完成的异步操作。它将在给定时间后通过解析来完成 promise。

接下来，我们使用 `then` 方法调用 `shout`，我们已经定义了在 promise 完成时将执行的操作。在第一个方法中，我们简单地将 `val` 参数（包含 `shoutText` 的值）传递给 `log.insertAdjacentHTML` 函数。这将在 `div` 元素的内容旁边显示 Promise，并用小字体显示 Promise fulfilled。接下来，我们定义了一个新变量 `newVal`，将其赋值为文本 "Shout Again" 并返回它。继续，第二个 `then` 也显示从上一次调用返回的值。我们也定义了一个新变量，为其赋值一个文本值并返回它。最后一个 `then` 只是将 `val` 的值（此时它等于 `newVal2`）并到 `div` 元素的内容中。注意，`val` 持有了链中上一个操作到下一个操作 promise 返回的值的内容。

此示例也可以在 JSFiddle.net 上测试。

## 顺序链式

我们不仅可以用 promise 链组合异步操作，还可以按这种方式组合，使其按顺序运行这些操作。正如我们在在本章之前学到的，如果一个 `then` 操作返回一个值，后续的 `then` 将带有该值调用，除非第一个 `then` 返回一个 promise；如果发生这种情况，后续的 `then` 将等待返回的 promise，并且仅在 promise 解决或拒绝时才被调用。这条规则允许我们以这种方式队列这些异步操作，使每个操作等待上一个操作完成，从而按顺序运行。让我们来看一个解释此点的例子。在这个例子中，我们有一个函数 `getData`，它接收一个 JSON 文件并从 JSON 文件中检索数据。第一个 JSON 文件有类别，对于每个类别，我们需要按顺序获取每个类别下的项目。让我们使用以下代码来实现此：

```javascript
getData(jsonCategoryUrl).then(function(data) {
  // 获取类别 1 的项目
  getItemsPerCategory(data.categories[0]).then(function(items) {
    // 在处获取了项目
  });
  return getData(data.categories[0]); //返回类别 1
}).then(function(category1) {
  alert("We now have category 1", category1);
  // 返回类别 2
  return getData(data.categories[1]);
}).then(function(category2) {
  alert("We now have category 2", category2);
  // 返回类别 3
  return getData(data.categories[2]);
});
```

之前的代码示例对 `jsonCategoryUrl` 函数进行了异步调用，它将返回一组类别；在此之后，我们通过传递 `data.categories[0]` 参数来获取第一个类别中的项目，并将第一个类别传递给下一个 `then` 调用。在链式 promise 的第二个链接中，我们获取第二个类别数据 `data.categories[1]` 并将其传递给最后一个 `then` 调用，反而又获取了第三个类别 `data.categories[2]`。这个例子向我们展示了如何在链式 promise 中队列异步操作，我们需要一个链，其中一个链接依赖或需要等待前一个 promise 的结果。

## Promise 链式

这种功能真正让 promise 与普通的回调模式脱颖而出。我们可以通过制作一个快捷方法来获取类别来优化之前的代码，如下代码所示：

```javascript
// 声明 categorypromise 变量
var catPromise;
function getCategory(i) {
  // 如果 catPromise 没有值则获取数据，否则直接从
  // catPromise 的值填充
  catPromise = catPromise || getData(jsonCategoryUrl);
  return catPromise.then(function(category) {
    // 获取该类别下的项目
    return getData(category.Items[i]);
  });
}
getCategory(0).then(function(items) {
  alert(items);
  return getCategory(1);
}).then(function(items) {
  alert(items);
});
```

在之前的代码示例中，我们首先声明一个名为 `catPromise` 的变量来持有类别 promise。接下来，我们声明一个名为 `getCategory(i)` 的函数，它接收 `i` 的值作为参数；并将 `catPromise` 设置为 `getData(jsonCategoryUrl)` 函数检索的 JSON 数据；然而，使用 `||` 运算符我们可以首先检查 `catPromise` 对象是否有值，这样我们只获取一次类别 JSON 文件。当我们调用 `getCategory(0)` 时，它将检索第一个类别；在此之后，它通过 `getCategory(1)` 返回类别并传递给最后一个 `then`。通过这种方式，在调用 `getCategory` 之前我们不会下载类别 JSON 文件；尽管我们经常再次调用 `getCategory` 函数，但我们不需要下载，因为它在操作序列中被重用。通过 promise 流水，第一个操作的结果被传递给后续操作。此外，此示例展示的重要特性是，`then` 函数返回一个新的 promise，`then` 返回的 promise 在该函数返回的 promise 完成之前将不会完成，从而在链中队列了异步操作。

## 总结

Promise 是处理异步操作复杂性的极佳方法。Promise 为 JavaScript 中异步操作的简单链式提供了一种极佳的机制。它们允许你比回调模式更好地管理这些操作的序列。

在下一章中，我们将学习处理 promise 中的错误，查看如何使用 promise 管理异常，并查看处理 promise 异步操作中出现错误的示例。





# 4 错误处理

与任何编程语言一样，错误和异常不可避免地会出现；为了确保代码运行顺畅并便于调试，我们需要抛出并捕获这些异常。异步 JavaScript 编程可能是枯燥的。然而，Promise 为我们提供了一种处理错误的优秀机制，我们将在本章中进行探索。在整个章节中，我们学习了异步操作的链式。我们还看到如何将“回调地狱”转换为更具可读性和维护性的 Promise 链。在本章中，我们将涵盖以下主题：

- Promise 中的异常和错误处理
- 如何使用 `then` 和 `catch` 方法通过 Promise 处理错误

### # 异常与 Promise

在异步 JavaScript 编程中，没有标准或公认的异常处理机制，这主要是因为这些异常发生在未来，并且无法判断一个被拒绝（rejected）的 Promise 是否最终会被处理。此外，在异步世界中，我们不能简单地抛出异常，因为当这些错误准备就绪时，没有人去捕获它们。因此，人们创建了解决方法来解决这个问题。捕获错误和异常的常用技术是将这些异常手动向嵌套回调的链上传。而另一方面，Promise 为我们提供了开箱即用的错误处理和冒泡机制。它们通过声明：你的函数应该返回一个 Promise，如果失败，则返回一个带有原因的拒绝。

## 错误处理

我们在第 1 章《JavaScript Promises - 我为什么要关注它？”中学习到，一个 Promise 可以处于三种不同的状态：等待中（pending）、已完成（fulfilled）和已拒绝（rejected）。
拒绝状态的要求如下：

- Promise 不得变为任何其他状态（pending 或 fulfilled）
- Promise 必须有一个被拒绝的原因，且该原因在该 Promise 内部不能改变

这些对拒绝状态的要求允许了错误处理，更重要的是允许错误组合，即该 Promise 拒绝的原因将通过 `then` 方法自动冒泡到该 Promise 链中。Promise 允许错误像同步异常一样在代码链中向上传播。此外，它提供了一个更清晰的状态来异步处理错误。

通常，在使用回调方法的异步编程中，我们需要将认为不安全的代码块封装在 `try-catch` 块中。如下代码示例所示：

```javascript
try {
  return JSON.parse("json"); // 这会导致一个错误
} catch (error) {
  alert("I have an error with the following details:\n\n" + error);
}
```

之前的代码示例显示了一个意图提示错误的脚本块。在该代码块中，我们将 `return JSON.parse("json");` 封装在 `try...catch` 块中，并通过传递无效的 JSON 参数故意导致了错误。JavaScript 函数 `JSON.parse()` 用于将 JSON 文本转换为 JavaScript 对象。在我们的示例中，它将尝试解析文本 "json" 并抛出错误。我们将捕获该异常并显示一个包含错误详情的警告框。

如果我们在 HTML 页面或在线 JavaScript 编辑器中运行此脚本，结果将是一个带有以下消息的警告框：

I have an error with the following details:
SyntaxError: Unexpected token j

我们可以通过此公共 jsFiddle URL 查看代码：http://jsfiddle.net/RamiSarieddine/mj6hs0xu/

# 第 4 章

正如我们目前所见，如果 Promise 发生错误，它要么是已完成的要么是已拒绝的。当一个 Promise 被拒绝时，它类似于在同步代码中抛出异常。带有 `then` 函数的标准 Promise 按照代码所示接收两个参数 `onFulfilled` 和 `onRejected`：

```javascript
promise.then(onFulfilled, onRejected)
```

`onRejected` 参数是一个作为错误处理器的函数，它会在 Promise 失败时被调用。当 Promise 中发生错误或异常时，意味着该 Promise 被拒绝了，抛出的错误将传递给 `onRejected` 错误处理器。当我们调用 `onRejected` 时有几个考虑因素，可以总结为以下列表（假设是一个简单的 Promise）：`then(onFulfilled, onRejected)`：

- `onRejected` 必须仅在 Promise 被拒绝后才被调用，并将拒绝原因作为其第一个参数
- `onRejected` 的调用次数不能超过一次

第二个考虑因素非常直观易见。`onRejected` 函数不会在同一个 Promise 上被多次调用。第一个考虑因素断言，如果 Promise 被拒绝，`onRejected` 将会被调用。

尽管如此，拒绝也会隐式发生，以及在 във Promise 的构造函数回调中抛出错误的情况。以下代码示例说明了这一点：

```javascript
var promiseTest = new Promise(function (resolve) {
  // JSON.parse 将因为无效的 JSON 抛出错误
  // 所以这直接导致拒绝
  resolve(JSON.parse("json"));
});

promiseTest.then(function (data) {
  alert("It worked!" + data);
}, function (error) { // 错误处理器
  alert("I have failed: " + error);
});
```

在之前的代码中，我们定义了一个新 Promise `promiseTest`，并在构造函数回调调用 `JSON.parse()` 时，我们故意传递了一个无效参数以导致错误。现在，这将在构造函数中抛出一个错误，并且当我们使用 `then` 方法调用 Promise 时，它将间接导致一个拒绝。如果我们有一个 `onFulfilled` 处理器，我们就不会捕获该错误。异常将作为拒绝中的参数抛出，其值为 `error`。我们在 `promiseTest.then()` 的参数中提供了一个错误处理器；因此我们可以捕获并处理该错误。

你可以通过此公共 Fiddle 测试此示例代码：http://jsfiddle.net/RamiSarieddine/mj6hs0xu/

> 错误会自动冒泡并变成拒绝，这在处理 Promise 相关的构造函数回调时非常方便；如果那里出现任何错误，当 Promise 被调用时将被捕获。

## 使用 Promise 处理错误

正如我们所见，在异步编程中，Promise 提供了更丰富的错误处理机制。尽管 Promises/A+ 规范只处理了一个方法即 `.then(onFulfilled, onRejected)`，并没有提供其他，但这些方法为 Promise 的互操作性奠定了基础，并扩展了 Promise 的功能。

我们可以考虑与 Promises/A+ 兼容的库中的几种错误处理实现。这些扩展中包含了 `catch()` 方法，它是通过基础的 `then()` 函数实现的。任何人都可以编写 `catch()` 方法并通过扩展对象将其包含在脚本中，如下：

```javascript
Promise.prototype.catch = function(onRejected) {
  return this.then(null, onRejected);
};
```

在之前的代码中，定义了一个名为 `catch` 的方法来扩展 `then()` 函数（注：此处 OCR 文本为“extends the object”，但我们遵循逻辑）。逻辑：在之前的代码中，定义了一个名为 `catch` 的方法来扩展 `then()` 函数（注：此处 OCR 文本为“extends the object”，但代码是 `Promise.prototype.catch`）。

实际上，查看原始文本：在之前的代码中，定义了一个名为 `catch` 的方法来扩展 `then()` 函数（注：此处 OCR 文本为“extends the object”，但代码是 `Promise.prototype.catch`）。

实际上，查看原始文本：在之前的代码中，定义了一个名为 `catch` 的方法来扩展 `then()` 函数（注：此处 OCR 文本为“extends the object”，但代码是 `Promise.prototype.catch`）。

实际上，查看原始文本：在之前的代码中，定义了一个名为 `catch` 的方法来扩展 `then()` 函数（注：此处 OCR 文本为“extends the object”，但代码是 `Promise.prototype.catch`）。

实际上，查看原始文本：在之前的代码中，定义了一个名为 `catch` 的方法来扩展 `then()` 函数（注：此处 OCR 文本为“extends the object”，但代码是 `Promise.prototype.catch`）。





## 错误处理

正如我们所学到的，对于应用程序开发者来说，`Catch()` 函数更优，因为它具有更好的可读性和直观的错误处理流；而 `promise.then(handler1, handler2)` 主要用于实现 promise 内部。

错误处理机制允许我们编写以安全方式执行任务的函数。让我们来看下面这段包含 `catch()` 错误处理的 promise 链，并查看它是如何转换为流程图：

```
promise1.then(function () {
  return promise2();
}).then(function () {
  return promise3();
}).catch(function (error) {
  return promiseError1();
}).then(function () {
  return promise4();
}, function (error) {
  return promiseError2();
})
.catch(function (error) {
  alert("Everything is gonna be alright!");
})
.then(function () {
  alert("We are out of here!");
});
```

上述 promise 链和错误对应的流程图将如下所示：


绿色的框将是执行（fulfilled）的部分；红色的框代表 promise 被拒绝（rejected）时的错误处理器。我们可以通过线条跟踪处理流程，知道哪些是执行的，哪些是被拒绝的，并与之前的代码示例进行比较，从而更直观地理解错误在该 promise 链中是如何传播的。

## 总结

JavaScript promise 提供了一种标准化的错误处理方法，其实现基础存在 `then` 方法的规范中，并可以扩展出如 `catch` 等方法，从而编写出更易读、更直观的错误处理代码。`then` 函数提供了两个强大的参数：`onFulfilled` 和 `onRejected`。这些函数参数允许我们处理已执行的 promise 操作返回的值，以及 promise 被拒绝时返回的错误。在下一章中，我们将介绍 WinJS 库；我们将学习该库中的 promise 对象以及我们如何在 Windows 开发中使用它。

# 第5 章

## WinJS 中的 Promises

Promise 具有来自各种框架的各种实现，但它们都共享一个共同的基础；这就是 promise 的概念。实际上，几乎所有的 promise 库都提供了一个共同特性，使使用 JavaScript 进行异步编程变得更加简单和高效。WinJS（Windows JavaScript 库）是拥有自己 promise 实现的库之一，我们将在本章节中探索它。在上一章中，我们学习了如何处理 promise 操作过程中产生的异常。我们还看到 JavaScript promise 如何配备了强大的错误处理机制。此外，我们学习了如何通过 `then` 和 `catch` 方法处理错误。在本章中，我们将涵盖以下内容：

- WinJS 命名空间介绍
- WinJS promise 对象的详细说明
- 在 Windows 应用开发中使用 `WinJS.Promise` 的基础示例

## 介绍 WinJS

WinJS 是 Windows library for JavaScript 的缩写，是微软开发的一个 JavaScript 库，最近已开源。该库的设计目的是允许开发者为 Windows 8（使用 HTML5 和 JavaScript）构建具有原生级和原生质量体验的 Windows Store 应用，例如 Skype 和音乐应用。它已成为使用 XAML 和 C#、VB.Net 或 C++ 编写原生应用的第二选择。这种替代方案允许 Web 开发人员利用他们的知识和技能来构建商店应用。WinJS 库更像是一个全面的工具包，它不仅提供了丰富的命名空间，还包含了以下特性：

- 通过 Windows Runtime (WinRT) 访问设备硬件

## WinJS 中的 Promises

- 提供精细的 UI 控件，如 ListView、FlipView 和 Semantic Zoom 以及页面控件
- 提供稳健的基础设施，如 promise 和数据绑定

此外，WinJS 也可以与其他库和框架一起在独立解决方案中使用。

WinJS 自启动以来已经进化了很多。它最初是一个针对 Windows Store 应用的特定平台，现在支持 Web 浏览器和其他设备，以尝试跨平台化。这种尝试正在最新的 WinJS 2.1 版本中结出晶，该版本支持 Windows Phone 8.1，并且现在 WinJS 已被用于 Xbox One，并且已准备好涵盖其他非微软浏览器和设备上的网站及 Web 应用。

> 开源的 WinJS 现在托管在 GitHub 上：https://github.com/winjs/winjs/，社区成员可以在那里查看库并贡献其源代码。

所有 WinJS 库函数都定义在一个名为 WinJS 的命名空间下。WinJS 命名空间为 Windows Library for JavaScript 提供了特殊功能，包括 promise 对象和 `xhr` 函数。它包含了三类型的成员对象：属性和函数

对象包含以下两个成员：

- ErrorFromName：这是一个简单的错误对象。
- 一个 promise 对象：这是我们本章的讨论重点。与整本书一直在讨论的 promise 对象类似，它基本上提供了一种技术，针对一个尚不存在的值分配要执行的任务。它为处理异步执行的 API 交互提供了一种抽象机制。

属性包括：

- validation：此属性包含一个 setter，用于显示验证过程的结果

函数包含以下三个成员：

- log：此函数记录输出并将其写入 Visual Studio 内部的 JavaScript 控制台。此函数可以通过自定义实现进行扩展，或使用 `WinJS.Utilities.startLog` 将日志记录到 JavaScript 控制台。

# 第 5 章

- strictProcessing：此函数已不再需要，因为严格处理默认是开启的。由于该函数不再需要，它已被弃用。
- xhr：此函数仅是将 `XMLHttpRequest` 封装为 promise。

以上从宏观视角总结了 WinJS 命名空间；WinJS 的代码位于 `base.js` 中。

## 解释 WinJS.Promise 对象

该对象是 WinJS 库最重要的部分之一，promise 实例涉及我们与异步 API 的一切交互。让我们深入该对象的细节。从结构上来说，promise 对象包含以下三类型的成员。

### 构造函数

在 WinJS 的构造函数层面，使用 `WinJS.Class.define` 函数创建类。在其第一个参数中是一个作为构造函数的函数。现在，在 Promise 类的情况下，它派自一个名为 `PromiseStateMachine` 的基类，使用 `WinJS.Class.derive` 函数，其第二个参数是构造函数。在两种情况下，构造函数都可以命名为任何名称；也可以是匿名的。然而，WinJS.Promise 构造函数的描述与对象本身相同。WinJS.Promise 构造函数接受两个参数：`init` 和 `onCancel`。

声明一个新的 promise 对象时，我们需要两个参数。这两个参数都是函数。语法如下：

```
promiseObj = new WinJS.Promise(init, onCancel);
```

`init` 参数是可选的。`init` 函数在 promise 对象初始化或构造时被调用，它包含了 promise（在本例中为 promiseObj）将代表的工作的实现。这种实现可以是异步的或同步的，取决于任务的范围和性质。

> 这里需要注意的一点是，在 `init` 函数内部编写的代码默认并使其变为异步的。为了确保代码异步运行，我们必须使用异步 API，例如 Windows Runtime 异步 API、`setTimeout`、`setImmediate` 和 `requestAnimationFrame`。





此参数中使用的 `init` 函数接受以下参数：

-   completeDispatch: 当 `init` 内部的操作完成时，此参数将被调用，从而传递该操作的结果。`init` 代码应在操作完成后调用此项，并将操作结果作为参数传递。

-   errorDispatch: 当该操作发生错误且 promise 变为错误状态时，此参数将被调用。由于是错误，`errorDispatch` 的参数应该是 `WinJS.Promise.ErrorFromName` 的实例。

-   progressDispatch: 在操作处理过程中，此参数会被定期调用。该函数将包含一个中间结果。如果 promise 内部的操作由于需要支持进度报告，则使用此参数。

`onCancel` 参数是 Promise 构造函数的第二个参数。promise 的调用者可以使用此函数取消其任何未完成的工作。然而，在 WinJS 中，promise 并不提供或支持取消。

### 事件 (Events)

在 promise 对象成员类型的列表中，接下来是事件（Events）。目前，Promise 对象有一个名为 `onerror` 的事件。正如名称所示，该事件在处理 promise 过程中发生错误时触发。此外，每当任何 promise 抛出运行时错误时，无论该错误是否在其他地方被处理，此 `onerror` 事件都会触发。错误处理器可以辅助调试，可用于设置断点并提供错误日志。然而，归结底，它可以提供关于导致错误的代码或输入的见解和细节。此 `onerror` 事件提供了一种通用的错误处理机制。在代码中，添加一个通用的错误处理器如下所示：

```
WinJS.Promise.onerror = errorHandler;

function errorHandler(event) {
    // 获取通用错误处理信息
    var exc = event.detail.exception;
    var promiseErrored = event.detail.promise;
}
```

代码示例的第一行仅仅是将 `errorHandler` 函数附加到 promise 对象的错误事件上。接下来，我们定义 `errorHandler` 函数，它接受一个参数 `event`；在该示例中，函数的作用是从事件中获取信息，例如异常和 promise。然后，我们将这些值赋值给变量。参数 `event` 是 `CustomEvent` 类型的事件处理器参数；它通常是一个包含事件信息的对象。

### 方法 (Methods)

promise 对象的最后一个成员类型是方法（Methods），目前 WinJS.Promise 拥有以下方法：

-   addEventListener: 此方法简单地为 promise 附加一个事件监听器。它接受三个参数：`eventType`（事件的字符串名称）、`listener`（在事件触发时被调用的函数）以及 `capture`（用于启用或禁用捕获的布尔值）。此方法没有返回值，其基本语法如下：
`promise.addEventListener(eventType, listener, capture);`

-   removeEventListener: 此方法从控制中移除事件监听器。在语法上，它与 `addEventListener` 方法类似，如下所示代码所示：
`promise.removeEventListener(eventType, listener, capture);`

-   Cancel: 此方法尝试取消 promise。在 promise 支持取消且尚未完成的情况下，此方法将导致 promise 进入错误状态，其值为 `Error("Canceled")`。它没有参数也没有返回值。其基本语法如下：
`promise.cancel();`

-   dispatchEvent: 此方法简单地分发并触发一个指定类型和属性的事件。它接受两个参数，并返回一个布尔值，取决于是否在事件上调用了 `preventDefault`。此方法的参数类型为字符串值（包含事件名称）和 `eventDetails`（一个包含要附加到事件对象的额外属性集的对象）。此方法的基本语法如下：
`promise.dispatchEvent(type, eventDetails);`

## WinJS 中的 Promises

-   Then: 这是 promise 对象中最重要的方法。它接受三个 `function` 类型的参数：第一个函数允许我们指定 promise 完成后要执行的工作（promise 的值已完成）；第二个函数是在 promise 抛出错误未能完成值时将执行的错误处理；最后一个是处理过程中 promise 内部工作进度的处理。`then` 的返回值是一个 promise，其值是内部 `execute` 函数执行的结果。在基本形式下，`then` 方法将具有以下语法：`promise.then(onComplete, onError, onProgress);`

`then` 方法的三个参数类型均为 `function`。具体如下：
-   onComplete: 当 promise 成功完成并带有值完成时，将调用此处理器。该值将作为单个参数传递。`onComplete` 返回的值成为 `then` 返回的 promise 的完成值。如果在执行此函数期间发生错误或异常，`then` 返回的 promise 将进入错误状态。
-   onError: 当 promise 发生中断并带有错误完成时，将调用此处理器；`onError` 返回的值将成为 `then` 方法返回的 promise 的值。它不是像 `onComplete` 函数那样传递值，而是将错误作为参数传递。
-   onProgress: 当我们需要报告 promise 操作的进度时，使用此处理器。它有一个参数，即进度数据。注意，WinJS 中的 promise 并不强制支持进度。

-   `Done` 方法与 `Then` 一样，也允许我们指定 promise 完成时需要执行的内容、promise 失败时的错误处理以及沿途的进度报告。此外，此函数将抛出任何本作为值从 `then` 返回的错误。与返回 promise 的 `then` 不同，`Done` 不返回任何值。该方法的基本语法如下所示：
`promise.done(onComplete, onError, onProgress);`

`then` 和 `done` 之间存在一些差异，最明显的是返回值。如前所述，下列表总结了这些差异：`Then` 允许链式调用函数，因为它返回一个 promise。而在 `done` 中我们无法链式调用，因为它不返回值；具体来说，它返回 `undefined`。因此，`done` 必须是最后的调用。例如，我们可以拥有 `.then().then().then()` 等以此类推，而 `done` 止于 `.done()`。

如果没有为 `done` 提供错误处理器且发生了错误（换句话说，发生了未处理的异常），异常将抛出到事件循环，允许在 `window.onerror` 事件中捕获，但在 `try/catch` 块中不能。因此，该函数向调用者方法抛出任何在方法内部未处理的错误。而在 `then` 中，这些未处理的异常会被明智地捕获并作为 promise 状态的一部分，`then` 不抛出异常而是返回一个处于错误状态的 promise。了解这两个方法的区别对于使用至关重要。尽管如此，对于这两个方法，建议采用扁平的 promise 链而不是嵌套，因为 promise 链的格式使其更容易阅读和处理错误。例如，以下示例代码更优越：

```
asyncFunc()
  .then(function () { return asyncFunc1(); })
  .then(function () { return asyncFunc2(); })
  .done(function () { return theEnd(); });
```

而以下被标记为 `done` 的用法：

```javascript
// 不太整洁！
asyncFunc().then(function () {
  asyncFunc1().then(function () {
    asyncFunc2().done(function () { theEnd(); });
  })
});
```




请记住，WinJS 中的 Promise 符合 CommonJS Promises / A 提议中定义的 Promise，并且在编写本文时，WinJS Promise 尚未针对新的 Promises/A+ 规范进行测试。这对于 Windows 应用开发没有影响，因为应用运行在商店中。在浏览器中，WinJS Promise 与符合 A+ 规范的 Promise 之间可能出现的主要区别是，WinJS 不保证 Promise 的回调函数是异步的。例如，如果我们调用 `promise.then(a)` 且 `a` 为回调函数，我们无法确定 `a` 是以异步还是同步的方式被被调用的。而在 Promises/A+ 规范中，回调函数始终以异步方式被调用，这是必须的。规范解释说，不确保异步回调将使 Promise 变得难以理解和调试。尽管如此，正如我在本章早期提到的，WinJS 本身是开源并托管在 GitHub 上的，社区成员以及对此感兴趣的任何人都可以下载 WinJS，进行构建并针对 Promises/A+ 合规套件进行测试。

接下来，让我们看看如何在 Windows 应用开发中使用这些 WinJS Promise。

## 使用 WinJS Promise

我们在 Web 上利用 Promise 来使 UI 更具响应性，通过通过异步执行工作来避免阻塞 UI 线程。同样，我们使用 WinJS Promise 来异步处理工作，从而保持 Windows 应用的 UI 线程可用以响应用户输入。我们还允许应用布局和静态项目能够正常加载，同时在后台异步从服务器和数据库获取所需数据。为了这一目的，WinJS 和 Windows Runtime 中的异步 API 以 Promise 的形式在 JavaScript 中暴露出来。

让我们来看一个 Promise 的基础示例。为了遵循并复制以下示例，我们需要 Visual Studio（Express 版本即可）。我们首先需要创建一个 JavaScript 类型的基础应用。要实现这一点，我们需要从 Visual Studio 顶部菜单中进入 `File（文件） | New Project（新建项目）`，这将弹出一个包含项目类型的小窗口。在那里，我们需要进入 `JavaScript | Store Apps | Windows Apps`，这会列出所有不同的 JavaScript Windows 应用模板。对于此示例，我们可以选择 `Blank App（空白应用）`这是一个单页 Windows 应用项目，没有预定义的控件或布局。随心为应用命名并点击 Ok。接下来的截图说明了这些步骤：

# 第 5 章

![](img/04c7981ae2601bc5401805f632a22d49_53_0.png)

现在，我们有一个可以添加代码的空白 Windows 应用。为此，我们需要导航到 `default.html` 页面并对其进行修改。打开该页面，按照以下语法在 `body` 元素中插入一个 `input` 元素和一个 `div` 元素来显示结果：

```html
<body>
  <p>内容在此处</p>
  <br/>
  <div>
    <input id="urlInput" />
  </div>
  <br/>
  <div id="resultDiv">结果将在此显示</div>
</body>
```

接下来，我们需要为 `input` 元素添加更改处理程序添加代码，以便每当输入元素发生变化时我们都能执行某些工作。我们可以通过 `addEventListener` 方法作为 `WinJS.Utilities.ready` 函数的一部分来实现。在此函数内部添加此事件监听器，将允许我们绑定的处理程序在 DOM 通过 `DOMContentLoaded` 事件加载后直接被调用，而这反过来会在页面代码解析后所有资源加载之前触发。

## WinJS 中的 Promise

导航到位于 `js` 文件夹内的 `default.js` 文件。在那里，我们需要将以下代码添加到 `app.onactivated` 事件处理程序的末尾：

```javascript
WinJS.Utilities.ready(function () {
  var inp = document.getElementById("urlInput");
  inp.addEventListener("change", onChangeHandler);
}, false);
```

在之前的代码中，我们向 `WinJS.Utilities.ready` 添加了一段匿名函数代码。在那个匿名函数中，我们首先从 DOM 中获取该输入元素并将其赋值给名为 `inp` 的变量，然后在该输入变量上调用 `addEventListener` 方法，这会将名为 `onChangeHandler` 的函数添加到事件处理程序中。

最后一步将是为 `onChangeHandler` 函数编写代码。在那个函数中，我们将调用 `WinJS.xhr` 方法，它基本上封装了对 `XMLHttpRequest` 的调用并将其暴露为 Promise。我们可以使用此方法进行跨域请求和内网请求。然后，我们将用户在输入元素中输入的 URL 传递给 `xhr` 的参数，并相应地用结果更新 `resultDiv` 元素。`Xhr` 是一个返回 Promise 的异步函数；因此我们可以接受三个参数：成功、错误和进度来更新 UI。然后我们在该函数上调用 Promise 对象的方法或 `then` 方法，该方法会在 `xhr` 成功完成 `XMLHttpRequest` 或抛出错误时立即被调用。正如之前的定义所示。然而，对于这个基础示例，我们将查看如何添加 `onSubmit` 函数。此成功处理程序将通过将 `resultDiv` 的背景颜色设置为蓝色并将内部文本设置为“Hooray!”来应用一些更改。

`onChangeHandler` 函数的语法如下代码所示：

```javascript
function onChangeHandler(e) {
  var input = e.target;
  var resDiv = document.getElementById("resultDiv");

  WinJS.xhr({ url: e.target.value }).then(function
  onCompleted(result) {
    if (result.status === 200) {
      resDiv.style.backgroundColor = "blue";
      resDiv.innerText = "Hooray!";
    }
  })
```




## 整合应用 – 实战中的 Promises

在第 5 章“WinJS 中的 Promises”中，我们学习了 WinJS 库并详细了解了 WinJS promise 对象。我们还通过一个基础示例快速浏览了如何在 Windows 应用程序开发中使用 WinJS promises。最后，我们来到了最后一章，在这里我们将把全书中积累的关于 promises 的知识付诸实践。我们将尝试通过创建一个简单的实现来更深入地理解 promises 的工作原理。在创建实现库之后，我们将在一个基础示例中利用该库来执行异步操作。在本章中，我们将涵盖以下主题：

- 对到目前为止涵盖和学习的内容总结 - 在简单的 JavaScript 中创建一个 promise 实现

### 实现一个 promise 库

Promises 已经变得非常流行，从许多独立的实现中可以看出。此外，随着我们接近 ECMAScript 6 的发布，Promises/A+ 已经有超过 35 种符合规范的实现。需要注意的是，Promise/A+ 在 JavaScript 中日益增长的应用也反映在其他语言中，在 ActionScript、Python 和 Objective C 中都有许多实现。尽管在语义方面，由于语言能力的差异，这些实现可能不一定与 JavaScript 规范中的实现匹配，但最终可以通过直接测试 Promise/A+ 的 JavaScript 测试套件来验证其合规性。尽管如此，值得提到这些实现并展示所付出的努力。

## 整合应用 – 实战中的 Promises

让我们通过一个 promises 的基础实现代码示例；这将有助于我们更好地理解 promises 的工作原理。深入理解其运作方式可以提高我们利用代码的能力，并在代码出错时更容易、更快速地进行调试。我们将创建一个实现 promises 的极简 JavaScript 库，并从 promise 的状态开始编写该库的代码。当我们在第 2 章“Promise API 及其兼容性”中探索 Promise API 时，我们学到 promises 有三种不同的状态：pending（等待中）、fulfilled（已完成）和 rejected（已拒绝）。

promises 的规范没有为它们的状态指定值，因此让我们像下面的代码所示声明并为枚举器分配值：

```
var promState = {
  pending: 1,
  fulfilled: 2,
  rejected: 3
}
```

这个枚举允许我们通过名称调用状态，例如 `promState.fulfilled`。接下来，我们将创建一个对象，包含所有 promise 逻辑，从从状态之间的转换到 `then` 方法以及解析 promise。我们将此对象命名为 `PromiseMe`。

首先，我们需要定义 状态的变化及其从一个状态到另一个状态的转换。规范对状态之间的转换规定了一些规则和考虑，我们已经在第 2 章“Promise API 及其兼容性”中详细探讨了。这些规则可以总结如下：

- 一个 promise 在某一时刻只能处于一种状态
- 当 promise 从 pending 转换到任何其他状态（fulfilled 或 rejected）时，它不能回回
- 当 promise 成功时，它必须有一个值（即使可以是 undefined），当它失败时，它必须有一个理由（任何指定 promise 被拒绝的值）

在 `PromiseMe` 对象内部，我们首先将定义一个名为 `changeMyState` 的函数，用于处理和管理由上述代码控制的此 promise 状态之间的转换，如下：

```
var PromiseMe = {
  //设置默认状态
  myState: promState.pending,
  changeState: function(newState, newValue) {

    // 检查是否切换到相同状态并报告
    if (this.myState == newState) {
      throw new Error("Sorry, But you can't do this to me! You are transitioning to same state: " + newState);
    }

    // 尝试跳出 fulfilled 或 rejected 状态
    if (this.myState == promState.fulfilled ||
        this.myState == promState.rejected) {
      throw new Error("You can't leave this state now: " + this.myState);
    }
    // 如果 promise 因空原因被拒绝
    if (newState == promState.rejected &&
        newValue === null) {
      throw new Error("If you get rejected there must be a reason. can't be null!");
    }

    // 如果 fulfilled 时没有传递任何值
    if (newState == promState.fulfilled &&
        arguments.length < 2) {
      throw new Error("I am sorry but you must have a non-null value to proceed to fulfilled!");
    }

    // 我们通过了所有条件，现在可以更改状态
    this.myState = newState;
    this.value = newValue;
    return this.myState;
  }
};
```

对象内部的代码首先会通过 `myState: promState.pending` 将名为 `myState` 的属性设置为枚举 `promState` 的 `pending` 值。之后，我们将名为 `changeState` 的属性设置为一个接收两个参数（`newState` 和 `value`）的匿名函数。在该函数内部，我们处理状态转换并检查它是否符合规则。在继续执行代码之前，我们有四个检查点：

- 1. 首先，我们检查是否正在转换到相同状态并抛出错误。
- 2. 在第二次检查中，我们确保 promise 不尝试从 rejected 或 fulfilled 状态转换，并相应抛出错误。
- 3. 第三次检查是针对拒绝时传递的值。如果是 null，将抛出错误，这确保了 promise 被除 null 以外的值拒绝。
- 4. 最后一次检查：我们确保对于 fulfilled 状态，提供了一个非空值。

### 实现 then 方法

我们实现中的下一步是 `then` 方法。这是 promises 的核心支柱，也是它们变得实用的原因。让我们如下所示定义 `then` 方法：

```
then: function (onFulfilled, onRejected) {
  // 定义一个数组
  this.handlers = this.handlers || [];
  // 创建一个 promise
  var returnedPromise = Object.create(Promise);

  this.handlers.push({
    fulfillPromise: onFulfilled,
    rejectPromise: onRejected,
    promise: returnedPromise
  });

  return returnedPromise;
}
```

你可能注意到 `handlers` 数组包含两个属性：`fulfillPromise` 和 `rejectPromise`。这是两个函数，被设置为在 `then` 方法参数中传递的处理器。让我们定义这两个函数，以便我们可以在 `resolve` 方法中使用它们。这些函数是辅助方法，仅允许我们手动更改 promise 的状态。

```javascript
fulfillPromise: function (value) {
  //将状态更改为 fulfilled 并返回一个带有值的 promise
  this.changeState(promState.fulfilled, value);
}
rejectPromise: function (reason) {
  //将状态更改为 rejected 并返回一个带有原因的拒绝 promise
  this.changeState(promState.rejected, reason);
}
```

### 定义 resolve 方法

接下来，我们需要处理解析 promise。我们需要定义一个 `resolve` 方法来处理该 promise，并根据 promise 的状态将其解析或拒绝。你可以将 `resolve` 方法视为 promise 调用的内部方法，旨在仅当 promise 成功时执行 `then` 调用。实际上，为了解析或拒绝 promise，你需要调用的函数在我们的情况下是 `changeMyState`。让我们按照下面的代码开始为 `resolve` 方法创建基础逻辑：

```javascript
resolve: function () {
  // 检查是否为 pending 且存在
```





# 汇总一切 – 实践中的 Promise

```javascript
if (this.myState == promState.pending) {
  return false;
}
```

之前的代码将 `resolve` 属性赋值为一个函数。在该函数内部，我们首先检查该 Promise 的状态。如果它是 `pending`（待定中），我们返回 `false`。接下来的代码将遍历包含我们在方法中定义的处理器的数组：

```javascript
// 只要 handlers 数组包含项，就循环每一个 then
while(this.handlers.length) {
```

```javascript
// 返回并移除数组中的第一个项
var handler = this.handlers.shift();
```

在循环内部，我们对数组应用了 `shift()` 函数。`shift()` 函数允许我们从数组中获取第一个项并直接将其删除。因此，`handler` 变量将包含 `handlers` 数组中的第一个项，反之，`handlers` 数组将包含除当前存储在 `var handler` 中的项之外的所有的所有项。

接，在 `resolve` 函数中，我们将定义一个名为 `doResolve` 的变量，根据以下代码所示的状态，将其设置为 `fulfillPromise` 函数或 `rejectPromise` 处理器的值之一：

```javascript
// 根据当前状态设置函数
var doResolve = (this.myState == promState.fulfilled) ?
handler.fulfillPromise : handler.rejectPromise;
```

> 前述语法使用了三元运算符。它被称为三元运算符，与其他所有运算符不同的是，该运算符要求在运算符中间放置第三个值。它类似于 `if` 语句的简写替代方案，如下例所示，`if` 和 `else` 子句为同一个变量分配不同的值：
  if (condition == true)
    result = "pick me"
  else
    result = "No! pick me instead";

三元运算符将 `if` 语句转换为以下单行条件语句：
result = (condition == true) ? "pick me" : "No! pick me instead";

![](img/04c7981ae2601bc5401805f632a22d49_62_0.png)

我们需要为 `doResolve` 函数添加一些健全性检查。如果它不是函数类型或者该函数不存在，我们就调用 Promise 上的 `changeMyState` 方法，以便传递状态和值：

```javascript
// 如果 doResolve 不是函数
if (typeof doResolve != 'function') {
  handler.promise.changeMyState(this.myState, this.value);
}
```

## 实现 doResolve 函数

此代码的另一种路径是 `doResolve` 函数存在，并且我们需要返回一个带有值的 Promise 或用错误拒绝它。因此，我们按照如下代码所示，在 `if` 语句之后紧跟一个 `else` 语句来实现这种情况：

```javascript
else {
  //用值完成 Promise 或用错误拒绝
try {
```

根据所看到的代码逻辑，我们现在拥有 `doResolve` 包含了 `handler.fulfillPromise` 或 `handler.rejectPromise` 函数。这两个函数可以手动更改 Promise 的状态并接受一个参数，即当前的值或当前的原因。这两个值都包含在 `this.value` 变量。在这里，我们将当前值传递给 `doResolve`，并按照如下行代码将结果赋值给名为 `promiseValue` 的变量：

```javascript
var promiseValue = doResolve(this.value);
```

接下来，我们需要管理通过 `promiseValue` 返回的 Promise。首先，我们按照如下代码检查 Promise 是否存在以及是否为有效的 `then` 函数：

```javascript
// 处理返回的 promise
if (promiseValue && typeof promiseValue.then ==
  'function') {
```

假设该条件成立，在内部我们现在对 `promiseValue` 调用 `then` 方法，因为现在现在包含一个作为 `doResolve` 函数执行结果的 Promise。我们将向其 `then` 方法传递两个参数：一个用于 `onFullfilled` 的函数参数，另一个用于 `onRejected` 的参数，如下代码所示：

```javascript
// 在 promise 上调用 then
promiseValue.then(function (val) {
  handler.promise.changeMyState(
    promState.fulfilled, val);
}, function (error) {
```

```javascript
handler.promise.changeState(
  promState.rejected, error);
}}
```

另一方面，如果 `promiseValue` 返回的值不是一个 Promise，我们不需要调用 `then` 方法。相反，我们简单地将状态更改为 `fulfilled`（已完成）并传递该值。我们将按照如下所示在 `else` 语句处理这种情况：

```javascript
// 如果返回的值不是 promise
else {
  handler.promise.changeState(promState.fulfilled, promiseValue);
}
```

最后，由于我们处于 `try` 语句中，我们需要相应提供一个 `catch` 语句，其中我们将处理操作失败时抛出的任何错误。在该 `catch` 语句中，我们将 Promise 的状态更改为 `rejected`（已拒绝）并传递产生的错误。我们还会关闭所有的尾括号：

```javascript
// 处理错误
catch (error) {
  handler.promise.changeState(promState.rejected, error);
}
```

解析 Promise 包含一些繁琐的检查，但这些对于保证 Promise 实现相对于规范的保真度是必要的。正如你所看到的，我们在执行过程中添加了逻辑，从一个简单的检查开始，查看我们是否正在根据 Promise 状态运行 `onFfilled` 或 `onRejected` 函数。之后，我们根据返回值更改它们对应的 Promise 状态。

> 请记住，实现需要遵守现有的考虑因素和规则。





```javascript
// 定义一个名为 handlers 的数组
this.handlers = this.handlers || [];
// 创建一个 promise 对象
var returnedPromise = Object.create(PromiseMe);
var that = this;
setTimeout(function () {
    this.handlers.push({
        fulfillPromise: onFilled,
        rejectPromise: onRejected,
        promise: returnedPromise
    });
    that.resolve();
}, 2);
```

return returnedPromise;

```javascript
resolve: function () {
    // 检查是否处于等待状态
    if (this.myState == promState.pending) {
        return false;
    }
    // 遍历 handlers 数组，只要数组不为空
    while (this.handlers && this.handlers.length) {
        // 返回并移除数组中的第一个项
        var handler = this.handlers.shift();
    }
    // 根据当前状态设置函数
    var doResolve = (this.myState == promState.fulfilled ? handler.fulfillPromise :
        handler.rejectPromise);
    // 如果 doResolve 不是函数
    if (typeof doResolve != 'function') {
        handler.promise.changeMyState(this.myState,
        this.value);
    } else {
        // 使用值完成 promise 或拒绝 promise
        try {
            var promiseValue = doResolve(this.value);
        }
        // 处理返回的 promise
        if (promiseValue && typeof promiseValue.then == 'function') {
```

## 整合到一起 – Promises 的实际应用

```javascript
promiseValue.then(function (val) {
  handler.promise.changeState(
    promState.fulfilled, val);
  }, function (error) {
    handler.promise.changeState(
      promState.rejected, error);
  });
  // 如果返回的值不是一个
  // promise 
} else {
  handler.promise.changeState(
    promState.fulfilled, promiseValue);
  }
  // 处理抛出的错误
} catch (error) {
  handler.promise.changeState(
    promState.rejected, error);
  }
}
};
return Object.create(PromiseMe);
```

之前的代码代表了一个小型 JavaScript 库中基础的 promise 实现。它实现了一个带有 `then` 方法的 promise 对象，考虑了如何完成和拒绝 promise 的规范要求，同时处理了避免实现中出现异常的必要检查。我们可以使用这个库并开始调用它的 Promise 对象及其相应的函数，即 `fulfillPromise` 和 `rejectPromise`，来实现一些异步操作。

> 该实现是基础的；我们可以对其进行扩展，包含许多可以构建在 Promises API 之上的功能和方法。此外，我们可以构建此实现，并针对 Promises/A+ 符合性测试套件对其进行测试，可以通过此链接找到：https://github.com/promises-aplus/promises-tests。

在前面的信息框提供的链接中，我们可以找到完成测试的步骤，这些测试需要在 Node.js 环境中运行，并且我们需要确保已经安装了 Node.js。

## 让 promise 运行

我们可以利用刚刚编写的这个基础 promise 实现，并在代码中使用它来处理异步操作。让我们来看一个使用这个 PromiseMe 库的示例。以下代码可以添加在 PromiseMe 对象的代码之后：

```javascript
var multiplyAsync = function (val) {
  var promise = new PromiseMe();
  promise.fulfillPromise(val * 2);

  return promise;
};

multiplyAsync(2)
  .then(function (value) {
    alert(value);
  });
```

我们在之前的代码中做的仅仅是将一个函数赋值给名为 `multiplyAsync` 的变量，该变量反过来实例化了 `PromiseMe`，然后对创建的 promise 变量调用了 `fulfillPromise` 方法，该变量是 `PromiseMe` 对象的一个实例。`fulfillPromise` 方法的作用仅仅是将 `val` 参数乘以数字 2。随后，我们调用 `multiplyAsync`并将数字 2 作为其参数的值传递进去；由于它返回一个 promise，因此我们可以在它上调用 `then` 方法。`then` 方法有一个处理器，它处理成功情况并简单地弹出一个显示应该是 4 的值的警框。

在 HTML 页面中运行脚本，我们应该会看到一个显示数字 4 的警框。

> 你可以在 jsFiddle 上找到完整代码并测试：http://jsfiddle.net/Ramasieradienne/g8oj4guo/
确保浏览器支持 promises。

让我们为这段代码添加一些错误处理。首先，为了简单和易读，我将创建一个名为 `alertResult` 的函数来替换 `alert(value)`。

因此，我们将拥有如下函数：

```javascript
var alertResult = function (value) {
  alert(value);
};
```

## 整合在一起 – Promises 的实际应用

我们将添加另一个名为 `onError` 的函数，它基本上是显示传递给它的错误信息的警框。该函数将具有以下语法：

```javascript
var onError = function(errorMsg) {
  alert(errorMsg);
};
```

现在，让我们添加一个通过检测异常并拒绝 promise 来包含错误处理的函数。以下代码展示了：

```javascript
var divideAsync = function (val) {
  var promise2 = new PromiseMe();
    if (val == 0) {
      promise2.rejectPromise("cannot divide by zero");
    }else {
      promise2.fulfillPromise(1 / val);
    }
  return promise2;
}
```

之前的代码简单的是检查是否为零；如果是零，它拒绝 promise；否则，它完成 promise。为了测试这一点，我们将调用 `divideAsync`。代码如下：

```javascript
divideAsync(0)
  .then(alertResult)
  .catch(onError);
```

最终结果将是“不能除以零”的错误信息。

![img/04c798ae2601bc540180f632a22970](img/04c798ae2601bc540180f632a22970)

## 总结

在本书之前的章节中，我们学习了大量关于 promises 的知识。我们从 JavaScript 异步编程开始，回顾 promises 的现状，期间详细讨论了为什么现在应该关注 promises。接下来，我们深入研究了 Promises API 以及对其 `then` 方法的彻底描述。之后，我们学习了支持 promises 的浏览器以及实现 promises 的库，并详细解释了我们如何实现以及使用 promise 链来实现异步操作。我们的第三站是错误处理，这是 promises 最重要的方面之一。我们回过头来看 JavaScript 中的异常以及它们在 promises 中是如何处理的。我们还学习了作为处理错误一部分的 `catch` 方法。

Promises 现在有了 JavaScript 的原生支持，这是我们在 Web 和客户端开发领域利用这项技术的关键时期。随着时间的推移，更多的浏览器将采用 promises 作为标准并使其成为浏览器原生。





# 索引

# A
- addEventListener 方法 49
- 异步 JavaScript 和 XML (AJAX) 6
- 异步编程 6-9
- doResolve 函数
- 实现 63, 64

# E
- errorDispatch 参数 48
- errorFromName 对象 46
- 使用 promises 进行处理 40-43
- 事件，WinJS.Promise 对象 48, 49
- 异常
  - 与 promises 37-39

# B
- 浏览器兼容性 24, 25
- 浏览器支持 23

# C
- 回调地狱 28
- 回调 13-15
- cancel 方法 49
- catch() 函数 40, 42
- 链式
  - 关于 27, 28
  - 顺序执行 33, 34
  - promises 27, 30-32
- completeDispatch 参数 48
- 合规性测试
  - 关于 23
  - URL 23
- 构造函数，WinJS.Promise 对象 47

# F
- 函数，WinJS
  - log 函数 46
  - strictProcessing 函数 47
  - xhr 函数 47

# I
- init 函数，参数
  - completeDispatch 48
  - errorDispatch 48
  - progressDispatch 48

# D
- Deferred
  - 关于 16
  - URL 26
- disdispatchEvent 方法 49
- done 方法
  - 关于 50
  - 与 then 方法的差异 51

# J
- JavaScript
  - 异步编程 6-9
  - jsFiddle
    - URL 69, 70

# L
- 库，promises
  - 关于 25, 26
  - Q.js 25
  - RSVP.js 25
  - when.js 25
  - log 函数 46
- promises
  - 关于 12, 29, 45, 57
  - 与异常 37-39
  - 链式 30-32
  - 特性 14
  - 代码，封装 65, 68
  - 定义 11
  - 错误处理 40-43
  - 已完成状态 (fulfilled state) 11
  - 实现 58-70
  - 在 WinJS 中 45
  - 库 25, 26
  - onFulfilled 参数 11
  - onRejected 参数 11
  - 等待状态 (pending state) 11
  - 拒绝状态 (rejected state) 11

# M
- 方法，WinJS.Promise 对象
  - addEventListener 方法 49
  - cancel 方法 49
  - dispatchEvent 方法 49
  - removeEventListener 方法 49
  - then 方法 50
- Promises/A+ Compliance测试套件
- Promises/A 规范
  - 与 Promises/A+ 的区别
  - 规范 18, 19
- Promises/A 规范
  - 关于 18
  - 与 Promises/A 的区别
  - 规范 18, 19
  - 缺失 18
  - URL 18

# O
- object.addEventListener() 方法 8
- object，WinJS
  - ErrorFrom 对象 46
  - promise 对象 46
  - onComplete 处理器 50
  - 非错误处理器 50
  - onProgress 处理器 50
  - onRejected 参数 39

# P
- polyfill (垫片)
  - 关于 24
  - 下载的 URL 24
- progressDispatch 参数 48
- Promise API 18-23
- promise 库，实现
  - 关于 57-60
  - doResolve 方法，实现 63, 64
  - resolve 方法 61-63
  - then 方法，实现 60, 61
- promise 对象 46
- promise polyfill 库
  - 关于 26
  - URL 26
- Promise Resolution Procedure. 参见 PRP
- 属性，WinJS
  - 验证属性 (validation property) 46

# Q
- Q.js
  - 关于 25
  - 下载的 URL 25

# R
- 拒绝状态 (rejected state)
  - 要求的 38
- removeEventListener 方法 49
- resolve 方法 61-63
- RSVP.js
  - 关于 25
  - 下载的 URL 25

# S
- shift() 函数 62
- strictProcessing 函数 47
- 同步函数
  - 特性 27

# W
- when.js
  - 关于 25
  - 下载的 URL 25
- Windows JavaScript 库 (WinJS)
  - 关于 45
  - 特性 45, 46
  - 函数 46
  - 现场演示，URL 56
  - 对象 46
  - 在 GitHub 上，URL 46
  - promises 45
  - 使用 promises 52-56
  - 属性 46

# T
- then() 函数 24
- then 方法
  - 关于 19, 20, 25, 50
  - 与 done 方法的差异 51
  - 参数 50
  - 实现 60, 61
  - onFulfilled 参数 20
  - onRejected 参数 20
  - URL 25
- then 方法，参数
  - onComplete 处理器 50
  - 非错误处理器 50
  - onProgress 处理器 50
- WinJS.Promise 对象
  - 关于 47
  - 构造函数 47, 48
  - 事件 48
  - 方法 49
  - 使用 52-56
# V

- 验证属性 (validation property) 46

# XMLHttpRequest API 6
- xhr 函数 47

