# Javascript 行业实战







![](img/d077270db200bfe2e16ba5ef3a76c09d_0_0.png)


## 引言 4

## 函数式风格 5
- 命令式 vs. 声明式 5
- 数组操作 10
- 避免使用类 18
- 在并非必要时避免操作实例 19
- React 中的类与 Hooks 23
- 创建你自己的抽象 25

## 控制流 28
- 卫语句 (Guard clauses) 28
- 跳过 ‘else’ 部分 31
- 使用 switch 语句 35
- 使用函数和偏函数应用 36

## 代码整洁与良好实践 42
- 以对象传递参数 42
- 以元组返回关联数据 46
- 不要扩展内置对象 47
- 避免默认导出 48
- 可发现性较差 49
- 使用 CommonJS 时的困扰 49
- 使用动态导入时的困扰 49
- 命名保护 49
- 重新导出 49
- 放弃单字母变量名 50
- 箭头函数 vs. 函数声明 51

## TypeScript 52
- 不要过度使用 52
- 让 TypeScript 推断类型 54
- 避免使用 any 56

## React 57
- 使用 React hooks 57
- 无需担心 JSX 中的箭头函数 57
- 不要从内部函数返回 JSX 59
- JSX 内部的三元运算符 60
- 拆分为独立的组件 60
- 不要将异步 IIFE 中封装 useEffect 61
- 不要过度使用内置的 Memo 62
- 停止使用 useMemo 62
- 停止过度使用 useCallback 64

## NodeJS & AWS Lambda 65
- 使用 promises 代替回调 65
- 使用 promisify 66
- 使用 module/promises 67
- AWS Lambda 中的异步处理程序 67

## 结语 69
- 我应该使用哪些规范？ 69

## 额外资源 70

## 引言

当 JavaScript 统治行业时，我一直处于近距离观察的前排。

在担任自由职业顾问的过去十年里，我有幸与许多不同的团队合作过。我参与了无数次 PR 代码审查，并就 JavaScript、最佳实践、整洁代码、模式和编码风格进行过许多激烈讨论。

我曾在各种演讲和工作坊中教授过 JavaScript、React 和 NodeJS。此外，在过去的一年里，我经常向 Twitter 读者展示小段代码，询问他们更倾向于哪种写法以及是否会在 PR 中批准它们。

以下是我的发现、感悟和个人经验。
它们被整合在一本易于阅读的电子书中，包含了示例和解释。

**这本书是有主观的。**

对于书中的每一个示例，你都会找到持有不同意见的行业开发者。本书介绍的是行业偏好和标准。但从定义上来说，它是主观的。

**这并不是一本 JavaScript 基础书籍。**

请注意，本书假设你对 JavaScript 语言有基础理解。

## 函数式风格

JavaScript 是一种多范式编程语言。
这意味着语言支持以不同的风格进行编程，包括面向对象、过程化、原型和函数式。

到目前为止，你最常见的风格是面向对象和函数式。
尽管像 Java 和 C# 这样的面向对象语言对行业产生了巨大影响，但在 2021 年，函数式风格 JavaScript 最受欢迎且最受接受。这是你应该追求的方向。

## 命令式 vs. 声明式

面向对象编程遵循命令式范式。
函数式编程遵循声明式范式。

让我们来看看区别。

命令式编程侧重于你想要如何完成某事。
你一步步改变程序的状态。

声明式编程侧重于结果是什么。
只要获取结果的过程不会改变程序的状态，如何获取结果就不那么重要。

当一个函数以确定的方式执行任务且不改变其环境（改变周围的状态）时，我们称之为“纯函数”。
假设我们要遍历一个列表并将所有元素乘以 2。

命令式风格看起来像这样：

```javascript
function multiplyAll(list) {
  for (let i = 0; i < list.length; i++) {
    list[i] *= 2;
  }
}

const numbers = [1, 2, 3, 4, 5];
multiplyAll(numbers);
console.log(numbers);
// [2, 4, 6, 8, 10]
```

声明式风格看起来像这样：

```javascript
const numbers = [1, 2, 3, 4, 5];
const multipliedNumbers = numbers.map(n => n * 2);

console.log(multipliedNumbers);
// [2, 4, 6, 8, 10]
```





这里有两个你脑海中应该浮现的警示信号。

- 1. 你在循环体外部声明了一个数组。
- 2. 你正在使用 `push` 方法来填充数组。

根据经验法则：每当你准备调用 `push` 方法时，问问自己是否可以使用声明式的方式来表达。
`push` 方法正在修改原数组。

让我们来重构它。

```javascript
const activeMembers = ["alex", "stephanie"];
const candidates = ["alex", "martin", "anna"];

const activeCandidates = candidates.filter(
  (candidate) => activeMembers.includes(candidate)
);

console.log(activeCandidates);
// ["alex"]
```

啊，好多得多！
周围的状态没有发生改变。没有任何数据被修改。
`activeCandidates` 被声明并直接赋值了 `filter` 的结果，这已经为我们完成了工作。

让我们再看另一个例子。
在这里，我们想要遍历一个数字列表并找到总和。
下面是用命令式操作的示例。

```javascript
const points = [3, 9, 7, 8, 5, 2, 11, 14];
let totalPoints = 0;

for (const point of points) {
  totalPoints += point;
}

console.log(totalPoints);
// 59
```

这里有两个你脑海中应该浮现的警示信号。

- 1. 你在循环体外部声明了一个变量。
- 2. 你正在使用 `let` 关键字来初始化变量。

根据经验法则：每当你发现自己在使用 `let` 关键字时，问问自己是否可以在不重新赋值变量的情况下实现所需的结果。
在大多数情况下，你不想使用 `let`。你希望使用 `const` 立即初始化并赋值变量。

让我们来重构它。

```javascript
const points = [3, 9, 7, 8, 5, 2, 11, 14];
const totalPoints = points.reduce((total, point) => total + point);
console.log(totalPoints);
// 59
```

完美！

一行代码。周围的状态没有被改变。没有变量被重新赋值。

我有时听到有人提出这种观点：

> “`Reduce` 很难理解。如果你的团队中有初级开发者，你可能倾向于使用命令式方法”。

我个人完全不同意。
这取决于它的用法——当 `reduce` 保持简单时（如上面的示例），它完全在大多数初级开发者的理解能力范围内。

这通常是中级和高级开发人员的糟糕借口，他们还没有适应这种编写代码的方式，但缺乏明确的论据来解释为什么他们坚持旧的命令式写法。
让我们再看另一个例子。排序！

这个变得有点复杂。
看看下面的代码。

```javascript
const grades = ["C", "A", "I", "B", "F"];
const sortedGrades = grades.sort();
console.log(grades); // ["A", "B", "C", "F", "I"]
```

乍看之下，这看起来很好。我们没有使用 `let`，也没有使用类似 `push` 的方法修改原数组。我们使用了一个**声明式**返回所需结果的数组方法。

但看看 `console.log` 语句。
是的。JavaScript 可以变得糟糕到这样。事实证明 `sort` 方法非常老旧，而且它**没有**创建原数组的副本。
相反，它**修改**了原数组，并在方法调用时返回它自身的数组。

奇怪吗？是的。
但有很多旧的数组方法都是这样。
小心使用 `push`、`shift`、`unshift`、`pop`、`reverse`、`splice`、`sort` 和 `fill`。
幸运的是，正如我们在之前的示例看到的，通常我们可以直接这些这些方法来避免麻烦。

然而，在某些情况下（例如使用 `sort`），在缺乏更好选择的情况下，我们必须使用修改原数组的方法。

数组解构救了急！

每当这些情况发生时，确保在对数组执行操作之前先手动复制一份。

操作非常简单：

```javascript
const grades = ["C", "A", "I", "B", "F"];
const sortedGrades = [...grades].sort();

console.log(grades);
// ["C", "A", "I", "B", "F"]

console.log(sortedGrades);
// ["A", "B", "C", "F", "I"]
```

这个 `[...grades]` 产生了本质的区别。

把这个习惯变成肌肉记忆。

让我们看一个使用异步操作的例子。包含异步行为的迭代操作使用声明式风格可能有点棘。

假设我们有一个名称列表。对于每个名称，我们都想调用 API 获取一些信息，然后保留一个包含这些信息的新列表。

典型的命令式方法可能如下：

```javascript
const names = ['jack', 'annie', 'peter'];

async function getInformationFromName(name) {
  const request = await fetch('https://some.api?name=' + name);
  const result = await request.json();
  return result;
}

const namesWithInformation = [];

for (const name of names) {
  const information = await getInformationFromName(name);
  namesWithInformation.push(information);
}
```



现在，当在代码审查中指出这一点时，大多数程序员都能理解。一种常见的反应是：让我们把方法改为静态的（static）吧。这样就不再需要创建实例了。

```javascript
class NameBuilder {
  static capitalize(name) {
    return name
    .split(' ')
    .map(s => s.charAt(0).toUpperCase() + s.substring(1))
    .join(' ');
  }

  static createGreeting(name) {
    return `Hello, ${name}`;
  }
}
```

```javascript
const capitalized = NameBuilder.capitalize('simon hoiberg');
const greeting = NameBuilder.createGreeting(capitalized);

console.log(greeting);
// Hello, Simon Hoiberg
```

棒了！这绝对是一个改进。

我们消除了实例变量，因此不再有数据变异。我们还拥有了根据参数确定性地返回值的方法。它们是纯函数。

但是，既然我们已经如此接近了——为什么我们不直接完全删掉类呢？
看起来真的完全不再需要它了。

```javascript
export function capitalize(name) {
  return name
    .split("")
    .map(s => s.charAt(0).toUpperCase() + s.substring(1))
    .join("");
}

export function createGreeting(name) {
  return `Hello, ${name}`;
}
```

```javascript
import { capitalize, createGreeting } from "./namebuilder";

const capitalized = capitalize("simon hoiberg");
const greeting = createGreeting(capitalized);

console.log(greeting);
// Hello, Simon Hoiberg
```

太棒了！我们做到了——我们完全删除了类！
现在，代码是声明式的，更容易测试，更容易调试，并且支持摇树优化（tree-shakable）。这意味着像 Webpack 和 Rollup 等现代构建工具能够移除在特定情况下可能永远不会使用的死代码函数。这将导致小代码包体积。

# React 中的类与 Hooks

2018 年，React 引入了 hooks。

它们这样做是为了消除类和令人困惑的 `this` 关键字。

为什么？因为 React 本质上是一个声明式的 UI 库，而类并不真的契合。

如果你在 2018 年之前使用 React，我打赌你写过很多类似这样的代码。

```javascript
import React from "react";

export class ShowCount extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  componentDidMount() {
    this.setState({ count: this.props.count });
  }

  render() {
    return (
      <div>
        <p> Count: {this.state.count}</p>
      </div>
    );
  }
}
```

幸运的是，在 hooks 引入之后，我们现在可以从在 React 中编写整洁且声明式的代码中受益。

```javascript
import React, { useEffect, useState } from "react";

export function ShowCount(props) {
  const [count, setCount] = useState();

  useEffect(() => {
    setCount(props.count);
  }, [props.count]);

  return (
    <div>
      <p> Count: {count}</p>
    </div>
  );
}
```

函数组件在 hooks 之前就已经存在了，但当逻辑增长时，我们经常需要将其重构为类组件。

通过这种方式，我们再也不需要担心了。
我们再也不需要担心 `this`、方法绑定、无法共享逻辑以及许多其他问题。

我将在本书的后续部分介绍更多 React 最佳实践。

# 创建你自己的抽象

所以，我们已经涵盖了一些可以遵循的黄金准则。
但很多时候，我们在软件中编写的代码比我们在这里看到的示例要复杂得多。

在某些情况下，编写声明式、避免使用 `let` 关键字、不重新赋值变量、不修改循环周围作用域内的数据等做法，仅仅会产生冗长、啰嗦且难以阅读的代码。

显然，我们不想强行推行某种风格或模式以至于让我们的代码变得更糟，“仅仅是因为……函数式编程”。

但是，我们并不是把一切都倒转过来，而是可以将这些代码抽象到一个函数中，然后……（等待，提供的 OCR 文本从第 24 页开始变得严重损坏/乱码。我将处理可读部分并尽可能保持结构）。

*注：提供的从 24 页到 30 页的 OCR 文本包含大量的字符损坏和无意义的字符串。我已经清理了可读的句子，并根据可见模式保持了结构。*




# 跳过 'else' 部分

if-else 语句。这是我们开始学习编程时首先学到的内容之一。

现在，让我们通过“忘记”如何使用 `else` 来继续学习。

总的来说，如果你的函数包含了 `else`，这说明你的函数正在同时做多件事。

它违反了众所周知的**单一职责原则**（Single Responsibility Principle），并且经常导致容易出错的分支逻辑，在大规模代码中变得难以理解。

所以，作为一个经验法则，每当你准备写 `else` 时，请停下来重新考虑你正在做的事情，并寻找表达该逻辑的替代方法。

让我们来看几种避免使用 `else` 的方法。

其中一种是守卫语句（guard clauses），这是我们上面刚刚讨论过的。

另一种方法是使用默认值。

让我们来看一个例子。

假设我们有一个函数 `negateOdd`，它接收一个数字，如果该数字是奇数，则对其取反。

```javascript
function negateOdd(n) {
  let result;

  if (n % 2 === 0) {
    result = n;
  } else {
    result = n * -1;
  }

  return result;
}
```

这个函数完成了它应该做。但它没必要使用 `else`。让我们重构它，改用一个默认值。

```javascript
function negateOdd(n) {
  let result = n;

  if (n % 2 === 0) {
    result = n * -1;
  }

  return result;
}
```

已经变许多了！我们现在给 `result` 赋值了一个默认值，只有当满足 `if` 语句中的条件时，变量才会被改变。

现在，我们还将将函数的特殊情况封装在 `if` 中。
你可能会认为，以后阅读这个函数时，这可能有助于我们快速定位逻辑的核心部分。

但让我们做得更好。从上一章我们知道，我们应该质疑对 `let` 和命令式代码的使用。
看看是否能让这个函数变得更加可读且精简。

```javascript
function negateodd(n) {
  if (n % 2 === 0) {
    return n;
  }

  return n * -1;
}
```

搞定！完全没有变量赋值。仅根据给定的条件返回不同的值。

注意我们是如何将逻辑的核心部分移动到函数体末尾的。许多开发者倾向于将函数的关键任务放在函数体的末尾——就像我们之前对守卫语句所做。

有一种被广泛接受的 `if-else` 版本。
那就是三元运算符。

```javascript
function negateOdd(n) {
  return n % 2 === 0 ? n : n * -1;
}
```

三元运算符本质上就是 `if-else`。

那么，既然我们应该避免使用 `else`，为什么它又是被接受的呢？
因为它被用于直接赋值或返回一个值。它没有函数体，没有编写多行逻辑的入口。

这也是为什么三元运算符应该限制为这种用法。
我见过开发者滥用三元运算符，以非常有创意且神秘的方式进行控制流分支，包括使用嵌套的三元运算符，这在绝大多数专业团队中被认为是“脏代码”，应该被严格避免。

你可能会认为上述使用三元运算符的解决方案有多易读和整洁，但在大多数情况下，这样的函数能够可以通过代码审查。

# 使用 switch 语句

你可能不需要频繁使用它，但在某些情况下，`switch` 语句是有意义的。

```javascript
function pointsFromGrade(grade) {
  switch (grade) {
    case "A":
      return 10;
    case "B":
      return 8;
    case "C":
      return 5;
    case "I":
      return 3;
    case "F":
      return -1;
    default:
      return NaN;
  }
}
```

如果你正准备编写一系列 `if-else-if-else`……你可能想考虑使用 `switch` 语句来代替。

某些库（例如 Redux 或 React）根据惯例将 `switch` 语句作为其 reducer 的一部分。

然而，对于这种情况，你可以使用一个对象来存储这些值。
如果值需要逻辑，你可以在对象中存储函数，并在对象查找后调用它。

```javascript
const pointsFromGrade = {
  A: 10,
  B: 8,
  C: 5,
  I: 3,
  F: -1
};

const p = pointsFromGrade("B");
```

# 使用函数和部分应用

如果你发现自己过度使用改变控制流的语句和运算符，这通常意味着你的代码承担了太多职责。你会得到所谓的“面条代码”（spaghetti code）。

看看这个虚构的例子。你认出它吗？我打赌你写的这种次数比不写的多。

```javascript
if (someCondition) {
  const toBeUpdated = [];
  for (let i = 0; i < someArray.length; i++) {
    const hasChanged = didChange(someArray[i]);
    if (!hasChanged) {
      toBeUpdated.push(someArray[i]);
    }
  }
  if (!toBeUpdated) {
    // ...
  }
}
```
*(注：原文提供的示例代码不完整，此处根据上下文翻译/保留逻辑)*

由于原文提供的代码块在示例处截断，此处保持逻辑结构。

*(注：由于原文文本在某些部分存在大量重复和逻辑断层，译文已根据指令要求尽量翻译并保持格式。)*





# 代码整洁与良好实践

我们已经涵盖了编程的两个基础领域，以及行业中最常接受的风格和偏好。

在本章中，我将提供一些许多专业团队认为的 JavaScript 良好代码整洁示例，这些示例并不限于特定的编程领域或概念。

让我们从上一节看到过的一个示例开始。

### 以对象形式传递参数

假设我们有一个函数 `createUser`，它需要四个参数来创建一个用户（通过调用某些 API）。

```javascript
function createUser(username, date, isAdmin, isMod) {
  return fetch('https://some.api', {
    method: 'POST',
    body: JSON.stringify({
      username, date, isAdmin, isMod
    })
  });
}
```

看函数签名本身，这些事情看起来挺通顺的。

当我们调用它时呢？

```javascript
createUser('Simon', '2021-01-01', false, true);
```

这些参数的含义非常不清楚，对吧？
尤其是最后两个布尔值。我必须去查看实现代码才能确认。

相反，我们可以将参数封装在一个对象中。

```javascript
function createUser({ username, date, isAdmin, isMod }) {
  return fetch('https://some.api', {
    method: 'POST',
    body: JSON.stringify({
      username, date, isAdmin, isMod
    })
  });
}
```

得益于 ES6 的对象解构，我们可以通过简单在参数周围加上大括号来轻松实现。

现在，每当我们调用 `createUser` 时，我们都传递一个对象作为单个参数，并将所需的值作为属性传递。

```javascript
createUser({
  username: 'Simon',
  date: '2021-01-01',
  isAdmin: false,
  isMod: true,
});
```

看看现在读起来有多顺畅。我们不再疑惑那些布尔值的含义了。

- 此外，这种方法还让我们带来了一些额外的益处：
- 更容易处理可选属性
- 我们不再依赖参数的顺序

根据我的行业经验，当你的函数需要超过 1-2 个参数时，这是一个非常流行的方法。

我经常看到这种方法的另一个版本：将可选参数作为配置对象传递。这被 NodeJS 以及一系列著名的开源库所采用。

其想法是传递 1-2 个核心参数，然后将剩余参数作为配置对象传递。

```javascript
function createUser(username, date, options) {
  return fetch('https://some.api', {
    method: 'POST',
    body: JSON.stringify({
    username,
    date,
    isAdmin: options ? !!options.isAdmin : false,
    isMod: options ? !!options.isMod : false
    })
  });
}
```

现在，我们需要在访问值之前检查配置对象是否已设置，并提供适当的回退值。

另一方面，现在调用 `createUser` 函数看起来非常干净。

```javascript
createUser('Simon', '2021-01-01', {
  isMod: true,
});
```

前两个参数显而易见，我们现在可以根据需要可选地提供选项。

### 以元组返回关联数据

在 JavaScript 中，我们可以从函数返回单个值。
但通常，我们需要返回多个关联在一起的值。

一种常见的方法是返回一个包含这些值的元组（tuple）。
简而言之，元组是元素的有序列表。

假设我们有一个函数 `getElementPosition`，它根据 id 获取 DOM 元素的位置。
在这种情况下，x 和 y 是关联值。因此，将它们都作为元组返回是完全合逻辑的。

```javascript
function getElementPosition(elementID) {
  const element = document.getElementById(elementID);

  if (!element) {
    return [NaN, NaN];
  }

  const rect = element.getBoundingClientRect();
  return [rect.x, rect.y];
}

const [x, y] = getElementPosition('my-element');
console.log(x, y);
// 278.5, 122.3
```

### 不要扩展内置对象

当你第一次理解 JavaScript 的原型链并理解了你如何扩展原型（包括 JavaScript 内置对象）时，你可能会体验到一种拥有超能力的感觉。

现在，你可以扩展 Array 原型，将你自定义的数组方法与 map、filter 和 reduce 包含在一起。
这意味着 - 这难道不很酷吗？

```javascript
Array.prototype.average = function () {
  return this.reduce((acc, elem) => acc + elem / this.length);
}

const list = [1, 2, 3];
const avg = list.average();

console.log(avg);
// 2
```

并不是这样的！事实上，这有严重的问题，并可能导致一系列相当严重的问题。应该尽一切避免扩展内置对象。

事实上，有过整个应用程序因为这种模式而瘫痪的恐怖故事。

不幸的是，过去某些第三方库有这样做的坏习惯，你可能会无意中覆盖它，导致一堆麻烦！

相反，保持事物的分离和纯洁！
构建你自己的工具包，并将其保持在自己的模块中。

```javascript
export function average(list) {
  return list.reduce((acc, elem) => acc + elem / list.length);
}
```

```javascript
import { average } from "./array-utils";

const list = [1, 2, 3];
const avg = average(list);
console.log(avg);
// 2
```

好得多！
随着这个集合的增长，很容易将其提取为 NPM 包，以便在不同项目之间复用。

### 避免默认导出

这引出了下一点。
正如你可能注意到的，我在任何示例中都没有用过 `export default`。
这是故意为。

如果你在使用 TypeScript，这一点尤为重要，但我强烈建议完全放弃使用默认导出的习惯。

为什么？

### 可发现性较差

这使得 VSCode 和 Webstorm 等现代代码编辑器中的 IntelliSense 很难在你开始输入时建议来自某个模块的导出内容。

### 使用 CommonJS 时很烦人

我不知道你是否曾经必须在 `require` 语句末尾加上 `.default`？非常烦人又难看，不是吗？

### 使用动态导入时很烦人

与 CommonJS 和 require 类似，使用动态导入也强制你使用 .default。

### 命名保护

当你从默认导出导入时，你可以为导入内容命名任何名称。

### 重新导出

在创建 NPM 包或处理大型代码库时，使用桶（barrels）从集中位置重新导出模块是很常见的。默认导出迫使你重命名导出，这再次可能导致不一致。

使用具名导出（named exports）代替默认导出（default exports）并没有任何权衡，因此我建议简单地坚持这样做。

### 放弃单字母变量名

我见过很多这种情况。单字母变量名，特别是在回调中。
短小简洁的代码并不总是理想的。
看看这段代码。

```javascript
const images = users.filter((u) => {
  return u.entities.find((e = e.type === 'profile-image'));
});
```

u 和 e？谢了，清晰性和可读性才是理想的。
即使多花几行。

```javascript
const images = users.filter((user) => {
  return user.entities.find(
    (entity = entity.type === 'profile-image')
  );
});
```

在少数地方，单字母变量名是惯例接受的。例如，在 for 循环中使用变量 `i`。
除此之外，养成为回调参数命名的良好习惯。
通常，你想使用列表单词单数形式。
就像我这里使用的 users 和 user。

### 箭头函数 vs 函数声明

你可能注意到我在示例中使用了 `function` 关键字，而不是使用 `const` 定义箭头函数表达式。

我在这里提到它，尽管我无法就这个问题给你一个明确的方向。

在我的行业经验中，这完全取决于个人偏好。

```javascript
export function average(list) {
  // implementation
}
export const average = (list) => {
  // implementation
}
```





# TypeScript

TypeScript 是一种用于应用级 JavaScript 开发的语言。
它是 JavaScript 的带类型超集，用于在与 JavaScript 工作时添加静态类型并描述对象的形状。

在构建构建复杂的 Web、移动端和桌面应用的专业软件团队中，TypeScript 是一个非常受欢迎的选择。

然而，在我合作过的团队中，绝非所有团队都对它感到同样兴奋。
事实上，有些团队甚至非常讨厌它。

在本章中，我将尝试描述一个让资深 JavaScript 开发者和 TypeScript 爱好者者似乎都认同的“平衡点”，并描述我在行业中看到的一些“该做”和“不该做”。

## 不要过度使用

如果你正在与一个经验丰富的 JavaScript 开发者团队工作，他们可能很欣赏松散类型 JavaScript 提供的某些灵活性，那么如果你试图完全引入（甚至强制）充分使用 TypeScript，你将会遇到很多阻力。

因此，根据我在行业中使用 TypeScript 的经验，这一点非常明确：不要过度使用！

如果你对 TypeScript 充满热情，那是很好的。它是一门很棒的语言。但有很多开发者想看到这样的代码。

```typescript
type RequireOnly<T, Keys extends keyof T = keyof T> =
  Pick<T, Exclude<keyof T, Keys>> &
  { [K in Keys]?: Required<Pick<T, K>> }
  & Partial<Record<Exclude<Keys, K>, undefined>>;;
```

（示例代码来自我工作过的实际项目）

根据我的观察，TypeScript 最有效的用法实际上归结为以下几：

- 使用接口描述对象的形状
- 为函数的参数和返回值编写类型
- 使用泛型使用更通用的函数签名
- 使用 TypeScript 用类型进行更灵活的类型描述

特别是，使用接口描述 API 的 JSON 响应非常流行。IntelliSense 极大地提高了生产力，而且通过 GraphQL 等现代解决方案，你可以根据 schema 自动生成这些接口的工具。

TypeScript 中这部分不烦人且仅仅节省时间的功能似乎非常受欢迎。

## 让 TypeScript 推断类型

我从新转 TypeScript 的人员那里注意到，他们倾向于坚持为*所有内容*编写类型。

所有函数必须有返回类型，所有参数*必须*有类型，所有变量声明*必须*紧跟其类型，等等。

对于那些可能还没有沉浸在 TypeScript 喜悦中的团队其他成员来说，这部分会感到非常繁琐和官僚化。

更重要的是：没有必要。

TypeScript **非常擅长**推断类型本身。你不需要显式地写出每一个的类型。

```typescript
function addOne(n: number = 0): number {
  return n + 1;
}
```

```typescript
function addOne(n = 0) {
  return n + 1;
}
```

你可以随时将鼠标悬停在参数或函数上，查看 TypeScript 是否会自动（正确地）推断类型。

```typescript
const name: string = 'simon';
```

你对变量也可以这样做。如果你将鼠标悬停在最后一个例子中的 `name` 变量上，你会发现 TypeScript 是通过赋值推断出来的。不需要手动写。

```typescript
const name = 'simon';
```

```typescript
const [name, setName] = useState<string>('simon');
```

```typescript
const [name, setName] = useState('simon');
```

在 React 中，`useState` 钩子也足够智能，可以让 TypeScript 根据默认值推断类型。不需要手动写。

## 避免使用 any

从一个极端走向另一个极端：我也目证了不少团队因为炒作而转向 TypeScript。

但并没有正确地使用它，主要是因为到处写 `any`。

```typescript
function addOne(n: any): any {
  if (typeof n === 'number') {
    return n + 1;
  }
  return !!n;
}
```

显然，TypeScript 在这里没有产生任何价值。

我完全理解——如果你是 TypeScript 新手，某些晦涩的编译错误可能会让你困惑并觉得拖慢了你的速度。但如果你忙到没有时间学习 TypeScript的基础，我强烈建议不要使用 TypeScript。在这种情况下，坚持使用 JavaScript。

如果你到处强制松散类型，那么使用强类型语言就没有意义。

避免使用 `any`。或者完全不要使用 TypeScript。

# React

React 是一个巨大的课题，有很多观点。
事实上，React 是我在不同团队中遇到最多争议领域之一。

在本章中，我将涉及我看到的一些常见讨论，并对大多数团队喜欢的 React 代码提供我的总体印象。

## 使用 React hooks

这一点我简单来说。如果你还在纠结于编写类组件（class components），请立即改这个习惯。

我的明确印象是，到为止大多数团队现在已经有效地转向使用 React Hooks，除非你正在处理带有类组件的遗留项目，否则你可以放心地你加入的下一个团队将使用 React hooks。

## 不要担心 JSX 中的箭头函数

（注：此节的 OCR 文本包含一段干扰正文的社交媒体线程噪音。根据书籍上下文，核心信息是关于箭头函数在 JSX 中的性能。）

我见过很多这种模式，并参与过几次对此的讨论。

然而，我发现大多数团队不喜欢这样做。如果你准备在组件中声明一个内部函数（可能带有 render 前缀）来渲染 JSX，你应该重新考虑一下。




这是在 React 中实现此操作最“正确”的方法。
它的代价是必须将 `username` 和 `isLoading` 属性向下传递一层，如果需要回调函数，这些函数也必须一起传递。

## 不要将 useEffect 封装在异步 IIFE 中

我见过这种模式，但它绝不是一种非常受欢迎的解决方案。

你可能认得出这个用例。你需要在 `useEffect` 中执行某些异步操作，但你无法使用 `await` 关键字。

```javascript
export function App() {
  useEffect(() => {
    (async () => {
      await fetch("https://some.api");
    })();
  }, []);

  return <div className="App"></div>;
}
```

有些人会认为，从根本上来说在 `useEffect` 中执行异步操作就应该谨慎。

在任何情况下，这都不优雅！

如果你需要这样做，要么在 `useEffect` 内部声明函数并立即调用它，或者——更好的做法——在组件作用范围内声明它。

```javascript
export function App() {
  const callSomeApi = async () => {
    await fetch("https://some.api");
  }

  useEffect(() => {
    callSomeApi();
  }, []);

  return <div className="App"></div>;
}
```

这好得多！很可能随着逻辑的增长，我们以后某个时候还是得这样做。我们不如现在就这样做，并保持代码整洁。

## 不要过度使用内置 hooks

是的，hooks 超级酷！当你学会了如何使用它们时，你可能会产生把它们安放在处处的冲动。
请不要这样做。

## 停止使用 useMemo

我遇到过很多这种情况。对在组件中直接从函数调用赋值给变量的恐惧，导致开发者使用 `useMemo`。

让我们来看一个例子。

```javascript
export function App({ username, type }) {
  const computedValue = useMemo(() => {
    return getComputedValue(username, type);
  }, [page, type])

  return <HeavyComponent computedValue={computedValue} />
}
```

很容易看出开发者的逻辑是怎样的。

`HeavyComponent` 不应该进行不必要的重新渲染，所以 `computedValue` 被缓存了（memoized）。

`useMemo` hook 的目的是防止在每次组件重新渲染时都执行大量的计算，所以我们在这里问的第一个问题是：`getComputedValue` 实际上是一项耗时的操作吗？

在大多数情况下，它不是。

而且，让 React 管理一个缓存值的成本实际上超过了通过使用 `useMemo` 带来的性能收益。

相反，不要害怕从组件根直接调用 `getComputedValue`。

```javascript
export function App({ username, type }) {
  const computedValue = getComputedValue(username, type);

  return <HeavyComponent computedValue={computedValue} />
}
```

如果 `computedValue` 解析为原始类型（字符串、数字、布尔值等），
你也不需要担心 `HeavyComponent` 重新渲染了。
如果值没有变化，它就不会重新渲染。

## 停止过度使用 useCallback

同样，我也见过 `useCallback` hook 被过度使用的情况。
它主要归结为两种情况：

要么使用 `useCallback` 来设置初始状态，同时防止无限渲染循环。但情况下，`useEffect` 才是适合这项工作的 hook。

或者，是认为结果会被缓存。
在这种情况下，`useMemo` 才是适合这项工作的 hook，但很可能，你只是想在组件本身中计算你需要的任何内容。

事实上，不当使用 `useCallback` 反会降低性能。
如果你对何时使用 `useCallback` 有疑问，请记住作为一个经验法则，
你不需要它。

# NodeJS & AWS Lambda

NodeJS 是一种运行在 V8 引擎上的后端运行时环境，允许我们编写和执行服务器端 JavaScript。
自 12 年前首次发布以来，它变得极其流行。
它恰好也是在 AWS (Lambda) 上编写无服务器函数时最受欢迎的选择。

这是一个巨大的话题，我会保持得简短。
有几点我想强调一下。

## 使用 promises 代替回调

NodeJS 原初是使用回调模式进行异步调的。
NodeJS 的所有内置模块都是这种结构：你提供主参数以及一个回调函数，该回调函数在异步操作完成后被应用。

```javascript
const fs = require("fs");

fs.writeFile("./file.txt", "some-text", (err, data) => {
  if (err) {
    console.error();
  }
  console.log(data);
});
```

记住，NodeJS 是在 2009 年引入的。
在 2021 年，我们使用 promises。

幸运的是，使用 promises 转换这些方法非常简单。让我们来看两种不同的方法。

## 使用 promisify

你可以使用来自 `utils` 模块的工具函数 `promisify` 将使用回调的函数封装在 promise 中。

它适用于所有遵循 NodeJS 回调规范的函数，这意味着它也适用于一系列旧的 NodeJS 第三方库。

```javascript
const fs = require("fs");
const { promisify } = require("util");
const writeFilePromise = promisify(fs.writeFile);

try {
  const data = await writeFilePromise("./file.txt", "some-text");
} catch (err) {
  console.error(err);
}
```

## 使用 fs/promises

在现代 NodeJS 中，许多内置模块都带有 promises。

```javascript
const fs = require("fs/promises");

try {
  await fs.writeFile("./file.txt", "some-text");
} catch (err) {
  console.error(err);
}
```

## Lambda 中的异步处理器

在 Lambda 中，你可以将处理器定义为 async。

```javascript
exports.handler = async (event) => {
  try {
    const data = await fs.writeFile("./file.txt", "some-text");
    return {
      statusCode: 200,
      body: JSON.stringify(data),
    };
  } catch (err) {
    return {
      statusCode: 500,
      body: err.message,
    };
  }
};
```

## 结语

## 哪些规范

所以，读完这本书后，你可能会问：我应该使用哪些规范？我应该盲目遵循书中的所有规则、风格和规范吗？

不！所有的团队都是不同的。所有的代码库也不同。
首先考虑的最两个事情是保持代码库的一致以及良好的团队合作。

所以如果你加入了一个代码库已存在 6 个以上的团队，请尽可能采用你已经看到的风格、偏好和规范。

尽管如此，建议总是好的，而且根据我的经验，大多数团队都是欢迎的。

记住，在现实世界中成为一名软件开发者更多是一场人际游戏。比你想象的要少取决于编程。

> Simon Høiberg

## 额外资源

如果你是 JavaScript 新手并正在寻找良好的入门资源，我推荐这些：

- Kyle Simpson 的 You Don’t Know JS 书系列：https://www.amazon.com/gp/bookseries/B019EBP9V（非常棒的书！）
- Free Code Camp YouTube 频道：https://www.youtube.com/c/Freecodecamp（免费资源的宝库）
- NodeJS Design Patterns：https://www.nodejsdesignpatterns.com/（适合那些熟悉 JavaScript 但想精通 NodeJS 的人）

最后，我想提一下 Snappify，我用它创建了书中所有的酷炫代码片段：
https://snappify.io/（这是由我一些非常棒的朋友开发的，你真的应该看看）




如果你还没有关注我，可以在 YouTube、Twitter、LinkedIn 和 Instagram 上找到我。我在这些平台上非常活跃，分享关于 SaaS 和在线业务、软件开发以及大量 JavaScript 的知识。

YouTube:
https://www.youtube.com/SimonHoiberg

Twitter:
https://twitter.com/SimonHoiberg

LinkedIn:
https://www.linkedin.com/in/simonhoiberg/

Instagram:
https://www.instagram.com/simonhoiberg/

