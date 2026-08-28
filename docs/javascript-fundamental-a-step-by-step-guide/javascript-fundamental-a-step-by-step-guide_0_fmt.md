
# JavaScript 基础：循步指南

Steven Bright 的其他作品：

- CorelDraw 教程：CorelDRAW 基础
- 工具与功能列表：工程工具手册
- Microsoft Word 基础：循序渐指南
- 网页设计与开发技术：网站制作方法
- Microsoft PowerPoint 精选：品牌曝光技术
- 破解 Microsoft Excel 技巧：循序渐进的方法
- 变革的浪潮：Adams Aliyu Oshiomhole：为什么他是我们所需的人，创造我们渴望的变革氛围，建立一个成功、伟大且强大的国家

## 如何使用本书

本书是关于 JavaScript 用途（主要用于网站开发）的文档。请遵循循序渐指南以充分利用本书的价值。请逐一章节进行阅读，当你读到最后一页时，你会感到非常满意。你需要一个如 `Dreamweaver` 的网页制作软件或如 `Notepad++` 的网页编辑软件，以及如 `Google chrome` 和 `Mozilla Firefox` 等网页浏览器来预览你的作品。

## 引言

JavaScript 是一种脚本语言。它是一种用于网页、服务器、个人电脑、笔记本电脑、平板电脑、手机等的语言。

它用于为 HTML 页面添加交互性，赋予页面某种动态效果。

脚本语言是一种轻量级的编程语言。它可以插入 HTML 页面中，并且是一种解释型语言（这意味着脚本无需预先编译即可执行）。

脚本可以放在 HTML 文档的 `head` 或 `body` 部分。尽管，通常的做法是将脚本放在 `head` 部分或网页的底部，这样它们就集中在一个地方，且不会干扰页面内容。

当 JavaScript 解释器嵌入到浏览器中时，结果就是客户端 JavaScript。它将 JavaScript 解释器的脚本能力与 Web 浏览器定义的文档对象模型（DOM）结合起来。客户端 JavaScript 为原本静态的网页添加了某种程度的动态行为。

尽管 JavaScript 和 Java 之间有许多明显的外部相似之处，包括语言名称、语法和各自的标准库，但它们是两种不同的语言，在设计上存在巨大差异。

请注意以下几点：

- JavaScript 代码是区分大小写的。
- 单词之间的空格和制表符会被忽略。
- JavaScript 语句以分号（`;`）结束。
- 语句内部的换行符会被忽略。
- 除了第一个单词外，每个单词的首字母要大写，例如 `userFirstName`。
- 要声明变量，请使用关键字 `var` 和变量名：`var username`。为变量赋值，请添加等号和值：`var userName = "Smith"`，`var price = 100`。

## JavaScript 语法

这是一组决定程序员如何编写该语言以及浏览器如何解释该语言的规则。

基本语法如下：

```html
<script>
<!-- - -->
var myDate=new Date();
myDate.setDate(myDate.getDate());
document.write(myDate)
<!-- - -->
</script>
```

### 解析

- `script` 标签（即 `<script></script>`）告诉浏览器在它们之间有一个脚本。
- `<!-- - -->`：这些是 HTML 注释标签，但在 JavaScript 中，它们被用于告诉不支持 JavaScript 或禁用了 JavaScript 的浏览器忽略之间的代码。这防止了代码被输出到用户的浏览器中。
- `Document.write`：这是向用户浏览器中写入实际文本的部分。
- 你的脚本应该存放在哪里：你可以将脚本放在 `head` 部分、`body` 部分，或者作为外部文件。

## JavaScript 在网页开发中的用途

JavaScript 在网页开发中的基本用途是：

1. JavaScript 为 HTML 设计师提供了一个编程工具。
2. JavaScript 可以在 HTML 页面中放入动态文本。
3. JavaScript 可以动态创建页面（如日期或其他数据），它可以生成专为用户量身定制的页面。
4. JavaScript 可以对事件做出反应。
5. JavaScript 可以读取和写入 HTML 元素。
6. JavaScript 可验证输入数据。
7. JavaScript 可用于检测访问者的浏览器。
8. JavaScript 可用于创建 Cookie。

## JavaScript 的类型

JavaScript 有两种类型：内部脚本和外部脚本。

### 内联 JavaScript

示例：

```html
<script>
alert ("WELCOME!");
</script>
```

### 外部 JavaScript

你使用 `<script>` 标签的 `SRC` 属性从外部文件调用 JavaScript 代码。如果你有很多代码或想从多个页面运行外部文件，这将非常有用，因为任何数量的页面都可以调用同一个外部文件。

下面的脚本保存为 `miscript.js` 文件：

```javascript
alert("WELCOME!");
```

然后通过下面的语法放在 `head` 部分闭合 `head` 标签之前调用它：

```html
<script src="miscript.js"></script>
```

### 独立 JavaScript

此脚本在页面加载时加载。下方给出了良好的示例：

```html
<script>
alert('Welcome!')
</script>
```

## 你可以在哪里放置 JavaScript

JavaScript 可以存放在文档的以下部分：

1. 文档的 `head`
2. 文档的 `body`
3. 作为外部 `.js` 文件

## JavaScript 显示方法

JavaScript 可以通过下述的不同方式“显示”数据：我将使用示例来展示使用这些不同方法显示 JavaScript 的可能性。

使用 `window.alert()` 写入警报框：

```html
<script>
window.alert( 24+ 44 );
</script>
```

注意，当测试上述脚本时，会弹出一个警报窗口并显示 24+44 的结果。

使用 `document.write()` 写入 HTML 输出：

```html
<button onclick="document.write(24 + 44)"></button>
```

注意当点击按钮时，会弹出一个显示结果的文档。

使用 `console.log()` 写入浏览器控制台：

```html
<script>
console.log( 24 + 44);
</script>
```

你需要在浏览器中激活 JavaScript 控制台（例如在 Google Chrome 中使用 F12），然后输入上面的脚本，按回车键，它就会给你结果。

使用 `innerHTML` 写入 HTML 元素：

```html
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 24 + 44;
</script>
```

注意：你设置了一个 `id` 属性，脚本通过该 ID 获取结果。

## 弹出框 (POPUP BOXES)

JavaScript 有三种类型的弹出框：

- 提示框 (Alert box)
- 确认框 (Confirm box)
- 输入框 (Prompt box)

### 提示框 (Alert Box)

用于确保信息传递给用户。当提示框弹出时，用户必须点击 `OK` 才能继续。

示例：

```html
<script>
alert("WELCOME!");
</script>
```

### 确认框 (Confirm Box)

用于需要用户验证或确认信息的情况。当确认框弹出时，用户必须点击 `OK` 或 `CANCEL` 才能继续。

示例 1：

```html
<script>
confirm("BUY");
</script>
```

示例 2：

```html
<script>
var r=confirm("press a button");
if ("r==true") {
  x="You pressed OK!";
} else {
  x="You pressed cancel!";
}
</script>
```

### 输入框 (Prompt Box)

用于需要用户在进入页面前输入值的情况。当输入框弹出时，用户必须输入值并点击 `OK` 或 `CANCEL` 才能继续。

示例：

```html
<script>
prompt("BUY", "YES");
</script>
```

### 弹出框换行 (Popup Box Line Break)

用于在弹出框内显示换行。这是通过在值之间插入反斜杠后跟字符 `n` 实现的。

示例：

```html
<script>
alert("Hello\nHow are You?");
</script>
```

## 日期和时间 (DATE AND TIME)

### 时间

```html
<script>
function time(){
  time=new Date()
  document.write(time.getHours() + ":" + time.getMinutes())
}
</script>
```

上述语法被插入到 head 部分，并通过插入到 body 函数中的 `time` 函数调用，如下下方的 `<script>time()</script>`：

欢迎 Sadiku 周一。现在是

```html
<script>
time()
</script>
```

点！

### 日期和时间 (Date and Time)

`Date` 对象用于处理日期和时间。`Date` 对象通过 `Date()` 构造函数创建。

示例：

```html
<script>
var myDate=new Date();
myDate.setDate(myDate.getDate());
document.write(myDate)
</script>
```

上述语法被插入到 head 部分，并通过插入到 body 函数中的 `time` 函数调用，如下方的：

```html
<script>
date()
</script>
```

## 函数 (FUNCTION)

函数是一个当它被调用时就会执行的代码块。函数写在大括号内，前面名前有 `function` 关键字。

示例：

```html
<script>
function myFunction(name, job) {
  alert("Welcome " + name +", the " + job);
}
</script>
```

上述是一个函数，当用户点击下方的 `onclick` 事件处理程序时它会被调用。

```html
<button onclick="myFunction('Sadiku Moday', 'Engineer')">Try it</button>
```

## 事件处理器 (EVENT HANDLERS)

嵌入 HTML 源代码中并根据特定操作执行预定义函数或命令的指令——被称为事件处理器。所有事件处理器都以 `on..` 开头，例如 `onclick`、`onabort`、`onfocus`、`onchange`、`onload`、`onmouseover` 都是事件处理器。

### onload

```html
<script>
function hello(){
  alert(“Hello World!”)
}
</script>
```

上述语法在页面加载时加载一次。

### onclick

```html
<script>
function message(element){
  alert("You clicked the " + element + " element!")
}
</script>
```

上述语法被插入到 head 部分，并通过插入到 body 函数中的 `hello` 函数调用。

```html
<form>
  <input type="radio" name="Radio" onClick="message('Radio Button 1')">Option 1<br>
  <input type="radio" name="Radio" onClick="message('Radio Button 2')">Option 2<br>
  <input type="checkbox" onClick="message('Check Button')">Check Button<br>
  <input type="submit" value="Send" onClick="message('Send Button')">
  <input type="reset" value="Reset" onClick="message('Reset Button')">
  <input type="button" value="Mine" onClick="message('My very own Button')">
</form>
```

### onMouseOver

这当用户在下方事件中的图像上 `onMouseOver` 时告知用户：

```html
<a href="http://index.html" onmouseover="alert('you onMouseOverover the image');return false">
  <img src="images/cdw.jpg" width="100" height="30">
</a>
```

其他还有：

- `onBlur`
- `onMouseOver`
- `onFocus`
- `onChange`

## 使用 JavaScript 在 HTML 文中设置颜色

使用 JavaScript，你可以访问 HTML 文档的颜色设置。你可以更改的元素包括文本颜色、背景颜色，以及未访问的链接、已访问的链接和活动状态的链接的颜色。

```html
<script>
function color(background, foreground, new_link, visited_link, active_link){
  document.bgColor=background
  document.fgColor=foreground
  document.linkColor=new_link
  document.vlinkColor=visited_link
  document.alinkColor=active_link
}
</script>
```

这是普通文本。<br>

<a href="Page2.htm">我还没有访问过 Page 2。</a><br>

<a href="Page3.htm">我已经访问过了</a><br>

<a href="Page4.htm">点击这里</a><br>

<a href="Page5.htm">color('orange','green','blue')">更改颜色</a>

## 重复执行 (REPEATED PERFORMANCE)

在每种语言中，你想要重复相同的命令。

### 使用 While 循环 (Looping with While)

假设你想创建一个 1 到 100 的数字表格，例如：

```html
<script>
function square(){
  // 1-100 的逻辑
}
</script>
```

### 使用 For 循环 (Looping with For)

假设你想创建一个 1 到 100 的数字表格，我们有下面的代码。示例：

```html
<script>
function square(){
  for (var i=1; i<=100; i++){
    document.write("<tr>");
    document.write("<td>" + i);
    document.write("</td><td>" + (i*i));
    document.write("</td></tr>");
  }
}
</script>
```

## 数组 (Array)

`Array` 对象用于在单个变量中存储多个值。它们是具有相同数据类型的数据项的有序堆。JavaScript 数组从零开始。你可以通过引用数组名称和索引号访问并显示数组元素。

示例：

```html
<script>
var country=new Array();
country[0]="Nigeria";
country[1]="China";
country[2]="U.S";
country[3]="Iran";
country[4]="U.K";
country[5]="Russia";
country[6]="Egypt";
country[7]="Cuba";
country[8]="Japan";
document.write(country[7])
</script>
```

**注意**：数组构造函数 `Array()` 中的字母 ‘A’ 必须大写。

### 阶乘表 (Factorial Table)

这用于获取阶乘值，以获取 1 到 18 (<19) 数字的阶乘，我们有下面的代码：

```html
<script>
var fact = 1;
for(i = 1; i <19; i++) {
  fact = fact*i;
  document.write(i + "! = " + fact + "<br>");
}
</script>
```

## 文档格式化 (DOCUMENT FORMATTING)

### 创建新的格式化页面 (Create a New Formatted Page)

```html
<SCRIPT language="JavaScript">
function newPage() {
  var userName = prompt("m:", "")
  document.write("<H1>欢迎 " + userName + "</H1><BR>")
  document.write("<H2>来到你的新主页。</H2>")
}
</SCRIPT>
```

为了允许用户创建新页面，下面的链接调用了 `head` 部分中的 `newPage` 函数：

<A HREF="JavaScript:newPage()">创建页面!</A>

## 创建一个新的格式化窗口

```html
<SCRIPT language = "JavaScript">
function openWin() {
  window.open("index.html", "newWindow",
  "height=100,width=100,")
}
</SCRIPT>
```

为了允许用户创建新页面，下面的链接调用了 `head` 部分中的 `openWin` 函数：

<A HREF="JavaScript:openWin()">新窗口!</A>

## 事件对象 (EVENT OBJECT)

### 文档对象 (Document Object)

使用 `getElementById()` 或 `getElementsByName()`。

#### 使用 `getElementById()`：

```html
<script type="text/javascript">
function getElement() {
  var x=document.getElementById("myHeader")
  alert("I am a " + x.tagName + " element")
}
</script>
```

为了允许用户通过 ID 获取元素，下面的链接调用了 `head` 部分中的 `getElement` 函数：

<h2 id="myHeader" onclick="getElement()">点击查看我是什么元素！</h2>

#### 使用 `getElementsByName()`：

```html
<script type="text/javascript">
function getElements() {
  var x=document.getElementsByName("myInput")
  alert(x.length + " elements!")
}
</script>
```

为了允许用户通过 ID 获取元素，下面的链接调用了 `head` 部分中的 `getElementById` 函数：

<input name="myInput" type="text" size="10"><br />

<input name="myInput" type="text" size="10"><br />

<input name="myInput" type="text" size="10"><br />

<input name="myInput" type="text" size="10"><br />

<input name="myInput" type="text" size="10"><br />

<input name="myInput" type="text" size="10"><br />

### 事件对象：光标的坐标是多少？

```html
<script type="text/javascript">
function show_coords(event) {
  x=event.clientX
  y=event.clientY
  alert("X coords: " + x + ", Y coords: " + y)
}
</script>
```

为了允许用户在页面的任何地方获取光标坐标，下面的链接调用了 `head` 部分中的 `show_coords` 函数：

<body onmousedown="show_coords(event)">

<p>在文档中点击。弹出框将显示光标的 x 和 y 坐标。</p>

</body>

### 事件对象：按下按键的 Unicode 是什么？

```html
<script type="text/javascript">
function whichButton(event) {
  alert(event.keyCode)
}
</script>
```

使用上述代码，在键盘上按下一个按键。弹出框将显示按下按键的 Unicode 值。

<p>在键盘上按下一个按键。弹出框将显示按下按键的 Unicode。</p>

### 事件对象：点击了哪个元素？

```html
<script type="text/javascript">
function whichElement(e) {
  var targ
  if (!e) var e = window.event
  if (e.target) targ = e.target
  else if (e.srcElement) targ = e.srcElement
  if (targ.nodeType == 3) //  Safari bug
  targ = targ.parentNode
  var tname
  tname=targ.tagName
  alert("You clicked on a " + tname + " element.")
}
</script>
```

点击的元素将通过下面的代码获取，该代码调用了 `head` 部分中的 `whichElement` 函数：

<body onmousedown="whichElement(event)">

<p>在文档中某处点击。弹出框将显示你点击的元素的标签名称。</p>

<h3>这是一个标题</h3>

<p>这是一个段落</p>

<img border="0" src="ball16.gif" width="29" height="28" alt="Ball">

</body>

## 鼠标悬停 (IMAGE ROLLVER)

当用户将鼠标悬停在原始图片上时，会更改图片。

<A HREF="URL"

onMouseOver="document.hot.src='images/BUTTON 4.jpg'"

onMouseOut="document.hot.src='images/BUTTON 5.jpg'">

<IMG name="hot" src="hot2.gir"> </A>

## JavaScript 变量 (JAV VARIABLE)

JavaScript 变量是存储数据值的容器。这些变量必须像下面所示进行赋值：

在这个示例中，`m`、`n` 和 `p` 是变量，`m` 和 `n` 将赋予某些值：要变量赋值，使用 `var` 变量，使用 `=` 赋值，设置值例如 `7`，并以分号结束。

### 示例

1. 声明变量：

```javascript
var s = 9;
var w = 39;
var person = "Steven Bright";
var price = $2.99;
var pi = 3.14;
```

2. `var m = 9;`

```javascript
var n = 23 ;
var p = m + n;
```

即 `p = 9+23 = 32`

3. `var m = 12;`

```javascript
var n = 40 ;
var p = m - n;
```

即 `p = 12-40 = -28`

注意：`m` 存储值 `9`，`n` 存储值 `23`，`p` 存储值 `32`。

#### 构建变量名称的规则：

构建变量名（唯一标识符）的通用规则如下，在命名 JavaScript 变量时请务必注意这些点：

- 命名可以包含字母、数字、下划线和美元符号。
- 命名必须以字母开头。
- 命名也可以以 `$` 开头。
- 区分大小写（`y` 和 `Y` 是不同的变量）。
- 不能使用保留字（如 JavaScript 关键字）作为名称。

# JavaScript 运算符 (JAVASCRIPT OPERATORS)

## JavaScript 算术运算符

这些运算符用于对数字（无论是字面量还是变量）进行算术。以下是各种 JavaScript 算术运算符及其功能：

| 运算符 | 说明 |
| :--- | :--- |
| `+` | 加法 |
| `-` | 减法 |
| `*` | 乘法 |
| `/` | 除法 |
| `%` | 取模 |
| `++` | 加增 |
| `--` | 递减 |

## JavaScript 赋值运算符

这些运算符将值赋值给 JavaScript 变量。

| 运算符及其用途 | 说明 |
| :--- | :--- |
| `=` | `x = y` 等于 `x = y` |
| `+=` | `x += y` 等于 `x = x + y` |
| `-=` | `x -= y` 等于 `x = x - y` |
| `*=` | `x *= y` 等于 `x = x * y` |
| `/=` | `x /= y` 等于 `x = x / y` |
| `%=` | `x %= y` |

## JavaScript 字符串运算符

这涉及使用 `+` 运算符（拼接）字符串。

示例：

```javascript
txt1 = "The room" + "is hot";
```

`txt1` 的结果将是 is hot

## 添加字符串和数字

记住，两个两个数字将返回和，但将一个数字和一个字符串将返回一个字符串：

示例：

```javascript
w = "steven" + 2006;
```

`w` 的结果将是 steven2006

## JavaScript 布尔值 (JAVASCRIPT BOOLEANS)

JavaScript 布尔表示两个值之一：即 `true` 或 `false`。这意味着 JavaScript 布尔值是真或假。

示例：

- `Boolean(57>34)` // 返回 true
- `Boolean(45 > 78)` // 返回 false

## 比较和条件

在这种情况下，所有具有“真实”值的都是真，而所有没有“真实”值的都是假。

示例：

1. `var y = 0; Boolean(y);` // 返回 false
2. `var y = null; Boolean(y);` // 返回 false
3. `var y = false; Boolean(y);` // 返回 false

# JavaScript 数学对象 (JAVASCRIPT MATH OBJECT)

JavaScript Math 对象允许你对数字执行各种数学任务。

### Math.round()

这会将数字舍入到最接近的整数：

示例：

```javascript
Math.round(467.9); // 返回 468
```

### Math.min()

`Math.min()` 用于找到一组参数中的最小值：

示例：

```javascript
Math.min(7, 180, 60, 32, 0, -250); // 返回 -250
```

### Math.max()

`Math.max()` 用于找到一组参数中的最大值：

示例：

```javascript
Math.max(7, 180, 60, 32, 0, -250); // 返回 180
```

### Math.random()

这返回一个 0（包含）到 1（不包含）之间的随机数：

示例：

```javascript
Math.random(); // 返回一个随机数
```

### Math.ceil()

这会将数字向上舍入到最近的整数：

示例：

```javascript
Math.ceil(37.3); // 返回 37
```

### Math.floor()

这会将数字向下舍入到最近的整数：

示例：

```javascript
Math.floor(35.9); // 返回 35
```

# JavaScript 在网页之外的使用 (JAVASCRIPT USES OUTSIDE WEB PAGES)

除了 JavaScript 用于 浏览器和服务器外，JavaScript 解释器还嵌入在许多其他工具中，每个这些应用程序都提供了自己的对象模型以访问主机环境。这些工具包括：

## 嵌入脚本语言

以下是使用 JavaScript 实现的：

- Opera 扩展
- Google Chrome 扩展
- Apple 的 Dashboard 小部件
- Microsoft 的小部件
- Yahoo! 小部件
- OpenOffice.org，一个办公应用程序套件，以及其流行的分支 LibreOffice。

## 脚本引擎

以下脚本语言也基于 JavaScript：

- Microsoft 的 Active Scripting 技术支持 `JScript` 作为脚本语言。
- Qt C++ 工具包包含一个用于解释 JavaScript 的 QtScript 模块，类似于 Java 的 `javax.script` 包。
- Java 编程语言在第 6 版本中引入了 `javax.script` 包，其中包含一个基于 Mozilla Rhino 的 JavaScript 实现。

## 应用平台

以下应用平台也基于 JavaScript：

- `Adobe Integrated Runtime` 是一个 JavaScript 运行时，允许开发者创建桌面应用程序。
- `Mozilla platform` 是 Firefox、Thunderbird 以及其他 Web 浏览器的底层平台，使用 JavaScript 实现其各种产品的图形用户界面 (GUI)。
- `GNOME Shell` 是 `GNOME 3` 桌面环境的外壳，也将 JavaScript 设为默认编程语言。

## 结论

JavaScript 作为一种脚本语言，主要用于 Web、Web 应用程序以及数学基础项目的开发，但它在嵌入式脚本语言、脚本引擎以及 `Mozilla platform` 和 `ActionScript` 等应用平台中也有巨大的用途。

感谢阅读我的书。如果您喜欢它，能否请抽空时间在您最喜欢的零售商处给我留个评价？也请告诉您的朋友去他们最喜欢的零售商处购买。

谢谢！

Steven Bright

作者

## 关于作者

Steven Bright 是一位技术专家、图形设计师、Web 开发者和博客作者。他还是以下书籍的作者：

- `CorelDraw How: The Fundamental of CorelDRAW`
- `Tools and Function Lists: Engineering Tools Manual`
- `Microsoft Word Fundamental: A Step by Step Guide`
- `Web Design and Development Technology: Website How`
- `The Best of Microsoft PowerPoint: Brand Exposure Techniques`
- `Hacking Through Microsoft Excel Skills: A Step by Step Approach`
- `The wave of Change: Adams Aliyu Oshiomhole: Why he is the man we need to Create the Atmosphere of Change we Desire to Build a Successful, Great and Powerful Nation`

## 与 Steven Bright 联系

Amazon 作者页面：[`amazon.com/author/stevenbright`](http://amazon.com/author/stevenbright)

Facebook: [`www.facebook.com/steven.bright.9022`](http://www.facebook.com/steven.bright.9022)

博客：

- [`ebookstrati.blogspot.com`](http://ebookstrati.blogspot.com)
- [`computerskillsworld.blogspot.com`](http://computerskillsworld.blogspot.com)
- [`hackingthroughsuccess.blogspot.com`](http://hackingthroughsuccess.blogspot.com)
