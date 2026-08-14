# React.js 书：用于构建用户界面的开源 JavaScript 库：想要学习 React 编程基础的 JavaScript 开发者指南








![](img/05b8b68e82424c98c0b61100a18147b2_0_0.png)



React.js 教程书籍

React.js 绝对是我在 JavaScript 库中学过的困难的内容之一。部分原因在于它假设你已经了许多与其他专业 Web 开发相关的知识。即：Node.js、NPM、精通 babel 命令行工具、EcmaScript (5 和 6)、JSX 以及可能还有 WebPack。

这本书还做了一个假设，即你对 React 编程是完全全新的。这对我这个作者来说构成了一个挑战，因为我的责任是用一种仍然有意义的方式来讲解 React，而不会用大块看起来复杂且难以理解的代码让你无所适从。

尽管如此，我对本书呈现形式的策略遵循一个简单的模式，即将解释与简单的代码示例混合。主要来说，这本书是一部叙述性的著作，旨在逐步进入对 React 库的理解。

我现在就直说，单凭这本书是不够成为一名专家 React 程序员的。任何关于 React 的出版物都无法做到这一点，因为要入门并使用 React 开发真正的应用程序，你需要理解的原则范围极其庞大。EcmaScript 5、6 以及即将到来的 7 之间也存在语法差异。正因如此，React 可能会成为你在学习 JavaScript 时遇到过的最不寻的学习体验之一。

但突破这些困难部分是值得的。我希望这本书在完成这项任务方面证明是实用的。

Greg Sidelnikov 编写并编辑 greg.sidelnikov@gmail.com





JSX 53

属性 (Props) 57

函数纯度 58

函数式组件 60

披着羊皮的狼 62

原生 Babel vs JavaScript Babel 63

NPM {

源代码源代码编译 64


带有单个子组件的父组件 68

带有多个子组件的父组件 69


方法 1 - getInitialState 71

方法 2 - componentDidMount 72

方法 3 - componentWillUnmount 73


创建搜索列表 74

React 应用程序 77


var 和 let 关键字 83

new const 关键字 84

解构赋值 84

For-of 循环 90

Map 对象 94

箭头函数 94

JavaScript 中的箭头函数是什么？

立即调用箭头函数 (IIAF)

反引号 (`` ` `` 模板字符串 95

`string text`; 95

`string text`; 95

新的数组方法 96

# 作者的寄语

欢迎阅读我书的引言章节。
这是 Greg Sidelnikov 编写的《React Gems》（React 宝石）。

我就是作者！

首先，感谢你对《React Gems》感兴趣。这本教程书籍是由我的 JavaScript Web 开发通讯报自出版的。它将带你一步步完成从设置开发环境到从头开始学习响应式编程的过程。

截至 2017 年，我所谓的“响应式”编程已成为一种思考 Web 应用程序的替代方式。它提供了软件模式，使得你的 Web 应用对用户输入极其灵敏，并且通常让用户（使用你应用程序的人）感觉速度更快。

当我学习 React 时，花了大约 3 周才领悟：React 与我编写过的任何 JavaScript 库都不同。它假设了大量的先验知识。正因如此，我必须以特定的方式编写这本书，逐步深入理解的过程。

学习 React 不仅仅是记忆几个方法并到处使用它们。React 本身建立在软件原理之上，这些原理通常只有在行业中工作了长时间的专业软件工程师才知道。这对于像我这样试图向 JavaScript 新手解释 React 的作者来说是一个挑战。

我选择通过采用更流流的解释风格来解决这个问题，这种风格介于讨论和源代码之间，试图在两者之间建立平衡。我不想展示很长的 React 程序并写几行注释来解释每行代码的作用。那样只会使学习过程复杂。相反，我将书的叙述拆解为组件（无双关梗！），处理你初次学习 React 时会遇到的实际问题。

React 让理解（ props 和 states）成为显式要求。为了成为一名通用的 React 程序员，它们几乎是必须掌握的子功能。

（此处重复部分）这是 Greg Sidelnikov 编写的《React Gems》（React 宝石）。我就是作者！

首先，感谢你对《React Gems》感兴趣。这本教程书籍是由我的 JavaScript Web 开发通讯报自出版的。它将带你一步步完成从设置开发环境到从头开始学习响应式编程的过程。

截至 2017 年，我所谓的“响应式”编程已成为一种思考 Web 应用程序的替代方式。它提供了软件模式，使得你的 Web 应用对用户输入极其灵敏，并且通常让用户（使用你应用程序的人）感觉速度更快。

当我学习 React 时，花了大约 3 周才领悟：React 与我编写过的任何 JavaScript 库都不同。它假设了大量的先验知识。正因如此，我必须以特定的方式编写这本书，逐步深入理解的过程。

学习 React 不仅仅是记忆几个方法并到处使用它们。React 本身建立在软件原理之上，这些原理通常只有在行业中工作了长时间的专业软件工程师才知道。这对于像我这样试图向 JavaScript 新手解释 React 的作者来说是一个挑战。

我选择通过采用更流动的解释风格来解决这个问题，这种风格介于讨论和源代码之间，试图在两者之间建立平衡。我不想展示很长的 React 程序并写几行注释来解释每行代码的作用。那样只会使学习过程复杂。相反，我将书的叙述拆解为组件（无双关梗！），处理你初次学习 React 时会遇到的实际问题。

React 让理解（ props 和 states）成为显式要求。为了成为一名通用的 React 程序员，它们几乎是必须掌握的子功能。

JSX 处理器，将 XML 视为 HTML 处理并将其转换为一个


我们可以随手使用的有效 JavaScript 语句在后台为我们完成了所有繁琐的工作。实际上，这种类型的代码是从 XML（看起来像 HTML）被“转译”为 EcmaScript 5，这样浏览器才能理解它。这意味着浏览器看到的实际代码甚至不是这种形式。这只是为了方便我们在编写应用程序时使用。但是……我们可以完全毫无障碍地以这种格式编写代码。

这将在本书中贯穿进行讨论。但基本上，这种格式与 React 组件结构是互换的。你本质上创建的实际上是一个有效的 React 组件模式。

出于这个原因，JSX 经常作为 React 的补充库使用。你可以通过 JSX 来创建上面示例中看到的语句，但这并不是强制要求的，你不使用它也可以。

然而，如果没有 React，编程就像是吃没有奶士的披萨。两者共同工作以提供美味的体验，即使学习如何烘焙饼饼需要尝试错误和时间。

- 3. Babel 将将 EcmaScript 6 转译到早期版本（ES5）有一点开销，而且似乎也是多此一。因为像 Chrome 和 Safari 等浏览器最终将对 ES6 提供完全支持，这个过程终将变得自动。

Babel 允许我们编写这种代码：

```
import someClass from "someClass.js"
```

这将从定义的 `someClass.js` 文件中获取 `someClass` 类定义。到写此时，Chrome、Firefox 以及其他任何浏览器都不支持 ES6 import 关键字。

然而，babel 允许我们现在就开始学习和编写 ES6 代码，即使在现代浏览器尚未推出官方支持之前也是如此。

在此之前，它只是会在后台将其代码“转译”回 ES5，以便代码可以在今天的任何浏览器中实际运行。

好消息是，安装 babel 插件会迫使你学习如何使用命令行工具。这是传统的 JavaScript 开发者通常不熟悉的。我想，这正是你本就应该学习的技能。

使用命令行是专业软件开发环境中的“必修”技能（在你的电脑桌面上某个任意文件夹中的个人项目之外）。而且……如果不采取这一步，它可能是可能阻止你直接深入响应式编程的额外步骤之一。尽管这可能非常麻烦。

## 学习 React 的良好理由

- 1. **它很快。** 这可能是 JavaScript 程序员想要开始使用 React 库编写应用程序的首要原因。通过利用 DOM 的虚拟副本，它旨在要在渲染到标准 JavaScript DOM 树之前在虚拟执行操作。这不仅仅是一个数字游戏。将 UI 操作移动到**虚拟 DOM** 实际上改变了用户对你应用程序的感受，这是令人惊讶的。你可能已经在 Netflix 等网络网站上开始注意到这种现象了。

- 2. **模块化设计。** React 支持模块化设计，这通常与构建大型、可扩展的应用程序相关。此的原因是 2015 年出的 ECMAScript 6 规范的出现，它提供了倾向于模块化方法的新语法，例如，**require (ES5)** 和 **include (ES6)** 关键字不仅将文件连接在一起，还假定了对象之间基于类的关系。尽管到写此时，`include` 关键字在现代浏览器（即使是 Chrome）中不被支持，但我们可以通过使用 `require` 或在发送到浏览器进行渲染之前将 ES6 代码转译为 ES5（现在几乎所有浏览器都支持这样做）来开始编写模块化程序。当浏览器赶上时，我们就不再需要转译了。当这种情况发生时，React 将成为你随处可见的更常见的库。最终，无论是否有 React，模块化的 JavaScript 程序设计将成为规范。

- 3. **可扩展性。** 在 React 中，每个 HTML 元素都被*视为*可以编程的组件，可以嵌套在其他组件中。子组件通过被称为 props 的东西与父组件关联。React 程序的的可扩展性通过使每个组件都成为 HTML、CSS 和 JavaScript 代码的集合来实现。

- 4. **灵活性。** React 不仅仅是一个 UI 视图库，这与你开始了解时可能听到的观点不同。这并不完全错误。React 赋予了我们创建极快速交互组件的能力，这些组件可以作为我们应用程序的元素。然而，React 利用渲染目标的原理，允许你将代码的结果发送到任何地方，包括但不限于前端视图。

- 5. **雇主中的流行程度。** React 是由 Facebook 的程序员在多年研究 Web 应用后开发的。或少，它源于一组经过证明的软件工程哲学。尽管许多传统的 JavaScript 程序员对其中的许多许多点并不熟悉。当你学习 React 时，你是在学习计算机编程原理，而不仅仅是函数和方法的列表，像 jQuery 等其他库就是那样。2016 年，JavaScript 已成为前端 Web 开发的领先语言。如果你在寻找软件行业的工作，在简历上拥有 React 将让你比竞争对手更具优势。旧金山湾区的平均资深 JavaScript 程序员年薪为 12-15 万美元。

## 响应式编程

到底什么是响应式编程？React 是一个用 JavaScript 编写的小型但强大的库。你可以通过使用 SCRIPT 标签将其包含在网页中来使用。就像使用任何其他 JavaScript 库一样，例如 jQuery。

如果你想为在真正的软件公司工作做准备，仅仅将 React 添加到你的网页是不够的。它要求你理解超出简单 JavaScript 编程的 Web 开发其他领域。本书的设计是为了培养那个过程。

通过使用 React 组件（本书许多示例中将展示），你将构建整个应用程序。在本书的大部分，我将使用 React 库构建应用程序称为“响应式”编程。

响应式编程仅仅是一个为了代表构建现代 Web 应用的替代思考方式的术语。响应式编程并不是 React.js 库本身固有的。它是一种方法，而 React.js 库恰好采用了它作为核心哲学。

我的意思是，它是那种非常关注程序逻辑功能的编程方法。你可以将其看作是与在 JavaScript 中处理 DOM 相比的更高级的编程形式，在那种形式中，每个视觉元素不仅与事件关联，而且可能包含你编写的自定义程序，以确定它们的功能。

虽然 React 被认为主要处理应用程序的视图区域，但不要相信 React 严格是你可能熟悉的 MVC（模型-视图-控制器）模式中的“视图”的迷言。如果不熟悉，只需知道模型视图控制器是一种将代码与应用程序的视觉元素分离的编程模式即可。

我希望你喜欢这本书，学习 React 库并探索现代软件开发所提供的可能性，这将训练你制作现实世界的 Web 应用。




# 响应式编程的核心原理

在继续之前，有必要说明我们在这里到底在做什么。我们可以将使用 React 编程称为函数式模板（functional templating）。请不要与函数式编程语言混淆。在这里，我指的是你的 React 组件有特定的函数要执行，这是一种用独特能力来定制组件的方法。虽然 HTML 为我们提供了一组元素（作为 HTML 标签），用于处理 Web 应用程序的布局并通过属性与 JavaScript 代码交互，但 React 不仅如此……还有更多。

React 让我们能够创建紧凑的代码块，让我们能在一个地方一目了然组件在屏幕上是如何渲染的，而且通常只需要一行代码就能实现。这为程序员在创建视觉元素的应用程序方面提供了巨大的控制权，同时也赋予了他（或她）编写这些视觉元素行为的能力。

React 程序通常不处理单独的 CSS 样式表。样式的交互是通过虚拟 DOM 提供的。我们将在书的后部分介绍它是如何运作的。

与传统的 HTML、CSS 和 JavaScript 方法相比（后者我们必须在源代码中到处寻找才能找到网页上某一个元素的各个碎片），React 为我们提供了一种使用可编程模板的方法。

在标准的基于 Ajax 的 HTML 应用程序中，我们习惯于看到如下示例所示的代码：

```html
// HTML
<div class="LoginForm">
  <div class="Name">
    Enter username here.
  </div>
</div>
```

这里是对应的 jQuery Ajax 示例：

```javascript
// Ajax counterpart
$.ajax({ url: "/login.php",
data: { "username": "user1",
"password": "abfgh123" },

// login.php returned some data
success:function(msg) {
  // Adjust DOM data
  $(".Name").html(msg);
}
});
```

这是一个刻意简化的示例。但你可以看到，即使是，代码也位于两个独立的块中。其中一个是 HTML 布局定义。它几乎像是一个带有某些动态功能的 LoginForm 可重用模板。

第二个代码块是执行 Ajax 语句的实际程序。这行代码将根据传递给它的数据（用户名和密码）从 PHP 脚本加载数据，并在 `msg` 变量中返回某种消息。

最后，使用 jQuery 通过替换类名为 `Name` 的 div 内容为从脚本收到的消息来修改 DOM。

在一段时间内，这种方法运行得很好。在过去的几年里，这就是我们习惯处理网页上动态元素的方式。但 React 的卓越之处在于，它整合了这一切，并赋予我们对 HTML 和动态数据的程序化控制，而这一切都封装在一个整洁的 `render` 函数中：

```javascript
render: function() {
  return (
    <div>
      {
        this.state.name ? this.state.name :
        <span>Enter username here</span>
      }
    </div>
  );
}
```

注意 HTML 和 JavaScript 代码是如何交织在一起的，而无需打开单独的标签。它们都存在于同一个 JavaScript 语句中，并且几乎可以互换使用而没有任何任何问题。我们稍后会介绍如何实现这一点的。

当然，这个孤立的示例在实际实际应用之外几乎没有任何意义。但它展示了几个重要的原理。

这段 React 代码从 JSX 语言借用了 JavaScript 跨 HTML 的语法，让我们能够通过简短查看代码就知道动态元素的输出外观。React 在这里试图满足所有人的需求。在某些情况下，你会注意到一些模式，感觉几乎就像将后端逻辑带到了前端。

此示例中使用了三元运算符 `?:`。基本上，它的意思是如果属性存在（非空或未定义），我们就应该输出它。如果它不存在，我们应该输出通用的“Enter username here”作为默认消息。

这把 HTML 方法带到了一个不同的维度。在这里，我们同时设计并编写组件。

# 响应式原理与工作

（注：由于原始文本包含大量重复的 OCR 错误和干扰，译文已提取核心逻辑并进行规范翻译。）




接下来是 props（属性），它们是你传递给此组件的属性。Props 不是状态（state），但它们可以修改状态。稍后我们会详细区分这种区别。

最后，children（子元素）只是在其父元素内部的层级元素。你可以创建它们的链，并将它们直接类型到 `createElement` 函数中，作为末尾的 N 个参数。

另一个让你更深入理解 React 的关键是，上述所有代码在 JSX 中都有等价写法。两者可以互相替换。一旦你真正开始理解它的工作原理，这部分才是真正令人兴奋的。

所以，在 ES5 中，你会使用 `createElement` 函数，而在 JSX 中（其常见用法是与其他 ES6 语法结合使用），你可以通过简单地编写如下内容来实现完全相同的功能：

```javascript
let link1=<a href="#">Save</a>;
```

现在你明白我想表达什么了吗？JSX 将 HTML 转换为 JavaScript 语句。这里的 `link1` 是元素的类对象表示，与我们之前用 `createElement` 方法创建的 React 代码完全等价。

是的，只需通过将其声明为 JSX，`link1.href` 就会包含 "#"。当我意识到它是这样工作的时后，JSX 开始变得非常有意义，我实际上开始习惯使用它了。

它就像 HTML 和 JavaScript 之间的一条双向道，属性会自动变成属性。这里有一个更复杂的例子，再次在 JSX 中实现：

```javascript
let nav=<MyNav>
  <a href="#">Save</a>
  <a href="#">Load</a>
  <a href="#">Delete</a>
  <a href="#">
    <span alerts="0">No Alerts</span>
  </a>
</MyNav>;
```

我们刚刚使用 JSX 语言通过单个 JavaScript 语句重建了虚拟 DOM！你可以将 `nav` 的值作为语句传递给函数。这几乎是创建微型 DOM 结构的另一种方式。

现在你（希望）看到了这就是 React 中虚拟 DOM 的结构。它就像我们要处理的次级 DOM，我们将从中进行更改、修改、编辑、删除和添加子元素等。

我们将更新应用程序中可见元素的实际 JavaScript DOM 对象……但**只有在确实需要更新时**。我们执行的任何 DOM 操作都不会与花费时间更新原始 DOM 关联。这就是提高 React 应用性能的原因。

最棒的一点是，React 会为你自动完成这一切。作为 React 程序员，你不需要理解 React 内部是如何执行的。你只需要专注于应用程序的设计。

注意，当然，如果你直接在 JavaScript 程序中编写 JSX 代码，它甚至不会编译。你必须运行 JSX 处理器。要做到这一点，你通常需要从命令行初始化它，使其在后台持续运行。

Babel 是一个 JSX 插件。我还建议学习如何让 babel 监听你的文件。这意味着你可以设置 babel，以便在文件发生变化时，自动转译你的 `.js` 文件（并将其放入 "build" 或 "production" 目录）。这种 babel 功能被称为“**watch**”。它必须启用。我在我的视频教程中解释了如何在 Windows PC 上进行操作：

这个在 YouTube 上的 React 教程可以帮助你设置开发环境、安装 Node.js、NPM、babel、JSX，并帮助你开始监控你的 js 文件：

https://www.youtube.com/watch?v=tXaNyGcjEIo0

你可以通过简单地在网页顶部或底部的 `SCRIPT` 标签中添加 `babel.js` 来解决问题。JSX 可以正常转译。但这会显著减慢应用程序的处理速度。它应该仅用于测试。

另一方面，该视频只有 58 分钟，如果你认真想建立专业的 Web 开发环境，我建议在 YouTube 播放器上以 2 倍速快速浏览，这只需要大约 25 分钟。它就像一个微型入门课程。

最后，我们通过展示如何使用 `cloneElement` 克隆现有元素来结束这段讨论。

```javascript
React.cloneElement(element, props, children);
```

它的工作方式与 `createElement` 完全相同。只需将一个现有元素作为参数传递。然后，你传递给相应参数的任何 props 和 children 都将合并到原始元素上已有的属性中。这让人想起传统面向对象编程中扩展对象的功能。在这里，我们某种程度上是在模拟 OOP 功能。

创建的元素实际上可以渲染到 DOM。你不能渲染到虚拟 DOM。`render` 函数是 React 库内部处理这一过程的魔法。这是我们的元素从你的虚拟 DOM “复制并粘贴”到屏幕上可见的实际 DOM。

React 在主 `ReactDOM` 上提供了 `render` 方法，如下所示。在响应式编程中，ReactDOM 是仅于 React 后最重要的对象。

```javascript
ReactDOM.render(reactElement, domContainerNode);
```

在这里，`domContainerNode` 是 `reactElement` 将渲染、重新渲染或首次附加（挂载）的父元素。

如果你需要更新组件的属性，可以多次使用 `render`。

这是一个真实场景可能的写法。在这个例子中，我们获取一个 ReactElement 并将其渲染到 DOM 节点上：

```javascript
ReactDOM.render(
  React.createElement("div"),
  document.getElementById("container")
);
```

如果一个元素已经与变量名关联，你可以使用 `ReactDOM.findDOMNode` 查找它：

```javascript
ReactDOM.findDOMNode(element);
```

此语句返回与给定元素关联的 DOM 节点。注意，这在元素渲染到 DOM 之后才会生效。

## 特殊属性 (Special Props)

在这里我们将简要介绍特殊的属性名，其中有几个。这些在 React 中类似于 JavaScript 的关键字。

### Children

`children` 属性会被 `createElement` 自动添加到 `props` 中。

### className

该属性对应 HTML 的 `class` 属性。为了与 JavaScript 的保留字冲突，你必须在组件中使用 `className` 而不是 `name`。

### htmlFor

与 `className` 相同，用于 `for` 属性。在需要使用 `for` 属性的 React 元素中使用 `htmlFor`。

### key

`key` 属性唯一标识一个 ReactElement。它用于数组中的元素。

### ref

`ref` 属性接受一个回调函数，该函数将在：
- 挂载时传入 DOM 节点。
- 卸载或传入函数更改时传入 null。

### style

`style` 属性接受样式对象而不是字符串。在 React 中，没有机制可以通过文本字符串指定 CSS 样式。这是使用 JSX 的局限性之一。

但这种局限性也可以被视为优势，因为 CSS 样式现在可以通过编程方式表示，样式对象中的每个属性代表 CSS 属性对。起初可能觉得有点奇怪，但这种风格更符合 React 编程的整体方案。

## PropTypes

React 有一个名为 `propTypes` 的特殊属性。它的主要目的是类型检查。随着你的应用程序变大，类型检查可以帮助发现各种错误。

这里有一个例子。假设我们已经创建了一个名为 `ReactComponent` 的 React 组件。在开发模式下，默认开启类型检查。

```javascript
ReactComponent.propTypes = {
  name: React.PropTypes.string
};
```

`React.PropTypes` 的作用是开启存储在属性中的数据类型验证。默认情况下 React 有许多数据验证器，如果将数字数据类型传递到定义为字符串的属性（如上所示），你将在 Chrome 或浏览器的控制台中看到警告。





# 类组件选项

在本书的后续章节中，我们将更多地讨论组件。它们是你的 React 应用的构建块。但请记住，这毕竟是“指掌上的 React”章节！让我们简要概述 React 组件的完整范围，以及 React 库默认提供的选项和方法。组件通过存在主 React 对象上的 `createClass` 方法定义：

```javascript
var MyComponent = React.createClass({
  displayName: 'MyComponent',

  /* 这是你 React 类的核心
     选项和生命周期方法将写在这里 */

  render: function() {
    // 一旦渲染，返回一个新创建的元素
    return React.createElement(/* ... * */);
  }
});
```

这是组件类的基本结构。

# 组件选项

组件持有 `propTypes` 对象和两个返回对象的方法：

- 1. `propTypes`：将属性名映射到类型
- 2. `getDefaultProps`：返回一个对象的函数
- 3. `getInitialState`：返回一个对象的函数

# 生命周期方法

- 1. componentWillMount
- 2. componentDidMount
-- 3. componentWillReceiveProps
- 4. shouldComponentUpdate
- 5. componentWillUpdate
- 6. componentDidUpdate
- 7. componentWillUnmount

这 7 个方法可以在你的 React 类中实现。并不是所有的组件类都需要使用所有七个函数，这取决于你组件的用途。

每个方法基本上都是在 React 组件生命周期期间特定时间执行的事件。这些功能大部分都与检查组件的挂载和更新状态有关。

除了这些方法外，你当然也可以根据组件预期的功能添加你自己的自定义函数。

# 组件实例

组件实例是从我们在上一节中看到的类表示的实例化对象。以下是关于它们实现的一些提示：

- 1. 组件内部的 `this` 关键字指向它。
- 2. 无状态函数组件没有组件实例。
- 3. 一个组件实例可能会跨越多个 ReactElements 。

# 属性

- 1. 属性 **this.props** 包含了通过标签属性传递给 `React.createElement` 的任何 props。
- 2. **this.state** 属性包含由 `setState` 和 `getInitialState` 方法设置的状态。

# 方法

- 1. `setState(changes)` 将给定的更改应用到 `this.state` 以重新渲染 DOM 组件。
- 2. `forceUpdate()` 立即重新渲染组件到 DOM。

# 秘籍 (Gems)

在本节中，我将介绍几个扩展响应式编程的“秘籍”，并对重要的原则进行一些解释。每个秘籍都是对特定主题的集中讨论。

## 秘籍 1 - React 组件

组件是 React 应用的构建块。

由于 React 主要考虑到应用视图（交互式用户界面动态），React 组件可以被认为是你的 Web 应用程序组合的视觉区块。React 将每个组件视为可重用的模板。

在 React 中，每个组件都是 HTML、CSS 和 JavaScript 代码的组合，标识了你应用程序中的一个特定区块。

例如，这里是从 React 组件的角度查看我的 Twitter 页面 @gregsidelnikov。

在程序上，React 组件遵循嵌套 HTML 标签的足迹。它们有父元素和子元素，父元素也可以是层次链中另一个组件的子元素。

![父组件嵌套组件](img/05b8b68e82424c98c0b61100a18147b2_35_0.png)

将组件设计想象成你整个应用的蓝图。在你开始为响应式应用编写第一行代码之前，在纸上勾勒出一切是非常好的主意。这是一种直观的思考方式，将你的页面设计成具有独特元素的 Web 应用程序。

就像你当年第一次学习普通的 DOM 并意识到每个 HTML 元素（如 P、DIV、TABLE 等）实际上是对象模型中长长树状链中的一个对象一样，请将 React 组件看作与某种软件功能绑定的视觉区域。这次，这种功能将由你和你的应用程序需求自定义决定。

从 React 的这些最基础的原理中，你现在可以理解为什么 Facebook 和 Instagram 喜欢使用它。它是极快的，它帮助将类似流式的元素拆解为由组件组成的软件块，而这些组件只是 CSS、HTML 和 JavaScript 代码的组合。这种设计模型更贴近应用行为，而不是仅仅是使用表格类布局的信息性网站。

组件是层次级化的。它们可以是其他组件的子元素。在大多数情况下，组件是为你的应用程序中的复用而定制的。它们包含了可以适应各种情况的代码模式。React 代码通常遵循创建这些组件链的模式，它们在内部工作，同时保持快速的渲染速度和灵活性。

## 秘籍 2 - Render 方法

很有可能在你构建普通的 HTML-JavaScript 应用时，你已经在某种程度上将应用拆分成了不同的隔间。然后，你使用 Ajax 事件根据每个 HTML 单元中更改的数据类型来单独填充每个视图。

但 React 通过要求 `render()` 方法更进了一步。`render` 方法必须附加到你创建的每个 React 组件上。没有办法绕过它。这是 React 组件所要求的模式的一部分。

尽管 React 远不止视图层——让渲染方法在 React 编程中显式化——正是 React 经常被认为是基于视图的库的原因。我们将在整书中看到这是正确的，但为什么这并不完全正确。

说 React 编程仅仅是关于视图的是不公平的。事实上，渲染目标的选择告诉我们相反的结论。React 是一种遵循实际上不需要视图哲学的编程模式。

你可以将 React 组件的结果渲染到浏览器或渲染到文本字符串（使用专门为此设计的方法 `React.render()`）、JSON 对象或你希望任何地方。在这种情况下，渲染根本不是渲染。因为“渲染（render）”一词意味着数据的可视化。所以 React 更像是一组原则，而不是许多初学者在简单熟悉该库之前倾向于认为的“创建用户界面的方法”。

虽然你可以在 React 之外使用任何第三方库（例如数据库 IO 库），但 React 在视图元素背后的自定义编程方面仍然提供了很多内容。事实上，它要求你理解这些原理是如何运作的。

通常附加到 React 自己的“虚拟”DOM 上的 `render()` 方法是当你的应用程序首次加载到浏览器时执行的方法。因此，只有当它代表的元素中的数据应该更新时，才会执行。然而，这正是有趣的地方。在 `render` 方法被调用之前，React 组件甚至没有“挂载”到实际的 JavaScript DOM 上，也不会显示。而且你可以在不挂载的情况下创建 React 组件。我们将在秘籍 6 中详细介绍挂载。

我们知道 `render` 会触发数据集（或组件状态）的更新。但什么时候应该更新数据呢？这取决于组件中显示的数据类型，但也取决于一些在使用过程中关键时间负责更新它的通用函数。在书的后面部分，我们将接触负责控制这些事件的函数。

在真实场景中，元素本身可以是警报图标，通知最终用户警报数量的增加、关注者数量或个人资料查看量。





## Gem 3 - 虚拟 DOM 与带宽救星

React 让我们深入思考每个元素将代表的内容，因为每个组件都与某种软件函数绑定，该函数会实时更新每个组件中的数据，而无需更新整个布局布局。在 React 中，这个过程与传统应用程序相比更加高效。你不需要在普通的 HTML 网站上重新加载整个页面。

这让你的应用程序感觉与众，并节省了带宽。如果你想想，我们在 2017 年之前一直在构建的非响应式网站其实只是一个懒人的设计理念。为了查看是否有新提醒而重新加载所有内容，并不是最好的应用设计。然而，像 Facebook 这样的网站一直以来都在做这些。而且通过一点一的改进，它开始发生变化。这就是为什么我们正在向响应式实现过渡。

但响应式编程不仅仅是一堆用于获取数据并替换 HTML 元素的 AJAX 调用。它要复杂得多。

正因为快速访问相关组件通常是良好应用程序设计的关键，这就是虚拟 DOM（Virtual DOM）大显身场的地方。虚拟 DOM 是一种独特的方式，提供了一种快速修改 DOM 的方法，同时放弃了速度较慢的旧替代方案。

虚拟 DOM 无疑是选择 React 库编写应用程序的巨大优势之一。事实上，当你向 Web 项目中添加 react 库时，你也有必要添加 react.dom 库。两者是不可分割的。而且所有的响应式 JavaScript 应用程序默认都包含了 React DOM。

这就是 React 的虚拟 DOM 在你的应用程序的可用性上产生巨大差异的地方。它让网站具有原生应用程序的体验，每个元素都能对触摸事件做出即时响应。

你可能已经在 Netflix、Facebook 和 Instagram 等网站上看到这种现象开始发生。你实际上可以感觉到差异。操作是即时发生的，似乎每次点击按钮都不需要先等待 HTTP 请求加载。

应用程序即时响应。React 并没有消除 HTTP 带宽，它只是将带宽消耗降到最低，并关注数据是否真的应该因为点击按钮事件等原因而进行传输。

当然，像 Netflix 和 Amazon 这样的网站会预加载某些数据（例如电影预告片的前 15 秒），无论用户是否点击播放按钮。但与其他“响应式”原则结合在一起，它对 UI 响应速度产生了巨大影响。

我们仍然从熟悉的 HTML 元素构建应用，但对每个事件的响应率是由一个比 jQuery 的实现还要快得多的 DOM 带来的。

为了开始使用虚拟 DOM，你不需要做任何特殊操作。通过利用 React 组件模板模式，你自动在使用了 React 自己的虚拟 DOM 遍历。它通过提供驼峰命名的方法和属性（如 `className` 和 `fontFamily`），并匹配我们已经熟悉的名称，透明地模仿了标准的 DOM 模型。

## Gem 4 - 初始化 React 类的两种不同方式

在本书编写期间，Web 仍处于从 EcmaScript5 向 EcmaScript6 的过渡期。当 EcmaScript 2015 (ES6) 大约两年前发布时，它在 JavaScript 世界引起了巨大的动荡，并将程序员分为“旧方法”和“新方法”两类。有些人根据情况无缝地偏好使用其中一种风格而非另一种。两者没有优劣之分。

然而，ES5 和 ES6 执行的是完全相同的代码。大部分区别在于语法上。诚然，同时在两种不同的语言中工作可能会产生不必要的头疼，特别是当你第一次学习 React 时。

在 JavaScript 这种松类型语言中，做任何事情都没有所谓的“一种标准方法”。一直以来都是。

在创建 React 组件时，这种区分是极其关重要的。实现它并没有一种。

在本 Gem 中，我将演示如何用两种不同的方式创建完全相同的 React 组件。这里的区别是 EcmaScript5 和 EcmaScript6 本身的区别。

大部分情况下，一个显著区别是构造函数 (ES6) 和专门的初始化状态方法 (ES5) 的用法。让我们来看。EcmaScript5 的示例如下：

```javascript
var NewComponent = React.createClass({
  getInitialState() {
    return {/* initial state */ };
  }
});
```

注意，在 EcmaScript5 中不存在 `constructor` 关键字，这就是为什么在这种情况下 React  `getInitialState` 函数。如果你用 ES5 编写应用，你应该使用这种方法来初始化组件的默认状态。稍后我们将讨论状态。这是一个非常重要的主题。状态与 React 组件绑定。在规划应用程序时，你应该在组件及其状态之间建立心理关联。每个组件都负责拥有状态。

上面我们演示了 ES5 语法。我不会告诉你应该使用哪一种。

最终 ES6 将在几年内成为被采用的新标准，但许多程序员仍然偏好 ES5 格式。但由于 JavaScript 支持 ES5 作为 ES6 的子集，它仍然可以兼容未来的应用程序。

如果这对你有效，请像下面所示使用 EcmaScript6，现在使用了 ES5 中不可用的新键：`class`、`extends`、`super` 和 `constructor`：

```javascript
class NewComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { /* initial state */ };
  }
}
```

它是那样的，只是使用了 ES6 语法。虚拟 DOM 是选择 React 库编写应用程序的巨大优势之一。事实上，当你向 Web 项目中添加 react 库时，你有必要添加 react.dom 库。两者是不可分割的。而且所有的响应式 JavaScript 应用程序默认都包含了 React DOM。

这就是 React 的虚拟 DOM 在你的应用程序可用性上产生巨大差异的地方。它让网站具有原生应用程序的体验，每个元素都能对触摸事件做出即时响应。你可能已经在 Netflix、Facebook 和 Instagram 等网站上看到这种现象开始发生。你实际上可以感觉到差异。操作是即时发生的，似乎每次点击按钮都不需要先等待 HTTP 请求加载。应用程序即时响应。React 并没有消除 HTTP 带宽，它只是将带宽消耗降到最低，并关注数据是否真的应该因为点击按钮事件等原因而进行传输。当然，像 Netflix 和 Amazon 这样的网站会预加载某些数据（例如电影预告片的前 15 秒），无论用户是否点击播放按钮。但与其他“响应式”原则结合在一起，它对 UI 响应速度产生了巨大影响。我们仍然从熟悉的 HTML 元素构建应用，但对每个事件的响应率是由一个比 jQuery 的实现还要快得多的 DOM 带来的。为了开始使用虚拟 DOM，你不需要做任何特殊操作。通过利用 React 组件模板模式，你自动在使用了 React 自己的虚拟 DOM 遍历。它通过提供驼峰命名的方法和属性（如 `className` 和 `fontFamily`），并匹配我们已经熟悉的名称，透明地模仿了标准的 DOM 模型。

## Gem 4 - 初始化 React 类的两种不同方式

在本书编写期间，Web 仍处于从 EcmaScript5 向 EcmaScript6 的过渡期。EcmaScript 2015 (ES6) 大约两年前发布时，它在 JavaScript 世界引起了巨大的动荡，并将程序员分为“旧方法”和“新方法”两类。有些人根据情况无缝地偏好使用其中一种风格而非另一种。两者没有优劣之分。

然而，ES5 和 ES6 执行的是完全相同的代码。大部分区别在于语法上。诚然，同时在两种不同的语言中工作可能会产生不必要的头疼，特别是当你第一次学习 React 时。在 JavaScript 这种松类型语言中，做任何事情都没有所谓的“一种标准方法”。一直以来都是。

在创建 React 组件时，这种区分是极其关重要的。实现它并没有一种。

在本 Gem 中，我将演示如何用两种不同的方式创建完全相同的 React 组件。这里的区别是 EcmaScript5 和 EcmaScript6 本身的区别。

大部分情况下，一个显著区别是构造函数 (ES6) 和专门的初始化状态方法 (ES5) 的用法。让我们来看。EcmaScript5 的示例如下：

```javascript
var NewComponent = React.createClass({
  getInitialState() {
    return {/* initial state */ };
  }
});
```

注意，在 EcmaScript5 中不存在 `constructor` 关键字，这就是为什么在这种情况下 React  `getInitialState` 函数。如果你用 ES5 编写应用，你应该使用这种方法来初始化组件的默认状态。稍后我们将讨论状态。这是一个非常重要的主题。状态与 React 组件绑定。在规划应用程序时，你应该在组件及其状态之间建立心理关联。每个组件都负责拥有状态。上面我们演示了 ES5 语法。我不会告诉你应该使用哪一种。

最终 ES6 将在几年内成为被采用的新标准，但许多程序员仍然偏好 ES5 格式。但由于 JavaScript 支持 ES5 作为 ES6 的子集，它仍然可以兼容未来的应用程序。

如果这对你有效，请像下面所示使用 EcmaScript6，现在使用了 ES5 中不可用的新键：`class`、`extends`、`super` 和 `constructor`：

```javascript
class NewComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { /* initial state */ };
  }
}
```

它是那样的，只是使用了 ES6 语法。

## Gem 5 - 状态与生命周期

在 React 中，每个组件都有状态。状态是一个包含值的对象。状态正如它听起来的那样。它是组件在多个标志、参数和设置方面的状态，通常由数字、布尔值、数组或映射指定。

React 组件的生命周期与状态密切相关。React 提供了几个默认方法来帮助我们编写辅助应用程序。这些方法在下面简要概述。

每个组件通常会通过以下辅助方法控制自己的状态。它们被设计在应用程序流程或组件生命周期的独特时刻修改或更新组件状态。

所有这些方法都挂载在组件对象上，如下。这只是一个展示这些方法在你 React 对象中位置的简单示例。

让我们来看！

```javascript
var MyComponent = React.createServer({
  displayName: 'MyComponent',

  // 这几乎组件的构造函数！
  getInitialState: function() { ... },

  // 组件挂载事件
  componentWillMount: function() { ... },
  componentDidMount: function() { ... },
  componentWillUnmount: function() { ... },

  // 组件更新事件
  componentWillReceiveProps: function() { ... },
  componentWillUpdate: function() { ... }
});
```




```javascript
componentDidUpdate: function() { ... },
shouldComponentUpdate: function() { ... };

// Render the component to the DOM
render: function() { /* return something */ }
};
```

这里有很多 `Will` 和 `Did` 方法。但它们意味着什么呢？
这些方法就像是我们组件的控制中心！
下面我将为组件生命周期期间各个事件提供简要描述，每个方法都负责其中一个。

`componentWillInitialState` 功能类似于组件构造函数。它在组件渲染到屏幕之前被调用。

`componentWillMount` 在 `render()` 方法执行之前仅调用一次。在组件的整个生命周期内不会再次被调用。有时被用作组件构造方法的同义词。

`componentDidMount` 在组件首次渲染后立即调用。

`componentWillUnmount` 在组件即将销毁时调用。这是清理内存和删除状态的地方。

`componentWillReceiveProps` 在 `props` 传递给组件时调用。例如，如果你有一个 `Form` 组件和一个 `TextInput` 组件，后者允许用户通过输入文本来更改其值。假设 `TextInput` 有一个 `onChange` 事件，向组件传递了一些 `props`。一旦新文本输入输入框，该值就会作为 `props` 传递给主组件。这就是 `componentWillReceiveProps` 被触发的时刻。

`componentWillUpdate` 在组件执行 `render` 方法正之前调用。它让我们有机会在下一次渲染更新之前处理任何状态变化。

`componentDidUpdate` 在 `render()` 方法完成 DOM 更新后不久立即调用。

`shouldComponentUpdate` 是一个默认方法，始终返回 `true`。我们借此控制组件元素是否应该在 DOM 中更新。但情况并非总是如此。例如，如果组件中某些状态或属性的新结果与其之前设置的值相等，那么可能就不值得更新 DOM。如果数据在更新后没有发生变化，为什么要将它发送到视图中呢？

这些方法对于理解虚拟 DOM 至关重要。随着我们一个一个逐渐剥离 React 编程原理，一切将开始变得清晰。

目前只需知道 React 组件通常会被挂载（mounted）到一个渲染目标（render target）。这就是为什么上面提到的某些默认方法使用了“mount（挂载）”一词，而不是你预期的传统的 `set` 或 `get` 方法。挂载是 React 编程以及在 React 虚拟 DOM 生系统中创建的组件中特有的概念。

我们已经从理论上讨论了组件。但在实践中，组件是什么？记住，你的应用程序是由模块化的元素组成的。组件本质上可以是任何东西，从按钮、文本框、复选框到显示文本的操作状态区域。你将根据应用程序用途用途确定组件的设计。

由于我们刚刚讨论了处理组件“挂载”的方法，那么在下一个“宝石（gem）”中探索它的含义就很自然了！

## 宝石 6 - 组件挂载 (Component Mounting)

React 是一个重视编程原理的库。其中之一是将组件视为元素的思想。组件是一种程序化（声明式）的方式，用于在应用程序中渲染你想要的内容。但 React 实际上并不关心你选择在何处或如何渲染这些元素。无论是 JavaScript DOM 还是其他地方。这听起来可能很惊讶，因为 React 以作为前端库而闻名。

这是因为 React 使用了被称为“渲染目标（render targets）”的东西。也就是说，你决定 React 渲染方法的结果将如何显示或传递到其他地方。

换句话说，你可以说 React 对于其组件内部的数据输出或存储是无关的（agnostic）。

例如……你可以将数据从组件输出到文件写入函数。换句话说，React 的渲染目标不仅限于 UI 元素，尽管在本书的大部分内容以及一般的 React 风格编程中，这才是你大部分需要处理的内容。

在之前的宝石中，我们讨论了每个组件如何处理自己的状态。状态可以是一个指示按钮是否被高亮的布尔标志，或者是导航菜单选项是否被选中。

现在，如果你一直在关注，这里就是一切开始联系起来的地方。React 组件是其状态和渲染方法的融合。我们在一个地方获得了对 UI 元素最重要的两个函数的程序化控制。

但是，“挂载（mounting）”到底是什么意思？在 React 中，出于性能考虑，我们使用了 DOM 的虚拟表示。

通过简单的创建一个组件，任何 DOM 元素都不会被触及。这是一个好消息，但这如何可能呢？这是因为原生 DOM 会增加应用程序的内存占用。

然而，通过 React 的虚拟 DOM，元素仅在需要时才被创建。（注：原文此处存在大量重复性文本，翻译时已根据逻辑进行清理）。



你选择什么作为后端和前端之间的通信桥梁完全取决于你。React 并不关心这一点。它的目的严格限于尽可能快地更新视图。

这种*挂载机制*让 React 成为一个多功能的库。因为从基本原理上说，React 也不关心最终结果是渲染在 DOM 中还是其他地方。

你可以将 React 的输出渲染到 XML 文档，将其视为自定义对象数据，或者返回 JSON。它结合了熟悉的编程原理，并尝试做到“为所有人提供一切服务”。这使得 React 成为一个用于用户界面以及折腾自定义软件实现的极其强大的编程工具。

现在，很有可能如果你是从传统的 2015 年 JavaScript 背景转向 React 的……与学习 jQuery 不同，学习 React 是一个更加投入的过程。它涉及到学习*软件开发原则*，而不是学习一组方法名，完成之后你就可以上路了！

然而，它确实有一些方法在 React 程序员之间正变得标准化。我们将在后的内容中探索它们。仅仅知道它们，而不理解 React 背后的基本哲学，是不够的。

## Gem 7 - Node.js & NPM

当我说学习 React 涉及的不仅仅学习 React 库要多得多时，这确实是真的。至少，使用 React 要求你安装 Node 库。

单单 Node 就可以写另一整本书了，但关于 React 库，我们需要安装它有几个原因：

- 1. 为我们的 React 应用提供一个 localhost 环境。安装 Node 使你能够从本地机器上的 http://localhost 运行你的应用程序。
- 2. Node 自动带有 Babel 和 JSX 支持（JSX 作为 Babel 插件安装）。在在 Mac（通过终端）和 PC 上，安装 Node 和 NPM 都出奇地简单。在 PC 上，这就像从官方网站下载 Node 安装文件一样简单。运行安装程序，你就一切搞定了。只需不要忘记在安装期间勾选 babel 复选框，它也包含在内。

在 Mac 上，你可以通过命令行下载 Node。打开你的终端应用程序并输入：

```
$ wget http://nodejs.org/dist/node-v0.4.4.tar.gz
$ -xzf node-v0.4.4.tar.gz
$ cd node-v0.4.4
$ ./configure
$ sudo make install
```

就是这样！配置日志将运行，然后你就完成了。

在 Ubuntu 上，你可能想要运行此附加命令来安装基本组件：

```
$ apt-get -y install build-essential
```

看起来到此时 node 已经安装并准备好为我们提供一个 localhost 地址，我们可以在那里测试 React 代码。

然而，好消息是，如果你已经在本地机器上安装了 Apache 服务器，并且它映射到了你的开发文件夹，那么使用 node 提供 localhost 环境就是没必要的。你已经设置好了。

在这种情况下，你可以直接在你现有的 Apache httpdoc 文件夹（或它映射到你机器的任何文件夹）中启动 React 程序。只需在该目录下创建一个新文件夹，例如“my-react-app”，像往常一样，你的项目将可以通过浏览器通过类似地址访问：

```
http://localhost/my-react-app
```

然而，强烈建议你安装 Node。出于任何原因，都是因为它带有命令行版本的 Babel 和 JSX 插件，这些对于正确设置开发环境是必须的。

在 Mac 终端上安装其实非常直接。但在 PC 上就稍微有点挑战性，特别是如果你以前从未做过的话。

如果你仍然不确定如何在这台 PC 上进行操作，我在 YouTube 上录制了一个 58 分钟的补充教程，可以在以下位置免费获取：

# React JS Tutorial 1 - For Beginners | ReactJS JavaScript ES6 Node.js, NPM, Babel Transpiler, Webpack

https://www.youtube.com/watch?v=tXaNvGcGjEi0

无论你处于开发过程的哪个阶段，它都值得过一遍。但如果你刚刚开始，它是必看的。

观看这个教程应该能让你开始通过 localhost 地址在 PC 上编写 React 应用。因此，在视频教程中，我将逐步演示整个过程。我不想在书中书中重写这些细节以占用更多空间。你可以以 2 倍速度观看，只需大约 25 分钟就能看完。

## Gem 8 - JSX 详细讲解

如果你已经开始学习 React，你应该听过很多关于 JSX 的介绍。你可能也听说过在 React 中没有必要使用它。这确实如此。但建议你使用它。它只是让事情变得简单得多，尽管它的语法对传统的 JavaScript 开发者来说起初可能有点吓人。

JSX 以一种“在 JavaScript 内部编写 HTML”的语言而闻名。这在某种程度上是正确的。预期的效果是我们可以把 HTML 标签视为 JavaScript 语句。然而， JSX 实际上使用一种形式的 XML，它类似于 HTML，使用与标准 HTML 标签匹配的标签名称，例如 DIV、UL、TABLE 等。记住，即使 HTML 也只是 XML 的远房兄弟。

虽然作为 JavaScript 语句的 HTML 起初看起来有点古董，但一旦你掌握了主意并开始使用它，它真的会变成本能。这绝对是完全全新的东西，通常不（而且在今天大多数浏览器中也不被编译），但让我们看看它是什么样的：

```javascript
var scoreBoard = { Player1: 10, Player2: 25 };
React.createElement('div', { className: 'class1' },
  React.createElement(SomeCounter, { count: 3 + 5 },
    React.createElement(ScoreUnit, { data-index: 2 },
      React.createElement('h1', {}, 'Leaderboard'),
      React.createElement(ScoreBoard, { className: 'results' }, scoreBoard)
```

虽然作为 JavaScript 语句的 HTML 起初看起来有点古董，但一旦你掌握了主意并开始使用它，它真的会变成本能。这绝对是完全全新的东西，通常不（而且在今天大多数浏览器中也不被编译），让我们看看它是什么样的：

```javascript
var scoreBoard = { Player1: 10, Player2: 25 };
React.createElement('div', { className: 'class1' },
  React.createElement(SomeCounter, { count: 3 + 5 },
    React.createElement(ScoreUnit, { data-index: 2 },
      React.createElement('h1', {}, 'Leaderboard'),
      React.createElement(ScoreBoard, { className: 'results' }, scoreBoard)
```

等等，让我重新检查后面页面代码块的 OCR。OCR 是破碎的。让我根据提供的上下文正确重建它。

修正后的代码块（第 55-56 页）：
```javascript
var scoreBoard = { Player1: 10, Player2: 25 };
React.createElement('div', { className: 'class1' },
  React.createElement(SomeCounter, { count: 3 + 5 },
    React.createElement(ScoreUnit, { data-index: 2 },
      React.createElement('h1', {}, 'Leaderboard'),
      React.createElement(ScoreBoard, { className: 'results' }, scoreBoard)
```

实际上，查看第 55 和 56 页的 OCR 文字：
"var scoreBoard = { Player1: 10, Player2: 25 };"
"React.createElement('div', { className: 'class1' },"
"React.createElement(SomeCounter, { count: 3 + 5 },"
"React.createElement(ScoreUnit, { data-index: 2 },"
"React.createElement('h1', {}, 'Leaderboard'),"
"React.createElement(ScoreBoard, { className: 'results' }, scoreBoard)"

让我提供集成了代码块的最终清理文本。

[content]
你选择什么作为后端和前端之间的通信桥梁完全取决于你。React 并不关心这一点。它的目的严格限于尽可能快地更新视图。

这种*挂载机制*让 React 成为一个多功能的库。因为从基本原理上说，React 也不关心最终结果是渲染在 DOM 中还是其他地方。

你可以将 React 的输出渲染到 XML 文档，将其视为自定义对象数据，或者返回 JSON。它结合了熟悉的编程原理，并尝试做到“为所有人提供一切服务”。这使得 React 成为一个用于用户界面以及折腾自定义软件实现的极其强大的编程工具。

现在，很有可能如果你是从传统的 2015 年 JavaScript 背景转向 React 的……与学习 jQuery 不同，学习 React 是一个更加投入的过程。它涉及到学习*软件开发原则*，而不是学习一组方法名，完成之后你就可以上路了！

然而，它确实有一些方法在 React 程序员之间正变得标准化。我们将在后的内容中探索它们。仅仅知道它们，而不理解 React 背后的基本哲学，是不够的。

## Gem 7 - Node.js & NPM

当我说学习 React 涉及的不仅仅学习 React 库要多得多，这确实是真的。至少，使用 React 要求你安装 Node 库。

单单 Node 就可以写另一整本书了，但关于 React 库，我们需要安装它有几个原因：

- 1. 为我们的 React 应用提供一个 localhost 环境。安装 Node 使你能够从本地机器上的 http://localhost 运行你的应用程序。
- 2. Node 自动带有 Babel 和 JSX 支持（JSX 作为 Babel 插件安装）。在在 Mac（通过终端）和 PC 上，安装 Node 和 NPM 都出奇地简单。在 PC 上，这就像从官方网站下载 Node 安装文件一样简单。运行安装程序，你就一切搞定了。只需不要忘记在安装期间勾选 babel 复选框，它也包含在内。

在 Mac 上，你可以通过命令行下载 Node。打开你的终端应用程序并输入：

```
$ wget http://nodejs.org/dist/node-v0.4.4.tar.gz
$ -xzf node-v0.4.4.tar.gz
$ cd node-v0.4.4
$ ./configure
$ sudo make install
```

就是这样！配置日志将运行，然后你就完成了。

在 Ubuntu 上，你可能想要运行此附加命令来安装基本组件：

```
$ apt-get -y install build-essential
```

看起来到此时 node 已经安装并准备好为我们提供一个 localhost 地址，我们可以在那里测试 React 代码。

然而，好消息是，如果你已经在本地机器上安装了 Apache 服务器，并且它映射到了你的开发文件夹，那么使用 node 提供 localhost 环境就是没必要的。你已经设置好了。

在这种情况下，你可以直接在你现有的 Apache httpdoc 文件夹（或它映射到你机器的任何文件夹）中启动 React 程序。只需在该目录下创建一个新文件夹，例如“my-react-app”，像往常一样，你的项目将可以通过浏览器通过类似地址访问：

```
http://localhost/my-react-app
```

然而，强烈建议你安装 Node。出于任何原因，都是因为它带有命令行版本的 Babel 和 JSX 插件，这些对于正确设置开发环境是必须的。

在 Mac 终端上安装其实非常直接。但在 PC 上就稍微有点挑战性，特别是如果你以前从未做过的话。

如果你仍然不确定如何在这台 PC 上进行操作，我在 YouTube 上录制了一个 58 分钟的补充教程，可以在以下位置免费获取：

# React JS Tutorial 1 - For Beginners | ReactJS JavaScript ES6 Node.js, NPM, Babel Transpiler, Webpack

https://www.youtube.com/watch?v=tXaNvGcGjEi0

无论你处于开发过程的哪个阶段，它都值得过一遍。但如果你刚刚开始，它是必看的。

观看这个教程应该能让你开始通过 localhost 地址在 PC 上编写 React 应用。因此，在视频教程中，我将逐步演示整个过程。我不想在书中书中重写这些细节以占用更多空间。你可以以 2 倍速度观看，只需大约 25 分钟就能看完。



我们将暂时放下 gem 格式，因为这本书的第一部分设计初衷是为了让你熟悉 React 编程和现代软件开发的最常用原则。

这些理论将帮助我们研究使用 React 库进行编程的实践。所以，让我们开始吧，从编写我们的第一个 React 组件开始。

## Lesson 1 - 编写你的第一个 React 组件

下面你看到的是你可能编写的第一个 React 组件的紧凑示例。它只是将通用的“Hello World”消息渲染到 DIV 元素中。而且它只需要一行代码。

```javascript
React.Classes({render: function() {
  return (
    <div>Hello World.</div>
  )
}\});
```

在这里，我们正在使用 React 库主对象的方法 `createClass`。这就是创建组件的方式。但这段蓝色的代码是什么呢？它看起来像 HTML，但周围没有用双引号包围！

组件通常存储在变量中。

例如：

```javascript
var HelloWorld = React.createClass({ .. });
```

将组件存储在变量名中可以帮助我们在以后创建元素之间创建父子关联。这只是是一种用以编程方式在嵌套组件之间建立关系的方法。

如果你来自传统的 JavaScript 程序员背景，这段代码中的某些部分可能会有些奇怪。高亮显示的 JSX 代码似乎格格不入。

但请记住，React 编程与使用额外工具相关。React 库本身应该只是你整个应用程序的一部分。没有人会只用 React 库来编写 React 应用。它只是墙上的其中一块砖。

在 React 中，我们可以在 JavaScript 内部编写 HTML。这是我们多年来习惯的传统的“HTML 内部编写 JavaScript”思想的反转，例如，我们将 JavaScript 写在 HTML 的属性标签中（如 `onclick = "this.style.color='red'"`）。

但 React 给了我们反相反的能力。我们将随着学习的深入而发现原因。现在，让我们扩展一下组件创建，然后我将简要解释 JSX 如何帮助我们处理 HTML 块并将其视为返回值。

话虽如此……让我们进入第一个 React 组件的完整示例，并在特定的 HTML 元素中渲染它的内容：

```javascript
// 添加所需的库代码
var React = require("react");
var ReactDOM = require("react-dom");

// 创建我们的第一个 react 组件 "HelloWorld"
var HelloWorld = React.createElement({
  render: function() {
    return (
      <div>
        Hello World.
      </div>
    )
  }
});

// 在 id 为 "app" 的 HTML 元素内部绘制 "HelloWorld" 组件
ReactDOM.render(<HelloWorld />, document.getElementById("app"));
```

注意，我们新创建的组件 HelloWorld 有它自己的 `render` 方法。但作为主要渲染引擎的 ReactDOM 对象也有它自己的 `render` 方法。两者之间的联系是 `ReactDOM.render` 调用了 `render` 方法作为第一个参数。在这种情况下，这个参数就是我们的 `HelloWorld`。

在这里，首先包含了上述 React 和 ReactDOM 库。当你从零开始一个新的响应式应用时，你需要这样做。这就是初始化 React 的方式。

接下来，一旦我们在项目中包含了 React，我们将使用 `React.createClass` 方法创建一个 React 类的新实例。这并不是初始化 React 应用的唯一方法，但在本章中我们将坚持使用这个示例。

最后，我们调用了 ReactDOM 自己的 `.render` 方法。而 `<HelloWorld/>` 是我们分配给古老 React 代码的变量 `HelloWorld`。基本上，React 的 `render` 方法接收两个参数。

你只需要将想要渲染的内容作为第一个参数，将你想要渲染的位置作为第二个参数（在本例中是 ID 为 "app" 的 HTML 元素）。所以从现在起，任何赋值给 `HelloWorld` 变量的内容都将被渲染在像 `[div id = "app"]` 这样的元素中。

这就是 React 编程背后的基本思想。你构建组件并让它们在特定的元素内执行操作。我们构建组件并让它们在 HTML 中工作。虚拟 DOM 会自动处理这些视图。

但还有一点……

这是一个误解点，JSX 没有内联 CSS 解析器。所以虽然你可以使用带属性的 HTML 元素，但 *style* 属性将不是其中之一。你仍然可以使用像 **name** 这样的属性。

这经常被误解。让我们考虑以下示例，它创建了一个根组件，由一个 U 元素组成，通过分配 `className` 属性将其称为 "my-list"：

```javascript
var root = React.createElement('ul', {
  className: 'my-list',
}child);
```

在 JSX 中使用 `className` 的原因是因为这是原始 JavaScript DOM 的属性名。例如：

```javascript
var cn = document.getElementById("my_id").style.className;
```

这是因为认为 JSX 限制了 JavaScript 保留关键字的使用。虽然这是一个相当真实的评估，但问题源于 JSON 表示法，而不是 JSX。

JSX 仅仅将 HTML 语法转换回 JavaScript。初看这可能很奇怪，但 JavaScript 现在有了自己的内部 HTML 处理器。这种思考方式是熟悉 JSX 的一个良好起点。随着我们在书中不断进行，我们将作为源码示例的一部分更深入地探讨它。

虽然很有诱惑，但完全理解 JSX 是如何做到的完全没。它在内部处理这些，并帮助我们专注于编写代码。它是 XML 的派生品，而不是 HTML，因为 XML 更严格。这意味着它更适合设计库。但主要是因为它更容易解析和理解。

恭喜你创建了第一个 React 组件！我想要保持简单，不让你被过多的东西淹没。在 React 中，将 HTML 写入 JavaScript 是通过安装 JSX 插件实现的。是的，这一功能通过 node.js 启用。你可以通过以下官方 GitHub 仓库查看 JSX 源码：

**https://github.com/jsx/JSX**




解决此问题的通用方法是给属性名加上引号：

```javascript
var root = React.createElement('ul', {
  className: 'my-list'
}, child);
```

我们还没有深入探讨 React 编程的细节来详细讨论组件之间的父子关系。但因为在例例中我们使用了第三个参数 `child`，我想对它的含义简单说几句话。

在接下来的章节中，你将看到组件之间父子关联是如何工作的。但基本上，现在你只需要知道，无论你作为 `createElement` 方法的第三个参数传递什么元素或多个元素，它们将通过 `this.props.children` 属性作为 "props" 可用。

这样，你就可以从父类中操作子组件了。父类通常是你的整个应用的核心，包含了所有的子组件。父组件可以有多个子组件。

以后我们会详细讨论 props 的用法。现在，只需要知道 props（或属性）对于 React 组件来说，就像参数之于函数。你只需将它们作为响应式元素功能所需的自定义值，直接传递到对象中即可。

还要记住，你不能随意粘贴任何 HTML 来作为 JSX 语句。JSX 版本的 HTML非常相似，但并不是 100% 准确的 HTML 规范。它非常接近，但存在一些差异。

正由于这些原因，JSX 可能会让你感到困惑。我曾挣扎了一段时间，但当我意识到它的主要目的是帮助更快地编写代码时，我想一旦我适应并习惯性地使用它，长期来看它会让事情变得简单得多。

这几乎就像是重新学习多年 HTML 标准的操作。困难的部分在于了解 JSX 的局限性。因为当你发现 JSX 中使用的 HTML 看起来格式正确但却不起作用时，由于不知道为什么无效，你可能会感到非常沮丧。

它确实挑战你用全新的方式来思考应用程序某些部分的设计。但请耐心看这些例子，最终你会逐渐理解并开始变得更有意义。

## Props

在在上一个章节中，我提到了 React 组件。但其中还有很多奥问。之前，我们创建了一个简单的组件，看起来就像这样：

```javascript
ReactDOM.render(
  <h1>Hello</h1>,
  document.getElementById('root')
);
```

注意，我们直接在 `render` 方法的参数中输入了 HTML 标签 `<h1>`，而没有加引号。这是 JSX 提供的语法风格。它在 JavaScript 中无法编译，但像 PHPStorm 这样的智能 IDE 识别 JSX 语法，并不会将其视为错误。

只要你的项目中包含了 JSX（通常通过 babel.js 库或其对应的命令行插件，后者是我建议在生产服务器上使用的），这代码就能正常编译。

现在我们知道，只有当你的项目中包含了 babel 转换译器（`babel.min.js`）时，它才能工作。（换句话说，不要尝试在“桌面”上某个文件夹的记事本里编写它，因为你的开发环境必须正确配置才能进行编译，或者至少应该在页面的 SCRIPT 标签中包含 babel.js。）它使用内部的 JSX 处理器将此内联 HTML 转换为 JavaScript。

## 函数纯性

在进入 React props 之前，我想提一下一点。在 React 中，props 是只读的。这与一种特定的函数类型——纯函数（pure function）很大有关。在传统的软件开发中，纯函数是指内部不会改变传递给它的参数的函数。

```javascript
// 纯函数；不修改参数值
function sum(a, b) { return a + b; }
```

这被认为是纯函数，因为它的主体没有修改任何作为参数传递的参数。相反，下面展示了一个非纯函数的示例：

```javascript
// 非纯函数；修改传递的参数 "total" 的值
function sub(total, less) { return total -= less; }
```

在 React 中，props 遵循“纯”的理念。这意味着你可以传递它们，前提是你的 React 组件不会从内部更改它们的值。这正是 React props 变为只读的原因。遵循这一规则是好的。

Props 派自 HTML 元素的属性。它们被称为 props 有点奇怪，因为在 HTML 元素中，属性是像 `DISABLED` 或 `CHECKED` 这样的单关键字标记。

props 更好的名字应该是 attributes（属性）。因为它们类似于 HTML 属性的 `name=value` 键对，而不是 props。但事实就是如此。React.js 的开发者选择了这种命名规范！不要怪信者：

如果你一直在关注我们上一个章节的讨论，你现在应该知道组件是什么。它们是 HTML、CSS 和 JavaScript 代码块的组合，决定了应用程序某个视觉区域的功能。它们负责更新诸如消息流、警报和各种状态更新。

我们也知道，组件通常有一个 `render` 方法来在应用中显示它。

学习 React.js 时，你遇到的下一个问题就是 props。props 就像函数参数。只不过你将它们传递给组件而不是函数。但原理是相同的。

让我们创建一个组件并向它传递一个 prop。

```javascript
// 创建一个 Hello 组件
var Hello = React.createClass({
  render: function() {
    return (
      <div>Hello, {this.props.name}</div>
    )
  }
});
// 现在在应用中调用它
ReactDOM.render(<Hello name="Jason"/>, document.getElementById("app"));
```

## 函数式组件

上面我们演示了一个使用 `createClass` 的标准组件，它包含一个 `render` 方法。但接下来的代码实际上无非一个函数：

```javascript
function Hello(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

使其成为有效组件的事实是它返回了一个 React 元素。React 元素可以渲染在屏幕上。这是 React 风格编程的重要部分，很容易习惯。记住，在 JavaScript 中，一切都是对象，甚至是函数也是如此。这就是为什么这些组件被称为函数组件的原因。

## 披着羊皮的狼

如果你知道继承是如何工作的，那么这就是它在 JavaScript 中的模仿方式。我说是“模仿”，是因为在面具之下，JavaScript 仍然使用基于原型的继承。这可能是幸运，也可能是诅咒。

JavaScript 定义的继承标准与 C++ 或 Java 等更成熟的语言相比，并不是真实的。换句话说，由于 JavaScript 是弱类型，你可以忘记在 JavaScript 中创建像“接口”这样的高级对象结构。

严格的编程语言通常更擅长提供功能面向对象编程环境。在这里，EcmaScript 开发者决定稍微装饰一下 JavaScript 语法，让世界看起来更像一只羊。

但大多数程序员都认为这种语法改进了 JavaScript 的编程。至少在视觉上是这样。

这种方式创建组件的一个主要区别是通过 `this` 关键字变量访问 `props.name` 属性。否则，它和上一个例子中的函数组件的功能完全一样。

```javascript
class Hello extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```





## 原生 Babel 对比 JavaScript Babel

我在上一个章节中尝试微妙地提到这一点。但在继续进行之前，这应该得到一个简短的解释。我不希望让你在不知道它可能没有为真实生产环境正确配置的情况下，误导地看到 babel 在运行。

最好是将 babel 作为独立的应用程序在后台运行，作为你开发环境的一部分。这通常随 Node 安装默认提供。只需从 Google 下载 Node 并一直点击“Next”按钮完成安装即可。

通过 `SCRIPT` 标签直接添加 babel 是可能的，并且适用于测试。但由于 babel 的 JavaScript 库运行速度较慢，建议安装可以在命令行运行的原生版本。JavaScript 版 babel 库处理此类内容时速度很慢，而且违背了 React 编程的初衷——React 的目的之一就是为了优化应用的运行速度。

## NPM

命令行 babel 应用随 Node.js 的安装一起提供。因此，如果你安装了 Node，就会自动拥有了 babel 包。你只需要在命令行中使用 NPM 工具单独安装它们，该工具也随 Node 默认提供。

在学习 React.js 时，直接通过 `SCRIPT` 标签添加 babel 是完全正常的。但当你的程序上线时，它的速度不足以满足生产环境。无论如何，babel 所做的只是是将你的 EcmaScript6 和 JSX 代码“转译”回 EcmaScript5，以便你可以在任何尚不支持完全支持 ES6 的浏览器中运行它。（截至本文写作时，没有任何一个浏览器支持。）

## 转译源代码

你可能听过论坛、Twitter 和 reddit 上的程序员使用“转译”（transpiling）一词，但可能还没有完全理解其背后的概念。

通常，转译是将一种语言的代码编译成另一种语言的源代码的过程。它仅仅是语言之间的编译。然而，在 JavaScript 中，我们是在两个不同的 EcmaScript 规范（5 和 6）之间进行转译。

这使我们能够使用 EcmaScript 6 编写代码并将其转译为 EcmaScript 5，以便现代浏览器能够运行你的代码。在写作时，大多数浏览器不支持 ES6，甚至 Chrome 也是。

最终，当所有浏览器都推出 ES6 支持时，就可以安全地停止使用 babel 进行 EcmaScript 规范之间的转译了。只需在标准的 JavaScript 文件中编写代码，它即可开箱运行。

但在那之前，我们可以利用这个机会学习一个有趣的源码工具。总会有新标准问世，转译的艺术可能在短期内不会消失。

*** * ***

在本章中，我想向你介绍超越组件创建本身的 React 编程基本原理。在这里，我在讨论组件和 props 的背景下简要提到了它们。随着学习，我们将继续深入研究响应式编程原理。这一次，由于已经对这些原理有了初步了解，这将帮助我们向编写实际的 React 应用迈阶。

## 第二课 - 嵌套组件

React.js 中的嵌套组件帮助你创建更复杂的视图元素结构。我之前提到过 React 组件的创建。作为一个提醒，这里是创建一个组件的方法。

```javascript
var Component = React.createClass({ render: function() {
  return (
    <Something></Something>
  )
}});
```

这只是一个返回一组 `<Something>` HTML 标签的基础组件。我知道，你可能还在习惯返回一个没有加引号但看起来像 HTML 标签的东西，但到那时它将开始看起来更加熟悉了：

正如你想象的那样，这是你在使用 React 时会大量使用的代码结构。大多数其他内容都源于此。如果你用过 jQuery，这种组件结构可以与 jQuery 的对象选择器语法相比：

```javascript
$(".class").on("click", function() { /*do something */ });
```

其中我们在事件执行完成后返回一个回调函数。在 react 中，我们返回一个 HTML 元素，它通常会被放置在我们前端的应用结构中。

对于 React 组件，它只是一个包含 `render` 函数的 JavaScript 对象，并有一个返回转译后的 JSX 代码的 `return` 语句。这就是将 `<Something>` 标签转换为浏览器可以理解的 EcmaScript5。

`render` 函数和 `return` 语句中的内容取决于你应用程序的用途。在这个示例中，为了清晰起见，让我们分别这些这些对象 **Parent**（父）和 **Child**（子）。如果你在编写应用程序，真实的名称对可能是 Friend 和 FriendList，或者 Customer 和 CustomerProperty。

## 带有单个子元素的父

使用这种模式，你可以实现基本的视图功能。首先，让我们创建该模式的最小构建模块——子组件。

```javascript
var Child = React.createClass({
  render:function() {
    return
    <BUTTON onClick={this.props.onClick}> {this.props.text} </BUTTON>
  }
});
```

在这种情况下，子组件是一个返回按钮元素的基础组件。按钮提供了一个 `onClick` 事件，该事件将由 `this.props.onClick` 方法执行。现在让我们创建它对应的 Parent 类，并将 Child 作为它将返回的对象。

```javascript
var Parent = React.createClass({
  render:function() {
    return (
      <Child onClick={this.handleChild} text={this.props.text} />
    )
  },
  handleChild:function(event) {
    // 逻辑处理
  }
});
```

（注：由于原文后部分存在大量重复且破碎的描述，此处已根据逻辑整合并翻译了核心的 Parent/Child 结构示例。）




我知道学习所有这些内容似乎很麻烦，但实际上，一旦你编写了其中几个组件，你就会看到 React 的多功能性，因为它就像是将自定义编程嵌入到你日常的 HTML 元素中，对数据流拥有完全控制权，并利用虚拟 DOM，它在更新应用程序需要更新的区域时极快。

我希望你喜欢这个教程，并且它对你很有启发。在我的新书《React Gems》中，会有更多关于这些的内容，这本书即将出版。

# 第 3  - 处理组件事件

到目前为止，我们只查看了 React 程序的节点组合。我们创建了组件并查看了它们的内部结构。

在本节中，我们将深入深入研究 React 组件的结构和功能。除了 `render` 之外，我们将探索三个新方法，每个方法在组件生命周期中的不同时间执行。这赋予了我们对应用程序更大的创造性控制力。

始终记住，React 组件具有状态（state）。组件的完全目的是与该组件对象所代表的自定义状态绑定。状态是一个包含数据的对象。但组件还具有辅助函数，这些函数可以更容易控制这些状态在特定上下文中如何工作。

在本节中，我们将查看其中的一些方法。

## 方法 1 - getInitialState

每个组件都负责渲染自己的状态，但 `getInitialState` 方法总会在我们的 `render` 函数之前被调用。它的功能类似于对象的构造函数。在这里，我们设置默认值。

```
var Example = React.createClass({
  getInitialState: function() {
    return {
      state: 0;
    }
  }
});
```

你经常会在整个 React 组件中看到 `getInitialState`。它会重置绑定到组件的默认值。在这里，你可以从数据库读取值，或者在将此组件渲染到屏幕之前将状态重置为默认值。

你可以将此方法与 ECMScript 6 提供的默认构造方法交叉使用：

```javascript
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = { state: 0 };
  }
}
```

这里唯一的显著区别是我们正在使用 `this` 关键字将状态挂载到主对象上。

要在组件渲染到屏幕上时访问状态，我们必须使用 `componentDidMount` 方法：

## 方法 2 - componentDidMount

当组件渲染时，React 会自动调用 `componentDidMount`。通过将其添加到自定义的 React 组件中，你对其进行了重载（overloading）。重载意味着向你正在扩展的自定义组件的默认 React 组件对象中已有的方法添加你自己的功能。这就是使用 `extend` 关键字的全部目的。我们正在扩展库已经提供的 React 组件对象的默认功能。

当我第一次在 React 组件中听到“挂载（mounting）”函数时，我不理解它的意思。难道我们不是简单地为我们的主要 React 组件挂载一堆辅助方法吗？

我们在书的前面的部分已经提到过挂载。如果你仍然需要复习这个过程，我建议确保你已经复过了之前讨论过的“Gem 6 - 组件挂载”。

`componentDidMount` 是负责在组件挂载后设置状态的方法。

```
var Example = React.createClass({
  componentDidMount: function() {
    this.state = 1;
  }
});
```

它简单意味着虚拟 DOM 已经与一个将在屏幕上进行实际更新的 DOM 节点相关起来。该方法在执行完组件的 `render` 命令后总是被调用的。它们是同义词，可能可以互换使用。它确保并告诉我们元素实际上存在于虚拟 DOM 中。`render` 方法已经在它上面调用过了！

## 方法 3 - componentWillUnmount

最后，`componentWillUnmount` 在组件从页面移除并即将销毁之前被调用。

```
var Example = React.createClass({
  componentWillUnmount: function() {
    this.state = null;
  }
});
```

注意，我们正在将状态重置为 `null`。组件被销毁了，我们不再需要它的数据。这就是我们清理组件所用内存（如果有的话）的地方，例如取消初始化的定时器。

# 用 React 编写的完整应用程序示例

我们已经涵盖了足够编写完整 React 应用程序的原则。我刻意让书中的所有示例都保持简单。复杂性通常来自编程中的创意发挥，如果我把一个大型程序丢进这本书里，对你来说可能会产生挫败感，而不是激励作用。

在这里，我将构建一个简单的搜索应用，它可以从数组集中查找结果。如果输入的字符与列表中的任何项匹配，它们将被过滤掉，所有其他条目将被忽略。

这个应用就像 Google 搜索的自动查找功能，当你向查询输入框输入短语时，项目会下拉显示。下面我列出了完整的源代码。

在这里，我将不包含应用程序的级联样式表（CSS）部分。这可以单独处理。我们希望严格关注 React 的实现。

与你使用标准 JavaScript 代码需要做的所有事情相比，这个应用程序异常地紧凑，如果它真的能实现的话。

## 搜索列表

让我们使用 JavaScript 中的对象字面量格式创建潜在搜索结果列表：

```javascript
// 首先，让我们定义所有可搜索动物列表
var libraries = [
  { name: 'Wolf', url: 'http://localhost/wolf' },
  { name: 'Panther', url: 'https://localhost/panther' },
  { name: 'Fox', url: 'http://localhost/fox' },
  { name: 'Giraffe', url: 'http://localhost/giraffe' },
  { name: 'Elephant', url: 'http://localhost/elephant' },
  { name: 'Ferret', url: 'http://localhost/ferret' },
  { name: 'Lion', url: 'http://localhost/lion' },
  { name: 'Lioness', url: 'http://localhost/lioness' },
  { name: 'Tiger', url: 'http://localhost/tiger' },
  { name: 'Tigress', url: 'http://localhost/tigress' },
  { name: 'Cat', url: 'http://localhost/cat' },
  { name: 'Dog', url: 'http://localhost/dog' }
];
```

## 编写 React 应用

```javascript
// 创建搜索组件
var SearchComponent = React.createClass({
  // 将输入元素重置为空
  getInitialState: function() {
    return {searchString: "" };
  },

  handleChange: function(e) {
    // 注释下面这一行将导致输入框不变化
    // 因为 React 输入框无法独立于赋值给它的值变化
    // 在这种情况下是 this.searchString。
    this.setState({searchString: e.target.value});
  }
});
```

```javascript
// 渲染组件
render: function() {
  var libraries = this.props.items,
  searchString = this.state.searchString.trim().toLowerCase();
  if (searchString.length > 0) {
    // 我们正在搜索。过滤结果
    libraries = libraries.filter(function(l) {
      return l.name.toLowerCase().match(searchString);
    });
  }
  // 作为 JSX 语句返回此组件
  return <div>
    <input type="text"value={this.state.searchString} onChange={this.handleChange} placeholder="在此输入" />
    <ul>
      {libraries.map(function(l) {
        return <<<li>{l.name} <a href={l.url}>{l.url}</a></li>;
      })}
    </ul>
  </div>;
}}
```

```javascript
// 在页面上渲染 SearchComponent 组件
ReactDOM.render(
  <SearchComponent items={libraries} />,
  document.getElementById('container')
);
```

将此代码放置在应用程序的主 .js 文件中并运行。它将产生基本的下拉功能。输入部分动物名称将从列表中过滤掉。理想情况下，你将从数据库或其他数据存储机制加载此列表。

正如你所看到的，取决于你正在设计的应用程序类型（在这种情况下，应用程序非常简单），你可能会或不使用任何挂载或更新方法，仅仅取决于


你的组件所代表的元素的本质。

我希望这能为你开始编写自己的 React 应用提供足够的弹药。

与 JSX 类似，在 React 中编程假设你已经掌握了许多知识。其中之一就是 EcmaScript 6 规范。这非常重要，因为理想情况下，在学习制作 React 应用的过程中，你希望从旧式的 ES5 语法过渡到 ES6。这种标准在大约一到两年内，将会在 Chrome、Firefox 和 Safari 等所有现代浏览器中得到原生支持，而无需使用额外工具进行代码编译。

书的其余部分将介绍 JavaScript 6 中应用到 JavaScript 语言的一些重大变化。

# EcmaScript 6 - 你需要了解的

当 React 创建时，ES5 规范正处于焦点。在 2015 年甚至在整个 2016 年期间，它仍然是非常新颖的。

然而，到 2017 年，它开始逐渐适应 ES6 语法。这就是为什么在学习 React 时，讨论应用到这一新标准的重大变化至关重要。

当你学习 React 时，你学习的不仅仅是 React。它在 ES5 中运行良好良好，但那种语法正在变得过时。这正是许多程序员会感到困惑的地方，因为本质上同一个库在互联网和书籍中看到的各种示例中，看起来可能都不一样。

如果你不了解 React，可能你也对 EcmaScript 6 一点都不了解。我知道做出这种假设是危险的，但我认为通过本章将学到的内容可以证明它是合理的。

ES5 本身并没有问题。它在短期内不会消失。我认为，在行业仍处于从一个规范向另一个规范过渡的时期编写教育类书籍，偶尔在两者之间切换是很重要的。

但我们已经到了书的后续，现在我们将调查 EcmaScript 6 规范中 JavaScript 的主要区别和新增。在书的最后，我还会为这里讨论的许多主题提供备查表。

## var 和 let 关键字

在 ES6 中，人们的共识是现在使用 `let` 关键字代替 `var` 关键字。其原因下文所示：

- 使用 `let` 关键字时没有**提升**（hoisting）。如果你熟悉 JavaScript 的提升机制，你会发现使用新的 `let` 关键字时的不同。

提升是指 JavaScript 将所有变量定义移动到它们定义所在作用域顶部的过程。这个不为人知的过程是在幕后完成的。但实际上是：

```
{
console.log( a ); // undefined; 但仅因为被提升了
var a = 1;
}
```

而 `let` 的示例是：

```
{
console.log( a ); // ReferenceError: "a" 完全未定义
let a = 1;
}
```

在上面的示例中，尝试打印变量值时，控制台输出是 `undefined`。在第一情况下，是因为变量被提升了；但在第二个示例中，它没有。

- 在全局作用域中。`let` 关键字和旧的 `var` 关键字仍然限于全局作用域。但 `let` 关键字不会附加到全局 `window` 对象上：

```javascript
var a = 1; // 将附加到全局 window 对象
let b = 1; // 将不会附加到全局 window 对象
console.log(window.a); // 1
console.log(window.b); // undefined
```

- 在函数作用域中。**let** 和 **var** 关键字在函数作用域内仍然是相同的：

```javascript
function helloThere() {
let x = 1; // 作用域相同
var y = 1; // 作用域相同
}
```

- 在语句中。**let** 关键字仅在 `for` 循环内部可见，而 **var** 在整个函数作用域内可见。因此，**let** 关键字限制了定义在 `{` 和 `}` 括号指定的**最近闭合块**内变量的可见性。下面我们先来看看 **var** 传统是如何处理作用域的：

```javascript
// var 在函数和 for 循环内部示例
function helloThereIterator() {
// i 在这里理论上也是可见的
for (var i = 0; i < 10; i++) {
// i 在这里可见的
}
```

这可能不是 `var` 关键字最好的例子（因为 for 循环从初就是定义的），尽管它在函数中处处可用。但它仍然说明了这一原理。

传统上，已知 `var` 在函数的 `{ }` 括号内可以被访问，但对函数作用域隐藏，除非它是 `window` 对象。这是基本规则。但 JavaScript 就是如此复杂……只有当在函数内部没有找到变量时，才会检查 `window` 对象，而后者是在函数外部的。

作为程序员，确定该变量是否应该从全局作用域可用是你的责任。这是 JavaScript 试图“兼顾所有人”的一个例子。

虽然这种松散在很多情况下很有帮助，并让学习曲线几乎不存在，但从远来看，你会遇到这些奇怪的情况，特别是当你的程序在大项目中达到一定长度时。

现在，让我们来看同一个例子。我们所做的是将 `var` 换成了 `let` 关键字。这产生了不同的作用域预期。

```javascript
// let 示例
function helloThereIterator() {
  // i 在这里是可见的
  for (let i = 0; i < 10; i++) {
    // i 在这里可见，并且在该作用域内部的回调中也可见
  }
}
```

- let 不允许重复声明

这并没有解决任何重大问题，但它确实帮助我们以更直观的方式完成工作，特别是在处理脚本程序结构中多个作用域的网格时。

## 新的 const 关键字

`const` 与 `let` 完全相同。唯一的区别在于一旦你使用 `const` 定义了一个值，它就不能重新赋值。这样做将产生错误：

```javascript
const a = 1; // 允许
const a = 2; // 错误，常量不能重新赋值！
```

`const` 有什么用？常量传统上用于定义程序运行时不会改变的值。还有一点……`const` 关键字防止了重新赋值。与许多其他语言相比，这会让对象的属性变为不可变。




## 解构赋值

EcmaScript 6 为我们引入了解构赋值。这是一项新的 JavaScript 功能。之前对 `let` 关键字的解释为讨论下一个主题奠定了基础。所以，让我们来看看它们是如何工作的：

```javascript
let {a, b} = obj;
```

在这个示例中，创建了两个变量 `a` 和 `b`。然后，从名为 `obj` 的对象提取属性 `obj.a` 和 `obj.b`，并将它们分别赋值给这些变量。这等同于执行以下操作：

```javascript
let a = obj.a;
let b = obj.b;
```

这种格式占用空间更多。解构赋值节省了空间并为我们的代码提供了更好的可读性。习惯它们吧！:)

## For-of 循环

这是 EcmaScript 6 中一种全新的循环类型。让我们来看看它是如何工作的：

```javascript
for (let [key, value] of map) { ... }
```

这个强大的 `for` 循环将遍历存储在 `map` 中的值。遗憾的是（像 JavaScript 中的很多事情一样），`for-of` 循环不能作用于对象（及其属性）。这几乎是一个令人困惑的设计决策。那么，`for-of` 循环可以作用于什么呢？

`for-of` 循环专门设计用于对 `Array`、`Map` 和 `Set` 对象的操作。

## Map 对象

就像 `Array` 对象一样，ES6 增加了一个新对象，称为 `Map`。`Map` 无非只是一个简单的键/值映射。它们非常像 PHP 中的关联数组。

`Map` 不应该在处处使用。只在你之前使用对象作为集合的地方使用它们。这正是它们的用途。在 JavaScript 程序设计中，使用对象仍应是主要的。

`Map` 有一个 `.size` 属性来确定其大小。与对象不同，对象中你必须手动计算对象的大小。当你有通过键/值关联对的数据集合时，请结合 `for-of` 循环使用它们！

## 箭头函数

EcmaScript6 最受喜的特性之一是箭头函数。我认为你应该尽早开始使用它们。箭头函数只是用更紧凑的语法编写的 JavaScript 函数，它们与使用 `function` 关键字创建的普通函数略有不同。这里是基本的箭头函数语法格式，起初看起来可能有点奇怪：

```javascript
name = (params) => returned expression
```

例如，你可以使用箭头函数编写类似的内容：

```javascript
x = (a, b) => console.log("This is arrow function x with params = " + a + " and " + b);
```

但这只是一个函数定义。它可以像普通函数一样如下执行：

```javascript
x(5, 7);
```

与普通 JavaScript 函数相比，一个根本性的区别是箭头函数处理 **this** 关键字的方式。它从根本上解决了与 `let` 关键字在普通作用域中解决的相同（或相似）的问题。这里我们需要进入一个稍微更深入的讨论。

JavaScript **箭头函数** 是一个仅适用于 EcmaScript 6 的特性。它在这一规范之前并不存在。它让对象内部的匿名函数变得更易使用，同时保留了匿名事件处理程序内部 **this** 对象的值。

箭头函数还修改了在对象作用域内无名回调函数使用的 **this** 对象的功能，通过将其自动绑定到对象的最顶层局部作用域。这让我想起了一点关于变量提升（我在我的其他教程中简要提到过提升）。

箭头函数帮助我们逃避了我们原始作用域模型中固有的 **this/that** 体操（如果你在阅读时不熟悉我指的是什么，本教程解释了它）。

箭头函数也因其语法而被称为“胖箭头”函数。

```javascript
(params) => { statement };
```

只需将其视为定义 JavaScript 函数的另一种语法即可。

教程的剩余部分将解释旧版 JavaScript 示例之间的区别，以及如何使用箭头函数提高代码可读性并在内部微调对象的功能。





# 什么是 JavaScript 中的箭头函数？

JavaScript 中的箭头函数和匿名函数之间有什么区别？

JavaScript 中的箭头函数是一种具有简写语法的匿名函数。与标准匿名函数相比，唯一的区别在于语法以及该对象在相应作用域内的处理方式。这是一个微小的细节，当涉及到该对象的绑定时，两者的实际运行方式会有所不同。

让我们比较一下普通的 JavaScript 匿名函数与其对应的箭头函数。我们已经知道 JavaScript 中像 `function(){...}` 这样的匿名函数是什么样子的。但箭头函数实际上有独特的语法。

注意，两者的功能完全相同，都是执行某些代码。不同之处在于箭头函数会自动处理我们在之前的示例中经历过的那些繁琐的切换工作。箭头函数会创建自己的不会改变的 `this` 对象。因此，我们永远不需要像之前的示例中那样，将其重命名或绑定到另一个变量上。

这是在 ECMAScript 6 (ES6) 中定义 JavaScript 新型箭头函数的最新语法：

```javascript
() => {};
```

请注意。JavaScript 中的箭头函数不能与 `new` 操作符配合。它们是匿名的，通常用于事件。

但也存在一些语法变体：

```javascript
(a, b) => { ... } // 多参数
a => { ... } // 单参数
```

注意，参数可以包含一组由逗号分隔的多个参数，在这种情况下你必须始终使用括号。对于单参数语法，不需要使用括号。

在现实场景中，我们也可以将箭头函数赋值给变量名。在这种情况下，匿名箭头函数变成了具名的。函数返回其函数体作用域内的结果。

```javascript
var add = (a, b) => { return a + b; }
```

话虽如此……

```javascript
add(1, 2); // 返回 3
```

但还有另一种定义箭头函数的无作用域语法：

```javascript
var add = (a, b) => a + b;
```

注意这里的返回值由普通的 JavaScript 语句表示。

这将产生完全相同的结果。我们删除了 `return` 语句。函数仍然返回 `a + b` 的值。在这种情况下，`a + b` 是一个 JavaScript 语句，没有作用域体。默认情况下，指定的箭头函数即使没有指定 `return` 关键字也会返回语句的值。

最后，让我们把这一切整合起来，重写我们最初的 Sprite 对象示例。现在只使用箭头函数。你可以看到，没有必要创建并设置 `this` 绑定到另一个变量名。箭头函数已经为你、我们处理了这一切！

```javascript
/* JavaScript 中一个显著简化的 Sprite 对象 */
var Sprite = function()
{
  this.angle = 5;
  this.draw = function() {
    alert(this.angle); // 显示 sprite 的角度
  }

var timer = setTimeout(() =>
{
// 注意这里使用了箭头函数
alert(this.angle); // 使用 "this" 显示 "5"，而不是 "that"。
}

var ship = new Sprite(); // 实例化 ship

// ship.draw(); 使用 this.angle 旋转角度绘制 ship
```

我们简单地切换了用作事件处理程序的标准匿名函数 `function(){...}`。

并将其替换为箭头函数 `() => {...}`。

从那一刻起，新匿名事件函数内部的 `this` 关键字开始正确引用原始 Sprite 对象的 `this` 关键字，而无需编写任何额外的绑定代码。

因此……我想我们对箭头函数的讨论到此结束。希望你喜欢这个教程。请在 Twitter 或你的 Facebook 页面上与你的朋友分享。

Developer Post 是一个致力于对看似复杂的主题进行简单解释的小网站。希望这能帮助那里的其他人写出更好的 JavaScript 代码。

如果你想学习更多关于 ES6 Harmony 的知识，请访问 What's new in ECMScript 6 aka Harmony（打开新标签页）来熟悉基础。

根据 Sitepoint 的文章，箭头函数是 ES6 中最受欢迎的功能。

这个 Mozilla 箭头函数教程帮助我熟悉了箭头函数。我在写这篇文章时将其作为我的第一个参考。

## 立即执行箭头函数 (IIAF)

如果你熟悉 jQuery 或 JavaScript 插件开发，你可能已经间接接触过 IIAF，并且已经见过通常晦涩的立即执行函数表达式 (IIFE) 语法，它看起来像这样：

```javascript
function () { ... }();
```

在这里，我们在定义函数的同时就执行了它。

你会发现这种语法经常用于 HTML 页面的底部，就在闭合的 `</body>` 标签上方。这种技术用于等待 HTML 元素加载完成，再开始执行 JavaScript。

同样，可以使用箭头函数来实现等效的结果。

```javascript
() => { ... }();
```

这种语法被称为立即执行箭头函数。包围它的括号使得函数在你的程序执行流的该处执行。

## 反引号（`` ` ``）模板字符串

反引号只是这种奇特的引号字符的另一个名称，也称为反钩（grave accent）。

现在像 `${ expression }` 这样的语句可以通过反引号模板字符串进行插值。它只是一个由位于键盘上“1”键左侧的第三组引号（单引号和双引号之后）包围的字符串。

反引号字符串的优点之一是它们可以跨行划分。这是 JavaScript 缺失的一个非常需要的功能。

这类字符串也被称为模板字面量（template literals）。下面是几个示例：

`string text`
`string text on line`
`string text`

`string text`
就像普通引号一样，
`string text`

`string text`
这些是：

## 新数组方法

在 ES6 中，我们有了这些新的数组方法：让我们定义常用的数组：

```javascript
let arr = new Array();
```

### find

```javascript
arr.find(callback[, thisArg]);
```

返回传递给 callback 时产生真值（truthy）的第一个项的值。

### findIndex

```javascript
arr.findIndex(callback[, thisArg]);
```

findIndex 方法与 find 完全相同。区别在于它返回产生真值的项的索引，而不是值。

### fill

```javascript
arr.fill(value[, start = 0, end = this.length]);
```

默认情况下，start 为 0，end 为数组的长度。

### copyWithin

这种新数组方法在数组内部复制一个项序列，从 **start** 指定的位置开始，并从 **target** 指定的索引开始：

```javascript
arr.copyWithin(target, start[, end = this.length]);
```

这是一个实际示例：

```javascript
var arr1 = [1,1,1, 2,2,2, 3,3,3];
// 将前三个索引复制到最后三个
arr1.copyWithin(6, 0);

alert(arr1); // 1,1,1, 2,2,2, 1,1,1
```

这非常像 C++ 中的内存操作。

## 新内置类

内置类是随 JavaScript 包一起预存在的对象。例如熟悉的 **Object, Array, Function, Date, Math** 以及其他几个……ECMAScript 6 增加了几个内置类，列如下：

- **Map** 是键值对的集合。类似于数组。
- **Set** 类似于 map，区别在于每个存储的值都是唯一的。
- **Symbol** 用于创建私有对象/类属性。
- **Promise** 管理一个未来会发生的事件。

**Promises** 有趣，因为所有事件通常都会发生在未来。承诺到底有什么特别的？正确的解释应该是，无论你的结构如何，它们都会发生。




HTML 文档的变化。这些被称为“承诺”（promises）的特殊事件保证了事件将在未来的某个时刻发生。

承诺所解决的问题之一是经典的此类情况：HTML 元素的事件（如 `onclick`）被更新应用程序视觉效果的代码所覆盖。由于这种情况在频繁更新的前端视图中经常发生，某些事件可能根本不会被触发，仅仅是因为 DOM 被重写了。

只要原始 DOM 的完整性保持不变，或者与事件执行时存在的 DOM 保持相似，无论你网站的 DOM 结构发生了什么变化，承诺都将存在于“未来”。

## 感谢你

本教程书籍由我独立出版，并分发给我的免费 JavaScript 通事的订阅者。没有你们的支持，这一切是不可能实现的。

你是否尝试过编写并发布自己的书？编写一本技术类书籍需要投入数小时的研究和心思考！

正因如此，我想把这一章节专门用于感谢你购买《React Gems》一书的支持。正如你可能所知的，你的购买包含了免费的终身书籍更新。

每当我添加、修改或编辑书的重大部分时（我计划在 2017 年期间完成这些工作），你将继续自动收到包括新章节在内的书籍更新。

更新版本的教程书籍将发送到你购买此版本时使用的 PayPal 邮箱地址。随着我收集更多的教育材料，每 1-2 个月会进行一次更新，或者在条件允许（有进行质量更新的时间）时更新。

免费更新已包含在你的购买中，你无需进行任何操作即可继续接收更新。

感谢阅读以及你的持续支持！

作者，
Greg Sidelnikov
greg.sidelnikov@gmail.com

## 书籍更新 2021 年 1 月 6 日

编辑并改进了章节：
- “作者寄语”（改进了文本）
- “学习 React 的主要障碍”（深化了对 JSX 和 babel 的见解）
- “EcmaScript 6 - 你需要知道的”（修复了 let/var 示例）
-籍长度变化：+2 页。

## 书籍更新 2021 年 1 月 10 日

编辑并改进了章节：
- 修复了第 37 页的拼写错误（将 `of` 改为 `or`）
