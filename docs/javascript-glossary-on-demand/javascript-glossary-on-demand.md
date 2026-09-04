
# JavaScript 术语手册

Andrea Giammarchi

@Web Reflection

**推特分享这本书！**

请通过在 Twitter 上分享这本书来帮助 Andrea Giammarchi。

本书建议的标签（hashtag）是 `#jsglossary`。

点击此链接在 Twitter 上搜索该标签，查看其他人对这本书的评价：

https://twitter.com/search?t=#jsglossary

献给充满活力的 JavaScript 社区

*(注：后文页面提供的 OCR 文本由于字符偏移/编码错误导致严重乱码。我已处理了清晰的部分，并尽可能保留了其余部分的结构，但偏移的乱码文本大部分无法恢复。)*

## 调试

我们喜欢这种基础，因为当我们编写代码并想知道代码执行成功还是失败时，我们需要它。这种验证过程被称为*调试*（debugging），原因是因为它通常通过*调试器*（debugger）进行，调试器是大多数现代浏览器提供的开发者辅助工具。

- 尝试在任何网页上进行*右键点击*（Right Click），查看菜单的最后一项是否有*检查元素*（Inspect Element）。这就是你如何测试书中所有示例的方法：点击*检查元素*，然后点击名为*控制台*（Console）的按钮或标签页，在我们讲解示例的同时开始编写代码段，称为*代码片段*（snippets）。

作为替代方案，你也可以使用 `Node.js` 命令行界面，因为大多数示例与环境无关，这意味着它们可以在任何浏览器以及服务器中运行。

每个代码示例都包含一些分级注释，我强烈建议你至少阅读一遍它们，然后再关注实际的编程。

## 注释

在编程中，注释是对代码本身的有意义的描述。它们在代码执行期间会被忽略，可以是 `//` 单行注释，遇到新行时结束，也可以是 `/* 多行注释 */`。

## 符号

如果你拿一个计算器，你可以看到数字和算术运算。在编程中基本上也是一样，有算术、比较、赋值、条件和其他操作。我们可以在任何控制台中直接使用它们。

| 我们来做些数学题 | |
| :--- | :--- |
| `2 + 2` | `4` |
| `3 * 3` | `9` |
| `2 * 15` | `30` |
| `1 - 2` | `-1` |
| `2 / -1` | `-2` |

*在计算器中符号 `=` 表示*显示结果*，而在 JavaScript 中它意味着*赋值结果*。你可以使用 `=` 号来保留某些结果以便以后使用。*

```
var result = 7;
result * 2 // 显示 14
```

如果你想比较两个不同的值，可以使用三等运算符 `===`。

- `2 === 2` // 当然，相同的数字，它与自身是等同的
- `2 === 3` // 嗯，2 和 3 不同，所以它们不能相同

要验证两个值是否不同，可以使用*非*（not）版本。

- `2 !== 2` // false
- `2 !== 3` // true // 当然 2 和 3 不同。这是真的

*非*（not）运算符可以通过反转其值来否定某些逻辑条件。例如，`!true` 为 `false`，反之亦然。

如果你想说明不同的值实际上是相同的，可以使用逻辑运算符。

- `(4 == 5)` // false
- `(5 == 4)` // false
- `(2 == 3)` // false
- `(true || false)` // true

*在书中后面有一个专门关于这些操作的章节，现在先如此。*

## 部分

可以通过部分（parts）对不同的操作序列分组。这会立即变得更具读性，使开发变得更清晰。例如，如果将一个读取操作视为 `2 * 3`，人们应该认为结果是 `10`，而不是将 `3` 和 `2` 的和相乘，让你和 JavaScript 解释器都对此了然。

部分也简称为 parts，稍后会进行描述。

在 JavaScript 中有大括号 `{}` 或方括号 `[]`。这些可以用于创建对象，在方括号中还可以创建它们的值。

## 变量

变量是一个用于引用值的驼峰命名法（camelCase）。始终以小写开头，最终通过大写字母连接多个单词。如果复合变量名包含单个字符或缩写词，可以使用多个大写字母。

## 引用

引用就像一个指向特定值的简单链接。想象一个对象，照片可以被视为对一个人的引用；你不需要让这个人出现在房间里就能看到她什么样或在做什么，照片就足够了。

### 变量

变量通常是一个用于引用通用值的有意义名称。回到对象的示例，`var photo = new Object()` 创建了一个指向名为 `photo` 的对象的引用。你可以把它留给我，并在需要时从其他人那里接收其他对象，并随时为其赋值。

创建一个引用我对象的变量：

```
var photo = new Object();
// 5 年后
// 保存旧照片
// 通过使用新的变量名
oldPhoto = photo;
// 然后拍摄一个新对象
// 简单地将其赋值给同一个变量
photo = new Object();
```

JavaScript 变量名的常用命名规范是 `camelCase`；始终以小写开头，最终通过大写字母连接多个单词。如果复合变量名包含单个字符或缩写词，可以使用多个大写字母。

### 常用命名规范示例

- `var thisIs$goodNameFor$variable = anyValue;`
- `var result = obj.load();` // `object.property` `genericValue`;

### 常量

常量类似于变量，但只能创建和赋值一次。在现代 JavaScript 中，可以使用 `const` 关键字显式地创建。

*常量的值是静态值*

```
const result = obj.load(); // object.property genericValue;
const a = 'a'; // 显示字母 a
```

*常量的值是静态的*

```javascript
// 它不会改变值
const five = 5; // 显示 5 静态值
```

它们在大多数编程语言中的常用命名规范如下：

这类变量经常（但不限于）被用于描述不改变且具有固定值的数据。

## 参考

此术语与特定的操作有关：使用括号执行任何类型的函数引用。

### 声明函数

**函数** `something()`

- **当 `SOMETHING` 是引用名称时**
- 即我们刚刚声明的函数：`SOMETHING`
- **没有任何**发生（仅显示函数本身）
- **要执行**此函数
- 我们需要使用括号调用它：`SOMETHING()`
- 记录某些内容，

如果你仔细观察，你会发现即使是 `console.log(something)` 这种操作也是在调用一个函数。然而，在这种情况下，`log` 函数是通过 `console` 对象引用调用的，而不是直接调用的，并且它是通过*点符号法*访问的。

每当在点之后调用函数时，该函数就可以被视为一个*方法*。

## 函数声明 VS 表达式

定义函数有几种方法，每种方法的一致性可能有所不同。

例如，函数声明会创建一个*作用域*内任何地方都可用的引用。即使在调用之前，它也已经被声明了：

```
function SOMETHING() {}
SOMETHING(); // 即使在声明之前也可以工作。
```

这可以帮助你将代码组织成独立的块。如果不同部分有许多声明，良好的做法是将所有需要的函数声明在一起。

### 变量-函数声明

通过声明引用的`变量名-函数`：`const SOMETHING = function() {}`

它是与生俱来的，即使在调用之前也是：`SOMETHING = function() {}`

就像每一个变量一样，函数也应该被赋值一个值来引用它，尽管在函数声明中（如示例所示）不需要显式赋值。简单地定义引用的`变量-名-函数`：`const SOMETHING = function() {}`

还有另一个步骤：

- 使用函数名进行赋值：`SOMETHING = 10`
- 在这种情况下，计数从 10 开始。

## 作用域

此术语表示代码执行的边界。将其想象成：宇宙是每一个星系，星系是系统作用域，行星是所有大陆的作用域，对于每个大陆，我们将拥有国家、地区、城市，最后是你自己的房子，当你在里面时，它是你自己的作用域，而当你出来时，城市的其他部分将是你的作用域。

在 JavaScript 中，默认有一个本地作用域，你可以在其中定义函数和变量。然而，回到房子的比喻，你不希望每个邻居都知道你在家里所做的每一件事。你的家是你的地方，而在 JavaScript 中，函数是定义你自己的私有空间的方式，不会被街道中间或其他任何地方（包括其他房屋）发生的事情干扰或干扰。

- 全局作用域在代码执行之前就开始（它已经在那里了）
- 函数作用域从这里开始：

```
function myScope(arg1, arg2, args) {
  // 在 myScope 内部定义变量使其仅在此处可用：
  var myMess = 'my room';
}
// 函数 myScope() 在这里结束：
typeof myScope; // 是函数
// 作用域 myScope 是私有的。
```

由于可以在其他函数内部创建函数，因此也可以在房子内有一个私密房间。要创建私有的，我们可以使用函数名：`SOMETHING = private`。

```
function SOMETHING() {
  // private
  // 在这种情况下，计数为 10
  function SOMETHING() {
    // private
  }
  function SOMETHING() {
    // private (已声明)
  }
}
```

### 本地上下文

如果你打开浏览器控制台或启动 Node.js，你可以通过编写 `console.log(this)` 或直接输入 `this` 来检查本地上下文。

当你在全局范围内定义变量或声明函数时，你也可以通过本地上下文引用这些变量，因为它就像一个对象一样。

- 在全局作用域中直接创建变量：
  - `var definedVariable = '所有人都可以访问我'`
  - 通过全局对象访问：`console.log(this.definedVariable)`
- 当你创建函数时：
  - `function globalFunction() {}`
  - `console.log(this.globalFunction)` (已声明)

重要的是记住，函数可以访问其他变量，但并不总是如此。

然而，每当函数被调用时，在我们完成任务后有一种方法自动清理或释放内存。

### 上下文

每当函数被调用时，可以通过自动可用的 `this` 引用其执行上下文，它具有以下值之一：

- 浏览器和全局服务器中的全局上下文，称为 `window`
- 通过点符号法调用的通用对象：`obj.function()`
- 通过函数方法（如 `.call` 或 `.apply`）调用时，包括 `undefined` 在内的任意值

为了防止意外的全局作用域和上下文污染，JavaScript 规范的第五版本（定义 JavaScript 语言、语法和行为的标准）引入了特殊的 `"use strict"` 指令。

这个奇怪的字符串如果放在函数开头，将保护本地上下文并切换到更严格的行为。如果你再次尝试之前的代码，你将看到错误而不是数字 123。

```
function MYSCOPE() {
  "use strict"; // 将局部作用域切换到严格模式
  return 123;
}
MYSCOPE(); // 显示错误
```

### 未定义

不仅无法在全局作用域意外定义变量，而且当使用此指令时，执行上下文也是未定义的，除非显式提供。

### 在全局作用域中定义

```
function WHO_THIS() {
  "use strict";
  return this;
}
WHO_THIS(); // undefined
```

### 方法上下文

在 JavaScript 对象中，可以拥有任何种类型的属性，函数也不例外。

#### 创建一个空对象

```
var rem = {};
```

#### 将属性定义为函数表达式

```
rem.SOME_PROPERTY_NAME = function() {
  return this;
}
```

#### 返回的上下文值会是什么？

让我们通过调用 `rem.SOME_PROPERTY_NAME()` 来找出答案。

```
rem.SOME_PROPERTY_NAME(); // 正好是 REM 本身
```

当通过对象调用函数时，它会隐式地使用该对象作为其当前的执行上下文。记住，任何函数都可以随时附加到任何对象上，即使它没有被直接定义为该对象的属性。

#### 此处定义的通用函数在其他处

```
function SAY_THE_NAME() {
  console.log(this.name);
}
var obj = { name: 'Generic Object' };
// 我们可以将其作为方法调用
obj.sayName = SAY_THE_NAME;
obj.sayName(); // "Generic Object"
```

尽管附加方法不是个好主意，但我们可以借用**任何类型**的函数并将其作为不同的对象使用，这一事实是令人惊讶的。我们为什么需要这些？这不仅仅是一个小问题，答案是每个项目集合并不一定像数组那样拥有所有方法。新增：有更好、更整洁的方法通过提供上下文来调用函数。

正如类型段落中所描述，通过 `CALL` 或 `APPLY` 调用函数，函数是可执行的特殊对象。就像任何对象一样，函数也可以拥有属性，然后是方法。

任何函数最常用的方法是 `.call()` 和 `.apply()`，它们仅区别在于写法。`.call()` 接受任意数量的参数进行传递，`.apply()` 只接受一个数组作为调用参数。

#### 三个打印某些信息的函数

```
function withArguments() {
  console.log('此处无事可做');
}
function withOneArgument(first) {
  console.log('接收', first);
}
function withTwoArguments(a, b) {
  console.log('接收', a, b);
}
```

#### 现在使用 CALL 并忽略第一个上下文值，使用 NULL：

```
withArguments.call(null);
withOneArgument.call(null, 'SOME VALUE');
withTwoArguments.call(null, 'FIRST VALUE', 'SECOND VALUE');
```

#### 要使用 APPLY() 你需要一个或多个数组

```
var empty = [];
var withOneArg = ['ANY VALUE'];
var withTwoArgs = ['1ST', '2ND'];
```

#### 与你通过 .CALL 打印的结果相同

```
withArguments.apply(null, empty);
withOneArgument.apply(null, withOneArg);
withTwoArguments.apply(null, withTwoArgs);
```

记住 `.call()` 和 `.apply()` 区别的小贴士。"WITH" 单词和 `forEach`。

现在这两种方法的区别已经很清楚了，理解它们以及关于它们。记住上一页的集合。所有方法 `console.log(type.name)`。

### 函数参数

每次函数被调用时，它都需要许多参数，每个参数也是每次执行函数时创建的特殊对象的名称。

```
function contextAndArgs(a, b, c) {
  console.log(arguments);
}
```

正如类型段落中所描述，通过 `CALL` 或 `APPLY` 调用函数，函数是可执行的特殊对象。就像任何对象一样，函数也可以拥有属性，然后是方法。

任何函数最常用的方法是 `.call()` 和 `.apply()`，它们仅区别在于写法。`.call()` 接受任意数量的参数进行传递，`.apply()` 只接受一个数组作为调用参数。

#### 三个打印某些信息的函数

```
function withArguments() {
  console.log('此处无事可做');
}
function withOneArgument(first) {
  console.log('接收', first);
}
function withTwoArguments(a, b) {
  console.log('接收', a, b);
}
```

#### 现在使用 CALL 并忽略第一个上下文值，使用 NULL：

```
withArguments.call(null);
withOneArgument.call(null, 'SOME VALUE');
withTwoArguments.call(null, 'FIRST VALUE', 'SECOND VALUE');
```

#### 要使用 APPLY() 你需要一个或多个数组

```
var empty = [];
var withOneArg = ['ANY VALUE'];
var withTwoArgs = ['1ST', '2ND'];
```

#### 与你通过 .CALL 打印的结果相同

```
withArguments.apply(null, empty);
withOneArgument.apply(null, withOneArg);
withTwoArguments.apply(null, withTwoArgs);
```

记住 `.call()` 和 `.apply()` 区别的小贴士。"WITH" 单词和 `forEach`。

现在这两种方法的区别已经很清楚了，理解它们以及关于它们。记住上一页的集合。所有方法 `console.log(type.name)`。

### 函数参数

每次函数被调用时，它都需要许多参数，每个参数也是每次执行函数时创建的特殊对象的名称。

```
function contextAndArgs(a, b, c) {
  console.log(arguments);
}
```

正如类型段落中所描述，通过 `CALL` 或 `APPLY` 调用函数，函数是可执行的特殊对象。就像任何对象一样，函数也可以拥有属性，然后是方法。

任何函数最常用的方法是 `.call()` 和 `.apply()`，它们仅区别在于写法。`.call()` 接受任意数量的参数进行传递，`.apply()` 只接受一个数组作为调用参数。

#### 三个打印某些信息的函数

```
function withArguments() {
  console.log('此处无事可做');
}
function withOneArgument(first) {
  console.log('接收', first);
}
function withTwoArguments(a, b) {
  console.log('接收', a, b);
}
```

#### 现在使用 CALL 并忽略第一个上下文值，使用 NULL：

```
withArguments.call(null);
withOneArgument.call(null, 'SOME VALUE');
withTwoArguments.call(null, 'FIRST VALUE', 'SECOND VALUE');
```

#### 要使用 APPLY() 你需要一个或多个数组

```
var empty = [];
var withOneArg = ['ANY VALUE'];
var withTwoArgs = ['1ST', '2ND'];
```

#### 与你通过 .CALL 打印的结果相同

```
withArguments.apply(null, empty);
withOneArgument.apply(null, withOneArg);
withTwoArguments.apply(null, withTwoArgs);
```

记住 `.call()` 和 `.apply()` 区别的小贴士。"WITH" 单词和 `forEach`。

现在这两种方法的区别已经很清楚了，理解它们以及关于它们。记住上一页的集合。所有方法 `console.log(type.name)`。

### 函数参数

每次函数被调用时，它都需要许多参数，每个参数也是每次执行函数时创建的特殊对象的名称。

```
function contextAndArgs(a, b, c) {
  console.log(arguments);
}
```

## 循环

### FOR 循环

> 一个或多个变量计算，用分号分隔

#### 第一分号

初始化：需满足的条件

#### 第二分号

条件：用于更新条件的更改

#### 第三分号

增量：对当前值进行某些操作。请注意，这实际上是 for 循环的第三部分。第四部分在它之后。

以之前的 `while` 循环为例，你可以在下面的 `for` 循环中执行完全相同的过程：

| FOR VAR | 索引大小，长度; | 索引 | 0 <= 1 |
| :--- | :--- | :--- | :--- |
| `console.log(list[index]);` | | | |
| `console.log(index);` | | | |
| `console.log();` | | | |

非常重要的是，如果不满足条件，循环的第三部分和第四部分都不会执行。

- 空列表，其长度为 0
- `for (var i = 0; i < length; i++)`

| FOR VAR | i = 0; i < length; | i++ |
| :--- | :--- | :--- |
| `i = 0; i < length;` | | |
| 条件永远不会满足 | | |
| `i = 1` | | |
| 如果条件退出循环，则不会发生 | | |
| `console.log(i);` | | |
| `console.log(i);` | | |
| 因为第四部分 `;` 从未发生 | | |

只要你向列表中放入至少一个项目，条件至少会被满足一次，你会发现循环后 `i` 的值是 1 而不是 0。

### 增量运算符 `++`

使用 `++` 符号来增加整数，而不是通过重新赋值变量本身来加 1，是非常常见的。因此，下面的示例是 `for` 循环通常的写法：

```
for (var i = 0; i < collection.length; i++) {
  // 对 collection[i] 进行某些操作
}
```

`++` 运算符既可以放在变量之前，也可以放在之后。在两种情况下，变量都会递增，但其立即返回的值是完全不同的。

- 使用 `++` 作为后缀（也称为后自增）

```
var num = 0;
var plusNum = num++;
console.log(num++); // 0, 赋值时 num 还没有递增
console.log(num);   // 1
// 1, 因为在 num++ 之后它递增了
```

- 使用 `++` 作为前缀（也称为前自增）

```
var num = 0;
var plusNumPlusNum = ++num;
console.log(++num); // 1, 赋值时 num 已经递增了
console.log(num);   // 1
// 1, ++num 递增了 num 并返回 1
```

没有特定理由偏于其中一种方式，虽然 `num++` 通常更受青睐，但 `++num` 也可以作为遍历包含至少 2 个元素的集合的示例：

```
var i = 10;
while (++i < list.length) {
  compare(list[i-1], list[i]);
}
```

使用 `--` 运算符通过递减（`--`）来减少整数也是可能的，这简化了 `num = num - 1` 操作。

关于 `++` 运算符的所有内容，包括作为前缀或后缀使用时的区别，已最后解释。

## 数组方法

在 JavaScript 中，数组带有一些特殊方法，用于更改、更新或整合项目。数组方法比循环看起来更整洁，但它可以遍历任何集合，包括组。

### `Array.prototype.forEach()`

这可能是最接近循环的数组方法，它的工作原理如下：

```
array.forEach(function(value, index) { ... })
```

函数将被调用 `array.length` 次，在这种情况下意味着三次：

```
console.log(index, value);
```

| FOR VAR | 索引 | 值 |
| :--- | :--- | :--- |
| 0 | | |
| 1 | | |
| 2 | | |
| 3 | | |
| | | |

任何函数都递增了三次，需要详细处理这些组。让我们用良好的 `for` 循环来重构 `forEach` 中发生了什么：

```
for (var i = 0; i < list.length; i++) {
  console.log(i, list[i]);
}
```

`undefined` 是一个确实被用到的特性，但在某些情况下非常有用。某些集合可能没有 `forEach` 方法，但你可以分别遍历其项目。

### `Array.prototype.map()`

通用社交页面上的当前用户：

```
var user = { name: "Andrea" };
// 一个在通用 DOM 元素中写入用户名的方法：
element.textContent = user.name;
// 找到所有显示用户名的节点：
var nodes = document.querySelectorAll(".user-name");
// 遍历用户名的节点：
nodes.forEach(function(user) { ... });
// 将回调作为迭代上下文：
array.forEach(function(value, index) { ... });
```

### `NEW ARRAY`

如果你想根据迭代期间发现的值创建一个新数组，`MAP` 是正确的方法。它的用法与 `forEach` 基本相同，但它调用的函数应该返回每个迭代的值。

```
var single = [1, 2, 3];
var doubled = single.map(function(num, i) {
  return num * 2;
});
// 返回一个新值给索引 i:
console.log(single);  // [1, 2, 3]
console.log(doubled); // [2, 4, 6]
```

`MAP` 的主要用例是在提取、更改或转换集合的初始值后创建一个新列表。

```
var persons = [
  { name: "Andrea", age: 37 },
  { name: "Robert", age: 17 }
];
var adults = persons.filter(function(person) {
  return person.age >= 18;
});
// false, Robert is too young
```

### `Array.prototype.indexOf(value, fromIndex)`

如名称所示，`indexOf` 在数组中查找包含特定值的索引。

```
var alphabet = ['a', 'b', 'c', 'd', 'e', 'z', 'y'];
var index = alphabet.indexOf('c'); // 2
alphabet.indexOf('c'); // 'c'
如果未找到返回 -1
alphabet.indexOf(123); // -1
```

在最新的规范中，`array.includes(value, fromIndex)` 返回一个指示值是否存在布尔值。

实际上有几十种数组方法。它们在 Mozilla 开发者网络中描述了许多示例和用法。

### `Array.methods`

`Array` 是一个包含每个数组集成的所有行为的对象。

- [Methods](https://developer.mozilla.org) (not false)

## 变量与原型继承

当一个新变量的值是一个对象、数组或函数时，它默认会带有一些没有人显式赋值的方法；这些是核心功能中的只读部分。

继承对象有两种机制：直接链接或用于设置继承的特殊函数。在对象之间进行原型继承的第一种直接链接方式是原型（prototype）。

- 被称为原型的通用对象
- 它有两个属性：`name`（名字）和 `age`（年龄）
- 并且有一个更改年龄的方法
- `var obj = { name: '', age: 0, change: function() {} }`

通常，浏览器控制台只会显示自身的属性，忽略继承的属性。这就是为什么即使变量属性还有更多内容，记录时也只显示这些。

### `Generic.prototype` 与全局

在 JavaScript 中，默认可用的方法之一是 `.prototype`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量对象作为一个示例，你可以假设 `object.prototype` 调用的结果为 `true`。

但这具体意味着什么呢？控制台是如何向我展示的？

- Name：Andrew
- 但他也有年龄吗？
- 0 岁，年龄从原型继承
- 他也有生日方法吗？
- `typeof prototype.birthday` // Function：years，从原型继承
- 如果我们把 `birthday` 作为 `object` 的方法来调用会发生什么？
- Name: Andrew, age: 1（突然，那个疯狂的年龄出现了！）
- 他的生日影响了 person one 吗？
- Name: Anonymous, age: 0（没有，一切正常）

关于方法上下文（context）的简要回顾：当我们通过某个对象调用一个函数时，该对象将成为执行上下文。这并不意味着两个 person 都有生日方法，而是意味着它将把 person 作为其自己的方法来执行。

### `Object.prototype`

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象
- 这个对象可以被表示为字符串吗？`[object Object]`
- 但是谁把 `toString` 方法放入你的空对象中的？`Object.prototype.toString`
- 它是 `true`，因为这两个对象之间存在一条原型链。

### `Object.prototype.toString`

由于每个对象在根部都有 `.toString` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，`Array.prototype` 也会继承自 `Object.prototype`，你可以执行 `Array.prototype.toString`。`toString` 方法不是继承来的，它被定义为返回特定格式。

- `Array` 是一个对象，拥有一个简单返回执行上下文的方法。
- `Object.prototype.toString.call([])` // `[object Array]`
- 它是 `true`，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 `Object`。

一旦你理解了方法不需要直接附加或赋值为对象的属性，而是可以被简单地继承，那么原型继承的含义就变得清晰了；它是不同对象之间的一条隐形链。

## Native

在 JavaScript 中，默认可用的方法之一是 `.prototype`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量对象作为一个示例，你可以假设 `object.prototype` 调用的结果为 `true`。

但这具体意味着什么呢？控制台是如何向我展示的？

- Name：Andrew
- 但他也有年龄吗？
- 0 岁，年龄从原型继承
- 他也有生日方法吗？
- `typeof prototype.birthday` // Function：years，从原型继承
- 如果我们把 `birthday` 作为 `object` 的方法来调用会发生什么？
- Name: Andrew, age: 1（突然，那个疯狂的年龄出现了！）
- 他的生日影响了 person one 吗？
- Name: Anonymous, age: 0（没有，一切正常）

关于方法上下文（context）的简要回顾：当我们通过某个对象调用一个函数时，该对象将成为执行上下文。这并不意味着两个 person 都有生日方法，而是意味着它将把 person 作为其自己的方法来执行。

## 构造函数

当你声明一个函数时，引擎会自动为其提供原型 `prototype` 对象。

### 函数

```
function JUST_FUNCTION() {
  // 它可以做任何想做的事
}
console.log(
  "是谁把这个对象放在这儿的",
  JUST_FUNCTION.prototype,
  "它是从全局函数解释的吗",
  JUST_FUNCTION.prototype === Function.prototype
); // FALSE
```

通常情况下，每个 JavaScript 函数都可以用于创建与其自身原型关联的对象，该原型是一个只包含一个属性的对象：`CONSTRUCTOR`（构造函数）。

```
function LINK_NAME() {} // 简单函数
// 当我们通过 NEW 变量和 NEW LINK_NAME() 调用它时，LINK_NAME 就变得特殊了
var instance = new LINK_NAME();
console.log(
  "我们创建了一个原型链",
  LINK_NAME.prototype.isPrototypeOf(instance), // TRUE
  "默认情况下，我们也解释了构造函数",
  "它无非就是函数 LINK_NAME 本身",
  instance.constructor === LINK_NAME, // TRUE
  "这样的构造函数实际上被解释了",
  "因为它确实是 LINK_NAME.prototype 的一部分",
  LINK_NAME.prototype.constructor === LINK_NAME // TRUE
);
```

回到你之前看到的从另一个对象 `Object.create` 的机制，你可以使用函数来创建新实例，如下所示：

```
function SHAPE() {} // 仅用于解释其原型的哑函数
// 使用 SHAPE.prototype 创建一个链
var oneShape = Object.create(SHAPE.prototype);
// 等同于创建一个新的 SHAPE
var anotherShape = new SHAPE();
console.log(
  SHAPE.prototype.isPrototypeOf(oneShape),   // TRUE
  SHAPE.prototype.isPrototypeOf(anotherShape) // TRUE
);
```

这两种方法最大的区别在于，使用 `new SHAPE` 不可避免地涉及 `SHAPE` 函数，隐式地将第一个创建的实例作为执行上下文。

这反过来例如将赋予我们我们在那里进行一些设置的能力。

*作为一种命名规范，类使用 PascalCase（首字母大写）*

```
function PERSON(name) {
  this.name = name;
}
var me = new PERSON("ANDREA"); // 类的方式
// 等效且显式的方式
var me = Object.create(PERSON.prototype);
// 过程式的方式
// 调用 PERSON 来设置 me.name
// 否则完全没有任何 name 属性
PERSON.call(me, "ANDREA");
```

在任何情况下，通过 `PERSON` 或从其原型创建的通用对象，都解释了一个构造函数属性，该属性是 `PERSON` 本身，就像对于通用函数一样。

总结：当我们谈论 JavaScript 中的构造函数时，我们指的是一种特殊方法，一旦实例通过 `new` 关键字被创建，它就会隐式地初始化。

## 实例

只要使用 `new CONSTRUCTOR` 创建对象，它就可以被认为是构造函数的实例。

这有助于我们更好地解释类定义，将对象解释为通过构造函数解释的原型相关对象。

1) 什么是实例？
1) 它是实例
2) 它是从原型解释的实例

正如你看到的，使用实例来区分更加方便，并且它有一个相似的键。

```
function PERSON(name) {
  this.name = name;
}
var me = new PERSON("ANDREA"); // 类的方式
// 等效且显式的方式
var me = Object.create(PERSON.prototype);
// 过程式的方式
// 我们读取了原型实例，但在实际中没有工作。这里有一个逻辑作为属性访问的简单示例。
```

`Object.prototype` 作为通用属性名

```
CLASS.prototype
// 实例.属性
CLASS.prototype
// 实例.属性值
// TRUE
// 实例，返回实例.属性
// CLASS.prototype
// TRUE
```

在上下文中找到属性吗？

- 实例，返回实例.属性
- 不，检查解释的对象。

在 `Object.prototype` 中找到属性吗？

- 实例，返回实例.属性
- 不，检查解释的对象。

在 `Object.prototype` 中找到属性吗？

- 实例，返回实例.属性
- 不，检查解释的对象。

在 `Object.prototype` 中找到属性吗？

- TRUE
- 不，返回 undefined。

### `in` 运算符

如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

```
var obj = { key: 'VALUE' };
console.log(
  '属性可以通过 KEY IN 可达吗',
  'KEY' in obj, // TRUE
  '也可以通过 KEY IN 可达', // TRUE
);
```

非常重要的是记住，知道一个对象可以通过其原型链访问特定属性，并不意味着该属性包含任何值。

例如，即使 `undefined` 也可以认为是全局执行上下文的属性。

```
var root = this; // window / global
console.log(
  '全局上下文包含一个 undefined 引用吗',
  'undefined' in root, // TRUE
  '这意味着该属性有值吗',
  root.undefined, // undefined
  '不'
);
```

这就是为什么我们经常看到检查是否存在并返回值的代码，如果定义了，提供对值的访问。许多人想知道如何遍历属性。`for...in` 是传统的方式，它是定义的。

### `in` 运算符

如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

```
var obj = { key: 'VALUE' };
console.log(
  '属性可以通过 KEY IN 可达吗',
  'KEY' in obj, // TRUE
  '也可以通过 KEY IN 可达', // TRUE
);
```

### `hasOwnProperty`

对于 `WITH PROPERTY`，答案是方法 `hasOwnProperty`，它仅在属性是自身的（直接附加的而非继承的）时返回 `true`。

```
var obj = { PROPERTY: true };
console.log(
  obj.hasOwnProperty('PROPERTY'), // TRUE, PROPERTY 定义了它
  obj.hasOwnProperty('toString'), // FALSE
  Object.prototype.hasOwnProperty.call(obj, 'toString'), // TRUE
  obj.hasOwnProperty('toString'), // FALSE
);
```

如果你通过 `for...in` 遍历，你会发现 `PROP` 在那里是可达的，但别无其他。

`Object.hasOwnProperty(`

如何判断一个属性或方法是否被继承过？`hasOwnProperty`，它仅在属性是自身的（直接附加的）时返回 `true`。

```
obj.hasOwnProperty('OWN_PROPERTY'); // TRUE, 它是自身的
obj.hasOwnProperty('toString');     // FALSE
```

如果你在想为什么需要知道所有这些方法，答案是因为原型实例既是强大的又是危险的。例如，设置一个属性如 `OM.VALUE` 不会简单影响 `OM` 方法，相反，它会影响继承过的 `OM` 方法，因为它还没有被重新定义。

### 共享属性

当我们谈论类和原型时，特别是当存在私有作用域和私有引用时，`SHARED` 术语描述了方法、函数被用于许多地方，通过许多对象。

*作为命名规范，类使用 PascalCase（首字母大写）*

```
function PERSON(name) {
  this.name = name;
}
var me = new PERSON("ANDREA"); // 类的方式
// 等效且显式的方式
var me = Object.create(PERSON.prototype);
// 过程式的方式
// 调用 PERSON 来设置 me.name
// 否则完全没有任何 name 属性
PERSON.call(me, "ANDREA");
```

在任何情况下，通过 `PERSON` 或从其原型创建的通用对象，都解释了一个构造函数属性，该属性是 `PERSON` 本身，就像对于通用函数一样。

总结：当我们谈论 JavaScript 中的构造函数时，我们指的是一种特殊方法，一旦实例通过 `new` 关键字被创建，它就会隐式地初始化。

## 实例

只要使用 `new CONSTRUCTOR` 创建对象，它就可以被认为是构造函数的实例。

这有助于我们更好地解释类定义，将对象解释为通过构造函数解释的原型相关对象。

1) 什么是实例？
1) 它是实例
2) 它是从原型解释的实例

正如你看到的，使用实例来区分更加方便，并且它有一个相似的键。

```
function PERSON(name) {
  this.name = name;
}
var me = new PERSON("ANDREA"); // 类的方式
// 等效且显式的方式
var me = Object.create(PERSON.prototype);
// 过程式的方式
// 我们读取了原型实例，但在实际中没有工作。这里有一个逻辑作为属性访问的简单示例。
```

`Object.prototype` 作为通用属性名

```
CLASS.prototype
// 实例.属性
CLASS.prototype
// 实例.属性值
// TRUE
// 实例，返回实例.属性
// CLASS.prototype
// TRUE
```

在上下文中找到属性吗？

- 实例，返回实例.属性
- 不，检查解释的对象。

在 `Object.prototype` 中找到属性吗？

- 实例，返回实例.属性
- 不，检查解释的对象。

在 `Object.prototype` 中找到属性吗？

- 实例，返回实例.属性
- 不，检查解释的对象。

在 `Object.prototype` 中找到属性吗？

- TRUE
- 不，返回 undefined。

### `in` 运算符

如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

```
var obj = { key: 'VALUE' };
console.log(
  '属性可以通过 KEY IN 可达吗',
  'KEY' in obj, // TRUE
  '也可以通过 KEY IN 可达', // TRUE
);
```

非常重要的是记住，知道一个对象可以通过其原型链访问特定属性，并不意味着该属性包含任何值。

例如，即使 `undefined` 也可以认为是全局执行上下文的属性。

```
var root = this; // window / global
console.log(
  '全局上下文包含一个 undefined 引用吗',
  'undefined' in root, // TRUE
  '这意味着该属性有值吗',
  root.undefined, // undefined
  '不'
);
```

这就是为什么我们经常看到检查是否存在并返回值的代码，如果定义了，提供对值的访问。许多人想知道如何遍历属性。`for...in` 是传统的方式，它是定义的。

### `in` 运算符

如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

```
var obj = { key: 'VALUE' };
console.log(
  '属性可以通过 KEY IN 可达吗',
  'KEY' in obj, // TRUE
  '也可以通过 KEY IN 可达', // TRUE
);
```

### `hasOwnProperty`

对于 `WITH PROPERTY`，答案是方法 `hasOwnProperty`，它仅在属性是自身的（直接附加的而非继承的）时返回 `true`。

```
var obj = { PROPERTY: true };
console.log(
  obj.hasOwnProperty('PROPERTY'), // TRUE, PROPERTY 定义了它
  obj.hasOwnProperty('toString'), // FALSE
  Object.prototype.hasOwnProperty.call(obj, 'toString'), // TRUE
  obj.hasOwnProperty('toString'), // FALSE
);
```

如果你通过 `for...in` 遍历，你会发现 `PROP` 在那里是可达的，但别无其他。

`Object.hasOwnProperty(`

如何判断一个属性或方法是否被继承过？`hasOwnProperty`，它仅在属性是自身的（直接附加的）时返回 `true`。

```
obj.hasOwnProperty('OWN_PROPERTY'); // TRUE, 它是自身的
obj.hasOwnProperty('toString');     // FALSE
```

如果你在想为什么需要知道所有这些方法，答案是因为原型实例既是强大的又是危险的。例如，设置一个属性如 `OM.VALUE` 不会简单影响 `OM` 方法，相反，它会影响继承过的 `OM` 方法，因为它还没有被重新定义。

### 共享属性

当我们谈论类和原型时，特别是当存在私有作用域和私有引用时，`SHARED` 术语描述了方法、函数被用于许多地方，通过许多对象。

*作为命名规范，类使用 PascalCase（首字母大写）*

```
function PERSON(name) {
  this.name = name;
}
var me = new PERSON("ANDREA"); // 类的方式
// 等效且显式的方式
var me = Object.create(PERSON.prototype);
// 过程式的方式
// 调用 PERSON 来设置 me.name
// 否则完全没有任何 name 属性
PERSON.call(me, "ANDREA");
```

在任何情况下，通过 `PERSON` 或从其原型创建的通用对象，都解释了一个构造函数属性，该属性是 `PERSON` 本身，就像对于通用函数一样。

总结：当我们谈论 JavaScript 中的构造函数时，我们指的是一种特殊方法，一旦实例通过 `new` 关键字被创建，它就会隐式地初始化。

## 实例

只要使用 `new CONSTRUCTOR` 创建对象，它就可以被认为是构造函数的实例。

这有助于我们更好地解释类定义，将对象解释为通过构造函数解释的原型相关对象。

## 共享数据协议

```
function SHARED_DATA() {} // 将被继承
var ONE = new SHARED_DATA(); // 两个不同的实例
var TWO = new SHARED_DATA(); // 继承自 SHARED_DATA.prototype
// 注意：部分是可选的
ONE.DATA = { TEST: 'ONE CHECK' };
console.log("DID previous operation affected TWO.DATA");
TWO.DATA.TEST = 'ONE CHECK'; // ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据
console.log(ONE.DATA === TWO.DATA); // TRUE 是的，它们是完全相同的引用
```

上面的示例是现代 JavaScript 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

### `FUNCTION NOTSHARED()`

```
function NOTSHARED() {
  this.DATA = {}; // 创建实例属性的正确位置
}
var ONE = new NOTSHARED();
var TWO = new NOTSHARED();
ONE.DATA.TEST = 'ONE CHECK';
console.log("DID previous operation affected TWO.DATA");
TWO.DATA.TEST = 'ONE CHECK'; // ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据
console.log(ONE.DATA === TWO.DATA); // FALSE 它们是完全不同的引用
```

上面的示例是现代 JavaScript 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

### `CLASS NOTSHARED DATA`

#### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | `{}` |
| TEST | `ONE CHECK` |
| CONSOLE | `LOG` |

### `FUNCTION NOTSHARED()`

```
function NOTSHARED() {
  this.DATA = {}; // 创建实例属性的正确位置
}
var ONE = new NOTSHARED();
var TWO = new NOTSHARED();
ONE.DATA.TEST = 'ONE CHECK';
console.log("DID previous operation affected TWO.DATA");
TWO.DATA.TEST = 'ONE CHECK'; // ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据
console.log(ONE.DATA === TWO.DATA); // FALSE 它们是完全不同的引用
```

上面的示例是现代 JavaScript 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

### `CLASS NOTSHARED DATA`

#### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | `{}` |
| TEST | `ONE CHECK` |
| CONSOLE | `LOG` |

### `FUNCTION NOTSHARED()`

```
function NOTSHARED() {
  this.DATA = {}; // 创建实例属性的正确位置
}
var ONE = new NOTSHARED();
var TWO = new NOTSHARED();
ONE.DATA.TEST = 'ONE CHECK';
console.log("DID previous operation affected TWO.DATA");
TWO.DATA.TEST = 'ONE CHECK'; // ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据
console.log(ONE.DATA === TWO.DATA); // FALSE 它们是完全不同的引用
```

### `CLASS NOTSHARED`

#### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | `{}` |
| TEST | `ONE CHECK` |
| CONSOLE | `LOG` |

```
function NOTSHARED() {
  this.DATA = {}; // 创建实例属性的正确位置
}
var ONE = new NOTSHARED();
var TWO = new NOTSHARED();
```

### `UNDEFINED PROPERTY`

`UNDEFINED` 是因为 ONE 和 TWO 正在共享相同的数据。每个实例有不同的数据。

作为对比，在现代环境中，上述类将如下所示：

### `CLASS NOTSHARED DATA`

#### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | `{}` |
| TEST | `ONE CHECK` |
| CONSOLE | `LOG` |

### `FUNCTION NOTSHARED()`

```
function NOTSHARED() {
  this.DATA = {}; // 创建实例属性的正确位置
}
var ONE = new NOTSHARED();
var TWO = new NOTSHARED();
```

### `UNDEFINED PROPERTY`

`UNDEFINED` 是因为 ONE 和 TWO 正在共享相同的数据。每个实例有不同的数据。

## 访问器和赋值器

### `VAR ME`

```
var me = {
  name: "Andrea",
  realAge: 37,
  birthday: function() {
    console.log("Happy birthday " + this.name);
    this.realAge++;
  },
  get age() {
    return this.realAge;
  },
  set age(newAge) {
    console.warn("I am afraid I cannot change my age to " + newAge);
  }
};
console.log(me.age); // 37
me.age = 40; // "I am afraid I cannot change my age to 40"
me.birthday(); // "Happy birthday Andrea"
console.log(me.age); // 38
```

提到现代类时，语法与上面看到的非常相似。

## 属性

任何对象的属性可以使用以下特征来描述：

- 可枚举的 (`enumerable`)
- 可配置的 (`configurable`)
- 可写入的 (`writable`)
- 值 (`value`)

属性是可以定义或删除的，如果你想将其定义为访问器 (`accessor`)，你还可以设置数组的长度。在这种情况下会发生什么？

我们应该检查我们的手表、电话或媒体吗？访问器函数将返回期望的值，而赋值器可以更新它，甚至发生错误，在方便的情况下，将其设为不可写。

如果你熟悉页面，你可能知道像 `textContent` 或 `innerHTML` 这样的属性，一旦定义就会影响整个内容。

所有这些神奇属性都归功于访问器和赋值器。它们与普通方法不同，但你不需要显式调用它们。

这是一个方法的示例：`object.property`：`var size = 8` (`configurable: true`, *你可以以后删除它*, `getter: function() { return this.size; }` *每次都计算一次*), `set: function() { throw new Error('不允许'); }` *并不是简单地改变区域*。

读取区域，它调用构造函数 `get` as method `console.log("DID previous operation affected TWO.")`

### `UNDEFINED PROPERTY`

`UNDEFINED` 属性是因为 ONE 和 TWO 正在共享相同的数据。每个实例有不同的数据。

## 属性定义与赋值

为了确保安全或免受错误影响，我们对许多可能出错的问题完全没有控制能力。有更好的方法来控制我们的应用程序，并防止许多可能出现的问题不断增加。

定义属性有许多方法，特别是在创建新对象时。

### 在什么情况下使用什么描述符

有多种定义属性的方法，既方便又令人沮丧。谈到描述符（descriptors）时，有很多问题需要讨论，但让我们专注于 JavaScript 中常用的描述符即可。

例如，每个作为赋值的通用属性都将具有可配置、可写入和可枚举的描述符。

| 属性 | 可配置 | 可写入 | 值 |
| :--- | :--- | :--- | :--- |
| Name | True | True | String |
| Age | True | True | 7 |
| Function | True | True | Function |

### Native Code

原生描述符的可配置和可写入实际上是幸运的，这意味着它们可以在需要时重新赋值和修复。

## 防御性方法描述符

如果我们为了自己的目的创建一个类，我们可能希望确保其方法在应用程序执行过程中无法在其他地方被修改。

在这种情况下，我们可能希望按照如下方式在原型中直接设置方法：

- 直接在类或函数中定义属性方法。
- `Configurable: false`, `Enumerable: false`, `Writable: false` - 之后无法更改。

## 懒加载属性描述符

当我们谈论属性时，指的是那些在我们第一次需要之后将具有预期值的属性。

在后续页中，我们将通过许多功能详细介绍它，但我们可以请求更多属性。在理论上，汽车有一个定义的属性，但它的定义方式是那样。

### 懒加载属性描述符

我们需要使用定义属性的原因是，如果我们将来想更改该属性，我们应该能够删除或替换该属性，这就是我们将其设置为可配置的原因。

关于描述符的最后一个重要信息是，你不仅可以设置它们，而且始终获取它们。让我们尝试用这种方法进行练习，解释或验证我们目前学到的所有内容。仔细观察对象属性。

### 最直接访问的 JavaScript 类

| 属性名 | 可配置 | 可写入 | 值 |
| :--- | :--- | :--- | :--- |
| Name | True | True | String |
| Age | True | True | 7 |
| Function | True | True | Function |

## `Object.defineProperties(obj, descriptors)`

`Object.defineProperties` 的复数版本某种程度上简化了多个描述符的赋值，因为它需要的输入更少（这总是一个加分项）。

| 属性名 | 可配置 | 可写入 | 值 |
| :--- | :--- | :--- | :--- |
| Name | True | True | String |
| Age | True | True | 7 |
| Function | True | True | Function |

## 静态方法

我们一直使用方法作为对象的键等，这些方法通过全局可用的类暴露。在大多数原生类中还有其他方法，例如 `Array.isArray(array)`、`String.fromCharCode(0x1f49)` 或 `Number.isNaN(NaN)` 等。

这些方法与其依附的构造函数相关。我们也可以以正确的方式自己定义类似的静态方法。

## 函数描述符



记住：函数只是对象。`square.function = function(n) { return n * n; }`，`square.return = function(n) { return n * n; }`。

测试两个不同的矩形：

- `var rect1 = new Rectangle(2, 3);`
- `var rect2 = new Rectangle(2, 2);`

反转矩形的 `.isSquare`：`square(rect1.isSquare)`

`square` 属性为 false，但如果该实例是正方形，它仍然返回 true。这不涉及任何上下文。

后者的条件对于每个公共静态函数都是相同的。例如，对象键在执行时不需要对象的上下文。

## 对象：222 静态对象函数快捷方式

（可选，使用 `const` 以便我们之后可以直接使用它）

## 继承 (EXTENDS)

继承之旅始于讨论对象继承其他对象，结束于讨论类继承其他类。没有理由感到恐慌，这只是对以下问题的简短回答：

### 什么是正方形

- 1) 一个继承原型的类
- 2) 一个原型直接继承另一个原型的类

原型可以继承的量没有具体限制，但两个类之间只能有一个直接的继承关系。因此，当我们使用“扩展（extended）”一词时，我们只能指的是一种特定的关系。

- 一个继承的构造函数

```
Function extending(width, height) Return this.width height 带有一个面积对象。object.defineProperty(prototype, area)
Return this.height
```

- 一个正方形构造函数

```
Function square(size) Invoke the super constructor which will set up我们的实例上下文。extending prototype.all(size, size) 这里正方形通过 prototype 继承了 prototype。Square.prototype createSquare(prototype, area)
Var two new square(width, height) console.log 2 2 case 2 2*
```

## SUPER

当 `super` 词（有时也用 `parent`）在面向对象编程中出现时，它指的是当前执行上下文继承的最直接祖先类。它是一个特殊的关键字，绝不应该在通用类方法之外使用。它曾经是一个保留字，遇到它可能会破坏 JS 程序。

在 Pre-AScript 2015 时代，在 `class` 关键字从保留字状态提升为可用状态之前，某些库曾使用此关键字作为属性，来快捷访问从继承的原型提供的任何内容。但如今，在实际代码中看到它的用法已经非常常见。

### ES6 中的类原型 (D.N.A. (ES2015*))

| 类原型 | 构造函数(width, height) | this.width | this.height | 获取面积(width) | 返回 this.width * height |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Square | square(size) | this.width size | this.height size | Return this.width * height | |
| Rectangle | rectangle(width, height) | this.width width | this.height height | Return this.width * height | |

我们现在如何使用 `extended` 关键字：

请记住，如果你需要调用一个不是构造函数的正方形方法，你需要通过点操作符来访问它，例如 `square.`。在这两种情况下，正方形方法的执行都会被自动识别，所以你需要使用 `.`。

## 实现 (IMPLEMENTS)

在编写时，这个术语实际上并不是当前接口 true 的一部分。它通常表示一个类或通用对象正在继承某些接口。

### 接口 (Interfaces)

接口通常是指通过方法或属性描述的行为。接口可以用于描述执行操作：它们需要实现任何逻辑。例如，下面是一个通过接口数量描述的部分类。请注意，以下文本不是 JavaScript，而是两个接口看起来像样的示例：

```
Interface WalkingMethodMove(which specified)
Interface WalkingMethodInhale
ClassHuman: Walking, Breathing
```

记住：“部分（部分）”一词也常描述某些在最终形状上尚未完全组成的应用、类或对象。

## 特性与混入 (TRAIT AND MIX)

这两个术语表示了相似的概念：一个对象或函数能够继承另一个对象、类或函数，并带来它特定的行为。

### 基础混合工具

#### mix(source, target)

- 对于目标对象中的每个属性名（`Object.getOwnPropertyNames(target)`）。对于每个函数键，使用相同的 `target>key` 描述符来丰富 source。（`Object.defineProperty(target, key, Object.getOwnPropertyDescriptor(source, key))`）
- 返回 source

#### 一种我们可以用来丰富任何对象的简单特性。它内部包含了完整的逻辑，可以独立工作。

```
Var circle
r = 0,
- 初始半径值
Get circumference(r)
- 计算周长 Return this 2 * Math.PI * r
- 计算面积 Return this Math.PI * r * r
- 返回宽度
```

如果我们有一个为 12 的半径，`console.log 12 75.3982236861553 2 3*`

## 混入 (MIX)

通过 `mix` 组合对象或原型，这不需要修改活跃的类，相反，这实际上让我们的代码去冗余且极具可移植可合并性。

在学习面向对象编程和 JavaScript 时，你会有很多其他细节想要学习，但在这些页面中，最近已经涵盖了描述代码片段、应用或任何其他关于各类对象的主要词汇。

### 否则 switch 和条件逻辑

在介绍了像面向对象编程这样更复杂的课题之后开始阅读基础逻辑，感觉很奇怪，但其背后的原因是你现在应该能够理解即使是复杂的例子。

## 条件语句 (Conditional statement)

几乎所有的程序都基于条件。只有当数据库中已知用户和密码时才会执行登录。如果我们按下按钮，电梯会移动到其他层并在门关闭时通过，否则它会打开门并重新开始整个过程。

倒计时器在数值达到 0 时响，以此类推。

我们每天做的每件事，以及环绕我们的一切都是基于基础的 `if` 流，这同样适用于任何可能执行也可能不执行某事的软件。

## 让我们开车 (LetsDrive)

```
Function letsDrive(car, where)
- 只有在关闭时才启动引擎
- 如果 (car.isEngine(off)) car.start(engine())
- 让我们小心移动，以防下雨
- 如果 (global.weather.israining()) car.lowerThanual(size)
- 让我们小心移动，以防下雨 (重复)
- 如果 (global.weather.israining()) car.lowerThanual(size)
- 让我们小心移动，以防下雨 (重复)
- 如果 (global.weather.israining()) car.findRongs(size)
- 让我们小心移动，以防下雨 (重复)
- 如果 (global.weather.israining()) car.findRongs(all)
- 返回宽度 (重复)
```

### 返回 result

```
Function newVar car,
- 每次需要开车 letsDrive
```

### 返回 source

- 一种我们可以用来丰富任何对象的简单特性。它内部包含了完整的逻辑，可以独立工作
- 一种我们可以用来丰富任何对象的简单特性。它内部包含了完整的逻辑，可以独立工作。

```
Var circle
r = 0,
- 初始半径值
Get circumference(r)
- 计算周长 Return this 2 * Math.PI * r
- 计算面积 Return this
```

## Switch 语句 (Switch statement)

- 让我们开车
- 只有在关闭时才启动引擎 (重复)
- 如果 (global.weather.israining()) car.lowerThanual(size)
- 让我们小心移动，以防下雨
- 如果 (global.weather.israining()) car.lowerThanual(size)
- 让我们小心移动，以防下雨
- 如果 (global.weather.israining()) car.findRongs(size)
- 让我们小心移动，以防下雨
- 如果 (global.weather.israining()) car.findRongs(all)
- 让我们开车
- 每次需要开车

## 逻辑运算符 (&&)

与其使用许多 `else if` 导致执行相同的操作，你可以使用 `&&`。

因此，上一个例子可以重写为如下方式：

## 条件语句 (Conditional statement)

几乎所有的程序都基于条件。只有当数据库中已知用户和密码时才会执行登录。倒计时器在数值达到 0 时响，以此类推。

我们每天做的每件事，以及环绕我们的一切都是基于基础的 `if` 流，这同样适用于任何可能执行也可能不执行某事的软件。以下代码是一个关于我们的驾驶路线如何基于条件的虚构示例。

## FUNCTION IS/LETTER()

### IF LETTER A __ LETTER B __ LETTER C __ LETTER D __ LETTER E __ LETTER F )

**RETURN TRUE**;

* 当函数返回时，它会退出该函数
* 这让你能够避免冗余的操作

**RETURN FALSE**;

* 否则，因为真的没有其他可以做的事了

## 逻辑运算符 (&& (读作与与))

与 `__` 运算符相反，`__` 运算符只有在在前一个条件通过验证后才会继续检查条件。这可能是需要记住的最重要概念之一。

例如，以下 ATM 操作将不会同时执行，而是一个接一个地执行。

## FUNCTION GETMONEY()

### IF CARDVALID() )

* 卡片有效吗？是的。下一个*

### PINVALID() )

* 用户知道密码 吗？下一个*

### USERSELECTED$AMOUNT() )

* 用户需要一定金额
* 金钱吗？下一个*

**RETURN** GET$AMOUNTSELECTED%BYUSER() ); *一切顺利，进展良好。*

**RETURN** 0;

* 上面发生了错误*

也可以结合这两个运算符，这在某种程度上简化了三元运算符的功能。

* 通过布尔逻辑实现三元运算符 `console.log(1 && 2)` 2. __ (&&||) ) ;
* 显示 2。
* 三元运算符的评估 `console.log(1 || 2)` 2. (||) ) ;
* 显示 2。也是

然而，当我们需要三元逻辑时，可能应该使用适当的运算符。

## 真值与假值

if 或 else 语句，以及三元或逻辑运算符都是非常仁慈的。检查一个实际的布尔类型 true 或 false 值并没有区别。值 `false` 连同数字 0、空字符串 `""`、null 值、undefined 以及自身的 NAN 引用，被视为*假值 (falsey values)*。这意味着其他所有内容都被视为*真值 (truthy)*，就好像它们是一个真条件一样。

### IF `console.log` 任何对象都是真 ) ;

### IF `[]` `console.log` 即使是空数组也是真 ) ;

### IF `-1` `console.log(` 或负数 ) ;

### IF `FUNCTION()()` ) `console.log(` 或函数 ) ;

* 假值……全部检查过了，没有一个通过*

**FALSE __ NAN __ 5 __ 0 __ NULL __ UNDEFINED** ) `console.log` 这条消息永远不会显示 ;)

## 反模式 (ANTIPATTER)

不一定与布尔逻辑有关，“反模式”一词指的是某些糟糕的实践，或者代码中具有已知且非预期效果的逻辑。例如，模拟三元运算符而不是使用它，就构成了一个反模式。

**TRUE** `console.log(2) || console.log(false)` ) ;

* 2. 正确

**TRUE** `console.log(2) || console.log(false)` ) ; * 2. 然后为假/*

这是因为 `console.log` 总是返回 `undefined`，而 `undefined` 是*假值*。

## DOM

文档对象模型指的是任何网页的*并行世界*。它是一个巨大的接口集合，描述了每个 HTML 元素、SVG 和 XML 节点，或通过文档树可用的外部对象的能力和行为。

当我们处理来自页面的对象时，我们可以称之为 DOMNODE。

## 树 (TREE)

许多 DOM 节点可以包含其他元素。层次结构是嵌套的，从通用根节点到每一个节点，同一层级可能存在多个节点。以下是一个简单的 HTML 页面及其树示例。

- DOMNODE element
- DOMNODE head own- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE element
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element
- DOMNODE text
- DOMNODE element

## 59

文档对每个方法以及每个接受的参数的含义提供了更详细的解释，但这里有一些新术语。澄清这些术语有助于更好地理解我们在讨论什么。

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

```
console.log(VOID 0) ;
* 0 或任何其他值，都会打印出 undefined*
console.log(VOID "hello!") ) ;
* undefined*
```

## VOIDSTRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 `addlistener(type, listener, false)` 方法以及一个 `detachedevent(event)` 方法，该方法可能会抛出异常。

## 异常 (EXCEPTION)

上面的描述基本上说明每个节点都将有一个 `addlistener(type, listener, false)` 方法，加上一个 `detachedevent(event)` 计数器。

* 接口名称所有* 接口元素，其他元素
* 返回类型
* 方法属性名
* VOID

ADDEVENTLISTENER

* 参数类型和名称 没问题
* EVENTLISTENER LISTENER
* BOOL
USE-CAPTURE

VOID

ADDEVENTLISTENER

* 接口名称
* 接口元素，其他元素
* 方法属性名
* 返回类型
* 方法是 VOID
* 参数类型和名称
* 静态方法
* 方法属性名

ADDEVENTLISTENER

* 方法属性名
* 方法属性名

## 559

文档提供的远不仅仅是节点或元素属性，阅读文档参考最好的地方是 WEB。它直接用于描述 DOM 相关的接口以及大多数用户想要知道的：能够读取到预期的用法。例如，如果你阅读文档参考，你会发现

* 接口名称
* 其他元素，
* 方法属性名
* 返回类型
* 方法属性名
* 返回类型
* 方法属性名
* 返回类型
* 方法属性名
* -
* -
*

## 560

文档对每个方法以及每个接受的参数的含义提供了更详细的解释，但这里有一些新术语。澄清这些术语有助于更好地理解我们在讨论什么。

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

```
console.log(VOID 0) ;
* 0 或任何其他值，都会打印出 undefined*
console.log(VOID "hello!") ) ;
* undefined*
```

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 `addlistener(type, listener, false)` 方法以及一个 `detachedevent(event)` 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 `addlistener(type, listener, false)` 方法，加上一个 `detachedevent(event)` 计数器。

* 接口名称所有* 接口元素，其他元素
* 返回类型
* 方法属性名
* VOID

ADDEVENTLISTENER

* 参数类型和名称 没问题
* EVENTLISTENER LISTENER
* BOOL
USE-CAPTURE

VOID

ADDEVENTLISTENER

* 接口名称
* 接口元素，其他元素
* 方法属性名
* 返回类型
* 方法是 VOID
* 参数类型和名称
* 静态方法
* 方法属性名

ADDEVENTLISTENER

* 方法属性名
* 方法属性名

## 559

文档提供的远不仅仅是节点或元素属性，阅读文档参考最好的地方是 WEB。它直接用于描述 DOM 相关的接口以及大多数用户想要知道的：能够读取到预期的用法。例如，如果你阅读文档参考，你会发现

* 接口名称
* 其他元素，
* 方法属性名
* 返回类型
* 方法属性名
* 返回类型
* 方法属性名
* 返回类型
* 方法属性名
* -
* -
*

## 560

文档对每个方法以及每个接受的参数的含义提供了更详细的解释，但这里有一些新术语。澄清这些术语有助于更好地理解我们在讨论什么。

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

```
console.log(VOID 0) ;
* 0 或任何其他值，都会打印出 undefined*
console.log(VOID "hello!") ) ;
* undefined*
```

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 `addlistener(type, listener, false)` 方法以及一个 `detachedevent(event)` 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 `addlistener(type, listener, false)` 方法，加上一个 `detachedevent(event)` 计数器。

* 接口名称所有* 接口元素，其他元素
* 返回类型
* 方法属性名
* VOID

ADDEVENTLISTENER

* 参数类型和名称 没问题
* EVENTLISTENER LISTENER
* BOOL
USE-CAPTURE

VOID

ADDEVENTLISTENER

* 接口名称
* 接口元素，其他元素
* 方法属性名
* 返回类型
* 方法是 VOID
* 参数类型和名称
* 静态方法
* 方法属性名

ADDEVENTLISTENER

* 方法属性名
* 方法属性名

## 559

文档提供的远不仅仅是节点或元素属性，阅读文档参考最好的地方是 WEB。它直接用于描述 DOM 相关的接口以及大多数用户想要知道的：能够读取到预期的用法。例如，如果你阅读文档参考，你会发现

* 接口名称
* 其他元素，
* 方法属性名
* 返回类型
* 方法属性名
* 返回类型
* 方法属性名
* 返回类型
* 方法属性名
* -
* -
*

## 560

文档对每个方法以及每个接受的参数的含义提供了更详细的解释，但这里有一些新术语。澄清这些术语有助于更好地理解我们在讨论什么。

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

```
console.log(VOID 0) ;
* 0 或任何其他值，都会打印出 undefined*
console.log(VOID "hello!") ) ;
* undefined*
```

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 `addlistener(type, listener, false)` 方法以及一个 `detachedevent(event)` 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 `addlistener(type, listener, false)` 方法，加上一个 `detachedevent(event)` 计数器。



## 统计信息

- `STATISTICS` 始终是一个数组
- 针对许多 1-10 个参数 `ARGUMENTS.LENGTH`
- 如果有额外的参数 `CONSOLE.LOG(STATISTICS)<1@)`
- 记录之前的文本 `CONSOLE.LOG(ARGUMENTS>1)`
- 记录当前值 `CONSOLE.LOG(STATISTICS)<1@)`
- 记录最后的统计信息字符串
- 我们现在可以标记任何反引号后的字符串，并在 `2 6 3` 之后检查控制台标记器
- 在标签之前的、`=`、标签之后的函数在返回值之前对其进行转换时特别有用

## 函数属性（标记）

- 针对许多输出声明一个输出、一个正则表达式和一个转换器 `>@, RE <2>! , IN (P)! .CHARCODE$AT(0), 1-10 ARGUMENTS.LENGTH) OUTPUT(MASK)<1@, ARGUMENTS>1). REPLACE RE, IN (P); OUTPUT(MASK)<1@), OUTPUT(MASK)<2@).`
- 返回 `OUT.JOIN(),`
- 转换后的任何值
- 恶性输入 `CONSOLE.LOG(ATTRIBUTES)` 输入值 `5****VALUE****5!C)` 已清洗

### 正则表达式

正则表达式构造函数及其实例引入了一种强大的语法，能够通过具有特殊含义的特殊字母对字符串进行搜索、匹配、测试或替换。

有许多注意事项、可能的安全影响、字符串编码问题以及处理这些问题的现代或旧方法，我认为在这里部分介绍它们将是明智的。

重要的是了解它们的字面量表示法：

- 如何识别字面量的、内联的正则表达式实例 `REGEX <A("SEARCH) VIA.\SPECIFIC-CHARS)IMP)`
- 开始
- 结束
- 可选 `g,i,m,x` 标志
- `-621`

一个没有关于 JavaScript 对象表示法的解释术语表将是不可靠的，所以这里是：

- `JSON` 是对象、数组、字符串、布尔值、数字、`null` 以及其他任何内容的字符串表示标准。
- `JSON-21` 是以下值的字符串表示：
- `STR ^NAME$:-JSON,21,VALUES$::>STRING,1.2,^,>@,TRUE,FALSE,NULL)`

我们可以通过 `JSON-21.PARSE(STR OR CODE)` 解析任何兼容值，使用 `JSON-21.STRINGIFY(COMPATIBLEVALUE)`，两种方法都接受回调作为可选参数。在解析过程中读取每个实体以及生存值时，将调用回调。

## 数学

这个全局可用的对象充满了方法，其目的是帮助我们进行数学计算。

最常用的是 `MATH.POW(NUM, POWER)`、`MATH.STRT(NUM, RAD)`、`MATH.MAX(NUM1, NUM2, NUM1)` 和 `MATH.MIN(NUM1, NUM2, NUM1)`，但你始终可以通过名称检查所有它们，并最终在线调查它们的签名。

- 以下是一个帮助函数，可以告诉我们关于任何对象的很多
- `FUNCTION TELLMEABOUT(THAT) CONSOLE.OBJECT.GETOWNPROPERTIESNAMES(THAT)`
- `TELLMEABOUT(MATH);`
- `LET SS` 看看里面有什么 `S*`

### `PARSEINT(STRING, BASE)` NUMBER

当你处理输入时，你处理的是字符串。如果你请求年龄或任何数字，`PARSEINT` 将帮助你转换输入。`CONSOLE.LOG(PARSEINT(3)`，我们可以省略基数，然而 `PARSEINT(11)`，`PARSEINT(11)` 的 `BASE` 是 `3`，不是 `11`) `PARSEINT(08)` 应该是 `0`) `PARSEINT(16)` `BASE 25`)

### `PARFLOAT(STRING)`

当你需要将字符串转换为浮点数时，`PARFLOAT` 是方法。它不接受任何参数，`PARFLOAT` 不会被识别为数字。

## 新的 JavaScript 特性

自从我开始编写这个术语表以来，情况发生了变化。阅读。这意味着随着步骤匹配，新功能变得可用。JavaScript 规范确实是一个活的标准。新的 JavaScript 特性，`JASCRIPT, 9D`。

## JASCRIPT FAST

下面是针对常见问题的快速回答列表：

- `JASCRIPT FAST?` 按需提供
- `JASCRIPT FAST?`

### 生产环境（PRODUCTION）意味着什么？

它是通用网站、应用程序、框架、设计或程序的正式版本，目前提供给每个用户。这是我们交付的内容，而不是为了快速测试我们的想法而制作的原型。

### 原型（原型）意味着什么？

我知道这个术语表可能令人困惑，但在涉及非技术 `J6` 讨论时，原型是一个草图，或者是最终产品的快速创建版本，它可能不应该直接这样进入生产环境。

## 关于 J6 我还应该知道什么？

我一直在使用 `J6` 及其变体。学习更多是一个好主意，但如果你对前端后端开发感兴趣，你应该先尝试理解。也尝试阅读更新后的书籍，因为在过去的 20 年里 `J6` 发生了很大变化。了解过去是好的，但归根结底我们将使用现代功能。

你听说过转换器（`TRANSIPLES`）吗？

我不光听说过它们，也使用它们。例如，这个术语表中的大多数平台示例已经通过 `LABEL-NODE` 成功测试，这是一个命令行界面 (`CLI`)，它将最新的 `J6ASCRIPT` 规范的最新功能引入代码中。我应该在生产环境中使用它们吗？这取决于情况。

### 生产环境意味着什么？

它是通用网站、应用程序、框架、设计或程序的正式版本，目前提供给每个用户。这是我们交付的内容，而不是为了快速测试我们的想法而制作的原型。

### 原型意味着什么？

我知道这个术语表可能令人困惑，但在涉及非技术 `J6` 讨论时，原型是一个草图，或者是最终产品的快速创建版本，它可能不应该直接这样进入生产环境。

### 哪个框架、库或工具我应该使用？

解决你问题的那个。

### JASCRIPT 仅用于网页吗？

现在很难找到不运行 `J6` 的电子设备。智能手表、路由器、你现在的电脑，甚至是彩色的灯泡，都兼容某些 `J6` JavaScript 引擎或已经在运行它。

### `WEAKMAP` 快速吗？

类似于 `WEAKMAP`，`J6^3` 实例可以关联对象，但移除这种关系是你的责任。

### `JASCRIPT` 快速吗？

新的 JavaScript 特性

现代 JavaScript 引擎可以通过关键字声明。

`JASCRIPT FAST$4` 按需提供

下面是针对常见问题的快速回答列表：

- `JASCRIPT FAST?` 按需提供
- `JASCRIPT FAST?`
- 需求驱动

这里肯定还有我遗漏的其他问题，我鼓励你去寻找答案。一个拥有优质且通常是最实时的文档的地方是 `MDN` 开发者网络。

还有许多我没有机会讨论的话题，例如：

- `Web Workers`、`Service Workers`、`IndexedDB`、本地存储（`localStorage`）和会话存储（`SessionStorage`）、通过 `WebSockets` 和 `XRequests` 进行分页，以及最近的 `Fetch API`，但我相信如果你已经读到了这里，你现在能够理解大多数在线技术文章了。

## 有用链接

| 名称 | 地址 |
| :--- | :--- |
| [Mozilla 开发者网络](https://developer.mozilla.org) | developer.mozilla.org |
| [万维网联盟](https://www.w3.org) | w3.org |
| [IDE Web 控制台](https://ideweb.com) | ideweb.com |
| [WHATWG](https://whatwg.org) | whatwg.org |
| [Node.js](https://nodejs.org) | nodejs.org |
| [Base64](https://base64.js) | base64.js |
| [<.-6 (书籍系列)](https://youdontknows.com) | youdontknows.com |
| [探索 ES6](https://exploringes6.com) | exploringes6.com |
| [HTTPs](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) | developer.mozilla.org/en-US/docs/Web/API/Fetch_API |
