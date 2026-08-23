# 艾迪森·韦斯利 JavaScript 参考卡片

`Javascript`：一种脚本语言，旨在集成到HTML代码中，以创建增强的、动态的、交互式的网页。

## 数据类型

定义：根据值存储的具体类别对其进行的分类。

基本类型：字符串、布尔值、整数、浮点数、空值、无定义值。

复合类型：对象、数组、函数。复合数据类型在代码中位于单独的部分。

### 数值型

**整数**：没有小数部分或小数点的正数或负数。

**浮点数**：包含小数点或科学记数法的正数或负数。

**字符串**：由单引号或双引号括起来的可读字符或文本序列。

**布尔值**：用于比较数据或做出决策的逻辑值，例如 `True`/`False`。

**空值**：变量没有值；没有值可报告。`Null`与零不同，零是一个数值。

**类型转换**：将一种类型的变量内容移动到不同类型的变量中。你并非将内容移动到不同的变量；它保持在同一个变量中，但数据类型被改变或“重新转换”。

## 变量

定义：用于存储数据的占位符。在JavaScript中，声明语句由保留字 `var` 和一个或多个变量的名称（标识符）组成。

格式：

```
var variable_name
```
`var` 命令用于声明（创建）变量。

示例：

```
var myHouseColor
var myAddress
var vacation_house, condominium, primaryResidence
```

变量命名规则：

1. 变量不能是保留字。
2. 变量必须以字母或下划线开头，不能以符号、数字或算术符号开头。
3. 变量名中不能包含空格。

提示：

1. 虽然JavaScript中的变量可以在未声明的情况下使用，但良好的编程实践是声明（初始化）所有变量。
2. 变量名区分大小写；例如，`X` 不等于 `x`。

### 初始化变量

使用声明语句为变量赋值。值在等号的右边；变量在左边。

格式：

```
var variable_name = value
```

示例：

```
var myHouseColor = "yellow"
// 将字符串字面量值 yellow 赋值给变量 myHouseColor

var myAddress = 473
// 将数值 473 赋值给变量 myAddress

var bookTitle = "Time Capsule", cost = 28.95, publisher = "Tucker Bay"
// 可以在一条语句中为多个变量赋值
```

## 决策与控制结构

定义：用于改变计算机操作执行顺序的语句和结构。

类型：条件分支 `IF`、`IF-ELSE`、`IF-ELSE IF`、`SWITCH`、`WHILE`、`DO`、`FOR`

### 条件语句

`IF` 语句：一种条件分支语句，用于判断指定条件是否为真。

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

`IF-ELSE` 语句：一种条件分支语句，包含条件为真时执行的路径和条件为假时执行的路径。

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

`IF-ELSE IF` 语句：一种允许有两个以上可能路径的条件分支语句。当第一次遇到为真的条件时，执行该语句，其余条件将不再被测试。

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

`SWITCH` 语句：处理多个选项时`IF-ELSE IF` 语句的一种替代方案。将表达式与测试值进行比较以找到匹配项。

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

`FOR` 循环：

格式：

```
For (initialization; conditional test; increment/decrement) {
    要执行的语句;
}
```

示例：

```
For (var i=0; i<=10; i++) {
    document.write ("This line " + i);
}
```

`DO/WHILE` 循环：

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
    document.write ("This line " + i);
    i++;
} while (i <= 10);
```

`WHILE` 循环：

格式：

```
while (condition) {
    要执行的语句;
}
```

示例：

```
var i = 0;
while (i<=10) {
    document.write ("This line " + i);
    i++;
}
```

提示：注意无限循环，它们没有停止条件，永远达到。

## 对象

定义：对象是一种复合类型，包含属性和方法。JavaScript包含内置对象，允许用户自定义对象。创建对象：使用 `new` 构造函数

```
var X = new Array()
```

示例：日期、时间、数学、字符串。

### 数组对象

定义：数组对象是存储多个值的变量。每个值都有一个索引，通过索引来引用。数组与简单变量一样。格式：

```
var arrayname = new Array(size)
```

提示：当你创建数组时，创建了数组的一个实例。数组的所有属性都可使用。示例：

```
var days = new Array (7)
```
包含七元素的数组。第一个项目是 `days[0]`，最后一个项目是 `days[6]`。初始化数组：

```
days[0] = "Sunday";
days[1] = "Monday";
```

### 字符串对象

定义：字符串对象通过赋值给变量，或者使用新的构造函数创建。

```
var name = new String("Carol");
```

属性：
- `length`：返回字符串中的字符数

原型：
- `big`
- `blink`
- `italics`

方法：允许用户查找、匹配或更改字符串模式
- `indexOf()`
- `charAt()`
- `replace()`

### 数学对象

定义：数学对象允许基本算术计算。是一个内置对象，不需要定义。示例：

- `Math.abs(number)` 返回数值的绝对值
- `Math.cos(number)` 返回弧度
- `Math.round(number)` 将数字舍入接近的整数

### 日期/时间对象

定义：日期对象用于获取或设置日期信息。注意：不支持170年。

### 函数

定义：一个代码块，用于执行任务。有些函数会返回值；其他函数遵循相同的规则。括号中可以没有参数。格式：

```
function 函数名 (参数) {
    要执行的语句;
}
```

自定义函数：

`parseInt()` 或 `parseFloat()` 将字符串转换为数字。示例：

```
function kilosToPounds(kilos) {
    pounds=kilos*2.2;
}
```
获取 `kilos` 的值，乘以2.2，将结果赋值给变量 `pounds`。调用函数：给出函数名，后面跟参数 `kilosToPounds(X)`

## 综合应用：网络中的 JavaScript

**Cookies**：浏览器在用户计算机上存储文本消息。**目的**：识别用户、存储偏好，并在每次访问页面时呈现定制信息。**类型**：临时（会话）存储在临时内存中，仅在会话期间可用。**持久**（永久的）存储在计算机上，直到删除或过期。**浏览器检测**：一个脚本，用于确定正在运行哪个浏览器；确定浏览器是否有能力。**嗅探**：用于是否存在特定的功能；例如，在加载网页前检测。**事件处理**：使用 HTML 事件属性（鼠标悬停、点击等）并将事件连接到事件处理器。

## 方法

定义：一种特殊的函数，用于描述对象的行为。JavaScript 中的每种类型都有相关的方法供使用。示例：

```
array.sort();
document.write();
string.length();
```

## 运算符

### 算术运算符

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| + | 加法 | 两个数字相加 |
| - | 减法 | 从一个数字中减去另一个数字 |
| * | 乘法 | 两个数字相乘 |
| / | 除法 | 一个数字除以另一个数字 |
| % | 取模 | 返回两个数字除后的整数余数 |
| ++ | 自增 | 数值变量加一 |
| -- | 自减 | 数值变量减一 |

### 字符串运算符

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| + | 连接 | 连接或连接两个字符串或其他元素 |
| += | 连接/赋值 | 连接两个字符串并将结果赋值给第一个变量 |

### 逻辑运算符

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| && | 逻辑与 | 比较两个操作数；如果两者都为 true，则返回 true，否则返回 false |
| \| | 逻辑或 | 比较两个操作数；如果任一操作数为 true，则返回 true，否则返回 false |
| ! | 逻辑非 | 如果其操作数可以转换为 true，则返回 false，否则返回 false |

### 比较运算符

| 符号 | 描述 |
| :--- | :--- |
| == | 如果操作数相等，则返回 true |
| != | 如果操作数不等，则返回 true |
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
| += | 两个数值操作数相加，并将结果赋值给第一个 |
| -= | 从第一个操作数中减去另一个操作数，并将结果赋值给第一个 |
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
| catch | finally | new | transient |
| char | float | null | true |
| class | finally | package | try |
| const | for | private | typeof |
| continue | function | protected | var |
| debugger | goto | public | void |
| default | if | return | volatile |
| delete | implements | short | while |
| double | import | static | with |
| do | in | super | |