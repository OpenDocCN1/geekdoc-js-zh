# JavaScript 入门指南：让 JavaScript 变得有趣
























































- navigator 对象




- 什么是块级作用域？



# JavaScript 简介

JavaScript 是一种用于创建交互式网页的编程语言。

JavaScript 的核心格言是“让它动起来”。

JavaScript 就像氧气。它赋予网页生命，因此奇妙的交互吸引着我们。

JavaScript 负责所有让我们流留在网页上的酷炫动画。

如果你查看过足球比赛的实时比分，JavaScript 可能正在其中运行。

JavaScript 无处不在。

JavaScript 是世界上最通用的语言。

JavaScript 的之处在于，你可以用它构建任何东西（并非字面意思）。

以下是我们用 JavaScript 构建的内容列表……

- JavaScript 用于为桌面和移动应用程序创建交互式网页。
- JavaScript 用于创建我们每天使用的移动应用程序。
- 我们还可以用它创建 iOS 和 Android 应用。
- JavaScript 也用于创建完整的桌面应用程序。

Google、Facebook、Microsoft、Uber 以及你能想到的其他公司都在使用 JavaScript！
无论有意还是无意，我们都使用过他们的服务，因此利用了 JavaScript。

## 什么是计算机程序？

**计算机**只是会盲目**执行指令**的盒子。
但与人类不同，它们会**准确地执行指令**。
如果你妈妈要求你在购物清单上增加 2 个洋葱，你很有可能忘记带洋葱。
与我们不同，计算机会**记住**一切。

正如我们所讨论的，计算机遵循一组指令并相应地执行任务。
以之前的例子为例，你妈妈给了你关于在购物清单上添加内容的指令。
所以，那些指令无非就是计算机程序。
计算机程序是计算机为了完成任务而遵循的一组指令。

让我们从**命令计算机****打印** "Hello World" 开始。
你能猜到我们将如何操作的吗？
我们将开始为计算机提供所需的指令来打印 "Hello World"。
我们将用计算机能理解的语言来编写这些指令。

## 打印文本

在 **JavaScript** 中**打印**文本的**命令**是：

```
document.write
```

这个命令告诉计算机在文档（即网页）上写入（打印）某些内容。
但如果没有几个特殊字符，这个命令是不完整的。
让我们把它们加上。

圆括号 `()` 告诉计算机将命令与要打印的文本隔离开。
在我们的命令中添加圆括号。

```
document.write()
```

双引号 (`""`) 用于指示计算机要打印哪部分。
在我们的命令中添加双引号，并加上 Hello World。

```
document.write("Hello World")
```

分号 `;` 表示命令的结束，因此在每个命令后都会加上分号。这是我们的命令：

```javascript
document.write("Hello World");
```

上述命令的结果将是：
Hello World

## 存储值

之前我们学习了如何命令计算机打印某些内容。
现在，让我们深入学习，学习如何在 JavaScript 中存储值。

想象你自己是一个化学实验室里的科学家。
如果你环顾实验室，你会发现几个气瓶。
每个气瓶都装有不同类型的气体，从氧气到氮气都有。
但我们如何区分哪个气瓶装的是什么气体呢？
为了解决这个问题，我们在上面贴上名称标签。
同样，如果我们想存储某些信息，我们就将其存储在内存中。
我们对所有信息都贴了标签以避免混淆。
如果有人问我们，我们不会告诉他们祖父的名字。
对吧？绝对不会！
在编程中，这种存储容器被称为“变量”。
所以，变量是存储值的容器。
我们将值放入这些容器中，然后通过引用容器名称来使用这些值。

## 存储字符串

假设我们要打印 "Niflare"

```javascript
document.write("Niflare");
```

觉得这写了很多内容吗？
不如让我们使用一个变量来节省精力。
在 JavaScript 中，创建一个变量被称为“声明”变量。

每种编程语言都有一组预留名称，被称为关键字。

变量用 `var` 关键字声明，后面跟着等号 (`=`) 和值。
让我们在变量 `x` 中存储单词 "Niflare"。

```javascript
var x = "Niflare";
```

不要忘记用分号 `;` 结束语句。
现在，如果我们想打印两次这个单词，可以用以下方式操作：

```javascript
var x = "Niflare";
document.write(x);
document.write(x);
```

附：有一种更好的方法可以用更少的代码完成相同的任务，我们很快就会学习。

所以，单词在编程语言中被称为字符串。希望你记住，我们会经常使用这个名字。
字符串是字母数字字符的序列。
字符串值始终用引号 (`"""`) 括起来。

## 布尔值

在生活中，我们必须做出许多决定。




这一切都归结为两个选项，即“是”或“否”，在编程术语中这被称为 **true**（真）或 **false**（假）。
这种真或假被称为 **Boolean values**（布尔值）。
一个 **Boolean** 值的声明方式如下：

```
var JS_sucks = false;
```

在创建带有布尔值的变量时，需要记住以下几点：
- 布尔值代表 **true** 或 **false**。
- 布尔值在定义时始终**不带引号**。

```javascript
var JS_Rocks = true;
var JS_rocks = "true"; // 不是布尔值
```

请记住，**双引号**用于声明*字符串 (Strings)*。因此，我们在创建带有布尔值的变量时不使用双引号。

## 存储数字

假设我们想将年龄存储在**变量**中并打印出来。
我们可以通过先将年龄存储在变量中，将其打印出来来实现。
让我们从**创建一个变量**开始。
```javascript
var age = 22;
```
请注意，**age** 和 **Age** 是两个不同的变量，因为 **JavaScript** 是一种**大小写敏感**的语言。

在创建数字数值变量时，需要记住以下几点：
数字可以带小数，也可以不带小数。

```javascript
var without_decimal = 10;
var with_decimal = 11.07;
```

正如我们所知，数字始终是不带引号（""）的数值，只有字符串是带引号的。

## 基础数学计算

数学是一门我们大多数人在一生中至少遇到过一次的学科。
我们中有些人讨厌它，有些人则迷上了它。
对于那些讨厌的人，不要担心，我们不会学习任何复杂的内容，而是将专注于基础知识。

## 加法和减法

假设，如果我们想让变量的值增加1，我们可以按照以下方式操作：

```javascript
var pizza = 1;
pizza = pizza + 1;
```

如果我告诉你有一种简单的方法可以执行相同的操作，而且可以节省大量的打字精力呢？
这就是自增 (incrementation) 概念用用场的地方。自增无非将变量的值增加1。

自增的语法是变量名加上 "++"，然后是一个分号 (;)。
让我们重写上面的程序：

```javascript
var pizza = 1;
pizza++;
```

是的，就是这样！
这就是你将变量的值增加1的方法。
同样，如果我们想让变量的值减少1，我们将按照以下方式操作：

```javascript
var pizza = 2;
pizza--;
```

是的，你完全正确！
自减 (decrementation) 的语法是变量名加上 "--"，然后是一个分号。

## 比较

我们作为人类，喜欢比较。
即使在日常生活中，我们也进行很多比较，比如“黑莓比三星好吗？”之类，比不穷。
我们在编程中也会进行比较。

## 等于

我们使用 "==" 来检查两个值是否相等，如果值相等，则条件变为 true。
记住，"=" 和 "==" 之间是有区别的。
"=" 用于声明变量，例如：

```javascript
var x = 2;
var y = 4;
```

而 "==" 用于检查两个值的相等性。

```javascript
x == y // false
```

## 不等于

而 "!=" 用于检查两个值是否不等。如果值不等，则条件变为 true，否则变为 false。

```javascript
x != y // true
```

简而言之，正如图像所示，所有比较的结果最终都是 true 或 false。

## 深入理解比较

假设你想买一台新手机，你有两个主要需求：
第一，手机的像素应该超过 10mp，且手机内存应该超过 16 GB。
让我们使用刚刚学习的比较概念为该需求写一个程序。

```javascript
var mp = 5;
var gb = 16;
```

让 mp 代表手机的像素，gb 代表手机内存。
那么条件将是：

```javascript
mp > 5 && gb > 16
```

现在，这两个条件是相互独立的。
如果我们想在两个值相等时得到一个“是”或“否”的答案呢？
即，我们在编程中如何编写“与 (and)”条件？
非常简单！
语法是 "&&"。

让我们重写上面的程序：

```javascript
mp > 5 && gb > 16;
```

所以，当两个或多个条件需要都为真时，就加上 "&&"。
同样，如果我们把需求修改为：手机像素超过 10mp 或内存超过 16gb。

```javascript
mp > 5 || gb > 16
```

“||” 也称为“或 (or)”。它被用于许多条件中只要有一个条件为真即可继续执行的情况。

现在我们已经知道了如何进行比较，
让我们继续学习如何在其中实现它们。





```javascript
var students = ["Bekky", "John", "Timothy", "Mac", "Green"];
```

如果我们想访问第一个元素，即 "Bekky"，我们可以按照以下方式操作：
编写数组名称，后面跟一个左方括号并写上索引。

`students[0]` 将让我访问到 "Bekky"。
同样地，我们可以猜猜如何访问其余的项目吗？
同样地，我们可以通过在方括号内编写它们的数字来打印所有其他项目。

## 重复任务

老实说，我们都是非常懒惰的生物！
为了避免手动重复操作，我们热爱自动化处理事情。
你还记得那些被要求写作业写 10 遍所有字母表的时候吗？
那感觉太糟糕了，对吧？
幸运的是，我们可以在编程中重复内容。
而且这非常容易学习。

假设我们想打印 10 遍 "I love JavaScript"。
我们将从创建一个变量并存储所需的值开始。

```javascript
var x = "I love JavaScript";
```

接着打印它……

```javascript
document.write(x); 
document.write(x);
document.write(x);
```

如果同一个任务可以用 3-4 行**代码**完成呢？
是的！3-4 行！你没读错！
这种**过程**被称为**循环**（looping）。
**循环**基本上是**重复**一组指令，直到满足了**条件**。
这好比做 50 个俯卧撑，这里 50 是**最大限制**，而做俯卧撑就是一组**指令**序列。
让我们考虑上一个例子，
打印 "I love JavaScript" 是一条指令，10 遍是一个条件。
所以，“I love JavaScript" 应该重复 10 遍。

## JavaScript 中的循环

当需要多次执行一段指令序列时，就会使用循环。
在 JavaScript 中，两种最常见的循环是：

- for 循环
- do...while 循环

## For 循环

For 循环由三个主要部分组成：

- 给变量赋初始值。
- 条件（例如 i<10）。
- 计数器语句：用于增加或减少变量值，以便满足条件。

一旦我们完成了变量初始值的赋值和条件，以及增加/减少变量值，我们就准备好编写要执行的语句，直到满足条件。让我们通过示例来理解它……

## For 循环示例

让我们考虑上一个例子并尝试打印 10 遍 "I love JavaScript"。我们将从创建一个变量开始。

```javascript
var i;
```

接着按照以下方式编写 for 循环：

```javascript
for(i = 1; i<= 10; i++)
```

这里需要注意的是，初始值、条件和计数器语句之间是用分号（";"）分隔的。

到为止，我们已经写了以下代码：

```javascript
var i;
(i = 1; i<=10; i++)
```

现在，我们只需要在大括号内编写语句，它将被重复 10 遍。

```javascript
var i;
for(i = 1; i < 10; i++){
  document.write("I love JavaScript");
}
```

## Do..While 循环

Do..while 循环与 for 非常相似。
从名称中我们可以猜到，do..while 循环有两个主要部分：

- do：这是我们编写执行代码直到其满足条件的地方（在大括号内）。
- while：这是我们提到条件的地方（在圆括号内）。

让我们来看一个示例……
### do..while 循环示例

```javascript
do{
  要被执行的代码块
}while(condition);
```

让我们也为 do..while 循环重复相同的示例。
尝试打印 10 遍 "I love JavaScript"。

第一步是创建一个变量。

```javascript
var i = 1;
```

接着编写 do 块。

```javascript
do {
  document.write("I love JavaScript");
  i = i + 1;
}
```

在上面的代码中

通过这种方式我们将满足条件。
到为止，我们已经写了以下代码：

```javascript
var i = 1;
do{
  document.write("I love JavaScript");
  i = i + 1;
}
```

现在，让我们添加 while 部分，并在圆括号中提到条件。

```javascript
var i = 1;
{
    document.write("I love JavaScript");
    i = i + 1;
}
while(i<=10);
```

注意：不要忘记在 while (()) 之后加上分号。

## 对话框

在某些情况下，我们需要传达某些重要的信息，通常我们会大声说出来。
例如，当妈妈给我们购物清单时，她会提到诸如“不要忘记西红柿”、“牛奶应该是无糖的”。
在文章中，作者通常会加粗关键词汇。
同样，在我们想要显示重要信息的网站上，我们展示一种被称为对话框的窗口。对话框是按下特定按键时弹出的小窗口。
它通常用于传递重要消息。

## 对话框的类型

JavaScript 有三种对话框。

这些对话框可以用于显示确认消息、弹出错误或显示警告消息。我们还可以从这些对话框中获取输入。
以下是 JavaScript 中的对话框：

- Alert 对话框（警框）
- Prompt 对话框（提示框）
- Confirm 对话框（确认框）

不要担心；我们将详细学习其中的每一个。

## Alert 对话框

警框通常用于显示消息。
它也可以用于显示警告消息。
警框只有一个“OK”按钮用于选择并继续。
让我们看看如何生成一个警告对话框。
假设你想显示消息“I am a cool dude!”
我们将从编写 alert 关键字开始，后面跟上左、右圆括号。

```javascript
alert();
```

不要忘记分号。
在圆括号之间，我们写入消息。
示例

```javascript
alert("I am a COOL dude");
```

## Prompt 对话框

提示框通常在我们需要用户输入时使用。
它包含两个按钮：“OK”和“Cancel”。
让我们看看如何创建一个……
假设我们想要用户输入。
我们将从编写 prompt 关键字开始，后面跟上左右圆括号。

```javascript
prompt();
```

在圆括号之间，我们写入消息。
示例

```javascript
prompt("What is name?");
```

## Confirm 对话框

确认框通常在我们需要确认时使用。
它包含两个按钮：“OK”和“Cancel”。
让我们看看如何创建一个……
假设我们想要用户确认。
我们将从编写 confirm 关键字开始，后面跟上左右圆括号。

```javascript
confirm();
```

在圆括号之间，我们写入消息。
示例

```javascript
confirm("Are sure you want to delete?");
```

## 函数

假设我们想创建一个程序来打印两个数字之和的结果。
我们将创建两个变量来存储两个数字的值以及另一个变量来存储相和的值。

```javascript
var x = 2;
var y = 3;
var z = x + y;
```

接着按照如下方式打印第3个变量：

```javascript
document.write(z);
```

如果我们需要计算多个组合的结果，例如 1 和 2，4 和 5，6 和 7 呢？
每次都创建一个新变量并加到第三个变量中将是大量的工作。
如果我告诉你有一种方法只需编写一次代码即可用于任何数字组合呢？
即编写可以在程序任何地方使用的可重复代码。
我们要寻找的术语被称为函数。

## 什么是函数？

函数是一个可重复的代码块，可以在程序的任何地方使用。
函数的主要目的是消除重复编写相同代码的需求。

例如如果我们创建一个执行加法的函数，我们可以多次调用它来执行相同的任务，而不是在每次需要加法时都单独编写代码。

## 如何创建函数？

函数只有在被调用时才能被使用。
除非我们调用那个相数字的函数，否则函数将一直处于闲业状态 :p
所以第一步是函数定义，基本上意味着定义函数，即创建一个函数。




一旦我们定义了函数，下一步就是调用并使用它。

函数可以按照以下方式定义：

```
function functionname(){
  code
}
```

我们通过使用 `function` 关键字开始定义函数，后面紧跟函数名，然后是一对圆括号。完成后，我们在大括号内部编写可重用的代码。

## 函数示例

让我们创建一个打印“I know JavaScript!”的函数。我们先从编写 `function` 关键字开始，然后为函数命名并加上开启的圆括号。

```
function print()
```

我们已经将函数命名为 `print`。完成后，让我们在大括号内编写用于打印的代码。

```
function print() {
  document.write("I know JavaScript!");
}
```

是的，函数定义已经完成；让我们继续调用函数吧。

## 调用函数

现在，我们有一个名为 `print` 的函数，它可以打印“I know JavaScript!”。下一步是调用该函数。调用函数非常简单，只需编写函数名并加上一对圆括号。因此，整个代码看起来像这样：

```
function print() {
  document.write("I know JavaScript!");
}
print();
```

## 参数

我们为什么在函数内部需要外部变量？

让我们在加法函数的基础上继续。
我们将创建一个函数，接着声明两个变量，然后在第三个变量中执行加法，最后将其打印出来。
最后，我们将调用该函数。
正如我们之前提到的，函数的主要目的是让代码可重用。
那么，我们如何向函数存入不同的值以便它打印结果呢？解决方案就是参数（Parameters）！

```
function functionname(parameter){
  code
}
functionname(parameter)
```

参数在调用函数时传递，稍后这些传递的参数可以在函数内部进行操作。
也就是说，假设我们在调用 `add` 函数时传递了 2 和 3，然后在函数内部可以使用可以使用定的参数（即 2 和 3）进行相加并将其打印出来。
同样地，我们可以将 4 和 5 作为参数传递给该函数，并打印结果。
从而成功地实现了我们函数的可重用。
让我们写一个程序来清晰地了解这一点。

## 示例

让我们创建一个两个数字之和的函数。
让我们从创建一个函数开始。

```
function add(){
}
```

现在，由于我们将使用**参数**来调用此函数，因此在创建函数时必须提到它。我们是这样做的：

```
function add(num1, num2){
}
```

在这里，**num1** 和 **num2** 是我们在调用函数时作为参数获取的两个数字。
现在，让我们创建一个**变量**来存储最终结果的值。

```
function add(num1, num2){
  var result = num1 + num2;
  document.write(result);
}

add(3,4);
```

我们已准备好调用函数了！

在这种情况下，我们将 3 和 4 作为参数传递给函数。
因此，`num1` 变为 3，`num2` 变为 4，结果变量 `result` **存储**了结果并将其打印。

## 作用域

你多久以及在什么情况下使用“作用域”（scope）这个词？
在通常情况下，如果你可以访问某个东西，它就在你的作用域范围内，否则它就在你的**作用域**之外。同样的概念适用于编程。

**变量**的可访问性或有效性是由其**作用域**决定的。
假设一个变量声明在函数内部。如果我们尝试在函数外部访问该变量。
那么我们将遇到一个错误，提示我们尝试访问的变量未定义。

在 JavaScript 中有两种类型的作用域：

- 局部作用域 (Local Scope)
- 全局作用域 (Global Scope)

让我们详细探索每一个。

## 局部作用域

每当变量在函数内部声明时，被称为具有**局部作用域**。在函数内部声明的变量只能在该函数内部。让我们写一个函数 `localFunction` 并在内部声明一个变量 `localVar`。

```javascript
// 这将定义一个函数
function localFunction(){
    // 这将创建一个变量并
    // 存储值 50
    var localVar = 50;
}
```

在这里，localVar 是一个变量，其作用域局限于函数 `localFunction`。
现在，让我们尝试在函数外打印 `localVar` 的值。

```javascript
// 这将定义一个函数
function localFunction(){
  // 这将创建一个变量并
  // 存储值 50
  var localVar = 50;
}
// 这将打印变量的值
console.log(localVar);
```

你能猜到上述代码段的输出吗？
我们将遇到一个错误，类似于
`Uncaught ReferenceError: localVar is not defined`
因为该变量的作用域局限于函数。

```javascript
// 这将定义一个函数
function localFunction() {
  // 这将创建一个变量并
  // 存储值 50
  var localVar = 50;
  // 这将打印变量的值
  console.log(localVar);
}
// 这将调用函数
localFunction();
```

上述代码段的输出将是一个错误，因为该变量的作用域局限于函数。

## 全局作用域

随处可以访问的变量具有全局作用域。
这些变量没有在任何函数内部声明。让我们来看看。

```javascript
// 创建一个变量并存储值 50
var globalVar = 50;

// 这将定义一个函数
function localFunction(){
    // 这将打印变量的值
    console.log(globalVar);
}
```

程序的输出将是 50，因为 globalVar 定义在函数外部。

## 变量提升 (Hoisting)

在 JavaScript 中，所有的变量声明都会移动到顶部。这被称为变量提升。
这意味着变量可以在声明之前使用。

```javascript
var newVar;
console.log(newVar);
newVar = 50;
```

## 字符串 (String)

字符串是字符序列。
你在屏幕上看到的所有文本数据都是字符串。在 JavaScript 中，字符串用于存储和处理数据。
写在引号内部任何字符串。

```javascript
var newStr = "Hey! I am a string.";
```

在这里，newStr 的类型为字符串 "Hey! I am a string."
在这里，newStr 是一个字符串类型的变量。
"Hey! I am a string" 是该变量的值

与其他所有变量声明一样，字符串使用 `var` 关键字声明。

```javascript
var strName = "Mike";
```

JavaScript 接受单引号 ('') 和双引号 ("") 包裹字符串。
注意不要混合使用。
如果你使用单引号开始字符串，你应该用单引号结束。
如果你使用双引号开始字符串，你应该用双引号结束。

太好了，我们知道如何在 JavaScript 中声明和初始化字符串。
让我们看看一些用于对字符串操作的内置属性和方法。

## 查找字符串的长度

要找到字符串的长度，我们使用内置的 `length` 属性。使用该属性时我们写：

```
stringName.length;
```

那么，为了找到字符串 "HeyString" 的长度应该写什么？

```javascript
// 创建一个变量并存储字符串值
var newStr = "HeyString";
// 查找定义变量的长度
// 并存储在另一个变量中
var strLength = newStr.length;
```



你能猜到输出会是什么吗？
我们将得到变量长度为 9。

## 合并两个字符串

要合并或拼接两个字符串，可以使用 `concat()` 方法。

```javascript
string1.concat(string2);
```

就是如此！
该方法返回一个在 `string1` 之后连接 `string2` 形成的新字符串。

```javascript
-- 这将创建一个变量并存储一个字符串值 -->
var string1 = "Hey";
-- 这也将另一个变量并存储另一个字符串值 -->
var string2 = "String";
-- 这将创建一个变量并存储前两个变量值的组合 -->
var string3 = string1.concat(string2);
```

因此，`string3` 的值将是 HeyString。
这就是字符串拼接的工作原理。
字符串拼接也可以使用 `'+'` 运算符来实现。

```javascript
-- 这将创建一个变量并存储一个字符串值 -->
var string1 = "Hey";
-- 这也将另一个变量并存储另一个字符串值 -->
var string2 = "String";
-- 这将创建一个变量并存储前两个变量值的组合 -->
var string3 = string1 + string2;
```

因此，`string3` 的值将是 **HeyString.**

## 查找子字符串

**substr()** 方法用于从字符串中提取子字符串。
它接受两个参数，

```javascript
`stringName.substr(starting index of substring, length of the substring);
```

让我们从 **"I am in love with strings."** 中提取一个子字符串。

```javascript
-- 这将创建一个变量并存储一个字符串值
var myString = "I am in love with Strings.";
-- 这将从变量中提取一个字符串
-- 从位置 5 开始，长度为 7 --
myString.substr(5,7);
```

语句 `myString.substr(5,7)` 表示从第 5 个位置开始选取 7 个字符。
上面的代码段将返回 "in love "
记住！空格被算作一个字符。

## 将字符串转换为大写和小小写

没有什么更好的内置方法可以将字符串转换为大写和小小写了。
`toUpperCase()` 方法用于将字符串转换为大写。
而 `toLowerCase()` 方法用于将字符串转换为小写。
让我们来看看实际效果。

```javascript
-- 这将创建一个变量并存储一个字符串值
var myString = "Don't mess with my case.";
-- 这将变量的值转换为大写 --
myString.toUpperCase();
```

上面的代码段将返回 "DON’T MESS WITH MY CASE."
而编写

```javascript
<-- 这将变量的值转换为
小写 -->
myString.toLowerCase();
```

将返回 "don’t mess with my case. "

## 数字和布尔值

与其他编程语言不同，JavaScript 没有为整数和浮点设置不同的数据类型。
数字被归类为**一种数据类型**，即 **number**。
因此，**5** 和 **5.62** 都具有相同的类型 **number**。
与其他任何**变量声明**一样，数字也使用 `var` 关键字进行声明。
例如：

```javascript
var height=5.62;
var age=19;
```

在这里，`var` 是关键字，`Height` 和 `age` 是变量名，5.62 和 19 是变量的对应值。
变量 `height` 和 `age` 的类型都是 **number**。
太棒了，我们知道如何在 JavaScript 中声明数字了。
让我们跳转到可以在这些数字上执行的操作。
JavaScript 有许多内置方法来实现。让我们探索其中的几个。

## 数字的四舍五入

很多时候，我们需要将数字四舍五入到固定的小位数。
这时 `toFixed()` 方法就上场了。
如何使用它？

```javascript
variable_name.toFixed(number_of_decimal_places);
```

示例：
将 3.142 四舍五入到两位，我们写道：

```javascript
var myNum=3.142;
myNum.toFixed(2);
```

```javascript
-- 这将创建一个变量并存储一个
小数 --
var newNum = 34.463;
-- 这将被变量四舍五入
到 2 位小数 --
newNum.toFixed(2);
```

上面的方法将返回 34.46 。
并且，`newNum.toFixed(0)` 将返回 34。




```javascript
// 这将使用 new 关键字创建一个对象 --
var Student = new object();
-- 这将访问对象的第 1 个项并赋值字符串值 --
Student.name = "Favour";
-- 这将访问对象的第 2 个项并赋值整数值 --
Student.class = 10;
-- 这将访问对象的第 3 个项并赋值整数值 --
Student.roll_no = 45;
```

在这里，使用点运算符 (.) 来编写键名并为其赋值值。

## 使用对象构造函数

对象构造函数是一个函数，其名称与对象的名称相同。

```javascript
-- 这将定义一个与对象同名的构造函数 --
function Student(name, class, roll_no) {
  -- 这将将用户定义的值赋值给项 --
  this.name = name;
  this.class = class;
  this.roll_no = roll_no;
}
// 这将创建一个对象并将值作为参数传递给构造函数 --
```

this 指向当前对象。
值作为参数传递给对象构造函数。

## 访问对象属性

访问任何对象的属性与上面的示例类似。
你需要某些东西，只需请求它即可。继续吧。加油。试一下。
“Object Student 我需要知道你的名字。”就这样。
但是，JavaScript 并不智能到解析那个句子。
所以，让我们用 JavaScript 能理解的格式编写相同的内容。
访问对象属性有两种方法。

- 使用点运算符
- 使用方括号表示法

让我们逐一探索每一种。

## 使用点运算符

相同的语法也可以用于编写新属性，也可以重新分配现有属性的值。

```javascript
Student.name = "Favour";
```

将替换对象中 name 的当前值。并且，

```javascript
Student.house = "Green";
```

将向对象添加一个值为 Green 的属性 house。

## 使用方括号表示法

我们也可以使用方括号 [ ] 访问对象属性。

```javascript
Student['name'];
```

返回与 Student.name 相同的结果。而且，编写 Student['name'] = "Favour"; 将为对象 Student 的 name 属性分配一个新值。同样，我们可以添加新属性。

## JavaScript 中的日期

JavaScript 可以帮助你获取日期。
你只需要抓住 JavaScript 提供的礼物 - **日期对象 (Date Object)**。
就这样。然后你就可以创建自己的日期了。
Date 是内置的 JavaScript 对象。
它是一个 JavaScript 对象。
你还能回想起对象由什么组成吗？
我们已经学习它由某些属性和方法组成。
我们将在后续章节中探索其中的一些。

使用此对象，我们可以获取如当前年份、当前日期、当前星期和当前时间等信息。
此外，我们可以指定一个新的日期和一个新的时间。
而且，我们还可以对这些值进行操作，从处理日期格式到查找两个日期之间的差。

你是否想过这个对象是如何处理日期的？

嗯，它根据 Unix 时间戳来理解和存储日期

这无非是自 1970 年 1 月 1 日星期四以来所经过的毫秒数吗？
我们将在接下来的章节中看到用于获取毫秒级日期的方法。

让我们探索这个日期对象，找出可以进行哪些操作。

## 对日期的操作

让我们从**定义日期对象的实例**开始。
你还记得我们如何使用 new 运算符来编写一个对象的实例吗？

```javascript
// 这将创建一个
// Date 对象的实例 -->
var myDate = new Date();
```

这将初始化一个日期对象的新实例。
你能猜到 myDate 变量的值吗？
变量 myDate 将包含类似于 
Wed Mar 28 2018 01:08:46 GMT+0530 (India Standard Time)
的内容内容

这是一个包含日期、月份、年份、时间和时区的长字符串。
这无非是当前的日期和时间。
所以，编写

```javascript
var myDate = new Date();
```

将当前的日期和时间存储在变量 myDate 中。
是时候探索日期对象中存在的一些常用方法了。
记得，我们学习过可以获取当前年份、当前日期、当前星期、当前时间等等！
要获取所有这些信息，请使用以下方法：

- getDate() - 返回月份中的几几。一个 1 到 31 之间的数字。
- getDay() - 返回当前的星期。一个 0 到 6 之间的数字。
- getTime() - 返回自 1970 年 1 月 1 日以来经过的毫秒数，这无非是当前时间。
- getFullYear() - 返回当前年份。
- getMonth() - 返回当年的月份。

同样，getMinutes(), getHours(), getSeconds() 是日期对象中存在的其他方法。

如何使用这些方法？
它就像 ABC 一样简单。

```javascript
// 这将创建一个 Date 对象的实例 -->
var myDate = new Date();
// 这使用点运算符调用所需的方法 -->
myDate.getFullYear();
```

上面的方法 getFullYear() 目前将返回 2018。
同样，也可以使用其他方法来获取相应的数据。

你注意到网站上版权符号旁边提到的年份了吗？
我很确定，到目前为止你已经猜到它是如何运作的。
使用 myDate.getTime() 继续前进并探索日期对象中存在的更多方法。
就像我们可以从日期对象中获取数据一样，我们也可以设置自己的数据。

为了做到，它提供了以下方法：

- setDate() - 设置月份中的几几。一个 1 到 31 之间的数字。
- setTime() - 设置自 1970 年 1 月 1 日以来经过的毫秒数。
- setFullYear() - 设置年份。
- setMonth() - 设置当年的月份。

同样，setMinutes(), setHours(), setSeconds() 是日期对象中存在的其他方法。

```javascript
// 这将创建一个 Date 对象的实例 -->
var myDate = new Date();
// 这使用点运算符调用所需的方法 -->
myDate.setFullYear(2025);
```

上面的方法将年份设置为 **2025**。
同样，也可以使用其他方法。

## 文档对象模型 (DOM)

你可以在纸上画出你的家族树吗？
从你的祖先、祖父，然后是你。

DOM 或文档对象模型是应用程序的灵魂。
它是由浏览器创建的树形结构。
它由元素、属性、值组成。

因此，HTML 定义了一种标准，通过它我们可以添加、删除或获取元素。
让我们看看它实际上是什么样的。
考虑一个具有以下标记的基础网页。

```html
<html>
<head>
</head>
<body>
<p></p>
</body>
</html>
```





- 2. getElementsByClassName() - 使用元素分配的类（class）来查找元素。
3. getElementById() - 使用分配的 id 来查找元素。

所以，让我们来看看这三个方法的实际应用。

## 使用标签名访问

假设我们想访问网页中所有的 `<p>` 标签。
我们可以直接写：

```
document.getElementsByTagName('p');
```

上述方法将获取网页上存在的所有 `<p>` 标签。

## 使用类名访问

现在，为了使用元素中存在的类来访问元素，我们使用 `getElementsByClassName()` 方法。
要访问如所示具有类 `newClass` 的 `<p>` 标签，我们可以写：

```javascript
document.getElementsByClassName('newClass');
```

这将选择所有包含类 `newClass` 的元素。

## 使用 ID 访问

为了使用元素中存在的 id 来访问元素，我们使用 `getElementById()` 方法。
我们可以访问分配了 id `newId` 的 `<p>` 标签，
我们写道：

```javascript
document.getElementById('newId');
```

这将选择包含 id - newId 的元素。

## 使用 JavaScript 访问 HTML 元素

通过 JavaScript，我们可以操作网站的 HTML。你还记得浏览器会创建一个对象树结构，被称为 DOM 或 Document Object Model（对象模型）吗？要更改 HTML，我们必须对 DOM 进行更改，而对 DOM 的更改将反映在我们的网页上。这一切都在弹指间瞬间完成。

但在我们学习**如何更改 HTML 内容**之前，我们应该先知道**如何通过 JavaScript 访问我们网站的 HTML**。

使用 JavaScript 访问 HTML 内容有许多方法。

### 使用标签名

**document** 对象（无非就是我们的 DOM）提供了一个通过标签名访问元素的方法。

```
getElementsByTagName();
```

该方法接受**标签的名称**作为参数，并返回所有具有相同标签名的元素。所以，如果我们写

```javascript
getElementsByTagName("h1");
```

该方法将返回所有带有 `<h1>` 标签的元素。由于该方法是 **document 对象**的一部分，要使用它我们需要写：

```javascript
document.getElementsByTagName("h1");
```

就这样。我们将拥有所有可以修改的 `<h1>` 元素。

## 使用类名

我们都知道 HTML 元素包含类属性（class attributes）。
并且可以使用这些类名来识别它们。
在 JavaScript 中实现这一点，document 对象提供了一个方法。

```
getElementsByClassName();
```

该方法接受类名作为参数，并返回包含该类的元素。
所以，为了访问上面图片中的 `<p>` 元素，我们需要写：

```javascript
document.getElementsByClassName("custom-p");
```

这将返回包含类 `custom-p` 的元素。在这种情况下，它将返回该 `<p>` 元素。

## 使用 Id

用于通过 id 访问元素的方法是：

```
getElementById();
```

该方法接受 **id 的名称**作为参数，并返回具有该 id 的元素。
要访问上述 `<p>` 元素，我们可以写：

```javascript
document.getElementById("custom-id");
```

## 使用 CSS 选择器访问 HTML 元素

CSS 选择器用于选择你想要样式的元素，这些元素可以是 id、类名、类型、属性、属性值等。
我们有两种方法可以根据指定的 CSS 选择器来访问 HTML 元素。

- 1. `querySelector()`
- 2. `querySelectorAll()`

使用 `querySelector` 是访问 DOM 元素的一种现代方法。
该方法接受选择器作为参数并返回相应的元素。
让我们理解一下它们是如何工作的。

**querySelector()** 方法只返回匹配指定选择器的第一个**元素，而 **querySelectorAll()** 返回所有匹配的元素。

这两个方法都接受类名、id 和元素名作为参数。

```javascript
document.querySelector(".className"); // 使用类访问
document.querySelector("#idName"); // 使用 id 访问
document.querySelector("tagName"); // 使用标签名访问
```

`querySelectorAll()` 可以像上面一样使用。

## 使用 JavaScript 操作 HTML 元素

现在我们知道如何访问 HTML 元素了。
同时我们也知道如果对 DOM 进行任何更改，这些更改都会反映在我们的网页上。
操作 HTML 元素只是一个两步过程：

- 1. 选择 HTML 元素。
- 2. 对它进行操作

使用 JavaScript 可以对 HTML 做很多事情。

## 编写 HTML 内容

JavaScript 提供了 `innerHTML` 属性，可以设置 HTML 内容。
显然，我们需要做的第一件事是访问元素。然后使用点运算符使用 `innerHTML` 属性：

```javascript
document.getElementById("lone-p").innerHTML = "Here is some text for you!";
```

这将在网页上打印“Here is some text for you !”。

## 更改 HTML 内容

如果 `<p>` 元素中已经存在某些文本怎么办？
那么写

```javascript
document.getElementById("not-alone").innerHTML = "Replaced you!";
```

将覆盖现有文本并将其替换为新值。
让我们通过一个示例来看看它的工作；
我们还可以通过在 `innerHTML` 属性的值中编写标签来添加 HTML 标签：
例如，我们考虑这个 `<p>` 元素。

```html
<!-- 这将声明一个带有 id 的段落 -->
<p id="bold-me"></p>
```

我们想在上述 `<p>` 元素内部编写一些加粗文本。我们可以这样做：

```html
<!-- 这将设置段落设置内容 -->
document.getElementById("bold-me").innerHTML = "<b>Bold text</b>";
```

## 创建新元素

让我们探索如何使用 JavaScript 创建新元素。
这样做，我们使用 document 对象的 `createElement()` 方法。

```javascript
document.createElement("p");
```

现在你足够聪明，知道我们要创建的元素。

```html
<!-- 这将创建一个带有 id 的 div -->
<div id="meDiv"></div>
```

## 插入元素

假设我们要向现有的 `div` 插入元素。我们知道如何创建一个新元素，但还需要将其**插入**。

```javascript
<!-- 创建新元素并将其存储在变量中 -->
var newEl = document.createElement("p");
<!-- 创建文本并将其存储在变量中 -->
var someText = document.createTextNode("Some Text!");
<!-- 将文本插入新元素 -->
var insertThis = newEl.appendChild(someText);
<!-- 将 p 元素插入 div -->
document.getElementById("meDiv").appendChild(insertThis);
```

## 移除元素

考虑下面的 HTML。

```html
<!-- 创建一个带有 id 的 div -->
<div id="thisDiv">
  <!-- 创建带有 id 的段落并文本 -->
  <p id="thisP">
    Hehe! I am going to die.
  </p>
</div>
```

我们希望移除 div 内部的 `<p>` 元素。
这样做我们有 `removeChild()` 方法。

```javascript
<!-- 带有特定 id 的 div -->
var divEl = document.getElementById("thisDiv");
<!-- 段落元素 -->
var pEl = document.getElementById("thisP");
<!-- 从 div 中移除段落元素 -->
divEl.removeChild(pEl);
```

## 设置属性

虽然我们在上面的示例中删除了标签，但学习 JavaScript 仍然酷。

属性提供了元素的额外信息。我们可以使用 JavaScript 设置元素中存在的属性值。这可以通过 `setAttribute()` 方法实现。该方法接受两个参数 - 属性名称和它的值。

```
setAttribute("attribute", "value");
```

让我们看看它是工作的。让我们尝试给下面的锚点标签添加 `href` 属性。

```html
<!-- 创建带有给定文本的链接 -->
<a>Google</a>
<!-- 访问锚点元素 -->
var aEl = document.querySelector("a");
<!-- 在 <a> 标签中设置 href 属性 -->
aEl.setAttribute("href", "http://google.com");
```

这将为锚标签添加 `href` 属性。同样，也可以添加其他属性。如果属性已经存在，则它的值将被替换。

要移除任何属性，我们使用 `removeAttribute()` 方法。假设我们要从元素移除 `href` 属性。





```html
<!---- This will create a link -->
<a href="http://niflare.com">Niflare</a>
```

要做到这一点，我们可以写：

```javascript
document.querySelector("a").removeAttribute("href");
```

`removeAttribute()` 方法只接受属性名称作为参数。

## 使用 JavaScript 操控 CSS

JavaScript 确实是一个艺术家。
我们已经看到了它是如何操作网页的 HTML 的。
现在是时候看看它能对 CSS 做些什么了。正如我们预期的，它无所不能的。
它可以更改字体、字体大小、颜色、添加图像等等。

## 操控 CSS

我们可以为任何元素添加任何 CSS 或更改其现有的 CSS。
要做到这一点，我们使用元素的元素的 `style` 属性。
其语法如下：

```javascript
el.style.CSSProperty = value;
```

其中 `el` 是元素，`style` 是元素的属性，
`CSSProperty` 是要被操控的属性，而 `value` 是该属性的值。
显然，我们需要先访问元素来更改它的属性。

```html
<!---- This will print the paragraph text -->
<p>Here I come. again.</p>
```

让我们看看如何更改 `p` 标签中文字的 `font-size`。

```javascript
<!---- This will access the paragraph element -->
var el = document.querySelector("p");
<!-- This will make paragraph font-size 25px -->
```

这将使 `p` 标签中文字的 `font-size` 等于 25px。
如果我们想更改文字的颜色怎么办？
要做到这一点，我们只需写：

```javascript
el.style.color = "green";
```

这将文字颜色更改为绿色。
你想让我让文字不可吗？
这可以通过 `display` 属性来实现。

```javascript
el.style.display = "none";
```

这将段落的 `display` 属性设置为 `none`，文字将会被隐藏。
我们还可以更改文字的背景颜色。
要做到这一点，我们需要写：

```javascript
el.style.background = "red";
```

这将背景颜色设置为红色。
同样地，我们可以更改外边距（margin）、内边距（padding）、边框（border）、更改对齐方式等。
基本上，所有能用 CSS 到的事情。

我们已经学习了**如何使用 JavaScript 更改 CSS**。

## JavaScript 中的事件

**事件**（event）是一种发生。
JavaScript 在遇到事件时主要与 HTML 交互。

事件可以通过用户的操作发生，也可以通过浏览器本身的操作发生。
**点击按钮、悬停**、调整浏览器窗口大小、按下键盘上的键都是用户完成的事件。而**网页的加载**、调整浏览器窗口是发生在浏览器上的事件。

JavaScript 是一种强大的语言。
它在这些事件发生时利用力量采取行动。
我们可以决定在这些事件发生时想要执行的动作。
为了这个目的，每个事件都有一个**事件处理器**（event handler），它是一个在事件发生时运行的代码块。

## 事件类型

是时候学习不同类型的事件了。

- **onclick()** - 当任何 HTML 元素被点击时触发此事件。
- **onload()** - 当浏览器完成加载网页时触发此事件。
- **onkeydown()** - 当按下键盘上的任意键时，发生此事件。
- **onmouseout()** - 当指针移出任何元素时，发生此事件。
- **onmouseover()** - 当指针移动到任何元素上，发生此事件。

这个列表是无尽的。
但这些是一些最常用的事件。
让我们学习如何将这些事件绑定到我们的 HTML 元素。

## 将事件绑定到 HTML 元素

将事件绑定到 HTML 元素无非决定当某个事件发生在该元素或页面上会发生什么。

事件有两种编写方式。
第一，内联编写事件。

假设有一个按钮，我们为它分配一个点击事件。
让我们看看如何做：

```html
<button onclick="alert('Oh! Clicked.')">Click me</button>
```

在这里，我们在按钮本身的 `onclick` 属性中定义了需要执行的动作...
就是这样。点击按钮时会弹出一个警告框。

当要执行的动作是简单的时，使用这种方法。

另一种方法是在点击按钮时调用在程序其他地方定义的函数。
这种方法用于函数复杂的情况，而且它将 HTML 代码和 JavaScript 代码分开结构。

```html
<button onclick="clicked()">Click me</button>
```

在 JavaScript 中：

```javascript
function clicked(){
  alert('Oh! Clicked.');
}
```

但还有另一种方法，允许我们将事件绑定到 HTML 元素，而不是直接写在 HTML 元素内部。

这是通过 `addEventListener()` 函数实现的。使用 `addEventListener()`，我们可以将事件绑定到 HTML 元素。让我们看看如何。尝试给按钮绑定同一个点击事件。

```html
<button>Click Me</button>
```

在 JavaScript 中：

```javascript
<!---- This will access the button element -->
var myBtn = document.querySelector("button");
<!-- This will add an event using proper method -->
myBtn.addEventListener('click',function(){
  alert('Oh! Clicked.');
});
```

（注：由于原文中存在大量重复和 OCR 错误，以上翻译已根据核心逻辑进行了整理和清理。）





## Cookies

JavaScript 中的 Cookies 允许我们在用户的浏览器中存储数据。
Cookie 是存储在用户浏览器中的一段数据。
但为什么我们需要在浏览器中存储数据呢？
当我们想要记住用户信息时，它就非常有用。
例如记住你在特定网站的用户名，这样当你再次访问同一网站时，就不需要再次输入。或者存储会话变量——用于在不同页面之间维持登录会话。
JavaScript 可以读取、创建、修改和删除 cookies。
让我们来看看如何操作。

## 创建 cookie

可以通过文档对象的 `cookie` 属性创建 cookie。
创建 cookie 使用以下语法：

```
document.cookie = "key=value";
```

其中 key 是 cookie 的名称，value 是 cookie 的值。

## 创建多个 cookies

我们无法通过 `document.cookie` 一次创建多个 cookie。
写入多个 cookie：

```
document.cookie = "key1=value1";
document.cookie = "key2=value2";
```

我们需要反复使用 `document.cookie` 写入所需数量的键值对。
Cookies 带有过期日期。是的，它们不是永久的。

## 删除 cookie

默认情况下：

```document.cookie = "key=value; expires=Date";
```

`expires` 取 `Date` 作为值。

## 读取 cookies

既然我们已经知道如何创建 cookie，让我们来看看如何读取当前激活的 cookies。
写入 `document.cookie` 会返回已经存在的 cookies。

```
var myCook = document.cookie;
```

上述操作将包含所有 cookie 信息的字符串存储在变量 `myCook` 中，其格式为相同的键值对格式。

## 在 JavaScript 中修改 cookie

我们可以以创建 cookie 的方式修改 cookie 的值：

```
document.cookie = "username=Favour Niflare; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";
```

旧 cookie 将被新 cookie 替换。

也可以删除现有的 cookies。
要这样做，我们只需要在 `expires` 字段中写一个过去的日期即可。

```document.cookie = "key=; expires=Past_date;";
```

其中 key 是要删除的 cookie 名称。
删除 cookie 时不需要指定值。

# 开始学习 es6

到为止我们一直在学习 ECMAScript。
**ECMAScript 不过是 JavaScript 的另一个名字...**

ECMA 是一个信息和通信系统的标准组织。
JavaScript 的标准化实现被称为 ECMAScript。

简单来说，我们可以说 JavaScript 是受 ECMA 标准规范的。

标准化以周期形式进行，**ECMAScript 的第六个主要大版本**（也称为 **es6**）于 2015 年发布。

**ES6** 带有许多新**特性**。

其中一些特性在很大程度上增强了我们在 JavaScript 中执行最常见操作的方式。

## let and const

在 ES6 之前，`var` 变量使用 `var` 声明。
使用 `var` 声明的变量是**函数作用域 (function scoped)**。
在 ES6 中，我们可以使用 **let** 和 **const** 来声明变量。
**let** 与 *var* 相同，但它是**块作用域 (block scoped)** 的，与 var 不同。

## 什么是块作用域？

每个每个函数都会创建一个`函数作用域 (function scope)`。
而当我们编写条件语句或循环时，会创建一个`块作用域 (block scope)`。

## let vs var

当我们学习作用域时，看到在函数内部使用 `var` 声明的变量在函数外部是不可用的。

但是，在块作用域内部使用 `var` 声明的变量在块外部仍然可用。
例如：

```
for(var count=0; count<5; count++) {
  //some action 
  console.log(count);
}
```

变量 `count` 在块作用域外部可用，且其值会被记录为 5。
我们并不真的需要块变量存在块外部。
这就是 `let` 派上用场的地方。
如果我们写：

```
for(let count=0; count<5; count++) {
  //some action 
} 
console.log(count);
// Reference Error**
```

`const` 用于声明常量变量。
它的工作方式与 `let` 完全相同，但使用 `const` 声明的变量值在整个程序运行期间保持不变。
`let` 和 `const` 都用于声明变量。





上面的类简单地获取学生的姓名和学号并返回它们。我们已经成功声明了第一个类。但如果不去使用它，它只是一个模板。让我们看看如何编写该类的实例并访问类方法。

## 访问类成员

可以通过创建类的实例来访问类的成员。
对象被用于访问变量并给变量赋值。
这是通过使用 `new` 关键字来实现的。

```js
let objName = new ClassName();
```

`new` 关键字用于实例化对象以备使用。
`ClassName()` 是类构造函数的名称。
让我们写一个 `Student` 类的实例。

```javascript
<-- 这定义了一个类 -->
class Student{
  -- 这定义了类的构造函数 -->
  constructor(name, roll_no){
    -- 这初始化变量 -->
    this.name = name;
    this.roll_no = roll_no;
  }

  -- 这定义了类的方法 --
  showName(){
    -- 这是一个返回方法
    return name;
  }

  -- 这定义了类的另一个方法 --
  showRoll(){
    -- 这是一个返回 roll_no 的方法 -
    return roll_no;
  }
}
<-- 这创建了一个带有参数的定义类的实例 -->
```

就是这样！现在我们可以调用 `showName()` 和 `showRoll()` 函数了。

```js
-- 使用实例变量调用第1个方法 --
student1.showName();
-- 使用实例变量调用第2个方法 --
```

这将调用上述方法，它们将分别返回 Favour 和 45。太棒了，我们学习了如何编写类以及如何类的实例来访问它们。
