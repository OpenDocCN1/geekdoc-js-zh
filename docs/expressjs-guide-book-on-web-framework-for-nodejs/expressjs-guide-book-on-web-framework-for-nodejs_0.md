# Express.js：Node.js Web框架指南




尽管已尽力验证本书中提供的信息，但作者对其中所含主题的任何错误、遗漏或相反解释不承担任何责任。本书提供的信息仅供教育和娱乐之用。读者应对自己的行为负责，作者不承担因使用此信息而产生的任何责任或损害（无论是实际还是感知的）。

所使用的商标未经任何同意，商标的发布未经商标所有者的许可或支持。本书中的所有商标和品牌仅用于说明目的，归其所有者所有，与本文件无关。

# 引言

ExpressJS 是最有用且最有趣的 Node 框架之一。它用于 Web 和移动应用程序的开发。这类应用程序在软件环境中使用最为广泛。这表明您需要了解如何使用此框架进行开发。该框架拥有众多模块，可用于增强应用程序的外观和感觉。

# 第 1 章 - ExpressJS 概述

ExpressJS 是一个 Node 框架，非常灵活，为开发人员提供了众多用于 Web 和移动应用程序开发的功能。该框架可用于 API 的开发。在本书中，我们将讨论 ExpressJS 的各种特性。

# 第 2 章 - 会话

要在 Express 中安装此模块，只需执行以下命令：

`$ npm install express-session`

上述命令会将会话安装到您的系统中。要在程序中使用它，您必须使用 `require` 命令。如下所示：

`var session = require('express-session')`

会话中间件可以通过使用给定的 `options` 来创建。您应该知道，会话数据不应保存在 cookie 本身中，而此处仅存储会话 ID。会话数据存储在应用程序的服务器端。然而，默认的服务器端会话存储 `MemoryStore` 并非为生产环境使用而开发。在大多数情况下，它会泄漏且无法扩展到单个进程之外。它是为调试目的而开发的。

`express-session` 会在 options 对象中接受以下属性：

## Cookie

这些是会话 ID 的 cookie 设置。请参考下面给出的示例：

`{ path: '/', httpOnly: true, secure: false, maxAge: null }`.

## Genid

这是一个用于生成新会话 ID 的函数。提供的函数应返回一个字符串，该字符串将用作会话 ID。`req` 作为第一个参数传递给该函数，以防在生成 ID 时需要将某个值附加到 `req`。此属性的默认值将是一个可以使用 `uid2` 生成 ID 的函数。

注意：为避免会话冲突，请确保生成的 ID 是唯一的，即它们应彼此不同。请参考下面给出的示例，展示如何实现这一点：

```
application.use(session({
    genid: function(req) {
    return genuuid() // 使用 UUID 作为会话 ID
},
    secret: ' my secret '
}))
```

## Name

这是要在响应中设置的会话 ID cookie 的名称。请注意，它是从请求中读取的。此属性的默认值是 `connect.sid`。对于在同一主机上运行多个应用程序的用户，会话 cookie 必须彼此分离。为此，必须在每个应用程序中设置不同的名称。

## Proxy

当您设置安全 cookie 时，必须信任反向代理。这可以通过 `X-Forwarded-Proto` 标头来完成。此属性的默认值是 `undefined`。

可能的取值如下所述：

1. `true` - 将使用 `X-Forwarded-Proto` 标头。
2. `false` - 将忽略所有标头，并且仅当存在直接的 `TLS/SSL` 连接时才考虑该连接。
3. `undefined` - 将使用 Express 本身的 `trust proxy` 设置。

## Resave

这将强制将会话保存回会话存储。无论会话在请求期间是否被修改，都会发生这种情况。其必要性取决于您的会话存储。但是，如果客户端发出并行请求，则可能会产生竞态条件。

## Rolling

这将强制在每个响应上设置 cookie。过期日期也会重置。此属性的默认值是 `false`。

## saveUninitialized

使用此选项，未初始化的会话将被保存到会话存储。未初始化的会话是指新的且未经任何修改的会话。此属性的默认设置是 `true`。但是，此设置已弃用，预计将来会更改。

## Required option

这是用于签署会话 ID cookie 的密钥。它可以由一组密钥字符串组成，也可以只是一个字符串用于单个密钥。如果您提供一组密钥，则仅使用数组中的第一个元素来签署会话 ID cookie。其余元素将用于验证请求中的签名。

## Store

这是会话存储的实例。其默认值是一个新的 `MemoryStore` 实例。

请参考下面给出的示例：

```
var application = express()

application.set('trust proxy', 1) // 信任第一个代理

application.use(session({
    secret: 'my secret',
    resave: false,
    saveUninitialized: true,
    cookie: { secure: true }
}))
```

我们需要能够在生产环境中使用 cookie，同时允许在开发环境中进行测试。可以通过使用 `NODE_ENV` 来启用此设置。请参考下面给出的示例，展示如何实现这一点：

```
var application = express()
var session = {
    secret: ' my secret ',
    cookie: {}
}
```




```javascript
if (application.get('env') === 'production') {
application.set('trust proxy', 1) // trusting the first proxy
     session.cookie.secure =  true // serving secure cookies
}
    application.use(session(session))
```

`cookie.maxAge`的默认设置为`null`，永不过期，这意味着 cookie 将成为浏览器会话 cookie。只有当用户关闭浏览器时，cookie 才会被移除。会话也会被移除。

`req.session`

要存储和访问会话数据，应使用属性`req.session`，存储会将其初始化为 JSON。会话对象将保持良好状态。考虑下面给出的示例，它展示了一个特定于用户的视图计数器：

```javascript
application.use(session({ secret: ' my secret ', cookie: { maxAge:  50000 }}))
```

```javascript
application.use(function(req, res, next) {
var session = req.session
if (session.views) {
session.views++
res.setHeader('Content-Type', 'text/html')
res.write('<p>views: ' + session.views + '</p>')
res.write('<p>will expires in: ' + (session.cookie.maxAge /  1000) + 's</p>')
res.end()
} else {
session.views =  1
res.end(' This is a demo for sessions. Refresh the page!')
}
})
```

### `Session.regenerate()`

当我们想要生成会话时，会调用此方法。之后，一个新的会话实例和 SID 将在`req.session`中初始化。如下所示：

```javascript
req.session.regenerate(function(error) {
// a new session should be added here
})
```

### `Session.destroy()`

通过此方法，会话被销毁，`req.session`被移除。它将在下一个请求中重新生成。如下所示：

```javascript
req.session.destroy(function(error) {
// a session cannot be accessed here.
})
```

### `Session.reload()`

用于重新加载会话，如下所示：

```javascript
req.session.reload(function(error) {
// the session has been updated
})
```

### `Session.save()`

用于保存会话，如下所示：

```javascript
req.session.save(function(error) {
// session has been saved
})
```

考虑下面给出的示例，它使用`express-session`来存储用户的页面浏览量：

```javascript
var express =  require('express')
var purl =  require('parseurl')
var session =  require('express-session')
var application = express()
application.use(session({
secret: ' my secret ',
resave:  false,
saveUninitialized:  true
}))
application.use(function (req, res, next) {
var vws = req.session.views
if (!vws) {
vws = req.session.views = {}
}
// getting the url pathname
var pathname = purl(req).pathname
// counting the views
vws[pathname] = (vws[pathname] ||  0) +  1
next()
})
application.get('/foo', function (req, res, next) {
res.send('you have viewed this page ' + req.session.vws['/test'] + ' times')
})
application.get('/bar', function (req, res, next) {
res.send('you have viewed this page ' + req.session.vws['/bar'] + ' times')
})
```

这就是在 ExpressJS 中使用会话的方式。

# 第 3 章 - serve-index

它用于提供包含目录列表的页面到特定路径。可以通过执行以下命令来安装：

`$ npm install serve-index`

上述命令会将`serve-index`安装到你的计算机上。要在程序中使用它，必须通过`require`方法包含或调用它。如下所示：

```javascript
var svIndex =  require('serve-index')
```

然后 API 将被包含在你的程序中。

## `serveIndex(path, options)`

这将返回一个中间件，用于提供你指定的`path`目录的索引。这里的路径基于`req.url`的值。要更改 URL 基址，请使用`app.use`。

serve index 在 options 对象中接受以下属性：

**过滤器**

此过滤器函数应用于文件。其默认值为`false`。它会为每个文件调用，并使用签名`filter(filename, index, files, dir)`。`Filename`是文件名，`index`是数组索引，`files`是文件数组，而`dir`是文件所在的绝对路径。

**隐藏文件**

用于显示隐藏文件。其默认值为`false`。

**图标**

用于显示图标。其默认值为`false`。

**样式表**

这是一个可选的路径，指向 CSS 样式表。其默认值为内置样式表。

**模板**

这是一个可选的路径，指向 HTML 模板，用于渲染 HTML 字符串。

**视图**

这是显示模式。

考虑下面给出的示例，它展示了如何使用上述所有内容：

```javascript
var fhandler =  require('finalhandler')
var http =  require('http')
var svIndex =  require('serve-index')
var svStatic =  require('serve-static')
// The Serve directory works to indexe for public/ftp folder (having icons)
var index = svIndex('public/ftp', {'icons':  true})
// Serving up the public/ftp folder files
var serve = svStatic('public/ftp')
// Creating a server
var server = http.createServer(function onRequest(req, res){
var done = fhandler(req, res)
serve(req, res, function onNext(error) {
if (error) return done(error)
index(req, res, done)
})
})
// Listen
server.listen(3000)
```

要使用 express 提供目录索引，请执行以下操作：

```javascript
var express =  require('express')
var svIndex =  require('serve-index')
var application = express()
// Serving URLs like the /ftp/thing as public/ftp/thing
application.use('/ftp', svIndex('public/ftp', {'icons':  true}))
application.listen()
```

# 第 4 章 - cookie-sessions

这是一个用于提供访客会话的模块，这样每个访问者都会有一个会话，无论是否经过身份验证。如果会话是新的，无论你是否填充会话，都会生成`Set-Cookie`属性。

可以通过以下命令安装：

`$ npm install cookie-session`

要在程序中使用 API，我们必须使用`require`命令，如下所示：

```javascript
var cookieSession =  require('cookie-session')
```

cookie session 在 options 对象中接受以下选项：

**名称**

这是要设置的 cookie 的名称。其默认值为`session`。

**密钥**

用于签名和验证 cookie 值的密钥列表。已设置的 cookie 始终使用`keys[0]`签名。其余密钥将用于验证，从而允许轮换。

**秘密**

这是一个字符串，当未提供`keys`时，将用作密钥。还有一些 cookie 选项需要了解如何使用。

如果需要销毁特定会话，请按如下方式操作：

```javascript
req.session =  null
```

考虑下面给出的简单视图计数器示例。示例如下：

```javascript
var cookieSession =  require('cookie-session')
var express =  require('express')
var application = express()
appliation.set('trust proxy', 1) // trusting the first proxy
application.use(cookieSession({
     name: 'session',
     keys: ['key1', 'key2']
}))
application.use(function (req, res, next) {
     // Updating the views
req.session.views = (req.session.views ||  0) +  1
     // Writing the response
res.end(req.session.views + ' views')
})
application.listen(3000)
```

考虑下面给出的下一个示例：

```javascript
var cookieSession =  require('cookie-session')
var express =  require('express')
var application = express()
application.set('trust proxy', 1) // trusting the first proxy
application.use(cookieSession({
name: 'session',
keys: ['key1', 'key2']
}))
// This will allow you to set req.session.maxAge for letting certain sessions
// have a different value other than the default one.
application.use(function (req, res, next) {
req.sessionOptions.maxAge = req.session.maxAge || req.sessionOptions.maxAge
})
// ... the logic should be added here ...
```



你必须注意，整个会话对象将被编码并存储在 cookie 中。这可能会超出不同浏览器对 cookie 大小的最大限制。如果会话对象足够大，并且在编码后可能超出浏览器的限制，那么在大多数情况下，浏览器会拒绝或避免存储该 cookie。

# 第 5 章 - ExpressJS 中的 Morgan

这是一个用于 Node.js HTTP 请求的日志记录中间件。要在程序中使用该 API，你必须使用 `require` 关键字，如下所示：

```javascript
var morgan = require('morgan')
```

创建时使用以下格式：

## morgan(format, options)

如上格式所示，我们有两个参数或参数项。

Morgan 在 options 对象中接受以下属性：

**Immediate**

日志行应在请求时而非响应时写入。这意味着即使服务器本身崩溃，请求也始终会被记录，但我们将无法记录来自响应的数据。

**Skip**

这是一个用于判断是否跳过日志记录的函数。其默认值为 `false`。请参考下面的示例，该示例展示了如何调用该函数：

```javascript
// 示例：仅记录错误响应
morgan('combined', {
  skip: function (req, res) { return res.statusCode < 400 }
})
```

**Stream**

这是一个用于写入日志行的输出流，其默认值为 `process.stdout`。

请参考下面的示例，该示例展示了如何将所有请求以 Apache combined 格式记录到 STDOUT。示例如下：

```javascript
var express = require('express')
var morgan = require('morgan')
var application = express()

application.use(morgan('combined'))

application.get('/', function (req, res) {
  res.send('hello, there!')
})
```

## 原生 HTTP 服务器

下面是一个演示如何实现此功能的示例：

```javascript
var fhandler = require('finalhandler')
var http = require('http')
var morgan = require('morgan')

// 创建“中间件”
var logger = morgan('combined')

http.createServer(function (req, res) {
  var done = finalhandler(req, res)
  logger(req, res, function (error) {
    if (error) return done(error)

    // 响应请求
    res.setHeader('content-type', 'text/plain')
    res.end('hello, there!')
  })
})
```

## 将日志写入文件

请参考下面的示例，该示例展示了如何将请求以 Apache combined 格式记录到我们的 `access.log` 文件中：

```javascript
var express = require('express')
var fs = require('fs')
var morgan = require('morgan')
var application = express()

// 创建一个写入流（追加模式）
var aLogStream = fs.createWriteStream(__dirname + '/access.log', {flags: 'a'})

// 设置日志记录器
application.use(morgan('combined', {stream: aLogStream}))

application.get('/', function (req, res) {
  res.send('hello, there!')
})
```

## 日志文件轮转

在下面的示例中，应用将使用 `file-stream-rotator` 模块，将所有请求以 Apache combined 格式记录到 `log/` 目录下的任意日志文件中。示例如下：

```javascript
var FStreamRotator = require('file-stream-rotator')
var express = require('express')
var fs = require('fs')
var morgan = require('morgan')
var application = express()
var lDirectory = __dirname + '/log'

// 确保日志目录存在
fs.existsSync(lDirectory) || fs.mkdirSync(lDirectory)

// 创建一个轮转写入流
var aLogStream = FStreamRotator.getStream({
  filename: lDirectory + '/access-%DATE%.log',
  frequency: 'daily',
  verbose: false
})

// 设置日志记录器
application.use(morgan('combined', {stream: aLogStream}))

application.get('/', function (req, res) {
  res.send('hello, there!')
})
```

## 自定义令牌格式

在下一个应用中，我们将使用自定义令牌格式。它通过为所有请求添加一个 ID，然后使用 `:id` 令牌来显示该 ID。应用如下：

```javascript
var express = require('express')
var morgan = require('morgan')
var id = require('node-uuid')

morgan.token('id', function getId(req) {
  return req.id
})

var application = express()

application.use(assignid)
app.use(morgan(':id :method :url :response-time'))

app.get('/', function (req, res) {
  res.send('hello, world!')
})

function assignId(req, res, next) {
  req.id = uuid.v4()
  next()
}
```

# 第 6 章 - CORS

这是一个 Node.js 包，提供了一个 ExpressJS/Connect 中间件，可用于启用 CORS 的各种选项。

要通过 npm 命令安装它，请执行以下命令：

```bash
$ npm install cors
```

它可以按如下方式使用：

```javascript
var express = require('express')
, cors = require('cors')
, application = express();

application.use(cors());

application.get('/products/:id', function(req, res, next){
  res.json({msg: 'This has CORS enabled for all the origins!'});
});

application.listen(80, function(){
  console.log(' web server which is CORS enabled listening on port 80');
});
```

要为单个路由启用 CORS，请按如下方式操作：

```javascript
var express = require('express')
, cors = require('cors')
, application = express();

application.get('/products/:id', cors(), function(req, res, next){
  res.json({msg: 'This has the CORS enabled for all the origins!'});
});

application.listen(80, function(){
  console.log(' web server which is CORS enabled now listening on port 80');
});
```

要配置 CORS，请按如下方式操作：

```javascript
var express = require('express')
, cors = require('cors')
, application = express();

var cOptions = {
  origin: 'http://sample.com'
};

application.get('/products/:id', cors(cOptions), function(req, res, next){
  res.json({msg: 'This has CORS enabled only for sample.com.'});
});

application.listen(80, function(){
  console.log(' web server which is CORS-enabled is now listening on port 80');
});
```

## 使用动态来源配置 CORS 可以按如下方式完成：

```javascript
var express = require('express')
, cors = require('cors')
, application = express();

var whitelist = ['http://sample1.com', 'http://sample2.com'];
var cOptions = {
  origin: function(origin, callback){
    var orIsWhitelisted = whitelist.indexOf(origin) !== -1;
    callback(null, orIsWhitelisted);
  }
};

application.get('/products/:id', cors(cOptions), function(req, res, next){
  res.json({msg: 'This has CORS enabled for the whitelisted domain.'});
});

application.listen(80, function(){
  console.log('CORS-enabled web server listening on port 80');
});
```

## 如何启用 CORS 预检

某些 CORS 请求被认为是复杂的，这些请求需要一个初始的 OPTIONS 请求。使用 HTTP 动词的 CORS 请求与使用 POST/GET/HEAD 或使用自定义标头的请求相比，被认为是复杂的。要启用预检，需要为需要支持的路由添加一个新的 OPTIONS 处理程序。如下所示：

```javascript
var express = require('express')
, cors = require('cors')
, application = express();

application.options('/products/:id', cors()); // 为 DELETE 请求启用预检
application.del('/products/:id', cors(), function(req, res, next){
  res.json({msg: 'This has CORS enabled for all the origins!'});
});

application.listen(80, function(){
  console.log(' The web server which is CORS-enabled is listening on port 80');
});
```

也可以全局启用预检，如下所示：

```javascript
application.options('*', cors()); // 在其他路由之前包含
```

## CORS 的异步配置

```javascript
var express = require('express')
, cors = require('cors')
, application = express();

var whitelist = ['http://sample1.com', 'http://sample2.com'];
var cOptionsDelegate = function(req, callback){
  var cOptions;
  if(whitelist.indexOf(req.header('Origin')) !== -1){
    cOptions = { origin: true }; // 在 CORS 响应中反映（启用）请求的来源
  }else{
    cOptions = { origin: false }; // 为我们的请求禁用 CORS
  }
}
```




```
callback(null, cOptions); // callback 需要两个参数：error 和 options

};

application.get('/products/:id', cors(cOptionsDelegate), function(req, res, next){

res.json({msg: '此接口已为白名单域名启用 CORS。'});

});

application.listen(80, function(){

console.log(' 已启用 CORS 的 Web 服务器正在监听 80 端口');

});
```

这就是实现方式。

# 第 7 章 - Express-Paginate

该模块需与数据库的分页插件（如 MongoDB 的分页插件）配合使用。

安装方法：执行以下命令：

`npm install -S express-paginate`

要在程序中使用它，需要使用 `require` 关键字将其引入。示例如下：

```
var paginate = require('express-paginate');
```

通过 `paginate`，将创建一个新的 `express-paginate` 实例。参考下面的示例：

```
// # app.js
var express = require('express');
var paginate = require('express-paginate');
var application = express();

// 放在所有使用分页的路由之前
application.use(paginate.middleware(10, 50));

application.get('/users', function(req, res, next) {
  // 假设 `Users` 已在示例中预先定义
  // 例如 `var Users = database.model('Users')`（针对使用 `mongoose` 的情况）
  // 并且已通过 `User.plugin(require('mongoose-paginate'))` 为 Users 模型添加了 Mongoose 插件 `mongoose-paginate`

  Users.paginate({}, { page: req.query.page, limit: req.query.limit }, function(error, users, pageCount, itemCount) {
    if (error) return next(error);

    res.format({
      html: function() {
        res.render('users', {
          users: users,
          pageCount: pageCount,
          itemCount: itemCount
        });
      },
      json: function() {
        // 由 API 响应创建列表对象
        res.json({
          object: 'list',
          has_more: paginate.hasNextPages(req)(pageCount),
          data: users
        });
      }
    });
  });
});

application.listen(3000);
```

第二个代码文件内容如下：

```
//- users.jade
h1 用户

//- 以下代码将创建一个用于按名称排序的链接
//- 你可能已经注意到，我们只需传递要修改的查询字符串参数，
//- 而不需要传递整个查询字符串
a(href=paginate.href({ sort: 'name' })) 按名称排序

//- 这将假设查询字符串中包含 `?age=1` 或 `?age=-1`
//- 因此该链接会取反这些值，从而提供相反的排序顺序
//- （即 -1 表示降序，1 表示升序）
a(href=paginate.href({ sort: req.query.age === '1' ? -1 : 1 })) 按年龄排序

ul
  each myuser in users
    li= myuser.email

include _paginate
```

第三个代码文件内容如下：

```
//- _paginate.jade
//- 在此示例中，我们将使用 Bootstrap 3.x 的分页类

if paginate.hasPreviousPages || paginate.hasNextPages(pageCount)
  .navigation.well-sm#pagination
    ul.pager
      if paginate.hasPreviousPages
        li.previous
          a(href=paginate.href(true)).prev
            i.fa.fa-arrow-circle-left
            |  上一页
      if paginate.hasNextPages(pageCount)
        li.next
          a(href=paginate.href()).next
            | 下一页&nbsp;
            i.fa.fa-arrow-circle-right
```

# 第 8 章 - Multer

这是 Node.js 中的一个中间件，用于处理 `multipart/form-data` 类型的数据。它主要用于将文件上传到服务器。为了最大化效率，它构建在 `busboy` 之上。需要注意的是，Multer 无法处理非 multipart 类型的表单。

安装方法：执行以下命令：

`$ npm install --save multer`

它的工作原理是向 `request` 对象添加一个 `body` 对象和一个 `file/files` 对象。`body` 对象中存储表单字段的值，`file/files` 对象则包含已上传到服务器的文件。

参考下面的示例，了解如何实现：

```
var express = require('express')
var multer = require('multer')
var uploadfile = multer({ dest: 'uploads/' })
var application = express()

application.post('/profile', uploadfile.single('avatar'), function (req, res, next) {
  // req.file 是我们的 `avatar` 文件
  // req.body 用于保存文本字段（如果有的话）
})

application.post('/photos/upload', uploadfile.array('photos', 12), function (req, res, next) {
  // req.files 是一个包含多个 `photos` 文件的数组
  // req.body 包含文本字段（如果有的话）
})

var cUpload = uploadfile.fields([{ name: 'avatar', maxCount: 1 }, { name: 'gallery', maxCount: 8 }])
application.post('/cool-profile', cUpload, function (req, res, next) {
  // req.files 是一个对象（String -> Array），字段名作为键，值是一个文件数组
  //
  // 示例
  //  req.files['avatar'][0] -> File
  //  req.files['gallery'] -> Array
  //
  // req.body 包含文本字段（如果有的话）
})
```

如果需要处理 multipart 表单中的文本数据，可以使用 Multer 的任何方法，包括 `single()`、`.array()` 和 `fields()`。下面的示例展示了如何使用 `.array()`：

```
var express = require('express')
var application = express()
var multer = require('multer')
var uploadfile = multer()

application.post('/profile', uploadfile.array(), function (req, res, next) {
  // req.body 包含我们的文本字段
})
```

Multer 接受一个选项对象，其中最基本的属性是 `dest`，它指定了上传文件的目标路径。如果省略选项对象，上传的文件将保存在内存中，而不是磁盘上。

为了避免命名冲突，Multer 默认会重命名文件。其余功能可以根据需要进行自定义。

Multer 支持多种选项，请确保理解如何传递这些选项。

在普通的 Web 应用程序中，可能只需要 `dest` 属性，配置方式如下：

```
var uploadfile = multer({ dest: 'uploads/' })
```

如果需要对上传文件进行更精细的控制，可以使用 `storage` 属性代替 `dest` 属性。Multer 内置了 `DiskStorage` 和 `MemoryStorage` 两种存储引擎。你也可以使用第三方存储引擎。

如果需要完全控制存储在磁盘上的文件，可以使用磁盘存储引擎。示例如下：

```
var storage = multer.diskStorage({
  destination: function (req, file, cb) {
    cb(null, '/tmp/file-uploads')
  },
  filename: function (req, file, cb) {
    cb(null, file.fdname + '-' + Date.now())
  }
})

var uploadfile = multer({ storage: storage })
```

可用的两个选项是 `filename` 和 `destination`。它们都是函数，用于决定文件的存储方式。`destination` 属性确定上传文件在目录中的存储文件夹，也可以在程序中指定为路径。如果未指定此属性，则使用操作系统的默认路径。

## 文件过滤器

此属性可用于设置哪些文件应被上传，哪些应被跳过。该函数的使用方法如下例所示：

```
function fileFilter (req, file, cb) {
  // 该函数将调用 `cb` 并传入一个布尔值
  // 以指示文件是否应被接受
  // 如果要拒绝文件，则传入 `false`，如下所示：
  cb(null, false)

  // 如果要接受文件，则传入 `true`，如下所示：
  cb(null, true)

  // 由于某些环节可能出错，你也可以传递一个错误：
  cb(new Error('我完全不知道！'))
}
```

## 错误处理

当遇到错误时，Multer 会将其传递给 Express。可以使用标准的 Express 错误处理方式来显示错误。




为了让您捕获源自 Multer 的错误，只需自行调用中间件函数。如下例所示：

```
var uploadfile = multer().single('avatar')

application.post('/profile', function (req, res) {

uploadfile(req, res, function (error) {

if (error) {

// 上传时发生了错误

return

}

// 一切正常

})

})
```

这就是它的用法。

# 第 9 章 - 压缩

这是 Node.js 中可用的中间件。它支持以下压缩编码：

* deflate
* gzip

要在您的系统中安装此中间件，请执行以下命令：

`$ npm install compression`

要在您的程序中包含此 API，请使用 `require` 关键字，如下所示：

`var compression = require('compression')`

有多种选项可用于返回压缩中间件。

## .filter

这是默认的过滤函数。它用于构建一个自定义过滤函数，该函数将是默认函数的扩展。下面的示例展示了如何使用它：

```
application.use(compression({filter: compress}))

function compress(req, res) {

if (req.headers['x-no-compression']) {

// 带有此标头的请求的响应不应被压缩。

return false

}

// 回退到标准过滤函数

return compression.filter(req, res)

}
```

## red.flush()

使用此模块，可以将部分压缩的响应刷新到客户端。让我们举例说明。

## express/connect

此模块可以通过 `app.use` 使用，该函数在 Express 和 Connect 中均可用。通过中间件的请求始终会被压缩。考虑下面的示例，展示了如何实现：

```
var compression = require('compression')

var express = require('express')

var application = express()

// 压缩所有请求

application.use(compression())

// 添加所有路由
```

这就是它的实现方式。

## 服务器发送事件

此模块与服务器端配合使用时，并非开箱即用。为了压缩内容，必须缓冲输出窗口，以便获得良好的压缩效果。

为此，我们需要为那些需要将数据写入客户端的人调用 `red.flush()`。如下所示：

```
var compression = require('compression')

var express = require('express')

var application = express()

// 压缩响应

application.use(compression())

// 服务器发送事件流

application.get('/events', function (req, res) {

res.setHeader('Content-Type', 'text/event-stream')

res.setHeader('Cache-Control', 'no-cache')

// 大约每 2 秒发送一次 ping

var timer = setInterval(function () {

res.write('data: ping\n\n')

// !!! 我们程序中最重要的一部分

res.flush()

}, 2000)

res.on('close', function () {

clearInterval(timer)

})

})
```

# 第 10 章 - csurf

这是一个用于 CSRF 的令牌中间件。它充当保护目的的中间件。要使用它，必须首先初始化 cookie-parser 或 session 中间件。可以通过执行以下命令将其安装到您的计算机上：

`$ npm install csurf`

要在您的程序中使用该 API，请使用 `require` 命令，如下所示：

`var csurf = require('csurf')`

这就是将其包含到程序中的方式。

此模块的选项接受多个不同的对象，您可以学习如何使用它们。

考虑下面的示例，它展示了一个用于生成可回发的 CSRF 表单的服务器端代码。示例如下：

```
var cParser = require('cookie-parser')

var csrf = require('csurf')

var bParser = require('body-parser')

var express = require('express')

// 设置路由中间件

var csrfProtection = csrf({ cookie: true })

var pForm = bParser.urlencoded({ extended: false })

// 创建一个 express 应用

var application = express()

// 解析 cookies

// 这是必需的，因为 csrfProtection 中的 "cookie" 为 true

application.use(cParser())

application.get('/form', csrfProtection, function(req, res) {

// 将 csrfToken 传递给视图

res.render('send', { csrfToken: req.csrfToken() })

})

application.post('/process', pForm, csrfProtection, function(req, res) {

res.send('数据正在处理中')

})
```

在您的视图中，`csrfToken` 的值应设置为隐藏输入字段 `_csrf` 的值。如下所示：

```
<form action="/process" method="POST">

<input type="hidden" name="_csrf" value="{{csrfToken}}">

最佳颜色: <input type="text" name="bestColor">

<button type="submit">提交</button>

</form>
```

就是这么简单。

## 忽略路由

在网站的 API 区域中，如果我们的请求已完全通过身份验证，则应禁用 CSRF。可以通过使用路由器和 Express 来忽略 API 路由。考虑下面的示例，展示了如何实现：

```
var cParser = require('cookie-parser')

var csrf = require('csurf')

var bParser = require('body-parser')

var express = require('express')

// 设置路由中间件

var csrfProtection = csrf({ cookie: true })

var pForm = bParser.urlencoded({ extended: false })

// 创建一个 express 应用

var application = express()

// 解析 cookies

// 这是必需的，因为 csrfProtection 中的 "cookie" 为 true

application.use(cParser())

// 创建一个 API 路由器

var api = createApiRouter()

// 在将 csrf 附加到应用堆栈之前挂载 API

application.use('/api', api)

// 在 "/api" 挂载之后添加 csrf

appliation.use(csrfProtection)

application.get('/form', function(req, res) {

// 将 csrfToken 传递给视图

res.render('send', { csrfToken: req.csrfToken() })

})

application.post('/process', pForm, function(req, res) {

res.send('需要 csrf 才能到达这里')

})

function createApiRouter() {

var router = new express.Router()

router.post('/getProfile', function(req, res) {

res.send('这里没有 csrf 需要获取')

})

return router

}
```

这就是它的实现方式。

## 自定义错误处理

当 CSRF 验证失败时，会抛出一个带有 `err.code === 'EBADCSRFTOKEN'` 的错误。这也可以用于显示错误消息。考虑下面的示例，展示了如何实现：

```
var bParser = require('body-parser')

var cParser = require('cookie-parser')

var csrf = require('csurf')

var express = require('express')

var application = express()

application.use(bParser.urlencoded({ extended: false }))

application.use(cParser())

application.use(csrf({ cookie: true }))

// 错误处理程序

application.use(function (error, req, res, next) {

if (error.code !== 'EBADCSRFTOKEN') return next(error)

// 在此处处理 CSRF 令牌错误

res.status(403)

res.send('表单已被篡改')

})
```

这就是它的实现方式。

# 第 11 章 - body-parser

这是用于解析请求体的 Node.js 中间件。但是，它不处理 multipart 请求体，因为其体积庞大且结构复杂。在处理 multipart 请求体时，您可能需要处理以下模块：

* [multer](https://www.npmjs.org/package/multer#readme)
* [busboy](https://www.npmjs.org/package/busboy#readme) 和 [connect-busboy](https://www.npmjs.org/package/connect-busboy#readme)
* [formidable](https://www.npmjs.org/package/formidable#readme)
* [multiparty](https://www.npmjs.org/package/multiparty#readme) 和 [connect-multiparty](https://www.npmjs.org/package/connect-multiparty#readme)

该模块为用户提供以下解析器：

* [URL 编码的表单请求体解析器](https://github.com/expressjs/body-parser#bodyparserurlencodedoptions)
* [原始请求体解析器](https://github.com/expressjs/body-parser#bodyparserrawoptions)
* [JSON 请求体解析器](https://github.com/expressjs/body-parser#bodyparserjsonoptions)




## [文本正文解析器](https://github.com/expressjs/body-parser#bodyparsertextoptions)

要安装它，只需执行以下命令：

```
$ npm install body-parser
```

要使用该 API，请通过 `require` 命令将其包含到程序中。如下所示：

```
var bParser = require('body-parser')
```

通过 `bParser` 对象，可以暴露各种工厂方法，用于创建中间件。所有中间件都会使用解析后的请求体填充 `req.body` 属性，或者将错误传递给回调函数。

在 Express 中，可以将通用的 JSON 和 URL 编码解析器添加为顶层中间件。这样，所有传入请求的请求体都会被解析。请参考下面的简单示例，展示如何实现：

```
var express = require('express')
var bParser = require('body-parser')
var application = express()

// 解析 application/x-www-form-urlencoded
application.use(bParser.urlencoded({ extended: false }))

// 解析 application/json
application.use(bParser.json())

application.use(function (req, res) {
  res.setHeader('Content-Type', 'text/plain')
  res.write('你提交了：\n')
  res.end(JSON.stringify(req.body, null, 2))
})
```

## express 路由特定

可以将请求体解析器添加到需要它们的路由中。这在 Express 中是可行的，并且很容易实现。这是在 Express 中使用 `body-parser` 最简单且推荐的方式。请参考下面的示例，展示如何实现：

```
var express = require('express')
var bParser = require('body-parser')
var application = express()

// 创建 application/json 解析器
var jParser = bodyParser.json()

// 创建 application/x-www-form-urlencoded 解析器
var urlenParser = bParser.urlencoded({ extended: false })

// POST /login 将获取 urlencoded 请求体
application.post('/login', urlenParser, function (req, res) {
  if (!req.body) return res.sendStatus(400)
  res.send('欢迎，' + req.body.username)
})

// POST /api/users 将获取 JSON 请求体
application.post('/api/users', jParser, function (req, res) {
  if (!req.body) return res.sendStatus(400)
  // 在 req.body 中创建用户
})
```

## 更改解析器的内容类型

所有解析器都接受一个 `type` 选项，通过它可以更改 `content-type`，使其成为中间件要解析的类型。请参考下面的示例，展示如何实现：

```
// 将各种不同的自定义 JSON 类型解析为 JSON
application.use(bodyParser.json({ type: 'application/*+json' }))

// 将自定义内容解析为 Buffer
application.use(bParser.raw({ type: 'application/vnd.custom-type' }))

// 将 HTML 请求体解析为字符串
application.use(bParser.text({ type: 'text/html' }))
```

# 第 12 章 - Flash

这是实现 Express 的最简单方式。要安装它，请执行以下命令：

```
npm i flash
```

请参考下面的示例，展示如何实现：

```
application.use(session()); // session 中间件
application.use(require('flash')());
application.use(function (req, res) {
  // 闪现一条消息
  req.flash('info', '你好！');
  next();
})
```

请参考第二个示例：

```
for msge in flash
  a.alert(class='alert-' + msge.type)
  p= message.msge
```

这是最后一个示例：

```
while msge = flash.shift() // 消费消息，因为 jade 已经读取了它们
  a.alert(class='alert-' + msge.type)
  p= message.msge
```

一个 Flash 消息数组可以如下所示：

```
{
  "type": "info",
  "message": "message"
}
```

# [method-override](https://github.com/expressjs/method-override)

这用于覆盖 HTTP 动词。通过它，可以在客户端不支持“DELETE”和“PUT”等 HTTP 动词的地方使用它们。要在系统中安装它，请执行以下命令：

```
$ npm install method-override
```

要使用此模块，您需要知道，它必须在任何需要请求方法的模块之前使用。

## 使用标头进行覆盖

要使用标头进行覆盖，必须将标头名称作为字符串参数传递给 `methodOverride` 函数。要进行调用，必须将 POST 请求发送到具有该标头作为覆盖方法的 URL。请参考下面的示例，展示如何实现：

```
var connect = require('connect')
var mthdOverride = require('method-override')

// 在请求中使用 X-HTTP-Method-Override 标头进行覆盖
application.use(mthdOverride('X-HTTP-Method-Override'))
```

请参考下面的示例，展示如何与 `XMLHttpRequest` 一起使用：

```
var c = new XMLHttpRequest()
c.onload = onload
c.open('post', '/resource', true)
c.setRequestHeader('X-HTTP-Method-Override', 'DELETE')
c.send()

function onload() {
  alert('已获取响应：' + this.responseText)
}
```

# 第 13 章 - serve-favicon

这是一个 Node.js 中间件，用于提供 favicon。Favicon 是一种视觉提示，浏览器和其他客户端软件用它来识别网站。

可以通过执行以下命令将模块安装到系统中：

```
npm install serve-favicon
```

请参考下面的示例，展示如何在 express 中使用：

```
var express = require('express');
var favicon = require('serve-favicon');
var application = express();

application.use(favicon(__dirname + '/public/favicon.ico'));

// 在此处添加你的路由。
application.listen(3000);
```

在 connect 中，可以按如下方式实现：

```
var connect = require('connect');
var favicon = require('serve-favicon');
var application = connect();

application.use(favicon(__dirname + '/public/favicon.ico'));

// 在此处添加你的中间件等。
application.listen(3000);
```

## 普通 HTTP 服务器

这是一种可以在任何地方使用的中间件，包括 Express 和 connect 之外。

下面的示例展示了如何实现：

```
var http = require('http');
var favicon = require('serve-favicon');
var fnhandler = require('finalhandler');
var _favicon = favicon(__dirname + '/public/favicon.ico');

var server = http.createServer(function onRequest(req, res) {
  var done = fnhandler(req, res);
  _favicon(req, res, function onNext(error) {
    if (error) return done(error);
    // 在此处继续处理请求等。
    res.statusCode = 404;
    res.end('hello');
  });
});

server.listen(3000);
```

# 第 14 章 - response-time

这是 node.js 的响应时间标头。它通过创建一个中间件来记录 HTTP 服务器中请求的响应时间。此处的响应时间是指从请求进入中间件到标头写入客户端的时间。

可以通过执行以下命令安装此模块：

```
$ npm install response-time
```

可以通过使用 `require` 关键字将模块包含到程序中，如下所示：

```
var respTime = require('response-time')
```

请参考下面的示例，展示如何在 Express 和 connect 中使用：

```
var express = require('express')
var respTime = require('response-time')
var application = express()

application.use(respTime())

application.get('/', function (req, res) {
  res.send('你好！')
})
```

## 这就是它的用法。

## 普通 HTTP 服务器

可以按如下方式使用：

```
var finalhandler = require('finalhandler')
var http = require('http')
var respTime = require('response-time')

// 创建“中间件”
var _responseTime = respTime()

http.createServer(function (req, res) {
  var done = fnhandler(req, res)
  _responseTime(req, res, function (err) {
    if (error) return done(error)
    // 响应请求
    res.setHeader('content-type', 'text/plain')
    res.end('你好！')
  })
})
```

这就是该模块的用法。

响应时间指标





```javascript
var express = require('express')
var respTime = require('response-time')
var StatsD = require('node-statsd')
var application = express()
var statistics = new StatsD()
statistics.socket.on('error', function (err) {
  console.error(err.stack)
})
application.use(respTime(function (req, res, time) {
  var stat = (req.method + req.url).toLowerCase()
    .replace(/[:\.]/g, '')
    .replace(/\//g, '_')
  statistics.timing(stat, time)
}))
application.get('/', function (req, res) {
  res.send('hello, there!')
})
```

# 第 15 章 - [express-namespace](https://github.com/expressjs/express-namespace)

通过此模块，Express 增加了命名空间路由功能。要将其安装到系统中，可以执行以下命令：

`$ npm install express-namespace`

考虑下面给出的示例，该示例可用于响应任何请求。示例如下：

```
GET /forum/12
GET /forum/12/view
GET /forum/12/edit
GET /forum/12/thread/5
DELETE /forum/12
```

要使用该模块，必须使用 `app.namespace()` 和 `require('express-namespace')`。然后该模块将可供您使用。

要使用它，我们必须传递一个回调函数，然后对方法进行路由。在每个回调之后，调用将完成，命名空间将与其状态一起存储。如下所示：

```javascript
application.namespace('/forum/:id', function(){
  application.get('/(view)?', function(req, res){
    res.send('GET forum ' + req.params.id);
  });
  application.get('/edit', function(req, res){
    res.send('GET forum ' + req.params.id + ' edit the page');
  });
  application.namespace('/thread', function(){
    application.get('/:tid', function(req, res){
      res.send('GET forum ' + req.params.id + ' thread ' + req.params.tid);
    });
  });
  application.del('/', function(req, res){
    res.send('DELETE the forum ' + req.params.id);
  });
});
```

当前命名空间也可以通过 `app.currentNamespace` 访问。您还应该知道如何运行测试。但是，在此之前，请确保系统中已安装所有子模块。可以通过执行以下命令来安装它们：

`$ git submodule update –init`

可以通过执行以下命令来运行测试：

`$ make test`

这就是该模块的使用方式。

# 第 16 章 - [express-expose](https://github.com/expressjs/express-expose)

此模块用于将对象、函数和原始 JavaScript 暴露给客户端。此功能非常适合共享设置、工具和用户的当前数据。辅助方法和局部变量也会暴露给客户端。

要安装此模块，请执行以下命令：

`npm install -S express-expose`

它可以如下所示使用：

```javascript
var express = require('express');
var expose = require('express-expose');
application = expose(application);
application.expose(...);
```

以上是模块在 express 4.x 中的使用方式。在 express 2.x 和 3.x 中，可以按如下方式完成：

```javascript
var express = require('express');
var expose = require('express-expose');
application.expose(...);
```

## 如何暴露对象

将对象暴露给客户端的一种方法是暴露属性，最可能是 Express 配置。当 `app.expose(object)` 被暴露时，属性将暴露给 `application.*`。下面的示例展示了如何做到这一点：

```javascript
application.set('views', __dirname + '/views');
application.set(' the view engine ', 'jade');
application.set('title', ' Sample ');
application.set('default language', 'en');
application.expose(application.settings);
```

辅助方法也可以通过另一种用例来暴露。这可以与当前暴露的方式相同。如下所示：

```javascript
application.expose({ en: 'English', fr: 'French' }, 'application', 'languages');
```

然后您需要将默认缓冲区输出到模板。对于 Jade 用户，可以按如下方式完成：

```
script!= javascript
```

对于 EJS 用户，可以按如下方式完成：

```
<script><%- javascript %></script>
```

原始 JavaScript 字符串也可以如下所示暴露：

```javascript
application.expose('var some = "variable";');
```

## 暴露函数

可以轻松暴露一个命名函数。您只需将其与一个默认名称一起传递，以便缓冲区用模板名称替换它。下面是一个示例：

```javascript
application.expose(function someFunction(){
  return 'yes';
}, 'foot');
```

这就是它的实现方式。

## 自调用函数

也可以传递一个匿名函数，该函数将自行执行以创建一个包装函数。考虑下面的示例，展示了如何做到这一点：

```javascript
application.expose(function(){
  function notify() {
    alert('this will be executed finely:D');
  }
  notify();
});
```

这就是它的实现方式。

## 请求级别的暴露

以上所有讨论的内容都可以应用于请求级别。考虑下面的示例，展示了如何做到这一点。示例如下：

```javascript
application.get('/', function(req, res){
  var user = { name: 'john' };
  res.expose(user, 'application.current.user');
  res.render('index', { layout: false });
});
```

# 第 17 章 - connect-render

这是一个用于 connect 的模板渲染辅助工具。可以通过执行以下命令来安装：

`$ npm install connect-render`

它可以如下所示使用：

```javascript
var connect = require('connect');
var render = require('connect-render');
var application = connect(
  render({
    root: __dirname + '/views',
    layout: 'layout.html',
    cache: true, // `false` 用于调试
    helpers: {
      sitename: 'connect-render sample site',
      starttime: new Date().getTime(),
      now: function (req, res) {
        return new Date();
      }
    }
  })
);
application.use(function (req, res) {
  res.render('index.html', { url: req.url });
});
application.listen(8080);
```

API 可以如下所示使用：

```javascript
/**
 * connect-render: 一个用于 connect 的模板渲染辅助工具
 *
 * 使用场景：
 *
 * var render = require('connect-render');
 * var connect = require('connect');
 *
 * connect(
 *   render({
 *     root: __dirname + '/views',
 *     cache: true, // 在生产环境中必须设置为 `true`
 *     layout: 'layout.html', // 如果没有布局则设为 false
 *     open: "<%",
 *     close: "%>", // 默认的 ejs 关闭标签是 '%>'
 *     helpers: {
 *       config: config,
 *       sitename: 'NodeBlog Engine',
 *       _csrf: function (req, res) {
 *         return req.session ? req.session._csrf : "";
 *       },
 *     }
 *   });
 * );
 *
 * res.render('index.html', { title: 'Index Page', items: items });
 *
 * // 无布局
 * res.render('blue.html', { items: items, layout: false });
 *
 * @param {Object} [options={}] 渲染选项。
 *  - {String} layout, 布局名称，默认是 `'layout.html'`。
 *    设置 `layout=''` 或 `layout=false` 表示无布局。
 *  - {String} root, 视图文件的根目录。
 *  - {Boolean} cache, 缓存视图内容，默认是 `true`。
 *    在生产环境中必须设置 `cache = true`。
 *  - {String} viewExt, 视图文件扩展名，默认是 `''`。
 * @return {Function} 用于 `connect` 的渲染中间件
 */
function middleware(options) {}
```

# 结论

可以说 ExpressJS 是一个 Node 框架。它为开发者提供了一个可以用来创建 Web 和移动应用程序的框架。它具有许多开发者可以利用的功能来创建他们的应用程序。它通过其中间件来工作。该框架还为开发者提供了许多可用于开发应用程序的模块。





这些模块各自拥有独立的命令，可用于安装。要使用其中任何一个模块，你必须先安装它。它支持会话功能，这在创建 Web 应用程序时非常有用。它提供了多种选项，可供开发使用。你应该学习如何使用每个 ExpressJS 模块中可用的不同选项。`serve-index` 模块用于提供包含目录列表的页面，并将其映射到特定路径。

这在开发过程中非常有趣。借助 `cookie-sessions` 模块，你可以提供访客会话，这样每位访问者都会拥有一个会话，无论是否经过身份验证。这也是 Express 中最出色且最有趣的功能之一。这个 Node 框架即使对于初学者来说也非常容易学习。本书将帮助你学习如何使用它。

