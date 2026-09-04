
# HTML5 Web Workers - 高性能 Web 应用多线程 JavaScript

## 引言

在HTML5 Web Workers出现之前，所有JavaScript代码都与浏览器窗口的用户界面运行在同一个线程中。结果是，所有长时间运行的脚本都会导致浏览器窗口对用户输入无响应，直到处理完成。如果脚本运行时间足够长，浏览器甚至会提示用户是否要停止无响应的脚本。

Web Workers通过允许JavaScript代码在与浏览器窗口UI线程分开的线程中运行来解决这个问题。这使得长时间运行的脚本可以在不干扰浏览器UI响应性的情况下进行处理（例如，用户仍然可以点击按钮和滚动内容）。

关于Web Workers需要注意几点：由于它们运行在与UI分开的线程中，worker线程无法访问DOM或其他UI功能。此外，Web Workers并非设计为大量使用，并且预期是长期运行的，因为它们每个worker实例都有很高的启动性能成本和内存成本。

## Worker的类型

有两种可用的worker类型：专用worker（dedicated workers）和共享worker（shared workers）。

专用worker与它们的创建者相关联，并且比共享worker稍微简单一些。另一方面，共享worker允许来自同一源/域的任何脚本获取对worker的引用并与之通信。

由于worker线程初始启动需要时间并且每个worker使用大量内存，能够共享单个worker而不是为每个打开的窗口创建一个worker可以提高性能。然而，代价是共享worker的设置和使用比专用worker稍微复杂一些。

### 共享Worker的作用域

您可能想知道当创建共享worker的窗口被关闭时会发生什么。其他来自同一源的窗口是否仍然可以访问该worker线程？

只要有一个窗口与之保持连接，共享worker就会保持活动状态。例如：窗口1创建一个共享worker，窗口2连接到它。之后，窗口1被关闭，但是因为窗口2仍然连接着，共享worker线程即使没有被窗口2最初创建，也仍然保持活动状态。

## 浏览器支持

`http://caniuse.com`：这个方便的网站可以告诉您某个功能是否被浏览器支持，以及在哪个版本的浏览器中该所需功能变得可用。这可以节省确定所需功能在您打算支持的浏览器中是否可用所需的大量测试时间。该网站会定期更新。

在撰写本文时，专用worker获得了最多的浏览器支持，包括：Internet Explorer 10+、Firefox、Chrome、Safari、Opera、iOS Safari、BlackBerry、Opera Mobile、Android版Chrome和Android版Firefox。

共享worker支持目前包括：Chrome、Safari、Opera、iOS Safari、BlackBerry和Opera Mobile。

## 创建Workers

### 测试功能是否存在

除非您确定您的用户将使用特定的浏览器版本，否则您的网站有可能会被一个不支持您希望使用的HTML5功能的浏览器访问。在尝试使用某个功能之前，最好先测试浏览器是否支持您打算使用的功能。

如果浏览器支持，专用worker和共享worker都将作为对象存在于全局`window`对象上。以下是测试浏览器是否支持专用或共享worker的示例：

```
if (window.Worker) { /* 支持专用Workers */ }
if (window.SharedWorker) { /* 支持共享Workers */ }
```

### 创建一个Worker

要创建专用worker，您只需创建一个新的`Worker`对象实例，并传入一个字符串，该字符串指定包含worker线程主要代码的JavaScript文件的位置。以下是如何创建专用worker的示例：

```
var aDedicatedWorker = new Worker("DedicatedWorker.js");
```

共享worker的创建方式与创建专用worker相同，唯一的区别在于，我们指定一个`SharedWorker`对象而不是`Worker`对象：

```
var aSharedWorker = new SharedWorker("SharedWorker.js");
```

`Worker`对象被设计为接受一个指示JavaScript文件位置的字符串（而不是一个函数），以防止创建一个闭包，从而使worker能够直接访问浏览器的DOM或其他页面元素。

## 从Worker接收消息

Worker与创建它们的线程之间的通信是通过传递消息来完成的。由于多种HTML5技术都传递消息，因此存在一个专门的规范，称为HTML5 Web Messaging。我提到这一点是因为，Web Workers工作方式的某些关键细节并不在web worker规范中，而是在web messaging规范中。

为了从worker接收消息，您需要附加到worker实例的`onmessage`事件处理程序。以下是如何为专用worker设置事件监听器的示例：

```
aDedicatedWorker.onmessage = OnWorkerMessage;
```

为共享worker对象设置事件监听器与专用worker类似，但在此情况下您需要访问`port`对象，如下例所示：

```
aSharedWorker.port.onmessage = OnWorkerMessage;
```

对于专用和共享worker，您也可以通过使用`addEventListener`方法附加到`message`事件处理程序事件类型，如下例所示：

```
aSharedWorker.port.addEventListener("message", OnWorkerMessage, false);
```

如果您使用`addEventListener`方法，需要注意的一点是，对于共享worker，您还需要启动该worker：

```
aSharedWorker.port.start();
```

`onmessage`事件监听器方法将被传递一个`MessageEvent`参数，该参数将有一个`.data`属性，其中包含从worker线程传递的消息。以下是我们`onmessage`事件监听器的实现（在这里专用worker和共享worker没有区别）：

```
function OnWorkerMessage(evt){
    alert("Message received from the worker: " + evt.data);
}
```

## 向Worker传递消息

要向专用worker传递消息，您可以调用worker实例的`postMessage`函数，如下例所示：

```
aDedicatedWorker.postMessage("Hello from the UI thread!");
```

向共享worker传递消息类似，但在此情况下`postMessage`函数位于`port`对象上：

```
aSharedWorker.port.postMessage("Hello from the UI thread!");
```

`postMessage`函数不仅限于在线程之间传递字符串。您还可以传递结构化数据，如JSON对象、JavaScript对象（如数字和`Date`对象），以及某些数据对象，如`File Blob`、`FileList`和`ArrayBuffer`。以下是传递一个对象的示例：

```
var objData = {
    "employeeId": 103,
    "name": "Sam Smith",
    "dateHired": new Date(2006, 11, 15)
};
aDedicatedWorker.postMessage(objData);
```

因为对象在两个线程之间无缝传递（我们在一侧传入对象，在另一侧接收它，而无需我们做任何特殊工作），感觉数据是直接传递的，但实际上默认情况下并非如此。默认情况下，所有数据实际上都是在线程之间复制的（也称为结构化克隆）。

当您向另一个线程传递数据时，幕后对象被序列化为字符串，传递到另一个线程，然后在另一侧反序列化回对象。在大多数情况下，如果您只是传递少量数据，您可能不会注意到太大的性能影响，但如果您需要传递大量数据，这种克隆可能会导致明显的延迟。

幸运的是，一些浏览器现在支持一种称为可传输对象（transferable objects）的概念，其中数据的所有权被转移给另一个线程。数据是被移动而不是被复制，这可以带来巨大的性能提升。

例如，当您将像`ArrayBuffer`这样的对象传输到另一个线程时，内容被移动到另一个线程，在调用线程中留下一个空的`ArrayBuffer`对象。要将对象传输到线程，您仍然使用`postMessage`方法，但在可选的第二个参数中包含一个数组，指示消息中的哪些项目应该被传输。

> 实用提示：在撰写本文时，并非所有浏览器都支持`postMessage`方法的第二个参数，如果您尝试使用第二个参数，实际上会抛出异常。如果您希望使用此技术，建议在`postMessage`调用周围使用`try/catch`语句。

如果您只传递一个对象，如下例所示，那么您可以在数组中指定该对象本身：

```
var abBuffer = new ArrayBuffer(32);
aDedicatedWorker.postMessage(abBuffer, [abBuffer]);
```

并非所有对象都是可传输的，但如果您传递的对象包含一个可传输对象，您可以在传输参数数组中指定您希望传输的对象的哪一部分，如下例所示：

```
var objData = {
    "employeeId": 103,
    "name": "Sam Smith",
    "dateHired": new Date(2006, 11, 15),
    "abBuffer": new ArrayBuffer(32)
};
aDedicatedWorker.postMessage(objData, [objData.abBuffer]);
```

如果您传递到另一个线程的对象包含多个可传输对象，您可以通过在传输参数数组中用逗号分隔来指定每个项目。

并非所有浏览器都支持可传输对象。以下示例展示了一种检测浏览器是否支持可传输对象的方法，即通过实际尝试将少量数据放在`ArrayBuffer`中传递到另一个线程。如果`postMessage`调用后buffer的长度为零，那么我们知道数据是被传输了，而不是仅仅被复制：

```
var abBuffer = new ArrayBuffer(32);
aDedicatedWorker.postMessage(abBuffer, [abBuffer]);
if (abBuffer.byteLength) {
    alert("您的浏览器不支持可传输对象");
}
```

## 错误处理

对于专用和共享工作线程，你都可以将工作线程实例的`onerror`事件处理程序附加到它，以便在发生运行时错误（例如，可能存在阻止创建工作线程对象的网络错误）时得到通知。对于专用工作线程，`onerror`事件处理程序还会告诉你工作线程内部任何未处理的异常。

以下是如何在工作线程对象上添加`onerror`事件监听器的示例：

```
aDedicatedWorker.onerror = function(evt) { alert(evt.message); }
aSharedWorker.onerror = function(evt) { alert(evt.message); }
```

| ErrorEvent 属性 | 描述 |
| --- | --- |
| `message` | 人类可读的错误消息 |
| `filename` | 发生错误的脚本文件的名称（在某些浏览器中此属性未定义，在其他浏览器中此属性是空字符串） |
| `lineno` | 发生错误的脚本文件的行号（在某些浏览器中此属性设置为零） |

## 关闭工作线程

可以通过在工作线程实例上调用`terminate`来关闭专用和共享工作线程，如下例所示：

```
aDedicatedWorker.terminate();
aSharedWorker.terminate();
```

调用`terminate`时需要注意的一点是，它不会给工作线程提供完成其操作或自行清理的机会。

以下是创建专用和共享工作线程的JavaScript代码摘要：

```
var gDedicatedWorker = null;
var gSharedWorker = null;

$(document).ready(function () {
    // 如果此浏览器支持专用工作线程...
    if (window.Worker) {
        gDedicatedWorker = new Worker("DedicatedWorker.js");
        gDedicatedWorker.onerror = handleError;
        gDedicatedWorker.onmessage = handleMessage;

        gDedicatedWorker.postMessage("Hello from the UI thread!");
    } // 结束 if (window.Worker)

    // 如果此浏览器支持共享工作线程...
    if (window.SharedWorker) {
        gSharedWorker = new SharedWorker("SharedWorker.js");
        gSharedWorker.onerror = handleError;
        gSharedWorker.port.onmessage = handleMessage;

        gSharedWorker.port.postMessage("Hello from the UI thread!");
    } // 结束 if (window.SharedWorker)
});

// 错误事件监听器
function handleError(evtError) {
    if (typeof evtError === "string") {
        updateResults("错误: " + evtError);
    }
    else if (evtError.message) {
        updateResults("错误...消息: " + evtError.message +
            ", 文件名: " + evtError.filename +
            ", 行号: " + evtError.lineno);
    }
    else {
        updateResults("未知错误");
    }
}

// 消息事件监听器
function handleMessage(evtMessage) {
    updateResults("收到来自工作线程的消息: " +
        evtMessage.data);
}

// 一个用于用新消息更新页面上某个 div 的辅助函数
function updateResults(sMessage) {
    var $divResults = $("#divResults");
    $divResults.html($divResults.html() + "<br />" + sMessage);
}
```

## 在工作线程内部

### 包含 JavaScript 文件

工作线程有权访问一个`importScripts`函数，该函数允许线程引入所有必要的JavaScript文件。`importScripts`函数可用于导入一个或多个文件。如果指定了多个文件，它们将并行下载，但将按指定的顺序同步加载和处理。此外，`importScripts`文件在所有指定的文件加载和处理完毕之前不会返回。

以下是使用`importScripts`将3个JavaScript文件导入工作线程的示例（此示例到3个文件为止，但你可以指定任意数量的文件）：

```
importScripts("file1.js", "file2.js", "file3.js");
```

### 接收消息

为了使专用工作线程能够从其创建者接收消息，它必须附加到`onmessage`事件，如下例所示：

```
self.onmessage = function(evt) {
    // 来自调用线程的数据可以在参数的 .data 属性中找到
}
```

在共享工作线程中，你需要处理`onconnect`事件，该事件在每次有线程连接到共享工作线程时触发。在`onconnect`事件监听器中，你可以附加到`ports`数组中第一个端口对象的`onmessage`事件（数组中永远只有一个端口）：

```
self.onconnect = function(evt) {
    evt.ports[0].onmessage = function(evtMessage) {
        // 来自调用线程的数据可以在参数的 .data 属性中找到。
        // 调用线程的端口可以在参数的 .target 属性中找到
    }
}
```

### 传递消息

专用工作线程能够通过`postMessage`函数向其创建者传递消息：

```
self.postMessage("Hello from the dedicated worker");
```

从共享工作线程出发，为了向已连接的线程传递消息，你需要使用你希望发送消息给的那个已连接线程的端口上的`postMessage`事件。有几种方法可以获取端口对象。一种选项是在`onconnect`事件处理程序中创建一个全局数组来保存每个已连接的端口。

另一种获取端口对象的选项是访问`onmessage`事件对象的`target`属性，该属性保存对调用线程端口的引用，如下例所示：

```
evt.target.postMessage("Hello from the shared worker");
```

### 超时

工作线程支持超时（`setTimeout`、`clearTimeout`、`setInterval`和`clearInterval`），如果你只想在设定的时间间隔而不是持续处理时进行处理，这非常有用。一个场景可能是你想检查第三方服务器是否有新信息，但又不想用请求轰炸该网站。你可以设置一个超时，每隔5分钟左右检查一次是否有新信息。

### XMLHttpRequest

在工作线程内部，可以发起`XMLHttpRequest`，由于工作线程与浏览器窗口的UI线程分离，不会影响性能，因此由你决定是同步还是异步发起请求。然而，需要注意的一点是，在工作线程内部，`XMLHttpRequest`对象将仅通过`responseText`属性返回数据（当`XMLHttpRequest`对象在工作线程中使用时，`responseXML`属性始终返回`null`）。

以下是在工作线程内部使用`XMLHttpRequest`对象的示例：

```
// 我们要发送给服务器端代码的数据
var objData = { "sPageIndex": iPage };

// 向服务器发起同步调用
var xhrRequest = new XMLHttpRequest();
xhrRequest.open("POST", "/main.aspx/GetNextPage", false);
xhrRequest.setRequestHeader("Content-Type", "application/json");
xhrRequest.send(JSON.stringify(objData));

// 将响应返回给 UI 线程
self.postMessage(xhrRequest.responseText);
```

### location

工作线程有权访问一个`location`对象，该对象表示线程创建时设置的绝对URI。可用的`location`属性有：`href`、`protocol`、`host`、`hostname`、`port`、`pathname`、`search`和`hash`。

### navigator

`navigator`对象在工作线程内可用，提供有关浏览器的一些详细信息。一些可用的属性是：`appName`、`appVersion`、`platform`和`userAgent`。

`navigator`对象中另一个可用的属性是`onLine`，如果用户代理确定离线，则返回`false`；如果用户代理可能在线，则返回`true`。关于`navigator`对象的`onLine`属性需要注意的一点是，在撰写本文时，并非每个浏览器都支持它。因此，如果你选择使用此属性，最好先检查该属性是否存在。

### 错误处理

工作线程可以选择附加到全局`onerror`事件处理程序，以监听未处理的异常。这对于共享工作线程特别有用，因为许多浏览器不会将未处理的异常传递给工作线程对象本身的`onerror`事件处理程序。

以下是在工作线程内部附加到`onerror`事件处理程序的示例：

```
self.onerror = function(evt) {
    // 处理错误，可能通过向此线程的创建者发起 postMessage 调用，以便可以显示一条消息
}
```

### 自行关闭

工作线程可以通过调用`close`方法自行关闭：

```
self.close();
```

以下是专用工作线程内部JavaScript的摘要：

```
// 可选地加载一些通用 JavaScript
// self.importScripts("common.js");

// 附加到 onmessage 事件以监听来自调用者的消息
self.onmessage = function (evt) {
    // 传回一条消息
    self.postMessage("Text received from the UI: " + evt.data);
}

// 附加到 onerror 事件以监听未处理的异常
self.onerror = function (evtError) {
    var sMsg = "Unknown Error";

    // 测试错误事件对象，看它是否有 message 属性。如果没有，检查它是否是一个字符串。
    if (evtError.message) { sMsg = evtError.message; }
    else if (typeof evtError === "string") { sMsg = evtError; }

    // 将消息传递给此工作线程的创建者
    postMessage("Dedicated Worker - Error Message: " + sMsg);
}

// 在某个时候，我们可以自己关闭线程
self.close();
```

以下是共享工作线程内部JavaScript的摘要：

```
// 可选地加载一些通用 JavaScript
// self.importScripts("common.js");

// 全局变量，将保存对最后连接到此共享工作线程的线程的引用。也可以使用数组来存储每个已连接线程的端口。
var gLastPort = null;

// 附加到 onconnect 事件以监听连接到此共享工作线程的线程
self.onconnect = function (evtConnect) {
    // 获取已连接线程端口的引用（数组中永远只有 1 个端口），并附加到 onmessage 事件
    gLastPort = evtConnect.ports[0];
    gLastPort.onmessage = function (evtMessage) {
        evtMessage.target.postMessage("Text received from the UI: "
        + evtMessage.data);
    }
}

// 附加到 onerror 事件以监听未处理的异常
self.onerror = function (evtError) {
    var sMsg = "Unknown Error";

    // 测试错误事件对象，看它是否有 message 属性。如果没有，检查它是否是一个字符串。
    if (evtError.message) { sMsg = evtError.message; }
    else if (typeof evtError === "string") { sMsg = evtError; }
}
```

## 附加内容

### 创建多个共享工作者

共享工作者的一个优势在于，你可以让多个打开的窗口共享使用单个工作者线程，但你并不局限于只使用一个共享工作者。`SharedWorker`对象在构造函数中接受第二个参数来指定工作者的名称。

第二个参数是大小写敏感的。因此，如果在一个窗口中将共享工作者命名为`Worker`，而在另一个窗口中命名为`worker`，由于'W'的大小写差异，实际上会创建两个共享工作者线程，而不是两个窗口之间共享的一个。

以下是如何创建两个共享工作者的示例：

```
// 窗口 1 - 共享工作者 1 和 2
var aSharedWorker1 = new SharedWorker("SharedWorker.js", "Worker1");
var aSharedWorker2 = new SharedWorker("SharedWorker.js", "Worker2");

// 窗口 2 - 共享工作者 1 和 2
var aSharedWorker1 = new SharedWorker("SharedWorker.js", "Worker1");
var aSharedWorker2 = new SharedWorker("SharedWorker.js", "Worker2");
```

### 从工作者内部生成额外的工作者

如果需要，工作者线程可以像在UI线程中创建工作者对象一样，以相同的方式创建额外的工作者对象（有时称为子工作者）。子工作者需要与父页面属于相同的来源/域名。此外，子工作者中的URI是相对于父线程的位置进行解析的，而不是相对于主页面的位置。

### 在工作者中使用 JSONP

在进一步讨论这个主题之前，重要的是要理解从第三方站点导入JavaScript文件/内容存在安全问题。当你使用脚本注入导入数据时，浏览器会下载接收到的JavaScript数据，对其求值——将接收到的文本转换为函数、变量、对象等——并且负载中的任何全局代码都将被运行。除了可能运行任意代码外，还有可能通过交换过程中使用的HTTP流量（如Cookie或其他头部信息）将信息泄露给第三方站点。

传统上，JSONP通过修改DOM来使用脚本注入。而在Web Workers的情况下，你无法访问DOM，那么我们如何实现脚本注入呢？事实证明，通过使用`importScripts`函数，从工作者内部发出JSONP请求出奇地简单，如下例所示：

```
function MakeRequest(){
    importScripts("http://SomeServer.com?jsonp=HandleRequest");
}
function HandleRequest(objJSON){
    // 处理返回的 JSON 对象
}
```

### 内联工作者

有时你可能想要利用Web Workers，但同时又不想处理单独的工作者文件。内联工作者有几个优点，包括：

- 你可以发出一个服务器请求，该请求动态返回包含自定义工作者代码的字符串，以满足代码的当前需求
- 通过将工作者代码作为字符串包含在JavaScript文件中或作为页面标记的一部分，你可以消除网络请求，从而加快加载速度

要实现内联工作者，你需要用一个包含工作者代码的字符串填充一个`Blob`对象。然后为该`Blob`创建一个URL，并使用该URL创建`Worker`对象。为了创建`Blob`的URL，我们使用`window.URL.createObjectURL`方法，它会给我们一个类似于以下内容的URL：

```
blob:http://localhost/72cdddc4-7989-4104-87ef-cf65ed5f5bf9
```

Blob URL将是唯一的，并且在你的应用程序生命周期内有效。如果你不再需要该URL，可以通过调用`window.URL.revokeObjectURL`并传入Blob的URL来释放它。

以下是创建内联工作者的一个示例：

```
var bInlineWorker = new Blob(["onmessage = function(evt) {
    postMessage(\"Text received from the UI: \" + evt.data);
}"]);
var sBlobURL = window.URL.createObjectURL(bInlineWorker);

var aDedicatedWorker = new Worker(sBlobURL);
aDedicatedWorker.onmessage = handleMessage;
aDedicatedWorker.postMessage("Hello to our inline worker!");
```

以下示例是对上述方法的修改，它在页面的标记中定义工作者代码，与直接在`Blob`对象中将其构建为字符串相比，允许更自然地编辑代码：

```
<script id="scriptWorker" type="javascript/worker">
    // 由于指定的类型，浏览器的 JavaScript 引擎会忽略此代码块
    self.onmessage = function(evt) {
        self.postMessage("Text received from the UI: " + evt.data);
    };
</script>
```

然后，主页面的JavaScript代码会从script标签的内容动态填充blob：

```
var bInlineWorker = new Blob([document.getElementById("scriptWorker").textContent]);
var sBlobURL = window.URL.createObjectURL(bInlineWorker);

var aDedicatedWorker = new Worker(sBlobURL);
aDedicatedWorker.onmessage = handleMessage;
aDedicatedWorker.postMessage("Hello to our inline worker!");
```

## 附加资源

已编写了一些示例代码，以展示专用Web Workers的一个可能的实际用例。该示例演示了如何使用专用工作者线程来预取用户可以分页浏览的垂直项目列表所需的数据。大部分代码位于`main.js`和`DedicatedWorker.js`文件中，可以在以下GitHub仓库中找到：

`https://github.com/dovicoapi/HTML5WebWorkerExample`

W3C规范位于此处：`http://www.w3.org/TR/workers/`

有关HTML5 Web Messaging的更多信息（这是用于与Web Workers传递和接收消息的技术）：`http://www.w3.org/TR/webmessaging/`。查看`http://caniuse.com/`了解当前浏览器支持情况的详细分解。

由于规范和浏览器发展得如此之快，在这种情况下，对规范本身有深入的了解尤其重要。教程和分步指南可能会过时，但Web Workers背后的基本原则相当稳固。作为适用于包括但不限于Web Workers在内的HTML5技术的一般规则，尝试将规范与你找到的任何操作指南或代码片段进行交叉引用——并特别注意编写良好的测试代码。网络上充斥着HTML5开发者网站，但我发现以下网站非常突出，并且在理解各种技术的一些细节方面非常有帮助：

- HTML5 Zone: `http://www.DZone.com/mz/html5`
- Mozilla Developer Network: `https://developer.mozilla.org/en-US/docs/HTML/HTML5`
- HTML5 Rocks: `http://www.html5rocks.com`

## 关于作者

Gerard Gallant是Dovico Software的高级软件开发人员/软件架构师。十多年来，他在Dovico发布的大多数软件产品的开发中发挥了重要作用，从创建Microsoft Project链接ActiveX控件到创建新的托管服务API。他已婚，有两个美丽聪明的女孩。他通过投篮或看电影来放松身心，也喜欢广泛旅行。最近的出版物可以在他的博客上找到：`http://cggallant.blogspot.ca/`

## 推荐书籍

如果繁重的计算可以在后台执行，而不是与用户界面竞争，Web应用程序的运行效果会好得多。通过这本书，你将学习如何使用Web Workers在与UI并行的线程中运行计算密集型JavaScript代码。是的，多线程编程很复杂，但Web Workers提供了一个简单的API，帮助你在不使用复杂算法的情况下提高生产力。
