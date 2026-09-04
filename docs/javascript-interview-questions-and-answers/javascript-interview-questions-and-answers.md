
# JavaScript 面试问题与答案

## 关于书籍

JavaScript 面试题与解答对于准备 JavaScript 或 Web 技术面试的初学者和专业人士非常有帮助。本书涵盖了 UI 和全栈开发所需的 JavaScript 面试题。同时也建议学习 HTML、CSS 等其他 Web 技术，因为在这本小书中很难涵盖这么多技术。

本书将帮助你准备面试，并完善你的 JavaScript 知识，让你为进入行业工作做好准备。

对于关于这本书的任何正面或负面反馈，请通过 `pratikbandal007@gmail.com` 与我联系。

## 关于作者

我是 Pratik Bandal，目前在一家大型跨国公司工作，在软件行业拥有 6 年以上的经验。我获得了电子与通信（E&TC）学位和高级计算研究生文凭。我在医疗、支付和银行等不同领域拥有经验。

但最重要的是，我像你们一样也是一名开发者，每天工作 8 小时。写作是我在工作之余做的事情，我热爱它。没有人是完美的，对我也是如此。没有你们，我就无法成为一名作者。

编写一本面试题书是一项巨大的责任。但面试中巨大的自然差异在本书中很难完全涵盖。

文档对象模型 (DOM) 以一种方式表示 HTML 或 XML 页面，使得程序可以更改文档的结构、内容和样式。

DOM 代表文档节点也代表对象。

DOM 是网页的面向对象的表示，可以通过 JavaScript 等脚本语言进行修改。

### 99. 什么是 DOM 节点？

根据 W3C HTML DOM 标准，HTML 中的一切内容都可以表示为节点。

- 文档节点（Document node）代表整个文档。
- 元素节点（Element node）代表每个 HTML 元素，如 `HTML`、`HEAD`、`BODY`、`A`、`H1` 等。
- 文本节点（Text node）代表元素内部的文本。
- 属性节点（Attribute node）代表每个 HTML 属性。

节点（Node）拥有包含节点相关信息的节点属性。

- `nodeValue` 属性指定节点的值。
- `nodeType` 属性指定节点的类型。

### 100. 如何在 DOM 中通过 id 获取元素？

可以使用 `document` 对象的 `getElementById()` 方法通过 id 获取元素。

例如：

```javascript
document.getElementById("myUniqueId");
```

### 101. 如何在 DOM 中通过 class 获取元素？

可以使用 `document` 对象的 `getElementsByClassName()` 方法通过 class 获取元素。

例如：

```javascript
document.getElementsByClassName("myClass");
```

### 102. 如何获取任何元素的内容？

`innerHTML` 属性用于获取或替换 HTML 元素的内容。

### 103. 什么是 DOM 级别？

W3C DOM 规范分为不同的级别，每个级别包含一些必选模块和可选模块。

- Level 1：核心 DOM。
- Level 2：增加了对 CSS 的支持和更多功能。
- Level 3：增加了验证和更多功能。

### 104. 什么是延迟脚本？

`defer` 属性允许脚本在 HTML 文档完全解析后执行。

```html
<script src="script.js" defer></script>
```

### 105. 什么是异步脚本？

`async` 属性允许脚本在下载完成后立即执行。

```html
<script src="script.js" async></script>
```

### 106. 属性（attribute）和属性（property）之间有什么区别？

- Attributes 是定义在 HTML 标记中的，如 `id` 或 `class`。
- Properties 是 DOM 对象的一部分，如 `value` 或 `checked`。

### 107. innerHTML 和 innerText 有什么区别？

- `innerHTML` 返回元素内部的标记，包括标签。
- `innerText` 返回元素的文本内容，并会考虑 CSS 样式。

### 108. textContent 和 innerText 有什么区别？

- `textContent` 返回所有元素的文本，包括隐藏的元素。
- `innerText` 会感知样式且不会返回隐藏的文本。

### 109. 什么是 HTMLCollection？

`HTMLCollection` 接口表示元素（按文档顺序）的通用集合，并提供了用于从中选择的方法和属性。

- `HTMLCollection` 拥有 `length` 属性，返回集合中的项目数量。
- 无法使用 `forEach` 遍历 `HTMLCollection` 列表。

### 110. 什么是 NodeList？

`NodeList` 对象是节点集合，通常由 `childNodes` 等属性和 `querySelectorAll()` 等函数返回。

- `NodeList` 拥有 `length` 属性，返回节点的数量。
- 使用 `for...of` 循环可以遍历 `NodeList`。

### 111. 什么是帧（frames）？

Frame 将页面划分为若干部分，在每个部分中可以显示不同的页面。

## 8. Cookies

Cookies 是很小的数据项，由名称和值对组成。它们存储在你的计算机上，以便你的网络浏览器访问。

网络浏览器和服务器通过 HTTP 协议进行通信。这种无状态协议独立地处理每个请求，因此服务器在将数据发送给浏览器后不会保留数据。通过 Cookie，这些数据可以从存储的 cookie 文件中获取，而不是与服务器通信。

例如，当用户访问网页时，可以将用户名存储在 cookie 中。现在当用户下次访问该页面时，属于该页面的 cookie 会被添加到请求中。

### 112. Cookie 如何帮助客户端服务器之间的 HTTP 通信？

当用户向服务器发送请求时，每个该请求都会被视为由不同用户发送的新请求。

在接收 HTTP 请求时，服务器可能在响应中发送一个 `Set-Cookie` 头部。

现在，每当用户向服务器发送请求时，cookie 都会自动添加到该请求中。由于 cookie 的存在，服务器可以识别用户。

### 114. Cookie 存储在哪里？

在浏览会期间，浏览器将 Cookie 存储在内存中，在退出时，它们会进入名为 `cookies.txt` 的文件。

不同的浏览器会将 Cookie 文件存储在磁盘的不同位置。

例如，在 Windows 系统上，Chrome 将 Cookie 存储以下位置：`C:\Users\YourUser\AppData\Local\Google\Chrome\User\Default\`

当 Cookie 过期后，它将不再保存在硬盘上。

### 115. Cookie 的参数有哪些？

Cookie 有六个参数：名称（name）、值（value）、过期（expires）、路径（path）、域名（domain）和安全性（security）。

名称和值是必须的，而其他参数都是可选的。

```javascript
document.cookie = "name=VALUE;expires=DATE;path=PATH;domain=DOMAIN;secure";
```

**Name and Value**：Cookie 的第一部分必须包含名称和值。整个名称/值必须是一个单一字符串，不能包含逗号、分号或空白字符。

**Expires**：用户退出浏览器时，Cookie 会消失。为了让 Cookie 保存得久一点，你必须按照以下格式设置过期日期：

`DD-Mon-YY HH:MM:SS GMT`

**Path**：通常路径被设置为根级目录（`/`），这意味着该 Cookie 适用于你网站的所有页面。如果你希望 Cookie 在特定目录 `<directoryname>` 中是可用的，则路径应指定为 `path/<directoryname>`。

**Domain**：某些网站有许多域名。“domain”参数的目的是允许 Cookie 用于其他域名。在这种情况下，如果网站是 `http://www.<domain>.com`，拥有子域名 `http://www.<subdomainaine>.<domain>.com` 和 `http://www.<subdomaintwo>.<domain>.com`，访问 `subdomainaine` 页面设置的 Cookie，`subdomaintwo` 页面将无法读取。但如果你添加 `domain=<domain>`，则所有以 `<domain>` 结尾的域名都可以读取该 Cookie。

**Secure**：Cookie 的最后一个参数是 secure，这是一个布尔值。如果 Cookie 被标记为 secure，则 Cookie 将发送到 Web 服务器，并尝试使用安全通信通道进行检索。

### 116. 用户可以禁用 Cookie 吗？

是的，用户可以从浏览器禁用 Cookie。

在 Chrome 中，你可以进入：设置 --> 高级设置 --> 隐私和安全 --> 内容设置 --> Cookie 并禁用 Cookie。

### 117. 如何创建 Cookie？

当访问者第一次访问网页时，他输入自己的姓名。该名称将如下所示存储在 Cookie 中：

```javascript
function createCookie(username, value) {
  document.cookie = username + "=" + value;
}
```

### 118. 如何读取 Cookie？

可以像这样读取 JavaScript Cookie：

```javascript
var x = document.cookie;
```

### 119. 如何删除 Cookie？

删除 Cookie 时，不需要指定值。

通过将 `expires` 参数设置为过去的日期，可以删除 JavaScript Cookie。

```javascript
document.cookie = "username; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/";
```

如果不指定路径，某些浏览器将不允许你删除 Cookie。

### 120. 本地存储（Local Storage）和会话存储（Session Storage）有什么区别？

**Local Storage**：对于每个 HTTP 请求，数据都不会发送回服务器（HTML、图像、JavaScript、CSS 等），从而减少了客户端和服务器之间的总流量。数据将一直保留，直到通过设置或程序手动清除。

**Session Storage**：类似于本地存储；唯一区别在于存储在本地存储中的数据没有过期时间，而存储在会话存储中的数据会在会话结束时清除。浏览器关闭时，Session Storage 会清除。

## 9. 表单验证（Form validation）

### 121. 什么是表单验证？

表单验证验证表单中的所有字段是否按照要求的格式填写。

如果用户输入的数据不符合格式，则向用户显示相应的错误信息。

表单可以使用服务端验证和客户端验证进行校验。

服务端验证更安全，且需要服务器连接进行验证；而客户端验证速度更快，不需要服务器连接，但安全性较低。

JavaScript 用于客户端验证。

客户端验证的优点是：它可以节省时间、减轻服务器负载，并可以在表单提交之前验证表单元素。

### 122. 什么是 required 属性？

HTML 元素中的 `required` 属性防止元素作为空值提交。

### 123. 什么是 pattern 属性？

`pattern` 属性允许你指定一个正则表达式。如果值不匹配，则表单无法提交。

## 10. 异常处理

### 133. 如何在 JavaScript 中处理异常？

JavaScript 使用 `try...catch...finally` 语句以及 `throw` 运算符来处理异常。

你可以捕获用户定义的运行时异常，但无法捕获 JavaScript 语法错误。

### 134. 解释 try...catch...finally。

- **Try**：将可能抛出错误的代码包裹在 `try` 块中。
- **Catch**：在 `catch` 块中编写代码来处理发生的错误。`catch` 块可以包含参数，为你提供错误信息。通常，`catch` 块用于记录错误或向用户显示特定消息。
- **Finally**：无论是否发生错误，`finally` 块中的代码都将始终执行。`finally` 块通常用于完成剩余任务，或重置在 `try` 块中发生错误前可能已更改的变量。

### 135. 如何通过程序抛出异常？

可以使用 `throw` 语句程序化地抛出异常。

对于作为异常抛出的数据类型没有限制。例如：

```javascript
throw "error occurred!";
throw new SyntaxError("syntax error occurred!");
```

## 11. 调试

### 136. 什么是调试？

调试是检测并修复软件代码中现有和潜在错误的过程，这些错误可能会导致程序出现异常之外的行为。

为了调试程序，程序员必须从问题开始，识别问题源，然后修复它。

有时调试一个程序花费的时间比编写代码还要长。

### 137. 什么是 debugger 关键字？

`debugger` 语句会停止 JavaScript 的执行。如果调试功能不可用，此语句将不起作用。

`debugger` 关键字就像脚本源代码中的断点。

例如：

```javascript
function someErroneousFunction() {
    debugger;
    // code
}
```

### 138. 什么是 console 对象？

`console` 对象提供了访问浏览器调试控制台的方法。

如果浏览器支持调试，你可以使用 `console.log()` 方法在调试窗口中显示所需的文本。

`console` 对象提供了 `debug()`、`log()`、`error()`、`info()`、`trace()`、`warn()` 等方法，这些方法对代码调试非常有用。

### 139. 如何在浏览器中激活调试？

你可以通过按 `F12` 并在调试器菜单中选择 `console` 来激活浏览器调试。

### 140. 如何在桌面浏览器中获取网页的移动设备视图？

1. 在浏览器中按 `F12`，
2. 然后点击“切换设备工具”，
3. 然后，选择你想查看网页的设备。

### 141. 如何在浏览器中停用断点？

可以通过点击浏览器开发者工具中“Sources（源代码）”选项卡中的“停用断点”图标来实现。

### 142. 如何暂停脚本执行？

可以通过点击“Sources（源代码）”选项卡中的“暂停脚本执行”图标来实现。

### 143. 如何在调试时逐行执行代码？

可以通过点击“Sources（源代码）”选项卡中的“逐行执行”图标来实现。

### 144. 如何在调试时跳过函数执行？

可以通过点击“Sources（源代码）”选项卡中的“跳过函数”图标来实现。

### 145. 什么是代码气味（Code Smell）？

在编程中，代码气味是指任何可能指示深层次问题的特征。

确定什么是代码气味是主观的，并且因语言而异。

用于代码分析的两个工具是 `ESLint` 和 `JSHint`。

## 12. AJAX

### 146. 什么是 AJAX？

AJAX 代表异步 JavaScript 和 XML。它允许在不刷新页面的情况下与服务器交换数据。

### 147. GET 和 POST 的区别是什么？

| 特性 | GET | POST |
| :--- | :--- | :--- |
| 历史 | 参数保留在历史中。 | 参数不会保存在历史中。 |
| 安全 | 参数暴露在 URL 中。 | 相对更安全，参数在请求体中。 |
| 缓存 | 可以缓存。 | 不缓存。 |

### 148. 什么是 XMLHttpRequest 对象？

`XMLHttpRequest` 对象用于客户端与服务器之间的异步通信。它提供了 `open()`、`send()`、`setRequestHeader()` 等方法。

### 149. 如何使用 AJAX 进行 GET 请求？

要使用 AJAX 发送 GET 请求，首先需要实例化 `XMLHttpRequest`。

使用对象的 `open()` 方法指定 URL 和 HTTP 方法（GET）。

然后调用 `send()` 方法来发送请求。

通过 `onreadystatechange` 接收响应。

例如：

```javascript
const xhr = new XMLHttpRequest();
xhr.open("GET", "http://some.domain.com/method");
xhr.send();
xhr.onreadystatechange = (event) => {
  console.log(xhr.responseText);
};
```

### 150. 如何使用 AJAX 进行 POST 请求？

要使用 AJAX 发送 POST 请求，首先需要实例化 `XMLHttpRequest`。

使用对象的 `open()` 方法指定 URL 和 HTTP 方法（POST）。

然后调用 `send()` 方法并传递数据来发送请求。

通过 `onreadystatechange` 接收响应。

例如：

```javascript
const xhr = new XMLHttpRequest();
xhr.open("POST", "http://some.domain.com/method");
xhr.send("fname=Pratik&lname=Bandal");
xhr.onreadystatechange = (event) => {
  console.log(xhr.responseText);
};
```

### 151. 什么是 HTTP 状态码？

HTTP 状态码是网站服务器提供的标准响应码。这些代码有助于识别导致网页或其他资源无法正常加载的原因。

#### 4xx 客户端错误：

此类 HTTP 状态码包括对网页或资源的请求包含语法错误，或由于某些原因无法执行，通常是客户端的错。

常见的客户端错误 HTTP 状态码包括 404（未找到）、403（禁止）和 400（请求错误）。

#### 5xx 服务器错误：

此类 HTTP 状态码包括网站服务器理解了对网页或其他资源的请求，但由于某些原因无法执行。

常见的服务器错误 HTTP 状态码包括 500（内部服务器错误）、503（服务不可用）和 502（网关错误）。

还有 1xx、2xx 和 3xx 代码是信息性的、确认成功的或指示重定向的，它们不是错误，因此你不应该对它们发出警报。
