
# JavaScript 入门指南：使用逻辑、DHTML 和 AJAX 创建动态网页

全彩印刷

# JavaScript 术语

- **脚本块 (Script block)**：HTML `<script>` 和 `</script>` 标签之间所有的 JavaScript 代码和注释
- **变量 (Variable)**：JavaScript 代码中用于存储数据的容器，存储数字、文本字符串、字符或布尔值（真/假）
- **初始化 (Initialize)**：为 JavaScript 变量分配初始值——可以在声明时赋值，也可以在随后的脚本中赋值
- **调用 (Call)**：通过在脚本中引用函数名来执行 JavaScript 函数
- **函数 (Function)**：在脚本块中定义一次的 JavaScript 代码段，可以被调用多次
- **参数 (Argument)**：调用者传递给函数的值，用于执行要运行的代码
- **表达式 (Expression)**：将变量或字面量与一个或多个 JavaScript 运算符结合产生结果的代码
- **语句 (Statement)**：单一完整的 JavaScript 指令，始终以分号结束
- **语句块 (Statement block)**：当函数被调用时要执行的 JavaScript 语句
- **for 循环 (For loop)**：按指定次数重复执行某些 JavaScript 代码的语句
- **while 循环 (While loop)**：只要满足测试条件，就重复执行 JavaScript 代码的语句
- **条件分支 (Conditional branching)**：只有在满足测试条件时才执行某段代码，否则执行另一段代码的语句
- **多路分支 (Multi-way branching)**：评估表达式并执行与该结果相关的代码或默认代码的语句
- **返回 (Return)**：JavaScript 函数中执行的语句的最终结果，并将其传回调用者
- **DHTML**：动态 HTML（Dynamic HTML）的缩写——使用 JavaScript 操作 HTML 元素的大小、位置和外观的技术
- **AJAX**：异步 JavaScript 与 XML（Asynchronous JavaScript And XML）的缩写——使用 JavaScript 配合其他技术实现网页组件动态更新的技术

访问 `www.ineasystems.com` 下载书中示例的源码并获取任何重要的更新。

我们已尽力确保本书包含准确的当前信息。然而，对于读者因使用本文包含的任何信息而遭受的任何损失或损害，Computer Step 和作者概不承担责任。

# 6 数学运算

本章专注于 JavaScript 的 `Math` 对象，并描述了可用的常量和方法。

- 70 个 Math 常量
- 72 个 Math 方法
- 73 比较数字
- 74 浮点数舍入
- 76 生成随机数
- 78 总结

## Math 常量

内置的 JavaScript 对象包含若干标准数学常量值，方便引用。

始终使用大写字母来引用常量值，它们都列在下表中：

| 常量 | 说明 |
| :--- | :--- |
| `Math.E` | 常数 e，自然对数的底，值约为 2.71828 |
| `Math.LN2` | 2 的自然对数，约为 0.6931471805994528623 |
| `Math.LN10` | 10 的自然对数，约为 2.302585092994049011 |
| `Math.LOG2E` | e 的以 2 为底数，约为 1.442695040888963387 |
| `Math.LOG10E` | e 的以 10 为底数，约为 0.4342944819032518677 |
| `Math.PI` | 常数 pi，约为 3.14159265358979 |
| `Math.SQRT1_2` | 2 的平方根的倒数，约为 0.707106781186547 |
| `Math.SQRT2` | 2 的平方根，约为 1.414213562373095 |

`Math` 常量可以在脚本的任何地方使用。大多数 `Math` 常量仅用于具有特定数学目的 JavaScript 应用程序，但上方列出列表是为了完整性。

示例中使用了 `Math.PI` 常量来根据给定的半径计算圆的周长和面积。

```javascript
// 请求用户输入半径大小
var rad = prompt("Please enter radius size...");
// 使用 πr² 计算圆面积
var area = Math.PI * (rad * rad);

// 使用 2πr 计算周长
var circ = 2 * (Math.PI * rad);

// 显示结果
alert("Area: " + area + "\nCircumference: " + circ);
```

## Math 方法

JavaScript `Math` 对象有很多方法。所有方法都列在下表中：

| 方法 | 说明 |
| :--- | :--- |
| `Math.abs()` | 返回绝对值 |
| `Math.acos()` | 返回反余弦 |
| `Math.asin()` | 返回反正弦 |
| `Math.atan()` | 返回反正切 |
| `Math.atan2()` | 返回来自 X 轴位置的角度 |
| `Math.ceil()` | 向上取整数字 |
| `Math.cos()` | 返回余弦值 |
| `Math.exp()` | 返回常数的指数 |
| `Math.floor()` | 向下取整数字 |
| `Math.log()` | 返回自然对数 |
| `Math.max()` | 返回两个数字中的较大者 |
| `Math.min()` | 返回两个数字中的较小者 |
| `Math.pow()` | 返回幂值 |
| `Math.random()` | 返回随机数 |
| `Math.round()` | 四舍五入到整数 |
| `Math.sin()` | 返回正弦值 |
| `Math.sqrt()` | 返回平方根 |
| `Math.tan()` | 返回正切值 |

上述列表中最常用的 `Math` 方法将在接下来的页面中进行详细介绍。

## 比较数字

`Math` 对象有两个方法可以比较两个数字并返回较大或较小的值。

`Math.max()` 接受两个用于比较的值并将返回两者中的较大值。

`Math.min()` 方法的工作方式相同，但返回给定值中的较小值。

在示例中，`Math.pow()` 方法被用来创建平方和立方值，然后与 `Math.max()` 和 `Math.min()` 进行比较。`Math.pow()` 方法需要两个参数来指定数字和它的幂次数：

```javascript
var sq = Math.pow(2, 2);
var cube = Math.pow(2, 3);
var max = Math.max(sq, cube); // 8
var min = Math.min(sq, cube); // 4
```

## 浮点数舍入

`Math.round()` 方法将数字四舍五入到最近的整数。

`Math.ceil()` 方法将数字向上取整。

`Math.floor()` 方法将数字向下取整。

下面的示例显示了这些方法的用法：

```javascript
var x = 7.1;
alert(Math.round(x)); // 7
alert(Math.ceil(x));  // 8
alert(Math.floor(x)); // 7

var y = 7.9;
alert(Math.round(y)); // 8
alert(Math.ceil(y));  // 8
alert(Math.floor(y)); // 7

var z = 7.5;
alert(Math.round(z)); // 8
alert(Math.ceil(z));  // 8
alert(Math.floor(z)); // 7
```

## 生成随机数

`Math.random()` 方法返回一个 0（包含）到 1（不包含）之间的随机浮点数。

要生成指定范围内的随机整数，通常将其乘以范围并使用 `Math.floor()`。

```javascript
// 生成 0 到 9 之间的随机整数
var rand = Math.floor(Math.random() * 10);

// 生成 1 到 10 之间的随机整数
var rand1 = Math.floor(Math.random() * 10) + 1;

// 生成 1 到 100 之间的随机整数
var rand2 = Math.floor(Math.random() * 100) + 1;
```

此示例使用 `Math.random()` 生成一组 1 到 49 之间的六个随机数，这些可以作为抽票中的选择：

```javascript
// 创建变量
var i, rand, temp, str;

// 创建一个包含 50 个元素的新数组
var nums = new Array(50);
// 用数字 1-49 填充元素 1-49
for(i = 1; i < 50; i++) nums[i] = i;

// 随机化这些数字的算法
for(i = 1; i < 50; i++) {
  rand = Math.ceil(Math.random() * 49);
  temp = nums[i];
  nums[i] = nums[rand];
  nums[rand] = temp;
}

// 将前六元素添加到字符串中
str = "您的六个幸运数字是：\n\n"
for(i = 1; i < 7; i++) {
  str += nums[i];
  if(i != 6) str += " -";
}

// 显示字符串
alert(str);
```

## 总结

- JavaScript 包含一系列常量，方便引用常用的数学常值，例如使用 `Math.PI` 的 pi 值
- 常量名称始终使用大写字母
- 内置的 `Math` 对象提供了执行数学运算的方法，例如使用 `Math.sqrt()` 计算平方根
- `Math.max()` 和 `Math.min()` 方法用于比较两个数字并返回较大或较小的值
- 使用 `Math.pow()` 可以轻松地计算幂值
- 浮点数可以使用 `Math.round()` 方法四舍五入到最近的整数
- `Math.round()` 方法也可以用于将长浮点数转换为保留两位小数
- 可以使用 `Math.ceil()` 方法对数字进行特定的向上舍入，或者使用 `Math.floor()` 进行特定的向下舍入
- `Math.random()` 方法返回一个 0.0 到 1.0 之间的浮点值
- 将 `Math.random()` 返回的值相乘，创建一个 0 到 n 范围内的随机数
- 使用 `Math.ceil()` 方法将随机值向上舍入，提供 1 到 n 范围内的整数

# 7 处理字符串

本章解释了字符串的特征，并通过示例演示了如何使用 JavaScript 代码处理文本字符串。

- 80 计算字符串长度
- 81 合并字符串
- 82 查找字符
- 83 改变大小
- 84 拆分字符串
- 85 创建子字符串
- 86 转换为字符串
- 87 发现 Unicode 值
- 88 提取字符串数字
- 89 在字符串中插入变量
- 90 总结

## 计算字符串长度

JavaScript 中的字符串简单来说是在引号内的零或多个字符，这些都是字符串：

```javascript
var str1 = "My First String";
var str2 = "";
var str3 = "2";
var str4 = "null";
```

`str2` 中的空引号定义该变量为字符串类型，无论字符串值是什么。赋值给 `str3` 的数值在包含在引号内会自动转换为字符串类型，而 JavaScript 的 `null` 关键字在包含在引号内只是一个字符串字面量。

> **不要忘记** 空格也被视为一个字符。

本质上，字符串是字符的集合，每个字符都包含自己的数据，就像定义数组中的元素一样。将字符串视为字符数组并在使用字符串时应用数组特性是符合逻辑的。

下面的示例将 `Array.length` 属性与 `String.length` 属性并列对比：

```javascript
// 创建并初始化字符串变量
var a = "JavaScript Strings";

// 显示字符串的长度
alert("String length is " + a.length);
```

## 合并字符串

`+` 运算符用于拼接字符串，并在本书提供的示例代码中被广泛使用。会创建一个新字符串，它由第一个字符串紧随第二个字符串组成。

下面的示例将多个变量值合并到一个字符串中，无论它们原始的数据类型如何——因为 JavaScript 执行了自动的数据类型转换：

```javascript
// 创建并初始化一个整数变量
var num = 99;

// 创建并初始化一个浮点数变量
var flt = 98.6;

// 创建并初始化一个布尔变量
var bool = true;

// 创建并初始化几个字符串变量
var str1 = "Although ";
var str2 = " F is cited as body temperature";
var str3 = "\nthe ";
var str4 = " range is from about 97 to ";
var str5 = " F.";

// 显示拼接后的字符串
alert(str1 + flt + str3 + str4 + num + str5);
```

> **不要忘记** 空格也被计为一个字符

## 查找字符

字符串就像是数组，其字符可以以数组的方式被找到。使用 `charAt()` 方法查找字符，该方法接收索引作为唯一参数。

下面的示例演示了如何通过这种方式来查找字符：

```javascript
// 创建并初始化字符串变量
var str = "abcdefghij", newstr = "";

// 获取字符串的第一个字符
var a = "First : " + str.charAt(0);
var z = "";

// 遍历字符串每个字符并复制到 newstr
for(var i = 0; i < str.length; i++) {
    if (str.charAt(i) != " ") newstr += str.charAt(i);
    else newstr += " ";
}

// 显示 newstr 和最后一个字符
var result = "STRINGS\n";
result += "New : " + a + "\n";
alert(result + z);
```

## 改变大小

字符串的大小写可以使用 `toUpperCase()` 或 `toLowerCase()` 方法来强制转换为大写或小写。这些方法在比较用户输入时非常有用。

在下面的示例中，当用户点击按钮时转换字符串的大小写：

```html
<input type="button" value="Check Input" onclick="check_input()">
```

```javascript
function check_input() {
  // 从表单获取输入
  var entry = document.forms[0].textfield.value;

  // 比较输入并显示相应消息
  if(entry.toLowerCase() == "castle")
    alert("Accepted");
  else alert("Refused");
}
```

> **不要忘记** 在使用这些方法时确保观察大小写正确。

## 拆分字符串

字符串的内容可以使用 JavaScript 的 `split()` 方法进行拆分。

单个参数应指定一个字符作为分隔符，以定义字符串拆分的位置。最常见的是空格字符，将具有正常间的短语拆分成单词数组。每个单词都可以使用拆分字符串数组的索引号进行引用，与其他数组一样。

下面的示例说明了 `split()` 方法的另一个用法，数据库中的项可能使用 `|` 管道字符作为分隔符：

```javascript
// 创建并初始化字符串变量
var str = "JavaScript in easy steps";

// 按空格拆分为数组元素
var ss = str.split(" ");

// 创建并初始化另一个字符串变量
var bk = "JavaScript in easy steps|Mike McGrath";
// 按管道符拆分为数组元素
var bks = bk.split("|");

// 显示一些元素
var res = "Topic : " + ss[0];
res += "\nTitle : " + bks[0];
res += "\nAuthor : " + bks[1];
alert(res);
```

> **热提示** 数据通常以逗号分隔的字符串形式存储。

## 创建子字符串

可以使用 `String.substring()` 方法从现有字符串中提取子字符串，该方法需要两个参数来指定所需子字符串在主字符串中的起始和结束位置。

起始位置的字符将是返回子字符串的第一个字符。子字符串的最后一个字符将是给定参数位置的前一个字符。

从字符串中提取子字符串的另一种方法是使用 `String.substr()` 方法，同样需要两个参数。第一个参数指定子字符串的起始位置，第二个参数指定要返回的子字符串的长度。

`substr()` 方法通常更容易使用。

下面的示例演示了两种子字符串方法：

```javascript
// create and initialize a string variable
var str = "JavaScript in easy steps";

// get two substrings with the substring() method
var sub1 = str.substring(14,19) + str.substring(0,11);

// get two substrings with the substr() method
var sub2 = str.substr(14,5) + str.substr(0,10);

// display all the substrings
var res = "Substr method : " +sub1;
res += "\nSubstr method : " +sub2;
alert(res);
```

## 转换为字符串

通过调用 `Object.toString()` 方法，可以手动调用将其他数据类型转换为字符串的 JavaScript 函数。这是一个非常有用的 JavaScript 函数，旨在返回所查询对象的字符串表示，即使该对象本身不是字符串。

在这个示例中，首先是两个整数的简单加法，然后是字符串与整数的拼接，其中整数被转换为字符串值。最后，通过不同的数据类型演示了 `Object.toString()` 方法，以说明生成的输出将揭示对象的类型。

```javascript
// create an integer variable and add another integer
var num = 9;
var nostr = num + 9;

// create a string version of the num integer variable
// then concatenate a second value to it
var adstr = num.toString() + 9;

// create a new Image object
var img = new Image();

// display string values of the variables
var res = "No strings : " + nostr;
res += "\nAdded strings : " + adstr;
res += "\nImage : " + img.toString();
alert(res);
```

`toString()` 方法可以用于 JavaScript 中的任何地方，揭示任何对象的字符串信息。

## 发现 Unicode 值

可以使用 `String.charCodeAt()` 方法返回字符串中每个单独字符的 Unicode 值。该方法需要字符在字符串中的索引作为参数。相反，可以使用 JavaScript `String.fromCharCode()` 函数从 Unicode 获取字符，该函数将 Unicode 值作为参数。

下面的示例首先遍历字符串，并将其 Unicode 字符值创建一个用逗号分隔的字符串。创建了一个包含这些 Unicode 数值的数组，用于第二个循环，以返回每个数字对应的字符：

```javascript
// create and initialize three strings
var str = "Code Fun", enc = "", unc = "";

// get the String numbers, comma delimited
for(var i = 0; i < str.length; i++) {
  enc += str.charCodeAt(i) + ",";
}

// split the list of the numbers into array elements
var ss = enc.split(",");

// convert the Unicode values back to characters
for(var i = 0; i < ss.length; i++) {
  unc += String.fromCharCode(ss[i]);
}

alert("Encoded : " + enc + "\nUnencoded : " + unc);
```

注意 `fromCharCode` 函数是 `String()` 构造函数的静态方法，而不是字符串对象的实例方法。关于 JavaScript 中对象的更多信息，请参见下一章。

## 提取字符串数字

可以使用 `parseInt()` 和 `parseFloat()` 方法从字符串开头提取数字。

`parseInt()` 方法解析字符串并返回找到的第一个整数。`parseFloat()` 方法的工作相同，但返回的是浮点值。

# 8 理解对象

本章演示了如何构建新的自定义对象以及它们如何继承属性和方法。

- 92 构建对象
- 94 继承对象特性
- 96 查询浏览器
- 98 发现已启用的功能
- 100 总结

## 构建对象

访问对象属性和方法的 JavaScript 语法使用对象名后跟点，然后是属性名。例如，`Array.length` 访问数组对象的长度属性。

书中之前的示例代码使用了具有预定义方法的 JavaScript 固有内置对象。

可以使用 JavaScript 的 `new` 关键字配合 `Object()` 构造函数轻松地创建新的自定义对象。

可以通过声明属性名并为其赋值，来为新的自定义对象分配属性。

下面的示例创建了一个名为 `car` 的新对象，然后为它提供了三个带有赋值值的属性：

```javascript
// 创建一个新的 "car" 对象
var car = new Object();

// 创建并初始化 "maker" 属性...
car.maker = "Dodge";
// 创建并初始化 "model" 属性...
car.model = "Viper";
// 创建并初始化 "color" 属性...
car.color = "Silver";
```

要声明属性，请同时使用对象名和给定的属性名。

```javascript
// 显示 car 对象的所有属性...
alert(car.color + " " + car.maker + " " + car.model);
```

方法也可以以与属性非常相似的方式添加到自定义对象中。在调用方法时需要执行的语句应该在普通函数块中使用给定的名称进行定义。然后，可以将该函数的名称赋值给对象，从而创建一个对象方法。

让对象方法与它调用的函数保持相同的名称是合理的。例如，下面的示例为在相反页创建的 `car` 对象添加了一个名为 `startup` 的方法，该方法调用一个同名的函数：

```javascript
// 定义 startup 方法...
function startup() {
  alert("... 引擎现在正在运行!");
}

// 为 car 对象添加方法...
car.startup = startup;

// 调用 car 对象的 startup 方法...
car.startup();
```

**注意：** 注意赋值时不使用末尾的括号——只需函数名。

## 继承对象特性

通过编写一个带有参数的函数来设置其属性值，可以轻松创建自定义构造函数。传递给函数的值可以使用 JavaScript 的 `this` 关键字指定对象属性名来分配给属性。当调用者未指定属性时，可以使用 `||` OR 运算符指定默认值。

下面的示例使用这种技术通过自定义构造函数重新创建了之前的示例。函数调用者只需创建 `car` 对象的实例而不指定任何属性值——因此对象继承了默认值：

```javascript
// 创建一个 car 构造函数
function car(maker, model, color) {
  this.maker = maker || "Dodge";
  this.model = model || "Viper";
  this.color = color || "Silver";
  this.startup = startup;
}

// 定义 startup 函数
function startup() {
  alert("... 引擎现在正在运行!");
}

// 创建 car 对象的实例...
var viper = new car();
alert(viper.color + " " + viper.maker + " " + viper.model);
```

可以通过将其名称作为 `Object()` 构造器的参数来创建上一个示例对象的实例——例如：`var van = new Object(car)`。

可以这样通过调用者参数指定新的属性值来创建另一个 car 对象实例：

```javascript
function car(maker, model, color) {
  this.maker = maker || "Dodge";
  this.model = model || "Viper";
  this.color = color || "Silver";
  this.startup = startup;
}

function startup() {
  alert("... 引擎现在正在运行!");
}

// 创建 car 对象的实例...
var vette = new car("Chevrolet", "Corvette", "Red");

// 显示实例值
alert(vette.color + " " + vette.maker + " " + vette.model);
vette.startup();
```

在此示例中，属性接收了新值——但默认继承自构造函数。

## 查询浏览器

固有 `navigator` 对象具有有关浏览器的属性。浏览器名称由 `navigator.appName` 显示，描述可以通过 `navigator.userAgent` 获取。

除了发行号外，`navigator.userAgent` 属性包含主机平台等详细信息。在下面的示例中，`navigator.userAgent` 属性显示浏览器为在 Windows 平台 (NT5.1) 上运行的 Internet Explorer 7.0 (MSIE 7.0) 和 Firefox 1.5：

```javascript
// 获取浏览器名称
var browser = navigator.appName;

// 获取浏览器描述
var description = navigator.userAgent;

// 显示浏览器名称和版本
alert(browser + "\n" + description);
```

`navigator` 对象的其他属性提供了有关操作系统和浏览器的特定信息。这些属性为特定浏览器定制 JavaScript 应用非常有用。下面的示例使用 `indexOf()` 方法搜索 `navigator.platform` 字符串以识别并生成相应的消息：

```javascript
// 获取操作系统...
var platform;
if(navigator.platform.indexOf("Linux") != -1)
  platform = "Linux";
if(navigator.platform.indexOf("Win") != -1)
  platform = "Windows";

alert("Welcome " + platform + " user\nYour system is: " + navigator.platform + " " + navigator.appCodeName + " " + navigator.appVersion);
```

## 发现已启用的功能

可以使用 `navigator.javaEnabled()` 方法评估浏览器以发现是否启用了 Java。根据结果返回 `true` 或 `false`。如果浏览器中加载了包含 Java 小程序的页面，可以使用 `navigator.javaEnabled()` 方法显示警告：

```javascript
// 测试浏览器中是否启用了 Java
if (!navigator.javaEnabled()) {
  var warning =
  "您的浏览器似乎未启用 Java。\n  此页面上的某些项目在没有 Java 的情况下运行";
  alert(warning);
}
```

Mozilla 浏览器可以使用 `navigator.plugins` 数组显示任何已安装插件的信息。每个插件都作为 `navigator.plugins` 数组中的一个元素添加。例如，如果安装了 Macromedia Shockwave 插件，则有一个 `navigator.plugins["Shockwave Flash"]` 元素。

插件元素有一个 `name` 属性，存储该插件的名称和版本，以及一个包含插件信息的 `description` 属性。

在下面的示例中，循环显示 `navigator.plugins` 数组中的每个 `name` 属性，列出所有已安装的插件：

```javascript
// 列出已安装的 Mozilla 插件...
if(navigator.appName == "Netscape") {
  var str = "";
  for(var i = 0; i < navigator.plugins.length; i++) {
    str += navigator.plugins[i].name + "\n";
  }
  alert(str);
}
```

`navigator.plugins` 在 Internet Explorer 中存在但尚未实现。

## 总结

- 自定义对象可以像内置 JavaScript 对象一样包含属性和方法——就像 `Array` 对象拥有 `Array.length` 属性和 `Array.sort()` 方法一样。
- 使用 JavaScript 的 `new` 关键字配合 `Object` 构造函数来创建一个新对象。
- 通过点号 (`.`) 在对象名后附加其名称来访问属性或方法——例如 `car.color` 和 `car.startup()`。
- 使用 JavaScript 的 `this` 在自定义构造函数中为属性和方法赋值。
- 使用 JavaScript 的 `new` 关键字配合自定义构造函数来创建对象的新实例。
- 对象的实例会自动继承其源自对象的属性和方法。
- `navigator` 对象包含有关网络浏览器的信息。
- 使用 `navigator.appName` 属性显示浏览器名称，或使用 `navigator.userAgent` 显示浏览器的描述、版本及其环境。
- 你可以通过 `navigator.platform` 属性发现用户运行的是什么操作系统。
- 使用 `navigator.javaEnabled()` 方法发现浏览器是否能够执行 Java Applet。
- `navigator.plugins` 属性包含一个包含已插件详情的数组——每个元素代表一个插件。
- 使用 `navigator.plugins` 元素的 `name` 属性显示其名称，或使用该元素的 `description` 属性获取详情。

# 9 探索 window 对象

本章演示了 JavaScript 如何使用 `window` 对象的属性和方法来修改浏览器窗口的不同方面。

- 102 控制位置
- 104 获取显示器设置
- 105 识别帧
- 106 访问帧
- 108 建议状态消息
- 109 滚动与移动
- 110 寻求确认
- 111 提示输入
- 112 打开新窗口
- 114 总结

## 控制位置

`window.location` 对象包含当前在浏览器中加载的文档的完整 URL 地址。

它将完整的 URL 存储在 `window.location.href` 属性中，为该属性赋新值或为 `window.location` 对象本身赋值，会将指定的 URL 加载到浏览器中。

一个典型的 URL 地址可能包含以下部分：

```
protocol://host/pathname?query#hash
```

存储在 `window.location` 对象中的 URL 地址的每个部分都可以使用适当的 `location` 属性单独访问——如示例所示：

```javascript
// 将当前 URL 的每个部分赋值给变量
var locn = "Href : " + window.location.href;
var prot = "Protocol : " + window.location.protocol;
var host = "Host : " + window.location.host;
var path = "Path : " + window.location.pathname;
var hash = "Hash : " + window.location.hash;

// 显示变量值
alert(locn+"\n"+prot+"\n"+host+"\n"+path+"\n"+hash+"\n")
```

> **热点** 为 `location.hash` 赋新值将浏览器跳转到页面中指定的地点。

`window.history` 属性包含一个浏览器会话期间之前访问过的 URL 地址数组。出于安全考虑，这些地址无法直接读取，但它们被用于导航回之前的页面。

`window.history` 对象的 `back()` 和 `forward()` 方法模拟了浏览器的“后退”和“前进”按钮。

`window.history.go()` 方法通常提供更灵活的导航，它接受一个参数来通过相对位置指定目标位置。例如，参数值 `-1` 将返回上一个页面，而值 `-2` 将重新打开在此之前的页面。

同样地，`window.history.go(1)` 会前进到访问过的 URL 历史数组中的下一页。

调用 `window.history.go(0)` 会导致浏览器重新加载当前文档。

示例中的函数将用户带到上一个页面。在这种情况下，该函数是从 HTML 文档中按钮表单单元的 `onclick` 属性调用的。

```javascript
// 加载上一个页面的函数
function go_back() {
  window.history.go(-1);
}
```

## 获取显示器设置

有时让 JavaScript 从 `window.screen` 对象的 `width` 和 `height` 属性获取用户的屏幕分辨率是有用的。你还可以使用 `availWidth` 和 `availHeight` 属性确定排除任务栏后的可用屏幕尺寸。

当前的颜色设置也可以作为存储在 `window.screen.colorDepth` 属性中的每像素位值来获取。

在下面的示例中，从相应的 `window.screen` 属性获取屏幕尺寸：

```javascript
// 获取屏幕尺寸
var w = window.screen.width;
var h = window.screen.height;

// 获取可用尺寸
var aw = window.screen.availWidth;
var ah = window.screen.availHeight;

// 获取颜色深度
var depth = window.screen.colorDepth;

// 显示设置
var res = "Resolution: " + w + " x " + h;
var col = "Colors: " + depth;
var avl = "Available screen: " + aw + " x " + ah;
alert(res + "\n" + col + "\n" + avl);
```

## 识别帧

`window.frames` 对象包含了在 `<frameset>` 标签定义的所有帧的数组。JavaScript 可以在帧内部访问这些帧。

下面的脚本包含在一个帧中。它查找帧的总数并读取每个帧的名字：

```javascript
// 查找帧的总数
var framenums = "No. frames: " + parent.frames.length;

// 获取每个帧的名字
var framenames = "\nframe 1: " + parent.frames[0].name;
framenames += "\nframe 2: " + parent.frames[1].name;
framenames += "\nframe 3: " + parent.frames[2].name;

alert(framenums + framenames);
```

> **热点** 始终为供 JavaScript 使用的 HTML 元素命名，以便产生易理解的代码。

## 访问帧

上一页的示例允许访问窗口中的不同帧，由于浏览器的对象模型是分层的，任何帧内部的对象和属性也是可见的。

这意味着 JavaScript 可以为这些属性赋值并使用它们的方法，就像在没有框架窗口中一样。

通常，窗口左侧的导航帧会有导航按钮，点击时会为屏幕右侧的主帧分配新的 URL 位置。

此示例在导航“Menu”帧中包含了一个 HTML 表单按钮。当按钮被按下时，按钮的 HTML `onclick` 属性调用 `next()` 函数来更改另外两个帧“Page”和“Banner”的位置：

```javascript
// 为帧2和帧3加载新文档的函数
function next() {
  parent.frames.Page.window.location = "nextpage.html";
  parent.frames.Banner.window.location = "nextbanner.html";
}
```

虽然点击此按钮似乎同时更改了两个帧的内容，但值得注意的是，浏览器实际上在执行两个独立的操作。点击浏览器的“后退”按钮说明了这一点，因为它第一次点击只卸载一个帧，第二次点击卸载另一个。

## 提示状态消息

`window.status` 属性可以在浏览器的状态栏中显示消息，直到另一个文档特性设置了不同的消息，或者状态恢复到默认状态。可以使用 `window.defaultStatus` 属性指定要显示的默认消息。

若要在用户将光标悬停在超链接上时显示消息，应该用 HTML 的 `onmouseover` 属性指定要显示的消息。它还必须返回 `true`，以防止链接 URL 像通常那样出现在状态栏中。

此示例在 HTML 标签内使用 JavaScript，指定了一个默认消息并为链接添加了 `onmouseover` 属性。这会在光标悬停在链接上时显示另一条消息：

```html
<body onload = "window.defaultStatus = 'Status Demo';">
<p><a href="nextpage.html" onmouseover="window.status='Click Here';return true">超文本链接</a></p>
```

某些版本的 Firefox 浏览器默认禁用了状态栏消息——要启用它们，请在地址栏中输入 `about:config`，然后从出现的列表中将 `dom.disable_window.status_change` 设置为 `false`。

## 滚动与移动

可以使用 JavaScript 的 `window.scrollBy()` 和 `window.scrollTo()` 方法调整文档内的滚动。每个方法都需要两个数值参数，说明沿 X 轴和 Y 轴移动多少像素。同样地，可以使用 `window.moveTo()` 和 `window.moveBy()` 方法调整屏幕上的窗口位置，这些方法也需要两个 X 和 Y 坐标的参数。下面的示例调用了 `window.scrollBy()` 方法，在用户按下按钮时沿 X 轴移动 100 像素：

```html
<input type="button" value="Scroll" onclick="window.scrollBy(100,0)">
```

## 寻求确认

`alert()` 函数在本书中被广泛使用，它实际上是一个 `window` 对象的方法，因此可以正确地写为 `window.alert()`。

由于 `window` 对象是文档对象模型（DOM）中的顶层对象，它的属性和方法可以选择省略地址中的 "window."——所以 "window.alert()" 可以被识别为仅 "alert"。

`window.confirm()` 方法是另外两个产生对话框的窗口方法中的第一个。当它用于从包含 OK 按钮的对话框中获取用户确认时，OK 按钮向脚本返回 `true`，Cancel 按钮向脚本返回 `false`。应向该方法传递一个文本字符串参数，包含要询问用户的的问题。

此示例演示了 `window.confirm()` 方法执行条件分支以确定显示哪条消息——取决于用户点击了哪个按钮：

```javascript
// 创建一个变量来存储对话响应
var ask = window.confirm("你确定要继续吗？");

// 显示相应的回复消息
( ask ) ? window.alert("点击了 OK 按钮") : window.alert("点击了取消 按钮");
```

## 提示输入

另一个在调用时会产生对话框的窗口对象方法是 `window.prompt()` 方法，它在之前的示例中以简写形式 `prompt()` 引入过。该方法通过包含文本字段以及 OK 和取消按钮的对话框，从用户处获取键盘输入。它需要两个参数，用于指定要显示的消息和默认文本值。当用户按下 OK 按钮时，对话框返回文本字段的值。此示例获取用户输入以创建一个合适的消息：

```javascript
// 请求用户选择菜单
var dest = window.prompt("请选择一个目的地... 1. 法国 2. 西班牙", "");

// 显示相应的消息
dest = (dest == "2") ? "西班牙" : "法国"
window.alert("欢迎来到 " + dest);
```

## 打开新窗口

JavaScript 可以 `window.open()` 方法打开新的浏览器窗口来显示指定的文档。这些所谓的“弹出”窗口总是比原始窗口小，并且有许多用途，包括显示一组缩略图尺寸的图像。`window.open()` 方法接受三个参数，分别指定在弹出窗口中加载的 URL、该窗口的名称以及使用以下关键字指定的所需的尺寸：

| 特性 | 描述 |
| :--- | :--- |
| `directories` | 添加目录（链接） |
| `height` | 设置文档区域的高度（像素） |
| `left` | 窗口在屏幕上的 X 坐标 |
| `location` | 添加地址栏 |
| `menubar` | 添加标准菜单栏 |
| `resizable` | 允许调整窗口大小 |
| `scrollbars` | 需要时启用滚动条 |
| `status` | 添加状态栏 |
| `toolbar` | 添加带有前进和后退按钮的工具栏 |
| `top` | 窗口在屏幕上的 Y 坐标 |
| `width` | 设置文档区域的宽度（像素） |

在特性列表中包含任何空格都会导致错误。第三参数中的所有必要特性必须作为一个由逗号分隔的列表列出，且不能有空格。

`window.open()` 方法的工作原理是创建一个可以赋值给变量的窗口对象。可以调用 `window.close()` 方法关闭该弹出窗口，并调用 `window.print()` 方法打印其内容。在示例中，全局变量被初始化为 `null` 值。第一个函数为其分配了一个 `window` 对象并打开一个包含指定“pop.html”文档的弹出窗口。第二个函数关闭弹出窗口并为全局变量重新赋值为 `null`。这种技术确保了在任何时刻只能存在一个弹出窗口实例。

```javascript
// 用于存储窗口对象的空变量
var popwin = null;

// 打开弹出窗口的函数
function open_popwin() {
  if(popwin == null) { // 检查它是否不存在
    // 然后创建一个窗口对象并打开弹出窗口
    popwin = window.open("popup.html", "",
      "top=100,left=80,width=250,height=100,status");
  }
}

// 关闭弹出窗口的函数
function close_popwin() {
  if(popwin != null) { // 检查它是否已存在
    // 然后关闭弹出并删除窗口对象
    popwin.close(); popwin = null;
  }
}
```

> **不要忘记** 如果未为弹出窗口指定名称，`window.open()` 方法的第二个参数必须为空字符串——如此处所示。

## 总结

- `window.location` 对象的 `href` 属性存储当前文档的完整 URL 地址，可以通过 `protocol`、`host`、`pathname` 和 `hash` 属性找到。
- 为 `location` 赋值完整 URL 会加载该文档。
- `window.history` 对象的 `back()` 和 `forward()` 方法模拟浏览器的后退按钮。
- 向 `window.history.go()` 方法传递正或负数值参数以确定加载的步数。
- `window.screen` 对象通过其 `width`、`height`、`availWidth`、`availHeight` 和 `colorDepth` 属性存储显示器信息。
- `window.frames` 对象是所有帧的数组。
- 可以使用 `parent` 关键字访问帧集，并通过数组索引数字或给定的名称访问每个帧。
- 可以使用 `window.status` 属性在状态栏中显示消息，或通过 `window.defaultStatus` 属性指定默认消息。
- `window.moveBy()` 和 `window.moveTo()` 方法调整窗口在屏幕上的位置。
- `window.scrollBy()` 和 `window.scrollTo()` 方法调整浏览器窗口内的焦点位置。
- 可以使用 `window.prompt()` 和 `window.confirm()` 方法获取用户输入。
- JavaScript 使用 `window.open()` 和 `window.close()` 方法打开和关闭弹出窗口。

# 10 探索文档对象

本章探索了 `window.document` 对象，它允许 JavaScript 访问浏览器中加载的文档的组件。

- 116 访问数组组件
- 118 直接访问元素
- 120 使用 Cookie
- 122 使用 JavaScript 写入内容
- 124 提取文档信息
- 126 创建新组件
- 128 总结

## 访问数组组件

`window.document` 对象具有许多属性和方法，JavaScript 可以通过访问这些内容来操作加载的文档。当文档加载时，关于其组件特征的信息会存储在 `window.document` 对象的 `anchors`（锚点）、`forms`（表单）、`images`（图像）和 `links`（链接）数组属性中。与所有其他数组一样，可以使用 `length` 来发现任何组件数组的大小，并可以使用索引数字访问单个元素。

以下示例展示了从 `window.document` 数组获取 HTML 组件的名称和数字：

```html
<a name="top_of_page" id="fragment">
Select a search engine...</a>
<a href="http://www.google.com" name="google_link">
<img src="google.gif" alt="google_graphic">
</a>
<a href="http://www.yahoo.com" name="yahoo_link">
<img src="yahoo.gif" id="engine-2" alt="Yahoo_graphic">
</a>

<form id="form-1" action="">
<p><input type="button" value="Click Me" onclick="show_parts()" /></p>
</form>
```

```javascript
function show_parts() {
  var parts = "Anchors: " + document.anchors.length;
  parts += "\nlist anchor name: " + document.anchors[0].name;
  parts += "\nForms: " + document.forms.length;
  parts += "\nlist form id: " + document.forms[0].id;
  parts += "\nImages: " + document.images.length;
  parts += "\nlist image id: " + document.images[0].id;
  parts += "\n2nd image id: " + document.images[1].id;
  parts += "\nLinks: " + document.links.length;
  parts += "\nlist link name: " + document.links[0].name;
  parts += "\n2nd link name: " + document.links[1].name;
  alert(parts);
}
```

> **别忘了** 分段锚点包含在 `anchors` 数组中，但不在 `links` 数组中。

## 直接访问元素

在上一个示例中，通过 `window.document` 数组访问文档组件的技术，在符合世界维网联盟（W3C）制定的文档对象模型（DOM）规范的现代浏览器中是可以避免的。

W3C DOM 强调在 HTML 元素中包含唯一的 `id` 属性，以便可以通过 `window.document.getElementById` 方法直接对其进行访问。在最初测试该方法是否存在是有用的，以确保用户拥有的是符合 W3C DOM 的现代浏览器。

下面的示例访问了 `id` 属性值为 "engine-1" 的元素，如第 116 页的 HTML 文档所示。在获取元素的其他属性值之前，它首先检查浏览器是否符合 W3C DOM。

```javascript
function show_attribs() {
  // 测试现代浏览器
  if (!window.document.getElementById) {
    alert("Not W3C DOM browser!");
    return;
  }
  // 使用 id 获取属性值
  var attribs = "";
  attribs += "Link name: " + window.document.getElementById("engine-1").name;
  attribs += "\nTarget: " + window.document.getElementById("engine-1").href;
  alert(attribs);
}
```

> **别忘了** 因为 `window` 对象是顶层，因此可以从地址中省略，你可以直接使用 `document.getElementById()`。

符合 W3C 的浏览器中引入的另一个实用方法允许 JavaScript 通过将标签名称作为 `window.document.getElementsByTagName()` 的参数，创建一个特定标签所有元素的数组。注意，这将是标签的实际名称——而不是分配给属性的值。

标签按照它们在文档中出现的顺序分配给数组，因此第一个出现的标签索引为 0。然后可以使用数组名称和其索引来访问数组中的每个元素。

下面的示例检查了 W3C DOM 并创建了 `<img>` 标签的数组，如第 116 页所示。最后分配给每个 `<img>` 标签的 "alt" 属性的值将显示在警报框中：

```javascript
function show_attribs() {
  // 检查 W3C DOM
  if (!window.document.getElementById) {
    alert("Not W3C DOM browser!");
    return;
  }

  // 创建 <img> 标签数组
  var pics = window.document.getElementsByTagName("img");
  alert(pics[0].alt + "\n" + pics[1].alt);
}
```

> **记住** 这个方法中有一个 "s"，因为你通过 `getElementsByTagName()` 获取多个元素——而通过 `getElementById()` 只获取一个元素。

## 使用 Cookie

Cookie 是 JavaScript 写入本地硬盘以存储少量数据的微型文件。Cookie 的大小限制为 4KB，且浏览器通常允许存储多个 Cookie。

Cookie 数据在 `window.document.cookie` 对象中以 `name=value` 对的形式存储。在后续访问期间，`window.document.cookie` 会返回这些 `name=value` 对。

`window.document.cookie` 返回的 `name=value` 对是以分号分隔的。

除非指定了过期时间（expires），否则 Cookie 的生命周期取决于浏览器会话。

通过 `toGMTString()` 方法以 GMT 格式表示过期时间。

下面的示例说明了如何使用天、小时、分钟和毫秒来增加 Date 对象。

此示例在 Cookie 中存储了一周的用户名和账号：

```javascript
// 要存储在 Cookie 中的数据
var user = "Mike McGrath,00456";

// 创建一个新的 Date 对象
var expiry = new Date();

// 设置 7 天后的时间
expiry.setTime(expiry.getTime() + 7*24*60*60*1000);

// 创建 Cookie
window.document.cookie = "cookie=" + escape(user) + ";expires=" + expiry.toGMTString() + ";";
```

如果设置了 Cookie，`window.document.cookie` 对象将返回 true，因此 JavaScript 可以测试 Cookie 是否存在。定位 Cookie 时，`window.document.cookie` 返回存储的字符串。可以使用本书之前过的字符串处理方法从存储的字符串中提取数据。当下面的脚本运行时，它首先寻找之前设置的 Cookie；然后提取值显示 Cookie 内容：

```javascript
// 查找任何 Cookie
if(window.document.cookie) {
  // 解码 Cookie 数据
  var cookiedata = unescape(window.document.cookie);
  // 分割 name=value 对
  var userdata = cookiedata.split("=");
  // 如果 Cookie 名为 cookie
  if(userdata[0] == "cookie") {
    // 分割逗号分隔的值
    var data = userdata[1].split(", ");
    var user = data[0];
    var acct = data[1];
    // 显示从 Cookie 获取的数据
    alert("Welcome " + user + "\nAccount number: " + acct);
  }
}
```

> **在检索 Cookie 时，解码任何转义的数据。**

多个 `name=value` 对将自动以分号分隔每个对的形式返回。使用 `string.indexOf()` 来识别所需的对。

## 使用 JavaScript 写入

`window.document` 对象的 `write()` 方法是一个极其强大的功能，它允许 JavaScript 在加载网页时动态创建内容。该方法接受一个字符串参数，其中包含要写入页面的内容，该内容可能包含用于格式化内容的 HTML 标签。

通常情况下，`window.document.write()` 方法会在 HTML 文档的 `<body>` 部分内添加内容，并根据条件测试的结果写入选定的内容。

需要注意的是，在运行时调用此方法将导致指定的内容写入新的空白文档，或者替换当前页面。

变量值也可以与字符串参数拼接，以便将变量值引入网页内容中。

此示例首先生成一个随机数，然后测试以确定该数字是奇数还是偶数。根据测试结果，将选定的内容添加到页面中：

```javascript
// 获取一个 1 - 100 之间的随机整数
var n = Math.ceil(Math.random() * 100);

// 判断数字是奇数还是偶数
var ntype = (n % 2 == 0) ? "Even" : "Odd";

// 写入数字的描述
document.write("<h1>Number "+n+" is "+ntype+"</h1>");
```

> **别忘记** 地址中的“window”部分可以省略——直接使用 `document.write()` 即可。

`window.document.open()` 方法打开一个新的 HTML 文档，可以使用 `window.document.write()` 方法向其写入以创建动态内容。当内容写入后，应该通过 `window.document.close()` 方法关闭文档流。下面的示例在上一章弹出窗口示例的基础上，通过从 JavaScript 写入内容而不是简单地加载现有的 HTML 文档：

> **小贴士** 传递空字符串作为 URL 参数可以打开一个空窗口。

```javascript
// 一个创建动态弹出窗口的函数
function popup() {
  // 创建弹出窗口
  var popwindow = window.open("", "", "top=40,left=30,width=250,height=125");
  // 打开弹出窗口 HTML 文档
  popwindow.document.open();
  // 在弹出窗口中写入内容
  popwindow.document.write("<title>Pop-up</title>");
  popwindow.document.write("<h1>Dynamic Pop-up Page</h1>");
  popwindow.document.write("<img src='dex.gif'>");
  popwindow.document.close(); // 关闭 HTML 文档
}
```

> **别忘记** 记住在双引号内部使用单引号。

## 提取文档信息

`window.document` 对象有多个属性，存储有关当前加载文档的信息。其 `domain` 属性包含 URL 地址的域名部分，完整地址存储在 `window.document.URL` 属性中。

当在浏览器中通过超链接加载网页时，`window.document.referrer` 属性包含提供链接的页面 URL。当前文档的标题（由 HTML `<title>` 元素定义）存储在 `window.document.title` 属性中。

在下方列出的简单 HTML 文档中，调用了一个脚本来在无序列表中动态写入列表项，详细列出该文档的属性，该文档是在通过超链接加载的：

```html
<html>
<head>
<title>Document Properties</title>
</head>
<body>
<ul>
<script type="text/javascript" src="props.js"></script>
</ul>
</body>
</html>
```

```javascript
// 写入属性...
document.write("<li>Domain: " + document.domain + "</li>");
document.write("<li>Referrer: " + document.referrer + "</li>");
document.write("<li>Title: " + document.title + "</li>");
document.write("<li>URL: " + document.URL + "</li>");
```

> **注意** `URL` 属性名是大写的。

## 创建新组件

在现代浏览器中，符合 W3C DOM 的 JavaScript 可以使用 `window.document.createElement()` 动态创建一个新的 HTML 元素。通过指明属性名称和值作为 `setAttribute()` 方法的参数，可以向 HTML 元素添加属性。对于包裹文本的 HTML 元素，可以使用 `window.document.createTextNode()` 指定一个字符串。



# 处理事件

本章描述了由用户操作引起的浏览器事件，并演示了 JavaScript 如何做出响应。

- 响应窗口事件
- 响应点击
- 确认按键动作
- 识别鼠标移动
- 识别焦点和大小
- 总结

## 响应窗口事件

当网页上的所有 HTML 元素完全加载时，会触发 Load 事件。这意味着 `window.onload` 事件处理器只有在所有元素存在后才会被激活。通常，`window.onload` 事件处理器会调用一个 JavaScript 函数（通常命名为 "init"）来初始化多个值。

相反，Unload 事件在用户移动到另一个网页或关闭浏览器时发生，此时 `window.onunload` 事件处理器会被激活。

此示例在表单文本框中设置了一个初始值，并在用户离开页面时显示一个最终的警报对话框消息：

```javascript
// 指定 onload 和 unload 事件处理器
window.onload = init;
window.onunload = term;

// 用于响应 LOAD 事件的函数
function init() {
    document.getElementById("box-1").value = 
    "The Page Is Loaded";
}

// 用于响应 UNLOAD 事件的函数
function term() {
    alert("感谢访问\n欢迎经常光临");
}
```

分配给 `<body>` 标签 `onload` 属性的 HTML 事件处理器可以替换脚本中分配的那个句柄。

当遇到运行时错误时，会发生 Error 事件，此时 `window.onerror` 事件处理器会被激活以确定如何处理错误。`window.onerror` 事件处理器可以调用 JavaScript 函数来处理错误；否则浏览器将通过打开错误对话框来自行处理错误。

一旦通知了错误，将向浏览器返回一个 `true` 值，表示错误已处理。为了避免出现所有错误对话框，自定义的错误处理器函数仅在遇到错误时才返回 `true`。

有用的是，浏览器将向错误处理器传递三个参数，其中包含错误性质的信息、包含错误的文件的 URL，以及该文件中错误实际的实际行号。

在下面的示例中，浏览器传递给错误处理函数的每个错误信息都将显示给用户：

```javascript
// 指定 onerror 错误处理器
window.onerror = errorhandler;

// 用于响应 ERROR 事件的函数
function errorhandler( msg, url, ln ) {
    alert("Error: " + msg + " \nIn File: " + url + " \nAt Line: " + ln);
    return true; // 告诉浏览器已处理
}

// 一个故意制造的错误 - 此项不存在
document.getElementById("btn").value = "myButton";
```

必须在脚本顶部指定错误处理器，以捕获所有可能的错误。

## 响应点击

最常见的交互事件是 Click 事件，当用户在网页上按下鼠标左键时创建，以激活其 `onclick` 处理器——通常是一个 HTML 表单按钮。`onclick` 事件处理器通常被分配在按钮的 HTML `<input>` 类型的 `onclick` 属性中，如下：

```html
<input type="button" value="Do Click" onclick="dbl_click('Button Pressed')" />
```

同样，当用户双击鼠标左键以激活 `ondblclick` 事件处理器时，会发生 DblClick 事件。

此示例指定了一个事件处理器来“监听”窗口中的 DblClick 事件，以及一个处理按钮组件事件的函数。

```javascript
// 指定一个 DBLCLICK 事件处理器
window.ondblclick = do_dblclick;

// 用于响应按钮 CLICK 事件的函数
function do_click(str) { 
    alert(str);
}

// 用于响应 DBLCLICK 事件的函数
function do_dblclick() { 
    alert("Double Clicked"); 
}
```

MouseDown 事件在用户按下鼠标键时发生，MouseUp 事件在释放鼠标键时发生。通常这些会被一起使用，使得单个鼠标点击将激活两个事件处理器，如下：

```html
<input type="button" value="Light Switch" onmousedown="light(1)" onmouseup="light(0)">
```

此示例在光标悬停在图像上并按下鼠标键时，交换图像并更改文本框的值。当释放按钮时，两者都会恢复到原始状态：

```javascript
// 用于响应 MOUSEDOWN 和 MOUSEUP 事件的函数
function light(n) {
  var pic = document.getElementById("bulb");
  var box = document.getElementById("txt");
  if(n == 1) {
    pic.src = "on.gif";
    box.value = "Button Down";
  } else {
    pic.src = "off.gif";
    box.value = "Button Up";
  }
}
```

`document`、`link` 和 `button` HTML 元素都支持 `onmousedown` 和 `onmouseup` 属性。

## 确认按键动作

当用户按下键盘按键时发生 KeyDown 事件，释放时发生 KeyUp 事件。通常这些会被一起使用，因此按下和释放按键将激活两个事件处理器。此示例在按下键盘按键时交换图像并更改文本框的值，当释放按键时，两者都会恢复到原始状态：

```javascript
// 指定 KEYDOWN 和 KEYUP 事件处理器
window.document.onkeydown = iskeydown;
window.document.onkeyup = isup;

// 用于响应 KEYDOWN 事件的函数
function iskeydown() {
    document.getElementById("bulb").src = "on.gif";
    document.getElementById("txt").value = "Key Down";
}
```

此代码故意遗漏了 `window.document` 地址中的 `window.` 部分。

```javascript
// 用于响应 KEYUP 事件的函数
function isup() {
    document.getElementById("bulb").src = "off.gif";
    document.getElementById("txt").value = "Key Up";
}
```

| Key & KeyDown | |
| :--- | :--- |
| ⬅ | key-keydown |
| + | KeyUp & KeyDown |
| 💡 | Key is Up |
| Done | |
| KeyUp & KeyDown | |
| :--- | :--- |
| ➡ | key-keyup |
| + | KeyUp & KeyDown |
| 💡 | Key is Down |
| Done | |

当用户按下按键时，KeyDown 事件会将一个数值传递给 `KeyboardEvent` 对象的 `keyCode` 属性。该数字是按键的 Unicode 字符编号，可以使用 JavaScript 发现按下了哪个键。

此示例显示了大小写的字符代码。`KeyboardEvent` 对象作为参数传递给指定的 Key 事件处理器。Internet Explorer 将值存储在它的事件对象中，可以直接访问其 `keyCode` 属性，因此脚本分支到：

```javascript
// 指定一个 KEYDOWN 事件处理器
window.document.keydown = showkey;

// 用于响应 KEYDOWN 事件的函数
// 将 KeyboardEvent 对象作为参数
function showkey(e) {
  var obj = (navigator.appName == "Microsoft Internet Explorer") ? event : e;
  // 考虑 keyCode 属性值
  if(obj.keyCode == 89 || obj.keyCode == 121)
    alert("Y pressed");
  if(obj.keyCode == 78 || obj.keyCode == 110)
    alert("N pressed");
}
```

## 识别鼠标移动

当用户将光标置于网页上的对象上时，会发生 MouseOver 事件；当光标移出该对象时，会发生 MouseOut 事件。

通常，这些事件在 JavaScript 中用于提供图像切换的“悬停”效果。可以使用 `<img>` 标签配合 `onmouseover` 和 `onclick` 属性来指定事件处理器，如下所示：

```html
<img src="off.gif" onmouseover="swap(this, 1)" id="rollover" onmouseout="swap(this, 0)">
```

在这种情况下，发生 MouseOver 和 MouseOut 事件时，事件处理器会接收两个参数——一个是通过 `this` 关键字的图像对象的引用，以及一个整数。事件处理器更改所引用图像对象的源，并在状态栏消息中确认所提供的整数值：

```javascript
// 一个用于响应 MOUSEOVER 和 MOUSEOUT 的函数
function swap(pic, n) {
  if(n == 1)
    pic.src = "on.gif"; window.status = "MouseOver"
  if(n == 0)
    pic.src = "off.gif"; window.status = "MouseOut";
}
```

脚本可以通过 id 来指定目标元素，但传递引用参数会更高效。

当用户移动鼠标时，`MouseMove` 属性会将数值值传递给 `MouseEvent` 对象的 `pageX` 和 `pageY` 属性。这些数字是光标在浏览器窗口中的 X 和 Y 坐标。

此示例在光标移动时在文本输入框中显示坐标，并将 `MouseEvent` 对象作为参数传递给指定的 MouseMove 事件处理器。Internet Explorer 将这些值存储在其事件对象的 `x` 和 `y` 属性中，可以直接访问，因此脚本会进行分支处理：

```javascript
// 指定一个 MOUSE 事件处理器
window.document.onmousemove = showcoords;

function showcoords(e) {
  var xpos, ypos;
  if(navigator.appName == "Microsoft Internet Explorer")
    xpos = event.x; ypos = event.y;
  else
    xpos = e.pageX; ypos = e.pageY;
  // 显示坐标
  document.getElementById("txt").value =
    "X: " + xpos + " Y: " + ypos;
}
```

> **热提示** 许多令人兴奋的动态 HTML (XMLHttpRequest) 利用了这种跟踪鼠标坐标的能力。

## 识别焦点和大小

当用户将光标移动到网页的某个组件上时（聚焦于该组件），会发生 Focus 事件。相反，当用户将光标移出该组件时（将焦点移到其他处），会发生 Blur 事件。

表单元素通过其 HTML 的 `focus` 和 `onblur` 属性为 Focus 和 Blur 事件创建事件处理器，如下所示：

```html
<input type="text" value="Enter a quantity" onfocus="wipe(this)" onblur="check(this,'quantity')">
```

在这种情况下，当用户聚焦于该文本框时，Focus 事件处理器会移除文本字段中的初始值。当用户将光标离开文本框时，Blur 事件处理器会检查是否已输入值，如果没有输入，则显示警报框：

```javascript
// 一个用于响应 FOCUS 事件的函数
function wipe(box) {
  box.value = ""
}

// 一个用于响应 BLUR 事件的函数
function check(box, str) {
  if(box.value == "") alert("Enter a " + str);
}
```

**热提示**  

注意 "this" 关键字参数是如何将表单组件的引用传递给事件处理器的。

当用户更改浏览器窗口大小时，会发生 Resize 事件，`onresize` 事件处理器可以指定一个函数，使页面适应新的窗口大小。

这在重新定位 HTML 组件时最有用，如下例所示，它在加载时以及每当窗口大小发生变化时将 HTML `<div>` 元素居中显示：

```javascript
// 指定 LOAD 事件处理器
window.onload = set_pos;

// 指定 RESIZE 事件处理器
window.onresize = set_pos;

// 一个用于响应 LOAD 事件的函数
function set_pos() {
  // 获取窗口宽度
  var width = document.body.clientWidth;

  // 计算宽度的一半
  var left_pos = parseInt(width / 2);

  // 设置左侧位置
  document.getElementById("layer").style.left = left_pos + "px";
}
```

> **热提示**  

有关 DHTML 的更多信息，请参阅第 13 章

## 总结

- 当用户将光标移动到网页组件上时，发生 Focus 事件。
- 当用户将光标移出组件时，发生 Blur 事件。
- 当用户更改浏览器窗口大小时，发生 Resize 事件。
- `onresize` 事件处理器可以指定一个函数，使页面适应新的窗口大小。
- `MouseMove` 属性将数值值传递给 `pageX` 和 `pageY` 属性。
- Internet Explorer 将这些值存储在其事件对象的 `x` 和 `y` 属性中。
- Focus 事件处理器移除文本框中的初始值。
- Blur 事件处理器检查是否已输入值。
- "this" 关键字参数将表单组件的引用传递给事件处理器。

# 表单交互

`document.forms[]` 元素对象包含表单内所有元素的数组，并按照它们在 HTML 代码中出现的顺序进行索引。例如，对于名称为 "f" 的表单，`document.forms.elements[0]` 指向该表单中出现的第一个元素。

如果元素的 `id` 属性已分配了值，则可以通过该值来访问该元素。因此，表单 "f" 中 id 为 "btn1" 的元素可以通过 `document.forms.f.btn1` 进行访问：

```html
<form id="f" method="post" action="">
<input type="button" id="btn1" value="Click Me" onclick="alert('Hi - I am a button')"></form>
```

其他属性可以作为元素的属性进行访问——此示例所示：

```javascript
function element_info() {
  var msg = "Element Type: " + document.forms.btn1.type; // 元素类型
  msg += "\nElement Value: " + document.forms.btn1.value; // 元素值
  msg += "\nOnclick: " + document.forms.btn1.onclick; // onclick 值
  alert(msg);
}
```

## 赋值文本值

HTML `<input>` 中显示的文本可以通过 JavaScript 简单地通过为该元素的 `value` 属性分配一个新字符串来更改。

在历史上，文本框被限制只能显示一种固定字体的文本，但现代浏览器允许对字体、大小和颜色进行选择。

下面的示例在文本框中显示一个字符串，并为字体、前景颜色和背景颜色添加样式特征：

```javascript
// 一个设置表单文本字段文本的函数
function set_text() {
  // 针对表单 f 中的文本字段 txtl
  with(window.document.forms.f.txtl) {
    // 设置文本值
    value = "JavaScript in easy steps";
    // 设置样式特征
    style.fontFamily = "comic sans ms";
    style.fontSize = "16pt";
    style.color = "yellow";
    style.background = "red";
  }
}
```

HTML `<textarea>` 元素类似于一个大型滚动文本输入框，其值可以被 JavaScript 读取和写入。

示例在文档加载后，通过向其 `value` 属性分配字符串来向文本区域写入内容。

分配该字符串的函数被脚本指定为文档的 `onload` 事件处理器。

使用这种方法时需要小心——如果脚本包含在 HTML 文档的 `<head>` 部分，`<body>` 标签中的 `onload` 属性可能会覆盖它。

```javascript
// 为 textarea 字段分配字符串
window.document.forms.f.textarea.value = 
"Computers in the future may perhaps weigh 1.5 tons. (Popular Mechanics forecasting the development of computer technology, 1949)";

// 定义 onload 函数
window.onload = write_text;
```

## 轮询单选按钮

一组在任何时候只允许其中一个被选中的单选按钮，应该在 HTML `<input>` 标签的 `name` 属性中被分配相同的 `name`。

在浏览器 DOM 中，单选按钮会根据给定的名称创建一个 `window.document.forms` 对象。

该对象包含该组内单选按钮的数组，按照它们在 HTML 代码中出现的顺序进行索引。

JavaScript 可以使用数组名和索引号来访问每个单选按钮。在下面的示例中，JavaScript 遍历每个名为 "rad" 的单选按钮的 `checked` 属性，以发现哪一个被选中。然后将该按钮的 HTML `value` 属性的值赋值给设置文档的背景颜色：

```javascript
function radio_poll() {
  for( var i = 0; i < window.document.forms.f.rad.length; i++) {
    if( window.document.forms.f.rad[i].checked ) {
      window.document.body.style.background = window.document.forms.f.rad[i].value;
    }
  }
}
```

## 轮询复选框

与单选按钮不同，复选框与其他复选框独立运行，因此所有复选框都应通过其 HTML 代码中的 `name` 属性唯一标识。

每个复选框都会根据其给定的名称创建一个 `window.document.forms` 对象，并且像单选按钮一样，每个都有一个 `checked` 属性。

在此示例中，JavaScript 检查名为 "chk1"、"chk2" 和 "chk3" 的三个复选框，以发现哪些被选中。它使用 `eval()` 函数来拼接属性名和数字。被选中的项的值被加到一个字符串中以便在 `alert()` 对话框中显示：

```javascript
function checkbox_poll() {
  var str = "Choice is ";
  for(var i=1; i<4; i++) {
    // 如果复选框被选中，则添加其值
    if(eval("document.forms.chk" + i).checked) {
      str += eval("document.forms.chk" + i).value;
    }
  }
  alert(str);
}
```

> 提示 使用 `eval()` 函数来组合属性名和数字。

## 选择选项

HTML `<select>` 列表中的 `<option>` 项为每个显示的标签都有一个 `text` 属性和一个关联的 `value` 属性。这些等同于 `<select>` 列表中 `<option>` 元素的 HTML `name` 和 `value` 属性。

这种 name=value 对在表单提交时发送到服务器。

所有菜单项存储在 `<select>` 对象的 `options[]` 数组中，其标签和关联值可以由 JavaScript 动态设置。

此示例在下拉列表中动态设置选项标签和值。表单 id 为 "f"，`<select>` 元素 id 为 "menu"。

```javascript
// 一个设置选项标签和值的函数
function set_options() {
  with(window.document.forms.f) {
    options[0].text = "One"; options[0].value = "1";
    options[1].text = "Two"; options[1].value = "2";
    options[2].text = "Three"; options[2].value = "3";
  }
}
```

`options[]` 元素必须由 HTML 代码初始创建。

`options[]` 有一个名为 `selectedIndex` 的属性，包含当前选中项的索引号。

JavaScript 可以获取当前选择的值来实现动态效果。

此示例在文本框中提取当前选择的值。表单 id 为 "f"，`<select>` 元素 id 为 "city"。当用户点击按钮时通过其 `onclick` 属性调用函数。

```javascript
// 获取选中项的函数
function get_selected() {
  // 存储索引号的变量
  var pick = window.document.forms.f.city.selectedIndex;

  // 将选中元素的值赋值给 id 为 "txt1" 的文本字段
  window.document.forms.f.txt1.value = 
  window.document.forms.f.city.options[pick].value;
}
```

> 提示 此示例可以使用 `with` 语句使其更简洁，正如对面页面示例所示。

## 响应变化

当表单输入发生变化时会触发 Change 事件，例如用户在选项列表中选择一个项时。`onchange` 事件处理器可以调用 JavaScript 函数在每次 Change 发生时执行某些代码。

下面的示例将初始选中选项设置为绿色，然后分配一个事件处理器，每当选择更改时在文本框中显示关联的值：

```javascript
// 指定 onload 事件处理器
window.onload = init;

// 响应 LOAD 事件的函数
function init() {
  window.document.forms.f.s.options[1].selected = true;
  // 指定 CHANGE 事件处理器
  window.document.forms.f.s.onchange = show_selected;
}

// 响应 CHANGE 事件的函数
function show_selected() {
  var num = window.document.forms.f.s.selectedIndex;
  window.document.forms.f.txt.value = 
  window.document.forms.f.s.options[num].value;
}
```

## 重置与提交表单

当用户点击表单的 HTML 重置按钮时，会发生 Reset 事件，JavaScript `window.onerror` 属性可以指定一个在 Reset 事件发生时调用的事件处理器。

在本例示例中，Reset 事件处理器简单地打开一个警告对话框，告知用户表单已重置：

```javascript
// 指定一个 LOAD 事件处理器
window.onload = init;
// 指定一个 RESET 事件处理器
function init()
{
  window.document.forms.f.onreset = advise;
}
```

```javascript
// 一个用于响应 RESET 事件的函数
function advise()
{
  alert("Form has been reset\nPlease select a color");
}
```

> 注意
> 只有在用户点击警告对话框中的 OK 按钮后，选中的单选按钮会被清除。

# 提交表单

JavaScript 可以通过调用表单的 `reset()` 方法将表单组件恢复到原始状态，或者通过调用 `submit()` 方法将其内容发送到 Web 服务器。

理想情况下，可以在提交表单之前，通过为表单的 `onSubmit` 属性指定事件处理器来验证表单的值——该处理器由表单的 Submit 事件调用。

在以下示例中，JavaScript 测试输入字符串格式是否包含 `@` 和点 字符，并且只有当电子邮件地址验证看起来正确时才会提交表单：

```javascript
// 一个验证基本电子邮件地址格式的函数
function send_if_valid() {
    // 在地址中寻找 @ 和 . 字符
    if(document.forms.f.email.value.indexOf("@") == -1
    || document.forms.f.email.value.indexOf(".") == -1) {
        // 如果不存在则显示消息
        alert("Email address is absent or incorrect");
        return false; // ...并且不提交表单
    }
}
```

> 注意：使用 JavaScript 的表单 `submit()` 方法不会触发 `onSubmit` 事件处理器。

# 中止图像下载

Internet Explorer 允许为 Abort 事件指定事件处理器，该事件在用户取消图像下载时发生——通常是通过点击浏览器工具栏上的停止按钮。当图像下载被取消时，`onload` 事件处理器可以调用 JavaScript 函数。

为了识别图像名称，必须在 HTML `<img>` 元素的 `id` 属性中赋予名称，如下：

```html
<img id="big pic" src="bigpic.jpg" onabort="abort_msg()" alt="">
```

将事件处理器分配给该图像元素的 `onabort` 属性。在本例中，事件处理器创建了一个 `alert()` 消息来确认取消：

```javascript
// 一个为 Internet Explorer 用户显示取消确认消息的函数
function abort_msg() {
 if (navigator.appName == "Microsoft Internet Explorer")
alert("Image Download Has Been Aborted");
}
```

> 注意
> `onabort` 属性被 Internet Explorer 支持，但不符合最近的 W3C 标准。

## 总结

- `window.document.forms` 对象包含网页上所有表单的数组，按它们出现的顺序排列。每个表单可以通过其 `forms` 数组索引访问，例如 `window.document.forms[0]`，或者通过使用分配给其 HTML `id` 属性的值访问，例如 `window.document.forms.f`。
- `window.document.forms.elements` 对象包含表单中所有元素的数组，按它们出现的顺序排列。表单中的每个元素都可以通过其 `elements` 数组索引访问，例如，第一个元素通过 `window.document.forms.elements[0]`，或者通过其 `id` 访问，例如 `window.document.forms.f.btn1`。
- JavaScript 可以使用表单组件的 `value` 属性为其赋值一个字符串。
- 循环可以检查单选按钮或复选框的 `checked` 属性，以发现用户选中的项。
- HTML `<select>` 元素的 `options` 属性包含其嵌套 `<option>` 元素的数组。数组中的每个元素都有一个 `text` 属性（存储字符串标签）和一个 `value` 属性（存储其关联的值）。
- `options` 数组的 `selectedIndex` 属性存储当前选中选项的索引号。
- 当表单的值发生变化时，会发生 Change 事件并调用其 `onchange` 事件处理器。当用户点击表单重置按钮时，会发生 Reset 事件并调用 `onreset` 事件处理器。
- JavaScript 可以使用 `reset()` 方法重置表单并使用 `submit()` 方法将其提交到服务器。
- 在 Internet Explorer 中，当用户点击浏览器停止时，会发生 Abort 事件，然后调用 `onabort()` 事件处理器。

# 13 创建动态效果

本章演示了文档对象模型 (DOM) 如何允许 JavaScript 访问 HTML 文档中的任何元素。

- 介绍 DOM
- 使用 javascript: 协议
- 操作样式属性
- 切换可见性
- 插入内容
- 制作幻灯片
- 处理层移动
- 总结

## 介绍 DOM

下表说明了文档对象模型 (DOM) 的重要部分以及页面组件之间的关系：

所示项目都是不同类型的元素。

理解层级 DOM 使得在 JavaScript 中访问属性“f”变得简单。

> 注意
> 因为空格的原因，第一条语句在这里被换行了。

```javascript
function modify() { // 3 种方式
window.document.forms[0].elements[1].selected = true;
window.document.forms.f.checked = true;
window.document.getElementById("txt").value = "Modified";
}
```

## 使用 javascript: 协议

超链接中的 HTML `href` 属性通常包含用户点击链接时加载的 URL，但通过使用 `javascript:` 协议可以改为执行 JavaScript 代码。

`javascript:` 协议允许将最多 512 字节的短 JavaScript 代码直接包含在 HTML 文档的 `<a>` 元素中，适用于创建动态效果。

包含 JavaScript 代码的字符串应包含双引号，因此代码内部的字符串应包含单引号，以避免混淆浏览器。

在下面的示例中，使用 `javascript:` 协议创建一个警告对话框——单引号包裹一个文本字符串，该字符串与对象属性进行拼接：

```html
<p>
<a href="javascript:alert('You are browsing with\n' + navigator.appName)">Show browser name</a>
</p>
```

使用 `javascript:` 协议受到许多人的反对，但为了完整性将其在此包含。

使用 `javascript` 协议执行 JavaScript 代码段可以为禁用了 JavaScript 的浏览器提供替代方案，向浏览器返回布尔值 `false`。

下面的示例说明了这一点，它调用 `window.open()` 方法（在已启用 JavaScript 的情况下）在弹出窗口中加载指定的 HTML 文档。该代码段向浏览器返回一个 `false` 值，浏览器将忽略 "href" 属性且不会将页面加载到当前窗口。

相反，在未启用 JavaScript 的浏览器中，`onclick` 属性会被忽略，由 "href" 属性指定的 HTML 文档不会在当前窗口中加载。

```html
<p>
<a href="more.html"
onclick="javascript:window.open('more.html','.width=350,height=100');return false">了解更多</a>
</p>
```

> 注意：在此示例中返回 `true` 值而不是 `false`，将导致在启用 JavaScript 的浏览器中页面同时加载到两个窗口中。

## 操作样式属性

网页组件的 `style` 对象包含许多存储其位置和外观信息的属性。JavaScript 可以动态地更改这些属性，以改变其位置和外观，从而创建交互效果。这种技术通常被称为动态 HTML (DHTML)。

在 HTML 中使用的 `<div>` 元素最重要的样式属性可能是 `id`、`top`、`left`、`z-index`、`visibility`、`color` 和 `background-color`。可以通过 JavaScript 赋值新值来动态更改这些样式属性。

此示例中的第一个函数由 `window.onload` 事件处理器调用，用于显示 `<div>` 元素的样式属性。它的 `onclick` 属性被赋值为第二个函数，这样当用户点击该元素时，它的某些样式属性就会改变，并显示新的样式属性值：

```javascript
window.onload = get_styles;

function get_styles() {
  var obj = window.document.getElementById("lyr");
  var str = "ID: " + obj.id + "\n";
  str += "Top: " + obj.style.top + "\n";
  str += "Left: " + obj.style.left + "\n";
  str += "Z-Index: " + obj.style.zIndex + "\n";
  str += "Visibility: " + obj.style.visibility + "\n";
  str += "Background:" + obj.style.backgroundColor + "\n";
  str += "Foreground: " + obj.style.color + "\n";
  alert(str);
}

function restyle() {
  var obj = window.document.getElementById("lyr");
  obj.style.top = "150px";
  obj.style.left = "20px";
  obj.style.zIndex = "20";
  obj.style.backgroundColor = "lime";
  obj.style.color = "blue";
  get_styles();
}
```

## 切换可见性

`style` 对象有一个 `visibility` 属性，可以用 JavaScript 来判断浏览器是否应该显示该对象。将对象属性赋值为 `hidden` 会使对象不可见，而将 `visibility` 属性赋值为 `visible` 则会显示该对象。

该属性在下面的示例中用于控制两个 `<div>` 的可见性。当光标悬停在图像中两个脸之一上时，会从图像映射调用一个 JavaScript 函数，使用适当的气泡图形显示另一个元素。这两个 `<div>` 元素在 HTML 代码中创建时，其 `visibility` 样式属性被设置为 `hidden` —— 因此它们初始时是不可见的。

将光标悬停在图像映射的活动区域上会触发 `mouseover` 事件调用 `toggle()` 函数。该函数传递一个字符串参数（即要操作的元素的 `id` 值）以及一个数值（用于判断该元素是否应该是可见的）。如果传递的值为 "1"，`toggle()` 将把相应对象的 `visibility` 样式设置为“visible”。

将光标移出图像映射的活动区域会触发 `mouseout` 事件再次调用 `toggle()` 函数，同样会传递一个字符串标识符和一个数值。如果传递的值为 "0"，`toggle()` 函数将把相应对象的 `visibility` 样式设置为“hidden”。

```html
<img src="couple.jpg" usemap="#couple" />
<map id="couple" name="couple">
<area shape="rect" coords="41,26,138,143"
onmouseover="toggle('sal', 1)"
onmouseout="toggle('sal', 0)" />
<area shape="poly" coords="244,69,208,132,202,185,227,205,298,171,318,110,247,65"
onmouseover="toggle('har', 1)"
onmouseout="toggle('har', 0)" />
</map>
```

> 注意：避免创建相邻的活动区域 —— 始终留出小间隙，以便让鼠标事件在触发另一个 `mouseover` 事件之前触发。此示例中的区域覆盖了图像中的脸。

```javascript
// 用于切换的函数
function toggle(str, n) {
  // 存储对象的变量
  var obj;
  // 获取对应的对象
  obj = window.document.getElementById(str);
  // 设置可见性状态
  obj.style.visibility = (n == 1) ? "visible" : "hidden";
}
```

## 插入内容

JavaScript 使用 `innerHTML` 属性动态地向元素插入内容。下面的示例通过 `window.onload` 事件在 `<div>` 中显示时间。

```javascript
// 显示时间的函数
function tick() {
  // 创建 Date 对象
  var now = new Date();

  // 提取时、分、秒
  var hh = now.getHours();
  var mn = now.getMinutes();
  var ss = now.getSeconds();

  // 确保是两位
  if(hh <= 9) hh = "0" + hh;
  if(mn <= 9) mn = "0" + mn;
  if(ss <= 9) ss = "0" + ss;

  // 将当前时间字符串赋值 div
  window.document.getElementById("clock").innerHTML = hh + ": " + mn + ": " + ss;

  // 设置每秒调用一次此
  window.setTimeout("tick", 1000);
}

// 页面加载时启动时钟
window.onload = tick;
```

> **注意**：h1 元素中的内容不受动态变化的影响。

## 制作幻灯片

JavaScript 可以旋转图像以创建一个按设定间隔更新当前图片的自动幻灯片。

在此脚本中，预加载程序将所有图像下载到浏览器缓存中以便随时显示。旋转速度（毫秒）由赋值给变量 `pause` 的值决定。

变量 `n` 是由 `rotate()` 函数增加的计数器，用于显示 `window.imgs[]` 数组中的索引图像。所有图像具有相同的尺寸和较小的文件大小，以避免下载延迟。

> **提示**：只需向 `imgs[]` 数组中添加图像文件名即可扩展幻灯片。

```javascript
// 将间隔存储在变量中
var pause = 3000;
// 创建并初始化计数器
var n = 0;
// 创建文件名数组
var imgs = new Array ("butterfly.gif", "globe.gif", "fish.gif", "clock.gif");

// 预加载所有图像
var preload = new Array();
for(var i = 1; i < imgs.length; i++) {
  preload[i] = new Image();
  preload[i].src = imgs[i];
}
```

```javascript
// 按设定间隔显示每个图片的函数
function rotate() {
  window.document.imgs.pic.src = imgs[n];
  ( n == (imgs.length - 1) ) ? n = 0 : n++;
  window.setTimeout("rotate", pause );
}
```

// 指定 ONLOAD 事件处理器
window.onload = rotate;

> 别忘了：确保所有图像都是显示所需的实际尺寸，这样浏览器在显示时就不需要重新调整大小。

## 处理层移动

可以通过 JavaScript 修改层对象的样式左侧坐标，以便沿 X 轴重新定位该层。

以下示例移动了一个 `id` 为 "boat" 的 `<div>` 层。它包含一幅紧贴窗口左边缘之外的帆船图像。一个定时函数让帆船横跨屏幕。

当帆船消失在窗口右侧边缘时，JavaScript 将图像替换为预先加载的、朝向相反方向的帆船版本。然后脚本会让它从右向左横跨屏幕。

当帆船消失在窗口左侧边缘时，图像恢复为原始版本，并继续从左向右航行，帆船继续往复调头。

`go_right` 变量决定了移动的方向。它最初被设置为 `true`，但在每个极点处都会被反转。

`ext` 变量存储浏览器窗口的当前宽度，以便脚本确定何时反转移动方向。

`set_sail()` 函数最初由脚本调用以启动程序，然后在函数内部对其进行递归调用。

> 热提示：使用此脚本配合动画 GIF 图像可以创建更令人兴奋的结果。

```javascript
// 预加载交换图像
var preload = new Image();
preload.src = "sail_1.gif";
```

```javascript
// 设置初始行驶方向为从左到右
var go_right = true;
```

```javascript
// 一个用于让 <div> 跨越页面的函数
function set_sail() {
  // 获取 div 对象和窗口宽度
  var obj = document.getElementById("boat");
  var ext = document.body.clientWidth;

  // 按设定方向移动 1 像素
  if(go_right) {
    obj.style.left = (parseInt(obj.style.left) + 1) + "px";
  } else {
    obj.style.left = (parseInt(obj.style.left) - 1) + "px";
  }

  // 在右极点处改变方向
  if(parseInt(obj.style.left) >= (ext + 15)) {
    go_right = false;
    document.getElementById("boat_image").src = "sail_1.gif";
  }

  // 在左极点处改变方向
  if(parseInt(obj.style.left) <= -75) {
    go_right = true;
    document.getElementById("boat_image").src = "sail_r.gif";
  }

  // 设置调用此函数的间隔时间
  window.setTimeout("set_sail()", 50);
}
```

```javascript
// 启动程序
set_sail()
```

> 别忘了：此脚本必须包含在 HTML 文档的 `<body>` 部分中 —— 在 `<div>` 元素创建之后。

> 热提示：位置像素值末尾带有 "px"（例如：left="70px"），因此需要使用 `parseInt()` 方法来提取整数部分进行操作。

## 总结

- “动态 HTML”（DHTML）描述了 JavaScript 响应用户操作更改网页组件属性的能力。
- “文档对象模型”（DOM）定义了网页组件的层级关系。
- 页面组件属性可以使用 DOM 层级结构或通过 `window.document.getElementById()` 方法进行访问。
- `javascript:` 协议允许在 HTML 文档中直接包含短小的 JavaScript 代码段。
- 大多数网页组件都有一个 `style` 对象，该对象拥有控制其尺寸、位置和外观的属性。
- JavaScript 可以为网页组件 `style` 对象的任何属性分配新值，以创建 DHTML 效果。
- 网页组件 `style` 属性的 `top`、`left` 和 `zIndex` 属性可以动态更改其位置。
- 通过更改其 `style` 对象的 `color` 和 `backgroundColor` 属性可以动态更改网页组件的颜色。
- 使用 `innerHTML` 属性可以向网页中动态插入内容。
- 可以通过递归调用 `window.setTimeout()` 方法来更改图像源，从而创建网页幻灯片。
- 通过递归调用 `window.setTimeout()` 方法可以创建动画效果。

# 制作富互联网应用程序 (RIA)

本章描述了如何将 JavaScript 与其他现代技术结合使用以创建交互式应用程序。

- 介绍 AJAX
- 发送 HTTP 请求
- 使用响应文本
- 使用 XML 数据
- 创建 RIA
- 编写 RIA
- 执行 RIA

## 介绍 AJAX

最近的创新使得多种 Web 技术能够和谐工作，从而创建富互联网应用程序（RIA），其响应性与桌面应用程序相似。这些组合技术统称为“AJAX”（异步 JavaScript XML），它包含了：

- 基于标准的呈现 —— 使用 HTML
- 动态交互 —— 使用 DOM
- 数据交换 —— 使用 XML
- 异步数据处理 —— 使用 JavaScript

理解 AJAX 并不是一种特定的技术，而是一种技术。为了充分理解 AJAX 的优势，首先要意识到它并不是一种技术，而是一种技术。AJAX 允许用户在不等待页面加载的情况下与服务器进行交互。当服务器返回响应时，AJAX 引擎会处理这些：

AJAX 引擎的核心是一个特殊的 `XMLHttpRequest` 对象，它提供了从 Web 服务器检索 XML 和数据的方法。在 Internet Explorer 7、Safari 和 Mozilla 浏览器中，其完整地址是 `window.XMLHttpRequest`，可以使用 `new` 关键字创建该对象的实例。在早期的 Internet Explorer 中，可以使用 `new ActiveXObject("Microsoft.XMLHTTP")` 创建实例。

请求的性质通过 `XMLHttpRequest` 对象的 `open()` 方法的三个参数定义，指定检索方法、URL 以及一个用于异步请求的布尔值。

然后可以使用 `XMLHttpRequest` 对象的 `send()` 方法将请求发送到服务器 —— 将要发送到服务器的文本作为参数，或使用 `null` 关键字。

最后，`readystatechange` 属性可以指定在接收到服务器响应时调用的事件处理器。此时，`XMLHttpRequest` 对象的 `readyState` 属性赋予 4 表示响应已完成，其 `status` 属性在响应正常时赋予代码 200。

在示例中，使用适用于浏览器的方法创建 `XMLHttpRequest` 对象。它然后使用 "GET" 方法向服务器发送请求，以打开名为 "data.txt" 的纯文件并检索其内容。

第二个函数被指定为响应 `XMLHttpRequest` 对象的 `readystatechange` 事件的事件处理器。它会在服务器响应完成时被调用。在此示例中，事件处理器将 `XMLHttpRequest` 对象的 `readyState` 和 `status` 属性的值赋值给表单元素，并将显示在网页上。

> 热提示：尽管该对象被称为 `XMLHttpRequest`，但它可以用于处理 XML 数据和纯文本。

> 请务必按照此处描述的大小写写此对象名称、其方法和属性，以避免错误。

> 热提示：Google Maps 是一个 AJAX 应用程序。

```javascript
var _http_request = false; // 用于 XMLHttpRequest 对象

function make_request() {
  if (window.XMLHttpRequest) { // IE7, Mozilla
    _http_request = new XMLHttpRequest();
  } else if (window.ActiveXObject) { // IE6
    _http_request = new ActiveXObject("Microsoft.XMLHTTP");
  } else return false;

  _http_request.open("GET", "data.txt", true);
  _http_request.send(null);

  // 指定一个 READYSTATE 事件处理器...
  _http_request.onreadystatechange = show_status;
}

function show_status() {
  window.document.forms[0].elements[0].value = _http_request.readyState;
  window.document.forms[0].elements[1].value = _http_request.status;
}
```

> 请记住：本章中的所有示例都使用了 `XMLHttpRequest` 对象，只有在从 Web 服务器调用时才能进行尝试 - 直接在浏览器中打开示例文件将不会执行。

## 使用响应文本

当 AJAX 引擎使用 `XMLHttpRequest` 对象对文本内容发出成功的服务器请求时，响应会自动存储在对象的 `responseText` 属性中。这意味着 JavaScript 可以轻松地将返回的文本赋予页面组件，从而无需重新加载整个页面即可显示文本。

为了演示这种能力，接下来的示例在上一个示例的基础上进一步请求服务器打开名为 "data.txt" 的文件。`XMLHttpRequest` 对象的 `onreadystatechange` 属性指定了一个事件处理器，该处理器首先通过检查对象的 `status` 和 `readyState` 值来确认请求成功。如果发现请求成功，则存储在 `XMLHttpRequest` `responseText` 属性中的文本被动态赋值给页面中 id 为 "cell" 的单元格组件：

```javascript
var http_request = false; // 用于 HttpRequest

function make_request() {
  if (window.XMLHttpRequest) { // IE7, Mozilla
    http_request = new XMLHttpRequest();
  } else if (window.ActiveXObject) { // IE6
    http_request = new ActiveXObject("Microsoft.XMLHTTP");
  } else return false;

  http_request.open("GET", "data.txt", true);
  http_request.send(null);
  http_request.onreadystatechange = show_text;
}

function show_text() {
  if (http_request.readyState == 4) {
    if (http_request.status == 200) {
      window.document.getElementById("cell").innerHTML = http_request.responseText;
    }
  }
}
```

> 注意：AJAX 可能会让浏览器的后退按钮失效——请提供页面链接用于导航。

## 使用 XML 响应数据

当 `XMLHttpRequest` 成功请求 XML 数据时，响应会自动存储在对象的 `responseXML` 属性中。JavaScript 可以通过 `window.document.getElementsByTagName()` 方法通过 XML 元素访问这些数据。

此示例请求对面列出的 "data.xml" 文件，并将其加载到 `responseXML` 属性中。当用户从下拉列表中选择一个项目时，会在第二个函数中触发 `onchange` 事件，传递的 `selectedIndex` 值减 1（因为数组索引从 0 开始），并用于从给定名称的 XML 元素数组中选择对应的数据。然后将数据动态赋值给页面中 id 为 "cell" 的表格组件：

```javascript
window.onload = make_request; // LOAD 事件处理器
var http_request = false; // 用于 XMLHttpRequest 对象

function make_request() {
 if (window.XMLHttpRequest) { // IE7, Mozilla 
  http_request = new XMLHttpRequest();
 } else if (window.ActiveXObject) { // IE6
  http_request = new ActiveXObject("Microsoft.XMLHTTP");
 } else return false;

  http_request.open("GET", "data.xml", true);
  http_request.send(null);
}

function reveal(n) {
 if((http_request.readyState == 4) &&
  (http_request.status == 200) && (n != 0)) {
  var obj = http_request.responseXML;
  var fname = obj.getElementsByTagName("name")[n-1].firstChild.data;
  var sname = obj.getElementsByTagName("name")[n-1].firstChild.data;
  window.document.getElementById("cell").innerHTML = n + " " + fname + " " + sname;
 }
}
```

> 提示：`getElementsByTagName` 方法形成了一个包含具有给定名称的所有 XML 元素的数组——对应数组中的文本内容通过其 `firstChild.data` 进行访问。

```xml
<?xml version="1.0"?>
<members>
  <name>John</name>
  <name>Ellison</name>
  <name>Sara</name>
  <name>Palmer</name>
  <name>Bob</name>
  <name>Petersen</name>
</members>
```

## 创建 RIA

本章的其余部分将说明如何创建一个运行的富应用程序（RIA），该程序允许根据用户输入动态更新 Web 界面中的数据。HTML 和 CSS 文档创建一个表单和若干空单元格。然后使用上一个示例描述的 AJAX 技术从 XML 文档填充这些数据。

> 提示：表格主体中的空白色单元格为 n0-n14，行合计单元格为 rt1-rt13，列合计单元格为 ct1-ct3，右下角的总计单元格 id 为 gt。

```javascript
window.onload = make_request;
var obj, http_request = false; // 全局变量

function make_request() {
  if (window.XMLHttpRequest) {
    http_request = new XMLHttpRequest(); // IE7
  } else if (window.ActiveXObject) { // IE6
    http_request = new ActiveXObject("Microsoft.XMLHTTP");
  } else return false;

  http_request.onreadystatechange = create_ria;
  http_request.open('GET', 'ajax.xml', true);
  http_request.send(null); // 发送请求
}
```

（部分）
ajax.js

```javascript
function create_ria() {
  if (http_request.readyState == 4) { // 完成
    if (http_request.status == 200) { // OK
      obj = http_request.responseXML; // XML 对象
      populate_cells(); // 填充单元格
    } else alert("HTTP 请求失败");
  }
}

function populate_cells() {
  for (i = 0; i < obj.getElementsByTagName("num").length; i++) {
    document.getElementById("n" + i).innerHTML = obj.getElementsByTagName("num")[i].firstChild.data;
  }
  totalize(); // 调用函数计算单元格合计
}
```

> 提示：ajax.xml 文档中的 15 个数据元素被称为 "num"。该函数遍历这些元素并将数据应用到每个空单元格。

> 请记住：`populate_cells()` 函数结束时会调用另一个函数来计算合计——位于下一页。

## 编写 RIA

一旦空白色表格单元格填充了来自 XML 文档的数据，自定义的 `totalize()` 函数就可以计算行合计和总合计。该函数使用循环通过 `window.document.getElementsByTagName("name")` 方法结合 "num" 与循环迭代次数来访问 XML 对象元素的值。然后将计算出的合计动态赋值给相关的 `window.document.getElementById(id)`：

```javascript
// 计算行和列合计的函数
function totalize() {
  var sum = 0; // 运行总计变量
  var row_number = 1; // 行数
  var col_number = 0; // 列数

  // 遍历所有 <num> 元素
  for (i = 0; i < obj.getElementsByTagName("num").length; i++) {
    sum += eval(obj.getElementsByTagName("num")[i].firstChild.data); // 相加所有
  }

  // 然后显示总计
  document.getElementById("gt").innerHTML = sum;

  // 遍历所有 <num> 元素
  for(i = 0; i < obj.getElementsByTagName("num").length; i++) {
    sum += eval(obj.getElementsByTagName("num")[i].firstChild.data); // 相加行单元格
    if((i+1) % 5 == 0) {
      document.getElementById("rt" + row_number).innerHTML = sum;
      sum = 0; // 并置零
      row_number++; // 开始下一行
    }
  }

  while(col_number != 5) { // add 5 columns 0-4
    // loop through all <num> elements
    for(i = 0; i < obj.getElementsByTagName("num").length; i++) {
      if(i % 5 == 0) { // add every 5th item
        sum += eval(obj.getElementsByTagName("num")[i + col_number].firstChild.data);
      }
    }
    // move along columns
    col_number++; // move along columns
    document.getElementById("ct" + col_number).innerHTML = sum; // display column total
    sum = 0; // then reset to zero
  }
}
```

> 注意：注意 `getElementsByTagName` 方法使用了 "element" 的复数形式，而 `getElementById` 方法使用了单数形式。

## 富有互联网应用

| 1. | 2 | 3 | 4 | 5 | 总计 |
|---|---|---|---|---|---|
| 5.00 | 5.25 | 5.50 | 5.75 | 6.00 | 27.50 |
| 10.50 | 8.00 | 4.25 | 7.50 | 3.75 | 34.00 |
| 2.25 | 10.75 | 4.75 | 5.00 | 9.25 | 32.00 |
| 17.75 | 24.00 | 14.50 | 18.25 | 19.00 | 93.50 |

单元格编辑器
行 [] 列 新值: [] 更新

## 执行 RIA

此 AJAX 程序的最后部分提供了一个函数，当用户点击表单按钮时会被调用。它首先检查用户是否正确输入了行、列和值；然后用新值以及修订后的行、列和总计动态地更新相关的表格单元格：

```javascript
// 用于编辑和更新单元格内容的函数...
function update() {
  var row = document.getElementById("rownum").options.selectedIndex; // 获取选定的行
  var col = document.getElementById("column").options.selectedIndex; // 获取选定的列
  // 获取用户输入的新值
  var new_value = parseFloat(document.getElementById("new_value").value);
  // 确保用户输入了列、行和值
  if(row == 0) {
    alert("请选择行号");
  }
  if(col == 0) {
    alert("请选择列号");
  }
  if(!new_value) {
    alert("请输入新值");
  }
  // 计算目标单元格
  var target = ((row - 1) * 5) + col - 1;
  // 将新值赋值给 XML 对象元素
  obj.getElementsByTagName("num")[target].firstChild.data = new_value;
  populate_cells(); // 显示修订后的单元格值
  totalize(); // 并计算新的总计
  // 最后重置所有单元格表单输入...
  window.document.getElementById("rownum").options[0].selected = true;
  window.document.getElementById("column").options[0].selected = false;
  window.document.getElementById("new_value").value = "";
}
```



## 提示

表单包含名为 `rownum` 和 `column` 的输入，以及一个名为 `new value` 的文本输入。

## 总结

- AJAX 是 “Asynchronous JavaScript And XML”（异步 JavaScript 和 XML）的缩写
- AJAX 是一种使用多种现有技术创建富有互联网应用（RIA）的技术，其响应性与桌面应用程序相似
- AJAX 引擎是使用 JavaScript 编写的 Web 服务器和浏览器之间的中间件
- 与服务器的异步通信不会中断用户与 AJAX 程序的交互
- Internet Explorer 7、Mozilla 和 Safari 浏览器支持 `window.XMLHttpRequest` 对象
- `XMLHttpRequest` 使用其 `open()` 方法指定并使用其 `send()` 方法发送到服务器
- 当从 Web 服务器接收响应时，`XMLHttpRequest` 对象的 `onreadystatechange` 事件会发生
- 使用 `XMLHttpRequest` 对象的 `onreadystatechange` 属性指定一个处理响应的事件处理器
- `State` 和 `status` 属性被赋值为描述 `XMLHttpRequest` 当前状态的值
- `XMLHttpRequest` 的文本响应会自动赋值给其 `responseText` 属性
- `XMLHttpRequest` 的 XML 数据响应会自动赋值给其 `responseXML` 属性
- `getElementsByTagName()` 方法可以创建指定名称的 XML 元素数组
- XML 对象元素内的文本包含在 `firstChild.data` 中

## 索引

### A
- 取消下载 153
- Abort 事件 153
- `XMLHttpRequest("Microsoft.HTTP")` 174
- 添加数组元素 51
- 加法 24
- 添加 HTML 元素 157
- AJAX (异步 JavaScript 和 XML) 10
- `alert()` 函数 26
- AND 运算符 126
- `append()` 方法 18
- 算术运算符 24
- 加 `+` 运算符 24
- 加加并赋值 `+=` 28
- 赋值运算符 28
- 属性 142
- 异步 JavaScript 和 XML (AJAX) 172

### B
- 返回 103
- `background-color` 160
- 反斜杠 15
- 布尔值 14
- `break` 语句 44
- 浏览器 ID 96

### C
- 大写敏感 83
- 大写敏感 11
- Change 事件 150
- 字符代码 87
- 字符位置 82
- 复选框 147
- 选中属性 146
- Click 事件 112
- 时钟 164
- 关闭窗口 160
- 逗号分隔符 11
- 注释 73
- 比较运算符 30
- 等于 `==` 30
- 大于 30
- 大于等于 `>=` 30
- 组件新的
- 组件数组
- 连接字符串
- 条件分支
- 条件运算符 `?`
- `confirm()` 函数
- 构建对象
- `continue` 语句
- 转换为字符串

### D
- 数据类型
- `Date()` 构造函数
- `Date.getDay()` 方法
- `Date.getHours()` 方法
- `Date.getMilliseconds()` 方法
- `Date.getMinutes()` 方法
- `Date.getSeconds()` 方法
- `Date.getTime()` 方法
- `Date.getTimezoneOffset()` 方法
- `Date.getCHours()` 方法
- `Date.set()` 方法
- `Date.toString()` 方法
- 日期和时间
- `Date` 对象
- Click 事件
- 递减
- HTML (Dynamic HTML)
- 除法
- `while` 循环
- `document` 对象
- DOM (Document Object Model)
- 双引号
- 下拉列表 105-106

### E
- `else` 语句
- 电子邮件地址验证
- 等于
- Error 事件
- 转义
- `eval()` 函数
- 事件处理器
- `event.property`
- `event.property`
- 事件对象
- 文档信息
- 提取数字

### F
- `false`
- 填充元素
- Focus 事件
- `for-in` 循环
- 表单属性
- 表单元素
- `frames`
- 函数

### G
- 生成随机数
- `get cookie`
- 全局变量
- 大于等于

### H
- `hasChildNodes()` 方法
- `head` 区域
- 高
- 隐藏值
- 历史
- HTML (HyperText Language)
- HTTP 请求

### I
- `id` 属性
- `if-else` 语句 38
- `if` 语句 36
- `image map` 162
- 增加 24
- `indexOf()` 方法 97
- 不等于 30
- 继承对象 94
- 初始化 40
- `innerHTML` 属性 164
- `isNaN()` 函数 88

### J
- Java 14
- `javascript` 协议 158
- JavaScript 文件 9
- 合并元素

### K
- `Keyboard` 对象 135
- `keyCode` 属性 135
- `KeyDown` 事件 134
- `KeyUp` 事件 134
- 关键字 12

### L
- `length` 属性 160
- 小于等于 49
- LiveScript 8
- `Load` 事件 130
- 本地变量 20
- 位置 102
- 逻辑运算符 26
- `AND &&` 26
- `NOT !` 26
- `OR ||` 26

### M
- `Math` 常数 70
- `Math.E` 70
- `Math.LN10` 70
- `Math.LN2` 70
- `Math.LOG10E` 70
- `Math.LOG2E` 70
- `Math.PI` 70
- `Math.SQRT1` 70
- `Math.SQRT2` 70
- `Math` 方法 70
- `Math.abs()` 72
- `Math.acos()` 72
- `Math.asin()` 72
- `Math.atan()` 72
- `Math.atan2()` 72, 76
- `Math.cos()` 72
- `Math.exp()` 72
- `Math.floor()` 72, 75
- `Math.log()` 72, 73
- `Math.max()` 72, 73
- `Math.min()` 72, 73
- `Math.pow()` 72
- `Math.random()` 72, 76
- `Math.round()` 72, 74
- `Math.sin()` 72
- `Math.sqrt()` 72
- `Math.tan()` 72
- 监控设置 104

## 索引（续）
- 不等于 `!=`
- 小于 `<`
- 大于等于 `<=`
- `!` 26
- 不等于 30
- `%` 24
- `%=` 28
- `&&` 26
- `()` 18
- `*=` 24
- `+` 28
- `++` 24
- `-=` 28
- `/` 24
- `/=` 28
- `<` 24
- `<=` 30
- `=` 30
- `==` 30
- `?` 32
- `{}` 16
- `||` 26
- `Array.join()` 方法 52
- `Array length` 49
- `Array.reverse()` 方法 53
- `Array.slice()` 方法 54
- `Array.sort()` 方法 55
- 数组元素 49
- 赋值文本 144
- 赋值运算符 28
- 加加并赋值 `+=` 28
- 除以并赋值 `/=` 28
- 乘乘并赋值 `*=` 28
- 减去并赋值 `-=` 28
- 递减 `--` 24
- 递增 `++` 24
- 取模 `%` 24

# 目录

- `navigator.platform` 属性 97
- `navigator.plugins` 对象 99
- `description` 属性 99
- `name` 属性 99
- `navigator.userAgent` 属性 96
- `navigator` 对象 96
- `new` 关键字 48, 92
- `NOT |` 运算符 26
- `null` 值 112
- 传递的值 18
- `platform` 96
- 弹出窗口 112
- 预加载 112
- `print` 166
- `prompt()` 函数 37, 11
- 属性 41
- 查询浏览器 96
- 引号 10, 15
- `Object()` 构造函数 92
- `Object.toString()` 方法 86
- 对象 92
- `abort` 事件处理程序 153
- `onblur` 事件处理程序 138
- `onchange` 事件 178
- `onchange` 事件处理程序 150
- `onclick` 事件处理程序 132
- `ondblclick` 事件处理程序 132
- `onerror` 事件处理程序 131
- `onfocus` 事件处理程序 136
- `onkeyup` 事件处理程序 134
- `onload` 事件处理程序 130
- `onmousedown` 事件处理程序 133
- `onmousemove` 事件处理程序 137
- `onmouseout` 事件 162
- `onmouseout` 事件处理程序 136
- `onmouseover` 事件 162
- `onmouseup` 事件处理程序 133
- `onreset` 事件处理程序 151
- `onresize` 事件处理程序 139
- `onsubmit` 事件处理程序 152
- `unload` 事件处理程序 112
- 打开新窗口 136
- 选项 148
- `options[]` 数组 148
- `OR |` 运算符 26
- 单选框按钮 146
- 随机数 76
- `removeChild()` 方法 127
- `reset()` 方法 152
- `Resize` 事件 118
- `resizable` 事件 139
- 响应数据 176
- 相关元素 53
- 丰富互联网应用程序 (RIA) 180
- 创建可行的应用程序 184
- 执行可行的应用程序 182
- 编写可行的应用程序 74
- `rollover` 滚动事件
- 作用域 20
- `script` 块 9
- `script` 标签 9
- 滚动 109
- `selectedIndex` 属性 149
- `selectedIndex` 值 178
- 分号 11
- `setAttribute()` 方法 126
- 设置日期时间 64
- 设置 cookie 120
- 单行注释 11
- 单引号 18
- `pageX` 属性 137
- `pageY` 属性 137
- `parent.window.frames[]` 数组 105
- `parseFloat()` 方法 88
- `parseInt()` 方法 88
- 元素切片 54
- 幻灯片 166
- 元素排序 55
- 状态栏消息 108
- `String.charAt()` 方法 82
- `String.charCode()` 方法 87
- `String.fromCharCode()` 方法 87
- `String.length` 属性 80
- `String.split()` 方法 84
- `String.substring()` 方法 85
- `String.substring(0)` 方法 85
- `String.toLowerCase()` 方法 83
- `String.toUpperCase()` 方法 83
- `style.backgroundColor` 160
- `style.color` 160
- `style.left` 160
- `style.top` 160
- `style.visibility` 160
- `style.zIndex` 160
- `style.attributes` 160
- `background-color` 160
- `left` 160
- `top` 160
- `visibility` 160
- `z-index` 152
- `submit()` 方法 160
- `substring` 85
- 减法 24
- `switch` 语句 39
- 堆叠层 168
- 文本区域 145
- 文本框 144
- `text` 属性 48
- `this` 关键字 94
- 定时器 66
- 定时器函数 168
- 时区 63
- 切换可见性 162
- `toGMTString()` 方法 65
- `top` 160
- `toString()` 方法 65
- `true` 14
- `typeof` 14
- Unicode 值 87, 135
- 协调协调时 62
- `Unload` 事件 130
- URL 地址 102
- `value` 属性 144, 148
- 变量 13
- 变量作用域 20
- `var` 关键字 13
- `visibility` 160, 162
- 可见值 162
- `while` 循环 42
- 空白 104
- `window.alert(text)` 方法 110
- `window.clearTimeout(timeout)` 方法 67
- `window.close()` 方法 112
- `window.confirm(message)` 方法 112
- `window.document.close()` 方法 120
- `window.document.cookie` 对象 126
- `window.document.createNode(node)` 方法 124
- `window.document.domain` 属性 142
- `window.document.forms[index].elements` 对象 163
- `window.document.forms.object` 方法 118
- `window.document.forms.getElementsByById(id)` 119, 178
- `window.document.forms.getElementsByTagName(name)` 166
- `window.document.createElement(node)` 124
- `window.document.open()` 123
- `window.document.referrer` 124
- `window.document.title` 124
- `window.document.URL` 124
- `window.document.write()` 122
- `window.document.tagName` 126
- `anchors` 116
- `forms` 116
- `images` 116
- `links` 116
- `frames[]` 105
- `history.back()` 103
- `history.forward()` 103
- `history.go()` 103
- `location.hash` 102
- `location.pathname` 102
- `location.protocol` 102
- `location.host` 102
- `location.href` 102
- `location.origin` 102
- `location.replace` 102
- `location.moveY` 109
- `location.moveX` 109
- `onload` 130
- `opener` 112
- `prompt` 111
- `screen.availHeight` 104
- `screen.availWidth` 104
- `screen.colorDepth` 104
- `screen.height` 104
- `screen.width` 104
- `scrollBy()` 109
- `scrollTo()` 109
- `setTimeout()` 66
- `status` 108
- `XMLHttpRequest` 174
- `onreadystatechange` 174
- `open()` 174
- `onreadystatechange` 174
- `readyState` 174
- `responseText` 176
- `responseXML` 178
- `send()` 174
- `status` 174
- `events` 130
- `writing` 122
- `z-index` 160
- `z-index` 160
- `XML` 178
- `X axis` 168
- `X coordinate` 137

## 喜欢这本书吗？你也会喜欢这些 Easy Steps 系列

| 标题 | ISBN |
| --- | --- |
| Access 2003 in easy steps | 1840782722 |
| Building a PC in easy steps | 1840782919 |
| C Programming in easy steps, 2nd ed. | 1840783230 |
| C# in easy steps | 1840781505 |
| C++ Programming in easy steps, 2nd ed. | 1840782951 |
| Computing for Seniors in easy steps | 1840782900 |
| CSS in easy steps | 184078301X |
| Digital Photography in easy steps, 5th ed. | 1840782986 |
| Digital Scrapbooking in easy steps | 1840783036 |
| Dreamweaver 8 in easy steps | 1840783125 |
| eBay.co.uk in easy steps, 2nd ed. | 1840783222 |
| Excel 2003 in easy steps | 1840782668 |
| Excel VBA in easy steps | 1840782714 |
| FrontPage 2003 in easy steps | 1840782692 |
| HTML in easy steps, 4th ed. | 1840782544 |
| Illustrator CS2 in easy steps | 1840783028 |
| InDesign CS2 in easy steps | 1840783044 |
| JavaScript in easy steps, 3rd ed. | 184078315X |
| Linux in easy steps | 1840783052 |
| Mac OS X Tiger in easy steps | 1840782943 |
| Online Poker in easy steps | 1840783060 |
| PCs in easy steps, 6th ed. | 184078341 |
