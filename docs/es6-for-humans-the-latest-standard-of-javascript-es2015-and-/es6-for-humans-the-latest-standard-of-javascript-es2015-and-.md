# 人类的 ES6：JavaScript 最新标准：ES2015 及未来




## 第 1 章

## ES6 入门

如今，全球约 46% 的人口可以访问互联网，这一数字还在稳步增长。在你阅读本书的同时，世界各地有人正在使用互联网服务预订出租车、航班，或预订一家高档餐厅的双人桌；重点是，当今的互联网让人们的生活变得更加便捷。每天都有越来越多的 Web 应用被构建出来，旨在为人们节省时间、提供更高标准的舒适度，或仅仅是为了娱乐。这些应用可以随时随地访问，其中很多都是用 JavaScript 构建的。

根据 StackOverflow 开发者调查，JavaScript 是地球上最常用的编程语言。Web 平台的普遍性促使开发者使用 JavaScript 的频率超过任何其他语言，这推动了 JavaScript 平台如 Node.js、前端框架如 Angular 和 React，以及完整 Web 技术栈如 MEAN（MongoDB、ExpressJS、AngularJS 和 NodeJS）的发展。

本书讨论 ES 2015（通常称为 ES6）及更高版本的核心概念，同时关注最佳开发实践。当你读完本书时，你将对 ES6 的核心概念、特性及其在现代开发工作流中的适用性有很好的理解。

### ES6 规范

多年来，ECMAScript 6（ES6）一直在开发中，但在 2015 年 6 月 17 日，第 109 届 Ecma 大会批准了 ECMA-262 标准的第 6 版，正式对我们熟知和喜爱的 JavaScript 进行了一次重大升级。

JavaScript 的演进，更具体地说 ECMAScript 的演进，主要由社区驱动，TC39 是负责此事的官方委员会。TC39 主要由代表各利益相关方的成员组成，如主要浏览器公司和其他受邀成员。他们定期会面和交流，负责维护和提升 ECMAScript 编程语言的标准，以及扩展其功能的库。在此过程中，他们考虑和评估用于演进 ES 的补充和附加技术的提案。如果你有兴趣了解更多或查看他们的会议议程和纪要，它们都在 GitHub 上在线提供（https://github.com/tc39/tc39-notes）。

ECMAScript 标准的设计过程围绕提案构建，这些提案通常是开发者社区对新特性或现有特性升级的热门请求。由于 TC39 有大量参与者，使得协作设计工作变得困难，通常指定一名或两名委员会成员作为负责人，负责维护提案、进行设计工作并向委员会汇报。

一个提案要成为标准，必须经过多个阶段。提案的初始功能草图，也称为"稻草人提案"，是委员会讨论的第一阶段，如果委员会认为它很重要，它就被视为正式提案。然后，提出的特性需要至少由两个主要的 JavaScript 引擎实现，以获取社区反馈并进一步演进提案。一旦提案通过这些阶段并纳入反馈，TC39 就会批准它，并将其纳入新版 ECMAScript 标准。

### ECMA、ECMAScript 和 JavaScript 的历史

对于不了解 JavaScript 历史的人来说，这么多不同的名称如 JavaScript、ECMAScript、不同的版本号，以及其他流行的分支如 ActionScript、JScript 和 TypeScript（它们都是 JavaScript 的不同形式），很快就会让人感到困惑。

JavaScript 最初由 Brendan Eich 开发，作为 Web 的脚本语言，用于 Netscape 浏览器。这个名字本身是出于营销原因而选择的，因为当时 Java 越来越流行，尽管它与 Java 毫无关系。为了尝试标准化该语言和规范，它被提交给 ECMA International，一个负责信息和通信技术及消费电子产品标准化的机构。最终，在 ECMA-262 中标准化的语言被称为 ECMAScript 或简称 ES，因为 JavaScript 是 Sun 公司（现属于 Oracle）的商标名称。尽管如此，该语言仍然被所有人普遍称为 JavaScript。ECMAScript 作为主干，在各种实现中有许多变体，例如微软为 Internet Explorer 采用的略有不同的版本称为 JScript。ActionScript 是另一个由 Adobe 开发的衍生语言的例子。

最初的版本 ES1 和 ES2 分别于 1997 年和 1998 年发布，但 1999 年的 ES3 版本是一次重大升级，新增了正则表达式、改进的字符串处理、更多的控制语句、更好的错误处理以及 try catch 异常处理等许多我们今天在 JavaScript 中常用的增强功能。它在各种主要浏览器和引擎中以不同形式得到了广泛的基础实现。

ES3 发布之后，ES4 的工作已全面展开，包含许多激进的变更和庞大的范围。更新的特性包括新语法、模块、类、经典继承、私有对象成员、可选类型注解等。提议的变更在社区各利益相关方之间引发了技术和政治上的诸多分歧，导致其于 2003 年被搁置。部分提议的特性被纳入 ActionScript 和 Jscript .NET 等实现中。在收到这些实现的反馈后，TC39 决定于 2005 年恢复 ES4 的工作，但此时社区已出现严重分裂，形成了两个主要派别，在前进方向上存在分歧。

由微软和雅虎等公司支持的替代版本，特性添加较少，主要改进现有规范，被称为 ECMAScript 3.1。由于各派别之间没有达成共识，JavaScript 的未来令人质疑，因此几年内没有重大进展。最终，2008 年 TC39 在 ES4 和 ES3.1 之间达成了共识。ECMAScript 3.1 最终被标准化为



## 一个 JavaScript

原则上，当语言实现有新版本时，这是一个清理的机会，可以移除过时的旧特性，为更新、更好的实现铺平道路。这导致了版本控制，基本上意味着每一段代码都需要与语言的特定版本相关联。例如，在 Python 中，要在 Python 2 和 Python 3 之间切换，需要迁移代码库。但这个选项对 Web 和像 JavaScript 这样的语言是不可行的。你总是会在互联网上遇到旧的代码片段。

ECMA-262 的第五版，也称为 ECMAScript 5，委员会从未发布 ECMAScript 4 标准以避免混淆。ES5 将是一个小的增量更新，他们将致力于下一个主要版本，该版本将比 ES4 更温和，放弃了许多提议的功能，如包、命名空间和早期绑定。这个提议的版本根据会议的性质被代号命名为 ES Harmony。

ES5 于 2009 年 12 月发布，目前是现代浏览器中支持最广泛的版本。它带来了标准库的许多增强功能，并通过严格模式更新了语言语义。

当 ES Harmony 的计划对于单个发布版本来说变得过于雄心勃勃时，他们将第一组最高优先级的功能分开，并将该版本代号命名为 ES。接下来，为了避免像 ES4 那样过早地使用版本号命名，一旦规范成熟，它被称为 ECMAScript 6。

ES6 花了很长时间才成为官方标准。ES6 提案的截止日期是 2011 年 5 月，之后不再考虑主要提案；但从较新的版本开始，TC39 决定对发布进行时间限制，并每年发布一个新版本，包含较小的增量更改，使用当时批准的任何功能。因此，委员会决定改变版本的命名约定，以表示发布年份。因此，ES6 的官方名称在最终发布前更改为 ECMAScript 2015，但 ES6 这个名字多年来被广泛使用，ES2015 仍然通常被称为 ES6，这就是为什么我们在本书中选择将新规范称为 ES6。但展望未来，ES 版本将正式以其发布年份来称呼。所以当我们说 ES6 时，我们指的是 ES2015 中更广泛的更改。

从鸟瞰的角度看 ES6，规范草案分为四个主要部分：目标、要求、手段和主题。目标旨在修复 JavaScript 中的常见陷阱并添加新功能，而要求则声明这两者都需要以不破坏任何现有代码的方式完成，同时保持语言的轻量级特性。

我们不会在这里深入探讨所有目标。但你应该知道，这些目标旨在使它成为编写复杂应用程序、库等的更好语言。保持版本控制简单和增量，ES6 避免了版本控制；这最好用一个 JavaScript 的理念来描述。例如，在 ES6 中，一切都是 ES6 代码：没有仅特定于 ES5 的部分。

ES6 旨在为大型应用程序和库创建提供更好的支持。它提供了诸如类、模块、词法块作用域、迭代器、生成器、对 Promise 的原生语言支持等增强功能。

ECMAScript 标准的发展是社区驱动的，语言的要求和功能将继续在未来的版本中进化以变得更好。

因此，ES 规范旨在升级语言并避免版本控制。这是通过始终向后兼容来实现的，即所有有效的 ES5 代码对于 ES6 代码也是有效的。因此，ES6 设计为没有任何破坏性更改，并且不会移除任何先前的功能。因此理论上，引擎不需要指定版本。所以不是移除现有功能，而是引入新的更好的功能。

这对您，一个 JavaScript 开发者来说意味着什么？由于 ES6 是 ES5 的超集，您将不需要迁移任何旧代码。您现有的 JS 代码也是有效的 ES6 代码。因此，重申一下，您不需要做任何事情。因此，您在现有 JavaScript 中学习和使用的一切都可以带到 ES6 中，它拥有更多更好的工具来添加到您现有的武器库中。如果您希望将当前系统增量地移植到 ES6，这真的很有帮助，因为一切都是向后兼容的。

### 使用 ES6

许多 JavaScript 环境，包括 Web 浏览器和 Node.js，正在积极实施 ECMAScript 6 及更高版本的所有功能。但 ES6 在互联网上普遍支持还需要一些时间。在撰写本书时，最新版本的 Chrome 已实现 97% 的功能，Safari 已实现 100% 的功能。您可以在 http://kangax.github.io/compat-table/es6/ 查看所有引擎当前的特性支持情况。

在 ES6 的所有功能被普遍支持之前，我们需要一种将 ES6 转换为兼容 JavaScript 代码的方法。这就是转译的作用。转译（transformation + compiling）是一种技术，我们使用特殊工具将 ES6 代码转换为其最接近的等效物 ES5 代码，以在旧浏览器或环境中运行。

考虑以下 ES6 代码：

```javascript
const fruits = ["apples", "bananas", "oranges"];
let store = {
    fruits
};
store.fruits; // ["apples", "bananas", "oranges"]
```

这大致转译为：

```javascript
var fruits = ["apples", "bananas", "oranges"];
var store = {
    fruits: fruits
};

store.fruits; // ["apples", "bananas", "oranges"]
```

一些 ES6 功能可以通过使用 polyfills 或 shims 简单地工作，这些是定义旧环境中新行为的简单模式。您也可以通过像 https://jsfiddle.net/ 和 https://babeljs.io/repl/ 这样的 ES6 REPL 在线运行和转译少量的 ES6 代码。但对于较大的项目，您需要使用任何可用的转译器。我们建议使用 Babel，它是当今最受欢迎的 JavaScript 转译器之一。

### 使用 Babel 和 webpack 设置 ES6

为了在您的项目中使用 ES6，您需要一组构建工具来启动和运行。在本节中，我们将讨论一些构建工具，并将设置一个 ES6 模板，您可以将其用作 ES6 项目的入门套件。

#### 使用 Babel 转译

Babel.js 是一个很棒的工具，可以将您的 ES6 代码转译为 ES5 代码，然后可以在当前的 JavaScript 环境中运行。Babel 通过语法转换器支持最新版本的 JavaScript，这些插件允许您使用新语法，而无需等待浏览器支持。

第一步是使用 npm 在本地机器上安装 Babel。

> **注意** 在继续之前，请确保您已安装 Node.js 和 npm。如果您尚未安装 node 和 npm，您可以访问 [https://nodejs.org/en/](https://nodejs.org/en/) 来设置您的开发环境。

```
npm install -g babel-cli
```

现在，您可以使用以下命令从命令行运行任何包含 ES6 代码的文件：

```
babel-node <filename.js>
```

但手动转译每个文件效率不高，在大多数情况下，不是管理大型项目的解决方案。因此，让我们设置一个 ES6 入门套件，它将帮助您自动化构建过程并使开发过程更高效。

#### 设置 ES6 模板

为了转译一个 ES6 项目，我们将使用 babel-loader 和 webpack，它们将帮助我们生成一个包含所有转译代码和相关依赖项的捆绑输出。

##### 启动一个新项目

在终端中运行以下命令集来启动一个新项目：

```
mkdir es6-boilerplate
cd es6-boilerplate
npm init -yes
```

`npm init` 创建一个新项目及其自己的 package.json，`-yes` 标志可防止 npm 提示您任何选项，并将使用默认值。



### 安装 webpack 和 webpack-dev-server

Webpack 是一个非常灵活的模块打包工具，它接收具有依赖关系的模块，并生成代表这些模块的静态资源。我们将使用 webpack 来让 babel-loader 将我们的 ES6 代码转译成传统的 ES5 代码，并生成一个打包后的输出文件。

```
npm install --save-dev webpack
```

除了 webpack，我们还需要使用 webpack-dev-server 来提供我们的应用服务并即时转译代码。但是，请注意 webpack-dev-server 是一个开发服务器，不应在生产环境中使用。

```
npm install --save-dev webpack-dev-server
```

> 要更详细地了解 webpack 和 webpack-dev-server，您可以访问 https://webpack.js.org/concepts/。

### 在项目中安装 Babel

您可以使用以下 npm 包非常轻松地将 babel 安装到您的项目中：

```
npm install --save-dev babel-loader babel-core babel-preset-es2015
```

下一步是配置 babel 以使用 ES2015 预设，方法是在项目根目录下创建一个新文件 **.babelrc**，并添加以下 JSON 内容：

```
{
    "presets": ["es2015"]
}
```

您的 package.json 文件应该或多或少看起来像这样：

```
{
  "name": "es6-boilerplate",
  "version": "1.0.0",
  "description": "ES6 Boilerplate",
  "devDependencies": {
    "babel-core": "^6.24.1",
    "babel-loader": "^6.4.1",
    "babel-preset-es2015": "^6.24.1",
    "webpack": "^2.4.1",
    "webpack-dev-server": "^2.4.2"
  }
}
```

现在，在您的项目根目录中创建一个新的 index.html 文件和 index.js 文件。您当前的项目目录结构应如下所示：

```
├── index.html
├── **node_modules**
├── package.json
└── index.js
```

### 配置 Webpack

下一步是通过在项目根目录创建一个配置文件 - webpack.config.js 来设置 webpack。webpack 配置文件是一个 CommonJS 风格的模块，其中导出了一个配置对象。

```
// webpack.config.js

module.exports = {
    entry: './index.js',
    output: {
        path: './dist',
        filename: 'bundle.js'
    }
};
```

这里，entry 是您项目源代码的路径，webpack 将分析您的入口文件以查找依赖关系，并生成一个打包后的输出（包含所有依赖模块）。请注意，启动时只有入口模块会被执行。

### 添加 Loaders

Loaders 允许您在加载文件时对文件进行预处理。Loaders 提供了一种强大的方式来处理前端构建步骤，可以将不同语言的文件进行转换，例如将 CoffeeScript 转换为 JavaScript，或者将内联图像转换为数据 URL。例如，babel-loader 使用 Babel 来加载 ES2015 文件。

因此，现在修改 webpack.config.js 以使用 babel-loader 处理所有 .js 文件：

```
module.exports = {
    entry: './index.js',
    output: {
        path: __dirname + '/dist',
        publicPath: '/dist/',
        filename: 'bundle.js'
    },
    module: {
        rules: [{
            test: /\.js$/,
            exclude: /node_modules/,
            use: 'babel-loader'
        }]
    }
};
```

以上配置意味着以下几点：

- 1. './index.js' 是应用程序的入口点。
- 2. 输出将生成在 './dist/bundle.js' 中。
- 3. 我们使用 babel-loader 处理每个 .js 文件，排除 node_modules 以避免外部库经过 Babel，从而减慢编译速度。

### 将生成的 bundle.js 脚本添加到您的 index.html

现在我们可以将 bundle.js 脚本包含到我们的 html 文件中以运行代码。

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>ES6 Boilerplate</title>
</head>
<body>
    <h1>ES6 Boilerplate</h1>
    <p>Check console for details</p>
    <div id="main"></div>
    <script src="dist/bundle.js"></script>
</body>
</html>
```

要编译您的 .js 文件，您可以在终端中运行以下命令：

```
webpack
```

您还可以将以下附加标志与 webpack 一起使用：

- webpack 用于一次性构建用于开发。
- webpack -p 用于一次性构建用于生产（压缩）。
- webpack -w 用于在开发过程中进行持续增量构建（快速）。
- webpack -d 以包含源代码映射。

> **专业提示** 我们可以使用 `webpack --progress --colors` 来获得更漂亮的输出，它会在终端中的 webpack 输出中添加进度条和颜色。

### 设置开发服务器

要启动一个开发服务器来测试您的代码，您可以运行以下命令：

```
webpack-dev-server -d --progress --colors
```

这将绑定一个小型 node-express 服务器到 localhost:8080，该服务器提供您的静态资源以及打包文件（自动编译）。当打包文件重新编译时，它会自动更新浏览器页面。

我们也可以将这些 webpack 命令添加到您的 package.json scripts 中。

```json
"scripts": {
    "start": "webpack-dev-server --hot --inline",
    "watch": "webpack -w -d",
    "build": "webpack -p"
},
```

现在，您可以使用以下命令：

- **npm start** 在 localhost:8080 运行一个开发服务器，并监视更改/重新编译。
- **npm run watch** 仅在您自己的 web 服务器上监视更改/重新编译。
- **npm run build** 生成一个压缩的、可投入生产环境的构建。

让我们在 `index.js` 文件中用一个 `helloWorld()` 函数来试试：

```javascript
const helloWorld = () => {
    console.log("Hello! We are all set!");
    console.log("Arrow functions are working");
};

helloWorld();
```

为确保一切正常运行，您可以在终端中运行 `npm start`，并检查服务器在 `http://localhost:8080` 运行。

## 第一章 ES6 入门

您可以运行 `npm run watch` 来查看位于 dist 目录中的 `bundle.js` 文件中转译后的代码，其中将包含这段转译后的 ES5 代码：

```javascript
function(module, exports) {
    "use strict";
    var helloWorld = function sayHello() {
        console.log("Hello! We are all set!");
        console.log("Arrow functions are working");
    };
    helloWorld();
}
```

最后，我们还建议在您的项目中使用 ESLint 来遵循最佳实践并在编写代码时避免错误。您可以在 https://github.com/metagrover/ES6-boilerplate 找到上述样板代码，其中还包含一个 `.eslintrc` 文件，其中包含我们使用的标准规则和配置。

### 总结

JavaScript 是当今网络上最强大的语言之一，并且只会变得越来越强大。ES6，或者官方称为 ES2015 以及后续版本，为 JavaScript 引入了一种新的范式。正如我们将在接下来的几章中看到的，对于传统的 JavaScript 开发者来说，有很多新东西。但是，现有的 JavaScript 开发者需要了解这些新功能，以便在浏览器和框架的世界中越来越多的功能成为主流时保持领先。

JavaScript 的发展速度比以往任何时候都快，转译器和垫片/polyfill 是让您保持在语言发展方向前沿的重要工具。ECMAScript 6 附带了一个非常广泛的新功能列表，这些功能都经过了社区的仔细考虑、深入讨论和选择，成为标准的一部分。现在，轮到我们开发者使用和应用这个新标准到我们的产品中，以更好地服务使用它们的人们。

您可能会问自己，这种改变值得吗？将 ES6 集成到您的项目和工作中是否必要？您是否真的需要改变现有的做事方式？我们想说“是的，值得”，并且通过这本书，我们渴望鼓励您适应这个新世界。即使您在摆脱旧方式时遇到一些阻力，我们建议您坚持下去并改变您的实践。

JavaScript 社区充满活力且动态变化，事物变化迅速。ES6/ES2015 的知识现在已成为 JavaScript 开发者的期望。新的语言结构不仅变得流行，而且现在也得到了广泛支持。掌握 ES6 的内部工作原理将使您能够构建现代应用程序，并让您能够使用更强大的语言，从而帮助您提高编程技能。

通过 ES6，您将能够使用更强大的编程概念，例如实用的面向对象代码以及其他过去根本不可能实现的新功能。我们希望向您介绍现代工作流程和工具，如 Babel 和 Webpack，以使应用程序开发更快、更愉快。然后您将能够衡量代码质量并编写更具可测试性的 JavaScript。



## 第2章

## ES6 新语法

ECMAScript 6 中引入的新特性代表了未来 JavaScript 应用程序构建的基础。在本章中，我们将查看 ES6 语法的变化和新增内容，这些改进修复了以前版本 JavaScript 中存在的许多问题。我们将详细讨论声明变量和定义作用域的新方式。我们还将介绍新概念，如箭头函数、默认函数参数、展开和剩余运算符，以及对象字面量扩展。

### 变量声明：let、const 和块级作用域

在过去，JavaScript 中的所有变量都是使用关键字 `var` 来声明的。这些变量是函数作用域的，意味着它们的作用域在包含它们的函数内部，这对于来自其他语言的开发人员来说有时会令人困惑。因此，如果你需要创建具有自己作用域的新块，则必须将所需代码包装在常规函数或立即调用的函数表达式中。

以下是常规函数级别作用域的示例：

```javascript
var price = 10; // 全局声明

function showPrice() {
    var price = 12; // 使用 var 的局部声明
    console.log(price); // 12
}
showPrice();
console.log(price); // 10
```

以下是使用 IIFE 的函数级别作用域示例：

```javascript
var price = 10; // 全局声明
(function () {
    var price = 12; // 使用 var 的局部声明
    console.log(price); // 12
})();
console.log(price); // 10
```

上面的代码表明变量 `price` 现在被限定在封闭函数内，并且更改不会泄漏到父作用域，在这种情况下是全局作用域。新值 `price = 12` 仅在封闭函数作用域内可用。如果我们将函数作用域替换为块作用域（`'if'` 块），它看起来像这样：

```javascript
var price = 10;
if (price) {
    price = 12;
    console.log(price); // 12
}
console.log(price); // 12
```

上面的代码清楚地表明，`'if'` 块内部的更改泄漏到了父作用域，这告诉我们 `var` 声明绑定到函数作用域，并且不会创建块作用域。在 ES6 之前，JavaScript 使用函数作用域，但块作用域在大多数编程语言中比函数作用域更常见。借助 ES6，我们现在有两种额外的变量声明方式，`let` 和 `const`，它们都声明块级作用域的变量。

#### 使用 let 和 const 进行块级作用域

非常简单，块级作用域意味着在一对 `{ }` 之间创建一个新的作用域。使用关键字 `let` 和 `const` 声明的变量仅存在于围绕它们的最内层块中。在下面的示例中，你认为执行以下代码片段时，什么会打印到控制台？

```javascript
let nbr = 42;
{
    let nbr = 1000;
}
console.log(nbr);
```

值 `42` 被打印到控制台，因为第二个 `nbr` 变量被限定在它声明的块内，并且不会影响块外的 `nbr` 变量，那里它仍然是 `42`。通常，你不会像这样使用块，除非它在控制流语句（如 `if` 条件或循环）中，但这说明了变量是如何进行块级作用域的。我们现在知道 `var` 绑定到函数作用域，而 `let` 和 `const` 是块作用域，这意味着如果你有一组花括号（一段代码块），你就有了一个块作用域。但是，需要注意的是，你只能在块作用域内声明一次变量。另一方面，与 `let` 不同，`const` 创建不可变变量。使用 `const` 创建的变量的值需要在声明期间分配，并且不能在程序中稍后更改。

考虑以下示例：

```javascript
const value = 42;

console.log(value);  // 42
value = 1000;         // TypeError
```

> **注意：** 尝试更改 `const` 变量的值将抛出 `TypeError`。在严格模式下更改不可变绑定只会导致异常 `SetMutableBinding()`。

确保你始终使用值初始化使用 `const` 声明的变量；否则会抛出错误。考虑以下示例：

```javascript
const item;  // SyntaxError: Missing initializer in const declaration
```

如果你需要一个值为 undefined 的常量，你仍然需要这样做：

```javascript
const value = undefined;
```

如果你知道变量的值在整个代码中不会更改，则应使用 `const`；否则使用 `let` 来声明变量。我们建议放弃使用 `var` 声明变量的做法，因为如果你使用块级作用域，它更干净、更高效且易于调试。`let` 和 `const` 避免了误解的来源，特别是对于对块作用域语言有期望的程序员。`let` 和 `const` 如果你尝试在声明它们的块之外访问它们声明的变量，则会抛出异常，并且消除了变量提升，帮助你本地化代码片段的影响。

考虑以下示例以了解 *变量提升* 如何影响使用关键字 `var` 声明的变量：

```javascript
console.log(nbr);  // undefined
var nbr = 42;
```

上面的示例打印 `undefined` 到控制台，因为存在变量提升。当我们使用 `var` 声明变量 `nbr` 时，由于变量提升，它等同于在作用域开头声明变量，并将其值设置为 `undefined`。但如果你将 `console.log` 语句移到声明之后，它会打印数字 `42`，因为进入使用 `var` 声明的变量的作用域，即其周围的函数，会创建一个绑定。然后通过将值设置为 `undefined` 来初始化变量。当执行到达声明时，此变量随后在赋值语句中设置为指定的值。

让我们看看使用 `let` 的类似示例：

```javascript
console.log(nbr); // Reference Error: nbr is not defined
let nbr = 42;
```

这实际上会给你一个 *Reference Error: nbr is not defined*，因为这里不会发生变量提升。这对于调试由于变量在声明之前被使用而导致的不同类型的错误有很大帮助。此引用错误在技术上也被称为 **Temporal Dead Zone (TDZ)** 错误，因为你正在访问一个已声明但尚未初始化的变量。

#### 更多关于 Temporal Dead Zones 的内容

这次讨论的主要要点是，`let` 和 `const` 声明具有临时死区（TDZ）的变量，而使用 `var` 时发生的变量提升形成对比。临时死区中的变量尚未用任何值初始化。创建内存绑定并在变量声明时保持未初始化状态。此时尝试获取或设置变量会引发 **Reference Error**。当程序流到达声明时，变量随后设置为语句中指定的值；否则，如果语句中没有赋值，则设置为 `undefined`。`const` 以类似方式工作，唯一的区别是它需要在声明期间有一个初始化值，该值以后无法更改。

```javascript
let data = true;

if (true) { // 进入新作用域，TDZ 开始
    // 为 "data" 创建未初始化的绑定

    console.log(data); // ReferenceError

    let data; // TDZ 结束，"data" 初始化为 "undefined"
}
console.log(data); // true
```

一旦通过为变量赋值发生初始化，TDZ 就结束了。临时死区主要存在是为了捕获错误。你应该无法在变量声明之前访问它，即使你意外这样做了，也应该收到警告。TDZ 是 `const` 按当前方式工作的最佳解决方案，并且让 `let` 也具有 TDZ 使得在它们之间切换非常容易。TDZ 帮助我们确保运行时变量始终具有正确的值。

```javascript
if (true) {
    console.log(typeof anUndeclaredVariable); // 'undefined'
    console.log(typeof random); // ReferenceError (TDZ)

    let random;
}
```

即使你尝试使用 `typeof` 访问临时死区中的变量，你也会得到异常。`typeof` 是检查变量是否存在的一种安全方式。但如果使用 `let` 在代码中进一步声明了变量，则会抛出 TDZ 错误，因为



当你调用 `typeof` 时，该变量正处于临时死区。因此，始终在作用域顶部声明变量是一种良好的实践。此检查对于使用 `var` 条件性地创建全局变量也很有用。你可以通过以下方式检查全局变量是否存在：

```
if (typeof globalVariable === 'undefined') {
    var globalVariable = { ... };
}
```

**注意**：`const` 用于声明不可变变量，但它不会使变量中包含的值变得不可变。

在以下代码片段中，`obj` 是一个常量，但它指向的值是可变的；因此你可以向它添加属性，但不能将不同的值赋给 `obj`。

```
const obj = {};

obj.key = 42;

console.log(obj.key); // 42

obj = {}; // TypeError
```

如果你愿意，你可以通过冻结它使值本身变得不可变。

```
const obj = Object.freeze({});

obj.key = 42;

console.log(obj);  // {}
```

请记住，`Object.freeze()` 是浅层的。它只会冻结传递给它的对象的属性。只有对象的一级属性会变得不可变，而存储在其属性中的对象则不会。

#### 循环中的变量声明

`for` 循环（`for`、`for-in`、`for-of`）允许你在它们的头部声明变量。但你使用 `var`、`let` 或 `const` 声明这些变量的方式会改变情况。让我们逐一查看这些情况。

在基本的 `for` 循环中，使用 `var` 会为该变量创建一个单一绑定。

```
let arr = [];

for (var i=0; i < 3; i++) {
    arr.push(function () { return i });
}

let value = arr[0]();

console.log(value); // 3
```

你可能预期输出为 0，但输出是 3，因为在循环结束时，变量 `i` 上形成了一个闭包。`i` 被设置为 3，并且循环体中的每个 `i` 实例都引用同一个绑定。因此，函数总是返回 3。现在让我们看看使用 `let` 声明 `i` 的情况：

```
let arr = [];

for (let i=0; i < 3; i++) {
    arr.push(function () { return i });
}

let value = arr[0]();

console.log(value); // 0
```

当我们在 `for` 循环中使用 `let` 时，循环的每次迭代都会获得自己的 `i` 变量，并且创建的任何闭包都会关闭自己的 `i` 值。对于 `const`，它的行为类似于 `var`，因为赋给 `const` 变量的初始值将不再改变。

```
for (const i=0; i<3; i++) {
    console.log(i);
}

// TypeError: Assignment to constant variable (due to i++)
```

#### 使用函数参数和全局作用域的变量声明

如果你在函数内部使用 `let` 声明一个变量，且该变量与参数同名，ES6 会抛出一个静态（加载时）错误。

```
function fn(param) {
    let param; // SyntaxError: Identifier 'param' has already been declared
}
```

使用 `var` 执行同样的操作则什么也不会发生，因为它只是相当于重新声明一个变量。解决此问题的另一种方法是在块内使用 `let`，但新声明的变量只会覆盖参数：

### 箭头函数

JavaScript 中的全局对象（浏览器中是 *window*，Node.js 中是 *global*）一直令人困惑。这就是为什么在 ES6 中引入了区分。考虑以下示例：

```
function fn(param) {
    {
        let param;
    }
}

let notGlobal = "hello";
var isGlobal = "what up";

{ console.log(notGlobal); } // hello
{ console.log(isGlobal); } // what up

global.isGlobal //'what up'
global.notGlobal // undefined
```

全局对象的所有属性都是全局变量。因此，在全局作用域中，*var* 声明和函数声明会创建这些属性。但使用 *let* 和 *const* 声明创建的全局变量不会是全局对象的属性。

箭头函数是 ES6 中另一个主要的语法更新。箭头函数是使用新语法 "*胖*" 箭头 `=>` 定义的函数。这个箭头基于 CoffeeScript 中的一个类似概念。它们通过省略 *function* 和 *return* 语法，使代码更具可读性，并且阅读方式与函数执行方式相同。在本节中，我们将详细讨论箭头函数的用法以及何时使用它们是合理的。

箭头函数的基本语法如下：

```
var fn = data => data;
```

赋值语句左侧的第一部分是提供给函数的参数。如果只有一个参数，你不需要任何额外的语法。下一部分是箭头，然后是要返回的表达式。在这种情况下，它只返回参数。该函数实际上等同于

```
var fn = function(data) {
    return data;
};
```

考虑另一个示例：

```
let getNumber = () => 42;

console.log(typeof getNumber); // function
console.log(getNumber()); // 42
```

在上面的代码中，我们声明了一个名为 `getNumber` 的新函数，并使用箭头函数为其赋值。空括号 `()` 表示该函数没有参数，最后，函数返回值 `42`。在箭头函数中，我们可以省略 `return` 关键字。只要箭头后面指定的表达式没有用 `{}` 包裹，它就会被返回。

```
var getPrice = (quantity, tax) => (quantity * 5) * (1 + tax);
console.log(getPrice(2, .095)); // 10.95
```

请注意，在只有一个参数的情况下，你可以省略括号 `()`，但当有零个或多个参数时，你始终需要使用它。

如果你想指定一个包含多个表达式的更传统的函数块，你需要将函数体包裹在花括号中。但你需要特别使用 `return` 关键字来指定返回值。请查看以下代码片段作为示例：

```
var getPrice = (quantity, tax) => {
  let price = (quantity * 5)
  price *= (1 + tax);
  return price;
}

console.log(getPrice(2, .095)); // 10.95
```

花括号代表函数体。如果你想让箭头函数在函数体外返回一个对象字面量，你必须将该字面量包裹在括号中。例如：

```
var getNumber = data => ({ data: "check", number: 42 });

// 实际上等同于：

var getNumber = function(data) {
  return {
    data: "check",
    number: 42
  };
};
```

用括号包裹的对象字面量表明花括号是一个对象字面量，而不是函数体。

#### 使用箭头函数创建 IIFE

JavaScript 中的函数可以用于创建立即调用函数表达式（IIFE）。你可以定义一个匿名函数并调用它，而无需持有对它的任何引用。这是一种有效的模式，可以将表达式与程序的其余部分隔离开来。

```
var fn = function(number) {
    return {
        getNumber: function() {
            return number;
        }
    };
}(42);

console.log(fn.getNumber());    // 42
```

在上面的代码中，使用 IIFE 来创建 `getNumber()` 方法，该方法使用 `number` 参数作为返回值，确保 `number` 属性实际上是返回对象的私有成员。通过将箭头函数包裹在括号中，也可以实现非常类似的效果。

```
var fn = ((number) => {
    return {
        getNumber: function() {
            return number;
        }
    };
})(42);

console.log(fn.getNumber());    // 42
```

需要注意的一个区别是，箭头函数是函数表达式，而不是函数声明。它们是匿名的函数表达式，没有命名引用，不能用于递归或事件绑定/解绑。

箭头函数不仅仅是漂亮和更简洁的语法。箭头函数确实为我们节省了几行代码和字符，但箭头函数的真正目的是处理函数内部的 `this` 关键字。`this` 在箭头函数内部的行为有所不同。但在我们讨论这一点之前，在下一节中让我们先看看 `this` 关键字通常是如何工作的。

#### 关于 this 的故事

在 JavaScript 中，`this` 是函数的当前执行上下文。让我们看看在以下场景中它意味着什么：

##### 1. 函数调用

在 Chrome 中调用 `getContext()` 函数将在控制台中打印 Window 对象。这是因为 `getContext()` 的上下文是 Window/全局对象。在调用 `getContext()` 时，JavaScript 会自动将 `this` 设置为全局对象，在浏览器中就是 Window。



## 第2章 ■ ES6中的新语法

```javascript
function getContext() {
    console.log(this); // 全局对象或Window
}
```

当`this`用在任何函数作用域之外时，它也指向全局作用域。查看以下代码片段：

```javascript
if (this === window) {
    console.log("this refers to the Global context");
}
```

> **注意**：如果你在严格模式（"use strict"）下，`this`将是`undefined`。

##### 2. 方法调用

方法调用指的是一个对象的方法被调用，这种情况下，`this`是方法调用中拥有该方法的对象。

```javascript
let myObj = {
    name: 'fancy',
    operation: function() {
        console.log(this);
    }
}
```

```javascript
myObj.operation(); // { name: 'fancy', operation: [Function: operation]}
```

方法调用，即在调用`myObj.operation()`时，控制台将打印出`myObj`对象。
现在，让我们尝试这个：

```javascript
let x = myObj.operation;
x(); // Window
```

这里，`x`引用了`myObj`对象内部的`operation()`方法。调用`x()`意味着我们进行的是函数调用而非方法调用，因此，`this`将指向全局（或Window）对象。
如果我们要用`myObj`对象来调用`x`（以进行方法调用），我们必须使用`.call()`方法：

```javascript
let x = myObj.operation;
x.call(myObj); // { name: 'fancy', operation: [function]}
```

##### 3. 构造函数调用

当使用`new`关键字创建对象时，就会发生构造函数调用。考虑以下示例：

```javascript
function Employee(name, department, salary) {
    this.name = name;
    this.department = department;
    this.salary = salary;

    console.log("Welcome " + this.name + "!");
}

let john = new Employee('John', 'Sales', 4000);
// Welcome John!
```

`new Employee('John', 'Sales', 4000)`是`Employee`函数的构造函数调用。执行的结果是一个新对象，`this`指向这个新创建的对象。构造函数`Employee()`在ES6中可以写成一个类，我们将在本书后面讨论。

##### 箭头函数中的this

让我们看看`this`在箭头函数中是如何工作的。箭头函数被设计为词法绑定上下文，这意味着`this`指向定义箭头函数的外围上下文。与普通函数不同，箭头函数不创建自己的执行上下文，而是从其定义的外部函数中获取`this`。考虑以下代码：

```javascript
function Employee(firstName, department, salary) {
    this.firstName = firstName;
    this.department = department;
    this.salary = salary;

    this.getInfo = function() {
        // 外部函数上下文 = Employee对象
        return function () {
            // 内部函数上下文 = 全局对象
            console.log(this.firstName + " from " +
                this.department + " earns " + this.salary);
        };
    }
}

let jim = new Employee('Jim', 'Finance', 5200);
```

在上面的例子中，我们创建了一个名为`Employee`的构造函数，并使用构造函数和`new`关键字创建了一个名为`jim`的新员工对象。为了打印员工信息，我们需要使用`jim.getInfo()`返回的函数。查看以下代码片段：

```javascript
let printInfo = jim.getInfo();
printInfo();  // undefined from undefined earns undefined
```

这里，`printInfo`指向内部函数，由于我们只是进行函数调用，`this`指向全局对象，该对象没有任何`Employee`属性，因此无论何时访问`this`的属性都会产生`undefined`。

让我们看看如果我们用箭头函数替换内部函数，`this`的行为会有什么不同：

```javascript
function Employee(firstName, department, salary) {
    this.firstName = firstName;
    this.department = department;
    this.salary = salary;

    this.getInfo = function() {
        // 外部函数上下文 = Employee对象
        return () => {
            // 内部函数上下文 = 周围上下文 = Employee对象
            console.log(this.firstName + " from " +
                this.department + " earns " + this.salary);
        };
    }
}

let jim = new Employee('Jim', 'Finance', 5200);

let printInfo = jim.getInfo();
printInfo();  // Jim from Finance earns 5200
```

在这种情况下，`this`关键字指向包含箭头函数的函数上下文，这与之前指向全局对象的情况不同。此时，需要注意箭头函数不会在调用时更改其上下文。考虑以下示例：

```javascript
function Employee() {
    this.firstName = 'Mike',
    this.department = 'HR',
    this.salary = 4500,

    this.getContext = () => {
        console.log(this);
    }
}

let mark = new Employee();
mark.getContext(); // [Employee对象]

let context = mark.getContext;
context(); // [Employee对象]（无论是否是函数调用）
```

在上面的例子中，箭头函数的上下文在声明时就已设定，并且无法更改。这里需要注意的一点是，你不能“重新绑定”箭头函数。上下文总是固定的。查看以下代码片段作为示例：

```javascript
var details = {
    number: 42,
    operation: function () {
        return () => console.log(this.number);
    }
};

var details2 = {
    number: 84
};

details.operation().bind(details2)(); // 42
```

在上面的例子中，我们将`details2`的`number`设置为84。但我们要知道，不能将新对象绑定到箭头函数。引擎不会抛出任何错误，它只是完全忽略了bind。所以即使我们使用`details2`对象调用`operation`方法，打印的仍然是42。这也适用于`call`和`apply`。因此，对于箭头函数，调用**bind、call或apply**将无法改变`this`的值。
从这个例子可以清楚地看出，在函数内部，`this`关键字的值是不能改变的。函数内部的`this`值将保持不变，但你仍然可以在箭头函数上使用`bind`、`call`和`apply`。

```javascript
var product = (x, y) => x * y;

console.log(product.call(null, 2, 3));           // 6
console.log(product.apply(null, [2, 3]));       // 6

var multiply = product.bind(null, 2, 3);
console.log(multiply());                       // 6
```

除了词法`this`外，箭头函数还有词法arguments。它们没有自己的arguments数组，而是从父函数继承。箭头函数没有`this`、`super`、`arguments`和`new.target`绑定，因此函数内部的`this`、`super`、`arguments`和`new.target`的值是最接近的包含非箭头函数的值。

> **注意**：通常在JavaScript中，代码之间的额外换行没有意义，代码仍然可以正常工作，但对于箭头函数来说，这是一个问题。我们不能将箭头符号放在新行上。ES6禁止在箭头函数的参数定义和箭头之间换行。

箭头函数的另一个重要方面是，它们不能使用`new`调用，因为它们没有构造方法，不能用作构造函数。当与`new`一起使用时会产生错误。查看下面的示例：

```javascript
var newFn = () => {},
    object = new newFn();  // 错误 - 你不能对箭头函数使用'new'
```

通常在ES5中声明函数时，它有一个`prototype`属性，用于构造函数。但既然你不能对箭头函数使用`new`，那么就不需要prototype。因此，使用箭头函数声明的函数不能访问`prototype`字段。

```javascript
var details = () => 42;
console.log(details.hasOwnProperty("prototype")); // false
```

类似于在严格模式下不允许重复命名参数的非箭头函数，箭头函数在严格或非严格模式下都不能有重复命名的参数。

### 使用箭头函数

所以，只要你有一个简短的单语句内联函数表达式，具有计算返回值，并且函数不使用`this`进行自引用，你就可以用箭头函数来替换它。
如果你有函数使用`var self = this`的技巧来处理`this`问题，或者使用`.bind(this)`调用来正确绑定`this`，箭头函数正是为了解决这个问题而构建的。例如，考虑以下代码片段，我们在点击按钮后等待1秒切换`btn-active`类。

```javascript
$('.btn').on('click', function() {
    var self = this;

    setTimeout(function() {
        $(self).toggleClass('btn-active');
    }, 1000);
});
```



没有箭头函数，我们需要将上下文存储在一个变量中，才能在 `setTimeout` 函数内部访问它。使用箭头函数可以简单地重写为这样：

```
$('.btn').on('click', function() {
    setTimeout(() => {
        $(this).toggleClass('btn-active');
    }, 1000);
});
```

因此，除了更短、更简洁的语法外，箭头函数对 `this` 关键字的处理方式也略有不同，这使得在许多情况下管理代码变得更容易。

### 默认函数参数

与其他语言中的常见模式不同，JavaScript 中的函数在允许你传递任意数量参数调用它们方面是独特的，无论函数定义中声明了哪些参数。这为开发人员提供了在未指定参数时使用任何值的机会。在 ES5 中，如果未指定参数，其值将被设置为 `undefined`。用于为未指定参数设置默认值的常用模式是这样的：

```
function getSum(a,b) {
    a = (a !== undefined) ? a : 1;
    b = (b !== undefined) ? b : 41;

    console.log( a + b );
}

getSum();         // 42
getSum(1, 2);     // 3
getSum(10);       // 51
getSum(null, 6);  // 6
```

ES6 试图简化这个过程，允许我们在函数声明语句本身中设置参数的默认值。

```
var getSum2 = function(a = 1, b = 41) {
    console.log(a + b);
}

getSum2();         // 42
getSum2(1, 2);     // 3
getSum2(10);       // 51
getSum2(null, 6);  // 6
```

当我们调用函数时，如果没有指定任何参数，则使用参数的默认值。指定默认值的语法是参数后跟等号 `=` 和一个表达式。

```
var getAnswer = function(number = 42, item = "universe") {
	console.log(number + " is the answer to " + item);
}

getAnswer(undefined, "life"); // 42 is the answer to life
```

这里，我们将 `undefined` 作为第一个参数传递，ES6 将使用默认值 42。

函数默认值可以不仅仅是像 42 这样的简单值；它们可以是任何有效的表达式，甚至可以是函数调用。你可以使用复杂的表达式作为参数的默认值。默认值表达式是惰性求值的，这意味着它们仅在参数不存在或为 `undefined` 时才运行。

```
var getName = function(firstName = "John", lastName = "Doe") {
	console.log(firstName + " " + lastName);
}

getName("Jane"); // Jane Doe
```

你也可以在用作默认值的表达式中访问其他变量。

```
var defaultName = "John";

var getName = function(firstName = defaultName, lastName = "Doe") {
	console.log(firstName + " " + lastName);
}

getName(); // John Doe
```

你也可以在为参数指定默认值时访问一个函数。

```
var getFirstName = () => "John";

var getName = function(firstName = getFirstName(), lastName = "Doe") {
	console.log(firstName + " " + lastName);

}

getName(); // John Doe
```

在上面几个例子中，如果我们尝试检查参数的数量：

```
var getName = function(firstName, lastName = "Doe") {
	console.log(arguments.length);
}

getName("John"); // 1
```

即使第二个参数获得了默认值，**arguments.length** 只返回传递给它的参数数量。

让我们看一个稍微复杂一点的例子：

```
var getPrice = function(quantity = price, price = 5) {
	console.log(quantity + ", " + price);
}

getPrice(); // ReferenceError: price is not defined
```

将函数声明和参数想象成一个作用域。函数声明的参数位于它们自己的作用域中，即在括号 **(...)** 之间。不要将其与函数体作用域混淆。JavaScript 在评估 `quantity` 时还没有遇到 `price` 的声明，因此它不知道 `price` 的值。默认值表达式中对标识符的引用首先匹配形式参数的作用域，然后才查找外部作用域。

正如我们在 `let` 声明部分所讨论的，ES6 有一个 TDZ（暂时性死区），不允许在变量初始化之前访问它。因此，在上面的例子中，当你尝试在声明之前使用参数时，会发生 TDZ 引用错误。

ES6 中默认参数的另一个很棒的特性是，它们在创建动态函数时也能工作：

```
var getNumber = new Function("number = 42", "return number;");
console.log(getNumber()); // 42
```

### Rest 和 Spread 运算符

JavaScript 一直允许函数传递比函数声明中正式指定的更少或更多的参数，而不会有任何问题。如前所述，默认参数帮助你接受更少的值作为参数，同时仍然让其他参数被赋值。

许多现代编程语言提供了函数接受可变数量参数的能力。ES6 通过 Rest 参数将这个急需的特性引入 JavaScript。你现在可以非常轻松地向函数传递动态数量的参数。如果你想在 ES5 中做到这一点，你必须将所有值放入像数组这样的数据容器类型中。Rest 参数简化了这整个过程。

> **注意** 不要将这个术语与 Web 服务中的 REST 概念混淆。这与 Web 服务中的 REST 无关。这里的 Rest 指的是收集参数并将它们全部放入一个数组中。Spread 指的是将数组（甚至字符串）的元素展开。

让我们看一个例子，

```
var showCollections = function (id, ...collection) {
    console.log(collection instanceof Array);
};

showCollections(42, "movies", "music");  // true
```

`...` 符号是 rest 符号。它位于一个命名参数之前。这个命名参数将成为一个数组，它将收集传递给函数的所有剩余参数。因此在这里，`collection` 被设置为一个数组。为了更清楚地说明，如果我们这样执行上面的程序，

```
var showCollections = function (id, ...collection) {
    console.log(collection);
};

showCollections(42, "movies", "music"); // ["movies", "music"]
```

Rest 参数收集 `id` 参数之后的所有剩余参数，并将其放入一个名为 `collection` 的数组中。除第一个定义的参数 'id' 之外，所有内容都将被放入数组中。

如果我们用只传递一个值（即 id）的方式调用同一个函数，它会输出一个空数组 `[]`。

让我们看看函数的 `length` 属性。如果我们调用 `showCollections.length`，它会返回函数中参数的数量。

```
var showCollections = function (id, ...collection) {};
console.log(showCollections.length); // 1
```

`length` 属性忽略 *Rest 参数*。在这种情况下，它是 1。函数的 `length` 属性只计算命名参数的数量，不包括 rest 参数。现在让我们看看在函数内部检查 `arguments.length` 的情况：

```
var showCollections = function (id, ...collection) {
    console.log(arguments.length);
};

showCollections(123, "movies", "music"); // 3
```

#### 已有 arguments 对象

我们已经有一个 `arguments` 对象，可以用来检查传递给函数的所有参数，而不必特别定义每个参数。记住，函数中可以有命名和未命名参数。在这种情况下，尽管我们在函数定义中有两个参数，`arguments` 对象会引用原始函数调用，而 3 是传递给函数的参数数量。

在 ES4 规范中，*Rest 参数* 本应取代 `arguments`，`arguments` 对象完全被废除，但 ES4 从未实现，而在 ES6 中，这个概念被重新引入，但这次 'arguments' 并没有从语言中移除。

我们可以在函数构造函数中使用 Rest 运算符。看看下面的例子，我们正在创建一个新函数，它有一个 rest 参数，并返回传递进来的第一个参数。

```
var getFirst = new Function("...args", "return args[0]");
console.log(getFirst(1, 2));  // 1
```

#### Spread 运算符

Spread 运算符也用 `...` 表示，放在一个数组之前，它执行的操作与 rest 运算符基本相反。它将一个数组展开，并将值传递给指定的函数。考虑以下例子：

```
let values = [200, 300, 400];
let newSet = [100, ...values, 500]
```

```
console.log(newSet);  // [100, 200, 300, 400, 500]
```

Spread 运算符与 rest 参数密切相关。在这种特定的格式中作为 spread 运算符，`...` 被用作一种连接或插入机制，其中 `values` 数组被插入到现有值之间，以将新形成的数组赋值给 `newSet`。

在 rest 参数的情况下，你可以将多个参数合并为一个数组，而在 spread 运算符的情况下，你可以指定一个可以被拆分为单独参数的数组，然后传递给函数或方法。让我们看看另一个使用 `Math.max()` 方法和 spread 运算符的例子：

```
let numbers = [-25, 100, 42, -1000];
console.log(Math.max(...numbers, 900));        // 900
```

在上面的例子中，`Math.max` 被传递了五个参数，前四个是 -25、100、42 和 -1000，第五个参数我们添加了 900。结果是其中最大的，即 900。因此，spread 运算符将数组中的值展开为函数调用中的参数。

Spread 运算符有助于更轻松地处理作为数组传递给函数的参数。就像 rest 运算符一样，你也可以在函数构造函数中使用 spread 运算符。



如果我们尝试展开一个空数组，例如 `[,,]`，它可能缺少两个值，那么最后一个逗号会被视为尾随逗号而被忽略。展开的参数也将是 `undefined`。请看下面的示例：

```
function printInput(...input) {
    console.log(input);
}

let input = [,,];

printInput(...input); // [undefined, undefined]
```

### 对象字面量扩展

ES6 引入了一些针对对象字面量的新扩展。
要声明对象字面量，目前使用变量时，我们必须采用如下的编码模式：

```
var price = 4.20, quantity = 20;
var invoiceData = {
    price: price,
    quantity: quantity
};

console.log(invoiceData);
```

声明 `price` 和 `quantity` 两次有些冗余，但现在 ES6 提供了一种简写方式，使编写更简单。请看下面的示例：

```
const price = 4.20, quantity = 20;
const invoiceData = {
    price,
    quantity
};

console.log(invoiceData);
```

我们只需列出字段名一次，ES6 的对象字面量足够智能，能够推断出我们想要一个名为 `price` 的字段，并将其值设置为名为 `price` 的变量的值。这种简写方式不仅减少了代码，还使其更易阅读。
ES6 还为我们提供了一种在对象字面量中编写函数的简写符号。例如，请看下面的代码片段：

```
const price = 4.20, quantity = 20;
const invoiceData = {
    price,
    quantity,
    calculateTotal() {
        return this.price * this.quantity;
    }
};
console.log(invoiceData.calculateTotal());
```

在上面的简写符号中，你不再需要 `function` 关键字。当我们在对象字面量中使用函数简写时，`this` 指向代码的执行上下文，就像箭头函数一样。它不指向包含该函数的对象。其行为与箭头函数完全相同。

请注意，你可以在对象字面量中使用动态字段名：

```
const field = 'dynamicRandom';
const price = 5.99;
const quantity = 2;
const invoiceData = {
    [field]: price,
    quantity,
    calculateTotal() {
        return this.price * this.quantity;
    }
};

console.log(invoiceData);
// { dynamicRandom: 5.99,
//   quantity: 2,
//   calculateTotal: [Function: calculateTotal] }
```

对象中的字段被赋值为 `dynamicRandom` 这个名称。实际上，你可以使用一个完整的表达式，使属性命名更加动态：

```
const field = 'dynamicRandom';
const price = 5.99, quantity = 2;
const invoiceData = {
    [field + "-01"]: price,
    quantity,
    calculateTotal() {
        return this.price * this.quantity;
    }
};

console.log(invoiceData);
// { dynamicRandom-01: 5.99,
//   quantity: 2,
//   calculateTotal: [Function: calculateTotal] }
```

你实际上也可以在方法中创建动态字段名。它们也适用于 setter 和 getter。

### 模板字面量与分隔符

JavaScript 中的字符串在历史上功能有限，缺乏其他编程语言可能具备的能力。ES6 引入了模板字面量，为你提供了一种定义字符串的方式，并附加了如下功能：

-   字符串插值
-   嵌入表达式
-   无需技巧的多行字符串
-   字符串格式化

模板字面量使用反引号（`` ` ``）而不是单引号或双引号。模板字面量最终总是产生字符串。模板字面量可以这样编写：

```
let user = `Kevin`;
```

模板字面量允许 **字符串替换**，这为我们提供了一种在字符串中替换任何有效 JavaScript 表达式的方式。模板字面量可以使用 `${ }` 语法包含用于字符串替换的占位符。请看下面的示例：

```
console.log(`Hi ${user}!`); // Hi Kevin!
```

在上面的示例中，模板字面量由反引号（`` ` ``）界定，而字面量内部的插值表达式则由 `${` 和 `}` 界定。
我们还可以替换比变量名更多的内容。模板字面量允许我们使用 **表达式插值** 来嵌入可读的内联数学运算，例如：

```
let a = 10;
let b = 20;
console.log(`Sum of ${a} and ${b} is ${a+b}`);
```

模板字面量还允许你轻松添加多行字符串（无需使用 `\n`）：

```
console.log(`I am line-one
I am line-two`);

// I am line-one
// I am line-two
```

### 标签模板字面量

模板字面量的一种更高级形式是标签模板字面量。标签模板通过在模板字符串前放置一个函数名来转换模板字符串。例如：

```
output`Hi, my name is ${name} and I love ${language}`;
```

这个表达式可以被转换成一个函数调用，该函数接受两种类型的参数：

1.  字面量字符串数组，即 `["Hi, my name is", " and I love", ""]`
2.  替换值，即 `name`、`language`。

字面量字符串的总数总是比替换值的数量多一个。你可以认为每个替换值都被两侧的两个字面量所包围。这就是为什么上面的字面量字符串数组的最后一个元素是一个空字符串。

因此，上面的标签模板可以写成：

```
output(["Hi, my name is ", " and I love ", ""], name, language)
```

标签函数通常使用剩余参数来定义，以便于处理参数。上面的函数可以定义为：

```
function output(literals, ...substitutions) {
    let result = "";

    // 连接字面量字符串和替换值
    for (let i=0; i<substitutions.length; i++) {
        result += literals[i] + substitutions[i];
    }

    // 连接 literals 数组中的最后一个元素
    // 它总是比 substitutions 数组多一个元素
    result += literals[literals.length - 1];

    return result;
}

const name = 'John',
    language = 'JavaScript';

let text = output`Hi, my name is ${name} and I love ${language}`

console.log(text); // Hi, my name is John and I love JavaScript
```

由于这些函数接收模板字符串的各个部分作为参数，因此你可以决定如何使用这些字符串和替换值来确定字符串的最终输出。例如，你可以使用 `output` 函数将所有字符转换为大写、将输入转换为哈希字符串，或者任何你想要的操作。

### 使用 for...of 迭代

在过去的二十年里，在 JavaScript 中，我们一直使用 `for`、`for-in` 和 `forEach`（用于数组）进行迭代。ES6 引入了另一种结构，即 `for...of` 循环，它允许迭代可迭代对象，如数组、映射（Map）、集合（Set）、字符串等。

我们将在本书后面更详细地探讨迭代器和可迭代对象。考虑一个用于迭代数组的简单 `for` 循环：

```
let names = ['matt', 'smith', 'jack'];

for (let i = 0; i<names.length; i++) {
    console.log(names[i]);
}
// matt
// smith
// jack
```

这种格式完全没有问题，但使用新语法，我们不必初始化并跟踪循环计数器变量（`i`）。我们可以用更少、更清晰的语法实现相同的迭代逻辑。请看下面使用 `for...of` 语法编写的代码片段：

```
let names = ['matt', 'smith', 'jack'];

for (let name of names) {
    console.log(name);
}
// matt
// smith
// jack
```

请注意，使用 `for...of` 循环遍历的值必须是可迭代的。可迭代对象就是一个能够产生迭代器的对象，循环随后会使用该迭代器。`for...of` 循环不仅适用于数组，也适用于其他可迭代对象，如 DOM 的 `NodeList` 对象、`arguments` 对象和字符串对象。就像数组一样，`for...of` 循环使得迭代这些非数组序列变得更容易。例如，请看下面的代码片段：

```
for (let char of 'Bye') {
    console.log(char);
}

// B
// y
// e
```

> **注意：** 重要的是不要将 `for...of` 与旧的 `for...in` 循环语法混淆，后者用于遍历对象的可枚举属性（或键）。

当我们将在本书后面详细讨论迭代器和可迭代对象时，`for...of` 循环结构的应用和优势将会更加清晰。本节仅旨在介绍新的 `for...of` 循环语法及其与数组和字符串等数据结构的用法。



 ## 小结

如果你已经是一名 JavaScript 程序员，你可能会意识到我们在编写 JavaScript 时的一些怪癖，尽管它拥有与其他语言类似、相当合理且直接的语法。ES6 试图通过引入大量新语法以及对 JavaScript 现有模式的更改来解决其中的许多问题。有大量新概念等待你去熟悉。许多新引入的模式旨在解决之前版本语言中的现有挑战，并简化 JavaScript 编程过程。它们有助于编写更清晰的代码、更快地调试、用更少的代码行实现逻辑，并避免混淆。

像 `let` 和 `const` 这样的新关键字用于变量声明，为 JavaScript 引入了块级作用域，带来了其他编程语言中常见的功能，使其更容易编写更健壮的代码，并辅助调试过程。箭头函数（Arrow functions）等特性在帮助我们编写更短、更美观的函数的同时，也带来了可用于特定场景的特定行为，比如让 `this` 关键字的使用更加简单。

在本章中，我们还向你介绍了默认值（用于函数参数）、剩余（Rest）和展开（Spread）运算符等新概念。将函数的"剩余"参数收集到数组中的模式现在只需使用三个点。我们还讨论了模板字面量如何赋予我们更多用于模板和字符串操作的能力。最后，我们介绍了新的 `for . . . of` 循环结构，用于遍历可迭代对象，而无需使用额外的计数器变量。

本章我们只介绍了一些重要的新语法特性，但在接下来的几章中，我们将看到更多新特性，如解构（Destructuring）、类与模块（Classes and Modules）、迭代器与生成器（Iterators and Generators）、元编程（Meta Programming）等。敬请期待。

## 第三章

## 解构

对象字面量和数组可能是 JavaScript 中应用最广泛的表示法之一。这些 JavaScript 表示法的流行程度甚至延伸到了语言之外，在 JSON 数据格式中也有体现。对象和数组通常用于在 JavaScript 中对数据进行分组，当我们需要时，存在各种模式来系统地从这些定义好的结构中取得数据。ES6 通过一个称为*解构*（destructuring）的过程进一步简化了这一步。

### 对象与数组的解构

解构基本上是一种将数据结构拆分成更小部分的便捷方式，以便更轻松地访问其数据，并从对象或数组中提取多个值。要更好地理解解构，只需将其视为从对象或数组中进行结构化赋值。请看以下示例：

```
var letters = ['a', 'b', 'c'],
    x = letters[0],
    y = letters[1],
    z = letters[2];

console.log( x, y, z );           // a b c
```

在上面的示例中，我们将值赋给一个名为 letters 的数组，然后利用 letters 变量的索引将 x、y 和 z 变量赋值。让我们再看一个使用对象的类似示例：

```
var numbers = {a: 1, b: 2, c: 3},
    a = numbers.a,
    b = numbers.b,
    c = numbers.c;

console.log( a, b, c );           // 1 2 3
```

在这个示例中，我们使用 numbers.a 的值来给变量 a 赋值，numbers.b 和 numbers.c 同理用于 b 和 c 变量。ES6 引入了一种名为*解构*的全新专用语法，使这种结构化赋值模式更加简单。

这种语法消除了对临时中间变量——letters 和 numbers——的需求。请看以下示例：

```
var [ x, y, z ] = ['a', 'b', 'c'];
var { a: a, b: b, c: c } = {a: 1, b: 2, c: 3};

console.log( x, y, z );           // a b c
console.log( a, b, c );           // 1 2 3
```

> **注意** 我们通常习惯于看到赋值语句右侧出现像 `{a: a, b:b, c:c }` 和 `[x, y, z]` 这样的对象和数组语法。解构颠覆了这一模式，将它们放在左侧并带上变量声明关键字，让你将右侧分解为单独的值，然后将它们赋给左侧的变量。

如前面两个示例所示，在 ES6 之前，从对象和数组中获取信息并将其放入本地变量需要更多的代码。想象一下，如果你需要从非常大的对象或数组中提取值，并将它们存储到同名的变量中。你不得不编写大量代码逐个赋值，但使用解构，这一过程简化为一条赋值语句。使用解构将数据结构拆分成更小的部分，使获取所需数据变得更加容易。此外，ES6 中的解构使用了对象和数组字面量表示法语法，这是 JavaScript 传统用户已经熟悉的。

#### 对象解构语法

让我们更仔细地看看对象解构语法。正如我们所见，对象解构语法为：

```
var { a: a, b: b, c: c } = {a: 1, b: 2, c: 3};
```

在这个示例中，你可以注意到被赋值的变量与返回对象的属性使用了相同的名称。不过它们不必相同，你可以为被赋值的本地变量使用任意名称。但在相同的情况下，语法还可以进一步缩短，省略掉 `"a:  "` 这部分表示法。这条声明语句可以简单地写为：

```
var { a, b, c } = {a: 1, b: 2, c: 3};

console.log( a, b, c );           // 1 2 3
```

使用更短的语法而不是长形式对我们来说非常合理，除非你想将属性赋给不同的变量名，但在使用长形式时有一个重要的细微差别需要注意。请看以下示例：

## 第三章 解构

```
var { a: foo, b: bar, c: baz } = {a: 1, b: 2, c: 3};

console.log( foo, bar, baz );      // 1 2 3
console.log( a, b, c );             // ReferenceError
```

仔细观察这个示例。这个模式看起来非常简单，左侧从右侧对象表示法 `{ a: foo, b: bar, c: baz }` 中获取值。但实际上恰恰相反。它并不是我们通常习惯的 "目标: 来源" 模式，更准确地说，它是反过来的，即 "来源: 目标" 模式。为什么会有这种混淆呢？如果你换个角度来看，这种模式会更有意义。请看以下赋值：

```
var foo = 42, bar = 100;

var obj = { a: foo, b: bar };
var { a: FOO, b: BAR } = obj;

console.log( FOO, BAR );            // 42 100
```

在这个示例中，a 和 b 指的是对象的属性，在对象解构赋值语句中，a 和 b 也代表对象属性。记得在前面我们缩短代码的示例中，我们说过可以省略 `a:` 部分。正是出于这个原因。在这个示例中，如果你去掉语法的 `a:` 和 `b:` 部分，剩下的就是 `FOO` 和 `BAR`。这种语法有时可能会令人困惑，但如果你把它看作对应的属性名和值相互映射，就很容易理解：在这个例子中，foo 被赋给 FOO，bar 被赋给 BAR，使用的是 a 和 b 属性名。

使用对象解构，你实际上可以使用相同的属性值为多个变量赋值。请看以下示例：

```
var { x: foo, x: bar } = { x: 42 };

console.log( foo );  // 42
console.log( bar );  // 42
```

在这种情况下，foo 和 bar 都使用对象的 x 属性来获取值。

在解构声明语句中，你可以根据情况和需求自由选择 `let`、`const` 或 `var`。但一定要确保语句中有赋值，也就是说，语句的右侧是必需的。

```
var { x, y };           // 语法错误！
let { x, y };           // 语法错误！
const { x, y };         // 语法错误！
```

以上所有声明都会因为解构声明中缺少初始化器而导致语法错误。虽然我们知道 `const` 在所有情况下都需要初始化器，但在使用解构时，`var` 和 `let` 也需要初始化器。



## 第三章 解构赋值

#### 使用解构进行赋值

到目前为止，在我们的讨论中，我们只看到使用解构声明语句的情况。但解构也可以用于赋值语句。考虑以下示例，其中使用了前面示例中的 `getChars()` 和 `getNumbers()` 函数：

```
var a, b, c, x, y, z;

[x, y, z] = getChars();
( { a, b, c } = getNumbers() );

console.log( x, y, z );           // a b c
console.log( a, b, c );           // 1 2 3
```

在这个例子中，`x`、`y`、`z`、`a`、`b` 和 `c` 都是在声明后使用解构赋值来赋值的。

> **注意** 你必须始终在对象解构赋值语句周围使用括号。这是因为左花括号用于表示代码块的开始。围绕它的括号表示该花括号应被解释为用于解构赋值语句的表达式。

你也可以在使用解构赋值后更改变量的值。考虑以下示例：

```
let item = {
        name: "Apples",
        quantity: 5
    },
    name = "Oranges",
    quantity = 3;

// assigning different values using destructuring
({ name, quantity } = item);

console.log(name);         // "Apples"
console.log(quantity);     // 5
```

在这个例子中，`name`、`quantity` 和 `item` 在一个声明语句中初始化。然后通过使用解构从 `item` 中获取值，为 `name` 和 `quantity` 赋予新值。

#### 默认值

当使用解构将值赋给一个变量，而对象中没有对应的属性名时，其值将被设置为 `undefined`。例如：

```
var item = {
    name: "Apples",
    quantity: 5
};
var { name, quantity, value } = item;
console.log(name);         // "Apples"
console.log(quantity);     // 5
console.log(value);        // undefined
```

在这个例子中，解构语句中声明了一个额外的变量 `value`，它在 `item` 内部没有对应的属性。它被设置为 `undefined`，而 `name` 和 `quantity` 则从 `item` 中获取各自的值。

此外，你可以选择为额外的变量定义一个默认值，以防指定属性不存在，而不是让它们的值为 `undefined`。为此，只需在属性名后使用等号（`=`）并指定一个默认值，如下所示：

```
var item = {
    name: "Apples",
    quantity: 5
};

var { name = "Oranges", quantity = 3, value = 25 } = item;

console.log(name);         // "Apples"
console.log(quantity);     // 5
console.log(value);        // 25
```

在这个例子中，变量 `quantity` 和 `value` 分别被赋予默认值 3 和 25。由于没有 `item.value` 属性，变量 `value` 使用其默认值 25。这与我们在上一章看到的函数的默认参数值的工作方式类似。

> **注意** 默认值（或如果未指定则为 `undefined`）仅会在 `item` 中缺少该属性时分配给变量。

你也可以在解构赋值语句的完整形式中使用默认值。但此时代码可能开始变得混乱且有点令人困惑。考虑以下示例：

```
var { a, b, c: c = 3, d: FOO = 42 } = {a: 1, b: 2};
console.log( a, b, c, FOO );   // 1 2 3 42
```

在这个例子中，变量 `a` 和 `b` 被声明并设置为右侧对象字面量中的对应属性值，但由于对象中不存在属性 `c`，其值被设置为默认值 3。声明的变量 `FOO` 也被设置为默认值 42，因为对象中不存在对应的属性 `d`。这里你需要记住我们上面讨论的“目标:源”语法，这有时会导致混淆。因此，除非绝对必要，最好避免使用这种混合编码风格。

我们的另一个建议是避免在解构语句内部使用对象或数组作为默认值。这也可能让阅读你的代码的人感到困惑，包括你自己。看看下面的例子：

```
var a = 1, b = 2, c = 3;
var obj = { a: { b: 42 }, c: { b: c } };

( { b: a = { b: b } } = obj );
( { c: b = { b: c } } = obj );
( { a: c = { b: a } } = obj );

console.log( a.b, b.b, c.b );
```

试着猜猜 `console.log` 语句的输出会是什么。如果你猜到了 "2 3 42"，那就完全正确了。但你应该明白为什么这会令人困惑了。

#### 嵌套解构

解构语法，与对象字面量语法非常相似，可用于导航到嵌套对象内部以检索信息。如果你正在解构的值包含嵌套对象或数组，你也可以解构这些嵌套值。这里有一个例子：

```
let items = {
  count : 2,
  name: "fruits",
  apple: {
    quantity: 5,
    value: 25
  },
  orange: {
    quantity: 3,
    value: 5
  }
};

let { apple: { quantity }} = items;

console.log(quantity);      // 5
```

这里的花括号表示我们必须首先进入 `items` 对象内的 `apple` 属性，然后获取 `quantity` 属性。根据我们之前的讨论，冒号（`:`）前的标识符表示我们需要前往的位置，而右侧则分配一个值。如果冒号后面出现花括号，则表示目标嵌套在对象的更深层级中，以此类推。

因为空花括号在对象解构中是合法的，所以在使用嵌套解构时必须非常小心。考虑以下示例：

```
let { apple: {} } = items;
console.log(apple);       // ReferenceError: apple is not defined
```

这个解构语句没有绑定，并且由于右侧的花括号，`apple` 不是一个要创建的变量绑定，而是被用作在 `items` 对象内部进行检查的位置。在这种情况下，如果你想为变量 `apple` 创建一个绑定，使用 `=` 来定义默认值而不是使用 `:` 来定义位置是合理的，例如：

```
let { apple = {} } = items;
console.log(apple);       // {quantity: 5, value: 25}
```

让我们用另一个嵌套数组解构的例子来说明。你可以在整体模式中插入另一个数组模式，解构将深入到嵌套数组中：

```
let fruits = [ "apple", [ "blueberry", "raspberry" ], "orange" ];

let [ fruit1, [ fruit2 ], fruit4 ] = fruits;

console.log(fruit1);      // "apple"
console.log(fruit2);      // "blueberry"
console.log(fruit4);      // "orange"
```

在这个例子中，变量 `fruit2` 将被赋予从 `fruits` 数组中第二个数组（表示浆果）内部获取的值 "blueberry"。解构语句中 `fruit2` 周围的额外方括号对于解包 `fruits` 数组及其内部的浆果数组是必需的。与我们上面看到的对象类似，你可以拥有任何深度的嵌套数组，并且在解构语句中需要有相应的符号来从中获取值。

我们可以构建复杂的表达式来解构对象和数组，以获取正确的值并将其分配给不同的变量，无论对象或数组嵌套有多深，或者来自对象和数组的混合体，只需使用一条解构语句即可。考虑以下示例：

```
let student = {
    name: "Tony",
    courses: {
        english: {
            id: 1,
            score: 7
        },
        math: {
            id: 2,
            score: 9
        }
    },
    scoreRange: [0, 10]
};

let {
    courses: { english },
    scoreRange: [ minScore ]
} = student;

console.log(english.id);       // 1
console.log(english.score);    // 7
console.log(minScore);         // 0
```

此代码将 `student.courses.english` 和 `student.scoreRange[0]` 分别提取到 `english` 和 `minScore` 中。在这个例子中，`courses` 和 `scoreRange` 都是解构模式中的变量，它们从 `student` 对象内的对应属性中获取值。当你需要从复杂的 JSON 结构中获取特定数据或值而无需遍历整个树时，这种方法非常有用。

#### 使用 rest 语法进行解构

在 ES6 中，将 rest 操作符与解构模式一起使用，可以成为变量赋值的一种非常强大而简洁的语法。我们已经在前一章探讨过 rest 模式。现在让我们将其与解构模式结合起来看看。考虑以下示例：

```
var num1, num2, rest;
var x, y, z;

[num1, num2, ...rest] = [1, 2, 3, 4, 5];
[x, y, z] = [1, 2, 3, 4, 5];

console.log(num1);       // 1
console.log(num2);       // 2
console.log(rest);       // [3, 4, 5]
console.log(x, y, z);    // 1 2 3
```

在上面的例子中，我们使用解构为变量 `num1`、`num2` 和 `rest`（仅对剩余部分使用 rest 操作符）赋值。我们对另一组变量 `x`、`y` 和 `z` 做了完全相同的事情。但如果你注意到输出，当我们使用包含五个数字的数组赋值时，前两个值被分配给 `num1` 和 `num2`，而剩余的值被收集到一个数组中并分配给变量 `rest`，因为我们在其后使用了 rest 操作符。将此与第二个解构语句进行比较，其中只有值 3 被分配给 `z`。

这里需要重点注意的是，如果在左侧的剩余元素（rest element）后使用尾随逗号，将会抛出 [SyntaxError](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError)。请看下面的示例：

```
var [a, b,] = [1, 2, 3];
console.log(a, b)          // 1 2
var [num1, ...num2,] = [1, 2, 3];
// SyntaxError: rest element may not have a trailing comma
```

因此，请记住，尽管在简单的解构语句中使用尾随逗号不会产生任何影响，但在解构语句中的剩余元素后不应使用它。

#### 解构参数

除了提供更简单的声明和赋值语法外，解构语法还可以用于传递函数参数。之前讨论的所有解构变体同样适用于参数解构。解构还能很好地与 ES6 的其他函数参数功能混合使用，例如默认参数值和剩余参数。

让我们看一个简单的使用解构数组参数的例子：

```
function sum( [ num1, num2 = 0 ] ) {
    console.log( num1 + num2 );
}
```

```
sum( [ 1, 2 ] );           // 3
sum( [ 1 ] );              // 1
sum( [ ] );                // NaN
```

在上面的示例中，有多个值得注意的地方：当给 `sum()` 函数传入包含两个值 1 和 2 的数组时，它会打印它们的和 3；但当只传入一个值 1 时，输出为 1，这是因为 num2 被赋予了默认值 0。当没有值传递给解构数组时，它打印 NaN（非数字），因为尽管 num2 默认为 0，但 num1 被设置为 undefined。

当你需要为函数提供大量参数时，一种常见的模式是创建一个包含参数属性的对象，然后将该对象传入函数。但这种模式的问题是，仅通过查看函数定义很难猜测函数需要什么输入。你必须遍历函数体才能理解函数所需的不同输入。考虑以下示例，该函数接收一个 options 对象：

```
function createObj(name, value, options) {
    let obj = {};
    obj.x = options.a;
    obj.y = options.b;
    obj.z = options.c;
    obj[name] = value;
    return obj;
}
```

```
let options = {a: 1, b: 2, c: 3};
let testObj = createObj('test', 4, options);
console.log(testObj)// {x:1, y:2, z:3, test:4}
```

在这里，options 对象是函数 createObj 所需的参数之一，但解构可以帮助更好地读取和获取函数内部所需的 options 属性。我们可以使用解构参数重写函数定义，如下所示：

```
function createObj(name, value, {x:a, y:b, z:c}) {
    // 返回对象的代码
}
```

这个函数的行为与前面的示例完全相同，但由于第三个参数使用解构从 options 对象中获取相应的值，因此仅通过查看函数定义就很容易理解函数需要什么输入。此外，这些值可以在函数调用语句本身中进行赋值。因此，你可以使用默认值、混合对象和数组模式，以及与你读取的属性不同的变量名。

> 注意 解构参数的作用类似于常规参数，即如果未传递，则设置为 undefined。

使用对象解构参数的能力为我们带来了额外的好处。它们使我们能够在参数列表的任何位置拥有可选参数。请看以下示例：

```
function printNums( { num1, num2 } ) {
    console.log( num1, num2 );
}
```

```
printNums( { num2: 1, num1: 2 } );         // 2 1
printNums( { num2: 42 } );                // undefined 42
```

在这个示例中，`printNums()` 函数打印作为参数传入解构对象的两个数字，该对象具有 num1 和 num2 属性。注意在第一次函数调用中，如何通过先指定 num2 再指定 num1 来切换参数的顺序。类似地，通过仅指定 num2，你可以实际上将第一个预期参数 num1 的值设置为 undefined。

在此之际，有必要指出解构默认值与函数参数默认值之间的行为差异。请看这个示例：

```
function foo({ num1 = 42 } = {}, { num2 } = { num2: 42 }) {
    console.log( num1, num2 );
}
foo();                  // 42 42
foo( {}, {} );          // 42 undefined
```

在这个示例中，如果不注意输出，可能会觉得我们用两种不同的方式为 num1 和 num2 都声明了默认值 42。第一次函数调用也表明了这一点。但第二次函数调用，当两个空对象传入函数时，情况就不同了。

如果仔细观察，两种声明参数值的方式存在微妙的差异。在上面的示例中，函数 foo 接收两个参数：

- `{ num1 = 42 } = {}`
- `{ num2 } = { num2: 42 }`

当没有参数传递给函数时，第一个参数默认为空对象 {}，但由于它使用了对象解构，命名参数 num1 默认为 42，在这种情况下如此，当作为参数传入的对象没有 num1 属性时也是如此。

对于第二个参数，默认参数值是一个对象 `{ num2: 42 }`。当没有提供第二个参数时，参数默认为此对象。由于左侧的解构对象，当参数默认为该对象时，num2 被设置为 42。但在空对象 `{}` 作为第二个参数传入的情况下，默认值永远不会被使用，`{ num2 }` 解构针对传入的 `{}` 空对象值进行，导致 num2 被设置为 undefined。

### 总结

当你在 JavaScript 中移动数据时，你会开始体会到通过分解对象和数组来单独检查其组件，从而提取特定信息片段的必要性。在 ES6 之前，开发者需要编写相当多的代码来解构他们的数据，但现在他们可以享受 ES6 带来的解构新语法，使他们在代码量方面大大简化了这个过程。

此外，解构有助于使函数的对象参数更加明确。使用解构，你可以拥有默认值，而无需检查属性是否存在于对象中，我们现在可以通过为属性提供默认值来使可选属性更加明确。明确可见的事物使代码更易于维护，因为你不必猜测或阅读整个函数来弄清楚。

# 第4章 ES6 中的类

## ES6 中的类

如果你来自 C++、Java 或 Python 等面向对象编程语言，你一定已经了解类是如何工作的。在 ES6 之前，JavaScript 中从未存在过类，但从早期开始，就已经存在许多模式来模拟经典的面向类的开发。类的概念以各种不同的形式被戏谑，主要是因为类和经典继承无法在 JavaScript 中以干净直接的方式得到支持。这让许多来自其他语言的传统开发者感到困惑，因为 JavaScript 中的类和继承并不是创建相似或相关对象的主要方法。

语法和编码模式试图在原型系统中以隐藏的方式使用面向类的开发，如 `new`、`instanceOf` 和 `constructor` 属性。许多库如 JSClass、Classify.js 等存在，使 JavaScript 感觉像支持传统类。因此，尽管许多传统的 JS 开发者不认为有必要以传统意义上的类存在，但仅仅是库的数量就影响了 TC39 在 ES6 中引入"类"。目标是使它们看起来像真正的类，这是通过引入 `class` 关键字和相关的声明机制来实现的。

## ES6 中的类

类模式在 ES6 的设计过程中被广泛争论和辩论，最终达成了妥协。在这里重要的是要理解，ES6 类的工作方式与其他面向对象语言并不完全相同。也就是说，TC39 仍在 ES6 之后的过程中添加更多功能来增强类，使它们更接近经典定义。

从概念上讲，传统 JavaScript 中不存在类。ES6 中的类本质上只是一个函数。它不过是对象和原型的语法糖，为鼓励互操作性的类模式提供了一种方便的声明形式。ES6 中的这个新 `class` 关键字支持基于原型的继承、构造函数、super 调用、实例方法和静态方法。

让我们看看如何在 ES6 中编写最基本的类声明形式，这与在其他语言中定义类的方式非常相似。请看下面的示例：

```
class Car {
    constructor(brand) {
        this.brand = brand;
```



 # 第4章  ES6 中的类

```
const myTesla = new Car("Tesla");
```

```
console.log(myTesla.hasOwnProperty("brand"));  // true
```

```
console.log(typeof Car);                         // function
```

在本例中，**brand** 是赋值给 myTesla 对象的属性。该对象也可以用对象字面量的形式表示，如下所示：

```
const myTesla = {
    brand: "Tesla"
};
```

上面的例子展示了如何创建一个带可选构造方法（constructor method）的类，当该类的对象被实例化时，构造方法会被调用。ES6 中的类并没有为语言增添任何新功能；它们只是构建对象的更简单语法。传递给 `new Car()` 的任何参数都会作为参数接收，并可用于初始化同一类的实例。因此，**constructor()** 方法是初始化对象属性的地方，而这些属性是可枚举的。此外，由于 **constructor()** 方法是可选的，你可以声明一个空类，如下例所示：

```
class EmptyClass {

}
```

如果你在类内部没有定义 **constructor()** 方法，JavaScript 引擎会为你插入一个空的：

```
class EmptyClass {

    /* JavaScript 插入一个空的构造方法：
    constructor () { }
    */

}
```

既然我们知道了如何在类中初始化属性，下面来看看如何定义方法。类声明允许你在不使用 "function" 关键字的情况下在类上定义方法：

```
class Car {
      constructor(brand) {
          this.brand = brand;
      }

      start() {
          console.log(`Your ${this.brand} is ready to go!`);
      }
}

const myTesla = new Car("Tesla");

myTesla.start();
// Your Tesla is ready to go!
```

在上面的例子中，我们在类定义内部定义了一个 **start()** 方法，它使用 *this* 关键字访问类的 brand 属性。该方法会自动附加到类的原型上，因此是不可枚举的。我们将在本章稍后更详细地讨论这一点以及类方法，但首先，让我们看看在 ES6 中定义类的不同方式。

### 在 ES6 中定义类

就像函数一样，在 ES6 中有两种方式可以定义类。让我们逐一了解。

#### 类声明

如前面的例子所示，类声明非常简单。你使用 "class" 关键字声明一个类，后面跟着类名，按照惯例使用**首字母大写**（TitleCase）格式。这里需要注意的一点是，类名的行为就好像它是类定义内部的常量，这意味着你不能在类内部使用类名来覆盖类：

```
class SimpleClass {
    constructor() {
        SimpleClass = "42";     // 执行时抛出错误
    }
}

SimpleClass = "42";          // 声明后正常工作
```

与函数声明不同，类声明**不会被提升**。与 *let* 和 *const* 类似，类声明存在于暂时性死区（**temporal dead zone，TDZ**）中，直到执行到达类声明的位置。因此，你需要在访问类之前声明它，否则会发生 ReferenceError：

```
const b = new Bike(); // ReferenceError

```

在上面的例子中，由于类尚未声明，它存在于 TDZ 中，因此当你尝试使用 *new* 关键字初始化新实例时，会抛出引用错误。

#### 类表达式

除了类声明之外，在 ES6 中定义新类的第二种方式是通过**类表达式**。它们与函数表达式相同，而且就像函数表达式一样，它们也可以是匿名的。考虑下面的例子：

```
const Circle = class {
    constructor() {
        this.radius = 20;
    }
}
```

注意，在上面的例子中，*class* 关键字后面的标识符缺失了；这使其成为一个**匿名类表达式**。除了变量声明之外，这些类表达式还可以作为参数传递给函数。考虑以下代码片段，其中有一个创建汽车的工厂函数：

```
function carFactory(car) {
    return new car();
}

const Toyota = carFactory(class {
    start() {
        console.log("Your car is ready to roll");
    }
    stop() {
        console.log("Shutting down the engines");
    }
});

Toyota.start();
// Your car is ready to roll

Toyota.stop();
// Shutting down the engines
```

工厂函数将类定义作为参数传入，并返回传入的类的对象。在编程语言中，如果一个实体可以作为参数传递、从函数返回、被修改，并赋值给变量，那么它被认为是该语言的**一等公民**。函数式编程在 JavaScript 中流行的众多原因之一就是因为函数是该语言的**一等公民**，使我们能够充分利用函数并轻松创建高阶函数。在 ES6 中，与函数类似，**类也是该语言的一等公民**，允许将类作为参数传递给函数（如上面的例子所示），并通过类表达式赋值给变量。

### 类方法和访问器属性

在 ES6 之前，你需要使用 `Object.defineProperty()` 来使方法不可枚举，但在 ES6 中，类的所有方法都是不可枚举的。这些方法被附加到原型上，这使得方法可以被类的所有实例共享，提供了一种节省内存的有效方式。

在 ES6 中定义类方法的语法类似于对象字面量方法简写（即，不带 *function* 关键字的函数）：

```
class AeroPlane {
    constructor(model, capacity) {
        this.model = model;
        this.capacity = capacity;
    }
    getData() {
        console.log(`You're flying a ${this.model} aeroplane`);
        console.log(`This plane can fly with ${this.capacity} passengers`);
    }
}
```

```
const jet = new AeroPlane("Jet", 60);

jet.getData();
// You're flying a Jet aeroplane
// This plane can fly with 60 passengers

console.log(jet.hasOwnProperty("getData"));              // false
console.log(jet.__proto__.hasOwnProperty("getData"));    // true
```

上面的例子展示了一个 `AeroPlane` 类，我们在构造每个实例时初始化名为 model 和 capacity 的实例属性。**getData()** 方法声明告诉我们的 `AeroPlane` 类的实例，它们将有一个 **getData()** 方法，每当调用该方法时，将返回该方法的结果。这个 **getData()** 方法会自动被添加到原型上。用 ES5 方式重新创建上述示例的代码如下：

```
function AeroPlane(model, capacity) {
    this.model = model;
    this.capacity = capacity;
}

AeroPlane.prototype.getData = function() {
    console.log("You're flying a " + this.model + " aeroplane");
    console.log("This plane can fly with " + this.capacity + " passengers");
}
```

```
var jet = new AeroPlane("Jet", 60);

jet.getData();

// You're flying a Jet aeroplane
// This plane can fly with 60 passengers
```

ES6 类还允许你在原型上创建**访问器属性**。我们可以在标识符前使用 *get* 和 *set* 关键字分别创建 getter 和 setter 属性。这些属性描述符是不可枚举的，可以使用 `Object.getOwnPropertyDescriptor()` 在类的原型上访问，因为这些属性位于原型对象上。例如，考虑以下代码片段：

```
class AeroPlane {
    constructor(model, capacity) {
        this._model = model;
        this._capacity = capacity;
    }

    get model() {
        return this._model;
    }

    get capacity() {
        return this._capacity;
    }

    set model(model) {
        this._model = model;
    }

    set capacity(capacity) {
        this._capacity = capacity;
    }
}

const jet = new AeroPlane("Jet", 100);

console.log(jet.capacity);
// 100

console.log(Object.getOwnPropertyDescriptor(AeroPlane.prototype, "model"));

/*
{
    get: [Function: get model],
    set: [Function: set model],
    enumerable: false,
```

### 计算属性名

与对象字面量类似，类内部的方法也可以使用计算属性名。这也适用于类的 getter 和 setter 访问器属性。正如在对象字面量中所见，计算属性名可以包裹在 [ ] 中；下面的代码片段展示了一个示例：

```
const methodName = "getColor";
const propName = "color";

class AeroPlane {
    constructor(color) {
        this._color = color
    }

    [methodName]() {
        return this._color;
    }

    get [propName]() {
        return this[`_${propName}`];
    }

    set [propName](value) {
        return this[`_${propName}`] = value;
    }
}

const whiteJet = new AeroPlane("white");

console.log(whiteJet.color);
// white
```

在上面的示例中，我们通过将方法名以及 getter 和 setter 访问器属性名包裹在 [ ] 中，在类定义内部计算它们的名称。我们还在 getter 和 setter 方法中使用字符串字面量来求值动态属性名。

### 类属性与隐私

到目前为止，我们已经了解了如何通过将属性定义在类定义的构造函数方法内部，来将其添加到类的实例上。然而，迄今为止我们看到的所有属性都是公共属性，可以在类定义外部轻松访问，而无需使用 setter 或 getter 方法。关于 JavaScript 中私有属性的讨论已经持续了很长时间。遗憾的是，在 ES6 之前，JavaScript 中从未存在过私有属性，因此它们不得不被模拟出来。最常见的约定是在属性或方法名前加上下划线，这一点我们在前面的示例中已经看到。

借助 ES6，有几种方法可以在类内部管理数据隐私。

#### 使用构造函数环境

将方法和属性存储在构造函数环境内部，通过闭包捕获变量，可以确保这些方法或属性不会被添加到原型上，而只有构造函数及其创建的函数才能访问。

```
class AeroPlane {
    constructor(capacity) {
        this.checkCapacity = function(value) {
            if (capacity >= value) {
                return true;
            }
            return false;
        }
    }
}

const jet = new AeroPlane(200);

console.log(jet.checkCapacity(100));    // true

console.log(jet.capacity);              // undefined
```

在上面的示例中，构造函数环境存储了参数和局部变量，通过使类属性（此处为 `capacity`）在构造函数外部不可访问来保持其私有性。这让私有数据完全安全，无法从类的实例访问。

#### 使用 WeakMap

在我们继续了解 WeakMap 如何帮助在类内部保持数据私有之前，让我们快速看一下 WeakMap 是什么。WeakMap 是 ES6 中引入的一种新数据类型。它们本质上只是键和值的集合，其主要限制是键必须是对象。我们将在本书稍后更详细地学习它们。但就目前而言，你应该注意可以使用以下方式创建 WeakMap：

```
const myMap = new WeakMap();
```

并且你可以在返回的 WeakMap 上使用 set 和 get 方法来存储和检索与其关联的值：

```
const myMap = new WeakMap();

const myObj = { name: "jack" };

myMap.set(myObj, "developer");

console.log(myMap.get(myObj));
// developer
```

如上面的代码片段所示，我们使用对象作为键来在 WeakMap 内部存储值。

WeakMap 的另一个特性是，当对象没有其他引用时，它们不会阻止垃圾回收。因此，使用 WeakMap 来存储类的属性有助于保持数据私有，并且当与类关联的实例被销毁时，这些私有属性也会被销毁。

```
const data = new WeakMap();

class AeroPlane {
    constructor(seats) {
        data.set(this, {
            capacity: seats
        });
    }

    get seats() {
        return data.get(this).capacity;
    }

    set seats(value) {
        data.get(this).capacity = value;
    }
}

const jet = new AeroPlane(200);
console.log(jet.capacity);         // undefined
console.log(jet.seats);            // 200
```

在上面的示例中，我们使用 WeakMap 来保持数据私有，并暴露 setter 和 getter 来与类的私有数据交互。但这需要你将 WeakMap 对外部世界隐藏。只要它不被外部访问，你的属性就会保持安全和私有。

除了 WeakMap 之外，ES6 还提供了另一种新技术来保持数据私有（或者说，防止随意访问），即使用 Symbols，我们将在本书稍后学习。

#### 静态方法和属性

使用类时，你还可以定义属于类本身而非该类的任何特定实例的属性和方法。这些方法和属性与类相关联，而非与类的实例相关联，这通常对于创建应用程序的实用函数很有用。ES6 允许你在方法名前使用 **static** 关键字来轻松创建静态方法：

```
class AeroPlane {
    constructor(capacity) {
        this.capacity = capacity;
    }

    static radio(message) {
        console.log(`Message from broadcast: ${message}`)
    }
}

AeroPlane.radio("Sky is clear");
// Message from broadcast: Sky is clear
```

如前所述，重要的是要注意静态方法和属性直接从它们的类访问，你无法从类的实例访问静态方法或属性。因此，静态方法也无法使用 **this** 访问定义在类的实例上的属性或方法。

在撰写本书时，ES6 不支持使用 **static** 关键字创建属性。有一项提案建议将其添加到语言规范中，但在该提案被接受且实现发布之前，你可以使用静态 getter 和 setter，或者手动将静态属性附加到类上，如下所示：

```
class AeroPlane {
    constructor(capacity) {
        this.capacity = capacity;
    }
}

AeroPlane.color = "white";

console.log(AeroPlane.color);
// white

console.log(AeroPlane.capacity);
// undefined
```

在这个示例中，请注意我们如何能够使用类名访问静态属性，而非静态属性则返回 `undefined`。

### 类继承与 Super 关键字

ES6 引入了 **extends** 关键字，允许创建一个类作为另一个类的子类。继承让我们能够将另一个类的状态和行为整合到我们自己类中。从父类扩展一个类可以防止代码重复。请看下面的示例：

```
class AeroPlane {
    constructor(capacity) {

在上面的示例中，你必须注意我们在类定义内部属性名前添加了 _（下划线）。让我们看看为什么要这样做，通过以下代码片段：

```
class StudyGroup {
    constructor(name) {
        this.name = name;
    }

    set name(newName) {
        this.name = newName;
    }
}

const jsGroup = new StudyGroup("js");

// RangeError: Maximum call stack size exceeded
```

如果你尝试运行上面的代码片段，你会看到一个 RangeError，提示 *Maximum call stack size exceeded*，这是因为你的 setter 属性递归地设置自身，陷入了无限函数调用。因此，你绝不能让 setter 方法的名称与属性名称相同，因为在 setter 内部通过自身名称访问属性 setter 会创建无限递归函数调用。

此时，如果你想知道为什么要使用 setter 和 getter，以下是一些你应该考虑使用它们的原因：

- Setter 和 getter 允许我们将与获取或设置对象属性相关联的行为封装起来，这使得代码更具可扩展性，因为你可以轻松添加更多功能，如输入验证或根据需求对输入数据进行某些转换。此外，它还可以帮助将这些验证或转换功能继承给子类，并根据应用程序需求进行保留或修改。
- 有时，通过属性访问器向用户公开属性的另一种表示形式似乎是个好主意，从而隐藏属性的内部表示。
- 拥有属性访问器方法允许我们设置不同的访问级别，例如，getter 可以是公共的，但 setter 方法对于某些用户组可以是受保护的。

你还应注意，setter 必须恰好有一个形式参数，这意味着你应该为类实例的每个属性创建单独的 setter 和 getter。



 # 第四章 ES6 中的类

```
this.capacity = capacity;
	}

	showCapacity() {
		console.log(`Capacity of this plane: ${this.capacity}`);
	}
}

class FighterPlane {
	constructor(capacity) {
		this.capacity = capacity;
	}

	showCapacity() {
		console.log(`Capacity of this plane: ${this.capacity}`);
	}

	fire() {
		console.log("Loading weapons and firing");
	}
}
```

在上面的示例中，数据属性 `capacity` 和方法 `showCapacity` 在两个类中重复出现。我们可以通过让 `FighterPlane` 继承自 `AeroPlane` 来轻松消除这种重复，从而将 `AeroPlane` 的状态和行为整合到 `FighterPlane` 中。请看下面的示例，其中 `FighterPlane` 类使用 `extends` 关键字继承自父类 `AeroPlane`：

```
class AeroPlane {
	constructor(capacity) {
		this.capacity = capacity;
	}

	
	showCapacity() {
		console.log(`Capacity of this plane: ${this.capacity}`);
	}
}

class FighterPlane extends AeroPlane {
	fire() {
		console.log("Loading weapons and firing");
	}
}

const phantom = new FighterPlane(2);

phantom.showCapacity();
// Capacity of this plane: 2
```

```
phantom.fire();
// Loading weapons and firing
```

如果你想在派生类中也定义一个构造方法，你需要使用 `super()`，它允许在派生类中调用父类的构造方法。`super()` 负责初始化上下文，因此，你必须在构造方法内部访问上下文（`this`）之前调用 `super()`；否则将会导致错误。

如果没有定义构造方法，那么在创建类的新实例时，`super()` 会自动被调用，并传入所有给定的参数，如下例所示：

```
class FighterPlane extends AeroPlane {
	// 无构造方法

	fire() {
		console.log("Loading weapons and firing");
	}
}
```

```
// 等价于

class FighterPlane extends AeroPlane {
	constructor(...args) {
		super(...args);
	}

	fire() {
		console.log("Loading weapons and firing");
	}
}
```

#### 继承静态属性

ES6 允许我们将父类的静态属性继承到子类中。请看下面的示例，其中 `AeroPlane` 的静态方法在其派生类（`FighterPlane`）上被调用：

```
class AeroPlane {
  static radio() {
    console.log("Radio works");
  }
}

class FighterPlane extends AeroPlane {}
```

```
FighterPlane.radio();
// Radio works
```

在这段代码中，一个新的静态 `radio()` 方法被添加到 `AeroPlane` 类中。通过继承，这个方法可以作为 `FighterPlane.radio()` 使用，并且其行为与 `AeroPlane.radio()` 方法相同。

### 方法重写

父类的方法可以在派生类中通过同名方法轻松地被覆盖。例如，查看下面的代码片段，其中父类（`AeroPlane`）的 `fly()` 方法在派生类（`FighterPlane`）中被 overridden：

```
class AeroPlane {
    constructor(capacity) {
        this.capacity = capacity;
    }

    showCapacity() {
        console.log(`Capacity of this plane: ${this.capacity}`);
    }

    fly() {
        console.log("Engines on, and the plane will take off soon");
    }
}

class FighterPlane extends AeroPlane {
    fly() {
        console.log("Engines on, and the plane is gone");
    }

    fire() {
        console.log("Loading weapons and firing");
    }
}

const phantom = new FighterPlane(2);

phantom.fly();
// Engines on, and the plane is gone

phantom.showCapacity();
// 2
```

如果你想访问父类版本的方法，可以使用 `super.fly()`，如下所示：

```
class FighterPlane extends AeroPlane {
    fly() {
        super.fly();
        console.log("Engines on, and the plane is gone");
    }
}
```

这确保了每次在 `FighterPlane` 的实例上调用 `fly()` 方法时，首先会调用父类的方法。除了方法之外，你还可以重写构造方法；例如，考虑以下代码片段：

```
class AeroPlane {
    constructor(capacity, color) {
        this.capacity = capacity;
        this.color = color;
    }
}

class FighterPlane extends AeroPlane {
    constructor(color) {
        // 这架战斗机是双座的
        super(2, color);
    }
}

const phantom = new FighterPlane("grey");

console.log(phantom.capacity);          // 2
```

### 可继承的内置类

ES6 使得从 `Array`、`String`、`RegExp` 等内置类继承变得非常容易，这在需要栈、队列或任何其他链表结构等数据结构时非常有帮助。你还可以利用此功能来根据需要在数组上使用额外的辅助方法，如 `first`、`last`、`shuffle` 等。

考虑下面的代码片段，我们通过扩展 `String` 内置类来实现一个 `ReversedString` 数据类型：

```
class ReversedString extends String {
    print() {
        return this.split('').reverse().join('');
    }
}
```

```
const str = new ReversedString("Awesome");

console.log(str.print());
// emosewA
```

### 小结

ES6 类将 JavaScript 中现有的模式正式化，即构建模拟其他编程语言中基于类的开发模式的伪类。它们使 JavaScript 中的继承更易于使用，并为你提供语法糖，以用更简单的基于类的语法实现 JavaScript 的经典原型继承模型。

在本章中，我们了解了 ES6 中的类如何在底层使用原型继承，即在类原型上定义非静态方法，而所有静态方法都定义在类本身上，使所有类方法都不可枚举。我们还学习了新的基于类的继承语法，它允许你从基类创建派生类，还允许你继承 JavaScript 中的内置类，如 `Array`、`String` 和其他数据类型。总的来说，类是 JavaScript 中非常重要的语法补充，通过提供简洁的语法，使我们能够以更清晰的方式声明自定义对象类型。

# 第五章

# # 模块

JavaScript 在早期刚出现时，是作为网页浏览器的一种简单脚本语言。因此，它最初采用了一种*"所有内容都是共享的"*方法构建而成。但随着时间推移，随着语言的发展以及 JavaScript 应用程序变得越来越复杂，这种加载代码的方法开始变得更加容易出错和令人困惑。相比之下，大多数高级语言都使用模块和包等概念来帮助定义代码作用域。在 ES6 之前，JavaScript 应用程序中的所有内容，包括应用程序不同文件之间的代码，都共享相同的作用域。这就是模块发挥作用的地方，帮助更好地管理和引入代码分离，减少命名冲突等问题并提高数据安全性。JavaScript 开发者被迫求助于外部库来引入模块以帮助解决这些特定问题，但随着 ES6 的出现，模块现在已成为该语言的官方组成部分。

### 模块系统与一点历史

在过去，JavaScript 有过两种主要的模块系统：异步模块定义（AMD）和 CommonJS。CommonJS 是 Node.js 中广泛实现的模块标准。它具有简洁的语法，专为同步加载和服务器设计。另一方面，AMD 是 RequireJS 中的一种流行实现，其语法稍为复杂，使其无需 `eval()` 或编译步骤即可工作。它专为异步加载和浏览器设计。两者在浏览器中都不能原生使用。

当 TC39 决定在 ES6 中实现模块规范时，他们没有采用这两种中的任何一种，而是提出了一种新的实现方法。他们的目标是兼顾 CommonJS 和 AMD 的用户。这种新方法建立在两者之上，并试图解决开发者在这些实现中面临的许多常见问题。

ES6 模块提供了 AMD 和 CommonJS 两者的特性。它们使用紧凑的语法和静态模块结构，有助于代码优化、静态检查和消除无用代码。它还支持像 CommonJS 那样的循环依赖，并支持像 AMD 那样的异步加载和可配置的模块加载。

结束 CommonJS 和 AMD 之间的分裂，拥有一个单一的模块原生标准，还带来了其他优势，例如摆脱了传统上用于使同一文件能在不同系统中使用的 UMD（通用模块定义）模式。



第5章 ■ 模块

### 传统 JavaScript 中的模块模式

为了帮我们更好地理解模块，在进入 ES6 模块之前，我们将在传统 JavaScript 中实现模块模式。简而言之，模块是一个包含内部变量和函数的函数，然后通过返回一个"公共 API"将其暴露给外部环境，该 API 通过那些对数据拥有闭包的方法来访问函数内部的数据。为了说明这一点，让我们使用模块模式编写一个函数：

```
function Message(text) {
    function printMessage() {
        console.log("This is the message: " + text + "!");
    }
    return {
        printMessage: printMessage
    };
}

var printer = Message("test");
printer.printMessage();       // This is the message: test!
```

在这个示例中，变量 printer 被赋值为一个带有参数 "test" 的 Message 函数。Message 是实现模块模式的函数，它为 printer 提供了一个公共 API，使其能够访问其内部函数 printMessage，该方法用于输出 text 参数。

### ES6 中的模块

ES6 中的模块使代码更容易被划分和分离为更小的独立片段，这些片段可以在需要时被重用并注入到其他位置，从而使代码测试变得更加容易，因为模块与主代码是解耦的。模块还有助于异步加载脚本，改善应用的加载时间。但模块系统对 JavaScript 来说并非全新事物。

模块本质上是从其他文件加载到 JavaScript 代码中的 JavaScript 文件。但理解这与传统脚本加载方式的区别非常重要。如果我们将 JavaScript 模块的语义与传统脚本加载进行比较，一些关键差异就会变得明显。首先，模块始终在严格模式下运行，而传统脚本则可以更改模式。如果查看模块的顶层作用域，this 的值是 undefined，而在顶层创建的变量不会出现在共享的全局作用域中。模块内部的任何东西都需要显式导出，我们才能模块外部使用它们。现在让我们通过理解导入和导出绑定的能力来看看模块的核心价值。

### 导出

可以使用 `export` 关键字将模块内部的部分代码暴露给其他模块。你可以从模块中导出变量、函数或类声明。未从模块导出的变量、函数或类在模块外部不可访问。让我们看几个示例：

```
export var text = "ES6 is awesome";
export let name = "Ian Murawski";
export const number = 7;
```

在这个示例中，你导出了使用不同变量声明关键字声明的 text、name 和 number。你还可以从模块中导出函数或类。考虑以下示例：

```
export function add(a, b) {
    return a + b;
}

export class Rectangle {
    constructor(length, width) {
        this.length = length;
        this.width = width;
    }
}
```

在此代码片段中，我们导出了函数 add 和类 Rectangle。你还可以导出模块中已有的私有函数。

```
function multiply(a, b) {
    return a * b;
}
export { multiply };
```

从这个示例中可以看出，不仅可以导出函数声明，还可以导出对模块私有函数的引用。

此时重要的是要理解，只有带名称的函数或类声明才能以这种方式导出，所有这些导出都被称为*命名导出*。除非将匿名函数或类标记为使用 `default` 关键字指定的*默认导出*，否则不能从模块中导出它们。一个模块中可以有多个命名导出，但只能有一个默认导出。可以同时使用两者，但通常最好将它们分开。

### 默认导出

在 Node.js 中，模块仅导出单个值是一种常见做法。即使在使用类作为模型和组件的前端 JS 中，一个模块一个类也是常见做法。ES6 模块旨在选择一个默认导出，该导出将成为主要的导出值。

可以使用 default 关键字将单个变量、函数或类指定为模块的默认导出。一个模块内只能有一个值作为默认导出。在模块内的多个导出上使用关键字会引发错误。默认导出有助于减少从模块导入导出时的语法量。

```
export default function(a, b) {
    return a * b;
}
```

在这个示例中，函数作为默认导出从模块中导出。你可以注意到函数不需要名称，因为它是默认的，而且模块本身代表该函数，允许你省略函数的名称。你也可以为其分配一个名称，并使用 default 导出函数名称。考虑以下示例：

```
function multiply(a, b) {
    return a * b;
}

export default multiply;
```

### 导入

一旦设置了带有相关导出的模块，就可以使用 `import` 关键字在另一个模块中访问它。导入语句包含两部分：要导入的标识符，以及应从这些标识符导入的模块。这是其基本形式：

```
import { identifier1, identifier2 } from "./moduleFile.js";
```

在上面的语句中，identifier1 和 identifier2 是从 moduleFile.js 导入的绑定。

模块使用一个字符串来指定，该字符串表示 `from` 关键字后包含模块的文件路径。请注意，绑定列表看起来像一个解构对象，但请记住它不是。而且绑定类似于使用 `const` 定义的变量，也就是说，你不能使用相同的名称定义其他变量，也不能导入具有相同名称的另一个模块。

使用上述语法，你可以从模块中导入特定的绑定，如下所示：

```
// importing the functions sum and multiply
import { sum, multiply } from "./moduleFile.js";
console.log(sum(1, 7));            // 8
console.log(multiply(2, 3));       // 6
```

在这里，从 moduleFile 模块导入了两个绑定：sum 和 multiply，可以像本地定义的标识符一样使用它们。但让我们考虑一种情况，即你想导入模块中所有可用的导出，而无需显式地按名称声明它们。这可以使用通配符 `*` 并将标识符作为对象的属性导入来完成。

```
// import everything
import * as example from "./moduleFile.js";
console.log(example.sum(1,7));      // 8
console.log(example.multiply(2, 3));  // 6
```

在此代码中，moduleFile 中的所有导出绑定都被加载到一个名为 example 的对象中。

模块中的所有导出都可以作为声明对象的属性来访问。这会创建一个新的命名空间，因为该对象不存在于实际模块中。

重要的是要注意，无论导入语句中导入模块多少次，它只会执行一次。执行导入时，模块会被存储在内存中，并在所有后续导入中重用。存储模块的文件仅执行一次。

### 导入默认值

从模块导入默认值很简单：

```
import multiply from "./moduleFile.js";
```

此导入语句从模块中导入默认值。请注意，与导入命名导出时不同，我们不使用任何花括号。这里的名称 multiply 是局部名称，将用于引用从模块导入的默认值。

对于同时导出默认值和非默认值的模块，你可以使用单个语句导入所有绑定。

```
export let message = "42 is the answer to the everything.";

export default function(a, b) {
    return a * b;
}

import multiply, { message } from "./moduleFile.js";

console.log(multiply (21, 2));  // 42
console.log(message);            // "42 is the answer to the everything."
```

你需要使用逗号来分隔默认的本地名称和非默认的标识符，后者在花括号内列出。确保始终将默认导出放在非默认值之前。

导入默认模块并指定特定本地名称的另一种方式是：

```
import { default as multiply, message } from "./moduleFile.js";
```

在这种情况下，与前面的示例一样，multiply 存储了从 moduleFile.js 导出的默认模块。我们将在本章后面讨论使用关键字重命名标识符。



### 导出已导入的绑定

若需重新导出已导入模块的绑定，可通过`export`语句实现：

```
import { message } from "./moduleFile.js";
// 一些JavaScript代码
export message;
```

此例中，我们从`moduleFile.js`导入绑定`message`，随后再次导出该绑定。也可将两步合并为一步：

```
export { multiply } from "./moduleFile.js";
```

更进一步，可使用通配符`'*'`重新导出所有内容，例如：

```
export * from "./moduleFile.js";
```

上述示例将`moduleFile.js`中的所有内容（包括默认值）从当前模块导出。

### 重命名标识符

在许多情况下，可能不希望使用导入的变量、函数或类的原名，因其可能与代码中其他声明冲突。ES6通过`as`关键字支持对导出和导入进行重命名，从而解决此问题。

```
function sum(a, b) {
    return a + b;
}

export { sum as add };
```

此例中，`sum`是导出函数的本地名称，但该函数以`add`名称导出，需在其他模块中通过导出名`add`导入。

```
import { add } from "./moduleFile.js";
```

类似地，若希望在导入标识符时使用不同名称，可采用如下方式：

```
import { add as sum } from "./moduleFile.js";
console.log(typeof add);          // "undefined"
console.log(sum(1, 2));           // 3
```

此处，导出名`add`以`sum`名称导入。因此，从技术上讲，代码其余部分不存在名为`add`的可用标识符，只能通过`sum`引用。

还可将标识符重命名为`default`以创建默认导出：

```
function multiply(a, b) {
    return a * b;
}

export { multiply as default };
```

类似地，如前所述，也可在重命名后导入默认值：

```
import { default as multiply, message } from "moduleFile.js";

console.log(multiply(1, 2));       // 2
console.log(message);           // "42 is the answer to the everything."
```

由于`default`是JavaScript关键字，不能用作变量、函数或类名。因此，使用`default`重命名导出可视为特殊情况，旨在与非默认导出的定义方式保持一致。若希望使用单条`export`语句同时指定多个导出（包括默认导出），此语法非常实用。

### 加载模块

ES6未具体定义模块加载方式，因其设计目标之一是保持环境无关性。ES6仅定义语法规范，而非创建适用于所有JavaScript环境的规范。浏览器和Node.js需自行决定如何实现`HostResolveImportedModule`（ES6抽象出的加载机制内部操作）。

### Web浏览器中的模块

在Web应用中使用JavaScript的方式众多，但向HTML插入JavaScript的主要方式是通过`<script>`标签。`<script>`标签的`src`属性可告知应用程序脚本位于特定位置。另一种方式是直接在标签内包含代码。也可使用Web Worker加载JavaScript。以下将结合模块情境探讨这些机制。

### 使用`<script>`加载模块

`<script>`元素默认以脚本方式加载JavaScript文件，等同于显式指定`type`属性为`"text/javascript"`。为支持模块，`type`选项新增了`module`值。例如：

```
<script type="module" src="moduleFile.js"></script>
<!-- 加载JavaScript文件并将其识别为模块-->

<script type="module">
<!-- 内联模块 -->
import { multiply } from "./moduleFile.js";
let result = multiply(1, 2);
</script>
```

与脚本不同，模块使用`import`指定需加载的其他文件以正确执行。为使此功能正常工作，脚本元素的模块类型始终表现为已应用`defer`属性。加载脚本文件时`defer`属性是可选的，但加载模块文件时始终应用。当HTML解析器遇到`<script type="module">`元素时，模块文件即开始下载。因此所有模块均按出现顺序执行。

### 在浏览器中异步加载模块

可能已使用过HTML中`<script>`标签的`async`属性。在脚本标签内使用此属性时，浏览器会在获取脚本后立即执行，因此异步脚本的执行顺序是非同步的：无论声明顺序如何，脚本一就绪即执行。模块同样适用此异步执行流程。需注意的是：模块执行前必须先获取其`import`的资源。

### 常见陷阱

模块在代码分区和创建可复用逻辑组件方面极为有用，但有效使用需注意若干陷阱。本节将详细讨论这些问题。

#### 语法

请记住，`export`和`import`仅能在顶层使用，不能成为其他语句或函数的一部分。例如，以下代码将引发语法错误：

```
if (condition) {
    export condition;
    // SyntaxError: 'import' and 'export' may only appear at the top level
}
```

此处，`export`语句是`if`语句的一部分，导致错误。导出和导入不能以任何条件或动态方式执行。在`try-catch`块中使用`import`/`export`语句同样如此。`export`和`import`关键字被专门设计为静态结构，以便文本编辑器在导入模块时能轻松提供模块的可用信息。

#### 只读绑定

ES6的`import`语句仅对相应的变量、函数或类创建只读绑定。因此，导入它们的模块无法更改其值，但导出标识符的模块可以修改其值。例如：

```
// moduleFile.js   starts here
export var message = "Message from moduleFile";

export function setMessage(newText) {
    message = newText;
}
// moduleFile.js   ends here
```

```
// file.js
import { message, setMessage } from "./moduleFile.js"
console.log(message);        // "Message from moduleFile"

setMessage ("New Message");
console.log(message);        // "New Message"

message = "This is another message";     // error
```

上述示例中，我们从模块导入了两个绑定：`message`和`setMessage`。函数`setMessage()`可修改`message`变量的值，但直接更改其值将引发错误。

#### 解构导入语句与变量使用

尽管`import`语句形式类似解构，但本质不同。因此以下代码无效并会引发错误：

```
import { toto: { tata } } from 'someModule'; //error
```

还需注意：`import`语句不应依赖任何需在运行时计算的内容。因此类似以下示例也会引发错误：

```
import toto from "someModule" + tata; //error
```

因此，请确保在从模块导入时不使用此类复杂机制。

#### 使用eval()

不能对模块使用`eval()`，因为模块是其高层抽象结构。`eval()`通常仅接受不包含`import`或`export`的脚本。

#### 模块标识符

以上所有示例中，模块标识符均使用相对路径（如`"./moduleFile.js"`）。浏览器尝试执行此类代码时，按以下方式解析：

| 模式 | 解析为 |
| - | - |
| `/` | 根目录 |
| `./` | 当前目录 |
| `../` | 父目录 |

### 总结

ES6模块为扩展JavaScript功能提供了新途径，助力代码组织与模块化语义代码库维护。ES6引入`import`、`export`和`default`等新关键字，使模块使用成为可能。由于ES6融合了多种优势，您无需再使用UMD或CommonJS、AMD等额外模块系统。

通过模块可编写可复用、封装更佳的代码。与脚本不同，模块不修改全局作用域，降低出错概率。若需在其他位置使用模块中的值，必须显式导出所有值。



 # 第 6 章

## ES6 中的 Symbol

自 1996 年首次标准化 JavaScript、ECMA 尝试制定标准规范以来，JavaScript 中一直存在五种原始数据类型：Boolean、Number、String、Undefined 和 Null，每种类型都代表一个值。但现在 ES6 引入了一种全新的原始数据类型——Symbol。在本章中，我们将详细介绍这种新的原始类型及其应用。

### Symbol

Symbol 代表一个唯一的值，其核心是一个唯一的标识符，保证永远不会与其他任何 Symbol 冲突。ES6 中的 Symbol 可以通过工厂函数创建。可以使用 Symbol() 方法来创建一个新的 symbol。请看下面的例子：

```
const foo = Symbol();
console.log(typeof foo);    // "symbol"
```

每次调用工厂函数时，都会创建一个新的、唯一的 symbol。对 symbol 类型使用 typeof 的输出结果是 `"symbol"`，这是识别 symbol 的主要方式：

> 注意：ES6 中的 Symbol 不像其他原始类型那样具有字面量形式。

可选地，在创建 Symbol 时，你还可以通过向 Symbol() 方法传递一个字符串作为参数来为其添加一个标签：

```
const chocolate = Symbol("this is my chocolate");

console.log(chocolate);
// Symbol(this is my chocolate)

console.log(chocolate.toString());
// "Symbol(this is my chocolate)"
```

作为参数传入的标签不会影响 Symbol 的值。除了作为在打印时描述该 symbol 的字符串外，它不会产生其他任何影响。当你对返回的 symbol 调用 `.toString()` 方法时，这个标签也很有用，该方法会将 symbol 转换为字符串。当你使用 `console.log()` 输出 symbol 时，以及在可能的错误消息中，都会显示这个标签。这对于调试目的很有帮助。

注意，你不应该使用 `new` 关键字来创建 symbol。Symbol 没有对象构造函数，因此你不能使用 `new` 关键字来创建 Symbol：

```
const bar = new Symbol();         // Type Error
```

如前所述，symbol 始终是唯一的，两个 symbol 永远不可能是相同的。然而，你可以创建具有相同标签的多个 symbol，但返回的 symbol 始终是唯一的。请查看以下代码片段示例：

```
const kit = Symbol("hello");
const kat = Symbol("hello");

console.log(kit === kat);     // false
```

或者你也可以简单地尝试，

```
Symbol() !== Symbol()      // true
```

因此，symbol 始终是唯一的，在各种情况下都非常有用。让我们在下一节中看看它的应用。

### Symbol 的应用

就其性质而言，Symbol 主要用作唯一的属性键，因为 symbol 永远不会与对象的任何其他属性（symbol 或字符串）冲突，这在不希望冒覆盖对象原生属性风险的场景中非常有帮助。Symbol 还通常用于为类或对象类型的内部使用创建匿名（或在某种程度上是私有的）属性。请看下面的例子，我们有一个具有一些"公共"属性的 Person 对象：

```
let Person = {
			name: "John",
			age: 14,
			location: "New York"
}
```

现在假设我们想向 Person 对象添加一个私有方法。我们可以使用 Symbol 来实现，如下所示：

```
let votingEligibility = Symbol();
Person[votingEligibility] = function() {
	return this.age >= 18;
}
```

现在让我们看看 Person 对象，你可以看到一个匿名方法已经被添加到其中。

```
console.log(Person);
// {name: "John", age: 14, location: "New York"}

// 如果你在较新版本的 Google Chrome 中运行此代码，
// 你还会看到 - Symbol(): [Function] 属性
```

你也可以在这里使用计算属性键，这是我们已经在前面的章节中讨论过的：

```
let Person = {
    name: "John",
    age: 14,
    location: "New York",
    [Symbol()]: function() {
        return this.age >= 18;
    }
}
```

Symbol 属性是不可枚举且匿名的。因此，在使用 `for...in` 循环时，遍历过程中无法访问对象的 symbol 属性，并且由于它是匿名的，它不会出现在 `Object.getOwnPropertyNames()` 方法返回的结果数组中。然而，你可以使用 `Object.getOwnPropertySymbols()` 来获取 symbol 属性。例如：

```
Object.getOwnPropertyNames(Person);
// ["name", "age", "location"]

Object.getOwnPropertySymbols(Person);
// [Symbol()]
```

让我们看看在前面创建 Person 对象的例子中如何使用 `Object.getOwnPropertySymbols()`。

```
let canVote = Object.getOwnPropertySymbols(Person)[0];

Person[canVote]();

// false
```

> **注意** 我们看到 `Object.getOwnPropertySymbols()` 返回与对象关联的属性 Symbol 数组，因此这些属性是可访问的，并不是私有的。但使用 symbol，我们确实具有不会轻易发现这些属性的优势。

你还可以通过使用创建的引用将该属性绑定到 Person 对象来实现这一点。回想一下我们是如何创建 symbol 的：`let votingEligibility = Symbol();`。因此，

```
Person[votingEligibility]();
// false
```

类似地，自定义类也可以这种方式创建私有成员，使其对类中定义的其他方法私有可用。动态创建的 symbol 值可以保存到作用域类变量中，该变量只能由类的内部方法访问，从而保护私有属性免受不必要的随意发现。例如，请看下面的代码片段：

```
const age = Symbol("age");

class Person {
    constructor(value) {
        this[age] = value;
    }

    getAge() {
        console.log(this[age]);
    }
}

const jack = new Person(23);

console.log(jack);
// Person {}

console.log(jack.age);
// undefined

console.log(jack[Symbol("age")]);
// undefined

jack.getAge();
// 23
```

在这个例子中，我们有一个 Person 类，它使用 Symbol 创建了一个私有属性来存储人的年龄。从代码片段中可以明显看出，该属性是不可枚举的，因为它返回一个空对象，并且只能通过暴露的 `getAge()` 方法访问。由于 Symbol 始终是唯一的，通过使用相同的标签 `age` 创建 symbol：`Symbol("age")` 来访问私有属性只会创建一个新的唯一 symbol，它将无法访问对象的所需属性。

### Symbol 与注册表

到目前为止，我们已经讨论了本地 symbol 以及如何通过获取引用来访问它们。Symbol 也可以被放置在一个全局注册表中，从那里可以在称为领域（realm）的不同上下文中访问它们。领域是代码片段存在的上下文，例如你的应用程序正在运行的页面，或者页面中的 `<iframe>`，或者具有包含全局变量和加载模块的上下文的 Web Worker。Symbol 具有在整个运行时全局 symbol 注册表中可用的特殊能力，你可以使用以下方法将 symbol 添加到运行时全局注册表中：

`Symbol.for(key)` 和 `Symbol.keyFor(symbol)`。

#### Symbol.for(key)

此方法在运行时全局 symbol 注册表中查找具有给定键的现有 symbol。如果注册表中存在具有该键的 symbol，则返回该 symbol。如果在注册表中找不到具有该键的 symbol，则会创建一个新的 symbol。例如，请看下面的代码片段，其中第一次调用 `Symbol.for('myCar')` 会创建一个 symbol，将其添加到注册表中，并返回它；而第二次调用则返回相同的 symbol，因为该键已经在运行时全局 symbol 注册表中了：

```
Symbol.for('myCar') === Symbol.for('myCar')
// true
```

运行时全局注册表跟踪使用 `Symbol.for(key)` 方法创建的所有 symbol，这些 symbol 可以跨不同的领域访问。例如，在网页的任何位置创建的 symbol 也可以在 iframe 的上下文中访问。请查看下面的代码片段（你可以在浏览器的控制台中运行此代码）：

```
// 创建一个 iframe
const frame = document.createElement('iframe');

// 将 iframe 附加到 body
document.body.appendChild(frame);

console.log(Symbol.for('temperature') === frame.contentWindow.Symbol.for('temperature'));
// true
```

在上面的例子中，网页上下文中的全局 Symbol 与 iframe 中的全局 Symbol 是相同的，这告诉我们使用 `Symbol.for(key)` 方法创建的 symbol 可以跨不同的领域访问。



## 第 6 章 ■ ES6 中的符号

#### Symbol.keyFor(symbol)

`Symbol.keyFor(symbol)` 从全局符号注册表中检索与给定符号关联的键，该符号是在被添加到注册表时与此键关联的。当在注册表中找不到该符号时，它返回 `undefined`。

```javascript
const symbol = Symbol.for('myHouse');

console.log(Symbol.keyFor(symbol)); // myHouse

const myCat = Symbol();

Symbol.keyFor(myCat); // undefined
```

### 内置符号

ES6 提供了一系列在语言规范中预先定义的符号，其中大多数暴露了 JavaScript 对象的某些元属性和行为。一些广为人知的符号如下：

- `Symbol.hasInstance` — 它允许我们确定一个对象是否是某个构造函数的实例。它在内部被 `instanceof` 运算符调用。
- `Symbol.iterator`，我们将在本书后面深入探讨。它持有对象的默认迭代器。数组、Set、Map 和 WeakMap 在其结构中都存在一个不可枚举的 `[Symbol.iterator]` 属性。

### 小结

符号是 ES6 引入 JavaScript 的一种新的原始类型。当你希望避免属性键的名称冲突时，它们可能非常有帮助，尤其是在你不希望冒险覆盖对象的本地属性的情况下。符号由于不可枚举，通过创建受保护的属性提供了优势，防止它们被随意发现，因为你必须专门去查找符号才能找到它们。

## 第 7 章 ■ 数组与集合

到目前为止，我们已经涵盖了许多 ES6 提供的新特性和改进功能。在本章中，我们将进一步查看数组和集合等数据类型的增强。ES6 为 JavaScript 语言带来了许多新的静态属性和方法，扩展了内置原生对象和对象的功能。我们将查看 Array 类型的扩展特性以及一些现在已成为语言原生组件的新数据结构抽象。

### 数组与新方法

多年来，许多流行的 JavaScript 库如 Underscore 和 Lodash 不断演进，其中数组数据结构是最常被扩展的特性之一。因此，随着时间的推移，在语言中内置支持这些库所普及的一系列数组功能变得越来越有必要。在本节中，我们将介绍所有新的 ES6 数组功能，并查看一些它们大显身手的用例。

我们现在有了一些新的静态方法和原型方法，语言通过这些方法来帮助你创建、操作、填充和过滤数组。首先让我们看看静态方法：`Array.from()` 和 `Array.of()`，然后我们将探索 ES6 中为数组引入的新原型方法。

#### Array.from()

在 ES6 之前，为了将类数组对象（例如 `arguments` 和 `NodeList`）转换为真正的数组，我们需要使用一些技巧，比如在 `arguments` 或 `NodeList` 上调用 `Array.prototype.slice.call()` 来将对象转换为数组。考虑下面的例子，你有一个存在于 DOM 中的元素列表：

```html
<ul>
    <li>Apple</li>
    <li>Mango</li>
    <li>Orange</li>
    <li>Litchi</li>
    <li>Banana</li>
</ul>
```

```javascript
var listItems = document.querySelectorAll('li');

// 将 NodeList 转换为数组
listItems = Array.prototype.slice.call(listItems);

// 对新转换的数组使用 Array 方法
listItems.map(item => { console.log(item.innerText) });

// Apple
// Mango
// Orange
// Litchi
// Banana
```

使用 ES6，我们现在有了更直接的解决方案，将上述示例中描述的类数组对象转换为数组。新的 `Array.from` 静态方法允许我们从任何类数组或可迭代对象创建数组。不过，在继续之前，让我们先清楚地理解我们所说的类数组对象到底是什么。这些只是具有 `length` 属性或索引元素的简单对象。例如，考虑以下对象：

```javascript
const customers = {
    '0': 'matt',
    '1': 'ian',
    '2': 'mikhail',
    '3': 'akia',
    '4': 'vincent',
    length: 5
};
```

现在，如果我们要将此对象转换为数组，我们可以使用 `Array.from()` 语法简单地这样做：

```javascript
Array.from(customers).forEach(customer => {
    console.log(customer);
});
```

在这个例子中，我们只是将 `customer` 对象传递给了函数，然后它返回了一个由各元素组成的数组。让我们看看具体的 `Array.from` 语法：

```
Array.from(arrayLike[, mapFn[, thisArg]])
```

在此语法中，`arrayLike` 是一个类数组或可迭代对象，`mapFn` 是一个可选参数，是可以应用于数组每个元素的映射函数。`thisArg` 是另一个可选参数，其值在 `mapFn` 执行时作为 `this` 使用。

`Array.from()` 尝试检查其第一个参数是否是可迭代对象，如果是，则使用迭代器生成要复制到返回数组中的值。但如果你传递的是类数组对象，它的行为与 `slice()` 或 `apply()` 相同，即只是简单地遍历数值命名的属性，从 0 到对象的长度来访问值。

如果我们现在使用带有可选的 `mapFn` 参数的上述示例，它看起来会是这样的：

```javascript
Array.from(customers, customer => {
    console.log(customer);
});
```

注意我们如何移除了 `forEach` 方法，并使用第二个参数作为映射函数来遍历结果数组。

#### Array.of()

ES6 中引入的另一个非常便捷的方法是 `Array.of()`，它可以让你轻松创建元素数组。`Array.of()` 接受一系列项目作为参数，并将它们作为数组返回给你。考虑以下示例：

```javascript
let arr = Array.of(10, 20, 30, 40);
console.log(arr); // [10, 20, 30, 40]
```

你可能想知道这与传统的 `Array(…)` 构造函数有何不同。你也可以使用数组构造函数并通过 `Array()` 语法创建数组。但是，`Array.of()` 和 `Array` 构造函数的区别在于它们处理单个数字作为参数的方式。`Array` 构造函数有一个非常奇怪的行为：如果只向它传递一个数字，它不会创建一个包含该数字值的单元素数组，而是构造一个以该数字为长度的空数组。所有元素都被设置为 `undefined`。`Array.of()` 静态方法修复了这个问题，现在它是数组的首选函数形式构造函数。看看下面的例子：

```javascript
const arr1 = Array.of(10);
console.log(arr1); // [10]
console.log(arr1.length); // 1

const arr2 = Array(10);
console.log(arr2); // [,,,,,,,,]
console.log(arr2.length); // 10
```

正如你在上面的示例中看到的，`Array.of(10)` 创建了一个单数字数组 `[10]`，而 `new Array(10)` 方法创建了一个长度为 10 的空数组。说了这么多，我们需要理解为什么首先要使用构造函数，而不是像 `a = [1, 2, 3]` 这样的字面量语法。你会使用构造函数，例如，当你有一个回调函数应该将传递给它的参数包装成数组时，或者如果你必须子类化 `Array` 并希望在子类的实例中创建或初始化元素时。

现在我们已经了解了 ES6 中为数组引入的两个新的静态方法，让我们更深入地了解一下 ES6 中为 Array 原型引入的新原型方法。

#### 新的 Array 原型方法

既然我们已经讨论了创建数组的新方法，让我们来看看 ES6 中引入的新数组方法如何帮助我们轻松访问和操作存储在数组中的数据。在本节中，我们将介绍新的 `Array.prototype` 方法，包括 `entries()`、`keys()`、`values()`、`find()`、`findIndex()`、`fill()` 和 `copyWithin()`，并看一些实际示例来理解这些方法如何帮助我们轻松访问和操作数据。

#### Array.prototype.entries( )

`entries()` 方法返回一个值序列，但使用迭代器逐个揭示它们，而不是一次性作为数组全部返回。你将在后面的章节中更详细地学习迭代器，但让我们在这里快速介绍一下迭代器。

迭代器从集合中一次访问一个项目，同时跟踪其在该序列中的当前位置。它提供了一个 `next()` 方法，返回序列中的下一个项目。`next()` 方法返回一个具有两个属性的对象：`done` 和 `value`，其中 `value` 表示集合中的项目，`done` 是一个布尔值，当可迭代对象的所有元素都已遍历完毕时为 `true`。

每个可迭代对象（例如数组）必须实现可迭代协议，这意味着该对象（或其原型链上的某个对象）必须具有一个带有 `Symbol.iterator` 键的属性。`Symbol.iterator` 是另一个 ES6 新增功能，我们将在本书后面讨论，但现在，请将其视为一种定义永远不会与普通对象键冲突的特殊键的方式。

让我们看看数组，它是一个可迭代对象，以及它可以生成的用于消费其值的迭代器：

```javascript
const arr = [11,12,13];
const itr = arr[Symbol.iterator]();

itr.next(); // { value: 11, done: false }
itr.next(); // { value: 12, done: false }
itr.next(); // { value: 13, done: false }

itr.next(); // { value: undefined, done: true }
```



既然我们已经对迭代器和可迭代对象有了基本的理解，那么让我们深入探讨一下`Array.prototype.entries()`方法如何帮助我们遍历数组。该方法返回一个新的数组迭代器对象，其中包含数组中每个索引的键/值对。例如，考虑以下代码片段：

```
const breakfast = ['apples', 'bananas', 'oranges'];
const eBreakfast = breakfast.entries();

console.log(eBreakfast.next().value); // [0, 'apples']
console.log(eBreakfast.next().value); // [1, 'bananas']
console.log(eBreakfast.next().value); // [2, 'oranges']
```

你也可以使用`for-of`循环来遍历从`breakfast.entries()`调用返回的迭代器：

```
for (let entry of eBreakfast) {
    console.log(entry);
}

// [0, 'apples']
// [1, 'bananas']
// [2, 'oranges']
```

类似地，还有两个数组方法可以分别访问键和值。让我们来看看它们。

#### Array.prototype.keys()

此方法返回一个新的数组迭代器，其中包含数组中每个索引的键：

```
const breakfast = ['apples', 'bananas', 'oranges'];
const kBreakfast = breakfast.keys();

console.log(kBreakfast.next().value); // 0
console.log(kBreakfast.next().value); // 1
console.log(kBreakfast.next().value); // 2
```

#### Array.prototype.values()

此方法返回一个新的数组迭代器对象，其中包含数组中每个索引的值：

```
const breakfast = ['apples', 'bananas', 'oranges'];
const vBreakfast = breakfast.values();

console.log(vBreakfast.next().value); // apples
console.log(vBreakfast.next().value); // bananas
console.log(vBreakfast.next().value); // oranges
```

**第7章 — 数组与集合**

#### Array.prototype.find()

`find()`方法让你遍历数组，并返回第一个匹配数组的回调函数`(element, index, array)`的元素。此方法还允许你可选地传递一个`this`的上下文绑定。换句话说，`find()`方法返回数组中第一个使测试函数返回`true`的值；否则返回`undefined`。`find()`方法的语法如下：

```
arr.find(callback[, thisArg])
```

其中`callback`是对每个值执行的测试函数，接受三个参数：

`element`，`index`和`array`。

```
function callback(element, index, array) {
// 根据某些条件返回 true 或 false
}
```

考虑以下代码片段：

```
const inventory = [
    {name: 'apples', quantity: 2},
    {name: 'bananas', quantity: 0},
    {name: 'oranges', quantity: 5}
];
```

```
let result = inventory.find((fruit) => fruit.name === 'apples');
console.log(result);              // {name: 'apples', quantity: 2}
```

上面的例子展示了我们如何轻松地找到数组中第一个`fruit.name`为`'apples'`的元素。你也可以使用`find()`方法获取某个索引位置的元素，例如：

```
result = inventory.find((fruit, i) => i > 2);
console.log(result);              // {name: 'oranges', quantity: 5}
```

如前所述，如果元素在数组中未找到，`find()`方法将返回`undefined`：

```
result = inventory.find((fruit, i) => i > 10);
console.log(result);              // undefined
```

下一个参数`thisArg`允许你可选地传递一个`this`的上下文绑定；例如，考虑以下代码片段：

```
function eligibleToVote(age) {
    return age >= this.legalAge;
}
```

```
function foo() {
    this.legalAge = 18;
    const result = [10, 12, 23, 26, 32].find(eligibleToVote, this);
    console.log(result);
}

foo();     // 23
```

在这个例子中，`foo`的上下文作为第二个参数传递给`find()`方法，因此`eligibleToVote()`中的`this`指向`foo`的上下文，且`this.legalAge`为18。你可能认为这个方法类似于ES5中的`filter()`方法，但请注意`filter()`总是返回一个匹配项的数组（并会返回多个匹配项），而`find()`总是只返回一个元素（数组中第一个满足条件的元素）。

#### Array.prototype.findIndex()

此方法是`find()`的等效方法。它不是返回一个元素，而是返回索引位置。如果集合中没有任何元素匹配回调函数`(element, index, array)`的标准，返回值为-1。例如，考虑以下代码片段：

```
result = inventory.findIndex((fruit) => fruit.name === 'apples');

console.log(result);            // 0
result = inventory.findIndex((fruit) => fruit.name === 'grapes');

console.log(result);            // -1
```

此方法类似于ES5中的`indexOf()`方法，后者只是定位数组中的元素。使用`indexOf()`方法，你只能在数组内搜索一个元素；它不支持回调函数方法。而在`findIndex()`方法的情况下，我们能够应用一个条件，返回的索引位置上的元素必须满足该条件。

#### Array.prototype.fill()

这是一个非常简单的方法，允许我们用一个静态值填充数组的所有元素。它还接受可选的起始和结束索引值。考虑以下代码片段：

```
[1, 2, 3].fill(4);          // [4, 4, 4]
[1, 2, 3].fill(4, 1);       // [1, 4, 4]
[1, 2, 3].fill(4, 1, 2);    // [1, 4, 3]
```

输入值可以是任意的，不一定是数字、字符或任何其他基本类型。它可以是一个对象，例如：

```
new Array(4).fill({}); // [{}, {}, {}]
```

#### Array.prototype.copyWithin()

`copyWithin()`方法将数组内的一个元素序列复制到从目标位置开始的数组位置。应复制的元素取自`(start, end)`范围。`start`参数是可选的，默认为0。同样，`end`参数也是可选的，默认为数组的长度。

`copyWithin()`方法的语法如下：

```
Array.prototype.copyWithin(target, start = 0, end = this.length)
```

让我们从一个简单的例子开始。考虑以下代码片段：

```
let fruits = ["apples", "bananas", "oranges", "grapes", "guava",
"watermelon"];
fruits.copyWithin(4);
console.log(fruits);
// ["apples", "bananas", "oranges", "grapes", "apples", "bananas"]
```

`fruits.copyWithin(4)`将目标索引设为4，即`"guava"`。它进一步确定要复制的元素将从起始位置0（默认）到结束位置6（数组长度）获取。你显然可以根据需要指定起始和结束值：

```
fruits = ["apples", "bananas", "oranges", "grapes", "guava", "watermelon"];
fruits.copyWithin(4, 1, 3);
console.log(fruits);
// ["apples", "bananas", "oranges", "grapes", "bananas", "oranges"]
```

`copyWithin()`方法也接受负的起始索引、负的结束索引和负的目标索引。让我们看一个使用它们的例子：

```
[1, 2, 3, 4, 5].copyWithin(-3, -4, -1); // [1, 2, 2, 3, 4]
```

在这个例子中，-3作为目标索引，将起始位置确定为数组末尾的第三个元素（在输入数组中是3）。它进一步将起始值和结束值分别确定为2和5（从数组末尾数的第四个和第一个元素）。

### 类型化数组

ES6中的类型化数组提供了一种高效访问和操作二进制数据的方式。在ES6之前，JavaScript在处理二进制数据方面表现并不出色。类型化数组有助于在处理二进制数据时提高性能。

使用类型化数组，JavaScript引擎无需推断数组的类型。如果你在JavaScript中创建一个普通数组，并且只存储浮点数，你的JavaScript引擎可能会乐观地决定它是一个浮点数数组，并为此优化代码。那么性能可能与类型化数组相当。但是，让我们考虑这样一种情况：你有一个浮点数数组，而在代码中的某个时刻，你在一个元素中存储了一个对象。在这种情况下，你的JavaScript引擎必须取消优化并重新生成使数组再次成为通用类型的代码。因此，使用类型化数组，事情简单得多，因为它们保证是一种类型，你不能将对象等其他东西存储在其中。它们简单得多这一事实意味着不太复杂的JavaScript引擎可以轻松实现它们，并且你可以获得一致的性能。

类型化数组的架构由一个缓冲区和一个视图组成。缓冲区是表示一块数据的对象。我们不能直接操作缓冲区的内容。为了访问缓冲区中包含的内存，我们需要使用视图。视图使我们能够读取和写入缓冲区的数据内容。

因此，类型化数组有两个独立的类：`ArrayBuffer`和`DataView`。`ArrayBuffer`包含我们的数据，而`DataView`提供对这些数据的自定义视图，它以特定格式表示缓冲区，并支持数据访问和操作。

### 使用类型化数组的基础

查看以下代码片段；这里我们创建一个`ArrayBuffer`，然后创建一个特定的`DataView`来处理该缓冲区中的数据：

```
const buffer = new ArrayBuffer(16);
const int32View = new const buffer = new ArrayBuffer(16);
const int32View = new Int32Array(buffer);

for (let i = 0; i < int32View.length; i++) {
    int32View[i] = i * 2;
}

console.log(int32View); // [0, 2, 4, 6]
```

类型化数组视图提供了所有常用数字类型的视图，如`Int8`、`Uint32`、`Float64`等。你可以在表7-1中查看所有类型及其相应的大小和描述。



 CHAPTER 7 ■ 数组与集合

### 表 7-1. 类型化数组视图

| 类型 | 字节大小 | 描述 |
| :--- | :--- | :--- |
| Int8Array | 1 | 8 位有符号整数 |
| Uint8Array | 1 | 8 位无符号整数 |
| Uint8ClampedArray | 1 | 8 位无符号整数（钳位） |
| Int16Array | 2 | 16 位有符号整数 |
| Uint16Array | 2 | 16 位无符号整数 |
| Int32Array | 4 | 32 位有符号整数 |
| Uint32Array | 4 | 32 位无符号整数 |
| Float32Array | 4 | 32 位浮点数 |
| Float64Array | 8 | 64 位浮点数 |

请注意，对于钳位数组，所有超出范围的值都会被设置为最接近该范围的元素，即第一个或最后一个元素。`Uint8ClampedArray` 类型化数组表示一个钳位到 0-255 的 8 位无符号整数数组，这意味着如果你指定的值超出了 [0,255] 的范围，将会设置 0 或 255。如果你指定了非整数，将会设置最接近的整数。

### 类型化数组与普通数组

类型化数组和普通数组在某些方面相似：它们都有 `length` 属性，而且在两种情况下，都可以使用 `[ ]` 运算符访问数组中的元素。类型化数组也支持所有标准数组方法。但它们在各种方面也存在差异。

JavaScript 中的类型化数组与其他编程语言（如 C、C++）中的数组类似，其中数组的所有元素都是同一类型，不像 JavaScript 中的数组那样元素可以是任意类型。类型化数组对所有元素都有严格的类型。

类型化数组不能有空元素。它们总是以 0 值初始化，不像普通数组那样值可以为空（undefined）。查看以下代码片段：

```
const buffer = new ArrayBuffer(16);
const float32View = new Float32Array(buffer);
let arr = new Array(10);

console.log(float32View); // Float32Array [0, 0, 0, 0]
console.log(arr); // [ , , , , , , , , , ]
```

各种浏览器 API 都支持类型化数组：文件 API、XMLHttpRequest、Fetch API、Canvas、WebSockets、WebGL、Web Audio API、媒体元素等。目前，某些类型化数组功能可能并非所有浏览器和 JavaScript 引擎都支持，因此你可以在 [https://kangax.github.io/compat-table/es6/#typed_arrays](https://kangax.github.io/compat-table/es6/#typed_arrays) 查看所需 JavaScript 引擎的可用性。

### Map 和 WeakMap

ES6 引入了一组称为 Map 和 WeakMap 的新数据结构，它们本质上是哈希表或 Python、C# 中的字典。ES6 的 Map 提供了一个简单的 API 来通过任意键存储对象，这是许多 JavaScript 程序中非常需要的基本功能。我们将在本节中详细介绍它们。

#### Map

实际上，我们在 JavaScript 中一直使用 map。事实上，每个对象都可以被视为一个 Map。对象由键（始终是字符串）和值组成，而在 Map 中，任何值（对象和原始值）都可以用作键或值。

在 Map 中，键可以是任何类型：字符串、布尔值、数字、对象或函数。看看这段代码：

```
let myMap = new Map();

const keyString = "a string",
      keyObj = {},
      keyFunc = () => {};
```

// 设置值

```
myMap.set(keyString, "value associated with 'a string'");
myMap.set(keyObj, "value associated with keyObj");
myMap.set(keyFunc, "value associated with keyFunc");
```

请注意，`set()` 方法是可链式调用的，所以你也可以这样做：

```
myMap.set(keyString, "value associated with 'a string'")
     .set(keyObj, "value associated with keyObj")
     .set(keyFunc, "value associated with keyFunc");

myMap.size; // 3
```

// 获取值

```
myMap.get(keyString);   // "value associated with 'a string'"
myMap.get(keyObj);      // "value associated with keyObj"
myMap.get(keyFunc);     // "value associated with keyFunc"
```

##### 检查键的相等性

Map() 中的键相等性基于"same-value"算法，它类似于 `===` 运算符，但也认为 NaN 等于 NaN（尽管通常 NaN !== NaN），这意味着当 NaN 用作键时，将返回先前使用 NaN 作为键设置的 map 对象。例如，考虑以下代码片段：

```
let myMap = new Map();
myMap.set(NaN, "not a number");
myMap.get(NaN); // "not a number"
```

请注意，你也可以通过键/值对的可迭代对象来创建 map：

```
let myMap = new Map([
[ 1, 'apple' ],
[ 2, 'banana' ],
[ 3, 'orange' ]
]);
```

此外，可以使用 `for...of` 或 `forEach()` 对 map 进行迭代：

```
for (let [key, value] of myMap) {
console.log(key + " = " + value);
}

// 1 = apple
// 2 = banana
// 3 = orange
```

Map 还支持 `keys()`、`values()` 和 `entries()` 方法：

```
for (let key of myMap.keys()) {
console.log(key);
}
// 1
// 2
// 3

for (let value of myMap.values()) {
console.log(value);
}
// apple
// banana
// orange
```

```
for (let [key, value] of myMap.entries()) {
    console.log(key + " = " + value);
}
// 1 = apple
// 2 = banana
// 3 = orange
```

如果你是经验丰富的 JS 开发人员，你知道对象是作为数据结构创建无序键/值对的主要机制。然而，使用对象作为 map 并不能让我们使用非字符串值作为键。

此时，你一定在想，何时该使用 map 而非对象，何时不该。当你需要键/值集合时，应该始终使用 Map，因为对象本质上并非设计为用作集合，结果是没有高效的方法来确定对象有多少属性。当你遍历对象的属性时，你还会得到其原型属性。当然，有一些解决方法，但当你遍历对象的属性时，属性不一定会按照插入的顺序被检索。这就是为什么建议在 JavaScript 程序中需要键/值集合时使用 map。

另一个很好的指标是，当你事先不知道集合的键时，也就是说，它们正从数据库读取或由用户输入，这意味着它们不一定是字符串或数字。相反，当你知道对象有哪些以及多少属性时，应该在编写代码时使用对象，也就是说，当它们的形状是静态的。

#### WeakMap

WeakMap 与普通 Map 类似，尽管方法较少，并且在垃圾回收方面有一些差异。WeakMap 是一种键被弱引用的 Map，这意味着如果所有对键的引用都丢失了，并且没有对值的更多引用，WeakMap 不会阻止其键被垃圾回收。因此，你不必担心 WeakMap 中的内存泄漏。通常，当存储与某物（如 DOM 节点）相关的元数据时，你希望有这种行为，这样当 DOM 元素不再受关注时，它们应该从内存中释放。

WeakMap 最大的限制是它**不可**迭代，与 Map 相反——这意味着它不支持 `entries()`、`keys()`、`values()`、`forEach()` 和 `clear()` 方法。另一点需要注意的是，在 WeakMap 中，每个键**必须**是对象。

尽管它几乎具有与 Map 相同的 API，但我们无法迭代 WeakMap 集合。我们甚至无法确定集合的长度，因为这里我们没有 `size` 属性。WeakMap 只有四个方法：

- delete(key)
- has(key)
- get(key)
- set(key, value)

```
let wMap = new WeakMap();

wMap.set('a', 'b');
// Uncaught TypeError: Invalid value used as weak map key

const o1 = {},
      o2 = () => {},
      o3 = window;

wMap.set(o1, 42);
wMap.set(o2, "hello");
wMap.set(o3, undefined);

wMap.get(o3); // undefined, because that is the set value
wMap.has(o1); // true
wMap.delete(o1);
wMap.has(o1); // false
```

### Set 和 WeakSet

Set 和 WeakSet 是 ES6 中引入的另一种集合类型。如果你来自 Python 等编程语言，你会知道 set 有多么有用。让我们在本节中看看它们。

#### Set

Set 对象是**唯一值**的集合。重复值被忽略，因为集合必须包含所有唯一值。Set 速度快，值可以是原始类型或对象引用。查看以下代码片段以了解更多关于 set 及其方法的信息：

```
let mySet = new Set([1, 1, 2, 2, 3, 3]);

mySet.size; // 3

mySet.has(1); // true

mySet.add('strings');
mySet.delete('strings'); // true
mySet.has('strings'); // false

mySet.add({ a: 1, b:2 });

mySet.size; // 4
mySet.clear(); // 清除 set
mySet.size; // 0
```

请注意，与 Map 类似，在 Set 中 NaN 也等于 NaN。你可以使用 `forEach` 方法或 `for...of` 循环，按插入顺序遍历一个 Set：

```javascript
mySet = new Set([1, 1, 2, 2, 3, 3, { a: 1, b: 2 }]);

mySet.forEach((item) => {
    console.log(item);
});

// 1
// 2
// 3
// Object { a: 1, b: 2 }

for (let value of mySet) {
    console.log(value);
}

// 1
// 2
// 3
// Object { a: 1, b: 2 }
```

如果你需要一个动态的唯一元素列表用于下拉菜单或输入框的自动建议，Set 会非常有帮助。使用 Set 可以确保你的建议列表中不会有重复值，省去了检查重复项的麻烦。

#### WeakSet

与 WeakMap 类似，WeakSet 对象允许你将弱持有的对象存储在一个集合中，这意味着 WeakSet 不会阻止其元素被垃圾回收。WeakSet 中的对象只能出现一次；它在 WeakSet 的集合中是唯一的。WeakSet 中的值必须是唯一的对象引用。如果没有任何其他对象引用 WeakSet 中的某个对象，该对象就会被垃圾回收。与 WeakMap 类似，WeakSet 不是可迭代的，也没有 `size` 属性。WeakSet 只支持三种方法：

-   `add(value)`
-   `has(value)`
-   `delete(value)`

```javascript
let ws = new WeakSet();
const obj = {};
const foo = {};
ws.add(window);
ws.add(obj);

ws.has(window); // true
ws.has(foo);    // false, foo has not been added to the set

ws.delete(window); // removes window from the set
ws.has(window);    // false, window has been removed
```

当你在集合中需要垃圾回收能力时，应该使用 WeakSet 而不是 Set。另一个典型的用例是标记一个对象是否满足某些条件。考虑以下示例：

```javascript
const fruits = new WeakSet();

class Fruit {
  constructor() {
    fruits.add(this);
  }

  getName() {
    if (!fruits.has(this)) {
      throw new TypeError("getName() called on an incompatible object!");
    } else {
      // returns the name
    }
  }
}
```

这是一个很好的方法，可以防止在类构造函数创建的任何对象之外使用该类的方法。

### 总结

在本章中，我们学习了 ES6 引入的用于处理和操作数组与集合的新且高效的方法。这些新特性为在 ES6 之前处理起来很繁琐的常见用例提供了内置解决方案。通过新的数组方法，你可以在 JavaScript 程序中轻松地创建和管理数组。我们还学习了 ES6 引入的新的数组原型方法，这些方法帮助我们高效地遍历和访问数组中存储的元素。我们还讨论了类型化数组如何帮助你在 JavaScript 中处理二进制数据时提升性能。在本章的后半部分，我们学习了 ES6 引入的新集合类型：Map、WeakMap、Set 和 WeakSet，以及它们强大的功能集和有效的用例。

至此，你应该对在 JavaScript 应用程序中使用这些新的数据类型充满信心。在下一章中，我们将深入探讨之前简要提到的迭代器和可迭代对象，并学习 ES6 引入的生成器概念。

# 第 8 章 ■ 迭代器和生成器

在本章中，我们将全面学习新引入的迭代器和生成器，它们为 JavaScript 的遍历机制带来了简洁性和可定制性。许多编程语言已经摒弃了那些在遍历集合元素时需要额外努力来跟踪当前索引位置的、乏味的旧式 for 循环。让我们来看看如何使用迭代器和生成器来在应用程序中高效地处理数据。

### 可迭代对象和迭代器

在 ECMAScript 标准的最新版本中，投入了大量精力来改进我们组织代码的方式。ES6 引入了一套全新的遍历机制，使得实现一个可迭代对象和一个迭代器变得非常简单。这个版本的 JavaScript 引入了一组称为迭代器协议和可迭代协议的协议，任何 JavaScript 对象要想成为迭代器或可迭代对象，都必须实现这些协议。在继续讨论这些协议之前，让我们先了解一下 JavaScript 中的可迭代对象和迭代器：

简而言之，迭代器模式是一种结构化的模式，用于按特定顺序从元素集合中逐个获取信息。它是一个具有特定迭代接口的对象。这种模式一直存在，并通过自定义对象在 JavaScript 中使用，但随着 ES6 的到来，我们看到了迭代器模式的隐式标准化。现在，JavaScript 中许多现有的数据结构都暴露了一个迭代器，你也可以使用相同的标准构建自己的迭代器，这为你提供了最大的互操作性。

**可迭代对象**是对一系列可以被迭代的元素的简单表示。它没有任何迭代状态，比如“当前元素”。相反，它有一个生成迭代器的方法。

**迭代器**是具有迭代状态的对象。所有迭代器对象都有一个 `next()` 方法，用于返回集合中的下一个对象。`next()` 方法返回的对象有两个属性：
(i) `value`，即集合中的下一个值；以及
(ii) `done`，一个布尔值，表示序列是否已结束，只要序列中还有要返回的值，它就是 `false`，只有当集合中的值用尽时，它才返回 `true`。

每次调用 `next()` 方法都会产生集合中的下一个值。一旦集合中的所有值都被遍历完毕，调用 `next()` 方法将返回 `value` 为 `undefined`，`done` 为 `true`。

说了这么多，让我们看看如何在 ES6 中手动实现一个迭代器：

```javascript
function myIterator(data) {
    let currentIndex = 0;
    return {
        next: () => {
            const done = (currentIndex >= data.length);
            const value = !done ? data[currentIndex] : undefined;
            currentIndex += 1;

            return {
                done,
                value
            };
        }
    };
}

const itrObj = myIterator([41, 42, 43]);
itrObj.next();  // { value: 41, done: false }
itrObj.next();  // { value: 42, done: false }
itrObj.next();  // { value: 43, done: false }
itrObj.next();  // { value: undefined, done: true }

// for all further calls
console.log(itrObj.next());     // { value: undefined, done: true }
```

在上面的代码片段中，`myIterator()` 函数返回一个具有 `next()` 方法的对象，每次调用该方法都会返回集合中的下一个值。在最后一个元素之后，返回对象的 `done` 值变为 `true`，而返回的 `value` 总是 `undefined`。

ES6 通过引入 `[Symbol.iterator]` 简化了实现迭代器的过程，它指定了对象的默认迭代器。这个键持有 `@@iterator` 方法，这是本章后面将讨论的可迭代协议的基础。每当一个对象需要被迭代时，例如在 `for..of` 循环开始时，会无参数地调用其 `@@iterator` 方法。这个方法返回对象的默认迭代器。在 ES6 中，`@@` 描述一个众所周知的符号。这里，`@@iterator` 指定了存储在对象键 `[Symbol.iterator]` 中的迭代器函数。因此，对于上面的例子，`@@iterator` 方法将返回 `next()` 函数：

```javascript
myIterator[Symbol.iterator] = function () {
  return {
    next: function () {}
  }
}
```

使用符号作为键来存储迭代器方法，可以确保它永远不会与常规对象键冲突。现在让我们看看在 ES6 中使用 `Symbol.iterator` 的同一个例子：

```javascript
const arr = [41, 42, 43];
const itrObj = arr[Symbol.iterator]();
itrObj.next(); // { value: 41, done: false }
itrObj.next(); // { value: 42, done: false }
itrObj.next(); // { value: 43, done: false }
itrObj.next(); // { value: undefined, done: true }
```

当为给定的数组 `arr` 调用 `Symbol.iterator` 处的 `@@iterator` 方法时，它将创建一个新的迭代器。请注意，每次调用时都会创建一个新的迭代器。作为可迭代对象的内置 ES6 数据结构都具有这种行为，允许使用 `next()` 方法遍历其值。

让我们以原始字符串值为例：

```javascript
const message = "Ian is an awesome student";
const itrObj = message[Symbol.iterator]();

itrObj.next();    // { value: "I", done: false }
itrObj.next();    // { value: "a", done: false }
// ...
```

在上面的例子中，我们能够使用 `next()` 方法遍历字符串 `message` 的每个字符。ES6 还允许我们迭代新的数据结构，比如 Map 和 Set 集合。让我们以 Map 为例：

```javascript
const permissionMap = new Map();

permissionMap.set("admin", {read: true, write: true, del: true});
permissionMap.set("student", {read: true, write: false, del: false});
permissionMap.set("faculty", {read: true, write: true, del: false});
permissionMap.set("staff", {read: true, write: false, del: true});

const permissions = permissionMap[Symbol.iterator]();

console.log(permissions.next());
// {value: ['admin', { read: true, write: true, del: true }], done: false}

console.log(permissions.next());
// {value: ['student', { read: true, write: false, del: false }], done: false}

console.log(permissions.next());
// {value: ['faculty', { read: true, write: true, del: false }], done: false}
```



 ```
console.log(permissions.next());
// {value: ['staff', { read: true, write: false, del: true }], done: false}

console.log(permissions.next());
// {value: undefined, done: true}
```

在上面的示例中，我们为不同用户类型的权限创建了一个以用户类型为键的映射。我们可以通过调用 @@iterator 方法创建一个新的迭代器，并使用 next() 遍历这些值。这里需要注意的一点是，这些集合还提供了生成迭代器的 API 方法，例如，你可以使用 entries() 方法获取映射的迭代器：

```
const permissionEntries = permissionMap.entries();

console.log(permissionEntries.next());
// {value: ['admin', { read: true, write: true, del: true }], done: false}

console.log(permissionEntries.next());
// {value: ['student', { read: true, write: false, del: false }], done: false}
```

### 迭代协议

现在我们已经对迭代器和可迭代对象有了基本的了解，让我们来谈谈本章开头简要讨论过的那些协议。有两种迭代协议：**可迭代协议（iterable protocol）** 和 **迭代器协议（iterator protocol）**。任何对象都可以通过遵守一些约定来实现这些协议。

### 可迭代协议

可迭代协议允许你自定义 JavaScript 对象的迭代行为。该协议规定，所有可迭代对象都必须使用 `[Symbol.iterator]` 属性实现 @@iterator 方法。当需要迭代某个对象时，就会调用此方法。它不接受任何参数，并返回默认的迭代器，该迭代器可用于从可迭代对象中获取值。内置的可迭代对象，如 Array、Map、Set 等，都有一个默认的 @@iterator 方法，这使我们能够遍历相应的集合。

### 迭代器协议

迭代器协议定义了一种从可迭代对象中获取值序列的标准方式。该协议规定，迭代器对象必须定义一个 `next()` 方法，该方法不接受任何参数，并返回一个具有两个属性 `done` 和 `value` 的对象。

### 作为可迭代对象的迭代器

如果一个迭代器同时也是可迭代的，那么它可以直接与 `for…of` 循环一起使用。你可以通过为迭代器提供 `Symbol.iterator` 来使其成为可迭代对象，该属性返回迭代器本身。看看下面的代码片段，我们将迭代器转换为可迭代对象，然后使用 `for…of` 循环进行遍历：

```
const infiniteSequenceGenerator = {
        currentNumber: 0,

        // 将 "infiniteSequenceGenerator" 迭代器变为可迭代对象
        [Symbol.iterator]() {
            return this;
        },

        next() {
            return {
                value: this.currentNumber++,
                done: false
            }
        }
};

const iter = infiniteSequenceGenerator[Symbol.iterator]();

console.log(iter === infiniteSequenceGenerator);   // true

console.log(iter.next().value);   // 0
console.log(iter.next().value);   // 1
console.log(iter.next().value);   // 2
console.log(iter.next().value);   // 3

for (let item of iter) {
    if (item > 20) break;
    console.log( item );
}

// 4
// 5
// 6
// 7
// ... 20
```

在上面的示例中，注意我们如何直接对可迭代对象使用 `for…of` 循环，但它在内部使用了 `next()` 方法，因为在循环之前我们手动使用 `next()` 方法调用了迭代器四次，所以我们从 `for…of` 循环中得到的数字列表是从 4 开始的。

### 迭代器中的 return() 和 throw()

迭代器还有两个额外的可选方法：`return(...)` 和 `throw(...)`，大多数内置迭代器都没有实现这两个方法，但它们在生成器（generators）的上下文中 definitely 具有重要意义，我们将在本章后面进行探讨。

在某些情况下，你可能希望最后一项 `{done: true, value: undefined}` 的 `value` 不是 `undefined`。这时就需要用到 `return()`。`return(...)` 方法用于向迭代器发送信号，表示使用迭代器的代码将不再从迭代器请求更多值。它可以在迭代器已经消耗完所有值或遇到异常终止时使用，允许其执行清理操作，如关闭数据库连接、保存或关闭文件。如果存在，`return(...)` 将在集合耗尽时自动调用，也可以手动调用。`return(...)` 方法接受一个可选参数，通常作为返回对象中的 `value` 发送回去。

另一方面，`throw(...)` 用于向迭代器发送可能发生异常或错误的信号。迭代器对 `throw(...)` 的处理方式可能与 `return(...)` 方法的信号不同，因为它不像 `return(...)` 那样意味着完全停止。我们将在生成器部分更详细地研究这些方法。

### 生成器

简单来说，**生成器（Generators）** 是可以暂停的函数。在 ES6 之前，JavaScript 只有会运行到完成才会被中断执行的函数。随着 ES6 的推出，我们通过生成器引入了一种不同类型的函数，它们不总是像普通函数那样运行到完成，而是可以在执行过程中暂停和恢复。

生成器是一种允许我们创建特殊类型迭代器的函数，其执行可以被暂停和保留，同时保持上下文。如果一个函数包含一个或多个 `yield` 表达式，并且使用 `function*` 语法，那么它就是一个生成器：

```
function *gen() {
    yield 42;
}
```

在这种语法中，`*` 的位置并不是很重要。生成器可以用以下任何方式书写：

```
function *gen() { .. }
function* gen() { .. }
function * gen() { .. }
function*gen() { .. }
```

尽管如此，在代码中使用生成器时，最好保持风格的一致性。我们将在本书的其余部分使用第一种格式。

### 生成器函数

生成器函数通过在函数体中执行 `yield` 关键字来暂停，该关键字可以在函数体中使用任意多次。你可以从 `yield` 表达式返回一个值。查看下面的示例，我们从生成器中生成值 42：

```
yield 42;
(ui
```

生成器就像任何其他函数一样执行，你可以向其中传递参数。唯一的区别是，执行生成器并不会真正运行其中的代码。它只是产生一个可用于执行其中代码的迭代器。

```
function *gen() {
    yield "Hello";
    yield "from";
    yield "generator";
}
```

现在如果我们调用这个生成器函数，它不会被执行；相反，它会返回一个将用于执行其中代码的迭代器。

```
let obj = gen();
```

在上面的生成器中，开头的操作会先运行，然后 `yield` 语句会暂停生成器的执行，直到调用 `next()` 方法。方法 `obj.next()` 继续执行 `gen`，直到下一个 `yield` 表达式：

```
console.log(obj.next());   // { value: "Hello", done: false}
console.log(obj.next());   // { value: "from", done: false}
console.log(obj.next());   // { value: "generator", done: false}
console.log(obj.next());   // { value: undefined, done: true}
```

`yield` 可以在生成器内部使用任意多次。它也可以作为循环的一部分，表示重复的暂停位置。注意，`yield` 不仅仅是暂停点，它在暂停生成器时还会发送出一个值。

```
function *infiniteNumbers() {
    var n = 1;
    while (true) {
        yield n++;
    }
}
```

```
var numbers = infiniteNumbers(); // 返回一个可迭代对象

console.log(numbers.next()); // { value: 1, done: false }
console.log(numbers.next()); // { value: 2, done: false }
console.log(numbers.next()); // { value: 3, done: false }
```

每次调用 `yield` 时，生成的值就成为序列中的下一个值。没有提供值的 `yield` 语句只是意味着该值是 `undefined`。

### 与生成器通信

在上一节中，我们看到了生成器如何使用 `yield` 语句与我们的代码通信。我们还可以通过 `yield` 向生成器函数传递值，并在执行恢复时在生成器函数内部使用这些值。例如，看看下面的代码片段：

```
function *calculator() {
    const num1 = yield "I am a calculator";
    const num2 = yield "I add numbers";
    console.log(`Sum is: ${num1 + num2}`);
}

const myGenerator = calculator();

console.log(myGenerator.next());
// { value: 'I am a calculator', done: false }

console.log(myGenerator.next(2));
// { value: 'I add numbers', done: false }

console.log(myGenerator.next(3));
// Sum is: 5
// { value: undefined, done: true }
```

在上面的示例中，第一次调用 `next()` 时，生成器生成字符串 "I am a calculator" 并暂停。第二次 `next(2)` 的值将被赋给 `num1`，因为在生成器内部，我们指定了在 `yield "I am a calculator"` 处生成的任何值都会被赋给 `num1`，`num2` 同理。因此，第三次调用 `next()` 时，`Sum is: 5` 被打印到控制台，并且由于没有更多的 `yield` 语句，`undefined` 被作为值返回。

生成器的这种与代码良好通信的行为在异步编程的情况下真的很有帮助。生成器可以使你的异步代码看起来是同步的。再看另一个示例，演示生成器和异步代码如何很好地协同工作：



 # 第8章 迭代器与生成器

```
function getFlightDurations() {
    setTimeout(() => {
        flightIterator.next({
            Qatar: "39h 0m",
            Emirates: "40h 20m"
        });
    }, 1200);
}

function getFlightPrices() {
    setTimeout(function(){
        flightIterator.next({
            Qatar: "$2010",
            Emirates: "$1904"
        })
    }, 1000);
}

function *getFlights() {
    const allFlights = ["Qatar", "Emirates"];
    const flightDurations = yield getFlightDurations();
    const flightPrices = yield getFlightPrices();

    for (let flight of allFlights) {
        console.log(`New York to Auckland takes
${flightDurations[flight]} in ${flight} airlines for around
${flightPrices[flight]}`);
    }
}

const flightIterator = getFlights();

flightIterator.next();
// New York to Auckland takes 39h 0m in Qatar airlines for around $2010
// New York to Auckland takes 40h 20m in Emirates airlines for around $1904
```

在上面的示例中，`getFlights()` 是一个生成器函数，它返回一个迭代器。调用返回迭代器的 `next()` 方法时，生成器执行到第一个 `yield` 语句处，此时 `getFlightDurations()` 被调用。`getFlightDurations()` 是一个异步函数，它使用 `setTimeout` 将执行延迟 1.2 秒，然后在迭代器上调用 `next()` 方法，从而确保 `flightDurations` 能被正确赋值。`flightPrices` 的处理方式相同，一旦再次在 `getFlightPrices()` 中调用 `next()` 方法，输出就会被记录到控制台。如果我们在这里没有使用 `yield`，`flightDurations` 和 `flightPrices` 只会被赋值为 `undefined`，因为函数本身在赋值时就会返回 `undefined`。使用 `yield` 语句可以阻止值被赋值，直到 `setTimeout` 函数执行完毕。这就是生成器如何帮助我们在使用异步操作时编写阻塞式代码，使代码看起来更像是同步的。

### 提前完成

在本章早些时候，我们讨论了迭代器有两个可选方法：`return(...)` 和 `throw(...)`，这些方法在生成器的上下文中具有重要意义。这些方法可以在生成器暂停状态时立即结束序列。请看下面的代码片段，例如：

```
function *getFruits() {
	yield "apple";
	yield "orange";
	yield "banana";
}

const fruitIterator = getFruits();

console.log(fruitIterator.next());			// {value: 'apple', done: false}

console.log(fruitIterator.return("kiwi"));	// {value: 'kiwi', done: true}

console.log(fruitIterator.next());			// {value: undefined, done: true}
```

在上面的示例中，`return("kiwi")` 返回作为参数传入的相同值 `"kiwi"` 并结束序列，导致 `done` 为 `true`。这等同于在生成器函数中使用一个返回值，尽管你都应该记住，遍历从生成器获得的序列时，不包括表示 `{ done: true }` 的那个值。请看下面的代码片段，例如，我们在 `fruitIterator` 集合上进行迭代，其中只包含在源生成器中调用 `return()` 方法之前所 `yield` 出的元素：

```
function *getFruits() {
	yield "apple";
	yield "orange";
	yield "banana";
	return "kiwi";
	yield "watermelon";
}

const fruitIterator = getFruits();

for (let fruit of fruitIterator) {
	console.log(fruit);
}

// apple
// orange
// banana
```

你还可以通过将代码包装在 `try-finally` 块中来避免立即终止序列，确保 `finally` 子句中的代码在序列完成时执行，无论是提前终止还是 `yield` 语句全部执行完毕。这有助于在序列结束后执行任何清理或关闭操作。请看下面的代码片段，例如：

```
function *getFruits() {
    try {
      yield "apple";
      yield "orange";
      yield "banana";
    }

    finally {
      console.log("You must always eat a big watermelon");
      yield "watermelon";
    }
}
```

```
const fruitIterator = getFruits();

console.log(fruitIterator.next());
// { value: 'apple', done: false }

console.log(fruitIterator.return("kiwi"));
// You must always eat a big watermelon
// { value: 'watermelon', done: false }

console.log(fruitIterator.next());
// { value: 'kiwi', done: true }

console.log(fruitIterator.next());
// { value: undefined, done: true }
```

在上面的示例中，一旦 `finally` 块中的表达式执行完毕，序列将以值为 `'kiwi'`、`done` 为 `true` 的状态终止，其中 `'kiwi'` 是通过 `return(...)` 方法的参数传入的。

同样，`throw(...)` 也会停止生成器的执行，但永远不会自动调用。这个方法在某些情况下可能很有用，例如当你想告知用户一些意外错误时，可以利用 `try-catch` 块来实现生成器中的错误处理。请看下面的代码片段，例如：

```
function *getFruits() {
    yield "apple";
    yield "orange";
    yield "spinach";
    yield "watermelon"
}
```

```
const fruitIterator = getFruits();

for (let fruit of fruitIterator) {
    try {
        console.log(fruit);
        if (fruit === "spinach") {
            fruitIterator.throw("Vegetable Found");
        }
    } catch (err) {
        console.log(`Exception: ${err}`);
    }
}

// apple
// orange
// spinach
// Exception: Vegetable Found
```

注意 "watermelon" 从未从生成器中 `yield` 出来，因为当 "spinach" 被返回时调用了 `throw(...)`，导致序列执行停止。

### 小结

ES6 中引入的迭代器和生成器为我们提供了对集合中存储的值的顺序访问，还允许我们自定义遍历这些值的方式。ES6 还引入了一组新的协议来定义迭代器和可迭代对象，即**迭代协议**。在本章中，我们学习了如何使用独特的 `[Symbol.iterator]` 属性为对象定义默认迭代器。当对象上提供了 `Symbol.iterator` 时，该对象被视为可迭代的。

在本章的后半部分，我们还学习了生成器函数，它们由星号（*）和函数体中的一个或多个 `yield` 语句来表示。它们是一种特殊类型的函数，可以在执行过程中暂停和恢复。

108

# 第9章

## ES6 中的 Promise

众所周知，JavaScript 在设计上就是单线程的。在浏览器中，它使用事件处理来同时管理许多任务。JavaScript 引擎管理一个事件队列，当事件发生时，会调用已注册的处理器函数。如果你有任何使用传统 JavaScript 的经验，那么你一定很清楚，理解异步编程是正确使用 JavaScript 的必要条件。使用异步的主要模式是通过回调函数。ES6 为标准 JavaScript 规范带来了一个新特性——*Promise*（某些最新 JS 库和框架中已有的特性），它解决了回调——这种异步唯一方案——中的许多重大问题。

### Promise 概述

在需要等待异步操作完成后再执行某项任务的情况下，JavaScript 严重依赖回调函数，以允许代码执行继续经过长时间运行的任务。你一定已经知道 `setTimeout`、`XMLHttpRequest` 以及所有基于浏览器的异步函数都是基于回调的。虽然这个概念在理论上简单易懂，但它可能导致一些非常令人困惑和难以跟踪的代码，尤其是在需要进行回调套回调（嵌套回调）的情况下，这通常被称为"回调地狱"。例如，考虑下面的代码片段，其中 X 必须在 Y 之前发生，Y 又必须在 Z 之前发生：

```
x = getData();
y = getMoreData(x);
z = getMoreData(y);
```

在 ES6 之前，你可以使用回调函数异步获取 x，然后将其作为参数传递给获取 y 的函数，z 也是如此，方式如下：

```
getData(function(x){
    getMoreData(x, function(y){
        getMoreData(y, function(z){
            ...
        });
    });
});
```



# 第9章 ES6中的Promise

在现实应用中，当存在大量回调函数时，这种情况会变得越来越复杂，可能导致回调金字塔的出现。这些回调金字塔无处不在——在处理HTTP请求、数据库操作、动画、进程间通信以及各种其他地方。通常，使用回调函数的代码可能变得更难以理解、重构和测试。

这就是Promise的用武之地。Promise为我们提供了一种以更可控模式处理异步操作的方式。它们代表一个可在将来某个时刻处理的值，并提供了一种逃离回调地狱的途径。与基于回调的方法相比，Promise为执行、组合和管理异步操作提供了一种更简单的替代方案。它们还使得代码的逻辑流程更易于理解。

ES6原生支持Promise。Promise是一个等待异步操作完成的对象，当该操作完成时，Promise要么被兑现（fulfilled），要么被拒绝（rejected）。一个Promise对象可以是以下三种状态之一：

- **已兑现（fulfilled）** - 当Promise成功时
- **已拒绝（rejected）** - 当Promise失败时
- **待定（pending）** - 当它既未兑现也未被拒绝时

一个待定的Promise可能会转变为已兑现或已拒绝的状态，而当一个Promise被兑现或拒绝时，它就被认为是已定型的（settled）。重要的是要注意，一个已定型的Promise是不可变的，这意味着一旦Promise被定型，它就不能被重新定型。

### 创建Promise

Promise使用新的 `Promise()` 构造函数创建，该函数接受一个**执行器**（executor，一个函数）作为参数，该执行器有两个参数：

**执行器**启动一些异步操作，一旦完成，就调用resolve或reject函数来兑现Promise，或者如果发生错误则拒绝它。

一个简单的Promise如下所示：

- 第一个参数（通常命名为resolve）是一个函数，当未来值准备好时（即Promise被兑现时），会调用该函数并传入未来值；
- 第二个参数（通常命名为reject）是一个函数，当无法解析未来值时调用，用于拒绝Promise。

```
const p = new Promise((resolve, reject) => {
    if (/* some condition */) {
        resolve(/* some value */);  // 兑现成功
    } else {
        reject(/* some reason */);  // 出错，拒绝
    }
});
```

第二种方法（reject）是可选的，你完全可以只使用resolve方法来创建一个Promise，如下方代码片段所示，Promise分别被兑现和拒绝：

```
new Promise(resolve => resolve()) // Promise被兑现
new Promise((resolve, reject) => reject()) // Promise被拒绝
```

你也可以使用以下方式创建一个立即兑现的Promise：

```
const sayHello = Promise.resolve("hello!");
```

类似地，你也可以使用 `Promise.reject(value)` 来拒绝一个Promise。不带值地兑现或拒绝Promise用处不大。通常，Promise会兑现为一个值，该值可以是HTTP请求、动画或其他一些异步操作的结果。

一个Promise一旦创建，就只能被定型，这意味着它要么被兑现，要么被拒绝。并且如上所述，由于已定型的Promise是不可变的，已定型的值或失败原因无法更改（该值也可能是undefined）。但是，一个对象可以作为兑现值使用，而对象的属性可能会发生变更。

### 使用then()和catch()消费Promise

一旦创建了Promise，它就可以作为一个值被传递，本质上代表一个未来值的占位符。这个值可以在Promise被兑现时使用 `.then()` 方法来消费。该方法接受一个函数，一旦Promise被兑现，该函数将被传入解析后的值。考虑以下代码片段：

```
const p = new Promise((resolve, reject) => resolve(42));
p.then((val) => console.log(val)); // 42
```

每个Promise都必须有一个 `.then()` 方法，该方法实际上接受两个可能的参数。第一个参数是Promise被兑现时调用的函数，第二个参数是Promise被拒绝时调用的函数，如图9-1所示。

```
p.then((value) => { console.log("Promise已兑现:", value) },
      (error) => { console.log("Promise已拒绝: ", error) });
```

**图9-1。** *一个待定的Promise可以被兑现或拒绝，并使用 `.then()` 方法处理*

如果一个给定的Promise总是会被兑现，为了简洁，我们可以省略第二个参数。看看下面这个例子，顾客在下单五秒后收到他的披萨：

```
const pizza = new Promise((resolve) => {
    console.log("5秒后给你披萨...");
    setTimeout(() => {
        resolve("洋葱披萨");
    }, 5000);
});

pizza.then(
    (item) => { console.log(`收到订单: ${item}`) },
    (error) => { console.log("你的披萨出了点问题") }
);

// 5秒后给你披萨...
// 收到订单: 洋葱披萨
```

这个例子说明了两点：

- 首先，我们附加到Promise上的处理程序是在所有其他代码异步运行之后被调用的。
- 其次，兑现处理程序仅在Promise被兑现时调用，并传入其被解析时的值（在我们的例子中是洋葱披萨）。拒绝处理程序也是如此。

以下是另一个消费Promise的典型示例，其中 `getRentalList(location)` 是异步的，它使用一个返回Promise的Web服务返回给定地点的当前可用租赁房产列表：

```
const housingPromise = getRentalList("伦敦");
housingPromise.then(
    (res) => {
        if (res.properties && res.properties.length > 0) {
            console.log(`我们为你找到了房子: ${res.properties}`);
        } else {
            console.log(`抱歉，在${res.location}没有可用的住房`);
        }
    },
    (error) => {
        console.log(`出了点问题: ${error}`);
    }
);
```

如果你只对拒绝一个Promise感兴趣，可以省略第一个参数并将其作为null传递。例如，查看以下代码片段：

```
const networkReq = new Promise((resolve, reject) => {
    reject("未找到服务器");
});
networkReq.then(
    null,
    (error) => { console.log(error); }
);
```

一方面，如果一个处理程序在 `.then()` 调用中返回一个值，它在返回时会自动包装在一个Promise中。这些 `.then()` 调用可以链式调用。我们将在下一节详细讨论Promise链的工作原理。另一方面，你也可以使用 `catch()` 方法以更紧凑的方式处理**已拒绝**的Promise。例如，你可以将上面的示例重写如下：

```
networkReq.catch((error) => { console.log(error); });
```

`catch()` 方法在Promise组合中用于错误处理非常有用。与 `then()` 方法类似，它也返回一个Promise，但只处理拒绝的情况。`catch()` 方法的行为类似于 `then(null, onRejected)` 的缩写。我们将在本章后面了解更多关于错误处理的内容。

### Promise链

由于 `.then()` 和 `.catch()` 总是返回一个新的Promise，因此可以轻松地链接Promise，并对错误的处理方式和位置进行极其精细的控制。链接Promise允许将异步操作链接在一起，从而保证它们以正确和预期的顺序发生，使得代码看起来几乎是同步的。考虑以下示例：

```
const bond = new Promise((resolve, reject) => {
    resolve("Bond");
});

bond.then((str) => `${str}, James ${str}`)
    .then((str) => `Hello, I'm ${str}!`)
    .then((str) => console.log(str));

// Hello, I'm Bond, James Bond!
```

上面是一个简单的例子，展示了Promise链如何帮助顺序执行不同的任务并获得最终结果。让我们看看下面这个更实际的代码片段，它展示了Promise链如何在异步任务中发挥优势：

```
getPaymentFromUser
    .then(displayTransactionDetails)
    .then(queueTransactionEmail)
    .then(redirectToOrdersPage)
    .catch(logError)
```

这里，`getPaymentFromUser` 返回一个Promise，Promise链中的每个函数都会在前一个处理程序完成后，使用其返回值被调用。在这个例子中，`displayTransactionDetails()` 将等待 `getPaymentFromUser()` 完成后才开始，而 `queueTransactionEmail()` 将等待 `displayTransactionDetails()` 完成后才开始，以此类推。重要的是要注意，`logError()` 仅在任何一个先前的Promise被拒绝时才会运行。这种方式序列化了调用，而不会阻塞主执行线程，并保证这些操作的执行将以串行顺序发生。

### 错误处理

在本章前面，我们讨论了如何在使用以下任何一种方式消费Promise时处理错误：

```
somePromise().then(onResolved, onRejected);

// 或者简单地使用 catch()

somePromise()
    .then(onResolved)
    .catch(onRejected);
```

那么，应该优先选择哪种方式，原因是什么？这个问题的答案取决于一个具体场景：当你的 `onResolved()` 函数抛出错误时会发生什么。`then()` 方法返回的 promise 会被拒绝（rejected），但如果使用第一种方式，这种拒绝无法被捕获——导致错误在你的应用中被吞没。而使用第二种方式，无论是来自 `somePromise()` 还是 `onResolved()` 的错误，都可以在 `catch()` 方法中处理。如果我们有多个 `then()` 调用，错误会一直传递下去，直到遇到一个错误处理器。因此，建议在所有 promise 链的末尾都使用 `catch()` 方法。

### 结合使用 Promise 和 Promise.all

`Promise.all` 接收一个 promise 数组（或任何可迭代对象），并返回一个 promise，该 promise 在可迭代参数中的所有 promise 都已解决（resolved）时解决，或者在第一个被传递的 promise 失败（rejected）时，以其失败原因为由拒绝。

如果任何一个传入的 promise 被拒绝，那么所有的 promise 都会立即以该被拒绝的 promise 的值作为原因而被拒绝，无论其他 promise 是否已解决，都会被丢弃。请注意，如果传递的是一个空数组，则该方法会立即解决。

```
const p1 = Promise.resolve(3);
const p2 = 42;
const p3 = new Promise((resolve, reject) => {
    setTimeout(resolve, 100, "foo");
});

Promise.all([p1, p2, p3]).then(values => {
    console.log(values); // [3, 42, "foo"]
});
```

然而，在某些情况下，你可能不想等待数组中的所有 promise 都解决，而只是想获取数组中第一个 promise 履行（fulfill）的结果。在这种场景下，可以使用 `Promise.race()`。

`Promise.race()` 同样接收一个 promise 数组，但与 `Promise.all()` 不同的是，它会在数组中的第一个 promise 履行时，立即履行其返回的 promise。例如，考虑这样一种情况：我们想从一个 API 端点获取一些 JSON 数据，但我们不想永远等待响应。在这种情况下，我们只想使用一个默认值。我们可以使用 `Promise.race()` 来实现：

```
// 一个在给定时间 (t) 后超时的 Promise
function delay(t) {
    return new Promise((resolve, reject) => {
        setTimeout(resolve, t);
    });
}
```

```
// 哪个 Promise 先履行，其结果就会传递给我们的处理器
Promise.race([
      fetchData(),
      delay(5000).then(() => { data: "test" })
])
.then((res) => {
      // 如果 fetchData() 耗时超过 5 秒，这里将是 "test"
      console.log("data:", res.data);
})
.catch(function(err) {
      console.log("error:", err);
});
```

在这个例子中，`delay()` 函数返回一个新的 promise，它在 t 毫秒后解决。然后我们将一个处理器附加到这个返回的 promise 上，以返回我们的默认用户对象 `{user: "guest"}`，这确保了如果我们能在 5 秒内从服务器获取到用户数据，我们将得到用户详情；否则将使用一个访客用户。

### 总结

Promise 已成为处理大量异步操作的标准方法。在本章中，我们学习了 promise 在正确使用时如何产生易于阅读的代码，这使得它们比传统的回调函数更容易调试。它们允许我们组合异步 API，并让我们能够用真正的 promise 包装不符合规范的 promise API 或回调 API。与回调函数和事件不同，promise 帮助我们避免竞态条件，并确保其所代表值的不可变性。promise 让我们能够以同步的方式编写异步代码，具有扁平的缩进和单一的异常通道。

## 元编程

“元”（meta）一词表征具有自我指涉特性的事物。就编程而言，元编程意味着对程序本身的编程进行编程。它可以是检查或修改程序的结构，或者改变语言本身的工作方式。ES6 引入了一套围绕元编程的强大特性，为程序的代码机制提供了底层的钩子。在本章中，我们将深入探讨这些特性，并了解元编程在 JavaScript 中如何工作。

### ES5 和 ES6 中的元编程概述

元编程的概念对 JavaScript 来说并不新鲜。你可能每天都在使用元编程，却浑然不觉。例如，检查一个对象是否是另一个对象的原型，我们使用 `a.isPrototypeOf(b)`。这就是一种元编程形式。通常，所有 `Object.*` 方法都可以被视为一种元编程形式。元编程提供了一种巧妙的方式来利用语言的特性和功能，使你能够编写更具灵活性的程序，并高效处理应用程序的自定义需求。

元编程的一个关键策略是反射（Reflection）。它允许我们在运行时检查或修改程序的结构，或改变程序内部（特别是元数据属性和函数）的行为。ES6 通过三种形式的元编程提供了反射能力。

元编程有三种形式：*内省*、*自修改*和*介入*。

- **内省** - 当你的代码检查自身时，例如：`a.isPrototypeOf(b)` 就是内省。`typeof`、`instanceof` 也是内省运算符，因为它们收集关于代码的信息。
- **自修改** - 当你修改程序的结构时。一个例子是 `Object.defineProperty()` 方法，它在对象上定义一个新属性，或者在属性存在时修改它：

```
let cake = {};

console.log(cake);      // {}
```

```
Object.defineProperty(cake, "ingredients", {
    value: ["sugar", "all things nice"],
    enumerable: true,
    configurable: true,
    writable: true
});
```

```
console.log(cake);
// { ingredients: [ 'sugar', 'all things nice' ] }
```

在上面的例子中，请注意我们如何使用 `Object.defineProperty()` 修改了 `cake` 对象的结构。自修改涉及在运行时访问或创建新属性以及修改程序结构的能力。

- **介入** - 当你的代码修改了默认行为，从而影响到其他代码时。介入涉及修改语言的语义，或者在运行时向你的程序添加新的构造。这对 ES6 来说是新的，我们将在本章后面了解更多。

ES6 通过三个新 API 引入了元编程：Symbol、Proxy 和 Reflect。在本书的前面部分，我们已经看到 symbol 如何允许我们创建唯一且不可变的标识符。它们为我们提供了一种高效地为对象创建唯一且不可枚举属性的方式，这有助于将对象的元数据与其公共接口分离。Symbol 还帮助我们自定义对象的默认迭代行为，本质上是通过允许我们在运行时修改程序的行为或在对象上创建新的（且唯一的）属性来提供反射（自修改）。现在让我们看看 Proxy 和 Reflect 带来了什么。

### ES6 中的 Proxy

Proxy 代表了元编程的介入形式。Proxy 对象允许我们拦截任何程序的行为。它们使我们能够修改对象的操作并实现自定义行为。简单地说，可以对对象执行许多操作，proxy 帮助我们修改这些操作并实现所需的行为。这些操作可以是属性查找、赋值、枚举、函数调用等。

Proxy 对象包装目标对象并修改其行为。我们可以使用以下方式创建一个 proxy：

```
const proxy = new Proxy(target, handler);
```

其中 `target` 是其行为被修改的对象，而 `handler` 是一个对象，其属性是函数（称为陷阱），当对 proxy 执行各种操作时，这些函数会被调用。Handler 对象允许我们定义目标对象的新行为。它使我们能够在转发操作到目标/包装对象的基础上执行额外的逻辑。

### Proxy Handler 中的陷阱

Handler 对象提供了一系列方法，这些方法充当 proxy 的陷阱。这些方法是可选的，如果一个陷阱未被定义，默认行为是将操作转发给目标对象。

最常见的陷阱是用于 getter 和 setter。看下面的代码片段，例如，我们为 `get` 属性访问器方法定义了一个陷阱：

```
const restaurant = {
    soda: 2,
    burger: 1
};
```

```
const restHandler = {
    get: function(target, property) {
        if (property in target && target[property] > 0) {
            target[property] -= 1;
            return `Enjoy your ${property}`;
        }
        return `Sorry, We are out of ${property}s!`;
    }
};
```

```
const restProxy = new Proxy(restaurant, restHandler);
```

```
console.log(restProxy.soda);
// Enjoy your soda
```

```
console.log(restProxy.soda);
// Enjoy your soda
```

```
console.log(restProxy.soda);
// Sorry, We are out of sodas!
```

```
console.log(restProxy.burger);
// Enjoy your burger
```

```
console.log(restProxy.burger);
// Sorry, We are out of burgers!
```

在上面的示例中，我们有一个包含可用库存列表和数量的餐厅对象。我们使用代理（proxy）来包装餐厅对象，这使我们能够拦截（或"捕获"）餐厅对象的原生操作，并在其上执行修改后的行为。这里的处理程序（handler）对象包含一个针对 `get` 属性访问器的捕获器（trap），当被调用时，它会接收目标对象（target）和属性名（property）。此方法会捕获所有"get 属性访问器"的调用，并检查该属性是否存在且其值是否大于0；如果条件成立，其值递减，并返回消息 `Enjoy your ${property}`；否则，返回消息 `Sorry, We are out of ${property}s!`。这个 "get" 捕获器可用于拦截目标对象上所有的 getter 事件。类似地，你也可以拦截 setter 事件。请看以下代码片段：

```
const restaurant = {
    soda: 5
};
const restHandler = {
    set: function(target, property, value) {
        target[property] = value;
        console.log(`${property} has been added to inventory`);
    }
}

const restProxy = new Proxy(restaurant, restHandler);

restProxy.beer = 10;
// beer has been added to inventory
```

在此示例中，我们重写了 `set` 属性访问器方法，它覆盖了默认的赋值行为。在验证场景中，代理（Proxy）非常有用。我们可以轻松地使用 `set` 处理程序来验证传递给对象的值。例如，假设我们正在创建一个投票应用程序，只有年龄超过18岁且拥有该国居留权的人才被允许投票：

```
const voterValidator = {
    set: function(obj, prop, value) {
        if (prop === "age") {
            if (!Number.isInteger(value)) {
                throw new TypeError("Input age is not an integer");
            }
            if (value < 18) {
                throw new RangeError("Input age seems invalid");
            }
        } else if (prop === "residency") {
            if (value === false) {
                throw new Error("Residency is mandatory to vote");
            }
        }
    }
}
```

```
// The default behavior to store the value
obj[prop] = value;

// Indicate success
return true;
  }
};

const person = new Proxy({}, voterValidator);

person.age = 23;
person.residency = false;     // Throws an exception
person.age = "young";         // Throws an exception
person.age = 200;             // Throws an exception
```

`set` 捕获器的另一个绝佳用例是数据绑定，你可以在其中设置一个回调方法，当属性被设置时该方法将被调用，并且该回调方法可以响应目标对象属性所做的更改。

除了 **setters**（设置器）和 **getters**（获取器），代理还提供了一系列其他可以设置的捕获器。以下是一些能帮助你更好理解代理的捕获器。

#### has

`has` 捕获器用于拦截 "in" 操作符。如果你想隐藏对象的特定属性，`has` 捕获器会非常有用。即使属性存在于对象上，我们也可以返回 false。请看以下示例，我们使用 `has` 方法来拦截 "in" 操作符，从而隐藏餐厅对象中的啤酒库存。

```
const restaurant = {
  soda: 5,
  beer: 10
};
const restHandler = {
  has: function(target, property) {
    if (property === "beer") {
      return false;
    }
    return property in target;
  }
}

const restProxy = new Proxy(restaurant, restHandler);
console.log("beer" in restProxy);   // false
console.log("soda" in restProxy);   // true
```

在上面的示例中，所有的 "in" 操作符调用都被 "has" 方法捕获。如果属性名是 "beer"，则返回 false；否则，保持默认行为（检查属性是否在目标对象中）。请注意，"has" 只能帮助你阻止 "in" 操作符检测到特定属性。该属性仍然是可枚举的，并且可以通过 `for...in` 循环访问。

#### ownKeys

`ownKeys` 捕获器用于拦截通过 `Object.keys()`、`Object.getOwnPropertyNames()` 或 `Object.getOwnPropertySymbols()` 访问自有属性（owned properties）和自有 symbol 属性（owned symbol properties）的行为。它也可以与 `has` 捕获处理程序结合使用，以增强目标对象属性的隐私性。（请注意，这些属性仍然不是完全私有的）：

```
const restaurant = {
    soda: 5,
    beer: 10
};

const restHandler = {
    has: function(target, property) {
        if (property === "beer") {
            return false;
        }
        return property in target;
    },

    ownKeys: function(target) {
        return ["soda"];
    }
}

const restProxy = new Proxy(restaurant, restHandler);

console.log("beer" in restProxy);             // false
console.log(Object.keys(restProxy));         // ["soda"]
```

你还可以添加另一个捕获处理程序：`getOwnPropertyDescriptor`，它会拦截 `Object.getOwnPropertyDescriptor()` 调用，以进一步增强隐私性。

#### apply

`apply` 捕获器用于拦截函数调用。它接受三个参数：

-   **target**：其行为被修改的目标函数；
-   **context**：调用时作为 `this` 传递给目标的上下文；
-   **args**：应用调用时传递的参数。

请看以下代码片段，例如，我们使用 `apply` 捕获处理程序对最终账单金额应用季节折扣：

```
function getBill(amount) {
    return amount;
}

const billHandler = {
    apply: function(target, context, args) {
        console.log("Applying Discount of 35%");
        return args[0] - (args[0] * 0.35);
    }
}

const billProxy = new Proxy(getBill, billHandler);

console.log(billProxy(300));
// Applying Discount of 35%
// 195
```

由于这里的目标对象是一个函数，这些也被称为函数捕获器，你也可以选择为 `.call()` 和 `.bind()` 方法设置捕获器。

到目前为止，我们已经介绍了足够多的捕获处理程序，以给你一个整体的概念。我们已经了解了代理如何帮助我们拦截 setter 和 getter、装饰对象、添加验证规则、增强隐私，并从根本上修改对象的默认行为。你可以通过以下链接探索更多捕获处理程序：

-   https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Meta_programming。

### 可撤销代理（Revocable Proxy）

ES6 允许我们创建可撤销的代理。`Proxy.revocable()` 方法用于创建一个可撤销的代理对象。与代理对象类似，它也接受一个处理程序（handler）和一个目标对象（target），并返回一个新创建的可撤销代理对象。

一个可撤销代理对象有两个属性：`proxy` 和 `revoke`。

```
const { proxy, revoke } = Proxy.revocable(target, handler);
```

其中，

-   **proxy** - 通过 `new Proxy (target, handler)` 调用创建的代理对象。
-   **revoke** - 一个无参数的函数，用于使代理失效（关闭）。

如果调用 `revoke()` 函数，代理将变得不可用，这意味着任何对处理程序的捕获器调用都将抛出 `TypeError`。一旦代理被撤销，它将保持撤销状态并可被垃圾回收。后续调用 `revoke` 不再有任何效果。请看以下代码片段，例如：

```
const restaurant = {
    soda: 10,
    beer: 5
};

const { proxy, revoke } = Proxy.revocable(restaurant, {});

console.log(proxy.soda);  // 10
console.log(proxy.beer);  // 5

revoke();

console.log(proxy.soda);  // TypeError: Revoked
```

由于可撤销代理允许你完全切断代理及其捕获器，它在需要增强对象安全性的场景中非常有用，例如，如果尝试访问私有属性，则可以撤销代理。我们可以修改上面的示例，以增强 `beer` 属性的隐私性，如下所示：

```
const restaurant = {
    soda: 10,
    beer: 5
};

const resthandler = {
    get: function(target, property) {
        if (property === "beer") {
            revoke();
            return undefined;
        }
        return target[property];
    }
}
const { proxy, revoke } = Proxy.revocable(restaurant, resthandler);

console.log(proxy.soda);  // 10
console.log(proxy.beer);  // undefined
console.log(proxy.soda);  // TypeError: Revoked
```

在上面的示例中，如果访问 `beer` 属性，我们将返回 `undefined` 并撤销代理，从而切断通过代理对目标对象的进一步调用。

到目前为止，我们已经了解了 ES6 中自修改（self-modification）和介入（intercession）的工作原理。现在，让我们通过自省（introspection）来看看反射（Reflection）。



### Reflect

Reflect 是一个内置的全局对象，提供了一系列内省方法。这些方法本质上收集了关于对象运行时级别元操作的信息。除了已有的内省方法（如 `typeof`、`instanceof` 等）之外，Reflect 作为一组重要的内部方法的统一对象包装器，这些内部方法只能通过 JavaScript 引擎内部访问。Reflect 的一个简单实现如下所示：

```
const restaurant = {
    soda: 10,
    beer: 5
};

console.log(Reflect.ownKeys(restaurant));
// ["soda", "beer"]
```

请注意，Reflect 是一个静态对象，因此不能使用 `new` 关键字来创建实例。ES6 Proxy 中的每个陷阱方法，在 Reflect 中都有一个与之对应的反射方法。因此，Reflect 在实现代理陷阱时也非常有用。查看以下使用 Reflect 与 Proxy 的代码片段：

```
const restaurant = {
    soda: 2,
    beer: 5
};

const restHandler = {
    get: function(target, property) {
        if (property === "beer") {
            return undefined;
        }
        return Reflect.get(target, property);
    }
};

const restProxy = new Proxy(restaurant, restHandler);

console.log(restProxy.beer);
// undefined

console.log(restProxy.soda);
// 2
```

同样，在上面的例子中，我们阻止了对 beer 的访问，并使用 `Reflect.get()` 来访问目标对象的其他属性。你应该优先使用 Reflect 而非传统的 `target[property]` 方式，原因之一是：如果对非对象目标使用 `Reflect.get`，它会抛出一个错误，而 `target[property]` 则只是返回 `undefined`。因此，在这里使用 `Reflect.get` 是一个好习惯。查看以下代码片段，例如，我们尝试在非对象目标上获取属性：

```
console.log(Reflect.get(1, "name"));
// TypeError: Reflect.get called on non-object
```

```
console.log(1["name"]);
// undefined
```

除此之外，在 `Function.prototype` 上调用方法时也推荐使用 Reflect，因为如果参数列表为 `null` 或 `undefined`，`Function.prototype.apply` 会以无参数方式调用函数，而 `Reflect.apply` 则会抛出一个错误。另一个原因是 Reflect 提供了更简洁的语法，而 `Function.prototype` 则显得过于冗长。查看以下代码片段，例如：

```
function sayHello() {
    console.log(`${this.name} says hello`);
}

const person = {
    name: "Jack"
};
```

```
Function.prototype.apply.call(sayHello, person);
// Jack says hello
```

```
Reflect.apply(sayHello, person);
// TypeError: CreateListFromArrayLike called on non-object
```

```
Reflect.apply(sayHello, person, []);
// Jack says hello
```

类似地，还有许多其他有用的静态函数，其中一些与代理处理方法同名，以下是一些常见的实用方法：

- **Reflect.get()** — 返回属性值的函数。
- **Reflect.set()** — 为属性赋值的函数。返回一个布尔值，如果更新成功则为 `true`。
- **Reflect.getPrototypeOf()** — 与 `Object.getPrototypeOf()` 相同。
- **Reflect.has()** — `in` 操作符的函数形式。返回一个布尔值，指示是否存在自有属性或继承属性。

### 总结

ES6 中的元编程为我们提供了一种修改内部语言特�行为的方式，它通过提供底层挂钩来访问程序的代码机制。它有三种形式：内省、自我修改和介入。

在本章中，我们学习了新的 Proxy 和 Reflect API，它们帮助我们实现不同形式的元编程。我们还看了一些有趣的例子，其中 Proxy 帮助我们管理对象中的私有属性。我们了解了 Proxy 附带的各种陷阱处理方法，以及它们一一对应的静态 Reflect 方法，以及我们如何在应用程序中利用它们的优势。随着未来 ECMAScript 版本的不断演进，我们期待看到更多有趣的元编程特性，让我们能够更广泛地操控语言的默认内部操作。

# 第 11 章

## 超越 ES6

正如第一章所描述的，ES6 的发布内容非常丰富，它是对现有 JavaScript 版本（即 ES5）的一次重大更新。我们在本书的前几章中已经广泛介绍了所有主要的变化。TC39 花了超过六年的时间才推出了新版语言，期间引入了许多全新的概念和功能。委员会在发布接近尾声时做出的一项重大决定是，他们不会再像之前那样等待太久才得出结论并发布新特性。他们决定正式将 ES6 命名为 ES2015，并且今后将以较小的增量更新发布语言新特性，并以发布年份来标识。在本章中，我们将了解 ES2016 和 ES2017 中的变化和新特性。

### ES2016

ES2016 是对现有 ES2015（ES6）版本的一次小规模增量更新，引入了 `Array.prototype.includes` 方法和指数运算符（`**`）。你还可以查看 KangaX 兼容性表，了解 ES2016 的新特性在支持 JavaScript 的不同浏览器和平台上的支持情况：
https://kangax.github.io/compat-table/es2016plus/.

#### 数组上的 includes 方法

ES2016 在 JavaScript 的数组原型上引入了 `includes` 方法。你可以使用此方法检查某个元素是否存在于数组中。它将返回一个布尔值，表示传入的元素是否是该数组的一部分。考虑以下示例：

```
['apple', 'banana', 'carrot'].includes('apple');     //true
['apple', 'banana', 'carrot'].includes('orange');    //false
```

如上面的例子所示，对水果数组使用 `includes` 方法时，如果传入的元素是数组的一部分则返回 `true`，否则返回 `false`。在传统 JavaScript 中，这种检查通常使用 `indexOf` 方法来完成，它返回元素的索引（如果存在），否则返回 `-1`。因此，上面的例子本质上等价于：

```
['apple', 'banana', 'carrot'].indexOf('apple') >= 0; //true
['apple', 'banana', 'carrot'].indexOf('orange') >= 0; //false
```

上面两条语句与使用 `includes` 的前一个示例效果完全相同，但 `includes()` 和 `indexOf()` 之间的主要区别在于它们与值 `NaN`（Not a Number，非数字）的交互方式，这在识别值时很有帮助。

```
const arr = [NaN];
arr.includes(NaN);       // true
arr.indexOf(NaN);        // -1
```

从这个例子可以明显看出，`indexOf` 不能用于检查数组中的 `NaN` 值，而 `includes` 方法允许我们检查数组中是否存在 `NaN` 值。

#### 指数运算符 **

指数运算符是 ES2016 引入的一种新的算术运算符，它与 Python 等语言中的同类运算符非常相似，使用双星号来计算一个数的指数值。它等价于 `Math` 库中传统的 `pow()` 函数。

```
let a = 2;
let b = 3;
a ** b          //8
Math.pow(a, b) // 8
```

使用指数运算符是计算一个数的幂次方值的快捷方式，例如在这个例子中，2 的 3 次方等于 8。

### ES2017

ES2017 为语言带来了两个主要的新特性，即异步函数（Async functions）和带有共享内存的原子操作（atomics with Shared memory）。它还包括一些较简单的特性，如 `Object.entries()`、`Object.values()`、`Object.getOwnPropertyDescriptors()`、`padStart`、`padEnd`，以及在函数参数列表和调用中使用尾逗号的能力。让我们逐一详细了解这些特性。

#### 异步函数

ES2017 引入了一种处理异步代码的令人兴奋的新方式，这正是 JavaScript 的生存之道。我们已经了解了使用 promises 处理异步操作的流行方法。ES2017 通过使用 `async` 和 `await` 关键字，让这种模式能够以同步方式工作，从而进一步发展了该模式。要正确理解这一点，请考虑以下示例，其中我们只是创建一个返回 promise 的函数：

```
function getData(site) {
  return fetch(site)
    .then(request => request.json())
}
```

对于上面的例子，调用 `getData()` 函数将返回一个 promise，该 promise 将在我们的执行上下文中异步地 settle。现在使用 `async`/`await` 关键字，我们可以让上述基于 promise 的方法利用生成器模式，使我们的代码表现得像同步一样。`async` 总是返回一个 promise，该 promise 可以被解析为一个值，而 `await` 则会挂起执行，直到该 promise settle。我们可以使用 `async`/`await` 关键字重写上面的示例，如下所示：

```
async function getData(site) {
  let request = await fetch(url);
  let text = await request.text();
  return JSON.parse(text);
}
```

请注意，`await` 关键字仅适用于 promise，如果表达式不是 promise，它会将该表达式强制转换为 promise。你也可以在函数表达式、方法定义和箭头函数中使用 `async`，如下所示：

```
// 使用函数表达式：
const getData = async function () {};

// 使用方法定义：
const item = { async getData() {} }

// 使用箭头函数：
const item = async () => {};
```

你可能对前面示例中使用的 `await` 关键字感到好奇：`await` 操作符等待其操作数（即 promise）settle，如果 promise 被 fulfill，其结果就是 fulfill 值；如果 promise 被 reject，它会抛出 rejection 值。因此，我们可以将传统的 `try...catch` 块与 `async`/`await` 一起使用，以更好地处理 promise。

#### 原子操作与共享内存

任何使用过 WebWorkers 的人都已经熟悉创建 worker 的过程。它们是通过分配 `Worker` 对象并传递需要运行的脚本来创建的。worker 通过消息通道进行通信，许多类型的数据都可以通过此通道发送，并且在到达目的地时类型和结构会被保留。在 ES2017 中，要分配共享内存，你可以简单地使用 `SharedArrayBuffer` 构造函数。它就像一个普通的 `ArrayBuffer`，但其内存是共享的。

此外，ES2017 中的这个新规范为我们带来了新的低级 `Atomics` 命名空间对象的概念，它与 `SharedArrayBuffer` 构造函数一起，为我们提供了构建更高层并发抽象的基础构建块。你可以使用这些特性在几个 web worker 和核心线程之间共享 `SharedArrayBuffer` 对象中的数据。这让你能够轻松地在 worker 之间共享数据，从而获得更好的协作。Lars Hansen（Shared Memory 和 Atomics 的原始提案撰写者）撰写的关于此主题的更详细的教程和规范可以在以下链接在线找到：https://github.com/tc39/ecmascript_sharedmem/blob/master/TUTORIAL.md，但这超出了本书的范围。

#### Object.entries() 和 Object.values()

`Object.entries()` 和 `Object.values()` 是 ES2017 中引入的两个新方法。`Object.entries()` 方法在对象上运行时，会返回对象自身可枚举属性的 `[key, value]` 对数组，顺序与 `for-in` 循环提供的一致。但与 `for-in` 循环不同，它不会枚举原型链中的属性。类似地，`Object.values()` 接收一个对象时，会返回其自身可枚举属性值的数组：

```
const myObj = { a: 1, b: 42 };

Object.entries(myObj);   // [['a', 1], ['b', 42]]

Object.values(myObj);    // [1, 42]
```

如上面的示例所示，当传递给 `Object.entries()` 方法时，对象返回一个包含其键/值对的数组，而 `Object.values()` 方法返回属性值。

#### padStart 和 padEnd

`padStart()` 和 `padEnd()` 方法是 ES2017 中引入的两个新字符串方法，它们有助于向字符串添加填充，使得结果字符串的长度等于作为第一个参数传入的长度。你还可以传递第二个可选参数，使用另一个字符串进行填充，而不是默认的空格。考虑以下示例：

```
'string'.padStart(10);               // "    string"

'string'.padStart(10, "abc");       // "abcastring"

'string'.padStart(10,"12345");    // "1234string"

'string'.padStart(8, "0");       // "00string"

'string'.padStart(3);             // "string"

'string'.padEnd(10);               // "string    "

'string'.padEnd(10, "abc");        // "stringabca"

'string'.padEnd(8, "123456");      // "string12"

'string'.padEnd(1);                // "string"
```

如上面的示例所示，向给定字符串添加填充使得结果字符串长度要么大于第一个参数的长度（基于其原始长度）；如果给定的长度更大，则会根据你使用的方法在字符串的开头或末尾添加足量的填充。你还可以使用第二个参数来使用不同的字符串进行填充，而不是使用空格。

#### Object.getOwnPropertyDescriptors()

顾名思义，`Object.getOwnPropertyDescriptors()` 是 ES2017 中的一个新方法，它让你可以精确地检查给定对象所有自身属性的描述符。JavaScript 对象中的属性通常由一个字符串名称和一个属性描述符组成。描述符是属性值、可写布尔值、一个 get 函数、一个 set 函数、一个可配置布尔值和一个可枚举布尔值的记录。考虑以下示例：

```
const myObj = {
   [Symbol('mySymbol')]: 42,
   get random() { return 'test' },
};

console.log(Object.getOwnPropertyDescriptors(myObj));

// Object {random: Object, Symbol(mySymbol): Object}

//  {random:{
//      configurable: true,
//      enumerable: true,
//      get: function random(),
//      set: undefined}
//  [Symbol('mySymbol')]:{
//      configurable: true,
//      enumerable: true,
//      value: 42,
//      writable: true}
//  }
```

对像 `myObj` 这样的对象使用 `Object.getOwnPropertyDescriptors()` 的输出或多或少会像上面那样。请注意，所有这些特性都相当新且具有实验性，因此你可能并不总是得到完全相同的结果。话虽如此，它们正变得越来越标准。

#### 函数参数列表和调用中的尾逗号

ES2017 中的这个特性是一个简单的语法更新。在引入此特性之前，在 JavaScript 中最后一个函数参数之后放一个逗号是不允许的，尽管规范的其余部分（如数组和对象字面量）中相当常见地使用了这种写法。通过 ES2017 的这次更新，你在 JavaScript 中可以获得更统一的尾随逗号语法。所以你可以这样做，

```
const trailFunct = function(x, y, z,) {
    //函数体
}
```

这纯粹是对语言的语法更新，对语言的行为或功能没有重大改变。

### 总结

在本章中，我们探讨了 JavaScript 的各种小型增量更改，以及在撰写本书时已发布的 ES6 之上的更新。TC39 的目标是每年发布新的规范，这些规范从提案阶段进入最终规范阶段，然后纳入语言。它们应该是小型的功能更新，不像 ES6 (ES2015) 那样的巨大变革。

## 索引

### A, B

- Array.from(), 81, 83
- Array.of(), 83–84
- Array.prototype.copyWithin(), 88
- Array.prototype.entries(), 84–85
- Array.prototype.fill(), 87–88
- Array.prototype.find(), 86–87
- Array.prototype.findIndex(), 87
- Array.prototype.keys(), 85
- Array.prototype.values(), 85
- 异步函数, 131
- 异步模块定义 (AMD), 65, 74

### C

- CommonJS 风格模块, 7, 65
- Constructor() 方法, 50

### D

- 解构
  - 赋值, 40
  - 默认值, 41–42
  - 定义, 37
  - JavaScript 中, 47
  - 在 JSON 数据格式中, 37
  - 嵌套值, 42–44
  - 对象和数组, 37–39
  - 参数值, 45–47
  - 剩余语法, 44–45

### E, F

- ECMA 国际, 2
- ECMAScript 2015, 3
- ECMAScript 3.1, 2
- ECMAScript 4, 6
- ECMAScript 6 (ES6)
  - 添加加载器, 7–8
  - 箭头函数, 17–19, 24–25
  - 项目中的 Babel, 6–7
  - 与块级作用域, 11–14
  - 样板代码, 5
- 类
  - 与访问器属性, 53–55
  - 内置类, 63–64
  - 基于类的开发模式, 64
  - 经典的面向类开发, 49
  - 计算的方法名, 56
  - constructor() 方法, 50
  - 构造器环境, 57–58
  - 声明, 51–52
  - 表达式, 52
  - 继承与 super 关键字, 59–61
  - 继承静态属性, 61
  - 语言, 49
  - 可选的构造器方法, 50
  - 属性与私有性, 56
  - 静态方法与属性, 58–59
- 构造器调用, 21–24
- 核心概念, 1
- 默认函数参数, 25–27
- ECMA、ECMAScript 和 JavaScript, 1–3
- ES6/ES2015 知识, 10
- 函数调用, 19
- 函数参数与全局作用域, 16–17



## 索引

ECMAScript 6 (ES6) *（续）*
- 循环结构，34
- 对象字面量，30–31
- 原型方法，96
- 剩余和展开运算符，27–30，35
- "稻草人提案"，2
- 标签模板字面量，32–33
- TDZ（暂时性死区），14–15
- 模板字面量和分隔符，32
- 转译，4，5
- Web 浏览器和 Node.js，4
- webpack 和 webpack-dev-server，6

ES2016
- 数组相关，129–130
- 原子操作和共享内存，132
- ES2017，130
- 幂运算符 **，130
- object.entries()，132
- object.getOwnPropertyDescriptors()，133–134
- object.values()，132
- padStart 和 padEnd，132–133
- 尾随逗号，134

ES2017，130
表达式插值，32

### G, H

生成器，3，35，96，97–108，131

### I, J, K, L

立即执行函数表达式（IIFE），18
中介，118
内省，117
可迭代协议，100
迭代器
- 生成器，102
- 可迭代对象，97–100，101
- 可选方法，106
- 协议，100
- return() 和 throw()，102
- Symbol.iterator，108
- yield 语句，107

### M

Map，91
元编程
- ES5 和 ES6 概述，117–118
- 未来 ECMAScript 版本，127
- 内部语言特性，127
- ES6 中的代理，118
- 代理处理程序中的元编程，119–121，123
- 可撤销代理，123–126

## 模块系统

- 浏览器中的模块，72
- 解构，73
- ES6 中的模块，66
- eval()，74
- 导出，67–68
- 导入，68–71
- JavaScript 应用程序，65
- 模块化语义代码库，74
- 只读绑定，73

### N

新增的 Array.prototype 方法，84

### O

Object.defineProperty()，53
对象解构语法，38
Object.entries()，132
Object.getOwnPropertyDescriptors()，133–134
Object.getOwnPropertySymbols()，77
Object.getOwnSymbolProperties()，122
Object.values()，132
OnResolved() 函数，115

### P, Q

padEnd() 方法，132
padStart() 方法，132
Pending promise（待定状态的 Promise），112
Promise() 构造函数，110

## Promise

- 异步操作，116
- 链式调用，113–114
- 创建，110–111
- 错误处理，114
- 嵌套回调，109
- 对象，110
- setTimeout，109
- 使用 then() 和 catch()，111–113
- XMLHttpRequest，109

### R

- Reflect.get()，126
- Reflect.getPrototypeOf()，126
- Reflect.has()，126
- Reflect.set()，126
- Revoke() 函数，123

### S

- 自我修改，117
- 字符串替换，32
- Symbol.for(key) 方法，79
- Symbol.for(myCar)，79
- Symbol.iterator，98，100–101
- Symbol
    - 应用场景，76–78
    - 内置 Symbol，80
    - 创建，75–76
    - symbol.for(key)，79
    - Symbol.keyFor(symbol)，80
    - .toString() 方法，76

### T

- 暂时性死区（TDZ），14–15，51
- 类型化数组，89–90

### U, V

- 通用模块定义（UMD），65，74

### W, X, Y, Z

- WeakMap，93–94，57–58
- WeakSet，95–96
