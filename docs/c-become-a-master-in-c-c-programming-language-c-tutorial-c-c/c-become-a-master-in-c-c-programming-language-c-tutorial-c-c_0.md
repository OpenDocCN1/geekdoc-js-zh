# C#：精通C# (C#编程语言, C#教程, C#编码, .NET, Visual Studio, C#运算符, Python, PowerShell, JavaScript)


# 引言

恭喜您下载了《*C#*》一书，感谢您这样做。

接下来的章节将讨论您需要了解的关于 C# 的所有内容。当您读完本书时，您应该能够使用 C# 编写程序，并以该语言应有的水平与计算机进行交互。

C# 将与其他 C 语言类似，但您会意识到存在一些差异，使其成为一种独特的语言。

市面上有很多关于这个主题的书籍，再次感谢您选择这一本！我们已尽一切努力确保本书包含尽可能多的有用信息，请尽情享受阅读！

# 第一章：C# 概述

当您开始使用 C# 时，您会注意到它是一种面向对象的语言，由微软公司创建，并随后获得了 ECMA（欧洲计算机制造商协会）和 ISO（国际标准化组织）的批准。

安德斯·海尔斯伯格开发了这种语言，同时他的团队也在开发与之配套的 .Net 框架。它被设计用于 CLI（公共语言基础结构），这将向您展示可执行的代码以及运行时环境，使您能够在各种平台和架构上使用高级别功能。

使 C# 成为一种广泛使用的语言的一些原因如下：

1.  您可以将其作为 .Net 框架的一部分使用
2.  它是一种通用编程语言
3.  您可以在多种平台上使用它
4.  它是一种面向对象的程序
5.  它将生成高效的程序
6.  它面向组件
7.  该语言结构清晰且易于学习

虽然 C# 可能看起来只是 C 编程语言的另一种变体，但它实际上更像 Java 而非 C，因为它是一种被全球程序员使用的程序。

程序员认为重要的一些特性包括：

1.  可与 Windows 集成
2.  布尔条件
3.  LINQ 和 Lambda 表达式
4.  自动垃圾回收
5.  简化的多线程
6.  标准库
7.  条件编译
8.  程序集变体
9.  索引器
10. 属性和事件
11. 易于使用的泛型
12. 委托和事件管理

# 第二章：C# 的历史

在 .Net 框架开发过程中，类库是使用一种称为“简单托管 C”（Simple Managed C）的系统中的托管代码编译器编写的。直到 1999 年 1 月，海尔斯伯格才组建了一个团队，开发了一种新语言，简称为 Cool，但实际上它是“类似 C 的面向对象语言”（C like Object Oriented Language）。当时微软曾考虑将 Cool 作为该项目的最终名称，但由于版权原因未能实现。

2000 年，在专业开发者大会上，.Net 项目被公之于众，该语言被赋予了新名称 C#，类库被命名为 ASP.Net，而运行时则被移植到了该语言中。

C# 语言的首席设计师同时也是微软的首席架构师，他曾参与创建 Turbo Pascal、Embarcadero Delphi（曾用名 CodeGear Delphi、Inprise Delphi 和 Borland Delphi）的设计，并参与了 Visual J++ 的工作。在采访和撰写的论文中，海尔斯伯格表示，大多数编程语言中存在的缺陷正是推动公共语言运行时基础设计的动力，进而推动了该语言本身的设计。



1994 年，詹姆斯·高斯林创造了 Java 语言，而太阳微系统公司的联合创始人比尔·乔伊表示，C#只是对 Java 语言的模仿。他甚至进一步说：“C#就像是去掉了可靠性、生产力和安全性的 Java。”克雷夫特和朗格回应道：“Java 和 C#几乎是相同的编程语言。无聊的重复，缺乏创新。几乎没有人会声称 Java 或 C#是改变了我们编写程序方式的革命性编程语言。而且，C#从 Java 借鉴了很多，反之亦然。现在 C#支持装箱和拆箱，我们 Java 中也将有非常类似的功能。”

后来在 2000 年，海尔斯伯格站出来说：“C#不是 Java 的克隆，它在设计上更接近 C++。”

自 2005 年版本 2.0 发布以来，C#和 Java 走上了不同的发展轨迹，这使得它们之间的相似性降低。最大的区别之一是泛型被添加到这两种语言中，这使它们彼此不同。C#使用具体化来提供一流的泛型对象，这些对象能够在类加载时生成的代码中被其他类使用。除此之外，C#还具有一些特性，使其成为一种函数式编程语言，可与 C# 3.0 版本发布的 LINQ 扩展一起使用。

以下是 C#每个版本发布时添加的功能。

## 版本 2.0

1. 委托推断
2. 泛型
3. 静态类
4. 分部类
5. 委托的协变和逆变
6. 匿名方法
7. 方法组转换
8. 迭代器
9. Getter/Setter 单独可访问性
10. 可空类型

## 版本 3.0

1. 分部方法
2. 隐式类型局部变量
3. 表达式树
4. 对象和集合初始化器
5. Lambda 表达式
6. 自动实现的属性
7. 查询表达式
8. 匿名类
9. 扩展方法

## 版本 4.0

1. 嵌入式互操作类
2. 动态绑定
3. 泛型协变和逆变
4. 命名参数和可选参数

## 版本 5.0

1. 调用方信息特性
2. 异步方法

## 版本 6.0

1. 字典初始化器
2. 编译器即服务
3. nameof 运算符
4. 将静态类成员导入命名空间
5. 字符串插值
6. 异常筛选器
7. null 传播器
8. 在 catch/finally 块中使用 await
9. 表达式体成员
10. 自动属性初始化器
11. 仅 getter 属性的默认值

## 版本 7.0

1. 表达式体 getter 和 setter
2. out 变量
3. 表达式体构造函数和终结器
4. 模式匹配
5. 通用异步返回类型
6. 元组
7. 引用返回和局部变量
8. 解构
9. 二进制文本
10. 局部函数
11. 数字分隔符

## 版本 7.1

1. 默认表达式
2. 异步 Main 方法

# 第三章

![](img/00001.jpeg)

## C# 环境

.NET 是一个运行在自身平台上的框架，它将帮助你编写 Windows 应用程序、Web 服务和 Web 应用程序。由于该框架设计为几乎可以与任何编程语言一起使用，因此其应用程序将能够在多个平台上运行。每种语言都可以选择访问该框架，以便它们能够相互通信。

.NET 框架附带一个包含大量代码的库，你可以将其与 C# 一起使用。.NET 框架的一些组件包括：

1. LINQ
2. CLR（公共语言运行时）
3. WCF（Windows Communication Foundation）
4. .NET 框架类库
5. Windows Presentation Foundation
6. 公共语言规范
7. WF（Windows Workflow Foundation）
8. 公共类型系统
9. ADO.NET
10. 元数据和程序集
11. ASP.NET 和 ASP.NET AJAX
12. Windows 窗体

每个组件将执行不同的任务，你可以通过使用该组件或查看 Microsoft 提供的文档来了解它们。

### 集成开发环境

除了 C# 之外，你还可以使用更多的开发工具，这些工具包括：

1. Visual Web 创建器
2. VS（Visual Studio 2010）
3. VCE（Visual C# 2010 Express）

Web 创建器和 VCE 可以在 Microsoft 官方网站上找到。使用这些工具时，你将能够编写几乎任何类型的 C# 程序。你还可以选择使用基本文本编辑器（如记事本）编写源代码文件，然后通过命令提示符（它是 .NET 框架的一部分）将代码编译成程序集。

VCE 和 Web 创建器是比 Visual Studio 更小的版本，并且具有与 Visual Studio 相同的外观。

在安装 Visual Studio 的 Express 版本时，你需要有稳定的网络连接。

### 在 Linux 和 Mac 上编写程序

由于 .NET 框架是 Windows 系统软件功能，因此在使用其他系统软件时，你还可以使用其他版本。Mono 是 .NET 框架的一个变体，它可与 C# 编译器一起使用，并能在多种不同的系统软件上运行，例如 Linux 和 Mac OS。

Mono 的整个目的是能够运行为 Microsoft .NET 构建的应用程序，以便它们能够与为其他系统软件（如 Android、iOS、Linux 和 Unix）开发的工具一起工作。

# 第四章

![](img/00001.jpeg)

## C# 的程序结构

在你能够学习构建 C# 程序需要什么之前，你必须先了解该编程语言是如何构建的。

程序中有某些部分对于确保你在创建 C# 程序时添加它们是至关重要的。

1. 注释
2. 命名空间声明
3. 语句和表达式
4. 类
5. Main 方法
6. 类方法
7. 类属性

**示例**

```
using System;

namespace HelloOuterSpaceApplication

{

class HelloOuterSpace

{

static void Main(string[] args)

{

/* 你的第一个 C# 程序 */

Console.WriteLine("Hello outer space");

Console.ReadKey();

}

}

}
```

一旦代码被执行，你将得到结果“Hello outer space”。

程序中的第一行是代码的 `using System` 部分。`using` 关键字用于将系统的命名空间包含到程序中。大多数 C# 程序使用多个 `using` 语句。

你的命名空间声明是你所使用的类的集合。你的应用程序的名称将是该应用程序的类。

你的类声明将包含程序最终要使用的所有数据和定义。类将包含多个方法，这些方法最终将定义类的行为。但是，示例中使用的类只有一个名为 `Main` 的方法。

你的 `Main` 方法是所有 C# 程序的入口点。该方法将指明类何时被执行。

星号和斜杠之间的内容将被编译器忽略，因为它们是程序中的注释。

你的 `Main` 方法将告诉你语句将遵循什么行为。

`WriteLine` 是 `Console` 类在命名空间中拼写时使用的方法。这个语句将导致你的结果显示在你面前的屏幕上。





# 第五章

![](img/00001.jpeg)

## C# 语法

由于 C# 是一种面向对象的编程语言，你将需要使用对象来与其他对象交互，从而创建动作。这些动作在使用时会产生方法。相同的对象将拥有类，或者属于同一个类。

以矩形为例。长度和宽度是矩形的属性。根据矩形的设计，这些属性接受相应的值，同时计算面积并显示详细信息。

**示例：**

```
Using system;

Namespace circle application

{

Class circle

{

// variables

Double width;

Double circumference

Open void accept details ()

{

Width = 3. 4

Circumference = 3.2

}

Open double ()

{

Return width * circumference

}

Open void display ()

{

Console. WriteLine (“width: {0}”, width);

Console. WriteLine (circumference: {0}, circumference);

}

}

Class perform circle

{

Static void main (string [] para)

{

Circle c = new circle ();

C accept details ();

C. display ();

Console. ReadiLine ();

}

}

}
```

对于上面所示的示例，你将得到圆的测量值。

**Using**

在 C# 中，你的第一条语句始终是 `using system;`

关键字 `using` 用于 C# 中的命名空间。

**Class**

当你声明类时，将使用此关键字。

**注释**

当你需要解释所创建的代码时，可以使用注释。C# 编译器会忽略你添加的任何注释。多行注释以 `/*` 开头，以 `*/` 结尾。

单行注释使用一组双斜杠。

**成员变量**

这些变量是类成员的属性。使用时可以存储数据。

**成员函数**

成员函数是执行任务的语句。类的这些函数通常在类内部声明。

**实例化类**

类将在脚本的 `main` 方法中包含类的名称。

**标识符**

标识符是你用来标识类、变量和函数的单词。在 C# 中创建标识符有三条规则。

1. 不能使用 C# 中的关键字。
2. 必须以字母开头，后面可以跟其他字母、数字或下划线。但不能以数字开头。
3. 不能使用任何特殊字符，但下划线除外。

**C# 中的关键字**

关键字是 C# 编译器保留的单词。这些关键字被设置为不能用作标识符。但是，如果你想将这些单词用作标识符，可以在单词前使用 at 符号（`@`），使其在 C# 中有效。

C# 中的标识符在代码中具有特殊含义，因此有些被称为上下文关键字。

**保留关键字**

1. `abstract`
2. `catch`
3. `default`
4. `explicit`
5. `foreach`
6. `interface`
7. `null`
8. `private`
9. `sealed`
10. `switch`
11. `ulong`
12. `volatile`
13. `while`
14. `unchecked`
15. `this`
16. `short`
17. `protected`
18. `object`
19. `internal`
20. `goto`
21. `extern`
22. `delegate`
23. `char`
24. `as`
25. `base`
26. `checked`
27. `do`
28. `false`
29. `if`
30. `is`
31. `operator`
32. `open`
33. `sizeof`
34. `throw`
35. `unsafe`
36. `ushort`
37. `true`
38. `stackalloc`
39. `readonly`
40. `out`
41. `lock`
42. `implicit`
43. `finally`
44. `double`
45. `class`
46. `bool`
47. `break`
48. `const`
49. `else`
50. `fixed`
51. `in`
52. `long`
53. `out`
54. `ref`
55. `static`
56. `try`
57. `using`
58. `virtual`
59. `classof`
60. `string`
61. `return`
62. `override`
63. `namespace`
64. `in`
65. `float`
66. `enum`
67. `continue`
68. `byte`
69. `case`
70. `decimal`
71. `event`
72. `for`
73. `int`
74. `new`
75. `params`
76. `sbyte`
77. `struct`
78. `uint`
79. `void`

**上下文关键字**

1. `partial`
2. `get`
3. `from`
4. `orderby`
5. `let`
6. `dynamic`
7. `set`
8. `join`
9. `descending`
10. `ascending`
11. `into`
12. `select`
13. `remove`
14. `group`
15. `alias`
16. `partial`
17. `global`
18. `add`

# 第六章

![](img/00001.jpeg)

## 数据类型

C# 中有三种不同的数据类型。

1. 指针类型
2. 值类型
3. 引用类型

### 值类型

值类型是直接赋值的变量。它们派生自 `System.ValueType`。

值类型直接包含数据，例如 `char`、`int` 和 `float`。当声明 `int` 类型时，系统会为其分配空间。

**值类型：**

1. `bool`：布尔值
2. `byte`：8 位无符号整数
3. `char`：16 位 Unicode 字符
4. `decimal`：128 位精确十进制值，最多 29 个有效数字
5. `double`：64 位双精度浮点类型
6. `float`：32 位单精度浮点类型
7. `int`：32 位有符号整数
8. `long`：64 位有符号整数
9. `sbyte`：8 位有符号整数
10. `short`：16 位有符号整数
11. `uint`：32 位无符号整数
12. `ulong`：64 位无符号整数
13. `ushort`：16 位无符号整数

变量的确切大小取决于所使用的平台，可以通过 `sizeof` 方法获知。该表达式将返回对象存储空间的大小（以字节为单位）。

**语法**

```
Using system;

Namespace dataclass application

{

Class program

{

Static void main (string [] args)

{

Console. Write line (size of int: {0}, Sizeof (int));

Console. ReadiLine ()

}

}

}
```

### 引用类型




你实际上不会在引用类变量中存储任何数据。基本上，你只是引用程序内存中的一个位置。当你使用多个变量时，引用类将指向这些类所在的位置。如果该位置的数据被某个变量修改，那么另一个变量将自动反映这一变化。

### 对象类

该类将成为你在 C# 中遇到的所有数据类的基类。CTS（通用类型系统）在使用该系统时会使用别名 `Object` 类。只要该类由程序预定义或由用户定义，这个 `Object` 类就可以被赋值为本章将要讨论的其他类的值。在你可以赋值之前，需要先进行转换。

当 `Object` 类被转换时，这一过程称为装箱（boxing）；而当它被转换为值类型时，则称为拆箱（unboxing）。

### 动态类型

任何类的任何值都可以存储在 `dynamic` 类中。你需要在运行时检查这些变量类，因为它们的类型检查发生在运行时。`dynamic` 类与 `object` 类类似，但 `object` 类的类型检查发生在编译时。

**语法**

```
Dynamic <variable_name> = value;
```

### 字符串类

该类允许你将任何字符串值赋给任何变量。`string` 类在系统中包含一个别名 `String` 类。该类也派生自 `object` 类。你会注意到，`string` 类的值是通过字符串字面量来赋值的，字符串字面量有两种形式：带引号的和 @ 引号的。

用户定义的引用类被称为 `interface`、`delegate` 和 `class`。

### 指针类

指针变量将存储其他类的内存地址。这些指针具有与其他 C 语言中指针相同的功能。

**语法**

```
Class * identifier;
```

# 第七章

![](img/00001.jpeg)

## C# 中的类型转换

C# 类型转换是将一种数据类型转换为另一种数据类型的行为。你可能也听说过这种转换称为类型强制转换。你会发现有两种不同的转换类型。

1. 隐式转换：在此类转换下，C# 会以与正在转换的类相同的方式执行转换。例如，当转换从最小到最大时，会使派生类转换为基类。

2. 显式转换：显式转换由用户在使用预定义函数时完成。这些转换需要强制转换运算符。

**语法**

```
using System;

namespace TypeClassConversionApplication
{
    class ExplicitConversion
    {
        static void Main(string[] args)
        {
            double d = 5673.74;
            int i;

            // cast double to int.
            i = (int)d;

            Console.WriteLine(i);
            Console.ReadKey();
        }
    }
}
```

### 转换方法

1. `ToBoolean`：将转换为布尔类
2. `ToByte`：将转换为字节
3. `ToChar`：将转换为单个 Unicode 字符中的字符
4. `ToDateTime`：将转换你的日期和时间结构
5. `ToDecimal`：将浮点数或整数转换为十进制类
6. `ToDouble`：将类转换为双精度类
7. `ToInt16`：将类转换为 16 位整数
8. `ToInt32`：将类转换为 32 位整数
9. `ToInt64`：将类转换为 64 位整数
10. `ToSByte`：将你的类转换为有符号字节类
11. `ToSingle`：将类转换为浮点数，但数值较小
12. `ToString`：将你的类转换为字符串
13. `ToType`：将你的类转换为指定的类
14. `ToUInt16`：你将得到一个无符号整数类
15. `ToUInt32`：你将得到一个无符号长整型类
16. `ToUInt64`：你将得到一个无符号大整数

**示例：**

```
using System;

namespace ClassConversionApplication
{
    class StringConversion
    {
        static void Main(string[] args)
        {
            int i = 75;
            float f = 53.005f;
            double d = 2345.7652;
            bool b = true;

            Console.WriteLine(i.ToString());
            Console.WriteLine(f.ToString());
            Console.WriteLine(d.ToString());
            Console.WriteLine(b.ToString());

            Console.ReadKey();
        }
    }
}
```

# 第八章

![](img/00001.jpeg)

## C# 中的变量

变量本质上只是存储区域中的一个名称，用于操作数据。每个变量都包含特定的类，该类决定了变量内存的大小和布局。每个内存区域都有一系列可以存储的值，以及一组可以应用于每个变量的操作。

C# 提供的一些基本值类型包括：

1. 整型类：`char`、`ulong`、`long`、`uint`、`int`、`ushort`、`short`、`byte`、`sbyte`
2. 浮点型：`double` 和 `float`
3. 十进制类：`decimal`
4. 布尔型：`true`、`false`、赋值
5. 可空类型：`Nullable`

C# 允许你使用 `class` 和 `enum` 等变量来定义值类型。

### 定义变量

**语法**

```
<data_class> <variable_lists>;
```

数据类型必须是有效的 C# 数据类型。变量列表必须至少包含一个标识符，多个标识符之间用逗号分隔。

**变量定义：**

```
int i, j, k;
char c, ch;
float f, salary;
double d;
```

**初始化变量**

初始化变量时，需要有一个等号，后面跟着一个常量表达式。

**语法**

```
variable_name = value;
```

你可以在声明变量的同时进行初始化。初始化器由一个等号和后面的常量表达式组成。

**语法**

```
<data_class> <variable_name> = value;
```

**示例**

```
int d = 3, f = 5; /* 初始化 d 和 f。 */
byte z = 22; /* 初始化 z。 */
double pi = 3.14159; /* 声明 pi 的近似值。 */
char x = 'x'; /* 变量 x 的值为 'x'。 */
```

你需要以正确的方式初始化变量，否则程序会给出你意想不到的结果。

**示例**

```
using System;

namespace VariableDefinition
{
    class Program
    {
        static void Main(string[] args)
        {
            short a;
            int b ;
            double c;

            /* 实际初始化 */
            a = 10;
            b = 20;
            c = a + b;

            Console.WriteLine("a = {0}, b = {1}, c = {2}", a, b, c);
            Console.ReadLine();
        }
    }
}
```

**接受用户输入**

你的 `Console` 类位于 `System` 命名空间中，它提供了一个名为 `ReadLine()` 的函数，用于接受用户输入并将其存储为变量。

**示例**

```
int num;
num = Convert.ToInt32(Console.ReadLine());
```

你的 `Convert.ToInt32()` 函数会获取数据并将其转换，以便程序能够读取。

### 左值和右值表达式

在 C# 中，你会遇到两种不同的表达式：

1. 右值：该表达式出现在赋值操作的右侧，而不是左侧。
2. 左值：该表达式可以出现在赋值操作的左侧或右侧。

左值变量可以出现在赋值操作的左侧。数值字面量是右值，这就是为什么它们不能被赋值，因此不能出现在赋值操作的左侧。

# 第九章

![](img/00001.jpeg)

## C# 常量和字面量





你的常量将指向一个固定值，在程序执行代码期间该值无法更改。这些固定值被称为字面量。常量可以是任何数据类型，例如整数或字符。你也可以使用枚举常量。

除了值在定义后无法更改之外，你可以像对待普通变量一样对待常量。

### 整数字面量

整数字面量可以是十进制或十六进制等形式。前缀会告诉你基数或进制。当使用十六进制时，前缀是 `0x` 或 `0X`，但十进制没有前缀标识。

整数字面量还可以使用 `U` 和 `L` 作为后缀，分别表示无符号和长整型。后缀可以是大写或小写，具体取决于顺序。

**示例**

```
85 /* 十进制 */
0x4b /* 十六进制 */
30 /* int */
30u /* unsigned int */
30l /* long */
30ul /* unsigned long */
```

### 浮点字面量

浮点字面量由四部分组成：指数、小数部分、整数部分、小数点。你也可以用指数形式或十进制形式来表示这些字面量。

**示例**

```
3.14159 /* 合法 */
314159E-5F /* 合法 */
510E /* 非法：指数不完整 */
210f /* 非法：没有小数或指数 */
.e55 /* 非法：缺少整数或小数部分 */
```

使用十进制形式时，需要确保包含小数点、指数或两者都包含。对于指数形式，你需要包含整数部分、小数部分，或者如果你愿意，可以两者都包含。对于有符号指数，使用 `e` 或 `E`。

### 字符常量

字符字面量由一组单引号包围，并存储在 `char` 类型中。这些字面量可以是普通字符，甚至是转义序列，你甚至可能看到一些通用字符。

在 C# 中使用的一些字符前面会带有反斜杠，这意味着它们具有特殊含义，并且会以不同的方式表示。

转义序列如下：

1. `\xhh`：十六进制，多位数字
2. `\\`：`\` 字符
3. `\v`：垂直制表符
4. `\'`：`'` 字符
5. `\t`：水平制表符
6. `\"`：`"` 字符
7. `\r`：回车
8. `\?`：`?` 字符
9. `\n`：换行
10. `\a`：警报
11. `\f`：换页
12. `\b`：退格

**示例**

```
using System;

namespace EscapeChar
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello\tWorld\n\n");
            Console.ReadLine();
        }
    }
}
```

### 字符串字面量

字符串字面量或常量由双引号包围，或者包含 at 符号（`@`）。这些字符串包含一系列字符，看起来与字符字面量类似。

长行可以通过使用字符串字面量拆分为多行，只要使用空白字符进行分隔即可。

**示例**

```
"hello, dear"
"hello, \
dear"
"hello, " "d" "ear"
@"hello dear"
```

### 定义常量

常量通过使用 `const` 关键字来定义。

**语法**

```
const <数据类型> <常量名> = 值;
```

**示例**

```
using System;

namespace DeclaringConstants
{
    class Program
    {
        static void Main(string[] args)
        {
            const double pi = 3.14159;
            // 常量声明
            double r;
            Console.WriteLine("Enter Radius: ");
            r = Convert.ToDouble(Console.ReadLine());
            double areaCircle = pi * r * r;
            Console.WriteLine("Radius: {0}, Area: {1}", r, areaCircle);
            Console.ReadLine();
        }
    }
}
```

# 第十章

![](img/00001.jpeg)

## C# 运算符

运算符是告诉编译器在数学或逻辑表达式中执行何种操作的符号。C# 内置了多种运算符，例如：

1. 杂项
2. 算术
3. 赋值
4. 关系
5. 位运算
6. 逻辑

### 算术运算符

1. 加法（`+`）
2. 减法（`-`）
3. 乘法（`*`）
4. 除法（`/`）
5. 取模（`%`）
6. 自增（`++`）
7. 自减（`--`）

### 关系运算符

1. 值是否相等？（`==`）
2. 值是否不相等（`!=`）
3. 大于（`>`）
4. 小于（`<`）
5. 大于等于（`>=`）
6. 小于等于（`<=`）

### 逻辑运算符

1. 逻辑与（`&&`）
2. 逻辑或（`||`）
3. 逻辑非（`!`）

### 位运算符

1. 按位与（`&`）
2. 按位或（`|`）
3. 按位异或（`^`）
4. 按位取反（`~`）
5. 左移（`<<`）
6. 右移（`>>`）

### 赋值运算符

1. 赋值（`=`）
2. 加后赋值（`+=`）
3. 减后赋值（`-=`）
4. 乘后赋值（`*=`）
5. 除后赋值（`/=`）
6. 取模后赋值（`%=`）
7. 左移后赋值（`<<=`）
8. 右移后赋值（`>>=`）
9. 按位与后赋值（`&=`）
10. 按位异或后赋值（`^=`）
11. 按位或后赋值（`|=`）

### 杂项运算符

1. `sizeof()`
2. `classof()`
3. 变量地址（`&`）
4. 指向变量的指针（`*`）
5. 条件表达式（`? :`）
6. 对象类型判断（`is`）
7. 若转换失败则不引发异常（`as`）

### 运算符优先级

C# 中的优先级告诉你哪一组项会先被求值。某些运算符的优先级高于其他运算符，例如乘法的优先级高于加法。

以下是 C# 的优先级顺序：

1. 后缀：`()`、`[]`、`.`、`++`、`--`
2. 一元：`+`、`-`、`!`、`~`、`++`、`--`、`(类型)*`、`&`、`sizeof`
3. 乘法：`*`、`/`、`%`
4. 加法：`+`、`-`
5. 移位：`<<`、`>>`
6. 关系：`<`、`<=`、`>`、`>=`
7. 相等：`==`、`!=`
8. 按位与：`&`
9. 按位异或：`^`
10. 按位或：`|`
11. 逻辑与：`&&`
12. 逻辑或：`||`
13. 条件：`?:`
14. 赋值：`=`、`+=`、`-=`、`^=`、`/=`、`%=`、`=>`、`>=`、`<<=`、`&=`、`^=`、`|=`
15. 逗号：`,`

# 第十一章

![](img/00001.jpeg)

## C# 中的决策

你将使用 C# 中的决策来了解程序如何工作。决策结构意味着你需要告诉程序需要评估和测试哪个条件，以及在条件为真或假时需要执行的任何语句。

### 决策语句

1. `if` 语句：包含一个布尔表达式
2. `if-else` 语句：一个 `if` 语句后跟一个 `else` 语句
3. 嵌套语句：一个语句嵌套在另一个语句内部
4. `switch` 语句：该语句允许对变量进行相等性测试
5. 嵌套 `switch` 语句：一个 `switch` 语句放在另一个 `switch` 语句内部

**`? :` 运算符**

该运算符可用于替代 `if-else` 语句。

**语法**

```
表达式 1 ? 表达式 2 : 表达式 3 ;
```

该表达式的值取决于 `表达式 1` 的求值结果：如果为真，则 `表达式 2` 被求值并成为问号的值；但如果 `表达式 1` 为假，则 `表达式 3` 被求值并成为该表达式的值。

# 第十二章

![](img/00001.jpeg)

## 循环

在某些情况下，你会发现需要连续多次执行特定的代码块。语句将按照编写的顺序执行。

大多数编程语言都会提供控制结构，使你能够处理更复杂的执行路径。循环允许语句连续多次执行，而无需反复调用需要执行的语句。

1. `while` 循环：如果条件为真，则重复执行所选语句。
2. `for` 循环：语句会被执行并简化，以便管理循环变量。





### 3. do while 循环：条件将在循环体的末尾进行测试。

### 4. 嵌套循环：就像其他嵌套语句一样，这是一个循环嵌套在另一个循环内部。

### 循环控制语句

控制语句将改变循环的正常执行方式。每当执行离开作用域时，任何自动对象都将被销毁。

1. `Break` 语句：循环或 `switch` 语句将被终止，同时执行循环或 `switch` 之后的语句。

2. `Continue` 语句：循环将跳过其所有主体，并在再次迭代之前测试条件。

### 无限循环

当循环的条件永远不会被判定为假时，循环就属于这一类。`for` 循环通常是属于这一类的循环。由于三个表达式都不是必需的，你可以通过将条件表达式留空来造成无限循环。

**示例**

```csharp
using System;

namespace Loops

{

class Program

{

static void Main(string[] args)

{

for (; ; )

{

Console. WriteLine("Hey! I am Trapped");

}

}

}

}
```

当条件表达式不存在时，它将被假定为真。你可能需要初始化增量表达式。然而，许多程序员使用 `for ( ; ; )` 来构造无限循环。

# 第十三章

![](img/00001.jpeg)

## C# 中的封装

你可以将封装定义为将一个或多个项目封装在逻辑或物理包中的过程。封装是在面向对象的编程语言中完成的，这种方法最终会阻止对实现细节的访问。

抽象和封装是你只能在面向对象编程中找到的特性。然而，抽象将代码中的相关信息转化为代码的可见部分，而封装则允许程序员在代码中实现他们想要的抽象级别。

有一些访问说明符可以实现封装。访问说明符将定义作用域以及类成员的可见性。以下是 C# 支持的说明符。

1. `Protected internal`

2. `Open`

3. `Internal`

4. `Private`

5. `Protected`

### OPEN

这些说明符将使类能够展示其成员变量和函数，以便其他对象和函数可以看到它们。当一个成员是 `Open` 时，它可以从外部访问。

**示例**

```csharp
using System;

namespace RectangleApplication

{

class Rectangle

{

//member variables

Open double length;

Open double width;

Open double GetArea()

{

return length * width;

}

Open void Display()

{

Console. WriteLine("Length: {0}", length);

Console. WriteLine("Width: {0}", width);

Console. WriteLine("Area: {0}", GetArea());

}

}//end class Rectangle

class PerformRectangle

{

static void Main(string[] args)

{

Rectangle r = new Rectangle();

r.length = 4.5;

r.width = 3.5;

r.Display();

Console.ReadLine();

}

}

}
```

在这个示例中，你可以看到成员变量 `length` 和 `width` 是 `Open` 的，因此可以通过使用类名从你的函数中访问它们。你的成员函数只能直接访问变量，而不需要使用任何类实例。它们也通过使用 `main()` 函数被声明为 `Open`。

### PRIVATE

`Private` 说明符将使类能够隐藏其成员变量和函数，使其不被代码中的其他内容访问。只有在同一个类中的函数才能访问私有成员。甚至会出现类无法访问私有成员的情况。

**示例**

```csharp
using System;

namespace RectangleApplication

{

class Rectangle

{

//member variables

private double length;

private double width;

Open void Acceptdetails()

{

Console. WriteLine("Enter Length: ");

length = Convert.ToDouble(Console.ReadLine());

Console. WriteLine("Enter Width: ");

width = Convert.ToDouble(Console.ReadLine());

}

Open double GetArea()

{

return length * width;

}

Open void Display()

{

Console. WriteLine("Length: {0}", length);

Console. WriteLine("Width: {0}", width);

Console. WriteLine("Area: {0}", GetArea());

}

}//end class Rectangle

class PerformRectangle

{

static void Main(string[] args)

{

Rectangle r = new Rectangle();

r.Acceptdetails();

r.Display();

Console.ReadLine();

}

}

}
```

在上面的示例中，成员变量被声明为私有，因此函数无法访问它们。然而，成员函数会显示这些变量。由于成员函数是开放的，因此可以通过使用类名的实例从主函数中访问它们。

### 受保护的访问说明符

该说明符将允许子类访问其基类中的成员变量和函数。这在处理继承时非常有用。

### 内部访问说明符

`internal` 访问说明符将允许成员函数和变量暴露给你正在处理的程序集中的其他函数和对象。因此，只要成员定义所在的应用程序中定义了任何类或方法，你就可以访问它们。

**示例**

```csharp
using System;

namespace RectangleApplication

{

class Rectangle

{

//member variables

internal double length;

internal double width;

double GetArea()

{

return length * width;

}

Open void Display()

{

Console. WriteLine("Length: {0}", length);

Console. WriteLine("Width: {0}", width);

Console. WriteLine("Area: {0}", GetArea());

}

}//end class Rectangle

class PerformRectangle

{

static void Main(string[] args)

{

Rectangle r = new Rectangle();

r.length = 4.5;

r.width = 3.5;

r.Display();

Console.ReadLine();

}

}

}
```

这个示例表明，成员函数没有用提供访问权限的说明符声明。因此，类成员的默认访问说明符没有被提及，因为它实际上是私有的。

### 受保护的内部访问说明符

该说明符将隐藏类的成员变量和函数，使其不被其他类对象和函数访问，但同一应用程序中的子类除外。你将在实现继承时使用此方法。

# 第十四章

![](img/00001.jpeg)

## C# 中使用的方法

方法是用于执行任务的一组语句。C# 中的每个程序都有一个名为 `main` 的类方法。

要使用一个方法，你必须：

1. 定义你的方法

2. 调用你的方法

### 定义方法

每当定义一个方法时，你必须声明结构的元素。

**语法**

```csharp
<access specifier> <return class> <method name> (parameter list)

{

Method body

}
```

方法的一些元素包括：

1. 访问说明符：变量的可见性将由另一个类决定。

2. 返回类：该方法将返回一个值。这个返回类将是返回给你的值的数据类。如果方法不返回值，那么返回类将是 `void`。

3. 方法名：方法名是区分大小写的标识符。它不会与类中声明的其他标识符相同。

4. 参数列表：在括号之间，参数将用于向正在使用的方法传递和获取数据。参数指的是方法所使用的参数的顺序、数量和类。参数不是必须使用的。





5. 方法体：你的指令将放在这里，你需要这些指令来完成需要执行的步骤。

**示例**

```csharp
class NumberManipulator
{
   Open int FindMax(int num1, int num2)
   {
      /* 局部变量声明 */
      int result;

      if (num1 > num2)
         result = num1;
      else
         result = num2;
      return result;
   }
   ...
}
```

### 调用方法

通过使用你想要调用的方法名称来调用方法。

**示例**

```csharp
using System;

namespace CalculatorApplication
{
   class NumberManipulator
   {
      Open int FindMax(int num1, int num2)
      {
         /* 局部变量声明 */
         int result;

         if (num1 > num2)
            result = num1;
         else
            result = num2;
         return result;
      }

      static void Main(string[] args)
      {
         /* 局部变量定义 */
         int a = 100;
         int b = 200;
         int ret;

         NumberManipulator n = new NumberManipulator();

         // 调用 FindMax 方法
         ret = n.FindMax(a, b);
         Console.WriteLine("最大值是：{0}", ret );
         Console.ReadLine();
      }
   }
}
```

你也可以选择从其他类中调用 Open 方法，这些方法将在该类的实例中使用。

**示例**

```csharp
using System;

namespace CalculatorApplication
{
   class NumberManipulator
   {
      Open int FindMax(int num1, int num2)
      {
         /* 局部变量声明 */
         int result;

         if(num1 > num2)
            result = num1;
         else
            result = num2;
         return result;
      }
   }

   class Test
   {
      static void Main(string[] args)
      {
         /* 局部变量定义 */
         int a = 100;
         int b = 200;
         int ret;

         NumberManipulator n = new NumberManipulator();

         // 调用 FindMax 方法
         ret = n.FindMax(a, b);
         Console.WriteLine("最大值是：{0}", ret );
         Console.ReadLine();
      }
   }
}
```

### 递归方法调用

这种方法是对自身的调用，被称为递归。

**示例**

```csharp
using System;

namespace CalculatorApplication
{
   class NumberManipulator
   {
      Open int factorial(int num)
      {
         /* 局部变量声明 */
         int result;

         if (num == 1)
         {
            return 1;
         }
         else
         {
            result = factorial(num - 1) * num;
            return result;
         }
      }

      static void Main(string[] args)
      {
         NumberManipulator n = new NumberManipulator();

         // 调用 factorial 方法
         Console.WriteLine("6 的阶乘是：{0}", n.factorial(6));
         Console.WriteLine("7 的阶乘是：{0}", n.factorial(7));
         Console.WriteLine("8 的阶乘是：{0}", n.factorial(8));
         Console.ReadLine();
      }
   }
}
```

### 向方法传递参数

每当调用参数时，你必须将参数传递给方法。至少有以下三种方式可以传递参数。

1. 值参数：值参数会将实参的值复制到函数的形参中。这样做之后，对参数所做的任何更改都不会影响实参。

2. 引用参数：你的引用将被复制到实参的内存位置，并传递给形参。这最终意味着你对参数所做的更改将影响实参。

3. 输出参数：你将获得多个返回值。

# 第十五章

![](img/00001.jpeg)

## C# 中的可空类型

可空类型是一种特殊的数据类型，它可以将正常范围的值赋为 null。

你可以存储从 -2,147,483,648 到 2,147,483,647 的任何值，或者 null。你也可以分配具有 true、false 或 null 输出的值。

**语法**

`<数据类型> ? <变量名> = null;`

**示例**

```csharp
using System;

namespace CalculatorApplication
{
   class NullablesAtShow
   {
      static void Main(string[] args)
      {
         int? num1 = null;
         int? num2 = 45;
         double? num3 = new double?();
         double? num4 = 3.14157;
         bool? boolval = new bool?();

         // 显示值
         Console.WriteLine("可空类型显示：{0}, {1}, {2}, {3}", num1, num2, num3, num4);
         Console.WriteLine("可空布尔值：{0}", boolval);
         Console.ReadLine();
      }
   }
}
```

### 空合并运算符（??）

当使用可空值类型和引用类型时，会用到空合并运算符。你将使用空合并运算符将一个操作数转换为另一个可空值类型操作数的类型，前提是这种转换是可行的。

如果你的第一个操作数的值为 null，那么当运算符返回第二个操作数的值时，它将返回第一个操作数的值。

**示例**

```csharp
using System;

namespace CalculatorApplication
{
   class NullablesAtShow
   {
      static void Main(string[] args)
      {
         double? num1 = null;
         double? num2 = 3.14157;
         double num3;

         num3 = num1 ?? 5.34;
         Console.WriteLine("num3 的值：{0}", num3);

         num3 = num2 ?? 5.34;
         Console.WriteLine("num3 的值：{0}", num3);

         Console.ReadLine();
      }
   }
}
```

# 第十六章

![](img/00001.jpeg)

## C# 中的数组

数组用于存储固定大小的顺序集合，这些集合由对象或数据类型组成。数组可用于存储一组数据，这些数据作为数组比作为其他数据类型更有用。它还使得数据存储在连续的内存位置中。

与其声明单个变量，不如将数组中的一个变量声明为数字，并使用方括号来表示单个变量。你的变量将有一个索引位置，在尝试访问该元素时将使用该索引。

数组由连续的内存位置组成，其中最低地址对应第一个元素。

### 声明数组

**语法**

`数据类型 [] 数组名;`

1. 数据类型告诉你数组中元素的类型。

2. 方括号告诉你数组的秩。秩将告诉你数组的大小。

3. 数组名显然告诉你正在处理的数组的名称。

**示例**

`double [ ] hello ;`

### 初始化数组

声明数组时，你不会在程序的内存中初始化数组。当数组变量被初始化时，你可以为数组赋值。

数组被称为引用类型，这意味着你需要使用 `new` 关键字来创建将在数组中发生的实例。

**示例：**

`double [ ] hello = new double [ 39 ]`

### 为数组赋值

可以通过使用索引号为单个数组元素赋值。你也可以在声明时分配需要分配给数组的值。还可以选择手动创建和初始化数组。

另一种为数组赋值的方法是省略数组的大小。或者，你可以将数组中的变量复制到另一个目标数组变量中。这样做时，目标和源指针将位于内存中的同一位置。

创建数组时，C# 编译器会将数组的每个元素初始化为一个默认值，该值基于你正在处理的数组类型。

### 访问数组元素

元素将通过索引访问。你将通过将元素的索引放在数组名称后面的一组方括号内来实现这一点。

**示例：**

```csharp
using System;

namespace ArrayApplication
{
   class MyArray
   {
      static void Main(string[] args)
      {
         int [] n = new int[10]; /* n 是一个包含 10 个整数的数组 */
         int i,j;

         /* 初始化数组 n 的元素 */
         for ( i = 0; i < 10; i++ )
         {
            n[ i ] = i + 100;
         }

         /* 输出每个数组元素的值 */
         for (j = 0; j < 10; j++ )
         {
            Console.WriteLine("元素[{0}] = {1}", j, n[j]);
         }
         Console.ReadKey();
      }
   }
}
```

### For Each 循环

For Each 语句用于遍历数组。

**示例**

```csharp
using System;

namespace ArrayApplication
{
   class MyArray
   {
      static void Main(string[] args)
      {
```





```csharp
int [] n = new int[10]; /* n 是一个包含 10 个整数的数组 */

/* 初始化数组 n 的元素 */

for ( int i = 0; i < 10; i++ )
{
    n[i] = i + 100;
}

/* 输出每个数组元素的值 */

foreach (int j in n )
{
    int i = j-100;
    Console. WriteLine("Element[{0}] = {1}", i, j);
}

Console.ReadKey();
}
}
}
```

### 数组

1. 多维数组
2. 交错数组
3. 将数组传递给函数
4. 参数数组
5. 数组类

# 第十七章

![](img/00001.jpeg)

## C# 中的字符串

使用 C#，你可以将字符串当作数组来使用。但更常见的做法是使用 `string` 关键字来声明字符串变量。`string` 关键字是 `System.String` 的别名。

### 创建字符串对象

可以通过以下方式创建字符串对象：

1. 调用格式化方法，将值或对象转换为字符串表示形式
2. 将字符串字面量赋值给字符串变量，或检索返回字符串的属性/方法
3. 使用字符串类构造函数
4. 使用字符串连接运算符

#### 示例

```csharp
using System;

namespace StringApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            // 通过字符串字面量和字符串连接
            string fname, lname;
            fname = "Rowan";
            lname = "Atkinson";
            string fullname = fname + lname;
            Console. WriteLine("Full Name: {0}", fullname);

            // 通过字符串构造函数
            char[] letters = { 'H', 'e', 'l', 'l','o' };
            string greetings = new string(letters);
            Console. WriteLine("Greetings: {0}", greetings);

            // 返回字符串的方法
            string[] sarray = { "Hello", "From", "Tutorials", "Point" };
            string message = String.Join(" ", sarray);
            Console. WriteLine("Message: {0}", message);

            // 格式化方法转换值
            DateTime waiting = new DateTime(2012, 10, 10, 17, 58, 1);
            string chat = String.Format("Message sent at {0:t} on {0:D}", waiting);
            Console. WriteLine("Message: {0}", chat);
        }
    }
}
```

### 字符串类的属性

1. `Chars`：获取字符串对象中指定位置的字符对象
2. `Length`：字符串对象中的字符数

### 字符串类的方法

字符串类有许多方法，可以帮助你更轻松地处理字符串对象。

1. `Open static int compare (string strA, string strB)`
2. `Open static int compare (string strA, string strB, bool ignoreCase )`
3. `Open static string concat (string str0, string str 1)`
4. `Open static string concat( string str0, string str1, string str 2)`
5. `Open static string concat (string str0,string str1, string str2, string str 3)`
6. `Open bool contains (string value)`
7. `Open static string copy (string str)`
8. `Open void copyto (int sourceindex, char [] destination, int destinationindex, int count)`
9. `Open bool endswith (string value)`
10. `Open bool equals (string value)`
11. `Open static bool equals (string a, string b)`
12. `Open static string format (string format, object arg 0)`
13. `Open int index of (char value)`
14. `Open int index of (string value)`
15. `Open int indexof (char value, int startindex)`
16. `Open int indexof (string value, int start index)`
17. `Open int indexof any (char [] anyof)`
18. `Open int index of any (char [] anyof, int start index)`
19. `Open string insert (int startindex, string value)`
20. `Open static bool is null or empty (string value)`
21. `Open static string join (string separator, params string [] value)`
22. `Open static string join (string, string [] value, int start index, int count)`
23. `Open int last index of (char value)`
24. `Open int last index of (string value)`
25. `Open string remove (int start index)`
26. `Open string remove (int start index, int count)`
27. `Open string replace (char old char, cha new char)`
28. `Open string replace (string old value, string new value)`
29. `Open string [] split (params char [] separator)`
30. `Open string [] split (char [] separator, int count)`
31. `Open bool starts with (string value)`
32. `Open char [] to char array ()`
33. `Open char [] to char array (int start index, int length)`
34. `Open string to lower ()`
35. `Open string to upper ()`
36. `Open string trim ()`

#### 示例

```csharp
using System;

namespace StringApplication
{
    class StringProg
    {
        static void Main(string[] args)
        {
            string str1 = "This is test";
            string str2 = "This is text";

            if (String.Compare(str1, str2) == 0)
            {
                Console. WriteLine(str1 + " and " + str2 + " are equal.");
            }
            else
            {
                Console. WriteLine(str1 + " and " + str2 + " are not equal.");
            }

            Console.ReadKey() ;
        }
    }
}
```

#### 字符串包含子串示例

```csharp
using System;

namespace StringApplication
{
    class StringProg
    {
        static void Main(string[] args)
        {
            string str = "This is test";

            if (str.Contains("test"))
            {
                Console. WriteLine("The sequence 'test' was found.");
            }

            Console.ReadKey() ;
        }
    }
}
```

#### 获取子字符串示例

```csharp
using System;

namespace StringApplication
{
    class StringProg
    {
        static void Main(string[] args)
        {
            string str = "Last night I dreamt of San Pedro";
            Console. WriteLine(str);
            string substr = str.Substring(23);
            Console. WriteLine(substr);
        }
    }
}
```

#### 连接字符串示例

```csharp
using System;

namespace StringApplication
{
    class StringProg
    {
        static void Main(string[] args)
        {
            string[] starray = new string[]{"Down the way nights are dark",
                "And the sun shines daily on the mountain top",
                "I took a trip on a sailing ship",
                "And when I reached Jamaica",
                "I made a stop"};
            string str = String.Join("\n", starray);
            Console. WriteLine(str);
        }
    }
}
```

# 第十八章

![](img/00001.jpeg)

## C# 结构体

在 C# 中，数据类有值类型，它们可以帮助你创建单个变量来保存与该数据类相关的任何数据。`struct` 关键字用于创建结构体。

结构体用于表示记录。

### 定义结构体

要定义结构体，你需要使用 `struct` 语句。该语句用于在程序中定义包含多个成员的新数据类。

#### 示例

```csharp
using System;

struct Books
{
    Open string title;
    Open string author;
    Open string subject;
    Open int book_id;
};

Open class testStructure
{
    Open static void Main(string[] args)
    {
        Books Book1; /* 声明 Book1 为 Books 类型 */
        Books Book2; /* 声明 Book2 为 Books 类型 */

        /* book 1 规格 */
        Book1.title = "C Programming";
        Book1.author = "Nuha Ali";
        Book1.subject = "C Programming Tutorial";
        Book1.book_id = 6495407;

        /* book 2 规格 */
        Book2.title = "Telecom Billing";
        Book2.author = "Zara Ali";
        Book2.subject = "Telecom Billing Tutorial";
        Book2.book_id = 6495700;

        /* 打印 Book1 信息 */
        Console. WriteLine( "Book 1 title : {0}", Book1.title);
        Console. WriteLine("Book 1 author : {0}", Book1.author);
        Console. WriteLine("Book 1 subject : {0}", Book1.subject);
        Console. WriteLine("Book 1 book_id :{0}", Book1.book_id);

        /* 打印 Book2 信息 */
        Console. WriteLine("Book 2 title : {0}", Book2.title);
        Console. WriteLine("Book 2 author : {0}", Book2.author);
        Console. WriteLine("Book 2 subject : {0}", Book2.subject);
        Console. WriteLine("Book 2 book_id : {0}", Book2.book_id);

        Console.ReadKey();
    }
}
```

### C# 结构体的特性

既然你已经有了上面示例中创建的结构体，你会意识到它们与其他 C 编程语言中的结构体不同。C# 为其结构体提供了以下特性：

1. 结构体可以包含方法、字段、属性、事件、运算符方法和索引器。
2. 结构体可以包含构造函数，但不能包含析构函数。
3. 禁止继承。
4. 不能将结构体用作任何其他结构体或类的基类。
5. 结构体至少要实现一个接口。





6. 结构成员不允许被指定为 `protected`、`virtual` 或 `abstract`。

7. 每当使用 `new` 运算符创建结构对象时，你将创建该对象及其对应的构造函数。

8. 如果未使用 `new` 运算符，则在字段初始化之前，该字段将保持未赋值状态。

### 类与结构

在 C# 中，结构与类之间至少存在三个区别：

1. 结构不允许拥有默认构造函数。
2. 类使用引用类型，而结构使用值类型。
3. 结构不能使用继承。

**示例**

```csharp
using System;

struct Books
{
    private string title;
    private string author;
    private string subject;
    private int book_id;

    Open void getValues(string t, string a, string s, int id)
    {
        title = t;
        author = a;
        subject = s;
        book_id = id;
    }

    Open void display()
    {
        Console.WriteLine("Title : {0}", title);
        Console.WriteLine("Author : {0}", author);
        Console.WriteLine("Subject : {0}", subject);
        Console.WriteLine("Book_id :{0}", book_id);
    }
};

Open class testStructure
{
    Open static void Main(string[] args)
    {
        Books Book1 = new Books(); /* 声明 Book1 为 Books 类型 */
        Books Book2 = new Books(); /* 声明 Book2 为 Books 类型 */

        /* book 1 规格 */
        Book1.getValues("C Programming",
            "Nuha Ali", "C Programming Tutorial", 6495407);

        /* book 2 规格 */
        Book2.getValues("Telecom Billing",
            "Zara Ali", "Telecom Billing Tutorial", 6495700);

        /* 打印 Book1 信息 */
        Book1.display();

        /* 打印 Book2 信息 */
        Book2.display();

        Console.ReadKey();
    }
}
```

# 第十九章

![](img/00001.jpeg)

## C# 中的枚举

枚举用于命名一组整数常量。这些枚举类型通过 `enum` 关键字进行声明。

C# 中的枚举属于值类型。最终，枚举将持有自身的值，并且不会继承或传递继承。

### 声明枚举变量

**语法**

```csharp
Enum <enum_name>
{
    Enumeration list
};
```

1. `enum_name` 是所使用的枚举类型。
2. 枚举列表是一个由逗号分隔的标识符列表。

枚举列表中的每个符号都代表一个特定的整数。较大的值会排在前面。默认情况下，第一个枚举符号为 0。

示例：`enum num { 1, 2, 3, 4, 5, 6 };`

**枚举变量示例**

```csharp
using System;

namespace EnumApplication
{
    class EnumProgram
    {
        enum Days { Sun, Mon, Tue, Wed, Thu, Fri, Sat };

        static void Main(string[] args)
        {
            int WeekdayStart = (int)Days.Mon;
            int WeekdayEnd = (int)Days.Fri;

            Console.WriteLine("Monday: {0}", WeekdayStart);
            Console.WriteLine("Friday: {0}", WeekdayEnd);

            Console.ReadKey();
        }
    }
}
```

# 第二十章

![](img/00001.jpeg)

## C# 中的类

当定义一个类时，你实际上是在为该数据类型定义一个蓝图。你并没有真正定义任何数据，而是定义了该类名称的含义。这意味着它将包含该类中的对象以及操作将执行的内容。类中的方法和变量被称为类的成员。

### 定义类

类定义以关键字 `class` 开头，后跟类名。类体由一对花括号括起来。

**示例**

```csharp
<access specifier> class class_name
{
    // 成员变量
    <access specifier> <data class> variable1;
    <access specifier> <data class> variable2;
    ...
    <access specifier> <data class> variableN;

    // 成员方法
    <access specifier> <return class> method1(parameter_list)
    {
        // 方法体
    }
    <access specifier> <return class> method2(parameter_list)
    {
        // 方法体
    }
    ...
    <access specifier> <return class> methodN(parameter_list)
    {
        // 方法体
    }
}
```

请记住：

1. 要按特定访问规则访问说明符，你需要访问成员和类。如果未指定任何内容，则使用默认值，即内部类。成员的默认访问级别是私有。
2. 需要指定数据类型，即你正在使用的变量类型以及返回类型，以便在需要时按预期返回数据类型方法。
3. 要访问类成员，需要使用点运算符。
4. 点运算符链接将告诉你对象名称和成员名称。

**示例**

```csharp
using System;

namespace BoxApplication
{
    class Box
    {
        Open double length;   // 盒子的长度
        Open double breadth;  // 盒子的宽度
        Open double height;   // 盒子的高度
    }

    class Boxtester
    {
        static void Main(string[] args)
        {
            Box Box1 = new Box();   // 声明 Box1 为 Box 类型
            Box Box2 = new Box();   // 声明 Box2 为 Box 类型
            double volume = 0.0;    // 在此存储盒子的体积

            // box 1 规格
            Box1.height = 5.0;
            Box1.length = 6.0;
            Box1.breadth = 7.0;

            // box 2 规格
            Box2.height = 10.0;
            Box2.length = 12.0;
            Box2.breadth = 13.0;

            // box 1 的体积
            volume = Box1.height * Box1.length * Box1.breadth;
            Console.WriteLine("Volume of Box1 : {0}", volume);

            // box 2 的体积
            volume = Box2.height * Box2.length * Box2.breadth;
            Console.WriteLine("Volume of Box2 : {0}", volume);

            Console.ReadKey();
        }
    }
}
```

### 成员函数与封装

成员函数是类的一部分，在类定义内部拥有自己的定义和原型，类似于其他变量。这些函数操作类的对象，成员可以访问该对象所属类的所有成员。

成员变量被称为属性，通常保持私有以实现封装。正是这些变量可以通过 `Open` 函数进行访问。

**示例**

```csharp
using System;

namespace BoxApplication
{
    class Box
    {
        private double length;   // 盒子的长度
        private double breadth;  // 盒子的宽度
        private double height;   // 盒子的高度

        Open void setLength(double len)
        {
            length = len;
        }

        Open void setBreadth(double bre)
        {
            breadth = bre;
        }

        Open void setHeight(double hei)
        {
            height = hei;
        }

        Open double getVolume()
        {
            return length * breadth * height;
        }
    }

    class Boxtester
    {
        static void Main(string[] args)
        {
            Box Box1 = new Box();   // 声明 Box1 为 Box 类型
            Box Box2 = new Box();
            double volume;

            // 声明 Box2 为 Box 类型

            // box 1 规格
            Box1.setLength(6.0);
            Box1.setBreadth(7.0);
            Box1.setHeight(5.0);

            // box 2 规格
            Box2.setLength(12.0);
            Box2.setBreadth(13.0);
            Box2.setHeight(10.0);

            // box 1 的体积
            volume = Box1.getVolume();
            Console.WriteLine("Volume of Box1 : {0}", volume);

            // box 2 的体积
            volume = Box2.getVolume();
            Console.WriteLine("Volume of Box2 : {0}", volume);

            Console.ReadKey();
        }
    }
}
```

### 构造函数

类的构造函数是该类的特殊函数，当你在该类中创建新对象时，它们会按需执行。

构造函数与类名相同，但没有返回类型。

**示例**

```csharp
using System;

namespace LineApplication
{
    class Line
    {
        private double length;   // 线的长度

        Open Line()
        {
            Console.WriteLine("Object is being created");
        }

        Open void setLength(double len)
        {
            length = len;
        }

        Open double getLength()
        {
            return length;
        }

        static void Main(string[] args)
        {
            Line line = new Line();

            // 设置线的长度
            line.setLength(6.0);
            Console.WriteLine("Length of line : {0}", line.getLength());

            Console.ReadKey();
        }
    }
}
```





默认构造函数不会提供任何参数，但如果你需要一个可以带参数的构造函数，则存在一些称为参数化构造函数的参数，它们有助于在创建对象时为其赋予初始值。

**示例**

```
using System;

namespace LineApplication

{

class Line

{

private double length; // Length of a line

Open Line(double len) //Parameterized constructor

{

Console. WriteLine("Object is being created, length = {0}", len);

length = len;

}

Open void setLength( double len )

{

length = len;

}

Open double getLength()

{

return length;

}

static void Main(string[] args)

{

Line line = new Line(10.0);

Console. WriteLine("Length of line : {0}", line.getLength());

// set line length

line.setLength(6.0);

Console. WriteLine("Length of line : {0}", line.getLength());

Console.ReadKey();

}

}

}
```

### 析构函数

析构函数也是一种特殊函数，当某个类超出其作用域时会被执行。析构函数与类同名，但前面会有一个波浪号（~），并且不能有任何参数或返回值。

当你需要在退出程序前释放内存时，析构函数会很有用，但析构函数不能被继承或重载。

**示例**

```
using System;

namespace LineApplication

{

class Line

{

private double length; // Length of a line

Open Line() // constructor

{

Console. WriteLine("Object is being created");

}

~Line() //destructor

{

Console. WriteLine("Object is being deleted");

}

Open void setLength( double len )

{

length = len;

}

Open double getLength()

{

return length;

}

static void Main(string[] args)

{

Line line = new Line();

// set line length

line.setLength(6.0);

Console. WriteLine("Length of line : {0}", line.getLength());

}

}

}
```

# 结语

![](img/00001.jpeg)

感谢您坚持读完了《C#》的全文，希望它内容丰富，并能为您提供实现目标所需的一切工具，无论目标是什么。

下一步就是运用您所学到的新编程语言，并将其付诸实践。无论您使用 C# 做什么，您都会发现所有 C 语言之间都存在相似之处。

学习编程语言时请务必保持耐心，因为如果不这样做，您将不得不回头纠正许多错误，这会占用您本可用于其他事情的宝贵时间。

谢谢，祝您好运。

