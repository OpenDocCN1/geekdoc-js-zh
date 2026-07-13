# AngularJS 手册：简易Web应用开发

## 免责声明

尽管已尽力验证本书中提供的信息，但作者对其中包含的主题内容的错误、遗漏或相反解释不承担任何责任。本书提供的信息仅供教育和娱乐之用。读者应对自己的行为负责，作者不承担因使用这些信息而产生的任何责任或损害（无论是实际还是感知的）。

所使用的商标未经任何同意，商标的发布未经商标所有者的许可或支持。本书中的所有商标和品牌仅用于说明目的，归其所有者所有，与本文件无关。

# 第 1 章 - AngularJS 概述

该框架通过扩展 HTML 提供的功能来工作。如果 HTML 是为了开发 Web 应用而创建的，那么它就会是 AngularJS。HTML 在声明静态文档方面表现最佳。然而，它并不适合在我们的 Web 应用中声明动态视图。使用 Angular，可以极大地扩展应用中使用的 HTML 词汇。完成此操作后，您将获得一个易于阅读、表达力强且开发速度更快的环境。

在本书中，我们将探讨 AngularJS 的各种特性，作为开发人员，您可以利用这些特性来改善应用的外观和感觉。

# 第 2 章 - [AngularJS](https://github.com/angular/bower-material) 与 HTML

如您所知，AngularJS 用于扩展 HTML 的功能。大多数人都知道如何使用标准 HTML。然而，AngularJS 用于扩展其功能。在本章中，我们想要创建一个 HTML 页面，然后将用 HTML 编写的代码转换为模板，该模板将由 AngularJS 使用，以便动态显示相同的数据。HTML 页面中只会添加基本信息。

以下是网页的第一个代码：

```html
<ul>
<li>
   <span> Motorola </span>
<p>
    I really like Motorola phones.
</p>
</li>
<li>
    <span>Nokia are the best in Wi-Fi connection</span>
<p>
    I really like to make use of devices.
</p>
</li>
</ul>
```

您可以继续向上述文件添加静态 HTML。下面给出了一个示例：

```html
<p> The number of available phones is: 2</p>
```

在示例中，我们仅使用静态 HTML 来呈现我们刚刚创建的网页内容。使用 AngularJS，可以动态呈现相同的内容。

我们的目标是使我们创建的页面变得动态。还应实现一个测试用例，以便测试我们创建的控制器。在 AngularJS 中，使用 MV 模型（模型-视图-控制器）来组织应用的结构。通过这种方式，代码被解耦，并实现了关注点分离的概念。模型、视图和控制器将被添加到这个应用中。Angular 中的工作方式是，模型通过视图投影到模板中。这表明，如果某些内容发生变化，所有绑定点也会更新，以便视图得到更新。在 Angular 中，视图是从模型构建的。

考虑下面给出的示例：

```html
<html ng-app="myApp">
<head>
...
<script src="myapps/angular/angular.js"></script>
<script src="js/controllers.js"></script>
</head>
  <body ng-controller="mply “Repeat”?PnListCtrl">
<ul>
<li ng-repeat="model in phones">
<span>{{model.name}}</span>
<p>{{model.snippet}}</p>
    </li>
  </ul>
</body>
</html>
```

您应该注意到，硬编码的手机列表已被 AngularJS 表达式和 `ngRepeat` 指令所取代。

应用的控制器应该只是一个构造函数，它将接受参数 `$scope`。如下所示：

```javascript
var myApp = angular.module('myApp', []);
   myApp.controller('PhoneListCtrl', function ($scope) {
$scope.phones = [
   {'name': 'Motorola,
'snippet': ' I really like Motorola phones.
.'},
  {'name': ' Nokia are the best in Wi-Fi connection ',
   'snippet': 'Their devices are really liked by many.'},
   {'name': 'MOTOROLA XOOM™',
  'snippet': ' I really like to make use of devices.
.'}
];
});
```

我们所做的是声明了控制器，然后最终将其链接到模块。

## 测试

在 AngularJS 中，控制器和视图是分离的。这样，即使在开发过程中，代码也变得可测试。如果控制器在全局空间中可用，那么我们可以模拟 `scope` 对象来实例化它。如下例所示：

```javascript
describe('PnListCtrl', function(){
   it(' a "phones" model with 2 phones should be created', function() {
var scope = {},
   ctrl = new PnListCtrl(scop);
   expect(scop.phones.length).toBe(2);
});
});
```

然后应该创建非全局控制器。没有人希望他们的控制器函数位于全局命名空间中。相反，大多数人希望它通过我们刚刚创建的模块的匿名构造函数进行注册。

在这种情况下，我们将由 AngularJS 的 `$controller` 服务来证明。该服务将负责通过名称检索控制器。考虑下面给出的示例，展示了如何实现这一点：

```javascript
describe('PnListCtrl', function(){
   beforeEach(module('pncatApp'));
   it('you should create "phones" model with the 2 phones', inject(function($controller) {
var scope = {},
   ctrl = $controller('PnListCtrl', {$scope:scope});
   expect(scope.phones.length).toBe(2);
}));
});
```

我们所做的是指示 Angular 在任何测试之前加载每个模块。然后应将 `$controller` 服务注入到我们的服务中。该服务还用于创建新的 `PnListCtrl`。然后使用该实例进行验证。

## 实验

可以向文件添加另一个绑定。如下所示：

```html
<p>The available number of phones: {{phones.length}}</p>
```

可以在控制器中创建一个新的模型属性，然后从模板进行绑定。下面给出了一个示例：

```javascript
$scope.name = "John";
```

可以按如下方式将新绑定添加到文件：

```html
<p>Hi, {{name}}!</p>
```

现在您可以刷新浏览器并观察发生了什么。然后应更新 `./test/unit/controllersSpec.js` 中的控制器单元测试，以反映新的更改。




接下来，应在文件中创建一个用于生成简单表格的重复器。实现方式如下：

```
<table>
   <tr><th>行号</th></tr>
   <tr ng-repeat="j in [0, 1, 2, 3, 4, 5, 6, 7]"><td>{{j}}</td></tr>
</table>
```

然后将列表修改为以下内容：

```
<table>
  <tr><th>行号</th></tr>
  <tr ng-repeat="j in [0, 1, 2, 3, 4, 5, 6, 7]"><td>{{j+1}}</td></tr>
</table>
```

`ng-repeat` 可用于创建具有其他规格的表格。这在 Angular 中也非常强大。此时，你将拥有一个动态运行的应用程序，并且其模型、视图和控制器分别位于不同位置。

# 第 3 章 - XHR

你不应总是在应用程序中处理小型且硬编码的数据。我们应该能够通过使用名为 `$http` 的预构建服务，从 AngularJS 服务器获取大型数据集。

我们将有一个文件 `app/phones/devices.json`，其中包含我们拥有的手机列表。这些数据将以 JSON 格式存储。该文件的一个示例部分如下所示：

```
[
  {
    "age": 15,
    "id": "motorola ",
    "name": "Motorola DEFY\u2122 with MOTOBLUR\u2122",
    "snippet": "你喜欢使用摩托罗拉设备和手机吗？"
  },
  ...
]
```

## 控制器

Angular 的 `$http` 服务将在控制器中使用，用于向 Web 服务器发出 HTTP 请求，以便从文件 `app/phones/devices.json` 获取数据。这只是处理此类操作或与 Web 应用相关操作的一种方式。使用 AngularJS，这些服务会被注入到需要它们的地方。

控制器的代码应如下所示：

```
var myApp = angular.module('myApp', []);
myApp.controller('PnListCtrl', function ($scope, $http) {
  $http.get('phones/devices.json').success(function(data) {
    $scope.phones = data;
  });
  $scope.orderProp = 'age';
});
```

要在 Angular 中使用服务，需要将所需的依赖项名称定义为控制器构造函数函数的参数。如下所示：

```
myApp.controller('PnListCtrl', function ($scope, $http) {...}
```

AngularJS 中的依赖构造函数会在启动后为我们的控制器提供服务。它还会处理服务可能需要的任何传递依赖项的创建。考虑下面的示例，展示了如何实现这一点：

```
var myApp = angular.module('myApp', []);
myApp.controller('PnListCtrl', ['$scope', '$http',
  function ($scope, $http) {
    $http.get('phones/devices.json').success(function(data) {
      $scope.phones = data;
    });
    $scope.orderProp = 'age';
  }
]);
```

测试可以按如下方式进行：

```
describe('myApp controllers', function() {
  describe('PnListCtrl', function(){
    var scope, ctrl, $httpBackend;

    // 在测试前加载我们的应用模块定义。
    beforeEach(module('myApp'));

    // 注入器会忽略这里的前导和下划线（即 _$httpBackend_）。
    // 这将允许我们注入服务，同时将其附加到与服务同名的变量上，以避免名称冲突。
    beforeEach(inject(function(_$httpBackend_, $rootScope, $controller) {
      $httpBackend = _$httpBackend_;
      $httpBackend.expectGET('phones/devices.json').
        respond([{name: 'Motorola'}, {name: 'Motorola Phone'}]);
      scope = $rootScope.$new();
      ctrl = $controller('PnListCtrl', {$scope: scope});
    }));
  });
});
```

注意上述测试用例中的两个辅助函数。它们可用于配置和访问注入器。

考虑下面的代码：

```
it('你应该创建包含从 xhr 获取的两个手机的 "phones" 模型', function() {
  expect(scope.phones).toBeUndefined();
  $httpBackend.flush();
  expect(scope.phones).toEqual([{name: 'Motorola'},
    {name: 'Motorola Phone'}]);
});
```

我们希望在收到响应之前，对作用域上不存在的模型进行验证。调用 `$httpBackend.flush()` 函数后，请求队列将被刷新到浏览器。`$http` 服务返回的 promise 将使用我们解析的响应进行解析。我们将进行断言，然后验证模型是否属于作用域。然后我们可以验证 `orderProp` 是否已正确设置。如下所示：

```
it('应为 orderProp 模型设置默认值', function() {
  expect(scope.orderProp).toBe('age');
});
```

在 karma 选项卡中，应观察到以下输出：

```
Chrome 22.0: Executed 2 of 2 SUCCESS (0.028 secs / 0.007 secs)
```

可以在文件底部添加 `<pre>{{phones | filter:query | orderBy:orderProp | json}}</pre>`，以便以 JSON 格式列出或显示可用的手机。可以在回调中添加以下内容：

```
$scope.devices = data.splice(0, 5);
```

# 第 4 章 - 链接与图片

你应该知道如何为列表中的设备添加缩略图。还应添加指向这些设备的链接。

请注意，在 JSON 文件中，设备的链接及其 URL 以及唯一 ID 都是可用的。URL 应指向 `app/img/devices/`。

考虑下面的代码片段：

```
[
  {
    ...
    "id": "motorola ",
    "imageUrl": "img/phones/motorola.0.jpg",
    "name": "Motorola PHONE ",
    ...
  },
  ...
]
```

模板应如下所示：

```
...
<ul class="phones">
  <li ng-repeat="device in phones | filter:query | orderBy:orderProp" class="thumbnail">
    <a href="#/phones/{{device.id}}" class="thumb"><img ng-src="{{device.imageUrl}}"></a>
    <a href="#/phones/{{device.id}}">{{device.name}}</a>
    <p>{{device.snippet}}</p>
  </li>
</ul>
...
```

在 `href` 的属性值中使用了双花括号绑定，以便动态生成链接。在第二步中，将绑定 `{{device.name}}` 添加为内容元素。

使用了 `ngSrc` 指令来为每个设备添加图片。测试可以按如下方式实现：

```
...
it('应渲染设备特定的链接', function() {
  var myquery = element(by.model('query'));
  myquery.sendKeys('nexus');
  element.all(by.css('.phones li a')).first().click();
  browser.getLocationAbsUrl().then(function(url) {
    expect(url).toBe('/phones/motorola');
  });
});
...
```

我们需要验证应用程序是否为可能需要实现的设备视图生成了正确的链接。`ngSrc` 指令可以替换为普通的 `src`。

# 第 5 章 - 使用动画

有时，你可能需要通过添加一些动画来增强应用程序。这可以通过使用 CSS 和 JavaScript 来实现。为了在整个应用程序中启用动画，我们必须使用 `ngAnimate` 模块。必须使用常见的 `ng` 指令来触发我们正在接入的动画的钩子。这应该自动完成。一旦找到动画，它将在标准 DOM 元素之间执行，该元素在给定时间被发出到该元素。可以使用 `ngRepeat` 和 `ngClass` 来实现这一点，只需向它们添加或删除元素即可。

AngularJS 模块 `ngAnimate` 将为我们提供执行动画的功能。该模块已与我们的核心 Angular 框架分开分发。为了执行额外的动画，我们将使用 jQuery。

我们现在需要安装要在应用程序客户端使用的依赖项。可以使用 Bower 来实现这一点。我们需要更新配置文件 `bower.json`，使其包含新的依赖项。可以按如下方式操作：

```
{
  "name": "angular-seed",
  "description": "一个用于 AngularJS 启动的项目",
  "version": "0.0.0",
  "homepage": "https://mysite.com/angular/angular-project",
  "license": "MIT",
  "private": true,
  "dependencies": {
    "angular": "1.4.x",
```




```
"angular-mocks": "1.4.x",
"jquery": "~2.1.1",
"bootstrap": "~3.1.1",
"angular-route": "1.4.x",
"angular-resource": "1.4.x",
"angular-animate": "1.4.x"
}
}
```

上述步骤中安装的所有元素都应兼容，否则会出现问题。`bower` 也已被告知安装 jQuery。然而，这不能说是 Angular 库，而是一个标准的 jQuery 库。

通过执行以下命令，指示 `bower` 下载并安装依赖项：`npm install`

请注意，如果在您上次执行上述命令之后发布了新版本的 Angular，则可能会出现不兼容问题。要解决此问题，您只需在执行上述命令之前删除 `app/bower_components` 文件夹。

## 模板

我们需要对 HTML 模板进行一些更改，以便链接定义动画的资源文件和 `angular-animate.js` 文件。动画模块，即 `ngAnimate`，定义在此文件中，其中包含负责让应用程序感知动画效果的代码。

需要对文件进行以下更改：

```
...
<!—这是用于 CSS 过渡和/或关键帧动画 -->
<link rel="stylesheet" href="css/animations.css">
...
<!—jQuery 将用于 JavaScript 动画（应在 angular.js 之前包含） -->
<script src="bower_components/jquery/dist/jquery.js"></script>
...
<!—这是在 AngularJS 中启用动画支持所需的模块 -->
<script src="bower_components/angular-animate/angular-animate.js"></script>
<!—这是用于 JavaScript 动画 -->
<script src="js/animations.js"></script>
...
```

对于使用 Angular 1.4 版本的用户，请确保您使用的是 jQuery 2.1 或更高版本。任何低于此版本的 jQuery 都将与 Angular 1.4 不兼容。这意味着动画将无法被检测到，或者可能以非预期的方式工作。

动画可以在 CSS 代码（`animations.css`）或 JavaScript 代码（`animations.js`）中实现。我们需要首先创建一个新模块，该模块将 `ngAnimate` 模块作为依赖项，就像我们在 `ngResource` 中所做的那样。

`animations.js` 文件应如下所示：

```
angular.module('myAnimations', ['ngAnimate']);
   // ...
// 此模块将用于稍后定义动画
   // ...
```

然后，该模块应附加到应用程序模块。如下所示：

```
// ...
angular.module('myApp', [
'ngRoute',
'myAnimations',
'myControllers',
'myFilters',
'myServices',
]);
// ...
```

此时，我们的模块将能够感知动画。

## 使用 CSS 过渡动画实现“ngRepeat”动画

应将 CSS 动画添加到包含我们设备的网页中的 `ngRepeat` 指令。我们首先需要向已重复的元素添加一个额外的 CSS 类，以便将其与 CSS 动画代码挂钩。如下所示：

```
<!--
让我们更改重复器的 HTML，以包含一个新的 CSS 类
稍后我们将用它来实现动画：
-->
<ul class="phones">
<li ng-repeat="device in phones | filter:query | orderBy:orderProp"
class="thumbnail device-listing">
<a href="#/phones/{{device.id}}" class="thumb"><img ng-src="{{device.imageUrl}}"></a>
<a href="#/phones/{{device.id}}">{{device.name}}</a>
<p>{{device.snippet}}</p>
</li>
</ul>
```

请注意 CSS 类是如何添加的。HTML 文件中需要这样做，以便动画能够正常工作。

动画的 CSS 代码应如下所示：

```
.device-listing.ng-enter,
.device-listing.ng-leave,
.device-listing.ng-move {
    -webkit-transition: 0.5s linear all;
    -moz-transition: 0.5s linear all;
    -o-transition: 0.5s linear all;
    transition: 0.5s linear all;
}
.device-listing.ng-enter,
.device-listing.ng-move {
   opacity: 0;
   height: 0;
   overflow: hidden;
}
.device-listing.ng-move.ng-move-active,
.device-listing.ng-enter.ng-enter-active {
    opacity: 1;
    height: 120px;
}
.device-listing.ng-leave {
    opacity: 1;
    overflow: hidden;
}
.device-listing.ng-leave.ng-leave-active {
    opacity: 0;
    height: 0;
    padding-top: 0;
    padding-bottom: 0;
}
```

`device-listing` 的 CSS 类与动画钩子结合，这些钩子会在项目被插入列表或从列表中移除时触发。

当新设备被添加到列表并显示在页面上后，`ng-enter` 类将应用于该元素。当元素在列表中被移动后，`ng-move` 类将应用于该元素。当元素从列表中被移除后，`ng-leave` 类将应用于该元素。

## “ngView”动画

现在我们需要为 `ngView` 中的路由切换添加动画。与之前的示例一样，我们需要向 HTML 添加一个新的 CSS 类。不过这次不是添加到 `ngRepeat` 元素，而是添加到 `ngView`。这意味着 HTML 代码需要稍作更改。这样，视图切换时的动画将更加可控。

`index.html` 文件应如下所示：

```
<div class="view-container">
    <div ng-view class="view-frame"></div>
</div>
```

`view-container` CSS 类用于将 `ng-view` 指令嵌套在父元素内。该类将添加样式 `position: relative`，以便在动画过渡时，`ng-view` 指令的定位相对于父元素。

过渡的 CSS 应添加到 `animation.css` 文件中。如下所示：

```
.view-container {
    position: relative;
}
.view-frame.ng-enter, .view-frame.ng-leave {
    background: white;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
}
.view-frame.ng-enter {
     -webkit-animation: 0.5s fade-in;
     -moz-animation: 0.5s fade-in;
    -o-animation: 0.5s fade-in;
    animation: 0.5s fade-in;
    z-index: 100;
}
.view-frame.ng-leave {
     -webkit-animation: 0.5s fade-out;
      -moz-animation: 0.5s fade-out;
      -o-animation: 0.5s fade-out;
       animation: 0.5s fade-out;
       z-index:99;
}
@keyframes fade-in {
       from { opacity: 0; }
        to { opacity: 1; }
}
@-moz-keyframes fade-in {
        from { opacity: 0; }
        to { opacity: 1; }
}
@-webkit-keyframes fade-in {
     from { opacity: 0; }
      to { opacity: 1; }
}
@keyframes fade-out {
      from { opacity: 1; }
      to { opacity: 0; }
}
@-moz-keyframes fade-out {
       from { opacity: 1; }
       to { opacity: 0; }
}
@-webkit-keyframes fade-out {
       from { opacity: 1; }
       to { opacity: 0; }
}
/* 不要忘记供应商前缀 */
```

## 使用 JavaScript 实现“ngClass”动画

我们需要为应用程序添加另一个动画。在 `device-list.html` 页面中会看到一个漂亮的缩略图。点击缩略图后，图像会发生变化。需要更改 CSS 类，以确保图像的显示准确无误。如下所示：

```
.phone-images {
    background-color: white;
    width: 450px;
    height: 450px;
    overflow: hidden;
    position: relative;
    float: left;
}
...
img.device {
     float: left;
     margin-right: 3em;
     margin-bottom: 2em;
     background-color: white;
     padding: 2em;
     height: 400px;
     width: 400px;
    display: none;
}
img.device:first-child {
     display: block;
}
```

您可能认为我们将创建一个基于 CSS 的动画。然而，我们可以通过使用 JavaScript 的 `animation()` 模块来实现这一点。如下例所示：





```javascript
var myAnimations = angular.module('myAnimations', ['ngAnimate']);

    myAnimations.animation('.device', function() {

    var animUp = function(element, cName, done) {

if(cName != 'active') {

   return;

}

element.css({

     position: 'absolute',

     top: 500,

     left: 0,

     display: 'block'

});

jQuery(element).animate({

     top: 0

}, done);

return function(cancel) {

if(cancel) {

     element.stop();

}

};

}

var animDown = function(element, cName, done) {

if(cName != 'active') {

      return;

}

element.css({

      position: 'absolute',

      left: 0,

     top: 0

});

jQuery(element).animate({

      top: -500

}, done);

return function(cancel) {

if(cancel) {

     element.stop();

}

};

}

return {

      addClass: animUp,

      removeClass: animDown

};

});
```

正如你所注意到的，动画是通过使用 jQuery 实现的。借助 Angular 和 JavaScript，我们并不需要 jQuery 来执行动画。用 JavaScript 编写自己的动画库将会很困难。

# 第 6 章 - $watch()、$digest() 和 $apply()

这些方法在 AngularJS 中被广泛使用。你应该学会如何在 Angular 中使用它们。

当在视图中将数据绑定到 `$scope` 对象的某个变量上时，Angular 会在内部创建一个“监视器”。这个监视器意味着它会监视 `$scope` 对象中包含的内容。这表示框架将监视该变量。要创建监视器，我们使用 `$scope.$watch()` 函数。

在大多数情况下，`$scope.$digest()` 和 `$scope.$watch()` 函数会自动为你调用，但在某些情况下，你可能需要手动调用它们。这就是为什么你应该了解并理解它们的工作原理。

`$scope.$apply` 函数用于执行特定的代码，然后在其后调用 `$scope.$digest()` 函数。这将检查所有监视器，并调用所有对应的监视监听器函数。`$apply()` 函数在将 AngularJS 代码与其他代码集成时非常有用。

## $watch()

`$scope.watch()` 函数用于创建对特定变量的监视。一旦注册了监视器，就需要向 `$watch()` 函数传递两个参数。这两个参数包括：

*   一个值函数
*   一个监听器函数

考虑下面的示例，展示如何实现：

```javascript
$scope.$watch(function() {},

      function() {}

);
```

第一个函数代表值函数，第二个函数代表监听器函数。值函数会返回正在被监视的值。AngularJS 的工作就是检查返回的值与上次监视函数返回的值是否相同。AngularJS 改变了检查值是否返回的方式。下面是一个示例：

```javascript
$scope.$watch(function(scope) { return scope.data.myVariable },

     function() {}

);
```

在上面的函数中，值函数会返回 `scope.data.myVariable` 的值。如果这个变量的值发生了变化，那么返回的值也会不同。然后 AngularJS 会调用监听器函数。

如果值发生了变化，监听器函数会尝试执行它所能做的任何操作。通过使用这个值，值函数可以访问 `$scope` 及其变量。如果需要，值函数也可以监视全局变量，但大多数情况下，监视的是 `$scope` 变量。

如果值发生了变化，监听器函数可以执行它需要做的任何操作。有些人可能需要改变变量的内容，而另一些人可能需要改变 HTML 元素的内容。考虑下面的示例：

```javascript
$scope.$watch(function(scope) { return scope.data.myVariable },

function(nValue, oValue) {

    document.getElementById("").innerHTML =

     "" + newValue + "";

}

);
```

上面的示例会将 HTML 元素的 innerHTML 设置为变量的新值，并且该值被嵌入到 `b` 元素中，以使内容变为粗体。

## $digest()

`$scope.$digest()` 函数会遍历 `$scope` 对象及其子 `$scope` 对象中的监视器。当 `$digest()` 函数遍历完监视器后，会调用每个监视器的值函数。如果发现值函数返回的值与上次调用时返回的值不同，则会调用该监视器的监听器函数。

每当 AngularJS 认为有必要时，它就会调用 `$digest()` 函数。但可能会遇到 AngularJS 不调用 `$digest()` 函数的情况。为了解决这个问题，只需手动调用 `$scope.$digest()` 函数。

## $apply()

`$scope.$apply()` 函数接受一个函数作为参数，该函数会被执行，然后内部会调用 `$scope.$digest()` 函数。这是确保所有监视器都被检查的一种方式。所有数据绑定随后都会被刷新。

考虑下面的示例：

```javascript
$scope.$apply(function() {

$scope.data.myVariable = "A new value";

});
```

一旦将一个函数作为参数传递给此函数，`$scope.data.myVar` 的值就会被改变。当函数退出后，AngularJS 会调用 `$scope.$digest()` 函数，这意味着监视器会检查被监视值的变化。

考虑下面的示例，展示如何在 AngularJS 中使用这些函数：

```html
<div ng-controller="appController">

{{data.time}}

<br/>

<button ng-click="updateTime()">update time - ng-click</button>

<button id="upTimeButton"  >change time</button>

</div>

<script>

var module       = angular.module("myapplication", []);

var appController1 = module.controller("appController", function($scope) {

$scope.data = { time : new Date() };

$scope.updateTime = function() {

$scope.data.time = new Date();

}

document.getElementById("upTimeButton")

.addEventListener('click', function() {

console.log("change time clicked");

$scope.data.time = new Date();

});

});

</script>
```

在上面的示例中，变量 `$scope.data.time` 被绑定到一个插值指令上，该指令会将变量值合并到 HTML 页面中。通过这种绑定，会在变量 `$scope.data.time` 上内部创建一个监视器。

我们为应用程序创建了两个按钮。第一个按钮附加了一个 `ng-click` 类型的监听器。点击此按钮会调用 `$scope.updateTime()` 函数，然后 AngularJS 通过调用 `$scope.$digest()` 函数来更新绑定。

第二个按钮附加了一个 JavaScript 事件监听器。当第二个按钮被点击时，该监听器会被执行。两个监听器之间的唯一区别是，对于第二个按钮的监听器，点击后数据绑定不会被更新。原因在于，第二个按钮的事件监听器执行后不会调用 `$scope.$digest()` 函数。这意味着点击第二个按钮会更新变量 `$scope.data.time` 中的时间，但这个新时间不会显示出来。

为了解决这个问题，可以在事件监听器的最后一行添加对 `$scope.$digest()` 的调用。如下面的示例所示：

```javascript
document.getElementById("upTimeButton")

.addEventListener('click', function() {

console.log("change time clicked");

$scope.data.time = new Date();

$scope.$digest();

});
```

上述调用被添加到了程序的最后一行。这就是应该做的。




与其像上面那样在事件监听器内部调用 `$digest()` 函数，不如使用 `apply()` 函数，如下所示：

```
document.getElementById("upTimeButton")
.addEventListener('click', function() {
$scope.$apply(function() {
console.log("change time clicked");
$scope.data.time = new Date();
});
});
```

函数 `$scope.$apply()` 已在按钮的事件监听器中被调用，并且变量 `$scope.data.time` 的更新已作为参数传递给函数 `$apply()`。一旦函数 `$apply()` 执行完毕，AngularJS 将在内部调用函数 `$digest()`，以便所有数据绑定都被更新。

# 第 7 章 - `$scope` 的层次结构

AngularJS 中供视图使用的 `$scope` 对象被组织成一个层次结构。我们从根作用域开始，它由一个或多个子作用域组成。每个可用的视图都有自己的作用域，这些作用域只是根作用域的子级。这意味着视图控制器在变量 `$scope` 上设置的任何变量对其他控制器都是不可见的。

以下面的 AngularJS 代码为例：

```
<!DOCTYPE html>
<html lang="en">
<head>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.5/angular.min.js"></script>
</head>
<body ng-app="myapplication">
<div ng-controller="appController1">
{{data.theVariable}}
</div>
<div ng-controller="appController2">
{{data.theVariable}}
</div>
<script>
var module       = angular.module("myapplication", []);
var appController1 = module.controller("appController1", function($scope) {
$scope.data = { theVariable : "first value"};
});
var appController2 = module.controller("appController2", function($scope) {
$scope.data = { theVariable : "second value"};
});
</script>
</body>
</html>
```

在上面的例子中，我们使用了两个视图，每个视图都有自己的控制器。每个控制器会将 `data.theVariable` 变量设置为不同的值。

程序执行后，你将得到以下层次结构：

根 `$scope`

*   appController1 的 `$scope`
*   appController2 的 `$scope`

如上所示，两个视图使用了不同的作用域对象。在这个例子中，两个视图中的 `{{data.theVar}}` 数据绑定也会写入两个不同的值。`$scope` 对象中的变量 `data.theVariable` 也会被设置为不同的值。

# 第 8 章 - 重构 AngularJS 应用

基于组件的指令在 AngularJS 中越来越流行。原因在于组件易于使用。然而，目前大多数正在使用的 Angular 应用并非基于组件。

对于 Angular2 用户，可以按如下方式使用组件：

```
< confirmation
    [message]="'Start firing?'"
       (ok)="startFiring()">
</ confirmation>
```

如上例所示，组件只是一个自定义 HTML 元素，它匹配一个已在其他地方定义的组件名称。每个组件都有其输入和输出，这些作为属性提供给元素。

上述组件也可以按如下方式定义：

```
@Component({
selector: 'confirmation',
properties: ['message'],
events: ['ok']
})
@View({
template: `
<div>
{{message}}
    <button (click)="ok()">OK</button>
     </div>
`})
class Confirmation {
    okEvents = new EventEmitter();
    ok() {
     this.okEvents.next();
}
}
```

接口边界定义用于指定组件可以处理的输入和输出。UI 模板用于定义用户界面。组件逻辑位于 UI 模板之后，用于定义组件的行为以及当用户与之交互时它做什么。组件作为指令的定义可以如下所示：

```
@Component({
    selector: 'confirmation',
     properties: ['message'],
    events: ['ok']
})
@View({
template: `
    <div>{{message}}
    <button (click)="ok()">OK</button>
</div>
`
})
class Confirmation {
     okEvents = new EventEmitter();
     ok() {
     this.okEvents.next();
}
}
```

上述代码与我们之前看到的完全不同。

在 AngularJS 中，重构可以轻松完成或使用。我们想给出一个如何实现的示例：

考虑下面给出的 `index.html` 文件代码：

```
<div ng-include="'bar.html'">
</div>
```

为了替换上述代码，我们需要为 `bar` 创建一个指令。该指令将使用继承的作用域和模板 `bar.htm`。

`bar_directive.js` 的代码应如下所示：

```
module.directive('bar', function() {
return {
     scope: true,
     templateUrl: 'bar.html'
};
});
```

为了使其有效工作，指令和模板必须位于同一位置，并且它们的名称也应匹配。如下所示：

```
components/foobar/
*   bar_directive.js
*   bar.html
```

然后，原始的 `ng-include` 应被新指令替换。如下所示：

```
<div ng-include="'footbar.html'">
     </div>
<footbar></footbar>
```

添加上述组件指令（即 `footbar`）后，模板本身将如下所示：

```
<div ng-controller="FoobarCtrl as c">
     <p>{{c.getText()}}</p>
</div>
```

然后，我们想要移动并重命名包含 FootCtrl 的文件，使其与我们的组件指令位于同一位置。如下所示：

```
components/foobar/
*   bar_directive.js
*   bar_controller.js
*   bar.html
```

然后，控制器应在指令中使用，并且使用与 `ng-controller` 相同的 ctrl 别名。文件 `bar_directive.js` 应如下所示：

```
module.directive('foobar', function() {
return {
    scope: true,
    controller: 'FoobarCtrl',
    controllerAs: 'ctrl',
    templateUrl: 'bar.html'
};
});
```

现在可以从模板中移除包装器 `ng-controller`。如下所示：

```
<div ng-controller="FooBarCtrl as c">
<p>{{c.getText()}}</p>
</div>
```

也可以为了样式目的保留该元素，然后移除 `ng-controller` 属性。

考虑下面的示例：

```
<div ng-controller="FoobarCtrl as c"
class=" foo-bar">
<p>{{c.getText()}}</p>
</div>
```

在上面的模板示例中，我们有一个 `ng-controller`。它用于实例化一个 `FoobarCtrl`，然后将其别名为 `c`。

我们现在需要创建一个新指令。该指令应创建一个继承的作用域，然后使用 `FoobarCtrl` 并将其别名为 `c`。如下所示：

```
module.directive('bar', function() {
return {
    scope: true,
    controller: 'FoobarCtrl',
    controllerAs: 'c'
};
});
```

我们的新指令和现有的控制器将被移动到同一位置。两者还应具有相同的前缀。如下所示：

```
components/foobar/
*   bar_directive.js
*   bar_controller.js
```

最后，在原始模板中，`ng-controller` 可以被替换为组件 `foobar` 的一个实例。如下所示：

```
<div ng-controller="FoobarCtrl as c"
class="foo-bar">
<foobar class="foo-bar">
<p>{{c.getText()}}</p>
</foobar>
</div>
```

目前我们得到的是：

```
<div ng-controller="FoobarCtrl as c"
class="foo-bar">
<foobar class="foo-bar">
<p>{{c.getText()}}</p>
</foobar>
</div>
```

然后，应为组件指令创建一个模板文件。如下所示：

```
components/foobar/
*   bar_directive.js
*   bar_controller.js
*   bar.html
```

然后，新模板应从指令中引用。可以按如下方式完成：

```
module.directive('foobar', function() {
return {
scope: true,
controller: 'FoobarCtrl',
controllerAs: 'c',
templateUrl: 'bar.html'
};
});
```

然后，我们将使用指令元素中包含的内容来填充新模板。如下所示：

```
<p>{{c.getText()}</p>
```





指令元素本身将变为空。`index.html` 文件将如下所示：

```
<foobar>

<p>{{c.getText()}}</p>

</foobar>
```

在 `ng-controller` 被指令替换后，原始模板将剩下以下内容：

```
<foobar>

<h2>{{c.getTitle()}}</h2>

<p>{{mainC.getText()}}</p>

</foobar>
```

可以使用嵌入（Transclusion）来支持这两种情况。我们将首先为组件指令创建一个模板文件。如下所示：

`components/foobar/`

*   `bar_directive.js`
*   `bar_controller.js`
*   `bar.html`

然后可以从指令中引用新模板。同时，嵌入功能也将被启用，如下所示：

```
module.directive('foobar', function() {

return {

transclude: true,

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

templateUrl: 'bar.html'

};

});
```

模板文件的内容将通过使用原始模板中需要放入组件的一部分来填充。另一部分将添加指令 `ng-transclude`。`bar.html` 文件应包含以下代码：

```
<h2>{{c.getTitle()}}</h2>

<p ng-transclude></p>
```

在我们的指令元素中，我们将保留需要被嵌入的部分。如下所示：

```
<foobar>

<h2>{{c.getTitle()}}</h2>

<p>{{mainC.getText()}}</p>

</foobar>
```

考虑下一个示例。

我们有一个用于列出某些数据的 `<ul>` 元素。如下所示：

```
<div>

<h1>Foobars</h1>

<ul>

<li ng-repeat="foo in c.bars">

<img ng-src="foo.imageUrl"/>

{{file.text}}

</li>

</ul>

</div>
```

我们需要将列表提取到它自己的组件中。应为该组件创建一个指令和一个模板文件。在指令中应如下调用：

`components/foobar_list/`

*   `foobar_list_directive.js`
*   `foobar_list.html`

该指令将创建一个继承作用域，然后引用已创建的模板。如下所示：

```
module.directive('foobarList', function() {

return {

     scope: true,

     templateUrl: 'list.html'

};

});
```

模板将通过复制从原始模板中填充的 HTML 文件来填充。如下所示：

```
<ul>

<li ng-repeat="foo in c.bars">

<img ng-src="foo.imageUrl"/>

{{file.text}}

</li>

</ul>
```

然后可以在原始模板中使用此组件的新实例。它将替换已创建的标记。如下所示：

```
<div>

<h1>Foobars</h1>

<ul>

<li ng-repeat="foo in c.bars">

<img ng-src="foo.imageUrl"/>

{{file.text}}

</li>

</ul>

<foobar-list></foobar-list>

</div>
```

还可以创建一个使用嵌入的示例。如下所示：

```
<div>

<h1>Foobars</h1>

<ul>

<li ng-repeat="foo in c.bars">

<h3>

{{mainC.itemHeader}}

</h3>

<img ng-src="foo.imageUrl"/>

{{file.text}}

</li>

</ul>

</div>
```

我们之前示例中的 `<ul>` 元素有一些来自外部的内容，嵌入可以用于这两者。在上面的示例中，我们使用了由 `mainC` 提供的项目标题。

当列表被提取到它自己的组件中时，应为该文件创建一个指令和一个模板。如下所示：

`components/foobar_list/`

*   `bar_list_directive.js`
*   `bar_list.html`

该指令将创建一个继承作用域，然后引用新创建的模板文件。嵌入功能也将被启用。

文件 `bar_list_directive.js` 的代码应如下所示：

```
module.directive('foobarList', function() {

return {

     transclude: true,

     scope: true,

     templateUrl: 'bar_list.html'

};

});
```

模板的填充将通过复制从原始模板中提取的 HTML 来完成。项目标题部分将被替换为 `ng-transclude` 元素。

`bar_list.htm` 的代码应如下所示：

```
<ul>

<li ng-repeat="foo in c.bars">

<ng-transclude></ng-transclude>

<img ng-src="foo.imageUrl"/>

{{file.text}}

</li>

</ul>
```

然后可以在新模板中使用此组件的新实例。它将替换已提取的标记，但项目标题将保留在原位，然后对每个项目进行嵌入。如下所示：

```
<div>

<h1>My Foobars</h1>

<ul>

<li ng-repeat="foo in c.bars">

<h3>

{{mainC.itemHeader}}

</h3>

<img ng-src="foo.imageUrl"/>

              {{file.text}}              

</li>

</ul>

<foobar-list>

<h3>

{{mainC.itemHeader}}

</h3>

</foobar-list>

</div>
```

现在我们有了一个组件模板。其中可以看到两个外部引用，它们引用了控制器 `mainC`。请注意，这不是组件的控制器，它只是在我们层次结构的更上层定义的另一个控制器。如下所示：

```
<div ng-show="mainC.isFooBarVisible()">

<p>

{{c.getText(mainC.getLanguage())}}

</p>

</div>
```

应逐个移除外部引用，并始终保持代码正常工作。

首先必须选择表达式 `mainC.isFooBarVisible()`。它指的是调用位于父控制器上的方法，我们使用结果来控制元素是否可见。为了替换外部引用，必须为组件指令引入一个名为 `visible` 的绑定。

文件 `bar_diretive.js` 的代码应如下所示：

```
module.directive('foobar', function() {

return {

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

bindToController: {

visible: '='

},

templateUrl: 'bar.html'

};

});
```

上述代码显示组件有一个名为 `visible` 的输入，用户应向组件提供该输入。您还应该注意到我们引入了 `bindToController`，但属性 `scope: true` 保持不变。然而，它并不是一个隔离作用域指令。我们不隔离它的原因是其中还有其他外部引用，我们不需要破坏这些引用。在 Angular 1.4 中，可以将 `scope: true` 和 `bindToController` 结合起来，以便为非隔离的作用域引入绑定。

对于新的 `visible` 绑定，我们必须在任何使用组件 `foobar` 的地方插入一个值。我们能够访问 `mainC`，并且可以使用模板中原本包含的模板。如下所示：

```
<foobar

visible="mainC.isFooBarVisible()">

</foobar>
```

现在可以在组件内部引用作用域绑定，并且将打破对外部世界的依赖。如下所示，在 `bar.html` 中：

```
<div ng-show="c.visible">

<p>

{{c.getText(mainC.getLanguage())}}

</p>

</div>
```

现在可以为指令定义引入另一个名为 `language` 的绑定。如下所示：

```
module.directive('foobar', function() {

return {

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

bindToController: {

visible: '=',

language: '='

},

templateUrl: 'bar.html'

};

});
```

然后应在使用组件的地方为其插入一个值。如下所示：

```
<foobar

visible="mainC.isFooBarVisible()"

language="mainC.getLanguage()">

</foobar>
```

绑定也应在组件模板内部完成。如下所示：

```
<div ng-show="c.visible">

<p>{{c.getText(c.language)}}</p>

</div>
```

我们的模板将不再有外部引用。所有需要的数据都将在接口边界处显式指定。

## `$watch` 表达式示例





外部引用不仅可以在组件模板中找到。在组件控制器中，也可能存在 `$watch`、`$watchCollection` 或 `$watchGroup` 表达式。如果可用，也可以使用链接函数。考虑下面给出的示例，它展示了如何用绑定输入来替代：

```
function FoobarCtrl($scope) {

var c = this;

$scope.$watch('mainC.foo', function(nFoo) {

if (nFoo.active) {

ctrl.actFoo = nFoo;

} else {

c.actFoo = null;

}

});

}
```

我们的 watch 表达式引用了 `mainC` 的 `foo` 属性。应该使用绑定输入来代替它。考虑下面给出的代码：

```
module.directive('foobar', function() {

return {

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

bindToController: {

foo: '='

},

templateUrl: 'bar.html'

};

});
```

一旦组件被使用，就应该填入实际的值。如下所示：

```
<foobar foo="mainC.foo">

</foobar>
```

在控制器的 watch 表达式内部，就可以使用绑定输入了。如下所示：

```
function FoobarCtrl($scope) {

var c = this;

$scope.$watch('c.foo', function(nFoo) {

if (nFoo.active) {

ctrl.actFoo = nFoo;

} else {

ctrl.actFoo = null;

}

});

}
```

在某些情况下，可能不允许使用外部引用。我们希望为控制器编写一段代码，该代码将引用一个仅继承自普通 JavaScript 作用域属性的代码。以下是示例代码：

```
function FoobarCtrl($scope) {

var c = this;

c.getActiveFoo = function() {

if ($scope.mainC.foo.active) {

return $scope.mainC.foo;

} else {

return null;

}

};

}
```

上面的示例与之前的类似，唯一的区别是需要一个绑定输入。如下所示：

```
module.directive('foobar', function() {

return {

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

bindToController: {

foo: '='

},

templateUrl: 'bar.html'

};

});
```

`foo` 值将在组件使用时提供。如下所示：

```
<foobar foo="mainC.foo">

</foobar>
```

然后我们的控制器代码就可以使用绑定输入了。如下所示：

```
function FoobarCtrl($scope) {

var c = this;

ctrl.getActiveFoo = function() {

if (c.foo.active) {

return c.foo;

} else {

return null;

}

};

}
```

## 事件处理器与绑定输出

组件中使用的所有外部组件并非都是逻辑输入。有些充当逻辑输出。考虑下面给出的示例：

```
<div ng-show="c.visible">

<p>{{c.getText(c.language)}}</p>

<button ng-click="mainC.deleteFoobar()">

Delete

</button>

</div>
```

在上面的示例中，在我们的组件模板内部，我们使用了 `ng-click` 指令。它被用来调用继承而来的 `mainC` 引用上的一个方法。这就是我们所做的。

为了打破依赖关系，需要在指令定义中引入一个名为 `onDelete` 的表达式绑定。如下所示：

```
module.directive('foobar', function() {

return {

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

bindToController: {

visible: '=',

language: '=',

onDelete: '&'

},

templateUrl: 'bar.html'

};

});
```

为了在 AngularJS 中区分输入和输出，使用 `[]` 语法表示输入，使用 `()` 语法表示输出。然而，在 AngularJS 的早期版本（如 1.x）中，并没有区分它们的机制。这就是为什么大多数人倾向于为输出使用 `on` 前缀。

一旦组件被使用，就会填入新绑定的表达式。组件的使用者将决定删除操作对他或她意味着什么。在我们的例子中，我们使用它来调用主控制器的 `deleteFoobar` 函数。如下所示：

```
<foobar

visible="mainC.isFooBarVisible()"

language="mainC.getLanguage()"

onDelete="mainC.deleteFoobar()">

</foobar>
```

然后，表达式绑定将从组件模板内部被调用。如下所示：

```
<div ng-show="c.visible">

<p>{{c.getText(c.language)}}</p>

<button ng-click="c.onDelete()">

Delete

</button>

</div>
```

考虑下面给出的示例代码：

```
function FoobarCtrl($scope) {

   var c = this;

c.onFooClick = function() {

   mainC.setActiveFoo(c.foo);

};

}
```

在上面的示例中，我们使用了一个控制器函数，该函数会调用父作用域中的一个函数。外部函数调用不一定非得是特定模板中的事件处理器。它可以包含在控制器中。这就是我们对输入所做的处理。

我们应该对指令定义做的是添加一个表达式绑定。如下所示：

```
module.directive('foobar', function() {

return {

scope: true,

controller: 'FoobarCtrl',

controllerAs: 'c',

bindToController: {

     onActivateFoo: '&'

},

templateUrl: 'bar.html'

};

});
```

一旦模板被使用，就会调用我们在组件控制器中设置的 `mainCtrl.setActiveFoo`。如下所示：

```
<foobar

on-activate-foo="mainC.setActiveFoo(foo)">

</foobar>
```

然后，表达式绑定应该在控制器内部被调用，而不是在外部继承的控制器中。应该向 Angular 提供一个对象参数，以便知道要在绑定表达式中使用的 `foo` 的值。如下所示：

```
function FoobarCtrl($scope) {

var c = this;

c.onFooClick = function() {

    c.onActivateFoo({foo: c.foo});

};

}
```

考虑下面给出的示例：

```
module.directive('foobar', function() {

return {

    scope: true,

    controller: 'FoobarCtrl',

    controllerAs: 'c',

bindToController: {

    visible: '=',

    language: '=',

   onDelete: '&'

},

templateUrl: 'bar.html'

};

});
```

在上面的示例中，我们定义了所有的输入和输出。

# 结论

可以得出结论，AngularJS 是一个用于开发 Web 应用程序的非常有用的框架。AngularJS 的实用性体现在它对 HTML 所做的改进上。总的来说，它被开发出来是为了扩展 HTML 所包含的内容。请注意，HTML 并非为开发 Web 应用程序而设计。

然而，AngularJS 的出现填补了这一空白。它通过扩展 HTML 所包含的词汇来获得额外且令人惊叹的功能。使用 HTML，声明和显示动态内容非常容易。但是，当涉及到处理动态内容时，HTML 就不是最佳选择了。这正是 AngularJS 发挥作用的地方，它填补了这一空白。

正如我们所说，AngularJS 用于扩展 HTML 的功能。一个很好的例子是，当我们创建一个 HTML 页面，然后通过使用 AngularJS 来修改它。这个页面随后可以通过使用 AngularJS 动态地显示内容。这就是两者协同工作的方式。应用程序总是使用数据。这对任何应用程序都非常重要。

然而，除了处理少量数据之外，你还应该学会在 AngularJS 中处理大型数据集。这在 AngularJS 中是可行的，并且你最终得到的应用程序将非常有用。AngularJS 还可以用于为你的应用程序添加动画效果。这使你的 Web 应用程序对用户非常有吸引力。AngularJS 中有一个名为 `ngAnimate` 的模块，可用于执行这些动画。这些就是本书中讨论的一些特性。

