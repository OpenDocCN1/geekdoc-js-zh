# JavaScript：绝对初学者编程基础指南（循步渐进 JavaScript 第 1 册）














# 引言

恭喜你购买《JavaScript：零基础学者编程入门》，感谢你的支持。

接下来的章节将讨论你将如何利用 JavaScript 来创造优势。读完本书后，尽管你以前从未用过它，也将学会如何使用 JavaScript。你可能无法做到一切，但你将掌握基础知识。

市场上有许多关于这个主题的书，再次感谢你选择这一本！我们尽力确保它包含尽可能有用的信息，请尽情享受！

# 什么是 JavaScript?

编程中使用的语言之一是 JavaScript。它经常被用于设计网页，使其能够与用户进行交互。用户的计算机无需下载任何内容即可运行 JavaScript。很多时候，JavaScript 可以用于创建测验和投票。

作为一种高级程序，JavaScript 是动态的、无类型的且解释型的。在你通常在网上看到的所有内容中，是用 JavaScript 或另外两种技术创建的。许多主流浏览器、电子邮件服务器和网站都运行在 JavaScript 代码上。

JavaScript 包含原型的一等函数，这使其成为一种多范式语言。




JavaScript 实际上并不是 HTML 代码。在你编写 JavaScript 代码时，你需要允许浏览器理解你正在向 HTML 中输入 JavaScript。JavaScript 的函数是 `<script>`。`<script type = “text/javascript”> <script>` 函数将允许页面确切知道 JavaScript 代码从哪里开始到哪里结束。

## 示例

```html
<<html>>
<head>
<title> 我的 JavaScript 页面 </title>
</head>
<body>
<script type = “text/javascript”>
Alert (“Welcome to my world!!!”);
</script>
</body>
</html>
```

`alert` 单词会在你的屏幕上弹出一个提示框。为了让它消失以便你继续正在做的工作，你必须点击“ok”。当浏览器需要识别代码为 JavaScript 时，会输入 `alert` 命令。每当你没有在代码中放置 `<script>`，浏览器都会认为你输入的内容是普通文本。你可以在 HTML 编写的文档的 `head` 和 `body` 部分中都放置 JavaScript。你应该尝试将尽可能多的代码保留在 `head` 部分。

## 第一个脚本

在使用 JavaScript 编写第一个程序之前，你不仅需要知道要把代码放在哪里，还需要了解更多事情。JavaScript 代码行必须以分号结束。所有代码都可以放在同一行，而不必担心破坏其性能。尽管这不会影响代码的性能，但它会破坏你脚本的外观。你的文本应该放在一组引号内。当你忘记给文本加引号时，它会被视为变量。大写字母和小写字母的含义不同。大写字母应该只放在正确的位置，以免弄乱你的脚本。

## 示例

```html
<<html>>
<head>
<title> 我的 JavaScript 页面 </title>
</head>
<body>
<script type = “text/javascript”>
</script>
Document.write (“Welcome to my world!!!”);
</script>
</body>
</html>
```

`Document.write` 将告诉用户将括号中的内容放入文档中。你将获得类似于 Python 测试文件中的 Hello World! 的输出。

## 示例

```html
<<html>>
<head>
<title> 我的 JavaScript 页面 </title>
</head>
<body>
Hello!!! <br>
<script>
Document.write (“Welcome to my world!!!”);
</script>
Enjoy your stay…<br>
</body>
</html>
```

输出：
Hello!!!
Welcome to my world!!!
Enjoy your stay…

文本将写入它在 HTML 代码中所在的位置。许多 HTML 标签是用 `document.write` 编写的。

## 大写字母

在 JavaScript 中，`yourname` 和 `YOURNAME` 是两个不同的变量。

## 示例

```html
<<html>>
<head>
<title> 我的页面 </title>
</head>
<body>
<script>
myvalue =2;
myvalue =5;
result = myvalue + myvalue;
document.write(result) ;
</script>
</body>
</html>
```

## 示例

```html
<<html>>
<head>
<title> 我的页面 </title>
</head>
<body>
<script>
myvalue =2;
MyValue =5;
result = myvalue + MyValue;
document.write(result) ;
</script>
</body>
</html>
```

两者的变量都是不一样的，因此它们会有不同的输出。不要混合使用语法。你使用哪种语法并不如你在整个代码中保持一致重要。

## 弹出窗口

使用 JavaScript 时你会得到三个弹出框：警告框（alert）、确认框（confirm）和提示框（prompt）。

### Alert（警告）

语法将提示你输入的文本。你需要点击“ok”继续。你将被通知必须知道的信息。

### Confirm（确认）

此框用于确认你的文本。你需要点击“ok”或“cancel”。你将被强制接受某些东西。点击“ok”时，值为 true。点击“cancel”时，值将为 false。

## 示例

```javascript
If (confirm(“Do you agree”)) {alert)”You agree”)}
Else(alert (“You do not agree”)) ;
```

### Prompt（提示）

此框将你的文本与默认值进行提示。你必须点击“ok”或“cancel”。在继续访问页面之前，你必须输入一些内容。“okay”将返回输入的内容。“cancel”将表示返回为空。

## 示例

```javascript
Username = prompt (“Please enter your name” , “Enter your name here”) ;
```

# JavaScript 语法

语法是关于 JavaScript 代码如何构建的基础规则。

## 程序

程序将包含一组指令列表，规定计算机程序需要执行的内容，以便程序或网站正常运行。这些指令被视为语句。这些语句由分号分隔。

## 示例

```javascript
Var x = 5;
Var y = 7;
Var z = x + y;
```

JavaScript 程序将在网络浏览器内部执行。

## 语句

JavaScript 语句包含五个部分：关键字、值、运算符、注释和表达式。

## 值

有两种不同的值类型：固定值和变量。固定值也称为字面量。

## 字面量

在编写固定值时有规则。固定值可以使用小数点。

## 示例

```
10.50
```

字符串位于双引号或单引号内。

## 示例

```
“Jane Doe”
'Jane Doe'
```

## 变量

存储数据的变量是定义。`Var` 告诉 JavaScript 这是一个变量。

## 示例

```javascript
Var x;
X = 6;
```

## 运算符

运算符用于为变量赋值。赋值运算符是等号。

## 示例

```javascript
Var x = 8
Var y = 9
```

你也可以使用算术运算符，如加法、减法、乘法和除法。

## 表达式

运算符、变量和值的组合构成表达式。计算值的过程称为求值。

## 示例

```
10 * 20
```

输出将是 200。表达式也可以包含变量。

## 示例

```javascript
x = 5
```

值可以是数字或字符串类型。

## 示例

```
“Jane” + “Doe”
```

输出是 Jane Doe

## 关键字

关键字标识需要执行的动作。`Var` 告诉浏览器创建一个变量。

## 示例

```javascript
Var x = 6 + 8;
Var y = x * 15;
```

## 注释

所有注释都不会被执行。代码后面的双斜杠是注释。注释会被忽略，因为它们是为了帮助程序员理解编写的代码。

## 示例

```javascript
Var x = 9; //我将被执行以给你输出。
// var x = 7; //这不会被执行，因为它前面有双斜杠，因此它只是一个注释。
```

## 标识符

标识符是 JavaScript 中发现的各种事物的名称。标识符命名各种变量、函数、标签和关键字。合法名称与其他任何编程语言规则相同。起始字符必须是美元符号、下划线或字母。后面的字符可以是任何符号、数字或字母。数字不允许作为标识符的首字母，因为 JavaScript 会认为数字而不是名称。

## 大写敏感

标识符对大小写敏感。像 `middleName` 和 `middlename` 这样的变量是不同的变量。

## 示例

```javascript
lastName = “Mann”;
lastname = “Johnson”;
```

然而，`var` 和 `VAR` 是相同的。

## 变量连接

通常有 3 种连接单词形成单个变量的方法：

### 字符

连字符（如 `My-name-is`）在 JavaScript 中是不允许的。它们被保留用于减法。

### 下划线

`My_name_is`

### 驼峰命名法

有两个或多个大写字母，如 `myNameIs`。想象驼背上的峰。大多数程序员会让第一个字母小写。

## 字符集




JavaScript 包含一组 Unicode 字符集。大部分字符、标点符号和符号将由 Unicode 覆盖。

# JavaScript 变量

变量是带有名称的盒子。变量用于存储值。你盒子的名称将是变量名。盒子的内容将与变量有关。这就像计算机的内存，信息被放在内存中，就像内容被放在变量中。变量将引用你给它的名称。

## 示例

```html
<<html>>
<head>
<title> 我的 JavaScript 页面 </title>
</head>
<body>
<script>
Myname = “Susann” ;
Document.write(myname) ;
</script>
</body>
</html>
```

你想要存储在变量中的文本需要包含在引号中。这将允许程序区分变量和普通文本。

## 示例

```html
<html>
<head>
<title> 我的 JavaScript 页面 </title>
</head>
<body>
<script>
Susann = “my first name” ;
Myname = Susann ;
Document.write (myname) ;
</script>
</body>
</html>
```

输出结果是：

*   `Susan` 是变量
*   它位于 `myname` 变量中
*   `myname` 将被置于文档
*   最终结果是 my first name

## 赋值给变量的值

将值赋予变量的最常用方法是等号。

## 运算符

像 `++` 和 `--` 这样的运算符是你最可能不想使用的。你可以使用其他运算符来完成与这些运算符相同的工作。但它们会让你的代码输入速度更快，因此许多程序员使用它们来使编码运行得更快。运算符 `++` 会增加 1。`--` 会减少 1。百分比符号将返回两个数相除后余数的模。

## 变量比较

你有多种方法可以比较变量。最简单的方法是双等号。当你忘记不使用双等号时，你并没有比较变量。列在左侧的变量将被赋值右侧列的值。

## 示例

```javascript
If (firstname = “Susann”) {alert(“Nice name!!!”)}
```

这是常见的，但它会导致你的脚本运行方式不同。你可以在 JavaScript 中使用你在小学学过的运算符：

*   `==` 等于
*   `!=` 不等于
*   `<` 小于
*   `>` 大于
*   `<=` 等于或小于
*   `=` 等于或大于

# JavaScript 中的函数

JavaScript 中的函数将被封装在代码中，旨在执行特定任务。函数将在每次被调用或请求时执行。

## 示例

```javascript
Function myFunction(p1, p2) {
Return p1 * p2;
// 你的函数将返回 p1 和 p2 的乘积
}
```

## 函数语法

函数由关键字 `function` 定义。名称后跟着一组圆括号。名称将包含数字、下划线、字母和美元符号。它们遵循与变量相同的规则。括号内将用逗号分隔的参数名。所有要执行的代码都将放在花括号中。

## 示例

```javascript
Functionname(parameter1, parameter2, parameter3) {
要执行的代码
}
```

参数是定义函数中已经存在的名称。参数包含函数在被调用时所接受的真实值。参数的行为类似于局部变量。

## 调用

当代码被放入函数中时，它将在被调用后被使用。代码在以下情况下被调用：

*   从脚本中被调用
*   发生事件，例如按钮被点击时
*   它是自调用的

## 返回

代码将到达一个已返回的语句，这意味着它将停止运行。当语句返回到调用语句之后的执行代码中时，代码将被调用。函数将评估返回的值。返回的值将返回给原始调用者。

## 示例

```javascript
Var x = myFunction (4, 3); //此函数已被调用，并将返回值为 x。

Function myFunction(a, b) {
Return a * b; //函数返回 a 乘以 b 的乘积
}
```

`X` 将是 `12`，这将是你的输出。

## 为什么使用函数？

函数将允许代码被复用。代码将被定义一次，然后可以多次使用。相同的代码将使用不同的参数获得不同的结果。

## 示例

```javascript
Function toCelsius (Fahrenheit) {
Return ( 5/9) * (Fahrenheit -32);
}

Document.getElementById(“demo”).innerHTML = toCelsius(77);
```

## 圆括号运算符

要在不使用圆括号的情况下访问函数，你将获得一个定义。

## 示例

```javascript
Function toCelsius( Fahrenheit) {
Return ( 5/9) * (Fahrenheit – 32);
}

Document.getElementById(“demo”). innerHTML = toCelsius;
```

## 函数中的变量

函数可以像变量一样使用。它们将用于公式、赋值和计算。

## 示例

```javascript
Var x = toCelsius(77);
```

 JavaScript 决策

有不同的语句用于决策。

## If 语句

语句将检查条件是否为真或假。条件将是一个表达式。语句将被执行。

### 语法

```javascript
If(condition)
{
语句
}
```

如果有一个语句，将不使用花括号。如果有多个语句，则需要括号。

建议使用花括号，这样你的代码更容易管理和清晰。

## 示例

```html
<script>
If (6 > 2)
{
Document.write( “yes 6 is greater than 2”);
Document.write“<br />” + “JavaScript is easy”);
Document.write(<br />);
}
</script>
```

输出：

Yes 6 is greater than 2.JavaScript is easy.

## 示例

```javascript
If(true)
Document.write (“Ah! A Boolean inside. Also, I am not using curly brackets”);
```

//不使用花括号也可以

## 示例

```javascript
If ( 2 == 4)
{
Document.write (“This is not going to be printed”);
}
```

//由于条件为假，语句将被执行。

## Else 语句

语句将与 if 语句一起使用。当条件为假时，else 语句将被执行。

在使用 else 语句时会去掉花括号。这只有在需要执行单个语句时才会发生。

## 示例

```html
<script>
If 5 > 7
{
Document.write(“True”);
}

Else
{
Document.write(“False”);
}
</script>
```

输出将是 false。

## Else If 语句

有很多条件需要检查，那么将需要大量的 if 语句。if 条件将同时被检查。如果一个条件失败，检查将停止。这就是你使用 else if 语句的时候。

### 语法

```javascript
If(condition)
{
语句
}

Else if (condition)
{
语句
}

Else
{
语句
}
```

当所有条件都失败时，最后的 else 语句将被执行。

## 示例

```html
<script>
Var a = 3;

Var b = 4;

If (a > b)
{
```




```javascript
Document.write(“a is greater than b”);
} else if (a < b) {
  Document.write(“ a is smaller than b”);
} else {
  Document.write(“Nothing worked”);
}
</script>
```

## Switch 语句（Switch）

Switch 语句的作用与 `else if` 语句相同。当存在多个条件时，会使用 `switch` 语句。Switch 语句的性能比 `else if` 语句更好。

### 语法

```java
Switch(expression)
{
  Case value -1: statements; break;
  Case value -2: statements; break;
  Case value 3: statements; break;
  ….
  Case value-n: statements; break;
  Default: statements; break;
}
```

`switch` 语句会评估待检查的语句并查看是否匹配任何 `case`。如果匹配，则将执行 `case` 内部的语句，随后执行 `break` 语句。`Break` 语句可以确保其他 `case` 语句不再执行。

如果一个 `expression` 无法匹配到 `case` 值，则将执行 `default` 情况。无论 `case` 中是什么种类型的语句都不重要。不必须使用大括号。如果 `default` 构建是 `switch` 中找到的最后一个语句，则会省略 `Break` 语句。

## 示例

```javascript
<script>
Var a = 8
Switch(a)
{
  Case 1: document.write(“one”); break;
  Case 2: document.write( “two”); break;
  Case 3: document.write( “three”); break;
  Case 4: document.write( “four”); break;
  Case 5: document.write( “five”); break;
  Default: document.write(“number not found”);
}
// 输出 five
</script>
```

Case 值可以是字符串、字符和数字。

## 示例

```javascript
<script>
Var I = ‘j’;
Switch(i)
{
  Case ‘a’: document.write(“a found”); break;
  Case ‘b’: document.write(‘b found”); break;
  Case ‘c’: document.write(“c found”); break;
  Case ‘j’: document.write(“j found”); break;
  Case ‘string’: document.write(“string found”); break;
  Default: document.write(“nothing found”);
}
// 输出 j found
</script>
```

## 三元运算符（Ternary）

三元运算符是许多程序员使用的运算符。三元运算符有三个操作数。

### 语法

```java
Condition ? if-true-execute-this : if-false-execute-this;
```

如果 `condition` 为真，则将执行冒号之前的语句。如果该语句返回假，则将执行冒号后的语句。不能使用多种语句，因为 JavaScript 不允许这样做。可以使用函数并在发现条件为真或假时对该函数命名来执行多条语句。

## 示例

```javascript
<script>
True ? document.write (“True value found”) : document.write(“False value found”);
Document.write(“<br />”);
// 输出 True value found.
( 6 > 5 && 3 == 2) ? document.write(“True”) : document.write(“False”);
Document.write(“ <br />”);
// 输出 False
Var a = (true) ? 1 : 2;
Document.write(a);
// 输出 1
</script>
```

## 嵌套的 If Else 和 Switch 语句

你可以在另一个条件中放入 `if`、`or`、`else` 或 `switch` 语句。你将将其称为嵌套。`Else, if` 或 `switch` 语句可以嵌套任意深度。但代码会比以前更加复杂。

### 语法

```java
If(condition)
{
  If (other condition)
  {
    Statements;
  }
}
Else
{
  If (other condition)
  {
    Statements;
  }
  Else
  {
    Switch(expression)
    {
      Case value-1: statements; break;
      …
    }
  }
}
```

# JavaScript 中的控制流语句

当你找到一个源文件时，其中的叙述将按照列出的顺序执行，就像阅读书籍一样。控制流语句处理运算符如何在分支、循环、决策中流转，并允许程序基于某些条件的特定代码块正确运行。

## If-Then（条件分支）

`if then` 语句是控制语句中最简单的语句。`if then` 语句仅在求值为为真时才会执行代码段。

## 示例

```java
Void applyBrakes() {
  // “if” 子句：汽车必须在移动
  If (isMoving) {
    // “then” 子句：减小当前速度
    currentSpeed -- ;
  }
}
```

如果 `condition` 为假，控制将移动到下一个 `if then` 语句。如果大括号中的语句被证明是唯一的语句，那么大括号是可选的。

## 示例

```java
Void applyBreaks() {
  // 如上所示，大括号是不必要的
  If (isMoving)
  CurrentSpeed --
}
```

如果你决定省略大括号，`switch` 语句将是脆弱的。如果 `default` 是 `switch` 中找到的最后一个语句，则会省略 `Break` 语句。后续的 `then` 子句会产生错误结果。

## If-Then-Else（条件-分支-否则）

`if-then-else` 语句会在 `if` 子句失败时提供路径。

## 示例

```java
Void applyBreaks() {
  If (isMoving) {
    CurrentSpeed --
  } else {
  }
```

## Switches（Switch 语句）

Switch 语句有多种路径。Switch 语句适用于 `byte`、`char` 和 `int` 类型。

## 示例

```java
Public class SwitchDemo {
  public void main (String[] args) {
    Int month = 8 ;
    String monthString ;
    Switch (month) {
      Case 1: monthString = “January”; break;
      Case 2: monthString = “February”; break;
      Case 3: monthString = “March”; break;
      Case 4: monthString = “April”; break;
      Case 5: monthString = “May”; break;
      Case 6: monthString = “June”; break;
      Case 7: monthString = “July”; break;
      Case 8: monthString = “August”; break;
      Case 9: monthString = “September”; break;
      Case 10: monthString = “October”; break;
      Case 11: monthString = “November”; break;
      Case 12: monthString = “December”; break;
      Default: monthString = “Invalid month”; break;
    }
    System.out.println(monthString);
  }
}
```

`switch` 语句部分是 `switch` 块。`switch` 语句在执行前会评估表达式。所有成功的语句都带有相同的标签。`if-then-else` 语句将用于标记月份。

```javascript
Int month = 8
If (month == 1) {
  System.out.println (“January”)
} else if (month == 2) {
  System.out.println (“February”)
}
```

`if-then-else` 语句用于检查表达式的清晰。`if-then-else` 语句将根据整数、枚举值和字符串值测试表达式。`Break` 语句将结束 `switch` 语句。

控制流将继续执行 `switch` 块之后的注释。如果 `switch` 块发生穿透（未使用 `break`），则所有语句将按照它们出现的顺序执行，无论 case 标签是什么，直到到达列为 `break` 的语句为止。

## 示例

```java
Public class SwitchDemoFallThrough {
  public static void main (String[] args) {
    Java.util.ArrayList<String> futureMonths = New java.util.ArrayList<String> ();
    Int month = 8 ;
    Switch (month) {
      Case 1: futureMonths.add (“January”);
      Case 2: futureMonths.add (“February”);
      Case 3: futureMonths.add (“March”);
      Case 4: futureMonths.add (“April) ;
      Case 5: futureMonths.add (“May”);
      Case 6: futureMonths.add (“June”);
      Case 7: futureMonths.add (“July”);
      Case 8: futureMonths.add (“August”);
      Case 9: futureMonths.add (“September”);
      Case 10: futureMonths.add (“October”) ;
      Case 11: futureMonths.add (“November”);
      Case 12: futureMonths.add (“December”);
      Default: break ;
    }
    If (futureMonths.isEmpty()) {
```





```java
System.out.println (“Invalid month number”) ;
} else {
    For (String monthName : futureMonths) {
        System.out.println (monthName) ;
    }
}
}
```

输出是：8 月至 12 月。代码中不需要放置结尾的断句，因为花已经从 `switch` 语句中消失了。但建议使用 `break`，因为这样修改代码更简单，而且你可以减少错误代码概率。`default` 部分将处理不在 `case` 部分中的值。代码具有包含多个 `case` 的能力。

### Example

```java
Class SwitchDemo2 {
    Public static void main (String[] args) {
        Int month = 2;
        Int year = 2016;
        Int numDays = 0
        Switch (month) {
            Case 1: case 3: case 5:
            Case 7: case 8: case 10:
            Case 12
            numDays = 28
            break ;
            case 4: case 6:
            case 9: case 11:
            numDays = 31;
            break;
            case 2:
            if ((year % 4 == 0) &&
            !(year % 100 == 0))
            || (year % 400 == 0))
            NumDays = 31;
            Else
            numDays= 30;
            break;
            default:
            system.out.println (“Invalid month.”) ;
            break ;
        }
        System.out.println (“Number of Days = “ + numDays) ;
    }
}
```

输出将是 29，因为二月有 29 天。

## Switch Statement Strings

`String` 对象在 `switch` 语句中有其位置。在字符串被放入 `switch` 时，该表达式将与关联 `case` 标签的另一个表达式进行比较。如果 `case` 是小写的且 `case` 标签也是小写的，则 `switch` 可以接受字符串。

### Example

```java
Public class StringSwitchDemo {
    Public static int getMonthNumber(String month) {
        Int monthNumber = 0
        If (month == null) {
            Return monthNumber ;
        }
        Switch (month.toLowerCase()) {
            Case “January”:
            monthNumber = 1
            break ;
```

这将一直持续到所有 12 个月份都以小写列出并关联相应的数字。

## While and Do While Statements

`While` 语句连续执行语句块，直到条件被判定为真。

### Syntax

```java
While (expression) {
    Statement(s)
}
```

`While` 语句将评估表达式并返回一个布尔语句。当发现条件为真时，`while` 块中的语句将被执行。`while` 语句将测试语句并执行它，直到它被证明为假。

### Example

```java
Class WhileDemo {
    Public static void main(String[] args) {
        Int count = 1 ;
        While (count < 11) {
            System.out.println(“ Count is: “ + count) ;
            Count++;
        }
    }
}
```

无限循环通过这种语法在 `while` 语句中实现。

### Example

```java
While (true){
    // your code goes here
}
```

`Do while` 语句也是 JavaScript 的一部分。

### Example

```java
Do {
    Statement(s)
} while (expression) ;
```

区别在于在循环底部评估方程，而不是位于顶部的方程。循环中的每个部分至少会被评估一次。

### Example

```java
Class DoWhileDemo {
    Public static void main(String[] args) {
        Int count = 1
        Do {
            System.out.println (“Count is: “ + count) ;
            Count++;
        } while (count < 11) ;
    }
}
```

## For Statement

该语句将提供了一种迭代范围内数值的紧凑方式。这被称为 `for` 循环，因为它会一直循环，直到设置的条件被满足为止。

### Syntax

```java
For (initialization; termination;
    Increment) {
    Statement(s)
}
```

你应该记住，增量表达式在循环迭代后被调用。该表达式对值进行增加或减少都是可以的。初始化表达式将初始化循环并在循环开始时执行一次。终止将在循环停止时评估为假。

### Example

```java
Class ForDemo {
    Public static void main(String[] args) {
        For (int i=l ; i<11; i++){
            System.out.println (“Count is: “ + i);
        }
    }
}
```

输出是 1-10。

代码将在初始化表达式中说明变量。变量的作用范围从声明延伸到块的结束。`for` 语句也将用于表达式的终止。如果变量是 `for` 语句中的，它将不会在循环外部使用。它将在初始化过程中声明变量。名称 `i`、`k` 和 `j` 用于循环控制。在初始化表达式中声明后，其寿命将缩短且错误数量会减少。`for` 语句也将用于表达式的终止。无限循环这种语法在 `for` 语句中。

### Example

```java
While (true){
    // your code goes here
}
```

`Do while` 语句在 JavaScript 中也是一部分。

### Example

```java
Do {
    Statement(s)
} while (expression) ;
```

区别在于在循环底部评估方程，而不是位于顶部的方程。循环中的每个部分至少会被评估一次。

### Example

```java
Class DoWhileDemo {
    Public static void main(String[] args) {
        Int count = 1
        Do {
            System.out.println (“Count is: “ + count) ;
            Count++;
        } while (count < 11) ;
    }
}
```

## For Statement

该语句将提供了一种迭代范围内数值的紧凑方式。这被称为 `for` 循环，因为它会一直循环，直到设置的条件被满足为止。

### Syntax

```java
For (initialization; termination;
    Increment) {
    Statement(s)
}
```

你应该记住，增量表达式在循环迭代后被调用。该表达式对值进行增加或减少都是可以的。初始化表达式将初始化循环并在循环开始时执行一次。终止将在循环停止时评估为假。

### Example

```java
Class ForDemo {
    Public static void main(String[] args) {
        For (int i=l ; i<11; i++){
            System.out.println (“Count is: “ + i);
        }
    }
}
```

输出是 1-10。

代码将在初始化表达式中说明变量。变量的作用范围从声明延伸到块的结束。`for` 语句也将用于表达式的终止。如果变量是 `for` 语句中的，它将不会在循环外部使用。它将在初始化过程中声明变量。名称 `i`、`k` 和 `j` 用于循环控制。在初始化表达式中声明后，其寿命将缩短且错误数量会减少。`for` 语句也将用于表达式的终止。无限循环这种语法在 `for` 语句中。

### Example

```java
While (true){
    // your code goes here
}
```

`Do while` 语句在 JavaScript 中也是一部分。

### Example

```java
Do {
    Statement(s)
} while (expression) ;
```

区别在于在循环底部评估方程，而不是位于顶部的方程。循环中的每个部分至少会被评估一次。

### Example

```java
Class DoWhileDemo {
    Public static void main(String[] args) {
        Int count = 1
        Do {
            System.out.println (“Count is: “ + count) ;
            Count++;
        } while (count < 11) ;
    }
}
```

## For Statement

该语句将提供了一种迭代范围内数值的紧凑方式。这被称为 `for` 循环，因为它会一直循环，直到设置的条件被满足为止。

### Syntax

```java
For (initialization; termination;
    Increment) {
    Statement(s)
}
```

你应该记住，增量表达式在循环迭代后被调用。该表达式对值进行增加或减少都是可以的。初始化表达式将初始化循环并在循环开始时执行一次。终止将在循环停止时评估为假。

### Example

```java
Class ForDemo {
    Public static void main(String[] args) {
        For (int i=l ; i<11; i++){
            System.out.println (“Count is: “ + i);
        }
    }
}
```

输出是 1-10。

代码将在初始化表达式中说明变量。变量的作用范围从声明延伸到块的结束。`for` 语句也将用于表达式的终止。如果变量是 `for` 语句中的，它将不会在循环外部使用。它将在初始化过程中声明变量。名称 `i`、`k` 和 `j` 用于循环控制。在初始化表达式中声明后，其寿命将缩短且错误数量会减少。`for` 语句也将用于表达式的终止。无限循环这种语法在 `for` 语句中。

### Example

```java
While (true){
    // your code goes here
}
```

`Do while` 语句在 JavaScript 中也是一部分。

### Example

```java
Do {
    Statement(s)
} while (expression) ;
```

区别在于在循环底部评估方程，而不是位于顶部的方程。循环中的每个部分至少会被评估一次。

### Example

```java
Class DoWhileDemo {
    Public static void main(String[] args) {
        Int count = 1
        Do {
            System.out.println (“Count is: “ + count) ;
            Count++;
        } while (count < 11) ;
    }
}
```

## Break Statement

存在两种 `break` 变体。第一个用于终止 `switch` 语句。第二个用于终止循环。

### Example

```java
Class BreakDemo {
    Public static void main(String[] args) {
        Int[] arrayOfs = {32, 87, 3, 589, 12, 1076, 2000, 8, 622, 127, 77, 955};
        Int searchfor = 12;
        Int i;
        Boolean foundIt = false;
        For (i = 0; i < arrayOfs.length; i++) {
            If (arrayOfs[i] == searchfor) {
                foundIt = true;
                break;
            }
        }
        If (foundIt) {
            System.out.println(“found ” + searchfor + “ at “ + i);
        } else {
            System.out.println(searchfor + “ not in the array”);
        }
    }
}
```

Labeled breaks 用于终止嵌套循环。示例将展示如何使用带标签的 `break`。

### Example

```java
Class BreakLabelDemo {
    Public static void main(String[] args) {
        Int[][] arrayOfs = {
            {32, 87, 3, 589},
            {12, 1076, 2000, 8},
            {622, 127, 77, 955}
        };
        Int searchfor = 12;
        Int i;
        Int j = 0
        Boolean foundIt = false;
        Search:
        For (i = 0; i < arrayOfs.length; i++) {
            For (j = 0; j < arrayOfs[i].length; j++) {
                If (arrayOfs[i][j] == searchfor) {
                    foundIt = true;
                    break search;
                }
            }
        }
        If (foundIt) {
            System.out.println(“Found ” + searchfor + “ at “ + i + “, “ + j);
        } else {
            System.out.println(searchfor + “ not in the array”);
        }
    }
}
```

## Continue Statement

`Continue` 语句跳过 `for`、`do-while`、`while` 和 `for` 循环中的迭代。未标记的形式将跳到循环体内部的部分，然后评估主导循环的布尔方程。示例将展示遍历字符串的路径，同时计算字母 `p` 出现的次数。

### Example

```java
Class ContinueDemo {
    Public static void main(String[] args) {
        String searchMe = “Peter Piper picked a “ + “peck of pickled peppers”;
        Int max = searchMe.length();
        Int numPs=0;
        For (int i =0; i<max; i++) {
            if (searchMe.charAt(i) != 'p') {
                continue;
            }
            numPs++;
        }
        System.out.println("Number of p's: " + numPs);
    }
}
```





```java
for (int I = 0; I < max; I++) {
    // 只对 p’s 感
    if (searchMe.charAt(i) != ‘p’) {
        continue;
    }
    // 处理 p’s
    numPs++;
}
System.out.println(found” + numPs + “ p’s in the string. ");
```

输出是 9 个 p。如果你删除了 `continue` 语句，将会有 35 个 p。带有标签的 `continue` 语句将跳过带有标签的外层循环的当前迭代。在下面的示例中，有两个嵌套循环，用于在字符串中搜索子字符串。为了遍历子字符串以及任何可能被搜索的字符串，需要两个嵌套循环。

## 示例

```java
class ContinueWithLabelDemo {
    public static void main(String[] args) {
        String searchMe = “Look for a substring in me” ;
        String substring = “sub”;
        Boolean foundIt = false;
        Int max = searchMe.length() – Substring.length();
        Test:
        for (int I = 0; I <= max; i++) {
            Int n = substring.length();
            Int j = I;
            Int k = 0;
            while (n -- != 0) {
                if (searchMe.charAt(j++) != substring.charAt((k++))) {
                    continue test;
                }
            }
            foundIt = true;
            break test;
        }
        System.out.println(foundIt ? “Found it” : “Didn’t find it”);
    }
}
```

## 返回语句 (Returned Statements)

返回语句位于分支语句的最后。返回语句是当前控制流中的退出方法，当方法首次被调用时将返回到此处。返回语句有两种形式。其中一种的值将被返回，而另一种的值不会返回。要返回一个值，你需要在关键字后面有一个要返回的值。

语法是 `return ++ count;`。

在返回数据类型后，它必须与方法声明的类型相匹配。当方法声明返回值为 `void` 时，返回的形式将不会提供值。

不作为值的值的语法为 `return;`。

## 在 JavaScript 中的位置 (Placement in JavaScript)

JavaScript 在实际放入 HTML 文档时的位置是非常灵活的。不过，有一种首选的方法将其放入文档，以便代码知道它需要执行什么以及何时执行。

*   `<head>` 中的脚本将位于 `</head>`
*   `<body>` 中的脚本将位于 `</body>`
*   `<body> </body>` 和 `<head> </head>` 区域中的脚本
*   `<head>` 部分中的外部文件区域将位于 `</head>`

## Head 部分中的脚本 (Script in the Head Sections)

每当你因为某个事件（例如用户点击鼠标）需要运行脚本时，你必须将脚本放置在 head 部分，以便事件能够正常工作。

## 示例

```html
<html>
<head>
<script type = “text/javascript”>
//! –
function sayHello() {
    alert(“Hello Earth”)
}
// - >
</script>
</head>
<body>
<input type = “button” onclick =” sayHello()” value = “Say Hello” />
</body>
</html>
```

此代码的输出将是 Hello Earth。

## Body 部分中的脚本 (Script in the Body Sections)

当你需要在脚本在页面加载时运行时，以便它能生成页面上的内容，你的脚本需要存放在文档的 body 部分才能正确运行。

## 示例

```html
<html>
<head>
</head>
<body>
<script type = “text/javascript”>
// - -
document.write (“Hello Universe”)
// - - >
</script>
<p> This is web page body </p>
</body>
</html>
```

这段代码的结果将是：
Hello Universe.
This is web page body

## Body 和 Head 部分中的代码 (Code in the Body and Head Sections)

代码可以同时放置在两个部分中，以产生与仅放置在其中一个部分不同的结果。

## 示例

```html
<html>
<head>
<script type = “text/javascript”>
// - -
function sayHello() {
    alert (“Hello people of Earth”)
}
// - - >
</script>
</head>
<body>
<script type = “text/javascript”>
// - -
document.write( “Hello people of Earth”)
// - - >
</script>
<input type = “button” onclick = “sayHello()” value = “Say Hello” />
</body>
</html>
```

你的结果将是 Hello people of Earth。

## 外部文件 (External Files)

当你更深入处理 JavaScript 代码时，你会发现某些情况下，相同的代码将放置在单个网站的多个页面上。你不需要在多个 HTML 文件中使用重复相同的代码。`script` 标签将为你提供将代码存储在外部文件的位置，以便你可以正确地处理 HTML 文件。

## 示例

```html
<html>
<head>
<script type = “text/javascript” src = “filename.js” ></script>
</head>
<body>
…..
</body>
</html>
```

当在外部文件中使用 JavaScript 时，你必须写出：

## 示例

```javascript
function sayHello() {
    alert(“Hello Earth”)
}
```

## Cookies

Cookies 是你用于存储在计算机上的数据。网站通过这种方式获取信息。

## 创建 Cookie (Creating Cookies)

使用 JavaScript，你可以使用 `document.cookie` 创建、删除和读取 Cookie。

## 示例

```javascript
document.cookie = “username = Mary Jane”
```

## 示例

```javascript
document.cookie = “username = Mary Jane; expires Wed 9, 2016 12:01:00 UTC”
```

## 读取 Cookie (Reading Cookies)

JavaScript 使用 `var x = document.cookie` 来读取任何 Cookie。

## 修改 Cookie (Changing Cookies)

Cookie 的修改方式与其创建时一样。

## 删除 Cookie (Deleting Cookies)

当你想要删除 Cookie 时，你需要设置一个参数，使日期已经过去。

## 示例

```javascript
document.cookie = “username = ; expires Sat 01 Jan 1980 00:00:00 UTC”
```

## 字符串 (Strings)

`document.cookie` 看起来像是一个普通的文本字符串，尽管它实际上不是。

### 设置 Cookie 的函数示例

首先必须创建该函数，以便将用户名存储在 Cookie 中。

```javascript
function setCookie(cname, cvalue, exdays) {
    var d = new Date();
    d.setTime(d.getTime() + (exdays * 24 *60 *60 *1000));
    var expires = “expires=” + d.toUTCString();
}
```





`document.cookie = cname + “=” + cvalue + “;” + expires + “;path=/”;`

这些参数将定义 cookie 的名称 (`cname`)，值将是 (`cvalue`)，而过期日期将是 (`exdays`)。cookie 将通过将名称、值和过期日期拼接成字符串来设置。

## 获取 Cookie 的函数

每当你创建一个函数时，返回值将是特定 cookie 的值。

## 示例

```javascript
Function getCookie(cname) {
  Var name = cname +”=”
  Var ca = document.cookie.split(‘;’);
  For (var I = 0; i <ca.length; i++) {
    Var c = ca[i];
    While (c.charAt(o) == ‘ ‘) {
      C = c.substring(1);
    }
    If (c.indexOf(name) == 0) {
      Return c.substring(name.length, c.length);
    }
  }
  Return “”;
}
```

cookie 的名称将被视为参数。为了创建一个变量，你需要名称和文本，以便能够使用 (`cname + “=”`) 进行正确搜索。

`document.cookie` 将通过分号进行分割，得到一个名为 `ca` 的数组。遍历 `ca` 数组将读取提供的每个值。一旦找到 cookie，将返回该值。如果没有找到，则返回 `""`。

## 检查 Cookie

在设置 cookie 后，将显示设置时对应的问候语。如果尚未设置，则不会显示问候语，但会弹出一个提示框询问用户的名称，以便使用 `setCookie` 函数将 cookie 保存长达。

## 示例

```javascript
Function checkCookie() {
  Var username = getCookie (“username”);
  If (username! = “”) {
    Alert( “Welcome again “ + username);
  } else {
    Username = prompt (“Please enter your name:” , “”);
    If (username != “” && username != null) {
      setCookie (“username”, username, 365);
    }
  }
}
```

## 整合在一起

下面的示例将在页面加载时使用 `checkCookie()`。

## 示例

```javascript
Function setCookie( cname, cvalue, exdays) {
  Var d = new Date();
  d.setTime(d.getTime() + (exdays* 24 *60 *60 *1000));
  var expires = “expires=”+d.toUTCString();
  document.cookie = cname + “=” + cvalue + “;” + expires + “;path=/”;
}

Function getCookie(cname) {
  Var name = cname + “=”;
  Var ca = document.cookie.split(‘;’);
  For( var I = 0; I < ca.length; I++) {
    Var c = ca[i];
    While (c.charAt(0) == ‘ ‘) {
      C = c.substring(1);
    }
    If (c.indexOf(name) == 0) {
      Return c.substring(name.length, c.length);
    }
  }
  Return “”;
}

Function checkCookie() {
  Var user = getCookie(“username”);
  If (user != “”) {
    Alert (“Welcome again + user);
  } else {
    User = prompt (“Please enter your name:” , “”);
    If (user != “” && user != null) {
      setCookie( “username”, user, 365);
    }
  }
}
```

# 你用 JavaScript 可以做什么和不能做什么

有些事情你可以用 JavaScript 来的。就像任何其他程序一样，JavaScript 允许你做的事情是有限制的。

## 用 JavaScript 可以做什么？

* 与表单交互
* 提供反馈
* 检测用户正在做什么
* 通知用户某些事项
* 询问某事是否正确
* 让用户输入数据
* 验证停止的脚本
* 转换
* 计算
* 为文档添加内容
* 弹出窗口操作
* DOM 脚本编写
* 注册表单
* 搜索框
* 不断变化的信息
* 表单信息
* 布局问题
* 增强 HTML 界面
* 元素动画

## 你用 JavaScript 不能做什么

* 在没有帮助的情况下在服务器上写文件
* 访问数据库
* 从客户端读取或写入文件
* 关闭它未打开的窗口
* 访问另一个域的网页
* 保护页面源码或图像

# 常见陷阱

* 混淆相等运算符 (`==`) 和不等于运算符 (`!=`)。
* 混淆严格相等运算符 (`===`) 和严格不等于运算符 (`!==`)。
* 因为 JavaScript 基于真假陈述，所以存在两种运算符。
* 当你期望操作数类型相同时，`==` / `!=` 可以工作；如果它们类型不同，这些运算符将尝试强制它们转换。
* 真值（Truthy）和假值（Falsy）是为了假装成布尔值的非布尔表达式设计的。
* 这些值将被评估为假：`NaN`、`False`、`Null`、`0`、空字符串 (`""`)。
* `===` 和 `!==` 比 `==` 和 `!=` 更好。
* `NaN` 不是数字，只在边缘情况下有用。
* 如果你必须...

# 技巧与窍门

## 从不同数组追加元素
更好的选项是通过代码使用原生 JavaScript 排序函数来实现随机排序。

## 字符串修剪函数

JavaScript 和其他编程语言中经典的修剪函数，用于移除字符串中 JavaScript 不会发生的空白字符，以便可以附加到字符串对象上。现代 JavaScript 引擎使用了原生的 `trim()` 函数。





## 验证给定参数是否为数组

注意：如果 `toString()` 方法被重写，你将无法通过此种技巧获得预期的结果。如果你没有在多个帧中工作，你也可以也可以执行 `instanceof`。但是，如果你有不同的上下文，你将得到错误的结果。

## 获取数字数组中的最大值最小值

`Var numbers = [5, 458, 120, -215, 228, 400, 122205, -85411];`

`varmaxInNumbers = Math.max.apply (Math, numbers) ;`

`var minInNumbers = Math.min.apply (Math, numbers) ;`

## 清空数组

`Var myArray = [12, 222, 1000 ];`

`myArray.length = 0; //myArray 将等于[]`

## 不要使用 delete 移除数组中的项

如果你想从数组中删除项，请使用 `splice` 函数而不是 `delete` 函数。当你使用 `delete` 函数时，它会将该项替换为 `undefined` 变量，而不是从数组中删除它。

## 使用 length 截断数组

`Var myArray = [12, 222, 1000, 124, 98, 10];`

`myArray.length = 4; //myArray 将等于 [12, 222, 1000, 124]`

## 在条件判断中使用 AND/ OR 逻辑

逻辑 OR 也用于为函数参数中的函数设置默认值。

## 使用 map() 函数循环遍历数组项

`Var squares = [1,2,3]. Map(function (val) {`

`Return val*val`

`)) ;
//squares 将等于 [1, 4, 9]`

## 将数字舍入到小数位

`Var num = 2.4432432;`

`Num = num.toFixed(4); //num 将等于 2.4432`

`toFixed()` 函数将返回字符串而不是数字。

## 浮点数问题

`0.1+0.2` 将等于 `0.3000000000000004`。你需要了解的知识是，JavaScript 中的所有数字都是内部用 64 位表示的浮点数。

## 在 for-in 循环时检查对象的属性

此代码段有助于避免遍历对象的属性。

`For (var name in object) {`

`If (object.hasOwnProperty(name)) {`

`// 对 name 执行某些操作`

`}`

## 逗号运算符

`Var a = 0;`

`Var b = (a++, 99) ;`

`Console.log(a); // a 将等于 0`

`Console.log(b); // b 将等于 99`

## 缓存计算或查询的变量

jQuery 选择器将缓存 DOM 元素

`Var navright = document.querySelector('#right');`

`Var navleft = document.querySelector('#left');`

`Var navup = document.querySelector('#up');`

`Var navdown = document.querySelector('#down');`

## 在传递给 isFinite() 之前验证参数

`isFinite(0) ; // false`

`isFinite("10") //true`

## 避免在数组中使用负索引

`Var numbersArray = [1, 2, 3, 4, 5];`

`Var from = numbersArray.indexOf("foo"); //from 等于 -1`

`numbersArray.splice(from,2); //将返回 [5] 任何通过 splice 的参数都不应为负数。`

# 循环

当一个操作被重复执行时，它被视为循环。循环包含若干条指令，在条件返回真或假之前（取决于需要），继续执行相同的代码块。为了控制循环，你需要一个在每次循环重复时增加或减少的变量。JavaScript 中使用了两种循环类型：`For` 循环和 `while` 循环。语句在循环循环时执行效果最佳。如果你使用 `break`，可以 `continue` 循环内部的语句。

## For 循环

`For` 循环将一直执行直到条件返回假。语法与每种编程语言相同。`for` 循环有三个参数：

```
For (initialization; condition; increment)
{
    // 语句
}
```

循环语句只有在以下情况下才能执行：
- 语句和控制进入第二步。
- 执行等式且条件为真。如果值为假，则将执行语句，然后终止循环。
- 执行开头的表达式。这将初始化一个或多个不同的循环，因为它们在通过语法时允许来自各种复杂性和程度的表达式。
- 增量定义被移除、更新或执行。

## 示例

```html
<script type="text/javascript">
Document.write("<h1>乘法表</h1>");
Document.write("<table border=2 width=50%");
For (var I = 1; I <=9;i++) { //这是外层循环
Document.write("<tr>");
Document.write("<td>" + I + "</td>");
For (var j = 1; j <= 9; j++) { //这是内层循环
Document.write("<td>" + I * j + "</td>");
}
Document.write("</tr>");
}
Document.write("</table>");
</script>
```
*(注：原文示例中的 HTML 结构存在未闭合标签，翻译时保持了逻辑并微调了可读性)*

`For` 循环将一直执行直到条件返回假。语法与每种编程语言相同。

## While 循环

While 循环在 JavaScript 中很常见。while 语句会重复循环直到条件为真。如果条件为假，语句将停止并传递到循环后面的语句。

### 语法

```
While (condition)
{
    // 语句
}
```

下面的示例将展示如何定义一个从 `I = 0` 开始的循环，直到 `I` 变量大于 10。每当通过循环时，`I` 都会增加一次。

## 示例

```javascript
<script type="text/javascript">
Var I = 0;
While (I<=10) // 输出 0 到 10 的值
{
Document.write(I + "<br>");
I++;
}
</script>
```

无论你当前编写什么循环，都需要确保条件最终会变为假。如果没有发生这种情况，循环将永远不会终止并无限运行。

## Break 和 Continue

有时循环在启动时没有任何真/假条件的限制。但是，位于括号内的语句将决定何时退出循环。在循环内部可以找到两条语句：`break` 语句和 `continue` 语句。

`continue` 语句将在任何 `for` 或 `while` 循环中停止语句块，并在下一个起始点继续循环。`break` 语句将停止 `while` 或 `for` 循环，并在执行循环后面的脚本（如果有的话）。

## 示例

```javascript
<script type="text/javascript">
Document.write("<p><b>使用 break 语句的示例：</b></p>");
Var I = 0;
For (i=0; i<=10; i++) {
    If (i==3){break}
    Document.write ("数字是 " +i);
    Document.write("<br />");
}
</script>
```





```javascript
Document.write(“<p><b>使用 continue 语句的示例： </b><p>”);

Var I = 0;

For (I = 0; i <= 10; i++) {
  If ( i==3) (continue)
  Document.write(“数字是 “ + i);
  Document.write(“<br />”)
}
```

# JavaScript 中的运算符

表达式包含运算符和操作数。操作数是表达式中使用的数字，运算符是算术符号。JavaScript 支持的运算符类型有：

* 算术
* 比较
* 逻辑
* 位运算
* 赋值
* 条件
* Typeof

## 算术

* 加法：将两个操作数相加。
* 减法：从第一个操作数中减去第二个操作数。
* 乘法：将两个操作数相乘。
* 除法：将被除数除以除数。
* 取模：余数是除法后剩余的整数。
* 增增：整数加一。
* 递减：整数减一。

## 示例

```html
<html>
<<body>
<script type = “text/javascript”>
<! - -
Var a = 33;
Var b = 10;
Var c = “test”;
Var linebreak = “<br />”;

Document.write(“a + b =”);
Result = a + b;
Document.write (result) ;
Document.write(linebreak);

Document.write (“ a – b = “);
Result = a – b;
Document.write(result);
Document.write(linebreak);

Document.write(“a / b = “);
Result = a / b;
Document.write(result);
Document.write(linebreak);

Document.write(“ a % b = “);
Result = a % b;
Document.write(result);
Document.write(linebreak);

Document.write( “a + b + c = “);
Result = a + b + c;
Document.write(result);
Document.write(linebreak);

A = ++a;
Document.write (“++a = “);
Result = ++a;
Document.write(result);
Document.write(linebreak);

B = --b
Document.write(“ - - b = “);
Result = - - b;
Document.write(result);
Document.write(linebreak);

// 给变量设置不同的值并尝试一下。
</</body>>
</</html>
```

你的输出将会是：
a = 43
b = 23
c = 34
b = 3
++a = 35
--b = 8

## 比较

* 等于：检查两个操作数的值以判断是否相等。如果相等，则条件为真（true）。
* 不等于：检查操作数是否相等，如果不相等，则条件为真（true）。
* 大于：表示左侧的值大于右侧的值，如果是，则该条件为真。
* 小于：表示左侧的数字小于右侧，如果是，则条件为真。
* 大于等于：检查左侧的值是否大于或等于右侧的值。如果是，则条件为真。
* 小于等于：表示左侧的值小于或等于右侧的值，如果是，则条件为真。

## 示例

```html
<html>
<body>
<script type = “text/javascript”>
<! - -
Var a = 10;
Var b = 20;
Var linebreak = “<br />”;

Document.write((a == b) => “);
Result = (a == b);
Document.write(result);
Document.write(linebreak);

Document.write( (a < b) => “);
Result = (a < b);
Document.write(result);
Document.write(linebreak);

Document.write( (a > b) => “ );
Result = (a > b);
Document.write(result);
Document.write(linebreak);

Document.write (a != b) => “);
Result = a != b);
Document.write(result);
Document.write(linebreak);

Document.write( (a >= b) => “);
Result = (a >= b);
Document.write(result);
Document.write(linebreak);

Document.write( (a <= b) => “);
Result = (a <= b);
Document.write(result);
Document.write(linebreak);
</script>
</</body>>
</html>
```

此示例的输出将会是：
a == b = false
a < b = true
a > b = false
a != b = true
a >= b = false
a <= b = true

## 逻辑

* 逻辑与（AND）：表示两个操作数都为非零。如果是，则条件为真。
* 逻辑或（OR）：表示至少有一个操作数为非零。如果发现一个是非零，则这是一个真命题。
* 逻辑非（NOT）：根据操作数的状态反转逻辑状态。如果条件为真，由于“非”操作将变为假。

## 示例

```html
<html>
<body>
<script type = “text/javascript”>
<! - -
Var a = true;
Var b = false;
Var linebreak = “<br />”;

Document.write(a && b);

Result = (a && b);
Document.write(result);
Document.write(linebreak);

Document.write(a || b = true);
Result = (a || b);
Document.write(result);
Document.write(linebreak);

Document.write(a || b);
Result = (a || b);
Document.write(result);
Document.write(linebreak);

Document.write(!a = false);
Result = (!a);
Document.write(result);
Document.write(linebreak);
</script>
</body>
</html>
```

上述示例的结果为：
a && b = false
a || b = true
!a = false

## 位运算

* 位与（AND）：对操作数进行位与运算。
* 位或（OR）：对操作数进行位或运算。
* 位异或（XOR）：对操作数进行位异或运算。
* 位非（NOT）：对位进行取反。
* 左移：将操作数向左移动指定的位数。
* 右移：将操作数向右移动指定的位数。

## 示例

```html
<html>
<body>
<script type = “text/javascript”>
<! - -
Var a = 2; // 二进制为 10
Var b = 3; // 二进制为 11
Var linebreak = “<br />”;

Document.write(a & b = “);
Result = (a & b);
Document.write(result);
Document.write(linebreak);

Document.write(a | b = “);
Result = (a | b);
Document.write(result);
Document.write(linebreak);

Document.write(a ^ b = “);
Result = (a ^ b);
Document.write(result);
Document.write(linebreak);

Document.write(~b = “);
Result = (~b);
Document.write(result);
Document.write(linebreak);

Document.write(a << b = “);
Result = (a << b);
Document.write(result);
Document.write(linebreak);

Document.write(a >> b = “);
Result = (a >> b);
Document.write(result);
Document.write(linebreak);
</script>
</body>
</html>
```

结果：
a & b = 2
a | b = 3
a ^ b = 1
~b = -4
a << b = 16
a >> b = 0

## 赋值

* 赋值：将右侧的值赋值给左侧。
* 加法赋值：将右操作数加到左侧，然后赋值给左侧。
* 减法赋值：从左侧减去右侧的值并赋值给左侧。
* 乘法赋值：将操作数相乘后将结果赋值给左侧。
* 除法赋值：将左侧除以右侧并将结果赋值给左侧。
* 取模赋值：对两个操作数取模并将结果赋值给左侧。
* 位赋值运算符变为 `<<=`、`>>=`、`&=`、`|=` 和 `^=`。

## 示例

```html
<html>
<body
<script type = “text/javascript”>
<! - -
Var a = 33;
Var b = 10;
Var linebreak = “<br />”;

Document.write(“a 的值变为 (a = b) => ”);
Result = (a = b);
Document.write(result);
Document.write(linebreak);

Document.write(“a += b => ”);
Result = (a += b);
Document.write(result);
Document.write(linebreak);

Document.write(“a *= b => ”);
Result = (a *= b);
Document.write(result);
Document.write(linebreak);
```





```javascript
Result = (a /= b);
Document.write(result);
Document.write(linebreak);
Document.write (“Value of a => (a %= b) => “);
Result = (a %= b);
Document.write(result);
Document.write(linebreak);
```

输出:
```
Value of a => (a =b) = 10
Value of a => (a += b) = 20
Value of a => (a -=b) = 10
Value of a => (a *= b) = 100
Value of a => ( a /= b) = 10
Value of a => (a %= b) = 0
```

## 条件判断

- 条件运算符会在语句执行之前对表达式进行求值以得到真或假值，具体的执行语句取决于求值的结果。
- 如果条件为真，则语句的值将是 x；如果不是，则你将移动到另一个语句。

## 示例

```html
<html>
<body>
<script type = “text/javascript”>
<! - -
Var a = 10;
Var b = 20;
Var linebreak = “<br />”;
Document.write (“ ((a >b) ? 100 : 200) => “);
Result = (a > b) ? 100 : 200;
Document.write(result);
Document.write(linebreak);
Document.write (“ (( a < b) ? 100 : 200) => “);
Result = (a < b) ? 100 : 200;
Document.write(result);
Document.write(linebreak);
// - - >
</script>
</body>
</html>
```

结果如下：
```
(( a > ) ? 100 : 200 => 200
((a < b) ? 100 : 200 => 100
```

## Typeof

- `Typeof` 运算符是一一元运算符。它位于单个操作数之前。操作数可以是任何类型。
- 结果将变成一个字符串，显示所使用的数据类型。
- 只有当根据求值结果为真或假时，`Typeof` 运算符才会评估字符串、数字和布尔值。
- 使用 `typeof` 运算符返回的值：`Number = number`、`Object = object`、`Null = object`、`String = string`、`Function = function`、`Undefined = undefined`。

## 示例

```html
<html>
<body>
<script type “text/javascript”>
<! - -
Var a = 10
Var b = “String”;
Var linebreak = “<br />”;
Result = (typeof b == “string” ? “B is String” : “B is Numeric”);
Document.write( “Result => “);
Document.write(result);
Document.write(linebreak);
Result = (typeof a == “string” ? “A is String” : “A is Numeric”);
Document.write(“result => “);
Document.write(result);
Document.write(linebreak);
// - ->
</script>
</body>
</html>
```

结果：
```
Result => B is String
Result => A is Numeric
```

# 使用 JavaScript 打印页面

你可能需要一个允许将页面内容打印到实际打印机的按钮。JavaScript 有一个可以实现此点的函数。`window.print()` 函数将打印你当前查看的任何页面。此函数也被认为是一个 `onclick` 事件。

## 示例

```html
<html>
<head>
<script type = “text/javascript”>
<! - -
// - - >
</script>
</head>
<body>
<form>
<input type = “button” value = “Print” onclick = “window.print()” />
</form>
</body>
</html>
```

这可以帮助你获取你正在查看内容的打印副本，但当你想要打印页面时，并不建议使用它。有一个打印友好的页面，它不会包含通常出现在网页侧边缘的广告等图像。

为了使页面适用于打印，你需要：
- 复制页面上的文本，且不包含任何你不想要的图片。
- 如果你不需要额外的副本，则需要使用适当的注释制作可打印的文本。
- `<! – PRINT STARTS HERE - - > <! - - PRINT ENDS HERE - - >`

如果这些步骤不起，请使用浏览器上的工具栏打印页面。文件路径为 `file – print – okay`

# 结论

感谢你读完《JavaScript 编程基础：零基础初学者入门》，希望这本书对你有所启发，并能够为你提供实现目标所需的所有工具，无论你的目标是什么。

下一步是将你新学到的知识应用于创建 JavaScript 代码。

你一直有无尽的内容供你学习，如果你感兴趣，你可以在网上找到书籍和其他资源来进一步丰富你的知识，以便你能够使用 JavaScript 做更多事情。

如果你的脚本第一次运行没有按照你的预期工作，请不要气馁，这需要耐心和练习才能让你的脚本运行正确。

最后，如果你发现这本书对你有任何帮助，我们将非常感谢你在亚马逊上的好评！

# 关于作者

Nathan Clark 是一位经验丰富的程序员，在软件行业拥有近 20 年的经验。

他拥有省理工学院（MIT）的硕士学位，曾在美国领先的软件公司工作，并积累了大量的软件设计和开发知识。

Nathan 和他的妻子 Sarah 在 2009 年创立了自己的开发公司，以便能够承担更具挑战性和创造性的项目。如今，他们为全球的高端客户提供服务。

Nathan 喜欢通过他的书籍系列分享编程知识，为客户开发创新的软件解决方案，并在空闲时间观看经典科幻电影。

若想从专家那里学习编程，请关注商店或网上 Nathan 的其他书籍。

