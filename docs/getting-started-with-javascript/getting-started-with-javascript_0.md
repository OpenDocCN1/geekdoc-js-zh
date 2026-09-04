
# JavaScript 入门指南

您正在阅读的电子书采用文件格式（EPUB 或 Mobi），该格式使书籍内容能够适应您阅读设备的显示选项以及您的个人需求。这非常棒；但遗憾的是，并非所有设备都能以相同方式显示内容，图片、表格或连字符等功能的表现可能会遇到困难。本电子书已针对尽可能多的常见阅读设备进行了显示优化。

如果您想放大查看图片（尤其是在 iPad 的 iBooks 中），请点击相应图片一次。再次点击即可返回上一屏幕。您可以在服务页面找到更多关于屏幕布局自定义的建议。

## 目录

### 14.3 趣味跑

### 14.5 记忆配对

## 15 媒体、绘图与传感器

### 15.1.1 音频文件

### 15.2 画布

### 15.2.2 图像

### 15.3 传感器

### 15.3.2 路径追踪

### 15.3.4 加速度传感器

### A.1 XAMPP 包的安装

### A.1.2 在 Ubuntu Linux 上安装

### A.2 关键字列表

## 索引

### 法律声明

- 所有习题及解答
- 它们实现了类似于你在其他计算机应用程序中所习惯的交互。你可以进行输入并触发处理，程序将返回结果。

为了简化程序的开发，你只需要一个能够高亮显示 HTML 标记和 JavaScript 关键字以便清晰识别的文本编辑器。Notepad++ 编辑器是众多能做到这一点的编辑器之一。

## 1.2 JavaScript 不能做什么？

JavaScript 无法自行开启。可能存在个别情况下浏览器中禁用了 JavaScript，但无法完全使用的网站比例相当高。不过，我们至少可以识别出 JavaScript 是否被禁用，并在这种情况下发送一条消息（第 1.11 节）。

JavaScript 也无法在 Web 服务器上保存任何内容（除非借助额外工具）。JavaScript 程序在浏览器中执行，而不是在加载它们的 Web 服务器上执行，因此无法在 Web 服务器上保存数据。

JavaScript 在使用过程中只能在浏览器中存储少量数据。它不会在那里造成任何损害。

## 1.3 浏览器与移动浏览器

无论是否包含 JavaScript，互联网页面都会被不同终端设备上不同操作系统的不同浏览器接收，并在使用过程中实现。

互联网上有各种浏览器统计数据，例如在 [`www.w3schools.com/browsers/`](https://www.w3schools.com/browsers/) 上，这些数据可用于确定哪些浏览器被使用以及使用频率。多年来，Google Chrome 浏览器的用户份额最高，因此它作为本书示例程序最重要（但非唯一）的参考。

某些 JavaScript 语句可能针对特定浏览器有不同的写法，但我建议始终使用标准形式，以便该语句尽可能适用于更多浏览器。这一原则也适用于本书中的示例程序。

配备移动浏览器的移动设备比例正在不断增加。移动设备提供了一些额外的选项，例如用于地理定位数据的接收器或传感器，以及移动设备的位置和加速度。这些过程中确定的数据可以由 JavaScript 进一步处理（参见第 15 章，第 15.3 节）。

## 1.4 ECMAScript

JavaScript 基于 ECMAScript。你可以以传统方式在 JavaScript 中应用面向对象编程，基于原型和构造函数。自 ECMAScript 2015 标准引入以来，出现了一种新的标准表示法，它使用类、构造函数、属性和方法，就像其他面向对象语言一样。在本书中，我们只使用这种表示法，所有现代浏览器也都实现了它。更多细节将在第 3 章中详细说明。

ECMAScript 标准自 2015 年以来每年更新一次，ECMAScript 2024 标准已于 2024 年 7 月完成。你可以在以下网站上找到许多标准化元素及其在个别浏览器中实现的概述：[`compat-table.github.io/compat-table/es2016plus`](https://compat-table.github.io/compat-table/es2016plus)。

较新标准的许多元素对初学者也很有用，并且可以在本书的相关章节中找到。我将分别介绍它们。

## 1.5 本书结构

```html
<!DOCTYPE html>
<html lang="en-us">
  <meta charset="utf-8">
  <link rel="stylesheet" href="js5.css">

  <body>
    <p>
      A paragraph with line breaks
    </p>

    <p>
      An area with line breaks
    </p>

    <p>An image:<br><img src="im_paradise.jpg" alt="Paradise"></p>

    <p>A list:</p>
    <ul>
      <li>First entry</li>
    </ul>

    <p>A table:</p>
    <table>
      <tr>
        <td>Cell B</td>
      </tr>
      <tr>
        <td>Cell D</td>
      </tr>
    </table>
  </body>
</html>
```

- 如果需要，可以快速且统一地更改所有文档的格式。

```css
body {
  font-family: Verdana;
  font-size: 11pt;
  color: #202020;
}

td {
  font-size: 11pt;
  background-color: #e0e0e0;
  padding: 5px;
}

@media only screen and (max-width: 992px) {
  @media only screen and (orientation: landscape) {
    body {
      font-size: 20pt;
    }

    img {
      width: 240px;
      height: 180px;
    }

    select {
      font-size: 20pt;
    }

    input[type=checkbox] {
      width: 30px;
      height: 30px;
    }

    input[type=range] {
      width: 250px;
      height: 30px;
    }
  }

  td {
    font-size: 36pt;
  }

  input {
    font-size: 32pt;
  }

  input[type=radio] {
    width: 45px;
    height: 45px;
  }

  input[type=color] {
    width: 250px;
    height: 45px;
  }

  textarea {
    font-size: 32pt;
    height: 140px;
  }
}
```

- 通过 `font-size` 确定 11 磅的字体大小。
- 通过 `background-color` 确定背景颜色 `#f8f8f8`。

你可以使用 RGB 值指定颜色。`#` 字符后跟两个十六进制数字，分别表示红色、绿色和蓝色分量。颜色 `#202020` 对应深灰色，而 `#f8f8f8` 对应非常浅的灰色。

表格单元格（标记 `td`）内的字体大小单独设置为 11 磅。表格单元格的背景颜色通过 `#e0e0e0` 设置为浅灰色，这使得单元格比文档背景稍暗。通过使用 `padding` 规范，你可以调整元素与其周围元素之间的内部距离。此处，表格单元格的文本内容到单元格边缘的距离设置为 5 像素。

至此，用于 PC 或笔记本电脑的 CSS 信息结束。

你可以使用媒体查询来响应查看文档的设备属性。CSS 规范 `@media only screen and (max-width: 992px)` 使后续花括号内的 CSS 规范执行以下操作：

- 仅引用屏幕上的输出，与打印机上的输出相对。
- 使用菜单进行选择（`select`）。
- 使用单选按钮进行选择（`input type=radio`）。
- 选择颜色（`input type=color`）。
- 多行文本字段（`textarea`）。

## 1.7 一些特殊字符

你可以使用以下程序输出一些特殊字符。你也可以直接用键盘输入一些特殊字符，而所有这些字符都可以通过所谓的实体来输出。

程序如下：

```html
<body>
  还有实体：&gt; &amp; &dollar; &#64;<br>
  &frac14; &frac12; &frac34; &sup2; &sup3; &micro; &pi;<br>
</body>
</html>
```

- 第三行包含 ©（版权）、®（注册商标）、‰（千分号）、¼（四分之一）、½（二分之一）、¾（四分之三）、²（平方）、³（立方）、µ（微）和 π（圆周率）的实体：分别是 `&copy;`、`&reg;`、`&permil;`、`&frac14;`、`&frac12;`、`&frac34;`、`&sup2;`、`&sup3;`、`&micro;` 和 `&pi;`。

```html
...
<p>HTML 中的文本</p>
<script>
  document.write("<p>JavaScript 中的文本</p>");
</script>
<p>HTML 中的文本</p>

<script>
  document.write("<p>JavaScript，双引号</p>");
  document.write("<p><span>"
    + " 在</span>双引号内部</p>");
  document.write('<p><span>'
    + ' 在</span>单引号内部</p>');
</script>
</body>
</html>
```

- JavaScript 区分大小写。使用 `document.Write(...)` 语句不会成功，因为 `Write()` 方法（大写 W）并不存在。

```html
...
<script src="external_file.js"></script>
<script>
  document.write("<p>这来自 external.htm</p>");
</script>
</body>
</html>
```

```javascript
document.write("<p>这来自 external_file.js</p>");
```

请注意，外部文件中没有 `script` 容器。该文件的名称可以使用任何扩展名，但以 `js` 结尾已成为惯例。

jQuery 库（参见第 11 章）以及其他包含许多实用函数的大型 JavaScript 库都是通过这种方式集成到应用程序中的。

## 1.10 注释

注释用于描述程序的各个部分，使您和他人更容易理解这些程序。让我们看一个示例：

```html
<body>
  <!-- in the HTML section -->

  <script>
    /*
      This is a comment across multiple lines
      document.write("<p>A paragraph from the JS section</p>");
    */
  </script>
</body>
</html>
```

- 在 JavaScript 部分，跨越多行的注释位于 `/*` 和 `*/` 字符串之间。

```html
...
<script>
  document.write("<p>JavaScript is running here</p>");
</script>

<p>JavaScript is not running here<br></p>
</noscript>
```

**清单 1.8**　`no_script.htm` 文件

在 `noscript` 容器内，您可以写下文本和 HTML 标记，以便在 JavaScript 关闭时显示。

如果 JavaScript 已启用，则只会执行 `script` 容器中的语句，页面将如图 1.7 所示。

![JavaScript 已启用](img/img-f1.7.html)

**图 1.7**　JavaScript 已启用

您可以暂时停用 JavaScript 以进行测试，以下以 Google Chrome 浏览器为例说明必要步骤。点击右上角的三个点调用菜单，选择“设置”菜单项，在搜索窗口中输入“JavaScript”。在搜索结果中找到“网站设置”。在那里，您会找到“JavaScript”区域，默认选项为“网站可以使用 JavaScript”。选择另一个选项“不允许网站使用 JavaScript”。

然后，当您调用包含 JavaScript 的文件时，浏览器地址栏最右侧会显示一个图标，提示该页面上的 JavaScript 已被阻止。点击该图标打开一个对话框。在那里，您可以为此页面激活 JavaScript。“管理”按钮也会直接带您进入前面提到的用于开启和关闭 JavaScript 的选项。

当 JavaScript 关闭时，`no_script.htm` 页面看起来像图 1.8。

![JavaScript 已禁用](img/img-f1.8.html)

**图 1.8**　JavaScript 已禁用

# 2 编程的基本原则

变量、运算符、分支、循环和函数是开始编程所需的基本元素。

在本章中，您将学习 JavaScript 编程的基础知识：变量、运算符、分支、循环和函数。这些元素构成了许多编程语言的基础，并将使您以后更容易入门其他领域。

## 2.1 存储值

文本或数字通常需要在程序序列中保存，它们既可以来自程序开发过程中的赋值，也可以来自使用程序时的输入。这些保存的值在程序的后续点中会再次用到。

本节讨论使用变量存储文本、数字和真值，变量可以是可变的或不可变的。不可变的变量也称为常量。在本节中，您还将了解两个用于简单输入和输出的对话框。

JavaScript 中的变量没有定义的类型。您可以在变量中保存一个字符串（即文本），如果变量是可变的，您以后可以在同一个变量中保存一个数字。

### 2.1.1 格式化字符串

文本由单个字符组成，整体称为字符串。变量用于存储值。以下程序包含一些示例：

```html
<body>
  <p>
    <script>
      let helloText = "Hello world";
      helloText = "Good morning";

      document.write("Text: " + text2 + "<br>");

      let text3 = 'With single quotation marks';

      document.write("Text: " + text4 + "<br>");

      // document.write("Text: " + text5 + "<br>");

      // document.write("Text: " + text5 + "<br>");

      const text6 = "Cannot be changed";

      // text6 = "Not allowed";
    </script>
  </p>
</body>
</html>
```

一个输出可以由多个部分组成。这可能包括一个用双引号括起来的字符串，其中也可以包含 HTML 标签。然而，它也可以是一个变量，其当前值被输出。各个部分通过 `+` 运算符组合成一个更长的字符串。

使用 `text2` 变量，声明和赋值被合并到一条语句中。

字符串的值也可以写在单引号之间，正如你在 `text3` 变量中看到的那样。

`text4` 变量被声明了，但在程序代码中没有被赋值。因此它的值为 `undefined`。

对尚未声明且尚未赋值的变量进行读取访问是不允许的。第一条包含 `text5` 变量的程序行会导致错误并终止程序，因此该行已被注释掉。

虽然允许对尚未声明的变量进行写入访问，但不推荐这样做，因为该变量更容易被意外修改，也更难控制。因此，其他包含 `text5` 变量的程序行也被注释掉了。

如果你想将一个变量标记为不可更改，同时确保其值在程序的后续过程中不能被修改，你应该使用 `const` 关键字而不是 `let`。变量 `text6` 就是这样一个不可更改的变量（即常量）。

给常量赋新值会导致错误并终止程序，因此这一行也被注释掉了。

你可以为了测试目的，暂时取消上述某个错误程序行的注释。单词 `End` 的输出会告诉你程序是运行到了结尾还是提前终止了。

程序的输出如图 2.1 所示。

![字符串的输出](img/img-f2.1.html)

**图 2.1**　字符串的输出

### 注意

变量也可以使用 `var` 关键字声明，但这些变量更容易被意外修改，也更难控制。这在由大量程序段组成的较长程序中尤其不利，因此使用这些变量更容易导致程序错误。相反，你应该始终使用 `let` 和 `const` 关键字，就像本书所有示例中所做的那样。

### 2.1.2 命名规则

以下是命名变量的一些规则：

- 名称可以由大写和小写字母、数字以及下划线（`_`）组成。
- 名称开头不能是数字。
- 名称中不允许出现特殊字符，例如德语变音字母 ä、ö、ü、Ä、Ö、Ü，ß 或空格。
- 名称不能与 JavaScript 关键字之一相同。关键字列表见附录 A 的 A.2 节。

此外，还有两个常见的约定：

- 变量名称应具有自解释性（即，它应能说明其内容）。如果要保存姓氏，你应该将变量命名为 `familyName`。
- 较长的变量名称尤其具有自解释性。驼峰式命名法已成为惯例：名称以小写字母开头，每个新单词以大写字母开头（例如 `buttonStart`、`buttonStop`）。

### 2.1.3 字符串的输入与输出

在本节中，你将学习两个有用的方法：

- `prompt()` 方法，它会打开一个对话框，提示你输入文本。
- `alert()` 方法，它会打开一个显示消息的对话框。

这两个方法都使用字符串，并导致程序在其运行过程中暂停，之后，只有在输入完成或消息被确认后，程序才会重新开始运行。这让你有机会进行交互、请求输入或启动输出的读取。

以下是一个示例：



```html
<body>
  const input = prompt("输入：\n 请进行输入：",
    alert("你的输入：\n" + input + "\n 非常感谢");
</body>
</html>
```

```html
<script>
  let number;
  const anotherNumber = number + 30.8;
  const bigNumber = 5.2e6;

  document.write("Another number: " + anotherNumber + "<br>");
  document.write("Addition correct: " + (anotherNumber + 25) + "<br>");
  document.write("Big number: " + bigNumber + "<br>");
</script>
```

```html
</body>
</html>

<script>
  let saved;
  const done = false;
  document.write("Done: " + done + "</p>");
</script>
```

**清单 2.4**　`bool.htm` 文件

`saved` 变量被赋值为 `true`，而 `done` 常量被赋值为 `false`。然后输出它们，如图 2.5 所示。

![真值的输出](img/img-f2.5.html)

**图 2.5**　真值的输出

## 2.2　执行复杂计算

以下各节将向你展示如何使用变量和数值进行计算。通过输入数字和输出结果，你的程序变得具有交互性。

### 2.2.1　计算运算符

除了 `+` 运算符，以下运算符也可用于执行计算：`-` 用于减法，`*` 用于乘法，`/` 用于除法，`%` 用于取模（计算整数除法的余数）。自 ECMAScript 2016 起，还增加了 `**` 运算符用于乘方。

下面的程序进行了一些简单的数学运算：

```html
<body>
  <p>
    z = 2 + 4 - 2.5;
    document.write("2 + 4 - 2.5 = " + z + "<br>");

    z = (2 + 4) * (3 - 6) / 2;

    z = 13.5 % 5;
    document.write("13.5 % 5 = " + z + "<br><br>");

    z = 6;
    document.write("z = " + z + "<br>");

    z = z * 5;
    document.write("z = z * 5 | z = " + z + "<br><br>");

    z = 2.5 ** -3.5;
    document.write("2.5 ** -3.5 = " + z + "<br>");

    z = (-2) ** -3.5;
    document.write("(-2) ** -3.5 = " + z + "<br>");
  </p>
</body>
</html>
```

首先，执行清单 2.5 中三个块中的第一个块的计算：

* 第一个计算从左到右进行，结果为 3.5。
* 在第三个计算中，先计算括号内的内容 `(2 + 4)` 和 `(3 - 6)`。然后才能进行剩余的计算。结果为 `6 * -3 / 2 = -9`。
* 变量可以出现在赋值语句的两侧。在最后一个示例中，可以看到 `z` 的旧值（-6）乘以 5 得到 `z` 的新值（-30）。

第三个块涉及指数运算符 `**`，其优先级甚至高于乘法和除法：

* 第一个计算是 `2.5^(-3.5)`。`**` 运算符前的值称为底数，运算符后的值称为指数。两者都可以有小数位，指数前可以加负号。
* 第三个示例表明，对负数进行带有小数位的负指数运算在数学上是不允许的。这会产生 `NaN` 值，表示非数字。

```html
<script>
  let tx;
  tx = tx + " is a";
  document.write(tx + "<br>");

  z = 6;
  document.write("<p>" + z + " ");

  z--;
  document.write(z + " ");

  z -= 5;
  document.write(z + " ");

  z /= 6;
  document.write(z + " ");

  d = a++;
  document.write("<p>" + d + " ");

  d = c++ + ++c + c++;
  document.write(d + "</p>");
</script>
```

**清单 2.6**　`assignment_combined.htm` 文件

首先，一个字符串被赋值并扩展了两次。第二次扩展使用了赋值运算符 `+=`。

然后，一个变量被赋值并多次更改。`++` 运算符将变量的值增加 1，而 `--` 运算符将其减少 1。使用 `z = z + 1` 或 `z = z - 1` 语句可以达到相同的结果。

相应地，`+=` 运算符将变量的值增加后续值，`-=` 运算符将其减少后续值。因此，`*=`、`/=` 和 `%=` 运算符分别表示以下语句的缩写：`z = z * [value]`、`z = z / [value]` 和 `z = z % [value]`。

你可以将 `++` 和 `--` 运算符放在变量之前（前缀表示法）和变量之后（后缀表示法）。对于语句 `d = a++;`，`d` 接收 `a` 的旧值，然后 `a` 增加。对于语句 `d = ++b;`，先增加 `b`，然后 `d` 接收增加后的 `b` 值。

通过这种方式，（不幸的是）你还可以构造出非常令人困惑的表达式，其结果只有经过长时间思考才能识别，正如你在最后一个示例中所见。

你可以在图 2.7 中看到赋值的结果。

![赋值运算符](img/img-f2.7.html)

**图 2.7**　赋值运算符

### 2.2.3　输入数字

在本节中，使用 `prompt()` 方法输入两个数字，然后应使用 `alert()` 输出这两个数字的和。

`prompt()` 方法返回一个字符串。在第 2.1.4 节中，你已经看到 `+` 运算符对字符串和数字的处理方式不同，因此有必要先将这样的输入转换为数字，然后才能用于计算和。

以下是一个示例程序：

```html
<body>
```

```javascript
const z1 = parseFloat(input);
const result = z1 + z2;
```

```html
</body>
</html>
```

**图 2.9**　输入第二个数字

![整个计算的结果](img/img-f2.10.html)

**图 2.10**　整个计算的结果

### 注意

在本书可下载资料（位于 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)）的附加章节 2 中，你可以在 `regexp_point.htm` 文件中找到该程序的扩展版本。它支持输入和输出带逗号的数字。

数字也可以以指数格式输入。如果输入无法转换为数字（例如“abc”或空输入），`parseFloat()` 会返回结果 `NaN`。在第 2.3.5 节中，我们将判断是否输入了数字。

`parseInt()` 函数与 `parseFloat()` 函数类似，它也会截断小数部分并返回一个整数。因此，字符串“3.8”会变成整数 3。

### 注意

`write()` 方法是在 `document` 对象上调用的，但全局函数 `parseFloat()` 和 `parseInt()` 并不是针对特定对象调用的。

通常，`parseInt()` 将文本解释为十进制数（即基数为 10 的数字）。你可以使用第二个参数指定不同的基数，例如，调用 `parseInt("101", 2)` 的结果是十进制值 5，因为文本“101”被解释为基数 2（即二进制数）。

### 注意

你可以在本书可下载资料（位于 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)）的附加章节 1 第 1.2 节中找到 `u_number` 练习。

### 2.2.4　数制

你通常使用基数为 10 的十进制数制，但也可以使用 `toString()` 方法将数字输出为使用其他数制数字的字符串，例如：

* 二进制数制（基数为 2）
* 十六进制数制（基数为 16）

示例如下：

```html
<body>
  <p>
    const z = 27;

    document.write("Hexadecimal: " + z.toString(16) + "<br>");
    document.write("Dual: " + z.toString(2) + "<br>");
  </p>
</body>
</html>
```

* 如果条件不满足，则执行关键字 `else` 后面的语句或语句块（如果存在）。

条件通过比较运算符形成，并产生真值。`>` 运算符表示大于，`<` 运算符表示小于，`>=` 表示大于或等于，`<=` 表示小于或等于。你可以使用 `==` 检查相等性，使用 `!=` 检查不相等性。

你应特别注意 `==` 运算符的双等号。一个常见的错误是将 `==` 与 `=` 运算符混淆，后者会导致赋值而不是比较。所有比较运算符都可用于数字，但只有最后两个——`==` 和 `!=`——可用于字符串。

你可以使用三元运算符 `?:` 创建简化的分支，它会提供一个可以赋值的值。

以下是一个包含总共六个分支的示例。为了便于查看，这些分支在程序和输出中进行了编号：

```html
<body>
  const a = 12, b = 7;

  // 1: 单分支
  document.write("<p>1: a is greater than b</p>");

  // 2: 单分支，带 else
  document.write("<p>2: a is less than b</p>");
  document.write("<p>2: a is not less than b</p>");

  // 3: 单分支，块中有多条语句
  {
    document.write("3: An additional line</p>");
  }

  if (a > b)
  else if (a < b)
  else

  const country = "Spain";
  document.write("<p>5: Country is Spain</p>");
  document.write("<p>5: Country is not Spain</p>");

  // 6: 三元运算符
  document.write("<p>6: The greater number is " + greater + "</p>");
</body>
</html>
```

```html
<script>
  const response = confirm("您要执行此操作吗？");

  document.write("此操作将被执行");
  document.write("此操作将不会被执行");
</script>
```

**清单 2.10**　`if_confirm.htm` 文件

如果单击“确定”按钮，将返回 `true`。这对于分支来说已经足够了，因为它提供了一个真值。你不需要比较运算符，`if(response == true)` 查询也会得到相同的结果。

如果单击“取消”按钮，将返回 `false`，并执行 `else` 分支。

在图 2.13 中，你可以看到带有问题的对话框。

![使用“confirm()”确认](img/img-f2.13.html)

**图 2.13**　使用“confirm()”确认

### 2.3.3　链接多个条件

如果需要链接多个条件，可以使用逻辑运算符 `&&` 表示逻辑与，或 `||` 表示逻辑或。对于逻辑与，所有单个条件都必须为真，整个条件才为真。对于逻辑或，只要有一个条件为真，整个条件就为真。

还有逻辑运算符 `!` 表示逻辑非，它会反转条件的真值。`true` 变为 `false`，`false` 变为 `true`。

示例如下：

```html
<body>
  <p>
    document.write("1: 介于 10 和 20 之间</br>");
    document.write("1: 不介于 10 和 20 之间<br>");

    if (a < 10 || a > 20)
    else

    document.write("3: 不介于 10 和 20 之间");
    document.write("3: 介于 10 和 20 之间");
  </p>
</body>
</html>
```

**清单 2.11**　`if_linked.htm` 文件

在第一种情况下，系统检查数字是否大于等于 10 且小于等于 20（即是否在 10 到 20 的数字范围内）。

第二种情况测试数字是否小于 10 或大于 20（即在范围之外）。

第三种情况使用 `!` 运算符判断数字是否不在 10 到 20 的数字范围内。

在图 2.14 中，你可以看到当每次检查数值 12 时，各种链接的输出结果。

![链接的条件](img/img-f2.14.html)

**图 2.14**　链接的条件

如果在程序中将值 `a` 设为 `25`，输出会是什么？请自行思考答案。然后相应地修改程序，检查你的假设是否正确。当 `a = -15` 时会发生什么？同样，先通过思考确定结果，然后使用修改后的程序检查你的假设是否正确。

### 两个提示

* `a >= 10 || a <= 20` 条件对每个数字都成立，而 `a < 10 && a > 20` 条件对任何数字都不成立。你应该避免这些链接。
* JavaScript 中为逻辑运算符定义了所谓的短路行为。这对于函数的使用很重要，在第 2.6.7 节中可以看到一个示例。

### 注意

你可以在本书的可下载材料中找到 `u_linked` 练习，位于附加章节 1 的第 1.4 节，下载地址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

### 2.3.4　链接与赋值

自 ECMAScript 2021 起，新增了两个运算符 `&&=` 和 `||=`，它们将逻辑连接与赋值操作结合在一起。以下程序展示了这一较少使用的选项，其中使用了三个布尔值：

```html
<body>
  <p>
    let a = true, b = true, c = false;

    a &&= b;
    document.write("a after a&&=b : " + a + "<br>");

    a ||= c;
    document.write("a after a||=c : " + a + "<br>");
  </p>
</body>
</html>
```

**清单 2.12**　`assignment_linked.htm` 文件

每条语句的结果都赋值给变量 `a`。程序的输出如图 2.15 所示。

![逻辑连接与赋值](img/img-f2.15.html)

**图 2.15**　逻辑连接与赋值

### 2.3.5　检查数字输入

在本节中，将使用多分支结构检查输入的数字。在程序过程中，你将熟悉以下有用的函数和方法：

* `isNaN()` 函数用于判断变量是否不包含有效数字。
* `Math.abs()` 方法计算一个数字的绝对值（即不带符号的数字）。例如，值 -5 变为 +5，值 5 仍为 +5。

```html
<script>
  const input = prompt("Please enter a number from 0 to 1, without 1");

  const distance = Math.abs(number_random - number_input);

  if (input == null)
  else if (input == "")
  else if (isNaN(input))
  else if (number_input < 0 || number_input >= 1)
  else if (distance < 0.1)
  else

  document.write("Input: " + input + "<br>");
  document.write("Number: " + number_input + "<br>");
  document.write("Distance: " + distance);
</script>
</body>
</html>
```

```html
<script>
  const b = "4711";
  const d = true;

  document.write("<p>a: " + a + ", " + typeof a + "<br>");
  document.write("c: " + c + ", " + typeof c + "<br>");

  document.write("a == b<br>");
</script>
```



```html
document.write("a === c<br>");

if (a === b)

else

</script></p>
```

**清单 2.14**　　`if_exact.htm` 文件

在图 2.18 中，你可以看到程序中使用的四个变量的名称、值以及（借助 `typeof`）值的类型。对于数字，`typeof` 返回 `number`；对于字符串，返回 `string`；对于布尔值，返回 `Boolean`。

![检查值和类型](img/img-f2.18.html)

**图 2.18**　　检查值和类型

变量 `a`、`b` 和 `c` 都包含值 `4711`，但 `b` 中是字符串。使用 `==` 运算符对这些变量进行的所有比较都会返回 `true`。如果使用 `===` 运算符，则只有在比较 `a` 和 `c` 时才会成功。

### 2.3.7 运算符的优先级

JavaScript 中的运算符具有不同的优先级。如果在一条语句中使用了多个运算符，则优先级较高的部分会先执行。如果优先级相同，则从左到右执行。

表 2.1 按优先级顺序列出了到目前为止使用的运算符。

| 优先级 | 运算符 | 描述 |
|---|---|---|
| 1（最高） | `( )` | 括号 |
| 3 | `**` | 幂运算 |
| 5 | `+`、`-` | 加法、减法 |
| 7 | `==`、`!=`、`===`、`!==` | 等于、不等于、全等（类型比较）、不全等（类型比较） |
| 9 | `||` | 逻辑或 |

```html
<script>
  let city;

  switch (country)
    case "Italy":
      break;
    case "Wales":
      city = "London";
    default:
  }

  document.write("Capital of the country: " + city);
</body>
</html>
```

```html
<script>
  document.write("<p>1: ");

  document.write(i + " ");

  // 2: Downward
  for (let i = 20; i >= 10; i--)

  document.write("<br>3: ");

  document.write(i + " ");

  // 4: With decimal number, optimized
  for (let i = 3; i <= 4.1; i += 0.2)

  document.write("<br>5: ");

  continue;
  break;
</script>
```

**清单 2.16**　　`for.htm` 文件

```html
<script>
  for (let z = 0; z < 3; z++)

  document.write("</table>");

  for (let s = 0; s < 3; s++)

  document.write("</tr></table>");

  for (let z = 0; z < 3; z++)

    document.write("<tr>");

    document.write("<td>Z" + z + "/S" + s + "</td>");
  }
</script>
```

**清单 2.17**　　`for_table.htm` 文件

程序的输出如图 2.20 所示。

![多个表格](img/img-f2.20.html)

**图 2.20**　　多个表格

第一步是创建一个包含三行的表格。每行包含一个表格单元格，其中显示当前行的编号，编号从 0 开始。你经常会遇到这种与数组相关的编号方式（第 2.4.3 节）。

然后，创建一个只有一行的表格。这一行包含三个表格单元格，每个单元格显示当前表格单元格的编号。

最后，是一个包含三行五列的表格。每个表格单元格中显示当前行和当前列的编号。

这里使用了两个嵌套循环，并用不同的变量控制：

- 最初，外层循环的变量 `z` 的值为 0。然后，内层循环使用变量 `s` 和值 0 到 4 总共运行五次，以创建一行的五个单元格。
- 然后，`z` 的值变为 1，再次创建五个单元格，以此类推。

### 注意

你可以在本书的下载材料中找到 `u_table` 练习，位于附加章节 1 的第 1.6 节，下载地址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

### 2.4.3 循环与数组

数组用于记录大量主题相关的数据。它们由单个元素组成，并且可以使用循环快速访问数组的所有元素。我们在此已经介绍了第一个简单的数组，你可以在第 6 章的 6.1 节中了解更多关于数组的内容。

以下是一个示例程序：

```html
<body>
  let person;

  for (let z = 0; z < 3; z++)

  document.write("</table>");

  for (let z = 0; z < 3; z++)

    document.write("<tr>");

    document.write("<td>" + age[z][s] + "</td>");
  }
</script>
```

**清单 2.18**　　`for_array.htm` 文件

可以使用方括号创建数组。方括号内是数组的各个元素，用逗号分隔。通常，数组的元素在主题上属于同一类，并且类型相同（例如，数字、字符串、布尔值）。

`person` 变量表示字段被赋值后对该字段的引用，可以通过该引用访问字段及其元素。字段的名称为 `person`，你可以更改字段的各个元素，也可以为变量分配不同的字段。

字段的各个元素可以通过其顺序编号来标识：即所谓的索引，索引在字段名称后的方括号中指定。第一个元素可以通过 `person[0]` 访问，第二个元素通过 `person[1]` 访问，以此类推。索引始终从 0 开始。

在 `for` 循环中利用这种关系，以表格形式输出字段的所有元素。循环变量 `z` 遍历字段的所有索引，对于包含三个元素的字段，这些索引为 0、1 和 2。

你可以在图 2.21 中看到表格的输出。

![循环与字段](img/img-f2.21.html)

**图 2.21**　　循环与字段

字段本身可以包含字段作为元素，从而可以创建多维字段。

在此示例中，关于三个人的三组数据各自位于一维字段中。这三个一维字段再次写在方括号内，并用逗号分隔。这样便生成了一个二维字段，并且可以在二维表格中清晰地显示出来。

无论维度数量如何，你都可以使用不可更改的变量作为对字段的引用。但只有引用是不可更改的。你仍然可以更改字段的各个元素，但不能为变量分配不同的字段。

二维字段的各个元素只能通过两个索引来访问，每个索引都包含在方括号内。你可以通过 `age[0][0]` 访问第一个人的姓名，通过 `age[0][1]` 访问该人的年龄，通过 `age[1][0]` 访问第二个人的姓名，以此类推。

在嵌套的 `for` 循环中利用这种关系，以表格形式输出字段的所有元素。循环变量 `z` 遍历字段的行索引，而循环变量 `s` 遍历字段的列索引。

你还可以在图 2.21 中看到二维表格的输出。

### 2.4.4 使用 `while` 的循环

使用 `while` 的循环依赖于在循环开始时检查的条件。

在以下示例中，随机数被相加，`while` 循环会一直运行，直到数字之和达到值 4。在程序开发过程中，由于数字的随机性，这些值未知，因此不知道需要相加多少个数字（即循环将运行多少次）。

程序如下：

```html
<body>
  let sum = 0;

  {
    document.write(sum + "<br>");
  }
</script></p>
```

**清单 2.19**　　`while.htm` 文件

数字之和初始设置为 0，原因有二：

- 在循环开始时，将总和与值 4 进行比较，只有当所有涉及的值都已知时，比较才有意义。
- 在循环内部，总和被赋予一个新值，该值会加到旧值上。因此，开始时需要一个旧值 0。

只要总和小于 4，循环就会执行。由于循环包含多条语句，必须使用花括号。在循环内部，总和增加一个随机值并输出，你可以在图 2.22 中看到可能的输出。

![“while”循环用于相加随机数](img/img-f2.22.html)

**图 2.22**　　“while”循环用于相加随机数

### 2.4.5 使用 `do … while` 的循环

使用 `do` ... `while` 的循环依赖于在循环结束时检查的条件。与 `while` 循环不同，此循环至少执行一次。

以下程序包含一个心算任务。两个介于 1 到 20 之间的随机数需要相加，程序会提示你，直到输入正确的结果。

与 `while` 循环一样，在程序开发过程中不知道循环必须执行多少次。然而，至少需要一次尝试，因此使用了 `do` ... `while` 循环。`do` ... `while` 循环也称为读入循环，因为它常用于控制输入一个值：

- 输入至少执行一次。
- 如果输入不符合规范，则会重复。

程序如下：

```html
<body>
  const number_random = Math.random() * 20 + 1;

  const b = Math.floor(Math.random() * 20 + 1);

  let number_input;

  do {
    const input = prompt(a + " + " + b + " = ");

    if (number_input != sum)
  }
</script></p>
```

**清单 2.20**　　`do_while.htm` 文件

随机数生成器返回一个介于 0 和 1 之间的数字（不包括 1）。如果将此数字乘以 20，结果是一个介于 0 和 20 之间的数字（不包括 20）。如果加 1，结果是一个介于 1 和 21 之间的数字（不包括 21），正如这里 `number_random` 变量的情况。

`Math` 对象的 `floor()` 方法会截断数字的所有小数部分，因此数字 3.8 将变为数字 3。你可以在第 6 章的第 6.3 节中了解更多关于 `Math` 对象的信息。`Math.floor()` 方法首先使用 `number_random` 变量调用，然后直接调用（无需中间存储）以处理介于 1 和 20 之间的随机数。这样，过程可以缩短。

输入的文本保存在 `number_input` 变量中，然后使用 `parseInt()` 将其转换为整数。接下来是一个条件，该条件被使用了两次：整数是否与正确结果不同？如果是，则显示一条消息，并且 `do` ... `while` 循环继续运行。

如果输入了正确结果，条件不再成立，循环结束，任务和正确结果会再次显示在文档中。

在图 2.23 中，你可以看到任务和可能的错误输入。程序对此的响应显示在图 2.24 中。

![任务与错误输入](img/img-f2.23.html)

**图 2.23**　　任务与错误输入

![程序响应](img/img-f2.24.html)

**图 2.24**　　程序响应

### 三个提示

- 在编程工作开始时，`while` 或 `do` ... `while` 循环的条件以及 `for` 循环第二部分中的条件会带来一定挑战。请记住，这是一个运行条件，而不是终止条件，因此并非条件满足时循环就立即终止。只要条件成立，循环就会继续运行。
- `for` 循环或 `while` 循环的开头后面不能跟分号，因此不应写成 `for(let i = 1; i <= 5; i++);` 或 `while(a > b);`。这会导致循环立即终止，后续语句只执行一次。这种错误很难发现。
- 相反，`do` ... `while` 循环的结尾后面必须跟分号。

### 2.4.6 记忆训练游戏

在本节中，我们将开发一个用于训练记忆力的游戏。由于没有添加新的语言元素，如果你愿意，可以跳过本节。不过，看看你目前学到的语言元素如何在游戏中相互配合，会很有趣。

以下是游戏规则，这些规则也会在浏览器中调用文件后显示：记住即将出现的数字序列，然后输入它们。首先出现三组三位数，然后是三组四位数，依此类推。一旦你输入错误的数字序列，训练即告结束，并会得到评分。当你刷新网页时，训练会从头开始。

程序如下：

```html
<body>
  + "然后输入它们。首先出现三组三位数，"
  + "训练即告结束，并会得到评分。当你刷新网页时，"

  {
    if (counter > 3)
      length++;
  }

  text = "";

  text += Math.floor(Math.random() * 10);

  output += text + "<br>";

} while (input == text);

let quantity = length - 1;

quantity = 0;

document.write(output);
</script></p>
```

**清单 2.21**　　`memory.htm` 文件

随机数字序列存储在 `text` 变量中。`length` 变量包含当前数字序列的长度，`counter` 则记录这是相同长度的第几个数字序列（第一个、第二个或第三个）。

`do` ... `while` 循环在输入与数字序列匹配时持续运行。每次 `counter` 的值都会增加，如果超过 3，则重置为 1。同时，`length` 的值增加，确保相同长度的数字序列出现三次。

`for` 循环用于编译当前长度的随机数字序列。该序列被显示出来，需要记住，然后必须正确输入。

循环结束后（即输入错误后），会显示结果。结果是一个列表，包含到目前为止出现的所有数字序列，最后会显示成功记住并重新输入三次的数字个数。在图 2.25 中，你可以看到一个可能的结果，希望你能超越它。

![记忆训练](img/img-f2.25.html)

**图 2.25**　　记忆训练

## 2.5 发现并避免错误

在开发程序的过程中，你难免会犯一些错误。这是正常的，也是编写程序时的家常便饭。更重要的是要知道如何快速发现并纠正错误——而更棒的是知道如何避免错误。

这些错误可能是语法错误（即不正确或不完整的 JavaScript 语句写法），但也可能是逻辑错误（程序运行完美，但未产生你期望的结果）。

### 2.5.1 开发程序

你应该循序渐进。首先，在纸上思考整个程序应该如何构建。它应该按顺序包含哪些部分？不要试图一次性编写包含所有复杂组件的完整程序。这是你在开始时——甚至有时在后期——可能犯的最大错误！

首先，编写程序第一部分的简单版本，然后进行测试。在成功测试之前，不要添加后续的程序部分。每次更改后都要再次测试，这样如果出现错误，你就会知道是由最后一次更改引起的。最后一次添加后，你就创建了整个程序的简单版本。

现在，将程序的某一部分改为更复杂的版本。通过这种方式，你逐步使程序变得更复杂，直到最终创建出与你在纸上最初设想完全一致的完整程序。

有时，在实际编程过程中，你的设计会发生一两次变化。只要整体结构不变，这没问题；但如果结构变了，那么你应该短暂地回到纸上，重新考虑结构。这并不意味着你必须删除之前的程序行，而是可能只需稍作修改并重新排列。

编写清晰的程序。如果你在考虑如何一次性编写三四个具体步骤，请将它们转化为依次执行的独立语句。这可以简化任何故障排除过程，并且如果你（或其他人）日后修改或扩展程序，重新构建程序会快得多。

我已经提到了一些与分支和循环相关的典型错误。你是否关闭了所有打开的括号和圆括号？这是一个经典的编程错误，尤其是在 JavaScript 中，常常导致什么都不显示。你还已经看到了如何使用 `alert()` 方法来检查值并查找逻辑错误。

你可以将程序的各个部分放在注释括号中，以确定程序的哪一部分运行无误，哪一部分包含错误。

### 2.5.2 使用 `onerror` 查找错误

查找错误的一种方法是使用 `onerror` 事件。一旦发生某些错误，该事件就会被触发，并调用一个函数，该函数会提供有关错误的信息。让我们看下面的例子：

```html
<body>
  <p>
```

```javascript
document.write(x + "<br>");
```

```html
</body>
</html>

... <head> ...
```

```javascript
{
  + "\n 行号：" + line);
```

```html
</head>

<script>
  onerror = error_handling;

  document.write(x + "<br>");
```

```html
</body>
</html>

...
```

```html
<script>
  const y = 42;

  try {
    document.write(x + "<br>");
  }

  {
  }

  {
  }
</script>
</p>
```



```html
**清单 2.24** `try_catch.htm` 文件

两个变量的值将在 `try` 块中输出。注意到 `x` 缺少声明，程序跳转到 `catch` 块，并且关于所发生错误的信息通过一个错误对象传递。通常用 `e`（表示错误）来命名这样的错误对象，你可以使用 `alert()` 输出该对象。

图 2.27 中的输出包含一个 `ReferenceError`。与之前的程序相比，这个错误已被拦截，因此不会出现“Uncaught”，程序继续运行。

![使用 try...catch 捕获错误](img/img-f2.27.html)

**图 2.27** 使用 `try...catch` 捕获错误

### 2.5.4 使用 `throw` 抛出异常

你也可以通过使用 `throw` 创建自己的错误情况，从而抛出异常。你可以利用异常处理过程，确保程序跳转到 `catch` 块。

在以下示例中，需要输入一个大于 0 的数字。有两种情况被视为错误：

- 输入不是有效的数字。
- 输入的数字太小。

在这两种情况下，都会显示相应的错误消息。

程序如下：

```html
<body><p>
  <script>
    {
      throw "不是有效的数字";
      throw "数字太小";
    }

    {
    }
  </script>
</p></body>
```

**清单 2.25** `throw.htm` 文件

如果发生两种情况之一，则会通过分支识别出来。`throw` 语句确保程序直接跳转到 `catch` 块，同时将相关的错误消息发送到 `catch` 块。该消息被输出，在图 2.28 中，你可以看到输入值 `-5` 时显示的消息。

![自定义抛出的异常](img/img-f2.28.html)

**图 2.28** 自定义抛出的异常

### 2.5.5 调试程序

在现代浏览器中，你可以选择调试程序。调试有助于你发现逻辑错误，你可以逐步运行程序，并在任何时间点查看所有变量的值。本节以 Google Chrome 浏览器为例进行说明。

作为示例，使用 `chrome_debug.htm` 文件中的一个程序，该程序将两个数字相加。在图 2.29 中，你可以看到程序的默认输出。

启动调试时，假设浏览器已打开并运行该程序。使用右上角的三个点打开浏览器菜单，选择“更多工具”•“开发者工具”菜单项。然后，开发者工具会显示出来，它们可能提供许多不同的选项。

![程序，正常流程](img/img-f2.29.html)

**图 2.29** 程序，正常流程

对于调试，你需要选择屏幕顶部的“Sources”选项卡。程序代码会如图 2.30 所示显示，每行前面都有行号。

![带有行号的程序代码](img/img-f2.30.html)

**图 2.30** 带有行号的程序代码

```html
... <head> ...
   function hello()
         document.write("<p>Hello world</p>");
   </script>
<body>
   hello();
   </script>
```

**清单 2.26** `function_simple.htm` 文件

对于函数，需要区分定义和调用。浏览器读取函数的定义，然后知道它应该如何工作，只有在调用后才会执行。

函数通常在文档的 `head` 中定义。定义以 `function` 关键字开头，后跟函数名称，函数名称的命名规则与变量名称相同（第 2.1.2 节）。然后是括号（此处尚无内容），接着是一个语句块，始终使用花括号。

在此示例中，函数被调用了两次，调用由函数名称后跟括号（此处尚无内容）组成。你可以在程序中任意多次调用 `hello()` 函数，每次调用时，程序都会跳转到该函数并执行其内容。

你可以在图 2.34 中看到程序的输出。

![调用函数两次](img/img-f2.34.html)

**图 2.34** 调用函数两次

### 2.6.2 提取函数

你可以将经常需要且在不同程序中使用的函数定义提取到外部文件中。这样，你就可以创建自己的函数库。包含许多有用函数的大型库（如 jQuery 库）就是以此方式构建的。

在第 1.9 节中，我已经描述了如何集成外部文件。

以下是外部文件中的代码：

```html
... <head> ...
   <script>
      {
      }
   </script>
</head>
<script>
   greetings();
</body></html>
```

```html
... <head> ...
   function output(country, city)
         document.write("The capital of " + country + " is " + city + "<br>");
   </script>
<body><p>
   const a = "Spain", b = "Madrid";
   output("France", "Paris");
</body></html>
```

```html
... <head> ...
 function output(n, t, d, p)
         document.write(n + ", " + t + ", " + d + ", " + p + "<br>");

      {
         t = "Hello";

         document.write("In the function, element changed: ");

         document.write("In the function, field newly created: ");
      }
</head>
<p><script>
         person = [ "Peter", "Monica", "John" ];
      output(number, tx, done, person);
      change(number, tx, done, person);
      output(number, tx, done, person);
</body></html>
```

```html
... <head> ...
 function sum(a, b)
         const result = a + b;
      }
</head>
<p><script>
      const z = sum(x, y);
      document.write("Sum: " + sum(14, 20/4));
</body></html>
```

```html
... <head> ...
```

```javascript
{
   const temp = x;
   y = temp;
   return [x, y];
```

```html
</head>
<script>
let a = 7, b = 12;
[a, b] = swap(a, b);
```

```html
</body></html>
```

- 如果两个条件通过逻辑与连接，且第一个条件为假，则不再检查第二个条件，因为整个条件已经为假。

在此示例中，返回布尔值的函数被用于逻辑运算中。根据第一个函数的返回值，由于短路行为，第二个函数可能不再被调用。

为了理解以下示例程序，假设我们处于一个游戏场地，玩家允许的位置为 1 到 10。针对特定位置，需要检查某些相邻位置是否存在。

```html
<script>
function leftNeighbor(p)
   document.write("Function leftNeighbor()<br>");

   if (p > 1)
      return true;
   else
      return false;

function rightNeighbor(p)
{
   document.write("Function rightNeighbor()<br>");

   if (p < 10)
      return true;
   else
      return false;
}
</script>
</head>

<body><p>
<script>
if(leftNeighbor(5) || rightNeighbor(5))
   document.write("At least one neighbor exists<br>");
else
   document.write("No neighbor exists<br>");

document.write("<br>");

if(leftNeighbor(1) && rightNeighbor(1))
   document.write("Both neighbors exist<br>");
else
   document.write("Not both neighbors exist<br>");

document.write("<br>");

if(leftNeighbor(5) && rightNeighbor(5))
   document.write("Both neighbors exist<br>");
else
   document.write("Not both neighbors exist<br>");
</script></p>
</body></html>
```

**清单 2.33** `function_short_circuit.htm` 文件

第一个逻辑运算检查位置 5 是否存在至少一个邻居。由于已经存在左邻居，`rightNeighbor()` 函数不会被调用。

第二个逻辑运算检查位置 1 是否存在两个邻居。由于左邻居不存在，`rightNeighbor()` 函数同样不会被调用。

第三个逻辑运算检查位置 5 是否存在两个邻居。由于存在左邻居，`rightNeighbor()` 函数也会被调用。

你可以在图 2.40 中看到这些运算的输出。

![短路求值](img/img-f2.40.html)

**图 2.40** 短路求值

### 2.6.8 任意数量的参数

在标准情况下，调用函数时的参数数量应与期望的参数数量匹配。你可以使用 `arguments` 对象传递任意数量的参数。

以下程序展示了一个函数，它接受任意数量的参数并返回所有参数的总和：

```html
... <head> ...
<script>
function sum()
{
   let result = 0;

   for(let i=0; i<arguments.length; i++)
      result += arguments[i];

   return result;
}
</script>
</head>

<body><p>
<script>
const x = 12;

document.write("Sum: " + sum(3 * x, 3.5) + "<br>");
document.write("Sum: " + sum(-9, 3, x, 5.5) + "<br>");
document.write("Sum: " + sum());
</script></p>
</body></html>
```

**清单 2.34** `function_any.htm` 文件

首先来看函数的定义。函数名后的括号是空的，函数调用时传递的所有参数不仅可以在这些括号内使用，还可以在 `arguments` 对象中使用。该对象类似于一个字段，你可以通过 `arguments[0]` 访问第一个参数，通过 `arguments[1]` 访问第二个参数，以此类推。`length` 属性包含参数的数量。

为了计算总和，使用 `for` 循环遍历所有参数。确定参数的总和，并将其作为函数的返回值返回。

在程序中，你会看到对该函数的三种不同调用：一次有两个参数，一次有四个参数，一次没有参数。确定并输出参数的总和，不带参数的调用表明参数数量确实是任意的。

程序的输出如图 2.41 所示。

![任意数量的参数](img/img-f2.41.html)

**图 2.41** 任意数量的参数

### 2.6.9 参数的默认值

定义函数时，可以在参数列表末尾为个别参数分配默认值。这为你提供了另一种调用函数的方式，即使用不同数量的参数。

示例如下：

```html
... <head> ...
<script>
function add(a, b, c = 0, d = 0)
{
   const sum = a + b + c + d;
   return sum;
}
</script>
</head>

<body><p>
<script>
document.write("两个数：" + add(3, 5) + "<br>");
document.write("三个数：" + add(3, 5, 4) + "<br>");
document.write("四个数：" + add(3, 5, 4, 9));
</script></p>
</body></html>
```

**清单 2.35** `function_default.htm` 文件

`add()` 函数用于对两个、三个或四个值进行求和。最后两个参数的默认值为 0，因此总和不会失真。程序的输出如图 2.42 所示。

![带默认值的函数](img/img-f2.42.html)

**图 2.42** 带默认值的函数

### 2.6.10 变量的有效性

使用 `let` 或 `const` 声明的变量的有效性取决于声明的位置：

- 如果在花括号块外部声明，则在整个程序中有效。
- 如果在花括号块内部声明，则仅在该块内有效。该块也可以是一个函数，并且可以在不同块中声明多个同名变量。在块内，具有更大有效性的同名变量会被隐藏。

函数的参数仅在相关函数内有效，并且不能在所讨论函数的顶层声明同名变量。

在以下程序中，你可以看到上述关系：

```html
... <head> ...
<script>
function oscar(x)
{
   const a = 52;
   const d = 45;

   document.write("在函数内：a:" + a + ", b:" + b
      + ", x:" + x + ", d:" + d + "<br>");

   if(true)
   {
      const a = 62;

      document.write("在块内：a:" + a + ", b:" + b
         + ", x:" + x + ", d:" + d + "<br>");
   }
}
</script>
</head>

<body><p>
<script>
const a = 42;
const b = 43;
const c = 44;

document.write("在整个程序中：a:"
   + a + ", b:" + b + ", c:" + c + "<br>");

oscar(c);
</script></p>
</body></html>
```



**清单 2.36**　`function_validity.htm` 文件

变量 `a`、`b` 和 `c` 在文档的下半部分声明。它们在整个程序中有效，并且当调用 `oscar()` 函数时，变量 `c` 被传递。`oscar()` 函数中的变量 `x` 是 `c` 的副本，并且仅在函数内有效。

### 注意

你也可以在函数中使用原始的 `c` 变量，但在函数内部，应尽可能少地使用适用于整个程序的变量。如果函数外部需要某个变量，则应将其作为参数传递。这样更容易控制，也更难被意外更改。

函数内部声明了另一个名为 `a` 的变量。它隐藏了上述同名变量，并在整个函数内有效，变量 `d` 也在整个函数内有效。

在 `if` 之后的块内再次声明了一个名为 `a` 的变量。该变量隐藏了上述所有同名变量，并在整个 `if` 块内有效。

在图 2.43 中，你可以看到变量及其值。

![变量的有效性](img/img-f2.43.html)

**图 2.43**　变量的有效性

### 注意

应始终在尽可能靠近变量使用的位置声明变量（即在函数或块内，且在使用之前）。这样更容易控制，也更难被意外更改。

## 2.6.11 递归函数

函数也可以调用其他函数。这被称为嵌套调用，程序每次都会返回到调用点。函数也可以调用自身，这一过程称为递归。递归函数必须包含一个终止递归的分支；否则会导致无限的自调用链。解决某些问题最优雅的方式就是递归。

在以下程序中，一个数字被不断减半，直到达到或低于某个限制值。程序的输出如图 2.44 所示。

![递归函数](img/img-f2.44.html)

**图 2.44**　递归函数

以下是示例程序的代码：

```html
... <head> ...

   <script> 

   function halve(value, i)
   {
      document.write(i + ") " + value + "<br>");
      value /= 2;
      i++;

      if(value > 0.1)
         halve(value, i);

      document.write("结束 " + (i-1) + ")<br>");
   } 

   </script>
</head>

<body><p>
   <script> 

   const value = 3.5, i = 1;
   halve(value, i);
   document.write("程序结束"); 

   </script></p>
</body></html> 
```

**清单 2.37**　`function_recursive.htm` 文件

`halve()` 函数以初始值 3.5 被调用。输出该值，然后将其减半，如果值大于限制值 0.1，则函数再次调用自身。当达到或低于限制值时，递归结束。变量 `i` 在此用作调用次数的计数器。

在此示例中，递归在第六次调用时结束，函数首次终止。执行顺序返回到第五次运行的末尾，然后到第四次运行的末尾，依此类推，直到第一次运行的末尾。最后，程序结束。

本书中还有更多递归的示例，例如第 5 章的第 5.3 节。

## 2.6.12 匿名函数

到目前为止，我们一直在使用命名函数（即具有名称的函数）。然而，还有匿名函数（即没有名称的函数）。它们乍看起来有点不寻常，但在某些情况下，它们可以显著缩短程序代码。例如，匿名函数用于处理事件（参见第 4 章）或使用庞大的 jQuery 库（参见第 11 章）。

此外，你不仅可以处理对字段或对象的引用，还可以处理对函数的引用。可以将对函数的引用赋值给变量，也可以将对函数的引用作为参数传递。

以下是一个示例程序：

```html
... <head> ...

   <script> 

   const greeting = function()
   {
      document.write("Hello world<br>");
   }

   const sum = function(a,b)
   {
      const s = a + b;
      return s;
   }

   function oscar(welcome)
   {
      welcome();
   } 

   </script>
</head>

<body><p>
   <script> 

   greeting();

   oscar(greeting);

   const result = sum(35, 7);
   document.write(result + "<br>");

   const add = sum;
   document.write(add(45, 17) + "<br>");

   document.write((function() { return "Good morning<br>"; })());

   document.write((function(a, b) { return a * b; })(12, 6)); 

   </script></p>
</body></html> 
```

**清单 2.38**　`function_anonymous.htm` 文件

第一个匿名函数输出文本 `Hello world`，且定义时没有参数。该函数的引用被赋值给 `greeting` 变量。

在第二个匿名函数中，两个传入的参数相加，结果作为返回值返回。该函数的引用被赋值给 `sum` 变量。

这两个匿名函数都通过变量名后跟括号的方式调用，就像命名函数一样：`greeting()` 或 `sum(35, 7)`。

你可以将函数的引用传递给另一个函数。这里在调用 `oscar()` 函数时就发生了这种情况。在 `oscar()` 函数内部，`welcome` 名称引用了第一个匿名函数，因此 `welcome()` 调用会产生相同的结果。

引用函数的变量值可以赋值给另一个变量。这里将变量 `sum` 赋值给了变量 `add`，然后就可以使用 `add(...)` 调用来启动第二个匿名函数。

在程序末尾，你可以看到两个匿名函数，它们没有赋值给任何变量，而是直接调用：

- 第一个函数没有参数，返回文本 `"Good morning"`。返回的文本通过 `document.write()` 输出。
- 第二个匿名函数有参数 `a` 和 `b`，返回这两个参数的乘积。这里以值 12 和 6 调用它，同样，返回结果通过 `document.write()` 输出。

要调用匿名函数，必须将其整个定义括在圆括号中。后面跟着参数括号（如果有的话）。请始终留意多级括号。在图 2.45 中你可以看到程序的运行结果。

![匿名函数](img/img-f2.45.html)

**图 2.45**　匿名函数

## 2.6.13 回调函数

函数的引用可以传递给另一个函数供内部使用。在此上下文中，传递的函数被称为回调函数。你可以将命名函数和匿名函数作为回调函数传递。回调函数也用于处理事件（参见第 4 章）。

在下面的程序中，`output()` 函数被调用了两次。它用于输出一个常规的值序列。然后对每个值执行数学计算，计算结果显示在值旁边。

数学计算可以自由选择。它在一个函数中定义，并在调用时将该函数的引用传递给 `output()` 函数：

- 第一次调用传递了命名函数 `square()` 的引用，该函数返回传入值的平方。
- 第二次调用传递了一个匿名函数，该函数返回传入值的倒数。

程序如下：

```html
... <head> ...

   <script> 

   function square(x)
   {
      return x * x;
   }

   function output(from, to, step, fct)
   {
      for(let p = from; p < to + step / 2.0; p += step)
         document.write(p + " " + fct(p) + "<br>");

      document.write("<br>");
   } 

   </script>
</head>

<body><p>
   <script> 

   output(5.0, 15.0, 2.5, square);

   output(3.0, 7.0, 1.0, function(p) { return 1 / p; }); 

   </script></p>
</body></html> 
```

**清单 2.39**　`function_callback.htm` 文件

第一次调用计算从 5 到 15、步长为 2.5 的数的平方，第二次调用计算从 3 到 7、步长为 1 的数的倒数。

与第 2.6.12 节中的程序不同，匿名函数不需要放在圆括号中，因为这里并没有调用它。只是传递了函数的引用。

程序的输出如图 2.46 所示。

![回调函数](img/img-f2.46.html)

**图 2.46**　回调函数

# 3 自定义对象

在本章中，你将学习创建自己的对象，并更好地理解现有对象的结构。

在 JavaScript 中，你以面向对象的方式进行编程。有一系列预定义的对象：

- 你已经了解了 `window`、`document` 和 `Math` 对象。
- 在第 4 章的第 4.8 节中，你将使用 `location` 对象。
- 第 6 章描述了其他预定义对象。

然而，你也可以创建自己的对象，正如我将在本章中描述的那样。这允许你将主题相关的数据打包并访问，从而使你更容易理解和处理众多预定义对象。如果你的应用程序需要特殊选项，你可以通过继承来扩展自己的对象和预定义对象。

传统上，在 JavaScript 中，自定义对象是使用原型和构造函数创建的。自 ECMAScript 2015 标准引入以来，出现了一种新的标准表示法，其中使用类、构造函数、属性和方法，就像其他面向对象语言一样。所有现代浏览器都使用这种表示法，本书也只使用这种表示法。

原型概念只会在个别、独立的上下文中讨论。

## 3.1 对象和属性

本节描述如何定义一个名为 `Car` 的类，以及属性 `color` 和 `speed`。首先定义的类将在实际程序中使用，然后创建该类的两个对象并输出。同一类的不同对象彼此相关，它们具有相同的属性，但值不同。

程序如下：

```html
... <head> ...

   <script> 

   class Car
   {
      constructor(c, s)
      {
         this.color = c;
         this.speed = s;
      }
   } 

   </script>
</head>

<body>
   <p><script> 

   const dodge = new Car("Red", 50);

   document.write("Color: " + dodge.color
      + ", Speed: " + dodge.speed + "<br>");

   dodge.speed = 75;

   document.write("Color: " + dodge.color
      + ", Speed: " + dodge.speed + "<br>");

   let renault = new Car("Yellow", 65);
   renault = new Car("Blue", 85);

   document.write("Color: " + renault.color
      + ", Speed: " + renault.speed); 

   </script></p>
</body></html> 
```

**清单 3.1**　`obj_property.htm` 文件

`class` 关键字用于引入类的定义。注意，类的名称后面不跟括号，这与函数不同。

构造函数用于创建类的对象。它有固定的名称 `constructor`，其参数对应于该类对象的属性。

在构造函数中定义了两个属性，每个属性都使用 `this` 关键字、点运算符和一个名称。这两个属性被赋值为创建 `Car` 类对象时作为参数传递的值。`this` 关键字引用该对象（即当前对象），并确保访问当前对象的属性或为当前对象执行方法。

定义的类在实际程序中使用。声明了不可变的 `dodge` 变量，并使用 `new` 关键字为其分配了对 `Car` 类新对象的引用。两个值作为两个属性的初始值传递，然后可以使用点表示法访问对象的属性。这些值可以输出或更改。

然后，声明了 `renault` 变量，并连续两次将 `Car` 类的对象分配给该变量。这些对象也具有 `color` 和 `speed` 属性，但对象的属性值不同。

在声明引用对象的变量时，对象的情况与字段相同：如果不可变变量引用了一个对象，则只有引用是不可变的。你可以更改对象的各个元素，但不能将另一个对象分配给该变量。

程序的输出如图 3.1 所示。

![对象与属性](img/img-f3.1.html)

**图 3.1**　对象与属性

## 3.2 方法

方法是一种只能为其定义所在类的对象调用的函数。例如，`write()` 方法只有在使用点运算符为 `document` 对象调用时才会表现出熟悉的行为。方法通常用于更改相关类对象的属性，类的属性和方法统称为该类的成员。

在下面的示例中，第 3.1 节中的 `Car` 类得到了扩展。定义了 `paint()` 和 `accelerate()` 方法，用于更改 `color` 和 `speed` 属性。此外，还定义了一个名为 `toString()` 的特殊方法；它能够像输出变量一样简单地输出对象。

程序如下：

```html
... <head> ...

   <script> 

   class Car
   {
      constructor(c, s)
      {
         this.color = c;
         this.speed = s;
      }

      accelerate(value)
      {
         this.speed += value;
      }

      paint(c)
      {
         this.color = c;
      }

      toString()
      {
         return "Color: " + this.color
            + ", speed: " + this.speed;
      }
   } 

   </script>
</head>

<body><p>
   <script> 

   const dodge = new Car("Red", 50);

   document.write("Color: " + dodge.color
      + ", Speed: " + dodge.speed + "<br>");

   dodge.accelerate(35);
   dodge.paint("Blue");

   document.write(dodge); 

   </script></p>
</body></html> 
```

**清单 3.2**　`obj_method.htm` 文件

`accelerate()` 方法通过点运算符为 `dodge` 对象调用。该方法期望一个数值，用于更改 `speed` 属性的值，而 `paint()` 方法期望一个字符串，表示 `color` 属性的新值。

当调用 `document.write()` 方法需要输出对象本身时，会自动调用特殊的 `toString()` 方法。`toString()` 方法返回一个包含对象所有属性值的字符串（参见图 3.2）。

### 注意

你可以在本书的可下载材料中找到 `u_class` 练习，位于附加章节 1 的第 1.9 节，下载地址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

![使用方法](img/img-f3.2.html)

**图 3.2**　使用方法

## 3.3 私有成员

在本章之前的程序中，你可以直接从实际程序访问对象的属性和方法。因此，这些程序中的成员是公开可访问的，简称为公有成员。

然而，根据面向对象的数据封装原则，对象的属性应尽可能受到保护。应该通过方法对这些属性进行受控访问，并且某些仅用于类内部流程的方法也应受到保护。这种受保护的成员称为私有成员。

自 ECMAScript 2022 起，你可以使用井号字符 `#` 声明私有成员。以下是一个示例程序，其中声明了一个私有属性和一个私有方法：

```html
... <head> ...

   <script> 

   class Car
   {
```



```javascript
#color;

constructor(c, s)
{
   this.#color = c;
   this.speed = s;
}

accelerate(value)
{
   this.speed += value;
}

#paint(c)
{
   if (c == "Red" || c == "Yellow" || c == "Blue")
      this.#color = c;
}

change(c, value)
{
   this.#paint(c);
   this.accelerate(value);
}

toString()
{
   return "Color: " + this.#color
      + ", speed: " + this.speed;
}
```

```html
</script>
</head>
<body>
   <p><script>
```

```javascript
const dodge = new Car("Red", 50);
document.write(dodge + "<br>");
// document.write("Color: " + dodge.#color + "<br>");
dodge.change("Green", 25);
document.write(dodge + "<br>");
dodge.change("Blue", 10);
document.write(dodge + "<br>");
// dodge.#paint("Yellow");
```

```html
</script></p>
</body></html>
```

**清单 3.3**　obj_private.htm 文件

私有属性在方法外部声明，通常位于类定义的开头。这里通过`#color;`语句完成。在类定义内部，通过`this.#color`访问该属性。在类定义外部则无法再访问。

要定义私有方法，需要在方法名称前加上`#`，如`#paint(c)`方法头所示。在类定义内部，通过`this.#paint(...)`访问该方法。在类定义外部则无法访问。

在`paint()`方法中，注意确保只能使用允许的颜色：红色、黄色或蓝色。这样，私有属性`color`就得到了保护。你可以在图 3.3 中看到程序运行结果。

![访问私有成员](img/img-f3.3.html)

**图 3.3**　访问私有成员

## 3.4　设置器与获取器

自 ECMA 2022 起，你也可以使用设置器（setter）和获取器（getter）（即所谓的访问器）来对属性进行受控访问。设置器用于写访问，使用`set`关键字；获取器用于读访问，使用`get`关键字。

以下是一个示例程序，其中为私有属性定义了访问器：

```html
... <head> ...
<script>
```

```javascript
class Car
{
   #speed;

   constructor(c, s)
   {
      this.color = c;
      this.setSpeed = s;
   }

   get getSpeed()
   {
      return this.#speed;
   }

   set setSpeed(s)
   {
      if (s < 0)        s = 0;
      else if (s > 100) s = 100;
      this.#speed = s;
   }

   accelerate(value)
   {
      this.setSpeed = this.getSpeed + value;
   }

   toString()
   {
      return "Color: " + this.color
         + ", Speed: " + this.getSpeed;
   }
}
```

```html
</script>
</head>
<body>
   <p><script>
```

```javascript
const dodge = new Car("Red", 150);
document.write(dodge + "<br>");
dodge.accelerate(20);
document.write(dodge + "<br>");
dodge.accelerate(-120);
document.write(dodge + "<br>");
dodge.accelerate(30);
document.write(dodge + "<br>");
```

```html
</script></p>
</body></html>
```

**清单 3.4**　obj_accessor.htm 文件

在程序中，私有属性`speed`的值只能通过`accelerate()`方法更改。在该方法中，首先使用`getSpeed`获取器获取`speed`属性的当前值，获取器像方法一样通过`return`返回值。

在赋值语句的右侧计算`speed`属性的新值。赋值本身会调用`setSpeed`设置器，新值作为参数传递，就像调用方法一样。设置器确保速度的新值仅在 0 到 100 的允许范围内，然后将其赋给私有属性`speed`。

设置器也在类的构造函数中使用，以限制属性的值。程序的输出如图 图 3.4 所示。

![使用访问器进行控制](img/img-f3.4.html)

**图 3.4**　使用访问器进行控制

## 3.5　静态成员

同一类的不同对象通常具有不同的属性值。除了这些与对象相关的属性外，你还可以定义静态属性，这些属性与整个类相关，并且所有对象都可以使用相同的值。你还可以定义静态方法，这些方法也引用整个类，并针对该类进行调用。

以下是一个示例程序，其中使用`static`关键字在类中声明了一个静态属性，并定义了一个静态方法：

```html
... <head> ...
<script>
```

```javascript
class Car
{
   static quantity = 0;

   constructor(c, s)
   {
      this.color = c;
      this.speed = s;
      Car.quantity = Car.quantity + 1;
      this.number = Car.quantity;
   }

   toString()
   {
      return "Color: " + this.color + ", Speed: "
         + this.speed + ", Number: " + this.number;
   }

   static output_quantity()
   {
      document.write("Quantity: " + Car.quantity + "<br>");
   }
}
```

```html
</script>
</head>
<body>
   <p><script>
```

```javascript
const dodge = new Car("Red", 50);
document.write(dodge + "<br>");
const renault = new Car("Yellow", 65);
document.write(renault + "<br>");
document.write("Quantity: " + Car.quantity + "<br>");
Car.output_quantity();
```

```html
</script></p>
</body></html>
```

**清单 3.5**　obj_static.htm 文件

静态属性在方法外部声明，通常位于类定义的开头，并赋予一个初始值。在这里，我们在构造函数中对其进行读写访问。

静态属性`quantity`用于确定类中创建的对象数量。它还为每个对象赋予一个独立的`number`属性值，该值表示对象按创建顺序的序号。

静态属性`quantity`必须在方法内部和程序中通过类名访问（即通过`Car.quantity`）。

静态方法`output_quantity()`输出一行指定对象数量的信息，该方法必须在程序中或其他方法内部通过类名调用（即`Car.output_quantity()`）。

程序的输出如图 图 3.5 所示。

![静态成员的使用](img/img-f3.5.html)

**图 3.5**　静态成员的使用

## 3.6　静态块

自 ECMAScript 2022 起，你可以使用静态块对类进行一次性初始化。它们通常也写在类定义的开头，并且可以在这样的语句块中定义静态属性。这样的块还可以包含其他要执行的语句。

在下面的程序片段中，你只会看到与 obj_static.htm 程序不同的那些行：

```html
... <head> ...
<script>
```

```javascript
class Car
{
   static
   {
      Car.quantity = 0;
   }

   constructor(c, s)
   { ...
```

**清单 3.6**　obj_static_block.htm 文件片段

静态块使用`static`关键字引入。在其中声明的变量是静态的，由于变量位于块内，必须通过类名访问。程序的输出与 obj_static.htm 程序相同，如图 3.5 所示。

## 3.7　空引用

在与对象相关的场景中，一个给定的变量可以引用空值而不是一个对象。这种情况可能发生在该变量被赋值为`null`之后，也可能发生在变量本应引用一个文档中不存在的 DOM 元素时（参见第 5 章）。

引用空值的变量具有值`null`，而空引用常常导致程序中止。有两个运算符可以防止这种情况发生：

- 空值合并运算符`??`
- 可选链运算符`?.`

以下程序展示了这些运算符的使用示例：

```html
... <head> ...
<script>
```

```javascript
class Car
{
   constructor(c, s)
   {
      this.color = c;
      this.speed = s;
   }

   toString()
   {
      return "Color: " + this.color
         + ", speed: " + this.speed;
   }
}
```

```html
</script>
</head>
<body><p>
   <script>
```

```javascript
let dodge = new Car("Red", 50);
document.write((dodge ?? "Object does not exist") + "<br>");
document.write("Color: " + dodge?.color + "<br>");
dodge = null;
document.write((dodge ?? "Object does not exist") + "<br>");
// document.write("Color: " + dodge.color + "<br>");
document.write("Color: " + dodge?.color + "<br>");
```

```html
</script></p>
</body></html>
```

**清单 3.7**　obj_null.htm 文件

使用空值合并运算符`??`时，会检查左操作数。如果其值为`null`，则返回右操作数；否则返回左操作数。

然后，由于`dodge`变量引用的对象存在，因此输出该对象。为了演示，程序中随后将该引用赋值为`null`，这意味着`dodge`不再引用任何对象，从而导致显示文本`"Object does not exist"`。

点运算符`.`用于访问对象的属性和方法。如果对象不存在，程序将中止。因此，程序中的倒数第二条语句被注释掉了。

可选链运算符`?.`也用于访问对象的属性和方法。如果对象不存在，则返回`undefined`值，程序不会中止。

程序的输出如图 3.6 所示。

![引用空对象](img/img-f3.6.html)

**图 3.6**　引用空对象

## 3.8　对象中的对象

一个类的对象的属性可以是另一个类的对象。为了阐明这种关系，我们通过`Engine`类的`drive`属性来扩展`Car`类。

以下是示例程序：

```html
... <head> ...
<script>
```

```javascript
class Engine
{
   constructor(p, c, f)
   {
      this.power = p;
      this.cylinders = c;
      this.fuel = f;
   }

   tune(x)
   {
      this.power += x;
   }

   toString()
   {
      return "Power: " + this.power + ", Cylinders: "
         + this.cylinders + ", fuel: " + this.fuel;
   }
}

class Car
{
   constructor(c, s, d)
   {
      this.color = c;
      this.speed = s;
      this.drive = d;
   }

   toString()
   {
      return "Color: " + this.color + ", Speed: "
         + this.speed + ", Drive: " + this.drive;
   }
}
```

```html
</script>
</head>
<body><p>
   <script>
```

```javascript
const dodge = new Car("Red", 50,
   new Engine(60, 4, "Diesel"));

dodge.drive.tune(10);
document.write(dodge + "<br>");

dodge.drive.power = 80;
dodge.drive.cylinders = 6;
dodge.drive.fuel = "Gasoline";

document.write(dodge);
```

```html
</script></p>
</body></html>
```



**清单 3.8**　`obj_in_object.htm` 文件

`Engine` 类的对象具有 `power`、`cylinders` 和 `fuel` 属性。此外，还有用于改变性能的 `tune()` 方法和用于输出三个属性值的 `toString()` 方法。

`Car` 类中添加了 `drive` 属性，并且该属性的值也通过 `toString()` 方法输出。

程序中创建了一个 `Car` 类的对象，第三个参数是一个 `Engine` 类的对象，该对象也通过 `new` 创建。

`dodge` 对象名称后的第一个点用于访问 `Car` 对象的 `drive` 属性，第二个点则指向 `Engine` 对象的子属性。

调用 `Car` 类的 `toString()` 方法来输出 `Car` 对象，该方法内部通过 `this.drive` 调用了 `Engine` 类的同名方法。整个字符串就是这样构建的，如图 3.7 所示。

![Car 对象中的 Engine 对象](img/img-f3.7.html)

**图 3.7**　Car 对象中的 Engine 对象

## 3.9　继承

如果你需要一个类，它拥有已在另一个类中定义的属性，那么可以使用继承原则。在这种情况下，你可以在基类的基础上创建一个派生类，并添加额外的属性。

在以下示例中，基于 `Car` 基类创建了派生类 `Truck`。`Truck` 类的对象应具有额外的 `payload` 属性和 `load()` 方法，并且两个类各自拥有自己的 `toString()` 方法定义。

以下是程序：

```html
... <head> ...

   <script>
```

```javascript
 class Car
      {
         constructor(c, s)
         {
            this.color = c;
            this.speed = s;
         }
         accelerate(value)
         {
            this.speed += value;
         }
         toString()
         {
            return "Color: " + this.color
               + ", Speed: " + this.speed;
         }
      }

      class Truck extends Car
      {
         constructor(c, s, p)
         {
            super(c, s);
            this.payload = p;
         }
         load(value)
         {
            this.payload += value;
         }
         toString()
         {
            return super.toString() + ", Payload: " + this.payload;
         }
      }
```

```html
   </script>
</head>

<body><p>
   <script>
```

```javascript
 const kenworth = new Truck("Orange", 30, 15);

      document.write(kenworth + "<br>");

      kenworth.accelerate(50);

      kenworth.load(25);

      document.write(kenworth);
```

```html
   </script></p>
</body></html>
```

**清单 3.9**　`obj_inheritance.htm` 文件

`Car` 基类的构造函数期望两个参数，分别用于 `color` 和 `speed` 属性的初始值。派生类 `Truck` 的构造函数期望三个参数，分别是 `Car` 基类的 `color` 和 `speed` 属性的初始值，以及派生类 `Truck` 的 `payload` 属性的初始值。

`super()` 方法在构造函数中调用基类的特定构造函数，通过这种方式，前两个参数被传递给基类的构造函数。第三个参数被赋值给 `payload` 属性，这样 `Truck` 类对象的所有属性都被赋予了初始值。

此外，还有 `super` 引用（不带括号），用于访问基类的属性和方法。在派生类 `Truck` 的 `toString()` 方法中，调用了 `Car` 基类的同名方法：`super.toString()`。

程序创建并输出一个带有三个初始值的 `Truck` 类对象。通过调用基类的 `accelerate()` 方法和派生类的 `load()` 方法对其进行修改，然后再次输出，如图 3.8 所示。

![继承](img/img-f3.8.html)

**图 3.8**　继承

### 注意

关于继承主题，你可以在本书的可下载材料中找到附加章节 1 第 1.10 节中的 `u_inheritance` 练习，下载地址为 [www.rheinwerk-publishing.com/5875](http://www.rheinwerk-publishing.com/5875)。

## 3.10　对象的操作

在本节中，你将看到一个示例程序，其中对一个类、其属性和方法以及该类的某些对象执行了许多有用的操作和检查。该类在文档的 `head` 中定义如下：

```html
... <head> ...

   <script>
```

```javascript
 class Car
      {
         constructor(c, s)
         {
            this.color = c;
            this.speed = s;
         }
         accelerate(value)
         {
            this.speed += value;
         }
         paint(c)
         {
            this.color = c;
         }
         toString()
         {
            return "Color: " + this.color
               + ", Speed: " + this.speed;
         }
      }
```

```html
   </script>
</head>
```

**清单 3.10**　`obj_operation.htm` 文件，第 1 部分（共 8 部分）

### 3.10.1　访问运算符

访问对象的属性有两种方式。第一种是使用点运算符 `.`，第二种是使用方括号 `[]`。你可以在以下程序片段中看到这一点：

```html
<body><p>
   <script>
```

```javascript
 const dodge = new Car("Red", 50);

      document.write("Notation with dot: " + dodge.color + " "
         + dodge.speed + "<br>");

      document.write("Notation with [ and ]: " + dodge["color"]
         + " " + dodge["speed"] + "<br>");

      document.write("Notation with toString(): "
         + dodge + "<br><br>");
```

**清单 3.11**　`obj_operation.htm` 文件，第 2 部分（共 8 部分）

创建对象后，其属性被多次输出。在方括号内，属性名以字符串形式写在双引号中。你可以从各个部分组合这个字符串，也可以使用变量，这种表示法使程序的创建更加灵活。你可以在图 3.9 中看到输出结果。

![访问选项与比较](img/img-f3.9.html)

**图 3.9**　访问选项与比较

### 3.10.2　创建和比较对象引用

如果将引用对象的变量赋值给另一个变量，并不会创建新对象或原始对象的副本，而只是创建了对同一对象的第二个引用。然后你可以通过这两个变量访问同一个对象（另请参见图 3.9）。

两个比较运算符 `==` 和 `!=` 可用于检查两个变量是否引用同一个对象。

在程序的以下部分中，变量以如下方式相互比较：

- 首先，有两个变量引用同一个对象。
- 其次，有两个变量引用两个不同的对象，但具有相同的属性和属性值。

```javascript
 const renault = dodge;

      document.write("Second reference: " + renault + "<br>");

      if(renault == dodge)
         document.write("Same object<br>");

      const simca = new Car("Red", 50);

      if(simca != dodge)
         document.write("Not the same object<br><br>");
```

**清单 3.12**　`obj_operation.htm` 文件，第 3 部分（共 8 部分）

你也可以在图 3.9 中看到这个输出。

关于对象的复制，请参考第 3.11 节。

### 3.10.3　检查实例

类的对象被称为类的实例，创建对象的过程称为实例化。`instanceof` 运算符检查一个对象是否是某个特定类（或其基类）的实例：

```javascript
if(dodge instanceof Car)
   document.write("instanceof:<br>Object is an instance of the class<br><br>");
```

**清单 3.13**　`obj_operation.htm` 文件，第 4 部分（共 8 部分）

你可以在图 3.10 中看到输出结果。

![instanceof 和 typeof 运算符](img/img-f3.10.html)

**图 3.10**　instanceof 和 typeof 运算符

### 3.10.4　确定类型

`typeof` 运算符返回变量的类型（另请参见第 2 章，第 2.3.6 节），类的方法具有函数类型，类的对象具有对象类型。JavaScript 中的类基于原型和构造函数，因此类本身也具有函数类型，如下所示：

```javascript
 document.write("typeof:<br>"
         + "Car: " + typeof Car + "<br>"
         + "dodge: " + typeof dodge + "<br>"
         + "color: " + typeof dodge.color + "<br>"
         + "speed: " + typeof dodge.speed + "<br>"
         + "accelerate: " + typeof dodge.accelerate + "<br>"
         + "paint: " + typeof dodge.paint + "<br><br>");
```

**清单 3.14**　`obj_operation.htm` 文件，第 5 部分（共 8 部分）

在图 3.10 中，你可以看到 `Car` 类以及 `accelerate()` 和 `paint()` 方法具有函数类型，而 `dodge` 对象具有对象类型。这两个属性是字符串或数字类型的简单变量。

### 3.10.5　检查成员

你可以使用 `in` 运算符检查一个类是否具有特定的成员（即特定的属性或方法）：

```javascript
 document.write("in:<br>");

      if("color" in dodge)
         document.write("color is member<br>");

      if("accelerate" in dodge)
         document.write("accelerate is member<br>");

      if("paint" in dodge)
         document.write("paint is member<br>");

      if(!("power" in dodge))
         document.write("power is no member<br><br>");
```

**清单 3.15**　`obj_operation.htm` 文件，第 6 部分，共 8 部分

检查结果显示，字符串 `color`、`accelerate` 和 `paint` 是 `dodge` 对象所属类的成员，但 `power` 不是，如图 3.11 所示。

![in 运算符、对象与函数](img/img-f3.11.html)

**图 3.11**　in 运算符、对象与函数

### 3.10.6　对象与函数

你可以将一个代表对象引用的变量作为参数传递给函数。在函数内部，你可以修改该对象或调用其方法，也可以将一个代表对象引用的变量作为返回值从函数中返回，并将其赋值给另一个变量：

```javascript
 function change(x)
      {
         x.accelerate(10);
         return x;
      }

      const lada = change(dodge);
      document.write(lada + "<br><br>");
```

**清单 3.16**　`obj_operation.htm` 文件，第 7 部分，共 8 部分

变量 `dodge`、参数 `x` 和变量 `lada` 引用的是同一个对象。你同样可以在图 3.11 中看到输出结果。

### 3.10.7　删除属性

你可以使用 `delete` 运算符删除对象的单个属性。同一类的其他对象的属性不受此影响，但这个过程会产生一个副作用：这些对象不再相似。

最后，这是程序的最后一部分：

```javascript
 delete dodge.speed;

      document.write("Values of members:<br>"
         + "color: " + dodge.color + "<br>"
         + "speed: " + dodge.speed + "<br>"
         + "paint: " + dodge.paint + "<br>"
         + "power: " + dodge.power);
```

```html
   </script></p>
</body></html>
```

**清单 3.17**　`obj_operation.htm` 文件，第 8 部分，共 8 部分

`speed` 属性被删除，之后输出了 `color`、`speed`、`paint` 和 `power` 属性的值。`speed` 属性已不存在，而 `power` 属性从未存在过。你可以在图 3.12 中看到最终的输出结果。

![删除操作后的属性值](img/img-f3.12.html)

**图 3.12**　删除操作后的属性值

## 3.11　复制对象

要复制一个对象，仅仅复制引用该对象的变量是不够的（另请参见第 3.10.2 节）。相反，必须创建一个新对象，并将其属性赋值为原始对象的值。

以下程序中的类包含一个用于复制该类对象的方法：

```html
... <head> ...

   <script>
```

```javascript
 class Car
      {
         constructor(c, s)
         {
            this.color = c;
            this.speed = s;
         }
         accelerate(value)
         {
            this.speed += value;
         }
         toString()
         {
            return "Color: " + this.color
               + ", Speed: " + this.speed;
         }
         copy()
         {
            const c = new Car(this.color, this.speed);
            return c;
         }
      }
```

```html
   </script>
</head>

<body><p>
   <script>
```

```javascript
 const dodge = new Car("Red", 50);

      document.write(dodge + "<br>");

      const renault = dodge.copy();

      dodge.accelerate(25);

      document.write(dodge + "<br>");

      document.write(renault + "<br>");
```

```html
   </script></p>
</body></html>
```



**清单 3.18**　`obj_copy_flat.htm` 文件

在 `copy()` 方法中创建了一个 `Car` 类的新对象，并将当前对象的两个属性值传递给构造函数。这意味着新对象是当前对象的一个副本。`copy()` 方法返回对这个新对象的引用。

程序中调用了 `dodge` 对象的 `copy()` 方法，并将该方法的结果（即对新对象的引用）赋值给变量 `renault`。于是就有了两个对象，它们的属性可以具有不同的值。

程序的输出结果如图 3.13 所示。

![原始对象与副本](img/img-f3.13.html)

**图 3.13**　原始对象与副本

前面示例中类的属性可以通过简单的赋值来复制，因为它们具有简单的数据类型，例如字符串、数字或布尔值。在这种情况下，浅拷贝就足够了。

然而，如果某个属性具有非简单数据类型，例如字段或对象，则必须进行深拷贝。深拷贝涉及将字段中所有元素的值复制到新字段，或者将对象的属性值复制到新对象。

接下来使用你已经从第 3.9 节中了解到的 `Car` 和 `Engine` 类，其中 `Car` 类的 `drive` 属性是一个 `Engine` 类的对象。以下是一个程序片段，该程序使用总共两个复制方法复制了一个 `Car` 类的对象：

```html
... <head> ...

   <script>
```

```javascript
class Engine
{
   constructor(p, c, f)
   {
      this.power = p;
      this.cylinders = c;
      this.fuel = f;
   }

   tune(x)
   {
      this.power += x;
   }

   toString()
   {
      return "Power: " + this.power + ", Cylinders: "
         + this.cylinders + ", Fuel: " + this.fuel;
   }

   copy()
   {
      const e = new Engine(this.power, this.cylinders, this.fuel);
      return e;
   }
}

class Car
{
   constructor(c, s, d)
   {
      this.color = c;
      this.speed = s;
      this.drive = d;
   }

   toString()
   {
      return "Color: " + this.color + ", Speed: "
         + this.speed + ", Drive: " + this.drive;
   }

   copy()
   {
      const c = new Car(
         this.color,
         this.speed,
         this.drive.copy()
      );
      return c;
   }
}
```

```html
</script>
</head>

<body><p>
   <script>
```

```javascript
const dodge = new Car("Red", 50, new Engine(60, 4, "Diesel"));

document.write(dodge + "<br>");

const renault = dodge.copy();

dodge.drive.tune(15);

document.write(dodge + "<br>");
document.write(renault + "<br>");
```

```html
</script></p>
</body></html>
```

**清单 3.19**　`obj_copy_deep.htm` 文件片段

当 `Car` 类的对象被复制时，会调用该类的 `copy()` 方法。这会创建一个新的 `Car` 类对象，并将原始对象的 `color` 和 `speed` 属性的值赋给新对象。

对于第三个属性（`drive`），过程稍微复杂一些。首先，针对该属性调用 `Engine` 类的 `copy()` 方法，这会创建一个新的 `Engine` 类对象。原始 `Engine` 类对象的三个属性的值被赋值，然后返回对新创建对象的引用，该引用被传递给 `Car` 类的 `copy()` 方法，并赋给 `Car` 类的 `drive` 属性。

你可以在图 3.14 中看到程序的结果。

![原始副本与深拷贝](img/img-f3.14.html)

**图 3.14**　原始副本与深拷贝

# 4　表单与事件

在本章中，你将学习如何检查表单和处理事件。

表单能够实现类似于你在计算机上其他应用程序中习惯的交互。你可以进行输入并触发处理，然后程序返回结果。

表单也用于将数据传输到 Web 服务器。在发送之前，可以通过 JavaScript 检查其内容的有效性。这避免了不必要的网络流量。

JavaScript 还允许你编写能够响应浏览器事件的程序。通过这种方式，你可以与程序进行交互，而不仅仅是 `prompt()` 和 `confirm()` 函数的简单返回值。这些事件可能涉及按钮点击、从列表中选择条目、使用鼠标的特定操作、表单提交等等。

如果你希望程序响应某个事件，你需要开发包含在事件发生时必须执行的语句的 JavaScript 程序代码。事件处理程序用于处理事件；它在事件触发的文档部分、事件本身以及 JavaScript 程序代码之间建立联系。

## 4.1　第一个表单和第一个事件

在本节中，你将了解处理事件所需的一些典型元素。

以下示例展示了一个包含输入字段 `Input` 和按钮 `Click` 的表单。在输入字段中输入文本后，你必须点击按钮（参见图 4.1），然后会出现一个包含信息的对话框（参见图 4.2）。

![带输入字段和按钮的表单](img/img-f4.1.html)

**图 4.1**　带输入字段和按钮的表单

![对事件的响应](img/img-f4.2.html)

**图 4.2**　对事件的响应

你也可以使用输入字段在已完全映射的文档中后续输出信息。在示例中，输出字段中显示的信息与对话框中的相同（参见图 4.3）。你可以使用 `disabled` 属性确保无法在此字段中进行输入。

![输出字段](img/img-f4.3.html)

**图 4.3**　输出字段

以下是程序：

```html
... <head> ...

   <script>
```

```javascript
function clicked()
{
   const inputField = document.getElementById("idInput");
   const input = inputField.value;

   alert("Click: " + input);

   const outputField = document.getElementById("idOutput");
   outputField.value = "Click: " + input;
}
```

```html
</script>
</head>

<body>
   <form>
      <p><input id="idInput"> Input</p>
      <p><input id="idButton" type="button" value="Click"></p>
      <p><input id="idOutput" disabled> Output</p>
   </form>

   <script>
```

```javascript
const bu = document.getElementById("idButton");
bu.addEventListener("click", clicked);
```

```html
</script>
</body></html>
```

**清单 4.1**　`form_click.htm` 文件

表单的元素位于 `form` 容器中，而 `input` 类型的简单元素对应单行输入字段。如果为 `input` 元素的 `type` 属性指定了 `button` 值，则会显示一个按钮，并且 `value` 属性的值对应按钮上的文本。

`id` 属性的值作为文档中元素的唯一标识符（ID）。该 ID 用于访问元素并与 JavaScript 程序代码连接。

在下面的 `script` 容器中，调用了 `document` 对象的 `getElementById()` 方法。它期望一个元素的 ID 作为参数，并返回一个引用，该引用指向表示该元素的对象。在示例中，该引用保存在 `bu` 变量中，因此 `bu` 引用了按钮。

事件监听器检测事件并对其做出响应，而 `element` 对象的 `addEventListener()` 方法将文档中的元素与特定事件以及命名函数或匿名函数的引用链接起来。在本例中，这意味着点击 `bu` 按钮会触发 `click` 事件，从而调用命名函数 `clicked()`。

在 `clicked()` 函数中，`inputField` 变量引用了输入字段。输入字段的 `value` 属性包含输入的文本，该文本显示在对话框中。

`outputField` 变量引用了用于输出的输入字段。`value` 属性也可以被赋值，从而改变输入字段的内容。

### 注意

你可以在本书的下载材料中找到 `u_form` 练习，位于附加章节 1 的第 1.11 节，下载地址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

### 注意

自 JavaScript 早期以来，文档元素与程序代码之间的连接使用了不同的技术。现代浏览器熟悉 `getElementById()` 和 `addEventListener()` 方法及其多种用途。

## 4.2　提交与重置

对于表单，可能会发生提交和重置事件。可以使用表单将数据提交到 Web 服务器，而重置过程会将表单的值设置为其初始值。

以下示例响应这两个事件。此外，表单的内容被发送到一个包含 PHP 程序的文件，该程序位于 Web 服务器上并进一步处理数据。在此示例中，传输的数据仅显示在屏幕上。

PHP 是一种广泛用于 Web 服务器的编程语言，但你无需学习 PHP 也能理解本示例。这里只是要阐明完整的流程。

### 4.2.1　提交过程

在图 4.4 中，你可以看到对 `form_submit.htm` 文件的调用。与之前的示例一样，它是从 JavaScript 程序的目录中调用的。在我的例子中，该目录是 `C:\js`。

![从目录调用表单](img/img-f4.4.html)

**图 4.4**　从目录调用表单

图 4.5 展示了 JavaScript 对提交的响应。

![JavaScript 对提交的响应](img/img-f4.5.html)

**图 4.5**　JavaScript 对提交的响应

由于整个过程并非在 Web 服务器上进行，因此无法正确调用 PHP 文件。只会显示你的代码（参见图 4.6）。针对此问题的解决方法见第 4.2.2 节。

![PHP 响应代码](img/img-f4.6.html)

**图 4.6**　PHP 响应代码

如果你重置表单而不是提交它，响应将如图 4.7 所示。

![重置表单的响应](img/img-f4.7.html)

**图 4.7**　重置表单的响应

### 4.2.2　作为替代方案的 Web 服务器

如果你想在 Web 服务器上跟踪整个传输过程，有两种替代方案：

- 你可以在自己的计算机上使用本地 Web 服务器，并通过该 Web 服务器调用表单。为此，你需要安装免费提供的 XAMPP 程序包，并将涉及的两个文件——`form_submit.htm` 和 `form_submit.php`——保存到 Web 服务器的某个目录中。例如，这可以是基础目录下的 `jse` 目录。调用 `form_submit.htm` 文件并提交表单后，PHP 程序的响应将如图 4.8 所示。XAMPP 的安装和使用在附录 A 的第 A.2 节中进行了描述。

  ![通过本地 Web 服务器的响应](img/img-f4.8.html)

  **图 4.8**　通过本地 Web 服务器的响应

- 你是否可以将数据存储到互联网服务器上？如果可以，你可以将涉及的两个文件——`form_submit.htm` 和 `form_submit.php`——上传到互联网服务器的某个目录中。我已将这些文件保存到我的域名 [theisweb.de](http://www.theisweb.de) 下的 `jse` 目录中。该目录的地址是 [`theisweb.de/jse`](https://theisweb.de/jse)，你可以在那里找到本书所有程序的超链接，并按它们在章节中出现的顺序排列。本章中的其他示例均通过我的域名访问，即使并非所有程序都需要这样做。

  调用 `form_submit.htm` 文件并提交表单后，PHP 程序的响应如图 4.9 所示。

  ![通过互联网服务器的响应](img/img-f4.9.html)

  **图 4.9**　通过互联网服务器的响应

如果你不使用这两种替代方案，而只是从目录中调用带有表单的程序，也没有问题。你仍然可以使用 JavaScript 代码。

### 4.2.3　提交代码

以下是包含提交表单的文件的代码：

```html
... <head> ...

   <script>
```

```javascript
function submit()
{
   const tx = document.getElementById("idText");
   const entry = tx.value;

   alert("Form will be sent\nEntry: " + entry);
}

function reset()
{
   alert("Form will be reset");
}
```

```html
</script>
</head>

<body>
   <form id="idForm" method="post" action="form_submit.php">
      <p><input id="idText" name="entry"> Enter text</p>
      <p><input type="submit"> <input type="reset"></p>
   </form>

   <script>
```

```javascript
const fo = document.getElementById("idForm");

fo.addEventListener("submit", submit);
fo.addEventListener("reset", reset);
```

```html
</script>
</body></html>
```

**清单 4.2**　`form_submit.htm` 文件

该表单具有唯一 ID `idForm`，并使用 `method` 属性的 `post` 值来定义安全的传输方法 `post`，所有示例均采用此方法。`action` 属性的值引用了响应的 PHP 程序，我们假设该程序位于同一目录中。

输入字段具有唯一 ID `idText`，这是使用 JavaScript 访问字段内容所必需的。输入字段还具有 `name` 属性，此处值为 `entry`，这是使用 PHP 访问字段内容所必需的。

两个 `input` 元素的 `type` 属性的 `submit` 和 `reset` 值将它们标识为用于提交或重置表单的按钮。

`fo` 变量引用了表单，`addEventListener()` 方法用于将 `submit` 和 `reset` 事件与命名函数 `submit()` 和 `reset()` 关联起来。

### 4.2.4　接收代码

如前所述，你无需学习 PHP——但为了提供信息和说明，这里例外地给出了接收 PHP 文件的代码，正如你在图 4.6 中已经看到的那样：

```php
<!DOCTYPE html>
<html lang="en-us">

<head>
   <meta charset="utf-8">
   <title>Response from the web server</title>
   <link rel="stylesheet" href="js5.css">
</head>

<body><p>

<?php
   echo "Entry: " . htmlentities($_POST["entry"]) . "<br>";
?>

</p></body>
</html>
```



**清单 4.3**　`form_submit.php` 文件

这是一个标准的 HTML 文档，PHP 代码嵌入在 `<?php` 和 `?>` 之间的容器中。语言元素 `echo` 用于在屏幕上输出，点号（`.`）用于连接各个文本部分，类似于 JavaScript 中的加号（`+`）。

表单中具有 `name` 属性的元素会自动以其属性值成为 PHP 字段 `$_POST` 的元素。具体如下：`name="entry"` 变为 `$_POST["entry"]`。

`htmlentities()` 函数用于防范恶意用户可能通过输入字段向 Web 服务器传输的恶意代码的影响。

本书中几乎所有表单示例都配有相应的 PHP 文件，以说明处理过程。

## 4.3　必填字段与检查

你可以使用 HTML 轻松验证表单中的条目（即检查其有效性）。还可以使用 JavaScript 对表单中输入或选择的内容进行进一步验证。

在以下示例中，必须在两个必填字段中输入姓氏和密码（参见图 4.10），并且可以在多行输入字段中输入评论。单击“提交”按钮时会发生以下情况：

- 如果两个必填字段中有一个为空，则会在表单内显示一条错误消息（参见图 4.11），并且表单不会被提交。
- 如果输入的密码少于三个字符或多于八个字符，JavaScript 会显示一条错误消息（参见图 4.12），并且表单不会提交。
- 如果两个必填字段都已填写且密码长度正确，则表单会提交。

当你对字符串的结构和处理有了更多了解后，可以执行进一步的检查。在第 6 章的第 6.2.5 节中，你可以找到一个更长的示例。

![必填字段和多行输入字段](img/img-f4.10.html)

**图 4.10**　必填字段和多行输入字段

![来自 HTML 的错误消息](img/img-f4.11.html)

**图 4.11**　来自 HTML 的错误消息

![来自 JavaScript 的错误消息](img/img-f4.12.html)

**图 4.12**　来自 JavaScript 的错误消息

以下是包含表单的文件代码：

```html
... <head> ...

   <script>
```

```javascript
 function submit(e)
      {
         const pw = document.getElementById("idPassword").value;

         if(pw.length < 3 || pw.length > 8)
         {
            alert("Password must contain 3-8 characters");
            e.preventDefault();
            return false;
         }

         alert(document.getElementById("idFamilyName").value
            + "\n" + document.getElementById("idPassword").value
            + "\n" + document.getElementById("idComment").value);
      }
```

```html
 </script>
</head>

<body>
   <form id="idForm" method="post" action="form_text.php">
      <p><input id="idFamilyName" name="familyName"
            required="required"> Family name (*)</p>

      <p><input id="idPassword" name="password"
            type="password" required="required"> Password (*)</p>

      <p><textarea id="idComment" rows="3" cols="25"
            name="comment">(Contents)</textarea> Comment</p>

      <p><input type="submit"> <input type="reset"></p>

      <p>(*) = required field</p>
   </form>

   <script>
```

```javascript
 document.getElementById("idForm").addEventListener
         ("submit", function(e) { return submit(e);});
```

```html
 </script>
</body></html>
```

**清单 4.4**　`form_text.htm` 文件

表单的结构如下：

- `input` 元素的 `type` 属性的 `password` 值将该元素转换为密码输入字段。只能识别输入的字符数——字符本身无法读取。
- 使用 `textarea` 容器显示多行输入字段。字段的大小最初取决于 `rows` 和 `cols` 属性的值，但通常可以在浏览器中更改。与单行输入字段一样，可以通过 `value` 属性在 JavaScript 中访问该条目。
- 姓氏和密码的两个输入字段具有 `required` 属性，其值为 `required`，因此这些字段不能留空。如果两个输入字段都不为空，则会触发 `submit` 事件。

事件处理程序中的过程如下：

1. `addEventListener()` 方法直接针对表单的引用调用，在后续的大多数示例中也使用这种简写表示法。
2. 将事件链接到函数时传递参数只能通过匿名函数实现。在此示例中，参数是对 `event` 对象的引用，当事件发生时，该对象会自动提供更多信息。按照惯例，该引用被命名为 `e`。
3. 在匿名函数中，调用名为 `submit()` 的函数。匿名函数的参数被依次传递，`submit()` 函数向匿名函数返回一个真值。如果该值为 `false`，则表单不会提交。

`submit()` 函数中的过程如下：

1. 在 `submit()` 函数中，通过直接针对输入字段的引用调用 `value` 属性来确定输入的密码。这也是一种简写表示法，在后续示例中也会使用。
2. 字符串的 `length` 属性包含字符串中的字符数。有关字符串的更多信息，请参见第 6 章的第 6.2 节。如果密码太短或太长，`submit()` 函数返回值 `false` 并显示错误消息。
3. 此外，还会调用 `event` 对象的 `preventDefault()` 方法，以便不执行该元素的默认操作（在本例中为提交表单）。
4. 如果密码长度正确，则会显示三个条目，`submit()` 函数返回值 `true`，并且表单被提交。

## 4.4　单选按钮和复选框

一组单选按钮允许用户选择不同的选项，而复选框允许用户进行额外选择。你可以使用 JavaScript 确定已做出哪个选择。

在以下示例中，可以选择三个不同国家之一，还可以选择另外两个国家（参见图 4.13）。

![单选按钮和复选框](img/img-f4.13.html)

**图 4.13**　单选按钮和复选框

提交表单时，会显示各个选择元素的值（参见图 4.14）。这些值不必与显示的文本匹配。

![选择元素的值](img/img-f4.14.html)

**图 4.14**　选择元素的值

以下是包含表单的文件代码：

```html
... <head> ...

   <script>
```

```javascript
 function submit()
      {
         let tx;

         if(r1.checked) tx = r1.value;
         else if(r2.checked) tx = r2.value;
         else if(r3.checked) tx = r3.value;

         if(c1.checked) tx += "\n" + c1.value;
         if(c2.checked) tx += "\n" + c2.value;

         alert(tx);
      }
```

```html
 </script>
</head>

<body>
   <form id="idForm" method="post" action="form_check.php">
      <p><input id="idEstonia" name="balticCountries" type="radio"
            value="Estonia" checked="checked">Estonia

         <input id="idLatvia" name="balticCountries" type="radio"
            value="Latvia">Latvia

         <input id="idLithuania" name="balticCountries" type="radio"
            value="Lithuania">Lithuania</p>

      <p><input id="idSweden" name="sweden" type="checkbox"
            value="Sweden">Sweden</p>

      <p><input id="idFinland" name="finland" type="checkbox"
            value="Finland" checked="checked">Finland</p>

      <p><input type="submit"> <input type="reset"></p>
   </form>

   <script>
```

```javascript
 const r1 = document.getElementById("idEstonia");
 const r2 = document.getElementById("idLatvia");
 const r3 = document.getElementById("idLithuania");
 const c1 = document.getElementById("idSweden");
 const c2 = document.getElementById("idFinland");

 document.getElementById("idForm")
    .addEventListener("submit", submit);
```

```html
 </script>
</body></html>
```

**清单 4.5**　`form_check.htm` 文件

表单的结构如下：

- `radio` 和 `checkbox` 属性分别将 `input` 元素标识为单选按钮和复选框。`value` 属性包含为该元素传输的值。
- 所有具有相同 `name` 属性值的单选按钮属于同一组。如果在组内进行选择，则之前的选择将被取消。
- 组内的一个单选按钮应已使用 `checked` 属性和 `checked` 值进行标记，以便该组始终有一个值。

对各个元素的引用被保存。

`submit()` 函数中的处理过程如下：使用多个分支检查单选按钮组，并使用单个分支检查每个复选框。如果 `checked` 属性的值为 `true`，则相应的元素被选中。`value` 属性在此处也包含元素的值。

### 注意

你可以在本书的可下载材料中找到 `u_radio` 练习，位于附加章节 1 的第 1.12 节，下载地址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

## 4.5　选择菜单

你可以使用单选菜单在不同选项中进行选择，也可以使用 (ª) 和 (Ctrl) 键在多选菜单中同时选择多个选项。你还可以使用 JavaScript 确定选择了哪个选项。

以下示例展示了一个单选菜单和一个多选菜单。每个菜单包含三个国家（参见图 4.15）。

![单选和多选菜单](img/img-f4.15.html)

**图 4.15**　单选和多选菜单

当表单提交时，会显示各个选择元素的值（参见图 4.16）。这些值不必与显示的文本匹配。

![选择元素的值](img/img-f4.16.html)

**图 4.16**　选择元素的值

以下是包含表单的文件的代码：

```html
... <head> ...

   <script>
```

```javascript
 function submit()
      {
         let tx = document.getElementById("idSingle").value;
         const opt = document.getElementById("idMultiple").options;

         for(let i=0; i<opt.length; i++)
            if(opt[i].selected)
               tx += "\n" + opt[i].value;

         alert(tx);
      }
```

```html
 </script>
</head>

<body>
   <form id="idForm" method="post" action="form_select.php">
      <p>国家 1: <select id="idSingle" name="single">
            <option value="Italy" selected="selected">意大利</option>
            <option value="Spain">西班牙</option>
            <option value="Romania">罗马尼亚</option>
         </select></p>

      <p>国家 2 到 4:
         <select id="idMultiple" name="multiple[]" multiple="multiple">
            <option value="Belgium" selected="selected">比利时</option>
            <option value="Netherlands">荷兰</option>
            <option value="Luxembourg" selected="selected">卢森堡</option>
         </select>
      </p>

      <p><input type="submit"> <input type="reset"></p>
   </form>

   <script>
```

```javascript
 document.getElementById("idForm").addEventListener("submit", submit);
```

```html
 </script>
</body></html>
```



## 清单 4.6　`form_select.htm` 文件

表单的结构如下：

- 选择菜单位于`select`容器中，`multiple`属性和`multiple`值将其变为多选菜单。各个选项位于`option`容器中，各个选项的值通过`value`属性定义。
- 与单选按钮类似，在简单选择菜单中，应使用`selected`属性和`selected`值选中一个选项，以便菜单始终有一个值。

对于多选菜单，建议在`name`属性的值中添加方括号。这意味着在 PHP 程序中解析时，各个元素可以像字段元素一样被处理。

`submit()`函数中的处理过程如下：

1. 简单选择菜单的值很容易确定，因为只能选择一个选项。菜单的`value`属性包含所需的值。
2. 对于多选菜单，确定过程更复杂，因为可以选择多个值。菜单的`options`属性是一个包含各个选项引用的字段。`length`属性对应字段的大小（即选项的数量），可以使用方括号访问单个选项。每个选项都有`selected`属性。如果选项被选中，该属性的值为`true`；否则为`false`。选项的`value`属性包含其值。

### 注意

你可以在本书的可下载材料中找到`u_select`练习，位于附加章节 1 的第 1.13 节，下载地址为[www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

## 4.6　其他表单事件

你已经熟悉了`click`（在按钮上）、`submit`和`reset`（在表单上）事件。以下程序添加了可以在表单内发生的以下事件：

- `click`：单击单选按钮或复选框
- `change`：更改输入字段的内容或选择菜单中的选择
- `keyup`：在输入字段中释放按键
- `focus`：访问元素（即元素获得输入焦点，输入光标定位在该元素中）
- `blur`：离开元素（即元素失去输入焦点，输入光标不再定位在该元素中）

对各种事件的响应显示在一个只读输入字段中。例如，在图 4.17 中，你可以看到单击复选框以选中它后的输出。

![标记复选框的响应](img/img-f4.17.html)

**图 4.17**　标记复选框的响应

以下是包含表单的文件的代码：

```html
... <head> ...

   <script> 

      function value(e)
      {
         const re = document.getElementById("idResponse");
         re.value = e.type + ", ";

         const id = e.target.id;

         if(id == "idTrip")
            if(document.getElementById(id).checked)
               re.value += "Marker set";
            else
               re.value += "Marker deleted";
         else
            re.value += document.getElementById(id).value;
      } 

   </script>
</head>

<body id="idBody">

   <form method="post" action="form_event.php">

      <p><input id="idMr" name="address" type="radio"
            value="Mr" checked="checked"> Mr

         <input id="idMs" name="address" type="radio"
            value="Ms"> Ms</p>

      <p><input id="idFamilyName" name="familyName"> Family name</p>

      <p><input id="idFirstName" name="firstName"> First name</p>

      <p><input id="idCity" name="city"> City</p>

      <p><select id="idCountry" name="country">

            <option value="Italy" selected="selected">Italy</option>

            <option value="Spain">Spain</option>

            <option value="Portugal">Portugal</option>

         </select> Country</p>

      <p><input id="idTrip" name="trip" type="checkbox"

         value="OneWayOnly"> one-way only</p>

      <p><input type="submit"> <input type="reset"></p>

      <p><input id="idResponse"

         readonly="readonly"> Response</p></p>

   </form>

   <script> 

      document.getElementById("idMr").addEventListener
         ("click", function(e) { value(e); });

      document.getElementById("idMs").addEventListener
         ("click", function(e) { value(e); });

      document.getElementById("idFamilyName").addEventListener
         ("change", function(e) { value(e); });

      document.getElementById("idFirstName").addEventListener
         ("keyup", function(e) { value(e); });

      document.getElementById("idCity").addEventListener
         ("focus", function(e) { value(e); });

      document.getElementById("idCity").addEventListener
         ("blur", function(e) { value(e); });

      document.getElementById("idCountry").addEventListener
         ("change", function(e) { value(e); });

      document.getElementById("idTrip").addEventListener
         ("click", function(e) { value(e); }); 

   </script>

</body></html>
```

**清单 4.7**　`form_event.htm` 文件

表单和事件处理程序的结构如下：

- `readonly`属性与`readonly`值确保输入字段中无法输入。它仅用于输出信息。
- 当两个单选按钮之一被选中时，会触发`click`事件。该事件与一个匿名函数关联，该函数调用命名函数`value()`，并传递参数`e`，该参数引用一个事件对象。其他事件以相同方式与`value()`函数关联。
- 在输入字段中，`change`事件发生在输入字段内容改变之后，并且一旦选择了另一个元素或在输入字段外部点击时触发。
- 输入字段中的`keyup`事件在按键释放后立即触发。该事件发生在输入或删除字符之后。
- 在选择菜单中，`change`事件在选择发生变化时立即触发。如果复选框被选中或取消选中，则会触发`click`事件。
- `focus`和`blur`事件在输入字段被访问或随后离开时立即触发。

`value()`函数中的过程如下：

1. 事件对象的`target`属性引用触发事件的元素。`type`属性包含事件名称，`target`属性的`id`子属性对应元素的唯一 ID。这样，你可以为多个元素或事件使用同一个函数。
2. 检查复选框的`checked`属性，以确定在`click`事件中是否设置或取消了勾选标记。对于所有其他元素，显示触发事件的元素的当前值。

你应该测试可能的事件一次，并注意信息出现的时间以及响应的内容。

## 4.7　鼠标事件

除了表单之外，还有一些可以使用鼠标触发的事件。以下程序处理以下事件：

- `click`：点击元素
- `mousemove`：在元素上移动鼠标
- `mousedown`：在元素上按下鼠标按钮
- `mouseup`：在元素上释放鼠标按钮
- `mouseover`：进入元素
- `mouseout`：离开元素

为了说明这一点，这些事件发生在图像上。事件信息显示在一个只读输入字段中（参见图 4.18）。

![鼠标事件](img/img-f4.18.html)

**图 4.18**　鼠标事件

以下是该文件的代码：

```html
... <head> ...

   <script> 

      function mouse(e)
      {
         document.getElementById("idResponse").value = e.type + " " + e.offsetX
            + "/" + e.offsetY + " " + document.getElementById(e.target.id).src;
      } 

   </script>
</head>

<body>

   <form>

      <p><input size="70" id="idResponse" readonly="readonly"></p>

   </form>

   <p><img src="im_paradise.jpg"      id="idParadise"     alt="Paradise">

      <img src="im_solar_eclipse.jpg" id="idSolarEclipse" alt="Solar eclipse">

      <img src="im_wave.jpg"          id="idWave"         alt="Wave"></p>

   <p><img src="im_winter.jpg"        id="idWinter"       alt="Winter">

      <img src="im_tree.jpg"          id="idTree"         alt="Tree"></p>

   <script>

      document.getElementById("idParadise").addEventListener
         ("click", function(e) { mouse(e); });

      document.getElementById("idSolarEclipse").addEventListener
         ("mousemove", function(e) { mouse(e); });

      document.getElementById("idWave").addEventListener
         ("mousedown", function(e) { mouse(e); });

      document.getElementById("idWave").addEventListener
         ("mouseup", function(e) { mouse(e); });

      document.getElementById("idWinter").addEventListener
         ("mouseover", function(e) { mouse(e); });

      document.getElementById("idWinter").addEventListener
         ("mouseout", function(e) { mouse(e); });

      const tree = document.getElementById("idTree");

      tree.addEventListener("mouseover",
         function() { tree.src = "im_paradise.jpg"; });

      tree.addEventListener("mouseout",
         function() { tree.src = "im_tree.jpg"; }); 

   </script>

</body></html>
```

**清单 4.8**　`mouse_event.htm` 文件

事件处理程序的结构如下：

- 点击第一张图片会触发`click`事件，该事件连接到一个匿名函数，该函数调用命名函数`mouse()`。指向事件对象的`e`参数被传递，其他事件也相同方式链接到`mouse()`函数。
- `img`元素具有`src`属性，该属性包含图像文件的名称，包括路径（如果适用）。在最后一张图片中，通过为`mouseover`或`mouseout`事件调用匿名函数来执行图像更改。在函数内部为`src`属性赋予新值。

在`mouse()`函数中输出三条信息：

- 鼠标事件的名称
- 鼠标事件发生位置在元素内的相对坐标（`offsetX`和`offsetY`）
- 相关`img`元素中显示的图像文件的名称

你应该测试所有可能的事件，并记录事件的位置、相关信息以及信息出现的时间。

### 注意

你可以在本书的可下载材料中的附加章节 1 第 1.14 节找到`u_mouse`练习，下载地址为[www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

## 4.8　更改文档

默认情况下，超链接用于在浏览器中切换到另一个文档。使用预定义的`location`对象和适当的事件，也可以以不同的方式实现。

在下面的程序中（参见图 4.19），通过三种方式实现：

- 点击按钮后
- 点击图片后
- 通过更改选择菜单中的选项

预定义的`location`对象包含当前 URL 的信息，例如 HTML 文档。

![更改文档](img/img-f4.19.html)

**图 4.19**　更改文档

以下是文件的代码：

```html
...

<body>

   <form>

      <p><input id="idButton" type="button" value="First document"></p>

      <p><img src="im_tree.jpg" id="idTree" alt="Tree"></p>

      <p><select id="idSelection">

            <option value="(Selection)" selected="selected">(Selection)</option>

            <option value="strings.htm">Strings</option>

            <option value="numbers.htm">Numbers</option>

            <option value="bool.htm">Truth values</option>

         </select> </p>

   </form>

   <script>

      document.getElementById("idButton").addEventListener
         ("click", function() { location.href = "first.htm"; } );

      document.getElementById("idTree").addEventListener("click",
         function() { location.href = "special_characters.htm"; } );

      const selection = document.getElementById("idSelection");

      selection.addEventListener("change", function() {

         if(selection.value != "(Selection)")
            location.href = selection.value; } );

   </script>

</body></html>
```



**清单 4.9**　`form_location.htm` 文件

按钮上的`click`事件连接到一个匿名函数，该函数将一个文件名作为新值赋给`location`对象的`href`属性。这会导致切换到所需的文档，点击图片时也会发生同样的情况。

当你在选择菜单中更改选项时，`change`事件也连接到一个匿名函数。该函数检查当前选中选项的值（即整个选择菜单的值）是否与第一个选项的值一致。第一个选项作为选择菜单的标题，不应导致文档更改。如果选中的选项不是第一个选项，系统将切换到所需的文档。

## 4.9　其他类型和属性

自 HTML 5 版本以来，输入字段提供了其他类型和属性。它们提供了广泛且易于使用的选项。

各种类型可以包含验证（即在提交表单时对元素进行检查）。这有助于避免传输错误数据，并且此功能可以补充甚至替代使用 JavaScript 进行的表单检查。在创建 JavaScript 程序之前，你应该检查是否已经可以在现代浏览器中使用 HTML 进行所需的验证。

如果某个浏览器没有实现某种输入字段类型，则会显示一个标准输入字段。这样在任何情况下都可以进行输入。特别是移动浏览器，它们利用了许多功能，并通过显示带有合适元素的键盘来提供支持。

### 4.9.1　文本输入、搜索字段和颜色

以下程序展示了各种文本类型的输入字段、带有列表的搜索字段以及用于选择颜色的元素。还解释了特殊属性的使用。

你可以在图 4.20 中看到整个文档。

![其他类型和属性](img/img-f4.20.html)

**图 4.20**　其他类型和属性

以下是文件的代码：

```html
... <head> ...

   <script>
```

```javascript
 function submit()

      {

         alert(document.getElementById("idFirstName").value

            + "\n" + document.getElementById("idFamilyName").value

            + "\n" + document.getElementById("idZip").value

            + " " + document.getElementById("idCity").value

            + "\n" + document.getElementById("idCountry").value

            + "\n" + document.getElementById("idColor").value

            + "\n" + document.getElementById("idAddresses").value

            + "\n" + document.getElementById("idWeb").value

            + "\n" + document.getElementById("idPhone").value

            + "\n" + document.getElementById("idLicensePlate").value);

      }
```

```html
   </script>

</head>

<body>

   <p>A form with <mark>additional</mark> elements follows.</p>

   <form id="idForm" method="post" action="form_input.php">

      <p><input id="idFirstName" name="firstName"

         placeholder="Your first name"> placeholder (first name)</p>

      <p><input id="idFamilyName" name="familyName" autofocus>

         autofocus (family name)</p>

      <input id="idZip" name="zip" type="hidden" value="02171">

      <p><input id="idCity" name="city" type="search"> search (city)</p>

      <p><input id="idCountry" name="country" type="search"

         list="idList"> search, datalist (country)</p>

      <datalist id="idList">

         <option value="Germany">

         <option value="France">

         <option value="Italy">

      </datalist>

      <p><input id="idColor" name="color" type="color" value="#ff0000"> color</p>

      <p><input id="idAddresses" name="addresses" type="email"

         multiple="multiple" value="a1@b.com, a2@b.com"> email</p>

      <p><input id="idWeb" name="web" type="url" value="https://www.c.com"> url</p>

      <p><input id="idPhone" name="phone" type="tel"

         value="+1.781.228.5070"> phone</p>

      <p><input id="idLicensePlate" name="licensePlate" value="68G D72"

         pattern="^[1-9][0-9][A-Z] [A-Z][0-9]{1,2}$">

         pattern (license plate)</p>

      <p><input type="submit"> <input type="reset"></p>

   </form>

   <script>
```

```javascript
 document.getElementById("idForm").addEventListener("submit", submit);
```

```html
   </script>

</body></html>
```

**清单 4.10**　`form_input.htm` 文件

`mark` 容器用于视觉上突出显示文本（例如，使用黄色高亮）。它可以用来标记表单中的重要元素。

在名字（first name）的输入元素中，使用`placeholder`属性以浅灰色显示占位符。占位符用于解释输入字段，如果在输入字段中开始输入内容，占位符就会消失。

调用程序后，由于`autofocus`属性，输入光标会自动出现在姓氏（family name）的输入元素中。你可以立即在那里开始输入数据，如果该元素中已有文本，则会被完全选中。

长期以来，可以通过将`type`属性设置为`hidden`来隐藏输入字段。这样，可以将使用过程中不应可见的附加数据传输到 Web 服务器。

`type`属性的`search`值标识一个输入字段，该字段可被识别为典型的搜索字段。它还可以包含一个用于删除搜索词条的图标。

搜索字段可以具有额外的`list`属性，其值对应于一个包含预定义条目的列表的 ID，这些条目可以在操作搜索字段时选择（另请参见图 4.21）。一旦在搜索字段中输入字符，列表中只会显示包含这些字符的条目。也可以输入其他搜索词。该列表使用`datalist`容器创建，每个条目代表一个`option`标签的`value`属性的值。

![带有列表的搜索字段](img/img-f4.21.html)

**图 4.21**　带有列表的搜索字段

`type`属性的`color`值表示用于设置颜色的输入字段。选择输入字段后，会打开一个带有设置选项的对话框（另请参见图 4.22）。

![设置颜色](img/img-f4.22.html)

**图 4.22**　设置颜色

在`type`属性值为`email`的输入字段中可以输入电子邮件地址。该字段可以为空，如果不为空，则必须包含电子邮件地址的最基本组成部分，否则表单将无法提交。如果添加了值为`multiple`的`multiple`属性，则可以输入多个地址，用逗号分隔。

对于`type`属性值为`url`的输入字段，情况类似。该字段可以为空，如果不为空，则必须包含 URL 的最基本组成部分，否则表单将无法提交。但是，不能输入多个 URL。

用于输入电话号码的元素具有`type`属性的`tel`值。它可以提供访问现有电话列表的选项。

`pattern`属性用于使用正则表达式验证输入。如果输入的内容与模式不匹配，则无法提交表单。

这里我们有一个车牌号的示例。我们假设它由两位数字开头，第一位不能是 0。后面跟着一个大写字母、一个空格和另一个大写字母。最后是 1 或 2 位数字。有关正则表达式的更多信息，请参阅本书可下载材料中的附加章节 2，网址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

提交后，会调用`submit()`函数。所有值都通过`value`属性显示。

### 4.9.2　数字输入元素

本节介绍一些可用于安全输入和清晰表示数值的元素（参见图 4.23）。

![数字输入元素](img/img-f4.23.html)

**图 4.23**　数字输入元素

以下是文件中间部分的表单内容：

```html
...

<body>

   <form id="idForm" method="post" action="form_number.php">
```

```html
 <p><input id="idNumber" name="number" type="number"

            min="32" max="58" step="2" value="42">

         <input id="idPlus1" type="button" value="+1 增量">

         <input id="idMinus1" type="button" value="-1 增量">

         <input id="idPlus3" type="button" value="+3 增量">

         <input id="idMinus3" type="button" value="-3 增量"></p>

      <p>数字（32 到 58，步长 2）</p>

      <p><input id="idRequired" type="checkbox"> 需要输入</p><br>

      <p><input id="idRange" name="range" type="range" min="3.2"

            max="5.8" step="0.2" value="4.2"> 范围 <input id="idRValue"

            readonly="readonly" size="5" value="4.2"></p>

      <p><input type="submit"> <input type="reset"></p><br>

      <p><progress id="idProgress" max="100" value="10"></progress>

         <input id="idStart" type="button" value="开始">

         <input id="idStop" type="button" value="停止"> 进度 <input

            id="idPValue" readonly="readonly" size="5" value="10%"></p>

   </form>

...
```

**清单 4.11**　`form_number.htm` 文件，中间部分

用于输入数值的元素具有`type`属性的`number`值。如果将光标放在输入字段中，会显示一个向上/向下按钮，点击它可以更改数字。为了设置该元素，可以为`min`、`max`、`step`和`value`属性输入值。这些值表示下限 32、上限 58、步长 2 和显示值 42。不在范围内或不匹配步长的值将无法提交，并且会显示错误消息（参见图 4.24）。

![不允许的数字](img/img-f4.24.html)

**图 4.24**　不允许的数字

你也可以通过代码设置该值。+1 增量、–1 增量、+3 增量和 –3 增量按钮会按步长 2 的相应倍数更改值（例如，+3 增量按钮将值从 42 更改为 42 + 3 × 2 = 48）。`required`属性也可以通过代码更改。如果选中复选框，则数字字段不能再留空。

滑块用于安全地传输来自某个范围的数值。该元素具有`type`属性的`range`值。值本身不显示，因此这里在只读输入字段中添加了一个单独的显示。`min`、`max`、`step`和`value`属性也可用于设置，并且可以使用滑块设置带小数位的数字。

`progress`容器通常用于显示百分比进度。`min`和`max`属性的默认值分别为 0 和 1。此处，当前值取 10，最大值取 100。开始和停止按钮用于启动一个 JavaScript 函数来动画显示进度条，当前值显示在一个只读输入字段中。

让我们看看文档的下半部分：

```html
...

   <table>

      <tr><td>Revenue 2017:</td><td><meter min="0" max="10000"

              value="4500"></meter> $4,500</td></tr>

      <tr><td>Revenue 2018:</td><td><meter min="0" max="10000"

              value="7500"></meter> $7,500</td></tr>

      <tr><td>Revenue 2019:</td><td><meter min="0" max="10000"

              value="6000"></meter> $6,000</td></tr>

   </table>

   <script>
```

```javascript
 document.getElementById("idForm").addEventListener("submit", submit);

      const number = document.getElementById("idNumber");

      document.getElementById("idRequired").addEventListener

         ("click", function() { number.required = !number.required; } );

      document.getElementById("idPlus1").addEventListener

         ("click", function() { number.stepUp(); } );

      document.getElementById("idMinus1").addEventListener

         ("click", function() { number.stepDown(); } );

      document.getElementById("idPlus3").addEventListener

         ("click", function() { number.stepUp(3); } );

      document.getElementById("idMinus3").addEventListener

         ("click", function() { number.stepDown(3); } );

      document.getElementById("idRange").addEventListener

         ("change", changeRange);

      document.getElementById("idStart").addEventListener

         ("click", startProgress);

      document.getElementById("idStop").addEventListener

         ("click", stopProgress);
```

```html
   </script>

</body></html>
```




**清单 4.12**　`form_number.htm` 文件，下半部分

`meter` 容器实际上用于显示填充水平。此处，三个 `meter` 容器用于显示收入，使用了 `min`、`max` 和 `value` 属性，类似于条形图。

`number` 变量用于引用数字输入字段。

激活复选框后，布尔属性 `required` 的值通过逻辑非（`!`）运算符取反。如果复选框被选中，数字输入字段变为必填字段，不能为空。

`stepUp()` 和 `stepDown()` 方法按增量的相应倍数改变元素的值。如果没有参数，则值将恰好改变一个增量。

移动滑块会触发 `change` 事件，从而调用 `changeRange()` 函数。这确保当前值显示在滑块旁边。

开始按钮启动 `startProgress()` 函数，该函数改变进度条。按下停止按钮调用 `stopProgress()` 函数，在该函数中结束改变。这确保当前值显示在进度条旁边。

现在，这是文档第一部分的 JavaScript 代码：

```html
... <head> ...

   <script>
```

```javascript
function submit()

{
   alert(number.value + "\n"
      + document.getElementById("idRange").value);
}

function changeRange()

{
   const range = parseFloat(
      document.getElementById("idRange").value);
   document.getElementById("idRValue").value
      = range.toFixed(1);
}

let pValue = 10;
let reference;

function startProgress()

{
   if(pValue<100)
   {
      pValue++;
      document.getElementById("idProgress").value = pValue;
      document.getElementById("idPValue").value = pValue + "%";
      reference = setTimeout(startProgress, 20);
   }
}

function stopProgress()

{
   clearTimeout(reference);
}
```

```html
</script>
</head>

...
```

**清单 4.13**　`form_number.htm` 文件，JavaScript 代码

数字输入字段的值在 `submit()` 函数中输出，`changeRange()` 函数用于输出滑块数值，保留一位小数。

`window` 对象的 `setTimeout()` 方法会产生一个超时。一个函数在延迟一段时间后启动，参数包括相关函数的引用（此处为 `startProgress()`）和所需的延迟时间（毫秒）。返回一个引用，并保存在 `reference` 变量中，该变量在整个程序中有效。由于 `startProgress()` 函数不断调用自身，进度条从起始值 10 逐步动画到结束值 100。

可以通过调用 `clearTimeout()` 函数来阻止已经计划好的下一次 `startProgress()` 函数调用。这需要将 `setTimeout()` 函数返回的引用作为参数，从而提前终止动画。你可以在第 6 章的 6.5 节中了解更多关于时间控制过程的内容。

`pValue` 变量在整个程序中有效，包含进度条的当前值。

### 4.9.3　时间信息元素

本节介绍一些可用于安全设置和传输时间数据的元素（参见图 4.25）。选择其中一个元素后，如图 4.26 所示，会出现控制元素，方便在定义的时间范围内输入或选择时间规范的各个部分，如图 4.27 所示。

让我们从表单的代码开始：

```html
...

<body>

   <form id="idForm" method="post" action="form_time.php">

      <p>1: <input id="idDate" name="date" type="date" value="2024-05-25"

         min="2024-04-15" max="2024-06-20"> date</p>

      <p>2: <input id="idTime" name="time" type="time"

         value="10:30" min="08:00" max="13:00"> time</p>

      <p>3: <input id="idLocale" name="locale" type="datetime-locale"

         value="2024-05-25T10:30"> datetime-locale</p>

      <p>4: <input id="idMonth" name="month" type="month" value="2024-05"

         min="2023-10" max="2025-03"> month</p>

      <p>5: <input id="idWeek" name="week" type="week" value="2024-W21"

         min="2024-W10" max="2024-W30"> week</p>

      <p><input type="submit"> <input type="reset"></p>

   </form>

   <script>

      document.getElementById("idForm").addEventListener("submit", submit);

   </script>

</body></html>
```

**清单 4.14**　`form_time.htm` 文件，包含元素的表单

![时间信息元素](img/img-f4.25.html)

**图 4.25**　时间信息元素

所有元素都具有 `input` 类型，其 `type` 属性取值不同：`date`、`time`、`datetime-locale`、`month` 和 `week`。`min` 和 `max` 属性用于限制时间范围，`value` 属性表示时间规范的默认设置。对于这五种不同的元素，默认设置会采用相应的输出格式。

第一个 `input` 元素类型为 `date`，用于设置日期，时钟时间为协调世界时（UTC）00:00。你可以选择时间输入的各个部分进行输入（参见图 4.26）。

![选择时间规范的一部分](img/img-f4.26.html)

**图 4.26**　选择时间规范的一部分

如果没有预设日期，则会显示当前月份——但此时提交表单时不会传输任何日期，因此建议进行预设。超出允许范围的数据会以浅灰色显示，且无法选择（参见图 4.27）。

![时间规范的限制](img/img-f4.27.html)

**图 4.27**　时间规范的限制

第二个 `input` 元素类型为 `time`，用于设置时钟时间，日期为 1970 年 1 月 1 日。

`datetime-locale` 类型的元素可用于同时设置日期和时钟时间。注意 `value` 属性的单独格式。

第四个元素选择 `month` 类型，只能设置整月。第五个元素为 `week` 类型，只能设置整周。

以下是 `submit()` 函数的结构：

```html
... <head> ...

   <script>
```

```javascript
function submit()

{
   const d = document.getElementById("idDate");
   const dValue = d.value;
   const dDate = d.valueAsDate;
   const dLocale = dDate.toLocaleDateString();

   const t = document.getElementById("idTime");
   const tValue = t.value;
   let tDate = t.valueAsDate;
   tDate.setHours(tDate.getHours() - 1);
   const tLocale = tDate.toLocaleTimeString();

   const cValue = document.getElementById("idLocale").value;
   const mValue = document.getElementById("idMonth").value;
   const wValue = document.getElementById("idWeek").value;

   alert(dValue + " # " + dLocale + "\n" + tValue + " # " + tLocale
      + "\n" + cValue + "\n" + mValue + "\n" + wValue);
}
```

```html
</script>
</head>

...
```

**代码清单 4.15**　`form_time.htm` 文件，JavaScript 代码

输入字段的值通过 `value` 属性获取。

对于前两个输入字段，还可以获取 `valueAsDate` 属性的值。该属性包含一个 `date` 对象的值，可以调用 `toLocaleDateString()` 和 `toLocaleTimeString()` 函数。这些函数会生成一个包含本地时间规范的字符串。

需要从时间中减去一小时，以使显示的结果与设置的值匹配。`getHours()` 方法返回 `Date` 对象的小时值，而 `setHours()` 方法则更改该值。

有关 `Date` 对象的更多信息，请参见第 6 章的第 6.4 节。

在图 4.28 中，你可以看到表单提交后的显示效果。

![时间数据的输出](img/img-f4.28.html)

**图 4.28**　时间数据的输出

### 4.9.4　验证表单

JavaScript 在表单内容验证方面提供了更多选项。你可以设置是否检查单个元素或整个表单。文档中有两个表单，每个表单都有一个提交按钮（参见图 4.29）。

![两个表单](img/img-f4.29.html)

**图 4.29**　两个表单

第一个表单包含一个文本输入字段，你可以使用复选框来决定是否要检查该表单（例如，根据输入的内容）。

在第二个表单中，你可以使用复选框来决定其中的数字输入字段是否可操作。如果不可操作，则不会检查输入。

此外，你可以使用“测试”按钮来确定输入是否应被检查以及是否能够通过测试。这在表单内容自动设置，并且你想知道当前内容是否能通过检查时非常有用。

以下是包含两个表单和事件处理程序的文档下半部分：

```html
...

<body>

   <form id="idForm1" novalidate method="post" action="form_validation1.php">

      <p><input id="idContents1" name="contents1" required>

      <input id="idCheck1" type="checkbox"> 表单正在被检查</p>

      <p><input type="submit"></p>

   </form>

   <p> </p>

   <form id="idForm2" method="post" action="form_validation2.php">

      <p><input id="idContents2" name="contents2" disabled type="number" min="32"

         max="58" step="2" value="42"> 从 32 到 58，步长为 2</p>

      <p><input id="idCheck2" type="checkbox"> 元素可操作</p>

      <p><input id="idTest2" type="button" value="测试"></p>

      <p><input type="submit"></p>

   </form>

   <script>

      document.getElementById("idForm1").addEventListener("submit", submit1);
      document.getElementById("idCheck1").addEventListener("click", check1);
      document.getElementById("idTest2").addEventListener("click", test2);

      document.getElementById("idForm2").addEventListener
         ("submit", function(e) { return submit2(e);});

      document.getElementById("idCheck2").addEventListener("click", check2);

   </script>

</body></html>
```

**代码清单 4.16**　`form_validation.htm` 文件，下半部分

`novalidate` 属性用于指定第一个表单不应被检查。在这种情况下，即使输入字段（实际上是必填字段）留空，也不会出现错误消息。你可以使用复选框来决定是否检查该表单。

第二个表单的数字输入字段由于 `disabled` 属性最初不可操作。输入值为 42 时可以通过测试，但只有 32 到 58 之间的偶数才是有效值。

现在，以下是文档的上半部分：

```html
... <head> ...

   <script>
```

```javascript
function submit1()

{
   alert(document.getElementById("idContents1").value);
}

function check1()

{
   const f = document.getElementById("idForm1");
   f.noValidate = !f.noValidate;
}

function test2()

{
   const number = document.getElementById("idContents2");

   alert("Would be tested: " + number.willValidate + "\n"
      + "Too large: " + number.validity.rangeOverflow + "\n"
      + "Too small: " + number.validity.rangeUnderflow + "\n"
      + "Would be valid: " + number.validity.valid);
}

function submit2(e)

{
   const contents2 = document.getElementById("idContents2");
   const number = contents2.valueAsNumber;

   if(contents2.disabled)
   {
      alert("Entry is disabled");
      e.preventDefault();
      return false;
   }
   else
      alert(number);
}

function check2()

{
   document.getElementById("idContents2").disabled =
      !document.getElementById("idContents2").disabled;
}
```

```html
</script>
</head>

...
```




### 清单 4.17　`form_validation.htm` 文件，JavaScript 代码

每次点击第一个表单的复选框时，都会执行`check1()`函数。这会将表单的`noValidate`属性值设置为`true`或`false`。当您提交表单时，只有当`noValidate`的值为`false`且输入字段为空时，才会出现错误消息，如图 4.30 所示。因此，您可以在程序中指定是否应检查表单。

![切换到 noValidate = false 后](img/img-f4.30.html)

**图 4.30**　切换到 noValidate = false 后

在`test2()`函数中，确定了元素的一些布尔属性或`validity`属性的值：

- `willValidate`：该元素将被测试。
- `validity.rangeOverflow`和`validity.rangeUnderflow`：该值超出或低于有效范围。
- `validity.valid`：该值将作为有效值发送。

第二个表单中的值 82 导致结果如图 4.31 所示。在这种情况下，`validity`对象的`rangeOverflow`属性返回`true`。

![值 82 的测试结果](img/img-f4.31.html)

**图 4.31**　值 82 的测试结果

对于值 51，结果如图 4.32 所示。虽然该值在允许范围内，但它是奇数，因此无效。

![值 51 的测试结果](img/img-f4.32.html)

**图 4.32**　值 51 的测试结果

每次点击第二个表单的复选框时，都会执行`check2()`函数。这会将表单的`disabled`属性值设置为`true`或`false`，并且只有当`disabled`的值为`false`时，表单才能操作。

## 4.10　动态创建的表单

在本节中，使用 JavaScript 动态创建了一个表单。通过双重`for`循环，表单在表格中包含大量输入字段（参见图 4.33）。`id`（用于 JavaScript）和`name`（用于 PHP）属性的值以及事件处理程序都是使用变量创建的。

您可以在文档开头的程序代码中设置行数和列数。在此示例中，表格有五行三列（即十五个输入字段）。

![带有输入字段的表格](img/img-f4.33.html)

**图 4.33**　带有输入字段的表格

文档代码如下：

```html
... <head> ...

   <script> 
```

```javascript
const rows = 5, columns = 3;

      function change(e)

      {

         const id = e.target.id;

         document.getElementById("idResponse").value

            = id + ": " +  document.getElementById(id).value;

      }

      function submit()

      {

         let output = "";

         for(let r=0; r<rows; r++)

         {

            for(let c=0; c<columns; c++)

               output += document.getElementById("idInput"

                  + r + c).value + " ";

            output += "\n";

         }

         alert(output);

      }
```

```html
   </script>

</head>

<body>

   <form id="idForm" method="post" action="form_dynamic.php">

   <table>

   <script> 
```

```javascript
for(let r=0; r<rows; r++)

      {

         document.write("<tr>");

         for(let c=0; c<columns; c++)

         {

            document.write("<td><input id='idInput" + r + c + "' name='input"

               + r + c + "' value='" + r + "/" + c + "' size='10'></td>");

            document.getElementById("idInput" + r + c)

               .addEventListener("change", function(e) { change(e); });

         }

         document.write("</tr>");

      }

      document.getElementById("idForm").addEventListener("submit", submit);

      document.write("<input type='hidden' name='rows'"

         + " value='" + rows + "'>");

      document.write("<input type='hidden' name='columns'"

         + "value='" + columns + "'>");
```

```html
   </script>

   </table>

   <p><input type="submit"> <input type="reset"></p>

   <p><input id="idResponse" readonly="readonly"></p>

   </form>

</body></html>
```

### 清单 4.18　`form_dynamic.htm` 文件

行数和列数在文档开头的`rows`和`columns`变量中定义。

循环变量`r`和`c`用作`id`和`name`属性值的组成部分。注意，在`document.write()`的字符串中，属性值使用了单引号，而该字符串本身位于双引号内。

如果确定输入字段的内容已更改，则会调用一个匿名函数，该函数再调用命名函数`change()`。该函数确定已更改输入字段的 ID，并将其与输入字段的新内容一起输出。

在`submit()`函数中，再次使用双重`for`循环确定并输出所有输入字段的内容。

您可以使用隐藏的表单元素将行数和列数发送到 PHP 文件；这样，您可以动态确定发送的值。但是，输入字段不应超过一千个，否则 PHP 在默认设置下会报错。

# 5　文档对象模型

DOM 提供对 HTML 文档所有元素的读写访问。

文档对象模型（DOM）是一种用于访问特定类型文档（如 HTML、XML（参见第 7 章、第 7.3 节）和 SVG（参见第 9 章））元素的模型。

该模型的结构类似于树，就像目录树一样，由各个节点组成。有一个根节点，它拥有子节点，子节点又可以拥有自己的子节点，以此类推。每个节点还可以拥有属性节点。

在 JavaScript 中，每个节点由一个`node`对象表示，它可以是 HTML 元素节点、HTML 属性节点或文本节点。节点对象可以被读取、修改、添加和删除。

在 JavaScript 中，你可以通过`document`对象访问文档的内容，该对象提供了创建新文档对象并访问它们的方法。你已经频繁使用过`getElementById()`方法。

本章将介绍如何访问和修改 HTML 文档的元素，这是后续章节中许多技术的前提条件。

## 5.1　树与节点

在本节中，我们将查看一个简单 HTML 文档的 DOM 树。首先，这是 HTML 代码：

```html
<!DOCTYPE html><html lang="en-us">

<head>

   <meta charset="utf-8">

   <title>DOM, first example</title>

   <link rel="stylesheet" href="js5.css">

</head>

<body>

   <p>First paragraph</p>

   <p>Second paragraph with <span style="font-weight:bold;">

      bold font</span></p>

   <p>Third paragraph with <a href="embed.htm">a link</a></p>

</body>

</html>
```

**清单 5.1**　`dom_example.htm` 文件

该文档包含三个`p`容器，其中一些容器还包含其他容器。在浏览器中，它看起来如图 Figure 5.1 所示。

![DOM 树的简单示例](img/img-f5.1.html)

**图 5.1**　DOM 树的简单示例

现代浏览器提供了根据 DOM 可视化文档结构的功能。在 Google Chrome 浏览器中，你可以通过开发者工具实现这一点，你已经在第 2 章的第 2.5.5 节中了解过它。

假设浏览器已打开并运行上述程序。点击右上角的三个点打开浏览器菜单，选择“更多工具”•“开发者工具”菜单项。随后会显示开发者工具，它为你提供了许多不同的选项。

选择屏幕上方区域的“Elements”选项卡。与目录树类似，你现在可以显示或隐藏各个层级（见图 Figure 5.2）。如果代码显示选项卡太小，你可以将整个开发者工具区域向左拖动，从而为各个选项卡提供更多空间。

### 注意

在接下来的示例中，我们将查看或修改不同层级的各个节点。为了清晰起见，你应该始终牢记根据 DOM 的文档结构。

![开发者工具，Elements 选项卡](img/img-f5.2.html)

**图 5.2**　开发者工具，Elements 选项卡

## 5.2　检索节点

除了`getElementById()`方法，你还可以使用`getElementsByTagName()`方法。该方法的参数是一个字符串，包含不带尖括号的标签名称，该方法返回一个字段，其中包含所有具有所需标签的 HTML 元素的引用。

字段的元素从 0 开始编号。你可以通过方括号中的索引访问单个字段元素，字段的`length`属性提供元素的数量。关于字段的更多信息，请参见第 6 章的第 6.1 节。

你可以通过相关`node`对象的`getAttribute()`方法获取 HTML 元素的属性节点。该函数的参数是一个字符串，包含要搜索的属性名称。

以下是一个示例程序：

```html
... <head> ...

   <script>
```

```javascript
function retrieve()

      {

         let output = "";

         const parArray = document.getElementsByTagName("p");

         for (let i=0; i<parArray.length; i++)

            output += "Content: " + parArray[i].firstChild.nodeValue + "\n"

              + "Attribute Style: " + parArray[i].getAttribute("style") + "\n";

         alert(output);

      }
```

```html
   </script>

</head>

<body>

   <p style="font-family:Tahoma;">First paragraph</p>

   <p>Second paragraph</p>

   <p style="font-weight:bold;">Third paragraph</p>

   <form>

      <input type="button" id="idRetrieve" value="Retrieve">

   </form>

   <script>
```

```javascript
document.getElementById("idRetrieve").addEventListener("click", retrieve);
```

```html
   </script>

</body></html>
```

**清单 5.2**　`dom_retrieve.htm` 文件

该文档的 HTML 部分包含三个`p`容器，因此`parArray`字段有三个元素。

你可以通过`node`对象的`firstChild`属性访问节点的第一个子节点。这三个段落各自只有一个文本节点作为子节点。

`node`对象的`nodeValue`属性提供关联的文本作为值。调用`getAttribute("style")`方法返回 HTML 元素节点的`style`属性的值。由于第二个段落没有这个属性，该方法返回一个空引用（即值`null`）。

程序的输出如图 Figure 5.3 所示。点击按钮后，会弹出一个对话框，其输出类似于图 Figure 5.4 所示。

![包含三个段落的文档结构](img/img-f5.3.html)

**图 5.3**　包含三个段落的文档结构

![检索节点和节点值](img/img-f5.4.html)

**图 5.4**　检索节点和节点值

## 5.3　子节点

节点及其子节点都使用`node`对象表示。`hasChildNodes()`方法返回节点是否拥有子节点的信息，节点的`childNodes`属性包含一个字段，其中包含节点的子节点。

`nodeType`属性包含节点的类型。值`1`表示元素节点（此处为 HTML 元素节点），值`3`表示文本节点。文本节点的文本内容位于`nodeValue`属性中，HTML 元素节点的标签名称位于`nodeName`属性中。

以下示例程序使用前面描述的属性和方法以及一个递归函数，遍历文档 DOM 树的一部分：

```html
... <head> ...

   <script>
```

```javascript
function nodes(reference, level)

      {

         for(let i=0; i<reference.childNodes.length; i++)

         {

            const ch = reference.childNodes[i];

            if(ch.nodeType == 3)

               document.write("Level:" + level + ", Text: "

                  + ch.nodeValue + "<br>");

            else if(ch.nodeType == 1)

               document.write("Level:" + level + ", Tag: "

                  + ch.nodeName + "<br>");

            if(ch.hasChildNodes())

            {

               level++;

               nodes(ch, level);

               level--;

            }

         }

      }
```

```html
   </script>

</head>

<body>

   <p id="idParagraph">

      This <span style="font-style:italic;">is</span> a paragraph

      <span style="font-weight:bold;">with tags

      <span style="font-style:italic;">on multiple

      </span></span>levels</p>

   <script>
```

```javascript
const level = 0;

      nodes(document.getElementById("idParagraph"), level);
```

```html
   </script>

</body></html>
```



### 清单 5.3　`dom_children.htm` 文件

我们正在查看包含第一个段落的 DOM 树部分，并且递归函数 `nodes()` 首次被调用，参数是对该段落的引用。

变量 `level` 表示树中的当前层级。段落的子节点位于层级 0，它们的子节点位于层级 1，而它们的子节点位于层级 2。

在 `nodes()` 函数中，使用 `for` 循环遍历当前元素的子节点字段，并在循环中设置对当前字段元素的引用以简化代码。如果字段元素是对文本节点的引用，则输出其值；但如果是对 HTML 元素节点的引用，则显示其名称。

如果当前字段元素本身有子节点，则层级数递增，并再次调用 `nodes()` 函数。

通过这种方式，你可以遍历 DOM 树的所有分支。在某个时刻，你会确定每个分支都没有子节点，递归将返回。层级数会再次减少，最终回到层级 0。

程序的输出如图 5.5 所示。

![第一个段落的子节点](img/img-f5.6.html)

**图 5.5**　第一个段落的子节点

## 5.4　添加节点

在本节中，我们将创建文本节点、HTML 元素节点和属性节点，并将它们添加到文档中。我们使用 `document` 对象的以下两个方法：

- `createTextNode()` 方法，用于创建文本节点。该方法的参数是一个包含文本的字符串。
- `createElement()` 方法，用于创建 HTML 元素节点。该方法的参数是一个包含标签名称的字符串，不带尖括号。

此外，`node` 对象还使用了三个方法：

- `appendChild()` 方法，用于向节点添加子节点，添加在子节点字段的末尾。该方法的参数是对要添加的节点的引用。
- `setAttribute()` 方法，用于设置属性节点的值。如果属性节点尚不存在，则会先创建它。该方法的参数是两个字符串，分别包含属性的名称和新值。
- `insertBefore()` 方法，用于在另一个子节点之前向节点添加子节点。该方法的参数是两个引用：一个是对要添加的节点的引用，另一个是对插入位置之前的节点的引用。

以下是程序代码：

```html
... <head> ...

   <script>
```

```javascript
function append()
{
   const text = document.createTextNode("Appended");
   const par = document.createElement("p");

   par.appendChild(text);
   par.setAttribute("style", "font-weight:bold;");
   document.getElementById("idBody").appendChild(par);
}

function insert()
{
   const text = document.createTextNode("Inserted");
   const par = document.createElement("p");

   par.appendChild(text);
   par.setAttribute("style", "font-style:italic;");
   document.getElementById("idBody").insertBefore(
      par,
      document.getElementById("idParagraph3")
   );
}
```

```html
   </script>
</head>

<body id="idBody">
   <p id="idParagraph1">First paragraph</p>
   <p id="idParagraph2">Second paragraph</p>
   <p id="idParagraph3">Third paragraph</p>
   <p>
      <input id="idAppend" type="button" value="Append">
      <input id="idInsert" type="button" value="Insert">
   </p>

   <script>
```

```javascript
document.getElementById("idAppend")
   .addEventListener("click", append);

document.getElementById("idInsert")
   .addEventListener("click", insert);
```

```html
   </script>
</body>
</html>
```

**清单 5.4**　`dom_add.htm` 文件

在图 5.6 中，你可以看到原始文档。

![添加之前](img/img-f5.6.html)

**图 5.6**　添加之前

Append 和 Insert 按钮用于追加或插入新的 HTML 元素节点。

在 JavaScript 函数 `append()` 中，创建了一个包含文本 `Appended` 的新文本节点，然后为段落创建一个 HTML 元素节点。将文本节点和属性节点添加到 HTML 元素节点，然后将该 HTML 元素节点追加到文档的 `body` 节点的末尾。

在 `insert()` 函数中，一个新创建的包含文本节点和属性节点的 HTML 元素节点被插入到 `body` 节点的指定子节点之前。

在图 5.7 中，你可以看到两个按钮各点击两次后的文档。

![添加之后](img/img-f5.7.html)

**图 5.7**　添加之后

## 5.5　更改节点

在本节中，我将向你展示如何更改文本节点和 HTML 元素节点。这里介绍 `node` 对象的另外两个方法：

- `cloneNode()` 方法，用于创建节点的副本，可以选择是否包含所有子节点、子节点的子节点等。该方法的参数是一个布尔值。如果该布尔值为 `true`，则节点及其整个子节点结构都会被复制。
- `replaceChild()` 方法，用于将一个节点的子节点替换为另一个子节点。该方法的参数是两个引用：一个是对要添加的节点的引用，另一个是对要被替换的节点的引用。

`element` 对象的 `innerHTML` 属性也非常有用。它用于获取或设置包含文本的 HTML 标签。

以下是程序代码：

```html
... <head> ...

   <script>
```

```javascript
function textChange(id)
{
   const par = document.getElementById(id);

   if (par.hasChildNodes())
      par.firstChild.nodeValue = "Text changed";
   else
   {
      const text = document.createTextNode("Text created");
      par.appendChild(text);
   }
}

function htmlChange()
{
   const par = document.getElementById("idParagraph4");
   par.innerHTML = "Change <i>in fourth</i> paragraph";
}

function surround()
{
   const par = document.getElementById("idParagraph3");
   const italic = document.createElement("span");

   italic.setAttribute("style", "font-style:italic;");

   const replaced = par.replaceChild(italic, par.firstChild);
   italic.appendChild(replaced);
}

function clone()
{
   const par = document.getElementById("idParagraph3");
   const copy = par.cloneNode(true);

   document.getElementById("idBody").appendChild(copy);
}
```

```html
   </script>
</head>

<body id="idBody">
   <p id="idParagraph1">First paragraph</p>
   <p id="idParagraph2"></p>
   <p id="idParagraph3">
      <span style="font-weight:bold;">Third</span> paragraph
   </p>
   <p id="idParagraph4">Fourth paragraph</p>

   <p>
      <input id="idTextChange" type="button" value="Change text">
      <input id="idTextCreate" type="button" value="Create text">
      <input id="idHtml" type="button" value="Change text and HTML">
   </p>

   <p>
      <input id="idSurround" type="button" value="Surround node with HTML">
      <input id="idClone" type="button" value="Clone node">
   </p>

   <script>
```

```javascript
document.getElementById("idTextChange").addEventListener(
   "click",
   function() {
      textChange("idParagraph1");
   }
);

document.getElementById("idTextCreate").addEventListener(
   "click",
   function() {
      textChange("idParagraph2");
   }
);

document.getElementById("idHtml").addEventListener("click", htmlChange);
document.getElementById("idSurround").addEventListener("click", surround);
document.getElementById("idClone").addEventListener("click", clone);
```

```html
   </script>
</body>
</html>
```

**清单 5.5**　`dom_change.htm` 文件

在图 5.8 中，你可以看到原始文档。

![更改前](img/img-f5.8.html)

**图 5.8**　更改前

第二个段落不可见。虽然它是用 `p` 容器创建的，但它没有内容（即没有子节点）。

“更改文本”和“创建文本”按钮用于更改文本节点。如果文本节点尚不存在，则会先创建它。“更改文本和 HTML”按钮更改段落的内容，“用 HTML 包围节点”按钮用于用一个 HTML 节点包围一个节点（该节点可能包含子节点）。最后一个按钮“克隆节点”用于复制一个段落，包括所有子节点。该按钮被插入到文档的末尾。

JavaScript 函数 `textChange()` 被调用了两次，每次都以一个段落的唯一 ID 作为参数：

- 第一次通过“更改文本”按钮调用该函数时，第一个段落有一个文本节点作为其内容。因此 `hasChildNodes()` 方法返回 `true`，现有文本节点的内容被替换为其他内容。第二次点击“创建文本”按钮时也会发生同样的情况，因为所涉及的节点现在有了一个子节点。
- 第二次通过“创建文本”按钮调用该函数。第二个段落没有内容，因此 `hasChildNodes()` 方法返回 `false`。创建一个新的文本节点，并将其作为新的子节点添加到段落中。

在 `htmlChange()` 函数中，第四个段落的内容通过 `innerHTML` 属性被重置，即包含文本的 HTML 标签。

在 `surround()` 函数中创建了一个新的 HTML 元素节点。新的 HTML 元素节点替换了第三个段落的第一个子节点，然后这个（原来的）第一个子节点被放置在新节点下。这样就用 HTML 代码包围了这个子节点。

在 `clone()` 函数中，创建一个新节点作为第三个段落的副本，包括所有子节点。这个副本被追加到文档的末尾。

在图 5.9 中，你可以看到每个按钮被点击一次后的文档。

![更改后](img/img-f5.9.html)

**图 5.9**　更改后

## 5.6　删除节点

你也可以从 DOM 树中删除节点，使用 `node` 对象的以下方法：

- `removeChild()` 方法，用于删除节点的子节点。该方法的参数是对要删除的子节点的引用。
- `removeAttribute()` 方法，用于删除节点的属性节点。该方法的参数是一个字符串，包含要删除的属性名称。

这里是程序：

```html
... <head> ...

   <script>
```

```javascript
function removeNode()
{
   const par = document.getElementById("idParagraph2");
   document.getElementById("idBody").removeChild(par);
}

function removeAttribute()
{
   const par = document.getElementById("idParagraph3");
   par.removeAttribute("style");
}
```

```html
   </script>
</head>

<body id="idBody">
   <p id="idParagraph1">First paragraph</p>
   <p id="idParagraph2">Second paragraph</p>
   <p id="idParagraph3" style="font-weight:bold;">Third paragraph</p>

   <p>
      <input id="idNode" type="button" value="Remove node">
      <input id="idAttribute" type="button" value="Remove attribute">
   </p>

   <script>
```

```javascript
document.getElementById("idNode")
   .addEventListener("click", removeNode);

document.getElementById("idAttribute")
   .addEventListener("click", removeAttribute);
```

```html
   </script>
</body>
</html>
```

**清单 5.6**　`dom_delete.htm` 文件

在图 5.10 中，你可以看到原始文档。

![删除前](img/img-f5.10.html)

**图 5.10**　删除前

“删除节点”按钮删除第二个段落，“删除属性”按钮删除第三个段落的 `style` 属性。

在图 5.11 中，你可以看到删除后的文档。

![删除后](img/img-f5.11.html)

**图 5.11**　删除后

## 5.7　创建表格

在最后一个较大的示例中，你可以使用双重 `for` 循环创建一个全新的表格并将其嵌入文档中。在此上下文中，你使用 `document` 对象的 `createTextNode()` 和 `createElement()` 方法以及 `node` 对象的 `appendChild()` 方法。在 DOM 树中，你首先从外向内工作，然后再从内向外工作。

你按如下方式创建表格：

- 首先，为表格创建 HTML 元素节点。
- 然后在外层循环中创建行的 HTML 元素节点。
- 在内层循环中，依次执行以下步骤：
  - 为单元格创建文本节点。
  - 创建 HTML 元素节点。
  - 将文本节点嵌入到单元格的 HTML 元素节点中。
  - 将单元格嵌入到行的 HTML 元素节点中。
- 在外层循环中，将行的 HTML 元素节点插入到表格的 HTML 元素节点中。
- 最后，将表格的 HTML 元素节点嵌入到文档中。

这里是程序代码：

```html
... <head> ...

   <script>
```



```javascript
function createTable()
{
   const table = document.createElement("table");

   for(let r=1; r<=3; r++)
   {
      const row = document.createElement("tr");

      for(let c=1; c<=5; c++)
      {
         const text = document.createTextNode("Cell " + r + "/" + c);
         const cell = document.createElement("td");

         cell.appendChild(text);
         row.appendChild(cell);
      }

      table.appendChild(row);
   }

   document.getElementById("idBody").appendChild(table);
}
```

```html
</script>
</head>

<body id="idBody">
   <p><input id="idTable" type="button" value="Table"></p>

   <script>
```

```javascript
document.getElementById("idTable")
   .addEventListener("click", createTable);
```

```html
</script>
</body>
</html>
```

**清单 5.7**　`dom_table.htm` 文件

单击 Table 按钮一次后，文档显示如图图 5.12 所示。

![创建表格后](img/img-f5.12.html)

**图 5.12**　创建表格后

# 6　使用标准对象

在本章中，你将学习如何使用数组、字符串、数字和时间规范。

基于你在第 3 章中学到的知识，你可以创建自己的对象。然而，在 JavaScript 中，你经常也会使用许多预定义对象及其众多的属性和方法。本章将介绍预定义对象——`Array`、`String`、`Math`、`Number` 和 `Date`——它们用于编辑数组、字符串、数字、数学问题以及日期。

## 6.1　用于大量数据的数组

你已经熟悉了第一个简单的数组。它们被简称为字段。本节将详细讨论该主题。

数组用于将一组主题相关的数据存储在一个共同的名称下。数组由单个元素组成，这些元素从 0 开始编号。元素的编号称为其索引。

数组中的值通常具有相同的类型（例如，多个字符串作为城市名称，或几个数字作为温度值）。但是，你也可以在同一数组中保存不同类型的值。

在 JavaScript 中，使用 `Array` 对象来创建数组。它具有属性和方法，使你能够访问自己的数组和预定义数组。

### 6.1.1　一维数组

在下面的程序中，我们将创建一些一维数组，遍历它们并输出它们。以下是第 1 部分：

```html
...

<body><p>
   <script>
```

```javascript
let person = ["Ben", "Angela", "Will"];
person = ["Peter", "Monica", "John"];

const personTwo = person;

document.write("简单输出: " + personTwo + "<br><br>");
document.write("所有元素:<br>");
document.write("for 循环: ");

for(let i=0; i<person.length; i++)
   document.write(i + ":" + person[i] + " ");

document.write("<br>");
document.write("for-of 循环: ");

for(let p of person)
   document.write(p + " ");

document.write("<br><br>");
...
```

**清单 6.1**　`array_one_dim.htm` 文件，第 1 部分（共 4 部分）

这里，数组由一组名称组成。默认情况下，`Array` 对象写在方括号内，各个元素用逗号分隔。

该数组被赋值给 `person` 变量，因此该变量作为对数组的引用。它使用 `let` 声明，因此也可以将另一个数组赋值给它。

你可以创建对数组的更多引用，就像我们在这里使用 `personTwo` 所做的那样，它不是一个新数组。`toString()` 方法已经为 `Array` 对象预定义。它依次输出数组元素，仅用逗号分隔。

`length` 属性包含数组的长度（即元素的数量）。例如，它可以用于控制 `for` 循环。

有两种方法可以使用循环访问数组的所有元素：

- 通过 `for` 循环。数组的第一个元素索引为 0，因此称为 `person[0]`，第二个元素索引为 1，第三个索引为 2，依此类推。可以在 `for` 循环内更改数组的元素。
- 通过 `for`-`of` 循环，该循环是在 ECMAScript 2015 中引入的。每次运行循环时，数组的另一个元素会被赋值给一个变量（在本例中为 `p` 变量）。由于此变量是元素的副本，因此在循环内更改此变量不会导致元素更改。

在图 6.1 中，你可以看到不同的输出。

现在让我们看一下程序的第 2 部分：

```javascript
...
document.write("at() 方法:<br>");
document.write("for 循环: ");

for(let i=0; i<person.length; i++)
   document.write(i + ":" + person.at(i) + " ");

document.write("<br>");
document.write("最后一个元素: ");
document.write(person.at(-1) + " " + person.at(-2));
document.write("<br><br>");
...
```

**清单 6.2**　`array_one_dim.htm` 文件，第 2 部分（共 4 部分）

![数组的不同输出](img/img-f6.1.html)

**图 6.1**　数组的不同输出

`at()` 方法是在 ECMAScript 2022 中引入的。此方法访问索引作为参数传递的元素。与使用方括号访问元素不同，你还可以传递负值。–1 引用数组的最后一个元素，–2 引用倒数第二个元素，依此类推。

你可以在图 6.2 中看到第 2 部分的输出。

![at() 方法](img/img-f6.2.html)

**图 6.2**　`at()` 方法

程序的第 3 部分如下：

```javascript
...
document.write("包含:<br>");
document.write("John: " + person.includes("John") + "<br>");
document.write("Julia: " + person.includes("Julia") + "<br><br>");

document.write("转换、检查:<br>");

const tx = "Hello world";
const tf = Array.from(tx);

document.write("来自字符串的数组: " + tf + "<br>");
document.write(tx + " 是数组: " + Array.isArray(tx) + "<br>");
document.write(tf + " 是数组: " + Array.isArray(tf) + "<br><br>");
...
```

**清单 6.3**　`array_one_dim.htm` 文件，第 3 部分（共 4 部分）

`includes()` 方法是在 ECMAScript 2016 中引入的。它在现有数组上调用，检查数组是否包含特定值，并返回一个布尔值。

`Array.from()` 方法是在 `Array` 类本身上调用的，而不是在现有数组上，因为此时还没有数组。因此，它是一个静态方法，从合适的对象创建一个新数组。对象的每个元素成为数组的一个元素，对于字符串，字符串的每个单独字符成为一个元素，如你在图 6.3 中所见。

`Array.isArray()` 方法也是在 `Array` 类上调用的。此方法检查一个对象是否为 `Array` 对象，并返回一个布尔值。

![检查与转换](img/img-f6.3.html)

**图 6.3**　检查与转换

现在，这是程序的第 4 部分：

```javascript
...
document.write("填充:<br>");

const za = new Array(7);

document.write("开始时: " + za + "<br>");

za.fill(42, 3, 5);
document.write("部分元素: " + za + "<br>");

document.write("元素 0: " + za[0] + "<br>");
document.write("元素 7: " + za[7] + "<br>");

za.fill(42, 3);
document.write("结束时: " + za + "<br>");

za.fill(42);
document.write("所有元素: " + za + "<br><br>");
```

```html
</script></p>
</body>
</html>
```

**清单 6.4**　`array_one_dim.htm` 文件，第 4 部分（共 4 部分）

如果你只知道数组的大小而不知道其元素，你可以使用 `new` 创建一个新的 `Array` 对象。所需的大小在括号内指定。

`fill()` 方法用于用值填充数组，如下所示：

- 如果该方法只调用一个参数，则所有数组元素都会收到指定的值，此处为 42。
- 可选的第二个参数表示从哪个索引开始用指定值填充数组，此处为从索引 3 开始。
- 可选的第三个参数表示填充到哪个索引（不包括）为止，此处为从索引 3 到索引 5 之前。

如果你访问一个尚未赋值的元素，将输出 `undefined`，此处为 `za[0]` 元素。如果你访问数组外部的元素，此处为 `za[7]`，同样会输出 `undefined`。你可以在图 6.4 中看到输出。

![填充数组](img/img-f6.4.html)

**图 6.4**　填充数组

### 注意

ECMAScript 2024 引入了使用 `#` 字符使数组不可变的选项。例如，`let person = #["Ben", "Angela", "Will"];` 意味着数组的值不能再被更改。`person[0] = "Monica";` 语句将导致错误。

### 6.1.2　多维数组

你可以创建包含数组本身的数组。通过这种方式，你可以创建多维数组。例如，表格的数据可以保存在二维数组中，如下面程序的第一部分所示：

```html
...

<body><p>
   <script>
```

```javascript
document.write("Two-dimensional array:<br><br>");

const za = [[22.3, 18.5], [21.6, 19.7], [24.6, 20.1]];

document.write("Output with loop:<br>");

for(let i=0; i<za.length; i++)
   for(let k=0; k<za[i].length; k++)
      document.write(i + "/" + k + ":" + za[i][k] + "<br>");

document.write("<br>Simple output:<br>" + za + "<br>");
document.write("<br>Method at():<br>");

for(let i=0; i<za.length; i++)
   for(let k=0; k<za.at(i).length; k++)
      document.write(i + "/" + k + ":" + za.at(i).at(k) + "<br>");

if(Array.prototype.flat)
{
   const zb = za.flat();

   document.write(
      "<br>After conversion, length: "
      + zb.length + "<br><br>"
   );
}

...
```

**清单 6.5**　`array_multi_dim.htm` 文件，第 1 部分（共 2 部分）

`za` 数组是一个由子数组组成的数组。每个子数组用方括号括起来，所有子数组再次嵌入一个用方括号括起来的数组中。我插入空格只是为了说明清楚。

这里创建了一个二维数组，其中存储了一个小表格的数据。例如，它显示了三天不同日期的温度值，分别在上午和下午测量。

整个数组的 `length` 属性包含子数组的数量，而给定子数组的 `length` 属性包含该子数组的元素数量。你可以使用带有两个不同循环变量的双重 `for` 循环来输出数组的所有元素。这些变量表示数组第一维和第二维的索引。

得益于预定义的 `toString()` 方法，多维数组也可以轻松输出。然而，只列出了元素，数组的多维结构就不再可识别，如图 6.5 所示。

ECMAScript 2022 中引入的 `at()` 方法也可以用于多维数组。使用链式调用来输出单个元素：在通过 `at(i)` 访问的子数组中，访问通过 `at(k)` 访问的元素。

`flat()` 方法是在 ECMAScript 2019 中引入的。它可以使用内部递归从多维数组的元素创建一维数组，此处输出其数量。

![二维数组](img/img-f6.5.html)

**图 6.5**　二维数组

### 注意

JavaScript 中的对象具有 `prototype` 属性。在 JavaScript 面向对象编程的经典表示法中，该属性代表对象的原型，并允许你访问该原型。通过这种方式，你可以检查你所使用的浏览器是否存在特定元素。

### 注意

各个子数组中的元素数量也可能不同。

现在让我们看一下程序的第 2 部分：

```javascript
...
document.write("Three-dimensional array:<br>");

const zc = [
   [[19.8, 17.4], [16.5, 22.7]],
   [[15.1, 16.9], [22.7, 18.6]]
];

document.write("Output with loop:<br>");

for(let i=0; i<zc.length; i++)
   for(let k=0; k<zc[i].length; k++)
      for(let m=0; m<zc[i][k].length; m++)
         document.write(
            i + "/" + k + "/" + m + ":" + zc[i][k][m] + "<br>"
         );

document.write("<br>Simple output:<br>" + zc + "<br>");

if(Array.prototype.flat)
{
   const zd = zc.flat(2);

   document.write(
      "<br>After conversion with depth 2, length: "
      + zd.length
   );
}
```

```html
</script></p>
</body>
</html>
```




### 清单 6.6　array_multi_dim.htm 文件，第 2 部分（共 2 部分）

`zc`数组是三维的。例如，在不同日期、不同地点和不同时间测量的温度值可以存储在这样的数组中。

需要三个不同循环变量的三重循环来输出整个数组。这些变量表示数组第一维、第二维和第三维的索引。你可以在图 6.6 中看到输出。

![三维数组](img/img-f6.6.html)

**图 6.6**　 三维数组

你可以使用可选值调用`flat()`方法，以指定内部递归的深度，直到收集数组的元素。深度的默认值为 1，但要收集三维数组的所有元素，必须指定深度 2。

### 6.1.3　数组作为参数和返回值

数组可以作为参数传递给函数。传递是通过引用（按引用调用）进行的。因此，原始数组的值可以在函数中更改，无论对原始数组的引用是分配给可变变量还是不可变变量，这一点都适用。

函数可以返回对数组的引用作为结果。无论数组是先前作为参数传递的，还是仅在函数中创建的，这一点都成立。

在下面的程序中，使用一维和二维数组解释了这些关系。为了清楚起见，函数的定义写在调用附近。以下是程序的第一部分：

```html
...

<body><p>

   <script>
```

```javascript
function doubleOneDim(x)
{
   for(let i=0; i<x.length; i++)
      x[i] *= 2;
}

document.write("Array as parameter:<br>");

const za = [ 13, -2 ];

document.write(za + "<br>");

doubleOneDim(za);

document.write(za + "<br>");

...
```

#### 清单 6.7　array_function.htm 文件，第 1 部分（共 4 部分）

一维数组的引用被传递给`doubleOneDim()`函数。数组中的元素在函数内部被修改，并在函数调用前后输出数组（参见图 6.7）。

以下是程序的第 2 部分：

```javascript
...

function doubleTwoDim(x)
{
   for(let i=0; i<x.length; i++)
      for(let k=0; k<x[i].length; k++)
         x[i][k] *= 2;
}

const zb = [ [5, 8], [6, -2] ];

document.write(zb + "<br>");

doubleTwoDim(zb);

document.write(zb + "<br><br>");

...
```

#### 清单 6.8　array_function.htm 文件，第 2 部分（共 4 部分）

二维数组被传递给`doubleTwoDim()`函数。你可以在图 6.7 中看到输出。

![数组作为参数的引用](img/img-f6.7.html)

**图 6.7**　 数组作为参数的引用

以下是程序的第 3 部分：

```javascript
...

function addOneDim(x, y)
{
   const p = [];

   for(let i=0; i<x.length; i++)
      p[i] = x[i] + y[i];

   return p;
}

document.write("Array as return value:<br>");

const zc = [ 5, 12 ];

document.write(zc + "<br>");

const zd = addOneDim(za, zc);

document.write(zd + "<br>");

...
```

#### 清单 6.9　array_function.htm 文件，第 3 部分（共 4 部分）

两个一维数组被传递给`addOneDim()`函数。该函数使用空方括号创建一个空的一维数组，并通过赋值创建该数组的每个元素。两个传入数组的对应元素之和被赋值。

在`addOneDim()`函数末尾返回数组的引用，并将其赋值给`zd`变量。程序这一部分的输出显示在图 6.8 中。

现在来看程序的第 4 部分：

```javascript
...

function addTwoDim(x, y)
{
   const p = [ [], [] ];

   for(let i=0; i<x.length; i++)
      for(let k=0; k<x[i].length; k++)
         p[i][k] = x[i][k] + y[i][k];

   return p;
}

const ze = [ [7, -4], [2, 9] ];

document.write(ze + "<br>");

const zf = addTwoDim(zb, ze);

document.write(zf + "<br>");
```

```html
</script></p>

</body></html>
```

#### 清单 6.10　array_function.htm 文件，第 4 部分（共 4 部分）

两个二维数组被传递给`addTwoDim()`函数，该函数使用多对空方括号创建一个由两个空一维数组组成的二维数组。两个传入数组的对应元素之和被赋值。

返回的二维数组引用被赋值给`zf`变量，你可以在图 6.8 中看到程序这一部分的输出。

![返回数组的引用](img/img-f6.8.html)

**图 6.8**　 返回数组的引用

### 6.1.4　回调函数

你已经从第 2 章的 2.6.13 节中熟悉了回调函数这个术语。你可以将回调函数的引用赋值给一个函数，然后该函数在内部调用传入的回调函数，并使用其程序逻辑。

`Array`对象有一些预定义的方法会使用回调函数。在这个例子中，传递了一些命名的回调函数，为了清晰起见，我将它们定义在调用附近。你也可以传递匿名回调函数。

以下是程序：

```html
...

<body><p>

   <script>
```

```javascript
const za = [28.3, 16.5, 23.6, 16.7];

document.write("Array: " + za + "<br><br>");

document.write("Run with forEach():<br>");

function output(element, index)
{
   document.write(index + ":" + element + " ");
}

za.forEach(output);

document.write("<br><br>");

document.write("Examine with function:<br>");

function over(value)
{
   return value > this;
}

document.write("At least one value over 20: "
   + za.some(over, 20) + "<br>");

document.write("All values over 20: "
   + za.every(over, 20) + "<br><br>");

document.write("Filtering with function:<br>");

const zb = za.filter(over, 20);

document.write("New array with values over 20: " + zb + "<br><br>");

document.write("Apply to function:<br>");

function multiple(value)
{
   return value * this;
}

const zc = za.map(multiple, 4);

document.write("New array with values * 4: " + zc + "<br>");
```

```html
</script></p>

</body></html>
```

#### 清单 6.11　array_callback.htm 文件

`forEach()` `Array`方法用于对数组的所有元素执行一个回调函数（本例中为`output()`函数）。调用`forEach()`方法时，会传入回调函数的名称。

在内部，`forEach()`方法确保向`output()`回调函数传递多个参数（其中一些是可选的）。这些参数可以出现在`output()`回调函数的定义中。第一个参数是当前数组元素的副本，第二个参数是可选的，对应于当前元素的索引。`output()`回调函数输出数组的所有元素及其索引和值。

`Array`方法`some()`检查数组中是否至少有一个元素满足回调函数（此处为`over()`）中的某个条件。`Array`方法`every()`对数组的所有元素执行相同的检查。参数（其中一些是可选的）也会在内部传递给`over()`回调函数。

在调用某个`Array`方法时，除了回调函数的名称外，还可以传递一个额外的参数。在回调函数内部，可以通过`this`访问这个参数。回调函数`over()`随后检查某些（或所有）元素的值是否大于额外传入的参数值。

`Array`方法`filter()`创建一个新的`Array`对象，其中包含原始数组中满足回调函数中某个条件的所有元素的副本。这里再次调用了回调函数`over()`，并且也传递了一个额外的参数。

`Array`方法`map()`也会创建一个新的`Array`对象，其中包含原始数组所有元素的副本。这里调用了`multiple()`回调函数，并将所有元素的值乘以一个作为附加参数传入的因子。

以下是一个使用匿名回调函数调用`map()`函数的示例：`const zd = za.map(function(value) { return value * this; }, 4);`。`map()`函数的第一个参数不是命名函数的名称，而是函数的完整定义，不包含函数名。

程序的输出如图 6.9 所示。

![回调函数](img/img-f6.9.html)

**图 6.9**　 回调函数

### 6.1.5　添加和删除元素

在 JavaScript 中，数组是动态的。本节介绍`Array`对象的方法，这些方法允许你向数组添加元素或从数组中删除元素。

方法如下：

* `push()`方法，用于在数组末尾添加元素
* `pop()`方法，用于从数组末尾删除元素
* `unshift()`方法，用于在数组开头添加元素
* `shift()`方法，用于从数组开头删除元素
* `splice()`方法，用于在数组中间添加或删除元素

`toSpliced()`方法自 ECMAScript 2023 起可用。它的工作方式与`splice()`方法类似，只是结果会保存到一个新数组中。

除了这里提到的方法外，以下示例程序还使用了`delete`运算符来删除元素的内容：

```html
...

<body><p>

   <script>
      const city = ["Berlin", "Rome"];

      document.write("Array: " + city + "<br><br>");

      city.push("Bern", "Brussels");

      document.write("push: " + city + "<br>");

      const p = city.pop();

      document.write("pop: " + city + "<br>");

      document.write("Removed: " + p + "<br><br>");

      city.unshift("Madrid", "London");

      document.write("unshift: " + city + "<br>");

      const s = city.shift();

      document.write("shift: " + city + "<br>");

      document.write("Removed: " + s + "<br><br>");

      city.splice(2, 1, "Prague", "Sofia");

      document.write("splice to add: " + city + "<br>");

      city.splice(1, 2);

      document.write("splice to delete: " + city + "<br><br>");

      let cityTwo = city.toSpliced(1, 1, "Oslo", "Athens");

      document.write("add for new array: " + cityTwo + "<br>");

      cityTwo = city.toSpliced(1, 1);

      document.write("remove for new array: " + cityTwo + "<br><br>");

      delete city[1];

      document.write("delete: " + city);
   </script></p>

</body></html>
```

**清单 6.12**　array_dynamic.htm 文件

创建了一个包含城市名称的数组，并对其进行了多次修改。每次修改后都会输出数组，如图 6.10 所示。

你可以使用`push()`方法在末尾追加一个或多个元素，追加顺序与调用时作为参数指定的顺序一致。`pop()`方法从数组末尾删除一个元素，并将该元素作为返回值返回。

`unshift()`和`shift()`方法在数组开头执行相同的操作。`shift()`方法将删除的元素作为返回值返回。

![添加和删除元素](img/img-f6.10.html)

**图 6.10**　 添加和删除元素

`splice()`方法可以在任意位置修改数组。第一个参数指定开始删除或添加元素的位置，第二个参数确定要删除的元素数量，从第三个参数开始，可以指定一个或多个要添加的新元素。如果不指定新元素，则只会删除现有元素。

`toSpliced()`方法的工作方式与`splice()`方法类似，但结果会保存到一个新数组中（此处为`cityTwo`数组）。

`delete`运算符仅删除元素的内容，而不删除元素本身。这会产生一个空位，因此为了避免这种空位，可以使用`splice()`代替`delete`。

### 6.1.6　修改数组

本节包含一些可用于整体修改数组的方法。修改的结果可以保存在原数组中，也可以保存在新数组中。

用于在原数组内修改的方法如下：

* `concat()`方法，用于连接两个数组
* `sort()`方法，用于对数组进行排序
* `reverse()`方法，用于反转数组元素的顺序
* `join()`方法，用于从数组元素创建字符串
* `copyWithin()`方法，用于在数组内复制元素

自 ECMAScript 2023 起新增的方法（结果保存到新数组中，不修改原数组）包括：

* `toSorted()`，用于对数组进行排序
* `toReversed()`，用于反转数组元素的顺序
* `with()`，用于修改数组中的选定元素

以下是程序：

```html
...

<body><p>

   <script>
      let city = ["Berlin", "Rome", "Oslo"];

      document.write("Original: " + city + "<br><br>");

      const cityTwo = ["Brussels", "Madrid", "London"];

      city = city.concat(cityTwo);

      document.write("Concatenated: " + city + "<br>");

      city.sort();

      document.write("Sorted: " + city + "<br>");

      city.reverse();

      document.write("Reversed: " + city + "<br><br>");

      const tx = city.join(" # ");

      document.write("Concatenated to a string: " + tx + "<br><br>");
```




```javascript
document.write("Previously: " + city + "<br>");

city.copyWithin(1, 3, 5);

document.write("Internally copied: " + city + "<br><br>");

let cityThree = city.toSorted();

document.write("Sorted into new array: " + cityThree + "<br>");

cityThree = city.toReversed();

document.write("Reversed into new array: " + cityThree + "<br>");

cityThree = city.with(2, "Paris");

document.write("With change into new array: " + cityThree);
```

**清单 6.13**　`array_change.htm` 文件

同样，创建了一个包含城市名称的数组。对该数组应用了多种方法，图 6.11 显示了结果。

`concat()` 方法在最初创建的数组上调用，并将另一个数组的元素按指定顺序追加到该数组中。

你可以使用 `sort()` 方法按字母顺序对数组进行排序。排序顺序基于 UTF-16 编码，这是一种用于 Unicode 字符的编码方式。其中，大写字母优先于小写字母，因此字符串 `oslo`（小写 `o`）会排在末尾。我在第 6.1.8 节中描述了如何按数值对数组进行排序。

`reverse()` 方法用于反转元素的顺序。由于数组之前已经排序，在这种情况下它会按相反顺序排序。

`join()` 方法用于将数组转换为字符串。该字符串包含数组的所有元素，每个元素之间由调用 `join()` 时作为参数指定的字符串分隔。对于反向操作（即将字符串转换为数组），可以使用 `split()` 方法（第 6.2.2 节）。

`copyWithin()` 方法可以接受最多三个参数。第一个参数指定从哪个位置开始用复制的元素覆盖原数组中的元素。复制的元素按如下方式选择：第二个参数指定第一个元素的位置，第三个参数指定最后一个元素之后的位置。如果省略第三个参数，则从第一个元素开始复制所有元素。

![更改数组](img/img-f6.11.html)

**图 6.11**　更改数组

`toSorted()` 方法用于将数组的元素按字母顺序排序后保存到一个新数组中。相应地，`toReversed()` 方法用于将数组的元素反转后保存到一个新数组中。

使用 `with()` 方法时，会将一个数组保存到新数组中，并更改新数组中的某个选定元素。该方法的第一个参数指定该元素的位置，第二个参数指定其新值。

在这三种情况下，原始数组都不会被改变。

### 6.1.7　复制数组

`slice()` 方法用于从现有数组的特定（或全部）元素创建一个新数组。以下是一个示例程序：

```html
...

<body>
  <p>
    <script>
```

```javascript
let city = ["Berlin", "Rome", "Oslo"];

document.write("Original: " + city + "<br><br>");

let cityTwo = city.slice();

document.write("slice, from 0 to end, thus copy: " + cityTwo + "<br>");

cityTwo = city.slice(2);

document.write("slice, from 2 to end: " + cityTwo + "<br>");

cityTwo = city.slice(-2);

document.write("slice, from -2 to end: " + cityTwo + "<br>");

cityTwo = city.slice(1, 2);

document.write("slice, from 1 to 2 excluded: " + cityTwo + "<br>");

cityTwo = city.slice(0, -2);

document.write("slice, from 0 to -2 excluded: " + cityTwo + "<br><br>");
```

```html
    </script>
  </p>
</body>
</html>
```

**清单 6.14**　`array_copy.htm` 文件

已知的城市名称数组作为原始数组。`slice()` 方法用于创建一个新数组，其中包含原始数组的特定（或全部）元素，该方法有两个可选参数，用于指定位置。

如果调用该方法时不带参数，则整个原始数组会被复制到一个新数组中。如果调用时带一个参数，则从指定位置开始的所有元素都会被复制到新数组中。如果调用时带两个参数，则新数组包含从第一个指定位置到第二个指定位置（不包括）之间的元素。

如果两个参数中的任何一个为负值，则相应的位置从原始数组的末尾开始计算。请记住，索引 `0` 表示第一个元素，索引 `–1` 表示最后一个元素。

程序的输出如图 6.12 所示。

![复制数组](img/img-f6.12.html)

**图 6.12**　复制数组

### 6.1.8　对数字数组进行排序

使用回调函数，你可以通过 `sort()` 方法按数字对数组进行排序。以下是一个示例程序：

```html
... <head> ...

<script>
```

```javascript
function ascending(x, y) {
  if (x > y) return 1;
  else return -1;
}

function descending(x, y) {
  if (y > x) return 1;
  else return -1;
}
```

```html
</script>
</head>

<body>
  <p>
    <script>
```

```javascript
const za = [3, 28, 2, 14];

document.write("Unsorted: " + za + "<br>");

za.sort();

document.write("Sorted by characters: " + za + "<br>");

za.sort(ascending);

document.write("Sorted by numbers, ascending: " + za + "<br>");

za.sort(descending);

document.write("Sorted by number, descending: " + za + "<br><br>");

const zb = [3, 28, 2, 14];

const zc = zb.toSorted(ascending);

document.write("Sorted to a new array: " + zc);
```

```html
    </script>
  </p>
</body>
</html>
```

**清单 6.15**　`array_sort.htm` 文件

名为 `za` 的数字数组最初是未排序的。

如果调用 `sort()` 方法时不带参数，数组将按字母顺序排序，如第 6.1.6 节所述。这意味着，例如，数字 `14` 会排在数字 `2` 之前。这是因为数字被单独考虑，数字 `1` 排在数字 `2` 之前——但对于数字数组来说，这毫无意义。

调用 `sort()` 方法时，你可以传递一个比较函数的引用，用于排序。在第一种情况下，你想按数字升序排序。这里，将 `ascending()` 函数的引用传递给该方法，`sort()` 方法内部使用该函数来比较两个元素。

如果在此比较中第一个元素大于第二个元素，则返回正值；否则返回负值。这会导致两个被比较的元素按升序排序。在 `sort()` 方法的内部排序过程中，会对两个元素重复执行此操作，因此最终数组的所有元素都按升序排序。

`descending()` 函数用于按数字降序排序。在图 6.13 中，你可以看到程序的结果。

你也可以在调用 `toSorted()` 方法时传递比较函数的引用。该函数是在 ECMAScript 2023 中引入的。它按数字升序对数组的元素进行排序，并将它们保存到一个新数组中。在此过程中，原始数组不会被改变。

![对数字数组排序](img/img-f6.13.html)

**图 6.13**　对数字数组排序

### 6.1.9　在数组中查找元素

`find()` 和 `findIndex()` 方法也使用回调函数，这些函数可以访问内部传递的参数。这些方法找到数组中满足特定条件的第一个元素或其索引，并且在每种情况下，还可以传递另一个有助于搜索的参数。

ECMAScript 2023 引入了紧密相关的 `findLast()` 和 `findLastIndex()` 方法。它们用于查找满足特定条件的最后一个元素或其索引。

以下是一个示例程序：

```html
...

<body>
  <p>
    <script>
```

```javascript
const za = [3, 14, 2, 28, 5, 8];

document.write("Array: " + za + "<br>");

function elementGreaterValue(element) {
  if (element > this) return element;
}

document.write(
  "First element > 10: " + za.find(elementGreaterValue, 10) + "<br>"
);

document.write(
  "Last element > 10: " + za.findLast(elementGreaterValue, 10) + "<br>"
);

function indexGreaterValue(element, index) {
  if (element > this) return index;
}

document.write(
  "Index for first element > 10: " +
    za.findIndex(indexGreaterValue, 10) +
    "<br>"
);

document.write(
  "Index for last element > 10: " +
    za.findLastIndex(indexGreaterValue, 10) +
    "<br>"
);
```

```html
    </script>
  </p>
</body>
</html>
```

**清单 6.16**　`array_find.htm` 文件

创建了一个名为 `za` 的数字数组。

调用 `find()` 方法时，会传入对 `elementGreaterValue()` 回调函数的引用。该回调函数返回第一个大于额外传入参数值的元素。所有元素依次被检查，一旦找到符合条件的元素，检查即中止并返回该元素。

调用 `findIndex()` 方法时，会传入对 `indexGreaterValue()` 回调函数的引用。它返回第一个满足检查条件的值的索引，图 6.14 显示了结果。

`findLast()` 和 `findLastIndex()` 方法的工作方式相同，只是针对最后一个元素或其索引。

![在数组中查找元素](img/img-f6.14.html)

**图 6.14**　在数组中查找元素

### 6.1.10　解构与展开运算符

在第 2 章的第 2.6.6 节中，你已经了解了解构赋值。借助解构和展开运算符 `...`（三个点），数组还有更多可能性，下面通过示例进行说明。

以下是程序的第一部分：

```html
...

<body>
  <p>
    <script>
```

```javascript
let a, b, c, remainder;

[a, b, c] = [12, 15, -6];

document.write("Variables: " + a + " " + b + " " + c + "<br>");

[a, b, c] = [12, 15];

document.write(
  "Too few array elements: " + a + " " + b + " " + c + "<br>"
);

[a, b] = [12, 15, -6];

document.write("Too many array elements: " + a + " " + b + "<br>");

[a, ...remainder] = [12, 15, -6];

document.write(
  "Variable: " + a + ", Remainder to array: " + remainder + "<br>"
);

const f = [3, 28, 4];

[a, b, c] = f;

document.write("From array: " + a + " " + b + " " + c + "<br><br>");

...
```

**清单 6.17**　`array_destructuring.htm` 文件，第 1 部分（共 3 部分）

数组 `[12, 15, –6]` 在一条语句中被赋值给三个变量。如果变量太少，剩余变量会被赋值为 `undefined`。如果变量太多，多余的数组元素会被忽略。

使用展开运算符 `...`，可以确保多余的数组元素被赋值给另一个数组（此处为 `remainder`）。

如果赋值右侧有一个引用数组的变量，所有操作的行为相同。

该部分程序的输出如图 6.15 所示。

![解构与展开运算符](img/img-f6.15.html)

**图 6.15**　解构与展开运算符

以下是程序的第二部分：

```javascript
...

function add(a, b, ...remainder) {
  let sum = a + b;

  for (let i = 0; i < remainder.length; i++) sum += remainder[i];

  return sum;
}

document.write("One number: " + add(3) + "<br>");

document.write("Two numbers: " + add(3, 5) + "<br>");

document.write("Six numbers: " + add(3, 5, 4, 9, 3, 2) + "<br><br>");

...
```

**清单 6.18**　`array_destructuring.htm` 文件，第 2 部分（共 3 部分）

你也可以使用展开运算符 `...` 让函数更灵活。可以向 `add()` 函数传递两个或更多参数，该函数会将所有参数相加。前两个参数存储在变量 `a` 和 `b` 中，其余所有参数存储在 `remainder` 数组中。如果参数少于两个，将会发生错误。

该部分程序的输出如图 6.16 所示。

![函数与展开运算符](img/img-f6.16.html)

**图 6.16**　函数与展开运算符

以下是程序的第三部分：

```javascript
...

function maxi(x) {
  let maximum = x[0][0],
    row = 0,
    column = 0;

  for (let i = 0; i < x.length; i++)
    for (let k = 0; k < x[i].length; k++)
      if (x[i][k] > maximum) {
        maximum = x[i][k];
        row = i;
        column = k;
      }

  return [maximum, row, column];
}

const zb = [
  [-3, 28, 4],
  [6, -5, 12],
];

document.write("Array: " + zb + "<br>");

let maximum, row, column;

[maximum, row, column] = maxi(zb);

document.write(
  "Maximum:" + maximum + ", Row:" + row + ", Column:" + column + "<br>"
);
```

```html
    </script>
  </p>
</body>
</html>
```



**清单 6.19**　`array_destructuring.htm` 文件，第 3 部分（共 3 部分）

解构允许函数返回多个值。该程序确定二维数组的最大值及其首次出现的位置（由行索引和列索引组成）。程序返回所有三个值。

在`maxi()`函数中，二维数组被传递给变量`x`。首先，假定最大值位于左上角的数组元素（即行索引 0、列索引 0）。检查所有数组元素，如果找到比当前最大值更大的元素，则保存其值和位置。函数末尾返回一个包含三个结果的数组，并将其赋值给三个变量。

该部分程序的输出如图 6.17 所示。

![函数返回值的解构](img/img-f6.17.html)

**图 6.17**　函数返回值的解构

### 6.1.11 对象数组

你可以将对象的引用分组到一个数组中。借助`toString()`方法，此类数组的输出很简单。可以使用合适的排序标准对此类数组进行排序。

以下是一个示例程序：

```html
... <head> ...

   <script>
```

```javascript
class Car
{
   constructor(c, s)
   {
      this.color = c;
      this.speed = s;
   }

   toString()
   {
      return this.color + "/" + this.speed;
   }
}

function descending(x, y)
{
   if (y.speed > x.speed)
      return 1;
   else
      return -1;
}
```

```html
   </script>
</head>

<body><p>
   <script>
```

```javascript
const vc = [new Car("Red", 50),
   new Car("Blue", 85), new Car("Yellow", 65)];

document.write("unsorted: " + vc + "<br>");
vc.sort(descending);
document.write("sorted: " + vc);
```

```html
   </script></p>
</body></html>
```

**清单 6.20**　`array_object.htm` 文件

程序创建了三个`Car`对象，并将这些对象的引用保存在名为`vc`的数组中。`toString()`方法对`Array`对象和`Car`对象都可用，因此可以使用`document.write()`方法输出整个数组。

数组按速度降序排序，当调用`sort()`方法时，会传入一个回调函数的名称来实现排序。内部比较的两个数组元素是`Car`类对象的引用。通过比较两个`speed`属性的值，回调函数返回正数或负数，从而确保数组正确排序。结果如图图 6.18 所示。

![带排序的对象数组](img/img-f6.18.html)

**图 6.18**　带排序的对象数组

### 注意

你可以在本书的可下载材料中找到`u_one_dimensional`和`u_multi_dimensional`练习，位于附加章节 1 的第 1.15 和 1.16 节，下载地址为[www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

## 6.2 处理字符串

你已经熟悉了字符串，它们类似于数组，用于存储来自输入等来源的文本。字符串中的单个字符从 0 开始编号，字符串中单个字符的编号也称为索引。

`String`对象及其属性和方法可用于读取和修改字符串。在一些示例中，你已经看到了用于连接字符串的`+`运算符和用于扩展字符串的组合赋值运算符`+=`。

### 6.2.1 创建和检查字符串

以下程序创建一个字符串并确定其长度。ECMAScript 2015 引入了`includes()`、`startsWith()`和`endsWith()`方法，你可以使用这些方法来确定一个字符串是否包含、以另一个字符串开头或结尾。

程序如下：

```html
...

<body><p>
   <script>
```

```javascript
const tx = "info@rheinwerk-publishing.com";

document.write("Text: " + tx + "<br>");
document.write("Length: " + tx.length + "<br>");
document.write("Length: " + "publish".length + "<br>");
document.write("Contains 'publish': " + tx.includes("publish") + "<br>");
document.write("Contains 'Publish': " + tx.includes("Publish") + "<br>");
document.write("Contains 'publish' from 16: "
   + tx.includes("publish", 16) + "<br>");
document.write("Starts with 'info': " + tx.startsWith("info") + "<br>");
document.write("Starts with 'info' from 1: "
   + tx.startsWith("info", 1) + "<br>");
document.write("Ends with 'com': " + tx.endsWith("com") + "<br>");
document.write("Ends with 'com' before 28: "
   + tx.endsWith("com", 28) + "<br><br>");
```

```html
   </script></p>
</body></html>
```

**清单 6.21**　`string_check.htm` 文件

`tx`变量被赋值为一个包含电子邮件地址的字符串，`length`属性包含字符串中的字符数。属性和方法不仅可以应用于引用`String`对象的变量，还可以直接应用于双引号内的字符串（参见`"publish".length`）。

`includes()`方法最多接受两个参数。第一个参数对应要在`String`对象中搜索的字符串，第二个可选参数可用于指定搜索开始的`String`对象中的位置。

`startsWith()`方法的情况类似。`endsWith()`方法也可以指定第二个参数，在这种情况下，`String`对象首先被缩短到指定的长度进行搜索。然后程序检查它是否以你要查找的字符串结尾。

程序的输出如图图 6.19 所示。

![创建和检查字符串](img/img-f6.19.html)

**图 6.19**　创建和检查字符串

### 6.2.2 字符串的元素

与数组一样，你可以使用方括号确定字符串的单个字符。此外，自 ECMAScript 2022 起，`at()`方法也可用于此目的，并且支持负索引。

你可以使用`split()`方法通过分隔符字符串来分割字符串。会创建一个包含字符串各个部分的`Array`对象，在此上下文中，再次展示了`Array`对象的`join()`方法，它又将数组连接成一个字符串。

`fromCodePoint()`方法是在 ECMAScript 2015 中引入的，它从一系列码点（对应于 UTF-16 编码中字符的编号）创建字符串。`codePointAt()`方法返回字符串中单个字符的此编号。

以下是一个带有示例的程序：

```html
...

<body><p>
   <script>
```

```javascript
const tx = "info@rheinwerk-publishing.com";

document.write("Text: " + tx + "<br>");

document.write("Characters with []: ");
for (let i = 0; i < 5; i++)
   document.write(i + ":" + tx[i] + " ");

document.write("...<br>Characters with at(): ");
for (let i = 0; i < 5; i++)
   document.write(i + ":" + tx.at(i) + " ");

document.write("...<br>");
document.write("Last elements: ");
document.write(tx.at(-1) + " " + tx.at(-2));
document.write("<br><br>");

document.write("Split in array: ");
const a = tx.split(".");
for (let i = 0; i < a.length; i++)
   document.write(i + ":" + a[i] + " ");

document.write("<br>");
const txNew = a.join(".");
document.write("Join array to string: " + txNew + "<br><br>");

const uc = String.fromCodePoint(
   97, 48, 65, 228, 246, 252, 196, 214, 220, 223
);

document.write("Codepoints result in string: " + uc);
document.write("<br>String results in codepoints:<br>");

for (let i = 0; i < uc.length; i++)
   document.write(i + ":" + uc.codePointAt(i) + " ");

document.write("<br><br>");
```

```html
   </script></p>
</body></html>
```

**清单 6.22**　`string_elements.htm` 文件

使用两个`for`循环，以两种不同方式将各个字符连同索引一起输出。

然后使用`split()`方法根据点（即使用`"."`分隔符字符串）分割字符串。各个数组元素不包含分隔符字符串本身。使用`Array`方法`join()`和相同的分隔符字符串，从数组元素创建一个新字符串。

`String.fromCodePoint()`方法是在`String`对象本身上调用的，而不是在现有字符串上，因为此时还没有字符串。这种方法被称为静态方法（另请参见第 6.1.1 节）。

小写字母的码点为 97 到 122，大写字母的码点为 65 到 90，数字的码点为 48 到 57。例如，德语变音符号和ß字符不在这个常规序列中。而`codePointAt()`方法则返回码点。

你可以在图 6.20 中看到输出。

![字符串的元素](img/img-f6.20.html)

**图 6.20**　字符串的元素

### 6.2.3 搜索与子字符串

`indexOf()`和`lastIndexOf()`方法返回一个字符串在另一个字符串中首次或最后一次出现的位置索引。如果未找到该字符串，则返回值–1。

`substring()`和`substr()`方法返回字符串一部分的副本。下面是一个带有示例的程序：

```html
...

<body><p>
   <script>
```

```javascript
const tx = "info@rheinwerk-publishing.com";

document.write("Text: " + tx + "<br>");
document.write("First character 'i': " + tx.indexOf("i") + "<br>");
document.write("Last character 'i': " + tx.lastIndexOf("i") + "<br>");

document.write("All characters 'i': ");
let pos = tx.indexOf("i");

while (pos != -1)
{
   document.write(pos + " ");
   pos = tx.indexOf("i", pos + 1);
}

document.write("<br><br>");
document.write("From 4 to end: " + tx.substring(4) + "<br>");
document.write("From 4 to 7 excluded: " + tx.substring(4, 7) + "<br>");
document.write("From 4, length 6: " + tx.substr(4, 6) + "<br><br>");
```

```html
   </script></p>
</body></html>
```

**清单 6.23**　`string_position.htm` 文件

首先，程序确定字符串中第一个或最后一个字符`i`的位置。

在`indexOf()`方法中，你可以选择指定搜索开始的起始位置。相应地，`lastIndexOf()`方法可以选择指定搜索结束的位置。

你可以使用`while`循环来搜索所有字符`i`的位置。对字符`i`下一次出现的搜索总是从上次找到的位置开始。

如果只为`substring()`和`substr()`方法各指定一个参数，则返回从指定位置开始到字符串末尾的部分。`substring()`方法的第二个可选参数指定哪个字符是第一个不再被复制的字符。相比之下，`substr()`方法可以指定要复制的字符数。

你可以在图 6.21 中看到输出。

![搜索与子字符串](img/img-f6.21.html)

**图 6.21**　搜索与子字符串

### 6.2.4 修改字符串

有许多方法可用于修改字符串。`toUpperCase()`和`toLowerCase()`方法将每个字母转换为大写或小写字母。

`replace()`方法将搜索到的字符串的第一次出现替换为另一个字符串。ECMAScript 2021 引入了`replaceAll()`方法，它对搜索到的字符串的所有出现执行相同的操作，并且已被所有现代浏览器使用。

`repeat()`方法是在 ECMAScript 2015 中引入的，它返回字符串的指定重复次数。

自 ECMAScript 2017 起，`padStart()`和`padEnd()`方法可用。你可以用另一个（可能重复的）字符串填充字符串的开头或结尾，直到达到所需长度。

`trim()`方法是在 ECMAScript 2015 中引入的。它移除字符串开头和结尾的所有空白字符——例如空格、制表符或行尾字符。自 ECMAScript 2019 起，还有`trimStart()`和`trimEnd()`方法，它们仅移除开头或结尾的指定字符。

下面是一个带有示例的程序：

```html
...

<body><p>
   <script>
```

```javascript
const tx = "info@rheinwerk-publishing.com";

document.write("Text: " + tx + "<br>");

const tg = tx.toUpperCase();
document.write("All uppercase: " + tg + "<br>");
document.write("All lowercase again: " + tg.toLowerCase() + "<br><br>");

document.write("Replace: " + tx.replace("info", "mail") + "<br>");
document.write("Replace all: " + tx.replaceAll("i", "I") + "<br><br>");

const ha = "Hello";
document.write("Repeat: " + ha.repeat(5) + "<br><br>");

document.write("Padding at the beginning: "
   + ha.padStart(10, "xy") + "<br>");
document.write("Padding at the end: "
   + ha.padEnd(10, "xy") + "<br><br>");
```



```javascript
const tr = " \t Hello\t \n \r";

document.write("Before trimming: |" + tr + "|<br>");

document.write("Codepoints: ");

for (let i = 0; i < tr.length; i++) {
  document.write(tr.codePointAt(i) + " ");
}

document.write("<br>");

document.write(
  "After trimming at the beginning: |" + tr.trimStart() + "|<br>"
);

document.write("After trimming at the end: |" + tr.trimEnd() + "|<br>");

document.write("After trimming: |" + tr.trim() + "|<br>");
```

```html
</script></p>

</body></html>
```

**清单 6.24**　`string_change.htm` 文件

变量 `tg` 被赋值为 `tx` 字符串的一个副本，该副本仅包含大写字母。`tx` 字符串本身保持不变，然后输出 `tg` 的一个副本，其中仅包含小写字母。

在字符串中，第一次（也是本例中唯一一次）出现的字符串 `"info"` 被替换为 `"mail"`。然后，所有字符 `i` 被替换为字符 `I`。

字符串 `"Hello"` 被重复五次返回，然后使用字符串 `"xy"` 填充至十个字符，一次在开头，一次在结尾。字符串 `"xy"` 被完整重复两次，一次不完整。

另一个字符串在修剪前共有十三个字符。开头和结尾有一些空白字符：空格（码点 32）、制表符（码点 9）以及行结束字符（码点 10 或 13）。在开头修剪后，只剩下十个字符；在结尾修剪后，只剩下八个字符；全部修剪后，只剩下五个字符。为清晰起见，在字符串前后显示了 `|` 字符。

你可以在图 6.22 中看到输出。

![字符串修改](img/img-f6.22.html)

**图 6.22**　字符串修改

### 6.2.5 检查密码

作为 `String` 对象的一个应用示例，对输入的密码进行检查。如果密码不符合图 6.23 中的标准，则相应的表单将不会被提交。

![检查密码](img/img-f6.23.html)

**图 6.23**　检查密码

以下是程序：

```html
... <head> ...

<script>
```

```javascript
const lowercase = "abcdefghijklmnopqrstuvwxyz";

const uppercase = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";

const number = "0123456789";

const special = "!&?+-*";

function submit(e) {
  const pw = document.getElementById("idPassword").value;

  if (pw.length < 8 || pw.length > 12) {
    alert("Password must contain 8-12 characters");
    e.preventDefault();
    return false;
  }

  let l = 0,
    u = 0,
    n = 0,
    s = 0;

  for (let i = 0; i < pw.length; i++) {
    if (lowercase.includes(pw[i])) l++;
    if (uppercase.includes(pw[i])) u++;
    if (number.includes(pw[i])) n++;
    if (special.includes(pw[i])) s++;
  }

  if (l < 2 || u < 2 || n < 2 || s < 1) {
    alert("Minimum number not met");
    e.preventDefault();
    return false;
  }

  return true;
}
```

```html
</script>

</head>

<body>
  <form id="idForm" method="post" action="string_password.php">
    <p>
      <input id="idPassword" type="password" name="password" />
      密码
    </p>

    <p><input type="submit" /> <input type="reset" /></p>

    <p>
      最少 8 个字符，最多 12 个字符<br />
      最少 2 个小写字母<br />
      最少 2 个大写字母<br />
      最少 2 个数字<br />
      最少 1 个来自 "!&?+-*" 的特殊字符
    </p>
  </form>

  <script>
```

```javascript
document
  .getElementById("idForm")
  .addEventListener("submit", function (e) {
    return submit(e);
  });
```

```html
</script>

</body>
</html>
```

**清单 6.25**　`string_password.htm` 文件

一些字符串保存了以下允许的字符：

- 小写字母和大写字母，不含任何语言特定的特殊字符
- 数字 0 到 9
- 一组特殊字符

当表单提交时，会调用 `submit()` 函数。输入的密码被保存为一个字符串。如果密码太短或太长，会显示相应的错误信息，函数终止，表单不会被提交。

如果字符串长度正确，首先声明一些计数器并设置为 0。然后使用 `for` 循环遍历输入的各个字符，并使用 `includes()` 方法判断它们是否为允许的字符之一。如果是，则相应的计数器增加。

循环结束后，判断是否有任何计数器的值不满足各自的最小数量要求。如果不满足，也会在此处显示相应的错误信息，函数终止，表单不会被提交。

如果所有标准都满足，则表单被提交。

### 注意

本书可下载资料（位于 [`www.rheinwerk-computing.com/5875`](http://www.rheinwerk-computing.com/5875)）中的补充章节 2 介绍了 `regexp` 对象。它还提供了使用正则表达式处理字符串的其他选项。

### 6.2.6 Unicode 字符

Unicode 字符集包含来自许多不同语言和字符系统的大量符号和字符。自 ECMAScript 2024 起，你可以确保 Unicode 字符是格式良好的（即在浏览器中统一且正确地显示）。

Unicode 字符的代码在字符串中由两部分组成。每部分由字符组合 `\u` 和四个十六进制数字组成。

此外，你可以使用 `isWellFormed()` 字符串方法来检查一个字符串是否对应于一个格式良好的 Unicode 字符代码。

在以下程序中，显示了一些表情符号领域的字符，然后进行了一些测试：

```html
...

<body>
  <p>
    <script>
```

```javascript
document.write("\uD83D\uDE00" + "\uD83D\uDE0F" + "<br>");

document.write("\uD83D\uDE10" + "\uD83D\uDE1F" + "<br>");

document.write("\uD83D\uDE20" + "\uD83D\uDE2F" + "<br>");

document.write("\uD83D\uDE30" + "\uD83D\uDE3F" + "<br>");

document.write("\uD83D\uDE40" + "\uD83D\uDE4F" + "<br>");

document.write("Hello".isWellFormed() + "<br>");

document.write("\uDE00".isWellFormed() + "<br>");

document.write("\uD83D\uDE00".isWellFormed() + "<br>");
```

```html
</script>
</p>

</body>
</html>
```

**清单 6.26**　`character_unicode.htm` 文件

你可以在图 6.24 中看到程序的结果。

![Unicode 字符](img/img-f6.24.html)

**图 6.24**　Unicode 字符

## 6.3 数字与数学

预定义的 `Math` 和 `Number` 对象让你能更轻松地处理数字和数学计算。在本节中，我们将介绍许多你在计算器中熟悉的函数，同时还会学习简单的随机数生成器以及适用于加密的随机数生成器。

### 6.3.1 `Math` 对象

`Math` 对象允许你使用一系列有用的数学方法，并且还提供了一些数学常量作为属性。

首先来看示例程序：

```html
...

<body>
  <p>
    <script>
      const a = 4.75,
        b = -4.75;

      let output =
        "a:" +
        a +
        " b:" +
        b +
        "<br>" +
        "ceil(a):" +
        Math.ceil(a) +
        " &nbsp; ceil(b):" +
        Math.ceil(b) +
        "<br>" +
        "floor(a):" +
        Math.floor(a) +
        " &nbsp; floor(b):" +
        Math.floor(b) +
        "<br>" +
        "round(a):" +
        Math.round(a) +
        " &nbsp; round(b):" +
        Math.round(b) +
        "<br>" +
        "abs(a):" +
        Math.abs(a) +
        " &nbsp; abs(b):" +
        Math.abs(b) +
        "<br>" +
        "sign(a):" +
        Math.sign(a) +
        " &nbsp; sign(b):" +
        Math.sign(b) +
        " &nbsp; sign(0):" +
        Math.sign(0) +
        "<br>" +
        "max(a,b):" +
        Math.max(a, b) +
        " &nbsp; min(a,b):" +
        Math.min(a, b) +
        "<br><br>";

      const c = 64;

      output +=
        "c:" +
        c +
        " &nbsp; sqrt(c):" +
        Math.sqrt(c) +
        " &nbsp; cbrt(c):" +
        Math.cbrt(c) +
        "<br>" +
        "pi:" +
        Math.PI +
        " &nbsp; e:" +
        Math.E +
        "<br>" +
        "exp(4.6):" +
        Math.exp(4.6) +
        " &nbsp; log(100):" +
        Math.log(100) +
        "<br>" +
        "pow(10,3):" +
        Math.pow(10, 3) +
        " &nbsp; log10(1000):" +
        Math.log10(1000);

      document.write(output);
    </script>
  </p>
</body>

</html>
```

**清单 6.27**　`number_math.htm` 文件

首先，使用 `ceil()`、`floor()` 和 `round()` 取整方法将一个正数和一个负数取整为整数。`ceil()` 方法将数字向上取整为下一个最大的整数，`floor()` 方法将数字向下取整为下一个最小的整数。

`round()` 方法按照商业惯例将数字四舍五入为整数。例如，对于正数，3.000 到 3.499 变为 3，3.500 到 3.999 变为 4。对于负数，–3.000 到 –3.499 变为 –3，–3.500 到 –3.999 变为 –4。

`abs()` 方法计算数字的绝对值（即不带符号的数字）。`sign()` 方法自 ECMAScript 2015 起可用，它确定数字的符号，对于正数返回 1，负数返回 –1，数字 0 返回 0。`max()` 和 `min()` 方法返回任意给定数字集合中的最大值或最小值。

`sqrt()` 方法计算数字的平方根，而 `cbrt()` 方法计算立方根。`PI` 和 `E` 属性包含数学常量 Pi（π）或欧拉数 e（即指数函数的底数）。

`exp()` 方法计算指数函数的结果（即 e 的幂）。这里，该方法计算 e 的 4.6 次方，结果约为 100。`log()` 方法计算数字的自然对数（即以 e 为底的对数），数学上称为 ln。这对应于 `exp()` 方法的逆运算。在示例中，该方法计算 100 的自然对数（ln 100），结果约为 4.6。

`pow()` 方法计算幂函数的结果（即 x 的 y 次方）。这里，该方法计算 10 的 3 次方，结果为 1,000。`log10()` 方法自 ECMAScript 2015 起可用，它计算数字以 10 为底的对数。这里，该方法计算 1,000 的对数，结果为 3。

你可以在图 6.25 中看到程序的结果。

![Math 对象、方法和属性](img/img-f6.25.html)

**图 6.25**　Math 对象、方法和属性

### 6.3.2 三角函数

以下程序用于显示一个表格，其中包含角度从 0 到 90 度（步长为 15 度）的正弦、余弦和正切三角函数值。

`Math` 对象的 `sin()`、`cos()` 和 `tan()` 方法基于弧度角度计算值。一个完整圆的 360 度对应 2π 弧度，因此角度必须使用因子 π/180 转换为弧度。

以下是相应的示例程序：

```html
...

<body>
  <table>
    <tr>
      <td style="font-weight:bold;">Angle</td>
      <td style="font-weight:bold;">Radian</td>
      <td style="font-weight:bold;">Math.sin()</td>
      <td style="font-weight:bold;">Math.cos()</td>
      <td style="font-weight:bold;">Math.tan()</td>
    </tr>

    <script>
      for (let i = 0; i <= 90; i += 15) {
        const rad = (i / 180) * Math.PI;

        document.write(
          "<tr><td>" +
            i +
            "</td><td>" +
            rad.toFixed(3) +
            "</td><td>" +
            Math.sin(rad).toFixed(3) +
            "</td><td>" +
            Math.cos(rad).toFixed(3) +
            "</td><td>" +
            Math.tan(rad).toFixed(3) +
            "</td></tr>"
        );
      }
    </script>
  </table>
</body>

</html>
```



**清单 6.28**　`number_math_angle.htm` 文件

第一步是转换为弧度。结果使用 `Number` 对象的 `toFixed()` 方法四舍五入到三位小数，但遗憾的是，90 度（= `π/2`）到弧度的转换在数学上并不精确，因此 90 度的正切值并非无穷大。

程序的输出如图 6.26 所示。

![三角函数表](img/img-f6.26.html)

**图 6.26**　　三角函数表

### 6.3.3　随机生成器与类型化数组

`Math` 对象的 `random()` 方法在本书中已多次用于生成简单的随机数。这里，它被用来模拟掷骰子十次。

`crypto` 对象用于生成更优质的随机数，这些随机数也可用于加密目的。`crypto` 对象的 `getRandomValues()` 方法会用随机数填充一个类型化数组。什么是类型化数组？默认情况下，JavaScript 中的变量没有数据类型，可以存储任何值（例如整数、小数、字符串、布尔值）。此外，对于存储数字，需要提供固定大小的存储区域的需求日益增长。类型化数组正是为此而创建的。

在下面的程序中，一个大小为 10 的 `Uint32Array` 类型的类型化数组被填充了随机数：

```html
...

<body><p>

   <script>
```

```javascript
let output = "random(): ";

for(let i=0; i<10; i++)
   output += Math.floor(Math.random() * 6 + 1) + " ";

output += "<br><br>crypto():";

const za = new Uint32Array(10);

crypto.getRandomValues(za);

za.sort();

for(let i=0; i<za.length; i++)
   output += "<br>" + za[i];

document.write(output);
```

```html
   </script></p>

</body></html>
```

**清单 6.29**　`number_random.htm` 文件

`Math.random()` 方法返回一个介于 0 和 1 之间的随机数，不包括上限 1。乘以 6 后得到介于 0 和 6 之间的值，不包括 6。加 1 后得到介于 1 和 7 之间的值，不包括 7。最后，`floor()` 方法向下取整到最接近的整数（即得到 1 到 6 之间的值）。

`za` 变量引用了一个 `Uint32Array` 类型的数组，该数组的引用作为参数传递给 `crypto` 对象的 `getRandomValues()` 方法。类型化数组在该方法中被填充，然后为了更清晰地展示而进行排序。类型化数组的 `sort()` 方法按数值对数组进行排序，之后显示该数组。

例如，程序的输出可能如图 6.27 所示。

![随机数生成器与类型化数组](img/img-f6.27.html)

**图 6.27**　　随机数生成器与类型化数组

类型化数组有多种类型，既包括整数类型，也包括小数类型。这里只介绍 `Int32Array` 和 `Uint32Array` 类型。使用这些类型，可以在大小为 32 位 = 4 字节的存储区域中存储整数。

`Int32Array` 的一个元素中可以存储从 –2,147,483,648 到 +2,147,483,647 的数字。`U` 代表无符号，`Uint32Array` 的一个元素中只能存储从 0 到 +4,294,967,295 的正数。

### 6.3.4　整数

`Number` 对象提供了与 JavaScript 中数字范围和精度相关的属性和方法。此外，我还介绍了用于超大整数的 `BigInt` 对象。下面是一个示例程序：

```html
...

<body><p>

   <script>
```

```javascript
let nu = Number.MAX_SAFE_INTEGER;

document.write("最大安全整数: " + nu + "<br>");

document.write("安全整数: "
   + Number.isSafeInteger(nu) + "<br>");

nu = nu + 1;

document.write("+1: 安全整数: "
   + Number.isSafeInteger(nu) + "<br>");

nu = Number.MIN_SAFE_INTEGER;

document.write("最小安全整数: " + nu + "<br><br>");

nu = Number.MAX_SAFE_INTEGER;

x = nu + 1;

y = nu + 2;

document.write("不使用 BigInt 时的错误:<br>" + x + "<br>" + y + "<br><br>");

const numberBig = BigInt(nu);

x = numberBig + 1n;

y = numberBig + 2n;

document.write("使用 BigInt 时无错误:<br>" + x + "<br>" + y);
```

```html
   </script></p>

</body></html>
```

**清单 6.30**　`number_integer.htm` 文件

ECMAScript 2015 引入了 `Number` 对象的 `MAX_SAFE_INTEGER` 和 `MIN_SAFE_INTEGER` 属性。它们分别对应最大和最小安全整数。只有安全整数才能在 JavaScript 中用于数学精确计算。大于 `MAX_SAFE_INTEGER` 或小于 `MIN_SAFE_INTEGER` 的数字会以小数形式存储。整数的存储和比较只有在安全整数范围内才是数学精确的，你可以使用 `isSafeInteger()` 方法来检查某个数字是否为安全整数。

然而，自 ECMAScript 2020 起，有了另一种选择。`BigInt` 对象可以处理更大的整数，通过附加字符 `n` 或调用 `BigInt()` 函数可以生成 `BigInt` 类型的数字。在这个程序中，你可以看到两个大于 `MAX_SAFE_INTEGER` 的不同整数只有作为 `BigInt` 值才能被正确区分。

程序的结果如图 6.28 所示。

![整数](img/img-f6.28.html)

**图 6.28**　　整数

### 6.3.5　小数

本节介绍 `Number` 对象用于小数的属性和方法，并介绍针对这类数字的类型化数组。

首先来看一个示例程序：

```html
...

<body><p>

   <script>
```

```javascript
let nu = 1000 / 7;

document.write("数字: " + nu + "<br>");

document.write("显示 0 位小数: "
   + nu.toFixed(0) + "<br>");

document.write("显示 2 位小数: "
   + nu.toFixed(2) + "<br>");

document.write("指数形式: "
   + nu.toExponential() + "<br><br>");

nu = Number.MAX_VALUE;

document.write("最大值数字: " + nu + "<br>");

nu = nu * 10;

document.write("放大后: " + nu + "<br>");

nu = Number.MIN_VALUE;

document.write("最小值数字: " + nu + "<br>");

nu = nu / 10;

document.write("缩小后: " + nu + "<br><br>");

nu = Number.EPSILON;

document.write("&epsilon; = 最小距离: " + nu + "<br>");

nu = 1 + Number.EPSILON;

document.write("1 + &epsilon;: " + nu.toFixed(40) + "<br>");

nu = 1 + Number.EPSILON / 2;

document.write("1+ &epsilon;/2: " + nu.toFixed(40) + "<br><br>");

let ar = new Float32Array(2);

ar[0] = 1000 / 7;

document.write("Float32: " + ar[0].toFixed(20) + "<br>");

ar = new Float64Array(2);

ar[0] = 1000 / 7;

document.write("Float64: " + ar[0].toFixed(20) + "<br>");
```

```html
   </script></p>

</body></html>
```

**清单 6.31**　`number_point.htm` 文件

该程序计算 `1000 / 7` 的值，结果为 142.857142857142...。在标准 JavaScript 变量中，数字只能存储 14 到 15 位小数，因此结果变为 142.85714285714286。

`Number` 对象的 `toFixed()` 方法返回一个字符串，其中包含一个四舍五入到指定小数位数的数字。数字本身在此上下文中不会改变。参数为 0 时，返回的字符串包含一个整数；参数为 2 时，数字四舍五入到两位小数。

`Number` 对象的 `toExponential()` 方法将数字输出为带有底数和指数的指数形式。此处显示的数字读作：`1.42857... 乘以 10 的 2 次方`。

这两种方法都直接应用于变量，无需指定 `Number` 对象。

`MAX_VALUE` 属性对应 JavaScript 可处理的最大数值。如果增加该值，将得到无穷大。

另一方面，`MIN_VALUE` 属性对应 JavaScript 可处理的最小数值。如果减小该值，结果为 0。

`EPSILON` 属性是在 ECMAScript 2015 中引入的，它表示 1 与大于 1 的最小带小数位数数字之间的差值。

### 注意

术语 epsilon 在数学中用于描述两个值之间可能的最小距离。在 JavaScript 中，无法检测到更小的距离。

在 `Float32Array` 或 `Float64Array` 类型的类型化数组中（另请参见第 6.3.3 节），带小数位的数字存储在大小为 32 位 = 4 字节或 64 位 = 8 字节的内存区域中。前者提供 6 到 7 位小数的精度，后者提供 14 到 15 位小数的精度。

你可以在图 6.29 中看到程序的结果。

![带小数位的数字](img/img-f6.29.html)

**图 6.29**　　带小数位的数字

### 6.3.6　数字的自定义扩展

在本节中，我们将扩展数字输出的选项。为此，我们通过自定义的 `format()` 方法扩展 `Number` 对象，并用它来用前导字符填充数字以进行输出。

你可以使用一个或两个参数调用该方法。第一个参数表示输出中所需的总位数，第二个参数可以传递一个字符串，作为填充字符。如果没有第二个参数，则用零填充。

该方法定义在名为 `number.js` 的外部文件中。你可以用其他有用的数字方法填充此文件，集成该文件后，即可使用这些方法。

以下是使用外部文件中方法的程序：

```html
... <head> ...

   <script src="number.js"></script>

</head>

<body>

   <script>
```

```javascript
const x = 15;

document.write(x.format(5) + "<br>");

document.write(x.format(5, "#"));
```

```html
   </script>

</body></html>
```

**清单 6.32**　`number_extend.htm` 文件

程序分配了一个两位数字。输出时，它被填充到五位。第一次输出使用字符 `0` 填充；第二次输出使用井号字符 `#`。

你可以在图 6.30 中看到输出。

![自定义 format() 方法](img/img-f6.30.html)

**图 6.30**　　自定义 `format()` 方法

接下来是定义 `format()` 方法的外部文件：

```javascript
Number.prototype.format = function(number_of_digits, character = "0")
{
   let formatted = this.toString();

   while(formatted.length < number_of_digits)
      formatted = character + formatted;

   return formatted;
}
```

**清单 6.33**　`number.js` 文件

JavaScript 中的对象具有 `prototype` 属性。在 JavaScript 面向对象编程的经典表示法中，此属性代表对象的原型，并允许你扩展所有具有相同原型的对象。在此程序中，我们为 `Number` 对象使用此属性。

将一个匿名函数赋值给 `Number.prototype` 对象的 `format` 属性，这使 `format()` 成为一个方法。

你可以传递一个或两个参数。第一个参数指定所需的位数，第二个参数对应填充字符，默认值为字符 `0`。调用时，可以将不同的填充字符作为第二个参数传递。

你可以通过 `this` 访问调用该方法的 `Number` 对象。对象的内容（即数字）使用 `toString()` 方法转换为字符串。

只要此字符串的长度小于所需位数，就会在开头添加填充字符。然后返回填充后的字符串。

## 6.4　使用时间规格

`Date` 对象提供了多种计算和输出日期与时间信息的选项。

`Date` 对象的原点为 1970 年 1 月 1 日 00:00 格林威治标准时间（GMT），尽管今天我们使用协调世界时（UTC）。`Date` 对象在该时间点之前为负值，之后为正值。时间以毫秒计算。

### 6.4.1　创建时间数据

在本节中，你将看到创建新 `Date` 对象的多种选项：

- 无参数时，创建一个包含 PC 系统时间（即当前日期和时间）的 `Date` 对象。
- 一个参数时，该值被视为自原点（1970 年 1 月 1 日 00:00）以来的毫秒数。
- 三个参数时，值分别为年、月、日。
- 六个参数时，值分别为年、月、日、时、分、秒。

月份的编号从 0 开始，因此值范围为 0（一月）到 11（十二月）。如果输入的值过大或过小，会自动转换（例如，1 月 32 日变为 2 月 1 日）。

以下是程序：

```html
...

<body><p>

   <script>
```

```javascript
const timeA = new Date();

document.write("当前日期: " + timeA + "<br>");

const timeB = new Date(2024, 6, 10);

document.write("由日、月、年创建的日期: " + timeB + "<br>");

const timeC = new Date(2024, 6, 10, 17, 8, 3);

document.write("额外包含时、分、秒: " + timeC + "<br>");

const timeD = new Date(2024, 1, 30, 17, 68, -3);

document.write("由转换值创建的日期: " + timeD + "<br>");

const timeE = new Date(2 * 60 * 1000);

document.write("由毫秒创建的日期: " + timeE + "<br>");

const timeF = new Date(-1.5 * 24 * 60 * 60 * 1000);

document.write("负值: " + timeF);
```

```html
   </script></p>

</body></html>
```



**清单 6.34**　time_create.htm 文件

结果如图 6.31 所示。

![创建时间数据](img/img-f6.31.html)

**图 6.31**　创建时间数据

创建的 `Date` 对象以默认格式输出，其中包含星期和月份的英文缩写名称，以及日期、年份和时间。更多输出选项请参见第 6.4.2 节。

`GMT+0100` 表示本地时间比格林威治时间早一小时，这是由于与伦敦-格林威治之间存在一小时的时差。如果因夏令时而再增加一小时时差，则会显示 `GMT+0200`。同时还会显示中欧标准时间（`CET`）和中欧夏令时间（`CEST`）的名称。

其他时间规格是通过传递的值生成的。输入 2024、6、10 会变成 2024 年 7 月 10 日，时间设置为 00:00:00 或 17:08:03。

以下是一些需要转换的值：2024 年 2 月 30 日变成 2024 年 3 月 1 日，17:68 变成 18:08。如果减去 3 秒，则变成 18:07:57。

值 `2 × 60 × 1,000` 毫秒对应从原点起两分钟的差值。结果是 1970 年 1 月 1 日 00:02 GMT，由于时差，对应 `CET` 的 01:02。

负值 `–1.5 × 24 × 60 × 60 × 1,000` 对应 1.5 天的差值，结果是 1969 年 12 月 30 日 12:00 GMT。由于时差，对应 `CET` 的 13:00。

### 6.4.2 输出时间数据

在本节中，你将了解输出 `Date` 对象的各种选项。我将以当前时间段为例进行说明：

* 你已经知道不使用方法的对象输出方式。
* `toLocaleString()` 方法生成特定于国家/地区的信息，这些信息来自当前使用的浏览器信息。
* `toUTCString()` 方法生成 UTC 时间。增加一小时后，结果即为 `CET`。
* `getTimezoneOffset()` 方法返回本地时间相对于 UTC 的时间偏移量（以分钟为单位）。例如，南澳大利亚州的时差为 9.5 小时。
* `dateFormat()` 方法是 `Date` 对象的自定义扩展，用于格式化输出时间。内部使用了多个预定义方法（第 6.4.3 节）。

调用 `dateFormat()` 方法时，可以传递一个包含格式说明的字符串，该字符串提供以下信息：

* `w`：星期几
* `d`：月份中的日期，两位数
* `M`：月份编号，两位数
* `y`：年份，四位数
* `h`：小时，两位数
* `m`：分钟，两位数
* `s`：秒，两位数
* `i`：毫秒

两位数的值在必要时会输出前导零。其他字符，如 `:`（冒号）或 `.`（点），不会被转换，而是直接输出在相应位置。

以下是程序代码：

```html
... <head> ...

   <script src="number.js"></script>

   <script src="date.js"></script>

</head>

<body><p>

   <script>
```

```javascript
const time = new Date();

      const output = "Time object: " + time + "<br>"
         + "Local format: " + time.toLocaleString() + "<br>"
         + "UTC format: " + time.toUTCString() + "<br>"
         + "Local offset from UTC: "
         + (time.getTimezoneOffset()/60) + " hour(s)<br>"
         + "Default format: " + time.dateFormat("M/d/y h:m:s") + "<br>"
         + "With weekday: " + time.dateFormat("w, M/d/y") + "<br>"
         + "With milliseconds: " + time.dateFormat("h:m:s,i") + "<br>";

      document.write(output);
```

```html
</script></p>

</body></html>
```

**清单 6.35**　time_output.htm 文件

集成了两个扩展：首先是来自 `number.js` 文件的 `Number` 对象扩展（第 6.3.5 节），其次是来自 `date.js` 文件的 `Date` 对象扩展（第 6.4.3 节）。在内部，`dateFormat()` 方法使用 `number.js` 文件中的 `format()` 方法来输出前导零。

当你使用 `toLocaleString()` 和 `toUTCString()` 方法时，还会列出星期几和月份的名称。`toUTCString()` 方法以 UTC 格式指定时间。

`getTimezoneOffset()` 方法返回以分钟为单位的指示，此处将其转换为小时。接下来是三个不同的输出示例，作为 `dateFormat()` 的演示。

结果如图 6.32 所示。

![输出时间数据](img/img-f6.32.html)

**图 6.32**　输出时间数据

### 6.4.3 Date 对象的扩展

独立的 `dateFormat()` 方法用于扩展 `Date` 对象，提供了一种便捷的方式来输出不同的时间规格。

首先，这是代码：

```javascript
Date.prototype.dateFormat = function(formatcharacter)

{

   const wday = ["Sunday", "Monday", "Tuesday",

      "Wednesday", "Thursday", "Friday", "Saturday"];

   let output = "";

   for(let i=0; i<formatcharacter.length; i++)

      switch(formatcharacter[i])

      {

          case "w": output += wday[this.getDay()];           break;

          case "d": output += this.getDate().format(2);      break;

          case "M": output += (this.getMonth()+1).format(2); break;

          case "y": output += this.getFullYear();            break;

          case "h": output += this.getHours().format(2);     break;

          case "m": output += this.getMinutes().format(2);   break;

          case "s": output += this.getSeconds().format(2);   break;

          case "i": output += this.getMilliseconds();        break;

          default:  output += formatcharacter[i];

      }

    return output;

}
```

**清单 6.36**　date.js 文件

将一个匿名函数赋值给 `Date.prototype` 对象的 `dateFormat` 属性，从而将 `dateFormat()` 变为一个方法。你传递一个包含所需格式细节的字符串作为参数，该字符串在 `for` 循环中逐字符处理，以组装并返回格式化后的时间规格。

在准备阶段，创建了一个包含星期几全称的数组。`Date` 对象的 `getDay()` 方法返回星期几的数字：值 0 代表星期日，值 1 代表星期一，依此类推，直到值 6 代表星期六。这些值用作数组的索引。

你可以通过 `this` 访问调用该方法的 `Date` 对象。在 `for` 循环中，每个字符通过 `switch` 分支进行检查。不同的格式字符会调用 `Date` 对象的不同方法：`getDay()`、`getDate()`、`getMonth()`、`getFullYear()`、`getHours()`、`getMinutes()`、`getSeconds()` 和 `getMilliseconds()`。有几个特殊之处需要注意：

* `getMonth()` 方法返回的值介于 0 到 11 之间，因此输出时必须加 1。
* 对于某些值，会调用 `Number` 对象的 `format()` 方法来输出前导零。

如果某个字符与任何格式字符都不匹配，它会直接添加到格式化后的时间字符串中，无需进一步转换。例如，冒号、点号或空格就属于这种情况。

### 6.4.4 使用时间数据进行计算

你也可以使用 `Date` 对象来相互偏移时间。下面的程序包含四个示例：

* 计算两个时间之间的时间差
* 计算程序段的运行时长
* 计算一个人的年龄
* 使用 `Date` 对象的自定义 `dateAdd()` 方法将时间差添加到时间规范中

最后一个方法定义在外部 `date.js` 文件中，就像独立的 `dateFormat()` 方法一样。

以下是程序的第一部分：

```html
... <head> ...

   <script src="number.js"></script>

   <script src="date.js"></script>

</head>

<body><p>

   <script>
```

```javascript
let timeA = new Date(2024, 6, 15, 23, 59, 20);

      let timeB = new Date(2024, 6, 16, 0, 1, 50);

      document.write("1: " + timeA.dateFormat("M/d/y h:m:s") + "<br>");

      document.write("2: " + timeB.dateFormat("M/d/y h:m:s") + "<br>");

      let difference = timeB - timeA;

      document.write("Difference in minutes: "
         + (difference / 60000) + "<br><br>");

...
```

**清单 6.37**　time_compute.htm 文件，第 1 部分，共 4 部分

创建了两个 `Date` 对象，每个都带有预定义的日期和时间数据。要计算它们之间的日期和时间差，只需将一个减去另一个即可。`Date` 对象中的时间规范在内部存储为自原点（即 1970 年 1 月 1 日 00:00）以来的毫秒数。因此，差值也是一个数字。要将其表示为分钟，请除以 60,000。

结果显示在图 6.33 中。

![计算时间差](img/img-f6.33.html)

**图 6.33**　计算时间差

以下是程序的第二部分：

```javascript
...

      const msecA = new Date();

      let a = 1;

      for(let i=0; i<5e7; i++)

         a = a * -1;

      const msecB = new Date();

      difference = msecB - msecA;

       document.write("Computing time in milliseconds: "
         + difference + "<br><br>");

...
```

**清单 6.38**　time_compute.htm 文件，第 2 部分，共 4 部分

程序两次查询当前系统时间，一次在程序段之前，一次在之后。通过这种方式，程序计算计算机处理一个程序段所需的时间，该程序段中 `for` 循环运行得非常频繁。时间长短取决于计算机的性能和当前利用率。

你也可以在图 6.33 中看到这个结果。

现在来看程序的第三部分：

```javascript
...

      timeA = new Date(1979, 7, 16);

      timeB = new Date();

      difference = timeB.getFullYear() - timeA.getFullYear();

       if(( timeB.getMonth() < timeA.getMonth() )

            || ( timeB.getMonth() == timeA.getMonth()

            && timeB.getDate() < timeA.getDate() ) )

         difference--;

      document.write("1: " + timeA.dateFormat("M/d/y") + "<br>");

      document.write("2: " + timeB.dateFormat("M/d/y") + "<br>");

      document.write("Age: " + difference + "<br><br>");

...
```

**清单 6.39**　time_compute.htm 文件，第 3 部分，共 4 部分

程序生成两个时间规范，一个包含出生日期，另一个包含当前系统时间。它按如下方式计算年龄：一个人的年龄最初等于两个时间之间的年份差。然后程序比较两个时间的月份，如果出生月份尚未到达，或者当前月份是出生月份但生日尚未到达，则程序减去 1。

### 注意

链接条件中的括号并非必需，仅用于澄清。逻辑与运算符的优先级高于逻辑或运算符。

结果显示在图 6.34 中。

![计算年龄并添加时间规范](img/img-f6.34.html)

**图 6.34**　计算年龄并添加时间规范

程序的第四部分也是最后一部分如下：

```javascript
...

      timeA = new Date(2024, 6, 31, 17, 55, 30);

      timeB = timeA.dateAdd(0, 0, 3, 6, 10, 0);

      document.write("1: " + timeA.dateFormat("M/d/y h:m:s") + "<br>");

      document.write("3 days, 6 hours and 10 minutes later:<br>");

      document.write("2: " + timeB.dateFormat("M/d/y h:m:s"));
```

```html
</script></p>

</body></html>
```

**清单 6.40**　time_compute.htm 文件，第 4 部分，共 4 部分

首先，程序生成一个单独的时间条目，然后使用 `dateAdd()` 方法创建第二个 `Date` 对象。这是 `Date` 对象的另一个自定义扩展。内部使用了许多预定义的方法（第 6.4.5 节）。

调用时，你可以传递一个包含六个部分值的时间值，这些值将被添加或减去。这六个部分值依次代表年、月、日、时、分、秒。

你也可以在图 6.34 中看到这个结果。

### 6.4.5 Date 对象的第二个扩展

自定义的 `dateAdd()` 方法用于扩展 `Date` 对象，提供了将时间值添加或减去现有时间的功能。

首先，代码如下：

```javascript
Date.prototype.dateAdd = function(year, month, day, hour, minute, second)

{

   const time = new Date();

   time.setFullYear(this.getFullYear() + year);

   time.setMonth(this.getMonth() + month);

   time.setDate(this.getDate() + day);

   time.setHours(this.getHours() + hour);

   time.setMinutes(this.getMinutes() + minute);

   time.setSeconds(this.getSeconds() + second);

   return time;

}
```



**清单 6.41**　`date.js` 文件，扩展

该程序将一个匿名函数赋值给 `Date.prototype` 对象的 `dateAdd` 属性。这使得 `dateAdd()` 成为一个方法，并将时间值的六个部分值作为参数传递。你可以通过 `this` 访问调用该方法的当前 `Date` 对象。

同时还会创建一个新的 `Date` 对象（`time`），并返回对该对象的引用作为计算结果。总共调用了六个预定义的 `set` 方法来计算新对象的各个部分值，计算每个部分值时，将对应的参数加到当前对象的对应部分值上。如果部分值过大或过小，它们会被相应转换。例如，对于像 –10 分钟或 +50 天这样的输入，就会进行转换。

### 注意

你可以在本书的可下载材料中找到 `u_time_estimate` 练习，位于附加章节 1 的第 1.17 节，下载地址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

## 6.5　时间控制过程

你已经熟悉了 `window` 对象的 `alert()`、`prompt()` 和 `confirm()` 方法。`window` 对象还有以下其他方法，可以让你控制时间过程，例如在游戏或模拟中所需的那样：

* `setTimeout()` 方法，确保语句在指定时间后调用一次。
* `setInterval()` 方法，确保语句在指定时间后按计划重复调用。

### 6.5.1　启动时间控制过程

在下面的程序中，使用 `setTimeout()` 和 `setInterval()` 方法来显示带有日期和时间的当前时间规格：

```html
... <head> ...

   <script src="number.js"></script>

   <script src="date.js"></script>

   <script>
```

```javascript
function intervalDateTime()
{
   const d = new Date();
   document.getElementById("idInterval").firstChild.nodeValue =
      "With Interval: " + d.dateFormat("M/d/y h:m:s");
}

function timeoutDateTime()
{
   const d = new Date();
   document.getElementById("idTimeout").firstChild.nodeValue =
      "With Timeout: " + d.dateFormat("M/d/y h:m:s");
   setTimeout(timeoutDateTime, 100);
}
```

```html
</script>
</head>

<body>

   <p id="idInterval">With Interval:</p>
   <p id="idTimeout">With Timeout:</p>
   <script>
```

```javascript
setInterval(intervalDateTime, 100);
setTimeout(timeoutDateTime, 100);
```

```html
</script>
</body></html>
```

**清单 6.42**　`process_digital_clock.htm` 文件

`setInterval()` 方法在下面的 `script` 容器中被调用。该方法的参数是一个函数引用和一个以毫秒为单位的持续时间。

从调用 `setInterval()` 方法开始，`intervalDateTime()` 函数每 100 毫秒重复运行一次。函数中创建了一个包含当前时间的 `Date` 对象，并将该时间规格格式化到文档的第一个段落中。

此外，`setTimeout()` 方法也在下面的 `script` 容器中被调用，参数相同。

通过这次 `setTimeout()` 方法的调用，`timeoutDateTime()` 函数在 100 毫秒后运行一次，并在函数中生成并格式化当前时间。然后再次调用 `setTimeout()` 方法，这样该方法每 100 毫秒自我调用一次。如果没有这次新的调用，过程将在此时结束。

图 6.35 显示了该程序的输出。

![setInterval() 和 setTimeout() 方法](img/img-f6.35.html)

**图 6.35**　`setInterval()` 和 `setTimeout()` 方法

### 6.5.2　启动和结束时间控制过程

`window` 对象的 `clearInterval()` 方法用于结束由 `setInterval()` 方法启动的时间控制过程。在下面的程序中，一个 10 秒的倒计时运行并停在 0 处。

程序如下：

```html
... <head> ...

   <script>
```

```javascript
function countdown()
{
   const timeB = new Date();
   const difference = (timeB - timeA) / 1000;
   const countdownNumber = 10 - difference;

   document.getElementById("idCountdown").firstChild.nodeValue =
      "Countdown: " + countdownNumber.toFixed(1);

   if(countdownNumber < 0.06)
   {
      clearInterval(intervalReference);
      document.getElementById("idCountdown")
         .firstChild.nodeValue = "Countdown: End";
   }
}
```

```html
</script>
</head>

<body>

   <p id="idCountdown">Countdown:</p>
   <script>
```

```javascript
const timeA = new Date();
const intervalReference = setInterval(countdown, 100);
```

```html
</script>
</body></html>
```

**清单 6.43**　`process_countdown.htm` 文件

首先，将过程启动的时间保存在 `timeA` 变量中，然后调用 `setInterval()` 方法。后者还有一个返回值，引用该过程，并将该引用保存在一个变量中。

`countdown()` 函数计算从启动开始的时间差（以秒为单位），然后计算并输出剩余时间。如果剩余时间小于 0.06 秒，则调用 `clearInterval()` 方法结束过程。使用保存的 `setInterval()` 方法的引用作为参数。

程序的输出如图 6.36 所示。

![倒计时，clearInterval() 方法](img/img-f6.36.html)

**图 6.36**　倒计时，`clearInterval()` 方法

### 注意

你也可以启动多个独立的过程，并且由于每个过程都有独立的引用，因此可以单独控制每个过程。

### 6.5.3　控制过程

时间控制过程通常由事件启动，例如点击按钮。在大多数情况下，你不希望过程在其活动运行期间被重新启动，而只希望在它结束后才能重新启动。你还希望能够暂停过程，然后恢复它。

下面的程序有三个按钮：

* 当点击“开始”按钮时，过程启动，并且在活动运行期间忽略对该按钮的其他点击。
* 一旦点击“暂停”按钮，过程停止，当点击“开始”按钮时恢复运行。
* 点击“停止”按钮结束过程，无论它当前是活动还是暂停状态。

程序如下：

```html
... <head> ...

   <script>
```

```javascript
let intervalReference, intervalActive = false;

function output()
{
   document.getElementById("idOutput").firstChild.nodeValue += "x";
}

function start()
{
   if(intervalActive)
      return;

   intervalActive = true;
   intervalReference = setInterval(output, 500);
}

function pause()
{
   intervalActive = false;
   clearInterval(intervalReference);
}

function stop()
{
   intervalActive = false;
   clearInterval(intervalReference);
   document.getElementById("idOutput").firstChild.nodeValue = "Output: ";
}
```

```html
</script>
</head>

<body>

   <p>
      <input id="idStart" type="button" value="Start">
      <input id="idPause" type="button" value="Pause">
      <input id="idStop" type="button" value="Stop">
      <span id="idOutput">Output: </span>
   </p>

   <script>
```

```javascript
document.getElementById("idStart").addEventListener("click", start);
document.getElementById("idPause").addEventListener("click", pause);
document.getElementById("idStop").addEventListener("click", stop);
```

```html
</script>
</body></html>
```

**清单 6.44**　`process_control.htm` 文件

`intervalReference` 变量包含对进程的引用，可通过此引用终止进程；`intervalActive` 变量包含进程是否处于活动状态的信息。

在活动运行期间，每 0.5 秒会在现有输出后追加一个 `x` 字符。如果在活动运行期间激活 `start()` 函数，该函数会立即中止。

`pause()` 函数会保留现有输出。而 `stop()` 函数则会将其重置为初始状态。

图 6.37 展示了该程序的输出。

![控制进程](img/img-f6.37.html)

**图 6.37**　控制进程

### 6.5.4　幻灯片与单张图片

借助时间控制进程以及不同图片之间的切换，可以以单张图片模式或幻灯片模式显示图片，如图 6.38 所示。

![幻灯片与单张图片](img/img-f6.38.html)

**图 6.38**　幻灯片与单张图片

您可以点击 `<<`、`<`、`>` 或 `>>` 按钮，分别立即显示下一张、上一张、第一张或最后一张图片。同时会显示当前图片的编号和图片总数。您还可以使用“开始幻灯片”和“结束幻灯片”按钮来启动和停止幻灯片。

首先来看程序的下半部分：

```html
...

<body>

   <p><img id="idImage" src="im_paradise.jpg" alt="Paradise"></p>

   <p>
      <input id="idFirst" type="button" value="&lt;&lt;">
      <input id="idBack" type="button" value="&lt;">
      <input id="idNext" type="button" value="&gt;">
      <input id="idLast" type="button" value="&gt;&gt;">

   <script>
```

```javascript
document.write("<span id='idOutput'>1/" + image.length + "</span></p>");
```

```html
</script>

   <p>
      <input id="idStart" type="button" value="Start slideshow">
      <input id="idStop" type="button" value="End slideshow">
   </p>

   <script>
```

```javascript
document.getElementById("idFirst").addEventListener
   ("click", function() { move(0); });

document.getElementById("idBack").addEventListener
   ("click", function() { move(imageIndex - 1); });

document.getElementById("idNext").addEventListener
   ("click", function() { move(imageIndex + 1); });

document.getElementById("idLast").addEventListener
   ("click", function() { move(image.length - 1); });

document.getElementById("idStart").addEventListener("click", start);
document.getElementById("idStop").addEventListener("click", stop);
```

```html
</script>
</body></html>
```

**清单 6.45**　`process_slideshow.htm` 文件，下半部分

前四个按钮使用匿名函数调用 `move()` 函数。每次调用 `move()` 函数时都会传入不同的参数。`image` 变量引用一个包含图片文件名称的数组，`imageIndex` 变量包含当前显示的图片在 `image` 数组中的索引。

要显示下一张图片，`imageIndex` 增加 1；要显示上一张图片，则减少 1。第一张图片的索引为 0，最后一张图片的索引为 `image.length - 1`。

接下来的两个按钮调用 `start()` 和 `stop()` 函数来启动和停止幻灯片。

现在来看程序的第一部分：

```html
... <head> ...

   <script>
```

```javascript
const image = ["im_paradise.jpg", "im_solar_eclipse.jpg",
   "im_wave.jpg", "im_winter.jpg", "im_tree.jpg"];

let imageIndex = 0, timeoutReference, timeoutActive = false;

function move(number)
{
   imageIndex = number;

   if(imageIndex >= image.length)
      imageIndex = 0;
   else if(imageIndex < 0)
      imageIndex = image.length - 1;

   document.getElementById("idImage").src = image[imageIndex];
   document.getElementById("idOutput").firstChild.nodeValue =
      (imageIndex + 1) + "/" + image.length;

   if(timeoutActive)
      timeoutReference = setTimeout(function() {
         move(imageIndex + 1);
      }, 1000);
}

function start()
{
   if(timeoutActive)
      return;

   timeoutActive = true;
```



```javascript
timeoutReference = setTimeout(function() {move(imageIndex+1);}, 500);

}

function stop()

{

   clearTimeout(timeoutReference);

   timeoutActive = false;

}
```

```html
</script>

</head>

...
```

**清单 6.46**　　`process_slideshow.htm` 文件，上半部分

首先，程序创建包含所有图片文件名称的数组。如果您想在幻灯片中显示自己的图片，只需修改这部分程序。

该数组的当前索引设置为 0，`timeoutReference` 变量引用时间控制进程。`timeoutActive` 变量表示幻灯片当前是否处于活动状态。

在 `move()` 函数中，`imageIndex` 的值根据函数的参数设置。如果 `imageIndex` 过大，则从 0 重新开始；如果 `imageIndex` 过小，则系统从数组末尾重新开始。

`src` 属性被赋予新值。这会切换图片，同时输出也会相应更新。

如果幻灯片当前处于活动状态，`move()` 函数会在短暂延迟后通过匿名函数再次调用自身。参数则根据 `imageIndex` 的当前值确定。

如果幻灯片已经在运行，`start()` 函数会立即退出。否则，在此处触发幻灯片的第一次图片切换。幻灯片在 `stop()` 函数中结束。

## 6.6 其他数据结构

数据结构用于将一组主题相关的数据存储在一个共同的名称下。这些数据由单个元素组成，这些元素通常具有相同的类型，但也可以具有不同的类型。

在第 6.1 节中，你学习了数组数据结构。在本节中，我们将添加更多称为集合和映射的数据结构。

### 6.6.1 集合

集合是一组唯一值的集合，这意味着每个值在集合中只出现一次。在 JavaScript 中，`Set` 对象用于创建集合。集合具有可用于访问其值的属性和方法。

以下程序展示了集合的一些典型操作：

```html
...

<body><p>

   <script>

const s = new Set([23, 5, 28, -4, 5, 8, 23]);

   s.add(5);

   s.add(36);

   document.write("Values with forEach(): ");

   function output(value)

   {

      document.write(value + " ");

   }

   s.forEach(output);

   document.write("<br>");

   let v = 23;

   if(s.has(v))

      document.write("Value " + v + " is in the set<br>");

   v=24;

   if(!s.has(v))

      document.write("Value " + v + " is not in the set<br>");

   document.write("Values with values(): ");

   const it = s.values();

   for(let i=0; i<s.size; i++)

      document.write(it.next().value + " ");

   document.write("<br>");

   document.write("Number of values: " + s.size + "<br>");

   s.delete(8);

   document.write("After deleting a value: " + s.size + "<br>");

   s.clear();

   document.write("After clearing the set: " + s.size);

</script></p>

</body></html>
```

**清单 6.47**　　`set.htm` 文件

你可以在创建集合时填充值。为此，需要在方括号中传递一个包含可能值的枚举。如果某个值出现两次，它只会被添加到集合中一次。

`add()` 方法用于添加单个值。这里遵循同样的原则：如果值已存在，则不会添加。

你可以使用 `forEach()` 方法按照值添加的顺序完全遍历集合。该方法接受一个函数引用作为参数，该函数会为每个值执行。这里，它是用于显示值的 `output()` 方法。我们看不到的是，`forEach()` 方法确保将值作为第一个参数传递给 `output()` 方法。

`has()` 方法用于确定某个特定值是否在集合中。

`values()` 方法返回一个迭代器类型的枚举对象，我们简称为迭代器。可以对此类型的对象调用 `next()` 方法，它提供对枚举中下一个元素的引用。该元素的值可以通过 `value` 属性确定。`size` 属性的值对应于集合中的值的数量，可以在 `for` 循环中使用它来输出集合的所有值。

`delete()` 方法用于从集合中删除特定值，`clear()` 方法用于删除集合中的所有值。程序的输出如图 6.39 所示。

![集合：创建、属性和方法](img/img-f6.39.html)

**图 6.39**　　集合：创建、属性和方法

### 6.6.2 映射

在 JavaScript 中，`Map` 对象用于创建关联数组，我们简称为映射。映射由一组键值对组成，你可以通过使用例如由字符串组成的键来访问各个值。相比之下，对于标准数组（第 6.1 节），你使用数字索引来访问各个值。映射具有可用于访问其键和值的属性和方法，并且与集合的属性和方法有一些相似之处。

以下程序展示了涉及映射的一些典型操作：

```html
...

<body><p>

   <script>

const m = new Map([["Peter", 31], ["Julia", 28], ["Warren", 35]]);

   m.set("Sandy", 38);

   m.set("Warren", 34);

   document.write("Elements with forEach(): ");

   function output(value, key)

   {

      document.write(key + ":" + value + " ");

   }

   m.forEach(output);

   document.write("<br>");

   let s = "Julia";

   if(m.has(s))

      document.write("Key:" + s + ", Value: " + m.get(s) + "<br>");

   s = "Ben";

   if(!m.has(s))

      document.write("Key:" + s + ", not available" + "<br>");

   document.write("Values with values(): ");

   const v = m.values();

   for(let i=0; i<m.size; i++)

      document.write(v.next().value + " ");

   document.write("<br>");

   document.write("Keys with keys(): ");

   const k = m.keys();

   for(let i=0; i<m.size; i++)

      document.write(k.next().value + " ");

   document.write("<br>");

   document.write("key-value pairs with entries(): ");

   const e = m.entries();

   for(let i=0; i<m.size; i++)

      document.write(e.next().value + " ");

   document.write("<br>");

   document.write("Number of elements: " + m.size + "<br>");

   m.delete("Warren");

   document.write("After deleting an element: " + m.size + "<br>");

   m.clear();

   document.write("After clearing the map: " + m.size);

</script></p>

</body></html>
```

**清单 6.48**　　`map.htm` 文件

你可以在创建映射时填充它。为此，需要传递一个键值对的枚举。每个对以及整个列表都用方括号括起来。

`set()` 方法用于添加单个对。如果该对的键已存在，则相应的值将被覆盖。

你可以使用 `forEach()` 方法按照对添加的顺序完全遍历映射。该方法接受一个函数引用作为参数，该函数会为每个值执行。这里，它是用于显示对的 `output()` 方法。我们看不到的是，`forEach()` 方法确保将键和值作为参数传递给 `output()` 方法。

`has()` 方法用于确定某个特定键是否在映射中，`get()` 方法可用于访问特定键的值。

`values()` 方法返回一个包含映射所有值的迭代器（第 6.6.1 节），`keys()` 方法提供包含映射所有键的迭代器。`entries()` 方法返回一个包含映射所有对的迭代器，`size` 属性的值对应于映射中的对数。在 `for` 循环中，可以利用这些关系输出映射的所有值、键或对。`delete()` 方法用于从映射中删除特定对，`clear()` 方法用于删除映射中的所有对。

程序的输出如图 6.40 所示。

![映射：创建、属性和方法](img/img-f6.40.html)

**图 6.40**　　映射：创建、属性和方法

### 注意

你可以在本书的下载材料中找到 `u_map` 练习，位于附加章节 1 的第 1.18 节，网址为 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。

## 6.7 JavaScript 对象表示法

JavaScript 对象表示法（JSON）是一种紧凑表示法的名称，可应用于对象和数组。我们将这种表示法称为 JSON 格式。

现代浏览器都熟悉 `JSON` 对象，它拥有静态方法，可用于将 JSON 格式的对象转换为可传输的字符串。反过来，你也可以从这样的字符串创建 JSON 格式的对象。

可传输的字符串不仅可由 JavaScript 处理，也可由其他语言处理，这简化了不同应用程序之间的数据传输。

### 6.7.1 JSON 格式与 JSON 对象

在以下示例中，程序创建了一个 JSON 格式的对象，然后使用 `JSON` 对象对其进行转换。

程序如下：

```html
...

<body><p>

   <script>
```

```javascript
const dodge = { "color":"Red", "speed":50.2 };

   document.write(dodge.color + " " + dodge.speed + "<br>");

   const tx = JSON.stringify(dodge);

   document.write(tx + "<br>");

   const renault = JSON.parse(tx);

   document.write(renault.color + " " + renault.speed + "<br>");

   renault.speed += 2.5;

   document.write("Faster: " + renault.speed);
```

```html
</script></p>

</body></html>
```

**清单 6.49**　　`json_compact.htm` 文件

在 JSON 格式中，对象用花括号括起来，各个属性-值对用逗号分隔，属性与值之间用冒号分隔，属性名放在双引号中。如果值是字符串，则同样用双引号；如果是数值，则不加引号。小数部分使用小数点分隔。

在程序中，JSON 格式的 `dodge` 对象通过 `JSON` 对象的 `stringify()` 方法转换为可传输的 `tx` 字符串。随后进行反向过程：`tx` 字符串通过 `JSON` 对象的 `parse()` 方法转换为 `renault` 对象，该对象随后以 JSON 格式可用。

`speed` 属性的值被识别为数值，因此也可以参与计算。

程序的输出如图 6.41 所示。

![JSON 格式与 JSON 对象](img/img-f6.41.html)

**图 6.41**　　JSON 格式与 JSON 对象

### 注意

ECMAScript 2024 引入了使用 `#` 字符使 JSON 格式对象不可变的功能。例如，`const dodge = #{ "color": "Red" };` 意味着对象的属性不能再被更改，而 `dodge.color = "Blue";` 语句将导致错误。

### 6.7.2 自定义类与 JSON 方法

借助一个中间步骤，`JSON` 对象的转换方法也可用于 `Car` 类。

程序如下：

```html
... <head> ...

   <script>
```

```javascript
class Car

   {

      constructor(c, s)

      {

         this.color = c;

         this.speed = s;

      }

      toString()

      {

         return this.color + " " + this.speed;

      }

   }
```

```html
</script>

</head>

<body><p>

   <script>
```

```javascript
const dodge = new Car("Red", 50.2);

   document.write(dodge + "<br>");

   const tx = JSON.stringify(dodge);

   document.write(tx + "<br>");

   const x = JSON.parse(tx);

   const renault = new Car(x.color, x.speed);

   document.write(renault + "<br>");

   renault.speed += 2.5;

   document.write("Faster: " + renault.speed);
```

```html
</script></p>

</body></html>
```

**清单 6.50**　　`json_class.htm` 文件

程序使用 `JSON` 类的 `stringify()` 方法将自定义 `Car` 类的对象转换为可传输的字符串。作为中间步骤，使用 `parse()` 方法从可传输字符串创建一个 JSON 格式的对象（`x`）。然后使用对象 `x` 的属性和值创建一个新的 `Car` 类对象。

程序的输出同样如图 6.41 所示。

### 6.7.3 JSON 对象与数组

`JSON` 对象也允许你使用数组，如下程序所示：

```html
...

<body><p>

   <script>
```

```javascript
const city = ["Berlin", "Hamburg", "Munich"];

   document.write(city + "<br>");

   const tx = JSON.stringify(city);

   document.write(tx + "<br>");

   const cityNew = JSON.parse(tx);

   document.write(cityNew);
```

```html
</script></p>

</body></html>
```

**清单 6.51**　　`json_array.htm` 文件

程序使用 `JSON` 对象的 `stringify()` 方法将字符串数组（`city`）转换为可传输的 `tx` 字符串。然后，使用 `JSON` 对象的 `parse()` 方法创建一个字符串数组（`cityNew`）。

程序的输出如图 6.42 所示。

![JSON 对象与数组](img/img-f6.42.html)

**图 6.42**　　JSON 对象与数组

### 6.7.4 JSON 格式与数组

以下程序使用一个以 JSON 格式提供的对象数组：

```html
...

<body><p>

   <script>
```

```javascript
const cr = [{"color":"Red", "speed":50.2},
```



```javascript
{"color":"Blue", "speed":85.3},

{"color":"Yellow", "speed":65.1}];

for(let i=0; i<cr.length; i++)

   document.write(cr[i].color + " " + cr[i].speed + " # ");

document.write("<br>");

const tx = JSON.stringify(cr);

document.write(tx + "<br>");

const crNew = JSON.parse(tx);

for(let i=0; i<crNew.length; i++)

   document.write(crNew[i].color + " " + crNew[i].speed + " # ");

document.write("<br>Faster: ");

for(let i=0; i<crNew.length; i++)

{

   crNew[i].speed += 2.5;

   document.write(crNew[i].speed + " # ");

}
```

```html
</script></p>

</body></html>
```

**清单 6.52**　`json_array_compact.htm` 文件

整个 JSON 格式的对象数组（`cr`）用方括号括起来，各个对象用花括号括起来。

使用 `JSON` 对象的 `stringify()` 方法创建可传输的 `tx` 字符串，然后使用 `JSON` 对象的 `parse()` 方法将 `tx` 字符串转换为新的 JSON 格式对象数组。

同样，`speed` 属性的值被识别为数值，因此可以参与计算。

这部分程序的输出如图图 6.43 所示。

![JSON 格式与数组](img/img-f6.43.html)

**图 6.43**　JSON 格式与数组

### 6.7.5 自定义类与数组

以下程序使用了 `Car` 类的对象数组。JSON 对象的转换方法在此同样适用，这得益于为 `Car` 类设置的中间步骤。

程序如下：

```html
... <head> ...

<script>
```

```javascript
class Car
{
   constructor(c, s)
   {
      this.color = c;
      this.speed = s;
   }

   toString()
   {
      return this.color + " " + this.speed;
   }
}
```

```html
</script>
</head>

<body><p>
<script>
```

```javascript
const cr = [new Car("Red", 50.2),
   new Car("Blue", 85.3), new Car("Yellow", 65.1)];

for(let i=0; i<cr.length; i++)

   document.write(cr[i] + " # ");

document.write("<br>");

const tx = JSON.stringify(cr);

document.write(tx + "<br>");

const crNew = new Array(3);

const x = JSON.parse(tx);

for(let i=0; i<crNew.length; i++)

{
   crNew[i] = new Car(x[i].color, x[i].speed);
   document.write(crNew[i] + " # ");
}

document.write("<br>Faster: ");

for(let i=0; i<crNew.length; i++)

{
   crNew[i].speed += 2.5;
   document.write(crNew[i].speed + " # ");
}
```

```html
</script></p>

</body></html>
```

**清单 6.53**　`json_array_class.htm` 文件

该程序使用 `JSON` 类的 `stringify()` 方法，将自定义 `Car` 类的对象数组转换为可传输的字符串。

然后，按所需大小创建一个空数组（`crNew`）。

作为中间步骤，从可传输字符串生成一个 JSON 格式的对象数组（`x`）。接着，利用 `x` 数组元素的属性和值创建 `Car` 类的新对象，并保存在 `crNew` 数组中。

程序的输出结果也与图 6.43 所示类似。JSON 文件将在第 7 章的第 7.4 节中导入。

### 注意

在本书可下载材料（位于 [`www.rheinwerk-computing.com/5875`](http://www.rheinwerk-computing.com/5875)）的附加章节 3 中，您可以找到一些包含第 6 章各元素的示例项目。

# 7 使用 Ajax 进行更改

Ajax 技术使得无需完全重建显示的文档，即可用来自 Web 服务器的数据交换网站的部分内容。

异步 JavaScript 与 XML（Ajax）提供了浏览器与 Web 服务器之间的异步数据传输。它允许您更改网站的部分内容，而无需重新创建并提交整个文档，从而降低了开发成本和网络流量，使网站更快、更灵活。Ajax 技术是许多网站的标准组件。

其过程如下：由于某个事件，从网站向 Web 服务器发送请求，Web 服务器返回响应。响应在仍在显示的文档中进行分析，分析结果导致文档的一部分被更改。整个流程的核心组件是 `XMLHttpRequest` 类型的对象。

本章中的所有文档均通过 Web 服务器访问，您从该服务器请求数据以插入到页面中。在本章中，我通过我的域名 [`theisweb.de`](http://www.theisweb.de) 从 `jse` 目录中检索文档。数据可以以多种形式存在于 Web 服务器上：

- 作为 PHP 程序（第 7.1 节）
- 作为文本文件中的文本（如第 7.1 节末尾所示）
- 作为 XML 文件（第 7.3 节）
- 作为文本文件中的 JSON 对象（第 7.4 节）

## 7.1 Hello Ajax

通过第一个示例 `Hello Ajax`，我将解释适用于整章的基本流程。

在该示例中，显示了一个包含超链接的 HTML 文档（参见图 7.1）。此处，超链接并不引用其他文档，因此超链接目标仅由 `#` 字符组成。相反，超链接用于触发事件。

![永久显示的文档](img/img-f7.1.html)

**图 7.1**　永久显示的文档

该文档包含另一个段落。点击超链接会向 Web 服务器发送请求，服务器响应返回一段文本，该文本成为段落的内容，并显示在文档中，如图 7.2 所示。文档的其余部分保持不变。

![从 PHP 文件补充的文档](img/img-f7.2.html)

**图 7.2**　从 PHP 文件补充的文档

首先，我们来看包含 JavaScript 代码的 HTML 文档：

```html
... <head> ...

<script>
```

```javascript
function request()
{
   const req = new XMLHttpRequest();

   req.open("get", "ajax_hello.php", true);

   // req.open("get", "ajax_hello.txt", true);

   req.onreadystatechange = evaluate;
   req.send();
}

function evaluate(e)
{
   if(e.target.readyState == 4 && e.target.status == 200)
      document.getElementById("idParagraph")
         .firstChild.nodeValue = e.target.responseText;
}
```

```html
</script>
</head>

<body>

<p><a id="idLink" href="#">请点击</a></p>

<p id="idParagraph"> </p>

<script>
```

```javascript
document.getElementById("idLink").addEventListener("click", request);
```

```html
</script>
</body></html>
```

**清单 7.1**　`ajax_hello.htm` 文件

此外，以下是响应的 PHP 程序：

```php
<?php

header("Content-type: text/html; charset=utf-8");

echo "PHP 文件：Hello Ajax";

?>
```

**清单 7.2**　`ajax_hello.php` 文件

`ajax_hello.htm` 文件包含超链接和段落，点击超链接会调用 `request()` 函数。首先，创建一个新的 `XMLHttpRequest` 对象。

该对象的 `open()` 方法打开与 Web 服务器上另一个文件的通信，此处为 `ajax_hello.php`，使用 `GET` 方法。`open()` 方法的第三个参数通常设置为 `true`。这确保了通信以异步方式处理，意味着其他进程无需等待请求结束。

`onreadystatechange` 事件处理程序被赋予一个对命名函数或匿名函数的引用，此处为 `evaluate()` 函数。发送后，`XMLHttpRequest` 对象会多次改变其状态，事件处理程序响应此更改事件。简而言之，每次状态改变时都会调用 `evaluate()` 方法。

`XMLHttpRequest` 对象的 `send()` 方法将请求发送到 Web 服务器。最初不会传输其他数据，并且传输应在注册事件处理程序之后进行。这样，就不会有任何事件被遗漏。

一个事件对象被传递给 `evaluate()` 方法，该对象的 `target` 属性引用了 `XMLHttpRequest` 对象。首先，会检查它的 `readystate` 和 `status` 属性。只有当 `readystate` 取值为 `4` 且 `status` 取值为 `200` 时，评估才有意义。`status` 属性表示超文本传输协议（HTTP）状态码的值。200 表示成功，404 表示页面未找到，500 表示服务器内部错误，以此类推。

`XMLHttpRequest` 对象的 `responseText` 属性包含来自 Web 服务器的响应——在本例中，是 `Hello Ajax` 文本，该文本通过 PHP 关键字 `echo` 输出。这段文本被设置为段落的新内容。

你也可以从 Web 服务器请求一个文本文件的内容，并将其插入到现有文档中。为此，你需要交换 `request()` 函数中 `open()` 方法的调用（即，为第二行设置注释字符，并为第三行取消注释）。文本文件内容如下：

```text
TXT 文件: Hello Ajax
```

**清单 7.3**　`ajax_hello.txt` 文件

### 注意

以下内容适用于浏览器与 Web 服务器之间的传输：

- 通信通过 HTTP 进行规范。HTTPS 是 HTTP 的安全加密演进版本。
- 浏览器向 Web 服务器发出的请求用于请求数据，而响应则是 Web 服务器对浏览器的回答。
- 请求有多种方法。GET 方法传输较小数据量（最多 255 字节），而 POST 方法传输较大数据量。

## 7.2 发送参数

本节包含一个示例，其中参数被发送到 Web 服务器。PHP 程序的响应取决于这些参数中的数据。

显示一个包含两个超链接和一个空段落的 HTML 文档（参见图 7.3）。

![带参数调用](img/img-f7.3.html)

**图 7.3**　带参数调用

当你点击第一个超链接时，系统请求人员编号为 6714 的人员数据；当你点击第二个超链接时，系统请求人员编号为 81343 的人员数据。随后，该人员的数据会显示在超链接下方（参见图 7.4 和图 7.5）。

![人员编号 6714 的全部数据](img/img-f7.4.html)

**图 7.4**　人员编号 6714 的全部数据

![人员编号 81343 的部分数据](img/img-f7.5.html)

**图 7.5**　人员编号 81343 的部分数据

首先来看包含 JavaScript 代码的 HTML 文档：

```html
... <head> ...

<script>
```

```javascript
function request(personnel_number, scope)
{
   const req = new XMLHttpRequest();

   req.open("get", "ajax_parameters.php?pno=" + personnel_number
      + "&scope=" + scope, true);

   req.setRequestHeader("Content-Type",
      "application/x-www-form-urlencoded");

   req.onreadystatechange = evaluate;
   req.send();
}

function evaluate(e)
{
   if(e.target.readyState == 4 && e.target.status == 200)
      document.getElementById("idParagraph").firstChild.nodeValue =
         e.target.responseText;
}
```

```html
</script>
</head>

<body>

<p>人员编号：</p>

<p><a id="idLink0" href="#">6714</a></p>

<p><a id="idLink1" href="#">81343</a></p>

<p id="idParagraph"> </p>

<script>
```

```javascript
document.getElementById("idLink0").addEventListener
   ("click", function() { request(6714, "all"); });

document.getElementById("idLink1").addEventListener
   ("click", function() { request(81343, "part"); });
```

```html
</script>
</body></html>
```

**清单 7.4**　`ajax_parameters.htm` 文件

此外，以下是响应的 PHP 程序：

```php
<?php

header("Content-type: text/html; charset=utf-8");

if($_GET["pno"] == 6714)
{
   if($_GET["scope"] == "all")
      echo "6714, Mayer, John, $3,500, born on 03/15/1962";
   else
      echo "6714, Mayer, John";
}
else if($_GET["pno"] == 81343)
{
   if($_GET["scope"] == "all")
      echo "81343, Smith, Peter, $3,750, born on 04/12/1958";
   else
      echo "81343, Smith, Peter";
}

?>
```



**清单 7.5**　`ajax_parameters.php` 文件

点击两个超链接中的任意一个都会调用`request()`函数，该函数会传输两个参数：一个数字和一个字符串。

你使用`XMLHttpRequest`对象的`setRequestHeader()`方法来定义这些数据的传输形式。在本例中，数据被附加到网站地址后面。`XMLHttpRequest`对象的`open()`方法的参数对应于所谓的查询字符串的内容，查询字符串的各个部分之间用`&`符号分隔。对于第一个超链接，查询字符串是`pno=6714&scope=all`。

数据发送后，PHP 文件中的`$_GET["pno"]`和`$_GET["scope"]`元素将分别包含各自的值。在分支中，决定返回哪个响应。

## 7.3　读取 XML 文件

可扩展标记语言（XML）是一种广泛使用的、平台无关的数据格式，适用于通用数据交换。你可以使用 Ajax 将外部程序生成并存储在 Web 服务器上的 XML 文件内容整合到你的文档中。

XML 实际上是一种关于语言如何构建的规范。XML 中有一个包含子节点的节点层次结构，正如你在第 5 章中已经看到的 HTML 那样。XML 文件的元素也是通过标签、容器和属性创建的。XML 文件可以在简单的文本编辑器中编辑。

### 7.3.1　单个对象

你可以使用 Ajax 将 Web 服务器上 XML 文件的内容集成到文档中。

首先是 XML 文件：

```xml
<?xml version="1.0" encoding="UTF-8"?>

<car>

   <color>红色</color>

   <speed>50</speed>

   <power displacement="1600" cylinders="4">76.2</power>

</car>
```

**清单 7.6**　`ajax_xml_single.xml` 文件

现代浏览器可以直接显示 XML 文件的结构，无论该 XML 文件是通过 Web 服务器检索还是直接从本地硬盘获取，这一点都成立。在图 7.6 中，你可以看到指定的 XML 文件。

XML 文件可以链接到另一个文件以格式化 XML 数据，但本章的示例中没有这样做。因此，图 7.6 中提供了带有文本`此 XML 文件似乎未显示...`的注释。

![XML 文件结构](img/img-f7.6.html)

**图 7.6**　XML 文件结构

XML 代码的第一行标识了内容为 XML。接下来的字符编码指定了所使用的字符集，这与 HTML 文档类似。每个 XML 文件中都有一个主元素或根节点，你可以自由选择各个节点的名称，只要遵守 XML 规则并保持自身结构的一致性即可。

这里的根节点是`car`元素。一个`car`有三个属性，其值被定义为子节点，而第三个子节点有两个属性，每个属性都有值。如果某个值是带小数的数字，则必须用小数点分隔。

点击超链接后，通过 Ajax 从 XML 文件中读取这些数据，并填充到段落中（参见图 7.7）。

![单个对象的数据](img/img-f7.7.html)

**图 7.7**　单个对象的数据

以下是相应的程序：

```html
... <head> ...

   <script>

      function request()

      {

         const req = new XMLHttpRequest();

         req.open("get", "ajax_xml_single.xml", true);

         req.onreadystatechange = evaluate;

         req.send();

      }

      function evaluate(e)

      {

         if(e.target.readyState == 4 && e.target.status == 200)

         {

            const response = e.target.responseXML;

            const kcolor = response.getElementsByTagName("color")[0];

            const kpower = response.getElementsByTagName("power")[0];

            document.getElementById("idData").firstChild.nodeValue =

               "Color: " + kcolor.firstChild.nodeValue

                  + ", Power: " + kpower.firstChild.nodeValue

                  + ", Displacement: " + kpower.getAttribute("displacement")

                  + ", Cylinders: " + kpower.getAttribute("cylinders");

         }

      }

   </script>

</head>

<body>

   <p>Car data:</p>

   <p><a id="idLink" href="#">Dodge</a></p>

   <p id="idData"> </p>

   <script>

      document.getElementById("idLink").addEventListener("click", request);

   </script>

</body></html>
```

**清单 7.7**　`ajax_xml_single.htm` 文件

在`request()`函数中，`open()`方法打开与响应 XML 文件的通信。这里请求的是 XML 文档而非文本文档，因此`evaluate()`函数使用`responseXML`属性而非`responseText`属性。

在接下来的段落中，你会看到许多与第 5 章内容相似的地方。`document`对象的`getElementsByTagName()`方法返回一个数组，其中包含对所有具有所需标签的 XML 元素的引用，在本例中，是针对`color`标签和`power`标签。示例中只有一个数组元素，索引为 0。

第一个元素的第一个子节点通过`node`对象的`firstChild`属性输出。然后通过`node`对象的`getAttribute()`方法确定并输出两个不同属性的值。

### 7.3.2　对象集合

在下面的 XML 文件中，你可以看到一个结构相似的对象集合。通过 Ajax 将该 XML 文件的内容集成到 HTML 文档中。

首先是 XML 文件：

```xml
<?xml version="1.0" encoding="UTF-8"?>

<collection>

   <car>

      <color>Red</color>

      <speed>50</speed>

      <power displacement="1600" cylinders="4">76.2</power>

   </car>

   <car>

      <color>Yellow</color>

      <speed>65</speed>

      <power displacement="1800" cylinders="4">85.0</power>

   </car>

</collection>
```

**清单 7.8**　`ajax_xml_collection.xml` 文件

在图 7.8 中，你可以看到未格式化的 XML 文件。

![XML 文件的结构](img/img-f7.8.html)

**图 7.8**　XML 文件的结构

这里有多个`car`类型的节点。必须添加另一个节点作为父节点，以确保仍然只有一个主元素或根节点。该元素具有`collection`标签，以及两个之前描述过的`car`类型的子节点。

点击图 7.9 中的某个超链接后，最初为空的段落将通过 Ajax 填充。

![集合中对象的数据](img/img-f7.9.html)

**图 7.9**　集合中对象的数据

以下是相应的程序：

```html
... <head> ...

   <script>

      function request(x)

      {

         const req = new XMLHttpRequest();

         req.open("get", "ajax_xml_collection.xml", true);

         req.onreadystatechange = function(e) { evaluate(e, x); };

         req.send();

      }

      function evaluate(e, x)

      {

         if(e.target.readyState == 4 && e.target.status == 200)

         {

            const response = e.target.responseXML;

            const kcolor = response.getElementsByTagName("color")[x];

            const kpower = response.getElementsByTagName("power")[x];

            document.getElementById("idData").firstChild.nodeValue =

               "Color: " + kcolor.firstChild.nodeValue

                  + ", Power: " + kpower.firstChild.nodeValue

                  + ", Displacement: " + kpower.getAttribute("displacement")

                  + ", Cylinders: " + kpower.getAttribute("cylinders");

         }

      }

   </script>

</head>

<body>

   <p>Car data:</p>

   <p><a id="idLink0" href="#">Dodge</a></p>

   <p><a id="idLink1" href="#">Renault</a></p>

   <p id="idData"> </p>

   <script>

      document.getElementById("idLink0").addEventListener

         ("click", function() { request(0); } );

      document.getElementById("idLink1").addEventListener

         ("click", function() { request(1); } );

   </script>

</body></html>
```

**清单 7.9**　`ajax_xml_collection.htm` 文件

当你点击某个超链接时，相应的值会作为参数传递给`request()`函数。然后，该值通过匿名函数进一步传递给`evaluate()`函数。这样，就可以从集合中确定匹配对象的数据并返回，以填充最初为空的段落。

### 7.3.3　搜索建议

Ajax 的典型用途之一是在输入字段中输入搜索字符串时显示建议。我将在下面的示例中演示这一点。

一个 XML 文件包含欧盟国家数据的集合。当你在程序的搜索字段中输入字符时，那些首字母与已输入字符匹配的国家数据会作为搜索辅助显示出来。搜索字段的任何变化都会直接导致显示内容的变化。

在图 7.10 中，你可以看到在搜索字段中输入“B”后的结果。在图 7.11 中，输入扩展为“Be”，如果删除“e”，则会再次显示为图 7.10。

![输入“B”后](img/img-f7.10.html)

**图 7.10**　输入“B”后

![输入“Be”后](img/img-f7.11.html)

**图 7.11**　输入“Be”后

首先是 XML 文件的内容：

```xml
<?xml version="1.0" encoding="UTF-8"?>

<countries>

   <country>

      <name>Belgium</name>

      <area>30528</area>

      <city>Brussels</city>

   </country>

   <country>

      <name>Bulgaria</name>

      <area>110994</area>

      <city>Sofia</city>

   </country>

   <country>

      <name>Denmark</name>

      <area>43094</area>

      <city>Copenhagen</city>

   </country>

</countries>
```

**清单 7.10**　`ajax_eu.xml` 文件

在图 7.12 中，你可以看到没有格式化的 XML 文件。

主元素或根节点具有`countries`标签和`country`类型的子节点。对于每个`country`类型的对象，都有`name`、`area`和`city`子节点。

![XML 文件的结构](img/img-f7.12.html)

**图 7.12**　XML 文件的结构

以下是程序的第一部分：

```html
...
<body>

   <p id="idParagraph"><input id="idInput"> 搜索欧盟国家</p>

   <script>
```

```javascript
document.getElementById("idInput")
         .addEventListener("keydown", request);
```

```html
   </script>
</body></html>
```

**清单 7.11**　`ajax_eu.htm` 文件，下半部分

具有`idParagraph` ID 的段落包含两个子节点：具有`idInput` ID 的搜索字段和文本“搜索欧盟国家”。还有一个`keydown`事件的事件处理程序，当按下某个键时触发。

现在让我们看看程序上半部分包含 JavaScript 函数的部分：

```html
... <head> ...

   <script>
```

```javascript
function request()
      {
         const req = new XMLHttpRequest();
         req.open("get", "ajax_eu.xml", true);
         req.onreadystatechange = evaluate;
         req.send();
      }

      function evaluate(e)
      {
         if(e.target.readyState == 4 && e.target.status == 200)
         {
            const par = document.getElementById("idParagraph");
             while(par.childNodes.length > 2)
               par.removeChild(par.lastChild);

            if(document.getElementById("idInput").value == "")
               return;

            const response = e.target.responseXML;
            const nameAll = response.getElementsByTagName("name");
            const search = document.getElementById("idInput").value;

            for(let i=0; i<nameAll.length; i++)
            {
               const name = nameAll[i].firstChild.nodeValue;

               if(search == name.substr(0,search.length))
               {
                 const area = response.getElementsByTagName(
                     "area")[i].firstChild.nodeValue;

                 const city = response.getElementsByTagName(
                     "city")[i].firstChild.nodeValue;
```



```javascript
const text = document.createTextNode(name + ", "
   + area + " sq mi, " + city);

const divElement = document.createElement("div");

divElement.appendChild(text);

par.appendChild(divElement);

}
}
}
}
```

```html
</script>
</head>

...
```

**清单 7.12**　ajax_eu.htm 文件，上半部分

在`request()`函数中，`open()`方法打开与响应 XML 文件的通信。响应在`responseXML`属性中提供。

在`evaluate()`函数中，旧的搜索建议被移除。这些是段落（具有`idParagraph` ID）的额外子节点。使用`while`循环，这些额外的子节点被逐个删除，从最后一个子节点开始。删除过程一直运行，直到只剩下两个原始子节点：具有`idInput` ID 的搜索字段和文本“搜索欧盟国家”。

如果搜索字段完全为空，则退出`evaluate()`函数，不显示任何搜索帮助。但是，如果搜索字段中仍有字符，则会从 XML 响应中确定包含所有国家名称的字段。检查该字段的元素，如果已输入的字符与国家名称的前几个字母匹配，则显示该国家的数据。

首先，为此目的，确定该国家的面积和首都信息。接下来，创建一个文本节点，以可读形式汇总国家数据，并将该文本节点作为子节点分配给新创建的`div`类型的 HTML 元素节点。最后，将此`div`节点作为新的子节点添加到具有`idParagraph` ID 的段落中。

### 注意

以下是一些可能的改进建议：

- 你可以使用`setTimeout()`在点击按钮后等待一小段时间再发起请求。这样，可以在不每次都调用函数的情况下，在请求中实现多次更改。
- XML 文件的内容可以使用 PHP 和数据库动态生成；这样就会有更多信息可供选择。

## 7.4　读取 JSON 文件

你已经在第 6 章的第 6.7 节中了解了 JSON。JSON 格式是 XML 作为通用数据交换格式的替代方案，在这里，我将向你展示 JSON 如何简化不同应用程序之间的数据传输。

一个文本文件包含 JSON 格式的数据，例如使用 PHP 保存。我们将使用 Ajax 将这些数据集成到现有的 HTML 文档中。

### 7.4.1　单个对象

首先，我们来看一个文本文件中 JSON 格式的单个对象。我们将使用 Ajax 将此对象集成到网站中，文本文件如下所示：

```json
{"color":"Red","speed":50.2}
```

**清单 7.13**　ajax_json_single.txt 文件

文本文件包含 JSON 格式的整个对象。点击超链接后，使用 Ajax 从文本文件中读取其数据，并填充段落（参见图 7.13）。

![JSON 格式的单个对象数据](img/img-f7.13.html)

**图 7.13**　JSON 格式的单个对象数据

以下是相应的程序：

```html
... <head> ...

<script>
```

```javascript
function request()
{
   const req = new XMLHttpRequest();

   req.open("get", "ajax_json_single.txt", true);
   req.onreadystatechange = evaluate;
   req.send();
}

function evaluate(e)
{
   if(e.target.readyState == 4 && e.target.status == 200)
   {
      const response = JSON.parse(e.target.responseText);

      document.getElementById("idOutput").firstChild.nodeValue
         = "颜色: " + response.color
         + ", 增加的速度: " + (response.speed + 2.5);
   }
}
```

```html
</script>
</head>

<body>
   <p>汽车数据：</p>
   <p><a id="idLink" href="#">道奇</a></p>
   <p id="idOutput">&nbsp;</p>

   <script>
```

```javascript
document.getElementById("idLink").addEventListener("click", request);
```

```html
</script>
</body>
</html>
```

**清单 7.14**　ajax_json_single.htm 文件

在`request()`函数中，`open()`方法打开与响应文本文件的通信。当请求文本时，响应位于`evaluate()`函数的`responseText`属性中。

使用`JSON.parse()`方法将字符串转换为对象。输出对象属性的值，识别数值，并可以对其进行计算。

### 7.4.2　对象集合

以下文本文件包含一个 JSON 格式的对象数组。使用 Ajax 将内容集成到 HTML 文档中：

```json
[
  {"color":"Red","speed":50.2},
  {"color":"Blue","speed":85.3},
  {"color":"Yellow","speed":65.1}
]
```

**清单 7.15**　ajax_json_collection.txt 文件

单击图 7.14 中的某个超链接后，Ajax 会填充其下方的文本字段。

![来自集合的 JSON 格式对象数据](img/img-f7.14.html)

**图 7.14**　来自集合的 JSON 格式对象数据

以下是相应的程序：

```html
... <head> ...

<script>
```

```javascript
function request(x)
{
   const req = new XMLHttpRequest();

   req.open("get", "ajax_json_collection.txt", true);
   req.onreadystatechange = function(e) { evaluate(e, x); };
   req.send();
}

function evaluate(e, x)
{
   if(e.target.readyState == 4 && e.target.status == 200)
   {
      const response = JSON.parse(e.target.responseText);

      document.getElementById("idOutput").firstChild.nodeValue
         = "Color: " + response[x].color + ", increased speed: "
         + (response[x].speed + 2.5);
   }
}
```

```html
</script>
</head>

<body>
   <p>Car data:</p>
   <p><a id="idLink0" href="#">Dodge</a></p>
   <p><a id="idLink1" href="#">Nissan</a></p>
   <p><a id="idLink2" href="#">Renault</a></p>
   <p id="idOutput"></p>

   <script>
```

```javascript
for(let i = 0; i < 3; i++)
   document.getElementById("idLink" + i).addEventListener(
      "click", function() { request(i); }
   );
```

```html
</script>
</body>
</html>
```

**清单 7.16**　ajax_json_collection.htm 文件

当单击某个超链接时，程序会将相应的值作为参数传递给`request()`函数。然后，该值通过匿名函数进一步传递给`evaluate()`函数。这样，就可以从数组中确定相应的元素。该元素的数据被返回，并在必要时进行计算后填充到段落中。

# 8　使用层叠样式表进行设计

使用 CSS 以标准化方式对网站元素进行格式化和定位。JavaScript 允许进行更改和效果，包括动画。

层叠样式表（CSS）是相互补充的格式化模板。通常只使用术语“样式表”，而不带“层叠”二字。

样式表使我们能够做到以下几点：

- 将 HTML 文档的格式与内容分离。
- 定义集中的、标准化的格式。
- 通过局部格式补充或覆盖这些格式。
- 实现超越 HTML 的格式。
- 将元素定位在文档中的任意位置。

包含许多独立网页的大型网站通常使用集中式格式。它们赋予网站统一的外观，节省代码，并且易于对整个网站进行更改。在本书中，我仅解释 CSS 丰富功能中的一小部分，而 CSS 本身也在不断扩展。

你可以使用 JavaScript 动态更改样式表。这开辟了有趣的可能性，特别是在定位元素（如动画）方面。

## 8.1　结构与规则

本节介绍样式表的结构、不同样式表的组合以及使用样式表的一些规则。

本节中的三个文件不包含`js5.css`文件，该文件在本书的大多数示例中使用样式表确保统一显示。相反，本节使用自己的样式表来演示效果。

### 8.1.1　位置与选择器

你可以在以下不同位置定义样式表：

- 外部：在外部文件中定义，该文件可以被集成，并在许多文档中实现统一格式。
- 嵌入：在文档的头部使用`style`容器定义，使格式在整个文档中统一。
- 内联：在 HTML 标签中使用`style`属性定义，使格式仅适用于文档中的该位置。

你还可以通过以下方式使用选择器将样式表分配给文档的特定部分：

- HTML 选择器：将样式表分配给所有具有相同 HTML 标签的元素。
- 类选择器：将样式表分配给所有分配了相关类的 HTML 标签。
- ID 选择器：将样式表分配给各个具有唯一 ID 的元素。

我们将在以下段落中基于一个示例解释各种位置和选择器。样式表可以由多个 CSS 属性组成，但在此示例中，我们最初只使用一个 CSS 属性：值为`overline`的`text-decoration`。这会导致相关元素出现上划线（不是下划线！），如图 8.1 所示。

![样式表的位置与选择器](img/img-f8.1.html)

**图 8.1**　样式表的位置与选择器

以下是程序：

```html
<!DOCTYPE html>
<html lang="en-us">
<head>
   <meta charset="utf-8">
   <title>CSS, locations and selectors</title>
   <link rel="stylesheet" href="css_external.css">

   <style>
```

```css
p      { text-decoration: overline; }
.over  { text-decoration: overline; }
#idTop { text-decoration: overline; }
```

```html
   </style>
</head>

<body>
   <p>The first paragraph</p>
   <p>A list:</p>

   <ul>
      <li>First <span class="über">entry</span></li>
      <li>Second entry</li>
      <li class="over">Third entry</li>
   </ul>

   <table>
      <tr>
         <td>First cell</td>
         <td id="idTop">Second cell</td>
         <td>Third <span style="text-decoration: overline;">cell</span></td>
         <td><b>Fourth</b> cell</td>
      </tr>
   </table>
</body>
</html>
```

**清单 8.1**　css_details.htm 文件

你可以使用`<link rel="stylesheet" href="css_external.css">`从`css_external.css`文件集成外部样式表，该文件可以被许多文件使用。我们将在后续文本中解释外部文件的内容。

来自文件头部嵌入的`style`容器的样式表仅适用于当前的`css_details.htm`文件。你可以像在 JavaScript 中一样，在`/*`和`*/`之间为样式表添加解释性注释。

单个 CSS 属性由属性和值组成，用冒号分隔，并以分号结尾。整个 CSS 用花括号括起来。

选择器按如下方式分配样式表：

- HTML 选择器由相关的 HTML 标签组成；此处为`p`。结果，所有`p`容器的内容都被赋予上划线。
- 类选择器由一个点号和自定义的类名标识；这里使用的是`.over`。命名规则与 JavaScript 变量类似（即只能包含字母、数字或下划线，且不能以数字开头）。所有使用了`over`类的 HTML 标签都会显示上划线。
- ID 选择器以井号`#`开头，后接 ID；这里完整的选择器是`#idTop`。这会使具有`idTop` ID 的元素内容显示上划线。

以下是外部文件的内容：

```css
/* CSS specifications to implement */

b { text-decoration: overline; }
```

**清单 8.2**　css_external.css 文件

外部文件包含一条注释和一个带有 HTML 选择器的样式表。该 HTML 选择器的作用是：在所有引用此外部文件的文件中，所有`b`容器内的内容都会显示上划线。

由于文件头部的 HTML 选择器，这两个段落都带有上划线。在列表中，有两个元素被分配了`over`类：第一个列表项中的`span`元素，以及整个第三个列表项。分配通过`class`属性完成。

表格中的第二个单元格具有`idTop` ID，而第三个单元格内通过`style`属性进行了内联声明。这里不需要花括号，每条 CSS 声明应以分号结尾。在第四个单元格中，有一个加粗区域，根据外部 CSS 规则，该区域显示上划线。

### 8.1.2　组合

你可以将选择器和类相互组合，本节将展示一些示例。除了上划线，你还可以在文档中使用 CSS 属性`font-weight`并设置值为`bold`来实现加粗格式，也可以使用 CSS 属性`font-style`并设置值为`italic`来实现斜体。

以下是程序代码：

```html
<!DOCTYPE html>
<html lang="en-us">
<head>
   <meta charset="utf-8">
   <title>CSS, combinations</title>

   <style>
```

```css
p.over   { text-decoration: overline; font-weight: bold; }
.slanted { font-style: italic; }
li b     { text-decoration: overline; }
div, td  { text-decoration: overline; }
```

```html
   </style>
</head>

<body>
   <p class="over">The first paragraph</p>
   <p>The <i class="over">second</i> paragraph</p>
   <div>An additional line</div>
   <p>A <b>list</b>:</p>

   <ul>
      <li>First <b>entry</b></li>
      <li>Second entry</li>
   </ul>

   <table>
      <tr>
         <td>First cell</td>
         <td>Second cell</td>
      </tr>
   </table>

   <p class="over slanted">The last paragraph</p>
</body>
``` 



</html>

### 清单 8.3：css_combinations.htm 文件

`p.over` 声明是一个关联选择器，两个不同的选择器（此处为 HTML 选择器和类选择器）必须匹配。只有被分配了 `over` 类的段落才会显示上划线并加粗。多个 CSS 属性以分号分隔列出。接下来是一个简单的类选择器：`slanted` 类。

`li b` 声明（中间没有点号）是一个嵌套选择器。两个选择器也必须同时生效，但以嵌套形式。只有位于 `b` 容器内且该 `b` 容器又位于 `li` 容器内的文档部分才会显示上划线。

你可以将多个选择器用逗号分隔依次列出。以下样式表适用于所有列出的选择器，因此 `div` 容器的内容和单元格的内容都会显示上划线。

第一个段落显示上划线并加粗，因为它被分配了 `over` 类。第二个段落没有任何上划线或加粗。该段落中的 `i` 容器被分配了 `over` 类，但整个段落没有。接下来是一个带有上划线的 `div` 容器。

列表上方的段落没有适用的选择器。虽然有一个 `b` 容器，但它不在 `li` 容器内。第一个列表项的第二个单词情况则不同：这里有一个 `b` 容器位于 `li` 容器内。

表格中有两个带有上划线的 `td` 容器。

最后一个段落被分配了两个类，用空格分隔。这意味着 `over` 类和 `slanted` 类的样式表都会生效。

格式化的结果见图 8.2。

![组合选择器](img/img-f8.3.html)

**图 8.2**　组合选择器

### 8.1.3　层叠与覆盖

由于 CSS 提供了众多选项，常常会出现多个样式表同时作用于文档中某个元素的情况。这种行为是可取的，并且增加了灵活性。除了对整个网站进行集中格式化外，你还可以使用局部格式化而不会产生任何矛盾。

当使用多个样式表时，适用以下规则：

- 如果 CSS 属性不同，它们会相互补充。这也称为层叠。
- 如果 CSS 属性相同，则离元素最近的定义值生效：内联定义覆盖嵌入定义，嵌入定义又覆盖外部定义。

让我们通过一个示例来演示：

```html
<!DOCTYPE html><html lang="en-us">

<head>

   <meta charset="utf-8">

   <title>CSS, rules</title>

   <link rel="stylesheet" href="css_external.css">

   <style>
```

```css
 b {text-decoration:underline;}
```

```html
 <style>

</head>

<body>

   <p>The <b>first</b> paragraph</p>

   <p>The <b style="text-decoration:line-through;">second</b> paragraph</p>

   <p>The <b style="font-style:italic;">third</b> paragraph</p>

</body>

</html>
```

**清单 8.4**　css_rules.htm 文件

首先，从`css_extern.css`文件集成了外部样式表，正如你在第 8.1.1 节中已经了解的那样。该节规定加粗区域显示上划线。

在文档头部嵌入的定义中，为同一个选择器定义了相同的属性，但使用了不同的值进行覆盖。这意味着在该文档中，加粗区域显示下划线，如第一个段落所示。

在第二个段落中，为同一个属性（同样是加粗区域）进行了第三次定义。再次发生覆盖，该区域显示删除线。

在第三个段落中，加粗区域内发生了属性的层叠。在下划线的基础上增加了另一个特性：斜体字体样式。

结果如图 8.3 所示。

![层叠与覆盖](img/img-f8.3.html)

**图 8.3**　层叠与覆盖

## 8.2　更改属性

你可以使用`style`属性为 HTML 元素定义 CSS 样式。在 JavaScript 中，你可以通过同样名为`style`的属性来更改 CSS 样式。如果通过时间控制的过程，以小步幅重复进行更改，最终就能像电影一样产生动画效果。

在本节中，我们将定义位置、大小、`z-index`、透明度和颜色的 CSS 属性，然后更改并动画化`style`属性的相关子属性。`z-index`是元素在 z 方向（即朝向或远离观察者）上的位置。

### 8.2.1　位置

CSS 的`position`、`top`和`left`属性用于定义元素的位置，具体如下：

- CSS 的`position`属性表示定位类型。在此上下文中常使用`absolute`值，表示相对于文档边缘的绝对定位。
- CSS 的`top`和`left`属性定义了定位元素的左上角与文档左上角之间的距离。该值通常以`px`单位（像素）给出。

现在，我们来看一下图 8.4 中的文档。

![定位元素](img/img-f8.4.html)

**图 8.4**　定位元素

文档中有两个定位元素：一张图片和一个包含文本且背景为深色的`div`容器。

以下是程序的下半部分，展示了文档的结构：

```html
...

<body>

   <p><input id="idChange" type="button" value="Change">

      <input id="idAnimate" type="button" value="Animate"></p>

   <p>Text outside of positioned elements</p>

   <p>Another text outside of positioned elements</p>

   <img src="im_paradise.jpg" alt="Paradise" id="idImage"

        style="position:absolute; top:80px; left:120px;">

   <div style="position:absolute; top:100px; left:50px;

         width:150px; height:120px; background-color:#e0e0e0;">

      A positioned area with text</div>

   <script>
```

```javascript
 const image = document.getElementById("idImage");

      document.getElementById("idChange").addEventListener("click", change);

      document.getElementById("idAnimate").addEventListener("click",

         function() { reference = setInterval(animate, 20); } );
```

```html
 </script>

</body></html>
```

**清单 8.5**　css_position.htm 文件，下半部分

图片具有`style`属性。如果没有 CSS 的`position`属性，CSS 的`top`和`left`属性将不起作用。`div`容器还分别设置了 CSS 的`width`和`height`属性用于宽度和高度，以及`background-color`用于背景颜色。

定位元素在文档中独立于非定位元素。它们可以遮盖其他元素。`div`容器在代码中定义于图片之后，因此，加上其位置和大小，`div`容器部分遮盖了图片。

`image`变量引用了图片。第一个事件处理程序将点击“Change”按钮与`change()`函数关联起来，而点击“Animate”按钮则启动一个时间控制过程，以动画方式移动图片。

现在，来看程序的上半部分，包含 JavaScript 代码：

```html
... <head> ...

   <script>
```

```javascript
 function change()
      {
         image.style.top = "130px";
         image.style.left = "220px";
      }

      let reference, imTop = 80, imLeft = 120;

      function animate()
      {
         if (imTop >= 130)
            clearInterval(reference);
         else
         {
            imTop++;
            imLeft += 2;
            image.style.top = imTop + "px";
            image.style.left = imLeft + "px";
         }
      }
```

```html
 </script>

</head>

...
```

**清单 8.6**　css_position.htm 文件，上半部分

`change()`函数为`style`属性的`top`和`left`子属性赋予新值。这些值位于字符串中，并包含`px`单位。这样，图片就从默认位置移动到了另一个位置。

`reference`变量引用了时间控制过程。`imTop`和`imLeft`变量分别存储了`top`和`left`子属性的两个数值，其初始值与图片`style`属性中设定的值一致。

在`animate()`函数中检查当前位置。`top`子属性的值`130`对应最终位置，一旦达到该值，时间控制过程就会终止。如果尚未达到，则每次运行`animate()`函数时，图片会向下移动 1 像素，向右移动 2 像素。数值后面会附加`px`单位。

位置更改后，图片位于右下角，如图 8.5 所示。

![更改位置后](img/img-f8.5.html)

**图 8.5**　更改位置后

### 8.2.2　大小

CSS 的`width`和`height`属性用于定义元素的大小。文档中有一张定位图片（参见图 8.6）。

更改大小后，图片如图 8.7 所示。

![定位元素](img/img-f8.6.html)

**图 8.6**　定位元素

![更改大小后](img/img-f8.7.html)

**图 8.7**　更改大小后

以下是程序的第一部分：

```html
...

<body>

   <p><input id="idChange" type="button" value="Change">

      <input id="idAnimate" type="button" value="Animate"></p>

    <img src="im_paradise.jpg" alt="Paradise" id="idImage"

        style="position:absolute; top:60px; left:20px;

               width:160px; height:120px;">

   <script>
```

```javascript
 const image = document.getElementById("idImage");

      document.getElementById("idChange").addEventListener("click", change);

      document.getElementById("idAnimate").addEventListener("click",

         function() { reference = setInterval(animate, 20); } );
```

```html
 </script>

</body></html>
```

**清单 8.7**　css_size.htm 文件，下半部分

图像使用 CSS 属性`width`和`height`以 160 × 120 像素的尺寸显示。在这种情况下，这也对应于原始尺寸。对图像的引用以及事件处理程序与第 8.2.1 节中的相同。

现在，这是程序的上半部分，包含 JavaScript 代码：

```html
... <head> ...

   <script>
```

```javascript
 function change()
      {
         image.style.width = "240px";
         image.style.height = "180px";
      }

      let reference, imWidth = 160, imHeight = 120;

      function animate()
      {
         if (imWidth >= 240)
            clearInterval(reference);
         else
         {
            imWidth++;
            imHeight += 0.75;
            image.style.width = imWidth + "px";
            image.style.height = imHeight + "px";
         }
      }
```

```html
 </script>

</head>

...
```

**清单 8.8**　css_size.htm 文件，上半部分

`change()`函数为`style`属性的`imWidth`和`imHeight`子属性赋予新值。

对于动画，`imWidth`和`imHeight`变量包含这两个子属性的数值。在`animate()`函数中，`imWidth`变量以 1 为增量变化，直到达到 240。为了保持图像的宽高比，`imHeight`变量仅以 0.75 为步长变化。

### 8.2.3　Z 方向上的位置

你可以通过使用`z-index` CSS 属性来影响已定位元素在 z 方向上的位置。如果不进行设置，`z-index`的值为 0，但此时该元素至少位于未定位元素的前面。

z 方向上，值较高的元素位于值较低的元素前面，而值为负的元素甚至位于未定位元素的后面。

你可以在图 8.8 中看到一个示例。

![CSS Z-Index 属性](img/img-f8.8.html)

**图 8.8**　CSS Z-Index 属性

文档中包含三个不同颜色的`div`容器，它们被定位并部分重叠。`z-index` CSS 属性具有不同的值：`-1`、`2`或`3`，这导致了 z 方向上的顺序。`z-index` CSS 属性值为`-1`的`div`容器被一个未定位的元素部分覆盖。

以下是程序的第一部分：

```html
...

<body>

   <p><input id="idChange" type="button" value="Change"></p>

   <p style="background-color:#c0c0c0; width:80px; height:80px;">

      Without position</p>

   <div style="position:absolute; top:100px; left:100px; width:80px;

         height:80px; z-index:3; background-color:#f0f0f0;">

      3 3 3 3 3 3 3 3 3 3</div>

   <div id="idArea" style="position:absolute; top:70px; left:70px;

         width:80px; height:80px; z-index:2; background-color:#d0d0d0;">

      2 2 2 2 2 2 2 2 2 2</div>

   <div style="position:absolute; top:40px; left:40px; width:80px;

         height:80px; z-index:-1; background-color:#e0e0e0;">

      -1 -1 -1 -1 -1 -1 -1 -1 -1 -1 </div>

   <script>
```

```javascript
 const area = document.getElementById("idArea");

      document.getElementById("idChange").addEventListener("click", change);
```

```html
 </script>

</body></html>
```

**清单 8.9**　css_zindex.htm 文件，下半部分

`div`容器的定义顺序无关紧要，因为它们都具有`z-index` CSS 属性的值。`area`变量引用了`z-index` CSS 属性值为`2`的`div`容器，点击 Change 按钮会调用`change()`函数。

现在，这是程序的上半部分，包含 JavaScript 代码：

```html
... <head> ...

   <script>
```

```javascript
 function change()
      {
         area.style.zIndex = 4;
         area.firstChild.nodeValue = "4 4 4 4 4 4 4 4 4 4";
      }
```



</script>

</head>

...

```
**清单 8.10** css_zindex.htm 文件，上半部分
```

`change()`函数为`style`属性的`zIndex`子属性赋予新值 4。这意味着该`div`容器位于最前面，可能会遮挡程序中的其他`div`容器和未定位元素（参见图 8.9）。`div`容器的文本内容也相应更改。

![更改 Z 方向位置后](img/img-f8.9.html)

**图 8.9** 更改 Z 方向位置后

### 8.2.4 透明度

你可以通过使用`opacity` CSS 属性来设置元素的透明度。可以输入 0.0 到 1.0 之间的任意值。默认值 1.0 表示元素不透明（即无透明度），这意味着其 z 方向后面的元素将不可见。`opacity`的值越接近 0.0，元素越透明：值为 0.0 时完全透明，因此不可见。

在图 8.10 中，你可以看到一个`div`容器中的文字，该容器未设置透明度。此外，还显示了另外三个`div`容器，它们设置了不同的透明度值。

![使用 Opacity 的透明度](img/img-f8.10.html)

**图 8.10** 使用 Opacity 的透明度

以下是程序的第一部分：

```
...

<body>

   <p><input id="idChange" type="button" value="Change">

      <input id="idAnimate" type="button" value="Animate"></p>

   <div id="idArea" style="top:100px; left:20px; width:330px;

      height:20px;">No setting for transparency</div>

   <div style="top:60px; left:50px;  opacity:0.2;">0.2</div>

   <div style="top:60px; left:150px; opacity:0.5;">0.5</div>

   <div style="top:60px; left:250px; opacity:1.0;">1.0</div>

   <script>
```

```
const area = document.getElementById("idArea");

      document.getElementById("idChange").addEventListener("click", change);

      document.getElementById("idAnimate").addEventListener("click",

         function() { reference = setInterval(animate, 20); } );
```

```
</script>

</body></html>
```

**清单 8.11** css_transparency.htm 文件，下半部分

三个方形`div`容器的`opacity` CSS 属性分别被设置为 0.2、0.5 和 1.0。

`area`变量引用了包含文本`No setting for transparency`的`div`容器，点击 Change 和 Animate 按钮会分别调用`change()`和`animate()`函数。

接下来是程序的上半部分，包含 JavaScript 代码：

```
... <head> ...

   <style>
```

```
div {position:absolute; width:80px; height:80px;

           background-color:#c0c0c0;}
```

```
<style>

   <script>
```

```
function change()

      {

         area.style.opacity = 0.4;

      }

      let reference, value = 1.0;

      function animate()

      {

         if (value <= 0.0)

           clearInterval(reference);

         else

         {

           value -= 0.01;

           area.style.opacity = value;

           area.firstChild.nodeValue = "Transparency " + value.toFixed(2);

         }

      }
```

```
</script>

</head>

...
```

**清单 8.12** css_transparency.htm 文件，上半部分

首先，为`div`容器设置了一些常见的 CSS 属性。`change()`函数将值 0.4 赋给`style`属性的`opacity`子属性（参见图 8.11）。

![透明度变化后](img/img-f8.11.html)

**图 8.11** 透明度变化后

对于动画，`value`变量包含该子属性的数值。`animate()`函数以 0.01 的增量将`value`变量从 1.0 更改为 0.0。动画开始时，元素完全不透明，结束时完全透明。当前透明度显示为`div`容器的文本内容。

### 8.2.5 可见性

透明度为 0.0 会使元素不可见，你也可以通过使用`visibility` CSS 属性来影响元素的可见性。`visible`值使元素可见，而`hidden`值使其不可见。不可见的元素在文档中占据空间，但不会响应`mouseover`或`mouseout`等事件。

以下示例中的文档（参见图 8.12）包含两张图片。第一张图片在开始时不可见。当鼠标悬停在可见图片上时，另一张图片变为不可见。如果鼠标离开可见图片的区域，另一张图片变为可见（参见图 8.13）。

![使用 Visibility 属性控制可见性](img/img-f8.12.html)

**图 8.12** 使用 Visibility 属性控制可见性

![离开第二张图片区域后](img/img-f8.13.html)

**图 8.13** 离开第二张图片区域后

程序如下：

```
...

<body>

   <img src="im_tree.jpg" alt="Tree" id="idTree" style="visibility:hidden;">

   <img src="im_solar_eclipse.jpg" alt="SolarEclipse" id="idSolarEclipse">

   <script>
```

```
const tree = document.getElementById("idTree");

      const se = document.getElementById("idSolarEclipse");

      tree.addEventListener("mouseover",

         function() { se.style.visibility = "hidden"; });

      tree.addEventListener("mouseout",

         function() { se.style.visibility = "visible"; });

      se.addEventListener("mouseover",

         function() { tree.style.visibility = "hidden"; });

      se.addEventListener("mouseout",

         function() { tree.style.visibility = "visible"; });
```

```
</script>

</body></html>
```

**清单 8.13** css_visibility.htm 文件

程序创建了对两张图片的引用。通过`mouseover`和`mouseout`事件，使用匿名函数设置另一张图片的`style`属性的`visibility`子属性的值。

### 8.2.6 颜色

你可以通过`background-color` CSS 属性设置元素的背景颜色，通过`color` CSS 属性设置元素的文本颜色。有多种选择颜色的方法，但特别对于动画，我们建议使用`rgb()`公式来赋值。颜色的红、绿、蓝分量可以使用 0 到 255 之间的值。

在图 8.14 中，你可以看到深灰色`div`容器中的浅灰色文字。

![文本颜色和背景颜色](img/img-f8.14.html)

**图 8.14** 文本颜色和背景颜色

程序的第一部分如下：

```
...

<body>

   <p><input id="idChange" type="button" value="Change">

      <input id="idAnimate" type="button" value="Animate"></p>

   <div id="idArea" style="position:absolute; top:50px; left:50px;

         width:100px; height:100px; color:rgb(192,192,192);

         background-color:rgb(64,64,64);">Light gray on dark gray</div>

   <script>
```

```
const area = document.getElementById("idArea");

      document.getElementById("idChange").addEventListener("click", change);

      document.getElementById("idAnimate").addEventListener("click",

         function() { reference = setInterval(animate, 20); } );
```

```
</script>

</body></html>
```

**清单 8.14** css_color.htm 文件，下半部分

值 192/192/192 对应浅灰色，值 64/64/64 对应深灰色。`div`容器包含当前颜色设置的信息。`area`变量引用了定位的`div`容器，点击 Change 按钮调用`change()`函数，点击 Animate 按钮调用一个匿名函数，该函数调用`setInterval()`方法。

接下来是程序的上半部分，包含 JavaScript 代码：

```
... <head> ...

   <script>
```

```
function change()

      {

         area.style.color = "rgb(64,64,64)";

         area.style.backgroundColor = "rgb(192,192,192)";

         area.firstChild.nodeValue = "Dark gray on light gray";

      }

      let reference, red = 64, green = 64, blue = 64;

      function animate()

      {

         if (red >= 192)

         {

            clearInterval(reference);

            area.firstChild.nodeValue = "Dark gray on light gray";

         }

         else

         {

            red++;

            green++;

            blue++;

            area.style.color = "rgb(" + (256-red)

               + "," + (256-green) + "," + (256-blue) + ")";

            area.style.backgroundColor =

               "rgb(" + red +", "+ green +", "+ blue + ")";

         }

      }
```

```
</script>

</head>

...
```

**清单 8.15** css_color.htm 文件，上半部分

`change()`函数为`style`属性的`color`和`backgroundColor`子属性赋予新值（参见图 8.15）。它通过字符串中的`rgb()`公式来赋值。`div`容器也包含了新内容：新的颜色设置。

在动画中，`red`、`green`和`blue`变量分别存储颜色分量的三个数值。`animate()`函数将这些比例从 64 到 192 以 1 为增量进行变化。这些值直接用于改变背景颜色，而文本颜色则按相反顺序变化。由于使用了三个变量，你可以为动画设置任意的起始和结束颜色。

![更改颜色后](img/img-f8.15.html)

**图 8.15** 更改颜色后

## 8.3 其他选项

本节包含使用前述属性的其他程序。

### 注意

`style`属性的子属性名称与相关 CSS 属性的名称非常相似。如果 CSS 属性名称包含连字符，则连字符会被省略，且后面的字母大写。以下两个示例：`border-width`（总边框宽度）变为`borderWidth`，`border-top-width`变为`borderTopWidth`。如果 CSS 属性的值由多个数值组成，则在 JavaScript 中表示为字符串。

### 8.3.1 图像切换时的透明度

在以下程序中，两张图像被放置在同一位置。第一张图像显示时不设置透明度（参见图 8.16），第二张图像的透明度为 0.0（即初始时完全透明）。

点击“动画”按钮会改变透明度值。第一张图像逐渐变得透明，第二张图像逐渐变得不透明（参见图 8.17）。这样便实现了动画图像切换——最终只有第二张图像可见（参见图 8.18）。

![第一张图像可见，第二张图像透明](img/img-f8.16.html)

**图 8.16** 第一张图像可见，第二张图像透明

![从第一张图像过渡到第二张图像](img/img-f8.17.html)

**图 8.17** 从第一张图像过渡到第二张图像

![第二张图像可见，第一张图像透明](img/img-f8.18.html)

**图 8.18** 第二张图像可见，第一张图像透明

以下是程序：

```
... <head> ...

   <script>

let reference, value = 1;

      function animate()

      {

         if (value <= 0)

            clearInterval(reference);

         else

         {

            value -= 0.01;

            pa.style.opacity = value;

            se.style.opacity = 1 - value;

         }

      }

</script>

</head>

<body>

   <p><input id="idAnimate" type="button" value="Animate"></p>

   <img src="im_paradise.jpg" alt="Paradise" id="idParadise"

        style="position:absolute; top:60px; left:20px;">

   <img src="im_solar_eclipse.jpg" alt="SolarEclipse" id="idSolarEclipse"

        style="position:absolute; top:60px; left:20px; opacity:0.0;">

   <script>

const pa = document.getElementById("idParadise");

      const se = document.getElementById("idSolarEclipse");

      document.getElementById("idAnimate").addEventListener("click",

         function() { reference = setInterval(animate, 20); } );

</script>

</body></html>
```



**清单 8.16**　`css_transparency_image.htm` 文件

两张图像均位于 60 × 20 像素的位置，尺寸为 160 × 120 像素。在第二张图像中，`opacity` CSS 属性的值设置为 0.0，并设置了两张图像的链接以及按钮的事件处理程序。

`value` 变量用于设置两张图像的 `style` 属性的 `opacity` 子属性。该变量的初始值为 1.0，以 0.01 为增量递减，最终为 0.0。该值直接赋给第一张图像，而第二张图像的透明度则按相反方向变化，因此需要预先计算差值 `1 - value`。

### 8.3.2 菜单的可见性

我们利用可见性来动态显示带有子菜单的菜单。在图 8.19 中，可以看到菜单的初始状态。当鼠标悬停在某个菜单项上时，对应的子菜单变为可见（参见图 8.20），只有当鼠标离开关联菜单或显示的子菜单区域时，子菜单才会再次隐藏。

![菜单初始状态](img/img-f8.19.html)

**图 8.19**　菜单初始状态

![可见的子菜单](img/img-f8.20.html)

**图 8.20**　可见的子菜单

以下是示例程序：

```
... <head> ...

   <script> 

 function subOn(x)

      {

         if(x==1)

            sub1.style.visibility = "visible";

         else

            sub2.style.visibility = "visible";

      }

      function subOff(x)

      {

         if(x==1)

            sub1.style.visibility = "hidden";

         else

            sub2.style.visibility = "hidden";

      } 

 </script>

   <style> 

 div {position:absolute; width:200px; height:20px; padding:5px;

           border-top:solid 1px #000000; border-bottom:solid 1px #000000; 

           background-color:#f0f0f0;}

      .sub    {visibility:hidden; height:60px; border-top-width:0px;}

      a:link  {color:#000000; text-decoration:none;}

      a:hover {background-color:#d0d0d0;} 

 <style>

</head>

<body>

   <div id="idMenu1" style="top:20px; left:20px;">Menu 1</div>

   <div id="idMenu2" style="top:20px; left:220px;">Menu 2</div>

   <div id="idSub1" class="sub" style="top:50px; left:20px;">

      <a href="#">Submenu 1 A</a><br>

      <a href="#">Submenu 1 B</a><br>

      <a href="#">Submenu 1 C</a>

   </div>

   <div id="idSub2" class="sub" style="top:50px; left:220px;">

      <a href="#">Submenu 2 A</a><br>

      <a href="#">Submenu 2 B</a><br>

      <a href="#">Submenu 2 C</a>

   </div>

   <script> 

 const menu1 = document.getElementById("idMenu1");

      menu1.addEventListener("mouseover", function() { subOn(1); });

      menu1.addEventListener("mouseout",  function() { subOff(1); });

      const menu2 = document.getElementById("idMenu2");

      menu2.addEventListener("mouseover", function() { subOn(2); });

      menu2.addEventListener("mouseout",  function() { subOff(2); });

      const sub1 = document.getElementById("idSub1");

      sub1.addEventListener("mouseover", function() { subOn(1); });

      sub1.addEventListener("mouseout",  function() { subOff(1); });

      const sub2 = document.getElementById("idSub2");

      sub2.addEventListener("mouseover", function() { subOn(2); });

      sub2.addEventListener("mouseout",  function() { subOff(2); }); 

 </script>

</body></html> 
```

**清单 8.17**　`css_visibility_menu.htm` 文件

主菜单项和子菜单都位于具有以下属性的 `div` 容器中：

- 尺寸为 200 × 20 像素
- 一条上边缘和一条下边缘
- 浅灰色背景
- 距边缘五像素的内边距

子菜单的属性通过 `sub` 类进行添加或覆盖：高度改为 60 像素，移除顶部边框，最重要的是，它们不可见。

子菜单中的菜单项是超链接，可用于调用其他页面等。对于这些超链接，定义了以下属性：文本颜色为黑色，无下划线。当鼠标悬停在某个超链接上时，背景颜色会发生变化。

菜单和子菜单在文档中相互定位，并且 `sub` 类被分配给子菜单。

当鼠标悬停在某个主菜单项上时，会调用 `subOn()` 函数，并传递参数 1 或 2。在 `subOn()` 函数内部，将对应子菜单的 `style` 属性的 `visibility` 子属性设置为 `visible`。

相反，当鼠标离开某个主菜单项时，会调用 `subOff()` 函数，并传递相同的参数。在 `subOff()` 函数内部，将对应子菜单的 `style` 属性的 `visibility` 子属性设置为 `hidden`。

悬停或离开某个子菜单会产生相同的结果。否则，一旦鼠标从关联的主菜单项移动到子菜单，相关的子菜单就会消失。

位置的选择使得子菜单略微重叠主菜单项。否则，一旦鼠标离开关联的主菜单项，子菜单就会变得不可见。

### 8.3.3 动画投掷

在本节的可下载资料中，你可以找到 `css_throw.htm` 程序，其中包含许多解释性注释作为额外内容。该程序让你模拟向目标投掷球。

为此，你可以调整投掷与地面的角度以及球在投掷开始时的速度。程序考虑了重力的影响，使球的轨迹呈抛物线状。你还可以将目标放置在固定或随机位置（参见图 8.21）。

球在 `time` 之后在 x 和 y 方向上的 `轨迹` 由两个物理公式确定（另请参见 [`en.wikipedia.org/wiki/Projectile_motion`](https://en.wikipedia.org/wiki/Projectile_motion)）：

```
sx(t) = s0 + v0 * cos(w) * t

sy(t) = s0 + v0 * sin(w) * t + 0.5 * a0 * t * t 
```

![向目标投掷球](img/img-f8.21.html)

**图 8.21**　向目标投掷球

以下是物理公式中各个项的更多信息：

- `s[0]` 是投掷开始时的轨迹。该轨迹对应于起点的坐标。
- `v[0]` 是投掷开始时的速度（即输入字段中设置的速度）。速度在 x 方向和 y 方向上的分量可以根据角度 `w` 使用余弦和正弦计算。角度在输入字段中设置。
- `a[0]` 是投掷开始时的加速度，取决于重力。它只存在于 y 方向。

公式中的表达式在程序中赋予了因子，以使运动看起来更自然。

# 9 使用 SVG 的二维图形和动画

你可以使用 SVG 在浏览器中显示二维矢量图形和动画。

可缩放矢量图形（SVG）是一种基于 XML 的语言格式，可用于创建二维矢量图形。你可以通过描述创建矢量图形；它占用很少的存储空间，并且可以轻松更改而不会损失任何质量（例如，关于其位置、大小或旋转）。

SVG 可以包含动画，并且无需额外程序即可在现代浏览器中显示。使用 JavaScript 和你在第 5 章中学到的 DOM，你可以访问、更改或添加 SVG 的各个元素。

你可以将 SVG 代码直接嵌入到 HTML 代码中，或者将其保存在单独的 SVG 文件中，该文件提供一个（可能带有动画的）图像，你可以使用 `object` HTML 标签将其作为多媒体对象插入到不同 HTML 文档的任何位置。本章仅展示 SVG 广泛可能性的一部分。

本章中的程序基于 SVG 1.1 标准，该标准由万维网联盟（W3C）于 2011 年 8 月发布。自 2016 年 9 月起，已有 SVG 2 标准的草案，但迄今为止，各浏览器仅部分实现了该标准。

## 9.1 创建 SVG 文件

在本节中，我们将创建第一个 SVG 文件并将其嵌入到 HTML 文档中。该 SVG 有一个用于说明的边框，并在特定位置包含一个黑色矩形（参见图 9.1）。

![带有 SVG 的 HTML 文档](img/img-f9.1.html)

**图 9.1**　带有 SVG 的 HTML 文档

以下是 SVG 文件的代码：

```
<svg xmlns="https://www.w3.org/2000/svg" width="400" height="150">

   <!-- 矩形 -->

   <rect x="50" y="20" width="100" height="50" />

</svg> 
```

**清单 9.1**　`svg_insert.svg` 文件

`svg` 标签引入 SVG 代码。根据第 5 章中的 DOM，此标签是根节点，所有子节点（图形元素）都嵌入其中。子节点又可以拥有子节点，依此类推，每个节点也可以拥有属性节点。

`xmlns` 属性使用指定的值定义所使用的 SVG 元素来自的 XML 命名空间，`width` 和 `height` 属性确定图形的宽度和高度（以像素为单位）。注释的创建方式与 HTML 相同，使用 `<!--` 和 `-->`。

如果 SVG 元素没有子元素（即没有子节点），则不需要结束标签。在这种情况下，开始标签必须以 `/>` 结束。子元素可以是例如引用该 SVG 元素的动画。

`rect` 标签创建一个矩形，通过其左上角的 x 和 y 坐标进行定位。这些值相对于图形的左上角，矩形的大小通过 `width` 和 `height` 属性定义。如果没有提供更多信息，SVG 元素将被填充并显示为黑色。

现在，以下是 HTML 文件的代码：

```
...

<body>

   <p>SVG 图形上方</p>

   <p><object data="svg_insert.svg" type="image/svg+xml"

         width="400" height="150" style="border:1px solid black;">

      此处为 SVG 图形

   </object></p>

   <p>SVG 图形下方</p>

</body></html> 
```

**清单 9.2**　`svg_insert.htm` 文件

你可以通过使用 `object` HTML 标签将 SVG 文件作为多媒体对象插入到 HTML 文档中。你也可以使用 `img` HTML 标签，但那样的话，现有的动画将不会执行。

`data` 属性引用 SVG 文件，`type` 属性指文件类型。`width` 和 `height` 属性定义 HTML 文档中多媒体对象的大小，此处为了清晰起见，添加了细黑边框。只有当浏览器无法显示 SVG 图形时，“这是一个 SVG 图形”文本才可见。

## 9.2 基本形状

第一个基本形状显示在 `svg_basic_shapes.htm` 文件中：矩形（见图 9.2）、圆形和椭圆（见图 9.3）以及线条、折线和多边形（见图 9.4）。

在本章及本章其他示例中，SVG 代码直接嵌入在 HTML 代码中。你可以利用第 9.1 节学到的知识，将所有图形的 SVG 代码保存下来，也可以保存在单独的 SVG 文件中。

### 9.2.1 矩形

以下是图 9.2 中矩形的代码：

```
...

<body>

   <svg xmlns="https://www.w3.org/2000/svg" width="600"

         height="300" style="border:1px solid black;">

      <rect x="50"  y="20" width="100" height="50" />

      <rect x="200" y="20" width="100" height="50" rx="10" ry="10"

         fill="#bbbbbb" stroke="#000000" stroke-width="2" />

      <rect x="350" y="20" width="100" height="50" />

      <rect x="355" y="25" width="50"  height="25" fill="#ffffff" />

...

   </svg>

</body></html> 
```

**清单 9.3**　`svg_basic_shapes.htm` 文件、结构和矩形

![矩形](img/img-f9.2.html)

**图 9.2**　矩形

SVG 容器嵌入在 HTML 文档的 `body` 中，并且可以被其他 HTML 标签和文本包围。选择图形大小为 600 × 300 像素，边框线直接分配给 SVG 元素。

我们在第 9.1 节中描述了如何创建一个简单的黑色矩形。

通过使用 `rx` 和 `ry` 属性，你可以给第二个矩形添加圆角。你可以使圆角在 x 和 y 方向上不同，并且可以使用 `fill` 属性为 SVG 元素定义填充颜色。在我们的示例中，颜色是灰色，但默认颜色是黑色。

`stroke` 属性定义 SVG 元素边框线的颜色（此处为黑色），并确保其显示。SVG 元素的边框线默认宽度为 1 像素；你可以使用 `stroke-width` 属性选择 2 像素的值。

一个 SVG 元素可以完全或部分覆盖先前在代码中创建的另一个 SVG 元素。小的白色矩形覆盖了大黑色矩形的一部分。

### 9.2.2 圆形和椭圆

现在，以下是图 9.3 中圆形和椭圆的代码：

```
... 

      <circle cx="80"  cy="130" r="30" />

      <circle cx="180" cy="130" r="30" stroke="#000000"

         stroke-width="2" fill="#bbbbbb" />

      <circle cx="280" cy="130" r="30" />

      <circle cx="295" cy="130" r="30" fill="#ffffff" />

      <ellipse cx="400" cy="130" rx="60" ry="30"/>

... 
```

**清单 9.4**　`svg_basic_shapes.htm` 文件、圆形和椭圆

![圆形和椭圆](img/img-f9.3.html)

**图 9.3**　圆形和椭圆

`circle` 标签创建一个圆形，你使用 `cx` 和 `cy` 属性定位其中心的 x 和 y 坐标。通过使用 `r` 属性定义半径来确定圆形的大小，如果不做进一步输入，该 SVG 元素也将被填充为黑色，如第一个圆形所示。

为第二个圆形定义了填充颜色以及边框线的颜色和线宽。

通过用一个白色圆形覆盖黑色圆形的右侧部分，创建了“月牙”。

`ellipse` 标签创建一个椭圆。与圆形一样，你使用 `cx` 和 `cy` 属性定位椭圆中心的坐标。椭圆有两个半径，你通过 `rx` 属性确定 x 方向的半径，通过 `ry` 属性确定 y 方向的半径。如果两个半径相同，那么椭圆实际上就是一个圆形。

### 9.2.3 线条、折线和多边形

以下是图 9.4 中线条、折线和多边形的代码：

```
... 

      <line x1="20" y1="190" x2="20" y2="250"

            stroke="#000000" stroke-width="2" />

      <polyline points=" 50,250  80,190 110,250" />

      <polyline points="150,250 180,190 210,250"

         stroke="#000000" stroke-width="2" fill="none" />

      <polyline points="250,250 280,190 310,250"
```



```html
stroke="#000000" stroke-width="2" fill="#bbbbbb" />

<polygon points="350,250 380,190 410,250"
   stroke="#000000" stroke-width="2" fill="#bbbbbb" />
```

**清单 9.5** `svg_basic_shapes.htm` 文件、线条、折线和多边形

`line` 标签创建一条从 `x1`、`y1` 开始到 `x2`、`y2` 结束的线条。`stroke` 属性定义线条的颜色并确保其显示。默认情况下，线条宽度为 1 像素，但你可以使用 `stroke-width` 属性选择 2 像素的值。

![线条、折线和多边形](img/img-f9.4.html)

**图 9.4** 线条、折线和多边形

折线是一组线条，你将各个点（每个点由一对 x 和 y 坐标指定）相互连接起来形成折线。多边形也是一组线条，区别在于最后一个点与第一个点相连，从而使折线闭合。在这个程序中，你总是将三个点相互连接形成一个三角形，该三角形可以是折线或多边形。

`polyline` 标签创建折线，`polygon` 标签创建多边形。你使用 `points` 属性定位各个点，并依次指定 x 和 y 坐标对。允许使用空格和逗号作为分隔符，为了清晰起见，我建议用逗号分隔一对中的 x 和 y 坐标。不同的坐标对之间应该用空格分隔。

如果不输入更多信息，该 SVG 元素也会被填充为黑色，如第一个折线所示。

如果折线或多边形不应该被填充，你必须指定 `fill` 属性为 `none` 值。在这种情况下，你应该使用 `stroke` 属性，以便折线或多边形可见，就像第二个折线一样。

第三个折线有灰色填充，并且独立地有黑色边框。

最右侧的多边形构造方式与相邻的第三条折线类似，但第三个点会自动连接到第一个点，从而使线条闭合。

如果一条折线只包含两个点，或者折线的所有点都位于同一条直线上，则不会形成区域。在这种情况下，无法进行填充，并且如果未为此类线条的 `stroke` 属性输入值，则线条将完全不可见。这也适用于路径（第 9.3 节）。

## 9.3 路径

路径是一种线条，它不仅可由直线组成，还可由曲线组成。路径也可以中断，你可以使用在图形上移动的绘图笔创建各种线条形状。你可以从路径创建所有基本形状。

你可以使用绝对坐标或相对坐标创建路径的元素：

- 绝对坐标由大写字母的规范引入，与之前已知的元素一样，它们参考图形左上角的零点。
- 相对坐标由小写字母的规范引入，它们参考路径的前一个元素。它们通常比绝对坐标更容易处理。

你可以像基本形状一样用颜色填充路径。`svg_path.htm` 文件包含一些示例。

### 9.3.1 填充的路径

首先，我们来看一下图 9.5 中四个填充路径的代码：

```html
...

<body>

   <svg xmlns="https://www.w3.org/2000/svg" width="600px"
         height="250px" style="border:1px solid black;">

      <path d="M  50,20 L 80,50 L 80,80 L 50,80" />

      <path d="M 120,20 L 150,50 V 80 H 120" />

      <path d="M 190,20 l 30,30 l 0,30 l -30,0" />

      <path d="M 260,20 l 30,30 v 30 h -30" />

...

   </svg>

</body></html>
```

**清单 9.6** `svg_path.htm` 文件，填充的路径

![填充的路径](img/img-f9.5.html)

**图 9.5** 填充的路径

`path` 标签创建一条路径，你使用 `d` 属性定位各个点。`d` 属性的值中可以出现以下规范：

- `M`，表示移动到：此规范将绘图笔移动到下一对绝对坐标，而不绘制线条。可用于实现线条的中断。
- `m`：此规范与 `M` 类似，但将绘图笔移动到下一对相对坐标。
- `L`，表示画线到：此规范绘制一条线到下一对绝对坐标。
- `l`：此规范与 `L` 类似，但绘制一条线到下一对相对坐标。
- `V`，表示垂直：此规范绘制一条垂直线到下一个绝对 y 坐标。
- `v`：此规范与 `V` 类似，但绘制一条垂直线到下一个相对 y 坐标。正值将绘图笔向下移动，负值将其向上移动。
- `H`，表示水平：此规范绘制一条水平线到下一个绝对 x 坐标。
- `h`：此规范与 `H` 类似，但绘制一条水平线到下一个相对 x 坐标。正值将绘图笔向右移动，负值将其向左移动。

四个填充路径外观相同，但结构不同：

- 第一个路径使用 `M` 或 `L` 使用绝对坐标。
- 第二个路径使用 `M`、`L`、`V` 和 `H` 使用绝对坐标。
- 第三个路径使用 `M` 作为起点，使用 `l` 作为后续的相对坐标。
- 第四个路径使用 `M` 作为起点，使用 `l`、`v` 和 `h` 作为后续的相对坐标。

第四个路径比之前的路径更易读。如果未输入更多信息，此 SVG 元素也会被填充并显示为黑色。

### 9.3.2 组和路径

以下是图 9.6 中组和三个未填充路径的代码：

```html
...

      <g stroke="#000000" stroke-width="2" fill="none">

         <path d="M 330,20 l 30,30 v 30 h -30" />

         <path d="M 400,20 l 30,30 v 30 h -30 z" />

         <path d="M 470,20 l 30,30 m 0,30 h -30" />

...

      </g>

...
```

**清单 9.7** `svg_path.htm` 文件，未填充的路径和组

![未填充的路径](img/img-f9.6.html)

**图 9.6** 未填充的路径

你使用 `g` 标签对要分配共同属性和值的元素进行分组。`fill` 属性的 `none` 值表示此组中的三个未填充路径和其他元素不会被填充。你使用 `stroke` 属性使折线可见。这三个路径结构相似，但存在细微差别：

- 第一个路径使用 `M` 作为起点，使用 `l`、`v` 和 `h` 作为后续的相对坐标。
- 第二个路径以 `z` 规范结束，你使用它来闭合折线（即，从最后一个元素连接到起点）。
- 在第三个路径中，你使用了一次 `m` 规范而不是 `v` 规范。这确保笔移动到下一个点而不绘制线条，因此路径显示为中断。然而，它仍然是一个逻辑上连续的路径。

### 9.3.3 带曲线的路径

带曲线的路径结构复杂。有椭圆弧以及二次和三次贝塞尔曲线。在本介绍中，我将只讨论椭圆弧。

以下是图 9.7 中路径的代码，该路径总共包含三条曲线：

```html
...

      <g stroke="#000000" stroke-width="2" fill="none">

...

         <path d="M 50,120
                  v 60
                  a 30,30 0 0 0 60,0
                  v -30
                  a 30,30 0 0 1 30,-30
                  h 60
                  a 30,30 0 1 1 -30,30" />

      </g>

...
```

**清单 9.8** `svg_path.htm` 文件，带曲线的路径

![带曲线的路径](img/img-f9.7.html)

**图 9.7** 带曲线的路径

为了清晰起见，`d` 属性的各个条目被上下排列。`A` 或 `a` 规范创建一条椭圆弧。总共需要七个值：

- 椭圆在 `x` 和 `y` 方向上的两个半径（另请参见第 9.2.2 节）。为简化起见，三个椭圆的两个半径值均选择相同，因此曲线呈圆形。
- 弧线绕 `x` 方向的旋转角度，以度为单位。这指定了弧线绕其 `x` 轴倾斜的度数。为简化起见，所有三条曲线均选择值 0，因此没有曲线发生倾斜。
- 一个值，用于确定弧线是从起点到终点沿短路径（值 = 0）还是长路径（值 = 1）绘制。此处，仅对第三条弧线选择长路径，以便它跨越四分之三的弧线绘制。
- 一个值，用于定义旋转方向（即弧线从起点到终点是逆时针 [值 = 0] 还是顺时针 [值 = 1] 运行）。此处，第二条和第三条曲线顺时针运行。
- 弧线终点的绝对（使用 `A` 的弧线）或相对（使用 `a` 的弧线）坐标。

## 9.4 动画

你可以使用动画更改 SVG 元素的属性。如同电影一样，这涉及位置、大小、颜色、透明度或其他属性的连续变化。

你可以确定动画的开始时间和持续时间。动画可以针对一个或多个 SVG 元素同时或顺序运行，并且可以由特定事件触发并按需重复。

### 9.4.1 过程

`svg_animation.htm` 文件包含一些动画示例。首先，你会看到两个带有灰色填充的矩形（参见图 9.8）。短暂时间后，第一个矩形的动画开始。它向下移动，然后移回起始位置并同时变高。最后，它变得几乎透明（参见图 9.9）。

![第一个动画，初始状态](img/img-f9.8.html)

**图 9.8** 第一个动画，初始状态

![第一个动画，最终状态](img/img-f9.9.html)

**图 9.9** 第一个动画，最终状态

点击第二个矩形会启动该元素的动画。它向下移动并同时变为白色（参见图 9.10），然后移回起始位置并同时变回灰色。整个过程重复一次。

![第二个动画，中间状态](img/img-f9.10.html)

**图 9.10** 第二个动画，中间状态

### 9.4.2 时间控制

以下是第一个矩形的时间控制动画的代码：

```html
...

<body>

   <svg xmlns="https://www.w3.org/2000/svg" width="400px"
         height="300px" style="border:1px solid black;">

      <g stroke="#000000" stroke-width="2" fill="#a0a0a0">

         <rect x="50" y="20" width="100" height="50">

            <animate attributeName="y"
               begin="1" dur="1" from="20" to="120" fill="freeze" />

            <animate attributeName="height"
               begin="2" dur="1" by="100" fill="freeze" />

            <animate attributeName="y"
               begin="2" dur="1" by="-100" fill="freeze" />

            <animate attributeName="opacity"
               begin="3" dur="1" from="1" to="0.2" fill="freeze" />

         </rect>

...

      </g>

   </svg>

</body></html>
```

**清单 9.9** `svg_animation.htm` 文件，第一个矩形的动画

两个矩形位于一个组中，该组定义了填充颜色和边框线的属性。四个不同的动画各自作为子节点从属于该矩形。

你使用 `animate` 标签为父元素创建动画，并使用 `attributeName` 属性定义要动画化的属性。在本例中，这些属性是用于垂直位置的 `y`、用于高度的 `height` 以及用于透明度的 `opacity`。

我在此仅介绍 SVG 元素的透明度属性，因为它在与动画关联时更清晰。位于部分或完全透明的其他 SVG 元素后面的 SVG 元素是可见的，相关 `opacity` 属性允许的值介于 0.0（完全透明）和默认值 1.0（完全不透明）之间。

`begin` 和 `dur`（duration 的缩写）属性定义了时间控制动画的开始时间和持续时间。这使你能够为过程编写脚本。默认情况下，值以秒为单位指定，在此示例中，每个动画持续一秒。开始时间的选择方式使得第一个动画首先发生，第二个和第三个动画紧随其后同时发生，第四个动画紧随其后。

你也可以使用特定单位的缩写来指定时间值。例如，`h` 表示小时单位（例如 `2h`），`min` 表示分钟单位（例如 `0.5min`），`s` 表示秒单位（例如 `3.5s`），`ms` 表示毫秒单位（例如 `500ms`）。

你使用 `from` 和 `to` 属性来确定动画属性的绝对起始值和结束值。为避免动画开始时发生突变，应将属性已有的值作为起始值。在此示例中，`y` 的值在第一个动画期间从 20 连续变化到 120，`opacity` 的值从 1.0 连续变化到 0.2。

你使用 `by` 属性来确定动画属性的相对变化。在此示例中，`height` 的结束值比起始值大 100，而第三个连续动画中 `y` 的结束值比起始值小 100。

动画的 `fill` 属性与填充无关，`freeze` 值确保值在动画结束时冻结。如果省略该属性或设置默认的 `remove` 值，则会重新设置属性的起始值。

### 9.4.3 事件控制

现在让我们看看第二个矩形的事件控制动画的代码：

```html
...

         <rect id="re2" x="200" y="20" width="100" height="50">

            <animate attributeName="y" begin="re2.click" dur="2"
               repeatCount="2" values="20;120;20" />

            <animate attributeName="fill" begin="re2.click" dur="2"
               repeatCount="2" values="#a0a0a0;#ffffff;#a0a0a0" />

         </rect>

...
```

**清单 9.10** `svg_animation.htm` 文件，第二个矩形的动画

该矩形具有 `id` 属性，此处值为 `re2`。需要唯一的 ID 才能将事件分配给 SVG 元素。两个不同的动画各自作为子节点从属于该矩形。

两个动画的 `begin` 属性值均为 `re2.click`，因此点击对应 ID 的矩形会同时启动两个动画。除了 `click`，还有 `mouseover`、`mouseout` 等其他事件标识符，正如你在第 4 章中已经看到的，但没有 `on` 前缀。

两个动画均持续 2 秒。`repeatCount` 属性定义了动画序列的次数，因此值为 `2` 并不意味着动画结束后还会再运行两次，而是总共运行两次。

如果动画从起始值经过多个中间值到达最终值，`values` 属性尤其有用。在此例中，`y` 的值首先从 `20` 连续变化到 `120`，然后再从 `120` 连续变化回 `20`。填充颜色的值从灰色开始，连续变化为白色，然后再连续变化回灰色。在这两种情况下，最终值都与起始值相同，因此可以省略带有 `freeze` 值的 `fill` 属性。

## 9.5 旋转

使用 `rotate` 语句旋转 SVG 元素属于变换（transformations）的范畴。我在这里介绍它，只是因为它在动画的上下文中更清晰。

除了旋转之外，还有其他类型的变换，这里不再赘述。你可以通过更改属性来实现它们，但需要一些额外的工作：

- 你可以使用 `translate` 语句通过其他位置规格来实现平移。
- 你可以使用 `scale` 语句通过其他尺寸规格来实现缩放。
- 你可以使用 `skewX` 和 `skewY` 语句通过其他形状规格来实现扭曲，但稍微复杂一些。

在 `svg_rotation.htm` 文件中，加载文档后你会看到三个灰色填充的矩形（参见图 9.11）。

![左前矩形的固定旋转](img/img-f9.11.html)

**图 9.11** 左前矩形的固定旋转

左侧的两个矩形上下重叠。上方的矩形相对于下方的矩形旋转了 30 度，旋转中心（更准确地说，是旋转轴穿过屏幕的点）是矩形的中心。你也可以定义其他旋转中心（例如，矩形的某个角点或左上角 SVG 图形的零点）。

片刻之后，右侧的矩形开始动画。它从 0 度的起始位置连续旋转到 30 度的结束位置（参见图 9.12）。

![右侧矩形动画旋转后](img/img-f9.12.html)

**图 9.12** 右侧矩形动画旋转后

代码如下：

```html
...

<body>

   <svg xmlns="https://www.w3.org/2000/svg" width="400px"
         height="200px" style="border:1px solid black;">

      <g stroke="#000000" stroke-width="2" fill="#a0a0a0">

         <rect x="50" y="75" width="100" height="50" />

         <rect x="50" y="75" width="100" height="50"
            transform="rotate(30, 100, 100)" />
```



```html
<rect x="250" y="75" width="100" height="50">
   <animateTransform attributeName="transform"
      type="rotate" begin="1" dur="2" from="0, 300, 100"
      to="30, 300, 100" fill="freeze" />
</rect>
</g>
</svg>
</body>
</html>
```

**清单 9.11** `svg_rotation.htm` 文件

这两个矩形位于一个组中，该组定义了填充和边框线的属性。

左侧上方的矩形具有 `transform` 属性。该属性的值指定了变换的类型，例如 `translate`、`scale`、`skewX`、`skewY` 或（本例中的）`rotate`，后面括号内是参数值。对于旋转，参数是旋转角度（以度为单位），然后是旋转中心的坐标。

动画是右侧矩形的子节点。使用 `animateTransform` 标签可以为父元素的变换创建动画，并且 `attributeName` 属性被赋予 `transform` 值。

对于旋转动画，`type` 属性被赋予 `rotate` 值。`begin`、`dur` 和 `fill` 属性的作用我们已经了解。`from` 和 `to` 属性的值的写法与上面相同：首先是旋转角度（以度为单位），然后是旋转中心的坐标。

## 9.6 SVG 与 JavaScript

借助 JavaScript 和你在第 5 章中了解的 DOM，你可以访问 SVG 图形的各个元素，修改它们或补充它们。

使用 `svg_event.htm` 中的程序，每次点击矩形时，都可以通过 JavaScript 将灰色矩形向右移动一点。你也可以直接在 SVG 中实现这一点，但我们将展示如何使用 JavaScript 注册与 SVG 元素相关的事件、读取其属性值并修改它们。

代码如下：

```html
... <head> ...
<script>
```

```javascript
function change()
{
   let xPos = parseInt(re.getAttribute("x"));
   xPos += 100;
   re.setAttribute("x", xPos);
}
```

```html
</script>
</head>

<body>
   <svg xmlns="https://www.w3.org/2000/svg" width="400px"
      height="150px" style="border:1px solid black;">
      <rect id="re" x="50" y="20" width="100" height="50"
         fill="#a0a0a0" stroke="#000000" stroke-width="2" />
   </svg>

   <script>
```

```javascript
const re = document.getElementById("re");
re.addEventListener("click", change);
```

```html
</script>
</body>
</html>
```

**清单 9.12** `svg_event.htm` 文件

矩形有一个 ID，与 HTML 元素一样，这是通过 `getElementById()` 方法与 JavaScript 建立连接所必需的。在 `change()` 函数中，`getAttribute()` 方法以字符串形式返回属性的值，属性名称在字符串中指定。

如果该值需要进一步作为数字处理，则必须首先使用 `parseInt()` 方法进行转换。在这种情况下，数值增加 100，然后使用 `setAttribute()` 方法将这个新值赋给属性。该方法需要两个参数：属性名称（字符串形式）和属性的新值。

## 9.7 动态 SVG 元素

你不仅可以使用 JavaScript 访问现有的 SVG 元素，还可以创建新的 SVG 元素。这使你能够创建包含许多相似元素的动态 SVG 图形。

### 9.7.1 动画序列

`svg_create.htm` 文件中的程序总共生成了 36 个矩形。它们被赋予随机颜色，并排列成 6×6 的网格（参见图 9.13）。

![使用 JavaScript 创建的 SVG 元素](img/img-f9.13.html)

**图 9.13**　使用 JavaScript 创建的 SVG 元素

所有矩形随后经历类似的动画：它们向右移动，延迟一段时间后旋转 90 度（参见图 9.14），然后被赋予另一种随机颜色。

![使用 JavaScript 动画化的 SVG 元素](img/img-f9.14.html)

**图 9.14**　使用 JavaScript 动画化的 SVG 元素

### 9.7.2 创建初始状态

创建初始状态的代码如下：

```html
... <head> ...
<script>
```

```javascript
function create()
{
   const svgCont = document.getElementById("idSVG");
   const ns = "http://www.w3.org/2000/svg";
   const colorArray = ["#ff0000", "#ffff00", "#00ff00", "#0000ff"];

   for(let i=0; i<6; i++)
   {
      for(let k=0; k<6; k++)
      {
         /* Add rectangle to SVG container */

         const re = document.createElementNS(ns, "rect");

         const xValue = 20 + 40 * i;
         re.setAttribute("x", xValue);

         const yValue = 20 + 40 * k;
         re.setAttribute("y", yValue);

         re.setAttribute("width", "20");
         re.setAttribute("height", "20");

         const fillValue = colorArray[Math.floor(Math.random() * 4)];
         re.setAttribute("fill", fillValue);

         re.setAttribute("stroke", "#000000");
         re.setAttribute("stroke-width", "2");

         svgCont.appendChild(re);

         ...
      }
   }
}
```

```html
</script>
</head>

<body>
   <svg xmlns="https://www.w3.org/2000/svg" id="idSVG" width="310px"
      height="260px" style="border:1px solid black;" />

   <script>
```

```javascript
create();
```

```html
</script>
</body>
</html>
```

**清单 9.13**　`svg_create.htm` 文件，初始状态

文档主体包含一个带有 ID 的 SVG 容器，该容器尚未包含任何元素。在这种情况下，不需要结束标签，但开始标签必须以 `/>` 结束。

在此之下，调用了 JavaScript 函数 `create()`。这种顺序确保了在创建 SVG 元素之前，包含 SVG 容器的 HTML 文档已被加载。

在 `create()` 函数中，首先设置了一些变量。`svgCont` 变量引用 SVG 容器，而 `ns` 变量引用 SVG 元素所需的命名空间。`colorArray` 字段包含使用随机生成器选择的四种可能颜色。

通过嵌套循环，可以在 6×6 网格中排列 36 个 SVG 元素。要创建新的 SVG 元素，可以使用 `createElementNS()` 方法，该方法可以从特定命名空间创建元素。该方法需要两个参数：命名空间和元素类型，在本例中为 `rect`。该方法在指定 `https` 时存在问题，因此这里仍使用 `http`。

使用 `setAttribute()` 方法将属性及其值赋给新创建的 SVG 元素。根据 6×6 网格中的当前行和当前列确定 x 和 y 坐标的值，并使用随机生成器和之前创建的字段确定颜色的值。

一旦分配了所有属性，新创建的矩形就会使用 `appendChild()` 方法作为子节点添加到 SVG 容器中。

### 9.7.3 创建动画

现在让我们来看看动画的代码。它位于内层循环中，因此每次为一个矩形执行：

```javascript
...

/* Add animated translation to rectangle */

const animX = document.createElementNS(ns, "animate");

animX.setAttribute("attributeName", "x");
animX.setAttribute("begin", "1");
animX.setAttribute("dur", "1");
animX.setAttribute("by", "50");
animX.setAttribute("fill", "freeze");

re.appendChild(animX);

/* Add animated rotation to rectangle */

const animRot = document.createElementNS(ns, "animateTransform");

animRot.setAttribute("attributeName", "transform");
animRot.setAttribute("type", "rotate");

const beginValue = 3 + 0.2 * i;
animRot.setAttribute("begin", beginValue);

animRot.setAttribute("dur", "1");

const fromValue = "0, " + (80+40*i) + ", " + (30+40*k);
animRot.setAttribute("from", fromValue);

const toValue = "90, " + (80+40*i) + ", " + (30+40*k);
animRot.setAttribute("to", toValue);

animRot.setAttribute("fill", "freeze");

re.appendChild(animRot);

/* Add animated color change to rectangle */

const animFill = document.createElementNS(ns, "animate");

animFill.setAttribute("attributeName", "fill");
animFill.setAttribute("begin", "6");
animFill.setAttribute("dur", "1");

/* Color must change */

let fillToValue;

do
   fillToValue = colorArray[Math.floor(Math.random() * 4)];
while(fillToValue == fillValue);

animFill.setAttribute("to", fillToValue);
animFill.setAttribute("fill", "freeze");

re.appendChild(animFill);

...
```



**清单 9.14**　`svg_create.htm` 文件，动画

要创建动画平移，可以使用`createElementNS()`方法创建一个`animate`类型的新 SVG 元素。使用`setAttribute()`方法分配属性及其值后，新创建的动画将使用`appendChild()`方法作为子节点添加到相应的矩形中。

你使用`createElementNS()`、`setAttribute()`和`appendChild()`方法来创建并分配动画旋转。这次，SVG 元素的类型是`animateTransform`，为了确保旋转有延迟，你根据 6×6 网格中的当前列单独设置`begin`属性的值。请注意`from`和`to`属性的值：旋转从 0 度的起始状态到 90 度的结束状态，每个矩形围绕其自身中心旋转。

你还使用`createElementNS()`、`setAttribute()`和`appendChild()`方法来创建并分配动画颜色变化。这次，SVG 元素再次使用`animate`类型，并且你使用`do-while`循环来确保新颜色值与旧颜色值始终不同。

### 注意

你可以在本书的可下载材料中找到 bonus 第 1 章第 1.19 节的`u_svg`练习，下载地址为[`www.rheinwerk-computing.com/5875`](http://www.rheinwerk-computing.com/5875)。

# 10　使用 Three.js 的三维图形与动画

你可以使用 Three.js 库来显示三维图形和动画。

Three.js 是一个 JavaScript 库，无需额外程序即可在浏览器中显示三维（3D）图形。这些 3D 图形还可以包含动画。

Three.js 基于 Web 图形库（WebGL），这是一个图形编程接口，是许多现代浏览器的组成部分。该库在不断改进，部分得益于活跃的社区。

目前（截至 2024 年 8 月），Three.js 的版本为 167。包含整个库的 revision 157 的`three.min.js`文件大小为 634 KB，你可以在本书的可下载材料中找到它以及示例文件。在以下示例中，我们访问此文件，它位于与示例文件相同的目录中。

你可以在[`threejs.org`](https://threejs.org)找到任何更新的版本，并使用下载链接下载大小约为 260 MB 的`three.js-master.zip`文件。所需的`three.min.js`文件位于解压后包的`build`子目录中。偶尔会出现下载问题，如果遇到这种情况，请使用本书可下载材料中提到的文件。

本章涵盖 Three.js 的基础知识：不同的三维几何体、不同的相机位置，以及三维物体的位移、旋转和动画。它不涉及高级主题，如不同的材质、光照类型和投影。

## 10.1　第一个 3D 图形

使用一个简单的立方体 3D 几何体来说明 3D 图形的各个元素（参见图 10.1）。

![作为第一个 3D 对象的立方体](img/img-f10.1.html)

**图 10.1**　作为第一个 3D 对象的立方体

我们从右上方向用相机观察立方体。这样，立方体的三个面以不同颜色可见。

### 10.1.1　3D 坐标系

为了阐明 3D 图形的结构，我们首先需要了解 3D 坐标系的基础知识。3D 空间中的每个点都可以通过其 x 坐标、y 坐标和 z 坐标唯一标识。

坐标`x=0`、`y=0`和`z=0`表示系统的中心。默认情况下，该点位于屏幕中心。

- x 坐标的值在中心右侧为正，左侧为负。我们系统的 x 轴在屏幕平面内从左向右延伸。
- 在中心上方，y 坐标的值为正，中心下方为负。我们系统的 y 轴在屏幕平面内从下向上延伸。
- 我们系统的 z 轴垂直穿过屏幕平面，从屏幕后方指向我们（观察者）。z 坐标的值在屏幕前方为正，屏幕后方为负。

在图 10.2 中，你可以看到带有三个轴的 3D 坐标系。为了在书的二维（2D）平面中说明 3D 空间，我选择了一种透视表示法，其中距离观察者较远的物体看起来更小。出于同样的原因，我在示例中使用透视相机来在屏幕的 2D 平面中显示 3D 图形。

![带有 X、Y 和 Z 轴的 3D 坐标系](img/img-f10.2.html)

**图 10.2**　带有 X、Y 和 Z 轴的 3D 坐标系

### 10.1.2　程序结构

以下是使用 Three.js 库对象的程序代码。在程序代码中，我将这些对象称为 Three.js 对象，以区别于屏幕上可见的 3D 对象。

我的 3D 图形结构总是相似的，因此我对第一个程序的详细解释也将帮助你了解本章中的其他程序。

```html
... <head> ...

   <script src="three.min.js"></script>

</head>

<body id="idBody">

   <script> 

 /* 3D 对象 */

      const geometry = new THREE.BoxGeometry(200, 200, 200);

      const material = new THREE.MeshNormalMaterial();

      const object = new THREE.Mesh(geometry, material);

      /* 相机 */

      const camera = new THREE.PerspectiveCamera(45,

         innerWidth/innerHeight, 1, 100000);

      camera.position.set(200, 250, 500);

      camera.lookAt(object.position);

      /* 绘图区域 */

      const drawing = new THREE.WebGLRenderer();

      drawing.setSize(innerWidth*0.8, innerHeight*0.8);

      drawing.setClearColor(0xc0c0c0);

      /* 3D 场景 */

      const scene = new THREE.Scene();

      scene.add(object);

      drawing.render(scene, camera);

      /* 将绘图添加到文档 */

      document.getElementById("idBody").appendChild(drawing.domElement); 

</script>

</body></html>
```

**清单 10.1**　`th_grafic.htm` 文件

在程序开头，包含了`three.min.js`文件中的库。

### 10.1.3　具有几何体和材质的 3D 对象

3D 对象具有形状，也称为几何体。3D 对象的几何体由许多单独的三角形表面组成，Three.js 库提供了一系列现成的常用几何体，包括球体、长方体和平截头圆锥体的几何体。这些现成的几何体将为你节省大量组装工作。

你可以使用`BoxGeometry`类型的 Three.js 对象来创建一个盒子。构造函数至少需要三个参数来指定长方体的宽度（x 方向）、高度（y 方向）和深度（z 方向）。如果选择三个相同的值，则得到立方体的特殊情况。

3D 对象具有表面材质，`MeshNormalMaterial`类型的 Three.js 对象从 x 方向显示为红色，从 y 方向显示为绿色，从 z 方向显示为蓝色。

你可以使用`Mesh`类型的 Three.js 对象以所需的几何体和所需的表面材质创建 3D 对象。未指定对象的位置，因此其位置位于坐标系的原点。

### 10.1.4　相机

相机有多种类型。`PerspectiveCamera`类型的 Three.js 对象提供了一种相机，能够呈现图形场景的透视视图。该相机位于一个具有矩形底面的金字塔顶端。

在图 10.3 中，相机由右侧的一个粗点表示。相机透过金字塔看向左侧的底面。金字塔之外的所有内容在图形场景中均不可见。

![带图层的透视相机](img/img-f10.3.html)

**图 10.3**　带图层的透视相机

构造函数需要以下四个参数：

- `fov` = 视野：这是以度数为单位的视角。45 度时能获得自然的透视效果。
- `aspect` = 宽高比：这是矩形金字塔底面的宽度与高度之比。建议使用浏览器窗口的宽高比。
- `near` = 近平面：这是图 10.3 中金字塔的一个（虚线）横截面。该图层之前的所有内容在图形场景中均不可见。
- `far` = 远平面：这是金字塔的底面（在图 10.3 中用点线表示）。该图层之后的所有内容在图形场景中同样不可见。

通过使用`position`类型的 Three.js 对象，可以访问 Three.js 对象的位置属性。可以单独调用或设置`position`对象的`x`、`y`和`z`属性来设定坐标，也可以使用`set()`方法同时设置三个坐标。此处选择的`x=200`、`y=250`和`z=500`值将相机定位在坐标原点右上方且前方。

在默认情况下，相机的观察方向是正前方，但可以使用`lookAt()`方法改变观察方向，使相机朝向原点。

### 10.1.5　画布与场景

`WebGLRenderer`类型的 Three.js 对象提供了一个绘图区域，即画布。`setSize()`方法用于设置画布的大小，这里使用浏览器窗口宽度和高度的 80%，即`window`对象的`innerWidth`和`innerHeight`属性值。

`setClearColor()`方法使用十六进制数字序列来确定画布背景颜色的红、绿、蓝分量。默认值为黑色。

`Scene`类型的 Three.js 对象创建一个图形场景，可以在其中布置 3D 对象，而`add()`方法将之前创建的 3D 对象（即立方体）添加到场景中。

画布的`render()`方法用于在画布内显示场景及相机。

画布的`domElement`属性引用了画布本身。它通过`appendChild()`方法添加到文档中。

## 10.2　移动相机

为了展示三维结构，我们可以通过以下程序在三个方向上移动相机。

这里仅展示与第 10.1 节程序相比新增的代码部分：

```html
...

<body id="idBody">

   <form>

   <script>
```

```javascript
 ...

      let cx = 200, cy = 250, cz = 500;

      camera.position.set(cx, cy, cz);

      ...
```

```html
 </script>

   <p>

   <input id="posPX" type="button" value="+X">

   <input id="posMX" type="button" value="-X">

   <input id="posPY" type="button" value="+Y">

   <input id="posMY" type="button" value="-Y">

   <input id="posPZ" type="button" value="+Z">

   <input id="posMZ" type="button" value="-Z"></p>

   </form>

   <script>
```

```javascript
 document.getElementById("posPX").addEventListener

         ("click", function(){move(50,0,0)});

      document.getElementById("posMX").addEventListener

         ("click", function(){move(-50,0,0)});

      document.getElementById("posPY").addEventListener

         ("click", function(){move(0,50,0)});

      document.getElementById("posMY").addEventListener

         ("click", function(){move(0,-50,0)});

      document.getElementById("posPZ").addEventListener

         ("click", function(){move(0,0,50)});

      document.getElementById("posMZ").addEventListener

         ("click", function(){move(0,0,-50)});

      function move(dx, dy, dz)

      {

         cx += dx;

         cy += dy;

         cz += dz;

         camera.position.set(cx, cy, cz);

         camera.lookAt(object.position);

         drawing.render(scene, camera);

      }
```

```html
 </script>

</body></html>
```

**清单 10.2**　`th_camera.htm` 文件

文档中间部分引入了`cx`、`cy`和`cz`变量，用于指定相机的位置。

文档下半部分创建了六个按钮，用于实现相机在 x、y、z 方向上的正向或负向移动（参见图 10.4）。点击按钮会调用`move()`函数，并传入三个方向上的位移值作为参数。

在文档下半部分的`move()`函数中，将传入的三个移动值加到相机当前的位置值上。相机获得新确定的位置后，程序确保相机再次看向立方体。最后，必须重新渲染绘图。

随着相机位置值的绝对值增大，相机与物体之间的距离也随之增加，因此从观察者的视角看，物体会变得越来越小。

![移动按钮](img/img-f10.4.html)

**图 10.4**　移动按钮

## 10.3　动画

为了进一步展示 3D 结构，本节第一个程序中的立方体将通过动画绕 y 轴缓慢旋转总计 90 度。

这里仅展示与第 10.1 节程序相比新增的代码部分：

```html
...

<body id="idBody">

   <script>
```

```javascript
 ...

      function rotate()

      {

         object.rotation.y += 0.2 * Math.PI / 180;

         drawing.render(scene, camera);

         if(object.rotation.y <= 90 * Math.PI / 180)

            requestAnimationFrame(rotate);

      }

      rotate();
```

```html
 </script>

</body></html>
```



**清单 10.3**　`th_animation.htm` 文件

你可以使用 Three.js 对象的 `rotation` 类型来访问其旋转角度。你可以通过 `rotation` 对象的 `x`、`y` 或 `z` 属性单独调用或设置绕相关轴的角度，并且必须以弧度为单位指定角度。如果以度为单位指定，则必须先乘以系数 `π / 180`。

绕 y 轴的旋转角度值增加 0.2 度，起初看起来非常小。然后使用 `render()` 方法重新绘制图形场景，如果绕 y 轴的旋转角度小于或等于 90 度，则调用 `window` 对象的 `requestAnimationFrame()` 方法，并再次传入对 `rotate()` 方法的引用。这确保了 `rotate()` 方法会被再次调用。然后，对象再次旋转 0.2 度，图形场景再次绘制，依此类推。这就是创建动画的方式。默认情况下，这些操作每秒执行六十次，从而产生每秒 12 度的旋转。因此，最终值 90 度在 7.5 秒后达到。如果移除分支，3D 对象将无限旋转下去。

## 10.4 各种形状

在本书的可下载资料中，你可以找到作为额外内容的 `th_multiple.htm` 程序。该程序可用于在网格视图中显示总共八种不同的形状：球体、长方体、圆锥体、四面体、八面体、胶囊体、圆环体和圆环结（参见图 10.5）。摄像机看向原点，即绘图的中心。这就是为什么最左边和最右边的四个形状在透视中会发生变形。

![八种不同形状](img/img-f10.5.html)

**图 10.5**　八种不同形状

### 注意

`th_change.htm` 程序在本书可下载资料的额外章节 4 中进行了描述，可访问 [www.rheinwerk-computing.com/5875](http://www.rheinwerk-computing.com/5875)。该程序允许单独且更清晰地显示来自图 10.5 的八种不同几何形状。它们还可以被动画移动和旋转。

# 11 jQuery

jQuery 库中与浏览器无关的标准化方法已成为许多网站不可或缺的一部分。

jQuery 是使用最广泛的 JavaScript 库，并被用作许多内容管理系统和 Web 框架（如 Joomla 和 WordPress）的基础。jQuery 提供了便捷、与浏览器无关的方法，用于处理 CSS、Ajax 和动画等。我在本章的示例中使用了当前（截至 2024 年 8 月）版本 3.7.1。

包含整个库的 `jquery-3.7.1.min.js` 文件仅有 86 KB。你可以在本书的可下载资料中找到它以及示例文件。

如果你想下载任何更新的版本，应访问 [`jquery.com`](https://jquery.com)。你可以通过压缩生产术语在下载页面上找到此处使用的文件。在以下示例中，我假设该文件与示例文件位于同一目录中。

## 11.1 结构

通过一个初始示例，我将解释使用 jQuery 的不同方式。图 11.1 显示了一个文件，其中包含一个带有文本的段落和三个带有超链接的段落。

点击各个超链接后，由于使用了 jQuery，第一个段落的内容会发生变化，如图 11.2、图 11.3 和图 11.4 所示。

![第一个 jQuery 文件](img/img-f11.1.html)

**图 11.1**　第一个 jQuery 文件

![第一次更改](img/img-f11.2.html)

**图 11.2**　第一次更改

![第二次更改](img/img-f11.3.html)

**图 11.3**　第二次更改

![第三次更改](img/img-f11.4.html)

**图 11.4**　第三次更改

以下是代码：

```html
... <head> ...

   <script src="jquery-3.7.1.min.js"></script>

   <script> 

 $(document).ready(function()

      {

         $("#idParagraph").html("<i>After loading</i>");

         $("#idLink1").click(function()

            { $("#idParagraph").html("<b>After click 1</b>"); });

      }); 

 </script>

</head>

<body>

   <p id="idParagraph" style="background-color:#e0e0e0;

      width:300px;">Hello</p>

   <p><a id="idLink1" href="#">Click 1</a></p>

   <p><a id="idLink2" href="#">Click 2</a></p>

   <p><a id="idLink3" href="#">Click 3</a></p>

   <script> 

 $("#idLink2").click(function(){ 

         $("#idParagraph").html("After click 2"); });

      jQuery("#idLink3").click(function(){ 

         jQuery("#idParagraph").html("<b><i>After click 3</i></b>"); }); 

 </script>

</body></html> 
```

**清单 11.1**　`jq_loaded.htm` 文件

该文档包含一个带有示例文本 `Hello` 的段落。在其下方，有三个段落，每个段落包含一个超链接。

在上方的 JavaScript 区域中调用了 `ready()` 方法，该方法以一个回调函数的引用作为参数。在内部，`ready()` 方法确保回调函数仅在文件及其所有元素在浏览器中加载完成后才被调用。否则，可能会访问一个尚不存在的元素。

jQuery 经常使用匿名回调函数，如下所示：

- 函数中的第一条语句为具有 `idParagraph` ID 的元素调用 `html()` 方法。它会更改元素的文本（包括 HTML 标签）。因此，一旦文档完全加载，第一个段落将以斜体显示。
- 第二条语句为具有 `idLink1` ID 的元素调用 `click()` 方法，该方法也以一个匿名回调函数的引用作为参数。在内部，`click()` 方法确保在点击超链接后调用回调函数。然后，第一个段落中会出现粗体文本。

在文档末尾，点击第二个或第三个超链接后，会调用 `click()` 方法，第一个段落的内容随之改变。

此处不再需要调用 `ready()` 方法，因为文档的所有元素都已加载完毕。

你可以使用 `$` 函数和 `jQuery` 函数来调用 jQuery 语句。两种调用方式结果相同。

### 注意

jQuery 语句针对选择器中指定的元素执行，这些选择器通常是 CSS 选择器。

由于 jQuery 语句中括号层级较多，我建议使用此处采用的紧凑写法。在你自己的程序中，也请注意经常需要的引号。

## 11.2 选择器与方法

你使用选择器来选取 jQuery 代码所引用的元素。本节介绍以下选择器：

- `css()`，用于更改 CSS 属性
- `html()`，用于更改包含 HTML 代码的文本
- `text()`，用于更改不含 HTML 代码的文本

我们还使用了其他各种方法。在图 11.5 中，你可以看到四个不同的 `div` 元素。你可以通过超链接来改变它们。

![选择器与方法](img/img-f11.5.html)

**图 11.5**　选择器与方法

现在让我们来看一下代码，首先是不包含 `ready()` 方法内容的部分：

```html
... <head> ...

   <script src="jquery-3.7.1.min.js"></script>

   <script> 

 $(document).ready(function() { ... }); 

 </script>

   <style> 

 div       {width:250px; height:20px; background-color:#c0c0c0;}

      #idBright {background-color:#e0e0e0;}

      .dark     {background-color:#a0a0a0;} 

 <style>

</head>

<body>

   <div>div 元素，无 id，无 class</div>

   <div id="idBright">具有 'idBright' id 的元素</div>

   <div class="dark">1. 具有 'dark' class 的 div 元素</div>

   <div class="dark">2. 具有 'dark' class 的 div 元素</div>

   <p><a id="idLink1" href="#"> 1: div 元素的 CSS</a></p>

   <p><a id="idLink2" href="#"> 2: 'idBright' id 的 CSS</a></p>

   <p><a id="idLink3" href="#"> 3: 'dark' class 的 CSS</a></p>

   <p><a id="idLink4" href="#"> 4: 集合的 CSS</a></p>

   <p><a id="idLink5" href="#"> 5: 'idBright' id 的多重 CSS</a></p>

   <p><a id="idLink6" href="#"> 6: 'idBright' id 的 HTML</a></p>

   <p><a id="idLink7" href="#"> 7: 'idBright' id 的文本</a></p>

   <p><a id="idLink8" href="#"> 8: 'idBright' id 的 CSS 和 HTML</a></p>

</body></html>
```

**清单 11.2**　`jq_select.htm` 文件，不含 `ready()` 方法

接下来我将解释 `ready()` 方法的内容。以下是对所有 `div` 元素的通用设置：

- 它们的大小为 250×20 像素，颜色为中灰色。
- 具有 `idBright` ID 的元素为浅灰色。
- `dark` CSS 类的所有元素为深灰色。

以下是四个 `div` 元素：

- 第一个元素没有 ID，也不属于任何 CSS 类。
- 第二个元素具有 `idBright` ID。
- 第三和第四个元素被分配了 CSS 类 `dark`。

接下来是八个段落，每个段落包含一个链接。这些链接的 ID 分别为 `idLink1` 到 `idLink8`。

现在，这是 `ready()` 方法的内容：

```javascript
$("#idLink1").click(function(){

    $("div").css({"width":"350px"}); });

$("#idLink2").click(function(){

    $("#idBright").css({"width":"400px"}); });

$("#idLink3").click(function(){

    $(".dark").css({"width":"450px"}); });

$("#idLink4").click(function(){

    $("#idBright, .dark").css({"width":"500px"}); });

$("#idLink5").click(function(){

    $("#idBright").css({"background-color":"#f0f0f0",

                       "width":"550px"}); });        

$("#idLink6").click(function(){

    $("#idBright").html("<b>HTML new</b>"); });

$("#idLink7").click(function(){

    $("#idBright").text("Text new"); });

$("#idLink8").click(function(){

    $("#idBright").css({"width":"+=20px"}).html("CSS and HTML new");});
```

**清单 11.3**　`jq_select.htm` 文件，`ready()` 方法的内容

点击第一个超链接后，`css()` 方法会对所有 `div` 元素执行，并更改 CSS 属性。这里将元素的宽度设置为 350 像素，并以 JSON 格式指定属性-值对。第二个超链接更改具有 `idBright` ID 的元素，第三个超链接更改所有具有 `dark` CSS 类的元素。

你可以将多个选择器组合到一个集合中。第四个超链接更改具有 `idBright` ID 的元素以及所有具有 `dark` CSS 类的元素。

在 JSON 格式中，多个属性-值对用逗号分隔。第五个超链接更改具有 `idBright` ID 的元素的背景颜色和宽度。

第六个超链接调用 `html()` 方法，该方法会更改包含 HTML 代码的文本。

第七个超链接调用 `text()` 方法，该方法会更改文本，但不考虑 HTML 代码。任何意外包含的 HTML 元素也会作为文本输出。

你可以使用链式调用来为一个选择器执行多个方法，还可以通过 `+=` 和 `-=` 运算符相对于原始值更改 CSS 值。第八个超链接依次对具有 `idBright` ID 的元素执行 `css()` 和 `html()` 方法，并且在 `css()` 方法中，每次点击宽度增加 20 像素。

## 11.3 事件

除了 `click` 事件，你还可以使用其他事件来启动 jQuery 代码。

在图 11.6 中，你可以看到一个 `div` 元素，其下方有一系列超链接。在链接上触发事件会导致元素的动画展开，你可以使用 `animate()` 方法来创建动画。更多关于动画的内容请参见第 11.4 节。

![各种事件](img/img-f11.6.html)

**图 11.6**　各种事件

现在，让我们来看一下代码，首先是不包含 `ready()` 方法内容的部分：

```html
... <head> ...

   <script src="jquery-3.7.1.min.js"></script>

   <script> 

 $(document).ready(function() { ... }); 

 </script>

</head>

<body>

   <div id="idRect" style="width:200px; height:100px;

        background-color:#c0c0c0;">矩形</div>

   <p><a id="idLink1" href="#"> 1: click</a></p>

   <p><a id="idLink2" href="#"> 2: dblclick</a></p>

   <p><a id="idLink3" href="#"> 3: mouseenter</a></p>

   <p><a id="idLink4" href="#"> 4: mouseleave</a></p>

   <p><a id="idLink5" href="#"> 5: mousemove</a></p>

   <p><a id="idLink6" href="#"> 6: mousedown</a></p>

   <p><a id="idLink7" href="#"> 7: mouseup</a></p>

   <p><a id="idLink8" href="#"> 8: hover</a></p>

   <p><a id="idLink9" href="#"> 9: mousedown 和 mouseup</a></p>

   <p><a id="idLink10" href="#">10: click（带参数）</a></p>

</body></html>
```

**清单 11.4**　`jq_event.htm` 文件，不含 `ready()` 方法

`div` 元素具有 `idRect` ID，大小为 200×100 像素，颜色为灰色。

现在，这是 `ready()` 方法的内容：

```javascript
$("#idLink1").click(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink2").dblclick(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink3").mouseenter(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink4").mouseleave(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink5").mousemove(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink6").mousedown(function(){
```



```javascript
$("#idRect").animate({"width":"+=20px"}); });

$("#idLink7").mouseup(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink8").hover(function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink9").bind("mousedown mouseup", function(){

    $("#idRect").animate({"width":"+=20px"}); });

$("#idLink10").click(function(e){

    $("#idRect").html("Event: " + e.type

        + "<br>Position X: " + e.pageX + " , Y: " + e.pageY

        + "<br>Time: " + Date(e.timeStamp)); });
```

**清单 11.5**　`jq_event.htm` 文件，`ready()` 方法的内容

只需点击第一个超链接即可调用 `click()` 方法。该元素会变宽 20 像素，后续几乎所有事件也是如此。双击第二个超链接可调用 `dblclick()` 方法。

第三个超链接在鼠标光标进入超链接上方区域时立即触发（即通过 `mouseenter` 事件）。这会调用 `mouseenter()` 方法，同样的事情发生在鼠标光标离开第四个超链接上方区域（事件和方法名称为 `mouseleave`）以及悬停在第五个超链接上时（事件和方法名称为 `mousemove`）。

在第六个超链接上按下鼠标按钮会触发 `mousedown` 事件，在第七个超链接上释放鼠标按钮会触发 `mouseup` 事件。这些操作分别调用 `mousedown()` 和 `mouseup()` 方法。

`hover()` 方法结合了 `mouseenter` 和 `mouseleave` 事件，当鼠标光标进入第八个超链接上方区域或离开该区域时（分别）触发。

你使用 jQuery 的 `bind()` 方法将事件绑定到方法。实际上，本节中的其他方法都是 `bind()` 方法的简化形式。你使用第九个超链接来绑定 `mousedown` 和 `mouseup` 事件，因此通过按下和释放鼠标按钮都能触发动画。

每个事件的信息都包含在一个事件对象中。使用 jQuery，这个事件对象在所有浏览器中都是标准化的，你可以通过传递给方法作为参数的引用来访问它。当你点击第十个超链接时，会显示一些信息：本例中，使用 `type`、`pageX`、`pageY` 和 `timeStamp` 属性显示事件的类型、位置和时间。`timeStamp` 以毫秒为单位，你可以使用 jQuery 的 `Date()` 方法进行转换。

## 11.4 动画

本节介绍动画元素的各种选项。为此，你使用 `animate()` 方法，它（如同电影一样）营造出连续单帧图像的印象。

在图 11.7 中，你可以看到一个定位的 `div` 元素。你可以使用前 11 个超链接为该元素启动不同的动画。为清晰起见，你应在每次动画后恢复页面加载后的初始状态。你可以通过第十二个超链接来实现。

![动画](img/img-f11.7.html)

**图 11.7**　动画

现在，让我们看看代码，首先是不包含 `ready()` 方法的内容：

```html
... <head> ...

   <script src="jquery-3.7.1.min.js"></script>

   <script>
```

```javascript
$(document).ready(function() { ... });
```

```html
   </script>

</head>

<body>

   <div id="idRect" style="position:absolute; width:100px; height:100px;

      left:300px; top:100px; background-color:#c0c0c0;">Rectangle</div>

   <p><a id="idLink1" href="#"> 1: One property (width)</a></p>

   <p><a id="idLink2" href="#"> 2: Two properties (width/height)</a></p>

   <p><a id="idLink3" href="#"> 3: Position (left/top)</a></p>

   <p><a id="idLink4" href="#"> 4: Transparency (opacity)</a></p>

   <p><a id="idLink5" href="#"> 5: Time (duration)</a></p>

   <p><a id="idLink6" href="#"> 6: Easing: linear instead of swing</a></p>

   <p><a id="idLink7" href="#"> 7: Callback: next animation</a></p>

   <p><a id="idLink8" href="#"> 8: Relative change (+=, -=)</a></p>

   <p><a id="idLink9" href="#"> 9: Chain</a></p>

   <p><a id="idLink10" href="#">10: Chain, with delay</a></p>

   <p><a id="idLink11" href="#">11: Simultaneously (queue)</a></p>

   <p><a id="idLink12" href="#">12: Initial state</a></p>

</body></html>
```

**清单 11.6**　`jq_animate.htm` 文件，不含 `ready()` 方法

`div` 元素具有 `idRect` ID，初始大小为 100×100 像素，初始位置为 300×100 像素，颜色为灰色。仅当位置被动画化时才需要定位。

现在，这是 `ready()` 方法的内容：

```javascript
$("#idLink1").click(function(){

    $("#idRect").animate({"width":"200px"}); });

$("#idLink2").click(function(){

    $("#idRect").animate({"width":"200px", "height":"50px"}); });

$("#idLink3").click(function(){

    $("#idRect").animate({"left":"400px", "top":"200px"}); });

$("#idLink4").click(function(){

    $("#idRect").animate({"opacity":"0.5"}); });

$("#idLink5").click(function(){

    $("#idRect").animate({"width":"200px"}, {"duration":2000});});

$("#idLink6").click(function(){

    $("#idRect").animate({"left":"400px"},

    {"duration":2000, "easing":"linear"}); });

$("#idLink7").click(function(){

    $("#idRect").animate({"left":"400px"},

        function(){$("#idRect").animate({"left":"300px"}) }); });

$("#idLink8").click(function(){

    $("#idRect").animate({"left":"+=100px", "opacity":"-=0.3"});});

$("#idLink9").click(function(){

    $("#idRect").animate({"left":"+=100px"})

        .animate({"left":"-=100px"}); });

$("#idLink10").click(function(){

    $("#idRect").animate({"left":"+=100px"})

        .delay(1000).animate({"left":"-=100px"}); });

$("#idLink11").click(function(){

    $("#idRect").animate({"width":"200px"}, {"duration":1000})

        .animate({"height":"50px"}, {"duration":2000, "queue":false}); });

$("#idLink12").click(function(){

    $("#idRect").animate({"width":"100px", "height":"100px",

        "left":"300px", "top":"100px", "opacity":1.0}); });
```

### 清单 11.7　`jq_animate.htm` 文件，`ready()` 方法的内容

第一个超链接将宽度动画化到目标值 200 像素。你可以同时更改多个属性。第二个超链接将宽度动画化到目标值 200 像素，并将高度动画化到目标值 50 像素。

通过更改 `left` 和 `top` 的属性值，可以实现动画移动。第三个超链接将矩形移动到目标点 400 像素/200 像素。你可以使用第四个超链接通过 `opacity` 属性将透明度更改为 0.5（另请参见第 8 章、第 8.2.4 节）。

未进一步指定时，动画持续 0.4 秒（即 400 毫秒）。你可以通过 `animate()` 方法的第二个参数中的 `duration` 属性设置动画持续时间。以毫秒为单位写入值，不带引号。第五个超链接在 2 秒内将宽度更改为目标值 200 像素。

`easing` 属性描述了动画的时间特性。默认值 `swing` 表示动画开始时加速，以稳定速度继续，并在结束时减速。这营造出自然过程的印象。

如果在 `animate()` 方法的第二个参数中为 `easing` 属性输入 `linear` 值，动画将以恒定速度运行，看起来不那么自然。你可以在互联网上找到的缓动插件提供了更多缓动函数的选项。第六个超链接用于在 2 秒内将元素线性移动到目标值。

你还可以将回调函数的引用作为附加参数传递，该函数在动画结束后执行。第七个超链接将元素移动到目标值 400 像素，然后元素再移动到目标值 300 像素。

到目前为止，我们为动画属性指定了绝对目标值，但你也可以使用 `+=` 和 `-=` 运算符进行相对更改。第八个超链接每次点击时将元素向右移动 100 像素，并根据当前值将透明度更改 0.3。对于 `opacity` 属性，大于 1.0 或小于 0.0 的值没有意义，但不会导致错误。

方法调用可以串联。第九个超链接用于将元素向右移动 100 像素，然后向左移动 100 像素。

你可以使用 `delay()` 方法在动画中添加延迟。第十个超链接与第九个超链接产生相同的移动，但在两个部分动画之间有一秒的等待。

在链中，动画的各个部分默认依次运行，但你可以使用 `queue` 参数确保它们同时发生。第十一个超链接在一秒内将宽度动画化到目标值 200 像素。高度在 2 秒内动画化到目标值 50 像素，但同时进行。这是通过将 `queue` 属性设置为布尔值 `false`（不带引号）实现的。默认值为 `true`。

第十二个超链接用于恢复总共五个属性的初始状态：`width`、`height`、`left`、`top` 和 `opacity`。

事件会被缓冲。如果在正在运行的动画结束前点击超链接，相应的操作将在之后执行。

以下方法不提供任何额外选项，但可用作快捷方式：

- `slideDown()`、`slideUp()` 和 `slideToggle()` 方法用于更改 `height` 属性。
- `fadeIn()`、`fadeOut()`、`fadeToggle()` 和 `fadeTo()` 方法用于更改 `opacity` 属性。
- `show()`、`hide()` 和 `toggle()` 方法用于同时更改 `width`、`height` 和 `opacity` 属性。

## 11.5 示例：正弦运动

到目前为止，各个函数中只调用了 jQuery 方法，但我们不应忘记，我们还可以使用 JavaScript 的其他部分。以下示例展示了 jQuery 与 JavaScript 其他部分的结合。点击最左侧的小方块后，它将沿正弦曲线移动。此外，还有一些辅助线（参见图 11.8）。

![正弦曲线动画，起始点](img/img-f11.8.html)

### 图 11.8　正弦曲线动画，起始点

曲线由单个线段组成。每个线段由 jQuery 动画生成，`for` 循环确保动画按顺序执行。曲线划分得越细，曲线进展越平滑，但即使将其划分为每 10 度一段，也能看到相当均匀的进展。

以下是代码：

```html
... <head> ...

   <script src="jquery-3.7.1.min.js"></script>

   <script>
```

```javascript
function sine()
{
    for(let angle = 10; angle <= 360; angle += 10)
    {
        const pLeft = (10 + angle) + "px";
        const pTop = (110 - Math.sin(angle / 180 * Math.PI) * 100) + "px";
        $("#idBlock").animate({"left":pLeft, "top":pTop},
            {"duration":"100", "easing":"linear"});
    }
}

$(document).ready(function() { $("#idLink").click(sine); });
```

```html
   </script>

</head>

<body>

   <div id="idBlock" style="position:absolute; left:10px; top:110px;">

   <a id="idLink" href="#"><img src="block.gif" alt="Block"></a></div>

   <script>
```

```javascript
for(let pTop = 10; pTop < 211; pTop += 50)
    document.write("<div style='position:absolute; left:20px; top:"
        + pTop + "px;'><img src='im_line.jpg' alt='Line'></div>");
```

```html
   </script>

</body></html>
```

### 清单 11.8　`jq_sine.htm` 文件

辅助线通过 `for` 循环生成，`pTop` 属性取值分别为 10、60、110、160 和 210 像素。

在 `sine()` 函数中，`angle` 变量以 10 为步长，取值从 10 到 360。图像在 x 方向上均匀向右移动，而 y 方向的移动则使用了 JavaScript 中 `Math` 对象的 `sin()` 方法。该方法要求角度以弧度为单位，因此需要事先进行转换。通过这种方式计算得到的目标点值被保存在 `pLeft` 和 `pTop` 变量中，这些变量又可以用作 `animate()` 方法参数中 `left` 和 `top` 属性的目标值。

## 11.6 jQuery 与 Ajax

Ajax 允许你重新加载文档的部分内容，正如我们在第 7 章中所述。jQuery 中有许多方法在内部使用了 Ajax 技术，你可以像习惯使用 jQuery 那样，独立于浏览器和版本进行工作。

在本例中，你将使用 `load()` 和 `post()` 方法从文本文件、HTML 文件、PHP 程序和 XML 文件中加载内容到当前文档，而无需重建页面的其余部分。

你可以在下面的程序中看到一些示例。页面的初始状态如图 11.9 所示，你需要通过 Web 服务器加载该页面（另请参见第 7 章）。

![jQuery 与 Ajax](img/img-f11.9.html)

**图 11.9**　jQuery 与 Ajax

以下是代码，最初不包含第二个 JavaScript 容器的内容：

```html
<!DOCTYPE html><html lang="en-us">

<head>

   <meta charset="utf-8">

   <title>jQuery and Ajax</title>

   <link rel="stylesheet" href="js5.css">

   <script src="jquery-3.7.1.min.js"></script>

   <script> ... </script>

</head>

<body>

   <p><b>load() 方法用于文本和 HTML：</b></p>

   <p><a id="idLink1" href="#"> 1: 整个文本文件</a></p>
```



<p><a id="idLink2" href="#">2: 整个 HTML 文件</a></p>

<p><a id="idLink3" href="#">3: HTML 文件中的第 1 部分</a></p>

<p><b>`post()` 方法用于 XML 和 PHP：</b></p>

<p><a id="idLink4" href="#">4: PHP 返回的 HTML 结果</a></p>

<p><a id="idLink5" href="#">5: 提交并获取 PHP 返回的 HTML 结果</a></p>

<p><a id="idLink6" href="#">6: XML 文件中的一部分</a></p>

<p><a id="idLink7" href="#">7: XML 文件中的一部分（第二种版本）</a></p>

<p id="idOutput">起始文本</p>

```html
</body></html>
```

**清单 11.9** `jq_ajax.htm` 文件（不含第二个 JavaScript 容器）

加载的内容将显示在底部带有 `idOutput` ID 的段落中。

以下是第二个 JavaScript 容器的内容：

```javascript
function xmlData(result) {
  const a = result.getElementsByTagName("nodeA")[0].firstChild.nodeValue;
  const b = result.getElementsByTagName("nodeB")[0].getAttribute("attributeA");
  $("#idOutput").html(a + ", " + b);
}

function xmlOutput() {
  $.post("jq_ajax_test.xml", function(result) {
    xmlData(result);
  });
}

$(document).ready(function() {
  $("#idLink1").click(function() {
    $("#idOutput").load("jq_ajax_test.txt");
  });

  $("#idLink2").click(function() {
    $("#idOutput").load("jq_ajax_test.htm");
  });

  $("#idLink3").click(function() {
    $("#idOutput").load("jq_ajax_test.htm #t1");
  });

  $("#idLink4").click(function() {
    $.post("jq_ajax_test.php", function(result) {
      $("#idOutput").html(result);
    });
  });

  $("#idLink5").click(function() {
    $.post(
      "jq_ajax_test_data.php",
      {number1: 12.2, number2: 25.5},
      function(result) {
        $("#idOutput").html(result);
      }
    );
  });

  $("#idLink6").click(function() {
    $.post("jq_ajax_test.xml", function(result) {
      $("#idOutput").html(
        result.getElementsByTagName("nodeA")[0].firstChild.nodeValue +
        ", " +
        result.getElementsByTagName("nodeB")[0].getAttribute("attributeA")
      );
    });
  });

  $("#idLink7").click(xmlOutput);
});
```

**清单 11.10** `jq_ajax.htm` 文件，`ready()` 方法的内容

第一个超链接使用 `load()` 方法将 `jq_ajax_test.txt` 文本文件中的整个文本加载到段落中。

```text
This is the text from the text file
```

**清单 11.11** `jq_ajax_test.txt` 文件

第二个超链接将 HTML 文件 `jq_ajax_test.htm` 的整个内容（包括标签）加载到段落中。

第三个超链接仅将 HTML 文件中具有 `t1` ID 的元素的内容（也包括标签）加载到段落中。请注意 `load()` 方法参数中文件名与 ID 的井号之间的分隔空格。

```html
...
<body>
  <p><b>HTML 文件中的文本</b></p>
  <p id="t1"><i>HTML 文件中的第 1 部分</i></p>
  <p id="t2"><i>HTML 文件中的第 2 部分</i></p>
</body></html>
```

**清单 11.12** `jq_ajax_test.htm` 文件

第四个超链接和 jQuery 的 `post()` 方法用于调用 `jq_ajax_test.php` 文件中的 PHP 程序。回调函数的参数（此处为 `result`）随后包含 PHP 程序的输出，并通过 `html()` 方法成为段落的内容。

```php
<?php
header("Content-type: text/html; charset=utf-8");

echo "<b>数据</b>来自 PHP 文件";
?>
```

**清单 11.13** `jq_ajax_test.php` 文件

第五个超链接使用 jQuery 的 `post()` 方法调用 PHP 程序 `jq_ajax_test_data.php`。发送的是以冒号分隔的属性-值对。在本例中，PHP 程序计算并返回两个值的和，该返回值成为段落的内容。

```php
<?php
header("Content-type: text/html; charset=utf-8");

echo "<b>总和</b>: "
  . (doubleval($_POST["number1"]) + doubleval($_POST["number2"]));
?>
```

**清单 11.14** `jq_ajax_test_data.php` 文件

第六个超链接调用 `jq_ajax_test.xml` 文件，同样使用 jQuery 的 `post()` 方法。确定 `nodeA` 节点的值和 `nodeB` 节点的 `attributeA` 属性的值，并将其添加到段落的内容中。

```xml
<?xml version="1.0" encoding="UTF-8"?>
<root>
  <nodeA>节点 A 的值</nodeA>
  <nodeB attributeA="节点 B 的属性 A"
          attributeB="节点 B 的属性 B">
    节点 B 的值
  </nodeB>
</root>
```

**清单 11.15** `jq_ajax_test.xml` 文件

第六个超链接中调用和匿名函数的嵌套令人困惑，因此我添加了第七个超链接，它产生相同的结果。这里使用了两个命名函数和部分结果，这有助于理解整个过程。

# 12 使用 Onsen UI 开发移动应用

你可以使用 JavaScript 和 Onsen UI 库为移动设备创建用户界面。

Onsen UI 是一个框架，提供了用于开发移动应用的组件。这些 Onsen UI 应用的用户界面特别适合智能手机和平板电脑等移动设备。这些应用还可以轻松地与其他技术（例如 JavaScript 程序）集成。

当前版本（截至 2024 年 8 月）为 2.12.8。你可以从 [`onsen.io`](https://onsen.io) 下载所需的 CSS 和 JavaScript 文件，但通常页面是通过移动设备在线访问的。因此，我在示例程序中使用所需文件的在线版本，以便始终使用最新版本。

本章中的程序已在智能手机上测试，图片是在智能手机上的 Google Chrome 浏览器中创建的。在开发过程中，你也可以使用标准 PC 上的现代浏览器来测试大部分程序功能。

Onsen UI 框架使用自己的样式表，因此本章的文件中不包含 `js5.css` 文件（该文件在本书大多数示例中通过样式表确保统一显示）。

## 12.1 页面的结构

首先，我想描述页面的基本结构，然后我会向你展示可用于设计页面的列表和表格。

### 12.1.1 第一个页面

第一个页面由一个导航栏和一个内容区域组成（参见图 12.1）。导航栏可以包含页面标题和核心操作元素，内容区域则包含文档的实际内容：一个包含一个条目的列表，即一个按钮。

按下按钮后，会出现一条信息提示（参见图 12.2）。

![第一个页面](img/img-f12.1.html)

**图 12.1** 第一个页面

程序如下：

```html
<!DOCTYPE html>
<html lang="en-us">
<head>
  <meta charset="utf-8">
  <title>Onsen UI, first page</title>
  <link rel="stylesheet" href="https://unpkg.com/onsenui/css/onsenui.css">
  <link rel="stylesheet" href="https://unpkg.com/onsenui/css/onsen-css-components.min.css">
  <script src="https://unpkg.com/onsenui/js/onsenui.min.js"></script>
</head>
<body>
  <ons-page>
    <ons-toolbar>
      <div class="left" style="padding-left:10px;">Links</div>
      <div class="center">Center</div>
      <div class="right" style="padding-right:10px;">Right</div>
    </ons-toolbar>

    <ons-list>
      <ons-list-item>
        <ons-button id="idHello">Hello</ons-button>
      </ons-list-item>
    </ons-list>
  </ons-page>

  <script>
    document.getElementById("idHello").addEventListener(
      "click",
      function() {
        ons.notification.alert("Hello");
      }
    );
  </script>
</body>
</html>
```

**清单 12.1** `onsen_page.htm` 文件

文件头部包含了我在本章开头提到的所需 CSS 和 JS 文件的在线版本链接。其他文件中的头部也类似，因此不再重复显示。

Onsen UI 组件像 HTML 容器一样集成到文档中。`ons-page` 类型的组件构成了页面的基本元素，它占据整个屏幕，并作为其他元素的容器。

页面可以使用 `ons-toolbar` 类型的组件包含一个导航栏。导航栏通过 `div` 容器和 Onsen UI 的以下 CSS 类分为三个区域：

- `left`，用于左侧边缘的元素
- `center`，用于略微缩进的元素
- `right`，用于右侧边缘的元素

在左侧和右侧区域，使用了 `padding` CSS 属性来在左右边缘之前创建小的间隙。

你可以使用 `ons-list` 和 `ons-list-item` 类型的组件来创建列表或列表条目。关于列表的更多细节将在第 12.1.2 节中介绍。

你可以使用 `ons-button` 类型的组件在内容区域显示按钮。通过 `id` 属性以及 `getElementById()` 和 `addEventListener()` 方法，以通常的方式建立与 JavaScript 的连接。

`ons.notification` 类型的组件提供了多种标准对话框的方法（另请参见第 12.2.2 节），而 `ons.notification.alert()` 方法会生成一个带有消息的信息窗口（参见图 12.2）。

![链接到 JavaScript](img/img-f12.2.html)

**图 12.2** 链接到 JavaScript

### 12.1.2 元素列表

列表常用于以清晰的方式显示多个元素。你可以为列表指定标题，将列表中的相关元素分组，并将每个列表元素分为三个区域。你还可以将列表元素链接到操作。

在图 12.3 中，你可以看到一个分组的列表。

![分组的列表](img/img-f12.3.html)

**图 12.3** 分组的列表

以下是相关程序：

```html
...
<body>
  <ons-page>
    <ons-list>
      <ons-list-title>Title</ons-list-title>

      <ons-list-header>Countries</ons-list-header>
      <ons-list-item tappable id="idSpain">Spain</ons-list-item>
      <ons-list-item tappable id="idItaly">Italy</ons-list-item>
      <ons-list-item tappable id="idFrance">France</ons-list-item>

      <ons-list-header>Cities</ons-list-header>
      <ons-list-item>
        <div class="left">No. 1</div>
        <div class="center">Rome</div>
        <div class="right">R</div>
      </ons-list-item>

      <ons-list-item>
        <div class="left">No. 2</div>
        <div class="center">Naples</div>
        <div class="right">N</div>
      </ons-list-item>
    </ons-list>
  </ons-page>

  <script>
    document.getElementById("idSpain").addEventListener(
      "click",
      function() {
        ons.notification.alert("Madrid");
      }
    );

    document.getElementById("idItaly").addEventListener(
      "click",
      function() {
        ons.notification.alert("Rome");
      }
    );

    document.getElementById("idFrance").addEventListener(
      "click",
      function() {
        ons.notification.alert("Paris");
      }
    );
  </script>
</body>
</html>
```

**清单 12.2** `onsen_list.htm` 文件

一个列表至少包含一个 `ons-list` 类型的组件作为整个列表，以及使用 `ons-list-item` 类型组件创建的条目。列表可以在 `ons-list-title` 类型的组件中拥有一个整体标题，你可以使用 `ons-list-header` 类型的组件来对元素进行分组并作为组标题。与导航栏类似，单个元素通过 `left`、`center` 和 `right` 类分为三个区域。

点击列表项对应一个事件，你可以用它来触发操作（参见图 12.4）。`tappable` 属性确保列表项本身有可见的反馈。

![点击列表项后](img/img-f12.4.html)

**图 12.4** 点击列表项后

### 12.1.3 带项目的表格

显示多个元素的另一种方式是通过 `ons-row` 类型的组件及其子组件 `ons-col`。这允许你以类似表格的方式创建单独的行。在每一行内，你可以通过列来创建单独的单元格。与 HTML 表格不同，行之间相互独立，你可以在每一行内单独设置单元格的数量和宽度。在图 12.5 中，你可以看到一个包含三行的表格。

![表格](img/img-f12.5.html)

**图 12.5** 表格

以下是相关程序：

```html
...
<body>
  <ons-page>
    <ons-row>
      <ons-col width="80px">
```



```html
style="background-color:#c0c0c0; padding:10px;">1/1</ons-col>

<ons-col style="background-color:#e0e0e0; padding:10px;">1/2</ons-col>

<ons-col width="80px"
  style="background-color:#c0c0c0; padding:10px;">1/3</ons-col>

</ons-row>

<ons-row>

<ons-col width="40%"
  style="background-color:#b0b0b0; padding:10px;">2/1</ons-col>

<ons-col width="60%"
  style="background-color:#f0f0f0; padding:10px;">2/2</ons-col>

</ons-row>

<ons-row>

<ons-col style="background-color:#c0c0c0; padding:10px;">3/1</ons-col>

<ons-col style="background-color:#e0e0e0; padding:10px;">3/2</ons-col>

</ons-row>

</ons-page>

</body></html>
```

**清单 12.3**　`onsen_table.htm` 文件

这里的单元格具有不同的背景颜色，以便更清晰地显示。在单元格内，你可以使用 `padding` CSS 属性在内容与单元格边缘之间创建间距。

在第一行中，左右两侧各有一个固定宽度为 80 像素的单元格。中间的第三个单元格占据该行的剩余空间。第二行包含两个单元格，分别占据该行宽度的 40% 和 60%。第三行也有两个单元格，由于未指定宽度，它们各占该行宽度的一半。

## 12.2　页面内的元素

在本节中，你将了解各种支持交互的元素。这些元素包括图标、对话框、输入字段和选择字段。

### 12.2.1　图标和浮动操作按钮

你可以集成大量图标，作为易于理解的符号或象形图，用于提供信息或交互提示。你可以像创建字体字符一样，以矢量图形的形式创建这些图标。这意味着你可以轻松更改图标的大小、颜色和其他属性。

浮动操作按钮（FAB）是一个圆形按钮，通常用于触发 Android 应用中最重要的操作。在图 12.6 中，你可以看到来自两个大型图标集合的一些示例，而图 12.7 则展示了一个 FAB。

![各种图标](img/img-f12.6.html)

**图 12.6**　各种图标

![屏幕底部的 FAB](img/img-f12.7.html)

**图 12.7**　屏幕底部的 FAB

以下是相关程序：

```html
...

<body>

<ons-page>

  <ons-list>

    <ons-list-item>

      <ons-icon icon="md-face"></ons-icon>

      <ons-icon icon="md-home"></ons-icon>

      <ons-icon icon="md-zoom-in"></ons-icon>

    </ons-list-item>

    <ons-list-item>

      <ons-icon icon="fa-file"></ons-icon>

      <ons-icon icon="fa-cog"></ons-icon>

      <ons-icon icon="fa-car"></ons-icon>

    </ons-list-item>

    <ons-list-item>

      <ons-icon style="color:#ff0000;" icon="md-home"></ons-icon>

      <ons-icon style="color:#00ff00;" icon="md-home"></ons-icon>

      <ons-icon style="color:#0000ff;" icon="md-home"></ons-icon>

    </ons-list-item>

    <ons-list-item>

      <ons-icon size="10px" icon="md-home"></ons-icon>

      <ons-icon size="20px" icon="md-home"></ons-icon>

      <ons-icon size="30px" icon="md-home"></ons-icon>

    </ons-list-item>

    <ons-list-item>

      <ons-icon spin icon="md-spinner"></ons-icon>

      <ons-icon rotate="90" icon="md-home"></ons-icon>

      <ons-icon rotate="180" icon="md-home"></ons-icon>

      <ons-icon rotate="270" icon="md-home"></ons-icon>

    </ons-list-item>

    <ons-list-item>

      <ons-button id="idHome">

        <ons-icon icon="md-home"></ons-icon> Home

      </ons-button>

    </ons-list-item>

  </ons-list>

  <ons-fab position="bottom right" id="idAction">

    <ons-icon icon="md-plus"></ons-icon>

  </ons-fab>

</ons-page>

<script>
```

```javascript
document.getElementById("idHome").addEventListener("click",
  function(){ons.notification.alert("Home");});

document.getElementById("idAction").addEventListener("click",
  function(){ons.notification.alert("Action");});
```

```html
</script>

</body></html>
```

**清单 12.4**　`onsen_icon.htm` 文件

图标在此处显示在列表项中。

你可以使用 `ons-icon` 组件创建图标。`icon` 属性引用图标的名称，名称的开头表明其来源自广泛使用的图标集合：`fa` 代表 Font Awesome，`md` 代表 Material Design Iconic Font。

你可以使用 `color` CSS 属性更改图标的颜色，并使用 `size` 属性设置大小。`spin` 属性使图标持续旋转，而 `rotate` 属性则用于将图标顺时针旋转 90、180 或 270 度。你还可以将图标集成到其他元素中，例如这里的按钮上。

FAB 通常位于屏幕的某个角落，通常是右下角，但也可以使用 `bottom`、`right`、`top` 和 `left` 值进行定位。FAB 会覆盖该位置的屏幕内容。如果没有特殊定位，FAB 会显示在正常屏幕内容中而不覆盖它。点击 FAB 后，其外观如图 12.8 所示。

![点击 FAB 后](img/img-f12.8.html)

**图 12.8**　点击 FAB 后

### 12.2.2　标准对话框

你已经熟悉了使用 `ons.notification.alert()` 方法的简单标准对话框。还有另外三种标准对话框，具有以下特点：

- `ons.notification.confirm()` 方法对应于用于确认或拒绝的 JavaScript `confirm()` 方法。
- `ons.notification.prompt()` 方法对应于用于输入文本的 JavaScript `prompt()` 方法。
- `ons.notification.toast()` 方法用于引起对某条信息的注意。它会从屏幕底部以消息形式推入，让人联想到从烤面包机中弹出的吐司。

在图 12.9 中，你可以看到一个包含四个按钮的应用程序，用于调用这四种不同的标准对话框。

![调用四种标准对话框的应用程序](img/img-f12.9.html)

**图 12.9**　调用四种标准对话框的应用程序

现在，让我们看看用于评估输入的程序：

```html
...

<body>

<ons-page>

  <ons-list>

    <ons-list-item>

      <ons-button id="idInfo">Information</ons-button>

    </ons-list-item>

    <ons-list-item>

      <ons-button id="idConfirmation">Confirmation</ons-button>

    </ons-list-item>

    <ons-list-item>

      <ons-button id="idInput">Input</ons-button>

    </ons-list-item>

    <ons-list-item>

      <ons-button id="idToast">Toast</ons-button>

    </ons-list-item>

  </ons-list>

</ons-page>

<script>
```

```javascript
function info()
{
  ons.notification.alert("Info");
}

const confirmation = function() {
  ons.notification.confirm("Confirmation?")
    .then(function(sch) {
      if(sch==0) ons.notification.alert("Canceled");
      else ons.notification.alert("Confirmed");
    });
};

const input = function() {
  ons.notification.prompt("Please make an entry")
    .then(function(tx) {
      if(tx=="") ons.notification.alert("No input");
      else ons.notification.alert("Input: " + tx);
    });
};

function toast()
{
  ons.notification.toast("The toast", {timeout: 2000});
}

document.getElementById("idInfo").addEventListener("click", info);

document.getElementById("idConfirmation")
  .addEventListener("click", confirmation);

document.getElementById("idInput").addEventListener("click", input);

document.getElementById("idToast").addEventListener("click", toast);
```

```html
</script>

</body></html>
```

**清单 12.5**　`onsen_dialog.htm` 文件

用于调用对话框的按钮在此处显示在列表项中。

`ons.notification.confirm()` 方法会调用一个包含问题的消息窗口（参见图 12.10）。你可以使用两个按钮：确定和取消。你点击的按钮的内部编号会作为返回值返回，并可以通过 `then()` 方法进行评估。在这里，该值作为参数传递给一个匿名函数。点击取消按钮后，该值为 0。

![标准确认对话框](img/img-f12.10.html)

**图 12.10**　标准确认对话框

`ons.notification.prompt()` 方法会调用一个包含输入字段的消息窗口（参见图 12.11）。同时会显示一个键盘（此处不可见）。输入完成后，你必须点击确定按钮。

![标准输入对话框](img/img-f12.11.html)

**图 12.11**　标准输入对话框

输入的文本随后被返回，也可以通过 `then()` 方法进行评估。在这里，文本同样作为参数传递给一个匿名函数。如果文本是空字符串，则显示相应的消息；否则，显示该字符串本身。

你可以将 `timeout` 参数（以毫秒为单位）传递给 `ons.notification.toast()` 方法。在这种情况下，消息会在指定时间后消失；否则，它会一直保留。在图 12.12 中，你可以看到 toast 的显示效果。

![标准 Toast 对话框](img/img-f12.12.html)

**图 12.12**　标准 Toast 对话框

### 12.2.3　输入字段

`ons-input` 类型的组件在功能上对应于 HTML 的 `input` 元素。你可以使用不同类型的输入字段，用于数字、日期和时间、电话号码、URL、电子邮件地址、文件、颜色、纯文本和密码（另请参见第 4 章，第 4.9 节）。

你还可以添加带有帮助文本的标签和占位符。选择其中一个输入字段后，会显示相应的键盘或选择选项。

`ons-search-input` 类型的组件比带有 `search` 子类型的 `ons-input` 组件更适合输入搜索词。

如果你想从特定范围中选择一个数字，`ons-range` 类型的组件比带有 `range` 子类型的 `ons-input` 组件更合适。更多信息，请参见第 12.2.5 节。

在图 12.13 和图 12.14 中，你可以看到我们提到的带有占位符的类型的示例。

输入表单的末尾有两个按钮。你可以使用第一个按钮显示输入的值以供检查，如图 12.15 所示。第二个按钮将数据发送到 PHP 程序。

![输入字段，上半部分](img/img-f12.13.html)

**图 12.13**　输入字段，上半部分

![输入字段，下半部分](img/img-f12.14.html)

**图 12.14**　输入字段，下半部分

![用于检查的输入值](img/img-f12.15.html)

**图 12.15**　用于检查的输入值

以下是程序代码：

```html
... <head> ...

  <script>
```

```javascript
function values()
{
  ons.notification.alert(
    "Search: " + document.getElementById("se").value
    + "<br>Number: " + document.getElementById("no").value
    + "<br>Date: " + document.getElementById("dt").value
    + "<br>Time: " + document.getElementById("ti").value
    + "<br>Phone: " + document.getElementById("ph").value
    + "<br>URL: " + document.getElementById("ul").value
    + "<br>Email: " + document.getElementById("em").value
    + "<br>Color: " + document.getElementById("co").value
    + "<br>Text: " + document.getElementById("tx").value
    + "<br>Password: " + document.getElementById("pw").value);
}

function submit()
{
  document.getElementById("idForm").submit();
}
```

```html
  </script>
</head>

<body>

<form id="idForm" method="post" action="onsen_input.php">

<ons-page>

  <ons-list>

    <ons-list-item>

      <label for="se" class="left">搜索：</label>

      <ons-search-input id="se" name="se" modifier="underbar"
        placeholder="搜索词"></ons-search-input>

    </ons-list-item>

    <ons-list-item>

      <label for="no" class="left">数字：</label>
```



```html
<ons-input id="no" modifier="underbar" type="number"
  placeholder="123.456" name="no"></ons-input>

</ons-list-item>

<ons-list-item>
  <label for="dt" class="left">日期：</label>
  <ons-input id="dt" modifier="underbar" type="date"
    name="dt"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="ti" class="left">时间：</label>
  <ons-input id="ti" modifier="underbar" type="time"
    name="ti"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="ph" class="left">电话：</label>
  <ons-input id="ph" modifier="underbar" type="phone"
    placeholder="#49-1234-567890" name="ph"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="ul" class="left">网址：</label>
  <ons-input id="ul" modifier="underbar" type="url"
    placeholder="www..." name="ul"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="em" class="left">邮箱：</label>
  <ons-input id="em" modifier="underbar" type="email"
    placeholder="...@..." name="em"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="co" class="left">颜色：</label>
  <ons-input id="co" name="co" modifier="underbar" type="color"
    value="#c0c0c0" style="width:150px;"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="tx" class="left">文本：</label>
  <ons-input id="tx" modifier="underbar" placeholder="输入文本"
    name="tx"></ons-input>
</ons-list-item>

<ons-list-item>
  <label for="pw" class="left">密码：</label>
  <ons-input id="pw" modifier="underbar" type="password"
    placeholder="（不可见）" name="pw"></ons-input>
</ons-list-item>

<ons-list-item>
  <ons-button id="idValues">值</ons-button>
</ons-list-item>

<ons-list-item>
  <ons-button id="idSubmit">提交</ons-button>
</ons-list-item>

</ons-list>
</ons-page>

<script>
document.getElementById("idValues").addEventListener("click", values);
document.getElementById("idSubmit").addEventListener("click", submit);
</script>
</form>
</body></html>
```

**清单 12.6**　`onsen_input.htm` 文件

整个 `ons-page` 组件嵌入在一个表单中，表单内容将发送给一个 PHP 程序。输入字段在此处显示在列表项内。

使用输入字段的 `id` 属性和 `label` 容器的 `for` 属性来关联输入字段和标签。

`modifier` 属性的 `underbar` 值会在组件下方显示一条线，用于定位。可以使用 `placeholder` 属性的值作为占位符，提供输入字段的说明；而 `name` 属性则用于在响应的 PHP 程序中标识输入字段。

### 12.2.4 选择字段

`ons-select` 类型的组件在功能上对应于 HTML 的选择菜单。可以使用 `selected` 属性进行默认设置。

`ons-checkbox` 和 `ons-radio` 类型的组件在功能上对应于 HTML 的选择元素：复选框和单选按钮。可以使用 `checked` 属性设置预选状态。

可以使用 `ons-switch` 类型的组件创建一个开关，提供两个选项之间的选择，例如开和关。可以通过拖动或点击来操作开关，同样使用 `checked` 属性进行默认设置。

在图 12.16 和图 12.17 中，可以看到选择字段的示例。

![选择字段，上半部分](img/img-f12.16.html)

**图 12.16**　选择字段，上半部分

![选择字段，下半部分](img/img-f12.17.html)

**图 12.17**　选择字段，下半部分

在输入表单的末尾，有两个按钮，分别用于显示值（参见图 12.18）和提交表单。

![选中的值，用于控制目的](img/img-f12.18.html)

**图 12.18**　选中的值，用于控制目的

以下是程序代码：

```html
... <head> ...

<script>
function values()
{
  let output = document.getElementById("bo").value + "<br>";

  output += document.getElementById("ov").checked
    ? "有" : "无";

  output += " 海景<br>";

  output += document.getElementById("gy").checked
    ? "有" : "无";

  output += " 健身房权限<br>";

  output += document.getElementById("do").checked
    ? "一张双人床<br>" : "两张单人床<br>";

  output += document.getElementById("sm").checked
    ? "吸烟者<br>" : "非吸烟者<br>";

  ons.notification.alert(output);
}

function submit()
{
  document.getElementById("idForm").submit();
}
</script>
</head>

<body>
<form id="idForm" method="post" action="onsen_selection.php">
<ons-page>
  <ons-list>
    <ons-list-header>膳食</ons-list-header>

    <ons-list-item>
      <ons-select select-id="bo" name="bo">
        <select>
          <option value="仅早餐" selected="selected">仅早餐</option>
          <option value="半膳">半膳</option>
          <option value="全膳">全膳</option>
        </select>
      </ons-select>
    </ons-list-item>

    <ons-list-header>选项</ons-list-header>

    <ons-list-item>
      <label for="mb">海景房</label>
      <label class="left">
        <ons-checkbox id="ov" name="ov"></ons-checkbox>
      </label>
    </ons-list-item>

    <ons-list-item>
      <label for="gy">健身房权限</label>
      <label class="left">
        <ons-switch id="gy" name="gy" checked="checked"></ons-switch>
      </label>
    </ons-list-item>

    <ons-list-header>床型</ons-list-header>

    <ons-list-item>
      <label for="do">一张双人床</label>
      <ons-radio class="left" id="do" name="bed"
        value="一张双人床" checked="checked">
      </ons-radio>
    </ons-list-item>

    <ons-list-item>
      <label for="tw">两张单人床</label>
      <ons-radio class="left" id="tw" name="bed"
        value="两张单人床">
      </ons-radio>
    </ons-list-item>

    <ons-list-header>吸烟</ons-list-header>

    <ons-list-item>
      <label for="sm">吸烟者</label>
      <ons-radio class="left" id="sm" name="smoker"
        value="吸烟者">
      </ons-radio>
    </ons-list-item>

    <ons-list-item>
      <label for="ns">非吸烟者</label>
      <ons-radio class="left" id="ns" name="smoker"
        value="非吸烟者" checked="checked">
      </ons-radio>
    </ons-list-item>

    <ons-list-item>
      <ons-button id="idValues">值</ons-button>
    </ons-list-item>

    <ons-list-item>
      <ons-button id="idSubmit">提交</ons-button>
    </ons-list-item>
  </ons-list>
</ons-page>

<script>
document.getElementById("idValues").addEventListener("click", values);
document.getElementById("idSubmit").addEventListener("click", submit);
</script>
</form>
</body>
</html>
```

**清单 12.7**　`onsen_selection.htm` 文件

同样，整个 `ons-page` 组件被嵌入到一个表单中，表单内容会发送给一个 PHP 程序。选择组件以分组列表项的形式显示。

选择菜单通过 `select-id` 属性标识，`value` 属性提供选择菜单的值。

复选框、开关和单选按钮通过 `id` 属性标识。使用 `?:` 三元运算符来评估 `checked` 属性。

在 HTML 中，`name` 属性用于对单选按钮进行分组，而在 PHP 中评估时则需要 `name` 和 `value` 属性。

### 12.2.5 从数值范围中选择

`ons-range` 类型的组件在功能上对应于带有 `range` 子类型的 `input` HTML 元素。该组件用作滑块，用于从某个范围中选择数字，这些数字也可以是带小数的数字。

你可以定义数值范围的界限、预设值以及变化的增量。你可以通过拖动或点击来操作滑块，在图 12.19 中，你可以看到一个包含三个滑块的示例。

![从数值范围中选择](img/img-f12.19.html)

**图 12.19**　从数值范围中选择

点击“Values”按钮会显示当前值（参见图 12.20）。

![当前值显示](img/img-f12.20.html)

**图 12.20**　当前值显示

以下是程序代码：

```html
... <head> ...

<script>
function values()
{
  ons.notification.alert(
    document.getElementById("rg1").value + "<br>"
    + document.getElementById("rg2").value + "<br>"
    + document.getElementById("rg3").value
  );
}

function submit()
{
  document.getElementById("idForm").submit();
}
</script>
</head>

<body>
<form id="idForm" method="post" action="onsen_range.php">
<ons-page>
  <ons-list>
    <ons-list-item>
      <label for="rg1" class="left">0</label>
      <ons-range id="rg1" name="rg1" value="25"
        style="width:100%;">
      </ons-range>
      <label for="rg1" class="right">100</label>
    </ons-list-item>

    <ons-list-item>
      <label for="rg2" class="left">10</label>
      <ons-range id="rg2" name="rg2" min="10"
        max="20" step="2" value="12" style="width:100%;">
      </ons-range>
      <label for="rg2" class="right">20</label>
    </ons-list-item>

    <ons-list-item>
      <label for="rg3" class="left">1.5</label>
      <ons-range id="rg3" name="rg3" min="1.5"
        max="5.5" step="0.1" value="2.1"
        style="width:100%;">
      </ons-range>
      <label for="rg3" class="right">5.5</label>
    </ons-list-item>

    <ons-list-item>
      <ons-button id="idValues">Values</ons-button>
    </ons-list-item>

    <ons-list-item>
      <ons-button id="idSubmit">Submit</ons-button>
    </ons-list-item>
  </ons-list>
</ons-page>

<script>
document.getElementById("idValues").addEventListener("click", values);
```



```html
document.getElementById("idSubmit").addEventListener("click", submit);
```

```html
</script>

</form>

</body></html>
```

**清单 12.8**　`onsen_range.htm` 文件

整个 `ons-page` 组件也被嵌入到一个表单中，表单内容会发送给一个 PHP 程序。滑块及其范围界限以列表项的形式显示。

默认情况下，范围从 0 到 100，增量为 1。你可以使用 `min` 和 `max` 属性更改范围界限，使用 `step` 属性更改增量。你也可以使用带小数的数字，并使用 `value` 属性进行默认设置。

滑块通过 `id` 属性的值来标识。`value` 属性提供当前值。

### 注意

本书可下载资料（位于[`www.rheinwerk-computing.com/5875`](http://www.rheinwerk-computing.com/5875)）中的附加章节 5 描述了另外三个使用 Onsen UI 库的程序。它们描述了显示多页文档的不同方法。

# 13　使用 MML 和 MathJax 的数学表达式

你可以使用 MathML、MathJax 和 JavaScript 动态且交互地创建数学公式。

你可以使用数学标记语言（MathML）将数学表达式集成到文档中。与 JavaScript 结合使用时，你还有更多动态和交互设计的可能性。W3C 于 2014 年 4 月发布了 MathML 3.0 标准第二版的推荐。MathML 是 HTML 第 5 版的一部分，自 2015 年起已成为 ISO 标准。

不幸的是，MathML 在某些浏览器中不会立即被处理。然而，JavaScript 库 MathJax（[`www.mathjax.org`](https://www.mathjax.org)）使得 MathML 能够在所有现代浏览器中实现，因此我们在本章的示例程序中包含了 MathJax 库。

## 13.1　基本元素

以下程序展示了数学表达式结构的重要基本元素：

```html
... <head> ...

<script id="MathJax-script" async src="https://cdn.jsdelivr.net/

        npm/mathjax@3/es5/tex-mml-chtml.js"></script>

</head>

<body>

<p> 标识符、运算符、数字：

    <math>

       <mi>a</mi>

       <mo>+</mo>

       <mn>2.5</mn>

       <mo>=</mo>

       <mn>3</mn>

       <mi>a</mi>

       <mi>b</mi>

    </math>

</p>

<p> 平方根：

    <math>

        <msqrt> <mi>a</mi> <mo>+</mo> <mn>2.5</mn> </msqrt>

    </math> </p>

<p> 根：

    <math> <mroot> <mi>b</mi> <mn>3</mn> </mroot> </math> </p>

<p> 下标：

    <math> <msub> <mi>a</mi> <mn>2</mn> </msub> </math> </p>

<p> 上标：

    <math> <msup> <mi>b</mi> <mn>-3.5</mn> </msup> </math> </p>

<p> 下标和上标：

    <math>

        <msubsup> <mi>c</mi> <mn>0</mn> <mn>2</mn> </msubsup>

    </math> </p>

<p> 格式：

    <math mathbackground="#909090" mathcolor="#ffffff" mathsize="16pt">

        <msqrt> <mi>a</mi> <mo>+</mo> <mn>2.5</mn> </msqrt>

    </math> </p>

</body></html>
```

**清单 13.1**　`mm_basic_element.htm` 文件

MathJax 库的在线版本包含在文件的头部。地址应该是连续的，并且在一行内。这里由于打印原因分为两行。我们使用 `async` 关键字来确保在构建文档其余部分的同时并行请求在线库。本章其他程序的集成方式相同，因此我们不再重复展示。

数学表达式和公式的所有元素都位于 `<math>` 容器内，而该容器又位于页面的普通文本和 HTML 代码中。

你只需在一个简单的数学表达式中依次编写各个元素。数学标识符存储在 `<mi>` 容器中，运算符存储在 `<mo>` 容器中，数值存储在 `<mn>` 容器中。在数学中，表达式 `3ab` 默认表示乘法 `3 * a * b`，且不带任何乘号。标识符 `a` 和 `b` 是分开的，每个都位于各自的 `<mi>` 容器中。

为了更清晰地概览，你会以更紧凑的形式编写许多以下 MathML 容器，因此嵌入的容器不再位于文件中的独立行中。

你使用 `<msqrt>` 容器来显示平方根。你将所谓的被开方数写在根号下；它是被开方的值。对于平方根，它可以是一个单独的标识符或数字，但也可以是一个更长的表达式，其元素依次编写。

你使用 `<mroot>` 容器来显示一般根。与 `<msqrt>` 容器不同，我们必须在 `<mroot>` 容器内编写两个元素：首先是被开方数（此处为 `b`），然后是根指数（此处为 `3`）。如果这两个元素之一由更长的表达式组成，则必须先将该表达式汇总。你可以使用 `<mrow>` 容器（第 13.3 节）来做到这一点，并且这个汇总规则也适用于后续示例中的许多容器。

你通过使用 `<msub>` 容器来编写标识符的下标。容器内必须有两个元素：首先是标识符，然后是下标。你通过使用 `<msup>` 容器来创建带指数的表达式，容器内也必须有两个元素：底数和指数。你通过使用 `<msubsup>` 容器来编写同时包含下标和指数的表达式。容器内必须有三个元素：标识符、下标和指数。

对于 `<math>` 容器以及许多用于单个元素的容器，你可以通过 `mathbackground`、`mathcolor` 和 `mathsize` 属性来设置背景颜色、字体颜色和字体大小。

数学表达式显示在图 13.1 中。

![MathML 基本元素](img/img-f13.1.html)

**图 13.1**　MathML 基本元素

## 13.2　括号与表格

在数学表达式中，子表达式通过括号组合在一起，以便优先计算。MathML 使用括号来直观地表示这种运算顺序。括号也是汇总表达式所必需的，并且用于表示向量或矩阵。你可以使用任何括号字符，并处理多个括号层级。

你可以使用表格来清晰地表示二维结构。在此示例中，使用表格显示了一个矩阵和一个方程组。

首先来看示例程序：

```html
...

<body>

<p> 单层括号：

    <math> <mfenced separators="">

              <mi>a</mi> <mo>+</mo> <mi>b</mi>

           </mfenced> </math> </p>

<p> 双层括号：

    <math>

      <mfenced open="{" close="}" separators="">

        <mfenced separators=""> <mi>a</mi> <mo>+</mo>

                                <mi>b</mi> </mfenced>

        <mfenced separators=""> <mi>c</mi> <mo>+</mo>

                                <mi>d</mi> </mfenced>

      </mfenced>

    </math> </p>

<p> 表格，用于方程组：

    <math> <mtable>

              <mtr>

                 <mtd> <mn>1.5</mn> <mo>+</mo> <mi>a</mi> </mtd>

                 <mtd> <mo>=</mo> </mtd>

                 <mtd> <mi>b</mi> </mtd>

              </mtr>

              <mtr>

                 <mtd> <mi>a</mi> </mtd>

                 <mtd> <mo>=</mo> </mtd>

                 <mtd> <mn>4.2</mn> <mo>-</mo> <mi>b</mi> </mtd>

              </mtr>

           </mtable> </math> </p>

<p> 表格，用于矩阵：

    <math> <mi>X</mi> <mo>=</mo>

      <mfenced separators="">

        <mtable>

          <mtr> <mtd> <mn>1.5</mn> </mtd> <mtd> <mi>a</mi>   </mtd> </mtr>

          <mtr> <mtd> <mi>b</mi>   </mtd> <mtd> <mn>2.8</mn> </mtd> </mtr>

        </mtable>

      </mfenced>

    </math> </p>

</body></html>
```

**清单 13.2**　`mm_parenthesis_table.htm` 文件

你可以使用 `<mfenced>` 容器来显示一对带括号的定界符。元素在容器内依次编写，`separators` 属性的值表示用于分隔各个元素的字符串。默认情况下，该字符串是逗号字符。在此示例中，它是一个空字符串。

你可以使用嵌套的 `<mfenced>` 容器来实现多个括号层级，并且 `open` 和 `close` 属性允许你为每对括号定义两个字符串，分别用作左括号和右括号。

MathML 表格的结构和用途与 HTML 表格类似。表格使用 `<mtable>` 容器，表格内的行使用 `<mtr>`，行内的数据单元格使用 `<mtd>`。

在第一个表格示例中，两个方程式的左侧、等号和右侧借助表格上下对齐显示。你可以像第二个表格示例那样，将整个表格放在括号内。这样可以将数据显示为矩阵。

在图 13.2 中，你可以看到带括号和表格的数学表达式。

![括号与表格](img/img-f13.2.html)

**图 13.2**　括号与表格

## 13.3　汇总表达式

`<mrow>` 容器允许你将一个较长的表达式汇总为单个元素。许多容器要求对其元素执行此操作。

你可以使用 `<munderover>` 容器在字符下方和上方输入必要的信息。例如，这些可以是积分、求和或乘积的符号。

下面是一些示例：

```html
...

<body>

<p>创建平方根的摘要：

    <math> <mroot>

              <mrow> <mi>a</mi> <mo>+</mo> <mn>2.5</mn> </mrow> <mn>3</mn>

           </mroot> </math> </p>

<p>积分：

    <math> <munderover>

              <mo>&int;</mo> <mn>0</mn> <mn>1</mn>

           </munderover>

           <mi>x</mi> <mi>d</mi> <mi>x</mi> </math> </p>

<p>创建求和的摘要：

    <math> <munderover>

              <mo>&sum;</mo>

              <mrow> <mi>k</mi> <mo>=</mo> <mn>3</mn> </mrow>

              <mn>5</mn>

           </munderover>

           <mi>k</mi> <mo>=</mo>

             <mn>3</mn> <mo>+</mo> <mn>4</mn> <mo>+</mo> <mn>5</mn>

           <mo>=</mo> <mn>12</mn> </math> </p>

<p>创建乘积的摘要：

    <math> <munderover>

              <mo>&prod;</mo>

              <mrow> <mi>k</mi> <mo>=</mo> <mn>3</mn> </mrow>

              <mn>5</mn>

           </munderover>

           <mi>k</mi> <mo>=</mo> <mn>3</mn> <mo>&sdot;</mo>

             <mn>4</mn> <mo>&sdot;</mo> <mn>5</mn>

           <mo>=</mo> <mn>60</mn> </math> </p>

</body></html>
```

**清单 13.3**　`mm_summary.htm` 文件

根号下的被开方数是一个较长的表达式，因此需要将其放在 `<mrow>` 容器中。或者，你也可以使用不带可见括号的 `<mfenced>` 容器。

HTML 特殊字符 `&int;` 用于创建积分符号。`<munderover>` 容器中必须包含三个元素：实际的主元素、元素下方的信息和元素上方的信息。如果在示例中将 `dx` 字符串放在普通的 `<mi>` 容器中，则无法正确表示数学含义，因此最好将 `d` 和 `x` 字符分别放在各自的 `<mi>` 容器中。

HTML 特殊字符 `&sum;` 和 `&prod;` 分别用于创建求和符号和乘积符号。`<munderover>` 容器中的下方规格包含一个较长的表达式，因此必须进行汇总。在计算乘积的中间步骤中，使用 HTML 特殊字符 `&sdot;` 来显示乘号，以便更清晰。

在图 13.3 中，你可以看到汇总后的表达式、积分、求和以及乘积。

![汇总表达式、积分、求和与乘积](img/img-f13.3.html)

**图 13.3**　汇总表达式、积分、求和与乘积

## 13.4　分数

你可以使用 `<mfrac>` 容器来显示分数。通常使用水平分数线，但也可以使用斜分数线。你还可以嵌套包含分数的表达式，这样就有机会在分子或分母中表示分数。下面是一些示例：

```html
...

<body>

<p>分数，水平：

    <math>

        <mfrac>

            <mi>a</mi> <mn>3</mn>

        </mfrac>

    </math> </p>

<p>分数，倾斜：

    <math>

      <mfrac bevelled="true"> <mi>a</mi> <mn>3</mn> </mfrac>

    </math> </p>

<p>分数，水平，带表达式：

    <math>

        <mfrac>

          <mrow> <mi>a</mi> <mo>+</mo> <mi>b</mi> </mrow>

          <mn>2</mn>

        </mfrac>

    </math> </p>

<p>分数，水平，多重：

    <math mathsize="16pt">

       <mfrac>

           <mrow>

             <mfrac>

                <mrow> <mi>a</mi> <mo>+</mo> <mi>b</mi> </mrow>

                <mn>2</mn>

             </mfrac>

             <mo>+</mo>

             <mn>3</mn>

           </mrow>

           <mi>c</mi>

       </mfrac>

    </math> </p>

</body></html>
```

**清单 13.4**　`mm_fraction.htm` 文件

正如预期，`<mfrac>` 容器中必须包含两个元素：分子和分母。`bevelled` 属性的值为 `true` 时，会创建斜分数线而不是水平分数线。你可以使用 `<mrow>` 容器来转换分子或分母中的较长表达式。

在最后一个示例中，分子包含一个较长的表达式，该表达式又由一个分数和其他元素组成。这里建议使用更大的字号。

你可以在图 13.4 中看到各种分数。

![分数](img/img-f13.4.html)

**图 13.4**　分数

## 13.5　数学符号

有一系列 HTML 特殊字符适合在 MathML 表达式中显示运算符。在下面的两部分程序中，你可以看到其中一些符号及其简要说明：

```html
...

<body>

<p>比较：<br>

    <math> <mo>&sim;</mo> </math> 相似于<br>

    <math> <mo>&asymp;</mo> </math> 约等于，四舍五入<br>

    <math> <mo>&ne;</mo> </math> 不等于<br>

    <math> <mo>&lt;</mo> </math> 小于<br>
```



<math> <mo>&gt;</mo> </math> 大于

<math> <mo>&le;</mo> </math> 小于或等于

<math> <mo>&ge;</mo> </math> 大于或等于

逻辑：

<math> <mo>&and;</mo> </math> 逻辑与

<math> <mo>&or;</mo> </math> 逻辑或

<math> <mo>&not;</mo> </math> 逻辑非

<math> <mo>&rarr;</mo> </math> 如果……则……（条件）

<math> <mo>&harr;</mo> </math> 当且仅当（双条件）

...

```html
<p>集合：<br>

    <math> <mo>&isin;</mo> </math> 属于<br>

    <math> <mo>&notin;</mo> </math> 不属于<br>

    <math> <mo>&cap;</mo> </math> 交集<br>

    <math> <mo>&cup;</mo> </math> 并集</p>

<p>角度：<br>

    <math> <mo>&deg;</mo> </math> 度<br>

    <math> <mo>&prime;</mo> </math> 分<br>

    <math> <mo>&Prime;</mo> </math> 秒<br>

    <math> <mo>&alpha;</mo> </math> 阿尔法<br>

    <math> <mo>&beta;</mo> </math> 贝塔<br>

    <math> <mo>&gamma;</mo> </math> 伽马</p>

<p>其他符号：<br>

    <math> <mo>&Delta;</mo> </math> 德尔塔，差值<br>

    <math> <mo>&pi;</mo> </math> 圆周率<br>

    <math> <mo>&micro;</mo> </math> 微<br>

    <math> <mo>&plusmn;</mo> </math> 正负号<br>

    <math> <mo>&infin;</mo> </math> 无穷大</p>

</body></html>
```

**清单 13.6**　`mm_symbols.htm` 文件，第 2 部分（共 2 部分）

这些字符显示在图 13.6 中。

![数学符号，第 2 部分](img/img-f13.6.html)

**图 13.6**　数学符号，第 2 部分

## 13.6 动态生成的表达式

在已完全加载的文档中动态插入数学表达式非常耗时。因此，在本节中，我使用了两个独立的文档：`location` 对象和搜索字符串的传递（另请参见第 4 章，第 4.8 节）。

数据在第一个文档中输入，然后通过 JavaScript 发送到第二个文档，在文档加载时数据将完全可用。然后，再次使用 JavaScript 将数据插入到数学表达式中。

在本例中，计算了两个各含三个分量的向量的标量积。标量积等于对应分量乘积之和，本例中的计算结果如下：

```javascript
sp = 3.2 * (-2.6) + (-2.7) * 0.6 + 1.9 * 3.4 = -3.48
```

输入分量并用空格分隔（参见图 13.7）。提交后，计算结果并输出整个表达式（参见图 13.8）。

![输入分量](img/img-f13.7.html)

**图 13.7**　输入分量

![计算结果与表示](img/img-f13.8.html)

**图 13.8**　计算结果与表示

此处展示的技术可应用于更复杂的示例，例如两个任意数量分量的向量的标量积，或两个矩阵的乘法。

首先，这是输入程序：

```html
... <head> ...

   <script>
```

```javascript
function calculate()
{
   const tx1 = document.getElementById("idVector1").value;
   const v1 = tx1.split(" ");

   const tx2 = document.getElementById("idVector2").value;
   const v2 = tx2.split(" ");

   if(v1.length != 3 || v2.length != 3)
   {
      alert("There must be three components in each case");
      return;
   }

   location.href = "mm_sp_output.htm"
      + "?v10=" + v1[0] + "&v11=" + v1[1] + "&v12=" + v1[2]
      + "&v20=" + v2[0] + "&v21=" + v2[1] + "&v22=" + v2[2];
}
```

```html
</script>
</head>

<body>

<p>Three components of the first vector, separated by
   spaces:<br><input size="20" id="idVector1"></p>

<p>Three components of the second vector, separated by
   spaces:<br><input size="20" id="idVector2"></p>

<p><input type="button" id="idCalculate"
   value="Calculate and display scalar product"></p>

<script>
```

```javascript
document.getElementById("idCalculate").addEventListener("click", calculate);
```

```html
</script>

</body></html>
```

**清单 13.7**　`mm_sp_input.htm` 文件

输入数据并点击按钮后，两个输入字符串按空格分割并存储到字段中。如果任一字段不包含恰好三个元素，程序将退出。利用所需的特殊字符 `?`、`&` 和 `=` 以及两个字段的内容，拼接出搜索字符串，并调用第二个文档。

接下来是评估程序：

```html
...

<body>

<script>
```

```javascript
const v = new Array();

const search_field = location.search.split("&");

for(let i=0; i<search_field.length; i++)
{
   if(i==0)
      search_field[0] = search_field[0].substr(1);

   const parts = search_field[i].split("=");
   v.push(parts[1]);
}

document.write("Scalar product: <math>");

document.write("<mfenced separators=''> <mtable>");

for(let i=0; i<3; i++)
   document.write("<mtr> <mtd> <mn>" + v[i] + "</mn> </mtd> </mtr>");

document.write("</mtable> </mfenced>");

document.write("<mo>&sdot;</mo>");

document.write("<mfenced separators=''> <mtable>");

for(let i=0; i<3; i++)
   document.write("<mtr> <mtd> <mn>" + v[i+3] + "</mn> </mtd> </mtr>");

document.write("</mtable> </mfenced>");

let sp = 0;

for(let i=0; i<3; i++)
   sp += v[i] * v[i+3];

document.write("<mo>=</mo> <mn>" + sp.toFixed(2) + "</mn>");
document.write("</math>");
```

```html
</script>

</body></html>
```

**清单 13.8**　`mm_sp_output` 文件

搜索字符串再次利用特殊字符进行拆分，两个向量的总共六个分量存储在一个字段中。使用 `<mfenced>` 和 `<mtable>` 容器显示两个向量的值，计算并显示标量积。

# 14 示例项目

较大的项目能很好地展示 JavaScript 各种功能的交互。

在本章中，我将描述几个较大的示例项目。首先，你将看到三个面向实践的项目：

- 金融投资价值的计算
- 健身领域数值的计算与评估
- 趣味跑报名，包含输入值检查

接着是三个游戏领域的项目：

- 一款纸牌游戏，需要冷静思考后将扑克牌按特定顺序放置
- 双人版本的记忆配对游戏
- 技巧游戏贪吃蛇，玩家控制屏幕上的对象

这些程序在开发过程中也需要仔细规划，最终产品与严肃程序一样受欢迎。

你可以在本书的可下载材料中找到所有程序作为附加内容，并附有大量解释性注释。通常，你可以通过这些程序理解 JavaScript 在交互中的能力，也可以根据自己的想法扩展这些程序。

## 14.1 金融投资

该程序位于 `investment.htm` 文件中，页面底部显示了银行提供的各种条件。你可以输入投资金额和期望期限，点击“计算”按钮后，程序处理输入值并返回到期时的金额（参见图 14.1）。

![金融投资](img/img-f14.1.html)

**图 14.1**　金融投资

## 14.2 健身数值

你可以在 `fitness.htm` 文件中找到该程序，页面顶部可以输入个人数据——年龄、身高、体重、静息心率和性别。

点击“计算”按钮后，程序检查输入值，并使用它们根据卡沃宁公式计算身体质量指数和训练心率（参见图 14.2）。

![健身数值](img/img-f14.2.html)

**图 14.2**　健身数值

## 14.3 趣味跑

该程序位于 `fun_run.htm` 文件中，你可以输入个人数据（参见图 14.3）。姓氏、名字和同意数据存储为必填字段，并且必须选择性别、出生年份和距离，使其相互匹配。在图 14.4 中，你可以看到可跑各种距离的展开选择菜单。

在真实的趣味跑报名中，数据随后会通过 PHP 存储到 MySQL 数据库中，你可以查看已注册参与者列表以进行核对。组织者可以选择在受保护区域将所有数据从数据库导出为 CSV 文件（例如用于 Microsoft Excel）。这简化了跑步评估以及结果列表和证书的打印。

![趣味跑报名](img/img-f14.3.html)

**图 14.3**　趣味跑报名

![各种距离](img/img-f14.4.html)

**图 14.4**　各种距离

## 14.4 纸牌游戏

该程序位于 `solitaire` 子目录下的 `solitaire.htm` 文件中。你还可以在那里找到相应的图像文件，包括 52 张扑克牌的图像。

在图 14.5 中，你可以看到初始顺序的牌，该顺序在游戏开始时随机生成。点击“规则”按钮后，你将看到游戏过程的描述（参见图 14.6）。

![游戏开始时的牌序](img/img-f14.5.html)

**图 14.5**　游戏开始时的牌序

![游戏规则](img/img-f14.6.html)

**图 14.6**　游戏规则

最后，所有卡片应按正确顺序排列。

## 14.5 配对游戏

你可以在 `concentration` 子目录下的 `concentration.htm` 文件中找到这个程序，同时也能找到相关的图像文件（包括需要寻找的 18 对匹配卡片）。你可以在图 14.7 中看到游戏进行中的结果。

![游戏进行中的结果](img/img-f14.7.html)

**图 14.7**　游戏进行中的结果

玩家 2 已经找到了三对卡片，而玩家 1 只找到了一对。现在轮到玩家 1，他刚刚翻开了第二张卡片。两位玩家有 2 到 3 秒的时间记住这两张正面朝上卡片的位置，你可以看到所有剩余卡片的背面。点击“规则”按钮后，会显示游戏过程的说明（参见图 14.8）。

![游戏规则](img/img-f14.8.html)

**图 14.8**　游戏规则

玩家 1 和玩家 2 通常轮流进行，但当某位玩家找到一对匹配的卡片时，该玩家可以立即再玩一轮。

## 14.6 贪吃蛇

你可以在 `snake.htm` 文件中找到这个程序。调用程序后，蛇会立即自动在屏幕上移动，你可以使用四个方向键控制它的移动方向，以便蛇能捕捉到它的猎物（参见图 14.9）。一旦蛇撞到周围的墙壁，游戏结束。

![蛇与猎物](img/img-f14.9.html)

**图 14.9**　蛇与猎物

一旦蛇到达猎物位置，得分增加一分。然后猎物会出现在一个新的随机位置，蛇再次尝试到达那里。同时，蛇的速度会加快，因此更难控制，随着分数的增加，游戏自然走向终点。

# 15 媒体、绘图与传感器

自 HTML 5 版本发布以来，HTML 提供了额外的功能，这些功能也与 JavaScript 结合使用。

自 HTML 5 版本发布以来，HTML 提供了一些额外的功能，这些功能与 JavaScript 结合也很有趣。这些功能包括音频和视频文件的播放、画布绘图，以及使用移动设备的定位数据、位置和加速度的接收器或传感器。

## 15.1 播放媒体文件

与 HTML 5 版本之前存在的选项相比，`audio` 和 `video` 标签使得播放音频和视频文件变得更加容易。

### 15.1.1 音频文件

在你的文档中，你可以使用 `audio` 标签部署一个音频播放器，它包含一些显示和控制元素：播放/暂停按钮、模拟和数字进度指示器以及音量控制。如果需要，你还可以隐藏音频播放器或通过事件来控制它。

以下是一个包含两个波形音频文件格式（WAV）文件和总共三个音频播放器的示例（参见图 15.1）。

第一个音频播放器可以像平常一样操作，但第二个音频播放器不可见，你只能通过事件和 JavaScript 来控制它。

第三个播放器展示了更多选项。你可以执行以下操作：

- 暂停或继续播放过程。
- 从某个特定点继续播放过程。
- 开启或关闭无限重复。
- 调整音量。
- 在两个 WAV 文件之间切换。

![三个音频播放器](img/img-f15.1.html)

**图 15.1**　三个音频播放器

让我们先看文档的下半部分：

```html
...

<body>

   <p>音频播放器 1：</p>

   <p><audio src="guitar.wav" controls></audio></p>

   <p> </p>

   <!-- 音频播放器 2： -->

   <audio id="idAudioHidden" src="chord.wav" hidden></audio>

   <p><input id="idHidden" type="button"
       value="播放隐藏的音频播放器"></p>

   <p> </p>

   <p>音频播放器 3：</p>

   <p>
      <audio id="idAudioThree" src="guitar.wav" loop></audio>
      <input id="idPlay" type="button" value="播放">
      <input id="idPause" type="button" value="暂停">
      <input id="idSet" type="button" value="设置到 1.5">
      <input id="idLoop" type="checkbox" checked="checked"> 循环
   </p>

   <p><input id="idVolumeUp" type="button" value="音量增大">
      <input id="idVolumeDown" type="button" value="音量减小">
      <span id="idDisplayThree">(100%)</span></p>

   <p><input id="idGuitar" name="selection" type="radio"
              value="Guitar" checked="checked"> guitar.wav
      <input id="idChord" name="selection" type="radio"
           value="Chord"> chord.wav</p>

   <script>
```



```javascript
const audioHidden =
  document.getElementById("idAudioHidden");

document.getElementById("idHidden").addEventListener(
  "click",
  function () {
    audioHidden.play();
  }
);

const audioThree = document.getElementById("idAudioThree");

document.getElementById("idPlay").addEventListener(
  "click",
  function () {
    audioThree.play();
  }
);

document.getElementById("idPause").addEventListener(
  "click",
  function () {
    audioThree.pause();
  }
);

document.getElementById("idSet").addEventListener(
  "click",
  function () {
    audioThree.currentTime = 1.5;
  }
);

document.getElementById("idLoop").addEventListener(
  "click",
  function () {
    audioThree.loop = !audioThree.loop;
  }
);

document.getElementById("idVolumeUp").addEventListener(
  "click",
  function () {
    volume(0.2);
  }
);

document.getElementById("idVolumeDown").addEventListener(
  "click",
  function () {
    volume(-0.2);
  }
);

document.getElementById("idGuitar").addEventListener(
  "click",
  function () {
    change("guitar");
  }
);

document.getElementById("idChord").addEventListener(
  "click",
  function () {
    change("chord");
  }
);
```

```html
</script>

</body></html>
```

**清单 15.1**　`audio.htm` 文件，音频元素和事件处理程序

关于三个音频播放器的一些说明：

- 对于第一个播放器，你使用 `src` 属性的值指定音频文件的名称，并使用 `controls` 属性显示操作元素。
- 第二个播放器除了 `src` 属性外，还有 `hidden` 属性。这确保它虽然存在且可用，但不可见。唯一的 ID 通过 JavaScript 建立了与控制器的连接。
- 第三个播放器输入了 `loop` 属性，这会启动无限播放过程。

接下来是一个用于操作隐藏播放器的按钮，并且在 JavaScript 部分设置了指向该播放器的链接。点击“播放隐藏的音频播放器”按钮会调用该播放器的 `play()` 方法。

总共有五个按钮、一个复选框和一组两个单选按钮，用于操作第三个播放器。在 JavaScript 部分也设置了指向该播放器的引用。点击“播放”和“暂停”按钮会调用 `play()` 和 `pause()` 方法。你使用 `currentTime` 属性来确定或设置播放过程的当前位置，并使用复选框来激活或停用用于无限重复的布尔属性 `loop`。

您无法预设音量值。最初，您听到的声音是输出设备（PC、智能手机等）当前设置的音量，这对应于 `volume` 属性的值 1。您通过音量增大和音量减小按钮调用 `volume()` 函数。改变音量的值作为参数传递，改变后的音量只能在 0 到 1 之间。您使用两个单选按钮来选择要播放的音频文件。

现在，来看文档的上半部分：

```html
... <head> ...

<script>
```

```javascript
function volume(value) {
  audioThree.volume += value;

  document.getElementById("idDisplayThree")
    .firstChild.nodeValue =
    "(" + (100 * audioThree.volume).toFixed(0) + "%)";
}

function change(filename) {
  audioThree.src = filename + ".wav";
  audioThree.load();
  audioThree.play();
}
```

```html
</script>

</head>

...
```

**清单 15.2**　`audio.htm` 文件

您可以在 `volume()` 函数中更改 `volume` 属性的值，这将改变您最初听到的音量百分比，从 100% 变为新的百分比。

在 `change()` 函数中，您通过函数参数为 `src` 属性赋予新值。该属性包含播放器的音频文件名，`load()` 方法加载相应的音频文件，然后您可以通过 `play()` 播放它。

### 15.1.2　视频文件

您可以使用浏览器中的 `video` 标签播放视频文件。并非所有浏览器都支持所有视频格式，因此将视频文件转换为多种格式并使用 `source` 标签集成所有格式是合理的。将使用第一个被识别的格式，并且有许多免费软件程序允许您将一种格式转换为另一种格式。

除了在标记 `audio` 内容时学到的属性外，还有 `width` 和 `height` 属性，您可以使用它们在加载过程中为视频在网站内预留和定义区域。在 JavaScript 中，您可以使用与音频文件相同的属性。

在图 15.2 中，您可以看到一个短视频的显示。如果视频当前未播放或鼠标光标悬停在视频上，则会显示控制栏。

![带控制栏的视频文件](img/img-f15.2.html)

**图 15.2**　带控制栏的视频文件

以下是程序代码：

```html
...

<body>

<video width="400" height="300" controls loop>
  <source
    src="shadow1.mp4"
    type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'
  >
  <source
    src="shadow1.ogv"
    type='video/ogg; codecs="theora, vorbis"'
  >
  <source
    src="shadow1.webm"
    type='video/webm; codecs="vp8, vorbis"'
  >
</video>

</body>
</html>
```

**清单 15.3**　`video.htm` 文件

为视频预留并定义了一个 400×300 像素的区域。一个 `video` 容器内可以有多个 `source` 标签，每种情况下，您都希望使用 `src` 属性指定正在播放的文件名。

指定 MIME 类型（包括编解码器）有助于浏览器分配文件。编解码器标识模拟视频录制被数字化的过程。

## 15.2　Canvas

`canvas` 标签在网站内创建一个空白画布。然后您可以使用 JavaScript 创建绘图、插入图像或输出格式化文本等。

### 15.2.1　绘图

在图 15.3 中，您可以看到一些绘图元素，每次单击其中一个按钮时都会生成这些元素。您使用“清除”按钮清除画布。

先来看文档的下半部分：

```html
...

<body>

<canvas
  id="idCanvas"
  width="400"
  height="300"
  style="border:solid 1px #000000;"
></canvas>

<p>
  <input id="idRect" type="button" value="Rectangle">
  <input id="idArc" type="button" value="Arc">
  <input id="idLine" type="button" value="Line">
  <input id="idClear" type="button" value="Clear">
</p>

<p>
  <input
    id="idGradientLin"
    type="button"
    value="Linear gradient"
  >
  <input
    id="idGradientRad"
    type="button"
    value="Radial gradient"
  >
</p>

<script>
```

```javascript
const c = document.getElementById("idCanvas");
const ct = c.getContext("2d");

ct.fillStyle = "#f0f0f0";
ct.lineWidth = 1;
ct.strokeStyle = "#000000";

document.getElementById("idRect")
  .addEventListener("click", rectangle);

document.getElementById("idArc")
  .addEventListener("click", arc);

document.getElementById("idLine")
  .addEventListener("click", line);

document.getElementById("idClear")
  .addEventListener("click", clear);

document.getElementById("idGradientLin")
  .addEventListener("click", gLinear);

document.getElementById("idGradientRad")
  .addEventListener("click", gRadial);
```

```html
</script>

</body>
</html>
```

**清单 15.4**　`canvas.htm` 文件，下半部分

画布大小为 400×300 像素，周围环绕着细黑边框，以便在页面中更好地可见。然后是六个按钮。

![画布中的图形元素](img/img-f15.3.html)

**图 15.3**　画布中的图形元素

在 JavaScript 部分，变量 `c` 被引入作为对 `canvas` 元素的引用。`getContext()` 方法返回一个可用于绘图的对象。进行了一些默认设置，这些设置一直适用，直到进行其他设置；之后，新设置生效：

- `fillStyle` 属性标识对象的填充类型和颜色。默认情况下，对象以黑色均匀填充。此处设置为灰色，但您可以指定图案或渐变（即颜色渐变）。
- `lineWidth` 属性表示线条粗细。其默认值为 1。
- `strokeStyle` 属性标识线条样式和颜色。默认情况下，线条以黑色连续绘制，但您可以设置不同的线条类型。

最后，是六个按钮的事件处理程序。

现在来看文档的上半部分，其中包含创建矩形、弧线和线条的函数：

```html
... <head> ...

<script>
```

```javascript
function rectangle() {
  ct.fillRect(5, 25, 75, 100);
  ct.strokeRect(5, 25, 75, 100);
}

function pathArc() {
  ct.beginPath();
  ct.arc(150, 75, 50, 0, 1.5 * Math.PI);
  ct.fill();
  ct.stroke();
}

function pathLine() {
  ct.beginPath();
  ct.moveTo(225, 25);
  ct.lineTo(300, 50);
  ct.lineTo(300, 100);
  ct.lineTo(225, 125);
  ct.fill();
  ct.stroke();
}
```

**清单 15.5**　`canvas.htm` 文件，上半部分

在 `rectangle()` 函数中，你使用 `fillRect()` 方法，根据当前设置的填充类型和颜色创建一个填充矩形。前两个参数表示左上角的 x 和 y 坐标，指示该角距离画布左边缘或上边缘的距离。接下来的两个参数指定矩形的宽度和高度值。

`strokeRect()` 方法使用当前设置的线条类型和颜色创建一个空心矩形。参数相同，因此空心矩形构成了填充矩形的边框。

你可以沿路径创建填充或空心的圆弧，或填充或空心的折线。在 `pathArc()` 函数中，你使用 `beginPath()` 方法初始化路径。

`arc()` 方法创建一个圆弧。前两个参数表示绘制圆弧所围绕的圆心的 x 和 y 坐标，下一个参数指定圆弧的半径。

最后两个参数指示起始角度和结束角度。角度以弧度为单位，在示例中，起始角度为 0 度。通常，这位于 3 点钟方向，并顺时针旋转到 270 度（即 12 点钟方向）。2π 弧度对应 360 度。

`fill()` 方法创建路径的轮廓并填充它，你在路径的起点和终点之间绘制填充。`stroke()` 方法仅绘制路径的轮廓。

`pathLine()` 函数中的路径由单独的线段组成，而 `moveTo()` 方法将绘图笔移动到指定 x 和 y 坐标的点。`lineTo()` 方法绘制一条连接到指定点的线。

现在，这里是文档的中间部分，包含用于创建渐变和清除画布的函数：

```javascript
...

function gLinear() {
  const gr = ct.createLinearGradient(5, 150, 80, 250);

  gr.addColorStop(0.0, "#000000");
  gr.addColorStop(0.5, "#ffffff");
  gr.addColorStop(1.0, "#000000");

  ct.fillStyle = gr;
  ct.fillRect(5, 150, 75, 100);
  ct.fillStyle = "#f0f0f0";
}

function gRadial() {
  const gr = ct.createRadialGradient(150, 200, 0, 150, 200, 50);

  gr.addColorStop(0.0, "#000000");
  gr.addColorStop(0.5, "#ffffff");
  gr.addColorStop(1.0, "#000000");

  ct.fillStyle = gr;
  ct.beginPath();
  ct.arc(150, 200, 50, 0, 2 * Math.PI);
  ct.fill();
  ct.fillStyle = "#f0f0f0";
}

function clear() {
  ct.clearRect(0, 0, 400, 300);
}
```

```html
</script>

</head>

...
```



**清单 15.6**　canvas.htm 文件，中间部分

你在`gLinear()`函数中生成线性渐变。你必须将渐变想象成一条直线，图形对象的填充颜色沿这条直线变化。`createLinearGradient()`方法的前两个参数表示直线起点的 x 和 y 坐标，接下来的两个参数表示直线终点的 x 和 y 坐标。

该方法返回一个提供对直线访问的对象。`addColorStop()`方法将特定颜色分配给直线上的各个点，第一个参数标识直线上的点。0.0 点代表直线的起点，1.0 点代表直线的终点，0 到 1 之间的所有值都在中间（例如，0.5 点位于中点）。

创建渐变后，它被分配给`fillStyle`属性作为当前的填充类型和颜色。为了说明颜色渐变，你可以创建一个使用渐变的填充矩形，并选择渐变的坐标，使矩形的左上角位于渐变的起点，右下角位于渐变的终点。然后，你可以为随后创建的图形对象设置不同的填充类型和颜色。

你在`gRadial()`函数中创建径向颜色渐变。`createRadialGradient()`方法需要两个圆的信息：第一个圆标记颜色渐变的起点，第二个圆标记其终点。你使用圆心的 x 和 y 坐标以及半径依次创建这两个圆。这产生了该方法的六个参数。

为了说明颜色渐变，你可以创建一个使用渐变的圆弧。圆弧从 0 度到 360 度完整绘制，你选择渐变的坐标，使圆弧的圆心位于第一个圆上，圆弧的边缘位于第二个圆上。

### 15.2.2 图像

你可以使用`drawImage()`方法在画布中显示图像。你可以按原始大小或缩放将图像添加到绘图中，也可以添加图像的一个部分（参见图 15.4 中的示例）。

![多次显示图像](img/img-f15.4.html)

**图 15.4**　多次显示图像

以下是程序代码：

```html
...

<body>

   <canvas id="idCanvas" width="400" height="220"

           style="border:solid 1px #000000;"></canvas>

   <p><input id="idOriginal" type="button" value="Original">

      <input id="idScale" type="button" value="Scale">

      <input id="idSection" type="button" value="Section"></p>

   <script>
```

```javascript
 const c = document.getElementById("idCanvas");

      const ct = c.getContext("2d");

      const image = document.createElement("img");

      image.src = "im_paradise.jpg";

      document.getElementById("idOriginal").addEventListener

         ("click", function() {ct.drawImage(image, 5, 25);} );

      document.getElementById("idScale").addEventListener

         ("click", function()

         {ct.drawImage(image, 205, 25, 120, 90);} );

      document.getElementById("idSection").addEventListener

         ("click", function()

         {ct.drawImage(image, 0, 60, 80, 60, 205, 150, 80, 60);} );
```

```html
 </script>

</body></html>
```

**清单 15.7**　canvas_image.htm 文件

画布大小为 400 × 220 像素，带有细黑色边框。随后是三个用于创建三个对象的按钮。

在 JavaScript 部分，你通过使用`createElement()`方法创建一个新的`img`类型的 HTML 元素，并将其引用赋给`image`变量。图像文件的名称被赋给 HTML 元素的`src`属性，但图像尚未添加到文档中。

你可以通过使用`drawImage()`方法在文档中显示该 HTML 元素。随后是三个事件处理程序，它们导致对该方法的不同调用。你可以使用三个、五个或九个参数调用该方法，这些参数的作用如下：

- 第一个参数引用要显示的`img`类型的 HTML 元素。
- 参数 2 和 3 表示图像左上角的 x 和 y 坐标。
- 参数 4 和 5 指定图像的可见宽度和高度。应保持宽高比。
- 如果在调用时传递了九个参数，则参数 2 到 5 会被向后移动。新的参数 2 和 3 标记图像中图像部分的左上角，图像部分的大小则跟在参数 4 和 5 中。与之前方法调用中的参数 2 到 5 一样，参数 6 到 9 表示坐标和图像的可见大小。

### 15.2.3 格式化文本

`fillText()`和`strokeText()`方法可在绘图中创建填充或轮廓文本，你可以使用`textBaseline`属性来定义文本写入的基线（参见图 15.5 中的示例）。

![集成文本](img/img-f15.5.html)

**图 15.5**　集成文本

我们先来看文档的下半部分：

```html
...

<body>

   <canvas id="idCanvas" width="400" height="220"

           style="border:solid 1px #000000;"></canvas>

   <p><input id="idFilled" type="button" value="Text filled">

      <input id="idFramed" type="button" value="Text framed"></p>

   <script>
```

```javascript
 const c = document.getElementById("idCanvas");

      const ct = c.getContext("2d");

      ct.fillStyle = "#000000";

      ct.lineWidth = 1;

      ct.strokeStyle = "#000000";

      ct.font = "italic bold 50px Arial";

      document.getElementById("idFilled").addEventListener("click", filled);

      document.getElementById("idFramed").addEventListener("click", framed);
```

```html
 </script>

</body></html>
```

**清单 15.8**　canvas_text.htm 文件，下半部分

开头对线条和填充进行了一些默认设置，正如你在弧线中已经看到的那样。你可以使用`font`属性来定义字体属性。

现在，这是文档的上半部分：

```html
... <head> ...

   <script>
```

```javascript
 function filled()

      {

         ct.beginPath();

         ct.moveTo(0, 100);

         ct.lineTo(400, 100);

         ct.stroke();

         ct.textBaseline = "alphabetic";

         ct.fillText("Alp", 10, 100);

         ct.textBaseline = "top";

         ct.fillText("Top", 110, 100);

         ct.textBaseline = "middle";

         ct.fillText("Mid", 210, 100);

         ct.textBaseline = "bottom";

         ct.fillText("Bot", 310, 100);

      }

      function framed()

      {

         ct.textBaseline = "alphabetic";

         ct.strokeText("Framed", 10, 200);

      }
```

```html
 </script>

</head>

...
```

**清单 15.9**　canvas_text.htm 文件，上半部分

在`filled()`函数中，首先绘制一条基准线以明确文本基线。然后针对文本基线的不同距离使用不同的值，并分别生成一个文字。`fillText()`方法的第一个参数包含输出文本，接下来的两个参数包含第一个字符左下角的位置。

默认的`alphabetic`值会使大多数字符恰好位于线上。只有小写字母`g`、`j`、`p`、`q`和`y`会向下突出到线下方。使用`top`值时，线位于文字上方；使用`middle`时，线穿过文字中间；使用`bottom`时，线位于文字下方。

在`framed()`函数中，你使用`strokeText()`方法来创建轮廓文本。其参数与`fillText()`方法相同。

## 15.3 传感器

现代移动设备中的浏览器提供了访问设备传感器数据（用于地理定位、位置和加速度）的选项。确定的值可以使用 JavaScript 显示，并用于控制目的。

### 15.3.1 地理定位

你可以使用`navigator`对象的`geolocation`属性来访问地理定位数据，并可以将这些数据作为数值或在地图上使用。

在下面的`geolocation.htm`程序中，时间戳、纬度和经度分别以两种方式输出（参见图 15.6）。在调用请求你地理定位数据的程序后，程序会首先征求你的同意。

![地理定位数据](img/img-f15.6.html)

**图 15.6**　地理定位数据

> **注意**
>
> 你可能需要多次调用传感器程序，传感器才会响应并首次提供数据。

你可以将纬度和经度的十进制值输入到 Google 地图的搜索字段中，例如用空格分隔。然后地图上会显示该地理位置。

我们先来看程序的下半部分：

```html
...

<body>

   <div id="idInfo"> </div>

   <script>
```

```javascript
 const info = document.getElementById("idInfo");

      if(navigator.geolocation)

         navigator.geolocation.getCurrentPosition(receive, error);

      else

         error();
```

```html
 </script>

</body></html>
```

**清单 15.10**　geolocation.htm 文件，下半部分

你使用带有`idInfo` ID 的`div`区域来输出地理定位数据。`info`变量引用了这个`div`区域。

下一步是检查浏览器是否识别`geolocation`属性。在标准情况下，你还会被询问是否允许在运行期间检索地理定位数据。如果浏览器识别该属性并且你同意检索地理定位数据，则使用`getCurrentPosition()`方法请求地理定位数据。两个函数引用作为参数传递。

成功接收到的数据在`receive()`函数中输出。如果浏览器不认识该属性，或者你拒绝同意检索地理定位数据，则`error()`函数会抛出错误消息。

这是程序的上半部分：

```html
... <head> ...

   <script>
```

```javascript
 function receive(e)

      {

         const lat = e.coords.latitude;

         const latInteger = parseInt(lat);

         const latDecimalPlace = (lat - latInteger) * 60;

         const latMinutes = parseInt(latDecimalPlace);

         const latSeconds

            = (latDecimalPlace - parseInt(latDecimalPlace)) * 60;

         const lng = e.coords.longitude;

         const lngInteger = parseInt(lng);

         const lngDecimalPlace = (lng - lngInteger) * 60;

         const lngMinutes = parseInt(lngDecimalPlace);

         const lngSeconds

            = (lngDecimalPlace - parseInt(lngDecimalPlace)) * 60;

         const time = new Date(e.timestamp);

         info.innerHTML = "<p>Timestamp: " + e.timestamp + "<br>"

            + "Time: " + time.toUTCString() + "<br>"

            + "Latitude: " + lat.toFixed(4)

            + " = " + latInteger + "&deg; "

            + latMinutes + "&prime; "

            + latSeconds.toFixed(1) + "&Prime;<br>"

            + "Longitude: " + lng.toFixed(4)

            + " = " + lngInteger + "&deg; "

            + lngMinutes + "&prime; "

            + lngSeconds.toFixed(1) + "&Prime;</p>";

      }

      function error()

      {

         info.innerHTML = "No positioning";

      }
```

```html
 </script>

</head>

...
```



**清单 15.11**　`geolocation.htm` 文件，上半部分

一个包含地理定位数据的对象被传递给`receive()`函数。该对象包含`timestamp`和`coords`属性。`timestamp`可以转换为`Date`对象，而`coords`属性则包含表示纬度和经度的`latitude`和`longitude`属性。这些值输出时保留四位小数。

图 15.6 中的示例值中，纬度为正值，经度为负值。这表示北纬（赤道以北）和西经（英国格林尼治以西）。度数带有小数部分，这里将其转换为常见的表示形式：度、分、秒。纬度为 0 度时位于赤道，北极位于纬度 90 度，南极位于纬度 –90 度。经度为 0 度时也称为本初子午线，它穿过格林尼治，并且像所有经线一样穿过两极。经度为 180 度或 –180 度时，大致穿过新西兰等地，代表国际日期变更线。

下面以图 15.6 中的示例值 42.2757 度为例，说明如何转换为分和秒。小数部分（`dv`）的计算如下：辅助值`x = dv * 60`，`bm = x`的整数部分，`bs = (x 的小数部分) * 60`。当`dv = 0.2757`时：`x = dv * 60 = 16.542`，`bm = 16`，`bs = 0.542 * 60 = 32.52`，四舍五入保留一位小数得 32.5（即 42°16'32.5''）。反之，小数度数的十进制部分可计算如下：`(bm * 60 + bs) / 3600`。本例结果为`(16 * 60 + 32.52) / 3600 = 0.2757`。

### 15.3.2 路径追踪

你可以利用收集到的地理定位数据来确定步行、骑行或驾车所经路线的时间与地理轨迹。在本书的可下载资料中，你将找到`waytracking.htm`程序作为附加内容，其中包含大量解释性注释。

除了你在第 15.3.1 节中已经了解的数据外，你还可以使用`coords.altitude`子属性来记录海拔高度。该程序也考虑了移动设备可能无法记录该值的情况。

点击“开始”按钮后，每五秒记录一次地理定位数据，并将其作为新行添加到表格中。点击“停止”按钮后，记录和输出将结束。你可以在图 15.7 中看到表格的标题。

![路径追踪表格标题](img/img-f15.7.html)

**图 15.7** 路径追踪表格标题

特别是在低速、海拔变化小且检测频繁的情况下，测定的值可能与实际值略有偏差。经验表明，随着距离增加，偏差会趋于平均。

以下是表格列的描述：

- 纬度（度）：`coords.latitude`属性
- 经度（度）：`coords.longitude`属性
- 单段距离（米）：当前检测点与前一检测点之间的大圆距离（见下文）
- 总距离（米）：各段路径之和
- 时间（时、分、秒）：`timestamp`属性
- 单段时间（秒）：当前检测点与前一检测点的时间差
- 总时间（秒）：当前检测点与第一个检测点的时间差
- 单段速度（米/秒）：单段距离除以单段时间
- 总速度（米/秒）：总距离除以总时间
- 海拔（米）：`coords.altitude`属性
- 单段海拔差（米）：当前检测点与前一检测点的海拔差
- 总上升（米）：各段海拔差中正值（至少 1 米）的总和
- 总下降（米）：各段海拔差中负值（至少 1 米）的总和

大圆是球面上两点之间的最短路径。转换的源代码可在[`en.wikipedia.org/wiki/Great-circle_distance`](https://en.wikipedia.org/wiki/Great-circle_distance)找到。

单段时间的平均值约为五秒。各个值会有波动，尤其是在开始时，因为尝试记录数据与实际接收数据之间存在不同的时间差。

总速度在一段时间后会稳定在恒定速度附近。由于记录的不准确性，我决定在计算总上升和总下降时只考虑超过 1 米的海拔差。

### 注意

请确保在自动检测结束前，你的移动设备屏幕不会因你不再操作而关闭。否则可能导致无法继续记录数据。

### 15.3.3 位置传感器

你可以使用`DeviceOrientationEvent`对象来处理`deviceorientation`事件。这允许移动设备中的位置传感器检测并接收方向变化。位置传感器的工作原理示例如下：如果你旋转移动设备，屏幕会在竖屏和横屏模式之间切换。

然后你可以输出变化后的位置数据，也可以进一步处理这些数据。例如，你可以将其用于游戏和模拟。在下面的`orientation.htm`程序中，你可以看到一个简单的进一步处理，用于控制屏幕上的对象（参见图 15.8）。

位置信息包含三个值：`alpha`、`beta`和`gamma`角度。`alpha`角表示移动设备纵轴与北极之间的夹角（参见图 15.9）。该值范围在 0 到 360 度之间。

![位置数据、输出与控制](img/img-f15.8.html)

**图 15.8** 位置数据、输出与控制

![移动设备纵轴](img/img-f15.9.html)

**图 15.9** 移动设备纵轴

为了说明这些角度，最好先将移动设备平放在面前的桌子上。然后执行以下操作：

- 如果移动设备仍平放在桌子上，你转动它，`alpha`角会发生变化。在 0 度或 360 度时，移动设备的纵轴指向北极。
- 如果你将移动设备的上边缘向上抬起，直到它直立在你面前，你会注意到`beta`角从 0 度缓慢变化到 90 度。对移动设备的下边缘做同样的操作（即将其朝远离你的方向倾斜，直到完全倒置），`beta`角会从 0 度变化到 –90 度。总体而言，该角度的可能取值范围为 –180 度到 +180 度。
- 如果抬起左边缘并将移动设备向侧面倾斜，`gamma`角会从 0 度变为 90 度，而抬起右边缘则会使`gamma`角从 0 度变为 –90 度。同样，这里也可能出现从 –180 度到 +180 度的总值。

此外，在`orientation.htm`程序中，当设备倾斜时，深色方块会在浅色矩形内部移动。因此，位置数据的变化被用来移动一个对象。

让我们看看程序的下半部分：

```html
...

<body>

   <table>

      <tr><td>alpha</td><td><input id="idAlpha"

         style="text-align:right; width:100px;" readonly></td></tr>

      <tr><td>beta</td> <td><input id="idBeta"

         style="text-align:right; width:100px;" readonly></td></tr>

      <tr><td>gamma</td><td><input id="idGamma"

         style="text-align:right; width:100px;" readonly></td></tr>

   </table>

   <div style="position:absolute; top:300px; left:50px;

        width:800px; height:350px; background-color:#e0e0e0;"></div>

   <div id="idRect" style="position:absolute; top:300px; left:200px;

        width:200px; height:200px; background-color:#b0b0b0;"></div>

   <script>
```

```javascript
const rect = document.getElementById("idRect");

      if(DeviceOrientationEvent)

         addEventListener("deviceorientation", position, false);
```

```html
   </script>

</body></html>
```

**清单 15.12**　`orientation.htm`文件，下半部分

这里有一个包含三个只读输入字段的表格，用于输出位置数据，还有用于深色方块和浅色矩形的`div`区域，它们位于表格下方。

系统会检查浏览器是否识别`DeviceOrientationEvent`对象。如果识别，则会为`window`对象注册一个`deviceorientation`事件的事件监听器。因此，当位置发生变化时，会调用`position()`函数。

以下是程序的上半部分：

```html
... <head> ...

   <script>
```

```javascript
let moveReference, pTop = 300, pLeft = 200;

      function position(e)

      {

         clearTimeout(moveReference);

         document.getElementById("idAlpha").value = Math.round(e.alpha);

         document.getElementById("idBeta").value = Math.round(e.beta);

         document.getElementById("idGamma").value = Math.round(e.gamma);

         move(e.beta, e.gamma);

      }

      function move(b,g)

      {

         if(b > 3 && pTop < 450)       pTop += 5;

         else if(b < -3 && pTop > 300) pTop -= 5;

         rect.style.top = pTop + "px";

         if(g > 3 && pLeft < 650)      pLeft += 5;

         else if(g < -3 && pLeft > 50) pLeft -= 5;

         rect.style.left = pLeft + "px";

         moveReference = setTimeout(function() { move(b,g); }, 50);

      }
```

```html
   </script>

</head>

...
```

**清单 15.13**　`orientation.htm`文件，上半部分

要改变深色方块的位置，首先需要将位置的初始值存储在`pTop`和`pLeft`变量中。

此外，引入了一个变量作为时间控制过程的引用。这个引用有什么用呢？

`deviceorientation`事件仅在位置发生变化时触发，因此如果你倾斜移动设备然后保持倾斜状态，事件将不再发生。然而，深色方块应该继续按照物理规律移动。因此，每次位置变化时，都会启动一个时间控制过程，持续移动直到新的位置变化发生。只有新的位置变化才会以同样的方式被评估。

一个包含位置数据的对象被传递给`position()`函数，该对象包含`alpha`、`beta`和`gamma`属性。然后，当前移动的计时器被删除，调用`move()`函数，并将`beta`和`gamma`角度传递给`move()`函数。

`move()`函数检查设备是否在四个可能方向中的至少一个方向上倾斜了三度。这可以补偿手部的小抖动，并且你有机会通过将移动设备保持水平来停止深色方块的移动。其次，该函数检查深色方块是否已经到达浅色矩形的边缘。它不应该移动到边缘之外。

如果检查通过，深色方块会移动五个像素。然后，该函数在 50 毫秒后使用相同的位置数据再次调用自身，以便移动平滑地继续。如果在此期间移动设备被置于不同的位置，`position()`函数中的时间控制过程会终止，并启动新的位置变化。

### 15.3.4 加速度传感器

你可以使用`DeviceMotionEvent`对象，它处理`devicemotion`事件。这允许测量加速度（即速度的变化）。

你可以输出这些加速度数据并进一步处理（例如，用于游戏或模拟）。在下面的`motion.htm`程序中，屏幕上的一个对象被控制（参见图 15.10），但所需的移动设备动作与处理位置数据时不同。

![加速度数据、最大值和控制](img/img-f15.10.html)

**图 15.10**　加速度数据、最大值和控制

### 关于物理的说明

如果一个物体沿某个方向运动，它具有以米/秒为单位的速度。如果这个速度发生变化（例如，当车辆启动或刹车时），这被称为加速度，它对应于单位时间内速度的变化，并以米/秒²（我们写作 m/s²）为单位。

如果你以恒定速度沿某个方向移动你的移动设备，则不会产生加速度。传感器只测量加速度，并在移动设备停止或开始运动时触发`devicemotion`事件。

地球上所有物体都因重力而不断向地心加速。为简单起见，这种加速度也被称为重力加速度，其在地球表面的标准值约为 9.81 m/s² = 1 g。这解释了`z`的值。

在图 15.10 中，你可以看到`x`、`y`、`z`、`alpha`、`beta`和`gamma`的值。为了澄清这些值，最好先将你的移动设备平放在光滑表面的桌子上，然后执行以下操作：

- 在桌子上快速向右移动设备，然后减速直至停止。在过程开始时，会短暂测量到一个正的`x`值，而在结束时则短暂测量到一个负的`x`值。
- 在桌面上将设备快速远离自己，然后减速直至停止。过程开始时，会短暂测量到正的`y`值，结束时则短暂测量到负的`y`值。
- 拿起设备，快速向上举向天花板，然后减速直至停止。在序列开始时，由于施加的加速度与重力加速度叠加，会短暂测量到大于 9.81 的`z`值；结束时，会短暂测量到小于 9.81 的`z`值。

这些加速度用于改变浅色矩形中深色方块的位置和大小。

在`x`和`y`方向上，由于程序设定，方块表现出滞后的行为。当你在桌面上快速向右移动设备并减速直至停止时，方块最初会向左移动，因为它似乎无法快速跟上加速度；结束时，它会向右移动，因为它似乎无法快速减速。当你快速向上举起设备并减速直至停止时，方块在过程开始时变小，结束时又变大。

### 关于物理的补充说明

物体在某个方向上的速度和加速度也被称为轨道速度和轨道加速度，因为物体沿轨道运动。与之相对的是角速度和角加速度，分别以度每秒和度每平方秒为单位测量。

移动设备可以测量角加速度。为了明确这一参数，将设备平放在面前的桌子上。在设备仍平放时旋转它，会导致`gamma`角产生加速度；快速抬起设备的上边缘，会导致`alpha`角产生加速度；快速抬起设备的侧边缘，会导致`beta`角产生加速度。

这六种加速度都只持续很短的时间，因此程序中会永久显示它们的最大值。

以下是文档的下半部分：

```html
...

<body>

   <table>

      <tr>

         <td>x:</td><td><input id="idX"

            style="text-align:right; width:100px;" readonly></td>

         <td>xMax:</td><td><input id="idXMax"

            style="text-align:right; width:100px;" readonly></td>

         <td>&alpha;:</td><td><input id="idAlpha"

            style="text-align:right; width:100px;" readonly></td>

         <td>&alpha;Max:</td><td><input id="idAlphaMax"

            style="text-align:right; width:100px;" readonly></td>

      </tr>

      <tr>

         <td>y:</td> <td><input id="idY"

            style="text-align:right; width:100px;" readonly></td>

         <td>yMax:</td><td><input id="idYMax"

            style="text-align:right; width:100px;" readonly></td>

         <td>&beta;:</td> <td><input id="idBeta"

            style="text-align:right; width:100px;" readonly></td>

         <td>&beta;Max:</td> <td><input id="idBetaMax"

            style="text-align:right; width:100px;" readonly></td>

      </tr>

      <tr>

         <td>z:</td><td><input id="idZ"

            style="text-align:right; width:100px;" readonly></td>

         <td>zMax:</td><td><input id="idZMax"

            style="text-align:right; width:100px;" readonly></td>

         <td>&gamma;:</td><td><input id="idGamma"
```



```html
style="text-align:right; width:100px;" readonly></td>

<td>&gamma;Max:</td><td><input id="idGammaMax"

style="text-align:right; width:100px;" readonly></td>

</tr>

</table>

<div style="position:absolute; top:300px; left:50px;
     width:800px; height:350px; background-color:#e0e0e0;"></div>

<div id="idRect" style="position:absolute; top:300px; left:200px;
     width:200px; height:200px; background-color:#b0b0b0;"></div>

<script>
```

```javascript
const rect = document.getElementById("idRect");

if (DeviceMotionEvent)
  addEventListener("devicemotion", acceleration, false);
```

```html
</script>

</body></html>
```

**清单 15.14**　`motion.htm` 文件，下半部分

表格中共有十二个只读输入字段，用于输出六个测量值及其对应的六个最大值。随后是两个 `div` 区域，分别用于深色方块和浅色矩形。

系统会检查浏览器是否识别 `DeviceMotionEvent` 对象。如果识别，则为 `window` 对象注册一个 `devicemotion` 事件监听器。这意味着在加速过程中会调用 `acceleration()` 函数。

以下是程序的上半部分：

```html
... <head> ...

<script>
```

```javascript
let pTop = 300, pLeft = 200, size = 200;

let xMax = 0, yMax = 0, zMax = 9.81;

let alphaMax = 0, betaMax = 0, gammaMax = 0;

function acceleration(e)
{
  const acc = e.accelerationIncludingGravity;

  document.getElementById("idX").value = acc.x.toFixed(1);
  document.getElementById("idY").value = acc.y.toFixed(1);
  document.getElementById("idZ").value = acc.z.toFixed(1);

  if (Math.abs(acc.x) > xMax)
  {
    xMax = Math.abs(acc.x);
    document.getElementById("idXMax").value = xMax.toFixed(1);
  }

  if (Math.abs(acc.y) > yMax)
  {
    yMax = Math.abs(acc.y);
    document.getElementById("idYMax").value = yMax.toFixed(1);
  }

  if (Math.abs(acc.z) > zMax)
  {
    zMax = Math.abs(acc.z);
    document.getElementById("idZMax").value = zMax.toFixed(1);
  }

  if (acc.x > 3 && pLeft > 50)
    pLeft -= 50;

  if (acc.x < -3 && pLeft < 650)
    pLeft += 50;

  rect.style.left = pLeft + "px";

  if (acc.y < -3 && pTop > 300)
    pTop -= 50;

  if (acc.y > 3 && pTop < 450)
    pTop += 50;

  rect.style.top = pTop + "px";

  if (acc.z > 12.81 && size > 100)
    size -= 20;

  if (acc.z < 6.81 && size < 300)
    size += 20;

  rect.style.width = size + "px";
  rect.style.height = size + "px";

  if (e.rotationRate)
  {
    const rot = e.rotationRate;

    document.getElementById("idAlpha").value = Math.round(rot.alpha);
    document.getElementById("idBeta").value = Math.round(rot.beta);
    document.getElementById("idGamma").value = Math.round(rot.gamma);

    if (Math.abs(rot.alpha) > alphaMax)
    {
      alphaMax = Math.abs(rot.alpha);
      document.getElementById("idAlphaMax").value = Math.round(alphaMax);
    }

    if (Math.abs(rot.beta) > betaMax)
    {
      betaMax = Math.abs(rot.beta);
      document.getElementById("idBetaMax").value = Math.round(betaMax);
    }

    if (Math.abs(rot.gamma) > gammaMax)
    {
      gammaMax = Math.abs(rot.gamma);
      document.getElementById("idGammaMax").value = Math.round(gammaMax);
    }
  }
}
```

```html
</script>

</head>

...
```

**清单 15.15**　`motion.htm` 文件，上半部分

深色方块的位置和大小的初始值记录在 `pTop`、`pLeft` 和 `size` 变量中。此外，六个最大值被设置为 0，但有一个例外：`z` 的最大值被赋予起始值 9.81。

包含加速度数据的对象被传递给 `acceleration()` 函数，该对象除了其他属性外，还包含 `acceleration`、`accelerationIncludingGravity` 和 `rotationRate` 属性。其中前两个属性包含不同轨道加速度的 `x`、`y` 和 `z` 属性。区别在于，如果移动设备处于静止状态，`acceleration` 对象的 `z` 值为 0；否则，其值为 9.81。

然后，程序会检查某个加速度值是否偏离静止状态下的值至少 3 m/s²，同时检查深色方块是否已到达浅色矩形的边缘。方块不应移出边缘。

如果检查结果均为肯定，深色方块将移动 50 像素，或者变大或变小 20 像素。

在某些移动设备上，无法输出角加速度，因此需要事先查询相应的 `rotationRate` 对象。该对象在 `alpha`、`beta` 和 `gamma` 属性中包含三个不同的值。

对于所有六个加速度值，系统会检查当前值是否大于相应最大值的值。如果大于，则保存并输出新的最大值。

正确操作程序（即沿特定方向移动方块）并不容易，因此你应该缓慢启动移动并突然停止。只有在减速时才会出现超过 3 m/s² 的加速度，这会使效果更容易观察。

最后一条提示：测试加速度时请牢牢握住移动设备。

# A 安装与关键字

本附录介绍 XAMPP 的安装，然后提供 JavaScript 语言的关键字列表。关于 XAMPP 的使用，请参考第 4 章、第 4.2.2 节。

## A.1 安装 XAMPP 软件包

在本附录中，我将介绍免费 XAMPP 软件包的安装，你可以用它来测试 PHP 程序。目前可用的 XAMPP 版本（截至 2024 年 8 月）是 8.2.12 版。

### A.1.1 在 Windows 上安装

你可以从 [`www.apachefriends.org`](https://www.apachefriends.org) 下载适用于 Windows 的 XAMPP 软件包。

然后，通过调用可执行文件 `xampp-windows-x64-8.2.12-0-VS16-installer.exe` 开始安装。开始时可能会出现两个警告，提示正在运行防病毒程序等。你可以继续操作并确认建议的安装选项。我建议选择 `C:\xampp` 作为目标目录。

安装完成后，启动 XAMPP 控制面板应用程序，你可以通过 Apache 字样右侧的按钮启动和停止 Apache Web 服务器。

如果在启动服务器时收到 `Unable to open process` 错误消息，可能是由于端口已被占用。你可以在以下地址找到解决此问题的清晰说明：[`www.coder-welten.com/windows-10-unable-to-open-process`](http://www.coder-welten.com/windows-10-unable-to-open-process)。（请注意，这篇非常详细的文章是德文的。在现代浏览器中，你可以让它自动翻译。）

你可以通过 localhost 地址在浏览器中访问本地 Web 服务器的起始页，并将 HTML 文件和 PHP 程序保存在 `C:\xampp\htdocs` 目录及其子目录中。

以下 PHP 程序可用于检查安装是否成功。你可以使用编辑器编写并保存到 `C:\xampp\htdocs\phpinfo.php` 文件中：

```php
<?php

phpinfo();

?>
```

**清单 A.1**　`phpinfo.php` 文件

在浏览器中输入相应的 `localhost/phpinfo.php` 地址后，将显示已安装 PHP 版本的信息。

在 XAMPP 控制面板应用程序中停止 Apache Web 服务器，然后关闭该应用程序。

### A.1.2 在 Ubuntu Linux 上安装

你可以从 [`www.apachefriends.org/`](https://www.apachefriends.org/) 下载适用于 Linux 的 XAMPP 软件包。下载后，将获得 `xampp-linux-x64-8.2.12-0-installer.run` 文件。

打开终端输入安装命令，如有必要，使用以下命令更改文件的访问权限：

```bash
chmod 744 xampp-linux-x64-8.2.12-0-installer.run
```

通过以下命令开始安装：

```bash
sudo ./xampp-linux-x64-8.2.12-0-installer.run
```

你可以确认建议的安装选项，XAMPP 将安装在 `/opt/lampp` 目录中。

安装结束时，你可以保留“启动 Xampp”复选框的勾选状态。这将打开一个用于管理各个服务器的对话框。在“管理服务器”选项卡中，你可以选择 Apache Web 服务器，并使用右侧的按钮启动和停止它。你也可以直接通过以下方式调用管理服务器的对话框：

```bash
sudo /opt/lampp/manager-linux-x64.run
```

然而，Ubuntu Linux 的 Apache Web 服务器通常在系统启动后就已经运行。如果它正在运行，XAMPP 的 Apache Web 服务器将无法启动。如果发生这种情况，你必须先使用以下命令终止 Ubuntu Linux 的 Apache Web 服务器一次：

```bash
sudo /etc/init.d/apache2 stop
```

之后，你可以按照前面所述启动 XAMPP 的 Apache Web 服务器。

为了避免每次系统启动后都要关闭 Ubuntu Linux 的 Apache Web 服务器，你可以使用以下命令禁用相关服务的自动启动：

```bash
sudo update-rc.d apache2 disable
```

如果将来想重新启用相关服务的自动启动，可以通过以下命令进行：

```bash
sudo update-rc.d apache2 enable
```

你可以通过 localhost 地址在浏览器中访问本地 Web 服务器的起始页，然后将 HTML 文件和 PHP 程序保存在 `/opt/lampp/htdocs` 目录及其子目录中。

要测试安装是否成功，你可以使用下面的 PHP 程序。你可以使用 nano 编辑器编写并保存到 `phpinfo.php` 文件中，操作如下：

```bash
sudo nano /opt/lampp/htdocs/phpinfo.php
```

退出 nano 编辑器的方法如下：按 (Ctrl)+(X)，在底部“保存”处确认“是”，然后确认建议的文件名。PHP 程序如下所示：

```php
<?php

phpinfo();

?>
```

**清单 A.2**　`phpinfo.php` 文件

在浏览器中输入相应的 `localhost/phpinfo.php` 地址后，将显示已安装 PHP 版本的信息。

### A.1.3 在 macOS 上安装

你可以从 [`www.apachefriends.org`](https://www.apachefriends.org) 下载适用于 OS X 的 XAMPP 软件包。下载后，将获得 `xampp-osx-8.2.12-0-installer.dmg` 文件。双击此文件以创建一个新驱动器，然后你可以调用该新驱动器上的安装文件。

由于安装程序并非来自经过验证的 Apple 开发者，因此最初会被 macOS 阻止。在系统设置中调用“安全”菜单项，在那里你会找到“仍要打开”按钮，旁边有对 XAMPP 的引用。点击该按钮后，你将可以选择启动安装程序。

默认情况下，XAMPP 安装在 `/Applications/XAMPP` 目录中，这对应于 Finder 中的 `Applications/XAMPP` 目录。

安装结束时，你可以保留“启动 Xampp”复选框的勾选状态。这将打开一个用于管理各个服务器的对话框。在“管理服务器”选项卡中，你可以选择 Apache Web 服务器，并使用右侧的按钮启动和停止它。你也可以通过 `Applications/XAMPP/manager-osx` 调用管理各个服务器的对话框。

你可以在浏览器中通过 localhost 地址访问本地 Web 服务器的起始页，并将你的 HTML 文件和 PHP 程序保存在 `Applications/XAMPP/htdocs` 目录及其子目录中。

要测试安装是否成功，你可以使用以下 PHP 程序。你可以使用 App Store 中的 TextWrangler 编辑器编写并保存该程序到 `Applications/XAMPP/htdocs/phpinfo.php` 文件中。

PHP 程序如下所示：

```php
<?php

phpinfo();

?>
```



**列表 A.3**：`phpinfo.php` 文件

在浏览器中输入相应的`localhost/phpinfo.php`地址后，将显示已安装 PHP 版本的信息。

## A.2 关键字列表

在创建变量和自定义函数时，应尽量使用具有自解释性的自定义名称。命名应遵循一定规则（参见第 2 章，第 2.1.2 节），尤其不能使用以下 JavaScript 语言的关键字名称，因为它们已被或将被 JavaScript 自身使用：

`await`、`abstract`、`boolean`、`break`、`byte`、`case`、`catch`、`char`、`class`、`const`、`continue`、`debugger`、`default`、`delete`、`do`、`double`、`else`、`enum`、`export`、`extends`、`false`、`final`、`finally`、`float`、`for`、`function`、`get`、`goto`、`if`、`implements`、`import`、`in`、`instanceof`、`int`、`interface`、`let`、`long`、`native`、`new`、`null`、`package`、`protected`、`private`、`prototype`、`public`、`return`、`set`、`short`、`super`、`static`、`switch`、`synchronized`、`this`、`throw`、`throws`、`true`、`transient`、`try`、`typeof`、`undefined`、`var`、`void`、`volatile`、`while`、`with` 和 `yield`。

# B 作者

![](img/img-f_none_A_00.html)

Thomas Theis 拥有超过 40 年的软件开发者和 IT 讲师经验。他拥有计算机工程研究生学位。他曾在多所机构任教，包括亚琛应用技术大学。他是多本关于 Python、C#、PHP、C++ 和 Unity 的成功技术书籍的作者。

# 索引

↓**A**　↓**B**　↓**C**　↓**D**　↓**E**　↓**F**　↓**G**　↓**H**　↓**I**　↓**J**　↓**K**　↓**L**　↓**M**　↓**N**　↓**O**　↓**P**　↓**Q**　↓**R**　↓**S**　↓**T**　↓**U**　↓**V**　↓**W**　↓**X**　↓**Z**

`$`（美元符号）[[→ 第 1.7 节]](#01_007.html_i01_77)

`$_POST` [[→ 第 4.2 节]](#04_002.html_i04_43)

`$()`（jQuery）[[→ 第 11.1 节]](#11_001.html_i11_05)

`-`（减法）[[→ 第 2.2 节]](#02_002.html_i02_41)

`--`（递减）[[→ 第 2.2 节]](#02_002.html_i02_62)

`-=`（赋值）[[→ 第 2.2 节]](#02_002.html_i02_63)

`_`（分隔符）[[→ 第 2.1 节]](#02_001.html_i02_32)

`!`（逻辑非）[[→ 第 2.3 节]](#02_003.html_i02_119)

`!=`（不等于）[[→ 第 2.3 节]](#02_003.html_i02_100) [[→ 第 3.10 节]](#03_010.html_i03_68)

`!==`（不相等，含类型）[[→ 第 2.3 节]](#02_003.html_i02_135)

（换行符）[[→ 第 2.1 节]](#02_001.html_i02_21)

`[ ]`（对象成员）[[→ 第 3.10 节]](#03_010.html_i03_65)

`[ ]`（字符串）[[→ 第 6.2 节]](#06_002.html_i06_138)

`{ }`（花括号）[[→ 第 2.3 节]](#02_003.html_i02_91)

`@`（at 符号）[[→ 第 1.7 节]](#01_007.html_i01_79)

`*`（乘法）[[→ 第 2.2 节]](#02_002.html_i02_43)

`**`（乘方）[[→ 第 2.2 节]](#02_002.html_i02_50)

`*=`（赋值）[[→ 第 2.2 节]](#02_002.html_i02_64)

`/`（除法）[[→ 第 2.2 节]](#02_002.html_i02_45)

`/* */`（注释）[[→ 第 1.10 节]](#01_010.html_i01_107)

`//`（注释）[[→ 第 1.10 节]](#01_010.html_i01_109)

`/=`（赋值）[[→ 第 2.2 节]](#02_002.html_i02_65)

`&`（与符号）[[→ 第 1.7 节]](#01_007.html_i01_76)

`&&`（逻辑与）[[→ 第 2.3 节]](#02_003.html_i02_115)

`&&=`（逻辑与赋值）[[→ 第 2.3 节]](#02_003.html_i02_122)

`#`（井号）[[→ 第 3.3 节]](#03_003.html_i03_30)

`%`（取模）[[→ 第 2.2 节]](#02_002.html_i02_47)

`%=`（赋值）[[→ 第 2.2 节]](#02_002.html_i02_66)

`+`（加法）[[→ 第 2.1 节]](#02_001.html_i02_27)

`+`（歧义）[[→ 第 2.2 节]](#02_002.html_i02_72)

`+`（连接）[[→ 第 2.1 节]](#02_001.html_i02_07)

`++`（递增）[[→ 第 2.2 节]](#02_002.html_i02_61)

`+=`（赋值）[[→ 第 2.2 节]](#02_002.html_i02_60)

`<`（小于）[[→ 第 1.7 节]](#01_007.html_i01_89)

`<`（小于）[[→ 第 2.3 节]](#02_003.html_i02_95)

`<!--`（注释）[[→ 第 1.10 节]](#01_010.html_i01_105)

`<=`（小于等于）[[→ 第 2.3 节]](#02_003.html_i02_97)

`<?php ... ?>` [[→ 第 4.2 节]](#04_002.html_i04_42)

`==`（等于）[[→ 第 2.3 节]](#02_003.html_i02_98) [[→ 第 3.10 节]](#03_010.html_i03_67)

## 运算符与符号

- `===`（相等，带类型）[→ 第 2.3 节]
- `>`（大于）[→ 第 1.7 节]
- `>`（大于）[→ 第 2.3 节]
- `>=`（大于等于）[→ 第 2.3 节]
- `||`（逻辑或）[→ 第 2.3 节]
- `||=`（逻辑或并赋值）[→ 第 2.3 节]
- `.`（点运算符）[→ 第 1.8 节] [→ 第 3.1 节] [→ 第 3.10 节]
- `?` [→ 第 6.3 节]
- `?`（分支）[→ 第 2.3 节]
- `?.`（点运算符，可选）[→ 第 3.7 节]
- `??`（空值合并）[→ 第 3.7 节]
- `©`（版权）[→ 第 1.7 节]
- `®`（注册商标）[→ 第 1.7 节]
- `µ`（微）[→ 第 1.7 节]
- `¼`（四分之一）[→ 第 1.7 节]
- `½`（二分之一）[→ 第 1.7 节]
- `¾`（四分之）[→ 第 1.7 节]
- `…`（展开运算符）[→ 第 6.1 节]
- `‰`（千分之）[→ 第 1.7 节]
- `π`（圆周率）[→ 第 1.7 节]

## 图形与坐标

- 2D 图形 [→ 第 9.1 节]
- 3D 坐标系 [→ 第 10.1 节]
- 3D 图形 [→ 第 10.1 节]
- 3D 对象 [→ 第 10.1 节]
- 位置 [→ 第 10.1 节]

## A

- `a` [→ 第 1.6 节]
- `abs()` [→ 第 2.3 节] [→ 第 6.3 节]
- 绝对值 [→ 第 2.3 节] [→ 第 6.3 节]
- 加速度 [→ 第 15.3 节] [→ 第 15.3 节]
- 访问器 [→ 第 3.4 节]
- `action` [→ 第 4.2 节]
- `add()`
  - `Set` [→ 第 6.6 节]
  - `Three.js` [→ 第 10.1 节]
- `addColorStop()` [→ 第 15.2 节]
- `addEventListener()` [→ 第 4.1 节]
- 加法 [→ 第 2.1 节]
- Ajax [→ 第 7.1 节] [→ 第 11.6 节]
  - JSON 数组 [→ 第 7.4 节]
  - JSON 对象 [→ 第 7.4 节]
  - 参数 [→ 第 7.2 节]
  - XML 数据 [→ 第 7.3 节]
- `alert()` [→ 第 2.1 节]
- Onsen UI [→ 第 12.1 节]
- `alpha`
  - 加速度 [→ 第 15.3 节]
  - 位置 [→ 第 15.3 节]
  - 高度 [→ 第 15.3 节]
- 海平面高度 [→ 第 15.3 节]
- AND
  - 逻辑 [→ 第 2.3 节]
  - 短路 [→ 第 2.6 节]
- 角加速度 [→ 第 15.3 节]
- 动画 [→ 第 9.4 节]
- `animate()` [→ 第 11.3 节] [→ 第 11.4 节]
- 动画 [→ 第 9.4 节]
  - 创建 [→ 第 9.7 节]
  - `jQuery` [→ 第 11.3 节]
  - 序列 [→ 第 9.7 节]
  - SVG [→ 第 9.4 节]
  - `Three.js` [→ 第 10.3 节]
  - 时间控制 [→ 第 9.4 节]
- 匿名函数 [→ 第 2.6 节]
- `appendChild()` [→ 第 5.4 节]
  - SVG [→ 第 9.7 节]
- 弧 [→ 第 9.3 节] [→ 第 15.2 节]
- `arc()` [→ 第 15.2 节]
- `arguments` [→ 第 2.6 节]

## Array

- `Array` [→ 第 2.4 节] [→ 第 6.1 节]
  - 添加元素 [→ 第 6.1 节]
  - 作为参数 [→ 第 6.1 节]
  - 作为返回值 [→ 第 6.1 节]
  - 赋值 [→ 第 6.1 节]
  - `at()` [→ 第 6.1 节] [→ 第 6.1 节]
  - 回调 [→ 第 6.1 节]
  - 更改元素 [→ 第 6.1 节]
  - 检查 [→ 第 6.1 节]
  - `concat()` [→ 第 6.1 节]
  - 连接 [→ 第 6.1 节]
  - 包含值 [→ 第 6.1 节]
  - 转换 [→ 第 6.1 节]
  - 复制 [→ 第 6.1 节]
  - 复制元素 [→ 第 6.1 节]
  - `copyWithin()` [→ 第 6.1 节]
  - 创建 [→ 第 6.1 节] [→ 第 6.1 节]
  - 递归创建 [→ 第 6.1 节]
  - `delete` [→ 第 6.1 节]
  - 删除内容 [→ 第 6.1 节]
  - 元素 [→ 第 6.1 节] [→ 第 6.1 节]
  - `every()` [→ 第 6.1 节]
  - `fill()` [→ 第 6.1 节]
  - 填充 [→ 第 6.1 节]
  - `filter()` [→ 第 6.1 节]
  - `find()` [→ 第 6.1 节]
  - `findIndex()` [→ 第 6.1 节]
  - 查找元素 [→ 第 6.1 节]
  - `findLast()` [→ 第 6.1 节]
  - `findLastIndex()` [→ 第 6.1 节]
  - `flat()` [→ 第 6.1 节]
  - `forEach()` [→ 第 6.1 节]
  - `from()` [→ 第 6.1 节]
  - `includes()` [→ 第 6.1 节]
  - 索引 [→ 第 6.1 节]
  - `isArray()` [→ 第 6.1 节]
  - `join()` [→ 第 6.1 节] [→ 第 6.2 节]
  - JSON [→ 第 6.7 节]
  - `length` [→ 第 6.1 节] [→ 第 6.1 节]
  - `map()` [→ 第 6.1 节]
  - 多维 [→ 第 6.1 节]
  - 多维输出 [→ 第 6.1 节]
  - 对象 [→ 第 6.1 节]
  - 对象数组 [→ 第 6.1 节]
  - 输出 [→ 第 6.1 节]
  - `pop()` [→ 第 6.1 节]
  - `push()` [→ 第 6.1 节]
  - 元素 [→ 第 6.1 节]
  - `reverse()` [→ 第 6.1 节]
  - 反转 [→ 第 6.1 节]
  - `shift()` [→ 第 6.1 节]
  - `slice()` [→ 第 6.1 节]
  - `some()` [→ 第 6.1 节]
  - `sort()` [→ 第 6.1 节] [→ 第 6.1 节]
  - 字符排序 [→ 第 6.1 节]
  - 数字排序 [→ 第 6.1 节]
  - `splice()` [→ 第 6.1 节]
  - `toReversed()` [→ 第 6.1 节]
  - `toSorted()` [→ 第 6.1 节] [→ 第 6.1 节]
  - `toSpliced()` [→ 第 6.1 节]
  - `toString()` [→ 第 6.1 节]
  - `unshift()` [→ 第 6.1 节]
  - 带数据类型 [→ 第 6.3 节]
  - `with()` [→ 第 6.1 节]

## 杂项

- `aspect` [→ 第 10.1 节]
- 赋值 [→ 第 2.1 节]
  - 解构赋值 [→ 第 2.6 节] [→ 第 6.1 节]
- 关联数组映射 [→ 第 6.6 节]
- `async` [→ 第 13.1 节]
- `at()`
  - 数组 [→ 第 6.1 节] [→ 第 6.1 节]
  - 字符串 [→ 第 6.2 节]
- 属性节点 [→ 第 5.1 节] [→ 第 9.1 节]
- 音频 [→ 第 15.1 节]

## B

- 音频播放器 [[→ 第 15.1 节]](15_001.html_i15_02)
- `autofocus` [[→ 第 4.9 节]](04_009.html_i04_128)
- 背景颜色 [[→ 第 1.6 节]](01_006.html_i01_63) [[→ 第 1.6 节]](01_006.html_i01_64) [[→ 第 8.2 节]](08_002.html_i08_56) [[→ 第 8.2 节]](08_002.html_i08_61)
- MathML [[→ 第 13.1 节]](13_001.html_i13_15)
- 条形图 [[→ 第 4.9 节]](04_009.html_i04_159)
- 基 [[→ 第 2.2 节]](02_002.html_i02_55)
- 基类 [[→ 第 3.9 节]](03_009.html_i03_57)
  - `access` [[→ 第 3.9 节]](03_009.html_i03_61)
- `beginPath()` [[→ 第 15.2 节]](15_002.html_i15_29)
- 测试版
  - `acceleration` [[→ 第 15.3 节]](15_003.html_i15_78)
  - `position` [[→ 第 15.3 节]](15_003.html_i15_71)
- 贝塞尔曲线 [[→ 第 9.3 节]](09_003.html_i09_46)
- `BigInt` [[→ 第 6.3 节]](06_003.html_i06_261)
- `bind()` [[→ 第 11.3 节]](11_003.html_i11_29)
- 块
  - 语句 [[→ 第 2.3 节]](02_003.html_i02_90)
  - `static` [[→ 第 3.6 节]](03_006.html_i03_44)
  - 有效性 [[→ 第 2.6 节]](02_006.html_i02_236)
- `blur` [[→ 第 4.6 节]](04_006.html_i04_92)
- `body` [[→ 第 1.6 节]](01_006.html_i01_22)

### 额外内容

- 3D 形状 [[→ 第 10.4 节]](10_004.html_i10_48)
- `comma` [[→ 第 2.2 节]](02_002.html_i02_76)
- 专注 [[→ 第 14.5 节]](14_005.html_i14_05)
- 练习 [[→ 第 1.5 节]](01_005.html_i01_12)
- 健身值 [[→ 第 14.2 节]](14_002.html_i14_02)
- 趣味跑 [[→ 第 14.3 节]](14_003.html_i14_03)
- 投资 [[→ 第 14.1 节]](14_001.html_i14_01)
- Onsen UI [[→ 第 12.2 节]](12_002.html_i12_58)
- 正则表达式 [[→ 第 6.2 节]](06_002.html_i06_194)
- 示例项目 [[→ 第 6.7 节]](06_007.html_i06_401)
- 贪吃蛇 [[→ 第 14.6 节]](14_006.html_i14_06)
- 纸牌 [[→ 第 14.4 节]](14_004.html_i14_04)
- 投掷抛物线 [[→ 第 8.3 节]](08_003.html_i08_66)
- 路径追踪 [[→ 第 15.3 节]](15_003.html_i15_61)
- `Boolean` [[→ 第 2.1 节]](02_001.html_i02_36) [[→ 第 2.3 节]](02_003.html_i02_140)
- `BoxGeometry` [[→ 第 10.1 节]](10_001.html_i10_12)
- `br` [[→ 第 1.6 节]](01_006.html_i01_32)
- 分支 [[→ 第 2.3 节]](02_003.html_i02_86)
  - `if` [[→ 第 2.3 节]](02_003.html_i02_88)
  - 多个 [[→ 第 2.3 节]](02_003.html_i02_107)
  - 短形式 [[→ 第 2.3 节]](02_003.html_i02_105)
  - `switch` [[→ 第 2.3 节]](02_003.html_i02_144)
- `break`
  - 循环 [[→ 第 2.4 节]](02_004.html_i02_155)
  - `switch` [[→ 第 2.3 节]](02_003.html_i02_145)
- 断点 [[→ 第 2.5 节]](02_005.html_i02_198)
- 浏览器统计 [[→ 第 1.3 节]](01_003.html_i01_08)
- 浏览器窗口 [[→ 第 10.1 节]](10_001.html_i10_33)
- 按钮 [[→ 第 4.1 节]](04_001.html_i04_04) [[→ 第 4.1 节]](04_001.html_i04_07)
  - 点击 [[→ 第 4.1 节]](04_001.html_i04_20)

## C

- 计算 [[→ 第 2.2 节]](02_002.html_i02_39)
- 日历周 [[→ 第 4.9 节]](04_009.html_i04_180)
- 按引用调用 [[→ 第 2.6 节]](02_006.html_i02_214) [[→ 第 6.1 节]](06_001.html_i06_45)
- 按值调用 [[→ 第 2.6 节]](02_006.html_i02_213)
- 回调 [[→ 第 2.6 节]](02_006.html_i02_246)
  - 数组 [[→ 第 6.1 节]](06_001.html_i06_48)
  - jQuery [[→ 第 11.4 节]](11_004.html_i11_47)
- 驼峰命名 [[→ 第 2.1 节]](02_001.html_i02_14)
- 相机 [[→ 第 10.1 节]](10_001.html_i10_07) [[→ 第 10.1 节]](10_001.html_i10_17)
  - 移动 [[→ 第 10.2 节]](10_002.html_i10_43)
  - 视线方向 [[→ 第 10.1 节]](10_001.html_i10_28)
- `Capsule` [[→ 第 10.4 节]](10_004.html_i10_54)
- 层叠 [[→ 第 8.1 节]](08_001.html_i08_27)
- `catch` [[→ 第 2.5 节]](02_005.html_i02_185)
- `cbrt()` [[→ 第 6.3 节]](06_003.html_i06_221)
- `ceil` [[→ 第 6.3 节]](06_003.html_i06_200)
- 单元格 [[→ 第 1.6 节]](01_006.html_i01_47)
- 更改
  - 输入框 [[→ 第 4.6 节]](04_006.html_i04_81)
  - 滑块 [[→ 第 4.9 节]](04_009.html_i04_165)
- 更改文档 [[→ 第 4.8 节]](04_008.html_i04_116) [[→ 第 13.6 节]](13_006.html_i13_41)
- 字符串 [[→ 第 2.1 节]](02_001.html_i02_02)
- 复选框 [[→ 第 4.4 节]](04_004.html_i04_61)
  - 标记 [[→ 第 4.6 节]](04_006.html_i04_80)
  - Onsen UI [[→ 第 12.2 节]](12_002.html_i12_52)
  - `checked` [[→ 第 4.4 节]](04_004.html_i04_64)
- 检查密码 [[→ 第 6.2 节]](06_002.html_i06_192)
- 子节点 [[→ 第 5.1 节]](05_001.html_i05_03) [[→ 第 5.3 节]](05_003.html_i05_25) [[→ 第 9.1 节]](09_001.html_i09_07)
  - `childNodes` [[→ 第 5.3 节]](05_003.html_i05_28)
- 圆 [[→ 第 9.2 节]](09_002.html_i09_23) [[→ 第 9.2 节]](09_002.html_i09_25)
  - `canvas` [[→ 第 15.2 节]](15_002.html_i15_26)
  - SVG [[→ 第 9.2 节]](09_002.html_i09_26)
- 类 [[→ 第 3.1 节]](03_001.html_i03_04)
  - CSS [[→ 第 8.1 节]](08_001.html_i08_22)
  - 定义 [[→ 第 3.1 节]](03_001.html_i03_05)
  - 继承 [[→ 第 3.9 节]](03_009.html_i03_55)
  - 初始化 [[→ 第 3.6 节]](03_006.html_i03_46)
  - 实例 [[→ 第 3.10 节]](03_010.html_i03_70)
  - 成员 [[→ 第 3.2 节]](03_002.html_i03_22)
  - 方法 [[→ 第 3.2 节]](03_002.html_i03_20)
  - 操作 [[→ 第 3.10 节]](03_010.html_i03_62)
  - 属性 [[→ 第 3.1 节]](03_001.html_i03_07)
  - `class`（关键字）[[→ 第 3.1 节]](03_001.html_i03_08)
- 类选择器 [[→ 第 8.1 节]](08_001.html_i08_12)
  - jQuery [[→ 第 11.2 节]](11_002.html_i11_16)
- `clear()`
  - `Map` [[→ 第 6.6 节]](06_006.html_i06_389)
  - `Set` [[→ 第 6.6 节]](06_006.html_i06_365)
- `clearInterval()` [[→ 第 6.5 节]](06_005.html_i06_341)
- `clearTimeout()` [[→ 第 4.9 节]](04_009.html_i04_169)
- 点击
  - 事件 [[→ 第 4.1 节]](04_001.html_i04_18) [[→ 第 4.6 节]](04_006.html_i04_77)
  - 鼠标 [[→ 第 4.7 节]](04_007.html_i04_101)
- `click()` [[→ 第 11.1 节]](11_001.html_i11_03)
- `cloneNode()` [[→ 第 5.5 节]](05_005.html_i05_49)
- 码点 [[→ 第 6.2 节]](06_002.html_i06_151)
- 编解码器 [[→ 第 15.1 节]](15_001.html_i15_15)
- `codePointAt()` [[→ 第 6.2 节]](06_002.html_i06_153)
- 颜色
  - CSS [[→ 第 1.6 节]](01_006.html_i01_62) [[→ 第 8.2 节]](08_002.html_i08_58)
  - 输入框 [[→ 第 4.9 节]](04_009.html_i04_137) [[→ 第 4.9 节]](04_009.html_i04_138)
- `cols` [[→ 第 4.3 节]](04_003.html_i04_52)
- 注释 [[→ 第 1.10 节]](01_010.html_i01_104)
  - CSS [[→ 第 8.1 节]](08_001.html_i08_19)
  - HTML [[→ 第 1.10 节]](01_010.html_i01_106)
  - JavaScript [[→ 第 1.10 节]](01_010.html_i01_108)
- `concat()` [[→ 第 6.1 节]](06_001.html_i06_78)
- 条件 [[→ 第 2.3 节]](02_003.html_i02_89)
  - for 循环 [[→ 第 2.4 节]](02_004.html_i02_167)
  - 链接 [[→ 第 2.3 节]](02_003.html_i02_112)
- `Cone` [[→ 第 10.4 节]](10_004.html_i10_51)
- `confirm()` [[→ 第 2.3 节]](02_003.html_i02_109)
  - Onsen UI [[→ 第 12.2 节]](12_002.html_i12_31)
- `const` [[→ 第 2.1 节]](02_001.html_i02_10)
  - 有效性 [[→ 第 2.6 节]](02_006.html_i02_235)
- 常量 [[→ 第 2.1 节]](02_001.html_i02_01)
- 构造函数 [[→ 第 3.1 节]](03_001.html_i03_03) [[→ 第 3.1 节]](03_001.html_i03_10)
  - 基类 [[→ 第 3.9 节]](03_009.html_i03_59)
  - 方法 [[→ 第 3.1 节]](03_001.html_i03_09)
- 容器 [[→ 第 1.6 节]](01_006.html_i01_19)
- `continue` [[→ 第 2.4 节]](02_004.html_i02_154)
- `controls` [[→ 第 15.1 节]](15_001.html_i15_05)
- `coords` [[→ 第 15.3 节]](15_003.html_i15_58)
- 复制
  - 数组 [[→ 第 6.1 节]](06_001.html_i06_105)
  - 深拷贝 [[→ 第 3.11 节]](03_011.html_i03_88)
  - 扁平化 [[→ 第 3.11 节]](03_011.html_i03_87)
  - 对象 [[→ 第 3.11 节]](03_011.html_i03_86)
- `copyWithin()` [[→ 第 6.1 节]](06_001.html_i06_91)
- `cos()` [[→ 第 6.3 节]](06_003.html_i06_245)
- 余弦 [[→ 第 6.3 节]](06_003.html_i06_239)
- 倒计时 [[→ 第 6.5 节]](06_005.html_i06_343)
- `createElement()` [[→ 第 5.4 节]](05_004.html_i05_37)
- `createElementNS()` [[→ 第 9.7 节]](09_007.html_i09_73)
- `createLinearGradient()` [[→ 第 15.2 节]](15_002.html_i15_38)
- `createRadialGradient()` [[→ 第 15.2 节]](15_002.html_i15_40)
- `createTextNode()` [[→ 第 5.4 节]](05_004.html_i05_35)
- `crypto` [[→ 第 6.3 节]](06_003.html_i06_253)

`CSS` [[→ 第 1.6 节]](#01_006.html_i01_14) [[→ 第 8.1 节]](#08_001.html_i08_00)
`animating` [[→ 第 8.2 节]](#08_002.html_i08_32)
`assigning a class` [[→ 第 8.1 节]](#08_001.html_i08_24)
`background-color` [[→ 第 8.2 节]](#08_002.html_i08_57)
`cascading` [[→ 第 8.1 节]](#08_001.html_i08_28)
`change` [[→ 第 8.2 节]](#08_002.html_i08_31)
`changing using jQuery` [[→ 第 11.2 节]](#11_002.html_i11_09)
`class` [[→ 第 8.1 节]](#08_001.html_i08_23)
`class selectors` [[→ 第 8.1 节]](#08_001.html_i08_13)
`color` [[→ 第 8.2 节]](#08_002.html_i08_59)
`combination` [[→ 第 8.1 节]](#08_001.html_i08_26)
`comment` [[→ 第 8.1 节]](#08_001.html_i08_20)
`definition` [[→ 第 8.1 节]](#08_001.html_i08_03)
`embedded` [[→ 第 8.1 节]](#08_001.html_i08_06)
`external file` [[→ 第 8.1 节]](#08_001.html_i08_04)
`file` [[→ 第 1.6 节]](#01_006.html_i01_55)
`height` [[→ 第 8.2 节]](#08_002.html_i08_42)
`HTML selector` [[→ 第 8.1 节]](#08_001.html_i08_11)
`ID selector` [[→ 第 8.1 节]](#08_001.html_i08_15)
`including` [[→ 第 1.6 节]](#01_006.html_i01_29)
`inline` [[→ 第 8.1 节]](#08_001.html_i08_07)
`left` [[→ 第 8.2 节]](#08_002.html_i08_37)
`opacity` [[→ 第 8.2 节]](#08_002.html_i08_53)
`overlay` [[→ 第 8.1 节]](#08_001.html_i08_30)
`position` [[→ 第 8.2 节]](#08_002.html_i08_34)
`position (z)` [[→ 第 8.2 节]](#08_002.html_i08_47)
`selectors` [[→ 第 8.1 节]](#08_001.html_i08_09)
`size` [[→ 第 8.2 节]](#08_002.html_i08_44)
`top` [[→ 第 8.2 节]](#08_002.html_i08_36)
`transparency` [[→ 第 8.2 节]](#08_002.html_i08_51)
`visibility` [[→ 第 8.2 节]](#08_002.html_i08_55)
`width` [[→ 第 8.2 节]](#08_002.html_i08_40)
`z-index` [[→ 第 8.2 节]](#08_002.html_i08_46)
`css()` [[→ 第 11.2 节]](#11_002.html_i11_08)
`Cuboid` [[→ 第 10.1 节]](#10_001.html_i10_11) [[→ 第 10.4 节]](#10_004.html_i10_50)
`Current object` [[→ 第 3.1 节]](#03_001.html_i03_14)
`currentTime` [[→ 第 15.1 节]](#15_001.html_i15_08)

## D

- `deviceorientation` [[→ 第 15.3 节]](#15_003.html_i15_66)
- `focus` [[→ 第 4.6 节]](#04_006.html_i04_89)
- `handler` [[→ 第 4.1 节]](#04_001.html_i04_02)
- 在表单中 [[→ 第 4.6 节]](#04_006.html_i04_76)
- `jQuery` [[→ 第 11.3 节]](#11_003.html_i11_20)
- `keydown` [[→ 第 7.3 节]](#07_003.html_i07_33)
- `keyup` [[→ 第 4.6 节]](#04_006.html_i04_86)
- `listener` [[→ 第 4.1 节]](#04_001.html_i04_14)
- `motion` [[→ 第 15.3 节]](#15_003.html_i15_74)
- `mousedown` [[→ 第 4.7 节]](#04_007.html_i04_105)
- `mousemove` [[→ 第 4.7 节]](#04_007.html_i04_103)
- `mouseout` [[→ 第 4.7 节]](#04_007.html_i04_111)
- `mouseover` [[→ 第 4.7 节]](#04_007.html_i04_109)
- `mouseup` [[→ 第 4.7 节]](#04_007.html_i04_107)
- `object` [[→ 第 4.6 节]](#04_006.html_i04_98)
- `offsetX` [[→ 第 4.7 节]](#04_007.html_i04_114)
- `reset` [[→ 第 4.2 节]](#04_002.html_i04_40)
- `submit` [[→ 第 4.2 节]](#04_002.html_i04_38)
- `target` [[→ 第 4.6 节]](#04_006.html_i04_97)
- `event.preventDefault()` [[→ 第 4.3 节]](#04_003.html_i04_59)

## E

- `every()` [[→ 第 6.1 节]](#06_001.html_i06_54)
- 异常处理 [[→ 第 2.5 节]](#02_005.html_i02_183)
- `exp()` [[→ 第 6.3 节]](#06_003.html_i06_227)
- 指数 [[→ 第 2.2 节]](#02_002.html_i02_56) [[→ 第 13.1 节]](#13_001.html_i13_12)
- 指数格式 [[→ 第 2.1 节]](#02_001.html_i02_29)
- 指数函数 [[→ 第 6.3 节]](#06_003.html_i06_228)
- 幂运算 [[→ 第 2.2 节]](#02_002.html_i02_51) [[→ 第 2.2 节]](#02_002.html_i02_54)
- 外部
  - CSS 文件 [[→ 第 1.6 节]](#01_006.html_i01_28) [[→ 第 8.1 节]](#08_001.html_i08_05)
  - `JavaScript` [[→ 第 1.9 节]](#01_009.html_i01_99) [[→ 第 2.6 节]](#02_006.html_i02_208)

## F

F ⇑

- `fadeIn()` [[→ 第 11.4 节]](#11_004.html_i11_53)
- `fadeOut()` [[→ 第 11.4 节]](#11_004.html_i11_54)
- `fadeTo()` [[→ 第 11.4 节]](#11_004.html_i11_56)
- `fadeToggle()` [[→ 第 11.4 节]](#11_004.html_i11_55)
- `false` [[→ 第 2.1 节]](#02_001.html_i02_38)
- `far` [[→ 第 10.1 节]](#10_001.html_i10_22)
- 字段 [[→ 第 2.4 节]](#02_004.html_i02_160)
  - `length` [[→ 第 4.5 节]](#04_005.html_i04_75)
  - 简单 [[→ 第 2.4 节]](#02_004.html_i02_161)
  - 二维 [[→ 第 2.4 节]](#02_004.html_i02_164)
- 填充颜色 [[→ 第 9.2 节]](#09_002.html_i09_18)
- `fill()`
  - 数组 [[→ 第 6.1 节]](#06_001.html_i06_31)
  - 路径 [[→ 第 15.2 节]](#15_002.html_i15_31)
- 填充级别 [[→ 第 4.9 节]](#04_009.html_i04_158)
- `fillRect()` [[→ 第 15.2 节]](#15_002.html_i15_23)
- `fillStyle` [[→ 第 15.2 节]](#15_002.html_i15_20)
- `fillText()` [[→ 第 15.2 节]](#15_002.html_i15_44)
- `filter()` [[→ 第 6.1 节]](#06_001.html_i06_57)
- `finally` [[→ 第 2.5 节]](#02_005.html_i02_187)
- `find()` [[→ 第 6.1 节]](#06_001.html_i06_111)
- `findIndex()` [[→ 第 6.1 节]](#06_001.html_i06_113)
- `findLast()` [[→ 第 6.1 节]](#06_001.html_i06_116)
- `findLastIndex()` [[→ 第 6.1 节]](#06_001.html_i06_118)
- `firstChild` [[→ 第 5.2 节]](#05_002.html_i05_20) [[→ 第 7.3 节]](#07_003.html_i07_28)
- `flat()` [[→ 第 6.1 节]](#06_001.html_i06_38)
- `Float32Array` [[→ 第 6.3 节]](#06_003.html_i06_279)
- `Float64Array` [[→ 第 6.3 节]](#06_003.html_i06_280)
- `floor()` [[→ 第 2.4 节]](#02_004.html_i02_171) [[→ 第 6.3 节]](#06_003.html_i06_203)
- 焦点 [[→ 第 4.6 节]](#04_006.html_i04_88) [[→ 第 4.6 节]](#04_006.html_i04_91) [[→ 第 4.9 节]](#04_009.html_i04_129)
- 字体 [[→ 第 1.6 节]](#01_006.html_i01_56)
  - `font` [[→ 第 15.2 节]](#15_002.html_i15_48)
  - `CSS` [[→ 第 1.6 节]](#01_006.html_i01_57)
  - 字体颜色 [[→ 第 1.6 节]](#01_006.html_i01_61)
  - `MathML` [[→ 第 13.1 节]](#13_001.html_i13_16)
  - 字体大小 [[→ 第 1.6 节]](#01_006.html_i01_59) [[→ 第 1.6 节]](#01_006.html_i01_60)
  - `MathML` [[→ 第 13.1 节]](#13_001.html_i13_17)
  - `font-family` [[→ 第 1.6 节]](#01_006.html_i01_58)
- `for`
  - 标签 [[→ 第 12.2 节]](#12_002.html_i12_43)
  - 循环 [[→ 第 2.4 节]](#02_004.html_i02_148)
- `forEach()`
  - 数组 [[→ 第 6.1 节]](#06_001.html_i06_50)
  - `Map` [[→ 第 6.6 节]](#06_006.html_i06_372)
  - `Set` [[→ 第 6.6 节]](#06_006.html_i06_351)
- 表单 [[→ 第 4.1 节]](#04_001.html_i04_00) [[→ 第 4.1 节]](#04_001.html_i04_05)
  - 动态创建 [[→ 第 4.10 节]](#04_010.html_i04_202)
  - 必填字段 [[→ 第 4.3 节]](#04_003.html_i04_47)
  - 可操作性 [[→ 第 4.9 节]](#04_009.html_i04_194)
  - 重置 [[→ 第 4.2 节]](#04_002.html_i04_25)
  - 提交 [[→ 第 4.2 节]](#04_002.html_i04_23)
  - `target` [[→ 第 4.2 节]](#04_002.html_i04_36)
  - 验证 [[→ 第 4.3 节]](#04_003.html_i04_45) [[→ 第 4.9 节]](#04_009.html_i04_121) [[→ 第 4.9 节]](#04_009.html_i04_191)
- `format()` [[→ 第 6.3 节]](#06_003.html_i06_283)
- 格式化模板 [[→ 第 8.1 节]](#08_001.html_i08_01)
- `for-of` [[→ 第 6.1 节]](#06_001.html_i06_14)
- `fov` [[→ 第 10.1 节]](#10_001.html_i10_19)
- 分数 [[→ 第 13.4 节]](#13_004.html_i13_36)
- 框架（SVG）[[→ 第 9.2 节]](#09_002.html_i09_20)
- `from()` 数组 [[→ 第 6.1 节]](#06_001.html_i06_22)
- `fromCodePoint()` [[→ 第 6.2 节]](#06_002.html_i06_148)
  - 字符串 [[→ 第 6.2 节]](#06_002.html_i06_155)
- 函数 [[→ 第 2.6 节]](#02_006.html_i02_202)
  - 匿名 [[→ 第 2.6 节]](#02_006.html_i02_243)
  - 自动调用 [[→ 第 6.5 节]](#06_005.html_i06_340)
  - 调用 [[→ 第 2.6 节]](#02_006.html_i02_206)
  - 回调 [[→ 第 2.6 节]](#02_006.html_i02_247)
  - 库 [[→ 第 2.6 节]](#02_006.html_i02_209)
  - 命名 [[→ 第 2.6 节]](#02_006.html_i02_241)
  - 参数 [[→ 第 2.6 节]](#02_006.html_i02_211)
  - 递归 [[→ 第 2.6 节]](#02_006.html_i02_239)
  - 引用 [[→ 第 2.6 节]](#02_006.html_i02_245)
  - 返回值 [[→ 第 2.6 节]](#02_006.html_i02_218)
  - 替换 [[→ 第 2.6 节]](#02_006.html_i02_207)
  - 类型 [[→ 第 3.10 节]](#03_010.html_i03_76)
- `function`（关键字）[[→ 第 2.6 节]](#02_006.html_i02_205)

## G

- `g`（SVG）[[→ 第 9.3 节]](#09_003.html_i09_42)
- gamma
  - 加速度 [[→ 第 15.3 节]](#15_003.html_i15_76)
  - 位置 [[→ 第 15.3 节]](#15_003.html_i15_72)
- 地理定位 [[→ 第 15.3 节]](#15_003.html_i15_51)
- 地理定位数据 [[→ 第 15.3 节]](#15_003.html_i15_53)
- `get` [[→ 第 3.4 节]](#03_004.html_i03_38)
- GET 方法 [[→ 第 7.1 节]](#07_001.html_i07_18)
- `get()` [[→ 第 6.6 节]](#06_006.html_i06_376)
- `getAttribute()` [[→ 第 5.2 节]](05_002.html_i05_17) [[→ 第 7.3 节]](07_003.html_i07_30)
  - `SVG` [[→ 第 9.6 节]](09_006.html_i09_68)
- `getContext()` [[→ 第 15.2 节]](15_002.html_i15_002.html_i15_19)
- `getCurrentPosition()` [[→ 第 15.3 节]](15_003.html_i15_56)
- `getDate()` [[→ 第 6.4 节]](06_004.html_i06_313)
- `getDay()` [[→ 第 6.4 节]](06_004.html_i06_310)
- `getElementById()` [[→ 第 4.1 节]](04_001.html_i04_11)
  - `SVG` [[→ 第 9.6 节]](09_006.html_i09_67)
- `getElementsByTagName()` [[→ 第 5.2 节]](05_002.html_i05_13) [[→ 第 7.3 节]](07_003.html_i07_26)
- `getFullYear()` [[→ 第 6.4 节]](06_004.html_i06_004.html_i06_317)
- `getHours()` [[→ 第 4.9 节]](04_009.html_i04_187) [[→ 第 6.4 节]](06_004.html_i06_319)
- `getMilliseconds()` [[→ 第 6.4 节]](06_004.html_i06_325)
- `getMinutes()` [[→ 第 6.4 节]](06_004.html_i06_321)
- `getMonth()` [[→ 第 6.4 节]](06_004.html_i06_315)
- `getRandomValues()` [[→ 第 6.3 节]](06_003.html_i06_254)
- `getSeconds()` [[→ 第 6.4 节]](06_004.html_i06_323)
- 获取器 [[→ 第 3.4 节]](03_004.html_i03_34)
- `getTimezoneOffset()` [[→ 第 6.4 节]](06_004.html_i06_299)
- 谷歌浏览器 [[→ 第 1.3 节]](01_003.html_i01_09)
  - 调试 [[→ 第 2.5 节]](02_005.html_i02_196)
  - `DOM` [[→ 第 5.1 节]](05_001.html_i05_11)
  - `JavaScript` 关闭 [[→ 第 1.11 节]](01_011.html_i01_112)
- 渐变 [[→ 第 15.2 节]](15_002.html_i15_37)
- 图形
  - 二维 [[→ 第 9.1 节]](09_001.html_i09_02)
  - 三维 [[→ 第 10.1 节]](10_001.html_i10_03)
- 格林威治时间（GMT）[[→ 第 6.4 节]](06_004.html_i06_290)

## H

- `has()`
  - `Map` [[→ 第 6.6 节]](06_006.html_i06_374)
  - `Set` [[→ 第 6.6 节]](06_006.html_i06_353)
- `hasChildNodes()` [[→ 第 5.3 节]](05_003.html_i05_26)
- 哈希字符 [[→ 第 3.3 节]](03_003.html_i03_29)
- `head` [[→ 第 1.6 节]](01_006.html_i01_21)
- `height` [[→ 第 8.2 节]](08_002.html_i08_41)

# 索引参考

十六进制数 [[→ 章节 2.2]](#02_002.html_i02_85)

隐藏 [[→ 章节 4.9]](#04_009.html_i04_130)

`hide()` [[→ 章节 11.4]](#11_004.html_i11_58)

高亮 [[→ 章节 4.9]](#04_009.html_i04_124)

`hover()` [[→ 章节 11.3]](#11_003.html_i11_27)

## href

`href`

`a` [[→ 章节 1.6]](#01_006.html_i01_37)

链接 [[→ 章节 1.6]](#01_006.html_i01_27) [[→ 章节 8.1]](#08_001.html_i08_17)

位置 [[→ 章节 4.8]](#04_008.html_i04_119)

HTML [[→ 章节 1.6]](#01_006.html_i01_13) [[→ 章节 1.6]](#01_006.html_i01_20)

使用 jQuery 更改 [[→ 章节 11.2]](#11_002.html_i11_12)

`document` [[→ 章节 1.6]](#01_006.html_i01_17)

元素节点 [[→ 章节 5.5]](#05_005.html_i05_57)

文件 [[→ 章节 1.6]](#01_006.html_i01_15)

选择器 [[→ 章节 8.1]](#08_001.html_i08_10)

`html()` [[→ 章节 11.2]](#11_002.html_i11_11)

`htmlentities()` [[→ 章节 4.2]](#04_002.html_i04_44)

HTTP [[→ 章节 7.1]](#07_001.html_i07_12)

HTTPS [[→ 章节 7.1]](#07_001.html_i07_15)

超链接 [[→ 章节 1.6]](#01_006.html_i01_35)

上 ↑

## I

ID [[→ 章节 4.1]](#04_001.html_i04_10)

ID 选择器 [[→ 章节 8.1]](#08_001.html_i08_14)

`jQuery` [[→ 章节 11.2]](#11_002.html_i11_18)

`if` [[→ 章节 2.3]](#02_003.html_i02_87)

图片 [[→ 章节 1.6]](#01_006.html_i01_38) [[→ 章节 15.2]](#15_002.html_i15_41)

动画和更改 [[→ 章节 8.3]](#08_003.html_i08_63)

`canvas` [[→ 章节 15.2]](#15_002.html_i15_43)

更改 [[→ 章节 4.7]](#04_007.html_i04_112)

`img` [[→ 章节 1.6]](#01_006.html_i01_39)

在……中 [[→ 章节 3.10]](#03_010.html_i03_78)

`includes()`

- `array` [[→ 章节 6.1]](#06_001.html_i06_19)
- `string` [[→ 章节 6.2]](#06_002.html_i06_129)

缩进 [[→ 章节 2.3]](#02_003.html_i02_108)

索引 [[→ 章节 2.4]](#02_004.html_i02_163)

`array` [[→ 章节 6.1]](#06_001.html_i06_04)

`string` [[→ 章节 6.2]](#06_002.html_i06_128)

`indexOf()` [[→ 章节 6.2]](#06_002.html_i06_158)

继承 [[→ 章节 3.9]](#03_009.html_i03_54)

`innerHeight` [[→ 章节 10.1]](#10_001.html_i10_36)

`innerHTML` [[→ 章节 5.5]](#05_005.html_i05_55)

`innerWidth` [[→ 章节 10.1]](#10_001.html_i10_34)

`Input` [[→ 章节 4.1]](#04_001.html_i04_06)

`confirmation` [[→ 章节 2.3]](#02_003.html_i02_11)

`dialog box` [[→ 章节 2.1]](#02_001.html_i02_17)

`focus` [[→ 章节 4.6]](#04_006.html_i04_90)

`number` [[→ 章节 2.2]](#02_002.html_i02_70)

`Input field` [[→ 章节 4.1]](#04_001.html_i04_03)

`color` [[→ 章节 4.9]](#04_009.html_i04_13)

`content changed` [[→ 章节 4.6]](#04_006.html_i04_83)

`email` [[→ 章节 4.9]](#04_009.html_i04_140)

`multiline` [[→ 章节 4.3]](#04_003.html_i04_49)

`number` [[→ 章节 4.9]](#04_009.html_i04_149)

`Onsen UI` [[→ 章节 12.2]](#12_002.html_i12_39)

`phone` [[→ 章节 4.9]](#04_009.html_i04_145)

`placeholder` [[→ 章节 4.9]](#04_009.html_i04_126)

`time` [[→ 章节 4.9]](#04_009.html_i04_171)

`types` [[→ 章节 4.9]](#04_009.html_i04_122)

`URL` [[→ 章节 4.9]](#04_009.html_i04_143)

`insertBefore()` [[→ 章节 5.4]](#05_004.html_i05_45)

`Instance` [[→ 章节 3.10]](#03_010.html_i03_69)

`instanceof` [[→ 章节 3.10]](#03_010.html_i03_71)

`Int32Array` [[→ 章节 6.3]](#06_003.html_i06_258)

`Integral symbol` [[→ 章节 13.3]](#13_003.html_i13_32)

`Internet server` [[→ 章节 4.2]](#04_002.html_i04_30)

`Interpreters` [[→ 章节 1.1]](#01_001.html_i01_02)

`isArray()` [[→ 章节 6.1]](#06_001.html_i06_27)

`isNaN()` [[→ 章节 2.3]](#02_003.html_i02_124)

`isSafeInteger()` [[→ 章节 6.3]](#06_003.html_i06_265)

`isWellFormed()` [[→ 章节 6.2]](#06_002.html_i06_196)

`Iterator` [[→ 章节 6.6]](#06_006.html_i06_358) [[→ 章节 6.6]](#06_006.html_i06_380)

`next()` [[→ 章节 6.6]](#06_006.html_i06_360)

## J

`JavaScript` [[→ 章节 1.1]](#01_001.html_i01_00) [[→ 章节 1.8]](#01_008.html_i01_90)

`embedding` [[→ 章节 1.8]](#01_008.html_i01_91)

`external` [[→ 章节 1.9]](#01_009.html_i01_100)

`keywords` [[→ 章节 A.2]](#A_002.html_i16_06)

`statement` [[→ 章节 1.8]](#01_008.html_i01_93)

`switching off` [[→ 章节 11.1]](#01_011.html_i01_111)

`switching on` [[→ 章节 1.2]](#01_002.html_i01_07)

`JavaScript Object Notation (JSON)` [[→ 章节 6.7]](#06_007.html_i06_391) [[→ 章节 7.4]](#07_004.html_i07_35)

`format` [[→ 章节 6.7]](#06_007.html_i06_394)

`object` [[→ 章节 6.7]](#06_007.html_i06_395)

`parse()` [[→ 章节 6.7]](#06_007.html_i06_399)

`stringify()` [[→ 章节 6.7]](#06_007.html_i06_397)

`join()` [[→ 章节 6.1]](#06_001.html_i06_87) [[→ 章节 6.2]](#06_002.html_i06_46)

`jQuery` [[→ 章节 11.1]](#01_001.html_i11_00)

`()` [[→ 章节 11.1]](#01_001.html_i11_06)

`animate()` [[→ 章节 11.3]](#01_003.html_i11_23) [[→ 章节 11.4]](#01_004.html_i11_40)

`bind()` [[→ 章节 11.3]](#01_003.html_i11_30)

`class selector` [[→ 章节 11.2]](#01_002.html_i11_17)

`click()` [[→ 章节 11.1]](#01_001.html_i11_04)

`css()` [[→ 章节 11.2]](#01_002.html_i11_07)

`dblclick()` [[→ 章节 11.3]](#01_003.html_i11_26)

`event` [[→ 章节 11.3]](#01_003.html_i11_21)

`hover()` [[→ 章节 11.3]](#01_003.html_i11_28)

`html()` [[→ 章节 11.2]](#01_002.html_i11_10)

`ID selector` [[→ 章节 11.2]](#01_002.html_i11_19)

`loading a file` [[→ 章节 11.6]](#01_006.html_i11_63)

`pageX` [[→ 章节 11.3]](#01_003.html_i11_33)

`pageY` [[→ 章节 11.3]](#01_003.html_i11_35)

`position` [[→ 章节 11.4]](#01_004.html_i11_44)

`ready()` [[→ 章节 11.1]](#01_001.html_i11_02)

`size` [[→ 章节 11.4]](#01_004.html_i11_42)

`text()` [[→ 章节 11.2]](#01_002.html_i11_13)

`timeStamp` [[→ 章节 11.3]](#01_003.html_i11_37)

`type` [[→ 章节 11.3]](#01_003.html_i11_31)

`js (ending)` [[→ 章节 1.9]](#01_009.html_i01_103)

## K

`pressing` [[→ 章节 7.3]](#07_003.html_i07_34)

`releasing` [[→ 章节 4.6]](#04_006.html_i04_87)

`keydown` [[→ 章节 7.3]](#07_003.html_i07_32)

`keys()` [[→ 章节 6.6]](#06_006.html_i06_381)

`keyup` [[→ 章节 4.6]](#04_006.html_i04_85)

`Key-value pair` [[→ 章节 6.6]](#06_006.html_i06_369)

`Keywords` [[→ 章节 2.1]](#02_001.html_i02_13) [[→ 章节 A.2]](#A_002.html_i16_05)

## L

`label` [[→ 章节 12.2]](#12_002.html_i12_44)

`Landscape format` [[→ 章节 15.3]](#15_003.html_i15_69)

`Landscape mode` [[→ 章节 1.6]](#01_006.html_i01_71)

`lastIndexOf()` [[→ 章节 6.2]](#06_002.html_i06_16)

`Latitude` [[→ 章节 15.3]](#15_003.html_i15_54)

`left` [[→ 章节 8.1]](#08_001.html_i08_38)

`length` [[→ 章节 8.1]](#08_001.html_i08_29)

`arguments` [[→ 章节 6.1]](#06_001.html_i06_16)

`array` [[→ 章节 6.1]](#06_001.html_i06_11)

`field` [[→ 章节 4.1]](#04_001.html_i04_05)

`string` [[→ 章节 4.3]](#04_003.html_i04_15)

`string` [[→ 章节 6.2]](#06_002.html_i06_30)

`let` [[→ 章节 2.1]](#02_001.html_i02_05)

`validity` [[→ 章节 4.6]](#04_006.html_i04_23)

`li` [[→ 章节 1.6]](#01_006.html_i01_43)

`Line` [[→ 章节 9.2]](#09_002.html_i09_28)

`dialog break` [[→ 章节 2.1]](#02_001.html_i02_22)

`document` [[→ 章节 1.6]](#01_006.html_i01_31)

`lineTo` [[→ 章节 15.2]](#15_002.html_i15_35)

`lineWidth` [[→ 章节 15.2]](#15_002.html_i15_21)

`link` [[→ 章节 1.6]](#01_006.html_i01_25)

`Linux` [[→ 附录 A.1]](#A_001.html_i16_03)

`List` [[→ 章节 1.6]](#01_006.html_i01_41) [[→ 章节 4.9]](#04_009.html_i04_133)

`load()`

`Loop` [[→ 第 2.4 节]](#02_004.html_i02_147) [[→ 第 15.1 节]](#15_001.html_i15_09)

`continue` [[→ 第 2.4 节]](#02_004.html_i02_156)

`do while` [[→ 第 2.4 节]](#02_004.html_i02_168)

`endless`（死循环）[[→ 第 2.4 节]](#02_004.html_i02_150)

`for` [[→ 第 2.4 节]](#02_004.html_i02_149)

`for-of` [[→ 第 6.1 节]](#06_001.html_i06_15)

`nested`（嵌套）[[→ 第 2.4 节]](#02_004.html_i02_159)

`terminating`（终止）[[→ 第 2.4 节]](#02_004.html_i02_157)

`while` [[→ 第 2.4 节]](#02_004.html_i02_165)

## M

macOS [[→ 附录 A.1]](#A_001.html_i16_04)

Mandatory field（必填字段）[[→ 第 4.3 节]](#04_003.html_i04_46)

changing（更改）[[→ 第 4.9 节]](#04_009.html_i04_161)

`Map` [[→ 第 6.6 节]](#06_006.html_i06_367)

`clear()` [[→ 第 6.6 节]](#06_006.html_i06_390)

`delete()` [[→ 第 6.6 节]](#06_006.html_i06_388)

`entries()` [[→ 第 6.6 节]](#06_006.html_i06_384)

`forEach()` [[→ 第 6.6 节]](#06_006.html_i06_373)

`get()` [[→ 第 6.6 节]](#06_006.html_i06_377)

`has()` [[→ 第 6.6 节]](#06_006.html_i06_375)

`keys()` [[→ 第 6.6 节]](#06_006.html_i06_382)

`set()` [[→ 第 6.6 节]](#06_006.html_i06_371)

`size` [[→ 第 6.6 节]](#06_006.html_i06_386)

`values()` [[→ 第 6.6 节]](#06_006.html_i06_379)

`map()` [[→ 第 6.1 节]](#06_001.html_i06_59)

`mark` [[→ 第 4.9 节]](#04_009.html_i04_123)

Material（材质（3D 表面））[[→ 第 10.1 节]](#10_001.html_i10_14)

`Math` [[→ 第 6.3 节]](#06_003.html_i06_198) [[→ 第 13.1 节]](#13_001.html_i13_02) [[→ 第 13.1 节]](#13_001.html_i13_04)

`abs()` [[→ 第 2.3 节]](#02_003.html_i02_129) [[→ 第 6.3 节]](#06_003.html_i06_206)

`cbrt()` [[→ 第 6.3 节]](#06_003.html_i06_220)

`ceil()` [[→ 第 6.3 节]](#06_003.html_i06_199)

`cos()` [[→ 第 6.3 节]](#06_003.html_i06_244)

`exp()` [[→ 第 6.3 节]](#06_003.html_i06_226)

`floor()` [[→ 第 2.4 节]](#02_004.html_i02_172) [[→ 第 6.3 节]](#06_003.html_i06_202)

`log()` [[→ 第 6.3 节]](#06_003.html_i06_229)

`log10()` [[→ 第 6.3 节]](#06_003.html_i06_236)

`max()` [[→ 第 6.3 节]](#06_003.html_i06_212)

`min()` [[→ 第 6.3 节]](#06_003.html_i06_215)

`pi` [[→ 第 6.3 节]](#06_003.html_i06_222)

`pow()` [[→ 第 6.3 节]](#06_003.html_i06_233)

`random()` [[→ 第 2.3 节]](#02_003.html_i02_126)

`round()` [[→ 第 6.3 节]](#06_003.html_i06_204)

`sign()` [[→ 第 6.3 节]](#06_003.html_i06_209)

`sin()` [[→ 第 6.3 节]](#06_003.html_i06_242)

`sqrt()` [[→ 第 6.3 节]](#06_003.html_i06_217)

`tan()` [[→ 第 6.3 节]](#06_003.html_i06_246)

`Math.random()` [[→ 第 6.3 节]](#06_003.html_i06_249)

`mathbackground` [[→ 第 13.1 节]](#13_001.html_i13_18)

`mathcolor` [[→ 第 13.1 节]](#13_001.html_i13_19)

`MathJax` [[→ 第 13.1 节]](#13_001.html_i13_01)

`MathML` [[→ 第 13.1 节]](#13_001.html_i13_00)

`dynamic` [[→ 第 13.6 节]](#13_006.html_i13_42)

`mathsize` [[→ 第 13.1 节]](#13_001.html_i13_20)

`Matrix` [[→ 第 13.2 节]](#13_002.html_i13_24)

`MAX_SAFE_INTEGER` [[→ 第 6.3 节]](#06_003.html_i06_263)

`MAX_VALUE` [[→ 第 6.3 节]](#06_003.html_i06_272)

`max()` [[→ 第 6.3 节]](#06_003.html_i06_213)

`max-width` [[→ 第 1.6 节]](#01_006.html_i01_68)

`Media` [[→ 第 15.1 节]](#15_001.html_i15_00)

`Media query`（媒体查询）[[→ 第 1.6 节]](#01_006.html_i01_53)

`Member`（成员）[[→ 第 3.2 节]](#03_002.html_i03_21)

`private`（私有）[[→ 第 3.3 节]](#03_003.html_i03_27)

`static`（静态）[[→ 第 3.5 节]](#03_005.html_i03_40)

`Memory training`（记忆训练）[[→ 第 2.4 节]](#02_004.html_i02_174)

`Mesh`（网格）[[→ 第 10.1 节]](#10_001.html_i10_16)

`MeshNormalMaterial` [[→ 第 10.1 节]](#10_001.html_i10_15)

`Metadata`（元数据）[[→ 第 1.6 节]](#01_006.html_i01_24)

`meter` [[→ 第 4.9 节]](#04_009.html_i04_157)

`Method`（方法）[[→ 第 2.6 节]](#02_006.html_i02_204) [[→ 第 3.2 节]](#03_002.html_i03_19)

`attribute`（属性）[[→ 第 4.2 节]](#04_002.html_i04_34)

`private`（私有）[[→ 第 3.3 节]](#03_003.html_i03_32)

`static`（静态）[[→ 第 3.5 节]](#03_005.html_i03_42) [[→ 第 6.1 节]](#06_001.html_i06_25)

`mfenced` [[→ 第 13.2 节]](#13_002.html_i13_26)

`mfrac` [[→ 第 13.4 节]](#13_004.html_i13_37)

`mi` [[→ 第 13.1 节]](#13_001.html_i13_05)

`MIME type`（MIME 类型）[[→ 第 15.1 节]](#15_001.html_i15_14)

`MIN_SAFE_INTEGER` [[→ 第 6.3 节]](#06_003.html_i06_264)

`MIN_VALUE` [[→ 第 6.3 节]](#06_003.html_i06_274)

`min()` [[→ 第 6.3 节]](#06_003.html_i06_216)

`mn` [[→ 第 13.1 节]](#13_001.html_i13_07)

`mo` [[→ 第 13.1 节]](#13_001.html_i13_06)

Mobile device（移动设备）

`app` [[→ 第 12.1 节]](#12_001.html_i12_01)

`formatting`（格式化）[[→ 第 1.6 节]](#01_006.html_i01_69)

`Modularization`（模块化）[[→ 第 2.6 节]](#02_006.html_i02_203)

`Modulo`（取模）[[→ 第 2.2 节]](#02_002.html_i02_48)

`month` [[→ 第 4.9 节]](#04_009.html_i04_178)

Mouse（鼠标）

`coordinates`（坐标）[[→ 第 4.7 节]](#04_007.html_i04_115)

`event`（事件）[[→ 第 4.7 节]](#04_007.html_i04_100)

`mousedown` [[→ 第 4.7 节]](#04_007.html_i04_104)

`mousemove` [[→ 第 4.7 节]](#04_007.html_i04_102)

`mouseout` [[→ 第 4.7 节]](#04_007.html_i04_110)

`mouseover` [[→ 第 4.7 节]](#04_007.html_i04_108)

`mouseup` [[→ 第 4.7 节]](#04_007.html_i04_106)

`moveTo()` [[→ 第 15.2 节]](#15_002.html_i15_33)

`mroot` [[→ 第 13.1 节]](#13_001.html_i13_10)

`mrow` [[→ 第 13.3 节]](#13_003.html_i13_30)

`msqrt` [[→ 第 13.1 节]](#13_001.html_i13_08)

`msub` [[→ 第 13.1 节]](#13_001.html_i13_11)

`msubsup` [[→ 第 13.1 节]](#13_001.html_i13_14)

`msup` [[→ 第 13.1 节]](#13_001.html_i13_13)

`mtable` [[→ 第 13.2 节]](#13_002.html_i13_27)

`mtd` [[→ 第 13.2 节]](#13_002.html_i13_29)

`mtr` [[→ 第 13.2 节]](#13_002.html_i13_28)

`Multimedia object`（多媒体对象）[[→ 第 9.1 节]](#09_001.html_i09_13)

`multiple`（多选）

`email input`（电子邮件输入）[[→ 第 4.9 节]](#04_009.html_i04_142)

`selection menu`（选择菜单）[[→ 第 4.5 节]](#04_005.html_i04_69)

`Multiplication`（乘法）[[→ 第 2.2 节]](#02_002.html_i02_44)

`sign`（符号）[[→ 第 13.3 节]](#13_003.html_i13_35)

`munderover` [[→ 第 13.3 节]](#13_003.html_i13_31)

## N

`name` [[→ 第 4.4 节]](#04_004.html_i04_63)

`Named function`（具名函数）[[→ 第 2.6 节]](#02_006.html_i02_240)

`Naming rules`（命名规则）[[→ 第 2.1 节]](#02_001.html_i02_12)

`NaN` [[→ 第 2.2 节]](#02_002.html_i02_57) [[→ 第 2.3 节]](#02_003.html_i02_133)

`Natural logarithm`（自然对数）[[→ 第 6.3 节]](#06_003.html_i06_231)

`navigator` [[→ 第 15.3 节]](#15_003.html_i15_52)

`near`（附近）[[→ 第 10.1 节]](#10_001.html_i10_21)

`new`（新建）

`array`（数组）[[→ 第 6.1 节]](#06_001.html_i06_30)

`object`（对象）[[→ 第 3.1 节]](#03_001.html_i03_18)

`next()` [[→ 第 6.6 节]](#06_006.html_i06_359)

`Node`（节点）[[→ 第 5.1 节]](#05_001.html_i05_01) [[→ 第 5.1 节]](#05_001.html_i05_05)

`node`（节点）[[→ 第 5.1 节]](#05_001.html_i05_06)

`appendChild()` [[→ 第 5.4 节]](#05_004.html_i05_40)

`appending`（追加）[[→ 第 5.4 节]](#05_004.html_i05_41)

`changing`（更改）[[→ 第 5.5 节]](#05_005.html_i05_48)

`child`（子节点）[[→ 第 5.3 节]](#05_003.html_i05_24)

`childNodes` [[→ 第 5.3 节]](#05_003.html_i05_29)

`cloneNode()` [[→ 第 5.5 节]](#05_005.html_i05_50)

`cloning`（克隆）[[→ 第 5.5 节]](#05_005.html_i05_51)

`creating`（创建）[[→ 第 5.4 节]](#05_004.html_i05_34)

`deleting`（删除）[[→ 第 5.6 节]](#05_006.html_i05_58)

`deleting an attribute`（删除属性）[[→ 第 5.6 节]](#05_006.html_i05_63)

`determining an attribute`（确定属性）[[→ 第 5.2 节]](#05_002.html_i05_16)

`first`（第一个）[[→ 第 5.2 节]](#05_002.html_i05_19)

`firstChild` [[→ 第 5.2 节]](#05_002.html_i05_21) [[→ 第 7.3 节]](#07_003.html_i07_29)

`getAttribute()` [[→ 第 5.2 节]](#05_002.html_i05_18) [[→ 第 7.3 节]](#07_003.html_i07_31)

`hasChildNodes()` [[→ 第 5.3 节]](#05_003.html_i05_27)

`insertBefore()` [[→ 第 5.4 节]](#05_004.html_i05_46)

`inserting`（插入）[[→ 第 5.4 节]](#05_004.html_i05_47)

`nodeName` [[→ 第 5.3 节]](#05_003.html_i05_33)

`nodeType` [[→ 第 5.3 节]](#05_003.html_i05_30)

`nodeValue` [[→ 第 5.2 节]](#05_002.html_i05_22)

`removeAttribute()` [[→ 第 5.6 节]](#05_006.html_i05_62)

`removeChild()` [[→ 第 5.6 节]](#05_006.html_i05_60)

`replaceChild()` [[→ 第 5.5 节]](#05_005.html_i05_53)

`replacing`（替换）[[→ 第 5.5 节]](#05_005.html_i05_54)

`setAttribute()` [[→ 第 5.4 节]](#05_004.html_i05_43)

`setting an attribute`（设置属性）[[→ 第 5.4 节]](#05_004.html_i05_44)

`type`（类型）[[→ 第 5.3 节]](#05_003.html_i05_31)

`value`（值）[[→ 第 5.2 节]](#05_002.html_i05_23)

`nodeName` [[→ 第 5.3 节]](#05_003.html_i05_32)

`noscript` [[→ 第 1.11 节]](#01_011.html_i01_110)

`NOT`（逻辑）[[→ 第 2.3 节]](#02_003.html_i02_120)

`Not a number`（非数字）[[→ 第 2.2 节]](#02_002.html_i02_58) [[→ 第 2.3 节]](#02_003.html_i02_132)

`Not equal to`（不等于）[[→ 第 2.3 节]](#02_003.html_i02_101)

`Notepad++` [[→ 第 1.1 节]](#01_001.html_i01_06) [[→ 第 1.6 节]](#01_006.html_i01_52)

`noValidate` [[→ 第 4.9 节]](#04_009.html_i04_196)

`novalidate` [[→ 第 4.9 节]](#04_009.html_i04_193)

`null` [[→ 第 2.1 节]](#02_001.html_i02_23) [[→ 第 3.7 节]](#03_007.html_i03_47)

`null coalescence`（空值合并）[[→ 第 3.7 节]](#03_007.html_i03_49)

`Number`（数字）[[→ 第 2.1 节]](#02_001.html_i02_26) [[→ 第 6.3 节]](#06_003.html_i06_259)

作为指数形式 [[→ 第 6.3 节]](#06_003.html_i06_271)

基数 [[→ 第 2.2 节]](#02_002.html_i02_79)

检查 [[→ 第 2.3 节]](#02_003.html_i02_125)

截断 [[→ 第 2.4 节]](#02_004.html_i02_173)

`EPSILON` [[→ 第 6.3 节]](#06_003.html_i06_277)

扩展 [[→ 第 6.3 节]](#06_003.html_i06_282)

极值 [[→ 第 6.3 节]](#06_003.html_i06_214)

格式化 [[→ 第 6.3 节]](#06_003.html_i06_284)

输入 [[→ 第 2.2 节]](#02_002.html_i02_71)

输入字段 [[→ 第 4.9 节]](#04_009.html_i04_150) [[→ 第 4.9 节]](#04_009.html_i04_151)

输入字段已更改 [[→ 第 4.9 节]](#04_009.html_i04_164)

整数 [[→ 第 6.3 节]](#06_003.html_i06_260)

多位数字 [[→ 第 2.1 节]](#02_001.html_i02_31)

`MAX_VALUE` [[→ 第 6.3 节]](#06_003.html_i06_273)

`MIN_VALUE` [[→ 第 6.3 节]](#06_003.html_i06_275)

舍入 [[→ 第 2.4 节]](#02_004.html_i02_153) [[→ 第 6.3 节]](#06_003.html_i06_201) [[→ 第 6.3 节]](#06_003.html_i06_268)

符号 [[→ 第 6.3 节]](#06_003.html_i06_211)

系统 [[→ 第 2.2 节]](#02_002.html_i02_81)

`toExponential()` [[→ 第 6.3 节]](#06_003.html_i06_270)

`toFixed()` [[→ 第 2.4 节]](#02_004.html_i02_152)

非常大 [[→ 第 6.3 节]](#06_003.html_i06_262)

带小数位 [[→ 第 6.3 节]](#06_003.html_i06_266)

`number`（类型）[[→ 第 2.3 节]](#02_003.html_i02_138)

`number.js` [[→ 第 6.3 节]](#06_003.html_i06_285)

## O

`Object`（对象）[[→ 第 3.1 节]](#03_001.html_i03_01) [[→ 第 6.1 节]](#06_001.html_i06_00)

从数组创建 [[→ 第 6.1 节]](#06_001.html_i06_126)

检查 [[→ 第 6.1 节]](#06_001.html_i06_42)

检查类 [[→ 第 3.10 节]](#03_010.html_i03_72)

转换（JSON）[[→ 第 6.7 节]](#06_007.html_i06_393)

复制 [[→ 第 3.11 节]](#03_011.html_i03_85)

当前 [[→ 第 3.1 节]](#03_001.html_i03_15)

扩展 [[→ 第 6.3 节]](#06_003.html_i06_281) [[→ 第 6.4 节]](#06_004.html_i06_307) [[→ 第 6.4 节]](#06_004.html_i06_332)

对象中 [[→ 第 3.8 节]](#03_008.html_i03_53)

JSON 格式 [[→ 第 6.7 节]](#06_007.html_i06_392)

成员 [[→ 第 3.10 节]](#03_010.html_i03_63)

输出 [[→ 第 3.2 节]](#03_002.html_i03_25)

参数 [[→ 第 3.10 节]](#03_010.html_i03_80)

引用 [[→ 第 3.1 节]](#03_001.html_i03_16)

返回值 [[→ 第 3.10 节]](#03_010.html_i03_82)

SVG [[→ 第 9.1 节]](#09_001.html_i09_15)

`Three.js` [[→ 第 10.1 节]](#10_001.html_i10_08)

类型 [[→ 第 3.10 节]](#03_010.html_i03_77)

面向对象 [[→ 第 3.1 节]](#03_001.html_i03_00)

八面体 [[→ 第 10.4 节]](#10_004.html_i10_53)

八进制数 [[→ 第 2.2 节]](#02_002.html_i02_84)

`offsetX` [[→ 第 4.7 节]](#04_007.html_i04_113)

`onerror` [[→ 第 2.5 节]](#02_005.html_i02_180)

`onreadystatechange` [[→ 第 7.1 节]](#07_001.html_i07_04)

`ons.notification` [[→ 第 12.1 节]](#12_001.html_i12_10)

`ons.notification.confirm()` [[→ 第 12.2 节]](#12_002.html_i12_29)

`ons.notification.prompt()` [[→ 第 12.2 节]](#12_002.html_i12_32)

`ons.notification.toast()` [[→ 第 12.2 节]](#12_002.html_i12_35)

`ons-button` [[→ 第 12.1 节]](#12_001.html_i12_09)

`ons-checkbox` [[→ 第 12.2 节]](#12_002.html_i12_50)

`ons-col` [[→ 第 12.1 节]](#12_001.html_i12_23)

Onsen UI [[→ 第 12.1 节]](#12_001.html_i12_00)

对齐 [[→ 第 12.1 节]](#12_001.html_i12_19)

按钮 [[→ 第 12.1 节]](#12_001.html_i12_08)

确认 [[→ 第 12.2 节]](#12_002.html_i12_30)

浮动操作按钮 [[→ 第 12.2 节]](#12_002.html_i12_26)

图标 [[→ 第 12.2 节]](#12_002.html_i12_25)

输入 [[→ 第 12.2 节]](#12_002.html_i12_33)

输入字段 [[→ 第 12.2 节]](#12_002.html_i12_41)

标签 [[→ 第 12.2 节]](#12_002.html_i12_45)

列表 [[→ 第 12.1 节]](#12_001.html_i12_14)

消息 [[→ 第 12.1 节]](#12_001.html_i12_13)

导航栏 [[→ 第 12.1 节]](#12_001.html_i12_05)

选择菜单 [[→ 第 12.2 节]](#12_002.html_i12_48)

滑块 [[→ 第 12.2 节]](#12_002.html_i12_57)

标准对话框 [[→ 第 12.1 节]](#12_001.html_i12_11) [[→ 第 12.2 节]](#12_002.html_i12_28)

结构 [[→ 第 12.1 节]](#12_001.html_i12_04)

开关 [[→ 第 12.2 节]](#12_002.html_i12_54)

表格 [[→ 第 12.1 节]](#12_001.html_i12_24)

点击 [[→ 第 12.1 节]](#12_001.html_i12_21)

吐司提示 [[→ 第 12.2 节]](#12_002.html_i12_36)

`ons-icon` [[→ 第 12.2 节]](#12_002.html_i12_27)

`ons-input` [[→ 第 12.2 节]](#12_002.html_i12_40)

`ons-list` [[→ 第 12.1 节]](#12_001.html_i12_15)

`ons-list-header` [[→ 第 12.1 节]](#12_001.html_i12_18)

`ons-list-item` [[→ 第 12.1 节]](#12_001.html_i12_16)

`ons-list-title` [[→ 第 12.1 节]](#12_001.html_i12_17)

`ons-page` [[→ 第 12.1 节]](#12_001.html_i12_06)

`ons-radio` [[→ 第 12.2 节]](#12_002.html_i12_51)

`ons-range` [[→ 第 12.2 节]](#12_002.html_i12_56)

`ons-row` [[→ 第 12.1 节]](#12_001.html_i12_22)

`ons-search-input` [[→ 第 12.2 节]](#12_002.html_i12_42)

`ons-select` [[→ 第 12.2 节]](#12_002.html_i12_47)

`ons-switch` [[→ 第 12.2 节]](#12_002.html_i12_54)

`ons-toolbar` [[→ 第 12.1 节]](#12_001.html_i12_07)

`opacity`（不透明度）

CSS [[→ 第 8.2 节]](#08_002.html_i08_52)

SVG [[→ 第 9.4 节]](#09_004.html_i09_52)

`open()` [[→ 第 7.1 节]](#07_001.html_i07_02)

运算符

赋值 [[→ 第 2.2 节]](#02_002.html_i02_59)

计算 [[→ 第 2.2 节]](#02_002.html_i02_40) [[→ 第 2.2 节]](#02_002.html_i02_49)

比较 [[→ 第 2.3 节]](#02_003.html_i02_93)

逻辑 [[→ 第 2.3 节]](#02_003.html_i02_114)

优先级 [[→ 第 2.2 节]](#02_002.html_i02_53) [[→ 第 2.3 节]](#02_003.html_i02_142)

三元 [[→ 第 2.3 节]](#02_003.html_i02_103)

选项 [[→ 第 4.5 节]](#04_005.html_i04_73)

搜索列表 [[→ 第 4.9 节]](#04_009.html_i04_136)

选择菜单 [[→ 第 4.5 节]](#04_005.html_i04_70)

`OR`（或）

逻辑 [[→ 第 2.3 节]](#02_003.html_i02_118)

短路 [[→ 第 2.6 节]](#02_006.html_i02_225)

方向 [[→ 第 1.6 节]](#01_006.html_i01_70)

大圆航线 [[→ 第 15.3 节]](#15_003.html_i15_64)

输出

对话框 [[→ 第 2.1 节]](#02_001.html_i02_20)

对象 [[→ 第 3.2 节]](#03_002.html_i03_24)

叠加层 [[→ 第 8.1 节]](#08_001.html_i08_29)

## P

- `PerspectiveCamera` [→ 第 10.1 节]
- PHP 程序 [→ 第 4.2 节] [→ 第 4.2 节]
- `Pi` [→ 第 1.7 节] [→ 第 6.3 节]
- 占位符（Placeholder）[→ 第 4.9 节] [→ 第 4.9 节] [→ 第 12.2 节]
- `play()` [→ 第 15.1 节]
- `Polygon`（多边形）[→ 第 9.2 节] [→ 第 9.2 节]
- SVG [→ 第 9.2 节]
- `Polyline`（折线）[→ 第 9.2 节] [→ 第 9.2 节]
- SVG [→ 第 9.2 节]
- `pop()` [→ 第 6.1 节]
- 竖向格式（Portrait format）[→ 第 15.3 节]
- 竖向模式（Portrait mode）[→ 第 1.6 节]
- `position` [→ 第 10.1 节]
- 位置（Position）
  - CSS [→ 第 8.2 节]
  - jQuery [→ 第 11.4 节]
  - `sensor` [→ 第 15.3 节]
  - `z-direction` [→ 第 8.2 节]
- `post` [→ 第 4.2 节]
- POST 方法 [→ 第 7.1 节]
- `post()` [→ 第 11.6 节]
- 后缀法（Postfix）[→ 第 2.2 节]
- `pow()` [→ 第 6.3 节]
- 幂函数（Power function）[→ 第 6.3 节]
- 前缀（Prefix）[→ 第 2.2 节]
- `preventDefault()` [→ 第 4.3 节]
- 优先级（Priority）[→ 第 2.2 节] [→ 第 2.3 节]
- `private` [→ 第 3.3 节]
- 乘积符号（Product symbol）[→ 第 13.3 节]
- 程序（Program）
  - 避免中止 [→ 第 2.5 节]
  - 子分（subdividing）[→ 第 2.6 节]
- `progress` [→ 第 4.9 节]
- 进度条（Progress bar）[→ 第 4.9 节]
- `prompt()` [→ 第 2.1 节] [→ 第 2.2 节]
- Onsen UI [→ 第 12.2 节]
- 属性（Property）[→ 第 3.1 节]
  - 访问（access）[→ 第 3.4 节]
  - 组合名称（composing a name）[→ 第 10.0 节]
  - 删除（deleting）[→ 第 10.0 节]
  - `private` [→ 第 3.3 节]
  - `static` [→ 第 5.0 节]
  - `prototype` [→ 第 3.1 节] [→ 第 6.1 节] [→ 第 6.3 节] [→ 第 6.4 节] [→ 第 6.4 节]
  - `public` [→ 第 3.3 节]
- `push()` [→ 第 6.1 节]

## Q

- `queue`（队列）[→ 第 11.4 节]
- 引号（Quotation marks）[→ 第 1.8 节]

## R

- 弧度（Radians）[→ 第 6.3 节]
- 单选按钮（Radio button）[→ 第 4.4 节] [→ 第 4.4 节]
  - Onsen UI [→ 第 12.2 节]
  - `selected` [→ 第 4.6 节]
- 随机数（Random number）[→ 第 2.3 节] [→ 第 6.3 节]
- `random()` [→ 第 2.3 节] [→ 第 6.3 节]
- `range`（范围）[→ 第 4.9 节]
- `rangeOverflow`（范围溢出）[→ 第 4.9 节]
- `rangeUnderflow`（范围下溢）[→ 第 4.9 节]
- 循环读取（Read-in loop）[→ 第 2.4 节]
- 只读（Read-only）[→ 第 4.6 节]
- `readonly` [→ 第 4.6 节]
- `ready()` [→ 第 11.1 节]
- `readystate` [→ 第 7.1 节]
- 记录路由（Recording a route）[→ 第 15.3 节]
- `rect`（矩形）[→ 第 9.1 节]
- `Rectangle`（矩形）[→ 第 9.2 节]
  - `canvas`（画布）[→ 第 15.2 节]
  - SVG [→ 第 9.1 节]
- 递归（Recursion）[→ 第 2.6 节]
- 引用（Reference）[→ 第 2.6 节]
  - 拷贝（copying）[→ 第 2.6 节]
  - 错误（error）[→ 第 2.5 节] [→ 第 2.5 节]
  - 传递给函数（to a function）[→ 第 2.6 节]
  - 传递给元素（to element）[→ 第 4.1 节]
  - 传递给无（to nothing）[→ 第 2.1 节] [→ 第 3.7 节]
  - 传递给对象（to object）[→ 第 3.1 节]
- 正则表达式（Regular expression）[→ 第 4.9 节]
- `rel`（相对）[→ 第 1.6 节] [→ 第 8.1 节]
- `removeAttribute()` [→ 第 5.6 节]
- `removeChild()` [→ 第 5.6 节]
- `render()` [→ 第 10.1 节]
- `repeat()` [→ 第 6.2 节]
- `replace()` [→ 第 6.2 节]
- `replaceAll()` [→ 第 6.2 节]
- `replaceChild()` [→ 第 5.5 节]
- `Request`（请求）[→ 第 7.1 节]
- `requestAnimationFrame()` [→ 第 10.3 节]
- `required`（必须的）[→ 第 4.3 节]
  - 更改（change）[→ 第 4.9 节]
  - 重置（reset）[→ 第 4.2 节]
- 重置中（Resetting）[→ 第 4.2 节]
- `Response`（响应）[→ 第 7.1 节]
- `responseText` [→ 第 7.1 节]
- `responseXML` [→ 第 7.3 节]
- 响应式网页设计（Responsive web design）[→ 第 1.6 节]
- `return`（返回）[→ 第 2.6 节]
- 返回值（Return value）[→ 第 2.6 节]
  - 数组（array）[→ 第 6.1 节]
  - 多个（multiple）[→ 第 2.6 节]
  - 对象（object）[→ 第 3.10 节]
- `reverse()`（反转）[→ 第 6.1 节]
- `rgb()` [→ 第 8.2 节]
- 根节点（Root node）[→ 第 5.1 节]
- 根符号（Root symbol）[→ 第 13.1 节]
- 旋转（Rotation）[→ 第 9.5 节] [→ 第 10.3 节]
- `rotationRate`（旋转速率）[→ 第 15.3 节]
- `round()`（四舍五入）[→ 第 6.3 节]
- `rows`（行）[→ 第 4.3 节]

## S

- 示例项目（Sample projects）[→ 第 14.1 节]
- 量积（Scalar product）[→ 第 13.6 节]
- 缩放（Scaling）[→ 第 9.5 节]
- `Scene`（场景）[→ 第 10.1 节]
- 屏幕（Screen）[→ 第 1.6 节]
- `script`（脚本）[→ 第 1.8 节]
- `src`（源）[→ 第 1.9 节]
- 搜索（Search）
  - 输入字段（input field）[→ 第 4.9 节]
  - 列表（list）[→ 第 4.9 节]
  - 字符串（string）[→ 第 13.6 节]
  - 术语（term）[→ 第 4.9 节]
  - `select`（选择）[→ 第 4.6 节]
  - `selected`（已选中）[→ 第 4.6 节]
- 选择菜单（Selection）
  - Onsen UI [→ 第 12.2 节]
  - 状态改变（changed）[→ 第 4.6 节]
  - 可见性（visibility）[→ 第 8.3 节]
- 选择器（Selector）[→ 第 8.1 节]
- 分号（Semicolon）
  - CSS [→ 第 8.1 节]
  - JavaScript [→ 第 1.8 节]
- `send()`（发送）[→ 第 7.1 节]
- `Sensor`（传感器）[→ 第 15.3 节]
- 分隔符（Separator）[→ 第 2.1 节]
- `Set`（集合）[→ 第 6.2 节]
- `set`（设置）[→ 第 3.4 节] [→ 第 6.2 节]
  - `add()`（添加）[→ 第 6.2 节]
  - 添加元素（adding an element）[→ 第 6.2 节]
  - `clear()`（清空）[→ 第 6.2 节]
  - `delete()`（删除）[→ 第 6.2 节]
  - `forEach()`（遍历）[→ 第 6.2 节]
  - `has()`（拥有）[→ 第 6.2 节]
  - `size`（大小）[→ 第 6.2 节]
  - `values()`（值）[→ 第 6.2 节]

`setAttribute()` [→ 第 5.4 节]

`SVG` [→ 第 9.6 节]

`setClearColor()` [→ 第 10.1 节]

`setHours()` [→ 第 4.9 节]

`setInterval()` [→ 第 6.5 节]

`setRequestHeader()` [→ 第 7.2 节]

`setSize()` [→ 第 10.1 节]

`Setter` [→ 第 3.4 节]

`setTimeout()` [→ 第 4.9 节] [→ 第 6.5 节]

`Shift` [→ 第 9.5 节]

`shift()` [→ 第 6.1 节]

短路 [→ 第 2.3 节] [→ 第 2.6 节]

`show()` [→ 第 11.4 节]

`sign()` [→ 第 6.3 节]

`sin()` [→ 第 6.3 节]

`Sine` [→ 第 6.3 节]

`Size` [→ 第 8.2 节]

`jQuery` [→ 第 11.4 节]

`Map` [→ 第 6.6 节]

`Set` [→ 第 6.6 节]

`slice()` [→ 第 6.1 节]

`slideDown()` [→ 第 11.4 节]

`Slider` [→ 第 4.9 节]

`Slideshow` [→ 第 6.5 节]

`slideToggle()` [→ 第 11.4 节]

`slideUp()` [→ 第 11.4 节]

智能手机 [→ 第 12.1 节]

`some()` [→ 第 6.1 节]

## sort()

- 按字符排序 [→ 第 6.1 节]
- 按数字排序 [→ 第 6.1 节]

`source` [→ 第 15.1 节]

`span` [→ 第 0.6 节]

特殊字符 [→ 第 0.7 节] [→ 第 13.5 节]

`Sphere` [→ 第 10.4 节]

`splice()` [→ 第 6.1 节]

`split()` [→ 第 6.2 节]

展开运算符 [→ 第 6.1 节]

`sqrt()` [→ 第 6.3 节]

## src

- audio [→ 第 15.1 节]
- img [→ 第 0.6 节]
- script [→ 第 0.9 节]

起始状态 [→ 第 9.7 节]

`startsWith()` [→ 第 6.2 节]

`static` [→ 第 3.5 节]

- 成员 [→ 第 3.5 节]

静态块 [→ 第 3.6 节]

## Static method

- 数组 [→ 第 6.1 节]
- 字符串 [→ 第 6.2 节]

`status` [→ 第 7.1 节]

`stepDown()` [→ 第 4.9 节]

`stepUp()` [→ 第 4.9 节]

## String

`String` [→ 第 2.1 节] [→ 第 6.2 节]

`[ ]` [→ 第 6.2 节]

`at()` [→ 第 6.2 节]

`codePointAt()` [→ 第 6.2 节]

组合的 [→ 第 2.1 节]

包含 [→ 第 6.2 节]

`endsWith()` [→ 第 6.2 节]

`fromCodePoint()` [→ 第 6.2 节] [→ 第 6.2 节]

`includes()` [→ 第 6.2 节]

`indexOf()` [→ 第 6.2 节]

`isWellFormed()` [→ 第 6.2 节]

`lastIndexOf()` [→ 第 6.2 节]

`length` [→ 第 4.3 节] [→ 第 6.2 节]

填充 [→ 第 6.2 节]

`padEnd()` [→ 第 6.2 节]

`padStart()` [→ 第 6.2 节]

移除空格 [→ 第 6.2 节]

`repeat()` [→ 第 6.2 节]

重复字符 [→ 第 6.2 节]

`replace()` [→ 第 6.2 节]

`replaceAll()` [→ 第 6.2 节]

替换字符 [→ 第 6.2 节]

搜索位置 [→ 第 6.2 节]

单字符 [→ 第 6.2 节]

`split()` [→ 第 6.2 节]

`startsWith()` [→ 第 6.2 节]

`substr()` [→ 第 6.2 节]

`substring()` [→ 第 6.2 节]

转数组 [→ 第 6.1 节] [→ 第 6.2 节]

转整数 [→ 第 2.2 节]

转数字 [→ 第 2.2 节]

`toLowerCase()` [→ 第 6.2 节]

`toUpperCase()` [→ 第 6.2 节]

`trim()` [→ 第 6.2 节]

`trimEnd()` [→ 第 6.2 节]

`trimStart()` [→ 第 6.2 节]

Unicode [→ 第 6.2 节]

大写/小写 [→ 第 6.2 节]

字符串（类型）[→ 第 2.3 节]

`stringify()` [→ 第 6.7 节]

`stroke` [→ 第 9.2 节]

`stroke()` [→ 第 15.2 节]

`strokeRect()` [→ 第 15.2 节]

`strokeStyle` [→ 第 15.2 节]

`strokeText()` [→ 第 15.2 节]

`stroke-width` [→ 第 9.2 节]

## style

- 属性 [→ 第 8.1 节]
- 标签 [→ 第 8.1 节]

样式表 [→ 第 8.1 节]

子菜单 [→ 第 8.3 节]

`submit` [→ 第 4.2 节]

提交到 PHP [→ 第 4.2 节]

`substr()` [→ 第 6.2 节]

`substring()` [→ 第 6.2 节]

减法 [→ 第 2.2 节]

求和符号 [→ 第 13.3 节]

`super` [→ 第 3.9 节]

`super()` [→ 第 3.9 节]

表面材料 [→ 第 10.1 节]

## SVG

`SVG` [→ 第 9.1 节]

`svg` [→ 第 9.1 节]

- 动画 [→ 第 9.4 节]
- 隐藏 [→ 第 9.2 节]
- 创建文件 [→ 第 9.1 节]
- 失真 [→ 第 9.5 节]
- 动态 [→ 第 9.7 节]
- 嵌入 [→ 第 9.2 节]
- 事件 [→ 第 9.4 节]
- 组 [→ 第 9.3 节]
- 插入文件 [→ 第 9.1 节]
- JavaScript [→ 第 9.6 节]
- 旋转 [→ 第 9.5 节]
- 缩放 [→ 第 9.5 节]
- 平移 [→ 第 9.5 节]

`switch` [→ 第 2.3 节]

语法错误 [→ 第 2.5 节]

系统方程 [→ 第 13.2 节]

## T

Table [→ 第 1.6 节]

- DOM [→ 第 5.7 节]
- HTML [→ 第 1.6 节]
- JavaScript [→ 第 2.4 节]
- MathML [→ 第 13.2 节]

平板 [→ 第 12.1 节]

标签 [→ 第 1.6 节] [→ 第 5.2 节]

取根 [→ 第 6.3 节]

`tan()` [→ 第 6.3 节]

Tangent [→ 第 6.3 节]

可点击 [→ 第 12.1 节]

`target` [→ 第 4.6 节]

`td` [→ 第 1.6 节]

`tel` [→ 第 4.9 节]

三元运算符 [→ 第 2.3 节]

四面体 [→ 第 10.4 节]

`text()` [[→ Section 11.2]](#11_002.html_i11_14)

`textarea` [[→ Section 4.3]](#04_003.html_i04_50)

`textBaseline` [[→ Section 15.2]](#15_002.html_i15_47)

`theisweb.de` [[→ Section 4.2]](#04_002.html_i04_32)

`then()` [[→ Section 12.2]](#12_002.html_i12_38)

`this`

`callback` [[→ Section 6.1]](#06_001.html_i06_56)

`object` [[→ Section 3.1]](#03_001.html_i03_11)

`Three.js` [[→ Section 10.1]](#10_001.html_i10_00)

`object` [[→ Section 10.1]](#10_001.html_i10_09)

三维图形 [[→ Section 10.1]](#10_001.html_i10_01)

`throw` [[→ Section 2.5]](#02_005.html_i02_193)

抛出异常 [[→ Section 2.5]](#02_005.html_i02_192)

时间 [[→ Section 4.9]](#04_009.html_i04_176)

添加 [[→ Section 6.4]](#06_004.html_i06_329) [[→ Section 6.4]](#06_004.html_i06_331)

计算 [[→ Section 6.4]](#06_004.html_i06_327)

日期对象 [[→ Section 6.4]](#06_004.html_i06_289)

差值 [[→ Section 6.4]](#06_004.html_i06_301)

输入字段 [[→ Section 4.9]](#04_009.html_i04_173)

规范，格式 [[→ Section 6.4]](#06_004.html_i06_303) [[→ Section 6.4]](#06_004.html_i06_306)

时间数据

创建 [[→ Section 6.4]](#06_004.html_i06_292)

输出 [[→ Section 6.4]](#06_004.html_i06_294)

时间控制过程 [[→ Section 6.5]](#06_005.html_i06_335)

超时 [[→ Section 4.9]](#04_009.html_i04_168)

`timestamp` [[→ Section 11.3]](#11_003.html_i11_38) [[→ Section 15.3]](#15_003.html_i15_57)

`title` [[→ Section 1.6]](#01_006.html_i01_23)

吐提示 [[→ Section 12.2]](#12_002.html_i12_37)

`toExponential()` [[→ Section 6.3]](#06_003.html_i06_269)

`toFixed()` [[→ Section 2.4]](#02_004.html_i02_151) [[→ Section 6.3]](#06_003.html_i06_267)

`toggle()` [[→ Section 11.4]](#11_004.html_i11_59)

`toLocaleDateString()` [[→ Section 4.9]](#04_009.html_i04_183)

`toLocaleString()` [[→ Section 6.4]](#06_004.html_i06_295)

`toLocaleTimeString()` [[→ Section 4.9]](#04_009.html_i04_185)

`toLowerCase()` [[→ Section 6.2]](#06_002.html_i06_170)

`top` [[→ Section 8.2]](#08_002.html_i08_35)

`toReversed()` [[→ Section 6.1]](#06_001.html_i06_96)

圆环体 [[→ Section 10.4]](#10_004.html_i10_55) [[→ Section 10.4]](#10_004.html_i10_56)

`toSorted()` [[→ Section 6.1]](#06_001.html_i06_94) [[→ Section 6.1]](#06_001.html_i06_109)

`toSpliced()` [[→ Section 6.1]](#06_001.html_i06_73)

`toString()` [[→ Section 6.1]](#06_001.html_i06_73)

数组 [[→ Section 6.1]](#06_001.html_i06_08)

转换数字 [[→ Section 2.2]](#02_002.html_i02_82)

对象 [[→ Section 3.2]](#03_002.html_i03_23)

`toUpperCase()` [[→ Section 6.2]](#06_002.html_i06_167)

`toUTCString()` [[→ Section 6.4]](#06_004.html_i06_297)

`tr` [[→ Section 1.6]](#01_006.html_i01_46)

翻译 [[→ Section 9.5]](#09_005.html_i09_60)

透明度

CSS [[→ Section 8.2]](#08_002.html_i08_50) [[→ Section 8.3]](#08_003.html_i08_62)

SVG [[→ Section 9.4]](#09_004.html_i09_53)

树（DOM）[[→ Section 5.1]](#05_001.html_i05_10)

三角函数 [[→ Section 6.3]](#06_003.html_i06_241)

`trim()` [[→ Section 6.2]](#06_002.html_i06_185)

`trimEnd()` [[→ Section 6.2]](#06_002.html_i06_190)

`trimStart()` [[→ Section 6.2]](#06_002.html_i06_188)

`true` [[→ Section 2.1]](#02_001.html_i02_37)

真值 [[→ Section 2.1]](#02_001.html_i02_35)

条件 [[→ Section 2.3]](#02_003.html_i02_106)

`try` [[→ Section 2.5]](#02_005.html_i02_184)

二维图形 [[→ Section 9.1]](#09_001.html_i09_01)

类型 [[→ Section 3.10]](#03_010.html_i03_73)

转换 [[→ Section 2.1]](#02_001.html_i02_34)

确定 [[→ Section 3.10]](#03_010.html_i03_75)

事件 [[→ Section 4.6]](#04_006.html_i04_99)

输入 [[→ Section 4.1]](#04_001.html_i04_08)

jQuery [[→ Section 11.3]](#11_003.html_i11_32)

类型数组 [[→ Section 6.3]](#06_003.html_i06_256) [[→ Section 6.3]](#06_003.html_i06_278)

`typeof` [[→ Section 2.3]](#02_003.html_i02_136) [[→ Section 3.10]](#03_010.html_i03_74)

## U

Ubuntu Linux [[→ Section A.1]](#A_001.html_i16_02)

`Uint32Array` [[→ Section 6.3]](#06_003.html_i06_257)

`ul` [[→ Section 1.6]](#01_006.html_i01_42)

`undefined` [[→ Section 2.1]](#02_001.html_i02_09)

Unicode [[→ Section 1.6]](#01_006.html_i01_51) [[→ Section 6.2]](#06_002.html_i06_195)

协调世界时（UTC）[[→ Section 4.9]](#04_009.html_i04_175) [[→ Section 6.4]](#06_004.html_i06_291)

`unshift()` [[→ Section 6.1]](#06_001.html_i06_67)

上/下按钮 [[→ Section 4.9]](#04_009.html_i04_152)

URL [[→ Section 4.8]](#04_008.html_i04_118)

`url` [[→ Section 4.9]](#04_009.html_i04_144)

UTF-8 编码 [[→ Section 1.6]](#01_006.html_i01_50)

UTF-16 编码 [[→ Section 6.1]](#06_001.html_i06_101) [[→ Section 6.2]](#06_002.html_i06_152)

## V

`valid` [[→ Section 4.9]](#04_009.html_i04_201)

验证表 [[→ Section 4.9]](#04_009.html_i04_120) [[→ Section 4.9]](#04_009.html_i04_192)

有效性 [[→ Section 2.6]](#02_006.html_i02_232) [[→ Section 4.9]](#04_009.html_i04_197)

`value`按钮 [[→ Section 4.1]](#04_001.html_i04_09)

复选框 [[→ Section 4.4]](#04_004.html_i04_66)

输入字段 [[→ Section 4.1]](#04_001.html_i04_21)

单选按钮 [[→ Section 4.4]](#04_004.html_i04_65)

选择菜单 [[→ Section 4.5]](#04_005.html_i04_71)

值 [[→ Section 4.3]](#04_003.html_i04_53)

`valueAsDate` [[→ Section 4.9]](#04_009.html_i04_181)

`values()`Map [[→ Section 6.6]](#06_006.html_i06_378)Set [[→ Section 6.6]](#06_006.html_i06_355)

`var`变量 [[→ Section 2.1]](#02_001.html_i02_00)

变量 [[→ Section 2.1]](#02_001.html_i02_00)

确定类型 [[→ Section 2.3]](#02_003.html_i02_137)

隐藏 [[→ Section 2.6]](#02_006.html_i02_237)

监控 [[→ Section 2.5]](#02_005.html_i02_200)

有效性 [[→ Section 2.6]](#02_006.html_i02_233)

向量 [[→ Section 13.2]](#13_002.html_i13_22)

图形 [[→ Section 9.1]](#09_001.html_i09_04)

`video`视频播放器 [[→ Section 15.1]](#15_001.html_i15_11) [[→ Section 15.1]](#15_001.html_i15_12)

查看方向 [[→ Section 10.1]](#10_001.html_i10_27)

`visibility` [[→ Section 8.2]](#08_002.html_i08_54)

## W

等待 [[→ Section 2.5]](#02_005.html_i02_199)

波形音频格式（WAV）[[→ Section 15.1]](#15_001.html_i15_03)

跟踪 [[→ Section 15.3]](#15_003.html_i15_60)

Web 服务器

互联网 [[→ Section 4.2]](#04_002.html_i04_31)

本地 [[→ Section 4.2]](#04_002.html_i04_28)

`WebGL` [[→ Section 10.1]](#10_001.html_i10_04)

`WebGLRenderer` [[→ Section 10.1]](#10_001.html_i10_29)

`week` [[→ Section 4.9]](#04_009.html_i04_179)

工作日 [[→ Section 6.4]](#06_004.html_i06_312)

`while` [[→ Section 2.4]](#02_004.html_i02_166)

`width` [[→ Section 8.2]](#08_002.html_i08_39)

`willValidate` [[→ Section 4.9]](#04_009.html_i04_198)

`window`

`alert()` [[→ Section 2.1]](#02_001.html_i02_19)

`clearInterval()` [[→ Section 6.5]](#06_005.html_i06_342)

`clearTimeout()` [[→ Section 4.9]](#04_009.html_i04_170)

`confirm()` [[→ Section 2.3]](#02_003.html_i02_10)

`innerHeight` [[→ Section 10.1]](#10_001.html_i10_37)

`innerWidth` [[→ Section 10.1]](#10_001.html_i10_35)

`prompt()` [[→ Section 2.1]](#02_001.html_i02_16)

`requestAnimationFrame()` [[→ Section 10.3]](#10_003.html_i10_47)

`setInterval()` [[→ Section 6.5]](#06_005.html_i06_339)

`setTimeout()` [[→ Section 4.9]](#04_009.html_i04_167) [[→ Section 6.5]](#06_005.html_i06_337)

`with()` [[→ Section 6.1]](#06_001.html_i06_98)

## X

`XAMPP` [[→ Section 4.2]](#04_002.html_i04_29) [[→ Section A.1]](#A_001.html_i16_00)

安装 [[→ Section A.1]](#A_001.html_i16_01)

`XML` [[→ Section 7.3]](#07_003.html_i07_23)

命名空间 [[→ Section 9.1]](#09_001.html_i09_10)

`XMLHttpRequest` [[→ Section 7.1]](#07_001.html_i07_01)

`onreadystatechange` [[→ Section 7.1]](#07_001.html_i07_05)

`open()` [[→ Section 7.1]](#07_001.html_i07_03)

`readyState` [[→ Section 7.1]](#07_001.html_i07_09)

`responseText` [[→ Section 7.1]](#07_001.html_i07_14)

`send()` [[→ Section 7.1]](#07_001.html_i07_07)

`setRequestHeader()` [[→ Section 7.2]](#07_002.html_i07_22)

`status` [[→ Section 7.1]](#07_001.html_i07_11)

`xmlns` [[→ Section 9.1]](#09_001.html_i09_09)

# 服务页面

以下部分包含如何联系我们的一些说明。此外，我们还为您提供了关于电子书屏幕布局自定义的进一步建议。

## 赞誉与批评

我们希望您喜欢阅读本书。如果它达到了您的期望，请推荐给他人。如果您认为还有改进空间，请与本书编辑联系：Megan Fuerst。我们欢迎任何改进建议，当然也欢迎任何赞誉！您也可以通过社交媒体或电子邮件分享您的阅读体验。

## 补充材料

如果有可用的补充材料（示例代码、练习材料、列表等），它们将提供在您的在线图书馆以及本书的网络目录页面上。您可以通过以下链接直接导航到该页面：[`www.rheinwerk-computing.com/5875`](http://www.sap-press.com/5875)。如果我们发现影响含义的拼写错误或内容错误，我们也会在那里提供更正列表。

## 技术问题

如果您在使用 Rheinwerk Computing 的电子书或电子书账户时遇到技术问题，请随时联系我们的读者服务：`support@rheinwerk-publishing.com`。

但请注意，关于书籍内容屏幕显示的问题通常不是由电子书文档中的错误引起的。由于几乎每种阅读设备（电脑、平板、智能手机、电子书阅读器）对 EPUB 或 Mobi 文件格式的解析方式不同，不幸的是，无法将电子书文档设置为满足所有使用场景的要求。

此外，并非所有阅读设备都提供相同的文本显示功能，也并非所有功能都能正常工作。最后，作为用户，您也可以通过自己的设置来定义书籍内容在屏幕上的显示方式。

目前设备制造商提供和处理的 EPUB 格式实际上主要适用于纯文本文档的显示，例如小说。一旦技术文本包含图形、表格、脚注、边注或编程代码，就会出现困难。更多信息请参考屏幕显示说明部分以及下一节。

如果推荐的设置均无法满足您的布局要求，我们建议您使用本书的 PDF 版本，该版本可在您的在线图书馆中下载。

## 屏幕显示与导航建议

我们建议使用无衬线字体，例如 Arial 或 Seravek，并在竖屏模式下使用约 30–40%的小字号，横屏模式下使用 20–30%。背景不宜过亮。

请使用连字符选项。如果该功能无法正常工作，请将文本左对齐。否则，请两端对齐。

要在电子书中进行搜索，本书的索引将可靠地引导您找到真正相关的页面。如果索引没有帮助，您可以使用阅读设备的搜索功能。

由于本书在横屏模式下以双页展开形式提供，我们包含的目录可能比您阅读设备的相应功能更能提供书籍内容和结构的概览。为了方便您随时打开目录，它已被作为单独条目包含在设备生成的目录中。

如果您想放大查看图形，请点击该图形一次。再次点击即可返回上一屏幕。如果双击（在 iPad 上），图形将以原始尺寸显示，然后需要放大到所需尺寸。如果单击一次，图形将直接放大并以更高分辨率显示。

对于包含编程代码的书籍，请注意，当字体大小达到一定程度时，代码行可能会被错误换行或显示不完整。如有疑问，请减小字体大小。

## 关于我们及我们的出版计划

网站 [`www.rheinwerk-computing.com`](http://www.rheinwerk-computing.com) 提供了关于我们当前出版计划的详细第一手信息。您也可以在此轻松订购我们所有的书籍和电子书。关于 Rheinwerk Publishing Inc.的信息以及其他联系方式也可在 [`www.rheinwerk-computing.com`](http://www.rheinwerk-computing.com) 找到。

## 法律声明

本节包含本电子书的详细且具有法律约束力的使用条件。

## 版权声明

本出版物整体受版权保护。所有使用和开发权均由作者和 Rheinwerk Publishing 保留；特别是复制权和发行权，无论是印刷形式还是电子形式。

© 2025 Rheinwerk Publishing Inc., Boston (MA)

## 用户权利

您仅有权将本电子书用于个人目的。特别是，您可以出于个人使用目的打印本电子书或复制它，前提是您将此副本存储在仅由您个人使用的设备上。您无权进行任何其他使用或开发。

特别禁止将电子或印刷副本转发给第三方。此外，禁止在互联网、内联网或以任何其他方式分发本电子书或将其提供给第三方。任何公开展示、其他出版或超出个人使用范围的复制行为均明确禁止。上述规定不仅适用于整本电子书，也适用于其部分内容（例如图表、图片、表格、文本段落）。

不得从电子书中删除版权声明、品牌标识和其他法律保留以及数字水印。

## 数字水印

本电子书副本包含一个数字水印，即一个标识，表明谁可以使用此副本。

如果您，亲爱的读者，不是此人，则您正在侵犯版权。因此，请勿使用本电子书，并告知我们此侵权行为。发送一封简短的电子邮件至`info@rheinwerk-publishing.com`即可。谢谢！

## 商标

本出版物中使用的通用名称、商品名称、商品描述等可能未经特别标识即为商标，并受相关法律规定的约束。

本书中提及的所有产品均为其各自公司的注册或未注册商标。

## 责任限制

尽管在创建文本、图形和程序时已尽到谨慎义务，但出版商、作者、编辑或翻译者均不对可能的错误及其后果承担任何法律责任或赔偿责任。

文档存档
