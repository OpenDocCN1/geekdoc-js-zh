# React.js 书籍：从零开始学习 JavaScript 库 React







![](img/7872743894e432d99205d370e86ceeae_0_0.png)



## 深入理解一个难以学习的 JavaScript 库

React 教程书籍

React 绝对是我在 JavaScript 库中遇到过的最难的内容之一。在某种程度上，因为它假设你已经掌握了许多与专业 Web 开发相关的知识。即：Node.js、精通 babel 命令行工具、EcmaScript (5 和 6)、JSX，以及可能还有 WebPack。

这本书还做了一个假设：即你对 React 编程是完全的新手。这对我这个作者来说是一个挑战，因为我的责任是用一种仍然有意义的方式来讲解 React，而不会用大块看起来复杂且难以理解的代码让你感到目不应接。

尽管如此，我在这本书呈现格式上的策略遵循一个简单的模式：将解释与简单的代码示例结合起来。主要来说，这是一本叙述性的著作，旨在逐步深入理解 React 库。

我现在就要直言：单凭这本书是不够成为 React 程序员专家的。任何关于 React 的出版物无法声称做到，因为为了入门并开始使用 React 编写真实的应用程序，你需要理解的原则范围极其广泛。此外，还有 EcmaScript 5、6 以及即将到来的 7 之间的语法差异。由于这个原因，React 在 JavaScript 可能会成为你经历过的最独特的学习体验之一。

但突破这些难点是值得的。我希望这本书在完成这一任务方面被证明是实用的。

Greg Sidelnikov 编写与编辑
greg.sidelnikov@gmail.com





完整的 React 应用程序示例 73
创建搜索列表 74
React 应用程序 74



# 作者寄语

欢迎阅读我书的介绍章节。
这是 Greg Sidelnikov 编写的《React Gems》这本书。

这就是我，作者！

首先，感谢你对《React Gems》感兴趣。这本教程书籍是我通过我的 JavaScript 开发时事自出版的。它将引导你一步步完成从设置开发环境到从头学习响应式编程的全过程。

截至 2017 年，我所谓的“响应式”编程已成为思考 Web 应用程序的替代方式。它提供了软件模式，使得你的 Web 应用程序对用户输入极其灵敏，通常让终端用户（使用你应用程序的人）感觉速度更快。

当我学习 React 时，我花了大约 3 周时间才开悟。React 与我编写过的任何其他 JavaScript 库都不同。它假设了大量的背景知识。正因如此，我必须以特定的方式写这本书，逐步深入理解它的过程。

学习 React 不仅仅是记忆这里那里几个方法并随心所欲地使用它们。React 本身构建在软件原则之上，这些原则通常只有在行业工作了很久的专业软件工程师才知道。

# 学习 React 的主要障碍

在这里，我将尝试探讨从零开始学习 React 时面临的常见困难。正是这些困难让 React 不像你所熟悉的那些直观库那样简单上手。

我会尝试这样做，而不让 React 看起来像是一个糟糕的选择……总而言之，这确实是一本关于如何成为 React 程序员的书中。然而，如果我们现在至少简短地谈谈这些困难部分，在我们之后向前移动时会更容易接受。

1. 新设计模式。新的，在许多情况下是不熟悉的。如果你是从传统的 2015 年之前的 JavaScript 编程世界来到 React，可能需要时间来适应 React 库采用的模块化和声明式设计。当然，如果你处理过大型 JavaScript 应用程序，可能已经处理过长长的 .js 文件列表并将其视为独立的模块。但对于大多数程序员来说事实并非如此。React 要求我们使用模块化设计来实现最大的应用程序管理效率。

2. JSX 语言让很多人感到困惑。它看起来像是在 JavaScript 中编写 HTML，对于初学者来说，看起来简直不可思议，如果你第一次遇到它：

```javascript
var divblocks = <div>
<div>另一个嵌套标签</div>
</div>;
```

就像，等等，你看到我看到的了吗？我们刚刚在 JavaScript 语句中不断输入了 HTML，没有给 HTML 加上引号，甚至使用了换行符将它们分开……而且还逃过罚。

JSX 处理器（像处理 HTML 一样处理 XML 并将其转换为我们可以使用的有效 JavaScript 语句）在幕后为我们完成了所有的脏活。实际上，这种代码是从 XML（看起来像

“编译”而来的。




将 HTML 转换为 EcmaScript 5，以便浏览器可以理解它。这意味着浏览器看到的实际代码甚至不是这种样子。这只是为了方便我们在编写应用程序时使用。但是……我们可以毫无障碍地以这种格式编写代码。

关于如何使用它将在全书中进行讨论。但基本上，这种格式与 React 组件结构是互换的。你刚刚创建的本质实际上是一个有效的 React 组件模式。

正因如此，JSX 经常作为辅助库与 React 一起使用。你可以通过使用 React 方法创建我们在上面示例中看到的相同语句。使用 JSX并不是强制要求的，你也可以不使用它运行。

然而，如果没有 React，编程就就像吃没加奶酪的披萨。两者共同工作可以提供美妙的体验，即使学习如何烘焙饼饼需要反复尝试。

- Babel & 从 EcmaScript 6 转译到较早版本（ES5）这有一点点额外开销，看起来似乎也是件没必要的事情。因为像 Chrome 和 Safari 等浏览器最终将对 ES6 提供完全支持，这个过程无论如何都会变成自动。

Babel 允许我们编写这样的代码：

```javascript
import someClass from "someClass.js";
```

这将从定义文件 `someClass.js` 中获取 `someClass` 类定义。在编写本文时，Chrome、Firefox 以及其他任何浏览器都不支持 ES6 import 关键字。

然而，babel 允许我们现在（现代浏览器推出官方支持之前）就开始学习和编写 ES6 代码。在此之前，它只会在后台将其“转译”回 ES5，以便代码在实际上可以在今天的任何浏览器中运行。

好消息是，安装 babel 插件会迫使你学习如何使用命令行工具。传统的 JavaScript 开发者通常不熟悉这些工具。我认为，这正是你应该学习的技能。

使用命令行是专业软件开发环境中的一项“必修”技能（除了在桌面某个任意文件夹中的个人项目之外）。而且……如果不采取这一步，它可能是可能阻止你直接深入响应式编程的额外步骤之一，尽管这可能很麻烦。

## 学习 React 的良好理由

- 1. **它很快。** 这可能是 JavaScript 程序员想要开始使用 React 库编写应用程序的首要原因。它利用 DOM 的虚拟副本，被设计为在渲染到标准 JavaScript DOM 树之前执行操作。这不仅仅是一个数字游戏。令人惊讶的是，将 UI 操作移动到虚拟 DOM 实际上改变了用户对应用程序的感受。你可能已经在 Netflix 等网站上注意到这种现象了。

- 2. **模块化设计。** React 支持模块化设计，这通常与构建大型可扩展的应用程序有关。2015 年发布的 EcmaScript 6 规范出现提供了有利于模块化方法的新语法，例如，`require` (ES5) 和 `import` (ES6) 关键字不仅将文件连接在一起，还假设了对象之间的类关系。尽管在编写本文时现代浏览器（即使是 Chrome）不支持 `import` 关键字，但我们可以通过使用 `require` 或将我们的 ES6 代码转译为 ES5 发送到浏览器进行渲染来开始编写模块化程序。当浏览器赶上时，我们就不再需要转译了。这种情况发生时，React 将成为随处可见的更常见的库。最终，无论是否有 React，模块化的 JavaScript 程序将成为常态。

- 3. **可扩展性。** 在 React 中，每个 HTML 元素都被视为一个可以嵌套在其他组件中的可编程组件。子组件与其父组件相关联。父组件和子组件之间的关系通过被称为 `props` 的东西建立。React 程序的的可扩展性通过让每个组件成为 HTML、CSS 和 JavaScript 代码的集合体来实现。

- 4. **灵活性。** React 不仅仅是一个 UI 视图库，与你开始了解它时可能听到的说法不同。虽然这并不完全错误。React 赋予了我们创建极速交互式组件的能力，这些组件可以作为我们应用程序的元素。然而，React 利用了渲染目标的原理，这允许你将代码的结果发送到几乎任何地方，包括但不限于前端视图。

- 5. **雇主中的流行度。** React 是 Facebook 的程序员在研究多年 Web 应用程序后开发的。多或少，它源于一组经过证明的软件工程哲学。尽管许多传统的 JavaScript 程序员可能并不熟悉其中的许多内容。当你学习 React 时，它将使你在行业中获得竞争优势。

## 什么是响应式编程？

到底什么是响应式编程？我们可以将使用 React 编程称为函数性模板化。不要与函数式语言混淆。我只是意味着你的 React 组件有一个特定的函数要执行，并且这是你用独特的功能自定义组件的方法。而 HTML 为我们提供了一组元素（如 HTML 标签）……后者是我在写这本书时采用的方法。我希望你喜欢这本书，学习 React 库并探索现代软件开发提供的可能性，这将训练你去制作现实世界的应用程序。

## 响应式编程的主要原则

在我们继续之前，提到我们在这里在做什么是重要的。我们可以将使用 React 编程称为函数性模板化。不要与函数式语言混淆。我只是意味着你的 React 组件有一个特定的函数要执行，并且这是你用独特的功能自定义组件的方法。而 HTML 为我们提供了一组元素（如 HTML 标签）来处理我们 Web 应用程序的布局并通过属性与 JavaScript 代码提供接口，React 是这些……以及更多。

React 程序通常不处理独立的 CSS 样式表。与的接口通过虚拟 DOM 提供。我们将在书中之后介绍它是如何工作的。

与传统的 HTML、CSS 和 JavaScript 方法相比（即我们必须在源代码中寻找网页上某一个元素的不同部分），React 为我们提供了一种使用可编程模板的方法。

在标准的基于 Ajax 的 HTML 应用程序中，我们习惯看到如下示例所示的代码：

```html
// HTML
<div class="LoginForm">
  <div class="Name">
    Enter username here.
  </div>
</div>
```





```javascript
$.ajax({ url: "/login.php",
  data: { "username": "user1",
    password": "abfgh123" },

  // login.php 返回了一些数据
  success: function(msg) {

    // 调整 DOM 数据
    $(".Name").html(msg);
  }
});
```

这是一个刻意简化的示例。但你可以看到，即使如此，代码也位于两个独立的块中。第一个是 HTML 布局定义。它几乎是一个带有某些动态功能的 LoginForm 可用模板。

第二个代码块是执行 Ajax 语句的实际程序。这行代码将根据传递给它的数据（用户名和密码）从 PHP 脚本加载数据，并在 `msg` 变量中返回某种消息。

最后，使用 jQuery 通过替换类名为 `Name` 的 div 内容为从脚本接收的消息来修改 DOM。

在一段时间内，这种方法工作得很好。在过去的几年里，这就是我们处理网页上动态元素的方式。但 React 的卓越之处在于，它获取了这一切，并赋予了我们对 HTML 和动态数据的程序化控制，且封装在一个整洁的 `render` 函数中：

```javascript
render: function() {
  return
  <div>
    {
      this.state.name ? this.state.name :
      <span>在此处输入用户名</span>
    }
  </div>
}
```

注意看 HTML 和 JavaScript 代码是如何交织在一起的，而无需打开单独的标签。它们都存在于同一个 JavaScript 语句中，并且几乎可以互换使用而没有任何任何问题。我们稍后会介绍这是如何实现的。

当然，这个孤立的示例在实际世界应用之外几乎没有任何意义。但它展示了几个重要的原则。

这段 React 代码从 JSX 语言中借用了 JavaScript 跨 HTML 的语法，让我们能够通过简短查看代码就看出动态元素的输出样式。React 在这里试图满足所有人的需求。在某些情况下，你会注意到一些模式，感觉就像是将后端逻辑带入了前端。

这个示例使用了三元运算符 `? :`。基本上，它的意思是如果属性名存在（不为 null 或 undefined），我们就应该输出它。如果不存在，我们应该输出通用的“在此处输入用户名”作为默认消息。

这把 HTML 方法论带到了另一个维度。在这里，我们同时在设计和编写组件。

# 宝石与矿井中工作

这只是第一章，我已经在深入研究 React 编程的复杂性了。然而，让我们回到基础，将一些重要的原则拆解成更小的教程片段。这将对我们以后的学习有所帮助。

就像我的《jQuery Gems（宝石）》这本书一样，我们将从一组“宝石”开始，这些是先备知识，将提供前进所需的快速、富有见解的碎片信息。由于软件行业目前正处于 EcmaScript 5 和 6 的过渡时期，这可以帮助我们解决掉常见的怪异问题，并在当我们学习书中其余课程时，保持关注在重要的事情上。

如果跳过了这些“宝石”，书的后面某些部分可能变得难以理解。特别是如果你将学习 React 作为你接触 JavaScript 编程的第一个尝试。

但“宝石”只是书的一部分。它们旨在减少许多动荡，并帮助你在响应式原则的提示下进入现代 JavaScript 编程的世界。

在深入矿井之前，你必须理解这些原则。宝石将磨利你的镐。书的第二部分将向你展示洞穴的其余部分。

# 掌中的 React

为了让你的旅程更加轻松，我在这里包含了这一部分，代表 React 程序的每个独立方面。系好安全带，准备好吸收许多新原则！我们现在真正要进入 React 编程的世界了 :)

这是一个俯瞰式的解释，涵盖了构建 React 程序所涉及的最重要概念。我已经提到过学习 React 是碎片化的。而且它假设你具备高级编程模式的知识。

在这一节中，我将尝试将它们拆分成可以单独分析的合理区块。随着我们的进行，这将帮助你把拼图碎片组合在一起。把这里描述的原则视为驱动 React 核心引擎的想法。

仅仅因为它们在这里被整齐地列出，并不意味着学习 React 会很容易。但通过花时间熟悉它们，确实会让阅读书的其余部分变得更容易。

## 核心要素

现在需要理解什么是 `createElement` 接收参数：type, props, children。

在这里，`type` 是元素的名称。例如 A、H1、DIV 等。

然后我们有 `props`，即你传递给此组件的属性。`Props` 不是状态（state），但它们可以修改状态。我们稍后会更详细地区分这一点。

最后，`children` 只是位于父元素内的层级元素。创建它们的链，并将它们直接输入 `createElement` 函数末尾的 N 个参数。

```javascript
let link = React.createElement('a', {href: '#'}, "Save");
let nav = React.createElement(MyNav, {flat: true}, link);
```

（注：由于原始文本存在大量 OCR 错误和重复，以上内容已基于核心逻辑进行了去重整合。）




一旦你真正开始它的工作原理，这部分才是真正有趣的地方。

所以，在 ES5 中，你会使用 `createElement` 函数，但在 JSX 中（可以说，它的常用用法是与其他 ES6 语法配合使用），你可以通过简单地写如下内容来实现完全相同的功能：

```
let link1 = <a href="#">Save</a>;
```

现在你明白我的意思了吗？JSX 将 HTML 转换为 JavaScript 语句。在这里`link1` 是元素的类对象表示，等同于我们之前用 `createElement` 方法创建的 React 代码。

是的，通过直接在 JSX 中声明它，`link1.href` 就会包含 "#"。当我意识到 JSX 是这样运作的时，它开始变得非常有意义，我实际上也开始习惯使用它了。

HTML 和 JavaScript 之间是一条双向道路，属性会自动变成属性。
这里有一个更复杂的例子，这次再次使用了 JSX：

```
let nav = <MyNav>
<a href="#">Save</a>
<a href="#">Load</a>
<a href="#">Delete</a>
<a href="#">
  <span alerts="0">No Alerts</span>
</a>
</MyNav>;
```

我们刚刚使用 JSX 语言通过 JavaScript 语句重新创建了虚拟 DOM！你可以将 `nav` 的值作为语句传递到函数中。这就像是创建微 DOM 结构的另一种方式。

现在你（希望）看到了这就是 React 中虚拟 DOM 的结构。它就像我们要处理的次级 DOM，我们将对其进行更改、修改、编辑、删除和添加子元素等。

我们将更新负责应用程序中可见元素的实际 JavaScript DOM 对象……但只有在它实际上需要更新时。我们执行的任何虚拟 DOM 操作都不会与花费时间更新原始 DOM 相关。这正是 React 应用提高性能的原因。

最棒的一点是，React 会自动我们完成这一切。作为一个 React 程序员，你不需要理解 React 内部是如何做到的。你只需要专注于应用程序的设计。

当然注意，你直接在 JavaScript 应用程序中输入 JSX，它甚至不会被编译。你必须运行 JSX 处理器。为了做到这一点，你通常从命令行初始化它，让它在后台持续运行。

Babel 是一个 JSX 插件。我也建议学习如何让 babel 处理你的文件。这意味着，你可以设置 babel，使得只要文件发生变化，它就会自动转译你的 js 文件（并将其放入 "build" 或 "production" 目录）。Babel 的功能被称为 "watch"。它必须先启用。我在视频教程中解释了如何在 Windows PC 上进行操作：

YouTube 上的 React 教程可以帮助你设置开发环境、安装 Node.js、NPM、babel、JSX 并帮助你开始监控你的文件：

https://www.youtube.com/watch?v=tXanVgcjEiE0

你可以简单地在网页顶部或底部的 `SCRIPT` 标签中添加 `babel.js` 来省事。JSX 会直接翻译。但这会显著减慢应用程序的处理速度。它应该用于测试。

另一方面，视频只有 58 分钟，如果你认真要设置一个专业的 Web 开发环境，我建议在 YouTube 播放器上开启 2 倍速快速浏览，这应该只需要 25 分钟。它就像一门入门介绍课程。

最后，我们通过展示你也可以使用 **cloneElement.** 来克隆元素来结束这次讨论。

```
React.cloneElement(element,props,children);
```

它的工作方式与 `createElement` 完全相同。只需将一个现有元素作为参数传递即可。然后，你传递给相应参数的任何 props 和 children 都将合并到原始元素上已有的属性中。这让人想起了传统面向对象编程中扩展对象的功能。在这里，我们在某种程度上模仿了 OOP 功能。

创建的元素现在可以实际渲染到 DOM 中。你不能渲染虚拟 DOM。`render` 函数是 React 库内部处理这一过程的魔法。在此时，我们的元素从虚拟 DOM “复制并粘贴”到屏幕上可见的实际 DOM 中。

React 在主 `ReactDOM` 对象上提供了 `render` 方法，如下所示。在响应式编程中，ReactDOM 是仅于 React 之后最重要的对象。

```
ReactDOM.render(reactElement, domContainerNode);
```

在这里，`domContainerNode` 是 `reactElement` 将被渲染、重新渲染或首次挂载（mount）的父元素。

如果你需要更新组件的属性，可以多次使用 `render`。

这里是真实场景可能的模样。在这个例子中，我们取了一个 ReactElement 并将其渲染到 DOM 节点上：

```
ReactDOM.render(
  React.createElement("div", document.getElementById("container"))
);
```

如果你有一个元素已经与变量名关联，你可以使用 `ReactDOM.findDOMNode` 查找它：

```
ReactDOM.findDOMNode(element);
```

该语句返回与给定元素关联的 DOM 节点。注意，只有在元素通过 `render` 方法渲染到 DOM 之后才会生效。在此之前，即使它已经创建，在 DOM 中也是无法找到。

## 特殊 Props

在这里我们将简要讨论特殊的 prop 名称，其中有几个。
这些应该被视为类似于 JavaScript 中的保留关键字，除了 React 之外。它们都有特殊的含义。

## Children

**children** 属性会被 **React.createElement** 自动添加到 `this.props` 中

## className

此属性对应于 HTML 的 class。

## htmlFor

与 **className** 相同，仅用于 "for"。

## key

**key** 属性唯一标识元素。

## ref

**ref** 属性接受一个回调函数：

## style

**style** 属性接受一个样式 对象。

## PropTypes

React 有一个特殊的属性叫做 PropTypes。类型检查是它的主要用途。随着你的应用程序变得巨大，类型检查可以帮助发现各种 bug。

这是一个例子。假设我们已经创建了一个名为 ReactDOM 的组件。在开发模式下，默认启用类型检查。在生产代码中实际上是没有开启的。

```
ReactComponent.propTypes = {
  name: React.PropTypes.string
};
```

React.PropTypes 的作用是开启对属性中存储的数据类型的验证。React 默认有许多数据验证器，如果将 Numeric 数据类型传递给定义为 String 的属性（如示例所示），你将在 Chrome 或其他浏览器的 JavaScript 控制台中看到警告。

React 中的 `propTypes` 定义如下：

- any
- array
- bool
- element
- func
- node
- number
- object
- string

## 类组件选项

在书的其余部分我们将更多地讨论组件。它们是 React 应用程序的构建模块。但请记住这是“掌中 React”部分！让我们简要概述 React 组件的完整范围、React 库默认提供的选项和方法。组件通过 React 对象上的 `createClass` 方法定义：

```
var MyComponent = React.createClass({
  displayName: 'MyComponent',

  /* 这是你 React 类的核心
     选项和生命周期方法将在这里编写 */

  render:function() {
    // 渲染后，返回一个新创建的元素
    return React.createElement(/* ... */);
  }

});
```

这是组件类的基本结构。

## 组件选项

组件持有 `propTypes` 对象和两个返回对象的方法：

- propTypes 映射属性名称到类型的对象
- getDefaultProps 返回对象的函数
- getInitialState 返回对象的函数

## 生命周期周期方法

- componentWillMount
- componentDidMount
- componentWillReceiveProps
- shouldComponentUpdate
- componentWillUpdate




- 6. componentDidUpdate
- 7. componentWillUnmount

这 7 个方法可以在你的 React 类中实现。并不是所有组件都需要使用这 7 个函数，这取决于你组件的用途。

每个方法基本上都是在 React 组件生命周期内的特定时间执行的事件。这些功能大部分都与检查组件的挂载和更新状态有关。

除了这些方法外，当然你也可以根据组件需要执行的操作添加你自己的自定义函数。

## 组件实例 (Component Instances)

组件实例是我们在上一节中看到的从类表示的实例化的对象。以下是关于它们实现的一些提示：

- 1. 组件内部的 **this** 关键字指向它本身。
- 2. 无状态函数组件没有组件实例。
- 3. 一个组件实例可能会跨越多个等效的 ReactElements 。

## 属性 (Properties)

- 1. 属性 `this.props` 包含了通过标签属性传递给 `React.createElement` 的 props。
- 2. `this.state` 属性包含由 `setState` 和 `getInitialState` 方法设置的状态。

## 方法 (Methods)

- 1. `setState(changes)` 将给定的更改应用于 *this.state*，以重新渲染 DOM 组件。
- 2. `forceUpdate()` 立即将组件渲染到 DOM。

## 秘籍 (Gems)

在这一节中，我将介绍几个扩展响应式编程的“秘籍”，并对一些重要的原理进行一些解释。每个秘籍都是对特定主题的深入讨论。

## 秘籍 1 - React 组件 (React Components)

组件是 React 应用的构建块。

由于 React 主要是为了考虑应用视图（交互式用户界面动态），因此 React 组件可以被视为构成 Web 应用程序的视觉区块。React 将每个组件视为一个可重用的模板。

在 React 中，每个组件都是 HTML、CSS 和 JavaScript 代码的组合，标识了你应用程序中的一个特定区块。

例如，这里是我从 React 组件的角度来看我的 Twitter 页面 @gregsidelnikov。

在程序上，React 组件遵循了 嵌套 HTML 标签的足迹。它们有父元素和子元素，且父元素也可以是层级链上另一个组件的子元素。

![](img/7872743894e432d99205d370e86ceeae_33_0.png)

将组件设计想象为你整个应用程序的蓝图。在为你的响应式应用编写第一行代码之前，在纸上规划出一切是一个极好的主意。这是一种直观的方法，将你的页面设计视为一个具有独特元素的 Web 应用程序来思考。

就像你当年第一次学习普通的 DOM 并意识到每个 HTML 元素（如 P、DIV、TABLE 等）实际上是对象模型长树链中的一个对象一样，把 React 组件看作与某种软件函数关联的视觉区域吧。这一次，这种功能将由你和你的应用程序需求来自定义决定。

从这些 React 的最基本原理中，你现在可以看到为什么 Facebook 和 Instagram 喜欢使用它。它速度极快，可以帮助将类似流的元素拆分为由组件组成的软件块，而这些组件只是 CSS、HTML 和 JavaScript 代码的组合。这种设计模型更接近 App 的行为，而不仅仅是使用表格类布局的信息性网站。

组件是层级化的。它们可以是其他组件的子元素。在大多数情况下，组件是为你的应用程序中的重用而定制的。它们包含了可以适应各种情况的代码模式。React 代码通常遵循创建这些组件链的模式，它们在内部工作，同时保持了快速的渲染速度和灵活性。

## 秘籍 2 - 渲染方法 (Render Method)

很有可能在构建普通的 HTML-JavaScript 应用时，你已经在某种程度上将应用拆分成不同的隔间。然后，你使用 Ajax 根据每个 HTML 元素单元格中更改的数据类型单独填充每个视图。

但 React 将这种方法又进一步了一步，要求 `render()`。`render` 方法必须附加在你创建的每个 React 组件上。没有办法绕过它。它是 React 组件所要求的使用的模式的一部分。

尽管 React 不仅仅是视图层——使得在使用 React 编程时 `render` 方法变得显式——但这正是 React 被认为主要是一个基于视图的库的原因。我们将在整书中看到为什么这是真的，以及为什么这并不完全正确。

说 React 编程仅仅是视图编程是不公平的。事实上，渲染目标的选择告诉我们相反的结论：React 是一种遵循基本哲学的编程模式，这种哲学实际上不需要视图。

你可以将 React 组件的结果渲染到浏览器或渲染到文本字符串（使用专门为此创建的方法，称为 `React.toString()`）、JSON 对象或你希望任何地方。在这种情况下，渲染根本不是渲染。因为“渲染（render）”这个词意味着数据可视化。React 更像一套原则，而不是许多初学者在熟悉该库之前倾向于认为的“创建用户界面的方法”。

虽然你可以在 React 之外使用任何第三方库（例如数据库 IO 库），但 React 在视图元素背后的自定义编程方面仍然提供了。事实上，它要求你理解这些编程原理是如何工作的。

`render()` 方法通常附加到 React 自己的“虚拟”DOM 上，当你的应用程序首次加载到浏览器时执行该方法。但这里是有趣的地方。我们将在秘籍 6 中更详细地介绍挂载（mounting）。

虚拟 DOM 无疑是选择 React 库编写应用程序的最大优势之一。事实上，当你将 react 库添加到你的 Web 项目时，你有必要添加 `react-dom` 库。这两者是不可分割的。而且所有响应式 JavaScript 应用默认都包含 React 库。

（注：原文此处存在大量重复段落，译文已根据要求去重并仅保留核心逻辑翻译）

The method render() which is usually attached to React's own "virtual" DOM is the method that will be executed when your application is loaded into the browser for the first time. But this is where it gets interesting. We'll cover mounting in greater detail in Gem 6.

The Virtual DOM is hands down one of the greatest advantages of choosing to write your application with the React library. In fact, when you add react library to your web project, it behooves you to add react dom library. The two are inseparable. And all reactive JavaScript applications by default also include React library.

（重复内容略）

## 秘籍 3 - 虚拟 DOM 和带宽 (Virtual DOM and Bandwidth)

虚拟 DOM 无疑是选择 React 库编写应用程序的最大优势之一。事实上，当你将 react 库添加到你的 Web 项目时，你有必要添加 `react-dom` 库。这两者是不可分割的。而且所有响应式 JavaScript 应用默认都包含 React 库。

React 让我们彻底思考元素代表什么，因为每个组件都与某种软件函数关联。这是你的应用程序首次加载到浏览器时。但这里是有趣的地方。我们将在秘籍 6 中更详细地介绍挂载。

应用程序即时响应，只有当数据应该更新时。

（重复内容略）

[content]
- 6. componentDidUpdate
- 7. componentWillUnmount

这 7 个方法可以在你的 React 类中实现。并不是所有组件都需要使用这 7 个函数，这取决于你组件的用途。

每个方法基本上都是在 React 组件生命周期内的特定时间执行的事件。这些功能大部分都与检查组件的挂载和更新状态有关。

除了这些方法外，你也可以根据组件需要执行的操作添加你自己的自定义函数。

## 组件实例 (Component Instances)

组件实例是我们在上一节中看到的从类表示的实例化的对象。以下是关于它们实现的一些提示：

- 1. 组件内部的 **this** 关键字指向它本身。
- 2. 无状态函数组件没有组件实例。
- 3. 一个组件实例可能会跨越多个等效的 ReactElements 。

## 属性 (Properties)

- 1. 属性 `this.props` 包含了通过标签属性传递给 `React.createElement` 的 props。
- 2. `this.state` 属性包含由 `setState` 和 `getInitialState` 方法设置的状态。

## 方法 (Methods)

- 1. `setState(changes)` 将给定的更改应用于 *this.state*，以重新渲染 DOM 组件。
- 2. `forceUpdate()` 立即将组件渲染到 DOM。

## 秘籍 (Gems)

在这一节中，我将介绍几个扩展响应式编程的“秘籍”，并对一些重要的原理进行一些解释。每个秘籍都是对特定主题的深入讨论。

## 秘籍 1 - React 组件 (React Components)

组件是 React 应用的构建块。

由于 React 主要是为了考虑应用视图（交互式用户界面动态），因此 React 组件可以被视为构成 Web 应用程序的视觉区块。React 将每个组件视为一个可重用的模板。

在 React 中，每个组件都是 HTML、CSS 和 JavaScript 代码的组合，标识了你应用程序中的一个特定区块。

例如，这里是我从 React 组件的角度来看我的 Twitter 页面 @gregsidelnikov。

在程序上，React 组件遵循了 嵌套 HTML 标签的足迹。它们有父元素和子元素，且父元素也可以是层级链上另一个组件的子元素。

将组件设计想象为你整个应用程序的蓝图。在为你的响应式应用编写第一行代码之前，在纸上规划出一切是一个极好的主意。这是一种直观的方法，将你的页面设计视为一个具有独特元素的 Web 应用程序来思考。

就像你当年第一次学习普通的 DOM 并意识到每个 HTML 元素（如 P、DIV、TABLE 等）实际上是对象模型长树链中的一个对象一样，把 React 组件看作与某种软件函数关联的视觉区域吧。这一次，这种功能将由你和你的应用程序需求来自定义决定。

从这些 React 的最基本原理中，你现在可以看到为什么 Facebook 和 Instagram 喜欢使用它。它速度极快，可以帮助将类似流的元素拆分为由组件组成的软件块，而这些组件只是 CSS、HTML 和 JavaScript 代码的组合。这种设计模型更接近 App 的行为，而不仅仅是使用表格类布局的信息性网站。

组件是层级化的。它们可以是其他组件的子元素。在大多数情况下，组件是为你的应用程序中的重用而定制的。它们包含了可以适应各种情况的代码模式。React 代码通常遵循创建这些组件链的模式，它们在内部工作，同时保持了快速的渲染速度和灵活性。

## 秘籍 2 - 渲染方法 (Render Method)

很有可能在构建普通的 HTML-JavaScript 应用时，你已经在某种程度上将应用拆分成不同的隔间。然后，你使用 Ajax 根据每个 HTML 元素单元格中更改的数据类型单独填充每个视图。

但 React 将这种方法又进一步了一步，要求 `render()`。`render` 方法必须附加在你创建的每个 React 组件上。没有办法绕过它。它是 React 组件所要求的使用的模式的一部分。

尽管 React 不仅仅是视图层——使得在使用 React 编程时 `render` 方法变得显式——但这正是 React 被认为主要是一个基于视图的库的原因。我们将在整书中看到为什么这是真的，以及为什么这并不完全正确。

说 React 编程仅仅是视图编程是不公平的。事实上，渲染目标的选择告诉我们相反的结论：React 是一种遵循基本哲学的编程模式，这种哲学实际上不需要视图。

你可以将 React 组件的结果渲染到浏览器或渲染到文本字符串（使用专门为此创建的方法，称为 `React.toString()`）、JSON 对象或你希望任何地方。在这种情况下，渲染根本不是渲染。因为“渲染（render）”这个词意味着数据可视化。React 更像一套原则，而不是许多初学者在熟悉该库之前倾向于认为的“创建用户界面的方法”。

虽然你可以在 React 之外使用任何第三方库（例如数据库 IO 库），但 React 在视图元素背后的自定义编程方面仍然提供了。事实上，它要求你理解这些编程原理是如何工作的。

`render()` 方法通常附加到 React 自己的“虚拟”DOM 上，当你的应用程序首次加载到浏览器时执行该方法。但这里是有趣的地方。我们将在秘籍 6 中更详细地介绍挂载。

虚拟 DOM 无疑是选择 React 库编写应用程序的最大优势之一。事实上，当你将 react 库添加到你的 Web 项目时，你有必要添加 `react-dom` 库。这两者是不可分割的。而且所有响应式 JavaScript 应用默认都包含 React 库。

（重复内容略）


例如，仅仅因为一个按钮点击事件就进行转换，或者不进行转换。

当然，像 Netflix 和 Amazon 这样的网站会预加载部分数据（例如电影预告片的前 15 秒），无论用户是否点击了播放按钮。但与其他“响应式”原则结合时，它对 UI 响应速度产生了巨大的影响。

我们仍然在使用熟悉的 HTML 元素来构建应用，但对每个事件的响应速率是由一个显著比 jQuery 实现快得多的 DOM 提供的。

要开始使用虚拟 DOM，你不需要做任何特殊操作。通过利用 React 组件模板模式，你会自动使用 React 自身的虚拟 DOM 遍历。它通过提供驼峰命名法（如 `className` 和 `fontFamily`）方法和属性，来匹配我们已经熟悉的名称，从而透明地模拟了标准的 DOM 模型。

## Gem 4 - 初始化 React 类的两种不同方式

在本书编写期间，Web 仍处于从 ECMAScript5 向 ECMAScript6 过渡时期。当 ECMAScript 2015 (ES6) 在大约两年前发布时，它在 JavaScript 世界引起了巨大的动荡，并将程序员分成了“老派”和“新派”两类。有些人根据情况倾向于使用其中一种风格而非另一种，这没有任何问题。两者并无优劣之分。

然而，最终 ES5 和 ES6 执行的是完全相同的代码。大部分区别在于语法上。诚然，同时在两种不同的语言中工作可能会产生不必要的困扰，特别是当你第一次学习 React 时。

在像 JavaScript 这样一种弱类型语言中，做任何事情都不存在所谓的“唯一标准方法”。情况一直如此。

在创建 React 组件时，做出这种区分至关重要。实现它并没有一种方法。

在本节中，我将演示如何用两种不同的方式创建两个完全相同的 React 组件。这里的区别在于 ECMAScript5 和 ECMAScript6 本身的区别。

在大多数情况下，一个显著的区别在于构造函数 (ES6) 和专门的初始化状态方法 (ES5) 的用法。让我们来看看。

ECMAScript5 示例如下：

```javascript
var NewComponent = React.createClass({
  getInitialState() {
    return { /* initial state */ };
  }
});
```

注意，在 ECMAScript5 中不存在 `constructor` 关键字。这就是为什么在这种情况下 React 提供了 `getInitialState` 函数。如果你用 ES5 编写应用，你应该使用此方法来初始化组件的默认状态。

我们稍后会讨论状态，因为这是一个非常重要的主题。状态与 React 组件紧密相关。在规划应用时，你应该在组件及其状态之间建立一种心理关联。每个组件都负责拥有一个状态。

上面演示了 ES5 语法。我不会告诉你应该使用两者中的哪一个。

最终，ES6 将在未来几年内成为新被采纳的标准，但许多程序员仍然偏好 ES5 的格式化。由于 JavaScript 支持 ES5 作为 ES6 的子集以兼容未来的应用，这两种仍然可以工作。

如果这对你有效，请像下面所示那样使用 ECMAScript6，现在使用了 ES5 中不可用的新关键字：`class`、`extends`、`super` 和 `constructor`：

```javascript
class NewComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { /* initial state */ };
  }
}
```

这本质是一样的，只是使用了 ES6 语法。如果你来自 Java、C# 或 C++ 语言，你可能更熟悉这种类创建语法，并可能认为它优于过时的 ES5 格式。

这里的另一个区别是我们使用 `.Component` 方法来创建组件，而不是 `.createClass`。但本质上，底层发生的是完全相同的事情。

我知道用两种不同的方法做同样的事情听起来很困惑。但在这里你有选择：使用 ES5 让你的代码在所有浏览器中即箱运行，或者使用 ES6 语法并将其转换回 ES5。然而，学习较新的 ES6 语法的优势是，你的应用程序看起来会更整洁、更直观。

这只是我们目前在 JavaScript 规范成熟过程中所面临的时期。在浏览器完全采用 ECMAScript 6 之前，学习这种语法格式可以给你带来优势，让你学习到一些尚未广泛使用、但在未来几年内绝对会成为下一个标准的内容。

我个人的倾向是开始使用 ECMAScript 6 语法。这条路可能会有些坎坷，但为了在成为更优秀的 JavaScript 程序员方面保持领先，这是一件明智的事。而且这类事情总是需要辛水努力的努力。好消息是，一旦你过了学习曲线，这将变成你的本能。

## Gem 5 - 状态与生命周期

在 React 中，每个组件都有一个状态。状态是一个带有值的对象。状态正如其听起来的那样。它是组件在一个或多个标记、参数和设置方面的状态，通常由数字、布尔值、数组或映射指定。

React 组件的生命周期与状态很大很大。React 提供了几个默认方法来帮助我们编写高效的应用。下面简要概述了这些方法。

每个组件通常会通过以下方法控制自己的状态。这些方法的设计用于在应用流程或组件状态的特定时刻修改或更新组件的状态。

```javascript
var MyComponent = React.createClass({
  displayName: 'MyComponent',
  getInitialState: function() {
    // ...
  },
  componentWillMount: function() {
    // ...
  },
  componentDidMount: function() {
    // ...
  },
  componentWillUnmount: function() {
    // ...
  },
  componentWillReceiveProps: function() {
    // ...
  },
  componentWillUpdate: function() {
    // ...
  },
  componentDidUpdate: function() {
    // ...
  },
  shouldComponentUpdate: function() {
    // ...
  },
  render: function() {
    // 将组件渲染到 DOM
    return null;
  }
});
```

| 方法 |  |
| :--- | :--- |
| `getInitialState` | 在组件渲染之前调用。有时与构造函数同义使用。 |
| `componentWillMount` | 在 `render()` 之前调用一次。它之后不会再次被调用。 |
| `componentDidMount` | 在组件首次渲染后立即调用。 |
| `componentWillUnmount` | 在组件即将销毁时调用。这是清理内存和删除状态的地方。 |
| `componentWillReceiveProps` | 当属性传递给组件时调用。 |
| `componentWillUpdate` | 在执行 `render` 方法之前立即调用。 |
| `componentDidUpdate` | 在 `render()` 方法更新 DOM 之后不久调用。 |
| `shouldComponentUpdate` | 一个始终返回 `true` 的默认方法。让我们控制组件元素是否应该更新。 |





## Gem 6 - 组件挂载 (Component Mounting)

React 是一个重视编程原则的库。其中之一是将组件视为元素的理念。组件是一种程序化（声明式）的方式，用于在应用程序中渲染你想要的内容。

但 React 实际上并不关心你选择在何处或如何渲染这些元素。无论是 JavaScript DOM 还是其他地方。这听起来可能令人惊讶，因为 React 以主要作为一个前端库而闻名。

这是因为 React 使用了被称为“渲染目标”（render targets）的东西。也就是说，你决定了 React 渲染方法的结果将如何被显示或传递到其他地方。

换句话说，你可以说 React 对于存储在其组件内部的数据或状态的输出是“不可感知”（agnostic）的。

例如……你可以将数据从组件输出到文件写入函数中。换句话说，React 的渲染目标不仅限于 UI 元素，尽管本书的大部分内容以及通用的 React 风格编程都是你大部分时间里会处理的 UI 元素。

在之前的 Gem 中，我们讨论了每个组件如何处理自己的状态。状态可以是一个布尔标记，指示按钮是否被高亮，或者导航菜单选项是否被选中。

现在，如果你一直在关注，那么这里就是一切开始汇合的地方。一个 React 组件是状态与其渲染方法的融合。我们在一个地方获得了对 UI 元素最重要的两个函数的程序化控制。

但“挂载”（mounting）到底是什么意思？在 React 中，出于性能考虑，我们使用了 DOM 的虚拟表示形式。

只需创建一个组件，任何 DOM 元素都不会被触及。这是一个极好的消息，但这怎么可能呢？这是因为使用原生 DOM 会增加我们应用程序的内存占用。然而，通过 React 的虚拟 DOM，元素只有在应用程序需要使用时才被创建。

我将详细解释这一点。

React 是一个同构框架（isomorphic framework）。它的功能可以映射到任意输出，而不仅仅是 JSX 风格的 UI 元素。

react 库提供的虚拟 DOM 正如其名：虚拟的。在它真正被应用程序需要之前，它物理上并不存在于真实的 JavaScript DOM 中。

想一想，JavaScript 的 DOM 是存储在内存中的 HTML 元素的物理树。它在页面加载到你的浏览器时被填充。

通常，当页面加载到 Web 应用程序时，每个由 HTML 元素标签表示的 DOM 分支，无论它将如何被使用，或者是否会显示在屏幕上，都会加载到主 DOM 元素中。页脚会被加载到 DOM 中，即使它显示在书折下方。

相反，React 甚至不会触碰 DOM 树。正如在之前的 Gem 中讨论过的，它在其自己的虚拟 DOM 中添加或删除组件，而虚拟 DOM 是完全存储在内存中的。元素通常在组件在你的应用程序中被特意使用时，在渲染目标的内存中产生物理表示。这几乎就像将虚拟 DOM 复制并粘贴到渲染目标（无论目标是什么）。在 Web 应用程序的情况下，它就是 JavaScript DOM 树。

我将通过以下示例来演示：

```javascript
var component = React.createElement(ComponentDefinition) );
```

此时，`component` 是 React 类型 `ComponentDefinition` 的实例，这是我为了这个示例而虚构的。在现实中，它会对应于像 `LoginScreen`、`NavigationMenu` 或 `Button` 这样的组件。它包含了我们在书中之前的 Gem 中已经过的标准组件定义代码。

它仅仅是一个 React 类型。它在主 JavaScript 文档 (DOM) 对象中尚未物理存在。除了作为一个 React 节点之外，在其他任何地方都找不到它。这是因为就其在你的应用程序中显示而言，它还没有物理用途。

但只有当在此组件上执行渲染方法时，这一点才是真的。在这里，`container` 只是某个 DIV 或其他 HTML 元素：

```javascript
React.render(component, container);
```

渲染方法将此组件挂载到 DOM 上。这个过程被称为“挂载”（mounting）的原因类似于虚拟硬盘。如果你曾经在计算机上挂载过虚拟 CD-ROM 或硬盘硬盘，你就知道它是如何工作的了。硬盘在物理上并不存在。出于相同的原因，这就是为什么这类软件被称为虚拟硬盘或虚拟 CD-ROM。而这就是为什么虚拟驱动器有“挂载你的驱动器”这样的功能。

同样，这是 React 中虚拟 DOM 背后的相同原理。在被挂载之前，无法对其进行操作。这使得 React 比常规的 DOM 操作快得多。这可能也是使用 React 的首要原因之一。React 存储了 DOM 的快速内存表示。

但这个虚拟 DOM 甚至没有与 JavaScript 的 DOM 关联。它并排存在，只有在变得必要时才渲染到屏幕上的实际 DOM。通常，当代表元素的组件用新传入的数据进行更新时。

本质上，React 的设计目标是仅在需要时才更新屏幕上的组件。这种做法的另一个优势是，它将你的应用程序与后端分离，同时有效地执行负责更新屏幕的函数，几乎在它们发生的瞬间完成。

你选择什么作为后端和前端之间的通信桥梁完全由你决定。React并不在乎这个。它的目的严格限于尽可能快地更新视图。

这种挂载机制使 React 成为一个多功能的库。因为在基本原理上，React 也不关心最终结果是渲染在 DOM 中还是在其他地方。

你可以将 React 的输出渲染到 XML 文档，将其视为自定义数据，或返回一个 JSON。这使得 React 成为编写用户界面以及折腾软件实现的一个极其强大的工具。

现在，很有可能如果你是从传统的 2015 年之前的 JavaScript 背景转向 React，学习 React 包含不仅仅是 React 库。它涉及到学习软件开发原则，而不是一组方法名，你就准备好了！不过，它确实有一些在 React 开发者之间变得标准的方法。我们将在后文中探索它们。

## Gem 7 - Node.js & NPM

当我学习 React 包含不仅仅是 React 库时，这无疑是正确的。至少，使用 React 开发需要你安装 Node 库。

关于 Node 本身就可以写一整本书，但对于 React 库，我们需要安装它有几个原因：

- 为我们的 React 应用程序提供本地环境。安装 Node 让你能够从本地的 localhost 运行应用程序。
- Node 自动带有 Babel 和 JSX 支持（JSX 作为 Babel 插件安装的）。

安装 Node 和 NPM 在 Mac（通过终端）和 PC 上都异常简单。在 PC 上，只需从官方网站下载 Node 安装文件即可。运行安装程序，你就搞定了。只需不要忘记在安装期间勾选该框，这样它也被包含了。

在 Mac 上，你可以通过命令行下载 Node。打开你的终端应用程序并输入：

```bash
$ wget http://nodejs.org/dist/node-v0.4.4.tar.gz

$ tar -xzf node-v0.4.4.tar.gz

$ cd node-v0.4.4

$ ./configure

$ sudo make install
```

这就！配置日志将运行，然后你就完成了。




目前到此，node 已经安装并准备好使用了，为我们提供了一个 localhost http 地址，我们可以在那里测试 React 代码。

不过，好消息是，如果你已经在本地机器上安装了 Apache 服务器，并且它已经映射到了你的开发文件夹，那么就没有必要使用 node 来提供本地环境了。你已经拥有了。

在这种情况下，你可以直接在现有的 Apache httpdoc 文件夹（或它映射到你机器上的任何其他文件夹）中编写 React 程序。只需在该目录下创建一个新文件夹，例如 "my-react-app"，然后像往常一样，你的项目将可以通过类似地址在浏览器访问：

```
http://localhost/my-react-app
```

但是，强烈建议你安装 Node。出于某些原因，因为它附带了命令行版本的 Babel 以及 JSX 插件，这些对于适当的开发设置是必不可少的。

在 Mac 的终端上安装其实非常简单。但在 PC 上会稍微有点挑战性，特别是如果你以前从未做过这类事情。

如果你仍然不确定在 PC 上如何操作，我在 YouTube 上录制了一个 58 分钟的补充教程，可以在以下地址免费观看：

# React JS Tutorial 1 - For Beginners | ReactJS JavaScript ES6 Node.js, NPM, Babel Transpiler, Webpack

```
https://www.youtube.com/watch?v=tXaNvGcjEi0
```

无论你处于开发过程的哪个阶段，这个视频都值得一看。但如果你是初学者，这是必看的。

观看这个教程应该可以帮助你通过 localhost 地址在 PC 上开始编写 React 应用。因此，在视频教程中，我将逐步演示整个过程。我不想在书中向你重写这些细节。你可以以 2 倍速速观看，大约只需要 25 分钟就能看完。

## Gem 8 - JSX 深度解析

如果你已经开始学习 React，你应该听过很多关于 JSX 的介绍。你可能也听过在 React 中并不必须使用它。这确实如此。但建议你使用它。它能让事情变得简单得多，尽管它的语法对传统的 JavaScript 开发者来说初看起来可能有点吓人。

JSX 以一种允许你“在 JavaScript 内部编写 HTML”的语言而闻名。这在某种程度上是正确的。预期的效果是我们可以将 HTML 标签视为 JavaScript 语句。然而， JSX 实际上使用的是一种形式的 XML，它只是看起来像 HTML，因为它使用了与标准 HTML 标签匹配的标签名称，如 DIV、UL、TABLE 等。记住，HTML 只是 XML 的远远兄弟。

虽然 HTML 初看起来可能有点像“恐龙”，但一旦你掌握了这一概念并习惯了它，它就会变成你的本能。这绝对是完全全新的，而且通常不会这样做（在今天的大多数浏览器中甚至无法编译），但让我们来看看它实际上长什么样：

```
var highScore = { Player1: 10, Player2: 25 };

<div className="class" />

<SomeCounter count = { 3 + 5 } />

<ScoreBoardUnit data-index="2">
  <h1>Score Leaderboard</h1>
  <ScoreBoard className="results" scores={scoreBoard} />
</ScoreBoardUnit>
```

这段代码在标准浏览器中自然无法编译，除非 Babel 的 JSX 插件帮助我们将其转换回 ES5（这是我们可以确定所有现代浏览器都能理解的规范）。在这种情况下，它将编译成如下 React 元素：

```
var scoreBoard = { Player1: 10, Player2: 25 };

React.createElement('div', { className:'class1' }, null)

React.createElement(SomeCounter, { count: 3 + 5 }, null)

React.createElement(ScoreBoardUnit, { 'data-index': 2 },
  React.createElement('h1', {}, 'Scoreboard'),
  React.createElement(Scoreboard, {
    className: 'result',
    Scores:scoreBoard }, null)
)
// close React.createElement(ScoreBoardUnit...)
```

这些 JSX 和 React 代码示例可以等同使用。只要你在后台对代码进行 JSX 编译，它就能工作，且你可以在两者之间切换。JSX 强烈建议与 React 结合使用，它对于使用或编译 React 程序并不是必须的。如果你必须这样做，直接使用没有 JSX 的 `createElement` 语法即可。

然而，如果你想正确处理，并开始编译过程，我建议观看 Gem 7 中的教程，以熟悉通过 Babel 进行编译过程的复杂性。

设置 Babel 和 JSX 需要一点耐心，但非常值得。只需观看视频教程，并按照说明在你的自己的机器上进行设置。

一旦你的文件被积极编译为 ES5，你就可以在自己的程序中使用 JSX 了。

如从上面的示例所示，这就像是在编写 HTML 标签的同时将它们视为 JavaScript 语句。当然，这段代码发生在某个 .js 文件内部。这不是 HTML。

注意 DashboardUnity 真的只是一个 XML 标签。它包含子元素，正如你对任何其他标准 XML 代码所预期那样。之所以有效是因为它被 JSX 语言处理机制处理。这有点像学习一种新语言，但因为你可能已经知道 HTML 语法，所以理解起来并不困难。

唯一的区别是花括号 `{ }` 现在也可以用于 JSX 语句中的标签属性名下。整个 `Scoreboard` 标签被视为一个对象。它的属性 `score` 是它的属性，包含了早早在代码中通过 JavaScript 对象 `score Board` 指定的值，而 `score Board` 是创建对象的 JSON 字面量对象表示法。

起初看起来可能有点奇怪，但它让你对应用程序拥有巨大的控制力。它将 `document.getElementById`（或 jQuery 中等效的 `$("#id").attr("scores")`——即你否则必须使用来访问属性的方法——统一到了一种新格式。

这种格式允许不直接将属性写入你的 HTML 元素（JSX）中并将其赋值给已存在的变量/对象，而且将 HTML 本身视为 JavaScript 语句。这太棒了，因为想象你可以从函数作为 JavaScript 语句返回 HTML 代码，然后将其传递给应用程序中的其他抽象方法。这就像是在函数之间投递 HTML，并为在应用程序的某个容器中进行输出做准备。

有一点。你会发现 JSX 使用 `className` 而不是传统 DOM 对象中的 `"class"`。JSX 文档对此解释为：“由于 JSX 是 JavaScript，因此不建议将 `class` 和 `for` 这样的标识符作为属性名。”这就是为什么 JS 中有 `className`，而 `for` 对应 `htmlFor`。

要学习 JSX，你应该查看官方文档。再次强调，可以专门为这个主题再写一本书，而我们正试图让你掌握基础知识，以便我们可以在这本书的其余部分重点关注 React。

# 编写 React.js 应用

欢迎来到 Gems 的第二部分。在本节中，我们将抛弃 Gem 的格式，因为书的第一部分旨在让你简单熟悉 React 编程和现代软件开发的最常见原则。

这些理论将帮助我们研究使用 React 进行编程的实践方面。所以，让我们开始吧，从编写你的第一个 React 组件开始。

## 课程 1 - 编写你的第一个 React 组件

下面你看到的是你可能编写的最第一个 React 组件样样的紧凑示例。它只是将通用的 Hello World 消息渲染到 DIV 元素中。它只需要一行代码。

```
React.createClass({render: function() {
  return (
    <div>Hello World.</div>
  )
});
```

在这里，我们正在使用 `React` 库对象的 `createClass` 方法。这就是创建组件的方式。但这段蓝色的代码是什么呢？它看起来像 HTML，但周围没有双引号！

组件通常存储在变量中。

例如：

```
var HelloWorld = React.createClass({ .. });
```

将组件存储在变量名中可以帮助我们以后在元素之间创建父子关联。这只是一种以程序化的方式在嵌套组件之间建立关系的方法。



墙上的一块石头。

在 React 中，我们可以在 JavaScript 内部编写 HTML。这与我们多年年来习惯的“在 HTML 中编写 JavaScript”的传统观念相反，在传统模式中，我们会在 HTML 的属性标签中编写 JavaScript（例如 `onclick="this.style.color='red'"`）。

但 React 给了我们反向操作的能力。我们将发现如何继续前进。现在，让我们扩展一下组件的内容，我将简要解释一下 JSX 如何帮助我们处理 HTML 块并将其视为返回值。

话如此……让我们来看创建第一个 React 组件的完整示例，并在一个特定的 HTML 元素中渲染其内容：

```javascript
// 添加必需的库代码
var React = require("react");

var ReactDOM = require("react-dom");

// 创建我们的第一个 react 组件 "HelloWorld"
var HelloWorld = React.createClass({
  render: function() {
    return (
      <div>
        Hello World.
      </div>
    )
  }
});
```

```javascript
// 在 id 为 "app" 的 HTML 元素中绘制 "HelloWorld" 组件

ReactDOM.render(<HelloWorld/>, document.getElementById("app"));
```

注意，我们新创建的组件 HelloWorld 有它自己的 `render` 方法。但作为主渲染引擎的 ReactDOM 对象也有它自己的 `render` 方法。两者之间的联系是，`ReactDOM.render` 会调用它作为第一个参数传递的组件的 `render` 方法。在这种情况下，它就是我们的 HelloWorld 组件。

在这里，我们首先包含了上述 React 和 ReactDOM 库。当你从零开始创建一个新的响应式应用时，你需要这样做。这就是初始化 React 的过程。

接下来，我们在项目中包含了 React，并将使用 `React.create` 方法创建一个 React 类的新实例。虽然这并不是初始化 React 应用的唯一方法，但在本章中我们将坚持使用这个示例。

最后，我们调用 ReactDOM 的 `.render` 方法。这里的 `<HelloWorld/>` 是我们分配 React 代码的变量名 `HelloWorld`。基本上，React 的 `render` 方法接受两个参数。

你只需要将你想渲染的内容作为第一个参数，将你想渲染的位置作为第二个参数（在本例中是 ID 为 "app" 的 HTML 元素）。从现在起，分配给 HelloWorld 变量的任何内容都将渲染在类似 `[div id = "app"]` 的元素中。

这正是 React 编程背后的基本思想。你构建组件并让它们在特定的 HTML 元素中执行操作。虚拟 DOM 会自动处理应用前端视图的快速渲染。

但有一件事……

蓝色高亮的 HTML 代码是将被写入组件渲染区域的部分。是的，我们直接在 JavaScript 语句中输入了 HTML。再次强调，此功能是通过通过 babel 从你的 node.js 安装 JSX 插件来实现的。

设置这个环境的过程有点复杂。但在我的 YouTube 教程以及本书的后后部分，会有更详细的展示。

恭喜你创建了你的第一个 React 组件！我希望保持简单，不让设置 React 仍需完成的过量内容让你所淹没。但在未来的章节中，我们将继续逐步解读使用 React 库进行编程，以及它具体包含哪些内容。

### JSX

在 React 中，在 JavaScript 内部编写 HTML 是通过开源 JSX 引擎实现的。你可以通过访问官方 GitHub 仓库查看 JSX 源码：

https://github.com/jsx/JSX

根据官方网站，JSX 是一种静态类型的、面向对象的编程语言，设计用于运行在现代网络浏览器上。涉及到 React 时，我们将使用它以 JavaScript 格式编写 HTML 标签。这有点奇特且不寻常。但主要是，它赋予了我们像返回 JavaScript 语句一样返回 HTML 代码块的能力。你会发现这是非常有用且直观的。

JSX 简单地将 HTML 语法翻译为 JavaScript。初初看起来可能非常奇怪，但它就像 JavaScript 现在有了它内部的 HTML 处理器。这种思考方式是熟悉 JSX 的良好起点。随着书籍的推进，我们将在更深入地探讨它。




### Props

在上一章节中，我提到了 React 组件。但关于它还有很多内容。之前，我们创建了一个简单的组件，看起来就像这里这样：

```javascript
ReactDOM.render(
  <h1>Hello</h1>,
  document.getElementById('root')
);
```

注意，我们直接在 `render` 方法中作为参数输入了 HTML 标签 `<h1>`，而没有加引号。这是 JSX 提供的一种语法风格。它在 JavaScript 中通常是无法编译的，但像 PHPStorm 这样的智能 IDE 能够识别 JSX 语法，因此不会将其视为错误。

只要你的项目中包含了 JSX（通常通过 `babel-js` 库或其对应的命令行插件，后者是我建议在生产服务器上使用的），这段代码就能正常编译。

现在我们知道，只有在你的项目中包含了 babel 译译器（`babel.min.js`）时，它才能工作。（换句话说，不要尝试在“桌面”上某个文件夹的记事本里编写这些代码；你的开发环境必须在 `<script>` 标签中正确设置才能进行编译，或者至少要在你的页面 `<script>` 标签中包含 `babel-js`。）它使用内部 JSX 处理器将这些内联 HTML 转换为 JavaScript。

## 函数的纯性

在讨论 React props 之前，我想提提一点。在 React 中，props 是只读的。这与一种被称为“纯函数”（pure function）的特殊函数有关。在传统的软件开发中，纯函数是指其内部不会改变传递给它的参数的。

例如：

```javascript
// 纯函数；不修改参数值
function sum(a, b) { return a + b; }
```

这被认为纯函数，因为它的主体没有修改任何作为参数传递的参数。另一方面，下面是一个不纯函数的示例：

```javascript
// 不纯函数；修改了传递的参数 "total" 的值
function sub(total, less) { return total -= less; }
```

在 React 中，**props** 遵循了“纯”的理念。这意味着你可以传递它们，前提是你的 React 组件不会从内部改变它们的值。这正是 React props 成为**只读**的本质。遵循这一规则是好的。

Props 派自 HTML 元素的属性。将它们称为 props 有点奇怪，因为在 HTML 元素中，属性是像 `DISABLED` 或 `CHECKED` 这样的单关键字标记。

props 更好的名称应该是 *attributes*（属性），因为它们看起来像 HTML 属性的 `name=value` 对，而不是 props。但事实就是如此。React 开发者选择了这种命名规范！不要怪送信者：

如果你一直在关注我们上一章节的讨论，你现在应该知道**组件**（components）是什么。它们是 HTML、CSS 和 JavaScript 代码块的组合，决定了应用程序某个视觉区域的功能。它们负责更新消息流、警报和各种状态更新。

我们也知道组件通常有一个 `render` 方法来在应用中显示它。在学习 React.js 时，你将遇到的下一件事就是 props。Props 就像函数参数。只不过你将它们传递给组件，而不是函数。不过原理是相同的。

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

// 现在调用 "render" 方法在你的 #app 中显示此组件
ReactDOM.render(<Hello name="Jason"/>, document.getElementById("app"));
```

在这里我添加了一个名为 `name` 的 prop，并将其赋值为 "Jason"。注意它包含在一个自闭标签 `<Hello />` 中。

在组件内部，我们可以通过 `this.props.name` 引用它来打印值，而不是使用上一个教程中通用的 "Hello World" 示例。

### 函数组件

上面我们演示了一个标准的 React 组件。它具有所有的复杂性：它是使用 `createClass` 函数创建的，并包含一个 `render` 方法。但下面的代码实际上也被认为是有效的 React 组件，尽管它仅仅是一个标准的 JavaScript 函数：

```javascript
function Hello(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

它之所以是一个有效的 React 组件，是因为它返回了一个 React 元素。React 元素可以被 React 渲染。（注：此处原文中存在大量重复和 OCR 错误，已按逻辑提取核心含义）。





## NPM

命令行 babel 应用是随着 Node.js 一起安装的。因此如果你安装了 Node，就会自动拥有 babel 软件包。你只需要在命令行中使用 NPM 工具单独安装它们即可，该工具默认也随 Node 一起提供。

在学习 React.js 时，直接通过 `script` 标签添加 babel 是完全正常的。只是当你的应用上线时，这种方法对于生产环境来说速度不够快。无论如何，babel 所做的仅仅是将你的 EcmaScript6 和 JSX 代码“转译”回 EcmaScript5，这样你就可以在任何尚未完全支持 ES6 的浏览器中运行它。（截至本文写作时，还没有哪个浏览器支持。）

## 源代码转译

你可能听过论坛、Twitter 和 Reddit 上的程序员使用“转译”（transpiling）这个词，但可能还没有完全理解其背后的概念。

通常，转译是将一种语言的代码编译成另一种语言的源代码的过程。它仅仅是语言之间的编译。然而，当涉及到 JavaScript 时，我们是在两个不同的 EcmaScript 规范（5 和 6）之间进行转译。

这使我们能够使用 EcmaScript 6 编写代码并将其转译为 EcmaScript 5，以便现代浏览器实际上可以运行你的代码。在本文写作时，大多数浏览器不支持 ES6，甚至 Chrome 也不支持。

最终，当 ES6 支持覆盖所有浏览器后，就可以安全地停止使用 babel 来进行 EcmaScript 规范之间的转译。你只需在标准的 JavaScript 文件中编写代码，它即可开箱即用。

但在那时，我们不妨利用这个机会学习一种有趣的源代码工具。新标准会不断涌现，转译的艺术可能在短期内不会消失。

在本章中，我想向你介绍 React 编程的基本原理，这些原理不仅限于组件的创建。在这里，我在关于组件和属性（props）的讨论中简要提到了它们。随着学习的深入，我们将继续探索响应式编程的原理。这一次，由于已经对这些原理有了初步了解，将帮助我们进阶到编写实用的 React 应用。

## 课程 2 - 嵌套组件

React.js 中的嵌套组件帮助你创建更复杂的视图元素结构。我之前提到过 React 组件的创建。为了提醒一下，这里是创建组件的方法：

```
var Component = React.createClass({ render: function(){

return (

<Something></Something>
)
});
```

这只是一个返回一组 `<Something>` HTML 标签的基础组件。我知道，你可能还在习惯于返回一个没有引号的看起来像 HTML 标签的内容，但到这时它应该开始看起来更熟悉了：

正如你可能想象的那样，这是你在使用 React 时会经常用到的代码结构类型。大多数其他内容都源于此。如果你用过 jQuery，这种组件结构可以与 jQuery 的对象选择器语法相比：

```
$(".class").on("click", function() { /*执行某些操作*/});
```

其中，我们在事件执行完毕后返回一个回调函数。在 react 中，我们返回的是一个 HTML 元素，该元素通常会被放置在应用前端的结构中。

对于 React 组件，它是一个包含 `render` 函数的 JavaScript 对象，并有一个返回转译后的 JSX 代码的 `return` 语句。这就是将 `<Something>` 标签转换为浏览器可以理解的 Ecma5 的东西。

什么放在 `render` 函数和 `return` 语句中取决于你的应用的目的。在这个示例中，为了清晰起见，让我们分别这些对象命名为 **Parent**（父组件）和 **Child**（子组件）。如果你在编写一个应用，实际名称对可能是 Friend 和 FriendList，或者 Customer 和 CustomerProperty。

### 单子组件父组件

使用这种模式，你可以实现基础的视图功能。

首先，让我们创建该模式最小的构建模块——子组件。

```
var Child = React.createClass(
  render: function() {
    return
    <BUTTON onClick = {this.props.onClick} >{this.props.text}</BUTTON>
  }
);
```

在这种情况下，子组件是一个返回按钮元素的基础组件。按钮提供了一个 `onClick` 事件，该事件将通过 `this.props.onClick` 方法执行。

现在让我们创建对应的 `Parent` 类，并使用 `Child` 作为它返回的对象。我高亮了 `Child` 以确保容易看到 `Child` 组件是如何与 `Parent` 关联的。

```
var Parent = React.createClass(
  render: function() {
    return (
      <Child onClick = {this.handleChildClick} text = {this.state.childText} />
    );
  },
  handleChildClick: function(event) {
    // 在此方法中，你可以访问
    // 传递给 Child 的 props，使用 this.state 属性
    var child_text = this.state.childText;

    // 访问点击的目标元素
    var target = event.target;
  }
);
```

注意，你可以从 `Parent` 容器内的 `handleChildClick` 方法访问子组件的文本。`Parent` 和 `Child` 容器通过传递到 `Child` 容器 `text` 属性的 props 绑定在一起。

无论你传递给 `Child`（位于 `Parent` 内部）什么，都可以通过父容器自动访问。因此，props 确实是建立两者之间关系的。

React 是一个相对新的库。然而，如果你计划在应用中使用动态的 `Parent` 和 `Child`，它确实使用了一个你只需要学会使用的 JavaScript 函数。

这个标准函数就是 `map` 方法，它原生存在于所有数组对象上。如果你以前处理过数组，可能至少听说过这个函数。它所做的是创建一个新数组，对每个项调用回调函数，并将回调函数应用的结果填充到新数组中。

### 多个子组件的父组件

为了保持简单，在这个示例中我将保持 `Child` 组件不变。注意更新后的 `Parent` 组件中对数组 `map` 函数的新用法：

```
var Parent = React.createClass({
  /* 为数组设置默认值 */
  getChildrenState: function() {
    return childData: [
      { childText: "点击我1!", childNumber: 1 },
      { childText: "点击我2!", childNumber: 2 }
    ];
  },
  render: function() {
    var children = this.state.childData.map(function(data, index) {
      return <Child onClick={this.handleChildClick.bind(null,data)} 
      text={data.childText} />;
    }).bind(this));
    return <div>{children}</div>;
  },
  handleChildClick: function (event) {
    // 在此方法中，你被传递给 Child，使用 this.state 属性
    var child_text = this.state.childText;

    // 访问点击的目标元素：
    var target = event.target;
  }
});
```

现在，我特意创建这些通用示例来向你展示父子之间的关联，因为这并不像简单的嵌套 HTML 元素那么容易。在 react 中，这种链接是如上面所示通过编程方式建立的。

这里展示的示例是响应式编程的基础块。在现实场景中，你将构建代表应用程序实际元素的组件，如警报、朋友列表、消息、评论和按钮。但这些示例是通用的。我知道学习这一切可能看起来很麻烦，但实际上，一旦你


通过编写其中的这几个组件，你将看到 React 的多功能性，因为它就像是将自定义编程嵌入到你日常的 HTML 元素中，对数据流拥有完全控制权，并利用 Virtual DOM 极速更新应用程序中需要更新的区域。

我希望你喜欢这个教程，并且它被证明是有启发性的。我将在即将出版的新书《React Gems》中更多地讨论这些内容。

## 第 3  - 处理组件事件

到为止，我们只查看了 React 程序的的基础组合。我们创建了组件并查看了它们的内部结构。

在本节中，我们将深入探讨 React 组件的结构和功能。除了 `render` 之外，我们还将探索三个新方法，每个方法都在组件的生命周期内的不同时间执行。这让我们对应用程序拥有更大的创作控制力。

始终记住，React 组件具有状态（state）。组件的整个目的是绑定到由该组件对象表示的自定义状态。状态是一个包含数据的对象。但组件还拥有辅助函数，这些函数可以更方便地控制这些状态在特定上下文中如何工作。

在本节中，我们将查看其中一些方法。

### 方法 1 - getInitialState

每个组件负责渲染它自己的状态，但 `getInitialState` 方法总会在我们的 `render` 函数之前被调用。这与对象的构造函数具有类似的功能。在这里我们设置默认值。

```javascript
var Example = React.createClass({
  getInitialState: function() {
    return {
      state: 0;
    };
  }
});
```

你经常会在 React 组件中看到 `getInitialState`。它会重置绑定到组件的默认值。在这里，你可以从数据库读取值，或者在屏幕上渲染此组件之前将状态重置为默认值。

你可以将此方法与 ECMScript 6 提供的默认构造方法互换使用：

```javascript
class Example extends React.Component({
  constructor: function() {
    this.state = 0;
  }
});
```

这里唯一的显著区别是我们正在使用 `this` 关键字附加到主对象上。

要在组件渲染在屏幕上时访问状态，我们必须使用 `componentDidMount` 方法：

### 方法 2 - componentDidMount

当组件渲染时，React 会自动调用 `componentDidMount`。通过将其添加到自定义的 React 组件中，你对其进行了重载（overloading）。重载意味着在你扩展自定义组件的所自的默认 React 组件对象中，向已存在的方法中添加你自己的功能。这就是使用 **extend** 关键字的全部意图。我们正在扩展库已经提供的 React 组件对象的默认功能。

当我第一次在 React 组件中听到“挂载（mounting）”函数时，我不理解它的意思。我们难道不是简单地为我们的主要 React 组件附加一堆辅助方法吗？

我们在书中前面已经讨论过挂载。如果你仍然需要复习这个过程，我建议确保你已经学过之前讨论过的 **Gem 6 - 组件挂载 (Component Mounting)**。

`componentDidMount` 是负责设置组件已挂载状态的方法。

```javascript
var Example = React.createClass({
  componentDidMount: function() {
    this.state = 1;
  }
});
```

它仅意味着虚拟 DOM 已经与一个将在屏幕上实际更新的 DOM 节点关联。该方法在执行组件的 render 命令后总是被调用。它们是同义词，可能可以互换使用。它确保并告诉我们元素已经存在于虚拟 DOM 中。`render` 方法已经在其上调用过了！

### 方法 3 - componentWillUnmount

最后，`componentWillUnmount` 在组件从页面移除并即将被销毁之前被调用。

```javascript
var Example = React.createClass({
  componentWillUnmount: function() {
    this.state = null;
  }
});
```

注意，我们在这里将状态重置为 `null`。组件被销毁，我们不再需要它的数据。这是你清理组件所用内存（如果有）的地方，例如初始化定时器。

## 用 React 编写的完整应用程序示例

我们已经涵盖了足够编写完整 React 应用程序的原则。我刻意尝试让书中的所有示例保持简单。复杂性通常来自编程中的创意，如果我把一个大型程序放进这本书，你可能会让你产生挫败感而不是动力。

在这里，我将构建一个简单的搜索应用，从数组中查找结果。如果输入的字符与列表中的任何内容匹配，它们将被过滤掉，所有其他条目将被忽略。

这个应用程序非常像 Google 的搜索查找功能，当你向查询输入框中输入短语时，项目会下拉显示。下面我列出了完整的源代码。

在这里，我不会包含应用程序的级联样式表（CSS）部分。这可以单独处理。我们希望严格关注 React 的实现。

与你使用标准 JavaScript 代码必须做的一切相比，考虑到它实际的功能，这个应用程序意外地紧凑。

### 创建搜索列表

### 使用 JavaScript 中的对象字面量格式创建潜在搜索结果列表

```javascript
// 首先，让我们定义所有可搜索动物列表
var libraries = [
  { name: 'Wolf', url: 'http://localhost/wolf' },
  { name: 'Panther', url: 'http://localhost/panther' },
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

### 编写 React 

```javascript
// 创建我们的搜索组件
var SearchComponent = React.createClass({
  // 将输入元素重置为空格
  getInitialState: function() {
    return { searchString: "" };
  },

  handleChange: function(e) {
    // 注释掉下面这一行将导致文本框不改变值， 
    // 因为 React 输入框不能独立于分配给它的值进行更改。 
    // 在这种情况下
    this.setState({ searchString: e.target.value });
  },

  // 渲染此组件
  render: function() {
    var libraries = this.props.items,
        searchString = this.state.searchString.trim().toLowerCase();

    if (searchString.length > 0) {
      // 我们正在搜索。过滤结果。
      libraries = libraries.filter(function(l) {
        return l.name.toLowerCase().match(searchString);
      });
    }

    // 将此组件作为 JSX 语句返回
    return (
      <div>
        <input type="text" value={this.state.searchString} onChange={this.handleChange} placeholder="在此输入" />
        <ul>
          {libraries.map(function(l) {
            return <li>{l.name} <a href={l.url}>{l.name}</a></li>;
          })}
        </ul>
      </div>
    );
  }
});

// 在页面上渲染 SearchComponent
ReactDOM.render(
  <SearchComponent items={ libraries } />,
  document.getElementById('container')
);
```

将此代码放入你应用程序的主 .js 文件中并运行。它将产生基本的下拉功能。输入部分动物名称将它们从主列表中过滤掉。理想情况下，你将从数据库或其他数据存储机制加载此列表。

正如你所看到的，取决于你设计的应用程序类型（在这种情况下，应用程序非常简单），你可能会根据组件所代表的元素的性质，使用或不使用任何挂载或更新方法。




## EcmaScript 6 - 你需要了解的

当 React 创建时，ES5 规范正处于焦点位置。在 2015 年甚至整个 2016 年，它仍然是新颖的。

然而，到 2017 年，它开始逐渐适应 ES6 语法。这就是为什么在学习 React 的时候，讨论应用于这一新标准的重大变化是如此重要的。

当你学习 React 时，你学习的不仅仅是 React。它在 ES5 中运行良好良好，但那种语法正在变得过时。这正是许多程序员可能会感到困惑的地方，因为本质上同一个库在你在互联网和书籍中看到的各种不同示例中，看起来可能完全不同。

如果你不知道 React，那么你可能对 EcmaScript 6 一点都不了解。我知道这样假设是危险的，但我想认为你在这一章中学到的内容可以证明它是合理的。

ES5 本身并没有问题。但它在短期内不会消失。我认为，在行业仍从一个规范过渡到另一个规范的时期编写教育类书籍时，偶尔在两者之间进行切换是很重要的。

但我们已经到了书的这里，现在我们将研究 EcmaScript 6 规范中 JavaScript 的主要区别和新增。在书结束时，我还将这里讨论的许多主题提供备忘页（cheat sheets）。

## var 和 let 关键字

在 ES6 中，共识是不再使用 `var` 关键字，而是使用 `let` 关键字。对此是有原因的，如下所示：

- 使用 `let` 关键字时没有变量提升（hoisting）。如果你熟悉 JavaScript 的变量提升机制，当你使用新的 `let` 关键字时会发现不同。

变量提升是指 JavaScript 将所有变量定义移动到它们定义所在的作用域的顶部。这个不为人知的过程是在幕后完成的。但它确实是如此：

```javascript
console.log( a ); // undefined; 但仅是因为它被提升了
var a = 1;
}
```

而 let 的示例：

```javascript
{
console.log( a ); // ReferenceError: "a" is not defined at all
let a = 1;
}
```

在上面的示例中，当尝试打印变量的值时，控制台输出的结果是 `undefined`。在第一情况下，是因为变量被提升了。在第二个示例中，是因为它没有被提升。

- 在全局作用域中。`let` 关键字和旧的 `var` 关键字仍然作用于全局作用域。但 `let` 关键字没有绑定到全局 `window` 对象：

```javascript
vara = 1; // 将绑定到全局 window 对象
letb = 1; // 将不会绑定到全局 window 对象
console.log(window.a); // 1
console.log(window.b); // undefined
```

- 在函数作用域中。`let` 和 `var` 关键字在函数作用域内仍然是相同的：

```javascript
function helloThere() {
  let x = 1;// 相同的作用域
  var y = 1;    // 相同的作用域
}
```

**语句中。** `let` 关键字仅在 `for` 循环内部可见，而 `var` 可见以确保函数作用域的可见性。因此，`let` 关键字限制了在 `{ }` 括号指定的最近嵌套块内定义的变量可见性。下面，让我们先来看看 `var` 传统上是如何处理作用域的：

```javascript
// 函数内部和 for 循环示例
function helloThereIterator() {
  // i 在理论上在这里也是可见的
  for (var i = 0; i < 10; i++) {
    // i 在这里是可见的
  }
}
```

这可能不是 `var` 关键字的最佳示例（因为循环是它最初定义的地方），因为它在函数内部的处处可用。但它仍然证明了这一原理。

传统上，已知 `var` 可以在函数的括号 `{ }` 内部进行访问，并对函数作用域隐藏，除非它是 `window` 对象。这是基本规则。但 JavaScript 就是这么复杂……而且只有在函数内部没有找到变量时，才会检查 `window` 对象，而它是在函数外部的。

确定变量是否应该在全局作用域内可用是程序员的责任。这是 JavaScript 试图做到“为所有人提供一切”的一个例子。

虽然这种松散性在很多情况下是有帮助的，并让学习曲线几乎不存在，但从长远来看，你会遇到这些奇怪的情况，特别是当你的程序在大型项目中达到一定长度时。

现在，让我们来看同样的示例。我们所做的只是将 `var` 交换为 `let` 关键字。这产生了不同的作用域预期。

```javascript
// let 示例
function helloThereIterator() {
  // i 在这里不可见
  for (let i = 0; i < 10; i++) {
    // i 在这里可见，并且在该作用域内部的回调中可见
  }
}
```

- `let` 关键字不允许重复声明

`var` 关键字（在严格模式下）允许你在同一个作用域内重复声明它的值。但对于 `let` 关键字并非如此：

```javascript
'use strict';
var a = 1; // OK.
var a = 2; // OK. a 现在是 2.
```

```javascript
'use strict';
let a = 1; // OK.
let a = 2; // Syntax error: 符 a 已经声明
```

- `let` 关键字也可以用于避免闭包问题。它将绑定一个新值，而不是保留对旧值的引用。

```javascript
"use strict";
for (let i = 1; i < 10; i++) {
  $.ajax("url":"script.php", function(msg) {
    console.log(i); // 变量 i 在这里失去了它的原始作用域，它不再与循环中定义的 i 关联
  });
}
```

这段代码演示了当在循环中使用 `var` 关键字并结合 `ajax` 调用时，经常发生的常见 JavaScript 问题。在这里，由于 `i` 似乎在 `ajax` 的回调函数内部被重新定义，它不再与 `for` 循环内定义的同一个 `i` 关联。

这个经典问题通常通过将变量作为参数传递给函数来避免，但这不必要创建该变量的新实例。

然而，当使用 `let` 定义相同的作用域时，情况并非如此。它有效地解决了这个常见问题。这里是同样的示例，只是这次使用了 `let`。

```javascript
"use strict";
for (var i = 1; i < 10; i++) {
  $.ajax("url": "script.php", function(msg) {
    console.log(i); // 这里 i 是最初在循环中定义的那个
  });
}
```

这确实节省了许多与循环和回调函数相关的烦恼。

- 此外，`let` 关键字允许我们将变量的值保持在它定义的作用域中，如这个独立示例所示：

```javascript
let a = 1;
console.log( a ); // Reference error: a 是未定义的
```

- 换句话说，可以说使用 `var` 定义的变量从它定义的那刻起，在定义的整个函数中都是已知的。而 `let` 关键字仅对定义所在的作用域块以及其内部的所有其他作用域（即使是回调函数）是知的。

## 新的 `const` 关键字

`const` 与 `let` 完全一样。唯一的区别是，一旦你使用 `const` 定义了一个值，在程序的后续部分就无法再重新定义它。这样做将产生错误：

```javascript
let a = 1;
a = 2; // 这是可以的，我们只是重新赋值了变量的值
```

```javascript
const a = 1;
a = 2; // error，这是一个常量，不能重新赋值！
```

这有什么用？常量变量传统上用于计算机程序定义在整个应用程序运行期间不会改变的值。它们对于标志位值和不应更改的应用配置设置非常有用。

哦，还有一件事……当涉及到对象时……`const` 关键字虽然防止了重新赋值，但它实际上并没有让被赋值的对象变得不可变。与许多其他语言不同，将对象设为 `const` 会让它的属性变为不可变。

JavaScript 不是这样。





## 解构赋值

EcmaScript 6 引入了**解构赋值**。这是 JavaScript 的一项新功能。之前对 `let` 关键字的解释为讨论接下来的主题奠定了基础。所以，让我们来看看它是如何工作的：

```
let {a, b} = obj;
```

在这个例子中，创建了两个变量 *a* 和 *b*。然后，从名为 **obj** 的对象提取属性 **obj.a** 和 **obj.b**，并分别赋值给这些变量。因此，这等于执行以下操作：

```
let a = obj.a;
let b = obj.b;
```

这种格式占用的空间大得多*解构赋值*可以节省空间并为我们的代码提供更好的可读性。习惯它们吧！:)

## For-of 循环

这是 EcmaScript 6 中一种全新的循环类型。让我们来看看它是如何工作的：

```
for (let [key, value] of map) { ... }
```

这个强大的 for 循环将遍历 map 中存储的值。遗憾的是（和 JavaScript 中的很多事情一样），for-of 循环不能作用于对象（及其属性）。这几乎是一个令人困惑的设计决策。那么，哪些 for-of 循环可以工作呢？

for-of 循环专门设计用于仅处理 Array、Map 和 Set 对象。

## Map 对象

与 Array 对象一样，ES6 增加了一个新对象，称为 Map。Map 无非只是一个简单的键/值映射。它们非常像 PHP 中的关联数组。

不应该在处处使用 Maps。只有在你之前使用对象作为集合的地方才使用它们。这是它们的初衷。在你的 JavaScript 程序设计中，使用对象仍然应该是首主要的。

Maps 有一个 `.size` 属性来确定其大小。与对象不同，在对象中你必须手动计算对象的大小。当你有通过键/值关联的数据集合时，请结合 for-of 循环使用它们！

## 箭头函数

EcmaScript6 最受欢迎的特性之一是箭头函数。我认为你应该尽早开始使用它们。箭头函数只是用更紧凑语法编写的 JavaScript 函数，与使用 `function` 关键字创建的普通函数略有不同。这是箭头函数的基本格式，起初看起来可能有点奇怪：

```
name = (params) => returned expression
```

例如，你可以使用箭头函数这样写：

```
x = (a, b) => { console.log("This is arrow function x with params = " + a + " and " + b); };
```

但这只是函数定义。它可以像普通函数一样如下所示执行：

```
x(5, 7);
```

与普通 JavaScript 函数相比，一个根本的区别在于箭头函数处理 **this** 关键字的方式。它从根本上解决了与 **let** 关键字为普通作用域解决的相同（或相似）的问题。我们在这里需要进行稍微深入的讨论。

**JavaScript 箭头函数**是一个仅适用于 EcmaScript 6 的特性。它在这一规范之前并不存在。它增加了在对象内部创建匿名函数使用的便利性，同时在匿名事件处理程序中保留了 **this** 对象的值。

箭头函数还修改了对象作用域定义内无名回调函数中使用的 **this** 对象的功能，通过自动将其绑定到对象的最层局部作用域。这让我想起了一点提升（hoisting）（我在我的其他教程中简要提过提升）。

箭头函数帮助我们逃避原始作用域模型中固有的 **this/that** 操（如果你不熟悉我指的是什么，请继续阅读，本教程将解释它）。

箭头函数也由于其语法而被称为“胖箭头”函数。

```
(params) => { statement };
```

只需将其看作定义 JavaScript 函数的另一种语法即可。

本教程的其余部分将解释旧 JavaScript 示例与区别，以及如何使用箭头函数来提高代码可读性并在内部调整对象功能。

箭头函数的目的是解决源于原始 JavaScript 语言设计的根本问题，该问题涉及对象作用域和自动 this 关键字绑定。

与其他许多 Web 开发者一样，我曾用 JavaScript 开发过基于画布的游戏引擎库，这需要创建和实例化 Line、Rectangle、Sprite 以及许多其他有用对象（一个辅助开发浏览器电脑游戏的库），我面临了以下问题。

让我们假设我们有一个名为 Sprite 的简化对象版本，用于创建游戏角色和敌人对象精灵！

此外，让我们创建一个类型为 Sprite 的新“ship”对象并实例化它。

```javascript
/* JavaScript 中一个显著简化的 Sprite 对象 */
var Sprite = function() {
  this.angle = 5;
  this.draw = function() {
    alert(this.angle); // 显示精灵的角度
  }
}
var ship = new Sprite(); // 实例化 ship
ship.draw(); // 使用 this.angle 旋转角度绘制 ship
```

注意 draw 函数。在这个例子中，我们输出了精灵的当前旋转角度。在现实世界中，代码实际上会更复杂。但这只是一个演示 JavaScript 中箭头函数的示例。

我知道 JavaScript 函数的内部机制一直让程序员难以捉摸。这种“实验”事物如何运作并根据感觉和黑客结果来行的想法是诱人的。在示例中，“this” 关键字在 Sprite 自身的作用域和其 draw 函数的作用域内是相同的。

我们在 Sprite 的作用域中指定了 5。通过从 Sprite 的 draw 函数中引用它，我们只是获取了它的值。（等等，检查逻辑流...)

事件处理程序内部的 "this" 关键字会自动赋值给事件发生的对象。让我们运行这个程序看看发生了什么，与我们之前的示例相比。

alert 消息现在将返回：

# Undefined

这是因为匿名函数 `function() { ... }` 的 `this.angle` 不再指向 Sprite 对象的 "this" 对象。而且匿名函数上没有附加名为 "angle" 的属性（该属性作为参数传递给 setTimeout 函数的）。

```javascript
/* JavaScript 中一个简化的 Sprite 对象 */
var Sprite = function() {
  this.angle = 5;
  this.draw = function() {
    alert(this.angle); // 显示精灵的角度
  };

  // 新！一种解决方案是在此作用域内仍然创建一个 "that" 变量
  var that = this;

  // 以下代码将作为对象
  // 构建过程的一部分执行
  var timer = setTimeout(function() {
    alert(that.angle); // 从这里显示精灵的角度
  }, 1000);
};

var ship = new Sprite(); // 实例化 ship

ship.draw(); // 使用 this.angle 旋转角度绘制 ship
```

我在这个例子中所做的只是将对象赋值给主 Sprite 对象作用域内新创建的 `that` 变量。在 timer 定义之前。所以实际上，我们现在有了类似这样的内容，在 Sprite 内部。

我还将将 `this` 改为 `that` 在 `setTimeout(function() { ... });` 中。

让我们再次运行代码看看现在会发生什么：



5

`this.that` 的值为 5。这发生在我们将 *this* 对象绑定到名为 *that* 的变量时。

我确信你已经在之前的示例中使用过我刚才描述的技巧。如果没有用，那么，我很高兴你现在知道了它。大多数程序员都是靠直觉发现它的。因为要学习 JavaScript 中函数对象与这些函数内部匿名事件之间的作用域规则差异是需要时间的。

在脸上带着微笑并做完这些解释后，我们终于来到了最后一个重大的终极问题！

## 什么是 JavaScript 中的箭头函数？

JavaScript 中的箭头函数和匿名函数之间有什么区别？

JavaScript 中的箭头函数是一种具有简写语法的匿名函数。与标准匿名函数相比，唯一的两个区别在于语法以及 `this` 对象在相应作用域内被处理的方式。这是一个小细节，在涉及到 `this` 对象的绑定时，两者的实际运行方式略有不同。

让我们比较一下普通的 JavaScript 匿名函数和对应的箭头函数。我们已经知道 JavaScript 中像 `function(){...}` 这样的匿名函数是什么样子的。但箭头函数实际上有独特的语法。

注意，两者的功能完全相同，都是执行某些代码。不同之处在于，箭头函数会自动处理我们在之前的示例中经历过的繁琐的 `this`/`that` 切换。这一点并没有改变。所以我们再也不需要重命名或将其绑定到另一个变量（如 `that`），就像之前的示例中那样。

这是 EcmaScript 6 中定义 JavaScript 新箭头函数的语法：

```javascript
() => {};
```

提个醒。JavaScript 中的箭头函数不能与 "new" 操作符配合。它们是匿名的，通常用于事件。

但也有语法上的变体：

```javascript
(a, b) => { ... } // 多个参数
a => { ... } // 单参数
```

注意参数可以包含一组由逗号分隔的多个参数。在这种情况下，你必须始终使用括号。对于单参数语法，你不需要使用括号。

在现实场景中，我们也可以将箭头函数赋值给变量名。在这种情况下，匿名箭头函数就变成了命名的。函数从其体的作用域内返回。

```javascript
var add = (a, b) => { return a + b };
```

话虽如此...

```javascript
add(1, 2); // 返回 3
```

但还有另一种无作用域的函数定义语法：

```javascript
var add = (a, b) => a + b;
```

注意，这里的返回值由普通的 JavaScript 语句表示。这将产生完全相同的结果。我们删除了 `return` 语句。但函数仍然返回 `a + b` 的值。在这种情况下，`a + b` 是一个 JavaScript 语句，没有作用域体。默认情况下，如果没有指定 return 关键字，未指定作用域的箭头函数将返回语句的值。

最后，让我们结合起来并重写我们原始的 Sprite 对象示例。现在只使用箭头函数。你可以看到，没有必要创建并设置 `this` 绑定到 `that` 变量名。箭头函数为你处理这一切！

```javascript
/* JavaScript 中显著简化的 Sprite 对象 */
var Sprite = function() {
  this.angle = 5;
  this.draw = function() {
    alert(this.angle); // 显示 sprite 的角度
  }
  var timer = setTimeout(() => {
    // 注意这里使用了箭头函数
    alert(this.angle); // 使用 "this" 显示 "5"，而不是 "that"
  });
  var ship = new Sprite(); // 实例化 ship
  // ship.draw(); // 绘制带有 this.angle 旋转角度的 ship
};
```

我们只是切换了通常用作事件处理器的标准匿名 `function(){...}`，并将其替换为箭头函数 `() => {...}`。

从那一刻起，新匿名事件函数内部的 **this** 关键字开始正确地引用原始 Sprite 对象的 **this** 关键字。无需我们编写任何额外的绑定代码。

那么……我想我们对箭头函数的讨论就此结束。希望你喜欢这个教程。请将其分享给你的朋友，发布在 Twitter 或你的 Facebook 页面上。

Developer Post 是一个小型网站，致力于简单解释那些看起来很复杂的课题。希望这能帮助某人写出更好的 JavaScript 代码。

如果你想学习更多关于 ES6 Harmony 的知识，请访问 [Ecmascript 6 的新特性 Harmony] 以熟悉基础知识。

根据 Sitepoint 的这篇文章，箭头函数是 ES6 中最受欢迎的功能。

这个 Mozilla 箭头函数教程帮助我熟悉了箭头函数。当我将其作为我的第一个参考时……

## 立即调用箭头函数 (IIAF)

如果你熟悉 JavaScript，你可能遇到过立即调用函数表达式 (IIFE)。你也可以用箭头函数实现这一点：

```javascript
(() => {
  // 这是一个匿名的 IIFE
})();
```

## 新数组方法

在 ES6 中，我们有了这些新的数组方法。让我们定义常用的数组：

```javascript
let arr = [1, 2, 3, 4, 5];
```

### find

返回数组中第一个满足所提供的测试函数的元素值。如果没有找到任何值，则返回 undefined。

### findIndex

`findIndex` 方法返回数组中第一个满足所提供的测试函数的元素索引。如果没有找到任何元素，则返回 -1。

### fill

`fill` 方法用静态值填充数组中的所有元素。它可以使用数组的一部分进行填充：

## copyWith

这个新的数组方法复制它内部的一个序列项目，从由 `start` 指示的位置开始，到由 `end` 指示的索引结束：

```javascript
arr.copyWith(target, start, end = this.length);
```

这是一个实际的示例：

```javascript
var arr1 = [1, 2, 3, 4, 5];
// 将前 3 个索引复制到最后
arr1.copyWith(6, 3);
alert(arr1); // 1, 2, 3, 1, 2, 3
```


我们承诺解决的问题之一是经典案例：即 HTML 元素的事件（如 `onclick`）被更新应用程序视觉效果的代码所覆盖。因为这在频繁更新的前端视图中经常发生。

只要原始 DOM 结构的完整性保持不变，或与事件执行时的结构相似，无论你网站的 DOM 结构发生了什么变化，承诺（Promise）都可以存在于“未来”。

# 感谢你

本教程书籍由我独立出版，并分发给我的免费 JavaScript 时事通讯的订阅者。没有你们的支持，这一切是不可能实现的。

你是否尝试过编写并发布自己的书？撰写一本技术书籍需要投入数小时的研究和心思考！

正因如此，我想专门用这一章节来单纯对购买了《React Gems》的你表示感谢。正如你所知到的，你的购买包含了免费的终身书籍更新。

每当我添加、修改或编辑书的重大部分时（我计划在 2017 年期间一直这样做），你将继续自动收到包括新章节在内的书籍更新。

更新后的教程书籍将发送到你购买此版本时使用的 PayPal 邮箱地址。随着我收集更多的教育材料，每 1-2 个月或在可用时会进行新更新（一次高质量的更新需要时间）。

免费更新已包含在你的购买中，你无需做任何事情即可继续接收它们。

感谢阅读以及你的持续支持！

作者，
Greg Sidelnikov
greg.sidelnikov@gmail.com

### 书籍更新 1 - 2017年1月6日

- 编辑并改进了章节：
- “作者的寄语”（改进了文本）
- “学习 React 的主要障碍”（加深了对 JSX 和 babel 的见解）
- “EcmaScript 6 - 你需要知道的事”（修复了 `let/var` 示例）
- 书籍长度变化：+2 页。

### 书籍更新 2 - 2017年1月10日

- 编辑并改进了章节：
- 修复了第 37 页的拼写错误（将 `of` 改为 `or`）
