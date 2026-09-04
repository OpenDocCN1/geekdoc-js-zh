
# JavaScript 随需字典 (JavaScript 初学者指南 - 最佳 JavaScript 基础)：A 到 Z

![](img/f3aee4f425dde94406cfd16da04bde08_0_0.png)

《JavaScript 随身字典》是一本开启 JavaScript 编程复杂世界的终极参考指南。此书专为初学者和中级开发者设计，提供了一份全面的 JavaScript 词汇表、常用术语和核心概念汇编，并以易于阅读和通于理解的格式呈现。

## 读者群体：这本书是给谁看的

对于初学者和中级开发者，这本书提供了一份全面的 JavaScript 词汇表、常用术语和核心概念汇编，并以易于阅读和通于理解的格式呈现。

## 如何阅读本书

对于初学者和中级开发者，这本书提供了一份全面的 JavaScript 词汇表、常用术语和核心概念汇编，并以易于阅读和通于理解的格式呈现。

## 特别致谢

感谢所有相信我并帮助我实现想法的人，特别是：Robert Wolchan, Stoyan Stefanov, Arianna De, Cinzia Sardella, Luca Vavassori 以及 TC39 邮件列表的成员，他们耐心处理了我的问题和抱怨。

## 作者

Andrea Garchi 是一位丰富的 Web 和移动开发顾问，曾就职于 Twitter、Facebook 和 NOKIA。

## 本书介绍的内容

许多文章假设读者了解每一个术语的含义。事实是，许多人在遇到诸如变量、上下文、作用域、对象等术语时可能会困惑。

## 本书不包含的内容

书中的每一个术语都可能需要一整本书来详细描述其光辉、历史或“坑”。

## 调试

这是基础，因为每当我们编写代码时，都需要知道代码是成功还是失败。这种验证过程被称为“调试”，原因在于它通常通过大多数浏览器提供的“调试器”工具来完成。

环境无关性，这意味着它们可以在每个浏览器和服务器上运行。

每个代码示例都包含一些灰色的注释，我强烈建议你至少阅读一遍它们，然后再关注实际编程。

## comments (注释)

在编程中，注释是对代码本身有意义的描述。它们在代码执行期间会被忽略，可以是 `//` 单行注释，遇到新行时结束，或者是 `/* 多行注释 */`。

## operators (运算符)

如果你拿一个计算器，你可以在上面看到数字和算术运算。

在编程中，这基本上是一样的，有算术、比较、赋值、条件和其他操作。我们可以在任何控制台中直接使用它们。

```javascript
// let's do some math
1 + 2; // shows 3
3 * 5; // shows 15
1 - 2; // shows -1
```

在计算器中，等号 `=` 表示“显示结果”，而在 JavaScript 中它意味着“赋值结果”。你可以使用 `=` 符号来存储某些结果以便稍后重用。

```javascript
var result = 3 * 7; result; // shows 21
```

如果你想比较两个不同的值，可以使用三等运算符 `===`。

```javascript
2 === 2; // true → 当然，相同的数字，它等同于它自己
2 === 3; // false → 嗯，2 和 3 不同，所以它们不能相同
```

为了验证这两个值是不同的，你可以使用“非”版本。

```javascript
2 !== 2; // false → 2 是这些，所以它们不可能是不同的 
2 !== 3; // true → 当然 2 和 3 不同。它就是 2！
```

“非”运算符 `!` 可以通过反转其值来否定某些逻辑条件。例如，`!true === false`，反之亦然。

如果你想说明不同的值实际上是相同的，可以使用逻辑运算符。

```javascript
(4 + 5) === (5 + 4) && (2 * 3) === (3 * 2); // true → 交换律
```

书中后面有一个专门关于这些操作的章节，所以我们现在先继续关注术语。

## parenthesis (括号)

可以通过括号对不同的操作序列分组。这会立即变得更易读，使开发者的意图变得清晰。

例如，如果有人读取诸如 `2 * 3 + 4` 的操作，他们会认为结果是 10。实际上，你是想让 3 和 4 的和乘以 2，为了让你自己的眼睛和 JavaScript 程序解释器都看清楚，你应该写成 `2 * (3 + 4)`，这消除了对结果的所有疑虑。

括号通常简称为 *parens*，也用作函数语法的一部分，这将在后文中描述。

## brackets (中括号)

在 JavaScript 中有大括号 `{}`，或简称为 *braces*，以及方括号 `[]`。这些可以用来创建对象，在方括号的情况下，还可以访问它们的值。

```javascript
var obj = {hello: 'world'}; // 对对象的通用引用
var arr = ['a', 'b', 'c']; // 对 Array 对象的通用引用
arr[0]; // 显示字母 'a'
obj.hello; // "world"
// ↑ 也可以通过 obj['hello'] 访问
```

## references (引用)

引用就像一个指向特定值的符号链接。想象一张自拍照，照片可以被看作是对一个普通人的引用：你不需要让这个人出现在房间里就能看到她长什么样或她在做什么，照片就足够了。

## variables (变量)

变量通常是一个用于引用通用值的有意义的名字。回到自拍照的例子，`var myPhoto = new Selfie();` 创建了一个指向我的自拍的引用，名字是 `myPhoto`。我可以把它留给自己，像明信片一样发送出去，接收来自其他人的自拍，并随时重新给它赋值值。

```javascript
// 创建一个引用我自拍的变量
var myAvatar = new Selfie();
// ... 5 年后 ...

// 保存旧照片
// 通过使用新变量名 var oldMe = myAvatar;

// 然后拍一张新自拍
// 简单地将其重新赋值给同一个变量
myAvatar = new Selfie();
```

JavaScript 变量名的常用约定是 `var camelCase = anyValue;`，始终以小写开头，并最终通过大写字母将多个单词组合在一起。

如果复合变量名中包含单个字符或缩写，组合多个大写字母是可以的。

```javascript
// 常见命名约定示例
var thisIsAGoodNameForVariable = anyValue;
var result = loadSDK();
object.genericProperty = genericValue;
```

## constants (常量)

常量类似于变量，但只能创建和赋值一次。在现代 JavaScript 引擎中，可以通过 `const` 关键字显式创建。

```javascript
// 代替 var MY_CONSTANT = 'staticValue';
const MY_CONSTANT = 'staticValue';
// 它不会改变值 MY_CONSTANT = 'nope';
MY_CONSTANT; // 显示 "staticValue"
```

它们在大多数流行编程语言中的常用命名约定是：`EVERY-THING_IN_UPPER_CASE_WITH_UNDERSCORE_BETWEEN_WORDS`。

这类变量经常（但不是限于）用于描述永远不会改变且具有固定值（通常是为人知的）的数据。

## types (类型)

当引用一个值的变量被创建时，可以假设它有一个类型。回到自拍照的例子，`var myPhoto = new Selfie();` 例子，你可以说 `myPhoto` 的类型是“object”，它在某种程度上描述了你可以对它做什么：看它、分享它、丢弃它等。

- **boolean (布尔值)**：由两个可能的值表示：`true` 和 `false`。

- **number (数字)**：由整数表示，如 `0,1,2,-3`，浮点数如 `0.9,1.2,-1`，以及少数特殊情况如 `Infinity` 和 `NaN`。

- **string (字符串)**：由单引号或双引号内的任何内容表示：`'I am a string'` 和 `"so am I"` 都是有效的字符串。大多数现代 JavaScript 引擎也支持反引号包裹的字符串。

- **undefined (未定义)**：由值的缺失表示。默认情况下，有一个名为 `undefined` 的全局引用。

- **object (对象)**：主要由大括号 `{}` 或方括号 `[]` 表示。对象是键值对的容器。

```javascript
// tellMeSomething 是我们刚刚声明
// 函数的引用名
tellMeSomething; // 什么都没有发生（只是显示了函数本身）

// 要“执行”这个函数
// 我们需要使用括号 () 来调用它
tellMeSomething(); // 打印 'something'
```

如果你仔细观察，你会发现即使是 `console.log('something');` 这种操作也是调用了一个函数。然而，在这种情况下，`log` 函数是通过 `console` 对象的引用被调用的，而不是直接调用的，并且是使用“点符号”来访问的。

每当在点号之后调用函数时，该函数就可以被视为一个“方法”（method）。

## 函数声明 VS 函数表达式

定义函数有几种方式，每种方式可能或多或不方便。

例如，函数声明（function declaration）会创建一个在它所声明的“作用域”内随处可用的引用，即使在声明之前调用也可以的。

```javascript
// 即使在声明之前调用它
readyJack(); // 按照预期工作
```

```javascript
function readyJack() {
  console.log('I was born ready');
}
```

这可以帮助将代码组织在单独块中。

但如果在许多不同部分有许多声明，也可能会令人困惑。由于将一起声明所有需要的变量是一个良好的习惯，函数表达式（function expressions）可能更合适。

```javascript
var name = 'Jack';
// 通过 readyJack 引用的函数表达式
readyJack = function () {
  console.log(name + 'was just an expression'); 
};
```

就像每一个变量声明都应该以分号结尾一样，当表达式赋值给变量函数时，表达式也应该以分号结尾。如上例所示，函数声明不需要分号。记住：函数表达式在定义之前无法被执行。

## 命名函数表达式 (named function expressions)

为了方便我们自己的调试，给函数命名是一个良好的习惯，即使已经有一个函数表达式和对它的引用。

```javascript
var anonymous = function () {};
var named = function helloThere() {};
console.log(anonymous.name); // 空字符串
console.log(named.name); // 打印 'helloThere'
```

必须说，现代调试器足够智能可以识别出引用名，但了解你可以在运行时创建带有名称的函数表达式是有益的。

当你想要立即调用函数本身时，这特别方便。

* 过程也称为 IIFE：立即执行函数表达式（Immediately Invoked Function Expression）

```javascript
function areWeThereYet(tenSteps) {
  if (tenSteps === 0) {
    console.log('finally arrived');
  } 
  else {
    console.log('yet another step');
    // 使用函数名调用自己 // 传递减少后的计数
    areWeThereYet(tenSteps - 1);
  }
}
areWeThereYet(10); // 在这种情况下计数从 10 开始
```

## 作用域 (scope)

这个术语表示代码执行的边界。将其想象成宇宙星系的作用域，银河系是我们的太阳系作用域，太阳系是地球的作用域，地球是所有大陆的作用域，而对于每个大陆，我们将拥有国家、地区、城市、委员会，最后是你自己的房子——当你住在里面时，房子是你自己的作用域，而当你离开时，城市的其他部分就是你的作用域。

在 JavaScript 中，默认有一个全局作用域（global scope），你可以在其中定义函数和变量。然而，回到房子的比喻，你不希望每个邻居都知道你在家里所做的每一件事：你的家是你的地方，而在 JavaScript 中，函数是定义你自己的领地的方式，而不会被街道中间或其他任何地方（包括其他房子）发生的事情干扰或打扰。

```javascript
// 全局作用域在 JS 代码执行之前就开始（它已经存在了）
// 函数 `myHouse` 作用域在这里开始
function myHouse(sco, ped, args) {
  // 在 `myHouse` 内部定义变量使其仅在此处可用
  var myMess = 'my own room';
} // 函数 `myHouse` 作用域在此结束
typeof myHouse; // 是 'function' `myHouse`
typeof myMess; // 是 'undefined'，因为在这个作用域中它是未知的
```

## 私有和嵌套作用域 (private and nested scope)

由于可以在函数内部创建函数，因此也可以在已经私有的函数内部拥有私有作用域，就像房子里的房间一样。

要创建一个私有作用域，我们可以使用之前看到的 IIFE 方法，而不给函数表达式命名。

```javascript
// 匿名 IIFE
(function () {
  var myPrivateScope = 'a string value';
  console.log(typeof myPrivateScope); // 'string'
});
console.log(typeof myPrivateScope); // 'undefined'
```

通过拥有一个自调用的匿名函数表达式，你可以完全确定该函数外部的人无法干扰你的代码。此外，你还可以在其中定义其他函数，并创建嵌套作用域。

```javascript
(function (){
  var who = 'I am '
  var nestedExpression = function () { // 嵌套函数表达式作用域
    var nested = who + 'expression'; 
    return nested;
  };
  function nestedDeclaration() { 
    var nested = who + 'declaration'; 
    return nested;
  }
  console.log(nestedExpression());
  console.log(nestedDeclaration());
}());
// 嵌套函数声明
// 'I am an expression' // 'I am a declaration'
```

记重要的是，嵌套作用域始终可以访问外部变量，但反之则不然。这就是为什么在上例中，函数表达式和声明在执行时可以使用 `who`。然而，外部作用域无法到达在每个函数内部定义的变量：这些变量只能通过它们自己的作用域访问。我们想要使用作用域是因为……

## 上下文 (context)

每当函数被调用时，都可以通过自动可用的 `this` 引用引用其当前的执行上下文，该引用具有以下值之一：

- 全局程序上下文，在浏览器中称为 `window`，在服务器上称为 `global`

- 通过点符号调用函数的通用对象：`obj.method()`

- 通过 `.call`、`.apply` 等函数方法调用时的任意显值，包括 `undefined`

## 全局上下文 (global context)

如果你打开浏览器控制台或启动 node js，你可以通过编写 `console.log(this)` 或直接输入 `this` 来检查全局上下文。

每当你在全局定义变量或声明函数时，你也可以通过全局上下文引用这些变量，因为它们就像对象一样。

```javascript
// 在全局作用域中直接创建变量
globallyDefinedVariable = 'can everyone access me'; //可以通过全局对象访问
console.log(this.globallyDefinedVariable);
```

```javascript
// 全局创建函数时也是一样
function globallyDeclaredFunction() { return globallyDefinedVariable; }
console.log(globallyDeclaredFunction());
```

还可能在给引用赋值时简单地遗漏 `var` 关键字，从而无意中在通用函数内部定义全局变量。

```javascript
console.log(typeof a); // 'undefined'
function myFunction() {
  a = 123; // 代 var a = 123
}
myScope();
console.log(typeof a); // 'number'
console.log(a); // 123
```

```javascript
console.log(typeof a); // 'undefined'
function myScope() {
  'use strict'; // 局部作用域切换到严格模式
  var a = 123;
}

myScope(); // 显示 Error
console.log(typeof a); // 仍然是 'undefined'
```

不仅无法意外在全局作用域定义变量，而且在使用此指令时，执行上下文也将是 `undefined`，除非显式提供。

```javascript
// 在全局作用域定义
function whoIsThis() {
  'use strict';
  return this;
}
whoIsThis(); // undefined
this.whoIsThis(); // 全局上下文
```

## 方法上下文 (method context)

在 JavaScript 中，对象可以拥有任何类型的属性，函数也不例外。

```javascript
// 创建空对象
var obj = {};
// 将属性定义为函数表达式
obj.somePropertyName = function () {
  return this;
};
// 返回的上下文值是什么呢？让我们让我们通过调用 obj.somePropertyName 来找出
obj.somePropertyName(); // 正好是 obj 本身
```

当通过对象调用函数时，它会隐式地使用该对象作为当前的执行上下文。需要记住，任何函数都可以随时地附加到任何对象上，即使它没有被直接定义为该对象的属性。

```javascript
// 在此处某处定义的通用函数
function sayTheName() {
  console.log(this.name);
} // 通用对象
var me = {};
// 定义 name 属性，值为 'Andrea'
me.name = 'Andrea';
```

```javascript
// 将 sayTheName 挂载为 'whoAmI' 属性
me.whoAmI = sayTheName;
// 这样我们可以像方法一样调用它
me.whoAmI(); // 'Andrea'
```

尽管在运行时附加方法不是一个好主意，但我们可以借用任何类型的函数并将其作为不同对象的方法使用，这仍然是一个令人惊叹的特性。“为什么我们需要这个？”这是一个非常合理的问题，答案是：例如，每个项目集合并不一定像普通的 `Array` 那样拥有所有方法。在网上确实可以找到类似下面的代码示例：

```javascript
// 反例
var allNodes = document.querySelectorAll('*'); // 从空数组中借用 forEach 方法
allNodes.forEach = [].forEach;
// 使用该方法遍历所有节点
allNodes.forEach(function (node) {
  console.log(node.nodeName);
});
```

正如前面提到的，尽管可行，但修改并非自己创建的对象是一种非常粗劣的方法。例如，如果让某人坐我们我们闪闪的新车兜一风，我们不希望他们到处留下食物碎屑和脏东西。他们上车时那里并没有这些东西，为什么现在会有呢！

好消息是：有更好、更干净的方法通过提供上下文来调用函数。

## 通过 call 或 apply 调用函数

正如在 *types* 段落中特别描述的那样，函数是可以执行的特殊对象。就像任何对象一样，函数也可以拥有属性，因此拥有方法。

任何函数最常用的方法是 `.call()` 和 `.apply()`，它们的区别在于：`.call()` 接受任意数量的参数进行传递，而 `.apply()` 只接受一个数组作为调用参数。

```javascript
// 三个打印某些信息的函数
function fnWithNoArguments() {
  console.log('nothing to do here');
}
function fnWithOneArgument(first) {
  console.log('received', first);
}
function fnWithTwoArguments(a, b) {
  console.log('received', a, b);
}
// 使用调用并暂时忽略第一个上下文值，使用 null
fnWithNoArguments.call(null);
fnWithOneArgument.call(null, 'some value');
fnWithTwoArguments.call(null, 'first value', 'second value');
```

```javascript
// 要使用 `apply`，你需要一个或多个数组
var myArray = [];
var arrayWithOneArgument = ['any value'];
var arrayWithTwoArguments = ['1st', '2nd'];
```

```javascript
// 结果与你通过 .call 打印的相同
fnWithNoArguments.apply(null, myArray);
fnWithOneArgument.apply(null, arrayWithOneArgument);
fnWithTwoArguments.apply(null, arrayWithTwoArguments);
```

记住 `.call` 和 `.apply` 区别的小贴士：“apply”一词以 “a” 开头，Array 也是；-)

## 显式上下文 (explicit context)

现在这两种方法的区别已经很清楚了，是时候理解它们的强大之处了。你还记得上一页的集合吗？

```javascript
var allNodes = document.querySelectorAll('*'); // 一种粗劣且不一定可行的方法
// allNodes.forEach = [].forEach;

// 这是借用并调用 ArrayEach 方法的方法
[].forEach.call(allNodes, function (node) {
  console.log(node.nodeName);
});
```

通过其 `.call` 方法调用以下函数，并将第一个上下文参数传递任何将作为 `this` 返回的值。

```javascript
function whoIsIt() {
  'use strict';
  return this;
}
whoIsIt.call(null);
whoIsIt.call(123);
whoIsIt.call(['a', 'b', 'c']);
```

## 参数 (arguments)

每当函数被调用时，它可能会接收从零个到多个参数，每个参数也是一个对象。

## for 循环 (for loop)

与之前的 `while(condition)...` 示例类似，`for` 循环也会一直执行，直到其条件不再满足。然而，它的逻辑顺序略有不同，描述如下：

（请注意，以下内容不是有效的 JavaScript 代码，仅为文本描述）

```
for (
  [1] 一个或多个变量声明，用逗号隔开 ;
  第一个分号 —> 
  [2] 需要满足的条件 ; ◄ 第二个分号
  [4] 更新更新的更改
) {
  [3] 对当前值进行某些操作。请注意，这实际上是 for 循环流的第三部分。第 4 部分紧随其后
}
```

考虑到之前的 `while` 循环示例，你可以在下面的 `for` 循环中执行完全相同的过程：

```javascript
for (var index = 0, size = list.length; index < size; index = index + 1) { 
  console.log(list[index]);
}
```

非常重要的一点是，如果条件不满足，`for` 循环的第 3 和第 4 部分都不会执行。

```javascript
// 空列表，其长度为 0
var list = [];
for (var
  i = 0;
  i < list.length; // 条件永远不会满足 i = i + 1
){
  console.log(i);
}
console.log(i);
```

// 如果条件退出循环，这种情况不会发生

//  输出 0 是因为第 4 部分 (i = i + 1) 从未发生过

只要你向列表中放入至少一个项目，条件就会满足（至少一次），你会发现循环后 `i` 的值是 1 而不是 0。

## 递增运算符 ++ (incremental++ operator)

通常常见使用 `+` 号来增加整数，而不是将变量重新赋值为自身加 1。相应，下面的示例是 `for` 循环通常的写法：

```javascript
for (var i = 0; i < collection.length; i++) { // 对 collection[i] 执行某些操作
}
```

`++` 运算符既可以用在变量之前，也可以在变量之后。在两种情况下，变量都会增加，但它立即返回的值非常不同。

```javascript
// 使用 ++ 作为后缀（也称为后增）
var num = 0;
var numPlusPlus = num++;
console.log(numPlusPlus); // 0, 赋值时 num 还没有增加
console.log(num); // 1, 因为在 num++ 之后它被增加了了
```

```javascript
// 使用 ++ 作为前缀（也称为前增）
var num = 0;
var plusPlusNum = ++num;
console.log(plusPlusNum); // 1, 赋值时，num 已经增加了
console.log(num); // 1, ++num 增加了并将其返回为 1
```

并没有特定的理由去偏于其中一种方式，虽然通常更偏于使用 `num++`，但 `++num` 也可以作为遍历包含至少 2 个项目的集合的示例：

```javascript
var i = 0;
while (++i < list.length) { compare(list[i-1], list[i]); };
```

使用 `-` 运算符将整数减少 1（递减）也是可能的，模拟了 `num = num - 1` 的操作。

所有已针对 `++` 运算符提到的内容，包括作为前缀或后缀使用时的区别，同样适用于 `-` 减运算符。

## 数组方法 (Array methods)

在 JavaScript 中，每个数组都带有一些特殊方法，用于更改、复制、更新或迭代其项目。方法不仅看起来比循环更整洁，而且借用它们来遍历任何类型的集合（包括参数）也是很常见的做法。

### array.forEach(callback, context)

这可能是“最接近循环”的数组方法，它的工作原理如下：

```javascript
['a', 'b', 'c'].forEach(function (value, index, array) { // 函数将被调用 array.length 次 // 在 ['a', 'b', 'c'] 列表的情况下意味着三次
  console.log(index, value);
  // 0, 'a'
  // 1, 'b'
  // 2, 'c'
});
```

匿名函数被调用三次，默认接收这些参数。

让我们用旧的循环语法来重构 `forEach` 发生了了什么。

```javascript
for (var
  list = ['a', 'b', 'c'],
  context, // 除非指定，否则 forEach 的 context 为 undefined
  callback = function (value, index, array) {
    console.log(index, value);
  },
  i = 0;
  i < list.length;
  i++
) {
  // 记录之前通过 forEach 记录的序列
  callback.call(context, list[i], i, list);
}
```

`context`（上下文）是一个很少使用的特性，但在某些情况下非常有用。由于某些集合可能没有 `forEach` 方法，你可以借用它的迭代能力。

```javascript
// 如果未找到，返回 -1
alphabet.indexOf(123); // -1
```

在最新的规范中，`array.includes(value, fromIndex)` 返回布尔值，表示该值是否存在。

实际上有几十个数组方法。所有方法在 Mozilla 开发者网络（MDN）的 `Array.prototype`¹ 节目下都通过大量的示例和用法进行了描述，该节目是包含了每个数组继承的所有方法和行为的对象。

> ¹https://developer.mozilla.org/Web/docs/JavaScript/Reference/Global_Objects/Array/prototype

## 原型与原型继承 (prototype and prototypal inheritance)

当一个新变量的值是一个对象、数组或函数时，它默认带有一些没有人显式赋值的方法：这些方法已经是核心功能的一部分；它们是从另一个对象继承来的属性和方法。

从其他对象继承的方法有两种两种机制：通过直接链接，或通过用于初始化对象并设置其继承关系的特殊函数。对象之间显式继承属性的第一种直接链接方式如下：

```javascript
// 被用作 `person` 的通用对象 // 它有两个属性：`name` 和 `age` // 以及一个负责增加年龄的方法 var person = {
  name : 'anonymous',
  age: 0,
  birthday: function () {
    this.age++;
  }
}
```

```javascript
// 这就是我，继承了
// 属性和方法
// 来自 `person` 对象
// 使用全局始终可用的 // `Object` “构造函数”（后文将描述） var me = Object.create(person);
```

```javascript
me.name = 'Andrea';
console.log(me); // {name: 'Andrea'}
console.log(person); // {name: 'anonymous', age: 0}
```

通常，浏览器控制台只会显示对象的“自身”（own）属性，而忽略继承的属性。这就是为什么记录变量 `me` 时，你只看到 `name` 属性，即使里面还有其他内容。

## genericA.isPrototypeOf(genericB) → 布尔值

在 JavaScript 中，默认可用的方法之一是 `isPrototypeOf()`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量 `person` 和 `me` 作示例，你可以假设 `person.isPrototypeOf(me)` 调用的结果将为 `true`。但这到底意味着什么？

```javascript
// 控制台是如何显示 me 的？
console.log(me); // {name:'Andrea'}
// 但 `me` 也有 `age` 吗？
me.age; // 0 → 是，`age` 是继承自 `person` 的
// 那么 `me` 也有 `birthday` 方法吗？
```

```javascript
typeof me.birthday; //'function' -> 是，继承自 `person`
// 如果我们把 `birthday` 作为 `me` 的方法来调用会发生什么？me.birthday();
// `birthday` 的调用是如何影响 `me` 的？
console.log(me); // {name: "Andrea", age: 1}
```

```javascript
// 突然之间，▲ “野的年龄出现了” // me 的 birthday
// 影响了 `person` 吗？
console.log(person); // {name: "anonymous", age: 0} -> 没有，
一切正常
```

方法上下文（context）章节的小要回顾：当我们通过点符号语法从一个通用对象调用函数时，该对象将临时成为该函数的执行上下文。

这并不意味着 `person` 和 `me` 都拥有 `birthday` 方法，而是意味着 `me` 将临时执行 `person.birthday`，就像它是自己的方法一样。

```javascript
// `root` 是一个拥有方法的对象 // 它简单返回
// 当前执行上下文 var root = {method: function () {
  return this;
}};
// `child` 是一个继承自 `root` 的对象 var child =
Object.create(root);
```

```javascript
// 如果通过 `root` 执行 `root.method`，它将返回
`root` 本身 // 因为它是隐式执行上下文
console.log(root.method) === root); // true -> 因为
`this` 在这里是 `root`
```

```javascript
// 但我们通过 `child` 引用调用继承的方法 //
// 它返回当前的执行上下文
// 即 `child`，而不是 `root` console.log(child.method) ===
child); //true -> 因为现在 `this` 是 `child` 
```

```javascript
// 这是因为我们正在隐式地执行以下操作：
root.method.call(child); // 这将使用 `child` 作为 `this`
```

一旦你理解了方法不需要直接挂载或赋值为对象的属性，而是可以简单地继承，那么原型继承的本质就变得清晰了：它是不同对象之间一种隐式的、“不可见”的链。

## Object.prototype

默认情况下，每个 JavaScript 对象都继承自 `Object.prototype` 的属性，它实际上也是一个对象，是为所有其他对象提供基本方法的那个。

```javascript
// 创建一个空对象 var justEmpty = {};
// 这个对象可以被表示为字符串吗？
console.log(justEmpty.toString()); // '/[object Object]'
// 但是谁把那个 `toString` 方法放入你的空对象的？ 
console.log(justEmpty.toString == Object.prototype.toString()); // true
// 这是因为这两个对象之间存在原型链 吗？ 
console.log(Object.prototype.isPrototypeOf(justEmpty)); // true
```

由于每个对象在根部都有一个 `toString()` 方法，你可能认为无论使用哪个变量，它的行为都是样的，对吧？

不不。继承某些属性或方法并不意味着它会以相同的方式运行，无论你使用哪个变量。

事实上，继承某些属性或方法并不会阻止“重写”，因此 `toString` 方法可能被重定义。`Array.prototype` 同样继承自 `Object.prototype`，并且它重定义了 `toString` 方法以返回转换为字符串的数值。

```javascript
// 包含 7, 11, 2 的数字 arr = [7, 11, 2];
```

```javascript
// 继承自 Array.prototype 的方法
// 而不是 Object.prototype。
console.log(arr.toString === Object.prototype.toString); // false
```

```javascript
// 但方法继承自根
console.log(Array.isArray); // true
```

```javascript
// 它是怎样的？// 是字符串 '[7,11,2]'
```

## object.toString() -> string

位于原型链的根部具有某些优势。例如，即使数组继承了不同的 `toString` 方法，你也可以借用根部的方法来看看它有什么不同。

```javascript
var arr = ['a', 'b', 'c', 'd'];
// 借用 Array.prototype 的方法
Array.prototype.toString.call(arr), // 'a,b,c,d'
// 这确实与以下操作等效
arr.toString(), // 'a,b,c,d'
// 但当你使用原始方法会发生什么？
Object.prototype.toString.call(arr) // '[object Array]'
```

`Object.prototype.toString` 方法是一个非常特殊的方法：它可以告诉你处理的是通用对象还是“原生”对象。

## native

在 JavaScript 中，这个术语指的是所有由环境提供而非库提供的变量、对象、函数、方法、类或构造函数。来自原生类的对象一旦作为 `Object.prototype.toString` 方法的上下文使用时，就会暴露它们的“类”名称。

```javascript
// 为了演示目的直接引用该方法
var toString = Object.prototype.toString;

// 这样就可以方便地多次调用
console.log(
  toString.call({}),
  toString.call([]),
  toString.call(""),
  toString.call(0),
  toString.call(true),
  toString.call(null),
  toString.call(undefined),
  toString.call(function () {}),
  toString.call(JSON),
  toString.call(Math),
  toString.call(new Date()),
);
```

```javascript
// ['object Object'] // ['object Array'] // ['object String'] // ['object Number'] // ['object Boolean'] // ['object Null']
// ['object Undefined'] // ['object Function'] // ['object JSON']
// ['object Math']
// ['object Date']
```

`toString.call(this.window || global);` // ['object global']

在历史上，与许多其他情况不同，`Object.prototype.toString` 方法在不同平台上的实现都是一致且可靠的。

## class

在大多数现代 JavaScript 实现中，`class` 是一个非常特殊的关键字，用于定义通过其名称创建的每个对象的行为。下面是一个现代 JS 语法的示例 * 该语法可能在旧的浏览器或 JS 引擎中无法工作 *

```javascript
// 定义一个通用的矩形行为
class Rectangle {
  // 每当创建一个新的 Rectangle(w, h) 时，此方法都会被隐式地调用
  constructor(width, height) {
    // `this` 的调用上下文将是
    // 新创建的实例
    // 你将接收到的参数赋值给它们以便稍后使用
    this.width = width;
    this.height = height;
  }
}
// ← 注意，类定义中的方法之间不需要逗号
```

```javascript
// 定义包含一个 `area()` 方法
// 该方法将被每个 `new Rectangle` 继承
area() {
  // 执行上下文将是调用 area 方法的 `Rectangle` 实例
  // 每个实例都拥有 `width` 和 `height` 属性，
  // 这些属性是在创建时分配的
  return this.width * this.height;
}
// 注意：这里也不需要逗号
```

// Rectangle 实例示例

```javascript
var myDesk = new Rectangle(5, 3);

console.log(myDesk.area()); // 因为 5 * 3 所以是 15 // 另一个引用

var myTV = new Rectangle(16, 9);

console.log(myTV.area()); // 144
```

每当在 JavaScript 中使用特殊关键字 `new` 时，引擎期望后面紧跟一个类或“构造函数”，以便创建一个与构造函数自身的原型相连的对象。

## constructor

每当你声明一个函数时，引擎都会自动提供它的原型对象。

```javascript
function justAFunction() { /* * 并且它可以做任何想做的事 */ }

console.log(
  // 谁把这个对象放在这里的
  justAFunction.prototype, // {} {} // 它是继承自
  // 全局 Function 吗？justAFunction.prototype === Function.type.prototype // false
);
```

通常，每个 JavaScript 函数都可以用于创建与其自身的原型相连的对象，该原型是一个只包含一个属性的对象：`constructor`

```javascript
function linkMe() {} // 简单函数
// 一旦我们通过 new 调用它，linkMe 就会变得特殊了
var obj = new linkMe();
```

```javascript
console.log(
  // 我们创建了一个原型链
  linkMe.prototype.isPrototypeOf(obj), // true // 默认情况下
  // 我们也继承了构造函数 // 除了
  // 函数 linkMe 之外没有别的 obj.constructor === linkMe, //
  true // 这种构造函数实际上被继承了 // 因为它是
  // linkMe.prototype 自身的一部分 linkMe.prototype.constructor === linkMe // true
);
```

回到你之前看过的 `Object.create(fromAnotherObject)` 机制，你可以使用函数来创建新实例，如下操作所示：

```javascript
function Shape() {} // 仅用于继承其原型的虚哑函数
// 使用 Shape.prototype 创建链 var oneShape =
Object.create(Shape.prototype);
// 等同于创建一个新的 Shape var anotherShape =
new Shape();
```

```javascript
console.log(
  Shape.prototype.isPrototypeOf(oneShape), // true
  Shape.prototype.isPrototypeOf(anotherShape) // true
);
```

这两种方法之间最大的区别在于，使用 `new Shape()` 会不可避免地调用 shape 函数，并隐式地使用新创建的实例作为执行上下文。

这反过来例如会赋予我们我们在其中进行一些设置的能力。

```javascript
// 按照命名规范，类使用 PascalCase（首字母大写）
function Person(name) {
  this.name = name;
}
```

```javascript
var me = new Person('Andrea'); // 类的方式
```

```javascript
// 等效且显式的方式
var me = Object.create(Person.prototype); // 过程化方式 // 调用 Person 来设置 me.name
// 否则将完全没有 name 属性 Person call(me, 'Andrea');
```

在任何种情况下，通过 `Person` 或从其原型创建的通用对象，都继承一个 `constructor` 属性，该属性本身就是 `Person`，就像对于通用函数来说一样。

总结一下：当我们谈论 JavaScript 中的构造函数时，指的是一种特殊方法，一旦任何实例通过 `new` 关键字创建，它就会隐式地初始化该实例。

## instance

每当对象被创建时，通过 `Person` 或从其原型创建的通用对象，都继承一个 `constructor` 属性，该属性本身就是 `Person`，就像对于通用函数来说一样。

总结一下：当我们谈论 JavaScript 中的构造函数时，指的是一种特殊方法，一旦任何实例通过 `new` 关键字创建，它就会隐式地初始化该实例。

每当对象被创建时，通过 `Person` 或从其原型创建的通用对象，都继承一个 `constructor` 属性，该属性本身就是 `Person`，就像对于通用函数来说一样。

总结一下：当我们谈论 JavaScript 中的构造函数时，指的是一种特殊方法，一旦任何实例通过 `new` 关键字创建，它就会隐式地初始化该实例。

每当对象被创建时，通过 `Person` 或从其原型创建的通用对象，都继承一个 `constructor` 属性，该属性本身就是 `Person`，就像对于通用函数来说一样。

总结一下：当我们谈论 JavaScript 中的构造函数时，指的是一种特殊方法，一旦任何实例通过 `new` 关键字创建，它就会隐式地初始化该实例。

每当对象被创建时，通过 `Person` 或从其原型创建的通用对象，都继承一个 `constructor` 属性，该属性本身就是 `Person`，就像对于通用函数来说一样。

总结一下：当我们谈论 JavaScript 中的构造函数时，指的是一种特殊方法，一旦任何实例通过 `new` 关键字创建，它就会隐式地初始化该实例。

（此处由于原文存在大量重复，已按要求翻译并保留重复结构逻辑）

... 继承一个 `constructor` 属性，该属性本身就是 `Person`，就像对于通用函数来说一样。

总结一下：当我们谈论 JavaScript 中的构造函数时，指的是一种特殊方法，一旦任何实例通过 `new` 关键字创建，它就会隐式地初始化该实例。

每当对象被创建时，

- Q: "这是预期的"

- A1: "这是预期的"

- A2: "这是预期的"

...（后续重复内容略）

```javascript
object.hasOwnProperty(name) -> boolean
```

如何判断一个属性（或方法）是否被继承了？答案在 `hasOwnProperty` 方法中，只有当该属性是自身的（即直接附加的，而不是继承的）时，它才会返回 `true`。

```javascript
var obj = {prop: 123};
console.log(
  obj.hasOwnProperty('prop'), // true -> 我们定义的它
  obj.hasOwnProperty('toString'), // false -> 是继承的
  Object.prototype.hasOwnProperty('toString') // true -> 它是自身的
);
```

如果你在想为什么需要了解所有这些方法，答案是因为原型继承既可能是强大的，又是危险的。

例如，设置像 `obj.toString.prop = 'value';` 这样的属性不会简单地影响该对象引用的 `toString` 方法，相反，它会影响通用继承的 `toString` 方法，因为每当你调用一个未重定义的通用 `toString()` 时，访问的都是它。

## 共享属性 

在特别讨论类和原型时，以及当存在私有作用域和某些私有引用时，“共享”一词描述的是一个对象或函数被许多不同的地方、为了相似的用途以及通过许多对象使用的事实。

```javascript
function SharedData() {}
SharedData.prototype.data = {}; // 将被继承
var one = new SharedData(); // 只是两个不同的实例
var two = new SharedData(); // 继承自 SharedData.prototype 
// 注意：括号是可选的。
one.data.test = 'one check, one check';
```

```javascript
console.log(
  // 之前的操作影响了 `two.data` 吗？
  two.data.test, // 'one check, one check'
  // 那是因为 `one` 和 `two` 共享相同的数据 吗？
  one.data === two.data // true -> 它们是完全相同的引用
);
```

上面的示例是现代 JavaScript 类语法不允许属性的定义与方法的的定义有所区别的原因之一，唯一的例外是“get值器”（getters）和“设置器”（setters），它们是具有“隐式调用”能力的特殊类型的方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是执行它的最佳地方。

```javascript
function NotSharedData() {
  this.data = {}; // ← 创建实例属性的正确位置
}
```

```javascript
var one = new NotSharedData();
var two = new NotSharedData();
one.data.test = 'one check, one check';
```

```javascript
console.log(
  // 之前的操作影响了 `two.data` 
  two.data.test, // undefined
  // 那是因为 `one` 和 `two` 共享相同的数据 吗？
  one.data === two.data // -> 每个实例都有不同的数据
);
```

为了比较，在现代环境中，上面的类看起来如下：

```javascript
class NotSharedData { constructor() { this.data = {}; }; }
```

## getters 和 setters

如果有人问“现在几点？”，我们必须在回答之前检查我们的手表、手机或“我们的经线”，因为我们没有持续地跟踪时间。

比喻地说，每当我们访问数组的 `.length` 属性时，都会发生类似的情况：它将计算此时有多少个项目，并将计数作为整数返回。同样，就像我们可以给手表设置时间一样，我们也可以设置数组的长度。但在那种情况下会发生什么？

```javascript
var arr = ['a', 'b', 'c']; console.log(arr); // 'a,b,c'
// 它计算它自己的项目并返回 3 
console.log(arr.length);
// 如果我们设置了长度
arr.length = 2;

console.log(arr); // 'a,b' -> 我们丢失了索引 3 的 'c'
console.log(arr.length); // 2 -> 我们确实丢失了 'c'

arr.length = 5; // 即使我们再次设置了长度
console.log(arr); // 'a,b' 或 'a,b,<3>
console.log(arr.length); // 5 -> 索引 2,3,4 是 undefined
```

设置长度看起来是一个透明的操作。然而，事实是，在背后发生了其他事情！

如果你熟悉网页，你可能知道像 `textContent` 和 `innerHTML`（其中 el 是任何 DOM 元素）这样的属性一旦修改，可能会影响整个页面的内容。

所有这些“魔法”属性和行为之所以可能，是因为 getters 和 setters。它们与通用方法不同，但你不需要显式地调用它们。

```javascript
var me = { // 嘿，又是 me _
  name: 'Andrea',
  realAge: 37,
  birthday: function () { // 我可以增长
    this.realAge++;
    console.log('Happy birthday' + this.name);
  },
  // getters 和 setters 有特殊的语法
  get age() { return this.realAge; }, // 如果你问我的年龄，我会告诉你
  set age(newAge) { // 如果你尝试设置它...
    console.warn('我恐怕我无法更改它');
  }
};
```

## try catch finally

每当程序执行时，可能会发生许多类型的错误。有些错误是可以预期的，而有些错误可能是致命的。计算机历史上大多数为人知的致命错误就是“真理冥想”（guru meditation）和“蓝屏死机”，它们曾出现在老老的 Commodore Amiga 或 Windows 操作系统中。

我们绝对不需要尝试去复制一个致命错误，特别是因为我们实际上希望它永远不会发生。然而，我们可以做的是尝试防止那些会中断我们的应用程序并在完全不知道发生了什么的情况下的情况下退出的错误。

`try/catch/finally` 语句为我们提供了一种处理预期的可能发生的错误的方法，同时也提供了一种生成错误的方法，并期望其他人做出相应的反应。

```javascript
// 检查可能不存在的引用可以被调用
try {
  iAintEvenDefined();
} catch(errorObject) {
  console.warn(errorObject.message);
}
// 注意 finally 是可选的
```

```javascript
// 创建一个会抛出错误的属性
var me = Object.defineProperty({}, 'name', {
  enumerable: true,
  get: function () { return 'Andrea'; },
  set: function () {
    throw new Error('I already have a name');
  } // throw 是用于通知程序发生 Error 的关键字
});

console.log(me.name); // Andrea
try {
  me.name = 'Robert';
} catch (whatHappened) {
  console.warn(whatHappened);
} finally {
  console.log('Hello ' + me.name); // 'Hello Andrea'
}
```

过度使用这些机制很少是一个好主意。在周围有太多的 `try/catch` 语句并不意味着代码更安全或对错误产生免疫。相反，它可能表明我们对可能出现的问题完全没有控制，甚至更糟糕，完全不知道有多少事情可能出错。我们有更好的方法来控制我们的应用程序，而且此外，`try/catch` 语句还会显著减慢代码的执行。总结来说：谨慎地使用此功能，仅在必要时使用，并结合常识。

错误对象有一个 `message` 属性，它是一个字符串，包含了在创建 `new Error("info")` 对象时传递的信息。

## 什么描述符对应什么

有多种定义属性的方法，既方便又让人困惑。当涉及到描述符时，有很多小问题可以讨论，但最好遵循 JavaScript 核心中提供的常用约定。

例如，每个通用对象的属性赋值都将是一个可写的、可配置的且枚举的描述符，其值将完全是提供的值。

## 常用属性描述符

```javascript
var me = {name: 'Andrea'};
me.age = 37;
```

`name` 和 `age` 属性将具有类似的描述符。下面你可以看到 `name` 的描述符：

```javascript
// me['name'] 属性描述符的表示 
{
  configurable: true, enumerable: true, writable: true, value: 
  'Andrea'
}
```

当你设置像 `name` 或 `age` 这样的通用属性时，使用繁琐的 `Object.defineProperty` 方法实际上毫无意义。特别是所有的默认配置都是 `false` 而不是 `true`，而且不需要输入那么多！

## 常用类和原生方法描述符

虽然数据属性（如名称或年龄）通常是那些迭代、收集或操作的对象，但在我们的路径中出现方法通常并不方便。特别是当使用实例时，所有方法都是继承的，你并不希望它们出现在你的 `for/in` 循环中。没有必要知道每个对象都会有一个 `toString`。

因此，JavaScript 中提供的所有原生方法都可以描述如下：

```javascript
// 原生 Object.prototype['toString'] 描述符的表示
{
  configurable: true,
  enumerable: false, // ← 永远不会出现在 for/in 循环中
  writable: true,
  value: function toString() { [native code] }
}
```

原生描述符是可配置和可写的实际上是很幸运的，这意味着它们在需要时可以被重新赋值和修复。

## 常用防御性方法描述符

如果我们为了自己的目的创建一个类，我们可能希望确保它的方法在应用程序执行期间无法在其他地方修改。

在这种情况下，我们可能希望直接在原型中设置方法，如下：

```javascript
// 在类或函数原型中直接定义属性方法
Object.defineProperty(Constructor.prototype, 'method', {
  // 默认值 // enumerable: false, configurable: false, writable: false 
  // 之后无法补丁或更改此方法
  value: function () { /*...*/ }
});
```

## 常用懒加载属性描述符

当我们讨论懒属性（lazy properties）时，指的是那些只有在我们第一次需要它们之后才会获得预期值的属性。想象我们要买一辆车。默认情况下，它带有许多功能（属性），但我们可以要求更多的属性。在纸面上，汽车有一个连接我们设备的 USB 端口，但只有当我们要求时它才会被配置，而不是默认如此。

```javascript
class CarOrder {
  constructor(chosenColor) {
    // color 是在汽车创建期间设置的自有属性
    this.color = chosenColor;
  }

  // 作为懒属性的 usbConnector
  get usbConnector() {
    // 第一次时按需配置
    Object.defineProperty(
      this,
      'usbConnector',
      {
        configurable: true,
        value: 'connected'
      }
    );
    return this.usbConnector;
  }
}
```

我们需要使用 `defineProperty` 来配置懒描述符的原因是，如果我们尝试直接设置 `this.usbConnector = {}`，我们将不可避免地导致 `CarOrder` 类中已定义的设置器（setter）。此外，如果我们将来能够更改或替换它，我们应该将其设为可配置的。

关于描述符的最后一个重要信息是，你不仅可以设置它们，还可以随时检索它们。让我们尝试玩玩这个，验证我们到为止所学的所有内容。

```javascript
// 对最访问内容的某些检查
console.log(Object.getOwnPropertyDescriptor(Object, 'prototype'));
console.log(Object.getOwnPropertyDescriptor(window || global, 'toString'));
console.log(Object.getOwnPropertyDescriptor({name: 'Robert'}, 'name'));
```

## delete

当存在可配置的属性时，我们不仅再次使用 `defineProperty` 来更改它的描述符，还可以使用 `delete` 从对象中删除该属性。

```javascript
// 还记得吗？默认情况下所有属性都被定义为可配置的
var me = {name: 'Andrea'};

delete me.name; // true

'name' in me; // false

console.log(me.name); // undefined
```

返回的布尔值表示：要么没有要做，因此该属性可以没有问题地重新赋值给该对象，要么该属性存在但被删除了。记住：只有当自有属性是不可配置且无法删除时，`delete` 返回 `false`。

## Object.getOwnPropertyNames(obj) → 所有名称数组

我们已经提到过 `object.hasOwnProperty(propName)`，但我们如何获取直接定义在通用对象上的属性呢？

```javascript
// 可能我不想告诉所有人我的年龄
var me = { name: 'Andrea' };

Object.defineProperties(me, { age: { writable: true, value: 37 } });

for (var k in me) console.log(k, me[k]);

// 上述输出了 `name` `Andrea` ... 但年龄呢？

console.log(Object.getOwnPropertyNames(me)); // ['name', 'age']
```

## Object.defineProperties(obj, descriptors) → obj

`Object.defineProperties` 的复数版本某种简化了多个描述符的赋值，因为它需要的输入更少（这是一个加分项！）。

```javascript
var me = {};

Object.defineProperties(me, {

  name: {enumerable: true, value: 'Andrea'},

  age: {enumerable: true, value: 37}

});
```

一旦有一种方法可以检索对象的所有命名属性及其描述符，我们就拥有了分析任何类型对象所需的一切。

## Object.keys(obj) → 自身可枚举属性名的数组

这个“公共”方法与 `Object.getOwnPropertyNames` 类似，但它返回的是对象自身可枚举属性的数组。

## 公共与公共静态 (public and public static)

我们一直在使用如 `Object.keys` 等方法，这些方法通过全局可用的 `Object` 类暴露。在大多数原生类中也有其他方法。

`Array.isArray(obj)`、`String.fromCodePoint(0x1F4A9)`、`Number.isNaN(0/0)`，仅列举几个。
这些方法与其所属的构造函数有关。我们可以用老办法自己定义类似的“静态”方法。

```javascript
function Rectangle(w, h) {
  this.width = w;
  this.height = h;
}
```

// 记住：函数就像对象

```javascript
Rectangle.isSquare = function (instance) {
  return instance.width === instance.height;
};
```

```javascript
// let's test two different rectangles var spongeBob = new Rectangle(2, 3); spongeBob.pants = new Rectangle(2, 2);
```

```javascript
// invoke the Rectangle.isSquare
console.log(Rectangle.isSquare(spongeBob)); // false
console.log(Rectangle.isSquare(spongeBob.pants)); // true
```

在大多数更新的 JavaScript 引擎中，你实际上有一个特殊的静态属性用于为此。

```javascript
class Rectangle {
  static isSquare(instance) {
    return instance.width === instance.height;
  }
  constructor(w, h) {
    this.width = w;
    this.height = h;
  }
}
```

`Rectangle.isSquare` 方法具有以下特点：

- 它不被继承，但可以通过 `Rectangle` 构造函数公开访问。
- 它是静态的，也就是说，不期望在任何执行上下文中使用或调用。我们甚至可以写 `Rectangle.isSquare.call(null, spongeBob)`，如果该实例是正方形，它仍然返回 `true`。完全不涉及此上下文！

后者的条件对于每个公共静态函数都是相同的。例如，`Object.keys` 执行不需要 `Object` 上下文，它也不被继承。

```javascript
var keys = Object.keys; // 公共静态 Object.key 函数快捷方式
keys({a,'a'}); // 这样我们以后可以直接使用它
```

## extends (扩展)

继承之旅始于讨论对象继承其他对象。现在它结束于讨论类扩展其他类。没有理由惊慌，这只是对以下问题的简短回答：

- Q：“什么是 Square（正方形）？”
- A1：“它是一个扩展 Rectangle（矩形）的类”
- A2：“它是一个原型直接继承自 `Rectangle.prototype` 的类”

对象可以继承自原型的数量没有具体的限制，但只有一个直接的“扩展”，这在 JavaScript 中只可以在两个类之间实现。

因此，当我们使用“扩展”（extend）一词时，我们只能指的是一种非常特定的关系。

```javascript
// a Rectangle 构造函数
function Rectangle(w, h) {
  this.width = w;
  this.height = h;
}

// ... with an area getter
Object.defineProperty(Rectangle.prototype, 'area', {
  get: function () {
    return this.width * this.height;
  }
});
```

```javascript
// a Square 构造函数
function Square(size) {
  // invoke the "super" (parent)构造函数
  // 它将设置我们当前的实例上下文
  Rectangle.call(this, size, size);
}

// here Square extends Rectangle through its prototype
Square.prototype = Object.create(Rectangle.prototype); var twoXtwo = new Square(2);

console.log(twoXtwo.area); // 4 -> 'cause 2 * 2 == 4 ^_;
```

## super

在面向对象编程中，每当出现 super 一词（有时是 parent）时，它指的是当前执行所继承的最近祖先类。

这是一个特殊的关键字，绝不应该在通用类方法之外使用。它曾经是一个保留字，遇到它可能会破坏 JS 应用程序。

在 ECMAScript 2015 时代，在 `class` 关键字从保留字状态提升为未使用状态之前，只有一些库使用此关键字作为属性，以快捷访问从继承的原型提供的任何内容。

但如今，在现实中看到它的用法非常常见。

```javascript
// the class Rectangle in ES6 -> a.k.a. ES2015 class Rectangle
{
  constructor(w, h) {
    this.width = w;
    this.height = h;
  }
  get area() {
    return this.width * this.height;
  }
}
```



// how we use the `extends` keyword now

```javascript
class Square extends Rectangle { 
  constructor(size) {
    super(size, size);
  }
}

var twoXtwo = new Square(2);
console.log(twoXtwo.area); // 4
```

记住，如果你需要调用不是构造函数的 `super` 方法，你需要通过点符号来访问它，例如：`super.calculateArea()`。

`Rectangle.isSquare` 方法具有以下特点：

- 它不被继承，但可以通过 `Rectangle` 构造函数公开访问。
- 它是静态的，也就是说，不期望在任何执行上下文中使用或调用。我们甚至可以写 `Rectangle.isSquare.call(null, spongeBob)`，如果该实例是正方形，它仍然返回 `true`。完全不涉及此上下文！

后者的条件对于每个公共静态函数都是相同的。例如，`Object.keys` 执行不需要 `Object` 上下文，它也不被继承。

```javascript
var keys = Object.keys; // 公共静态 Object.keys 函数快捷方式
keys({a: 'a'}); // 这样我们以后可以直接使用它
```

继承之旅始于讨论对象继承其他对象。现在它结束于讨论类扩展其他类。没有理由惊慌，这只是对以下问题的简短回答：

- Q：“什么是 Square（正方形）？”
- A1：“它是一个扩展 Rectangle（矩形）的类”
- A2：“它是一个原型直接继承自 `Rectangle.prototype` 的类”

对象可以继承自原型的数量没有具体的限制，但只有一个直接的“扩展”，这在 JavaScript 中只可以在两个类之间实现。因此，当我们使用“扩展”（extend）一词时，我们只能指的是一种非常特定的关系。

（注：原文中后半部分存在大量重复的段落，已根据注意事项“不要重复输出原文”的原则进行去重处理，仅保留核心翻译内容。）

我们每天所做的每件事，以及我们周围的一切，都是基于基本的 `else` 逻辑流的，这同样适用于任何可能执行或不执行某些操作的软件。

以下代码是一个虚拟示例，展示了我们的驾驶程序是如何基于条件的。

```javascript
function letsDrive(car, where) {
  // 只有在引擎关闭状态时才启动引擎
  if (car.isEngineOff()) {
    car.startEngine();
  }

  // 如果下雨，我们就小心行驶
  if (global.weather.isRaining()) {
    car.goSlowerThanUsual();
  } else {
    car.goUsualSpeed();
  }

  // 电台呢？
  if (Date.now() < global.today.LATE_MORNING) {
    car.radio.findMorningNews(); // 每天
  } else if (where === 'beach') {
    car.radio.findSurfingSongs(); // 假期间
  } else {
    car.radio.findRockNRoll(); // 每天晚上
  }
}
```

```javascript
var myNewCar = new Car();
// 每次我需要开车时调用 letsDrive(myNewCar, 'my office');
```

`if` 并不总是需要一个 `else`，并且中间可以有一个可选的 `else if`。

## 三元运算符

最常用的内联 `if...else` 快捷方式是由三元运算符提供的，它看起来像一个问号：`?
它只做一件事：如果条件为真，它返回第一个值；如果条件为假，则返回第二个值。

```javascript
var ternaryResult = (14 / 7 === 2) ? 'correct' : 'back to school!';
```

## switch 语句

如果说三元运算符是 `if...else` 的快捷方式，那么 `switch` 语句就是长长的 `if...else if...else if...else` 条件的快捷方式。

```javascript
function isLetterInAFRange(letter) {
  var result;

  // switch 语法，传递任何值
  switch (letter) {
    // 它会像这样对每个 case 进行比较
    // if (letter === 'G') ...
    case 'G':
      // 如果比较为真，它将执行后续操作
      result = false;
      // 你可以任意 break 它，退出 switch; break;
      // 或者你可以创建不同的入口点，即所谓的“穿透”
    case 'A': // else if (letter === 'A')
    case 'B': // else if (letter === 'B')
    case 'C': // else if (letter === 'C')
    case 'D': // else if (letter === 'D')
    case 'E': // else if (letter === 'E')
    case 'F': // else if (letter === 'F')
      result = true; // 所有这些条件都返回 true
      break;
    // 没有满足的条件？我们有一个默认回退
    default:
      result = false;
      break; // 在 `default` 部分内是可选的
  }

  return result;
}
```

大量的 `else if (letter === 'A') { ... } else if (letter === 'B') { ... }` 会让你的代码看起来像由毕加索设计的章鱼。

## 逻辑 || 运算符（读作或）

与其使用许多执行相同操作的 `else...if`，你可以使用 `||`。
因此，上一个示例可以重写如下所示：

```javascript
function isLetterInAFRange(letter) {
  if (
    letter === 'A' || letter === 'B' || letter === 'C' || letter === 'D' ||
    letter === 'E' || letter === 'F'
  ) {
    return true; // 只要函数返回，它就会退出函数
  }
  // 这让你能够避免冗余的
  return false; // `else`，因为真的没有别的事情可以做了
}
```

## 逻辑 && 运算符（读作与）

与 `||` 运算符相反，`&&` 运算符只有在上一个条件通过验证时才会继续检查条件。这可能是需要记住的最重要概念之一。

例如，下面的 ATM 操作将不会一起执行，而是一个一个执行。

```javascript
function getMoney() {
  if (
    cardIsValid() && pinCodeIsValid() && userSelectedAmount()
  ) {
    // 卡有效吗？好的……下下一个
    // 用户知道密码吗？
    // 下一个！
    // 用户需要特定的金额吗？
    // 好的……下一个
    return getAmountSelectedByUser(); // 一切正常，一切顺利 OK
  }
  return 0; // 上面发生了错误
}
```

还可以结合这两个运算符，以某种方式模拟三元运算符可以的功能。

```javascript
// 通过逻辑运算符实现三元运算符
console.log((1 < 2) && 'OK' || 'EPIC FAIL'); // 显示 'OK'
// 与三元运算符等价
console.log((1 < 2) ? 'OK' : 'EPIC FAIL'); // 也显示 'OK'
```

然而，每当我们需要三元逻辑时，可能应该使用相应的运算符。

## 真值（truthy）和假值（falsy）

`if` 或 `else...if` 语句，以及三元或逻辑运算符都是非常仁慈的。检查实际的布尔类型 `true` 或 `false` 值没有关系。`false` 值、数字 `0`、空字符串 `""`、`null` 值、`undefined` 以及异常的 `NaN` 引用都被视为假值，其余均为真值。

每个被接受的参数，但这里有几个新术语。最好对它们进行澄清说明，以便更好地理解我们正在讨论的内容。

## void

`void` 在 JavaScript 中的等价于 `undefined`。它还是一个 JS 历史运算符，类似于 `typeof`，但无论是什么，它总是返回 `undefined`。

```javascript
console.log(void 0); // 或任何其他值，均记录 undefined
console.log(void "hello"); // undefined
```

## DOM

与普通的 JavaScript 字符串没有太大区别。没什么新需要学的。

## EventListener

W3C 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。无论如何，我们可以很容易地说，`EventListener` 可能是 Web 上最被误解的接口。

让我们看看在 2000 年它是通过 Web IDL 被描述的。

```javascript
interface EventListener {
  void handleEvent(in Event evt);
};
```

每当注册事件时，我们可以传递一个带有 `handleEvent` 方法的对象。

下面可以通过浏览器控制台运行的示例代码。一旦你把所有内容都写进去，你只需要点击该页面上的任何地方即可（链接除外）。

```javascript
var listener = {
  // 如果存在 handleEvent 方法，它会在事件发生时被调用
  handleEvent: function (event) {
    // 这个监听器在哪里注册的？
    var node = event.currentTarget;
    // 这个监听器真的是 document 吗？
    console.log(node === document); // true
    console.log(this === listener); // true
    // 我们通过移除这个监听器来清理
    // event.type 总是可用的
    // 它是我们注册监听器时使用的字符串
    node.removeEventListener(event.type, this);
  },
  // 我们注册了监听器，如果点击 document，它应该记录一次。
};

document.addEventListener('click', listener);
```

`handleEvent` 方法也可以通过类继承，将逻辑限制在每个实例内部。

```javascript
function ClickCounter(el) {
  // 为此元素 el 注册点击事件
  el.addEventListener('click', this);
  // 我们还注册了一种最终丢弃它的方法
  el.addEventListener(this.drop, this);
}

ClickCounter.prototype = {
  drop: 'drop:click-counter',
  value: 0,
  handleEvent: function (evt) {
    var el = evt.currentTarget;
    if (evt.type === this.drop) {
      // 自定义事件类型
      // 计数开始的地方
      // 移除监听器
      el.removeEventListener(evt.type, this);
    } else {
      el.textContent = ++this.value; // 显示计数
    }
  }
};

// 一个新的 ClickCounter 实例，显示 body 上的点击
new ClickCounter(document.body);
```

## 使用函数的 EventListener

该接口被认为最容易误解的原因是，几乎每个人都使用函数而不是对象来注册事件。

“为什么呢？”回到 2000 年，当开发者试图让事件在标准和非标准浏览器中都能工作时，还没有简单的方法可以通过丑陋的 `attachEvent`/`detachEvent` 非标准替代方案来复制对象的行为。

退回到“仅限函数”在某种程度上损害了旧的书籍、文章、库和框架，引入了已经通过标准接口解决的问题。

```javascript
// 与之前的逻辑相同，使用函数
document.addEventListener('click', function (event) {
  // 这个监听器在哪里注册的？
  var node = event.currentTarget;
  // 这个监听器真的是 document 吗？
  console.log(node === document); // true
  console.log(this === document); // 又是 true，多余了
  // 如果我们不给这个函数命名
  // 我们永远无法移除它
  // 因为我们没有引用，即：
  // node.removeEventListener(event.type, ???); ← 在这里我们可以用什么？
});
```

每当我们使用函数作为事件监听器时，我们就自动接受了以下内容：

- `this` 执行上下文始终指向 `event.currentTarget` 节点
- 如果我们想增加计数或执行任何其他与节点或组件通用状态相关的操作，我们最终将需要一个辅助对象
- 如果我们没有引用，以后将永远无法“取消订阅”。

为了解决上述低效列表中的前两点，社区提出了一个想法：按需创建函数，其上下文是静态捕获的。

```javascript
// 工具示例
function bindTheContext(fn, context) {
  // 返回一个使用 `context` 变量的函数
  return function () { // 并显式强制 fn 使用 context
    return fn.apply(context, arguments);
  };
}
```

```javascript
function whoIsIt() { return this }; // 它只是返回上下文
var me = {name: 'Andrea'};
var alwaysMe = bindTheContext(whoIsIt, me); // 现在永远被捕获了！

alwaysMe() === me;
alwaysMe.call({}) === me;
alwaysMe.call(document) === me;

// true -> 它们一直是我
// true -> 它们一直是我
// true -> 仍然是我！
```

## function bind

在被广泛采用后，“函数捕获”模式变成了标准，`Function.bind` 也随之诞生了。

```javascript
// 与之前的逻辑相同，使用函数
function sum(x, y) {
  return x + y;
}
```

自诞生以来，JavaScript 证明了其作为优秀的事件驱动环境的优势和能力。你可以在浏览器和服务器端引擎中注册任何类型的事件，并传递任何类型的数据。

然而，Node.js（一个让你完全在服务器端运行 JavaScript 程序的环境）的实现与浏览器有许多不同之处。

## 浏览器事件

在之前的页面中介绍过，浏览器事件可以分为两大类：

- 1. 用户或系统事件
- 2. 自定义事件，也称为“合成”，即通过代码生成的事件。当你浏览 Web 并在键盘上打字、点击鼠标、手指触摸屏幕或使用通用笔指针时，你正在创建并隐式触发被特殊信任用户意图的事件。

## 冒泡和捕获

现在应该很清楚 DOM 包含树。每个树的特性是可以进入每个分支，这种过程也被描述为 DOM 树遍历。默认情况下，每个事件都会执行这种遍历，从 document 开始，到达目标节点，然后向上冒泡。

```javascript
// 遍历数组中的每个元素 ...
[document, document.documentElement, document.body].forEach(function(el) { // 添加相同的事件类型 ...
  el.addEventListener(this.type, this, true); // true 用于捕获
  el.addEventListener(this.type, this, false); // false 用于冒泡 // false 是默认值
}, {
  type: 'click',
});
```

```javascript
handleEvent: function (e) { 
  console.log(
    e.currentTarget.nodeName,
    e.target.nodeName,
    e.eventPhase === e.CAPTURING_PHASE
  );
}
```

// 事件类型 // 监听器
// 监听器所在位置 // 通过 forEach 添加 // 创建此事件通知的节点 // 事件阶段

`e.CAPTURING_PHASE` 常量实际上继承自 `Event` 构造函数。这是 JavaScript 类与 DOM 类之间的差异之一。

`document.documentElement` 是始终始终可用的 HTML 根节点。为了更好地理解我们正在做什么，现在可能是切换到一个空白页的好时机。这通常可以通过简单在 URL 栏中输入 `about:blank` 即可，URL 栏是我们通常输入网站地址（如 www...）的地方，我们也可以用它进行搜索。

如果你打开控制台并在其中编写之前的 `forEach` 代码，一旦按下回车并点击页面上的任何空白区域，你应该看到以下内容：

```
# document HTML true
HTML BODY true
BODY BODY true
BODY BODY false
BODY BODY false
HTML BODY false
#document BODY false
```

```javascript
// 它从 document 开始捕获
// 它遍历 HTML 节点到达 target
// 到达 target 后，没有更多可捕获的
// 它从 target 开始冒泡
// 所以它将触发父 HTML 节点监听器
```

再次，捕获阶段发生的是：document -> html -> body。而在冒泡阶段发生的是：body -> html -> document。

```javascript
event.stopPropagation()
```

遍历可能是开销昂贵的，特别是在巨大的嵌套树中。

如果某个特定的监听器对其他节点没有意义，`stopPropagation` 可以中断事件的冒泡或捕获阶段，从而丢弃当前事件的传播。

以之前的点击监听器为例。只需在 `handleEvent` 方法的开头添加 `e.stopPropagation()`，点击事件永远不会到达其他节点。

```
#document BODY true // 在 document 捕获阶段执行 e.stopPropagation()
```

上述行就是你在控制台中能看到的全部内容。目标（即 `document.body`）从未见过事件的到来。如果在冒泡阶段停止事件传播，也会发生同样的情况。

一旦它到达 `event.target`，它就不会再向上冒泡了。

```
body -> html -> document // 常规 冒泡阶段
document -> html -> body // 常规 捕获阶段
```

```javascript
evt.stopPropagation();
body -> | // 停止冒泡
document -> | // 停止捕获
```

## event.preventDefault()

如果一个节点关联了某些特殊操作，`.preventDefault()` 方法会阻止该操作的发生。你正在点击链接吗？阻止默认将让浏览器**不**跟随该链接！你正在填写表单吗？阻止默认将让你无法更改输入框中的文本，或者让你无法提交该表单。

```javascript
function justPreventDefault(evt) { event.preventDefault(); }
// 它不会打开链接
a.addEventListener('click', justPreventDefault);
// 它不会让你在 `input` 中写入
input.addEventListener('keydown', justPreventDefault);
```

通过触摸事件，你甚至可以阻止页面滚动！

## CustomEvent

每当我们想要创建自己的合成事件时，DOM 都提供了它自己的构造函数，Web IDL 对其描述如下：

```javascript
// 以下意味着 → new CustomEvent('event-type', {detail: anyValue}) 
[Constructor(DOMString type, optional CustomEventInit eventInitDict), Exposed=(Window,Worker)] 
interface CustomEvent : Event {
  // 可用于页面和 Web Worker // 实现 Event
  readonly attribute any detail; // Event 之间的主要区别
};
// 它描述了预期作为选项字典的 CustomEventInit 对象
dictionary CustomEventInit : EventInit {
  any detail = null; // 默认，detail 属性将为 null 
};
```

嗯，也许 Web IDL 格式有点冗长，但它确实提供了所有必要的细节。

```javascript
// TL;DR (太长，没读)
var myEvent = new CustomEvent('my:type', {
  detail: { 
    any: 'sort',
    of: 'data',
    callback: function () {
      return 'possibly think about';
    }
  }
});
```

```javascript
// 这样如果某个节点中有一个这样的监听器 
document.addEventListener('my:type', function (event) {
  console.log(event.detail);
});
```

（注：OCR 文本在代码块中包含一些片段。让我根据提供的文本流进行重新对齐：此处已根据要求去除了重复的干扰内容。）

```javascript
console.log(
  myReference.relationship, // 对象不受影响
  Data(myReference).relationship // 弱引用的对象受影响
);
```

## Symbol（符号）

在本术语表的开头已作为一种类型被提到，符号是特殊的键，用于设置或读取唯一标识的对象属性。它们对于避免命名冲突非常有用。

```javascript
var obj = {};
var uniqueKey = Symbol('unique'); // 创建一个名为 "unique" 的键
obj[uniqueKey] = 123;
var anotherKey = Symbol('unique'); // 创建另一个名为 "unique" 的键 
console.log(
  obj[uniqueKey], // 123
  obj[anotherKey] // undefined, 它是一个唯一的键！
);
```

Symbol 的一个特殊之处在于它不能通过 `new Symbol()` 创建新的符号，否则会抛出错误。“……为什么呢？” 因为 `typeof Symbol() === "symbol"`，这与构造函数创建其他原始类型（如 "string"、"boolean" 或 "number"）的方式是一致的。

以下是通过 `new` 创建的 JavaScript 原始类型中常见的预期问题：

```javascript
typeof new String("string"); // "object"，如果预期是 "string" 则是错误的
typeof String(); // "string"，这通常是正确或符合预期的
```

## Primitives（原始类型）

任何 `typeof` 返回非 "function" 或 "object" 的值（且该值不为空）都是原始类型。原始类型的主要特征是不可能为它们附加属性：这些都是不可变的值。

```javascript
var t = true; t.key = 'value'; // 没有报错，但也没有值
var s = 'string'; s.key = 'value'; // 同上所示
var i = 0; i.key = 'value'; // 再次如此
var k = Symbol(); k.key = 'value'; // ……再次

console.log(t.key, s.key, i.key, k.key); // 所有结果都是 undefined
```

## Object.getOwnPropertySymbols(obj)

→ Symbols 数组

默认的符号描述符是可配置、可枚举的、可写的，并且具有通用值，就像其他属性一样。然而，符号对于常见的操作（如 for/in 循环、`Object.keys(obj)` 或 `Object.getOwnPropertyNames(obj)`）来说是“不可见的”。

```javascript
var obj = {};
var key = Symbol();
obj[key] = 'value';
for(var k in obj) console.log(k); 
console.log(
  Object.keys(obj),
  Object.getOwnPropertyNames(obj)
); // 不，这里什么都没有发生

// [] -> 它是一个空数组
// [] -> 再次是一个空数组
Object.getOwnPropertySymbols(obj), // [Symbol()] -> 终于找到了它！
console.log(key in obj); // true -> `in` 运算符同样有效
```

需要记住，即使符号不那么“阻碍你”，但它们并不是私有的。

还应该记住，它们和属性是一样的：如果意图是在两个对象之间建立一种不侵入的关系，我们仍然最好使用新的 `WeakMap`。

## Shared Symbols（共享符号）

可以通过 `.for(key)` 和 `.keyFor(sym)` 方法处理全局共享的符号。

```javascript
var root = this.window || global; // 获取全局上下文
var myKey = Symbol.for('my:info'); // 创建标记为 'my:info' 的符号
root[myKey] = Math.random(); // 仅在尚未可用时分配随机值
```

```javascript
console.log(
  Symbol.keyFor(myKey),
  root[myKey],
  root[Symbol.for('my:info')]
); // 返回标签 'my:info' // 返回随机值 // 与使用 root[myKey] 相同
```

## Special Symbols（特殊符号）

符号构造函数有几个公共静态属性，它们也是为人知的符号。这些属性可以用于更改代码运行的默认方式。

例如，`Symbol.iterator`（别名为 `@@iterator`）可以描述 for/of 循环如何遍历通用集合。

## for/of loop

在现代 JS 引擎中，可以使用 for/of 遍历一些集合。

```javascript
for (var value of ['a', 'b', 'c']) console.log(value); // 'a', 'b', 'c'
```

这之所以可行，归功于 `Symbol.iterator` “协议”，该术语用于指定迭代器属性应该是什么样子以及它应该返回什么。

```javascript
var me = {name: 'Andrea', age: 37}; // 猜猜又是是谁？
me[Symbol.iterator] = function () {
  var keys = Object.keys(this), i = 0;
  return {
    // 使用箭头函数语法来绑定 `this`：
    next: () => {
      return {
        done: i >= keys.length, value: this[keys[i++]]
      };
    }
  };
};
// 定义迭代器协议 // 获取所有当前键 // 返回一个对象 ……
// 带有 next 方法 …… 它每次都会被调用 // 返回另一个对象 // 两个属性
// done -> 直到结束为 false // value -> 类似于 me[currentKey]

// 我们现在可以获取所有的值
for (var value of me) console.log(value); // 'Andrea', 37
```

## Fat arrow（箭头函数）

现代 JavaScript 带有许多语法简写，箭头函数可能是最实用的之一。定义时不需要 `function` 关键字。

```javascript
var obj = {
  x: 2,
  add: function(v) { return this.x + v; },
  sub: (v) => this.x - v // 箭头函数
};
console.log(obj.add(1)); // 3
console.log(obj.sub(1)); // 1
```

```javascript
var received = yield sent++;
// ↑ sent will be the value of the object returned // when we'll
invoke gen.next() the first time console.log(received); // ←
// will log the value in gen.next(value)
}
```

需要记住 `yield` 是“从右向左”暂停的，也就是说，它会发送出其可选的右侧值，并最终将 `gen.next(one)` 的值赋值给它的左侧。

这解释了为什么当我们第一次调用 `.next()` 时无法传入任何值：我们只是开始了函数的执行，直到我们停止并接收到第一个被 `yield` 出来的值（如果有）。

下面是一个示例，它会漏掉传递的第一个值。

```javascript
var g = forever(); // g 现在暂停在 forever 控制台的顶部
log(g.next('A').value); // 第一个 yield 是 0，'A' 被忽略了
log(g.next('B').value); // 接收到 'B'，while 循环 yield
```

→ 2 console.log(g.next('C').value); // 接收到 'C'，while 循环 yield → 3

接下来通过文本描述尝试描述我们在循环时发生了什么。

```javascript
function forever() {
  var sent = 0;
  while (true) {
    var received = yield sent++; // {value: 0}
    // g.next('B'); // {value: 1}
    // g.next('C');
  }
}
```

## generator.throw(error)

如果在迭代过程中发生任何错误，可以通过返回（像普通函数一样）或抛出错误来从生成器中退出。

然而，使用生成器的意义在于能够从外部控制它们，而无需直接访问它们的作用域或上下文，但可以使用等同于遥控器的“播放/暂停”按钮。

`gen.throw(new Error('get out!'))` 方法赋予了我们强制生成器停止执行的能力，即使它的执行作用域内没有发生任何错误。

## Promises

如果我们需要链式调用异步操作，我们有几种选择：

- 如果引用相关，则嵌套回调
- 向处理过程中所需的每个函数传递几十个相关的引用
- 在运行时附加任何类型的数据并到处调用绑定的方法

然而，如果我们想处理在此过程中可能出现的错误，我们基本上就完了，所以这是我们可以扭转局面的时刻。

### 常用方法

```javascript
async(input, function (output) { // 使用 output + 执行某些事情
}).then(function (output) { // 使用 output + 返回某些值
});
```

经典方法与基于 Promise 的方法之间存在着细微但非常重要的区别，即 Promise 可以原样传递，然后我们可以通过简单地调用其 `.then(callback)` 方法在任何时候添加我们的逻辑。

```javascript
var waitTillIsFinished = new Promise(function (res, rej) {
  var thingsToWrite = 1000;
  while (thingsToWrite) {
    thingsToWrite--;
    setTimeout(function() {}, 0); // 模拟异步
  }
  res('All books finished and parsed'); // 书已完成并解析
}); // 谁在等它

waitTillIsFinished.then(function (content) {
  console.log(content); // 这样一旦解析
});

// 某人 else
waitTillIsFinished.then(function (content) {
  writeAboutBook(content); // 另一个人
  // do something else
});
```

Promises 最适合与异步代码一起。上面的示例并不是最佳实践。

“一次性”异步操作确实是最适合用 Promises 解决的类型。

```javascript
var userToIgnoreApp = new Promise(function (res, rej) {
  var fn = function (evt) {
    evt.currentTarget.removeEventListener(evt.type, fn); // 清理
    res();
  };
  document.querySelector('#app').addEventListener('click', fn);
  localStorage.setItem('do-not-ever-bloody', true); // ↑ 这只是浏览器上可用的一个小数据库
}); // 当该点击发生时
userToIgnoreApp.then(function () {
  // ...
});
```

## promise.then(resolved, rejected) -> newPromise

如果一个 promise 仅通过 `.then(notify)` 来调用其接收到的 `reject(anyValue)`，则不会产生任何影响：还需要一个处理可能错误的回调。

```javascript
var p = new Promise(function (res, rej) {
  rej('because'); 
});
p.then(
  function (result) { console.log('All good!'); },
  function (err) { console.error(err); } // 'because' 错误
);
```

## promise.then(resolved).catch(anyError) → newPromise

如果 promise 链中的任何调用内部发生错误，只有 `.catch(function)` 会被通知（而不是 `rejected` 那个）。这实际上是这两种模式之间的一个重要区别，因为一种确实涉及手动拒绝，而另一种即使在 promise 已经解析的情况下也会做出反应。

后面是示例代码。

```javascript
var p = new Promise(function (res, rej) { res('OK'); }); // 一切
p.then(
  function (result) {
    console.log('All good!');
    throw new Error('actually no!');
  },
  function (err) {
    console.error('nope', err);
  }
).catch(function (err) {
  console.error('caught', err);
});
// 'All good!' // 该死的！
// 永远不会 // 我们在这里了
```

## promise.then(fn).then(fn).then(fn) → newPromise

每当我们调用 `.then(fn)` 时，都会创建一个新的 promise。通过链创建的 promise 与简单 promise 之间的主要区别在于，对于链式的，我们需要返回某些值，否则它们将无法接收值。

```javascript
var pRoot = new Promise(function (res, rej) { res('OK'); });

var pFirst = pRoot.then(function (info) {
  console.log(info); // 'OK' -> 来自 pRoot 的解析数据
  return 123; // 链 pFirst 将接收 123
});

var pSecond = pFirst.then(function (info) {
  console.log(info); // 可能转换后的 info
});
```

如果我们想暴露接收到的数据只需返回它，否则我们可以返回不同的结果，甚至什么都不返回。

## Promise.all(arrayOfPromises) -> newPromise

异步非阻塞操作并不一定相关。考虑组织一次旅行，需要考虑票务、租车以及最后准备行李。

```javascript
Promise.all([ // 通过 Promise 规划旅行
  new Promise(function (res, rej) { res('酒店已预订!'); }),
  new Promise(function (res, rej) { res('机票已预订!'); }),
  new Promise(function (res, rej) { res('行李已就绪!'); }),
  new Promise(function (res, rej) { res('车已租好!'); })
]).then(function (results) {
  console.log(results);
  // 预订房间
  // 预订机票
  // 准备行李
  // 租车
  // 太棒了，我们可以出发了 !!!
});
```

一旦这些 Promise 中的任何一个失败，拒绝捕获器就会获知，我们可能需要重新安排整个旅行。希望如此！

如果我们想创建一个已经解析的 promise，`Promise.resolve(value)` 是一个方便的快捷方式。它的对应部分是 `Promise.reject(anyValue)`，它提供了类似的实用函数。

```javascript
var p = Promise.resolve('any value');
p.then(function (result) { console.log(result); });
```

# Generators and Promises

让我们看看下面的工具，它结合了两种模式。

```javascript
// 最初解释于 https://www.promisejs.org/generators/
function syncLike(genFunc) { // 它接受一个生成器函数
  return function () { // 它返回一个匿名函数
    var gen = genFunc.apply(this, arguments), // 一旦被调用将创建一个生成器
    handle = function (result) { // 它将在这里管理它
      // it will return a Promise, no matter what the value is
      var p = Promise.resolve(result.value);
      // if the generator hasn't finished yet, we can
      // chain a new Promise passing `next` and `orFail` as call-
      // backs
      return result.done ? p : p.then(next, orFail);
    },
    next = function (value) { return handle(gen.next(value)); },
    orFail = function (error) { return handle(gen.throw(error)); };
    // `next` and `orFail` return ↑ promises chained via `handle`
    try { return next(null); } catch(err) { return Promise.reject(err); }
    // ↑ our journey begins, with a fallback in here ↑
    // it's a Promise “circus” that drives a generator
  };
}
```

It's hard to understand what's going on until we see a concrete example so here it is: do you remember when we talked about planning your vacation? Here it is how it could look like now:

```javascript
function arrange(what) { // it returns a new Promise that will resolve
  return new Promise(function (res, rej) { res(what + ' is ready'); });
}
```

```javascript
// an always welcomed activity to do ^_;
var letsGoOnVacation = syncLike(function* {
  var
  hotel = yield arrange('hotel'),
  flight = yield arrange('flight'),
  // multiple var declaration // it will arrange the Hotel // it will arrange the flight
  luggage = yield arrange('luggage'), // it will arrange the luggage
  car = yield arrange('car'); // it will arrange the car too
  console.log("let's go!", hotel, flight, luggage, car);
});

letsGoOnVacation(); // it will log pretty much everything! // let's go! The hotel, the flight, the luggage, and the car are ready!
```

Using promises to somehow resolve generators is a nice way to make the code look synchronous. If you are wondering whether Promise.all could have been used instead of having to wait for one action after the other one, the answer is Yes! And that would have been more efficient, for the simple reason that we could have executed all those actions in parallel.

```javascript
// a better approach to multiple asynchronous actions
var letsGoOnVacation = syncLike(function* () { 
  console.log("let's go!", yield Promise.all([
    arrange('hotel'),
    arrange('flight'),
    arrange('luggage'),
    arrange('car')
  ]));
});

letsGoOnVacation();
```

To conclude: Promises' main strength, but also their main caveat, is the fact that they cannot be cancelled. That means that we might regret using them for any operation that could take a long time, as these are probably the wrong solution to the problem. Instead we could track those through a progress-friendly operation, something a file download or an image upload could require.

# Timers

Asynchronous code have been already mentioned, but so far without concretely testing what they are about. Well, asynchronous is not usually something created just for fun, but rather an inevitable part of our application, such as a database query, a client/server interaction, a worker notification, and so on.

JavaScript also offers its own mechanisms to schedule the execution of some arbitrary code at some point in time. The most documented and widely implemented functions to schedule such executions are `setTimeout` and `setInterval`, which are both capable of detaching from the current execution flow in a nonblocking way.

```javascript
setTimeout(fn, delay, arg1, arg2, argN) -> timerIdentifier
```

To schedule the invocation of any function at any time:

```javascript
var t = setTimeout(
  function laterOn(logMe) { // it will receive arguments, if specified
    console.log(logMe);
  },
  1000, // it's the delay represented in milliseconds
  Math.random() // it's the optional argument to pass later on
);
```

If you are patient enough to wait for a whole second, you’ll see the random number returned by `Math.random()` invocation appear in the console. However, if you are no longer interested in that operation, you can always clean it up, as long as you hold its identifier.

## clearTimeout(timerIdentifier)

If you set a timer, you should be able to cancel it too. This method does exactly that.

```javascript
var ti = setTimeout(console.log, 1000, 'content');
clearTimeout(ti);
```

## setInterval(fn, delay, arg1, arg2, argN) -> timerIdentifier

```javascript
var t = setInterval(function () {
  console.log("hello");
}, 1000);

// you should be able to cancel it with
clearInterval(t);
```

## 模板字符串 (Template strings)

```javascript
function greetingsOldWay(name) { 
  return 'Hello ' + name + ',\n' + ' thank you for being here!';
}

function greetingsNewWay(name) { 
  return `Hello ${name},\nthank you for being here!`;
}
```

上述比较展示了引号和反引号之间的区别：使用后者，我们不仅可以忘记换行问题，还可以访问本地引用，包括 `this.context`。

该语法由定界符 `${ }` 表示，在其中我们可以编写 JS。

## 标签模板字符串 (tagged template strings)

反引号字符串的一个特殊之处是它们的“可标签性”（tag-ability）。标签是一个函数，它在执行时会将紧跟在可能的大括号前后的字符串数组作为第一个参数，并将字符串中这些可能的大括号内存在的任何代码的结果作为零、一个或多个计算后的值。

```javascript
function tagLogger(statics) { // statics 始终是一个数组
  for (var i = 1; i < arguments.length; i++) { // 如果有额外的参数
    console.log(statics[i - 1]);
    console.log(arguments[i]);
  }
  console.log(statics[i - 1]); // 输出最后一个 statics 字符串
}

tagLogger `before ${2 + 3} after`; // 输出 'before ', 5, ' after'
```

在返回值之前进行转换时，标签函数变得特别有用。

```javascript
function htmlAttributes(markup) {
  // 声明一个输出、正则表达式和一个转换器
  for (var out=[], re = /[&<>"]/g, fn = (m) => ('&#' + m.charCodeAt(0) + ';'),
       i = 1; i < arguments.length; i++) {
    out.push(markup[i - 1], arguments[i].replace(re, fn));
  }
  out.push(markup[i - 1]);
  return out.join(""); // 转换后的
}

var value = '<any>'; // 恶意输入
console.log(htmlAttributes`<input value="${value}">`); // 已清洗！
```

## 正则表达式 (regular expression)

`RegExp` 构造函数及其实例引入了一种强大的语法，能够通过具有特殊含义的特殊字母来搜索、匹配、测试或替换字符串。

这里有很多注意事项、可能的安全影响、字符串编码问题，以及处理这些问题的现代或旧版方法，我认为在这里部分介绍它们是不明智的。

重要的是了解它们的字面量表示形式：

```javascript
// 如何识别字面量、内联 RegExp 实例
var RegExp = /^(?:search)*via.[special-chars]/gim;
//      ▲ 开始 结束 ▲ ▲ 可的 g,i,m,u 标记 ▲
```

## JSON

一个没有关于“JavaScript 对象表示”（JavaScript Object Notation）解释的 JS 词汇表将是不可信的，所以这里是：JSON 是对象、数组、字符串、布尔值、数字、null 以及其他任何内容的字符串表示标准。

```javascript
// JSON 是以下值的字符串表示
var str = '{"name":"JSON","values":["string",1.2,{},[],true,false,null]}';
```

我们可以通过 `JSON.parse(str)` 解析字符串，或者使用 `JSON.stringify(compatibleValue)` 编码任何兼容的值，两种方法都接受回调函数作为选项。回调会在读取每个条目或在解析期间恢复值时被调用。

## 数学 (Math)

这个全局可用对象充满了方法，其目的是帮助我们做……数学！

最常用的是 `Math.pow(num, power)`、`Math.sqrt(num)`、`Math.max(num1, num2, numN)` 和 `Math.min(num1, num2, numN)`，但你可以通过名称检查所有它们，并在线查询它们的签名。

```javascript
// 以下是一个辅助函数，告诉我们关于任何对象的许多信息
function tellMeAbout(that){
  console.log(Object.getOwnPropertyNames(that))
}

tellMeAbout(Math); // 看看里面有什么！
```

## parseInt(string, base) -> 整数 (integerNumber)

每当你处理用户输入时，你就在处理字符串。如果你询问年龄或任何整数，`parseInt` 将帮助你转换用户输入。

```javascript
console.log(
  parseInt('3'), // 然而我们可以避免指定进制
  parseInt('11', 2), // 2进制下的 11 是 3，而不是 11
  parseInt('08', 10), // 在十进制世界中 08 是 8
  parseInt('FF', 16) // 十六进制 FF 将是 255
);
```

## parseFloat(string) → 浮点数 (floatNumber)

当你需要将字符串转换为浮点数时，`parseFloat` 是不二选择。它不接受任何额外参数，因此 `parseFloat('FF')` 将产生 `NaN` 值，因为它不会被识别为数字或十六进制字符串。

## 最近的 ECMAScript 特性 (features)

自从我开始写这个词汇表以来，JS 已经发生了一些变化。

ECMAScript 规范是一个活跃且不断更新的标准。这意味着一旦符合所有阶段步骤，新功能就会变得可用。

此词汇表省略了一些现代主题，但网上有描述，另外还有一些值得快速探索的内容。

## let 声明 (let declaration)

`let` 声明是块作用域的。与 `var` 不同，它没有以允许使用的方式被提升。

```javascript
let x = 10;
console.log(x); // 10
// let x = 20; // 语法错误：标识符 'x' 已声明
```

## 展开运算符 (spread operator)

展开运算符 (`...`) 允许你展开数组或对象。

```javascript
let arr = [1, 2, 3];
let combined = [...arr, 4, 5];
console.log(combined); // [1, 2, 3, 4, 5]
```

## 剩余参数 (rest parameters)

剩余参数允许函数接收无限数量的参数作为数组。

```javascript
function sum(...numbers) {
  return numbers.reduce((acc, curr) => acc + curr, 0);
}
console.log(sum(1, 2, 3, 4, 5)); // 15
```

我们将使用现代特性。

**你听过转译器（transpilers）吗？** 我不仅听过它们，还在使用它们。例如，本术语表中大多数与平台无关的示例都通过 `babel-node` 成功了测试，这是一个命令行界面（CLI），它将最新 ECMAScript 规范中的最新特性引入 node.js。我会在生产环境中使用它们吗？这取决于情况！

**“生产环境（in production）”意味着什么？** 它是向每个用户提供的通用网站、应用程序、框架、设计或程序的正式版本。它是我们交付的内容，而不是为了快速测试想法而做的“原型（prototype）”。

**“原型（prototype）”意味着什么？** 我知道这个术语表可能会让人困惑，但在涉及非技术的 JS 讨论时，原型是一个草图，或者是最终产品的快速创建版本，它本身可能永远不应该投入生产环境。

**我应该使用哪个框架、库或工具？** 只要能解决你的问题的那个（如果有的话）。否则，使用前端或后端核心已经提供的更好。

- JavaScript 仅用于网页吗？如今，很难找到不运行 JS 的电子产品。智能手表、路由器、你现在的电脑，甚至是彩色的 LED 灯泡，都兼容某些 JavaScript 引擎或已经在运行它。
- JavaScript 是内存安全的吗？有一个垃圾回收器负责清理我们创建的混乱。我们可以做的是帮助它完成工作，例如不要无限期地持有值。

## 有用链接

- Mozilla 开发者网络 (Mozilla Developer Network) - <https://developer.mozilla.org/en-US/>
- 世界维网联盟 (World Wide Web Consortium) - <https://www.w3.org/>
- WHATWG - <https://whatwg.org/>
- Node.JS - <https://nodejs.org/>
- Babel JS - <https://babeljs.io/>
- YDKJS (书籍系列) - <https://youdontknowjs.com/>
- Exploring ES6 - <https://exploringjs.com/>
