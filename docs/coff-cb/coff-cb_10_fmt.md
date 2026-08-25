
# 十、Ajax

## 不使用 jQuery 的 Ajax 请求

### 问题

你想要通过 AJAX 来从你的服务器加载数据，而不使用 jQuery 库。

### 解决方案

你将使用本地的 `XMLHttpRequest` 对象。

通过一个按钮来打开一个简单的测试 HTML 页面。

```html
<!DOCTYPE HTML>
<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <title>XMLHttpRequest Tester</title>
</head>
<body>
    <h1>XMLHttpRequest Tester</h1>
    <button id="loadDataButton">Load Data</button>

    <script type="text/javascript" src="XMLHttpRequest.js"></script>
</body>
</html>
```

当单击该按钮时，我们想给服务器发送 Ajax 请求以获取一些数据。对于该例子，我们使用一个 JSON 小文件。

```json
// data.json
{
  message: "Hello World"
}
```

然后，创建 CoffeeScript 文件来保存页面逻辑。此文件中的代码创建了一个函数，当点击加载数据按钮时将会调用该函数。

```coffeescript
# XMLHttpRequest.coffee
loadDataFromServer = ->
  req = new XMLHttpRequest()

  req.addEventListener 'readystatechange', ->
    if req.readyState is 4                        # ReadyState Complete
      successResultCodes = [200, 304]
      if req.status in successResultCodes
        data = eval '(' + req.responseText + ')'
        console.log 'data message: ', data.message
      else
        console.log 'Error loading data...'

  req.open 'GET', 'data.json', false
  req.send()

loadDataButton = document.getElementById 'loadDataButton'
loadDataButton.addEventListener 'click', loadDataFromServer, false
```

### 讨论

在以上代码中，我们对 HTML 中按键进行了处理（第 16 行）以及添加了一个*单击*事件监听器（第 17 行）。在事件监听器中，我们把回调函数定义为 `loadDataFromServer`。

我们在第 2 行定义了 `loadDataFromServer` 回调的开头。

我们创建了一个 `XMLHttpRequest` 请求对象（第 3 行），并添加了一个 *readystatechange* 事件处理器。请求的 `readyState` 发生改变的那一刻，它就会被触发。

在事件处理器中，我们会检查判断是否满足 `readyState=4`，若等于则说明请求已经完成。然后检查请求的状态值。状态值为 200 或者 304 都代表着请求成功，其它则表示发生错误。

如果请求确实成功了，那我们就会对从服务器返回的 JSON 重新进行运算，然后把它分配给一个数据变量。此时，我们可以在需要的时候使用返回的数据。

在最后我们需要提出请求。

在第 13 行打开了一个 “GET” 请求来读取 `data.json` 文件。

在第 14 行把我们的请求发送至服务器。

### 旧版服务器支持

如果你的应用需要使用旧版本的 Internet Explorer，你需确保 `XMLHttpRequest` 对象存在。为此，你可以在创建 `XMLHttpRequest` 实例之前输入以下代码。

```coffeescript
if (typeof @XMLHttpRequest == "undefined")
  console.log 'XMLHttpRequest is undefined'
  @XMLHttpRequest = ->
    try
      return new ActiveXObject("Msxml2.XMLHTTP.6.0")
    catch error
    try
      return new ActiveXObject("Msxml2.XMLHTTP.3.0")
    catch error
    try
      return new ActiveXObject("Microsoft.XMLHTTP")
    catch error
    throw new Error("This browser does not support XMLHttpRequest.")
```

这段代码确保了 `XMLHttpRequest` 对象在全局命名空间中可用。
