# 艾迪森·韦斯利 JavaScript 参考卡片





**Javascript：** 一种脚本语言，旨在集成到HTML代码中，以创建增强的、动态的、交互式的网页。

## 数据类型

*定义：* 根据值存储的具体类别对其进行的分类。

*基本类型：* 字符串、布尔值、整数、浮点数、空值、无定义值

*复合类型：* 对象、数组、函数。复合数据类型在代码中位于单独的部分。

### 数值型

**整数：** 没有小数部分或小数点的正数或负数。

**浮点数：** 包含小数点或科学记数法的正数或负数。

**字符串：** 由单引号或双引号括起来的可读字符或文本序列。

**布尔值：** 用于比较数据或做出决策的逻辑值，例如 True/False。

**空值：** 变量没有值；没有值可报告。Null与零不同，零是一个数值。

**类型转换：** 将一种类型的变量内容移动到不同类型的变量中。你并非将内容移动到不同的变量；它保持在同一个变量中，但数据类型被改变或“重新转换”。

## 变量

*定义：* 用于存储数据的占位符。在JavaScript中，声明语句由保留字 `var` 和一个或多个变量的名称（标识符）组成。

*格式：*

```
var variable_name
[var 命令用于声明（创建）变量]
```

*示例：*

```
var myHouseColor
var myAddress
var vacation_house, condominium, primaryResidence
```

*变量命名规则：*

1. 变量不能是保留字。
2. 变量必须以字母或下划线开头，不能以符号、数字或算术符号开头。
3. 变量名中不能包含空格。

**提示：**

1. 虽然JavaScript中的变量可以在未声明的情况下使用，但良好的编程实践是声明（初始化）所有变量。
2. 变量名区分大小写；例如，X 不等于 x。

### 初始化变量

使用声明语句为变量赋值。值在等号的右边；变量在左边。

格式：

```
var variable_name = value
```

示例：

```
var myHouseColor = "yellow"
[将字符串字面量值 yellow 赋值给变量 myHouseColor]

var myAddress = 473
[将数值 473 赋值给变量 myAddress]

var bookTitle = "Time Capsule", cost = 28.95, publisher = "Tucker Bay"
[可以在一条语句中为多个变量赋值]
```

## 决策与控制结构

**定义：** 用于改变计算机操作执行顺序的语句和结构。

**类型：**

条件分支 IF、IF-ELSE、IF-ELSE IF、SWITCH、WHILE、DO、FOR

### 条件语句

IF 语句：一种条件分支语句，用于判断指定条件是否为真。

格式：

```
if (condition) {
    条件为真时执行的语句
}
```

示例：

```
if (score >= 65) {
    grade = "Pass";
    message = "Congratulations";
}
```

IF-ELSE 语句：一种条件分支语句，包含条件为真时执行的路径和条件为假时执行的路径。

格式：

```
if (condition) {
    条件为真时执行的语句;
} else {
    条件为假时执行的语句;
}
```

示例：

```
if (score >= 65) {
    grade = "Pass";
    message = "Congratulations";
} else {
    grade = "Fail"
    message = "Try again";
}
```

IF-ELSE IF 语句：一种允许有两个以上可能路径的条件分支语句。当第一次遇到为真的条件时，执行该语句，其余条件将不再被测试。

格式：

```
if (condition) {
    条件为真时执行的语句;
} else if (condition) {
    条件为真时执行的语句;
} else {
    如果没有先前的条件为真，则执行的语句;
}
```

示例：

```
if (score>=90) {
    grade="A";
}
else if (score>=80) {
    grade="B";
}
else if (score>=70) {
    grade="C";
}
else if (score>=65) {
    grade="D";
}
else {
    grade="F";
}
```

SWITCH 语句：处理多个选项时，IF-ELSE IF 语句的一种替代方案。将表达式与测试值进行比较以找到匹配项。

格式：

```
switch (expression or variable name) {
    case label:
        如果表达式匹配此标签，则执行的语句;
        break;
    case label:
        如果表达式匹配此标签，则执行的语句;
        break;
    default:
        如果表达式不匹配任何标签，则执行的语句;
        break;
}
```

示例：

```
switch (colorchoice) {
    case "red":
        document.bgColor="red";
        break;
    case "blue":
        document.bgColor="blue";
        break;
    default:
        document.bgColor="white";
        break;
}
```

### 循环

循环使一段代码重复执行，直到满足指定条件。你可以对任何类型的代码使用任何循环格式。

FOR 循环：

格式：

```
For (initialization; conditional test; increment/decrement) {
    要执行的语句;
}
```

示例：

```
For (var i=0; i<=10; i++) {
    document.write ("This is line " + i);
}
```

DO/WHILE 循环：

格式：

```
do {
    要执行的语句;
} while (condition);
```

示例：

```
var i=0;
do {
    document.write ("This is line " + i);
    i++;
} while (i <=10);
```

WHILE 循环：

格式：

```
while (condition) {
    语句;
    递增/递减;
}
```

示例：

```
var i = 0;
while (i<=10) {
    document.write ("This is line " + i);
    i++;
}
```

提示：注意无限循环，它们没有停止条件，或者停止条件永远无法达到。

## 对象

定义：对象是一种复合数据类型，包含属性和方法。JavaScript包含内置对象，并允许用户创建自定义对象。

创建对象：使用 `new` 构造函数

```
var X = new Array()
```

示例：
日期、时间、数学、字符串、数组

### 数组对象

定义：数组对象是存储多个值的变量。每个值在数组中都有一个索引编号，每个值都通过数组名和索引编号来引用。数组与简单变量一样，可以保存任何类型的数据。在创建数组时，你可以将大小留空。数组的大小将由放置在其中的项目数量决定。

格式：

```
var arrayname = new Array(size)
```

提示：当你创建数组时，你创建了数组对象的一个新实例。数组对象的所有属性和方法都可用于你的新数组。

示例：

```
var days = new Array (7)
```

这使用数组构造函数创建了一个包含七个元素的数组。
第一个项目是 `days[0]`，最后一个项目是 `days[6]`。

#### 初始化数组：

数组项目可以当作简单变量处理：

```
days[0] = "Sunday";
days[1] = "Monday";
等等。
```

### 字符串对象

定义：字符串对象通过将字符串赋值给变量来创建，或者使用新的对象构造函数来创建。

示例：

```
var name = "Carol";
var name = new String("Carol");
```

属性：
- **长度：** 返回字符串中的字符数
- **原型：** 允许用户为字符串添加方法和属性

方法：
- 字符串格式化方法（类似于HTML格式化标签）
    - `String.big`
    - `String.blink`
    - `String.italics`
- 子字符串方法（允许用户查找、匹配或更改字符串中的字符模式）
    - `indexOf()`
    - `charAt()`
    - `replace()`

### 数学对象

定义：数学对象允许进行基本算术运算符不支持的算术计算。Math是一个内置对象，用户不需要定义。

示例：
- `Math.abs(number)` 返回数值参数的绝对值
- `Math.cos(number)` 返回参数的余弦值，以弧度为单位
- `Math.round(number)` 将数字四舍五入到最接近的整数

### 日期/时间对象

日期对象提供用于获取或设置日期和时间信息的方法。
注意：不支持1970年1月1日之前的日期。



### 函数

*定义：* 一个预编写的代码块，用于执行特定任务。有些函数会返回值；其他函数则执行排序等任务，但不返回值。函数名遵循与变量名相同的规则。括号中可以有参数，也可以没有，但括号必须存在。

**用户自定义函数：**

*示例：*

`parseInt()` 或 `parseFloat()` 将字符串转换为数字。

创建一个函数：

格式：

```
function 函数名 (参数) {
    函数被调用时
    要执行的语句;
}
```

示例：

```
function kilosToPounds (){
    pounds=kilos*2.2046;
}
```

这个新函数获取变量 `kilos` 的值，乘以 2.2046，然后将结果赋值给变量 `pounds`。

调用一个 *函数*：给出函数名，后面跟上参数（如果有的话）

`parseInt(X)`；将变量 `X` 中存储的数据转换为数值。

`kilosToPounds(17)`；将 17 公斤转换为相同质量的磅数，返回值 37.4782。

## 综合应用：网络中的 JavaScript 与 HTML

**Cookies：** 浏览器在用户计算机上存储的文本文件消息

*目的：* 识别用户、存储偏好设置，并在用户每次访问页面时呈现定制化信息

*类型：*

*临时*（临时的、会话）— 存储在临时内存中，仅在浏览器会话期间可用

*持久*（永久的、存储的）— 保留在用户计算机上，直到被删除或过期

**浏览器检测：** 一个脚本，用于确定正在运行的是哪个浏览器；确定浏览器是否有能力加载网页并支持 JavaScript 代码；以及在需要时，加载备用的 JavaScript 代码以匹配浏览器和平台。

**嗅探：** 一个脚本，用于确定是否存在特定的浏览器功能；例如，在加载网页前检测 Flash 的存在。

**事件处理：** 使用 HTML 事件属性（鼠标悬停、鼠标点击等）并将事件连接到一个称为事件处理器的 JavaScript 函数

## 方法

*定义：* 一种特殊类型的函数，用于描述或指示对象的行为方式。JavaScript 中的每种对象类型都有相关的方法可供使用。

*示例：*

```
array.sort();
document.write();
string.length();
```

**调用：** 要调用或使用一个方法，请说明方法名，后跟括号中的参数。

*示例：*

```
document.write("Hello, world!");
```

## 运算符

### 算术运算符

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| + | 加法 | 两个数字相加 |
| - | 减法 | 从一个数字中减去另一个数字 |
| * | 乘法 | 两个数字相乘 |
| / | 除法 | 一个数字除以另一个数字 |
| % | 取模 | 返回两个数字相除后的整数余数 |
| ++ | 自增 | 数值变量加一 |
| -- | 自减 | 数值变量减一 |

### 字符串运算符

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| + | 连接 | 连接或连接两个字符串或其他元素 |
| += | 连接/赋值 | 连接两个字符串变量并将结果赋值给第一个变量 |

### 逻辑运算符

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| && | 逻辑与 | 比较两个操作数；如果两者都为 true，则返回 true，否则返回 false |
| \|\| | 逻辑或 | 比较两个操作数；如果任一操作数为 true，则返回 true，否则返回 false |
| ! | 逻辑非 | 如果其操作数可以转换为 true，则返回 false，否则返回 false |

### 比较运算符

| 符号 | 描述 |
| :--- | :--- |
| == | 如果操作数相等，则返回 true |
| != | 如果操作数不相等，则返回 true |
| === | 如果操作数相等且数据类型相同，则返回 true |
| !== | 如果操作数不相等和/或数据类型不同，则返回 true |
| > | 如果第一个操作数大于第二个，则返回 true |
| >= | 如果第一个操作数大于或等于第二个，则返回 true |
| < | 如果第一个操作数小于第二个，则返回 true |
| <= | 如果第一个操作数小于或等于第二个，则返回 true |

### 赋值运算符

| 符号 | 描述 |
| :--- | :--- |
| = | 将第二个操作数的值赋给第一个操作数 |
| += | 两个数值操作数相加，并将结果赋值给第一个操作数 |
| -= | 从第一个操作数中减去第二个操作数，并将结果赋值给第一个 |
| *= | 两个操作数相乘，并将结果赋值给第一个 |
| /= | 第一个操作数除以第二个操作数，并将结果赋值给第一个 |
| %= | 计算两个数值操作数的模，并将结果赋值给第一个 |

### 保留字

| 字 | 字 | 字 | 字 |
| :--- | :--- | :--- | :--- |
| abstract | else | instanceof | switch |
| boolean | enum | int | synchronized |
| break | export | interface | this |
| byte | extends | long | throw |
| case | false | native | throws |
| catch | final | new | transient |
| char | finally | null | true |
| class | float | package | try |
| const | for | private | typeof |
| continue | function | protected | var |
| debugger | goto | public | void |
| default | if | return | volatile |
| delete | implements | short | while |
| do | import | static | with |
| double | in | super | |
