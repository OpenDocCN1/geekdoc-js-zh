
# SitePoint：现代 JavaScript 工具与技能

## 前言

毫无疑问，JavaScript 生态系统的变化非常迅速。不仅新工具和框架不断引入和开发，语言本身也随着 ES2015（又名 ES6）的引入发生了巨大变化。可以理解，有许多文章抱怨如今学习现代 JavaScript 开发有多么困难。我们的目标是通过这系列关于现代 JavaScript 的书籍来尽量减少这种困惑。

本书概述了每个现代 JavaScript 开发者应该掌握的基本工具和技能。

## 谁应该读这本书？

本书适合所有希望提高 JavaScript 技能的前端开发者。您需要熟悉 HTML 和 CSS，并对 JavaScript 有合理的理解，才能跟上这些讨论。

## 使用的规范

### 代码示例

书中的代码使用等宽字体显示，如下：

```
 <h1>一个完美的夏日</h1>
<p>这是一个在公园散步的好日子。
 鸟儿在歌唱，孩子们都回学校了。</p> 
```

当需要现有代码来提供上下文而不是重复全部内容时，将显示 `⋮`：

```
 function animate() {
    ⋮
new_variable = "Hello";
}
```

某些代码行应该在一行内，但由于页面限制，我们不得不对它们进行换行。`➥` 表示仅出于格式目的而存在的换行，应该被忽略：

```
 URL.open("http://www.sitepoint.com/responsive-web-
➥design-real-user-testing/?responsive1");
```

你会注意到，我们在整本书中使用了一些特定的布局样式来表示不同类型的信息。请关注以下项目。

#### 提示、注释与警告

##### 嘿，你！

提示（Tips）提供有用的小贴士。

##### 咳，打扰一下……

注释（Notes）是与当前主题相关但并非关重要的补充说明。将它们看作额外的信息片段。

##### 务必始终……

...注意这些重要点。

##### 注意！

警告（Warnings）强调在过程中可能会让你绊倒的任何陷阱。

## 第 1 章：Babel 入门指南

### 作者：James Kolce

本文介绍了 [Babel](https://babeljs.io/)，它是一个 JavaScript 编译器，允许开发者今天就使用下一代 JavaScript。

在构建 Web 应用程序时编写 JavaScript 可能会令人沮丧。我们必须考虑目标浏览器中可用的功能，以及当某个功能未实现时会发生什么。有些人会建议干脆不要使用它，如果我们正在构建复杂的程序，这在大多数情况下是一种痛苦的经历。

幸运的是，某些工具允许我们停止担心支持情况，只需编写我们能写的最好的代码。它们被称为转译器（transpilers）。`transpiler` 是一种将源代码作为输入并产生新源代码作为输出的工具，具有不同的语法，但在语义上尽可能接近——或等同于原始。

Babel 几乎是将现代 JavaScript (ES2015+) 翻译为可在旧浏览器中运行的兼容实现的标准转译器。如果你只想专注于编写 JavaScript，它是完美的解决方案。

尽管 Babel 的主要目标是将最新的 ECMAScript (ES) 标准翻译给旧的（有时是当前的）浏览器，但它可以做得更多。存在一个预设（presets）和插件（plugins）的生态系统，使得添加非标准功能成为可能。每个插件为你的代码提供了新的功能/转换，而预设只是插件的集合。

## 开始上手

根据你的项目和使用的工具，设置 Babel 有多种方法。本文中，我们将解释如何使用 CLI 设置 Babel，尽管如果你正在使用构建系统或框架，可以查看[官方网站](https://babeljs.io/docs/setup/)上的特定说明。大多数情况下，CLI 是最快最简单的方法。如果你是第一次用户，请继续。

在项目上设置 Babel 的第一步是使用 [npm 安装该包](https://babeljs.io/docs/setup/)（此处包）并将其作为开发依赖。假设你已经准备好了 Node.js 环境，只需在终端中运行以下命令：

```
mkdir babel-test
cd babel-test
npm init -y
npm install --save-dev babel
```

这将创建一个目录(`babel-test`)，进入该目录，初始化 npm 项目（从而创建一个 `package.json` 文件），然后作为开发依赖安装 `babel-cli`。

如果你对上述内容有任何疑问，请参考我们关于[安装 Node](https://www.sitepoint.com/quick-tip-multiple-versions-nvm/) 和[使用 npm](https://www.sitepoint.com/beginners-guide-node-manager/) 的教程。

接下来，我们可以打开 `package.json` 在 npm 脚本中添加 `build` 命令：

```json
"scripts": {
  "build": "babel src -d dist"
}
```

这将从 src 目录提取源代码到 dist 目录。然后我们可以执行：

```
npm run build
```

等一下！在运行 Babel 之前，我们必须安装并设置转换代码的插件。此最简单快速的方法是添加 [Env 预设](https://babeljs.io/docs/plugins/preset-env/)，它根据你指定的浏览器选择合适的插件。可以使用以下命令安装：

```
npm install babel-preset-env --save-dev
```

然后在项目根目录下创建一个 `.babelrc` 文件并添加预设：

```json
{
  "presets": ["env"]
}
```

`.babelrc` 文件是你放置所有 Babel 设置的地方。你将主要使用它来设置预设和插件，但还有更多选项。你可以在 [Babel API 页面](https://babeljs.io/docs/usage/api/#options) 查看完整列表。

请注意，取决于你的操作系统，以点开头的文件默认是隐藏的。如果这对你来说有问题（或者你只是更喜欢更少的文件），可以将 Babel 设置放在 `package.json` 文件中，`babel` 键下，如下：

```json
{
  "name": "babel-test",
  "version": "1.0.0",
  "babel": {
    // config
  }
}
```

最后，让我们创建 Babel 期望找到的目录和文件：

```
mkdir src dist
```

并为其提供一些需要转换的内容：

```
let a = 1;
let b = 2;
[a, b] = [b, a];
console.log(a);
console.log(b);
```

此示例使用了[解构赋值](https://www.sitepoint.com/preparing-ecmascript-6-destructuring-assignment/）来交换两个变量的值。

## 运行 Babel

现在你已经有了一个可用的 Babel 安装，可以执行 `build` 命令来运行编译过程：

```
npm run build
```

这将会从 `src/main.js` 获取代码，将其转换为 ES5 代码，并将转换后的代码输出到 `dist/main.js`。

以下是生成的内容：

```
"use strict";

var a = 1;
var b = 2;
var _ref = [b, a];
a = _ref[0];
b = _ref[1];

console.log(a);
console.log(b);
```

如你所见，`let` 已替换为 `var`，并且 Babel 引入了一个临时变量（用下划线表示）来方便交换。

就是这些。你在 `src` 目录中编写的代码将被翻译为旧版本。默认情况下，如果你不在预设（preset）中添加任何选项，它将加载所有转换。你也可以如下所示指定目标浏览器：

```json
  "presets": [
    ["env", {
      "targets": {
        "browsers": ["last 2 versions", "safari >= 7"]
      }
    }]
  ]
```

这将加载支持每个浏览器最后两个版本以及 Safari 7 及以上所需的转换。你可以在 [Browserlist 仓库](https://github.com/ai/browserslist#queries) 中找到目标浏览器的可用选项。

## Babel 生态系统：概述

正如你在上一节中注意到的，安装 Babel 后它不会执行任何操作。我们必须安装一组插件来获得所需的行为，或者可以使用预设（presets），它们是预定义的插件集。

通常，你想要包含的每个功能都会以插件的形式存在。ES2015 的一些示例包括：

* [常量](https://babeljs.io/docs/plugins/check-es2015-constants/)
* [箭头函数](https://babeljs.io/docs/plugins/transform-es2015-arrow-functions/)
* [块级作用函数](https://babeljs.io/docs/plugins/transform-es2015-block-scoped-functions/)
* [类](https://babeljs.io/docs/plugins/transform-es2015-classes/)
* [for-of](https://babeljs.io/docs/plugins/transform-es2015-for-of/)
* [展开运算符](https://babeljs.io/docs/plugins/transform-es2015-spread/)
* [模板字面量](https://babeljs.io/docs/plugins/transform-es2015-template-literals/)

查看 Babel 文档中的[插件页面](https://babeljs.io/docs/plugins/#transform-plugins) 以获取完整列表。

但有时你不想一个一个地包含所有插件。因此，有预构建的预设可以方便安装每个插件的过程。

目前可用的三个官方预设是：

* [Env](https://babeljs.io/docs/plugins/preset-env/)
* [React](https://babeljs.io/docs/plugins/preset-react/)
* [Flow](https://babeljs.io/docs/plugins/preset-flow/)

`Env` 是最常用的，也是我们在这里使用的。它会根据目标浏览器自动加载所有必要的转换，使你的代码兼容。

`React` 预设转换通常在 React 项目中常见的代码，主要增加了对 [Flow](https://flow.org/) 注解和 [JSX](https://facebook.github.io/jsx/) 的兼容性。

最后，`Flow` 预设用于清理 [Flow](https://flow.org/) 类型注解（尽管它并不检查类型是否有效）。

### Babel Polyfill（垫片）

有些 JavaScript 特性无法在语法上进行转换，通常是因为没有实现等效的功能——例如 Promises 和生成器函数（generator functions）。

这类功能必须通过库在浏览器中实现才能在你的代码中使用，这就是 polyfill 的工作。

Babel polyfill 由 [core-js](https://github.com/zloirock/core-js) 和 [Regenerator](https://github.com/facebook/regenerator) 运行时组成。它们共同涵盖了 ES2015+ 中的所有功能。

### 高级用法

如所述，Babel 还可以用于转换语言中尚未实现的功能。一个很好的例子是类字段（class fields）提案（目前处于 [TC39 stage 3：候选阶段](https://github.com/tc39/proposal-class-fields)）。这在 React 开发者之间特别流行，因为它消除了显式将方法绑定到特定组件的必要，并且意味着组件的 `state` 可以声明为类。

[Webpack](https://webpack.js.org/) 已经成为现代 Web 开发最重要的工具之一。它主要是一个用于 JavaScript 的模块打包器，但你可以教它转换你所有的前端资源，如 HTML、CSS 甚至图像。它可以让你对应用发出的 HTTP 请求数量有更多控制，并允许你使用这些资源的其他格式（例如 Pug、Sass 和 ES8）。Webpack 还允许你轻松地使用 npm 包。

本文面向 Webpack 的初学者，将涵盖初始设置与配置、模块、加载器（loaders）、插件（plugins）、代码分割和热模块替换。如果你觉得视频教程很有帮助，我强烈推荐将 Glen Maddern 的[从原理开始 Webpack](https://www.youtube.com/watch?v=WQue1AN93YU) 作为起点，来理解 Webpack 的特殊之处何在。虽然它现在有点久远了，但原理仍然相同，而且是一个非常棒的介绍。

## 示例代码

为了在家里跟着练习，你需要[安装 Node.js](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/)。你也可以[从 GitHub 下载演示应用](https://github.com/markbrown4/webpack-demo)。

## 设置

让我们用 npm 初始化新项目并安装 `webpack` 和 `webpack-cli`：

```
mkdir webpack-demo && cd webpack-demo
npm init -y
npm install --save-dev webpack webpack-cli
```

接下来我们将创建以下目录结构和内容：

```
 webpack-demo
  |- package.json
+ |- webpack.config.js
+ |- /src
+   |- index.js
+ |- /dist
+   |- index.html
```

### `dist/index.html`

```
<!doctype html>
<html
  <head>
    <title>Hello Webpack</title>
  </head>
  <body>
    <script src="bundle.js"></script>
  </body>
</html>
```

### `src/index.js`

```javascript
const root = document.createElement("div")
root.innerHTML = `<p>Hello Webpack.</p>`
document.body.appendChild(root)
```

### `webpack.config.js`

```javascript
const path = require('path')

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist')
  }
}
```

这告诉 Webpack 编译我们入口点 `src/index.js` 中的代码，并在 `/dist/bundle.js` 输出包。让我们添加一个用于运行 Webpack 的 [npm 脚本](https://docs.npmjs.com/misc/scripts)。

### `package.json`

```json
 {
    ...
    "scripts": {
-     "test": "echo \"Error: no test specified\" && exit 1"
+     "develop": "webpack --mode development --watch",
+     "build": "webpack --mode production"
    },
    ...
  }
```

使用 `npm run develop` 命令，我们可以创建第一个包！

```
Asset      Size      Chunks           Chunk Names
bundle.js  2.92 KiB  main  [emitted]  main
```

你现在应该能够在浏览器中加载 `dist/index.html` 并看到“Hello Webpack”的欢迎了。

打开 `dist/bundle.js` 查看 Webpack 做了什么。顶部是 Webpack 的模块引导代码，最底部是我们的模块。你可能还没觉得惊艳，但如果你已经走到了这里，现在就可以开始使用 ES Modules 了，Webpack 将能够创建一个可以在所有浏览器中运行的生产包。

使用 `Ctrl` + `C` 重启构建并运行 `npm run build` 以生产模式编译我们的包。

```
Asset      Size       Chunks           Chunk Names
bundle.js  647 bytes  main  [emitted]  main
```

注意到包的大小从 `2.92 KiB` 降到了 `647 bytes`。

再次查看 `dist/bundle.js`，你会看到一团杂乱的代码。我们的包已经通过 UglifyJS 了压缩：代码运行方式完全相同，但实现了尽可能小的文件大小。

*   `--mode development` 为构建速度和调试进行优化。



`--mode production` 为运行时的执行速度和输出文件大小进行优化。

## 模块

使用 ES Modules，你可以将大型程序分成许多较小的、自独立的程序。

默认情况下，Webpack 知道如何使用 `import` 和 `export` 语句消费 ES Modules。例如，让我们现在尝试一下，安装 [lodash-es](https://lodash.com/) 并添加第二个模块：

```
npm install --save-dev lodash-es
```

### `src/index.js`

```javascript
import { groupBy } from "lodash-es"
import people from "./people"

const managerGroups = groupBy(people, "manager")

const root = document.createElement("div")
root.innerHTML = `<pre>${JSON.stringify(managerGroups, null, 2)}</pre>`
document.body.appendChild(root)
```

### `src/people.js`

```javascript
const people = [
  {
    manager: "Jen",
    name: "Bob"
  },
  {
    manager: "Jen",
    name: "Sue"
  },
  {
    manager: "Bob",
    name: "Shirley"
  }
]

export default people
```

运行 `npm run develop` 启动 Webpack 并刷新 `index.html`。你应该能看到屏幕上打印了按经理分组的人数组。

### 不带相对路径的导入

不带相对路径的导入（如 `'es-lodash'`）是安装到 `/node_modules` 的 npm 模块。自己的模块始终需要相对路径，如 `'./people'`，因为这是区分它们的方法。

注意控制台中，我们的包大小增加到了 `1.41 MiB`！这值得关注，尽管在这种情况下不需要担心。使用 `npm run build` 在生产模式下编译，所有来自 `lodash-es` 的未使用的 lodash 模块都会从包中移除。这种移除未使用导入的过程被称为树摇优化（tree-shaking），是 Webpack 免费提供的功能。

```
> npm run develop

Asset      Size      Chunks           Chunk Names
bundle.js  1.41 MiB  main
```

## 加载器 (loaders) 允许你对文件运行预处理器。让我们通过 [Babel](https://babeljs.io/) 加载 `.js` 时发生了什么：

```
npm install --save-dev babel-loader @babel/preset-env
```

### `webpack.config.js`

```javascript
const path = require('path')

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist')
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /(node_modules|bower_components)/,
        use: {
          loader: 'babel-loader',
        }
      }
    ]
  }
}
```

### `.babelrc`

```json
{
  "presets": [
    ["@babel/env", {
      "modules": false
    }]
  ],
  "plugins": ["syntax-dynamic-import"]
}
```

此配置防止 Babel 将 `import` 和 `export` 语句编译为 ES5，并启用动态导入——我们稍将在代码分割章节中讨论。我们现在可以自由使用现代语言特性，并将编译为在所有浏览器中运行的 ES5。

### Sass

加载器可以链成一系列转换。演示其工作原理的好方法是从我们的 JavaScript 中导入 Sass：

```
npm install --save-dev style-loader css-loader sass-loader node-sass
```

### `webpack.config.js`

```javascript
module.exports = {
  ...
  module: {
    rules: [
      ...
      {
        test: /\.scss$/,
        use: [{
          loader: 'style-loader'
        }, {
          loader: 'css-loader'
        }, {
          loader: 'sass-loader'
        }]
      }
    ]
  }
}
```

这些加载器按相反顺序处理：

*   `sass-loader` 将 Sass 转换为 CSS。

*   `css-loader` 解析 CSS 为 JavaScript 并解析任何依赖。

*   `style-loader` 将我们的 CSS 输出到文档的 `<style>` 标签中。你可以将这些看作函数调用。一个加载器的输出作为下一个加载器的输入：

```
styleLoader(cssLoader(sassLoader("source")))
```

让我们添加一个 Sass 源文件并将其作为模块。

`src/style.scss`

```scss
$bluegrey: #2b3a42;

pre {
  padding: 8px 16px;
  background: $bluegrey;
  color: #e1e6e9;
  font-family: Menlo, Courier, monospace;
  font-size: 13px;
  line-height: 1.5;
  text-shadow: 0 1px 0 rgba(23, 31, 35, 0.5);
  border-radius: 3px;
}
```

`src/index.js`

```javascript
 import { groupBy } from 'lodash-es'
import people from './people'

+ import './style.scss'

  ...
```

使用 `Ctrl` + `C` 和 `npm run develop` 重新构建。在浏览器中刷新 `index.html`，你应该能看到一些样式。

## JS 中的 CSS

我们刚刚以模块的形式从 JavaScript 中导入了一个 Sass 文件。

打开 `dist/bundle.js` 并搜索 `pre {`。确实，我们的 Sass 已经编译成了一个 CSS 字符串并作为模块保存在我们的包中。当我们将此模块导入到 JavaScript 时，`style-loader` 会将该字符串输出到嵌入的 `<style>` 标签中。

### 为什么要这么做？

我在这里不会深入探讨这个话题，但有几个值得考虑的理由：

-   你可能想要包含在项目中的 JavaScript 组件依赖于其他资源才能正常运行（HTML、CSS、图像、SVG）。如果这些内容都能打包在一起，那么导入和使用将要容易得多。

-   死代码消除：当一个 JS 组件不再被你的代码导入时，CSS 也不会再被导入。生成的包将只包含有作用的代码。

-   CSS Modules：CSS 的全局命名空间使得我们很难确定对 CSS 的修改不会产生任何副作用。[CSS 模块](https://github.com/css-modules/css-modules) 通过让 CSS 默认变为局部化，并暴露可以在 JavaScript 中引用的唯一类名来改变这一点。

-   通过巧妙的打包/拆分代码来减少 HTTP 请求的数量。

## 图像

我们将看到的最后一个 loader 示例是使用 `file-loader` 对图像的处理。

在标准的 HTML 文档中，当浏览器遇到 `img` 标签或具有 `background-image` 属性的元素时会获取图像。使用 Webpack，对于小图像，可以将图像源作为字符串存储在 JavaScript 内部进行优化。通过这样做，我们预加载了它们，浏览器以后无需通过单独的请求来获取它们：

```bash
npm install --save-dev file-loader
```

`webpack.config.js`

```javascript
 module.exports = {
    ...
    module: {
      rules: [
        ...
+       {
+         test: /\.(png|svg|jpg|gif)$/,
+         use: [
+           {
+             loader: 'file-loader'
+           }
+         ]
+       }
      ]
    }
  }
```

使用此命令下载[测试图像](https://raw.githubusercontent.com/sitepoint-editors/webpack-demo/master/src/code.png)：

```bash
curl https://raw.githubusercontent.com/sitepoint-editors/webpack-demo/master/src/code.png --output src/code.png
```

使用 `Ctrl` + `C` 和 `npm run develop` 重新构建，你现在可以导入图像作为模块了！

`src/index.js`

```javascript
 import { groupBy } from 'lodash-es'
import people from './people'

  import './style.scss'
+ import './image-example'

  ...
```

`src/image-example.js`

```javascript
import codeURL from "./code.png"

const img = document.createElement("img")
img.src = codeURL
img.style = "background: #2B3A42; padding: 20px"
img.width = 32
document.body.appendChild(img)
```

这将包含一个图像，其中 `src` 属性包含了图像自身的 [data URI](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs)：

```html
<img src="data:image/png;base64,iVBO..." style="background: #2B3A42; padding: 20px" width="32">
```

我们 CSS 中的背景图像也由 `file-loader` 处理。

`src/style.scss`

```scss
 $bluegrey: #2b3a42;

  pre {
    padding: 8px 16px;
-   background: $bluegrey;
+   background: $bluegrey url("code.png") no-repeat center center / 32px 32px;
    color: #e1e6e9;
    font-family: Menlo, Courier, monospace;
    font-size: 13px;
    line-height: 1.5;
    text-shadow: 0 1px 0 rgba(23, 31, 35, 0.5);
    border-radius: 3px;
  }
```

我们 CSS 中的背景图像也由 `file-loader` 处理。

`src/style.scss`

```scss
 $bluegrey: #2b3a42;

  pre {
    padding: 8px 16px;
-   background: $bluegrey;
+   background: $bluegrey url("code.png") no-repeat center center / 32px 32px;
    color: #e1e6e9;
    font-family: Menlo, Courier, monospace;
    font-size: 13px;
    line-height: 1.5;
    text-shadow: 0 1px 0 rgba(23, 31, 35, 0.5);
    border-radius: 3px;
  }
```

我们 CSS 中的背景图像也由 `file-loader` 处理。

`src/style.scss`

```scss
 $bluegrey: #2b3a42;

  pre {
    padding: 8px 16px;
-   background: $bluegrey;
+   background: $bluegrey url("code.png") no-repeat center center / 32px 32px;
    color: #e1e6e9;
    font-family: Menlo, Courier, monospace;
    font-size: 13px;
    line-height: 1.5;
    text-shadow: 0 1px 0 rgba(23, 31, 35, 0.5);
    border-radius: 3px;
  }
```

在浏览器中打开 `http://localhost:5000` 并观察发生了什么。初始只获取了 `bundle.js`。当点击按钮时，聊天模块被导入并初始化。

![显示分块懒性加载的网络请求](img/1521906882lazy-loading.png)

只需极少少的努力，我们已经为应用添加了动态代码分割和模块的懒性加载。这是构建高性能 Web 应用程序的绝佳起点。

## 插件 (Plugins)

`loaders`（加载器）在单个文件上执行转换，而 `plugins`（插件）则在更大的代码块上运行。

既然我们正在打包代码、外部模块和静态资源，我们的构建包将会增长——*非常快*。插件的作用是为了帮助我们以巧妙的方式分割代码，并为生产环境进行优化。

在不经意间，我们已经使用了许多[带有“mode”的默认 Webpack 插件](https://webpack.js.org/concepts/mode/#usage)

### development (开发)

- 提供值为“development”的 `process.env.NODE_ENV`

- `NamedModulesPlugin`

### production (生产)

- 提供值为“production”的 `process.env.NODE_ENV`

- `UglifyJsPlugin`

- `ModuleConcatenationPlugin`

- `NoEmitOnErrorsPlugin`

#### Production (生产)

在添加额外的插件之前，我们将首先拆分配置，以便能够针对每个环境应用特定的插件。

将 `webpack.config.js` 重命名为 `webpack.common.js`，并为开发和生产环境添加配置文件。

```
- |- webpack.config.js
+ |- webpack.common.js
+ |- webpack.dev.js
+ |- webpack.prod.js
```

我们将使用 `webpack-merge` 将通用配置与特定环境的配置合并：

```
npm install --save-dev webpack-merge
```

#### webpack.dev.js

```javascript
const merge = require('webpack-merge')
const common = require('./webpack.common.js')

module.exports = merge(common, {
  mode: 'development'
})
```

#### webpack.prod.js

```javascript
const merge = require('webpack-merge')
const common = require('./webpack.common.js')

module.exports = merge(common, {
  mode: 'production'
})
```

### package.json



```json
 "scripts": {
-    "develop": "webpack --watch --mode development",
-    "build": "webpack --mode production"
+    "develop": "webpack --watch --config webpack.dev.js",
+    "build": "webpack --config webpack.prod.js"
  },
```

现在我们可以将开发环境特定的插件添加到 `webpack.dev.js`，将生产环境特定的插件添加到 `webpack.prod.js`。

#### Split CSS (分割 CSS)

在使用 `ExtractTextWebpackPlugin` 进行生产环境打包时，将 CSS 从 JavaScript 中分离出来被认为最佳实践。

当前的 `.scss` 加载器非常适合开发，因此我们将它们从 `webpack.common.js` 移动到 `webpack.dev.js`，并仅在 `webpack.prod.js` 中添加 `ExtractTextWebpackPlugin`。

```
npm install --save-dev extract-text-webpack-plugin@4.0.0-beta
```

#### webpack.common.js

```javascript
 ...
  module.exports = {
    ...
    module: {
      rules: [
-       {
-         test: /\.scss$/,
-         use: [
-           loader: 'style-loader'
-           }, {
-             loader: 'css-loader'
-           }, {
-             loader: 'sass-loader'
-           ]
-       }
        ...
      ]
    }
  }
```

#### webpack.dev.js

```javascript
 const merge = require('webpack-merge')
const common = require('./webpack.common.js')

module.exports = merge(common, {
  mode: 'development',
+   module: {
+     rules: [
+       {
         test: /\.scss$/,
+         use: [
           loader: 'style-loader'
           }, {
             loader: 'css-loader'
           }, {
             loader: 'sass-loader'
           ]
       }
     ]
   }
})
```

#### webpack.prod.js

```javascript
 const merge = require('webpack-merge')
+ const ExtractTextPlugin = require('extract-text-webpack-plugin')
const common = require('./webpack.common.js')

module.exports = merge(common, {
  mode: 'production',
+   module: {
+     rules: [
+       {
         test: /\.scss$/,
         use ExtractTextPlugin.extract({
           fallback: 'style-loader',
           use: ['css-loader', 'sass-loader']
         })
+       }
     ]
   },

   plugins: [
+     new ExtractTextPlugin('style.css')
   ]
})
```

让我们比较一下构建脚本的输出：

```
> npm run develop

Asset           Size      Chunks           Chunk Names
app.bundle.js   28.5 KiB  app   [emitted]  app
chat.bundle.js  1.4 KiB   chat  [emitted]  chat
```

```
> npm run build

Asset           Size       Chunks        Chunk Names
chat.bundle.js  375 bytes  0  [emitted]  chat
app.bundle.js   1.82 KiB   1  [emitted]  app
style.css       424 bytes  1  [emitted]  app
```

现在我们的 CSS 已经从生产环境构建包中提取出来，我们需要在 HTML 中通过 `<link>` 引用它。

#### dist/index.html

```html
 <!DOCTYPE html>
  <<html>
    <head>
      <meta charset="UTF-8">
      <title>Code Splitting</title>
+     <link href="style.css" rel="stylesheet">
    </head>
    <body>
      <script type="text/javascript" src="app.bundle.js"></script>
    </body>
  </html>
```

这允许在浏览器中并行下载 CSS 和 JavaScript，因此加载速度会比单个构建包更快。它还允许样式在 JavaScript 下载完成之前显示出来。

#### Generating HTML (生成 HTML)

每当我们的输出发生变化时，都必须不断更新 `index.html` 以引用新的文件路径。这正是 `html-webpack-plugin` 要完成的工作。

我们可能还需要同时添加 `clean-webpack-plugin` 来在每次构建之前清理 `dist` 目录。

```
npm install --save-dev html-webpack-plugin clean-webpack-plugin
```

#### webpack.common.js

```javascript
 const path = require('path')
+ const CleanWebpackPlugin = require('clean-webpack-plugin');
+ const HtmlWebpackPlugin = require('html-webpack-plugin');

  module.exports = {
    ...
   plugins: [
     new CleanWebpackPlugin(['dist']),
     new HtmlWebpackPlugin({
       title: 'My killer app'
     })]
  }
```

现在每当我们构建时，`dist` 都会被清理。我们现在也能看到 `index.html` 输出，它包含了正确的路径。

运行 `npm run develop` 输出如下：

```html
<!DOCTYPE html>
  <html>
    <head>
    <meta charset="UTF-8">
    <title>My killer app</title>
    </head>
    <body>
      <script type="text/javascript" src="app.bundle.js"></script>
    </body>
  </html>
```

而 `npm run build` 输出如下：

```html
<!DOCTYPE html>
  <html>
    <head>
    <meta charset="UTF-8">
    <title>My killer app</title>
    <link href="style.css" rel="stylesheet">
    </head>
    <body>
      <script type="text/javascript" src="app.bundle.js"></script>
    </body>
  </html>
```

## Development (开发)

`webpack-dev-server` 提供了一个简单的 Web 服务器并提供 `热重载`，因此你不需要刷新刷新即可看到更改。

### package.json

```json
 {
    ...
    "scripts": {
-     "develop": "webpack --watch --config webpack.dev.js",
+     "develop": "webpack-dev-server --config webpack.dev.js",
    }
    ...
  }
```

```
> npm run develop

ℹ ｢wds｣: 项目运行在 http://localhost:8080/
ℹ ｢wds｣: webpack 输出服务自 /
```

在浏览器中打开 `http://localhost:8080/` 并修改 JavaScript 或 CSS 文件之一。你应该看到它自动构建并刷新。

### HotModuleReplacement (热替换)

`HotModuleReplacement` 插件比热重载更进一步，它可以在不刷新的情况下运行时交换模块。当配置得当时，这在单页应用的开发过程中可以节省大量时间。当页面上有大量状态时，你可以对组件进行增量更改，只有被更改的模块会被替换和更新。

```
+ const webpack = require('webpack')
  const merge = require('webpack-merge')
  const common = require('./webpack.common.js')

  module.exports = merge(common, {
    mode: 'development',
+   devServer: {
+     hot: true
   },
+   plugins: [
+     new webpack.HotModuleReplacementPlugin()
+   ],
    ...
  }
```

现在我们需要从代码中 `accept` 变化的模块以重新初始化内容。

`src/app.js`

```
+ if (module.hot) {
+   module.hot.accept()
+ }

  ...
```

### 热模块替换 (Hot Module Replacement)

当启用热模块替换时，`module.hot` 在开发环境下会被设置为 `true`，在生产环境中设置为 `false`，因此这些代码会被从包中移除。

重新构建并执行以下操作看看会发生什么：

*   点击 `Open chat`（打开聊天）

*   在 `people.js` 模块中添加一个新人员

*   再次点击 `Open chat`

![向聊天中添加人员](img/1521906879hmr.png)

以下是发生的过程：

1.  当点击 `Open chat` 时，获取并初始化 `chat.js` 模块

2.  HMR 监测到 `people.js` 发生了修改

3.  `index.js` 中的 `module.hot.accept()` 导致由该入口块加载的所有模块被替换

4.  当再次点击 `Open chat` 时，将使用更新后模块的代码运行 `chat.init()`。

### CSS 替换

让我们将按钮颜色改为红色看看会发生什么：

`src/app.scss`

```
 button {
    ...
-   background: #24b47e;
+   background: red;
    ...
  }
```

![更改 CSS](img/1521906881hmr2.png)

现在我们可以看到样式即时更新，而不会丢失任何状态。这极大地提升了开发者体验！而且感觉就像未来。

## HTTP/2

使用像 Webpack 这样的模块打包器的主要优势之一是，它通过让你你控制资产如何 `built`（构建）以及如何在客户端被 `fetched`（获取），来帮助提高性能。多年来，合并文件被认为是[最佳实践](https://developer.yahoo.com/performance/rules.html)，以减少客户端需要进行的请求次数。这仍然有效，但 [HTTP/2 现在允许在一次 `single`（单个）请求中交付多个文件](https://www.sitepoint.com/file-bundling-and-http2/)，因此合并不再是万灵药了。你的应用程序实际上可能从许多小文件的单独缓存中获益。这样客户端就可以获取单个更改的模块，而无需再次获取内容 `mostly`（大部分）相同的整个包。

Webpack 的创建者 [Tobias Koppers](https://twitter.com/wSokra) 编写了一篇信息量丰富的文章，解释了为什么即使在 HTTP/2 时代，打包仍然重要。

可以在 [Webpack & HTTP/2](https://medium.com/webpack/webpack-http-2-7083ec3f3ce6) 了解更多信息。

## 轮到你了

我希望你发现这个关于 Webpack 的介绍有所帮助，并能够开始有效地使用它。理解 Webpack 的配置、加载器（loaders）和插件需要一些时间，但学习这个工具如何工作将是值得的。

Webpack 4 的文档目前正在编写中，但组织得非常好。我强烈建议阅读 [Concepts](https://webpack.js.org/concepts/) 和 [Guides](https://webpack.js.org/guides/) 以获取更多信息。这里是你可能感兴趣的其他主题：

*   [开发环境的 Source Maps](https://webpack.js.org/guides/development/#using-source-maps)

*   [生产环境的 Source Maps](https://webpack.js.org/guides/production/#source-mapping)

*   [使用哈希文件名进行缓存失效](https://webpack.js.org/guides/caching/)

*   [拆分 vendor 包](https://webpack.js.org/plugins/commons-chunk-plugin/#explicit-vendor-chunk)

# 第 3 章：Gulp.js 简介

### 作者：Craig Buckler

开发者编写代码的时间非常宝贵。即使我们忽略那些烦人的会议，工作中的很大一部分也涉及消耗你工作日的基础任务：

*   从模板和内容文件生成 HTML

*   压缩新的和修改的图像

*   将 Sass 编译为 CSS 代码

*   从脚本中移除 `console` 和 `debugger` 语句

*   将 ES6 转换为跨浏览器兼容的 ES5 代码

*   代码检查和验证

*   合并并压缩化 CSS 和 JavaScript 文件

*   将文件部署到开发、测试和生产环境服务器。

每当你做出更改时，都必须重复这些任务。你可能初衷良好，但即使是最万无一失的开发者也会忘记压缩一两个图像。随着时间的推移，生产前任务变得越来越艰巨且耗时；你将畏惧那些不可避免的内容和模板变化。这是一项令人枯燥、重复的工作。把时间花在更有价值的任务上不是更好吗？

如果是这样，你需要一个 `task runner`（任务运行器）或 `build process`（构建流程）。

## 这听起来吓人复杂！

创建一个构建流程需要时间。它比手动执行每个任务要复杂，但从长远来看，它可以为你节省大量的精力并减少人为错误。采取务实的方法：

*   自动化最令人痛苦的任务。

*   选择任务运行器软件并坚持一段时间。

*   不要心血来复杂化你的构建流程。

某些工具和概念对你来说可能是新的，但深呼吸，专注于一件事。

## 任务运行器：选项

像 [GNU Make](https://www.gnu.org/software/make/) 这样的工具已经存在了几十年，但 Web 任务运行器是一个相对新的现象。第一个是 [Grunt](http://gruntjs.com/) —— 一种由 JSON 配置控制的 Node.js 任务运行器。Grunt 取得了成功，但也存在一些问题：

1.  Grunt 需要插件来实现文件监听功能。

2.  Grunt 插件通常执行多个任务，这使得自定义变得很别扭。

3.  JSON 配置可能会变得臃肿。

4.  任务运行速度缓慢，因为 Grunt 在处理步骤之间保存文件。

许多问题在后续版本中得到了解决，但 [Gulp](http://gulpjs.com/) 已经并并许多改进：

1.  内置了文件监听功能。

2.  Gulp 插件 `mostly` 设计为执行单一工作。

3.  Gulp 使用的 JavaScript 配置更简洁、易读、易修改，并提供了更好的灵活性。



4. Gulp 运行更快，因为它使用 [Node.js streams](https://www.sitepoint.com/basics-node-js-streams/) 在一系列管道插件之间传递数据。文件只在任务结束时写入。

当然，Gulp 本身并不完美，新的任务运行器如 [Broccoli.js](http://broccolijs.com/)、[Brunch](http://brunch.io/) 和 [webpack](https://webpack.github.io/) 也在竞争开发者的关注。最近，[npm 本身也被推为更简单的选项](https://www.sitepoint.com/guide-to-npm-as-a-build-tool/)。所有工具都有优缺点，但 [Gulp 仍然是首选，目前被超过 40% 的 Web 开发者使用](https://ashleynolan.co.uk/blog/frontend-tooling-survey-2016-results)。

Gulp 需要 Node.js，虽然一些 JavaScript 知识会有帮助，但所有 Web 背景的开发者都能受益。

## 关于 Gulp 4

本教程描述了如何使用 Gulp 3 —— 这是编写时的最新发布版本。Gulp 4 已经开发了一段时间，但仍然是一个测试产品。你可以[使用或切换到 Gulp 4](https://www.joezimjs.com/complete-guide-upgrading-gulp-4/)，但我建议在正式发布之前坚持使用版本 3。

## 第一步：安装 Node.js

你可以从 [nodejs.org/download/](https://nodejs.org/download/) 下载适用于 Windows、macOS 和 Linux 的 Node.js。提供了从二进制文件、包管理器和 Docker 镜像安装的选项，以及完整的说明。

## Windows 用户

Node.js 和 `Gulp` 可以在 Windows 上运行，但如果某些插件依赖于原生 Linux 二进制文件（如图像压缩库），可能无法安装或运行。Windows 10 用户的一个选择是使用新的 [bash 命令行](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide)，它可以解决许多问题。

安装完成后，打开命令提示符并输入：

```
node -v
```

这会显示版本号。你即将将大量使用 `npm` —— 这是用于安装模块的 Node.js 包管理器。检查它的版本号：

```
npm -v
```

## 对于 Linux 用户

Node.js 模块可以全局安装，这样它们在整个系统中都是可用的。然而，除非在 `npm` 命令前加上 `sudo`，否则大多数用户没有权限写入全局目录。有许多[修复 npm 权限的选项](https://docs.npmjs.com/getting-started/fixing-npm-permissions)和像 [nvm 可以提供帮助](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/)这样的工具，但我经常更改默认目录。例如，在基于 Ubuntu/Debian 的平台上：

```
cd ~
mkdir .node_modules_global
npm config set prefix=$HOME/.node_modules_global
npm install npm -g 
```

然后，将以下行添加到 `~/.bashrc` 的末尾：

```
export PATH="$HOME/.node_modules_global/bin:$PATH" 
```

最后，使用此命令更新：

```
source ~/.bashrc 
```

## 第 2 步：全局安装 Gulp

全局安装 Gulp 命令行界面，以便可以在任何项目文件夹中运行 `gulp` 命令：

```
npm install gulp-cli -g
```

使用此命令验证 `Gulp` 是否已安装：

```
gulp -v
```

## 第 3 步：配置你的项目

### 对于 Node.js 项目

如果你已经有了 `package.json` 配置文件，可以跳过此步。

假设你在 `project1` 文件夹中有一个新或现有的项目。导航到该文件夹并使用 `npm` 初始化它：

```
cd project1
npm init
```

会被向你提出一系列问题。输入值或按 `Return` 键以接受默认值。完成后将创建一个 `package.json` 文件，它存储了你的 `npm` 配置设置。

### 对于 Git 用户

Node.js 将模块安装在 `node_modules` 文件夹中。你应该将其添加到 `.gitignore` 文件中，以确保它们不会被提交到仓库中。当将项目部署到另一台电脑时，你可以运行 `npm install` 来恢复它们。

在本文的剩余部分，我们假设你的项目文件夹包含以下子文件夹：

**`src` 文件夹：预处理过的源文件**

它包含以下子文件夹：

*   `html` - HTML 源文件和模板

*   `images` — 原始未压缩图像

*   `js` — 多个预处理过的脚本文件

*   `scss` — 多个预处理过的 Sass `.scss` 文件

**`build` 文件夹：编译/处理后的文件**

Gulp 将根据需要创建文件和子文件夹：

*   `html` — 编译后的静态 HTML 文件

*   `images` — 压缩后的图像

*   `js` — 单个合并并压缩的 JavaScript 文件

*   `css` — 单个编译并压缩的 CSS 文件

你的项目几乎肯定会有不同，但下面的示例使用了此结构。

### 在 Unix 上跟随操作

如果你使用的是基于 Unix 的系统，并且只想跟随教程操作，可以使用以下命令重建文件夹结构：

```
mkdir -p src/{html,images,js,scss} build/{html,images,js,css} 
```

## 第 4 步：本地安装 Gulp

你现在可以使用以下命令在项目文件夹中安装 Gulp：

```
npm install gulp --save-dev
```

这会将 Gulp 安装为开发依赖项，并且 `package.json` 中的 `"devDependencies"` 部分会随之更新。在教程的剩余部分中，我们假定 Gulp 和所有插件都是开发依赖项。

### 替代部署选项

当你的操作系统上的 `NODE_ENV` 环境变量设置为 `production` 时，不会安装开发依赖项。你通常会在上线服务器上通过 Mac/Linux 命令执行此操作：

```
export NODE_ENV=production
```

或者 Windows 上：

```
set NODE_ENV=production
```

本教程假设你的资产将编译到 `build` 文件夹，并提交到你的 Git 仓库或直接上传到服务器。然而，如果你想更改它们的生成方式，在上线服务器上构建资产可能更合适。例如，HTML、CSS 和 JavaScript 文件在生产环境中经过了压缩，但在开发环境中没有。在这种情况下，请对 Gulp 和所有插件使用 `--save` 选项，即：

```
npm install gulp --save
```

这会将 Gulp 设置为 `package.json` 中 `"dependencies"` 部分的应用程序依赖。它会在你输入 `npm install` 时被安装，并在项目部署的任何地方运行。你可以从仓库中移除 `build` 文件夹，因为在需要时可以在任何平台上创建这些文件。

## 第 4 步：创建 Gulp 配置文件

在根目录下创建一个新的 `gulpfile.js` 配置文件。添加一些基础代码开始开始：

```javascript
// Gulp.js 配置

var
  // 模块
  gulp = require('gulp'),

  // 开发模式
  devBuild = (process.env.NODE_ENV !== 'production'),

  // 文件夹
  folder = {
    src: 'src/',
    build: 'build/'
  };
```

这引用了 gulp，并在开发模式下设置 devBuild。

### ES6

6 及以上版本支持 ES6，所以你可以使用箭头函数、`let`、`const`。`gulpfile.js` 还没有任何操作，因为你需要

## 第 5 步：创建 Gulp 任务

Gulp 本身什么不做。你必须：

1.  安装 Gulp 插件，

2.  编写利用这些插件执行有用操作的任务。

编写自己的插件是可能的，但由于已有 3000 多个插件，你可能永远不需要。你可以通过 Gulp 自己的目录 [gulpjs.com/plugins/](http://gulpjs.com/plugins/)、[npmjs.com](https://www.npmjs.com/) 或搜索 "gulp *something*" 来利用它们。

Gulp 提供了三个主要的任务方法：

*   `gulp.task` — 定义一个带有名称、可选依赖项和函数的新任务。

*   `gulp.src` — 设置源文件所在的文件夹。

*   `gulp.dest` — 设置构建文件存放的目标文件夹。

任何数量的插件调用都可以在 `.src` 和 `.dest` 之间通过 `pipe` 设置。

### 图像任务

通过示例演示最好，所以让我们创建一个基础任务，压缩图像并将它们复制到相应的 `build` 文件夹。由于此过程可能耗时，我们只压缩新的和修改过的文件。有两个插件可以帮助我们：[gulp-newer](https://www.npmjs.com/package/gulp-newer) 和 [gulp-imagemin](https://www.npmjs.com/package/gulp-imagemin)。从从命令行安装它们：

```
npm install gulp-newer gulp-imagemin --save-dev
```

现在我们可以在 `gulpfile.js` 顶部引用这两个模块：

```javascript
// Gulp.js 配置

var
  // 模块
  gulp = require('gulp'),
  newer = require('gulp-newer'),
  imagemin = require('gulp-imagemin'),
```

现在我们可以在 `gulpfile.js` 的末尾以函数的形式定义图像处理任务本身：

```
// image processing
gulp.task('images', function() {
  var out = folder.build + 'images/';
  return gulp.src(folder.src + 'images/**/*')
    .pipe(newer(out))
    .pipe(imagemin({ optimizationLevel: 5 }))
    .pipe(gulp.dest(out));
});
```

所有任务在语法上都是相似的。这段代码：

1. 创建了一个名为 `images` 的新任务。

2. 定义了一个带有返回值的函数，该函数……

3. 定义了一个 `out` 文件夹，构建文件将位于其中。

4. 设置 Gulp 的 `src` 源文件夹。`/**/*` 确保子文件夹中的图像也会被处理。

5. 将所有文件管道到 `gulp-newer` 模块。比对应目标文件新的源文件将通过。其他所有文件将被移除。

6. 剩余的新或已更改的文件被管道到 `gulp-imagemin`，该插件设置了一个可选的 `optimizationLevel` 参数。

7. 压缩后的图像输出到由 `out` 设置的 Gulp `dest` 文件夹。

保存 `gulpfile.js` 并在从命令行运行任务之前，在项目的 `src/images` 文件夹中放置一些图像：

```bash
gulp images
```

所有图像都将相应进行压缩，你会看到如下输出：

```
Using file gulpfile.js
Running 'imagemin'...
Finished 'imagemin' in 5.71 ms
gulp-imagemin: image1.png (saved 48.7 kB)
gulp-imagemin: image2.jpg (saved 36.2 kB)
gulp-imagemin: image3.svg (saved 12.8 kB)
```

尝试再次运行 `gulp images`，不会发生任何变化，因为不存在更新的图像。

### HTML 任务

我们现在可以创建一个类似的任务，从源 HTML 文件夹复制文件。我们可以使用 [gulp-htmlclean](https://www.npmjs.com/package/gulp-htmlclean) 插件安全地压缩我们的 HTML 代码，以移除不必要的空格和属性：

```bash
npm install gulp-htmlclean --save-dev
```

随后在 `gulpfile.js` 顶部引用它：

```javascript
var
  // modules
  gulp = require('gulp'),
  newer = require('gulp-newer'),
  imagemin = require('gulp-imagemin'),
  htmlclean = require('gulp-htmlclean'),
```

我们现在可以在 `gulpfile.js` 的末尾创建一个 `html` 任务：

```javascript
// HTML processing
gulp.task('html', ['images'], function() {
  var
    out = folder.build + 'html/',
    page = gulp.src(folder.src + 'html/**/*')
      .pipe(newer(out));

  // minify production code
  if (!devBuild) {
    page = page.pipe(htmlclean());
  }

  return page.pipe(gulp.dest(out));
});
```

此操作复用了 `gulp-newer` 并引入了几个概念：

1. `[images]` 参数表示我们的 `images` 任务在处理 HTML 之前运行（HTML 可能会引用图像）。此数组中可以列出任意数量的依赖任务，所有任务将在任务函数运行之前完成。

2. 只有当 `NODE_ENV` 设置为 `production` 时，我们才将 HTML 管道到 `gulp-htmlclean`。因此，HTML 在开发期间保持未压缩状态，这可能有助于调试。

保存 `gulpfile.js` 并从命令行运行 `gulp html`。`html` 和 `images` 任务都将运行。

### JavaScript 任务

对你来说太简单了？让我们通过构建一个基础模块打包器来处理所有的 JavaScript 文件。它将：

1. 使用 [gulp-deporder](https://www.npmjs.com/package/gulp-deporder) 插件确保首先加载依赖。它通过分析每个脚本顶部的注释来确保正确的顺序。例如，`// requires: defaults.js lib.js`。

2. 使用 [gulp-concat](https://www.npmjs.com/package/gulp-concat) 将所有脚本文件合并为单个 `main.js` 文件。

3. 使用 [gulp-strip-debug](https://www.npmjs.com/package/gulp-strip-debug) 移除所有的 `console` 和 `debugging` ，并使用 [gulp-uglify](https://www.npmjs.com/package/gulp-uglify) 压缩代码。

```javascript
// watch for changes
gulp.task('watch', function() {

  // image changes
  gulp.watch(folder.src + 'images/**/*', ['images']);

  // html changes
  gulp.watch(folder.src + 'html/**/*', ['html']);

  // javascript changes
  gulp.watch(folder.src + 'js/**/*', ['js']);

  // css changes
  gulp.watch(folder.src + 'scss/**/*', ['css']);

});
```

与其立即运行 `gulp watch`，让我们添加一个默认任务：

```javascript
// default task
gulp.task('default', ['run', 'watch']);
```

保存 `gulpfile.js` 并在命令行中输入 `gulp`。你的图片、HTML、CSS 和 JavaScript 都将会被处理，然后 Gulp 将保持活跃状态并在更新并在需要重新运行任务。按下 `Ctrl/Cmd` + `C` 停止监控并返回命令行。

## 第 7 ：大获成功！

你可能觉得这些插件有用：

- [gulp-load-plugins](https://www.npmjs.com/package/gulp-load-plugins) ±无需 `require` 声明加载所有 Gulp 插件模块



- [gulp-preprocess](https://www.npmjs.com/package/gulp-preprocess) — 一个简单的 HTML 和 JavaScript [预处理器](https://github.com/jsoverson/preprocess)
- [gulp-less](https://www.npmjs.com/package/gulp-less) — [Less CSS 预处理器](http://lesscss.org/) 插件
- [gulp-stylus](https://www.npmjs.com/package/gulp-stylus) — [Stylus CSS 预处理器](http://stylus-lang.com/) 插件
- [gulp-sequence](https://www.npmjs.com/package/gulp-sequence) — 按特定顺序运行一系列 gulp 任务
- [gulp-plumber](https://www.npmjs.com/package/gulp-plumber) — 防止 Gulp 在失败时停止的错误处理
- [gulp-size](https://www.npmjs.com/package/gulp-size) — 显示文件大小和节省的空间
- [gulp-nodemon](https://www.npmjs.com/package/gulp-nodemon) — 使用 [nodemon](https://www.npmjs.com/package/nodemon) 在发生变化时自动重启 Node.js 应用
- [gulp-util](https://www.npmjs.com/package/gulp-util) — 包括日志和颜色编码的实用函数

`gulp-util` 中一个实用的方法是 `.noop()`，它可以直接传递数据而不执行任何操作。这可以用于更干净的开发/生产处理代码。例如：

```javascript
var gutil = require('gulp-util');

// HTML processing
gulp.task('html', ['images'], function() {
  var out = folder.src + 'html/**/*';

  return gulp.src(folder.src + 'html/**/*')
    .pipe(newer(out))
    .pipe(devBuild ? gutil.noop() : htmlclean())
    .pipe(gulp.dest(out));

});
```

Gulp 还可以调用其他 Node.js 模块，它们并不一定需要是插件。例如：

- [browser-sync](https://www.npmjs.com/package/browser-sync) — 发生变化时自动加载资源或刷新你的浏览器
- [del](https://www.npmjs.com/package/del) — 删除文件和文件夹（也许可以在每次运行开始时清理 `build` 文件夹）

投入一点时间，Gulp 就能节省许多小时的开发挫败感。优势是：

- [插件非常丰富](https://npmjs.org/browse/keyword/gulpplugin/)
- 使用管道的配置易读且易于遵循
- `gulpfile.js` 可以在其他项目中进行适配和复用
- 你可以减少总页面的权重以提高性能
- 你可以简化你的部署

有用链接：

- [Gulp 首页](http://gulpjs.com/)
- [Gulp 插件](https://npmjs.org/browse/keyword/gulpplugin/)
- [npm 首页](https://www.npmjs.com/)

将上述流程应用于简单的网站，总权重减少了 50% 以上。你可以使用 [页面权重分析工具](http://sitepoint.com/10-best-webpage-weight-analysis-tools/) 或像 [New Relic](http://newrelic.com/?r=phpm) 这样的服务来测试自己的结果，它提供了一系列复杂的应用程序性能监控工具。

Gulp 可以彻底改变你的工作流。我你发现这个教程有用，并考虑在生产流程中使用 Gulp。

# 第 4 章：编译为 JavaScript 的 10 种语言

### 作者 James Kolce

本章包含了十种可以编译为 JavaScript 的有趣语言，可以在浏览器或 Node.js 等平台上执行。

现代应用程序与简单网站相比有[不同的需求](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/)。但浏览器是一个拥有（大部分）固定技术集的平台，JavaScript 仍然是 Web 应用程序的核心语言。任何需要在浏览器中运行的应用程序都必须用该语言实现。

我们都知道 JavaScript 并不是所有任务的最佳语言，在处理复杂应用时，它可能会不从心。为了避免这个问题，人们创建了一些新语言以及现有语言的转换器，它们都能生成可以在环境中运行的代码。

## Dart

Dart 是一种用于构建快速且美观应用的客户端优化语言。它由 Google 开发，可以编译为 JavaScript。

任何需要在浏览器中运行的应用程序都必须用该语言实现。

我们都知道 JavaScript 并不是所有任务的最佳语言，在处理复杂应用时，它可能会不从心。为了避免这个问题，人们创建了一些新语言以及现有语言的转换器，它们都能生成可以在环境中运行的代码。

[TypeScript](https://www.typescriptlang.org/) 是 JavaScript 的超集。一个有效的 JavaScript 程序也是有效的 TypeScript，但增加了静态类型。编译器还可以用作从 ES2015+ 到当前实现的转译器，因此你始终可以获得最新的的特性。

与许多其他语言不同，TypeScript 保持了 JavaScript 的精髓，只添加了旨在提高代码健壮性的功能。这些是类型注解和其他与类型相关的功能，它们让编写 JavaScript 变得更加愉快，这得益于静态分析器等专门化工具的启用，这些工具可以为重构过程提供帮助。此外，类型的添加改进了你应用程序中不同组件之间的接口。

该语言支持类型推断，因此你不需要从一开始就编写所有的类型。你可以编写快速解决方案，然后添加所有类型以对你的代码充满信心。

TypeScript 还支持高级类型，例如交叉类型、联合类型、类型别名、判别式联合和类型守卫。你可以在 [TypeScript 文档](https://www.typescriptlang.org/docs) 网站中的[高级类型](https://www.typescriptlang.org/docs/handbook/advanced-types.html) 页面查看所有内容。

如果你使用 React，通过添加 React 类型定义也可以支持 JSX：

```typescript
class Person {
  private name: string;
  private age: number;
  private salary: number;

  constructor(name: string, age: number, salary: number) {
    this.name = name;
    this.age = age;
    this.salary = salary;
  }

  toString(): string {
    return `${this.name} (${this.age}) (${this.salary})`;
  }
}
```

有关 TypeScript 的更多信息，请查看 SitePoint 的[TypeScript 入门](https://www.sitepoint.com/introduction-to-typescript/) 文章。

## Elm

Elm 是一种纯函数编程语言，可以编译为 JavaScript、HTML 和 CSS。你只需要用 Elm 就可以构建完整的网站，使其成为 React 等 JavaScript 框架的极佳替代方案。用它构建的应用会自动使用虚拟 DOM 库，使其运行非常快。一个很大的优势是内置架构，它让你忘记数据流，转而关注数据声明和逻辑。

在 Elm 中，所有函数都是纯的，这意味着对于给定的输入，它们始终返回相同的输出。除非你指定，否则它们不会执行任何其他操作。例如，要访问远程 API，你需要创建`command`函数与外部世界通信，并使用`subscriptions`监听响应。纯性的另一个点是值是不可变的：当你需要某些东西时，你会创建一个新值，而不是修改它们。

对 Elm 的采用可以是渐进的。你可以使用`ports`与 JavaScript 和其他库进行通信。尽管 Elm 还没有达到版本 1，但它正被用于复杂的大型应用程序，使其成为复杂应用的可行解决方案。

Elm 最具吸引力的特性之一是对初友的编译器，它不会产生难以读懂的信息，而是生成帮助你修复代码的代码。如果你正在学习这种语言，编译器本身可以提供很大帮助。

```elm
module Main exposing (..)

import Html exposing (..)

-- MAIN

main : Program Never Model Msg
main =
    Html.program
        { init = init
        , update = update
        , view = view
        , subscriptions = subscriptions
        }

-- INIT

type alias Model = String

init : ( Model, Cmd Msg )
init = ( "Hello World!", Cmd.none )

-- UPDATE

type Msg
    = DoNothing

update : Msg -> Model -> ( Model, Cmd Msg )
update msg model =
    case msg of
        DoNothing ->
            ( model, Cmd.none )

-- VIEW

view : Model -> Html Msg
view model =
    div [] [text model]

-- SUBSCRIPTIONS

subscriptions : Model -> Sub Msg
subscriptions model =
    Sub.none 
```

如果你想了解更多信息，SitePoint 有篇实用的[Elm 入门](https://www.sitepoint.com/functional-reactive-programming-elm-introduction/) 文章。

## PureScript

[PureScript](http://www.purescript.org/) 是一种由 Phil Freeman 创建的纯函数且强类型编程语言。它的目标是与现有的 JavaScript 库提供强兼容性，在精神上类似于 Haskell，但将 JavaScript 保留在核心。

PureScript 的一个优点是它的极简主义。它不包含任何在其他语言中被认为是本质的功能库。例如，与其在编译器本身中包含生成器和承诺（promises），你可以使用特定的库来完成任务。你可以为需要的特性选择你想要的实现，这使得在使用 PureScript 时能够获得高效且个性化的体验，同时保持生成的代码尽可能小。

其编译器的另一个独特特性是能够在保持库和工具上与 JavaScript 兼容的同时，编写整洁且可读的代码。

与其他语言一样，PureScript 有它自己的[名为 Pulp 的构建工具](https://github.com/purescript-contrib/pulp)，它可以与 Gulp 相比，但是用于用这种语言编写的项目。

关于类型系统——与 Elm（另一种类 ML 语言）不同，PureScript 支持高级类型特性，如[高阶类型](https://en.wikipedia.org/wiki/Kind_%28type_theory%29) 和类型类，这些特性取自 Haskell，允许创建复杂的抽象：

```haskell
module Main where

import Prelude
import Data.Foldable (fold)
import TryPureScript

main =
    render $ fold
      [ h1 (text "Try PureScript!")
      , p (text "Try out the examples below, or create your!")
      , h2 (text "Examples")
      , list (map fromExample)
      ]
  where
    fromExample { title, gist } =
      link ("?=" <> gist) (text title)

    examples =
      [ { title: "Algebraic Data Types"
        , gist: "37c3c97f47a43f20c548"
        }
      , { title: "Loops"
        , gist: "cfdabcd085d4ac3dc46"
        }
      , { title: "Operators"
        , gist: "3044550f29a7c5d3d0"
        ]
```

学习 PureScript，请查看 GitHub 上的[PureScript 入门](https://github.com/purescript/documentation/blob/master/guides/Getting-Started.md) 指南。

## CoffeeScript

CoffeeScript 是一种旨在暴露 JavaScript 优点同时提供更简洁语法的语言。尽管该语言的流行程度近年来一直在下降，但它正在改变方向，并最近获得了一个新的主版本以支持 ES2015+ 特性。

用 CoffeeScript 编写的代码直接转换为可读的 JavaScript 代码，并与现有库兼容。从版本 2 开始，编译器生成的代码与最新版本的 ECMAScript 兼容。例如，每当你使用 `class` 时，你在 JavaScript 中就会得到一个 `class`。此外，如果你使用 React，有一个好消息：JSX 与 CoffeeScript 兼容。

编译器的一个非常独特的特性是能够处理以[文学化风格](https://en.wikipedia.org/wiki/Literate_programming)编写的代码，在这种风格中，不是在代码中强调并将注释作为额外，而是首先编写注释，代码只偶尔出现。这种编程风格由 Donald Knuth 引入，使得代码文件非常像技术文章。

与其他语言不同，CoffeeScript 代码可以使用库直接在浏览器中进行解释。因此，如果你想创建一个快速测试，你可以在 `text/coffeescript` 脚本标签中编写代码，并包含编译器，它将实时将代码转换为 JavaScript：

```coffeescript
# 赋值:
number   = 42
opposite = true

# 条件:
number = -42 if opposite

# 函数:
square = (x) -> x * x

# 数组:
list = [1, 2, 3, 4, 5]

# 对象:
math =
  root:   Math.sqrt
  square: square
  cube:   (x) -> x * square x

# 散参数:
race = (winner, runners...) ->
  print winner, runners

# 存在性:
alert "I knew it!" if elvis?

# 数组推导:
cubes = (math.cube num for num in list)
```

CoffeeScript 网站有一个实用的 [CoffeeScript 2 快速入门](http://coffeescript.org/v2/#coffeescript-2) 资源。

## ClojureScript

ClojureScript 是一个将 Clojure 编程语言翻译为 JavaScript 的编译器。它是一种通用的函数式语言，具有动态类型并支持不可变数据结构。

它是列表中唯一属于 Lisp 编程语言家族的，自然而然，它共享了许多特征。例如，代码可以被视为数据，并且提供了宏系统，使得元编程技术成为可能。与其他 Lisps 不同，Clojure 支持不可变数据结构，这使得副作用的管理变得更加简单。

由于使用了括号，这种语法对初学者来说可能望而生畏，但这种设计有深层次的原因，从长远来看，你一定会欣赏它的。语法上的极简主义和它的语法抽象能力使得 Lisp 成为解决需要高层次抽象问题的强大工具。

尽管 Clojure 主要是一门函数式语言，但它并不像 PureScript 或 Elm 那样纯粹。副作用仍然会发生，但其他函数式特征依然存在。

ClojureScript 使用 Google Closure 进行代码优化，并且与现有的 JavaScript 库兼容。



```js
; 提取自 https://github.com/clojure/clojurescript/blob/master/samples/dom/src/dom/test.cljs

(ns dom.test
  (:require [clojure.browser.event :as event]
            [clojure.browser.dom   :as dom]))

(defn log [& args]
  (.log js/console (apply pr-str args)))

(defn log-obj [obj]
  (.log js/console obj))

(defn log-listener-count []
  (log "listener count: " (event/total-listener-count)))

(def source      (dom/get-element "source"))
(def destination (dom/get-element "destination"))

(dom/append source
            (dom/element "Testing me ")
            (dom/element "out!"))

(def success-count (atom 0))

(log-listener-count)

(event/listen source
              :click
              (fn [e]
                (let [i (swap! success-count inc)
                      e (dom/element :li
                                      {:id "testing"
                                      :class "test me out please"}
                                      "It worked!")]
                  (log-obj e)
                  (log i)
                  (dom/append destination
                              e))))

(log-obj (dom/element "Text node"))
(log-obj (dom/element :li))
(log-obj (dom/element :li {:class "foo"}))
(log-obj (dom/element :li {:class "bar"} "text node"))
(log-obj (dom/element [:ul [:li :li :li]]))
(log-obj (dom/element :ul [:li :li :li]))
(log-obj (dom/element :li {} [:ul {} [:li :li :li]]))
(log-obj (dom/element [:li {:class "baz"} [:li {:class "quux"}]]))

(log-obj source)
(log-listener-count)
```

想要了解更多，请访问 ClojureScript 网站的 [ClojureScript 快速入门](https://clojurescript.org/guides/quick-start) 资源。

## Scala.js

`Scala.js` 是将 `Scala` 编程语言翻译为 `JavaScript` 的编译器。`Scala` 旨在将面向对象和函数式编程的思想合并到一种语言中，创建一个既强大又易于采用的工具。

作为一种强类型语言，你可以获得带有部分类型推断的灵活类型系统的优势。大多数值可以被推断，但函数参数仍然需要显式的类型注解。

虽然它支持许多常见的面向对象模式（例如，每个值都是对象，操作是方法调用），但你也可以获得函数式特征，如支持一等函数和不可变数据结构。

`Scala.js` 的特殊优势之一是，你可以从熟悉的面向对象方法开始，根据需要并按照自己的速度转向更具函数式的方法，而无需进行大量工作。此外，现有的 `JavaScript` 代码和库与你的 `Scala` 代码兼容。

初 `Scala` 开发者会发现这种语言与 `JavaScript` 没有太大区别。对比以下等效代码：

```javascript
// JavaScript
var xhr = new XMLHttpRequest();

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
);
xhr.onload = (e) => {
  if (xhr.status === 200) {
    var r = JSON.parse(xhr.responseText);
    $("#tweets").html(r);
  }
};
```

```javascript
// JavaScript
var xhr = new XMLHttpRequest();

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
);
xhr.onload = (e) => {
  if (xhr.status === 200) {
    var r = JSON.parse(xhr.responseText);
    $("#tweets").html(r);
  }
};
```

```javascript
// JavaScript
var xhr = new XMLHttpRequest();

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
);
xhr.onload = (e) => {
  if (xhr.status === 200) {
    var r = JSON.parse(xhr.responseText);
    $("#tweets").html(r);
  }
};
```

```scala
// Scala.js
val xhr = new XMLHttpRequest()

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
)
xhr.onload = { (e: Event) =>
  if (xhr.status == 200) {
    val r = JSON.parse(xhr.responseText)
    $("#tweets").html(r)
  }
}
xhr.send()
```

```javascript
// JavaScript
var xhr = new XMLHttpRequest();

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
);
xhr.onload = (e) => {
  if (xhr.status === 200) {
    var r = JSON.parse(xhr.responseText);
    $("#tweets").html(r);
  }
};
```

```javascript
// JavaScript
var xhr = new XMLHttpRequest();

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
);
xhr.onload = (e) => {
  if (xhr.status === 200) {
    var r = JSON.parse(xhr.responseText);
    $("#tweets").html(r);
  }
};
```

```javascript
// JavaScript
var xhr = new XMLHttpRequest();

xhr.open("GET",
  "https://api.twitter.com/1.1/search/" +
  "tweets.json?q=%23scalajs"
);
xhr.onload = (e) => {
  if (xhr.status === 200) {
    var r = JSON.parse(xhr.responseText);
    $("#tweets").html(r);
  }
};
```

请查看 [Scala.js 快速入门](https://www.scala-js.org/tutorial/basic/) 以了解更多。

## Reason

`Reason` 是由 `Facebook` 创建并维护的语言，它为 `OCaml` 提供了新的语法，并且可以翻译为 `JavaScript` 和原生代码。

作为 `ML` 家族的一员和函数式语言，它提供了强大但灵活的类型系统、代数类型和模式匹配。它还支持面向对象编程。

可以通过 `buckscript` 使用现有的 `JavaScript` 库。你也可以在 `Reason` 代码中混合 `JavaScript`。

如果你是 `React` 开发者，可以使用绑定，并且该语言支持 `JSX`：

```ocaml
/* 匹配变体类型 */

let possiblyValue1 = None
let possiblyValue2 = Some "Hello@"

match possiblyValue2 with
| None => print_endline "Nothing to see here."
| Some message => print_endline message

/* 参数化类型 */

type universityStudent = {gpa: float};
type response 'studentType = {status: int, student: 'studentType};
let result: response universityStudent = fetchData ();

/* 一个简单的简单的类型对象 */

type payload = Js.t {.
  name: string,
  age: int
};
let obj1: payload = {"name": "John", "age": 30};
```

查看 [Reason 快速入门](https://reasonml.github.io/guide/javascript/quickstart) 以了解更多。

## Haxe

`Haxe` 是一种多范式编程语言，它的编译器可以生成二进制文件和其他源代码。

尽管 `Haxe` 提供了支持类型推断的严格类型系统，但如果目标语言支持，它也可以作为动态语言工作。同样，它支持多种编程风格，如面向对象、泛型和函数式。

当你编写 `Haxe` 代码时，你可以针对多个平台和语言进行编译，而无需进行大量的修改。还可以针对特定目标的代码块。

你可以用 `Haxe` 编写后端和前端，并使用 `Haxe Remoting` 进行通信，支持同步和异步连接。

```javascript
// Example extracted from http://code.haxe.org

extern class Database {
  function new();
  function getProperty<T>(property:Property<T>):T;
  function setProperty<T>(property:Property<T>, value:T):Void;
}

abstract Property<T>(String) {
  public inline function new(name) {
    this = name;
  }
}

class Main {
  static inline var PLAYER_NAME = new Property<String>("playerName");
  static inline var PLAYER_LEVEL = new Property<Int>("playerLevel");

  static function main() {
    var db = new Database();

    var playerName = db.getProperty(PLAYER_NAME);
    trace(playerName.toUpperCase());

    db.setProperty(PLAYER_LEVEL, 1);
  }
}
```

访问 `Haxe` 网站的 [Haxe 入门](https://haxe.org/documentation/introduction/language-introduction.html) 页面获取更多信息。

## Nim

`Nim` 是一种静态类型多范式编程语言，语法极简且对空格敏感，它可以编译为 `JavaScript` 以及 `C`、`C++`。

语言本身非常精简，但它的元编程能力使其非常适合自己实现你可能在其他语言中发现内置的功能。实现这些功能的构建块是 `macros`、`templates` 和 `generics`，通过它们你可以实现从简单功能到不同范式的各种内容。这使得 `Nim` 了一种极其多功能的语言，可以秉持 `Lisp` 的精神适应你的需求。

`Nim` 的语法抽象特性允许你根据自己的问题调整语言，从而实现真正的领域语言 (`DSLs`)。如果你有特殊的任务需要解决，你可以获得更高层次的表达能力：

```nim
## 反转字符串
proc reverse(s: string): string =
  result = ""
  for i in countdown(high(s), 0):
    result.add s[i]

var str1 = "Reverse This!"
echo "Reversed: ", reverse(str1)

## 使用模板
template genType(name, fieldname: expr, fieldtype: typedesc) =
  type
    name = object
      fieldname: fieldtype

genType(Test, foo, int)

var x = Test(foo: 4566)
echo(x.foo) # 4566
```

`Nim` 网站有一些实用的[入门](https://nim-lang.org/documentation.html) 文档提供更多信息。

## 结论

如果 `JavaScript` 不是你喜欢的语言，你仍然可以创建 Web 应用程序，而无需忍受该技术的缺点。创建这些应用程序的选项涵盖了广泛审美，从像 `PureScript` 这样的纯函数式语言到像 `Dart` 这样的面向对象语言。如果你想要比一对一语言翻译更多的东西，还有像 `Elm` 这样的选项，它为你提供了虚拟 DOM 和内置架构等工具。

# 第 5 章：JavaScript 开发者必备的 10 个 VS Code 扩展

### 作者 Michael Wanyoike

在本文中，我将重点介绍一份 `JavaScript` 开发者必备的 `VS Code` 扩展列表。

[Visual Studio Code](https://code.visualstudio.com/) 无疑是今天最受欢迎的轻量级代码编辑器。它大量借鉴了其他流行的代码编辑器，主要是 `Sublime Text` 和 `Atom`。然而，它的成功主要源于提供更好的性能和稳定性的能力。此外，它还提供了许多所需的功能，如 `IntelliSense`，这些功能以前只在 `Eclipse` 或 `Visual Studio 2017` 等全功能 IDE 中可用。

`VS Code` 的力量无疑来自于[市场](https://marketplace.visualstudio.com/vscode)。得益于优秀的开源社区，该编辑器现在能够支持几乎所有的编程语言、框架和开发技术。对库或框架的支持以多种方式实现，主要包括针对特定技术的代码片段（snippets）、语法高亮、`Emmet` 和 `IntelliSense` 功能。

## 按类别划分 VS Code 扩展

对于本文，我将特别关注针对 `JavaScript` 开发者的 `VS Code` 扩展。目前有许多符合这一标准的 `VS Code` 扩展，这意味着我无法提到所有的扩展。相反，我将重点介绍受欢迎且对 `JavaScript` 开发者不可或缺的 `VS Code` 扩展。为了简单起见，我将它们分为十类。

## 代码片段类扩展

当你第一次安装 `VS Code` 时，它带了一些 `JavaScript` 和 `Typescript` 的代码片段。在你开始编写现代 `JavaScript` 之前，你需要一些额外的代码片段来帮助快速编写重复的 ES6/ES7 代码。



## 代码片段类扩展

* [VS Code JavaScript (ES6) 代码片段](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)：目前最受欢迎，截至目前安装量超过 120 万次。该扩展为`JavaScript`、`TypeScript`、`HTML`、`React`和`Vue`扩展提供了 ES6 语法。
* [JavaScript Snippet Pack](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-javascript-snippet-pack)：JavaScript 有用代码片段集合。
* [Atom JavaScript Snippet](https://marketplace.visualstudio.com/items?itemName=gluons.vscode-atom-javascript-snippet)：从`atom/language-javascript`扩展移植的 JavaScript 代码片段。
* [JavaScript Snippets](https://marketplace.visualstudio.com/items?itemName=nathanchapman.JavaScriptSnippets)：ES6 代码片段集。该扩展包含`Mocha`、`Jasmine`以及其他 BDD 测试框架的代码片段。

## 语法类扩展

VS Code 自带了良好的`JavaScript`代码语法高亮。你可以通过安装主题来更改颜色。然而，如果你需要某种程度的可读性，就需要语法高亮器。这里有几个：

* [JavaScript Atom Grammar](https://marketplace.visualstudio.com/items?itemName=ms-vscode.js-grammar)：该扩展用`Atom`编辑器的`JavaScript`语法替换 Visual Code 中的`JavaScript`语法。
* [Babel JavaScript](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel)：ES21x `JavaScript`、`React`、`FlowType`和`GraphQL`的语法高亮。
* [DotENV](https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv)：`.env`文件的语法高亮。如果你在使用`Node`，这非常有用。

## Linter 类扩展

以最少麻烦高效编写 JavaScript 代码需要一个 linter（代码检查工具），为所有团队成员执行特定标准。`ESLint`是最流行的，因为它支持`Standard`、`Google`和`Airbnb`等多种风格。以下是 Visual Code 中最流行的 linter 插件：

* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)：该扩展将 [ESLint](https://eslint.org/) 集成到 VS Code 中。它是最流行的 linter 扩展，目前安装量超过 670 万次。规则在`.eslintrc.json`中配置。
* [JSHint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.jshint)：JSHint](http://jshint.com/about/) 代码检查扩展。使用项目根目录下的`.jshintrc`文件进行配置。
* [JavaScript Standard Style](https://marketplace.visualstudio.com/items?itemName=chenxsan.standardjs)：零配置 linter。执行 [StandardJS 规则](https://github.com/standard/standard)。
* [JSLint](https://marketplace.visualstudio.com/items?itemName=ajhyndman.jslint)：JSLint](http://jslint.com/help.html) linter 扩展。

如果你想了解可用 linter 及其优缺点，请查看我们的 [JavaScript 代码检查工具比较](https://www.sitepoint.com/comparison-javascript-linting-tools/)。

## Node 类扩展

每个 JavaScript 项目都需要至少一个 Node 包，除非你是一个喜欢用困难方式做事的人。这里是一些帮助你更轻松地处理 Node 模块的 VS Code 扩展。

* [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)：使用`package.json`验证已安装的包。确保安装的包具有正确的版本号，高亮显示`package.json`中缺失的已安装包以及尚未安装的包。
* [Node.js Modules IntelliSense](https://marketplace.visualstudio.com/items?itemName=leizongmin.node-module-intellisense)：为 import 语句中的 JavaScript 和 TypeScript 模块提供自动补全。
* [Path IntelliSense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)：它并不真的与 Node 有关，但你确实需要本地文件的 IntelliSense，此扩展将自动补全文件名。
* [Node exec](https://marketplace.visualstudio.com/items?itemName=miramac.vscode-exec-node)：允许你使用 Node.js 执行当前文件或选定的代码。
* [View Node Package](https://marketplace.visualstudio.com/items?itemName=dkundel.vscode-npm-source)：通过此扩展快速查看 Node 包源码，允许你直接从 VS Code 打开 Node 包存储库/文档。
* [Node Readme](https://marketplace.visualstudio.com/items?itemName=bengreenier.vscode-node-readme)：快速打开 npm 包文档。
* [Search node_modules](https://marketplace.visualstudio.com/items?itemName=jasonnutter.search-node-modules)：此扩展允许你搜索`node_modules`文件夹，该文件夹通常在标准搜索之外。
* [Import Cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost)：显示导入包的大小。

## 格式化扩展

偶尔，你会发现自己正在格式化并非偏风格编写的代码。为了节省时间，你可以安装这些 VS Code 扩展之一来快速格式化和重构现有代码：

* [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify)：一个 [jsBeautifier](http://jsbeautifier.org/) 扩展，支持 JavaScript、JSON、CSS 和 HTML。可以通过`.jsbeautifyrc`文件进行自定义。截至目前安装量超过 230 万的最流行的格式化器。
* [Prettier Code Formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)：一个支持使用 [Prettier](https://github.com/prettier/prettier)（一种客观的代码格式化器）格式 JavaScript、TypeScript 和 CSS 的扩展。截至目前安装量超过 150 万。
* [JS Refactor](https://marketplace.visualstudio.com/items?itemName=cmstead.jsrefactor)：为重构 JavaScript 代码提供许多工具和操作，例如提取变量/方法、将现有代码转换为使用箭头函数或模板字面量以及导出函数。
* [JavaScript Booster](https://marketplace.visualstudio.com/items?itemName=sburg.vscode-javascript-booster)：一个强大的代码重构工具。具有多种编码操作，如将`var`转换为`const`或`let`、删除冗余的`else`语句以及合并声明与初始化。很大程度上源自 [WebStorm](https://www.jetbrains.com/webstorm/) 的启发。

## 浏览器扩展

除非你在用 JavaScript 写控制台程序，否则你极可能是在浏览器内部运行 JavaScript 代码。这意味着你需要频繁刷新页面以查看每次对代码进行更新的效果。与其一直手动这样做，这里有几个可以显著缩短迭代过程开发时间的工具：

* [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)：在 Chrome 中轻松调试你的 JavaScript（通过在编辑器内部设置断点）。
* [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)：实时重载功能的静态和动态页面本地开发服务器。
* [Preview on Web Server](https://marketplace.visualstudio.com/items?itemName=yuichinukiyama.vscode-preview-server)：提供 Web 服务器和实时预览功能。
* [PHP Server](https://marketplace.visualstudio.com/items?itemName=brapifra.phpserver)：适用于测试仅需要在客户端运行的 JavaScript 代码。
* [Rest Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)：无需使用浏览器或 CURL 程序来测试你的 REST API 端点，你可以安装此工具直接在编辑器内部交互式地运行 HTTP 请求。

## 框架扩展

对于大多数项目，你需要一个合适的框架来组织代码并缩短开发时间。VS Code 通过扩展支持大多数主流框架。然而，仍然有一些成熟的框架还没有完全开发的扩展程序。

* [Angular 6](https://marketplace.visualstudio.com/items?itemName=Mikael.Angular-BeastCode)：Angular 6 的代码片段。支持 TypeScript、HTML、Angular Material ngRx、RxJS & Flex Layout。截至目前安装量超过 220 万，包含 172 个 Angular 代码片段。
* [Angular v5 snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2)：提供 TypeScript、RxJS、HTML 和 Docker 文件的 Angular 代码片段。截至目前安装量超过 270 万。
* [React Native/React/Redux snippets for es6/es7](https://marketplace.visualstudio.com/items?itemName=EQuimper.react-native-react-redux)：为所有这些框架提供 ES6/ES7 语法的代码片段。
* [React Native Tools](https://marketplace.visualstudio.com/items?itemName=vsmobile.vscode-react-native)：为 React Native 框架提供 IntelliSense、命令和调试功能。
* [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur)：为 Vue 框架提供语法高亮、代码片段、Emmet、代码检查、格式化、IntelliSense 和调试支持。它在 [GitBook](https://vuejs.github.io/vetur/) 上发布了相应的文档。
* [Ember](https://marketplace.visualstudio.com/items?itemName=felixrieseberg.vsc-ember-cli)：为 Ember 提供命令支持和 IntelliSense。安装后，所有的`ember cli`命令都可以通过 Code 自己的命令列表可用。
* [Cordova Tools](https://marketplace.visualstudio.com/items?itemName=vsmobile.cordova-tools)：对 Cordova 插件和 Ionic 框架的支持。为基于 Cordova 项目提供 IntelliSense、调试和其他功能。
* [jQuery Code Snippets](https://marketplace.visualstudio.com/items?itemName=donjayamanne.jquerysnippets)：提供超过 130 个 jQuery 代码片段。通过前缀`jq`激活。

## 测试扩展

测试是软件开发中的关键部分，特别是对于生产阶段的项目。你可以获取 JavaScript 测试的概览，并在我们的指南中了解更多你可以运行的测试类型——[JavaScript 测试：单元 vs 功能 vs 集成](https://www.sitepoint.com/javascript-testing-unit-functional-integration/)。以下是一些流行的测试扩展：

* [Mocha sidebar](https://marketplace.visualstudio.com/items?itemName=maty.vscode-mocha-sidebar)：支持使用 Mocha 库进行测试。此扩展帮助你直接在代码上运行测试并显示错误。
* [ES6 Mocha Snippets](https://marketplace.visualstudio.com/items?itemName=spoonscen.es6-mocha-snippets)：ES6 语法的 Mocha 代码片段。此扩展的重点是保持代码简洁，利用箭头函数并尽可能省略大括号。可以配置为允许分号。
* [Jasmine Code Snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JasmineSnippets)：用于 Jasmine 测试框架的代码片段。
* [Protractor Snippets](https://marketplace.visualstudio.com/items?itemName=deerawan.vscode-protractor-snippets)：用于 Protractor 框架的端到端测试片段。支持 JavaScript 和 TypeScript。
* [Node TDD](https://marketplace.visualstudio.com/items?itemName=prashaantt.node-tdd)：为 Node 和 JavaScript 项目提供测试驱动开发支持。每当源代码更新时，可触发自动测试构建。

## 优秀的扩展

我只是把这下一批 VS Code 扩展放入了“优秀（awesome）”类别，因为这个词最能描述它们！

* [Quokka.js](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode)：一个极其强大的调试工具，为 JavaScript 代码提供了一个快速原型的实验场。带有[卓越的文档](https://quokkajs.com/docs/)。
* [Paste as JSON](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype)：快速将 JSON 数据转换为 JavaScript 代码。



- [Code Metrics](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics): 这是另一个优秀的扩展，用于计算 JavaScript 和 TypeScript 代码的复杂性。

## 扩展包

现在我们来到了最后一个类别，我想告诉大家，VS Code 市场有一个[扩展扩展包类别](https://marketplace.visualstudio.com/search?term=extension%20packs&target=VSCode&category=All%20categories&sortBy=Relevance)。本质上，这些是将相关的 VS Code 扩展打包成一个包的集合，方便安装。以下是一些比较好的扩展包：

- [Nodejs Extension Pack](https://marketplace.visualstudio.com/items?itemName=waderyan.nodejs-extension-pack): 此包包含`ESLint`、`npm`、JavaScript (ES6) 代码段、`node_modules`搜索、`NPM` IntelliSense 和`Path IntelliSense`。

- [VS Code for Node.js - Development Pack](https://marketplace.visualstudio.com/items?itemName=nodesource.vscode-for-node-js-development-pack): 这个包含`NPM` IntelliSense、`ESLint`、Chrome 调试器、`Code Metrics`、`Docker`和`Import Cost`。

- [Vue.js Extension Pack](https://marketplace.visualstudio.com/items?itemName=mubaidr.vuejs-extension-pack): Vue 和 JavaScript 扩展的集合。目前包含大约 12 个 VS Code 扩展，其中一些在这里没有提到，例如 [auto-rename-tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) 和 [auto-close-tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)。

- [Ionic Extension Pack](https://marketplace.visualstudio.com/items?itemName=loiane.ionic-extension-pack): 此包包含许多用于 Ionic、Angular、`RxJS`、Cordova 和 HTML 开发的 VS Code 扩展。

## 总结

VS Code 大量的高质量扩展使其成为 JavaScript 开发者的热门选择。编写如此高效的 JavaScript 代码从未如此简单。像`ESLint`这样的扩展可以帮助你避免常见错误，而像`Debugger for Chrome`这样的扩展可以帮助你更容易地调试代码。Node.js 扩展及其 IntelliSense 功能可以帮助你正确导入模块，而`Live Server`和`REST client`等工具的可用减少了你对外部工具完成工作的依赖。所有这些工具都让你的迭代过程变得简单得多。

希望这个列表可以向您介绍有助于您工作流的新型 VS Code 扩展。

# 第 6 章：使用 VS Code 和 Chrome 调试器调试 JavaScript 项目

### 作者：Michael Wanyoike

调试 JavaScript 并不是 JavaScript 编程中最有趣的方面，但是一项至关重要的技能。本文介绍了两个可以帮助你像专家一样调试 JavaScript 的工具。

想象一下，如果 JavaScript 中不存在`console.log()`函数。我敢肯定你问问自己的第一个问题是：“我该如何确认我的代码运行正常呢？”

答案在于使用调试工具。长期以来，大多数开发者（包括我在内）一直都在使用`console.log`来调试故障代码。它快速且易于使用。然而，如果你不知道 bug 发生在哪里以及是由什么引起的，有时情况会变得棘手。通常你会发现自己在整个代码中到处布下`console.log`陷阱，看看哪一个能揭示罪魁祸首。

为了解决这个问题，我们需要改变习惯并开始使用调试工具。有许多工具可调试 JavaScript 代码，例如 Chrome Dev Tools、[Node Debugger](https://www.sitepoint.com/debugging-javascript-node-debugger/)、`Node Inspect`等。事实上，每种[主流浏览器](https://www.w3schools.com/js/js_debugging.asp)都提供了自己的工具。

在本文中我们将我们将如何使用 Visual Studio Code 提供的调试功能。我们还将查看如何使用 [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) 扩展，该扩展允许 VS Code 与 Chrome Dev Tools 集成。一旦我们完成，你将再也不想用`console.log()`了。

## 前提条件

对于本教程，你只需要对[现代 JavaScript](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/) 有坚实的基础。我们还将查看如何使用 Visual Studio Code 提供的调试功能。我们还将查看如何使用 [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) 扩展，该扩展允许 VS Code 与 Chrome Dev Tools 集成。一旦我们完成，你将再也不想用`console.log()`了。

## 在 VS Code 中调试 JavaScript

我想让你看到的第一个文件是`src/places.js`。你需要在 VS Code 中打开`debug-example`文件夹（*文件* > *打开文件夹*），并在编辑器中选择该文件。

```
const places = [];

module.exports = {
  places,

  addPlace: (city, country) => {
    const id = ++places.length;
    let numType = 'odd';
    if (id % 2) {
      numType = 'even';
    }
    places.push({
      id, city, country, numType,
    });
  },
};
```

代码非常简单，如果你有足够的经验，你会发现它几个 bug。如果你发现了它们，请忽略它们。让我们在底部添加几行代码来手动测试：

```javascript
module.exports.addPlace('Mombasa', 'Kenya');
module.exports.addPlace('Kingston', 'Jamaica');
module.exports.addPlace('Cape Town', 'South Africa');
```

现在，我确信你正急于用`console.log`来输出`places`的值。但让我们不要这样做。相反，让我们添加断点。只需点击左侧行槽——即行号旁边的空白处即可添加：

![指示断点的红点](img/152442833001-breakpoint.png)

看到侧侧的红点了吗？那些就是断点。断点只是一个视觉指示，告诉调试工具在何处暂停。下一步，在操作栏上，点击调试按钮（显示“不允许 Bug”的图标）。

等等，看顶部区域。你会注意到有一个带点的齿轮图标。只需点击它。系统会为你创建一个调试配置文件`launch.json`。按如下所示配置，你就可以让 VS Code 调试器运行`places.js`了：

```json
"configurations": [
  {
    "type": "node",
    "request": "launch",
    "name": "Launch Places",
    "program": "${workspaceFolder}\\src\\places.js"
  }
]
```

### 反斜杠

根据你的操作系统，你可能需要将双反斜杠（`\\`）替换为单正斜杠（`/`）。

保存文件后，你会发现调试面板有了一个新的下拉菜单，`Launch Places`。要运行它，你可以：

* 点击调试面板上的绿色播放按钮

* 按`F5`

* 在菜单栏上点击`Debug` > `Start Debugging`。

使用你喜欢的任何方法，并观察调试过程的运行：

![调试正在运行](img/152442833503-debug-node-running.png)

一旦点击调试按钮，就会接连发生很多事情。首先，编辑器顶部会出现一个工具栏。它包含以下控制按钮：

* **拖动点锚**：用于将工具栏移动到不会遮挡任何内容的地方

* `Continue`：继续调试会话

* `Step over`：逐行执行代码，跳过函数

* `Step into`：逐行执行代码，进入函数内部

* `Step out`：如果已经在函数内部，此命令将带你退出

* `Restart`：重启调试会话

* `Stop`：停止调试会话。

现在，你会发现调试会话暂停在你的第一个断点处。要继续会话，只需点击`Continue`按钮，这将导致执行继续直到到达第二个断点并再次暂停。再次点击`Continue`将完成执行，调试会话也将结束。

让我们通过`F5`重新开始调试。确保两个断点仍然有效。当你放置断点时，代码会暂停在指定的行。除非你点击`Continue`（`F5`）或`Step Over`（`F10`），否则不会执行该行。在点击任何操作之前，让我们看看组成调试面板的各个：

* `Variables`：显示当前作用域内（即执行点处）的局部和全局变量

* `Watch`：你可以手动添加想要监控的变量表达式

* `Call Stack`：显示高亮代码的调用栈

* `Breakpoints`：显示带有断点的文件列表及其行号。

要向`Watch`部分添加表达式，只需点击`+`号并添加任何有效的 JavaScript 表达式——例如`places.length`。当调试器暂停时，如果你的表达式在作用域内，该值将被打印出来。你也可以悬停在当前作用域内的变量上，会出现一个显示其值的弹出窗口。

目前`places`数组是空的。按任何导航控制键查看调试是如何工作的。例如，`Step over`将跳转到下一行，而`Step into`将导航到`addPlace`函数。花一点时间熟悉这些控件。

一旦你完成了一些单步操作，悬停在`places`变量上。会出现弹出窗口。展开内部的值，直到你看到类似的视图：

![places 弹出窗口](img/152442833804-places-hover.png)

你还可以检查所有作用域内的变量。`Variables`部分：

![变量部分](img/152442834005-local-variables.png)

与我们通常使用的`console.log`相比，这简直太棒了。调试器允许我们在更深层次上检查变量。你可能已经注意到`places`数组输出中的几个问题：

1. 数组中有多个空白——即`places[0]`和`places[2]`是`undefined`

2. `numType`属性对奇数`id`值显示为`even`。

目前，只需结束调试会话。我们将在下一节中修复它们。

### 使用 Mocha 进行测试

打开`test/placesTest.js`并检查编写用于测试`places`中代码的代码。如果你从未用过 Mocha，你需要全局安装它以运行测试。

```bash
#### 安装 mocha
npm install -g mocha

#### 运行 mocha 测试
mocha
```

你也可以运行`npm test`来执行测试。你应该会得到如下输出：

![失败的 mocha 测试](img/152442834406-failing-mocha-tests.png)

所有测试都失败了。为了找到问题所在，我们将以调试模式运行测试。为此，我们需要一个新的配置。转到调试面板并点击下拉菜单访问`Add Configuration`选项：

![添加配置](img/152442834507-add-configuration.png)

`launch.json`文件将打开，并弹出一个列出若干供你选择的配置。

![添加 mocha 测试](img/152442834707-mocha-test-configuration.png)

只需选择`Mocha Tests`。将为你插入以下配置：

```json
{
  "type": "node",
  "request": "launch",
  "name": "Mocha Tests",
  "program": "${workspaceFolder}/node_modules/bin/_mocha",
  "args": [
    "-u",
    "tdd",
    "--timeout",
    "99999"
  ],
  "internalConsole": "openSession"
}
```

默认设置是正确的。转到调试面板并选择`Mocha Tests`。你需要注释掉`places.js`中的最后三行；否则测试将无法预期运行。回到`placesTest.js`在发生故障的行之前添加断点。

```javascript
addPlace('Nairobi', 'Kenya');
```

在`Watch`部分添加`places.length`表达式。点击`Play`按钮启动调试会话。

![测试开始](img/152442834908-test-start.png)

在测试开始时，`places.length`应该是 0。如果你点击`Step over`，`places.length`读取为 2，但我们还没有添加内容。重启调试会话，这次使用`Step into`进入`addPlace`函数。调试器将带你进入`places.js`。`places.length`仍然是 0。点击`Step over`执行当前行。

![测试单步](img/152442835209-test-step.png)

啊！`places.length`的值增加了 1，尽管我们还没有向数组添加任何内容。问题出在`++`运算符上，它改变了数组的长度。修复此问题，只需将其替换为：

```javascript
const id = places.length + 1;
```

我们可以安全地获取`id`的值而不改变`places.length`的值。当我们仍处于调试模式时，让我们尝试修复另一个问题：`numType`属性在`id`为 1 时被赋值`even`。问题似乎是`if`语句内部的模表达式：

![if 错误](img/152442835410-if-error.png)

让我们使用调试控制台进行快速实验。为`if`语句开始输入正确的表达式：

![调试控制台](img/152442835511-debug-console.png)

```javascript
id % 2 === 0
```

调试控制台与浏览器控制台类似。它允许你使用当前作用域内的变量进行实验。通过在控制台中尝试一些想法，你可以在不离开编辑器的情况下轻松找到解决方案。现在让我们修复失败的`if`语句：

```javascript
if (id % 2 === 0) {
  numType = 'even';
}
```

重启调试会话并点击`Continue`跳过当前断点。第一个测试“can add a place”现在通过了。但第二个测试没有。为了修复这个问题，我们需要另一个断点。移除当前的断点，并在第 16 行放置一个新的断点，该行为显示：

```javascript
addPlace('Cape Town', 'South Africa');
```

启动一个新的调试会话：

![测试 2 失败](img/152442835812-test2-error.png)

搞定！看一眼`Variables`部分。即使在第二个测试开始之前，我们也发现`places`数组已经包含了由第一个测试创建现有数据。这显然污染了我们当前的测试。为了修复这个问题，我们需要实现某种类型的`setup`函数，为每个测试重置`places`数组。在 Mocha 中实现这一点，只需在测试之前添加以下代码：

```javascript
beforeEach(() => {
  places.length = 0;
});
```

重启调试器并让它停在断点处。现在`places`数组有了一个干净的状态。这应该允许我们的测试在不受污染的情况下运行。只需点击*Continue*（继续）让剩下的测试代码执行。

![Mocha 测试通过](img/152442836013-mocha-tests-passing.png)

现在测试都通过了。你应该感觉棒极了，因为你学会了如何在不写任何一行`console.log`的情况下调试代码。现在让我们来看看如何使用浏览器来调试客户端代码。

## 使用 Chrome 调试器调试 JavaScript



现在你已经熟悉了在 VS Code 中调试 JavaScript 的基础知识，我们将学习如何使用 [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) 扩展调试一个稍微复杂的项目。通过操作栏打开市场面板。搜索该扩展并安装它。

![Debugger for Chrome](img/152442836414-debugger-for-chrome.png)

安装后，点击重载以激活扩展。让我们快速回顾一下即将调试的代码。该 Web 应用程序主要是一个客户端 JavaScript 项目，通过运行 Express 服务器启动：

```
const express = require('express');

const app = express();
const port = 3000;

// Set public folder as root
app.use(express.static('public'));

// Provide access to node_modules folder
app.use('/scripts', express.static(`${__dirname}/node_modules/`));

// Redirect all traffic to index.html
app.use((req, res) => res.sendFile(`${__dirname}/public/index.html`));

app.listen(port, () => {
  console.info('listening on %d', port);
});
```

所有的客户端代码都在 `public` 文件夹中。项目的依赖项包括 Semantic-UI-CSS、jQuery、Vanilla Router、Axios 和 Handlebars。这就是当你使用 `npm start` 运行项目时。你需要在浏览器中打开 URL [localhost:3000](http://localhost:3000) 来查看应用程序。

![缺失地点表格](img/152442836615-places-missing-table.png)

尝试添加一个新的地点。当你这样做时，你会发现似乎什么都没有发生。显然出问题了，是时候查看内部原理了。在开始调试会之前，我们先回顾代码。打开 `public/index.html`。我们目前的关注点是部分：

```
<!-- TEMPLATES -->
<!-- Places Form Template -->
<script id="places-form-template" type="text/x-handlebars-template">
  <h1 class="ui header">
    <i class="map marker alternate icon"></i>
    <div class="content"> Places</div
  </h1>
  <hr>
  <br>
  <form class="ui form">
    <div class="fields">
      <div class="inline field">
        <label>City</label>
        <input type="text" placeholder="Enter city" id="city" name="city">
      </</div>
      <div class="inline field">
        <label>Country</label>
        <input type="text" placeholder="Enter Country" name="country">
      </</div>
      <div class="ui submit primary button">Add Place</div></div>
    </div>
  </form>
  <br>
  <div id="places-table"></div>
</script>

<!-- Places Table Template -->
<script id="places-table-template" type="text/x-handlebars-template">
  <table class="ui celled striped table">
    <thead>
      <tr>
        <th>Id</th>
        <th>City</th>
        <th>Country</th>
        <th>NumType</th>
      </tr>
    </thead>
    <tbody>
      {{#each places}}
      <tr>
        <td>{{id}}</td>
        <td>{{city}}</td>
        <td>{{country}}</td>
        <td>{{numType}}</td>
      </tr>
      {{/each}}
    </tbody>
  </table>
</script>
```

如果你快速扫一眼，代码看起来是正确的。因此，问题一定出在 `app.js` 中。打开该文件并分析那里的代码。下面是你应该注意的代码段。花时间阅读注释以理解代码。

```
// Load DOM roots
const el = $('#app');
const placesTable = $('#places-table');

// Initialize empty places array
const places = [];

// Compile Templates
const placesFormTemplate = Handlebars.compile($('#places-form-template').html());
const placesTableTemplate = Handlebars.compile($('#places-table-template').html());

const addPlace = (city, country) => {
  const id = places.length + 1;
  const numType = (id % 2 === 0) ? 'even' : 'odd';
  places.push({
    id, city, country, numType,
  });
};

// Populate places array
addPlace('Nairobi', 'Kenya');

...

// Places View - '/'
router.add('/', () => {
  // Display Places Form
  const html = placesFormTemplate();
  el.html(html);
  // Form Validation Rules
  $('.ui.form').form({
    fields: {
      city: 'empty',
      country: 'empty',
    },
  });
  // Display Places Table
  const tableHtml = placesTableTemplate({ places });
  placesTable.html(tableHtml);
  $('.submit').on('click', () => {
    const city = $('#city').val();
    const country = $('#country').val();
    addPlace(city, country);
    placesTable.html(tableHtml);
  });
});
```

嗯……这不对。地点已经添加了，但国家没有显示。问题显然不在 HTML 表格代码，因为第一行已经填充了国家单元格，所以 JavaScript 端一定发生了什么。打开 `app.js`，在第 58 行添加断点，该行代码为：

```
addPlace(city, country);
```

重启调试会并再次尝试添加新地点。执行应该会在你设置的断点处暂停。开始将鼠标悬停在相关变量上。你也可以在监视（watch）面板中添加表达式，如下所示：

![发现国家 Bug](img/152442838920-country-bug-found.png)

如你所示，`country` 变量是 `undefined`，但 `city` 变量是有值的。如果你查看在监视面板中设置的 jQuery 选择器表达式，你会发现 `#country` 选择器返回空结果。这意味着它不在 DOM 中。回到 `index.html` 进行验证。

唉！如果你查看定义国家输入的第 59 行，会发现它缺少 `id` 属性。你需要像这样添加一个：

```
<input type="text" placeholder="Enter Country" name="country" id="country">
```

重启调试会话并尝试添加新地点。

![修复国家 Bug](img/152442839121-country-fixed.png)

现在可以工作了！做得好，没有没有 `console.log` 的情况下修复了另一个 Bug。现在让我们处理最后一个 Bug。

### 调试客户端路由

点击导航栏中的 `Convert` 链接。你应该会被带到此视图进行快速转换：

![转换货币](img/152442839322-convert-currency.png)

该部分运行正常。那里没有 Bug。

实际上有的，而且它们与表单无关。要发现它们，请刷新页面。

一旦你点击重新加载，用户就会导航回 `/`，即应用的根目录。这显然是一个路由问题，Vanilla Router 包本应该处理它。回到 `app.js` 寻找这一行：

```
router.navigateTo(window.location.path);
```

这段代码的作用是根据提供的 URL 将用户路由到正确的页面。但为什么不起作用呢？让我们在这里添加一个断点，然后导航回 `/convert` URL 并再次尝试刷新页面。

一旦你刷新，编辑器会在断点处暂停。将鼠标悬停在表达式 `windows.location.path` 上。弹出的窗口显示值为 `undefined`。让我们去调试控制台并输入下面的表达式：

![导航错误](img/15244283923-navigation-error.png)

等一下！调试控制台刚刚给了我们正确的表达式。它应该是读取 `window.location.pathname`。修正该行代码，删除断点并重启调试会话。

导航到 `/convert` URL 并刷新。页面应该加载正确的路径。太棒了！

这是我们要解决的最后一个 Bug 了，但我确实建议你在调试会话中继续实验。设置一个调试会话吧。

在发送请求时，你可以传递许多[额外选项](https://github.com/axios/axios#request-config)，但这里是最常用的几个：

* `baseUrl`：如果你指定了基础 URL，它将会被附加到你使用的任何相对 URL 之前。

* `headers`：一个键/值对的对象，将作为请求头（headers）发送。

* `params`：一个键/值对的对象，该对象将被序列化并作为查询字符串附加到 URL 中。

* `responseType`：如果你期望的响应格式不是于 JSON，可以将此属性设置为 `arraybuffer`、`blob`、`document`、`text` 或 `stream`。

* `auth`：传递一个包含 `username` 和 `password` 字段的对象将使用这些凭据对请求进行 HTTP Basic 认证。

### 便捷方法

就像 jQuery 一样，这里也提供了快捷方法来执行不同类型的请求。

`get`、`delete`、`head` 和 `options` 方法接受两个参数：一个 URL 和一个可选的配置对象。

```
axios.get('/products/5');
```

`post`、`put` 和 `patch` 方法接受数据对象作为第二个参数，并将可选的配置对象作为第三个参数：

```
axios.post(
  '/products',
  { name: 'Waffle Iron', price: 21.50 },
  { options }
);
```

### 接收响应

一旦发送了请求，Axios 会返回一个 promise，该 promise 将解析为响应对象或错误对象。

```
axios.get('/product/9')
  .then(response => console.log(response))
  .catch(error => console.log(error));
```

#### 响应对象

当请求成功时，你的 `then()` 回调将接收一个包含以下属性的响应对象：

* `data`：服务器返回的负载。默认情况下，Axios 期望返回 JSON 并将其为你解析为 JavaScript 对象。

* `status`：服务器返回的 HTTP 状态码。

* `statusText`：服务器返回的 HTTP 状态消息。

* `headers`：服务器返回的所有头。

* `config`：原始请求配置。

* `request`：实际的 `XMLHttpRequest` 对象（在浏览器中运行时）。

#### 错误对象

如果请求出现问题，promise 将被拒绝，并返回一个包含至少某些属性的错误对象：

* `message`：错误消息文本。

* `response`：响应对象（如果已接收），如前一节所述。

* `request`：实际的 `XMLHttpRequest` 对象（在浏览器中运行时）。

* `config`：原始请求配置。

### 转换器与拦截器

Axios 提供了灵感来自 [Angular 的 $http 库](https://docs.angularjs.org/api/ng/service/$http) 的一些巧妙功能。尽管它们看起来相似，但用途略有不同。

#### 转换器

Axios 允许你提供函数来转换传出或传入的数据，形式为发送请求时可以设置的两个配置选项：`transformRequest` 和 `transformResponse`。这两个属性都是数组，允许你链式调用多个数据通过的函数。

任何传递给 `transformRequest` 的函数都适用于 PUT、POST 和 PATCH 请求。它们接收请求数据和 headers 对象作为参数，并必须返回一个修改后的数据对象。

```
const options = {
  transformRequest: [
    (data, headers) => {
      // 对数据进行操作
      return data;
    }
  ]
}
```

函数可以以相同的方式添加到 `transformResponse` 中，但它们仅用响应数据进行调用，并在响应传递给任何链式 `then()` 回调之前执行。

那么，我们可以用转换器做什么呢？一个潜在的用例是处理期望特定格式数据（例如 XML 甚至 CSV）的 API。你可以设置一对转换器，将传出的数据与 API 需要的格式之间进行转换。

值得注意的是，Axios 默认的 `transformRequest` 和 `transformResponse` 函数会在数据与 JSON 之间进行转换，而指定你自己的转换器将覆盖这些设置。

#### 拦截器

虽然转换器允许你修改传出和传入的数据，但 Axios 也还允许你添加称为[拦截器](https://github.com/axios/axios#interceptors) 的函数。与转换器一样，这些函数可以绑定在发送请求时或接收到响应时触发。

```
// 添加请求拦截器
axios.interceptors.request.use((config) => {
    // 在发送请求前做一些事情
    return config;
  }, (error) => {
    // 对请求错误做一些事情
    return Promise.reject(error);
  });

// 添加响应拦截器
axios.interceptors.response.use((response) => {
    // 对响应数据做一些事情
    return response;
  }, (error) => {
    // 对响应错误做一些事情
    return Promise.reject(error);
  });
```

正如你可能从上面的示例中注意到的那样，拦截器与转换器有一些重要的区别。拦截器不仅仅接收数据或头，而是接收完整的请求配置或响应对象。

在创建拦截器时，你还可以选择提供一个错误处理函数，允许你捕获任何错误并进行妥善处理。

请求拦截器可用于此类操作，如[从本地存储中检索令牌并随所有请求发送](https://www.npmjs.com/package/axios-token-interceptor)，而响应拦截器可以用于[捕获 401 响应并重定向到登录页面](https://gist.github.com/yajra/5f5551649b20c8f66aec48549ef5c1f) 进行身份验证。
