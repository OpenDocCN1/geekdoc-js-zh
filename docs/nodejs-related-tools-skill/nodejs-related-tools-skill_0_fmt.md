
# Node.js 相关工具与技能

## 关于 SitePoint

`SitePoint` 专门为 Web 专业人士出版有趣、实用且易于理解的内容。访问 `http://www.sitepoint.com/` 获取我们的博客、书籍、时通讯、文章和社区论坛。你将在那里找到关于 JavaScript、PHP、设计等大量信息。

## 引言

尽管已经有很多尝试让 JavaScript 作为服务器端语言，但 Node.js（通常直接称为 Node）是第一个获得关注的环境。它现在被 Netflix、Uber 和 Paypal 等公司用于支持其 Web 应用程序。`Node` 允许极快的性能；得益于它的事件循环，网络连接和数据库 I/O 等常见任务执行速度确实非常快。

## 亮点

从初学者的角度来看，`Node` 的明显优势之一是它使用了 JavaScript，这是一种许多开发者都熟悉的通用的语言。如果你能为客户端编写 JavaScript，那么用 `Node` 编写服务端应用程序对你来说也并不难。

在书中，我们将介绍一些相关的工具和技能，它们将让你成为一名更高效的 `Node` 开发者。

## 谁应该读这本书？

本书适用于任何想要学习使用 `Node.js` 进行服务端开发的人。我们假设读者熟悉 `JavaScript`，但并不假设你有任何先前的后端开发经验。

## 使用的规范

### 代码示例

书中的代码使用等宽字体显示，如下所示：

```html
<h1>一个完美的夏日</h1>
<p>那是一个适合在公园里散步的美好日子。鸟儿在歌唱，孩子们都回上学了。</p>
```

当需要现有代码作为上下文，而不是重复所有代码时，将显示 `⋮`：

```javascript
function animate() {
  ⋮
  new_variable = "Hello";
}
```

某些行代码应该写在一行内输入，但由于页面限制，我们对它们进行了换行。`➥` 表示仅出于格式目的而存在的换行，应该被忽略：

```javascript
URL.open("http://www.sitepoint.com/responsiveweb➥designrealusertesting/?responsive1");
```

你会注意到，我们在整书中使用了某些布局样式来表示不同类型的信息。请关注以下项目。

### 提示、注释与警告

- **Hey, You!**：提示提供了有用的小建议。

- **Ahem, Excuse Me ...**：注释是与当前主题相关但并非至关重要的旁注。你可以将它们看作额外的信息片段。

- **Make Sure You Always ...**：……始终注意这些重要点。

- **Watch Out!**：警告强调了在过程中可能让你出错的陷阱。

# 第 1 章：使用 Mocha 和 Chai 对你的 JavaScript 进行单元测试

## 亮点

你是否曾经对代码做了一些更改，后来发现它导致了其他地方的崩溃？

我相信我们大多数人都有过这种情况。这几乎是不可避免的，尤其是当你有大量的代码时。一个东西依赖于另一个，然后更改它就会导致另一个东西坏掉。

但如果这种情况没有发生呢？如果你有一种方法知道东西是否由于某些更改而发生了故障，那将太棒了。你可以修改代码而不必担心弄坏任何东西，你的 Bug 会更少，调试时间也会更短。

这正是单元测试大放异彩的地方。它们会自动为你检测代码中的任何问题。做出更改，运行测试，如果任何部分崩溃，你将立即知道发生了什么、问题在哪里以及正确的行为应该是什么。这完全消除了任何猜测！

在本文中我将向你展示如何开始对 JavaScript 进行单元测试。本文所示的示例和技术同时适用于基于浏览器和 Node.js 代码。

## 什么是单元测试

单元测试的核心思想是测试函数在接收到特定输入时的行为。你带有特定的参数调用函数，并检查你是否得到了正确的结果。

```javascript
// 给出 1 和 10 作为输入...
var result = Math.max(1, 10);

// ...我们应该收到 10 作为输出
if(result !== 10) {
  throw new Error('Failed');
}
```

## 工具准备工作

对于本文，我们将使用 `Mocha`。它很容易上手，既可用于浏览器和 Node.js 测试，并且与其他测试工具良好协作。

安装 `Mocha` 最简单的方法是通过 `npm`（为此我们需要先安装 Node.js）。如果你不确定如何在系统中安装 `npm` 或 Node，请参阅我们的教程：npm 初学者指南 —— Node 包管理器。安装好 Node 后，在项目目录中打开终端或命令行。

如果你想在浏览器中测试代码，运行 `npm install mocha chai dev`。如果你想测试 Node.js 代码，除了上述操作再运行 `npm install mocha chai`。

这会安装 `mocha` 和 `chai` 包。`Mocha` 是允许我们运行测试的库，而 `Chai` 包含了我们用于验证测试结果的一些有用函数。

### 在 Node.js 上测试 vs 在浏览器中测试

后续示例旨在在浏览器中运行测试。如果你想测试 Node.js 应用程序，请按照以下步骤操作：

- 对于 Node，你不需要测试运行文件。

- 要包含 `Chai`，在文件顶部添加 `var chai = require('chai');`。

- 使用 `mocha` 命令运行测试，而不是打开浏览器。

### 设置目录结构

你应该将测试与主代码文件放在不同的目录中。这使得结构更加清晰，例如如果你将来想添加其他类型的测试（如集成测试或功能测试）。

JavaScript 代码最常用的做法是在项目的根目录下创建一个名为 `test/` 的目录。然后，将每个测试文件放置在 `test/someModuleTest.js` 之下。可选的是，你也可以在 `test/` 内部使用目录，但我建议保持简单 —— 如果需要，你以后随时更改。

### 设置测试运行器

为了在浏览器中运行测试，我们需要设置一个简单的 HTML 页面作为我们的测试运行器页面。该页面会加载 `Mocha`、测试库以及我们的实际测试文件。

要运行测试，我们只需在浏览器中打开该运行器即可。

如果你使用的是 Node.js，可以跳过此步。假设你遵循了推荐的目录结构，可以使用命令 `mocha` 运行 Node.js 单元测试。

下面我们将用于测试运行器的代码。我将把此文件保存为 `testrunner.html`。

```html
<!DOCTYPE html>
<html>
<head>
<title>Mocha Tests</title>
<link rel="stylesheet" href="node_modules/mocha/mocha.css">
</head>
<body>
<div id="mocha"></div>
<script src="node_modules/mocha/mocha.js"></script>
<script src="node_modules/chai/chai.js"></script>
<script>mocha.setup('bdd')</script>
<! 在此处加载你想测试的代码 >
<! 在此处加载你的测试文件 >
<script>
mocha.run()
</script>
</body>
</html>
```

测试运行器中重要的部分是：

- 我们加载了 `Mocha` 的 CSS 样式，为我们的测试结果提供良好的格式化。

- 我们创建了一个 ID 为 `mocha` 的 `div`。这是插入测试结果的地方。

- 我们加载了 `Mocha` 和 `Chai`。由于我们是通过 `npm` 安装它们的，它们位于 `node_modules` 文件夹的子目录下。

- 通过调用 `mocha.setup`，我们使 `Mocha` 的测试辅助可用。

- 然后，我们加载想要测试的代码和测试文件。目前这里还没有任何内容。

- 最后，我们调用 `mocha.run` 来运行测试。确保在加载源文件和测试文件之后*调用此方法。

### 基础测试构建块

现在我们可以运行测试了，让我们开始编写一些测试吧。

我们将首先创建一个新文件 `test/arrayTest.js`。像这样的单个测试文件被称为测试用例。我将其命名为 `arrayTest.js`，是因为在这个例子中，我们将测试一些基础数组功能。

每个测试用例文件都遵循相同的基本模式。首先，你有一个 `describe` 块：

```javascript
describe('Array', function() {
  // 额外的测试代码放在这里
})
```

`describe` 用于对单个测试分组。第一个参数应该指示我们正在测试什么 —— 在此情况下，由于我们要测试数组函数，所以我传入了字符串 `'Array'`。

其次，在 `describe` 内部，我们将有 `it` 块：

```javascript
describe('Array', function() {
  it('should start empty', function() {
    // 测试实现写在这里
  })
  // 我们可以在这里有更多的 its
})
```

`it` 用于创建实际的测试。`it` 的第一个参数应该提供对测试的人类可读描述。例如，我们可以将上面的内容读为“它应该从空开始”，这是对数组应该行为的良好描述。实现测试的代码随后写在传递给 `it` 的函数内部。

所有 `Mocha` 测试都是由这些相同的构建块构建的，并遵循这种相同的基本模式。

1. 首先，我们使用 `describe` 说明我们正在测试什么，例如`"describe how array should work"`。

2. 然后，我们使用多个 `it` 函数来创建单个测试，每个 `it` 应该解释一个特定的行为，例如我们上面数组用例中的 `"it should start empty"`。

### 编写测试代码

现在我们已经知道如何构造测试用例，让我们进入有趣的部分 —— 实现测试。

由于我们正在测试数组是否应该从空开始，我们需要创建一个数组，然后确保它是空的。这个测试的实现非常简单：

```javascript
var assert = chai.assert;

describe('Array', function() {
  it('should start empty', function() {
    var arr = []
    assert.equal(arr.length, 0)
  })
})
```

注意第一行，我们设置了 `assert` 变量。这只是为了让我们不需要在到处都重复输入 `chai.assert`。

在 `it` 函数中，我们创建一个数组并检查它的长度。虽然简单，但这是测试如何运作的一个良好示例。

- 首先，你有一个正在测试的东西 —— 这被称为被测系统或 `SUT`。

- 然后，如果需要，你对 `SUT` 执行某些操作。在这个测试中，我们什么都没做，因为我们正在检查数组是否是从空开始的。

- 测试中的最后一项应该是验证 —— 一个检查结果的*断言*（assertion*）。

在这里，我们正在使用 `assert.equal` 来做到这一点。大多数断言函数接收参数的顺序相同：首先是“实际”值，然后是“预期”值。

*实际*值是你的测试代码的结果，因此在此例中为 `arr.length`。*预期*值是结果*应该*是什么。由于数组应该从空开始，此测试中的预期值是 `0`。

`Chai` 还提供了两种不同的断言编写风格，但目前我们使用 `assert` 来保持简单。当你对编写测试变得更有经验时，你可能想改用 `expect` 断言，因为它们提供了更大的灵活性。

### 运行测试

为了运行此测试，我们需要将它添加到我们创建的运行器文件中。如果你使用的是 Node.js，可以跳过此步并使用命令 `mocha` 运行测试。

否则，要将此测试添加到运行器中，只需添加：

```html
<script src="test/arrayTest.js"></script>
```

### 测试结果

当你运行测试时，测试结果看起来会像这样（index-13_1.png-13_2.png）

注意，我们在 `describe` 和 `it` 函数中输入的内容会显示在输出中。注意，也可以嵌套 `describe` 块来创建进一步的分组。让我们看看失败的测试是什么样的：

```javascript
assert.equal(arr.length, 0)
```

将数字 `0` 替换为 `1`。这会导致测试失败，因为数组长度不再匹配预期值。再次运行测试，你会看到红色的失败测试，以及对错误的描述。测试的好处之一是它们能帮你更快发现 Bug，但这个错误在这方面并没有帮助。

大多数断言函数还可以接收一个可选的 `message` 参数。这是当断言失败时显示的消息。使用这个参数让错误消息更易理解是一个好主意。我们可以这样为断言添加消息：

```javascript
assert.equal(arr.length, 1, 'Array length was not 0')
```

如果你重新运行测试，自定义消息将取代默认消息。

### 整合在一起

到目前为止，我们看了一些相当简单的例子。让我们把所学的知识付诸实践，看看如何测试一段更贴真实的代码。

这里有一个向元素添加 CSS 类的函数。它应该放在新文件 `js/className.js` 中。

```javascript
function addClass(el, newClass) {
  if(el.className.indexOf(newClass) === 1) {
    el.className += newClass
  }
}
```

为了让它更有趣，我让它仅当该类不在元素的 `className` 属性中时添加新类 —— 毕竟谁想看到 `<div class="hello hello hello">` 呢？

在理想情况下，我们在编写代码之前会为这个函数编写测试。但测试驱动开发是一个复杂的主题，目前我们只想关注编写测试。

为了开始，让我们回顾一下单元测试的基本思想：我们给函数某些输入，然后验证函数的行为是否符合预期。那么，这个函数的输入和行为是什么？

给定一个元素和一个类名：

如果元素的 `className` 属性不包含该类名，则应该将其添加。

如果元素的 `className` 属性已经包含该类名，则不应该将其添加。

让我们这些情况转换为两个测试。在测试目录中，创建一个新文件 `classNameTest.js` 并添加以下内容：

```javascript
describe('addClass', function() {
  it('should add class to element');
  it('should not add a class which already exists');
})
```

我们对措辞进行了微调，使用了测试中常用的 "it should do X"（它应该执行 X）形式。这意味着它读起来更顺畅一些，但本质上与我们上面列出的可读性形式相同。从想法到测试通常并不比这困难得多。

但等一下，测试函数在哪里呢？嗯，当我们省略 `it` 的第二个参数时，Mocha 会在测试结果中将这些测试标记为 `pending`（待定）。这是一种设置多个测试的方便方法——就像是你打算编写内容的待办事项列表一样。

让我们继续实现第一个测试。

```javascript
describe('addClass', function() {
  it('should add class to element', function() {
    var element = { className: '' };
    addClass(element, 'testclass');
    assert.equal(element.className, 'testclass');
  });

  it('should not add a class which already exists');
})
```

在这个测试中，我们创建了一个 `element` 变量并将其作为参数传递给 `addClass` 函数，同时带有字符串 `testclass`（要添加的新类名）。然后，我们使用断言检查该类是否包含在值中。

再次，我们从最初的想法——给定一个元素和一个类名，它应该被添加到类列表中——并以相当直接的方式将其转换为代码。

尽管此函数设计为与 DOM 元素工作，但我们在这里使用了一个普通的 JS 对象。有时我们可以利用 JavaScript 的这种动态特性来简化测试。如果我们不这样做，就需要创建一个真实的元素，这会增加测试代码的复杂性。作为一个额外的好处，由于我们没有使用 DOM，如果如果我们愿意，也可以在 Node.js 中运行此测试。

### 在浏览器中运行测试

要在浏览器中运行测试，你需要将 `className.js` 和 `classNameTest.js` 添加到运行器中：

```html
<! 在此处加载你想要测试的代码 >
<script src="js/className.js"></script>
<! 在此处加载你的测试文件 >
<script src="test/classNameTest.js"></script>
```

你现在应该看到一个测试通过了，另一个测试显示为待定，如下面的 CodePen 所示。注意，代码与示例略有不同，以便代码在 CodePen 环境中正常运行。

实时代码！

查看 Pen Unit Testing with Mocha (1),

接下来，让我们实现第二个测试……

```javascript
it('should not add a class which already exists', function() {
  var element = { className: 'exists' };
  addClass(element, 'exists');
  var numClasses = element.className.split(' ').length;
  assert.equal(numClasses, 1);
})
```

经常运行测试是一个好习惯，所以让我们检查一下现在运行测试会发生什么。正如预期的，它们应该会通过。

这是另一个实现了第二个测试的 CodePen。

实时代码！

查看 Pen Unit Testing with Mocha (2),

等一下！我其实稍微耍了一下你们。这个函数还有第三种我们还没有考虑的行为。函数中还有一个 bug——一个相当严重的 bug。

它只是一个三行的函数，但你注意到了吗？

让我们为第三种行为再写一个测试，顺便暴露这个 bug。

```javascript
it('should append new class after existing one', function() {
  var element = { className: 'exists' };
  addClass(element, 'newclass');
  var classes = element.className.split(' ');
  assert.equal(classes[1], 'newclass');
})
```

这次测试失败了。你可以在下面的 CodePen 中看到它的运行情况。这里的问题很简单：元素中的 CSS 类名应该用空格隔开。然而，我们目前对 `addClass` 的实现并没有空格！

实时代码！

查看 Pen Unit Testing with Mocha (3)。

让我们修复函数并让测试通过。

```javascript
function addClass(el, newClass) {
  if(el.className.indexOf(newClass) !== 1) {
    return;
  }
  if(el.className !== '') {
    //确保类名用空格隔开
    newClass = ' ' + newClass;
  }
  el.className += newClass;
}
```

这是一个带有修复后的函数和通过测试的最后一个 CodePen。

实时代码！

查看 Pen Unit Testing with Mocha (4)。

### 在 Node 上运行测试

在 Node 中，事物只对同一个文件中的其他事物可见。由于 `className.js` 和 `classNameTest.js` 在不同的文件中，我们需要找到一种让它们相互可见的方法。实现此点的标准方法是使用 `module.exports`。如果你需要复习，可以在这里阅读相关内容：Understanding module.exports and exports in Node.js

代码基本上保持不变，但结构略有不同：

```javascript
// className.js
module.exports = {
  addClass: function(el, newClass) {
    if(el.className.indexOf(newClass) !== 1) {
      return;
    }
    if(el.className !== '') {
      //确保类名用空格隔开
      newClass = ' ' + newClass;
    }
    el.className += newClass;
  }
};
```

# 面向对象的 JavaScript

当开发者们努力让 JavaScript 的灵活性与浏览器文档对象模型（DOM）的复杂性相匹配时，现实世界中的实际 JavaScript 代码通常看起来像这样：

```javascript
var result;

function getText() {
  var someText = prompt("Give me something to capitalize");
  capWords(someText);
  alert(result.join(" "));
}

function capWords(input) {
  var counter;
  var inputArray = input.split(" ");
  var transformed = "";
  result = [];
  for (counter = 0; counter < inputArray.length; counter++) {
    transformed = [
      inputArray[counter].charAt(0).toUpperCase(),
      inputArray[counter].substring(1)
    ].join("");
    result.push(transformed);
  }
}

document.getElementById("main_button").onclick = getText
```

这段短小的代码片段发生了发生了事情。变量在全局作用域被定义。值在函数之间传递并修改。DOM 方法与原生 JavaScript 混合在一起。函数名没有很好的描述性，这部分程度上是因为整个东西依赖于一个可能存在也可能不存在的上下文。但如果你恰好在定义了 `<button id="main_button">` 的 HTML 文档浏览器中运行这段代码，你可能会被输入某些文本进行处理，然后看到一个弹窗，其中该文本中每个单词的首字母已大写。

这种命令式代码的设计是为了从上到下读取和执行的（忽略少量的变量提升）。但我们可以利用 JavaScript 的面向对象特性进行一些改进，以清理这些代码并使其更具可读性。

几年后，开发者们开始注意到在浏览器等共享环境中使用命令式编码的问题。来自一个 JavaScript 代码段的全局变量会覆盖另一个代码段设置的全局变量。代码调用的顺序会以不可预测的方式影响结果，特别是考虑到网络连接和渲染时间带来的延迟。

最终，出现了一些更好的实践来帮助封装 JavaScript 并使其更好地与 DOM 交互。上述代码的更新版本，按照面向对象的标准编写，可能如下：

```javascript
(function() {
  "use strict";

  var SomeText = function(text) {
    this.text = text;
  }

  SomeText.prototype.capify = function(str) {
    var firstLetter = str.charAt(0);
    var remainder = str.substring(1);
    return [firstLetter.toUpperCase(), remainder].join("");
  }

  SomeText.prototype.capifyWords = function() {
    var result = [];
    var textArray = this.text.split(" ");
    for (var counter = 0; counter < textArray.length; counter++) {
      result.push(this.capify(textArray[counter]));
    }
    return result.join(" ");
  }

  document.getElementById("main_button").addEventListener("click", function(e) {
    var something = prompt("Give me something to capitalize");
    var newText = new SomeText(something);
    alert(newText.capifyWords());
  });
}());
```

在这个面向对象的版本中，构造函数模拟了类来建模我们想要的对象。方法位于新对象的原型上以保持低内存占用。所有的代码都隔离在一个匿名的立即执行表达式中，这样它们就不会污染全局作用域。这里甚至有一个 `use strict` 指令来利用最新的 JavaScript 引擎，而且旧式的 `onclick` 方法被全新的 `addEventListener` 取代了，因为谁还会用 IE8 或更早的版本呢？这样的脚本可能会被插入到 HTML 文档 `<body>` 元素的结尾，以确保在处理之前所有 DOM 都已加载，这样它依赖的 `<button>` 就是可用的。

尽管经过了所有重构，但仍然存在许多导致我们陷入这种境地的命令式风格遗迹。构造函数中的方法依赖于作用域在父对象的变量。有一个循环结构用于遍历字符串数组中的所有成员。有一个没有任何用处的计数器变量。

除了通过 `for` 循环来增加进度外，这些方法产生了修改自身之外变量的副作用。

这一切使得代码变得脆弱、不易移植，并且更难在狭窄的上下文中测试这些方法。

### 函数式 JavaScript

面向对象的方法比我们开始的命令式方法更清晰、模块化，但让我们看看如何通过解决我们讨论过的缺点来改进它。如果我们能找到利用 JavaScript 将函数视为一等对象的方法，我们的代码将会变得更简洁、稳定且更容易复用。

```javascript
(function() {
  "use strict"
  var capify = function(str) {
    return [str.charAt(0).toUpperCase(), str.substring(1)].join("")
  }
  var processWords = function(fn, str) {
    return str.split(" ").map(fn).join(" ")
  }
  document.getElementById("main_button").addEventListener("click", function(e) {
    var something = prompt("给我一些需要大写的字符")
    alert(processWords(capify, something))
  })
}())
```

你注意到这个版本短了很多吗？我们只定义了两个函数：`capify` 和 `processWords`。这两个函数都是纯的，意味着它们不依赖调用它们的代码状态。它们不会产生修改自身之外变量的副作用。对于任何给定的参数集，函数有且只有一个结果。由于这些改进，新函数非常容易测试，并且可以从这段代码中剪切出来并在其他地方使用。

这里可能有一个你除非看过一些函数式代码否则不会认识的关键词。我们利用 `Array` 的新 `map` 方法将函数应用到分割字符串时产生的临时数组的每个元素上。`Map` 只是现代浏览器和服务器端 JavaScript 解释器实现 `ECMAscript 5` 标准时提供的少量便利方法之一。

# 任务运行器与构建流程

现代 Web 开发涉及：

- 支持从脚本中移除 `console` 和 `debugger` 语句。

- 将 ES6 编译为跨浏览器兼容的 ES5 代码。

- 代码检查和验证。

- CSS 和 JavaScript 文件的合并与压缩。

- 将文件部署到开发、测试和生产环境的服务器。

每当你做出更改时，都必须重复这些任务。你可能初衷良好，但即使是最严谨的开发者也会忘记压缩一两个图片。随着时间的推移，生产前的任务会变得越来越繁琐且耗时；你将对那些不可避免的内容和模板更改感到恐惧。这是一项枯燥、重复的工作。把时间花在更有价值的事情上不是更好吗？

如果是这样，你需要一个*任务运行器*或*构建流程*。

## 这听起来复杂得可怕！

创建一个构建流程需要时间。它虽然比手动执行每个任务要复杂，但从长远来看，你将节省数小时的努力，减少人为错误并保持理智。请采取务实的方法：

1. **首先自动化最令人沮丧的任务。**

2. **尽量不要让你的构建流程过于复杂。** 初始设置花费一两个小时完全足够。

3. **选择一个任务运行器软件并坚持一段时间。** 不要一时心血就切换到另一个选项。

某些工具和概念对你来说可能是新的，但请深呼吸，一次专注于一件事。

## 任务运行器：各种选择

像 `GNU Make` 这样的构建工具已经存在十年，但针对 Web 的任务运行器是一个相对新的现象。第一个达到临界点的是 `Grunt` —— 这是一个 Node.js 任务运行器，它使用（最初）由 `JSON` 配置控制的插件。`Grunt` 取得了巨大成功，但也存在许多问题：

1. `Grunt` 需要插件来实现文件监听等基础功能。

2. `Grunt` 插件通常执行多个任务，这使得自定义变得更加笨拙。

3. 对于最基础任务之外的任务，`JSON` 配置可能会变得难以管理。

4. 任务运行速度较慢，因为 `Grunt` 在每个处理步骤之间都会保存文件。

许多问题在后后的版本中得到了解决，但 `Gulp` 已经到来并提供了许多改进：

1. 内置了诸如文件监听等功能。

2. `Gulp` 插件（大多）设计为只做单项工作。

3. `Gulp` 使用 `JavaScript` 配置代码，更简洁、更易读、更易于修改，并提供了更好的灵活性。

4. `Gulp` 速度更快，因为它使用 `Node.js` 流来通过一系列管道式插件传递数据。文件只在任务结束时才写入。

当然，`Gulp` 本身并不完美，新的任务运行器如 `Broccoli.js`、`Brunch` 和 `webpack` 也在竞争开发者的关注。最近，`npm` 本身也被推崇为一种更简单的选择。它们都有自己的优缺点，但 `Gulp` 仍然是首选，目前有超过 40% 的 Web 开发者在使用。`Gulp` 需要 `Node.js`，虽然具备一些 `JavaScript` 知识会有帮助，但所有 Web 编程背景的开发者都会发现它很有用。

## Gulp 4 如何？

本教程描述了如何使用 `Gulp 3` —— 时的最新发布版本。`Gulp 4` 已开发了一段时间，但仍然是一个测试产品。你可以使用或切换到 `Gulp 4`，但我建议在最终发布之前坚持使用版本 3。

## 第 1 步：安装 Node.js

可以在 `nodejs.org/download/` 下载适用于 Windows、macOS 和 Linux 的 `Node.js`。从二进制文件、包管理器和 Docker 镜像安装有多种选择，并提供了完整的说明。

### 针对 Windows 用户

`Node.js` 和 `Gulp` 可以在 Windows 上运行，但如果某些插件依赖于原生 Linux 库（如图像压缩），则它们可能无法运行。Windows 的一种方案是使用新的 bash 命令行，它解决了许多问题。安装后，打开命令提示符并输入：

```
node -v
```

这会显示版本号。你将要大量使用 `npm` —— 用于安装模块的 `Node.js` 包管理器。

### 针对 Linux 用户

`Node.js` 模块可以全局安装到整个系统中。然而，大多数用户没有权限写入全局目录。

除非在 `npm` 命令前加了 `sudo`，否则会访问全局目录。有许多方法可以修复 `npm` 权限，像 `nvm` 等工具可以提供帮助，但我经常更改默认目录。例如，在 Ubuntu/Debian 平台平台上：

```bash
cd ~
mkdir .node_modules_global
npm config set prefix=$HOME/.node_modules_global
npm install npm -g
```

然后，将以下行添加到 `~/.bashrc` 的末尾：

```bash
export PATH="$HOME/.node_modules_global/bin:$PATH"
```

最后，使用此命令更新：

```bash
source ~/.bashrc
```

## 第 2 步：全局安装 Gulp

全局安装 Gulp 命令行界面，以便可以在任何项目文件夹中运行 `gulp` 命令：

```bash
npm install gulp-cli -g
```

使用此命令验证 Gulp 是否已安装：

```bash
gulp v
```

## 第 3 步：配置你的项目

### 针对 Node.js 项目

如果你已经有了 `package.json` 配置文件，可以跳过此步骤。

假设你在 `project1` 文件夹中有一个新项目或现有的项目。进入该文件夹并使用 `npm` 初始化它：

```bash
cd project1
npm init
```

你将被问一系列问题。输入值或按回车键接受默认值。完成后，将创建一个 `package.json` 文件，其中存储了你的 `npm` 配置设置。

### Git 用户

Node.js 将模块安装到 `node_modules` 文件夹中。你应该将其添加到 `.gitignore` 文件中，以确保它们不会被提交到存储库。

当将项目部署到另一台电脑时，你可以运行 `npm install` 来恢复它们。

在本文的剩余部分，我们假设你的项目文件夹包含以下子文件夹：

- `src` 文件夹：预处理源文件（包含更多子文件夹：）

    - `html`:HTML 源文件和模板

    - `images`:原始未压缩的图像

    - `js`:多个预处理过的脚本文件

    - `scss`:多个预处理过的 Sass `.scss` 文件

## 第 4 步：本地安装 Gulp

现在你可以可以使用以下命令在项目文件夹中安装 Gulp：

```bash
npm install gulp --dev
```

这会将 Gulp 安装为开发依赖，并相应地更新 `package.json` 中的 `devDependencies` 部分。在教程的剩余部分，我们假设 Gulp 和所有插件都是开发依赖。

## 备用部署方案

当操作系统中的 `NODE_ENV` 环境变量设置为 `production` 时，不会安装开发依赖。你通常会在你的生产服务器上使用 Mac/Linux 命令执行此操作：

```bash
export NODE_ENV=production
```

或在 Windows 上：

```bash
set NODE_ENV=production
```

本教程假设你的资源将被编译到 build 文件夹并提交到你的 Git 存储库，或直接上传到服务器。然而，如果你想更改创建资源的方式，在生产服务器上构建资源可能会更理想。例如，HTML、CSS 和 JavaScript 文件在生产环境中进行压缩，而在开发环境中不会。在这种情况下，请为 Gulp 和所有插件使用 save 选项，即：

```bash
npm install gulp save
```

这会将 `Gulp` 设置为 `package.json` 中 `"dependencies"` 部分的应用程序依赖。当你运行 `npm install` 时它会被安装，并且可以在部署项目的任何地方运行。你可以从仓库中删除 `build` 文件夹，因为这些文件可以在需要时任何平台上创建。

## 第 4 步：创建 Gulp 配置

在项目文件夹根目录下创建一个新的 `gulpfile.js` 文件。添加一些基础代码来开始：

```javascript
// Gulp.js configuration

var

// modules

gulp = require('gulp'),

// development mode?
devBuild = (process.env.NODE_ENV !== 'production'),

// folders
folder = {
  src: 'src/',
  build: 'build/'
}
```

此代码引用了 `Gulp` 模块，在开发环境（或非生产模式）运行时将 `devBuild` 变量设置为 `true`，并定义了源文件夹和构建文件夹的位置。

## ES6

本教程提供了兼容 ES5 的 JavaScript 代码。这适用于所有版本的 `Gulp` 和 `Node.js`（无论是否带有 harmony 标志）。`Node 6` 及以上版本支持大多数 ES6 特性，因此如果你使用的是较新版本，请自由使用箭头函数、`let`、`const` 等。

`gulpfile.js` 还没有产生任何作用，因为你需要……

## 第 5 步：创建 Gulp 任务

`Gulp` 本身什么都不做。你必须：

1. 安装 `Gulp` 插件，以及

2. 编写利用这些插件来完成有用操作的任务。

编写自己的插件是可能的，但由于已有近 3000 个插件可用，你可能不需要。你可以使用 `Gulp` 官方官方目录 `gulpjs.com/plugins/`、`npmjs.com`，或者搜索 `"gulp *something*"` 来利用 Google 的强大力量。

`Gulp` 提供了三个主要的任务方法：

- `gulp.task` — 定义带有名称、可选依赖项数组和函数的定义任务。

- `gulp.src` — 设置源文件所在的文件夹。

- `gulp.dest` — 设置构建文件将放置的目标文件夹。

任意数量的插件调用都可以通过 `.src` 和 `.dest` 之间的通过 `pipe`（管道）进行设置。

## 图像任务

通过示例来演示最好，所以让我们创建一个基础任务，用于压缩图像并将它们复制到相应的构建文件夹。由于此过程可能需要时间，我们只压缩新的和修改过的文件。有两个插件可以帮助我们：`gulpnewer` 和 `gulpimagemin`。从命令行安装它们：`npm install gulpnewer gulpimagemin save-dev`

我们现在可以在 `gulpfile.js` 顶部引用这两个模块：

```javascript
// Gulp.js configuration

var

// modules

gulp = require('gulp'),
newer = require('gulpnewer'),
imagemin = require('gulpimagemin'),
```

我们现在可以在 `gulpfile.js` 的末尾作为一个函数定义图像处理任务本身：

```javascript
// image processing

gulp.task('images', function() {
  var out = folder.build + 'images/'
  return gulp.src(folder.src + 'images/**/*')
    .pipe(newer(out))
    .pipe(imagemin({ optimizationLevel: 5 }))
    .pipe(gulp.dest(out))
})
```

所有任务在语法上都是相似的。这段代码：

1. 创建了一个名为 `images` 的新任务。

2. 定义了一个带有返回值的函数，该函数……

3. 定义了一个存放构建文件的 `out` 文件夹。

4. 设置了 `Gulp` 源文件夹。`**/*` 确保子文件夹中的图像也会被处理。

5. 将所有文件管道到 `gulpnewer` 模块。比对应目标文件新的源文件将通过。其他所有文件将被移除。

6. 剩余的新或更改的文件管道到 `gulpimagemin`，它设置了一个可选的 `optimizationLevel` 参数。

7. 将压缩后的图像输出到由 `out` 设置的 `Gulp` 文件夹。

保存 `gulpfile.js` 并在命令行运行任务之前，在项目的 `src/images` 文件夹中放置几图像：

```bash
gulp images
```

所有图像都会进行相应的压缩，你会看到如下输出：

`Using file gulpfile.js`

`Running 'imagemin'...`

`Finished 'imagemin' in 5.71 ms`

`gulpimagemin: image1.png (saved 48.7 kB)`

`gulpimagemin: image2.jpg (saved 36.2 kB)`

`gulpimagemin: image3.svg (saved 12.8 kB)`

尝试运行 `gulp images` 应该什么都不会发生，因为没有更新图像了。

## HTML 任务

我们现在可以创建一个类似的任务，从源 HTML 文件夹复制文件。我们可以使用 `gulphtmlclean` 插件安全地压缩我们的 HTML 代码，以删除不必要的空格和属性：

```bash
npm install gulphtmlclean save-dev
```

这在 `gulpfile.js` 顶部被引用：

```javascript
// modules

gulp = require('gulp'),
newer = require('gulpnewer'),
imagemin = require('gulpimagemin'),
htmlclean = require('gulphtmlclean'),
```

我们现在可以在 `gulpfile.js` 的末尾创建一个 html 任务：

```javascript
// HTML processing

gulp.task('html', ['images'], function() {
  var out = folder.build + 'html/',
  page = gulp.src(folder.src + 'html/**/*')
    .pipe(newer(out))
  // 压缩生产环境代码
  if (!devBuild) {
    page = page.pipe(htmlclean())
  }
  return page.pipe(gulp.dest(out))
})
```

这复用了 `gulpnewer` 并引入了几个概念：

1. `[images]` 参数表示在处理 HTML 之前必须运行图像任务（HTML 可能会引用图像）。任意数量的依赖任务都可以列在此数组中，并且它们会在任务运行之前完成。

2. 只有当 `devBuild` 为 false 时，我们才将 HTML 管道到 `htmlclean`。因此，开发期间 HTML 保持未压缩，这有助于调试。

保存 `gulpfile.js` 并从命令行运行 `gulp html`。html 和图像任务都会运行。

## JavaScript 任务

对你来说太简单？让我们通过构建模块打包器来处理所有的 JavaScript 文件。它将：

1. 使用 `gulporder` 插件确保先加载依赖。它分析脚本顶部的注释以确保正确的顺序。例如，`lib.js`。

2. 使用 `gulpconcat` 将所有脚本文件合并为一个 `main.js` 文件。

3. 使用 `gulpstrip` 移除所有 `console` 调试语句并使用 `gulpuglify` 最小化代码。此步骤仅在生产模式下运行时发生。

安装插件 `gulporder`, `gulpconcat`, `gulpstrip`, `gulpuglify`。



## Gulp 任务配置

### JavaScript 任务

首先，安装所需模块：

```bash
npm install gulpdeporder gulpconcat gulpstripdebug gulpuglify savedev
```

在 `gulpfile.js` 的顶部引用它们：

```javascript
var
  ...
  concat = require('gulpconcat'),
  deporder = require('gulpdeporder'),
  stripdebug = require('gulpstripdebug'),
  uglify = require('gulpuglify'),
```

然后添加一个新的 js 任务：

```javascript
// JavaScript processing
gulp.task('js', function() {
  var jsbuild = gulp.src(folder.src + 'js/**/*')
    .pipe(deporder())
    .pipe(concat('main.js'));

  if (!devBuild) {
    jsbuild = jsbuild
      .pipe(stripdebug())
      .pipe(uglify());
  }

  return jsbuild.pipe(gulp.dest(folder.build + 'js/'));
});
```

保存并运行 `gulp js` 来观察魔法的发生！

### CSS 任务

最后，让我们创建一个 CSS 任务，使用 `gulpsass` 将 Sass `.scss` 文件编译为单个 `.css` 文件。这是一个用于 `nodesass` 的 Gulp 插件，它绑定了极快的 Sass 引擎 `LibSass` C/C++ 移植版（你不需要安装 Ruby）。我们假设主 Sass 文件 `scss/main.scss` 负责加载所有的部分（partials）。

我们的任务还将通过 `postcss` 插件利用 `PostCSS`。`PostCSS` 需要它自己的插件，我们将安装这些 `postcss` 来管理资源。

首先，安装所有模块：

```bash
npm install gulpsass gulppostcss postcssassets autoprefixer cssmqpacker cssnano savedev
```

在 `gulpfile.js` 的顶部引用它们：

```javascript
var
  ...
  sass = require('gulpsass'),
  postcss = require('gulppostcss'),
  assets = require('postcssassets'),
  autoprefixer = require('autoprefixer'),
  mqpacker = require('cssmqpacker'),
  cssnano = require('cssnano'),
```

我们现在可以在 `gulpfile.js` 的结尾创建一个新的 css 任务。注意 `images` 任务被设置为依赖，因为 `postcssassets` 插件在构建过程中可以引用图像。此外，大多数插件都可以传递参数（请阅其文档获取更多信息）：

```javascript
// CSS processing
gulp.task('css', ['images'], function() {
  var postCssOpts = [
    assets({ loadPaths: ['images/'] }),
    autoprefixer({ browsers: ['last 2 versions', '> 2%'] }),
    mqpacker
  ];

  if (!devBuild) {
    postCssOpts.push(cssnano);
  }

  return gulp.src(folder.src + 'scss/main.scss')
    .pipe(sass({
      outputStyle: 'nested',
      imagePath: 'images/',
      precision: 3,
      errLogToConsole: true
    }))
    .pipe(postcss(postCssOpts))
    .pipe(gulp.dest(folder.build + 'css/'));
});
```

保存文件并在命令行运行任务：`gulp css`

## 第 6 步：自动化任务

我们之前是一次运行一个任务。我们可以通过向 `gulpfile.js` 中添加一个新的运行任务，在一个命令中运行所有任务：

```javascript
// 运行所有任务
gulp.task('run', ['html', 'css', 'js']);
```

保存并在命令行输入 `gulp run` 来执行所有任务。请注意，我省略了 `images` 任务，因为它已经被设置为 `html` 和 `css` 任务的依赖项。

这仍然太费力了吗？Gulp 提供了另一种方法 —— `gulp.watch` ——它可以监控源文件并在文件发生更改时运行相应的任务。

该方法接收一个文件夹和一个在发生更改时要执行的任务列表。让我们在 `gulpfile.js` 的末尾创建一个新的监听任务：

```javascript
// 监听变化
gulp.task('watch', function() {
  // 图片变化
  gulp.watch(folder.src + 'images/**/*', ['images']);
  // html 变化
  gulp.watch(folder.src + 'html/**/*', ['html']);
  // javascript 变化
  gulp.watch(folder.src + 'js/**/*', ['js']);
  // css 变化
  gulp.watch(folder.src + 'scss/**/*', ['css']);
});
```

与其立即运行 `gulp watch`，让我们添加一个默认任务：

```javascript
// 默认任务
gulp.task('default', ['run', 'watch']);
```

保存 `gulpfile.js` 并在命令行输入 `gulp`。你的图片、HTML、CSS 和 JavaScript 都将进行处理，然后 Gulp 将保持激活状态，等待更新并在需要时重新运行任务。按下 `Ctrl/Cmd + C` 终止监控并返回命令行。

## 第 7 步：大获丰收！

其他你可能发现的插件：

- `gulploadplugins`：无需 require 声明即可加载所有 Gulp 插件模块
- `gulppreprocess`：一个简单的 HTML 和 JavaScript 预处理器
- `gulpless`：Less CSS 预处理器插件
- `gulpstylus`：Stylus CSS 预处理器插件
- `gulpsequence`：按特定顺序运行一系列 gulp 任务
- `gulpplumber`：错误处理，防止 Gulp 在失败时停止
- `gulpsize`：显示文件大小和节省的体积
- `gulpnodemon`：使用 nodemon 在发生更改时自动重启 Node.js
- `gulputil`：工具函数，包括日志记录和颜色编码

`gulputil` 中一个有用的方法是 `.noop()`，它直接传递数据而不执行任何操作。这可以用于更整洁的开发/生产处理代码。例如：

```javascript
var gutil = require('gulputil');

// HTML 处理
gulp.task('html', ['images'], function() {
  var out = folder.src + 'html/**/*';
  return gulp.src(folder.src + 'html/**/*')
    .pipe(newer(out))
    .pipe(devBuild ? gutil.noop() : htmlclean())
    .pipe(gulp.dest(out));
});
```

Gulp 还可以调用其他 Node.js 模块，它们并不一定是插件。例如：

- `browsersync`：当发生更改时自动重新加载资源或刷新浏览器
- `del`：删除文件和文件夹（也许可以在每次运行时清理你的构建文件夹）

投入一点时间，Gulp 就能节省许多小时的开发沮丧。优势是：

- 插件非常丰富
- 使用 pipes 进行配置易读且易于遵循
- `gulpfile.js` 可以在其他项目中适配和复用
- 你可以减少页面的总重量以提高性能
- 你可以简化部署

有用的链接：

- Gulp 主页
- Gulp 插件
- npm 主页

将上述过程应用于一个简单的网站，总重量减少了 50% 以上。你可以使用页面重量分析工具或像 New Relic 服务（它提供了一系列复杂的应用程序性能监控工具）来测试你自己的结果。

Gulp 可以彻底改变你的工作流。希望你发现这个教程有用，并考虑在你的生产流程中使用 Gulp。

***

# Express、Koa 和 Hapi.js 的对比

如果你是一个 Node.js 开发者，很有可能在某个时候用过 Express.js 来创建你的应用程序或 API。Express.js 是一个非常流行的 Node.js 框架，甚至还有其他构建在其之上的框架，如 Sails.js、kraken.js、KeystoneJS 等许多其他。然而，在这种流行之下，其他框架在 JavaScript 世界中也受到了关注，例如 Koa 和 hapi。

在这篇文章中，我们将检查 Express.js、Koa 和 hapi.js —— 它们的相似之处、差异以及用例。

## 背景

让我们首先分别介绍这些框架。

### Express.js

Express.js 被描述为 Node.js 的标准服务器框架。它由 TJ Holowchuk 创建，并在 2014 年被 StrongLoop 收购，目前由 Node.js 孵化器维护。

### Koa

Koa 是 2013 年由 Express 的同事们开发的。它也被认为是更现代。

### Hapi.js

Hapi.js 是 Walmart 团队（由 Eran Hammer 领导）在尝试 Express 并发现其无效后开发的。随着时间的推移，它变成了一个完整的框架。*冷知识：hapi 是 HTTP API 的缩写。*

## 哲学

现在有了框架的背景，让我们根据哲学、路由等重要概念对它们进行比较。

### Express.js

Express 的设计目标是一个简单、无偏见的框架。Express 的哲学是提供小型、健壮的 HTTP 工具，使其成为单页应用程序、网站、混合体或公共 API 的绝佳解决方案。Express.js 开箱即用没有提供许多功能。它不强制文件结构、ORM 或模板引擎。

### Koa

虽然 Express.js 很小，但 Koa 可以拥有更简洁的代码。它的目标是让开发者更有表现力。像 Express.js 一样，它可以使用现有的或自定义的插件和中间件进行扩展。它的方法更具未来感，因为它严重依赖较新的 JavaScript 特性，如生成器和 async/await。

### Hapi.js

Hapi.js 更关注配置，并开箱即提供了比 Koa 和 Express.js 更多的功能。

## 启动服务器

启动服务器是我们在项目中需要做的基础操作之一。让我们看看在不同的框架中如何实现。我们将在每个示例中启动服务器并监听端口 3000。

### Express.js

```javascript
const express = require('express');
const app = express();

app.listen(3000, () => console.log('App is listening on port 3000!'));
```

在 Express.js 中启动服务器非常简单，引入 express 包，初始化 express 应用到 app 变量并调用 `app.listen()` 方法，该方法只是原生 Node.js `http.createServer()` 方法的封装。

### Koa

```javascript
const Koa = require('koa');
const app = new Koa();

app.listen(3000, () => console.log('App is listening on port 3000!'));
```

在 Koa 中启动服务器与 Express.js 非常相似。Koa 中的 `app.listen()` 方法也是对 `http.createServer()` 方法的封装。

### Hapi.js

在 hapi.js 中启动服务器与我们许多人可能在 Express 中习惯的用法有很大不同：

```javascript
const Hapi = require('hapi');

const server = Hapi.server({
  host: 'localhost',
  port: 3000
});

async function start() {
  try {
    await server.start();
  }
  catch (err) {
    console.log(err);
    process.exit(1);
  }
  console.log('Server running at:', server.info.uri);
}

start();
```

在上面的代码块中，我们首先引入了 `hapi` 包，然后使用 `Hapi.server()` 实例化了一个服务器，该方法接受一个单一的配置对象作为参数，该对象包含了 `host` 和 `port` 参数。然后我们使用异步函数 `server.start()` 启动服务器。

与 Express.js 和 Koa 不同，hapi 中的 `server.start()` 函数并不是原生 `http.createServer()` 方法的封装。相反，它实现了自己的自定义逻辑。

上面的代码示例来自 hapi.js 官网，展示了 hapi.js 创造者对配置和错误处理的重视。

## 路由

路由是现代 Web 应用另一个关键方面。让我们在每个框架中为简单的 Hello World 应用定义一个 `/hello` 路由，以感受路由在它们中是如何工作的。

### Express.js

```javascript
app.get('/hello', (req, res) => res.send('Hello World!'));
```

在 Express 中创建路由就像调用带有所需 HTTP 方法的 `app` 对象一样。语法为 `app.METHOD(PATH, HANDLER)`，其中 `PATH` 是服务器上的路径，`HANDLER` 是在路径匹配时被调用的函数。

### Koa

Koa 本身没有内置路由器，因此我们必须使用路由中间件来处理 Koa 应用中的路由。两种常见的路由选项是 `koaroute` 和 `koarouter`。这里是使用 `koaroute` 的示例：

```javascript
const route = require('koaroute');

app.use(route.get('/hello', ctx => {
  ctx.body = 'Hello World!';
}));
```

我们可以立即看到，Koa 需要将每个路由定义为 `app` 上的中间件。`ctx` 是一个包含 Node 请求和响应对象的上下文对象。`ctx.body` 是响应对象中的一个方法，可用于将响应体设置为字符串、Buffer、Stream、Object 或 `null`。`route` 方法的第二个参数可以是异步函数或生成器函数，因此减少了回调函数的使用。

### Hapi.js

```javascript
server.route({
  method: 'GET',
  path: '/hello',
  handler: function (request, h) {
    return 'Hello world!';
  }
});
```

hapi 中的 `server.route()` 方法接受一个带有以下参数的单一配置对象：`method`、`path` 和 `handler`。你可以在这里查看 hapi 路由的文档。

处理器函数中的 `request` 参数是一个包含用户请求详情的对象，而 `h` 参数被描述为响应工具包。

## 中间件

Node 开发者习惯的主要概念之一是处理中间件。

中间件函数是位于请求和响应之间的函数。它们可以访问请求和响应对象，并在处理完后运行下一个中间件。让我们通过实现一个简单的函数，记录请求发送到服务器的时间，来看看它们在不同框架中是如何定义的。

### Express.js

```javascript
app.use((req, res, next) => {
  console.log(`Time: ${Date.now()}`);
  next();
});
```

在 Express.js 中注册中间件与使用 `app.use()` 函数将中间件绑定到 `app` 对象上一样简单。你可以在这里阅读更多关于 Express.js 中间件的内容。

### Koa

```javascript
app.use(async (ctx, next) => {
  console.log(`Time: ${Date.now()}`);
  await next();
});
```

Koa 的中间件注册与 Express.js 类似。主要区别在于上下文对象（`ctx`）代替了 Express.js 中的请求和响应对象，并且 Koa 拥抱现代的 async/await 范式来定义中间件函数。

### Hapi.js

```javascript
server.ext('onRequest', (request, h) => {
  console.log(`Time: ${Date.now()}`);
  return h.continue;
});
```

在 hapi.js 中，请求生命周期中有某些扩展点。`server.ext()` 方法注册一个扩展函数，并在请求生命周期的特定点进行调用。你可以在这里阅读更多相关信息。在上面的示例中，我们利用 `onRequest` 扩展点来注册一个中间件（或扩展）函数。

## 使用建议

从我们看到的比较和代码示例可以看出，显然 Express 和 Koa 最相似，而 hapi.js 是偏离了 Node.js 开发者习惯的规范的框架。因此，在尝试构建快速易用的应用时，hapi.js 可能不是最佳选择。在我看来，在构建中小型应用时，Express 仍然是一个很棒的选择。对于大型应用，它可能会变得有点复杂，因为它缺乏 hapi.js 内置的模块化支持。

总之，这三个框架在启动新项目时都是很棒的选择，但你的选择将取决于项目需求、团队成员以及你所寻求的灵活性。

---

# Sails.js 入门指南

Sails.js 是一个类 Rails 的 Web 框架，允许你快速构建 REST API、单页应用以及实时（基于 WebSockets）应用。它高层地使用了代码生成器，使你能够编写更少代码来构建应用程序——特别是那些可以通过脚手架生成的常见代码。

Sails.js 构建在 `Express.js`（最流行的 Node.js 库之一）和 `Socket.io` 之上（一个为应用程序添加实时、双向、基于事件通信的 JavaScript 库/引擎）。在写作期间，Sails.js 的官方稳定版本为 `0.12.14`，可以通过 `npm` 获取。Sails.js `1.0` 版本尚未正式发布，但根据 Sails.js 创造者的说法，1.0 版本已用于某些生产应用中，他们甚至建议在启动新项目时使用它。

## 核心特性

Sails.js 拥有许多出色的特性：

- 它基于 `Express.js` 构建
- 它支持通过 `WebSockets` 进行实时通信
- 它采取了“约定优于配置”的方法
- 得益于 `Blueprints`，它拥有强大的代码生成能力
- 得益于其强大的 `Waterline` ORM/ODM，它是数据库无关的
- 它在同一个项目中支持多个数据存储器
- 它拥有良好的文档

目前存在一些重要的缺点，例如：

- `Waterline` 不支持 `JOIN` 查询
- 直到 Sails `v1.0`（写作期间处于测试阶段）之前，尚不支持 `SQL` 事务
- 在版本 1.0 之前，它仍然使用 `Express.js v3`，该版本已停止维护（EOL）——开发速度非常缓慢

## Sails.js 对比 Express.js

软件开发的核心在于构建抽象。Sails.js 是 `Express.js` 之上的一个高层抽象层（`Express.js` 本身是对 Node `HTTP` 模块的抽象），它提供了路由、中间件、文件服务等功能。它还添加了强大的 ORM/ODM、MVC 架构模式以及强大的生成器 CLI（以及其他特性）。

你可以使用 Node 的低级 `HTTP` 服务和其他实用程序模块（如 `filesystem` 模块）构建 Web 应用程序，但除非是为了学习 Node.js 平台，否则不建议这样做。你也可以更进一步使用 `Express.js`，这是一个用于构建 Web 应用的流行且轻量级的框架。

你将拥有 Web 应用所需的路由和其他有用构建结构，但你需要处理从配置、文件结构、代码组织到数据库操作的几乎所有事务。

`Express` 没有提供任何帮助你访问数据库的内置工具，因此你将整合所需的技术来构建一个完整的 Web 应用程序。这就是所谓的栈。使用 JavaScript 的 Web 开发者大多使用流行的 `MEAN` 栈，代表 `MongoDB`、`ExpressJS`、`AngularJS` 和 `Node.js`。

`MongoDB` 是 Node/Express 开发者首选的数据库系统，但你可以使用任何需要的数据库。这里最重要的一点是，在数据库方面，`Express` 不提供任何内置 API。

## Waterline ORM/ODM

Sails.js 的一个关键特性是 `Waterline`，这是一个针对基于 `SQL` 的数据库的强大 ORM（对象关系映射）以及针对 `NoSQL` 文档数据库的 ODM（对象文档映射）。`Waterline` 抽象了处理数据库时所有的复杂性，最重要的是，通过 `Waterline`，你不需要在开始开发时就做出选择数据库系统的决策。当你的客户尚未决定使用的数据库技术时，它也不会让你感到无所措。

你可以无需编写单行配置即可构建你的应用程序。事实上，最初完全不需要安装数据库系统。得益于内置的基于 `NeDB` 的 `sailsdisk` 文件数据库，你可以透明地使用文件系统存储和检索数据，以测试你的应用程序功能。

一旦你准备就绪并决定了项目使用的便捷数据库系统，你只需通过安装对应数据库系统的相关适配器即可切换数据库。`Waterline` 为流行的关系型数据库系统（如 `MySQL` 和 `PostgreSQL`）以及 `NoSQL` 数据库（如 `MongoDB` 和 `Redis`）提供了官方适配器，社区还为其他流行的数据库系统（如 `Oracle`、`MSSQL`、`DB2`、`SQLite`、`CouchDB` 和 `neo4j`）构建了大量适配器。如果找不到所需的适配器，你可以开发自定义的适配器。

`Waterline` 抽象了不同数据库系统之间的差异，允许应用程序通过标准化的接口与任何支持的数据库系统进行通信。你不需要处理 `SQL` 或任何低级 API（针对 `NoSQL` 数据库），但这并不意味着你不能这样做（至少对于基于 `SQL` 的数据库和 `MongoDB`）。

在某些情况下你需要编写自定义 `SQL`，例如出于性能考虑、处理复杂的数据库需求或访问特定的数据库功能。在这种情况下，可以使用仅适用于配置为使用 `SQL` 系统的 Waterline 模型的 `.query()` 方法（你可以在文档中找到更多关于 `query()` 的信息）。

由于不同的数据库系统具有通用特性和特定特性，`Waterline` ORM/ODM 只有在你仅限制于使用通用特性时才对你有益处。此外，如果你使用原始 `SQL` 或原生 `MongoDB` API，你将失去许多 `Waterline` 的特性。

## 开始使用 Sails.js

现在我们已经涵盖了 Sails.js 的基本概念和特性，让我们看看如何使用 Sails.js 快速上手。

### 先决条件

在使用 Sails.js 之前，你需要一个安装了 `Node.js`（以及 `npm`）的开发环境。你可以访问 Node.js 网站并下载安装程序来安装它们。

同时，确保安装了你想配合 Sails.js 使用的数据库管理系统（无论是关系型还是 `NoSQL` 数据库）。如果你现在不想使用完整的数据库系统，由于 `sailsdisk` 的存在，你仍然可以工作。

### 安装 Sails.js CLI

满足开发要求后，进入终端（Linux 和 macOS）或命令提示符（Windows），通过 `npm` 全局安装 Sails.js 命令行工具：

```bash
sudo npm install sails -g
```

如果你想安装最新的 *1.0* 版本来尝试新功能，需要使用 beta 版本：

```bash
npm install sails@beta -g
```

根据你的 npm 配置，全局安装包可能需要 `sudo`。

### 脚手架生成 Sails.js 项目

完成后，你可以通过一个命令脚手架生成新项目：

```bash
sails new sailsdemo
```

这将在当前目录下创建一个名为 `sailsdemo` 的项目文件夹。你也可以在现有文件夹内脚手架生成项目文件：

```bash
sails new .
```

你可以通过以下命令生成一个没有前端的 Sails.js 项目：

```bash
sails new sailsdemo --nofrontend
```

从文档中可以了解更多关于 CLI 特性的信息。

## Sails.js 项目结构

一个 Sails.js 项目是一个 Node.js 模块，包含 `package.json` 和 `node_modules` 文件夹。你可能还会注意到 `Gruntfile.js` 的存在。Sails.js 使用 Grunt 作为构建前端资源的工具。

如果你正在为浏览器构建应用，那么你运气不错了。Sails 内置了 Grunt ——这意味着你的整个前端资源工作流都是完全可定制的，并且支持目前现有的所有优秀 Grunt 模块。这包括对 Less、Sass、Stylus、CoffeeScript、JST、Jade、Handlebars、Dust 等许多模块的支持。当你准备好进入生产环境时，你的资源会自动进行压缩和 gzip 压缩。你甚至可以编译静态资源并将其推送到像 CloudFront 这样的 CDN，让应用加载得更快。（你可以在 Sails.js 网站上阅读更多关于这些点的信息。）

你也可以通过生成器使用 Gulp 或 Webpack 作为你的构建系统，而不是 Grunt。请查看 GitHub 上的 `sails-generate-new-gulp` 和 `sails-webpack` 项目。

更多社区生成器，请查看 Sails.js 网站上的此文档页面。

### 项目结构详解

项目包含许多配置文件和文件夹。大多数内容都是一目了然的，但让我们过一下你最经常使用的几个：

- `api/controllers`：这是存放控制器的文件夹。控制器对应于 `MVC` 中的 `C` 部分。它是你应用程序业务逻辑所在的地方。
- `api/models`：存放模型的文件夹。模型对应于 `MVC` 架构中的 `M` 部分。你需要在这里放置映射到 SQL/NoSQL 数据的类或对象。
- `api/policies`：这是你存放应用程序策略的文件夹。
- `api/responses`：此文件夹包含服务器响应逻辑，例如处理 404 和 500 响应的函数等。
- `api/services`：这是你应用级服务所在地。服务是一个全局类，封装了可以在多个控制器中复用的通用逻辑。
- `views`：此文件夹包含用于显示视图的模板。默认情况下，该文件夹包含 `ejs` 引擎模板，但你可以配置任何 Express 支持的引擎，如 EJS、Jade、Handlebars、Mustache 和 Underscore 等。
- `config`：此文件夹包含许多配置文件，允许你配置应用程序的每一个细节，例如 CORS、CSRF 保护、i18n、http、模型、视图、日志和策略的设置等。你经常使用的一个重要文件是 `config/routes.js`，你可以在这里创建应用程序路由，并将它们映射到控制器的实际操作或直接映射到视图。
- `assets`：这是你可以在其中应用程序放置任何静态文件（CSS、JavaScript 和图像等）的文件夹。

### 运行你的 Sails.js 项目

你可以通过在项目根目录下运行以下命令来启动开发服务器：

```bash
sails lift
```

这会提示你选择一种迁移策略，然后启动开发服务器。

然后你可以使用网络浏览器访问 [`localhost:1337/`](http://localhost:1337/)。如果你生成了一个带有前端的 Sails.js 项目（即没有使用 `--nofrontend` 选项），你将看到首页。

## 创建 Waterline 模型

模型是一种抽象，通常在通用编程语言中用对象或类表示，它引用/映射到关系型数据库中的 SQL 表，或者 NoSQL 数据库中的文档（键值对）。

你可以使用 Sails.js CLI 创建模型：

```bash
sails generate model product
```

这将在 `api/models` 中创建一个 `Product.js` 模型，内容如下：

```javascript
/**
* Product.js
*
* @description :: TODO: 你可以在这里写关于此模型如何工作以及它代表什么的简短摘要。
* @docs :: http://sailsjs.org/documentation/concepts/modelsandorm/models
*/
module.exports = {
  attributes: {

  }
};
```

然后你可以为你的模型扩展属性。例如：

```javascript
module.exports = {
  attributes: {
    name: {
      type: 'string',
      defaultsTo: '',
      required: true
    },
    description: {
      type: 'string',
      defaultsTo: ''
    },
    quantity: {
      type: 'integer'
    },
    user: {
      model: 'User'
    }
  }
};
```

注意我们如何为模型 `User` 定义关联（一对多 `onetomany` 或属于 `belongsTo` 关系）。你可以通过 Sails.js 关联页面查看所有支持的关联以及如何创建它们。

关于可用模型属性的更多信息，请参阅 Sails.js 属性页面。

你也可以通过在模型定义中添加顶层属性来为每个模型或模型设置添加配置，这将覆盖 `config/models.js` 中的全局模型设置。你可以覆盖与模型属性、数据库连接等相关的设置。

例如，让我们为 `product` 模型指定一个不同于项目范围内使用的全局数据存储器：

```javascript
module.exports = {
  connection: 'mysqlcon',
  attributes: { /*...*/ }
};
```

这将指示 Sails.js 使用名为 `mysqlcon` 的连接来存储此模型的数据。

请确保你已在 `config/connections.js` 的 `connections` 对象中添加了 `mysqlcon` 连接：

```javascript
module.exports.connections = {
  // sailsdisk 是默认安装的。
  localDiskDb: {
    adapter: 'sailsdisk'
  },
  mysqlcon: {
    adapter: 'sailsmysql',
    host: 'YOUR_MYSQL_HOST',
    user: 'YOUR_MYSQL_USER',
    password: 'YOUR_MYSQL_PASSWORD',
    database: 'YOUR_MYSQL_DB'
  }
};
```

你还需要从 npm 安装 `sailsmysql` 适配器：`npm install sailsmysql@forsails0.12`。

你可以在 Sails.js 模型设置页面找到可以指定的可用模型设置。

## Sails.js 控制器

控制器持有应用程序的业务逻辑。它们位于 `api/controllers` 中，并提供了一个胶接应用程序模型和视图的层。控制器包含绑定到路由并响应来自 Web/移动客户端 HTTP 请求的操作。

控制器是一个 JavaScript 对象，包含名为“控制器操作”的方法，这些方法接收两个参数：`request` 和 `response`。

你可以在 Sails.js 控制器页面找到更多关于控制器的信息。

你可以使用 Sails.js CLI 生成控制器：

```bash
sails generate controller product
```

此命令将生成一个名为 `api/controllers/ProductController.js` 的控制器，内容如下：

```javascript
/**
* ProductController
*
* @description :: 管理产品的服务器端逻辑
* @help :: http://sailsjs.org/#!/documentation/concepts/Controllers
*/
module.exports = {

};
```

代码导出一个空的 JavaScript 对象，你可以在其中添加新操作或覆盖默认（自动添加）的控制器操作。

此时，你实际上可以在不添加任何代码的情况下对你的服务器执行 CRUD 操作。由于 Sails.js 遵循“约定优于配置”的原则，它会将你的控制器连接到相应的路由，并为处理常见的 POST、GET、PUT 和 DELETE 请求提供默认操作。

## 使用 Postman 进行测试

使用 Postman，你可以发送 POST、GET 等请求来测试你的 API，所以请获取适用于你操作系统的 Postman 版本。

接下来，输入端点 URL `http://localhost:1337/product`。然后选择要发送的 HTTP 方法——在这里是 POST，因为我们要创建一个产品。接下来你需要提供数据，因此点击 *Body* 标签，选择 *Raw* 选项，然后输入以下内容：

```json
{
  "name": "Product 1",
  "description": "This is product 1",
  "quantity": 100
}
```

然后点击 Send。你应该注意返回的状态码：200 OK 表示产品创建成功。

你可以通过发送 GET 请求来验证产品是否创建。

你还可以通过发送 PUT 请求根据 ID 更新产品。

最后，你可以通过发送 DELETE 请求根据 ID 删除产品。

对于自定义逻辑，也可以覆盖这些操作并实现自己的逻辑。

当你创建一个 API（即控制器和模型）时，Sails.js 会自动添加八个默认操作，如下：

- add to
- create
- destroy
- find one
- find where
- populate where
- remove from
- update

`find where` 和 `find one`，`create`、`update` 和 `destroy` 都是大多数 API 中都需要存在的标准 CRUD 操作。其他的与外键记录有关：

- `add to`：用于将外键记录添加到另一个记录集中（例如将一个产品添加到用户的产品列表中）。
- `populate where`：用于为另一个记录的关联填充并返回外键记录。
- `remove from`：用于从相关的记录集合关联（例如用户的产品列表）中移除外键记录（例如某个产品）。

若要自定义默认操作的行为，你可以采取以下任一方法：

1. 在指定的控制器中覆盖操作。也就是说，创建一个与这些操作之一同名的操作：`find`、`findOne`、`create`、`update`、`destroy`、`populate`、`add` 或 `remove`。
2. 覆盖所有控制器的默认操作。你可以通过创建一个 `api/blueprints` 文件夹来实现，你需要在其中添加以默认操作小写命名的文件（例如 `find.js`、`findone.js`、`create.js` 等）。你可以通过检查 Sails.js Blueprint API 文档找到更多关于蓝图的信息。

## Sails.js 中的路由

路由允许你将 URL 映射到控制器或视图。与默认操作一样，Sails.js 会自动为默认操作添加默认路由，让你只需创建模型和控制器即可拥有自动 API。

你也可以为自定义操作或视图添加自定义路由。要添加路由，请打开 `config/routes.js` 文件并添加以下内容：

```javascript
module.exports.routes = {
  '/products': {
    view: 'products'
  }
};
```

这将 `/products` 映射到 `views` 文件夹中名为 `products` 的模板。

你可以选择性在 URL 中添加 HTTP 动词。例如：

```javascript
module.exports.routes = {
  'get /': {
    view: 'homepage'
  }
};
```

你还可以为路由指定控制器操作。例如：

```javascript
module.exports.routes = {
  'post /product': 'ProductController.create',
};
```

这告诉 Sails.js 当客户端向 `/product` 端点发送 POST 请求时，调用 `ProductController` 控制器的 `create` 操作。

## 结论

在本章中，你接触了 Sails.js。我们学习了 Sails.js 的基本概念、如何生成一个新的 Sails.js 项目，然后通过仅生成模型、添加一些属性并生成控制器创建了一个 API。Sails.js 还有其他高级概念，如服务、策略、蓝图和钩子。一旦掌握并熟悉了本介绍中的基本概念，你就可以进一步发现它们。



# 通过 git 从此处下载初始代码

```bash
git clone https://github.com/markbrown4/hapiapi.git
cd hapiapi
```

```bash
npm install
```

打开 `package.json`，你会发现 `start` 脚本使用 `nodemon` 运行 `server.js`。这会在我们修改文件时自动为我们重启服务器。

运行 `npm start` 并打开 `http://localhost:3000/`：

```json
[{ "so": "hapi!" }]
```

## 让我们来看源码

```javascript
// server.js

const Hapi = require('hapi')

// 配置服务器实例

const server = Hapi.server({
  host: 'localhost',
  port: 3000
})

// 添加路由
server.route({
  method: 'GET',
  path: '/',
  handler: () => {
    return [{ so: 'hapi!' }]
  }
})

// 启动！
server.start().then(() => {
  console.log('Server running at:', server.info.uri)
}).catch(err => {
  console.log(err)
  process.exit(1)
})
```

### 路由处理器

路由处理器是这段代码中最有趣的部分。将它替换为下面的代码，逐行注释掉 `return` 语句，并在浏览器中测试响应。

```javascript
server.route({
  method: 'GET',
  path: '/',
  handler: () => {
    // return [{ so: 'hapi!' }]
    return 123
    return `<h1><marquee>HTML <em>rules</em></marquee></h1>`
  }
})
```

## 配置数据库

```javascript
// 配置数据库主机、用户、密码的连接，SQLite 不需要这些
const sequelize = new Sequelize(null, null, null, {
  dialect: 'sqlite',
  storage: path.join('tmp', 'db.sqlite') // SQLite 将数据直接持久化到文件
})

// 在这里我们定义 Article 模型，包含一个字符串类型的 title 属性和一个文本类型的 body 属性。默认情况下，所有表都会 id、createdAt 和 updatedAt 列。

const Article = sequelize.define('article', {
  title: Sequelize.STRING,
  body: Sequelize.TEXT
})

// 创建表
Article.sync()

module.exports = {
  Article
}
```

让我们通过导入新模型并将路由处理程序替换为以下内容来测试它：

```javascript
// server.js
const { Article } = require('./models')

server.route({
  method: 'GET',
  path: '/',
  handler: () => {
    // 尝试逐行注释掉这些代码
    return Article.findAll()

    return Article.create({ title: '欢迎来到我的博客', body: '地球上的乐园' })
    return Article.findById(1)

    return Article.update({ title: '学习 Hapi', body: `JSON API 轻而易举.` }, { where: { id: 1 } })
    return Article.findAll()

    return Article.destroy({ where: { id: 1 } })

    return Article.findAll()
  }
})
```

如果你熟悉 SQL 或其他 ORM，`Sequelize` 的 API 应该是自而易懂的，它是基于 Promise 构建的，因此与 Hapi 的异步处理程序完美契合。

> **注意**：在本文演示的场景下，使用 `Article.sync()` 创建表或使用 `Article.sync({ force: true })` 删除并创建表都是可以的。如果你想在生产环境中使用它，应该检查 `sequelizecli` 并为任何架构更改编写 `Migrations`（迁移）。

## 我们的 RESTful 动作

让我们构建以下路由：

- `GET /articles` 获取所有文章
- `GET /articles/:id` 根据 ID 获取文章
- `POST /articles` 使用 `{ title, body }` 参数创建文章
- `PUT /articles/:id` 使用 `{ title, body }` 参数更新文章
- `DELETE /articles/:id` 根据 ID 删除文章

添加一个新文件 `routes.js`，将服务器配置与应用逻辑分离：

```javascript
// routes.js

const { Article } = require('./models')

exports.configureRoutes = (server) => {
  // server.route 接受一个对象或一个数组
  return server.route([{
    method: 'GET',
    path: '/articles',
    handler: () => {
      return Article.findAll()
    }
  }, {
    method: 'GET',
    // 大括号是我们定义参数（URL 中的可变路径段）的方式
    path: '/articles/{id}',
    handler: (request) => {
      return Article.findById(request.params.id)
    }
  }, {
    method: 'POST',
    path: '/articles',
    handler: (request) => {
      const article = Article.build(request.payload.article)
      return article.save()
    }
  }, {
    // method 可以是一个数组
    method: ['PUT', 'PATCH'],
    path: '/articles/{id}',
    handler: async (request) => {
      const article = await Article.findById(request.params.id)
      article.update(request.payload.article)
      return article.save()
    }
  }])
}
```

```bash
http GET http://localhost:3000/articles
http GET http://localhost:3000/articles/2
http PUT http://localhost:3000/articles/2 article='{"title": "True happiness, is an inner quality"}'
http GET http://localhost:3000/articles/2
http DELETE http://localhost:3000/articles/2
http GET http://localhost:3000/articles
```

Okay, everything seems to be working. let’s try few more:

```bash
http GET http://localhost:3000/articles/12345
http DELETE http://localhost:3000/articles/12345
```

Yikes! When we try to fetch an article that doesn't exist, we get 200 with empty body and our handler throws in 500. This is happening because `findById` returns null. We want our API to respond with 404 in both cases. There’s few ways we can achieve this.

### 方案一：防御性地检查 NULL 并返回错误

有一个名为 `boom` 的包可以帮助创建标准响应对象：`npm install boom`

导入它并修改 `/articles/:id` 路由：

```javascript
// routes.js
const Boom = require('boom')

{
  method: 'GET',
  path: '/articles/{id}',
  handler: async (request) => {
    const article = await Article.findById(request.params.id)
    if (article === null) return Boom.notFound()
    return article
  }
}
```

### 方案二：扩展 SEQUELIZE.MODEL 以抛出错误

`Sequelize.Model` 是所有模型继承的原型引用，因此我们可以轻松地添加一个新方法 `find` 来封装 `findById`，如果返回 null 则抛出错误：

```javascript
// models.js
const Boom = require('boom')
Sequelize.Model.find = async function (...args) {
  const obj = await this.findById(...args)
  if (obj === null) throw Boom.notFound()
  return obj
}
```

然后我们可以恢复处理程序的原始形式，并将 `findById` 的出现替换为 `find`：

```javascript
{
  method: 'GET',
  path: '/articles/{id}',
  handler: (request) => {
    return Article.find(request.params.id)
  }
}
```

```bash
http GET http://localhost:3000/articles/12345
http DELETE http://localhost:3000/articles/12345
```

`Boom`。现在每当我们尝试从数据库获取不存在的内容时，都会得到 404 Not Found 错误。我们用一个易于理解的约定替换了自定义错误检查，保持了代码的整洁。

> **注意**：另一个用于向 REST API 发出请求的流行工具是 Postman。如果你更喜欢 UI 和保存常用请求的功能，这是一个不错的选择。

### 路径参数

Hapi 中的路由与其他框架略有不同。路由是根据路径的特异性来选择的，因此定义它们的顺序无关紧要。

- `/hello/{name}` 匹配 `/hello/bob` 并将 'bob' 作为 `name` 参数传递
- `/hello/{name?}` —— `?` 使 name 成为可选的，同时匹配 `/hello` 和 `/hello/bob`
- `/hello/{name*2}` —— `*` 表示多个片段，匹配 `/hello/bob/marley` 并将 'bob/marley' 作为 `name` 参数传递
- `/{args*}` 匹配 `/any/route/imaginable` 且具有最低的特异性。

### 请求对象

传递给路由处理程序的请求对象具有以下有用属性：

- `request.params` —— 路径参数
- `request.query` —— 查询字符串参数
- `request.payload` —— JSON 或表单参数的请求体
- `request.state` —— Cookies
- `request.headers`
- `request.url`

## 添加第二个模型

我们的第二个模型将处理文章的评论。这是完整的文件：

```javascript
// models.js
const path = require('path')
const Sequelize = require('sequelize')
const Boom = require('boom')

Sequelize.Model.find = async function (...args) {
  const obj = await this.findById(...args)
  if (obj === null) throw Boom.notFound()
  return obj
}

const sequelize = new Sequelize(null, null, null, {
  dialect: 'sqlite',
  storage: path.join('tmp', 'db.sqlite')
})

const Article = sequelize.define('article', {
  title: Sequelize.STRING,
  body: Sequelize.TEXT
})

const Comment = sequelize.define('comment', {
  commenter: Sequelize.STRING,
  body: Sequelize.TEXT
})

// 这些关联向我们的评论添加了 articleId 外键
// 它们添加了有用的方法，如 article.getComments() 和 article.createComment()
Article.hasMany(Comment)
Comment.belongsTo(Article)

// 创建表
Article.sync()
Comment.sync()

module.exports = {
  Article,
  Comment
}
```

```javascript
const { Article, Comment } = require('./models')

{
  method: 'POST',
  path: '/articles/{id}/comments',
  handler: async (request) => {
    const article = await Article.find(request.params.id)
    return article.createComment(request.payload)
  }
},
{
  method: 'DELETE',
  path: '/articles/{articleId}/comments/{id}',
  handler: async (request) => {
    const { id, articleId } = request.params
    const comment = await Comment.find(id, { where: { articleId } })
    return comment.destroy()
  }
}
```

你可以将选项作为第二个参数传递给 `findById`：

```javascript
const comment = await Comment.find(id, { where: { articleId } })
```

最后，我们可以扩展 `/articles/:id` 以同时返回文章及其评论：

```javascript
{
  method: 'GET',
  path: '/articles/{id}',
  handler: async (request) => {
    const article = await Article.find(request.params.id)
    const comments = await article.getComments()
    return { ...article.get(), comments }
  }
}
```

这里的 `article` 是 `Model` 对象；`article.get()` 返回一个包含模型值的普通对象，我们可以在其上使用展开运算符将其与评论合并。让我们测试一下：

```http
http POST http://localhost:3000/articles/3/comments comment='{ "commenter": "mb4", "body": "Agreed, this blog rules!" }'
```

```http
http POST http://localhost:3000/articles/3/comments comment='{ "commenter": "Nigerian prince", "body": "You are the beneficiary of a Nigerian prince’s $4,000,000 fortune." }'
```

```bash
http GET http://localhost:3000/articles/3
http DELETE http://localhost:3000/articles/3/comments/2
http GET http://localhost:3000/articles/3
```

我们的博客 API 几乎准备好上线生产了，只需要进行最后的完善。

## 使用 JWT 进行身份验证

JSON Web Tokens 是 API 一种常见的身份验证机制。有一个名为 `hapi-auth-jwt2` 的插件可以设置它，但它还没有针对 Hapi 17.0 更新，因此我们目前需要安装一个分支：

```bash
npm install save salzhrani/hapi-auth-jwt2#v17
```

下面的代码注册了 `hapi-auth-jwt2` 插件，并使用 `jwt` `scheme` 设置了一个名为 `admin` 的 `strategy`。如果在头部、查询字符串或 Cookie 中发送了有效的 JWT 令牌，它将调用我们的 `validate` 函数来验证我们是否允许这些凭据的访问：



```javascript
// auth.js

const jwtPlugin = require('hapiauthjwt2').plugin

// 这在生产环境中应该是一个环境变量
const JWT_KEY = 'NeverShareYourSecret'

var validate = function (credentials) {
  // 在此处运行任何检查以确认我们是否想要授予这些凭据访问
  return {
    isValid: true,
    credentials // request.auth.credentials
  }
}

exports.configureAuth = async (server) => {
  await server.register(jwtPlugin)
  server.auth.strategy('admin', 'jwt', {
    key: JWT_KEY,
    validate,
    verifyOptions: { algorithms: ['HS256'] }
  })
  // 默认所有路由都需要 JWT，并对公共路由排除
  server.auth.default('admin')
}
```

接下来，在启动服务器之前，导入并配置我们的认证策略：

```javascript
// server.js
const { configureAuth } = require('./auth')

const main = async () => {
  await configureAuth(server)
  await configureRoutes(server)
  await server.start()
  return server
}
```

现在，所有路由都将需要我们的 `admin` 认证策略。尝试以下三个：

`http GET localhost:3000/articles`

`http GET localhost:3000/articles Authorization:yep`

`http GET localhost:3000/articles Authorization:eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6MSwibmFtZSI6IkFudGhvbnkgVmFsaWQgVXNlciIsImlhdCI6MTQyNTQ3MzUzNX0.KA68l60mjiC8EXaC2odnjFwdIDxE__iDu5RwLdN1F2A`

最后一个应该包含有效的令牌并返回数据库中的文章。要让某个路由变为公共，我们只需要在路由对象中添加 `config: { auth: false }`。例如：

```javascript
{
  method: 'GET',
  path: '/articles',
  handler: (request) => {
    return Article.findAll()
  },
  config: { auth: false }
}
```

# Express.js

Express.js 是一个 Node.js 框架，因其简单性而赢得了巨大的人气。它提供了路由和对视图引擎的支持，远优于基础 Node 服务器。

## 亮点

然而，启动一个 Express 应用需要一些模板代码：启动服务器实例、配置视图引擎以及设置错误处理。

## 支持

虽然有各种启动项目和模板，但 Express 有一个自己的命令行工具用于启动应用，名为 `express-generator`。

## 什么是 Express?

Express 内置许多功能，还可以与其他包无缝集成获取更多功能，但它原生提供了三个核心功能：

1. **路由**：这是通过 `/home`、`/blog` 和 `/about` 提供不同页面的方式。Express 允许将不同的路由放在不同的文件中，实现模块化。

2. **中间件**：如果你对这个术语陌生，中间件基本上是“软件胶水”。它在路由获取请求之前访问请求，处理 Cookie 解析、文件上传、错误等问题。

3. **视图**：这是渲染自定义 HTML 页的方式。传递要渲染的数据，Express 将使用你提供的视图引擎进行渲染。

## 如何开始

使用 Express 生成器启动新项目只需运行几条命令：

```bash
npm install express-generator -g
express myapp
cd myapp
npm install
```

`express-generator` 包含了几个 Express 服务器常用的依赖项。如果前端和 API 不在同一域名下，你需要开启 CORS：

```javascript
const express = require('express')
const server = express({
  host: 'localhost',
  port: 3000,
  cors: {
    origin: true
  }
})
```

如果前端和 API 在同一域名下，你就不需要考虑 CORS：

```javascript
const server = express({
  host: 'localhost',
  port: 3000
})
```

`express` 命令支持 `--css less|stylus|compass|sass` 参数。默认情况下，生成器会为你创建一个基础的 CSS 文件，但选择 CSS 引擎将为你的新应用配置中间件，以编译上述任何选项。

现在我们已经设置好了项目并安装了依赖，可以通过运行以下命令来启动新服务器：

```bash
npm start
```

然后，在浏览器中访问 `http://localhost:3000`。

# 应用结构

生成的 Express 应用最初包含四个文件夹。

## BIN

`bin` 文件夹包含启动应用程序的可执行文件。它会启动服务器（如果没有提供备选端口，则在 `3000` 端口启动）并设置一些基本的错误处理。你不需要真正担心这个文件，因为 `npm start` 会为你运行它。

## PUBLIC

`public` 文件夹是重要的文件夹之一：

* 此文件夹中的所有内容都都可以被连接到你应用程序的人访问。在这个文件夹中，你将放置用户访问你的网站时所需的 JavaScript、CSS、图像和其他资产。

## ROUTES

`routes` 文件夹是你存放路由文件的地方。生成器创建了两个文件 `index.js` 和 `users.js`，它们作为如何分离应用程序路由配置的示例。

通常，这里会为你网站上的每个主要路由准备不同的文件。因此，你可能在这个文件夹中拥有名为 `blog.js`、`home.js` 和/或 `about.js` 的文件。

## VIEWS

`views` 文件夹存放模板引擎使用的文件的地方。生成器会配置 Express，以便在你调用 `render` 方法时在此处查找匹配的视图。

在这些文件夹之外，有一个文件你应该非常熟悉。

### app.js

`app.js` 文件非常特殊，因为它设置了你的 Express 应用程序并将所有不同部分胶合在一起。让我们来看一下它的功能。以下是文件的开头部分：

```javascript
var express = require('express')
var path = require('path')
var favicon = require('serve-favicon')
var logger = require('morgan')
var cookieParser = require('cookie-parser')
var bodyParser = require('body-parser')
```

该文件的前六行是引入（requires）。如果你是 Node 的初学者，请务必阅读《理解 Node.js 中的 `module.exports` 和 `exports`》。

```javascript
var routes = require('./routes/index')
var users = require('./routes/users')
```

接下来的两行代码引入了 Express 生成器默认设置的不同路由文件：`routes` 和 `users`。

```javascript
var app = express()
```

之后，我们通过调用 `express()` 创建一个新的应用。`app` 变量包含了应用程序的所有设置和路由。这个对象将你的应用程序胶合在一起。

```javascript
app.set('views', path.join(__dirname, 'views'))
app.set('view engine', 'jade')
```

一旦创建了 `app` 实例，就会设置用于渲染视图的模板引擎。如果你想更改视图文件的路径，可以在这里修改。

之后，你会看到 Express 正在配置使用中间件。生成器安装了几个你可能在 Web 应用中常用的常用中间件。

```javascript
app.use(favicon(path.join(__dirname, 'public', 'favicon.ico')))
app.use(logger('dev'))
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({ extended: false }))
app.use(cookieParser())
app.use(express.static(path.join(__dirname, 'public')))
```

- `favicon`。这个非常不言而喻：它只是从你的 `public` 目录中提供 `favicon.ico`。

- `logger`。当你运行应用时，你可能会注意到所有请求的路由都记录在控制台中。如果你想禁用此功能，可以直接注释掉这个中间件。

- `bodyParser`。你可能会注意到有两行用于解析传入的 HTTP 请求体。第一行处理通过 `POST` 请求发送的 JSON，并将这些数据放入 `request.body`。第二行解析 URL 中的查询字符串数据（例如 `/profile?id=5`）并将其放入 `request.query`。

- `cookieParser`。它获取客户端发送的所有 cookie 并将其放入 `request.cookies` 中。它还允许你在将其发送回客户端之前通过更改 `response.cookies` 来修改它们。

- `express.static`。此中间件从你的 `public` 文件夹中提供静态资产。如果你想重命名或移动 `public` 文件夹，可以在这里更改路径。

接下来是路由：

```javascript
app.use('/', routes)
app.use('/users', users)
```

在这里，引入的示例路由文件被挂载到我们的 `app` 上。如果你需要添加额外的路由，请在此处进行。

此后的所有代码都用于错误处理。除非你想更改 Express 处理错误的方式，否则你通常不需要修改这些代码。默认情况下，它被设置为在开发模式下显示路由中发生的错误。

# 一个实用的工具

希望你现在已经清楚了 `express-generator` 工具在启动新的基于 Express 的项目时，如何节省你编写重复样板代码的时间。通过提供合理的默认文件结构，并安装和连接通常所需的中间件，生成器只需几条命令就能为新应用奠定坚实的基础。

# MongoDB 简介

作者：MANJUNATH M

MongoDB 是一个开源、面向文档的 NoSQL 数据库。如果你接触过传统的关系型数据库，面向文档的 NoSQL 数据库的想法听起来确实很奇怪。“数据库怎么没有表？”，你可能会这样想。

以下是官方文档对 MongoDB 的描述：MongoDB 是由 MongoDB Inc 开发的可扩展灵活数据库，以 JSON 类文档存储数据。

NoSQL 数据库中的文档对应 SQL 数据库中的行。一组文档被称为集合，它大致相当于关系型数据库中的表。关于 NoSQL 和 SQL 数据库及其差异的深度概述，我们已经在 SQL vs NoSQL 教程中涵盖了。

除了是一个 NoSQL 数据库，MongoDB 还有一些自身的特性。我在下面列出了一些关键特性：

- 它易于安装和设置
- 它使用 BSON（一种 JSON 类格式）存储数据，便于将文档对象映射到你的应用程序代码
- 它具有高度的可扩展性和可用性，并内置了复制支持
- 它支持 MapReduce 操作，将海量数据压缩为有聚合结果
- 它是免费且开源的。

MongoDB 支持所有主流平台和发行版，如果你有疑问，可以查看它们的官方文档。

我在下方涵盖了在 macOS 上安装 MongoDB 的说明。对于 Linux，MongoDB 建议使用你发行版的包管理器来帮助安装该软件。如果你使用的是 Windows，只需从 MongoDB 网站下载最新发布版本并运行交互式安装程序即可。

# 使用 Homebrew 在 macOS 上安装 MongoDB

Homebrew 是适用于 macOS 的包管理器，本教程假设你已经在机器上安装了 Homebrew。

1. 打开终端应用程序（terminal）并运行

```bash
brew update
```

2. 一旦 `brew` 更新，按照以下步骤安装 `mongodb` 包：

```bash
brew install mongodb
```

3. 创建数据目录，以便 `mongod` 进程能够写入数据。默认情况下，该目录为 `/data/db`：

```bash
mkdir -p /data/db
```

4. 确保你的用户账户有权限向该目录读写数据：

```bash
sudo chown -R $USER /data/db
```

# 输入你的密码

5. 启动 mongo 服务。运行 `mongod` 命令启动服务器。

6. 启动 Mongo shell。打开另一个终端窗口并运行 `mongo`。mongo shell 将尝试连接到我们之前启动的 mongo 守护进程。

一旦成功连接，你就可以使用 shell 作为练习场安全地运行所有命令。

7. 运行 `quit()` 退出 Mongo shell，按 `control + C` 停止 mongo 守护进程。

现在我们已经运行了 mongo 守护进程，让我们熟悉一下 MongoDB 的基础。

# 基础数据库操作

如果你还没有进入，请进入 Mongo shell：

```bash
[mj@localhost ~]$ mongo
MongoDB shell version v3.6.1
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.1
connecting to: test
```

登录时，你可以看到我的 MongoDB shell 版本。默认情况下，你连接到 `test` 数据库。你可以通过运行 `db` 来验证当前数据库名称：

```bash
db
test
```

这太棒了，但如果我们想要一个新数据库呢？要创建一个数据库，MongoDB 有一个 `use DATABASE_NAME` 命令：

```bash
use exampledb
switched to db exampledb
```

要显示所有现有数据库，尝试 `show dbs`：

```bash
show dbs
local 0.078GB
prototype 0.078GB
test 0.078GB
```

`exampledb` 不在列表中，是因为我们需要向数据库中插入至少一个文档。要插入文档，你可以执行 `db.COLLECTION_NAME.insertOne({"key":"value"})`。这里有一个示例：

```javascript
db.users.insertOne({'name':'Bob'})
{
  "acknowledged" : true,
  "insertedId" : ObjectId("5a52c53b223039ee9c2daaec")
}
```

MongoDB 会自动创建一个新的 `users` 集合并插入一个带有键值对 `'name':'Bob'` 的文档。返回的 `ObjectId` 是所插入文档的 id。MongoDB 在创建每个文档时都会创建一个唯一的 `ObjectId`，并成为 `_id` 字段的默认值：

```bash
show dbs
exampledb 0.078GB
local 0.078GB
prototype 0.078GB
test 0.078GB
```

同样，你可以使用 `show collections` 命令确认集合是否已创建：

```bash
show collections
users
```

我们已经创建了一个数据库，添加了一个名为 `users` 的集合并向其中插入了一个文档。现在让我们尝试删除它。要删除现有数据库，请使用如下所示的 `dropDatabase()` 命令：

```javascript
db.dropDatabase()
{ "ok" : 1 }
```

`show dbs` 确认数据库确实已被删除：

```bash
show dbs
local 0.078GB
prototype 0.078GB
test 0.078GB
```

有关更多数据库操作，请参阅 MongoDB 关于数据库命令（Database Commands）的参考页面。

# MongoDB CRUD 操作

你可能已经知道，CRUD 缩写代表创建（Create）、读取（Read）、更新（Update）和删除（Delete）。这些是在构建应用程序时无法避免的四个基本数据库操作。例如，任何现代应用程序都将创建新用户、读取用户数据、更新用户信息并在必要时删除用户账户的能力。让我们使用 MongoDB 在数据库级别完成这些操作。

## 创建操作 (CREATE OPERATION)

创建等同于向集合中插入文档。在上一节中，我们使用 `db.collection.insertOne()` 语法插入了单个文档。还有另一种方法 `db.collection.insertMany()` 方法，它可以让你一次性插入多个文档。语法如下：

```javascript
db.COLLECTION_NAME.insertMany(
  [ <document 1>, <document 2>, ... ]
)
```

让我们创建一个 `users` 集合并填充一些实际用户：

```javascript
db.users.insertMany([
  { "name": "Tom","age":33, "email": "tom@example.com" },
  { "name":"Bob", "age":35, "email":"bob@example.com" },
  { "name":"Kate", "age": 27, "email": "kate@example.com" },
  { "name":"Watson", "age":15, "email": "watson@example.com"}
])
{
  "acknowledged" : true,
  "insertedIds" : [
    ObjectId("5a52c53b223039ee9c2da5"),
    ObjectId("5a52c53b223039ee9c2da6"),
    ObjectId("5a52c53b223039ee9c2da7")
  ]
}
```

`insertMany` 方法接受一个对象数组，返回的是一个 `ObjectId` 数组。

## 读取操作 (READ OPERATION)

读取操作用于从集合中检索一个或多个文档。读取操作的语法如下：

```javascript
db.collection.find(query, projection)
```

要检索所有用户文档，你可以这样操作：

```
db.users.find().pretty()
```

```json
{
  "_id" : ObjectId("5a52cb2451dd8b08d5a22cf5"),
  "name" : "Tom",
  "age" : 33,
  "email" : "tom@example.com"
}
{
  "_id" : ObjectId("5a52cb2451dd8b08d5a22cf6"),
  "name" : "Bob",
  "age" : 35,
  "email" : "bob@example.com"
}
{
  "_id" : ObjectId("5a52cb2451dd8b08d5a22cf7"),
  "name" : "Kate",
  "age" : 27,
  "email" : "kate@example.com"
}
{
  "_id" : ObjectId("5a52cb2451dd8b08d5a22cf8"),
  "name" : "Watson",
  "age" : 15,
  "email" : "watson@example.com"
}
```

这对应于 SQL 数据库中的 `SELECT * FROM USERS` 查询。

`pretty` 方法是一个游标方法，还有许多其他方法。你可以链用这些方法来修改你的查询以及查询返回的文档。

如果你需要过滤查询并返回集合的子集怎么办？例如，查找所有年龄小于 30 岁的用户。你可以这样修改查询：

```
db.users.find({ "age": { $lt: 30 } })
```

```json
{ "_id" : ObjectId("5a52cb2451dd8b08d5a22cf7"), "name" : "Kate", "age" : 27, "email" : "kate@example.com" }
{ "_id" : ObjectId("5a52cb2451dd8b08d5a22cf8"), "name" : "Watson", "age" : 15, "email" : "watson@example.com" }
```

`$lt` 是一个查询过滤器运算符，用于选择 `age` 字段值小于 30 的文档。有很多比较和逻辑查询过滤器可用，你可以在查询选择器（Query Selector）文档中查看完整列表。

## 更新操作

更新操作修改集合中的文档。与创建操作类似，MongoDB 提供了两种更新文档的方法。它们是：

1. `db.collection.updateOne(filter, update, options)`
2. `db.collection.updateMany(filter, update, options)`

如果你需要向集合中的文档添加一个额外的字段，例如 `registration`，你可以：

```javascript
db.collection.updateMany({ "age": { $lt: 30 } }, { $set: { "registration": "active" } })
```

## 删除操作

删除操作从集合中移除文档。与更新操作类似，MongoDB 提供了两种删除文档的方法。它们是：

1. `db.collection.deleteOne(filter)`
2. `db.collection.deleteMany(filter)`

如果你需要删除匹配条件的单个文档，你可以使用：

```
db.users.deleteOne({ "name": "Tom" })
```

如果你需要删除匹配条件的所有文档，你可以使用：

```
db.users.deleteMany({ "age": { $lt: 30 } })
```

## 驱动概览

为了让应用程序与服务器通信，你需要使用驱动。MongoDB 有官方和第三方驱动可以与数据库交互。

### Node.js 驱动

这是 Node.js 的官方驱动。该驱动可以使用 Promise 或回调与数据库交互。下面的示例演示了连接服务器：

```javascript
const { MongoClient } = require('mongodb');
const assert = require('assert');

// 连接 URL
const url = 'mongodb://localhost:27017/exampledb';
// 数据库名称
const dbName = 'exampledb';

(async function() {
  let client;
  try {
    // 尝试连接服务器
    client = await MongoClient.connect(url);
    console.log("成功连接到服务器.");
    const db = client.db(dbName);
  } catch (err) {
    // 将错误打印到控制台
    console.log(err.stack);
  }

  if (client) {
    client.close();
  }
})();
```

### Mongoose 驱动

另一个流行的 MongoDB 驱动是 Mongoose。它是构建在官方驱动之上的。当 Mongoose 发布时，它拥有许多原生驱动不具备的功能。一个显著的功能是可以定义映射到数据库集合的模式（schema）。

然而，MongoDB 的最新版本已以 JSON schema 和模式验证的形式吸收了这些功能。

除了模式之外，Mongoose 的其他功能还包括模型、验证器和中间件、populate 方法、插件等。你可以在 Mongoose 文档中了解更多这些内容。这里有一个使用 `mongoose.connect()` 连接数据库的示例：

```javascript
var mongoose = require('mongoose');

// 连接 URL
const url = 'mongodb://localhost:27017/exampledb';

mongoose.connect(url);

var db = mongoose.connection;

db.on('error', console.error.bind(console, 'connection error:'));

db.once('open', function() {
  // 我们已经连接上了！
});
```

## 结论

MongoDB 是一种流行的 NoSQL 数据库解决方案，适用于现代开发需求。在本教程中，我们涵盖了 MongoDB 的基础知识、Mongo Shell 以及一些流行的驱动。我们还探索了 Mongo Shell 中常见的数据库操作和 CRUD 操作。现在是你去尝试这里涵盖的内容以及更多内容的时候了。如果你想学习更多，我建议使用 MongoDB 和 Node 创建一个 REST API，以熟悉常见的数据库操作和方法。

# 第一章

# 第二章

# 第三章

# 第四章

# 第五章

# 第六章

# 第七章

# 第八章
