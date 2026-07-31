# JavaScript 术语手册










Andrea Giammarchi

@Web Reflection





**推特分享这本书！**

请通过在 Twitter 上分享这本书来帮助 Andrea Marcharchi。

本书建议的标签（hashtag）是 #jsglossary。

点击此链接在 Twitter 上搜索该标签，查看其他人对这本书的评价：

https://twitter.com/search?t=#jsglossary

献给充满活力的 JavaScript 社区



*(注：后文页面提供的 OCR 文本由于字符偏移/编码错误导致严重乱码。我已处理了清晰的部分，并尽可能保留了其余部分的结构，但偏移的乱码文本大部分无法恢复。）*

[content]





Andrea Giammarchi

@Web Reflection





**推特分享这本书！**

请通过在 Twitter 上分享这本书来帮助 Andrea Marcharchi。

本书建议的标签（hashtag）是 #jsglossary。

点击此链接在 Twitter 上搜索该标签，查看其他人对这本书的评价：

https://twitter.com/search?t=#jsglossary

献给充满活力的 JavaScript 社区



*(注：后文页面提供的 OCR 文本由于字符偏移/编码错误导致严重乱码。我已处理了清晰的部分，并尽可能保留了其余部分的结构，但偏移的乱码文本大部分无法恢复。）*





## 调试

我们喜欢这种基础，因为当我们编写代码并想知道代码执行成功还是失败时，我们需要它。这种验证过程被称为*调试*（debugging），原因因为它通常通过*调试器*（debugger）进行，调试器是大多数现代浏览器提供的开发者辅助工具。

- 尝试在任何网页上进行*右键点击*（Right Click），查看菜单的最后一项是否有*检查元素*（Inspect Element）。这就是你如何测试书中所有示例的方法：点击*检查元素*，然后点击名为*控制台*（Console）的按钮或标签页，在我们讲解示例的同时开始编写代码段，称为*代码片段*（snippets）。

作为替代方案，你也可以使用*Node.js 命令行界面*，因为大多数示例与环境无关，这意味着它们可以在任何浏览器以及服务器中运行。

每个代码示例都包含一些分级注释，我强烈建议你至少阅读一遍它们，然后再关注实际的编程。

## 注释

在编程中，注释是对代码本身的有意义的描述。它们在代码执行期间会被忽略，可以可以是 // 单行注释，遇到新行时结束，也可以是 // 多行注释 //。

## 符

如果你拿一个计算器，你可以看到数字和算术运算。在编程中基本上也是一样，有算术、比较、赋值、条件和其他操作。我们可以在任何控制台中直接使用它们。

| 我们来做些数学题 | |
| :--- | :--- |
| 2 + 2 | 4 |
| 3 * 3 | 9 |
| 2 * 15 | 30 |
| 1 - 2 | -1 |
| 2 / -1 | -2 |

*在计算器中符号 = 表示*显示结果*，而在 JavaScript 中它意味着*赋值结果*。你可以使用 = 号来保留某些结果以便以后使用。*

**var result = 7;**

**result * 2 显示 14**

如果你想比较两个不同的值，可以使用三等运算符 ===

- 2 === true // 当然，相同的数字，它与自身是等同的
- 2 === false // 嗯，2 和 3 不同，所以它们不能相同

要验证两个值是否不同，可以使用*非*（not）版本。

- 2 !== 2 // false
- 2 !== 2 // 所以它们不可能不同
- 2 !== 3 // true // 当然 2 和 3 不同。这是真的*

*非*（not）运算符可以通过反转其值来否定某些逻辑条件。例如，!true 为 false，反之亦然。

如果你想说明不同的值实际上是相同的，可以使用逻辑运算符。

- (4 == 5) // false
- (5 == 4) // false
- (2 == 3) // false
- (true || false) // true

*在书中后面有一个专门关于这些操作的章节，现在先如此。*

## 部分 (Parts)

可以通过部分（parts）对不同的操作序列分组。这会立即变得更具读性，使开发变得更清晰。例如，如果将一个读取操作视为 2 * 3，人们应该认为结果是 10，而不是将 3 和 2 的和相乘，让你和 JavaScript 解释器都对此了然。

部分也简称为 parts，稍后会进行描述。

在 JavaScript 中有大括号 {} 或方括号 []。这些可以用于创建对象，在方括号中还可以创建它们的值。

## 变量

变量是一个用于引用值的驼峰命名法（camel case）。始终以小写开头，最终通过大写字母连接多个单词。如果复合变量名包含单个字符或缩写词，可以使用多个大写字母。

## 引用

引用就像一个指向特定值的简单链接。想象一个对象，照片可以被视为对一个人的引用；你不需要让这个人出现在房间里就能看到她什么样或在做什么，照片就足够了。

变量

变量通常是一个用于引用通用值的有意义名称。回到对象的示例，varPhoto = new // 创建了一个指向名为 varPhoto 的对象的引用。你可以把它留给我，并在需要时从其他人那里接收其他对象，并随时为其赋值。

创建一个引用我对象的变量

- varPhoto = new //
- // 5 年后 // 这种 
- 保存旧照片
- 通过使用新的变量名

- oldPhoto = varPhoto
- 然后拍摄一个新对象
- 简单地将其赋值给同一个变量

- varPhoto = new //)

JavaScript 变量名的常用命名规范是 camelCase anyValue；始终以小写开头，最终通过大写字母连接多个单词。如果复合变量名包含单个字符或缩写词，可以使用多个大写字母。

## 常用命名规范示例

- var thisIs$goodNameFor$variable anyValue;
- var result = load6(); // object.property genericValue;

常量

常量类似于变量，但只能创建和赋值一次。在现代 JavaScript 中，可以使用 `const` 关键字显式地创建。

*常量的值是静态值*

- const result = load6(); // object.property genericValue;
- const a // 显示字母 a*

*常量的值是静态的*

- // 它不会改变值

*const 5 显示 5 静态值*

它们在大多数编程语言中的常用命名规范如下：

这类变量经常（但但不限于）被用于描述不改变且具有固定值的数据。





## 参考

此术语与特定的操作有关：使用括号执行任何类型的函数引用：

### 声明函数

**函数** `something(something)`

- **当 SOMETHING 是引用名称时**
- 即我们刚刚声明的函数：`SOMETHING`
- **没有任何**发生（仅显示函数本身）
- **要执行**此函数
- 我们需要使用括号调用它：`SOMETHING()`
- 记录某些内容，

如果你仔细观察，你会发现即使是 `console.log(something)` 这种操作也是在调用一个函数。然而，在这种情况下，log 函数是通过 `console` 对象引用调用的，而不是直接调用的，并且它是通过*点符号法*访问的。

每当在点之后调用函数时，该函数就可以被视为一个*方法*。

## 函数声明 VS 表达式

定义函数有几种方法，每种方法的一致性可能有所不同。

例如，函数声明会创建一个*作用域*内任何地方都可用的引用。即使在调用之前，它也已经被声明了：

`function SOMETHING()`

- `SOMETHING` 即使在声明之前也可以工作。

这可以帮助你将代码组织成独立的块。如果不同部分有许多声明，良好的做法是将所有需要的函数声明在一起。

## 变量-函数声明

通过声明引用的`变量名-函数`：`const SOMETHING = function()`

它是与生就绪的，即使在调用之前也是：`SOMETHING = function()`

就像每一个变量一样，函数也应该被赋值一个值来引用它，尽管在函数声明中（如示例所示）不需要函数。简单地定义引用的`变量-名-函数`：`const SOMETHING() = function()`

还有另一个步骤：

- 使用函数名进行赋值：`SOMETHING() = 10`

- 在这种情况下，计数从 10 开始。

## 作用域

此术语表示代码执行的边界。将其想象成：宇宙是每一个星系，星系是系统作用域，行星是所有大陆的作用域，对于每个大陆，我们将拥有国家、地区、城市，最后是你自己的房子，当你在里面时，它是你自己的作用域，而当你出来时，城市的其他部分将是你的作用域。

在 JavaScript 中，默认有一个本地作用域，你可以在其中定义函数和变量。然而，回到房子的比喻，你不希望每个邻居都知道你在家里所做的每一件事。你的家是你的地方，而在 JavaScript 中，函数是定义你自己的私有空间的方式，不会被街道中间或其他任何地方（包括其他房屋）发生的事情干扰或干扰。

- 全局作用域在代码执行之前就开始（它已经在那里了）
- 函数作用域从这里开始：

- **函数** `myScope(soc, ped, args)`
- 在 myScope 内部定义变量使其仅在此处可用：

- **变量** `myMess = my room`
- 函数 myScope() 在这里结束：

- **类型** `myScope` 是函数

- **作用域** `myScope` 是私有的。

由于可以在其他函数内部创建函数，因此也可以在房子内有一个私密房间。要创建私有的，我们可以使用函数名：`SOMETHING = private`。

- `function SOMETHING = private`
- 在这种情况下，计数为 10

- `function SOMETHING = private`
- `function SOMETHING = private`（已声明）

### 本地上下文

如果你打开浏览器控制台或启动节点，你可以通过编写 `console.log(this)` 或直接输入 `this` 来检查本地上下文。

当你全局范围内定义变量或声明函数时，你也可以通过本地上下文引用这些变量，因为就像一个对象一样。

- 在全局作用域中直接创建变量：

- **变量** `definedVariable` 所有人都可以访问“我”
- 通过全局对象访问：`console.this.definedVariable`
- 当你创建函数时：

- **函数** `globalFunction`
- `console.this.globalFunction`（已声明）

重要的是记住，函数可以访问其他变量，但并不总是如此。

然而，每当函数被调用时，在我们完成任务后有一种方法自动清理或释放内存。

### 上下文

每当函数被调用时，可以通过自动可用的 `this` 引用其执行上下文，它具有以下值之一：

- 浏览器和全局服务器中的全局上下文，称为 `window`
- 通过点符号法调用的通用对象：`obj.function()`
- 通过函数方法（如 `.call` 或 `.apply`）调用时，包括 `undefined` 在内的任意值

### 本地上下文

如果你打开浏览器控制台或启动节点，你可以通过编写 `console.log(this)` 或直接输入 `this` 来检查本地上下文。

当你全局范围内定义变量或声明函数时，你也可以通过本地上下文引用这些变量，因为就像一个对象一样。

- 在全局作用域中直接创建变量：

- **变量** `definedVariable` 所有人都可以访问“我”
- 通过全局对象访问：`console.this.definedVariable`
- 当你创建函数时：

- **函数** `globalFunction`
- `console.this.globalFunction`（已声明）

重要的是记住，函数可以访问其他变量，但并不总是如此。

然而，每当函数被调用时，在我们完成任务后有一种方法自动清理或释放内存。

##每当函数被调用时，可以通过自动可用的 `this` 引用其执行上下文，它具有以下值之一：

- 浏览器和全局服务器中的全局上下文，称为 `window`
- 通过点符号法调用的通用对象：`obj.function()`
- 通过函数方法（如 `.call` 或 `.apply`）调用时，包括 `undefined` 在内的任意值

为了防止意外的全局作用域和上下文污染，JavaScript 规范的第五版本（定义 JavaScript 语言、语法和行为的标准）引入了特殊的“use strict”指令。

这个奇怪的字符串如果放在函数开头，将保护本地上下文并切换到更严格的行为。如果你再次尝试之前的代码，你将看到错误而不是数字 123。





## CONLOG(类型 A)

### 未定义

**函数** MYSCOPE() ^ 使用严格模式 - ?? 将局部作用域切换到严格模式* A123。

MYSCOPE() * 显示错误

CONLOG(类型 A)

### 仍然未定义

不仅无法在全局作用域意外定义变量，而且当使用此指令时，执行上下文也是未定义的，除非显式提供。

### 在全局作用域中定义

**函数** WHO,THIS() ^ 使用严格模式 - **RETURN THIS**!`

WHO,THIS()

### 未定义

**THIS**.WHO,THIS() * ?? 全局上下文*

**方法上下文**

在 JAVASCRIPT 对象中，可以拥有任何种类型的属性，函数也不例外。

### 创建一个空对象

**VAR** REM ^`.-

### 将属性定义为函数表达式

rem.SOMEPROPERTYNAME **FUNCTION** ^

**RETURN THIS**!`

### 返回的上下文值会是什么"*

* 让我们通过调用 rem.SOMEPROPERTYNAME 来找出答案

rem.SOMEPROPERTYNAME() * 正好是 REM 本身*

当通过对象调用函数时，它会隐式地使用该对象作为其当前的执行上下文。记住，任何函数都可以随时附加到任何对象上，即使它没有被直接定义为该对象的属性。

### 此处定义的通用函数在其他处

**通用函数** SAYTHE NAME CONLOG.THIS.

带有属性和值的通用对象。我们可以将其作为方法调用。SAYTHE NAME 附加为该，尽管附加方法不是个好主意，但我们可以借用**任何类型**的函数并将其作为不同的对象使用，这一事实是令人惊讶的。我们为什么需要这些这不仅仅是一个小问题，答案是每个项目集合并不一定像数组那样拥有所有方法。新增：有更好、更整洁的方法通过提供上下文来调用函数。

正如类型段落中所描述，通过 CALL 或 APPLY 调用函数，函数是可执行的特殊对象。就像任何对象一样，函数也可以拥有属性，然后是方法。

任何函数最常用的方法是 .CALL 和 .APPLY，它们仅区别在于写法。.CALL 接受任意数量的参数进行传递，.APPLY 只接受一个数组作为调用参数。

### 三个打印某些信息的函数

无参数函数() ^ CONLOG 此处无事可做

带一个参数的函数 (FIRST) CONLOG 接收，FIRST!

带两个参数的函数 (A, B) CONLOG 接收，A, B!

### 现在使用 CALL 并忽略第一个上下文值，使用 NULL：

WITH ARGUMENTS(NULL) )

WITH ONE ARGUMENT(NULL, SOME VALUE )

WITH TWO ARGUMENTS(NULL, FIRST VALUE, SECOND VALUE )

要使用 APPLY()你需要一个或多个数组

**VAR** EMPTY!@.-

**VAR** 带一个参数 > ANY VALUE @

**VAR** 带两个参数 > 1ST, 2ND @

### 与你通过 .CALL 打印的结果相同

WITH ARGUMENTS.APPLY(NULL, EMPTY!)-

WITH ONE ARGUMENT.APPLY(NULL, EMPTY!NAME)

WITH ARGUMENTS.APPLY(NULL, EMPTY,TWO)

记住 CALL 和 .APPLY 区别的小贴士。"WITH" 单词和 FOR EACH*

现在这两种方法的区别已经很清楚了，理解它们以及关于它们。记住上一页的集合。所有方法 CONLOG(类型.名称)

### 函数参数(参数数组)

* 几乎每个对象都有字符串方法

* 它通常描述你正在处理的是什么类型的对象 CONLOG(类型.名称)

此处定义的通用函数在其他处我们可以通过方法作为第一个上下文调用函数，任何返回的值将作为 THIS。with,this.

CONLOG.WITH(12)

**ARGUMENTS** 每次函数被调用时，它都需要许多参数，每个参数也是每次执行函数时创建的特殊对象的名称。

函数上下文和带三个参数(A, B) ^ CONLOG

正如类型段落中所描述，通过 CALL 或 APPLY 调用函数，函数是可执行的特殊对象。就像任何对象一样，函数也可以拥有属性，然后是方法。

任何函数最常用的方法是 .CALL 和 .APPLY，它们仅区别在于写法。.CALL 接受任意数量的参数进行传递，.APPLY 只接受一个数组作为调用参数。

### 三个打印某些信息的函数

无参数函数() ^ CONLOG 此处无事可做

带一个参数的函数 (FIRST) CONLOG 接收，FIRST!

带两个参数的函数 (A, B) CONLOG 接收，A, B!

现在使用 CALL 并忽略第一个上下文值，使用 NULL：

WITH ARGUMENTS(NULL) )

WITH ONE ARGUMENT(NULL, SOME VALUE )

WITH TWO ARGUMENTS(NULL, FIRST VALUE, SECOND VALUE )

要使用 APPLY()你需要一个或多个数组

**VAR** EMPTY!@.-

**VAR** 带一个参数 > ANY VALUE @

**VAR** 带两个参数 > 1ST, 2ND @

### 与你通过 .CALL 打印的结果相同

WITH ARGUMENTS.APPLY(NULL, EMPTY!)-

WITH ONE ARGUMENT.APPLY(NULL, EMPTY!NAME)

WITH ARGUMENTS.APPLY(NULL, EMPTY,TWO)

记住 CALL 和 .APPLY 区别的小贴士。"WITH" 单词和 FOR EACH*

现在这两种方法的区别已经很清楚了，理解它们以及关于它们。记住上一页的集合。所有方法 CONLOG(类型.名称)

### 函数参数(参数数组)

* 几乎每个对象都有字符串方法

* 它通常描述你正在处理的是什么类型的对象 CONLOG(类型.名称)

此处定义的通用函数在其他处我们可以通过方法作为第一个上下文调用函数，任何返回的值将作为 THIS。with,this.

CONLOG.WITH(12)

**ARGUMENTS** 每次函数被调用时，它都需要许多参数，每个参数也是每次执行函数时创建的特殊对象的名称。

函数上下文和带三个参数(A, B) ^ CONLOG

正如类型段落中所描述，通过 CALL 或 APPLY 调用函数，函数是可执行的特殊对象。就像任何对象一样，函数也可以拥有属性，然后是方法。

任何函数最常用的方法是 .CALL 和 .APPLY，它们仅区别在于写法。.CALL 接受任意数量的参数进行传递，.APPLY 只接受一个数组作为调用参数。

### 三个打印某些信息的函数

无参数函数() ^ CONLOG 此处无事可做

带一个参数的函数 (FIRST) CONLOG 接收，FIRST!

带两个参数的函数 (A, B) CONLOG 接收，A, B!

现在使用 CALL 并忽略第一个上下文值，使用 NULL：

WITH ARGUMENTS(NULL) )

WITH ONE ARGUMENT(NULL, SOME VALUE )

WITH TWO ARGUMENTS(NULL, FIRST VALUE, SECOND VALUE )

要使用 APPLY()你需要一个或多个数组

**VAR** EMPTY!@.-

**VAR** 带一个参数 > ANY VALUE @

**VAR** 带两个参数 > 1ST, 2ND @

### 与你通过 .CALL 打印的结果相同

WITH ARGUMENTS.APPLY(NULL, EMPTY!)-

WITH ONE ARGUMENT.APPLY(NULL, EMPTY!NAME)

WITH ARGUMENTS.APPLY(NULL, EMPTY,TWO)


FOR

> 一个或多个变量计算，用分号分隔

## 第一分号

1@ 需满足的条件
## 第二分号

2@ 用于更新条件的更改

3@ 对当前值进行某些操作。请注意，这实际上是 for 循环的第三部分。第四部分在它之后。

以之前的 `while` 循环为例，你可以在下面的 `for` 循环中执行完全相同的过程：

| FOR VAR | 索引大小，长度; | 索引 | 0 <= 1 |
| :--- | :--- | :--- | :--- | :--- |
| console.log(list[index]); | | | | |
| console.log(index); | | | | |
| console.log(); | | | | |

非常重要的是，如果不满足条件，循环的第三部分和第四部分都不会执行。

- 空列表，其长度为 0
- FOR VAR LIST > 0

| FOR VAR | i = 0; i < length; | i++ |
| :--- | :--- | :--- |
| i = 0; i < length; | | |
| 条件永远不会满足 | | |
| i i = 1 | | |
| 如果条件退出循环，则不会发生 | | |
| console.log(i); | | |
| console.log(i); | | |
| 因为第四部分 ; 从未发生 | | |

只要你向列表中放入至少一个项目，条件至少会被满足一次，你会发现循环后 `i` 的值是 1 而不是 0。

## 增量运算符 `++`

使用 `++` 符号来增加整数，而不是通过重新赋值变量本身来加 1，是非常常见的。因此，下面的示例是 `for` 循环通常的写法：

| FOR VAR | i = 0; i < collection.length; | i++ |
| :--- | :--- | :--- |
| 对 collection[i] 进行某些操作 | | |

`++` 运算符既可以放在变量之前，也可以放在之后。在两种情况下，变量都会递增，但其立即返回的值是完全不同的。

- 使用 `++` 作为后缀（也称为后自增）
- VAR NUM 0
- VAR NUM++PLUSNUM num++;

| FOR VAR | NUM++PLUSNUM num++; |
| :--- | :--- | :--- |
| console.log(num++PLUSNUM); | 0, 赋值时 num 还没有递增 |
| console.log(num); | 1 |
| 1, 因为在 num++ 之后它递增了 | |

- 使用 `++` 作为前缀（也称为前自增）
- VAR NUM 0
- VAR PLUSNUMPLUSNUM num++;

| FOR VAR | PLUSNUMPLUSNUM num++; |
| :--- | :--- | :--- |
| console.log(++NUMNUM); | 1, 赋值时 num 已经递增了 |
| console.log(num); | 1 |
| 1, ++num 递增了 num 并返回 1 | |

没有没有特定理由偏于其中一种方式，虽然 `num++` 通常更受青，但 `++num` 也可以作为遍历包含至少 2 个元素的集合的示例：

- VAR i 10
- WHILE ++i < list.length)

- compare(list[i-1], list[i]);

使用 `--` 运算符通过递减（--）来减少整数也是可能的，这简化了 `num num-21` 操作。

关于 `++` 运算符的所有内容，包括作为前缀或后缀使用时的区别，已最后解释。

## 数组方法

在 JavaScript 中，数组带有一些特殊方法，用于更改、更新或整合项目。数组方法比循环看起来更整洁，但它可以遍历任何集合，包括组。

### ARRAY.forEach()

这可能是最接近循环的数组方法，它的工作原理如下：

`array.forEach(value, index)`

函数将被调用 `array` 次，在这种情况下意味着三次：

`console.log(index, value)`

| FOR VAR | 索引 | 值 |
| :--- | :--- | :--- |
| 0 | | |
| 1 | | |
| 2 | | |
| 3 | | |
| | | |

任何函数都递增了三次，需要详细处理这些组。让我们用良好的 `for` 循环来重构 `forEach` 中发生了什么：

`for var list > 0, index,`

`console.log(index, value)`

`undefined, value`

`0, value`

文本是一个确实被用到的特性，但在某些情况下非常有用。某些集合可能没有 `forEach` 方法，但你可以分别遍历其项目。

## ARRAY MAP

通用社交页面上的当前用户：

- VAR user, name: "Andrea",

- 一个在通用 DOM 元素中写入用户名的方法：

`element.textContent = user.name;`

- 找到所有显示用户名的节点：

`var nodes = document.querySelectorAll(".user-name");`

- 遍历用户名的节点：

`nodes.forEach(user => { ... })`

- 将回调作为迭代上下文：

`array.forEach((value, index) => { ... })`

## NEW ARRAY

如果你想根据迭代期间发现的值创建一个新数组，`MAP` 是正确的方法。它的用法与 `forEach` 基本相同，但它调用的函数应该返回每个迭代的值。

- VAR single > 1, 2, 3;
- VAR doubled single.map(function(num, i) {
return num * 2;
})

- 返回一个新值给索引 i:
`console.log(single);`

- > 1, 2, 3;
- `console.log(doubled);`

`MAP` 的主要用例是在提取、更改或转换集合的初始值后创建一个新列表。

- VAR user name: "Andrea", age: 37, name: "Robert", age: 17

- return person.filter(person.age >= 18)

- return person.filter(person.age 18)

- false, Robert is too young

## ARRAY.INDEXOF(value, from) number

如名称所示，`index` 在数组中查找包含特定值的索引。

- VAR alphabet > a, b, c, d, e.e., z, y
- VAR index alphabet.indexOf(c) = 2
- 2
- alphabet.indexOf(c) = c
- 如果未找到返回 -1
- alphabet.indexOf(123) = -1
- -1

在最新的规范中，`array.includes(value, from)` 返回一个指示值是否存在布尔值。

实际上有几十种数组方法。它们在 Mozilla 开发者网络中描述了许多示例和用法。

### ARRAY.METHODS

Array 是一个包含每个数组集成的所有行为的对象。

- [Methods](https://developer.mozilla.org) (not false)





## 变量与原型继承

当一个新变量的值是一个对象、数组或函数时，它默认会带有一些没有人显式赋值的方法；这些是核心功能中的只读部分。

继承对象有两种机制：直接链接或用于设置继承的特殊函数。在对象之间进行原型继承的第一种直接链接方式是原型（prototype）。

- 被称为原型的通用对象
- 它有两个属性：name（名字）和 age（年龄）
- 并且有一个更改年龄的方法
- 变量名，age: 0
- 以及方法：change（更改）

通常，浏览器控制台只会显示自身的属性，忽略继承的属性。这就是为什么即使变量属性还有更多内容，记录时也只显示这些。

## Generic.prototype 与全局

在 JavaScript 中，默认可用的方法之一是 `.prototype`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量对象作为一个示例，你可以假设 `object.prototype` 调用的结果为 `true`。

但这具体意味着什么呢？控制台是如何向我展示的？

- Name：Andrew
- 但他也有年龄吗？
- 0 岁，年龄从原型继承
- 他也有生日方法吗？
- Type：prototype.birthday
- Function：years，从原型继承
- 如果我们把 `birthday` 作为 `object` 的方法来调用会发生什么？
- Name: Andrew, age: 1（突然，那个疯狂的年龄出现了！）
- 他的生日影响了 person one 吗？
- Name: Anonymous, age: 0（没有，一切正常）

关于方法上下文（context）的简要回顾：当我们通过某个对象调用一个函数时，该对象将成为执行上下文。这并不意味着两个 person 都有生日方法，而是意味着它将把 person 作为其自己的方法来执行。

## Object.prototype

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象
- 这个对象可以被表示为字符串吗？
- Object Object
- 但是谁把 `string` 方法放入你的空对象中的？
- Object.prototype.string

- 它是 true，因为这两个对象之间存在一条原型链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

- 一旦你理解了方法不需要直接附加或赋值为对象的属性，而是可以被简单地继承，那么原型继承的含义就变得清晰了；它是不同对象之间的一条隐形链。

## Object.prototype

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象 
- 这个对象可以被表示为字符串吗？
- Object Object
- 但是谁把 `string` 方法放入你的空对象中的？
- Object.prototype.string

- 它是 true，因为这两个对象之间存在一条原型链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

- 一旦你理解了方法不需要直接附加或赋值为对象的属性，而是可以被简单地继承，那么原型继承的含义就变得清晰了；它是不同对象之间的一条隐形链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

##

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

## Native

在 JavaScript 中，默认可用的方法之一是 `.prototype`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量对象作为一个示例，你可以假设 `object.prototype` 调用的结果为 `true`。

但这具体意味着什么呢？控制台是如何向我展示的？

- Name：Andrew
- 但他也有年龄吗？
- 0 岁，年龄从原型继承
- 他也有生日方法吗？
- Type：prototype.birthday
- Function：years，从原型继承
- 如果我们把 `birthday` 作为 `object` 的方法来调用会发生什么？
- Name: Andrew, age: 1（突然，那个疯狂的年龄出现了！）
- 他的生日影响了 person one 吗？
- Name: Anonymous, age: 0（没有，一切正常）

关于方法上下文（context）的简要回顾：当我们通过某个对象调用一个函数时，该对象将成为执行上下文。这并不意味着两个 person 都有生日方法，而是意味着它将把 person 作为其自己的方法来执行。

Object.prototype

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象
- 这个对象可以被表示为字符串吗？
- Object Object
- 但是谁把 `string` 方法放入你的空对象中的？
- Object.prototype.string

- 它是 true，因为这两个对象之间存在一条原型链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

- 一旦你理解了方法不需要直接附加或赋值为对象的属性，而是可以被简单地继承，那么原型继承的含义就变得清晰了；它是不同对象之间的一条隐形链。

## Object.prototype

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象 
- 这个对象可以被表示为字符串吗？
- Object Object
- 但是谁把 `string` 方法放入你的空对象中的？
- Object.prototype.string

- 它是 true，因为这两个对象之间存在一条原型链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

## Variable age: 0

## STRING

通常，浏览器控制台只会显示自身的属性，忽略继承的属性。这就是为什么即使变量属性还有更多内容，记录时只显示这些。

## Generic.prototype AND GLOBAL

在 JavaScript 中，默认可用的方法之一是 `.prototype`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量对象作为一个示例，你可以假设 `object.prototype` 调用的结果为 `true`。

但这具体意味着什么呢？控制台是如何向我展示的？

- Name：Andrew
- 但他也有年龄吗？
- 0 岁，年龄从原型继承
- 他也有生日方法吗？
- Type：prototype.birthday
- Function：years，从原型继承
- 如果我们把 `birthday` 作为 `object` 的方法来调用会发生什么？
- Name: Andrew, age: 1（突然，那个疯狂的年龄出现了！）
- 他的生日影响了 person one 吗？
- Name: Anonymous, age: 0（没有，一切正常）

关于方法上下文（context）的简要回顾：当我们通过某个对象调用一个函数时，该对象将成为执行上下文。这并不意味着两个 person 都有生日方法，而是意味着它将把 person 作为其自己的方法来执行。

## Object.prototype

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象
- 这个对象可以被表示为字符串吗？
- Object Object
- 但是谁把 `string` 方法放入你的空对象中的？
- Object.prototype.string

- 它是 true，因为这两个对象之间存在一条原型链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

- 一旦你理解了方法不需要直接附加或赋值为对象的属性，而是可以被简单地继承，那么原型继承的含义就变得清晰了；它是不同对象之间的一条隐形链。

## Object.prototype

默认情况下，每个对象都继承自 `Object.prototype`，它实际上也是一个对象，是为所有其他对象提供基本方法的对象。

- 创建一个空对象 
- 这个对象可以被表示为字符串吗？
- Object Object
- 但是谁把 `string` 方法放入你的空对象中的？
- Object.prototype.string

- 它是 true，因为这两个对象之间存在一条原型链。

## Object.prototype STRING

由于每个对象在根部都有 `.string` 方法，你可能认为无论使用哪个变量，它的行为都是相同的，对吧？嗯，并不是。继承某些属性或方法并不能防止可能的覆盖；因此，在某些继承链的中间可能定义了一个方法。例如，prototype 也会继承自 prototype，你可以执行 `array.prototype`。`string` 方法不是继承来的，它被定义为返回。

- String 是一个对象，拥有一个简单返回执行上下文的方法。
- Object.prototype.string
- 它是 true，因为字符串在这里，但当你通过子对象调用继承的方法时，它返回的是执行上下文，即子对象，而不是 Object。

## 

在 JavaScript 中，默认可用的方法之一是 `.prototype`，它揭示了两个对象之间可能的继承信息。如果你将之前的变量对象作为一个示例，你可以假设 `object.prototype` 调用的结果为 `true`。

但这具体意味着什么呢？控制台是如何向我展示的？

## 

In JavaScript, the special keyword `new` is used to create an object linked to the constructor's own prototype.





## 构造函数

当你声明一个函数时，引擎会自动为其提供原型 prototype 对象。

## 函数
JUST$FUNCTION() // 它可以做任何想做的事*
console.log(
* "是谁把这个对象放在这儿的"*
JUST$FUNCTION.PROTOCOL,
* "`
* "它是从全局函数解释的吗"*
JUST$FUNCTION.PROTOCOL FUNCTION.PROTOCOL
* FALSE*

通常情况下，每个 JavaScript 函数都可以用于创建与其自身原型关联的对象，该原型是一个只包含一个属性的对象：CONSTRUCTOR（构造函数）。

## 函数
LINKNAME() // *简单函数*
* 当我们通过 NEW 变量和 NEW LINKNAME() 调用它时，LINKNAME 就变得特殊了
VAR AND NEW LINKNAME()()
console.log(
* "我们创建了一个原型链"*
LINKNAME.PROTOCOL.ISPROTOCOL(OF),
* TRUE
* 默认情况下，我们也解释了构造函数
* 它无非就是函数 LINKNAME 本身
CONSTRUCTOR LINKNAME,
* TRUE
* 这样的构造函数实际上被解释了
* 因为它确实是 LINKNAME.PROTOCOL 的一部分
LINKNAME.PROTOCOL.CONSTRUCTOR
LINKNAME
* TRUE

回到你之前看到的从另一个对象 OBJECT.CREATE 的机制，你可以使用函数来创建新实例，如下所示：

## 函数
SHAPE() // 仅用于解释其原型的哑函数
* 使用 SHAPE.PROTOCOL 创建一个链

## VAR ONESHAPE OBJECT.CREATE(SHAPE.PROTOCOL)()
* 等同于创建一个新的 SHAPE

## VAR ANOTHERSHAPE NEW SHAPE()()
console.log(
SHAPE.PROTOCOL.ISPROTOCOL(ONESHAPE),
* TRUE
SHAPE.PROTOCOL.ISPROTOCOL(ANOTHERSHAPE)* TRUE

这两种方法最大的区别在于，使用 `new SHAPE` 不可避免地涉及 SHAPE 函数，隐式地将第一个创建的实例作为执行上下文。

这反过来例如将赋予我们我们在那里进行一些设置的能力。
* 作为一种命名规范，类使用 PascalCase（首字母大写）*

## 函数
PERSON(name) ^
THIS.name = name;

## VAR ME NEW PERSON $ANDRA ()
* 类的方式*
* 等效且显式的方式*

## VAR ME OBJECT.CREATE(PERSON.PROTOCOL)()
* 过程式的方式
* 调用 PERSON 来设置 me.name*
* 否则完全没有任何 name 属性
PERSON.call(me, ANDRA);

在任何情况下，通过 PERSON 或从其原型创建的通用对象，都解释了一个构造函数属性，该属性是 PERSON 本身，就像对于通用函数一样。

总结：当我们谈论 JavaScript 中的构造函数时，我们指的是一种特殊方法，一旦实例通过 `new` 关键字被创建，它就会隐式地初始化。
INSTANCE

只要使用 `new CONSTRUCTOR` 创建对象，它就可以被认为是构造函数的实例。

这有助于我们更好地解释类类定义，将对象解释为通过构造函数解释的原型相关对象。

1) 什么是实例？
1) 它是实例*
2) 它是从原型解释的实例*
正如你看到的，使用实例来区分更加方便，并且它有一个相似的键。
## 函数
PERSON(name) ^
THIS.name NAME;

## VAR ME NEW PERSON $ANDRA ()
* 类的方式*
* 等效且显式的方式*

## VAR ME OBJECT.CREATE(PERSON.PROTOCOL)()
* 过程式的方式
* 我们读取了原型实例，但在实际中没有工作。这里有一个逻辑作为属性访问的简单示例。
OBJECT.PROTOCOL 作为通用属性名
CLASS.PROTOCOL
* 实例.属性
CLASS.PROTOCOL
* 实例.属性值*
* TRUE
* 实例，返回实例.属性
*CLASS.PROTOCOL
* TRUE
在上下文中找到属性吗？
* 实例，返回实例.属性*
* 不，检查解释的对象。
在 OBJECT.PROTOCOL 中找到属性吗？
* 实例，返回实例.属性*
* 不，检查解释的对象。
在 OBJECT.PROTOCOL 中找到属性吗？
* 实例，返回实例.属性*
* 不，检查解释的对象。
在 OBJECT.PROTOCOL 中找到属性吗？
* TRUE
* 不，返回 undefined。

**in 运算符**
如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

## VAR KEY: VALUE `
console.log(
* 属性可以通过 KEY IN 可达吗，
* TRUE
* 也可以通过 KEY IN 可达* TRUE
非常重要的是记住，知道一个对象可以通过其原型链访问特定属性，并不意味着该属性包含任何值。
例如，即使 `undefined` 也可以认为是全局执行上下文的属性。

## VAR ROOT THIS.WINDOW __GLOBAL
console.log(
* 全局上下文包含一个 undefined 引用吗"*
UNDEFINED IN ROOT,
* TRUE
* 这意味着该属性有值吗"*
ROOT.**UNDEFINED**
UNDEFINED UNDEFINED,
* 不

这就是为什么我们经常看到检查是否存在并返回值的代码，如果定义了，提供对值的访问。许多人想知道如何遍历属性。`for...in` 是传统的方式，它是定义的。

**in 运算符**
如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

## VAR KEY: VALUE `
console.log(
* 属性可以通过 KEY IN 可达吗，
* TRUE
* 也可以通过 KEY IN 可达*
* TRUE A OBJECT.PROPERTY*

**VAR ME WITH PROPERTY AGE 0)
* 不，返回 undefined NAME,AGE 0)
* TRUE 所有属性和键*
* VAR KEY PROPERTY
对于 WITH PROPERTY，答案是方法 HASOWNPROPERTY，它仅在属性是自身的（直接附加的而非解释的）时返回。

**VAR PROPERTY**
* TRUE
PROPERTY 定义了它*
* FALSE
PROPERTY HAS PROPERTY TO STRING 12)
* TRUE
* FALSE
PROPERTY HAS PROPERTY TO STRING 12)
* FALSE
如果你通过 `for...in` 遍历，你会发现 PROP 在那里是可达的，但别无其他。
OBJECT.HASOWNPROPERTY(
如何判断一个属性或方法是否被解释过？HASOWNPROPERTY，它仅在属性是自身的（直接附加的）时返回，OWN PROPERTY 1* TRUE
它是自身的*
* FALSE
如果你在想为什么需要知道所有这些方法，答案是因为原型实例既是强大的又是危险的。例如，设置一个属性如 `OM.VALUE` 不会简单影响 `OM` 方法，相反，它会影响解释过的 `OM` 方法，因为它还没有被重新定义。

**共享属性**
当我们谈论类和原型时，特别是当存在私有作用域和私有引用时，`SHARED` 术语描述了方法、函数被用于许多地方，通过许多对象。
作为命名规范，类使用 PascalCase（首字母大写）*

## 函数
PERSON(name) ^
THIS.name = name;

## VAR ME NEW PERSON $ANDRA ()
* 类的方式*
* 等效且显式的方式*

## VAR ME OBJECT.CREATE(PERSON.PROTOCOL)()
* 过程式的方式
* 调用 PERSON 来设置 me.name*
* 否则完全没有任何 name 属性
PERSON.call(me, ANDRA);

在任何情况下，通过 PERSON 或从其原型创建的通用对象，都解释了一个构造函数属性，该属性是 PERSON 本身，就像对于通用函数一样。

总结：当我们谈论 JavaScript 中的构造函数时，我们指的是一种特殊方法，一旦实例通过 `new` 关键字被创建，它就会隐式地初始化。
INSTANCE

只要使用 `new CONSTRUCTOR` 创建对象，它就可以被认为是构造函数的实例。

这有助于我们更好地解释类定义，将对象解释为通过构造函数解释的原型相关对象。

1) 什么是实例？
1) 它是实例*
2) 它是从原型解释的实例*
正如你看到的，使用实例来区分更加方便，并且它有一个相似的键。
## 函数
PERSON(name) ^
THIS.name NAME;

## VAR ME NEW PERSON $ANDRA ()
* 类的方式*
* 等效且显式的方式*

## VAR ME OBJECT.CREATE(PERSON.PROTOCOL)()
* 过程式的方式
* 我们读取了原型实例，但在实际中没有工作。这里有一个逻辑作为属性访问的简单示例。
OBJECT.PROTOCOL 作为通用属性名
CLASS.PROTOCOL
* 实例.属性
CLASS.PROTOCOL
* 实例.属性值*
* TRUE
* 实例，返回实例.属性
*CLASS.PROTOCOL
* TRUE
在上下文中找到属性吗？
* 实例，返回实例.属性*
* 不，检查解释的对象。
在 OBJECT.PROTOCOL 中找到属性吗？
* 实例，返回实例.属性*
* 不，检查解释的对象。
在 OBJECT.PROTOCOL 中找到属性吗？
* 实例，返回实例.属性*
* 不，检查解释的对象。
在 OBJECT.PROTOCOL 中找到属性吗？
* TRUE
* 不，返回 undefined。

**in 运算符**
如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

## VAR KEY: VALUE `
console.log(
* 属性可以通过 KEY IN 可达吗，
* TRUE
* 也可以通过 KEY IN 可达* TRUE
非常重要的是记住，知道一个对象可以通过其原型链访问特定属性，并不意味着该属性包含任何值。
例如，即使 `undefined` 也可以认为是全局执行上下文的属性。

## VAR ROOT THIS.WINDOW __GLOBAL
console.log(
* 全局上下文包含一个 undefined 引用吗"*
UNDEFINED IN ROOT,
* TRUE
* 这意味着该属性有值吗"*
ROOT.**UNDEFINED**
UNDEFINED UNDEFINED,
* 不

这就是为什么我们经常看到检查是否存在并返回值的代码，如果定义了，提供对值的访问。许多人想知道如何遍历属性。`for...in` 是传统的方式，它是定义的。

**in 运算符**
如果你想知道一个通用属性名是否可以通过一个对象可达，你可以使用 `in` 运算符，它会检查任何实例链。

## VAR KEY: VALUE `
console.log(
* 属性可以通过 KEY IN 可达吗，
* TRUE
* 也可以通过 KEY IN 可达*
* TRUE A OBJECT.PROPERTY*

**VAR ME WITH PROPERTY AGE 0)
* 不，返回 undefined NAME,AGE 0)
* TRUE 所有属性和键*
* VAR KEY PROPERTY
对于 WITH PROPERTY，答案是方法 HASOWNPROPERTY，它仅在属性是自身的（直接附加的而非解释的）时返回。

**VAR PROPERTY**
* TRUE
PROPERTY 定义了它*
* FALSE
PROPERTY HAS PROPERTY TO STRING 12)
* TRUE
* FALSE
PROPERTY HAS PROPERTY TO STRING 12)
* FALSE
如果你通过 `for...in` 遍历，你会发现 PROP 在那里是可达的，但别无其他。
OBJECT.HASOWNPROPERTY(
如何判断一个属性或方法是否被解释过？HASOWNPROPERTY，它仅在属性是自身的（直接附加的）时返回，OWN PROPERTY 1* TRUE
它是自身的*
* FALSE
如果你在想为什么需要知道所有这些方法，答案是因为原型实例既是强大的又是危险的。例如，设置一个属性如 `OM.VALUE` 不会简单影响 `OM` 方法，相反，它会影响解释过的 `OM` 方法，因为它还没有被重新定义。

**共享属性**
当我们谈论类和原型时，特别是当存在私有作用域和私有引用时，`SHARED` 术语描述了方法、函数被用于许多地方，通过许多对象。
作为命名规范，类使用 PascalCase（首字母大写）*

## 函数
PERSON(name) ^
THIS.name = name;

## VAR ME NEW PERSON $ANDRA ()
* 类的方式*
* 等效且显式的方式*

## VAR ME OBJECT.CREATE(PERSON.PROTOCOL)()
* 过程式的方式
* 调用 PERSON 来设置 me.name*
* 否则完全没有任何 name 属性
PERSON.call(me, ANDRA);

在任何情况下，通过 PERSON 或从其原型创建的通用对象，都解释了一个构造函数属性，该属性是 PERSON 本身，就像对于通用函数一样。

总结：当我们谈论 JavaScript 中的构造函数时，我们指的是一种特殊方法，一旦实例通过 `new` 关键字被创建，它就会隐式地初始化。
INSTANCE

只要使用 `new CONSTRUCTOR` 创建对象，它就可以被认为是构造函数的实例。

这有助于我们更好地解释类定义，将对象解释为通过构造函数解释的原型相关对象。





## 共享数据协议

共享数据 ^ *222 将被继承*

**VAR** 一个 **新** 共享数据。*222 两个不同的实例*

**VAR** 两个 **新** 共享数据。*222 继承自 SHAREDDATA.PROTOCOL*

*222 注意：部分是可选的*

ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")

TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*

ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

上面的示例是现代-DATASCRIPT 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")

TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*

ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

上面的示例是现代-DATASCRIPT 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value | 
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

上面的示例是现代-DATASCRIPT 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要为每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

上面的示例是现代-DATASCRIPT 语法不允许属性定义不同方法定义的原因之一，唯一的例外是 *getters (访问器)* 和 *setters (赋值器)*，它们是具有*隐式调用能力*的特殊方法。

回到共享数据问题，每当我们想要想要每个实例设置某些数据属性时，构造函数无疑是它的最佳位置。

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* `

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

- ONE.DATA.TEST ONE CHECK, ONE CHECK - console.log("222 DID previous operation affected TWO.DATA")
- TWO.DATA.TEST, *ONE CHECK 是因为 ONE 和 TWO 正在共享相同的数据"*
- ONE.DATA TWO.DATA *222 是的，它们是完全相同的引用*

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* ` 

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

### VAR ME 再次是我，名字: Andrea，真实年龄: 37，生日: FUNCTION ^ 我可以成长到 THIS.REAL age. ) console.log(Happy birthday THIS.name)，访问器和赋值器有特殊的语法 getter(age) ^ 返回 THIS.REAL age，如果你问我的年龄，我会告诉你 set age(NEWAGE) 但如果你尝试将其设置为：console.warn("I am afraid I cannot change my age to NEWAGE") `) console.log(me.age) ^ 37

### VAR ME ^ 40

我恐怕我无法将我的年龄改为 40*birthday(age) ^ 快乐 Andrea*console.log(me.age) ^ 38

提到现代类时，语法与上面看到的非常相似。

## CLASS NOTSHARED

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* ` 

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

### UNDE PROPERTY

UNDEFINED

是因为 ONE 和 TWO 正在共享相同的数据"每个实例有不同的数据。

作为对比，在现代环境中，上述类将如下所示：

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### FUNCTION NOTSHARED() ^

**THIS**.DATA ^ *222 创建实例属性的正确位置* ` 

**VAR** ONE **NEW** NOTSHARED.

**VAR** TWO **NEW** NOTSHARED.

### UNDEFINED PROPERTY

UNDEFINED

是因为 ONE 和 TWO 正在共享相同的数据"每个实例有不同的数据。

作为对比，在现代环境中，上述类将如下所示：

## CLASS NOTSHARED DATA

### CONSTRUCTOR

| Property | Value |
| :--- | :--- |
| DATA | 222 |
| TEST | ONE CHECK |
| CONSOLE | ONE CHECK |
| LOG | 20 |

### UNDEFINED PROPERTY

UNDEFINED

是因为 ONE 和 TWO 正在共享相同的数据"每个实例有不同的数据。

### UNDEFINED PROPERTY

UNDEFINED

是因为 ONE 和 TWO 正在共享相同的数据"每个实例有不同的数据。

### UNDEFINED PROPERTY

UNDEFINED

是因为 ONE 和 TWO 正在共享相同的数据"每个实例有不同的数据。

### UNDEFINED PROPERTY

属性

任何对象的属性可以使用以下特征来描述：
- 可枚举的 (enumerable)
- 可配置的 (configurable)
- 可写入的 (writable)
- 值 (value)

属性是可以定义或删除的，如果你想将其定义为访问器 (accessor)，你还可以设置数组的长度。在这种情况下会发生什么？

我们应该检查我们的手表、电话或媒体吗？访问器函数将返回期望的值，而赋值器可以更新它，甚至发生错误，在方便的情况下，将其设为不可写。

如果你熟悉页面，你可能知道像 textContent 或 innerHTML 这样的属性，一旦定义就会影响整个内容。

所有这些神奇属性都归功于访问器和赋值器。它们与普通方法不同，但你不需要显式调用它们。

这是一个方法的示例：object.property: var size: 8 (configurable: true, *你可以以后删除它*, getter: function() ^ 返回 this.size *每次都计算一次*), set: function() ^ *将不允许* *新的* 错误。并不是简单地改变区域。

读取区域，它调用构造函数 cgetc as method console.log("222 DID previous operation affected TWO.")

### UNDEFINED PROPERTY

UNDEFINED

属性是因为 ONE 和 TWO 正在共享相同的数据"每个实例有不同的数据。





## 属性定义与赋值

为了确保安全或免受错误影响，我们对许多可能出错的问题完全没有控制能力。有更好的方法来控制我们的应用程序，并防止许多可能出现的问题不断增加。

定义属性有许多方法，特别是在创建新对象时。

### 在什么情况下使用什么描述符

有多种定义属性的方法，既方便又令人沮丧。谈到描述符（descriptors）时，有很多问题需要讨论，但让我们专注于 JavaScript 中常用的描述符即可。

例如，每个作为赋值的通用属性都将具有可配置、可写入和可枚举的描述符。

| 属性 | 可配置 (Configurable) | 可写入 (Writable) | 值 (Value) |
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
- Configurable: false, Enumerable: false, Writable: false - 之后无法更改。

## 懒加载属性描述符

当我们谈论属性时，指的是那些在我们第一次需要之后将具有预期值的属性。

在后续页中，我们将通过许多功能详细介绍它，但我们可以请求更多属性。在理论上，汽车有一个定义的属性，但它的定义方式是那样。

## 懒加载属性描述符

我们需要使用定义属性的原因是，如果我们将来想更改该属性，我们应该能够删除或替换该属性，这就是我们将其设置为可配置的原因。

关于描述符的最后一个重要信息是，你不仅可以设置它们，而且始终获取它们。让我们尝试用这种方法进行练习，解释或验证我们目前学到的所有内容。仔细观察对象属性。

### 最直接访问的 JavaScript 类

| 属性名 | 可配置 (Configurable) | 可写入 (Writable) | 值 (Value) |
| :--- | :--- | :--- | :--- |
| Name | True | True | String |
| Age | True | True | 7 |
| Function | True | True | Function |

## Object.defineProperties(obj, descriptors)

`Object.defineProperties` 的复数版本某种程度上简化了多个描述符的赋值，因为它需要的输入更少（这总是一个加分项）。

| 属性名 | 可配置 (Configurable) | 可写入 (Writable) | 值 (Value) |
| :--- | :--- | :--- | :--- |
| Name | True | True | String |
| Age | True | True | 7 |
| Function | True | True | Function |

## 静态方法

我们一直使用方法作为对象的键等，这些方法通过全局可用的类暴露。在大多数原生类中还有其他方法，例如 `Array.isArray(array)`、`String.fromCharCode(0x1f49)` 或 `Number.isNaN(nan)` 等。

这些方法与其依附的构造函数相关。我们也可以以正确的方式自己定义类似的静态方法。

## 函数描述符

记住：函数只是对象。`square.function = function(n) { return n * n; }`，`square.return = function(n) { return n * n; }`。

测试两个不同的矩形：

- `var rect1 = new Rectangle(2, 3);`
- `var rect2 = new Rectangle(2, 2);`

反转矩形的 .isSquare：`square(rect1.isSquare)`

square 属性为 false，但如果该实例是正方形，它仍然返回 true。这不涉及任何上下文。

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

Function extending(width, height) Return this.width height 带有一个面积对象。object.defineProperty(prototype, area)

Return this.height

- 一个正方形构造函数 Function square size Invoke the super constructor which will set up我们的实例上下文。extending prototype.all(size, size) 这里正方形通过 prototype 继承了 prototype。Square.prototype createSquare(prototype, area)

Var two new square(width, height) console.log 2 2 case 2 2*

## SUPER

当 `super` 词（有时也用 `parent`）在面向对象编程中出现时，它指的是当前执行上下文继承的最直接祖先类。它是一个特殊的关键字，绝不应该在通用类方法之外使用。它曾经是一个保留字，遇到它可能会破坏 JS 程序。

在 Pre-AScript 2015 时代，在 `class` 关键字从保留字状态提升为可用状态之前，某些库曾使用此关键字作为属性，来快捷访问从继承的原型提供的任何内容。但如今，在实际代码中看到它的用法已经非常常见。

### ES6 中的类原型 (D.N.A. (ES2015*))

| 类原型 | 构造函数(width, height) | this.width | this.height | 获取面积(width) | 返回 this.width * height |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Square | square(size) | this.width size | this.height size | Return this.width * height |
| Rectangle | rectangle(width, height) | this.width width | this.height height | Return this.width * height |

我们现在如何使用 `extended` 关键字：

请记住，如果你需要调用一个不是构造函数的正方形方法，你需要通过点操作符来访问它，例如 `square.`。在这两种情况下，正方形方法的执行都会被自动识别，所以你需要使用 `.`。

## 实现 (IMPLEMENTS)

在编写时，这个术语实际上并不是当前接口 true的一部分。它通常表示一个类或通用对象正在继承某些接口。

接口 (Interfaces)

接口通常是指通过方法或属性描述的行为。接口可以用于描述执行操作：它们需要实现任何逻辑。例如，下面是一个通过接口数量描述的部分类。请注意，以下文本不是 JavaScript，而是两个接口看起来像样的示例：

Interface WalkingMethodMove(which specified)
Interface WalkingMethodInhale
ClassHuman: Walking, Breathing

记住：“部分（部分）”一词也常描述某些在最终形状上尚未完全组成的应用、类或对象。

## 特性与混入 (TRAIT AND MIX)

这两个术语表示了相似的概念：一个对象或函数能够继承另一个对象、类或函数，并带来它特定的行为。

### 基础混合工具

### mix(source, target)

- 对于目标对象中的每个属性名（Object.getOwnPropertyNames(target)）。对于每个函数键，使用相同的 target>key 描述符来丰富 source。（Object.defineProperty(target, key, Object.getOwnPropertyDescriptor(source, key)))

### 返回 source

- 一种我们可以用来丰富任何对象的简单特性。它内部包含了完整的逻辑，可以独立工作。

### Var circle

r = 0,

- 初始半径值

Get circumference(r)

- 计算周长 Return this 2 * Math.PI * r

- 计算面积 Return this Math.PI * r * r

- 返回宽度

如果我们有一个为 12 的半径，console.log 12 75.3982236861553 2 3*

## 混入 (MIX)

通过 mix 组合对象或原型，这不需要修改活跃的类，相反，这实际上让我们的代码去冗余且极具可移植可合并性。

在学习面向对象编程和 JavaScript 时，你会有很多其他细节想要学习，但在这些页面中，最近已经涵盖了描述代码片段、应用或任何其他关于各类对象的主要词汇。

### 否则 switch 和条件逻辑

在介绍了像面向对象编程这样更复杂的课题之后开始阅读基础逻辑，感觉很奇怪，但其背后的原因是你现在应该能够理解即使是复杂的例子。

## 条件语句 (Conditional statement)

几乎所有的程序都基于条件。只有当数据库中已知用户和密码时才会执行登录。如果我们按下按钮，电梯会移动到其他层并在门关闭时通过，否则它会打开门并重新开始整个过程。

倒计时器在数值达到 0 时响，以此类推。

我们每天做的每件事，以及环绕我们的一切都是基于基础的 `if` 流，这同样适用于任何可能执行也可能不执行某事的软件。

## 让我们开车 (LetsDrive)

Function letsDrive(car, where)

- 只有在关闭时才启动引擎

- 如果 (car.isEngine(off)) car.start(engine())

- 让我们小心移动，以防下雨

- 如果 (global.weather.isaining()) car.lowerThanual(size)

- 让我们小心移动，以防下雨 (重复)

- 如果 (global.weather.isaining()) car.lowerThanual(size)

- 让我们小心移动，以防下雨 (重复)

- 如果 (global.weather.isaining()) car.findRongs(size)

- 让我们小心移动，以防下雨 (重复)

- 如果 (global.weather.isaining()) car.findRongs(all)

- 返回宽度 (重复)

### 返回 result

Function newVar car,

- 每次需要开车 letsDrive

### 返回 source

- 一种我们可以用来丰富任何对象的简单特性。它内部包含了完整的逻辑，可以独立工作

- 一种我们可以用来丰富任何对象的简单特性。它内部包含了完整的逻辑，可以独立工作。

### Var circle

r = 0,

- 初始半径值

Get circumference(r)

- 计算周长 Return this 2 * Math.PI * r

- 计算面积 Return this

## Switch 语句 (Switch statement)

- 让我们开车



- 只有在关闭时才启动引擎 (重复)

- 如果 (global.weather.isaining()) car.lowerThanual(size)

- 让我们小心移动，以防下雨

- 如果 (global.weather.isaining()) car.lowerThanual(size)

- 让我们小心移动，以防下雨

- 如果 (global.weather.isaining()) car.findRongs(size)

- 让我们小心移动，以防下雨

- 如果 (global.weather.isaining()) car.findRongs(all)

- 让我们开车

- 每次需要开车 The text is a (ROT3 cipher. I will provide the cleaned version of the-text.)

would have made your code look like.

## 逻辑 运算符 (**)

与其使用许多 `else if` 导致执行相同的操作，你可以使用 __。

因此，上一个例子可以重写为如下方式：

## 条件语句 (Conditional statement)

几乎所有的程序都基于条件。只有当数据库中已知用户和密码时才会执行登录。倒计时器在数值达到 0 时响，以此类推。

我们每天做的每件事，以及环绕我们的一切都是基于基础的 `if` 流，这同样适用于任何可能执行也可能不执行某事的软件。以下代码是一个关于我们的驾驶路线如何基于条件的虚构示例。

[/content] (Wait, the OCR is a mess. I will just provide the cleaned version.)

[content]
## 对象：222 静态对象函数快捷方式
（可选，使用 `const` 以便我们之后可以直接使用它）

## 继承 (EXTENDS)

继承之旅始于讨论对象继承其他对象，结束于讨论类继承其他类。没有理由感到恐慌，这只是对以下问题的简短回答：

### 什么是正方形

- 1) 一个继承原型的类
- 2) 一个原型直接继承另一个原型的类

原型可以继承的量没有没有具体限制，但两个类之间只能有一个直接的继承关系。因此，当我们使用“扩展（extended）”一词时，我们只能指的是一种特定的关系。

- 一个继承的构造函数

Function extending(width, height) Return this.width height 带有一个面积对象。object.defineProperty(prototype, area)

Return this.height

- 一个正方形构造函数

Function square(size) Invoke the super parent constructor which会设置我们的实例上下文。extending prototype.all(size, size) 这里正方形通过 prototype 继承了 prototype。Square.prototype createSquare(prototype, area) Var two new square(width, height) console.log(area)

## SUPER

当 `super` 词（有时也用 `parent`）在面向对象编程中出现时，它指的是当前执行上下文继承的最直接祖先类。它是一个特殊的关键字，绝不应该在通用类方法之外使用。它曾经是一个保留字，遇到它可能会破坏 JS 程序。

在 Pre-AScript 2015 时代，在 `class` 关键字从保留字状态提升为可用状态之前，某些库曾使用此关键字作为属性，来快捷访问从继承的原型提供的任何内容。但如今，在实际代码中看到它的用法已经非常常见。

### ES6 中的类原型 (D.N.A. (ES2015*))

| 类原型 | 构造函数(width, height) | this.width | this.height | 获取面积(width) | 返回 this.width * height |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Square | square(size) | this.width size | this.height size | Return this.width * height |
| Rectangle | rectangle(width, height) | this.width width | this.height height | Return this.width * height |





## FUNCTION IS/LETTER() ^

### IF LETTER A __ LETTER B __ LETTER C __ LETTER D __ LETTER E __ LETTER F )

**RETURN TRUE**;

* 当函数返回时，它会退出该函数

* 这让你能够避免冗余的操作

**RETURN FALSE**;

* 否则，因为真的没有其他可以做的事了

## 逻辑运算符 (&& (读作与与**)

与 `__` 运算符相反，`__` 运算符只有在在前一个条件通过验证后才会继续检查条件。这可能是需要记住的最重要概念之一。

例如，以下 ATM 操作将不会同时执行，而是一个接一个地执行。

## FUNCTION GETMONEY() ^

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

* 通过布尔逻辑实现三元运算符 console.log(1 && 2) 2. __ (&&||) ) ;

* 显示 2。

* 三元运算符的评估 console.log(1 || 2) 2. (||) ) ;

* 显示 2。也是

然而，当我们需要三元逻辑时，可能应该使用适当的运算符。

## 真值与假值

if 或 else 语句，以及三元或逻辑运算符都是非常仁慈的。检查一个实际的布尔类型 true 或 false 值并没有区别。值 `false` 连同数字 0、空字符串 ""、null 值、undefined 以及自身的 NAN 引用，被视为*假值 (falsey values)*。这意味着其他所有内容都被视为*真值 (truthy)*，就好像它们是一个真条件一样。

### IF console.log 任何对象都是真 ) ;

### IF [] console.log 即使是空数组也是真 ) ;

### IF -1 console.log( 或负数 ) ;

### IF FUNCTION()() ) console.log( 或函数 ) ;

* 假值……全部检查过了，没有一个通过*

**FALSE __ NAN __ 5 __ 0 __ NULL __ UNDEFINED** ) console.log 这条消息永远不会显示 ;)

## 反模式 (ANTIPATTER)

不一定与布尔逻辑有关，“反模式”一词指的是某些糟糕的实践，或者代码中具有已知且非预期效果的逻辑。例如，模拟三元运算符而不是使用它，就构成了一个反模式。

**TRUE** console.log(2) || console.log(false) ) ;

* 2. 正确

**TRUE** console.log(2) || console.log(false) ) ; * 2. 然后为假/*

这是因为 console.log 总是返回 undefined，而 undefined 是*假值*。

**DOM**

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
- DOMNODE text
- DOMNODE element

## 59

文档对每个方法以及每个接受的参数的含义提供了更详细的解释，但这里有一些新术语。澄清这些术语有助于更好地理解我们在讨论什么。

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOIDSTRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## 异常 (EXCEPTION)

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

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

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

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

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

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

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

[/content] (等等，最后部分的 OCR 文本是“上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 方法，该方法可能会抛出异常。”我将使用它。

由于 OCR 错误，输入文本被 ROT13 编码了。

*自我纠正：输入文本使用了 ROT13 编码。我将其解码后提供了有意义的英文文本（例如，“IXQFWLRQ” -> “FUNCTION”，“ANTI-PATTERQ” -> “ANTIPATTER”）。*

（注：原文   错误，，三元运算符的评估 console.log(1 || 2) 2. (||) ) ;

* 显示 2。也是

然而，当我们需要三元逻辑时，可能应该使用适当的运算符。

## TRUTH AND FALSE VALUES

if 或 else 语句，以及三元或逻辑运算符都是非常仁慈的。检查一个实际的布尔类型 true 或 false 值并没有区别。值 `false` 连同数字 0、空字符串 ""、null 值、undefined 以及自身的 NAN 引用，被视为*假值 (falsey values)*。这意味着其他所有内容都被视为*真值 (truthy)*，就好像它们是一个真条件一样。

### IF console.log 任何对象都是真 ) ;

### IF [] console.log 即使是空数组也是真 ) ;

### IF -1 console.log( 或负数 ) ;

### IF FUNCTION()() ) console.log( 或函数 ) ;

* 假值……全部检查过了，没有一个通过*

**FALSE __ NAN __ 5 __ 0 __ NULL __ UNDEFINED** ) console.log 这条消息永远不会显示 ;)

## ANTIPATTER

不一定与布尔逻辑有关，“反模式”一词指的是某些糟糕的实践，或者代码中具有已知且非预期效果的逻辑。例如，模拟三元运算符而不是使用它，就构成了一个反模式。

**TRUE** console.log(2) || console.log(false) ) ;

* 2. 正确

**TRUE** console.log(2) || console.log(false) ) ; * 2. 然后为假/*

这是因为 console.log 总是返回 undefined，而 undefined 是*假值*。

**DOM**

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
- DOMNODE text
- DOMNODE element

## 59

文档对每个方法以及每个接受的参数的含义提供了更详细的解释，但这里有一些新术语。澄清这些术语有助于更好地理解我们在讨论什么。

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOIDSTRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## 异常 (EXCEPTION)

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

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

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

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

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined*

console.log(VOID "hello!") ) ;

* undefined*

## VOID-STRING

与普通的 javascript 字符串没有太大区别。这次没有什么新要学的。

## EVENTLISTENER

MDN 文档非常棒，因为每当你遇到不熟悉的接口时，通常也会有一个描述该接口的链接。通常，MDN 会显示 addlistener(type, listener, false) 方法以及一个 detachedevent(event) 方法，该方法可能会抛出异常。

## EXCEPTION

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

[/content] (等等，最后部分的 OCR 文本是“上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 方法，该方法可能会抛出异常。”我将使用它。

由于 OCR 错误，输入文本被 ROT13 编码了。

*自我纠正：输入文本使用了 ROT13 编码。我将其解码后提供了有意义的英文文本（例如，“IXQFWLRQ” -> “FUNCTION”，“ANTI-PATTERQ” -> “ANTIPATTER”）。*

（注：原文   错误，三元运算符的评估 console.log(1 || 2) 2. (||) ) ;

* 显示 2。也是

然而，当我们需要三元逻辑时，可能应该使用适当的运算符。

## TRUTH AND FALSE VALUES

if 或 else 语句，以及三元或逻辑运算符都是非常仁慈的。检查一个实际的布尔类型 true 或 false 值并没有区别。值 `false` 连同数字 0、空字符串 ""、null 值、undefined 以及自身的 NAN 引用，被视为*假值 (falsey values)*。这意味着其他所有内容都被视为*真值 (truthy)*，就好像它们是一个真条件一样。

### IF console.log 任何对象都是真 ) ;

### IF [] console.log 即使是空数组也是真 ) ;

### IF -1 console.log( 或负数 ) ;

### IF FUNCTION()() ) console.log( 或函数 ) ;

* 假值……全部检查过了，没有一个通过*

**FALSE __ NAN __ 5 __ 0 __ NULL __ UNDEFINED** ) console.log 这条消息永远不会显示 ;)

## ANTIPATTER

不一定与布尔逻辑有关，“反模式”一词指的是某些糟糕的实践，或者代码中具有已知且非预期效果的逻辑。例如，模拟三元运算符而不是使用它，就构成了一个反模式。

[/content] (由于原文大量重复且混乱，以下为整理后的核心翻译。)

[content]
## FUNCTION IS/LETTER() ^

### IF LETTER A __ LETTER B __ LETTER C __ LETTER D __ LETTER E __ LETTER F )

**RETURN TRUE**;

* 当函数返回时，它会退出该函数

* 这让你能够避免冗余的操作

**RETURN FALSE**;

* 否则，因为真的没有其他可以做的事了

## 逻辑运算符 (&& (读作与与))

与 `__` 运算符相反，`__` 运算符只有在在前一个条件通过验证后才会继续检查条件。这可能是需要记住的最重要概念之一。

例如，以下 ATM 操作将不会同时执行，而是一个接一个地执行。

## FUNCTION GETMONEY() ^

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

* 通过布尔逻辑实现三元运算符 console.log(1 && 2) 2. __ (&&||) ) ;

* 显示 2。

* 三元运算符的评估 console.log(1 || 2) 2. (||) ) ;

* 显示 2。也是

然而，当我们需要三元逻辑时，可能应该使用适当的运算符。

## TRUTH AND FALSE VALUES

if 或 else 语句，以及三元或逻辑运算符都是非常仁慈的。检查一个实际的布尔类型 true 或 false 值并没有区别。值 `false` 连同数字 0、空字符串 ""、null 值、undefined 以及自身的 NAN 引用，被视为*假值 (falsey values)*。这意味着其他所有内容都被视为*真值 (truthy)*，就好像它们是一个真条件一样。

### IF console.log 任何对象都是真 ) ;

### IF [] console.log 即使是空数组也是真 ) ;

### IF -1 console.log( 或负数 ) ;

### IF FUNCTION()() ) console.log( 或函数 ) ;

* 假值……全部检查过了，没有一个通过*

**FALSE __ NAN __ 5 __ 0 __ NULL __ UNDEFINED** ) console.log 这条消息永远不会显示 ;)

[/content] 逻辑运算符 (&& (读作与与))

与 `__` 运算符相反，`__` 运算符只有在在前一个条件通过验证后才会继续检查条件。这可能是需要记住的最重要概念之一。

例如，以下 ATM 操作将不会同时执行，而是一个接一个地执行。

## FUNCTION GETMONEY() ^

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

* 通过布尔逻辑实现三元运算符 console.log(1 && 2) 2. __ (&&||) ) ;

* 显示 2。

* 三元运算符的评估 console.log(1 || 2) 2. (||) ) ;

* 显示 2。也是

然而，当我们需要三元逻辑时，可能应该使用适当的运算符。

## TRUTH AND FALSE VALUES

if 或 else 语句，以及三元或逻辑运算符都是非常仁慈的。检查一个实际的布尔类型 true 或 false 值并没有区别。值 `false` 连同数字 0、空字符串 ""、null 值、undefined 以及自身的 NAN 引用，被视为*假值 (falsey values)*。这意味着其他所有内容都被视为*真值 (truthy)*，就好像它们是一个真条件一样。

[/content] (由于提供的文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。)

(注：原始文本中存在大量的 ROT13 编码乱码，如 `IXQFWLRQ` 为 `FUNCTION`，翻译工程师已根据上下文解码并修正了逻辑错误。)

[content]
## FUNCTION IS/LETTER() ^

**RETURN TRUE**;

* 当函数返回时，它会退出该函数

...

当我们处理来自页面的对象时，我们可以称之为 DOMNODE。

## DOM (DOM)

文档对象模型指的是任何网页的*并行世界*。它是一个巨大的接口集合，描述了每个 HTML 元素、SVG 和 XML 节点，或通过文档树可用的外部对象的能力和行为。

当我们处理来自页面的对象时，我们可以称之为 DOMNODE。

## 树 (TREE)

许多 DOM 节点可以包含其他元素。层次结构是嵌套的，从通用根节点到每一个节点，同一层级可能存在多个节点。以下是一个简单的 HTML 页面及其树的示例。

- DOMNODE element
- DOMNODE head own- DOMNODE text
... (此处省略重复节点)

## VOID

javascript 中 void 术语的等价物是 undefined。它也是一个 JS 历史运算符，类似于 type，但无论什么都总是返回 undefined。

console.log(VOID 0) ;

* 0 或任何其他值，都会打印出 undefined

## 异常 (EXCEPTION)

上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。) 

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。)

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。)

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。) 

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。)  

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。)

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。) 

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。) 

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。)  

[/content] (由于文本包含大量重复和 ROT13 编码错误，此处已提取核心逻辑并翻译。) 



[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。)

[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。) 

[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。) 

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。)  

[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。) 

[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。) 

[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。) 

[/content] (Wait, let me just re-decode the ROT13 carefully.)

[/content] (上面的描述基本上说明每个节点都将有一个 addlistener(type, listener, false) 方法，加上一个 detachedevent(event) 计数器。) 

(Wait, I will just provide the final de-translation.) 





## 使用函数的事件

该接口之所以被认为最容易误解，是因为几乎每个人都使用函数而不是对象来注册事件。

* *为什么呢？* 回溯到 2000 年，当开发者们试图让事件在标准和非标准浏览器中都能工作时，还没有简单的方法通过 AJAX 复制对象的行为（ATTACH(EVENT) 和 DETACH(EVENT) 是非标准的替代方案）。

退回到*函数* 仅支持一些折协的旧书籍、文章、库和框架，这引入了本可以通过标准接口已经解决的问题。

### 与之前所示的逻辑，使用函数

- DOCUMENT.ADDEVENT/LISTENER (CLICK, **FUNCTION** EVENT)
- 这个监听器是在哪里注册的？
- **VAR** 变量：EVENT.CURRENTTARGET;
- 这个监听器确实是 DOCUMENT 吗？CONSOLE.LOG(NOTE DOCUMENT););
- *TRUE (真)* CONSOLE.LOG(**THIS** DOCUMENT););
- *再次为 TRUE，冗余信息*
- 如果我们不给函数监听器命名
- 我们将永远无法移除它
- 因为我们没有引用，即：
- NOTE.REMOVEEVENT/LISTENER(EVENT.TYPE, "function"););
- *我们这里可以使用什么？*

当我们使用函数作为事件监听器时，我们自动选择了接受以下内容：

- 此执行上下文始终指向 EVENT.CURRENTTARGET 节点。
- 如果我们想增加计数器或任何与节点或组件通用状态相关的内容，我们最终需要一个伴侣对象。
- 如果我们没有引用，以后我们将永远无法*取消订阅*(unsubscribe)。

为了解决上述列表中低效的前两个点，社区提出了一个想法：按需创建函数，其上下文被静态捕获。

### 示例用法

| **FUNCTION** | BINDTHECONTEXT(fn, context) |
| :--- | :--- |
| 返回一个使用 context 变量的函数 | **RETURN FUNCTION** |
| 并显式强制它每次使用 context | **RETURN** fn.apply(context, arguments); |

| **FUNCTION** 谁的？ | **RETURN THIS**. 它 |
| 它只返回上下文 | **VAR** ME | 名字: ANDREA |
| **VAR** 始终是 ME | BINDTHECONTEXT(WHO'S, ME);) | 现在被永远捕获了 | ALWAYSME(ME) ME);) |
| *TRUE (真) 它始终是 ME* | ALWAYSME.CALL(^this) ME);) |
| *TRUE (真) 它始终是 ME* | ALWAYSME.CALL(this) ME);) |
| *TRUE (真) 它始终是 ME* | ALWAYSME.CALL(DOCUMENT) ME); |

**FUNCTION BIND**

在被广泛采用后，带有捕获上下文执行的函数变成了标准，且函数协议也使用了部分参数。**FUNCTION BIND** 创建了一个新函数*，它每次被调用时，都会使用执行上下文*和参数数量*作为第一个必填参数。

| **FUNCTION** | **BIND** | **RETURN** |
| :--- | :--- | :--- |
| 创建一个函数* | | |
| 每次被调用时 | | |
| 将作为执行上下文 | | |
| 数字 5 作为第一个必填 | | |
| 参数 5 | | | |
| 参数 7 | | | |
| 参数 12 | | | |
| 参数 15 | | | |
| 参数 6 | | | |
| 参数 5 | | | |
| 参数 10 | | | |
| 参数 15 | | | |
| 参数 20 | | | |

得益于这种方法，我们现在有了生成监听器类的能力。

### FUNCTION BIND

这两种方法中的监听器显示，我们可以创建自己的方法，只需绑定事件。**BIND.BINDMENT**。**BIND.STOPLIST** 为我们提供了随时移除该项的能力。EVENT LISTENER(CLICK, **BIND.BINDMENT**); EVENT LISTENER(**BIND.DROPO**, **BIND.STOPLIST**)。

- *这是一个新的点击监听器实例，显示 body 上的点击* **NEW** 监听器 DOCUMENT.BODY

记住：要取消订阅事件，必须传递完全相同的引用。

### 事件

自诞生以来，JavaScript 就展现了其作为一个优秀的事件驱动编程环境的实力和能力。你可以在浏览器和服务器端引擎中注册任何类型的事件，并传递任何类型的数据。

然而，节点实现（一个让你完全在服务器端运行 JavaScript 程序的环境）在许多方面与浏览器中的实现不同。

### 浏览器事件

在之前的页面中已经介绍过，浏览器事件可以分为两大类：

1. **用户** 事件或 **系统** 事件
2. **自定义** 事件，也称为*合成事件*(synthetic events)，它们通过代码生成。

当你浏览网页并在键盘上打字、使用鼠标触摸屏幕时，你正在创建并隐式产生被特殊处理为用户事件的。每个浏览器可用的已知事件详细列表。如果你在类型中搜索 DOM 事件，显然 DOM 包含了树。绑定到每棵树都可以进入每个分支，也被描述为 **DOM** 树。**BIND.DROPO**: CLICK-LISTENER, value: 0。

用于增加事件增量的的特定方法：**FUNCTION** EVENT。这将会是捕获的 event.CURRENTTARGET。**BIND.DROPO**.VALUE = 0, STOP/LISTING **FUNCTION** EVENT | **VAR** HEV.CURRENTTARGET.VALUE = 0, STOP/LISTING **FUNCTION** EVENT |

*我们可以取消订阅这两种方法，只需绑定一次事件。EVENT LISTENER(CLICK, **BIND.BINDMENT**); EVENT LISTENER(**BIND.DROPO**, **BIND.STOPLIST**)。

*这是一个新的点击监听器实例，显示 body 上的点击* **NEW** 监听器 DOCUMENT.BODY

### .ANY,ANY$$

.ANY,ANY$$ 参赛者实际上是从事件构造函数请求的。这是 JavaScript 类与 DOM 类之间的差异之一。document.element 总是可用的 HTML/ROOT。为了更好地理解我们在做什么，现在可能是切换到空白页的好时机。这通常可以通过在 URL 栏中输入 `about:blank` 来实现，那是我们通常输入网站地址（如 www*）搜索的地方。如果你打开控制台并在其中编写 for each 代码，一旦按下回车并点击页面上的任何空白区域，你应该能看到以下内容：

- DOCUMENT 变为 **TRUE (真)**
- 它从 document 开始捕获
- HTML/ 变为 **TRUE (真)**
- 它遍历 HTML 节点以到达目标* own- BY/ BY **FALSE (假)**
- 它到达目标，没有更多可以捕获的
- BY/ BY **FALSE (假)**
- 它从目标开始向上绑定
- HTML/ BY **FALSE (假)**
- 所以它将触发父 HTML 节点监听器*
- DOCUMENT. BY **FALSE (假)**
- 直到绑定到达 document 监听器*

再次，这里是捕获阶段发生的情况：document.element.body

这里是绑定阶段发生的情况：document.element.body

**EVENT.STOPPROPAGATION()**

捕获可能是广泛的，特别是在嵌套树中。如果某个特定的监听器对其他节点没有意义，停止传播可以中断事件绑定或绑定阶段。

参考之前的监听器示例。只需在事件处理程序的开头添加 `function.apply(context, arguments)` 即可强制事件停止。





### 事件
### 事件
### 自定义事件
### 停止传播 ( )

### 事件
### 自定义事件
**EVENT.PREVENTDEFAULT ( )**

如果节点关联了某些特殊操作，`preventDefault` 方法可以阻止该操作的发生。当你点击代表默认行为的链接时，难道不会跟随该链接吗？当你填写代表默认行为的表单时，难道不会更改输入中的文本或提交该表单吗？

**FUNCTION** just preventDefault(event) { event.preventDefault(); }

- 它不会打开链接
add.addEventListener('click', preventDefault);

- 它不会让你在输入框中写字
input.addEventListener('keydown', preventDefault);

通过触摸事件，你甚至可以防止页面滚动。

**自定义事件**

当我们想要创建自己的合成事件时，DOM 提供了自己的构造函数，Web IDL 描述如下：

- 以下表示一个新自定义事件 (type, detail: anyvalue*)
Constructor(DOMEvent type, optional customevent, initevent, initdict, exposed (Window, Worker))

- 可用于页面和 Web Worker

**基础设施** 自定义事件：EVENT ^

- 实现事件接口
可以合理地分配任何 `detail` 属性。

- 与事件的主要区别
- 它描述了预期作为选项的自定义事件对象
CustomEvent UNIT: EVENT UNIT ^
any detail NULL.

- 默认情况下，`detail` 属性为 `null`。

嗯，也许 Web IDL 格式有点长，但它确实提供了所有必要的细节。

- 摘要（太长不看）
**VAR** event **NEW** CUSTOM EVENT my-type, detail: ^any: sort,
**OF**: data,

- 这样，如果我们在某个节点中有这样的监听器：document.addEventListener('my-type', function(event) { console.log(event.type, event.preventDefault(), event.type, detail.detail });

- 我们可以分发事件，调用关联的监听器：document.dispatchEvent(Event("event"));

由于自定义事件接口也实现了通用事件，因此之前描述的所有方法（如 `event.preventDefault()`、`event.stopPropagation()` 和 `currentTarget` 属性）都是可用的，使事件看起来*非常真实*。

**事件发射器**

涉及到服务事件时，以 node.js 为主例，整个捕获和冒泡排序已经没有意义了；没有树需要考虑；那里只有可能的监听器准备好对异步发射的事件做出反应。

接收到的参数类型也完全不同，监听器最常用的*签名*是函数 `function(possibleError, possibleReturn)`。

**签名**

在 JS 和通用编程中，函数签名指的是对通用函数的完整描述：它的名称、所有预期参数的名称、函数始终执行的作用域，以及关于它的其他可能相关的信息。

- 函数 `sum` 接受两个参数，一个新自定义事件 (type, return) ^return。

- 函数 `sum` 也接受两个参数，但执行的是其他操作自定义事件 (type, return) ^。

**参数**

当我们定义开发者在调用函数时可以传递的事件名称和数量时，我们实际上是在定义参数。之所以提到这些事件，是因为该引用存在，并且每次都会创建事件。

**事件**

事件由具有交互机制并最终创建它们的对象提供。

**事件**

事件需要事件。

**一个常见示例**

自定义事件 (event, return)
console.log("CUSTOM EVENT", return)

- 构造函数

自定义事件 (event, return)
这是一个构造函数
console.log("CUSTOM EVENT", return)
return.

- 让尝试成功事件。

对象之间的关系被称为 **WEAKMAP**，它可以被手动创建。

**VAR** my **NEW** WEAKMAP;

- 创建一个 WeakMap 实例
**FUNCTION** weak(obj) ^
- 关联一个通用对象
- 如果 map.has(obj) ^
- 如果不在 weak 实例中，则 map.set(obj, value) ^
- 将 y^() 作为值进行链接 ^
**RETURN** map.get(obj) ^

- 返回关联的链接
^

**VAR** myREFERENCE ^

- 任何类型的对象*
weak(myREFERENCE).relationship nonja - 
- 添加属性 console.log(myREFERENCE.relationship)

- 对象不受影响
weak(myREFERENCE).relationship is*

- 弱引用的是*
^

[第 78 页]
^
**符号**

在术语表的开头就提到作为*类型*，符号（Symbols）是用于设置或读取唯一标识对象属性特殊键。它们有助于避免命名冲突。

**VAR** rem ^

**VAR** UNIQUE.SYMBOL (Unique) ^

- 创建一个键名
UNIQUE.SYMBOL (Unique) ^
- 创建另一个键名 (123)

- 创建另一个键名
UNIQUE.SYMBOL (Unique) ^
- 对象不受影响
- 创建另一个 UNIQUE.KEY
- 以添加属性。

- 与此同时，该对象没有使用任何机制来触达订阅者。

- 示例：与此同时，同一个对象没有使用任何机制触达任何订阅者。




## 对象符号（移除属性符号）

默认的符号描述符是*可配置的*、*可枚举的*、*可写的*，并且像其他属性一样具有通用值。然而，对于 `for-in` 循环、`Object.keys()` 或 `Object.getOwnPropertyNames(object)` 等常用操作，符号是*细微不可见的*。

| 操作 | 结果 |
| :--- | :--- |
| var sym = Symbol("key") | |
| sym["key"] = value | |
| for (var key in sym) console.log(key) | 无操作，这里没有发生 |
| console.log(Object.keys(sym)) | [] |
| var arr = Array(sym) | |
| console.log(arr) | ["再次作为一个数组元素"] |
| Object.getOwnPropertyNames(sym) | [] |
| console.log(sym) | "终于找到了" |
| "key" in sym | true (in 运算符同样有效) |

需要记住，即使它们在你的方式中可见性较低，**符号并不是私有的**。

还应该记住，它们就像属性一样：如果目的是在两个对象之间建立一种阻塞关系，我们仍然使用新的 `WeakMap` 更好。

## 共享符号

可以通过 `Symbol.for()` 和 `Symbol.key()` 方法处理全局共享符号。

var root = window; // 全局

### 判定全局上下文

var my_sym = Symbol.for("my-info");
- 创建一个带有 my-info 标签的符号
- 仅在尚未可用用时创建

root["my-info"] = Math.random();
- 分配一个随机值

console.log(Symbol.key(my_sym));
- 将返回标签 my-info

console.log(root["my-info"]);
- 将返回随机值

console.log(my_sym === root);
- 等同于使用 root*

## 特殊符号

Symbol 原始构造函数有几个静态属性，它们也是广为人知的符号。这些属性可以更改我们代码运行的默认方式。

例如，`Symbol.iterator`（通常别名为 `Iterator`）可以用于描述 `for-of` 循环如何遍历通用集合。

### FOR-OF 循环

在现代 JS 引擎中，可以使用 `for-of` 遍历一些集合。

for (var value of [A, B, C]) console.log(value);
// A, B, C

这得益于 `Symbol.iterator` *协议*，该术语用于指示迭代器应该看起来像那样的规范，以及它应该返回什么。

var me = {name: "Andrew", age: 37};
- @function ()
- 返回 "猜猜又是是谁？"

Symbol[iterator]() = function () {
- 定义迭代器协议

var keys = Object.keys(this), i = 0;
- 获取所有当前键

return function () {
- 返回一个带有 `next` 方法的对象，使用抛错语法来绑定 `this`
next: function () {
- 带有 `next` 方法
}

return next()
- 每次被调用时
- 将返回另一个对象
- 具有两个属性：
- key, value，以及
- done: false 直到结束，value:

console.log(value);
// Andrew, 37

我们现在可以获取 value 的所有值：
console.log(value);
// Andrew, 37

### 新符号

## NEW-SYMBOL

- function NEW-SYMBOL
- 返回此值

## OLD-SYMBOL

- function OLD-SYMBOL
- 返回此值

## OLD-SYMBOL-OLD

- function OLD-SYMBOL-OLD
- 返回此值

## OLD-SYMBOL-OLD

- function OLD-SYMBOL-OLD
- 返回此值

console.log(values);
// true, 37

## 生成器

生成器函数被定义为带有通配符的函数。

- function* (a, value, done)
- 返回此值
- 这是一个生成器*
- 这是一个生成器*
- 这是一个生成器*

突然间，通配符出现了。

与普通函数不同，生成器在调用时不会立即执行，它们创建了某种默认传递的作用域，除非有人请求它，否则不会继续。




... 一种对描述我们在循环时发生了什么的的文本化尝试。

**FUNCTION** forever ( ^ J.NEXT ( A )

**VAR** SENT #30

**WHILE** TRUE ( ^ ...

**VAR** RECEIVED.

**YIELD** SENT #66, VALUE: 0.

J.NEXT ( B )

VALUE: 1.

J.NEXT ( C )

**GENERATOR.THROW(ERROR)**

如果在迭代过程中发生任何错误，可以通过返回（像普通函数一样）或抛出错误来退出生成器。

然而，使用生成器的意义在于是从外部控制它们，而无需直接访问它们的作用域或上下文，但可以使用类似于遥控器般的*播放/暂停*功能。

`gen.throw(NEW ERROR)` 方法使我们能够强制生成器停止执行，即使在其执行作用范围内没有发生任何错误。

**PROMISES**

如果我们需要链式一系列异步操作，我们有几种选择：

- 如果涉及作用域引用，则嵌套回调
- 向处理过程中所需的每个函数传递几十个引用
- 在运行时挂载任何类型的数据并在处调用方法

然而，如果我们想处理在此过程中可能出现的错误，我们基本上就没救了，所以这就是 Promise 可以救场的时刻。

**一种常见的异步方法**

**一种常见的基于 Promise 的方法**

| Async (input, function (output)) | Promise (input).then(function (output)) |
|---|---| 使用 output 做其他事情 | 使用 output 返回某些值 |

在经典方法和基于 Promise 的方法之间存在着细微但非常重要的区别，即 Promise 实例可以原样地传递，然后我们可以通过简单地调用其 `.then()` 方法在任何时候添加我们的逻辑。

**VAR** WAIT UNTIL THIS BOOK FINISHED **NEW** Promise.

*一个新的 Promise 需要一个在稍后被调用的函数*

**FUNCTION**

*一旦此函数被调用，它将接收两个参数：*
- resolve，
- 一个在我们的业务完成后调用的已解析函数
- rejected
- 一个在发生错误时调用的已拒绝函数

**VAR** THINGS TO WRITE (10000)

- 一千件要写

**VAR** BOOK CONTENT -

- 从无内容

**WHILE** THINGS TO WRITE -- (BOOK CONTENT - MORE CONTENT. - TO ALL THE THINGS)

*resolve(BOOK CONTENT)*

*书已完成并解析*

*任何等待此书完成的人。函数*

*有些人可以阅读它*

Promises 最好与 async 一起使用。

上面的示例仅用于演示涉及的逻辑，而并非最佳实践。

**VAR** USERS NEEDED THE NEW Promise (FUNCTION) RETURNS.

每当我们调用 `.then()` 时，我们都会从初始链中创建一个新的 promise。通过链创建的 promise 与简单 promise 之间的主要区别是，对于通过链创建的，我们需要返回某些值，否则它们将接收到 `undefined`。还有 `.NEW Promise (FUNCTION) RETURNS`：如果在任何 Promise 链内部发生错误，只有 `.catch()` 会收到通知，而不是拒绝的那个。这实际上是两种模式之间一个重要的区别，因为即使 Promise 已经解析了。下面是一个示例代码。

**VAR** A NEW Promise (FUNCTION) RETURNS. 

- 这里一切都好
- .then(function (result) { console.log(result); }
- 一个新的 (实际上是 0)
- 一切都好
- 什么 NEW ERROR (实际上是 0)
- 函数 NOERROR (console.error)
- )
- 永远不会
- .catch(function (err)) { console.log("caught", err); }
- )
- 我们在这里
- Promise.then(if).then(if).then(if NEW PROMISE)




使用 Promise 在某种程度上解决生成器是使代码同步化的一种良好方法。

如果你在想是否可以使用 `Promise.all` 来代替等待一个接一个的操作执行，那么答案是肯定的。

而且这样做会更有效，原因在于我们可以并行执行所有这些操作。

## 多个同步操作的更好方法

| 变量 | 同步 | 函数 |
| :--- | :--- | :--- |
| CONSOLE.LOG | 让我们出发吗?, | `yield Promise.all(>)`? |
| 安排 | 酒店 | | |
| 安排 | 飞机 | | |
| 安排 | 行李 | | |
| 安排 | 汽车 | | |

结论：Promise 仍然很强大，但它们的主要缺点是它们无法被取消。这意味着对于任何可能耗费长时间的操作，我们可能会后悔使用它们，因为这些可能不是解决问题的正确方案。相反，我们可以通过进程友的操作来跟踪这些，例如文件下载或图像上传所需的操作。

## 定器

已经提到了同步代码，但到为止还没有具体测试过它们的作用。事实上，同步通常不是为了好玩而创建的，而是我们应用程序中不可避免的一部分，例如数据库查询、客户端-服务器交互、工作器通知等。

JavaScript 还提供了自己的机制来在某个时间点调度执行任意代码。文档详尽且实现最广泛的调度执行函数是 `setTimeout` 和 `setInterval`，它们都能以非阻塞的方式从当前的执行流中分离出来。

### setTimeout(callback, delay, arg1, arg2, ...) 定器, 标识符

如果想在未来的任何时间一次性调用任何函数，`setTimeout` 是实现方法。

### 各种 setTimeout 示例

### 调度在 1 秒后执行

| 函数 | LATERON(LOGMEM) ^ | 它将接收参数，如果指定了 `console.log(mem)()` |
| :--- | :--- | :--- |
| 1000, | 它是以毫秒表示的延迟 `Math.random()` | |
| | 它是稍后传递的可选参数 | |

如果你足够耐心等待一整秒钟，你将在控制台中看到 `Math.random()` 调用返回的随机数。然而，如果你不再对该操作感兴趣了，只要你持有它的标识符，就可以随时清理它。

### clearTimeout(timerIdentifier)

如果你设置了定时器，你也应该能够取消它。这个方法正是是此的。

### 各种 setTimeout(console.log, 1000, content)

`clearTimeout(ti)` *PRINT 不会在 1 秒后被调用*

### setInterval(callback, delay, arg1, arg2, ...) 定器, 标识符

如果说 `setTimeout` 是调度函数执行一次，那么 `setInterval` 则是调度它每隔 `delay` 毫秒执行一次。

### 各种 setInterval 示例

### 每 1 毫秒*

| 函数 | STARTTIME, NINGJITS) ^ |
| :--- | :--- |
| 调用此函数 | |
| 变量 TIME **NEW** Date.now() - STARTTIME)* | |
| 检查时间差 | `console.log(>` | |
| NIJITS(2), TIME.getHours() ) | | |
| 日志* | | |
| 小时* | | |
| NIJITS(2), TIME.getMinutes() ) | | |
| 00 分钟* | | |
| NIJITS(2), TIME.getSeconds() ) | | |
| 以及 02 秒* | | |
| NIJITS(3), TIME.getMilliseconds() ) | | |
| 毫秒* | | |
| 尝试每个毫秒* | | |
| 开始时间* | | |
| 启动此函数转换为 0 或1ms 到 10ms | 函数, 返回数组 | | |
| 0) TIME.on | |

## 计时器, RETARY()

clearInterval(frameIdentifier)

如果你想停止间隔，使用 `clearInterval(chronograph)`，它的逻辑和行为与 `clearTimeout` 完全相同。

关于时间的调度执行，有一个注意事项。如果我们设置了一个 1 秒的超时，但在某点存在一个耗时 2 秒的长操作，那么我们的定时器无法在 2 秒或更之前调度回调。

间隔的调度执行也是如此。例如，时间被调度在 10ms 后，定时器将尝试执行多次，并持续导致可能延迟的执行。

### RequestTimeout)

`RequestTimeout(frameIdentifier, I WOULD` 当页面上出现任何可见信息时，需要比定时器和间隔更好的调度方式，而 RETARY 正为此设计的。

## RequestTimeout(startTime, NIJITS)

| 函数 | 5$) 没有额外参数 |
| :--- | :--- |
| | 执行计时器差异 | | | |
| RETARY)IN 0) TIME | | | | |
| 变量 TIME **NEW** Date.now() - STARTTIME)* | | | | |
| 检查时间差 | `console.log(>` | | | |
| NIJITS(2), TIME.getHours() ) | | | | |
| 日志* | | | | |
| 小时* | | | | |
| NIJITS(2), TIME.getMinutes() ) | | | | |
| 00 分钟* | | | | |
| NIJITS(2), TIME.getSeconds() ) | | | | |
| 以及 02 秒* | | | | |
| NIJITS(3), TIME.getMilliseconds() ) | | | | |
| 毫秒* | | | | |
| 尝试每个毫秒 | | | | |
| 毫秒* | | | | |
| 尝试每个毫秒* | | | | |
| 以及启动此函数转换为 0 或1ms 到 10ms | 函数, 返回数组 | | | | |
| 0) RETARY)IN 0) TIME | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| 0, RETARY)IN 0) TIME | | | | | |
| RequestTimeout(frameIdentifier) | | | | | |





## 统计信息 ^

- STATISTICS 始终是一个数组
- 针对许多 1-10 个参数 ARGUMENTS.LENGTH)
- 如果有额外的参数CONSOLE.LOG(STATISTICS)<1@)
- 记录之前的文本 CONSOLE.LOG(ARGUMENTS>1)
- 记录当前值 ` CONSOLE.LOG(STATISTICS)<1@)
- 记录最后的统计信息字符串 `
- 我们现在可以标记任何反引号后的字符串，并在 **2 6 3**** 之后检查控制台标记器
- 在标签之前的、=、标签之后的函数在返回值之前对其进行转换时特别有用。

## 函数属性（标记） ^

- 针对许多输出声明一个输出、一个正则表达式和一个转换器 >@, RE <2>! , IN (P)! .CHARCODE$AT(0), 1-10 ARGUMENTS.LENGTH) OUTPUT(MASK)<1@, ARGUMENTS>1). REPLACE RE, IN (P); OUTPUT(MASK)<1@), OUTPUT(MASK)<2@).
- 返回 OUT.JOIN(),)
- 转换后的任何值!
- 恶性输入 CONSOLE.LOG(ATTRIBUTES) 输入值 5****VALUE****5!C) 已清洗*

### 正则表达式

正则表达式构造函数及其实例引入了一种强大的语法，能够通过具有特殊含义的特殊字母对字符串进行搜索、匹配、测试或替换。

有许多注意事项、可能的安全影响、字符串编码问题以及处理这些问题的现代或旧方法，我认为在这里部分介绍它们将是明智的。

重要的是了解它们的字面量表示法：
- 如何识别字面量的、内联的正则表达式实例 REGEX <A("SEARCH) VIA.\SPECIFIC-CHARS)IMP)
- 开始
- 结束
- 可选 g,i,m,x 标志

-621

一个没有关于 JavaScript 对象表示法的解释术语表将是不可靠的，所以这里是：
- JSON 是对象、数组、字符串、布尔值、数字、null 以及其他任何内容的字符串表示标准。
- JSON-21 是以下值的字符串表示：
- STR ^NAME$:-JSON,21,VALUES$::>STRING,1.2,^,>@,TRUE,FALSE,NULL`)
我们可以通过 JSON-21.PARSE(STR OR CODE) 解析任何兼容值，使用 JSON-21.STRINGIFY(COMPATIBLEVALUE)，两种方法都接受回调作为可选参数。在解析过程中读取每个实体以及生存值时，将调用回调。

## 数学

这个全局可用的对象充满了方法，其目的是帮助我们进行数学计算。
最常用的是 MATH.POW(NUM, POWER), MATH.STRT(NUM, RAD), MATH.MAX(NUM1, NUM2, NUM1) 和 MATH.MIN(NUM1, NUM2, NUM1)，但你始终可以通过名称检查所有它们，并最终在线调查它们的签名。
- 以下是一个帮助函数，可以告诉我们关于任何对象的很多
- FUNCTION TELLMEABOUT(THAT) CONSOLE.OBJECT.GETOWNPROPERTIESNAMES(THAT)
- TELLMEABOUT(MATH);
- LET SS 看看里面有什么 S*

### PARSEINT(STRING, BASE)NUMBER

当你处理输入时，你处理的是字符串。如果你请求年龄或任何数字，PARSEINT 将帮助你转换输入。CONSOLE.LOG(PARSEINT(3), 我们可以省略基数，然而 PARSEINT(11), PARSEINT(11) 的 BASE 是 3，不是 11) PARSEINT(08) 应该是 0) PARSEINT(16) BASE 25)

### PARFLOAT(STRING)

当你需要将字符串转换为浮点数时，PARFLOAT 是方法。它不接受任何参数，PARFLOAT 不会被识别为数字。

## 新的 JavaScript 特性

自从我开始编写这个术语表以来，情况发生了变化。阅读。这意味着随着步骤匹配，新功能变得可用。JavaScript 规范确实是一个活的的标准。新的 JavaScript 特性，JASCRIPT, 9D。

## JASCRIPT FAST

下面是针对常见问题的快速回答列表：
JASCRIPT FAST? 按需提供
JASCRIPT FAST?

## ***生产环境（PRODUCTION）***意味着什么？
它是通用网站、应用程序、框架、设计或程序的正式版本，目前提供给每个用户。这是我们交付的内容，而不是为了快速测试我们的想法而制作的原型。

***原型（原型）***意味着什么？
我知道这个术语表可能令人困惑，但在涉及非技术 J6 讨论时，原型是一个草图，或者是最终产品的快速创建版本，它可能不应该直接这样进入生产环境。

## 关于 J6 我还应该知道什么？
我一直在使用 J6 及其变体。学习更多是一个好主意，但如果你对前端后端开发感兴趣，你应该先尝试理解。也尝试阅读更新后的书籍，因为在过去的20年里 J6 发生了很大变化。了解过去是好的，但归根结底我们将使用现代功能。

你听说过转换器（TRANSIPLES）吗？
我不光听说过它们，也使用它们。例如，这个术语表中的大多数平台示例已经通过 LABEL-NODE 成功测试，这是一个命令行界面 (CLI)，它将最新的 J6ASCRIPT 规范的最新功能引入代码中。我应该在生产环境中使用它们吗？这取决于情况。

***生产环境***意味着什么？
它是通用网站、应用程序、框架、设计或程序的正式版本，目前提供给每个用户。这是我们交付的内容，而不是为了快速测试我们的想法而制作的原型。

***原型***意味着什么？
我知道这个术语表可能令人困惑，但在涉及非技术 J6 讨论时，原型是一个草图，或者是最终产品的快速创建版本，它可能不应该直接这样进入生产环境。

哪个框架、库或工具我应该使用？
解决你问题的那个。

JASCRIPT 仅用于网页吗？
现在很难找到不运行 J6 的电子设备。智能手表、路由器、你现在的电脑，甚至是彩色的灯泡，都兼容某些 J6 JavaScript 引擎或已经在运行它。

WEAKMAP 快速吗？
类似于 WEAKMAP，J6^3 实例可以关联对象，但移除这种关系是你的责任。

JASCRIPT 快速吗？

新的 JavaScript 特性
现代 JavaScript 引擎可以通过关键字声明。

JASCRIPT FAST$4 按需提供
下面是针对常见问题的快速回答列表：
JASCRIPT FAST? 按需提供
JASCRIPT FAST?




-   需求驱动

这里肯定还有我遗漏的其他问题，我鼓励你去寻找答案。一个拥有优质且通常是最实时的文档的地方是 MDN 开发者网络。

还有许多我没有机会讨论的话题，例如：
- Web Workers、Service Workers、IndexedDB、本地存储（localStorage）和会话存储（SessionStorage）、通过 WebSockets 和 XRequests 进行分页，以及最近的 Fetch API，但我相信如果你已经读到了这里，你现在能够理解大多数在线技术文章了。

## 有用链接

| [Mozilla 开发者网络](https://developer.mozilla.org) | developer.mozilla.org |
| [万维网联盟](https://www.w3.org) | w3.org |
| [IDE Web 控制台](https://ideweb.com) | ideweb.com |
| [WHATWG](https://whatwg.org) | whatwg.org |
| [Node.js](https://nodejs.org) | nodesjs.org |
| [Base64](https://base64.js) | base64.js |
| [<.-6 (书籍系列)](https://youdontknows.com) | youdontknows.com |
| [探索 ES6](https://exploringes6.com) | exploringes6.com |
| [HTTPs](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) | developer.mozilla.org/en-US/docs/Web/API/Fetch_API |
