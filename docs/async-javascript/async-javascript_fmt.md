
# 异步 JavaScript

## 对 `Async JavaScript` 的早期赞誉

> `Async JavaScript` 是我所见过的第一本专注于当今 JavaScript 开发关键主题的完整著作：如何在不发疯的情况下处理并发和并发任务！为了您的理智，请阅读此书。
>
> **➤ Peter Cooper**，JavaScript Weekly 主编

Trevor 提供了一份关于编写异步 JavaScript 的简明指南，在浏览器端和服务器端示例之间取得了完美平衡。既是指南，又是概述，引人入胜，这本书是任何希望提升水平的 JavaScript 开发者的必读之作。

**➤ Wynn Netherland**，The Changelog 联合创始人

这是一本关于 JavaScript 异步领域的完整指南。本书涵盖的概念和工具对于任何希望构建完整、结构良好且高效的 JavaScript 应用程序的人来说都是必不可少的。

> **➤ Julien Biezemans**，Ruby/JavaScript 开发者，Cucumber.js 作者

无论原因如何，JavaScript 都已经扎根于此。Apple 通过 WebKit 和 Safari 支持 JavaScript。微软通过 Metro 支持 JavaScript。甚至 Adobe 也在支持 JavaScript，推出了将 Flash 转换为 HTML5 的工具。这个最初只是 humble 浏览器功能的东西，如今已成为 arguably 世界上最重要的编程语言。

得益于浏览器的普及，JavaScript 比其他任何语言都更接近实现 Java 曾经承诺的“编写一次，到处运行”。2007 年，Jeff Atwood 提出了 `Atwood 定律`：

> 任何可以用 JavaScript 编写的应用，最终都将用 JavaScript 编写。³

## 天堂里的麻烦

JavaScript 从一开始就被设计为单线程语言，异步任务通过事件来处理。当只有少数几个潜在事件时，基于事件的代码比多线程代码简单得多。它在概念上非常优雅，而且消除了将数据包装在互斥锁和信号量中以实现线程安全的需要。但当一个事件需要携带状态从一个事件传递到下一个事件时，这种简洁性往往会让位于一种如此可怕以至于被称为 `Pyramid of Doom` 的代码结构。

```javascript
step1(function(result1) {
  step2(function(result2) {
    step3(function(result3) {
      // and so on...
    });
  });
});
```

“我爱异步，但我不能这样写代码，”一位开发者在 Node.js Google Group 上 famously 抱怨道。⁴ 但问题并不在于语言本身，而在于程序员使用语言的方式。用优雅的方式处理复杂的事件组合在 JavaScript 中仍然是前沿领域。

所以，让我们推动这个前沿前进吧！让我们向世界证明，即使是最复杂的问题，也可以用干净、可维护的 JavaScript 代码来解决。

³ http://www.codinghorror.com/blog/2007/07/the-principle-of-least-power.html

⁴ https://groups.google.com/forum/#!topic/nodejs/wzSUdkPICWg

## 这本书适合谁？

这本书面向中级 JavaScript 开发者。你应该了解变量的作用域范围。像 `typeof`、`arguments` 和 `this` 这样的关键字不应该让你感到困惑。或许最重要的是，你应该理解

```javascript
func(function(arg) { return next(arg); });
```

只是

```javascript
func(next);
```

的一种 needless 冗长写法，除了极少数情况。（有关小型但重要的函数式习语的更多示例，请参阅 Reg Braithwaite 的优秀文章《Captain Obvious on JavaScript》。）

你*不需要*知道的是 JavaScript 中异步事件是如何调度的。我们将在下一章中介绍这一点。

## JavaScript 学习资源

随着 JavaScript 成为 Web（更不用说移动设备）的 `lingua franca`，大量关于它的信息性书籍、课程和网站纷纷出现。以下是我推荐的一些：

- 如果你完全是编程新手，请查看交互式教程网站 Codecademy。
- 如果你来自其他语言，希望快速上手 JavaScript 作为浏览器脚本语言，可以在 CodeSchool 上学习交互式 jQuery Air 课程。
- 如果你想更正式地了解 JavaScript 语言，请研读 Marijn Haverbeke 的 `Eloquent JavaScript`。
- 如果你是希望提升水平并避免常见陷阱的 JavaScript 初学者，请花些时间阅读 JavaScript Garden。

## 在哪里寻求帮助？

当思考“我应该在这里使用 `typeof` 还是 `instanceof`？”这样的问题时，请避开过时的 W3Schools 网站（遗憾的是，Google 搜索往往倾向于推荐它）。相反，请前往 Mozilla Developer Network (MDN)。

Mozilla 基金会（你可能听说过它的浏览器，Firefox）由 Brendan Eich 领导，他是 JavaScript 的创始人。这个基金会精通其领域。

如果你在 MDN 的页面中找不到答案，请将你的问题带到 Stack Overflow。¹¹ 该网站培养了一个 amazingly 乐于助人的开发者社区，可以安全地打赌，任何标记为 JavaScript 的 coherent 问题都会得到准时的回应。

## 运行代码示例

这本书有点不寻常，因为我同时讨论了客户端（浏览器）和服务器端（Node.js）代码。这反映了 JavaScript 独特的可移植性。核心概念适用于所有 JavaScript 环境，但某些示例针对其中一种或另一种。

即使你对编写 Node 应用没有兴趣，我也希望你能按照说明在本地运行这些代码片段。请参阅第 xiv 页的“在 Node.js 中运行代码”获取指导。

## 哪些示例是可运行的？

当你看到一个带有文件名的代码片段时，这意味着它是独立的，可以直接运行而无需修改。下面是一个例子：

```javascript
Preface/stringConstructor.js
console.log('str'.constructor.name);
```

周围的上下文应该能清楚地说明代码是在浏览器、Node.js 还是两者中都可以运行。

当代码片段没有文件名时，这意味着它不是独立的。它可能是 larger 示例的一部分，也可能是假设性的。下面是一个例子：

```javascript
var tenSeconds = 10 * 1e3;
setTimeout(launchSatellite, tenSeconds);
```

这些示例是用来阅读的，不是用来运行的。

## 在 Node.js 中运行代码

Node 非常易于安装和使用：只需访问 `http://nodejs.org/`，点击下载，然后运行 Windows 或 OS X 安装程序（或在 `*nix` 上从源代码构建）。然后你可以在命令行中运行 `node` 来打开一个 JavaScript REPL（类似于 Ruby 的 `irb` 环境）。

```bash
$ node
> Math.pow(5, 6)
15625
```

你可以通过将 JavaScript 文件名作为参数传递给 `node` 命令来运行它。

```bash
$ echo "console.log(typeof NaN)" > foo.js
$ node foo.js
number
```

## 在浏览器中运行代码

每个现代浏览器都提供了一个 nice 的小 REPL，让你可以在当前页面的上下文中运行 JavaScript 代码。但对于多行代码示例，你最好使用像 jsFiddle 这样的 web 沙箱。¹²

使用 jsFiddle，你可以输入 JavaScript、HTML 和 CSS，然后点击运行（或按 Ctrl+Enter）查看结果。（控制台输出将显示在你的开发者控制台中。）你可以通过左侧边栏选择 jQuery 等框架。你还可以保存你的工作，从而获得一个可共享的 URL。

## 本书中的代码风格

JavaScript 没有官方的风格指南，但在一个项目中保持一致的风格很重要。对于这本书，我采用了以下（非常常见的）约定：

- 两空格缩进
- camelCase 标识符
- 在每个表达式的末尾使用分号，除了函数定义

更专业地说，我采用了一种特殊的约定来处理函数调用链中的缩进，这是基于 Reg Braithwaite 的提议。规则本质上是这样的：链中的两个函数调用具有相同的缩进级别，当且仅当它们返回相同的对象。所以，例如，我可能会写如下代码：

```javascript
$('#container > ul li.inactive')
  .slideUp();
```

jQuery 的 `slideUp` 方法返回调用它的同一对象。因此，它没有缩进。相比之下：

```javascript
var $paragraphClone = $('p:last')
  .clone();
```

这里，`clone` 方法是缩进的，因为它返回一个不同的对象。

这种约定的优点是它阐明了链中每个函数的返回值。这里是一个更复杂的例子：

```javascript
$('h1')
    .first()
    .addClass('first')
.end()
    .last()
    .addClass('last');
```

jQuery 的 `first` 和 `last` 将集合过滤到其第一个和最后一个元素，而 `end`

撤销上一个过滤器。所以，`end` 没有缩进，因为它返回的值与

`$('h1')` 相同。（`last` 被允许与 `first` 占据相同的缩进级别，因为

链被重置了。）

当我们进行函数式编程时，这种缩进方法尤其有用，

正如我们将在第 47 页的第 4 章《使用 `Async.js` 进行流程控制》中将看到的。

```javascript
[1, 2, 3, 4, 5]
    .filter(function(int) { return int % 2 === 1; })
        .forEach(function(odd) { console.log(odd); })
```

## 关于 `altJS` 的一点说明

许多语言可以编译为 JavaScript，使代码更容易编写。

（你可以在 `http://altjs.org` 找到一个相当全面的列表。）这本书不是关于

它们的。它是关于在不使用预编译器的情况下编写最好的 JavaScript 代码。我没有什么反对 `altJS` 的（见下一节），但我相信

理解底层语言很重要。

一些 `altJS` 语言专门旨在通过允许以

更同步的风格编写来“驯服”异步回调。我在附录 1《驯服 JavaScript 的工具》第 81 页中包含了这些语言的概述。

## CoffeeScript

我 ♥ CoffeeScript 已经不是什么秘密了，这是一种美丽而富有表现力的语言，

编译为 JavaScript。我在 HubSpot 的日常工作中广泛使用它。

我曾在 Railsconf 和 Øredev 等会议上做过关于它的演讲。而且它是

我的第一本书 `CoffeeScript: Accelerated JavaScript Development` 的主题。¹³

¹³ http://pragprog.com/book/tbcoffee/coffeescript

¹¹ http://stackoverflow.com/

¹² （根据上下文暗示的参考文献）

但当我开始撰写你正在阅读的这本书时，我决定使用 `CoffeeScript` 编写会不必要地限制它的吸引力。总的来说，`CoffeeScript` 用户非常精通 JavaScript，而像 `square = (x) => x * x` 这样的代码对 JavaScript 纯粹主义者来说可能如同象形文字。¹⁴

所以，如果你是一位 `CoffeeScript` 用户，对于花括号的使用，我深表歉意。请放心，你从这本书中获得的经验教训将适用于任何替代 JavaScript 的语言。

## 本书资源

本书的网站地址是 `[http://pragprog.com/book/tbajs/async-javascript](http://pragprog.com/book/tbajs/async-javascript)`。在那里，你可以下载书中使用的示例代码，获取最新信息，并在一个友好的论坛中提出与本书相关的问题。

对于更通用的 JavaScript 相关问题，我（再次）真诚地推荐 `Stack Overflow`。¹⁵ 我与该网站没有关联，但我是一名热心的粉丝，拥有令人自豪的 23,000 个声望点（且还在增长）。在那里，表述清晰、格式规范的问题几乎总能迅速得到解答。

最后，如果你想直接联系我，可以通过 `trevorburnham@gmail.com` 或 Twitter：`@trevorburnham` 联系我。我总是很高兴收到读者的来信。

介绍到此为止。让我们开始异步之旅吧！

14. 然而，可能不会持续太久：`[http://wiki.ecmascript.org/doku.php?id=harmony:arrow_function_syntax](http://wiki.ecmascript.org/doku.php?id=harmony:arrow_function_syntax)`。

15. `[http://stackoverflow.com/](http://stackoverflow.com/)`

## 第 1 章

# 理解 JavaScript 事件

事件。它们*到底*是如何工作的？关于 JavaScript 异步事件模型的困惑与 JavaScript 本身一样古老。困惑导致错误，错误引发愤怒，而尤达大师告诉了我们剩下的道理....

然而在本质上，JavaScript 事件既概念优雅又实用。一旦你接受了这门语言的单线程设计，它感觉就像是一个特性而非限制。这意味着你的代码是不可中断的，并且你安排的事件会有序地排队。

在本章中，我们将浏览 JavaScript 的异步机制，并消除一些常见的误解。我们将看看 `setTimeout` *真正* 做了什么。然后我们将讨论在回调中处理错误。最后，我们将确立本书的主题：组织异步代码以提高清晰度和可维护性。

## 1.1 安排事件

在 JavaScript 中，当我们想让一段代码在未来某个时间运行时，会将其放入一个*回调*中。回调只是一个普通函数，只不过它被传递给像 `setTimeout` 这样的函数，或者被绑定为像 `document.onready` 这样的属性。当回调运行时，我们说一个事件（例如，超时到期或文档准备就绪）被触发了。

当然，细节决定成败，即使对于 `setTimeout` 这样看似简单的东西也是如此。对 `setTimeout` 的一个常见描述是这样的：

> 给定一个回调和 *n* 毫秒的延迟，`setTimeout` 会在 *n* 毫秒后运行该回调。

但正如我们将在本节以及整个本章中看到的，这个描述存在严重缺陷。在大多数情况下，它只是近似正确。在其他情况下，它完全错误。要真正理解 `setTimeout`，我们必须理解整个 JavaScript 事件模型。

### 现在还是以后？

为了开始我们对 `setTimeout` 的探索，让我们看一个简单例子，它经常让 JavaScript 新手感到困惑，特别是那些来自 Java 和 Ruby 等多线程语言的开发者。

```javascript
EventModel/loopWithTimeout.js
for (var i = 1; i <= 3; i++) {
  setTimeout(function() { console.log(i); }, 0);
};
```

4

4

4

大多数语言新手会期望循环输出 1, 2, 3，或者也许是这三个数字的某种组合，因为三个超时（每个都安排在 0 毫秒后触发）竞相首先触发。

要理解为什么输出是 4, 4, 4 而不是预期的结果，你需要知道三件事。

- 只有一个名为 `i` 的变量，其作用域由声明 `var i` 决定（顺便说一句，它的作用域不是在循环内，而是在包含该循环的最近函数内）。
- 循环结束后，`i===4`，因为在循环条件 `i<=3` 失败之前它一直在递增。
- JavaScript 事件处理程序在主线程空闲之前不会运行。

前两个概念属于 JavaScript 入门知识，但第三个则更令人惊讶。当我刚开始使用 JavaScript 时，我对此并不完全相信。Java 训练我担心我的代码可能随时被中断。数以百万计的潜在边缘情况让我充满焦虑，我想：“如果在这两行代码之间发生了一个罕见事件怎么办？”

然后有一天，这个负担从我身上卸下了....

### 阻塞线程

这段代码彻底改变了我对 JavaScript 事件的先入之见：

```javascript
EventModel/loopBlockingTimeout.js
var start = new Date;
setTimeout(function(){
  var end = new Date;
  console.log('Time elapsed:', end - start, 'ms');
}, 500);
while (new Date - start < 1000) {};
```

在我多线程的思维模式中，我原本期望定时函数在 500 毫秒后运行。但这需要设计为持续整整一秒的循环被中断。然而，如果你运行这段代码，你会得到类似这样的输出：

```text
< Time elapsed: 1002ms
```

你可能会得到一个略有不同的数字；遗憾的是，`setTimeout` 和 `setInterval` 的精确度远不如你希望的那样（参见 *第 5 页的“定时函数”*）。但它肯定会至少是 1000 毫秒，因为 `setTimeout` 的回调在 `while` 循环运行完成之前无法触发。

那么，如果 `setTimeout` 没有使用另一个线程，它到底在做什么呢？

#### 认识队列

当我们调用 `setTimeout` 时，一个超时事件被*排入队列*。然后执行继续：`setTimeout` 调用之后的那一行会运行，再之后的那一行也会运行，依此类推，直到没有更多行。只有那时 JavaScript 虚拟机才会问：“队列上有什么事件？”



### 1.1 事件队列与事件循环

如果队列上至少有一个有资格“触发”的事件（比如一个设置于1000毫秒前的500毫秒超时事件），虚拟机将选择一个并调用其[处理程序](#)（例如，我们传递给`setTimeout`的函数）。当处理程序返回后，我们又回到队列。

输入事件的工作方式相同：当用户点击一个附加了点击处理程序的DOM元素时，一个点击事件会被排入队列。但处理程序不会被执行，直到所有当前运行的代码完成（并且可能是在其他事件完成之后）。这就是为什么不谨慎使用JavaScript的网页往往变得无响应的原因。

你有时可能会听到*事件循环*这个术语，它描述了队列的工作原理。就好像你的代码是从一个看起来像这样的循环中运行的：

```javascript
runYourScript();
while (atLeastOneEventIsQueued) {
  fireNextQueuedEvent();
};
```

由此产生的一个结果是，每个触发的事件都将成为堆栈跟踪的根源。我们将在[第1.4节，处理异步错误，第12页](#)了解更多相关内容。

JavaScript中事件调度的简便性是这门语言最强大的特性之一。像`setTimeout`这样的异步函数使得延迟执行变得简单，而无需生成线程。JavaScript代码永远不会被中断，因为事件只能在代码运行时排队；它们不能在代码完成之前*触发*。

在下一节中，我们将更仔细地了解异步JavaScript的构建块。

### 1.2 异步函数的类型

每个JavaScript环境都自带一组异步函数。有些，如`setTimeout`和`setInterval`，是普遍存在的。其他一些则特定于某些浏览器或服务器端框架。JavaScript环境提供的异步函数通常分为两类：I/O和定时。这些是你将在应用程序中用于定义复杂异步行为的基本构建块。

#### I/O函数

Node.js的创建并非为了让人们能在服务器上运行JavaScript。它的创建是因为Ryan Dahl想要一个基于高级语言构建的事件驱动服务器框架。JavaScript恰好是这项工作的合适语言。为什么？因为这门语言非常适合*非阻塞*I/O。

在其他语言中，很容易“阻塞”你的应用程序（通常通过运行循环）直到I/O请求完成。在JavaScript中，这种做法甚至不可能。这样的循环将永远运行下去：

```javascript
var ajaxRequest = new XMLHttpRequest;
ajaxRequest.open('GET', url);
ajaxRequest.send(null);
while (ajaxRequest.readyState === XMLHttpRequest.UNSENT) {
  // readyState在循环返回之前无法改变
};
```

相反，你需要附加一个处理程序并返回到事件队列。

```javascript
var ajaxRequest = new XMLHttpRequest;
ajaxRequest.open('GET', url);
ajaxRequest.send(null);
ajaxRequest.onreadystatechange = function() {
  // ...
};
```

事情就是这样。无论你是等待用户的按键还是来自远程服务器的一批数据，你都需要定义一个回调——除非你的JavaScript环境为你提供了一个执行阻塞的同步I/O函数。

在浏览器中，Ajax方法有一个async选项，它可以（但*永远不应*）被设置为false，这会导致整个浏览器窗格在收到响应之前一直处于停止状态。在Node.js中，同步API方法通过像`fs.readFileSync`这样的名称明确标示。在编写短脚本时，这些方法很方便，但在编写需要并行处理多个请求或操作的应用程序时应避免使用。而如今，哪个应用程序不是这样呢？

一些I/O函数同时具有同步和异步效果。例如，当你在现代浏览器中操作DOM时，从你的脚本角度看，更改是立即生效的，但在返回事件队列之前不会被渲染。这防止了DOM在不一致的状态下被渲染。你可以在<http://jsfiddle.net/TrevorBurnham/SNBYV/>看到一个简单的演示。

### `console.log`是异步的吗？

WebKit的`console.log`因其异步行为而令许多开发者感到惊讶。在Chrome或Safari中，这段代码将记录`{foo: bar}`：

```javascript
// EventModel/log.js
var obj = {};
console.log(obj);
obj.foo = 'bar';
```

这是如何发生的？WebKit的`console.log`并非立即获取对象的快照，而是存储对该对象的引用，然后在代码返回事件队列时获取快照。

另一方面，Node的`console.log`是严格同步的，因此相同的代码会产生`{}`的输出。

适应非阻塞I/O是JavaScript新手面临的最大障碍之一，但它也是该语言的关键优势之一。它使得编写高效、基于事件的代码感觉很自然。

#### 定时函数

我们已经看到异步函数如何自然地适用于I/O操作，但有时我们为了异步而异步。也就是说，我们希望让函数在未来某个时间点运行，也许是为了动画或模拟。基于时间的事件的著名函数是`setTimeout`及其重复的变体`setInterval`。

不幸的是，这些著名的定时器函数有其缺陷。正如我们在*阻塞线程*（第2页）中所看到的，其中一个缺陷是无法克服的：没有JavaScript定时函数能在同一JavaScript进程中其他代码运行时导致代码运行。但即使考虑到这个限制，`setTimeout`和`setInterval`的不精确性也令人震惊。这里有一个演示：

```javascript
// EventModel/fireCount.js
var fireCount = 0;
var start = new Date;
var timer = setInterval(function() {
    if (new Date - start > 1000) {
        clearInterval(timer);
        console.log(fireCount);
        return;
    }
    fireCount++;
}, 0);
```

当我们用0ms延迟调度一个`setInterval`事件时，它应该尽可能频繁地运行，对吧？那么，在由高速Intel i7处理器驱动的现代浏览器中，这个事件以什么速率触发？

大约每秒200次。这包括Chrome、Safari和Firefox。在Node下，事件触发速率约为每秒1000次。（使用`setTimeout`调度每次迭代会产生类似结果。）相比之下，将`setInterval`替换为简单的while循环，在Chrome中将该速率提高到每秒4,000,000次，在Node中提高到每秒5,000,000次！

这是怎么回事？事实证明，`setTimeout`和`setInterval`在设计上就是慢的。事实上，HTML规范（所有主要浏览器都遵守）规定了最小超时/间隔为4ms！

那么，当你需要更精细的计时时该怎么办？一些运行时提供了替代方案。

- **在Node中**，`process.nextTick`让你可以调度一个事件尽快触发。在我的系统上，`process.nextTick`事件的触发速率超过每秒100,000次。
- 现代浏览器（包括IE9+）有一个`requestAnimationFrame`函数，它有两个用途：它允许JavaScript动画以每秒60帧以上的速度运行，并通过阻止这些动画在后台标签页中运行来节省CPU周期。在最新的Chrome中，你甚至可以获得亚毫秒级的精度。

尽管它们是异步JavaScript的支柱，但永远不要忘记`setTimeout`和`setInterval`是不精确的工具。当你只是想在Node中产生短延迟时，使用`process.nextTick`。在浏览器中，尽量使用[垫片](http://paulirish.com/2011/requestanimationframe-for-smart-animating/)，它在支持`requestAnimationFrame`的浏览器中会委托给`requestAnimationFrame`，而在不支持的浏览器中则回退到`setTimeout`。

```text
+ 1. http://www.whatwg.org/specs/web-apps/current-work/multipage/timers.html#dom-windowtimers-settimeout
+ 2. http://updates.html5rocks.com/2012/05/requestAnimationFrame-API-now-with-sub-millisecond-precision
```

至此，我们对JavaScript中基本异步函数的简要概述就结束了。但我们到底如何判断一个函数是否是异步的呢？在下一节中，我们将在编写自己的异步函数时思考这个问题。

### 1.3 编写异步函数

JavaScript中的每个异步函数都是建立在其他一些异步函数之上的。异步函数一路向下（到原生代码）都是如此！

反过来也是对的：任何使用异步函数的函数都必须以异步方式提供该操作的结果。正如我们从*阻塞线程*（第2页）中学到的，JavaScript没有提供一种机制来防止函数在异步操作完成之前返回。事实上，在函数返回之前，不会触发任何异步事件。

#### 何时函数是异步的？

异步*函数*这个术语有点用词不当：如果你调用一个函数，程序将不会继续执行，直到该函数返回。当JavaScript程序员称一个函数为“异步”时，他们的意思是可以导致另一个函数（当作为参数传递给该函数时称为回调[4]）稍后从事件队列中运行。

因此，*一个接受回调的异步函数永远不会通过这个测试*：

```javascript
var functionHasReturned = false;
asyncFunction(function() {
    console.assert(functionHasReturned);
})

functionHasReturned = true;
```

异步函数的另一个术语是*非阻塞*。这个术语强调了它们的速度：使用异步MySQL驱动程序进行的查询可能需要一个小时，但发送该查询的函数将在微秒内返回——对于需要快速处理大量传入请求的Web服务器来说，这是一个福音。

通常，接受回调的函数将其作为最后一个参数。（遗憾的是，著名的`setTimeout`和`setInterval`是此约定的例外。）但是一些异步函数通过返回`Promise`或使用`PubSub`间接接受回调。我们将在本书后面了解这些模式。

不幸的是，确保一个函数是否是异步的唯一方法是检查其源代码。一些同步函数的API看起来是异步的，要么是因为它们将来可能变成异步，要么是因为回调提供了一种返回多个参数的便捷方式。如有疑问，请不要依赖函数是异步的。

#### 有时异步的函数

有些函数有时是异步的，有时不是。例如，jQuery的同名函数（通常别名为`$`）可用于将函数延迟到DOM加载完成。但如果DOM已经加载完成，则没有延迟；其回调会立即触发。

如果你不小心，这种不可预测的行为可能会让你陷入很多麻烦。我见过（也犯过）的一个错误是假设`$`会在页面上其他脚本加载后运行函数。

```html
<!-- application.js -->
$(function() {
    utils.log('Ready');
});

<!-- utils.js -->
window.utils = {
    log: function() {
        if (window.console) console.log.apply(console, arguments);
    }
};
<script src="application.js"></script>
<script src="util.js"></script>
```

这段代码运行正常——除非浏览器从缓存加载页面，导致DOM在脚本运行之前就准备就绪。当这种情况发生时，传递给`$`的回调在`utils.log`设置之前运行，导致错误。（我们可以通过采用更现代的客户端依赖管理方法来避免这种情况。参见第6章“异步脚本加载”，第69页。）

让我们看另一个例子。

### 带缓存的异步函数

一种常见的有时异步的函数是缓存其结果的异步请求函数。例如，假设我们正在编写一个基于浏览器的计算器，该计算器使用 Web Worker 在单独的线程中运行计算。（我们将在[第 5 章，使用 Worker 进行多线程，见第 61 页](https://example.com)学习 Web Worker API。）我们的主脚本可能如下所示：

```javascript
var calculationCache = {},
    calculationCallbacks = {},
    mathWorker = new Worker('calculator.js');

mathWorker.addEventListener('message', function(e) {
    var message = e.data;
    calculationCache[message.formula] = message.result;
    calculationCallbacks[message.formula](message.result);
});

function runCalculation(formula, callback) {
    if (formula in calculationCache) {
        return callback(calculationCache[formula]);
    };
    if (formula in calculationCallbacks) {
        return setTimeout(function() {
            runCalculation(formula, callback);
        }, 0);
    };
    mathWorker.postMessage(formula);
    calculationCallbacks[formula] = callback;
}
```

这里，当结果已被缓存时，`runCalculation`函数是同步的，否则是异步的。有三种可能的场景。

- 公式已经计算完毕，因此结果在`calculationCache`中。在这种情况下，`runCalculation`是同步的。
- 公式已发送给`Worker`，但尚未收到结果。在这种情况下，`runCalculation`设置一个超时来再次调用自身；该过程将重复，直到结果出现在`calculationCache`中。
- 公式尚未发送给`Worker`。在这种情况下，我们将从`Worker`的`message`事件监听器中调用回调。

请注意，在场景2和3中，我们以两种不同的方式等待任务完成。我这样写示例是为了说明当我们等待某些事情发生变化时（如缓存计算的值）的常见方法。我们应该更倾向于哪种方法？接下来我们来探讨这个问题。

### 异步递归 vs. 回调存储

在`runCalculation`中，我们通过从超时中重复相同的函数调用（异步递归）或简单地存储回调来等待`Worker`完成其工作。

哪种方法最好？乍一看，似乎只使用异步递归最容易，从而消除了对`calculationCallbacks`对象的需求。JavaScript新手经常为此使用`setTimeout`，因为它类似于基于线程的语言中的常见惯用法。该程序的Java版本可能会有一个像这样的循环：

```javascript
while (!calculationCache.get(formula)) {
  Thread.sleep(0);
};
```

但超时并非没有成本。大量超时会产生显著的计算负载。异步递归的可怕之处在于，在我们等待任务完成时，触发的超时数量没有限制。此外，它使我们应用程序的事件结构变得不必要地复杂。因此，异步递归应被视为一种反模式。

我们可以通过为每个公式存储一个回调数组来在我们的计算器中避免异步递归。

```javascript
var calculationCache = {},
    calculationCallbacks = {},
    mathWorker = new Worker('calculator.js');
mathWorker.addEventListener('message', function(e) {
  var message = e.data;
  calculationCache[message.formula] = message.result;
  calculationCallbacks[message.formula]
  .forEach(function(callback) {
    callback(message.result);
  });
});

function runCalculation(formula, callback) {
  if (formula in calculationCache) {
    return callback(calculationCache[formula]);
  };
```

```javascript
if (formula in calculationCallbacks) {
    return calculationCallbacks[formula].push(callback);
};
mathWorker.postMessage(formula);
calculationCallbacks[formula] = [callback];
}
```

没有超时，我们的代码变得简单得多，也更高效。

总的来说，避免异步递归。只有在处理不提供任何回调机制的异步功能库时才需要它。如果你遇到这种情况，你应该做的第一件事是为该库编写一个补丁。或者找一个更好的库。

### 混合使用返回值和回调

在我们对`runCalculation`的两种实现中，我们有时会返回一个值。这是为了简洁而做出的任意选择。这行代码

```javascript
return callback(calculationCache[formula]);
```

可以很容易地写成

```javascript
callback(calculationCache[formula]);
return;
```



因为返回值并不打算被使用。这是 JavaScript 中的常见惯用法，通常无害。

然而，一些函数既返回一个有用的值，又接受一个回调。在这些情况下，重要的是要记住回调将被同步调用（在返回之前）或异步调用（在返回之后）。

永远不要定义一个可能同步的函数，该函数返回一个可能在回调中有用的值。例如，这个打开到给定服务器的 WebSocket⁵ 连接的函数（缓存以确保每个服务器只有一个连接）违反了该规则：

```javascript
var webSocketCache = {};
function openWebSocket(serverAddress, callback) {
  var socket;

  if (serverAddress in webSocketCache) {
    socket = webSocketCache[serverAddress];

    if (socket.readyState === WebSocket.OPEN) {
      callback();
```

+   5. https://developer.mozilla.org/en/WebSockets/

```javascript
    } else {
      socket.onopen = _.compose(callback, socket.onopen);
    }
  } else {
    socket = new WebSocket(serverAddress);
    webSocketCache[serverAddress] = socket;
    socket.onopen = callback;
  }
  return socket;
}
```

（此代码依赖于 Underscore.js 库。`_.compose` 定义了一个新函数，该函数同时运行 `callback` 和原始的 `socket.onopen` 回调。⁶）

这段代码的问题在于，如果套接字已经被缓存并且是打开的，那么回调将在函数返回之前运行，这会破坏这段代码：

```javascript
var socket = openWebSocket(url, function() {
  socket.send('Hello, server!');
});
```

解决方案是什么？将回调包装在 `setTimeout` 中。

```javascript
if (socket.readyState === WebSocket.OPEN) {
  setTimeout(callback, 0);
} else {
  // ...
}
```

在这里使用超时可能感觉像是一种变通方法，但它比拥有一个不一致的 API 要好得多。

在本节中，我们看到了编写异步函数的几个最佳实践。不要依赖一个函数总是异步的，除非你阅读过它的源代码。避免使用计时器方法等待事情发生变化。当从同一个函数返回值并运行回调时，确保回调在返回之后运行。

一次性接收这么多信息可能有点困难，但编写好的异步函数是编写好的 JavaScript 的关键。

## 1.4 处理异步错误

像许多现代语言一样，JavaScript 允许你抛出异常并在 `try/catch` 块中捕获它们。如果未捕获，大多数环境会给你一个有用的堆栈跟踪。例如，这段代码会抛出一个异常，因为 `'{'` 不是有效的 JSON：

6. http://documentcloud.github.com/underscore/#compose

```javascript
EventModel/stackTrace.js
function JSONToObject(jsonStr) {
  return JSON.parse(jsonStr);
}
var obj = JSONToObject('{');
```

> SyntaxError: Unexpected end of input

>     at Object.parse (native)

>     at JSONToObject (/AsyncJS/stackTrace.js:2:15)

>     at Object.<anonymous> (/AsyncJS/stackTrace.js:4:11)

堆栈跟踪不仅告诉我们错误是从哪里抛出的，还告诉我们最初的错误发生在哪里：第 4 行。不幸的是，跟踪异步错误的原因并不那么简单。在本节中，我们将了解为什么 `throw` 很少是处理回调中错误的正确工具，以及异步 API 是如何围绕此限制设计的。

## 从回调中抛出错误

当我们从异步回调中抛出错误时会发生什么？让我们运行一个测试。

```javascript
EventModel/nestedErrors.js
setTimeout(function A() {
  setTimeout(function B() {
    setTimeout(function C() {
      throw new Error('Something terrible has happened!');
    }, 0);
  }, 0);
}, 0);
```

这个应用程序的结果是一个非常短的堆栈跟踪。

> Error: Something terrible has happened!

>     at Timer.C (/AsyncJS/nestedErrors.js:4:13)

等一下——A 和 B 怎么了？为什么它们不在堆栈跟踪中？嗯，因为当 C 运行时，它们不在栈上。这三个函数都是直接从事件队列中运行的。

出于同样的原因，我们不能用 `try/catch` 块捕获从异步回调中抛出的错误。这是一个演示：

```javascript
EventModel/asyncTry.js
try {
  setTimeout(function() {
    throw new Error('Catch me if you can!');
  }, 0);
} catch (e) {
  console.error(e);
}
```

## 第 1 章 理解 JavaScript 事件 •

你看到这里的问题了吗？我们的 `try/catch` 块只能捕获 `setTimeout` 函数*内部*发生的错误。由于 `setTimeout` 是异步运行其回调函数的，即使超时时间为 0，它抛出的错误也会直接进入我们应用程序的未捕获异常处理程序（参见第 14 页的“处理未捕获的异常”）。

```javascript
EventModel/readFile.js

var fs = require('fs');
fs.readFile('fhgwgaz.txt', function (error, data) {
  if (err) {
    return console.error(err);
  }
  console.log(data.toString("utf8"));
});
```

---

在浏览器中，你可以将全局错误处理程序附加到 `window.onerror`。如果处理程序返回 `true`，它将阻止浏览器的默认错误处理行为。

```javascript
window.onerror = function(err) {
  return true;  // 完全忽略所有错误
};
```

在生产环境中，你可能需要考虑使用 JavaScript 错误处理服务，例如 Errorception。⁷ Errorception 提供了一个现成的 `window.onerror` 处理程序，将所有未捕获的异常报告给他们的服务器，然后服务器可以向你发送通知。

## 在 Node.js 中

Node 中与 `window.onerror` 对应的是 `process` 对象的 `uncaughtException` 事件。通常，Node 应用程序会在未捕获的异常时立即退出。但只要存在至少一个 `uncaughtException` 处理程序，应用程序就会简单地返回到事件队列。

```javascript
process.on('uncaughtException', function(err) {
  console.error(err); // 避免了关闭！
});
```

然而，从 Node 0.8.4 开始，`uncaughtException` 已被弃用。根据文档，⁸

> uncaughtException 是一种非常粗糙的异常处理机制，将来可能会被移除……

不要使用它，改用 `domain`。

什么是 `domain`？你可能会问。`Domain` 是将 `throw` 转换为 `'error'` 事件的事件化对象。（我们将在第 2 章第 19 页的“分发事件”中讨论更多关于事件化对象的内容。）以下是一个示例：

```javascript
EventModel/domainThrow.js
var myDomain = require('domain').create();
myDomain.run(function() {
  setTimeout(function() {
    throw new Error('Listen to me!');
  }, 50);
});

myDomain.on('error', function(err) {
  console.log('Error ignored!');
});
```

7. http://errorception.com/

8. http://nodejs.org/docs/latest/api/process.html#process_event_uncaughtexception

超时事件中的 `throw` 只会触发 `domain` 的错误处理程序。

> 错误被忽略了！

很神奇，不是吗？`Domain` 让 `throw` 变得更加可接受了。不幸的是，它们只在 Node 0.8+ 中可用，而且截至本文撰写时，它们仍被视为实验性功能。更多信息请参阅 Node 文档。⁹

无论你是在浏览器还是服务器上，全局异常处理程序都应被视为最后的手段。仅将它们用于调试。

### 抛出还是不抛出？

当你收到一个错误时，最简单的做法就是抛出它。在 Node 代码中，你经常会看到如下所示的回调：

```javascript
function(err) {
    if (err) throw err;
    // ...
}
```

我们将在第 4 章第 47 页的“使用 Async.js 进行流控制”中经常使用这种习语。但在生产应用程序中，让常规异常和致命错误都冒泡到全局处理程序是不可接受的。在回调中使用 `throw` 是 JavaScript 开发者说“我现在不想考虑这个”的方式。

那么，抛出你知道会被捕获的异常呢？这同样是一个棘手的领域。2011 年，Isaac Schlueter（npm 的创建者和 Node 开发的现任负责人）认为 `try/catch` 是一种反模式。¹⁰

> `Try/catch` 是用漂亮的括号包裹的 `goto`。一旦错误被处理，就无法从上次中断的地方继续。更糟糕的是，在抛出错误的代码中，你根本不知道会跳转到哪里。当你返回错误码时，你正在履行一个契约。当你抛出时，你是在说：“我知道我在和你说话，但我现在要跳过你，直接和你的老板说话。”这是无礼的。如果不是紧急情况，不要这样做；如果是紧急情况，那么我们应该崩溃。

Schlueter 主张将 `throw` 纯粹用作类似 `assert` 的构造，一种让应用程序在做出完全出乎意料的事情时停止运行的方式。Node 社区在很大程度上遵循了这一建议，尽管随着 `domain` 的出现，这种情况可能会改变。

那么，当前处理异步错误的最佳实践是什么？我建议遵循 Schlueter 的建议：如果你想让整个应用程序停止，那就放心使用 `throw`。否则，请考虑一下应该如何处理错误。你想向用户显示错误消息？重试请求？唱一首《Daisy Bell》？那就近源处理，越接近 `eem_omon` 生成的源越好。

## 1.5 取消回调嵌套

JavaScript 中最常见的反模式是在回调中嵌套回调。还记得引言中的“末日金字塔”吗？让我们来看一个你可能在 Node 服务器中看到的具体示例。

```javascript
function checkPassword(username, passwordGuess, callback) {
  var queryStr = 'SELECT * FROM user WHERE username = ?';
  db.query(selectUser, username, function (err, result) {
    if (err) throw err;
    hash(passwordGuess, function(passwordGuessHash) {
      callback(passwordGuessHash === result['password_hash']);
    });
  });
}
```

在这里，我们定义了一个异步函数（`checkPassword`），它触发另一个异步函数（`db.query`），后者又可能触发另一个异步函数（`hash`）。（如果不实际阅读它们的代码，不可能确定这些函数是否是异步的，但在这里做出这样的假设是合理的。）

这段代码有什么问题？现在，没什么。它能工作，而且简洁。但当我们尝试向其中添加新功能时，它就会变得非常棘手，比如处理数据库错误而不是抛出它（参见第 16 页的“抛出还是不抛出？”），记录访问尝试、限流等等。

嵌套回调诱使我们通过添加更多代码来添加更多功能，而不是以可管理、可重用的方式实现这些功能。下面这个 `checkPassword` 的等价实现避免了这种诱惑：

```javascript
function checkPassword(username, passwordGuess, callback) {
  var passwordHash;
  var queryStr = 'SELECT * FROM user WHERE username = ?';
  db.query(selectUser, username, queryCallback);

  function queryCallback(err, result) {
    if (err) throw err;
    passwordHash = result['password_hash'];
    hash(passwordGuess, hashCallback);
  }

  function hashCallback(passwordGuessHash) {
    callback(passwordHash === passwordGuessHash);
  }
}
```

这种方法更冗长，但读起来更清晰，也更容易扩展。因为我们给了异步结果（`passwordHash`）更广泛的作用域，所以我们有了更大的灵活性。

作为一条规则，避免超过两层函数嵌套。关键是要想出一种方法，将异步结果存储在发起异步调用的函数之外，这样回调就不需要嵌套了。

如果这一切听起来很棘手，别担心。在后面的章节中，我们会看到很多异步事件在不嵌套处理程序的情况下按顺序运行的示例。

## 1.6 我们学到了什么

在本章中，我们看到了 JavaScript 的单线程性既是福也是祸。在合适的人手中，它可以创造出美丽的代码，免受困扰多线程应用程序的可怕竞态条件的影响。但你需要培养正确的思维方式——以及正确的技术。

本书的其余部分将介绍用于在 JavaScript 中处理事件的库和设计模式。我们将要看到的所有示例都将在主流浏览器或未修改的 Node.js 中运行。然而，编写 JavaScript 并不是生成 JavaScript 代码的唯一方式。有关一些有趣的替代方案的概述，参见第 81 页的`附录 1，驯服 JavaScript 的工具`。

值得一提的是，JavaScript 中有一种多线程方式：你可以生成工作进程。每个生成的进程可以在与其他 I/O 相同的限制下与其他进程交换数据。工作进程使得利用多核成为可能，而不会违反 JavaScript 的规则（代码不能被中断；变量只能在其作用域内访问）。有关工作进程的更多信息，请跳至第 61 页的`第 5 章 使用工作进程进行多线程`。

接下来的两章将介绍基本的设计模式：PubSub，一种通过将回调分配给命名事件来组织回调的方式；以及 Promises，一种用于一次性事件的直观对象表示。

## 第二章

## 事件分发

在上一章中，我们探讨了 JavaScript 中异步事件的运作方式。但在实践中，我们应该如何处理这些事件呢？

这听起来可能是一个愚蠢的问题：只需将处理程序附加到你应用程序关心的每个事件上就行了吧？但当单个事件产生多个后果时，“一个事件对应一个处理程序”的方法会迫使处理程序的规模增长至*巨大无比*。

假设你正在构建类似 Google Docs 的基于 Web 的文字处理器。每当用户按下一次按键，就会发生多种事情：新字符必须在屏幕上显示、插入点必须移动、该操作必须被推送到本地撤销历史并同步到服务器、拼写检查可能需要运行，以及单词计数和页数可能需要更新。仅从一个按键处理程序中执行所有这些任务以及其他任务是令人望而却步的。

从纯粹的机械角度来看，我们希望在响应事件时执行的每项任务确实都需要从其处理程序发起启动。但对于人类而言，用更灵活、动态的结构替换那个庞大的事件处理程序通常要好得多——这是一个可以在运行时向其添加或移除任务的构造体。简而言之，我们要使用*分布式事件*（distributed events）的概念，其中单个事件可以触发应用程序中的各种反应。

在本章中，你将学习如何使用 Publish/Subscribe 模式（也称为 *PubSub* 来分发事件。在此过程中，我们将接触到 PubSub 的几种表现形式：Node.js 的事件发射器、Backbone 的可事件化模型以及 jQuery 的自定义事件。借助这些工具，我们将从回调函数中提取嵌套层数、减少重复代码，并编写易于理解的事件驱动代码。

### 2.1 PubSub

自从 JavaScript 诞生之日起，浏览器就一直允许将事件处理程序类似这样附加到 DOM 元素上：

```javascript
link.onclick = clickHandler;
```

Ah（啊），简单至极！这里只有一个细微差别：如果你想要为某个元素提供*两个*点击事件处理程序，你就必须自己使用包装函数将它们聚合。

```javascript
link.onclick = function() {
  clickHandler1.apply(this, arguments);
  clickHandler2.apply(this, arguments);
};
```



这不仅繁琐，还是导致臃肿、万金油式（all-purpose）处理函数的配方之源。这就是 W3C 于 2000 年将 `addElementEventListener` 添加到 DOM 规范以及 jQuery 通过 `bind` 方法对其进行抽象的原因。`bind` 使得你可以为任何元素（或任意一组元素上的）任何事件轻松添加尽可能多的监听器，而无需担心踩到其他人的尾巴[1](http://api.jquery.com/on/)。

```
$(link)
  .bind('click', clickHandler1)
  .bind('click', clickHandler2);
```

（在 jQuery 1.7+ 版本中，更倾向于使用新的 `on` 语法[1](http://api.jquery.com/on/)[^1]。还有一个 `click` 方法，它是 `bind('click', ...)` 的快捷方式；不过，我更倾向于始终一致地使用 `bind` 或 `on`。）

从软件架构的角度来看，jQuery 发布（publish）了 `link` 元素的任何想要订阅其事件的人都会接收到的事件。这就是它为什么被称为“PubSub[2](http://nodejs.org/docs/latest/api/events.html)[^2]”的原因。

就神学而言，PubSub 是一种民主制。旧式的 DOM 事件 API 中绑定到对象意味着书写 `object.onevent=...` 等代码现在在某种程度上已被人们所遗忘（转而使用 PubSub）。Node.js API 的设计者非常喜欢 PubSub，以至于他们决定包含一个通用的名为 `EventEmitter` 的实体供其他对象继承。可以说，Node.js 中的几乎每一项 I/O 来源都是一个 `EventEmitter`：文件流、HTTP 服务器甚至是应用程序进程本身都可以作为示例[3](http://nodejs.org/docs/latest/api/events.html)[^2]。

```
['room', 'moon', 'cow jumping over the moon']
.forEach(function(name) {
  process.on('exit', function() {
    console.log('Goodnight, ' + name);
  });
});
```

对于浏览器存在无数独立的 PubSub 库[4](http://nodejs.org/docs/latest/api/events.html)[^2]。此外，许多 MVC 框架如 Backbone.js 和 Spine 也提供了自己的类似事件发射器的模块。我们将在本章后面更深入地讨论 Backbone 的内容。

## 自行实现 EventEmitter

让我们使用 Node.js 的 `EventEmitter` 作为 PubSub 接口的示例，其设计简单而紧凑：[4](http://nodejs.org/docs/latest/api/events.html)[^2]。

要将处理程序附加到事件发射器上，只需调用 `on` 并传入事件类型和处理程序即可。

```
emitter.on('evacuate', function(message) {
  console.log(message);
});
```

`emit` 方法将调用给定的所有指定类型的处理函数。例如以下代码：

```
emitter.emit("evacuate");
```

会启动所有的 `evacuate` 处理器[5](http://nodejs.org/docs/latest/api/events.html)[^2]。

请注意，此处使用的术语*事件*（event）与事件队列没有任何关系。请参见第 22 页的[Synchronicity, on page 22](#)。

当你触发一个事件时，你可以添加任意数量的附加论据变量[6](http://nodejs.org/docs/latest/api/events.html)[^2]。所有这些参数都会传递给所有处理器函数：

```
emitter.emit('evacuate', 'Woman and children first!');
```

对事件名称没有限制，尽管 Node.js 文档建议了一些有用的约定^[7](http://nodejs.org/docs/latest/api/events.html)^。

通常，事件名由大驼峰命名的字符串表示^[8](http://nodejs.org/docs/latest/api/events.html)^。`EventEmitter` 的所有方法都是公开的，但以在 `EventEmitter`“内部”仅发射事件的惯例是常见的做法[9](http://nodejs.org/docs/latest/api/events.html)[^2]。即如果你的对象继承了 `EventEmitter` 原型并使用 `this.emit` 来广播事件，那么其 `emit` 不应在其他地方被调用。

## Roll Your Own PubSub

PubSub 实现非常简洁，我们可以用大约十二行代码就创建一个[7](http://nodejs.org/docs/latest/api/events.html)[^2]。

我们需要存储的唯一状态是每个支持的事件类型的处理器列表。

```
pubsub = {handlers: {}}
```

当你添加监听器时，它会被推送到数组末尾（这意味着监听程序会按照它们被添加的顺序被调用）：[8](http://nodejs.org/docs/latest/api/events.html)[^2]。

```
PubSub.on = function(eventType, handler) {
  if (!(eventType in this.handlers)) {
    this.handlers[eventType] = [];
  }
  this.handlers[eventType].push(handler);
  return this;
};
```

然后在发射事件时，我们遍历所有的监听程序[10](http://nodejs.org/docs/latest/api/events.html)[^2]。

```
PubSub.emit = function(eventType) {
  var handlerArgs = Array.prototype.slice.call(arguments, 1);
  for (var i = 0; i < this.handlers[eventType].length; i++) {
    this.handlers[eventType][i].apply(this, handlerArgs);
  }
  return this;
};
```

这就够了。我们刚刚实现了 Node.js `EventEmitter` 的核心功能。（唯一缺少的主要功能是移除处理器和附加一次性处理程序的功能。）

当然，PubSub 实现因功能而异略有不同[12](http://nodejs.org/docs/latest/api/events.html)[^2]。当 jQuery 团队注意到库中正在使用多种不同的 PubSub 实现时，他们决定通过在 jQuery 中的 `$.Callbacks` 进行抽象（在 jQuery 1.7 中）。与其用数组来存储对应于特定事件类型的处理程序，你可以使用一个 `$.Callbacks` 实例[5](http://nodejs.org/docs/latest/api/events.html)[^2]。

许多 PubSub 实现会解析事件字符串以提供特殊功能。例如你可能熟悉 jQuery 中的命名空间事件：如果我将名为 `"click.tbb"` 和 `"hover.tbb"` 的事件绑定器，那么只需调用 `unbind(".tbb")` 就可以同时解除这两个绑定[6](http://nodejs.org/docs/latest/api/events.html)[^2]。Backbone.js 允许你将处理器与“all”事件类型进行绑定，导致它们一旦有任何事情发生就触发。jQuery 和 Backbone 都可以通过间隔多个事件来支持同时绑定或发射多种事件类型的功能，例如 `"keydown mouseover"`[7](http://nodejs.org/docs/latest/api/events.html)[^2]。

## 同步性

尽管 PubSub 是处理异步事件的重要技术之一，但它本质上并非异步特性[8][9](http://nodejs.org/docs/latest/api/events.html)[^2]。考虑以下代码：

```
$('input[type=submit]')
  .on('click', function() {
    console.log('foo');
  })
  .trigger('click');

console.log('bar');
```

输出结果如下所示：

```
foo bar
```

[10](http://nodejs.org/docs/latest/api/events.html)[^2] 证明 `click` 处理器立即由 `trigger` 调用而触发。实际上，每当 jQuery 事件触发时都会按顺序执行其所有处理程序[8][^2]。

因此让我们明确一点：当用户点击提交按钮时那是一个异步事件。第一次点击是通过事件队列触发的（而不是手动调用的）。但是处理器无法确定它是在响应事件队列还是由应用程序代码直接呼出[1](http://nodejs.org/docs/latest/api/events.html)[^3]。

如果太多处理程序按顺序触发，你面临着阻塞线程并使浏览器无响应的风险。更糟糕的是，如果在处理程序中发射事件则很容易造成无限循环：

```
$('input[type=submit]')
  .on('click', function() {
    $(this).trigger('click');
    // 堆栈溢出！
  });
```

回想一下本章开头提到的文字处理器例子。当用户按下按键时会有许多事情需要做，其中一些需要复杂的计算[13](http://nodejs.org/docs/latest/api/events.html)[^2]。在执行完所有这些任务之前返回到事件队列的做法会导致应用程序无法响应（死机）。

解决这个问题的一个不错方案是维护一份清单列表以存放那些不必立即执行的任务，并使用时钟函数定期运行该队列中的下一个任务。初步尝试可能看起来像这样：

```
var tasks = [];
setInterval(function() {
  var nextTask;
  if (nextTask = tasks.shift()) {
    nextTask();
  }
}, 0);
```

（我们稍后将在第 4 章*动态异步队列*（见第 54 页）中学习一种更高级的任务排队方式：**第四节，[动态异步队列](#section-4.4)** [^2]）

## 2.2 事件化模型

当一个对象拥有 PubSub 接口时，我们称其为*事件化*对象。一种特殊情况是，当用于存储数据的对象（*模型*）在其内容被修改时发布事件。模型是模型-视图-控制器（MVC）中的 *M*，这在过去的几年里已成为 JavaScript 编程中最热门的话题之一。核心概念是 MVC 应用以数据为中心，因此模型事件会影响 DOM（也称为视图）和服务器（通过控制器）。

让我们看看大受欢迎的 Backbone.js 框架。你可以这样创建一个新的模型：

```
style = new Backbone.Model({
  font: 'Georgia'
});
```

`model` 仅代表传入的那个简单对象。

```
style.toJSON() // {"font": "Georgia"}
```

但与普通对象不同，这个对象会在做出更改时发布通知。

```
style.on('change:font', function(model, font) {
  alert('感谢你选择 ' + font + '!');
});
```

传统 JavaScript 直接通过输入事件处理程序更改 DOM。新一代 JavaScript 更改模型，然后发出事件，从而导致 DOM 更新。在几乎所有应用中，这种关注点分离带来了更优雅、更直观的代码。

## 传播模型事件

在最简单的形式下，MVC 由将模型连接到视图组成：“如果模型以这种方式更改，DOM 就以这种方式更改。”但 MVC 的最大收益发生在变更事件沿着数据树向上冒泡时。你无需在每个叶节点订阅事件，只需订阅根节点和分支即可。

> http://documentcloud.github.com/backbone/

## 事件化模型上的 Set/Get

正如我们所知，JavaScript 没有机制在每次对象被修改时触发事件。因此，为了让事件化模型起作用，我们必须记得使用像 Backbone 的 `set` 和 `get` 这样的方法。

```
style.set({font: 'Palatino'});  // 触发警报！
style.get('font');              // "Palatino"
style.font = 'Comic Sans';      // 不会触发事件
style.font;                     // "Comic Sans"
style.get('font');              // 仍然是 "Palatino"
```

如果被称为 `Object.observe` 的 ECMAScript 提案被广泛采用，这在将来可能不再是必需的[a](https://plus.google.com/111386188573471152118/posts/6peb6yffyWG)。

为此，Backbone 模型通常组织成 Backbone 集合，这些集合本质上是事件化数组。你可以监听模型何时被添加或从中移除。Backbone 集合会自动传播它们包含的模型中的事件。

例如，你可能有一个 `spriteCollection` 对象，其中包含数百个代表你在画布元素上绘制内容的模型。每当这些精灵中的任何一个发生变化时，你都需要重绘画布。与其将重绘函数单独作为每个精灵的 `change` 事件的处理程序附加上去，你只需编写以下内容：

```
spriteCollection.on('change', redraw);
```

请注意，这种自动传播仅向下延伸一级。Backbone 没有嵌套集合的概念。然而，你可以使用 Backbone 的 `trigger` 方法自己实现这种传播。通过它，任何 Backbone 对象都可以发出任意事件。

## 循环和嵌套变更

从一个对象向另一个对象传播事件会引起某些关注。如果一个对象上的事件引发了一系列事件，最终每次都会触发同一对象上的同一事件，那么结果就是一个事件循环。如果循环是同步的，结果将是栈溢出，就像我们在第 22 页的同步性中所见。

然而，通常情况下，变更事件的循环正是我们所想要的。最常见的情况是双向绑定，其中两个模型具有相互关联的值。假设我们要确保 `x` 始终等于 `2 * y`。

```
var x = new Backbone.Model({value: 0});
var y = new Backbone.Model({value: 0});
x.on('change:value', function(x, xVal) { y.set({value: xVal / 2}); });
y.on('change:value', function(y, yVal) { x.set({value: 2 * yVal}); });
```

你可能期望这段代码在 `x` 或 `y` 的值被更改的瞬间导致无限循环。但实际上，由于 Backbone 中的两个保护措施，它非常安全。

- 如果新值与旧值匹配，`set` 不会发出变更事件。
- 模型不能在其自身的变更事件期间发出变更事件。

第二个保护措施本身也存在陷阱。假设对模型进行了更改，导致对同一模型进行了第二次更改。因为第二次更改是“嵌套”在第一次中的，它会静默发生。观察者没有机会对此做出反应。

显然，在 Backbone 中维护双向数据绑定是一个挑战。另一个主要的 MVC 框架 Ember.js 采取了不同的方法：双向绑定是显式声明的。当一个值更改时，另一个值会从超时事件异步更新。因此，在该事件触发之前，应用程序的数据可能处于不一致状态。

跨事件化模型的绑定问题没有简单的解决方案。在 Backbone 中，明智地避开这个问题的方法是使用 `silent` 标志。如果你向 `set` 添加 `{silent: true}`，就不会发生变更事件。因此，如果需要同时更新几个纠缠的模型，一个很好的方法是将它们静默设置。然后调用它们的更改方法，以仅在它们处于一致状态时触发适当的事件。

事件化模型为我们提供了一种直观的方式，将应用程序状态变化转换为事件。Backbone 和其他 MVC 框架所做的所有事情都是关于这些模型，当它们的状态发生变化时更新 DOM 和服务器。在事件化模型中存储可变数据是控制客户端 JavaScript 应用程序日益增长的复杂性的绝佳第一步。

### 2.3 自定义 jQuery 事件



# 自定义事件

自定义事件是 jQuery 的一个未被充分重视的特性，它使得在任何 Web 应用中嫁接一个强大的分布式事件系统变得容易，而无需额外的库。你可以使用 `trigger` 从 jQuery 中的任何 DOM 元素发出任何你想要的事件。

```javascript
$('#tabby, #socks').on('meow', function() {
 console.log(this.id + ' meowed');
});
$('#tabby').trigger('meow'); // "tabby meowed"
$('#socks').trigger('meow'); // "socks meowed"
```

如果你之前处理过 DOM 事件，那么你无疑熟悉冒泡现象。每当一个元素发出一个事件（例如 `click`），它的父元素就会发出该事件，然后是其祖父元素，依此类推，一直上升到根元素 `document`——除非在此过程中某处调用了事件的 `stopPropagation` 方法。（当我们从处理程序返回 `false` 时，jQuery 会自动为我们执行此操作。）但你是否知道 jQuery 的自定义事件也会冒泡？例如，如果我们有一个名为 `"soda"` 的 `span` 嵌套在一个名为 `"bottle"` 的 `div` 中，代码

```javascript
$('#soda, #bottle').on('fizz', function() {
    console.log(this.id + ' emitted fizz');
});
$('#soda').trigger('fizz');
```

将产生以下输出：

```text
soda emitted fizz
bottle emitted fizz
```

这种冒泡并不总是可取的，我们将在下面的工具提示示例中看到这一点。幸运的是，jQuery 也提供了非冒泡的 `triggerHandler` 方法。

## 示例：工具提示

当事件可以直观地映射到页面元素时，jQuery 是分发它们的理想方式。例如，假设你在编写一个工具提示库，并且你希望一次只显示一个工具提示。你可能只是简单地在添加新工具提示的函数开头添加一行代码

```javascript
$('.tooltip').remove();
```

但是，如果我们稍后决定希望某些容器被隔离，例如当侧边栏中显示新工具提示时，其他地方不受影响，反之亦然呢？编写“不属于侧边栏后代的带有 `tooltip` 类的元素”的选择器很棘手，而且效率不高。如果我们决定允许隔离容器嵌套到任意深度，问题将呈指数级增长。

但是，使用事件逻辑而不是选择器逻辑来实现这种行为很容易。

```javascript
// $container 可以是 $('#sidebar') 或 $(document)
$container.triggerHandler('newTooltip');
$container.one('newTooltip', function() {
    $tooltip.remove();
});
```

## 我们学到了什么

（注意这里使用的是 jQuery 的 `one` 而非 `on`。区别在于，`one` 在事件触发后会自动移除处理程序。）

仅用这两行代码，每个提示框就能监听其容器，并在容器接收新提示框时自行移除。这是一种优雅、直接且高效的方法，免去了我们存储任何状态或构建复杂选择器的麻烦（后者会拖慢旧版浏览器的运行速度——IE7 及更早版本甚至无法在不遍历整个文档的情况下选中所有带有 `tooltip` 类的元素！）。

请注意，事件冒泡在这种情况下实际上会违背我们的意图：当我们在侧边栏创建一个新提示框时，我们只希望监听侧边栏本身 `newTooltip` 事件的提示框消失，而不是文档其他区域的提示框。务必仔细思考 `trigger` 或 `triggerHandler` 哪个才是完成任务的正确工具。

自定义 jQuery 事件是 PubSub 的一种独特变体，因为这些事件是由可选元素触发的，而不是我们脚本中的对象。正如基于事件的模型是表达状态相关事件的直观方式一样，jQuery 事件让我们能够直接通过 DOM 表达与 DOM 相关的事件，从而无需在应用程序的其他地方重复定义状态。请大胆使用它们，但尽量避免依赖应用程序标记的结构——你不希望下一次重新设计时导致你的脚本失效。

在本章中，我们学习了如何通过 PubSub 分发事件，这是 JavaScript 最基本的设计模式之一。当你不订阅已发布的事件时，PubSub 完全是非侵入式的。正确使用 PubSub 的关键在于决定通过哪些实体来分发事件。

我们已经看到，任何对象都可以用于 PubSub，只需继承类似 `Node.js` 的 `EventEmitter` 即可。每当一个对象与一组异步任务或 I/O 事件相关联时，将其设计为基于事件的是一个好主意。

这类基于事件的对象的一个例子是像 `Backbone.js` 这样的 MVC 库中的模型。这些模型既包含应用程序状态，又会宣布状态的变化。变化事件可以触发应用程序逻辑、DOM 更新以及与服务器的同步。这一切都显得非常自然，这也解释了为什么 `Backbone` 成为了一个大受欢迎的库。DOM 事件与之完美互补，有助于将应用程序的状态和视图相互封装。

所有这些都展示了 PubSub 的实际应用。然而，尽管 PubSub 用途广泛，但它并非适用于所有任务的合适工具。特别是，它不适合一次性事件，即异步函数执行某个任务，而其完成或失败需要以独特方式处理的情况。（Ajax 请求就是一个常见的例子。）解决此问题的一个工具称为 `Promise`，这将是下一章的主题。

# 第 3 章

## Promise 与 Deferred

2010 年，我与我那才华横溢的同事 `Ajax` 先生进行了如下对话：

我：嘿，你能帮我从这个 URL 获取一些数据吗？

`Ajax` 先生：我这就去！给我一个成功回调函数，完成后我就能通知你。

我：好的，给你。谢谢。

`Ajax` 先生：哦，你还应该给我一个错误回调函数。你知道，以防万一。

我：说得对。还有别的吗？

`Ajax` 先生：嘿，我注意到这两个回调函数之间有些代码重复！你可以把这部分提取出来放到第三个 `always` 回调函数里。

我：（不耐烦地）好吧，我来重构它们。这样吧：你现在先去执行，我稍后给你回调函数？

`Ajax` 先生：（愤怒地）我看起来像是个 `EventEmitter` 吗？

幸好，`jQuery 1.5` 改变了 `Ajax` 先生这种急于求成的态度。你所熟知和喜爱的所有 Ajax 函数（`$.ajax`、`$.get` 和 `$.post`）现在都返回 `Promise`。`Promise` 是一个代表具有两种可能结果（成功或失败）的任务的对象，并持有在其中一种结果发生时触发的回调函数。例如，在 `jQuery 1.4` 版本下，我必须这样写：

```javascript
// Promises/get-1.4.js
$.get('/mydata', {
 success: onSuccess,
 failure: onFailure,
 always: onAlways
});
```

但在 `jQuery 1.5+` 版本下，我可以这样写：

```javascript
// Promises/get-1.5.js
var promise = $.get('/mydata');
promise.done(onSuccess);
promise.fail(onFailure);
promise.always(onAlways);
```

你可能想知道这个改变有何妙处。为什么要在 Ajax 调用触发之后再附加回调函数呢？简而言之：`封装`。如果一个 Ajax 调用有多种效果（触发动画、插入 HTML、锁定/解锁用户输入等），让发起请求的应用程序部分来处理所有这些会显得笨拙。

传递 `Promise` 则要优雅得多。通过传递 `Promise`，你是在宣告：“发生了一件你可能感兴趣的事情。如果你想了解它何时完成，只需给这个 `Promise` 一个回调函数即可。” 并且，与 `EventEmitter` 类似，`Promise` 允许你将处理程序绑定到同一个事件任意多次（`堆叠`）。当一些小功能（如“加载中”动画）在多个 Ajax 调用之间共享时，这大大减少了代码重复。

但使用 `Promise` 的最大优势在于，你可以轻松地从现有的 `Promise` 派生出新的 `Promise`。你可以要求两个代表并行任务的 `Promise`，给你一个 `Promise` 来通知它们同时完成。或者，你可以要求一个代表系列中第一个任务的 `Promise`，给你一个代表系列中*最终*任务的 `Promise`。正如我们很快将看到的，这些操作在 `Promise` 中是自然而然的。

### 3.1 `Promise` 的简短历史

`Promise` 以多种形式存在于许多语言中。这个术语最早由 `Xanadu` 项目（Web 的前身）的 `C++` 工程师使用。后来 `Promise` 被用于 `E` 编程语言，这启发了 Python 开发者以 `Twisted` 框架的 `Deferred` 形式实现了它们。

`Promise` 在 `2007` 年进入 `JavaScript` 的主流视野，当时 `Dojo` 框架借鉴 `Twisted`，添加了一个名为 `dojo.Deferred` 的对象。当时，相对成熟的 `Dojo` 在流行度上与新兴的 `jQuery` 框架相匹敌。`2009` 年，`Kris Zyp` 在 `dojo.Deferred` 的影响下，提出了 `CommonJS Promises/A` 规范。¹ 同一年，`Node.js` 首次亮相。`Node` 的早期迭代在其非阻塞 API 中使用了 `Promise`。然而，在 `2010` 年 `2` 月，`Ryan Dahl` 决定切换到现在熟悉的 `callback(err, results...)` 格式，理由是 `Promise` 是一种属于“用户层”的高级抽象。

这一决定为针对 `Node` 的竞争性 `Promise` 实现开辟了道路，特别是 `Kris Kowal` 的 `Q.js`² 和 `AJ ONeal` 的 `Futures`。³（在常用术语中，`Promise`、`Deferred` 和 `Future` 大致同义。）`Q` 是 `Promises/A` 规范的一个相当直接的实现。`Futures` 是一个更广泛的工具包，包含了像 `Async.js` 这样的库中发现的许多流程控制功能。

但 `Promise` 今天如此受关注的原因，当然是 `jQuery`。伴随着 `2011` 年 `1` 月对 `$.ajax` 的重大重写，`jQuery 1.5` 的 `Promise` 实现让无数第一次接触 `Promise` 的开发者感到兴奋。然而，其他人则因为 `Promises/A` 规范被忽视，导致了微妙的 `API` 差异而感到沮丧。

在本章的其余部分，我们将专注于 `jQuery Promise`，除了[第 3.7 节 `jQuery 与 Promises/A`，第 43 页](#)。我们还将从 `jQuery` 中汲取词汇，特别是我们将在下一节看到的 `Deferred` 与 `Promise` 的区别，以及将“resolve”用作“reject”的反义词。

### 3.2 创建 `Promise`

我们通过展示 `jQuery 1.5+` 中的 Ajax 方法（`$.ajax`、`$.get` 和 `$.post`）如何返回 `Promise` 来开始本章。但为了真正理解 `Promise`，我们需要自己创建一些。

让我们给用户一个提示，按下 `Y` 或 `N`。我们要做的第一件事是创建一个代表用户决定的 `$.Deferred` 实例。

```javascript
var promptDeferred = new $.Deferred();
promptDeferred.always(function(){ console.log('做出了选择：'); });
promptDeferred.done(function(){ console.log('开始游戏...'); });
promptDeferred.fail(function(){ console.log('今天不玩游戏。'); });
```

（注意：`always` 仅在 `jQuery 1.6+` 中可用。）

你可能想知道为什么在这个名为“创建 `Promise`”的部分我创建了一个 `Deferred` 实例。别担心——`Deferred` 就是一个 `Promise`！更准确地说，它是 `Promise` 的超集，增加了一个关键特性：*你可以直接触发一个 `Deferred`*。纯粹的 `Promise` 只允许你添加更多回调；必须由其他东西来触发它们。

---

¹ `http://wiki.commonjs.org/wiki/Promises/A`

² `https://github.com/kriskowal/q`

³ `https://github.com/coolaj86/futures`

我们可以通过 `resolve` 和 `reject` 方法来触发我们的 `Deferred`。

```javascript
$('#playGame').focus().on('keypress', function(e) {
  var Y = 121, N = 110;
  if (e.keyCode === Y) {
    promptDeferred.resolve();
  } else if (e.keyCode === N) {
    promptDeferred.reject();
  } else {
    return false;  // our Deferred remains pending
  }
});
```

你可以在 [http://jsfiddle.net/TrevorBurn/Pj6Bf/](http://jsfiddle.net/TrevorBurn/Pj6Bf/) 看到这个实际示例。加载页面并按 `Y` 键。控制台会显示如下内容：

> < A choice was made:

  Starting game...

你看到发生了什么吗？当 `Deferred` 被 `resolve` 时，它的 `always` 和 `done` 回调都被执行了。（并非巧合，这些回调是按照它们绑定的顺序执行的。）

刷新页面并按 `N` 键。

> < A choice was made:

  No game today.

所以，当 `Deferred` 被 `reject` 时，它的 `always` 和 `fail` 回调被执行了。注意回调总是按照它们绑定的顺序执行。如果 `always` 回调最后被绑定，控制台的输出顺序就会反过来。

试着反复按 `Y` 和 `N`。在第一次选择之后，就没有效果了！这是因为 `Promise` 只能被 `resolve` 或 `reject` *一次*；在那之后，它就处于惰性状态了。我们说一个 `Promise` 处于 `pending`（挂起）状态，直到它被 `resolve` 或 `reject`。你可以通过调用 `state` 方法来全局检查一个 `Promise` 是 `"pending"`（挂起）、`"resolved"`（已解决）还是 `"rejected"`（已拒绝）。（但是，在 `jQuery 1.7` 及更早版本中，使用 `isResolved` 和 `isRejected`。）

当你执行一个具有两种广泛结果的一次性异步操作（例如，成功/失败 或 接受/拒绝）时，创建一个 `Deferred` 可以给你一个直观的表示。

## 创建纯 `Promise`

我们刚刚了解到 `Deferred` 就是一个 `Promise`。那么，我们如何获得一个不是 `Deferred` 的 `Promise` 呢？很简单：调用 `Deferred` 的 `promise` 方法。

## 两种术语的故事

你可能已经注意到，我一直在说当我 `resolve` 或 `reject` 一个 `Promise` 时，我“触发”了它，而一个已经被 `resolve` 或 `reject` 的 `Promise` 已经被“触发”了。这是一个非标准的术语，但我将在本章中一直使用它。不幸的是，`jQuery` 缺乏一个简洁的术语来描述一个已经被 `resolve` 或 `reject` 的 `Promise`，除了冗长的 `"nonpending"`（非挂起）。

一个更合理的术语用在 `Promises/A` 规范及其实现中：`Promise` 要么被 `fulfilled`（履行），要么被 `rejected`（拒绝）；无论是哪种情况，它都是 `resolved`（已解决）。我们将在 [Section 3.7, jQuery vs. Promises/A, on page 43](Section%203.7,%20jQuery%20vs.%20Promises/A,%20on%20page%2043) 中了解更多相关内容。

```javascript
var promptPromise = promptDeferred.promise();
```

`promptPromise` 只是 `promptDeferred` 的一个副本，没有 `resolve/reject` 方法。无论我们是将回调绑定到 `Deferred` 还是它的 `Promise` 上，都没有关系，因为它们内部共享相同的回调。它们也共享相同的状态（`"pending"`、`"resolved"` 或 `"rejected"`）。这意味着为一个 `Deferred` 创建多个 `Promise` 是没有意义的。事实上，jQuery 只会给你相同的对象。

```javascript
var promise1 = promptDeferred.promise();
var promise2 = promptDeferred.promise();
console.log(promise1 === promise2);  // true
```

而在纯 `Promise` 上调用 `promise` 只会给你一个指向同一对象的引用。

```javascript
console.log(promise1 === promise1.promise());  // true
```

使用 `promise` 方法的唯一原因是封装。如果我们传递 `promptPromise` 但将 `promptDeferred` 保留给自己，我们可以确信，在我们希望它们触发之前，我们的任何回调都不会触发。

重申一下，每个 `Deferred` 都包含一个 `Promise`，每个 `Promise` 都代表一个 `Deferred`。当你有一个 `Deferred` 时，你控制它的状态。当你有一个纯 `Promise` 时，你只能读取该状态并附加回调。

## `jQuery` `API` 中的 `Promise`

我在本章开头以 `jQuery` 的 Ajax 函数（`$.ajax`、`$.get` 和 `$.post`）返回的 `Promise` 为例。Ajax 是 `Promise` 的完美用例：每次调用远程服务器要么成功要么失败，而你想不同地处理这些情况。但 `Promise` 对于本地异步操作同样有用，比如动画。



# Chapter 3. Promises and Deferreds

在 jQuery 中，你可以将回调传递给任何动画方法，以便在其完成时收到通知。

```javascript
$('.error').fadeIn(afterErrorShown);
```

```javascript
var $flash = $('.flash');
var showPromise = $flash.show();
var hidePromise = $flash.hide();
```

在 jQuery 1.6+ 中，你可以改为向 jQuery 对象请求一个 Promise，它代表其当前和待处理动画的完成。

```javascript
var errorPromise = $('.error').fadeIn().promise();
errorPromise.done(afterErrorShown);
```

应用于同一 jQuery 对象的动画会排队顺序执行，而 Promise 只会在你调用 `promise` 时队列中的所有动画都 resolve 时才 resolve。所以，这会生成两个不同的 Promise，它们将按顺序 resolve（或者根本不会，如果先调用 `stop` 的话）。

jQuery 1.8 在 jQuery 中增加了一个更多的 Promise 来源：`$.ready.promise()` 给你一个 Promise，它在文档就绪时 resolve。这意味着下面这些现在是等效的：

```javascript
$(onReady);
$(document).ready(onReady);
$.ready.promise().done(onReady);
```

在本书付印前不久发布的 jQuery 1.8 中，动画 Promise 已经成为更强大的对象。Promise 附带了额外的信息，包括 `props`，即动画正在移动的计算值——对调试非常有价值。你还可以获取进度通知（参见 Section 3.4, Progress Notifications, on page 38）并即时调整动画。这套新功能的草案文档可以在 `https://gist.github.com/54829d408993526fe475` 找到。

在本节中，我们看到了如何获得 jQuery Promise：要么你创建一个 `$.Deferred` 实例，得到一个你控制的 Promise；要么你进行一个返回 Promise 的 API 调用。在接下来的几个小节中，我们将看到你能用所有这些 Promise 做什么。

## 3.3 向回调传递数据

Promise 可以给它的回调提供额外的信息。例如，这两个 Ajax 代码片段是等效的：

```javascript
// Using a callback directly
$.get(url, successCallback);

// Binding a callback to a Promise
var fetchingData = $.get(url);
fetchingData.done(successCallback);
```

当你 resolve 或 reject 一个 Deferred 时，你提供的任何参数都会传递给相应的回调。

```javascript
var aDreamDeferred = new $.Deferred();
aDreamDeferred.done(function(subject) {
    console.log('I had the most wonderful dream about', subject);
});
aDreamDeferred.resolve('the JS event model');
```

> I had the most wonderful dream about the JS event model

还有一些特殊方法可以在特定的上下文中运行回调（即将 `this` 设置为特定的值）：`resolveWith` 和 `rejectWith`。只需将上下文作为第一个参数传入，并将所有其他参数作为数组传入。

```javascript
var slashdotter = {
    comment: function(editor){
        console.log('Obviously', editor, 'is the best text editor.');
    }
};
var grammarDeferred = new $.Deferred();
grammarDeferred.done(function(verb, object) {
    this[verb](object);
});
grammarDeferred.resolveWith(slashdotter, ['comment', 'Emacs']);
```

> Obviously Emacs is the best text editor.

不过，必须将参数包裹在数组中是很麻烦的。所以，这里有一个实用提示：与其使用 `resolveWith`/`rejectWith`，不如直接在所需的上下文中调用普通的 `resolve`/`reject`。这是因为 `resolve`/`reject` 会将它们的 `this` 上下文直接传递给它们触发的回调。所以，在前面的例子中，我们可以通过以下方式达到相同的结果：

```javascript
grammarDeferred.resolve.call(slashdotter, 'comment', 'Emacs');
```

## 3.4 进度通知

Promise 是一束你希望在某个过程结束时发生的事情。但是，难道没有一张励志海报曾经告诉过你，旅程和目的地同样重要难？你从那张海报上什么都没学到吗？

幸运的是，jQuery 团队吸收了那句智慧（以及 Promises/A 规范），并在 jQuery 1.7 中增加了一种新的 Promise 回调，它可以被调用任意次数。它叫做 progress。例如，假设我们想更新一个指示器，显示一个人在 National Novel Writing Month (NaNoWriMo) 4 中距离每日字数目标的进度。

```javascript
var nanowrimoing = $.Deferred();
var wordGoal = 5000;
nanowrimoing.progress(function(wordCount) {
    var percentComplete = Math.floor(wordCount / wordGoal * 100);
    $('#indicator').text(percentComplete + '% complete');
});
nanowrimoing.done(function(){
    $('#indicator').text('Good job!');
});
```

有了 `nanowrimoing` Deferred，以下是我们如何响应字数的潜在变化：

```javascript
$('#document').on('keypress', function(){
    var wordCount = $(this).val().split(/\s+/).length;
    if (wordCount >= wordGoal) {
        nanowrimoing.resolve();
    };
    nanowrimoing.notify(wordCount);
});
```

Deferred 上的 `notify` 调用会调用我们的 `progress` 回调。就像 `resolve` 和 `reject` 一样，`notify` 可以接收任意参数。注意，一旦 `nanowrimoing` 被 resolve，对 `nanowrimoing.notify` 的调用将没有效果，就像任何额外的 `resolve` 和 `reject` 调用会被忽略一样。

所以，总结一下，Promise 接收三种回调：`done`、`fail` 和 `progress`。`done` 回调在 Promise resolve 时运行，`fail` 回调在它 reject 时运行，而 `progress` 回调在 pending Deferred 上调用 `notify` 时随时运行。

# 3.5 组合 Promise

进度通知的存在并不改变这样一个事实：归根结底，每个 Promise 要么被解决（resolved），要么被拒绝（rejected）。（或者，永远保持待定状态。）但为什么呢？为什么不让 Promise 在任何时候变成任何状态呢？

Promise 被设计成这样，主要是因为程序员在*二元性*上如鱼得水。我们完全知道如何将 1 和 0 组合起来，完成令人惊叹的逻辑壮举。这就是 Promise 如此强大的一个重要原因；它们让我们将任务视为布尔值。

逻辑组合 Promise 最常见的用例是确定一组异步任务何时完成。假设你在加载游戏资源的同时播放教程视频。你想在两件事都发生之后立即开始游戏，不论先后顺序。

- 教程视频已结束。
- 游戏已加载完毕。

假设每项进程都对应一个 Promise，你的任务是在两个 Promise 都被解决时启动游戏。你会怎么做？

这就引出了 jQuery 的 `when` 方法。

```javascript
var gameReadying = $.when(tutorialPromise, gameLoadedPromise);
gameReadying.done(startGame);
```

`when` 相当于 Promise 解决的逻辑与（AND）。它生成的 Promise 在所有给定的 Promise 都被解决时解决，或者在任一给定的 Promise 被拒绝时立即拒绝。

`when` 的一个绝佳用例是组合多个 Ajax 调用。如果你需要同时发起两个 POST 请求，并在两者都成功时获得通知，无需为每个请求定义单独的回调。

```javascript
$.when($.post('/1', data1), $.post('/2', data2))
.then(onPosted, onFailure);
```

成功时，`when` 可以访问其每个组成 Promise 的回调参数，但这样做比较棘手。它们以参数列表的形式传递，顺序与 Promise 传给 `when` 的顺序相同。如果一个 Promise 提供多个回调参数，这些参数会被转换为数组。

因此，要获取传给 `$.when` 的所有 Promise 的所有回调参数，你可以这样写（但我不推荐这样做）：

```javascript
$.when(promise1, promise2)
.done(function(promise1Args, promise2Args) {
    // ...
});
```

在这个例子中，如果 `promise1` 以单个参数 `'complete'` 解决，而 `promise2` 以参数 `1, 2, 3` 解决，那么 `promise1Args` 就是字符串 `'complete'`，而 `promise2Args` 则是数组 `[1, 2, 3]`。

虽然这是可行的，但如果你不是绝对必要，就不应该解析 `when` 的回调参数。相反，应将回调直接附加到传给 `when` 的 Promise 上，以收集它们的结果。

```javascript
var serverData = {};
var getting1 = $.get('/1')
.done(function(result) {serverData['1'] = result;});
var getting2 = $.get('/2')
.done(function(result) {serverData['2'] = result;});
$.when(getting1, getting2)
.done(function() {
    // GET 的数据现在都在 serverData 中了……
});
```

# 将函数用作 Promise

`$.when` 以及其他接受 Promise 的 jQuery 方法，允许你传入非 Promise 值。这些值被视为已在相应参数位置上以给定值解决的 Promise。例如，

```javascript
$.when('foo')
```

会给你一个立即以值 `'foo'` 解决的 Promise；下面的代码

```javascript
var promise = $.Deferred().resolve('manchu');
$.when('foo', promise)
```

会给你一个立即以值 `'foo'` 和 `'manchu'` 解决的 Promise；而下面的代码

```javascript
var promise = $.Deferred().resolve(1, 2, 3);
$.when('test', promise)
```

会给你一个立即以值 `'test'` 和 `[1, 2, 3]` 解决的 Promise。（记住，当 Deferred 向 `resolve` 传递多个参数时，`$.when` 会将这些参数强制转换为数组。）

这就引出了一个问题：`$.when` 如何知道一个参数是否是 Promise？原来，jQuery 会检查每个参数是否存在名为 `promise` 的方法；如果存在，jQuery 就使用该方法返回的值。`Promise.prototype.promise` 方法只是返回它自身。

正如你在第 35 页"jQuery API 中的 Promise"中所记得的，jQuery 对象也有一个 `promise` 方法，这意味着 `$.when` 将 jQuery 对象"强制转换"为它们的动画 Promise。因此，如果我们想创建一个 Promise，在我们获取到某些数据且 `#loading` 动画完成时解决，我们只需这样写：

```javascript
var fetching = $.get('/myData')
$.when(fetching, $('#loading'))
```

只需记住，我们必须在启动动画之后再这样做。如果 `#loading` 的动画队列为空，它的 Promise 会立即解决。

## 3.6 用 pipe 绑定未来

在 JavaScript 中，执行一系列异步任务常常很不方便，因为你无法在第一个任务完成之前为第二个任务附加处理程序。例如，让我们从一个 URL 获取（GET）数据，然后将其发布（POST）到另一个 URL。

```javascript
var getPromise = $.get('/query')
getPromise.done(function(data) {
    var postPromise = $.post('/search', data)
})
// 现在 we'd like to attach handlers to postPromise
```

你发现这里的问题了吗？在我们 GET 操作完成之前，我们无法为 `postPromise` 绑定回调，因为它还不存在！它是由我们发起 `$post` 调用才创建的，而在我们异步地从 `$.get` 调用获取到数据之前，我们无法发起这个调用。

这就是为什么 jQuery 1.6 为 Promise 添加了 `pipe` 方法。本质上，`pipe` 是这样的："给我一个针对此 Promise 的回调，我会给你一个代表该回调结果的 Promise。"

```javascript
var getPrompt = $.get('/query')
var postPromise = getPromise.pipe(function(data) {
    return $.post('/search', data)
})
```

看起来像黑魔法，对吧？以下是它的工作原理：`pipe` 为每种回调类型各接受一个参数：`done`、`fail` 和 `progress`。所以，在这个例子中，我们只提供了一个在 `getPromise` 解决时运行的回调。`pipe` 方法返回一个新的 `Promise`s`，它在我们的回调返回的 Promise 解决/拒绝时解决/拒绝。

实际上，`pipe` 就是通往未来的窗口！

你也可以使用 `pipe` 来"过滤" Promise，修改回调参数。如果 `pipe` 回调返回的是非 Promise/Deferred 的东西，那么该值就成为回调参数。例如，如果你有一个 Promise 发出 0 到 1 之间数字的进度通知，你可以使用 `pipe` 创建一个相同的 Promise，改为发出人类可读的字符串作为进度通知。

```javascript
var promise2 = promise1.pipe(null, null, function(progress) {
    return Math.floor(progress * 100) + '% complete';
});
```

总结一下，你可以在 `pipe` 回调中做两件事。

- 如果你返回一个 Promise，`pipe` 返回的 Promise 会模仿它。
- 如果你返回非 Promise 值（或什么都不返回），`pipe` 返回的 Promise 会立即根据原始 Promise 刚刚发生的情况，以该值解决、拒绝或通知。

`pipe` 判断某物是否为 Promise 的规则与 `$.when` 相同：如果它有 `promise` 方法，该方法的返回值就被用作代表原始对象的 Promise。同样，`promise.promise() === promise`。

### Pipe 级联

`pipe` 不要求你提供所有可能的回调。事实上，你通常只会写：

```javascript
var pipedPromise = originalPromise.pipe(successCallback);
```

或者：

```javascript
var pipedPromise = originalPromise.pipe(null, failCallback);
```

我们已经看到了当原始 Promise 在第一种情况下成功、或在第二种情况下失败时会发生什么，此时 `pipe` 的 Promise 的行为取决于 `successCallback` 或 `failCallback` 的返回值。但当我们没有为原始 Promise 的行为提供 `pipe` 回调时会怎样呢？



很简单。在这些情况下，被`pip`过的`Promise`会模仿原始`Promise`。我们可以说原始`Promise`的行为级联（cascades）通过了被`pip`过的`Promise`。这种级联非常方便，因为它让我们能够以最小的努力为异步任务定义分支逻辑。假设我们有一个三步流程。

## 3.7 jQuery 与 Promises/A

就功能而言，jQuery Promise 与 Promises/A 几乎完全相同。最受欢迎的 Promises/A 库`Q.js`甚至提供了可与 jQuery Promise 配合使用的方法。这些差异只是表面上的；它们使用相同的词汇，但含义不同。

正如第 3.2 节《创建 Promise》（第 33 页）之前提到的，jQuery 将`resolve`一词用作`fail`的反义词，而 Promises/A 则使用`fulfill`。

在 Promises/A 中，当一个 Promise 被满足或失败时，它被称为已“解决”。

在 1.8 版本发布之前，jQuery 的`then`方法只是同时调用`done`、`fail`和`progress`的简写，而 Promises/A 的`then`则更像 jQuery 的`pipe`。jQuery 1.8 通过将`then`设为`pipe`的同义词纠正了这一点。然而，由于向后兼容性问题，不太可能与 Promises/A 进行进一步的协调。

还有其他一些更微妙的差异。例如，在 Promises/A 中，`then`返回的 Promise 是被满足还是被拒绝，取决于被调用的回调函数是返回值还是抛出错误。（从 jQuery Promise 回调中抛出错误是个糟糕的做法，因为这些错误不会被捕获。）

由于这些问题，你应该尽量避免在同一项目中交互使用多个 Promise 实现。如果你只是从 jQuery 方法获取 Promise，就使用 jQuery Promise。如果你使用另一个给你 CommonJS Promise 的库，就采用 Promises/A。`Q.js`使得“同化” jQuery Promise 变得非常简单。

```
var qPromise = Q.when(jqPromise);
```

只要这两个标准保持分歧，这就是让它们协同工作的最佳方式。更多信息，请参阅 [Q.js 文档](https://github.com/kriskowal/q)。<sup>5</sup>

## 3.8 用 Promise 替代回调

在理想的世界里，每个启动异步任务的函数都会返回一个 Promise。不幸的是，大多数 JavaScript API（包括所有浏览器和 Node.js 中可用的原生函数）都是基于回调的，而不是基于 Promise 的。在本节中，我们将看到如何将 Promise 与基于回调的 API 结合使用。

将 Promise 与基于回调的 API 结合使用的最直接方法是创建一个 Deferred，并将其触发函数作为回调参数传递。例如，对于像`setTimeout`这样的简单异步函数，我们会传递我们 Deferred 的`resolve`方法。

```
var timing = new $.Deferred();
setTimeout(timing.resolve, 500);
```

在可能发生错误的情况下，我们会编写一个回调函数，根据条件路由到`resolve`或`reject`。例如，以下是我们如何处理 Node 风格回调的方式：

```
var fileReading = new $.Deferred();
fs.readFile(filename, 'utf8', function(err) {
  if (err) {
    fileReading.reject(err);
  } else {
    fileReading.resolve(Array.prototype.slice.call(arguments, 1));
  };
});
```

（是的，你可以从 Node 中使用 jQuery。只需`npm install jquery`并像使用任何其他模块一样使用它。也有一个独立的 jQuery 风格 Promise 实现，简单地称为 Standalone Deferred。<sup>6</sup>）

每次这样写会很麻烦，为什么不创建一个实用函数，从任何给定的 Deferred 生成一个 Node 风格的回调呢？

```
deferredCallback = function(deferred) {
  return function(err) {
    if (err) {
      deferred.reject(err);
    } else {
      deferred.resolve(Array.prototype.slice.call(arguments, 1));
    };
  };
}
```

有了这个，我们可以将之前的例子写成：

```
var fileReading = new $.Deferred();
fs.readFile(filename, 'utf8', deferredCallback(fileReading));
```

在`Q.js`中，Deferred 开箱即带有一个`node`方法来处理这个。

```
var fileReading = Q.defer();
fs.readFile(filename, 'utf8', fileReading.node());
```

随着 Promise 越来越流行，越来越多的 JavaScript 库将效仿 jQuery 的做法，在其异步函数中返回 Promise。在此之前，只需几行代码，你就可以将任何想要使用的异步函数转变为 Promise 生成器。

## 3.9 我们学到了什么

在我看来，Promise 是多年来添加到 jQuery 中最令人兴奋的特性之一。它们不仅极大地帮助我们理顺了典型 Ajax 密集型应用中常见的回调地狱，而且也使协调各种异步任务变得更加容易。

使用 Promise 需要一些练习，尤其是在使用`pipe`时，但这是一个值得培养的好习惯。你将窥见 JavaScript 的未来。返回 Promise 的 API 越多，它们就越有吸引力。

微软已宣布 Windows 8 的 Metro 环境将拥有一个基于 Promise 的 JavaScript API。<sup>7</sup> 时尚开发者和微软都去的地方，世界其他地方也必然会跟随。

# 第 4 章 使用 Async.js 进行流控制

到目前为止，本书一直在讨论使用抽象来管理整个应用程序中的异步任务。例如，PubSub 是一种抽象，允许我们将事件从其源分发到应用程序的其他层（例如，从视图到模型）。Promise 是一种抽象，允许我们使用可组合的对象来表示简单任务，以表示复杂任务。这些抽象在帮助我们解决回调地狱问题方面大有帮助。

然而，我们的盔甲中仍有一个弱点：迭代。当我们需要执行一系列 I/O 操作时，无论是串行还是并行，我们该怎么办？这在 Node 世界中是一个非常普遍的问题，它有一个名字：*流控制*（也称为*控制流*）。就像 Underscore.js 可以极大地简化（同步）迭代代码一样，一个好的流控制库可以从你的异步代码中剥离掉样板代码。

其中最受欢迎的库是 Caolan McMahon 强大的 Async.js。<sup>1</sup> 事实上，在撰写本文时，Async.js 是 npm 注册表中第三大最常被依赖的库，<sup>2</sup> 与 Underscore.js 和 Express 等明星库共享聚光灯。

在本章中，我们将探索 Async.js 在 Node 环境中的功能。（Async.js 也可以在浏览器中运行，但很少有客户端应用需要它。）我们还将简要地看一下另一个替代库，Tim Caswell 的简洁 Step。<sup>3</sup>

## 安装 Node 和 Async.js

要跟上本章内容，请从 [http://nodejs.org/](http://nodejs.org/) 获取最新版的 Node。安装后，你应该能够运行`npm`，即 Node 包管理器。使用此命令安装 Async.js 和 Step：

```
npm install -g async step
```

然后使用`node file.js`运行任何 JavaScript 文件。

## 4.1 Async 排序问题

假设我们想要按字母顺序读取`recipes`目录中的所有文件，然后将它们的内容连接成一个字符串并显示出来。使用同步方法，我们可以相当轻松地完成这项工作。

```
Asyncjs/synchronous.js
var fs = require('fs');
process.chdir('recipes'); // 更改工作目录

var concatenation = '';

fs.readdirSync('.')
  .filter(function(filename) {
    // 忽略目录
    return fs.statSync(filename).isFile();
  })
  .forEach(function(filename) {
    // 将内容添加到我们的输出
    concatenation += fs.readFileSync(filename, 'utf8');
  });

console.log(concatenation);
```

（请注意，`forEach`迭代器在较旧的 JavaScript 环境（如 IE6）中不可用。你可以使用像 Kris Kowal 的`es5-shim`这样的库来解决这个问题。<sup>4</sup> 我们将在第 6 章《异步脚本加载》（第 69 页）中学习如何将此库仅提供给需要它的浏览器。）

但所有这些阻塞都极其低效，特别是如果我们的应用程序可以同时做其他事情。问题在于，我们不能天真地将

```
concatenation += fs.readFileSync(filename, 'utf8');
```

替换为其异步等效代码

---

<sup>5</sup> https://github.com/kriskowal/q

<sup>6</sup> https://github.com/Mumakil/Standalone-Deferred

<sup>7</sup> http://msdn.microsoft.com/en-us/library/windows/apps/br211867.aspx

<sup>1</sup> https://github.com/caolan/async

<sup>2</sup> https://npmjs.org/

<sup>3</sup> https://github.com/creationix/step

<sup>4</sup> https://github.com/kriskowal/es5-shim/

## 4.2 异步收集方法

由于无法保证`readFile`回调函数的执行顺序与调用它们的顺序一致，因为`readFile`仅仅是告诉操作系统*开始*读取文件。很可能更短的会比更长的文件读得更快。作为结果，被添加到`concatenation`的食谱的顺序是不可预测的。此外，我们还得想办法让`console.log`行在所有回调函数触发后运行。

要使用多个异步任务并获得可预期的结果，我们需要做某些计划。

让我们尝试在不引入任何实用函数的情况下解决这个问题。我能想到的最简单的方法是从上一个回调中运行每个`readFile`调用，同时跟踪到目前为止已触发的回调数以最终显示输出结果。以下是我的实现：

```
fs.readFile(filename, 'utf8', function(err, contents) {
  if (err) throw err;
  concatenation += contents;
});
```

```
Asyncjs/seriesByHand.js
var fs = require('fs');
process.chdir('recipes'); // 更改工作目录
var concatenation = '';

fs.readdir('.', function(err, filenames) {
  if (err) throw err;

  function readFileAt(i) {
    var filename = filenames[i];
    fs.stat(filename, function(err, stats) {
      if (err) throw err;
      if (! stats.isFile()) return readFileAt(i + 1);

      fs.readFile(filename, 'utf8', function(err, text) {
        if (err) throw err;
        concatenation += text;
        if (i + 1 === filenames.length) {
          // 所有文件已读取，显示输出
          return console.log(concatenation);
        }
        readFileAt(i + 1);
      });
    });
  }
  readFileAt(0);
});
```

正如您可能注意到的那样，这比同步版本多了很多代码。当我们使用同步的`filter`和`forEach`方法时，这需要少一半的代码行并阅读起来清晰得多！如果我们能直接放入那些出色迭代方法的异步对应物就好了吗？利用 Async.js，我们可以做到这一点！

### 何时可以抛出异常

您可能会注意到我忽略了自己在第 4 节中关于在第 12 页处理异步错误的建议。从回调函数中抛出异常的写法是不规范的——在生产环境中如此。然而对于像这样的简单示例来说，抛出异常是非常可以的。在不太可能发生代码出错的情况下，`throw`将关闭它并向我们提供一个美好的堆栈跟踪来解释原因。

这里的真正罪过在于相同的错误处理逻辑（`if (err) throw err;`）重复了三次！我们将看到 Async.js 如何在“错误处理的”章节（第 52 页）帮助我们要减少这一重复。

### 使用 Async.js 的功能风格

我们想要用异步等效方法替换用于同步迭代的`filter`和`forEach`方法。Async.js 给出了两个选项：

+   `async.filter`和`async.forEach`，它们并行处理给定的数组

+   `async.filterSeries`和`async.forEachSeries`，按顺序处理给定数组

以并行方式运行我们的异步操作会更快，那么我们为什么要使用 series（系列）方法呢？有两个原因：

+   前述的不可预测排序问题。我们可能会通过将结果存储在数组中然后将其连接起来来解决这个问题，但这是一个额外的步骤

+   Node（或任何其他应用程序进程）可以尝试同时读取的文件数量有限制。如果我们遇到这个限制，操作系统将向我们抛出一个错误。如果我们要按顺序读取文件，就不必处理这种局限性了

所以我们将坚持使用`async.forEachSeries`。以下是我们同步代码的直接改编版本以使用 Async.js 的收集方法：

```
Asyncjs/forEachSeries.js
var async = require('async');
var fs = require('fs');
process.chdir('recipes'); // 更改工作目录

var concatenation = '';

var dirContents = fs.readdirSync('.');

async.filter(dirContents, isFilename, function(filenames) {
  async.forEachSeries(filenames, readAndConcat, onComplete);
});

function isFilename(filename, callback) {
    fs.stat(filename, function(err, stats) {
      if (err) throw err;
      callback(stats.isFile());
    });
}

function readAndConcat(filename, callback) {
  fs.readFile(filename, 'utf8', function(err, fileContents) {
    if (err) return callback(err);
    concatenation += fileContents;
    callback();
  });
}
```

现在我们的代码分成两部分：总体任务（以`async.filter`和`async.forEachSeries`调用的形式）和实施细节（两个迭代函数和一个最终回调的形式）。`filter`和`forEach`不是对应标准功能迭代方法的唯一 Async.js 实用工具，还有以下内容：

-   `reject`/`rejectSeries`，`filter`的反面。

-   `map`/`mapSeries`，用于 1:1 转换。

-   `reduce`/`reduceRight`，在每一步变换一个值。

-   `detect`/`detectSeries`，查找与过滤器匹配的值（检测）。

-   `sortBy`，生成排序副本。

-   `some`，测试是否至少有一个值符合给定标准。

-   `every`，测试所有值是否符合给定标准。

这些方法是 Async.js 的核心，允许你用最少的样板代码执行常见的迭代。在我们转向更高级的方法之前，让我们看看这些方法如何处理错误。

在我们的原始异步代码中，我们有三个`throw`（抛出的内容）。在 Async.js 版本中我们有两个。然而所有的错误仍将抛出异常。Async.js 是这样做的吗？为什么我们不能只做一个`throw`呢？

简而言之，Async.js 遵循 Node 约定，这意味着每个 I/O 回调都是`(err, result)`——除了那些结果是布尔值的回调。Boolean 回调只有`(result)`，这就是我们的`isFilename`迭代器从前面的代码示例中需要独立处理错误的原因。



```js
Asyncjs/forEachSeries.js
function (isfilename(fnname, callback) {
  fs.stat(filename, function (err, stats) {
    if (err) throw err;
    callback(stats.isFile());
  });
}
```

归咎于 Node 的`fs.exists`为设定这一先例。这意味着 Async.js 收集方法的迭代器（`filter`、`reject`、`detect`、`some`、`every`和他们的串联等效版）无法报告错误。

对于所有非布尔型 Async.js 迭代器，传递的值不是`null`或`undefined`给到迭代器的回调立即调用完成该异常（错误）。这就是为什么`readAndConcat`可以无需`throw`的原因。

```js
Asyncjs/forEachSeries.js

function readAndConcat(filename, callback) {
  fs.readFile(filename, 'utf8', function (err, fileContents) {
    if (err) return callback(Error);
    concatenation += fileContents;
    cb() {
      callback();
    }
  });
}
```

因此，如果`callback(err)`从`readAndConcat`得到调用，该`err`将传递至`onComplete`。Async.js 保证`onComplete`只会有一次被调用：要么第一次发生错误，要么所有操作完成后成功完成。

```js
Asyncjs/forEachSeries.js

function onComplete(err) {
  if (err) throw err;
  console.log(concatenatio);
}
```

Node 的错误约定可能对 Async.js 的收集方法不理想。但是对于 Async.js 的所有其他方法，遵循这些 convention 允许错误从各个任务顺利流转到完成回调。我们在下一节中看到更多关于此示例。

## 4.3 使用 Async.js 组织任务

Async.js 的收藏方法解决了将单个异步函数应用到一组数据的问题。然而如果是一组函数而非数据集，我们要如何使用呢？在本章节中我们将探索 Async.js 用于分发异步函数和收集其结果的强大工具之一。

### 运行一个异步系列

假设我们有一个按顺序运行的异步函数的数组。如果不使用实用函，我们必须编写一些如下代码：

```js
funcs[0](function () {
  funcs[1](function () {
    funcs[2](onComplete);
  });
});
```

幸运的是我们有`async.series`和`async.waterfall`（瀑布）。每个都接受一个函数数组（任务列表），并按顺序运行它们，为每一个传递节点风格的回调。两者的区别在于，`async.series`仅提供给任务的回调，而`async.waterfall`也提供来自前一个任务的结果（通过“结果”我意思是传递给它的非错误值）。

让我们看看使用超时进行简单演示的代码。

```js
// Asyncjs/seriesTimers.js
var async = require('异步');

Start = new Date;
async.series([
  Function(callback) {
    setTimeout(Callback, 10O);
  },
  Function(Callback) {
    settimeout(cobCallback, 3OO);
  },
  function(callkack) {
    setTimeotcabbak, 2CO);
  }
], function(Error, resultst) {
  // 显示从开头过去的时间
  console.log('Completedin' + (newDate - start) + 'ms');
});
```

（在此示例中，用`async.series`替换`async.waterfall`不会产生任何影响，因为每个任务的回调都是不带参数运行的。）

完成处理程序将在大约 600 毫秒后运行，因为数组中的每个任务都是按顺序完成的。Async.js 传递给每个任务函数的回调只问：“有没有错误（第一个参数）？如果没有，那么我将收集结果（第二个参数）并运行下一个任务。”

下次当你有一组想要顺序运行的异步函数时，请使用`async.series`或`async.waterfall`。很有可能其中之一就是这项工作的合适工具。

## 并行化异步函数

Async.js 提供了一个与`async.series`对应的并行版本，称为`async.parallel`。与`async.series`一样，它接受一个形式为`function(callback) {...}`的函数数组，以及一个（可选的）完成处理程序，该处理程序在最后一个回调触发后运行。

让我们重复一下 timeout 示例。

```js
// Asyncjs/parallelTimers.js
var async = require('async');
var start = new Date;
async.parallel([
  function(callback) { setTimeout(callback, 100); },
  function(callback) { setTimeout(callback, 300); },
  function(callback) { setTimeout(callback, 200); }
], function(err, results) {
  console.log('Completed in ' + (new Date - start) + 'ms');
});
```

`async.series`需要所有 timeout 的总和才能完成（约 600 毫秒），而`async.parallel`只需要最大的 timeout（约 300 毫秒）。

方便的是，Async.js 将结果按任务数组的顺序传递给完成处理程序，而不是按结果生成的顺序。因此，你可以获得并行的性能优势，而不必担心不可预测性。

与集合方法一起，`async.series`、`async.waterfall`和`async.parallel`是 Async.js 的核心：简单、省时的实用函数，适用于最常见的异步场景。

- 任务数组是静态的。一旦调用了`async.series`或`async.parallel`，就无法添加或删除任务。
- 也无法询问“已经完成了多少任务？”这是一个黑盒，除非你自己从任务中分发更新。
- 你只能选择无并发或无限并发。这在文件 I/O 方面是一个相当大的问题。如果我们要处理数千个文件，我们不想通过串行来降低效率，但如果尝试并行处理所有内容，很可能会让操作系统不堪重负。

Async.js 提供了一个多功能的方法来解决所有这些问题：`async.queue`。

### 理解队列

`async.queue`的基本概念让人联想到 DMV（车管所）；它可以同时处理多个人（最多取决于值班职员的数量），但它不是为每个职员设立单独的队列，而是有一个单一的叫号堆栈。当你到达时，你会得到一个号码。每当一个职员空闲时，该职员就会叫下一个号码。

`async.queue`的接口比`async.series`和`async.parallel`稍微复杂一些。它接受一个称为 worker 的函数（而不是函数数组）和一个并发值（worker 可以同时处理的最大任务数）。然后它返回一个队列，我们可以将任意任务数据推入其中（连同可选的回调）。

下面是一个简单的例子：

```js
// Asyncjs/simpleQueue.js
var async = require('async');

function worker(data, callback) {
  console.log(data);
  callback();
}

var concurrency = 2;
var queue = async.queue(worker, concurrency);
queue.push(1);
queue.push(2);
queue.push(3);
```

无论并发数是多少（只要至少为 1），我们都会得到以下输出：

```text
1
2
3
```

不过在底层还是有区别的：并发数为 2 时，我们需要两次事件队列的遍历。如果是 1，我们需要三次遍历，每行一次。而如果是 3 或更多，我们只需要一次遍历。

并发数为 0 的队列将什么都不做。而如果你想要最大并发数，只需使用`Infinity`。

### 推送任务

虽然`queue.push`与`[].push`同名，但有两个关键区别。

首先：

```js
queue.push([1, 2, 3]);
```

等同于以下内容：

```js
queue.push(1);
queue.push(2);
queue.push(3);
```

这意味着你不能直接使用数组作为任务数据。不过，你可以使用其他任何内容——甚至是函数。事实上，如果你想像使用`async.series`或`async.parallel`那样使用函数数组，你只需要定义一个 worker，将其第二个参数传递给其第一个参数。

```js
function worker(task, callback) {
  task(callback);
}

var concurrency = 2;
var queue = async.queue(worker, concurrency);
queue.push(tasks);
```

其次，你可以在每次 push 时提供一个回调函数；如果这样做，它会直接作为回调参数传递给 worker 函数。因此，例如：

```js
queue.push([1, 2, 3], function(err, result) {
  console.log('Task complete!');
});
```

将会（假设 worker 运行了它的回调）输出`Task complete!`三次。push 回调非常宝贵，因为与`async.series`/`async.parallel`不同，`async.queue`不会在内部存储结果。如果你想要结果，就必须自己捕获它们。

### 处理完成

与`async.series`及其同类方法一样，我们可以给`async.queue`一个完成处理程序。不过，不是将其作为参数传递，而是需要将其作为名为`drain`的属性附加。（想象一个装满未完成任务的浴缸；当最后一个任务流下去时，回调触发。）下面是一个使用定时器的演示：

```js
// Asyncjs/queueTimers.js
var async = require('async');

function worker(data, callback) {
  setTimeout(callback, data);
}

var concurrency = 2;
var queue = async.queue(worker, concurrency);
var start = new Date;

queue.drain = function() {
  console.log('Completed in ' + (new Date - start) + 'ms');
};

queue.push([100, 300, 200]);
```

回想一下，`async.series`需要约 600 毫秒来完成这些 timeout（总和），而`async.parallel`只需要约 300 毫秒（最大值）。这里，并发数为 2，所以最初，前两个 timeout 将并行运行。但当 100 毫秒的 timeout 完成时，队列上的下一个任务（200 毫秒的 timeout）将立即开始。因此，在这种情况下，`async.queue`将在大约与`async.parallel`相同的时间完成。顺序很重要：如果 300 是第三个 timeout，队列将需要约 400 毫秒才能完成。

注意，我们可以随时向队列推送更多任务，而`drain`将每次在队列上的最后一个任务完成时触发。不幸的是，这意味着`async.queue`无法像`async.waterfall`那样为我们提供整齐有序的结果。如果我们想从队列任务中收集数据，就只能靠自己了。

### 高级队列回调

虽然`drain`通常是你唯一需要的处理程序，但`async.queue`还提供了一些其他事件。

- 当最后一个任务开始运行时，队列调用`empty`。（当任务完成时，队列调用`drain`。）
- 当达到并发限制时，队列调用`saturated`。
- 如果你在`push`中提供函数作为第二个参数，它将在给定任务（或给定数组中的每个任务）完成时被调用。

在本节中，我们看到了`async.queue`如何成为 Async.js 中最强大的函数之一。当你需要以有限的并发运行大量异步任务时，请考虑`async.queue`。

这就是我们对 Async.js 的介绍，它是使用最广泛且可以说是功能最丰富的 JavaScript 流程控制库。不过，我不想让你产生 Async.js 是每种回调驱动工作的合适工具的印象。让我们通过看看它的主要竞争对手之一 Step 来结束本章。

## 4.5 使用 Step 进行极简流程控制

Tim Caswell 的 Step 是一个轻量级库。⁵ 事实上，它的 API 只包含一个函数：`Step`。

Step 接受一系列函数；下面是一个例子：

```js
Step(task1, task2, task3);
```

每个函数可以通过三种方式控制流程：

- 它可以调用`this`来让 Step 运行列表中的下一个函数。
- 它可以调用由`this.parallel`或`this.group`生成的回调 n 次，以告诉 Step 将下一个函数运行 n 次。
- 它可以返回一个值，这也会使 Step 运行列表中的下一个函数。这使得同步函数与异步函数混合使用变得很容易。

下一个函数将接收其前驱的结果（即其返回值或传递给`this`的参数），或者如果该前驱是使用`this.parallel`或`this.group`运行的，则接收该前驱所有实例的结果。（区别在于`this.parallel`将这些结果作为单独的参数提供，而`this.group`将它们合并为数组。）

整个库在撰写本文时只有 152 行（含注释），但足以处理大多数异步流程。这种极简主义的缺点是，使用 Step 创建的流程只能通过阅读其中的每个函数来理解。使用“包罗万象”的 Async.js 创建的流程往往更容易自我解释。

不过，如果你想卷起袖子大干一场，用 Step 编写类 Async.js 的实用函数可能是一个很好的练习。例如，下面是等效的`async.map`，只用了十一行：

5. https://github.com/creationix/step

```js
// Asyncjs/stepMap.js
var Step = require('step');

function stepMap(arr, iterator, callback) {
  Step(
    function() {
      var group = this.group();
      for (var i = 0; i < arr.length; i++) {
        iterator(arr[i], group());
      }
    },
    callback
  );
}
```

我发现使用 Step 是一种令人耳目一新的体验。虽然使用 Async.js 主要是为任务找到合适的工具函数，而 Step 则鼓励你清晰地思考问题，并写出优雅、高效的解决方案。

## 4.6 我们学到了什么

在本章中，我们看到了如何使用合适的流程控制函数，以最少的样板代码实现常见的异步模式。Async.js 已成为排名第一的流程控制库，它提供了强大的集合迭代和任务处理方法的组合。如果你有流程控制问题，很可能 Async.js 就有解决方案。或者如果你更倾向于自己动手，可以考虑使用 Step。

Node.js 项目的首席开发者 Isaac Schlueter 开发了一个非常小的流程控制库，名为 Slide，⁶ 该库用于 npm。在 Slide 的 README 中，他写道：

> 你应该将其作为编写自己流程控制工具的示例。你将永远不会完全欣赏一个不是你自己编写的流程控制库。

我希望这不是真的。编写流程控制库是一个很好的练习，但你不必仅仅为了看看它是如何工作的就重新发明轮子。随着 JavaScript 生态系统的成熟，流程控制应该会变得更加普及和标准化。目前，如果你的应用程序需要流程控制，重要的是选择一个好的库并深入学习。

6. https://github.com/isaacs/slide-flow-control

# 第 5 章

## 使用 Worker 进行多线程

在本书的开头，我将事件描述为多线程的一种替代方案。更准确地说，事件取代了一种特定类型的多线程，即应用程序进程的多个部分同时运行（无论是通过中断虚拟运行，还是在多个 CPU 核心上物理运行）。当在不同线程中运行的代码访问相同的数据时，这就会成为问题。即使是像下面这样简单的代码行：

```js
{ i++; }
```

当它允许不同的线程同时修改同一个`i`时，也可能成为棘手的海森堡 bug¹ 的来源。谢天谢地，这种多线程在 JavaScript 中是不可能的。

另一方面，将任务分配到多个 CPU 核心上变得越来越重要，因为这些核心的效率不再像过去那样每年都能实现指数级增长。所以，我们需要多线程。这是否意味着要放弃基于事件的编程呢？

恰恰相反！虽然在单线程上运行并不理想，但将应用程序天真地分布在多个核心上可能更糟糕。当多核系统中的核心必须不断地相互通信以避免冲突时，系统会变得极其缓慢。更好的方法是给每个核心一个单独的任务，然后偶尔同步一下。

这正是 JavaScript 中 Worker 所做的事情。从应用程序的主程序线程，你告诉一个 Worker：“去一个单独的线程运行这段代码。”



`Worker` 可以向你发送消息（反之亦然），这些消息的形式是（还有什么？）从事件队列运行的回调函数。简而言之，你与不同线程交互的方式与在 JavaScript 中进行 I/O 操作的方式相同。

> 1. http://en.wikipedia.org/wiki/Heisenbug

在本章中，我们将研究 `Worker` 在浏览器和 Node 中的实现形式，并讨论一些实际应用。

## 线程与进程

在本章中，我交替使用“线程”和“进程”这两个词。在操作系统级别，有一个重要的区别：进程内的线程可以共享状态，而独立的进程则不能。但在 JavaScript 中，并发代码（由 `Worker` 运行）从不共享状态。因此，`Worker` 可能使用轻量级操作系统线程实现，但它们的行为类似于进程。

有一些 Node 库，最著名的是 Threads-A-GoGo，⁸ 允许你为了效率而打破状态共享的规则。这些内容超出了本章的范围，本章仅关注标准 JavaScript 中的并发。

a. https://github.com/xk/node-threads-a-gogo

## 5.1 Web Workers

Web Worker 是广泛称为 HTML5 的现行标准的一部分。要创建一个 Worker，你需要使用脚本的 URL 调用全局 `Worker` 构造函数。

```javascript
var worker = new Worker('worker.js');
worker.addEventListener('message', function(e) {
  console.log(e.data);  // 回显通过 postMessage 发送的内容
});
```

（通常，我们只关心消息事件的 `data` 属性。如果我们将相同的事件处理程序绑定到多个 Worker，我们可以使用 `e.target` 来确定是哪个 Worker 发出了事件。）

所以，现在我们知道如何监听 Worker。方便的是，与 Worker 通信的接口是对称的：我们使用 `worker.postMessage` 向其发送消息，Worker 使用 `self.addEventListener('message', ...)` 来接收。以下是一个完整的示例：

```javascript
// 主脚本
var worker = new Worker('boknows.js');
worker.addEventListener('message', function(e) {
  console.log(e.data);
});
worker.postMessage('football');
worker.postMessage('baseball');

// boknows.js
self.addEventListener('message', function(e) {
  self.postMessage('Bo knows ' + e.data);
});
```

你可以在一个我创建的小网站 Web Worker Sandbox² 上体验消息传递接口。每次你创建一个新示例时，它都会获得一个唯一的 URL，你可以分享它。

## Web Workers 的限制

Web Worker 主要用于处理复杂计算，同时不损害 DOM 的响应性。潜在用途包括以下方面：

- 使用 H.264 编解码器的 Broadway 实现解码流式视频³
- 使用斯坦福 JavaScript 加密库⁴ 加密通信
- 在基于网络的编辑器中解析文本，如 Ace⁵

事实上，Ace 默认就执行此操作。当你在基于 Ace 的编辑器中输入代码时，Ace 在用适当的语法高亮更新 DOM 之前，需要进行一些相当繁重的字符串分析。在现代浏览器中，该分析在单独的线程上完成，确保编辑器保持流畅和响应性。

通常，Worker 会将其计算结果发送给主线程，主线程再更新页面。为什么不直接更新页面？主要是为了保持 JavaScript 异步抽象的完整性。如果一个 Worker 能够修改页面的标记语言，我们最终会陷入与 Java 相同的境地，需要将 DOM 操作代码包装在互斥锁和信号量中以避免竞态条件。

同样，Worker 无法看到全局 `window` 对象或主线程（或其他 Worker 线程）中的任何其他对象。当一个对象通过 `postMessage` 发送时，它会被透明地序列化和反序列化；可以想象成 `JSON.parse(JSON.stringify(obj))`。因此，对原始对象的更改不会影响另一个线程中的副本。

即使是可靠的 `console` 对象，Worker 也无法访问。Worker 唯一能看到的是其自身的全局对象，称为 `self`，以及与之捆绑的所有内容：标准 JavaScript 对象如 `setTimeout` 和 `Math`，加上浏览器的 Ajax 方法。

啊，是的，Ajax！Worker 可以自由使用 `XMLHttpRequest`。如果浏览器支持，它甚至可以使用 `WebSocket`。这意味着 Worker 可以直接从服务器拉取数据。如果我们处理大量数据（比如需要解码的流式视频），将其保留在一个线程中而不是通过 `postMessage` 序列化，是一个巨大的胜利。

还有一个特殊的 `importScripts` 函数，可以（同步地）加载并运行给定的脚本。

```javascript
importScripts('https://raw.github.com/gist/1962739/danika.js');
```

通常，同步加载是大忌，但请记住我们这里是在一个辅助线程中。只要 Worker 没有其他事情可做，阻塞是完全没问题的。

². http://webworkersandbox.com/

³. https://github.com/nicjohnson145/Broadway

⁴. http://crypto.stanford.edu/sjcl/

⁵. http://ace.ajax.org/

## 哪些浏览器支持 Web Worker？

在桌面端，Web Worker 标准在 Chrome、Firefox 和 Safari 中已经实现多年了，并且 IE10 也支持。移动设备的支持也参差不齐。最新的 iOS Safari 支持它们，但最新的 Android 浏览器则不支持。在撰写本文时，根据 Caniuse.com 的数据，⁶ 这相当于 59.12% 的浏览器支持率。

简而言之，你不能指望你网站的用户都拥有 Web Worker。不过，你可以轻松地编写一个垫片（shim），在 `window.Worker` 不可用时正常运行目标脚本。毕竟，Web Worker 只是一种性能增强。

请务必在多个浏览器中测试 Web Worker，因为它们的实现之间存在一些关键差异。例如，Firefox 允许 Worker 生成它们自己的“子 Worker”，但 Chrome 目前不允许。

## 5.2 使用 cluster 实现 Node Worker

在 Node 的早期，有许多相互竞争的多线程 API。这些解决方案大多很笨拙，要求用户启动多个服务器实例来监听不同的 TCP 端口，然后再通过代理将它们连接到真正的服务器。直到 0.6 版本，才内置了一个标准，允许多个进程绑定到同一个端口：`cluster`。⁷

通常，`cluster` 用于为每个 CPU 核心启动一个进程以获得最佳性能（尽管每个进程是否真正获得自己的核心完全取决于底层操作系统）。

⁶. http://caniuse.com/webworkers

⁷. http://nodejs.org/docs/latest/api/cluster.html

## 第五章

### 多线程/clusterMessage.js

```javascript
var cluster = require('cluster');
if (cluster.isMaster) {
  // 启动工作进程
  var coreCount = require('os').cpus().length;
  for (var i = 0; i < coreCount; i++) {
    var worker = cluster.fork();
    worker.send('Hello, Worker!');
    worker.on('message', function(message) {
      if (message._queryId) return;
      console.log(message);
    });
  }
} else {
  process.send('Hello, main process!');
  process.on('message', function(message) {
    console.log(message);
  });
}
```

输出结果将类似于：

```text
Hello, main process!
Hello, main process!
Hello, Worker!
Hello, Worker!
Hello, main process!
Hello, Worker!
Hello, main process!
Hello, Worker!
```

其中的顺序是不可预测的，因为每个线程都在争相首先执行 `console.log`。（你需要手动按 `Ctrl+C` 来终止进程。）

与 Web Workers 类似，该 API 是对称的，一方调用 `send` 会触发另一方的 `'message'` 事件。但请注意，`send` 的参数（或者更准确地说，是其序列化副本）是直接由 `'message'` 事件提供的，而不是作为 `data` 属性附加的。

请注意主人消息处理器中的这一行：

```javascript
if (message._queryId) return;
```

Node 有时会从工作进程发送自己的消息，这些消息通常看起来像这样：

```json
{ cmd: 'online', _queryId: 1, _workerId: 1 }
```

忽略这些内部消息是安全的，但要知道它们被用于执行一些重要的幕后魔法。最值得注意的是，当工作进程尝试监听 TCP 端口时，Node 使用内部消息来允许端口共享。

### Node 工作进程的限制

在很大程度上，`cluster` 遵循与 Web Workers 相同的规则：有一个主人，有工作进程；它们通过附加字符串或可序列化对象的事件进行通信。然而，虽然工作进程在浏览器中显然是二等公民，但 Node 的工作进程拥有主人的所有权利和特权，除了以下几项（这是值得注意的）：

- 关闭应用程序的能力
- 生成更多工作进程的能力
- 互相通信的能力

这使得主人承担起所有线间通信枢纽的负担。幸运的是，这种不便可以通过像 Roly Fentanes 的 Clusterhub[9](https://github.com/fent/clusterhub) 这样的库来抽象掉。

### 5.3 我们学到了什么

现在还为时过早，但我要说多核 JavaScript 的未来是光明的。对于任何可以拆分成很大程度上独立且只需要定期相互通信的进程的应用程序，工作进程是充分利用最大 CPU 能力的制胜方案。分布式计算从未如此有趣。

## 第六章

### 异步脚本加载

最初，是这样的：

```html
<script src="allMyClientSideCode.js"></script>
```

而这……并不理想。“它应该放在哪里？”开发者们疑惑道。“放在 `<head>` 里？还是 `<body>` 里？”对于脚本繁重的网站，这两种选择都会带来痛苦。`<head>` 中的大型脚本会延迟所有页面渲染，给用户一个“白屏死亡”[1]，直到脚本完全加载。但在 `<body>` 末尾放置大型脚本则会给用户一个毫无生气的、静态的页面，充斥着不起作用的控件和客户端渲染本应出现的空白区域。

解决这个问题的理想方案是对你的脚本进行分类：那些需要页面正确呈现和运行的脚本应该立即加载。可以等待的脚本则可以延迟。但是，如何在确保需要时可用的前提下，以正确的方式延迟这些脚本呢？

在过去的几年里，几种旨在解决此问题的技术已变得普及。在本章中，我们将看看 HTML5 的 `async` 和 `defer` 属性如何提供帮助。我们还将介绍两个流行的脚本加载库：yepnope 和 Require.js。

### Node.js 中的异步加载

> 本章我们将主要关注浏览器端，因为 Node 中的异步模块加载很少有用。Node 曾经提供过 `require` 的异步变体，但在 0.3 版本中移除了。如果你对移除背后的原因感兴趣，请参阅 https://groups.google.com/d/msg/nodejs/y_-LZqltb1A/mmpYlLurqkJ。

[1] 这个术语是由优秀的《JavaScript Performance Rocks》的作者创造的：http://javascriptrocks.com/performance/。

在我们继续之前，有几点重要的注意事项：

- 本章中的技术不适用于内联脚本（直接在页面标记中定义的脚本）。应尽可能避免内联。如果必须内联脚本，请不要尝试在其上使用 `defer` 或 `async` 属性。
- 使用本章中的任何技术时，都不应使用 `document.write`。其在异步加载脚本中的行为是不可预测的。如果你不知道 `document.write` 是什么，那很好。简单来说，它是 DOM 操作中的 GOTO。
- 这不是一份权威指南。为了简洁，我忽略了一些重要的平台特定细节。例如，某些移动浏览器会拒绝缓存超过特定大小的脚本。因此，如果你的目标是这些设备，保持脚本小巧很重要。

页面加载优化是一个丰富的课题，已有整本书籍论述，脚本加载只是其中一个因素。但对于尚未利用异步加载的脚本繁重网站来说，使用本章中的技术可以轻松拾取许多唾手可得的优化点。

### 6.2 重新介绍 `<script>` 标签

冒着夸张的风险，`<script>` 是有史以来最重要的 HTML 标签。不相信吗？想想看，一个完全由单个脚本标签组成的页面可以做任何事情。它可以凭空创建一个文档，加载任何它想要的资源。相比之下，即使是最神奇的没有 `<script>` 标签的页面，其能力也受到极大限制，无法对用户操作做出比 CSS 过渡更复杂的响应。

在现代浏览器中，`<script>` 有两种令人耳目一新的类型：经典型和非阻塞型。在本节中，我们将看到如何使用这两种类型来让你的页面尽可能快地加载。

#### 阻塞脚本的去处

标准的 `<script>` 标签通常被称为阻塞的。这个术语必须在上下文中理解：当现代浏览器遇到一个阻塞的 `<script>` 标签时，它会继续读取文档的后续部分并下载其他资源（脚本和样式表）。但是，它会在脚本完全下载并运行之前，不会评估这些资源。

那么，如果你的文档 `<head>` 中有五个阻塞的 `<script>` 标签，在所有五个脚本被下载并运行完毕之前，用户除了页面标题什么也看不到。此外，在这些脚本运行期间，用户只能看到运行到那部分为止的文档。如果他们想看到位于 `<body>` 中等待呈现的好内容，就必须将一个处理程序绑定到类似 `document.onreadystatechange` 这样的事件上。

正因如此，将脚本放在页面 `<body>` 末尾已成为一种流行做法。这样，用户能更快地看到页面，而脚本也能在无需等待事件触发的情况下看到完整的 DOM。对于大多数脚本来说，这个改动是一个巨大的进步。

但并非所有脚本都一样。在移动脚本位置之前，请自问三个问题：

- 这个脚本是否有可能从 `<body>` 中的内联 JavaScript 直接调用？这一点可能很明显，但值得反复确认。
- 这个脚本是否允许旧版浏览器识别 HTML5 元素？Modernizr² 就是如此，这就是为什么 HTML5 Boilerplate³——最佳实践的典范——将其置于顶部。
- 这个脚本是否会决定页面渲染时的外观？一个例子是 Typekit 的托管字体。如果你将 Typekit 的脚本放在文档末尾，页面上的文本会渲染两次：一次是立即渲染，第二次是在脚本运行后。

如果上述任何一个问题的答案是“是”，那么该脚本就应该放在 `<head>` 中。否则，它应该放在 `<body>` 中。将这两组脚本分别进行压缩和合并，你将得到一个类似这样的文档：

```html
<html>
<head>
  <!-- metadata and stylesheets go here -->
  <script src="headScripts.js"></script>
</head>
<body>
  <!-- content goes here -->
  <script src="bodyScripts.js"></script>
</body>
</html>
```

这对加载时间很有好处，但要注意，它可能会让用户有机会在 `bodyScripts.js` 加载完成之前与页面进行交互。

2. http://modernizr.com/

3. http://html5boilerplate.com/

## 延迟脚本（Deferring Scripts）

在上一节中，我建议将大多数脚本放在 `<body>` 中，因为这样能让用户更快地看到页面，并避免在操作 DOM 之前绑定“就绪”事件的开销。但有一个缺点：在文档完全加载之前，浏览器无法开始加载这些脚本。对于通过慢速连接发送的大型文档，这可能是一个主要的瓶颈。

理想情况下，我们会在文档加载的同时并行加载这些脚本，而不延迟 DOM 渲染。然后当文档就绪时，我们再运行这些脚本，因为它们已在加载期间，并且保持了 `<script>` 标签的顺序。

如果你读到了这里，无疑你对于编写一个自定义的 Ajax 脚本加载器来满足这些要求感到兴奋！但大多数浏览器支持一个更简单的解决方案。

```html
<script defer src="deferredScript.js">
```

添加 `defer` 属性会告诉浏览器：“立即开始加载此脚本，但不要在文档就绪并且所有前面的 `defer` 脚本运行完毕之前运行它。”将延迟脚本放在文档的 `<head>` 中，你可以获得 `<body>` 放置的所有优点，并在大型文档中获得显著的速度提升！



缺点呢？`defer`并非所有浏览器都支持。值得注意的是，截至本文撰写时，即使是最新版的Opera也忽略此属性。⁴ 这意味着，如果你想确保你的延迟脚本在文档加载后运行，你必须将每个脚本的代码包装在类似jQuery的`$(document).ready`中。这可能是值得的，因为大约97%的访客将享受到并行加载的好处，而另外3%的人仍将获得功能完备的JavaScript。

通过`defer`，我们可以通过将`bodyScripts.js`替换为`deferredScripts.js`来改进上一节的页面示例。

```
<html>
<head>
    <!-- metadata and stylesheets go here -->
    <script src="headScripts.js"></script>
    <script defer src="deferredScripts.js"></script>
</head>
<body>
    <!-- content goes here -->
</body>
</html>
```

4. http://caniuse.com/#search=defer

只需记住，重要的是要将`deferredScripts`包装起来，这样在那些不支持`defer`的浏览器中，它就不会在文档就绪事件之后才运行。如果`body`内容超过几KB，这种权衡是值得的。

## 脚本完全并行化（Full Script Parallelization）

如果你是一个硬核的、分秒必争的页面加载发烧友，`defer`对你来说可能听起来像弱鸡。你不想等到所有前面的`defer`脚本都运行完。你当然也不想让这些脚本等到文档就绪才运行，尤其是考虑到你无论如何都得为了Opera使用`$(document).ready`。你只想*尽快*加载这些脚本并*尽快*运行它们。

这就是为什么现代浏览器提供了`async`属性。

```
<script async src="speedyGonzales.js"></script>
<script async src="roadRunner.js"></script>
```

如果`defer`让你想到一个等待文档加载的有序队列，那么`async`应该让你想到无政府状态。前面显示的两个脚本可以以任何顺序运行，并且它们会在JavaScript引擎可用时立即运行，无论文档是否就绪。那么，除了追求速度感之外，你为什么会使用`async`呢？

对于大多数脚本来说，`async`很难推广。它的支持度不如`defer`广泛，因此更少的用户会注意到性能提升。⁵ 而且因为`async`脚本可以在任何时间运行，所以非常容易引入那些依赖于脚本恰好何时加载完成的海森堡缺陷（Heisenbugs）。

但对于那些旨在独立的脚本来说，`async`是一个虽小但显著的胜利。有一个添加反馈小部件的第三方脚本和另一个添加技术支持聊天框的脚本？没有它们页面也能正常运行，而且哪个先运行都无所谓。因此，你可以通过在它们身上使用`async`来获得免费的速度提升。

### 异步 + 延迟 = ？

你可能会问：“如果我在同一个脚本上同时使用`defer`和`async`会怎样？”答案是，在同时支持两者的浏览器中，`async`会覆盖`defer`。由于`defer`支持更广泛，并且提供了`async`的主要好处——允许DOM在脚本下载时渲染——我建议在你使用`async`时也使用`defer`。

5. http://caniuse.com/#search=async

在我们的最后一个页面示例中添加几个独立的小部件，我们得到：

```
<html>
<head>
  <!-- metadata and stylesheets go here -->
  <script src="headScripts.js"></script>
  <script src="deferredScripts.js" defer></script>
</head>
<body>
  <!-- content goes here -->
  <script async defer src="feedbackWidget.js"></script>
  <script async defer src="chatWidget.js"></script>
</body>
</html>
```

这个页面结构使你的优先级非常明确。在绝大多数浏览器中，DOM渲染只会被延迟到`headScripts.js`运行完毕。`deferredScripts.js`将在DOM渲染的同时在后台加载。然后，在DOM渲染之后，`deferredScripts.js`和两个小部件脚本将运行。在支持`async`的浏览器中，这些脚本的运行顺序是不确定的。如果你不确定这是否可以接受，就不要使用`async`！

在本节中，我们了解了`<script>`标签的放置位置和使用属性如何对用户开始使用你页面所需的时间产生重大影响。在下一节中，我们将了解如何通过使用脚本加载其他脚本，将异步加载的原理更进一步。

## 6.3 编程式加载（Programmatic Loading）

虽然`<script>`标签简单而有吸引力，但在某些情况下需要更复杂的脚本加载方法。也许我们希望某个脚本只为满足特定要求的用户加载，例如高级订阅用户或达到一定等级的游戏玩家。或者我们可能希望某个功能，比如聊天小部件，只在用户点击激活时才加载。

在本节中，我们将了解脚本如何加载其他脚本。在简要了解底层方法之后，我们将介绍两个使脚本加载变得轻而易举的流行库：`yepnope`和`Require.js`。

## 直接加载脚本

在浏览器API层面，有两种（合理的）方式可以从服务器获取脚本并运行。

后一种方法更优，因为浏览器会为你处理HTTP请求的工作。此外，`eval`存在实际问题：泄漏作用域、使调试变得混乱，还可能降低性能。因此，要加载一个名为`feature.js`的脚本，我们会插入一个`<script>`标签，代码大致如下：

```
var head = document.getElementsByTagName('head')[0];
var script = document.createElement('script');
script.src = '/js/feature.js';
head.appendChild(script);
```

但是等等——我们如何得知脚本何时加载完毕？当然，我们可以在脚本本身添加一些代码来触发事件，但为每个加载的脚本都添加这段代码将是一件苦差事（或者，对于第三方服务器上的脚本来说，是不可能的）。HTML5规范定义了一个`onload`属性，我们可以将回调绑定到该属性上。

```
script.onload = function() {
  // 现在我们可以调用脚本中定义的函数了
};
```

然而，IE8及更早版本不支持`onload`，它们使用的是`onreadystatechange`。在某些浏览器中插入`<script>`标签时，还有一些奇怪的边缘情况。我甚至还没提到错误处理！为了避免所有这些麻烦，我强烈建议使用脚本加载库。

## 使用yepnope进行条件加载

`yepnope`⁶是一个简单轻量级的库（压缩和gzip后仅1.7KB），旨在满足最常见的动态加载需求，而不花哨。它可以单独使用，也可以作为Modernizr特性检测库的一部分。

在最简单的情况下，`yepnope`加载一个脚本，并在脚本运行后给你一个回调。

```
yepnope({
  load: 'oompaLoompas.js',
  callback: function() {
    console.log('Oompa-Loompas ready!');
  }
});
```

还没被打动？让我们用`yepnope`并行加载多个脚本，并按给定顺序运行它们。例如，假设我们想加载依赖于Underscore.js的Backbone.js。我们只需将两个脚本的位置作为`load`参数的数组提供即可。

```
yepnope({
  load: ['underscore.js', 'backbone.js'],
  complete: function() {
    // Backbone逻辑放在这里
  }
});
```

注意我们这里使用了`complete`而不是`callback`。区别在于`callback`为`load`列表中的每个资源运行，而`complete`只在所有资源都加载完毕后运行。

`yepnope`的标志性特性是*条件加载*。给定一个`test`参数，`yepnope`可以根据该值是否为真值来加载不同的资源。例如，如果你在使用Modernizr，你可以（在一定程度上准确地）判断用户是否使用触摸屏设备，并相应地加载不同的样式表和脚本。

```
yepnope({
  test: Modernizr.touch,
  yep: ['touchStyles.css', 'touchApplication.js'],
  nope: ['mouseStyles.css', 'mouseApplication.js'],
  complete: function() {
    // 无论哪种方式，应用程序现在都准备好了！
  }
});
```

用短短几行代码，我们就为根据用户输入设备提供完全不同的体验奠定了基础。当然，我们不需要为每个条件都同时提供`yep`和`nope`。`yepnope`最常见的用途之一是加载polyfill，以填补旧浏览器缺失的功能。

```
yepnope({
  test: window.json,
  nope: ['json2.js'],
  complete: function() {
    // 现在我们可以安全地使用JSON了
  }
});
```

以下是使用`yepnope`的页面的良好标记结构：

```
<html>
<head>
    <!-- 元数据和样式表放在这里 -->
    <script src="headScripts.js"></script>
    <script src="deferredScripts.js" defer></script>
</head>
<body>
    <!-- 内容放在这里 -->
</body>
</html>
```

看起来很熟悉？这与我们在`defer`部分讨论的结构相同。唯一的区别是`yepnope.js`已被合并到其中一个脚本文件中（可能位于`deferredScripts.js`的顶部），而所有我们需要条件加载（因为浏览器需要polyfill）或想要动态加载（响应用户操作）的内容都可以单独加载。结果应该是一个更小的`deferredScripts.js`。

我喜欢`yepnope`。对于那些只想抓取几个polyfill或在用户点击某处时加载一个功能的相对简单的应用程序来说，`yepnope`几乎完美。然而，对于真正庞大的应用程序，则需要更强大的工具。

## 使用Require.js和AMD进行智能加载

`Require.js`是那些希望将脚本密集型应用程序的混乱转化为更有秩序的开发者们首选的脚本加载器。它是一个强大的包，能够使用AMD自动处理最复杂的依赖关系图。

我们稍后会谈到AMD，但首先让我们看一个使用`Require.js`同名函数的简单脚本加载示例。

```
require(['moment'], function(moment) {
    console.log(moment().format('dddd'));  // 星期几
});
```

`require`函数接受一个脚本名称数组，并行加载所有这些脚本。与`yepnope`不同，`Require.js`并不确保目标脚本按顺序运行。相反，它确保它们运行的顺序使得每个脚本的依赖关系都得到满足，前提是这些脚本是通过异步模块定义（AMD）指定的。

AMD是一个规范⁷，旨在为浏览器实现CommonJS标准为服务器所做的事情。（Node.js模块基于CommonJS标准。）它强制要求一个全局函数（由`Require.js`提供），名为`define`，它接受三个参数：一个名称、一个依赖项列表，以及一个当这些依赖项加载完毕时的回调。例如，这是一个依赖于jQuery的应用程序的有效AMD定义：

```
define('myApplication', ['jquery'], function($) {
    $('<body>').append('<p>Hello, async world!</p>');
});
```

注意，jQuery对象`$`被传递给了回调。事实上，回调总是会收到一个对应于依赖列表中每个项目的参数。你可能想知道`define`是如何知道捕获jQuery对象的。答案是jQuery自己的AMD定义⁸在其`define`回调中返回了jQuery，从而声明“这是我导出的对象。”

```
define( "jquery", [], function () { return jQuery; } );
```

AMD的内容比这稍微多一点，但这就是其精髓。为应用程序中的每个脚本添加AMD定义意味着你可以调用`require`，并放心，你的回调不仅会在你的直接依赖满足时被调用，而且当这些依赖的依赖以及依赖的依赖都满足时也会被调用，所有这些都以最大并行性加载，并按照与依赖关系图一致的顺序运行。

听起来很棒，对吧？但另一方面：虽然AMD在JavaScript社区中获得了一些支持，但也有很多怀疑者。例如，Jeremy Ashkenas拒绝为他流行的Underscore.js和Backbone.js库添加必要的样板代码，等待着一个预期的ECMAScript模块标准。因此，你不能指望第三方模块有自己的AMD定义。选择AMD可以使你的应用程序更一致，但也可能是样板代码的配方。

在最后几页中，我们了解了如何通过DOM操作在运行时加载脚本，并研究了两个简化此过程的库：`yepnope`，一个小而精确的工具；以及`Require.js`，一个大而强大的工具。你最终选择哪个取决于你正在开发什么样的应用程序以及你是什么样的开发团队。应用程序越“企业化”，前端团队越大，你就越有可能从`Require.js`所鼓励的AMD风格模块化中受益。

⁷. https://github.com/amdjs/amdjs-api/wiki/AMD

⁸. 参见 https://github.com/jquery/jquery/blob/master/src/exports.js#L17.

## 我们学到了什么

你可以通过异步加载那些不需要立即使用的脚本，使你的网站运行得更快。最简单的方法是明智地使用`defer`和`async`属性。如果你需要条件加载脚本，请考虑使用像`yepnope`这样的加载器。如果你的网站有大量相互依赖的脚本，请仔细研究一下`Require.js`。选择适合这项工作的工具，拥抱它，并享受它。

说到这里，我们已经到达了本书的结尾。感谢你花时间阅读它。能为您写作是我的荣幸。无论你的JavaScript之旅将你带向何方，我都希望它充满了优美、事件驱动的代码。

## 附录 1：驯服 JavaScript 的工具集

本章是对在同步风格中编写异步 JavaScript 代码的一些更流行的工具的概览。这些工具中没有哪一种是替代对 JavaScript 事件进行透彻理解的；相反，它们可以通过给您的异步技能库增加一些技巧来补充这种理解。

### A1.1 TameJS

OkCupid团队创造了一个巧妙的预编译器（拥有超过600名 GitHub关注者（http://tamejs.org/）），它为JavaScript增添了两个关键字：`await`和`defer`。一个`await block`定义了不会返回的代码，直到每个使用`defer`定义的异步任务都已完成为止。

```
await {
    setTimeout(defer(), 100);
}
console.log("this will run after the 100ms timeout");
```

TameJS团队还创造了一个具有相同`await/defer`机制的CoffeeScript分支，名为IcedCoffeeScript（http://maxtaco.github.com/coffee-script/）。

### A1.2 StratifiedJS

StratifiedJS（http://onilabs.com/stratifiedjs）是等待/`await/defer`范式的一个替代品，它提供了更细粒度的控制结构，并使用了像`waitfor`和`resume`这样直观的名称。

```
console.log('this code will run right away...');
waitfor() {
    setTimeout(resume, 500);
}
console.log('...and this will run 500ms later.');
```

虽然并没有被广泛使用，但StratifiedJS是一项雄心勃勃的项目，已经得到了像John Resig（jQuery的创建者）¹这样的赞誉。**²**注意：StratifiedJS是规范的名字，而不是实现；官方的参考实现称为Oni Apollo。³

### A1.3 Kaffeine

Kaffeine是一个自诩为“扩展 JavaScript”⁴的预编译器。除了其他功能外，该语言提供简单句法糖来取消回调嵌套：只需在异步函数名之后添加`!`。Kaffeine假设函数的最后一个参数是回调函数，并简单地将该调用之后的所有代码转换为回调。

例如，在一个jQuery应用程序中，通常希望在`$`回调内运行所有内容（准备就绪后）。使用Kaffeine可以轻松做到这一点。

```
$!()
alert('The document is ready.');
```

虽然它并没有CoffeeScript那样大的拥护者，但这些功能使得检查Kaffeine非常值得一试。Coco和LiveScript这两个CoffeeScript分支具有类似的功能，将其称为`backcalls`。在Coco/LiveScript中，前面的示例将写成这样：

```
<-$ 
alert 'The document is ready'
```

Kaffeine/Coco/LiveScript的方法提供了TameJS/StratifiedJS的大部分功能，但学习曲线更平缓。

### A1.4 Streamline.js



与Kaffeine一样，`Streamline.js`⁵提供了一种特殊语法，可将异步函数调用后的代码转换为其回调。只需使用`_____`来代替回调参数即可。

```javascript
for (var s = 1; s < 60; s++) {
  setTimeout(_, 1000);
  console.log(s + ' seconds have elapsed');
}
console.log('1 minute has elapsed');
```

---

1. https://twitter.com/jeresig/statuses/164496725254479872
2. https://github.com/onilabs/apollo
3. http://weepy.github.com/kaffeine/index.html
4. https://github.com/Sage/streamlinejs

有趣的是，`Streamline`可以生成标准的回调驱动JavaScript代码或用于`node-fibers`的基于纤程的代码（见下一节）。此外，与大多数其他JavaScript预编译器不同，`Streamline`可以与`CoffeeScript`一起使用。

注意：`Streamline`期望回调遵循Node风格的参数列表约定`(err, results...)`，这简化了Node中的错误处理，但在浏览器开发中使用时却比较困难。

### A1.5 Node-Fibers

而本列表中列出的其他项目仅仅编译为纯JavaScript，但`node-fibers`实际上扩展了解释器运行的语言理解范围，添加了类线程结构称为*纤程 (`http://en.wikipedia.org/wiki/Fiber_(computer_science)`)*⁶。一个纤程可以让渡给其他纤程，挂起自身的执行直到某个事件使其再次运行。

```javascript
var fiber = Fiber.current;
console.log('Yielding until the timeout elapses...')
setTimeout(function() {
  fiber.run();
}, 1000);
Fiber.yield();
console.log('...1 second later');
```

`node-fibers`相对于JavaScript预编译器的主要优势在于调试。`node-fiber`堆栈跟踪中的行号对应于`node-fiver`源代码中的行号，并且即使纤程在`try/catch`块内挂起时也能捕获抛出的异常。

### A1.6 JavaScript的未来：生成器（Generators）

ECMAScript的最新版本（所有主流JavaScript运行时实现的规范）定义了一种新的JavaScript功能，称为*generators*（生成器）。一个生成器是包含`yield`语句的特殊类型函数。`yield`类似于`return`，除了生成器在下一次运行时将从该`yield`语句处恢复。

从概念上讲，生成器有点棘手。然而，Mozilla的`Task.js`（`http://taskjs.org/`）库展示了它们如何让异步代码更简单。因为生成器可以恢复执行，所以您可以编写如下代码：

```javascript
task.spawn(function() {
  console.log("Yielding...");
  yield task.sleep(1000);
  console.log("...resuming 1 second later");
});
```

以下是代码工作原理的说明：`task.spawn`运行我们的生成器，它只是一个普通函数，除了包含`yield`之外。`task.sleep`返回一个`Promise`（参见第3章，*Promises and Deferreds*，第31页），它在1000ms后解决。`task.spawn`将该`Promise`接收并将其附加为`our generator`的解析回调。当`Promise`解决时，我们的生成器再次被调用，从`yield`处恢复。听起来可能很复杂，但它运作得非常完美。

ECMAScript 6（也称为Harmony）尚未最终确定。目前，生成器的唯一重大实现是在Firefox浏览器中，并且只有在您的`<script>`标签中指定JavaScript版本至少为1.7时才启用，如下所示：

```html
<script type="application/javascript;version=1.7">
```

如果您被生成器所吸引⁷，则有一个工具可以允许您将使用生成器的代码（以及其他ECMAScript 5+功能）编译为广泛支持的JavaScript代码：Google的`Traceur`。⁸

---

8. http://code.google.com/p/traceur-compiler/

## The Pragmatic Bookshelf（实用书柜）

`The Pragmatic Bookshelf`收录了由开发人员为开发人员撰写的书籍。这些标题延续了著名的Pragmatic Programmer风格，并继续赢得奖项和好评。随着开发变得越来越困难，实用的程序员们将提供更多产品和服务帮助您保持领先的游戏水平。（注：根据原文语境，此处“Pragmatic Programmers”指代该团队或品牌）

### 在线访问我们（Visit Us Online）

**本书主页（This Book's Home Page）**

[http://pragprog.com/titles/tbajs](http://pragprog.com/titles/tbajs)

来自本书的源代码勘误表和其他资源。来给我们反馈吧！

**注册更新通知（Register for Updates）**

[http://pragprog.com/updates](http://pragprog.com/updates)

当有新的更新和新书出版时随时收到通知。

### 加入社区（Join the Community）

```text
[http://pragprog.com/community](http://pragprog.com/community)
```

阅读我们的博客，参加在线讨论，参与我们的邮件列表，与我们的wiki互动，并从其他实用程序程序员的经验中受益。（注：原文可能意指“Pragmatic Programmers”作为群体名称，此处保留翻译一致性）。

**新颖和值得关注（New and Noteworthy）**

[http://pragprog.com/news](http://pragprog.com/news)

了解最新的务实发展、新书和其他产品。

### 购买此书（Buy the Book）

如果您喜欢这本电子书，也许您想拥有这本书的纸质副本。您可以在我们的商店购买：[http://pragprog.com/titles/tbajs](http://pragprog.com/titles/tbajs)

### 联系我们（Contact Us）

在线订购： [http://pragprog.com/catalog](http://pragprog.com/catalog)

客户服务： [support@pragprog.com](mailto:support@pragprog.com)

国际版权： [translations@pragprog.com](mailto:translations@pragprog.com)

学术使用： [academic@pragprog.com](mailto:academic@pragprog.com)

写给我们要约： [http://pragprog.com/write-for-us](http://pragprog.com/write-for-us)

或者致电：+1 800-699-7764
