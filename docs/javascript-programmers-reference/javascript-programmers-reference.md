
# JavaScript 程序员参考指南

指尖上的核心编程信息

涵盖语法、语句和控制结构

展示 JavaScript 强大的客户端功能

通过具体示例定义 JavaScript 的内置对象和函数

Christian MacAuley Web 编码员、设计师、作家和培训师

Paul Johnson Web 开发者和设计师

## 关于作者

**Christian MacAuley** 是一位 Web 编码员、作家和培训师。她在流媒体行业担任 JavaScript 编码员的丰富经验为她赢得了 PSINet、eStack 和 TV on the Web 等客户。Christian 关于 Web 设计和编码的文章曾发表在《Web Review》和《ArtToday》上。Christian 还是《视觉学习者的手持设备》（VisiBooks 2001）的作者。

**Paul Johnson** 自 1994 年以来一直在构建网站，在编写客户端 JavaScript、动态 HTML 和 Perl 代码方面拥有丰富经验。他目前在华盛顿大都会的一家财富 500 强企业提供合同服务。

## 致谢

我们要感谢 Ann。

## 分号 (Semicolons)

JavaScript 与许多编程语言一样，语句末尾有分号。尽管如此，JavaScript 并不要求你放置分号。以下每个语句都是有效的：

```
ThisMonth = "August"
someyear = "2022"; nextnum = 33;
testvalue = 300
```

如果一行中有多条语句，则必须使用分号：

```
thisyear = "2001"; othernum = 100;
```

尽管分号是可选的，但良好的编程习惯是不要省略它们。

## 注释 (Comments)

JavaScript 注释仅仅是代码中的说明文字——它们不是程序的一部分。开发者（如你）通常使用注释为代码添加说明，以便日后参考。JavaScript 中有两种形式的注释。行注释以 `//` 开始并以换行结束，多行注释以 `/*` 开始并以 `*/` 结束。这些符号之间可以包含多行。

```
// 这是一个注释
num = 5; // 注释可以跟在代码后面。
/* 注释可以跨越多行，
只要你使用这种注释方式即可 */
```

## 字面量与标识符 (Literals and Identifiers)

字面量代表 JavaScript 中的一个值。字面量是固定值，而不是你定义的变量。字面量的类型包括整数字面量、八进制字面量、十六进制字面量和字符串字面量。

## 保留字 (Reserved Words)

在 JavaScript 中，有几组属于“保留字”的单词。保留字是不应该作为标识符使用的单词。你不能使用任何 JavaScript 关键字作为变量名或函数名。

### JavaScript 关键字

```
break false this
in void continue
for new true
while delete function
null var typeof
with else return
if
```

**表 1-1.** JavaScript 关键字

表 1-1 显示了关键字。JavaScript 关键字是语言语法的一部分，因此应该避免使用。此外，表 1-2 显示的 Java 关键字也应该被避免。Java 关键字没有用于 JavaScript 中，但 JavaScript 未来的版本可能会使用它们。表 1-3 列出了其他需要避免的标识符——这些是由客户端 JavaScript 预定义的数据类型、函数和变量名称。由于 Internet Explorer 不区分大小写，表 1-2 中的所有关键字应同时避免小写和大写形式。最后，还有一些为 ECMA-262 标准可能的未来扩展的保留，如表 1-4 所示。

### Java 关键字

```
abstract default implements
private throw boolean
do import protected
throws byte double
instanceof public transient
case extends int
short try catch
final interface static
char finally long
class float native
switch const goto
package synchronized super
```

**表 1-2.** Java 关键字

### 其他需要避免的标识符

| alert | escape | JavaPackage |
| :--- | :--- | :--- |
| onunload | setTimeout | Anchor |
| eval | length | open |
| status | Area | FileUpload |
| Link | opener | String |
| Array | focus | Location |
| Option | Submit | assign |
| Form | location | Packages |
| sun | blur | Frame |
| Math | parent | taint |
| Boolean | frames | MimeType |
| parseFloat | Text | Button |
| Function | name | parseInt |
| Textarea | Checkbox | getClass |
| navigate | Password | top |
| clearTimeout | Hidden | close |
| Plugin | toString | Navigator |
| History | navigator | prompt |
| unescape | closed | history |
| netscape | prototype | untaint |
| confirm | Image | Number |
| Radio | valueOf | Date |
| is | Object | ref |
| Window | defaultStatus | java |
| onblur | Reset | onerror |
| Document | JSONArray | JavaClass |
| scroll | document | Element |
| onfocus | Select | self |
| JSONObject | onload | self |
| callee | caller | |

**表 1-3.** 其他需要避免的标识符

### ECMA 扩展保留字

```
catch const enum
finally throw class
debugger extends super
try
```

**表 1-4.** ECMA 扩展保留字

## 数字 (Numbers)

数字是基本数据类型；数值字面量可以是整数或浮点数；而整数可以是十进制、八进制或十六进制的。JavaScript 不区分浮点值和整数值；JavaScript 将所有数字都识别为浮点值。这些浮点数的表示范围可以从 +/- 1.7976931348623157x10³⁰⁸ 大小到 +/- 5x10⁻³²⁴。

### 整数字面量 (Integer Literals)

整数字面量用十进制数字表示，这些数字是不以零开头的正数或负数。整数字面量永远没有小数部分，例如：

32
61245
-128
1584

### 八进制和十六进制字面量 (Octal and Hexadecimal Literals)

整数字面量也可以用八进制（基数 8）和十六进制（基数 16）值表示。八进制字面量是 0 到 7 之间的数字，可以以 0 开头。例如，以下数字是八进制字面量：

030547
-447
56027

十六进制字面量是以 `0x` 或 `0X` 开头的正数或负数，后面跟着数字 0 到 9 和/或字母 A 到 F。字母 A 到 F 代表数字 10 到 15，且不区分大小写。例如，以下数字是十六进制字面量：

-0x21548FFAD
0Xabdf
0xABCD

### 浮点字面量 (Floating-Point Literals)

浮点字面量是可能包含指数的正数或负数。例如，以下数字是浮点数：

5.14
-2.5
.14

### 特殊值 (Special Values)

特殊值用于表示非数值状态。在 JavaScript 中，与许多其他语言不同，`null` 不等于 0。

`undefined` 与 `null` 不同。当使用不存在的变量或已声明未赋值的变量时，会返回 `undefined` 值。`null` 关键字代表值的缺失，而其他字面量代表某种值。

| 常量 | 含义 |
| :--- | :--- |
| `Number.MAX_VALUE` | 最大数字 |
| `Number.MIN_VALUE` | 最小数字 |
| `Number.NaN` | 特殊的非数字 |
| `Number.POSITIVE_INFINITY` | 特殊的正无穷 |
| `Number.NEGATIVE_INFINITY` | 特殊的负无穷 |

**表 1-5.** 特殊常量

## 字符串 (Strings)

字符串只是包含在单引号或双引号内的字符序列。

"This is a string."
"465"
'This is a test'
"10

### 字符串字面量中的转义序列 (Escape Sequences in String Literals)

转义序列始终以反斜杠 `\` 开始。参见表 1-6。它们代表标准键盘上不存在的字符。

| 序列 | 表示的字符 |
| :--- | :--- |
| `\b` | 退格 |
| `\f` | 换页 |
| `\n` | 换行 |
| `\r` | 回车 |
| `\t` | 制表符 |
| `\'` | 单引号 |
| `\"` | 双引号 |
| `\\` | 反斜杠 |
| `\xxx` | Latin-1 编码的字符；包含一到三个八进制数字，在 0 到 377 之间 |
| `\xXX` | Latin-1 编码的字符；包含两个十六进制数字，在 00 到 FF 之间 |
| `\uXXXX` | 由四个十六进制指定的 Unicode 字符（Netscape 4 不支持） |

**表 1-6.** 转义序列定义

### 布尔字面量 (Boolean Literals)

布尔字面量表示逻辑值，`true` 或 `false`。布尔字面量常用于 `while` 循环，如下：

```
while(test = true) {
  doSomething()
  if (num != 1) test = false;
}
```

## 声明变量 (Declaring Variables)

变量可以通过三种方式赋值。你可以通过简单地赋值一个值来隐式声明变量，例如：

```
x = 12; // 声明并给 x 赋值
```

你也可以使用 `var` 关键字显式地声明变量。使用 `var` 时，赋值是可选的。如果你不给变量赋值，其值将为 `undefined`。

```
var x; // 仅声明 x
var x = 12; // 声明并给 x 赋值
```

# 运算符

在接下来的页面中，我们将详细讨论每个 JavaScript 运算符。JavaScript 中使用的运算符与 C++ 和 Java 中使用的运算符非常相似。表 1-7 提供了 JavaScript 中可用运算符的概述、每个运算符的作用以及每个运算符期望的操作数。

| 运算符 | 操作数 | 操作总结 | 备注 |
|---|---|---|---|
| `+` | 数字，字符串 | 相加数字，拼接字符串 | |
| `+=` | 数字，字符串 | 将第二个数字加到第一个数字上并赋新值；拼接字符串并赋新值 | |
| `++` | 数字 | 前置或后置自增 | |
| `-` | 数字 | 减法 | |
| `-=` | 数字 | 从第一个操作数减去第二个操作数并赋新值 | |
| `--` | 数字 | 前置或后置自减 | |
| `*` | 数字 | 乘法 | |
| `/` | 数字 | 将第一个操作数除以第二个操作数 | |
| `/=` | 数字 | 将第一个操作数除以第二个操作数并赋新值 | |
| `%` | 数字 | 取余运算 | |
| `%=` | 数字 | 取余运算并赋新值 | |
| `<` | 数字或字符串 | 测试数字是否小于，测试字符串的 ABC 顺序 | |
| `<=` | 数字或字符串 | 测试数字是否小于或等于，测试字符串的 ABC 顺序 | |
| `>` | 数字或字符串 | 测试数字是否大于，测试字符串的 ABC 顺序 | |
| `>=` | 数字或字符串 | 测试数字是否大于或等于，测试字符串的 ABC 顺序 | |
| `==` | 任意 | 测试相等性 | Netscape JavaScript 1.3 及更高版本中存在某些不一致 |
| `===` | 任意 | 测试同一性 | |
| `!` | 布尔值 | 返回单个操作数的逻辑取反 | |
| `!=` | 任意 | 测试不等性 | |
| `!==` | 任意 | 测试非同一性 | JavaScript 1.3 及更高版本 |
| `&&` | 布尔值 | 测试逻辑与 | |
| `||` | 布尔值 | 测试逻辑或 | |
| `,` | 任意 | 求值两个语句 | |
| `.` | 对象，属性，方法 | 访问对象的属性和方法 | |
| `[]` | 数组，整数 | 访问数组索引 | |
| `()` | 函数，参数 | 执行函数调用 | |
| `?:` | 布尔值, 任意，任意 | 三元条件运算符；测试一个语句并返回一个操作数的值 | |
| `delete` | 对象，属性，数组元素 | 删除对象、属性和数组元素 | JavaScript 1.2 及更高版本 |
| `new` | 对象类型 | 创建带有构造函数的任何对象的实例 | |
| `typeof` | 任意 | 返回其操作数的类型 | |
| `void` | 任意 | 求值表达式并返回 undefined 值 | |
| `&` | 整数 | 计算位与 | |
| `&=` | 整数 | 计算位与并赋新值 | |
| `\|` | 整数 | 计算位或 | |
| `\|=` | 整数 | 计算位或并赋新值 | |
| `^` | 整数 | 计算位异或 | |
| `^=` | 整数 | 计算位异或并赋新值 | |
| `~` | 整数 | 计算位非 | |
| `<<` | 整数 | 计算位左移 | |
| `<<=` | 整数 | 计算位左移并赋新值 | |
| `>>` | 整数 | 计算位右移 | |
| `>>=` | 整数 | 计算位右移并赋新值 | |
| `>>>` | 整数 | 计算零填充的位右移 | |
| `>>>=` | 整数 | 计算零填充的位右移并赋新值 | |

**表 1-7.** 运算符总结

## JavaScript 运算符

JavaScript 有二元运算符、一元运算符以及一个三元运算符。一元运算符只需要一个操作数，二元运算符需要两个，而三元运算符需要三个操作数。

## 操作数

操作数可以是 JavaScript 中的任何“东西”，例如数字或字符串、变量或对象。

## 运算符优先级

运算符之间有高低之分。例如，`*` 运算符的优先级高于 `+` 运算符。运算符的优先级按照表 1-8 所示的顺序降低。

**高**
`. [] ()`
`++ -- ~ ! delete new typeof void`
`* / %`
`+ -`
`<< >> >>>`
`< > <= >=`
`== != === !==`
`&`
`^`
`\|`
`&&`
`\|\|`
`?:`
`= *= %= += -= <<= >>= >>>= &= ^= \|=`
**低**
`,`

**表 1-8.** 运算符优先级

### 从左到右结合的运算符

| `[]` | `()` | `.` |
| :--- | :--- | :--- |
| `*` | `/` | `%` |
| `+` | `-` | |
| `<<` | `>>` | `>>>` |
| `<` | `<=` | `>` |
| `>=` | `==` | `!=` |
| `===` | `!==` | `&` |
| `^` | `\|` | `&&` |
| `\|\|` | `,` | |

**表 1-9.** 从左到右结合的 JavaScript 运算符

### 从右到左结合的运算符

| `++` | `--` | `-` | `~` |
| :--- | :--- | :--- | :--- |
| `!` | `delete` | `new` | `typeof` |
| `void` | `+=` | `-=` | `*=` |
| `/=` | `%=` | `<<=` | `>>=` |
| `>>>=` | `&=` | `^=` | `\|=` |
| `=` | `?:` | | |

**表 1-10.** 从右到左结合的 JavaScript 运算符

## 运算符类型

## 算术运算符

### 加法 (+)

`+` 运算符是一个二元运算符。它相加数字：

```
z = 3 + 4; // z 现在等于 7
```

拼接字符串：

```
z = "3" + "4" // z 现在等于 "34"
greeting = "Hel" + "lo";
// greeting 现在等于 "Hello"
```

### 减法 (-)

当作为二元运算符使用时，`-` 将数字相互相减。

```
x = 10 - 4; // x 等于 6
```

当作为一元运算符使用时，`--` 从数字中减去一个。

```
x = 10;
x--; // x 现在等于 9
```

如果作为一元运算符使用，`-` 将数字变为负数，反亦然。

### 乘法 (*)

`*` 运算符是二元运算符，用于乘以两个操作数。

```
z = 3 * 2; // z 现在等于 6
```

### 除法 (/)

将第一个操作数除以第二个操作数。

```
z = 10 / 2; // z 等于 5
```

除以零会产生特殊值。

```
z = 3 / 0; // z 等于 POSITIVE_INFINITY
z = -3 / 0; // z 等于 NEGATIVE_INFINITY
```

如果 `/` 用于非数值，它将尝试计算两个操作数的商。

### 取余运算 (%)

`%` 运算符也称为模运算。它返回除两个操作数后剩余的数。

```
z = 7 % 2; // z 等于 1
z = 6 % 2; // z 等于 0
```

如果 `%` 用于非数值，它将尝试计算两个操作数的余数。

### 自增 (++)

`++` 运算符是一个一元运算符，用于将数字加一。

```
x = 5;
++x; // x 现在等于 6
```

`++` 运算符可以是前置的也可以是后置的。前置自增意味着在执行语句之前增加数字。在接下来的示例中：

```
x = 5;
y = ++x; // y 等于 6，x 也等于 6
```

后置自增意味着在执行语句之后再增加数字。在接下来的示例中：

```
x = 5;
y = x++; // y 等于 5，x 等于 6
```

### 自减 (--)

`--` 运算符是一个一元运算符，用于将数字减一。

`--` 运算符可以是前置的也可以是后置的。前置自减意味着在执行语句之前减小数字。在接下来的示例中：

```
x = 5;
y = --x; // y 等于 4，x 也等于 4
```

后置自减意味着在执行语句之后再减小数字。在接下来的示例中：

```
x = 5;
y = x--; // y 等于 5，x 等于 4
```

`--` 会尝试将非数值转换为数字后再进行自减。

## 逻辑运算符

### 逻辑与 (&&)

`&&` 运算符是一个二元运算符。当 `&&` 两侧的语句都为真时，`&&` 求值为真。非空字符串、非零且正值以及真表达式均求值为真。请参考以下示例。

```
x = (1 && 1); // x is true
x = (0 && 1); // x is false
x = ("cat" && "dog"); // x is true
x = ("cat" && null); // x is false
```

### 逻辑或 (||)

`||` 运算符是一个二元运算符。如果 `||` 左侧的值为正数、非零或真，则 `||` 返回左侧表达式的值。否则，如果右侧表达式的值为正数、非零或真，它返回右侧表达式的值。如果 `||` 右侧的值不真，则返回左侧的值。一个例外是 Netscape 2 和 3，如果右侧表达式求值为真，`||` 将返回真。

```
x = ("hello" || "hi"); // x is "hello"
x = (0 || "hi"); // x is "hi"
x = (-2 || 0); // x is -2
```

### 逻辑非 (!)

`!` 运算符是一个一元运算符。如果操作数为负数、零或假，则 `!` 返回真。否则，`!` 返回假。

```
x = null;
y = !x; // y is true
```

## 位运算符

位运算符将操作数视为二进制数而非整数。由于这个原因，它们通常是需要的。

### 位与 (&)

`&` 运算符是一个二元运算符，它接受 32 位整数。`&` 通过将两个操作数转换为二进制，然后按位进行比较来工作。比较的结果应用于位。

```
x = 9 & 3; // x is equal to 1
```

### 位或 (|)

`|` 运算符是一个二元运算符，它接受 32 位整数。`|` 通过将两个操作数转换为二进制，然后按位进行比较来工作。比较的结果应用于位。

```
x = 9 | 3; // x is equal to 11
```

### 位异或 (^)

`^` 运算符是一个二元运算符，它接受 32 位整数。`^` 将两个操作数转换为二进制，使用异或逻辑按位进行比较。比较的结果应用于位。

```
x = 9 ^ 3; // x is equal to 10
```

### 位取反 (~)

`~` 运算符是一个一元运算符，它接受 32 位整数。`~` 将单个整数转换为二进制，反转整数的所有位。

```
x = ~9; // x is equal to -10
```

### 左移 (<<)

`<<` 运算符是一个二元运算符，它接受 32 位整数。`<<` 将第一个操作数转换为二进制，在左侧添加第二个操作数指定的个数的零。左移溢出的位会被丢弃。

```
x = 9 << 3; // x is equal to 72
```

### 符号右移 (>>)

`>>` 运算符是一个二元运算符，它接受 32 位整数。`>>` 将第一个操作数转换为二进制，在右侧添加第二个操作数指定的个数的零。右移溢出的位会被丢弃。

```
x = 9 >> 3; // x is equal to 1
```

### 无符号右移 (>>>)

`>>>` 运算符是一个二元运算符，它接受 32 位整数。`>>>` 将第一个操作数转换为二进制，在右侧添加第二个操作数指定的个数的零。右移溢出的位会被丢弃，且左侧补零。

```
x = 9 >>> 3; // x is equal to 1
```

## 赋值运算符

### 赋值 (=)

`=` 运算符是一个二元运算符，简单地用于给变量赋值。

```
x = 1; // x is equal to 1
```

赋值运算符和操作运算符用于简写。在下面的示例中，一行代码可以使用赋值操作运算符进行简写。

```
x = x + 20; // 使用赋值运算符 x += 20;
// 使用赋值运算符结果相同
```

和大多数简写约定一样，赋值运算符对初学者来说可能看起来很复杂。为了方便这些程序员，表 1-11 提供了简写运算符及其等效形式的示例。

| 简写运算符 | 示例 | 含义 |
|---|---|---|
| `+=` | `x += 2` | `x = x + 2` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 2` | `x = x * 2` |
| `/=` | `x /= 2` | `x = x / 2` |
| `%=` | `x %= 2` | `x = x % 2` |
| `<<=` | `x <<= 2` | `x = x << 2` |
| `>>=` | `x >>= 2` | `x = x >> 2` |
| `&=` | `x &= 2` | `x = x & 2` |
| `\|=` | `x \|= 2` | `x = x \| 2` |
| `^=` | `x ^= 2` | `x = x ^ 2` |
| `>>>=` | `x >>>= 2` | `x = x >>> 2` |

**表 1-11.** 赋值运算符简写

## 相等运算符

### 相等 (==)

`==` 运算符是一个二元运算符，用于比较两个值的相等性。如果两个值相等，则返回真；否则返回假。

```
x = (5 == 5); // x is true
x = (5 == "5"); // x is true
```

### 严格相等 (===)

`===` 运算符是一个二元运算符，用于比较两个值的相等性和类型。如果值和类型都相同，则返回真；否则返回假。

```
x = (5 === 5); // x is true
x = (5 === "5"); // x is false
```

### 不等于 (!=)

`!=` 运算符是一个二元运算符，用于比较两个值。如果两个值不相等，则返回真；否则返回假。

```
x = (5 != 5); // x is false
x = (5 != "5"); // x is true
```

### 严格不等于 (!==)

`!==` 运算符是一个二元运算符，用于比较两个值的相等性和类型。如果值或类型不同，则返回真；否则返回假。

```
x = (5 !== 5); // x is false
x = (5 !== "5"); // x is true
```

## 比较运算符

### 大于 (>)

`>` 运算符是一个二元运算符，用于比较两个值。如果第一个值大于第二个值，则返回真；否则返回假。

```
x = (5 > 3); // x is true
x = (5 > 5); // x is false
```

### 大于等于 (>=)

`>=` 运算符是一个二元运算符，用于比较两个值。如果第一个值大于或等于第二个值，则返回真；否则返回假。

```
x = (5 >= 3); // x is true
x = (5 >= 5); // x is true
```

### 小于 (<)

`<` 运算符是一个二元运算符，用于比较两个值。如果第一个值小于第二个值，则返回真；否则返回假。

```
x = (3 < 5); // x is true
x = (5 < 5); // x is false
```

### 小于等于 (<=)

`<=` 运算符是一个二元运算符，用于比较两个值。如果第一个值小于或等于第二个值，则返回真；否则返回假。

```
x = (3 <= 5); // x is true
x = (5 <= 5); // x is true
```

## 特殊运算符

### 条件运算符 (?:)

第一个操作数是一个表达式或变量，其求值为真或假。如果第一个操作数求为真，则返回第二个操作数的值。如果第一个操作数为假，则返回第三个操作数的值。

```
x = false;
y = (x ? "Red" : "Blue"); // y 等于 "Blue"
```

### typeof

一元运算符 `typeof` 返回其操作数的类型。它可以以两种方式编写：

`typeof x;`
或
`typeof(x);`

该运算符可以返回许多不同的值。表 1-12 列出了其中一些。

注意：`typeof` 在 JavaScript 1.1 及更高版本中可用。

| 值类型 | 返回字符串 |
| :--- | :--- |
| Undefined | `"undefined"` |
| Null | `"object"` |
| Boolean | `"boolean"` |
| Number | `"number"` |
| 大多数原生 JavaScript 对象 | `"function"` |
| 其他原生 JavaScript 对象 | `"object"` |
| 用户定义的对象 | 取决于实现 |

**表 1-12.** `typeof` 返回的值

### 对象创建运算符 (new)

该一元运算符接受一个操作数，即一个对象类型的名称。`new` 用于创建任何具有构造函数的 JavaScript 对象的实例。

```
x = new Date(); // x 是对 Date 对象的引用
```

### 删除运算符 (delete)

`delete` 运算符接受单个操作数，该操作数可以是对象的名称、对象的属性或数组中的元素。`delete` 尝试删除操作数。如果成功，它返回 `true`。如果失败，它返回 `false`。

```
x = new Date(); // x 是对 Date 对象的引用
y = delete x; // y 为 true，x 为 undefined
```

你可以使用 `delete` 删除对象属性，但不能删除用 `var` 创建的变量。请看下例。

```
x = new Number();
// x 是对 Number 对象的引用
x.value = 42;
// 创建属性 value，其等于 42
y = delete x.value;
// y 为 true，x.value 为 undefined
```

### 空运算符 (void)

`void` 运算符接受单个操作数，该操作数是一个表达式。该表达式会被求值但不返回值。

```
void(0);
```

### 逗号运算符 (,)

该运算符接受两个操作数，且都是表达式。它求值两个操作数并返回第二个操作数的值。它可以用作在同一行放置多个表达式的快捷方式。例如，以下几行代码

```
x = 1;
y = 2;
z = 3;
```

可以使用逗号运算符压缩为一行：

```
x = 1, y = 2, z = 3;
```

### 函数调用运算符 (())

`()` 运算符用于调用 JavaScript 函数。该运算符没有固定的操作数数量；其操作数数量取决于被调用的特定函数。

```
alert("Hello, World.");
history.go(-1);
```

### 对象访问运算符 (.)

`.` 运算符接受两个操作数——左侧是对象名称，右侧是属性或方法名称。`.` 运算符用于访问对象的属性和方法。

```
navigator.plugins[]
history.go()
document.URL
```

# 第 2 章 语句与控制结构

在本章中，我们将讨论语句和控制结构。这些是 JavaScript 的构建块。语句定义了 JavaScript 的布局，包括表达式语句、变量、函数等。控制结构让语句变得有用，因为它允许你根据条件执行某些操作，例如在 `if...else` 语句中，以及在循环（如 `for` 和 `while` 循环）中。

## 表达式语句

表达式语句为变量赋值值或执行一个函数。

```
greeting = "Welcome!"; // 此表达式为 greeting 赋值
alert(greeting); // 此表达式执行一个函数
```

## 复合语句

复合语句将你希望的任意数量的语句分组成一个语句块。

```javascript
{
  url = "http://www.yahoo.com";
  document.location = url;
}
```

## var

`var` 语句用于显式定义任意数量的变量。关键字 `var` 可以跟在任意由逗号分隔的变量之前，并可以带有初始值。

```javascript
var x = 42; // 定义了一个变量
var x = 42, y, dog = "poodle", win = window.name, z;
// 定义了 5 个变量
```

## function

函数语句用于定义函数，包括它的参数和函数体。函数可以有任意数量的由逗号分隔的参数。圆括号和大括号都是必需的。

```javascript
function doubleX() {
  x *= 2;
} // 此函数没有参数

function multiply(x, y) {
  var product = x * y;
  return product;
} // 此函数有两个参数
```

## return

`return` 语句用于指定函数执行时将返回什么值。

```javascript
function triple(number) {
  return number * 3;
}
```

## with

`with` 语句用于临时更改工作作用域。为了节省输入时间，例如，你可以编写以下代码：

```javascript
with(document) {
  if (color == "red") {
    backgroundColor = "red";
  }
}
```

## if 和 else

`if` 语句用于在条件为真时执行代码块。`else` 语句用于在条件为假时执行代码块。

```javascript
if (CarSize == "small") {
  // 小型汽车
  CarType = 'small';
  document.write("You drive a " + CarType + " car.");
} else {
  // 不是小型汽车
  CarType = 'large';
  document.write("You drive a " + CarType + " car.");
}
```

`if` 和 `else` 语句也可以嵌套在其他的 `if` 和 `else` 语句中。

```javascript
if (CarSize != "small") {
  if (CarSeats <= 4) {
    // 中型汽车不是小的，且有四个或更少的座椅
    CarSize = 'medium';
    document.write("You drive a " + CarSize + " car.");
  } else {
    CarSize = 'large';
    document.write("You drive a " + CarType + " car.");
  }
}
```

## else if

可以使用 `else if` 语句代替在其他 `if` 语句内部嵌套多个 `else` 语句。简单来说，`else if` 是一种编码快捷方法，用于减少嵌套语句的数量并缩短代码。如你所示，以下代码包含几个嵌套语句：

```javascript
if (CarSize == "small") {
    // 执行此语句块
    document.write("You drive a small car.");
} else {
    if (CarSize == "medium") {
        // 执行此语句块
        document.write("You drive a medium car.");
    } else {
        if (CarSize == "large") {
            // 执行此语句块
            document.write("You drive a large car.");
        }
    }
}
```

此脚本可以大幅缩短，从 16 行缩减到 12 行。使用 `else if` 语句而不是嵌套的 `else` 和 `if` 语句的另一个优势是，它让脚本对你和其他开发者来说更容易阅读。

```javascript
if (CarSize == "small") {
  // 执行此语句块
  document.write("You drive a small car.");
} else if (CarSize == "medium") {
  // 执行此语句块
  document.write("You drive a medium car.");
} else if (CarSize == "large") {
  // 执行此语句块
  document.write("You drive a large car.");
}
```

## switch

`switch` 语句仅仅是一个匹配和执行工具。它用于将表达式与各种 `case` 进行比较。如果表达式匹配某个 `case`，则执行该 `case` 的语句块。每个 `case` 的语句块可以以 `break` 结束；如果省略，则 `switch` 语句将继续执行下一个 `case`。`switch` 语句还可以以 `default` case 结束，如果没有其他任何 `case` 匹配表达式，则将执行该默认 `case`。

```javascript
switch (CarSize) {
  case "small":
    document.write("You drive a small car.");
    break;
  case "medium":
    document.write("You drive a medium car.");
    break;
  case "large":
    document.write("You drive a large car.");
    break;
  default:
    document.write("Your car is " + CarSize + " sized");
}
```

如你所示，前面的 `switch` 示例比本章较早显示的 `if` 和 `else` 语句看起来清晰得多。

## 循环

循环是持续执行直到满足特定条件的命令。JavaScript 中使用了几种循环语句：`for`、`while`、`do-while` 和 `for-in`。循环内部使用了标签（label）、`break` 和 `continue` 语句来增加功能。此外，`for-in` 语句用于对象操作。

### while

`while` 语句用于在条件为真时执行语句。

```javascript
valueA = 0;
valueB = 100;
while(valueA < valueB) {
  document.write("<br>" + valueA);
  valueA++;
}
```

此示例将打印数字 0 到 99，每个数字占一行。在每次语句执行期间，`valueA` 首先打印在一行，然后增加 1。在 `while` 语句执行后，我们返回到 `while` 语句，评估 `valueA` 是否小于 `valueB`。如果为真，则语句将反复执行，直到 `valueA` 大于 `valueB`。

### do-while

`do...while` 循环与 `while` 循环非常相似。它在条件为真时执行一个语句块，但条件测试发生在循环的底部。`do-while` 循环有助于确保语句至少执行一次。例如：

```javascript
valueA = 0;
valueB = 100;
do {
  document.write("<BR>" + valueB);
  valueB--;
} while (valueB != 0); // 此循环将循环 100 次
```

### for

`for` 循环可以用于受控制的循环。`for` 语句的第一行指定了三件事：一个可以声明或陈述的值、退出循环的条件，以及在循环每次迭代时执行的语句。

```javascript
valueA = 100;
for (valueB = 50; valueA < valueB; valueB++) {
  document.write("Current value is: " + valueB + "<br>");
}
```

### for-in

`for-in` 循环最适合用于数组，其中变量会自动递增，并且为数组中的每个元素执行一次循环。

```javascript
for (valueX in myArray) {
  document.write("myArray Item Number: " + valueX + "<BR>");
  document.write("myArray Item: " + myArray[valueX]);
}
```

### break 和 continue

`break` 和 `continue` 语句用于循环内部，以增加功能性。`break` 语句用于跳出循环，`continue` 语句用于跳过循环的剩余部分并直接进入下次迭代。

# 第 3 章 函数

## 定义函数

函数是可重用的代码块。你可以定义一个函数，然后在需要时调用它。

```javascript
function addbox(num) { return (height * width) * num; }
document.write("The combined area of my boxes is " + addbox(boxes) + " cubic inches");
}
Box(10, 12, 15);
```

// 这将显示以下行内容：
// 我的箱子总面积为 1800 立方英寸。

## 将函数当作数据进行操作

JavaScript 的一个强大之处在于，函数可以被当作数据进行操作。这允许 JavaScript 将函数视为任何数据值。例如，你可以先定义函数 `mySalary()`：

```javascript
var myRate = 5.33;
function mySalary(HoursWorked) { return myRate * HoursWorked; }
```

然后你可以在其他变量中使用该函数名，它将返回相应的属性。

```javascript
WeekPay = mySalary(40); // WeekPay = 213.2
DailyPay = mySalary(8); // DailyPay = 42.64
MonthlySalary = (DailyPay * 30); // MonthlySalary = 1279.2
YearlySalary = (WeekPay * 52); // YearlySalary = 11086.4
document.write("I make $" + YearlySalary + " per year");
```

## 方法与属性

函数是 JavaScript 对象的一种类型，即 `Function` 对象。正如此，它们自带某些预设的方法和属性。

### Call 对象

每个 JavaScript 函数都在一个局部作用域中执行，这与全局的、“脚本范围”作用域不同。通过将 Call 对象添加到作用域链的前端，可以创建一个函数作用域；你可以从函数体内部访问该对象的属性。该对象的属性包括局部变量以及函数的参数。此外，Call 对象还定义了 `arguments` 属性。

### arguments 属性

该属性指向 `arguments` 对象。`arguments` 对象包含两个有用的属性，并且可以当作数组使用，存储传递给函数的参数。`arguments[]` 数组允许你访问传递函数的所有参数，即使传递的参数数量多于或少于预期。传递给 `arguments[]` 数组的第一个参数可以通过 `arguments[0]` 访问。`length` 属性也可以配合 `arguments[]` 数组来确定包含的元素个数。

```javascript
function DOB(Month, Day, Year) {
  if (!arguments[0]) {
    alert("The DOB function is missing the month of birth");
    return null;
  }
  if (!arguments[1]) {
    alert("The DOB function is missing the day of birth");
    return null;
  }
  if (!arguments[2]) {
    alert("The DOB function is missing the year of birth");
    return null;
  }
  if (arguments.length > 3) {
    alert("The DOB function passed " + arguments.length + " arguments.");
    return null;
  }
  // 函数的实际体在此
}
```

Navigator 4 将 Call 对象和 `arguments` 对象合并为一个对象。在调用函数的 `arguments` 对象的 `toString()` 方法时，调用该方法返回字符串 `'[object Call]'`。

`arguments` 另外两个属性是 `callee` 和 `caller`。

#### callee 属性

`callee` 属性在 JavaScript 1.2 中实现。JavaScript 1.4 弃用了 `callee` 作为 `Function.arguments` 的属性，并将其保留为函数局部变量的属性。`arguments.callee` 属性只能在函数体中使用。`arguments.callee` 属性用于返回它所在的函数。

```javascript
function DisplayFunction() {
  return arguments.callee;
}
```

上述函数将返回其自身：

```javascript
function DisplayFunction() {
  return arguments.callee;
}
```

这对于递归操作非常有用。

```javascript
var x = 0;
function NumberList(x) {
  if (x < 10) {
    document.write(x);
    arguments.callee(x + 1);
  }
}
// 此函数将打印从 0 到 9 的每个数字
```

#### caller 属性

`arguments.caller` 属性在 JavaScript 1.1 中引入，并在 JavaScript 1.3 中弃用。与 `callee` 属性一样，`caller` 属性仅在函数体内可用。`caller` 属性返回调用它的函数名。

```javascript
function tester() {
  return arguments.callee;
}
function trythis() {
  tester();
}
// tester() 函数返回：trythis()
```

你也可以将 `callee` 和 `caller` 结合使用：`arguments.caller.callee`。该属性返回调用它的函数。

```javascript
function tester() {
  return arguments.caller;
}
function trythis() {
  tester();
}
// tester() 函数返回整个 trythis()
```

### length 和 arity

函数的 `length` 属性允许你获取函数期望的参数个数。例如，你可以定义一个 `multiply()` 函数，然后通过以下代码确认它期望的参数数量：

```javascript
function multiply(x, y) {
  return x * y;
}
document.write(multiply.length); // 返回 2
```

对于习惯在结构化更强的语言中编程的程序员来说，这可能需要一点时间适应，但 JavaScript 基于原型的结构为 Web 开发者提供了灵活性和易用性。

# 第 4 章 对象

## 定义对象

### 构造函数

任何带有构造函数的定义的对象都可以通过 `new` 语句创建。

```
myObject = new Object(); // 这条语句创建一个空的 JavaScript 对象
myName = new Date(); // 这条语句创建一个新的 Date 对象
```

你也可以定义自己的对象构造函数，并在程序的后续部分配合 `new` 语句使用。在这个示例中，我们定义了一个名为 `myCar` 的 Car 对象，并将品牌设置为 Toyota，颜色设为红色：

```javascript
function Car(m, c) { // 此函数定义了 Car 对象的构造函数
  this.make = m;
  this.color = c;
}
var myCar = new Car("Toyota", "red");
// 定义一个新的 Car 对象
document.write("My " + myCar.make + " is " + myCar.color);
// 这条语句写入 "My Toyota is red"
```

你还可以在构造函数中定义对象方法。首先定义将作为对象方法的函数，然后将它们赋值给对象，如下所示：

```javascript
function Car_increasePrice() { this.price += 100; }
function Car(m, p) { // 定义 Car 构造函数
  this.make = m;
  this.price = p;
  this.increasePrice = Car_increasePrice;
  // 定义一个方法
}
var myCar = new Car("Toyota", 1300);
myCar.increasePrice();
document.write("My car now costs $" + myCar.price);
// 这条语句写入 "My car now costs $1400"
```

### 对象字面量

在 JavaScript 1.2 及更高版本中，可以使用对象字面量来定义新对象。这样，你就可以无需先定义对象构造函数定义自己的新对象。要写对象字面量，只需声明对象名称，后面跟着括号内的属性名和值，用逗号分隔。

```javascript
var myCar = {
  make: "Toyota",
  price: 1300,
  color: "silver"
}; // 定义 myCar
```

### 垃圾回收

与 C 和 C++ 不同，JavaScript 具有自动垃圾回收机制，这意味着不需要定义析构函数来释放 JavaScript 对象和属性消耗的内存。然而，如果你想在代码中显式地清理一个对象，可以使用 `delete` 语句。

```
delete myObject; // 显式删除对象
```

### 对象超类

在 JavaScript 1.1 及更高版本中，每个 JavaScript 对象都基于 `Object` 原型。你可以通过声明 `Object` 原型的实例来在程序中创建空对象。

```javascript
var myObject = new Object(); // 定义了一个名为 myObject 的空对象
```

## 属性和方法

每个 JavaScript 对象都自动内置了一个属性和一些方法，因为它们包含在 `Object` 原型中。

### constructor 属性

该属性保存了用于创建对象的构造函数的引用。它可以用于测试；但当它被写为字符串时，它会返回构造函数的完整源码。

```javascript
var myCar = new Car("Toyota", 1300);
if (myCar.constructor == Car) // 注意单词 Car 没有加引号作为字符串
  document.write("The constructor is Car.<br>");
document.write(myCar.constructor);
// 将 Car 函数的 JavaScript 代码作为字符串输出
```

### toString()

当一个对象的 `toString()` 方法被执行时，它会返回对象的字符串表示。默认情况下，它返回调用它的对象的引用，这被翻译为字符串 `"[object Object]"` 通常没用。

```
document.write(myCar.toString()); // 输出 "[object Object]"
```

这种默认行为的例外出现在 Netscape 4 的 JavaScript 1.2 中。在这种情况下，`toString()` 返回对象方法和属性的名称和值。

```javascript
var myCar = new Object();
myCar.make = "Toyota";
myCar.price = 1300;
document.write(myCar.toString());
// 在几乎所有情况下返回 "[object Object]"
// 在 Netscape 4 的 JavaScript 1.2 中返回 "make: Toyota, price: 1300"
```

## 类层次结构

JavaScript 的类层次结构没有像 Java 和 C++ 这种基于类的编程语言那样高级。JavaScript 的类层次结构最多只有三层。首先，定义一个继承自 `Object` 超类的类。接着，声明该类的实例，完成了第三层。这里展示了我们的 `Car` 超类和 `myCar` 对象的代码。

```javascript
function Car(m, p) { // 定义 Car 构造函数
  this.make = m;
  this.price = p;
}
var myCar = new Car("Toyota", 1300); // myCar 处于第 3 层
```

# 第 5 章 核心对象与函数

本章概述了 JavaScript 的核心方法和对象。表 5-1 总结了这些核心对象和方法，并在后续章节中对每一个都进行了更详细的描述。

| 对象/方法 | 描述 | JavaScript 版本 | 备注 |
|---|---|---|---|
| `Array` | 基于对象的数组支持 | 1.1, ECMA-262 | |
| `Boolean` | 基于对象的布尔值支持 | 1.1, ECMA-262 | |
| `Date` | 支持日期 | 1.1, ECMA-262 | |
| `Math` | 包含数学常量和函数 | 1.0, ECMA-262 | 静态对象 |
| `Number` | 支持数字，包含 JavaScript 特有的常量数字 | 1.1, ECMA-262 | |
| `MIME` | 表示 MIME 类型 | 仅限 Netscape 3 及以上 | |
| `parseFloat` | 从字符串返回浮点数 | JavaScript 1.0, ECMA-262 | 静态方法 |
| `parseInt` | 从字符串返回整数 | JavaScript 1.0, ECMA-262 | 静态方法 |
| `RegExp` | 提供正则表达式支持 | JavaScript 1.2, ECMA-262 | |
| `String` | 提供字符串操作和使用的支持 | JavaScript 1.0, ECMA-262 | |

**表 5-1.** JavaScript 的核心对象与方法

尽管 JavaScript 1.0 支持了一些数组功能，但 `Array` 对象直到 JavaScript 1.1 才被引入。数组特性在 Netscape 4 和 ECMA-262 规范中都得到了增强。

## Array (数组)

`Array` 对象提供了数组的创建和操作功能。数组是值的有序集合。存储在数组中的值被称为*元素*（elements）。通过数组名称和索引数字来引用元素。数组索引从零开始计数，例如，名为 `a` 的数组的第三个元素将引用为 `a[2]`。

表 5-2 总结了 `Array` 对象中的方法和属性。

| 方法/属性 | 描述 | JavaScript 版本 | 备注 |
|---|---|---|---|
| `concat()` | 返回一个将参数作为新元素添加的数组 | 1.2, ECMA-262 | |
| `join()` | 返回一个数组元素连接成的字符串 | 1.1, ECMA-262 | |
| `length` | 提供数组长度的访问 | 1.1, Internet Explorer 3, ECMA-262 | 在 JavaScript 1.3 中增强 |
| `pop()` | 删除并返回数组的最后一个元素 | 仅限 Netscape 4 及以上 | |
| `push()` | 将值追加到数组末尾 | 仅限 Netscape 4 及以上 | |
| `reverse()` | 反转数组中元素的顺序 | 1.1, ECMA-262 | |
| `shift()` | 删除并返回数组的第一个元素 | 1.2, ECMA-262 | |
| `slice()` | 返回一个表示数组部分的新数组 | 1.2 | 在 Internet Explorer 4 中行为不同 |
| `sort()` | 按指定顺序对数组元素排序 | 1.1, ECMA-262 | |
| `splice()` | 从数组中删除数量的元素，并在删除值的位置插入值 | Netscape 4 及以上, ECMA-262 | 在 JavaScript 1.3 中增强 |
| `toSource()` | 返回一个表示数组源代码的字符串 | 1.2, ECMA-262 | |
| `toString()` | 返回一个表示数组内容的字符串 | JavaScript 1.1, ECMA-262 | Netscape 4 的返回值与其他不同 |
| `unshift()` | 在数组开头处插入新元素 | 仅限 Netscape 4 及以上 | |

**表 5-2.** Array 对象中可用的方法和属性

### 创建数组

在 JavaScript 中有三种创建新数组的方法。通常最好的方法是使用 `Array` 构造函数，但有些人倾向于使用 JavaScript 1.0 的方法为了向后兼容，并使用数组字面量为了方便。

#### Array 构造函数

要创建一个新的 `Array` 对象，可以使用 `new` 语句。如果你向 `Array` 构造函数不传递任何参数，将创建一个空数组。

```javascript
var a = new Array();
```

如果你向 `Array` 构造函数传递一个数字，将创建一个具有该长度的数组。

```javascript
var a = new Array(3);
```

如果你向 `Array` 构造函数传递多个参数，将创建一个包含这些值的数组。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
```

#### 数组字面量

数组字面量可以在不使用 `new` 语句的情况下定义数组。

```javascript
var a = ["Honda", "Toyota", "Ford"];
```

### 数组方法与属性

以下是 `Array` 对象可用方法和属性的描述。

#### concat()

`concat()` 方法接受任意数量的参数，将它们与数组合并并返回一个新数组。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
var b = a.concat("Mazda", "BMW"); // b 等于 ["Honda", "Toyota", "Ford", "Mazda", "BMW"]
```

#### join()

`join()` 方法返回数组元素连接成的字符串。你可以向 `join()` 传递一个可选参数，该字符串将用于分隔每个值。如果你不传递 `join()`，它将自动使用逗号分隔每个值。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
var s = a.join(); // s 等于 "Honda,Toyota,Ford"
var s = a.join("; "); // s 等于 "Honda; Toyota; Ford"
```

#### length

`length` 属性返回数组对象中的元素数量。长度在 JavaScript 1.1 及更高版本可用，并包含在 ECMA-262 规范中。在 JavaScript 1.3 和 ECMA-262 中，`length` 必须是一个小于 2³² 的正 32 位整数。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
var i = a.length; // i 等于 3
```

`length` 属性是可读可写的。将 `length` 的值设置为较小的值是从数组末尾删除元素的良好技巧。

```javascript
a.length = 2; // a 现在为 ["Honda", "Toyota"]
```

`length` 属性通常用于 `for` 循环来处理数组中的每个元素。

```javascript
var numbers = new Array(1, 2, 3);
for (var i = 0; i < numbers.length; i++) { numbers[i]++; } // numbers 现在包含 [2, 3, 4]
```

#### pop()

`pop()` 方法删除数组的最后一个元素并减少数组的长度。它不接受任何参数并返回被删除元素的值。`pop()` 仅在 Netscape 4 及更高版本可用。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
// a.length 等于 3
var x = a.pop();
// 数组 a 现在包含 ["Honda", "Toyota"]，其长度为 2
// x 等于 "Ford"
```

#### push()

`push()` 方法向现有 `Array` 对象的末尾添加新元素。它可以接受任意数量的参数，这些参数是需要添加到数组中的值。`push()` 返回数组的新长度。`push()` 仅在 Netscape 4 及更高版本可用。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
// a.length 等于 3
var x = a.push("Mazda", "BMW");
// 数组 a 现在包含 ["Honda", "Toyota", "Ford", "Mazda", "BMW"]
// x 和 a.length 都等于 5
```

`concat()` 方法也可以用于向数组末尾添加新值。

#### reverse()

`reverse()` 方法反转 `Array` 对象中数组元素的顺序。它不接受任何参数并返回该数组的引用。`reverse()` 在 JavaScript 1.1 中可用，并包含在 ECMA-262 规范中。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
var x = a.reverse();
// a 现在包含 ["Ford", "Toyota", "Honda"]
// x 包含 Array a 的引用
```

#### shift()

`shift()` 方法删除 `Array` 对象的第一个元素，将数组中的每个元素向下移动一个位置，并将长度减一。它不接受任何参数并返回被删除的元素。`shift()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
// a.length 等于 3
var x = a.shift();
// a 现在包含 ["Toyota", "Ford"]，且 a.length 等于 2
// x 等于 "Honda"
```

#### slice()

`slice()` 方法提取 `Array` 对象的一个部分并返回一个新的 `Array` 对象。它接受两个参数。第一个参数是开始选择切片的索引。如果这个数字是负数，则表示从数组末尾开始计算切片的元素数量。第二个参数是可选的。它指定了要选择的切片中最后一个数组元素之后的数组索引。如果没有提供此参数，切片将在数组的末尾结束。如果该数字指向的索引超出了数组末尾，选择也会在数组末尾停止。如果该数字是负数，则表示从数组末尾向前结束的元素数量。`slice()` 方法在 JavaScript 1.2 及更高版本可用。在 Internet Explorer 4 和 5 中，第一个参数不能为负数。

```javascript
var numbers = new Array(1, 2, 3, 4, 5, 6);
// 创建一个包含 [1,2,3,4,5,6] 的新数组
var numbers2 = numbers.slice(0, 3); // 从开始到索引 2 进行切片
// numbers2 包含 [1,2,3]
// numbers 仍然包含 [1,2,3,4,5,6]
var numbers3 = numbers.slice(2); // 从索引 2 到末尾进行切片
// numbers3 包含 [3,4,5,6]
// numbers 仍然包含 [1,2,3,4,5,6]
var numbers4 = numbers.slice(2, 4); // 从索引 2 到索引 3 进行切片
// numbers4 包含 [3,4]
// numbers 仍然包含 [1,2,3,4,5,6]
var numbers5 = numbers.slice(-2); // 从末尾倒数第 2 个元素开始切片
// numbers5 包含 [5,6]
// numbers 仍然包含 [1,2,3,4,5,6]
var numbers6 = numbers.slice(-3, -1); // 从末尾倒数第 3 个元素到倒数第 1 个元素进行切片
// numbers6 包含 [4,5]
// numbers 仍然包含 [1,2,3,4,5,6]
```

#### sort()

`sort()` 方法对 `Array` 对象中的元素进行排序。默认按字母顺序排序。它可以接受一个可选的函数，该函数定义了排序方式。`sort()` 返回排序后的数组引用。`sort()` 方法可以按照数字、字母或用户定义的函数对元素进行排序。它接受一个可选的比较函数。如果 a 小于 b，则返回一个负数；如果 a 大于 b，则返回一个正数；如果 a 等于 b，则返回零。`sort()` 方法在 JavaScript 1.1 中可用，并包含在 ECMA-262 规范中。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
var x = a.sort();
// a 现在包含 ["Ford", "Honda", "Toyota"]
// x 包含 Array a 的引用

function dSort(a, b) {
  if (a < b) { return -1; }
  if (a > b) { return 1; }
  return 0;
}
var a = new Array("Honda", "Toyota", "Ford");
a.sort(dSort);
// a 现在包含 ["Ford", "Honda", "Toyota"]

function dSortNumeric(a, b) {
  return (a - b);
}
var a = new Array(10, 5, 8);
// 创建一个包含 [10, 5, 8] 的数组 a
a.sort(dSortNumeric);
// a 现在包含 [5, 8, 10]
```

#### splice()

`splice()` 方法从 `Array` 对象中删除元素并插入新值。它至少接受一个参数：起始索引。第二个参数是可选的，指定要删除的元素数量。任何额外的参数都是要插入数组的值。`splice()` 方法在 JavaScript 1.2 及更高版本可用。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
a.splice(1, 1);
// a 现在包含 ["Honda", "Ford"]

var a = new Array("Honda", "Toyota", "Ford");
a.splice(1, 0, "Mazda");
// a 现在包含 ["Honda", "Mazda", "Ford"]

var a = new Array("Honda", "Toyota", "Ford");
a.splice(1, 2, "Mazda", "BMW");
// a 现在包含 ["Honda", "Mazda", "BMW"]
```

#### toString()

`toString()` 方法返回 `Array` 对象的字符串表示。它不接受参数。当数组被当作字符串处理时，会自动执行。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
document.write(a);
// 输出 "Honda,Toyota,Ford"
```

#### toSource()

`toSource()` 方法返回代表 `Array` 对象的数组字面量。它在 JavaScript 1.2 及更高版本可用。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a
var s = a.toSource();
// s 等于 '["Honda", "Toyota", "Ford"]'
```

#### unshift()

`unshift()` 方法将一组值插入到 `Array` 对象的开头。它接受任意数量的参数并返回数组的新长度。`unshift()` 仅在 Netscape 4 及更高版本可用。

```javascript
var a = new Array("Honda", "Toyota", "Ford");
// 创建一个包含 ["Honda", "Toyota", "Ford"] 的数组 a，长度为 3
var x = a.unshift("Mazda");
// a 现在包含 ["Mazda", "Honda", "Toyota", "Ford"]，且 a.length 等于 4
```

### 多维数组

JavaScript 原生不支持多维数组，但它支持数组数组，你可以借此模拟多维数组。在下面的示例中，我们可以创建一个伪多维数组来存储不同部门的虚构员工。

```javascript
var employees = new Array(3);
// 创建空的 employees 数组并加载数组
employees[0] = new Array("Julie", "Joe", "Richard", "Emma");
employees[1] = new Array("Ann", "Chandra", "Eddy");
employees[2] = new Array("Mark", "Rhonda", "Paulina");
// 访问存储的值
document.write(employees[0][3]);
// 输出 "Emma"
document.write(employees[2][1]);
// 输出 "Rhonda"
// 访问 employees 内的数组
document.write(employees[1]);
// 输出 "Ann,Chandra,Eddy"
```

## Boolean (布尔)

`Boolean` 对象提供了对布尔值、true/false 值的支持。`Boolean` 是 JavaScript 中的基本数据类型。`Boolean` 对象在 JavaScript 1.1 及更高版本可用，并包含在 ECMA-262 规范中。`Boolean` 对象提供了一个方法：

| 方法 | 描述 | JavaScript 版本 | 备注 |
| :--- | :--- | :--- | :--- |
| `toString()` | 返回 "true" 或 "false" | 1.1 | 不需要显式调用 |

### 创建布尔对象和值

布尔对象可以显式或隐式地创建。

#### Boolean 构造函数

虽然没有必要显式创建 `Boolean` 对象，但可以使用 `new` 语句来创建一个。`Boolean` 构造函数接受一个参数，该参数可以是任何值。除了特殊值 `true` 和 `false` 外，该值将根据其自身的值确定为 `true` 或 `false`。值为 0、空字符串、`NaN`、`null` 或 `undefined` 的值都被转换为 `false`。非零值被转换为 `true`。

以下 `Boolean` 对象将求值为 `false`：

```javascript
var b = new Boolean(0);
var b = new Boolean(false);
var b = new Boolean(null);
var b = new Boolean(NaN);
var b = new Boolean(undefined);
var b = new Boolean("");
```

以下 `Boolean` 对象将求值为 `true`：

```javascript
var b = new Boolean(true);
var b = new Boolean("false");
var b = new Boolean(42);
var b = new Boolean(-42);
var b = new Boolean("The quick brown fox...");
```

此外，你可以在不使用 `new` 语句的情况下使用 `Boolean` 构造函数来简单地评估并返回 `true` 或 `false`。

```javascript
var boolean_test = Boolean(42); // boolean_test 等于 true
var boolean_test = Boolean(""); // boolean_test 等于 false
```

#### 隐式创建布尔

你不需要显式创建 `Boolean` 对象即可访问其属性和方法。可以这样创建一个原始布尔值：

```javascript
var b = false; // 将 b 设置为 false
var b = true; // 将 b 设置为 true
```

### Boolean 方法

`Boolean` 对象仅有一个方法 `toString()`。以下是 `toString()` 方法的描述。

#### toString()

`toString()` 方法根据 `Boolean` 对象的值返回字符串 `"true"` 或 `"false"`。通常没有必要显式调用 `toString()`，因为当 `Boolean` 对象被视为字符串时，它会被自动调用。`toString()` 在 JavaScript 1.1 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var b = new Boolean(42);
// 创建一个 Boolean 对象，b 设置为 true
var s = new String(b.toString());
// 将 s 设置为 "true"
document.write(b.toString());
// 显式调用 toString() 写入 "true"
document.write(b);
// 隐式调用 toString() 写入 "true"
```



# 日期 (Date)

`Date` 对象允许你使用和操作日期与时间。它在 JavaScript 1.0 及更高版本可用，某些功能在 JavaScript 1.1 和 1.2 中得到了增强。`Date` 对象包含在 ECMA-262 规范中。

JavaScript 内部使用毫秒格式表示日期，即从给定日期到 1970 年 1 月 1 日 GMT（格林威治时间）午夜之间的毫秒数。

表 4-3 总结了 `Date` 对象中的方法。

| 方法 | 描述 | JavaScript 版本 | 备注 |
|---|---|---|---|
| `getDate()` | 访问 Date 对象的每月几号 | 1.0, ECMA-262 | |
| `getDay()` | 访问 Date 对象的星期 | 1.0, ECMA-262 | |
| `getFullYear()` | 访问 Date 对象的四位年份 | 1.2, ECMA-262 | |
| `getHours()` | 访问 Date 对象的小时 | 1.0, ECMA-262 | |
| `getMilliseconds()` | 访问 Date 对象的毫秒 | 1.2, ECMA-262 | |
| `getMinutes()` | 访问 Date 对象的分钟 | 1.0, ECMA-262 | |
| `getMonth()` | 访问 Date 对象的月份 | 1.0, ECMA-262 | |
| `getSeconds()` | 访问 Date 对象的秒 | 1.0, ECMA-262 | |
| `getTime()` | 访问毫秒格式的 Date 对象 | 1.0, ECMA-262 | |
| `getTimezoneOffset()` | 访问本地时间与 GMT 之间的分钟偏移量 | 1.2, ECMA-262 | |
| `getUTCDate()` | 访问 UTC 下 Date 对象的每月几号 | 1.2, ECMA-262 | |
| `getUTCDay()` | 访问 UTC 下 Date 对象的星期 | 1.2, ECMA-262 | |
| `getUTCFullYear()` | 访问 UTC 下 Date 对象的四位年份 | 1.2, ECMA-262 | |
| `getUTCHours()` | 访问 UTC 下 Date 对象的小时 | 1.2, ECMA-262 | |
| `getUTCMilliseconds()` | 访问 UTC 下 Date 对象的毫秒 | 1.2, ECMA-262 | |
| `getUTCMinutes()` | 访问 UTC 下 Date 对象的分钟 | 1.2, ECMA-262 | |
| `getUTCMonth()` | 访问 UTC 下 Date 对象的月份 | 1.2, ECMA-262 | |
| `getUTCSeconds()` | 访问 UTC 下 Date 对象的秒 | 1.2, ECMA-262 | |
| `getYear()` | 访问 Date 对象的两位年份 | 1.0, ECMA-262 | 可能导致错误；在 JavaScript 1.2 中弃用 |
| `parse()` | 返回毫秒格式的日期 | 1.0, ECMA-262 | 静态方法 |
| `setDate()` | 设置 Date 对象的每月几号 | 1.0, ECMA-262 | 在 JavaScript 1.2 中增强 |
| `setFullYear()` | 设置 Date 对象的四位年份 | 1.2, ECMA-262 | |
| `setHours()` | 设置 Date 对象的小时 | 1.0, ECMA-262 | 在 JavaScript 1.2 中增强 |
| `setMilliseconds()` | 设置 Date 对象的毫秒 | 1.2, ECMA-262 | |
| `setMinutes()` | 设置 Date 对象的分钟 | 1.0, ECMA-262 | 在 JavaScript 1.2 中增强 |
| `setMonth()` | 设置 Date 对象的月份 | 1.0, ECMA-262 | 在 JavaScript 1.2 中增强 |
| `setSeconds()` | 设置 Date 对象的秒 | 1.0, ECMA-262 | 在 JavaScript 1.2 中增强 |
| `setTime()` | 使用毫秒格式设置 Date 的日期 | 1.0, ECMA-262 | |
| `setUTCDate()` | 设置 UTC 下 Date 对象的每月几号 | 1.2, ECMA-262 | |
| `setUTCFullYear()` | 设置 UTC 下 Date 对象的四位年份 | 1.2, ECMA-262 | |
| `setUTCHours()` | 设置 UTC 下 Date 对象的小时 | 1.2, ECMA-262 | |
| `setUTCMilliseconds()` | 设置 UTC 下 Date 对象的毫秒 | 1.2, ECMA-262 | |
| `setUTCMinutes()` | 设置 UTC 下 Date 对象的分钟 | 1.2, ECMA-262 | |
| `setUTCMonth()` | 设置 UTC 下 Date 对象的月份 | 1.2, ECMA-262 | |
| `setUTCSeconds()` | 设置 UTC 下 Date 对象的秒 | 1.2, ECMA-262 | |
| `setYear()` | 设置 Date 对象的年份 | 1.0, ECMA-262 | |
| `toGMTString()` | 返回 GMT 下的 Date 对象字符串表示 | 1.0, ECMA-262 | 在 JavaScript 1.2 中弃用；IE 和 Netscape 间不一致 |
| `toLocaleString()` | 返回本地时间的 Date 对象字符串表示 | 1.0, ECMA-262 | |
| `toString()` | 返回 Date 对象的字符串表示 | 1.1, ECMA-262 | |
| `toUTCString()` | 返回 UTC 下的 Date 对象字符串表示 | 1.2, ECMA-262 | IE 和 Netscape 间不一致 |
| `valueOf()` | 返回毫秒格式的日期 | 1.1, ECMA-262 | |
| `UTC()` | 根据日期参数返回毫秒格式的日期 | 1.0, ECMA-262 | 在 JavaScript 1.2 中增强 |

## Date 构造函数

要创建一个新的 `Date` 对象，可以使用 `new` 语句。如果你不向 `Date()` 传递任何参数，则你将创建一个设置为当前日期时间的新 `Date` 对象。

```javascript
var today = new Date();
// today 设置为当前日期时间
```

你也可以将日期传递给 `Date` 构造函数，为你的新 `Date` 对象设置特定的日期和时间。

你可以通过向 `Date` 构造函数传递日期规范，创建一个设置为 2001 年 7 月 1 日星期日 12:00:00 AM 的 `Date` 对象（见本节后文“参数”）。

```javascript
var myFunction = new Date(2001, 06, 01, 0, 0, 0);
// 创建新日期：2001 年 7 月 1 日星期日 12:00:00 AM
```

小时、分钟、秒和毫秒参数是可选的。你可以省略它们来创建相同的日期。

```javascript
var myFunction = new Date(2001, 06, 01);
// 创建新日期：2001 年 7 月 1 日星期日 12:00:00 AM
```

或者你可以简单地传递一个参数——毫秒，创建一个与 1970 年 1 月 1 日 GMT 午夜相关的日期。

```javascript
var myFunction = new Date(3000);
// 创建新日期：1970 年 1 月 1 日星期四 12:00:03 AM
```

### 参数

表 4-4 列出了按此顺序传递给 `Date` 构造函数的参数：年、月、日、小时、分钟、秒、毫秒。

在 JavaScript 1.0 和 1.1 中，`Date` 构造函数会忽略毫秒。

| 参数 | 说明 | 示例 |
|---|---|---|
| year | 年份是一个四位数，用于精确设置日期。两位数的年份会将日期设置为 1900 与该年份之和。 | 2001 等于 2001，01 等于 1901 |
| month | 月份是 0 到 11 之间的整数。 | 0 代表 1 月，11 代表 12 月 |
| day | 日是 1 到 31 之间的整数。 | 15 代表 15 号，0 代表上个月的最后一天。 |
| hour | 小时是 0 到 23 之间的整数。该参数是可选的。 | 0 代表凌晨 12:00，14 代表下午 2:00 或 14:00 |
| minute | 分钟是 0 到 59 之间的整数。该参数是可选的。 | 45 代表该小时后的 45 分 |
| second | 秒是 0 到 59 之间的整数。该参数是可选的。 | 45 代表该分钟后的 45 秒 |
| millisecond | 毫秒应该是 0 到 999 之间的整数。单独将毫秒传递给 `Date` 构造函数会将日期设置为 GMT 1970 年 1 月 1 日午夜加上指定的毫秒数。毫秒是可选的，且只能在 JavaScript 1.2 及更高版本中使用。在其他版本的 JavaScript 中，毫秒会被忽略。 | 300 代表 0.3 秒，3000 代表 3 秒，`Date(2000)` 将日期设置为 GMT 时间 1970 年 1 月 1 日星期四凌晨 12:00:03 |

## Date 方法

以下是 `Date` 对象中可用于日期的方法说明。

### getDate()

`getDate()` 方法返回 `Date` 对象的每月几号。这将是一个 1 到 31 之间的整数。

`getDate()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25); // 将日期设置为 2001 年 12 月 25 日
var day = d.getDate(); // day 等于 25。
```

### getDay()

`getDay()` 方法返回 `Date` 对象的星期几。这将是一个 0 到 6 之间的整数，其中 0 代表星期日，6 代表星期六。

`getDay()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25); // 将日期设置为 2001 年 12 月 25 日
var day = d.getDay(); // day 等于 2，代表星期二。
```

### getFullYear()

`getFullYear()` 方法返回 `Date` 对象的四位年份，用执行代码的系统本地时间表示。

`getFullYear()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25); // 将日期设置为 2001 年 12 月 25 日
var year = d.getFullYear(); // year 等于 2001
```

### getHours()

`getHours()` 方法返回 `Date` 对象的小时——一个 0 到 23 之间的整数。

`getHours()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 0);
// d 被设置为 2001 年 12 月 25 日 凌晨 6:30
var hour = d.getHours(); // hour 等于 6
```

### getMilliseconds()

`getMilliseconds()` 方法返回 `Date` 对象的毫秒。

`getMilliseconds()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 0, 20);
// d 被设置为 2001 年 12 月 25 日 凌晨 6:30:00.020
var ms = d.getMilliseconds();
// ms 等于 20。
```

### getMinutes()

`getMinutes()` 方法返回 `Date` 对象的分钟。

`getMinutes()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 0, 20);
// d 被设置为 2001 年 12 月 25 日 凌晨 6:30:00.020
var min = d.getMinutes();
// min 等于 30。
```

### getMonth()

`getMonth()` 方法返回 `Date` 对象的月份——一个从 0（1 月）到 11（12 月）的整数。

`getMonth()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25);
// d 被设为 2001 年 12 月 25 日
var month = d.getMonth();
// month 等于 11，代表 12 月。
```

### getSeconds()

`getSeconds()` 方法返回 `Date` 对象的秒——一个 0 到 59 之间的整数。

`getSeconds()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 10);
// d 被设为 2001 年 12 月 25 日 6:30:10
var sec = d.getSeconds();
// sec 等于 10
```

### getTime()

`getTime()` 返回毫秒格式的日期。这是 `Date` 对象到 1970 年 1 月 1 日午夜之间的毫秒数。日期的毫秒表示可以创建一个 `Date` 对象。

`getTime()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25);
// d 被设为 2001 年 12 月 25 日
var gTime = d.getTime();
// gTime 等于 97525400000
```

### getTimezoneOffset()

`getTimezoneOffset()` 方法返回格林威治时间 (GMT) 与执行代码计算机本地时间之间的分钟差。

`getTimezoneOffset()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var d = new Date();
var o = d.getTimezoneOffset();
// 在东部时间 (EST) 下执行时 o 等于 300。
```

### getUTCDate()

`getUTCDate()` 方法返回通用时间 (UTC) 的每月几号。UTC 与 GMT 基本相同。每月几号是一个 1 到 31 之间的整数。

`getUTCDate()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25);
// d 被设为 2001 年 12 月 25 日 凌晨 12:00（默认）
var uDate = d.getUTCDate();
// uDate 等于 25
```

### getUTCDay()

`getUTCDay()` 方法返回通用时间 (UTC) 的星期几。UTC 与 GMT 基本相同。星期是一个 0 到 6 之间的整数。

`getUTCDay()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25);
// d 被设为 2001 年 12 月 25 日 凌晨 12:00（默认）
var uDay = d.getUTCDay();
// uDay 等于 2，代表星期二。
```

### getUTCFullYear()

`getUTCFullYear()` 方法返回 `Date` 对象的四位年份，用通用时间 (UTC) 表示。UTC 与 GMT 基本相同。

`getUTCFullYear()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25);
// d 被设为 2001 年 12 月 25 日 凌晨 12:00 本地时间（默认）
var uYear = d.getUTCFullYear();
// uYear 等于 2001
```

### getUTCHours()

`getUTCHours()` 方法返回 `Date` 对象的小时——用通用时间 (UTC) 表示的 0 到 23 之间的整数。UTC 与 GMT 基本相同。

`getUTCHours()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 0);
// d 被设为 2001 年 12 月 25 日 凌晨 6:30
var uHour = d.getUTCHours();
// 在东部时间 (EST) 下执行时 uHour 等于 11。
```

### getUTCMilliseconds()

`getUTCMilliseconds()` 方法返回通用时间 (UTC) 下 `Date` 对象的毫秒。UTC 与 GMT 基本相同。

`getUTCMilliseconds()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 0, 20);
// d 被设置为 2001 年 12 月 25 日 凌晨 6:30:00.020
var uMS = d.getUTCMilliseconds();
// uMS 等于 20。
```

### getUTCMinutes()

`getUTCMinutes()` 方法返回通用时间 (UTC) 下 `Date` 对象的分钟。UTC 与 GMT 基本相同。

`getUTCMinutes()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 0, 20);
// d 被设置为 2001 年 12 月 25 日 6:30:00.020
var uMin = d.getUTCMinutes();
// uMin 等于 30。
```

### getUTCMonth()

`getUTCMonth()` 方法返回通用时间 (UTC) 下 `Date` 对象的月份——一个从 0（1 月）到 11（12 月）的整数。UTC 与 GMT 基本相同。

`getUTCMonth()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25);
// d 被设为 2001 年 12 月 25 日
var uMonth = d.getUTCMonth();
// uMonth 等于 11，代表 12 月。
```

### getUTCSeconds()

`getUTCSeconds()` 方法返回通用时间 (UTC) 下 `Date` 对象的秒。

`getUTCSeconds()` 在 JavaScript 1.2 及更高版本中可用。

```javascript
var d = new Date(2001, 11, 25, 6, 30, 10);
// d 被设为 2001 年 12 月 25 日 6:30:10
var uSec = d.getUTCSeconds();
// uSec 等于 10
```

### parse()

`Date.parse()` 方法将解析包含日期和时间的字符串，并返回毫秒格式的日期。以下是一个适用于 `Date.parse()` 的合适参数示例：

`Tue, 25 Dec 2001 05:00:00 UTC`

这种字符串是通过执行 `Date.toGMTString()` 创建的。一旦生成了日期的毫秒表示，就可以用它创建一个新的 `Date` 对象。

`Date.parse()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var date = d.toGMTString();
// date 等于 "Tue, 25 Dec 2001 05:00:00"
var i = Date.parse(date);
// i 等于 1009256400000
var d2 = new Date(i);
// d2 被设置为 2001 年 12 月 25 日
```

注意 `Date.parse()` 是一个静态方法，这意味着它只能从 `Date` 超类执行，而不能从 `Date` 实例执行。在前面的代码中，例如，不能执行 `d.parse()`，只能执行 `Date.parse()`。

### setDate()

`setDate()` 方法设置 `Date` 对象的日期。它接收一个参数，一个 1 到 31 之间的整数。

在 JavaScript 1.2 及更高版本中，此方法返回毫秒格式的新日期。在 JavaScript 1.0 和 1.1 中，它不返回任何值。

`setDate()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setDate(26);
// 日期现在是 26
// 在 JavaScript 1.2 及更高版本中，i 等于 1009342800000
```

### setFullYear()

`setFullYear()` 方法设置 `Date` 对象的四位年份。它接受一个参数，一个四位整数，并返回毫秒格式的新日期。

`setFullYear()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setFullYear(2002);
// 年份现在设置为 2002，且 i 等于 1040792400000
```

### setHours()

`setHours()` 方法设置 `Date` 对象的小时。它接受一个参数，一个从 0（午夜）到 23（晚上 11:00）的整数。

在 JavaScript 1.2 及更高版本中，`setHours()` 返回毫秒格式的新日期。在 JavaScript 1.0 和 1.1 中，`setHours()` 不返回任何值。

`setHours()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setHours(6);
// d 的时间现在设置为凌晨 6:00:00
// 在 JavaScript 1.2 及更高版本中，i 等于 1009278000000
```

### setMilliseconds()

`setMilliseconds()` 方法设置 `Date` 对象中时间的毫秒数。它接受一个参数，一个应该是 0 到 999 之间的整数。`setMilliseconds()` 返回毫秒格式的已调整的日期。

`setMilliseconds()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setMilliseconds(500);
// d 的时间现在设置为凌晨 12:00:00.500，且 i 等于 1009256400500
```

### setMinutes()

`setMinutes()` 方法设置 `Date` 对象中时间的分钟。它接受一个参数，一个应该是 0 到 59 之间的整数。

在 JavaScript 1.2 及更高版本中，`setMinutes()` 返回毫秒格式的新日期。在 JavaScript 1.0 和 1.1 中，`setMinutes()` 不返回任何值。

`setMinutes()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setMinutes(30);
// d 的时间现在设置为凌晨 12:30:00，且 i 等于 1009258200000
```

### setMonth()

`setMonth()` 方法设置 `Date` 对象的月份。它传递一个参数，一个从 0（一月）到 11（十二月）的整数。

在 JavaScript 1.2 及更高版本中，`setMonth()` 返回毫秒格式的新日期。在 JavaScript 1.0 和 1.1 中，`setMonth()` 不返回任何值。

`setMonth()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setMonth(0);
// 月份现在设置为 0，且 i 等于 978307200000
```

### setSeconds()

`setSeconds()` 方法设置 `Date` 对象中时间的秒数。它接受一个参数，一个应该是 0 到 59 之间的整数。

在 JavaScript 1.2 及更高版本中，`setSeconds()` 返回毫秒格式的新日期。在 JavaScript 1.0 和 1.1 中，`setSeconds()` 不返回任何值。

`setSeconds()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setSeconds(30);
// d 的时间现在设置为凌晨 12:00:30
// i 等于 1009256430000
```

### setTime()

`setTime()` 方法设置 `Date` 对象的日期。它接受一个参数，一个毫秒格式的整数。

`setTime()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setTime(1009256400000);
// d 被设置为 2001 年 12 月 25 日
```

### setUTCDate()

`setUTCDate()` 方法设置 UTC 下 `Date` 对象的每月几号。它接受一个参数，一个 1 到 31 之间的整数。

`setUTCDate()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setUTCDate(26);
// 日期现在是 26
// 在 JavaScript 1.2 及更高版本中，i 等于 1009342800000
```

### setUTCFullYear()

`setUTCFullYear()` 方法设置 UTC 下 `Date` 对象的四位年份。它接受一个参数，一个四位整数，并返回毫秒格式的新日期。

`setUTCFullYear()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setUTCFullYear(2002);
// 年份现在设置为 2002，且 i 等于 1040864400000
```

### setUTCHours()

`setUTCHours()` 方法设置 UTC 下 `Date` 对象的小时。它接受一个参数，一个从 0（午夜）到 23（晚上 11:00）的整数。

`setUTCHours()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setUTCHours(6);
// d 的时间现在设置为凌晨 6:00:00 UTC
// 在 JavaScript 1.2 及更高版本中，i 等于 1009256400000
```

### setUTCMilliseconds()

`setUTCMilliseconds()` 方法设置 UTC 下 `Date` 对象的毫秒。它接受一个参数，一个 0 到 999 之间的整数。

`setUTCMilliseconds()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setUTCMilliseconds(500);
// d 的时间现在设置为凌晨 12:00:00.500 UTC
```

### setUTCMinutes()

`setUTCMinutes()` 方法设置 UTC 下 `Date` 对象的分钟。它接受一个参数，一个 0 到 59 之间的整数。

`setUTCMinutes()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日，凌晨 12:00:00
var i = d.setUTCMinutes(30);
// d 的时间现在设置为凌晨 12:30:00 UTC
```

### setUTCMonth()

`setUTCMonth()` 方法设置 UTC 下 `Date` 对象的月份。它接受一个参数，一个从 0（一月）到 11（十二月）的整数。

`setUTCMonth()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setUTCMonth(0);
// 月份现在设置为 0
```

### setUTCSeconds()

`setUTCSeconds()` 方法设置 UTC 下 `Date` 对象的秒。它接受一个参数，即在 0 到 59 之间的整数。

`setUTCSeconds()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 默认将 d 设置为 2001 年 12 月 25 日 凌晨 12:00:00
var i = d.setUTCSeconds(30);
// d 的时间现在设置为 12:00:30 UTC
// 在 JavaScript 1.2 及更高版本中，i 等于 1009256430000
```

### setYear()

`setYear()` 方法设置 `Date` 对象的年份。它接受一个参数，四位数格式的年份，或者 1899 年之后 2000 年之前的两位格式年份。

在 JavaScript 1.2 及更高版本中，`setYear()` 返回毫秒格式的新日期。在 JavaScript 1.0 和 1.1 中，`setYear()` 不返回任何内容。

`setYear()` 引入于 JavaScript 1.0，并在 JavaScript 1.2 中被弃用，取而代之的是 `setFullYear()`。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.setYear(92);
// 年份现在设置为 1992
// 在 JavaScript 1.2 及后续版本中，i 等于 725259600000
var i = d.setYear(2002);
// 年份现在设置为 2002
// 在 JavaScript 1.2 及后续版本中，i 等于 1040792400000
```

### toGMTString()

`toGMTString()` 方法返回格林尼治时间 (GMT) 的 `Date` 对象的字符串表示。

`toGMTString()` 有一个异常的不一致。Netscape 和早期版本的 Internet Explorer 在日期字符串末尾打印“GMT”，而 Internet Explorer 4 在字符串末尾打印“UTC”。

`toGMTString()` 引入于 JavaScript 1.0，并在 JavaScript 1.2 中被弃用，取而代之的是 `toUTCString()`。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var dString = d.toGMTString();
// dString 等于 "Tue, 25 Dec 2001 05:00:00 UTC" (IE 4)
// 或 "Tue, 25 Dec 2001 05:00:00 GMT" (Netscape)
```

### toLocaleString()

`toLocaleString()` 方法使用执行代码的计算机的本地时区以及日期时间格式返回 `Date` 对象的字符串表示。由于世界各地日期时间格式差异巨大，这可能会根据执行位置的不同产生不同的结果。

`toLocaleString()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var dString = d.toLocaleString();
// dString 等于 "12/25/2001 00:00:00 in EST"
```

### toString()

`toString()` 方法使用执行代码的计算机的本地时区返回 `Date` 对象的字符串表示。日期的格式取决于实现，因为它并不一定使用本地的日期时间格式。由于此，该方法的结果可能差异很大。

`toString()` 在 JavaScript 1.1 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var dString = d.toString();
// dString 等于 "Tue Dec 25 00:00:00 EST 2001" (IE 4) 或
// "Tue Dec 25 00:00:00 GMT-0500 (Eastern Standard Time) 2001" (Netscape)
```

### toUTCString()

`toUTCString()` 方法返回转换为协调世界时间 (UTC) 的 `Date` 对象的字符串表示。

`toUTCString()` 有一个异常的不一致。Netscape 和早期版本的 Internet Explorer 在日期末尾打印“GMT”，而 Internet Explorer 4 在字符串末尾打印“UTC”。

`toUTCString()` 在 JavaScript 1.2 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25); // 将 d 设置为 2001 年 12 月 25 日
var dString = d.toUTCString();
// dString 等于 "Tue, 25 Dec 2001 05:00:00 UTC" (IE 4) 或
// "Tue, 25 Dec 2001 05:00:00 GMT" (Netscape)
```

### valueOf()

`valueOf()` 方法返回 `Date` 对象的毫秒表示。这是 `Date` 对象的日期与 GMT 1970 年 1 月 1 日午夜之间的毫秒数。`valueOf()` 的行为与 `getTime()` 相同。

日期的毫秒表示可用于创建一个新的 `Date` 对象。

`valueOf()` 在 JavaScript 1.1 及更高版本可用。

```javascript
var d = new Date(2001, 11, 25);
// 将 d 设置为 2001 年 12 月 25 日
var i = d.valueOf();
// i 等于 1009256400000
var d2 = new Date(i);
// d2 设置为 2001 年 12 月 25 日
```

### UTC()

`Date.UTC()` 将参数转换为毫秒格式的日期。这些参数与传递给 `Date` 构造函数的参数相同。参数顺序为：年、月、日、小时、分钟、秒、毫秒。毫秒参数在 JavaScript 1.0 和 1.1 中被忽略。

`Date.UTC()` 在 JavaScript 1.0 及更高版本可用。

```javascript
var i = Date.UTC(2001, 11, 25, 0, 0, 0); // 等于 1009256400000
var d = new Date(i); // d 设置为 2001 年 12 月 25 日 00:00:00
```

# Math

`Math` 对象包含了常量和函数。它是静态对象，意味着你不能通过构造函数创建 `Math` 实例。`Math` 对象的所有方法和属性都是只读的。`Math` 对象在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 标准中。

### 表 4-5. Math 方法

| 方法 | 描述 | JavaScript 版本 | 备注 |
| :--- | :--- | :--- | :--- |
| `abs()` | 计算绝对值 | 1.0, ECMA-262 | 静态方法 |
| `acos()` | 计算反余弦 | 1.0, ECMA-262 | 静态方法 |
| `asin()` | 计算反正弦 | 1.0, ECMA-262 | 静态方法 |
| `atan()` | 计算反正切 | 1.0, ECMA-262 | 静态方法 |
| `atan2()` | 计算从 X 轴到点的角度 | 1.0, ECMA-262 | 静态方法 |
| `ceil()` | 向上取整 | 1.0, ECMA-262 | 静态方法 |
| `cos()` | 计算余弦 | 1.0, ECMA-262 | 静态方法 |
| `exp()` | 计算 e 的指数 | 1.0, ECMA-262 | 静态方法 |
| `floor()` | 向下取整 | 1.0, ECMA-262 | 静态方法 |
| `log()` | 计算自然对数 | 1.0, ECMA-262 | 静态方法 |
| `max()` | 比较两个数字，返回较大的 | 1.0, ECMA-262 | 静态方法 |
| `min()` | 比较两个数字，返回较小的 | 1.0, ECMA-262 | 静态方法 |
| `pow()` | 计算数字的指定幂 | 1.0, ECMA-262 | 静态方法 |
| `random()` | 返回随机数 | 1.0, ECMA-262 | 静态方法 |
| `round()` | 将数字四舍五入到整数 | 1.0, ECMA-262 | 静态方法 |
| `sin()` | 计算正弦 | 1.0, ECMA-262 | 静态方法 |
| `sqrt()` | 计算平方根 | 1.0, ECMA-262 | 静态方法 |
| `tan()` | 计算正切 | 1.0, ECMA-262 | 静态方法 |

### 表 4-5. Math 对象属性（续）

| 属性 | 描述 | JavaScript 版本 | 备注 |
| :--- | :--- | :--- | :--- |
| `E` | e，自然对数的底 | 1.0, ECMA-262 | 只读，静态 |
| `LN10` | 10 的自然对数 | 1.0, ECMA-262 | 只读，静态 |
| `LN2` | 2 的自然对数 | 1.0, ECMA-262 | 只读，静态 |
| `LOG2E` | 以 2 为底的 e 的对数 | 1.0, ECMA-262 | 只读，静态 |
| `LOG10E` | 以 10 为底的 e 的对数 | 1.0, ECMA-262 | 只读，静态 |
| `PI` | π | 1.0, ECMA-262 | 只读，静态 |
| `SQRT1_2` | 1 除以 2 的平方根 | 1.0, ECMA-262 | 只读，静态 |
| `SQRT2` | 2 的平方根 | 1.0, ECMA-262 | 只读，静态 |

## Math 方法和属性

### abs()

`abs()` 方法返回数字的绝对值。它接受一个参数，可以是任何数值。

`abs()` 在 JavaScript 1.0 及后续版本可用，并包含在 ECMA-262 标准中。

```javascript
var i = Math.abs(-33.337);
// 等于 33.337
```

注意 `abs()` 是一个静态方法，只能通过执行 `Math.abs()` 来调用。

### acos()

`acos()` 方法返回数字的反余弦值。它接受一个在 -1 到 1 之间的数值参数。`acos()` 返回的值始终在 0 到 π（弧度）之间，如果传递给 `acos()` 的参数超出范围，则返回 `NaN`。

你可以通过除以 `((Math.PI * 2) / 360)` 将弧度转换为角度。

`acos()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var r = Math.acos(-1);
// 获取 -1 的反余弦
var a = r / ((Math.PI * 2) / 360);
// 将弧度转换为角度
```

注意 `acos()` 是一个静态方法，只能通过执行 `Math.acos()` 来调用。

### asin()

`asin()` 方法计算数字的反正弦值。它接受一个参数，该参数可以是 -1 到 1 之间的任意数值。`asin()` 返回的值始终在弧度为单位的 -π/2 到 π/2 之间，如果传递给 `asin()` 的参数超出范围，则返回 `NaN`。

你可以通过除以 `((Math.PI * 2) / 360)` 将弧度转换为角度。

`asin()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var r = Math.asin(0.5); // 计算 0.5 的反正弦值
var a = r / ((Math.PI * 2) / 360); // 将弧度转换为角度
```

注意 `asin()` 是一个静态方法，只能通过执行 `Math.asin()` 来调用。

### atan()

`atan()` 方法计算数字的反正切值。它接受一个参数，该参数可以是任意数值，并返回该数字以弧度为单位的反正切值。

你可以通过除以 `((Math.PI * 2) / 360)` 将弧度转换为角度。

`atan()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var r = Math.atan(35); // 计算 35 的反正切值
var t = r / ((Math.PI * 2) / 360); // 将弧度转换为角度
```

注意 `atan()` 是一个静态方法，只能通过执行 `Math.atan()` 来调用。

### atan2()

`atan2()` 方法计算点到 X 轴的角度。它接受两个参数，即点的 x 和 y 坐标。它返回一个以弧度为单位的角度，从正 X 轴逆时针测量到该点的角度。

你可以通过除以 `((Math.PI * 2) / 360)` 将弧度转换为角度。

`atan2()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var r = Math.atan2(3, 4);
// 计算弧度为单位的角度
var a = r / ((Math.PI * 2) / 360);
// 将弧度转换为角度
```

注意 `atan2()` 是一个静态方法，只能通过执行 `Math.atan2()` 来调用。

### ceil()

`ceil()` 方法将数字向上舍入到下一个整数。它接受一个参数，该参数可以是任意数值。

`ceil()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.ceil(23.253); // i 等于 24
```

注意 `ceil()` 是一个静态方法，只能通过执行 `Math.ceil()` 来调用。

### cos()

`cos()` 方法计算角度的余弦。它接受一个参数，即以弧度为单位的角度，并返回一个 -1 到 1 之间的值。

你可以通过乘以 `((Math.PI * 2) / 360)` 将角度转换为弧度。

`cos()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var d = 35 * ((Math.PI * 2) / 360); // 将 35 度转换为弧度
var c = Math.cos(d); // 计算 d 的余弦
```

注意 `cos()` 是一个静态方法，只能通过执行 `Math.cos()` 来调用。

### E

`E` 是一个只读常量，表示自然对数的底数。该值约等于 2.71828。

`E` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
document.write(Math.E);
// 写入 "2.718281828459045"
```

注意 `E` 是一个常量，一个只读属性，只能通过 `Math.E` 引用。

### exp()

`exp()` 方法计算 e 的指数幂，即自然对数的底数的指数。它接受一个参数，该参数可以是任意数值。

`exp()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.exp(2);
// 等于 7.38905609893065
```

注意 `exp()` 是一个静态方法，只能通过执行 `Math.exp()` 来调用。

### floor()

`floor()` 方法将数字向下舍入到整数。它接受一个参数，该参数可以是任意数值。

`floor()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.floor(23.253); // i 等于 23
```

注意 `floor()` 是一个静态方法，只能通过执行 `Math.floor()` 来调用。

### LN2

`LN2` 属性存储 2 的自然对数。该值约等于 0.69315。

`LN2` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
document.write(Math.LN2); // 写入 "0.693147180559945"
```

注意 `LN2` 是一个只读属性，只能通过 `Math.LN2` 引用。

### LN10

`LN10` 属性存储 10 的自然对数。该值约等于 2.30259。

`LN10` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
document.write(Math.LN10); // 写入 "2.302585092994046"
```

注意 `LN10` 是一个只读属性，只能通过 `Math.LN10` 引用。

### log()

`log()` 方法计算数字的自然对数。它接受一个参数，该参数可以是任意数值。

`log()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.log(10); // 等于 2.302585092994046
```

注意 `log()` 是一个静态方法，只能通过执行 `Math.log()` 来调用。

### max()

`max()` 方法比较两个数字并返回较大的那个。

`max()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.max(10, 20); // i 等于 20
```

注意 `max()` 是一个静态方法，只能通过执行 `Math.max()` 来调用。

### min()

`min()` 方法比较两个数字并返回较小的那个。

`min()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.min(10, 20); // i 等于 10
```

注意 `min()` 是一个静态方法，只能通过执行 `Math.min()` 来调用。

### PI

`PI` 是一个只读常量，表示圆周率 π。该值约等于 3.14159。

`PI` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
document.write(Math.PI); // 写入 "3.141592653589793"
```

注意 `PI` 是一个常量，一个只读属性，只能通过 `Math.PI` 引用。

### pow()

`pow()` 方法将数字提升到指定的幂。它接受两个参数。第一个参数是要提升幂的数字，第二个参数是提升的幂。

`pow()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.pow(2, 4); // i 等于 16
```

`pow()` 也可以用于计算数字的根。

```javascript
var i = Math.pow(2, 1/3); // i 等于 2 的立方根
```

若要将数字向上取整或向下取整，请使用 `Math.ceil()` 和 `Math.floor()` 方法。

### random()

`random()` 方法返回 0 到 1 之间的伪随机数。

`random()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.random(); // 返回 0 到 1 之间的随机数
```

注意 `random()` 是一个静态方法，只能通过执行 `Math.random()` 来调用。

### round()

`round()` 方法将数字四舍五入到最接近的整数。

`round()` 在 JavaScript 1.0 及更高版本可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.round(23.5); // i 等于 24
var j = Math.round(23.4); // j 等于 23
```

注意 `round()` 是一个静态方法，只能通过执行 `Math.round()` 来调用。

### sin()

`sin()` 方法计算角度的正弦值。它接受一个弧度作为参数，并返回一个 -1 到 1 之间的值。

你可以通过乘以 `((Math.PI * 2) / 360)` 将度转换为弧度。

`sin()` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var d = 35 * ((Math.PI * 2) / 360); // 将 35 度转换为弧度
var c = Math.sin(d); // 计算 d 的正弦
```

注意 `sin()` 是一个静态方法，只能通过执行 `Math.sin()` 来调用。

### sqrt()

`sqrt()` 方法计算数字的平方根。它接受一个参数，该参数可以是任何数值。

`sqrt()` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var i = Math.sqrt(9); // i 等于 3
```

注意 `sqrt()` 是一个静态方法，只能通过执行 `Math.sqrt()` 来调用。

`Math.pow()` 方法可以用于计算平方根以外的根。

### SQRT1_2

`SQRT1_2` 属性存储 1 除以 2 的平方根的值。这是 2 的平方根的倒数。`SQRT1_2` 约为 0.70710。

`SQRT1_2` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
document.write(Math.SQRT1_2); // 写入 "0.7071067811865476"
```

注意 `SQRT1_2` 是一个常量，一个只读属性，只能通过 `Math.SQRT1_2` 引用。

### SQRT2

`SQRT2` 属性存储 2 的平方根的值。`SQRT2` 的值约为 1.41421。

`SQRT2` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
document.write(Math.SQRT2); // 写入 "1.4142135623730951"
```

注意 `SQRT2` 是一个常量，一个只读属性，只能通过 `Math.SQRT2` 引用。

### tan()

`tan()` 方法计算角度的正切值。它接受一个参数，即以弧度为单位的角度。

你可以通过乘以 `((Math.PI * 2) / 360)` 将度转换为弧度。

`tan()` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var d = 35 * ((Math.PI * 2) / 360);
// 将 35 度转换为弧度
var t = Math.tan(d);
// 计算 d 的正切
```

注意 `tan()` 是一个静态方法，只能通过执行 `Math.tan()` 来调用。

# MimeType

`MimeType` 对象是查找用户浏览器支持的 MIME 类型应用程序的好方法——既可以通过 PC 上的程序也可以通过插件来实现。MIME 类型指的是一种数据格式。遗憾的是，`MimeType` 对象仅由 Netscape 3 及以上版本支持。

表 4-7 总结了 `MimeType` 对象的属性。

`MimeType` 对象使用一个数组 `navigator.mimeTypes[]`，该数组可以通过数字索引或所需的 MIME 类型名称进行索引。以下脚本将允许你查看所有的 MIME 类型：

```javascript
var num = 0;
document.write("<pre>");
while (navigator.mimeTypes[num] != undefined) {
  var MimeType = navigator.mimeTypes[num];
  document.write("Index:\t" + num + "\n");
  document.write("mimeTypes:\t" + MimeType + "\n");
  document.write("description:\t" + MimeType.description + "\n");
  document.write("enabledPlugin:\t" + MimeType.enabledPlugin + "\n");
  document.write("suffixes:\t" + MimeType.suffixes + "\n");
  document.write("type:\t" + MimeType.type + "\n\n");
  num++;
}
document.write("</pre>");
```

| 属性 | 说明 | JavaScript 版本 | 备注 |
|---|---|---|---|
| `description` | MIME 类型的描述 | 客户端 Navigator 3 | 只读 |
| `enabledPlugin` | 处理 MIME 类型的插件 | 客户端 Navigator 3 | 只读 |
| `suffixes` | MIME 类型的常用后缀 | 客户端 Navigator 3 | 只读 |
| `type` | MIME 类型的名称 | 客户端 Navigator 3 | 只读 |

## MimeType 属性

### description

`description` 属性是对 MIME 类型中描述的数据类型的一种易于阅读的描述。

```javascript
document.write(navigator.mimeTypes["application/pdf"].description);
```

### enabledPlugin

`enabledPlugin` 属性返回处理该 MIME 类型的插件对象。

```javascript
document.write(navigator.mimeTypes["application/pdf"].enabledPlugin);
```

### suffixes

`suffixes` 属性返回该 MIME 类型常用的文件扩展名列表。

```javascript
document.write(navigator.mimeTypes["application/pdf"].suffixes);
```

### type

`type` 属性返回 MIME 类型的名称。

```javascript
document.write(navigator.mimeTypes["application/pdf"].type);
```

# Number

`Number` 对象包含数值常量和方法。它在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

### 表 4-6. Number 对象属性

| 属性 | 描述 | JavaScript 版本 | 备注 |
| :--- | :--- | :--- | :--- |
| `MAX_VALUE` | 最大可表示数值 | 1.1, ECMA-262 | 只读，静态 |
| `MIN_VALUE` | 最小可表示正数值 | 1.1, ECMA-262 | 只读，静态 |
| `NaN` | 非数字值 | 1.1, ECMA-262 | 只读，静态 |
| `NEGATIVE_INFINITY` | 负无穷大 | 1.1, ECMA-262 | 只读，静态 |
| `POSITIVE_INFINITY` | 正无穷大 | 1.1, ECMA-262 | 只读，静态 |

## Number 对象属性

### MAX_VALUE

`MAX_VALUE` 是一个只读常量，表示 JavaScript 中可表示的最大数值。该值约等于 1.7976931348623157e+308。

`MAX_VALUE` 在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var max = Number.MAX_VALUE;
// max 等于 1.7976931348623157e+308
```

注意 `MAX_VALUE` 是静态变量；因此，如果你创建一个名为 `n` 的 `Number` 对象，你将无法访问 `n.MAX_VALUE`。`MAX_VALUE` 常量只能通过 `Number.MAX_VALUE` 来引用。

### MIN_VALUE

`MIN_VALUE` 是一个只读常量，表示 JavaScript 中可表示的最小正数值（最接近零的正数）。该值约等于 5e-324。

`MIN_VALUE` 在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var min = Number.MIN_VALUE;
// min 等于 5e-324
```

注意 `MIN_VALUE` 是静态变量；因此，如果你创建一个名为 `n` 的 `Number` 对象，你将无法访问 `n.MIN_VALUE`。`MIN_VALUE` 常量只能通过 `Number.MIN_VALUE` 来引用。

### NaN

`NaN` 是一个只读常量，表示非数字值。`NaN` 通常用于指示解析数字时的错误（例如 `parseInt("abc")`）。

`NaN` 在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var notANumber = Number.NaN;
```

注意 `NaN` 是静态变量；因此，如果你创建一个名为 `n` 的 `Number` 对象，你将无法访问 `n.NaN`。`NaN` 常量只能通过 `Number.NaN` 来引用。

### NEGATIVE_INFINITY

`NEGATIVE_INFINITY` 是一个只读常量，表示负无穷大。如果一个方法返回此数字，通常意味着发生了溢出错误。

`NEGATIVE_INFINITY` 在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var negativeInfinity = Number.NEGATIVE_INFINITY;
```

注意 `NEGATIVE_INFINITY` 是静态变量；因此，如果你创建一个名为 `n` 的 `Number` 对象，你将无法访问 `n.NEGATIVE_INFINITY`。`NEGATIVE_INFINITY` 常量只能通过 `Number.NEGATIVE_INFINITY` 来引用。

### POSITIVE_INFINITY

`POSITIVE_INFINITY` 是一个只读常量，表示正无穷大。如果一个方法返回此数字，通常意味着发生了溢出错误。

`POSITIVE_INFINITY` 在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var infinity = Number.POSITIVE_INFINITY;
```

注意 `POSITIVE_INFINITY` 是静态变量；因此，如果你创建一个名为 `n` 的 `Number` 对象，你将无法访问 `n.POSITIVE_INFINITY`。`POSITIVE_INFINITY` 常量只能通过 `Number.POSITIVE_INFINITY` 来引用。

## Number 对象方法

### toString()

`Number` 对象的 `toString()` 方法返回 `Number` 对象值的字符串表示。`toString()` 接受一个参数，该参数可以是 2 到 36 之间的基数。如果没有向 `toString()` 传递参数，它将使用 10 进制，这也是大多数人使用的基数。

`toString()` 在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var i = 32;
var s = i.toString(); // s 等于 "32"
var s = i.toString(2); // s 等于 "100000" (二进制)
var s = i.toString(8); // s 等于 "40" (八进制)
```

`toString()` 还可以用于以更易读的格式打印 `Number` 对象的常量。

```javascript
var s = Number.MAX_VALUE.toString();
// s 等于 "1.7976931348623157e+308"
var s = Number.MIN_VALUE.toString(); // s 等于 "5e-324"
var s = Number.NaN.toString(); // s 等于 "NaN"
var s = Number.NEGATIVE_INFINITY.toString(); // s 等于 "-Infinity"
var s = Number.POSITIVE_INFINITY.toString(); // s 等于 "Infinity"
```

# 全局函数

## parseFloat()

`parseFloat()` 方法将字符串转换为浮点数。它接受一个参数（字符串），并返回字符串中的数字，或者在未找到数字时返回 `NaN`。

`parseFloat()` 在 JavaScript 1.0 中可用，并包含在 ECMA-262 规范中。在 JavaScript 1.0 中，不支持 `NaN`，因此 `parseFloat()` 在遇到非数字字符串时会返回零。

```javascript
var s = "3.14 radians";
var i = parseFloat(s);
// i 等于 3.14
s = "pi radians (3.14)";
var i = parseFloat(s);
// 在 JavaScript 1.1 中等于 NaN，在 v1.0 中等于 0
```

## parseInt()

`parseInt()` 方法将字符串转换为整数。它接受两个参数。第一个是用于转换为整数的字符串。第二个是可选的基数，用于指定返回值的进制。如果留空，默认为 10 进制。返回的值是一个整数。

如果字符串开头没有找到数字，`parseInt()` 返回 `NaN`。

`parseInt()` 在 JavaScript 1.0 中可用，并包含在 ECMA-262 规范中。在 JavaScript 1.0 中，不支持 `NaN`，因此 `parseInt()` 在遇到非数字字符串时会返回零。

```javascript
var s = "3.14 radians";
var i = parseInt(s);
// i 等于 3
s = "pi radians (3.14)";
var i = parseInt(s);
// 在 JavaScript 1.1 中等于 NaN，在 JavaScript 1.0 中等于 0
```

# RegExp

`RegExp` 对象支持正则表达式，正则表达式用于匹配文本模式并辅助搜索和替换操作。正则表达式有多种不同的实现；JavaScript 使用与 Perl 编程语言相同的语法。

`RegExp` 在 JavaScript 1.2 及更高版本中支持，并包含在 ECMA-262 规范中。

可以使用 `RegExp()` 构造函数创建 `RegExp` 对象。正则表达式的字面量语法可以编码到 JavaScript 程序中。模式包含在两个斜杠（/）之间，第二个斜杠后面可以跟一个字母，以更改模式的功能。以下是几个正则表达式的示例：

```javascript
/<a href=/i
/[a-z][A-Z]/g
/<br\/n/
```

## 定义正则表达式

正则表达式可以使用字面量创建或使用 `RegExp()` 构造函数创建。这两种技术仅在 JavaScript 1.2 及更高版本中有效，因为之前的版本中没有正则表达式。

### RegExp 构造函数

这里为变量 `MyExpression` 分配了一个新的 `RegExp` 对象。它将匹配的模式必须以 `<a href` 开头。

```javascript
var MyExpression = new RegExp("^a href");
```

### 正则表达式字面量

任何正则表达式字面量都可以赋值给变量。区别在于正则表达式被斜杠（/）包含而不是单引号或双引号包含。

```javascript
var MyExpression = /^<a href/;
```

## 模式匹配

模式匹配描述了正则表达式的基本功能。模式匹配允许 `RegExp` 区分字母、数字、空格和符号字符串与其他文本。简单的模式匹配非常容易，而寻找特定的内容可能是一项艰巨的任务。如果你以前没有用过模式匹配，起初可能会困惑，但过了一段时间，你将获得一个强大的工具。

### 字面字符

字面字符分为几类：字符、元字符、特殊字符和字符类。每一类都有特定的功能，在此处讨论。

**字符**：字母和数字字符进行字面匹配。对于大多数其他字符也是如此，但有几个例外属于“元字符”组，将在下文中解释。

表 4-9 显示了三个字符匹配的示例。

| 正则表达式 | 匹配 | 不匹配 |
|---|---|---|
| `/abc/` | abc | abd |
| `/a-z/` | a, b, c... | A |
| `/[0-9]/` | 1, 2, 3... | a |

**元字符**：具有特殊功能的字符是元字符。

| 表达式 | 数字类型 |
|---|---|
| `\###` | 八进制数字 |
| `\x##` | 十六进制数字 |
| `\u####` | Unicode 数字 |
| `\cX` | 控制字符 |

**字符类** 字面字符的组被称为字符类，通常用于匹配一系列字面字符。字符类有助于匹配单词或字符组。表 4-14 列出了所有可用的字符类；表 4-15 给出了它们用法的一些示例。

| 表达式 | 匹配 |
|---|---|
| `\120` | 字母 P |
| `\x23` | # 符号 |
| `\u05E5` | 希伯来字母 Final Tsadi |
| `\t` | 制表符 |

### 字符类匹配

| 表达式 | 匹配项 |
| :--- | :--- |
| `[...]` | 括号内的任意单个字符 |
| `[^...]` | 括号内字符以外的任意单个字符 |
| `.` | 除换行符 `\n` 以外的任何字符 |
| `\w` | 任意单词字符 |
| `\W` | 任意非单词字符 |
| `\s` | 任意空白字符 |
| `\S` | 任意非空白字符 |
| `\d` | 任意数字 |
| `\D` | 任意非数字 |
| `\b` | 单词边界（在 `[]` 中表示退格键） |

表 4-14. 正则表达式字符类

| 示例 | 匹配项 | 不匹配 |
| :--- | :--- | :--- |
| `/fact[oid]/` | factoids, fictitious | fact, facts, factless |
| `/bob[^s]/` | bobby, bobcat | bob, bobs |
| `/.t/` | bit, bitrate, but, butter, b@test.com | bi, b, b\nt |
| `/\w/` | a, href, food, word | , \s, !, @, \t |
| `/\W/` | !@#!, \t | foot, big feet, size-large |
| `/\s/` | best in town, fast cars | small, medium, large |
| `/\S/` | small, medium, large | best in town, fast cars, a href |
| `/\d/` | 123, 321, 1245512, abc123 | color=green, word, letters |
| `/\D/` | color=green, word, letters | 123, 321, 1245512, abc123 |

表 4-15. 正则表达式字符类示例

### 重复字符

前面的示例可能会让你认为匹配许多字符需要巨大的正则表达式。坦率地说，有一种更简单的方法。重复字符通常用于匹配重复字符字符串，如表 4-16 所示。

| 字符 | 匹配项 |
| :--- | :--- |
| `X{Y,Z}` | 至少 Y 次，但不超过 Z 次 |
| `X{Y,}` | Y 次或更多次 |
| `X{Y}` | 正好 Y 次 |
| `X?` | X 的零次或一次；同 `X{0,1}` |
| `X+` | X 的一次或多次；同 `X{1,}` |
| `X*` | X 的零次或多次；同 `X{0,}` |

表 4-16. 带有正则表达式的重复字符

### 示例匹配

| 表达式 | 匹配项 |
| :--- | :--- |
| `\s.{2,5}\.` | 空白后跟两个到五个以点结尾的字符 |
| `\w{3,}` | 三个或多个单词字符 |
| `/a{4}/` | aaaa, aaaayxyz, aaaa1234 |
| `/ar{5}gh!/` | arrrrgh! |
| `\w?\.` | 零个或一个单词字符后跟点 |
| `\(\d+\)` | (1), (123), (32495), (234658) |
| `/[a-z][A-Z]*/` | 包含字母的字符串；不会匹配 "11" |

表 4-17. 重复字符的示例

### 分组与或 (OR)

分组允许你拆分正则表达式。这在匹配复杂模式时非常有用。要对正则表达式进行分组，只需将其括在括号中。例如：

```javascript
var MyGroup = /<a href="(.+)\(\w+)\)>/;
```

`MyGroup` 表达式包含两个分组。第一个分组匹配一个或多个字符，而第二个分组匹配一个或多个单词字符。

分组通常与 OR 使用，允许你匹配不同的分组可能性。例如：

```javascript
var OrGroup = /((bgcolor=".*?")|(background=".*?\.(gif|jpg)"))/;
```

前面的表达式将匹配以下字符串之一：

- `bgcolor="blue"`
- `background="waves.jpg"`
- `background="fruit.gif"`
- `bgcolor="black"`
- `background="image.gif"`
- `background="cloud.jpg"`

前面的 `OrGroup` 变量匹配 `bgcolor` 或 `background`，可能是 `gif` 或 `jpg`。

分组的部分可以通过 `$#` 引用。上一个代码中的 `OrGroup` 变量总共有六个子表达式，分别标记为 `$1` 到 `$6`。它们的计数从第一个括号开始向右移动，如下：

```
$1: ((bgcolor=".*?")|(background=".*?\.(gif|jpg)"))
$2: (bgcolor=".*?")
$3: .*?
$4: (background=".*?\.(gif|jpg)")
$5: .*?\.(gif|jpg)
$6: (gif|jpg)
```

使用子表达式时，记住它们引用匹配文本，而不是实际表达式。

```javascript
var SubRegExp = /(a|b|c) is the letter \1/;
// 匹配：a is the letter a
// 不匹配：a is the letter b
```

目前的 JavaScript 实现处理子表达式时有很多 Bug，你可能想要避免它们。例如，请注意下面的变量，它与之前的相似：

```javascript
var BrokenSub = /(a|b|c) \s\w+\1/;
// 这应该匹配：a is the letter a
// 它实际上没有匹配任何内容。
```

### 匹配内存

| 表达式 | 类型 | 匹配 |
|---|---|---|
| `(bob)` | 捕获括号 | 匹配 bob 并记住该匹配项 |
| `(?:bob)` | 非捕获括号 | 匹配 bob，但不记住匹配项 |
| `bob(?=sam)` | 正向前瞻 | 如果后面跟着 sam 则匹配 bob |
| `bob(?!sam)` | 负向前瞻 | 如果后面没有紧跟 sam 则匹配 bob |

表 4-18. 使用正则表达式的匹配内存

## String 方法

### replace()

`replace()` 方法被用于搜索和替换。你只需要简单地向它传递一个正则表达式以及你想替换它的文本即可。

```javascript
var TextString = "I drive a small car.";
var Replacement = TextString.replace(/small/, "large");
document.write(Replacement);
// 返回句子：I drive a large car.
```

将 `replace()` 与子表达式结合使用会增加另一层实用性。以下代码适用于将格式化后的电话号码转换为数字字符串。

```javascript
var phoneNumber = "(505) 555-1234";
var regexp = /\((\d{3})\)\s(\d{3})-(\d{4})/;
document.write(phoneNumber.replace(regexp, "$1$2$3"));
// 打印 5055551234
```

如你所见，子表达式 `$1`, `$2`, `$3` 用于调用每组数字。

### match()

`match()` 方法的作用是进行匹配。它将返回传递给它的第一个匹配项，除非设置了 `g` 标志。无论你是否使用 `g` 标志，数据都会存储在数组中。

```javascript
var phoneNumber = "(505) 555-1234";
var regexp = /\(\d{3}\)/;
var match = phoneNumber.match(regexp);
document.write(match); // 返回 (505)
document.write(match[0]); // 这同样返回 (505)
```

`match()` 返回的数组有三个属性：`length`、`index` 和 `input`。`length` 属性返回数组中元素的数量。如果使用了 `g` 标志，`index` 属性返回最后一次匹配的字符位置。最后，`input` 属性返回传递给 `match()` 的文本。

```javascript
var phoneNumber = "(505) 555-1234";
var regexp = /\d{3}/g;
var match = phoneNumber.match(regexp);
document.write(match.length); // 返回 3 (匹配到 505, 555, 123)
document.write(match.index); // 返回 1 (第一次匹配的位置)
document.write(match.input); // 返回 (505) 555-1234
```

### split()

`split()` 方法将一行数据拆分为一个数组。这里有一个我用来规范电话号码信息的快速正则表达式：

```javascript
var phoneNumber1 = "703-555-4321";
var phoneNumber2 = "703.555.1234";
var phoneNumber3 = "703 555 2231";
var phoneNumber4 = "(703) 555.4112";
var regexp = /[\(\)\.\-\s]+/g;
document.write(phoneNumber1.split(regexp)); // 返回 703,555,4321
document.write(phoneNumber2.split(regexp)); // 返回 703,555,1234
document.write(phoneNumber3.split(regexp)); // 返回 703,555,2231
document.write(phoneNumber4.split(regexp)); // 返回 703,555,4112
```

当然，你也可以获取数组的部分内容。在前面的示例中，你可以使用 `phoneNumber4.split(regexp)[3]` 仅返回 4112。

## RegExp 对象

正如我们在“定义正则表达式”章节中所学到的，`RegExp` 对象允许你创建正则表达式。你还可以包含 `g`、`i` 和 `m` 标志。此外，在使用字符串构造函数时，必须使用转义字符 `\`。例如：

```javascript
var Word = new RegExp("I use JavaScript", "i");
// 匹配给定的短语，忽略大小写。
// 等同于：/I use JavaScript/i
```

### RegExp 对象方法

#### compile()

`compile()` 方法用于更改 `RegExp` 对象的内容。

```javascript
Word.compile("\\w", "gi");
// 将 Word RegExp 对象更改为全局匹配任何单词字符，忽略大小写。
// 等同于：/\w/gi
```

#### test()

`test()` 方法与字符串的 `match()` 方法类似，尽管它返回 `true` 或 `false`，而不是匹配到的文本。

```javascript
var regexp = new RegExp("SMALL\\scar", "i");
document.write(regexp.test("I drive a small car."));
// 返回：true
```

#### exec()

`exec()` 方法返回匹配的文本，并更新几个属性和索引，这些索引提供了详细信息。

```javascript
var MyExpression = new RegExp("\\B(car)\\B", "g");
var ThisArray = MyExpression.exec("I have many scars from car wrecks.");
```

表 4-19 显示了上述示例中 `exec()` 方法更改的属性和索引。

| 对象 | 属性 | 描述 |
|---|---|---|
| `ThisArray` | `[0]` | 第一个匹配项 |
| `ThisArray` | `index` | 第一个匹配的位置 |
| `ThisArray` | `input` | 原始字符串 |
| `ThisArray` | `length` | 匹配项数组的长度 |
| `ThisArray` | `[1]` | 第一个捕获组 |

# String

`String` 对象用于处理文本数据。它在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

### 表 4-20. String 对象中可用的方法和属性（续）

| 方法/属性 | 描述 | JavaScript 版本 | 备注 |
|---|---|---|---|
| `replace()` | 将匹配给定表达式的任何模式替换为子字符串 | 1.2, ECMA-262 | |
| `search()` | 在字符串中搜索正则表达式 | 1.2, ECMA-262 | |
| `slice()` | 返回字符串的子字符串 | 1.2, ECMA-262 | |
| `small()` | 使用 `<SMALL>` 标签格式化字符串 | 1.0 | 生成不符合 XHTML 的代码 |
| `split()` | 在给定的分隔符处拆分字符串为数组 | 1.1, ECMA-262 | JavaScript 1.2 及更高版本中支持正则表达式 |
| `strike()` | 使用 `<STRIKE>` 标签格式化字符串 | 1.0 | 生成不符合 XHTML 的代码 |
| `sub()` | 使用 `<SUB>` 标签格式化字符串 | 1.0 | 生成不符合 XHTML 的代码 |
| `substr()` | 从起始索引返回指定长度的子字符串 | 1.2, ECMA-262 | |
| `substring()` | 返回两个索引之间的子字符串 | 1.0, ECMA-262 | |
| `sup()` | 使用 `<SUP>` 标签格式化字符串 | 1.0 | 生成不符合 XHTML 的代码 |
| `toLowerCase()` | 将字符串转换为小写 | 1.0, ECMA-262 | |
| `toUpperCase()` | 将字符串转换为大写 | 1.0, ECMA-262 | |

## 创建字符串

`String` 对象的实例可以显式或隐式地创建。在 JavaScript 1.0 中，它们只能隐式创建。

### String 构造函数

要创建一个新的 `String` 对象，你可以使用 `new` 语句。`String` 构造函数有一个可选参数，即字符串的初始值。如果省略此参数，则将创建一个空字符串。

`String` 构造函数在 JavaScript 1.1 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var s = new String("The quick brown fox...");
// 创建一个设为 "The quick brown fox..." 的 String 对象
var s = new String();
// 创建一个空字符串对象
```

### 在 JavaScript 1.0 中创建字符串

在 JavaScript 1.0 中，无法显式创建 `String` 对象。任何赋值为引号字符串的变量都会自动成为 `String` 对象。

在所有版本的 JavaScript 中，都可以这种方式创建字符串。

```javascript
var s = "The quick brown fox...";
// 创建一个设为 "The quick brown fox..." 的 String 对象
var s = "";
// 创建一个空字符串
```



# String 方法和属性

以下是目前 String 对象中可用方法和属性的描述。

## anchor()

`anchor()` 方法返回使用 `<A>` 标签格式化为命名锚点的 String 对象的值。它接受一个参数，即字符串，用于 `<A>` 标签的 `NAME` 属性。

`anchor()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var a = s.anchor("car");
// a equals "<A NAME="car">Toyota</A>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。

## big()

`big()` 方法返回使用 `<BIG>` 标签格式化的 String 对象的值。它不接受任何参数。

`big()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var b = s.big();
// b equals "<BIG>Toyota</BIG>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。

## blink()

`blink()` 方法返回使用 `<BLINK>` 标签格式化的 String 对象的值。它不接受任何参数。

`blink()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var b = s.blink();
// b equals "<BLINK>Toyota</BLINK>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。此外，`<BLINK>` 标签仅受 Netscape 支持。

## bold()

`bold()` 方法返回使用 `<B>` 标签格式化的 String 对象的值。它不接受任何参数。

`bold()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var b = s.bold();
// b equals "<B>Toyota</B>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。

## charAt()

`charAt()` 方法返回 String 对象中指定位置的字符。它接受一个参数，即要返回的字符的索引。如果参数小于 0 或大于字符串长度，`charAt()` 返回一个空字符串。`charAt()` 在 JavaScript 1.2 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var s = new String("Toyota");
var c = s.charAt(4);
// equals "t"
```

## charCodeAt()

`charCodeAt()` 方法返回 String 对象中指定位置的字符的 Unicode 编码。它接受一个参数，即要返回的代码。`charCodeAt()` 在 JavaScript 1.2 及更高版本中可用，并包含在 ECMA-262 规范中。早期的 Netscape 4 不完全支持 Unicode 字符集的所有 65,535 个值，但与 Unicode 的前 128 个字符完全匹配。

```javascript
var s = new String("Toyota");
var c = s.charCodeAt(4);
// equals "116"
```

## concat()

`concat()` 方法合并两个或多个字符串的值，将它们附加到 String 对象的末尾，并返回新字符串。它接受一个或多个参数。`concat()` 在 JavaScript 1.1 及更高版本中可用，并包含 ECMA-262。

```javascript
var s = new String("Toyota");
var c = s.concat(" is the name.");
// equals "Toyota is the name."
```

## fixed()

`fixed()` 方法返回使用 `<TT>` 标签格式化的 String 对象的值。它不接受任何参数。`fixed()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var f = s.fixed();
// equals "<TT>Toyota</TT>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。

## fontcolor()

`fontcolor()` 方法返回使用 `<FONT>` 标签格式化为颜色的 String 对象的值。它接受一个参数，即颜色。`fontcolor()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var f = s.fontcolor("#000FF");
// equals "<FONT COLOR='#000FF'>Toyota</FONT>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。

## fontsize()

`fontsize()` 方法返回使用 `<FONT>` 标签格式化为指定大小的 String 对象的值。它接受一个参数，整数或包含相对大小的字符串，例如 `"+1"` 或 `"-3"`。`fontsize()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var f = s.fontsize(4);
// equals "<FONT SIZE='6'>Toyota</FONT>"
f = s.fontsize("-2");
// equals "<FONT SIZE='-2'>Toyota</FONT>"
```

注意此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0、1.1 或 Basic）都不兼容，后者是当前的 W3C HTML 标准。

## fromCharCode()

`fromCharCode()` 方法从字符编码创建并返回字符串。它接受一个或多个 16 位 Unicode 字符值。`fromCharCode` 在 JavaScript 1.2 及更高版本中可用，并包含在 ECMA-262 规范中。早期的 Netscape 4 不完全支持 Unicode 字符集的所有 65,535 个值，但与 Unicode 的前 128 个字符完全匹配。

```javascript
var c = String.fromCharCode(84,111,121,111,116,97);
```

注意 `fromCharCode()` 是一个静态方法，因此必须通过 `String.fromCharCode()` 引用，而不是 String 实例的方法。

## indexOf()

`indexOf()` 方法在 String 对象中搜索子字符串并返回其第一次出现的位置。它接受两个参数。第一个参数是要搜索的子字符串，第二个参数（可选）是开始搜索的索引。默认值为零。

`indexOf()` 返回子字符串开始位置的索引。如果未找到子字符串，`indexOf()` 返回 -1。`indexOf()` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var s = new String("barbella@webbedtogether.com");
var i = s.indexOf("b");
// i equals 0
var i2 = s.indexOf("b",1);
// i2 equals 3
var i2 = s.indexOf("z");
// i2 equals -1
```

## italics()

`italics()` 方法返回使用 `<I>` 标签格式化的 String 对象的值。它不接受任何参数。

`italics()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var i = s.italics();
// i equals "<I>Toyota</I>"
```

注意，此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0, 1.1, Basic）不兼容，它们是当前的 W3C HTML 标准。

## lastIndexOf()

`lastIndexOf()` 方法在 String 对象中反向搜索子字符串，并返回该字符串最后一次出现的位置索引。它接受两个参数。第一个参数是要搜索的子字符串；第二个参数可选，是开始搜索的索引。默认值是字符串的末尾，或者字符串长度减一。

`lastIndexOf()` 返回子字符串起始位置的索引。如果未找到子字符串，`lastIndexOf()` 返回 -1。

`lastIndexOf()` 可用于 JavaScript 1.0 及更高版本，并包含在 ECMA-262 规范中。

```javascript
var s = new String("barbarella@webbedtogether.com");
var i = s.lastIndexOf("b"); // i equals 3
var i2 = s.lastIndexOf("b",2); // i2 equals 0
var i2 = s.lastIndexOf("z"); // i2 equals -1
```

### length

String 的 `length` 属性等于字符串中字符的数量。`length` 是只读的。

`length` 可用于 JavaScript 1.0 及更高版本，并包含在 ECMA-262 规范中。

```javascript
var s = new String("Toyota");
var i = s.length; // i equals 6
```

`length` 可以处理字符串中的每个字符。以下代码创建了字符串中每个字符的 Unicode 字符编码列表。

```javascript
var codes = "";
for(var i = 0; i < s.length; i++) {
  codes += (s.charCodeAt(i) + ", ");
}
// codes equals "84, 111, 121, 111, 116, 97,"
```

## link()

`link()` 方法返回使用 `<A>` 标签格式化为超链接的 String 对象的值。它接受一个参数（字符串），用作 HREF 属性或要链接的 URL。

`link()` 可用于 JavaScript 1.0 及更高版本。

```javascript
var s = new String("Toyota");
var a = s.link("http://www.toyota.com");
// equals "<A HREF=http://www.toyota.com>Toyota</A>"
```

注意，此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 文档类型（XHTML 1.0, 1.1, Basic）不兼容，它们是当前的 W3C HTML 标准。

## match()

`match()` 方法在 String 对象中查找一个或多个正则表达式匹配，并返回测试结果数组。它接受一个或多个参数，每个参数都应该是正则表达式。如果没有找到匹配项，`match()` 返回 null。否则，`match()` 返回匹配文本的数组。

`match()` 可用于 JavaScript 1.2 及更高版本，并包含在 ECMA-262 规范的第三版中。

```javascript
var s = new String("bararella@webbedtogether.com, Molly@YAHOO.COM");
var t = s.match(/.com/gi);
// t is an array containing {".com", ".COM"}
```

要了解更多关于正则表达式这一大主题，请参阅本章节的 "RegExp" 部分。

## replace()

`replace()` 方法在 String 对象中查找一个或多个正则表达式匹配，并将每个匹配项替换为新字符串。它接受两个参数。第一个参数应该是正则表达式。第二个参数仅为字符串，用于替换与第一个参数匹配的所有内容。如果未找到匹配项，`match()` 返回 null。

`replace()` 可用于 JavaScript 1.2 及更高版本，并包含在 ECMA-262 规范的第三版中。

```javascript
var s = new String("bararella@webbedtogether.com, Molly@YAHOO.COM");
var t = s.replace(/.com/gi, ".com");
// t equals "bararella@hotmail.com, Molly@YAHOO.COM"
// 两个实例都是小写的。
```

`replace()` 包含一组特殊参数，可以在其替换文本中指定，列举如下：

| 参数 | 替换内容 |
| --- | --- |
| `$$` | 一个美元符号 `$` |
| `$&` | 匹配的子字符串 |
| `$`` | 匹配子字符串之前的字符串部分 |
| `$'` | 匹配子字符串之后的字符串部分 |
| `$1` 到 `$9` | 正则表达式中用于匹配字符串的括号内子表达式 |

要了解更多关于正则表达式这一大主题，请参阅本章节的 "RegExp" 部分。

## search()

`search()` 方法对正则表达式和 String 对象进行搜索。它接受一个参数，即要搜索的正则表达式。`search()` 返回匹配的子字符串起始的位置，如果未找到匹配项，则返回 -1。

`search()` 可用于 JavaScript 1.2 及更高版本，并包含在 ECMA-262 规范的第三版中。

```javascript
var s = new String("barbarella@webbedtogether.com, Molly@YAHOO.COM");
t = s.search(/.com/gi);
// t equals -1
t = s.search(/.com/i);
// t equals 0
```

要了解更多关于正则表达式这一大主题，请参阅本章节的 "RegExp" 部分。

### slice()

`slice()` 方法提取字符串的一部分并返回它。它接受两个参数。第一个参数是提取开始的位置。第二个参数（可选）是提取结束的位置（不包含）。如果省略第二个参数，它将提取到字符串末尾。如果任何一个参数为负数，则被视为从字符串末尾开始偏移。

`slice()` 可用于 JavaScript 1.0 及更高版本，并包含在 ECMA-262 规范中。

```javascript
var s = new String("Toyota");
var i = s.slice(0, 4); // i equals "Toy"
var i2 = s.slice(-3); // i2 equals "ota"
```

## substr()

`substr()` 方法提取字符串的一部分并返回它。它接受两个参数。第一个参数是提取开始的位置。第二个参数是一个数字，表示到子字符串结束的字符位置数。如果不包含此参数，`substr()` 将包含到字符串末尾的所有字符。

`substr()` 在 JavaScript 1.2 及更高版本中可用，并包含在 ECMA-262 规范中。在 Internet Explorer 4 和 5 中，第一个参数不能为负数。

```javascript
var s = new String("Toyota");
var t = s.substr(0,3);
// t 等于 "Toy"
```

## substring()

`substring()` 方法提取字符串的一部分并返回它。`substring()` 接受两个参数，即字符串内的两个字符位置。

第一个参数是子字符串应该开始的字符位置。第二个参数是紧随结束字符位置之后的字符位置。

两个参数都必须是 0 到数组长度减一 之间的数字，且第一个参数必须小于第二个参数。

`substring()` 在 JavaScript 1.0 及更高版本中可用，并包含在 ECMA-262 规范中。

```javascript
var s = new String("Toyota");
var t = s.substring(0,3);
// t 等于 "Toy"
```

## sup()

`sup()` 方法返回用 `<SUP>` 标签格式化的 String 对象的值。它不接受任何参数。

`sup()` 在 JavaScript 1.0 及更高版本中可用。

```javascript
var s = new String("Toyota");
var b = s.sup();
// b 等于 "<SUP>Toyota</SUP>"
```

注意，此方法以大写形式打印 HTML 标签和属性。这与任何 XHTML 系列文档类型（XHTML 1.0, 1.1, Basic）都不兼容，后者是当前的 W3C HTML 标准。

## toLowerCase()

`toLowerCase()` 方法将 String 对象的值转换为小写字母。

`toLowerCase()` 在 JavaScript 1.0 及更高版本中可用，并被包含在 ECMA-262 规范中。

```javascript
var s = new String("Toyota");
var l = s.toLowerCase();
// l 等于 "toyota"
```

## toUpperCase()

`toUpperCase()` 方法将 String 对象的值转换为大写字母。

`toUpperCase()` 在 JavaScript 1.0 及更高版本中可用，并被包含在 ECMA-262 规范中。

```javascript
var s = new String("Toyota");
var u = s.toUpperCase();
// u 等于 "TOYOTA"
```

# 第 5 章 浏览器中的 JavaScript：客户端对象、方法和属性

## 在 HTML 页面中嵌入 JavaScript

你可以通过几种不同的方式将 JavaScript 嵌入 HTML 中。本章的一部分将介绍每种方法并包含示例。

### `<SCRIPT>` 标签

`<SCRIPT>` 标签是嵌入 JavaScript 最常用的方法。它们的用法与其他大多数 HTML 标签类似：以 `<SCRIPT>` 标签开始，插入任意数量的语句，并以 `</SCRIPT>` 标签结束。`<SCRIPT>` 标签可以放在 HTML 的 `<HEAD>` 或 `<BODY>` 中。一个 HTML 文档可以包含任意数量的 `<SCRIPT>` 标签。此外，这些标签是不区分大小写的。

```html
<html>
<head>
<title>JavaScript Example</title>
<script type="text/javascript">
<!--//
function add_numbers(x,y) {
  var sum = x+y;
  document.write(sum);
}
//-->
</script>
</head>
<body>
数字 20 和 35 的和是：
<script type="text/javascript">
<!--//
add_numbers(20,35);
//-->
</script>
</body>
</html>
```

注意在前面的示例中，有一些看起来很奇怪的注释标签：`<!--//` 和 `//-->`。这些注释标签用于不支持 JavaScript 的浏览器。如果不使用这些标签，浏览器将显示 `<SCRIPT>` 标签之间的所有内容。

### `<SCRIPT>` 标签属性

`<SCRIPT>` 标签可以使用一些属性。`TYPE` 属性定义了脚本的 MIME 类型。下表列出了常见的 MIME 类型：

| MIME 类型 | 说明 |
|---|---|
| text/ecmascript | JavaScript |
| text/javascript | JavaScript |
| text/microsoft | 微软特有的 JavaScript |
| text/vbscript | Visual Basic (BScript) |
| text/xml | XML |

`SRC` 属性用于嵌入外部文件。`DEFER` 属性是一个布尔值，用于在页面加载时等待。`ARCHIVE` 属性用于 JavaScript。`LANGUAGE` 属性已被废弃。

### URL

你可以使用 `javascript:` 协议在 URL 中嵌入 JavaScript 代码。

### JSS

Navigator 4 系列浏览器引入了样式语法，或简称为 JSS。JSS 使用属性、类和 ID 来创建样式表。JSS 不支持 Internet Explorer。JSS 应该出现在文档的头部。这里有一个示例：

```html
<style type="text/javascript">
tags.p.style="italic";
</style>
```

### 实体

Navigator 3 及以上版本的另一个功能是 JavaScript 实体，它允许你使用特殊的字符序列来执行。实体以 `&` 开始，用分号分隔 JavaScript 语句，并以 `;}` 结束，例如：

```html
<head>
<title>Test</title>
<script language="javascript">
 var MyColor="#aabbcc";
</script>
</head>
<body bgcolor="&{MyColor};}">
<p>Test</p>
</body>
</html>
```

此示例显示浅蓝色背景。奇怪的是，在 Internet Explorer 中它显示为绿色背景——事实上，所有颜色都显示为绿色背景。

## 文档对象模型

文档对象模型（DOM）指的是窗口内部的网页区域。通过 DOM，你可以访问网页中的所有对象，例如图像、表单元素和状态栏。

## navigator 对象

`navigator` 属性包含关于用户的只读信息。这些信息包括网络浏览器、操作系统、语言、插件和 MIME 类型。`navigator` 属性可以在 Netscape 或 Internet Explorer 中使用，尽管 IE 有它自己的版本 `clientInformation`，它返回相同的信息但 Netscape 不可用。表 5-1 列出了 `navigator` 对象的属性和函数。

### navigator 对象属性表

| 属性 | 描述 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `cookieEnabled` | 包含一个布尔值，决定用户是否启用了 Cookie | JavaScript 1.2 | 仅 IE 5+ 和 Netscape 6+ 只读 |
| `cpuClass` | 包含用户使用的 CPU 类型 | JavaScript 1.2 | 仅 IE 5+ 只读 |
| `javaEnabled()` | 测试 Java 的可用性 | JavaScript 1.1 | |
| `language` | 包含浏览器的默认语言 | JavaScript 1.0 | 仅 Netscape 4+ 只读 |
| `mimeTypes[]` | 一个包含浏览器支持的 Mime 类型的数组 | JavaScript 1.1 | 仅只读 |
| `online` | 包含一个布尔值，决定用户是在线还是离线 | JavaScript 1.2 | 仅 IE 4+ 只读 |
| `oscpu` | 显示浏览器所在的平台（操作系统） | JavaScript 1.2 | 仅 Netscape 6+ 只读 |
| `platform` | 包含浏览器所在的平台（操作系统） | JavaScript 1.2 | 只读 |
| `plugins[]` | 一个包含浏览器中安装的插件列表的数组 | JavaScript 1.1 | 仅 Netscape |
| `product` | 包含浏览器的产品名称 | JavaScript 1.2 | 仅 Netscape 6+ 只读 |
| `productSub` | 包含产品的版本信息 | JavaScript 1.2 | 仅 Netscape 6+ 只读 |
| `systemLanguage` | 包含平台的语言 | JavaScript 1.0 | 仅 Internet Explorer 只读 |
| `userAgent` | 包含 HTTP 请求中的 user-agent 头 | JavaScript 1.0 | 只读 |
| `userLanguage` | 包含浏览器的语言 | JavaScript 1.0 | 仅 IE 4+ 只读 |
| `vendor` | 包含浏览器厂商信息 | JavaScript 1.2 | 仅 Netscape 6+ 只读 |
| `vendorsSub` | 包含厂商的版本信息 | JavaScript 1.2 | 仅 Netscape 6+ 只读 |

### navigator.appCodeName

`appCodeName` 属性是一个只读字符串，包含浏览器的代码名称。

```javascript
document.write(navigator.appCodeName);
```

Netscape 2+ 以上版本以及 Internet Explorer 3+ 以上版本返回 Mozilla。

### navigator.appMinorVersion

`appMinorVersion` 属性是一个字符串值，返回浏览器和系统的升级信息。它仅对 Internet Explorer 5+ 浏览器可用。

```javascript
document.write(navigator.appMinorVersion);
// Returns: SP1;Q279328;
```

返回值中的每次升级都用分号分隔。如你所见，我有服务包 1 级和服务警报 Q279328。

### navigator.appName

`appName` 是一个只读属性，返回应用程序名称，即浏览器名称。

```javascript
document.write(navigator.appName);
// IE Returns: Microsoft Internet Explorer
// Netscape Returns: Netscape
```

### navigator.appVersion

`appVersion` 属性返回一个只读字符串，包含有关用户浏览器版本、平台、语言、加密和其他细节的信息。加密方式为 U 或 I，U 表示高加密的美国发行版；I 表示标准加密的国际版。表 5-2 给出了一些示例。

#### 表 5-2. navigator.appVersion 示例

| 示例 | 描述 |
| --- | --- |
| 4.0 (compatible; MSIE 4.01; Windows 98) | Windows 98 上的 Internet Explorer 4.01 |
| 4.04 [en] (Win95; I) | Windows 95 上的英语 Netscape 4.04，标准加密 |
| 4.05 [fr] (Win95; I) | Windows 95 上的法语 Netscape 4.05，标准加密 |
| 4.0 (compatible; MSIE 4.0; AOL 4.0; Windows 95) | Windows 95 上的 Internet Explorer 4.0，使用 AOL 4.0 |
| 4.05 [en] (X11; I; IRIX 6.3 IP32) | IRIX 6.3 上的英语 Netscape 4.05 运行 X-Windows（IRIX 运行在 SGI 机器上） |
| 3.04Gold (Win95; I) | Windows 95 上的 Netscape 3.04 Gold，标准加密 |
| 3.01 (X11; U; SunOS 4.1.4; sun4m) | SunOS 4.1.4 上的 X-Windows，Netscape 3.01 |
| 4.01 (Macintosh; I; PPC) | Macintosh 上的 Internet Explorer 4.01 |

### navigator.cookieEnabled

`cookieEnabled` 属性包含一个布尔值，决定用户是否启用了 Cookie。`navigator.cookieEnabled` 属性在 IE 5+ 和 Netscape 6+ 中可用。

```javascript
document.write(navigator.cookieEnabled);
// Returns: true or false.
```

### navigator.cpuClass

`cpuClass` 属性包含用户使用的 CPU 类型。它对 IE 5+ 只读。

### navigator.javaEnabled()

`javaEnabled()` 方法测试浏览器中 Java 的可用性。

### navigator.language

`language` 属性包含浏览器的默认语言。它对 Netscape 4+ 只读。

### navigator.mimeTypes[]

`mimeTypes[]` 是包含浏览器支持的 Mime 类型的数组。它是只读的。

### navigator.online

`online` 属性包含一个布尔值，决定用户是在线还是离线。它对 IE 4+ 只读。

### navigator.oscpu

`oscpu` 属性显示浏览器所在的平台（操作系统）。它对 Netscape 6+ 只读。

### navigator.platform

`platform` 属性包含浏览器所在的平台（操作系统）。它是只读的。

```javascript
document.write(navigator.platform);
```

这在不同的计算机之间会有所不同。以下是一些示例：

| 示例 | 描述 |
|---|---|
| Win32 | 32 位版本的 Windows |
| Win16 | 16 位版本的 Windows |
| MacPPC | Macintosh Power PC |

### navigator.plugins[]

`plugins[]` 属性是一个包含浏览器中安装插件列表的数组。它对 Netscape 可用。

### navigator.product

`product` 属性包含浏览器的产品名称。它对 Netscape 6+ 只读。

### navigator.productSub

`productSub` 属性包含产品的版本信息。它对 Netscape 6+ 只读。

### navigator.systemLanguage

`systemLanguage` 属性包含平台的语言。它对 Internet Explorer 只读。

### navigator.userAgent

`userAgent` 属性包含 HTTP 请求中的 user-agent 头。它是只读的。

### navigator.userLanguage

`userLanguage` 属性包含浏览器的语言。它对 IE 4+ 只读。

### navigator.vendor

`vendor` 属性包含浏览器厂商信息。它对 Netscape 6+ 只读。

### navigator.vendorsSub

`vendorsSub` 属性包含厂商的版本信息。它对 Netscape 6+ 只读。

## event 对象

### event.returnValue

`returnValue` 属性可以被设置为 true 或 false。如果设置，它的优先级将高于事件处理程序实际返回的值。将其设置为 false 可以取消发生事件的源元素的默认行为。

### event.screenX, event.screenY

`screenX` 和 `screenY` 属性决定了事件相对于屏幕的发生位置。

### event.srcElement

`srcElement` 属性指向生成事件的 Window、Document 或 HTML Element 对象。

### event.srcFilter

`srcFilter` 属性用于 `filterchange`（过滤器更改）事件。它指定发生变化的过滤器。

### event.target

`target` 属性指向生成事件的 Window、Document 或 HTML Element 对象。

### event.toElement

`toElement` 属性用于鼠标移动事件。它指向鼠标指针正在移动进入的对象。

### event.type

`type` 属性指定当前事件的类型。它返回一个类似于 `onMouseEvent` 的值，但不带 `on` 前缀。

### Event 常量

`Event` 类为每个支持的事件类型定义了位掩码常量。它们被传递给 `captureEvents()` 和 `releaseEvents()`。可用常量如下：

- `Event.ABORT`
- `Event.BLUR`
- `Event.CHANGE`
- `Event.CLICK`
- `Event.DBLCLICK`
- `Event.DRAGDROP`
- `Event.ERROR`
- `Event.FOCUS`
- `Event.KEYDOWN`
- `Event.KEYPRESS`
- `Event.KEYUP`
- `Event.LOAD`
- `Event.MOUSEDOWN`
- `Event.MOUSEMOVE`
- `Event.MOUSEOUT`
- `Event.MOUSEOVER`
- `Event.MOUSEUP`
- `Event.MOVE`
- `Event.RESET`
- `Event.RESIZE`
- `Event.SELECT`
- `Event.SUBMIT`
- `Event.UNLOAD`

### event.which

`which` 属性包含键盘和鼠标按钮事件。如果事件期间按了键盘，它会返回所按键的字符编码。如果按了鼠标按钮，它返回以下可能的值：

| which 值 | 说明 |
|---|--- |
| 1 | 左鼠标键 |
| 2 | 中键 |
| 3 | 右鼠标键 |

### event.width

`width` 属性在发生 `resize`（调整大小）事件时设置。它包含了被调整大小对象的新宽度。

### event.x, event.y

`x` 和 `y` 属性指定事件发生的 x 和 y 坐标。在 Netscape 4+ 中，`event.x` 和 `event.y` 等于 `event.layerX` 和 `event.layerY`，它们指定相对于包含层（如果有）的位置。在 IE 4+ 中，该属性指定相对于使用 CSS-P 动态定位的最内包含元素的位置。

## window 对象

`window` 对象描述 Web 浏览器的窗口或帧。该对象最初在 JavaScript 1.0 中引入，随后在 JavaScript 1.1 和 1.2 中得到了增强。表 5-4 列出了 `window` 对象的属性，表 5-5 列出了方法。

### 表 5-4. Window 属性

| 属性 | 描述 | JavaScript 版本 | 备注 |
|---|---|---|---|
| `_content` | 显示当前窗口的内容 | JavaScript 1.3 | Netscape 6 或更高版本 |
| `closed` | 返回一个布尔值，指定窗口是否关闭 | JavaScript 1.1 | 只读 |
| `crypto` | 引用 Crypto 对象 | JavaScript 1.2 | 只读 Netscape 4.04 或更高版本 |
| `defaultStatus` | 指定状态栏中出现的默认消息 | JavaScript 1.0 | |
| `dialogArguments` | 返回创建引用的对话窗口时使用的任何参数 | JavaScript 1.2 | IE 4 或更高版本 |
| `dialogHeight` | 指引用的模态对话窗口的高度 | JavaScript 1.2 | IE 4 或更高版本 |
| `dialogLeft` | 指引用的对话窗口的水平偏移 | JavaScript 1.2 | IE 4 或更高版本 |
| `dialogTop` | 指引用的模态对话窗口的垂直偏移 | JavaScript 1.2 | IE 4 或更高版本 |
| `dialogWidth` | 指引用的模态对话窗口的宽度 | JavaScript 1.2 | IE 4 或更高版本 |
| `document` | 指向窗口中的 Document 对象 | JavaScript 1.0 | 只读 |
| `event` | 包含最近事件的细节 | JavaScript 1.2 | 只读 IE 4 或更高版本 |
| `frames[]` | 指向窗口中帧的数组 | JavaScript 1.0 | 只读 也是 frames |
| `history` | 指向窗口的 History 对象 | JavaScript 1.0 | 只读 |
| `innerHeight` | 指定文档的高度 | | Netscape 6 或更高版本 |
| `innerWidth` | 指定文档的宽度 | | Netscape 6 或更高版本 |
| `length` | `frames[]` 数组的元素数量 | JavaScript 1.0 | 只读 frames |
| `location` | 指向窗口中的 Location 对象 | JavaScript 1.0 | |
| `locationbar` | 指定地址栏的可见性 | JavaScript 1.1 | Netscape 4 或更高版本 |
| `menubar` | 指定菜单栏的可见性 | JavaScript 1.1 | Netscape 4 或更高版本 |
| `name` | 包含窗口名称 | JavaScript 1.0 | 只读 IE |
| `offscreenBuffering` | 浏览器执行的缓冲 | | |
| `onblur` | 指定窗口失去焦点时 | JavaScript 1.1 | |
| `ondragdrop` | 当用户拖放时调用 | JavaScript 1.1 | |
| `onerror` | 当错误处理程序被调用时 | JavaScript 1.1 | |
| `onfocus` | 指定窗口获得焦点时 | JavaScript 1.1 | |
| `onload` | 指定文档或帧集加载时 | JavaScript 1.0 | |
| `onmove` | 指定用户移动顶层窗口时 | JavaScript 1.1 | |
| `onresize` | 指定用户调整窗口或帧的大小时 | JavaScript 1.2 | |
| `onunload` | 指定窗口或帧集卸载时 | JavaScript 1.0 | |
| `opener` | 指向通过 `open()` 创建当前窗口的窗口 | JavaScript 1.1 | 只读 IE |
| `outerHeight` | 返回窗口的总高度 | JavaScript 1.2 | Netscape 4 或更高版本 |
| `outerWidth` | 返回窗口的总宽度 | JavaScript 1.2 | Netscape 4 或更高版本 |
| `pageXOffset` | 返回页面位置相对于页面左边缘的偏移 | JavaScript 1.2 | |
| `pageYOffset` | 返回页面位置相对于页面顶边缘的偏移 | JavaScript 1.2 | |
| `parent` | 指向当前窗口的父窗口或帧 | JavaScript 1.0 | 只读 当当前窗口是帧时 |
| `personalbar` | 显示或隐藏个人栏 | JavaScript 1.1 | 只读 Netscape 4 或更高版本 |
| `screen` | 指向窗口的 Screen 对象 | JavaScript 1.0 | 只读 |
| `screenX` | 指定窗口左上角的 x 坐标 | JavaScript 1.1 | Netscape 4 或更高版本 |
| `screenY` | 指定窗口左上角的 y 坐标 | JavaScript 1.1 | Netscape 4 或更高版本 |
| `scrollbars` | 指定滚动条的可见性 | JavaScript 1.1 | 只读 Netscape 4 或更高版本 |
| `self` | 指向窗口本身 | JavaScript 1.0 | Netscape 可读写 IE 只读 也 window |
| `sidebar` | 指定侧边栏的可见性 | JavaScript 1.2 | 只读 Netscape 6 或更高版本 |
| `status` | 指定状态行的当前内容 | JavaScript 1.0 | 可读写 |
| `statusbar` | 指定状态栏的可见性 | JavaScript 1.1 | Netscape 4 或更高版本 |
| `toolbar` | 指定工具栏的可见性 | JavaScript 1.1 | Netscape 4 或更高版本 |
| `top` | 返回顶层浏览器窗口对象 | JavaScript 1.0 | 只读 |
| `window` | `window.window` 等于 `window` | | 只读 |

### 表 5-5. Window 方法

| 方法 | 描述 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `alert()` | 显示一个警告框 | JavaScript 1.0 | |
| `atob()` | 解码 Base-64 编码字符串 | JavaScript 1.1 | 仅限 Netscape 4.x，在 Netscape 6+ 中不起作用 |
| `back()` | 上一页的 URL | JavaScript 1.1 | 仅限 Netscape 4+ |
| `blur()` | 移除键盘焦点 | JavaScript 1.1 | |
| `btoa()` | 将数据编码为 Base-64 | JavaScript 1.1 | |
| `captureEvents()` | 允许捕获某些事件 | JavaScript 1.1 | 仅限 Netscape 4+ |
| `clearInterval()` | 取消对应的 `setInterval` 方法 | JavaScript 1.2 | |
| `clearTimeout()` | 清除指定的超时 | JavaScript 1.2 | |
| `close()` | 关闭顶层浏览器 | JavaScript 1.0 | |
| `confirm()` | 返回带有 OK 或 CANCEL 的对话框 | JavaScript 1.0 | |
| `disableExternalCapture()` | 不允许签名脚本捕获页面中的事件 | JavaScript 1.2 | 仅限 Netscape 4+ |
| `enableExternalCapture()` | 允许签名脚本捕获页面中的事件 | JavaScript 1.2 | 仅限 Netscape 4+ |
| `escape()` | 将 ASCII 字符转换为 HEX 字符 | JavaScript 1.2 | |
| `execScript()` | 允许在特定语言中执行脚本 | JavaScript 1.2 | 仅限 IE 4+ |
| `find()` | 允许在当前文档中查找 | JavaScript 1.2 | 仅限 Netscape 4+ |
| `focus()` | 给当前窗口赋予键盘焦点 | JavaScript 1.1 | |
| `forward()` | 返回浏览器历史中的下一个文档 | JavaScript 1.1 | 仅限 Netscape 4+ |
| `home()` | 将用户发送到其主 URL | JavaScript 1.1 | 仅限 Netscape 4+ |
| `moveBy()` | 将窗口移动到相对位置 | JavaScript 1.2 | |
| `moveTo()` | 将窗口移动到绝对位置 | JavaScript 1.2 | |
| `navigate()` | 将浏览器发送到新 URL | JavaScript 1.0 | IE 3 或更高版本 |
| `open()` | 打开一个新浏览器窗口 | JavaScript 1.0，在 JavaScript 1.1 中增强 | |
| `print()` | 打印文档 | JavaScript 1.1 | Netscape 4+ |
| `prompt()` | 获取用于输入字符串 | JavaScript 1.0 | |
| `releaseEvents()` | 用于释放之前捕获的事件 | JavaScript 1.1 | 仅限 Netscape 4+ |
| `resizeBy()` | 调整窗口大小 | JavaScript 1.2 | |
| `resizeTo()` | 用于将窗口调整为特定大小 | JavaScript 1.2 | |
| `routeEvents()` | 用于路由之前捕获的事件 | JavaScript 1.2 | Netscape 4+ |
| `scroll()` | 用于自动将用户移动到当前窗口的任何点 | JavaScript 1.1 | Netscape 6 或更高版本 |
| `scrollBy()` | 按值指定的数值滚动窗口的可视区域 | JavaScript 1.2 | |
| `scrollTo()` | 将可视窗口滚动到精确的像素位置 | JavaScript 1.2 | |
| `setHotKeys()` | 允许或禁止使用键盘快捷键 | JavaScript 1.2 | |
| `setInterval()` | 用于调用 JavaScript 函数或评估表达式 | JavaScript 1.2 | Netscape 4 或更高版本，对 IE 4+ 部分支持 |
| `setResizable()` | 允许或禁止调整窗口大小 | JavaScript 1.2 | |
| `setTimeout()` | 暂停 JavaScript 的执行 | JavaScript 1.0 | |
| `setZOptions()` | 控制窗口堆叠顺序 | JavaScript 1.2 | |
| `showModalDialog()` | 创建一个显示文档的模态对话框 | JavaScript 1.2 | IE 4 或更高版本 |
| `showModelessDialog()` | 创建一个显示文档的非模态对话框 | JavaScript 1.3 | IE 5 或更高版本 |
| `stop()` | 停止加载文档 | JavaScript 1.1 | |
| `unescape()` | 将 HEX 字符转换为 ASCII 字符 | JavaScript 1.2 | |

### window._content

`_content` 属性用于显示当前窗口的内容。

```javascript
// 如果你的 URL 是：
// http://www.mcgraw-hill.com/index.html
document.write(window._content.location.host);
// 这将打印：www.mcgraw-hill.com
```

### window.alert()

`alert()` 方法用于显示用户对话框。对话框包含你提供的文本以及一个 OK 按钮。该方法的语法如下：

```javascript
window.alert("message");
```

### window.atob() and window.btoa()

`atob()` 和 `btoa()` 方法分别解码和编码 base-64 字符串，并将结果作为字符串返回。

```javascript
var encode = btoa("encode this text");
var decode = window.atob("ZGVjb2RlIHRoaXMgdGV4dA==");
document.write(encode);
document.write(decode);
```

这返回编码后的字符串 `ZW5jb2RlIHRoaXMgdGV4dA==`，随后是解码后的字符串 `decode this text`。注意，我没有给 `atob()` 传递相同的 `btoa()` 编码字符串。

### window.back()

`back()` 方法返回一个包含之前访问过的页面 URL 的字符串。

### window.blur()

`blur()` 方法从 Window 对象中指定的顶层浏览器窗口移除键盘焦点。

### window.captureEvents()

`captureEvents()` 方法可用于 Window（或 Document）对象上设置事件，以处理单个或多个事件，这些事件通常将由不同的文档元素处理。例如：

```javascript
window.captureEvents(Event.CLICK | Event.DBLCLICK);
```

该示例设置窗口捕获所有的点击和双击事件（`onclick` 和 `ondblclick`）。

| 选项 | 描述 |
|---|---|
| 返回 true | 任何捕获的元素将执行其默认操作。 |
| 返回 false | 元素的默认操作将不会发生。 |
| 调用 route 方法 | 将导航到该 URL。 |
| 调用 handle 方法 | 将搜索其他事件。 |

### window.clearInterval()

`clearInterval` 方法取消一个对应的 `setInterval` 方法。语法如下：

```javascript
window.clearInterval(MyInterval);
```

### window.clearTimeout()

`clearTimeout` 方法用于通过 `setTimeout` 方法的 ID 来清除指定的超时。语法如下：

```javascript
window.clearTimeout(MyTimeout);
```

### window.close()

`close()` 方法关闭一个顶层浏览器窗口。

### window.closed

`closed` 属性是一个只读布尔值，确定窗口是否已关闭。关闭的 Window 对象并非简单的消失；它们的 `window.closed` 属性会被设置为 true。

### window.confirm()

`confirm()` 方法返回对话框，提示用户按 OK 或 CANCEL。对话框内有一个可以定义的消息。语法如下：

```javascript
window.confirm("Question Here");
```

### window.crypto

`crypto` 属性是与窗口关联的 Crypto 对象的引用。此属性仅适用于 Netscape 4+。

### window.dialogArguments

`dialogArguments` 属性返回创建引用模态对话框时使用的任何参数。注意此属性仅适用于通过 `showModalDialog` 方法创建的窗口。

### window.dialogHeight

`dialogHeight` 属性反映引用模态对话框的高度。它是 `showModalDialog` 方法的功能之一。

### window.dialogLeft

`dialogLeft` 属性反映引用模态对话框相对于桌面左边的水平偏移。它是 `showModalDialog` 方法的功能之一。

### window.dialogTop

`dialogTop` 属性反映引用模态对话框相对于桌面顶部的垂直偏移。它是 `showModalDialog` 方法的功能之一。

### window.dialogWidth

`dialogWidth` 属性反映引用模态对话框的宽度。它是 `showModalDialog` 方法的功能之一。

### window.disableExternalCapture()

`disableExternalCapture()` 方法禁止浏览器接受来自不同服务器的信息。

### window.document

`document` 属性包含引用窗口的 Document 对象。Document 对象拥有有关在浏览器窗口对象中查看的当前文档信息的属性，例如：

```javascript
myLinkColor = parent.document.linkColor;
```

### window.enableExternalCapture()

`enableExternalCapture()` 方法允许浏览器接受来自不同服务器的信息。

### window.escape() and window.unescape()

`escape()` 和 `unescape()` 方法分别将 ASCII 字符转换为 HEX（十六进制）字符，反之亦然。HEX 字符以 `%xx` 格式返回。

```javascript
var escaped = window.escape("s+~!@#$%^&*()\n\t");
var unescaped = window.unescape(escaped);
document.write(escaped);
document.write("<BR>");
document.write(unescaped);
```

第一个返回字符串 `s+%7E%21%40%23%24%25%5E%26*%28%29%0A%09`，可以看出这是编码后的字符串。第二个的字符串是 `s+~!@#$%^&*()`，这是传入的原始字符串。

### window.event

`event` 属性包含有关最近事件的详细信息。在 IE 4 中，没有 Event 对象传递给事件处理器，因此事件处理器必须从 window 对象的 `event` 属性获取事件信息。

### window.execScript()

`execScript()` 方法可用于执行特定语言的脚本函数。

### window.find()

`find()` 方法调用浏览器的查找窗口，允许用户在当前文档中搜索任何文本。其效果相当于用户使用了“编辑”菜单中的“查找”命令。

### window.focus()

`focus()` 方法将键盘焦点赋予 Window 对象指定的窗口。

### window.forward()

`forward()` 方法类似于浏览器的前进按钮，如果可用，则将用户移动到下一页。

### window.frames[]

`frames[]` 数组包含当前窗口中任何帧的引用。你可以通过名称或元素编号引用帧。也可以使用 `length` 属性，例如 `document.frames.length`。

### window.history

`history` 属性包含浏览器当前历史列表的只读列表（最近访问的站点列表）。

### window.home()

`home()` 方法将用户发送到其主页 URL。这仅在 Netscape 4+ 中有效。

### window.innerHeight

`innerHeight` 属性指的是窗口文档显示区域的高度（以像素为单位）。这不包括菜单栏、工具栏等。

### window.innerWidth

`innerWidth` 属性指的是窗口文档显示区域的宽度（以像素为单位）。这不包括菜单栏、工具栏等。

### window.length

`length` 属性包含窗口中包含的帧数，默认值为 0。

### window.location

`location` 属性指向窗口的 Location 对象。它指定了当前文档的 URL。

### window.locationbar

`locationbar` 属性允许你隐藏或显示位置栏。该属性的语法如下：

```javascript
window.locationbar.visibility;
```

### window.menubar

`menubar` 属性允许你隐藏或显示菜单。该属性的语法如下：

```javascript
window.menubar.visibility;
```

### window.moveBy()

`moveBy()` 方法可以相对于其当前位置移动 Navigator 窗口。

### window.moveTo()

`moveTo()` 方法可以通过移动 Navigator 的左上角到指定位置，将 Navigator 窗口移动到屏幕上的特定点。

### window.name

`name` 属性指定窗口的名称。如果窗口未命名，则返回空值。

### window.navigate()

`navigate()` 方法将浏览器发送到新的 URL。此方法在 IE 4+ 中有效。

```javascript
var newURL = window.navigate("http://www.mcgrawhill.com");
document.write(newURL);
```

### window.offscreenBuffering

`offscreenBuffering` 设置为字符串值 `auto`，它决定了是否需要离屏缓冲。可以在脚本函数中通过显式将 `offscreenBuffering` 属性设置为 true 或 false 来覆盖它。一旦设置完成（无论以何种方式），它将返回一个布尔值，表示是否启用了离屏缓冲。

### window.onblur

`onblur` 属性指定事件处理器函数，该函数在窗口失去键盘焦点时被调用。

### window.ondragdrop

当用户对窗口上的对象使用系统拖放功能时，会调用 `ondragdrop`。

### window.onerror

发生 JavaScript 错误时，会调用 `onerror` 属性。

### window.onfocus

`onfocus` 属性在窗口获得键盘焦点时被调用。

### window.onload

`onload` 属性在文档完成加载时被调用。

### window.onmove

`onmove` 属性在窗口移动时被调用。

### window.onresize

`onresize` 属性在窗口调整大小时被调用。

### window.onunload

当窗口或帧集卸载以加载另一个页面代替其位置时，会调用 `onunload` 属性。

### window.open()

`open()` 方法使用以下语法打开一个新的浏览器窗口：

```javascript
window.open(url, name, features, replace);
```



## window.open()

### 参数

| 参数 | 描述 |
| --- | --- |
| `url` | 指定在新窗口中显示的 URL；如果省略，则新窗口将为空。 |
| `name` | 新窗口的可选名称，允许你使用 `TARGET`。 |
| `features` | 指定窗口的特性。 |
| `replace` | 如果设置为 `true`，则当前页面将被新页面替换。 |

> **注**：`window.open` 表格的 OCR 文本在源文件中已严重破碎；我已根据提供的上下文重建了标准的 `window.open` 参数。

第一个返回字符串 `s+%7E%21%40%23%24%25%5E%26*%28%29%0A%09`，可以看出这是编码后的字符串。第二个返回的字符串是 `s+~!@#$%^&(*)`，这是传入的原始字符串。

---

## 窗口特性

| 特性 | 描述 | 浏览器 |
| --- | --- | --- |
| `alwaysLowered` | 将窗口发送到所有窗口的底部 | Netscape 4+ |
| `alwaysRaised` | 将窗口发送到所有窗口的顶部 | Netscape 4+ |
| `channelmode` | 决定窗口是否以通道模式显示 | IE 4+ |
| `dependent` | 指定窗口是否为当前窗口的子窗口 | Netscape 4+ |
| `fullscreen` | 决定浏览器是否为全屏模式 | IE 4+ |
| `height` | 指定窗口的高度 | |
| `hotkeys` | 禁用键盘快捷键 | Netscape 4+ |
| `innerHeight` | 指定文档显示区域的高度 | Netscape 4+ |
| `innerWidth` | 指定文档显示区域的宽度 | Netscape 4+ |
| `left` | 窗口的 X 坐标（像素为单位） | IE 4+ |
| `location` | URL 栏 | |
| `menubar` | 菜单栏，包括文件、编辑等。 | |
| `outerHeight` | 指定窗口的总高度 | Netscape 4+ |
| `outerWidth` | 指定窗口的总宽度 | Netscape 4+ |
| `resizable` | 允许调整窗口大小 | |
| `screenX` | 窗口的 X 坐标（像素为单位） | Netscape 4+ |
| `screenY` | 窗口的 Y 坐标（像素为单位） | Netscape 4+ |
| `scrollbars` | 启用水平和垂直滚动条 | |
| `status` | 状态栏 | |
| `toolbar` | 带有后退和前进按钮的工具栏 | |
| `top` | 窗口的 Y 坐标（像素为单位） | IE 4+ |
| `width` | 窗口文档显示区域的宽度（像素为单位） | |
| `z-lock` | 指定窗口不在堆叠顺序中置顶 | Netscape 4+ |

**表 5-6. 窗口特性**

---

## window 对象属性与方法

### window.opener

`opener` 属性返回创建当前窗口的窗口引用（通过 `window.open()` 创建）。它可以与进一步的对象属性（如 `location` 等）配合使用，以访问打开当前窗口的窗口/文档的属性，或使用方法（如 `close()`）自动关闭创建当前窗口的窗口。

### window.outerHeight

`outerHeight` 属性返回表示引用窗口总高度（包括工具栏、滚动条等）的值。

### window.outerWidth

`outerWidth` 属性返回表示引用窗口总宽度（包括工具栏、滚动条等）的值。

### window.parent

在普通文档窗口中，`parent` 属性指向窗口本身。在框架结构文档中，`parent` 属性指向文档所在的框架集文档。

### window.personalbar

`personalbar` 属性具有一个 `visible` 布尔属性。语法如下：

```javascript
window.personalbar.visible = false
```

### window.print()

`print()` 方法打印当前文档，与打印按钮相同。

### window.prompt()

`prompt()` 方法提示用户进行输入。此消息框上有三个按钮：确定（OK）、清除（Clear）和取消（Cancel）。语法如下：

```javascript
window.prompt(message, default);
```

| 按钮 | 描述 | 返回值 |
| --- | --- | --- |
| OK | 提交数据 | 用户输入的数据 |
| Clear | 清空数据 | 无 |
| Cancel | 取消输入 | `null` |

### window.releaseEvents()

`releaseEvents()` 方法用于释放之前通过 `captureEvents()` 方法捕获的事件。释放单个或多个事件的语法与 `captureEvents()` 方法相同。

### window.resizeBy()

`resizeBy()` 方法根据指定的数值按当前大小调整窗口尺寸。语法如下：

```javascript
self.resizeBy(x, y)
```

### window.resizeTo()

`resizeTo()` 方法用于将窗口调整为特定大小。语法如下：

```javascript
self.resizeTo(x, y)
```

### window.routeEvent()

`routeEvent()` 方法用于路由之前通过 `captureEvents()` 方法捕获的事件。语法如下：

```javascript
objectReference.routeEvent(eventType)
```

### window.screen

`screen` 属性提供指向 `Screen` 对象的引用，用于获取用户当前分辨率等属性。

### window.screenX

`screenX` 属性指的是窗口左上角的 X 坐标。如果窗口是一个框架，则该属性指定包含该框架的左上角窗口。

### window.screenY

`screenY` 属性指的是屏幕上窗口左上角的 Y 坐标。如果窗口是一个框架，则该属性指定包含该框架的左上角窗口。

### window.scroll()

`scroll()` 方法可以自动将用户移动到当前窗口任何位置。它与页内锚点类似，不同之处是它将用户移动到像素值位置，而不是链接。语法如下：

```javascript
SomeWindow.scroll(x, y)
```

### window.scrollbars

`scrollbars` 属性具有一个布尔属性 `visible`。语法如下：

```javascript
window.scrollbars.visible = false
```

### window.scrollBy()

`scrollBy()` 方法根据指定的数值滚动窗口可视区域。语法如下：

```javascript
self.scrollBy(x, y)
```

### window.scrollTo()

`scrollTo()` 方法根据给定的值将可视窗口滚动到精确像素位置。语法如下：

```javascript
self.scrollTo(x, y)
```

### window.self

`window.self` 属性包含当前 `Window` 对象的引用。该属性与 `window` 相同。

### window.setHotKeys()

`setHotKeys()` 方法允许你启用或禁用用户使用快捷键。仅适用于没有菜单栏的窗口。语法如下：

```javascript
window.setHotKeys(boolean_value);
```

### window.setInterval()

`setInterval()` 方法允许 JavaScript 以毫秒为间隔连续执行代码。语法如下：

```javascript
window.setInterval(string, interval);
window.setInterval(function, interval, arguments);
```

| 参数 | 描述 | 注意事项 |
| --- | --- | --- |
| `string` | 包含应按间隔执行的 JavaScript 字符串；多个字符串用分号隔开 | |
| `function` | 应按间隔执行的函数 | |
| `interval` | 间隔时间（毫秒） | |
| `arguments` | 传递给函数的参数 | |

### window.setResizable()

`setResizable()` 方法允许启用或禁用用户调整窗口大小的能力。语法如下：

```javascript
window.setResizable(boolean)
```

### window.setTimeout()

`setTimeout()` 方法允许在延迟后执行函数或字符串。语法如下：

```javascript
window.setTimeout(string, delay);
window.setTimeout(function, delay, arguments);
```

| 参数 | 描述 |
| --- | --- |
| `string` / `function` | 要执行的代码或函数 |
| `delay` | 延迟时间（毫秒） |
| `arguments` | 传递给函数的参数 |

### window.setZOptions()

`setZOptions()` 方法允许指定窗口的层级行为。语法如下：

```javascript
window.setZOptions(option);
```

| 选项 | 描述 |
| --- | --- |
| `"alwaysRaised"` | 窗口始终位于最顶层 |
| `"alwaysLowered"` | 窗口始终位于底部 |
| `"lock"` | 窗口层级被锁定 |
| `"normal"` | 窗口按正常顺序显示 |

### window.showHelp()

`showHelp()` 方法显示帮助文件。语法如下：

```javascript
window.showHelp(URL);
```

### window.showModalDialog() 和 window.showModelessDialog()

`showModalDialog()` 和 `showModelessDialog()` 方法创建一个显示文档的对话框。`showModalDialog()` 对话框与 `alert()` 类似，用户无法操作原始窗口。`showModelessDialog()` 对话框类似，但用户可以与底层窗口交互。

语法如下：

```javascript
window.showModalDialog(URL, arguments, features);
window.showModelessDialog(URL, arguments, features);
```

| 参数 | 描述 |
| --- | --- |
| `URL` | 传递给对话框的 URL |
| `arguments` | 用于对话框的参数 |
| `features` | 用于对话框的特性 |

#### 对话框特性

| 特性 | 描述 | 数值 |
| --- | --- | --- |
| `dialogHeight` | 设置对话框的高度，最小为 100 | 像素 |
| `dialogWidth` | 设置对话框的宽度 | 像素 |
| `dialogLeft` | 设置对话框相对于左上角的 X 坐标 | 像素 |
| `dialogTop` | 设置对话框相对于左上角的 Y 坐标 | 像素 |
| `center` | 在桌面上居中对话框，默认是 | 是/否 (1/0) |
| `help` | 是否在对话框显示帮助图标 | 是/否 (1/0) |
| `resizable` | 对话框是否可以调整，默认均为否 | 是/否 (1/0) |
| `status` | 是否在对话框显示状态栏，默认是 | 是/否 (1/0) |

### window.status

`status` 属性允许更改状态栏的内容，例如：

```javascript
self.status = "新状态栏文本";
```

### window.statusbar

`statusbar` 属性具有一个布尔属性 `visible`。语法如下：

```javascript
window.statusbar.visible = false
```

### window.stop()

`stop()` 方法的功能与“停止”按钮相同。它停止窗口加载。

### window.toolbar

`toolbar` 属性具有一个布尔属性 `visible`。语法如下：

```javascript
window.toolbar.visible = false
```

### window.top

`top` 属性返回最顶层浏览器窗口的 `Window` 对象。

### window.window

`window` 属性与 `window.self` 属性相同。

### window.screenX / window.screenY (Page Offset)

`screenX` 属性反映了当前水平位置与页面左边缘之间的差异。当页面进行水平滚动时，`screenX` 会增加或减少，如果当前可视区域是页面的左边缘，则值为 0。（注意：这与 Internet Explorer 的 `scrollLeft` 属性相似，但两者是不兼容的。）

`screenY` 属性反映了页面当前垂直位置与页面顶部边缘之间的差异。当页面进行垂直滚动时，`screenY` 会增加或减少，如果当前可视区域是页面的顶部，则值为 0。（注意：这与 Internet Explorer 的 `scrollTop` 属性相似，但两者是不兼容的。）

---

## Document 对象

文档属性可以是单个属性，也可以是属性数组。例如，`anchors[]` 指向文档中的锚点对象。这些数组像普通数组一样从数字 0 开始，代表该属性第一个实例。

### 文档属性列表

| 属性 | 说明 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `activeElement` | 返回当前活动元素 | JavaScript 1.2 | 仅限 IE 4+ |
| `alinkColor` | 用户点击链接时的颜色；对应 `<body>` 的 `ALINK` 属性 | JavaScript 1.0 | |
| `all` | 包含文档所有元素的数组 | JavaScript 1.2 | 仅限 IE 4+ |
| `anchors[]` | 文档中锚点的数组 | JavaScript 1.0 | |
| `applets[]` | 文档中 applet 的数组 | JavaScript 1.1 | |
| `attributes` | 属性信息的无序集合 | JavaScript 1.3 | 仅限 Netscape 6+ |
| `bgColor` | 文档背景色；对应 `<body>` 的 `BGCOLOR` 属性 | JavaScript 1.0 | |
| `body` | 包含 `<body>` 元素的所有内容 | JavaScript 1.2 | Netscape 6+ 可读写，IE 4+ 只读 |
| `characterSet` | 浏览器的字符集 | JavaScript 1.3 | 仅限 Netscape 6+ |
| `childNodes` | 包含文档中每个元素的信息 | JavaScript 1.2 | Netscape 6+ 可读写，IE 4+ 只读 |
| `cookie` | 允许 JavaScript 读写 HTTP cookies | JavaScript 1.0 | |
| `defaultCharset` | 包含字符信息 | JavaScript 1.2 | 仅限 IE 5.5+ |
| `documentElement` | 包含根文档信息 | JavaScript 1.3 | 仅限 Netscape 6+ |
| `domain` | 允许同域内的受信任服务器减少页面间交互的某些安全限制 | JavaScript 1.1 | |
| `embeds[]` | 文档中嵌入对象的数组 | JavaScript 1.1 | |
| `expando` | 接受一个布尔值，决定是否可以声明任意属性 | JavaScript 1.2 | 仅限 Internet Explorer 4+ |
| `fgColor` | 文档文本颜色；对应 `<body>` 的 `TEXT` 属性 | JavaScript 1.0 | |
| `fileCreatedDate` | 文件创建日期 | JavaScript 1.2 | 仅限 IE 4+ |
| `fileModifiedDate` | 文件修改日期 | JavaScript 1.2 | 仅限 IE 4+ |
| `fileSize` | 文件大小 | JavaScript 1.2 | 仅限 IE 4+ |
| `fileUpdatedDate` | 文件更新日期 | JavaScript 1.2 | 仅限 IE 4+ |
| `forms[]` | 文档中表单对象的数组 | JavaScript 1.0 | |
| `frames[]` | 包含 `<iframe>` 标签的数组 | JavaScript 1.1 | 仅限 Netscape 6+ 和 IE 4+ |
| `height` | 包含文档高度 | JavaScript 1.0 | Netscape 4+ |
| `images[]` | 文档中图像对象的数组 | JavaScript 1.1 | |
| `lastModified` | 文档修改日期 | JavaScript 1.0 | |
| `linkColor` | 文档中未访问链接的颜色；对应 `<body>` 的 `LINK` 属性 | JavaScript 1.0 | |
| `links[]` | 包含文档中每个链接的数组 | JavaScript 1.0 | |
| `location` | 已弃用——与 `URL` 相同 | | 参见 `URL` |
| `mimeType` | 包含当前文档的 MIME 类型 | JavaScript 1.2 | 仅限 IE 5.5+ |
| `nameProp` | 包含文档标题 | JavaScript 1.2 | 仅限 IE 5.5+ |
| `parentWindow` | 返回被引用文档的父窗口 | JavaScript 1.2 | 仅限 IE 5.5+ |
| `readyState` | 包含文档的加载状态 | JavaScript 1.0 | |
| `referrer` | 用户上次点击的 URL | JavaScript 1.0 | |
| `scripts[]` | 文档中脚本的数组 | JavaScript 1.0 | |
| `selection` | 选中的内容 | JavaScript 1.2 | |
| `styleSheets[]` | 文档中样式表的数组 | JavaScript 1.2 | |
| `title` | `<title>` 和 `</title>` 之间的文本 | JavaScript 1.0 | |
| `vlinkColor` | 文档中已访问链接的颜色 | JavaScript 1.0 | |
| `width` | 文档宽度 | JavaScript 1.0 | |

**表 5-8. 文档属性及说明**

### 文档方法列表

| 方法 | 说明 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `clear()` | 清空文档 | JavaScript 1.0 | 已弃用 |
| `close()` | 关闭文档输出流 | JavaScript 1.0 | |
| `createElement()` | 创建元素 | JavaScript 1.2 | |
| `createStyleSheet()` | 创建样式表 | JavaScript 1.2 | 仅限 IE |
| `elementFromPoint()` | 获取指定点的 HTML 元素 | JavaScript 1.0 | |
| `execCommand()` | 在文档中执行命令 | JavaScript 1.0 | |
| `getSelection()` | 返回选中文本 | JavaScript 1.2 | |
| `open()` | 打开文档输出流 | JavaScript 1.1 | |
| `queryCommandEnabled()` | 确定命令是否可用 | JavaScript 1.1 | |
| `queryCommandIndeterm()` | 确定命令是否处于确定状态 | JavaScript 1.1 | |
| `queryCommandState()` | 确定命令的状态 | JavaScript 1.1 | |
| `queryCommandSupported()` | 确定命令是否支持 | JavaScript 1.1 | |
| `queryCommandText()` | 确定命令相关的字符串 | JavaScript 1.1 | |
| `queryCommandValue()` | 确定命令的值 | JavaScript 1.1 | |
| `write()` | 向文档写入数据 | JavaScript 1.0 | |
| `writeln()` | 向文档新行写入数据 | JavaScript 1.0 | |

**表 5-9. 文档方法及说明**

---

### document.activeElement

`activeElement` 属性返回文档中当前活动元素（获得焦点的元素）。

### document.all

`all` 属性是文档内所有元素的数组。

### document.alinkColor, document.bgColor, document.fgColor, document.linkColor, document.vlinkColor

这些属性返回其 `<body>` 对应的颜色，如下表所示。Netscape 4 和 IE 4+ 总是返回十六进制值，而 Netscape 6+ 返回输入的值。

| 属性 | 对应项 |
| --- | --- |
| `alinkColor` | `ALINK` |
| `bgColor` | `BGCOLOR` |
| `fgColor` | `TEXT` |
| `linkColor` | `LINK` |
| `vlinkColor` | `VLINK` |

测试示例：

```html
<html>
<head><title>Color Test</title></head>
<body link="blue" text="white" alink="pink" vlink="green" bgcolor="black">
<pre>
<script type="text/javascript">
document.write("alinkColor : " + document.alinkColor + "\n");
document.write("bgColor : " + document.bgColor + "\n");
document.write("fgColor : " + document.fgColor + "\n");
document.write("linkColor : " + document.linkColor + "\n");
document.write("vlinkColor : " + document.vlinkColor + "\n");
</script>
</pre>
</body>
</html>
```

### document.anchors[]

`anchors[]` 数组包含页面中所有的锚点。锚点被表示为 `<a name="name"></a>`。此属性也可以与 `length` 属性一起使用，例如 `document.anchors.length`。

```javascript
var test = document.anchors;
document.write(test);
```

不同浏览器返回值差异：

| 浏览器 | 返回 |
| :--- | :--- |
| Netscape 4+ | `[object AnchorArray]` |
| Netscape 6+ | `[object HTMLCollection]` |
| IE 4+ | `[object AnchorArray]` |

### document.applets[]

`applets[]` 数组包含文档中所有的 applet 对象。可与 `length` 属性一起使用，如 `document.applets.length`。也可通过名称请求 applet，例如 `document.applets["name"]`。

### document.attributes

`attributes` 属性是属性信息项目的无序集合，对应该元素的每个属性（指定的或从 DTD 默认继承的）。

### document.body

`body` 属性包含 `<body>` 元素的内容。此属性仅适用于 Netscape 6+ 和 IE 4+。

### document.characterSet

`characterSet` 属性包含来自浏览器 `charset` 的字符集信息。此属性仅适用于 Netscape 6+。

```javascript
var chrset = document.characterSet;
document.write(chrset);
// 这在我的浏览器中返回 ISO-8859-1。
```

### document.childNodes

`childNodes` 属性包含关于文档中每个元素的信息。

示例 HTML 结构：
```html
<html>
<head>
  <title>This is the document's title</title>
</head>
<body>
  <h3>This is a heading 3</h3>
  <p>This is a paragraph.</p>
  <p>It contains <br> several paragraphs.</p>
  <p>This paragraph, has several, children.</p>
</body>
</html>
```
这个示例有两个子元素：`HEAD` 和 `BODY`。`HEAD` 有一个子元素 `TITLE`，而 `BODY` 有四个子元素：一个 `H3` 和三个 `P`。

修改最后一段文本的代码：
```javascript
document.childNodes[1].childNodes[3].firstChild.nodeValue = 'new text';
```

### document.clear()

`clear()` 方法用于清除当前文档。该方法已弃用。

### document.close()

`close()` 方法显示任何已写入但尚未显示的文档输出；然后关闭指向文档的输出流。在使用 `document.write()` 生成 HTML 页面时，你应该在页面结束时调用 `document.close()`。

### document.cookie

`cookie` 属性允许 JavaScript 读写 HTTP cookies。

### document.createElement()

`createElement()` 方法动态创建元素（如 `<img>` 或 `<option>`）并将其添加到相应集合中。

```javascript
var myOption = document.createElement("OPTION");
document.forms[0].elements["mySelect"].options.add(myOption, 0);
```

### document.createStyleSheet()

`createStyleSheet()` 方法可用于向引用的文档创建并添加一个 `StyleSheet` 对象（仅限 IE）。

### document.defaultCharset

`defaultCharset` 属性包含关于文档默认字符集的信息。此属性仅在 IE 4+ 中有效。

```javascript
var charset = document.defaultCharset;
document.write(document.defaultCharset);
// 我的电脑返回：windows-1252
```

### document.documentElement

`documentElement` 属性包含关于子节点的根节点文档信息。此属性在 IE 4+ 和 Netscape 6+ 中有效。

### document.domain

`domain` 属性可用于设置或返回文档的安全域，这将允许来自不同服务器的文档进行相互通信。例如，如果你为 `www.example.com` 和 `test.example.com` 准备了不同的服务器，从每个服务器加载的文档最初无法通信，除非在所有需要共享的文档中设置了 `document.domain = "example.com"`。

### document.elementFromPoint()

`elementFromPoint()` 方法确定指定点的 HTML 元素。语法为：

```javascript
document.elementFromPoint(x, y)
```

### document.embeds[]

`embeds[]` 数组包含文档中的每个嵌入对象。你可以使用 `document.embeds[0]` 引用嵌入元素，或通过元素名称使用 `document.embeds["name"]`。此属性也可以与 `length` 属性一起使用，如 `document.embeds.length`。

### document.execCommand()

`execCommand()` 方法可对整个文档或文本范围执行多个命令。语法为：

```javascript
object.execCommand(command, boolean, value)
```

#### execCommand() 命令列表

| 命令 | 描述 | 值 |
| :--- | :--- | :--- |
| `InsertParagraph` | 在插入处插入 `<p>` | |
| `InsertInputButton` | 在插入处插入 `<input type="button">` | |
| `InsertInputCheckbox` | 在插入处插入 `<input type="checkbox">` | |
| `InsertInputFile` | 在插入处插入 `<input type="file">` | |
| `InsertInputHidden` | 在插入处插入 `<input type="hidden">` | |
| `InsertInputPassword` | 在插入处插入 `<input type="password">` | |
| `InsertInputRadio` | 在插入处插入 `<input type="radio">` | |
| `InsertInputReset` | 在插入处插入 `<input type="reset">` | |
| `InsertInputSubmit` | 在插入处插入 `<input type="submit">` | |
| `InsertInputText` | 在插入处插入 `<input type="text">` | |
| `InsertMarquee` | 在插入处插入 `<marquee>` | |
| `InsertOrderedList` | 在插入处插入 `<ol>` | |
| `InsertSelectDropdown` | 在插入处插入 `<select type="dropdown">` | |
| `InsertSelectListbox` | 在插入处插入 `<select type="list">` | |
| `InsertTextArea` | 在插入处插入 `<textarea>` | |
| `InsertUnorderedList` | 在插入处插入 `<ul>` | |
| `InsertItalic` | 包裹 `<i>` 引用对象 | |
| `JustifyCenter` | 居中引用对象 | |
| `JustifyFull` | 两端对齐引用对象 | |
| `JustifyLeft` | 左对齐引用对象 | |
| `JustifyRight` | 右对齐引用对象 | |
| `Outdent` | 减少引用对象的缩进 | |
| `OverWrite` | 将输入模式设置为插入或覆盖 | 布尔值 - `true` = 覆盖, `false` = 插入 |
| `Paste` | 将剪贴板内容放在当前插入点 | |
| `PlayImage` | 开始播放引用对象的任何动态图像 | |
| `Refresh` | 重新加载当前文档的源 | |
| `RemoveFormat` | 移除引用对象的格式 | |
| `RemoveParaFormat` | 移除引用对象的任何段落格式 | |
| `SelectAll` | 选中整个文档文本 | |
| `StopImage` | 停止所有动态图像的播放 | |
| `Underline` | 在引用的对象周围包裹 `<u>` 标签 | |
| `Unlink` | 移除链接 | |
| `Unselect` | 清空文档的任何选择 | |
| `BackColor` | 设置背景颜色 | |
| `Bold` | 包裹 `<b>` 引用对象 | |
| `Copy` | 将引用对象复制到剪贴板 | |
| `CreateBookmark` | 包裹锚点引用对象 | |
| `CreateLink` | 包裹 `<a>` 引用对象 | |
| `Cut` | 从文档删除引用对象 | |
| `FontName` | 设置对象的字体 | |
| `FontSize` | 设置对象的字体大小 | |
| `ForeColor` | 设置对象的前景（文本）颜色 | |
| `FormatBlock` | 包裹块级引用对象 | |
| `Indent` | 在插入处插入缩进 | |
| `InsertFieldSet` | 在插入处插入 `<fieldset>` | |
| `InsertHorizontalRule` | 在插入处插入 `<hr>` | |
| `InsertIFrame` | 在插入处插入 `<iframe>` | `SRC` |

**表 5-10. execCommand() 命令**

### document.expando

`expando` 属性接受一个布尔值，用于决定是否可以为文档中的任何元素声明任意属性。此属性仅在 IE 4+ 中可用。

### document.fileCreatedDate

`fileCreatedDate` 属性包含当前文档创建的日期。返回的字符串为 `MM/DD/YYYY` 格式。此属性仅适用于 IE 4+。

### document.fileModifiedDate

`fileModifiedDate` 属性包含当前文档修改的日期。返回的字符串为 `MM/DD/YYYY` 格式。此属性仅适用于 IE 4+。

### document.fileSize

`fileSize` 属性包含当前文档的文件大小。返回的字符串是以字节计算的文件大小。此属性仅适用于 IE 4+。

### document.fileUpdatedDate

`fileUpdatedDate` 属性包含当前文档更新的日期。返回的字符串为 `MM/DD/YYYY` 格式。此属性仅适用于 IE 4+。

---

## Form 对象

`form` 对象提供了用于访问 HTML `<form>` 标签属性以及 `<form>` 标签内元素的 JavaScript 属性。它还包含两个方法，允许编码人员使用 JavaScript 提交和重置表单。

### Form 属性和方法

| 属性/方法 | 说明 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `acceptCharset` | 包含接受的字符集 | JavaScript 1.4+ | 仅限 IE 5+ 和 Netscape 6+ |
| `action` | `<form>` 标签 `action` 属性中的路径 | JavaScript 1.0+ | |
| `elements[]` | 包含表单中对象引用的数组 | JavaScript 1.0+ | `length` 属性仅适用于 JS 1.1+ |
| `elements.length` | 表单中元素的数量 | JavaScript 1.1+ | 只读 |
| `encoding` | 表单的 `enctype` 属性 | JavaScript 1.0+ | |
| `length` | 表单中元素的数量 | | 只读 |
| `method` | 在 `<form>` 标签 `method` 属性中设置的 HTTP 方法 | JavaScript 1.0+ | |
| `name` | 表单的名称，在 `<form>` 标签 `name` 属性中设置 | JavaScript 1.0+ | |
| `reset()` | 将表单重置为默认状态 | JavaScript 1.0+ | |
| `submit()` | 提交表单 | JavaScript 1.0+ | |
| `target` | 表单的窗口或框架目标，在 `<form>` 标签 `target` 属性中设置 | JavaScript 1.0+ | |

**表 5-11. Form 属性和方法**

### 定义表单对象

Form 对象是通过在 HTML 页面中插入 `<form>` 标签创建的。

```html
<form
  name="myForm"
  action="script.cgi"
  target="targetFrame"
  method="POST"
  enctype="encoding"
  onreset="goReset()"
  onsubmit="goSubmit()"
>
  <!-- 表单元素位于此处 -->
</form>
```

### Form 事件处理器

| 事件 | 说明 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `onclick` | 用户点击一次。 | JavaScript 1.0 | |
| `ondblclick` | 用户双击。 | JavaScript 1.0 | 仅在 Navigator 4 或 Mac 上有效 |
| `onkeydown` | 用户按下按键。 | JavaScript 1.2 | |
| `onkeypress` | 用户按下并释放按键。 | JavaScript 1.0 | 仅在 Navigator 4 或 Mac 上 |
| `onkeyup` | 用户释放按键。 | JavaScript 1.2 | |
| `onmousedown` | 鼠标按钮按下。 | JavaScript 1.2 | |
| `onmousemove` | 鼠标移动。 | JavaScript 1.2 | |
| `onmouseout` | 鼠标移出元素。 | JavaScript 1.0 | |
| `onmouseover` | 鼠标悬过元素。 | JavaScript 1.0 | |
| `onmouseup` | 鼠标按钮释放。 | JavaScript 1.2 | |
| `onreset` | 表单重置时。 | JavaScript 1.1 | |
| `onsubmit` | 表单提交时。 | JavaScript 1.1 | |

**表 5-12. 可用于 Form 对象的事件处理器**

### Form 对象中的对象

| 名称 | 说明 | JavaScript 版本 | 备注 |
| --- | --- | --- | --- |
| `Button` | 访问按钮元素。 | JavaScript 1.0 | 可通过 HTML 创建 |
| `Checkbox` | 访问复选框元素。 | JavaScript 1.0 | 可通过 HTML 创建 |
| `FileUpload` | 访问文件上传元素。 | JavaScript 1.0 | |
| `Hidden` | 访问隐藏元素。 | JavaScript 1.0 | 可通过 HTML 创建 |
| `Input` | 访问输入元素。 | JavaScript 1.0 | 可通过 HTML 创建 |
| `Password` | 访问密码字段。 | JavaScript 1.0 | |
| `Select` | 访问选择菜单元素。 | JavaScript 1.0 | |
| `Option` | 访问选项元素。 | JavaScript 1.0 | 可通过 HTML 创建 |
| `Radio` | 访问单选框元素。 | JavaScript 1.0 | |
| `Reset` | 访问重置元素。 | JavaScript 1.0 | |
| `Text` | 访问文本元素。 | JavaScript 1.0 | |
| `Textarea` | 访问文本区域元素。 | JavaScript 1.0 | |

**表 5-13. Form 对象中的对象**

---

### Button 对象

按钮是网页上的通用按钮，默认不执行任何操作。不要将这些通用按钮与提交和重置按钮混淆。

#### 定义
通过在 HTML 表单中插入一个 `type` 设置为 `"button"` 的 `<input>` 标签定义。

```html
<form name="myForm">
  <input type="button" name="myButton" value="Click Me" onclick="clicked()">
</form>
```

#### Button 事件属性
按钮对象的事件属性最初设置为与 `<input>` 标签事件处理器属性相同的值。可定义的事件处理器有 `onblur`、`onclick`、`onfocus`、`onmousedown` 和 `onmouseup`。

```javascript
// 访问
alert(document.myForm.myButton.onclick);

// 修改方式 1：函数字面量
document.myForm.myButton.onclick = function() {
    alert("New Function!");
};

// 修改方式 2：引用函数
function functionChange() { alert("New Function!"); }
document.myForm.myButton.onclick = functionChange;
```

| 事件处理器 | JavaScript 版本 | 备注 |
| --- | --- | --- |
| `onclick` | JavaScript 1.0+ | Mac 上的 Netscape 4 中必须返回一个值 |
| `onblur` | JavaScript 1.0+ | Unix 上的 Netscape 3 或更低版本中按钮无效 |
| `onfocus` | JavaScript 1.0+ | Unix 上的 Netscape 3 或更低版本中按钮无效 |
| `onmousedown` | JavaScript 1.2+ | |
| `onmouseup` | JavaScript 1.2+ | |

#### Button.value
`value` 属性初始设置为 `<input>` 标签的 `value` 属性，即显示在按钮上的文本。

```javascript
// 访问
alert(document.myForm.myButton.value);

// 修改
document.myForm.myButton.value = "Don't Click Me!";
```

---

### Checkbox 对象 (复选框)

复选框是在选中和未选中状态之间切换的表单元素。

#### 定义
通过插入 `type="checkbox"` 的 `<input>` 标签定义。通常成组使用，具有相同的 `name`。

```html
<form name="myForm">
您从哪里知道我们的？<br>
<input type="checkbox" name="myBox" value="TV" onclick="clicked()"> 电视<br>
<input type="checkbox" name="myBox" value="Radio" onclick="clicked()"> 收音机 <br>
<input type="checkbox" name="myBox" value="Other" checked onclick="clicked()"> 其他 <br>
</form>
```

在 JavaScript 中被视为对象数组：`document.myForm.myBox[0]` 为第一个。

#### Checkbox.checked
布尔值，可设置为 `true` 或 `false` 以勾选或取消勾选。

```javascript
// 访问
var test = document.myForm.myBox[0].checked;

// 修改单个
document.myForm.myBox[0].checked = true;

// 批量修改
for(var i = 0; i < document.myForm.myBox.length; i++) {
    document.myForm.myBox[i].checked = true;
}
```

#### Checkbox.defaultChecked
只读布尔值，引用复选框的初始状态（由 HTML 中 `checked` 属性指定）。

```javascript
var test = document.myForm.myBox[0].defaultChecked;
```

#### Checkbox 事件属性
事件处理器有 `onblur`、`onclick` 和 `onfocus`。

---

### FileUpload 对象

文件上传字段允许用户选择文件上传。

#### 定义
```html
<form name="myForm" enctype="multipart/form-data">
<input type="file" name="myFile" onchange="handleChange()">
</form>
```

#### FileUpload 事件属性
事件处理器有 `onblur`、`onchange`、`onfocus`。

```javascript
// 访问
alert(document.myForm.myFile.onchange);

// 修改
document.myForm.myFile.onchange = function() { alert("New Function!"); };
// 或
function handleChange() { alert("New Function!"); }
document.myForm.myFile.onchange = handleChange;
```

| 事件处理器 | JavaScript 版本 | Bug |
| --- | --- | --- |
| `onblur` | JavaScript 1.0+ | |
| `onchange` | JavaScript 1.0+ | Netscape 2.0 中 `onchange` 无法访问 `value` 属性 |
| `onfocus` | JavaScript 1.0+ | |

#### FileUpload.value
只读字符串，等同于文件上传字段的值（通常是文件路径）。

```javascript
alert(document.myForm.myFile.value);
```
无法在 JavaScript 中更改此值，也无法通过 HTML `value` 属性设置（安全限制）。

---

### Hidden 对象 (隐藏域)

隐藏字段用于存储客户端和服务器端脚本都会使用的数据。

#### 定义
```html
<form name="myForm">
<input type="hidden" name="myHiddenField" value="Special Data">
</form>
```

#### Hidden.value
初始值为 HTML 中 `value` 属性。

```javascript
// 访问
alert(document.myForm.myHiddenField.value);

// 修改
document.myForm.myHiddenField.value = "Really Special Data";
```

---

### Input 对象 (通用输入元素)

输入元素类型取决于 `<input>` 标签的 `type` 属性。

#### Input.blur()
移除输入元素上的焦点。

```javascript
document.myForm.myTextBox.blur();
```

#### Input.checked
适用于复选框和单选按钮。布尔值。

```javascript
var test = document.myForm.myBox[0].checked;
document.myForm.myBox[0].checked = true;
document.myForm.myRadio[0].checked = true;
```

#### Input.click()
模拟点击复选框、按钮、提交按钮或重置按钮。

```javascript
document.myForm.myButton.click();
```

#### Input.form
返回包含该输入元素的表单引用。

```html
<form name="myForm" action="script.cgi" method="POST">
<input type="button" name="myButton" value="Change Form Action"
onclick="this.form.action='new_script.cgi'">
</form>
```

#### Input.name
初始等于 HTML 中 `<input>` 标签的 `name` 属性。

```javascript
alert(document.myForm.myTextBox.name);
document.myForm.myTextBox.name = 'TextBox2';
```

#### Input.select()
选择文本字段、文本区域、密码字段或文件上传字段中的所有文本。

```javascript
// Netscape 建议先 focus
document.myForm.myTextBox.focus();
document.myForm.myTextBox.select();
```

#### Input.type
只读字符串，指定 Input 对象的类型。

| Input 对象 | `type` 字符串 | HTML 标签 |
| --- | --- | --- |
| Button | `button` | `<input type="button">` |
| Checkbox | `checkbox` | `<input type="checkbox">` |
| FileUpload | `file` | `<input type="file">` |
| Hidden | `hidden` | `<input type="hidden">` |
| Password | `password` | `<input type="password">` |
| Radio | `radio` | `<input type="radio">` |
| Reset | `reset` | `<input type="reset">` |
| Select (无 multiple) | `select-one` | `<select></select>` |
| Select (有 multiple) | `select-multiple` | `<select multiple></select>` |
| Submit | `submit` | `<input type="submit">` |
| Text | `text` | `<input type="text">` |
| Textarea | `textarea` | `<textarea></textarea>` |

**表 5-14. 不同 Input 对象的 type 字符串**

#### Input.value
初始等于 HTML 中 `<input>` 标签的 `value` 属性。表单提交时传递给脚本。

```javascript
// 访问
alert(document.myForm.myTextBox.value);

// 修改
document.myForm.myTextBox.value = "New TextBox Value";
```

| Input 对象类型 | `value` 显示方式 |
| --- | --- |
| Button, Reset, Submit | 按钮上的文字 |
| Text, Textarea, FileUpload | 文本框内的文字 |
| Password | 星号，显示在文本框内 |
| Checkbox, Radio, Hidden | 不显示 `value` |
| Select | `value` 不被直接显示 |

---

### Option 对象

选项是出现在 select 菜单中的菜单项。

#### 定义
通常用 `<option>` 标签指定，位于 `<select>` 标签之间。

```html
<form name="myForm">
  <select name="mySelect">
    <option value="Yahoo">Yahoo!</option>
    <option selected>Google</option>
    <option>dmoz.org</option>
  </select>
</form>
```

#### Option() 构造器
动态创建新选项。接受四个参数：`text`、`value`、`defaultSelected`、`selected`（后两者为 1 或 0）。

```javascript
document.myForm.mySelect.options[3] = new Option("GoTo.com", "goto");
```

#### Option.defaultSelected
只读布尔值，如果选项默认被选中则为 `true`。

```javascript
var test = document.myForm.mySelect.options[1].defaultSelected;
```

#### Option.index
只读，等于选项在 `options[]` 数组中的索引。

```javascript
var i = document.myForm.mySelect.options[2].index; // i 等于 2
```

#### Option.selected
布尔值，如果选项被选中则为 `true`。可读写。

```javascript
var test = document.myForm.mySelect.options[1].selected;
document.myForm.mySelect.options[1].selected = false;
```

#### Option.text
等于页面上 select 菜单中选项显示的文本。JS 1.0 只读，JS 1.1+ 可读写。

```javascript
// 访问
alert(document.myForm.mySelect.options[2].text); // "dmoz.org"

// 修改 (JS 1.1+)
document.myForm.mySelect.options[2].text = "Open Directory";
```

#### Option.value
表单提交时提交给脚本的可选值。初始由 `<option>` 标签的 `value` 属性设置。

```javascript
// 访问
var v = document.myForm.mySelect.options[1].value; // "Yahoo"

// 修改
document.myForm.mySelect.options[1].value = "Yahoo Directory";
```

---

### Password 对象 (密码字段)

密码字段会隐藏用户输入内容，通常显示星号。

#### 定义
```html
<form name="myForm">
<input type="password" name="myPassword" value="pAss" onclick="clicked()">
</form>
```



在密码字段出现在页面之前，无法访问`Password`对象，因此请务必在页面加载后执行的函数中，或者在 HTML 中密码字段`<INPUT>`标签下方的`<SCRIPT>`标签中访问`Password`对象。

JavaScript 可以访问密码字段的几个属性：事件属性和值。

`Password`对象在 JavaScript 1.0 及高版本版本中可用。

`Password.event` `Password`的一个事件属性，其初始值设置为 HTML 中定义密码字段的`<INPUT>`标签的事件处理程序属性的相同，例如`onclick`。可以为密码字段定义的事件处理器有`onblur`、`onclick`和`onclick`。

`Password`对象的事件属性应该等于一个函数或等于`null`，或者你也可以简单地不设置。如果事件属性设置为一个函数，则当执行事件时将执行该函数。如果事件属性设置为`null`或未设置，则表单字段将正常运行，在执行事件时不会执行任何特殊代码。

你可以这样在 JavaScript 中访问`Password`对象的事件属性：

```javascript
alert(document.myForm.myPassword.onclick);

// 访问 onclick 事件属性

// 弹出函数定义代码

// 用于用户确定的 onclick 函数

// 这在 IE 和 Netscape 之间不同
```

你可以通过两种方式用 JavaScript 更改事件属性。你可以将函数字面量赋值给事件属性，如下所示：

```javascript
document.myForm.myPassword.onclick = function() {

  alert("New Function");

};

// 将函数字面量赋值给 onclick 属性
```

或者你可以定义一个函数并将其赋值给事件属性：

```javascript
function onChange() { 

  alert("New Function!");

} // 定义新函数

document.myForm.myPassword.onclick=onChange;

// 将函数赋值给 onchange 属性

// 注意在引用函数时使用了括号 ()
```

在 JavaScript 的不同版本中，`Password`对象提供不同的事件属性，如下表所示。

| 密码对象的事件处理器 | JavaScript 版本 | 缺陷 |
|---|---|---|
| `onBlur()` | JavaScript 1.0 及更高版本 | |
| `onChange()` | JavaScript 1.0 及更高版本 | |
| `onFocus()` | JavaScript 1.0 及更高版本 | |

`Password.value` `Radio`对象的`value`属性初始值设置为与 HTML 中定义密码字段的`<INPUT>`标签的`value`属性相同的值。这是在提交表单时提交给脚本的文本。该值不会显示在 HTML 页面上，但大多数浏览器会为每个字符显示一个星号。

`Password.value`在从初始值更改后，在 JavaScript 1.0 和 1.1 中无法被访问。在 JavaScript 1.2 及更高版本中，你可以读取新值。你可以这样访问此值：

```javascript
alert(document.myForm.myPassword.value);

// 弹出密码的值
```

`Password.value`在实践中是只读的，在理论上却不是。尽管你可以在代码中更改`Password`对象的值，但当提交表单时，浏览器将提交用户最后输入的值，或者提交在它的`value`属性中指定的字段的初始值。

`Password.value`在 JavaScript 1.0 及更高版本中可用。

# 单选

单选按钮是一种表示一组互斥选项的表单元素。例如，你可能在订单表中使用单选按钮，在表单中询问客户希望以何种方式运输订单——通过 UPS、FedEx 还是 DHL。在这个例子中，客户最多可以选择一个选项。不要将单选按钮与之前讨论过的复选框混淆。

`Radio`对象用于通过 JavaScript 访问 HTML 页面中的单选按钮元素。`Radio`对象通过在你的 HTML 中插入一个`type`属性设置为`radio`的`<INPUT>`标签来定义。它们几乎总是成组使用的。为了指明它们是一组，它们应该具有相同的`name`。

```html
<form name="myForm">

您希望如何运输订单？

<input type="radio" name="myRadio" value="ups" onclick="clicked()"> UPS

<input type="radio" name="myRadio" value="fedex" onclick="clicked()"> FedEx

<input type="radio" name="myRadio" value="dhl" checked onclick="clicked()"> DHL <!-- 默认选中。 -->

</form>
```

`Radio`对象在 JavaScript 中作为数组引用，因此`document.myRadio[0]`指向页面上的第一个单选按钮，`document.myRadio[1]`指向第二个，以此此类推。与数组一样，`length`属性在 JavaScript 1.1 中可用。

`Radio`对象具有可以通过 JavaScript 访问的属性：事件属性、`checked`、`defaultChecked`和`value`。

在单选按钮出现在页面之前无法访问`Radio`对象，因此请始终在页面加载后执行的函数中，或者在 HTML 中单选按钮`<INPUT>`标签下方的`<SCRIPT>`标签中访问`Radio`对象。

`Radio`对象在 JavaScript 1.0 及更高版本中可用，某些功能在 JavaScript 1.1 中可用。

`Radio.checked` `Radio`对象的`checked`属性是一个布尔值，可以设置为`true`或`false`来选中或取消单选按钮。

你可以这样在 JavaScript 代码中访问`Radio.checked`：

```javascript
var test = document.myForm.myRadio[0].checked;

// 如果第一个按钮被选中，test 为 true，否则为 false
```

你可以更改`Radio.checked`属性来选中或取消按钮。

```javascript
document.myForm.myRadio[0].checked = true;

// 选中第一个按钮
```

此外，你可以使用单选按钮的`length`属性处理集合中的所有选框。

```javascript
for (var i = 0; i < document.myForm.myRadio.length; i++) {

  if (document.myForm.myRadio[i].checked) {

    oneChecked.checked = true;

  }

}
```

`Radio.checked`在 JavaScript 1.0 及更高版本中可用。

`Radio.defaultChecked` `Radio`对象的`defaultChecked`属性是一个只读布尔值，引用单选按钮的初始状态。单选按钮的初始状态通过在 HTML 页面的`<INPUT>`标签中设置`checked`属性来指定。如果单选按钮初始选中，`defaultChecked`等于`true`。如果单选按钮初始未选中，`default`等于`false`。

```javascript
var test = document.myForm.myRadio[0].defaultChecked;

// test 等于 false
```

`Radio.defaultChecked`在 JavaScript 1.0 及更高版本中可用。

`Radio.event` `Radio`对象的事件属性，其初始值设置为 HTML 中定义该单选按钮的`<INPUT>`标签的事件处理程序属性的相同，例如`onclick`。可以为`Radio`对象定义的事件处理器有`onblur`、`onclick`和`onfocus`。

## 文档属性 213

`Radio`对象的事件属性应该等于一个函数或`null`，或者你也可以直接设置它。如果将事件属性设置为函数，则在事件发生时将执行该函数。如果将事件属性设置为`null`或未设置，则单选按钮将按正常方式运行，在事件发生时不会执行任何特殊代码。

你可以在 JavaScript 中像这样访问事件属性：

```javascript
alert(document.myForm.myRadio[0].onclick);

// 访问 onclick 事件属性

// 弹出 onClick 函数的定义代码

// 这与 IE 和 Netscape 不同
```

你可以通过两种方式用 JavaScript 更改事件属性。你可以像这里一样给事件属性分配一个函数字面量：

```javascript
document.myForm.myRadio[0].onclick = function() {

  alert("New Function!");

} // 将函数字面量赋值给 onclick 属性
```

或者，你可以定义一个函数`functionChange()`并将其赋值给事件属性：

```javascript
function functionChange() { 

  alert("New Function!"); 

} // 定义新函数

document.myForm.myRadio[0].onclick = functionChange;

// 将函数赋值给 onclick 属性

// 注意在引用函数时

// 不要使用括号 ()
```

在不同版本的 JavaScript 中，`Radio`对象提供了不同的事件属性，如下表所示。

| Radio 对象的事件处理器 | JavaScript 版本 | Bug |
|---|---|---|
| `onblur` | JavaScript 1.0 及更高 | 在 Unix 的 Netscape 3 及更低版本中复选框无效 |
| `onclick` | JavaScript 1.0 及更高 | 在 Macintosh 的 Netscape 4 中必须返回一个值 |
| `onfocus` | JavaScript 1.0 及更高 | 在 Unix 的 Netscape 3 及更低版本中复选框无效 |

## 文档属性 214

`Radio.value` `Radio`对象的`value`属性最初被设置为与 HTML 中定义单选按钮的`<INPUT>`标签的`value`属性相同的值。这是单选按钮被选中时将提交的文本。它通常不会显示在 HTML 页面上。

```javascript
// 在 JavaScript 中可以这样访问 Radio.value：

alert(document.myForm.myRadio[0].value);

// 弹出按钮的值
```

你可以在 JavaScript 代码中将单选按钮的`value`修改为任何字符串。

```javascript
document.myForm.myRadio[0].value = "fed-ex";
```

`Radio.value`在 JavaScript 1.0 及更高版本可用。

## 重置 (Reset)

重置按钮将表单恢复到其默认值。它们通常被称为“清除”按钮。不要将其与普通按钮或提交按钮混淆，它们在各自的章节中进行了讨论。

`Reset`对象用于通过 JavaScript 访问 HTML 页面中的重置按钮元素。`Reset`对象通过在 HTML 表单中插入一个`type`属性设置为`reset`的`<INPUT>`标签来定义。

```html
<form name="reset">

  <input type="reset" name="myReset" value="Reset Form" onclick="clicked()">

</form>
```

在按钮出现在页面之前无法访问`Reset`对象，因此请务必在页面加载后执行的函数中，或者在 HTML 中重置按钮的`<INPUT>`标签下方的`<SCRIPT>`标签中访问`Reset`对象。

JavaScript 可以访问重置按钮的几个属性：
- 事件属性和`value`。

`Reset`对象在 JavaScript 1.0 及更高版本可用。

## 文档属性 215

`Reset.event` `Reset`对象的事件属性最初被设置为与 HTML 中定义该按钮的`<INPUT>`标签的事件处理器属性相同的值，例如`onclick`。可以为重置按钮定义的事件处理器有`onblur`、`onclick`、`onmouseover`和`mousedown`。

`Reset`对象的事件属性应该等于一个函数或`null`，或者你也可以不设置它。如果将事件属性设置为函数，则在事件发生时将执行该函数。如果将事件属性设置为`null`或未设置，则按钮将按正常方式运行，在事件发生时不会执行任何特殊代码。

你可以在 JavaScript 中像这样访问`Reset`对象的事件属性：

```javascript
alert(document.myForm.myReset.onclick);

// 访问 onclick 事件属性

// 弹出用户确定的 onclick 函数的定义代码

// 这在 IE 和 Netscape 之间不同
```

你可以通过两种方式用 JavaScript 更改事件属性。你可以像这里一样给事件属性分配一个函数字面量：

```javascript
document.myForm.myReset.onclick = function() {

  alert("New Function!");

}; // 将函数字面量赋值给

// onclick 属性
```

或者，你可以定义一个函数然后将其赋值给事件属性：

```javascript
function onChange() { 

  alert("New Function!");

}

// 定义新函数

document.myForm.myReset.onclick = onChange;

// 将函数赋值给 onclick 属性

// 注意在引用函数时

// 不要使用括号 ()
```

## 文档属性 216

在不同版本的 JavaScript 中，`Reset`对象提供了不同的事件属性，如下表所示。

| Reset 对象的事件处理器 | JavaScript 版本 | Bug |
|---|---|---|
| `onclick` | JavaScript 1.0 及更高 | 在 Macintosh 的 Netscape 4 中必须返回一个值才能工作 |
| `onblur` | JavaScript 1.0 及更高 | 在 Unix 的 Netscape 3 及更低版本中按钮无效 |
| `onfocus` | JavaScript 1.0 及更高 | |
| `mousedown` | JavaScript 1.2 及更高 | |
| `onmouseup` | JavaScript 1.2 及更高 | |

`Reset.value` `Reset`对象的`value`属性最初被设置为与 HTML 中定义按钮的`<INPUT>`标签的`value`属性相同的值。这是显示在页面上的文本。

你可以在 JavaScript 中像这样访问`Reset.value`：

```javascript
alert(document.myForm.myReset.value);

// 弹出值
```

你也可以在 JavaScript 代码中将`Reset`对象的`value`修改为任何字符串。这将改变页面的显示。

```javascript
document.myForm.myReset.value = "Don't Click!";
```

`Reset.value`在 JavaScript 1.0 及更高版本可用。

## 选择 (Select)

`Select`菜单是有时被称为下拉菜单的选项列表。它们允许用户从列表中选择一个选项或多个选项，取决于你在 HTML 中如何定义菜单。`Select`对象允许通过 JavaScript 访问`select`元素。

## 文档属性 217

你可以通过在 HTML 中放置`<SELECT>`标签来创建选择菜单。该标签始终应包含一个`<OPTION>`标签，并且结尾始终有一个闭合的`</SELECT>`标签。可选，`<SELECT>`标签可以包含等于菜单高度的`size`属性或`multiple`属性，后者允许用户在菜单中选择多个项目。

```html
<form name="myForm" size="3" multiple>

  <select name="mySelect" size="">

    <option value="Yahoo">Yahoo!</option>

    <option selected>Google</option>

    <option>dmoz.org</option>

  </select>

</form>
```

在选择菜单出现在页面之前就可以访问`Select`对象，因此请务必在页面加载后执行的函数中，或者在下方的`<SCRIPT>`标签中访问`Select`对象。

JavaScript 可以访问选择菜单的几个属性：
- 事件属性
- `length`
- `options`
- `selectedIndex`
- `value`。

`Select`对象在 JavaScript 1.0 及更高版本可用，某些功能在 JavaScript 1.1 及更高版本中可用。

`Select.event` `Select`的事件属性最初被设置为与 HTML 中定义选择菜单的`<INPUT>`标签的事件处理器属性相同的值，例如`onChange`。可以为密码字段定义的事件处理器有`onblur`、`onChange`和`onfocus`。

`Select`对象的事件属性应该等于一个函数或`null`，或者你也可以直接设置它。如果将事件属性设置为函数，则在事件发生时将执行该函数。如果将事件属性设置为`null`或未设置，则选择菜单将按正常方式运行，在事件发生时不会执行任何特殊代码。

## 218 文档属性

你可以通过两种方式用 JavaScript 更改事件属性。
你可以像这里一样，将函数字面量赋值给事件属性：

```javascript
document.myForm.mySelect.onchange = function() {

  alert("New Function!");

};
```

// 将函数字面量赋值给`onclick`属性

或者，你可以定义一个函数然后将其赋值给事件属性：

```javascript
function functionChange() { alert("New Function!"); } // 定义新函数

document.myForm.mySelect.onchange = functionChange;

// 将函数赋值给 onchange 属性

// 注意，在引用函数时时不使用括号 ()
```

在不同的 JavaScript 版本中，`Select`对象提供了不同的事件属性，如下表所示：

| Select 对象的事件处理程序 | JavaScript 版本 | 缺陷 |
|---|---|---|
| `onBlur()` | | 不适用于 Unix 上的 Netscape 3 及以下版本的`select`菜单。 |
| `onChange()` | JavaScript 1.0 及更高 | 在 Netscape 2 中，在菜单失去输入焦点之前，`onchange`事件不会被触发。 |
| `onFocus()` | JavaScript 1.0 及更高 | 不适用于 Unix 上的 Netscape 3 及以下版本的`select`菜单。 |

`Select.length` `Select.length`属性等于`select`菜单中选项（`option`）的数量。它是只读的。你可以这样在 JavaScript 代码中访问`Select.length`：

```javascript
alert("My menu has " + document.myForm.mySelect.length + " " options.");

//  select 菜单中选项的数量 *
```

`Select.length`在 JavaScript 1.0 及后续版本可用。

`Select.options[]` `Select.options[]`数组包含了`Option`对象的引用，这些对象代表`select`菜单的选项。它们最初是按照它们在 HTML 中出现的顺序列出的。

你可以这样在 JavaScript 代码中访问`Select.options[]`：

```javascript
alert("My menu has these options: " + document.myForm.mySelect.options[]);

// 表单中选项的列表
```

你可以使用循环来处理`select`菜单中的所有选项。

```javascript
for(var i=0; i < document.myForm.mySelect.options.length; i++) {

    document.myForm.mySelect.options[i].value = "";

}

// 清空 select 菜单中

// 每个选项的值
```

在 JavaScript 1.1 及更高版本中，`Select.options[]`也可以被修改。你可以将长度设置为较小的数字来截断菜单末尾的额外选项，如下：

```javascript
document.myForm.mySelect.options.length = 1;

// 删除 select 菜单中第一个选项以外的所有选项
```

你也可以通过向`options[]`数组添加新项在`select`菜单中创建一个选项：

```javascript
document.myForm.mySelect.options[3] = new Option("GoTo.com","goto");

// 为 select 菜单添加第四4 个选项
```

你可以通过将`Select.options[]`数组中对象的值设置为`null`来删除数组中的选项。这样做之后，`options[]`数组中其他元素的索引会自动移动以填充“空隙”。

```javascript
document.myForm.mySelect.options[3] = null;

// 从 select 菜单中删除第 4 个选项
```

`Select.options[]`在 JavaScript 1.0 及后续版本可用，并在 JavaScript 1.1 及后续版本中可读可写。

`Select.selectedIndex` `Select`对象的`selectedIndex`属性等于`select`菜单中被选中选项的索引。如果没有选中选项，该属性等于`-1`。

你可以这样在 JavaScript 代码中访问`Select.selectedIndex`：

```javascript
var i = document.myForm.mySelect.selectedIndex;

// 如果选择了第三个选项，则等于 2。
```

如果你的`<SELECT>`标签中设置了`multiple`属性，你应该使用循环而不是`selectedIndex`来确定哪些项被选中，如下：

```javascript
var selected[] = new Array();

for(var i=0; i < document.myForm.mySelect.options.length; i++) {

  if (document.myForm.mySelect.options[i].selected)

    alert(document.myForm.mySelect.options[i] + " is selected.");

}

// 当选中选项时弹出消息
```

在 JavaScript 1.1 中，你可以写入`selectedIndex`属性来选择`select`菜单中的任何选项：

```javascript
document.myForm.mySelect.selectedIndex = 0;

// 选择 select 菜单中的第一个选项
```

`Select.selectedIndex`属性在 JavaScript 1.0 中可用，并在 JavaScript 1.1 中可读可写。

`Select.type` `Select`对象的`type`属性等于两个字符串之一，告知`select`菜单是否允许多选。如果菜单允许多选，则`type`等于`"select-multiple"`。否则，`type`等于`"select-one"`。`Select.type`是只读的。

你可以这样在 JavaScript 代码中访问`Select.type`：

```javascript
alert("My menu is a " + document.myForm.mySelect.type + "menu.");

// 弹出 select 菜单的类型
```

`Select.type`在 JavaScript 1.1可用。

## Submit

提交按钮将表单数据发送到`<FORM>`标签`action`属性指定的脚本。不要将其与普通按钮或重置按钮混淆，它们在各自的章节中讨论。`Submit`对象用于通过 JavaScript 访问 HTML 页面中的提交按钮。

`Submit`对象通过在 HTML 表单中插入一个`type`属性设置为`submit`的`<INPUT>`标签来定义。

```html
<form name="myForm">

<input type="submit" name="mySubmit" value="Submit" onclick="clicked()">

</form>
```

在按钮出现在页面之前无法访问`Submit`对象，因此始终在页面加载后执行的函数中或在 HTML 中重置按钮`<INPUT>`标签下的`<SCRIPT>`标签中访问`Submit`对象。

JavaScript 可以访问提交按钮的几个属性：事件属性和值。`Submit`对象在 JavaScript 1.0 及更高版本可用。

`Submit.event` `Submit`对象的属性最初被设置为与 HTML 中定义提交按钮的`<INPUT>`标签的事件处理程序相同的值，例如`onclick`。为提交按钮对象定义的事件处理程序有`onblur`, `onclick`, `onfocus`, `mouseup`和`mousedown`。

## 文档属性

### Text.event `Text`对象的事件属性初始被设置为与 HTML 中定义文本字段的`<INPUT>`标签的事件处理程序属性相同的值，例如`onchange`。文本字段可以定义的事件处理器有`onblur`、`onchange`、`onfocus`和`onselect`。

`Text`对象的事件属性应该等于一个函数或`null`，你可以简单地不设置它。如果事件属性设置为函数，则当事件发生时将执行该函数。如果事件属性设置为`null`或未设置，则文本字段将正常运行，在事件发生时不会执行任何特殊代码。

在 JavaScript 中可以像这样访问`Text`对象的事件属性：

```javascript
alert(document.myForm.myText.onchange);

// 访问事件属性

// 弹出函数定义代码

// 针对用户定义的 onchange 函数

// 这在 IE 和 Netscape 之间不同
```

你可以通过两种方式用 JavaScript 更改事件属性。你可以将函数字面量赋值给事件属性，如下所示：

```javascript
document.myForm.myText.onchange = function() { alert("New Function!"); };

// 将函数字面量

// 赋值给 onChange 属性
```

或者你可以定义一个函数然后将其赋值给事件属性：

```javascript
function functionChange()

{ alert("New Function!"); } // 定义新函数

document.myForm.myText.onchange = functionChange

// 将函数赋值给 onChange 属性

// 注意在引用函数时

// 不使用括号 ()
```

在不同版本的 JavaScript 中，`Text`对象可用的不同的事件属性，如下表所示。

| 文本对象的事件处理器 | JavaScript 版本 | 缺陷 |
|---|---|---|
| `onblur` | JavaScript 1.0 及以上 | |
| `onchange` | JavaScript 1.0 及以上 | |
| `onfocus` | JavaScript 1.0 及以上 | |
| `onselect` | JavaScript 1.2 及以上 | |

### Text.value `Text`对象的数值（`value`）初始被设置为与 HTML 中定义文本字段的`<INPUT>`标签的`value`属性相同的值。这是显示在文本字段中的文本。

在 JavaScript 中可以像这样访问`Text.value`：

```javascript
alert(document.myForm.myText.value);

// 弹出 Text 对象的数值
```

你可以在 JavaScript 代码中将`Text`对象的数值改为任意字符串。这会改变页面上文本字段的显示。

```javascript
document.myForm.myText.value = "在此输入您的文本.";
```

`Text.value`在 JavaScript 1.0 及以上版本可用。

## Textarea

文本区域（text area）是一个单行或多行的区域，用户可以在其中输入文本。`Textarea`对象提供了对 HTML 页面中文本对象的访问。

通过在 HTML 表单中插入`<TEXTAREA>`标签来定义`Textarea`对象。你应该始终关闭此标签。

```html
<form name="myForm">

<textarea name="myTextarea" onchange="changed()">

  textarea 的值放在这里。

</textarea>

</form>
```

`Textarea`对象在 JavaScript 1.0 及后续版本可用。

### Textarea.event `Textarea`对象的属性初始被设置为与 HTML 中`<TEXTAREA>`标签的事件处理程序属性相同的值，例如`onchange`。文本区域可以定义的事件处理器有`onblur`、`onchange`、`keydown`、`keypress`、`keykeyup`和`onselect`。

`Textarea`对象的事件属性应该等于一个函数或等于`null`，你可以简单地设置一个。如果事件属性设置为函数，则当事件发生时将执行该函数。如果事件属性设置为`null`或未设置，则文本区域将正常运行，在事件发生时不会执行任何特殊代码。

在 JavaScript 中可以像这样访问`Textarea`对象的事件属性：

```javascript
alert(document.myForm.myTextarea.onchange);

// 访问 onclick 事件属性

// 弹出函数定义代码

// 针对用户指定的 onchange 函数

// 这在 IE 和 Netscape 之间不同
```

你可以通过两种方式用 JavaScript 更改事件属性。你可以将函数字面量赋值给事件属性，如下：

```javascript
document.myForm.myTextarea.onchange = function() { alert("New Function!"); };

// 将函数字面量

// 赋值给 onchange 属性
```

或者你可以定义一个函数然后将其赋值给事件属性：

```javascript
function functionChange()

{ alert("New Function!"); } // 定义新函数

document.myForm.myTextarea.onchange = functionChange

// 将函数赋值给 onChange 属性

// 注意在引用函数时

// 不使用括号 ()
```

在不同版本的 JavaScript 中，`Textarea`对象可用的不同的事件属性，如下表所示。

| Textarea 对象的事件处理器 | JavaScript 版本 | 缺陷 |
|---|---|---|
| `onblur` | JavaScript 1.0 及以上 | |
| `onchange` | JavaScript 1.0 及以上 | |
| `onfocus` | JavaScript 1.0 及以上 | |
| `keydown` | JavaScript 1.0 及以上 | |
| `keypress` | JavaScript 1.0 及以上 | |
| `keykeyup` | JavaScript 1.0 及以上 | |
| `onselect` | JavaScript 1.2 及以上 | |

### Textarea.value `Textarea`对象的数值初始被设置为与定义文本字段的`<INPUT>`标签的`value`属性相同的值。这是显示在文本字段中的文本。

在 JavaScript 中可以像这样访问`Textarea.value`：

```javascript
alert(document.myForm.myTextarea.value);

// 弹出 Text 对象的数值
```

你可以在 JavaScript 代码中将`Textarea`对象的数值改为任意字符串。这会改变页面上文本字段的显示。

```javascript
document.myForm.myTextarea.value = "在此输入您的文本.";
```

`Textarea.value`在 JavaScript 1.0 及以上版本可用。

## HTMLElement

`HTMLElement`指任何 HTML 元素，如`<A>`、`<BODY>`、`<FORM>`等。可以使用某些功能显示如`id`和`name`。

### HTMLElement.all[] `HTMLElement`的`all()`数组包含了元素内的所有对象，按它们在 HTML 中出现的顺序。通常在 JavaScript 代码中访问：

```javascript
if (document.all) alert("可以使用 IE");

else alert("无法使用 IE.");

// 测试 document.all 是否可以使用 HTML
```

你可以使用`all.length`查看对象中包含多少个对象。

```javascript
alert("我的文档包含 " + document.all.length + " 个对象");

// 文档对象的数量
```

### HTMLElement.children[] `children[]`数组包含了直接在另一个元素中的所有对象。例如，表单可能包含一个包含选项的选择菜单；但表单并没有直接包含`Option`对象，只包含`Select`对象，因此`form.children[]`只包含`Select`对象。

在 JavaScript 中可以像这样访问`children[]`数组：

```javascript
if (document.children) alert("页面不是空的");

else alert("页面是空的");

// 测试文档是否为空
```

你可以使用`children.length`查看对象中直接包含了多少个对象。

```javascript
alert("*此文档有 " + document.children.length + " 个子元素");

// 文档的子元素数量
```

### HTMLElement.className `className`属性等于 HTML 元素的`class`属性的值。你可以在 JavaScript 代码中像这样访问类：

```javascript
var bodyClass = document.body.className;

// body 类等于

// <body> 设置的类的值
```

你你也可以将类设置为任何通过样式表定义或导入的类名，如下：

```javascript
document.body.className = "redAndWhite";

// 将 <body> 类更改为

// 用户定义的 "redAndWhite" 类
```

# 文档属性 229

`HTMLElement.class`在 Internet Explorer 4 及更高版本以及 Netscape 6 中可用。

`HTMLElement.contains()` `contains`方法返回一个布尔值，表示一个对象是否包含在另一个对象内部。`HTMLElement.contains()`在 Internet Explorer 4 及更高版本中可用。例如，

```html
<html>

<body>

<form name="login">

<input name="username" type="text">

<input name="password" type="password">

<input type="submit" value="submit">

</form>

<script type="text/javascript">

var formcheck = document.body.contains(document.login);

var formlelementcheck = document.login.contains(document.login.username);

document.write(formcheck);

document.write(formlelementcheck);

</script>

</body>

</html>
```

这在在两种情况下都返回`true`，因为`<body>`包含一个名为`login`的`<FORM>`，而名为`login`的`<FORM>`包含一个名为`username`的元素。

`HTMLElement.document` `document`属性包含文档中的元素列表。`HTMLElement.document`在 Internet Explorer 4 及更高版本中可用。例如，

```html
<html>

<body>

<form name="login">

<input name="username" type="text">

<input name="password" type="password">

<input type="submit" value="submit">

</form>

<script type="text/javascript">

var formcheck = document.login;

if (formcheck) {

document.write("form exists");

}

// 这返回：form exists

</script>

</body>

</html>
```

# HTMLElement.getAttribute() `getAttribute`方法返回请求的元素的属性。它在 IE 4+ 和 Netscape 6 中可用。

```html
<html>

<body>

<form name="login" type="text">

<input name="username" type="text">

<input name="password" type="password">

<input type="submit" value="submit">

</form>

<script type="text/javascript">

var attribute = document.login.password.getAttribute("type");

document.write(attribute);

</script>

</body>

</html>
```

这返回`password`，这是`password`输入元素的`type`属性。

# HTMLElement.id `id`属性返回`id`属性（如果它已设置）。它在 IE 4+ 和 Netscape 6 中可用。

```html
<html>

<body>

<form name="login" type="text" id="form1">

<input name="username" type="text">

<input name="password" type="password">

<input type="submit" value="submit">

</form>

<script type="text/javascript">

var idname = document.login.id;

document.write(idname);

</script>

</body>

</html>
```

如你所见，这将返回`form1`，它是`login`表单的`id`。

`HTMLElement.innerHTML` `innerHTML`非常有用，它返回所选元素中的 HTML。它在 IE 4 和 Netscape 6+ 中可用。

```html
<html>

<body>

<form name="login" type="text">

  <input name="username" type="text">

  <input name="password" type="password">

  <input type="submit" value="submit">

</form>

<script type="text/javascript">

  var htmltest = document.login.innerHTML;

  document.write(htmltest);

</script>

</body>

</html>
```

这返回打印两次的上方表单。

`HTMLElement.innerText` `innerText`属性返回在请求元素内显示的字符串。它在 IE 4+ 中可用。

```html
<html>

<body>

<p id="text">here is some text</p>

<script type="text/javascript">

  var htmltest = window.text.innerText;

  document.write(htmltest);

</script>

</body>

</html>
```

这返回两次字符串`"here is some text"`。

`HTMLElement.insertAdjacentHTML()` `insertAdjacentHTML()`方法在请求的元素旁相邻插入 HTML。它仅在 IE 4 中可用。语法如下：

```
HTMLElement.insertAdjacentHTML("location", "html");
```

参数`html`指向你想要输入的 HTML。参数`location`指向`html`参数的位置。可能的位置如下：

| 节点 | 描述 |
| --- | --- |
| `BeforeBegin` | 在元素开始之前插入 HTML |
| `AfterBegin` | 在元素开始之后插入 HTML |
| `BeforeEnd` | 在元素结束之前插入 HTML |
| `AfterEnd` | 在元素结束之后插入 HTML |

`HTMLElement.insertAdjacentText()` `insertAdjacentText`方法在请求的元素旁相邻插入文本。它仅在 IE 4 中可用。语法如下：

```
HTMLElement.insertAdjacentHTML("location", "html");
```

参数指向你想要插入 HTML。参数`location`指向`html`参数的位置。可能的位置如下：

| 节点 | 描述 |
| --- | --- |
| `BeforeBegin` | 在元素开始之前插入文本 |
| `AfterBegin` | 在元素开始之后插入文本 |
| `BeforeEnd` | 在元素结束之前插入文本 |
| `AfterEnd` | 在元素结束之后插入文本 |

`HTMLElement.lang` `lang`属性指定元素的`lang`。它在 IE 4+ 中可用。

```html
<html>

<body>

<p id="text">here is some text</p>

<script type="text/javascript">

  var language = window.text.innerText;

  document.write(language);

</script>

</body>

</html>
```

这返回两次字符串`"here is some text"`。

# 文档属性 233

`HTMLElement.offsetHeight` `offsetWidth`

`offsetHeight`和`offsetWidth`属性返回指定元素的的高度和宽度（单位为像素）。它们在 IE 4+ 中可用。

```html
<html>

<body>

  <p id="text">here is some text</p>

  <script type="text/javascript">

    var height = window.text.offsetHeight;

    var width = window.text.offsetWidth;

    document.write("Height: "+height+"<br>Width: "+width);

  </script>

</body>

</html>
```

这返回高度和宽度。

`HTMLElement.offsetLeft` `offsetTop`

`offsetLeft`和`offsetTop`属性返回请求元素的 x 和 y坐标。它们在 IE 4+ 中可用。

```html
<html>

<body>

  <p id="text">here is some text</p>

  <script type="text/javascript">

    var Left = window.text.offsetLeft;

    var Top = window.text.offsetTop;

    document.write("Left: "+Left+"<br>Top: "+Top);

  </script>

</body>

</html>
```

这返回 x 和 y 坐标。

# HTMLElement.offsetParent `offsetParent`属性控制请求元素的父元素。它在 IE 4+ 中可用。

```html
<script lang="javascript">

  function displayparent() {

    var tabled = document.all.thistd;

    alert("offsetParent: " + tabled.tagName);

  }

</script>
```

# 文档属性 234

```html
</script>

<body onload="javascript:displayparent();">

<table border="1">

  <tr><td id="thistd">This is a small table</td></tr>

</table>

</body>

</html>
```

这显示一个警框，报告`offsetParent`为`TABLE`，它是`thistd`单元格的父元素。

`HTMLElement.outerHTML` `outerHTML`属性用于替换元素内的 HTML。它在 IE 4+ 中可用。

`HTMLElement.outerText` `outerText`属性用于替换元素内的文本。它在 IE 4 中可用。

`HTMLElement.parentElement` `parentElement`属性指定包含请求元素的元素。它在 IE 4 中可用。

`HTMLElement.removeAttribute()` `removeAttribute`方法用于从指定元素移除特定属性。它在 Netscape 6+ 和 IE 4+ 中可用。语法如下：

```
HTMLElement.removeAttribute(attribute);
```

指定的属性是你想要移除的属性。如果移除成功，该方法返回`true`，否则返回`false`。

`HTMLElement.scrollToView()` `scrollToView()`方法用于滚动到页面上的某个特定元素。它在 IE 4+ 中可用。语法如下：

```
HTMLElement.scrollToView(location);
```

`location`参数是可选的。你可以指定`top`或`bottom`，将浏览器滚动到页面的顶部或底部。

`HTMLElement.setAttribute()` `setAttribute`方法用于为请求的元素设置新属性。该方法在 IE 4+ 和 Netscape 6 中可用。

`name`参数指的是你正在设置的新属性的名称。`value`参数指的是新属性的值。这里有一个使用`id`为`doctile`的虚拟`<P>`标签的示例：

```
document.doctile.setAttribute("align", "center");
```



# JavaScript 核心要素与规范手册

## 文档对象模型 (DOM) 属性与方法

### HTMLElement 属性

- `HTMLElement.sourceIndex`：`sourceIndex` 属性决定指定元素在 `all[]` 数组中的索引。适用于 IE 4+。
- `HTMLElement.style`：`style` 属性允许你添加或更改指定元素的样式。适用于 IE 4+ 和 Netscape 6+。
- `HTMLElement.tagName`：`tagName` 属性决定指定元素的 HTML 标签名称。适用于 IE 4+ 和 Netscape 6+。
- `HTMLElement.title`：`title` 属性允许你为指定元素添加工具提示。适用于 IE 4+ 和 Netscape 6+。

### Document 对象属性

#### `document.forms[]`
`forms[]` 数组包含了文档中每个表单的 `Form` 对象。也可使用 `document.forms.length` 属性。

#### `document.frames[]`
`frames[]` 数组包含了文档中每个 `<FRAME>`（浮动框架）的索引。可通过名称或元素编号调用 `iframe`。也可配合 `document.frames.length` 属性使用。

#### `document.getSelection`
`getSelection` 方法返回当前在文档中选中的文本。文本将从其 HTML 标签中移除。

#### `document.height`
`height` 属性包含当前文档的高度（像素为单位）。

#### `document.images[]`
`images[]` 数组包含了文档中的每个 `Image` 对象。可通过名称或数组中的数字调用图像。也可使用 `document.images.length` 属性。

#### `document.lastModified`
`lastModified` 属性包含文档最后修改的日期和时间。

#### `document.links[]`
`links[]` 属性包含了文档中每个链接的数组。可通过名称或元素编号调用链接。也可使用 `document.links.length` 属性。

#### `document.mimeType`
`mimeType` 属性包含当前文档的 MIME 类型。

#### `document.open()`
`open()` 方法打开一个文档流，以便后续的 `document.write()` 调用可以向文档追加数据。也可指定 `mimetetype`。在使用 `open()` 和 `write()` 方法之后，应使用 `close()` 方法。

#### `document.parentWindow`
`parentWindow` 属性返回被引用文档的父窗口的引用。

#### `document.queryCommandEnabled()`
`queryCommandEnabled` 方法允许你判断特定命令（由其标识符定义）对于引用对象是否可用。

#### `document.queryCommandIndeterm()`
`queryCommandIndeterm()` 方法用于确定特定命令是否处于不确定状态。接受一个参数：包含所查询命令标识符的字符串值。

#### `document.queryCommandState()`
`queryCommandState()` 方法用于确定通过 `execCommand` 方法发布的任何命令的状态。如果命令在引用对象上成功执行，则返回 `true`；如果命令失败，则返回 `false`。

#### `document.queryCommandSupported()`
`queryCommandSupported()` 方法用于确定命令当前是开启还是关闭状态。接受一个字符串值参数，定义要查询的命令标识符，如果命令对引用对象是开启的，则返回 `true`，否则返回 `false`。

#### `document.queryCommandText()`
`queryCommandText()` 方法用于确定与命令关联的字符串。接受命令标识符的标准字符串参数，以及一个可以是 `Name` 或 `StatusText` 的字符串值。

#### `document.queryCommandValue()`
`queryCommandValue()` 方法用于确定 `execCommand` 方法中使用的 `value` 参数。

#### `document.readyState`
`readyState` 属性包含文档的加载状态。返回四个值之一：

| readyState 值 | 描述 |
| :--- | :--- |
| uninitialized | 文档尚未开始加载。 |
| loading | 文档正在加载。 |
| interactive | 文档已加载足够，用户可以与其交互。 |
| complete | 文档已完全加载。 |

#### `document.referrer`
`referrer` 属性包含用户最后点击的 URL（如果有的话）。

#### `document.scripts[]`
`scripts[]` 属性包含了文档中每个脚本的数组。也可使用 `document.scripts.length` 属性。

#### `document.selection`
`selection` 属性包含了用户可能选择的任何当前文档内容的引用。

#### `document.styleSheets[]`
`styleSheets[]` 属性包含了附加到当前文档的任何样式表的引用。可通过名称或元素编号调用样式。也可使用 `document.styleSheets.length` 属性。

#### `document.title`
`title` 属性包含当前文档的标题。

#### `document.URL`
`URL` 属性包含当前文档的 URL。

#### `document.width`
`width` 属性包含当前文档的宽度（像素为单位）。

#### `document.write()`
`write()` 方法将文本插入文档中。

#### `document.writeln()`
`writeln()` 方法将文本插入文档中，并跟一个换行符。

#### `document.close()`
`close()` 方法关闭文档流。

#### `document.clear()`
`clear()` 方法清除文档内容。

## 附录：浏览器兼容性表

下表列出了截至编写时常用浏览器的兼容性。

| 浏览器 | 平台 | 版本 | JavaScript 支持 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| Internet Explorer | Windows | 2.0 | 1.0 | None |
| Internet Explorer | Windows | 3.0 | 1.1 | None |
| Internet Explorer | Windows | 4.0 | 1.2 | ECMA-262-compliant |
| Internet Explorer | Windows | 5.0 | 1.3 | Full |
| Internet Explorer | Macintosh | 4.0 | 1.2 | ECMA-262-compliant |
| Internet Explorer | Macintosh | 5.0 | 1.3 | Full |
| Netscape Navigator | Windows | 2.0 | 1.0 | None |
| Netscape Navigator | Windows | 3.0 | 1.1 | None |
| Netscape Navigator | Windows | 4.0 | 1.2 | ECMA-262-compliant |
| Netscape Navigator | Windows | 4.7/4.5 | 1.3 | Full |
| Netscape Navigator | Windows | 6 | 1.5 | Full |
| Netscape Navigator | Macintosh | 4.0 | 1.2 | ECMA-262-compliant |
| Netscape Navigator | Macintosh | 5.0 | 1.3 | Full |
| America Online Browser | Windows | 3.0 | 1.0 | None | 早期 3.x 版本不支持 JavaScript。 |
| America Online Browser | Windows | 4.0 | 1.2 | ECMA-262-compliant | 弹出窗口已禁用 |
| America Online Browser | Windows | 5.0 | 1.3 | Full | |
| America Online Browser | Macintosh | 4.0 | 1.2 | ECMA-262-compliant | |
| America Online Browser | Macintosh | 5.0 | 1.3 | Full | |
| Mosaic | Windows | 3.0 | None | None | |
| Mosaic | Macintosh | 3.07 | None | None | |
| Opera | Windows | 4.02 | 1.3 | Full | |
| OS/2 | 2.02 | None | None | |
| Unix & Linux | 2.0 | 1.0 | None | |
| Unix & Linux | 3.0 | 1.1 | None | |
| Unix & Linux | 4.06 | 1.1 | None | |

## 字符编码表

### ASCII 控制字符表

| 十进制 | 八进制 | 十六进制 | 控制 | 字符 | 描述 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 00 | ^@ | NUL | 空字符 |
| 1 | 1 | 01 | ^A | SOH | 标题开始 |
| 2 | 2 | 02 | ^B | STX | 文本开始 |
| 3 | 3 | 03 | ^C | ETX | 文本结束 |
| 4 | 4 | 04 | ^D | EOT | 传输结束 |
| 5 | 5 | 05 | ^E | ENQ | 询问 |
| 6 | 6 | 06 | ^F | ACK | 确认 |
| 7 | 7 | 07 | ^G | BEL | 铃声 |
| 8 | 10 | 08 | ^H | BS | 退格 |
| 9 | 11 | 09 | ^I | HT | 水平制表 |
| 10 | 12 | 0A | ^J | LF | 换行 |
| 11 | 13 | 0B | ^K | VT | 垂直制表 |
| 12 | 14 | 0C | ^L | FF | 分页符 |
| 13 | 15 | 0D | ^M | CR | 回车 |
| 14 | 16 | 0E | ^N | SO | 移出 |
| 15 | 17 | 0F | ^O | SI | 移入 |
| 16 | 20 | 10 | ^P | DLE | 数据链路转逸 |
| 17 | 21 | 11 | ^Q | DC1 | 设备控制 1 |
| 18 | 22 | 12 | ^R | DC2 | 设备控制 2 |
| 19 | 23 | 13 | ^S | DC3 | 设备控制 3 |
| 20 | 24 | 14 | ^T | DC4 | 设备控制 4 |
| 21 | 25 | 15 | ^U | NAK | 否定确认 |
| 22 | 26 | 16 | ^V | SYM | 同步空闲 |
| 23 | 27 | 17 | ^W | ETB | 传输块结束 |
| 24 | 30 | 18 | ^X | CAN | 取消 |
| 25 | 31 | 19 | ^Y | EM | 媒体结束 |
| 26 | 32 | 1A | ^Z | SUB | 替换 |
| 27 | 33 | 1B | ^[ | ESC | 逸出 |
| 28 | 34 | 1C | ^\ | FS | 文件分隔符 |
| 29 | 35 | 1D | ^] | GS | 组分隔符 |
| 30 | 36 | 1E | ^^ | RS | 记录分隔符 |
| 31 | 37 | 1F | _ | US | 单位分隔符 |
| 32 | 40 | 20 | | SP | 空格 |
| 127 | 177 | 7F | ^? | DEL | 删除 |

### 基础 ASCII 字符表 (32-64)

| 十进制 | 八进制 | 十六进制 | HTML | 字符 |
| :--- | :--- | :--- | :--- | :--- |
| 32 | 40 | 20 | | 空格 |
| 33 | 41 | 21 | | ! |
| 34 | 42 | 22 | `&quot;` | " |
| 35 | 43 | 23 | | # |
| 36 | 44 | 24 | | $ |
| 37 | 45 | 25 | | % |
| 38 | 46 | 26 | `&amp;` | & |
| 39 | 47 | 27 | | ' |
| 40 | 50 | 28 | | ( |
| 41 | 51 | 29 | | ) |
| 42 | 52 | 2A | | * |
| 43 | 53 | 2B | | + |
| 44 | 54 | 2C | | , |
| 45 | 55 | 2D | | - |
| 46 | 56 | 2E | | . |
| 47 | 57 | 2F | | / |
| 48 | 60 | 30 | | 0 |
| 49 | 61 | 31 | | 1 |
| 50 | 62 | 32 | | 2 |
| 51 | 63 | 33 | | 3 |
| 52 | 64 | 34 | | 4 |
| 53 | 65 | 35 | | 5 |
| 54 | 66 | 36 | | 6 |
| 55 | 67 | 37 | | 7 |
| 56 | 70 | 38 | | 8 |
| 57 | 71 | 39 | | 9 |
| 58 | 72 | 3A | | : |
| 59 | 73 | 3B | | ; |
| 60 | 74 | 3C | `&lt;` | < |
| 61 | 75 | 3D | | = |
| 62 | 76 | 3E | `&gt;` | > |
| 63 | 77 | 3F | | ? |
| 64 | 100 | 40 | | @ |

### 字符表 245 (65-105)

| 十进制 | 八进制 | 十六进制 | HTML | 字符 |
| :--- | :--- | :--- | :--- | :--- |
| 65 | 101 | 41 | | A |
| 66 | 102 | 42 | | B |
| 67 | 103 | 43 | | C |
| 68 | 104 | 44 | | D |
| 69 | 105 | 45 | | E |
| 70 | 106 | 46 | | F |
| 71 | 107 | 47 | | G |
| 72 | 110 | 48 | | H |
| 73 | 111 | 49 | | I |
| 74 | 112 | 4A | | J |
| 75 | 113 | 4B | | K |
| 76 | 114 | 4C | | L |
| 77 | 115 | 4D | | M |
| 78 | 116 | 4E | | N |
| 79 | 117 | 4F | | O |
| 80 | 120 | 50 | | P |
| 81 | 121 | 51 | | Q |
| 82 | 122 | 52 | | R |
| 83 | 123 | 53 | | S |
| 84 | 124 | 54 | | T |
| 85 | 125 | 55 | | U |
| 86 | 126 | 56 | | V |
| 87 | 127 | 57 | | W |
| 88 | 130 | 58 | | X |
| 89 | 131 | 59 | | Y |
| 90 | 132 | 5A | | Z |
| 91 | 133 | 5B | | [ |
| 92 | 134 | 5C | | \ |
| 93 | 135 | 5D | | ] |
| 94 | 136 | 5E | `&circ;` | ^ |
| 95 | 137 | 5F | | _ |
| 96 | 140 | 60 | | ` |
| 97 | 141 | 61 | | a |
| 98 | 142 | 62 | | b |
| 99 | 143 | 63 | | c |
| 100 | 144 | 64 | | d |
| 101 | 145 | 65 | | e |
| 102 | 146 | 66 | | f |
| 103 | 147 | 67 | | g |
| 104 | 150 | 68 | | h |
| 105 | 151 | 69 | | i |

### 字符表 246 (106-127)

| 十进制 | 八进制 | 十六进制 | HTML | 字符 |
| :--- | :--- | :--- | :--- | :--- |
| 106 | 152 | 6A | | j |
| 107 | 153 | 6B | | k |
| 108 | 154 | 6C | | l |
| 109 | 155 | 6D | | m |
| 110 | 156 | 6E | | n |
| 111 | 157 | 6F | | o |
| 112 | 160 | 70 | | p |
| 113 | 161 | 71 | | q |
| 114 | 162 | 72 | | r |
| 115 | 163 | 73 | | s |
| 116 | 164 | 74 | | t |
| 117 | 165 | 75 | | u |
| 118 | 166 | 76 | | v |
| 119 | 167 | 77 | | w |
| 120 | 170 | 78 | | x |
| 121 | 171 | 79 | | y |
| 122 | 172 | 7A | | z |
| 123 | 173 | 7B | | { |
| 124 | 174 | 7C | | \| |
| 125 | 175 | 7D | | } |
| 126 | 176 | 7E | `&tilde;` | ~ |
| 127 | 177 | 7F | `&#127;` | DEL |

### 扩展 ASCII 表 (128-159)

| 十进制 | 八进制 | 十六进制 | HTML | 字符 | 描述 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 128 | 200 | 80 | `&#128;` | € | 欧元符号 |
| 129 | 201 | 81 | [reserved] | [reserved] | [保留] |
| 130 | 202 | 82 | `&#130;` | ‚ | 左下单引号 |
| 131 | 203 | 83 | `&ord;` | ƒ | 小斜体 f |
| 132 | 204 | 84 | `&#132;` | „ | 左下双引号 |
| 133 | 205 | 85 | `&#133;` | … | 左下水平省略号 |
| 134 | 206 | 86 | `&dagger;` | † | 剑号 |
| 135 | 207 | 87 | `&dagger;` | ‡ | 双剑号 |
| 136 | 210 | 88 | `&#136;` | ˆ | 修改抑音符号的字母 |
| 137 | 211 | 89 | `&per;` | ‰ | 千分号 |
| 138 | 212 | 8A | `&Caron;` | Š | S 变音 |
| 139 | 213 | 8B | `&laquo;` | ‹ | 左单引号 |
| 140 | 214 | 8C | `&OE;` | Œ | OE 连字 |
| 141 | 215 | 8D | [reserved] | [reserved] | [保留] |
| 142 | 216 | 8E | [reserved] | [reserved] | [保留] |
| 143 | 217 | 8F | [reserved] | [reserved] | [保留] |
| 144 | 220 | 90 | [reserved] | [reserved] | [保留] |
| 145 | 221 | 91 | | ‘ | 左单引号 |
| 146 | 222 | 92 | | ’ | 右单引号 |
| 147 | 223 | 93 | `&ldquo;` | “ | 左双引号 |
| 148 | 224 | 94 | `&rdquo;` | ” | 右双引号 |
| 149 | 225 | 95 | `&bull;` | • | 实心点 |
| 150 | 226 | 96 | `&ndash;` | – | 破折号 |
| 151 | 227 | 97 | `&mdash;` | — | 破折号 |
| 152 | 230 | 98 | `&#152;` | ˜ | 上波浪 |
| 153 | 231 | 99 | `&trade;` | ™ | 商标 |
| 154 | 232 | 9A | | š | 符号 |
| 155 | 233 | 9B | | › | 上变音 |
| 156 | 234 | 9C | `&ers;` | œ | 连字 |
| 157 | 235 | 9D | [reserved] | [reserved] | [保留] |
| 158 | 236 | 9E | [reserved] | [reserved] | [保留] |
| 159 | 237 | 9F | [reserved] | [reserved] | [保留] |

### 扩展 ASCII 表 (160-191)

| 十进制 | 八进制 | 十六进制 | HTML | 字符 | 描述 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 160 | 240 | A0 | `&nbsp;` |  | 不换行空格 |
| 161 | 241 | A1 | `&iexcl;` | ¡ | 倒叹号 |
| 162 | 242 | A2 | `&cent;` | ¢ | 分角符号 |
| 163 | 243 | A3 | `&pound;` | £ | 英镑符号 |
| 164 | 244 | A4 | `&currency;` | ¤ | 通用货币 |
| 165 | 245 | A5 | `&en;` | ¥ | 日元符号 |
| 166 | 246 | A6 | `&brvar;` | ¦ | 断节 |
| 167 | 247 | A7 | `&sect;` | § | 段落 |
| 168 | 250 | A8 | `&uml;` | ¨ | 双音符号 |
| 169 | 251 | A9 | `&copy;` | © | 版权符号 |
| 170 | 252 | AA | `&ord;` | ª | 女性序数指示 |
| 171 | 253 | AB | `&laquo;` | « | 左双角引号 |
| 172 | 254 | AC | `&not;` | ¬ | 逻辑非符号 |
| 173 | 255 | AD | `&shy;` |  | 软连字符 |
| 174 | 256 | AE | `&reg;` | ® | 注册商标 |
| 175 | 257 | AF | `&mac;` | ¯ | 长变音 |
| 176 | 260 | B0 | `&deg;` | ° | 度符号 |
| 177 | 261 | B1 | `&plusmn;` | ± | 加减号 |
| 178 | 262 | B2 | `&sup2;` | ² | 上标 2 |
| 179 | 263 | B3 | `&sup3;` | ³ | 上标 3 |
| 180 | 264 | B4 | `&acute;` | ´ | 急音符号 |
| 181 | 265 | B5 | `&micro;` | µ | 微符号 |
| 182 | 266 | B6 | `&para;` | ¶ | 段落符号 |
| 183 | 267 | B7 | `&middot;` | · | 中点 |
| 184 | 270 | B8 | `&cedill;` | ¸ | 变音符号 |
| 185 | 271 | B9 | `&sup1;` | ¹ | 上标 1 |
| 186 | 272 | BA | `&ordm;` | º | 男性序数指示 |
| 187 | 273 | BB | `&rsquo;` | » | 右双角引号 |
| 188 | 274 | BC | `&frac14;` | ¼ | 四分之一 |
| 189 | 275 | BD | `&frac12;` | ½ | 二分之一 |
| 190 | 276 | BE | `&frac34;` | ¾ | 四分之三 |
| 191 | 277 | BF | `&iquest;` | ¿ | 倒问号 |

### 扩展 ASCII 表 (192-255)

| 十进制 | 八进制 | 十六进制 | HTML | 字符 | 描述 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 192 | 300 | C0 | `&Agrave;` | À | 大写 A 重音符号 |
| 193 | 301 | C1 | `&Aacute;` | Á | 大写 A 急音符号 |
| 194 | 302 | C2 | `&Acirc;` | Â | 大写 A 带有圈符 |
| 195 | 303 | C3 | `&Atilde;` | Ã | 大写 A 带有波浪号 |
| 196 | 304 | C4 | `&Auml;` | Ä | 大写 A 带有变音符号 |
| 197 | 305 | C5 | `&Aring;` | Å | 大写 A 带有环 |
| 198 | 306 | C6 | `&AElig;` | Æ | 大写 AE 合字 |
| 199 | 307 | C7 | `&Ccedil;` | Ç | 大写 C 下标 |
| 200 | 310 | C8 | `&Egrave;` | È | 大写 E 重音符号 |
| 201 | 311 | C9 | `&Eacute;` | É | 大写 E 急音符号 |
| 202 | 312 | CA | `&Ecirc;` | Ê | 大写 E 带有圈符 |
| 203 | 313 | CB | `&Euml;` | Ë | 大写 E 带有变音符号 |
| 204 | 314 | CC | `&Igrave;` | Ì | 大写 I 重音符号 |
| 205 | 315 | CD | `&Iacute;` | Í | 大写 I 急音符号 |
| 206 | 316 | CE | `&Icirc;` | Î | 大写 I 带有圈符 |
| 207 | 317 | CF | `&Iuml;` | Ï | 大写 I 带有变音符号 |
| 208 | 320 | D0 | `&ETH;` | Ð | 大写 ETH |
| 209 | 321 | D1 | `&Ntilde;` | Ñ | 大写 N 带有波浪号 |
| 210 | 322 | D2 | `&Ograve;` | Ò | 大写 O 重音符号 |
| 211 | 323 | D3 | `&Oacute;` | Ó | 大写 O 急音符号 |
| 212 | 324 | D4 | `&Ocirc;` | Ô | 大写 O 带有圈符 |
| 213 | 325 | D5 | `&Otilde;` | Õ | 大写 O 带有波浪号 |
| 214 | 326 | D6 | `&Ouml;` | Ö | 大写 O 带有变音符号 |
| 215 | 327 | D7 | `&times;` | × | 乘法符号 |
| 216 | 330 | D8 | `&Oslash;` | Ø | 大写 O 划杠 |
| 217 | 331 | D9 | `&Ugrave;` | Ù | 大写 U 重音符号 |
| 218 | 332 | DA | `&Uacute;` | Ú | 大写 U 急音符号 |
| 219 | 333 | DB | `&Ucirc;` | Û | 大写 U 带有圈符 |
| 220 | 334 | DC | `&Uuml;` | Ü | 大写 U 带有变音符号 |
| 221 | 335 | DD | `&Yacute;` | Ý | 大写 Y 急音符号 |
| 222 | 336 | DE | `&THORN;` | Þ | 大写 THORN |
| 223 | 337 | DF | `&szlig;` | ß | 小写锐 s，sz 合字 |
| 224 | 340 | E0 | `&agrave;` | à | 小写 a 重音符号 |
| 225 | 341 | E1 | `&aacute;` | á | 小写 a 急音符号 |
| 226 | 342 | E2 | `&acirc;` | â | 小写 a 带有圈符 |
| 227 | 343 | E3 | `&atilde;` | ã | 小写 a 带有波浪号 |
| 228 | 344 | E4 | `&auml;` | ä | 小写 a 带有变音符号 |
| 229 | 345 | E5 | `&aring;` | å | 小写 a 带有环 |
| 230 | 346 | E6 | `&aelig;` | æ | 小写 ae 合字 |
| 231 | 347 | E7 | `&ccedil;` | ç | 小写 c 下标 |
| 232 | 350 | E8 | `&egrave;` | è | 小写 e 重音符号 |
| 233 | 351 | E9 | `&eacute;` | é | 小写 e 急音符号 |
| 234 | 352 | EA | `&ecirc;` | ê | 小写 e 带有圈符 |
| 235 | 353 | EB | `&euml;` | ë | 小写 e 带有变音符号 |
| 236 | 354 | EC | `&igrave;` | ì | 小写 i 重音符号 |
| 237 | 355 | ED | `&iacute;` | í | 小写 i 急音符号 |
| 238 | 356 | EE | `&icirc;` | î | 小写 i 带有圈符 |
| 239 | 357 | EF | `&iuml;` | ï | 小写 i 带有变音符号 |
| 240 | 360 | F0 | `&eth;` | ð | 小写 eth |
| 241 | 361 | F1 | `&ntilde;` | ñ | 小写 n 带有波浪号 |
| 242 | 362 | F2 | `&ograve;` | ò | 小写 o 重音符号 |
| 243 | 363 | F3 | `&oacute;` | ó | 小写 o 急音符号 |
| 244 | 364 | F4 | `&ocirc;` | ô | 小写 o 带有圈符 |
| 245 | 365 | F5 | `&otilde;` | õ | 小写 o 带有波浪号 |
| 246 | 366 | F6 | `&ouml;` | ö | 小写 o 带有变音符号 |
| 247 | 367 | F7 | `&divide;` | ÷ | 除法符号 |
| 248 | 370 | F8 | `&oslash;` | ø | 小写 o 划杠 |
| 249 | 371 | F9 | `&ugrave;` | ù | 小写 u 重音符号 |
| 250 | 372 | FA | `&uacute;` | ú | 小写 u 急音符号 |
| 251 | 373 | FB | `&ucirc;` | û | 小写 u 带有圈符 |
| 252 | 374 | FC | `&uuml;` | ü | 小写 u 带有变音符号 |
| 253 | 375 | FD | `&yacute;` | ý | 小写 y 急音符号 |
| 254 | 376 | FE | `&thorn;` | þ | 小写 thorn |
| 255 | 377 | FF | `&yuml;` | ÿ | 小写 y 带有变音符号 |

> **注**：除上述字符外，还有 Unicode 字符，包括希腊语、希伯来语、阿拉伯语、中文、盲文等字符集。内容过多，本书无法涵盖；请参考官方 Unicode 字符表，您可以通过 PDF 格式从 `http://www.unicode.org/charts/` 获取。

## Web 浏览器资源

以下是几个网络浏览器的 URL：

- **Netscape Navigator**：`http://home.netscape.com/download/index.html`；平台：Windows、Macintosh、Linux
- **Internet Explorer**：`http://www.microsoft.com/ie/`；平台：Windows
- **Internet Explorer (Unix)**：`http://www.microsoft.com/unix/default.asp`；平台：Unix (Solaris、HP-UX)
- **Mozilla**：`http://www.mozilla.org`；平台：Windows、Macintosh、Linux
- **Opera**：`http://www.opera.com`；平台：Windows
- **Lynx** (纯文本浏览器)：`http://lynx.browser.org/`；平台：Unix、Linux、Windows、VMS、DOS、OS/2
- **iCab**：`http://www.icab.de/`；平台：Macintosh
- **Konqueror**：`http://www.konqueror.org/`；平台：Linux
- **NCSA Mosaic**：`http://archive.ncsa.uiuc.edu/SDG/Software/Mosaic/`；平台：Linux、Unix
- **NCSA Mosaic (Windows)**：`http://archive.ncsa.uiuc.edu/SDG/Software/mosaic-w/releaseinfo/`；平台：Windows

## 国家代码表

| 国家代码 | 国家 | 国家代码 | 国家 |
| :--- | :--- | :--- | :--- |
| af | 南非荷兰语 | ar | 阿拉伯语 |
| ar-ae | 阿拉伯语 (阿联酋) | ar-bh | 阿拉伯语 (巴林) |
| ar-dz | 阿拉伯语 (阿尔及利亚) | ar-eg | 阿拉伯语 (埃及) |
| ar-iq | 阿拉伯语 (伊拉克) | ar-jo | 阿拉伯语 (约旦) |
| ar-kw | 阿拉伯语 (科威特) | ar-lb | 阿拉伯语 (黎巴嫩) |
| ar-ly | 阿拉伯语 (利比亚) | ar-ma | 阿拉伯语 (摩洛哥) |
| ar-om | 阿拉伯语 (阿曼) | ar-qa | 阿拉伯语 (卡塔尔) |
| ar-sa | 阿拉伯语 (沙特阿拉伯) | ar-sy | 阿拉伯语 (叙利亚) |
| ar-tn | 阿拉伯语 (突尼斯) | ar-ye | 阿拉伯语 (也门) |
| be | 白俄罗斯语 | bg | 保加利亚语 |
| ca | 加泰罗尼亚语 | cs | 捷克语 |
| da | 丹麦语 | de | 德语 (德国) |
| de-at | 德语 (奥地利) | de-ch | 德语 (瑞士) |
| de-li | 德语 (列支敦士登) | de-lu | 德语 (卢森堡) |
| el | 希腊语 | en | 英语 |
| en-au | 英语 (澳大利亚) | en-bz | 英语 (伯利兹) |
| en-ca | 英语 (加拿大) | en-gb | 英语 (英国) |
| en-ie | 英语 (爱尔兰) | en-jm | 英语 (牙买加) |
| en-nz | 英语 (新西兰) | en-tt | 英语 (特立尼达和多巴哥) |
| en-us | 英语 (美国) | en-za | 英语 (南非) |
| es | 西班牙语 (传统排序) | es | 西班牙语 (国际排序) |
| es-ar | 西班牙语 (阿根廷) | es-bo | 西班牙语 (玻利维亚) |
| es-cl | 西班牙语 (智利) | es-co | 西班牙语 (哥伦比亚) |
| es-cr | 西班牙语 (哥斯达黎加) | es-do | 西班牙语 (多米尼加共和国) |
| es-ec | 西班牙语 (厄瓜多尔) | es-gt | 西班牙语 (危地马拉) |
| es-hn | 西班牙语 (洪都拉斯) | es-mx | 西班牙语 (墨西哥) |
| es-ni | 西班牙语 (尼加拉瓜) | es-pa | 西班牙语 (巴拿马) |
| es-pe | 西班牙语 (秘鲁) | es-pr | 西班牙语 (波多黎各) |
| es-py | 西班牙语 (巴拉圭) | es-sv | 西班牙语 (萨尔瓦多) |
| es-uy | 西班牙语 (乌拉圭) | es-ve | 西班牙语 (委内瑞拉) |
| et | 爱沙尼亚语 | eu | 巴斯克语 |
| fa | 波斯语 | fi | 芬兰语 |
| fo | 法罗语 | fr | 法语 (法国) |
| fr-be | 法语 (比利时) | fr-ca | 法语 (加拿大) |
| fr-ch | 法语 (瑞士) | fr-lu | 法语 (卢森堡) |
| gd | 盖尔语 | he | 希伯来语 |
| hi | 印地语 | hr | 克罗地亚语 |
| hu | 匈牙利语 | in | 印尼语 |
| is | 冰岛语 | it | 意大利语 (意大利) |
| it-ch | 意大利语 (瑞士) | ja | 日语 |
| ji | 犹太语 | ko | 韩语 |
| lt | 立陶宛语 | lv | 拉脱维亚语 |
| mk | 马其顿语 (FYOM) | ms | 马来语 (马来西亚) |
| mt | 马耳他语 | nl | 荷兰语 (荷兰) |
| nl-be | 荷兰语 (比利时) | no | 挪威语 (博克马尔) |
| no | 挪威语 (尼诺尔语) | pl | 波兰语 |
| pt | 葡萄牙语 (葡萄牙) | pt-br | 葡萄牙语 (巴西) |
| rm | 罗曼什语 | ro | 罗马尼亚语 |
| ro-mo | 罗马尼亚语 (摩尔多瓦) | ru | 俄语 |
| ru-mo | 俄语 (摩尔多瓦) | sb | 塞尔维亚语 |
| sk | 斯洛伐克语 | sl | 斯洛文尼亚语 |
| sq | 阿尔巴尼亚语 | sr | 塞尔维亚语 (拉丁) |
| sr | 塞尔维亚语 (西里尔字母) | sv | 瑞典语 |
| sv-fi | 瑞典语 (芬兰) | sx | 索托语 |
| th | 泰语 | tn | 茨瓦纳语 |
| tr | 土耳其语 | ts | 宗加语 |
| uk | 乌克兰语 | ur | 乌尔都语 |
| vi | 越南语 | xh | 科萨语 |
| zh | 中文 | zh-cn | 中文 (中国) |
| zh-hk | 中文 (香港) | zh-sg | 中文 (新加坡) |
| zh-tw | 中文 (台湾) | zu | 祖鲁语 |

## JavaScript 安全

由于 JavaScript 通常用于网页，因此对于 JavaScript 代码人员来说，安全性是一个重要的考虑因素。涉及敏感信息时，无论使用哪种编程语言，每种网络应用程序都存在许多固有的安全陷阱。这些陷阱包括在不加密的情况下存储敏感信息、使用不充分的加密方法以及将敏感信息存储为“外部世界”成员可以访问的方式。

## 索引

### 符号与数字
- `20 min`：费曼技巧学习时间示例。

### A
- `activeElement` 属性，Document
- `alinkColor` 属性，Document
- `all[]` 数组，Document
- `anchors[]` 数组，Document
- `applets[]` 数组，Document
- `appCodeName` 属性，Navigator
- `appMinVersion` 属性，Navigator
- `appName` 属性，Navigator
- `appVersion` 属性，Navigator
- `arguments[]` 数组，Function
- `arity` 属性，Function

### B
- `background` 属性
- `back()` 方法，History/Window
- `blur()` 方法
- `body` 属性，Document
- `border` 属性
- `Button` 对象
- `button` 属性，Event

### C
- `call()` 方法，Function
- `caller` 属性，Function
- `callee` 属性，Arguments
- `cancelable` 属性，Event
- `cancelBubble` 属性，Event
- `captureEvents()` 方法，Window/Document
- `charAt()` 方法，String
- `charCodeAt()` 方法，String
- `CHARSET` 属性
- `Checkbox` 对象
- `checked` 属性，Checkbox/Radio
- `childNodes` 属性，Node
- `children[]` 数组，HTMLElement
- `className` 属性，HTMLElement
- `clear()` 方法，Document
- `clearInterval()` 方法，Window
- `clearTimeout()` 方法，Window
- `click()` 方法，HTMLElement
- `clientX` / `clientY` 属性，Event
- `close()` 方法，Document/Window
- `closed` 属性，Window
- `compile()` 方法，RegExp
- `concat()` 方法，Array/String
- `confirm()` 方法，Window
- `constructor` 属性，Object
- `contains()` 方法，Node
- `content` 属性
- `cookie` 属性，Document
- `cookieEnabled` 属性，Navigator
- `cos()` 方法，Math
- `cpuClass` 属性，Navigator
- `createElement()` 方法，Document
- `createStyleSheet()` 方法，Document
- `crypto` 属性，Window

### D
- `data` 属性，Event
- `Date` 对象
- `Date()` 构造函数
- `defaultCharset` 属性，Document
- `defaultChecked` 属性，Input
- `defaultSelected` 属性，Option
- `defaultValue` 属性，Input
- `description` 属性，MimeType/Plugin
- `dialog` 属性，Window
- `disableExternalCapture()` 方法，Window
- `domain` 属性，Document
- `do...while` 语句

### E
- `ECMA-262` 标准
- `elementFromPoint()` 方法，Document
- `embeds[]` 数组，Document
- `enabledPlugin` 属性，Navigator
- `enableExternalCapture()` 方法，Window
- `escape()` 方法，Global
- `eval()` 方法，Global
- `event` 对象
- `eventPhase` 属性，Event
- `execCommand()` 方法，Document
- `execScript()` 方法，Window
- `exp()` 方法，Math
- `expando` 属性
- `export` 语句

### F
- `fileCreatedDate` 属性，Document
- `fileModifiedDate` 属性，Document
- `fileSize` 属性，Document
- `fileUpdatedDate` 属性，Document
- `fileUpload` 对象
- `find()` 方法，Window
- `fixed()` 方法，String
- `floor()` 方法，Math
- `focus()` 方法，Window/HTMLElement
- `fontcolor()` 方法，String
- `fontsize()` 方法，String
- `for...in` 语句
- `forward()` 方法，History/Window
- `frames[]` 数组，Window
- `fromCharCode()` 方法，String
- `fromElement` 属性，Event

### G
- `getAttribute()` 方法，HTMLElement
- `getDate()` 方法，Date
- `getDay()` 方法，Date
- `getFullYear()` 方法，Date
- `getHours()` 方法，Date
- `getMilliseconds()` 方法，Date
- `getMinutes()` 方法，Date
- `getMonth()` 方法，Date
- `getSeconds()` 方法，Date
- `getSelection()` 方法，Document
- `getTime()` 方法，Date
- `getTimezoneOffset()` 方法，Date
- `getUTCDate()` 方法，Date
- `getUTCDay()` 方法，Date
- `getUTCHours()` 方法，Date
- `getUTCMilliseconds()` 方法，Date
- `getUTCMinutes()` 方法，Date
- `getUTCMonth()` 方法，Date
- `getUTCSeconds()` 方法，Date
- `getYear()` 方法，Date
- `global` 属性，RegExp

### H
- `height` 属性，Document/Event/Screen
- `history` 属性，Window
- `home()` 方法，Window
- `HTMLElement` 对象

### I
- `id` 属性，HTMLElement
- `if...else` 语句
- `images[]` 数组，Document
- `import` 语句
- `indexOf()` 方法，Array/String
- `innerHTML` 属性，HTMLElement
- `innerText` 属性，HTMLElement
- `innerWidth` / `innerHeight` 属性，Window
- `Input` 对象
- `insertAdjacentHTML()` 方法，HTMLElement
- `insertAdjacentText()` 方法，HTMLElement
- `isFinite()` 函数，Global
- `isNaN()` 函数，Global
- `italics()` 方法，String

### J
- `javaEnabled()` 方法，Navigator
- `JavaScript` 实体
- `JavaScript` 样式表语法
- `join()` 方法，Array

### K
- `keyCode` 属性，Event

### L
- `label` 语句
- `language` 属性，Navigator/Script
- `lastIndexOf()` 方法，Array/String
- `lastModified` 属性，Document
- `layerX` / `layerY` 属性，Event
- `length` 属性，Array/String/Function/NodeList等
- `link()` 方法，String
- `links[]` 数组，Document
- `location` 对象/属性
- `locationbar` 属性，Window
- `log()` 方法，Math
- `LN2` / `LN10` 属性，Math
- `LOG2E` / `LOG10E` 属性，Math

### M
- `match()` 方法，String
- `Math` 对象
- `max()` 方法，Math
- `MAX_VALUE` 属性，Number
- `menubar` 属性，Window
- `mimeType` 属性，Document
- `mimeTypes[]` 数组，Navigator
- `min()` 方法，Math
- `MIN_VALUE` 属性，Number
- `modifiers` 属性，Event
- `moveBy()` 方法，Window
- `moveTo()` 方法，Window

### N
- `name` 属性，Window/HTMLElement/Plugin等
- `NaN` 属性，Global/Number
- `navigator` 对象
- `NEGATIVE_INFINITY` 属性，Number
- `netscape` 属性
- `nextSibling` 属性，Node

### O
- `offscreenBuffering` 属性，Window
- `offsetX` / `offsetY` 属性，Event
- `offsetLeft` / `offsetTop` 属性，HTMLElement
- `offsetParent` 属性，HTMLElement
- `onblur` / `onfocus` 事件处理程序
- `ondragdrop` 事件处理程序
- `onerror` 事件处理程序
- `onload` / `onunload` 事件处理程序
- `onmove` / `onresize` 事件处理程序
- `online` 属性，Navigator
- `open()` 方法，Document/Window
- `opener` 属性，Window
- `Option` 对象
- `oscpu` 属性，Navigator
- `outerHTML` / `outerText` 属性，HTMLElement
- `outerWidth` / `outerHeight` 属性，Window

### P
- `pageX` / `pageY` 属性，Event
- `parent` 属性，Window
- `parentElement` 属性，HTMLElement
- `parentWindow` 属性，Document
- `parse()` 方法，Date
- `parseFloat()` 函数，Global
- `parseInt()` 函数，Global
- `Password` 对象
- `PI` 属性，Math
- `platform` 属性，Navigator
- `plugin` 对象
- `plugins[]` 数组，Navigator
- `pop()` 方法，Array
- `POSITIVE_INFINITY` 属性，Number
- `pow()` 方法，Math
- `previousSibling` 属性，Node
- `print()` 方法，Window
- `prompt()` 方法，Window
- `prototype` 属性，Function/Object
- `push()` 方法，Array

### Q
- `queryCommandEnabled()` 方法，Document
- `queryCommandIndeterm()` 方法，Document
- `queryCommandState()` 方法，Document
- `queryCommandSupported()` 方法，Document
- `queryCommandText()` 方法，Document
- `queryCommandValue()` 方法，Document

### R
- `Radio` 对象
- `random()` 方法，Math
- `readyState` 属性，Document
- `referrer` 属性，Document
- `RegExp` 对象
- `RegExp()` 构造函数
- `releaseEvents()` 方法，Window/Document
- `removeAttribute()` 方法，HTMLElement
- `replace()` 方法，String/Location
- `reset()` 方法，Form
- `Reset` 对象
- `resizeBy()` 方法，Window
- `resizeTo()` 方法，Window
- `return` 语句
- `returnValue` 属性，Event
- `reverse()` 方法，Array
- `round()` 方法，Math
- `routeEvent()` 方法，Window

### S
- `screen` 属性，Window
- `screenX` / `screenY` 属性，Window/Event
- `scroll()` 方法，Window
- `scrollbars` 属性，Window
- `scrollBy()` 方法，Window
- `scrollIntoView()` 方法，HTMLElement
- `scrollTo()` 方法，Window
- `search()` 方法，String
- `select()` 方法，Input/Textarea
- `Select` 对象
- `selected` 属性，Option
- `selectedIndex` 属性，Select
- `selection` 属性，Document
- `setAttribute()` 方法，HTMLElement
- `setDate()` 方法，Date
- `setFullYear()` 方法，Date
- `setHours()` 方法，Date
- `setInterval()` 方法，Window
- `setMilliseconds()` 方法，Date
- `setMinutes()` 方法，Date
- `setMonth()` 方法，Date
- `setResizable()` 方法，Window
- `setSeconds()` 方法，Date
- `setTime()` 方法，Date
- `setTimeout()` 方法，Window
- `setUTCDate()` 等方法，Date
- `shift()` 方法，Array
- `shiftKey` 属性，Event
- `showModalDialog()` 方法，Window
- `sidebar` 属性，Window
- `sin()` / `sqrt()` 方法，Math
- `slice()` 方法，Array/String
- `sort()` 方法，Array
- `sourceIndex` 属性，HTMLElement
- `split()` 方法，String
- `src` 属性，Script/Image/Frame
- `srcElement` 属性，Event
- `srcFilter` 属性，Event
- `stop()` 方法，Window
- `style` 属性，HTMLElement
- `styleSheets[]` 数组，Document
- `submit()` 方法，Form
- `Submit` 对象
- `substr()` / `substring()` 方法，String
- `suffixes` 属性，MimeType

### T
- `tan()` 方法，Math
- `target` 属性，Event/Link/Form
- `Text` 对象
- `Textarea` 对象
- `title` 属性，Document/HTMLElement
- `toElement` 属性，Event
- `toGMTString()` / `toLocaleString()` 方法，Date
- `toLowerCase()` / `toUpperCase()` 方法，String
- `toString()` 方法，Object/Array/Date等
- `type` 属性，Event/Input/Plugin等

### U
- `unshift()` 方法，Array
- `unwatch()` 方法，Object
- `URL` 属性，Document/Location
- `userAgent` 属性，Navigator
- `userLanguage` 属性，Navigator

### V
- `value` 属性，Input/Option/Param等
- `vendor` / `vendorSub` 属性，Navigator
- `visibility` 属性，Style

### W
- `watch()` 方法，Object
- `width` 属性，Document/Event/Screen
- `window` 对象
- `write()` / `writeln()` 方法，Document

### X
- `XOffset` 属性，Window

### Y
- `YOffset` 属性，Window

## 国际联系信息

### 澳大利亚
McGraw-Hill Book Company Australia Pty. Ltd.
TEL: +61-2-9417-9899
FAX: +61-2-9417-5687
`http://www.mcgraw-hill.com.au`
`books-it_sydney@mcgraw-hill.com`

### 新加坡（服务亚洲）
McGraw-Hill Book Company
TEL: +65-863-1580
FAX: +65-862-3354
`http://www.mcgraw-hill.com.sg`
`mghasia@mcgraw-hill.com`

### 加拿大
McGraw-Hill Ryerson Ltd.
TEL: +905-430-5000
FAX: +905-430-5020
`http://www.mcgraw-hill.ca`

### 南非
McGraw-Hill South Africa
TEL: +27-11-622-7512
FAX: +27-11-622-9045
`robyn_swaneepoel@mcgraw-hill.com`

### 希腊、中东、北非
McGraw-Hill Hellas
TEL: +30-1-654-0990-3-4
FAX: +30-1-654-5525

### 英国与欧洲（不包含南欧）
McGraw-Hill Education Europe
TEL: +44-1-628-502500
FAX: +44-1-628-770224
`http://www.mcgraw-hill.com.uk`
`computing_neurope@mcgraw-hill.com`

### 墨西哥（同时也服务拉丁美洲）
McGraw-Hill Interamericana Editores S.A. de C.V.
TEL: +525-117-1583
FAX: +525-117-1589
`http://www.mcgraw-hill.com.mx`
`fernando_castellanos@mcgraw-hill.com`

### 其他所有咨询联系
Osborne/McGraw-Hill
TEL: +1-510-549-6600
FAX: +1-510-883-7600
`http://www.osborne.com`
`omg_international@mcgraw-hill.com`

## 书籍简介

在这份便捷的资源和创意生成器中，你可以轻松找到当前任务所需的 JavaScript 信息。《JavaScript 程序员参考指南》提供了核心 JavaScript 语法、语句、控制结构、函数和对象的关键细节和工作示例。你还将获得关于跨平台实现 JavaScript 的具体说明。在这份简明的参考书中，你将找到重要的技巧和专家编程建议——所有内容以易于理解的格式呈现。

- 快速查找核心 JavaScript 语言规范、数据类型、变量和运算符
- 获取 JavaScript 内置基础对象和函数的详细信息
- 在浏览器中实现 JavaScript 的客户端对象、方法和属性
- 享受拥有一份小型桌面参考书的便利

**作者简介**：

**Christian MacAulay** 是一位网页编码员、设计师、作家和培训师。他擅长使用多种客户端和服务器端技术开发交互且友好的网站。他的文章经常发表在《Web Review》上，他的培训手册出现在教室和网络上。

**Paul Dobson** 是一位网页开发者，在互联网和内网网站的全生命周期开发方面拥有丰富经验。他是一位经验丰富的客户端 JavaScript 和 HTML 开发者，也是一位资深的 Perl 程序员。

## 示例代码

```javascript
if (condVar > someVal) {console.log("xxx")}
```
