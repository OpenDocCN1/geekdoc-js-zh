```markdown
# Backbone.js：快速轻松掌握基础！(javascript 框架) (第 1 卷)

## 免责声明

尽管已尽一切努力验证本书中提供的信息，但作者不对其中所含主题的误差、遗漏或相反解释承担任何责任。本书提供的信息仅用于教育和娱乐目的。读者需对自己的行为负责，作者不对因使用此信息而产生的任何实际或感知的责任或损害承担责任。

本书中使用的商标未获任何许可，商标的发布未经商标所有者同意或授权。本书内所有的商标和品牌仅用于说明目的，归其各自所有者所有，与本文件无关。

本书中使用的商标未获任何许可，商标的发布未经商标所有者同意或授权。本书内所有的商标和品牌仅用于说明目的，归其各自所有者所有，与本文件无关。

## 简介

Backbone.js 是一个非常实用的框架，适用于构建可在浏览器中执行的应用程序。它帮助开发者构建应用程序的客户端部分。它采用 MVC 框架来构建应用程序架构。

这也使得分离应用程序的用户界面部分与业务逻辑成为可能。由于对 Web 应用程序的需求不断增加，您应该学习如何使用此框架。这将帮助您为您的应用程序创建一个出色的客户端部分。只要您是 JavaScript 专家，就会觉得学习 Backbone.js 很容易。

然而，即使您尚未学习过 JavaScript，本书也会让您轻松掌握 Backbone.js。

## 第 1 章 - 概述

Backbone.js 是一个 JavaScript 库，用于开发可在 Web 浏览器中运行的应用程序的客户端部分。它使用 MVC 框架来构建应用程序结构。通过该框架，数据被抽象为模型，DOM 被抽象为视图，而事件则用于将两者绑定在一起。

Jeremy Ashkenas 开发了 Backbone.js，并于 2010 年 10 月 13 日发布。它允许我们使用 JavaScript 函数以简单的方式创建应用程序的前端部分。Backbone.js 为开发者提供了各种构建模块，以便开发应用程序的客户端。这些构建模块的示例包括模型、视图、路由器、集合和事件。每当应用程序的模型部分发生变化时，应用程序的 HTML 也会随之更新。使用该库，开发者可以轻松地将界面部分与业务逻辑分离。

该库是开源的，并提供超过 100 个扩展。它将帮助您构建代码结构。它负责处理包含用户数据的模型，并且这些数据将以与客户端输入时相同的格式在服务器端显示。

## 第 2 章 - 设置环境

设置 Backbone.js 的过程非常简单。设置该库有两种方式，如下所述：

- 1. 从其官方网站下载库。
- 2. 从内容分发网络（CDN）下载库。

### 从官方网站下载库

访问 Backbone.js 的官方网站，您将看到以下界面：

如上所示，您有三个下载选项，如下所述：

- 1. 开发版本 (Development version)- 只需右键点击按钮并选择“另存为”。您将获得完整的源代码 JavaScript 库。
- 2. 生产版本 (Production version)- 右键点击按钮并选择“另存为”。您将获得打包并压缩好的 `Backbone-min.js` 库文件。
- 3. 边缘版本 (Edge version)- 右键点击按钮并选择“另存为”。您将获得一个尚未发布的库版本，即仍处于开发中的版本。使用此版本的库存在风险。

### 依赖项

以下是 Backbone.js 所依赖的 JavaScript 文件：

- 1. `Underscore.js`- 这是硬性依赖项，必须包含。
- 2. `jQuery.js`- 此文件必须包含，以支持通过 `Backbone.Router` 实现的 Restful 持久化和历史功能，以及通过 `Backbone.View` 实现的 DOM 操作。
- 3. `json2.js`- 此文件应包含，以支持旧版 Internet Explorer。

### 从 CDN 下载库

内容分发网络 (CDN) 是由服务器组成的网络，用于向用户提供文件。一旦在页面中使用了 CDN 链接，文件的主机责任将从您的本地服务器转移到外部服务器。这意味着访问者如果曾经访问过您的网页并从同一网络下载了库，则无需重新下载。以下是 Backbone 所依赖的 JavaScript 文件：

- `jQuery`
- `Underscore`

上述内容的 CDN 链接应如下所示：

```html
<script type="text/javascript" src="https://ajax.googleapis.com/ajax-libs/jquery/1.5.2/jquery.min.js"></script>
```

```html
<script type="text/javascript" src="http://ajax.cdnjs.com/ajax/libs/underscore.js/1.1.4/underscore-min.js"></script>
```

```html
<script type="text/javascript" src="http://ajax.cdnjs.com/ajax-libs/backbone.js/0.3.3/backbone-min.js"></script>
```

以下是一个使用 Backbone.js 创建的示例：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
<title>Hello there using Backbone.js</title>
</head>
<body>

<!-- ============ -->
<!-- The HTML -->
<!-- ============ -->
<div id="container">Loading...</div>
```

库的引用

```html
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.3.3/underscore-min.js" type="text/javascript"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/backbone.js/0.9.2/backbone-min.js" type="text/javascript"></script>
```

```javascript
var ApplicationView = Backbone.View.extend({
  // elem - 代表 element（元素）。每个视图都会有一个与 HTML 内容相关联的元素，该内容将被渲染。
  elem: '#container',
  // 这是视图实例化后第一个被调用的函数。
  initialize: function(){
    this.render();
  },
  // $elem – 是一个缓存的 jQuery 对象（elem），通过它可以使用 jQuery 内容来推送内容。比如本例中的 Hello there。
  render: function(){
    this.$el.html("Hello there!!");
  }
});

var applicationView = new ApplicationView();
```

代码中的注释是不言自明的。HTML 代码：

```html
<div id="container">Loading…</div>
```

会在屏幕上打印出"**Loading...**"。CDNs 的添加方式如下所示：

```html
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.3.3/underscore-min.js" type="text/javascript"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/backbone.js/0.9.2/backbone-min.js" type="text/javascript"></script>
```

接下来的部分包含一个脚本。如下所示：

```javascript
var ApplicationView = Backbone.View.extend({
  // elem - stands for element. Every view will have an element associated with the HTML content, which will be rendered.
  elem: '#container',
  // It is the first function to be called when the view has been instantiated.
  initialize: function(){
    this.render();
  },
  // $elem – it is a cached jQuery object (elem), whereby jQuery content can be used for pushing the content. Like the Hello there in this case.
  render: function(){
    this.$el.html("Hello there!!");
  }
});
var applicationView = new ApplicationView();
```

它的作用是在屏幕上打印出以下文本：

```
<!DOCTYPE html>
<head>
<title>Trigger Event </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//创建对象 'myValue' 并使用 Backbone.Events 方法扩展它
var myValue = _.extend({title:'Hello!!!', site:'www.mysite.com'}, Backbone.Events);

//on() 方法将我们的回调函数绑定到对象
myValue.on('myFunction', function () {
document.write("The value triggered for the site is: ");
document.write(this.site); //通过引用当前对象来显示 site 的值
});
//trigger() 方法将在 'myValue' 上触发事件 'myFunction'
myValue.trigger('myFunction');
</script>
</body>
</html>
```

按照原样编写程序然后执行。将会观察到以下输出：

该站点触发的值为：www.mysite.com

## Once 事件

其工作方式与“on”事件相同，但会导致绑定的回调函数在被移除之前仅触发一次。其语法如下所示：

```
object.once(event, callback function, [context])
```

上述语法中使用了以下参数：

- `event`- 用于绑定对象。
- `callback`- 指向代码的引用。
- `context`- 可以传递给回调函数的对象。

请看以下示例，了解如何使用该事件：

```html
<!DOCTYPE html>
<head>
<title>Event Once Example</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.0/underscore.min.js" type="text/javascript"></script>
<script src="backbone.min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//We are creating the object 'myValue' and extends it by use of Backbone.Event method
var myvalue = _.extend({name:Hello!!!}), Backbone.Events);
The method `once()` will cause the bound callback to fire only once before it is being removed
myvalue.once(hello,function {} {
   document.write("After firing once, the value is:")
document.write(this.name); name ill shown by referring to the current object });
//This will trigger the hello event on this object myValue.
myvalue.trigger("hello")
</script>
</body>
</html>
```

执行上述程序后，您将得到以下输出：

触发一次后，其值为：Hello!!!

## Event listenTo 事件

此事件用于告知特定对象监听位于另一个对象上的特定事件。它将跟踪事件，并在事件发生时提供回调函数。如下所示：

```
object.listenTo(other, event, callback)
```

上述语法中使用了以下参数：

- `other`：定义其他对象的名称。
- `event`：用于绑定对象。
- `callback`：用于指向代码的引用。

请看以下示例，了解如何使用该事件：

```html
<!DOCTYPE html>
<head>
<title>Event Once </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript">
</script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>

<body>
<script type="text/javascript">
//Creating the object 'myValue' and 'myValue1' and extending them by use of
Backbone.Events
var myValue = _.extend({name: 'Hello..'}, Backbone.Events);
var myValue1 = _.extend({name: 'Welcome to MySite!!!'}, Backbone.Events);
//creating the 'listenMe' callback function and then invoking it when one object
listens to the particular event on the other object
var listenMe = function(){
document.write("Our value is: ");
document.write(this.name);
};
//The object 'myValue1' will listen once for the event 'listenMe' triggered on the
object 'myValue'
myValue1.listenTo(myValue, 'listenMe');
//The 'myValue' has no event listenMe and shows the value of 'myValue1'
myValue.trigger('listenMe');
</script>
</body>
</html>
```

以上就是它的实现方式。只需在自己的上按照原文编写代码，然后执行。您将观察到输出：我们的值为：Welcome to MySite

## Event stopListening 事件

此事件的作用是停止对象监听事件。其语法如下：

```
object.stopListening(other, event)
```

以下是关于参数的解释：

- `other`：定义其他对象的名称。
- `event`：用于绑定对象。
- `callback`：代码的引用。

以下示例展示了如何实现：

```html
<!DOCTYPE html>
<head>
<title>Event Once </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//Creating an object 'myValue' and 'myValue1' and extending them by use of Backbone.Events method
var myValue = _.extend({name:' Joel John '}, Backbone.Events);
var myValue1 = _.extend({name:' Mercy Andrew '}, Backbone.Events);

//creating the 'listenMe' callback function and then invoking it when one object listens to the particular event on the other object
var listenMe = function(){
document.write("We have the value: ");
document.write(this.name);
};
//The object 'myValue1' will listen once for the event 'listenMe' which was triggered on the object 'myValue'
myValue1.listenTo(myValue, 'listenMe);
//The 'myValue' has no 'listenMe' event and shows the value of 'myValue1'
myValue.trigger('listenMe');
//The 'myValue1' will stop listening to the specific event on the 'myValue'
myValue1.stopListening(myValue,'listenMe');
myValue.trigger('listenMe');
</script>
</body>
</html>
```

按照原文编写程序，然后运行。您将观察到输出：我们拥有该值：Welcome to MySite...在浏览器中打开该程序将获得上述输出。

## Event listenToOnce 事件

此事件的工作方式与 `listenTo` 事件相同，但会导致监听仅进行一次，之后便移除回调函数。其语法如下：

```
object.listenToOnce(other, event, callback)
```

上述语法中使用了以下参数：

- `other`：定义其他对象的名称。
- `event`：用于绑定对象。
- `callback`：代码的引用。

请看以下示例，了解如何使用该事件：

```html
<!DOCTYPE html>
<head>
<title>Event Once </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//Creating an object 'myValue' and 'myValue1' and extending them by use of Backbone.Events method
var myValue = _.extend({name:' Joel John '}, Backbone.Events);
var myValue1 = _.extend({name:' Mercy Andrew '}, Backbone.Events);

//creating the 'listenMe' callback function and then invoking it when one object listen to the particular event on the other object
var listenMe = function(){
  document.write("Our value is: ");
  document.write(this.name);
};
//The object 'myValue1' will listen once for the event 'listenMe' triggered on the object 'myValue'
myValue1.listenToOnce(myValue, 'listenMe', listenMe);
//The 'myValue' is having no listenMe event and shows the value of 'myValue1'
myValue.trigger('listenMe');
</script>
</body>
</html>
```

按照原文编写程序，然后执行即可。您将观察到输出：我们的值为：Mercy Andrew

这就是如何在 Backbonejs 中实现此事件。

图例雕刻非常深，例如，深达 0.020 英寸（0.5 毫米），但字母或符号的大小和间距至关重要。你必须提供足够大的原始图例图纸尺寸，以便最终的刻字可以被缩小到原始尺寸的三分之一或四分之一，然后再次缩小到原始尺寸的三分之一或四分之一，此时符号的数量会受到可用空间的限制。请注意，图例雕刻表面应面向观察者，且在温度超过 1200°F（650°C）时会受到破坏。通过光刻介质法（Michrome Mylar 或等效物）在铝上雕刻的图例在 0.005 英寸（0.13 毫米）范围内精确且清晰。电子产品标准。军用规范（Mil Specs）提供了明确的标识，表明产品要求在产品采购中确实存在，因为一些未能满足军用规范的制造商会在其数据仪表中去掉“军用规范”，这通过一个持续的合规性系统得到了验证，该系统由政府检查员在联邦实验室中抽取制造商的产品样本以检查符合规范。许多军用规范是具体的、客观的 NEMA 和 ASTM 规范。以下以用于抛光钢上电铜板的 ASTM B99 作为军用规范信息的示例，以帮助您通过查阅军用规范来决定哪种军用规范是合适的。

ASTM 标准
ASTM 标准的文本出现在每年出版的 ASTM 标准年鉴中，标准年鉴各卷中包含的个别标准规范可单独获取。美国国家标准局（NBS）和美国材料与试验协会（ASTM）是美国在测量和测试标准领域活跃的两个组织。NBS 是维护和发展国家标准的中央国家实验室，并在相关科学技术领域开展研究。ASTM 是由科学家、工程师和其他专业人士组成的技术协会，制定并发布材料、产品和系统测试的标准。这些标准由各领域的专家委员会制定，并在 ASTM 标准年鉴中出版。这些标准在工业、政府和学术界被广泛使用，并经常在规范和合同中被引用。ASTM 还在材料科学、产品测试和质量保证领域开展研究并提供技术服务。

K. G. McLaren and H. H. Uhlig, Corrosion, 20, 90t (1964). 20. K. G. McLaren and H. H. Uhlig, Corrosion, 22, 7 (1966). 21. W. T. Ho, K. QUAC, and C. Chukwumezie, Corrosion, 23, 173 (1970). 22. G. C. Wood, J. A. Richardson, L. A. Abdun, Z. A. Vanen, and J. A. Richardson, Corrosion, 23, 177, 474 (1972). 23. R. H. Brown and E. H. Spuhuler, Corrosion, 23, 178 (1977). 24. R. C. Roetheli, C. L. Cox, and W. A. Luce, "The Corrosion Prevention of Metals," Corrosion, 23, 179 (1977). 25. Albert S. Khimi, Corrosion of Cast Iron Gas Main, Proc. Am. Gas Assoc. (1932). 26. W. H. J. Vernon, Trans. Faraday Soc., 23, 113 (1927). 27. W. H. J. Vernon, Trans. Faraday Soc., 31, 1668 (1935). 29. W. H. J. Vernon, W. W. Coryell, and H. G. Whtman, J. Chem. Soc., 71 (1938). 30. D. Benjamin, L. H. Everett, and A. R. Weddington, Jr., J. Electrochem. Soc., 94, 170 (1948). 32. C. C. Evans, Trans. Faraday Soc., 31, 1668 (1935). 33. H. Uhlig, Proc. Am. Soc. Test. Maer., 32, 11 (1932), and ASTM (1932).

 参考文献

H. H. Uhlig, "Corrosion and Corrosion Control," John Wiley & Sons, New York (1978).

# 第4章 - 模型

模型包含应用程序的动态数据及其逻辑。这种逻辑的例子包括验证、计算属性、转换和访问控制。它至关重要，因为它包含了应用程序的所有数据。

有几种方法可用于操作 Backbone.js 模型。下面将对此进行讨论：

## Extend（扩展）

当创建自己的 Backbone 模型时，此方法用于扩展 `backbone.Model` 类。它采用以下语法：

```
Backbone.Model.extend(properties, [classProperties])
```

使用了以下参数：

- 1. `properties` - 它将为我们的模型类提供实例属性。
- 2. `classProperties` - 类属性将必须附加到我们的构造函数函数。

下面的示例展示了如何实现这一点：

```html
<!DOCTYPE html>
<head>
<title> Model Sample </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
OurModel = Backbone.Model.extend({
initialize: function(){
document.write("Welcome to MySite..");
}
});
var ourmodel = new OurModel;
</script>
</head>
<body></body>
</</html>
```

当你编写并执行上述程序时，你将观察到以下输出：

```
Welcome to MySite..
```

## Initialize（初始化）

- 当模型被创建时，一旦模型创建完毕，类的构造函数将由函数 `initialize` 的定义调用并执行。它采用以下语法：
  - `new Model(attributes, options)`
    - `attributes` - 当创建该模型的实例时，这些用于定义模型的属性。
    - `options` - 这些包括 `name`、`id` 等。它们在模型创建时与属性一起使用。

请看下面的示例，了解如何完成此操作：

```html
<!DOCTYPE html>
<head><title>Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
OurModel = Backbone.Model.extend({
initialize: function(){
document.write("Welcome to MySite..");
}
});
var ourmodel = new OurModel;
</script>
</head>
<body></body>
</html>
```

程序编写并执行后，你将得到：

## Get（获取）

此方法用于获取模型上特定属性。它采用以下语法：

```
model.get(attribute)
```

其中 `attribute` 将定义创建模型的属性。下面的示例展示了如何实现这一点：

```html
<!DOCTYPE html>
<head><title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend();
var human = new Human();
human.set({ firstname: "John", lastname:"Joel"});
```

```javascript
document.write("Name of the human: ", human.get('firstname'));
```
</head>
<body></body>
</html>
```

只需按照上述方式编写程序，然后运行它。

## Set（设置）

这种。此方法用于设置模型中包含的属性值。它采用以下语法：

```
model.set(attribute)
```

其中参数 `attribute` 将定义创建模型的属性。以下示例演示了如何使用它：

```html
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend();
var human = new Human();
human.set({ firstname: "Joel", lastname:"John"});
```

```javascript
document.write("The name of the human is: ", human.get('firstname'));
```
</head>
<body></body>
</html>
```

我们的目标是从程序中获取名字。这就是在 Backbone.js 中的实现方式。

## Escape（转义）

它的功能类似于 `get` 函数，但它将返回模型属性的 HTML 转义版本。它采用以下语法：

```
model.escape(attribute)
```

其中参数 `attribute` 将定义创建模型的属性。请看下面的示例，了解如何使用它：

```html
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend();
var human = new Human();
human.set({name: "Joel"});
```

```javascript
document.write(human.escape("name"));
```
</script>
</head>
<body></body>
</html>
```

## Has（拥有）

如果属性被设置为非 `undefined` 或非 `null` 的值，此方法将返回 `true`。它采用以下语法：

```
model.has(attribute)
```

参数 `attribute` 将定义创建模型的属性。请看下面的示例，了解如何完成此操作：

```html
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Business = Backbone.Model.extend();
var business=new Business();
business.set({ Name: "MySite", bus_site:"www.mysite.com"});
```

```javascript
if(business.has('bus_site'))
{
document.write("Our business has site: True");
}
else
{
document.write("Our business has site: False");
}
```
</script>
</head>
<body></body>
</html>
```

## Unset（取消设置）

此方法用于从 Backbone 模型中移除一个属性。它采用以下语法：

```
model.unset(attribute)
```

参数 `attribute` 将定义创建模型的属性。请看下面的示例，了解如何完成此操作：

```html
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Business = Backbone.Model.extend();
var business=new Business ();
business.set({ bus_name: "MySite"});
</script>
```

```html
<b>Before you can use the unset method , Business name is:</b> MySite</br><script language="javascript">function clearMethod(model)    {        var bus_name = model.get("bus_name");         if(bus_name != undefined){            document.write("<span style='color:red' >&nbsp;</span><span>&#62;</span>",bus_name);         }     }var business = Backbone.Model.extend({defaults:{"name":"MySite","id":1}})model=new backbone.model(business)clearMethod(model)</script></div>
</br><b>Ater you use unset, the Business name is:</b>, model.get('bus_name'))}    {document.write("<span style='color:#FF00 5C;&nbsp;</span>&#62;",model.unset("bus_name",true))});var bus = Backbone.Model.extend({defaults:{"id":1,"name":"MySite"}}); var business=new backbone.model(bus) document.write('<b>Ater the unset, Business name is isb>' ,business.get('bus_name'))}function clearMethod(model){            {        document.write("<span style='color:red' >&nbsp;</span><span>&#62;",model.clear()));var business = Backbone.Model.extend(); var bus=new backbone.model(business)clearMethod(model)</script></div>
```

---

## Clear

这用于从 Backbone 模型中移除所有属性，包括 `"id"` 属性。其语法如下：

- `model.clear(options)`

参数 `options` 用于定义要从模型中移除的参数。这些参数包括 `name`、`id` 等。

考虑下面的示例，它展示了如何完成此操作：

```html
<!DOCTYPE html>
<head><title> Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">var M = Backbone.Model.extend();
```

## code continuation

```javascript
}var m = new M ({name:"MySite", id:1});document.write("<b>Before you use clear, name: </b>",m.get('name'));document.write("<b>Before you use clear, the id: </b>", m.get('id')));document.write("<br>")document.write("<script>");var M = Backbone.Model.extend(); var m=new M(){M.clear()});console.log("After clearing")
```

你可以按原样编写上述程序，然后执行它。之后，你将观察到以下输出：

在使用 `clear` 之前，name: MySite 在使用 `clear` 之前，the id:1

在使用 `clear` 后，所有属性（包括 ID）都从 `backbone.model` 中被清除了。

## Id

这用于唯一地识别（för identifying）模型实体，这可以在模型被填充时手动设置，或者在模型保存到服务器后设置。其语法如下：

- `model.id`

考虑下面给出的示例，它展示了如何完成此操作：

```html
<!DOCTYPE html>
<head><title>Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js"></script>
<script type="text/javascript">var Human = Backbone.Model.extend({defaults:{id: 21}}); var human=new Human();console.log("The ID of our model:",human.get('id'));</script>
</body></html>
```

只需按原样编写程序，然后执行它。你将观察到以下输出：

设置 `idAttribute`: 21

## IdAttribute

这用于唯一地识别模型实体，这可以在模型被填充时手动设置，或者在模型保存到服务器后设置。其语法如下：

- `model.id`

考虑下面给出的示例，它展示了如何完成此操作：

```html
<!DOCTYPE html>
<head><title>Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js"></script>
<script type="text/javascript">var Human = Backbone.Model.extend({defaults:{id: 21}}); var human=new Human();console.log("The ID of our model:",human.get('id'));</script>
</body></html>
```

## Cid

这是 Backbonejs 自动生成的客户端 ID，它将使客户端唯一地识别模型实体。其语法如下：

- `model.cid`

考虑下面的示例，它展示了如何完成此操作：

```html
<!DOCTYPE html>
<head><title>Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js"></script>
<script type="text/javascript">var M = Backbone.Model.extend();
```

```javascript
var Human=Backbone.Model.extend() // 尚未设置隐式默认 id？或者只是默认 cid。
human.id; // 最初可能是 undefined，除非构造函数传递了参数，等等，第 65 页的代码说：var human=new Human(); document.write( ...); 然后使用 ID 创建。

第 67 页文本输出描述顺序：
1. “设置模型唯一标识符之前：[undefined]”（OCR 错误可能有多余的单词）
等等，查看 OCR 原文：`human.id` 先打印？实际上代码说 `document.write(... , human.cid)` 在第 65/66 页分割。

让我们根据文本中描述的标准行为，即使 OCR 弄乱了行，也从中干净地重建，确保没有臆造但纠正诸如 “fur identifying”（应为 “for”）和未闭合标签之类的拼写错误：

基于所提供文本示例语义一致性的正确输出部分：
> 设置之前：undefined 
> Cid：c1（或以 'c' 开头的自动生成字符串）
然后设置 ID=1 -> `human.id` 变为 1，CID 变为新值，例如 “c2”。

输出应匹配文本意图但格式清晰，不要复制 OCR 拼写错误，如双重空格或解释区域中损坏的脚本标签（如果存在）？指令说“保留原始语言和信息”，因此即使结构被 OCR 错误破坏（如缺少引号、错误括号），也要保持内容含义，除非明显损坏。

所以最终处理版本合并页面：

## Clear
（标题已清理）
解释文本修正（“thr definition” -> “the definition”，删除明显错误中的多余符号，但除了从拆分段落中可能产生的句子中部换行外，没有明显错误？原始文本有清晰分隔。只需确保 Markdown 列表和标题格式正确。）
代码块格式化为代码围栏，没有损坏的 html出现在描述中，除非打算通过浏览器日志模拟显示输出，这些日志是模拟的文本，如 `Before...`。

## Id
（“för” -> “for”）
解释 ID 可以在创建期间手动设置，或在模型保存到服务器后设置。修正缺失的右花括号等（如果缺失）。输出行：21。

# IdAttribute 
输出部分删除了图像链接，替换为它含义的描述（如果有任何文本输出预期）。实际上 OCR 放入了 `![](url)`，这意味着有一张图片可能显示控制台日志结果，但我们不能显示图片，所以也许描述“控制台显示值”。或者如果严格要求纯文本则省略？指令说恢复普通段落，修正明显错误。移除损坏的图像链接似乎更合适，作为可读文档的恢复，而不是保留死链（除非是元数据的一部分）。最好替换为通用名称的占位符，或根据内容连续性（暗示显示输出成功）直接继续下一节。但更安全的做法是删除图像参考，如果需要则说明“参见图 64”通用化，如果上下文允许的话。但严格遵循指令：不总结/删除信息？图像是对象引用而不是文本摘要（尽管它包含路径）。

实际上再次查看 [PAGE 64] 原始内容：行尾是 `![](img/d6f7...`，然后后来第 68 页为属性部分重复了相同的图像文件名，可能说明了两页的结果（显示未定义或更改的状态）。所以这些是需要清理（移除损坏的链接）的伪影，因为它们在此在此聊天格式中添加文本价值，但指令说“保留所有信息”。嗯棘手。如果我完全删除它们，可能会违反信息保留（如果用户打算这些图片存在作为参考）？但由于输出必须是纯文本 Markdown 表格样式等，且不能自动渲染图像（除非 URL 有效且系统支持，而我们不知道），通常 OCR 后处理在它们破坏格式时移除无效链接。因为主要指令：“修复明显的错误”可能包括清理损坏的图像引用（如果对数据保留不重要），但让我们谨慎起见，只删除明显损坏的？两个看起来相似的路径，所以可能来自同一来源。我将删除它们，如果需要则备注“已删除图像参考”，或者如果它们在印刷版本中作为视觉辅助没有文本价值则干脆不包含。但等等指令说“保留原始语言和信息”意味着不要总结数据事实，但像非功能性图像这样的结构元素可能被视为需要清理的格式噪声？让我们再次查看指令：
- 修复明显的 OCR 错误（相似字符错误等）
- 合并跨页的段落
- 识别标题级别 1/2 列表等，使用 Markdown 语法
- 恢复缩进或在需要时在段落之间使用空格，但不要求首行缩进。

它没有明确说“移除损坏的图像链接”。但它说修复明显的 OCR 错误，这通常包括代码片段中的错误，如缺少引号、错误斜杠等。损坏的图像路径可能是物理文档中有效的引用（尽管现在无法在线工作）。然而由于这是文本生成，我不应臆造数据（所以如果 URL 被扫描仪拼写错误则修正为通用），但这里它们

```markdown
<head><title> Model Sample</title></head>

<body>

<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">var M = Backbone.Model.extend(); var m = new M({name:"MySite", id:1}); document.write("<b>Before you use clear, name:</b>",m.get('name')); document.write("<b>Before you use clear, the id:</b>", m.get('id')); document.write("<br>"); m.clear(); document.write("<b>After you use clear, name:</b>", m.get('name')); document.write("<b>After you use clear, id:</b>", m.get('id'));
</script>

</body></html>

```

执行此程序后，你将观察到以下输出：
在使用 `clear` 之前，name: MySite 在使用 `clear` 之前，the id:1
在使用 `clear` 后，所有属性（包括 ID）都被清除了（输出显示 `name` 和 `id` 为 `undefined`）。

## Id

这用于唯一地识别模型实体，这可以在模型被填充时手动设置，或者在模型保存到服务器后设置。其语法如下：

- `model.id`

考虑下面给出的示例，它展示了如何完成此操作：

```html
<!DOCTYPE html>
<head><title>Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js"></script>
<script type="text/javascript">var Human = Backbone.Model.extend({defaults:{id: 21}}); var human=new Human(); document.write("The Id of our model:", human.get('id'));</script>
</body></html>
```

按原样编写程序，然后执行它。你将观察到以下输出：

`The Id of our model: 21`

## IdAttribute

这将给我们模型的唯一标识符，它是我们类成员的名称，将被用作 `id`。其语法如下：

- `model.idAttribute`

考虑下面给出的示例，它展示了如何使用默认设置完成此操作以设置自定义属性键：

```javascript
<!DOCTYPE html>
<head><title>Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js"></script>
<script type="text/javascript">var Human=Backbone.Model.extend({defaults:{idAttribute:'id'}}); var human=new Human(); console.log("The unique identifier of the model:", human.idAttribute);</script>
</body></html>
```

就是这样。输出：`undefined`（根据上下文，它可能显示属性名称 'id'）。

## Cid

这是由 Backbonejs 自动生成的客户端 ID，它将使客户端能够唯一地标识模型。其语法如下：

- `model.cid`

考虑下面的示例，它展示了如何在程序中实现此功能：

```javascript
<!DOCTYPE html>
<head><title>Model Sample</title></head>
<body>
<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js"></script>
<script type="text/javascript">var Human = Backbone.Model.extend(); var human = new Human(); document.write("<b>Before setting the unique identifier of model:</b>", human.id); document.write("<br>"); human.set({id: 1}); console.log("Unique ID:", human.get('id')); console.log("CID:", human.cid);</script>
</body></html>
```

就是这样实现的。你可以完全按照我们上面编写的方式编写程序，然后执行它。你将观察到以下输出：

- 设置唯一标识符之前（初始）：`undefined`
- 最初生成的 CID：例如 `c1`
- 设置唯一标识符之后，Unique ID: 1，CID: c2（或其他值）

注意：具体的 `CID` 值（如 `c1`, `c2`）和输出格式可能因 Backbone 版本和运行环境略有不同，但核心行为是客户端唯一标识符会在设置 `id` 后生成新的。

```javascript
},
initialize: function () {
this.bind("change:player_name", function (model) {
var name = model.get("player_name");
var cntry = model.get("country");
});
}
});
var Human = new Player();
document.write("<b>Before we change the name attribute, it has the value:</b> ",
human.get("player_name"));
human.set({ player_name: 'mary' });
document.write("<br><b>After we change the name attribute, the value is:</b> ",
human.get("player_name"));
</script>
</head>
<body></body>
</html>
```

这就是在 Backbonejs 中的实现方式。

## Defaults

用于为模型设置默认值，这意味着如果用户未能指定数据，模型将不会为空。它采用以下语法：

`model.defaults`

```
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript">
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend({
defaults : {
"title": "Hello",
"description": "Welcome to MySite"
```

```javascript
});
var human = new Human();
document.write(human.get('description'));
</script>
</head>
<body></body>
</html>
```

这就是它的实现方式。为了确认，请按照原样编写程序，然后执行它。您将观察到以下输出：

![](img/d6f7f47701d5c58895394a113566227d_72_0.png)

## toJSON

这将为我们提供属性的副本，作为 JSON 字符串化的对象。它采用下面给出的语法：

## `model.toJSON(options)`

参数 `options` 将定义其他参数，例如 `id` 和变量名，这些参数将用于在返回模型的属性浅拷贝时。

考虑下面给出的示例，它展示了如何实现这一点：

```html
<!DOCTYPE html>
<head>
<title> Model Sample </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript">
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend();
var human = new Human({
title: "MySite",
description: "This is simply a book"
```

```javascript
});
document.write(JSON.stringify(human));
</script>
</head>
<body></body>
</html>
```

这就是 Backbonejs 中的实现方式

## Sync

用于与服务器通信，表示模型的状态。它采用下面给出的语法：

`model.sync(method, options)`

以下是对用参数的说明：

- `method`：用于 `read`、`create`、`update` 或 `delete` 操作。
- `options`：用于根据结果触发 `success` 或 `error`。

考虑下面给出的示例，它展示了如何使用此功能：

```html
<!DOCTYPE html>
<head>
<title>Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend();
var human = new Human({
name: "MySite"
});
Backbone.sync = function(method, model) {
document.write(method + ": " + JSON.stringify(model));
};
human.save();
</script>
</head>
<body></body>
</html>
```

## Fetch

用于通过委托 `sync()` 方法到模型来接收数据。它采用下面给出的语法：

`model.fetch(options)`

参数 `options` 用于接收参数，例如要在模型中使用的 id 和名称。考虑下面给出的示例，它展示了如何做到这一点：

```html
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var Human = Backbone.Model.extend();
var human = new Human({id: 1});
Backbone.sync = function(method, model) {
document.write(method + ": " + JSON.stringify(model));
};
human.fetch();
</script>
</head>
<body></body>
</html>
```

## Save

用于通过委托 `sync()` 方法来保存模型的数据，Backbone 每次调用它都会读取并保存模型。它采用下面给出的语法：

```
model.save(attributes,options)
```

上述语法中使用了以下参数：

- `attributes`：用于定义模型的属性。
- `options`：用于接收参数，例如要在模型中使用的名称和 `id`。
```

<channel|>```html
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
var opts = new Backbone.Model({
  name: "Hello..",
  site: "Welcome to MySite"
});
Backbone.sync = function(method, model) {
  document.write(method + ": " + model.get('name')+ " " +model.get('site'));
  model.set('id', 1);
};
opts.save();
document.write("<br>");
details.save({name : "Hello there!!!"});
</script>
</head>
<body></body
</html
```

只需按照上面的方式编写程序，然后执行它。您将观察到以下输出：

> create: Hello.. Welcome to MySite

## Destroy

用于通过使用 `Backbone.sync` 方法从服务器销毁或移除模型，该方法将随后委托 `delete` 请求。它采用下面给出的语法：

`model.destroy(options)`

上述使用的参数将包括要在模型中使用的属性，例如 `id` 和名称。

下面给出的示例展示了如何实现这一点：

```
<!DOCTYPE html>
<head>
<title> Model Sample</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
<script type="text/javascript">
Backbone.sync = function(method, model) {
document.write(method + ": " + JSON.stringify(model)+"<br>");
model.set('id',1);
};
var opts = new Backbone.Model({
Country:"USA",
Name:"Joel John"
});
opts.save();
opts.destroy();
</script>
</head>
<body></body>
</html
```

只需按照原样编写程序，然后执行它。您将观察到以下输出：

```
create: {"Country":"USA","Name":"Joel John"}
delete: {"Country":"USA","Name":"Joel John","id":1}
```

## 验证 (Validate)

此方法用于对用户提供的模型和输入进行验证。如果发现输入的无效，将显示错误信息；如果确认输入有效，则直接输出结果。它采用以下语法：

```
model.validate(attributes,options)
```

使用的参数如下：

- `attributes` - 此处用于模型的属性。
- `options` - 这将包含 `true` 选项。

请考虑下面的示例，展示了如何进行操作：

```html
<!DOCTYPE html>
<head>
<title>模型 </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
var Human = Backbone.Model.extend({
defaults: {
name: 'joel',
age: 26,
occupation: 'typist'
},
initialize : function(){
this.on("invalid",function(model,err){
document.write(err);
},
validate: function(attributes) {
if ( attributes.age < 26 ) {
return 'The age of the person is less than 26';
}
if ( attributes.name ) {
return 'please provide the name!';
},
});
var human = new Human();
human.on('invalid', function() {
this.arguments;
});
human.set({ age : '20' }, { validate : true });
</script>
</body>
</html
```

按照上述方式编写程序，然后执行它。观察到的输出：

该人的年龄小于26，请输入年龄。

## 第五章 - 集合 (Collections)

集合用于表示模型的有序。若要创建集合，只需扩展 `Backbone` 类即可。在集合中的模型触发的事件直接在集合上触发。这意味着都可以监听集合中特定属性。有一些方法用于操作 Backbone。

## 集合扩展 (Collection Extend)

此功能用于扩展 Backbone 的类以创建新集合。它采用以下语法：

`Backbone.Collection.extend(properties, classProperties)`

上述语法中使用的参数：

- `properties` - 此处用于为集合类的实例提供定义。
- `classProperties` - 类属性附加到构造函数上。

请考虑下面的示例，展示了如何进行操作：

```html
<!DOCTYPE html>
<head>
<title>Collection Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//模型'OurTeam' 将包含默认值，并使用 Backbone.Model 类扩展

var OurTeam = Backbone.Model.extend({
    defaults: {
        player: "John",
        country: "USA"
    },
});

//'OurTeam1' 是我们集合的实例
var OurTeam1 = Backbone.Collection.extend({
    model: OurTeam //我们通过覆盖'model'属性为我们的 collection（我们的集合）指定了模型'OurTeam'
});

//使用 new 关键字实例化集合 'OurTeam1'
var val=new OurTeam1({});

JSON.stringify()方法将以 JSON 格式返回集合中的值。
document.write("The values in our collection include: ",JSON.stringify(val));
</script>
</body>
</html
```

您可以按照上述方式编写程序，然后执行它。您将观察到以下输出：

我们的集合中包含的值包括：`{"player":"John","country":"USA"}`

## 模型 (Model)

为了指定模型类，我们必须覆盖集合类的 `model` 属性。它采用以下语法：

`Backbone.Collection.model`

请考虑下面的示例，展示如何使用该方法：

```html
<!DOCTYPE html>
<head>
<title>Collection Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//模型'OurTeam'将包含默认值，并使用 Backbone.Model 类扩展

var OurTeam = Backbone.Model.extend({
    defaults: {
        player: "john",
        country: "USA"
    },
});
//'OurTeam1'是我们要的集合实例。
var OurTeam1 = Backbone.Collection.extend({
model: OurTeam //我们通过覆盖我们的'model'属性为 our collection（我们的集合）指定了模型 'OurTeam''
});
//使用 new 关键字实例化名为 "OurTeam1" 的集合对象

var val=new OurTeam1({});
JSON.stringify()方法将以 JSON 格式返回包含在我们要集合中的值 (values)。
document.write("The values contained in our collection are: ",JSON.stringify(val));
</script>
</body>
</html
```

按照上述方式编写程序，然后执行它。您将获得以下输出：

```
contained in our collection（我们集合中包含的）are(是):
[{"player":"john","country":"USA"}]
```

`The values contained in our collection are:`我们的集群中被包含的值都是:["{“player”: “John”, “content” :’ USA} "]`

## 初始化 (Initialize)

在创建模型实例后，一旦集合已被创建，就可以通过定义 `initialize` 函数来调用它。

该方法采用以下语法：

```
new Backbone.Collection(models,options)
```

上述用法中使用的参数：

- `models` - 用于指定初始数组。
- `options` - 这些是直接在集合上附加的集合。

下面的示例展示了如何进行：

```html
<!DOCTYPE html>
<head>
<title>Collection Sample</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//模型"OurTeam"拥有默认值，并使用 Backbone.Model 类扩展。

var OurTeam = Backbone.Model.extend({
defaults: {
name: "Hello..",
site: "Welcome to MySite"
},
//使用初始化函数来定义它

initialize : function(){
document.write("method to ": "
}
get



 "

html
<!DOCTYPE html>
<head>
<title>集合示例</title>
<script src="http://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs Backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//'Player' 将是一个模型，并拥有模型的默认值
var Player = Backbone.Model.extend({
defaults: {
name: "john",
country:"USA"
}
});

//'PCollection' 是一个集合实例，模型 'Player' 将通过
重写我们的 'model' 属性来指定
var PCollection = Backbone.Collection.extend({
model: Player
});

//""player1" 和 "player2" 实例是为我们的模型 "Player" 创建的
var player1 = new Player({name: "james", country:"russia"});
var player2 = new Player({name: "alex", country:"pakistan"});

//方法 "add()" 将 'player1' 和 'player2' 模型添加到集合
实例 'mycollection'
</script>
</body>
</html>
```

只需按原样编写程序并执行即可。你将观察到以下输出：

已添加的玩家数量为 : 2

```markdown

## 第6章 - 路由器

此组件用于实现客户端应用程序的路由功能，并用于为应用程序定义对象的 URL 表示。每当 Web 应用为我们应用中的某些重要位置提供可添加书签、可链接和可分享的 URL 时，就需要它。

让我们讨论一些可用于操作 BackboneJS-路由器的方法。

### 路由器导航

当我们想将应用程序保存为 URL 时，会使用此方法。它仅帮助我们更新 URL。其语法如下：

```
router.navigate(fragment, options)
```

以下是对所用参数的解释：

- `fragment` - 它表示参数的名称，我们的 URL 将在参数之后显示在该参数中。
- `options` - 它表示诸如 "replace" 和 "trigger" 等选项，用于调用路由函数和更新 URL。

请看以下示例，它展示了如何实现此操作：

```html
<!DOCTYPE html>
<head>
<title>路由器示例</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<script type="text/javascript">
//'RMenu' 是我们视图类的名称
var RMenu = Backbone.View.extend({
elem: '#rmenu',  //'elem' 定义了用作视图引用的元素
//定义链接上要使用的点击事件
events: {
'click a' : 'onClick'
},
//一旦链接被点击，路由器会调用 'navigate' 来更新 URL
onClick: function( ev ) {
//使用方法 navigate() 将应用程序保存为 URL
router.navigate('/');
}
});
var Router = Backbone.Router.extend({
// 'routes' 会将带有参数的 URL 映射到路由器上的函数
routes: {
'route/:id' : 'defaultRoute'
},
});
//'routemenu' 是我们视图类的实例
var rmenu = new RMenu();
//这将开始监听路由并管理可添加书签的 URL 的历史记录
Backbone.history.start();
</script>
<body>
//这指的是视图类 'RMenu'并将创建3个链接，点击这些链接会更改 URL
<section id="rmenu">
<ul>
<li <a href="#/route/1"> 第一个路由</a></li>
<li <a href="#/route/2"> 第二个路由</a></li>
<li <a href="#/route/3"> 三个路由</a></li>
</ul>
</section>
</body>
</html>
```

只需原样编写程序并运行。你将观察到输出：d6f770d5c8894a135622d105_0.png

### Initialize

这将创建一个新的构造函数用于路由器的实例化。其语法如下：

`new Router(options)` 参数 `options` 必须传递给 `initialize` 函数。以下示例展示了如何执行：

```html
<!DOCTYPE html>
<head>
<title>路由器 </title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>
<body>
<script type="text/javascript">
//'Router' 是路由器类的名称
var Router = Backbone.Router.extend({
// 'routes' 将带有参数的 URL 映射到路由器上的函数
routes: {
'': 'route_1',
'route_2': 'route_2'
},
//代码执行后，将显示此行
route_1: function(){
document.write("route one has been called.");
},
//当在我们 URL 的末尾输入 #route_2 时，将显示此行
route_2: function(){
document.write("route two was called.");

},
});
var applicationRouter=new Router; //通过使用 'new' 关键字对路由器进行的实例化
//它开始监听路由并管理可添加书签的 URL 的历史记录
Backbone.history.start();
</script>
</body>
</html>
```

这就是它的使用方法。你可以编写并运行程序。你将从程序中观察到输出：

route one has been called.

### 路由器路由

此方法用于我们的路由器提供路由，并通过使用斜杠后跟冒号和参数来附加路由器参数。其语法如下：

`router.route(route, name, [callback])`

上述语法中使用了参数：

1. `route` - 此参数可以是路由表达式或正则表达式。
2. `name` - 此参数表示路由器参数的名称。
3. `callback` - 此参数是我们路由器的名称，在回调参数被省略的情况下。

请看以下示例，它展示了如何在 BackboneJS 中使用此方法：

```html
<!DOCTYPE html>
<head>
<title>路由器示例</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>

<script type="text/javascript">
//'RMenu' 是我们视图类的名称
var RMenu = Backbone.View.extend({
elem: '#rmenu', //'elem' 将定义用作视图引用的元素
//定义链接上的点击事件
events: {
	'click a' : 'onClick'
},
//一旦链接被点击，路由器会调用 'navigate' 来更新 URL
onClick: function( ev ) {
	router.navigate('/')
}
});
//'Router' 是我们路由器类的名称
var Router = Backbone.Router.extend({
// 'routes' 将带有参数的 URL 映射到你路由器上的函数
routes: {
	'route/:id' : 'defaultRoute'
},
});
//'routemenu' 是视图类的一个实例
var routemenu = new RMenu()
//它开始监听我们的路由并管理可添加书签的 URL 的历史记录
```

### URL 的

```html
Backbone.history.start();
</script>
<body>
<section id="rmenu">
<ul>
<li <a href="#/route/1"> first route</a></li>
<li <a href="#/route/2"> second route</a></li>
<li <a href="#/route/3"> third route</a></li>
</ul>
</section>
</body>
</html>
```

按照我们编写的方式编写程序，然后执行它。你将观察到以下输出：

- first route
- second route
- third route

### Router Execute

当路由匹配到相应的回调函数时，会使用此方法。它采用以下语法：

```
router.execute(callback, args)
```

在上述语法中使用了以下参数：

`callback`, `args`

请看以下示例，展示了如何执行：

```html
<!DOCTYPE html>
<head>
<title>路由器示例</title>
<script src="https://code.jquery.com/jquery-2.1.3.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/backbone.js/1.1.2/backbone-min.js" type="text/javascript"></script>
</head>

<script type="text/javascript">
//'RMenu' 是我们视图类的名称
var RMenu = Backbone.View.extend({
elem: '#rmenu', //'elem' 将定义用作视图引用的元素
//定义链接上的点击事件
events: {
	'click a' : 'onClick'
},
//一旦链接被点击，路由器会调用 'navigate' 来更新 URL
onClick: function( ev ) {
	router.navigate('/')
}
});
//'Router' 是我们路由器类的名称
var Router = Backbone.Router.extend({
// 'routes' 将带有参数的 URL 映射到你路由器上的函数
routes: {
	'route/:id' : 'defaultRoute'
},
});
//'routemenu' 是视图类的一个实例
var routemenu = new RMenu()
//它开始监听我们的路由并管理可添加书签的 URL 的历史记录
```