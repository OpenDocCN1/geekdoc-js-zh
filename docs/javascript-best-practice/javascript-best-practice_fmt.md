
# JavaScript 最佳实践

## 关于 SitePoint

SitePoint 专门为 Web 行业人士编写有趣、实用且易于理解的内容。访问 `http://www.sitepoint.com/` 访问我们的博客、书籍、通讯、文章和社区论坛。你可以在那里找到关于 JavaScript、PHP、设计等大量信息。

## 前言

毫无疑问，JavaScript 生态系统的变化非常快。不仅新的工具和框架以快速的速度被引入和开发，语言本身随着 ES2015（又称 ES6）的引入也发生了巨大变化。可以理解，有很多文章在抱怨如今学习现代 JavaScript 开发有多么困难。我们的目标是通过这一关于现代 JavaScript 的书籍，尽可能地减少这种困惑。

本书介绍了现代 JavaScript 的最佳实践，利用语言现在可有的功能，让你能够编写更强大、整洁、高性能、可维护且可重的代码。

## 谁应该读这本书？

本书适用于所有希望提高 JavaScript 技能的前端开发者。你需要熟悉 HTML 和 CSS，并对 JavaScript 有合理的理解，才能跟上讨论内容。

## 使用的规范

### 代码示例

书中的代码使用等宽字体显示，如下：`<h1>A Perfect Summer's Day</h1><p>It was a lovely day for a walk in the park. The birds were singing and the kids were all back at school.</p>`

当上下文需要现有代码而不是重复全部内容时，将显示：`function animate() { new_variable = "Hello"; }`

某些代码行应该在一行内，但由于页面限制，我们不得不对其进行换行。➤ 表示仅出于格式目的而存在的换行，应该被忽略：`URL.open("http://www.sitepoint.com/responsive-web-design-real-user-testing/?responsive1");`

你会注意到，我们在整书中使用了某些布局样式来表示不同类型的信息。请关注以下项目。

### 提示、注释和警告

提示（Tips）提供了有用的小提示。

注释（Notes）是与主题相关但并非至关重要的有用补充。将它们想象成额外的信息片段。

警告（Warnings）突出了在执行过程中可能会让你绊脚的任何陷阱。

# 第 1 章：现代 JavaScript 应用程序的构造

James Kolce 著

毫无疑问，JavaScript 生态系统的变化非常快。不仅新的工具和框架以快速的速度被引入和开发，语言本身随着 ES2015（又称 ES6）的引入也发生了巨大变化。可以理解，有很多文章在抱怨如今学习现代 JavaScript 开发有多么困难。我们的目标是通过这一关于现代 JavaScript 的书籍，尽可能地减少这种困惑。

本书介绍了现代 JavaScript 的最佳实践，利用语言现在可有的功能，让你能够编写更强大、整洁、高性能、可维护且可重的代码。

本书适用于所有希望提高 JavaScript 技能的前端开发者。你需要熟悉 HTML 和 CSS，并对 JavaScript 有合理的理解，才能跟上讨论内容。

书中的代码使用等宽字体显示，如下：`<h1>A Perfect Summer's Day</h1><p>It was a lovely day for a walk in the park. The birds were singing and the kids were all back at school.</p>`

当上下文需要现有代码而不是重复全部内容时，将显示：`function animate() { new_variable = "Hello"; }`

某些代码行应该在一行内，但由于页面限制，我们不得不对其进行换行。➤ 表示仅出于格式目的而存在的换行，应该被忽略：`URL.open("http://www.sitepoint.com/responsive-web-design-real-user-testing/?responsive1");`

你会注意到，我们在整书中使用了某些布局样式来表示不同类型的信息。请关注以下项目。

提示（Tips）提供了有用的小提示。

注释（Notes）是与主题相关但并非至关重要的有用补充。将它们想象成额外的信息片段。

警告（Warnings）突出了在执行过程中可能会让你绊脚的任何陷阱。

## 模块

另一个在 ES2015 中新增显著特性是原生模块格式，使得模块的定义和使用成为语言的一部分。加载模块以前仅以第三方库的形式可用。我们将在下一节中深入讨论模块。

这里还有其他我们在这里不会讨论的功能，但我们已经涵盖了你在查看现代 JavaScript 时可能会注意到的一些主要区别。你可以在 [Babel 网站](https://babeljs.io/) 上的 [学习 ES2015](https://developer.mozilla.org/) 页面上查看带有示例的完整列表，你可能会发现这对跟上语言的发展很有帮助。其中一些功能包括模板字符串、块作用域变量和常量、迭代器、生成器、新的数据结构（如 `Map` 和 `Set`）等。

## 代码代码检查 (Code linting)

代码检查工具（Linters）是解析你的代码并将其与一组规则进行比较的工具，用于检查语法错误、格式和良好实践。虽然建议每个人使用代码检查工具，但当你刚开始时，它会格外有用。如果为你的代码编辑器/IDE 配置了正确的工具，你可以获得即时反馈，确保你在学习新功能时不会被语法错误所困扰。

你可以[查看 ESLint](https://eslint.org/)，它是最流行的工具之一，并且支持 ES2015+。

## 模块化代码 (Modular Code)

现代 Web 应用可能会有成千上万（甚至几十万）行代码。如果没有一种机制将所有内容组织成更小的组件，编写专门且隔离的代码片段并在需要时以受控的方式进行复用，那么在这种规模下工作将几乎是不可能的。这就是模块（modules）的工作。

## CommonJS 模块 (CommonJS modules)

多年来出现了一些模块格式，其中最流行的是 CommonJS。它是 Node.js 的默认模块格式，并可以在模块打包器（我们稍后会讨论）的帮助下在客户端代码中使用。

它利用一个模块对象（module object）来从 JavaScript 文件导出功能，并使用 `require()` 在需要的地方导入这些功能。

```javascript
// lib/math.js
function sum(x, y) {
  return x + y;
}
const pi = 3.141593

module.exports = {
  sum: sum,
  pi: pi
};

// app.js
const math = require("lib/math");

console.log("2pi " + math.sum(math.pi, math.pi));
```

## ES2015 模块 (ES2015 modules)

ES2015 引入了一种直接在语言中定义和消费组件的方法，这以前只能通过第三方库实现。你可以拥有包含你所需功能的单独文件，并导出某些部分供你的应用程序使用。

### 原生浏览器支持 (Native Browser Support)

在编写本文时，对 ES2015 模块的原生浏览器支持仍在开发中，因此你目前需要一些额外的工具才能使用它们。

这是一个示例：

```javascript
// lib/math.js

export function sum(x, y) {
  return x + y;
}
export const pi = 3.141593;
```

在这里我们有一个导出函数和变量的模块。我们可以将该文件包含在另一个文件中并使用这些导出函数：

```javascript
// app.js

import * as math from "lib/math";

console.log("2pi = " + math.sum(math.pi, math.pi));
```

或者我们也可以具体，只导入我们需要的：

```javascript
// otherApp.js

import {sum, pi} from "lib/math"

console.log("2pi = " + sum(pi, pi));
```

这些示例提取自 Babel 网站。要深入了解，请查看《理解 ES6 模块》（Understanding ES6 Modules）。

## 包管理 (Package Management)

其他语言长期以来一直有自己的包仓库和管理器，以便更容易地找到和安装第三方库和组件。Node.js 自带了自己的包管理器和仓库，即 npm。虽然还有其他包可用，但 npm 已经成为事实上的 JavaScript 包管理器，并被称为世界上最大的注册表。

在 npm 仓库中，你可以找到第三方模块，通过单一的 `npm install <package>` 命令即可轻松地下载并将其用于你的项目中。包被下载到本地的 `node_modules` 目录，该目录包含了所有包及其依赖项。

你下载的包可以在 `package.json` 文件中被注册为项目的依赖项，同时包含有关你的项目或模块的信息（这些信息可以发布为 npm 上的一个包）。

你可以为开发和生产环境定义不同的依赖。生产依赖是包运行所需要的，而开发依赖仅对于包的开发者来说是必要的。

### 示例 package.json 文件 (Example package.json file)

```json
{
  "name": "demo",
  "version": "1.0.0",
  "description": "Demo package.json",
  "main": "main.js",
  "dependencies": {
    "mkdirp": "^0.5.1",
    "underscore": "^1.8.3"
  },
  "devDependencies": {},
  "scripts": {
    "test": "echo \"Error: no test specified && exit 1\""
  },
  "author": "Sitepoint",
  "license": "ISC"
}
```

## 构建工具 (Build Tools)

我们编写的代码是将来进入生产环境的代码。我们使用现代版本的 JavaScript 编写代码，浏览器可能并不支持它；我们大量使用位于 `node_modules` 文件夹中的第三方包及其自身的依赖项；我们可能会诸如静态分析工具或压缩器等过程。构建工具的存在是为了帮助将所有这些内容转换为可以高效部署并被大多数浏览器理解的内容。

## 模块打包 (Module bundling)

在编写整洁的代码时，我们需要一种机制将所有内容组织成更小的组件，编写专门且隔离的代码片段并在需要时以受控的方式进行复用。这就是模块的工作。

## 应用架构

Web 应用程序与网站有不同的要求。例如，对于博客来说，页面刷新是可以接受的，但对于像 Google Docs 这样的应用则完全不是。你的应用程序行为应该尽可能接近桌面类型，否则易用性将受到影响。

旧式的 Web 应用通常通过从 Web 服务器发送多个页面来实现，当需要大量动态效果时，通过 Ajax 根据用户操作替换 HTML 块来加载内容。虽然这是向更动态的 Web 迈出的巨大一步，但它确实存在其复杂性。每次用户操作都发送 HTML 片段甚至页面都是资源的浪费——从用户的角度来看，尤其是时间的浪费。其易用性仍然无法匹配桌面应用的响应速度。

为了改进这些，我们创建了两种构建 Web 应用的新方法——从我们向用户展示的方式到客户端与服务器之间的通信方式。虽然应用程序所需的 JavaScript 数量也大幅增加，但结果是应用程序的行为非常接近原生应用，每次点击按钮时无需重新加载页面或长时间的等待。

## 单页应用 (SPAs)

Web 应用最常见的高层架构被称为 SPA，全称单页应用（Single Page Application）。SPA 是巨大的 JavaScript 集合，包含了应用程序运行所需的所有内容。UI 完全在客户端渲染，因此不需要重新加载。唯一变化的是应用程序内部的数据，这些数据通常通过 Ajax 或另一种异步通信方法通过远程 API 处理。

这种方法的一个缺点是应用程序首次加载时间较长。然而，一旦加载，视图（页面）之间的切换通常要快得多，因为客户端和服务器之间传输的是纯数据。

## 通用 / 同构应用 (Universal / Isomorphic Applications)

尽管 SPA 提供了极的用户体验，但根据你的需求，它们可能不是最佳解决方案——如果你需要更快的初始响应时间或搜索引擎的最优索引时。

有一种相当新的解决这些问题的方法，被称为同构（或通用）JavaScript 应用。在这种类型的架构中，大部分代码可以同时在服务器和客户端上执行。你可以选择在服务器上渲染的内容，以获得更快的初始页面加载，之后在用户与应用交互时，由客户端接管渲染。由于页面最初是在服务器上渲染的，搜索引擎可以正确地索引它们。

## 部署

在现代 JavaScript 应用中，你编写的代码与你部署到生产环境的代码不同：你只部署构建过程的结果。实现此点的的工作流取决于项目规模、参与开发者数量，有时还取决于你使用的工具/库。

例如，如果你独自开发一个简单的项目，每当你准备好部署时，只需运行构建过程并将生成的文件上传到 Web 服务器即可。请记住，你只需要上传构建过程产生的文件（转译、模块打包、压缩等），这可能只是一个包含你整个应用程序和依赖的单个 `.js` 文件。

你可以拥有这样的目录结构：

```
dist
  app.js
  index.html
node_modules
  src
    lib
      login.js
      user.js
    app.js
    index.html
gulpfile.js
package.json
README
```

因此，你所有的应用程序文件都在 `src` 目录中，使用 ES2015+ 编写，导入了通过 npm 安装的包以及来自 `lib` 目录的自定义模块。

然后你可以运行 Gulp，它将执行 `gulpfile.js` 中的指令来构建你的项目——将所有模块打包成一个文件（包括通过 npm 安装的模块）、将 ES2015+ 转译为 ES5、压缩结果文件等。你可以配置它将结果输出到方便的 `dist` 目录中。

### 重要的文件

如果你有不需要任何处理的文件，可以直接将它们从 `src` 拷贝到 `dist` 目录。你可以在你的构建系统中为此配置一个任务。

现在你只需要将 `dist` 目录中的文件上传到 Web 服务器，而无需担心其他文件（它们仅对开发有用）。

## 团队开发

如果你与其他开发者一起工作，你可能还会使用共享代码仓库（如 GitHub）来存储项目。在这种情况下，你可以在提交之前运行构建过程，并将结果与其他文件一起存储在 Git 仓库中，稍后下载到生产服务器。

然而，如果有多个开发者共同工作，在仓库中存储构建后的文件很容易出错，而且你可能希望保持一切不被构建产物污染。幸运的是，有一种更好的处理该问题的方法：你可以在过程中间加入 Jenkins、Travis CI、CircleCI 等服务，这样它可以在每次提交推送到仓库后自动构建你的项目。开发者只需要担心推送代码更改，而不需要每次都先构建项目。仓库也会保持没有自动生成的文件，而且最后，你仍然拥有可部署的构建文件。

## 结论

如果你已经离开 Web 开发几年了，从简单的 Web 页面到现代 JavaScript 应用的转变可能看起来望而生畏，但我希望这篇文章可以作为一个起点。我尽可能为每个主题链接了更深入的文章，以便你进一步探索。

并记住，如果在某一点，在查看了所有可用选项后，一切看起来都难以应对且混乱，请记住 KISS 原则（保持简单），只使用你认为需要的，而不是你拥有的。根结底，解决问题才是重要的，而不是使用最新的一切。

# 第 2 章：使用 ES6 默认参数与属性简写编写洁代码

作者 Moritz Kröger

创建一个方法意味着编写一个 API——无论是为了你自己、团队中的其他开发者，还是使用你项目的其他开发者。根据你函数的规模、复杂性和目的，你必须考虑默认设置以及输入输出的 API。

默认函数参数和简写是 ES6 的两个实用特性，可以帮助你编写 API。

## ES6 默认参数

让我们快速复习一下知识并再次查看语法。默认参数允许我们用默认值初始化函数。当参数缺失或为 `undefined` 时会使用默认值——这意味着 `null` 是一个有效值。默认参数可以是从数字到其他任何类型

```javascript
// 基础语法
function multiply(a, b = 2) {
  return a * b;
}
multiply(5); // 10

// 默认参数也可以用于后置默认
function foo(num = 1, multi = multiply(num)) {
  return [num, multi];
}
foo(); // [1, 2]
foo(6); // [6, 12]
```

## 真实世界示例

让我们来看一个基础函数，演示默认参数如何加速你的开发并使代码组织更良好。

我们的示例方法名为 `createElement()`。它接受几个配置参数并返回一个 HTML 元素。API 看起来如下：

```javascript
// 我们想要一个 <p> 元素，带有一些文本内容并附加两个类名。
// 返回 <p class="very-special-text super-big">Such unique text</p>
createElement('p',
  content: 'Such unique text',
  classNames: ['very-special-text', 'super-big']
);

// 为了让这个方法更有用，当省略任何参数或未传递参数时，
// 它应该始终返回一个默认元素。
```

```javascript
createElement(); // <div class="module-text default">Very default</div>
```

此实现不会包含太多逻辑，但由于其默认覆盖范围很大，代码可能会变得庞大。

```javascript
// 如果没有默认参数，它看起来非常臃肿且不必要的大。
function createElement (tag, config) {
  tag = tag || 'div';
  config = config || {};

  const element = document.createElement(tag);
  const content = document.content || 'Very default';
  const text = document.createTextNodeNode(content);
  let classNames = config.classNames;

  if (classNames === undefined) {
    classNames = ['module-text', 'default'];
  }
  element.classList.add(...classNames);
  element.appendChild(text);

  return element;
}
```

到目前为止良好。这里发生了什么？我们正在执行以下操作：

1. 为我们的参数 `tag` 和 `config` 设置默认值，以防未未传递（注意，某些 linter 工具不喜欢重新赋值）
2. 创建带有实际内容（以及默认值）的常量
3. 检查 `classNames` 是否定义，如果没有定义则分配一个默认数组
4. 在返回元素之前创建并修改它。

现在，让我们对这个函数进行优化，使其更整洁、编写更快，并且让它的目的比实际用途更直观：

```javascript
// 设置所有默认
function createElement (tag = 'div', {
  content = 'Very default',
  classNames = ['module-text', 'special']
} = {}) {
  const element = document.createElement(tag);
  const text = document.createTextNodeNode(content);

  element.classList.add(...classNames);
  element.appendChild(text);

  return element;
}
```

我们没有触动函数的逻辑，但从函数体中删除了所有的默认处理。函数签名现在包含了所有的默认值。

让我进一步解释其中一部分，它可能会稍微让人感到困惑：

```javascript
// 这里确切发生了什么？
function createElement ({
  content = 'Very default',
  classNames = ['module-text', 'special']
}) = {}) {
  // function body
}
```

我们不仅声明了一个默认对象参数，还声明了对象的属性默认值。这使得默认配置应该是什么样变得更加直观，而不是仅仅声明一个默认对象（例如 `config = {}`）稍后设置默认属性。这可能需要一些额外的时间来习惯，但最终它改进了你的工作流。

当然，我们仍然可以针对更大的配置进行争论，认为它可能会产生更多开销，而将默认处理保留在函数体内部会更简单。

## ES6 属性简写 (Property Shorthands)

如果一个方法接受大型配置对象作为参数，你的代码可能会变得非常大。准备一些变量并将它们添加到该对象中是种常见操作。属性简写（Property shorthands）是让这一步更短、更具可读性的语法糖：

```javascript
const a = 'foo', b = 42, c = function () {};

// 以前我们这样使用这些常量。

const alphabet = {
  a: a,
  b: b,
  c: c
};
// 但有了新的简写，我们现在实际上可以这样做，
// 它等同于上面的代码。

const alphabet = { a, b, c };
```

## 简化你的 API

好的，回到另一个更常见的例子。以下函数接收一些数据，对其进行修改并调用另一个方法：

```javascript
function updateSomething(data = {}) {
  const target = data.target;
  const veryLongProperty = data.veryLongProperty;
  let willChange = data.willChange;

  if (willChange === 'unwantedValue') {
    willChange = 'wayBetter';
  }

  // 我们可以使用解构来处理
  updateSomewhereElse({
    target,
    veryLongProperty,
    willChange
  });
}
```

现在让我们使用解构和默认值来让代码更简洁：

```javascript
function updateSomething({
  target,
  veryLongProperty,
  willChange
} = {}) {
  if (willChange === 'unwantedValue') {
    willChange = 'wayBetter';
  }

  updateSomewhereElse({
    target,
    veryLongProperty,
    willChange
  });
}
```

通过这种方式，我们减少了冗余变量赋值，代码变得更加清晰。

考虑到预算，你实际上只有 8–10ms 的时间来完成所有工作，其余时间会被浏览器内部机制和其他变量所占用。

## 空闲工作 (Idle work)

如果你有一个昂贵且持续运行的任务，请确保将其切分成更小的块，以允许主线程响应用户输入。你不应该拥有一个延迟用户输入超过 50ms 的任务。

## 加载 (Load)

你的目标应该是页面加载时间在 1000ms 以内。超过这个时间，你的用户就会开始焦虑。在移动设备上这是一个很难实现的目标，因为它涉及到页面的可交互性，而不仅仅是渲染在屏幕上并滚动。在实践中，目标是：

### 我们1000 毫秒预算的（短）寿命

在实践中，针对5秒的交互时间（time-to-interactive）。这是 Chrome 在 Lighthouse 审计中使用的标准。

现在我们已经知道了这些指标，让我们来看一些统计数据：

- 如果移动端网站加载超过三秒，53%的访问将会放弃。
- 每2个人中就有1个人期望页面加载在2秒内完成。
- 在3G网络上，77%的移动端网站加载时间超过10秒。
- 移动端网站在3G网络上的平均加载时间为19秒。

感谢 Addy Osmani 提供的更多信息：

- 应用程序在桌面设备上（使用电缆）需要8秒变得可交互，在移动端（通过3G连接的Moto G4）需要16秒。
- 在中位数水平，开发者为其页面交付了410KB的经过 gzip 压缩的 JS。

感到足够沮丧了吗？很好。让我们开始工作并修复 Web。

## 上下决定一切 (Context is Everything)

你可能已经注意到主要的瓶颈是加载网站的时间。具体来说，就是 JavaScript 的下载、解析、编译和执行时间。除此之外没有办法，只能加载更少的 JavaScript 并以更智能的方式加载。

但是除了启动网站之外，你的代码执行的实际工作呢？那里应该会有一些性能提升，对吧？

在深入优化代码之前，请考虑你正在构建什么。你是在构建一个框架还是 VDOM 库吗？你的代码需要每秒执行数千次操作吗？你正在编写一个处理用户输入和/或动画的时间关键库吗？如果不是，你可能希望将时间和精力转移到更有影响力的地方。

并不是说编写高性能的代码不重要，但从宏观来看，它通常产生很小的影响，特别是在谈论微优化（microoptimizations）时。所以，在你通过 JSPerf.com 比较结果陷入关于 `.map` vs `.forEach` vs `for` 循环的 Stack Overflow 争论之前，请确保看到的是森林而不仅仅是树木。在纸面上，50k ops/s 听起来比 1k ops/s 快50倍，但在大多数情况下并无区别。

## 解析、编译和执行 (Parsing, Compiling and Executing)

从根本上说，大多数性能不佳的 JS 问题不在于运行本身，而在于代码开始执行之前必须采取的所有步骤。

我们在这里讨论的是抽象层级。你电脑中的 CPU 运行的是机器码。你在电脑上运行的大多数代码都是编译后的二进制格式。（我用“代码”而不是“程序”，考虑到现在所有的 Electron 应用。）这意味着，抛开所有操作系统层面的抽象，它在你的硬件上原生运行，不需要任何准备工作。

JavaScript 不是预编译的。它通过（相对缓慢的网络）以可读代码的形式到达你的浏览器，而对于所有意图来说，浏览器就是你 JS 程序的“操作系统”。

这些代码首先需要被解析 --- 即被读取并转换为计算机可以索引的结构，以便用于编译。然后，它被编译成字节码，最后编译成机器码，然后由你的设备/浏览器执行。

另一个非常需要说明的一点是，JavaScript 是单线程的，运行在浏览器的主线程上。这意味着一次只能运行一个进程。如果你的 DevTools 时间轴布满了黄色峰值，导致 CPU 运行率为 100%，你将会遇到长帧/掉帧、卡顿滚动以及所有其他糟糕的问题。

它生成的生成。如果你使用 `commonChunks` 插件，可以使用以下代码将运行时（runtime）提取到自己的 chunk 中：

```javascript
new webpack.optimize.CommonsChunkPlugin({
  name: 'runtime',
});
```

它会将运行时从你所有的其他 chunk 中提取并放入自己的文件中，在此例中名为 `runtime.js`。只需确保在加载主 JS 包之前加载它。例如：

```html
<script src="runtime.js">
<script src="main-bundle.js">
```

然后是转译代码和填充程序（polyfills）的话。如果你正在编写现代（ES6+）JavaScript，你可能正在使用 Babel 将其转译为兼容 ES5 的代码。转译不仅因为冗冗性增加了文件大小，还增加了复杂性，而且与原生 ES6+ 代码相比，它通常会有性能退化。

此外，你可能还在使用 `babel-polyfill` 包和 `whatwg-fetch` 来修补旧版浏览器中缺失的功能。然后，如果你编写代码时使用了 `async/await`，你还需要使用生成器（generators）对其进行转译，这需要包含 `regenerator-runtime`……

要点是，你向 JS 包中增加了近 100KB，这不仅导致了巨大的文件体积，还有巨大的解析和执行成本，仅仅是为了支持旧版浏览器。

然而，惩罚使用现代浏览器的用户是没有意义的。我的一种方法（Philip 在这篇文章中也提到）是创建两个独立的包并根据条件加载它们。Babel 通过 `babel-preset-env` 让这变得简单。例如，你有一个支持 IE 11 的包，另一个是不带填充程序的适用于最新现代浏览器的包。

一种粗暴但高效的方法是将以下内容放在内联脚本中：

```javascript
function() {
  try {
    new Function('async () => {}}');
  } catch (error) {
    // 创建指向 legacy-bundle.js 的 script 标签；
    return;
  }
  // 创建指向 modern-bundle.js 的 script 标签；
}}();
```

如果浏览器无法评估异步函数，我们假设它是旧浏览器，并直接发送带填充程序的包。否则，用户将获得整洁且现代的版本。

## 结论

我们希望你从这篇文章获得的收获是JS 是昂贵的，应该节约使用。

确保在低端设备和真实网络条件下测试你网站的性能。你的网站应该快速加载并尽快实现可交互。这意味着通过任何必要手段发送更少的 JS，并更快地发送。你的代码应该始终经过压缩，拆分成更小的、易于维护的包，并尽可能地异步加载。在服务器端，确保已启用 HTTP/2 以实现更快的并行传输，并使用 gzip/Brotli 压缩来大幅减小 JS 的传输大小。

# 第4 章：JavaScript 设计模式：单例

作者 Samier Saeed

在本章中，我们将深入探讨在 JavaScript 中实现单例的最佳方法，观察它如何随着 ES6 的兴起而演变。

在广泛用于生产的语言中，JavaScript 的进化速度是最快的，它看起来不像早期的迭代，而更像 Python，随着 ECMA International 提出的每一项新规范。虽然这些变化也有许多反对者，但新的 JavaScript 确实成功地让代码更易阅读和推理，更容易以符合软件工程最佳实践（特别是模块化概念和 SOLID 原则）的方式编写，并且更容易组装成标准的软件设计模式。

## 解释 ES6

ES6（又称 ES2015）自2009年 ES5 标准化以来该语言的首次重大更新。几乎所有现代浏览器都支持 ES6。然而，如果你需要兼容旧版浏览器，可以使用 Babel 等工具将 ES6 代码轻松转译为 ES5。ES6 为 JavaScript 提供了许多新功能，包括更优的类语法和用于变量声明的新关键字。你可以通过阅读 SitePoint 上关于该主题的文章来了解更多。

## 什么是单例

如果你不熟悉单例模式，它本质上是一种限制类实例化为单个对象的的设计模式。通常，目标是管理全局应用程序状态。我见过或自己编写过的一些示例包括：使用单例作为 Web 应用配置设置的源；在客户端处理任何通过 API 密钥启动的操作（例如，你通常不想承担发送多次分析跟踪调用的风险），以及在客户端 Web 应用程序中内存中存储数据（例如 Flux 中的 stores）。

单例对于调用代码来说应该是不可变的，并且不应该存在实例化多个单例的危险。

> **单例坏的吗？**
>
> 在某些情况下，单例可能是坏的，也有观点认为它们实际上总是坏的。关于这个讨论，你可以查看这篇关于该主题的有用文章。

## 在 JavaScript 中创建单例的旧方法

在 JavaScript 中编写单例的旧方法涉及利用闭包和立即调用函数表达式（IIFE）。以下是我们可能如何为一个假设的 Flux 实现编写一个（非常简单的）store：

```javascript
var UserStore = (function(){
  var data = [];
  function add(item){
    data.push(item);
  }
  function get(id){
    return data.find((d) => {
      return d.id === id;
    });
  }
  return { add: add, get: get };
})();
```

代码被解释时，`UserStore` 将设置为立即调用函数的结果——一个允许访问数据的对象。但是，由于对象是不可变的，无法对其进行更改或添加。但这种方法比需要的冗长，而且我们的示例简单到看不到类的优势。此外，有时你可能希望利用类的优势。

## 新方法（们）

通过利用 ES6 特性，我们可以以简洁且强大的方式编写单例。让我们从最基础的实现开始：

```javascript
const data = [];
const UserStore = {
  add: item => data.push(item),
  get: id => data.find(d => d.id === id)
};

Object.freeze(UserStore);
export default UserStore;
```

你可以看到，这提供了改进。但从技术上说，使用这两种模式的单例不可变性和不可覆盖性可以被有心的挑衅者破坏。对象字面量即使是 `const` 也可以通过 `Object.assign` 进行拷贝。当我们导出类的实例时，虽然我们没有直接将其暴露给调用代码，但任何实例的构造函数在 JavaScript 中都是可用的并可以被调用创建新实例。显然，这至少需要一些努力，希望你的同事在违反单例模式方面不要如此。

假设你想额外确保没人破坏你单例的唯一性，而且你还想更贴近面向对象世界中单例的实现。这是你可以这样做：

```javascript
class UserStore {
  constructor() {
    this._data = [];
  }

  add(item){
    this._data.push(item);
  }

  get(id){
    return this._data.find(d => d.id === id);
  }
}

const instance = new UserStore();
Object.freeze(instance);

export default instance;
```

```javascript
if (!UserStore.instance) {
  this._data = [];
  UserStore.instance = this;
}

  return UserStore.instance;
}

// rest is the same code as preceding example
}
const instance = new UserStore();
Object.freeze(instance);

export default instance;
```

通过增加持有实例引用的额外步骤，我们可以检查是否已经实例化了 `UserStore`，如果已经存在，就不会创建一个新的。如你所见，这也充分利用了我们将 `UserStore` 设为类的这一事实。

## 结论

毫无疑问，许多开发者多年一直在 JavaScript 中使用旧的单例/模块模式，并且他们发现这种模式对他们非常有效。尽管如此，由于寻找解决问题的方法是开发者精神的核心，我们希望能看到像这种这样更简洁、更易理解的模式获得越来越多的关注。特别是在利用 ES6+ 特性变得更加容易和普遍之后。

# 第 5 章：JavaScript 对象创建：模式与最佳实践

作者 Jeff Mott

在本章中，我将带你游览 JavaScript 创建对象的各种风格，以及每种风格如何通过渐进的步骤在其他风格的基础上进行构建。

JavaScript 有许多创建对象的风格，新手和老手都可能对这些选择感到不知所措，并且不确定应该使用哪一种。但尽管种类多样且每种风格的语法看起来完全不同，但它们比你想象的要相似得多。

## 对象字面量 (Object Literals)

我们之旅的第一站是 JavaScript 创建对象最简单的方法——对象字面量。JavaScript 宣称对象可以“无中生有”——没有类、没有模板、没有原型——砰的一声，一个带有方法和数据的对象出现了：

```javascript
var o = {
  x: 42,
  y: 3.14,
  f: function() {},
  g: function() {}
};
```

但也有缺点。如果我们需要在其他地方创建相同类型的对象，就会不断复制对象的方法、数据和初始化代码。我们需要一种方法，不仅仅创建一个对象，而是创建一组对象。

## 工厂函数 (Factory Functions)

JavaScript 对象创建之旅的下一站是工厂函数。这是创建一组共享相同结构、接口和实现的对象的绝对最简单的方法。我们不是直接创建对象字面量，而是从函数返回一个对象字面量。这样，如果我们需要多次或在多个地方创建相同类型的对象，只需要调用它即可：

```javascript
function thing() {
  return {
    x: 42,
    y: 3.14,
    f: function() {},
    g: function() {}
  };
}

var o = thing();
```

但也有缺点。这种 JavaScript 对象创建方法会导致内存膨胀，因为每个对象都包含每个函数的唯一拷贝。理想情况下，我们希望每个对象都只共享一份函数拷贝。

## 原型链 (Prototype Chains)

JavaScript 为我们提供了一种跨对象共享数据的内置机制，称为原型链。当我们访问对象上的属性时，它可以通过委托给其他对象来完成该请求。我们可以利用这一点并修改工厂函数，使得每个对象只创建该特定对象特的数据，并将所有其他属性请求委托给单一的共享对象：

```javascript
var thingPrototype = {
  f: function() {},
  g: function() {}
};

function thing() {
  var o = Object.create(thingPrototype);
  o.x = 42;
  o.y = 3.14;
  return o;
}

var o = thing();
```

事实上，这种模式非常常见，以至于语言对其提供了内置支持。我们不需要创建自己的共享对象（原型对象）。相反，语言会为每个函数都自动创建一个原型对象，我们可以将共享数据放在那里：

```javascript
thing.prototype.f = function() {};
thing.prototype.g = function() {};

function thing() {
  var o = Object.create(thing.prototype);
  o.x = 42;
  o.y = 3.14;
  return o;
}

var o = thing();
```

但也有缺点。这种 JavaScript 对象创建方法会导致内存膨胀，因为每个对象都包含每个函数的唯一拷贝。理想情况下，我们希望每个对象都只共享一份函数拷贝。

## ES6 类 (ES6 Classes)

JavaScript 较新引入的是类，它为以下内容提供了显著清晰的语法：

```javascript
class Thing {
  constructor() {
    this.x = 42;
    this.y = 3.14;
  }

  f() {}
  g() {}
}

const o = new Thing();
```

# 可以赖以的坚实基础

我不认识任何一个会对如今 JavaScript 的现状感到困惑的人，无论你是 JavaScript 新手，还是已经用它写了一段时间代码。如此多的新框架，如此多的语言变化，还有这么多需要考虑的上下文。在我们每个月都要学习这么多新东西的情况下，大家还能完成工作，这简直是个奇迹。

我相信，使用任何编程语言成功的秘诀——无论应用多么复杂——都是回到回归基础。如果你想理解 Rails，请从提高你的 Ruby 技能开始；如果你想在带有 webpack（或无论那些酷炫的极客们最近在忙什么）的同构 React 中使用不可变数据和单向数据流，请从掌握你的核心 JavaScript 开始。

理解语言本身是如何运作的，比熟悉最新的框架和环境要实用得多。那些东西变化比天气还快。而且对于 JavaScript，我们在网上有长期关于 JavaScript 如何被创建以及如何有效地使用它的详尽且经过熟虑的信息。

问题是，JavaScript 最新版本中引入的一些新技术使得一些旧规则过时了。但并非所有规则都如此！有时，新语法可能会取代笨拙的语法来完成相同的任务。而在其他时候，新方法似乎可能是我们以前处理方式的更简单替代品，但之间存在细微的差别，意识到这些差异是非常关重要的。

## 一勺语法糖衣

近年来 JavaScript 的许多变化被描述为现有语法的“语法糖衣”。在很多情况下，这些语法糖衣可以帮助学习如何操作 JavaScript 的 Java 程序员更容易“药下口”，或者对于我们这些只想用更整洁、更简单的方法来完成已经学会的事情的人来说。其他变化似乎引入了神奇的新功能。

但如果你尝试用现代语法来重现一个熟悉的旧技术，或者在不理解其实际行为的情况下就直接套用，你可能会面临以下风险：

- 导致原本运行良好的代码出现问题
- 引入在运行时可能在你最意想不到的情况下出手的细微错误
- 创建出在它最意想不到的情况下静默失败的代码。

事实上，几项看起来是现有技术替代品的变化，其实行为与它们声称要替换的代码不同。在许多情况下，使用原始的、旧的风格来实现你正在尝试的事情可能更有意义。意识到这种情况何时会发生，并知道如何做出选择，对于编写有效的 JavaScript 至关重要。

## 当你的 const 不一致时

现代 JavaScript 引入两个关键字 `let` 和 `const`，它们在大多数情况下有效地取代了声明变量时对 `var` 的需求。它们的行为与 `var`并不相同。

在传统的 JavaScript 中，在使用变量之前用 `var` 关键字声明变量始终是一种良好的编码实践。不这样做意味着你声明的变量可以被在相同上下文中运行的任何脚本在全局作用范围内访问。由于传统的 JavaScript 经常运行在可能加载多个脚本的网页上，这意味着在一个脚本中声明的变量可能会泄漏到另一个脚本中。

现代 JavaScript 中 `var` 最干净的直接替代品是 `let`。但 `let` 有一些与 `var` 不同的特殊之处。使用 `var` 声明的变量总是被提升到其所在作用域的顶部，无论它们位于作用域内的什么位置。这意味着即使是深度嵌套的变量，从作用域开始就可以被视为已声明并可用。`let` 或 `const` 则并非如此。

```javascript
console.log(usingVar); // undefined
var usingVar = "defined";
console.log(usingVar); // "defined"

console.log(usingLet); // error
let usingLet = "defined"; // 永远不会执行
console.log(usingLet); // 永远不会执行
```

当你使用 `let` 或 `const` 声明变量时，该变量的作用域被限制在定义它的局部块（block）。JavaScript 中的块由一组大括号 `{}` 区分，例如函数体或循环内部的可执行代码。

这对于迭代器和循环等变量的块作用域使用来说是一个极大的便利。以前，在循环内部声明的变量在包含作用域中可用，这导致当多个计数器使用相同的变量名时可能会产生潜在的困惑。然而，如果你期望在脚本某个块内部声明的变量在其他地方可用，`let` 可能会让你感到意外。

```javascript
for (var count = 0; count < 5; count++) {
  console.log(count);
} // 向控制台输出数字 0 - 4
console.log(count); // 5
```

## 限制函数的作用域

使用 `function` 关键字定义的传统函数可以被调用执行语句，并可选返回一个值：

```javascript
function doSomething(param) {
  return `Hello ${param}`;
}
console.log(doSomething("World")); // "Hello World"
```

它们也可以与 `new` 关键字一起使用构造对象，并且定义可以放在作用域内的任何地方：

```javascript
function Animal(name) {
  this.name = name;
}
let cat = new Animal("Fluffy");
console.log(cat.name); // "My cat's name is Fluffy"
```

以这两种方式使用的函数可以在调用之前或之后定义。这对 JavaScript 来说没有区别。

```javascript
console.log(doSomething("World")); // "Hello World"

let cat = new Animal("Fluffy");
console.log(cat.name); // "My cat's name is Fluffy"
```

## 按时到达类

函数的一部分已被 `class` 关键字接管。这允许程序员选择倾向于使用可调用箭头函数遵循函数式编程范式，还是使用类这种更面向对象的方法代替传统函数的原型继承。

在 JavaScript 中进行面向对象编程时，函数和类的一个区别是，JavaScript 中的类需要前向声明，就像在 C++ 中一样（但不像 Java 中那样）。也就是说，在类使用 `new` 关键字实例化之前，必须在脚本中声明该类。

在 JavaScript 中，使用 `function` 关键字进行原型继承即使在脚本中后后定义也能正常工作，因为函数声明会被自动提升到顶部，而 `class` 并不会这样。

```javascript
// 使用函数声明并实例化对象（已提升）
let aProto = new Proto("Myra"); aProto.greet(); // "Hi Myra"

function Proto(name) {
  this.name = name;
  this.greet = function() {
    console.log(`Hi ${this.name}`); 
  };
}

// 使用类声明并实例化对象（未提升）
class Classy {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hi ${this.name}`);
  }
}
let aClass = new Classy("Sonja"); aClass.greet(); // "Hi Sonja"
```

## 与箭头函数的区别

传统函数的其他方面现在可以使用箭头函数来访问，这种新语法允许你更简洁地编写可调用函数，以便更整齐地嵌套在回调函数中。事实上，箭头函数最简单的语法是完全省略大括号的单行代码，并且它会自动返回所执行语句的结果：

```javascript
function traditional(data) {
  return (`data} from a traditional function`);
}

const arrow = data => `${data} from an arrow function`;
console.log(traditional("Hi")); // "Hi from a traditional function"
console.log(arrow("Hi")); // "Hi from an arrow function"
```

箭头函数封装了几个使其变得更方便的特性，并省略了其他在调用函数时不实用的行为。它们并不是功能更强大的传统 `function` 关键字的无缝替代品。

例如，箭头函数会从调用它的上下文继承 `this` 和 `arguments`。这对于事件处理或 `setTimeout` 等情况非常有用，因为程序员经常希望被调用的行为应用于请求它时的上下文中。传统函数迫使程序员编写复杂的代码，通过使用 `.bind(this)` 将函数绑定到现有的函数上。使用箭头函数时这些都不需要了。

```javascript
class GreeterTraditional {
  constructor() {
    this.name = "Joe";
  }

  greet() {
    setTimeout(function () {
      console.log(`Hello ${this.name}`);
    }, 1000); // 内部函数有自己的 this，没有名字
  }
}

let greeterTraditional = new GreeterTraditional();
greeterTraditional.greet(); // "Hello "

class GreeterBound {
  constructor() {
    this.name = "Steven";
  }

  greet() {
    setTimeout(function () {
      console.log(`Hello ${this.name}`);
    }.bind(this), 1000); // 从外部上下文传递 this
  }
}

let greeterBound = new GreeterBound(); // "Hello Steven"
greeterBound.greet();

class GreeterArrow {
  constructor() {
    this.name = "Ravi";
  }

  greet() {
    setTimeout(() => {
      console.log(`Hello ${this.name}`);
    }, 1000); // 箭头函数默认继承 this
  }
}

let greeterArrow = new GreeterArrow();
greeterArrow.greet(); // "Hello Ravi"
```

## 理解你所获得的内容

这不仅仅是语法糖。JavaScript 引入的许多新变化是因为需要新功能。但这并不意味着 JavaScript 传统语法的旧原因已经消失了。继续使用传统的 JavaScript 语法通常是有意义的，有时使用新语法可以让你你的代码写得更快、更易理解。

检查一下你正在学习的在线教程。如果作者使用 `var` 初始化所有变量，忽略 `class` 而倾向于使用原型继承，或者在回调函数中依赖函数语句，那么你可以预期的其余语法将基于旧的、传统的 JavaScript。对于今天来说，从 JavaScript 一直以来教学和使用的传统方式中，我们仍然有许多可以学习和应用的内容。但如果你在初始化中看到 `let` 和 `const`，在回调中看到箭头函数，并将 `class` 作为面向对象模式的基础，那么你可能也会在示例中看到其他现代 JavaScript 代码。

现代 JavaScript 的最佳实践是关注语言实际上在做什么。取决于你的习惯，这并不总是显而易见的。但请思考你写的代码试图实现什么，你将在哪里部署它，以及下一个修改它的人是谁。然后自己决定什么是最佳方法。

# 第7 章：现代 JS 中的流程控制：从回调到 Promise 再到 Async/Await

作者 Craig Buckler

JavaScript 经常被称为是*异步*的。这意味着什么？它如何影响开发？近年来这种方法发生了怎样的变化？

考虑以下代码：

```javascript
result1 = doSomething1();
result2 = doSomething2(result1);
```

大多数语言*同步*地处理每一行。第一行运行并返回结果。第二行在第一行完成后运行，*无论它需要多长时间*。

## 单线程处理

JavaScript 运行在单个处理线程上。在浏览器标签页中执行时，其他所有操作都会停止。这是必要的，因为对页面 DOM 的更改不能并行发生。这对用户来说很少明显，因为处理是以小分块进行的。例如，JavaScript 检测到按钮点击、运行计算并更新 DOM。

## 其他语言

PHP 等其他语言也使用单线程，但可能由多线程服务器实例管理。同时对同一个 PHP 页面的两个请求可以启动

## 使用回调实现异步

单线程引发了一个问题。当 JavaScript 调用“慢”过程（如浏览器中的 Ajax 请求或服务器上的数据库操作）时会发生什么？该操作可能需要几秒甚至几分钟。浏览器将在等待响应时被锁定。

解决方案是异步处理。与其等待完成，处理方法是在结果准备绪时调用另一个函数。这被称为回调（callback），它被作为参数传递给任何异步函数。例如：

```javascript
doSomethingAsync(callback1);
console.log('finished'); // 当 doSomethingAsync 完成时调用

function callback1(error) {
  if (!error) console.log('doSomethingAsync complete');
}
```

`doSomethingAsync()` 接受一个回调函数作为参数（仅传递该函数的引用，因此开销很小）。`doSomethingAsync()` 需要多长时间并不重要；我们只知道 `callback1()` 将在未来的某个时刻执行。控制台将显示：finished doSomethingAsync complete

## 回调地狱

通常，回调只会被一个异步函数调用。因此可以使用简洁的匿名内联函数：

```javascript
doSomethingAsync(error => {
  if (!error) console.log('doSomethingAsync complete');
});
```

两个或多个异步调用可以通过嵌套回调函数来顺序完成。例如：

```javascript
async1(err, res => {
  if (!err) async2(res, err, res) => {
    if (!err) async3(res, err, res) => {
      console.log('async1, async2, async3 complete.');
    }
  }
});
```

不幸的是，这引入了**回调地狱**（callback hell）——一个臭名昭著的概念甚至有自己的网页（https://en.wikipedia.org/wiki/Callback_hell）！代码难以阅读，在添加错误处理逻辑后会变得糟糕。

回调地狱在客户端编码中相对罕见。如果你在进行 Ajax 调用、更新 DOM 并等待动画完成，可能会达到两三层，但通常仍然可控。

在操作系统或服务器进程上情况不同。Node.js API 调用可以在发送响应之前，接收文件上传、更新多个数据库表、写入日志并进行进一步的 API 调用。

## Promises (承诺)

ES2015 (ES6) 引入了 Promises。虽然底层仍然在使用回调函数，但 Promises 提供了一种更清晰的语法来*链式调用异步命令使其按顺序执行（更多信息请见下一节）。*

为了启用基于 Promise 的执行，必须对基于回调的异步函数进行修改，以便它们立即返回一个 Promise 对象。该对象承诺在未来的某个时刻执行两个函数之一（作为参数传递）：

- *resolve*：当处理成功完成时执行的回调函数，以及——
- *reject*：当发生失败时执行的可选回调函数。

在下例中，一个数据库 API 提供了一个接受回调函数的 `connect()` 方法。外层的 `asyncDBconnect()` 函数会立即返回一个新的 Promise，并在连接建立或失败后运行 `resolve()` 或 `reject()`：

```javascript
const db = require('database');

// connect to database 连接数据库
function asyncDBconnect(param) {

  return new Promise((resolve, reject) => {
    db.connect(param, (err, connection) => {
      if (err) reject(err);
      else resolve(connection);
    });
  });
};
```

Node.js 8.0+ 提供了 `util.promisify` 工具，可以将基于回调的函数转换为基于 Promise 的替代方案。需要满足两个条件：

1. 回调必须作为最后一个参数传递给异步函数，并且
2. 回调函数必须期望一个错误参数后接值参数。

示例：

```javascript
// Node.js: promisify fs.readFile
const
  util = require('util'),
  fs = require('fs'),
  readFileAsync = util.promisify(fs.readFile)

readFileAsync('file.txt');
```

各种客户端库也提供了 `promisify` 选项，但你可以自己用几行代码创建一个：

```javascript
// 将作为最后一个参数的回调函数 Promise化
//回调函数必须接受 (err, data) 参数
function promisify(fn) {
  return function() {
    return new Promise(
      (resolve, reject) => fn(
        ...Array.from(arguments),
        (err, data) => err ? reject(err) : resolve(data)
      )
    );
  };
}

// 示例
function wait(time, callback) {
  setTimeout(() => callback(null, 'done'), time);
}

const asyncwait = promisify(wait);
asyncwait(1000);
```

## 异步链式 (Asynchronous Chaining)

任何返回 Promise 的内容都可以开始在 `.then()` 方法中定义的系列异步函数调用。每个调用都会接收来自上一个 `resolve` 的结果：

```javascript
asyncDBconnect('http://localhost:1234')
  .then(asyncGetSession) // 传递 asyncDBconnect 的结果
  .then(asyncGetUser) // 传递 asyncGetSession 的结果
  .then(asyncLogAccess) // 传递 asyncGetUser 的结果
  .then((result) => { // 非异步函数
    console.log('complete'); // (传递 asyncLogAccess 的结果)
    return result; // (传递给下一个 .then() 的结果)
  }).catch((err) => { // 在任何 reject 时调用
    console.log('error', err);
  });
```

同步函数可以在 `.then()` 块中执行。返回值会被传递给下一个 `.then()`（如果有）。

`.catch()` 方法定义了当任何之前的 `reject` 触发时被调用的函数。在此之后，将不再有后续的 `.then()` 方法运行。你可以在整个链中使用多个 `.catch()` 方法来捕获不同的错误。

ES2018 引入了 `.finally()` 方法，无论结果如何都会执行任何最终逻辑——例如清理工作、关闭数据库连接等。它目前在 Chrome 和 Firefox 中支持，但技术委员会 39（TC39）发布了 `.finally()` 的填充程序（polyfill）。

```javascript
function doSomething() {
    doSomething(1)
    .then(doSomething2)
    .then(doSomething3)
    .catch((err) => {
        console.log(err);
    })
    .finally(() => {
        // 在此处清理！
    })
}
```

## 使用 Promise.all 进行多次异步调用

Promise `.then()` 接一个地执行异步函数。如果顺序不重要——例如初始化不相关的组件——那么同时启动所有异步函数并在最后一个（最慢的）函数 `resolve` 时完成会更快。

这可以通过 `Promise.all()` 实现。它接受一个函数数组并返回另一个 Promise。例如：

```javascript
Promise.all([ async1, async2, async3 ])
.then(values => {      // 已 resolve 值的数组
  console.log(values);      // (顺序与函数数组相同)
  return values;
})
.catch(err => {      // 在任何 reject 时调用
  console.log('error', err);
});
```

如果任何一个异步函数调用 `reject`，`Promise.all()` 将立即终止。

## 使用 Promise.race 进行多次异步调用

`Promise.race()` 与 `Promise.all()` 类似，不同之处在于它会在第一个 Promise resolve 或 reject 时立即变为 resolve 或 reject。最快的基于 Promise 的异步函数将完成：

```javascript
Promise.race([ async1, async2, async3 ])
.then(value => {      // 单个值
  console.log(value);
  return value;
})
.catch(err => {      // 在任何 reject 时调用
  console.log('error', err);
});
```

这行不起作用。这样做也不行：

```javascript
async function process(array) {
  array.forEach(async i => {
    await doSomething(i);
  });
}
```

循环本身仍然是同步的，并且始终会在其内部异步操作之前完成。

ES2018 引入了异步迭代器，它们与普通迭代器相似，但 `next()` 方法返回的是一个 Promise。因此，可以使用 `await` 关键字配合 `...of` 来顺序串行执行异步操作，例如：

```javascript
async function process(array) {
  for await (let i of array) {
    doSomething(i);
  }
}
```

然而，在异步迭代器实现之前，最好的可能是将数组项映射到异步函数并使用 `Promise.all()` 运行它们。例如：

```javascript
const todo = ['a', 'b', 'c'],
alltodo = todo.map(async (v, i) => {
  console.log('iteration', i);
  await processSomething(v);
});

await Promise.all(alltodo);
```

这种方法的好处是可以并行运行任务，但无法将某次迭代的结果传递给另一次，而且映射大型数组可能会产生计算开销。

## try/catch 的糟糕性

如果你在任何失败的 `await` 周围省略了 `try/catch`，异步函数将静默退出。如果你有一组长的异步 `await` 命令，可能需要多个 `try/catch` 块。

另一种方案是使用高阶函数，它可以捕获错误，使得 `try/catch` 块变得不再必要（感谢 @wesbos 的建议）：

```javascript
async function connect() {
  const connection = await asyncDBconnect('http://localhost:1234'),
    session = await asyncGetSession(connection),
    user = await asyncGetUser(session),
    log = await asyncLogAccess(user);

  return true;
}

// 用于捕捉错误的高阶函数
function catchErrors(fn) {
  return function (...args) {
    return fn(...args).catch(err => {
      console.log('ERROR', err);
    });
  }
}

(async () => {
  await catchErrors(connect());
})();
```

然而，在应用程序必须以不同于其他方式响应某些错误的情况下，这种方案可能并不实用。

尽管存在一些陷阱，`async/await` 仍 JavaScript 一个优雅的补充。更多资源：

- MDN async and await
- Async functions - making promises friendly
- TC39 Async Functions specification
- Simplifying Asynchronous Coding with Async Functions

## JavaScript 之旅程

异步编程是 JavaScript 中无法避免的挑战。回调函数（Callbacks）在大多数应用程序中都是必不可少的，但很容易陷入深度嵌套函数的泥潭。

Promises 抽象了回调，但存在许多语法陷阱。转换现有函数可能是一项苦差，而且 `.then()` 链看起来仍然很混乱。

幸运的是，`async/await` 带来了清晰。代码看起来是同步的，但它不会独占单个处理线程。它将改变你编写 JavaScript 的方式，甚至可能让你欣赏 Promises——如果你以前还没有的话！

# 第 8 章：JavaScript 的新私有类字段以及如何使用

作者：Craig Buckler

ES6 为 JavaScript 引入了类（classes），但对于复杂应用来说它们太简单了。类字段（也称为类属性）旨在提供带有私有和静态成员的更简单的构造函数。该提案目前处于 TC39 第 3 阶段：候选阶段，可能会出现在 ES2019 (ES10) 中。

在更详细检查类字段之前，快速回顾 ES6 类是有有用的。

## ES6 类基础

JavaScript 的原型继承模型对于那些理解如 C++、C#、Java 和 PHP 等语言中经典继承的开发者来说，可能看起来非常令人困惑。JavaScript 的类主要是语法糖，但它们提供了熟悉的面向对象编程概念。

类是一个模板，定义了该类型对象的行为。接下来的 `Animal` 类定义了通用动物（类通常以大写字母开头，以区分于对象和其他类型）：

```javascript
class Animal {
  constructor(name = 'anonymous', legs = 4, noise = 'nothing') {
    this.type = 'animal';
    this.name = name;
    this.legs = legs;
    this.noise = noise;
  }

  speak() {
    console.log(`${this.name} says "${this.noise}"`);
  }

  walk() {
    console.log(`${this.name} walks on...`);
  }
}
```

## ESnext 类字段

类字段提案允许在类的顶部初始化属性：

```javascript
class MyClass {
    a = 1;
    b = 2;

    c = 3;
}
```

初始化器会在任何构造函数运行之前执行（假设仍需要构造函数）。

### 类字段 (Static Class Fields)

类字段允许在类内部声明静态属性。例如：

```javascript
class MyClass {

  x = 1;
  y = 2;

  static z = 3;
}
console.log( MyClass.z ); // 3
```

优雅的 ES5 等效写法：

```javascript
class MyClass {

  constructor() {

    this.x = 1;

    this.y = 2;

  }
}
MyClass.z = 3;

console.log(MyClass.z ); // 3
```

## 私有类字段 (Private Class Fields)

ES6 类中的所有属性默认公共，可以在类外部检查或修改。在上面的 `Animal` 示例中，没有任何机制阻止在不调用 `eats` setter的情况下更改 `food` 属性：

```javascript
class Animal {
  constructor(name = 'anonymous', legs = 4, noise = 'nothing') {

    this.type = 'animal';

    this.name = name;

    this.legs = legs;

    this.noise = noise;
  }

  set eats(food) {

    this.food = food;
  }

  get dinner() {

    return `${this.name} eats ${this.food || 'nothing'} for dinner.`;
  }
}
const rex = new Animal('Rex', 4, 'woof');

rex.eats = 'anything'; // 标准 setter

rex.food = 'tofu'; // 完全绕过了 eats setter

console.log( rex.dinner ); // Rex eats tofu for dinner.
```

其他语言允许声明私有属性。这在 ES6 中是不可行的，尽管开发者可以使用下划线约定 (`_propertyName`)、闭包、符号 (Symbols) 或 WeakMaps 来规避。

在 ESnext 中，私有类字段使用哈希 `#` 前缀定义：

```javascript
class MyClass {

  a = 1; // a 是公共的

  #b = 2; // #b 是私有的

  static #c = 3; // #c 是私有且静态的

  incB() {
    this.#b++;
  }

}
const m = new MyClass();

m.incB(); // 运行正常

m.#b = 0; //  - 类外部无法修改私有属性
```

注意，目前还没有定义私有方法、getter 和 setter的方法，尽管 TC39 阶段 2 建议在名称上使用哈希 `#` 前缀。例如：

```javascript
class MyClass {

  // 私有属性
  #x = 0;

  // 私有方法（只能在类内调用）
  #incX() {
    this.#x++;
  }

  // 私有 setter（只能在类内调用）
  set #setX(x) {
    this.#x = x;
  }

  // 私有 getter（只能在类内调用）
  get #getX() {
    return this.#x;
  }
}
```

## 直接收益：更简洁的 React 代码！

React 组件通常有绑定到 DOM 事件的方法。为了确保这些方法指向组件，必须对每个方法进行相应的绑定。例如：

```javascript
class App extends Component {

  constructor() {
    super();

    state = { count: 0 };

    // 绑定所有方法
    this.incCount = this.incCount.bind(this);
  }

  incCount() {
    this.setState(ps => ({ count: ps.count + 1 }));
  }

  render() {
    return (
      <div>
        <p>{this.state.count}</p>
        <button onClick={this.incCount}>add one</button>
      </div>
    );
  }
}
```

如果将 `incCount` 定义为类字段，则可以使用 ES6 的 `=>` 箭头函数将其设置为函数，这会自动将其绑定到定义对象。`state` 也可以声明为类字段，这样就不需要构造函数：

```javascript
class App extends Component {

  state = { count: 0 };

  incCount = () => {
    this.setState(ps => ({ count: ps.count + 1 }));
  };

  render() {
    return (
      <div>
        <p>{this.state.count}</p>
        <button onClick={this.incCount}>add one</button>
      </div>
    );
  }
}
```

## 今日如何使用类字段

目前浏览器或 Node.js 尚不支持类字段。但是，可以使用 Babel 对语法进行转译，Create React App 默认启用了该功能。或者，可以使用以下终端命令安装并配置 Babel：

`mkdir class-properties && cd class-properties && npm init -y && npm install --save-dev babel-cli babel-plugin-transform-class-properties && echo '{ "plugins": ["transform-class-properties"] }' > .babelrc`

在 `package.json` 的 `scripts` 部分添加构建命令：

`"scripts": { "build": "babel in.js -o out.js" }`

然后运行 `npm run build` 将 ESnext 文件 `in.js` 转译为兼容的 `out.js`。

针对私有方法、getter 和 setter 的 Babel 支持已经提交。

作者和出版者已尽一切努力确保书中信息的准确性。然而，书中所包含的信息按原样出售，不提供任何明示或暗示的保证。作者和 SitePoint Pty. Ltd. 及其代理商或分销商均对因书中包含指令或此处描述的软件或硬件产品而直接或间接造成的任何损害不负责。

并非对每个商标名称的出现进行标注，本书仅以编辑的方式使用这些名称，旨在造商标所有者的利，并无侵犯商标之意。
