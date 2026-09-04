
# React.js 书籍：从零开始学习 React JavaScript 库

本书作者向你问好！

欢迎阅读《React.js Book》。一本叙述性的教程书。

自从 90 年代 Netscape Navigator 时代以来，我就一直是一名 Web 开发人员。当时它是第一个支持 JavaScript 的浏览器。

《React Book》是 React 的入门指南。我给它起了一个简单的名字，因为这本书是对 2017 年一个日益流行的 JavaScript 库的介绍。

## 这本书写给谁看？

这本书是写给从未编写过 React 且正在寻找良好起点的人的。虽然不需要对 JavaScript 有基础了解，但最好越好。

React 绝对是我在众多 JavaScript 库中学习的最困难的内容之一。部分原因在于它假设你了解许多专业 Web 开发相关的其他知识。即：`Node.js`、`NPM`、精通 `babel` 命令行工具、`EcmaScript` (5, 6 和 7)、`JSX` 以及可能还有 `WebPack`。

这本书还假设你是 React 编程的新手。这对我这个作者来说带来了一个挑战，因为我有责任用一种仍然有意义的方式来讲解 React，而不会用看起来复杂的巨大代码块让你无所适从。

这是我作为 Learning Curve 作者的第一本实体书。

很高兴知道你决定购买我的 JavaScript 书籍之一：**React.js Book**。你现在手里拿着这本书。

一切始于 2013 年我的第一本 JavaScript 书。当时我将其作为我免费教程的一部分出版。今天我继续编写和出版我的教程作品，这是我 JavaScript 系列中的下一本。

我的教育文献可以在 Amazon 上找到。*Learning Curve* 官方出版的不断增长出版物可以通过以下链接找到：

`www.amazon.com/Greg-Sidelnikov/e/BooJZF64`

请在本书完成后查看并在 **Amazon 上发布你的评价**。比起评分，我更看重*诚实的反馈*。这有助于我改进我的工作。

**感谢你对我的教程书籍感兴趣！**

# 关于 React 编程的简单叙述

本书的呈现形式是通过代码示例，旨在作为深入理解 React 库的启动板。

我在这里说明，仅仅依靠这本书不足以成为一名 React 程序员并开始编写真实世界的 React 应用。因为在 `EcmaScript` 5、6 和 7 之间存在语法差异。由于这个原因，React 可能是你经历过的最困难的学习体验之一。

考虑到这些情况，这本书的编写和编辑是为了尽力帮助你应对陡峭的学习曲线。如果你有任何建议、意见或评论，请通过书末提供的邮箱联系我。

这本书由 Greg Sidelnikov 编写和编辑。这在某人手里感觉很奇怪，因为这是我的第一本实体书。那就是我！

你也可以通过我的邮箱联系我：`greg.sidelnikov@gmail.com`

> 教学是一个学习过程。

- 宝石 1 - React 组件 35
- 宝石 2 - Render 方法 36
- 宝石 3 - 虚拟 DOM 与带宽拯救 38
- 宝石 4 - 初始化 React 类的两种不同方式 40
- 宝石 5 - 状态与带宽拯救 43
- 宝石 6 - 组件挂载 46
- 宝石 7 - Node.js & NPM 51
- 宝石 8 - JSX 导览 53

| 编写 React 应用 | 56 |
| 课程 | 57 |
| Props | 64 |
| 函数式组件 | 64 |
| 羊皮下的狼 | 68 |
| 原生 Babel vs JavaScript | 69 |
| 源码编译 | 69 |
| 父组件 | 70 |
| 单子父组件 | 71 |
| 多子父组件 | 72 |
| 事件处理 | 74 |
| 方法 1 - getInitialState | 76 |
| 方法 2 - componentDidMount | 77 |
| 方法 3 - componentWillUnmount | 78 |
| 完整 React 应用示例 | 79 |
| 创建搜索列表 | 80 |
| React 应用 | 82 |
| EcmaScript 6 - 你需要知道的 | 83 |
| var 和 let 关键字 | 84 |
| 新的 const 关键字 | 89 |
| 解构赋值 | 89 |
| For-of 循环 | 90 |
| Map 对象 | 91 |
| 箭头函数 | 91 |
| 什么是 JavaScript 中的箭头函数？ | 93 |
| 立即执行箭头函数 (IIAF) | 101 |
| 反引号模板字符串 | 102 |
| 新数组方法 | 103 |
| 感谢 | 107 |

# 引言

《React Book》是一本由宝石、课程和图解组成的教程书。我是多本探索 JavaScript 语言及其库的 Web 开发教程书籍的作者。其中之一！

首先，感谢你对《React Book》感兴趣。它于 2017 年 3 月 17 日通过亚马逊 KDP 程序以实体书形式出版。它将引导你完成学习响应式编程的过程。

截至 2017 年，我所谓的响应式编程已成为一种思考 Web 应用的替代方式。它应用了让你的 Web 应用极具响应性的编程模式，并为用户带来更快的体验。

从零开始学习 React 时，我花了大约三周才意识到一件事：React 与我编写过的任何库都不同。它假设你拥有许多先知识。因此，我必须以特定的方式编写这本书。一种深入理解它的过程。

分解为处理你在初次学习 React 时将面临的实际问题的组件。

任何语言或编程库都假设学习者理解某些与其特有的基础术语。例如，如果你熟悉 `jQuery`，你就必须了解一些 CSS 选择器。同样，在编写 C++ 代码时，你必须了解各种与面向对象应用开发相关的基础原理，如继承。同样，React 也拥有一套其独特的原则。

但使用 React 库进行编程不仅仅是学习和使用 React 对象、组件、状态（`states`）、属性（`props`）和方法。因为这本书的主要受众是完全没有编写过 React 编程的人，因此整本书都致力于解释这些原则到底是什么。

你曾在其他库中听过 `props` 或 `states` 吗？你可能听过 `states`，但对 `props` 并不那么熟悉。在 React 中，`props` 指的是对象的“属性”（`properties`），它们实际上是传递给 React 对象的参数。为什么 React 库的开发者决定将它们称为 `props` 一直是个谜。因为即使它们所代表的内容也来自 HTML 属性（`attributes`）。你可能已经知道在 HTML 中，属性（`attribute`）和属性（`property`）之间是有区别的。

React 将理解 `props` 和 `states` 视为了显性要求。也就是说，如果你想在你的 React 应用中完成任何重大任务。它们几乎就像是你为了成为一个多才的 React 库程序员而绝对必须掌握的子功能。

正是这些奇特的细节需要以往的 JavaScript 经验，如果没有经验（以及对经验的解释），学习 React 编程将困难得多。

幸运的是，作为作者，我意识到了这一点，并且在编写时考虑了这一点。有时 React 会假设你具备 React 库本身并不具备的软件原理知识。书中的段落将在文中逐渐揭示这些原理。

这本书并不是对象名称、方法和函数的列表，并附带关于它们作用的辅助说明。你可以在 Facebook 的官方 React 文档页面查找它们，那里包含了对每个方法的详细列表和解释。

相反，这本书将处理涉及 React 编程的上述原则的渐进学习和理解过程。好消息是，我已经为你做好了所有重要的研究。接下来的内容是一段我希望能帮助你快速起手的旅。

在我们开始之前，我想向你展示我发现的一些内容。在接下来的章节中，你将看到一份学习 React 最困难的事项列表。随后是你会想要学习它的重要原因。

在这里，我将尝试谈谈从零学习 React 库时面临的常见困难。这些困难让学习 React 不如你已经习惯的简单库那样直观直接。

我会尝试在这样做的同时不让 React 看起来像是一个糟糕的选择，因为……总之，这确实是一本关于如何成为一名 React 程序员的书。然而，如果我们现在至少简短地谈论困难的部分，在我们之后进展时会更容易接受。

新的设计模式。新的，且在很多情况下是不熟悉的。如果你是从传统的 2015 年之前的 JavaScript 编程世界来到 React，可能需要时间来适应 React 库采用的模块化和声明式设计。

当然，如果你曾经工作过大型 JavaScript 应用，你可能已经处理过长长的 `*.js` 文件列表，并将它们视为独立的模块。但对于写此时的大多数程序员来说，事实并非如此。React 要求我们使用模块化设计以实现最大的管理效率。

然后我们当然还有 `JSX`。由于下文解释的原因，这初可能会引起困惑。React 编程本身并不需要 `JSX` —— 它是一个可选功能。

起初 `JSX` 看起来有点奇怪。但没有它事情将变得困难。我会在这里简要解释一下这个问题，然后我们继续。

`JSX` 格式让很多人感到困惑。它就像在 JavaScript 编写 HTML。当你第一次遇到它时，它看起来简直不可思议。

下面是包含 `JSX` 格式的 JavaScript 代码，允许将 HTML 标签作为 JavaScript 语句编写。

```javascript
var div_blocks = <div>
  <div>Another nested tag</</div>
</</div>;
```

等等。你看到我看到的了吗？我们刚刚不懈地将 HTML 输入到 JavaScript 语句中，而没有给 HTML 加引号。我们甚至使用换行符进行分隔而没有双引号……而且仍然逃过了。

`JSX` 处理器将 XML 视为 HTML 并将其转换为有效的 JavaScript 语句。它在后台完成了所有脏活。这种类型的代码从 XML（看起来像 HTML）转译为 `EcmaScript` 5。这样浏览器就能理解它了。这意味着浏览器看到的实际代码看起来甚至不是这样。这只是为了我们我们在编写我们的 React 程序时使用的。但只要 `JSX` 转换发生（我们将稍后讨论这一点），我们就可以毫无障碍地以这种格式编写代码。

你将在整本书中遇到 `JSX`。现在需要知道的一点是 `JSX` 与 React 组件结构是可以互换的。我们在上面的源代码示例中本质的实际上是一个有效的 React 对象。

由于这个原因，`JSX` 经常作为 React 的辅助库使用。你可以通过使用 React 方法而不使用 `JSX` 创建上面示例中相同的语句。使用 `JSX` 不是强制要求的，你可以不用它。

然而，没有了 `JSX`，React 编程就像吃没加奶酪的披萨。两者共同工作提供美味的体验，即使这需要试错和时间来学习如何烘焙饼饼。

如果你从未听说过转译（`transpiling`），也许我应该现在给出一个简短的解释。在书的后面，我们将介绍如何将其设置成我们在编写时的后台运行过程。

`Babel` 将代码从 `EcmaScript` 6 转到较早的版本（ES5）有些开销，看起来似乎是不必要的事情。因为最终 Chrome、Firefox、Safari 以及希望的 IE 将提供完整的 ES6 支持，这个过程将变得自动。然而，它仍然值得一看。

通过 `Babel` 我们可以使用任何 ES6 特性，例如 `import`：

```javascript
import someClass from "someClass.js"
```

这将从定义 `someClass` 的 `someClass.js` 文件中获取 `someClass` 类定义。截至写此时的 Chrome、Firefox，可能在本书的纸质版出版时，这些浏览器已经提供了完整的 ES6 和 ES7 特性并发布了对 `import` 关键字的支持。至少我希望如此。

然而，如果事实依然如此，`babel` 允许我们在现代浏览器提供官方支持之前现在就开始学习和编写 ES6 代码。

好消息是，安装 `Babel` 插件迫使你学习如何使用命令行工具。许多 JavaScript 开发者通常不熟悉这一点。这是一个非常好且有时非常宝贵的知识。

在专业的软件开发环境中，对于存在于桌面任意文件夹中的个人项目之外，这一点是极其真实的。

*它非常快。* 这可能是 JavaScript 程序员想要开始使用 React 库编写应用程序的首要原因。它通过利用 **DOM 的虚拟副本**，被设计为执行“虚拟化”操作。换句话说，在这些操作被渲染到标准的 JavaScript DOM 树之前，它们是相似但并不相同的。

令人惊讶的是，将 UI 移动到虚拟 DOM 实际上改变了终端用户对应用程序的感受。你可能已经在 Netflix 等网站的整个网络上开始注意到这种现象了。

React 的虚拟 DOM 是帮助你实现这一点的机制。它是 React 的一个巨大的核心特性。你在 React 中做的每项工作都将以某种方式与它相关。而且只有当你准备好渲染组件时，才能通过将其**挂载（mounting）**到 UI 上来实现。你将在书后部分听到更多关于这个术语的内容。

**模块化设计。** React 支持模块化设计，这通常与构建大型**可扩展**应用程序相关。其原因为 2015 年发布的 `EcmaScript` 6 规范提供了新特性，该规范提供了有利于模块化方法论的新语法。例如，**require** (ES5) 和 **import** (ES6) 关键字不仅将文件连接在一起，还假设了对象之间基于类的关系。

尽管在编写本文时，**import** 关键字在现代浏览器（甚至是 Chrome）中尚未被支持，但我们可以通过使用 `require` 或者在将我们的 ES6 代码转译为 ES5（现在几乎所有的浏览器都能理解了）后再发送到浏览器进行渲染，来开始编写模块化程序。当浏览器追上进度时，我们就不再需要**转译（transpile）**。当这种情况发生时，React 将成为你随处可见的更常见的库。最终，无论是否有 React，模块化的 JavaScript 程序设计将成为常态。

**可扩展性。** 在 React 中，每个 HTML 元素都被视为一个可以编程的组件，可以嵌套在其他组件中。子组件与其父组件关联。

父组件和子组件之间的关系通过被称为 **props** 的东西建立。*React 程序的可扩展性是通过让每个组件都成为 HTML、CSS 和 JavaScript 代码的集合来实现的。

诚实地说，在 React 中应用 CSS 有点奇怪且具有局限性。随着你对库的了解增加，你会发现这一点。但通常情况下，React 遵循常见的 CSS 规则。

**灵活性。** React 不仅仅是一个 UI 视图库，这与你开始研究它时可能听到的说法不同。而且这并不完全错误。

React 赋予我们创建极快速交互式组件的能力，这些组件可以作为我们应用程序的元素。

然而，React 利用了**渲染目标（render targets）**原则，这允许你将代码的结果发送到任何地方。即使它只是一个文件，而不一定是前端视图。

**可重用性。** React 组件具有极的可重用性。一旦你编写并编写了一个 React 组件，你可能再也不需要重复这样做。

React 意味着对几种原则的理解。但根结底，React 是一个极简的库。它是经过时间考验的编程技术的组合，专业 Web 开发者将其集成到一个实用的库中。

这种方法极地提高了可重用性，一旦彻底理解，它将是神奇的。

**受雇主的欢迎。** React 是由 Facebook 的程序员在多年研究 Web 后开发的。它现在由 Facebook 和 Instagram 的开发者维护。在多程度上，它源于一组经过证明的软件工程哲学。尽管许多传统的 JavaScript 程序员并不熟悉其中的许多内容。

当你学习 React 时，你是在**学习计算机编程原理**，而不仅仅是函数和方法列表。没有这些原理，理解 React 将是一项艰苦的学习。

然而，在 2016 年，JavaScript 已成为前端 Web 开发的主导语言。如果你在软件行业寻找工作，在简历上拥有 React 将让你比竞争对手更有优势。

在旧金山湾区——这几乎是软件开发世界的圣地——平均高级 JavaScript 程序员年薪为 12 万至 15 万美元。

React 的虚拟 DOM 是帮助你实现这一点的机制。它是 React 的一个巨大的核心特性。你在 React 中将将做的每项工作都将以某种方式与它相关。而且只有当你准备好渲染组件时，才能通过将其**挂载（mounting）**到 UI 上来实现。你将在书后部分听到更多关于这个术语的内容。

**模块化设计。** React 支持模块化设计，这通常与构建大型**可扩展**应用程序相关。其原因为 2015 年发布的 `EcmaScript` 6 规范提供了新特性，该规范提供了有利于模块化方法论的新语法。例如，**require** (ES5) 和 **import** (ES6) 关键字不仅将文件连接在一起，还假设了对象之间基于类的关系。

尽管在编写本文时，**import** 关键字在现代浏览器（甚至是 Chrome）中尚未被支持，但我们可以通过使用 `require` 或者在将我们的 ES6 代码转译为 ES5（现在几乎所有的浏览器都能理解了）后再发送到浏览器进行渲染，来开始编写模块化程序。当浏览器追上进度时，我们就不再需要**转译（transpile）**。当这种情况发生时，React 将成为你随处可见的更常见的库。最终，无论是否有 React，模块化的 JavaScript 程序设计将成为常态。

**可扩展性。** 在 React 中，每个 HTML 元素都被视为一个编程的组件，可以嵌套在其他组件中。子组件与其父组件关联。

父组件和子组件之间的关系通过被称为 **props** 的东西建立。*React 程序的可扩展性是通过让每个组件都成为 HTML、CSS 和 JavaScript 代码的集合来实现的。

诚实地说，在 React 中应用 CSS 有点奇怪且具有局限性。随着你对库的了解增加，你会发现这一点。但通常情况下，React 遵循常见的 CSS 规则。

**灵活性。** React 不仅仅是一个 UI 视图库，这与你开始研究它时可能听到的说法不同。而且这并不完全错误。

React 赋予我们创建极快速交互式组件的能力，这些组件可以作为我们应用程序的元素。

然而，React 利用了**渲染目标（render targets）**原则，这允许你将代码的结果发送到任何地方。即使它只是一个文件，而不一定是前端视图。



**可重用性。**

React 组件具有极高的可重用性。一旦你编写并编写了一个 React 组件，你可能再也不需要重复这样做。

React 意味着对几种原则的理解。但归根结底，React 是一个极简的库。它是经过时间考验的编程技术的组合，专业 Web 开发者将其集成到一个实用的库中。

这种方法极大地提高了可重用性，一旦彻底理解，它将是神奇的。

**受雇主的欢迎。**

React 是由 Facebook 的程序员在多年研究 Web 后开发的。它现在由 Facebook 和 Instagram 的开发者维护。在很大程度上，它源于一组经过证明的软件工程哲学。尽管许多传统的 JavaScript 程序员并不熟悉其中的许多内容。

当你学习 React 时，你是在**学习计算机编程原理**，而不仅仅是函数和方法列表。没有这些原理，理解 React 将是一项艰苦的学习。

然而，在 2016 年，JavaScript 已成为前端 Web 开发的主导语言。如果你在软件行业寻找工作，在简历上拥有 React 将让你比竞争对手更有优势。

在旧金山湾区——这几乎是软件开发世界的圣地——平均高级 JavaScript 程序员年薪为 12 万至 15 万美元。

**虚拟 DOM。**

它非常快。这可能是 JavaScript 程序员想要开始使用 React 库编写应用程序的首要原因。它通过利用 **DOM 的虚拟副本**，被设计为执行“虚拟化”操作。换句话说，在这些操作被渲染到标准的 JavaScript DOM 树之前，它们是相似但并不相同的。

令人惊讶的是，将 UI 移动到虚拟 DOM 实际上改变了终端用户对应用程序的感受。你可能已经在 Netflix 等网站的整个网络上开始注意到这种现象了。

React 的虚拟 DOM 是帮助你实现这一点的机制。它是 React 的一个巨大的核心特性。你在 React 中做的每项工作都将以某种方式与它相关。而且只有当你准备好渲染组件时，才能通过将其**挂载（mounting）**到 UI 上来实现。你将在书后部分听到更多关于这个术语的内容。

**模块化设计。**

React 支持模块化设计，这通常与构建大型**可扩展**应用程序相关。其原因为 2015 年发布的 EcmaScript 6 规范提供了新特性，该规范提供了有利于模块化方法论的新语法。例如，`require`（ES5）和 `import`（ES6）关键字不仅将文件连接在一起，还假设了对象之间基于类的关系。

尽管在编写本文时，`import` 关键字在现代浏览器（甚至是 Chrome）中尚未被支持，但我们可以通过使用 `require` 或者在将我们的 ES6 代码转译为 ES5（现在几乎所有的浏览器都能理解了）后再发送到浏览器进行渲染，来开始编写模块化程序。当浏览器追上进度时，我们就不再需要**转译（transpile）**。当这种情况发生时，React 将成为你随处可见的更常见的库。最终，无论是否有 React，模块化的 JavaScript 程序设计将成为常态。

**可扩展性。**

在 React 中，每个 HTML 元素都被视为一个编程的组件，可以嵌套在其他组件中。子组件与其父组件关联。

父组件和子组件之间的关系通过被称为 `props` 的东西建立。React 程序的可扩展性是通过让每个组件都成为 HTML、CSS 和 JavaScript 代码的集合来实现的。

诚实地说，在 React 中应用 CSS 有点奇怪且具有局限性。随着你对库的了解增加，你会发现这一点。但通常情况下，React 遵循常见的 CSS 规则。

**灵活性。**

React 不仅仅是一个 UI 视图库，这与你开始研究它时可能听到的说法不同。而且这并不完全错误。

React 赋予我们创建极快速交互式组件的能力，这些组件可以作为我们应用程序的元素。

然而，React 利用了**渲染目标（render targets）**原则，这允许你将代码的结果发送到任何地方。即使它只是一个文件，而不一定是前端视图。

**React 与 jQuery 的对比。**

布局定义。它几乎就像是带有某些动态功能的 `LoginForm` 重用模板。

第二个代码块是执行 Ajax 语句的实际程序。这行代码将根据传递它的数据（用户名和密码）从 PHP 脚本加载数据，并在 `msg` 变量返回某种类型的消息。

最后，使用 jQuery 通过替换类名为 `Name` 的 `div` 内容为从脚本接收到的消息来修改 DOM。

一段时间内，这种方法运行得很好。在过去的几年里，这就是我们习惯处理网页上动态元素的方式。

React 的卓越之处在于，它吸收了这一切，并赋予我们对 HTML 和动态数据的程序化控制，而这一切封装在一个整洁的 `render` 函数中：

```javascript
render : function() {
  return <div>{
    this.state.name ? this.state.name :
    <span>Enter username here</span>
  }
</div>;
}
```

注意 HTML 和 JavaScript 代码是如何交织在一起，而无需打开单独的标签。它们存在于同一个 JavaScript 语句中，并且几乎可以无间隙地交替使用。我们很快就会介绍如何实现这一点。

当然，这个孤立的示例在用于实际应用之外几乎没有任何意义。但它展示了一些重要的原则。

这段借用 JSX 语言的 JavaScript 跨 HTML 语法的 `React` 代码让我们有了一种方法，通过简短查看代码就能知道动态元素的输出是什么样子。`React` 在这里试图满足所有人的需求。在某些情况下，你会注意到一些模式，它们感觉几乎就像是将后端逻辑引入了前端。

这个示例使用了三元运算符 `? :`。基本上，它的意思是如果属性名存在（不等于 `null` 或 `undefined`），那么我们应该输出它。如果它不存在，我们应该输出通用的“Enter username here”作为默认消息。

这将 HTML 模板方法带到了一个不同的维度。在这里，我们同时在设计和编写组件。

这只是第一章，我已经在深入 React 编程的复杂性了。然而，让我们回到基础，首先将一些重要的原则拆解成较小的教程片段。这对我们以后的道路会有帮助。

就像我的 jQuery 宝石一样，我们将从一组“宝石”开始，这些是先决知识，提供了向前移动所需的快速且富有见解的信息片段。因为软件行业目前正处于 EcmaScript 5、6 和 7 之间的过渡时期，这有助于我们排除常见的怪癖，并在当我们学习书中其余课程时，专注于重要的事情。

如果跳过了这些宝石，稍后书中的某些部分可能就没那么好理解。特别是在你接触 JavaScript 语言的第一步就开始学习 `React` 的话。

但宝石只是书的一部分。它们的设计初衷是尽可能减少动荡，并帮助你在反应式原则的提示下，轻松地进入现代 JavaScript 编程的世界。



在深入下矿井之前，你必须理解这些想法。宝石将磨利你的铁镐。书的第二部分将向你展示洞穴的其他部分。

为了让你的旅程更加轻松，我在这里包含了这一部分，代表了 React 程序的每个独立方面。系好安全带，准备好吸收大量的新原则。我们现在正进入 React 编程的世界！这是一个鸟瞰式的解释，涵盖了构建 React 程序涉及的最重要概念。

我已经提到过，学习 React 是碎片化的。而且它假设你具备高级编程模式的先前知识。在本节中，我将尝试将它们拆分为可以单独分析的合理区块。随着我们的进展，这将帮助你拼凑出拼图。你可以把这里描述的原则是驱动 React 核心引擎的想法。

仅仅因为它们在这里被整齐地列出，并不意味着学习 React 会变得很轻松。但通过花时间熟悉它们，确实会让阅读书的其余部分变得更容易。

## React 中的元素创建

如果你熟悉 jQuery，你就使用过美元符号 (`$`) 对象来选择 HTML 元素并对它们应用各种操作。但当涉及到 HTML 元素时，React 中类似的构建块是什么？那一定是 `createElement` 方法。

```javascript
React.createElement(type, props, children);
```

这里是你在实践中如何使用 `createElement` 的几个示例：

```javascript
let link = React.createElement('a', {href: '#'}, "Save");
let nav = React.createElement(MyNav, {flat: true}, link);
```

我们刚刚使用 React 方法 `createElement` 程序化地创建了 HTML 元素。然后我们将创建的 `link` 元素放置在 `nav` 元素中作为它的子元素之一。当然，在这种情况下 `link` 是唯一的子元素，也可以使用多个链接作为逗号分隔的额外参数：

```javascript
let link1 = React.createElement('a', {href: '#'}, "Save");
let link2 = React.createElement('a', {href: '#'}, "Delete");
let nav = React.createElement(MyNav, {flat: true}, link1, link2);
```

你可以一直这样下去，添加应用程序所需的任意数量子元素。

注意 `nav` 变量使用了 `MyNav` 而没有双引号。这在 React 中是完全没问题的。当我们使用自己定义的自定义元素（而不是 `a`、`div`、`table` 等标准元素）时，我们必须使用大字母开头。在 JSX 中，它将翻译为 `<MyNav />`。

实际上，以下是按照示例所示创建元素的方法：

```javascript
let nav = React.createElement(MyNav, {flat: true},
// nav 的子元素
React.createElement('a', {href: '#'}, 'Save'), // link
React.createElement('a', {href: '#'}, 'Load'), // nav
React.createElement('a', {href: '#'}, 'Delete'), // link2
React.createElement('a', {href: '#'}, // AlertContainer (等等，这是 React.createElement('a', {href: '#'}, AlertContainer)
// AlertCounter 的子元素
React.createElement('span', {alerts: 0}, "No Alerts"));
```

注意某些子元素是简单的文本字符串。它们在这里用作文本节点。当它们不用于指定嵌套元素时，它们被用作 `innerHTML` 的文本。

## JSX 语法

所以，在 ES5 中你会使用 `createElement` 函数，而在 JSX 中（其常见用法是与其他 ES6 语法一起使用），你可以通过简单地编写如下内容创建完全相同的功能：

```javascript
let link1 = <a href="#">Save</a>;
```

现在你明白我想表达什么了吗？JSX 将 HTML 转换为 JavaScript 语句。在这里 `link1` 是元素的对象表示，与我们之前使用 `createElement` 方法创建的 React 代码完全等价。是的，只需将其声明为 JSX，`link1.href` 就会包含 "#"。

一旦我意识到这就是它的工作原理时，JSX 就开始变得非常有意义，我实际上也开始觉得使用它非常舒服了。它就像是 HTML 和 JavaScript 之间的一双向道，属性会自动变成属性。

这里有一个更复杂的例子，这次再次在 JSX 中：

```jsx
let nav = <MyNav>
  <a href="#">Save</a>
  <a href="#">Load</a>
  <a href="#">Delete</a>
  <a href="#">
    <span alerts="0">No Alerts</span>
  </a>
</MyNav>;
```

我们刚刚使用 JSX 语言通过单一的 JavaScript 语句重新创建了虚拟 DOM！你可以将 `nav` 的值作为语句传递到函数中。这几乎就像是创建微型 DOM 结构的另一种方式。

现在你（希望）看到了，这就是 React 中虚拟 DOM 的真实结构。它就像是我们我们将处理的次级 DOM，对其进行更改、修改、编辑、删除和添加子节点等操作。我们将更新负责应用程序中可见元素的实际 JavaScript DOM 对象……但只有在它实际上需要更新时。我们执行的任何虚拟 DOM 操作都不会与花费时间更新原始 DOM 相关。这正是提高 React 应用程序性能的原因。

最好的一点是，React 为我们自动完成了这一切。作为一名 React 程序员，你不需要理解 React 内部是如何做到的。你只需要专注于你应用程序的设计。

请注意，如果你直接在 JavaScript 应用程序中输入 JSX 代码，它甚至无法编译。你必须运行 JSX 处理器。要做到这一点，你通常需要从命令行初始化它，这样它就能在后台持续运行。

Babel 有一个 JSX 插件。我还建议你学习如何让 babel 监控你的文件。这意味着，你可以设置 babel，使其在文件发生变化时立即自动转译你的 `*.js` 文件（并将它们放入 "build" 或 "production" 目录）。这种 babel 功能被称为 "watch"。必须先启用。我在我的视频教程中解释了如何在 Windows PC 上进行操作。

YouTube 上的 React 教程，可以帮助你设置开发环境、安装 Node.js、NPM、babel、JSX，并帮助你开始监控你的 JavaScript 文件：

```
https://www.youtube.com/watch?v=tXaNvGcjEio
```

你可以简单地在网页顶部或底部的 `SCRIPT` 标签中添加 `babel.js` 来解决问题。JSX 可以正常转译。但这将显著减慢应用程序的处理。它应该只用于测试。

另一方面，视频只有 58 分钟，如果你认真要设置一个专业的 Web 开发环境，我建议在 YouTube 播放器上以 2 倍速度快速浏览，这只需要大约 25 分钟。它像是一门微型入门介绍课程。

## 元素克隆与渲染

最后，我们通过展示你也可以使用 `cloneElement` 克隆现有元素来为讨论画上句号。

```jsx
React.cloneElement( element, props, children );
```

它的工作方式与 `createElement` 完全相同。只需将现有的元素作为 `element` 参数传递即可。然后，你传递给相应参数的任何 `props` 和 `children` 都将合并到原始元素已有的属性中。这让我想起传统面向对象编程中扩展对象的功能。在这里，我们某种程度上是在模仿 OOP 功能。

创建的元素现在可以实际渲染到 DOM 中。你不能渲染到虚拟 DOM。`render` 函数是 React 库内部处理这一过程的魔法。这就是我们的元素从虚拟 DOM “复制并粘贴”到屏幕上可见的实际 DOM 的时刻。

React 在主 `ReactDOM` 对象上提供了 `render` 方法，如下所示。在响应式编程中，`ReactDOM` 是仅于 React 之后最重要的对象。

```jsx
ReactDOM.render( reactElement, domContainerNode );
```

在这里，`domContainerNode` 是 `reactElement` 将被渲染、重新渲染或首次挂载（mount）的父元素。如果你需要更新组件的属性，可以多次使用 `render`。

这是一个现实场景可能的样子如下。在这个例子中，我们获取一个 `ReactElement` 并将其渲染到 DOM 节点上：

```jsx
ReactDOM.render(
    React.createElement("div",
    document.getElementById("container")
);
```

如果你有一个元素已经与变量名关联，可以使用 `ReactDOM.findDOMNode` 查找它：

```jsx
ReactDOM.findDOMNode( element );
```

该语句返回与给定元素关联的 DOM 节点。请注意，这只有在元素通过 `render` 方法渲染到 DOM 之后才能生效。在此之前，即使它已经创建，在 DOM 中也是无法找到的。

## 特殊 props 属性

在这里我们将简要讨论一些特殊的 prop 名称，大约有几个。这些名称应该被处理得类似于 JavaScript 中的保留关键字，但在 React 中除外。它们都有特殊的含义。

- `children` 属性名由 `React.createElement` 自动添加到 `this.props` 中。
- `className` 属性对应于 HTML 的 `class` 属性。你必须在组件/元素中使用 `className` 而不是 `name`，以避免与 HTML 的保留关键字冲突。
- `htmlFor` 与 `className` 相同，仅用于 "for" 属性。在 React 元素任何需要使用 "for" 属性的地方应使用 `htmlFor`。
- `key` 属性唯一标识一个 `ReactElement`。它用于数组中的元素。
- `ref` 属性接受一个回调函数，该函数会被调用。带有组件实例 DOM 节点时调用。
- `style` 属性接受一个样式对象，而不是字符串。在 React 中，没有以文本字符串指定 CSS 样式的机制。但这种局限性也可以被看作是一种优势，因为 CSS 样式现在可以以编程的方式表示，样式对象中的每个属性代表 CSS 属性对。起初可能觉得有点奇怪，但这种风格实际上更符合 React 的整体方案。

React 有一个名为 `propTypes` 的特殊属性。它的主要目的是类型检查。随着你的应用程序变得很大，类型检查可以帮助发现错误。这是一个例子。假设我们已经创建了一个名为 `ReactComponent` 的 React 组件。默认情况下在开发模式下开启类型检查。在生产代码中实际上没有开启。

```jsx
ReactComponent.propTypes = {
  name: React.PropTypes.string
};
```

我们在书剩下的部分通过示例多次讨论组件。它们是你应用程序的构建块。

## React 组件结构

现在让我们简要概述 React 组件的常见结构。它是 React 库默认提供的选项和方法。

组件通过存在于 React 对象上的 `createClass` 方法定义：

```jsx
var MyComponent = React.createClass({
  displayName: 'MyComponent',
  /* 这是你 React 类的核心
  选项和生命周期方法将写在这里 */
  render: function() {
    // 渲染后，让我们返回一个新创建的元素
    return React.createElement(/* ... * */);
  }
});
```

这是类的基本结构。下面我列列出了 React 类默认可以拥有的几种方法。它们被假设为可用的。也就是说，就像在上面的示例中看到的 `render` 函数一样，这些是可以在类内部的方法。并不是每个 React 方法都一定需要使用它们。

组件持有 `propTypes` 对象以及另外两个返回对象的方法：

| propTypes | 属性名到类型的映射对象 |
| :--- | :--- |
| getDefaultProps | 返回 props 对象的函数 |
| getInitialState | 返回 state 对象的函数 |

以下是生命周期方法：

- `componentWillMount`
- `componentDidMount`
- `componentWillReceiveProps`
- `shouldComponentUpdate`
- `componentWillUpdate`
- `componentDidUpdate`
- `componentWillUnmount`

这些方法可以在你的 React 类中实现。并不是所有的组件类都要求使用这七个函数。这取决于你组件的用途。每个方法基本上都是在 React 组件生命周期内特定时间执行的事件。这些功能大部分都与检查组件的挂载和更新状态有关。除了这些方法之外，当然，你也可以根据组件预期要执行的操作添加你自己的自定义函数。

组件实例是从我们在上一个节中查看的类表示所实例化的对象。以下是关于它们实现的一些提示：

1. 组件内部的 `this` 关键字指向组件它本身。
2. 无状态函数组件没有组件实例。
3. 一个组件实例可能会跨越多个等效的 `ReactElements`。

属性 `this.props` 包含了通过标签属性传递给 `React.createElement` 的任何 props。`this.state` 属性包含了由 `setState` 和 `getInitialState` 方法设置的状态。`setState(changes)` 将给定的更改应用到 `this.state` 以重新渲染 DOM 组件。`forceUpdate()` 立即将组件渲染到 DOM。

## 组件的核心概念

在这一节中，我将介绍几个“宝石”（gems），它们扩展了响应式编程，并对一些重要原理进行了一些解释。每个宝石都是对特定主题的深入讨论。宝石的设计是为了逐渐扩大你对 React 库核心原理的视角。

组件是 React 应用的构建块。由于 React 主要用于考虑应用程序视图（交互式用户界面动态），React 组件可以被认为是你的 Web 应用程序所的视觉块。React 将每个组件视为一个可重用的模板。在 React 中，每个组件都是 HTML、CSS 和 JavaScript 代码的集合，它标识了你应用程序中的一个特定区块。

例如，这里是我从 React 组件的角度来看我的 Twitter 页面 @gregsidelnikov。在程序上，React 组件遵循了嵌套 HTML 标签的足迹。它们有父元素和子元素，父元素也可以是层次链中另一个组件的子元素。

将组件设计构成你整个应用程序的蓝图。在开始为你的响应式应用程序编写第一行代码之前，在纸上把它们全部规划出来是一个很棒的主意。这是一种直观的思考方式，将你的页面设计成一个具有独特元素的 Web 应用程序。

就像你多年前第一次学习普通 DOM 时，意识到每个 HTML 元素（如 `P`、`DIV`、`TABLE` 等）实际上是对象模型中长树状链中的一个对象一样，把 React 组件看作视觉区域，它们同时也与某种软件函数相连。这一次，功能性将由你和你的应用程序的需求进行自定义决定。

从这些 React 最基础的原理中，你现在可以看到为什么 Facebook 和 Instagram 喜欢使用它。它是极速的，它帮助拆解由组件组成的流式元素，而这些组件仅仅是 CSS、HTML 和 JavaScript 代码的集合。这种设计模型更接近应用级行为，而不是仅仅是使用表格类布局的纯信息类网站。

组件是层级化的。它们可以是其他组件的子元素。在大多数情况下，组件是为了在你的应用程序中复用而定制的。它们包含了代码模式，这些模式可以适应各种情况。React 代码通常遵循一种创建这些组件链的模式，这些链在内部工作，同时保持了快速的渲染速度和灵活性。

很有可能在构建普通的 HTML-JavaScript 应用时，你已经在某种程度上将你的应用分成了不同的隔间。然后，你使用 Ajax 事件根据每个 HTML 元素单元格中更改的数据类型分别填充每个视图。

但 React 通过要求 `render()` 方法更进了一步。`render()` 方法必须附加到你创建的每个 React 组件上。没有办法逃避它。它是 React 组件所要求的使用的模式的一部分。

尽管 React 远不止于视图层——在用 React 编程时显式地使用渲染方法，正是 React 经常被认为主要是基于视图的库的原因。我们将在整本书中看到为什么这是真的，以及为什么这并不完全正确。

说 React 编程仅仅是仅限视图的编程是不公平的。事实上，渲染目标的这种告诉了我们相反的结论。React 是一种遵循基本哲学的编程模式，这种哲学实际上并不需要视图。

你可以将 React 组件的结果渲染到浏览器，或者渲染到文本字符串（使用专门为此创建的方法，称为 `React.render()`）、JSON 对象或你要求的任何地方。在这种情况下，渲染根本不是渲染。“渲染”（render）这个词意味着数据的视觉化。因此，React 更像是一组原理，而不是许多学者在简要熟悉该库之前倾向于认为的“制作用户界面的方法”。

虽然你可以在 React 之外使用任何第三方库（例如数据库 IO 库），但 React 在视图元素背后的自定义编程方面仍然提供了很多内容。事实上，它要求你理解这些编程原理是如何工作的。



通常附加到 React“虚拟”DOM 的`render()`方法是在你的应用程序首次加载到浏览器时将执行的方法，因此，只有当它所代表的元素中的数据应该更新时，它才会执行。然而，这正是有趣之处。在`render`方法被调用之前，React 组件甚至还没有“挂载”到 JavaScript DOM，也不会被显示。而且可以在没有它们的情况下创建 React 组件。我们将在宝石 6 中详细地介绍挂载。

我们知道`render`会触发数据集（或组件状态）的更新。但什么时候应该更新数据呢？这取决于你组件中显示的数据类型，也取决于一些在关键时间更新它的通用函数。在书的后续章节（此处误译为 Later in the book），我们将介绍负责赋予我们控制这些事件的函数。

在真实场景中，元素本身可以是警告图标，通知最终用户警告数量、粉丝数量或简介访问量的增加。

React 让我们仔细思考每个元素将代表什么，因为每个组件都与某种软件函数相连，该函数将实时更新组件中的数据而不更新布局。在 React 中，这个过程与传统应用程序相比变得更加高效。你不需要像在普通 HTML 网站上那样加载整个页面。

这让你的应用程序感觉不同，并节省了带宽。如果你想，我们直到 2017 年构建的非响应式网站实际上只是一个懒人的设计想法。为了查看是否有新警告而重新加载所有内容并不是最好的应用程序设计。是的，这就是 Facebook 这样的网站一直以来工作的方式。而且一点一点地，它开始改变了。这就是为什么它们正在转向响应式实现。

但响应式编程不仅仅是一一组获取数据并替换 HTML 元素的 ajax 调用。它要复杂得多。

而且由于快速访问所有相关组件通常是良好的应用程序设计的关键，这就是虚拟 DOM 出场的地方。

在。虚拟 DOM 是一种提供快速修改 DOM 的奇特方式，同时放弃了速度较慢的旧替代方案。

虚拟 DOM 无疑是选择 React 库编写应用程序的巨大优势之一。事实上，当你为 Web 项目添加 react 库时，你也应该添加`react.dom`库。这两者是不可分割的。而且所有的响应式 JavaScript 应用程序默认都包含了 React DOM 库。

这就是 React 的虚拟 DOM 在你的应用程序易用性上产生巨大差异的地方。它让所有网站具有原生应用程序的体验，每个元素都能对触摸事件做出即时响应。

你可能已经在 Netflix、Facebook 和 Instagram 等网站上看到过这种现象了。你实际上可以感受到这种不同。操作发生得非常快，似乎不需要每次点击按钮都先等待 HTTP 请求加载。

应用程序会立即响应。React 并没有消除 HTTP 带宽，它只是将其降至最低，并仅关注数据是否真的因为某个事件（例如，按钮点击事件）而需要传输。

当然，像 Netflix 和 Amazon 这样的网站会预加载部分数据（例如电影预告片的前 15 秒），无论用户是否点击了播放按钮。但与其他“响应式”原则相结合，它对 UI 响应性产生了巨大影响。

我们仍然在使用熟悉的 HTML 元素来构建应用，但对每个事件的响应率是由一个比 jQuery 实现快得多的 DOM 提供的。

为了开始使用虚拟 DOM，你不需要做任何特殊操作。通过利用 React 组件模板模式，你实际上正在使用 React 自己的虚拟 DOM 遍历。它通过提供与我们熟悉的名称相匹配的驼峰命名方法和属性（如`className`和`fontFamily`），透明地模仿了标准的 DOM 模型。

在本书的编写期间，Web 仍处于从 EcmaScript 5 到 EcmaScript 6 的某种过渡阶段。当 EcmaScript 2015 (ES6) 在大约两年前发布时，它在 JavaScript 世界引起了巨大的动荡，并将程序员分为“旧方法”和“新方法”两类。有些人根据自己的喜好毫无问题地使用其中一种风格。这两者并没有优劣之分。

然而，最终 ES5 和 ES6 执行的是完全相同的代码。大部分区别在于语法上。诚无疑，同时在两种不同的语言中工作可能会产生不必要的头疼，特别是当你初次学习 React 时。

在像 JavaScript 这样的松类型语言中，任何事情都根本不存在“一种标准方法”。这一直以来如此。

在创建 React 组件时，区分这种区别至关重要。实现它的方法不止一种。

在本 gem 中，我将演示如何用两种不同的方式创建两个完全相同的 React 组件。这里的区别在于 EcmaScript 5 和 EcmaScript 6 本身的区别。

在大多数情况下，显著的区别在于构造函数（ES6）和专门的初始化状态函数方法（ES5）的使用。让我们来看一下。

EcmaScript 5 的示例如下：

```javascript
var NewComponent = React.createClass({
  getInitialState() {
    return { /* initial state */ };
  });
```

注意，在 EcmaScript 5 中不存在`constructor`关键字。这就是为什么在这种情况下 React 提供了`getInitialState`函数。如果你在用 ES5 编写应用程序，应该使用此方法来初始化组件的默认状态。

我们很快就会讨论状态（states），因为这是一个非常重要的主题！

状态与 React 组件绑定在一起。在规划应用程序时，你应该在组件和它的状态之间建立一种心理关联。每个组件都负责拥有自己的状态。

在上面的源代码示例中，我们演示了 ES5 语法。我不会告诉你应该使用两者中的哪一个。

最终，ES6 将在几年后（或更早）成为新采纳的标准，但许多程序员仍然会偏于 ES5 格式。

两者仍然可以工作，因为 JavaScript 支持 ES5 作为 ES6 的子集以兼容未来的应用程序。如果这符合你的需求，请像下面所示使用 EcmaScript 6。现在我们只是在使用 ES5 中不可用的新关键字：`class`、`extends`、`super`和`constructor`：

```javascript
class NewComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { /* initial state */ };
  }
}
```

它们是一是一样的，只是使用了 ES6 语法。如果你来自 Java、C# 或 C++ 语言，你可能更熟悉这种类创建语法，并可能偏于它优于过时的 ES5 格式。

注意这里的另一个区别是我们使用`.Component`方法来创建组件，而不是`.class`。但本质上，底层发生的是完全相同的事情。

我知道用两种不同的方法做同样的事情听起来可能很困惑。但在这里你有选择：使用 ES5 你的代码开箱即用，或者使用 ES6 语法并将其转换回 ES5。然而，学习较新的 ES6 语法的优势在于，你的应用程序看起来会更简洁、更直观。

这只是我们目前正面临的时期，随着 JavaScript 规范的成熟。在浏览器完全采用 EcmaScript 6 之前，学习这种语法格式会带给你一种优势，即学习一些尚未被广泛使用、但在未来几年内绝对会成为下一个标准的内容。

我个人的偏好是开始使用 EcmaScript 6 语法。这条路可能会有点坎坷，但一旦你过了学习曲线，这就会变成本能。好消息是，这些类型总是需要付出努力。

在 React 中，每个组件都有一个*state*。*state*是一个带有值的对象。*state*正如其字面意思。它是组件通过数值、布尔值、数组或映射指定的标志、参数和设置的状态。

React 组件的生命周期与状态有很大关系。React 提供了几个默认方法帮助我们编写高效的应用程序。这些方法将在接下来概述。

每个组件通常通过默认方法控制自己的状态。它们被设计用于在应用程序流或生命周期的独特时刻修改或更新状态。

所有这些方法都像下一页所示附加到组件对象。注意，这只是一个演示这些方法在你 React 对象中位置的简单示例。我必须将源代码移动到下一页，以免它被分页截断。

```javascript
var MyComponent = React.createClass(
  displayName: 'MyComponent',
  // 这就像组件的构造函数！
  getInitialState: function() { ... },
  // 组件挂载事件
  componentWillMount: function() { ... },
  componentDidMount: function() { ... },
  componentDidUnmount: function() { ... },
  // 组件更新事件
  componentWillReceiveProps: function() { ... },
  componentWillUpdate: function() { ... },
  componentDidUpdate: function() { ... },
  shouldComponentUpdate: function() { ... },
  // 将组件渲染到 DOM
  render: function() { /* return something */ }
);
```

有一大堆 “Will” 和 “Did”。但它们到底意味着什么？下面我将为每个方法在组件生命周期各个阶段所负责的事件提供简要描述。

`getInitialState`函数的作用类似于组件构造函数。它在组件渲染到屏幕之前被调用。

`componentWillMount`在`render()`方法执行之前仅调用一次。在组件的整个周期内，它不会再次被调用。有时它被用作组件构造方法的同义词。

`componentDidMount`在组件首次渲染后立即被调用。

`componentWillUnmount`在组件即将被销毁时调用。这是清理内存和删除状态的地方。

`componentWillReceiveProps`在 props 传递给组件时调用。例如，如果你有一个`Form`组件和一个`TextInput`组件，后者允许用户通过输入文本来更改其值。想象如果`TextInput`有一个`onChange`事件，并向组件传递一些 props。一旦新文本被输入输入框，该值就会作为 props 传递给主组件。这就是`componentWillReceiveProps`被触发的时刻。

`componentWillUpdate`在组件上执行`render`方法的紧 之前被调用。它让我们有机会在下一次渲染更新之前处理任何状态更改。

`componentDidUpdate`在`render()`方法完成 DOM 更新后立即被调用。

`shouldComponentUpdate`是一个始终返回`true`的默认方法。它让我们能够控制组件元素是否应该在 DOM 中更新。情况并非总是如此。例如，如果组件中某些状态或属性的新结果无论如何都与其之前设置的值相等，那么可能就不值得更新 DOM。如果数据在更新后没有发生变化，为什么要将数据发送到视图呢？

这些方法对于理解虚拟 DOM 至关重要。随着我们慢慢揭开 React 编程的原理，一切将开始变得有意义。

目前，你只需要知道 React 组件通常会被挂载（mounted）到一个渲染目标上。这就是为什么上面提到的某些默认方法使用“mount”（挂载）一词，而不是你预期的传统的 setter 或 getter 方法（如“set”或“get”）。挂载是 React 编程以及在 React 虚拟 DOM 生态系统中创建的组件所特有的概念。

我们已经从理论上讨论了组件。但在实践中，组件到底是什么？记住，你的应用程序是由模块化的元素组成的。组件字面上可以是任何东西，从按钮、文本输入框、复选框到显示文本的操作状态区域。你将根据应用程序用途来确定组件的设计。

由于我们刚刚讨论了处理组件“挂载”的方法，那么在我们的下一个 gem（小章节）中探索它的含义也就是自然而！

## Gem 6 - 组件挂载 (Component Mounting)

React 是一个重视编程原则的库。其中之一是将组件视为元素的思想。组件是以程序化（声明式）的方式在你的应用程序中渲染你想要的内容。

但 React 实际上并不关心你选择在何处如何渲染这些元素。无论是在 JavaScript DOM 还是其他地方。这听起来可能令人惊讶，因为 React 以主要作为一个前端库而闻名。

这是因为 React 使用了被称为渲染目标（render targets）的东西。也就是说，你决定 React 的`render`方法的结果将如何显示或传递到其他地方。

换句话说，你可以说 React 在处理其组件存储的数据或状态的输出时是无关的（agnostic）。

例如……你可以将数据从组件输出到文件写入函数。换句话说，React 的渲染目标不仅限于 UI 元素，尽管在本书的大部分以及通用的 React 风格编程中，你处理的大部分都是这些。

在之前的 gem 中，我们讨论了每个组件如何处理自己的状态。状态可以是一个指示按钮是否被高亮的布尔标志，或者是一个导航菜单选项是否被选中。

现在，如果你一直关注，这就是这一切开始结合的地方。一个 React 组件是其状态与其渲染方法之间的融合。我们在一个地方对 UI 元素最重要的两个函数提供了程序控制。

但挂载（mounting）到底是什么？在 React 中，出于性能考虑，我们使用了 DOM 的虚拟表示。

通过简单地创建一个组件，任何 DOM 元素都不会被触及。这是一个好消息，但这怎么可能呢？这是因为使用原生 DOM 会增加应用程序的内存占用。然而，通过 React 的虚拟 DOM，元素只有在应用程序需要使用时才被创建。

我将详细解释这一点。

React 是一个同构框架（isomorphic framework）。它的功能可以映射到任意输出，而不只是 JSX 风格的 HTML UI 元素。

React 库提供的虚拟 DOM 正直就是：虚拟的。在应用程序真正需要使用之前，它物理上并不存在于 JavaScript DOM 中。

只需这样想：JavaScript 的 DOM 是存储在内存中的 HTML 元素的物理树。它在页面加载到你的浏览器时被填充。

通常当 页面加载到 Web 应用时，每个由 HTML 元素括号表示的 DOM 分支无论将如何被使用或是否显示在屏幕上，都会加载到主根 DOM 元素中。页脚会被加载到 DOM 中，即使它显示在浏览器的折线以下。

相反，React 甚至不会触碰 DOM 树。正如在之前的 gem 中讨论的，它在其自己的虚拟 DOM 中添加或删除组件，而虚拟 DOM 完全存储在内存中。只有当组件在你的应用程序中被正确使用时，元素通常才会内存中物理表示。这几乎就像是将虚拟 DOM 复制粘贴到渲染目标（无论它是什么）。在 Web 应用中，当然是 JavaScript DOM 树。

我将通过以下示例进行演示：

```
var component = React.createElement(ComponentDefinition);
```

此时组件是`ComponentDefinition`的实例。但它还没有在 DOM 中。它只是一个虚拟表示。它还没有被渲染。

将其渲染到 DOM 中，我们使用如下代码：

```
React.render(component, container);
```

此时，组件被渲染到 DOM 中。这就是我们所说的挂载（mounting）。组件现在是 DOM 的一部分，用户可以与其交互。

所以，挂载是将你的虚拟组件转换为实际 DOM 元素的过程。它是 React 工作的一个关键部分，是你需要很好理解的。在下一个 gem 中，我们将深入探讨组件的生命周期。

## Gem 7 - Node.js & NPM

当我说学习 React 涉及的内容比学习 React 库多得多时，这确实是真的。至少，使用 React 需要你安装 Node 库。

关于 Node 本身就可以单独写一本书，但对于 React 库来说，我们需要安装它有以下几个原因：

- 为我们的 React 应用提供本地主机（localhost）环境。安装 Node 让你能够在本地机器上运行 http://localhost 上的应用程序。

- Node 自动带有 Babel 和 JSX 支持（JSX 是作为 Babel 插件安装的）。

在 Mac（通过终端）和 PC 上，安装 Node 和 NPM 都出奇地简单。在 PC 上，这就像从它们的官方网站下载 Node 安装文件一样简单。运行安装程序就大搞定了。只需不要忘记在安装过程中勾选 babel 复选框，这样它也会被包含在内。

在 Mac 上，你可以通过命令行下载 Node。打开你的终端应用程序并输入：

```bash
$ get http://node
$ tar -xzf node-v0...
$ cd node-v0.4.4
$ ./configure
$ sudo make install
```

就是这样！配置日志将运行，然后你就完成了。

在 Ubuntu 上，你可能想要运行此额外的的命令来安装基本组件。

在 Mac 的终端中也是如此：

```bash
$ apt-get -y install build-essential
```

看起来此时此时 node 已经安装，并准备好为我们提供一个本地主机 http 地址，我们可以在那里测试我们的 React 代码。

好消息是，如果你已经在本地机器上安装了 Apache 服务器，并且它已经映射到你的开发文件夹，那么就没有必要使用 node 来提供本地主机环境。你已经设置好了。

在这种情况下，你只需在现有的 Apache http 文件夹（或你机器上映射的任何文件夹）中开始编写 React 程序。只需在该目录下创建一个新文件夹，例如 "my-react-app"，像往常一样，你的项目将可以通过浏览器通过类似的地址访问：

```
http://localhost/my-react-app
```

然而，仍然建议你安装 Node。出于任何原因——因为它带了命令行版本的 Babel/JSX 插件，这对于正确设置开发环境是必需的。

在 Mac 终端上安装实际上非常直接。但在 PC 上就稍微有点挑战性，特别是如果你以前从未做过的话。



如果你仍然不确定如何在 PC 上进行这些操作，我在 YouTube 上录制了一个 58 分钟的补充教程，可以在以下位置免费查看（我在下一页提供了链接）。

## React JS 教程 1 - 针对初学者 | ReactJS JavaScript ES6 Node.js, NPM, Babel 译器, Webpack

无论你处于开发过程的哪个阶段，都值得过一遍。但如果你刚刚起步，这是必看之。

观看这个教程应该能让你开始通过本地主机地址在 PC 上编写 React 应用程序。因此，在视频教程中，我将逐步演示整个过程。

我不想在书中重写这些细节以避免占用更多空间。你可以以 2 倍速观看，并在 25 分钟内看完。

## Gem 8 - JSX 详详解

如果你已经开始学习 React，你应该听过很多关于 JSX 的内容。你可能也听说在 React 中没有必要使用它。这确实如此。

但我建议你这样做。它让事情变得简单得多，尽管它的语法对传统的 JavaScript 开发者来说初看起来可能有点吓人。

JSX 以一种让你“在 JavaScript 内部编写 HTML”的语言而闻名。这确实……（此处文本重复/中断）。

## 第一节 - 编写你的第一个 React 组件

你现在看到的是一个紧凑的示例，展示了你可能编写的第一个 React 组件的样子。它简单地将通用的“Hello World”消息渲染到 DIV 元素中。它只需要一行代码。

```javascript
React.createClass({render: function() {
  return (
    <div>Hello World.</div>
  );
});
```

在这里，我们使用了主 React 库对象的方法 `createClass`。这就是创建组件的方式。但这段蓝色的代码是什么呢？它看起来像 HTML，但周围没有双引号包围它！

组件通常存储在变量中。

例如：

```javascript
var HelloWorld = React.createClass({ .. });
```

将组件存储在变量名中可以帮助我们在以后创建元素之间的父子关联。这仅仅是一种用程序化的方式在嵌套组件之间建立关系的方法。

这段代码中的部分内容看起来很奇怪，特别是如果你来自传统的 JavaScript 程序员背景。那些蓝色高亮的 JSX 代码看起来格格不入。

但请记住，React 编程与使用额外的工具有关。React 库本身应该是你整个应用程序的一部分。没有人会只使用 React 库来编写 React 应用。它只是墙上的单块石头。

在 React 中，我们可以在 JavaScript 内部编写 HTML。这与我们多年习惯的“在 HTML 内部编写 JavaScript”的思想相反，在传统情况下，我们将 JavaScript 写在 HTML 的属性标签中（例如 `onclick="this.style.color='red';"`）。

但 React 给了我们反向的能力。我们将在后续的学习中发现其中的原因。现在，让我们详细介绍创建组件，然后我将简要解释 JSX 如何帮助我们处理 HTML 块并将其视为返回值。

话虽如此，让我们来看创建第一个 React 组件并在特定的 HTML 元素中渲染其内容的完整示例：

```javascript
// 添加所需的库代码
var React = require("react");
var ReactDOM = require("react-dom");
// 创建我们的第一个 react 组件 "HelloWorld"
var HelloWorld = React.createClass({
  render: function() {
    return (<div>
      Hello World.
    </div>);
  }
});

// 在 id 为 "app" 的 HTML 元素内
//绘制 "HelloWorld" 组件
ReactDOM.render(<HelloWorld/>,
document.getElementById("app"));
```

注意，我们新创建的组件 HelloWorld 有它自己的 `render` 方法。但作为主渲染引擎的 ReactDOM 对象也有它自己的 `render` 方法。

两者之间的关系是，`ReactDOM.render` 会调用它作为第一个参数传递的组件的 `render` 方法。在这种情况下，就是我们的 HelloWorld 组件。

在这里，我们首先包含了上述的 React 和 ReactDOM 库。当你从零开始创建一个新的响应式应用时，你需要这样做。这就是初始化 React 的过程。

接下来，一旦我们在项目中包含了 React，我们将使用 `React.createClass` 方法创建一个 React 类的新实例。这并不是初始化 React 应用的唯一方法，但我们将在在本章中坚持使用这个示例。

最后，我们调用了 ReactDOM 自己的方法 `.render`。而这里的 `<HelloWorld>` 是分配给 React 代码的变量名 `HelloWorld`。基本上，React 的 `render` 方法接收两个参数。

你只需要将想要渲染的内容作为第一个参数，将想要渲染它的位置作为第二个参数（在本例中，它是 ID 为 "app" 的 HTML 元素）。因此，从现在起，任何分配给 `HelloWorld` 变量都将在渲染在类似 `[div id="app"]` 的元素中。

这正是 React 编程背后的基本思想。你构建组件并让它们在特定的 HTML 元素内执行操作。虚拟 DOM 会自动处理应用程序前端的快速渲染。

但还有一件事...

蓝色高亮的 HTML 代码是将被写入组件渲染区域的部分。是的，我们直接在 JavaScript 语句中输入 HTML。再次强调，这一功能是通过 babel 从你的 node.js 安装 JSX 插件来实现的。

设置这个过程有点复杂。但在我的 YouTube 教程以及本书的后后部分会有更详细的展示。

恭喜你创建了你的第一个 React 组件！我想保持内容的简单，不让你被设置 React 仍需完成的过多内容所困扰。但在未来的章节中，我们将继续逐步拆解使用 React 库进行编程，以及它具体包含什么。

### JSX

在 React 中，在 JavaScript 内部编写 HTML是通过开源 JSX 引擎实现的。你可以通过访问官方 GitHub 仓库来浏览 JSX 源码：

```
https://github.com/jsx/JSX
```

根据官方网站，JSX 是一种静态类型、面向对象的编程语言，设计用于运行在现代网络浏览器上。但涉及到 React 时，我们将使用它来以 JavaScript 格式编写 HTML 标签。这有点奇特且不寻常。但主要是，这赋予了我们像返回 JavaScript 语句一样返回 HTML 代码块的能力。你会发现这是非常有用且直观的。

JSX 简单地将 HTML 语法翻译回 JavaScript。起初看起来可能非常奇怪，但它就像 JavaScript 现在有了自己内部的 HTML 处理器。这种思维方式是熟悉 JSX 的良好起点。随着书籍的深入，我们将在源码示例中在更复杂的细节上探索它。

虽然很有吸引力，但完全理解 JSX 是如何做到的完全没有必要。它在内部处理这些，并帮助我们专注于编写代码。但主要是，这赋予了我们像返回 JavaScript 语句一样返回 HTML 块的能力。你会发现这是非常有用且直观的。

（注：原文后续部分存在大量重复的段落，此处已根据翻译要求进行去重并保留核心逻辑）

# 63

通过此 `this.props.children` 属性作为元素内部的“props”（或属性）。

通过这种方式，你可以在父类内部与子组件进行交互。父类通常是你的整个应用的核心，包含了所有其他次级组件。父组件可以有多个子组件。

我们以后会详细讨论 props 是什么。现在，只需要知道 props 对于 React 组件来说，就像参数对于函数一样。你只需将它们作为自定义值传递到对象中，用于满足响应式元素的功能。

此外，请记住，你不能随意粘贴任何 HTML 来作为 JSX 语句。JSX 版本的 HTML 与它非常相似，但并不是 100% 准确的 HTML 规范。它与 HTML 非常相似，但有几处不同。

正由于这些原因，JSX 起初可能会让你感到困惑。我自己也为此挣扎了一段时间，但当我意识到它的主要目的是帮助更快地编写代码时，我想一旦我适应并开始习惯性地使用它，长远来看它会让事情变得简单得多。

这几乎就像重新学习多年 HTML 标准的工作。最困难的部分在于了解 JSX 的局限性。因为当某些事情不起作用时，由于你不知道为什么，你可能会感到沮丧，即使你在 JSX 中使用的 HTML 看起来格式是正确的。

它确实挑战了你用新的方式去思考应用程序某些部分的设计。但请坚持这些示例，最终它们会进入你的脑海并开始变得更有意义。

### Props

在上一个章节中，我提到了 React 组件。但其中还有很多新内容。之前，我们创建了一个简单的组件，看起来就像这里这样：

```javascript
ReactDOM.render (<H1>Hello</H1>, document.getElementById('root'));
```

注意，我们直接将 `<H1>` 这样的 HTML 标签作为参数输入到 `render` 方法中，而没有将其放在引号内。这是 JSX 提供的语法风格。它在 JavaScript 中通常无法编译，但像 PHPStorm 这样的智能 IDE 能够识别 JSX 语法，并且不会将其视为错误。

只要你的项目项目中包含了 JSX（通常通过 `babel.js` 库或其对应的命令行插件，后者是我建议在生产服务器上使用的），它就能正常编译。

现在我们已经知道，这只有在你的项目中包含了 `babel.min.js` 的情况下，它才能生效。换句话说，不要尝试在“桌面”的某个文件夹里的记事本里写这段代码。你的开发环境必须正确配置才能编译，或者至少在你的页面 `<script>` 标签中包含 `babel.js`。它使用内部的 JSX 处理器将这些内联 HTML 转换为 JavaScript。

### 函数纯性 (Function Purity)

在深入讨论 React props 之前，我想提一点。在 React 中，props 是只读的。这与一种特殊类型的函数——纯函数”（pure function）有关。在传统的软件开发中，纯函数是指其内部不会改变传递给它的参数。例如：

```javascript
// 纯函数；不修改参数值
function sum(a, b) { return a + b; }
```

这被认为是一个纯函数，因为它的体没有修改任何作为参数传递的参数。另一方面，下面是一个不纯函数的示例：

```javascript
// 不纯函数；
// 修改传递的参数 "total" 的值
function sub(total, less) { return total -= less; }
```

在 React 中，props 遵循了“纯”的理念。这意味着你可以传递它们，前提是你的 React 组件不会从内部更改它们的值。这正是让 props 只读的原因。遵循这个规则是好的。

props 衍生自 HTML 元素的属性。这有点奇怪，它们被称为 props。因为在 HTML 元素中，属性是像 `DISABLED` 或 `CHECKED` 这样的单关键字标记。

props 更好的名字应该是 attributes（属性）。因为它们更像 HTML 属性的 `name=value` 键对，而不是 props。不过，事实如此。

通过这种方式创建组件的另一个主要区别是通过 `this` 变量访问 `props.name` 属性。否则，它的行为与上一个示例中的函数组件完全相同。

### 原生 Babel 与 JavaScript Babel

在继续学习之前，我曾尝试在上一个章节中微妙地提到这一点。我不希望你在不知道 Babel 可能没有为真实生产环境妥善配置的情况下，就误导地看到它在工作。

最好的是将 Babel 作为一个独立的应用程序在后台运行，作为你开发环境的一部分。这通常随着 Node 的安装一起提供。只需从 Google 下载 Node 并一直点击“Next”按钮完成安装即可。

通过 `SCRIPT` 标签直接添加 Babel 是可行的，并且适用于测试。但由于 Babel 的 JavaScript 库运行速度较慢，建议安装可以在命令行运行的原生版本。JavaScript 版 Babel 处理此类内容的速度很慢，而且违背了 React 编程的初衷——React 的唯一目的之一就是优化应用的运行速度。

### NPM

命令行 Babel 应用与 Node.js 安装一起提供。所以如果你安装了 Node，就会自动拥有 babel 包。你只需要在命令行中使用 NPM 工具单独安装它们，NPM 也是 Node 默认带的。

在学习 React.js 时，直接通过 `SCRIPT` 标签添加 Babel 是完全正常的。只是当你的应用上线时，它对生产环境来说不够快。在任何情况下，Babel 所做的只是将你的 EcmaScript 6 和 JSX 代码“转换”回 EcmaScript 5，这样就可以在任何尚未完全支持 ES6 的浏览器中运行它。（截至本文写作时，没有一个支持。）

### 转换源代码

你可能在论坛、Twitter 和 Reddit 上听过程序员使用“转换”（transpiling）一词，但可能还没有完全理解其背后的概念。

通常，转换是将一种语言的代码编译成另一种语言的源代码。这仅仅是语言之间的编译。然而，当涉及到 JavaScript 时，我们是在 EcmaScript 的两个不同规范（5 和 6）之间进行转换。

这使我们能够能够用 EcmaScript 6 写代码，并将其转换为 EcmaScript 5，以便现代浏览器能够运行你的代码。在本文写作时，大多数浏览器都不支持 ES6，甚至是 Chrome。

最终，当所有浏览器都支持 ES6 时，就可以安全地停止使用 Babel 进行 EcmaScript 规范之间的转换了。你只需在标准的 JavaScript 文件中编写代码，它就能直接运行。

但在那之前，我们不妨利用这个机会学习一种源代码工具。新标准会不断出现，而转换的艺术可能在短期内不会消失。

在上一个章节中，我想向你介绍超越组件本身的 React 编程基本原理。在这里，我在讨论组件和 props 的语境下简要提到了它们。

随着学习的深入，我们将继续深入研究响应式编程原理。这一次，由于已经对这些原理有了初步了解，这将帮助我们向编写实用的 React 应用迈进。

## 节课 - 嵌套组件

React.js 中的嵌套组件可以帮助你创建更复杂的视图元素结构。我之前提到过 React 组件的创建。这里作为一个提醒，这里是创建一个组件的方法。

```javascript
var Component = React.createClass({
  render : function() {
    return (<Something></Something>);
  }
});
```

这只是一个返回一组 HTML 标签的基础级组件。

我知道，你可能还在习惯返回这种没有加引号但看起来像 HTML 标签的内容，但到这时它应该开始看起来更熟悉了 :)

正如你所想象的那样，这就是你在 React 中经常工作的这类代码结构。

大多数事情都源于此。如果你用过 jQuery，这种组件结构可以与 jQuery 的对象选择器语法相比：

```javascript
$("class").on("click",function(){ /* 执行某些操作 */ });
```

我们有一个在事件执行后返回的回调函数。在 React 中，我们返回一个 HTML 元素，该元素通常会被放置在前端的应用结构中。

对于 React 组件来说，它只是一个包含 `render` 函数的 JavaScript 对象，并有一个返回 JSX 代码的 `return` 语句。这正是将 `<Something>` 标签转换为浏览器可以理解的 EcmaScript 5 代码。

`render` 函数和 `return` 语句中的内容取决于你应用程序的用途。在这个示例中，为了起见，我们将它们称为 Parent（父）和 Child（子）。

### 带有单个子元素的父

在这个示例中，为了起见，我们将它们称为 Parent 和 Child。使用这种模式，你可以实现父子关系。首先，让我们创建 Child：

```javascript
var Child = React.createClass({
  render: function() {
    return <div>{this.props.text}</div>;
  }
});
```

无论你传递到 Child（位于 Parent 内部）的内容是什么，都可以通过父容器自动访问。因此，props 真正建立了两者之间的关系。

React 是一个相对新的库。然而，如果你计划在响应式应用中使用动态的父子结构，它确实使用了一个你必须学会使用的的重要 JavaScript 函数。

这个标准的 JavaScript 函数就是 `map` 方法，它原生存在于所有数组（Array）对象上。如果你以前处理过数组，你可能至少听过这个函数。它所做的是创建一个新数组，对每个项调用回调函数，并将回调函数对每个项所应用的修改结果填充到新数组中。

简而言之，`Array.map` 接收所有项并对它们应用自定义操作。然后，它将修改后的新数据集作为新数组返回。这在编写 React 父子组件方面如何帮助我们呢？可以通过提供以下示例来演示这一点，我们将在单个 Parent 中使用多个 Children。

### 带有多个子元素的父

在这个示例中，我会保持 Child 组件完全不变，以便保持简单。注意新更新的 Parent 组件中数组 `map` 函数的新用法：



# React 组件与事件处理

```javascript
var Parent = React.createClass({
  /* 为多子数组设置默认值 */
  getChildrenState: function() {
    return { childrenData: [
      { childText: "Click me 1", childNumber: 1 },
      { childText: "Click me 2", childNumber: 2 }
    ] };
  },
  render : function() {
    return (
      var children = this.state.childrenData.map(function (data, index) {
        return <Child
          onClick={this.handleChildClick.bind(null, data)}
          text={data.childText} />
      })
      .bind(this);
      return <div>{children}</div>;
    );
  },
  handleChildClick: function (data, event) {
    // 访问目标：
    var target = event.target;
  }
});
```

# 75

```javascript
handleChildClick: (event) => {
  // 在此方法中，你可以通过 this.state 属性访问
  // 传递给子元素的 props
  var next = this.state.child;
  // 访问子元素的目标元素：
  var target = event.target;
};
```

现在，我特意创建了这些通用示例来向你展示子元素与父元素的关联，因为这并不是简单地将 HTML 元素相互嵌套那么简单。在 React 中，这种链接是通过程序化建立的，如上面的示例所示。

在现实世界的场景中，你将构建代表应用程序中实际元素的组件，例如警报框、朋友列表、消息、评论和按钮。但这里展示的这些示例是响应式编程的基础构建块。

我知道学习所有这些内容可能看起来麻烦，但一旦你编写了几个这样的组件，你就会发现 React 的多功能性，因为它就像是将自定义软件嵌入到你的日常 HTML 元素中。

React 还让我们对数据流拥有完全控制权，并利用虚拟 DOM，它在更新应用程序中需要更新的区域速度极快。

我希望你喜欢这个教程，并证明它是很有见地的。我在我的新书《React Book》中深入讨论了这些内容，这本书即将出版。

## 第3节 - 处理组件事件

到目前为止，我们只查看了 React 程序的节点组合。我们创建了组件并查看了它们的内部结构。

在本节中，我们将深入研究 React 组件的结构和功能。除了 `render` 之外，我们将探索三个新方法，每个方法在组件生命周期内的不同时间执行。这赋予了我们对应用程序更大的创作控制力。

始终记住，React 组件具有状态（`state`）。组件的全部目的是与该组件对象所代表的自定义状态绑定。状态是一个包含数据的对象。但组件还拥有辅助函数，使我们更容易地控制这些状态在给定语文中如何工作。

在本节中，我们将查看这些方法中的一些。

### 方法 1 - getInitialState

每个组件都负责渲染自己的状态，但 `getInitialState` 方法总会在我们的 `render` 函数之前被调用。它的功能类似于对象构造函数。

在这里我们设置了默认值。

```javascript
var Example = React.createClass({
  getInitialState : function() {
    return { state: 0 };
  }
});
```

你经常会在各个 React 组件中看到 `getInitialState`。它重置了与组件绑定的默认对象。在这里，你可以从数据库读取值，或者在屏幕上渲染此组件之前将状态重置为默认值。

你可以将此方法与 EcmaScript 6 默认构造方法交叉使用：

```javascript
class Example extends React.Component {
  constructor(function) {
    this.state = 0;
  }
}
```

这里唯一的显著区别是我们正在使用 `this` 关键字将状态附加到主对象上。还要注意 `extends` 关键字的使用，它只在 EcmaScript 6 中可用。

要在组件渲染在屏幕上时访问状态，我们必须使用 `componentDidMount` 方法：

### 方法 2 - componentDidMount

`componentDidMount` 方法在组件渲染时由 React 自动调用。通过将其添加到自定义的 React 组件中，你是在对其进行重载（overloading）。

重载意味着将你的功能添加到已存在的方法中，该方法是你扩展自定义组件时所属的默认 React 组件对象的一部分。这就是使用 `extends` 关键字的全部目的。我们正在扩展库已经提供的 React 组件对象的默认功能。

当我第一次听到在我的 React 组件中使用“挂载（mounting）”函数时，我不理解它的意思。我们难道不是简单地为我们的主要 React 组件附加一堆辅助方法吗？

我们在书的早期部分已经提到过挂载了。如果你仍然需要复习这个过程，我建议确保你已经看过了之前讨论过的 Gem 6 - 组件挂载。

`componentDidMount` 是负责在组件挂载后设置状态的方法。

```javascript
var Example = React.createClass({
  componentDidMount: function() {
    this.state = 1;
  }
});
```

它简单意味着虚拟 DOM 已经与一个 DOM 节点关联，该节点将在屏幕上实际更新。此方法在执行组件的 `render` 命令后总是被调用。它们是同义词，可能交叉使用。它确保并告诉我们元素实际上已经存在于虚拟 DOM 中。`render` 方法已经对它调用过了。

### 方法 3 - componentWillUnmount

最后，`componentWillUnmount` 在组件从页面移除并即将被销毁之前被调用。在下一页中，我们将查看示例源码。

```javascript
var Example = React.createClass({
  componentWillUnmount : function() {
    this.state = null;
  }
});
```

注意，我们正在将状态重置为 `null`。组件被销毁了，我们不再需要它的数据。这是我们清理组件使用的内存（如果有的话）的地方，例如取消初始化定时器。

## 用 React 编写的完整应用程序示例

我们已经涵盖了足够编写完整 React 应用程序的原则。我故意尝试让书中的所有示例都保持简单。复杂性通常来自编程中的创意，如果我直接把一个大程序丢进这本书里，可能会让你产生挫败感而不是动力。

在这里，我将构建一个简单的搜索应用，它在数组中查找结果。如果输入的字符匹配列表上的任何项，它们将被过滤出来，所有其他条目将被丢弃。这个应用就像 Google 搜索自动完成功能，当你向查询框输入时项目会掉落。

下面我列出完整的源代码。在这里我没有列出应用程序的样式表（CSS）部分。这可以单独处理。我们想要专注于 React 的实现。

### 创建搜索列表

让我们使用对象字面量格式创建搜索列表：

```javascript
// 首先，定义可搜索的动物列表
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

### 编写 React 应用程序

到为止，我们的源代码示例都相对简单。我将尝试将这个复杂的内容挤在一页内且不换行。翻到下一页查看完整源代码。在这个应用程序示例中，我们简单地将所有数据存储在数组中。将此代码放入你应用程序的主 `*.js` 文件中并运行它。如果你的 React 开发环境配置正确且 React js 文件包含在你的项目中，那么每当你开始在搜索框中输入时，它都会显示一个基础的下拉菜单。

```javascript
// 让我们创建一个搜索组件
var SearchComponent = React.removeClass({
  // 将输入元素重置为空格
  getInitialState : function() {
    return { searchString : '' };
  },
  handleChange : function(e) {
    // 注释掉以下行将导致
    // 文本框不改变值，因为在 React 中，
    // 输入框无法独立于赋值给它的值进行改变。在这种情况下，
    // 是 this.state.searchString;
    this.setState({ searchString : e.target.value });
  },
  // 渲染此组件
  render : function() {
    var libraries = this.props.items.toLowerCase();
    if (this.state.searchString.length > 0) {
      // 我们正在搜索。过滤结果。
      libraries = libraries.filter(function(l) {
        return l.name.toLowerCase().match(searchString);
      });
    }
    // 以 JSX 语句返回此组件
    return (<div>
      <input type="text"
        value={this.state.searchString} onChange=
        {this.handleChange} placeholder="在此输入" />
      <ul
        { libraries.map(function(l) {
          return ...})}
      </ul>
    </div>);
  }
});
// 在页面上渲染 SearchComponent 组件
ReactDOM.render(
  <SearchComponent items={ libraries } />,
  document.getElementById('container')
);
```

看起来有点复杂。但如果你删掉注释，考虑到它实现的功能，这个应用程序如此简短真是非常令人惊讶。

如你所见，取决于你设计的应用程序类型（在本例中，应用程序非常简单），你根据组件所代表的元素的性质，可能使用或不使用任何挂载或更新方法。

我希望这能为你提供足够的素材来开始编写自己的 React 应用程序。

## React Applications

这就是全部。看起来我们已经涵盖了响应式应用的**基本结构、常见功能**以及**实际实现**。我们甚至创建了一个完成实际任务的完整 React 应用程序。

你接下来的方向取决于你对继续探索 React 库以及通用的 JavaScript 有多深。

我希望这些示例以某种方式增加了你对 React 的了解，并激发足够的好奇心来继续冒险。

## 你应该学习 EcmaScript 6 吗？

就像 JSX 一，在 React 中编程假设了解许多不同的事情。其中之一就是 EcmaScript 6 规范。

这很重要，因为理想情况下在学习制作 React 应用程序的过程中，你想从旧的 ES5 语法过渡到 ES6 —— 这个标准在大约一到两年内将由所有现代浏览器正常支持。

这些浏览器包括 Chrome、Firefox 和 Safari。等这本书出版时，你应该已经可以在任何浏览器中编写 EcmaScript 6 代码，而无需使用额外工具对代码进行编译。至少我是希望的。当我开始写作时，还没有浏览器提供完全支持。

为了帮助这种过渡，我将书的剩余部分用于探索 EcmaScript 6 的新功能。我不会介绍每一个函数或语法变化。

书的其余部分将仅处理应用于 EcmaScript 6 规范的 JavaScript 语言的一些重要更改。

### EcmaScript 6 - 你需要知道的事

当 React 被创建时，正处于 ES5 规范的焦点中心。在 2015 年甚至整个 2016 年，它仍然是新奇颖的。

然而，到 2017 年，它开始逐渐适应 ES6 语法。这就是为什么在学习 React 时，讨论应用于这一新标准的重要更改非常重要。

当你学习 React 时，你学到的远不止是 React。它在 ES5 中运行良好，但那种语法正在变得过时。这正是许多程序员感到困惑的地方，因为同一个库在你在互联网和书籍上看到的不同示例中看起来可能是不一样的。

如果你不认识 React，可能可能对 EcmaScript 6 并不了解。我知道这是一个危险的假设，但我认为通过你在这一章中学到的内容是可以合理的。

ES5 真的没有问题。但它在短期内不会消失。我认为在行业仍在从一个规范过渡到另一个规范的时期编写教育类书籍时，偶尔在两者之间切换是重要的。

但我们已经到了书的这里，现在我们将调查 EcmaScript 6 规范中对 JavaScript 的主要差异和新增。在书的最后，我还会为这里讨论的许多主题提供备忘表。

### var 和 let 关键字

在 ES6 中，人们通常认为不再使用 `var` 关键字，而是使用 `let` 关键字。对此有其原因，下文所述。

使用 `let` 关键字没有提升。如果你熟悉 JavaScript 的提升机制，当你使用新的 `let` 关键字时会发现不同。

提升是 JavaScript 将所有变量定义移动到它们被定义的作用域上方。这个鲜为人知的过程是在幕后完成的。但它确实是真的。

```javascript
{
  // 返回："undefined"; 但仅是因为被提升了
  console.log( a);
  var a = 1;
}
```

以及 `let` 的示例：

```javascript
{
  // 返回：ReferenceError: a is not defined
  console.log( a);
  let a = 1;
}
```

```javascript
'use strict';
var a = 1; // Ok.
var a = 2; // Ok. a is now 2;

'use strict';
let a = 1; // Ok.
let a = 2; // Error: identifier a is already declared.
```

`let` 关键字也可以用于避免闭包问题。它会绑定一个新值，而不是保留对旧值的引用。这里有一个示例：

```javascript
'use strict';
for (let i = 1; i < 10; i++) {
  $.ajax({ url: 'script.php' },
    function(msg) {
      // 变量 i 在这里丢失了它的原始
      // 作用域，它不再与
      // for 循环中定义的 i 变量关联
      console.log(i);
    });
}
```

这段代码展示了一个常见的 JavaScript 问题，该问题在 for 循环中使用 `var` 关键字并结合 ajax 调用时非常容易发生。

由于 `i` 似乎在 ajax 的回调函数内部被重新定义，因此它不再与 *for-loop* 中定义的同一个 `i` 变量关联。

这个经典问题通常通过将 `i` 作为参数传递给函数来避免，但这会无谓地创建变量的新实例。

然而，当使用 `let` 定义相同的循环时，情况就不如此了。它有效地解决了这个常见问题。这里是相同的示例，只是这次使用了 `let`。

```javascript
"use strict";
for (var i = 0; i < 10; i++) {
  $.ajax({ url: "script.php" },
    function( msg ) {
      // 这里 i 是最初在
      // for loop 中定义的那个
      console.log(i);
    });
}
```

这无疑节省了许多与循环和回调函数相关的烦恼。

此外，`let` 关键字允许我们将变量的值保持在它定义的作用域内，正如这个孤立的示例所示：

```javascript
{
  let a = 1;
}
console.log( a ); // Reference error: a is undefined
```



换句话说，可以说使用`var`关键字定义的变量从它定义的那一刻起，在整个函数范围内都是已知的。

而`let`关键字仅在定义它的作用域块以及其中的所有其他作用域内是已知的，即使它是一个回调函数。这并没有解决任何重大的软件问题，但它确实帮助我们以更直观的方式完成工作，特别是在处理脚本程序结构中多个作用域交织的网络时。

### 新的`const`关键字

`const`与`let`完全一样。唯一的区别是，一旦你使用它定义了一个值，在程序的后续部分就不能再次重新定义它。这样做将产生一个错误：

```javascript
let a = 1;
a = 2;
// 这是没问题的，我们只是重新赋值了变量的值
const a = 1;
a = 2;
// ，这是一个常量，不能重新赋值！
```

这有什么用呢？常量变量在计算机程序中传统用于定义在整个应用程序运行期间不会改变的值。它们对于标志位值和不应该改变的应用配置设置非常有用。

哦，还有一件事……涉及到对象时，防止重新赋值的`const`关键字并**不会**让所赋值的对象变得不可变。与许多其他语言不同，将对象设为`const`会让它的属性同样不可变。

JavaScript并非如此。

### 解构赋值

EcmaScript 6为我们引入了解构赋值。这是新的JavaScript功能。之前对`let`关键字的解释为讨论接下来的主题奠定了基础。所以，让我们来看看它们是如何工作的：

```javascript
let { a, b, c, d } = object;
```

在这个示例中，创建了两个变量`a`和`b`。然后，从名为`obj`的对象取出属性`obj.a`和`obj.b`，并将它们分别赋值给这些变量。所以这等于执行以下操作：

```javascript
let a = obj.a;
let b = obj.b;
```

这种格式占用空间更多。解构赋值节省空间并为我们的代码提供了更好的可读性。但它们应该很难习惯。

### For-of循环

这是EcmaScript 6中一种完全新的循环。让我们来看看它是如何工作的：

```javascript
for (let [key, value] of map) { ... }
```

这个强大的`for`循环将遍历`map`中存储的值。遗憾的是（像很多事情一样；JavaScript也如此），`for-of`循环不能适用于对象（以及它们的属性）。

这几乎是一个令人困惑的设计决策。那么，`for-of`循环作用于什么呢？

`for-of`循环专门设计用于与`Array`、`Map`和`Set`对象工作。

### Map对象

就像`Array`一样，ES6添加了一个新的类型，称为`Map`。`Maps`无非只是简单的键/值映射。它们非常像PHP中的关联数组。

`Maps`不应该随处使用。只有在你之前使用对象作为集合的地方才使用它们。这正是它们的用途。在你的JavaScript程序设计中，使用对象仍应是主要的。

`Maps`有一个`.size`属性来确定其大小。与对象不同，你不需要手动计算对象的大小。当你有通过键/值关联的数据集时，将它们配合`for-of`循环使用！

### 箭头函数

EcmaScript 6最受青睐的功能之一是箭头函数。你应该尽早开始使用它们。

箭头函数只是用更紧凑的语法编写的JavaScript函数，与使用`function`关键字创建的普通函数略有不同。

这是箭头函数的基本格式，初看起来有点奇怪：

```javascript
name = (params) => returned expression
```

例如，你可以使用箭头函数编写这样的代码：

```javascript
x = (a, b) => {
  console.log("这是箭头函数 x " +
    "带有参数 = " + 
    a + " 和 " + 
    b);
};
```

但这仅仅是一个函数定义。它可以像普通函数一样如下所示执行：

```javascript
x(5, 7);
```

与普通JavaScript函数相比，一个激进的区别在于箭头函数处理`this`关键字的方式。

它从根本上解决了与`let`关键字解决普通作用域问题时相同（或类似）的问题。我们需要在这里进行稍微深入一点的讨论。

```javascript
/* A significantly simplified Sprite object in JavaScript */
var Sprite = function() {
  this.angle = 5;
  this.draw = function() {
    // Display sprite's angle
    console.log(this.angle)
  }
}
// Instantiate ship
var ship = new Sprite();

// draw the ship with this.angle rotation angle
ship.draw();
```

注意`draw`成员函数。在这个简单的示例中，我们输出了精灵当前的旋转角度。在现实世界的场景中，代码实际上会更复杂。但这仅仅是一个演示JavaScript中**箭头函数**（arrow functions）的示例。

我知道JavaScript函数的内部机制一直让程序员们感到困惑。那种想要“实验”事物运行原理、并凭感觉和黑客技巧来行的想法是非常诱惑力的。

在上面的示例中，`this`关键字在`Sprite`自身的作用域和其`draw`函数的作用域内是相同的。

我们在`Sprite`的作用域内将`angle`初始化为5。然后通过在`Sprite`的`this.draw`函数内部引用它，我们简单地获取了它的值。听起来很容易！而且运行符合预期。

但让我们不要忘记JavaScript对象中的**匿名**事件函数（也称为**回调**函数）以及它们如何与**作用域**（scope）共同工作。

我们现在看一下吗？我是在上一个示例中看到的代码基础上进行的。所以我在这里重复一遍它。

# 95

但是……有一个新的添加。我添加了`setTimeout`函数，它接收一个匿名函数并在`Sprite`对象实例化1秒（1000毫秒）后执行它。

注意，每当执行`setTimeout`时（大约每隔秒重复一次），我们使用`this.angle`属性到开发者控制台进行调试。

```javascript
/* A significantly simplified Sprite object in JavaScript */
var Sprite = function() {
  this.angle = 5;
  this.draw = function() {
    // Display sprite's angle
    console.log(this.angle);
  };

  // New! 以下代码将作为
  // 对象构造过程的一部分执行:
  var timer = setTimeout(function() {
    // 从这里显示精灵的角度
    console.log(this.angle);
  }, 1000);
};
// 使用 new 关键字实例化 ship 对象
var ship = new Sprite();
// 使用 this.angle 旋转角度绘制 ship
ship.draw();
```

我暂时移除了`ship.draw();`。这样，当实例化`Sprite`对象时，只有`Sprite`对象构造器区域的代码会被执行，这是通过使用`new`关键字实现的。

事件处理器内部的`this`关键字会自动赋值给发生事件的对象。让我们运行这个程序，看看发生了什么，与我们之前的示例相比。

`console.log`消息现在将返回：

# 96

# Undefined

那是因为匿名函数`function() { ... }`内的`this.angle`不再指向来自`Sprite`对象的`this`对象。

而且匿名函数上没有名为`angle`的属性——那个是作为参数传递给`setTimeout`函数的。

```javascript
/* A significantly simplified Sprite object in JavaScript */
var Sprite = function() {
  this.angle = 5;

  this.draw = function() {
    // Display sprite's angle
    console.log(this.angle);
  }

// New! 一种解决方案是在这个作用域内
// 创建一个 "that" 变量：

var that = this;

// 以下代码将作为
// 对象构造过程的一部分执行:
var timer = setTimeout(function() {
    // 从这里显示精灵的角度
    console.log(that.angle);
}, 1000);
}
var ship = new Sprite(); // 实例化 ship
// 使用 this.angle 旋转角度绘制 ship
// ship.draw();
```

在这里我在添加新代码的地方添加了新注释。源代码的其他部分几乎完全相同。通过注意这些变化，你将发现一些有趣的东西。

在这个示例中，我所做的只是将该对象赋值给主`Sprite`对象作用域内新创建的`that`变量。在`timer`变量设置和定义之前。所以实际上，我们现在在`Sprite`内部有了像`this.that`这样的东西。

我还将其更改为：

```javascript
setTimeout(function() { ... });
```

这次我们运行我们的代码，看看现在发生了什么：

# 97

`that`的值是5。这是当我们把`this`对象绑定到名为`that`的变量时发生的。

我确定你以前用过我在上面示例中描述的技巧。如果没有，那么好吧，我很兴你现在知道了它。大多数程序员都是通过直觉发现它的。

学习JavaScript中函数对象与这些函数内部匿名事件之间作用域规则的差异需要时间。

而且在实际实现方面，我们还没有真正探索过箭头函数（Arrow Functions）。你看，ES6是构建在ES5特性集之上的。

我使用这个`Sprite`对象仅仅是为了为ES6出现之前的JavaScript基础作用域原则奠定基础。

最后……在我们脸上带着大微笑（或皱眉）经过所有这些解释后，这个讨论把我们带了最后的大问题！

# 98

## 什么是JavaScript中的箭头函数？

它们是什么？为什么它们不同？JavaScript中箭头函数和匿名函数之间的区别是什么？仅仅是语法吗？它不仅于此。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

虽然语法略有不同（更简洁），箭头函数也改变了其作用域内对象的实际功能。

.

从那一刻起，新匿名事件函数内部的`this`关键字开始正确引用原始`Sprite`对象的`this`，而无需我们编写任何额外的绑定代码。

因此，我认为关于箭头函数的讨论到此结束。我真的希望这能让你了解清箭头函数与普通构造函数之间的区别。

根据SitePoint的这篇文章，箭头函数是ES6 Web开发者最喜的功能。我深表赞同。

### 立即调用箭头函数 (IIAF)

如果你熟悉jQuery或JavaScript插件开发，你可能已经间接接触过IIAF，并且已经见过立即调用函数表达式 (IIFE) 这种通常晦涩的语法，它看起来像这样：

```
( function () { ... } )();
```

在这里，我们在定义函数的同时就执行了该函数。

你会发现这种语法经常出现在HTML页面的底部，闭合的`body`标签上方。这种技术用于等待HTML元素加载完成后再开始执行JavaScript。

同样地，可以使用箭头函数来实现等的效果。

```
( () => { ... } )()();
```

这种语法被称为立即调用箭头函数。外围的括号使得函数在程序执行流的该位置被执行。

### 反引号（`` ` ``）模板字符串

反引号只是这种特殊引号字符的另一个名称，也被称为重音（grave accent）。

现在像`${ expression }`这样的语句可以使用模板字符串进行插值。它仅仅是一个由键盘上"1"键左侧的第三组引号（在单引号和双引号之后）围成的字符串。

反引号字符串的优点之一是它们可以跨行。这是JavaScript之前的一个非常需要的功能。

这类字符串也被称为模板字面量（template literals）。下面展示了几个示例：

```
string text`;
`string text on line one
Can continues here without semicolons`;
another text with ${expression} within it`;
`string text`;

// 就像普通引号一样，反引号也可以
// 使用反斜杠转义，见下文：
// 以下语句将返回 true
`\name`
```

你也可以在反引号中使用普通的单引号（' '）和双引号（" "）。

### 新的数组方法

以下是ES6中`Array`对象最重要的补充。

让我们按如下定义常用的`Array`对象：

```
let arr = new Array();
```

在ES6中，我们有了这些新的数组操作方法：

### find

```
arr.find(callback{}, thisArg);
```

返回第一个项的值，该项在传递给回调时产生一个真值（truthy value）。

### findIndex

```
arr.findIndex(callback{}, thisArg);
```



`findIndex`方法与`find`完全相同。

区别在于它返回产生真值的第一个项的索引，而不是数值。

根据 MDN，在 JavaScript 中，真值（truthy value）是指在布尔上下文中求值时被视为 `true` 的值。

所有值都是真值（truthy），除非它们被定义为假值（falsy）（即：`false`、`0`、`''`、`null`、`undefined` 和 `NaN` 之外）。这就是 JavaScript 在布尔上下文中使用类型转换的方式。虽然我不喜欢这么说，但它并不总是遵循清晰的规则。

### fill

`fill`方法初始化或“填充”数组每个索引处的所有元素。它可以通过可选参数`start`和`end`仅初始化或设置数组的一个区域：

```
arr.fill(value[, start = 0, end = this.length]);
```

默认情况下，`start`为 0，`end`为数组的长度。

### copyWithin

这个新的数组方法将数组内部的一个项序列复制到自身，从`start`指向的位置开始，并从`target`指向的索引开始：

```
arr.copyWithin(target, start[, end = this.length] );
```

这是一个实用的示例：

```
var arr1 = [1,1,1, 2,2,2, 3,3,3];
// 复制前三个索引并粘贴到最后三个位置
arr1.copyWithin(6, 0, 3);
alert(arr1); // 1,1,1, 2,2,2, 1,1,1
```

这段代码显然复制了 "1,1,1" 序列，从数组索引 0 处开始将其复制到最后。

### 内置类

ES6 添加了几个新的内置类：

- `Map`：键值对的集合。

- `Set`：唯一值的集合。

- `Symbol`：一种唯一且不可变的原始值。

- `Promise`：代表异步操作的最终完成（或失败）。

### 特殊属性

- `children`：由`React.createElement`成员函数自动添加到此`props`中。

- `className`：对应 HTML 的`class`属性。

- `htmlFor`：对应 HTML 的`for`属性。

- `key`：一个唯一的 React 标识符

- `ref`：接收一个回调函数，该函数会在组件挂载（mount）时带有组件实例或 DOM 节点调用，在卸载（unmount）以及传入函数发生变化时带有`null`。

- `style`：接收一个样式对象而不是字符串。

我们使用`className`和`htmlFor`是因为`class`和`name`是 HTML 的保留关键字，不能直接作为 React 元素的一部分。

同样地，我们不使用 CSS 样式来尝试格式化，React 版本的`style`属性期望一个 JavaScript 对象，其属性模仿了 CSS 属性名。

带有连划线的 CSS 属性（如`font-family`）只需转换为驼峰命名的`fontFamily`等。

### 属性类型 (PROPETYPES)

在`React.PropTypes`下提供以下属性`types`：

| any | bool | element | func | number | object | string |

| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

### 类组件 (CLASS COMPONENTS)

React`Classes`（类）与 React`Elements`（元素）不同。

```javascript
var MyComponent = React.createClass({
  displayName : 'MyComponent',

  /* ... 配置和生命周期方法 ... */

  render : function() {
    return React.createElement(/* ... */)
  },
});
```

### 配置（用于类组件）

- `propTypes`：一个将属性名映射到`types`的`对象`

- `getDefaultProps`：返回`object`的`函数`

- `getInitialState`：返回`object`的`函数`

### 生命周期周期方法（用于类组件）

- `componentWillMount() {}`

- `componentDidMount() {}`

- `componentWillReceiveProps(nextProps) {}`

- `shouldComponentUpdate(nextProps, nextState) {}`

- `componentWillUpdate(nextProps, nextState) {}`

- `componentDidUpdate(prevProps, prevState) {}`

- `componentWillUnmount() {}`

### 组件实例 (COMPONENT INSTANCES)

1. 在类组件内部可以通过`this`访问。

2. 无状态函数组件没有组件实例。

3. 作为传递给`ref`回调函数的对象。

4. 一个组件实例可以跨越多个等效的`ReactElements`存在。

### 属性 (Properties)

- `props`：包含所有传递给`React.createElement`的`props`

- `state`：包含由`setState`和`getInitialState`设置的状态（state）

### 方法 (Methods)

1. `setState(changes)`将给定的更改应用到`this.state`并重新渲染组件。

2. `forceUpdate()`立即将组件重新渲染到 DOM。

### BABEL：组件即类

```javascript
export class MyComponent extends Component {
  componentWillMount() {
  }
  render(s) {
    return <div>Hello React</div>
  }
}
```

### 静态属性 (Static Properties)

```javascript
export class MyComponent extends Component {
  static propTypes = {
  }
  static defaultProps = {
  }
}
```

### 初始状态 (Initial State)

```javascript
export class MyComponent extends Component {
  state = {
    disabled: this.props.disabled
  }
}
```

### 构造函数 (Constructors)

替换`componentWillMount`:

```javascript
export class MyComponent extends Component {
  state = { disabled: this.props.disabled }
}
```

### BABEL：绑定方法 (Bound Methods)

使用箭头函数创建绑定回调方法：

```javascript
export class MyComponent extends Component {
  onMouseEnter = event => {
    this.setState({ hovering: true })
  }
}
```

### 导入 (Import)

JSX 假设 React 对象是可用的。确保按照示例所示导入：

```javascript
import React, { Component, PropTypes } from 'react'
```

### 解构 (Destructuring)

在配合无状态函数组件时非常有用。

```javascript
export const Commas = ({ items, ...otherProps }) =>
  <div {...otherProps}>{items.join(', ')}</div>
```

### 模板字符串 (Template Literals)

用于创建动态类名。

```javascript
this.setState({
  [`${inputValueName}`]: e.target.value,
});
```

### BABEL：类装饰器 (Class Decorators)

用于替代 mixins（混入）：

```javascript
@something(options)
class MyComponent extends Component {}

// 变为
let MyComponent = something(options)(function() {
  class MyComponent extends Component {}
});
```

`<tags>` 变为`React.createElement`。

使用`<lowercase />`标签表示 DOM 元素：

```jsx
<div></div>
```

`React.createElement('div')`

使用`<Capitalized />`标签表示自定义元素：

```jsx
<MyComponent />
```

`React.createElement(MyComponent)`

注意，大写字母头的标签不需要加引号。
