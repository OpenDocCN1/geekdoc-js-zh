# JavaScript 入门指南









![](img/c595610b738444dc06a09036110543e5_0_0.png)
















# JavaScript 口袋参考

# JavaScript 语言

JavaScript 是一种轻量级的基于对象的脚本语言，可以嵌入到 HTML 页面中。本书首先介绍 JavaScript 核心语言，随后介绍在网络浏览器中客户端 JavaScript 内容。本书的最后部分是核心和客户端 JavaScript API 的快速参考。

## 语法

JavaScript 语法基于 Java 语法，而 Java 语法又模仿了 C 和 C++ 语法。因此，C、C++ 和 Java 程序员应该会发现 JavaScript 语法非常熟悉。

## 大小敏感

JavaScript 是一种大小写敏感的语言。所有关键字均为小写。所有变量、函数名和其他标识符必须使用一致的大小写进行输入。

## 空白字符

JavaScript 忽略标记之间的空白字符。你可以使用空格、制表符和换行符来格式化和缩进代码，使其易于阅读。

## 分号

JavaScript 语句以分号结束。然而，当语句后面跟着换行符时，可以省略结束的分号。请注意，这限制了你在 JavaScript 程序中合法的换行位置：如果第一行本身可以是一个完整的合法语句，则你不能将一个语句跨行分为两行。

## 注释

JavaScript 支持 C 和 C++ 注释。`/*` 和 `*/` 之间的任意数量文本（跨多行）会被 JavaScript 忽略。此外，`//` 到当前行末尾之间的任何文本都是注释，并会被忽略。示例：

```
// 这是一个单行的 C++ 风格注释。
/*
  * 这是一个多行的 C 风格注释。
  * 这是第二行。
*/
/* 另一个注释。 */ // 也是。
```

## 标识符

变量、函数和标签名由字母和数字组成。

## 关键字

JavaScript 保留了以下单词，不能作为标识符使用：

```
abstract
break
case
continue
class
const
debugger
delete
do
double
else
export
extends
false
finally
float
for
function
if
instanceof
int
interface
long
new
null
package
private
public
return
static
super
switch
this
throw
try
typeof
volatile
while
with
```

## 变量

变量被声明和初始化。在 JavaScript 中，你可以使用 `var` 来声明：

```
var i = 1
var x = 3
var message = 'hello';
```

## 数据类型

JavaScript 支持三种原始类型：数字、布尔和字符串；两种复合类型：对象和数组。

## 数字

JavaScript 中的数字采用双浮点格式表示。JavaScript 不区分整数和浮点数。数字字面量在 JavaScript 程序中使用通常语法出现：数字序列，带有可选的小数点和可选指数。整数也可以以十六进制法出现：

```
0xFF // 十进制的 255
```

当数值运算溢出时，它返回一个表示正或负无穷大的特殊值。当运算下溢时，它返回零。当诸如负数的平方根产生错误或无意义的结果时，它返回特殊值 NaN。使用全局函数 `NaN()` 测试此值。Number 对象定义了有用的数值常量。Math 对象定义了各种数学函数，如 `Math.sin()`、`Math.pow()` 和 `Math.random()`。

## 布尔

布尔类型有两个可能，由关键字 `true` 和 `false` 表示。这些值代表真或假、开启或关闭、是或否，或其他任何可以用一个比特表示的内容。

## 字符串

JavaScript 字符串是任意字母、数字以及来自 16 位 Unicode 字符集的序列。字符串字面量出现在 JavaScript 程序中，位于单引号或双引号之间。一种引号可以嵌套另一种引号：

```
'testing'
"3.14"
'name="myform'
'Wouldn't you prefer O'Reilly's book?'
```

当反斜字符 (\) 出现在字符串字面量时，它会改变或转义随后的字符的含义。下表列出了这些特殊转义序列：

| 转义 | 表示 |
| --- | --- |
| \b | 退格 |
| \f | 换页 |
| \n | 换行符 |
| \r | 回车 |
| \t | 制表符 |
| \' | 撇号或单引号（不终止字符串） |
| \" | 双引号（不终止字符串） |
| \\ | 单个反斜杠字符 |





| | 含义 |
|---|---|
| \xdd | 由两个十六进制数字 dd 指定 Latin-1 编码的字符 |
| \udddd | 由四个十六进制数字 ddddd 指定 Unicode 编码的字符 |

String 类定义了许多你可以使用来操作字符串的方法。它还定义了 `length` 属性，该属性指定字符串中字符的数量。

加法运算符 (+) 用于拼接字符串。等号运算符 (==) 比较字符串，以检查它们是否包含完全相同的字符序列。（这是按值比较，而不是按引用，正如 C、C++ 或 Java 程序员可能预期的那样。）不等于运算符 (!=) 执行相反操作。关系运算符 (<, <=, >, 和 >=) 使用字母顺序（字典序）比较字符串。

JavaScript字符串是不可变的，这意味着没有办法改变字符串的内容。操作字符串的方法通常返回字符串的修改后的副本。

## 对象

对象是一个复合数据类型，包含任意数量的属性。每个属性都有一个名称和一个值。`.` 运算符用于访问对象的具名属性。例如，你可以按照如下方式读取和写入对象的属性值：

```
o.x = 1;
o.y = 2;
o.total = o.x + o.y;
```

对象的属性不像在 C、C++ 或 Java 那样预先定义的；任何对象都可以分配任何属性。JavaScript 对象是关联数组：它们将任意的数据值与任意名称关联。由于这一事实，也可以使用数组表示法访问对象属性：

```
o["x"] = 1;
o["y"] = 2;
```

对象使用 `new` 运算符创建。你可以如下所示创建一个没有任何属性的新对象：

```
var o = new Object();
```

通常，你会使用预定义的构造函数来创建属于对象类的成员，这些对象自动定义了合适的属性和方法。例如，你可以创建一个表示当前时间的 Date 对象：

```
var now = new Date();
```

你也可以定义自己的对象类和相应的构造函数；这将在本节稍后的部分介绍。

在 JavaScript 1.2 及更高版本中，你可以使用对象字面量语法在程序中直接包含对象。对象字面量是一个由逗号分隔的键值对列表，包含在花括号内。例如：

```
var o = {x:1, y:2, total:3};
```

请参见参考部分中的 Object（和 Date）。

## 数组

数组是一种包含编号值而非具名值的对象类型。`[]` 运算符用于访问数组的编号值：

```
a[0] = 1;
a[1] = a[0] + a[0];
```

JavaScript 数组的第一个元素是元素 0。每个数组都有一个 `length` 属性，指定数组中元素的数量。数组的最后一个元素是 `length-1`。数组元素可以持有任何类型的值，包括对象和其他数组，并且数组元素不需要都包含相同类型的值。

你使用 `Array()` 构造函数创建数组：

```
var a = new Array(); // 空数组
var b = new Array(10); // 10个元素
var c = new Array(1,2,3); // 元素 1,2,3
```

从 JavaScript 1.2 开始，你可以使用数组字面量语法直接在程序中包含数组。数组字面量是包含在方括号内的逗号分隔的值列表。例如：

```
var a = [1,2,3];
var b = [1, true, {x:1, y:2}, "Hello"];
```

请参见参考部分中的 Array 以获取许多常用的数组操作方法。

## 函数和方法

函数是一段定义一次的 JavaScript 代码，可以被程序执行多次。函数的定义看起来如下：

```
function sum(x, y) {
  return x + y;
}
```

使用 `()` 运算符调用函数，并传递参数值列表：

```
var total = sum(1,2); // 现在 total 现在为 3
```

在 JavaScript 1.1 中，你可以使用 `Function()` 构造函数创建函数：

```
var sum = new Function("x", "y", "return x+y;");
```

在 JavaScript 1.2 及更高版本中，你可以使用字面量语法定义函数，这使得 `Function()` 构造函数变得过时：

```
var sum = function(x,y) { return x+y; }
```

当一个函数被赋值给对象的属性时，它是该对象的方法。在方法体内部，`this` 关键字指向该函数作为属性的对象。

在函数体内，`arguments[]` 数组包含了传递给函数的完整参数集。请参见参考部分中的 Function 和 Arguments。

## null 和 undefined

有两个 JavaScript 值不属于上述描述的任何类型。JavaScript 关键字 `null` 是一个特殊值，表示“无值”。如果一个变量包含 `null`，你就知道它不包含任何其他类型的有效值。JavaScript 中的另一个特殊值是 `undefined` 值，即未初始化变量的值以及当查询不存在的对象属性时返回的值。在 JavaScript 1.5 中，有一个名为 `undefined` 的预定义全局变量，持有这个特殊的 `undefined` 值。`null` 和 `undefined` 的用途相似，且 `==` 运算符认为它们相等；如果你需要区分它们，请使用 `===`。

## 表达式和运算符

表达式通过使用运算符组合值、字面量、变量或函数调用形成。括号 `()` 可用于分组表达式并改变求值顺序。JavaScript 定义了一个完整的运算符，大部分对于 C、C++ 和 Java 程序员来说是熟悉的。如下表所示。P 列指定优先级，A 列指定结合性：

| P | A | 运算符 | 执行的操作 |
|---|---|---|---|
| 15 | L | . | 访问对象属性 |
| | L | [] | 访问数组元素 |
| | L | () | 调用函数 |
| | R | new | 创建新对象 |
| 14 | R | ++ | 后置自增 |
| | R | -- | 后置自减 |
| | R | - | 一元负 |
| | R | + | 一元加 |
| | R | ~ | 按位取反 |
| | R | ! | 逻辑否定 |
| | R | delete | 删除属性 |
| 12 | R | typeof | 返回数据类型 (JS 1.5) |
| | R | void | 返回 undefined 值 (JS 1.1) |
| 13 | L | *, /, % | 乘法、除法、取模 |
| 12 | L | +, - | 加、减法 |
| | L | + | 拼接字符串 |
| 11 | L | << | 整数左移 |
| | L | >> | 右移，符号扩展 |
| | L | >>> | 右移，零扩展 |
| 10 | L | <, <= | 小于、小于等于 |
| | L | >, >= | 大于、大于等于 |
| | L | instanceof | 检查对象类型 (JS 1.5) |
| | L | in | 检查属性是否存在 (JS 1.5) |
| 9 | L | == | 测试相等 |
| | L | != | 测试不相等 |
| | L | === | 测试恒等性 (JS 1.3) |
| | L | !== | 测试非恒等性 (JS 1.3) |
| 8 | L | & | 整数按位与 |
| 7 | L | ^ | 整数按位异异 |
| 6 | L | | | 整数按位或 |
| 5 | L | && | 逻辑与 |
| 4 | L | || | 逻辑或 |
| 3 | R | ?: | 条件运算符 (3 个操作数) |
| 2 | R | = | 赋值 |
| | R | *=,+=,-= 等. | 带运算的赋值 |
| 1 | L | | 多次求值 |





```
typeof
将操作数的类型作为字符串返回。求值为为
"number", "string", "boolean", "object", "function" 或
"undefined"。如果操作数是 null，则求值为 "object"。
```

```
instanceof
如果左侧的对象是用右侧的构造函数（如 Date 或 RegExp）创建的，则求值为 true。
```

```
in
如果右侧的对象具有（或继承自）左侧命名的属性，则求值为 true。
```

```
delete
删除对象的属性。注意，这并不等同于简单地将属性设为 null。如果属性无法删除，则求值为 false，否则为 true。
```

```
void
忽略操作数并求值为 undefined。
```

## 语句 (Statements)

JavaScript 程序是 JavaScript 语句的序列。大多数 JavaScript 语句与对应的 C、C++ 和 Java 语句具有相同的语法。

## 表达式语句

每个 JavaScript 表达式都可以独立作为语句使用。
赋值、方法调用、自增和自减都是
表达式语句。例如：

```
s = "hello world";
x = Math.sqrt(4);
++;
```

## 复合语句

当一组 JavaScript 语句被包裹在大括号内时，它被视为一个单一的复合语句。例如，while 循环的体由单个语句组成。如果你想让循环执行多个语句，请使用复合语句。这是在 if、for 以及后文描述的其他语句中一种“常用技术”。

## 空语句

空语句仅仅是一个独立的分号。它不执行任何操作，有时在编写空循环体时很有用。

## 标记语句

从 JavaScript 1.2 开始，任何语句都可以用一个名称进行标记。标记循环可以与标记版本的 break 和 continue 语句配合使用：

```
label : statement
```

## 语句字母顺序索引

接下来的段落按字母顺序记录了所有的 JavaScript 语句。

### break

- break 语句终止最内层嵌套循环的执行，或者在 JavaScript 1.2 及更高版本中，终止命名的循环：

```
break ;
break label ;
```

### case

case 不是一个真正的语句。相反，它是一个关键字，用于在 JavaScript 1.2 或更高版本的 switch 语句中标记语句：

```
case constant-expression :
statements
[ break ; ]
```

由于 switch 语句的性质，由 case 标记的语句组通常以 break 语句结束。

### continue

continue 语句重启最内层嵌套的循环，或者在 JavaScript 1.2 及更高版本中，重启命名的循环：

```
continue;
continue label;
```

### default

与 case 类似，default 不是一个真正的语句，而是一个可能出现在 JavaScript 1.2 或更高版本 switch 语句中的标记：

```
default:
statements
[ break ; ]
```

### do/while

do/while 循环在表达式为真时重复执行语句。它与 while 循环相似，区别在于循环条件出现在（并在其处进行测试）循环的底部。这意味着循环体至少会被执行一次：

```
do
statement
while ( expression );
```

该语句是在 JavaScript 1.2 中引入的。在 Netscape 4 中，continue 语句在 do/while 循环中无法正常工作。

### for

for 语句是一种易用的循环，它将初始化和递增表达式与循环条件表达式相结合：

```
for (initialize ; test ; update )
statement
```

只要测试表达式为真，循环就会重复执行语句。它在启动循环之前求值初始化表达式，并在每次迭代结束时求值更新表达式。

for/in 语句遍历指定对象的属性：
```
for (variable in object)
statement
```

for/in 循环为对象的每个属性执行一次语句。循环每次执行时，都会将当前属性的名称赋值给指定的变量。预定义 JavaScript 对象的某些属性不会被 for/in 循环枚举。用户定义的属性始终会被枚举。

函数语句（function statement）在 JavaScript 程序中定义一个函数：

```javascript
function funcname ( args ) {
statements
}
```

该语句定义了一个名为 funcname 的函数，其函数体由指定的语句组成，参数由 args 指定指定。args 是一个由逗号分隔的零或多个参数名称列表。这些参数可以在函数体中使用，以引用传递给函数的参数。

### if

if 语句在表达式为真时执行一个语句：

```javascript
if ( expression )
statement
```

当添加了 else 子句时，如果表达式为假，该语句将执行另一个语句：

```javascript
if ( expression )
statement
else
statement2
```

任何 else 子句都可以与嵌套的 if/else 语句组合产生 else if 语句：

```javascript
if ( expression )
    statement
  else if ( expression2 )
    statement2
  else
    statement3
```

### return

return 语句导致当前执行的函数停止执行并返回调用者。如果后面跟着一个表达式，该表达式的值将作为函数的返回值：
```
  return ;
  return expression;
```

### switch

switch 语句多多分支。它计算一个表达式，然后跳转到与表达式值匹配的 case 标记的语句。如果没有找到匹配的 case 标签，switch 语句跳转到标记为 default 的语句（如果有）：

```javascript
switch ( expression ) {
    case constant-expression : statements
    [ break ; ]
    default: statements
}
```

### throw

throw 语句指示错误或抛出异常。它导致程序跳转到最近的异常处理器（参见 try/catch/finally）。throw 语句由 ECMA3 定义并在 1.5 实现。其语法为：
```
throw expression;
```

### try/catch/finally

try/catch/finally 语句是 JavaScript 的异常处理机制。它由 ECMA3 定义并在 1.5 实现。其语法为：

```javascript
try {
  statements
} catch ( argument ) {
  statements
} finally {
  statements
}
```

该语句的 try 部分定义了一个处理异常和错误的代码块。如果发生程序错误或在 try 块中抛出异常，控制跳转到 catch 子句。该子句包含一个参数；抛出的值赋值给此本地变量，以便语句引用。finally 子句包含在 try 或 catch 子句之后执行的语句，无论是否抛出异常。catch 和 finally 子句是可选的，但不能两个都省略。

### var

var 语句声明并可选地初始化一个或多个变量。变量声明在顶层代码中可选的，但在函数体内是必须：

```javascript
var name [ = value ] , name2 [ = value2 ] ...
;
```

### while

while 语句基础循环。它在表达式为真时重复执行语句：

```javascript
while ( expression )
  statement;
```

### with

with 语句将对象添加到作用链中，以便语句在对象的上下文中进行解释：

```
with ( object )
  statement
```

with 语句具有一些且非直观的副作用；强烈建议不要使用。

## 面面向 JavaScript

JavaScript 对象是将值与命名属性关联的关联数组。JavaScript 提供了简单的继承机制，可以定义新的类供自己的程序使用。要定义一个新类，从编写构造函数开始。构造函数就像任何其他函数，除了它是用 `new` 运算符调用的，并且使用 `this` 关键字来引用和初始化新创建的对象。例如，这里创建一个名为 Point 的新类对象的构造函数：

```javascript
function Point(x,y) { // Point 的构造函数
  this.x = x; // 初始化 X 坐标
  this.y = y; // 初始化 Y 坐标
}
```

每个作为构造函数的 JavaScript 函数都有一个名为 prototype 的属性。该属性引用为构造函数创建的对象的类的特殊原型对象。你在原型对象上定义的任何属性都会被该构造函数创建的所有对象继承。原型对象通常用于为类的所有实例提供方法。定义名为 toString 的方法



允许你的类实例转换为字符串。例如：

```
// 定义函数字量并将它们赋值
// 给原型对象的属性。
Point.prototype.distanceTo = function(that) {
  var dx = this.x - that.x;
  var dy = this.y - that.y;
  return Math.sqrt(dx*dx + dy*dy);
}
Point.prototype.toString = function () {
  return ('(' + this.x + ',' + this.y + ')');
}
```

如果你想定义静态（或类级）方法或属性，可以直接将它们赋值给构造函数，而不是赋值给原型对象。例如：

```
// 定义一个通用的 Point 常量
Point.ORIGIN = new Point(0,0);
```

前面的代码片段定义了一个简单的 Point 类，我们可以像下面的代码一样使用它：

```
// 调用构造函数创建一个新的 Point 对象
var p = new Point(3,4);
// 调用对象的方法，使用静态
// 属性作为参数。
var d = p.distanceTo(Point.ORIGIN);
// 将对象添加到字符串中会隐式地
// 调用 toString();
var msg = "Distance to " + p + " is " + d;
```

## 正则表达式

JavaScript 支持用于模式匹配的正则表达式，其语法与 Perl 语言相同。JavaScript 1.2 支持 Perl 4 正则表达式，JavaScript 1.5 增加了 Perl 5 正则表达式的一些额外功能。正则表达式在 JavaScript 程序中以字面量指定，即斜杠（/）字符之间的字符序列，可选跟随一个或多个修饰符 g（全局搜索）、i（不区分大小写）和 m（多行模式；JavaScript 1.5 的特性）。除了这种字面量语法外，还可以使用 RegExp() 构造函数创建 RegExp 对象，它接受模式和修饰符字符作为字符串参数，不需要斜杠字符。

正则表达式语法的完整说明超出了本书的范范围，但后续小节中的表格提供了简要的语法总结。

## 字面字符

字母、数字和大多数其他字符在正则表达式中都是字面量：它们只需匹配自身。然而，正如我们在接下来的章节中看到的，有一些标点字符和转义序列（以 \ 开头）具有特殊含义。这些转义序列中最简单的是提供了表示字面字符的替代方法：

| 字符 | 含义 |
| :--- | :--- |
| \n, \r, \t | 匹配字面换行符、回车符、制表符 |
| \,, /, \*, \+, \?, 等. | 字面匹配标点字符，忽略或转义其特殊含义 |
| \xnn | 十六进制编码 nn 的字符。 |
| \xxxx | 十六进制编码 xxxx 的 字符。 |

## 字符类

正则表达式语法使用方括号表示模式中的字符集或类。此外，转义序列定义了某些常用的字符类，如下表所示。

| 字符 | 含义 |
| :--- | :--- |
| [...] | 匹配括号内的任意一个字符 |
| [^...] | 匹配括号外的任意一个字符 |
| . | 匹配除换行以外的任何字符 |

| 字符 | 含义 |
| :--- | :--- |
| \w, \W | 匹配任何单词/非单词字符 |
| \s, \S | 匹配任何空白/非空白 |
| \d, \D | 匹配任何数字/非数字 |

## 重复

下表显示了控制匹配项重复次数的正则表达式语法。

| 字符 | 含义 |
| :--- | :--- |
| ? | 可选术语；匹配零或一次 |
| + | 匹配前面的术语一次或多次 |
| * | 匹配前面的术语零或多次 |
| {n} | 匹配前面的术语恰好 n 次 |
| {n,} | 匹配前面的术语 n 次或多次 |
| {n,m} | 至少 n 次但不超过 m 次 |

在 JavaScript 1.5 中，任何重复字符后面都可以跟一个问号，使其变为非贪婪模式（non-greedy），这意味着它们在允许完整模式匹配的同时，尽可能匹配最少的重复次数。

## 分组与选择

正则表达式使用括号对子表达式进行分组，就像数学表达式一样。括号非常有用，例如可以允许重复字符应用于整个子表达式。它们对于 | 字符也很有用，该字符用于分隔备选方案。括号分组具有特殊行为：当找到模式匹配时，匹配每个组的文本会被保存，并通过组编号进行引用。下表总结了这种语法。

| 字符 | 含义 |
| :--- | :--- |
| (expression) | 捕获组 |
| (?:expression) | 非捕获组 |
| a|b | 选择（匹配 a 或 b） |

## 锚点

锚点用于匹配字符串中的位置而不是字符本身。

| 字符 | 含义 |
| :--- | :--- |
| ^ | 匹配字符串或行的开始 |
| $ | 匹配字符串或行的结束 |
| \b | 匹配单词边界 |
| \B | 匹配非单词边界 |

## 前瞻与后瞻

前瞻（Lookahead）和后瞻（Lookbehind）是根据周围文本匹配位置的断言类型。

| 字符 | 含义 |
| :--- | :--- |
| (?=...) | 正向先行 |
| (?!...) | 负向先行 |
| (?<=...) | 正向后瞻 |
| (?<!...) | 负向后瞻 |

[/

解释 JavaScript 代码如何嵌入到 HTML 文件中，然后介绍客户端 JavaScript 对象、JavaScript 事件和事件处理，以及 JavaScript 安全限制。

## HTML 中的 JavaScript

JavaScript 代码可以以脚本、事件处理程序和 URL 的形式嵌入到 HTML 文件中，详细信息见下文。

## <script> 标签

大多数 JavaScript 代码出现在 HTML 文件的 `<script>` 标签和 `</script>` 标签之间。例如：

```
<script>
document.write("The time is: " + new Date());
</script>
```

在 JavaScript 1.1 及更高版本中，你可以使用 `<script>` 标签的 `src` 属性指定要加载并执行的外部脚本的 URL。JavaScript 代码文件通常具有 .js 扩展名。请注意，在使用此属性时仍然需要 `</script>` 标签：

```
<script src="library.js"></script>
```

HTML 允许使用 JavaScript 以外的语言编写脚本，某些浏览器（如 Internet Explorer）支持 VBScript。你可以使用 `language` 属性来指定脚本编写的语言。该属性在所有浏览器中默认为“JavaScript”，因此你通常不需要设置它。你还可以使用如“JavaScript1.3”和“JavaScript1.5”等属性值来指定代码使用的 JavaScript 版本。不支持指定语言版本的浏览器将直接忽略该脚本。

HTML 4 实际上并不识别 `<script>` 标签的 `language` 属性。相反，指定脚本语言的官方方法是使用 `type` 属性。对于 JavaScript，将此属性设为 MIME 类型 "text/javascript"：

```
<script src="functions.js" language="JavaScript1.5" type="text/javascript"></script>
```

## 事件处理程序

JavaScript 代码也可以作为 HTML 标签事件处理程序属性的值出现。事件处理程序属性名称始终以 "on" 开头。其中一个属性指定的代码会在命名事件发生时执行。例如，下面的 HTML 创建了一个按钮，`onclick` 属性指定了一个在用户点击按钮时显示警框（对话框）的事件处理程序：

```
<input type="button" value="Press Me" onclick="alert('Hello World!');">
```

其他可用事件处理程序属性的列表在本节稍后包含。

## JavaScript URL

JavaScript 代码可以出现在特殊 `javascript:` 伪协议的 URL 中。此类 URL 的内容通过评估 JavaScript 代码并将结果值转换为字符串来确定。如果你想使用 JavaScript URL 执行 JavaScript 代码，而不返回任何会覆盖当前文档的内容，请使用 `void` 运算符：

```
<form action="javascript:void validate()">
```

## Window 对象

Window 对象表示浏览器窗口。在客户端 JavaScript 中，Window 对象是定义了所有顶层属性和方法的全局对象。Window 对象的属性和方法是全局属性和全局函数，你可以通过任何对象前缀来引用它们。Window 对象的属性之一名为 `window`，它指向 Window 对象本身：

```
window             // 全局 Window 对象
window.document //窗口的 document 属性
document         // 或者省略对象前缀
```

参见参考部分中的 Window 对象以获取属性和方法的完整列表。接下来的章节总结了这些属性和方法中最部分，并演示了使用 Window 对象的关键客户端编程技术。请注意，Window 对象最重要的属性是 `document`，它指向浏览器窗口显示的文档。Document 对象将在这些窗口相关子节之后的后续章节中进行描述。

## 简单对话框

三种方法允许你向用户显示简单的对话框。`alert()` 让你向用户显示消息，`confirm()` 让你向用户提一个是或否的问题，`prompt()` 让你要求用户输入单行文本。例如：

```
alert("Welcome to my home page!");
if (confirm("Do you want to play?")) {
    var n = prompt("Enter your name");
}
```

## 状态栏

大多数浏览器在窗口底部包含一个状态栏，用于显示链接的目的地和其他信息。你可以使用 `status` 属性指定出现在状态栏中的文本。你在该属性上设置的文本将显示在状态区域，直到你或浏览器用新值覆盖它。你还可以设置 `defaultStatus` 来指定当浏览器不在状态栏显示任何其他信息时默认显示的文本。这是一个使用 JavaScript 将状态设置为链接 URL 以外内容的 HTML：

```html
<a href="help.html" onmouseover="window.status='Help'; return true;">Help</</a>
```

## 定时器

客户端 JavaScript 使用定时器来指定在经过特定时间后运行的代码。要运行一次代码，请调用 `setTimeout()` 方法。如果你想重复运行代码，请使用 `setInterval()` 以及调用之间的毫秒数。这两个函数都会返回一个值，你可以将其传递给 `clearInterval()`。例如：

```javascript
var count = 0;
// 每秒更新状态
var timer = setInterval("status=++count",1000);
// 5秒后停止更新
setTimeout("clearInterval(timer)",5000);
```

## 系统信息

Window 对象的 `navigator` 和 `screen` 属性引用 `Navigator` 和 `Screen` 对象，这些对象本身定义了包含系统信息的属性，例如运行的操作系统和屏幕分辨率。详情请参见参考部分的 Navigator 和 Screen。在为特定的网络浏览器或版本编写代码时，通常使用 `navigator` 对象：

```javascript
if (navigator.appName == "Netscape" && parseInt(navigator.appVersion) == 4) {
    // 编写 Netscape 4 的代码
}
```




## 窗口控制

Window 对象定义了移动、调整窗口大小和滚动窗口的方法，以及为窗口赋予键盘焦点或撤销窗口焦点的方法。例如：

```
// 每秒自动滚动 10 像素
setInterval("scrollBy(0,1)", 100);
```

更多信息请参阅参考部分 Window 对象条目中的 `moveTo()`、`moveBy()`、`resizeTo()`、`resizeBy()`、`scrollTo()`、`scrollBy()`、`focus()` 和 `blur()`。

比起操作现有窗口的方法，更重要的是用于创建新浏览器窗口的 `open()` 方法和关闭脚本创建的窗口的 `close()` 方法。`open()` 方法接受三个参数。第一个是在新窗口中显示的 URL。第二个是窗口的可选名称。如果已经存在同名的窗口，则会重用它，而不会创建新窗口。第三个参数是一个可选的字符串，用于指定新窗口的大小以及它应该显示的特性（或外框，chrome）。例如：

```
// 打开一个新窗口
w = open("new.html", "newwin", // URL 和名称
"width=400,height=300," + // 大
"location,menubar," + // 外框
"resizable,scrollbars,status,toolbar");
w.close();
```

注意，大多数浏览器仅允许脚本关闭自己打开的窗口。此外，由于最近 Web 上讨厌弹出广告的泛滥，某些浏览器完全不允许脚本打开新窗口。

## 多个窗口和帧（frames）

如前所述，Window 对象的 `open()` 方法允许你创建由新 Window 对象表示的新浏览器窗口。脚本运行的窗口是该脚本的全局对象，你可以像使用它们是全局定义的一样使用该 Window 对象的所有属性和方法。然而，当运行在一个窗口中的脚本需要控制或与另一个窗口交互时，你必须显式指定该 Window 对象：

```
// 创建新窗口并对其进行操作
var w = open("newdoc.html");
w.alert("Hello new window");
w.setInterval(scroll(0,1),50);
```

HTML 允许单个窗口拥有多个帧（frames）。许多网页设计师选择避免使用帧，但它们仍然相当常用。JavaScript 将每个帧视为一个独立的 Window 对象，不同帧中的脚本独立运行。Window 对象的 `frames` 属性是一个 Window 对象数组，表示窗口的子帧：

```
// 帧中的脚本通过这种方式引用帧：
frames[0].location = "frame1.html";
frames[1].location = "frame2.html";
// 对于嵌套帧，你可以使用：
frames[1].frames[2].location = "frame2.3.html";
// 帧中的代码引用顶层窗口：
top.status = "Hello from the frame";
```

Window 对象的 `parent` 属性指向包含它的浏览器窗口或窗口。`top` 属性指向位于帧层次结构根节点的顶层帧或窗口。如果 Window 对象代表的是顶层窗口而非帧，那么 `parent` 和 `top` 属性直接指向 Window 对象本身。

每个浏览器窗口和帧都有独立的 JavaScript 执行上下文，并且在每个上下文中，Window 对象都是全局对象。这意味着在窗口或帧中的脚本声明的任何变量或定义的函数都将成为相应 Window 对象的属性。这允许一个窗口或帧中的脚本使用另一个窗口或帧定义的变量和函数。例如，通常会在顶层窗口的 `<head>` 中定义函数，然后让嵌套帧中的脚本和事件处理器使用 `top` 属性调用这些函数：

```
// 帧中的代码调用顶层窗口的代码。
top.stop_scrolling();
```

## Document 对象（Document）

每个 Window 对象都有一个 `document` 属性，指向一个 Document 对象。可以说，Document 对象比 Window 对象本身更重要；Window 代表浏览器窗口，而 Document 对象代表在窗口中显示的 HTML 文档。Document 对象具有各种指向其他对象的属性，这些属性允许访问和修改文档内容。访问和修改文档内容的方式被称为文档对象模型，或 DOM，目前存在多种 DOM：

## 遗留 DOM (Legacy DOM)

原始的遗留文档对象模型随着 JavaScript 语言早期版本的发展而进化。它得到了所有浏览器的支持，但允许访问文档的某些关键部分，例如表单、表单元素和图像。

## W3C DOM

该文档对象模型允许访问和修改所有文档内容，并由世界维网联盟（W3C）标准化。Netscape 6 及更高版本、Internet Explorer 5 及更高版本以及其他现代浏览器至少部分支持它。W3C DOM 与 IE4 DOM 并不完全兼容，但它确实标准化了原始 DOM 的许多遗留特性。本书涵盖了该标准的核心功能，并为处理 HTML 文档的 JavaScript 程序员提供了一个相关的 DOM 子集。你可以在《JavaScript: The Definitive Guide》中找到完整内容。

## IE 4 DOM

微软的 Internet Explorer 4 为遗留 DOM 增加了强大的功能，用于访问和修改文档内容。这些功能从未标准化，但非微软浏览器支持其中的某些功能。

## 遗留 DOM (Legacy DOM)

原始的客户端 JavaScript DOM 通过对象属性提供了对文档内容的访问。几个只读属性（如 `title`、`URL` 和 `lastModified`）提供了关于文档整体的信息。其他属性是指向特定类型内容的数组：

- `forms[]`：文档中表单对象的数组。
- `images[]`：文档中图像对象的数组。
- `applets[]`：表示嵌入文档的 Java applet 数组。JavaScript 实际上可以用于编写和控制这些 applet，但这超出了本文的范围。
- `links[]`：文档中超链接对象的数组。
- `anchors[]`：表示文档中锚点（通过 `<a>` 标签的 name 属性创建）的对象的数组。

这些数组按照对象在文档中出现的顺序排列。因此，文档中的第一个表单是 `document.forms[0]`，第三张图像是 `document.images[2]`。另一种引用文档表单、图像和 applet 的方法是使用 HTML `name` 属性为它们命名：

```
<form name="address">...</form>
```

当表单、图像或 applet 以这种方式命名时，你可以使用该名称在数组中查找，或者直接作为文档自身的属性查找：

```
document.forms["address"] // 一个命名的表单
document.address // 相同的结果
```

Form 对象特别有趣。它有一个 `elements[]` 数组，包含表单元素的对象，按它们在表单中出现的顺序排列。这些表单元素的详细信息，请参见参考部分的 Input、Select 和 Textarea 。

Form 的 `elements[]` 数组工作方式与 Document 的 `forms[]` 数组非常相似：它按照表单中出现的顺序持有元素元素，但也允许通过名称引用它们。考虑以下 HTML 代码：

```html
<form name='address'><input name='street'></form>
```

你可以通过多种方式引用表单中的输入元素：

```
document.forms[0].elements[0]
document.address.elements['street']
document.address.street
```

遗留 DOM 不提供除表单、表单元素、图像、applet 和锚点之外的引用文档内容的方法。例如，没有任何数组可以提供所有 `<h1>` 标签的列表，也没有任何方法



获取文档实际文本的脚本。这是 W3C 和 IE 4 DOM 已经解决的缺陷，正如我们稍后看到的。尽管具有局限性，但遗留 DOM 允许脚本动态更改某些文档内容，我们将在接章节中看到。

## 动态生成的文档

除了已经描述的属性外，文档对象定义了几个用于动态生成文档内容的重要方法。使用 `write()` 方法在包含方法调用的 `<script>` 标签位置向文档输出文本。例如：

```
document.write("<p>今天是: " + new Date());
document.write("<p>文档更新时间: " + 
document.lastModified);
```

注意，这种方式输出的文本可能包含任意 HTML 标签；浏览器会在执行输出这些文本的脚本后解析并显示此类文本。

只有在文档仍在加载时，才能在 `<script>` 标签中使用 `write()` 方法。如果你尝试在文档加载后触发的事件处理器中使用它，它会擦除文档以及其中包含的事件处理器。然而，在一个窗口或帧中使用一个事件处理器来触发另一个窗口的 `document.write()` 调用是合法的。但是，当你这样做时，必须写入新文档的完整内容，并记住在此时调用 `document.close()` 方法：

```
var clock = open("", "", "width=400,height=30");
var d = clock.document; // 为了方便输入
setInterval("d.write(new Date());\d.close();",
1000);
```

## 动态表单

正如我们看到的，Form  `elements[]` 数组包含了表示表单输入元素的对象。这些许多对象都具有你可以用于查询或设置显示在表单元素中的值的属性。这提供了动态更改文档内容的另一种方法。例如，以下代码设置 Text 对象的 `value` 属性以显示当前本地时间。

```
<form><input size=10></form>
<script> /* 在表单中显示时 */
// 我们正在处理的元素
var e = document.forms[0].elements[0];
// 在元素中显示时间的代码
var s="e.value=(new Date()).toLocaleString();";
setInterval(s, 1000); // 每秒运行一次
</script>
```

## 表单验证

`<form>` 标签支持 `onSubmit` 事件处理器，它会在用户尝试提交表单时触发。你可以使用此事件处理器执行验证：例如，检查所有必填字段是否已填写。如果 `onSubmit` 处理器返回 `false`，则表单不会提交。

```
<form name="address" onsubmit="checkAddress()">
<!-- 表单元素位于此处 -->
</form>
<script>
// 一个简单的表单验证函数
function checkAddress() {
var f = document.address; // 要检查的表单
// 遍历所有元素
for(var i = 0; i < f.elements.length; i++) {
// 忽略文本输入元素以外的所有元素
if (f.elements[i].type != "text") continue;
// 获取用户的输入
var text = f.elements[i].value;
// 如果未填写，则提示用户
if (text == null || text.length == 0) {
alert("请填写所有表单字段。");
return false;
}
}
}
</script>
```

## 图片悬停切换 (Image rollovers)

遗留 DOM 允许你完成一种常见的特殊特效：动态用另一张图片替换页面上的图片。这通常用于图片悬停切换，即图片在鼠标移动到其上方时发生变化。Document 对象的 `images[]` 数组包含了表示文档图片的 Image 对象。每个 Image 对象都有一个 `src` 属性，用于指定要显示的图片的 URL。要更改显示的图片，只需将此属性设置为新的 URL 即可：

```
document.images[0].src = "newbanner.gif";
```

要使用此技术进行图片悬停切换，你必须结合在鼠标移动进入和离开图片时触发的 `mouseover` 和 `mouseout` 事件处理器使用它。以下是带有 JavaScript 事件处理器的基础 HTML 代码，用于实现切换：

```
<img name="button" src="b1.gif"
onmouseover="document.button.src='b2.gif';
onmouseout="document.button.src='b1.gif';">
```

当图片要动态显示时，预先将其加载到浏览器缓存中是有帮助的，这样在它出现之前就不会有网络延迟。你可以通过动态创建一个离屏的 Image 对象来实现：

```
var i = new Image(); // 创建 Image 对象
i.src="b2.gif"; // 加载但不显示图片
```

## 使用 cookie

Document 对象的 `cookie` 属性是一个特殊的属性，它允许你设置和查询与文档相关的 cookie。要与文档关联一个瞬态 cookie，只需将 `cookie` 属性设置为如下格式的字符串：

```

name=value
```

这将为该文档创建一个具有指定名称和值的 cookie。如果你想创建一个即使用户退出浏览器也会存储的 cookie，请使用如下格式的字符串添加过期日期：

name=value; expires=date

过期日期应该是 `Date.toString()` 返回的格式。如果你希望你网站的其他文档可以访问该 cookie，可以指定路径前缀：

name=value; expires=date; path=prefix

单个文档可能有多个与其相关的 cookie。要查询文档的 cookie，只需读取 `cookie` 属性。该字符串包含由分号和空格分隔的多个 `name=value` 字符串。这里是一个获取命名 cookie 值的函数。它假设 cookie 永远不包含分号。

```
function getCookie(name) {
  // 将 cookies 拆分为数组
  var cookies = document.cookie.split('; ');
  for(var i = 0; i < cookies.length; i++) {
    var c = cookies[i]; // 一个 cookie
    var pos = c.indexOf('='); // 找到符号
    var n = c.substring(0,pos); // 获取名称
    if (n == name) // 如果匹配
      return c.substring(pos+1); // 返回值
  }
  return null; // 找不到命名的 cookie
}
```


 W3C DOM 标准化了遗留 DOM 的大部分功能，但也增加了一些重要的新功能。除了支持 `forms[]`、`images[]` 以及 Document 对象的其他数组属性外，它还定义了允许脚本访问和操作任何文档元素的方法，而不仅仅是表单和图片等特殊用途元素。

### 通过 ID 查找元素

在创建包含将被脚本操作的特殊元素的文档时，你可以通过为其提供唯一值的 id 属性来标识每个特殊元素。然后，你可以使用 Document 对象的 `getElementById()` 方法通过 ID 查找这些元素：

```
<h1 id="title">标题</h1>
<script>
  var t = document.getElementById("title");
</script>
```

### 通过标签名查找元素

访问文档元素的另一种方法是通过标签名查找它们。Document 对象的 `getElementsByTagName()` 方法返回一个该类型元素的数组。每个文档元素也支持相同的方法，因此你也可以获取特定元素后代的特定类型标签的数组：

```
// 获取所有 <ul> 标签的数组
var lists = document.getElementsByTagName("ul");
// Find第二个 <ul> 中的第 3 个 <li>
var item = lists[1].getElementsByTagName("li")[2];
```

### 遍历文档树

W3C DOM 将每个文档表示为树。树的节点代表组成文档的 HTML 标签、文本字符串和 HTML 注释。树的每个节点由一个 JavaScript 对象表示，每个节点都有允许遍历树的属性，代码片段所示：

```
// 在文档中查找节点
var n = document.getElementById("mynode");
var p = n.parentNode; // 父标签
var c0 = n.firstChild; // n 的第一个子节点
```



```javascript
var c1 = c0.nextSibling; // n的第2个孩子
var c2 = n.childNodes[2]; // n的第3个孩子
var last = n.lastChild; // n的最后一个孩子
```

更多细节请参见参考章节中的 Node。

Document 对象本身也是一种节点，并支持这些相同的属性。`Document` 对象的 `documentElement` 属性指向所有 HTML 文档根节点的单个 `<html>` 标签元素，而 `body` 属性指向 `<body>` 标签。

## 节点类型

文档树中的每个节点都有一个 `nodeType` 属性，用于指定节点的类型。不同类型的节点由 `Node` 对象的不同子类表示。以下节点值对于处理 HTML 文档的 JavaScript 程序员是相关的（XML 文档存在其他值）：

| node | Represents |
|---|---|
| 1 | Element: 一个 HTML 标签 |
| 2 | Text: 文档中的文本 |
| 8 | Comment: 一个 HTML 注释 |
| 9 | Document: HTML 文档 |

使用 `Element` 节点的 `nodeName` 属性来确定它所代表的 HTML 标签名称。使用 `Text` 和 `Comment` 节点的 `nodeValue` 属性来获取节点所代表的文档文本或注释文本。参见参考章节中的 `Element`、`Text`、`Comment` 和 `Document` 了解这些节点类型的详细信息。另见 `Node` 以了解它们共同拥有的属性和方法。

正如我们在上面看到的，文档树中的 HTML 标签由 `Element` 对象表示。在 HTML 文档中，每个 `Element` 对象都有直接对应于 HTML 标签属性的属性。例如，你可以通过设置相应 `Element` 对象的 `caption` 属性，来查询或设置 `<table>` 标签的 `caption` 属性值。参见参考章节中的 `Element` 了解详情。

## 操作文档元素

使用 W3C DOM 操作 HTML 文档的一种简单方法是设置与 HTML 属性相对应的属性。正如我们在旧版 DOM 中看到的，这允许你通过设置代表 `<img>` 标签的文档元素的 `src` 属性来更改图像，例如。它还允许你设置文档元素的颜色、大小和对齐。操作文档元素的一种特别有效的方法是通过控制 CSS 样式的 `style` 属性。我们将在稍后详细介绍这个重要的话题。

## 修改文档文本

你可以通过简单设置 `Text` 节点的 `nodeValue` 属性来更改文档的文本内容：

```javascript
// 找到文档中的第一个 <h1> 标签
var h1 = document.getElementsByTagName("h1")[0];
// 设置其第一个子节点的新文本
h1.firstChild.nodeValue = "New heading";
```

除了操作 `nodeValue` 属性外，`Text` 对象还允许你修改 `data` 属性，或者使用方法追加、插入、删除或替换文本。

注意，上述代码的问题在于它假设了 `<h1>` 标签的内容是纯文本。对于具有以下标题的文档，代码将失败：

因为标题的文本是 `<h1>` 标签的孙节点，而不是直接子节点：

```html
<h1><i>Original Heading</h1></h1>
```

解决此问题的方法有一种一种是设置标题节点的 `innerHTML` 属性。该属性是 IE 4 DOM 的一部分，而不是 W3C DOM，但由于它非常有用，大多数现代浏览器都支持它。当我们考虑 IE 4 DOM 时会再次看到它。另一种解决此问题的方法是用新建的 `<h1>` 标签和包含所需文本的文本节点替换标题节点，如下节所示。

## 修改文档结构

除了更改文档文本和文档元素的属性外，W3C DOM 允许你更改文档本身的树形结构。这是通过 `Node` 方法（允许插入、追加、移除和替换节点的子节点）以及 `Document` 方法（允许创建新的 `Element` 和 `Text` 节点）来实现。以下代码说明了：

```javascript
// 通过名称查找 <ol> 元素：
var list = document.getElementById("mylist");
// 创建一个新的 <li> 元素
var item = document.createElement("li");
// 将其添加到列表
list.appendChild(item);
// 创建文本节点
var text = document.createTextNode("new item");
// 将其追加到新的 <li> 节点
item.appendChild(text);
// 从列表中移除新项
list.removeChild(item);
// 将新项置于列表开头
list.insertBefore(item,list.firstChild);
```

作为一个进一步示例，这里有一个 JavaScript 函数，它使用 W3C DOM 通过在新建的 `<b>` 标签内重新设置父节点来体现任意文档节点：

## IE 4 DOM

IE 4 DOM 在微软 Internet Explorer 浏览器的 4 版本中引入。它是一个强大但非标准的 DOM，具有与 W3C DOM 类似的能力。IE 5 及更高版本包含了对大多数基本 W3C DOM 特的支持，但包含此关于 IE 4 DOM 的文档是因为 IE 4 仍然在使用中。以下子章节记录了 IE 4 DOM 与 W3C DOM 的差异，因此你应该先熟悉 W3C DOM。

## 访问文档 4 DOM 元素

IE 4 DOM 不支持 `getElementById()` 方法。相反，它允许你通过文档对象的 `all[]` 数组根据 `id` 属性查找任意文档元素：

```javascript
var list = document.all["mylist"];
list = document.all.mylist; // 这是相同的
```

IE 4 DOM 没有支持 `getTagName()`，而是使用 `all[]` 数组查找标签：

```javascript
var lists = document.all["UL"];
var items = document.all.LI;
```

#遍历文档树

正如我们在上面看到的，文档树中的 HTML 标签由 `Element` 对象表示。在 HTML 文档中，每个 `Element` 对象都有直接对应于 HTML 标签属性的属性。例如，你可以通过设置相应 `Element` 对象的 `caption` 属性，来查询或设置 `<table>` 标签的 `caption` 属性值。参见参考章节中的 `Element`。

IE 4 和 W3C DOM 之间的一个重要区别是 IE 4 DOM 注释。在 W3C DOM 中，注释被忽略了。在 IE 4 DOM 中，你可以使用以下属性遍历：

- `firstChild`
- `nextSibling`
- `parentNode`
- `previousSibling`
- `childNodes`
- `children`

注意，上述代码的问题在于它假设了 `<h1>` 标签的内容是纯文本。对于具有以下标题的文档，代码将失败因为标题的文本是 `<h1>` 标签的孙节点，而不是直接子节点：

## 修改文档内容和结构

正如我们在上面看到的，文档树中的 HTML 标签由 `Element` 对象表示。在 HTML 文档中，每个 `Element` 对象都有直接对应于 HTML 标签属性的属性。例如，你可以通过设置相应 `Element` 对象的 `caption` 属性，来查询或设置 `<table>` 标签的 `caption` 属性值。参见参考章节中的 `Element`。

IE 4 DOM 没有任何显式创建、插入、移除或替换节点的方法。然而，它支持非常重要的 `innerHTML` 属性，允许用任意字符串替换内容。这样做需要调用 HTML 解析器，因此效率低于直接操作节点。另一方面，由于它非常方便，Mozilla、Netscape 6 以及其他浏览器都实现了 `innerHTML`，尽管它是非标准的。

IE 4 DOM 还包含了相关的 `outerHTML` 属性（用于替换元素及其内容）以及 `insertAdjacentHTML()` 和 `insertAdjacentText()` 方法。这些在 IE 之外没有 `innerHTML` 常用。

## DOM 兼容性

如果你想编写在可用时使用 W3C DOM、在不可用时使用 IE 4 DOM 的脚本，可以使用能力测试方法，通过检查某个方法或属性是否存在来判断浏览器是否具有所需的功能。例如：

```
if (document.getElementById) {
  // 如果存在 W3C 方法，使用它
} else if (document.all) {
  // 如果存在 all[] 数组，使用它
} else {
  // 否则使用旧版 DOM
}
```

## DHTML：脚本化 CSS 样式

DHTML（动态 HTML）是 HTML、CSS 和 JavaScript 结合：它使用脚本动态修改文档元素的样式（可能包括位置和可见性）。在 W3C 和 IE 4 DOM 中，每个文档元素都有一个 `style` 属性，对应于指定内联样式的 HTML 属性。然而，`style` 属性指向的并不是简单的字符串，而是指向一个 `Style` 对象，该对象拥有与样式中每个 CSS 属性对应的属性。

例如，如果一个元素的样式属性指定了 CSS 颜色属性，你可以通过 `e.style.color` 查询该属性的值。当 CSS 属性名称包含连字符时，对应的 JavaScript 属性名称


移除连字符并使用混合大小写大写。因此，要设置元素的 `background-color` CSS 属性，你只需设置 `e.style.backgroundColor`。有一个特殊情况：CSS `float` 属性是 JavaScript 中的保留字，因此对应的 JavaScript 属性是 `cssFloat`。

CSS 标准定义了许多用于精细调整文档视觉外观的属性。参考部分中的 `Style` 条目包含一个列出所有属性的表格。定位和可见性属性对于动态脚本特别相关。如果将 `position` 设置为 `absolute`，你可以使用 `top` 和 `left` 属性来指定文档的绝对位置（以像素、百分比或其他单位）。同样，`width` 和 `height` 属性指定元素的大小。`visibility` 属性可以设置为 `hidden` 使文档元素不可见，然后动态设置为 `visible` 以在合适的时候显示元素。

请注意，所有 `Style` 属性的值始终都是字符串，即使是像 `left` 和 `width` 这样表示数字的属性。在设置这些长度和尺寸属性时，务必将数字转换为字符串并添加相应的单位说明（通常是像素的字符串 `px`）。下表总结了这些定位和可见性属性：

| 属性 | 描述/值 |
|:---|:---|
| position | 元素的定位方式。`absolute`, `relative`, `fixed` 或 `static`（默认值）。 |
| left, top | 元素左边缘和上边缘的 X 和 Y 坐标。 |
| width | 元素的宽度。 |
| height | 元素的高度。 |
| zIndex | 堆叠顺序。值为整数；值越高越在低值之上。 |
| display | 元素的显示方式。常见值为 `block`、`inline` 以及用于完全不布局的元素的 `none`。 |
| visibility | 元素是可见还是隐藏。非定位的隐藏元素仍会分配空间。 |
| overflow | 当元素内容超过元素大时的处理方式。值：`visible`（内容溢出）；`hidden`（隐藏超出内容）；`scroll`（可能显示滚动条）；`auto`（仅在需要时显示滚动条）。 |
| clip | 显示元素内容的哪个部分。语法：`rect (top right bottom left)`。 |

以下代码显示了一个简单的 HTML 动画。每次它将元素向右移动 10 像素，并使用 `setTimeout()` 通知 JavaScript 在 50 毫秒后再次调用它。调用 20 次后，该函数使用 `visibility` 属性隐藏元素并停止自调用。

```
<h1 id='title'>HTML Animation</h1>
<script>
// 查找要动画的元素
var e = document.getElementById("title");
// 使其可以定位
e.style.position = "absolute";
var frame = 0; // 初始化帧计数器。
// 此函数每次移动元素一帧
// 完成后将其隐藏。
function nextFrame() {
if (frame < 20) { // 只执行 20 帧
e.style.left = (10 * frame) + "px";
// 在 50ms 后再次调用我们。
settimeout("nextFrame()", 50);
} else e.style.visibility="hidden"; // 隐藏它。
}
nextFrame(); // 现在开始动画
</script>
```

## 事件与事件处理

我们在本节开头看到，将客户端  JavaScript 嵌入 HTML 文档的一种方法是使用 HTML 标签的事件处理器属性。下表列出了标准事件处理器属性及其可能应用的 HTML 标签。表格的第一列给出事件处理器属性名称：这些名称始终以 "on" 开头。表格的第二列列出了可以应用这些属性的 HTML 标签，并在必要时解释什么事件会触发处理器代码的执行。

| 处理器 | 支持者/触发条件 |
|:---|:---|
| onabort | \<img\>; 图像加载中断 |
| onblur | \<body\> 和表单元素；窗口失去焦点 |
| onchange | 表单元素；值改变 |
| onclick | 元素；点击 |
| ondblclick | 所有元素；双击 |
| onerror | \<img\>; 加载失败 |
| onfocus | \<body\> 和表单元素；窗口或元素获得焦点 |
| onkeydown | \<body\> 和表单元素；按下键 |
| onkeypress | \<body\> 和表单元素；按下并释放 |
| onkeyup | \<body\> 和表单元素；释放键 |
| onload | \<body\>, \<frameset\>, \<img\>, \<iframe\>, \<object\>; 加载 |
| onmousedown | 所有元素；按下鼠标 |
| onmove | 所有元素；鼠标移动 |
| onmouseout | 所有元素；鼠标移出 |
| onmouseover | 所有元素；鼠标悬停 |
| onmouseup | 所有元素；释放鼠标 |
| onreset | 所有元素；重置 |
| onresize | \<body\>, \<frameset\>; 大小改变 |
| onsubmit | \<form\>, \<frameset\>; 请求提交 |
| onunload | \<body\>, \<frameset\>; 文档卸载 |

## 作为函数的事件处理器

我们看到虽然事件处理器属性是以字符串形式写的，但对应的属性不是字符串，而是函数。你只需通过将函数赋值给相应的属性来创建新的事件处理器：

```
function validate() { // 函数
// 检查有效性
return true; // 返回 true 或 false
}
// 现在提交前检查用户输入
document.forms[0].onSubmit = validate;
```

## 高级事件处理

之前的章节描述了 JavaScript 的基础事件处理模型。也可以高级事件处理，但遗憾的是，有三种不兼容的模型：标准 W3C 模型、Internet Explorer 模型（微软未采用 W3C 标准）以及 Netscape 4 模型。

## 事件细节

在高级事件处理模型中，事件细节（如事件类型、鼠标键坐标、修饰键状态等）通过 Event 属性提供。在 W3C 和 Netscape 事件模型中，此 Event 对象作为参数传递给事件处理器。在 IE 模型中，Event 对象不是参数，而是存储在发生事件的 Window 上的。遗憾的是，三个高级事件模型使用不同的属性名称来存储事件细节，因此跨浏览器兼容性很难。请参见参考部分的 Event 以获取三种类型对象的文档。

## 事件传播

在基础事件模型中，事件处理器仅针对发生事件的文档元素触发。在高级模型中，事件可以沿着元素层次向上和/向下传播，并由一个或多个事件处理器处理。在 Netscape 和 W3C 模型中，事件从文档对象开始，向下通过文档树到达发生元素的元素。如果任何容器元素注册了特殊的捕获事件处理器，这些处理器将捕获事件并获得首次处理的机会。在 IE 和 W3C 模型中，某些类型的事件（如鼠标点击）在源处处理后会向上冒泡。

因此，你可能会在一个 <div> 对象上注册 onclick 事件处理器，以便处理发生在该 <div> 内部元素的所有鼠标点击。捕获、冒泡和


普通事件处理程序具有防止事件进一步传播的选项，尽管这种实现方式在每个模型中都是不同的。

## 事件处理程序注册

在 W3C 事件模型中，事件处理程序并非简单地赋值给文档对象的属性。相反，文档对象拥有一个 `addEventListener()` 方法，你通过调用该方法为特定类型的事件注册事件处理程序函数。这允许高级应用程序为同一个事件类型注册多个处理程序。

## JavaScript 安全限制

出于安全考虑，客户端 JavaScript 实现通常会对脚本可以执行的任务施加限制。最显而易见的限制是省略了危险的能力：例如，客户端 JavaScript 无法删除用户本地硬盘上的文件。此外还存在其他限制，以防止私有信息泄露或防止脚本骚扰用户。目前没有标准的安全限制集，但以下是典型浏览器实现中常见的限制。不要尝试编写执行这些操作的脚本：即使它们在你的浏览器中可以运行，在其他浏览器中也可能无法工作。

## 同源策略

脚本只能读取从同一 Web 服务器加载的窗口和文档的属性。这是对跨窗口脚本的一项重大且普遍的限制，防止脚本从用户正在查看的其他无关文档中读取信息。该限制还防止脚本在无关文档上注册事件处理程序或伪造事件。

## 文件上传

脚本无法设置 `FileUpload` 表单元素的 `value` 属性。

发送邮件和发布新闻
在没有用户确认的情况下，脚本无法将表单提交到 `mailto:` 或 `news:` URL。

关闭窗口
脚本只能关闭其自己创建的浏览器窗口，除非获得用户确认。

嗅探缓存
脚本不能加载任何 `about:` URL，例如 `about:cache`。

隐藏窗口和窗口装饰
脚本不能创建微小的、离屏的窗口，或没有标题栏的窗口。

请注意，这个安全限制列表并不是静态的。随着 JavaScript 使用的增长，广告商和不法分子已开始利用它做一些骚人的事情。因此，较新的浏览器（如 Mozilla 1.0）允许用户可配置的限制，可以防止脚本打开新窗口（如弹出窗口广告），或移动或调整现有窗口的大小。

## JavaScript API 参考



本书的其余部分包含了核心和客户端 JavaScript API 的快速参考。它涵盖了遗留的（Level 0）DOM API，并展示了 W3C Level 2 DOM API 的简化视图。省略了与处理 HTML 文档的 JavaScript 程序无关 API 部分。每个参考条目标题块的右上角包含信息，说明该功能是核心 API 还是客户端 API 的，并进一步指示了哪个版本的 JavaScript、哪个浏览器或哪个版本的 DOM 引入了该功能。

由于 JavaScript 是一种弱类型语言，因此 JavaScript API 的类和对象没有官方类名集，它们有时在不同的参考书中以不同的名称出现。（为了简洁起见，本书实际使用的名称集与它的“大哥”《JavaScript: The Definitive Guide》略有不同）。下表总结了后续的条目，并允许你快速查找你感兴趣的类或对象。

| | |
| --- | --- |
| Anchor | 文档中的具名位置 |
| Applet | Java Applet |
| Arguments | 函数的参数 |
| Array | 数组的创建与操作 |
| Attr | 文档元素的属性 |
| Boolean | 布尔值的包装对象 |
| Comment | HTML 注释 |
| DOMException | 信号 DOM 错误的异常 |
| DOMImplementation | 创建文档，检查 DOM 特性 |
| Date | 操作日期和时间 |
| Document | HTML 文档 |
| DocumentFragment | 共同操作的节点 |
| Element | 文档中的 HTML 标签 |
| Error | 预定义的异常类型 |
| Event | 事件详情 |
| Form | HTML 输入表单 |
| Function | JavaScript 函数 |
| Global | 全局属性和函数 |
| History | 浏览历史 |
| Image | HTML 图像 |
| Input | 表单输入元素 |
| Layer | 独立的文档层 |
| Link | `<a>` 或 `<area>` 链接 |
| Location | 当前浏览器位置 |
| Math | 数学函数和常量 |
| Navigator | 关于浏览器的信息 |
| Node | 文档树中的节点 |
| Number | 对数字的支持 |
| Object | 所有 JavaScript 对象的父类 |
| Option | 可选选项 |

### Anchor

RegExp
| 用于模式匹配的正则表达式
Screen
| 关于显示的信息
Select
| 图形化选择列表
String
| 字符串操作
Style
| 元素的内联 CSS 属性
Text
| 文档中的一段文本
Textarea
| 多行文本输入
Window
| 浏览器窗口或框架

### Anchor
客户端 JavaScript 1.2

文档中的具名位置
继承自：Element

## 摘要

```
document.anchors[index]
document.anchors[name]
```

## 描述

Anchor 对象表示带有 `name` 属性的 `<a>` 标签，用于在文档中创建具名位置。

## 属性

name
<a> 标签的 `name` 属性的值。

## 参见

document.anchors[ ], Link, Location.hash

### Applet
客户端 JavaScript 1.1

一个 Java Applet

## 摘要

```
document.applets[i]
document.applets[appletName]
document.appletName
```

### 属性与方法

Applet 对象的属性和方法与其代表的 applet 的公共字段和方法相同。

### 参数
核心 JavaScript 1.1; JavaScript 2.0; ECMA v1

函数的参数

## 摘要

```
arguments[n]
arguments.length
```

## 描述

Arguments 对象仅定义在函数体内，在每个函数体内部，局部变量 `arguments` 指向该对象。Arguments 对象是一个数组，其元素是传递给函数的值。元素 0 是第一个参数，元素 1 是第二个参数，依此类推。无论函数声明中是否命名，所有传递的值都会成为 Arguments 对象的元素。

## 属性

- callee
指向当前执行的函数的引用。用于匿名函数的递归。JS 1.2; JavaScript 5.5; ECMA v1；仅定义在函数体内。

- length
传递的参数数量。JS 1.1; JavaScript 2; ECMA v1。

## 参见

Function

### Array 核心 JavaScript 1.1; JavaScript 2.0; ECMA v1

数组的创建与操作

## 构造函数

- new Array() // 空
- new Array(n) // n 个空元素
- new Array(e0, e1,...) // 指定元素

## 字面量语法

在 JavaScript 1.2、JavaScript 3.0 和 ECMA v3 中，你可以通过在方括号放置逗号分隔的表达式列表来创建并初始化数组。这些表达式的值成为数组的元素。例如：

```
var a = [1, true, 'abc'];
var b = [a[0]*2, f(x)];
```

## 属性

- length 一个可读写的整数，指定数组中元素的数量；或者，当数组元素不连续时，等于数组最后一个元素的索引加一。更改此属性的值会截断或扩展数组。

## 方法

- concat(value, ...) 返回一个新数组，通过将每个指定的参数合并到当前数组形成。如果 concat() 的任何参数本身是数组，则合并的是它们的元素，而不是数组本身。JS 1.2; JavaScript 3.0; ECMA v3。
- join(separator) 返回将数组的每个元素转换为字符串并连接在一起的字符串，元素之间使用分隔符字符串。
- pop() 并返回数组的最后一个元素，递减数组长度。JS 1.2; JavaScript 5.5; ECMA v3.





push(value, ...)
将指定的值或多个值添加到数组的末尾，并返回数组的新长度。JS 1.2; JavaScript 5.5; ECMA v3.

reverse()
反转数组元素的顺序。不返回任何。

shift()
删除并返回数组的第一个元素，将后续元素向下移动一位，并减少数组长度。JS 1.2; JavaScript 5.5; ECMA v3.

slice(start, end)
返回一个新数组，其中包含从编号为 `start` 的元素到（但不包含）编号为 `end` 的元素。JS 1.2; JavaScript 3.0; ECMA v3.

sort(orderfunc)
对数组元素进行排序，并返回数组的引用。注意数组是在原地进行排序的，不会创建副本。可选的 `orderfunc` 参数可以指定一个定义排序的函数。该函数应接受两个参数，并且如果第一个参数小于第二个参数，则返回一个小于 0 的值；如果它们相等，则返回 0；如果第一个大于第二个，则返回一个大于 0 的值。

splice(start, deleteCount, value,...)
从指定的索引开始从数组删除指定数量的元素，然后将任何剩余参数插入数组的该位置。返回一个包含已删除元素的数组。JS 1.2; JavaScript 5.5; ECMA v3.

toLocaleString()
返回数组的本地化字符串表示。JS 1.5; JavaScript 5.5; ECMA v1.

toString()
返回数组的字符串表示。

unshift(value, ...)
将参数或多个参数作为新元素插入数组开头，将现有的数组元素向上移动以留空间。返回数组的新长度。JS 1.2; JS 5.5; ECMA v3.

### Attr

文档元素的一个属性
继承自：Node

### Properties

name
属性的名称。只读。

ownerElement
包含此属性的 Element 对象。只读。
DOM Level 2.

specified
如果属性在文档源中显式指定或通过脚本设置，则为 true；否则为 false。只读。

value
作为字符串的属性值。可读/写。

### See Also

Document.createAttribute(), Element.getAttributeNode(),
Element.setAttribute()

### Boolean

布尔值的包装对象

### Constructor

new Boolean(value)
Boolean(value)

作为函数调用时（不使用 `new` 运算符），`Boolean()` 将值转换为布尔值（而不是 Boolean 对象）并返回它。除了 0、NaN、null、undefined 和空字符串 "" 之外，所有值都转换为 true。当使用 `new` 运算符调用时，`Boolean()` 构造函数执行相同的转换并将结果封装在 Boolean 对象中。

### Methods

toString()
返回 "true" 或 "false"，取决于 Boolean 对象的值。

valueOf()
返回由 Boolean 对象封装的原始布尔值。

### Comment

HTML 注释
继承自：Node

### Properties

Comment 节点的属性与 Text 节点完全相同。

### Methods

Comment 节点支持 Text 节点的所有方法，但 `splitText()`。

### See Also

Text

### DOMException

信号 DOM 错误

### Properties

code
提供有关异常原因详细信息的错误代码。此属性的一些可能值（及其含义）由下面列出的常量定义。

### Constants

以下常量定义了处理 HTML 文档时可能遇到的代码值。注意，这些常量是 DOMException 的静态属性，而不是单个异常对象的属性。

DOMException.INDEX_SIZE_ERR = 1
数组或字符串索引越界错误。

DOMException.HIERARCHY_REQUEST_ERR = 3
尝试将节点放置在文档树层次结构中的非法位置。

DOMException.WRONG_DOCUMENT_ERR = 4
尝试使用与创建该节点的文档以外的节点。

DOMException.INVALID_CHARACTER_ERR = 5
使用了非法字符（例如，在元素名中）。

DOMException.NOT_FOUND_ERR = 8
在预期位置未找到节点。

DOMException.NOT_SUPPORTED_ERR = 9
当前 DOM 实现不支持该方法或属性。

DOMException.INUSE_ATTRIBUTE_ERR = 10
尝试将一个 Attr 关联到 Element，而该 Attr 节点已与另一个 Element 节点关联。

DOMException.SYNTAX_ERR = 12
发生了语法错误，例如在 CSS 属性规范中。

### DOMImplementation

创建文档，检查 DOM 特性

### Synopsis

```
document.implementation
```

### Methods

```
createHTMLDocument(title)
创建并返回一个新的 HTML Document 对象，并用 <html>、<head><title> 和 <body> 元素填充。title 是出现在 <title> 元素中的文本。
DOM Level 2.
```

```javascript
hasFeature(feature, version)
如果实现支持指定特征的版本，则返回 true，否则返回 false。如果没有指定版本号，如果实现完全支持指定特征的任何版本，则返回 true。feature 和 version 都是字符串；例如 "core""1.0" 或 "2.0"。
```

### Date

Core JavaScript 1.0; JavaScript 1.0; ECMA v1
处理日期和时间

### Constructor

```javascript
new Date()
```
返回当前时间。

```javascript
new Date(value)
```
返回指定的日期。

```javascript
new Date(year, month)
返回指定的月份。

```javascript
new Date(year, month, day)
返回指定的日期。

```javascript
new Date(year, month, day, hours)
返回指定的时间。

```javascript
new Date(year, month, day, hours, minutes)
返回指定的时间。

```javascript
new Date(year, month, day, hours, minutes, seconds)
返回指定的时间。

```javascript
new Date(year, month, day, hours, minutes, seconds, milliseconds)
返回指定的时间。

```javascript
new Date(timestamp)
```
返回自 Unix 纪元来的毫秒数。

### Methods

```javascript
getFullYear()
```
返回年份。

```javascript
getMonth()
```
返回月份。

```javascript
getDate()
```
返回日期。

```javascript
getHours()
```
返回小时。

```javascript
getMinutes()
```
返回分钟。

```javascript
getSeconds()
```
返回秒。

```javascript
getMilliseconds()
```
返回毫秒。

```javascript
getTime()
```
返回自 Unix 纪元来的毫秒数。

```javascript
getUTCFullYear()
```
返回 UTC 年份。

```javascript
getUTCMonth()
```
返回 UTC 月。

```javascript
getUTCDate()
```
返回 UTC 日。

```javascript
getUTCHours()
```
返回 UTC 小时。

```javascript
getUTCMinutes()
```
返回 UTC 分钟。

```javascript
getUTCSeconds()
```
返回 UTC 秒。

```javascript
getUTCMilliseconds()
```
返回 UTC 毫秒。

```javascript
setFullYear(year)
```
设置年份。

```javascript
setMonth(month)
```
设置月份。

```javascript
setDate(day)
```
设置日期。

```javascript
setHours(hours)
```
设置小时。

```javascript
setMinutes(minutes)
```
设置分钟。

```javascript
setSeconds(seconds)
```
设置秒。

```javascript
setMilliseconds(milliseconds)
```
设置毫秒。

```javascript
setTime(timestamp)
```
设置自 Unix 纪元来的毫秒数。

```javascript
setUTCFullYear(year)
```
设置 UTC 年份。

```javascript
setUTCMonth(month)
```
设置 UTC 月。

```javascript
setUTCDate(day)
```
设置 UTC 日。

```javascript
setUTCHours(hours)
```
设置 UTC 小时。

```javascript
setUTCMinutes(minutes)
```
设置 UTC 分钟。

```javascript
setUTCSeconds(seconds)
```
设置 UTC 秒。

```javascript
setUTCMilliseconds(milliseconds)
```
设置 UTC 毫秒。

```javascript
toString()
```
返回 Date 对象的字符串表示。

```javascript
toLocaleDateString()
```
返回 Date 对象的日期部分的本地化字符串。

```javascript
toLocaleTimeString()
```
返回 Date 对象的时间部分的本地化字符串。

```javascript
toJSON()
```
返回 Date 对象的 JSON 字符串表示，等同于调用 `toISOString()`。





### set[UTC]Seconds(seconds, millis)

使用本地时间或通用时间设置日期的秒字段（以及可选的毫秒字段）。返回调整后日期的毫秒-秒表示形式。

### setTime(milliseconds)

设置内部的毫秒级表示形式。返回毫秒参数。

### setYear(year)

设置 2 位年份字段。已弃用，改用 set[UTC]FullYear() 替代。

### toDateString()

返回一个表示日期部分的字符串，并用本地时区表示。JS 1.5; JavaScript 5.5; ECMA v3。

### toGMTString()

使用 GMT 时区将 Date 转换为字符串并返回该字符串。已弃用，改用 toUTCString() 替代。

### toLocaleDateString()

返回一个表示日期部分的字符串，使用本地日期格式规范，并用本地时区表示。JS 1.5; JavaScript 5.5; ECMA v3。

### toLocaleString()

使用本地时区和本地日期格式规范将 Date 转换为字符串。

### toLocaleTimeString()

返回一个表示日期时间部分的字符串，使用本地时间格式规范，并用本地时区表示。JS 1.5; JavaScript 5.5; ECMA v3。

### toString()

返回一个使用本地时区表示日期的字符串表示。

### getTime()

返回一个表示时间部分的字符串，并用本地时区表示。JS 1.5; JavaScript 5.5; ECMA v3。

### toUTCString()

使用通用时间将 Date 转换为字符串并返回该字符串。JS 1.2; JavaScript 3.0; ECMA v1。

valueOf() 返回日期的毫秒表示形式，与 getTime() 完全一致。JS 1.1; ECMA v1。

## 静态方法

除了之前列出的实例方法外，Date 对象定义了两个静态方法。这些方法通过 Date() 构造函数本身调用，而不是通过具体的 Date 对象：

Date.parse(date)

解析日期和时间的字符串表示并返回日期的内部毫秒表示形式。

Date.UTC(yr, mon, day, hr, min, sec, ms)

返回指定的 UTC 日期和时间的毫秒表示形式。

### 文档

客户端 JavaScript 1.0; DOM  级

一个 HTML 文档 继承自：Node（在 DOM 1级中）

## 概要

window.document document

## 描述

Document 对象表示一个 HTML 文档，是客户端 JavaScript 中最重要的对象之一。它引入于 JavaScript 1.0，并在 JavaScript 1.1 中增加了许多方法和属性。Netscape 和 Internet Explorer 分别为 Document 对象增加了非标准方法和属性，而 W3C DOM 标准规范了额外的属性和方法。

## 属性

Document 对象的所有实现都支持以下属性。此列表之后是 W3C DOM Document 对象定义的属性列表，以及 IE 4 和 Netscape 4 Document 对象定义的属性列表。

- 一个指定激活链接颜色的字符串。已弃用。

- anchors[]
一个 Anchor 对象的数组，文档中出现的每个锚点对应一个对象。JS 1.2。

- applets[]
一个 Applet 对象的数组，文档中出现的每个 applet 对应一个对象。JS 1.1。

- bgColor
一个指定文档背景色的字符串。已弃用。

- cookie
一个具有特殊行为的字符串值属性，允许查询和设置与此文档相关的 cookie。

- domain
一个指定文档所属 Internet 域名的字符串。用于安全目的。JS 1.1。

- embeds[]
表示通过 <embed> 标签嵌入文档的数据的对象数组。plugins[] 的同义词。某些插件和 ActiveX 可以使用 JavaScript 进行控制。API 取决于具体的控件。JS 1.2

- fgColor
一个指定文档默认文本颜色的字符串。已弃用。

- forms[]
一个 Form 对象的数组，文档中出现的每个 HTML 表单对应一个对象。

- images[]
一个 Image 对象的数组，文档中通过 HTML <img> 标签嵌入的每张图像对应一个对象。JS 1.1。

- lastModified
一个只读字符串，指定文档最近一次更改的日期（由网络服务器报告）。JS 1.0。

- linkColor
一个指定未访问链接颜色的字符串。已弃用。

- links[]
一个 Link 对象的数组，文档中出现的每个超文本链接对应一个对象。

- location
文档的 URL。已弃用，改用 URL 属性替代。

- plugins[]
embeds[] 数组的同义词。JS 1.1。

- referrer
一个只读字符串，包含链接到当前文档的文档 URL（如果有的话）。

- title
<title> 标签的文本内容。在 DOM 1级之前是只读的。

- URL
一个指定文档 URL 的只读字符串。JS 1.1。

- vlinkColor
一个指定已访问链接颜色的字符串。已弃用。

### W3C DOM 属性

在符合 DOM 的浏览器中，Document 对象继承了 Node 的属性，并定义了以下额外属性。

- body
指向代表文档 <body> 标签的 Element 对象引用。

- defaultView
显示文档的 Window。只读。DOM 2级。

- documentElement
指向 <html> 标签的只读引用。

- implementation
表示文档的实现对象。

## IE 4 属性

由 Internet Explorer 定义的非标准（可移植）属性：

- activeElement
指向当前活动元素的只读引用。

- all[]
文档中所有元素的数组。

- charset
文档的字符集。

- children[]
文档的直接子元素数组。

- defaultCharset
文档的默认字符集。

- readyState
指定文档的加载状态。

- loading
文档正在加载。

- interactive
文档已加载，可以交互。

- complete
文档已完全加载。

- height
文档的高度（像素）。

- layers[]
表示文档内部图层的数组。该属性仅适用于 Netscape 6。

- parentWindow
包含文档的窗口。

- uninitialized
文档尚未加载。

- width
文档的宽度（像素）。

### 普通方法

Document 对象的所有实现都支持以下方法。此列表之后是标准以及 Netscape 4 Document 对象定义的方法列表。

- clear()
清除文档内容并返回。该方法在 JavaScript 1.1 中已弃用。

- close()
关闭通过 open() 打开的流并返回。JS 1.0。

- open()
删除现有文档内容并打开可以写入新文档内容的流。返回。JS 1.0。

- write(value, ...)
将指定的字符串或字符串插入当前正在解析的文档，或追加到通过 open() 打开的文档。返回。JS 1.0。

- writ(value, ...)
与 write() 相同，但在输出末尾添加一个换行符。返回。JS 1.0。

### W3C DOM 方法

在符合 DOM 的浏览器中，Document 对象继承了 Node 方法，并定义了以下额外方法。

- createAttribute(name)
返回一个新创建的指定名称属性。

- createComment(text)
创建并返回一个包含指定文本的 Comment节点。

- createDocumentFragment()
创建并返回一个空的 DocumentFragment 节点。

- createElement(tagName)
创建并返回一个指定标签名的 Element 节点。

- createTextNode(text)
创建并返回一个包含指定文本的 Text节点。

- getElementById(id)
返回其 id 属性具有指定值的 Element；如果文档中不存在该 Element，则返回 null。

- getElementsByName(name)
返回文档中所有 name 属性具有指定值的元素的节点数组。如果没有找到这些元素，则返回一个空数组。





### getElementsByTagName(tagName)

返回此文档中所有具有指定标签名的 Element 节点数组。这些 Element 节点在返回数组中的顺序与它们在文档源代码中出现的顺序相同。

### importNode(importedNode, deep)

创建并返回来自其他文档的节点副本，该副本适用于插入到此文档中。如果 deep 参数为 true，则会递归地复制该节点的子节点。DOM Level 2。

### Netscape 4 方法

### getSelection()

返回当前选中的文档文本，并移除 HTML 标签。

### IE 4 方法

### elementFromPoint(x,y)

返回位于指定点的 Element。

### 事件处理器 (Handlers)

在符合 DOM 标准的浏览器和 IE 4 中，Document 对象支持与 Element 对象相同的通用事件处理器列表。虽然 `onload` 和 `onunload` 处理器在逻辑上属于 Document 对象，但它们是被实现为 Window 对象的属性的。

### 另请

Anchor, Applet, Element, Form, Image, Layer, Link, Window

### DocumentFragment (文档片段)

### DOM Level 1

需要一起操作的节点

继承自：Node

## 描述

DocumentFragment 继承了 Node 的方法和属性，本身没有定义任何新的方法或属性。然而，它具有重要的行为：当一个 DocumentFragment 被插入文档树时，插入的不是 DocumentFragment 节点本身，而是它的子节点。这使得 DocumentFragment 可以作为临时占位符，用于一次性插入到文档中的节点。

### 另请

Document.createDocumentFragment()

### Element DOM Level 1, IE 4

文档中的 HTML 标签

继承自：Node (在 DOM Level 1 中)

## 描述

Element 对象代表 HTML 元素或标签。IE 4 及后续版本、符合 DOM 标准的浏览器（如 IE 5 及后续）以及 Netscape 6 及后续允许访问文档的每个元素。它们在这些元素上定义了此处列出的属性和方法。遗憾的是，IE 4 DOM 定义的方法和属性与 W3C DOM 标准定义的方法和属性并不相同。由于这种不兼容性，它们在后续列表中被分组成。

### W3C DOM 属性

在支持 W3C DOM 的网页浏览器中，HTML 文档中的所有元素都具有与其 HTML 属性对应的属性，包括如 dir、id、lang 和 title 等通用属性。当 HTML 属性名由多个单词组成时，对应的 JavaScript 属性使用小写。否则如此（例如 id 和 href，tagName 和 accessKey）。有两个 HTML 属性名称是 JavaScript 或 Java 中的保留字，需要特殊的属性名。JavaScript 使用属性 `className` 来引用所有 HTML 标签的 class 属性，并使用 `htmlFor` 来引用 `<label>` 和 `<script>` 标签的 for 属性。除了 HTML 属性外，所有元素都定义了以下属性。同时记住，在符合 DOM 标准的浏览器中，所有 HTML 元素继承 Node 对象的属性。

### className

元素的类属性的字符串值，指定一个或多个 CSS 类。注意，该属性未名为 "class"，因为该名称是 JavaScript 中的保留字。

### style

一个代表 HTML 元素样式属性的 Style 对象。

### tagName

元素的只读标签名。对于 HTML 文档，无论文档源代码中的大小写如何，返回的标签名均为大写。�。在 XHTML 文档中，值为小写。

### IE DOM 属性

Internet Explorer 4 及后续版本定义了私有的 DOM。在 IE 4 DOM 中，与 W3C DOM 一样，每个 HTML 元素都有与其 HTML 属性对应的 JavaScript 属性。此外，IE 4 DOM 为每个元素定义了以下属性：

### all[]

包含此元素的所有后代 Element 对象的数组。此数组可以通过数字索引按源顺序访问元素。或者也可以通过元素 id 或 name 进行索引。另请 Document.all()。

### children[]

包含此元素直接子节点的 Element 对象的数组。注意，IE 4 DOM 没有等于 Text 或 Comment 的节点，因此元素的子节点只能是 Element 对象。

### className

一个可读可写的字符串，用于指定元素类属性的值。

### document

指向包含它的 Document 对象的引用。

### innerHTML

元素内部的 HTML 文本，不包括元素本身的起始和结束标签。设置此属性将替换元素的内容。由于此非标准属性强大且广泛使用，包括 Netscape 6 及后续版本和 Mozilla 在内的其他浏览器已实现它。

### innerText

元素内部的纯文本，不包括元素本身的起始和结束标签。设置此属性会将元素的内容替换为未解析的纯文本。

### offsetHeight

元素及其所有内容的高度（像素为单位）。

### offsetLeft

元素相对于 offsetParent 容器元素的 X 坐标。

### offsetParent

指定定义测量 offsetLeft 和 offsetTop 所在坐标系的容器元素。对于大多数元素，offsetParent 是包含它们的 Document 对象。然而，如果一个元素具有动态定位的祖先，则该祖先就是 offsetParent。表格单元格是相对于它们所在的行进行定位的。

### offsetTop

元素相对于 offsetParent 容器元素的 Y 坐标。

### offsetWidth

元素及其所有内容的宽度（像素为单位）。

### outerHTML

元素的 HTML 文本，包括其起始标签、结束标签和内容。设置此属性将替换该元素及其内容。

### outerText

元素的纯文本，包括其起始和结束标签。设置此属性将替换元素及其内容。

### sourceIndex

元素在文档中的索引。

### style

代表此元素内联样式的 Style 对象。设置此对象会更改元素的显示。

### tagName

指定标签名的只读字符串。

### W3C DOM 方法

在支持 W3C DOM 的网页浏览器中，HTML 文档中的所有元素都支持以下方法，并继承 Node 的方法。许多这些方法用于获取和设置属性值，但很少使用，因为 Element 对象拥有镜像所有 HTML 属性的属性。

getAttribute(name)

返回命名属性的字符串值。

getAttributeNode(name)

返回命名属性的 Attr 节点。

getElementsTagName(name)

返回此元素中所有具有指定名称的数组，按它们在文档中出现的顺序排列。

hasAttribute(name)

如果元素具有指定的属性，则返回 true，否则返回 false。

removeAttribute(name)

从元素中删除指定的属性及其值，无返回。

removeAttribute(oldAttr)

从元素的属性列表中移除指定的 Attr 节点。返回被移除的 Attr 节点。

setAttribute(name, value)

将命名属性设置为指定的字符串值，无返回。

setAttributeNode(newAttr)

将指定的 Attr 节点添加到元素的列表中。如果存在同名属性，则替换其值。返回被 newAttr 替换的 Attr 节点，如果没有属性被替换则返回 null。

### IE DOM 方法

Internet Explorer 4 及后续版本为所有文档元素支持以下非标准方法。

contains(target)

如果此元素包含 Element target，则返回 true，否则返回 false。

getAttribute(name)

返回元素命名属性的字符串值，如果没有此类属性则返回 null。

insertAdjacentHTML(where, text)

在元素附近的根据 where 指定的位置插入 HTML 文本。where 必须是 "BeforeBegin","AfterBegin","BeforeEnd" 或 "AfterEnd" 字符串之一。无返回。

insertAdjacentText(where, text)

在元素附近的根据 where 指定的位置插入纯文本。无返回。

removeAttribute(name)

从元素中删除命名属性及其值。成功返回 true；失败返回 false。

scrollToView(top)

滚动文档使此元素在窗口的顶部或底部可见。如果 top 为 true 或省略，元素出现在窗口顶部。如果为 false，元素出现在窗口底部。





setAttribute(name, value)
将命名的属性设置为指定的字符串值且不返回任何内容。

## 事件处理器

HTML 文档的元素定义了以下事件处理器，以响应鼠标和键盘事件。元素类型（例如 Form 和 Input 对象）可能会定义更专门的事件处理器（如 onSubmit 和 onchange），这些处理器会对原始输入事件施加特定的解释。

- onclick
当用户点击元素时触发。
- ondblclick
当用户双击元素时触发。
- onhelp
当用户请求帮助时触发。仅限 IE 。
- keydown
当用户按下按键时触发。
- keypress
当用户按下并释放按键时触发。
- keyup
当用户释放按键时触发。
- onmousedown
当用户按下鼠标键时触发。
- onmousemove
当用户移动鼠标时触发。
- onmouseout
当用户将鼠标移出元素范围时触发。
- onmouseover
当用户将鼠标悬停在元素上时触触发。
- onmouseup
当用户松开鼠标键时触发。

### 另参

Form, Input, Node, Select, Textarea

### 错误

核心 JavaScript 1.5; JavaScript 5.5; ECMA v3
继承自: Object

预定义异常类型

## 构造函数

- new Error(message)
new EvalError(message)
new RangeError(message)
new ReferenceError(message)
new SyntaxError(message)
new TypeError(message)
new URIError(message)

这些构造函数创建 Error 类或其一个子类的实例。message 参数是可选的。

## 属性

Error 及其所有子类定义了相同的两个属性：

message
一个提供异常详细信息的错误对象。该属性持有传递给构造函数的字符串，或由实现定义的默认字符串。

name
一个指定异常类型的字符串。该属性始终是用于创建异常对象的构造函数的名称。

## 方法

toString()
返回 Error（或其子类）对象的字符串表示。

### 事件

DOM Level 2, IE 4, Netscape 4

事件详情

## 描述

Event 对象用于提供有关事件的详细信息以及对事件的传播进行控制。DOM Level 2 定义了一个标准的 Event 对象，但 Internet Explorer 4, 5 和 6 使用的是私有对象。Netscape 4 有它自己不同于另外两个私有对象。DOM Level 2 尚未标准化键盘事件，因此对于对 Netscape 6 及更高版本的键事件感兴趣的程序员，Netscape 4 Event 对象可能仍然有用。DOM、IE 和 Netscape 4 对象的属性在不同的章节列出。

在 DOM 和 Netscape 事件模型中，Event 对象作为参数传递给事件处理器。在 IE 事件模型中，描述最近事件的 Event 对象则存储在 Window 对象的 event 属性中。

### DOM 常量

这些常量是 eventPhase 属性的合法值；它们代表此事件事件传播的当前阶段。

```
Event.CAPTURING_PHASE = 1
事件处于捕获阶段。
```

```
Event.AT_TARGET = 2
事件正在由其目标节点处理。
```

```
Event.BUBLING_PHASE = 3
事件正在冒泡。
```

### DOM 属性

此对象的所有属性都是只读的。

altkey
如果事件发生时按下了 Alt 键，则为 true。
定义用于鼠标事件。

bubbles
如果事件属于可以冒泡的类型，则为 true；否则为 false。
定义用于所有事件。

button
指定在 mousedown、mouseup 或 click 事件期间哪个鼠标键的状态发生了变化。0 表示左键，1 表示中间键，2 表示右键。注意，此属性仅在按钮状态改变时定义：例如，它不用于报告在 mousemove 事件期间某个按钮是否被按住。此外，此属性不是位图：它无法告诉你是否有一个多个按键被按住。Netscape 6.0 使用值 1, 2 和 3 代替 0, 1 和 2。这在 Netscape 6.1 中已修复。

cancelable
如果与事件关联默认操作可以通过 preventDefault() 取消，则为 true；否则为 false。定义用于所有事件。

clientX, clientY
这些属性指定了鼠标指针相对于浏览器窗口客户端区域的 X 和 Y 坐标。注意，这些坐标没有考虑文档滚动。定义用于鼠标事件。

ctrlKey
如果事件发生时按下了 Ctrl 键，则为 true。定义用于鼠标事件。

currentTarget
当前正在处理此事件的文档节点。在捕获和冒泡期间，这与 target 不同。定义用于所有事件。

detail
点击次数：1 表示单击，2 表示双击，3 表示三击，依此类推。定义用于 click、mousedown 和 mouseup 事件。

eventPhase
事件传播的当前阶段。上述常量定义了该属性的三个合法值。定义用于所有事件。

metaKey
如果事件发生时按下了 Meta 键，则为 true。定义用于鼠标事件。

currentTarget
（对于 mouseover 事件，这是鼠标在移动过目标时离开的文档节点。对于 mouseout 事件，这是鼠标进入的节点。）
这些属性指定了鼠标指针相对于用户屏幕左上角的 X 和 Y 坐标。定义用于鼠标事件。

shiftKey
如果事件发生时按下了 Shift 键，则为 true。定义用于鼠标事件。

target
此事件的目标；生成事件的文档节点。注意这可以是任何节点，包括文本节点。定义用于所有事件。

timeStamp
一个指定事件发生日期和时间的 Date 对象。定义用于所有事件，但实现并不要求提供有效时间。

type
发生的事件类型。这是去掉了前缀 "on" 的事件名称。例如，“click""load" 或 "mousedown"。定义用于所有事件。

view
生成事件的 Window 对象。

### DOM 方法

preventDefault()
告诉浏览器不要执行此事件关联的默认操作（如果有）。如果事件不是可取消的类型，此方法无效。不返回内容。

stopPropagation()
停止事件在捕获、目标或冒泡阶段进一步传播。不返回内容。

## IE 4 属性

altKey
指定事件发生时是否按下了 Alt 键的布尔值。

button
对于鼠标事件，button 指定了按下了哪些鼠标键。此只读整数是一个位掩罩：1 位被设置表示左键被按下；2 位被设置表示右键被按下；4 位被设置表示中间键（对于三键鼠标）被按下。

cancelBubble
如果事件处理器想阻止事件传播到包含它的对象，它必须将此属性设置为 true。

clientX, clientY
相对于 Web 浏览器页面事件发生的 X 和 Y 坐标。

ctrlKey
指定事件发生时是否按下了 Ctrl 键的布尔值。

fromElement
对于 mouseover 和 mouseout 事件，fromElement 指向鼠标指针移动的对象。

keyCode
对于键盘事件，keyCode 指定了击中按键生成的 Unicode 字符。

offsetX, offsetY
事件在源元素（见 srcElement）的坐标系内发生的 X 和 Y 坐标。

returnValue
如果设置了此属性，其值将优先于事件处理器实际返回的值。将此属性设置为 false 以取消事件发生时源元素的默认操作。




相对于屏幕的事件 X 和 Y 坐标。

shiftKey
布尔值，指定事件发生时是否按下了 Shift 键。

srcElement
产生事件的 Window、Document 或 Element 对象。

toElement
对于 `mouseover` 和 `mouseout` 事件，`toElement` 指鼠标指针正在移动的对象。

type
指定 Event 类型的字符串属性。其值是事件处理程序的名称，去掉 "on" 前缀。因此，当调用 `onclick()` 事件处理程序时，Event 对象的 `type` 属性为 "click"。

x, y
事件发生的 X 和 Y 坐标。这些属性指定了相对于使用 CSS 动态定位的最内层元素的坐标。

## Netscape 4 属性

height
仅在 `resize` 事件中设置。指定调整大小的窗口或帧的新高度。

layerX, layerY
指定事件发生相对于所在层的 X 和 Y 坐标。

modifiers
指定事件发生时按下了哪些键盘修饰键。此数值是一个位掩码，由常量 `Event.ALT_MASK`、`Event.CONTROL_MASK`、`Event.META_MASK` 或 `Event.SHIFT_MASK` 中的任何一个组成。由于 Bug，此属性在 Netscape 6 或 6.1 中未定义。

相对于 浏览器页面的事件 X 和 Y 坐标。注意这些坐标是相对于顶层页面的，而不是任何嵌套层。

相对于屏幕的事件 X 和 Y 坐标。

发生事件的 Window、Document、Layer 或 Element 对象。

指定事件类型的字符串属性。其值是事件处理程序的名称，去掉 "on" 前缀。因此，当调用 `onclick()` 事件处理程序时，Event 对象的 `type` 属性为 "click"。

对于键盘和鼠标事件，指定按下或释放了哪个键或鼠标按钮。对于键盘事件，此属性包含所按键的字符编码。对于鼠标事件，它包含 1、2 或 3，表示左键、中键或右键。

仅在 `resize` 事件中设置。指定调整大小的窗口或帧的新宽度。

事件发生的 X 和 Y 坐标。这些属性是 `layerX` 和 `layerY` 的同义词，指定相对于包含层（如果有）的位置。

### Form

客户端 JavaScript 1.0

一个 HTML 输入表单

继承自：Element

### 提要

```
document.forms[form_number]
document.forms[form_name]
document.form_name
```

## 属性

Form 对象为 HTML <form> 元素的每个属性定义属性，例如 `action`、`encoding`、`method`、`name` 和 `target`。此外，它定义了以下属性：

elements[]
只读 Input 对象数组，表示表单中出现的元素。数组可以通过数字索引，或者对于定义了 HTML `name` 属性的元素通过元素索引。

length
表单中的元素数量。等于 `elements.length`。

## 方法

reset()
将表单的每个输入元素重置为默认值。无。JS 1.1。

submit()
提交表单，但不会触发 `onsubmit` 事件处理程序。无。

## 事件处理程序

onreset
在表单元素重置之前调用。返回 `false` 可阻止重置。

onsubmit
在表单提交之前调用。此事件处理程序允许在提交之前对表单输入进行验证。返回 `false` 可阻止提交。

## 参见

Element, Input, Select, Textarea

### Function

核心 JavaScript 1.0; JavaScript 1.0; ECMA v1

一个 JavaScript 函数

## 构造函数

new Function(argument_names..., body)

此构造函数在 JavaScript 1.1 中引入，已被 JavaScript 1.2 的函数字面量语法废弃。

## 属性

length
声明函数时指定的具名参数数量。实际传递参数的数量参见 `Arguments.length`。JS 1.1; JavaScript 2.0; ECMA v1。

prototype
一个构造函数的对象，定义了由该构造函数创建的所有对象共享的属性和方法。JS 1.1; JavaScript 2.0; ECMA v1。

## 方法

apply(thisobj, args)
将函数作为 `thisobj` 的方法调用，并将数组 `args` 的元素作为参数传递给函数。返回函数调用的返回值。JS 1.2; JavaScript 5.5; ECMA v3。

call(thisobj, args...)
将函数作为 `thisobj` 的方法调用，使用后续参数作为函数的参数。返回函数调用的返回值。JS 1.5; JavaScript 5.5; ECMA v3。

toString()
返回函数的字符串表示。在某些实现中，这是函数的实际源代码。JS 1.0; JavaScript 2.0; ECMA v1。

## 参见

Arguments

### Global

核心 JavaScript 1.0; JavaScript 1.0; ECMA v1

全局属性和函数

### 提要

this

## 描述

Global 对象包含了列出的全局属性和方法。这些属性和方法不需要通过任何其他对象引用或调用。你在顶层代码中定义的任何变量和函数都会成为 Global 对象的属性。

### 全局属性

Infinity
代表正无穷的数值。JS 1.2; JavaScript 3.0; ECMA v1。

NaN
非数字值。JS 1.1; JavaScript 2.0; ECMA v1。

undefined
未定义值。JS 1.1; JavaScript 2.0; ECMA v1。

### 全局函数

decode(uri)
返回一个经过解码的 uri 副本。JS 1.5; JavaScript 5.5; ECMA v3。

decodeURIComponent(s)
返回一个经过解码的 s 副本。JS 1.5; JavaScript 5.5; ECMA v3。

### History

在浏览器历史中后退或前进

### 提要

```
window.history
history
```

## 方法

back()
回到浏览器历史中之前访问过的 URL。无。

forward()
在浏览器历史中前进。无。

go(n)
跳转到相对于当前显示 URL 的第 n 个 URL。调用此方法时使用 -1 等于调用 `back()` 方法。无。

### Global

encode(uri)
返回一个替换了某些字符的 uri 副本。JS 1.5; JavaScript 5.5; ECMA v3。

encodeURIComponent(s)
返回一个替换了某些字符的 s 副本。JS 1.5; JavaScript 5.5; ECMA v3。

escape(s)
返回一个替换了某些字符的 s 副本。JS 1.0; JavaScript 1.0;（在 ECMA v3 中已废弃；请改用 `decodeURI()` 和 `decodeURIComponent()`。

unescape(s)
解码用 `escape()` 编码的字符串。返回 s 的解码副本。JS 1.0; JavaScript 1.0;（在 ECMA v3 中已废弃；请改用 `decodeURI()` 和 `decodeURIComponent()`。

 参见
Window

### Image

一个 HTML 图像

继承自：Element

### 提要

```
document.images[i]
document.images[image-name]
document.image-name
```

## 构造函数

```
new Image(width, height);
```

Image 构造函数创建了一个不可显示的离屏 Image 对象。width 和 height 参数是可选的。设置生成对象的 src 属性会使浏览器将图像预加载到缓存中。

## 属性 (Properties)

Image 对象为 HTML `<img>` 元素的每个属性定义了属性，例如 src、border、width、height、vspace 和 hspace。此外，它还为以下属性定义或提供了特殊行为：

- *complete*: 如果图像仍在加载，则为 false；如果已完成加载或在加载过程中发生错误，则为 true。只读。
- *src*: 一个可读可写的字符串，指定浏览器要显示的图像的 URL。此属性简单地镜像了 `<img>` 标签的 src 属性，但在此列出是因为许多重要的 HTML 效果是通过动态设置 Image 对象的 src 属性创建的，用以其中一张图像替换另一张图像。

## 事件处理器 (Event Handlers)

Image 继承自 Element 的事件处理器，并定义了以下内容：

- *onabort*: 如果用户取消下载图像，则调用。
- *onerror*: 如果下载图像时发生错误，则调用。
- *onload*: 当图像成功加载完成时调用。

## 输入 (Input)

客户端 JavaScript 1.0

一个表单输入元素

继承自：Element

## 摘要 (Synopsis)

```
form.elements[i]
form.elements[name]
form.name
```

## 属性 (Properties)

Input 对象为 HTML `<input>` 标签的每个属性定义了属性，例如 maxLength、readOnly、size 和 tabIndex。此外，它还定义了以下属性：

- *checked*: 一个可读可写的布尔值，指定类型为 "checkbox" 或 "radio" 的输入元素是否被选中 (true) 或未被选中 (false)。
- *checked*: 一个布尔值，指定类型为 "checkbox" 或 "radio" 的输入元素在首次创建或重置为初始状态时是否被选中。
- *defaultValue*: 一个字符串，指定类型为 "text" 或 "password" 的输入元素在首次创建或重置为初始状态时显示的文本。出于安全考虑，此属性不影响类型为 file 的输入元素。
- *form*: 指向包含该元素的 Form 对象的只读引用。此属性适用于所有类型的输入元素。
- *name*: 此输入元素的名称，由 HTML name 属性指定。此属性适用于所有类型的输入元素。
- *type*: 一个字符串，指定表单元素的类型。此属性镜像了 HTML type 属性。合法值列如下表所示；默认值为 text。Submit 和 Textarea 对象也有一个 type 属性，可能的值有 select-one、select-multiple 和 textarea。JS 1.1。

| 类型 | 描述 |
| --- | --- |
| "button" | 按钮 |
| "checkbox" | 复选框元素 |
| "file" | 文件上传元素 |
| "hidden" | 隐藏元素 |
| "image" | 图形表单提交按钮 |
| "password" | 掩码输入框 |
| "radio" | 互斥单选按钮 |
| "reset" | 表单重置按钮 |
| "text" | 单行文本输入框 |
| "submit" | 表单提交按钮 |

- *value*: 表单提交时发送的字符串值。对于类型为 "text"、password" 和 "file" 的输入元素，这是元素中显示的可编辑文本。你可以设置此属性来更改显示的文本。对于类型为 "button"、submit" 和 "reset" 的输入元素，value 是按钮上显示的标签。对于其他类型，value 字符串不显示。注意，出于安全考虑，类型为 "file" 的元素的 value 属性通常是只读的。

## 方法 (Methods)

- *blur()*: 失去焦点且不返回任何值。除 "hidden" 之外的所有元素类型均定义。
- *click()*: 在表单元素上模拟鼠标点击。适用于 button、checkbox、radio、reset 类型。
- *focus()*: 获取键盘焦点且不返回任何值。除 "hidden" 之外定义。
- *select()*: 选中元素并不返回任何值。适用于 text、password、file、submit 类型。

## 事件处理器 (Event Handlers)

- *onblur*: 当元素失去键盘焦点时调用。适用于 "hidden" 之外的所有元素类型。
- *onchange*: 当用户更改值时调用。适用于 text、radio、reset、submit 类型。
- *onclick*: 当用户点击元素时调用。适用于 button、checkbox、radio、reset 类型。
- *onfocus*: 当元素获得键盘焦点时调用。适用于 "hidden" 之外的所有元素类型。

## 参见 (See Also)

Form, Option, Textarea

## Layer

一个独立的文档层

## 摘要 (Synopsis)

```
document.layers[i]
document.layers[layer-name]
document.layer-name
```

## 构造函数 (Constructor)

```
new Layer(width, parent_layer)
```

#or (Description)

Layer 对象仅支持 Netscape 4 并在后续已废弃。

## 属性 (Properties)

- *above*: 上方的层（如果有）。只读。
- *below*: 下方的层（如果有）。只读。
- *background*: 层的背景图像。
- *bgColor*: 层的背景颜色。
- *height*: 层的高度。
- *left*: 相对于容器层或文档的水平坐标。
- *name*: 层的名称。
- *layers[]*: 包含此 Layer 对象的数组。
- *parentLayer*: 指向包含（作为父级）此层的 Layer 对象的只读引用。
- *src*: 可读可写的字符串，指定层内容的 URL（如果有）。设置此属性为新 URL会导致浏览器读取该 URL 的内容并显示在层中。
- *visibility*: 可读可写的字符串，指定层的可见性。三个合法值为："show"、hide" 和 "inherit"。
- *window*: 包含该层的 Window 对象，无论层嵌套有多深。
- *x, y*: 层的 X 和 Y 坐标。x 是 left 属性的别名，y 是 top 属性的别名。
- *zIndex*: 层在 z 轴堆叠顺序中的位置。当两个层重叠时，zIndex 较高的层在上方并遮挡 zIndex 较低的层。如果两个层具有相同的 zIndex，则在 layers[] 数组中出现较晚的层显示显示并覆盖先前的。

## 方法 (Methods)

- *load(src, width)*: 为层加载新的 URL，设置宽度，不返回任何值。
- *moveAbove(other_layer)*: 将此层移动到另一层上方，不返回任何值。
- *moveBelow(other_layer)*: 将此层移动到另一层下方，不返回任何值。
- *moveToBy(dx, dy)*: 相对于当前位置移动层，不返回任何值。
- *moveTo(x, y)*: 将层移动到相对于容器层或窗口的 (x,y) 点，不返回任何值。




```
moveToAbsolute(x, y)
将图层移动到相对于的位置，不返回任何值。
```

```
resizeBy(dw, dh)
按指定的量调整图层的大小，不返回任何值。
```

```
resizeTo(width, height)
将图层调整为指定的尺寸，不返回任何值。
```

## 链接

客户端 JavaScript 1.0

<a> 或 <area> 链接

继承自：Element (元素)

## 概要

```
document.links[i]
```

## 属性

Link 对象的许多属性代表了其 URL 的部分。对于每个此类属性，示例所示都是以下（虚构的）URL 的部分：

```
http://www.oreilly.com:1234/catalog/search.html?q=JavaScript&m=10results
```

### hash

一个可读可写的字符串属性，指定 Link URL 中的锚点部分，包括开头的哈希符号 (#) 标记。例如：“#result”。

### host

一个可读可写的字符串属性，指定 Link URL 中的主机名和端口部分。例如：“www.oreilly.com:1234”。

### hostname

一个可读可写的字符串属性，指定 Link URL 中的主机名部分。例如：“www.oreilly.com”。

### href

一个可读可写的字符串属性，指定 Link URL 的完整文本。

### pathname

一个可读可写的字符串属性，指定 Link URL 中的路径部分。例如：“/catalog/search.html”。

### port

一个可读可写的字符串（非数字）属性，指定 Link URL 中的端口部分。例如：“1234”。

### protocol

一个可读可写的字符串属性，指定 Link URL 中的协议部分，包括末尾的冒号：例如：“http:”。

### search

一个可读可写的字符串属性，指定 Link URL 中的查询字符串部分，包括开头的问号。例如：“?q=JavaScript&m=10”。

### target

一个可读可写的字符串属性，指定链接文档应该显示的哪个 Window 对象（即框架或顶层浏览器窗口）的名称。该属性是标准的 HTML target 属性。允许使用特殊名称“blank”、“top”、“parent”和“self”。

## 事件处理器

onclick

当用户点击链接时触发。在 JavaScript 1.1 中，此事件处理器可以通过返回 `false` 来防止链接跳转。

mouseout

当用户鼠标移出链接时触发。JS 1.1。

mouseover

当用户鼠标悬在链接上时触发。可以在这里设置当前窗口的 status 属性。返回 `true` 告诉浏览器不在状态栏中显示链接的 URL。

## 参见下

Anchor (锚点), Location (位置)

## Location

客户端 JavaScript 1.0

当前浏览器位置

## 概要

location
window.location

## 属性

Location 对象定义了与 Link 对象相同的 URL 相关属性，但 hash、host、href、pathname、port、protocol 和 search 属性除外。关于 target 的描述请参阅 Link 对象。设置这些任何一个属性都会导致浏览器从新 URL 加载并显示文档。作为快捷，你也可以通过为 Window 的 location 属性赋值 URL 字符串来加载新文档。

## 方法

reload(force)

从缓存或服务器重新加载当前文档。force 参数是可选的。如果为 `true`，则强制完全重新加载，即使文档未被修改。不返回任何值。JS 1.1。

replace(url)

用新文档替换当前文档，且不在浏览历史中生成新条目。不返回任何值。JS 1.1。

## 参见下

Link, Window.location

## Math

Core JavaScript 1.0; JavaScript 1.0; ECMA v1

数学函数和常量

## 概要

```
Math.constant
Math.function()
```

## 描述

Math 对象是用于分组数学常量和函数的占位符。它不像 Date 和 String 那样定义了一类对象。没有 Math() 构造函数，像 Math.sin() 这样的函数只是函数，而不是作用于对象的方法。

## 常量

Math.E: 常数 e，自然对数的底。

Math.LN10: 10 的自然对数。

Math.LN2: 2 的自然对数。

Math.LOG10E: e 以 10 为底的对数。

Math.LOG2E: e 以 2 为底的对数。

Math.PI: 常数 $\pi$。

Math.SQRT1_2: 1 除以 2 的平方根。

Math.SQRT2: 2 的平方根。

## 函数

Math.abs(x): 返回 x 的绝对值。

Math.acos(x): 返回 x 的反余弦；返回值在 0 到 $\pi$ 弧度之间。

Math.asin(x): 返回 x 的反正弦；返回值在 $-\pi/2$ 到 $\pi/2$ 弧度之间。

### Math.atan(x)

返回 $x$ 的反正切；返回值在 $-\pi/2$ 到 $\pi/2$ 弧度之间。

### Math.atan2(y, x)

返回一个 $-\pi$ 到 $\pi$ 弧度之间的值，指定正 X 轴与点之间的逆时针角。

### Math.ceil(x)

返回大于或等于 $x$ 的最近整数。

### Math.cos(x)

返回 $x$ 的余弦。

### Math.exp(x)

返回 $e$ 的 $x$ 次方。

### Math.floor(x)

返回小于或等于 $x$ 的最近整数。

### Math.log(x)

返回 $x$ 的自然对数。

### Math.max(args...)

返回参数中最大的。

### Math.min(args...)

返回参数中最小的。

### Math.pow(x, y)

$x$ 的 $y$ 次方。

### Math.random()

返回一个 0.0 到 1.0 之间的伪随机数。

### Math.round(x)

返回距离 $x$ 的整数。

### Math.sin(x)

返回 $x$ 的正弦。

### Math.sqrt(x)

返回 $x$ 的平方根。

### Math.tan(x)

返回 $x$ 的正切。

## 参见下

Number (数字)

## Navigator (导航)

客户端 JavaScript 1.0

关于浏览器的信息

## 概要

navigator

## 属性

appName

一个只读字符串，指定浏览器的昵称。在所有 Netscape 中都是“Mozilla”。在 IE 中也是“Mozilla”。

appVersion

一个只读字符串，指定浏览器的版本和平台信息。字符串的第一部分是版本号。将字符串传递给 `parseInt()` 获取主版本号，或传递给 `parseFloat()` 获取浮点数格式的版本号。字符串的其余部分提供了有关浏览器的其他细节，包括它运行的操作系统。然而，信息的格式在浏览器之间差异很大。

cookieEnabled

一个只读布尔值，如果浏览器启用了 cookie 则为 `true`，否则为 `false`。IE 4, Netscape 6。

language

一个只读字符串，指定浏览器的默认语言。属性的值是一个标准的双字母代码，例如英语的“en”或法语的“fr”。它也可以是五个字母，表示语言和地区变体，例如加拿大法语的“fr_CA”。Netscape 4；注意 IE 4 提供了两个语言相关属性。

platform

一个只读字符串，指定浏览器运行的操作系统和或硬件平台。虽然此属性没有标准值集，但一些典型值有“Win32”、“MacPPC”和“Linux i586”。JS 1.2。

systemLanguage

一个只读字符串，指定操作系统的默认语言，使用与特定 语言属性相同的标准代码。IE 4。

userAgent

一个只读字符串，指定浏览器在 HTTP 请求的 user-agent 请求头中使用的值。通常，这是 `navigator.appName` 的值后跟一个斜杠和 `navigator.appVersion` 的值。

userLanguage

一个只读字符串，指定用户的首选语言，使用与特定 语言属性相同的标准代码。IE 4。

## 方法

```
javaEnabled()
```

如果当前浏览器支持并启用了 Java，返回 `true`，否则返回 `false`。JS 1.1。

## 参见下

Screen (屏幕)





## Node

文档树中的节点

## 子类

- Attr, Comment, Document, DocumentFragment, Element, Text

## 常量

HTML 文档中的所有节点都是上述列出的 Node 子类之一的实例。每个 Node 对象都拥有一个 `nodeType` 属性，用于指定它是哪一个子类的实例。以下常量是 `nodeType` 的合法值。请注意，这些是 `Node` 的静态属性，而不是单个 Node 对象的属性。它们在 Internet Explorer 4、5 或 6 中没有定义；在这些浏览器中，你必须使用对应的整数字面量。

```
Node.ELEMENT_NODE = 1; // Element
Node.ATTRIBUTE_NODE = 2; // Attr
Node.TEXT_NODE = 3; // Text
Node.COMMENT_NODE = 8; // Comment
Node.DOCUMENT_NODE = 9; // Document
Node.DOCUMENT_FRAGMENT_NODE = 11; // DocumentFragment
```

## 属性

### attributes[]

如果此节点是一个 Element，则 `attributes` 属性是一个只读的 `Attr` 对象数组，代表该元素的属性。该数组可以通过数字或属性名称进行索引。然而，所有的 HTML 属性都有对应的 Element 属性，因此很少使用 `attributes[]` 数组。

### childNodes[]

这是一个只读的 `Node` 对象数组，包含此节点的节点。如果节点没有节点，则该属性为长度为 0 的数组。

### firstChild

此只读属性指向此节点的第一个子节点，如果节点没有节点，则为 `null`。

### lastChild

此只读属性指向此节点的最后一个子节点，如果节点没有节点，则为 `null`。

### nextSibling

`parentNode` 的 `childNodes[]` 数组中紧跟在该节点之后的兄弟节点，如果不存在这样的节点，则为 `null`。只读。

### nodeName

节点的名称。对于 Element 节点，此属性指定了元素的标签名，也可以通过 Element 的 `tagName` 属性获取。对于 Attr 节点，此属性指定了属性名称。对于其他类型的节点，该值是一个指定节点类型的常量字符串。只读。

### nodeType

节点的类型。此属性的合法值由上述列出的常量定义。

### nodeValue

节点的字符串值。对于 Text 和 Comment 节点，此属性持有文本内容。对于 Attr 节点，它持有属性值。此属性是可读可写的。

### ownerDocument

此节点所属的 Document 对象。对于 Document 节点，此属性为 `null`。只读。

### parentNode

此节点的父节点或容器节点，如果没有父节点，则为 `null`。请注意，Document 和 Attr 节点永远没有父节点。从文档中移除的节点或新创建且尚未插入文档树的节点，其 `parentNode` 为 `null`。只读。

### previousSibling

`parentNode` 的 `childNodes[]` 数组中紧邻在该节点之前的兄弟节点，如果不存在这样的节点，则为 `null`。

## 方法

### addEventListener(type, listener, useCapture)
为此节点注册一个事件监听器。`type` 是一个字符串，用于指定事件类型，但不包含 "on" 前缀（例如 "click" 或 "submit"）。`listener` 是事件处理函数。当触发时，它将以一个 `Event` 对象作为参数被调用。如果 `useCapture` 为 `true`，则这是一个捕获事件处理程序。如果为 `false` 或省略，则是一个普通事件处理程序。无返回值。DOM Level 2；在 IE 4、5 或 6 中不支持。

### appendChild(newChild)
通过将 `newChild` 节点添加到此节点的 `childNodes[]` 数组末尾，将其添加到文档树中。如果节点已经在文档树中，则会先将其移除，重新插入到新位置。返回 `newChild` 参数。

### cloneNode(deep)
返回此节点的副本。如果 `deep` 为 `true`，则节点的后代也将被递归复制。

### hasAttributes()
如果此节点是一个 Element 且具有任何属性，则返回 `true`。DOM Level 2。

### hasNodes()
如果此节点有任何子节点，则返回 `true`。

### insertBefore(newChild, refChild)
将 `newChild` 节点插入到文档树中 `refChild` 节点之前，`refChild` 必须是此节点的子节点。如果要插入的节点已经在树中，则会先将其移除。返回 `newChild`。

### isSupported(feature, version)
如果此节点支持命名特征指定的版本号，则返回 `true`。另见 `DOMImplementation.hasFeature()`。DOM Level 2。

### normalize()
通过删除空的 Text 节点并合并相邻的 Text 节点，规范此节点的所有 Text 后代节点。无返回值。

### removeChild(oldChild)
从文档树中移除 `oldChild` 节点。`oldChild` 必须是此节点的子节点。返回 `oldChild`。

### removeEventListener(type, listener, useCapture)
移除指定的事件监听器。无返回值。DOM Level 2；在 IE 4、5 或 6 中不支持。

### replaceChild(oldChild, newChild)
用 `newChild` 节点替换 `oldChild` 节点（后者必须是此节点的子节点）。如果 `newChild` 已经在文档树中，则会先从其当前位置移除。返回 `oldChild`。

# 另

Attr, Comment, Document, DocumentFragment, Element, Text

## Number

核心 JavaScript 1.1; JavaScript 1.79; 2.0; ECMA v1

对数字的支持

## 构造函数

```
new Number(value)
Number(value)
```

使用 `new` 操作符，`Number` 构造函数将其参数转换为数值并返回封装了该值的 Number 对象。如果不使用 `new`，`Number()` 是一个将其参数转换为数字并返回该值的函数。

## 常量

Number.MAX_VALUE
最大的数字。约为 1.79e308。

Number.MIN_VALUE
最小的数字。约为 5e-324。

Number.NaN
非数字。同全局 NaN。

Number.NEGATIVE_INFINITY
负无穷。

Number.POSITIVE_INFINITY
无穷。同全局 Infinity。

## 方法

### toExponential(digits)
以指数计数法返回数字的字符串表示，小数点前有一位，小数点后 `digits` 位。数字的小数部分将被舍入，并根据需要填充零。如果省略，则尽可能。

### toFixed(digits)
返回一个不使用指数计数法的数字字符串表示，小数点后恰好有 `digits` 位。`digits` 必须在 0 到 20 之间。数字将被舍入，并根据需要填充零。

### toLocaleString()
返回一个根据本地环境格式化的数字的字符串表示。这可能会影响用于小数点和千分位分隔符的字符。

### toPrecision(precision)
返回包含 `precision` 位有效数字的数字字符串表示。`precision` 必须在 1 到 21 之间。返回的字符串尽可能使用固定点法，否则使用指数计数法。数字将被舍入，并根据需要填充零。

### toString(radix)
使用指定的基数（base）将数字转换为字符串并返回该字符串。`radix` 必须在 2 到 36 之间。如果省略，使用基 10。

# 另

Math

## Object

JavaScript 对象的超类

## 构造函数

```
new Object();
```

此构造函数创建一个空对象，你可以对其添加任意属性。

## 属性

所有 JavaScript 对象无论如何创建，都拥有以下属性。

- constructor 指向构造对象的 JavaScript 函数的引用。JS 1.1; JavaScript 2.0; ECMA v1。

## 方法

所有 JavaScript 对象无论如何创建，都拥有以下方法。

- hasOwnProperty(propname) 如果对象拥有指定名称的非继承属性，则返回 `true`。如果对象没有该属性，或者它继承自原型对象，则返回 `false`。JS 1.5; JavaScript 5.5; ECMA v3。

- isPrototypeOf(a) 如果此是 `a` 的原型，则返回 `true`。如果 `a` 不是对象或者此对象不是它的原型，则返回 `false`。JS 1.5; JavaScript 5.5; ECMA v3。

- propertyIsEnumerable(propname) 如果对象拥有指定名称的非继承的可枚举属性，则返回 `true`，否则返回 `false`。可枚举属性是可以通过 for/in 循环枚举的属性。JS 1.5; JavaScript 5.5; ECMA v3。





toLocaleString()
返回对象的本地化字符串表示。该方法的默认实现简单地调用 `toString()`，但子类可以重写它以提供本地化。JS 1.5; JavaScript 5.5; ECMA v3.

toString()
返回对象的字符串表示。Object 类提供的该方法实现非常通用，没有提供多少有用的信息。Object 的子类通常通过定义它们自己的 `toString()` 方法来重写此方法，以产生更有用的输出。JS 1.0; JavaScript 2.0; ECMA v1.

valueOf()
返回对象的原始值（如果有）。对于类型为 Object 的对象，此方法返回返回本身。Object 的子类（如 Number 和 Boolean）重写此方法以返回与对象关联的原始值。JS 1.1; JavaScript 2.0; ECMA v1.

## 另见

Array, Boolean, Function, Number, String

## Option

客户端 JavaScript 1.0

一个可选择的选项

继承自：Element

## 摘要

```
select.options[i]
```

## 构造函数

在 JavaScript 1.1 及更高版本中，可以使用 `Option()` 构造函数动态创建 `Option` 对象：

```
new Option(text, value, defaultSelected, selected)
```

## 属性

defaultSelected
一个可读/写的布尔值，指定包含它的 Select 对象创建或重置时，该选项是否初始被选中。

index
一个只读整数，指定该选项在包含它的 Select 对象 `options[]` 数组中的索引。

selected
一个可读/写的布尔值，指定该选项当前是否被选中。你可以使用此属性来测试给定选项是否被选中。你也可以设置它来选中或取消选中选项。注意，当通过这种方式选中或取消选中选项时，`Select.onchange()` 事件处理程序不会调用。

text
一个可读/写的字符串，指定显示给用户的选项文本。

value
一个可读/写的字符串，指定在表单提交时如果选项被选中则传递给 Web 服务器的文本。

## 另见

Select

## RegExp 核心 JavaScript 1.2; JavaScript 3.0; ECMA v3

用于模式匹配的正则表达式

## 字面量语法

/pattern/attributes

## 构造函数

```
new RegExp(pattern, attributes)
```

正则表达式模式使用一种复杂的语法表示，该语法在本书早之前已总结。

## RegExp 实例属性

global
一个只读布尔值，指定 `RegExp` 是否具有 `g` 属性，因此执行全局匹配。

ignoreCase
一个只读布尔值，指定 `RegExp` 是否具有 `i` 属性，因此执行不区分大小写的匹配。

lastIndex
对于全局 `RegExp` 对象，此可读/写属性指定上一次匹配之后的字符位置；这是下一次匹配检查的第一个字符。

multiline
一个只读布尔值，指定 `RegExp` 是否具有 `m` 属性，因此执行多行匹配。

source
一个只读字符串，持有正则表达式*pattern* 的源文本，不包括斜杠和属性。

## 方法

exec(string)
将 *string* 与此 `RegExp` 进行匹配，返回一个包含匹配结果的数组，如果没有找到匹配项则返回 `null`。数组的元素 0 是匹配的文本。数组的后续元素包含匹配 `RegExp` 中子表达式的子字符串。返回的数组还有一个 `index` 属性，指定匹配的起始位置。

test(string)
如果 *string* 包含匹配此 `RegExp` 的文本，则返回 `true`，否则返回 `false`。

## 另见

String.match(), String.replace(), String.search()

## Screen

客户端 JavaScript 1.2

关于显示的信息

继承自：

## 摘要

screen

## 属性

availHeight
屏幕可用高度（像素）。

availWidth
指定屏幕的可用宽度（像素）。

colorDepth
浏览器调色板的深度，或屏幕的像素位深。

height
指定屏幕的总高度（像素）。

width
指定屏幕的总宽度（像素）。

## 另见

Navigator

## Select

客户端 JavaScript 1.0

一个图形化选择列表

继承自：Element

## 摘要

```
form.elements[i]
form.elements[element_name]
form.element_name
```

## 属性

`Select` 对象为 HTML `<select>` 标签的每个属性定义了属性，例如 `disabled`、`multiple`、`name` 和 `size`。此外，它还定义了以下属性：

## Select

form
包含此 `Select` 对象的 Form 对象。只读。

length
一个只读整数，指定 `options[]` 数组中的元素数量。此属性的值与 `options.length` 相同。

options[]
`Option` 对象数组，每个对象描述 `Select` 元素内显示的选项之一。你可以通过将 `options.length` 属性设置为较小的值来缩短选项集（或通过设置为零来移除所有选项）。你可以通过将数组中的某个元素设置为 `null` 来移除单个选项——这将其上方的元素下移，从而缩短数组。你可以使用 `Option()` 构造函数创建一个新的 `Option` 并将其赋值给 `options[options.length]` 来向 `Select` 对象添加选项。

selectedIndex
一个可读/写的整数，指定 `Select` 对象中被选中选项的索引。如果没有选中任何选项，`selectedIndex` 为 -1。如果选中了多个，`selectedIndex` 指定第一个选项的索引。

type
一个只读字符串，指定元素的类型。如果 `Select` 对象仅允许一个，则此属性为“single”；否则为“multiple”。另见 Input。

## 方法

add(new, old)
将 `new` 插入 `options[]` 中 `old` 之前的位置。如果 `old` 为 `null`，则将 `new` 追加到数组末尾。无返回值。

blur()
获取焦点且无返回值。

remove(n)
从 `options[]` 中删除第 n 个元素。无返回值。

## 事件处理器

onblur
失去输入焦点时调用。

onchange
当用户选择或取消选择项目时调用。

onfocus
获得输入焦点时调用。

## 另见

Form, Option

## String

核心 JavaScript 1.0; JavaScript 1.0; ECMA v1

字符串操作继承自：Object

## 构造函数

```
String(s)
new String(s)
```

使用 `new` 运算符，`String()` 函数将其参数转换为字符串。使用 `new` 运算符，它是将转换的值封装在 `String` 对象中的构造函数。

## 属性

```
length
```
字符串中的字符数。只读。

## 方法

```
charAt(n)
```
返回字符串位置 n 处的字符。

```
charCodeAt(n)
```
返回字符串位置 n 处的 Unicode 编码。JS 1.2; JavaScript 5.5; ECMA v1.

```
concat(value, ...)
```
返回从每个参数转换为字符串并拼接字符串得到的新字符串。JS 1.2; JavaScript 3.0; ECMA v3.

```
indexOf(substring, start)
```
返回字符串中在 `start` 位置之后首次出现 `substring` 的位置，如果没有找到则返回 -1。如果省略 `start`，则使用 0。

```
lastIndexOf(substring, start)
```
返回字符串中在 `start` 位置之前最后一次出现 `substring` 的位置，如果没有找到则返回 -1。如果省略 `start`，则使用字符串长度。

```
match(regexp)
```
将此字符串与指定的正则表达式匹配，返回一个包含匹配结果的数组，如果没有找到则返回 `null`。如果 `regexp` 不是全局正则表达式，返回的数组与 `RegExp.exec()` 方法相同。如果 `regexp` 是全局的（具有 `g` 属性），返回数组的元素包含每个匹配项的文本。JS 1.2; JavaScript 3.0; ECMA v3.

```
replace(regexp, replacement)
```
返回新字符串，将匹配 `regexp` 的文本替换为 `replacement`。`regexp` 可以是正则表达式或普通字符串。`replacement`可以是字符串，包含可选的正则表达式转义序列（如 $1），这些序列会被匹配文本的部分替换。它也可以是一个函数，根据传入的匹配细节计算替换字符串。JS 1.2; JavaScript 3.0; ECMA v3.

```
search(regexp)
```
返回字符串中第一个匹配 `regexp` 的子字符串的起始位置，如果没有找到则返回 -1。JS 1.2; JavaScript 3.0; ECMA v3.





### slice(start, end)
返回一个新字符串，其中包含字符串从 `start` 开始但不包括 `end` 的所有字符。如果省略 `end`，切片将延伸到字符串末尾。负数参数指定从字符串末尾计算的字符位置。JS 1.2; JavaScript 3.0; ECMA v3。

### split(delimiter, limit)
返回一个字符串数组，通过在`delimiter`指定的边界将字符串拆分为子字符串创建。`delimiter` 可以是字符串或正则表达式。如果 `delimiter` 是带有括号子表达式的正则表达式，则匹配子表达式的边界文本将包含在返回的数组中。参见 Array.join()。JS 1.1; JavaScript 3.0; ECMA v1。

### substring(from, to)
返回一个新字符串，其中包含复制从字符串 `from` 到 `to-1` 位置的字符。如果省略 `to`，子字符串将延伸到字符串末尾。不允许使用负参数。

### substr(start, length)
返回此字符串某部分的副本，从 `start` 开始并持续 `length` 个字符；如果未指定 `length`，则持续到字符串末尾。JS 1.2; JavaScript 3.0; 非标准：请改用 slice() 或 substring()。

### toLowerCase()
返回字符串的副本，将其所有大写字母转换为对应的小写字母（如果有的话）。

### toUpperCase()
返回字符串的副本，将其所有小写字母转换为对应的大写字母（如果有的话）。

## 静态方法
String.fromCharCode(c1, c2, ...)
返回一个包含由数值参数指定的编码的新字符串。JS 1.2; JavaScript 3.0; ECMA v1。

## 样式
DOM Level 2; IE 4

元素的内联 CSS 属性继承自：

## 概要
```
element.style
```

## 属性
Style 对象定义了大量属性：为 CSS2 规范定义的每个 CSS 属性对应一个属性。属性名称与 CSS 属性名称密切对应，但为了避免 JavaScript 中的语法错误进行了细微调整。包含连字符的多单词属性（如 `font-family`）在 JavaScript 中编写时不带连字符，且从第一个单词后的每个单词首字母大写：`fontFamily`。此外，`float` 属性与保留字 `float` 冲突，因此翻译为属性 `cssFloat`。

视觉 CSS 属性如表所示。由于属性直接对应 CSS 属性，因此没有为每个属性提供单独的文档。请查看 CSS 参考（如 Eric A. Meyer 写的《Cascading Style Sheets: The Definitive Guide》）获取每个属性的含义和合法值。注意，当前浏览器并未实现所有这些属性。

所有属性均为字符串，在处理具有数值的属性时需要小心。当查询此类属性时，必须使用 `parseFloat()` 将字符串转换为数字。设置此类属性时，你必须将数字转换为字符串，通常可以通过添加所需的单位说明（例如 "px"）来实现。

| background | counterIncrement | orphans |
| :--- | :--- | :--- |
| backgroundAttachment | counterReset | outline |
| backgroundColor | cssFloat | outlineColor |
| backgroundImage | cursor | outlineStyle |
| backgroundPosition | direction | outlineWidth |
| backgroundRepeat | display | overflow |
| border | emptyCells | padding |
| borderBottom | font | paddingBottom |
| borderBottomColor | fontFamily | paddingLeft |
| borderBorderStyle | fontSize | paddingRight |
| borderWidth | fontSizeAdjust | paddingTop |

## Text
DOM Level 1

文档中的一段文本

继承自：Node

## 描述
Text 对象代表 DOM 文档树中一段没有标记的纯文本。不要将其与 HTML 的单行文本输入元素混淆，后者由 Input 对象表示。

## 属性
data
此节点包含的文本字符串。

length
此节点包含的字符数。只读。

## 方法
```
appendData(text)
```
将指定的文本附加到此节点且不返回任何内容。

```
deleteData(offset, count)
```
从此节点中删除文本，从指定的 `offset` 处的字符开始，持续删除 `count` 个字符。不返回任何内容。

```
insertData(offset, text)
```
在指定的字符偏移处将指定的文本插入此节点中。不返回任何内容。

```
replaceData(offset, count, text)
```
从指定的 `offset` 开始持续 `count` 个字符的字符替换为指定的文本。不返回任何内容。

```
splitText(offset)
```
在指定的字符位置将此节点一分为二，将新的 Text 节点插入原节点之后，并返回新节点。

```
substringData(offset, count)
```
返回一个由位置 `offset` 处的字符开始的 `count` 个字符组成的字符串。

## 参见
```
Node.normalize()
```

## Textarea
客户端 JavaScript 1.0

多行文本输入

继承自：Element

## 概要
```
form.elements[i]
form.elements[name]
form.name
```

## 描述
Textarea 对象与 Input 对象非常相似。

## 属性
Textarea 对象为 HTML <textarea> 标签的每个属性定义了属性，例如 `cols`、`defaultValue`、`disabled`、`name`、`readOnly` 和 `rows`。它还定义了以下属性：

form
包含此 Textarea 对象的 Form 对象。只读。

type
只读字符串属性，指定类型。

value
读写字符串属性，指定 Textarea 中包含的文本。此属性与 `defaultValue` 相同。

## 方法
blur()
失去焦点且返回任何内容。

focus()
获取焦点且不返回任何内容。

select()
选中整个区域的内容。不返回任何内容。

## 事件处理程序
onblur
失去焦点时触发。

onchange
用户更改 Textarea 中的值时触发。

onfocus
获得焦点时触发。

## 参见
Element, Form, Input

## Window
浏览器窗口或帧

## 概要
+ self
window
window.frames[i]

## 属性
Window 对象定义了以下属性。不可移植的特定属性单独列出。注意 Window 对象是客户端 JavaScript 的全局对象；因此 Window 对象也具有页面列出的属性。

closed
只读布尔值，指定窗口已关闭。

defaultStatus
读写字符串，当浏览器未显示其他消息时，指定状态栏显示的持久消息。

document
指向窗口或帧中 Document 对象的只读引用。参见 Document。

frames[]
窗口内每个帧的 Window 对象数组。注意由 frames[] 引用的帧可能包含帧并拥有自己的 frames[] 数组。

history
指向窗口或帧 History 对象的只读引用。参见 History。

length
指定窗口或帧中包含的帧数。同于 `frames.length`。

location
窗口或帧的 Location 对象。参见 Location。此属性具有特殊行为：如果你赋值一个 URL 字符串，浏览器将加载并显示该 URL。

navigator
指向 Navigator 对象的只读引用，提供浏览器的版本和配置信息。参见 Navigator。

opener
指向打开此窗口的 Window 的读写引用。JS 1.1。

parent
指向包含此窗口或帧的 Window 对象的只读引用。如果窗口是顶级窗口，parent 指向自身。

screen
指向 Screen 对象的只读引用，指定浏览器运行屏幕的信息。参见 Screen。JS 1.2。

top
指向包含此窗口的顶级窗口的只读引用。如果窗口是顶级窗口，top 指向自身。

window
window 属性等同于 self 属性；它包含指向此窗口的引用。





## Netscape 4 属性

innerHeight, innerWidth
读写属性，用于指定此窗口文档显示区域的高度和宽度（以像素为单位）。这些维度不包括菜单栏、工具栏、滚动条等的高度。

outerHeight, outerWidth
读写整数，用于指定窗口的总高度和宽度（以像素为单位）。这些维度包含了菜单栏、工具栏、滚动条、窗口边框等的高度和宽度。

pageXOffset, pageYOffset
只读整数，用于指定当前文档向右（pageXOffset）和向下（pageYOffset）滚动的像素数。

screen, screenY
只读整数，用于指定窗口在屏幕上左上角的 X 和 Y 坐标。如果此窗口是一个帧（frame），这些属性指定包含该帧的顶层窗口的 X 和 Y 坐标。

## IE 4 属性

clientInformation
IE 特有的 `navigator` 属性的别名。指向 `navigator` 对象。

event
event 属性指向一个 Event 对象，该对象包含此窗口内最近发生事件的详细信息。在 IE 事件模型中，Event 对象不作为参数传递给事件处理程序，而是赋值给此属性。

## 方法

Window 对象具有以下可移植方法。由于 Window 对象是客户端 JavaScript 中的全局对象，它还定义了 Global 引用页面上列出的方法。

alert(message)
在对话框中显示消息。无返回值。JS 1.0。

blur()
释放键盘焦点并无返回值。JS 1.1。

clearInterval(intervalId)
取消由 `intervalId` 指定的代码的周期性执行。参见 `setInterval()`。无返回值。JS 1.2。

clearTimeout(timeoutId)
取消由 `timeoutId` 指定待定超时。参见 `setTimeout()`。无返回值。JS 1.0。

close()
关闭窗口并无返回值。JS 1.0。

confirm(question)
在对话框中显示问题并等待“是”或“否”的响应。如果用户点击确定 按钮，返回 true；如果用户点击取消按钮，则返回 false。JS 1.0。

focus()
请求键盘焦点；这也会所有平台上将窗口置于顶层。无返回值。JS 1.1。

getComputedStyle(elt)
返回一个只读的 Style 对象，其中包含应用于指定文档元素 `elt` 的所有 CSS 样式（而不只是内联样式）。从此计算样式对象查询的定位属性（如 left、top 和 width）始终以像素值形式返回。DOM 第 2 级。

moveBy(dx, dy)
将窗口从当前位置移动指定的距离并无返回值。JS 1.2。

moveTo(x, y)
将窗口移动到指定的位置并无返回值。JS 1.2。

open(url, name, features)
在命名窗口中显示指定的 `url`。如果省略了 `name` 参数或没有同名的窗口，则创建一个新窗口。可选的 `features` 参数是一个字符串，以逗号分隔的特性列表指定新窗口的大小和装饰。所有平台通常支持的特性名称有：`width=pixels``height=pixels`、location、menubar、resizable、status 和 toolbar。在 IE 中，使用 `left=x` 和 `top=y` 设置窗口位置。在 Netscape 中，我们使用 `screenX=x` 和 `screenY=y`。返回现有或新的 Window 对象。JS 1.0。

print()
模拟点击浏览器的打印按钮并无返回值。Netscape 4；IE 5。

prompt(message, default)
在对话框中显示消息并等待用户输入文本响应。显示可选的 `default` 作为默认响应。返回用户输入的字符串；如果用户未输入字符串，返回空字符串；如果用户点击取消，则返回 null。JS 1.0。

resizeBy(dw, dh)
按指定量调整窗口并无无。JS 1.2。

resizeTo(width, height)
按指定大小调整窗口并无返回值。JS 1.2。

scroll(x, y)
将窗口滚动到指定的坐标并无返回值。JS 1.1；在 JS 1.2 中已弃用，改为 `scrollTo()`。

scrollToBy(dx, dy)
按指定量滚动窗口并无返回值。JS 1.2。

scrollTo(x, y)
将窗口滚动到指定的位置并无返回值。JS 1.2。

setInterval(code, interval, args...)
每隔 interval 毫秒执行一次 JavaScript 代码。在 Netscape 4 和 IE 5 中，`code` 可以是函数引用而不是字符串。在这种情况下，函数每隔 interval 毫秒被调用一次。在 Netscape 中，interval 之后的任何参数都会传递给该函数，但 IE 不支持此功能。返回一个间隔 ID，可以传递给 `clearInterval()` 取消周期性执行。JS 1.2。

setTimeout(code, delay)
在延迟 delay 毫秒后执行字符串 `code` 中的 JavaScript 代码。在 Netscape 4 和 IE5 中，`code` 可能是函数而不是字符串；参见 `setInterval()` 下的讨论。返回一个 ID 值，可以传递给 `clearTimeout()` 取消待定的执行。注意此方法立即返回。JS 1.0。

## 事件处理器

blur
当窗口失去焦点时触发。

onerror
当发生错误时触发。

focus
当窗口获得焦点时触发。

onload
当文档完全加载时触发。

resize
当窗口大小改变时触发。

unload
当浏览器离开文档时触发。





# 使用 Dreamweaver MX 构建数据驱动型网站

作者：Simon Allardice
第1版，2002年12月（预计）
375页（预估），ISBN 0-596-00340-4

本书向高级用户一步一步教导他们如何使用 Dreamweaver MX（原 UltraDev）创建页面，通过 ColdFusion、ASP、ASP.Net、JSP 或 PHP 访问远程数据库——而无需大量的编程。读者将从作者的一手知识和精湛的教学风格中受益。

# 动态 HTML：权威指南，第2版

作者：Danny Goodman
第2版，2002年9月
1500页，ISBN 0-596-00316-1

《动态 HTML：权威指南》包含了大量最新网络规范的信息，包括 HTML 4.01、CSS2、DOM Level 2 和 JavaScript 1.5，书中还详细介绍了主流浏览器的最新版本——Internet Explorer 6 和 Netscape Navigator 6。此书不可或缺、完整且简洁，是所有参与创建动态网页内容的开发者的必备汇编。它包含了开发者创建功能性、跨平台动态 HTML 应用程序所需的所有内容。

# 网络服务精要

作者：Ethan Cerami
第1版，2002年2月
304页，ISBN 0-596-00224-6

这本简洁的著作为程序员提供了关于 XML 网络服务的介绍和方便的参考。它解释了这种新型分布式服务的基础，演示了如何使用开源 Java 工具快速创建服务的方法，并探索了四种新兴技术：XML-RPC、SOAP、UDDI 和 WSDL。如果你想突破网络服务的炒作，找到有关这些演进技术的有用信息，看这一本就足够了。

# PHP 口袋参考，第2版

作者：Erasmus Lerdorf
第1版，2002年11月（预计）
96页（预估），ISBN 0-596-00402-8

本书由 PHP 项目的创始人编写，这本宝贵的小书既是 PHP 语法的实用入门介绍，也是 PHP 提供的大量函数的快速参考。第二版经过彻底更新，包含了语言最新版本 PHP 4 的规范，在口袋大小的指南中提供了权威的 PHP 概述。它易于随身携带，是学习 PHP 应用程序开发基础的完美教程，也是 O'Reilly《PHP》的理想伴侣。

![](img/c595610b738444dc06a09036110543e5_139_0.png)

订购：800-998-9338 • order@oreilly.com • www.oreilly.com
大多数 O'Reilly 书籍的在线版可通过 safari.oreilly.com 订阅获取
在大多数零售店和在线书店也有售。

# 使用 Mozilla 创建应用程序

作者：David Boswell, Brian King, Ian Oeschger, Pete Collins & Eric Murphy
第1版，2002年9月（预计）
480页（预估），ISBN 0-59600052-9

本书旨在任何想要更多了解 Mozilla 是什么以及如何使用 Mozilla 技术创建应用程序的人。Netscape 6、ActiveState 的 Komodo、Jabberzilla 等应用程序已经利用了 Mozilla 作为开发框架的独特能力。阅读此书后，你将能够为自己的应用程序利用该框架。

# PHP 菜谱

作者：David Sklar & Adam Trachtenberg
第1版，2002年10月
500页，ISBN 1-56592-681-1

这本菜谱为 PHP 程序员经常面临的问题提供了丰富的解决方案。主题涵盖从初级到高级的网络编程技术，《PHP 菜谱》为任何使用这种脚本语言生成动态网页内容的程序员或网页设计师提供了实用的示例——或“食谱”。对于每个食谱，作者都包含了一个讨论，解释了解决方案背后的逻辑和概念。

# 使用 PHP & MySQL 构建网络数据库应用程序

作者：Hugh E. Williams & David Lane
第1版，2002年3月
582页，ISBN 0-596-00041-3

本书为创建网络数据库应用程序提供了理论和实践指导。关于设计关系型数据库以及与之交互的网络应用程序架构的详细信息，对于那些以前处理过数据库支持网站的读者来说将特别有用。本书在 Apache 平台上使用 PHP 和 MySQL 实现了一个示例网络应用程序。

# PHP 编程

作者：Rasmus Lerdorf & Kevin Tatroe
第1版，2002年3月
528页，ISBN 1-56592-610-2

《Programming PHP》是一本 PHP 的全面指南，PHP 是一种简单而强大的创建动态网页内容的语言。书中充满了 PHP 创始人 Rasmus Lerdorf 的独特知识，是该语言及其应用的详细参考，包括表单处理、会、数据库、XML 和图形等主题。涵盖了语言的最新版本 PHP 4。

# JavaScript 口袋参考

JavaScript——一种可以直接嵌入 HTML 页面的强大基于对象的脚本语言——已经在开发者的工具箱中占据了地位，以至于成为 Web 开发者的必备知识。你可以使用 JavaScript 创建完全在浏览器中运行的动态交互应用程序。JavaScript 也是开发动态 HTML 内容的首选语言。

第二版《JavaScript 口袋参考》提供了核心语言和客户端脚本环境的概述，以及涵盖核心和客户端对象、方法和属性的快速参考材料。新版涵盖了 JavaScript 1.5，对于使用浏览器（如 Internet Explorer 6、Netscape 6 和 7 以及 Mozilla）的开发者特别有用。这本口袋书易于随身携带，是畅销书《JavaScript：权威指南》的完美伴侣卷。

![](img/c595610b738444dc06a09036110543e5_147_0.png)

