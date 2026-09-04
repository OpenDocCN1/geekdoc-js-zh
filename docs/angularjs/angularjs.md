
# AngularJS 实战

## 关于作者

菲利普·塔拉谢维奇（philipp.tarasiewicz@angularjs.de）是一位自由技术顾问、作家、演讲者和教练。多年来，他专注于企业级 JavaScript 领域，特别是 AngularJS，为企业客户提供员工教育和培训，并协助他们启动新项目。他与萨沙·布林克和罗宾·伯姆共同运营 AngularJS.DE，一个德国的 AngularJS 门户网站。

罗宾·伯姆（robin.boehm@angularjs.de）是一位充满激情的软件开发人员、顾问和作家，专注于 Web 技术领域，尤其是企业级 JavaScript。多年来，他广泛从事客户端 Web 应用程序的创建，并帮助企业进行员工教育和培训以及项目实施。他还共同创立了 AngularJS.DE 门户网站。

## 简介

AngularJS 是一个 JavaScript 框架，可帮助你创建现代的客户端 Web 应用程序。通过其优雅的约定，AngularJS 为常见问题提供了解决方案，并为你节省了大量原本需要编写的代码。这样，你就可以专注于实际任务。

本书通过一个逐步构建的示例项目向你介绍 AngularJS。你将学习基础概念，这些概念使你能够创建结构化、模块化且易于维护的应用程序。特别是，我们解释了诸如模块、作用域、服务和指令等概念，并展示了如何有效使用它们。有一个专门的章节致力于连接基于 REST 的 Web 服务。此外，我们讨论了诸如 Bower、Grunt、Karma 和 Yo 等工具。这些工具可以通过使某些任务变得不必要来为你节省时间。我们借助 Yeoman 概述了一个工作流，该工作流定义了如何利用这些工具为开发者创造一个高效的开发环境。

在本书的准备过程中，我们实施了大量使用 AngularJS 的项目。许多来自这些实践经验的见解都包含在本书中。

阅读本书后，你应能够：

- 理解如何使用 AngularJS 中的每个模块以及它们如何交互；
- 开发模块化、结构化且易于维护的客户端 Web 应用程序；
- 通过使用测试驱动开发方法创建高质量的 AngularJS 应用程序。

## 本书读者对象

本书主要面向具有 JavaScript 经验的 Web 开发者，他们已经掌握了该语言的基础知识，并希望通过使用测试驱动开发方法以及 JavaScript 代码结构化和模块化技术，将他们的知识提升到下一个水平。此外，如果你有过 jQuery 的使用经验，也会有所帮助。虽然这类技能不是必需的，但它们会帮助你更好地理解像 AngularJS 这样的框架在 JavaScript 应用开发中的作用。

## 前置知识

你不需要任何关于 AngularJS 的先验知识就能理解本书的内容。然而，你需要对 JavaScript 有基本的了解。此外，你还应该了解 HTML 和 CSS 的基础知识。如果你已经学习了测试驱动开发的基本概念，那将更有优势。

## 本书不适合谁

由于需要 Web 环境和 JavaScript 的经验，任何没有该领域经验的开发者建议先掌握所需的基础知识再阅读本书。此外，你不应该把它当作一本能解答所有 AngularJS 框架问题的参考书。本书并未讨论 AngularJS 的所有特性和指令。相反，它通过小型实用示例解释并演示了框架的主要特性和概念。

## 关于本书

本书从第一章“AngularJS 快速入门”开始，通过简短示例介绍 AngularJS 的一些核心概念来解释框架。本章展示了 AngularJS 的潜力和附加价值。你应该能够感受到为什么值得使用 AngularJS。然而，我们不会详细解释这些示例。如果你想快速产生令人印象深刻结果并稍作实验，请阅读本章。

接下来，第二章“基本原则与概念”深入探讨了框架的基本原理和概念。本章首先解释了 AngularJS 的几个关键概念，包括模型-视图-视图模型模式（MVVM）、双向数据绑定、依赖注入和可测试性。它还展示了 AngularJS 提供的各个应用模块，你可以使用它们来编写应用程序。

在讲解了基础知识后，本书继续通过第三章《BookMonkey 项目》开发一个名为 BookMonkey 的示例项目。这是本书的主要部分，它展示了如何使用 AngularJS 创建一个小型 Web 应用程序来浏览图书集合。此示例演示了 AngularJS 的基本概念和功能如何应用于现实世界的应用程序中。因此，我们在开发此应用程序时确保了遵循测试驱动开发方法。在第四章《扩展应用程序》中，我们扩展项目以包含管理部分和自定义指令，并解释如何消费 REST Web 服务。

在第五章《项目管理和自动化》和第六章《调试》中，我们讨论了与项目相关的问题，如项目管理、任务自动化、调试以及自动化测试。在第七章《常见问题解答》中，我们回答了人们在一个项目中经常向我们提出的问题。

对于 AngularJS 的完全初学者来说，建议先阅读第一章《AngularJS 快速入门》和第二章《基本原则与概念》，以学习框架的术语。在此基础上，第三章《BookMonkey 项目》和第四章《扩展项目》中的实际示例可以容易地更新。第五章、第六章和第七章可以独立于前面的章节阅读，以准备即将到来的项目或熟悉项目中使用的工具。

## 下载示例并获取更新

本书中的示例可从出版社的网站下载，网址为：

`http://books.brainysoftware.com`

这些示例是使用 AngularJS 版本 1.2.10 开发的。该版本反映了撰写本书时的最新版本。然而，如果未来版本的 AngularJS 出现不兼容情况，我们将相应地更新这些示例。

## 联系作者

自 2013 年以来，作者一直在运营 AngularJS.DE2 门户网站（`http://angularjs.de`）。该门户网站定期发布关于 AngularJS 当前议题的文章，AngularJS 开发者可以在此交流并提供服务。如果你的开发团队需要顾问或培训，你可以直接联系作者。

# 第 1 章 AngularJS 快速入门

本章通过简短示例展示了 AngularJS 的强大功能。我们还想向你展示 AngularJS 应用中典型的代码片段是什么样的。示例故意做得简单，以便在没有大量框架知识的情况下也能轻松理解和执行。我们不会解释所有细节。相反，我们会保持解释简短。在阅读完整本书后，你会详细了解这些示例。

## 双向数据绑定：样板代码已成为过去

双向数据绑定无疑是使 AngularJS 具有吸引力的最重要特性之一。双向数据绑定确保数据模型中的变化自动反映在视图中的相应元素上。当用户对相关视图进行修改时，它也会自动更新数据模型。这种双向的自动调整就是我们所说的双向数据绑定。由于这一特性，你可以节省大量原本需要编写以实现等效同步逻辑的样板代码。清单 1.1 中的示例展示了该功能的实际应用。

### 清单 1.1：带输入字段的双向数据绑定

```html
<!DOCTYPE html>
<html ng-app>
<head>
<meta charset="utf-8">
</head>
<body>
<div>
    <label>Name:</label>
    <input type="text" ng-model="yourName">
    <hr>
    <h1>Hello {{yourName}}!</h1>
</div>

<script src="lib/angular/angular.js"></script>
</body>
</html>
```

清单 1.1 中的简单 HTML 文件包含一个输入字段和一个以 `h1` 标题形式的输出。如果你在浏览器中运行此示例（见图 1.1），你会发现每次在输入字段中输入内容时，标题都会自动更新。这就是双向数据绑定。

![](img/7a003218cea01579a50512a6c0e40f28_13_0.png)

**图 1.1：清单 1.1 中代码的输出**

### 你好，AngularJS！

为了让双向数据绑定在示例中起作用，你需要在输入字段中使用 `ng-model` 属性。在 AngularJS 世界中，这个未知的 HTML 属性被称为指令。`ng-model` 指令在输入字段和变量 `yourName` 之间建立了双向数据绑定。由于有了这个指令，当输入字段的值发生变化时，变量的值也会自动变化。变量在哪里定义并不重要。

`h1` 标签内花括号中的表达式是 AngularJS 的输出机制。更准确地说，你使用表达式来输出变量值。表达式也受双向数据绑定约束。如果变量 `yourName` 的值发生变化，表达式会被重新计算，最终导致视图自动更新。通过这种方式，AngularJS 框架自动将输入字段的内容转移到 `h1` 标签中。

我们应该在此提到 `ng-app` 指令，它在示例中标注了 `html` 标签。你使用这个指令告诉 AngularJS DOM（文档对象模型）的哪一部分应被视为 AngularJS 应用。当你在 `html` 标签中添加此指令时，你告诉 AngularJS 整个 DOM 都要操作，因为 `html` 标签是根节点。或者，你也可以将 `ng-app` 添加到 `html` 标签内的 DOM 节点中，使 DOM 子树成为 AngularJS 应用。在后一种情况下，所有子树外的表达式将被保留原样并被忽略。

你也可以用 `ng-app` 标注 DOM 中的多个兄弟节点，以便在一个 HTML 文档中定义多个独立的 AngularJS 应用。对于大多数应用程序来说，这没什么意义，因为各个应用之间没有交互方式。尽管如此，我们还是要提到这一点，因为官方的 AngularJS 网站（`http://angularjs.org`）利用这一特性呈现了无数自包含的示例。

### 第二个示例

即使只有双向数据绑定，许多应用程序也可以在不写一行 JavaScript 代码的情况下优雅地实现。我们将通过提供一个更复杂的示例——颜色选择器——来证明这一点。颜色选择器是一个用户界面（UI）组件，它让用户通过提供反映颜色当前 RGBA 值的即时视觉反馈来轻松选择颜色。

### 清单 1.2：带 HTML5 滑块的双向数据绑定

```html
<!DOCTYPE html>
<html ng-app>
<head>
    <meta charset="utf-8">
</head>
<body ng-init="r=255; g=0; b=123; a=0.7">

R:<input type="range" name="color_r"
        min="0" max="255" step="1" ng-model="r"><br>
G:<input type="range" name="color_g"
        min="0" max="255" step="1" ng-model="g"><br>
B: <input type="range" name="color_b"
        min="0" max="255" step="1" ng-model="b"><br>
A: <input type="range" name="color_a"
        min="0" max="1" step="0.01" ng-model="a">

<div style="width: 300px; height: 100px;
      background-color:
      rgba({{ r }}, {{ g }}, {{ b }}, {{ a }});">
</div>

<script src="lib/angular/angular.js"></script>
</body>
</html>
```

清单 1.2 展示了一个简单的颜色选择器。在其基本设计中，这个示例与前面的示例类似。我们通过为四个 `input` 标签的 `type` 属性赋值 `"range"`，定义了四个 HTML5 滑块。我们还使用 `min` 和 `max` 属性为每个输入标签提供了取值范围。我们需要三个滑块来控制颜色选择器的红、绿、蓝值，第四个用于控制 alpha 通道（透明度）。`step` 属性指定了增量。

同样在这个示例中，我们使用 `ng-model` 指令来绑定滑块和相应的作用域变量 `r`、`g`、`b` 和 `a`。这同样是双向数据绑定。表达式也可以使用，而这一次我们使用表达式不是直接生成输出，而是设置 `div` 元素的 CSS `background-color` 属性的各个分量，`div` 元素中将渲染颜色预览。

结果 quite impressive。基本上，我们使用四个滑块来控制 RGBA 属性的四个独立分量，这些分量基于作用域变量 `r`、`g`、`b` 和 `a`，并创建双向数据绑定。如图 1.2 所示，我们几乎毫不费力地创建了一个带有实时颜色预览的简单颜色选择器。每当我们移动四个滑块中的任意一个时，`div` 元素的颜色就会改变。

注意，当前示例与前面的示例之间有一个细微差别。在当前示例中，我们在 `body` 标签中使用 `ng-init` 指令为变量 `r`、`g`、`b` 和 `a` 指派初始值。

![图 1.2：清单 1.2 中的颜色选择器示例](img/7a003218cea01579a50512a6c0e40f28_13_0.png)

#### `ng-init`

在较大的项目中应避免在模板中写入初始值，因为这意味着将部分逻辑转移到模板中。我们在示例中仅使用它是为了避免不得不使用 JavaScript 代码来初始化值。

## 指令：HTML 元素和属性

指令是另一个强大的功能，也是 AngularJS 的独特功能之一。正如你在前面两个示例中所见，指令在 AngularJS 中无处不在。该框架本身非常重度地基于这一概念。

通过指令，你可以扩展自己的 HTML 元素和属性。你可以将这种技术用于许多有趣的事情。例如，你可以定义自己的标签集合，并使用这些标签以声明式方式描述应用程序的许多部分。或者，你可以编写一个可复用的库，将 HTML 扩展为对你的应用程序至关重要的各种专用 UI 组件。想象一下像 `<chart>`、`<spreadsheet>` 或 `<input auto-complete="data">` 这样的标签。然后你可以在指令中封装所需的逻辑。

### 一个示例

在以下示例中，我们创建一个 `<color-picker>` 标签，它封装了颜色选择器示例中的逻辑，从而使其可复用。我们已确定我们的指令必须满足两个要求。首先，必须有一种方法来配置颜色选择器的初始颜色。其次，我们希望在颜色变化时得到通知，以便我们能够以某种形式做出响应。清单 1.3 中的模板展示了我们如何创建满足这些要求的 `<color-picker>` 指令。

#### 清单 1.3：使用颜色选择器指令

```html
<!DOCTYPE html>
<html ng-app="colorPickerApp">
<head>
    <meta charset="utf-8">
</head>
<body ng-controller="MainCtrl">

<h1>AngularJS 快速入门颜色选择器</h1>

<color-picker init-r="255"
              init-g="0"
              init-b="0"
              init-a="1.0"
              on-change="onColorChange(r,g,b,a)">
</color-picker>

<script src="lib/angular/angular.js"></script>
<script src="scripts/colorPickerApp.js"></script>

</body>
</html>
```

我们的 `color-picker` 指令看起来完全像标准的 HTML 标签，采用通常的标签语法并设置一些用户自定义属性。具体来说，这些属性是 `init-r`、`init-g`、`init-b`、`init-a` 和 `on-change`。根据其中一个要求，我们使用 `init` 属性来初始化颜色选择器的 RGB 和 alpha 值。

我们使用 `on-change` 属性来指定颜色变化时将调用的回调函数。该回调函数允许我们从标签外部响应颜色变化。在清单 1.3 中，我们告诉指令 `onColorChange()` 是要调用的回调函数。`onColorChange` 函数在 `MainCtrl` 控制器中定义，AngularJS 知道这一点，因为我们已经用 `ng-controller` 指令标注了 `body` 标签。我们稍后才会解释 `ng-controller`，目前你不必担心它。

> **注意**
>
> 回调函数是一个组件传递给另一个组件的函数，以便前者在后者中发生感兴趣的事件时得到通知，从而让第一个组件有机会对该事件做出响应。

在清单 1.3 的模板中，我们还用 `ng-app` 指令标注了 `html` 标签。`ng-app` 指令指定要加载的模块。如果像前面的示例一样没有指定模块，AngularJS 将使用默认模块。对于小型示例来说，这完全可以接受。然而，在具有多个模块的大型应用程序中，不指定模块是行不通的，因为在浏览器完成加载 DOM 后，框架将不知道要加载哪个模块。我们希望遵循最佳实践，因此在清单 1.3 的代码中，我们告诉 AngularJS 在浏览器完成加载 DOM 后，框架应该加载 `colorPickerApp` 模块。因此，我们需要在 JavaScript 代码中定义这个模块以及前述的 `MainCtrl` 控制器。看看清单 1.4 中的代码。

#### 清单 1.4：`colorPickerApp` 模块的定义，包括 `MainCtrl` 控制器

```javascript
var colorPickerApp = angular.module('colorPickerApp', []);

colorPickerApp.controller('MainCtrl', function ($scope) {
    $scope.onColorChange = function (r, g, b, a) {
        console.log('onColorChange', r, g, b, a);
    };
});
```



清单 1.4 中的定义有趣之处在于，AngularJS 的 `MainCtrl` 控制器具有作用域。作用域的概念已经在第一个示例中介绍过。作用域定义了在特定上下文中必须有效的所有变量和函数。它负责确保双向数据绑定可以在该上下文中使用。

## 12 AngularJS

在框架中，某些组件在调用时会创建新的作用域。控制器就是这些组件之一。在清单 1.4 的代码中，AngularJS 将作用域传递给控制器。在这个作用域中，你可以通过给定的 `$scope` 参数访问控制器的内部。在代码中，我们还在 `MainCtrl` 控制器的作用域内定义了回调函数 `onColorChange()`。该函数接受四个参数（`r`、`g`、`b` 和 `a`），并在每次颜色变化时由我们的 `color-picker` 指令调用。`onColorChange` 函数做的事情不多；它只是向浏览器控制台写入一些内容。

现在我们来定义实际的 `color-picker` 指令。我们从清单 1.5 中 `<color-picker>` 标签背后的模板开始。

### 清单 1.5：定义 color-picker 指令的模板

```html
R:<input type="range"
    min="0" max="255" step="1"
    ng-model="r"><br>

G:<input type="range"
    min="0" max="255" step="1"
    ng-model="g"><br>

B:<input type="range"
    min="0" max="255" step="1"
    ng-model="b"><br>

A:<input type="range"
    min="0" max="1" step="0.01"
    ng-model="a">

<div style="width: 300px; height: 100px;
    background-color:
    rgba({{ r }}, {{ g }}, {{ b }}, {{ a }});">
</div>
```

如你在清单 1.5 中所见，该模板与清单 1.2 中颜色选择器示例的模板相同。

### 指令定义

现在我们来看看示例中最有趣的部分，即指令的实际定义，如清单 1.6 所示。

### 清单 1.6：颜色选择器指令的定义

```javascript
colorPickerApp.directive('colorPicker', function () {
    return {
        scope: {
            r: '@initR',
            g: '@initG',
            b: '@initB',
            a: '@initA',
            onChange: '&'
        },

        restrict: 'E',
        templateUrl: 'colorPickerTemplate.html',
        link: function(scope) {
            var COLORS = ['r', 'g', 'b', 'a'];

            COLORS.forEach(function(value) {
                scope.$watch(value, function(newValue, oldValue) {
                    if (newValue !== oldValue) {
                        if (angular.isFunction(scope.onChange)) {
                            scope.onChange(generateColorChangeObject());
                        }
                    }
                });
            });

            var generateColorChangeObject = function() {
                var obj = {};

                COLORS.forEach(function(value) {
                    obj[value] = scope[value];
                });

                return obj;
            };
        }
    };
});
```

目前我们不会详细讨论清单 1.6 中的代码，而只会涉及一些关键点，以突出该指令是如何实现的。

看看清单 1.6 第一行中 `directive()` 函数的调用。我们使用 `directive()` 来注册一个新指令。`directive()` 的第一个参数是你想要注册的指令名称。这个名称直接决定了相应 HTML 标签或属性的调用方式，并在我们的模板中代表该指令。在这里，我们可以看出本例的一个特殊之处。我们的颜色选择器的 HTML 标签是 `color-picker`，而指令名称是 `colorPicker`。

指令名称到 HTML 元素或属性的映射遵循 AngularJS 的一条内部规则，如下所述。

作为第二个参数，`directive()` 函数期望接收一个函数，该函数返回一个函数或所谓的指令定义对象（DDO）的实例，其中包含某些属性。在此阶段，这两种返回类型之间的区别并不重要。在大多数情况下，你以返回一个 DDO 的方式定义指令，该 DDO 基于某些对象属性来描述指令的行为。在本例中，我们使用这样一个对象来定义我们的颜色选择器指令。你可以在配置对象中设置许多属性以实现特定的行为，包括 `scope`、`restrict`、`templateUrl` 和 `link`。

#### 指令名称和标签/属性映射的规则

如果指令名称由两个或更多单词组成，请使用驼峰表示法，例如 `ColorPicker`。对于相应的 HTML 标签或 HTML 属性，使用蛇形表示法，冒号（`:`）、连字符（`-`）或下划线（`_`）均可用作分隔符。也就是说，`color:picker`、`color_picker` 或 `color-picker` 都可以用来指代 `colorPicker` 指令。然而，你通常会使用连字符作为分隔符。

此外，AngularJS 还有两种其他调用指令的方式，即使用前缀 `data-` 或 `x-`。原因是为了让旧浏览器仅允许这些自定义标签或属性具有这些前缀。因此，我们可以使用 `<data-color-picker>` 或 `x-color-picker` 来引用我们的颜色选择器。了解这种命名约定对于创建指令以避免意外的惊喜非常重要。

#### templateUrl 属性

`templateUrl` 属性指定了指令模板的 URL。在清单 1.6 中，我们引用了之前定义的模板文件 `colorPickerTemplate.html`。

#### restrict 属性

`restrict` 属性指示哪些 HTML 元素将受到该指令的影响。`restrict` 的有效值是一个包含字母 E、A、C 或 M 的字符串。这些字母的含义是：

- E – HTML 元素或标签
- A – HTML 属性
- C – CSS 类
- M – HTML 注释

这四个字符的组合也是允许的。例如，字符串 `"EA"` 会导致该指令影响 HTML 标签和 HTML 属性，而忽略 CSS 类和 HTML 注释。

#### scope 属性

你使用 `scope` 属性来指定指令的实例是否拥有自己的作用域。在指令的上下文中，还有一种特殊形式的作用域：隔离作用域。隔离作用域将指令内部的作用域与外部的作用域分离，然后将外部作用域映射到指令的内部作用域。我们这里不深入探讨，仅解释示例中相关的一些方面。

#### link 属性

你通过 `link` 属性定义指令的核心功能。这就是所谓的链接函数。简单来说，AngularJS 恰好执行每个指令实例的链接函数一次，从而允许你为每个实例定义初始化代码。通常，你会在链接函数中注册事件处理程序，或者在必要时执行 DOM 操作。因此，在链接函数中，我们可以实现当颜色选择器中的滑块值发生变化并产生新颜色时，在每个函数回调中调用的逻辑。事实上，我们并没有监听控制器中的变化，而是使用所谓的观察者（watchers）监听相应的作用域变量 `r`、`g`、`b` 的变化。

总之，我们现在创建了一个新的 HTML 标签 `<color-picker>`，我们可以在我们的 AngularJS 应用中重用它。

### 过滤器（Filters）

虽然在 AngularJS 中模板起着重要作用，但该框架并没有模板引擎。原因是普通 HTML 结合表达式和指令已经足够强大，能够完成典型模板引擎的任务。

此外，该框架提供了格式化和集合过滤器。我们将通过讨论日期过滤器（一种格式化过滤器）来解释这些过滤器。使用此过滤器，你可以格式化一个日期。

#### 清单 1.7：使用日期过滤器

```html
<!DOCTYPE html>
<html ng-app="dateApp">
<head>
    <meta charset="utf-8">
</head>

<body ng-controller="DateCtrl">
Today's date:
{{ now | date:'dd. MMMM yyyy' }}<br> And the time is:
{{ now | date:'HH:mm:ss' }}

<script src="lib/angular/angular.js"></script>
<script src="scripts/dateApp.js"></script>

</body>
</html>
```

清单 1.7 显示了日期过滤器的一个示例。你可以看到，所有日期过滤器的实例——像其他所有格式化过滤器一样——都嵌入在表达式中。其语法类似于各种 Unix Shell 中的管道语法。你基本上使用管道字符（`|`）告诉 AngularJS，在求值并显示结果之前，表达式需要经过过滤器的处理。过滤器紧跟在管道之后。就像在所有常见的 Unix Shell 中一样，多个过滤器可以串联使用，处理从左到右进行。

此时日期过滤器所做的功能显而易见。在返回作用域变量 `now` 的值之前，日期过滤器会尝试根据给定的格式字符串对其进行格式化。该字符串可以包含要使用的日期或时间组件。为了让过滤器正常工作，作用域变量 `now` 必须满足一个要求。你必须为其赋值如下之一：

- 一个 `Date` 对象
- 一个字符串或数字对象，指定自 1970 年 1 月 1 日以来经过的毫秒数。
- 一个包含 ISO 8601 格式有效日期的字符串，例如遵循以下模式的日期：`yyyy-MM-DDTHH:mm:ss.SSSZ`

现在为了完成源代码，下面在清单 1.8 中展示了 `dateApp` 模块和 `DateCtrl` 控制器。

#### 清单 1.8：DateApp 模块和 DateCtrl 控制器的定义

```javascript
var DateApp = angular.module("DateApp", []);
dateApp.controller("DateCtrl", function ($scope, $timeout) {
  $scope.now = 'Loading...';

  var updateTime = function() {
    $timeout(function() {
      $scope.now = new Date();
      updateTime();
    }, 1000);
  };

  updateTime();
});
```

#### 清单 1.9：truncate 过滤器的定义

```javascript
dateApp.filter('truncate', function () {
    return function (input, charCount) {
        var output = input;
        if (output.length > charCount) {
            output = output.substr(0, charCount) + '...';
        }

        return output;
    };
});
```

清单 1.9 展示了我们的 `truncate` 过滤器的定义。在 AngularJS 中，你通过调用 `filter()` 函数来定义一个过滤器。该函数接受两个参数。第一个参数是一个包含过滤器名称的字符串。作为第二个参数，该函数期望一个返回函数的函数。整个东西在这个时候可能听起来有点复杂，但正如你在前面的示例中已经看到的，使用匿名函数和高阶函数来定义应用组件是 AngularJS 中的一个常见模式。

过滤器定义的关键是所谓的过滤器函数。在清单 1.9 中，这是位于过滤器逻辑中的函数，我们最终返回它。框架每次重新评估使用该过滤器的表达式时都会调用此函数。我们将表达式先前计算的值作为第一个参数获得。使用第二个参数，我们可以选择性地访问过滤器的参数。正如我们在 `date` 过滤器中已经看到的，许多过滤器接受一个或两个参数。例如，`date` 过滤器接受一个包含日期格式的字符串。

我们的 `truncate` 过滤器也接受一个参数。该参数应指定我们的过滤器将开始截断的最大字符数。过滤器本身的实现相当简单。我们检查字符串是否超过指定的最大字符数，如果是，则截断字符串并添加三个句点。

最后，清单 1.10 中的代码展示了如何使用我们刚刚定义的 `truncate` 过滤器。

#### 清单 1.10：使用我们的 truncate 过滤器

```html
<!DOCTYPE html>
<html ng-app="dateApp">
<head>
    <meta charset="utf-8">
</head>

<body ng-controller="DateCtrl">
Today's date:
{{ now | date:'dd. MMMM yyyy' }}<br>

And the time is:
{{ now | date:'HH:mm:ss' }}<br>
{{ 'This is an example for a long text' | truncate:18 }}

<script src="lib/angular/angular.js"></script>
<script src="scripts/dateApp.js"></script>

</body>
</html>
```

如清单 1.10 所示，我们使用 `truncate` 过滤器的方式与使用 `date` 过滤器相同。然而，在这种情况下，我们没有使用作用域变量。

相反，我们直接在表达式中定义一个输入字符串。这足以满足我们的目的。

结果是字符串被截断为 18 个字符，并附加了三个句点。

#### 总结

- 双向数据绑定是 AngularJS 中的一种机制，当绑定到视图的值发生变化时，可以自动更新视图。
- 整个事情也以相反的方式工作。如果用户交互导致视图本身发生变化，框架会确保更改在作用域中传播。
- 我们可以使用指令来创建新的 HTML 元素和属性。例如，我们可以创建可重用的组件，这些组件可以在应用程序中使用。
- 在 AngularJS 中存在两种类型的过滤器：格式化过滤器和集合过滤器。
- AngularJS 自带默认的格式化过滤器，例如 `date`、`uppercase` 和 `lowercase`。
- 集合过滤器与 `ngRepeat` 指令结合使用，将在后续章节中更详细地解释。
- 现在你已经初步体验了 AngularJS，你应该清楚 AngularJS 如何帮助你创建现代 Web 应用程序了。

# 第 2 章

## 基本原则和概念

在我们详细介绍 AngularJS 之前，我们将首先概述 AngularJS 框架的基本概念。这尤其重要，因为希望了解 AngularJS 工作原理的人需要首先了解一些基本原则。完成本章后，你将能够理解 AngularJS 世界中的最重要术语，并了解该框架如何利用某些经过验证的模式和最佳实践来促进客户端 Web 应用程序的开发。

### 关键概念

AngularJS 框架基于一些经过验证的设计模式。在本节中，我们介绍这些模式并解释它们在 AngularJS 上下文中的用途。

## 模型-视图-控制器还是模型-视图-视图模型？

### 模型-视图-控制器模式

软件工程中最基本的架构模式之一无疑是模型-视图-控制器（MVC）模式。任何编写过包含图形用户界面的应用程序的开发者肯定使用过或至少听说过这种模式，它最早在 Smalltalk 中使用。1979 年，挪威计算机科学家 Trygve Reenskaug 在认识到将数据存储、业务逻辑和表示方面的责任分离并外包到单独的层中对 GUI 应用程序很有用后，制定了这种模式。

自从第一个为每个 HTTP 请求动态组装响应的动态网站出现以来，MVC 模式经历了重大繁荣。人们很快认识到，将 MVC 的职责划分应用于服务器端 Web 应用程序领域是很有用的。无论是 Ruby on Rails、Zend Framework 还是 Spring MVC，每个相关的 Web 框架都需要 MVC 作为基本架构模式。在这种情况下，该模式的基本理念相当简单。

如前所述，数据管理（模型）、表示（视图）和业务逻辑（控制器）之间存在严格的划分。最初的想法是用户与视图组件（例如 GUI）交互，用户输入由控制器组件处理。该控制器组件负责在处理输入的数据之前检查它，以确保数据符合某些业务规则，并确保模型组件相应地操作底层数据模型。此外，模型组件和视图组件之间存在通信机制，允许视图组件在模型发生任何更改时得到通知。因此，视图组件最终负责确保用户看到数据的当前状态。



在基于经典往返（round-trip）的 Web 应用程序上下文中，MVC 模式的实际实现通常意味着应用程序包含一组控制器，每个控制器处理特定 URL 上的请求。一旦客户端（通常是浏览器）向服务器发送 HTTP 请求，该请求由负责处理被调用 URL 的控制器处理。现在该控制器具有上述责任：数据验证、根据某些业务逻辑处理数据以及向模型层报告可能的操纵，模型层通常以数据库和相应访问对象的形式体现。此外，控制器的任务是将数据和 HTML 模板合并，该模板使用用于组装 HTTP 响应的框架。这种以动态生成的 HTML 形式提供的 HTTP 响应然后被发送到客户端。

浏览器最终接收并显示的生成 HTML 代码，原则上是视图组件的一部分。Web 在其原始形式上基于往返原则，因此任何形式的 HTTP 通信要求客户端发送请求，服务器进行响应，这意味着在数据存储层和浏览器中显示的 HTML 代码（视图组件）之间无法建立顺畅的通信通道。因此，经典 Web 应用程序的视图组件仅仅是在更新 HTTP 响应的上下文中，而这种更新必须以 HTTP 请求为前提。这样一来，交互性就受到了影响。

总之，可以明确地说，在经典的基于往返处理的 Web 应用程序中，模型、控制器以及大部分视图逻辑都位于服务器端。这种类型的软件被称为**瘦客户端**。

虽然基于往返处理的机制在交互性较低的经典 Web 应用程序中表现良好，但要创建现代应用程序，你需要将大部分逻辑放在浏览器端。在这种架构中，服务器仅作为数据源和存储使用，通过基于 REST 的接口向运行在浏览器中的应用程序提供应用数据。因此，显而易见，即使在所谓的**胖客户端**中，也需要考虑如何应用 MVC 模式。

### Model-View-ViewModel 模式

事实上，MVC 模式在浏览器中扮演着主导角色。所有流行的 JavaScript 框架，包括 AngularJS，都将此模式作为构建应用程序的基本方法。然而，在客户端 Web 应用领域，更常使用的是一个扩展版的 MVC 模式：Model-View-ViewModel 模式，简称 MVVM。

MVVM 模式最初来自 Adobe Flex 和 Microsoft Silverlight 环境。它现已在 JavaScript 世界中确立了自己的地位。由于模型层（即应用数据）首先位于服务器端，并通过 REST API 对外提供服务，因此在客户端引入一个代理层是合理的，该代理层仅返回当前实际使用的数据。这个代理层被称为`ViewModel`。

数据通常需要以某种方式进行转换，然后才能用于显示。这种数据转换也是`ViewModel`的职责。此外，它还定义了我们在显示中所需的功能。例如，你可以在`ViewModel`中定义一个包含按钮点击处理逻辑的函数。图 2.1 说明了这种关系。

![img/7a003218cea01579a50512a6c0e40f28_31_0.png](img/7a003218cea01579a50512a6c0e40f28_31_0.png)

Figure 2.1: Model-View-ViewModel (completed)

在与 MVVM 相关的语境中，双向数据绑定的概念也频繁使用。你可以在下一节中详细了解这一点。总之，ViewModel 层有两个主要任务：

1. 提供并转换位于服务器上的应用数据的一部分。
2. 在显示的上下文中提供所需的功能。

ViewModel 概念的实际实现是通过 AngularJS 中的`scopes`（作用域）来完成的。`Scopes`将​​在下一节中介绍。

> **没有后端的应用程序中的 MVVM**
>
> 即使你正在处理的应用程序不需要与后端通信，使用 ViewModel 概念也是有意义的。一方面，双向数据绑定的概念是建立在 ViewModel 层之上的。另一方面，在大多数情况下，你的应用程序仍然会有一个数据源，其数据在显示之前需要以某种方式进行转换。

### 双向数据_ix 数据绑定和 Scopes

双向数据绑定是一种机制，用于在用户更改 GUI 中的内容时自动更新数据模型。反向过程——即响应底层数据模型的变化而自动更新视图——也被这一概念所涵盖。这个概念的名称含义就是双向的数据绑定。

由于这个概念是 AngularJS 的组成部分，我们可以节省大量代码，否则我们就需要自己实现相应的更新逻辑。如果你将 AngularJS 与 jQuery 进行比较，你会发现使用 jQuery 时，你需要在 DOM 元素上注册事件监听器，当事件触发时会调用回调函数。jQuery 的回调函数随后会修改数据模型的相应变量。此外，使用 jQuery 时，反方向的绑定也必须手动处理。换句话说，当你的变量发生变化时，你需要实现一些逻辑来更新相应 DOM 元素的值。这会涉及大量所谓的“样板代码”，即繁琐的应用程序逻辑，而在 AngularJS 中，得益于双向数据绑定，你可以省去这些麻烦。

在 AngularJS 中，双向数据绑定的实现本质上基于`scopes`。一个`scope`包含在特定上下文中定义的所有变量和函数。这个上下文是 DOM（文档对象模型）的特定部分。重要的是要理解，AngularJS 只能对`scope`中定义的变量或函数建立双向数据绑定。同样重要的是要认识到，框架会为应用程序创建一个根`scope`。

`Scopes`的另一个特性是它们可以通过原型相互继承，从而形成一个层次结构。从语义上讲，这对应于 JavaScript 中的原型继承，这是一种将通用数据和逻辑卸载到更高层级构造中的常见方式，以避免冗余。

如果 Scope B 继承自 Scope A，通俗地说，这意味着在 Scope B 的上下文中，你不仅可以访问 B 中定义的变量和函数，还可以访问 A 中定义的变量和函数。然而，请注意，同名变量或函数可能会被覆盖。因此，如果 A 和 B 中存在相同的变量或函数，那么 Scope B 中的变量或函数会隐藏 Scope A 中同名的变量或函数。在 Scope B 的上下文中，那么你只能通过迂回的方式保证访问 A 中同名的变量或函数。

#### 隔离 Scopes

在 AngularJS 中，你可以定义隔离的`scopes`。隔离`scopes`允许你精确控制如何授予对父`scope`中变量或函数的访问权限。这种特殊形式的`scope`主要用于指令（directives）中。通过隔离`scopes`，你可以确保自包含的可复用组件在访问共享变量时不会意外冲突。由此产生的错误通常很难识别，因此在这种情况下，你应该始终致力于实现这种隔离。指令的概念将在本章后面介绍。

除了双向数据绑定中的`scopes`之外，你还需要一种机制来决定何时同步用户界面和数据模型。你通常可以在脏检查（dirty checking）和基于观察者的解决方案之间进行选择。AngularJS 使用的是脏检查。

顾名思义，脏检查本质上是一个算法，它检查当前视图的所有相关`scope`以找到“脏”变量，并在发现视图和 ViewModel 之间存在差异时执行一些同步逻辑。请注意，该算法运行频繁，因此必须针对执行时间进行高度优化，以免对应用程序的响应性产生负面影响。幸运的是，你不必担心该算法何时执行，因为框架会处理这一点。尽管如此，你应该记住这个机制的工作原理，以免在应用程序中遇到性能问题。你应该注意的最重要规则是：只在`scope`中定义视图中实际需要的数据和函数。视图中所有不必要但仍定义在`scope`中的数据和函数都会增加执行脏检查的时间，而不会带来任何价值。

#### 控制反转和依赖注入

AngularJS 还利用控制反转（IoC）和自动依赖注入（DI）。Java 和 .NET 等各种平台多年来一直提供了广泛的可能性，以便在应用程序中无缝使用这些模式。多亏了 AngularJS，这些概念现在首次出现在客户端 Web 应用程序中。

这些概念解决了软件开发中的一个根本问题：如何管理应用程序组件，使其与现有依赖解耦，并实现高度的灵活性和可互换性？这最终是高质量软件的两个重要特征，因为它们负责确保应用程序是可测试的且易于适应。可测试是指你可以轻松地为组件编写单元测试。

没有使用过 IoC 和 DI 的 JavaScript 开发人员可能会问这些问题：到底什么被反转了？这里有什么优势？IoC 和 DI 有什么区别？为什么这些模式对于生成高质量软件如此重要？为了回答这些问题，我们将简要谈谈 IoC 和 DI。

要解决应用程序组件的依赖关系，在 JavaScript 中你有四种选择：

- 使用`new`运算符手动实例化。
- 通过全局变量集成。
- 灵活性和可互换性。
- 可测试性。

如果你仔细想想，在处理依赖关系时，前三个选项与其说是帮助，不如说是损害。第一个选项意味着这意味着在设计时，你必须编写代码来实例化一个固定组件，而这在运行时是难以（甚至根本无法）改变的。通过全局变量进行的集成存在类似的缺点，并且会使应用程序的全局命名空间变得混乱。第三种解决方案——通过服务定位器——虽然优于前两种，但并非最优，因为你无论如何都必须访问服务定位器并请求实际依赖项的实例。通过利用服务定位器提供的间接性，组件与依赖项被解耦。然而，你现在必须获取服务定位器的实例，这基本上意味着你只是将原始问题转移了。因此，最优的解决方案是将对象创建的责任交还给环境。这为一种约定奠定了基础，该约定可以自动确定应用程序组件所需的依赖项，并在运行时将其交给组件。这样，当需要不同的依赖项时，你无需重新配置应用程序组件。你只需将此任务交给环境即可。

你的组件不再负责生成其依赖项，这一责任已转移到了环境。因此，我们称之为控制流反转（IoC）。事实上，正是这一属性使得 IoC 原则在软件工程中如此重要，并且影响深远。

为了在应用程序组件依赖项解析的上下文中，为 IoC 模式找到一个独立且明确易懂的名称，人们选择了依赖注入（Dependency Injection, DI）这个名字。因此，DI 是 IoC 的一种特殊形式。

谈到这种模式的好处，你必须认识到，如果你决定在应用程序中使用 DI，它在灵活性和可互换性方面会带来哪些机会。如果你的应用程序组件中不再有硬编码的依赖项，并且已将解析依赖项的责任交给了环境，那么在测试中，你可以告诉环境它应该给你一个模拟对象（mock object）而不是实际对象。当然，你可以自己实现这个模拟对象。在测试中，指定某些依赖项应如何表现是非常简单的，这使得你可以单独测试一个组件。

在测试场景中，你显然拥有巨大的优势，因为你可以通过使用 DI 透明地替换某些依赖项的实际实现，而无需重新编译你的应用程序。因此，你的软件保持灵活，各个组件保持可互换性。

测试场景带来了巨大的优势，因为你可以通过使用 DI 轻松地替换某些依赖项的实际实现。因此，你的软件保持灵活，各个组件保持可互换性。

正如你将在本书后面看到的那样，DI 是 AngularJS 的一个核心主题，它为你在大多数应用程序组件中提供了优雅的依赖项处理方式。同样，DI 在测试中也很自然。你只需在测试中用模拟对象替换生产环境中的依赖项即可。

#### 可测试性

与大多数其他 JavaScript 框架不同，AngularJS 从设计之初就非常重视可测试性。其基本设计和对依赖注入的一致利用，使你能够广泛地以隔离和集成场景测试所有应用程序构建块。测试驱动开发方法使你能够实现客户端 Web 应用程序。对于所有 AngularJS 应用程序模块——特别是控制器、服务、指令和过滤器——都有单元测试的概念。此外，你可以使用`ngScenario`作为全面的特定领域语言（DSL）来定义端到端测试（E2E 测试）。

这些测试将单个应用程序视为一个黑盒。使用 DSL 函数，你可以触发用户交互并检查结果是否符合预期。清单 2.1 中的示例展示了一个虚构用户登录的 E2E 测试。

##### 清单 2.1：用户登录的 E2E 测试

```javascript
describe('User Login', function() {
  it('should successfully login the user', function() {
    input('user').enter('John');
    input('password').enter('123asd');
    element(':button').click();
    expect(element('h1').text()).toEqual('Hello, Tom!');
  });
});
```

此外，AngularJS 自带模拟服务实现，你可以用它来为测试产生给定的条件。例如，有一个用于`$http`服务的`$httpBackend`模拟对象，它可以阻止对基于 REST 的后端的真实请求，只检查是否调用了`$http`服务的相应功能。同样，你可以轻松地模拟一个基于 REST 的后端，并考虑如果真实的 REST 服务返回特定记录会发生什么。

#### 关键概念总结

- AngularJS 基于模型-视图-视图模型模式（MVVM）。
- 视图模型层在框架中通过作用域（scopes）实现。
- AngularJS 中一个非常重要的特性是双向数据绑定。它确保当作用域中的某些数据发生更改时，视图会自动更新。同样，反向的更新也会自动执行。
- 双向数据绑定基于作用域。这种类型数据绑定的所有数据都必须在作用域中定义。
- 另一个在 AngularJS 中无处不在的关键概念是依赖注入，即依赖项的自动解析。
- AngularJS 从设计之初就考虑到了可测试性。框架内的每个设计决策都强烈激励开发者编写整洁且可测试的源代码。

### 应用程序构建块

AngularJS 定义了一组具有明确指定功能的应用程序模块。通常，应用程序主要由这些构建块的组合构成。在本节中，我们将简要介绍这些模块，让你了解 AngularJS 的概念，并解释这些组件如何相互关联。

#### 模块

在 AngularJS 中，模块代表最大的结构，它封装了一组相关的应用程序组件。特别是，它作为控制器、服务、指令和过滤器的容器。符合软件工程中模块的定义，一个 AngularJS 模块应至少具有以下属性：

- 高内聚性。
- 明确的 API。
- 高度的可重用性。

在模块级别，AngularJS 也使用依赖注入。因此，其他模块可以轻松地作为模块的依赖项集成进来。只要该模块之前已通过`<script>`标签包含在`index.html`中，AngularJS 就会自动提供依赖项解析。

一个 AngularJS 应用程序至少包含一个模块，该模块在 DOM 完全加载时由框架自动启动和执行。使用`ngApp`指令，你可以告诉 AngularJS 哪个模块是起始模块。互联网上的许多示例都基于单个模块，该模块包含了示例所需的所有应用程序组件（控制器、服务、指令、过滤器）。这种最小化的组合类型对于大多数小型示例应用程序来说已经足够。然而，在一个有多团队的大型项目中，你应该考虑如何将各部分划分到模块中，以实现高度的可重用性。与官方的 AngularJS 开发者指南（在`http://docs.angularjs.org/guide/module`）所说的“模块应根据其包含的技术组件来定义”相反，我们自己的经验表明，技术定义在大项目中通常证明更有用。因此，在一个虚构的应用程序中，如果有一个名为用户管理的模块，其中实现了用户管理的完整方面，那么除了包含所有应用程序部分的`app-controllers`模块之外，几乎总是还有更多模块。

除了你自己的应用程序模块之外，还有各种由第三方实现和管理的开源模块。

## 3 AngularJS

本节包含 AngularJS 模块，例如 angular-translate、Angular UI 和 AngularStrap。

#### 控制器

控制器包含对作用域的设计要求，因此定义了特定视图所需的数据和逻辑。控制器实例会获得自己的作用域，在其中定义变量或函数。然后可以从视图内部访问这些变量和函数。正如已经提到的，作用域可以通过原型链相互继承，从而形成一个层次结构。当你在应用程序中嵌套控制器时，这个层次结构的很大一部分就建立在 AngularJS 之上。

在 AngularJS 中，控制器与服务有密切的联系。服务再次通过依赖注入获得。这也意味着你可以在测试中用一个模拟实现来替换服务。

在实现控制器时，你应该遵守某些准则。控制器实现应该是专注的，并且源代码有意义。这意味着你应该将任何复杂逻辑封装在服务中，然后通过依赖注入将其注入到控制器中。此外，控制器不应该持有任何数据，而只应在它们的作用域中提供对数据的引用。实际的数据存储反过来应该封装在作为数据访问对象的服务中。在控制器中进行任何操作以操作 DOM 都是禁忌。每当你发现自己需要进行 DOM 操作时，你应该首先考虑是否可以改用`ngRepeat`、`ngShow`或`ngClass`等默认指令。如果你确实需要进行 DOM 操作的情况，请在一个单独的指令中执行此操作。

#### 模型

与许多其他 JavaScript 框架不同，在 AngularJS 中，持有数据的对象（即模型）是普通的 JavaScript 数据类型。这意味着你的模型不必继承自某些框架类，也不需要遵循其他约定。定义一个普通对象或原始数据类型的数组就足以满足 AngularJS 模型的要求。如前所述，AngularJS 使用双向数据绑定来同步模型及其在视图中的相应表示。在此我们应该再次提及，只有当模型定义在作用域中时，才能应用此双向数据绑定。在下面的示例中，你可以看到如何建立一些有效的模型定义，其中包括双向数据绑定。

##### 清单 2.2：控制器作用域中的模型定义

```angular
angular.module('myApp')
    .controller('MyCtrl', function($scope) {
        // a simple JavaScript array
        $scope.family = [
          'James Doe', 'Clarissa Doe', 'Ted Doe'
        ];
        // a primitive value
        $scope.loggedIn = true;
    });
```

#### 路由



单页应用程序（SPA）中的一个典型问题是通过 URL 寻址应用程序的各个部分，同时与浏览器的前进和后退功能相结合。在这个语境中，我们也称之为深度链接。这方面对于经典的往返式 Web 应用程序来说有简单的解决方案，但在客户端 Web 应用程序中需要更高的开销。幸运的是，现代浏览器提供了 History API，允许对浏览历史进行读写访问。这样，你可以根据应用程序状态以编程方式更改 URL（例如，在浏览器的地址栏中），而无需重新加载完整的应用程序。

尽管 History API 很简单，Angular 更进一步，将这种逻辑抽象为路由。因此，你可以方便地将模板中的 URL 与其关联的控制器进行映射。

###### 清单 2.3：AngularJS 应用程序的路由定义

```angular
angular.module('myApp').config(function ($routeProvider) {
    $routeProvider
        .when('/', {
            templateUrl: 'templates/mainTemplate.html',
            controller: 'MainCtrl'
        })
        .when('/user/:userId', {
            templateUrl: 'templates/userDetailsTemplate.html',
            controller: 'UserDetailsCtrl'
        })
        .when('/user', {
            templateUrl: 'templates/
```

正如你在清单 2.6 的模板中看到的，花括号中写了一个表达式。在这些花括号内，你可以使用 JavaScript 的一个子集来生成输出。然而，该表达式无法使用 JavaScript 的 `eval()` 函数进行简单求值。因此，关于表达式有以下特别说明：

1. 求值并非像 `eval()` 那样针对全局的 `window` 对象进行，而是针对模板上下文中有效的作用域进行。
2. 求值结果为 `undefined` 或 `null` 的表达式不会生成输出，因为潜在的异常（如 `ReferenceError` 或 `TypeError`）会被捕获并忽略。
3. 不能使用控制流语句，如条件语句或循环语句。

你也可以在表达式中执行简单的计算（参见清单 2.7）。

###### 清单 2.7：表达式中的简单计算

```html
<div>
    <p>
        Hello, {{user.name}}!<br>
        Five years ago you were
        {{user.age - 5}} years old.
    </p>
</div>
```

我们已经提到，表达式主要存在于模板中求值作用域数据。结合双向数据绑定，这意味着 AngularJS 确保当对应的作用域值发生改变时，表达式会自动再次求值。因此，如果底层数据发生了改变，框架会自动更新视图。

表达式之所以如此强大，是因为你可以使用格式化过滤器来重新格式化数据。更详细的解释可以在后续的小节中找到。

#### 过滤器

在 AngularJS 中有两类过滤器。在上一章中我们提到了格式化过滤器。在同一章的另一节中，我们讨论了集合过滤器，它可以与 `ngRepeat` 指令结合使用，用于过滤或转换集合。此处的集合可以是数组或对象哈希。

##### 格式化过滤器

你在表达式中使用格式化过滤器来格式化或转换表达式的结果。你可以在表达式中使用管道语法，如清单 2.8 所示。

#### 清单 2.8：应用于表达式的过滤器

```html
<div>
    <p>
        Hello, {{user.name | uppercase}}!<br>
        Five years ago you were
        {{user.age - 5}} years old.
    </p>
</div>
```

在清单 2.8 的示例中，`uppercase` 过滤器被应用于求值后的表达式 `user.name`。作为 AngularJS 附带过滤器集的一部分，该过滤器将字符串转换为大写。此模板在视图中的输出结果将是清单 2.9 中的字符串。

#### 清单 2.9：uppercase 过滤器的结果

```text
Hello, JOHN DOE!

Five years ago you were

22 years old.
```

除了 `uppercase` 过滤器，AngularJS 还包含其他有用的格式化过滤器，我们将在后面讨论。此外，你可以定义自己的格式化过滤器。清单 2.10 展示了一个示例。

#### 清单 2.10：alternatingCase 过滤器

```javascript
angular.module('myApp').filter('alternatingCase', function () {
    return function (input) {
        var output = '',
            tmp;
        for (var i = 0; i < input.length; i++) {
            tmp = input.charAt(i);
            if (i % 2 === 0) {
                output += tmp.toUpperCase();
            }
            else {
                output += tmp.toLowerCase();
            }
        }
        return output;
    };
});
```

`alternatingCase` 过滤器可能看起来有些刻意，但其存在的唯一目的就是用于教学。该过滤器的作用是将输入字符串的大小写交替转换。格式化过滤器的编程接口非常简单。它接收求值后的表达式结果作为函数参数，然后可以对输入执行任何操作。最后，它返回一个输出，该输出随后会被显示。

#### 清单 2.11：使用 alternatingCase 过滤器

```html
<div>
    <p>
        Hello, {{user.name | alternatingCase}}!<br>
        Five years ago you were
        {{user.age - 5}} years old.
    </p>
</div>
```

#### 清单 2.12：alternatingCase 过滤器的结果

```text
Hello, JoHn dOe!

Five years ago you were

22 years old.
```

#### 集合过滤器

除了用于表达式的格式化过滤器，还有集合过滤器。从 API 角度看，集合过滤器的结构与格式化过滤器相同，但它们用在不同的上下文中，与 `ng-repeat` 指令结合使用。

此时你还不知道指令是什么以及能用它们做什么。然而，我们应该提到 `ng-repeat` 指令用于在模板中输出数组或对象哈希的元素。你可以将 `ng-repeat` 看作是循环的声明式对应物。

#### 清单 2.13：使用 ng-repeat

```html
<div>
    Family members of {{user.name}}:
    <ul>
        <li ng-repeat="member in family">{{member}}</li>
    </ul>
</div>
```

在清单 2.13 的示例中，作用域变量 `family` 引用一个字符串数组，其中包含家庭成员的名字。`ng-repeat` 指令确保每个元素在视图中渲染为一个 `<li>` 标签。因此，你得到一个显示 John Doe 家庭成员的视图。`ng-repeat` 指令在运行时生成的 HTML 代码如清单 2.14 所示。

#### 清单 2.14：视图中的 HTML 代码结果

```html
<div>
    Family members of John Doe:
    <ul>
        <li>James Doe</li>
        <li>Clarissa Doe</li>
        <li>Ted Doe</li>
    </ul>
</div>
```

脑海中立即浮现的问题是：我们能否过滤这个输出，只返回集合的一个子集？这正是集合过滤器的用武之地。它们确保根据某些元素过滤集合，或者以特定方式转换其元素。与 `ng-repeat` 结合时，我们再次使用管道表示法。下面的例子演示了 AngularJS 的 `filter` 过滤器。诚然，这个过滤器的命名不是很深思熟虑，但它确实达到了目的。

#### 清单 2.15：在 ng-repeat 中使用过滤器

```html
<div>
    Family members of {{user.name}}:
    <ul>
        <li ng-repeat="member in family | filter:'clarissa'">
            {{member}}
        </li>
    </ul>
</div>
```

我们在这里使用 `filter` 过滤器，是因为我们只想打印包含单词 `clarissa` 的家庭成员的名字。该过滤器不区分大小写。

AngularJS 的标准库中还有其他集合过滤器，包括 `limitTo` 和 `orderBy`。由于两者都影响集合的输出，它们的作用从名字上就应该很清楚了。尽管如此，我们将在本书后面提供一个使用它们的应用程序示例，并更详细地解释它们。

如果这些过滤器都不能满足你的需求，你可以定义一个新的集合过滤器。在以下示例中，我们定义了一个名为 `endsWithDoe` 的独立集合过滤器。使用这个过滤器，我们希望确保只返回以字符串 `Doe` 结尾的项目。

#### 清单 2.16：我们在 ng-repeat 中的 endsWithDoe 过滤器

```javascript
angular.module('myApp').filter('endsWithDoe', function () {
  return function (inputArray) {
    var outputArray = [];
    angular.forEach(inputArray, function(item) {
      if (item.length >= 3
        && item.substring(item.length - 3) === 'Doe') {
        outputArray.push(item);
      }
    });
    return outputArray;
  };
});
```

正如你在清单 2.16 的示例中所看到的，集合过滤器的 API 与格式化过滤器的 API 非常相似。唯一的区别是，在这个示例的过滤器函数中，我们得到一个数组作为输入（而不是像格式化过滤器那样的字符串），AngularJS 相应地期望过滤器函数返回一个数组。在过滤器函数内部，你可以操作输出数组以实现所需的行为，或者构建一个全新的数组。在 `endsWithDoe` 过滤器中，我们选择了后一种方式。为了完整性，下面的示例展示了如何使用我们自己的集合过滤器。为了解释效果，我们还应该向原始数组补充一些不以字符串 `Doe` 结尾的姓名。

#### 清单 2.17：向我们的数组添加成员

```javascript
angular.module('myApp').controller('MyCtrl', function ($scope) {
  $scope.user = {
    name: 'John Doe',
    age: 27,
    email: 'john@doe.com'
  };
  $scope.family = [
    'James Doe', 'Clarissa Doe', 'Ted Doe',
    'Burk Smith', 'Samantha Jones', 'Bill Brooks'
  ];
  $scope.loggedIn = true;
});
```

#### 清单 2.18：在 ng-repeat 中使用我们的 endsWithDoe 过滤器

```html
<div>
  Family members of {{user.name}}:
  <ul>
    <li ng-repeat="member in family | endsWithDoe">{{member}}</li>
  </ul>
</div>
```

如果你运行这个示例，你会发现只返回了三个名字，它们都以 `Doe` 结尾，尽管输出数组现在包含了六个名字。

最后，我们应该进行重构，使我们的过滤器更加通用。它应该不仅能过滤字符串“Doe”，而且能过滤任何任意字符串。

## 第 2 章：基本原则与概念 43

由于过滤器 API 支持过滤器参数，我们可以轻松融入这一改动。此外，我们还应该将过滤器重命名为 `endsWith`。

##### 清单 2.19：带参数的 endsWith 过滤器

```javascript
angular.module('myApp').filter('endsWith', function () {
	return function (inputArray, endsWith) {
		var outputArray = [],
			subString,
			hasMinLen,
			isSubStringMatching;
			angular.forEach(inputArray, function(item) {
				hasMinLen = item.length >= endsWith.length;
				subString = item.substring(item.length
					- endsWith.length);
				isSubStringMatching = subString === endsWith;
				if (hasMinLen && isSubStringMatching) {
					outputArray.push(item);
				}
			});
		return outputArray;
	};
});
```

本质上，如果我们使用过滤器参数，AngularJS 会用第二个参数调用我们的过滤器函数。我们现在可以利用它来调整逻辑，以适配第二个参数。临时变量 `subString`、`hasMinLen` 和 `isSubStringMatching` 并非必需，引入它们只是为了在函数体中避免过长的代码行。

为了完整起见，我们模板的新版本如清单 2.20 所示。

##### 清单 2.20：使用我们的 endsWith 过滤器

```html
<div>
  Family members of {{user.name}}:
  <ul>
    <li ng-repeat="member in family | endsWith:'Doe'">{{member}}</li>
  </ul>
</div>
```

这里的区别在于，我们调用 `endsWith` 过滤器时传递了一个字符串参数（"Doe"）。视图中的结果与 `endsWithDoe` 过滤器的示例相同。然而，得益于我们的重构，`endsWith` 过滤器变得可复用，并有可能在应用的其他部分使用。

#### 服务

通过其灵活的 API，服务可用于多种任务。如前所述，控制器应尽可能地保持精简，这意味着通常将复杂的例程和算法外包给服务。事实上，服务不仅可由控制器使用，而且几乎任何应用组件都可以使用。某些服务可以在其他服务中使用。服务的集成基本上是通过依赖注入完成的。

服务在实现应用时有一些特殊之处需要考虑。服务的一个基本特性是，每个服务在应用中只实例化一次。因此，每个服务都遵循单例模式。AngularJS 中所谓的注入器确保每次通过依赖注入获取服务时，总是复用相同的实例。因此，服务特别适合在多个控制器中复用逻辑和数据。

服务的另一个特点是可替换性，以及与之一同定义的清晰且稳定的 API。重要的是，要设计好服务的公共接口，以便能够轻松替换其实现。这是一个重要的特性，尤其关系到应用的可测试性和灵活性。例如，你可以定义一个服务来确保应用数据的持久化。你可以在其公共 API 中提供典型的 CRUD 操作。在整个系统的开发过程中，你可以最初基于 HTML5 本地存储 API 提供一个实现。当后端准备好后，你可以替换服务实现，使服务指向 REST 端点并将数据存储在服务器上。

除了可替换性和灵活性之外，刚才提到的示例还展示了服务的另一种应用。在 AngularJS 应用中使用服务作为数据访问对象是合理的，因为它们可以提供给每个需要相应数据的控制器。

清单 2.21 展示了服务的定义。

##### 清单 2.21：日志服务的定义

```javascript
angular.module('myApp').factory('log', function() {
    // Service Implementation
    var log = function(level, message) {
        console.log('[' + level + '] ' + message);
    };

    // Public API
    return {
        error: function(message) {
            log('ERROR', message);
        },
        info: function(message) {
```



```javascript
log('INFO', message);

},

debug: function(message) {

    log('DEBUG', message);

}

};

});
```

清单 2.21 展示了一个简单的服务，它定义了一个相当基础的日志 API，并基于`console.log()`提供实现。该服务实现远未达到可在生产环境中使用的水平，出于教学目的而有意保持简单。

这段代码有趣的是，我们没有使用名为`service()`的函数来定义服务，而是使用了`factory()`函数。事实上，在 AngularJS 中，服务可以通过多种方式之一来定义。其中，可以使用`service()`函数注册服务。通常仅在特定应用中使用此方法，即当你想将现有类的属性注册为服务实例时。

具体而言，有五种定义服务的方法。表 2.1 提供了一个概览，简要介绍了这五种方法。

最常见的形式是所谓的*工厂*方法，我们在清单 2.21 中使用了它。除了`factory()`之外，还可以使用`value()`、`constant()`、`provider()`和`service()`函数来定义服务。

| 服务定义 | API | 描述 |
| --- | --- | --- |
| Provider | `provider(...)` | 定义服务的基本 API，可在配置阶段进行配置。必须提供返回相应服务实例的`$get()`函数。可以使用构造函数或对象调用。 |
| Factory | `factory(...)` | 基于 Provider API 构建。从可配置性方面进行了抽象，如果可配置性无关紧要，可提供更便捷的服务定义。 |
| 构造函数 | `service(...)` | 基于 Factory API 构建。使用`new`运算符结合给定的构造函数实例化服务实例。因此，现有类的实例可以注册为服务。 |
| 值作为服务 | `value(...)` | 基于 Factory API 构建。允许将值注册为服务。该值可以是原始类型、对象或函数。 |
| 常量作为服务 | `constant(...)` | 将常量值注册为服务。该值在运行时无法更改。 |

表 2.1：五种服务定义方法

现在，你当然可能会问这个合理的问题：所有这些服务定义方法之间有什么区别？

如图 2.2 所示，各种服务定义方法大多是构建在彼此之上的。`providerCache`和`instanceCache`作为 AngularJS 应用的提供者或服务实例的基本容器。使用`provider()`函数可以访问`providerCache`，并以这种方式注册提供者。因此，服务提供者是一个必须定义`$get()`函数的组件，该函数最终由框架调用，并必须返回服务实例。你的服务的单例实例在`instanceCache`中管理。然而，在实际服务对象实例化之前，你可以在应用的配置阶段使用提供者配置服务对象。其他方法则不具备此选项。因此，提供者的服务定义是最强大但同时也是最复杂的获取服务实例的方式。

![](img/7a003218cea01579a50512a6c0e40f28_54_0.png)

##### 图 2.2：服务生态系统

服务工厂（我们在定义`log`服务时使用了它）在内部使用`provider()`函数，并通过从可配置性方面进行抽象来简化定义。这样，你可以通过简单地定义一个返回服务对象的工厂函数来创建服务定义。缺点是你无法再配置你的服务。

图 2.2 还显示`service()`和`value()`函数依次构建在工厂之上。因此，`service()`函数除了服务名称外还期望一个构造函数。在内部，`service()`函数创建一个服务工厂，最终使用传递的构造函数实例化服务对象。实例化在内部使用`new`运算符完成，这允许你在构造函数内定义你的服务对象。这意味着你可以很简单地将现有类的实例注册为服务实例。

`value()`函数是最简单但也是最原始的服务定义获取方式。顾名思义，`value()`函数将一个值注册为服务。在这种情况下，该值可以包含原始数据类型，例如数字或布尔值。然而，任何对象或函数都可以轻松地作为服务进行部署，并通过依赖注入在整个应用程序中使用。从纯粹技术的角度来看，`value()`函数创建一个工厂，该工厂进而将传递的值封装并返回到服务实例中。因此，在内部，`value()`函数使用`factory()`函数。

除了相互构建的服务定义方法之外，还有`constant()`函数。该函数将常量值注册为服务。这意味着注册的值在运行时不能更改。因此，`constant()`函数可以直接访问`providerCache`和`instanceCache`容器。

现在我们将为枯燥的理论注入一些活力，并通过一些示例服务定义来阐明上述描述。

##### 清单 2.21：使用工厂定义日志服务

基于我们在清单 2.21 中使用工厂定义的日志服务，我们现在将使用 provider 来实现相同的服务，以便仍然能够进行一些小的配置。

```javascript
angular.module('myApp').provider('log', function() {

    /* 私有状态/方法 */

    var prefix = '', suffix='';

    // 服务实现

    var log = function(level, message) {

        console.log(prefix + '[' + level +']' +

            ' ' + suffix);

    };

    return {

        $get: function() {

            return {

                error: function(message) {

                    log('ERROR', message);

                },

                info: function(message) {

                    log('INFO', message);

                },

                debug: function(message) {

                    log('DEBUG', message);

                }

            };

        }

    };

});
```

清单 2.22 展示了使用 provider 定义我们的`log`服务。这段代码中有趣的是，我们使用服务名称和一个 provider 的构造函数来调用`provider()`函数。如表 2.1 所示，除了构造函数之外，我们还可以选择传递一个需要类似构造的对象。特别是，这个对象也需要有一个名为`$get()`的函数。当框架需要创建适当的服务实例时，AngularJS 将调用该函数，一旦它首次作为依赖被请求。在这种情况下，每个服务恰好调用一次该函数，因为如前所述，服务是单例对象。

无论如何，此时我们选择了构造函数的替代方案。一般来说，这个选项也常被使用，因为它允许你定义无法从外部访问的变量。具体来说，在这个例子中，`prefix`和`suffix`变量包含我们日志消息的前缀或后缀。此外，引用函数的`log`变量是我们 API 实现的基础，它是“私有的”，无法从外部访问。

另一方面，使用`this`定义的`setPrefix()`和`setSuffix()`provider 函数是公共的，在配置阶段（在`config()`块中）被调用以进行服务的必要设置，即为所有日志消息定义前缀或后缀。`$get()`函数也是公开的，因此可以从外部访问。如前所述，该函数在 AngularJS 中具有特殊含义，因此不应从你自己的应用程序代码中调用。

#### JavaScript 中的函数

在 JavaScript 中，函数是一种非常强大的构造，你可以在其上映射许多经过验证的软件工程概念和范式。特别是，例如，在你的 provider 定义中，你采用了构造函数的概念，用它定义了一个匿名类。

在我们准备好 provider 以启用设置前缀或后缀的功能后，我们现在应该转向实际的配置。

#### 清单 2.23：在`config()`块中配置我们的日志 provider

```javascript
angular.module('myApp').config(function (logProvider) {

    logProvider.setPrefix('[myApp ');

    logProvider.setSuffix('.');

});
```

清单 2.23 展示了我们`log`服务的一种可能配置。要配置该服务，我们使用框架（通过依赖注入）传递的先前定义的 provider`logProvider`。我们使用`setPrefix()`和`setSuffix()`公共实例方法来设置字符串，这些字符串将包含每条日志消息的前缀和后缀。

#### 配置块

在本章的前面，我们使用`config()`块通过`$routeProvider`组件来配置应用程序路由。你可以使用配置块在实际应用程序启动之前，通过适当的服务 provider 来执行我们服务的配置。为此，你可以通过在服务名称后追加字符串“Provider”来使适当的 provider 通过依赖注入获得。

需要注意的是，在配置块中，你实际上传递的是服务 provider 而不是实际的服务。后者行不通，因为框架除了一些例外情况，只允许在配置块中注入 provider。

你可能仍然希望在应用程序启动时调用实际服务实例的函数，例如启动一个重复任务，因此 AngularJS 还为你提供了一个特殊的构造，即`run()`块。

在我们的日志服务配置完成后，我们展示一个示例，说明如何在控制器中使用该服务。

#### 清单 2.24：使用我们的日志服务

```javascript
angular.module('myApp').controller('MyCtrl', function($scope, log) {

    log.debug('MyCtrl has been invoked');

});
```

清单 2.24 展示了我们可以多么轻松地在控制器中使用我们的日志服务，只需将其名称指定为控制器函数的参数即可。然后我们可以访问属于公共 API 的函数。对于日志服务，这些函数是`debug()`、`info()`和`error()`，其中只有`debug()`用于在浏览器控制台中输出。

#### 指令

指令可能是 AngularJS 中最有趣的特性，因为框架通过这一特性展现了其独特的卖点。你可以使用指令扩展 HTML 词汇表。这意味着你可以发明新的 HTML 标签和属性。使用指令，你可以将复杂的逻辑隐藏在标签或属性后面。毫无疑问，这个概念因此是 AngularJS 的关键方面之一。

一个主要优势是，你可以首次使用指令创建可重用的 Web 组件。例如，你可以编写一个指令来封装应用程序中频繁使用的某些 UI 部件，从而消除大量否则必须编写的冗余代码。通过这种方式使用指令，你可以创建组织范围内具有统一“外观和感觉”的组件库。你还可以确保重复的部件不需要重新开发。

使用指令，应用程序还可以以声明方式描述。你可以设计开发人员已经知道的标签或属性名称。因此它们具有语义价值。新开发人员可以在不深入表面之下的情况下对应用程序有初步了解。你团队中的现有开发人员将对由此产生的清晰度和相关维护感到满意。

指令是一个强大的特性，负责确保应用程序代码结构化和可重用。遗憾的是，这一切是有代价的，即一个非常复杂的 API。

##### 命名约定

为了在一个真实的例子中说明指令的概念，我们现在展示上一章的`colorPicker`指令并讨论其细节。

##### 清单 2.25：`colorPicker`指令的定义

```javascript
angular.module('myApp').directive('colorPicker', function () {

    // 实现放在这里

});
```

正如你在上一章中学到的，你可以使用`directive()`函数定义指令。该函数接受两个参数，指令的名称和一个工厂函数。不要将此处的工厂函数与服务上下文中的工厂混淆。

按照约定，指令名称以小写字母开头，如果名称由多个单词组成，则遵循驼峰命名法。HTML 标签或由指令定义的属性的标识通过将驼峰命名法映射为短横线分隔的命名法来完成。例如，`spreadsheet`、`chart`或`colorPicker`都是有效的指令名称。相应的 HTML 标签将是`<spreadsheet>`、`<chart>`和`<color-picker>`。对于`colorPicker`，你还可以使用`<color:picker>`和`<color_picker>`，因为 AngularJS 使用冒号（`:`）、连字符（`-`）和下划线（`_`）作为分隔符。

正如上一章提到的，还有另外两种有效的调用指令的方式，即使用`data-`或`x-`前缀。原因是旧浏览器只允许带有这些前缀之一的用户定义标签和属性。因此，你还可以在模板中使用`<data-spreadsheet>`或`<x-spreadsheet>`。

# 指令命名

认识和理解这种命名约定非常重要，这样在创建自己的指令时才能避免任何令人不快的意外。特别不建议给指令起一个不符合隐式约定的名称。

##### 带链接函数的定义

AngularJS 期望你作为第二个参数传递的工厂函数返回一个函数或一个指令定义对象。如果你返回一个函数，那么这个函数就被称为指令的链接函数。在指令定义对象的情况下，你可以通过许多属性来非常精细地控制指令的行为。因此，返回一个函数（链接函数）代表简单情况，而返回一个指令定义对象则代表复杂情况。

###### 清单 2.26：通过返回链接函数定义`colorPicker`指令

```javascript
```

在清单 2.26 中，我们首先考虑简单情况，即在`colorPicker`指令的工厂函数中返回一个函数（一个链接函数）。对于指令的每个实例，链接函数恰好被调用一次。因此，在链接函数内，你可以注册事件处理器来执行 DOM 操作，并执行其他特定于该实例的例程。简而言之，链接函数允许你为指令的每个实例执行初始化操作。在调用链接函数时，AngularJS 至少传递三个参数：

清单 2.26 中链接函数的实现只是向浏览器控制台写入一条消息。为了查看这个最小指令的实际运行情况，我们需要编写一个使用该指令的小模板。

###### 清单 2.27：在模板中使用`colorPicker`指令

```html
<div color-picker></div>

<div color-picker></div>

<div color-picker></div>
```

清单 2.27 显示了一个使用我们最小`colorPicker`指令的示例模板。如模板中所示，我们使用我们的最小指令定义创建了一个新的 HTML 属性。该属性不一定非要放在`div`标签中，可以在任何其他标签中使用。因此，如果你通过简单地在工厂函数中返回一个链接函数来实现一个指令，那么默认情况下你会创建一个新的 HTML 属性。为了使示例可行，我们还将创建一个包含三个文件的最小应用程序。

1. **index.html**。我们应用程序的入口点和基础模板。
2. **app.js**。我们应用程序的模块定义。
3. **color-picker.js**。我们`colorPicker`指令的定义。

###### 清单 2.28：我们最小`colorPicker`应用程序的`index.html`

```html
<!DOCTYPE html>

<html ng-app="colorPickerApp">

<head>

    <meta charset="utf-8">

</head>

<body>

<div color-picker></div>

<div color-picker></div>

<div color-picker></div>

<script src="lib/angular/angular.js"></script>

<script src="scripts/app.js"></script>

<script src="scripts/directives/colorPickerDirective.js"></script>

</body>

</html>
```

清单 2.28 显示了我们最小 AngularJS 应用程序的`index.html`。它作为浏览器的入口点，并定义了应用程序的基本模板。为了防止此示例变得不必要的复杂，我们将清单 2.27 中的示例模板插入到了我们的基础模板中。

###### 清单 2.29：我们最小`colorPicker`应用程序的`app.js`

```javascript
var colorPickerApp = angular.module('colorPickerApp', []);
```

清单 2.29 显示了`colorPickerApp`模块的模块定义，当浏览器完成加载 DOM 时，AngularJS 会自动加载该模块。AngularJS 执行此操作的指令可以在`index.html`中的`ngApp`指令中找到。

###### 清单 2.30：我们最小`colorPicker`应用程序的`color-picker.js`文件

```javascript
colorPickerApp.directive('colorPicker', function() {

  return function(scope, element, attrs) {

    console.log("It's me, colorPicker!");

  }

});
```



最后但同样重要的是，我们仍然需要`colorPicker`指令的最小定义（`color-picker.js`文件），如清单 2.30 所示。

> 示例的项目结构

对于这个示例，我们将临时模块`myApp`重命名为`colorPickerApp`。此外，我们为 JavaScript 文件创建了一个`scripts`子目录。该目录包含`app.js`文件（其中包含我们的模块定义）以及一个名为`directives`的子目录，其中包含`color-picker.js`文件。该文件包含我们的最小指令定义。此结构与使用 Yo 工具创建应用程序组件时自动生成的结构相对应。事实证明，对于单模块应用程序（即只有一个模块的应用程序），这是一种有用且适用的最佳实践。

### 带指令定义对象的定义

如上一节所述，你可以通过在工厂函数中返回一个链接函数来定义指令。现在让我们更仔细地研究一下指令定义对象（DDO）。这种类型的定义要复杂得多，但允许非常细粒度地描述指令的行为。你在上一章开发`colorPicker`指令时学习了这种定义，当时我们使用了这样一个 DDO。因此，我们对这种类型定义的讨论也是基于`colorPicker`示例。

我们开始吧。我们将把前一节中返回链接函数的指令转换为 DDO。

#### 清单 2.31：使用指令定义对象定义 colorPicker 指令

```javascript
colorPickerApp.directive('colorPicker', function() {

  return {

    link: function(scope, element, attrs) {

      console.log("It's me, colorPicker as DDO!");

    }

  };

});
```

清单 2.31 显示了我们使用 DDO 定义的`colorPicker`指令。在这种形式下，此定义等效于清单 2.30 中的定义。你也可以在 DDO 中通过将函数赋值给`link`属性来定义链接函数。

接下来，我们想更改指令，使其定义一个 HTML 标签而不是 HTML 属性。我们通过在 DDO 中使用作用域的`restrict`属性来实现这一点。

#### 清单 2.32：使用 restrict 定义作用域

```javascript
colorPickerApp.directive('colorPicker', function() {

  return {

    restrict: 'E',

    link: function(scope, element, attrs) {

      console.log("It's me, colorPicker as DDO!");

    }

  };

});
```

清单 2.32 显示我们将作用域设置为`E`，这将指令限制为 HTML 元素或 HTML 标签。现在我们只能将指令用作 HTML 标签。因此，我们需要将模板修改为清单 2.33 中的模板。

#### 清单 2.33：将 colorPicker 指令用作 HTML 标签

```html
<color-picker></color-picker>

<color-picker></color-picker>

<color-picker></color-picker>
```

`restrict`属性的值必须是一个字符串，其中包含集合`{'E', 'A', 'C', 'M'}`中的一个或多个字母。这些字母具有以下含义：

- `E`。HTML 元素或 HTML 标签
- `A`。HTML 属性
- `C`。CSS 类
- `M`。HTML 注释

因此，指令也可以与 CSS 类或 HTML 注释结合使用。

必须注意的是，对于大多数指令，相应的 HTML 标签或属性背后隐藏着某些逻辑或某些标记。你通常在链接函数中实现逻辑。至于指令的标记，通常使用`template`或`templateUrl`属性。对于这两个属性，AngularJS 都期望一个字符串值。你可以使用`template`属性在 DDO 中直接以字符串形式设置模板标记。另一方面，`templateUrl`属性期望一个指向模板的 URL。

> **指令模板**

作为指导，较短的模板直接在 DDO 中定义，而较长的模板存储在单独的文件中，并通过`templateUrl`引用。

在我们的`colorPicker`示例中，我们处理的是一个更复杂的模板，因此我们将其存储在一个单独的文件中，并在`templateUrl`属性中设置对其的引用。

#### 清单 2.34：引用 colorPicker 指令的模板

```javascript
colorPickerApp.directive('colorPicker', function() {

  return {

    templateUrl: 'templates/colorPickerTemplate.html',

    restrict: 'E',

    link: function(scope, element, attrs) {

      console.log("It's me, colorPicker as DDO!");

    }

  }

});
```

清单 2.34 表明，我们的`colorPicker`指令的模板可以在`colorPickerTemplate.html`文件中找到，该文件位于`templates`子目录下。这与我们在前一章中使用的模板相同。不过，为了便于阅读，我们在清单 2.35 中再次将其列出。

#### 清单 2.35：colorPicker 指令的模板定义

```html
R:<input type="range"

         min="0" max="255" step="1"

         ng-model="r"><br>

G:<input type="range"

         min="0" max="255" step="1"

         ng-model="g"><br>

B:<input type="range"

         min="0" max="255" step="1"

         ng-model="b"><br>

A:<input type="range"

         min="0" max="1" step="0.01"

         ng-model="a">

<div style="width: 300px; height: 100px;

     background-color:

     rgba({{ r }}, {{ g }}, {{ b }}, {{ a }});">

</div>
```

我们的`colorPicker`现在已完成，示例将会正常工作。你可以在浏览器中看到 AngularJS 创建了三个颜色选择器实例。然而，如果仔细观察，你会发现两个主要缺陷。

到目前为止，我们的颜色选择器没有初始值。因此，最初没有颜色预览，因为相应的`r`、`g`、`b`和`a`作用域变量最初是未定义的，所以 CSS`background-color`属性无法渲染。只有在我们至少移动每个滑块一次后，变量才会被赋予适当的值，颜色预览才会出现。

除此之外，我们的颜色选择器不是一个独立的组件，并且对周围上下文有不愉快的影响。也就是说，这三个实例并非相互独立。如果我们移动，比如说，其中一个实例的`r`控制器，另外两个实例的`r`控制器也会同时移动。其原因在于，在这个阶段实例还没有自己的作用域。因此，每个颜色选择器实例当前仍然绑定到根作用域的`r`、`g`、`b`和`a`变量，并在滑块移动时修改这些值。这种情况在图 2.3 中再次进行了可视化。由此产生的双向数据绑定导致了`colorPicker`实例之间的交互。

![](img/7a003218cea01579a50512a6c0e40f28_66_0.png)

### 指令的独立作用域

在查看初始值的问题之前，我们首先需要确保我们的`colorPicker`实例拥有它们自己的作用域。

#### 清单 2.36：为 colorPicker 指令定义独立作用域

```javascript
colorPickerApp.directive('colorPicker', function() {

  return {

    scope: true,

    templateUrl: 'templates/colorPickerTemplate.html',

    restrict: 'E',

    link: function(scope, element, attrs) {

        console.log("It's me, colorPicker as DDO!");

    }

};

});
```

清单 2.36 表明，通过将我们的 DDO 的`scope`属性设置为`true`，指令实例将获得自己的作用域。因此，如果你运行这个示例，你会看到颜色选择器实例不再相互干扰。每个实例都有自己的作用域，其中定义了`r`、`g`、`b`和`a`变量。这意味着双向数据绑定作用于每个实例自身作用域中的变量，而不会影响根作用域。

这个解决方案让我们离一个独立且可重用的组件更近了一步。然而，仍然有些不尽如人意之处。

我们的`colorPicker`指令的实例有自己的作用域，但该作用域目前仍然继承其父作用域的原型，在这种情况下仍然是根作用域。这意味着我们可以在`colorPicker`指令中访问父作用域的变量和函数，并可能操纵它们。如果我们打算创建一个独立且可重用的组件，那么当前的`colorPicker`指令显然并不理想。我们迟早可能会依赖父作用域的某些特性或变量，从而变得依赖于父作用域。结果，我们的组件只有在这种上下文中才能正常工作。它不是一个独立且可重用的组件。

此外，无意中操纵父作用域的变量可能导致棘手且难以识别的错误，最终会导致耗时的调试工作。

为了避免这个问题并与父作用域彻底分离，AngularJS 引入了隔离作用域的概念。

### 隔离作用域

你可以在指令内创建隔离作用域。尽管隔离作用域仍然是应用程序有效作用域层次结构的一部分，但该作用域不继承其父作用域的原型。这意味着你无法从指令的隔离作用域内部访问父作用域的数据或逻辑。相应地，你不能无意中修改父作用域。这意味着隔离作用域是创建可重用和独立组件的关键概念。

#### 清单 2.37：为 colorPicker 指令定义隔离作用域

```javascript
colorPickerApp.directive('colorPicker', function() {

  return {

    scope: {},

    templateUrl: 'templates/colorPickerTemplate.html',

    restrict: 'E',

    link: function(scope, element, attrs) {

      console.log("It's me, colorPicker as DDO!");

    }

  };

});
```

如清单 2.37 所示，我们通过向 DDO 的`scope`属性分配一个空对象（`{}`）来告诉 AngularJS 为我们的指令创建隔离作用域。因此，在这一点上，我们拥有了一个不依赖任何上下文的可重用颜色选择器。当我们通过实现链接函数中的指令逻辑时，仍然可能无意中操纵父作用域的变量。这种作用域层次结构的配置可以在图 2.4 中看到。

到目前为止，一切顺利。然而，正如已经提到的，通过隔离作用域你可以访问父作用域的数据和函数。而且仔细想想，你会发现大多数可重用组件都需要与它们的上下文建立连接。这些连接可以用于多种目的。其中之一是让组件从其周围上下文中接收数据。

我们的`colorPicker`需要这种对其上下文的访问。一方面，我们想要传递初始值。另一方面，我们希望在`colorPicker`内部更改颜色值时通知环境。那现在怎么办呢？

![](img/7a003218cea01579a50512a6c0e40f28_69_0.png)

图 2.4：具有隔离作用域的 colorPicker 实例

尽管隔离作用域中有“隔离”二字，AngularJS 允许你与父作用域建立受控的连接。有三种方式可以实现这种连接。最常用的连接可能是与父作用域中的变量建立双向数据绑定。该框架还为你提供了创建与父作用域的单向连接的机会，以及在指令内部调用父作用域中定义的函数。在后一种情况下，你甚至可以调用指令函数并传递内部数据。

在我们的`colorPicker`指令中，我们使用单向链接来设置初始值，并使用函数来通知环境颜色值的变化。清单 2.38 展示了整个过程。

#### 清单 2.38：隔离作用域的定义，并与父作用域建立受控连接

```javascript
colorPickerApp.directive('colorPicker', function() {

    return {

        scope: {

            r: '@initR',

            g: '@initG',

            b: '@initB',

            a: '@initA',

            onChange: '&'

        },

        templateUrl: 'templates/colorPickerTemplate.html',

        restrict: 'E',

        link: function(scope, element, attrs) {

          console.log("It's me, colorPicker as DDO!");

        }

    };

});
```

清单 2.38 展示了如何在使用隔离作用域的同时，建立与父作用域的多个连接。这样，你可以访问父作用域的数据和函数。主要因素在于，你不再向 DDO 的`scope`属性分配空对象。相反，你指定一个配置对象。该配置对象中的键用于指定指令隔离作用域中的哪些作用域变量应该连接到父作用域。如前所述，基本上有三种形式。这些由前缀`=`、`@`和`&`指定。

- `=`。表示指令隔离作用域中指定为键的作用域变量应与父作用域中的变量建立双向数据绑定。
- `@`。表示指令隔离作用域中指定为键的作用域变量应与父作用域建立单向数据绑定。
- `&`。表示指定为键的作用域变量应引用父作用域中的函数，并能够调用该函数并传递来自指令的内部数据。

当你查看清单 2.38 中如何使用`colorPicker`指令定义时，这一点会变得更加清晰。

#### 清单 2.39：通过指定初始值来使用 colorPicker 指令

```html
<color-picker init-r="255"

  init-g="0"

  init-b="0"

  init-a="1.0">

</color-picker>
```

### 连接父级作用域

前缀后的字符串指定了指令 HTML 标签的哪个 HTML 属性包含了关于连接应涉及父级作用域中哪个变量或函数的信息。如果用作键的对应 HTML 属性名称与隔离作用域中变量的名称相同，那么你可以省略前缀后的字符串。在清单 2.38 中，`onChange`作用域变量就展示了这一点。

清单 2.39 展示了一个使用我们的`colorPicker`指令的模板片段。尽管它具有隔离作用域，我们仍希望向其传递数据。在这种情况下，我们传递的数据是各个颜色分量的初始值。这里使用的 HTML 属性，`init-r`、`init-g`、`init-b`和`init-a`，与我们清单 2.38 中的指令定义相对应，必须用蛇形命名法指定。因为颜色分量的作用域变量是`r`、`g`、`b`和`a`（而不是`initR`、`initG`等），除了连接类型（这里是：`@`）之外，我们还需要用驼峰命名法指定 HTML 属性，即`initR`、`initG`、`initB`和`initA`。单向绑定在这里工作得很好，因为我们只想设置初始值，因此不需要双向数据绑定。图 2.5 再次说明了这种关系。

![](img/7a003218cea01579a50512a6c0e40f28_71_0.png)

图 2.5：作用域变量`r`、`g`、`b`和`a`的单向绑定

### 单向绑定

使用单向绑定，你可以将数据从父级作用域传递给具有隔离作用域的指令。当指令仅消费数据而上级控制器不关心任何更改时，这种类型的绑定特别有用。我们称其为单向绑定，因为数据交换仅在一个方向上发生，从父级控制器到指令。相比之下，如果你想将数据传递给指令，同时也对该数据的更改感兴趣，则需要使用双向数据绑定。

在这个例子中使用单向绑定仅仅意味着你可以使用 HTML 属性将固定值传递给`colorPicker`指令。然而，通常你希望在变量值在父级作用域中发生更改时得到通知。在这种情况下，你不会给 HTML 属性赋一个固定值。相反，你会赋一个表达式，当父级作用域中的作用域变量更改时，该表达式会不断被重新求值。所以类似这样：

```html
<color-picker init-r="{{r}}"></color-picker>
```



在指令内部，然后你可以观察作用域变量`r`，并根据更改执行某些逻辑。实际上，你使用`$observe()`函数在`attrs`对象上，AngularJS将该对象作为`link`函数的第三个参数传递。

我们现在为`colorPicker`指令分配了一个隔离作用域，将其变成了一个自包含且可重用的组件。此外，我们定义了与父级作用域的五个受控连接。具体来说，这四个是单向连接（`initR`、`initG`等），通过它们我们可以将初始值传递给颜色选择器实例，还有一个工作链接（`&`），我们随后将在颜色更改时使用它来调用回调函数。

在讨论`link`函数的实现之前，我们将首先介绍`MainCtrl`控制器，我们在其中定义了回调函数。关键在于，尽管具有隔离作用域，我们仍然可以通过使用`onChange`拥有这个回调函数。

代码清单 2.40：带有`handleColorChange()`回调函数的`MainCtrl`控制器定义

```
colorPickerApp.controller('MainCtrl', function ($scope) {

    $scope.handleColorChange = function(r,g,b,a) {

        console.log('handleColorChange', r, g, b, a);

    };

});
```

代码清单 2.40 展示了刚刚提到的`MainCtrl`控制器的实现。我们在控制器作用域中定义的`handleColorChange()`函数，代表了我们希望使其可被`colorPicker`指令访问的回调函数。在这个例子中，我们用简单的控制台输出来响应颜色选择器中的颜色更改。此外，我们还提供每个颜色分量的值以供查看。

为了保持良好的风格，我们将这个控制器定义在一个名为`mainCtrl.js`的单独文件中。我们还在`scripts`目录下创建了一个名为`controllers`的目录来存放我们的控制器。然后`mainCtrl.js`文件保存在`controllers`目录中。我们必须修改我们的`index.html`文件，使其加载新创建的`mainCtrl.js`文件。此外，我们仍然必须使用`ngController`指令来确定应为控制器的哪个DOM部分定义新的作用域。我们必须确保启动该部分的DOM元素是我们的`colorPicker`实例的父元素。因此，我们将`ng-controller`属性添加到`<body>`元素。这些更改的结果可以在代码清单 2.41 中看到。

代码清单 2.41：带有`ngController`指令的`index.html`

```
<!DOCTYPE html>

<html ng-app="colorPickerApp">

<head>

    <meta charset="utf-8">

</head>

<body ng-controller="MainCtrl">

<color-picker init-r="255" init-g="0" init-b="0" init-a="1.0">

</color-picker>

<script src="lib/angular/angular.js"></script>

<script src="scripts/app.js"></script>

<script src="scripts/directives/colorPickerDirective.js"></script>

<script src="scripts/controllers/mainCtrl.js"></script>

</body>

</html>
```

接下来，我们改变调用`colorPicker`指令的方式，以便可以传递回调函数。`index.html`的相关部分如代码清单 2.42 所示。

代码清单 2.42：通过指定回调函数补充`colorPicker`调用

```
<color-picker init-r="255" init-g="0" init-b="0" init-a="1.0"

               on-change="handleColorChange(r, g, b, a)">

</color-picker>
```

我们使用`on-change`属性将`handleColorChange()`函数的引用传递给我们的`colorPicker`实例。同样，使用蛇形命名法，因为我们在指令定义中编写了将包含该引用的`onChange`作用域变量。回想一下，从DDO到相应HTML属性的名称映射是通过将驼峰命名法替换为蛇形命名法来完成的。

为了检查创建的连接函数，我们应该进行一个简单的测试，并在`colorPicker`指令的`link`函数中通过`onChange`属性调用`handleColorChange`函数。代码清单 2.43 打印了相应的源代码。

代码清单 2.43：通过`onChange`引用调用`handleColorChange`函数

```
colorPickerApp.directive('colorPicker', function() {

  return {

    scope: {

      r: '@initR',

      g: '@initG',

      b: '@initB',

      a: '@initA',

      onChange: '&'

    },

    templateUrl: 'templates/colorPickerTemplate.html',

    restrict: 'E',

    link: function(scope, element, attrs) {

      console.log("It's me, colorPicker as DDO!");

      scope.onChange();

    };

  };

});
```

作用域层次结构和刚刚描述的场景在图 2.6 中进行了总结。圆角矩形表示引用函数的作用域变量。

![](img/7a003218cea01579a50512a6c0e40f28_75_0.png)

如果你运行这个示例，你将在控制台中得到预期的输出，如图 2.7 所示。

![](img/7a003218cea01579a50512a6c0e40f28_75_1.png)

**图 2.7：Chrome 中的控制台输出**

这意味着，尽管我们的`colorPicker`指令具有隔离作用域，我们仍然可以创建一个到父级作用域和`MainCtrl`控制器作用域的工作链接，因此可以通过`onChange`作用域变量访问`handleColorChange`函数。输出包含颜色分量，但目前的值是`undefined`。然而，很明显这是因为我们在指令内部的调用中没有传递参数。

好了，现在我们可以专注于最终要求，实现`link`函数，使得`handleColorChange`回调函数仅在颜色更改时被调用。`link`函数的最终实现如代码清单 2.44 所示。

**代码清单 2.44：我们的`colorPicker`指令的`link`函数的最终实现**

```
colorPickerApp.directive('colorPicker', function() {

  return {

    [...]

    link: function(scope, element, attrs) {

      var COLORS = ['r', 'g', 'b', 'a'];

      COLORS.forEach(function(value) {

        scope.$watch(value, function(newValue, oldValue) {

          if (newValue !== oldValue) {

            if (angular.isFunction(scope.onChange)) {

              scope.onChange(generateColorChangeObject());

            }

          }

        });

      });

      var generateColorChangeObject = function() {

        var obj = {};

        COLORS.forEach(function(value) {

          obj[value] = scope[value];

        });

        return obj;

      };

    }

  };

});
```



基本上，实现相当简单。首先，我们定义一个数组，其中包含各个颜色值的`$scope`变量名称。这样做纯粹是为了让后续源代码更清晰、更简洁。然后，我们遍历这个数组（使用`forEach`），并使用`scope.$watch`为每个颜色分量注册一个监听器。`$watch`函数需要两个参数。第一个参数是要监控变更的`$scope`变量名称。第二个参数我们传入一个函数，该函数在发生变更时会被调用。框架会传递两个参数，`newValue`和`oldValue`，分别包含`$scope`变量的新值和旧值。然后，我们检查这两个值是否相等，如果不相等，就调用`handleColorChange`回调函数，该函数可以通过`onChange` `$scope`变量访问。在此之前，我们确保`onChange`确实引用了一个函数。

现在，我们引入另一个AngularJS约定。`handleColorChange`回调函数定义为接受四个参数，即各个颜色分量`r`、`g`、`b`和`a`。通过这个函数，我们可以将这些参数传递到一个参数对象中。图2.8展示了这样一个参数对象的样子。

![](img/7a003218cea01579a50512a6c0e40f28_77_0.png)

基本上，对象的键参数必须与模板中的参数名称匹配，以便参数最终能够正确传递。在图2.8中，必要的匹配项以粗体显示。在我们的实现中，我们使用一个名为`generateColorChangeObject`的小型辅助函数来生成这个参数对象。

至此，我们完成了。通过指令，我们创建了一个自包含且可复用的组件，称为`colorPicker`。它可以在模板中通过指定`<color-picker>`来使用。由于AngularJS还以其他一些名称注册了这个指令，因此也可以使用`<color:picker>`和`<data-color-picker>`来使用它。此外，我们可以通过HTML属性向我们的颜色选择器传递初始值。最后，我们实现了一种机制，通过调用回调函数通知父组件颜色已发生变更。

如果你运行示例并移动任何滑块，你会得到一堆控制台输出，应该与图2.9中的类似。

![](img/7a003218cea01579a50512a6c0e40f28_78_0.png)

除了这里提到的DDO属性外，还有其他属性可用于控制指令的操作。你完全可以想象，这里展示的示例还远未耗尽指令的全部潜力。然而，要解释指令的每一个细节，还需要另一本专门介绍这个概念的书。表2.2提供了概览。

## 与Polymer的关系

尽管指令的概念以及相关的独立HTML元素创建使AngularJS独树一帜，但不可否认这个概念仍然存在弱点。尽管通过隔离作用域可以实现一定程度的隔离，但指令实例仍然是DOM的一部分。这意味着不仅可以引用DOM中相应的HTML元素，还可以编写CSS选择器来选择由指令HTML模板定义的DOM元素。换句话说，在指令中，你只能在数据层面实现隔离。然而，在DOM层面，你可以轻松地编写一个脚本来修改指令的内部工作机制，这最终可能导致严重的错误。

## 72 AngularJS

| DDO属性 | 有效值 | 说明 |
| :--- | :--- | :--- |
| `link` | 最多四个参数的函数 | 定义链接函数，对于每个指令实例恰好调用一次。AngularJS向该函数传递3个或4个参数，具体取决于`require`属性：<br>- `scope`。作用域<br>- `element`。HTML元素<br>- `attrs`。访问HTML属性<br>- `ctrl`。控制器（如果设置了`require`） |
| `compile` | 最多三个参数的函数 | 定义编译函数，对于每个指令（不是实例！）恰好调用一次。AngularJS向该函数传递三个参数：<br>- `tElement`。模板元素<br>- `tAttrs`。访问模板属性<br>- `transclude`。用于transclusion的链接函数 |
| `restrict` | 字符串 | 限制范围，其值可以是属性（A）、元素（E）、CSS类（C）、注释（M）或它们的组合 |
| `template` | 字符串 | 定义HTML模板 |
| `templateUrl` | 字符串 | 定义HTML模板的URL，如果模板位于单独的文件中 |
| `scope` | 布尔值或对象 | 作用域定义 |
| `replace` | 布尔值 | 指示指令标签是否会被指令模板替换 |
| `require` | 字符串 | 定义对另一个指令的控制器依赖 |
| `controller` | 函数 | 更复杂的指令可以拥有自己的控制器 |
| `transclude` | 布尔值 | 定义transclusion，如果我们在调用指令标签时允许`innerHTML`字段。与`ngTransclude`指令配合使用 |
| `terminal` | 布尔值 | 指示该指令是否在模板指令中处理 |
| `priority` | 数字 | 确定多个指令作用于同一DOM元素时的处理顺序。优先级高的指令优先于优先级低的指令处理。如果两个指令优先级相同，则处理顺序未定义。 |

表2.2：指令DDO属性概览

然而，这个弱点是有原因的。在AngularJS的初始阶段，shadow DOM、自定义元素、模板等能够实现DOM层面隔离和封装的技术，甚至还没有出现在任何W3C规范的初稿中。因此，你只能接受这个限制，并在缺乏这种隔离的情况下实现指令概念。

在撰写本书时，我们离目标更近了一步。当时已经有了W3C规范，尽管还没有任何浏览器实现。至少已经有了初稿，这样专注的开发人员就可以使用polyfill或shim。这些小型软件组件可以弥补本机不可用功能的不足，通过模拟相同的API来实现。因此，即使是新浏览器的功能，也可以在一定程度上在旧浏览器中使用。

在这一点上，Polymer项目（http://polymer-project.org）开始发挥作用。Polymer为上述W3C规范提供了polyfill，并支持使用所讨论的功能，其中一些甚至在旧版本的Internet Explorer中也能使用。Polymer更进一步，基于上述规范定义了真正自包含且可复用的组件。当然，也可以使用Polymer来开发具有这些特性的自己的组件。

因此，很明显你应该尝试在指令实现中使用Polymer方法。事实上，AngularJS的开发者已经宣布，在未来的AngularJS版本中，指令功能将基于Polymer。

#### 总结

- 模块是AngularJS中最粗粒度的结构。它作为控制器、过滤器、服务和指令的容器。此外，它可以有任意数量的`config()`和`run()`代码块。
- 使用控制器为DOM定义独立的作用域。你应该尽量保持服务精简，并将复杂逻辑外包到控制器。
- 与大多数其他JavaScript框架不同，模型层由普通的JavaScript构造组成，如对象或原始数据类型。尽管如此，该框架仍能通过使用脏检查来检测这些普通JavaScript结构的变化，从而提供双向数据绑定功能。
- 路由使AngularJS应用成为单页应用，并为我们提供深层链接。
- 视图是模板的实例，在框架处理完所需模板时在运行时生成。模板是我们应用的HTML代码。
- AngularJS中有两种类型的过滤器：集合过滤器和格式化过滤器。
- 集合过滤器与`ngRepeat`指令配合使用，用于过滤或转换底层集合。
- 格式化过滤器与表达式配合使用，用于在输出之前格式化或转换已求值的值。
- 服务是一个单例，包含应用的大部分逻辑。它可以用于各种任务，包括作为数据访问对象。
- 指令是AngularJS的核心，因此是该框架的独特功能。它们允许我们定义新的HTML元素和属性。这些元素或属性可以创建自己的模板并拥有自己的逻辑。

# 第3章 BookMonkey项目

在讨论了AngularJS的基本概念之后，我们现在想利用目前所学的知识，用AngularJS构建一个真实世界的应用程序。我们还将基于具体的用例，介绍其他让AngularJS变得出色的机制。

## 项目与流程介绍

我们要实现的项目叫做BookMonkey。这是一个小型Web应用程序，用于浏览书籍收藏、查看书籍的详细信息，以及通过标签将书籍分类。还会有一个管理区域，允许管理员管理数据库。

实现将以迭代步骤进行。这些步骤的顺序经过精心选择，以提供最高的教育价值。例如，即使在真实项目中更倾向于采用测试驱动开发方法，它也不会作为第一步。我们可能会在热门方法的诸多方面上花费过多精力，从而可能偏离框架的核心功能。因此，我们将在未来的某些步骤中再引入测试先行的方法。

为了使每个步骤的目标具体化，每次迭代都会有一个用户故事需要完成。

项目的后端系统不是本章的主题。然而，我们已经创建了一个基于Node.js的初级后端实现，你可以使用。

### 要求

要运行本项目中的示例，你需要一个现代浏览器。我们在Chrome中测试了这些示例，并推荐使用该浏览器的最新版本。然而，任何实现了ECMAScript语言标准第5版或更高版本的其他浏览器都应该能够轻松运行该项目。Google Chrome可以从此网站免费下载。

http://www.google.com/chrome/

此外，示例应该从本地Web服务器加载。为此，你可以使用Node.js的`http-server`模块。此模块可以从此网站下载。

http://npmjs.org/package/http-server

使用`http-server`，你可以从任何目录启动一个HTTP服务器。但在安装`http-server`模块之前，你需要在机器上安装最新版本的Node.js和npm。你可以从其官方网站免费下载Node.js：

http://nodejs.org/download

> **npm**
>
> npm现在是Node.js不可或缺的一部分，因此会自动随Node.js安装程序一起安装。

Node.js和npm成功安装后，你可以使用npm安装`http-server`模块。在控制台使用此命令进行安装：

```
npm install -g http-server
```

安装成功后，你可以在控制台使用此命令启动`http-server`：

```
http-server
```

默认情况下，一个轻量级HTTP服务器将在端口8080上启动。该HTTP服务器将提供服务器运行所在目录中的所有文件。

你还需要Karma来运行测试。Karma也是作为Node.js模块安装的。它的官方网站是这个。

http://karma-runner.github.io

使用以下控制台命令安装Karma。

```
npm install -g karma
```

最后，你需要安装AngularJS自带的用于端到端测试的`ngScenario`框架的Karma支持。在控制台使用此命令安装它：

```
npm install -g karma-ng-scenario
```

### 设置项目环境

在开始实际的应用程序开发之前，你首先需要设置项目环境。为此，创建一个名为`bookmonkey`的新目录。在此目录中，通过创建两个名为`app`和`test`的子目录来定义一个基本结构。这样，你就可以将稍后编写的测试与实际应用程序分开。在`app`目录中，创建一个名为`index.html`的HTML文件。当用户未在地址栏中指定特定文件时，大多数Web服务器会将此文件作为默认页面提供。因此，它作为应用程序的入口点。此文件的内容如清单3.1所示。

**清单3.1：我们应用程序的初始index.html**

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>BookMonkey</title>
</head>
<body>
  <h1>Hello BookMonkey</h1>
</body>
</html>
```

# 78 AngularJS

现在，切换到`app`目录，并使用这个熟悉的命令启动上述HTTP服务器：

```
http-server
```

该命令应返回成功消息，并告知你服务器启动的端口号。

```
Starting up http-server, serving ./ on: 8080
Hit CTRL-C to stop the server
```

此语句简单说明你可以通过按CTRL+C来停止服务器。当然，你现在需要让它保持运行。

你现在可以浏览到此URL以获取当前的静态HTML页面：

```
http://localhost:8080
```

![](img/7a003218cea01579a50512a6c0e40f28_85_0.png)

如果你在浏览器中看到类似图3.1所示的内容，说明你已成功完成此步骤，可以继续进行AngularJS集成了。

在下一步中，我们想在项目中集成AngularJS。在这个项目中，我们使用AngularJS版本1.2.10。可以从其官方网站下载该库。

```
http://code.angularjs.org/1.2.10/angular.js
```

项目中，该文件存储在路径`app/lib/angular/angular.js`下。为此，你需要在`app`目录下创建一个`lib`目录。`lib`目录本身又有一个名为`angular`的子目录。顺便说一下，你还应该从http://code.angularjs.org/1.2.10/angular-route.js下载`ngRoute`模块，并将文件保存为`app/lib/angular-route/angular-route.js`。你将需要此模块来使用AngularJS的路由功能。

> ### AngularJS 1.3与Internet Explorer 8
>
> 在即将到来的1.3版本中，AngularJS将终止对Internet Explorer 8（IE8）的支持。做出这个决定是为了让框架能够快速下载新扩展，而不会因IE8带来大量额外的工作。

接下来，你需要在`index.html`页面中使用`<script>`标签引入该框架。你应该将此标签添加到`<body>`标签的末尾。紧接着应该是包含`ngRoute`模块（`angular-route.js`）的`<script>`标签。为了快速检查AngularJS是否正确挂载，我们将`index.html`页面扩展为一个简单的双向数据绑定。为此，我们必须告诉AngularJS我们想在哪个DOM部分创建一个AngularJS应用程序。我们知道必须使用`ngApp`指令，并且通过在`<html>`标签上添加`ng-app`属性，我们为整个DOM定义了它。这样，我们告诉AngularJS应该考虑并评估整个范围作为一个AngularJS应用程序。最后，我们构建一个简单的双向数据绑定示例，以确保我们的AngularJS已正确挂载。

**清单3.2：我们的应用程序现在需要AngularJS**

```
<!DOCTYPE html>
<html ng-app>
<head>
    <meta charset="utf-8">
    <title>BookMonkey</title>
</head>
<body ng-init="name='BookMonkey'">
    <h1>Hello {{ name }}</h1>
    <input type="text" ng-model="name" />
    <!-- Scripts -->
    <script src="lib/angular/angular.js"></script>
    <script src="lib/angular-route/angular-route.js"></script>
</body>
</html>
```



这里我们创建了一个新的文本字段，并使用`ngModel`指令将其绑定到作用域变量`name`。我们还将标题替换为表达式`Hello {{name}}`，并为`ngInit`指令提供了作用域变量`name`的初始值。我们的`index.html`页面现在应该看起来像清单3.2那样。

![](img/7a003218cea01579a50512a6c0e40f28_87_0.png)

如果你重新加载浏览器窗口，页面应该看起来像图3.2所示。它已经支持交互了。如果你更改我们框中的文本，标题中的文本也会立即更新。双向数据绑定工作了。这意味着你已成功将AngularJS集成到我们的项目中。

> ### 使用下载的项目
>
> 或者，你可以使用从出版商网站下载的随附项目。在这种情况下，请切换到`ch03_01_project_init/app`目录并从那里启动`http-server`。

为什么在这里使用自动更新？并且，这里到底发生了什么？因为我们在`<html>`上使用了`ngApp`指令进行注解，AngularJS将评估此DOM部分内的所有指令和表达式。在实践中，这意味着整个DOM都会被评估。通过在消息中使用`ngInit`指令……

`<h1>`标签中的表达式`Hello {{name}}`会触发AngularJS使用此区域的作用域。实际上，框架会检查作用域变量`name`是否在`$rootScope`中定义，如果已定义，则显示其值。此外，每次作用域变量`name`的值发生变化时，该表达式都会重新求值。

通过在`<input>`标签中使用`ngModel`指令，我们在作用域变量`name`上建立了双向数据绑定。因此，对该作用域变量名称的任何更改都会反映在`<input>`字段中。反之亦然。如果输入字段发生变化，作用域变量`name`也会自动更新。

#### 项目启动：图书详情视图

既然我们已经为项目奠定了基础并成功集成了AngularJS，我们现在需要着手处理BookMonkey项目。为此，我们引入了框架的更多概念和机制来解决相关问题。那么，让我们看看我们的第一个任务，我们以用户故事的形式来定义它：

> 作为用户Michael，我想要获取一本图书的详细信息，以便更多地了解这本书。

这个故事的核心方面是显示特定图书的详细信息。为此，我们应该首先制作视图的线框图（参见图3.3）。

基于这个线框图，我们尝试推导出一个能直接导向JSON结构的数据模型。我们选择了清单3.3中的数据模型。

82 AngularJS

![](img/7a003218cea01579a50512a6c0e40f28_89_0.png)

图3.3：详情视图的线框图

##### 清单3.3：以JSON格式表示的图书详情视图的数据模型

```json
{
  "title": "JavaScript for Enterprise Developers",
  "subtitle": "Professional Programming in the Browser"
               + "and on the Server",
  "isbn": "978-3-89864-728-1",
  "abstract": "JavaScript is no longer only interesting to"
               + " classic web programmers.",
  "numPages": 302,
  "author": "Oliver Ochs",
  "publisher": {
    "name": "dpunkt.verlag",
    "url": "http://dpunkt.de/"
  }
}
```

### 使用下载的项目

要测试本节的代码，您可以使用从出版商网站下载的随附项目。为此，请将目录更改为`ch03_02_details_view/app`并从那里启动`http-server`。

##### 使用表达式的详情视图模板

我们继续创建此视图的模板。为此，我们在`app`目录中创建一个名为`templates`的新目录来存放我们的模板。在这个新目录中，我们创建一个名为`book_details.html`的HTML文件。此文件将包含模板的定义。

###### 清单3.4：图书详情视图的模板

```html
<h2>{{ book.title }}</h2>

<h3>{{ book.subtitle }}</h3>

<p>
  <ul>
    <li>ISBN: {{ book.isbn }}</li>
    <li>Number of Pages: {{ book.numPages }}</li>
    <li>Author: {{ book.author }}</li>
    <li>
      Publisher:
      <a ng-href="{{ book.publisher.url }}" target="_blank">
        {{ book.publisher.name }}
      </a>
    </li>
  </ul>
</p>

<hr>

<p>
  {{ book.abstract }}
</p>
```

清单3.4显示了图书详情视图模板的HTML代码。我们使用表达式`{{book.title}}`、`{{book.subtitle}}`等来显示相关的会计信息。为了使这些表达式成功求值，作用域变量`book`必须位于对该视图有效的作用域中，并且`book`必须指向一个包含相应属性（`title`、`subtitle`等）的对象。我们将使用控制器来定义此视图的作用域。但是，首先让我们再看一下清单3.4中模板的另一个特性。

> **国际化**
>
> 在此处使用的示例中，我们并未涉及国际化。然而，有一些AngularJS模块可以处理它。最著名且使用最广泛的模块是Pascal Precht的`ng-translate`。它可以轻松适应现有的服务结构，拥有广泛的文档，并且仍在积极开发中。您可以从`http://pascalprecht.github.io/angular-translate`下载此模块。

##### 使用`ngBind`和`ngBindTemplate`的模板

考虑清单3.5中的HTML模板。

###### 清单3.5：使用`ngBind`显示图书信息

```html
<h2 ng-bind="book.title"></h2>

<h3 ng-bind="book.subtitle"></h3>

<p>
  <ul>
    <li ng-bind-template="ISBN: {{ book.isbn }}"></li>
    <li ng-bind-template="Number of Pages:
    {{ book.numPages }}"></li>
    <li ng-bind-template="Author: {{ book.author }}"></li>
    <li>
      Publisher:
      <a ng-bind="book.publisher.name"
         ng-href="{{ book.publisher.url }}"
         target="_blank">
      </a>
    </li>
  </ul>
</p>

<hr>

<p ng-bind="book.abstract">
</p>
```

在清单3.5中，我们基本上用特殊的`ng-bind`属性替换了表达式。定义`ng-bind`属性的`ngBind`指令也是框架标准配置的一部分。从技术上讲，该指令将作为属性值指定的作用域变量的值绑定到注解的HTML元素上。最后，使用此指令产生的输出与使用等效表达式相同。然而，与表达式相比，`ngBind`指令有两个决定性的优势：

1. 在AngularJS完成对表达式的求值之前，表达式在视图上可见。使用`ngBind`时则不会发生这种情况。
2. 当从表达式生成输出时，如果相应变量作用域的值发生变化，AngularJS总是创建一个新的DOM元素来替换包含旧值的旧DOM元素。如果您改用`ngBind`指令生成输出，框架将不会创建新的DOM元素，而是用作用域变量的新值更新现有DOM元素的文本内容。与表达式相比，`ngBind`具有性能优势，并且通常在我们的应用程序中消耗更少的内存。

此外，清单3.5中的模板还使用了一个与`ngBind`相关的指令，即`ngBindTemplate`指令。顾名思义，您可以使用它来定义HTML元素的文本内容模板。当我们想要生成将静态字符串与变量作用域的值组合在一起的输出时，`ngBindTemplate`指令非常有用。此外，`ngBindTemplate`还可以生成混合多个作用域变量值的输出，因为我们可以使用此指令指定多个表达式。`ngBindTemplate`指令与`ngBind`相对于简单表达式具有相同的优势。

##### 定义应用模块

在优化模板之后，我们现在想要实现为该视图提供作用域并在`book`变量的作用域中包含相应`Book`对象的控制器。此外，我们还想创建我们的第一个路由。为此，我们需要扩展我们的项目结构和`index.html`文件。我们`index.html`文件的新版本如清单3.6所示。

###### 清单3.6：`index.html`的高级版本

```html
<!DOCTYPE html>
<html ng-app="bmApp">
<head>
  <meta charset="utf-8">
  <title>BookMonkey</title>
</head>
<body>
  <header>
    <h1>BookMonkey</h1>
  </header>

  <div ng-view>
  </div>

  <!-- Scripts -->
  <script src="lib/angular/angular.js"></script>
  <script src="lib/angular-route/angular-route.js"></script>
  <script src="scripts/app.js"></script>
  <script src="scripts/controllers/book_details.js"></script>
</body>
</html>
```

清单3.6显示了一个使用`ngApp`指令指定的模块，当DOM加载完成后，AngularJS应自动加载该模块。一旦浏览器加载了DOM，就应启动`bmApp`模块。此时我们已经可以预见，我们的BookMonkey应用程序将只有一个模块。因此，我们将在此模块内定义和实现所有应用程序组件。

###### 第一个路由

查看清单3.6中的`<script>`标签，我们意识到还需要两个JavaScript文件：`app.js`和`book_details.js`。`app.js`文件将包含我们的`bmApp`模块的定义和路由定义。在`book_details.js`文件中，我们将实现`BookDetailsCtrl`控制器，该控制器为图书详情视图提供数据和功能。为此，我们首先在`app`目录下创建一个名为`scripts`的目录。在这个新目录中，我们将存储BookMonkey应用程序的所有JavaScript源代码。接下来，我们在`scripts`目录中创建一个名为`app.js`的文件。在`scripts`目录下，我们还创建一个名为`controllers`的目录，在其中创建`book_details.js`文件。同时，我们还将实现另一个控制器并存储在`controllers`目录中。除了`controllers`目录之外，在接下来的步骤中，我们还将为指令、服务和过滤器在`scripts`目录中创建更多目录。

**清单3.7：`app.js`中`bmApp`模块的定义和第一条路由**

```javascript
var bmApp = angular.module('bmApp', ['ngRoute']);

bmApp.config(function ($routeProvider) {
  $routeProvider.when('/books/:isbn', {
    templateUrl: 'templates/book_details.html',
    controller: 'BookDetailsCtrl'
  });
});
```

清单3.7展示了`app.js`的源代码。在第一行中，我们使用AngularJS的`module()`函数定义了`bmApp`模块。重要的是模块名称作为第一个参数传递。模块名称与`index.html`文件中用于`ngApp`指令的名称相对应。第二个参数是一个数组，我们的`bmApp`模块将依赖于其他AngularJS模块。因为我们希望在BookMonkey应用程序中使用路由，所以此时需要引入`ngRoute`模块。这个模块可用，是因为我们在`index.html`文件中已经包含了`angular-route.js`文件（参见清单3.6）。

此外，我们在`config()`块中使用`$routeProvider`来配置我们的第一条路由。回想一下，我们可以使用依赖注入来注入服务提供者在应用程序的配置阶段配置`config()`块。这意味着我们可以使用`$routeProvider`来配置`$route`服务的路由。如上一章所述，路由是模板上的URL映射。可选地，如我们的示例所示，我们还可以指定一个控制器。`$route`服务在运行时评估哪条路由是活动的，它与我们在`index.html`文件中使用`<div>`容器标注的`ngView`指令密切协作（参见清单3.6）。根据当前URL，配置的模板将被加载到该`<div>`元素的`innerHTML`属性中。此外，如果为某条路由配置了控制器，将为模板创建一个新的作用域，并调用控制器的构造函数。这种关系如图3.4所示。

88 AngularJS

![](img/7a003218cea01579a50512a6c0e40f28_95_0.png)

图3.4：`ngView`指令与`$routeProvider`之间的关系

查看映射到图书详细视图的`/books/:isbn`路由，还有一个小特性。您可以用冒号指定路径参数。在此路由中，`isbn`是一个路径参数。这意味着URL的这部分可以是变量，但仍将映射到配置的模板和控制器。在图书详细信息的后续开发阶段，我们可以使用`isbn`路径参数来访问相应的图书。在`BookDetailsCtrl`控制器内部，通过所谓的`$routeParams`服务可以实现访问。

##### 使用`BookDetailsCtrl`控制器创建独立的作用域

在清单3.8中`BookDetailsCtrl`的基本实现里，我们暂时还不关心ISBN。相反，我们希望将一个`Book`对象赋值给作用域变量`book`，以便制作出详细视图的第一个可用版本。回想一下，DOM元素的控制器定义了它自己的作用域。`BookDetailsCtrl`控制器也是如此。在模板的DOM部分（`book_details.html`）中，AngularJS在每次调用路由时都会创建一个新的作用域。在这个作用域中，我们可以访问控制器的构造函数内部部分。在作用域中，我们最终用包含模板中通过`ngBind`或`ngBindTemplate`指令指定的所有属性的`Book`对象来设置`book`变量。

##### 清单3.8：`BookDetailsCtrl`的实现

```javascript
bmApp.controller('BookDetailsCtrl', function ($scope) {
  $scope.book = {
    title: 'JavaScript for Enterprise Developers',
    subtitle:
      'Professional Programming in the Browser'
      + ' and on the Server',
    isbn: '978-3-89864-728-1',
    abstract: 'JavaScript is no longer only'
      + ' interesting to classic web programmers',
    numPages: 302,
    author: 'Oliver Ochs',
    publisher: {
      name: 'dpunkt.verlag',
      url: 'http://dpunkt.de/'
    }
  };
});
```

现在，如果您在浏览器中输入匹配已定义路由的URL，您应该能看到如图3.5所示的详细视图的初版。一个可能的URL是：

```text
http://localhost:8080/#/books/123
```



当然，您也可以传递除`123`以外的值作为路径参数。由于我们在创建详细视图时还未处理`isbn`路径参数，因此始终渲染相同的详细视图。

#### 首先，测试

如前所述，采用测试驱动开发的方法非常重要。从这个角度来看，我们已经犯了一个错误，因为我们没有在实现之前先编写测试。因此我们想在此时编写第一个简单的测试，以证明在模板中使用`ngBind`或`ngBindTemplate`指令将产生与表达式相同的结果。

![](img/7a003218cea01579a50512a6c0e40f28_97_0.png)

##### 图 3.5：图书详细视图

我们在 BookMonkey 主目录中有一个名为`test`的目录用于存放将要编写的测试。现在在`test`目录中，我们将创建两个名为`unit`和`e2e`的子目录。在`unit`目录中，我们将存储单元测试，而在`e2e`目录中，我们将进行 E2E 测试。

总之，您使用单元测试来测试与应用程序其余部分隔离的小型应用程序单元。此类火炉此类单元的示例包括控制器、服务、指令和过滤器。在单元测试中，您运行部分逻辑，然后检查执行结果是否符合预期。为了编写真正的隔离测试，应用程序单元的依赖通常会被模拟。这意味着您用模拟对象替换依赖的实际实现。模拟对象是一个具有为被测应用程序单元提供的相同公共 API 的对象。模拟对象不是实际实现，而是提供返回某些硬编码值的实现。基于这些硬编码值，您可以确定依赖在测试用例中应该如何表现。AngularJS 自带自己的模拟实现，可以在进行测试时为您节省大量工作。

然而，在 E2E 测试中，您应该将应用程序视为黑盒。您无法访问 JavaScript 代码的内部状态，因此无法基于这个条件来制定预期。相反，您只能制定与 DOM 状态相关的预期。

使用领域特定语言（DSL），您可以控制潜在用户应该如何行为。这样，您可以将应用程序置于特定状态，然后检查 DOM 以确定应用程序是否正常运行。

此时，我们想要通过 E2E 测试来检查图书详细视图的模板。为此，我们需要再次扩展模板，使其能够轻松引用我们想要在测试中检查其内容的相应 DOM 节点。

**清单 3.9：扩展模板以包含 CSS 类**

```html
<h2 ng-bind="book.title" class="bm-book-title"></h2>

<h3 ng-bind="book.subtitle" class="bm-book-subtitle"></h3>

<p>
  <ul>
    <li ng-bind-template="ISBN: {{ book.isbn }}"
        class="bm-book-isbn"></li>

    <li ng-bind-template="Number of Pages:{{ book.numPages }}"
        class="bm-book-num-pages"></li>

    <li ng-bind-template="Author: {{ book.author }}"
        class="bm-book-author"></li>

    <li>
      Publisher: <a ng-bind="book.publisher.name"
                   ng-href="{{ book.publisher.url }}"
                   target="_blank"
                   class="bm-book-publisher-name">
      </a>
    </li>
  </ul>
</p>

<hr>

<p ng-bind="book.abstract" class="bm-book-abstract"></p>
```

清单 3.9 展示了扩展后模板的标记。如您所见，包含相关图书信息的 HTML 元素补充了 CSS 类（如`bm-book-title`）。这使得我们可以制定简短的 CSS 选择器来引用这些 HTML 元素，并在 E2E 测试中检查其内容。

## 92 AngularJS

在编写实际的 E2E 测试之前，我们需要在`e2e`目录中创建一个名为`templates`的子目录。我们还需要在`templates`中创建一个`book_details.spec.js`文件，并在该文件中定义书籍详情的 E2E 测试。

> **测试的文件名与结构**
>
> 通常所有测试文件都使用`.spec.js`扩展名。此外，测试目录的结构应与`app`目录中应用程序的结构相似。

##### 清单 3.10：模板的 E2E 测试

```javascript
describe('E2E: book details view', function(){

    beforeEach(function() {
        browser().navigateTo('/');
    });

    it("should show the correct book details",function(){

        browser().navigateTo('#/books/978-3-89864-728-1');

        expect(element('.bm-book-title').html()).toBe('JavaScript for Enterprise Developers');

        expect(element('.bm-book-subtitle').html()).toBe('Professional Programming in the Browser' + ' and on the Server');

        expect(element('.bm-book-isbn').html()).toBe('ISBN: 978-3-89864-728-1');

        expect(element('.bm-book-num-pages').html()).toBe('Number of Pages: 302');

        expect(element('.bm-book-abstract').html()).toBe('JavaScript is no longer only interesting to classic web programmers.');
    });

});
```

清单 3.10 展示了书籍详情的 E2E 测试（参见`book_details.spec.js`），该测试检查作用域中的数据是否正确返回。如果你熟悉 Jasmine 测试框架（http://pivotal.github.io/jasmine），你可能会立即看出其中的相似之处。事实上，AngularJS 用于 E2E 测试的`ngScenario`就是基于 Jasmine 设计的。

#### Protractor 框架

Protractor 项目可以从`http://github.com/angular/protractor`下载，它是一个用于定义 E2E 测试的框架。它与`ngScenario`类似，但基于 WebDriver 规范，可以对浏览器进行更多的控制。AngularJS 官方文档提到，Protractor 将来会取代 AngularJS 的 E2E 环境。测试环境的配置和 API 的某些部分存在差异。然而，此处描述的 E2E 测试定义概念可以类似地应用，并且是普遍适用的。

基本上，E2E 测试的构建方式与单元测试相同。首先使用一个`describe()`函数来定义测试套件。该函数的第一个参数是测试套件的名称。第二个参数包含一个匿名函数，在其中定义测试用例。使用`it()`函数定义的单个测试用例，其第一个参数期望是一个用自然语言表达预期行为的字符串。第二个参数是一个匿名函数，测试用例在其中定义。这种测试用例的特点是先创建一个条件，然后执行被测试的功能，最后以一个或多个`expect()`函数来表述预期的后置条件。如果多个测试用例需要相同的条件，或者你想在每个测试用例之前执行某些逻辑，那么可以使用`beforeEach()`函数。该函数期望一个参数，即一个将在每个测试用例之前执行的函数。

在清单 3.10 的 E2E 测试套件中，我们使用`beforeEach()`函数在每个测试用例之前导航到应用程序的首页。具体的调用如下所示。

```javascript
browser().navigateTo('/')
```

在当前开发阶段，这是我们可能对测试套件中所有测试用例相关的唯一条件。由于我们只定义了一个测试用例，我们可以将这个前置条件直接编码到测试用例中。然而，将来我们可能会添加更多需要这个条件的测试用例。着眼于未来，我们因此将其放入`beforeEach()`函数中。

在我们的单个测试用例中，我们导航到与之前手动在浏览器中打开的相同 URL。不过，这次我们添加了一个带有真实 ISBN 的路径参数，为未来的开发准备这个测试用例。最终，我们将使用它来显示相应书籍的详情。

```javascript
browser().navigateTo('#/books/978-3-89864-728-1')
```

在内部，我们的应用程序现在应该根据`BookDetailsCtrl`控制器的路由配置和详情视图的模板（`templates/book_details.html`）加载。然后，书籍信息应该在 DOM 中可用。随后，我们可以开始使用`expect()`函数来表述我们的后置条件。由于我们在模板中为适当的 HTML 元素提供了有意义的 CSS 类，我们现在可以使用`element()`函数结合适当的 CSS 选择器（例如`bm-book-title`）来引用必要的 DOM 元素。接下来是调用匹配器。在`ngScenario`中，匹配器与 Jasmine 中的语义相同。有像`toBe()`匹配器这样的基本匹配器，它只比较两个对象的类型。更复杂的匹配器包括`ngScenario`提供的`toContain()`匹配器。该匹配器检查一个字符串是否是另一个字符串的一部分。你也可以使用`toContain()`来确保某个元素包含在数组中。匹配器的完整列表和`ngScenario`完整 API 的描述可以在`http://docs.angularjs.org/guide/dev_guide2e-testing`找到。

我们现在已经定义了我们的第一个测试套件。要执行 E2E 测试套件，我们现在需要一个运行时环境。在 AngularJS 领域中，Karma 已经确立了自己作为测试执行环境的地位，因为该项目实际上始于 AngularJS 开发人员自己寻找适合 AngularJS 的工具之时。你在本章开头已经安装了 Karma，现在可以将其用作单元测试和 E2E 测试的运行时环境。

> **Karma**
>
> 最流行的测试执行环境可能是 Testacular，它在成为 AngularJS 框架的官方测试环境后更名为 Karma。

要运行清单 3.10 中的测试套件，你需要 Karma 的配置文件。此时，不要担心 Karma 提供了哪些配置选项。这个方面将在第 5 章“项目管理与自动化”中讨论。如果你按照描述完全创建了项目结构，你可以轻松使用随附 zip 文件中的配置文件。为此，将`karma-e2e.conf.js`文件复制到`bookmonkey`目录中。而且，既然你要做这件事，也可以同时将`karma.conf.js`文件复制过去。`karma.conf.js`文件是单元测试的配置。

> **执行 E2E 测试**
>
> 根据我们对 E2E 测试的配置（`karma-e2e.conf.js`），Karma 假设 BookMonkey 应用程序可以在`http://localhost:8080`访问。这意味着在 Karma 执行测试之前，`http-server`必须在 8080 端口运行。Karma 将从该 URL 加载应用程序并执行 E2E 测试。

```bash
karma start karma-e2e.conf.js
```

如果你没有出错，Karma 应该会给你一个测试用例成功执行的反馈。

```text
Chrome 30.0.1599: Executed 1 of 1 SUCCESS (0.908 secs / 0.699 secs)
```

这个 E2E 测试的目的是展示`ngBind`或`ngBindTemplate`指令可以返回与使用简单表达式的模板相同的输出。

为了验证这一说法，你可以创建另一个使用表达式的书籍详情视图模板。但是，不要忘记用相应的 CSS 类来装饰 HTML 元素。否则，你的 E2E 测试中的 CSS 选择器将不再工作。新模板可以在清单 3.11 中看到。

##### 清单 3.11：用于测试的使用表达式的模板

```html
<h2 class="bm-book-title">{{ book.title }}</h2>

<h3 class="bm-book-subtitle">{{ book.subtitle }}</h3>

<p>
<ul>
    <li class="bm-book-isbn">ISBN: {{ book.isbn }}</li>

    <li class="bm-book-num-pages">Number of Pages: {{ book.numPages }}</li>

    <li class="bm-book-author">Author: {{ book.author }}</li>

    <li>
        Publisher:
        <a ng-href="{{ book.publisher.url }}" target="_blank" class="bm-book-publisher-name">
            {{ book.publisher.name }}
        </a>
    </li>
</ul>
</p>

<hr>

<p class="bm-book-abstract">{{ book.abstract }}</p>
```

如果你再次运行 E2E 测试，你会看到使用简单表达式时相同的输出。

#### 总结

- 表达式用于为模板返回值。
- 表达式可以用来输出作用域中变量的当前值，这些值在当前状态下对模板有效。
- 表达式受双向数据绑定约束。这意味着当作用域变量的值发生变化时，它们将被重新评估。
- 如果可能的话，出于性能考虑，你应该选择`ngBind`或`ngBindTemplate`指令而非表达式。
- 你可以使用`ngHref`指令来创建包含表达式的超链接。AngularJS 会确保只有在模板处理完毕且相应表达式求值完成后，链接才会变为可用状态。
- 使用`$routeProvider`，你可以在`config()`代码块中配置应用程序路由。
- `ngView`指令用于标注一个 HTML 元素，以告知框架应该加载哪个路由模板。
- 你可以使用 E2E 测试来编写模拟用户行为的脚本，并基于 DOM 提出特定的期望。
- Angular 自带了名为`ngScenario`的测试框架。

#### 列表视图

成功创建了基本的详情视图之后，我们现在来处理列表视图。该视图将显示一个书籍列表，用户可以从中选择以在详情视图中查看。你可以将列表视图用于多种用途。例如，你可以显示搜索结果（见图 3.6）。另外，列表视图也可以在管理区域中使用，以方便管理员管理。

![](img/7a003218cea01579a50512a6c0e40f28_104_0.png)

**图 3.6：所设计的列表视图**

98 AngularJS

本节的核心内容是`ngRepeat`指令。你可以使用此指令在模板中渲染类似数组的列表结构。`ngRepeat`指令提供了一系列用于筛选或排列输出内容的功能。

我们还为列表视图编写了一个用户故事。

> 作为用户 Michael，我希望能够查看一个书籍列表，以便获得概览。

**使用下载的项目**

要测试本节中的代码，你可以使用从出版商网站下载的配套项目。为此，请切换到`ch03_03_list_view/app`目录，并从那里启动`http-server`。

##### 首先，编写测试

我们提到过想要继续采用测试优先的方法。在本节中，我们首先通过创建`book_list.spec.js`文件并定义一个 E2E 测试套件来检查列表视图的测试。该文件位于`test/e2e/templates/`目录中。

**清单 3.12：准备 E2E 测试以验证列表视图**

```javascript
describe("E2E: book list view", function () {

    // Define the array of books in the expected order.

    // Sorted by title.

    var expectedBooks = [

        {

            title: 'CoffeeScript',

            isbn: '978-3-86490-050-1',

            author: 'Andreas Schubert'

        },

        {

            title: 'JavaScript for Enterprise Developers',

            isbn: '978-3-89864-728-1',

            author: 'Oliver Ochs'

        },

        {

            title: 'Node.js & Co.',

            isbn: '978-3-89864-829-5',

            author: 'Golo Roden'

        }

    ];
```



// Derive an array that only contains titles

// for easier expectation checks.

```javascript
var orderedTitles = expectedBooks.map(function(book) {
    return book.title;
});
```

清单 3.12 展示了测试套件的基本结构。在编写实际测试用例之前，我们定义了一些辅助构造以简化测试用例的实现。此时相关的辅助构造是`expectedBooks`书籍数组。在该数组中，我们定义了希望在列表视图中看到的书籍条目，即一个具有`title`、`isbn`和`author`属性的对象。特别地，在此定义中重要的是`Book`对象应按预期顺序排列，这样我们就可以在测试用例中轻松检查列表视图是否已正确排序条目。在此我们选择了按书名字母顺序进行定义。

此外，我们使用`map()`函数从`expectedBooks`数组派生出一个名为`orderedTitles`的第二个数组，其中我们只按相同顺序存储书名。`orderedTitles`数组是后续测试用例的辅助构造。

###### 清单 3.13：E2E 测试套件的 `beforeEach()` 代码块，用于验证列表视图

```javascript
describe("E2E: book list view", function () {
    [...]

    beforeEach(function () {
        browser().navigateTo('#/books');
        browser().reload();
    });

    [...]
});
```

清单 3.13 展示了我们在清单 3.12 中测试套件的延续。与书籍详情的 E2E 测试一样，这里我们使用`beforeEach()`代码块来生成测试的前提条件。在此情况下，我们告诉 Karma 在每次测试用例之前导航到`/books`路由并重新加载文档。重新加载是必要的，因为在某些未来的测试用例中我们将更改视图状态。因此，我们确保在每次测试用例执行之前，视图处于其原始状态。仅仅导航到`/books`路由在这里是不够的，因为当我们导航到相同 URL 之间时，通常不会重新生成初始状态。

###### 清单 3.14：验证正确书籍数量的测试用例

```javascript
describe("E2E: book list view", function () {
    [...]

    var selector = 'table.bm-book-list tr';

    it('should show the correct number of books', function () {
        expect(repeater(selector).count()).toEqual(
            expectedBooks.length
        );
    });

    [...]
});
```

我们在清单 3.14 中继续。由于我们在多个测试用例中需要该 CSS 选择器，因此将其存储在一个名为`selector`的变量中。

我们现在使用`it()`函数和`repeater`来编写第一个测试用例，以测试列表视图是否具有与`expectedBooks`数组中`Book`对象数量相同的条目。`repeater`是`ngScenario`提供的一种构造，用于方便地从表格化的类 DOM 结构（其中大多数使用`ngRepeat`指令生成）中检索信息。此类表格化 DOM 结构的示例包括 HTML 表格。这种结构的特点是重复特定的 DOM 模式若干次。HTML 表格因此是这种结构的完美示例，因为每一行（`<tr>`）通常具有相同数量的列（`<td>`），从而具有一致的结构。

基于我们作为参数传递给`repeater`的 CSS 选择器，我们隐含地确定了列表视图应基于 HTML 表格。这样，我们可以使用`repeater`来确定列表视图中包含多少条目。`repeater`上与此相关的函数是`count()`。因此，我们现在可以表述该测试的期望。

接下来是下一个测试，该测试检查列表视图中的条目是否按书名降序正确排序。

###### 清单 3.15：验证正确顺序的测试用例

```javascript
describe("E2E: book list view", function () {
    [
        it('should show the books in the proper order', function () {
            // Are they in the expected order
            // (ascending sorted by title)?
            expect(repeater(selector).column('book.title')).toEqual(
                orderedTitles
            );
        }),
        ...
    ]);
});
```

相应的测试用例如清单 3.15 所示。同样，我们使用`repeater`从 DOM 读取信息。然而，这次我们使用`repeater`的`column()`函数，从中可以再次看出`repeater`实际上是与`ngRepeat`指令配套的测试构造。`column()`函数接受一个数据绑定表达式作为参数，这正是我们在与`ngBind`指令结合使用时用于生成模板输出的片段。此时我们确定该表达式应读取`book.title`。之后，在实现中我们将必须使用以下表达式来生成输出：

```html
ng-bind="book.title"
```

使用`column()`函数，我们可以轻松读取包含书名的表格列的值。该函数返回一个包含所有行相应列值的数组。因此，我们可以使用`toEqual()`匹配器来比较返回的数组是否与我们的`orderedTitles`数组相符。如果该期望得到满足，则意味着列表条目符合我们手动在`expectedBooks`数组中指定的顺序，因为`orderedTitles`数组是从`expectedBooks`数组派生而来的。

> **`toEqual` 匹配器**
>
> `toEqual()`匹配器基于 AngularJS 的`angular.equals()`函数执行比较。该函数使用更复杂的算法来检查两个对象的相等性。除其他功能外，它还会检查两个数组中的各个元素是否匹配。使用该匹配器和`repeater`，我们可以轻松编写相对复杂的期望。

在继续实际实现列表视图之前，我们还缺少最后一个测试用例，该用例验证在书名之后是否正确返回了作者和 ISBN。该测试用例可在清单 3.16 中找到。

##### 清单 3.16：验证正确列表内容的测试用例

```javascript
describe("E2E: book list view", function () {
    [...]

    it('should show the correct book information', function () {
        // Do the other book details (isbn, author) match?
        for (var i = 0, n = expectedBooks.length; i < n; i++) {
            expect(repeater(selector).row(i)).toEqual([
                expectedBooks[i].title,
                expectedBooks[i].author,
                expectedBooks[i].isbn
            ]);
        }
    });
});
```

此测试用例的特殊之处在于，我们使用了`repeater`的一个新特性，即`row()`函数。顾名思义，该函数接受一个表格行索引作为参数，并返回包含该行中各列值的数组。因此，我们可以很容易地使用`for`循环来表达预期：每一行中的书名、作者和 ISBN 必须始终与`expectedBooks`数组中的相应定义等价。至此，我们已定义了列表视图上的最后一条预期。因此，我们现在可以按预期创建实现。在此之前，我们应该再次运行 E2E 测试，确保刚刚创建的测试套件中的测试失败，因为目前尚无实现。

```bash
karma start karma-e2e.conf.js
```

相应的负面反馈应如下所示。

```text
Chrome 30.0.1599: Executed 4 of 4 (3 FAILED)
                                     (1.217 secs / 0.971 secs)
```

我们的 Details 视图 E2E 测试仍然是“绿色”的，而我们刚刚定义的三个测试失败了。在输出中，我们还可以找出哪些测试失败了。

#### 列表视图的基础架构

定义完列表视图的 E2E 测试后，在开始实际实现之前，我们需要先创建基础架构。这意味着我们必须创建适当的文件，并在`app.js`文件中配置额外的路由。我们将从路由开始。为此，我们需要将`app.js`文件扩展为清单 3.17 中的内容。

##### 清单 3.17：列表视图的新路由

```javascript
var bmApp = angular.module('bmApp', ['ngRoute']);

bmApp.config(function ($routeProvider) {
    $routeProvider.when('/books/:isbn', {
        templateUrl: 'templates/book_details.html',
        controller: 'BookDetailsCtrl'
    })
    .when('/books', {
        templateUrl: 'templates/book_list.html',
        controller: 'BookListCtrl'
    });
});
```

我们使用`when`函数配置了另一条路由，以便将所有对`/books`的调用定向到列表视图，该视图当然有其自己的模板（`book_list.html`）和控制器（`BookListCtrl`）。因此，我们需要创建这两个文件，并使用`<script>`标签将它们包含在`index.html`文件中。我们将在`app/templates/`目录下创建`book_list.html`文件，在`app/scripts/controllers/`目录下的`book_list.js`文件中创建`BookListCtrl`控制器。

##### `BookListCtrl` 控制器

`BookListCtrl`控制器的实现类似于`BookDetailsCtrl`控制器的实现（见清单 3.18）。

##### 清单 3.18：`BookListCtrl` 控制器

```javascript
bmApp.controller('BookListCtrl', function ($scope) {
    $scope.books = [
        {
            title: 'JavaScript for Enterprise Developers',
            isbn: '978-3-89864-728-1',
            author: 'Oliver Ochs',
            [...]
        },
        {
            title: 'Node.js & Co.',
            isbn: '978-3-89864-829-5',
            author: 'Golo Roden',
            [...]
        },
        {
            title: 'CoffeeScript',
            isbn: '978-3-86490-050-1',
            author: 'Andreas Schubert',
            [...]
        }
    ];
});
```

我们用`Book`对象数组填充`books`作用域变量。在下一步从服务器加载这些信息之前，目前我们先满足于静态定义。还应注意，为了清晰起见，我们在清单 3.18 中省略了与当前讨论无关的图书信息。

#### `ngRepeat` 指令：在模板中显示数组

要在模板中显示来自类列表结构（如数组）的输出，我们必须使用`ngRepeat`指令。除了显示输出外，这个 AngularJS 指令还可以过滤、转换和分配列表。这些方面你将在接下来的章节中逐一学习。

为此，我们首先实现模板的最简版本，以确保至少有从数组返回的三本书。该版本的模板如清单 3.19 所示。

##### 清单 3.19：列表视图的模板，使用 `ngRepeat` 指令

```html
<table class="bm-book-list">
  <tbody>
    <tr ng-repeat="book in books">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```

正如 E2E 测试中所规定的，我们将列表视图扩展为 HTML 表格（`<table>`）形式。我们还用`bm-book-list` CSS 类标注了这个表格。现在到了关于`ngRepeat`指令的有趣部分。如清单 3.19 所示，我们将`ngRepeat`指令用作将被重复生成的 HTML 元素的属性，作为`books`数组的输出。HTML 元素的 DOM 子树（包括 HTML 元素本身）将该指令视为模板，将为底层数组的每个元素实例化一次。因此，在本例中，我们要确保为`books`数组中的每个`Book`对象渲染一个表格行（`<tr>`），因为我们是在`<tr>`标签上使用这个指令的。

`ngRepeat`指令期望一个结构化表达式，例如本例中的`"book in books"`。该表达式描述了要迭代哪个数组，以及在每个迭代中从循环内部访问数组元素时可用的变量名称。此处我们指定要迭代由作用域变量`books`引用的数组，循环变量`book`是在每次迭代中访问数组元素的方式。这样，在每次迭代中，我们都可以访问各个图书的详细信息，如书名（`book.title`）、作者（`book.author`）和 ISBN（`book.isbn`）。这种关系在图 3.7 中再次进行了说明。你还可以在图中看到`BookListCtrl`控制器作用域内有效的 DOM 部分。

```html
<!-- book_list.html -->
<table class="bm-book-list">
  <tbody>
    <tr ng-repeat="book in books">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```

```javascript
// book_list.js
bmApp.controller('BookListCtrl', function ($scope) {
    $scope.books = [
        { /* JavaScript for Enterprise */ },
        { /* News ... */ },
        { /* CoffeeScript */ }
    ];
});
```

##### 图 3.7：`ngRepeat` 在控制器作用域中迭代图书数组

因此，我们可以再次使用`ngBind`指令来生成实际输出。`ngRepeat`指令与 E2E 测试中`repeater`的关系如图 3.8 所示。

`ngRepeat`的一个特殊之处在于，该构造也受双向数据绑定约束。这意味着当底层数组的内容发生变化时，AngularJS 会自动在运行时创建新的 DOM 元素。在我们的例子中，这意味着我们只需在运行时为`books`数组添加新的`Book`对象，即可获得最新的图书列表视图。

```html
<!-- book_list.html -->
<table class="bm-book-list">
  <tbody>
    <tr ng-repeat="book in books">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```



</tbody>

</table>

```javascript
// book_list.spec.js

var selector = 'table.bm-book-list tr';

it('[...]', function() {
  expect(
    repeater(selector).column('book.title')
  ).toEqual(orderedTitles);
});
```

##### 图 3.8：`ngRepeat` 与 `repeater` 之间的关系

`ngRepeat` 的第二个特殊之处在于，它为迭代的数组的每个元素创建一个新的作用域。这一事实对我们当前的列表视图示例没有影响。然而，了解这些背景信息很重要，以避免在创建更复杂的视图时出现意外。这个方面在使用 `ngRepeat` 指令渲染表单字段时尤为重要。你应该始终清楚在哪个作用域中将字段绑定到变量。

`ngRepeat` 指令为底层数组的每个元素创建作用域，在我们的应用程序中，这导致了图 3.9 所示的列表。为了更好地理解这一点，我们在图中添加了 `ngRepeat` 生成的 HTML 代码。

你可以在图 3.9 中看到，AngularJS 在 `ngRepeat` 指令产生的每个作用域中定义了作用域变量 `book`。作用域变量 `book` 引用了相应的 `Book` 对象。

要查看列表视图，请将浏览器定向到以下 URL。

```text
http://localhost:8080/#/books
```

如果你没有出错，应该会看到如图 3.10 所示的列表视图。

## 108 AngularJS

**图 3.9：** 显示列表视图时的作用域层次结构

**图 3.10：** 列表视图

如果你得到了与图 3.10 相同的输出，那么逻辑上三个端到端（E2E）测试中至少有一个应该是“绿色”（即通过）的。最后，你可以使用熟悉的 Karma 调用来验证书籍的正确数量：

```bash
karma start karma-e2e.conf.js
```

现在只有两个测试失败了，如以下输出所示：

```text
Chrome 30.0.1599: Executed 4 of 4 (2 FAILED)

(1.233 secs / 0.983 secs)
```

那个测试书籍数量的测试现在应该能通过了。你可以继续让另外两个测试也“变绿”。

#### `orderBy` 过滤器：确定排序顺序

如前所述，你可以使用 `ngRepeat` 指令根据特定条件对数组进行排序。你可以使用 AngularJS 自带的 `orderBy` 过滤器。

所以现在让我们扩展列表视图的模板，以便我们的书籍能按书名升序排列。我们已经制定了相应的端到端测试来满足这个要求。扩展内容可见于清单 3.20。

**清单 3.20：使用 `orderBy` 过滤器确定排序顺序**

```html
<table class="bm-book-list">
  <tbody>
    <tr ng-repeat="book in books | orderBy: 'title'">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```

你可以通过相应地扩展结构化的 `ng-repeat` 表达式来使用集合过滤器。为此，你可以使用管道符号，就像使用格式化过滤器一样。管道符号位于集合过滤器的名称之后（此处为：`orderBy`）。名称后面是一个冒号，将过滤器与其参数列表分隔开。你可以使用静态值，也可以引用作用域变量。作为清单 3.20 中代码的替代方案，你也可以在 `BookListCtrl` 控制器的作用域中定义一个名为 `booksOrderedBy` 的变量，并将字符串 `"title"` 赋值给它。这样，`ng-repeat` 表达式就会变成这样：

```text
ng-repeat="book in books | orderBy: booksOrderedBy"
```

这里，`orderBy` 过滤器也受双向数据绑定的影响。这意味着你只需要在运行时更改作用域变量 `booksOrderedBy` 的值，就能根据不同的属性（如 ISBN）对书籍进行排序。

具体来说，`orderBy` 过滤器接受两个参数。第一个参数是比较谓词，你可以用几种不同的方式来指定。

- 如果你传递一个在当前有效作用域中定义的函数的引用，那么这个函数被理解为一个 getter 函数，其返回值被解释为每个元素的比较值。然后排序将基于每个元素的比较值进行，使用比较运算符 `>`、`<` 或 `==`。过滤器会将相应的数组元素传递给该函数，这样你（在对象的情况下）就可以轻松访问对象的某些属性并将其作为参考值返回。
- 如果你传递一个字符串，这个字符串将被解释为一个 AngularJS 表达式，并最终在数组的每个元素上求值以确定比较值。因此，这种比较谓词的指定方式仅对包含对象的数组有意义。此外，你可以在前面加上减号或加号，以使数组元素按升序（`+`）或降序（`-`）排序。不加前缀时，默认按升序排序。
- 你可以指定一个 getter 函数或表达式的数组。你使用第一个谓词进行比较。如果数组的两个元素相等，则使用下一个谓词来评估这两个元素。如果使用第二个谓词比较后，这两个元素仍然相等，则使用下一个谓词进行比较，依此类推。

`orderBy` 过滤器的第二个参数是可选的。如果你将 `true` 作为第二个参数传递，那么借助第一个参数完成的排序将被反转。如果你不提供该值，则假定排序不应被反转。

在我们清单 3.20 中的扩展模板中，我们使用了第二种方式来指定比较谓词。我们传递字符串 `"title"`，这表示排序应基于我们 `Book` 对象的 `title` 属性。

因此，我们通过这个小扩展在端到端测试中指定了排序。这样一来，剩下的两个测试用例现在也应该通过了。在浏览器中的手动版本应显示正确的顺序（参见图 3.11）。

**图 3.11：** 在列表视图中对书籍进行排序

接下来，我们想使用第一种方式来指定比较谓词，以实现相同的排序效果。我们通过更改 `ng-repeat` 表达式来实现这一点：

```text
ng-repeat="book in books | orderBy: getBookOrder"
```

现在 `getBookOrder` 必须是当前有效作用域中的一个变量，并且引用一个函数，该函数为 `books` 数组中的每个 `Book` 对象返回比较值。当前有效的作用域仍然是 `BookListCtrl` 控制器的作用域。这意味着我们必须扩展这个控制器的实现，使其达到清单 3.21 所示的程度。

**清单 3.21：带有 `getBookOrder()` 函数的 `BookListCtrl` 控制器**

```javascript
bmApp.controller('BookListCtrl', function ($scope) {
  $scope.books = [
    [...]
  ];

  $scope.getBookOrder = function(book) {
    return book.title;
  };
});
```

每次调用 `getBookOrder()` 函数时，`orderBy` 过滤器都会将相应的 `Book` 对象作为参数传递给该函数。因为我们想按书名排序，所以我们返回书名作为比较值。

至此，我们已经完成了使用 getter 函数定义比较谓词的所有工作。为了验证这个排序问题的解决方案，我们可以重新运行我们的端到端测试套件。

```text
Chrome 30.0.1599: Executed 4 of 4 SUCCESS (1.401 secs / 0.532 secs)
```

就是这样。所有测试都应该通过。

#### 以编程方式调用过滤器

到目前为止，我们只在 `ngRepeat` 指令中使用了 `orderBy` 过滤器。这是一种常见的过滤器使用方式。然而，你可能也想以编程方式调用过滤器，以便在控制器或服务中将其作为辅助函数使用。好消息是，在 AngularJS 中你可以这样做。让我们看看如何实现。

**清单 3.22：在 `BookListCtrl` 控制器中以编程方式调用 `orderBy` 过滤器**

```javascript
bmApp.controller('BookListCtrl', function ($scope, $filter) {
  $scope.books = [
    [...]
  ];

  $scope.getBookOrder = function(book) {
    return book.title;
  };

  // 这只是为了演示过滤器的编程用法
  var orderBy = $filter('orderBy');

  var titles = $scope.books.map(function(book) {
    return {title: book.title};
  });

  console.log('排序前的标题', titles);

  // 这是过滤器的实际调用
  titles = orderBy(titles, 'title');

  console.log('排序后的标题', titles);
});
```

如清单 3.22 所示，要以编程方式调用过滤器，你需要使用 `**$filter**` 服务，AngularJS 可以通过依赖注入将其传递给你。为此，你需要在构造函数中添加一个名为 `$filter` 的参数。这样你就告诉了 AngularJS 你在这个构造函数中需要 `$filter` 服务。

`$filter` 服务本身就是一个函数，它返回该过滤器过滤器函数的引用，你可以通过将过滤器名称传递给该函数来获取这个引用。我们在清单 3.22 中所做的就是调用 `$filter('orderBy')` 来获取 `orderBy` 过滤器过滤器函数的引用。我们将这个引用存储在一个局部变量 `orderBy` 中。我们现在可以通过 `orderBy()` 来调用 `orderBy` 过滤器中的逻辑。

为了展示一个编程调用的实际例子，我们定义了一个名为 `titles` 的新数组，并使用 `Array.map()` 函数从我们的 `books` 数组中填充数据。这个新数组只包含书名。起初，这个数组中的元素顺序与 `books` 数组中的 `Book` 对象顺序相同。然而，在我们对这个数组应用 `orderBy` 过滤器的过滤器函数之后，我们得到了一个新的数组，其中的标题按升序排列。

以编程方式调用的过滤器所期望的参数与其在模板中使用时相同。然而，对于集合过滤器（如此例），我们还必须将过滤器将要应用其上的数组作为第一个参数传递。

为了比较，我们在图 3.12 中展示了排序前后的 `titles` 数组。

### 第 3 章：BookMonkey 项目 113

#### 摘要

- 你可以使用 `orderBy` 过滤器对集合（如数组）进行排序。
- `filter` 过滤器是一种集合过滤器，与 `ngRepeat` 指令关联的模板一起使用。
- 在模板中使用：
  `ng_repeat_expression | orderBy:predicate[:reverse]`
- 使用 `$filter` 服务以编程方式调用：
  `$filter('orderBy')(array, predicate [, reverse])`
- 作为谓词，你可以定义一个函数、字符串或数组，以根据上述选项进行排序。
- 你可以通过向第二个参数传入 `true` 来反转排序顺序。第二个参数是可选的。

# 数据过滤

在上一节了解了 `orderBy` 过滤器之后，现在我们将更进一步，实现一个函数来为我们的列表视图过滤条目。我们将使用另一个 `filter` 过滤器。通过 `filter` 过滤器，我们可以根据特定条件限制底层数组的输出。

然而，在编写实际实现之前，我们将先实现指定过滤器函数预期行为的测试用例。为此，我们扩展列表视图的 E2E 测试套件，并再编写三个测试用例。这一扩展如清单 3.23 所示。

# 清单 3.23：搜索功能的 E2E 测试

```javascript
describe("E2E: book list view", function () {
  [...]

  it('should allow filtering by book title', function() {
    // Coffee
    var searchText = orderedTitles[0].substr(0, 6);

    input('searchText').enter(searchText);

    expect(
      repeater(selector).column('book.title')
    ).toEqual([orderedTitles[0]]);
  });

  it('should allow filtering by author', function() {
    // Andreas
    var searchText = expectedBooks[0].author.substr(0, 7);

    input('searchText').enter(searchText);

    expect(
      repeater(selector).column('book.title')
    ).toEqual([orderedTitles[0]]);
  });

  it('should allow filtering by isbn', function() {
    // 050-1
    var searchText = expectedBooks[0].isbn.substr(-5, 5);

    input('searchText').enter(searchText);

    expect(
      repeater(selector).column('book.title')
    ).toEqual([orderedTitles[0]]);
  });
});
```

为了表述实际预期，在三个测试用例中我们使用了与前面章节中相同的机制，即 `repeater`。然而，与之前的测试用例不同，在新的测试用例中我们使用了 ngScenario 的 `input()` 函数。使用此函数，你可以引用模板中使用 `<input>` 标签定义的 DOM 元素。这意味着你可以使用 `input()` 函数与输入字段、单选按钮和复选框等进行交互。因此，`input()` 函数需要一个参数，即 `<input>` 元素绑定到的作用域变量的名称。在过滤器函数的实现中，我们可以使用 `ngModel` 指令将 `<input>` 标签绑定到作用域变量。因此，使用 `input()` 函数，我们规定在我们的列表视图中必须有一个列表框，通过 `ngModel` 指令绑定到作用域变量 `searchText`。此输入字段用于输入搜索字符串，列表视图中的条目将据此进行过滤。

你可以使用 `enter()` 以编程方式向此框中输入字符串。

将字符串作为第一个参数传递给 `enter()` 函数。如果你仔细查看三个新的测试用例，你会发现它们都遵循相同的模式。我们让执行环境在输入字段中输入一个字符串，然后检查图书列表是否只包含正确的条目。应该能够对图书的所有属性进行全文搜索。在每个测试用例中，我们分别随机定义了一个针对图书标题、作者和 ISBN 的过滤器。因此，在测试用例 1 中输入“Coffee”、测试用例 2 中输入“Andreas”、测试用例 3 中输入“050-1”后，过滤后的列表视图应始终产生相同的结果，即只应显示一个条目：Andreas Schubert 的“CoffeeScript”图书。

自然，此时执行列表视图的 E2E 测试套件将导致三个失败的测试。

```text
Chrome 30.0.1599: Executed 7 of 7 (3 FAILED)

(1.479 secs / 1.186 secs)
```

我们现在可以着手满足测试用例的预期了。首先，我们扩展列表视图的模板，添加刚才提到的搜索功能的输入字段（参见清单 3.24）。

# 清单 3.24：搜索功能输入字段的定义

```html
<input type="text" placeholder="Search..." ng-model="searchText">

<table class="bm-book-list">
  <tbody>
    <tr ng-repeat="book in books | orderBy: getBookOrder">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```




这里有趣的是与`<input>`标签一起使用的`ngModel`指令。它确保在输入框和`searchText`作用域变量之间建立了双向数据绑定。我们在列表视图 DOM 部分有效的作用域中引用`searchText`变量。这将是我们`BookListCtrl`控制器的作用域。我们并没有随意选择作用域变量`searchText`的名称。我们知道，在我们的测试用例中，我们已经指定输入字段应该绑定到名为`searchText`的作用域变量。

我们在第 1 章“AngularJS 快速入门”中已经看到了`ngModel`指令的实际应用。通过双向数据绑定，AngularJS 在输入字段的值发生变化时自动更新`searchText`作用域变量，反之亦然。因此，作用域变量`searchText`的值发生变化时，输入字段中也会立即显示出来。对于我们的过滤器函数而言，双向数据绑定的第一个方面才是相关的。

如果我们没有犯错，搜索框现在应该出现在我们的图书列表中了（参见图 3.13）。然而，条目尚未被限制在列表中，因为我们还没有安装`filter`过滤器。

我们现在可以引入`filter`过滤器，如清单 3.25 所示。

#### 图 3.13：列表视图中的搜索字段

# 清单 3.25：使用`filter`过滤器的搜索功能

```html
<input type="text" placeholder="Search..." ng-model="searchText">

<table class="BM-book-list">
  <tbody>
    <tr ng-repeat="book in books | orderBy: getBookOrder | filter: searchText">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```

由于`filter`过滤器与`orderBy`过滤器一样也是集合过滤器，我们将其与`ngRepeat`指令一起使用。为此，我们用管道符号扩展`ng-repeat`表达式。

如前所述，`searchText`作用域变量作为过滤器的过滤谓词。因此，我们将此变量的值作为第一个参数传递给过滤器。这样，创建的`searchText`变量与`filter`过滤器之间建立了从输入框到过滤器的连接。结果，过滤器根据输入限制图书列表。AngularJS 执行过滤逻辑，使得每次`searchText`的值发生变化时，你都会立即获得一个过滤后的列表，该列表代表对`Book`对象数组的全文搜索结果。

如果你在浏览器中运行示例，例如在输入字段中输入字符串“coffee”，你会立即获得预期的效果，如图 3.14 所示。我们的列表视图应该只包含 Andreas Schubert 的“CoffeeScript”图书这一项，因为这是唯一一本在其属性中包含“Coffee”字符串的图书。我们应该在此强调，我们实现搜索功能时没有编写一行 JavaScript 代码。

#### 图 3.14：过滤后的列表视图

我们创建的测试现在必须成功运行。Karma 对我们 E2E 测试配置的结果如下。

```text
Chrome 30.0.1599: Executed 7 of 7 SUCCESS (1.763 secs / 1.474 secs)
```

在我们更详细地讨论`filter`过滤器的操作之前，我们可以在图 3.15 中看到`ngModel`指令、`filter`过滤器和 E2E 测试中的`input()`函数之间的关系。

```html
<!-- book_list.html -->

<input type="text" placeholder="Search..." ng-model="searchText">

<table class="bm-book-list">
  <tbody>
    <tr ng-repeat="book in books | orderBy: getBookOrder | filter: searchText">
      <td ng-bind="book.title"></td>
      <td ng-bind="book.author"></td>
      <td ng-bind="book.isbn"></td>
    </tr>
  </tbody>
</table>
```

```javascript
// book_list.spec.js

var selector = 'table.bm-book-list tr';

it('[...]', function() {
  // Coffee
  var searchText = orderedTitles[0].substr(0, 6);
  input('searchText').enter(searchText);

  expect(repeater(selector).column('book.title')).toEqual([orderedTitles[0]]);
});
```

#### 图 3.15：`ngModel`、`filter`与`input()`之间的关系

#### 摘要

- 使用`filter`过滤器，可以根据特定条件过滤数组。例如，您可以实现客户端搜索功能。
- 除了支持全文检索外，您还可以彻底控制数据集合的过滤方式。
- 通过可选的比较器（comparator），您可以为比较操作定义过滤逻辑。
- 在模板中使用：`ng_repeat_expression | filter:predicate[:comparator]`
- 程序式地调用`$filter`服务：`$filter('filter')(array, predicate[, comparator]);`

在例程 3.25 中，`filter`过滤器会根据包含字符串或可转换为字符串的任何`Book`对象属性来过滤数组。因此，匹配是基于子串的比较确定的，且不进行区分大小写。这意味着这种类型的过滤器使用等同于全文搜索。

与`orderBy`过滤器类似，您可以通过传递一个过滤器谓词（而不是字符串或函数）进一步配置`filter`过滤器。因此，存在以下可能的方式：

- 如果您将字符串作为过滤器谓词传入（如例程 3.25），则该过滤条件将根据数组元素比较的情况来筛选底层数组。如果某个元素与不包含区分大小写的该字符串或其任何子串匹配，则将其包含在返回的数组中。如果是对象形式的数组元素（如在`books`数组的情况下），则会比较所有对象的字符串属性以及所有可转换为字符串的属性。此外，您可以通过在该过滤谓词前加上感叹号（`!`）对其进行取反操作。
- 如果底层数组的元素是对象（如我们的`books`数组），您可以使用过滤器谓词来确定应检查哪些对象属性以进行匹配。您还可以为每个对象的属性指定一个单独的搜索字符串。示例：`book in books | filter: {title: 'Coffee', author: 'Andreas'}`。在这种情况下，只有满足两个条件的书才会被包含在结果中（标题中包含字符串“coffee”且作者中包含字符串“Andreas”）。由于比较时不区分大小写，因此值“coffee”和“andreas”也将视为匹配项。
- 如果您将函数作为过滤器谓词传入，则可以在该函数中指定任何过滤逻辑。当评估过滤器时，AngularJS 会对数组中的每个元素调用此函数。框架将该相应元素作为第一个参数传递给该函数。约定是：如果要将元素包含在返回的数组中，则该函数必须返回`true`。否则，它必须返回`false`。示例：`book in books | filter: getCoffeeBook`。

在该控制器的构造函数中，我们现在需要确保`getCoffeeBook()`函数已在作用域内定义并包含了适当的过滤逻辑。

```javascript
$scope.getCoffeeBook = function(book) {
  return book.title.indexOf('Coffee') !== -1;
};
```

在这种情况下，只有包含字符串“Coffee”的书才会被包含在结果中。由于我们使用的是`indexOf()`函数，因此不会再匹配到小写的“coffee”字符串。请注意，原意是若不指定忽略大小写或转换逻辑时，“coffee”将不再产生匹配。更准确的理解是：`indexOf()`默认进行严格匹配，因此如果不做额外的小写转换或忽略大小写的判断，像“coffee”这样的输入将不再产生匹配结果。

除了作为第一个参数传递的过滤谓词外，您还可以向过滤器传递一个可选的第二参数以进行比较器（comparator）。通过使用第二个参数，您可以指定比较器。顾名思义，比较器是一个定义如何将过滤器谓词与数组中的值进行比较的逻辑函数。这意味着我们可以使用比较器来确定字符串比较是否应该区分大小写或完全定义一条不同的规则。关于比较器，您有几个选项：

- 如果您传递一个比较器函数，当需要对来自底层数组的值和过滤器谓词进行比对时，框架总是会调用这个函数。第一个参数获取的是过滤器谓词，第二个参数则是底层的值。返回时必须存在匹配才返回`false`，否则必须为`true`。
- 您可以直接传递`true`。这表明将基于`angular.equals()`进行比较。这意味着比较时将考虑区分大小写，并且需要完全精确的匹配（而不仅仅是子串匹配）才能被视为匹配项。

## 程序式调用`filter`过滤器

其他 AngularJS 类似乎也可以被应用在应用程序组件中（例如控制器、服务和指令）。为了实现这一点，可以使用`$filter`服务，框架通过依赖注入传递给您的代码。实际看起来是这样的：

```javascript
$filter('filter')(array, predicate[, comparator]);
```

同样，您需要在第一个参数传递要过滤的数组，然后再作为第二个和第三个参数传入相应的谓词和可选的比较器。之后才可以传入相应的比较器和第三项参数，它们可以用于判断是否允许大小写敏感或自定义其他规则等处理流程。

#### 在应用中导航

我们现在已有一个基本的详细查看视图和列表视图的实现版本。但是到目前为止，这两者之间还没有建立任何链接，因此目前你只能通过浏览器地址栏在这两个视图之间进行切换。在这个步骤中我们要改变这种情况，并展示如何在 AngularJS 中使用路由机制实现应用内部的页面跳转。为此，我们构建如下的用户故事：

> “作为用户 Michael，我能够在应用中自由导航并与之交互。”

## 使用下载的项目文件测试本节代码

您可以从出版社网站获取配套项目，用于本节中的操作指导。首先请更改目录路径到`ch03_04_navigation/app`所在位置，然后从中启动`http-server`服务即可。之后我们接着进入下一步的操作说明部分。

### 带有关闭`$routeProvider.otherwise()`默认路由的配置方式

回顾一下，我们在`app.js`文件中配置了针对两个视图的路由逻辑。在这一步骤之前，我们先优化路由设置。通过一个`otherwise()`块，我们可以定义当用户导航到未被任何`when()`模块覆盖的 URL 地址时应发生的行为。使用`redirectTo`属性指定此类请求应重定向至`/books`路径，这样最终就能引导用户进入我们之前的列表页面。该扩展内容见例程 3.26。

**示例 3.26：在`app.js`中通过`otherwise`块扩展路由配置**

```javascript
[...]

bmApp.config(function ($routeProvider) {
  $routeProvider.when('/books/:isbn', {
    templateUrl: 'templates/book_details.html',
    controller: 'BookDetailsCtrl'
  })
  .when('/books', {
    templateUrl: 'templates/book_list.html',
    controller: 'BookListCtrl'
  })
  .otherwise({
    redirectTo: '/books'
  });
});
```

现在我们要建立一个列表与详情之间的跳转链路，通过实施工具实现从列表中调用特定书籍的详情页，反之也能支持由详情页返回列表的功能。当然也应该允许用户随时在两者之间相互切换，以便更好地体验整个流程的操作路径。

设计思路如下：首先在测试阶段，我们需要定义预期的行为，并通过单元测试验证实际效果。为此，我们需在原有的测试套件基础上扩展新的用例，分别针对 List 视图（书目录 list）和 Details view（详情页 details）添加对应的自动化检验内容。

**示例 3.27：列表页导航至详情页面的测试案例**

```javascript
describe("E2E: book list view", function () {
  [...]

  it('should appropriately navigate to details view', function() {
    var i = 0,
        detailsLink = selector + ':nth-child(' + (i + 1) + ') a';

    element(detailsLink).click();

    expect(
      browser().location().path()
    ).toEqual('/books/' + expectedBooks[i].isbn);
  });
});
```

例程 3.27 展示了针对列表页面的测试案例。该示例涉及一些在此之前未曾接触过的`ngScenario`机制特性。首先这里我们使用`element`函数结合 CSS 选择器来定位具体的 DOM 元素。其次，它表明可以通过`browser().location()`接口获取当前地址栏状态的某些信息。

我们还扩展了原始的 selector CSS 表达式，使其能够引用第*n*行中包含对应详情链接的`<a>`标签，随后将其结果存储在一个名为`detailsLink`的局部变量中。在当前测试用例里，该变量仅指代第一行的`<a>`元素（因为初始值`i=0`）。

也就是说，我们设定的是从列表页到详情页的连接应通过超链接构建。调用被绑定的 DOM 元素的`click()`方法，即模拟用户在执行测试时将点击对应的锚点按钮。这时 Karma 框架会触发相应的事件，让应用做出响应并打开目标详情页面。我们可以很容易地检查这一行为是否生效，只需查看其内容即可。

## 清单 3.28：从详情视图导航到列表视图的测试用例

```javascript
describe("E2E: book details view", function() {
  [...]

  it('should appropriately navigate to list view', function() {
    browser().navigateTo('#/books/978-3-89864-728-1');
    element('.bm-list-view-btn').click();

    expect(
      browser().location().path()
    ).toEqual('/books');
  });
});
```




如**清单 3.28**所示，从详情视图返回列表视图的测试用例与之前的测试用例具有相同的结构。我们导航到 ISBN 为`978-3-89864-728-1`的书籍的详细描述，并让 karma 点击我们通过`.bm-list-view-btn` CSS 选择器引用的 DOM 元素。然后，我们期望应用程序显示列表视图。我们通过将浏览器地址栏的值与 URL 的路径组件进行比较来检查这一点。

在扩展了两个测试套件之后，我们可以使用 E2E 配置运行我们的 E2E 测试，并确保它们失败。然后我们可以继续实现所需的功能，最终满足用户故事。

#### 使用 Hashbang URL 进行导航

要在详情视图中添加链接，我们可以利用`ngHref`指令轻松扩展列表视图的模板。我们在 BookMonkey 项目开始时使用这个指令在详情视图中放置了一个指向出版社网站的超链接。

我们需要将`ngHref`指令与`<a>`标签一起使用，以定义包含一个或多个表达式的超链接。这样做的原因是 AngularJS 使用这个指令来确保链接只在表达式被求值后才设置。如果我们不使用这个指令，用户可能会看到一个无效的链接，因为框架尚未对表达式进行求值。由于 AngularJS 通常非常快地对表达式进行求值，显示无效链接的概率相当小，但并非为零。

因此，我们使用`ngHref`指令和`<a>`标签将列表视图中的书籍标题与相应的详情视图链接起来。我们通过将`ng-href`指令设置为详情视图的相对路径来实现这一点（参见**清单 3.29**）。使用表达式`{{book.isbn}}`，我们确保为每本书使用正确的 ISBN。然而，我们需要在相对路径之前加上一个哈希键（`#`），以便旧浏览器不会用此 URL 完全重新加载网页。

我们现在来谈谈 hashbang URL。我们实际上使用 HTML 锚点机制来显示应用程序的不同部分。AngularJS 持续监控地址栏的内容，并将任何变化加载到相应的视图中。

为了使应用程序中的各个区域（列表视图、详情视图以及以后的其他视图）可以通过深度链接访问，我们在这里使用 hashbang URL。这些 URL 中，我们主要在 URL 的哈希部分（哈希符号后面的部分）编码以调用应用程序状态。本质上，我们使用 hashbang URL 来防止旧浏览器在用户点击应该加载应用程序另一部分的链接时重新加载页面。

除了 hashbang 方法—— admittedly 这感觉像是一个临时解决方案，而且也让深度链接看起来很难看——我们可以使用 HTML5 History API。使用这个 API，可以使用常规 URL 并仍然防止 Web 应用程序的完全重新加载。在 AngularJS 中，你可以为应用程序激活所谓的 HTML5 模式。

通过激活 HTML5 模式，框架将在旧浏览器中使用 hashbang URL 进行导航，而在现代浏览器中使用带有 HTML5 History API 的常规 URL。为了实现这一点，AngularJS 会在运行时相应地重写所有链接。

然而，使用 HTML5 模式有一个缺点，这就是为什么默认情况下它是禁用的。如果你为应用程序启用 HTML5 模式，你还需要在提供应用程序的 Web 服务器上描述任何深度链接。最后，你必须确保每个用于调用应用程序的深度链接在到达浏览器执行时都会产生请求的客户端应用程序状态。

你可以通过在配置块（`config()`）中使用`$locationProvider`组件来启用 HTML5 模式。实际调用如下：

```javascript
$locationProvider.html5Mode(true)
```

#### 搜索引擎优化

搜索引擎的爬虫程序是为静态网页设计的，无法轻松索引单页应用程序。由于当前的发展越来越趋向于动态网页和应用程序，现在已经有了针对 Ajax 爬虫和 HTML 快照的规范。使用主流搜索引擎达成的规范，动态页面有可能被纳入搜索索引。关于这一点的优秀文章可以在 ng-newsletter 网站上找到：

```text
http://www.ng-newsletter.com/posts/serious-angular-seo.html#.Ut6K6GSIUnV
```

## 清单 3.29：带有调用详情视图超链接的列表视图模板

```html
<input type="text" placeholder="Search..."
       ng-model="searchText">

<table class="bm-book-list">
    <tbody>
        <tr ng-repeat="book in books | orderBy: getBookOrder
            | filter: searchText">
            <td><a ng-href="#/books/{{ book.isbn }}"
                ng-bind="book.title"></a></td>
            <td ng-bind="book.author"></td>
            <td ng-bind="book.isbn"></td>
        </tr>
    </tbody>
</table>
```

通过**清单 3.29**中的扩展，我们有了从列表视图到详情视图的链接。在浏览器中执行代码应该显示预期的结果，我们的书籍标题应该被渲染为链接（参见**图 3.16**）。因此，我们定义的测试之一现在应该通过。

**图 3.16：书籍标题作为链接的列表视图**

仍然缺少的是详情视图中返回列表视图的链接。要添加该链接，我们需要一个`<a>`标签。然而，我们不需要`ngHref`指令，因为列表视图的相对路径不包含表达式。只需为链接提供普通的`href`属性就足够了。

但是，有一个方面我们必须考虑。在 E2E 测试中，我们使用`.bm-list-view-btn` CSS 选择器来引用要点击的 DOM 元素。这意味着我们需要用`bm-list-view-btn` CSS 类来标注我们的返回链接，以便 Karma 可以在 E2E 测试中引用该 DOM 元素。**清单 3.30**中可以看到必要的更改。

## 清单 3.30：带有返回列表视图链接的详情视图模板

```html
<h2 ng-bind="book.title" class="bm-book-title"></h2>

<h3 ng-bind="book.subtitle" class="bm-book-subtitle"></h3>

[...]

<a href="#/books" class="bm-list-view-btn">Back</a>
```

我们现在已经实现了所需的导航。如果我们再次运行 E2E 测试套件，之前创建的两个测试用例应该不再失败。此外，浏览器中的手动测试应该反映所需的行为。点击列表视图上的书籍标题应该将我们带到详情视图。要返回列表视图，我们可以点击“Back”链接。

**图 3.17：带有返回链接的详情视图**

当然，在详情视图中你仍然只能看到书籍“JavaScript for Enterprise Developers”的详细信息，因为我们在`BookDetailsCtrl`控制器中没有使用通过 URL 传递的 ISBN（参见**图 3.17**）。我们将在下一节介绍我们的第一个服务时处理这个问题。

#### ngClick 指令：响应点击事件

到目前为止，一切顺利。不过，我们要再次处理“详情”视图中“返回”链接的实现，以引入 AngularJS 的另外两个有趣特性：`ngClick`指令和`$location`服务。

通过`ngClick`指令，我们可以指定当用户点击某个 DOM 元素时调用哪个函数。因此，使用此指令来实现“返回”链接似乎是合乎逻辑的，尽管这样做除了用于教学目的外不会带来任何其他优势。

### 清单 3.31：使用 ngClick 指令从控制器作用域调用函数

```html
<h2 ng-bind="book.title" class="bm-book-title"></h2>

<h3 ng-bind="book.subtitle" class="bm-book-subtitle"></h3>

[...]

<a ng-click="goToListView()" href=""
  class="bm-list-view-btn">Back</a>
```

如清单 3.31 所示，我们使用`ngClick`指令来指定当用户点击`<a>`元素时调用`goToListView()`函数。因此，AngularJS 期望`goToListView()`函数在“详情”视图的当前有效作用域或其父作用域中被定义。“详情”视图的当前有效作用域仍然是`BookDetailsCtrl`控制器的作用域。因此，我们将在与此控制器相同的作用域中实现此功能。

您可能已经注意到，我们的`<a>`标签包含一个赋值为空字符串的`href`属性。这样做唯一的原因是，大多数浏览器只有在`<a>`标签包含`href`属性时才会格式化链接。因此，我们只需定义一个空的`href`属性来规避 CSS 规则。

#### $location 服务：与地址栏交互

我们现在可以继续在`BookDetailsCtrl`控制器的作用域中实现`goToListView()`函数。参见清单 3.32。

### 清单 3.32：BookDetailsCtrl 控制器中的 goToListView() 函数

```javascript
bmApp.controller('BookDetailsCtrl',
function ($scope, $location) {
    [...]

    $scope.goToListView = function() {
        $location.path('/books');
    };
});
```

如您在清单 3.32 中所见，`goToListView()`的实现很简单，仅由一行 JavaScript 代码组成。需要注意的重要一点是，我们可以通过依赖注入让 AngularJS 向我们传递`$location`服务。我们通过在控制器的匿名构造函数中添加一个参数来实现这一点。

`$location`服务允许您轻松地与浏览器地址栏交互。在内部，此服务使用 DOM API 的`window.location`对象，并提供一种双向数据绑定。这意味着您使用`$location`服务进行的任何更改都会直接影响地址栏，反之亦然。因此，您可以轻松地以编程方式更改地址栏的内容，并使用此服务导航到应用程序中的另一个视图。

这就是我们在`goToListView()`函数中所做的。使用`path()`函数，我们操作当前 URL 的路径部分并将其赋值为`/books`。这意味着当您在“详情”视图中点击“返回”链接时，会调用`/books`路由，从而导致显示列表视图。此行为与我们的第一个选择完全一致。因此，相应的 E2E 测试应该仍然通过。

除了`path()`函数，`$location`服务还提供了更多与地址栏交互的函数。完整的列表和描述可以在这里找到：http://docs.angularjs.org/api/ng.$location

我们应该指出，该服务 API 的结构设计使得您可以使用函数来写入和读取 URL 的各个部分。因此，调用`$location.path()`（不带参数）将返回当前加载 URL 的路径部分。

#### 总结

- 您可以在路由配置中使用`$routeProvider.otherwise()`来指定默认路由，当没有任何已定义的`when()`路由匹配时使用此默认路由。
- 在 E2E 测试中，您可以使用`element()`来访问 DOM 元素，只需向函数传递一个 CSS 选择器。您可以使用`click()`以编程方式对该元素执行鼠标点击。
- 在 E2E 测试中，您可以使用`browser().location()`对象及其众多函数（如`path()`或`hash()`）来收集有关地址栏当前状态的特定信息。
- 在我们的 AngularJS 应用程序中，我们通常使用 hashbang URL 在应用程序的不同部分之间导航，这些部分我们已通过路由定义。
- Hashbang URL 还允许将路由指定为深层链接。
- 对于普通链接，您使用`<a>`标签和`href`属性。如果链接包含表达式，请使用`ngHref`指令。
- 您可以以编程方式切换到应用程序的另一个部分。您可以使用 AngularJS 的`$location`服务轻松地与浏览器地址栏交互。
- 您也可以使用 HTML5 模式来强制 AngularJS 使用常规 URL 建立到应用程序的内部链接。但是，此模式需要调整交付应用程序的 Web 服务器。
- 使用`ngClick`指令，您可以在模板中定义当用户点击带有注释的 DOM 元素时应执行哪个函数。

#### 第一个服务

在为 BookMonkey 应用程序实现了两个视图，并在上一章中展示了您可以建立应用程序各个部分之间的链接后，我们现在想在本节中创建第一个服务。我们要修复“详情”视图始终显示“JavaScript for Enterprise Developers”书籍信息的问题，因为在`BookDetailsCtrl`控制器中传递的 ISBN 没有被评估。我们将创建的服务称为`BookDataService`。

正如您在第 2 章“基本原理和概念”中所学的，您可以使用 AngularJS 应用程序中的服务来执行许多任务，包括访问应用程序数据。因此，我们可以使用服务来创建一个数据访问对象，这正是我们的`BookDataService`所要设计的。

服务的一个基本特征是它提供清晰且稳定的 API。这一点很重要，因为有了清晰且稳定的 API，您可以替换服务的内部实现并提供整体灵活性。

对于我们在本节中要实现的功能，我们编写以下用户故事：

> 作为用户 Michael，我希望能够从列表中选择一本书并检索该书的详细信息。

**使用已下载的项目**

要测试本节中的代码，您可以使用从出版商网站下载的附带项目。为此，请将目录更改为`ch03_05_first_service/app`并从那里启动`http-server`。

#### 首先，测试

像以前一样，我们从测试开始，并且将第一次编写单元测试。在 BookMonkey 项目的开始，我们在`test`目录下创建了一个名为`unit`的目录。现在在`unit`目录中，我们需要创建一个名为`services`的目录，在此目录中我们将创建一个`book_data.spec.js`文件，该文件将包含`BookDataService`的单元测试。

如前所述，AngularJS 从根本上是为可测试性而设计的。因此，所有应用程序组件都可以用单元测试进行测试。到目前为止，我们只测试了与视图的用户交互，因此或多或少地将我们的应用程序视为一个黑盒子。我们的 E2E 测试也是为此目的而做的。然而，第一次编写单元测试来测试 BookDataService 是有意义的。

在清单 3.33 中，您可以看到单元测试的基本结构与 E2E 测试的结构相同。但是，我们应该从一开始就明确，我们将使用另一个测试框架进行单元测试，因此必须使用不同的测试 API。对于我们的 E2E 测试，我们使用了 AngularJS 中的 ngScenario。然而，对于单元测试，我们将使用 Jasmine。纯粹在语法上，这两个框架是相似的，但在功能上它们被设计用于不同的目的。就像使用 ngScenario 时，您可以编写 E2E 测试，实际上定义特定的用户行为，然后根据 DOM 检查相对表面的期望；而使用 Jasmine，您可以调用和单元测试组件的所有功能，并对组件状态做出精确的陈述。因此，您可以制定非常精确的期望。

AngularJS 自带 ngMock 模块，帮助您编写 Jasmine 单元测试。该模块提供了一个 API，允许您加载和引用应用程序模块和组件。因此，您可以完全访问组件提供的所有函数。另一个巨大的优势是 AngularJS 的依赖注入机制也可以在单元测试中使用。这意味着您可以在测试中用预定义的 mock 对象替换依赖项。ngMock 模块甚至自带一些 mock 实现，以简化孤立单元测试的创建。

### 清单 3.33：BookDataService 单元测试的 beforeEach() 块

```javascript
describe('Service: BookDataService', function () {
    var BookDataService;

    // load the application module
    beforeEach(module('bmApp'));

    // get a reference to the service
    beforeEach(inject(function (_BookDataService_) {
        BookDataService = _BookDataService_;
    }));
});
```



清单 3.33 展示了我们针对 `BookDataService` 的单元测试的初步步骤。与端到端测试一样，我们使用 `describe()` 函数为单元测试定义一个测试套件。此测试套件包含两个 `beforeEach()` 调用，它们定义了在每个单元测试之前要执行的函数。在这些 `beforeEach()` 调用中，我们甚至可以看到两个主要函数 `module()` 和 `inject()` 的实际应用。这些函数由 `ngMock` 模块提供。

使用 `module()` 函数，我们将为测试加载我们的 `bmApp` 应用模块。这确保我们可以访问在此模块中实现的所有组件（服务、指令、控制器等）。

`inject()` 函数主要负责确保你在加载模块后能够访问模块的组件。顾名思义，你可以使用此函数告诉 AngularJS 通过依赖注入来注入应用组件。这基本上遵循与我们组件的匿名构造函数相同的模式。`inject()` 函数接受一个函数作为参数，在该函数内，你可以在参数中指定框架应提供哪些应用模块。正如你在清单 3.33 中看到的，这些目前还是一个很小的功能。

我们希望 AngularJS 注入 `BookDataService`，因为我们想在测试中测试该服务中的函数。一个好做法是将服务对象的引用存储在一个同名的局部变量中，这样你就可以在单元测试中轻松访问该服务。这里，我们将传递的引用保存在一个名为 `BookDataService` 的局部变量中。我们在测试套件的开头声明了这个变量（`var BookDataService`）。然而，现在我们遇到了一个问题。

根据依赖注入规则，依赖解析基于参数名称。不幸的是，我们不能在第二个 `beforeEach()` 调用中将参数命名为 `BookDataService`，因为这会覆盖我们的局部 `BookDataService` 变量。幸运的是，`inject()` 函数允许我们用下划线括起变量名（`_BookDataService_`）。AngularJS 注入器（解析依赖的内部组件）知道在测试中解析依赖时应忽略下划线。因此，我们可以将服务对象的引用赋给我们的局部变量 `BookDataService`，以便在后续的单元测试中使用。

> ### 测试中的依赖注入
>
> 将引用服务的局部变量命名为与服务相同的名称是一个好做法。这样，AngularJS 注入器就可以解析用下划线括起来的依赖项。
>
> 但是，如果你必须将局部变量命名为不同的名称，你可以在 `inject()` 调用中按照不带下划线的常规依赖项规范进行。

既然我们已经创建了测试套件的基本结构，就可以继续为 `BookDataService` 编写第一个单元测试了。

如清单 3.34 所示，嵌套 `describe()` 块从而更细致地组织测试套件是完全可能的。我们在外部 `describe()` 块中定义的用于获取 `BookDataService` 引用的 `beforeEach()` 调用，同样适用于内部 `describe()` 块中定义的所有测试用例。这里我们应该提到，`describe()` 块可以嵌套到任意深度，并且它们也可以包含 `beforeEach()` 和 `afterEach()` 块，这些块会在每个内部测试用例之前和之后执行。

### 清单 3.34：验证公共 API 定义的单元测试

```javascript
describe('Service: BookDataService', function () {

    [...]

    describe('Public API', function() {

        it('should include a getBookByIsbn() function', function ()

        {

            expect(BookDataService.getBookByIsbn).toBeDefined();

        });

        it('should include a getBooks() function', function () {

            expect(BookDataService.getBooks).toBeDefined();

        });

    });

});
```

```javascript
[...]

});
```

首先，我们验证 `BookDataService` 公共接口的定义。在第一步中，我们要求服务提供两个函数：`getBookByIsbn()` 和 `getBooks()`。为此，我们在一个独立的子套件中用 `it()` 定义相应的测试用例。

就像 ngScenario 一样，Jasmine 附带了一个漂亮的匹配器集合，你可以用它们来方便地表达期望。在清单 3.34 中，我们使用匹配器 `toBeDefined()` 来确保这两个 API 函数（`getBookByIsbn()` 和 `getBooks()`）的存在。

> ### 结构性测试
>
> JavaScript 是一种解释型编程语言，具有动态类型系统。这意味着你必须接受这种语言的所有优点和缺点。许多批评者认为的一个很大缺点是，没有编译器可以警告类型不匹配。为了解决这个问题，我们在清单 3.34 中编写了 JavaScript 的结构性测试。确保所谓的鸭子类型得到维护。在软件工程的背景下，这个术语最初由 Alex Martelli 于 2000 年在新闻组 comp.lang.python 中提出："换句话说，不要检查它是否是一只鸭子：检查它是否像鸭子一样嘎嘎叫，像鸭子一样行走，等等，这完全取决于你需要用哪种鸭子的行为子集来玩你的语言游戏。"

既然我们已经确保服务的公共 API 提供了 `getBookByIsbn()` 和 `getBooks()` 函数，我们现在就可以继续编写这些函数的具体实现了。为此，我们定义了一个独立的套件（见清单 3.35），该套件又包含两个子套件，每个函数一个。从这个例子中我们可以看到，在一个文件内组织单元测试是多么容易。

### 清单 3.35：检查公共 API 功能的单元测试

```javascript
describe('Service: BookDataService', function () {
```

```javascript
[...]

describe('Public API usage', function() {

    describe('getBookByIsbn()', function() {

        it('should return the proper book object (valid isbn)',
        function() {

            var isbn = '978-3-86490-050-1',
                book = BookDataService.getBookByIsbn(isbn);

            expect(book.title).toBe('CoffeeScript');

        });

        it('should return null (invalid isbn)',
        function() {

            var isbn = 'test',
                book = BookDataService.getBookByIsbn(isbn);

            expect(book).toBeNull();

        });

    });

    describe('getBooks()', function() {

        it('should return a proper array of book objects',
        function() {

            var books = BookDataService.getBooks();

            expect(books.length).toBe(3);

        });

    });

});

});
```

这两个 API 函数的功能从名字上已经很明显了。`getBookByIsbn()` 函数返回与传入 ISBN 匹配的 `Book` 对象，而 `getBooks()` 返回所有现有书籍的数组。

相应的单元测试在清单 3.35 中实现。我们期望当传入 ISBN 978-3-86490-050-1 调用 `getBookByIsbn()` 函数时，它会返回一个标题为 "CoffeeScript" 的 `Book` 对象。我们使用 `toBe()` 匹配器进行检查。如果传入的 ISBN 没有关联的书籍，该函数应返回 null，这我们在第二个测试用例中使用 `toBeNull()` 匹配器进行了测试。

第三个测试用例验证了 `getBooks()` 函数返回一个包含三个元素的数组。我们没有在 BookMonkey 中输入更多书籍。在这个测试用例中，我们当然可以实现更多逻辑来检查返回的对象是否真的是一个数组，以及相应的元素是否具有 `Book` 对象的结构（关键词：鸭子类型）。我们保持了测试的简单性，因为我们只是想解释基本概念，而不是深入细节。

因此，我们以单元测试的形式制定了对 `BookDataService` 的期望。我们可以运行新创建的测试套件一次，以确保测试用例失败。毕竟，我们还没有实现 `BookDataService` 服务。

我们还需要注意，我们现在使用的是用于单元测试的 Karma 配置。此配置位于 `karma.conf.js` 文件中，也应在我们项目的根目录中。如果还没有这样做，你应该从下载的 zip 文件的根目录复制此配置。

以下是调用 Karma 运行单元测试的配置文件命令。

```bash
karma start karma.conf.js
```

如果没有出错，Karma 应该会给你关于失败单元测试的信息。

```text
Chrome 30.0.1599: Executed 5 of 5 (5 FAILED) ERROR (0.727 secs / 0.022 secs)
```

除了汇总输出外，对于每个测试用例，我们都会得到一个详细的堆栈跟踪和失败原因的解释。这可能是因为我们错误地表述了期望，或者是因为程序流程中的实际错误。在我们的情况下，这五个测试用例中的每一个都应该因为相同的原因而失败。

```text
Error: Unknown provider: BookDataServiceProvider <- BookDataService
```

此错误消息意味着 AngularJS 注入器找不到我们的 `BookDataService`，因此 `inject()` 函数无法解析依赖。这是非常合乎逻辑的，因为我们还没有实现该服务。

#### BookDataService：封装数据访问

我们现在可以开始编写 `BookDataService` 的第一个实现了。首先在 `/app/scripts` 目录下创建一个名为 `services` 的目录。然后在此目录中创建一个 `book_data.js` 文件，并实现 `BookDataService`。

### 代码清单 3.36：BookDataService 的公共 API

```javascript
bmApp.factory('BookDataService', function() {

    [...]

    // Public API

    return {

        getBookByIsbn: function(isbn) {

            [...]

        },

        getBooks: function() {

            [...]

        }

    };

});
```

正如你在第 2 章“基本原则与概念”中所学，AngularJS 自带了多种服务。在代码清单 3.36 中，你可以看到我们为 `BookDataService` 使用了服务工厂（`factory()` 函数）。相比于工厂，服务提供者的优势在于可以在 `config()` 块中进行配置。然而，我们的 `BookDataService` 不需要配置，因此我们可以省去编写提供者的时间。另一种可能的选择是使用 `service()` 函数将一个类的实例注册为一个服务。此外，我们决定不让示例变得不必要的复杂。服务工厂是创建服务最常见的方式。

代码清单 3.36 显示，在第一步中，我们根据单元测试为 `BookDataService` 设定了公共接口。我们通常在定义服务的匿名函数中返回一个所谓的 API 对象。我们将所有属于服务公共 API 的函数都定义在这个对象中。这些都是我们希望提供给其他组件的功能。正如之前的单元测试所规定，第一步应该包含在 `getBookByIsbn()` 和 `getBooks()` 函数中。

在定义了 API 将要返回的对象之后，我们现在可以开始关注实现了。第一步，我们将在服务内部存储静态的书籍数据。在着手这一步之前，我们应该为我们的实现创建一个本地命名空间。为此，我们创建一个新对象并将其赋值给一个名为 `srv` 的局部变量。

一个良好的实践是将完整的内部实现写在一个命名空间中，这样你就不会意外地用内部函数污染全局命名空间，如果应用程序的其他部分错误地调用了这些函数，可能会导致难以识别的错误。

> ECMAScript 是 JavaScript 语言背后标准的名称。在撰写本书时，最新版本是 5.1 版，尽管 6 版正在开发中。

> ### 严格模式
>
> 除了使用命名空间对象的中间方案外，还有其他方法来应对 ECMAScript 5 中缺乏命名空间的问题。这些方法包括所谓的模块设计模式和严格模式的启用。如果你在严格模式下运行脚本，JavaScript 解释器会检查源代码中潜在的错误源，并在出现此类错误时停止执行。例如，在严格模式下，将值赋给一个事先未声明的变量被认为是一个潜在的错误源。原则上，为完整的 JavaScript 代码库启用严格模式总是有用的。

在创建了本地命名空间对象 `srv` 之后，我们在此对象内定义一个名为 `_books` 的数组。这个数组最终将包含 `Book` 对象（见代码清单 3.37）。因为变量名以一个下划线开头，所以这个数组仅用于内部使用，因此不会对外发布。因此，`srv._books` 数组是我们内部用于管理 `Book` 对象的数据结构的第一步。

### 代码清单 3.37：BookDataService 的内部数据结构

```javascript
bmApp.factory('BookDataService', function() {

    var srv = {};

    srv._books = [

        {

            title: 'JavaScript for Enterprise Developers',

            [...]

        },

        {

            title: 'Node.js & Co.',

            [...]

        },

        {

            title: 'CoffeeScript',

            [...]

        }

    ];

    // Public API

    return {

        [...]

    };

});
```

我们现在可以实现 `getBookByIsbn()` 函数了（见代码清单 3.38）。我们再次在命名空间中声明 `srv`。实现相对简单。我们遍历 `srv._books` 数组中的所有书籍，并将每本书的 ISBN 与函数参数进行比较。如果找到了具有给定 ISBN 的书籍，我们返回相应对象的一个副本。我们返回副本，这样任何对内部数据结构对象的引用都不会暴露给外部。最后，我们希望对服务中数据结构的更改保持控制。

如果没有找到具有给定 ISBN 的书籍，我们返回 null。回想一下，我们在单元测试中已经指定了这一点。最后，我们需要在我们的 API 对象和内部实现之间建立连接。为此，我们将对 API（`getBookByIsbn()`）的调用委托给我们的内部实现（`srv.getBookByIsbn()`）。JavaScript 专家会立即注意到，这个连接会导致 `getBookByIsbn()` API 函数变成一个闭包，并且对 `srv.getBookByIsbn()` 函数的引用会被“包含”在内，这样在 API 对象从运行时环境返回后，`srv.getBookByIsbn()` 就不会被清除。

### 代码清单 3.38：getBookByIsbn() 函数的内部实现

```javascript
bmApp.factory('BookDataService', function() {

    var srv = {};

    [...]

    // Service implementation

    srv.getBookByIsbn = function(isbn) {

        for (var i = 0, n = srv._books.length; i < n; i++) {

            if (isbn === srv._books[i].isbn) {

                return angular.copy(srv._books[i]);

            }

        }

        return null;

    };

    [...]

    // Public API

    return {

        getBookByIsbn: function(isbn) {

            return srv.getBookByIsbn(isbn);

        },

        [...]

    };

});
```



接下来，我们在`srv`命名空间内实现第二个 API 函数`getBooks()`（见代码清单 3.39）。实现相当简单。由于我们不想暴露对内部数据结构`srv._books`的引用，我们在返回数组之前先复制它。这样，我们就不必担心潜在的调用者可能获得我们数据结构的引用并对其进行操作。和之前一样，我们必须将对 API`getBooks()`的调用委托给内部实现函数`srv.getBooks()`。在这种情况下，JavaScript 运行时环境在返回 API 对象后不会清除`srv.getBooks()`，因为`getBooks()`闭包包含了对这个实现函数的引用。

### 代码清单 3.39：`getBooks()`函数的内部实现

```javascript
bmApp.factory('BookDataService', function() {

    var srv = {};

    [...]

    // Service implementation

    [...]

    srv.getBooks = function() {

        // Copy the array in order not to expose

        // the internal data structure

        return angular.copy(srv._books);

    };

    // Public API

    return {

        [...]

        getBooks: function() {

            return srv.getBooks();

        }

    };

});
```

到目前为止，我们已经实现了`BookDataService`的第一个版本。因此，之前定义的单元测试应该通过了。为了证明这一点，再次使用我们的单元测试配置调用`karma`。

```bash
karma start karma.conf.js
```

你应该会得到以下反馈。

```text
Chrome 31.0.1650: Executed 5 of 5 SUCCESS (0.892 secs / 0.016 secs)
```

### 集成`BookDataService`

现在我们可以将`BookDataService`集成到我们的两个控制器`BookListCtrl`和`BookDetailsCtrl`中。首先，我们看`BookListCtrl`控制器（见代码清单 3.40）。为此，我们通过指定它为控制器匿名构造函数的第三个参数，告诉 AngularJS 通过依赖注入将`BookDataService`传递给我们。之后，我们就可以在控制器内部使用这个服务了。

我们不再使用作用域变量`books`来引用本地定义的`Book`对象数组，而是通过`BookDataService`的`getBooks()` API 函数来访问信息。从语义上讲，我们的`BookListCtrl`控制器没有任何改变。

### 代码清单 3.40：在`BookListCtrl`控制器中调用`getBooks`

```javascript
bmApp.controller('BookListCtrl', function (

    $scope, $filter, BookDataService) {

  $scope.getBookOrder = function(book) {

    return book.title;

  };

  $scope.books = BookDataService.getBooks();

  // 这只是为了演示过滤器的编程用法

  var orderBy = $filter('orderBy');

  var titles = $scope.books.map(function(book) {

    return {title: book.title};

  });

  console.log('titles before ordering', titles);

  // 这是过滤器的实际调用

  titles = orderBy(titles, 'title');

  console.log('titles after ordering', titles);

});
```

在我们编辑`BookListCtrl`控制器时，我们也可以移除那些用于编程方式调用过滤器的不必要部分。毕竟，它们对我们的应用没有任何价值。

结果如代码清单 3.41 所示。由于我们的`BookListCtrl`控制器现在看起来好多了，我们可以来处理`BookDetailsCtrl`控制器了。

### 代码清单 3.41：经过清理后的`BookListCtrl`控制器

```javascript
bmApp.controller('BookListCtrl',

function ($scope, BookDataService) {

  $scope.getBookOrder = function(book) {

    return book.title;

  };

  $scope.books = BookDataService.getBooks();

});
```

### `$routeParams`服务：选择 URL 参数

实现我们用户故事的一个重要方面是读取 URL 路径参数中传递的 ISBN。我们需要 ISBN 来通过`BookDataService`获取正确书籍的详情。我们将在`BookDataService`中实现`getBookByIsbn()`函数。

### 代码清单 3.42：在`BookDetailsCtrl`控制器中使用`$routeParams`服务读取 URL 路径参数

```javascript
bmApp.controller('BookDetailsCtrl',

function ($scope, $location, $routeParams, BookDataService) {

    var isbn = $routeParams.isbn;

    [...]

});
```

如代码清单 3.42 所示，我们使用 AngularJS 的`$routeParams`服务来读取 URL 路径参数。和往常一样，我们通过将其指定为控制器匿名构造函数的参数来让依赖注入传递它。`$routeParams`服务包含了我们为路由配置设置的所有 URL 路径参数的值。如您在以下代码片段中所见，我们只有一个 ISBN（`:isbn`）作为路径参数在相应的路由中传递。

```javascript
$routeProvider.when('/books/:isbn', {

    templateUrl: 'templates/book_details.html',

    controller: 'BookDetailsCtrl'

});
```

我们可以通过访问`$routeParams`服务的匹配属性来获取值。在这种情况下，访问方式如下：

```javascript
var isbn = $routeParams.isbn;
```

我们将 ISBN 存储在局部变量`isbn`中。我们现在可以使用这个变量来调用`BookDataService`的`getBookByIsbn()`函数，并获取调用其详情视图的`Book`对象。在此之前，我们必须通过依赖注入获取`BookDataService`。`BookDetailsCtrl`控制器的最终版本如代码清单 3.43 所示。

### 代码清单 3.43：在`BookDetailsCtrl`控制器中调用`getBookByIsbn()`函数

```javascript
bmApp.controller('BookDetailsCtrl',

function ($scope, $location, $routeParams, BookDataService) {

    var isbn = $routeParams.isbn;

    $scope.book = BookDataService.getBookByIsbn(isbn);

    $scope.goToListView = function() {

        $location.path('/books');

    };

});
```

在我们将`BookDetailsCtrl`扩展为使用`BookDataService`之后，我们可以在浏览器中运行应用程序，看看我们现在是否能获取每本书的详情。为此，我们调用列表视图的 URL。

```text
http://localhost:8080/#/books
```

似乎有些不对劲，因为列表视图中只有一条记录。如果我们仔细检查浏览器控制台，会注意到一条错误消息。

```text
Error: Unknown provider: BookDateServiceProvider <- BookDataService
```

这个错误看起来很熟悉。在创建`BookDataService`之前运行单元测试时，我们看到过相同的消息。

AngularJS 注入器无法找到我们的`BookDataService`，因此无法解析`BookListCtrl`控制器中的依赖。这是合乎逻辑的，因为我们尚未在`index.html`中导入`book_data.js`文件。

### 代码清单 3.44：在`index.html`中包含`BookDataService`

```html
<!DOCTYPE html>

<html ng-app="bmApp">

<head>

    [...]

</head>

<body>

    [...]

    <!-- Scripts -->

    <script src="lib/angular/angular.js"></script>
    <script src="lib/angular-route/angular-route.js"></script>
    <script src="scripts/app.js"></script>
    <script src="scripts/controllers/book_details.js"></script>
    <script src="scripts/controllers/book_list.js"></script>
    <script src="scripts/services/book_data.js"></script>

</body>

</html>
```

在我们导入`book_data.js`文件（参见代码清单 3.44）之后，我们的 BookMonkey 应用程序应该能正确运行，列表视图应包含正确的条目。

此外，我们现在可以通过点击相应的条目来获取每本书的详情。图 3.18 显示了“CoffeeScript”书籍的详情视图。

![](img/7a003218cea01579a50512a6c0e40f28_155_0.png)

##### 图 3.18：CoffeeScript 书籍的详情视图

我们也可以通过运行端到端测试来判断应用程序是否正常工作。这些测试应能确认引入`BookDataService`没有对我们的应用程序产生不利影响。

### 总结

- 除了用于创建端到端测试的 ngScenario DSL 外，AngularJS 还附带了`ngMock`模块，您可以使用它来包含 AngularJS 模块，允许您的应用组件通过依赖注入传递，并允许您为这些组件编写单元测试。
- 我们选择了 Jasmine 来创建单元测试。我们本可以使用的其他框架包括 Mocha 和 QUnit。
- ngMock 的主要函数是`module()`和`inject()`。
- 我们使用服务工厂`factory()`实现了`BookDataService`。
- `BookDataService`具有清晰的公共 API 和一个初步的基础实现。
- 我们可以通过依赖注入将`BookDataService`传递给其他组件。我们目前在`BookListCtrl`和`BookDetailsCtrl`控制器中使用它。
- 我们可以使用`$routeParams`服务读取 URL 路径参数。

# 第 4 章：扩展应用程序

在上一章中，我们实现了显示书籍数据的基本功能。在本章中，我们将处理书籍的创建、编辑和删除，并构建一个小型管理区域来执行这些操作。此外，本章的第二部分我们将通过设计特殊指令来处理标签，以便对书籍进行分类。

最后，为了让更多客户端能够使用 BookMonkey，我们将把应用程序连接到一个 REST Web 服务，以便我们可以在服务器上集中管理书籍数据。

## 管理区域

在本节中，我们将构建管理区域。具体来说，我们将编写函数来处理三个方面。我们将首先在`BookDataService`中实现创建、编辑和删除书籍的剩余 CRUD 操作。我们最终将需要这些函数来在管理区域中实现相应的功能。

扩展服务之后，我们将了解如何在 AngularJS 表单中轻松处理和验证输入。`FormController`和`NgModelController`控制器是 AngularJS 核心组件的一部分。

最后，我们将熟悉一些新的指令，这些指令将允许我们在其他视图中重用现有的模板。

对于这些功能，我们将编写以下用户故事。

> 作为管理员 Stefan，我希望能够创建、编辑和删除书籍，以便始终在不受限制的主页上向应用程序用户提供最新的信息。

### 使用下载的项目

要测试本节中的代码，您可以使用从出版商网站下载的附带项目。为此，将目录更改为`ch04_01_admin/app`并从那里启动`http-server`。

### 首先是测试

在第一步中，我们扩展`BookDataService`以包含创建、编辑和删除书籍的剩余 CRUD 操作。和往常一样，我们通过单元测试来指定 API 函数所需的行为。这样，我们通过代码清单 4.1 中的测试用例扩展了`BookDataService`的测试套件。

### 代码清单 4.1：`BookDataService`公共 API 的单元测试

```javascript
describe('Service: BookDataService', function () {

    var BookDataService;

    // 加载应用模块

    [...]

    // 获取服务的引用

    [...]

    describe('Public API', function() {

        [...]

        it('should include a storeBook() function', function () {

            expect(BookDataService.storeBook).toBeDefined();

        });

        it('should include a updateBook() function', function () {

            expect(BookDataService.updateBook).toBeDefined();

        });
```

第 4 章：扩展应用程序 153

```javascript
it('should include a deleteBookByIsbn() function',

  function () {

    expect(BookDataService.deleteBookByIsbn).toBeDefined();

});

});

});
```

清单 4.1 定义了剩余函数的单元测试。我们规定创建函数应调用存储图书，更新函数更新图书和删除函数通过 ISBN 删除图书。

对于存储图书函数的单元测试还有更多内容。如常例所示，我们为新的函数同时创建一个独立的测试套件（参见清单 4.2）。

##### 清单 4.2：存储图书的单元测试

```javascript
describe('Service: BookDataService', function () {

  var BookDataService;

  [...]

  describe('Public API usage', function() {

    [...]

    describe('storeBook()', function() {

      it('should properly store the passed book object',

      function() {

        var beforeCount = BookDataService.getBooks().length;

        // store an example book

        var book = storeExampleBook();

        expect(BookDataService.getBooks().length).toBe(

                    beforeCount + 1);

        expect(BookDataService.getBookByIsbn(

                    book.isbn)).not.toBeNull();

      });

    });

    [...]

  });

  [...]

});
```



测试的实现非常清晰。我们将当前图书数量存储在局部变量`前计数`中。我们从数组的`长度`属性获取此信息（该信息由`获取图书列表()`函数返回）。随后，我们借助函数`存储示例图书()`创建一本新书。正如清单 4.3 所示，我们在该函数内使用 API 函数`通过 ISBN 获取图书()`，这正是需要测试的目标函数。其他测试用例同样需要一个样本图书。因此，我们可以将创建`书籍`对象逻辑外包给外部函数。需要注意的是，`存储示例图书()`函数返回一本样本图书。

如果实现成功，图书数量必须增加一个。我们使用与`等于()`匹配器相结合的`期望()`函数进行检查。结果数量应等于`前计数 + 1`。此外，利用 API 函数`通过 ISBN 获取图书()`，我们确保服务确实识别出了新创建的图书。根据`通过 ISBN 获取图书()`函数的规范，该函数不能返回 null。如果您将`期望()`的调用与`not`链接起来，则`为 null()`匹配器会被否定。

##### 清单 4.3：辅助函数存储示例图书()

```javascript
describe('Service: BookDataService', function () {

    var BookDataService;

    [...]

    // Helper functions

    var storeExampleBook = function() {

        var isbn = '978-3-86490-127-0',

            book = {

                title : 'Effective JavaScript (German edition)',

                subtitle : '68 Specific Ways to Harness the Power of' + ' JavaScript',

                isbn : isbn,

                abstract :'Do you realy want to master JavaScript?',

                numPages : 240,

                author : 'David Herman',

                publisher : {

                    name: 'dpunkt.verlag',

                    url: 'http://dpunkt.de/'

                }

            };

        BookDataService.storeBook(book);

        return book;

    };

});
```

原则上，API 函数`更新图书()`的测试用例遵循相同的模式（参见清单 4.4）。接下来，我们通过调用`存储示例图书()`创建我们的示例图书。随后，通过将`book.abstract`设置为“TEST”来更改示例图书的简短描述（`book.abstract`）。通过调用我们要测试的 API 函数`更新图书()`来更新该对象。因此，`BookDataService`的`getBookByIsbn`现在应返回具有更新后简短描述的对象。最后，我们可以编写删除图书的测试用例。

##### 清单 4.4：API 函数 BookDataService 中 updateBook() 的单元测试

```javascript
describe('Service: BookDataService', function () {

    var BookDataService;

    [...]

    describe('Public API usage', function() {

        [...]

        describe('updateBook()', function() {

            it('should properly update the book object',

                function() {

                    // store an example book

                    var book = storeExampleBook();

                    // change it

                    book.abstract = 'TEST';

                    // update the example book

                    BookDataService.updateBook(book);

                    expect(BookDataService.getBookByIsbn(

                        book.isbn).abstract).toBe(book.abstract);

                });

        });

        [...]

    });

    [...]

});
```

正如清单 4.5 所示，API 函数`通过 ISBN 删除图书()`的单元测试比前两个测试用例更清晰。这里我们使用`存储示例图书()`来提供示例。当我们调用我们要测试的`通过 ISBN 删除图书()`函数时，将立即删除这本示例图书。有了正确的结果，`通过 ISBN 获取图书()`函数应返回 null。

##### 清单 4.5：API 函数 BookDataService 中 deleteBookByIsbn() 的单元测试

```javascript
describe('Service: BookDataService', function () {

    var BookDataService;

    [...]

    describe('Public API usage', function() {

        [...]

        describe('deleteBookByIsbn()', function() {

            it('should properly delete the book object with

                the passed isbn', function() {

                // store an example book

                var book = storeExampleBook();

                // delete the example book

                BookDataService.deleteBookByIsbn(book.isbn);

                expect(BookDataService.getBookByIsbn(

                    book.isbn)).toBeNull();

            });

        });

    });

    [...]

});
```

此时，一如既往，我们将执行一次单元测试以确保新的测试用例失败。如果我们没有犯错，所有新创建的测试用例都将失败。现在我们可以着手实现剩余的 API 函数。

#### BookDataService 的 CRUD 操作

由于我们已经通过一些单元测试指定了新 API 函数`存储图书()`、`更新图书()`和`通过 ISBN 删除图书()`的行为，我们可以继续进行实现。

首先我们将讨论`存储图书()`函数。沿此方向，我们将扩展由该指定函数返回的 API 对象，并将调用委派给我们的内部实现函数`srv.storeBook()`。因为到目前为止我们的`BookDataService`仍然无法与后端系统通信，`srv.storeBook()`函数的实现由“一行代码”组成，我们将新的`Book`对象插入内部数组`srv._books`（参见清单 4.6）。

##### 清单 4.6：API 函数 storeBook()在 BookDataService 中的实现

```javascript
bmApp.factory('BookDataService', function() {

    var srv = {};

    srv._books = [

        ...

    ];

    // Service implementation

    [...]

    srv.storeBook = function(book) {

        srv._books.push(book);

    };

    [...]

    // Public API

    return {

        [...]

        storeBook: function(book) {

            srv.storeBook(book);

        },

        [...]

    };

});
```

基本上，我们将以相同的方式处理其他两个 API 函数。我们将进一步扩展`updateBook()`的 API 对象并将调用委派给`srv.updateBook()`。因此，`srv.updateBook()`函数的实现比`srv.storeBook()`的实现稍微复杂一些。我们将在`for`循环中遍历我们的`srv._books`数组并查找 ISBN 与传递的 ISBN 匹配的`Book`对象。当我们找到正确的对象时，我们调用来自 AngularJS 的函数`angular.extend()`以将传递给该函数的`Book`对象的属性复制到找到的`Book`对象（参见清单 4.7）。调用`extend()`函数后，我们用`return`语句让函数提前终止。这是一种小的优化，可防止我们不必要地遍历更多书籍。

顾名思义，辅助函数`angular.extend()`将第二个对象的属性扩展至第一个对象。在相同属性名的情况下，第一个对象的属性将被第二个对象的属性覆盖。

##### 清单 4.7：API 函数 updateBook()在 BookDataService 中的实现

```javascript
bmApp.factory('BookDataService', function() {

    var srv = {};

    srv._books = [

        ...

    ];

    // Service implementation

    [...]

    srv.updateBook = function(book) {

        for (var i = 0, n = srv._books.length; i < n; i++) {

            if (book.isbn === srv._books[i].isbn) {

                angular.extend(srv._books[i], book);

                return;

            }

        }

    };

    [...]

    // Public API

    return {
        [...]
        updateBook: function(book) {
            srv.updateBook(book);
        },
        [...]
    };
});
```

API 函数`deleteBookByIsbn()`尚未讨论。我们扩展 API 对象，并将调用进一步委托给内部实现函数`srv.deleteBookByIsbn()`。在该函数内部，我们再次遍历所有`Book`对象，搜索与传入的 ISBN 相同的书籍。使用数组函数`splice()`，我们将找到的`Book`对象从数组中分离出来，并提前终止函数以优化代码。

此时应注意，我们使用递减索引的`while`循环来遍历`Book`对象。这种类型的迭代在这种情况下更为合适，因为在迭代过程中我们需要使用`splice`函数从数组中删除元素。

##### 清单 4.8：BookDataService 中 API 函数 deleteBookByIsbn() 的实现

```javascript
bmApp.factory('BookDataService', function() {

    var srv = {};

    srv._books = [

        ...

    ];

    // Service implementation

    [...]

    srv.deleteBookByIsbn = function(isbn) {

        var i = srv._books.length;

        while (i--) {

            if (isbn === srv._books[i].isbn) {

                srv._books.splice(i, 1);

                return;

            }

        }

    };

    // Public API

    return {
        [...]
        deleteBookByIsbn: function(isbn) {
            srv.deleteBookByIsbn(isbn);
        }
    };
});
```

至此，我们已经在`BookDataService`中实现了所有的 CRUD 操作。如果我们没有出错，新的测试用例现在应该能够通过。这意味着我们服务的操作方法符合规范。当我们在管理区域实现相应功能时，将会引入新的 API 函数。

#### ngShow 和 ngHide 指令：显示和隐藏内容

在上一节中扩展了`BookDataService`以包含创建、更新和删除功能后，我们现在准备好为管理区域奠定基础。

第一步，我们希望为管理员创建一个特殊的列表视图，用于显示所有书籍的概览。此外，它还应该允许创建新书和删除现有书籍（参见图 4.1）。这个特殊的列表视图将成为管理区域的基础视图，因为管理员可以将其用作创建新书以及编辑和删除书籍的视图。

![图 4.1：管理员列表视线的线框图](img/7a003218cea01579a50512a6c0e40f28_168_0.png)

##### 图 4.1：管理员列表视图的线框图

请注意，在此阶段我们不会详细介绍新视图的相应端到端测试，因为它们不包含任何重要的测试新方面，而且这只会使本章显得冗长。感兴趣的读者可以通过检出随附 zip 文件中的项目，并在当前项目状态的目录中查看相应的测试用例。

##### 清单 4.9：管理员列表视图的路由配置

```javascript
var bmApp = angular.module('bmApp', ['ngRoute']);

bmApp.config(function ($routeProvider) {

    [...]

    /* Admin routes */
    .when('/admin/books', {
        // we reuse the template from the list view
        templateUrl: 'templates/book_list.html',
        controller: 'AdminBookListCtrl'
    })

    [...]
});
```

162 AngularJS

如清单 4.9 所示，我们需要为管理员列表视图配置路由。通过使用`when()`，我们在`/admin/books`路由中构建相应的路由配置，使用`book_list.html`模板和`AdminBookListCtrl`控制器。注释表明我们希望重用列表视图的模板。这意味着现在有两个路由指向同一个模板。唯一的区别是模板背后的控制器。为了使这种重取得成功，我们必须稍微调整列表视图的模板并扩展一些方面。相应的扩展如清单 4.10 所示。

##### 清单 4.10：扩展列表视图模板以使其可重用



```html
<h2 ng-show="isAdmin">管理区域</h2>
[...]
    <tr ng-repeat="[...]">
        <td ng-hide="isAdmin">
            <a class="bm-details-link"
               ng-href="#/books/{{ book.isbn }}"
               ng-bind="book.title">
            </a>
        </td>

        <td ng-show="isAdmin">
            <a class="bm-edit-link"
               ng-href="#/admin/books/{{ book.isbn }}/edit"
               ng-bind="book.title">
            </a>
        </td>
        <td ng-bind="book.author"></td>
        <td ng-bind="book.isbn"></td>
        <td ng-show="isAdmin">
            <a class="bm-delete-link"
               ng-href="#/admin/books/{{ book.isbn }}/delete">
                删除
            </a>
        </td>
    </tr>
[...]
<p ng-show="isAdmin">
    <a class="bm-new-book-link" ng-href="#/admin/books/new">
        创建新书
    </a>
</p>
```

本质上，我们扩展了模板，使得现在多个 HTML 元素可以分别使用`ngShow`和`ngHide`指令来显示和隐藏。显示和隐藏取决于作用域变量`isAdmin`。我们在`AdminBookListCtrl`控制器中将其设置为`true`，而在`BookListCtrl`控制器中不为其赋值。这实际上使其值为`false`。这意味着我们希望仅在应用程序显示管理员列表视图时显示这些特定的 HTML 元素。然而，在无限制的列表视图中，我们希望隐藏这些元素。

`<h2>`标题“管理区域”、编辑书籍的超链接（`<a class="bm-edit-link">`）、删除书籍的超链接（`<a class="bm-delete-link">`）以及创建新书的超链接（`<a class="bm-new-book-link">`）是应该在管理员变体中显示的 HTML 元素。相比之下，在管理员列表视图中打开详情视图的超链接应该隐藏。因此，基于`ngShow`和`ngHide`指令的 resulting mutual exclusion 意味着在管理员变体中，书籍标题与编辑视图链接，而在无限制变体中，它与书籍的详情视图链接。

现在我们可以继续构建`AdminBookListCtrl`控制器。为此，我们将在`app/scripts/controllers/`目录中创建文件`admin_book_list.js`。

###### 清单 4.11：`AdminBookListCtrl`控制器

```javascript
bmApp.controller('AdminBookListCtrl',
function ($scope, BookDataService) {
    $scope.isAdmin = true;

    $scope.getBookOrder = function(book) {
        return book.title;
    };

    $scope.books = BookDataService.getBooks();
});
```

清单 4.11 展示了`AdminBookListCtrl`控制器，它定义了管理员列表视图的作用域：除了将值`true`分配给作用域变量`isAdmin`之外，它的实现与无限制变体的`BookListCtrl`控制器定义了相同的作用域。

关于列表视图的管理员变体，需要介绍的就是这些。此时，我们可以在浏览器中调用该视图。管理员列表视图应该如图 4.2 所示。

![图 4.2：管理员列表视图](img/7a003218cea01579a50512a6c0e40f28_171_0.png)

###### 图 4.2：管理员列表视图

#### 使用`FormController`和`NgModelController`进行表单处理和验证

大多数 Web 应用程序需要用户输入。HTML 标准已经为此定义了表单和字段，如文本字段、复选框和单选按钮。HTML5 扩展了各种其他小部件，如滑块控件以及数字和 URL 输入字段。在内部，支持 HTML5 的浏览器会验证用户输入，以确保用户输入有效的数据。

在本节中，我们将讨论表单处理和验证。尽管浏览器进行了内部验证，AngularJS 带来了自己的机制来轻松验证表单输入。原因是需要有一种方法来影响验证的工作方式。HTML5 的默认机制朝着正确的方向前进。然而，它相当有限。例如，使用它无法使用 CSS 格式化错误消息或显示条件错误消息。因此，许多关于错误处理的需求无法被实现。使用 AngularJS

#### BookMonkey 管理后台

##### 创建新书籍

##### 创建新书籍表单的路由配置

```javascript
var bmApp = angular.module('bmApp', ['ngRoute']);

bmApp.config(function ($routeProvider) {

    [...]

    /* 管理路由 */
    [...]

    .when('/admin/books/new', {
        templateUrl: 'templates/admin/book_form.html',
        controller: 'AdminNewBookCtrl'
    })

    [...]

});
```

如清单 4.12 所示，代码中引用了`/admin/books/new`路由、`book_form.html`文件中的模板以及`AdminNewBookCtrl`控制器。这意味着我们还需要创建两个文件。首先，我们需要在`/app/templates/admin`目录中创建一个`book_form.html`文件。为此，我们需要在`templates`目录中创建一个名为`admin`的子目录。我们将在位于`/app/scripts/controllers`目录的`admin_new_book.js`文件中实现`AdminNewBookCtrl`控制器。

接下来，我们查看用于创建和编辑书籍的模板（`book_form.html`）。如清单 4.13 所示，此模板将被设计得像列表视图的模板一样可重用。使用作用域变量`isEditMode`作为开关，我们可以显示或隐藏某些元素。我们最终将在`AdminEditBookCtrl`控制器中将此作用域变量设置为`true`，并在`AdminNewBookCtrl`控制器中将其设置为`false`。

正如预期的那样，你将在`<form>`元素内找到表单处理和验证中最有趣的部分。在 AngularJS 中，`<form>`元素具有特殊语义。当你在 AngularJS 中使用`<form>`标签时，你不仅仅是在定义一个 HTML 表单。在 AngularJS 中，`<form>`标签代表`form`指令。当处理`<form>`标签时，会执行`form`指令并创建`FormController`的实例。这个`FormController`的内部状态存储有关表单的信息，例如表单是否已被用户修改以及是否有效。你不应该实现它的逻辑，因为它已经由`form`指令覆盖了。

使验证如此方便的关键点在于，你可以将此控制器的实例设置在当前有效的作用域中。而且你知道，你可以使用模板来输出作用域内定义的所有变量和函数，或用它们来“驱动”指令。这意味着你可以在模板中使用`FormController`的内部状态属性，特别是使用`ngShow`指令来显示特定内容。

脑海中的问题是：你如何告诉 AngularJS 将`FormController`实例传递到作用域？哪个作用域变量引用了这个实例？这些问题的答案在于`<form>`元素的`name`属性。`name`属性在框架内也具有特殊含义。使用此属性，你可以告诉 AngularJS 在作用域中设置`FormController`的实例。你用来访问实例的作用域变量由属性值决定。在这种情况下，它是作用域变量`bookForm`。有了这个，你现在可以在模板中使用内部属性来有条件地显示指定内容。`FormController`的属性包括：

- `$pristine` – 一个布尔值，指示用户是否已经与表单进行过交互。
- `$dirty` – 包含`$pristine`的否定值。
- `$valid` – 一个布尔值，指示表单的当前状态是否有效。其值由每个相应表单组件的验证器决定。
- `$invalid` – 包含`$valid`的否定值。
- `$error` – 指向一个错误对象，该对象指定表单当前状态无效的原因。

#### 提交和取消按钮

```html
<h2>管理后台</h2>
<div>
  <h3 ng-hide="isEditMode">创建新书籍</h3>
  <h3 ng-show="isEditMode">编辑书籍</h3>

  <form name="bookForm" novalidate>
    [...]

    <button class="bm-cancel-btn"
            ng-click="cancelAction()">取消</button>
    <button class="bm-submit-btn"
            ng-click="submitAction()"
            ng-disabled="bookForm.$invalid">{{ submitBtnLabel }}
    </button>
  </form>
</div>
```

如清单 4.13 所示，我们使用`FormController`的`$invalid`属性在表单无效时禁用提交按钮。实际的停用操作发生在依赖于传递的作用域变量的`ngDisabled`指令激活或停用表单组件时。由于我们已告诉 AngularJS 在作用域变量`bookForm`中为我们提供`FormController`的实例，因此我们可以使用表达式`bookForm.$invalid`来查明表单是否有效。

> 关于清单 4.13 的说明
>
> 我们还在`<form>`元素上添加了`novalidate`属性，以关闭浏览器的默认验证，因为我们正在使用 AngularJS 的验证机制。

我们现在可能要问这个问题：基于哪些`FormController`属性，一个表单被视为有效或无效？在上面关于`$invalid`和`$error`属性的描述中，我们提到各个表单组件的单独验证器是决定因素。清单 4.14 展示了如何为表单组件提供验证器。用于书名的`<input>`字段中使用的`required`属性负责此功能。熟悉 HTML 5 的人知道，你可以使用`required`验证器来实现此目的，它告诉浏览器用户必须在相应的输入字段中输入值。如果你在`<form>`标签中使用`novalidate`属性来关闭浏览器的默认验证，浏览器将忽略该表单中的`required`验证器和其他验证器。然而，AngularJS 的`required`指令此时会执行，然后，如果采取了必要的预防措施，它会为该输入字段激活相应的验证。

但请注意，在 AngularJS 中使用`required`验证器的先决条件是在注释的`<input>`标签中也必须使用`ngModel`指令。借助`ngModel`指令，你可以在表单组件（例如输入字段）和作用域变量之间建立双向数据绑定。这意味着框架会自动确保每个输入都绑定到作用域变量，并且每次操纵该变量时也会更新输入。

此阶段的关键方面是，AngularJS 在每次为指定的表单组件使用`ngModel`指令时都会实例化`ngModel`控制器。`NgModelController`与`FormController`类似，包含数据绑定逻辑以及执行指定表单组件验证所必需的机制。像`required`这样的验证器指令使用此机制来提供必要的验证逻辑。因此，所有可用的验证器都必须与`ngModel`指令结合使用，这一点至关重要。

正如`FormController`提供了五个属性（`$pristine`、`$dirty`、`$valid`、`$invalid`和`$error`）来评估表单的整体状态一样，`NgModelController`也包含了这五个属性，以获取单个表单组件的此信息。这意味着你可以显示，例如，依赖于单个表单组件验证状态的错误消息。清单 4.14 显示你可以为“title”字段显示特定的错误消息。然而，这里我们再次提出问题：我们如何在模板中访问`NgModelController`的五个属性。

#### 带有必填验证器的书籍创建和编辑表单模板

```html
<h2>管理后台</h2>
<div>
    <h3 ng-hide="isEditMode">创建新书籍</h3>
    <h3 ng-show="isEditMode">编辑书籍</h3>

    <form name="bookForm" novalidate>
        <input type="text" placeholder="标题..."
            ng-model="book.title" name="title" required>
        <span ng-show="bookForm.title.$dirty
            && bookForm.title.$invalid">
            请输入书名。
        </span>
    </span>
```

# 第 4 章：扩展应用程序

与`FormController`类似，`NgModelController`的“答案”也在于`name`属性。不过，`NgModelController`略有不同。虽然 AngularJS 通过当前有效作用域中指定的变量（此处为`bookForm`）为您提供`FormController`实例，但`NgModelController`的机制是通过在父级`FormController`内作为属性发布该实例来工作的。同样，您可以使用属性值（此处为`title`）指定属性的名称。这意味着您可以通过表达式`bookForm.title`访问“title”字段的`NgModelController`实例。因此，您可以使用诸如`bookForm.title.$dirty`或`bookForm.title.$invalid`。利用这两个属性，您可以有条件地显示错误消息。为此，您再次使用`ngShow`指令。此处的命令为：如果用户与“title”字段（`bookForm.title.$dirty`）进行了交互，并且其中一个验证器返回状态表明输入被视为无效（`bookForm.title.$invalid`），则显示相应的错误消息。

如果您查看清单 4.15，您会看到 ISBN 输入字段已注释了`required`验证器。在这种情况下，我们告诉 AngularJS 在`FormController`实例内发布`NgModelController`实例。因此，您可以使用表达式`bookForm.isbn.$dirty && bookForm.isbn.$invalid`显示条件错误消息。

#### 清单 4.15：使用`ngDisabled`指令

```html
<h2>Administration Area</h2>
<div>
    <h3 ng-hide="isEditMode">Create new book</h3>
    <h3 ng-show="isEditMode">Edit book</h3>

    <form name="bookForm" novalidate>

        [...]

        <input type="text" placeholder="ISBN..."
               ng-model="book.isbn" name="isbn"
               ng-disabled="isEditMode" required>
        <span ng-show="bookForm.isbn.$dirty
                       && bookForm.isbn.$invalid">
            Please enter an ISBN.
        </span>
        <br>
        [...]
    </form>
</div>
```



`FormController`和`NgModelController`相当于五个条件属性`$pristine`、`$dirty`、`$valid`、`$invalid`和`$error`。`FormController`和`NgModelController`将确保为表单及其组件设置指定的 CSS 类。例如，如果`$dirty`和`$valid`均为 true，则`NgModelController`会将相应的`<input>`元素注释上 CSS 类`ng-dirty`和`ng-valid`。

这意味着您可以为这些 CSS 类定义特定规则，以便在验证期间通过错误消息向用户提供视觉反馈。我们不再对此多说。如果您已从出版商网站下载了 BookMonkey 项目，您将了解到我们在`main.css`文件中为许多示例定义了 CSS 规则。这些规则将为有效输入显示绿色背景，为无效输入显示红色背景。

此外，我们在清单 4.15 中使用`ngDisabled`指令使 ISBN 在编辑模式下不可编辑。

除了`required`指令之外，AngularJS 内部还包含更多验证器指令，它们故意以对相应 HTML5 属性的原生验证器命名，以实现无缝转换。具体来说，有以下属性的验证器指令：

- `required`。定义必填输入。
- `pattern`。检查输入是否匹配正则表达式。
- `min`。为数值设置最小值。
- `max`。为数值设置最大值。
- `minlength`。设置输入的最小长度。
- `maxlength`。设置输入的最大长度。

此外，框架还为 HTML5 新输入字段提供验证器指令。

- `<input type="number"/>`。检查数值。
- `<input type="url"/>`。检查输入是否指定了有效 URL。
- `<input type="email"/>`。检查输入是否指定了电子邮件地址。

Listing 4.16 显示了一个定义`numPages`输入字段的模板片段。由此可知，您除了使用`required`验证器之外，还使用了两个额外验证器。第一个是`<input type="number"/>`带来的验证器，另一个是`min`验证器，它指定了输入字段的最小值。这意味着表达式`bookForm.numPages.$invalid`的结果取决于这三个验证器。

#### 清单 4.16：数字输入字段中的 min 验证器

```html
<h2>Administration Area</h2>
<div>
    <h3 ng-hide="isEditMode">Create new book</h3>
    <h3 ng-show="isEditMode">Edit book</h3>

    <form name="bookForm" novalidate>

        [...]

        <input type="number" min="1" placeholder="Number of pages..."
               ng-model="book.numPages" name="numPages" required>
        <span ng-show="bookForm.numPages.$dirty
                      && bookForm.numPages.$invalid">
            <span ng-show="bookForm.numPages.$error.min">
                The book must have a minimum number of pages.
            </span>
            <span ng-hide="bookForm.numPages.$error.min">
                Please enter a valid number of pages.
            </span>
        </span>
    </form>
</div>
```

我们希望仅在`required`或数值验证器失败时显示一个聚合错误消息。此外，如果`min`验证器失败，我们希望代之以显示一个特殊错误消息，指示用户输入更高数量的页面。为此，我们使用`NgModelController`的`$error`属性。

正如前面提到的，`$error`属性引用了一个错误对象，其属性是确定当前输入无效的验证器的字符串表示形式。对于`NgModelController`来说，这些属性的值绝对不是组件数组，而是布尔值，每个布尔值指示相应的验证器是否认为输入有效或无效。因此，您可以使用表达式`bookForm.numPages.$error.min`显示或隐藏您的特殊错误消息。在此处，您使用了众所周知的互斥模式，就像您在应用`ngShow`和`ngHide`指令时所做的那样。

#### 清单 4.17：URL 输入字段中的 URL 验证器

```html
<h2>Administration Area</h2>
<div>
    <h3 ng-hide="isEditMode">Create new book</h3>
    <h3 ng-show="isEditMode">Edit book</h3>

    <form name="bookForm" novalidate>

        [ ... ]

        <input type="url" placeholder="Publisher's website..."
               ng-model="book.publisher.url" name="publisherUrl"
               required>
        <span ng-show="bookForm.publisherUrl.$dirty
               && bookForm.publisherUrl.$invalid">
            <span ng-show="bookForm.publisherUrl.$error.url">
                Please enter a valid URL.
            </span>
            <span ng-hide="bookForm.publisherUrl.$error.url">
                Please enter the publisher's website.
            </span>
        </span>
        <br>

        [...]
    </form>
</div>
```

现在，请查看清单 4.17 中的代码。输入字段看起来与清单 4.16 中的相同，只是我们输入的是 URL 而不是页数。在这种情况下，我们肯定想要显示一个取决于`url`验证器的特殊错误消息。

完成创建书功能所缺的唯一内容是一个`AdminNewBookCtrl`控制器，我们将在`admin_new_book.js`文件中编写它。在清单 4.18 中，您可以看到我们使用依赖注入传递`BookDataService`。我们将在这个`submitAction()`函数中使用此服务来保存新的`Book`对象，当用户点击“Create new book"按钮时。此外，在此函数中，我们调用`goToAdminListView()`函数从保存操作返回到 Admin List 视图。我们在`goToAdminListView()`函数中使用了已知的`$location`服务。

#### 清单 4.18：AdminNewBookCtrl 控制器

```javascript
bmApp.controller('AdminNewBookCtrl',
    function ($scope, $location, BookDataService) {
    $scope.book = {};
    $scope.submitBtnLabel = 'Create book';

    $scope.submitAction = function() {
        BookDataService.storeBook($scope.book);
        goToAdminListView();
    };

    $scope.cancelAction = function() {
        goToAdminListView();
    };

    var goToAdminListView = function() {
        $location.path('/admin/books');
    };
});
```

我们能够仅用少量源代码实现`submitAction()`函数的一个重要原因在于：我们在`Book`对象属性与`ngModel`指令中的表单定义之间使用了双向数据绑定。这使得在用户填写表单时，`Book`对象能够持续填充所需的必要信息。最终，所有的书籍信息都位于`Book`对象中，因此该对象可以直接传递给`BookDataService`的`storeBook()`函数。实际上，我们甚至不必在作用域（scope）中初始化`Book`对象（即`$scope.book = {}`）。AngularJS 会在用户与第一个表单组件交互时自动处理此事。当然，也有许多第三方指令无法处理未初始化的对象；在这种情况下，您应该自行进行初始化。

> **使用 ngModel 指令进行数据绑定**

`ngModel`指令的值应使用点分隔符（例如，`ng-model="book.title"`）。这样就可以轻松地向对象填充相应数据。此外，您还可以利用它来避免因作用域的原型式变化而产生的令人不悦的副作用。

如果到目前为止我们没有出错，那么应该能够创建一本新书。表单应如图 4.4 所示。

当您与表单交互时，您将发现即使我们定义的验证器也在生效，因此收到的错误信息会以无效状态显示。

#### 使用 ngInclude 指令绑定模板

在构建了用于创建和编辑书籍的表单之后，我们现在想要处理预览功能。当输入书籍信息时，用户将获得即时反馈，如图 4.5 所示。

176 AngularJS

![](img/7a003218cea01579a50512a6c0e40f28_183_0.png)

**图 4.4：创建新书的表单**

![](img/7a003218cea01579a50512a6c0e40f28_183_1.png)

**图 4.5：带有预览的新书添加视图**

# 第 4 章：扩展应用程序

使用双向数据绑定，您可以轻松实现预览功能，即通过`ngModel`指令建立数据绑定，以便在将来的某个时刻在模板中显示该绑定内容。

此时，如果我们重用 Details 视图的模板，肯定可以节省大量的模板编码工作。实现这种重用的关键元素是`ngInclude`指令。

#### 清单 4.19：使用 ngInclude 指令

```
<h2>管理区域</h2>
<div class="split-screen">
    <h3 ng-hide="isEditMode">创建新书</h3>
    <h3 ng-show="isEditMode">编辑书籍</h3>

    <form name="bookForm" novalidate>

        [...]

    </form>
</div>
<div class="split-screen">
    <h3>预览</h3>
    <div class="simple-border padded"
         ng-include="'templates/book_details.html'">
    </div>
</div>
```

正如清单 4.19 所示，您可以使用`ngInclude`指令在一个模板中包含另一个模板。为此，您需要提供模板的相对路径。请注意，`ngInclude`指令期望相对路径由作用域变量提供。因此，静态路径必须使用单引号输入。

#### 预览功能说明

为了确保预览仅在表单右侧的帧中渲染，我们已用一些 CSS 类（`split-screen`、`simple-border`和`padded`）标注了对应的 HTML 元素。此处不再详细讨论具体的 CSS 规则。感兴趣的人士可以在随本书提供的可下载 ZIP 文件中找到相应的样式表。

如果在这一步骤中没有出错，浏览器界面应类似于图 4.6。

![](img/7a003218cea01579a50512a6c0e40f28_185_0.png)

**图 4.6：带有创建新书表单（含即时预览）的视图**

在表单中输入数据时，您应该会注意到，所输入的内容会立即出现在右侧的预览区域中。为了实现此功能，我们确保所有对象属性（`title`、`subtitle`等）与输入字段的名称完全相同。

第 4 章：扩展应用程序 179

#### 编辑书籍的功能

我们的 BookMonkey 应用程序应该允许管理员编辑现有的书籍。我们已经在管理员列表视图中添加了相应的超链接以导航至编辑书籍表单。因此，我们需要再次更新`app.js`中的路由配置，并输入路由`/admin/books/:isbn/edit`（见清单 4.20）。当我们在应用中打开此路由时，`book_form.html`文件中的模板以及`AdminEditBookCtrl`控制器应该加载。这意味着我们在编辑功能中重用了用于“创建新书”表单的模板。您应该已经熟悉模板中需要进行的必要更改。

##### 清单 4.20：编辑书籍表单的路由配置

```
var bmApp = angular.module('bmApp', ['ngRoute']);

bmApp.config(function ($routeProvider) {

    [...]

    /* 管理员路由 */
    [...]

    .when('/admin/books/:isbn/edit', {
        templateUrl: 'templates/admin/book_form.html',
        controller: 'AdminEditBookCtrl'
    })

    [...]

});
```

对于`AdminEditBookCtrl`控制器，我们仍需将`admin_edit_book.js`文件保存到`/app/scripts/controllers/`目录中。其实现代码如清单 4.21 所示。

##### 清单 4.21：AdminEditBookCtrl 控制器

```
bmApp.controller('AdminEditBookCtrl',
function ($scope, $routeParams, $location, BookDataService) {
    $scope.isEditMode = true;

$scope.submitBtnLabel = '编辑书籍';

var isbn = $routeParams.isbn;
$scope.book = BookDataService.getBookByIsbn(isbn);
$scope.submitAction = function() {
    BookDataService.updateBook($scope.book);
    goToAdminListView();
};

$scope.cancelAction = function() {
    goToAdminListView();
};

var goToAdminListView = function() {
    $location.path('/admin/books');
};
});
```

```

在第 180 页

几乎可以说，`AdminEditBookCtrl`控制器是按与`AdminNewBookCtrl`控制器相同的模式设计的。这两个控制器之间的主要区别之一是作用域变量`isEditMode`的定义。我们改变该变量的值，以在模板中显示或隐藏必要的 HTML 元素，并禁用 ISBN 字段。此外，我们将作用域变量`submitBtnLabel`赋值为字符串“编辑书籍”，以便在调用`submitAction()`函数的按钮上显示该文本。我们还应该知道要编辑的是哪本书。为此，我们通过`$routeParams`服务再次访问作为 URL 路径参数呈现的 ISBN。利用 ISBN，我们可以调用`BookDataService.getBookByIsbn()`获取相应的`Book`对象，并使用作用域变量`book`对其进行引用。最后，通过调用`submitAction()`函数，我们使用`BookDataService.updateBook()`更新`Book`对象。实施编辑功能仅需到此步骤。结果如图 4.7 所示。

# 第 4 章：扩展应用程序

![](img/7a003218cea01579a50512a6c0e40f28_188_0.png)

**图 4.7：带有即时预览的编辑书籍表单**

#### 删除书籍的功能

与创建和编辑书籍类似，删除对于管理员来说自然也是一个重要功能。由于实际视图仅包含一个问题以及两个按钮（一个用于确认操作，一个用于取消操作），因此非常简单（见图 4.8）。

![](img/7a003218cea01579a50512a6c0e40f28_189_0.png)

**图 4.8：删除书籍视图的线框图**



我们已在管理员列表视图中为删除功能添加了超链接。我们只需编辑 `app.js` 以更新路由配置即可，这样当调用路由 `/admin/books/:isbn/delete` 时，将加载 `book_delete.html` 模板和 `AdminDeleteBookCtrl` 控制器（见清单 4.22）。

##### 清单 4.22：删除书籍对话框的路由配置

```javascript
var bmApp = angular.module('bmApp', ['ngRoute']);

bmApp.config(function ($routeProvider) {
    [...]

    /* 管理员路由 */
    [...]

    .when('/admin/books/:isbn/delete', {
        templateUrl: 'templates/admin/book_delete.html',
        controller: 'AdminDeleteBookCtrl'
    })

    [...]
});
```

与之前一样，我们需要为它创建文件。对于模板，我们在 `/app/templates/admin/` 目录中创建 `book_delete.html` 文件。文件内容如清单 4.23 所示。

##### 清单 4.23：删除书籍对话框的模板

```html
<h2>管理区域</h2>
<h3>
删除书籍
"{{ book.title }}"</h3>
```

#### 扩展应用程序

我们在模板中只使用已经讨论过的函数。我们询问管理员是否真的要删除该书，并让他或她确认或取消操作。对于这两个操作，我们都定义了一个按钮。如果管理员确认删除，我们就调用 `deleteBook()` 函数并传递 ISBN。否则，如果管理员取消操作，则调用 `cancel()` 函数。

`AdminDeleteBookCtrl` 控制器也包含最少量的代码。我们在 `/app/scripts/controllers/` 目录下为控制器创建一个 `admin_delete_book.js` 文件。与我们使用的所有其他 JavaScript 文件一样，我们还必须使用 `<script>` 标签在 `index.html` 中包含 `admin_delete_book.js`。

##### 清单 4.24：AdminDeleteBookCtrl 控制器

```javascript
bmApp.controller('AdminDeleteBookCtrl',
    function ($scope, $routeParams, $location, BookDataService) {
    var isbn = $routeParams.isbn;
    $scope.book = BookDataService.getBookByIsbn(isbn);

    $scope.deleteBook = function(isbn) {
        BookDataService.deleteBookByIsbn(isbn);
        goToAdminListView();
    };

    $scope.cancel = function() {
        goToAdminListView();
    };

    var goToAdminListView = function() {
        $location.path('/admin/books');
    };
});
```

清单 4.24 展示了 `AdminDeleteBookCtrl` 控制器的实现。与 `AdminEditBookCtrl` 控制器类似，我们使用 `$routeParams` 服务获取要删除的图书的 ISBN。然后将 ISBN 传递给服务函数 `BookDataService.getBookByIsbn()`，并将返回的 `Book` 对象赋值给作用域变量 `book`，这样我们就可以在模板中访问图书标题和 ISBN。最后，我们定义了两个函数 `deleteBook()` 和 `cancel()`，当用户点击其中一个按钮时会被调用。`deleteBook()` 函数内部调用 `BookDataService.deleteBookByIsbn()` 函数，该函数在管理员确认删除后实际删除图书。随后，我们使用 `$location` 服务跳转到管理员列表视图。如果用户取消删除操作，也会发生跳转。

图 4.9 展示了“删除图书”对话框的外观。要查看它，你必须在管理员列表视图中点击“删除”超链接。点击“Delete”会删除图书并将你带到管理员列表视图。点击“Cancel”会将你带回管理员列表视图，但在这种情况下，没有图书被删除。

![](img/7a003218cea01579a50512a6c0e40f28_191_0.png)

#### 小结

- 你可以使用 `ngShow` 和 `ngHide` 指令来显示或隐藏模板内容。
- AngularJS 包含一个验证机制。
- 对于 AngularJS 实例化的每个 HTML 表单，你可以在五对象属性（`$pristine`、`$dirty`、`$valid`、`$invalid` 和 `$error`）中立即找到表单的整体状态和 `FormController`。
- 整体状态是相关 `NgModelController` 实例个体状态的聚合。
- 对于每个表单组件，将依据表单组件的状态创建一个 `NgModelController`，并附带之前讨论的五个属性。
- 验证器在验证中扮演重要角色。AngularJS 包含所有 HTML5 属性和表单组件的相应验证器。
- 你可以使用 `ngInclude` 指令将一个模板与另一个模板绑定，从而使模板易于复用。

#### 使用标签创建分类

在上一节中，我们搭建了一个基本的图书管理区域，可以在其中创建、编辑和删除图书。现在，我们希望引入一种将图书分类的方法。许多现代 Web 应用程序使用标签来标注图书，标签可以代表图书所属的类别（参见图 4.10）。我们还可以使用这些标签，例如，来限制搜索结果或在特定分类中搜索图书。但就目前而言，我们只会为图书创建标签列表。

标签通常具有特定的格式。它们通常是小写的，并且不包含空格。因此，在我们的应用程序中，典型的标签可能如下所示：`javascript`、`web`、`browser` 或 `realtime`。

像往常一样，我们为此功能定义一个用户故事。

> 作为用户 Michael，我希望能够看到表单中标签状态的信息，并了解该图书属于哪些分类。

#### 使用下载的项目

要测试本节中的代码，你可以使用从出版商网站下载的配套项目。为此，请将目录切换到 `ch04_02_tags/app`，然后从那里启动 `http-server`。

![](img/7a003218cea01579a50512a6c0e40f28_193_0.png)

图 4.10：用于创建带有标签输入选项的图书的视图示意图

#### 用标签扩展数据模型

为了能够用标签对图书进行分类，显然我们需要扩展数据模型。为此，打开包含 `BookDataService` 实现的 `book_data.js` 文件，并为 `srv.books` 数组中的每个 `Book` 对象添加相应的标签（参见清单 4.25）。

#### 清单 4.25：用标签扩展我们的数据模型

```javascript
bmApp.factory('BookDataService', function() {
    var srv = {};

    srv._books = [
        {
            title : 'JavaScript for Enterprise Developers',
            [...]
            tags : [
                'javascript', 'enterprise',
                'nodejs', 'web', 'browser'
            ]
        },
        {
            title : 'Node.js & Co.',
            [...]
            tags : [
                'javascript', 'nodejs', 'web',
                'realtime', 'socketio'
            ]
        },
        {
            title : 'CoffeeScript',
            [...]
            tags : [
                'coffeescript', 'web'
            ]
        }
    ];

    [...]
});
```

如清单 4.25 所示，图书 *JavaScript for Enterprise Developers* 被标注了 `javascript`、`enterprise`、`nodejs`、`web` 和 `browser` 标签。我们还为图书 *Node.js & Co.* 分配了 `javascript`、`nodejs`、`web`、`realtime` 和 `socketio` 标签。此外，我们用 `coffeescript` 和 `web` 标注了图书 *CoffeeScript*。

除此之外，我们还必须用 `getTags()` 函数扩展 `BookDataService`（参见清单 4.26）。我们将在 `tokenfield` 指令中使用此函数，以便能够为 `token` 输入字段提供自动完成功能。目前，我们只编写 `getTags()` 函数的实现。定义适当的测试用例留给有兴趣的读者作为练习。

#### 清单 4.26：用 getTags() 扩展 BookDataService

```javascript
bmApp.factory('BookDataService', function() {
    var srv = {};

    [...]
    srv.getTags = function() {
        var obj = {},
            tag;

        for (var i = 0, n = srv._books.length; i < n; i++) {
            for (var j = 0, m = srv._books[i].tags.length;
                    j < m; j++)
            {
                tag = srv._books[i].tags[j];
                if (!obj.hasOwnProperty(tag)) {
                    obj[tag] = true;
                }
            }
        }

        return Object.keys(obj);
    };

    // Public API
    return {
        [...]
        getTags: function() {
            return srv.getTags();
        },
        [...]
    };
});
```

本质上，在清单 4.26 中我们使用一对 `for` 循环来遍历图书中的所有标签，并将它们作为键放入 `obj` 对象中。由于对象中的每个键只能使用一次，该对象实际上是一个集合。换句话说，它不允许重复的标签。然后我们使用 `Object.keys()` 返回一个包含所有键的数组。这就是 `tokenfield` 插件期望作为数据源的数据结构。

#### 首先，测试

#### 用于 Bootstrap 的 jQuery 插件“Tokenfield”

当我们在上一节讨论标签时，核心焦点是构建特殊指令。此时，我们想为 `tokenfield` 指令指定一些单元测试。

`tokenfield` 指令将简化用于创建/编辑书籍的 HTML 表单中的输入标签，因为它将普通的 `<input>` 字段转换为所谓的 `token` 输入字段。这个 `token` 输入字段由名为“Tokenfield for Bootstrap”的 jQuery 插件提供，您可以从该网站下载：

<http://sliptree.github.io/bootstrap-tokenfield>

要利用此 jQuery 插件提供的功能，您必须使用我们的 `tokenfield` 指令将其连接，以便它与双向数据绑定无缝集成。在 AngularJS 中绑定 jQuery 插件是一种可以在许多应用中使用的技术。我们也希望 jQuery 巨大的生态系统也能在 AngularJS 内部使用。

在我们能为未来的 `tokenfield` 指令编写单元测试之前，我们首先需要澄清 `tokenfield` 插件是如何工作的。正如 jQuery 插件的惯例，`tokenfield` 插件通过一个 `tokenfield()` 函数扩展了一个 jQuery 基础对象。由此，我们可以使用 jQuery 将每个 `<input>` 元素转换为一个 `token` 输入字段，该字段允许我们选择并最终调用 `tokenfield()` 函数。同时，我们可以向此函数传递一个配置对象来设置 `token` 输入字段的工作方式。一个可能的调用如下所示：

```javascript
$('input').tokenfield({
    autocomplete: {
        source: ['javascript','web','browser'],
        delay: 100
    },
    showAutocompleteOnFocus: false,
    allowDuplicates: false,
    createTokensOnBlur: true
});
```

您可以通过使用 `source` 设置令牌的来源以进行自动完成，并设置完成应生效的延迟（`delay`）。`showAutocompleteOnFocus` 属性控制当输入字段获得焦点时是否应显示自动完成。此外，您可以使用 `allowDuplicates` 属性来确定是否应在输入中允许重复的令牌。最近使用的属性 `createTokensOnBlur` 控制当输入字段失去焦点时，是否应将输入文本自动转换为令牌。

因此，当您使用带有上述配置对象的 `tokenfield()` 函数时，tokenfield 插件会将 `<input>` 元素渲染为以下 DOM 结构：

```html
<div class="tokenfield form-control">
  <input type="text" tabindex="-1"
         style="position: absolute; left: -10000px;">
  <span role="status"
        aria-live="polite"
        class="ui-helper-hidden-accessible"></span>
  <input type="text" class="token-input ui-autocomplete-input"
         placeholder=""
         id="1385909441234157-tokenfield"
         style="min-width: 60px; width: 431px;"
         autocomplete="off">
</div>
```

得益于 CSS 属性 `position: absolute` 和 `left: -10000px`，原始的 `<input>` 元素将被隐藏，取而代之的是插件将显示其他 HTML 元素来建立令牌功能。特别是在这个阶段，我们应该提到第二个带有 CSS 类 `token-input` 的 `<input>` 元素，也就是我们在最终将输入数据转换为令牌之前输入数据的输入字段。此外，值得注意的是，原始的 `<input>` 元素现在是插件生成的 `<div>` 元素的子元素。

此外，我们还应更仔细地观察当我们输入一些令牌时插件生成的 DOM 元素。使用输入 `javascript`、`web` 和 `browser`，会生成以下 DOM 元素：



```html
<div class="tokenfield form-control">
  [...]
  <div class="token" data-value="javascript">
    <span class="token-label" style="max-width: 419px;">
      javascript
    </span>
    <a href="#" class="close" tabindex="-1">x</a>
  </div>

  <div class="token" data-value="web">
    <span class="token-label" style="max-width: 419px;">
      web
    </span>
    <a href="#" class="close" tabindex="-1">x</a>
  </div>
</div>

<div class="token" data-value="browser">
  <span class="token-label" style="max-width: 419px;">browser</span>
  <a href="#" class="close" tabindex="-1">×</a>
</div>

[...]
</div>
```

如上述代码所示，插件为每个令牌生成一个带有 CSS 类 `token` 的`<div>`元素。在此元素内部是一个包含令牌文本的`<span>`元素。此外，在`<div>`元素内部还有一个带有 CSS 类 `close` 的`<a>`标签。这是用于移除相应令牌的超链接。

##### `tokenfield` 指令的单元测试

我们现在可以编写单元测试了。我们需要在`/test/unit/`目录下创建一个名为`directives`的目录。在`directives`目录中，我们将创建一个名为`tokenfield.spec.js`的文件，其中将包含`tokenfield`指令的测试套件。

###### 清单 4.27：`tokenfield` 指令测试套件的 `beforeEach()` 块

```javascript
describe('Directive: tokenfield', function () {

  var $compile,
      $rootScope,
      element,
      scope;

  var testTags = ['test1", "test2", "test3'];

  // 加载应用模块
  beforeEach(module('bmApp'));

  // 获取所有需要的 AngularJS 组件的引用
  beforeEach(inject(function ($compile_, $rootScope_) {
      $compile = $compile_;
      $rootScope = $rootScope_;
  }));

  // 每个测试用例的初始化逻辑
  beforeEach(function() {
      scope = $rootScope.$new();

      scope.book = {
          tags: angular.copy(testTags)
      };

      element = $compile('<input tokenfield="book">')(scope);
  });

  [...]
});
```

如您在清单 4.27 中所见，我们在测试套件中定义了三个`beforeEach()`块。我们在第一个块中放入了应用模块`bmApp`。第二个块使用依赖注入将`$compile`和`$rootScope`服务分配给类级别变量。我们需要这两个组件在第三个`beforeEach()`块中实现每个测试用例的实际初始化逻辑。

如果在执行单元测试期间 AngularJS 的自动化机制不起作用，您必须手动完成一些指令测试任务，以便为开发者提供对测试序列的完全控制。这意味着您需要创建指令正常运行所需的部分作用域层次结构。

在我们的案例中，这意味着我们必须使用`$new()`作用域函数为每个测试用例创建一个新的作用域。我们在这个作用域中定义了一个基本的`Book`对象（`scope.book`），它只有一个`tags`属性。使用此属性，我们通过复制`testTags`数组来引用一个测试标签数组。我们之前在测试套件中将三个测试标签`test1`、`test2`和`test3`定义为局部变量。

第三个`beforeEach()`块的最后一行是指令测试最重要的部分。我们使用`$compile`服务来编译简单的模板`<input tokenfield="book">`。这实际上执行了作为属性指定的`tokenfield`指令。我们将处理后的模板赋值给变量`element`，在这种情况下，它仅由受`tokenfield`指令影响的`<input>`元素组成。然后，我们可以使用变量`element`来访问各个测试用例。

在使用`beforeEach()`块进行必要的准备后，我们可以开始第一个测试用例，以便轻松实现测试用例。

###### 清单 4.28：确保正确初始化的测试用例

```javascript
describe('Directive: tokenfield', function () {

    [...]

    it('should properly create available tokens on initialization',
        function () {
            var tokens = element.parent().find('div.token');
            expect(tokens.length).toBe(testTags.length);
            tokens.each(function (index, token) {
                expect(
                    angular.element(token).data('value')
                ).toEqual(testTags[index]);
            });
        });
    [...]
});
```

清单 4.28 展示了我们即将实现的`tokenfield`指令的第一个测试用例。在第一步中，我们希望在这个测试用例中测试`Book`对象中的三个标签是否每个都生成了相应的令牌。我们知道每个令牌的`tokenfield`插件都会创建一个包含其他元素的`<div>`元素。

然而，由于我们只有对原始`<input>`元素的引用（该元素仍将作为子节点插入父`<div>`元素中），因此我们必须采取一些措施来引用父`<div>`元素。

在我们的指令成功执行后，`element`将包含正好三个带有 CSS 类`token`的`<div>`元素。我们使用语句`find('div.token')`获取一个 jQuery 对象，该对象包含在找到的带有 CSS 类`token`的`<div>`元素中。我们将此 jQuery 对象赋值给局部变量`tokens`。最后，我们可以使用`length`属性来期望带有 CSS 类`token`的`<div>`元素数量与`testTags`数组中的标签数量相同。

# 194

此外，我们可以使用`each()`遍历各个`div.token`元素，并期望每个元素的 token 内容必须与`testTags`数组中的相应标签匹配。我们必须小心操作，以便在回调函数中不仅能获取索引，还能获取对应的 DOM 元素。要从 DOM 元素创建 jQuery 对象并能够调用`data()`函数，我们必须使用`angular.element()`函数。

> **在 AngularJS 中使用 jQuery 的说明**

AngularJS 包含其自己的 jQuery 实现，称为 jqLite。你可以通过 AngularJS 的`angular.element()`函数访问 jqLite 实现，该函数接受一个 CSS 选择器作为参数。顾名思义，jqLite 仅实现了 jQuery 中部分可用的函数。

基本上，如果可能的话，你应该熟悉这个功能子集，这样就不必依赖外部依赖项。

然而，大多数大型项目，包括 BookMonkey，仍然需要一个或多个 jQuery 插件，这意味着你仍然需要将正确的 jQuery 库作为依赖项。在这种情况下，你必须确保在`index.html`中在 AngularJS 之前包含 jQuery。这样，AngularJS 将确保包含正确的 jQuery 库，并继续将所有来自`angular.element()`的调用委托给 jQuery。换句话说，即使你使用了完整的 jQuery 库，也应该始终使用`angular.element()`。`angular.element()`的输出将始终包含一个完整的 jQuery 对象。

我们的第二个测试用例涉及创建新 token。为此，我们首先使用之前使用的相同调用来确定当前输入 token 的数量，然后将其赋值给局部变量`tokenCount`（参见清单 4.29）。此外，我们获取对`input.token-input`输入字段的引用，并将其存储在局部变量`tokenInput`中。回想一下，这是用户将实例化并最终将其内容转换为 token 的输入字段。

###### 清单 4.29：用于添加新 token 的测试用例

```javascript
describe('Directive: tokenfield', function () {
[...]

it('should properly add new tokens', function () {
    var tokenCount = element.parent().find(`div.token`).length,
        tokenInput = element.parent().find(`input.token-input`),
        testToken = 'test4';

    
    tokenInput.focus();
    tokenInput.val(testToken);
    tokenInput.blur();
    var tokenCountAfter = element.parent().find('div.token').length;
    expect(tokenCountAfter).toBe(tokenCount + 1);
    expect(scope.book.tags.length).toBe(tokenCountAfter);
    expect(element.parent().html()).toContain(testToken);

});
```

![](img/7a003218cea01579a50512a6c0e40f28_202_0.png)

###### 清单 4.30：用于删除 token 的测试用例

```javascript
describe('Directive:tokenfield',function() {

...

it("should properly remove new tokens" , function () {

var indexToRemove = 0;

expect(

  element.parent().find('div.token').length

).toBe(testTags.length - 1);

expect(

  scope.book.tags.length

).toBe(testTags.length - 1);

expect(

  element.parent().html()

).not.toContain(testTags[indexToRemove]);

});

```

清单 4.30 展示了我们即将创建的`tokenfield`指令的最后一个单元测试。在这个测试用例中，我们希望确保现有 token 的正确移除。为此，我们将局部变量`indexToRemove`赋值为零，表示我们要删除第一个 token。随后，我们引用`div.token`元素下的`a.close`超链接并触发`click`事件。结果，`tokenfield`插件将移除相应的 token。同时，`scope.book.tags`数组中的元素数量应减少一个，并且被删除的 token 字符串不应再出现在`tokenfield`输入字段中。

在我们运行最近创建的测试套件以确保`tokenfield`指令的单元测试确实失败之前，我们应该扩展 Karma 配置以单元测试实现`tokenfield`指令所需的依赖项。因此，`files`属性现在应具有以下值：

```javascript
// list of files / patterns to load in the browser

files: [

    'app/lib/jquery/jquery-1.10.2.min.js',

    'app/lib/jquery-ui/jquery-ui.min.js',

    'app/lib/bootstrap-tokenfield/bootstrap-tokenfield.min.js',

    'app/lib/angular/angular.js',

    'app/lib/angular-route/angular-route.js',

    'app/lib/angular-mocks/angular-mocks.js',

    'app/scripts/app.js',

    'app/scripts/**/*.js',

    'test/unit/**/*.js'

],
```

或者，你可以从随书附带的 zip 文件中相应的项目文件夹复制新配置。

接下来，你可以使用已知的控制台命令运行单元测试，以确保三个新的测试用例失败。

#### `tokenfield` 指令：创建标签

在上一节中介绍了 jQuery 插件 "Tokenfield for Bootstrap" 并定义了相应的测试用例后，我们现在需要处理`tokenfield`指令的实现。为此，我们为创建此指令设定了两个目标：首先，我们想使用一个更复杂的示例来展示此 AngularJS 功能的强大之处。其次，我们想使用 tokenfield 插件的实际示例，展示如何将 jQuery 插件集成到 AngularJS 中，使插件能够在双向数据绑定中无缝工作。

我们将扩展创建/编辑书籍的表单以使用`tokenfield`指令。此 jQuery 插件除了提供 token 分配功能外，还提供自动完成功能。这意味着管理员可以减少为书籍添加标签所需的工作量。

不幸的是，tokenfield 插件需要一些依赖项。特别是，我们现在必须在`index.html`中包含以下第三方库才能使用 tokenfield 插件。

- jQuery（http://jquery.com/）
- jQuery UI（http://jqueryui.com/）
- Twitter Bootstrap（仅样式表 http://getbootstrap.com/）
- Tokenfield for Bootstrap（http://sliptree.github.io/bootstrap-tokenfield/）

在随书附带的 zip 文件中，我们已经准备好了包含所有依赖项的项目，这样你就不必去寻找它们了。此外，在第 5 章"项目管理和自动化"中，我们将进一步解释如何使用 Bower 轻松管理我们的前端依赖项。

接下来，我们在`/app/scripts/`目录下创建一个名为`directives`的子目录来存放我们的指令。我们将在`directives`目录中创建一个名为`tokenfield.js`的文件，其中将包含我们的 tokenfield 指令的实现。

# 198 AngularJS

在第 2 章"基本原则和概念"中，我们已经使用了 AngularJS 的指令定义功能。正如我们在清单 4.31 中所观察到的，我们决定使用指令定义对象（DDO）来定义`tokenfield`指令。

我们在单元测试中指定要将`tokenfield`指令用作 HTML 属性。为此，我们在 DDO 的`restrict`属性中输入了"A"（代表 attribute）。实际上，我们可以跳过这一步，因为框架默认假定我们想要使用指令创建新的 HTML 属性。

此外，我们在单元测试中定义了指令应接收一个`Book`对象作为输入的要求。这意味着我们必须在相应 DDO 的`scope`属性中输入。当我们为 DDO 的`scope`属性分配一个对象时，AngularJS 将为每个`tokenfield`指令实例创建自己的隔离作用域。由于我们需要在指令中访问给定的`Book`对象，我们通过将等号（"="）赋值给`tokenfield`属性的对象来定义与父作用域的双向数据绑定。这意味着现在我们可以在链接函数中使用`scope.tokenfield`来访问给定的`Book`对象。通过使用等号定义的双向数据绑定，我们在指令中对`Book`对象所做的所有更改也会立即显示在父作用域中。你将了解到此属性对于能够直接在预览中看到给定标签至关重要。

> **关于指令的说明**

在`tokenfield`指令定义中，我们使用了一种创建自定义 HTML 属性的典型模式。指令的名称与其参数相同。这意味着你可以在模板中将该指令用作 HTML 属性，并且该 HTML 属性的值同时为指令提供输入。

#### 清单 4.31：`tokenfield` 指令



```javascript
bmApp.directive('tokenfield', function(BookDataService) {
    return {
        restrict: 'A',
        scope: {
            // tokenfield 保存一个双向绑定的
            // 对 book 对象的引用
```

##### 代码清单 4.32：The tokenfield 指令

```javascript
bmApp.directive('tokenfield', function(BookDataService) {
  return {
    [...]
    link: function(scope, elem) {
      elem.tokenfield({
        autocomplete: {
          source: BookDataService.getTags(),
          delay: 100
        },
        showAutocompleteOnFocus: false,
        allowDuplicates: false,
        createTokensOnBlur: true
      }).on('afterCreateToken', function (e) {
        addToken(e.token.value);
      }).on('removeToken', function (e) {
        removeToken(e.token.value);
      });
      [...]
    }
  }
});
```

在第二章“基本原则与概念”中，您了解到**指令**（directive）的特征在于其`link`函数。您通过将函数分配给 DDO 的`link`属性来定义`link`函数。AngularJS 会为每个指令实例仅调用一次`link`函数。这意味着您可以在`link`函数内初始化实例。通常，您在`link`函数中注册特定事件处理器并执行 DOM 操作。

在代码清单 4.32 中，我们注册了两个事件处理器以响应`tokenfield`插件内的某些事件。然而，在此之前，我们通过调用`tokenfield()`函数初始化该插件。由于`elem`对象是一个 jQuery 对象，它包装了指令作用的 DOM 元素，且我们在单元测试中决定我们的`tokenfield`指令主要用于作用于`<input>`元素，因此我们可以直接在该`elem`对象上调用此函数。

因此，我们使用与上一部分引入插件时相同的配置对象。然而，此处我们要使用不同的自动完成源。允许相应的`source`数组通过调用`getTags()`接收来自`BookDataService`的输出。这需要`BookDataService`通过依赖注入进行集成。具体而言，重要的是我们在配置对象中将`createTokensOnBlur`属性设置为`true`，以便当 tokenfield 字段失去焦点时自动转换 token 中的所有文本。回想一下，我们定义了一个只能通过该属性满足的单元测试。

正如之前所述，我们在初始化后注册了两个事件处理器。首先，我们希望当`afterCreateToken`事件发生时，本地函数`addToken()`被调用。其次，`removeToken`事件的发生应调用本地函数`removeToken()`。在这两种情况下，我们都传递创建或删除的 token，可以通过`e.token.value`访问它。

##### 代码清单 4.33：The tokenfield 指令

```javascript
bmApp.directive('tokenfield', function(BookDataService) {
    return {
        [...]
        link: function(scope, elem) {
            [...]
            // only call $apply when directive is initialized
            // to avoid 'digest already in progress'
            var initialized = false;

            function addToken(token) {
                if (initialized) {
                    // $apply() to trigger dirty checking
                    // because of 3rd-party callback
                    scope.$apply(function() {
                        scope.tokenfield.tags.push(token);
                    });
                }
            }

            function removeToken(token) {
                if (initialized) {
                    // $apply() to trigger dirty checking
                    // because of 3rd-party callback
                    scope.$apply(function() {
                        var tags = scope.tokenfield.tags,
                            i = tags.length;

                        while(i--) {
                            if (token === tags[i]) {
                                tags.splice(i, 1);
                                break;
                            }
                        }
                    });
                }
            }
            [...]
        }
    }
});
```

现在我们可以处理本地函数`addToken()`和`removeToken()`的实现。这两个函数都负责将 tokenfield 插件集成到双向数据绑定循环中。

让我们来看看代码清单 4.33 中的`addToken()`函数。该函数的设计实际上非常简单，因为它所做的只是向我们的`Book`对象的`tags`数组（`scope.tokenfield`）插入一个新 token。关键在于，我们将此逻辑实现为传递给`scope.$apply()`函数的回调函数。这意味着在执行插入逻辑之后，立即触发 AngularJS 的脏检查，从而确保新输入的更改在所有 AngularJS 组件中可见。我们必须这样做，因为在来自第三方库的回调函数中进行范围操作。因此，我们必须使用`scope.$apply()`来通知任何更改。如果我们不这样做，框架内的其他组件将直到下一个脏检查循环才会注册这些更改。

> **AngularJS 中的脏检查**
>
> 在您在回调函数中（AngularJS 之外）进行范围操作后，您必须调用相应的范围的`$apply()`函数，以便为该范围触发脏检查。当脏检查处于活动状态时，AngularJS 将注意到该范围内的某些数据已更改，并确保所有受影响的组件会根据双向数据绑定自动更新。该原则适用于第三方库（例如 tokenfield 插件）在回调函数中做出的任何更改。然而，即使在回调函数`setTimeout()`或`setInterval()`中进行范围操作，您也必须使用`$apply()`触发脏检查。因此，AngularJS 还包括等效服务`$timeout`和`$interval`。这些服务也可以使用`$apply()`内部工作。

此外，我们引入了一个名为`initialized`的标记（flag），并且仅在将该标记设置为`true`时执行我们要讨论的逻辑。您将了解到需要此标记来避开所谓的"Digest already in progress"错误。如果您尝试在已经在脏检查循环中触发脏检查，AngularJS 会抛出这些错误。由于`link`函数是在脏检查循环中执行的，因此，在某些条件下，当您调用`scope.$apply()`时，可能会遇到"Digest already in progress"错误。我们将在后面更详细地讨论这种情况。

相同的规则当然也适用于`removeToken()`函数。然而，在此函数中，我们通过插件调用的回调函数操作范围，并必须手动使用`scope.$apply()`触发脏检查。从 tokenfield 插件返回的实际删除 token 的逻辑再次非常简单。我们遍历图书标签（book tags），一旦找到匹配项就删除相应的标签。

最后，我们讨论我们在定义后立即调用的`init()`函数（见代码清单 4.35）。此时，标记`initialized`如何帮助我们摆脱“Digest already in progress”错误也变得很清楚。

## 代码清单 4.35：The tokenfield 指令

```javascript
bmApp.directive('tokenfield', function(BookDataService) {
    return {
        [...]
        link: function(scope, elem) {
            [...]
            function init() {
                if (angular.isDefined(scope.tokenfield.tags)) {
                    if (scope.tokenfield.tags.length > 0) {
                        // this call emits an 'afterCreateToken'
                        // event and this would imply a 'digest
                        // already in progress' without the
                        // initialized flag
                        elem.tokenfield('setTokens',
                                         scope.tokenfield.tags);
                    }
                }
                else {
                    scope.tokenfield.tags = [];
                }
                initialized = true;
            }
            init();
        }
    }
});
```

我们的 tokenfield 指令必须处理两个潜在的调用场景，即编辑书籍和创建新书。在第一种情况下，`Book`对象很可能已经被指定标签标注。这意味着，在这种情况下，我们必须确保 tokenfield 插件已用现有标签填充，以便它可以生成相应的 token。该调用如下所示：

```javascript
elem.tokenfield('setTokens', scope.tokenfield.tags);
```

此调用的效果是，如果我们没有使用`initialized`标记，我们会得到"Digest already in progress"错误。通过此调用，the

对于 tokenfield 插件的默认设置也意味着，每当创建一个标记（token）时，该插件都会触发`afterCreateToken`事件。回想一下，我们正是通过响应此事件来调用`addToken()`函数，这意味着它内部使用`scope.$apply()`初始化脏检查。如果我们在此过程中又发起另一次脏检查循环，就会引发上述提到的错误。因此，在我们可能性的默认操作完成并初始化之后（即在启动潜在的默认行为后），先将`initialized`标志设置为`true`，即可排除此类错误。

##### Listing 4.36：在模板中使用 tokenfield 指令以实现对书籍的创建/编辑表单的使用

```html
<h2>管理区域</h2>

<div class="split-screen">
    <div class="split-screen">
        <h3>预览</h3>
        <div class="simple-border padded"
             ng-include="'templates/book_details.html'">
        </div>
    </div>
</div>
```

至此，我们已经完成了 AngularJS 中 tokenfield 插件的封装。如果我们现在按照我们在模板中的定义（参见 Listing 4.36），在书籍创建/编辑表单（book_form.html）中使用我们的 tokenfield 指令，那么我们应该能看到一个无缝集成到双向数据绑定循环中标记输入字段（见图 4.11）。利用这个输入字段，我们现在可以轻松地通过为每本书分配适当的标签来将书籍归类分组。此外，定义的单元测试现在应该可以通过验证了。

一旦我们在下一节实现了用于输出标签的指令标记时，结果将更加清晰明了。

![](img/7a003218cea01579a50512a6c0e40f28_212_0.png)

图 4.11：带有 tokenfield 指令的书籍创建/编辑表单

#### The tags Directive：显示标签

除了为标签提供的输入选项外，我们当然还需要创建一个能够显示标签的机制。正如之前提到的那样，我们还希望再次实现一个针对此问题的指令。

tags 指令应定义一个新的 HTML 元素`<tags>`。此外，我们应该能够通过 HTML 属性（`tag-data`）指定用于标签输出的数据源。我们希望将该字符串数组作为数据源进行指定。Listing 4.37 展示了使用我们的`tags`指令的书籍详情视图（book_details.html）模板。我们将`tag-data`属性设置为`book.tags`，以此将书籍标记数组传递给该指令。

##### Listing 4.37：在详情页中使用 tags 指令

```html
<h2 ng-bind="book.title" class="bm-book-title"></h2>

<h3 ng-bind="book.subtitle" class="bm-book-subtitle"></h3>

<p>
    [...]
    <tags tag-data="book.tags"></tags>
</p>

<hr>

<p ng-bind="book.abstract" class="bm-book-abstract">
</p>

<a ng-click="goToListView()"
   href=""
   class="bm-list-view-btn">
  返回
</a>
```

**tags** 指令的实现非常简单。接下来我们将在应用程序的`/app/scripts/directives/`目录中创建名为`tags.js`的文件，该文件将包含该指令的实现内容。Listing 4.38 展示了此文件的内容。

##### Listing 4.38：标签（tags）指令



```javascript
bmApp.directive('tags', function() {
    return {
        restrict: 'E',
        templateUrl: 'component_templates/directives/tags.html',
        scope: {
            tagData: '='
        }
    };
});
```

在 Listing 4.38 中，我们使用指令定义对象（DDO）定义了该指令。我们将 `restrict` 属性设置为“E”，以此告知 AngularJS 我们希望使用该定义来定义 HTML 元素。此外，我们还通过 `templateUrl` 属性为指令提供了自定义模板。同时，我们在 `scope` 属性上赋予了一个包含 `tagData` 属性的对象。通过这个属性，我们为指令提供了对 `tag-data` 的访问权。所有这些均符合第二章“基本原理和概念”中讨论的命名规范要求。由于我们希望保持双向绑定引用，我们将“=”赋值给 `tagData` 属性。稍后您将了解到，这种双向绑定对于自动更新指令中的标签输出至关重要，因为当数组内容发生变化时能够实现这一功能。

现在我们需要定义模板。为此，我们在应用程序目录下的 `app` 文件夹中创建一个名为 `component_templates` 的目录。在此目录中，我们还要创建一个名为 `directives` 的子目录，该子目录将存放 Listing 4.38 中的 `templateUrl` 属性所指向的 `tags.html` 文件。`tags` 指令如 Listing 4.39 所示。对于双向数据绑定的输出，我们使用 `ngRepeat` 指令遍历 `tagData` 数组，并显示循环中使用的标签变量的值。`<span>` 元素中的 CSS 类名称 `bm-tag` 赋予我们的标签蓝色背景和圆角效果。此处我们不深入探讨 CSS 类的工作原理细节。

##### Listing 4.39：标签（`tags`）指令的模板

```html
<span class="bm-tag" ng-repeat="tag in tagData"> {{ tag }} </span>
```

由于 `ngRepeat` 指令会自动为数组中的每个元素生成一个 `<span>` 元素，并且在发生数据变化时自动更新输出内容，因此当我们使用 `tokenfield` 指令添加或删除标签（通过填充或移除）后，在书籍创建/编辑表单的预览中将立即获得直接的反馈信息。回想一下，我们在书籍创建/编辑表单模板中复用了详情视图（Details view）的模板以创建实时预览效果。（见图 4.12：带有 `tags` 指令的书籍表单实时更新预览。）

![图 4.12：带有 `tags` 指令的书籍创建/编辑表单实时预览](img/7a003218cea01579a50512a6c0e40f28_215_0.png)

#### 摘要

- AngularJS 内部机制在单元测试中不会自动执行，以确保开发者能够完全掌控测试过程。这意味着在进行框架通常会自动执行的指令测试时，您需要手动处理某些方面，即那些正常情况下由框架自动完成的操作。特别地，您必须使用 `$compile` 服务手动编译用于该指令的模板；AngularJS 将识别出被测试的指令并由此执行其 `link` 函数。
- 您始终是针对某个作用域进行模板编译的。您可以在单元测试中创建一个新的作用域：通过依赖注入传递 AngularJS 中的 `$rootScope`，并对其调用 `$new()` 功能来生成新作用域。
- 在针对指令编写单元测试时，您应频繁使用 `jqLite`（AngularJS 提供的唯一 jQuery 实现）而非标准的 `angular.element()` 来审查 DOM 状态。但代价在于，JQLite 仅提供了 jQuery 功能的一个子集。
- 若在您的 `index.html` 中于引入 AngularJS 之前包含正确的 jQuery 实现，则 AngularJS 将会自动配置并委托每一个来自 `angular.element()` 调用的请求指向原生 jQuery 实现。换言之，如果在 `index.html` 中正确载入 jQuery，并在此之后导入 AngularJS，那么 AngularJS 会自动将所有 `angular.element()` 调用代理给对应的 jQuery 实现。
- 在 AngularJS 中，利用指令连接现有的 jQuery 插件或其他第三方库看起来相当简单；然而，务必确保正确地将这些集成纳入双向数据绑定循环。具体而言，在第三方库执行的每个回调函数中进行作用域操作时，都必须通过 `scope.$apply()` 启动脏检查。

#### 连接 REST Web 服务

老实说，由于每个用户的数据都存储在自己的浏览器中且缺乏统一管理，我们的应用目前显得相当枯燥。这意味着无法在两个活跃的应用程序之间同步书籍数据。在本节中，我们希望通过在一个中央服务器上管理应用程序数据来提升这一限制。与后端通信是单页应用的典型应用场景之一。

正如我们在项目开始时提到的那样，我们将基于 Node.js 实现一个后端服务；因此，我们将使用 Express 框架（<http://expressjs.com>）来设置一个端点，使我们的 AngularJS 应用能够发送 HTTP 请求。我们已经尽可能地将后台接口设计为“遵循 RESTful”规范。因此，我们的后端就是一个 REST Web 服务。

在此处，我们利用用户故事定义命令：

> 作为用户 Michael，我想要能够在中央服务器上保存数据，以便能够从多个终端检索到这些数据。

#### 使用已下载的项目

为了测试本节中的代码，您可以使用从出版商网站下载的配套项目目录 `ch04_03_http/app` 来完成此任务。请将当前工作目录切换至上述路径，并从那里启动 `http-server` 服务以搭建测试环境。

#### BookMonkey 后端

在此时我们想简要介绍一下后端情况：REST 端点允许操作书籍和标签资源，并使用 JSON 作为数据格式。特别是，我们允许对这些资源发送以下 HTTP 请求，包括 `GET`、`POST`、`PUT` 和 `DELETE` 操作：

```javascript
// books resource（books 资源）

GET /api/books              // get all books                 // 获取所有图书
POST /api/books             // create a new book            // 创建新图书
GET /api/books/:isbn        // get a book by isbn           // 根据 ISBN 检索某本书
PUT /api/books/:isbn       // update the book with specified isbn // 使用指定 ISBN 更新该书
DELETE /api/books/:isbn    // delete the book              // 删除拥有特定 ISBN 的书

// tags resource（标签资源）

GET /api/tags               // get all tags                  // 获取所有标签
```

得益于这一定义接口，我们可以描述 `BookDataService` 所提供的基本 CRUD（增删改查）操作。例如，通过 `GET /api/books` 可以获取一个图书对象数组；另一方面，`POST /api/books/:isbn` 返回单个书籍对象；同时，`POST` 和 `PUT` 方法的后端会接收 `Book` 对象作为参数，用于创建或者更新资源。删除书籍的请求 `DELETE /api/books/:isbn` 将按预期进行处理，无需用户干预。

#### 通过 `$http` 服务进行 HTTP 通信

为了在应用程序运行时使用 HTTP 异步重新加载单页应用数据，浏览器需要使用所谓的 `XMLHttpRequest` 对象。底层程序模型被称为 AJAX（异步 JavaScript 和 XML）。不建议直接使用 `XMLHttpRequest` 对象，因为你仍然需要编写一些代码并处理跨浏览器问题。使用 AJAX 的最佳方式是通过像 jQuery 这样的库，它为 `XMLHttpRequest` 提供了一个封装。

AngularJS 还包含一个大大简化了 HTTP 请求发送的组件：`$http` 服务。它是你处理 AJAX 的最佳选择，因为它确保在接收到 HTTP 响应后，任何作用域操作都会触发脏检查。`$http` 服务 API 基于所谓的 promise。

promise 代表一个异步操作最终到达的结果，它在很大程度上是你能够轻松使用异步 API 的关键。它尤其让你不会在“回调忙乱”中迷失方向，并避免所谓的“回调地狱”。我们将在第 7 章“常见问题”中提供相关的背景信息。

如果 `$http` 服务只包含一个函数，你可以指定一个 HTTP 请求来调用这个 `$http()` 函数。该函数将期望一个描述如何构建 HTTP 请求的配置对象作为参数。以下属性是此配置对象最重要的属性：

- `method`：将 HTTP 方法指定为字符串，例如“GET”或“POST”。
- `url`：指定要请求的绝对或相对 URL。
- `data`：应与请求一起发送的用户数据。该服务自动处理从 JSON 的反序列化和序列化。
- `headers`：一个描述应发送哪些 HTTP 头的对象。

除了核心属性之外，还有其他属性可用于配置 HTTP 请求的某些方面。你可以在 `$http` 服务的官方 API 文档 <http://docs.angularjs.org/api/ng.$http> 中找到完整的概述。

例如，为了调用后端的 `books` 资源，相应的 `$http()` 调用如下所示：

```javascript
$http({
    method: 'GET',
    url: 'http://localhost:4730/api/books'
});
```



`$http`调用的输出总是一个 promise。这意味着在我们的完整应用程序中，我们可以传递这个 promise，并为所有对此 HTTP 请求感兴趣的组件注册一个回调函数。我们稍后将在设计`BookDataService`后看到如何做到这一点。

该框架提供以下帮助函数：

- `$http.get()`
- `$http.head()`
- `$http.post()`
- `$http.put()`
- `$http.delete()`
- `$http.jsonp()`

例如，你可以使用以下代码简化对 books 资源的检索：

```javascript
$http.get('http://localhost:4730/api/books');
```

#### 首先是测试

我们已经一再提到，AngularJS 从一开始就考虑了可测试性。除了用于 E2E 测试的 ngScenario DSL 和 ngMock 模块的`module()`和`inject()`基础函数外，为此属性提供的模拟实现也特别重要。

在本节中，我们将重点介绍这些模拟对象之一，即`$httpBackend`模拟对象。背景是`$http`服务使用`$httpBackend`对象来执行实际的 HTTP 请求。在单元测试中，你通常用`$httpBackend`模拟对象替换这个`$httpBackend`对象，以避免向服务器发送实际请求，并使你能够定义自己的响应。此外，`$httpBackend`模拟对象允许你设定期望，以确保组件在生产环境中执行时确实会执行某些请求。这些就是所谓的请求期望。通过这种方式，你可以轻松测试与后端通信的组件。

我们的`BookDataService`就是这样一个组件。因此，我们现在将修改文件`book_data.spec.js`中现有的测试套件，以指定我们期望的 HTTP 请求以及何时调用`BookDataService`的 API 函数。为了设定请求期望，我们将使用`$httpBackend`模拟对象。我们不会详细描述所有测试用例。相反，我们将选择一个测试用例来展示我们如何使用`$httpBackend`模拟对象轻松设置预定义响应并设定请求期望。

接下来，我们必须使用依赖注入注入`$httpBackend`模拟对象。我们将模拟对象分配给局部变量`$httpBackend`，以便所有对`beforeEach()`、`afterEach()`以及`describe()`或`it()`的调用都可以访问它。在此阶段我们不需要做任何事情来实际获取模拟对象，因为我们已经在单元测试的 Karma 配置（`karma.conf.js`）中包含了文件`angular-mocks.js`和`angular.js`。对于单元测试，`$httpBackend`对象将被`$httpBackend`模拟对象覆盖。

##### 代码清单 4.40：新版本 BookDataService 测试套件的 beforeEach 块

```javascript
describe('Service: BookDataService', function () {

  // just to match the baseUrl in the service

  var baseUrl = 'http://localhost:4730';

  var BookDataService, $httpBackend;

  // load the application module

  beforeEach(module('bmApp'));

  // get a reference to all used services

  beforeEach(inject(function (_BookDataService_, __$$httpBackend__) {

    BookDataService = _BookDataService_;

    $httpBackend = _$$httpBackend_;

  }));

  [...]

});
```

在最后一个`beforeEach()`块中，我们为`$httpBackend`模拟对象设置一些预定义的 HTTP 响应（参见代码清单 4.41）。为此，我们使用`$httpBackend`模拟对象的`when()`函数。因此，如果`$http`服务在执行单元测试期间向`baseUrl` + `/api/books`发送 HTTP GET 请求，`$httpBackend`组件将使用我们的测试 Book 对象数组（`testBooks`）进行响应。这个测试数组包含我们经常使用的三本书。

通过这种方式，我们为单元测试期间提交的每个 HTTP 请求设置了预定义响应。重要的是，我们至少要为每个将在测试用例中设定请求期望的 HTTP 请求执行此步骤。否则，测试用例中那些没有预定义响应的请求将失败，并显示消息“No response defined!”（未定义响应！）。

## 清单 4.41：预定义 HTTP 响应的定义

```javascript
describe('Service: BookDataService', function () {

    [...]

    // 定义已训练的响应

    beforeEach(function() {

        $httpBackend.when(

            'GET', baseUrl + '/api/books'

        ).respond(testBooks);

        $httpBackend.when(

            'GET', baseUrl + '/api/books/' + csBook.isbn

        ).respond(csBook);

        $httpBackend.when(

            'GET', baseUrl + '/api/books/test'

        ).respond(404, '');

        $httpBackend.when(

            'POST', baseUrl + '/api/books'

        ).respond(true);

        $httpBackend.when(

            'PUT', baseUrl + '/api/books/' + csBook.isbn

        ).respond(true);

        $httpBackend.when(

            'DELETE', baseUrl + '/api/books/' + csBook.isbn

        ).respond(true);

    });

    [...]

});
```

在清单 4.42 中，我们首次使用了`afterEach()`块。如你所知，此块在每个测试用例执行完毕后执行一次。在此块中，我们使用`verifyNoOutstandingExpectation()`来在每个测试用例之后检查是否仍存在尚未满足的请求期望。如果情况确实如此，这意味着通过被测试代码发送的一个期望的 HTTP 请求没有被删除。因此，这将导致测试用例失败。

接下来，我们使用`verifyNoOutstandingRequest()`来测试是否仍存在现有的 HTTP 请求。通过这种方式，我们检查相反的情况。是否仍有现有的 HTTP 请求？如果情况确实如此，那么在我们已经制定了期望的请求之后，又提交了额外的请求。我们通常不允许这种情况，因此我们也在每个测试用例之后构建一个`verifyNoOutstandingRequest()`测试。

##### 清单 4.42：BookDataService 测试套件的 afterEach() 块

```javascript
describe('Service: BookDataService', function () {

[...]

    afterEach(function() {

        $httpBackend.verifyNoOutstandingExpectation();

        $httpBackend.verifyNoOutstandingRequest();

    });

[...]

});
```

现在，我们终于可以向你展示一个测试用例，我们将其打印在清单 4.43 中。这是一个用于保存新书的测试用例。其他测试用例将遵循相同的模式。

##### 清单 4.43：用于保存新书的测试用例

```javascript
describe('Service: BookDataService', function () {

    [...]

    describe('Public API usage', function() {

        [...]

        describe('storeBook()', function() {

            it('should properly store the passed book object',

            function() {

                $httpBackend.expectPOST(

                    baseUrl + '/api/books', effectiveJsBook

                );

                BookDataService.storeBook(effectiveJsBook);

                $httpBackend.flush();

            });

        });

    });

});
```

```javascript
[...]

});

[...]

// 辅助对象

var effectiveJsBook = {

    title : 'Effective JavaScript (German Edition)',

    [...]

};

});
```

制定请求期望时的关键点是调用`expect()`函数。如你在清单 4.43 中所见，对于每种 HTTP 方法（GET、POST 等），都有一个相应的辅助函数，它使你更容易制定请求期望。

因此，在这种情况下，我们期望`BookDataService.storeBook()`函数内部使用`$http`服务向 URL`baseUrl` + `/api/books`提交一个 HTTP POST 请求。此外，我们期望通过此请求，将在局部变量`effectiveJsBook`中定义的用户数据一并发送。

我们不应忘记在函数末尾调用`$httpBackend.flush()`。否则，`afterEach()`块中的`verifyNoOutstandingRequest()`测试将会失败。其原因是实际的`$httpBackend`对象是异步工作的。因此，`$httpBackend`模拟对象也必须遵守这些规则，以避免改变代码执行流程。测试异步代码并不那么简单，需要一些扩展的 Jasmine 构造，如`runs()`和`waitsFor()`。通过使用`flush()`，我们可以确保我们的测试，尽管是异步的，但在单元测试中可以同步执行。通过这个调用，我们可以在测试中设置返回相应 HTTP 响应的时间点，从而模拟来自服务器的响应。

通过`$httpBackend`模拟对象，你可以轻松地测试你的 AngularJS 应用程序。

我们将剩余测试用例的适配留作练习供你完成。或者，你可以打开随书附带的压缩包中文件`book_data.spec.js`的新版本。

#### 在 BookDataService 中使用 $http

在上一节中，我们调整了`BookDataService`的单元测试，以便当其 API 函数被调用时，它会向我们的后端发送 HTTP 请求。现在，我们想要更新新的实现以满足这些规范。

因此，我们将确保，此时，我们必须进行一次 API 破坏性更改。我们很快就会明白为什么我们必须这样做。

如清单 4.44 所示，我们让`$http`服务通过依赖注入传入，以便我们可以使用此服务发送 HTTP 请求。此外，我们必须稍微调整一下返回的 API 对象。在新版本中，所有 API 函数基本上都返回某些内容。这也是为什么我们的 API 与之前的版本相比发生了破坏性更改。之前的 API 调用直接返回本地可用的数据。相比之下，现在每个访问都与一个 HTTP 请求相关联，并且这个过程是异步发生的，因此我们以最优雅的方式处理它，即直接返回提供相应`$http`调用的 promise。这样，`BookDataService`的调用者（例如，所有控制器）可以决定当 HTTP 响应从服务器到达时应该发生什么。更重要的是，调用者可以决定如果收到错误响应应该发生什么。

##### 清单 4.44：BookDataService 的新 API 对象

```javascript
bmApp.factory('BookDataService', function($http) {

    [...]

    // 公共 API

    return {

        getBookByIsbn: function(isbn) {

            return srv.getBookByIsbn(isbn);

        },

        getBooks: function() {

            return srv.getBooks();

        },

        getTags: function() {

            return srv.getTags();

        },
```

```javascript
},

storeBook: function(book) {

    return srv.storeBook(book);

},

updateBook: function(book) {

    return srv.updateBook(book);

},

deleteBookByIsbn: function(isbn) {

    return srv.deleteBookByIsbn(isbn);

}

};

}});
```

清单 4.45 展示了读操作的实现。正如预期的那样，这些实现进行了破坏性更改，因为我们只是使用`$http`向服务器发送一个请求，并返回生成的 promise。通过这种方式，我们将所有 API 调用定向到我们在 REST Web 服务中可用的相应资源。

## 清单 4.45：读取访问被转换为使用 HTTP GET 请求

```javascript
bmApp.factory('BookDataService', function($http) {

    var srv = {};

    srv._baseUrl = 'http://localhost:4730';

    // 服务实现

    srv.getBookByIsbn = function(isbn) {

        return $http.get(

            srv._baseUrl + '/api/books/' + isbn

        );

    };

    srv.getBooks = function() {

        return $http.get(

            srv._baseUrl + '/api/books'

        );

    };

    srv.getTags = function() {

        return $http.get(

            srv._baseUrl + '/api/tags'

        );

    };

}];
```

那么写操作呢？自然，我们也按照清单 4.46 所示处理写操作。这里同样，API 调用将简单地被定向到相关的 REST 端点。我们像以前一样返回生成的 promise，以便调用者可以决定如何处理 HTTP 响应。

##### 清单 4.46：写操作使用 HTTP POST/PUT/DELETE 请求处理

```javascript
bmApp.factory('BookDataService', function($http) {

    var srv = {};

    srv._baseUrl = 'http://localhost:4730';

    // 服务实现

    srv.storeBook = function(book) {

        return $http.post(

            srv._baseUrl + '/api/books', book

        );

    };

    srv.updateBook = function(book) {

        return $http.put(

            srv._baseUrl + '/api/books/' + book.isbn, book

        );

    };

    srv.deleteBookByIsbn = function(isbn) {

        return $http.delete(

            srv._baseUrl + '/api/books/' + isbn

        );

    };

    [...]

});
```



经过修订后，我们的`BookDataService`看起来非常简洁，因为我们只在相关的 HTTP 请求中设计了 API 函数。然而，这些更改对我们的应用程序功能产生了深远的影响。

当我们执行单元测试时，针对`BookDataService`修改后的测试用例现在应该“变绿”（通过）。但是，我们`tokenfield`指令的测试用例将会失败，因为该指令——像`BookDataService`的所有其他使用者一样——并不期望我们的服务现在返回 promise。

通过这一改动，我们确实对大量的端到端测试进行了重大调整。

## 修复应用

由于我们在上一节中对`BookDataService`所做的更改，我们的应用程序在很大程度上已经无法正常工作。然而，很明显这是因为所有`BookDataService`的调用者还不知道如何处理返回的 promise。

在本节中，我们将展示调用者应如何处理基于 promise 的`BookDataService` API，以恢复应用程序的功能。我们不会讨论每个组件中所有必要的更改。相反，我们将通过两个示例来展示如何让相关组件重新运作起来。

特别说明，我们将不描述失败的测试用例。在本书附带的 zip 文件中，我们已经解决了项目中所有现存的问题。

基于我们现在展示的两个示例，你应该知道需要对调用组件进行哪些更改，以使整个应用程序再次运行起来。

> 我们假设你已经了解了 promise。如果不是这样，你可以回顾第 7 章 “常见问题解答” 中必要的信息。

### 修复编辑功能

我们必须在调用`BookDataService` API 函数的地方进行必要的更改。作为示例，我们选择了如清单 4.47 所示的`AdminEditBookCtrl`控制器，因为那里需要进行最多的更改。

具体来说，它处理对`getBookByIsbn()`函数的调用。以前，这个函数直接返回相关的`Book`对象。从现在起，我们可以将数据赋值给作用域变量`book`。我们可以这样做是因为这个函数现在返回一个 promise。为了能够响应 HTTP 响应的到达，promise 为我们提供了`then()`函数。

该函数的第一个参数是所谓的成功函数，当 promise 被解析（resolved）时执行。因此，我们包含了来自服务器的成功的 HTTP 响应。这个函数包含一个代表 HTTP 响应的`Response`对象作为参数。使用该对象，我们可以特别通过访问`data`属性来包含接收到的用户数据。如果这里的用户数据来自一个`Book`对象，我们可以在成功函数中直接将`res.data`赋值给作用域变量`book`。

我们可以向`then()`函数传递第二个参数。第二个参数是一个错误函数，当 promise 被拒绝（rejected）或在 HTTP 请求过程中及请求期间发生错误时被调用。错误函数包含一个`Error`对象作为参数，该对象告诉我们哪里出了问题。在这种情况下，我们只是在控制台上显示错误。当然，我们可以在这里编写更智能的错误处理器。

#### `$http`服务中的 Promises

当 HTTP 响应包含 200 到 299 之间的状态码时，`$http`服务会解析 promise。对于 HTTP 重定向，服务会透明地跟随重定向，而不解析或拒绝 promise。在所有其他情况下，promise 都会被拒绝。

##### 清单 4.47：调用`getBookByIsbn()`函数时对`AdminEditBookCtrl`控制器的必要更改

```javascript
bmApp.controller('AdminEditBookCtrl',

function ($scope, $routeParams, $location, BookDataService) {

    $scope.isEditMode = true;

    $scope.submitBtnLabel = 'Buch editieren';

    var isbn = $routeParams.isbn;

    BookDataService.getBookByIsbn(isbn).then(function(res) {

        $scope.book = res.data;

    }, function(error) {

        console.log('An error occurred!', error);

    });

    [...]

});
```

在清单 4.48 中调用`updateBook()`函数时，我们必须完全这样做。我们不能在调用`updateBook()`后直接调用`goToAdminListView()`函数。相反，只有当服务器成功响应并且相应的书籍也已在服务器上更新后，我们才能首先进行此调用。

##### 清单 4.48：调用`updateBook()`函数时在`AdminEditBookCtrl`控制器中的必要更改

```javascript
bmApp.controller('AdminEditBookCtrl',

    function ($scope, $routeParams, $location, BookDataService) {

        [...]

        $scope.submitAction = function() {

            BookDataService.updateBook($scope.book).then(function() {

                goToAdminListView();

            }, function(error) {

                console.log('An error occurred!', error);

            });

        };

        $scope.cancelAction = function() {

            goToAdminListView();

        };

        var goToAdminListView = function() {

            $location.path('/admin/books');

        };

    });
```

目前，这就是我们为了让书籍编辑视图再次工作所需做的一切。

### 修复 tokenfield 指令

除了`AdminEditBookCtrl`控制器外，我们还想看看`tokenfield`指令，因为异步操作在该组件中有双重影响。

如你所知，`tokenfield`指令依赖于`BookDataService`来访问系统中所有可用的标签，以填充 tokenfield 插件的自动完成功能。由于现在`getTags()`函数返回一个 promise，我们只能在成功函数中执行 tokenfield 插件的实际初始化，此时我们已经用服务器返回的标签填充了数组，如清单 4.49 所示。为了更好地组织源代码，我们为初始化程序定义了本地函数`initializeTokenfield`。我们在成功函数中调用此函数，并将仅存在于`tags`数组中的服务器返回的用户数据传递给它。

##### 清单 4.49：在 tokenfield 指令中调用`getTags()`时的必要更改

```javascript
bmApp.directive('tokenfield', function(BookDataService) {

    return {

        [...]

        link: function(scope, elem) {

            var initialized = false;

            // Fetch the tags from the server

            // and initialize directive.

            BookDataService.getTags().then(function(res) {

                initializeTokenfield(res.data);

            }, function(error) {

                console.log('An error occurred!', error);

            });

            // Main initialization routine

            function initializeTokenfield(tokens) {

                elem.tokenfield({

                    autocomplete: {

                        source: tokens,

                        delay: 100

                    },

                    [...]

                }).on('afterCreateToken', function (e) {

                    addToken(e.token.value);

                }).on('removeToken', function (e) {

                    removeToken(e.token.value);

                });

                function addToken(token) { [...] }

                function removeToken(token) { [...] }

                [...]

            }

        }

    }

})
```

实际的初始化逻辑现在看起来与之前版本的`tokenfield`指令相似。然而，存在一个差异，这个差异显示在清单 4.50 中。这个差异是`initializeTagsArray()`函数，在上一节中它被称为`init()`。

##### 清单 4.50：tokenfield 指令中的必要更改

```javascript
initializeTagsArray();
```

该指令现在必须处理这样一个事实：来自父作用域（例如，`AdminEditBookCtrl`控制器的作用域）的`Book`对象（我们可以通过双向绑定的引用`scope.tokenfield`获得）也是从服务器异步加载的。因此，我们必须注册一个一次性观察者（one-time watcher），以防`Book`对象尚不可用。回想一下，我们在颜色选择器中也使用了观察者来接收作用域变量更改的通知并能够做出响应。如果`scope.tokenfield`仍然未定义，这里我们几乎以相同的方式进行：我们使用`scope.$watch()`注册一个观察者。然而，我们不想一直监听`scope.tokenfield`的更改，只想监听到作用域变量`book`被赋值为止。因此，我们将这种模式称为一次性观察者。使用`initialized`标志，我们可以确保只有在`Book`对象最终可用时才执行令牌分配。

如果`Book`对象已经可用，在调用`initializeTagsArray`函数之前，我们必须检查`tags`数组是否已存在（例如，编辑）或仍然需要创建（例如，创建新书）。

完成这些更改后，我们让`tokenfield`指令重新工作了。

## BookMonkey 与后端通信

由于我们已经努力确保所有调用`BookDataService` API 函数的组件再次工作，我们现在可以运行整个项目。为此，我们必须使用以下控制台命令启动服务器：

```bash
node server.js
```

此外，我们必须确保使用正确的服务器 URL。

```javascript
srv._baseUrl = 'http://localhost:4730';
```

和之前一样，我们使用`http-server`模块来部署我们的 AngularJS 应用程序。这导致我们的应用程序通过向服务器发送 HTTP 请求来处理所有数据访问。我们可以通过在 Chrome 的 Network 标签页中查看执行情况来了解这一点。我们的应用程序发送到后端的 HTTP 请求应该会列在那里（参见图 4.14）。

![img/7a003218cea01579a50512a6c0e40f28_235_0.png](img/7a003218cea01579a50512a6c0e40f28_235_0.png)

#### 图 4.14：Chrome 中的 Network 标签页

## 总结

-   你可以使用`$http`服务轻松地与 REST Web 服务进行通信。
-   除了`$http()`基本函数外，该服务还提供了与特定 HTTP 方法（GET、POST 等）对应的帮助函数。这些帮助函数是`$http.get()`、`$http.post()`等等。
-   `$http`服务总是返回一个 promise，调用者可以使用`then()`函数注册成功或错误函数作为回调函数。
-   使用 promise，你可以优雅地处理异步操作。
-   依赖于`$http`服务的应用程序代码易于测试，因为 AngularJS 在`ngMock`模块中提供了`$httpBackend`模拟对象。
-   使用这个模拟对象，你可以制定请求期望并设置预定义的 HTTP 响应。

# 第五章

## 项目管理与自动化

软件开发并非易事。有许多挑战需要开发者的全神贯注。重复单调的任务可能导致粗心的错误，并减慢开发过程。因此，利用自动化来快速且最重要的是稳定地生产成果是有意义的。近年来，已经开发了许多工具来完成任务并解决 JavaScript 开发领域的问题。这些工具除了其他功能外，还管理客户端依赖项、自动化重复任务、生成源代码矩阵并提供自动测试环境。在本章中，我们将介绍各个工具，并探讨 Project Yeoman，一个为 Web 开发提供预定义工作流程的项目。

## Node.js：工具的运行时环境

我们将再次使用 Node.js 作为本章介绍的工具的运行时环境。我们的 BookMonkey 应用程序就使用了 Node.js。该平台还为`http-server`模块和 Karma 提供了运行时环境。

Node.js 是一个基于 Google V8 JavaScript 引擎的平台。它在服务器端执行 JavaScript 源代码。它的一个主要优势是具有非阻塞的事件驱动 I/O 模型，允许你编写轻量且高效的应用程序。Node.js 安装程序可以从其官方网站下载：

http://nodejs.org

### 使用 npm 进行包管理

在前端 Web 开发领域已经开发了许多非常有用的包和工具，你现在可以在 Node.js 平台上编写 JavaScript 应用程序。为了管理这些包，该平台提供了 npm（Node.js 包管理器）。npm 是一个用于搜索、管理、安装和卸载包的命令行工具。目前，在其官方注册表 https://npmjs.org 上有超过 50,000 个可用的包。

> **给有 Ruby 经验的开发者的说明**
>
> npm 与 Ruby 世界中流行的工具 gem 非常相似。使用 gem，你可以从在 Ruby gems 注册表中管理的庞大选择中挑选包。Ruby gems 的网站是 http://rubygems.org。

Node.js 模块包含一个名为`package.json`的数据文件。除了其他信息外，该文件还包含包名、版本号以及对其他包的依赖关系信息。由于应用程序可以定义为 Node.js 模块，你可以使用`package.json`定义对其他包的依赖关系。如清单 5.1 所示，你可以使用`npm init`命令生成此数据文件。该脚本将询问一系列关于配置的问题。

##### 清单 5.1：创建`package.json`文件

```bash
[app] $ npm init

This utility will walk you through

creating a package.json file.

It only covers the most common items,

and tries to guess sane defaults.

See 'npm help json' for definitive

documentation on these fields

and exactly what they do.

Use 'npm install <pkg> --save'

afterwards to install a package and

save it as a dependency in the package.json file.

Press ^C at any time to quit.

name: (app) bookMonkey

version: (0.0.0) 1.0.0

description: Example Application

git repository:

keywords: javascript angularjs

author: Robin Boehm, Philipp Tarasiewicz

license: (BSD-2-Clause) MIT

About to write [...]
```

```json
{
  "name": "bookmonkey",
  "version": "1.0.0",
  "description": "Example Application",
  "main": "index.js",
  "scripts": {
```



```json
"test": "echo \"Error: no test specified\" && exit 1"

},

"author": "Robin Boehm, Philipp Tarasiewicz",

"license": "MIT",

"dependencies": {},

"devDependencies": {},

"keywords": [

"javascript",

"angularjs"

]

}

```

要向项目添加依赖项，请使用`npm install {packagename}`命令。使用附加参数`--save`，你可以自动将你的应用程序依赖项输入到`package.json`中。借助`--save-dev`，你可以对开发依赖项进行相同的操作。以下示例安装 Node.js 包`http-server`并允许其在你的`package.json`的`devDependencies`下输入。

```bash
npm install http-server --save-dev
```

生成的`package.json`文件如清单 5.2 所示。你可以使用 npm 安装本章中的其他工具。

##### 清单 5.2：已安装包的自动条目

```json
{
  "name": "bookmonkey",
  "version": "1.0.0",
  "description": "Example Application",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Robin Boehm, Philipp Tarasiewicz",
  "license": "MIT",
  "dependencies": {},
  "devDependencies": {
    "http-server": "0.6.1"
  },
  "keywords": [
    "javascript",
    "angularjs"
  ]
}
```

Node.js 使用 CommonJS 模块系统，让你在创建新模块时可以轻松地嵌入现有模块。

#### 总结

- Node.js 是一个在服务器端执行 JavaScript 源代码的平台。所有平台的安装程序都可以从`http://nodejs.org`获取。
- 该平台的主要优势之一是具有非阻塞的事件驱动 I/O 模型。
- 通过 npm，Node.js 带来了一个简化包管理的包管理器。你可以访问其官方注册表中超过 50,000 个包。
- 你已经学习了如何安装 Node.js 模块和依赖项。
- 所有旨在简化 Web 开发过程的现代工具都使用 Node.js 作为运行时环境。

##### 使用 Bower 管理前端依赖项

Bower (`http://bower.io`) 是一个用于管理 Web 前端应用程序依赖项的开源工具。项目特定的依赖项可以轻松地在名为`bower.json`的 JSON 文件中定义。借助命令行中的一个简单命令，所有定义的包都可以加载到相应的项目中。另一方面，也可以在 Node.js 进程中使用 JavaScript API 激活 Bower。

未配置的包存储在名为`bower_components`的目录中。一个包可以包含任何内容并提供 Web 组件。使用 Bower，可以轻松地将 Twitter Bootstrap、jQuery 以及 AngularJS 等项目嵌入你自己的项目中。包可以通过多种不同方式引用，包括：

- Bower 注册表中的官方注册包
- 一个 Git 仓库
- 一个直接引用 GitHub 的简写形式，例如`angular/angular.js`
- 一个指向`.zip`或`.tar.gz`格式文件的 URL

由于 Bower 使用 Node.js 作为其运行时环境，你需要使用 npm 安装 Bower。你应该将 Bower 安装为全局包，以便你可以从系统中的任何位置使用它。你可以使用以下命令实现此目的。

```bash
npm install -g bower
```

###### 定义 bower.json 文件

你可以在`bower.json`文件中定义包特定于 Bower 的信息。除了依赖项的定义外，它还包含有关项目名称、版本号和描述的信息。你不必自己创建此文件；你可以使用`bower init`命令交互式地生成文件。如清单 5.3 所示，你可以在命令行中调用此命令。然后它将询问一系列问题。你的答案将用于创建一个初始的`bower.json`文件。在你回答完所有问题后，你将得到一个生成的配置形式的输出。如果你对最后一个问题（"Looks good?"）回答 yes，当前目录中将创建一个具有相应内容的`bower.json`文件。

### 清单 5.3：使用 bower init 生成 bower.json 文件

```text
[my-angular-project] $ bower init

[?] name: my-angular-project

[?] version: 1.0.0

[?] description: Sample project for the bower chapter

[?] main file: path/to/app.js

[?] keywords: angularjs, bower, book, example

[?] authors: Robin Böhm, Philipp Tarasiewicz

[?] license: MIT

[?] homepage: http://www.angularjs.de

[?] set currently installed components as dependencies? Yes
```

# 定义依赖项

此文件实际的主要任务是通过`dependencies`属性来定义项目的外部依赖。此外，依赖项可以列在`devDependencies`属性中，以表明它们仅在开发期间需要，不属于最终交付物的一部分。使用`bower install {packagename}`命令，您可以安装单个包。您可以使用`bower install angular`来安装 AngularJS。如清单 5.4 所示，您可以使用`--save`或`--save-dev`参数将已安装的包自动添加到现有的`bower.json`配置文件中。

**清单 5.4：安装外部依赖项**

```bash
bower install angular --save

bower install angular-route --save

bower install angular-mocks --save-dev
```

执行此命令后，我们的`my-angular-project`项目生成的`bower.json`将包含对`angular`和`angular-route`包的依赖。此外，`angular-mocks`包将作为开发依赖项（`dev-dependencies`）提供。使用`search`参数，您可以通过对命令行进行全文搜索来查询 Bower 注册表。或者，您也可以通过访问其网站`http://sindresorhus.com/bower-components`来搜索注册表。要从本项目中删除一个包，可以使用`bower uninstall angular`。我们当前`bower.json`文件的一部分如清单 5.5 所示。

**清单 5.5：bower.json 文件的结构**

```json
{
  "name": "my-angular-project",
  "version": "1.0.0",
  "dependencies": {
    "angular": "1.2.3",
    "angular-router": "1.2.3"
  },
  "devDependencies": {
    "angular-mocks": "1.2.3"
  }
}

[...]
```

###### 从特定版本安装包

如果您想使用命令行从特定版本安装一个包，可以在包名后面加上一个井号（`#`）和版本描述。因此，要安装 AngularJS 1.0.0 版本，请使用命令`bower install angular#1.0.0 --save`。它也会被添加到您的配置中。然而，有时也可能希望始终使用存储库的当前开发版本。为此，只需在存储库中提供所需的包即可。

###### 包含已安装的包

如果项目目录包含您的配置文件，您可以使用`bower install`下载配置中定义的所有依赖项。当使用 Git 等版本管理工具时，`bower_components`目录通常不会被导入，该目录也列在 Git 的`.gitignore`文件中。导出项目后，您可以通过执行`bower install`命令以正确的版本重新加载所有必要的包。

安装依赖项后，您可以根据需要实现以下内容。清单 5.6 展示了一个使用`<script>`标签包含依赖项的`index.html`示例。

**清单 5.6：包含由 Bower 安装的包**

```html
<!DOCTYPE html>
<html ng-app>
<head>
  <title>AngularJS.DE Bower Example</title>
</head>
<body>
  <script src="bower_components/angular/angular.js"></script>
  <script src="bower_components/angular-route/angular-route.js"></script>
</body>
</html>
```

###### 配置 Bower

您可以使用`.bowerrc`文件配置 Bower。您可以在项目目录中创建此文件并添加配置，从而为特定项目进行配置。此外，您也可以在用户的主目录中为用户创建全局配置。项目特定的配置会覆盖任何全局参数。在此文件中，您可以设置以下配置参数：

- `directory`。组件的安装位置
- `endpoint`。您自己的 Bower 注册表的定义
- `json`。项目中 Bower 元数据文件的名称
- `searchpath`。其他 Bower 注册表的列表
- `shorthand_resolver`。简写形式的模板

清单 5.7 展示了一个`.bowerrc`文件示例。

**清单 5.7：.bowerrc 文件的结构**

```json
{
  "directory": "bower_components",
  "endpoint": "https://bower.mycompany.com",
  "json": "myOwnBower.json",
  "searchpath": [
    "https://bower.herokuapp.com"
  ],
  "shorthand_resolver": "git://example.com/organization/package.git"
}
```

要在官方 Bower 注册表中注册您自己的包，您需要一个公开可用的 Git 存储库。该存储库必须在主目录中包含一个有效的`bower.json`文件，并且该文件必须包含包所需的元数据。在这种情况下，您必须确保将包的不同版本描述为 Git 标签，并且它们符合语义化版本控制（`http://semver.org`）。满足要求后，您可以使用清单 5.8 中的命令在公共注册表中注册该包。

**清单 5.8：在 Bower 注册表中注册一个包**

```bash
bower register <my-package-name> <git-endpoint>
```

目前还无法独立地从公共注册表中删除已注册的包。目前，这通过 Bower 项目在 GitHub 上的问题跟踪器中的条目来管理，但这种方式并不优雅。不过，很可能在不久的将来会有新的机制来解决这个问题。

###### 创建私有注册表

并不总是希望将包发布到外部的公共存储库中。幸运的是，您可以使用`endpoint`配置参数在私有注册表中注册一个包。为此，您必须创建自己的注册表。这可以相对轻松地完成。该注册表应用程序是一个非常简单的 Ruby 程序，可以从这个 URL 在 GitHub 上下载：

```text
https://github.com/bower/registry
```

其他公共和替代注册表可以使用`searchpath`配置参数来定义。您可以在数组中列出多个注册表（参见清单 5.9）。

**清单 5.9：带有自定义 endpoint 的 .bowerrc**

```json
{
  "endpoint": "https://bower.mycompany.com",
  "searchpath": [
    "https://bower.herokuapp.com",
    "https://bower.anothercompany.com"
  ]
}
```

###### 代理服务器的潜在问题

如果您需要在代理服务器后面运行 Bower，可以通过使用`HTTP_PROXY`和`HTTPS_PROXY`环境变量来通过代理服务器重定向网络通信。公司网络中经常出现的一个问题是全公司范围的防火墙会阻止用于 SSH 通信的端口 22。由于 Bower 注册表中的许多存储库都使用 SSH，因此问题很快就会出现。为了绕过这些问题，您可以配置 Git，使所有 SSH 通信都通过 HTTP 或 HTTPS 自动重定向。您可以使用此 Git 命令：

```bash
git config url."http://".insteadOf git://
```

#### 总结

- Bower 是一个用于管理前端依赖项的工具。Bower 基于 Node.js。
- 您可以在名为`bower.json`的 JSON 文件中定义项目特定的依赖项。您可以使用`bower init`命令交互式地生成此文件。此外，您可以在命令行中使用命令`bower install {packagename}`安装新的依赖项。要卸载一个包，请使用命令`bower uninstall {packagename}`。
- Bower 区分项目依赖项和开发依赖项。
- 您可以在`.bowerrc`文件中定义配置，从而使用您自己的公司注册表。
- 可能会出现与代理服务器相关的问题。您可以通过配置 Git 来解决这些问题。

#### 使用 Grunt 自动化任务

Grunt (`http://gruntjs.com`) 是一个开源工具，旨在简化并通常完全消除重复性任务的乏味完成。该工具可自动化以下任务：

- 编译任务
- 代码压缩
- 执行测试
- 执行质量保证工具，例如 JSLint (`http://www.jslint.com`)

要使用 Grunt，您需要 Node.js 0.8 或更高版本以及 npm 包管理器。使用 Grunt 的典型项目构建包含一个`package.json`文件，该文件定义了一个 Node.js 模块。您使用此文件来定义对项目所需的 Node.js 模块的依赖。由于 Grunt 也是一个 Node.js 模块，您可以在项目中使用以下命令安装它：

按照以下命令操作，并在`package.json`文件中将其指定为开发依赖项：

```bash
npm install grunt --save-dev
```

> **初始化 package.json 文件**
>
> 你可以使用`npm init`命令为你的项目生成一个`package.json`文件。关于此功能的详细描述，请参阅“Node.js：工具的运行时环境”一节。

#### 通过命令行使用 Grunt

一个名为`grunt-cli`的 Node.js 模块可以使使用 Grunt 更容易。该模块允许你从命令行使用 Grunt 命令。执行的脚本会在本地项目目录中查找已安装的 Grunt 包，并将命令行的调用委托给该位置。这种委托很重要，因为不同项目需要不同版本的 Grunt。因此，不建议全局安装 Grunt。你可以使用此命令安装 Grunt。（有时需要管理员权限！）

```bash
npm install -g grunt-cli
```

安装后，Grunt 在系统范围内都可用。如果现在在新项目中运行 Grunt 命令，你将收到如清单 5.10 所示的错误消息。如果看到此消息，请不要惊慌。你只是忘记了在当前项目中安装 Node.js 模块`Grunt`。

##### 清单 5.10：使用 Grunt-CLI 时可能出现的错误消息

```text
[app] $ grunt

grunt-cli: The grunt command line interface. (v0.1.9)

Fatal error: Unable to find local grunt.

If you're seeing this message, either a Gruntfile

wasn't found or grunt hasn't been installed

locally to your project. For more information about

installing and configuring grunt,

please see the Getting Started guide:
```



> http://gruntjs.com/getting-started

## 配置任务

要配置 Grunt 应为你执行的任务，请在`Gruntfile.js`文件中使用脚本。Grunt 期望你在此脚本中将函数作为 CommonJS 模块导出。在此函数中，你可以配置所有你希望 Grunt 自动执行的任务。这样做的时候，Grunt 会执行导出的函数，并将其委托给你可以访问的所谓的 Grunt API。此时，你应该确保 JavaScript 源代码包含在`Gruntfile.js`文件中，并且不包含 JSON 格式的配置（如在`package.json`中）。

### 清单 5.11：Gruntfile.js 文件的基本结构

```javascript
module.exports = function (grunt) { 

// do some stuff

};
```

> 面向 CoffeeScript 开发者的说明

也可以使用 CoffeeScript 创建此定义。但是，配置文件的扩展名必须是`.coffee`。例如，`Gruntfile.coffee`是一个有效的文件名。

## 注册任务

你可以将 JavaScript 函数注册到 Grunt。在 Grunt 的世界里，这样的函数被称为任务。你使用`grunt.registerTask`函数注册任务。此函数需要三个参数。第一个参数提供一个你可以用于检索该函数的名称。第二个参数包含一个描述，当你输入`grunt -help`时会显示。第三个参数指定一个函数，该函数在调用此任务时应执行。清单 5.12 展示了一个非常简单任务的定义。

### 清单 5.12：在 Grunt 中定义你自己的函数

```javascript
module.exports = function(grunt) {

// A very basic default task.

grunt.registerTask('log', 'Log some stuff.', function() {

grunt.log.write('Logging some stuff...');

});

};
```

你可以使用命令行命令`grunt`执行此任务。你需要将应执行的任务名称作为参数指定给`grunt`命令。执行结果如清单 5.13 所示。

### 清单 5.13：使用命令行执行你自己的函数

```shell
[app] $ grunt log

Running "log" task

Logging some stuff...
```

完成，无错误。

> **确定默认任务**

Grunt 中有一个约定，允许你定义一个默认任务，该任务将在不带参数调用 Grunt 时执行。你只需使用`grunt.registerTask`定义一个名为`default`的任务。通常，这将是对一个或多个任务的委托。

你还可以使用`grunt.registerTask`函数注册多个函数。但是，函数应该有唯一的名称，否则它们会相互覆盖。在后一种情况下，你只能访问最近定义的函数。

你可以将参数传递给一个任务。两个参数应使用冒号分隔。清单 5.14 向你展示了如何将参数传递给任务。

### 清单 5.14：使用命令行执行你自己的命令

```shell
[app (master)] $ grunt count

Running "count" task

Arguments: 0
```

完成，无错误。

```shell
[app (master)] $ grunt count:1:2:3

Running "count:1:2:3" (count) task

Arguments: 3
```

完成，无错误。

你还可以使用`grunt.registerTask`函数将多个任务与一个名称关联。在这种情况下，你需要提供两个参数。与之前一样，第一个参数指定任务的名称。第二个参数指定一个包含所需任务名称的数组。你在数组中定义任务的顺序决定了执行顺序。清单 5.15 展示了一个定义了三个任务的`Gruntfile.js`文件。最后一个任务名为`all`，并与前两个任务相关联。

### 清单 5.15：在 Grunt 中定义你自己的函数

```javascript
module.exports = function(grunt) {

  // A very basic log task

  grunt.registerTask('log', 'Log some stuff.', function() {

    grunt.log.writeln('Logging some stuff...');

  });

  // A very basic task with arguments

  grunt.registerTask('count', 'Count given Arguments.', function() {

    grunt.log.writeln('Arguments: ' + arguments.length);

  });

  // An aggregation task

  grunt.registerTask('all', ['log', 'count:a:b']);

};
```

此外，你可以使用`grunt.initConfig()`函数，将一个包含项目特定配置的 JavaScript 对象作为参数传递给任务。清单 5.16 展示了配置`log`任务的示例。你可以使用`grunt.config`方法访问这些配置设置，传递一个 JavaScript 表达式。在这种情况下，它是`grunt.config('log.prefix')`。

### 清单 5.16：配置 Grunt 任务

```javascript
module.exports = function(grunt) {

  grunt.initConfig({

    log: {

      prefix: "LOG"

    }

  });

// A very basic log task with prefix

grunt.registerTask('log', 'Log some stuff.', function() {

    grunt.log.write('[' + grunt.config('log.prefix') + ']');

    grunt.log.writeln('Logging some stuff...');

});

```

## 定义多任务

除了注册简单任务，你还可以使用`grunt.registerMultiTask()`函数注册多任务。多任务是一个可以接收多个已知配置值（称为目标）的任务。如果在执行任务时未定义目标，则将执行此任务注册的所有目标。

在多任务函数中，你可以访问正在执行的目标的名称。你可以使用`this.target`访问一个目标。使用`this.data`，你可以访问附带的数据。你可以通过 API 函数`grunt.initConfig()`以配置对象的形式来包含这些目标的定义。清单 5.17 展示了一个`log`任务，它显示附带参数的数量、当前目标和附带的数据。

### 清单 5.17：在 Grunt 中定义多任务

```javascript
module.exports = function(grunt) {

  grunt.initConfig({

      log: {

        string: 'Logging some stuff...',

        array: [1, 2, 3],

        object: { x: 5 }

      }

  });

  // Register Multi Task

  grunt.registerMultiTask('log', 'Log stuff.', function() {

    grunt.log.writeln('args: '

                      + arguments.length

                      + '\n'

                      + this.target

                      + ': '

                      + this.data);

});

};
```

该示例展示了注册多任务的配置以及多任务本身。为此，我们使用熟悉的`grunt.initConfig()`方法。你可以通过使用配置对象的属性名称来为特定多任务定义目标。此目标的名称对应于所选对象属性的名称，在我们的例子中是`log`。目标定义可以是任何类型的 JavaScript 数据结构。如果你遵循命名约定，由`grunt.initConfig`定义的数据结构将连接到多任务函数中的`this.data`属性。因此，你不必使用`grunt.config`导出此数据，因为你可以直接访问数据结构。在清单 5.18 中，你可以看到使用冒号指定不同目标来检索多任务`log`的情况。也可以在目标选择后使用冒号来包含更多参数。

### 清单 5.18：使用不同目标执行 log 多任务

```shell
[app] $ grunt log

Running "log:string" (log) task

args: 0

string: Logging some stuff...

Running "log:array" (log) task

args: 0

array: 1,2,3

Running "log:object" (log) task

args: 0

object: [object Object]

Done, without errors.

[app] $ grunt log:array

Running "log:array" (log) task

args: 0

array: 1,2,3

Done, without errors.

[app] $ grunt log:array:hello:world

Running "log:array:hello:world" (log) task
```

```text
args: 2

array: 1,2,3
```

完成，没有错误。

通常，一个多任务（multi-task）期望一个 JavaScript 对象来定义特定的配置，然后你可以在多任务函数中使用这些配置。因此，可以定义通用任务。

## Grunt 的替代品：Gulp

除了 Grunt，还有其他使用 Node.js 作为平台的构建工具。其中一种替代方案是 Gulp（https://github.com/gulpjs/gulp）。Gulp 令人印象深刻，因为它的配置非常简单。这是因为后者可以通过流插入非常容易地用 JavaScript 代码来描述。它是一个非常年轻的项目；尽管如此，它仍然值得研究。

## 任务外包

使用 Grunt，你可以将任务外包给不同的文件。你所要做的就是在需要时在你的 Grunt 文件中加载这些任务。实现这一功能的命令是`grunt.loadTasks`。使用这个命令，你可以提供一个任务目录的路径，该路径将被搜索以查找 JavaScript 文件。

让我们将我们的多任务函数`log`转移到一个名为`log`的目录中。在这种情况下，文件名并不重要，因为 Grunt 会搜索整个目录。唯一的要求是文件名必须有`.js`扩展名。此文件的内容在清单 5.19 中给出。

### 清单 5.19：将日志任务转移到外部文件

```javascript
module.exports = function(grunt) {

  // Register Multi Task

  grunt.registerMultiTask('log', 'Log stuff.', function() {

    grunt.log.writeln('args: '

                     + arguments.length

                     + '\n'

                     + this.target

                     + ': '

                     + this.data);

  });

};
```

清单 5.20 展示了一个包含语句`grunt.loadTasks('log')`的 Grunt 文件。通过这样，你可以搜索`log`目录并加载多任务的定义。使用`grunt.initConfig`，你可以像往常一样定义不同的任务。使用这种机制，你可以构建通用的、可重用的模块。在 Grunt 的世界里，这些特殊的模块被称为插件。

### 清单 5.20：从外部文件加载任务

```javascript
module.exports = function(grunt) {

    grunt.loadTasks('log');

    grunt.initConfig({

        log: {

            string: 'Logging some stuff...',

            array: [1, 2, 3],

            object: { x: 5 }

        }

    });

};
```

## 加载 Grunt 插件

你可以使用 npm 来注册 Grunt 插件并使其公开可用。你和其他开发者也可以安装这些已发布的插件，并将它们添加到`package.json`文件中。这将允许你定义一个 Node.js 模块及其依赖项。就像你将 Grunt 安装为一个模块一样，你现在可以使用 npm 安装 Grunt 插件。

清单 5.21 展示了在安装了两个 Grunt 插件`contrib-copy`和`contrib-uglify`之后的一个示例`package.json`文件。两者都列在`devDependencies`下。

### 清单 5.21：将 Grunt 插件作为依赖项的 package.json 文件结构

```json
{

    [...]

}

"devDependencies": {

  "grunt": "0.4.1",

  "grunt-contrib-copy": "0.4.1",

  "grunt-contrib-uglify": "0.2.7"

}

[...]

}
```

在 npm 上有很多可用的 Grunt 插件。你可以通过官方网站 http://gruntjs.com/plugins 上的“plugins”选项卡阅读这些插件的描述。

你可以使用函数`grunt.loadNpmTasks`来加载通过 npm 安装的 Grunt 插件。正如你在清单 5.22 中看到的，你只需要将已安装插件的名称作为参数添加即可。

### 清单 5.22：加载 Node.js Grunt 插件

```javascript
module.exports = function(grunt) {

  [...]

  grunt.loadNpmTasks('grunt-contrib-uglify');

  grunt.loadNpmTasks('grunt-contrib-clean');

  [...]

};
```

就像你自己的任务一样，该任务的配置通过一个你提供给`grunt.initConfig`函数的 JavaScript 对象来完成。我们不会在这里讨论这两个插件的配置细节。但是，你可以在清单 5.23 中看到一个小的示例配置。

### 清单 5.23：Grunt 插件的配置示例

```javascript
module.exports = function(grunt) {

  grunt.initConfig({

    uglify: {

      build: {

        src: 'src/app.js',

        dest: 'build/app.min.js'

      },

    },

    clean: ['build/**/*'],

    }

});

grunt.registerTask('build', ['clean', 'uglify']);

};
```

在此配置的最后，你使用`grunt.registerTask`函数创建了一个名为`build`的新任务。这将按照正确的顺序执行`clean`和`uglify`任务。如果你在命令行中使用`build`参数调用 Grunt，你将得到清单 5.24 中打印的结果。

### 清单 5.24：执行示例配置

```shell
[app] $ grunt build

Running "clean:dist" (clean) task

Running "uglify:build" (uglify) task

File "build/app.min.js" created.

Done, without errors.
```

## 使用模板

你可以在 Grunt 中使用一个小的模板机制。在 Grunt 的上下文中，模板是以`<%`开头并以`%>`结尾的字符串。在两者之间，你可以使用模板变量，这些变量对应于对象访问表达式以访问对象属性。后者非常依赖于你在 JavaScript 中使用的表示法。让我们扩展我们的示例，并在配置对象中定义一个`pkg`属性。该属性分配一个对象，其中包含我们应用程序的一些数据。清单 5.25 通过模板展示了我们`uglify`任务的扩展配置。

### 清单 5.25：使用模板

```javascript
module.exports = function(grunt) {

    grunt.initConfig({

        pkg: {

            name: 'app',

            version: '0.0.1'

        },

        uglify: {

            build: {

                src: 'src/<%= pkg.name %>-<%= pkg.version %>.js',
```



```javascript
dest: 'build/<%= pkg.name %>-<%= pkg.version %>.min.js'

},

clean: ['build/**/*'],

}

});

grunt.registerTask('build', ['clean', 'uglify']);

});

```

为了减少冗余，你可以在 Grunt 中访问`package.json`文件并分配其属性的内容。清单 5.26 展示了这一点。Grunt 提供了一个`grunt.file.readJSON`函数来帮助你完成此任务，这是一件好事。

### 清单 5.26：将文件作为配置对象导入

```javascript
module.exports = function(grunt) {

  grunt.initConfig({

    pkg: grunt.file.readJSON('package.json'),

    uglify: {

      build: {

        src: 'src/<%= pkg.name %>-<%= pkg.version %>.js',

        dest: 'build/<%= pkg.name %>-<%= pkg.version %>.min.js'

      },

    clean: ['build/**/*'],

    }

  });

  grunt.registerTask('build', ['clean', 'uglify']);

};

```

因此，你可以将项目特定的信息集中定义在一个地方，即`package.json`文件中，这比所有信息分散在项目中要容易得多。

### 适用于开发的合适包

接下来，我们想讨论一些在 AngularJS 开发中几乎总是必不可少的公共 Grunt 插件。在实践中，有几个 Grunt 插件可以插入到几乎每个程序中。

#### `load-grunt-tasks`

在加载第一个包之后，你很快就会遇到重复的行，除了`loadNpmTasks`语句，这使得配置难以理解。为了解决这个问题，你可以使用一个名为`load-grunt-tasks`（https://npmjs.org/package/load-grunt-tasks）的 Node.js 模块。清单 5.27 给出了一个示例。

### 清单 5.27：load-grunt-tasks 的配置示例

```javascript
module.exports = function(grunt) {

  require('load-grunt-tasks')(grunt);

};

```

这个插件使用一个约定，即所有专门为 Grunt 创建的 Node.js 包都有前缀`grunt-`。因此，这个插件可以导出你的`node_modules`目录，并加载所有匹配正则表达式`grunt-*`的模块。你可以使用 npm 安装此插件，使用此命令。

```bash
npm install load-grunt-tasks --save-dev
```

如果你需要一个更通用的版本，你可以使用替代模块 matchdep（https://npmjs.org/package/matchdep）。

#### `ng-min`

包`grunt-ngmin`（https://npmjs.org/package/grunt-ngmin）是 AngularJS 应用程序的预压缩器。你需要这个包，因为 AngularJS 中依赖注入的实现使用你函数的参数名来在此处取消依赖。

由于在最小化过程中会进行替换，此机制在此过程之后将不再起作用。

### 清单 5.28：ng-min 效果示例

```javascript
// ng-min 之前

angular.module('bmApp').controller('MyCtrl', function($scope, $http) {

    [...]

});

// ng-min 之后

angular.module('bmApp').controller('MyCtrl', ['$scope', '$http', function($scope, $http) {

    [...]

}]);

```

为了使 AngularJS 项目能够进行最小化（minification），在 AngularJS 中存在一种关于函数注释的约定。该约定指出，函数应作为数组的最后一个元素给出，并且所有在依赖项之前的参数都应作为字符串传递。由于字符串不受最小化影响，依赖项的取消（cancellation）在此之后将再次正常工作。像往常一样，配置必须添加到你的`Gruntfile.js`文件中。这里使用的参数`src`和`dest`分别代表源文件和目标文件。有关所有参数的确切目录及说明，可参见项目文档。

### 清单 5.29：ng-min 配置示例

```javascript
module.exports = function(grunt) {

    grunt.initConfig({

        [...]

        ngmin: {

            files: {

                src: 'build/**/*.js',

                dest: 'build/'

            }

        },

        [...]

    });

};

```

[第 262 页]（续）

```javascript
});

grunt.registerTask('build', [
    'clean',
    'copy:build',
    'ngmin',
    'uglify'
]);

```

你可以使用 npm 通过以下命令安装此插件。

```bash
npm install grunt-ngmin --save-dev
```

#### concat 和 uglify

借助 uglify 包（https://github.com/gruntjs/grunt-contrib-uglify），可以减小应用程序的文件大小。这可以通过对变量名称进行智能替换来实现。然而，这会导致人类阅读者的可读性下降。不出所料，正因为这一事实，该项目才得名“Uglify”（意为丑化）。进行最小化处理是值得的，这样可以使用户的加载时间尽可能短。

### 清单 5.30：concat 和 uglify 的配置示例

```javascript
module.exports = function(grunt) {

    grunt.initConfig({

        [...]

        concat: {

            src: ['src/module.js', 'src/book.js', [...]],

            dest: 'build/bookmonkey.js',

        },

        uglify: {

            files: {

                'build/bookmonkey.min.js': [
                    'build/bookmonkey.js',
                ]

            }

        }

    });

};

```

在清单 5.30 所示的配置中，`bookmonkey.js`文件被转换为`bookmonkey.min.js`文件。此任务通常在构建过程的最后执行。在本例中，它位于我们使用 Concat（https://github.com/gruntjs/grunt-contrib-concat）将 JavaScript 文件连接成`bookmonkey.js`文件之后。

你可以使用 npm 通过以下命令安装这两个插件。

```bash
npm install grunt-contrib-concat --save-dev
npm install grunt-contrib-uglify --save-dev
```

#### 总结

- Grunt 是一个基于 Node.js 的开源工具，用于自动化处理重复性任务。你可以使用 npm 来安装它。
- 你可以定义自己的任务，这些任务可以接受参数。此外，还有“多任务”的概念，允许你从配置中使用不同的目标（targets）。
- 有许多公共插件也可以通过 npm 安装。
- 你可以使用名为`Gruntfile.js`的文件来配置这些任务。
- 我们看了一些对 AngularJS 必不可少的插件及其配置。其中包括 ng-min 插件。

### 使用 Karma 自动执行测试

Karma（http://karma-runner.github.io）是一个用于自动测试 JavaScript 应用程序的运行时环境。它是为 AngularJS 创建的开源项目，由开发 AngularJS 的同一团队开发。Karma 的主要目标是使测试 Web 应用程序变得尽可能简单。定义的测试规范将在真实设备上执行，以尽量减少最终产品的差异。Karma 启动自己的 Web 服务器，并向任何连接到它的设备发送页面。要测试的设备必须能够处理 HTTP 并解释 JavaScript。该页面包含一个 iframe，用作实际的运行时环境。高层数据由此指导。每个连接的浏览器都通过 Web Socket 连接或相应的后备传输机制（如长轮询）直接从运行的 Karma 进程接收命令。

由于 Karma 像大多数之前讨论的工具一样在 Node.js 平台上运行，你可以使用以下命令通过 npm 安装它：

```bash
npm install -g karma
```

现在，你可以直接使用`karma start`命令启动 Karma，如清单 5.31 所示。

### 清单 5.31：启动 Karma

```bash
[bookMonkey] $ karma start

INFO [karma]: Karma v0.10.4 server started at http://localhost:9876/
```

由于你还没有编写任何配置，这一阶段相当平淡。因此，让我们看下一节，了解如何配置 Karma。

#### 配置

Karma 的配置是通过一个 JSON 文件完成的。如果没有找到明确提供的配置文件，Karma 将在你执行它的目录中搜索名为`karma.conf.js`的文件。如果你想使用另一个文件作为配置文件，必须作为第二个参数向`karma`提供该文件的路径。

```bash
karma start myproject.unit.js
```

在执行`karma`命令时，你可以通过向`karma`传递参数来仅在此会话期间覆盖配置文件中的某个参数。这在 CI（持续集成）环境中，当你希望覆盖配置中的个别值而不创建新文件时，非常有用。更多关于 Karma 配置文件的信息可以在其官方网站上找到，地址如下：

```text
http://karma-runner.github.io/0.10/config/configuration-file.html
```

清单 5.32 显示了 Karma 配置文件的一个片段。

### 清单 5.32：Karma 配置示例

```javascript
'use strict';

module.exports = function(config) {
    config.set({
        basePath: 'src/main/webapp/app/',
        frameworks: ['jasmine'],
        files: [
            'components/angular/angular.js',
            'components/angular-mocks/angular-mocks.js',
            'scripts/module.js',
            'scripts/**/*.js'
        ],
        reporters: ['progress'],
        port: 9876,
        logLevel: config.LOG_WARN,
        singleRun: true,
        autoWatch: false,
        browsers: ['Chrome']
    });
};
```

#### CoffeeScript 中的配置

也可以提供 CoffeeScript 格式的配置文件。你可以将配置保存为扩展名为`.coffee`的文件。Karma 会识别该格式并自动使用相应的 CoffeeScript 处理器。

#### 最重要的参数

在此，我们简要解释配置中最重要的参数。完整且最新的列表可以在在线官方 Karma 文档中找到，网址如下：

```text
http://karma-runner.github.io/0.10/config/configuration-file.html
```

##### `basePath`

为了减少大量的打字工作量，你可以设置`basePath`属性作为其他路径（包括由`files`和`exclude`属性定义的路径）的基础路径。

##### `files`和`exclude`

你可以使用`files`和`exclude`属性来指定在运行 Karma 时应包含或排除的文件列表。

![img](img/7a003218cea01579a50512a6c0e40f28_266_0.png)

##### `frameworks`

你使用`frameworks`属性在环境中嵌入不同的测试框架。你可以在 npm 注册表中查看可用的框架适配器列表：https://npmjs.org/browse/keyword/karma-adapter

要使用此测试框架，首先必须使用 npm 安装它。

```bash
npm install karma-<test-framework> --save-dev
```

此外，你还必须在配置中指定该框架。清单 5.33 展示了如何指定流行的测试框架 Jasmine。

### 清单 5.33：将 Jasmine 嵌入为测试框架

```javascript
'use strict';

module.exports = function(config) {
    config.set({
        [...],
        frameworks: ['jasmine'],
        [...]
    });
};
```



# `browsers`

你可以使用`browsers`属性选择 Karma 应自动启动以执行你的测试的各种浏览器。Karma 原生支持 Chrome 和 PhantomJS 浏览器。但是，你可以使用 npm 安装 Firefox、Opera、Internet Explorer 和 Safari 的包。

## 无头浏览器 PhantomJS

无头浏览器 PhantomJS（http://phantomjs.org）是一个功能完整的 WebKit 浏览器，没有图形用户界面。因此，你可以在没有窗口系统的平台上使用该浏览器执行测试。尽管如此，你拥有其他浏览器提供的所有功能，并可以接收被测网站的当前报告。

### 生成初始 Karma 配置文件

你不需要自己创建初始 Karma 配置文件。Karma 自带一个生成器，当你运行带有`karma init`参数的 Karma 时，它可以创建初始配置文件。通过回答一些关于你所需的测试环境的问题，该工具会生成你特定的`karma.conf.js`文件，并将其存储在你执行命令的目录中。对于我们的 BookMonkey 项目，对话将类似于清单 5.34 所示的内容。

## 清单 5.34：通过命令行生成 Karma 配置文件

```bash
[bookMonkey] $ karma init

你想使用哪个测试框架？
按 Tab 键列出可用选项。
按 Enter 键进入下一个问题。
> jasmine

你想使用 Require.js 吗？
这将添加 Require.js 插件。
按 Tab 键列出可用选项。
按 Enter 键进入下一个问题。
> no

你想自动捕获浏览器吗？
按 Tab 键列出可用选项。
输入空字符串进入下一个问题。
> Chrome >

你的源代码和测试文件位于何处？
你可以使用 glob 模式，例如 "js/*.js" 或 "test/**/*Spec.js"。
输入空字符串进入下一个问题。
> scripts/**/.js
之前模式包含的文件中，是否需要排除某些文件？
你可以使用 glob 模式，例如 "/**/.*.wp"。
输入空字符串进入下一个问题。
>
你希望 Karma 监视所有文件并在文件更改时自动运行测试吗？按 Tab 键列出可用选项。
> no
配置文件已生成于 "/Users/AngularJS/bookMonkey/karma.conf.js"。
```

你现在可以扩展或修改生成的文件。其格式和核心参数已设置妥当，因此你可以立即运行测试用例。诸如忘记某些必需参数或偏离支持格式等错误来源因此被降至最低。

### 自动执行更改

使用 Karma，你可以在每次更改源代码时自动运行测试。你可以使用`singleRun`和`autoWatch`属性来启用此功能。为实现此目的，你必须在配置文件中将`singleRun`设置为`false`，将`autoWatch`设置为`true`。但是，在处理大量数据时，这可能会导致较高的系统利用率。因此，我们建议你再次检查`files`属性中定义的规则，并在必要时使用`exclude`属性排除文件。

### 使用 Karma 扩展

你可以扩展 Karma。已有大量插件可供使用。你可以使用此 URL 上的 npm 注册表搜索并安装它们。

```text
https://npmjs.org/browse/keyword/karma-plugin
```

要实现此目的，请使用你已经熟悉的 npm 命令。

```bash
npm install karma-<plugin name> --save-dev
```

在这种情况下，遵循以下约定：Karma 会自动包含所有以`karma-`为前缀的 npm 模块。如果你需要使用不遵循此约定的插件，可以通过`plugins`属性扩展你的 Karma 配置。

### 清单 5.35：在 Karma 配置中嵌入插件

```javascript
plugins: [
  'karma-*',
  'plugin-example'
]
```

### 在 WebStorm 中直接执行测试

目前，WebStorm IDE 是最受欢迎的 JavaScript 开发环境之一。我们将在第 6 章“调试”中讨论它。因此，我们将在此讨论如何在此环境中安装 Karma。

我们从一个已安装 Node.js 和 Karma 的系统开始。自 WebStorm 7 起，你可以使用官方的 Karma 插件，这使得 WebStorm 集成变得非常简单。如图 5.1 所示，你可以在运行/调试配置对话框的“Karma”节点下选择测试类型。

![](img/7a003218cea01579a50512a6c0e40f28_270_0.png)

你必须在对话框中输入一些路径信息。首先，你必须提供 Node.js 的安装目录。随后，你必须输入用于执行测试的 Karma 的安装目录。如果 WebStorm 能识别你的 Node.js 和 Karma 安装，这两个字段将自动填充正确的路径。如果你想使用另一个版本的 Node.js 或 Karma 来执行测试，可以在此进行配置。同样，你还必须为测试环境提供`karma.conf.js`文件，这一点不足为奇。如果你正确输入了这些参数，就可以通过“运行”来启动执行。也可以在调试模式下执行。图 5.2 展示了我们的测试执行结果。

![](img/7a003218cea01579a50512a6c0e40f28_271_0.png)

图 5.2：测试执行结果

### 测试框架

正如示例配置中已经暗示的那样，你可以使用 Karma 以外的测试框架。目前已有针对 Jasmine（http://pivotal.github.io/jasmine/）、Mocha（http://visionmedia.github.io/mocha）和 Qunit（http://qunitjs.com）的插件。你也可以为其他测试框架创建自己的插件并将其嵌入。Jasmine 和 Mocha 是行为驱动开发（BDD）框架的示例。如清单 5.36 和 5.37 所示，它们的语法也非常相似。

### 清单 5.36：一个 Jasmine 测试规格说明

```javascript
describe("A suite", function() {
  it("contains spec with an expectation", function() {
    expect(true).toBe(true);
  });
});
```

### 清单 5.37：一个 Mocha 测试规格说明

```javascript
describe('A suite', function(){
  it('contains spec with an expectation', function(){
    ok(true);
  })
})
```

### 清单 5.38：一个 QUnit 测试规格说明

```javascript
test("a basic test example", function() {
  var value = "hello";
  equal(value, "hello", "We expect value to be hello");
});
```

无论你决定使用哪种测试框架，都可以使用 npm 安装它，并通过`frameworks`属性将其嵌入你的 Karma 配置。

```bash
npm install karma-jasmine --save-dev
```

作为示例，清单 5.39 展示了如何嵌入 Jasmine。

### 清单 5.39：嵌入 Jasmine 框架

```javascript
frameworks: ['jasmine'],
```

### 持续集成

持续集成（CI）主题也被 Karma 所涵盖。目前，已集成 CI 系统 Jenkins、Travis 和 Teamcity。在本节中，我们主要讨论同时使用 Jenkins 和 Maven，因为这在企业架构中是非常流行的配置。

至此，我们假设 Node.js 和 Karma 已经安装。在你的`pom.xml`文件（Maven 的项目文件）中，你现在可以通过使用 Maven Antrun 插件（http://maven.apache.org/plugins/maven-antrun-plugin）来启动 Karma 进程的执行。清单 5.40 展示了`pom.xml`文件中的摘要。

### 清单 5.40：使用 Maven Antrun 插件从 Maven 启动 Karma

```xml
<plugin>
    <artifactId>maven-antrun-plugin</artifactId>
    <version>1.7</version>
    <executions>
        <execution>
            <phase>generate-sources</phase>
            <configuration>
                <target name="building">
                    <exec
                        executable="cmd"
                        dir="${project.basedir}"
                        osfamily="windows"
                    />
                    <exec
                        executable="karma"
                        dir="${project.basedir}"
                        osfamily="unix"
                    />
                </target>
            </configuration>
            <goals>
                <goal>run</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```

你现在必须将测试结果重定向回 Jenkins。为此，你可以配置 Karma，使其在测试执行后生成 JUnit XML 格式的测试报告。为此，你首先必须安装`karma-junit-reporter`插件。和往常一样，你可以使用 npm 来完成此操作。

```bash
npm install karma-junit-reporter --save-dev
```

成功运行安装后，你可以在 Karma 配置中激活并配置该插件（参见清单 5.41）。

### 清单 5.41：使用 Karma 生成 JUnit 报告

```javascript
reporters = ['junit'];

junitReporter = {
    outputFile: 'test-results.xml'
};
```

最后，来自 Jenkins 的 xUnit 插件（https://wiki.jenkins-ci.org/display/JENKINS/xUnit+Plugin）允许你通过使用 JUnit 报告文件来嵌入生成的测试结果。为此，你必须安装此插件，并在“构建后操作”下选择选项“发布 JUnit 测试结果报告”。你现在可以选择包含测试结果的报告文件，该文件将在每次运行后被导入并添加。此外，你可以定义阈值，以确定在何时可以认为整个构建失败。

### 总结

- Karma 是一个基于 Node.js 平台的工具。它允许你自动执行测试。
- Karma 启动自己的 Web 服务器，测试设备可以连接到该服务器。网络上访问此服务器的每个设备上的每个浏览器都是测试执行的潜在区域。通过这种方式，执行也可以轻松地在移动设备上完成。
- 配置通过一个简单的 JSON 格式文件进行。该文件通常称为`karma.conf.js`。
- Karma 可以集成到 WebStorm IDE 中。
- 你可以嵌入不同的测试框架用于测试用例。我们已经介绍了最流行的 JavaScript 框架。
- Karma 提供了一种允许轻松集成到 CI 系统中的机制。你可以启动系统以将结果导出到 XML 文件中。该文件充当与其他系统的接口。
- 通过示例，我们介绍了在使用 Maven 和 Jenkins 的现有系统中的集成。

## Yeoman：定义工作流

什么是 Yeoman？Yeoman（http://yeoman.io）是一个经过验证的工作流。与 Bower 和 Grunt 一起使用时，它可以帮助你完全专注于实际的应用程序开发。你可以让工具完成相关的额外任务，例如确定合适的目录结构、管理依赖关系或为应用程序组件选择正确的语法。Yeoman 还为影响开发基础设施的任务提供了解决方案。该解决方案尤其包括提供 Web 服务器和创建构建过程。

### 安装 Yeoman

由于 Yeoman 是一个 Node.js 模块，你可以使用 npm 来安装它。

```bash
npm install -g yo
```

安装过程包含了 Bower 和 Grunt 工具，以及一个名为 Yo 的生成器。成功安装后，你就可以在命令行中使用`yo`、`bower`和`grunt`命令了。官方的安装说明也可以在网上找到，地址是 http://yeoman.io/gettingstarted.html。要实际使用 Yo 生成器，你首先需要一个为你决定使用的框架准备的生成器。这些生成器也是 Node.js 模块，同样可以使用 npm 安装。例如，要安装 AngularJS 的生成器，你需要使用这个命令。

```bash
npm install -g generator-angular
```

还有很多其他生成器可以安装。找到生成器的一种方法是用 npm 搜索。另一种方法是查看 Yeoman 官方项目在 GitHub 上的生成器列表（https://github.com/yeoman）。要使用 npm 开始相应的搜索查询，请使用这个命令：

```bash
npm search generator-%name%
```

### 生成应用程序模块

在每个新项目中，你首先要创建项目的基础结构。对于 Web 应用程序，这主要包括创建特定的文件，比如`index.html`文件，以及用于存放图片、CSS 文件和 JavaScript 文件（“资源”）的目录。话虽如此，创建这些基础结构并没有一个简单的方法。恰恰相反：作为开发者，你常常面临选择过多的困境。最终的选择往往受个人偏好影响。有些开发者会引入一个中间目录来存放资源。另一些人则将这个目录命名为`res`，或者完全不这样做。老实说，这些重复性的任务费时费力、容易出错，并且常常导致项目结构各异。为什么我们不能自动化和统一这些任务呢？受 Rails 启发，Yo 项目（http://yeoman.io）被创建出来。Yo 旨在完成客户端 Web 开发中的这些任务。Yo 是一个命令行工具，可以自动生成新项目的底层结构，并保持一致性。该工具的定义由生成器提供。Yo 还附带了适用于许多当前主流框架的生成器，包括一个 AngularJS（https://github.com/yeoman/generator-angular）生成器。AngularJS 生成器实际上是该项目中最早开发的生成器之一。除了 AngularJS 生成器，还有适用于以下框架的生成器：

- Ember.js
- Backbone.js
- jQuery
- Jasmine
- Mocha
- Twitter Flight

使用生成器的一个积极副作用是，项目结构始终保持统一，这使得新开发者更容易适应已有的项目。

### 用于 AngularJS 项目的 Yo

AngularJS 的生成器是 Yeoman 项目中最早创建的生成器之一。该生成器会生成典型的 AngularJS 应用程序模块，并自动将这些设置填入`index.html`文件。此外，每个创建的应用程序模块都会立即配套一个测试套件。

我们将在本章讨论不同的子生成器。我们首先在清单 5.42 中展示 AngularJS 生成器创建的基础目录结构。在第一层，你有两个目录：`app`和`test`，分别用于存放应用程序和测试。在`app`目录内，你有用于存放脚本、样式表和模板文件的目录。在脚本目录中，生成器会为典型的 AngularJS 应用程序的不同组件（`controllers`、`services`、`directives`等）创建目录。

### 清单 5.42：使用 AngularJS 生成器生成的目录结构

```text
app/
  scripts/
    controllers/
    decorators/
    directives/
    filters/
    services/
  styles/
  views/

test/
  spec/
    controllers/
    decorators/
    directives/
    filters/
    services/
```



在`test`目录中，有一个名为`spec`的子目录，其中包含应用程序不同模块的规格说明。`spec`目录的存在是因为可能存在另一个并行的目录`e2e`，用于定义端到端测试。这种类型的测试不容易自动生成，因为它们差异很大。因此，你必须自己创建它们。

## 模块化大型项目

生成器创建的目录结构适用于较小的项目或模块。在大型项目中，你应该使用 AngularJS 的模块系统来组织你的应用程序，并将其划分为不同的技术组件。遗憾的是，AngularJS 生成器生成的目录结构仅适用于单模块应用程序。不过，可以在单个模块内部使用生成器。目前还无法使用`Yo`来自动化管理多个模块。我们将在第 7 章“常见问题解答”中讨论如何借助模块来构建我们的应用程序。

你可以通过传递一个参数来为工具指定所需的生成器。例如，要使用 AngularJS，请使用参数`angular`。

```bash
yo angular
```

如果你不添加任何进一步的说明，`Yo`将为 AngularJS 应用程序生成基础的项目结构。你可以从列表中选择一个子生成器，并用冒号分隔来生成应用程序模块。如果你想添加一个新的控制器，可以使用参数`angular:controller`来执行`Yo`。你可以使用一个额外的参数来定义待生成控制器的名称。可用的子生成器在清单 5.43 中列出。

### 清单 5.43：有效的 AngularJS 生成器命令摘要

```bash
yo angular [applicationName]

yo angular:controller controllerName

yo angular:decorator serviceName

yo angular:directive directiveName

yo angular:filter filterName

yo angular:route routeName

yo angular:service serviceName

yo angular:view viewName
```

> **使用 CoffeeScript**
>
> 偏好用 CoffeeScript 编写应用程序的开发者，可以通过传递参数`--coffee`来使用相应的 CoffeeScript 模板。也可以使用在源代码被压缩后仍能继续工作的模板。这通过参数`--minsafe`实现。这应该由构建过程来处理，这样你在开发过程中就不用担心压缩问题了。

使用生成器时，你应该特别注意组件的命名约定。作为参数提供的名称会通过 Underscore.js JavaScript 库的`camelize()`函数（<https://github.com/epeli/underscore.string>）从连字符命名法转换为驼峰命名法。这意味着使用以下命令生成的 AngularJS 控制器将被命名为`MyControllerCtrl`。

```bash
yo angular:controller my-controller
```

生成的文件将被命名为`my-controller.js`，可以在`app/scripts/controllers/`下找到。在某些情况下这可能会令人困惑。因此，你应该熟悉这个约定。

除了创建组件，生成器还会确保生成的文件被自动添加到`index.html`文件的正确位置。由于 AngularJS 在开发时就考虑了可测试性，所以生成器能够为你的组件生成所需的测试文件也就不足为奇了。

## Yo Angular

你可以使用`yo`命令创建一个新的 AngularJS 应用程序。在内部，它使用子生成器`angular:app`。如果未明确指定子生成器，`angular:app`被定义为默认的子生成器。你可以使用参数`UserManager`创建一个名为`UserManagerApp`的新应用程序。当这个子生成器执行时，它生成的初始应用程序已经可以运行。因此，以下初始化任务将被完成：

- 底层目录结构
- 一个已嵌入 AngularJS 的`index.html`文件
- 第一个路由，包含模板和控制器
- 通用文件，如 404 模板或`.htaccess`文件
- 用于单元测试和集成测试的测试环境
- 依赖管理的基本配置

此外，你可以选择性地包含以下模块：

- Twitter Bootstrap
- Angular Resource
- Angular Cookies
- Angular Sanitize

另外，`Yo`在生成时会询问一个相关问题，你可以用一个请求条目来回答。最后，脚本会使用`npm install`命令启动，该命令也会安装构建过程所需的依赖项。这些依赖项在`package.json`文件中定义。我们将在下一节中更详细地讨论这个方面。

> **Yeoman 中的 Grunt**
>
> 除了为你的项目生成项目结构，`Yo`还会生成一个`Gruntfile.js`文件，该文件为你的项目定义了开发环境和构建环境。我们将在本章末尾讨论在 Yeoman 中使用 Grunt 服务器。

### yo angular:controller

借助控制器子生成器，你可以创建一个新的控制器。名称像往常一样通过第一个参数提供。需要注意的是，模板中的名称会被 Underscore.js 的`classify()`函数修改，并追加字符串`"Ctrl"`。因此，参数`my-controller`会生成文件名`myController`和内部组件名`MyControllerCtrl`。此外，生成的文件会被添加到`index.html`中，并生成相应的测试文件。你可以通过查看清单 5.44 中的模板源代码来理解其上下文。

#### 清单 5.44：yo angular:controller 的模板

```javascript
angular.module('<%_ = _.camelize(appname) %>App')
  .controller('<%= _.classify(name) %>Ctrl',
    ['$scope', function ($scope) {
      // Your logic here
    }]);
```

### yo angular:directive

你可以使用指令子生成器来创建一个指令。清单 5.45 中的模板用于生成指令。

#### 清单 5.45：yo angular:directive 的模板

```javascript
angular.module('<%_ = _.camelize(appname) %>App')
  .directive('<%= _.camelize(name) %>', [function () {
    return {
      template: '<div></div>',
      restrict: 'E',
      link: function postLink(scope, element, attrs) {
        element.text('<% _ = _.camelize(name) %> directive');
      }
    };
  }]);
```

生成的文件存储在`app/scripts/directives/`目录中，并自动添加到`index.html`文件中。

### yo angular:filter

你可以使用命令`yo angular:filter`创建一个过滤器。生成的过滤器将存储在`app/scripts/filters/`目录中。其模板可参见清单 5.46。

#### 清单 5.46：yo angular:filter 的模板

```javascript
angular.module('<%= _.camelize(appname) %>App')
  .filter('<%= _.camelize(name) %>', [function () {
    return function (input) {
      return '<%= _.camelize(name) %> filter: ' + input;
    };
  }]);
```

### yo angular:route

你可以使用`route`子生成器为应用程序添加一个新路由。该脚本会自动生成控制器和模板文件，并将路由自动添加到路由提供程序的配置中。控制器像往常一样自动添加到`index.html`中。

#### 清单 5.47：使用 yo angular:route 扩展路由配置

```javascript
$routeProvider
  .when('/', {
    templateUrl: 'views/main.html',
    controller: 'MainCtrl'
  })

  // this route has been generated by yo angular:route
  .when('/myRoute', {
    templateUrl: 'views/myRoute.html',
    controller: 'MyRouteCtrl'
  })
  .otherwise({
    redirectTo: '/'
  });
```

### yo angular:service

你可以使用`service`子生成器生成一个新的服务。此服务的独特之处在于它让你有机会选择服务类型。你可以从以下类型中选择：

- `constant`
- `factory`
- `provider`
- `service`
- `value`

如果未提供类型，`Yo`通常会选择`factory`作为默认值。你可以在清单 5.48 中查看相应的模板。

#### 清单 5.48：yo angular:service 的模板

```javascript
angular.module('<%= _.camelize(appname) %>App')
  .factory('<%= _.camelize(name) %>', [function () {
    var meaningOfLife = 42;

    // Public API here
    return {
      someMethod: function () {
        return meaningOfLife;
      }
    };
  }]);
```

### yo angular:decorator

装饰器模式是扩展或修改组件的一种非常有用的方式。它允许你后期修改现有服务。这可能是某个特定功能的扩展或替换。借助`decorator`子生成器，你可以为作为 Generator 参数提供的服务创建一个新的装饰器。装饰器生成在`app/scripts/decorators`目录中，其文件名通常由服务名称后接字符串`"Decorator"`组成。由于多个装饰器可以装饰同一个服务，因此可能存在同名文件已存在的情况。此时，子生成器会通过输入请求询问替代名称。你可以在清单 5.49 中找到相应的模板。

#### 清单 5.49：yo angular:decorator 的模板

```javascript
angular.module('<%= _.camelize(appname) %>App')
  .config(['$provide', function ($provide) {
    $provide.decorator('<%= _.camelize(name) %>',
      function ($delegate) {
        // decorate the $delegate
        return $delegate;
      });
  }]);
```




#### 生成的 Grunt 配置

Yo 还会通过命令`yo angular`生成 Grunt 的基本配置。在此配置中，定义了三个主要任务。我们现在将描述这些任务。你可以在本书关于 Grunt 的章节中找到 Grunt 以及`Gruntfile.js`文件构建的详细描述。

#### `grunt server`

当你使用参数`server`启动 Grunt 时，会启动一个最小化的 Web 服务器来为你的 Web 应用程序提供服务。此外，Grunt 会在默认浏览器中打开你的 Web 应用程序。然后 Grunt 连接到默认浏览器。Grunt 进程会持续监控你的项目变化，并在发生变化时导致浏览器中的应用程序完全重新加载。因此，繁琐的手动重新加载就不再必要了。

#### `grunt test`

通过命令`grunt test`，你可以在应用程序中执行单元测试。由于 AngularJS 生成器将测试环境 Karma 嵌入到你的项目中，你也可以在`karma.conf.js`文件中使用参数`singleRun`激活持续测试执行。当你使用此功能时，每次项目目录发生变化时都会执行你的测试。我们在关于 Karma 的章节中已经详细讨论了 Karma 及其有效配置参数。

#### `grunt`

当你不带参数启动 Grunt 时，可以启动应用程序的构建过程。在这种情况下，将执行以下任务：

- JavaScript 代码压缩
- JavaScript 代码合并
- CSS 代码压缩
- CSS 代码合并
- 通过 CDN 嵌入 AngularJS
- JavaScript 代码压缩（uglify）

此过程生成的构建产物通常可以在`dist`目录中找到。

#### 小结

- Yeoman 是一套用于创建 Web 应用程序的既定工作流程。
- 借助 Yo 工具，你可以通过生成器非常轻松地创建新的应用程序组件。
- 所有相关的 JavaScript 框架都有生成器，尤其是针对 AngularJS 组件。
- 可以通过 npm 进行安装。
- 这些工具通过 Bower、Grunt 和 Karma 的依赖关系自动为我们的项目安装和配置。
- AngularJS 生成器模板为你提供了用于开发、测试和交付应用程序的完整 Grunt 任务配置。

## Chapter 6 调试

软件开发人员会犯错。通过采用测试驱动开发（TDD）方法，你可以避免许多这类错误。尽管如此，你仍然会发现有时必须手动调试应用程序。在本章中，我们介绍一些工具和方法，以使这方面的工作更加轻松。

为了调试应用程序，你需要一个监控应用程序运行状况的工具。借助这个工具，你可以在特定的点设置断点，使应用程序执行暂停。然后你可以分析当前的执行状态。此外，你可以一步一步地查看应用程序状态的变化。

#### Chrome 开发者工具

毫无疑问，Chrome 开发者工具是最受欢迎且最常用的 Web 调试工具之一。这些工具随 Google Chrome 浏览器一起提供，并提供了多种实用的功能。我们在本节中介绍其中一些功能。

你可以通过以下两种方法之一打开 Chrome 开发者工具。首先，你可以在网页上右键单击，在出现的上下文菜单中选择**检查**菜单项。其次，键盘组合`Ctrl+Shift+I`（在 Macintosh 上为`Cmd+Alt+I`）可以打开此视图。只要当前没有其他设置打开，你就可以在当前执行程序的浏览器底部打开一个新区域。

##### “元素”选项卡

在“元素”选项卡中，你可以分析和操作当前的文档对象模型（DOM）。如图 6.1 所示，DOM 以可导航的 XML 结构形式呈现。语法高亮让 HTML 代码非常易读。如果你将鼠标移到某个结构上，就会在浏览器窗口中看到对应的容器，并带有一个半透明的蓝色覆盖层。如果你用鼠标点击选择一个元素，就会看到该元素的信息显示在窗口右侧。这些信息包含在各种窗格中，用于组织大量关于该 HTML 元素的数据。然后你可以检查应用于此元素的 CSS 样式。

![Chrome 开发者工具的“元素”选项卡](img/7a003218cea01579a50512a6c0e40f28_287_0.png)

**图 6.1：Chrome 开发者工具的“元素”选项卡**

##### 键盘控制

Chrome 开发者工具提供了一些实用的键盘快捷键。你可以在其官方文档中了解这些快捷键：

https://developers.google.com/chrome-developer-tools/docs/shortcuts

通过双击，你可以操作一个 HTML 元素。如果你双击一个元素或属性，会打开一个小文本框，让你修改当前值。你只需输入新值并按回车即可。数值可以用箭头键递增或递减。

“DOM 断点”子菜单显示当前注册的 DOM 操作断点。这个工具非常有用，因为有时你不清楚 JavaScript 代码的哪一部分修改了某个 HTML 元素。通过在相应元素上右键单击，你可以在**Break on...**下设置断点，直接修改属性、删除元素或修改子树。如果某个语句激活了此断点，处理将停止，并跳转到相应的 JavaScript 代码行。

##### “控制台”选项卡

在“控制台”选项卡下，你可以查看当前打开选项卡的控制台。在这里，你可以查看不同的日志结果，并按日志级别进行过滤。此外，你可以在控制台的一个输入字段中输入 JavaScript 语句。你还可以直接在当前网站的上下文中评估这些语句。在这种情况下，控制台通过提供自动补全功能为你提供便利。执行语句的返回值也会直接显示在执行之后。如果返回值是一个对象，你可以在控制台中分析它。因此，控制台提供了树状视图。`clear()`函数在控制台中也可用。这允许你删除当前的控制台结果。通过控制台，你可以导出和操作当前网站中定义的所有变量。此外，你可以使用`$()`函数轻松地从 DOM 中选择 HTML 元素。大多数 Web 开发人员应该对这个语法很熟悉。你可以将 CSS 选择器的字符串表示传递给此函数，使用 jQuery 风格的语法。返回值是对第一个匹配元素的引用，如果没有匹配则返回 null。

![Chrome 开发者工具的“控制台”选项卡](img/7a003218cea01579a50512a6c0e40f28_289_0.png)

**图 6.2：Chrome 开发者工具的“控制台”选项卡**

在分析 AngularJS 应用程序时，你通常可以访问全局变量`angular`。通过这个变量，你可以调用`angular.element()`函数，该函数允许你通过传递 CSS 选择器来选择 DOM 元素。`angular.element()`返回的 DOM 元素包含你可以调用的函数，用于分析特定的 AngularJS 构造。例如，你可以调用`scope()`函数来获取所选元素当前有效的 scope。

你可以从以下网页了解更多关于`angular.element()`的信息：

http://docs.angularjs.org/api/angular.element

##### “源代码”选项卡：调试 JavaScript 代码

“源代码”选项卡提供了当前网站加载的所有 JavaScript 文件的概览。在此选项卡中，你可以在源代码中定义断点，应用程序将在断点处停止，以便你分析当前的应用程序状态。

![Chrome 开发者工具的“源代码”选项卡](img/7a003218cea01579a50512a6c0e40f28_290_0.png)

**图 6.3：Chrome 开发者工具的“源代码”选项卡**

与任何强大的集成开发环境（IDE）一样，你可以在任何代码行设置断点。双击某一行可切换该行的断点。如果运行时环境成功执行到标有断点的行，应用程序将在该点停止。然后你可以分析当前函数的 scope，以及可能的继承 scope。当你对当前状态不再感兴趣时，可以继续运行程序到下一个断点。

以下键盘可用于帮助你调试。

- F8 – 继续执行程序
- F10 – 单步跳过下一个函数调用
- F11 – 步入下一个函数调用
- Shift+F11 – 步出当前函数调用

###### 条件断点

如果你正在调试提供压缩 JavaScript 代码的网站，可以使用“美化打印”选项自动格式化源代码。这也允许你在压缩源代码的任何行设置断点。该选项位于编辑器中，由对象字面量表示法中的空 JavaScript 对象表示。要分析 Web 应用程序中的一般异常，你有以下暂停功能选项：

- 不在异常处暂停
- 对所有异常暂停
- 对未捕获的异常暂停

由于此功能，你可以发现被 try-catch 块吞掉且未得到妥善处理的错误。

#### 总结

- Chrome 开发者工具是每位 Web 开发人员的宝贵工具集。
- 在“元素”选项卡中，你可以检查和操作当前的 DOM。此外，你还可以使用断点来暂停 DOM 操作。
- “控制台”选项卡提供了一个交互式控制台，允许你在网站的当前上下文中执行 JavaScript 代码。你还可以使用 CSS 选择器选择 DOM 元素。
- 你可以在“源代码”选项卡中检查加载的 JavaScript 文件并设置断点。

#### Batarang：检查运行中的 AngularJS 应用程序

除了 Chrome 开发者工具、Firebug 和各种 JavaScript 调试器等已建立的标准工具外，还有一个特殊工具可用于检查运行中的 AngularJS 应用程序。借助 Chrome 扩展程序 Batarang，你可以查看有关 AngularJS 应用程序状态和性能的信息。你可以查看服务器的各个依赖项、测量控制器函数的执行时间，并查看有关 scope 的相关信息。正是这最后一个方面使 Batarang 成为众多开发人员的必备工具。Batarang 项目是由 Brian Ford 创建的开源项目。源代码可从以下 GitHub 网站获取：

https://github.com/angular/angularjs-batarang

向下滚动查看安装说明。你可以从 Chrome 网上应用店或从源代码安装 Batarang。前者是更简单的安装方法，你只需点击链接并确认要安装即可。Batarang 成功安装后，名为 AngularJS 的选项卡将添加到 Chrome 开发者工具的选项卡集合中。在 AngularJS 选项卡内，有五个子选项卡：Models、Performance、Dependencies、Options 和 Help。还有一个名为`Enable`的复选框，你必须勾选它才能开始使用 Batarang。

#### 查看 Scope

如第 2 章“基本原则和概念”中所述，scope 构成模型层和表示层之间的连接纽带。许多人很快会想知道在视图上可以访问哪些数据，或者某个 scope 内定义了哪些变量。由于 scope 的状态在程序执行期间会发生变化，有时在程序运行时查看 scope 是很有用的。Batarang 在模型子选项卡。该选项卡为你提供了运行应用程序当前作用域层次结构的概览。

通过选择一个作用域，你可以查看当前的变量分配。作用域后面的三位数代表作用域 ID。值得一提的是，你可以在选项卡中查看你的作用域和绑定。这是通过简单的 CSS 类实现的，它会在为新创建的作用域所对应的元素周围绘制一个红色边框。通过此功能，不完全理解作用域概念的开发者可以直观地看到它。此外，在安装 Batarang 之后，你可以在 Chrome 开发者工具的“元素”选项卡中找到更多功能。

一旦你在概览中选择一个 DOM 元素，你会在“AngularJS”选项卡下的信息列中找到该元素的有效作用域。与 Batarang 中的模型分析不同，AngularJS 内部的作用域变量（可以通过`$`和`$$`前缀识别）并未被隐藏。此外，Batarang 会将选定作用域的引用存储在全局变量`$scope`中。然后你可以使用控制台来分析或操纵选定的作用域。

> ## 通过`$scope`操作作用域
>
> 在控制台中使用`$scope`操作作用域非常简单。
> 但是，请注意，更改只能在下一个脏检查周期后才能看到。因此，有必要通过调用`$scope.$apply()`或通过与应用程序的交互来激活它。

#### BookMonkey

搜索...

| CoffeeScript | Andreas Schubert 978-3-86490-050-1 |
|---|---|
| JavaScript for Enterprise Developers | Oliver Ochs 978-3-89864-728-1 |
| Node.js & Co. | Golo Roden 978-3-89864-829-5 |

| Elements | Resources | Network | Sources | Timeline | Profiles | Audits | Console | AngularJS |
|---|---|---|---|---|---|---|---|---|
| Models | Performance | Dependencies | Options | Help | Enable |

#### 作用域

- `< Scope (002)`
  - `< Scope (003)`
    - `< Scope (005)`
    - `< Scope (007)`
    - `< Scope (000)`

#### (005) 的模型

```text
{
  book: {
    title: CoffeeScript
    subtitle: Easy JavaScript
    isbn: 978-3-86490-050-1
    abstract: CoffeeScript is a young, small programming language that compiles into JavaScript.
    numPages: 200
    author: Andreas Schubert
    publisher: {
      name: dpunkt.verlag
      url: http://dpunkt.de/
    }
  }
}
```

启用检查器

图 6.4：使用 Batarang 进行作用域分析

#### 测量函数执行时间

![](img/7a003218cea01579a50512a6c0e40f28_295_0.png)

与大多数其他类似框架不同，AngularJS 使用脏检查来创建双向数据绑定。这意味着在任何给定时间，所有可操纵的作用域都将被检查是否有变化，以便相应地更新依赖组件。这种类型的校准使得使用 AngularJS 开发变得非常方便和容易，因为你可以在数据层使用普通的 JavaScript 对象，而无需继承自特殊的框架构造。然而，在复杂的应用程序中，脏检查可能会导致问题：一旦检查作用域开始耗时过长，应用程序就会开始变慢。

#### 监视表达式

![](img/7a003218cea01579a50512a6c0e40f28_296_0.png)

图 6.6：函数的运行时长分析

在性能子选项卡中，Batarang 允许你分析应用程序中的脏检查。当你激活此功能时，你将获得一个详细的概览，显示从应用程序中检索到的函数以及它们的执行花费了多少时间。你可以相对快速地发现可能导致应用程序变慢的潜在问题。

#### 检查服务依赖关系

当应用程序达到一定规模时，要理清服务依赖关系的纠葛就变得更加困难。然而，如果你希望将应用程序拆分成不同的模块，这仍然非常重要。为了获得已加载服务及其依赖关系的概览，Batarang 为你提供了一个依赖关系图，你可以在其中看到服务之间如何相互依赖。

**服务依赖关系**

![](img/7a003218cea01579a50512a6c0e40f28_297_0.png)

**图 6.7：**服务依赖关系分析

**服务依赖关系**

× Elements Resources Network Sources Timeline Profiles Audits Console AngularJS !

![](img/7a003218cea01579a50512a6c0e40f28_297_1.png)

#### 总结

- Batarang 是 Chrome 开发者工具的一个扩展，它允许你获取关于 AngularJS 应用程序的额外信息。
- 你可以通过多种方式分析和操作作用域。
- 由于 AngularJS 使用脏检查，因此关注性能非常重要。Batarang 允许你测量函数的性能。你可以使用 Batarang 轻松地发现性能问题。

#### WebStorm IDE

WebStorm 是一个用于 JavaScript、HTML 和 CSS 开发的专业 IDE。它是该领域最受欢迎的开发环境之一，可以从以下网址下载。

http://www.jetbrains.com/webstorm

> ## WebStorm 中的 Zen Coding
>
> WebStorm 允许你使用 Zen Coding。此功能由 Emmet 插件提供，你可以从以下网址下载：
>
> http://www.jetbrains.com/webstorm/features/#zen_coding_&_emmet
>
> Emmet 允许你使用类似选择器的表达式来生成更大的 HTML 结构。此插件可以加快开发时间，尤其是在 Web 项目中。

尽管 WebStorm 提供了许多有用的功能，但本章我们将重点介绍其调试功能。WebStorm 允许你在所需的位置暂停应用程序的运行，并分析当前的程序状态。

首先，你需要通过点击此链接从 Chrome 网上应用店安装 WebStorm。

```text
https://chrome.google.com/webstore/detail/jetbrains-idesupport/hmhgedddbhgjknpmjaqkdomcpobmllji
```





![JetBrains IDE 扩展](img/7a003218cea01579a50512a6c0e40f28_298_0.png)

图 6.8：JetBrains IDE 扩展

扩展安装后，Chrome 地址栏旁边会显示 JB 图标。安装扩展后，你可以创建一个新的启动配置类型`JavaScript Remote Debug`。你只需提供一个基础 URL 并在你的项目结构上定义一个本地映射。

![JetBrains IDE 扩展](img/7a003218cea01579a50512a6c0e40f28_299_0.png)

现在使用调试图标或键盘组合`Shift+F9`以调试模式启动 Chrome。你可以通过点击所需位置的左边缘轻松地在 IDE 内设置断点。当应用程序到达定义的断点之一时，执行将停止。

```javascript
$scope.books = [
  {
    title: 'JavaScript for Enterp',
    subtitle: 'Professional programm',
    isbn: '978-3-89864-728-1',
  }
];
```

图 6.10：在 WebStorm 中设置断点

然后你可以检查当前的堆栈跟踪和变量分配。此外，你可以使用以下键盘快捷键控制程序执行：

- `F9` – 恢复程序
- `F8` – 跳过下一个函数调用
- `F10` – 步入下一个函数调用
- `Shift+F8` – 跳出当前函数调用

#### 总结

- WebStorm 是最受欢迎的 JavaScript 开发 IDE 之一。它提供了调试 Web 应用程序的工具。
- 要将 WebStorm 连接到 Chrome，你需要一个名为 JetBrains IDE Support 的特殊 Chrome 扩展。
- 为应用程序设置调试配置并不是一项艰巨的任务。在调试过程中，你可以使用键盘快捷键控制执行流程。

# 第 7 章：常见问题

## AngularJS 模块：如何用模块构建应用程序？

什么是模块？在软件工程中，模块是形成封闭功能单元并表现出高度内聚性的构建块。根据这个定义，一个模块应该只负责一项任务，并且模块应该通过松耦合形成一个完整的系统。通常，你应该总是尝试创建模块化软件。当封装的功能被重用或者由于项目的复杂性需要更具结构性时，尤其如此。此外，模块具有明确定义的接口，其用户使用该接口与模块集成。然后，模块的内部实现可以更改，而无需更改模块用户。

### AngularJS 中的模块

在 AngularJS 中，模块由一系列特定于框架的组件组成，例如服务、过滤器或指令（参见图 7.1）。这些组件定义了模块的接口。

![AngularJS 中可能的模块组合](img/7a003218cea01579a50512a6c0e40f28_298_0.png)

图 7.1：AngularJS 中可能的模块组合

AngularJS 模块始终具有一个由字符串指定的唯一名称。此外，一个模块可以有一个或多个对其他模块的依赖关系。其他模块必须以可解析的方式加载。清单 7.1 展示了一个小例子。

### 清单 7.1：具有依赖关系的模块定义

```javascript
// 初始化应用模块
angular.module('yourAppName', ['yourAppDependency']);

// 定义依赖模块
angular.module('yourAppDependency', []);

angular.module('yourAppDependency').factory(...);

angular.module('yourAppDependency').filter(...);

angular.module('yourAppDependency').directive(...);
```

清单 7.1 中的 JavaScript 代码创建了一个名为`yourAppName`的模块。它需要使用模块`yourAppDependency`，该模块也必须加载以便依赖关系可以被解析。两个模块中哪个先定义并不重要，因为 AngularJS 在运行应用程序之前会异步加载所有已定义和集成的模块。

在模块`yourAppDependency`中，通过使用 AngularJS 函数如`factory`、`filter`和`directive`来注册应作为模块一部分的组件。

注册后，`yourAppDependency`中的组件可以被`yourAppName`访问。由于`yourAppName`现在是 AngularJS 应在 DOM 完全加载后执行的模块，你有两个选择。第一，你可以使用`ngApp`指令声明`yourAppName`模块为启动模块。第二，你可以使用`angular.bootstrap()`函数以编程方式执行模块。其他选项在 Bootstrap 的官方文档中有说明，网址为 http://docs.angularjs.org/guide/bootstrap。

### AngularJS 中的模块加载

AngularJS 模块是异步加载的。这并不意味着模块可以异步重新加载。而是说 AngularJS 首先加载文档中定义或包含的所有模块，然后再启动应用程序。换句话说，所有模块必须在应用程序启动时完成加载。AngularJS 中没有模块延迟加载的机制。

### 模块化何时有用？

定义一组模块并非易事，因为它们无法被泛化，必须根据应用程序的不同来解决。你需要大量经验才能做出正确的决定。这通常伴随着一个迭代过程。没有正式的规则。

然而，我们可以从大型项目的经验中推导出一些指导方针。

AngularJS 官方文档（网址为 http://docs.angularjs.org/guide/module）建议模块应按技术要点进行结构化。这意味着你应该为所有指令创建一个模块。另一个用于管理服务的模块，以及另一个用于过滤器的模块。

然而，根据我们的经验，按技术方面划分意味着在大多数情况下代码重用几乎是不可能的。这是因为解决不同技术问题的组件通常在同一模块中进行管理。这意味着即使你只需要模块中一小部分组件，也必须实现整个模块。

### 模块组合

此时应该注意的是，官方 AngularJS 文档中关于模块组合的建议是该框架早期时期的遗留产物。当时，没有关于大型 AngularJS 项目的具体案例研究。因此，团队只能根据他们当时的知识提出建议。AngularJS 团队现在已经承认，基于技术标准的划分更有意义。

根据我们的经验，通过按技术标准划分模块可以实现优雅的模块组合。因此，解决技术问题的所有组件都是模块的一部分。这意味着在重用模块组合时，很可能确实需要包含的大多数组件。

自 1.0 版本以来，AngularJS 按照这种方法构建其模块。许多以前属于核心部分的技术组件现在已外包到它们自己的模块中。以下列表显示了 AngularJS 中当前模块结构的一部分：

- `angular`
- `angular-animation`
- `angular-cookies`
- `angular-route`
- `angular-touch`
- `angular-...`

你还可以在 AngularJS 的模块划分中看到，主模块中的开发逐渐朝着将非必要部分逐步外包到它们自己的模块中。你可以在自己的项目中非常成功地使用这种方法。当你在家族产品中开发项目时，将对所有项目有用的通用概念外包到实用模块或通用模块中是有意义的。这可以显著缩短开发时间和延迟。然而，这通常需要更多的同步工作。

## 通用模块

对于实用模块，你应该记住这些概念不仅在 AngularJS 上下文中有用。一种好的方法应该允许独立于框架约定开发某些所需功能，并为相应的框架提供适配器模块（在这种情况下是 AngularJS）。因此，使用不同 JavaScript 框架的其他团队也可以从该模块中受益。

如果你正在开发开源模块，你可以使用 Bower 使其向公众开放。此时，你需要正确的版本控制策略。在开源世界中，Tom Preston-Werner 的语义化版本控制已成为一种非官方标准。其网站为 http://semver.org。

由于 AngularJS 中的模块是通过其名称识别的，并且没有权威机构来确定谁可以使用什么前缀，因此无法避免名称冲突。如果两个模块具有相同的名称，则最后加载的模块会毫无警告地覆盖先前注册的模块。因此，你和你的同事应该为整个组织商定命名约定。现有模块的一个良好来源是 http://ngmodules.org 的模块仓库。清单 7.2 展示了命名 AngularJS 模块的可能模式。

### 清单 7.2：模块命名约定

```javascript
// <命名空间>.<名称>-<可选类型>

angularjsde.bookmonkey

angularjsde.bookmonkey-1t8n

angularjsde.bookmonkey-util

angularrsde.bookmonsterlth
```

### 目录结构

在 JavaScript 世界中，没有目录结构的约定。然而，你可以从成功的项目中学习最佳实践。清单 7.3 中展示的结构就是一个例子。

### 清单 7.3：模块的目录结构

```text
module-name/
  scripts/
    module.js
  controllers/
  directives/
  filters/
  services/
  ...
  styles/
  views/
  test/
    controllers/
    directives/
    filters/
    services/
    ...
```

此结构遵循 AngularJS 官方文档的建议。然而，就过程自动化而言具有优势，因为你可以使用通配符模式。在文件`module-name/scripts/module.js`中，模块与其依赖项一起初始化。

### 清单 7.4：module.js 文件

```javascript
angular.module('module-name', ['module-dependency']);
```

以下方法强烈建议用于应用程序中各种模块的组织。

### 清单 7.5：应用程序中各种模块的目录结构

```text
bower_components/
  bower-component-a/
  bower-component-b/
  ...

project_components/
  project-module-a/
    scripts/
      controllers/
      directives/
      ...
      module.js
  project-module-b/
    ...

common_components/
  common-module-a/
    scripts/
      controllers/
      directives/
      ...
      module.js
  common-module-b/
    scripts/
      config/
        routeConfig.js
      module.js
    ...
```

在此结构中，所有由 Bower 管理的组件都位于`bower_components`目录中。特定于你项目的模块可以在名为`projectname_components`的目录中管理，其中`projectname`应替换为项目的实际名称。其他应用程序和团队需要的模块位于`common_components`目录中。

> ### 通用模块的组织
>
> 在项目或团队环境中组织通用模块（`common_components`）的一种非常好的方法是在单独的仓库中管理该模块。你可以将此仓库作为子仓库嵌入到你的项目仓库中。当它超过一定规模且 API 稳定后，你可以使用 Bower 将通用模块转换为组件。为此，你可以使用中央 Bower 注册表或为你的组织创建私有注册表。这两个选项都在第 5 章“项目管理和自动化”的 Bower 部分中讨论。

### 总结

- 在本节中，我们解释了模块的一般定义，并在 AngularJS 的上下文中研究了模块。
- 此外，我们介绍了用于模块和项目的目录结构。
- 已经有许多以不同方式列出的 AngularJS 模块。这些模块通常可以从 Bower 下载。

## Promises：你如何应对异步性？

### 异步性与非阻塞回调函数

JavaScript 应用程序在浏览器中单线程执行。该线程通常被称为事件循环（event loop）。你必须确保不能长时间阻挡应用程序的事件循环，否则整个应用程序都会出现延迟。

然而，存在一些需要在特定处理时间后才能为应用程序提供有价值结果的回调函数。其中包括 HTTP 请求。HTTP 请求会阻塞整个应用程序，因为此时应用程序正在等待来自服务器的响应。尽管运行应用程序只有一个线程，但仍然会出现这种情况，这些阻塞并不常见。那么，在只有一个执行线程的情况下，应用程序如何能快速做出响应呢？答案就是异步性和非阻塞命令函数。

异步性和非阻塞命令函数在 JavaScript 中无处不在。清单 7.6 展示了一个使用回调函数的异步函数的示例。该代码向服务器发送 HTTP 请求，并在控制台打印来自 HTTP 响应的数据。为实现此目的，它调用`makeHTTPRequest()`函数并提供两个参数。第一个参数`url`指定 HTTP 请求的目标地址；第二个参数是回调函数，一旦收到 HTTP 响应便会立即执行。

### 清单 7.6：使用回调函数调用异步函数

```javascript
var url = 'http://mydomain.com/api/user/42';

var user;

makeHttpRequest(url, function(response) {
  user = response.data.user;

  console.log('User data', user); // user is defined!
}); // makeHttpRequest() 是异步的 / 非阻塞的！

console.log('User data', user); // user 未定义！
```

在示例中，变量`user`被`console.log()`函数使用了两次。第一次是在调用`makeHTTPRequest()`之后立即进行，第二次是在匿名回调函数中进行。紧跟在`makeHTTPRequest()`调用之后的日志输出将首先打印。然而，此时变量`user`仍然未定义，因为尚未收到 HTTP 响应接收。

由于`makeHTTPRequest()`是一个异步非阻塞函数，即使 HTTP 请求仍在处理中，对其进行调用的操作也不会阻挡应用程序的执行。一旦收到 HTTP 响应，作为第二个参数传递给`makeHTTPRequest`的回调函数将被执行。在此回调函数中，变量`user`被赋值为`response.data.user`，其值将在控制台打印。在这种情况下，只要在处理 HTTP 请求过程中没有发生错误且相应的 User 对象在`response.data`中已定义，变量`user`就是定义的。

### 什么是 Promise？

如果你想执行多个相互依赖的异步回调函数，事情就会变得复杂起来。如果一个异步回调函数需要从另一个回调函数先获取数据才能为其自身的回调提供所需数据时，则它依赖于该另一异步回调函数。正如你在清单 7.7 中看到的那样，“金字塔地狱”（pyramid of doom）出现在源代码常见的缩进中，其不断将脚本向右推移。现在想象一下，如果除了正常处理外还需要拦截和跟踪错误会怎样呢。很明显，几个异步回调函数的组合会导致代码难以阅读。

### 清单 7.7：金字塔地狱

```javascript
makeHttpRequest(url, function(response) {
  performOperation(response.data.user, function(result) {
    calc(result, function(calcResult) {
      doSomething(calcResult, function() {
        ...
      });
    });
  });
});
```

如何优雅地处理异步回调函数？在 JavaScript 的世界中，Promise（承诺）已成为解决此问题的方法。在其他编程语言中，Promises 常被称为 Futures（未来对象）。有关该概念的开明规范称为 promises/A+（http://promises-aplus.github.io/promises-spec）。此规范涉及各种 Promise 实现之间的互操作性。清单 7.8 展示了之前使用回调函数解决的同样问题。现在借助异步操作返回 Promises `promise`，代表了其中一种异步操作的机制之一，并且通过该操作它可以优雅地处理 API 的回调。

如你在清单 7.8 中所见，返回值或错误会自动传递给下一个异步回调（下游值和错误的传播）。这意味着可以使用 Promise 以更可读的方式编写异步回调函数。此外，你可以更优雅地处理错误。

### 清单 7.8：返回承诺值的异步操作

```javascript
makeHttpRequestPromise(url)
  .then(function(response) {
    return response.data.user;
  })
  .then(performOperation)
  .then(calc)
  .then(doSomething, function(error) {
    console.log('An error occurred!', error);
  });
```




在此示例中，`makeHTTPRequestPromise()`返回一个 Promise 对象。Promise 最重要的功能是 `then()`函数。你可以使用 `then()`来定义当异步操作的结果可用或发生错误时应该调用哪个回调函数来实现此目的。然后`()`函数接收两个参数：第一个是成功函数，它将在异步回调执行成功且结果可用的情况下被调用；第二个是错误函数，它在回调过程中出现错误时将予以执行。在下列清单中可以看到一个使用 Promise 的 API 摘要：

```javascript
// onSuccess and onError are functions!

promise.then(onSuccess, onError)
```

由于返回值会自动传递给下一个异步操作，而且每个操作都返回 promise（承诺），你可以如图案所示地链接 `then()`回调函数。但是为了向 `performOperation()` function provide data from `response.data.user` object 而非整个响应对象提供数据，需要在 `makeHttpRequestPromise()`与`performOperation()`之间构建一个转换步骤来处理任何可能的错误：通过给 `then`提供一个匿名的 error function（仅打印），并在成功调用 `doSomething`的同时，由于潜在的错误会自动处理，因此只需在一个位置即可。

为了向你展示如何实现基于 Promise 的自定义异步操作，我们将使用 Q 库。Q (`http://documentup.com/kriskowal/q/`)是 promises/A+规范的流行实现之一。我们之所以选择 Q，是因为 AngularJS 对 Promises 的实现也基于 Q 的子集。

在清单 7.9 中概述了使用 Q 实现的 `makeHTTPRequestPromise()`函数的可能实现方案。这是一个包装器函数，它将传统的回调方式封装成返回 promise 的形式，使得回调中包含 response as promise。为实现这一目标，我们需要利用 `Q.defer`这个异步非阻塞的 API 来创建一个 deferred 对象。该 deferred 是转换基于回调式的调用到基于 Promise 式调用的关键组件。我们将对象的引用存储在局部变量 `deferred`中。

### 清单 7.9：将基于回调的调用转换为基于 Promise 的调用

```javascript
// Wrap makeHttpRequest

var makeHttpRequestPromise = function(url) {
  var deferred = Q.defer();

  makeHttpRequest(url, deferred.resolve, deferred.reject);

  return deferred.promise;
};
```

`deferred`对象可以通过 `promise`属性访问相关的 promise。你把这个 Promise 传递给`makeHTTPRequestPromise()`函数，从而满足了使其返回承诺的需求。调用者现可使用。

## AngularJS 中的 Promise

你可以在 AngularJS 中使用 promise。几乎所有提供的组件操作都会返回一个 promise。这包括 `$http`服务，它简化了 HTTP 请求的构建。AngularJS 中的 promise 实现在很大程度上基于 Q 的一个子集。你可以通过依赖注入提供一个 `$q`服务来访问这个实现。

与 Q 相比，AngularJS 的内部实现在几个方面存在差异，这是因为该框架必须将实现在 dirty checking（脏检查）上下文中无缝集成。如第 4 章“扩展应用”中所讨论的，AngularJS 外部发生的 scope 操作需要通过 `$scope.$apply()`手动调用 dirty checking 回调。为了确保这不会在异步操作后迫使浏览器重绘 DOM 元素，这些函数会在 `$rootScope`中借助一个辅助函数执行，以解决这一问题。

清单 7.10 展示了名为 `promisesService`的 AngularJS 服务中的 `makeHTTPRequest()`示例。为此，除了 `$q`服务外，我们还需要应用的 `$rootScope`，因为我们必须在异步函数执行后手动激活 dirty checking。如果我们不这样做，我们的 AngularJS 应用将不会收到此函数触发的更改通知。

使用 `then()`注册成功或错误函数，如清单 7.8 所示。现在你需要确保根据 `makeHTTPRequest()`回调的结果，promise 是被 fulfilled（完成）还是 rejected（拒绝）。你可以通过 `resolve()`和 `reject()`函数来实现这一点。`resolve()`用于处理成功的完成，而 `reject()`函数确保在发生错误时 promise 被拒绝。

你刚才看到，`makeHTTPRequest()`函数接受一个回调函数作为第二个参数，以便在成功时调用它。通常，基于回调的异步函数也会提供一个错误处理器。这是通过使用相应的回调函数来解决的。因此，假设 `makeHTTPRequest()`函数期望第三个参数是一个错误函数，如清单 7.9 所示。这意味着你可以将 `makeHTTPRequest()`分别以 `deferred.resolve`和 `deferred.reject`作为第二个和第三个参数传入，以便完成 promise 或拒绝错误。通过这种方式，我们将基于回调的函数 `makeHTTPRequest()`转换为基于 promise 的函数 `makeHTTPRequestPromise()`。Q 也提供了以更优雅的方式格式化源码的工具，但这在 AngularJS 上下文中并不相关。

> **Promises（Promise）**
>
> 要使用 Q 将基于回调的函数转换为基于 promise 的函数，请使用通过 `Q.defer()`创建的 deferred 对象。通过使用这个 deferred 对象，你可以通过 `deferred.promise`访问关联的 promise。然后你将此 promise 传递给回调函数。现在，你需要弄清楚为什么 deferred 对象和 promise 之间存在区分。为什么你不能直接使用 promise？答案其实非常明显。
>
> 你通常不希望将控制 promise 何时被完成或拒绝的权力交给回调函数。因此，你传递 promise，然后可以在函数简化过程中借助 deferred 对象控制何时发生完成或拒绝。如果你只使用 promise（没有 deferred 对象），回调函数自己就可以完成或拒绝该 promise。

### 清单 7.10：在 AngularJS 中使用 `$q`

```javascript
angular.module('app').factory('promisesService',
  function($rootScope, $q) {
    return {
      makeHttpRequestPromise: function(url) {
        var deferred = $q.defer();

        // 手动触发 dirty checking
        $rootScope.$apply(function() {
          makeHttpRequest(
            url,
            deferred.resolve,
            deferred.reject
          );
        });

        return deferred.promise;
      }
    };
  }
);
```

```javascript
angular.module('app').controller('PromisesCtrl',
  function($scope, promisesService) {
    promisesService
      .makeHttpRequestPromise('http://server/user')
      .then(function(result) {
        $scope.user = result;
      });
  }
);
```

通过在此处嵌入 `promisesService`（参见 `PromisesCtrl`），我们可以在调用 `promisesService.makeHTTPRequestPromise()`后使用 `then()`函数来处理成功或错误。

AngularJS 的 `$q`实现提供了额外的 API 函数，使处理 promise 变得更加容易。例如，`$q.all()`函数期望一个 promise 数组，并返回一个 promise。返回的 promise 将在数组中所有 promise 都 resolved 后 resolved。因此，`$q`允许你同步执行一系列异步操作，只要它们彼此不依赖。此外，你可以执行一个后续操作，该操作处理来自异步操作的各项结果。就像通常情况一样，你可以以带有 `then()`的成功函数的形式指定后续操作（参见清单 7.11）。这样，当每个单独的异步操作完成并且其结果可用时，此成功函数就会被执行。在这种情况下，AngularJS 会将各个结果以数组形式返回。如果至少有一个异步操作导致错误并且其 promise 被 rejected，那么结果 promise 也会被 rejected。

### 清单 7.11：PromiseCtrl 的实现

```javascript
function($scope, $q, promisesService) {
  $q.all([
    promisesService
      .makeHttpRequest('http://server/user/1'),
    promisesService
      .makeHttpRequest('http://server/user/2')
  ]).then(function(resultsArray) {
    $scope.users = resultsArray;
  });
}
```

`$q.when()`是 `$q`服务中的另一个有用函数。这个函数允许你模拟基于 promise 的 API。你可以向此函数传递一个值，它将返回一个代表该值的 promise。此外，借助此函数，你可以将一个属于第三方库的 promise 转换为 Q promise。这只有在外部 promise 实现了 promises/A+规范时才可行。

要使用 `$q.when()`模拟异步 API，让我们再次使用 BookMonkey 项目中的 `BookDataService`（参见第 3 章“Bookmonkey 项目”）。

在第 4 章“扩展应用”中介绍 `$http`服务之前，我们没有从函数返回 promise。相反，我们直接返回数据。之所以这样做，是因为直到那时为止没有执行任何异步操作，我们希望避免使示例过于复杂。然而，我们的解决方案存在问题，因为随着 `$http`服务的引入，我们必须更改应用中调用我们服务的所有部分。此更改后，BookDataService 的 API 最终基于 promise。因此，我们必须处理相应的 `then()`回调。如果我们在介绍 `$http`服务之前使用 `$q.when()`模拟即将成为异步的 API，将会减少工作量。

清单 7.12 展示了模拟基于 promise 的 API 所需执行的步骤。这里重写了 `getBookByIsbn()`函数。我们只需使用 `$q.when()`函数包装返回值，而不是直接返回它。`getBookByIsbn()`的返回值现在是一个代表实际返回值的 promise。我们现在可以使用 `then()`定义我们的成功和错误函数。

### 清单 7.12：使用 `$q.when()`模拟 Promise

```javascript
// BookDataService

bmApp.factory('BookDataService', function($q) {
  [...]

  // 公共 API
  return {
    getBookByIsbn: function(isbn) {
      var result = srv.getBookByIsbn(isbn);

      // 使用 $q.when() 模拟基于 Promise 的 API
      return $q.when(result);
    },

    [...]
  };
});

// BookDetailsCtrl

bmApp.controller('BookDetailsCtrl',
  function($scope, $location, $routeParams, BookDataService) {
    var isbn = $routeParams.isbn;

    BookDataService.getBookByIsbn(isbn).then(function(res) {
      $scope.book = res.data;
    }, function(error) {
      console.log('An error occurred!', error);
    });
  }
);
```

> **实现异步 API**
>
> 最佳实践是使用 promise 实现每一个异步操作。如果你知道你的 API 迟早会以异步方式工作，那么使用 `$q.when()`模拟未来的异步性是合理的。

## 在 AngularJS 中测试 Promise

测试异步函数并非易事。幸运的是，你可以使用 Jasmine 框架。Jasmine 提供了一些特殊函数，如 `runs()`和 `waitsFor()`。你使用 `runs()`来执行异步函数。你使用 `waitsFor()`来等待在给定超时时间内满足特定条件。

关于异步函数测试的详细信息，可以在 Jasmine 官方文档中找到，网址为 `http://pivotal.github.io/jasmine/#section-Asynchronous_Support`。

AngularJS 还提供了另一种针对基于 Promise 的异步 API 的扩展。这大大简化了测试的编写。通过嵌入测试模块 `ngMock`，你可以同步执行 Promise 的异步操作，从而决定何时使用特定的函数回调来解析 Promise。

清单 7.13 展示了我们人为扩展的 `BookDataService`，其中添加了 `promiseFn()`函数。通过 `$q.when()`函数，该函数返回一个代表 "BookMonkey" 的 Promise。

### 清单 7.13：为测试 Promise 而人为扩展的 BookDataService

```javascript
bmApp.factory('BookDataService', function($q) {
  [...]

  // Public API
  return {
    [...]

    promiseFn: function() {
      return $q.when('BookMonkey');
    }
  };
});
```

为了测试这个函数，我们创建了一个新的测试，如清单 7.14 所示。在这个测试中，我们调用函数 `BookDataService.promiseFn()`并接收一个 Promise 作为返回值。通过调用 `expect()`，我们可以测试返回的对象是否是一个 Promise。随后，我们定义变量 `result`并将其传递给 `then()`调用中的成功函数。通过将 `result`传递给 `expect()`函数，我们可以查询 `result`的值是否为 `undefined`，即尚未收到值。

接下来，我们可以通过调用 `$rootScope.$apply()`来同步调用 Promise。回想一下，使用此函数我们可以手动激活脏检查。

手动调用 Promise 后，我们可以测试是否有了确定的结果，以及该结果是否对应字符串 "BookMonkey"。我们通过另外两个 `expect()`调用来实现这一点。

### 清单 7.14：使用 Promise 的同步调用测试基于 Promise 的函数

```javascript
it('should include a promiseFn() function',
  inject(function($rootScope, BookDataService) {
    var promise = BookDataService.promiseFn();

    expect(promise).toBeDefined();
    expect(promise.then).toBeDefined();

    var result;

    promise.then(function(data) {
      result = data;
    });

    expect(result).toBeUndefined();

    // Resolve promise (execute success function)
    $rootScope.$apply();

    expect(result).toBeDefined();
    expect(result).toBe("BookMonkey");
  })
);
```




#### 小结

- 在本节中，我们讨论了如何在 JavaScript 中优雅地处理异步函数。许多异步 API 基于回调函数。由于异步回调的嵌套可能导致难以阅读的构造（尤其是回调地狱），我们引入了 Promise 来解决这个问题。
- 有一个名为 Promises/A+ 的开放规范。
- 该规范确保不同的 Promise 实现彼此兼容。
- 我们了解了 Promise 实现 Q。
- 我们可以在 AngularJS 中实现 Q 的一个子集。
- 在 AngularJS 中，我们可以通过`$q`服务访问这个子集。
- 在本节末尾，我们了解了如何使用`$q`服务基于 Promise 实现异步操作。
- 我们还展示了如何简化 AngularJS 中基于 Promise 的 API 的测试。该框架允许我们在测试中同步调用 Promise。

#### AngularJS 与 RequireJS：这是正确的组合吗？

##### 什么是 RequireJS？

RequireJS 可从`http://requirejs.org/`下载，是一个 JavaScript 框架，支持文件和模块的异步加载。它允许你定义模块及其依赖关系。为此，RequireJS 实现了异步模块定义（AMD）API，这是 JavaScript 世界中模块定义的**非**正式标准。AMD API 提供以下优势：

- 依赖项不再需要手动排序，而是隐式解析。
- 依赖项可以在需要时异步加载。
- AMD API 阻止使用全局变量。
- 模块名称可以被覆盖，以便在测试中使用模拟实现进行替换。
- 框架自动识别当前需要哪些依赖项，并按正确顺序加载它们。RequireJS 为每个依赖项在我们的应用程序的 head 标签中添加一个`script`标签。一旦该标签被添加到 DOM，浏览器就会尝试加载并执行该文件。这可以加快初始加载速度。

##### RequireJS 示例

我们在一个小项目中演示如何使用 RequireJS。项目结构如清单 7.15 所示。

##### 清单 7.15：RequireJS 示例的目录结构

```text
index.html
scripts/
  app.js
  require.js
  helper/
    util.js
    i18n.js
```

项目包含一个`index.html`文件，我们在其中加载 RequireJS 脚本（见清单 7.16）。注意额外的`data-main`属性，它定义了我们应用程序的入口点。

##### 清单 7.16：我们 RequireJS 示例的 index.html

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Sample Project</title>

  <!-- data-main 属性告诉 require.js 在 require.js 加载后加载
    scripts/app.js。 -->

  <script data-main="scripts/app" src="scripts/require.js">
  </script>
</head>
<body>
  <h1>My Sample Project</h1>
</body>
</html>
```

浏览器加载脚本后，开始执行 RequireJS。通过`data-main`属性定义的脚本（`scripts/app`）现在被重新加载并执行。在`app.js`中，我们使用 AMD API 并通过`require()`引入所提供函数的执行（见清单 7.17）。然而，该函数只有在所有依赖项完全加载后才会执行。依赖项通过第一个参数作为字符串数组提供。在我们的例子中，我们需要模块`helper/util`作为依赖项。该模块提供要执行的函数作为第一个参数。

##### 清单 7.17：我们 RequireJS 应用程序的入口点（app.js）

```javascript
require(["helper/util"], function(util) {
  var output = util.translateFn("Hello World");
  console.log(output);
});
```

> **定义 RequireJS 依赖项**
>
> 模块依赖项的路径相对于入口点定义（由`data-main`属性定义）。如果你需要不同的行为，可以使用参数`baseUrl`进行配置。你可以在官方文档`http://requirejs.org/docs/api.html#config-baseUrl`中查看准确定义。

你可以使用 RequireJS 的`define()`函数定义模块，如清单 7.18 所示。你可以在数组中为一个模块指定依赖项。在我们的`util`模块中，我们将模块`helper/i18n`指定为依赖项。在`util`模块中，我们使用来自`i18n`模块的`translate()`函数。在这个例子中，`util`模块返回一个提供公共函数`translateFn()`的 API 对象。这样，我们可以让其他模块使用本地函数`translate()`。

##### 清单 7.18：使用 RequireJS 定义的 util 模块

```javascript
define(["helper/i18n"], function (i18n) {
  var translate = function(input) {
    return "Translated: " + i18n.translate(input);
  };

  // Public API

  return {
    translateFn: translate
  };
});
```

因此，通过为每个组件定义一个 AMD 模块，你可以在一个简单的 JavaScript 应用中实现组件的清晰划分。此外，你不必处理`index.html`中各种 JavaScript 文件的正确加载顺序，因为 RequireJS 会处理这一点。

#### 加载外部依赖项

有时，你需要重新加载无法在`baseUrl`路径下找到的依赖项。为此，有一个约定可以覆盖标准行为。然后，你可以重新加载那些路径可以相对于当前地址指定的脚本。从 CDN 重新加载脚本也是可能的。在以下情况下，`baseUrl`约定被搁置：

1. 输入的依赖项以`.js`结尾。
2. 输入的依赖项以`/`开头。
3. 输入的依赖项包含协议信息，如`http://`或`https://`。

图 7.2 以图形方式展示了我们示例项目中的依赖关系。

![图 7.2：我们示例项目内部的依赖关系](img/7a003218cea01579a50512a6c0e40f28_323_0.png)

#### AngularJS 与 RequireJS

在本节中，你将学习如何一起实现 AngularJS 和 RequireJS。为此，你必须扩展一个 AngularJS 项目以接受

## 第七章：常见问题解答

针对某些特定的 RequireJS 构建方式，我们决定基于我们的 BookMonkey 项目来实现这些扩展。

第三章上一节中的 BookMonkey 版本为我们引入 RequireJS 提供了基础。回想一下，在那一节中，我们介绍了使用路由进行导航。现在的思路是将各个 AngularJS 组件定义在它们自己的 AMD 模块中。此外，我们将创建一个`requireConfig.js`文件，它将作为我们应用程序的入口点。我们还将使用 Bower 来管理依赖项。目录结构如清单 7.19 所示。

#### 清单 7.19：使用 Bower 进行依赖管理的 BookMonkey 目录结构

```text
bower_components/
  angular/
    angular.min.js
  angular-route/
    angular-route.min.js
  requirejs/
    require.js

scripts/
  config/
    routes.js
  controllers/
    book_details.js
    book_list.js
  services/
    book_data.js
  app.js
  requireConfig.js

index.html
bower.json
```

作为第一步，我们在`index.html`中包含 RequireJS。我们使用`data-main`属性来标识入口点。如清单 7.20 所示，该属性引用了我们定义在`scripts/requireConfig.js`文件中的 AMD 模块`scripts/requireConfig`。此外，我们移除或注释掉之前的`script`标签，因为 RequireJS 会负责文件加载。

#### 清单 7.20：集成了 RequireJS 的 BookMonkey 的 index.html

```html
<script src="bower_components/requirejs/require.js"
    data-main="scripts/requireConfig"></script>

<!--
这些脚本标签现在已过时！

<script src="lib/angular/angular.min.js"></script>
<script src="lib/angular-route/angular-route.min.js"></script>
<script src="scripts/app.js"></script>
<script src="scripts/controllers/book_details.js"></script>
<script src="scripts/controllers/book_list.js"></script>
<script src="scripts/services/book_data.js"></script>
-->
```

接下来，我们配置应用程序所需的 AMD 模块`angular`和`angularRoute`（参见清单 7.21）。为此，我们可以使用 RequireJS 的`require.config()`函数。该函数接收一个配置对象。为了嵌入 AngularJS，我们需要`paths`属性。此属性允许我们指定那些无法在`baseUrl`路径下直接找到的依赖项。此外，我们为这些依赖项指定一个确切的模块名。由于 AngularJS 和`ngRoute`模块是外部依赖，我们只能通过 Bower 来管理它们，因此我们在此处指定了指向`bower_components`目录的相对路径。

为了确保我们的 AngularJS 被正确嵌入，我们必须告诉 RequireJS 将 AngularJS 赋值给全局变量`angular`。这可以通过使用`shim`属性来完成。为了获得正确的初始化顺序，我们将 AMD 模块`angular`定义为 AMD 模块`angularRoute`的依赖项。

#### 清单 7.21：在 RequireJS 上下文中配置 AngularJS

```javascript
require.config({
  paths: {
    angular: '../bower_components/angular/angular',
    angularRoute: '../bower_components/angular-route/angular-route'
  },

  shim: {
    'angular': {'exports': 'angular'},
    'angularRoute': ['angular']
  }
});
```

你可以通过内容分发网络（CDN）加载库。前述的 RequireJS 模块约定在此处同样重要。你甚至可以指定一个回退选项（`http://requirejs.org/docs/api.html#pathsfallbacks`）。这样，你可以将 CDN 资源指定为第一个参数，而将本地资源作为备选方案，在 CDN 不可达时进行加载。这如清单 7.22 所示。

#### 清单 7.22：在 RequireJS 上下文中使用 CDN 和回退选项配置 AngularJS

```javascript
require.config({
  [...]

  paths: {
    angular: [
      '//ajax.googleapis.com/ajax/libs/angularjs/1.2.0/angular',
      '../bower_components/angular/angular'
    ]
  },

  [...]
});
```

RequireJS 还有其他配置选项。建议花时间研究其在线文档：`http://requirejs.org/docs/api.html`。

#### 清单 7.23：AMD 模块 app 的定义

```javascript
define([
  'angular',
  'angularRoute'
], function (angular) {
  return angular.module('bmApp', ['ngRoute']);
});
```

当我们与 RequireJS 一起使用 AngularJS 应用程序时，必须确保仅在所有脚本加载完成后才定义 AngularJS 的引导启动。我们可以使用 RequireJS 的`require()`函数来正确管理手动引导启动（参见清单 7.24）。

#### 清单 7.24：在 RequireJS 上下文中手动引导启动我们的 AngularJS 应用程序

```javascript
// requireConfig.js
[...]

require([
  'angular',
  'app',
  'config/routes'
], function(angular, app) {
  angular.element().ready(function() {
    var elem = document.getElementsByTagName('html')[0];
    angular.bootstrap(elem, [app['name']]);
  });
});
```

在此函数中，我们可以通过使用`ready()`注册回调函数来监听`DOMContentLoaded`事件。一旦此事件触发，我们就可以在回调函数中开始初始化 AngularJS 应用程序。为此，我们使用`angular.bootstrap()`函数。第一个参数指定 DOM 元素，在自动初始化的情况下，我们会用`ngApp`指令标记它。第二个参数定义要加载的应用模块名称。我们可以从此时可用的 AMD 模块`app`中导出应用模块的名称。

在清单 7.24 中，我们将 AMD 模块`config/routes`指定为依赖项。在此模块中，我们定义了 AngularJS 应用程序的路由。清单 7.25 展示了模块定义。

#### 清单 7.25：作为 AMD 模块的我们的 AngularJS 应用程序的路由配置

```javascript
define([
  'app',
  'controllers/book_list',
  'controllers/book_details'
], function (app) {
  app.config(function($routeProvider) {
    $routeProvider.when('/books/:isbn', {
      templateUrl: 'templates/book_details.html',
      controller: 'BookDetailsCtrl'
    })
    .when('/books', {
      templateUrl: 'templates/book_list.html',
      controller: 'BookListCtrl'
    })
    .otherwise({
      redirectTo: '/books'
    });
  });
});
```

AMD 模块`config/routes`需要三个依赖项。首先，它需要我们的 AMD 模块`app`，以便通过 AngularJS 的`config()`函数提供`$routeProvider`并配置路由。由于我们必须确保在路由配置中特定控制器已被加载，我们将定义该控制器的 AMD 模块指定为依赖项。这样我们就能确保 AMD 模块`controllers/book_list`和`controllers/book_details`都已可用。

#### 清单 7.26：在 RequireJS 上下文中作为 AMD 模块的 AngularJS 控制器

```javascript
define([
  'app',
  'services/book_data'
], function (app) {
  app.controller('BookListCtrl', function ($scope, BookDataService) {
    $scope.getBookOrder = function (book) {
      return book.title;
    };

    $scope.books = BookDataService.getBooks();
  });
});
```




像往常一样，我们在`define()`函数中添加一个新的 AMD 模块。在这种情况下，我们处理的是 AMD 模块`controllers/book_list`。我们还依赖于`app`模块，以便我们可以将控制器作为定义添加。由于此控制器还需要`BookDataService`，我们也应将相应的 AMD 模块`services/book_data`指定为依赖项。像往常一样，AngularJS 的内部机制（如依赖注入）在模块定义中仍然可用。AngularJS 可以毫无问题地指定作用域（`$scope`）以及`BookDataService`。

为完整起见，我们在清单 7.27 中展示了另一个摘要，即`BookDataService`的 AMD 模块`services/book_data`的定义。值得一提的是，我们也可以嵌入 AMD 模块`angular`并使用 AngularJS 的全局 API（例如`angular.element()`、`angular.copy()`等）。

## 清单 7.27：在 RequireJS 上下文中，作为 AMD 模块的 AngularJS 服务工厂

```javascript
define([
    'angular',
    'app'
], function (angular, app) {
    app.factory('BookDataService', function () {
        // angular.element()
        // angular.copy()
        // ...
    });
});
```

因此，我们已经展示了如何在 RequireJS 上下文中执行 AngularJS 应用程序。作为总结，我们应用程序的依赖关系如图 7.3 所示。该图在技术上并不完全准确，因为我们需要在其他每个模块中都包含`app`这个 AMD 模块。然而，这将使图表变得非常难以阅读。因此，我们在图中考虑略去了这些依赖关系。

## 使用 RequireJS 进行测试

在本节中，我们将探讨为了在 RequireJS 上下文中使用 AngularJS 应用程序所需执行的步骤。首先，我们必须使用 npm 安装 RequireJS Karma 适配器。我们还必须在`frameworks`下的 Karma 配置中指定它。Karma 适配器的安装是在命令行中通过以下命令完成的：

```bash
npm install karma-requirejs
```

# 第 7 章：常见问题

## 图 7.3：RequireJS 上下文中 BookMonkey 的模块依赖关系

完成上述步骤后，我们必须调整 Karma 配置中的`files`块。

由于 RequireJS 本身嵌入文件并异步重新加载它们，因此我们需要在测试套件中提供各种所需的文件，而无需直接嵌入它们。我们通过将属性`included`设置为`false`来实现这一点（参见清单 7.28）。因此，我们可以定义 Karma 启动的 Web 服务器允许在不使用`<script>`标签嵌入的情况下发送这些文件。Karma 已在第 5 章中介绍过。

## 清单 7.28：在 RequireJS 上下文中测试 AngularJS 应用程序的 Karma 配置

```javascript
// frameworks to use
frameworks: ['jasmine', 'requirejs'],

// list of files / patterns to load in the browser
files: [
  {
    pattern: 'app/bower_components/angular/angular*.js',
    included: false
  },
  {
    pattern: 'app/bower_components/angular-route/angular-route*.js',
    included: false
  },
  {
    pattern: 'app/bower_components/angular-mocks/angular-mocks*.js',
    included: false
  },
  'test/unit/**/*.ts',
  {
    included: true
  },
  'test/testRequireConfig.js'
]
```

此外，我们还需要为我们在 Karma 中执行的测试指定一个适配的 RequireJS 配置（参见清单 7.29）。在这个过程中，我们需要注意以下几点：

- AngularJS 必须包含所有必需的模块。
- 必须包含 AngularJS 模块`ngMock`。
- 路径配置应进行调整以适应 Karma。必须调整`baseUrl`。我们的测试必须被指定为依赖项。
- 我们必须定义一个启动测试的回调函数。由于 Karma 会沿着路径提供已加载的文件，因此我们在定义模块时必须对此加以注意。
- 我们也应相应地调整路径条目。

此外，我们将测试分组在一个名为`tests`的数组中。在此过程中，我们遍历 Karma 加载的所有文件，以查找匹配`spec.js`的文件。

## 清单 7.29：在 RequireJS 上下文中测试我们的 AngularJS 应用程序的 testRequireConfig.js 文件

```javascript
// we get all the test files automatically
var tests = [];

for (var file in window.__karma__.files) {
  if (window.__karma__.files.hasOwnProperty(file)) {
    if (/spec\.js$/i.test(file)) {
      tests.push(file);
    }
  }
}

require.config({
  paths: {
    angular: '/base/app/bower_components/angular/angular',
    angularRoute:
      '/base/app/bower_components/angular-route/angular-route',
    angularMocks:
      '/base/app/bower_components/angular-mocks/angular-mocks'
  },

  baseUrl: '/base/app/scripts/',

  shim: {
    'angular': { 'exports': 'angular' },
    'angularRoute': ['angular'],
    'angularMocks': {
      deps: ['angular'],
      'exports': 'angular.mock'
    }
  },

  deps: tests,
  callback: window.__karma__.start
});
```

完成这些之后，我们可以将测试定义为 AMD 模块。一如既往，在这个模块中，我们可以使用我们选择的任何测试框架（例如 Jasmine）。

清单 7.30 中的 AMD 模块展示了一些对我们`DataBookService`的测试。

## 清单 7.30：包含 BookDataService 测试用例的 AMD 模块

```javascript
define([
    'angular',
    'angularMocks',
    'services/book_data'
], function (angular, mock) {
    describe('Service: BookDataService', function () {
        var BookDataService;

        // load the application module
        beforeEach(module('bmApp'));

        // get a reference to the service
        beforeEach(inject(function (_BookDataService_) {
            BookDataService = _BookDataService_;
        }));

        describe('Public API', function () {
            it('should include a getBookByIsbn() function', function () {
                expect(BookDataService.getBookByIsbn).toBeDefined();
            });

            it('should include a getBooks() function', function () {
                expect(BookDataService.getBooks).toBeDefined();
            });
        });
    });
});
```

结合 RequireJS 对 AngularJS 应用程序进行测试最初需要稍多一些 effort。然而，在克服早期的障碍后，您可以通过以 AMD 模块的形式提供它们，像往常一样定义测试用例。

## 答案

正如你刚刚所见，使用 RequireJS 实现 AngularJS 是可能的。不幸的是，RequireJS 的最大优势——模块的异步重新加载——被这样一个事实所抵消：每个组件（控制器、服务等）必须在应用程序启动时即可供 AngularJS 使用。当嵌入其他 AngularJS 模块时，这个问题也存在。我们应用程序模块的依赖项也必须可供使用，因此无法异步重新加载。

AngularJS 和 RequireJS 结合的另一个问题是，我们无法执行我们的端到端（E2E）测试。原因是，只有通过`ngApp`指令启动应用程序时，AngularJS 的`ngScenario DSL`才能实现。由于与非 RequireJS 结合必须手动执行引导（Bootstrapping），因此`ngScenario`的实现条件已不复存在。

尽管 AngularJS 和 RequireJS 的混合使用仍然可能具有趣味性。因为我们通过依赖项将 RequireJS 中的每个信息片段都附加到其模块定义上，且只需处理一个`<script>`标签，所以我们就不必手动确保各个应用程序组件按正确的顺序嵌入。使用 RequireJS 时，顺序通过元信息隐式提供给依赖项。然而，通过巧妙的构建过程，可以在不使用 RequireJS 的情况下解决嵌入顺序问题。

根据我们的经验，我们不建议您同时使用 RequireJS 和 AngularJS。相反，我们建议使用优化的构建过程来解决加载顺序问题。原因是，在与 RequireJS 结合时，E2E 测试不再能够执行。因此，一个用于质量保证的重要机制不再可用。对于大型开发团队而言，这是一个不充分的考量，在这些团队中，了解需求的员工创建用户故事场景，而开发人员则将其编写为 E2E 测试。

此外，如果没有 AMD 模块的定义，源代码也不够令人满意。因此，它更难理解。那些不熟悉 JavaScript 或 AngularJS 的新开发人员必须进一步理解另一个复杂的库，以便在实现 RequireJS 的项目中找到联系。能够熟练掌握整个语言生态系统并能了解所有这些框架的 JavaScript 开发人员数量并不多。

## 异步重新加载 AngularJS 组件

你可以找到各种关于如何修补 AngularJS 的博客文章，以便在使用 AngularJS 和 RequireJS 时，应用组件能够异步重新加载。一般来说，我们不建议使用此类解决方案。在当前版本的 AngularJS 中，这些操作可能有效，但无法保证将来的版本也会如此。因此，最好等待并观察框架是否会提供异步重新加载组件的机制。

## 总结

- RequireJS 是一个 JavaScript 框架，支持文件和模块的异步加载。它实现了异步模块定义（AMD）API。
- 通过一个小例子，我们介绍了 AMD 模块的功能和定义。
- 我们展示了如何将 AngularJS 与 RequireJS 结合使用，以及这会带来什么影响。
- 我们讨论了测试同时使用 AngularJS 和 RequireJS 的应用程序所需的步骤。
- 我们通常不建议将 AngularJS 与 RequireJS 一起使用，因为这种组合有很多缺点。

## 移动设备：AngularJS 支持移动设备吗？

由于使用移动设备浏览网页的趋势日益增长，许多人想知道 AngularJS 是否特别适合此类设备。

除了可以独立于 AngularJS 实现的应用程序移动设备优化常用技术（例如响应式网页设计）之外，AngularJS 还提供了一些专门为移动应用程序开发的扩展。因此，我们可以问心无愧地用“是”来回答上述问题。

> **移动设备上的性能**
>
> 虽然 AngularJS 适合为手机和平板电脑创建 Web 应用程序，但你应该注意一些事项。你应该了解在应用程序作用域中存储了哪些数据，因为否则 AngularJS 的脏检查可能会花费很长时间。你可以针对渲染性能优化一些东西。如第 3 章所述，你应该优先使用`ngBind`指令而非等效的表达式来进行模板输出。这样可以避免通过`$interpolate`服务绕行。使用`ngBind`指令的另一个好处是，尚未评估的表达式不会显示出来。

## 支持触摸事件

AngularJS 提供了`ngTouch`模块，其中包含与触摸设备交互的扩展。`ngTouch`不是核心库的一部分。如果你想使用它，必须下载它并通过`<script>`标签嵌入。如果你不使用 Bower，可以在 http://code.angularjs.org/ 下载该模块来管理前端依赖。此外，在定义你的应用程序模块时，你必须将其指定为依赖项（参见清单 7.31）。

### 清单 7.31：嵌入 ngTouch 模块

```javascript
angular.module('app', ['ngTouch']);
```

当你嵌入`ngTouch`模块时，`ngClick`指令会被替换为专为触摸交互设计的替代实现。原因是大多数浏览器在点击和释放事件后 300 毫秒才会向文档发送点击事件。因此，在移动设备上使用`ngClick`指令时，点击交互显得较慢。另一方面，`ngTouch`模块的替代实现会立即做出反应，因此应用程序显得更加流畅。此外，它会抑制原生浏览器事件以避免重复。

你可以通过在简单模板中使用`ngClick`指令，并使用支持触摸的设备访问应用程序来测试此行为（参见清单 7.32）。

### 清单 7.32：在 ngTouch 模块中使用 ngClick

```html
<!DOCTYPE html>
<html ng-app="app">
  <body>
    <div ng-click="click=click+1" ng-bind="click"></div>

    <!-- Scripts -->
    <script src="lib/angular/angular.min.js"></script>
    <script src="lib/angular-touch/angular-touch.min.js"></script>
    <script src="scripts/app.js"></script>
  </body>
</html>
```

> **ngClick 指令的 CSS 扩展**
>
> 在你的应用程序中嵌入`ngTouch`模块时，替代`ngClick`指令会在你用手指按下相应元素时设置另一个名为`ng-click-active`的 CSS 类。这适用于触摸事件以及鼠标点击事件。因此，你可以使用这个 CSS 类来为元素的按下状态设置特殊样式。

## 滑动手势指令

`ngTouch`模块的另一项扩展是对滑动手势的支持。滑动是指用手指在触摸屏上划过。这种手势通常用于显示元素的上下文菜单。

AngularJS 选择的实现基于 jQuery Mobile。不需要将 jQuery Mobile 作为依赖项，因为`ngTouch`包含了该库的相关部分。

该模块为滑动手势提供了两个指令。`ngSwipeLeft`指令处理向左的滑动手势，而`ngSwipeRight`指令处理向右的滑动。

清单 7.33 展示了这些指令的使用。

### 清单 7.33：使用 ngSwipeLeft 和 ngSwipeRight

```html
<!DOCTYPE html>
<html ng-app="app">
  <body>
    <div ng-swipe-right="right=right+1" ng-swipe-left="left=left+1">
      <div>Swipe-right: {{right}}</div>
      <div>Swipe-left: {{left}}</div>
    </div>

    <!-- Scripts -->
    <script src="lib/angular/angular.min.js"></script>
    <script src="lib/angular-touch/angular-touch.min.js"></script>
    <script src="scripts/app.js"></script>
  </body>
</html>
```



```html
</html>
```

#### `$swipe`服务

如果你想实现更复杂的滑动交互，或者希望对滑动的行为有更多控制，仅使用`ngSwipeLeft`或`ngSwipeRight`是无法做到的。因此，`ngTouch`模块包含了`$swipe`服务，上述两个指令在内部也使用了它。通过它，你可以在更低级别处理滑动事件。

该服务的公共 API 包含一个名为`bind`的函数，用于监听事件。支持的不同事件类型列于表 7.1 中。

| 类型 | 描述 | 激活方式 |
|------|-------------|--------------|
| `start` | 交互开始 | `mousedown`, `touchstart` |
| `move` | 交互期间的当前位置 | `mousemove`, `touchmove` |
| `end` | 交互结束 | `mouseup`, `touchend` |
| `cancel` | 当前交互被取消时发生 | `touchcancel` |

表 7.1：`$swipe`服务支持的事件

`bind()`函数的第一个参数是要监控滑动事件的 DOM 元素的引用。

第二个参数是一个配置对象，定义了表 7.1 中事件的回调函数。`start`、`move`和`end`事件的回调函数返回一个包含滑动坐标的对象。因此，你可以访问手指移动的当前 x 和 y 位置。此外，在回调期间，该服务提供了对由滑动事件激活的原生浏览器元素的访问。清单 7.34 展示了一个示例`bind()`函数。

### 清单 7.34：`$swipe`服务的`bind()`函数的回调

```javascript
$swipe.bind(element, {
  'start': function(coords, event) {
    console.log('start', coords.x, coords.y);
  },

  'move': function(coords, event) {
    console.log('move', coords.x, coords.y);
  },

  'end': function(coords, event) {
    console.log('end', coords.x, coords.y);
  },

  'cancel': function(event) {
    console.log('cancel', event);
  }
});
```

作为示例，我们使用`$swipe`服务创建一个指令，允许我们拖动元素，即通过手指手势移动它。这样的对象可以说是可拖动的，因此我们将指令命名为`draggable`。

由于我们希望将此行为用于现有元素，因此我们创建了一个可以作为 HTML 属性实现的指令（参见清单 7.35）。在`link`函数中，我们可以通过`$swipe.bind()`的回调来创建所需的功能。为此，我们使用`move`事件，并通过`top`和`left`属性设置元素的位置。在此过程中，我们确保 CSS 属性`position`相对于其父容器设置。被指令注释的元素必须具有此 CSS 属性。然而，对于该元素，其值为`absolute`。

### 清单 7.35：基于`$swipe`服务的 Draggable 指令

```javascript
angular.module('app').directive('draggable',
```

```javascript
function ($swipe) {
  return {
    restrict: 'A',

    link: function (scope, element) {
      var width = element[0].offsetWidth,
        height = element[0].offsetHeight;

      var toggleActive = function () {
        element.toggleClass('swipe-active');
      };

      $swipe.bind(element, {
        'start': toggleActive,

        'move': function (coords) {
          element.css('left', coords.x - (width / 2) + "px");
          element.css('top', coords.y - (height / 2) + "px");
        },

        'end': toggleActive,
        'cancel': caredit
      });
    }
  };
});
```

此外，我们定义了一个`toggleActive()`函数，一旦该手势处于活动状态，就为元素设置`swipe-active`CSS 类。这样，我们可以通过边框或透明效果更好地可视化这一状态。

现在，我们可以通过创建一个带有 HTML 属性`draggable`的元素，将此指令嵌入到我们的示例中（参见清单 7.36）。

## 清单 7.36：使用我们的`draggable`指令

```html
<!DOCTYPE html>
<html ng-app="app">
<head>
  <meta charset="utf-8">
  <title>Usage of Draggable Directive</title>
  <link rel="stylesheet" href="css/draggable.css" media="screen">
</head>

<body>
  <div class="draggable" draggable></div>

  <div ng-click="click=click+1">
    <div>Click: {{click}}</div>
  </div>

  <div ng-swipe-right="right=right+1" ng-swipe-left="left=left+1">
    <div>Swipe-right: {{right}}</div>
    <div>Swipe-left: {{left}}</div>
  </div>

  <!-- Scripts -->
  <script src="lib/angular/angular.min.js"></script>
  <script src="lib/angular-touch/angular-touch.min.js"></script>
  <script src="scripts/app.js"></script>
  <script src="scripts/directives/draggable.js"></script>
</body>
</html>
```




#### 小结

- 在本节中，我们讨论了 AngularJS 对移动设备的支持程度。
- 通过使用`ngTouch`模块，你可以访问 AngularJS 为移动设备提供的扩展。它包含针对触摸优化的`ngClick`指令实现，还包含用于处理滑动事件的指令。
- 借助`$swipe`服务（它是`ngTouch`的一部分），你可以实现拖放等触摸功能。

# 索引

| 术语 | 页码 |
| :--- | :--- |
| `AJAX` | 212 |
| `allowDuplicates` 属性 | 189 |
| Angular UI | 32 |
| `angular-translate` | 32 |
| AngularJS 生成器 | 269 |
| AngularStrap | 32 |
| 异步模块定义 (asynchronous module definition) | 313 |
| 自动化 | 231 |
| `autoWatch` 属性 | 262 |
| Backbone.js | 269 |
| `background-color` 属性 | 8, 58 |
| `basePath` 属性 | 259 |
| Batarang | 285 |
| 行为驱动开发 (behavior-driven development) | 264 |
| 样板代码 | 25 |
| Bower | 268, 299, 301 |
| `bower install` 命令 | 238 |
| Bower 注册库 | 239 |
| `bower.json` 文件 | 235, 239 |
| 断点 | 279, 281, 283 |
| `browsers` 属性 | 260 |
| 浏览历史 | 33 |
| 回调函数 | 25 |
| 驼峰命名法 (camel case notation) | 14, 52, 64, 67 |
| CamelCase | 271 |
| Chrome | 260 |
| 经典 Web 应用程序 | 23 |
| `click` 函数 | 124 |
| CoffeeScript | 243, 258, 271 |
| 集合过滤器 (collection filter) | 20, 39, 109 |
| `column` 函数 | 101 |
| Common JS | 234 |
| 编译器 | 137 |
| 配置阶段 | 87 |
| `constant` 函数 | 48 |
| 持续集成 | 257, 265 |
| 控制器 | 10, 32, 83 |
| 数据访问对象 | 32 |
| 数据模型 | 25 |
| `date` 过滤器 | 17 |
| 调试 | 279 |
| 装饰器模式 (Decorator pattern) | 276 |
| 深层链接 (deep link) | 127 |
| 深层链接 (deep linking) | 33, 126 |
| 默认任务 | 244 |
| `dependencies` 属性 | 237 |
| 依赖注入 (dependency injection) | 27, 31p., 44, 87, 113, 121, 134p., 174, 192, 199, 215, 219 |
| 依赖解析 | 135 |
| `describe` 函数 | 93, 135 |
| 设计模式 | 21 |
| `devDependencies` 属性 | 237 |
| 指令 | 6, 9, 51 |
| 指令定义对象 (directive definition object) | 14, 53, 56, 198, 206 |
| `directive` 函数 | 13, 52 |
| 脏检查 (dirty checking) | 26, 201p., 204, 288p., 307 |
| 领域特定语言 (domain specific language) | 29, 91 |
| 双星号 | 259 |
| 鸭子类型 (duck typing) | 137 |
| E2E 测试 | 90 |
| ECMAScript | 76 |
| `element` 函数 | 94, 124 |
| Ember.js | 269 |
| Emmet | 291 |
| 端到端测试 | 29 |
| 端点配置参数 | 240 |
| 事件 | 25 |
| 事件处理程序 | 16 |
| 事件监听器 | 25 |
| 事件循环 | 302 |
| `exclude` 属性 | 259, 262 |
| `expect` 函数 | 94 |
| 表达式 | 6, 37p. |
| `factory` 函数 | 45, 52 |
| 胖客户端 | 23 |
| `files` 属性 | 259 |
| 过滤器 | 38 |
| `filter` 过滤器 | 121 |
| `filter` 函数 | 18p. |
| Firefox | 260 |
| 格式化过滤器 (formatting filter) | 20, 37 |
| `frameworks` 属性 | 259, 265 |
| `future` | 304 |
| `gem` | 232 |
| Git | 238, 241 |
| Google | 231 |
| Grunt | 242p., 268 |
| Grunt API | 243 |
| Grunt 服务器 | 273 |
| Gulp | 248 |
| `hashbang URL` | 132 |
| History API | 33 |
| HTML5 模式 | 127, 132 |
| HTTP | 256 |
| `http-server` 模块 | 76, 231 |
| `ignore` 属性 | 236 |
| `initConfig` 函数 | 245, 249p. |
| `inject` 函数 | 135 |
| 接口 | 295 |
| Internet Explorer | 260 |
| 控制反转 | 27 |
| 隔离作用域 | 15, 26, 60, 64, 71 |
| `it` 函数 | 93 |
| Jasmine | 93, 134, 137, 218, 259, 264, 269, 310, 325 |
| JavaScript | 256 |
| Jenkins | 265pp. |
| jQuery | 269 |
| jQuery | 25, 212, 234 |
| jQuery Mobile | 330 |
| JUnit | 266 |
| Karma | 94, 215, 231, 262, 264, 266 |
| `karma init` 命令 | 260 |
| `karma start` 命令 | 257 |
| `karma-junit-reporter` 插件 | 266 |
| `link` 函数 | 15, 53, 57, 67, 202 |
| `link` 属性 | 15, 199 |
| `loadNpmTasks` 函数 | 250 |
| `loadTasks` 命令 | 248 |
| 长轮询 | 257 |
| 松耦合 | 295 |
| `main` 属性 | 236 |
| `map` 函数 | 99 |
| 匹配器 | 94, 137 |
| Maven | 265, 267 |
| `max` 属性 | 8 |
| `min` 属性 | 8 |
| `min` 验证器 | 172 |
| 压缩 (minification) | 254p. |
| Mocha | 149, 264, 269 |
| 模拟对象 | 90 |
| 模型-视图-控制器 (Model-View-Controller) | 21 |
| 模型-视图-视图模型 (Model-View-ViewModel) | 23 |
| 模块 | 31, 295 |
| 模块组合 | 298 |
| `module` 函数 | 87, 135 |
| 模块模式 (Module pattern) | 141 |
| 模块仓库 | 299 |
| 命名冲突 | 299 |
| `new` 运算符 | 47 |
| `ng-app` 指令 | 7, 11 |
| `ng-bind` 属性 | 84 |

## 索引

- `ng-controller` 属性 ..........................................................................................66
- `ng-controller` 指令 ................................................................................................11
- `ng-init` 指令 ..........................................................................................................8
- `ng-min` 插件 ..........................................................................................................256
- `ng-model` 属性 ......................................................................................................6
- `ng-model` 指令 ..............................................................丢弃..................................8
- `ng-repeat` 指令 .....................................................................................................40
- `ng-translate` 模块 ...................................................................................................84
- `ngApp` 指令 .................................................................................................79, 297
- `ngBind` 指令 ...................................................................................................84p., 88
- `ngBindTemplate` 指令 ..............................................................................................88
- `ngClick` 指令 ..............................................................................................130, 330
- `ngDisabled` 指令 ...........................................................................................168, 171
- `ngHide` 指令 ......................................................................................................163
- `ngHref` 指令 ......................................................................................97, 126, 128, 132
- `ngInclude` 指令 ....................................................................................................177
- `ngMock` 模块 ......................................................................................................134p.
- `ngModel` 控制器 .....................................................................................................169
- `ngModel` 指令 ..................................................................................................81, 169
- `ngRepeat` 指令 .........................................................................20, 98, 105, 112, 207
- `ngRoute` 模块 ..........................................................................................35, 78p., 87
- `ngScenario` ........................................................................................................134, 137
- `ngScenario` 框架 ................................................................................................77
- `ngShow` 指令 .............................................................................................163, 167, 170
- `ngSwipeLeft` 指令 .................................................................................................330
- `ngSwipeRight` 指令 ...............................................................................................330
- `ngTouch` 模块 ......................................................................................................329p.
- `ngView` 指令 ...........................................................................................................87

- Node.js ..............................................................................................................76, 231p.
- Node.js 安装程序 ......................................................................................................231
- Node.js 平台 .......................................................................................................257
- `novalidate` 属性 .....................................................................................................168
- npm ......................................................................................................................76, 232
- 观察者 ................................................................................................................16, 26
- Opera ....................................................................................................................260
- `orderBy` 过滤器 ...........................................................................................................112
- `otherwise` 函数 ......................................................................................................34
- `package.json` 文件 ......................................................................................................241
- `path` 函数 ............................................................................................................131
- PhantomJS .............................................................................................................260
- 管道语法 ................................................................................................................17
- `plugins` 属性 ......................................................................................................262
- `polyfill` ....................................................................................................................73
- Polymer 项目 .........................................................................................................73
- `promise` .........................................................................................................212p., 304, 307
- `promises/A+` .........................................................................................................304p., 309
- 原型继承 ............................................................................................................26
- Protractor 项目 .......................................................................................................93
- Q ......................................................................................................................305, 307
- QUnit ....................................................................................................................264

## 索引 339

- QUnit...149
- Rails...269
- `readJSON` 函数...252
- `register` 应用...240
- `registerMultiTask` 函数...246
- `registerTask` 函数...244, 251
- `repeater`...100, 116
- `required` 属性...168
- `required` 指令...168, 171
- `required` 验证器...168pp., 172
- RequireJS...313p., 318, 327
- REST API...23
- `restrict` 属性...15, 57, 206
- 可复用性...31
- 根作用域...25, 59
- 往返原则...22
- `route`...34, 88
- 路由...35, 79
- `row` 函数...103
- Ruby...232
- Ruby on Rails...22
- 运行时环境...231, 235
- Safari...260
- 作用域...11, 25
- `scope` 属性...15, 206
- `scope` 变量...8, 16, 18, 58, 80p.
- `searchpath` 配置参数...240
- 语义版本控制...299
- 服务...32, 44, 112
- 服务工厂...140
- 服务提供者...87, 140
- `shim`...73
- 单星号 | 259
- 单页应用 | 33, 35
- `singleRun` 属性 | 262
- `startsWith` 模式 | 44
- 蛇形命名法 | 14, 52, 64, 67
- Spring MVC | 22
- SSH | 240
- `step` 属性 | 8
- 严格模式 | 141
- Teamcity | 265
- 模板 | 35
- 模板引擎 | 16
- `template` 属性 | 57
- `templateUrl` 属性 | 15, 57, 206p.
- 测试执行环境 | 95
- 测试框架 | 77
- 测试驱动开发 | 29, 75, 89, 279
- 可测试性 | 29, 44, 214

## 340 AngularJS

- 线程............................................................................302
- `toBe` 匹配器.....................................................................94
- `toContain` 匹配器.............................................................94
- `toEqual` 匹配器................................................................102
- `token` 输入字段.................................................................189
- 透明性............................................................................8
- Travis...................................................................................265
- Trygve Reenskaug...................................................................21
- Twitter Bootstrap..................................................................234
- Twitter Flight........................................................................269
- 双向数据绑定...........................6p., 11, 18, 24p., 37, 59, 62, 80, 106, 175, 177, 189, 195, 288
- `type` 属性..............................................................................8
- 类型不匹配...................................................................137
- UI Router..............................................................................35
- Underscore.js...................................................................271, 274
- 单元测试............................................................29, 90, 134
- `uppercase` 过滤器.............................................................38
- V8 引擎.........................................................................231
- 验证器............................................................................168
- 版本控制.....................................................................299
- 视图...................................................................................35p.
- ViewModel.........................................................................23
- 监听器............................................................16, 70, 227
- Web 服务器.......................................................................256
- WebKit..............................................................................260
- WebStorm.......................................................................263
- WebStorm IDE.....................................................................262
- `when` 函数............................................................34, 104
- 通配符...........................................................................259
- XML.................................................................................267
- XMLHttpRequest 对象............................................................212
- xUnit 插件.....................................................................266
- Yeoman...........................................................................231
- `yo` 命令.....................................................................272
- Zend Framework...................................................................22
- `.bowerrc` 文件......................................................................239
- `.gitignore` 文件.....................................................................238
- `$compile` 服务...............................................................192
- `$error` 属性..................................................................173
- `$filter` 服务........................................................113, 121
- `$get` 函数.................................................................49
- `$http` 服务....................................................212pp., 219, 307
- `$httpBackend` 对象.............................................................214
- `$location` 服务........................................................131p., 184
- `$locationProvider` 组件...................................................127
- `$q` 实现..............................................................308
- `$q` 服务.......................................................307, 309
- `$rootScope`.......................................................................80
- `$route` 服务...............................................................87
- `$routeParams` 服务....................................................146, 183

## 342 AngularJS

## AngularJS

AngularJS 是一个用于创建现代客户端 Web 应用程序的 JavaScript 框架。通过其优雅的约定，AngularJS 为常见问题提供了解决方案，使你能够专注于实际任务。

本书将通过一个逐步构建的示例项目来介绍 AngularJS。你将学习基本概念，这些概念使你能够创建结构化、模块化且易于维护的应用程序。特别是，它解释了诸如模块、作用域、服务和指令等概念，并展示了如何有效地使用它们。

有一个单独的章节专门介绍如何连接到基于 REST 的 Web 服务。此外，它还讨论了 Bower、Grunt、Karma 和 Yo 等工具。这些工具可以通过使某些任务变得不必要来为你节省时间。

## 关于作者

Philipp Tarasiewicz 是一位自由职业的技术顾问、作者、演讲者和教练。多年来，他一直专注于企业 JavaScript 领域，特别是 AngularJS，为企业客户提供员工教育和培训，并帮助他们启动新项目。

Robin Böhm 是一位 Web 技术领域的软件开发人员、顾问和作者，专注于企业 JavaScript。多年来，他一直广泛致力于创建客户端 Web 应用程序，并帮助公司进行员工教育培训和项目实施。

![](img/7a003218cea01579a50512a6c0e40f28_351_0.png)

计算机/Web编程

34.99美元
39.99加拿大元

