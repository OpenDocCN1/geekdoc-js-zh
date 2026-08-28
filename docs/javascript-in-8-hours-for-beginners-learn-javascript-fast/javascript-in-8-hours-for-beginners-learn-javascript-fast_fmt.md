
# JavaScript 8 小时：初学者指南，快速学习 JavaScript！

![](img/74374e7cea0edb214250be898a4b6131_0_0.png)

# 关于作者

## Ray Yao

- 美国 Zend 认证 PHP 工程师
- 美国 Sun 认证 JAVA 程序员
- 美国 Oracle 认证 SCWCD 开发人员
- 美国 CompTIA 认证 A+ 专业人士
- 美国 Microsoft 认证 ASP . NET 专家
- 美国 Microsoft 认证 MCP 专业人士
- 美国 CompTIA 认证 NETWORK+ 专业人士

## Ray Yao 的著作

- Linux 命令行
- JAVA 面试 100 题
- PHP 面试 100 题
- 8 小时精通 JAVA
- 8 小时精通 PHP
- 8 小时精通 JavaScript
- 8 小时精通 C++
- Ray Yao 系列书籍

# 前言

“8 小时精通 JavaScript”是一本适合初学者的实用书籍。你可以快速、轻松地学习 JavaScript 的完整基础知识。直观的定义、平易简单的示例、详尽的解释以及整洁美观的布局是这本极具益性和教育意义书籍的特点。新颖独特的风格将让你印象深刻。阅读这本书是一种巨大的享受！你可以在 8 小时内掌握所有的核心 JavaScript 技能。

从今天开始编程吧！

- 什么是 JavaScript？
- 注释
- 关键字
- 变量
- 数据类型
- 转义序列
- 函数
- 带参数的函数
- 返回值
- 变量作用域
- 显示文本
- 算术运算符
- 逻辑运算符
- 赋值运算符
- 比较运算符
- 条件运算符
- if 语句
- if-else 语句
- switch 语句
- for 循环
- while 循环
- do-while 循环
- 显示数组元素值
- 获取数组大小
- 合并数组元素
- 反转元素顺序
- 切片元素
- 排序元素
- 将元素转换为字符串
- 搜索特定元素 (1)
- 搜索特定元素 (2)
- Math 方法
- Ceil () & Floor ()
- Max () & Min ()
- Math.PI & random()
- 日期与时间
- 年、月、日
- 时、分、秒
- 不同时间
- 设置日期和时间
- 定时函数
- 字符串长度
- 合并字符串
- 搜索字符
- 转换字符大小写
- 将字符串转换为数组
- 提取子字符串
- 将数字转换为字符串
- 将字符串转换为数字
- 搜索特定文本 (1)
- 搜索特定文本 (2)
- 对象声明
- 页面导航
- 跳转到指定页面
- 打开自定义窗口
- 确认框
- 提示输入
- 通过 ID 定位元素
- 通过标签名定位元素
- break 语句
- continue 语句
- HTML 基础
- 点击事件 (click)
- 加载事件 (onload)
- 卸载事件 (unload)
- 鼠标悬入事件 (mouseover)
- 鼠标移出事件 (mouseout)
- 按键按下事件 (onkeydown)
- 按键释放事件 (onkeyup)
- 焦点事件 (focus)
- 模糊事件 (blur)
- 表单基础
- 访问表单属性
- 赋值文本
- 重置方法
- 提交方法
- “选择框”
- “单选框”
- “复选框”
- JavaScript: Function () (1)
- JavaScript: Function () (2)
- HTML 复习
- HTML 符号
- CSS 复习

# 结语

# 第一小时

## JavaScript 基础

### 什么是 JavaScript？

JavaScript 是一种动态计算机编程语言，用于制作交互式网页。它的解释器嵌入在浏览器软件（如 IE、Chrome 和 Firefox 等）中。它在访问者的计算机和浏览器上运行。

JavaScript 的语法如下：

```html
<script type="text/javascript">
......
</script>
```

### 示例

```html
<script type="text/javascript">
alert("Hello World");
</script>
```

（输出: Hello World）

### 解释

`alert` 会弹出一个显示消息的警告框。

`alert("Hello World")` 显示 "Hello World" 消息。

JavaScript 块可以位于 HTML 的任何地方。

### 注释

注释用于解释代码。

```javascript
// 这是一个单行注释
/*
这是一个多行注释；JavaScript 解释器
将忽略单行注释和多行
注释。
*/
```

### 示例

```javascript
function test() {
  alert("show a sample");
}

test();
```

(输出: show a sample)

### 解释

`test()` 是调用名为 `test(){ }` 的函数的命令。

当运行函数 `test()` 时，它将输出“show a sample”。

### 带参数的函数

函数在括号内可以有一个或多个参数。参数用于向函数传递数据。

```javascript
function function-name(var arg) {......}
```

```javascript
function-name(argument);
```

### 示例

```javascript
<script type="text/javascript">
function test(var arg) {
  alert(arg);
}
</script>
```

(输出: display a sample)

### 解释

当 `test("display a sample")` 调用函数 `test(var arg){...}` 时，它会将“display a sample”传递给 `var arg`。`var arg` 接收到数据后，它将传递函数内部的数据。`alert(arg)` 将使用该数据，然后输出“display a sample”。

### 返回值

`return` 可以向调用者返回一个值。

```javascript
function function-name(var arg) { return value }
```

要调用函数，请使用 `function-name(argument);`。

```javascript
function cube(var num) {
  return num * num * num;
}

alert(cube(2)); // 输出: 8
```

### 解释

`cube(2)` 意味着 `cube(2)` 调用了函数 `cube(var num){ }`，并将参数“2”传递给 `num`。

`return num*num*num` 将结果返回给调用者 `cube(2)`，你可以将其视为 `cube(2) = return num*num*num`，将值赋值给 `cube(2)`。

`alert(cube(2))` 将显示 `cube(2)` 的结果。

### 变量作用域

全局变量声明在函数外部，可以在任何地方使用；局部变量声明在函数内部，它只在当前函数内部使用。

### 示例

```javascript
<script type="text/javascript">
var num = 200; // 变量 num 是全局变量。

function test() {
  var num = 100; // 变量 num 是局部变量 
  alert(num);
}
</script>
```

(输出: 200)

### 解释

`alert(num)` 输出 200，这意味着变量 `num` 存储的是全局变量的值。

局部变量仅在声明它们的函数块内可见。

### 显示文本

```javascript
document.write()
```

`document.write()` 简单地将指定的文本打印或显示在当前网页上。

### 示例

```javascript
<script type="text/javascript">
document.write("Hello World Again!");
</script>
```

(输出: Hello World Again!)

### 解释

`document.write("Hello World Again!")` 直接将字符显示到 HTML 页面中。

注意，`alert()` 会弹出一个显示消息的对话框。

## 第 2 小节

### 运算符

### 算术运算符

| 运算符 | 说明 |
| --- | --- |
| + | 加法 |
| - | 减法 |
| * | 乘法 |
| / | 除法 |
| % | 取模 |
| ++ 或 -- | 加1或减1 |

`%` 取模运算符将第一个操作数除以第二个操作数，返回余数。例如 `4%2`，余数为 0。

### 示例

```javascript
var add = 100 + 200; alert(add);
var div = 800 / 2; alert(div);
var mod = 10 % 3; alert(mod);
var inc = 10; alert(++inc);
var str = "abc"; alert(str);
```

### 解释

```javascript
var add = 100 + 200; alert(add); // 输出 300
var div = 800 / 2; alert(div); // 输出 400
var mod = 10 % 3; alert(mod); // 输出 1
var inc = 10; alert(++inc); // 输出 11
var str = "abc"; alert(str); // 输出 abc
```

### 逻辑运算符

| 运算符 | 说明 |
| --- | --- |
| && | 与 |
| \|\| | 或 |
| ! | 非 |

使用逻辑运算符后，结果将为真（true）或假（false）。

### 示例

```javascript
var x = true; var y = false;
var a = x && y; alert(a); // 输出: false
var b = x || y; alert(b); // 输出: true
```

### 解释

| 运算符 | 等价于 |
| --- | --- |
| && | true; false |
| \|\| | true; false |
| ! | true; false |

### 赋值运算符

| 运算符 | 示例 | 等价于 |
| --- | --- | --- |
| += | x += y | x = x + y |
| -= | x -= y | x = x - y |
| *= | x *= y | x = x * y |
| /= | x /= y | x = x / y |
| %= | x %= y | x = x % y |

### 示例

```javascript
var a = 100;
```

### 比较运算符

| 运算符 | 说明 |
| --- | --- |
| > | 大于 |
| < | 小于 |
| >= | 大于等于 |
| <= | 小于等于 |
| == | 等于 |
| != | 不等于 |

使用比较运算符后，结果将为真或假。

### 示例

```javascript
var a = 100; var b = 200;
if (a < b) { ... }
```

### 解释

`a < b` 是一个比较表达式，`100 < 200` 为真。

### 三元运算符

```javascript
condition ? expression_if_true : expression_if_false
```

### 示例

```javascript
var a = 100; var b = 200;
var result = (a < b) ? "true" : "false";
alert(result);
```

### 解释

如果 `(a < b)` 为真，则 `result` 被赋值为 "true"，否则赋值为 "false"。由于 `100 < 200` 为真，因此 `result` 将被赋值为 "true"。

### if 语句

```javascript
if (condition) {
  // 代码块
}
```

### 示例

```javascript
var a = 100; var b = 200;
if (a < b) {
  alert("a is less than b");
}
```

### 解释

如果条件为真，则执行代码块。

### if-else 语句

```javascript
if (condition) {
  // 代码块 1
} else {
  // 代码块 2
}
```

### 示例

```javascript
var a = 100; var b = 200;
if (a > b) {
  alert("a is greater");
} else {
  alert("b is greater or equal");
}
```

### 解释

如果条件为真，执行代码块 1；否则执行代码块 2。

### switch 语句

```javascript
switch (variable) {
  case value1: 
    // 如果匹配此情况，执行此代码
    break;
  case value2: 
    // 如果匹配此情况，执行此代码
    break;
  case value3: 
    // 如果匹配此情况，执行此代码
    break;
  default: 
    // 如果不匹配任何情况，执行默认代码
    break;
}
```

变量的值将首先与每个 `case` 进行比较；如果匹配其中一个 `case` 值，它将执行该 `case` 代码。`break;` 终止代码运行。

### 示例

```javascript
var number = 20;
switch (number) {
  case 10: alert("Running case 10"); break;
  case 20: alert("Running case 20"); break;
  case 30: alert("Running case 30"); break;
  default: alert("Running default code"); break;
}
```

### 解释

`number` 的值为 20；它将匹配 `case 20`，因此它将运行 `case 20` 的代码。

### for 循环

```javascript
for (init; test-expression; increment) {
  // 代码块
}
```

`for` 循环通过指定的次数执行一段代码块。

### 示例

```javascript
<script type="text/javascript">
for (var x = 0; x <= 5; x++) {
  document.write(x + " ");
}
</script>
```

(输出: 0 1 2 3 4 5)

### 解释

`var x = 0` 是初始化器，
`x <= 5` 是测试表达式，代码最多运行 6 次（0 到 5）。
循环 6 次后，代码将输出 `0 1 2 3 4 5`。

### while 循环

```javascript
while (test-expression) {
  // 代码块
}
```

`while` 循环如果指定的条件为真，则循环执行一段代码块。

### 示例

```javascript
var counter = 0;
while (counter < 8) {
  document.write("&");
  counter++;
}
```

(输出: &&&&&&&&)

### 解释

`counter < 8` 是一个测试表达式，如果条件为真，代码将循环，直到 `counter` 达到 8，此时条件为假，代码将停止运行。

### do-while 循环

```javascript
do {
  // 代码块
} while (test-expression);
```

`do...while` 先循环一次一段代码块，如果指定的条件为真，则重复该循环。

### 示例

```javascript
var counter = 0;
do {
  document.write("@");
  counter++;
} while (counter < 8);
```

(输出: @@@@@@@@)

### 解释

`counter < 8` 是一个测试表达式，如果条件为真，代码将循环，直到 `counter` 达到 8，此时条件为假，代码将停止运行。

## 第 3 小时

### 数组

### 创建数组

`new Array()` 创建一个数组。

创建数组的语法：

```javascript
var array-name = new Array("value0", "value1", "value2");
```

创建数组的其他语法：

```javascript
var array-name = ["value0", "value1", "value2"];
```

### 示例

```javascript
var color = new Array();
color[0] = "red";
color[1] = "blue";
color[2] = "green";
```

### 解释

上述代码创建了一个数组，数组名为 `color`，它有三个元素：`color[0]`、`color[1]`、`color[2]`。它的索引是 0、1 和 2。它的值是 red、blue 和 green。

注意索引从 0 开始。

### 显示数组元素的值

要显示数组元素的值，请使用如下所示的语法：

```javascript
document.write(array-name[index]);
```

### 示例

```javascript
<script type="text/javascript">
var color = new Array("yellow", "purple", "orange");
document.write(color[1]);
</script>
```

(输出: purple)

### 解释

`color[0]` 的值是 yellow。
`color[1]` 的值是 purple。
`color[2]` 的值是 orange。

注意索引从零开始。

### 获取数组大小

`array.length` 可以获取数组的大小。

### 示例

```javascript
<script type="text/javascript">
var color = new Array("yellow", "purple", "orange");
var size = color.length;
document.write(size);
</script>
```

(输出: 3)

### 解释

`var size = color.length` 可以返回数组 `color` 的大小，并将数组的大小赋值给 `size`。

`new Array("yellow", "purple", "orange")` 有三个元素，所以它的大小是 3。

### 合并元素

```javascript
array.join();
array.join(" ");
array.join(", ");
```

`array.join()` 可以合并所有数组元素且不留空格。
`array.join(" ")` 可以通过空格合并所有数组元素。
`array.join(",")` 可以通过逗号合并所有数组元素。

### 示例

```javascript
var arr = new Array();
arr[0] = "I";
arr[1] = "love";
arr[2] = "JavaScript!";
document.write(arr.join(" ")); // 输出: I love JavaScript!
```

### 解释

`arr.join(" ")` 可以通过空格将 `arr` 的所有元素连接在一起。当然，你也可以尝试 `arr.join(",")` 用逗号连接元素。

### 反转元素顺序

```javascript
array.reverse();
```

`array.reverse()` 可以反转数组的元素顺序。

### 示例

```javascript
var arr = new Array("A", "B", "C");
arr.reverse(); // 反转元素顺序
var rev = arr.join(",");
```

(输出: C,B,A)

### 解释

`arr.reverse()` 反转了 `arr` 数组的元素顺序。
`rev = arr.join(",")` 将 `arr` 的所有元素合并并将值赋值给 `rev`。

### 切片元素

```javascript
array.slice(start, end);
```

`array.slice(start, end)` 可以将数组元素切成切片。
`start` 表示起始位置，
`end` 表示结束位置（不包含）。

### 示例

```javascript
var arr = new Array("a", "b", "c", "d", "e", "f");
var sli = arr.slice(2, 5);
document.write(sli); // 输出: c,d,e
```

### 解释

`arr.slice(2, 5)` 提取从索引 2 到 4 的元素（不包含 5）。

### 排序元素

```javascript
array.sort();
```

`array.sort()` 可以对数组元素进行排序。

### 示例

```javascript
var arr = new Array("C", "A", "B");
arr.sort();
document.write(arr.join(",")); // 输出: A,B,C
```

### 解释

`arr.sort()` 对 `arr` 数组的元素进行排序。

### 将元素转换为字符串

```javascript
array.toString();
```

`array.toString()` 可以将数组元素转换为字符串。

### 示例

```javascript
var arr = new Array("A", "B", "C");
var str = arr.toString();
document.write(str); // 输出: A,B,C
```

### 解释

`arr.toString()` 将 `arr` 数组转换为字符串。

### 搜索特定元素 (1)

```javascript
array.indexOf(element);
```

`array.indexOf(element)` 可以找到特定元素在数组中首次出现的索引。

### 示例

```javascript
var arr = new Array("A", "B", "C", "B");
var index = arr.indexOf("B");
document.write(index); // 输出: 1
```

### 解释

`arr.indexOf("B")` 返回 "B" 在 `arr` 中第一次出现的索引。输出为 1。

如果在数组中未找到该元素，`indexOf()` 返回 -1。

### 搜索特定元素 (2)

```javascript
array.lastIndexOf(element);
```

`array.lastIndexOf(element)` 可以找到特定元素在数组中最后一次出现的索引。

### 示例

```javascript
var arr = new Array("A", "B", "C", "B");
var index = arr.lastIndexOf("B");
document.write(index); // 输出: 3
```

### 解释

`arr.lastIndexOf("B")` 返回 "B" 在 `arr` 中最后一次出现的索引。输出为 3。

如果在数组中未找到该元素，`lastIndexOf()` 返回 -1。

## 第 4 小时

### Math 方法

### Ceil() & Floor()

```javascript
Math.ceil(number);
Math.floor(number);
```

`Math.ceil(number)` 返回大于或等于给定数字的最小整数。
`Math.floor(number)` 返回小于或等于给定数字的最大整数。

### 示例

```javascript
var num = 9.5;
document.write("Ceiling number is " + Math.ceil(num));
document.write("Flooring number is " + Math.floor(num));
```

(输出: Ceiling number is 10 Flooring number is 9)

### 解释

`Math.ceil(num)` 返回一个大于或等于 9.5 的整数，结果为 10。
`Math.floor(num)` 返回一个小于或等于 9.5 的整数，结果为 9。

### Max() & Min()

```javascript
Math.max(x, y);
Math.min(x, y);
```

`Math.max(x, y)` 返回两个数字之间的较大的一个。
`Math.min(x, y)` 返回两个数字之间的较小的一个。

### 示例

```javascript
var x = 100;
var y = 200;
document.write("Greater number is " + Math.max(x, y));
document.write("Less number is " + Math.min(x, y));
```

(输出: Greater number is 200 Less number is 100)

### 解释

`Math.max(x, y)` 返回 100 和 200 之间的较大的数，结果为 200。
`Math.min(x, y)` 返回 100 和 200 之间的较小的数，结果为 100。

### Math.PI & random()

| 属性/方法 | 说明 |
| --- | --- |
| `Math.PI` | 存储圆周率值的常量 |
| `Math.random()` | 生成一个 0.0 到 1.0 之间的随机数 |

### 示例

```javascript
var pi = Math.PI;
var ran = Math.random();
document.write("The PI value is " + pi);
document.write("The random number is " + ran);
```

(输出: The PI value is 3.141592653589793 The random number is 0.16869328)

### 解释

`Math.PI` 的值为 3.141592653589793。
`Math.random()` 生成一个 0.0 到 1.0 之间的随机数，这里的结果是 0.16869328。

### 日期与时间

JavaScript 经常使用日期和时间来设计网页。在使用日期和时间时，必须先创建一个日期对象。

```javascript
var dateObject = new Date();
```

### 示例

```javascript
var dateObject = new Date();
alert(dateObject);
```

(输出: Sun Apr 12 12:23 UTC 2015)

### 解释

`var dateObject = new Date()` 创建了一个日期对象。
`alert(dateObject)` 显示当前的日期和时间。

注意：要创建日期对象，你可以使用其他变量名，例如：`var now = new Date(); var timeObject = new Date();`。

### 年、月、日

Date 对象具有以下方法：

| 方法 | 说明 |
| --- | --- |
| `getDate()` | 获取日期 (1-31) |
| `getMonth()` | 获取月份 (0-11) |
| `getFullYear()` | 获取年份 (四位数) |
| `getDay()` | 获取星期几 (0-6) |

`getMonth()` 返回从 0（1月）到 11（12月）。

### 示例

```javascript
var now = new Date();
var y = now.getFullYear();
var d = now.getDate();
alert(y + " " + d);
```

(输出: 2015 12)

### 解释

`now.getFullYear()` 返回当前年份。
`now.getDate()` 返回当前日期。

### 时、分、秒

Date 对象具有以下方法：

| 方法 | 说明 |
| --- | --- |
| `getHours()` | 获取小时 (0-23) |
| `getMinutes()` | 获取分钟 (0-59) |
| `getSeconds()` | 获取秒 (0-59) |
| `getTime()` | 获取时间 (毫秒数) |

### 示例

```javascript
var now = new Date();
var h = now.getHours();
var m = now.getMinutes();
var s = now.getSeconds();
alert("Current time is " + h + ":" + m + ":" + s);
```

(输出: Current time is 19:30:28)

### 解释

`getHours()` 返回当前小时。
`getMinutes()` 返回当前的分钟。
`getSeconds()` 返回当前的秒。

### 不同时区

```javascript
getUTCHours();
getTimezoneOffset();
```

`getUTCHours()` 返回格林威治标准时间 (UTC) 的小时。
`getTimezoneOffset()` 返回 UTC 时间与本地时间之间的差值（分钟）。例如，如果你的时间是 GMT+2，将返回 -120。

### 示例

```javascript
var now = new Date();
var utc = now.getUTCHours();
var timezone = now.getTimezoneOffset();
alert(utc + " " + timezone);
```

(输出: 16 -120)

### 解释

`getUTCHours()` 返回 UTC 时间的小时部分。
`getTimezoneOffset()` 返回时区偏移量（分钟）。

### 设置日期和时间

Date 对象具有以下设置方法：

| 方法 | 说明 |
| --- | --- |
| `setDate()` | 设置日期 |
| `setMonth()` | 设置月份 |
| `setFullYear()` | 设置年份 |
| `setHours()` | 设置小时 |
| `setMinutes()` | 设置分钟 |
| `setSeconds()` | 设置秒 |

### 示例

```javascript
var now = new Date();
now.setFullYear(2020);
now.setMonth(11);
now.setDate(25);
alert(now);
```

(输出: Fri Dec 25 2020 ...)

### 解释

使用 `set` 系列方法可以修改日期对象的具体部分。

### 定时函数

```javascript
setTimeout(function, milliseconds);
setInterval(function, milliseconds);
```

`setTimeout()` 在指定毫秒数后执行函数一次。
`setInterval()` 每隔指定毫秒数执行函数一次。

### 示例

```javascript
setTimeout(function() { alert("Hello"); }, 3000);
// 3秒后弹出 "Hello"

setInterval(function() { alert("Hi"); }, 5000);
// 每5秒弹出 "Hi"
```

### 解释

`setTimeout` 用于延迟执行，`setInterval` 用于周期性执行。

## 第 5 小时

### 字符串操作

### 字符串长度

```javascript
string.length;
```

`string.length` 返回字符串的长度（字符数）。

### 示例

```javascript
var str = "JavaScript";
var len = str.length;
document.write(len); // 输出: 10
```

### 解释

`str.length` 返回字符串 "JavaScript" 的长度，即 10。

### 合并字符串

```javascript
string1 + string2;
string.concat(string2);
```

使用 `+` 运算符或 `concat()` 方法可以合并字符串。

### 示例

```javascript
var str1 = "Hello";
var str2 = "World";
var result = str1 + " " + str2;
document.write(result); // 输出: Hello World
```

### 解释

`str1 + " " + str2` 将三个字符串合并为 "Hello World"。

### 搜索字符

```javascript
string.indexOf(searchValue);
string.lastIndexOf(searchValue);
```

`indexOf()` 返回指定字符首次出现的索引。
`lastIndexOf()` 返回指定字符最后一次出现的索引。

### 示例

```javascript
var str = "JavaScript";
var pos = str.indexOf("S");
document.write(pos); // 输出: 4
```

### 解释

`str.indexOf("S")` 返回 "S" 首次出现的位置 4（索引从 0 开始）。

### 转换字符大小写

```javascript
string.toUpperCase();
string.toLowerCase();
```

`toUpperCase()` 将字符串转换为大写。
`toLowerCase()` 将字符串转换为小写。

### 示例

```javascript
var str = "JavaScript";
document.write(str.toUpperCase()); // 输出: JAVASCRIPT
document.write(str.toLowerCase()); // 输出: javascript
```

### 解释

`toUpperCase()` 和 `toLowerCase()` 分别返回转换大小写后的新字符串。

### 将字符串转换为数组

```javascript
string.split(separator);
```

`split()` 方法将字符串分割为字符串数组。

### 示例

```javascript
var str = "a,b,c";
var arr = str.split(",");
document.write(arr[1]); // 输出: b
```

### 解释

`str.split(",")` 以逗号为分隔符将字符串分割为数组 `["a", "b", "c"]`。

### 提取子字符串

```javascript
string.substr(start, length);
string.substring(start, end);
string.slice(start, end);
```

`substr(start, length)` 从 `start` 位置提取 `length` 个字符。
`substring(start, end)` 提取从 `start` 到 `end-1` 的字符。
`slice(start, end)` 功能类似 `substring`，但支持负数索引。

### 示例

```javascript
var mystring = "JavaScript is easy.";
var sub = mystring.substr(4, 6);
alert(sub); // 输出: Script
```

### 解释

`mystring.substr(4, 6)` 从 `mystring` 中提取一个子字符串。
`(4, 6)` 指定子字符串的起始位置为 4，长度为 6。
注意字符串索引从零开始。

### 将数字转换为字符串

```javascript
number.toString();
String(number);
```

为了满足 JS 编程的需求，有时需要将数字转换为字符串数据类型。

### 示例

```javascript
var num1 = 12;
var num2 = 68;
var str1 = num1.toString();
var str2 = num2.toString();
var sum = str1 + str2;
document.write(sum); // 输出: 1268
```

### 解释

`num1.toString()` 和 `num2.toString()` 将两个数字转换为字符串数据类型。因此，`str1` 加上 `str2` 的结果是 "1268"，而不是 80。

### 将字符串转换为数字

```javascript
parseInt(string);
parseFloat(string);
Number(string);
```

`parseInt(string)` 和 `parseFloat(string)` 可以将字符串转换为整数或浮点数。

### 示例

```javascript
var str1 = "12";
var str2 = "68";
var sum = str1 + str2;
alert(sum); // 输出: 1268
var num1 = parseInt(str1);
var num2 = parseInt(str2);
var addition = num1 + num2;
alert(addition); // 输出: 80
```

### 解释

`parseInt(str1)` 和 `parseInt(str2)` 将两个字符串转换为数字数据类型。因此，`num1` 加上 `num2` 的结果是 80，而不是 "1268"。

### 搜索特定文本 (1)

```javascript
string.indexOf(searchString);
```

`indexOf()` 可以找到特定文本在字符串中首次出现的位置。

### 示例

```javascript
var mystring = "Please find where find word occurs!";
var place = mystring.indexOf("find");
alert(place); // 输出: 7
```

### 解释

`mystring.indexOf("find")` 返回 "find" 在 `mystring` 中第一次出现的位置。输出为 7。
字符索引从零开始。
如果在字符串中未找到该文本，`indexOf()` 返回 -1。

### 搜索特定文本 (2)

```javascript
string.lastIndexOf(searchString);
```

`lastIndexOf()` 可以找到特定文本在字符串中最后一次出现的位置。

### 示例

```javascript
var mystring = "Please find where find word occurs!";
var place = mystring.lastIndexOf("find");
alert(place); // 输出: 18
```

### 解释

`mystring.lastIndexOf("find")` 返回 "find" 在 `mystring` 中最后一次出现的位置。输出为 18。
字符索引从零开始。
如果在字符串中未找到该文本，`lastIndexOf()` 返回 -1。

## 第 6 小时

### 对象

### 对象声明

对象指的是一个具体的某物。例如：汽车、书、狗、房子等……

```javascript
var obj = new Object();
obj.property;
```

`obj = new Object()` 创建了一个名为 `obj` 的新对象。
`obj.property` 意味着对象的属性。

### 示例

```javascript
var house = new Object();
house.color = "white";
house.size = "big";
document.write("House color: " + house.color + "\n");
document.write("House size: " + house.size + "\n");
```

(输出: House color: white House size: big)

### 解释

`house = new Object()` 创建了名为 `house` 的对象。
`house.color` 意味着房子的颜色。
`house.size` 意味着房子的尺寸。

### 页面导航

```javascript
window.history.back();
window.history.forward();
```

`back()` 用于导航到上一页。
`forward()` 用于导航到下一页。

### 示例

```javascript
window.history.back();
```

(输出: Previous page.)

```javascript
window.history.forward();
```

(输出: Next page.)

### 解释

`back()` 回到上一页。
`forward()` 前往下一页。
`window.history.method()` 用于导航到指定的页面。该方法通常由页面上的按钮调用。

### 跳转到指定页面

```javascript
window.history.go(number);
```

`window.history.go(number)` 可以跳转到指定的页面。

### 示例

```javascript
window.history.go(1);
```

(输出: Next page.)

```javascript
window.history.go(-1);
```

(输出: Previous page.)

```javascript
window.history.go(0);
```

(输出: 刷新当前页)

### 解释

`window.history.go(number)` 可以跳转到指定的页面。该方法通常由页面上的按钮调用。

### 打开窗口

```javascript
window.open(url, name, specs);
```

`window.open` 可以打开一个新窗口。
`url` 指定要打开的 URL。
`name` 指定窗口的名称。
`specs` 指定窗口的参数（如宽度、高度等）。

### 示例

```javascript
window.open("https://example.com", "myWindow", "width=500,height=600");
```

### 解释

`window.open` 打开一个名为 `myWindow` 的窗口，宽度 500px，高度 600px。

### 确认框

```javascript
confirm(message);
```

`confirm()` 显示一个带有“确定”和“取消”按钮的对话框。

### 示例

```javascript
var result = confirm("Are you sure?");
if (result) {
  alert("You clicked OK");
} else {
  alert("You clicked Cancel");
}
```

### 解释

用户点击“确定”返回 `true`，点击“取消”返回 `false`。

### 提示输入

```javascript
prompt(message, defaultValue);
```

`prompt()` 显示一个提示用户输入的对话框。

### 示例

```javascript
var name = prompt("Please enter your name:", "Guest");
alert("Hello " + name);
```

### 解释

用户输入内容后点击“确定”返回输入值，点击“取消”返回 `null`。

### 通过 ID 定位元素

```javascript
document.getElementById(id);
```

`getElementById()` 通过元素的 ID 返回对该元素的引用。

### 示例

```javascript
var element = document.getElementById("myDiv");
element.style.color = "red";
```

### 解释

获取 ID 为 `myDiv` 的元素并修改其样式。

### 通过标签名定位元素

```javascript
document.getElementsByTagName(tagName);
```

`getElementsByTagName()` 返回带有指定标签名的所有元素的集合。

### 示例

```javascript
var paragraphs = document.getElementsByTagName("p");
for (var i = 0; i < paragraphs.length; i++) {
  paragraphs[i].style.color = "blue";
}
```

### 解释

获取所有 `<p>` 标签元素并修改其颜色。

### break 语句

`break` 命令在循环或 `switch` 语句内部工作。

```javascript
break;
```

`break` 关键字用于跳出循环或 `switch` 语句。

### 示例

```javascript
var num = 0;
while (num < 10) {
  if (num == 5) break;
  num++;
}
document.write(num); // 输出: 5
```

### 解释

`if (num == 5) break;` 是一个 `break` 语句。如果 `num` 是 5，程序将运行 `break` 命令，`break` 语句将退出循环，然后运行 `document.write(num)`。

### continue 语句

`continue` 命令在循环内部工作。

```javascript
continue;
```

`continue` 关键字用于停止当前的迭代，忽略后续代码，然后继续下一次循环。

### 示例

```javascript
var num = 0;
while (num < 10) {
  num++;
  if (num == 5) continue;
  document.write(num);
}
```

(输出: 1234678910)

### 解释

注意输出结果没有 5。
`if (num == 5) continue;` 意味着：当 `num` 为 5 时，程序将运行 `continue` 命令，跳过下一个命令 `document.write(num)`，然后继续下一次循环。

## 第 7 小时

### 事件

### HTML 基础

当我们检查网页的源代码时，会发现一些 HTML 元素或标签，它们看起来如下：

### 示例

```html
<html>
<head>
<title>...</title>
</head>
<body>
<form>...</form>
</body>
</html>
```

### 解释

`<html>...</html>` 定义网页文档。
`<head>...</head>` 定义网页的头部。
`<title>...</title>` 定义网页的标题。
`<body>...</body>` 定义网页的主体部分。
`<form>...</form>` 定义一个表单，该表单用于接收来自用户的请求或输入。

### 点击事件

当用户点击网页上的某个元素时，会发生 `click`（点击）事件。

```javascript
onclick = function();
```

`onclick = function()` 意味着当点击元素时，函数会立即执行。

### 示例

```html
<form>
<input type="button" value="Previous" onclick="history.back()">
</form>
```

(返回：上一个网页。)

### 解释

`<form>` 和 `</form>` 是 HTML 标签，位于网页中，`form` 用于接收用户的请求。
`<input type="button" value="Previous"...>` 在表单中定义了一个按钮，按钮上带有“Previous”（上一个）文本。
`onclick="history.back()"` 意味着当点击按钮时，立即运行 `history.back()`，然后返回上一个网页。

### 加载完成事件

当网页完全加载完成时，会发生 `onload`（加载完成）事件。

```javascript
onload = function();
```

`onload = function()` 意味着当网页加载完成后，`function()` 立即执行。

### 示例

```html
<html>
<body onload="alert('Welcome to my page!')">
.....
</body>
</html>
```

### 解释

`<html>` 和 `</html>` 是 HTML 标签，定义了网页的主体。
`<body>` 和 `</body>` 定义网页的主体。
`onload="alert()"` 意味着当网页加载时，`alert()` 立即运行，并显示消息“Welcome to my page!”。

### 卸载事件

当网页卸载时，会发生 `unload`（卸载）事件。

```javascript
onunload = function();
```

`onunload = function()` 意味着当网页卸载时，`function()` 立即执行。

### 示例

```html
<html>
<body onunload="confirm('Are you sure?')">
......
</body>
</html>
```

### 解释

`<html>` 和 `</html>` 是 HTML 标签，定义了一个网页。
`<body>` 和 `</body>` 定义网页的主体。
`onunload="confirm()"` 意味着当网页卸载时，`confirm()` 立即运行，并显示消息“Are you sure?”。

### 鼠标悬入事件

当鼠标指针移动到元素上方时，会发生 `mouseover`（鼠标悬入）事件。

```javascript
onmouseover = function();
```

`onmouseover = function()` 意味着当鼠标指针移动到元素上方时，`function()` 立即执行。

### 示例

```html
<body>
<img src="myphoto.jpg" onmouseover="alert('Please view the photo.')">
</body>
```

### 解释

`<img>` 是用于定义图片的标签。
`src="myphoto.jpg"` 指定了网页中显示的图片“myphoto.jpg”。
`onmouseover="alert()"` 鼠标指针移动到图片上，`alert()` 立即运行，并显示消息“Please view the photo”。

### 鼠标移出事件

当鼠标指针移出元素范围时，会发生 `mouseout`（鼠标移出）事件。

```javascript
onmouseout = function();
```

`onmouseout = function()` 意味着当鼠标指针移出元素时，`function()` 立即执行。

### 示例

```html
<body>
<img src="myphoto.jpg" onmouseout="alert('See you!')">
</body>
```

### 解释

`<img>` 是定义图片的标签。
`src="myphoto.jpg"` 指定了网页中显示的图片“myphoto.jpg”。
`onmouseout="alert()"` 意味着当鼠标指针移出元素时，`alert()` 运行。

### 按键按下事件

当按键按下时，会发生 `keydown` 事件。

```javascript
onkeydown = function();
```

`onkeydown = function()` 意味着当按键按下时，`function()` 立即执行。

### 示例

```html
<body>
<input type="text" onkeydown="alert('Key down!')">
</body>
```

### 解释

`<input type="text">` 定义一个文本输入框。`onkeydown="function()"` 意味着当按键按下时，`function()` 运行。

### 按键释放事件

当按键释放时，会发生 `keyup` 事件。

```javascript
onkeyup = function();
```

`onkeyup = function()` 意味着当按键释放时，`function()` 立即执行。

### 示例

```html
<body>
<input type="text" onkeyup="keyUpFunction()">
</body>
<script>
function keyUpFunction() {
  alert("You released a key.");
}
</script>
```

### 解释

网页中的输入字段如下：`onkeyup="function()"` 意味着当按键释放时，`function()` 运行。

### 聚焦事件

当用户将光标置于元素时，会发生 `focus`（聚焦）事件。

```javascript
onfocus = function();
```

`onfocus = function()` 意味着当点击（聚焦）元素时，函数会立即执行。

### 示例

```html
<body>
<input type="text" onfocus="focusFunction()">
</body>
<script>
function focusFunction() {
  confirm("Are you ready to input?");
}
</script>
```

### 解释

`onfocus="function()"` 意味着当用户将光标置于字段时，`function()` 立即执行。

### 失去聚焦事件

当用户将光标移出元素时，会发生 `blur`（失去聚焦）事件。

```javascript
onblur = function();
```

`onblur = function()` 意味着当用户将光标移出元素时，`function()` 立即执行。

### 示例

```html
<body>
<input type="text" onblur="blurFunction()">
</body>
<script>
function blurFunction() {
  confirm("Are you sure to leave?");
}
</script>
```

### 解释

`onblur="function()"` 意味着当用户将光标移出字段时，`function()` 立即执行。

## 第 8 小时

### 表单操作

### 表单基础

HTML 中的 `form` 元素是一个非常重要的元素，用于接收用户的请求或输入。

### 示例

```html
<form id="myform" method="get" action="f.php">
<input id="txt" type="text">
<input id="pas" type="password">
<input id="rad" type="radio" value="val2">
<input id="chb" type="checkbox" value="val3">
<input id="sub" type="submit" value="OK">
<input id="rst" type="reset" value="Cancel">
</form>
```

### 解释

`id` 意味着元素的名称。
`method="get/post"` 意味着通过 `get` 或 `post` 发送数据。
`get` 方法公开发送链接数据，数量较少。
`post` 方法秘密发送数据，数量较多。
`action="f.php"` 意味着数据将由 `f.php` 处理。
`type` 指定元素的类型。

### 访问表单属性

`document.forms` 对象可以访问表单属性。

```javascript
document.forms.formId.attribute
```

`document.forms.formId.attribute` 可以访问表单中的属性。

### 示例（参考上一页的表单）

```javascript
var message1 = document.forms.myform.method;
var message2 = document.forms.myform.action;
document.write(message1);
document.write(message2);
```

(输出: get f.php)

### 解释

`document.forms.myform.method` 可以访问 `myform` 中的 `method`，结果为 `get`。
`document.forms.myform.action` 可以访问 `myform` 中的 `action`，结果为 `f.php`。

### 赋值文本值

```javascript
document.forms.formId.elementId.value = "newValue";
```

`document.forms.formId.elementId.value = "newValue"` 可以给元素赋值一个新值。

### 示例（参考上一页的表单）

```javascript
document.forms.myform.txt.value = "Hello World!";
document.forms.myform.txt.style.fontFamily = "Arial";
document.forms.myform.txt.style.fontSize = "16pt";
document.forms.myform.txt.style.color = "blue";
document.forms.myform.txt.style.background = "yellow";
```

(输出: Hello World!)

### 解释

`myform` 是表单的 `id`。
`txt` 是“文本字段”的 `id`。
`value = "Hello World!"` 给文本字段赋值一个新值。
`style.fontFamily = "Arial"` 设置字体族。
`style.fontSize = "16pt"` 设置字体大小。
`style.color = "blue"` 设置字体颜色。
`style.background = "yellow"` 设置背景颜色。

### 重置方法

```javascript
formElement.reset();
```

`reset()` 用于清空表单数据。

### 示例

```html
<form id="myform" method="get" action="f.php">
......
<input type="button" onclick="myFunction()" value="Clear">
</form>
<script>
function myFunction() {
  document.getElementById("myform").reset();
}
</script>
```

(结果：表单数据被完全清空。)

### 解释

`onclick="myFunction()"` 意味着当点击按钮时，`myFunction()` 立即执行。
`getElementById("myform")` 通过其 `id` 访问 `myform`。
`reset()` 清空 `myform` 的数据。

### 提交方法

```javascript
formElement.submit();
```

`submit()` 用于将表单数据提交到服务器。

### 示例

```html
<form id="myform" method="get" action="f.php">
......
<input type="button" onclick="myFunction()" value="Submit">
</form>
<script>
function myFunction() {
  document.getElementById("myform").submit();
}
</script>
```

(结果：表单数据已提交到服务器。)

### 解释

`onclick="myFunction()"` 意味着当点击按钮时，`myFunction()` 立即执行。
`getElementById("myform")` 通过其 `id` 访问 `myform`。
`submit()` 将 `myform` 数据提交到服务器。

### “Select”选择框

```html
<select id="myId" onchange="function()">
```

当表单中的 `select` 值发生变化时，会触发 `onchange` 事件并立即运行 `function()`。

### 示例

```html
<select id="mySelect" onchange="myFunction()">
<option value="Red">Red</option>
<option value="Blue">Blue</option>
<option value="Pink">Pink</option>
</select>
<script type="text/javascript">
function myFunction() {
  var v = document.getElementById("mySelect").value;
  alert("You selected: " + v); // 例如：选择 Pink
}
</script>
```

(输出：You selected: Pink)

### 解释

`getElementById("mySelect")` 通过其 `id` 访问 `mySelect`。
`getElementById("mySelect").value` 意味着获取一个值。

### “Radio”单选框

```html
<input type="radio" name="groupName" id="myId" value="">
```

单选按钮组允许用户随时勾选并提交选中值（同一 `name` 下互斥）。

### 示例

```html
<input type="radio" name="color" value="Red"> Red
<input type="radio" name="color" value="Blue"> Blue
<input type="radio" name="color" value="Pink"> Pink
<input type="button" value="submit" onclick="myFunc()">
<script>
function myFunc() {
  var radios = document.getElementsByName("color");
  var selectedValue;
  for (var i = 0; i < radios.length; i++) {
    if (radios[i].checked) {
      selectedValue = radios[i].value;
      break;
    }
  }
  alert(selectedValue); // 例如：选择 Blue
}
</script>
```

(输出：Blue)

### 解释

`getElementsByName("color")` 获取同名单选组。
遍历检查 `checked` 属性以获取选中值。

### “Checkbox”复选框

```html
<input type="checkbox" name="groupName" id="myId" value="">
```

复选框组允许用户随时勾选多个框并提交。

### 示例

```html
<input type="checkbox" name="color" value="Red"> Red
<input type="checkbox" name="color" value="Blue"> Blue
<input type="checkbox" name="color" value="Pink"> Pink
<input type="button" value="submit" onclick="myFunc()">
<script>
function myFunc() {
  var checkboxes = document.getElementsByName("color");
  var values = [];
  for (var i = 0; i < checkboxes.length; i++) {
    if (checkboxes[i].checked) {
      values.push(checkboxes[i].value);
    }
  }
  alert(values.join(", "));
}
</script>
```

### 解释

`getElementsByName("color")` 获取同名复选框组。
遍历检查 `checked` 属性，收集所有选中值。

## 附录

### HTML 标签复习

| 标签 | 说明 |
| --- | --- |
| `<p>` | 新段落 |
| `<param>` | 添加参数 |
| `<pre>` | 显示包含制表符、空格、换行的文本 |
| `<s>` | 显示带删除线的文本 |
| `<script>` | 包含 JavaScript 代码 |
| `<select>` | 创建选择菜单 |
| `<small>` | 字体比普通字体更小 |
| `<span>` | 为字符设置 CSS 样式 |
| `<strong>` | 加粗显示文本 |
| `<style>` | 包含 CSS 代码 |
| `<table>` | 包含列和行的表格 |
| `<td>` | 定义表格单元格 |
| `<textarea>` | 创建多行文本输入框 |
| `<title>` | HTML 文档的标题 |
| `<tr>` | 定义表格行 |
| `<u>` | 为文本添加下划线 |
| `<ul>` | 包含无序列表的项目 |

### HTML 符号

| 符号 | 源码 |
| --- | --- |
| `<` | `&lt;` |
| `>` | `&gt;` |
| `&` | `&amp;` |
| `"` | `&quot;` |
| `©` | `&copy;` |
| `®` | `&reg;` |
| 空格 | `&nbsp;` |

### CSS 复习

CSS 有 4 种编码方式：

```css
/* (1) 内部样式表 */
<style type="text/css">
tag { attribute: value; }
tag.class { attribute: value; }
tag#id { attribute: value; }
.class { attribute: value; }
#id { attribute: value; }
</style>
```

```html
<!-- (2) 内联样式 -->
<tag style="attribute: value">......</tag>
```

```html
<!-- (3) 外部样式表 -->
<link rel="stylesheet" title="My Style" type="text/css" href="myfile.css">
```

```css
/* (4) @import 导入 */
@import url("external/myfile.css");
```

时光飞得真快！是时候告别了。

查看 Ray Yao 的书籍：

- Linux 命令行
- JAVA 面试 100 题
- PHP 面试 100 题
- 8 小时精通 JAVA
- 8 小时精通 PHP
- 8 小时精通 JavaScript
- 8 小时精通 C++
- Ray Yao 系列书籍

# 结语

我的朋友，

如果你能为这本书写下好评，我将不胜感激。非常感谢你的支持！

此致

顺颂商祺

Ray

我的朋友，再见！
