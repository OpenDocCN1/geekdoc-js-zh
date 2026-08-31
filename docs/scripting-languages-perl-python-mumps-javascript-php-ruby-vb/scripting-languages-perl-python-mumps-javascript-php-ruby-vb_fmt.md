
# 脚本语言：Perl、Python、Mumps、Javascript、Php、Ruby、Vbscript、Awk、Command.com、Sed、Bash、Autolisp、Tcl、Shell 脚本、Quakec

`PERL`, `PYTHON`, `MUMPS`, `JAVASCRIPT`, `PHP`, `RUBY`, `VBSCRIPT`, `AWK`, `COMMAND.COM`, `SED`, `BASH`, `AUTOLISP`, `TCL`, `SHELL SCRIPT`, `QUAKEC`, `BOURNE SHELL`, `REBOL`, `KORN SHELL`, `NEWTONSCRIPT`, `SERVER-SIDE SCRIPTING`, `APPLESCRIPT`, `LUA`, `C SHELL`, `CLIENT-SIDE SCRIPTING`, `PIKE`

![](img/28b49089ea8cf20e1b8f2972fae5fffa_0_0.png)

- `Python for S60` ...... 159
- `QuakeC` ...... 159
- `RBScript` ...... 160
- `REBOL` ...... 160
- `REXX` ...... 162
- `Rc` ...... 160
- `Redirection (computing)` ...... 168
- `Revolution (development environment)` ...... 189
- `RunVer` ...... 177
- `Server-side scripting` ...... 185
- `Server Includes` ...... 186
- `Shell script` ...... 186
- `S-Lang (programming language)` ...... 178
- `SAM76` ...... 178
- `SMX (computer language)` ...... 192
- `SWIG` ...... 192
- `Scripting Layer for Android` ...... 218
- `Scripting language` ...... 182
- `Seb` ...... 182
- `Sed` ...... 183
- `SenseTack` ...... 184
- `Simkin (programming language)` ...... 188
- `Smalltalk YX` ...... 188
- `Smartface` ...... 188
- `Snit` ...... 189
- `Squib (web)` ...... 190
- `StepTalik` ...... 190
- `Sun Web Developer Pack` ...... 209
- `SuperTalk` ...... 211
- `Symbolic Stream Generator` ...... 212
- `TACL` ...... 218
- `Tel` ...... 218
- `Te/Java` ...... 218
- `Tellib` ...... 218
- `Tesh` ...... 196
- `Tea (programming language)` ...... 197

# 引言

购买此书将获得 `booksall.net` 的免费会员资格。你可以从成千上万本书中选择一个数字副本，无需额外费用即可阅读。你可以通过在线版本访问相关的页面、网站、功能、备注、照片。点击版本历史查看章节的贡献者。

`AMPL` 是一种用于建模和求解优化问题的强大数学语言。它允许用户使用高级语言描述复杂问题，然后将其翻译为各种求解器。

## 特性

`AMPL` 的主要优势之一是灵活性。它将模型描述与求解器分离，用户可以在不重写模型的情况下切换不同的求解器。`AMPL` 还支持广泛的问题类型，包括线性、非线性、整数和随机规划。

# 可性

`AMPL` 适用于许多操作系统，包括 `Linux`、`Windows` 和 `macOS`。还有适用于学术和教育目的免费版本。

# 示例模型

以下是 `AMPL` 中的一个运输问题。

```ampl
set Plants;
set Markets;

param Capacity{Plants};
param Demand{Markets};
var shipment{Plants, Markets} >= 0;

minimize cost:
    sum{p in Plants, m in Markets} TransportCost[p,m] * shipment[p,m];

subject to:
    supply(p in Plants):
        sum{m in Markets} shipment[p,m] <= Capacity[p];
    demand(m in Markets):
        sum{p in Plants} shipment[p,m] >= Demand[m];

solve;

display shipment;
```

# 运输问题

运输问题是一个经典的优化问题，目标是最小化从多个工厂到多个市场的货物运输成本。

```ampl
data;
Plants := seattle francisco;
Capacity :=
    seattle 350
    francisco 600;
Demand :=
    new york 325
    chicago 300
    topeka 275;
TransportCost :=
    (seattle, new york) 4.5    (seattle, chicago) 3.5
    (seattle, topeak) 5.5      (francisco, new york) 1.5
    (francisco, chicago) 2.0    (francisco, topeak) 2.0;
end;
```

## ARExx

我们实现的 “ARExx 端口”的第三方软件。任何 `Amiga` 应用程序都可以定义一组命令和函数供 `ARExx` 调用，使得该软件的功能可以通过 `ARExx` 编写。

包括 `TxdEditor`，并在 `Using AmigaTex` 中设置。这是一个 100% 的 `Amiga` 产品。

该库也易于添加其他库或单个函数。`ARExx` 脚本也可以从其他 `ARExx` 脚本调用。任何 `Amiga` 程序在其链中都有 `ARExx` 端口，用于与 `ARExx` 共享函数。

## 特性

`ARExx` 是一种可以与其他应用程序通信的语言。例如，使用 `ARExx` 用户可以从数据库请求数据并发送到电子表格应用程序。为了支持这一点，应用程序必须是 “ARExx 兼容的”，即能够接收来自 `ARExx` 的命令并执行它们。基础程序可能具有搜索、检索和保存 `MicroFile` 数据的原生 `ARExx` 命令。文本编辑器可能具有与其编辑命令相对应的命令，并可以与 `Jorth` 一起使用以提供集成的多视图环境。`AmigaVision` 多媒体演示程序也内置了 `ARExx` 端口，并可以使用 `ARExx` 控制其他程序。

`ARExx` 可以将命令定向到相同脚本的不同版本，提供了在不同程序之间输出和匹配函数的选项。例如，`ARExx` 脚本可以从数据库中提取数据，将数据插入并进行计算，然后将结果返回文字处理器。

## ARExx 常见问题的解决方案示例

通过脚本实现新功能和能力

如果用户在使用一个通过连接位图图像文件构建动画的脚本，但缺少处理能力，可以编写一个 `ARExx` 脚本来执行这些任务：

- `ARExx` 在其目录中定位图像文件
- `ARExx` 加载第一张图像
- `ARExx` 加载绘图程序
- 将图像加载到程序中进行修改
- 修改后的图像存储在另一个目录中
- `ARExx` 对目录中的图像重复操作
- 关闭绘图程序和动画程序
- 构建动画
- 将动画保存到其目录中
- 关闭动画程序

## 历史

`ARExx` 最初于 1987 年创建，由 `Amiga` 的 `Simon S. Harvey` 开发。它是 `Mike Cowlish` 在《REXX: A Practical Approach to Programming》一书中描述的语言。`ARExx` 被包含在 `AmigaOS 2.0` (1990) 中。此版本的 `ARExx` 遵循原始逻辑；`James Harvey` 参与了 `ARExx` ANSI 标准的草拟。

`ARExx` 用 68000 语言编写，没有 `PPC CPU` 的情况下无法以全速运行，因为 `ARExx` 没有为它们重写，且在 `MorphOS 2.0` 中仍然缺失。由于与 `ARExx` 最优秀的人士发生争执，`James Harvey` 没有参与 `Amiga` 程序的开发，没有其他 `Amiga` 相关公司正在制作 `ARExx` 的版本。

根据 `ARExx` 手册：`ARExx` 是在具有 512 字节内存和两块软盘的 `Amiga 1000` 上开发的。该语言原型是用 `C` 语言开发的，生产版本使用 `Metacomco` 汇编器用汇编语言编写。文档是用...

`ARExx` 可以增加各种程序的功能。由于独立 `ARExx` 包的强大，它被包含在 `AmigaOS` 的 Release 2.0 中。

与 `REXX` 实现一样，`ARExx` 使用的数据表示较少。其他程序对整数、浮点、字符串、向量等进行区分。相比之下，`ARExx` 将所有数据视为字符字符串、标记和表达式。正如良好的扫描语言中的一样，变量在使用之前不需要声明，它们在第一次使用时自动产生。

`ARExx` 脚本受益于一个监控和重复调用的处理系统。程序可以根据需要选择继续执行。

## 避免重复性程序

`FilesRExx` 是一个著名的简单 `ARExx` 脚本示例，用于自动化重复且无聊的程序。该脚本使用 `AlexaCompare` 程序比较文件，然后在一组文件中找到所有重复项，并返回输出，用不同颜色高亮任何差异之处。

## 扩展 AmigaOS 功能

`ARExx` 的主要功能之一是通过添加操作系统缺少的功能来扩展 `AmigaOS` 的能力。例如，可以编写一个简单的 `ARExx` 程序在显示器屏幕上打印警告消息，或者在 `Amiga` 程序停止、故障或完成计划任务时播放。

以下脚本是一个极简的 `ARexx` 脚本，根据发生的事件显示结果。

* Alarm.maxx *

## AS/400 控制语言

`AS/400 控制语言` (`CL`) 是用于 `IBM AS/400` 平台的脚本语言，类似于作业控制语言 (`Job Control Language`)，由一组不断扩展的命令 (`*CMD`) 组成，用于调用传统的 `AS/400` 程序并获取这些程序如何操作的帮助。`CL` 还可以用于创建 `CL` 程序（脚本组），其中有额外的命令提供功能（`GOTO`，`ELSE`，变量声明，文件输入等）。

`IBM` 引入了多种 `AS/400` 命令来执行系统级任务，如编译程序、备份数据、更改系统配置、显示对象详情或删除命令。它们限于某些系统级别，并可以为用户应用程序定义。

```
ARG event
IF event = 0 EXIT
IF event = 1 SAY "Program
has executed unexpectedly"
IF event = 2 SAY "Program
has finished its job"
IF event = 3 THEN SAY "Cannot
```

在 `select` 目录中查找数据”（源已编辑）：

（注：由于原文后续存在大量重复的 AS/400 描述段落，根据指令“不要重复输出原文”，此处仅保留核心描述，不再重复翻译完全相同的内容。）

## 6 - AS/400 控制语言

多于上述指定的四个。这是由于未指定 `CHPGM` 参数导致的结果，因此将传递默认值。

## 创建新命令

### 命令分组菜单

除了 `PGM` 参数外，该默认值是 `*SAME`（意味着你无法更改它）。

可以创建新命令来调用非系统程序，它们的工作方式与 `AS/400` 完全相同。命令定义语言在 `CL` 程序员指南中有所描述。

`VERB` 和 `SUBJECT` 菜单是所谓的分组菜单的一部分。每三个（或四个）字母都是一个以字母 `CMD` 开头的菜单。同样，所有的 `CHG` 都会执行命令 `CMDCHG`。对于程序，它将被命名为 `CMDPG`。

为新命令及其相关项创建屏幕界面是一个好主意。所有屏幕都使用面板组对象 (`*PLNGRP`)，并可以使用 `IBM AS/400` 应用规范的 UI 语言创建。

### 提示（Prompting）

所有 `AS/400` 命令都可以通过在命令行输入命令并按下 `F4` 键，或通过 `CL` 程序直接进行提示。`AS/400` 也可以在命令前输入 `*` 来进行提示。（这处于交互式界面中，显示命令字符串，并已经填充了部分内容。）

除了分组菜单外，还有其他菜单。在空命令行上按 `F4` 可以访问提及系统的起点。

### 命令选择

在系统的第 3 版本中，引入了一种更简单的创建方法：运行命令。

如果只知道命令的一部分，或者使用的第三方工具其命令不符合 `AS/400` 标准偏差，你只需输入已知命令部分，附加一个星号（使其成为通用名称），并按回车。系统将显示你的库列表中匹配你所需的通用名称的命令列表。然后可以翻页查找命令，并使用方向键进行选择。

系统将向你展示命令接受的参数集（必需参数会被突出显示）。

```
GENMCMD(CMD/LIB/MYTYOD)(QYS/LIB/MYLIB/PNRNRC.SRC)GENOPT(*)
```

列出了必需参数，带有系统默认值的参数列在最后。如果选择进一步的值（可以通过回答提示来更改的值），请使用 `F10`。

将使用 `UI` 面板自动生成命令描述的所有参数。结果可以进行编辑（`sed`, `wdsi`, `rid`），然后使用 `CRNPLGRP` 创建，最后通过命令 `CHOCLD MIPLGRP` 关联。

提示功能进一步增强到每个命令有效值的低因素程度。在提示期间，用户使用光标移动到字段问题并按下 `F4`。系统随后将显示一个显示输入类型和可用值列表的屏幕。

## 查找正确的命令

`IBM` 命令中有 2,611 条命令，但发现它们并非所有命令都有良好的系统设计来让生活变得轻松。这些节省设备是：标准化缩写、命令分组和命令选择。

要输入名称或进入输入额外值的列表，可以使用加号代替。（当列出要保存或还原的对象的名称时。）

## 示例代码

以下是 `CL` 编程的示例。该程序在月份和日期之间转换日期。共有 24 个版本。它接受两个参数：`&IN` 参数是待转换的日期。它应该是格式为 `YYYYmm` 的字符串，其中年份是月日。`MDYY` 必须是 `mmDD` 格式。第二个参数是 `&TYP`，它是要转换的日期类型。它必须是 `'J'`（儒历）或 `'M'`（公历）。例如：命令 `PGM(ICVTDATC) PARM('01480 'M')` 将转换儒历日期 01480（2004年6月28日）。

## 标准化缩写

`AS/400` 标准化了创建命令时使用的缩写。动词始终更改为 `CHG`，显示为 `DSP`，创建为 `CREATE` 等。主体始终为 `PGM`，用户为 `USER`，模块为 `MOD` 等等。你可以在 `VERB` 和 `SUBJECT` 菜单中看到 `AS/400` 上使用的每个动词和主体，然后输入命令 `GO VERB` 或 `GO SUBJECT`。

## 命令帮助

`AS/400` 上的非必需命令也可以提示光标帮助。如果帮助提供了帮助内容，你可以通过将光标移动到所需的字段并按下 `F1` 来查看帮助。要获取整个命令（本身及其任何一个参数）的帮助，你需要按下。

## AWK

`AWK` 是一种用于 `Unix` 类系统中的数据提取工具，用于文本处理和数据分析。它是一种使用模式-动作语句的脚本语言。`AWK` 创建于 20 世纪 70 年代的贝尔实验室，其名称源于作者的名字——`Alfred Aho`、`Peter Weiner` 和 `Brian Kernighan`。它通常不读作分开的字母签名，而是读作一种鸟的名字，这也是该语言的标志。

## AWK 程序的结构

`AWK` 是一种用于处理文本的语言。一个文件被视为记录，每一行被视为一条记录。每条记录被拆分为字段序列，因此我们可以将行中的第一个单词视为第一个字段，第二个单词视为第二个字段。因此，一个 `awk` 是模式-动作语句的序列。

## AWK 命令

`AWK` 命令是替换上述中“动作”的语句。`AWK` 命令可以包括函数调用、变量、计算或任何其他内容，其中许多函数是内置的，许多函数由不同版本的 `AWK` 提供，此外，某些版本偏好使用动态链接库，这些库也提供了更多函数。

## print 命令

`print` 命令用于输出文本。输出总是终止的。

## 8 - AWK

通过一个定义的字符串调用输出记录分隔符（`ORS`），其默认值是换行符。该命令最简单的形式是：

这显示记录的内容。在 `AWK` 中，记录被划分为字段（`fields`），这些字段可以单独显示：

```
print $1
```

显示记录的第一和第三个字段，它们之间用一个定义的字符串分隔，即输出字段分隔符（`ORS`），其默认值是一个空格：

```
print $1,$3
```

显示记录的第一和第三个字段，它们之间用逗号分隔（`$` 符号专门表示变量），`$0` 可以指代记录的字段。在特殊情况下，`$0` 指代整个记录。事实上，`"print"` 命令和 `print $0` 的功能是等价的。

`print` 命令还可以显示计算结果和函数调用的结果：

```
print $3+2
print floor(3)
print floor(variable)
print $(3-2)
```

输出可以发送到文件：

```
print "file name" > "file name"
```

或者通过管道发送：

```
print "expression" | "command"
```

## 内置变量

`AWK` 的内置变量包括字段：`$1`, `$2`, `$3` 等（`$0`）代表整个记录。它们存储了记录中各个字段的文本或值。

其他变量：

- `NR`：统计输入记录的个数。
- `NF`：统计输入记录中字段的个数。记录中的最后一个字段由 `NF` 指定。
- `FILENAME`：包含当前输入文件的名称。
- `FS`：包含用于划分输入记录中字段的“字段分隔符”字符。默认值“空白符”包括任何空格和制表符。可以将 `FS` 重新赋值为另一个字符以更改字段分隔符。
- `RS`：存储“记录分隔符”字符。由于默认情况下，输入行是记录，因此记录分隔符是“换行符”。
- `OFS`：存储“输出字段分隔符”，当 `AWK` 打印字段时用于分隔字段。默认值是“空格”。
- `ORS`：存储“记录分隔符”，当 `AWK` 打印记录时用于分隔记录。默认值是“换行符”。



# OFMT

`OFMT`：存储数值输出的格式。默认格式为 `"%6g"`。

该语句可以如下所示调用：

```awk
print add_3(36) # 输出 39
```

函数具有局部作用域变量。参数名被添加到参数列表的末尾，但在调用它们时应省略值，在函数参数中添加空格以指示本地变量的结束。

在函数定义中，函数名和左括号之间可能存在一个或多个空格，但在调用中不允许有空格。

## 示例应用

### Hello World

这是当前的 `"Hello World"` 字符。

```awk
BEGIN { print "Hello, world!" }
```

注意，这里不需要显式语句；由于唯一的模式是 `BEGIN`，命令行参数会被处理。

### 打印长度超过 80 字符的行

注意默认操作是打印当前行。

```awk
length($0) > 80
```

### 打印单词计数

统计输入中的单词，并打印单词数（类似于 `wc`）：

```awk
w += NF
c += length($0) + 1
```

```awk
END { print NR, w, c }
```

变量可以使用语言关键字的任何字符。运算符`+ - * /`，即乘法、减法、除法和连接。对于字符串或字符串变量：

```awk
function function_add(n) {
return n + 3
}
```

## 用户定义函数

采用类似于 C 语言的格式，函数定义由关键字`function`、函数名、参数和函数体组成。这是一个函数的示例。

由于程序的第一行没有模式，默认情况下匹配增量操作的每一行都会对每一行执行。注意`+=`是`w = w + NF`的简写。

### 列表单词求和

```awk
{ s += $NF }
END { print s + 0 }
```

`print`函数执行标准的 C `print`，其工作方式与上述的`print`命令类似。然而，匹配（`match`）的工作原理如下：`NR`是记录数，即 AWK 认为的行数，当前行是从输入的第一行开始计数的数字。`%`是模运算运算符。`NR == 4`对于第一、第五、第九等等行为真。同样，`NR == 6`对于第三、第七等等行为真。

该范围在第一部分匹配或包含第二部分行（第 3 行）之前为假。然后它在第 5 行再次匹配第一部分。第二个命令被发送到`print`字段，你防止刷新（`flush`）等同于如果头部匹配。在这种情况下，对于行上的每个字段，我们根据该计数转换为小写的次数增加一。最后，在`END`块中，我们打印频率`s`增加了`$NF`值的单词，`$NF`是由 AWK 的空白符字段分隔符定义的行中的最后一个单词。`NF`是该行字段的个数。`$`是第四个字段的值，`NF`是第一行的值，无论它有多少个字段，或者少于（的）行数。它是一个具有运算符优先级的实际一元操作。如果那么`NF == 0`，`$0`就是该中可能的空格之外的行，以此类推。

`for (in words)`创建一个遍历`words`的循环，将`i`设置为数组的每个值。这不同于...

## 10 - AWK

AWK 编写于 1977 年，并随 Unix 分发。在 1980 年代，其他人开始扩展该语言，增加了用户定义函数。该语言在 1988 年出版的《AWK 编程语言》中有所描述，其实现随 Unix 发布。为了避免与旧版本（有时被称为`new awk`）发生冲突，该实现是在自由软件许可证下发布的。

`gawk`是另一个自由软件，并在本地化和 TCP/IP 网络方面做了许多尝试。它允许用户扩展程序的功能。`gawk 3.0`版本包含在 FreeBSD 5.0 中。后续版本使用 FreeBSD `awk`以获得 GPL，这是一个比 BSD 许可证更严格的许可证。

注意`if`块，`awk`只在运行命令前检查它是否从标准输入读取。这意味着：

* 检查是否匹配；反之则不然。正则表达式只是一个字符串并可以存储在变量中。

* `BWK awk`指 Brian W. Kernaghan 的版本，被称为"真 AWK"，这个术语源于最初设计该语言且 Kernaghan 是 AWK 的作者之一。FreeBSD 将此版本称为`one-true awk`。

只有当程序运行后没有剩余文件名时才有效。这是一个使用`ENVIRON`的 shell 脚本，它是从 `One-True awk`的新版本内部引入的。下标`ENV`是环境变量的名称；其值是从各种标准库获取的。shell 将该参数标记为包含第一个参数的环境变量，并且`awk`拥有每个文件的模式。

`BEGIN`不仅是为了提取第一个参数，还为了防止它在`BEGIN`块结束后被解释为文件名。`ARGC`是参数个数，是

将 AWK 脚本转换为 C 代码的翻译器。在包含作者的`libawk`时，生成的的可执行文件速度大幅提升，且根据作者的测试，它们与其他版本的 AWK、Perl 或 Tel 兼容性非常好。小型脚本将变为 160-170 KB 的程序。

`tawk` (ActionScript) 是一种适用于 Solaris、DOS、OS/2 和 Windows 的 AWK 操作系统，此前由 Thompson Automation Software（该已已停止运营）销售。

* `Jawk`是一个在 Java 中实现 AWK 的源码项目。将添加扩展以提供在 AWK 脚本中使用 Java 特性（例如 Java 线程、套接字、集合等）。

* `gawk`是一个基于`awk`的 SourceForge 项目。它通过动态加载的库扩展了`awk`。

* `QSEAW`是包含在 QSE 库中的嵌入式 AWK 解释器，为 C 和 C++ 提供了嵌入 API。

`Busybox`是一个由 Dmitry Zakharov 编写的文档记录较少的 AWK 实现。这是一个用于嵌入式系统的微型实现。

来源（编辑自）：`http://en.wikipedia.org/wiki/AWK/`。

# ActionScript

ActionScript 是一种由 Macromedia Inc.（现归 Adobe Systems 所有）开发的面向对象的语言。它是 ECMScript 的衍生语言（意味着它具有与广为人知的 JavaScript 相同的语法和语义），用于网站开发并针对 Adobe Flash 平台。该语言是开源的，因此其规范是免费的，并提供了两个版本的开源虚拟机（Mozilla Timeline）。

ActionScript 最初设计用于控制在 Flash（原名为 Macromedia Flash）中制作的简单 2D 矢量动画。最初侧重于动画，Flash 版本提供的交互功能较少，且脚本能力非常有限。后来的版本允许创建基于 Web 的游戏以及与媒体（如视频和音频）的互联网交互。如今，ActionScript 适用于桌面应用程序、机器人技术等领域，例如 Movie Kit Controller。

Flash MX 2004 引入了 ActionScript 2.0，这是一种适用于应用程序开发的编程语言。现在可以通过脚本而不是动画来节省时间，这通常在编辑时能够提供更高水平的灵活性。

随着 Flash 9 alpha 的到来（已发布了更新版本的 ActionScript），ActionScript 3.0 是一种面向对象的语言，在构建复杂应用程序时允许更自由的控制和可读性。此版本旨在运行在从头完全重写的 ActionScript 虚拟机上（AV 翻了一倍）。由于由于，用 ActionScript 3.0 编写在 Flash 9 及更高版本上快得多，且在之前的版本无法运行。同时，ActionScript 3.0 的执行速度比 Flash 快达 10 倍。

Flash 可以与浏览器的 XML 属性配合使用，以渲染丰富的内容。这种技术被称为异步 Flash 和 XML，类似于 AJAX。Adobe 提供其 Flash 产品以满足基于 Flash 构建的富媒体网络应用的需求，并使用 ActionScript 进行行为处理和编程。ActionScript 3.0 构成了 Flash 2 API 的基础。

## 历史

ActionScript 最初作为 Macromedia 畅销工具的面向对象的语言，现在由 Adobe Systems 开发为 Flash。Flash 制作工具的前三个版本限制了交互功能。早期的 Flash 开发者可以向按钮或帧附载一个简单的命令，即"动作"（`action`）。动作集是基本的导航控制，命令如`"play"`（播放）、`"stop"`（停止）、`"getURL"`和`"gotoAndPlay"`（跳转并播放）。

随着 1999 年 Flash 4 的发布，这组动作变成了一门小型脚本语言。Flash 4 引入的新功能包括变量、表达式、操作和循环。尽管被称为"ActionScript"，但 Flash 4 的用户手册和营销文档继续使用这组命令。

# 按版本发布的时间线

* Flash 2：第一个带有脚本实现的版本，包括用于时间轴控制的`gotoPlay`、`gotoStop`、`nextFrame`和`nextScene`。

* Flash 3：扩展了脚本支持，具有加载外部 SWF (`loadMovie`) 的能力。

* Flash 4：第一个具有完整脚本实现（ActionScript）的版本。该语言基于 Flash 语法，并继续对图层、变量和其他基础语言结构的支持。

* Flash 5：包含了第一个版本的 ActionScript。基于 ECMScript 的原型编程，并允许完全的程序化和面向对象编程。

* Flash 6：增加了事件处理模型、无障碍控制以及对 Web 的支持，是第一个支持 AMF 和 RTMP 协议进行按需音频/视频流传输的版本。

* Flash Player 7：添加了文本的 CSS 样式并支持 ActionScript 2.0，这是一种基于 ECMScript 3 Netscape 原型的、具有基于类的继承特编程语言。ActionScript 2.0 可以编译为 ActionScript 1.0 字节码，可以在 Flash Player 6 中运行。

* Flash Player 8：通过添加新的类列表扩展了 ActionScript 1/2，这些 API 用于在运行时控制位图数据、实时视频滤镜以及阴影的模糊处理。

* Flash Player 9（最初为 8.5）：在高级虚拟机 AVM2（ActionScript 虚拟机 2）中加入了 ActionScript 3.0，它与之前的版本竞争。由于由于原因，用 ActionScript 3.0 编写的代码在 Flash 9 上速度快得多，且不会在之前的版本中工作。同时，ActionScript 3.0 的执行速度比 Flash 快达 10 倍。

Flash 可以与浏览器的 XML 属性配合使用，在其中渲染丰富的内容。这种技术被称为异步 Flash 和 XML，类似于 AJAX。Adobe 提供其 Flash 产品以满足基于 Flash 构建的富媒体网络应用的需求，并使用 ActionScript 进行行为处理和编程。ActionScript 3.0 构成了 Flash 2 API 的基础。

# ActionScript 版本时间线

2000-2003：ActionScript `"1.0"`随着 2000 年 9 月 Flash 5 的发布，对 Flash 4 的"动作"进行了增强。这是第一个支持 JavaScript 和 ECMScript 版、类及其许多核心类型的 ActionScript 版本。可以使用`var`语句声明局部变量，并可以创建带有参数和返回值的自定义函数。ActionScript 除了从下拉列表和对话框选择外，无法与其他文本编辑器配合。随着 Tool MX 及其支持的 Flash Player 6 发布，语言基本保持不变；除了一些变化，例如"严格相等"运算符，这使其更接近 ECMScript-262。ActionScript 与后期版本相比的两个重要特征是它的松散类型和对原型继承的依赖。

应用程序，ActionScript 2.0 的特点是编译时类型检查和基于类的语法，例如关键字和`extends`。（虽然这允许了更结构化的面向对象方法，但代码仍会被编译为 ActionScript 1.0 字节码以便在 Flash Player 6 运行时使用，类继承是原型系统之上的层）。在 ActionScript 2.0 中，开发者可以通过添加类型注解将变量限制为特定类型，从而在编译时捕获某些错误。ActionScript 2.0 还引入了基于类的继承，开发者可以创建类和接口，就像 Java 和 C++ 等语言一样。（此版本遵循 ActionScript 第四版规范。）

2006-今天：ActionScript 3.0 Adobe 在 2006 年 6 月引入了 ActionScript 3.0 及其对应的 Flash Player 9。ActionScript 3 是该语言的根本性重构，因此它使用一个完全不同的虚拟机。Flash Player 9 包含两个虚拟机 AVM1 和 AVM2。它增加了对硬件加速的有限支持。

响应用户对一种能够胜任更复杂的语言的需求

## ActionScript - 第 13 页

关于 DOM 事件处理标准。

在编写 ActionScript 2.0 类文件时，上述示例可以写入命名为`Greeter.as`的文件中，如下所示：

最后，开发 Flex 应用程序时 ActionScript 的示例如下，应存放在名为`Greeter...`的文件中：

* 为了处理目的集成了 XML 的 ECMAScript (E4X)。

```as
class com.example.Greeter extends MovieClip
```

```as
package
```

* 直接访问 Flash 运行时显示列表，以获取运行时显示的内容。

```as
public class Greeter
```

* 完全符合 ECMAScript 第四版规范的实现。

```as
public function Greeter() {}
public function onLoad():void {
```

```as
public static function sayHello(String) {
var greeter: String = "Hello, world!";
return greeter;
```

* 对动态 3D 对象 (X, Y, Z) 旋转和纹理映射的支持有限。

```as
var txtHelloField = this;
createTextField("hello", 0, 0, 100);
txtHelloField = "Hello, world";
```

* Flash Lite 1.0：Flash Lite 专为手机和消费电子产品开发。

* Flash Lite 1.1：增加了对 Flash 4 ActionScript 支持以及额外的 API。

* Flash Lite 2.0 和 2.1：增加了对 FlashScript 2.0 和一些额外命令 2 支持。

# ActionScript 3.0

ActionScript 3.0 具有类似的语法，但在创建对象方面与 AS2 不同。将下面的脚本与之前的 ActionScript 2.0 进行比较：

* Flash Lite 3：增加了对 Flash 8 ActionScript 2.0 和 FLV 视频播放的支持。

* Flash Lite 4：增加了对 Flash 10 ActionScript 3.0 作为浏览器插件的支持，以及硬件加速。

```as
var txtField:new TextField();
txtField.text = "Hello World";
this.addChild(txtField);
```

由于编程语言与 Flash IDE 之间的分离程度增加，极简的 ActionScript 3.0 程序可能会变得更大且更复杂。

此代码将与以下 MXML 应用配合：

```xml
<?xml version="1.0" encoding="utf-8"?>
<mx:Application xmlns:mx="http://www.adobe.com/2006/mxml" verticalLayout="" onComplete="initApp()">
<mx:Script>
<![CDATA[
public function initApp():void {
// Prints我们的 "Hello, world!"
var message = "MainText";
mainText.text = message;
}
]]>
</mx:Script>
```

# 语法

基本语法源自 ECMAScript。以下代码在任何编译器中均可运行，会在屏幕深度为 0 处（以像素为单位）创建一个宽 100 像素、高 100 像素的文本字段。文本设置为`"Hello, world"`，并自动在播放器中显示：

```as
createTextField("greet", 0, 0, 100);
greet.text = "Hello, world";
```

```as
package com.example;
import flash.display.Sprite;
import flash.text.TextField;

class Greeter extends Sprite {
    public function Greeter() {
        var txtField:TextField = new TextField();
        txtField.text = "Hello, world";
        this.addChild(txtField);
    }
}
```

## 数据结构

ActionScript 包含基础数据类型。在之前的版本中，`undefined`是 Object 值。在 ActionScript 3.0 中，这些是"基础"数据类型。

## ActionScript 顶级类型

* `String`：字符串。

* `Number`：数值，表示整数和浮点数。

* `Boolean`：布尔值，包含 `true`或`false`。

* `Object`：对象。

## ActionScript 复杂类型

* `MovieClip`：动画电影辑对象；Flash 时间线默认是 `MovieClip`。

* `TextField`：动态的文本字段对象。



- `Button`：具有“向上”、“悬停”、“按下”状态的简单按钮，继承自`MovieClip`。
- `Date`：表示特定时间点的对象。
- `Array`：线性存储。
- `XML`：XML 对象。
- `Node`：节点。
- `Null`：只包含一个值。
- `void`：空类型。在之前的版本中，`undefined`是`Object`类实例的值。在`ActionScript 3.0`中，实例的值是`null`。
- `Array`：包含数据列表。虽然`ActionScript 3`是强类型语言，但`Array`可以是任何类型的值并在检索后转换回原始类型。
- `Vector`：仅在发布为`Flash 10`及以上版本时支持的数组变体。它们是类型化的（必须定义类型），可以是固定长度。

# 16 - ActionScript 代码保护

大多数混淆方法都处于保密状态，因为它们被用于流行的 ActionScript 混淆器中。

```javascript
do {
  if (false) {
    if ((add).holder(1)); // popped
    if (true) {
      // 意外跳转
      do {
        stop();
        if (false) {
          // 意外跳转
        } while (this);
      } while (this); // popped
    } while (unexpected jump)
    }
  }
}
```

# 概述

混淆是修改 ActionScript 代码的过程，使得原始代码无法用于编程函数、参数和变量名；然而，带有混淆代码的 SWF 文件已为玩家准备绪。

ActionScript 混淆算法旨在抵抗反编译并保护开发成果不被窃取。有很多不同的频繁且共享的工具，提供了不同的混淆选项。某些 SWF 保护器实现了转换、控制流重命名和数据抽象变形器，以使生成和安全输出变得困难。另一些工具根据反编译器插入特定的陷阱来管理受保护的文件并提取其部分资源（声音、图像等），但它们无法正确读取 ActionScript 代码。这通常发生在受保护的 SWF 使用软件混淆加载时，后者可能会崩溃或意外退出。

```javascript
Set("x0B1A1\X136", true);
Set("x0B1A1\X136", true);
while (true) {
do {
  if (true) {
    /* 意外跳转*/ // not popped
    // 意外跳转
    if (false) {
      while (true);
      do {
        // 意外跳转
      } while (true);
    } while (swAction0AD)
  }
}
```

## 示例

理解 SWF 混淆优势最简单的方法是比较未受保护的 SWF ActionScript 代码与受保护的。

# ActionScript 2.0

混淆代码：

```javascript
stop();
if (this.holder == Number.this.holder(1)) {
  loadMovie("jopeClipLoader5.swf", this.holder);
} else {
  this.holder;
  loadMovie("jopeClipLoader5.swf");
}
```

```text
hexdata
05,x52,x07,x99,x02,x00,x02,x39,x00...
// 未知动作
(add).
holder(1)."holder1".holder(1);
holder(1).loadMovie();
// 意外跳转
/* Error1016 */
// 意外跳转
do {
  // (this) not popped
  if (true) {
    // 意外跳转
    while (this);
    // (this) not popped
    // 意外跳转
  } while (true);
} //swAction0AD- hexdata
05,x52,x07,x99,x02,x00,x02,x39,x00...
// 未知动作
"holder1".holder.loadMovie();
// 意外跳转
/* Error1016 */
```

# ActionScript 3.0

混淆代码：

```javascript
private function getNeighbors(i:int): Array {
  var a:Array = new Array();
  for (var k = 0; k < i; k++) {
    var ni = i + int(neighbor_map[k][0]);
    var nj = j + int(neighbor_map[k][1]);
    if (ni < 0 || ni >= size || nj < 0 || nj >= size) {
      continue;
      a.push(Cell(ni[nj]));
    }
  }
  return a;
}
```

混淆代码：

```javascript
function getNeighbors(i:int): Array {
  var a:Array = new Array();
  for (var k = 0; k < i; k++) {
    var ni = i + int(neighbor_map[k][0]);
    var nj = j + int(neighbor_map[k][1]);
    if (ni < 0 || ni >= size || nj < 0 || nj >= size) {
      continue;
      a.push(Cell(ni[nj]));
    }
  }
  return a;
}
```

# Action Script Script

Action Script (ACS) 是一种用于视频游戏（如 Hexen 和某些 Doom 源码端口）的脚本语言。它的语法与 C 相似，但灵活性较低。

来源（编辑）："http://en.wikipedia.org/Wiki/Action_Script"

# Active Script

Active Script（以前称为 ActiveX Script）是 Windows 用于实现基于组件脚本支持的技术。它基于 COM（更准确说是 OLE Automation），允许以 COM 模块的形式安装额外的脚本引擎。

用途与历史

Active Script 技术首次于 1996 发布，随着 Microsoft Internet Explorer 3.0（1996年8月）和 Internet Services 3.0 产品（1996年12月）的发布。

Active Script 的应用：

- Active Server Pages (ASP) 服务器脚本
- Internet Explorer
- 用于常规任务的 Windows 脚本，包括登录脚本、注册表操作等。其他管理用途包括 Windows 管理实例和 Active Directory 服务接口。Active Script 还可以用于通用脚本、文本处理、快速原型设计以及应用程序宏/脚本编程，使用脚本作为主要自动化方法的应用程序，其他没有方便的功能，但可以通过组件可以使用；或者用户可以选择默认添加语言/工具，例如 Excel 中的脚本或 Visual Basic Applications (VBA)，从终端到文字处理器或电子表格，这些具有不同的宏工具或完全没有。

# 18 - Adenine（编程语言）

Adenine 以核酸腺嘌呤命名，是一种脚本语言，是在麻省计算机科学与人工智能实验室 (CSAIL) 与 NTT 合作的 Haystack 项目和 Oxygen 项目背景下开发的。

特点是该语言支持 RDF。Constructine 的语言结构源自 Python 和 Lisp。

数据类型系统对应 RDF 和 XML Schema 的数据系统，并且可以扩展。作为脚本语言，Adenine 是跨平台的。

该语言也可以用基于 RDF 的语法表示和编写。此外，除了 RDF，Adenine 还可以

Adenine 的显著特征是

## Agena (编程语言)

Agena 是一种解释型过程化编程语言，设计用于科学、教育、语言学、图形和其他应用，包括脚本编写。它的语法与 Alist 非常相似，并引入了从 Maple、Lua 和 SQL 中提取的 68 个元素。其实现基于 Lua 5.1 的 ANSI C 源码。

Agena 以半人马座阿尔法星（Beta Centauri）命名，它是人马座中最亮的恒星，同时也与 20 世纪 60 年代美国航空航天局（NASA）双子座任务使用的 Agena 目标载天器同名。来源（已编辑）："http://en.wikipedia.org/wiki/Agena_(programming_language)"

## Alist shell

Alist shell（也称为 A shell 和 ash）比 Bourne shell 的 SVR4 变体流行得多；它是一个快速、兼容 POSIX 的 Unix shell，旨在在后来的发行版中取代 Bourne shell。最初，它不具备行编辑或命令历史记录功能，因为 Alist 认为这些功能应该移动到主驱动程序中；然而，目前的变体支持这些功能。ash 的 Debian 版本被称为 Alist Shell (dash)。大多数脚本似乎至少使用了 bash 特有的语法。Slackware 的设置脚本是一个显著例外，因为磁盘上安装的是 ash。NetBSD 和 Ubuntu 使用 ash 作为 /bin/sh。

某些 Linux 发行版也使用 ash 的派系（默认）。尽管 Bash 更流行，但 Debian 和 Ubuntu 使用 dash 来执行 shell 脚本，但 bash 同样存在。以下内容提取自软件包信息：Ash 在 Debian 和 Ubuntu 上均已被替换。dash 已经成为 ash 的替代品，并预计从 2006 年 10 月发布的 6.1 版本开始成为 Ubuntu 的默认 /bin/sh。

ash 的派系是 FreeBSD、NetBSD、GrayBSD 和 Minix 上的默认 ( /bin/sh )。ash 在嵌入式 Linux 系统中也相当流行；它的代码被整合到了 BusyBox 全能工具中。

ash（内核 Alist shell）是一种为内存有限的机器设计的轻量级（1992年）Bourne shell，但它没有提供 bash、tsch 和 zsh 等 shell 的所有额外功能。它可以运行大多数兼容 Source 的 shell 脚本。来源（已编辑）："http://en.wikipedia.org/wiki/Alist_shell"

## Apache River

Apache River 是一种开源编程语言，用于开发网站，并将 Tec 作为脚本语言来创建动态网站。River 与 PHP、ASP 和 JSR 。River 由 Cameron Courtney、David Denton 和 Library 开发。River 可以使用发布的数千个库之一，这些库提供了无数功能，如数据库交互（Oracle, PostgreSQL, MySQL 等）或强大应用程序的接口（如 GD Graphics）。来源（已编辑）："http://en.wikipedia.org/wiki/Apache_River"

## 使用 River 的知名网站

- FlightAward

## Appcelerator Titanium

Appcelerator Titanium 是一个利用技术开发移动和桌面应用的平台。Titanium 由 Appcelerator 公司开发，并于 2008 年 12 月推出。2009 年 6 月增加了对 iPhone 和 Android 移动应用的支持。2010 年 4 月增加了对 iPad 平板应用的支持。2010 年 6 月宣布了对 BlackBerry 的支持，目前处于封闭测试阶段。Appcelerator Titanium 是多个基于手机的应用程序框架之一，允许开发者利用现有技能为 iPhone、BlackBerry 和 Android 创建原生应用。Titanium 经常用于 Adobe Air 为 Windows、Mac 和 Linux 开发桌面应用。传统上，开发用于计算平台的原生软件应用需要专有工具和专用工具。

Appcelerator Titanium 包含一个基于 Web 的跨平台工具，需要访问互联网和开发者账户。该工具可以从任何这些平台为 Mac、Windows 和 Linux 部署独立应用程序。它通过将源文件提交到服务器端解决方案并返回二进制文件来实现。还有一个开源命令行编译器可用，具有相同的网络和账户要求，但它不支持跨编译。移动脚本需要额外要求：iPhone 构建需要 Mac OS，iPhone 构建需要 Mac OS。Titanium 经常用于 Adobe Air 为 Windows、Mac 和 Linux 开发桌面应用。传统上，开发用于计算平台的原生软件应用需要专有工具和专用工具。

Appcelerator Titanium 包含一个基于 Web 的跨平台工具，需要访问互联网和开发者账户。该工具可以从任何这些平台为 Mac、Windows 和 Linux 部署独立应用程序。它通过将源文件提交到服务器端解决方案并返回二进制文件来实现。还有一个开源命令行编译器可用，具有相同的网络和账户要求，但它不支持跨编译。移动脚本需要额外要求。随着 Services 和 Automator 扩展了 AppleScript，2011 年该公司引入了 Cocoa。随着 Services 和 Automator 扩展了 AppleScript，2011 年该公司引入了 Cocoa。

## AppleScript

AppleScript 利用了 Apple 事件（Apple Events）：这是一种 Macintosh 操作系统用于向应用程序发送信息的标准化数据格式。Apple 事件允许脚本同时与多个应用程序工作，在无需人工干预的情况下在它们之间传递数据。例如，一个用于创建简单网页图库的 AppleScript 可能遵循以下步骤：

在任何套件（suite）中都存在两种基本元素：类（Classes）和命令（Commands）。类是可脚本的对象——例如，文本编辑器允许用于文档（Documents）、窗口（Windows）和文本（Text）的类——这些类是可以更改的（窗口大小、背景颜色、字体大小等）。命令（一个窗口可以包含多个文档，一个文档可以包含文本和字符）可以传递给可脚本的对象。

- 在照片编辑应用中打开照片（通过向应用程序发送“打开文件”指令）
- 告诉照片编辑应用处理图像（降低分辨率、添加照片滤镜、裁剪）
- 告诉照片编辑应用将更改后的图像保存到不同的文件夹中（通过发送应用程序和保存/关闭 Apple 事件）
- 将新文件路径（通过 Apple 事件）发送到文本编辑器或网页编辑器
- 告诉文本编辑器在 HTML 文件中为照片编写链接
- 对每个文件夹条目（或数百个条目）重复上述步骤
- 通过向 FTP 客户端发送 Apple 事件、使用内置的 AppleScript 命令或向 Unix ftp 发送 Apple 事件，将 HTML 文件和修改后的照片文件夹上传到网站。

对于用户来说，应用程序中的数百或数千步可以减少为单一操作，运行速度更快，且没有人为错误的可能。可以开发复杂的脚本运行一次，而其他脚本则反复使用。

AppleScript 元素在脚本字典（Scripting Dictionary）中可见（作为应用程序的一部分分发），可以在任何脚本编辑器中查看。元素通常根据松散的功能关系分组在套件中。

```applescript
display dialog "Hello! -- 带有带有“确定”和“取消”的模态窗口 -- 或 display alert "Hello! -- 带有带有“确定”按钮的模态窗口 -- 或 say "Hello! -- 使用合成语音的音频消息
```

AppleScript 具有多种接口选项，包括对话框（dialogs）、警报（alerts）和“来自列表（from list）”。

```applescript
-- Dialog
set dialogReply to dialog "Text event" after answer text false
```

- buttons ("Skip", "Okay", "Cancel")
- default button -- "Okay"
- cancel button -- "Skip"
- with title --

```applescript
Dialog Title with icon note - giving up after 20
```

所有应用程序都提供免费的命令（通常称为脚本套件 Script Suite）——打开、保存文件、打印、退出、设置数据变量的命令——作为界面可脚本属性的基本对象。许多应用程序拥有能够执行脚本可以执行任何任务的套件。在特殊情况下，应用程序可能支持包含其脚本字典的插件。

AppleScript 设计用于通过记录操作立即处理脚本。当执行 AppleScript 或点击记录按钮时，计算机上的任何用户操作——在任何支持 Apple 事件和 AppleScript 的应用程序中——都会被记录为 AppleScript 命令。生成的脚本可以保存并重新运行以复制原始操作，或进行修改以更具通用性。

## Hello World!

在 AppleScript 中，传统的 Hello World! 程序可以用许多不同的形式编写：

- -- From list 来自列表

```applescript
set chosenList to list {"A", "B", "3"} with title
```

```applescript
List Title with prompt - "Prompt event" after "B" Ok name -- Looks Good! cancel name -
```

- 不，重试并允许空选择



## 脚本版本 (OSAX)

脚本版本是由 Apple 或第三方人员开发的 AppleScript 插件。它们被设计用于扩展内置的命令编辑器，扩大 AppleScript 的功能，并使其在某种程度上不再依赖于功能。例如，Apple 的 Standard Order Oscar 脚本增加了一组不属于 AppleScript 核心功能的命令和类 - 没有这个 `osax`（脚本扩展），AppleScript 将不具备显示对话框或导航服务的能力。

`constants`（常量） - 一种很少使用的整数和实数的通用基类。当你给变量赋值一个值时，它会被隐式调用，以检查该值是整数还是实数。

`on` 位于 "on" 的位置，并且可以写为接受标签参数，且不包含在括号内。AppleScript 中有四种预定义的处理器 - `run`、`open`、`idle` 和 `each`，其中每一个的执行方式与下面所示的 `run` 处理器相同：

## AppleScript 语言基础

### 类（数据类型）

AppleScript 拥有许多内置的（类或数据类型），尽管应用程序的运行很可能会为了其目的定义额外的数据类型。通用认可的各种数据类如下：

- `integer`（整数）
- `real`（实数）
- `date`（日期） - AppleScript 格式的日期。该类允许进行许多日期和时间操作。

定义脚本的主代码，在脚本运行时被调用。`run` 处理器是可选的，除非向脚本传递了参数。如果调用了脚本 `run` 处理器，所有包含在处理器块之外的代码都将像在隐式 `run` 处理器中一样执行。

- `alias`（别名） - 对文件系统对象（文件或文件夹）的引用。如果移动或重命名，`alias` 将保持其与对象的链接。
- `file`（文件） - 对文件系统对象（文件或文件夹）的引用。这是一个静态引用，可以指向一个不存在的对象。
- `POSIX` 类 - 纯文本文件系统对象（或文件夹）的引用，使用 Unix 风格的符号。

### Open 处理器

- `text`（文本） - 在 AppleScript 2.0 (Mac OS 10.5) 之前的 `text` 类与 `string`（字符串）和 `Unicode` 不同，三者的行为不同：在 2.0 及更高版本中，它们都是同义词并作为 Unicode 处理。
- `Container`（容器） - 一个可以包含任何类的列表对象，包括由应用程序和其他类型定义的。
- `list`（列表） - 对象的有序列表，每个对象由应用程序和其他类型定义。
- `record`（记录） - 项目的有序列表，每个项目的结构结构为键值对。

使用 "on ititems" 定义。

```
on repeat with items
tell updateitem
end repeat
```

- 基本对象
- `application`（应用程序） - 一个对象，通常指定为 `tell` 的目标（`tell application "..."`）。
- `script`（脚本） - 脚本对象。脚本对象是脚本的容器。每个 AppleScript 会创建一个脚本 `run` 对象，脚本对象可以由 AppleScript 创建。
- `class`（类） - 指定其他对象类型的元对象。
- `reference`（引用） - 指向不同对象的缩进指针。`'Reference to X'` 将返回 `X` 的当前值。

- 标准数据类型
- `boolean`（布尔） - 真/假值
- `constant`（常量） - 仅供开发者使用的类，指定一个常量。AppleScript 有许多预定义的常量 - `pi`、`tab`、`return` - 但允许定义为

当包含 `open` 处理器的脚本作为 drop（投放文件）被调用时，该 applelet 变成一个 drop。drop 在 Finder 中通过其图标识别，图标上有一个指向它的箭头。当项目被拖到 drop 上时，当文件或文件夹被拖到它上面，就会执行 `open` 处理器。然后这些项目将作为 `open` 处理器的参数传递给脚本。drop 也可以作为普通命令启动，执行其 `run` 处理器。

## Idle 处理器

系统在处理器空闲时执行的一段子程序。

## 语言

## 体内代码与代码块

以下为代码块的整合与格式化，代码块前后均使用三个反引号包裹：

```applescript
-- Alert 警报
set alertReply to display alert "Alert Text" with buttons ("Skip", "Okay", "Cancel") -
default button 2 --cancel button 1 -- giving up after 2
```

每种用户交互方法都可以返回点击按钮的值、用于进一步处理的项目或文本、类对象的“document”或 TIFF 的第 3 行第 7 像素 `my bitmap` paragraph——以及相应的动作——如“close”。系统还定义了引用对象属性的方法，因此可以引用“文档 Good Day 的第三段”，或最后一个前窗口的颜色。AEOM 使用应用程序字典将 Apple 事件与人类可读的术语关联，允许在人类可读的 AppleScript 和字节码之间来转换。

例如：

```applescript
display alert "Hello World!" buttons "Rudely click", "Happy accept"
set theAnswer returned of the result if theAnswer is "Happy accept" then beep else
```

在另一种编程语言中，这可以通过顺序方法调用实现：

```javascript
get("my bitmap").getPixel(3,7);
```

```applescript
say "Piffle!" if
```

AppleScript 包含了其他编码的语法，“第一段（first paragraph）”，以及序数，“类似段落（paragraph like）”，数字可以被视为文本或数值引用，“2”、“第五（fifth）”和“5”都由英语同义词支持。此外，可以在脚本的任何地方使用“the”来增强可读性；它对脚本的功能没有影响。

## 自然语言比喻

虽然 Apple 事件是向应用程序发送消息的方法，但 AppleScript 是一种为 Apple 事件设计的特殊语言。遵循 Mac OS 的使用传统，AppleScript 的设计基于自然语言比喻，就像桌面上的图形界面一样。一个编写良好的 AppleScript 应该足够清晰，供任何人阅读和理解，并容易编辑。这种语言很大程度上基于 HyperTalk，扩展后不仅可以指代单词卡片和栈，在理论上还可以指代文档。为此，AppleScript 引入了事件模型（AEOM），它规定了任何应用程序语言。

## AppleScript 开发工具

指定使用哪种应用程序。当执行 AppleScript 或点击记录按钮时，在任何支持 Apple 事件和 AppleScript 的应用程序中的任何用户操作都会被记录为 AppleScript 命令。生成的脚本可以保存并重新运行以复制原始操作，或进行修改以更具通用性。

AppleScript 元素在脚本字典中可见（作为应用程序的一部分分发），可以在任何脚本编辑器中查看。元素通常根据松散的功能关系分组在套件中。

`display dialog` "Hello! -- 带有“确定”和“取消”的模态窗口 -- 或 `display alert` "Hello! -- 带有“确定”按钮的模态窗口 -- 或 `say` "Hello! -- 使用合成语音的音频消息

AppleScript 具有多种接口选项，包括对话框、警报和“来自列表（from list）”。

```applescript
-- Dialog
set dialogReply to dialog "Text event" after answer text false
```

- `buttons` ("Skip", "Okay", "Cancel")
- `default button` -- "Okay"
- `cancel button` -- "Skip"
- `with title` --

```applescript
Dialog Title with icon note - giving up after 20
```

所有应用程序都提供免费的命令（通常称为脚本套件 `Script Suite`）——打开、保存文件、打印、退出、设置数据变量的命令——作为界面可脚本属性的基本对象。许多应用程序拥有能够执行脚本可以执行任何任务的套件。在特殊情况下，应用程序可能支持包含其脚本字典的插件。

AppleScript 设计用于通过记录操作立即处理脚本。当执行 AppleScript 或点击记录按钮时，计算机上的任何用户操作——在任何支持 Apple 事件和 AppleScript 的应用程序中——都会被记录为 AppleScript 命令。生成的脚本可以保存并重新运行以复制原始操作，或进行修改以更具通用性。

## Hello World!

在 AppleScript 中，传统的 Hello World! 程序可以用许多不同的形式编写：

- -- From list 来自列表

```applescript
set chosenList to list {"A", "B", "3"} with title
```

```applescript
List Title with prompt - "Prompt event" after "B" Ok name -- Looks Good! cancel name -
```

- 不，重试并允许空选择

```applescript
-- Alert 警报
set alertReply to display alert "Alert Text" with buttons ("Skip", "Okay", "Cancel") -
default button 2 --cancel button 1 -- giving up after 2
```

每种用户交互方法都可以返回点击按钮的值、用于进一步处理的项目或文本、类对象的“document”或 TIFF 的第 3 行第 7 像素 `my bitmap` paragraph——以及相应的动作——如“close”。系统还定义了引用对象属性的方法，因此可以引用“文档 Good Day 的第三段”，或最后一个前窗口的颜色。AEOM 使用应用程序字典将 Apple 事件与人类可读的术语关联，允许在人类可读的 AppleScript 和字节码之间来转换。

例如：

```applescript
display alert "Hello World!" buttons "Rudely click", "Happy accept"
set theAnswer returned of the result if theAnswer is "Happy accept" then beep else
```

在另一种编程语言中，这可以通过顺序方法调用实现：

```javascript
get("my bitmap").getPixel(3,7);
```

```applescript
say "Piffle!" if
```

AppleScript 包含了其他编码的语法，“第一段（first paragraph）”，以及序数，“类似段落（paragraph like）”，数字可以被视为文本或数值引用，“2”、“第五（fifth）”和“5”都由英语同义词支持。此外，可以在脚本的任何地方使用“the”来增强可读性；它对脚本的功能没有影响。

## 自然语言比喻

虽然 Apple 事件是向应用程序发送消息的方法，但 AppleScript 是一种为 Apple 事件设计的特殊语言。遵循 Mac OS 的使用传统，AppleScript 的设计基于自然语言比喻，就像桌面上的图形界面一样。一个编写良好的 AppleScript 应该足够清晰，供任何人阅读和理解，并容易编辑。这种语言很大程度上基于 HyperTalk，扩展后不仅可以指代单词卡片和栈，在理论上还可以指代文档。为此，AppleScript 引入了事件模型（AEOM），它规定了任何应用程序语言。

## AppleScript 开发工具

指定使用哪种应用程序。当执行 AppleScript 或点击记录按钮时，在任何支持 Apple 事件和 AppleScript 的应用程序中的任何用户操作都会被记录为 AppleScript 命令。生成的脚本可以保存并重新运行以复制原始操作，或进行修改以更具通用性。

AppleScript 元素在脚本字典中可见（作为应用程序的一部分分发），可以在任何脚本编辑器中查看。元素通常根据松散的功能关系分组在套件中。

可以将以下内容作为补充段落，说明具体的对话框和其他界面选项：

## 其他界面选项

在 AppleScript 中，除了上述基本命令，还可以通过以下方式实现不同的交互：

- `display dialog` "Hello! -- 带有“确定”和“取消”的模态窗口 -- 或 `display alert` "Hello! -- 带有“确定”按钮的模态窗口 -- 或 `say` "Hello! -- 使用合成语音的音频消息

```applescript
-- Dialog
set dialogReply to dialog "Text event" after answer text false
```

- `buttons` ("Skip", "Okay", "Cancel")
- `default button` -- "Okay"
- `cancel button` -- "Skip"
- `with title` --

```applescript
Dialog Title with icon note - giving up after 20
```

所有应用程序都提供免费的命令（通常称为脚本套件 `Script Suite`）——打开、保存文件、打印、退出、设置数据变量的命令——作为界面可脚本属性的基本对象。许多应用程序拥有能够执行脚本可以执行任何任务的套件。在特殊情况下，应用程序可能支持包含其脚本字典的插件。

AppleScript 设计用于通过记录操作立即处理脚本。当执行 AppleScript 或点击记录按钮时，计算机上的任何用户操作——在任何支持 Apple 事件和 AppleScript 的应用程序中——都会被记录为 AppleScript 命令。生成的脚本可以保存并重新运行以复制原始操作，或进行修改以更具通用性。

## Hello World!

在 AppleScript 中，传统的 Hello World! 程序可以用许多不同的形式编写：

- -- From list 来自列表

```applescript
set chosenList to list {"A", "B", "3"} with title
```

```applescript
List Title with prompt - "Prompt event" after "B" Ok name -- Looks Good! cancel name -
```

- 不，重试并允许空选择

```applescript
-- Alert 警报
set alertReply to display alert "Alert Text" with buttons ("Skip", "Okay", "Cancel") -
default button 2 --cancel button 1 -- giving up after 2
```

每种用户交互方法都可以返回点击按钮的值、用于进一步处理的项目或文本、类对象的“document”或 TIFF 的第 3 行第 7 像素 `my bitmap` paragraph——以及相应的动作——如“close”。系统还定义了引用对象属性的方法，因此可以引用“文档 Good Day 的第三段”，或最后一个前窗口的颜色。AEOM 使用应用程序字典将 Apple 事件与人类可读的术语关联，允许在人类可读的 AppleScript 和字节码之间来转换。

例如：

```applescript
display alert "Hello World!" buttons "Rudely click", "Happy accept"
set theAnswer returned of the result if theAnswer is "Happy accept" then beep else
```

在另一种编程语言中，这可以通过顺序方法调用实现：

```javascript
get("my bitmap").getPixel(3,7);
```

```applescript
say "Piffle!" if
```

AppleScript 包含了其他编码的语法，“第一段（first paragraph）”，以及序数，“类似段落（paragraph like）”，数字可以被视为文本或数值引用，“2”、“第五（fifth）”和“5”都由英语同义词支持。此外，可以在脚本的任何地方使用“the”来增强可读性；它对脚本的功能没有影响。

## 自然语言比喻

虽然 Apple 事件是向应用程序发送消息的方法，但 AppleScript 是一种为 Apple 事件设计的特殊语言。遵循 Mac OS 的使用传统，AppleScript 的设计基于自然语言比喻，就像桌面上的图形界面一样。一个编写良好的 AppleScript 应该足够清晰，供任何人阅读和理解，并容易编辑。这种语言很大程度上基于 HyperTalk，扩展后不仅可以指代单词卡片和栈，在理论上还可以指代文档。为此，AppleScript 引入了事件模型（AEOM），它规定了任何应用程序语言。

## AppleScript 开发工具

指定使用哪种应用程序。当执行 AppleScript 或点击记录按钮时，在任何支持 Apple 事件和 AppleScript 的应用程序中的任何用户操作都会被记录为 AppleScript 命令。生成的脚本可以保存并重新运行以复制原始操作，或进行修改以更具通用性。

AppleScript 元素在脚本字典中可见（作为应用程序的一部分分发），可以在任何脚本编辑器中查看。元素通常根据松散的功能关系分组在套件中。

## 脚本版本 (OSAX)

脚本版本是由 Apple 或第三方人员开发的 AppleScript 插件。它们被设计用于扩展内置的命令编辑器，扩大 AppleScript 的功能，并使其在某种程度上不再依赖于功能。例如，Apple 的 Standard Order Oscar 脚本增加了一组不属于 AppleScript 核心功能的命令和类 - 没有这个 `osax`（脚本扩展），AppleScript 将不具备显示对话框或导航服务的能力。

`constants`（常量） - 一种很少使用的整数和实数的通用基类。当你给变量赋值一个值时，它会被隐式调用，以检查该值是整数还是实数。

`on` 位于 "on" 的位置，并且可以写为接受标签参数，且不包含在括号内。AppleScript 中有四种预定义的处理器 - `run`、`open`、`idle` 和 `each`，其中每一个的执行方式与下面所示的 `run` 处理器相同：

## AppleScript 语言基础

### 类（数据类型）

AppleScript 拥有许多内置的（类或数据类型），尽管应用程序的运行很可能会为了其目的定义额外的数据类型。通用认可的各种数据类如下：

- `integer`（整数）
- `real`（实数）
- `date`（日期） - AppleScript 格式的日期。该类允许进行许多日期和时间操作。

定义脚本的主代码，在脚本运行时被调用。`run` 处理器是可选的，除非向脚本传递了参数。如果调用了脚本 `run` 处理器，所有包含在处理器块之外的代码都将像在隐式 `run` 处理器中一样执行。

- `alias`（别名） - 对文件系统对象（文件或文件夹）的引用。如果移动或重命名，`alias` 将保持其与对象的链接。
- `file`（文件） - 对文件系统对象（文件或文件夹）的引用。这是一个静态引用，可以指向一个不存在的对象。
- `POSIX` 类 - 纯文本文件系统对象（或文件夹）的引用，使用 Unix 风格的符号。

### Open 处理器

- `text`（文本） - 在 AppleScript 2.0 (Mac OS 10.5) 之前的 `text` 类与 `string`（字符串）和 `Unicode` 不同，三者的行为不同：在 2.0 及更高版本中，它们都是同义词并作为 Unicode 处理。
- `Container`（容器） - 一个可以包含任何类的列表对象，包括由应用程序和其他类型定义的。
- `list`（列表） - 对象的有序列表，每个对象由应用程序和其他类型定义。
- `record`（记录） - 项目的有序列表，每个项目的结构结构为键值对。

使用 "on ititems" 定义。

```
on repeat with items
tell updateitem
end repeat
```

- 基本对象
- `application`（应用程序） - 一个对象，通常指定为 `tell` 的目标（`tell application "..."`）。
- `script`（脚本） - 脚本对象。脚本对象是脚本的容器。每个 AppleScript 会创建一个脚本 `run` 对象，脚本对象可以由 AppleScript 创建。
- `class`（类） - 指定其他对象类型的元对象。
- `reference`（引用） - 指向不同对象的缩进指针。`'Reference to X'` 将返回 `X` 的当前值。

- 标准数据类型
- `boolean`（布尔） - 真/假值
- `constant`（常量） - 仅供开发者使用的类，指定一个常量。AppleScript 有许多预定义的常量 - `pi`、`tab`、`return` - 但允许定义为

当包含 `open` 处理器的脚本作为 drop（投放文件）被调用时，该 applelet 变成一个 drop。drop 在 Finder 中通过其图标识别，图标上有一个指向它的箭头。当项目被拖到 drop 上时，当文件或文件夹被拖到它上面，就会执行 `open` 处理器。然后这些项目将作为 `open` 处理器的参数传递给脚本。drop 也可以作为普通命令启动，执行其 `run` 处理器。

## Idle 处理器

系统在处理器空闲时执行的一段子程序。

## 语言



许多 AppleScript 示例由代码块进行管理，例如，一个块以命令开始并以 `end` 语句结束。使用 "on - end" 块的一种变体是定义处理器（子程序）。以`function(name)`开始并以`endName`结束的处理器，除非从脚本中调用，否则不会作为脚本的一部分执行。处理器也可以使用`to`定义。

- `RGB color` 颜色 - 一个 RGB 三元组，用于命令和工作中的颜色。
- `unit type`（单位类型） - 连接标准单位的类。例如，一个值被定义为平方码，并报告为平方英尺。

`idle`处理器可以在对象或 `droplets` 中作为保持打开的处理器（`stay-open handlers`）。

```
-- 脚本执行完成后执行的代码
return 60 -- 在执行 idle 处理器之前暂停的秒数
gain idle
end idle
```

`set variable1 to 1` – 创建一个名为`variable1`的整数

`set variable2 to "Hello"` – 创建一个名为`variable2`的文本

`set {17,double} to variable3` – 创建一个名为`variable3`的列表

`set {variable4,5} to variable5` – 创建一个由`variable4`隔开的项目列表，用于监听特定数据事件的脚本。默认空闲时间为一秒，可以通过在脚本末尾包含`return`语句来更改，其中`x`是处理器产生如 QuickKeys 和等于 Apples 状态之前应该等待的秒数。脚本作为脚本组件实现的，以及使用系统其他开发人员实现此类组件的基础。对于加载和复制脚本，所有组件的效果都相同。

## Quit 处理器

处理器是在接收到请求运行时运行的。

```
on quit
```

## 计算平均值

```
func findavg($nums)
    StringTrimRight($nums, 1)
    If InStr($nums, ",") < 1
        ; 计算用户指定的数字的平均值。
        ; 数字必须用逗号分隔。
        Return("malform1")
    EndIf

    $sData = StringSplit($nums, ",")
    $Sans = 0
    For $Si = 1 To $sData[0]
        $Sans += Number($sData[$Si])
    Next
    
    $Sans = $Sans / $sData[0]
    Return ($Sans)
EndFunc
```

```
#NoTrayIcon
#include <GUICConstantsEx.au3>
#include <Array.au3>
#region--------------------GUI
```

```
$form = GUICreate("平均值查找", 300, 100)
$Label = GUICreateLabel("输入用逗号分隔的数字,", 19, 20)
$textbox = GUICreateInput("", 20, 20, 220)
$Label2 = GUICreateLabel("=", 245, 20, 30, 20)
$Label3 = GUICreateLabel("总计:", 255, 50, 50, 20)
$Button = GUICreateButton("查找平均值", 100, 40)
$GUISState(@SW_SHOW)
#endregion--------------------GUI
```

```
While 1
    $msg = GUIGetMsg()
    If $msg = GUIC_EVENT_CLOSE Then Exit
    If $msg = $Button Then
        $result = findavg(GUIGetControl($textbox))
        If $result = "malform1"
            GUICSetData($SansLabel, "错误")
        Else
            GUICSetData($SansLabel, $result)
        EndIf
    EndIf
Wend
```

## 历史

- 1998年12月 - 能够发送按键的C程序想法
- 1999年1月 - 第一版 AutoIt (1.0)
- 1999年8月 - AutoIt v2 和 v3
- 1999年9月 - 第一个带有编译器的 AutoIt 版本
- 2002年12月 - AutoIt v3 (公共测试版)
- 2004年2月 - AutoIt v3 (稳定版)
- 2006年9月 - Auto3Lib启动
- 2007年11月 - 发布 AutoIt v3.2.10.0，Auto3Lib 并入 AutoIt v3
- 2008年5月 - 发布 AutoIt v3.2.12.0，包含新增的 GUI 功能
- 2008年12月至2009年12月 - 发布 AutoIt v3.3.2.0
- 2010年1月 - 发布 AutoIt v3.4.0.0
- 2010年3月 - 发布 AutoIt v3.3.6.0
- 2010年4月 - AutoIt v3.3.6.1

AutoIt 的开发者最初根据 GPL 许可证发布了源代码，但该做法在 2006 年 8 月的 3.2.0 版本后停止了。3.1 版本的部分代码被 AutoHotkey 项目用于创建一个分支，社区在该项目中继续以 GPL 协议开发代码。

来源（已编辑）："http://en.wikipedia.org/wiki/AutoIt"

## AutoLISP

AutoLISP 是 Lisp 编程语言的一种变言，专门为 AutoCAD 完整版及其衍生版本构建，包括 AutoCAD Map 3D、AutoCAD Architecture 和 AutoCAD Mechanical。执行 AutoLISP 的解释器均未包含在 AutoCAD 产品线中。

; AutoLisp 函数定义，可从其他 AutoLISP 函数调用：

```
(defun hello ()
  (alert "Hello World!")
)
```

: 函数也可以在命令行中作为普通的 AutoCAD 命令被调用：

```
(defun c_hello ()
  (alert "Hello World!")
  (princ)
)
```

## 特性

AutoLISP 是一种小型的、动态缩放的、通常强类型的 LISP 变言，具有垃圾回收机制、不可变符号，并将常规 LISP 特性标记为记录设施、变长参数数组或列表。从核心逻辑来看，最强大的函数用于几何图形、访问 AutoCAD 内部 DWG 数据库以及操作 AutoCAD 中的图形实体。向 AutoLISP 暴露的作为关联列表形式的属性与 AutoCAD 的“组”代码配对，这些代码用于识别属性点、半径、颜色、图层等。AutoCAD 从文件中加载 AutoLISP 代码。

: AutoLISP 条件语句的示例：

```
(cond (a = b)
      (princ "\n(a) 和 b 相等")
      (and (= type a) 'INT)
            (= type b) 'INT)
            (strcat "\n(a)+b" (itoa a)))
      (and (= type a) 'STR)
            (= type b) 'STR)
            (strcat "\n(a)+b" a))
      (and (list a (= type b) 'SUB)
            (mapcar function (lambda x)
              (print b x)) a))
```

David Betz 创建的 XLISP 版本。该语言于 1986 年 1 月引入 AutoCAD 2.18，并在后续的发布中一直发布到 Release 13 in-AutoLISP。

The-Babel 在 2006 年获得了 R&D 100 奖。它已应用于多种领域，如加速器动力学、生物学、化学、分子、电子、地磁、材料、核电站、无线电天文学和传输物理学，作为框架、网格化、求解器等。

## 基础库 (Base Foundation Library)

基础基金库 (BFC) 是一种用于在 Windows 和 .NET 上构建安全、容错数据库应用程序的工具包。与微软的虚拟开发环境相结合，BFC 提供了处理 Microsoft、Oracle、IBM、MySQL 数据库的通用应用程序框架，并运行。BFC 还包含了分布式计算、批处理、查询以及数据库和可维护性功能。BFC 对其核心技术拥有多项美国专利，申请正在中。

## 工作原理

BFC 基于一种以数据为中心的架构，该架构在支持数据安全、估值、优化方面起着核心作用。

BFC 运行在 t-X 网格（表格）、组合和编辑控件。随着 VisualStudio .NET 2002 的出现，BFC 扩展到支持 .NET 语言，如 C#、VB.NET 和 ASP.NET。

# 许可

Base One International Corp. 提供多个级别的 BFC 产品，这两者都提供示例和完整源代码：

- BFC Personal：单人开发者
- license 站点许可
- BFC Enterprise：站点许可（已编辑）："http://en.wikipedia.org/wiki/Base_Foundation_Component_Library"

# Bash (Unix 壳)

Bash 是由 Brian Fox 为 GNU 项目编写的一种 shell，作为 Bourne shell (sh) 的免费替代品。1989 年，它通过 GNU 操作系统广泛分发，并成为 Linux、Mac OS 的默认 shell，且已通过 Cygwin 和 MinGW 移植到 Microsoft Windows。GNU 代码是他们自己参与的少数几个项目之一，当时 Fox 是 FFS 的员工。Bash 于 1989 年 6 月以 Beta 版发布，并一直保持主要维护者身份直到 1994 年中期，当时他被解雇，责任转给了另一位作者。

Bash 是一个命令处理器，允许输入文本来创建命令。Bash 像所有 shell 一样也可以从文件中读取命令，支持通配符扩展、管道、注释和控制结构。其关键字和其他功能全部复制自 sh。

## 特性

Bash 的语法与 Bourne shell 相似。大多数 shell 脚本都由 Bash 执行，使用变量扩展的脚本除外（其行为可能不同）。Bash 包含了来自 Korn shell (ksh) 和 C shell (csh) 的项，如历史记录、目录栈 (PWD) 和命令替换 ($...)。当使用交互式 shell 并按下 Tab 键时，自动补全使用行完成来匹配输入的模式名称，Bash 命令行非常灵活，通常填充了用于特定任务的参数。

Bash 提供了 Bourne shell 一直以来提供的帮助。从 2.0 版本开始，Bash 能够使用 `<<` 从“此处字符串”重定向标准输入 (stdin)。兼容 POSIX 的 Bash 几乎是完美的。这个名字是一个缩写，代表 Bash Again Shell，即 Bourne shell 的免费替代品。作为一个双关语，它用一个看起来再次相同的短语表达了目标，同时也描述了它的所作。

Bash 3.0 支持内置正则表达式匹配，让人想起 Perl。Bash 4.0 支持关联数组，并允许多维数组，方式类似于。Fox 在 1988 年 1 月开始编码，在此之前 Richard Stallman 对没有由真正的开发者创建该项目感到不满。自由软件基金 (FSF) 认为这是一个可以运行脚本的、完全自由的 shell。Bash 的语法有许多扩展，允许在不产生外部进程的情况下进行计算，与 Bourne shell 不同。Bash 使用 `((...))` 命令和 `$...)` 变量进行语法。

# Bash 扩展

Bash 扩展也称为交替（alternation），是 C shell 的一项功能，用于生成替代组合。生成的可能可能。每个扩展字符串的结果经过排序，从左到右的顺序为：

```
echo (a,b,d) # e ace ade b
echo {a,c}(d,f) # ad ae af bd dc ce
```

Bash 扩展不应在可移植的 shell 脚本中使用，因为 Bourne shell 不产生相同的输出：

```
echo (jpg,jpg,png) # * {a,p,d,b}
```

当扩展与通配符结合时，大括号首先扩展，然后正常替换结果产生的通配符。因此，将获得当前目录下的 JPEG 和 PNG 图像列表：

# 启动脚本

当 Bash 启动时，它执行各种不同脚本中的命令。当 Bash 作为交互式 shell 调用时，如果存在，它会执行 `/etc/profile` 中的命令。读取后它按顺序查找 `~/.bashrc` 和 `~/.profile`，并执行第一个存在且可读的命令：

当登录 shell 启动时，Bash 读取并执行 `~/.bash_profile` 中的命令。如果启动的是非登录 shell，Bash 读取并执行 `~/.bashrc` 中的命令（如果该文件存在且可读）。通过使用 `-file` 选项，将强制 Bash 读取并执行来自 `~/.bashrc` 的命令。某些版本的 Unix 有自定义 Bash 脚本，通过过早加载或继续执行 Bash 启动脚本会违反执行 `~/.bashrc` 的顺序。

# 可移植性

带有 Bash 特有功能（bashisms）的 shell 脚本在运行 Bourne shell 或任何替代品的系统中无法工作，除非 Bash 以“shebang”行 `/bin/sh` 开始。

# 键盘快捷键

快捷键使用默认的 Emacs 键绑定。可以通过设置 `-vi` 启用绑定。



# 常用快捷键

- 从光标位置自动补全
- `Ctrl+a` 移动到行首（`home` 键）
- `Ctrl+e` 将光标移动到行尾（`end` 键）
- `Ctrl+_`（上）调用上一个命令（`f` 键）
- `Ctrl+n`（下）调用下一个命令（`j` 键）
- `Ctrl+r`（搜索）调用上一个命令。第二个 `Ctrl+r` 跳到最近的命令（`exit` 键）。
- `Ctrl+l` 清屏（`clear` 键）。
- `Ctrl+u` 删除光标之前的行并复制到剪贴板。
- `Ctrl+k` 删除光标后的行并复制到剪贴板。
- `Ctrl+c` 删除光标后的行并复制到剪贴板。
- `Ctrl+s` 进入 EOF 标记。
- `Ctrl+d` 删除光标后的字符（`d` 键）。
- `Ctrl+w` 删除光标之前的单词并复制到剪贴板。
- `Ctrl+y` 从当前位置添加剪贴板内容。
- `Alt+f`：（向前）移动一个单词的。
- `Alt+b`：（向后）移动一个单词的。
- `Alt-d`：删除光标之前的单词。
- `Alt+u`：从光标位置到行尾的所有字符大写。
- `Alt+-`：将下方字符小写并移动到行尾。
- `Alt+`：将下方字符大写并移动到行尾。
- `Ctrl+q`：（`fg`）如果你更改了它，使用 `Ctrl+q` 返回。
- `Ctrl+c`：向当前任务发送 `SIGINT`，将其挂并关闭。
- `Ctrl+z`：向当前任务发送 `SIGTSTP`，将其挂并关闭。
- `declare -A`：声明关联数组 `a`
- 初始化 `indices=1; j=2`
- 关联值 `"5"`
- 在键处打印字符串

# 批处理文件

在 DOS、OS/2 和 Windows 中，批处理文件是包含一系列命令的文本，由命令解释器执行。与其他系统的作业控制类似，批处理文件允许用户设置批处理脚本执行许多命令。当调用批处理文件时，shell（通常是 `COMMAND` 或 `cmd.exe`）读取它并逐行执行其命令。批处理文件用于自动运行一系列事件，通常用于自动化重复或繁琐的操作（如 Linux 有不同类型的文件称为脚本）。

# 变体

在 MS-DOS 中，可以通过命令行输入其名称（带有任何必要参数）并按下“回车”键启动批处理文件。MS-DOS 会自动加载并执行 `AUTOEXEC` 文件，因此任何需要在 MS-DOS 环境使用的命令都可以放在此文件中。计算机用户使用 `autoexec` 文件设置系统日期和时间、MS-DOS 环境、加载任何必要的程序或驱动程序或初始化网络连接。

# DOS

在 MS-DOS 中，`bat` 文件可以由命令解释器 `COMMAND` 执行，通过逐行运行，就像输入的命令列表一样，带有额外的批处理命令用于基本编程功能，并使用 `GOTO` 命令更改执行流。

# 早期 Windows

Microsoft Windows 在 95 年引入，作为文本界面操作系统的 GUI 操作系统替代品，并运行在 MS-DOS 上。为了启动 Windows，使用了 `WIN` 命令并添加到 `AUTOEXEC.BAT` 文件的末尾以实现自动加载。在早期版本中，可以从 MS-DOS 提示符运行 Windows，或直接从启动硬盘运行不基于 MS-DOS 的 Windows NT。为了替换 `COMMAND`，同样的方式引入了 `exe` 以及批处理文件，并使用了与 `COMMAND.COM` 略不同的命令，这意味着新的 `cmd.exe` 不兼容供 `COMMAND` 使用的其他批处理文件。Microsoft 为 Windows 95 和 ME 发布了 `cmd.exe` 版本，允许其他版本的 Windows 用户使用 `cmd.exe` 风格的文件。目前，`cmd.exe` 是 Windows NT 中批处理文件的命令解释器。

# 文件名扩展

- `.1`, `.2`, `.3`
- `.95` 和 `.98`
- `.ME`（限制访问 MS-DOS 内存）。

# OS/2

OS/2 操作系统使用 风格的批处理文件。它还包含 REXX 版本，这是一种更高级的批处理脚本语言。IBM 和 Microsoft 使用块结构分割后开始开发此，结果 IBM 将其称为类 MS-DOS 的 shell 而没有提到 Microsoft；尽管 MS-DOS 也没有影响批处理文件的工作方式。OS/2 的批处理解释器还支持 `EXPROC` 命令，它会将批处理文件传递给命名的提示符。命名的提示符可以是脚本文件；类似于 `#!`。

# Windows NT

除 NT MS 家族操作系统外的 Windows 版本运行于 MS-DOS，并使用相同的解释器 `COMMAND` 来执行批处理文件。然而，操作

- `.bat`：Microsoft 用于批处理文件的第一个扩展名。该扩展在 MS-DOS 和所有版本的 Windows 下通过 `COMMAND` 或 `cmd.exe` 运行，尽管命令解释器解释批处理文件的方式不同。
- `.cmd`：Windows NT 家族操作系统使用的扩展名，并发送进行解释。它在依赖 `COMMAND` 防止 `cmd.exe` 在错误环境中环境中计算机上无法工作。
- `.btm`：`4DOS` 和 `4NT` 脚本使用的扩展名运行速度更快，特别是较长的脚本，因为脚本确实已经准备好执行，而不是逐行执行。

## 批处理文件 - 第33 页

## 高级批处理示例 - 条件关机

当启用命令扩展时，而在 `.bat` 文件中 `ERRORLEVEL` 变量仅在发生错误时发生变化。

```
IF "%var%"==bar ECHO Correct.
```

处理此情况的典型方法是始终对被测试的变量加上引号，或者在评估的两侧使用其他固定不变的字符。例如，这些测试在语法上是正确的，如果 `%var%` 包含一个值，它们将评定为 `False`（假）。

## 示例

```batch
@echo off
color 3
title 条件关机
set /p=enter a name:
```

此示例文件是一个简单的程序，它显示一个问候程序并等待用户按键结束。

```batch
@start
cls
echo Hi, %name%
echo 1.Shutdown
echo 2.Quit
```

```batch
@ECHO OFF
ECHO Hello World!
PAUSE
@ECHO on
```

```batch
:invalid
set /p=enter your choice: 1,2
if %choice%==1 goto shutdown
if %choice%==2 goto invalid
echo invalid: %choice%
```

要执行此文件，必须将其保存为 `.bat` 或 `.cmd` 扩展名（可以使用记事本等程序）。

```batch
IF "%var%"==bar ECHO Correct.
IF 1==1bar ECHO Correct.
```

## 结果

如果被测试的变量包含多个单词且未加引号，则测试在语法上也会失败。例如，`%var%` 中的值 `"bar baz"` 会导致最后一个命令被解析为：

当执行（从 Windows 资源管理器或命令提示符）时，会显示以下内容：

```batch
:shutdown
set /p=enter the number of seconds
that you choose to shutdown:
set /p=cancel to stop shutdown
message you to display:
secho -s -f -t %sec% -c "%name"
echo initiated at %time%
if %cancel%==1 cancel-shutdown exit
if %cancel%==2 goto start
```

```batch
1bar baz===1 ECHO Correct.
```

Hello World!

Press key to continue ...

可以使用延迟 `!VARIABLE!` 扩展来避免这些语法问题。在 Windows 2000/XP/Vista/7 中，变量不会发生语法错误，因为变量将在执行 `IF` 命令后进行扩展：

## 解释

解释器从每一行开始执行，从第一行开始`%`。`%`符号在行首关闭了该命令的提示符。`ECHO` 立即关闭提示符，或者直到下一行将其开启。然后是 `Hello World!` 只有 `off` 和 `on` 函数。接着是名为 `PAUSE` 的命令，它会暂停脚本的执行，并显示 `Press key to continue ...`。按下按键后，脚本继续到下一行 `ECHO`，它会返回提示符供使用。然后到达脚本末尾并停止。如果脚本从命令提示符启动，它将保持在提示符状态。如果脚本从 Windows 启动，则使用窗口将会关闭。

```batch
IF "!!var!"=bar ECHO Correct.
```

## 局限性 / 异常

#### 空字符串中的引号

#### 变量中的空值

如果命令中的变量包含空值，某些命令可能会发生语法错误并终止脚本。如果 `%var%` 的值是 1 个字符且不包含空格，则此测试将正常工作：

- 对于某些命令，空格被视为命令中的分隔符，除非它们被引号括。单个引号（`"`）不包含在字符串中。然而，转义引号（`""`）是字符串的一部分。对于其他命令，空格被视为分隔符且不加引号。如果包含了引号，它们就是字符串的一部分。

```batch
IF "%var%"==bar ECHO Correct.
```

但如果 `%var%` 的值为空，则该命令将被评定为命令：

## 34 - 批处理文件

```cmd
C:> set foo
```

```cmd
C:> set foo="string is enclosed in quotes"
```

```cmd
C:> Echo %foo%
```

"string is enclosed in quotes"""

```

```cmd

C:> Eventcreate /T Warning /ID 1 /L /SO "D" /```
```

在 Windows 2000/XP/Vista/7 下，解决方案是对一个字符进行搜索并替换：

```cmd
C:> set foo=""""
```

```cmd
C:> Echo %foo%
```

"""string is enclosed in quotes"""

```

```cmd

C:> set foo=%%f:"""
```

```cmd

C:> Echo %foo%

```
"""string is enclosed in quotes"""
```

```cmd
C:> set foo=%%f00"""
```

```cmd
C:> Echo %foo%
```

"""string is enclosed in quotes"""

```

```cmd

C:> set foo=%%f00%%

```

```cmd

C:> Echo %foo%

```
```

### 字符串中的转义字符

某些字符在命令行具有特殊含义，例如管道符 `|`。除非使用符号 `^` 进行转义，否则无法使用 `ECHO` 命令打印：

```cmd
C:> Echo ^| bar
'bar' is not recognized as an internal or external command, operable or batch file
```

```cmd
C:> ^| bar
|
```

然而，转义在将转义字符扩展到环境变量时不起作用，且当仅显示包含管道的变量时。有必要转义符号本身以便在变量中显示：

```cmd
C:> set foo^|^ bar
'bar' is not recognized as an internal or external command, operable or batch file.
```

```cmd
C:> set foo^|^ bar
C:> echo %foo%
```

|

```

```cmd

C:> set foo^|^ bar

C:> echo %foo%

```
|
```

## BeanShell

BeanShell 是一种 Java 脚本语言，由 Patrick Niemeyer 发明。它运行在 Java 运行环境 (JRE) 中，除了脚本内容和语法外，还使用 Java 语法。虽然 BeanShell 允许用户定义可以在脚本内部调用的函数，但其底层哲学一直是通过过多的扩展和“语法糖”来污染其语法，确保 Java 编译器的代码几乎可以在不进行任何更改的情况下被 BeanShell 解释性地执行，反之亦然。

BeanShell 是一种流行的测试和调试工具。

BeanShell 支持将对象作为简单的方法闭包，类似于 Perl 和 JavaScript 中的闭包。

BeanShell 是一个开源项目，已集成到许多应用程序中，例如 OpenOffice.org、Apache Ant、WebLog Server Application Editor、JUMP GIS、Scripting Environment 等。BeanShell 提供了一个易于集成的 API。它也可以在命令行模式或在其自身的图形化环境中使用。

BeanShell 已通过 Java 社区进程 (JCP) 成为 JSR 274 的标准。

在 2005 年 JCP 批准 BeanShell JSR 投票案后，BeanShell 并没有发生过明显的活动。JSR 274 处于“非活跃”状态。

BeanShell 的一个分支 BeanShell2 于 2007 年 5 月在 Google Code 网站上创建。beanshell2 项目对 BeanShell 有更多的修复和增强。

来源（已编辑）："http://en.wikipedia.org/wiki/BeanShell"

## Bean Sheet

![](img/28b49089ea8cf20e1b8f2972fae5fffa_37_0.png)

Bean Sheet 是一个基于 BeanShell 的电子表格。由于它使用了 BeanShell，它与 Java 库以及 Bean 代码具有完全的可操作性。因此，BeanSheet 结合了过程编程、面向对象编程和函数式编程的特性。它的语法与传统的电子表格略有不同，最显著的是使用 `[... ]` 表示单元格和范围。

来源（已编辑）："http://en.wikipedia.org/wiki/Bean_Sheet"

## BnuGD

BnuGD（称为 Game Development 或 Bennu）是一个高级开源视频游戏开发套件，最初由 Argentine Splitter 作为 Fenix Project 的分支创建。它正式支持 Windows、Linux 和 GPZX，但在某种程度上也支持多个平台，包括 FreeBSD、Mac OS X 以及 GP2X、Dingo A32 和 Wii 等控制机。最近，Fuseki Games 已将另一个 SplitGU 移植到 Sega Dreamcast 上，并可以开始将其移植到 Bennu。

BnuGD 专注于模块化，让初学者和有经验的用户都能轻松创建自己的游戏。该项目由 Argentine Splitter 在与 Fenix Project 社区产生分歧后创建。

## 目录

BnuGD 是一个控制应用程序。有几个集成开发环境 (IDE) 可用，但没有官方支持的。该包包含一个编译器、运行时代码以及扩展核心功能的不同共享库。

## 媒体报道

2010 年，关于 BnuGD 的两部分系列文章的第一部分发表在西班牙语 TodoLinux 杂志上。2010 年 2 月，发表了第二部分。

来源（已编辑）："http://en.wikipedia.org/wiki/BnuGD"

## 历史

BnuGD 作为 Fenix Project 创建的。

## Bistro (编程语言)

Bistro 编程语言是面向对象、动态类型和反射的。它旨在整合 Smalltalk 和 Java 的特征，作为运行在任何 Microsystems Java 规范上的 Smalltalk Java 虚拟机变体。自 2002 年以来，Bistro 没有新的进展。

Bistro 重复了 Smalltalk 的绝大部分语法和 API，并引入了 Java 的包和导入概念。重载运算符是可用的：`++` 和 `-` 不是重载运算符。

声明类的包句和导入句的语法为：

`package:my.package.subpackage; import:my.package.MyClass; import:my.package.*;` 其中一个例外是能够从其他类中导入静态方法。

来源（已编辑）："http://en.wikipedia.org/wiki/Bistro_(programming_language)."

## Bourne shell

Bourne shell（或 `sh`）是 Version 7 的默认 Unix shell 以及 Thompson shell，后者的可执行文件具有相同名称，也称为 `sh`。它由 AT&T 贝尔实验室的 Stephen Bourne 开发，并在 1977 年在发布给国家和大学的 Version 7 中重新发布。它仍然是 Unix 账户流行的 shell。Bourne 或类似 shell 的二进制程序是默认值，并为现代 Unix 系统上的超级用户设计。它的命令解释器包含了用于生成结构化程序的所有功能。尽管它被用作交互式解释器，但它一直被设计为一种脚本语言。随着 Brian W. Kernighan 和 Rob Pike 出版《Unix 环境》，它变得流行。这是第一本商业出版的、以教程格式描述编程语言的书籍。

- 在解释 shell 时对字符串长度没有限制。
- 逻辑化并泛化字符串引用机制。
- 环境机制。

它的命令解释器包含了所有用于生成结构化程序的常用功能。尽管它被用作交互式解释器，但它一直被设计为一种脚本语言。它随着 Brian W. Kernighan 和 Rob Pike 出版《Unix 环境》而获得流行。这是第一本商业出版的、以教程格式描述编程语言的书籍。

- 在解释 shell 时对字符串长度没有限制。
- 合理化并泛化字符串引用机制。
- 环境机制。

它的命令解释器包含了所有用于生成结构化程序的常用功能。尽管它被用作交互式解释器，但它一直被设计为一种脚本语言。它随着 Brian W. Kernighan 和 Rob Pike 出版《Unix 环境》而获得流行。这是第一本商业出版的、以教程格式描述编程语言的书籍。

- 在解释 shell 时对字符串长度没有限制。
- 合理化并泛化字符串引用机制。



### Bourne shell

Bourne shell，或 `sh`，是 Version 7 的默认 Unix shell 以及 Thompson shell，后者的可执行文件具有相同名称，`sh`。它由 AT&T 贝尔实验室的 Stephen Bourne 开发，并在 1977 年在发布给国家和大学的 Version 7 中重新发布。它仍然是 Unix 账户流行的 shell。Bourne 或类似 shell 的二进制程序是默认值，并为现代 Unix 系统上的超级用户设计。它的命令解释器包含了所有用于生成结构化程序的常用功能。尽管它被用作交互式解释器，但它一直被设计为一种脚本语言。它随着 Brian W. Kernighan 和 Rob Pike 出版《Unix 环境》而获得流行。这是第一本商业出版的、以教程格式描述编程语言的书籍。

- 在解释 shell 时对字符串长度没有限制。
- 合理化并泛化字符串引用机制。

#### 环境机制

它的命令解释器包含了所有用于生成结构化程序的常用功能。尽管它被用作交互式解释器，但它一直被设计为一种脚本语言。它随着 Brian W. Kernighan 和 Rob Pike 出版《Unix 环境》而获得流行。这是第一本商业出版的、以教程格式描述编程语言的书籍。

- 2009 年 3 月，允许从其他类中脚本传递参数。
- 它的命令解释器包含了所有用于生成结构化程序的常用功能。尽管它被用作交互式解释器，但它一直被设计为一种脚本语言。
- 脚本可以以文件名调用。
- 脚本。
- 命令替换使用反引号：`''`。

### Descendants

Korn shell (`ksh`) 由 David Korn 编写，更像 Bourne shell 和 C shell。

由于版权原因，Bourne Shell 在 CSRG 版本中使用过，Kenneth Almquist 开发了 Bourne Shell 的一个克隆，被某些称为

### Quotes

来源（已编辑）："http://en.wikipedia.org/wiki/Bourne_shell"

### Cscript

Cscript 是 ColdFusion 上的 JavaScript 扩展。Cscript 类似于 ColdFusion，因为它比普通的 CFML 有更视觉和排版开销；唯一的更改体现在代码中（普通的 CFML 会包含 `CFSET` 标签）。

```
xParam = 115;
yParam = 200;
color = 'FCFF99';
```

```
</cscript>
```

所有的 Cscript 代码必须包含在 `Cscript` 标签内，如下：

虽然许多 ColdFusion 标签都有相应的 Cscript 类比，但仍有许多没有。这些复杂的标签很难复制，而简单的 Cscript 标签很容易模仿（使用 ColdFusion UDF）：复杂的：

```
<cffile>
<directory>
<cfdump>
<ethrow>
```

来源（已编辑）："http://en.wikipedia.org/wiki/CFscript"

```
<cscript>
```

### CHAIN (编程语言)

CHAIN 是 Datapoint 在 20 世纪 80 年代后期使用的批处理编程语言。

来源（已编辑）："http://en.wikipedia.org/wiki/CHAIN_programming_language"

### CMS EXEC

CMS EXEC，或 `EXEC`，是一种解释型的、命令控制、计算机编程语言，用于与

### COFFEE (Cinema 4D) - 第 39 页

由 IBM 虚拟机/对话系统监视器 (`VM/CMS`) 操作系统提供的 `EXEC` 处理器。

- REXX

源码（已编辑）："http://en.wikipedia.org/wiki/CMS_EXEC"

CMS EXEC 已被 `EXEC 2` 和 `REXX` 取代。CMS EXEC、`EXEC 2` 和 `REXX` —— 继续

#### 相关命令处理器语言控制

- REXX
- EXEC 2

### COFFEE (Cinema 4D)

COFFEE（通常写为 "C.O.F.F.E.E"）是一种计算机脚本语言，是 CINEMA 4D（一种 3D 图形应用程序）的一部分。虽然作为缩写，COFFEE 的字母似乎并不代表任何含义，而是对 Java（一种更为盛名的语言）的幽默引用，CINEMA 4D 的操作可以通过 COFFEE 脚本进行自定义，特别是针对用户界面、读取和读写新文件格式的扩展以及创建纹理着色器。应用程序的所有主要功能都可以通过 COFFEE 程序访问，某些自定义功能看起来和表现得像标准功能一样。

通常不需要担心它。然而，在必要时可以显式地控制该过程。

3D 图形编程利用某些数学技术，特别是三角法和向量算术。COFFEE 在这方面非常强大，拥有一组良好的数学函数和内置语言数据类型。

#### 目的

与大多数脚本语言一样，COFFEE 用于扩展或修改软件的功能。出于许多原因，这种技术比使用 C 等传统语言编写所谓的“插件”更优越：

- 脚本语言会代表用户处理内存管理，而 C 不会；
- 解释器不需要在程序使用之前作为独立步骤对其进行编译；
- 特别构建的脚本语言可以进行定制以适应其预期用途。例如，COFFEE 内置了 3D 图形所需的数学函数。

COFFEE 是一种相当奇的回调语言，任何以前使用过 C++、Perl 或类似语言的用户都会觉得很熟悉。函数和对象类的定义紧密模仿 C++。然而，COFFEE 是动态类型，允许在不引用其类型的情况下使用简单变量。

#### 与 CINEMA 4D 的接口

由于 COFFEE 用于扩展 CINEMA 4D，它显然需要在某种程度上使用宿主程序。通过应用程序编程接口 (API)，可以定位 3D 对象并访问其内部数据结构。例如，可以从脚本创建、修改或扭曲新对象。COFFEE 的主要目的是允许使用新的布局形式，COFFEE API 为该任务提供了很有用的函数；可以使用文件/输出类，该类处理读取和写入的所有单个数据项（如整数和浮点数）。

COFFEE 的内存管理完全由垃圾回收过程处理；本质上这意味着它会自动管理自己，程序源码（已编辑）："http://en.wikipedia.org/wiki_(Cinema_4D)"

### COMMAND.COM

COMMAND EXEC 是操作系统的默认操作系统外壳，也是 Windows 95、Windows 98 和 Windows Me 上的默认命令解释器。它还有一个额外的角色，作为启动后运行的第一个程序，负责通过运行 `AUTOEXEC.BAT` 配置文件来设置系统，并且是所有进程的祖先。在 OS/2 和基于 Windows 的操作系统上，COMMAND.COM 的系统是 `cmd.exe`。COMMAND.COM 也适用于这些系统的 32 位，以便在运行时提供兼容性。

#### 运行模式

作为外壳，`COMMAND.COM` 有两种不同的工作模式。首先是交互模式，用户输入的命令会立即执行。其次是批处理模式，执行存储为 `BAT` 文件的预定义命令序列。

#### 显著的内部命令

所有命令只有在行末按回车键后才会运行。COMMAND.COM 不区分大小写，这意味着命令可以大写或小写输入，且它们都是等效（所以 `DIR` 和 `dir` 的工作方式相同）。

- `BREAK` - 通过 `Ctrl+C` 或 `Ctrl-Break` 控制程序中断的处理。

未文档的命令

某些版本的 MS-DOS COMMAND.COM 识别未文档的内部命令。

- `CLS` - 清除屏幕。

文件系统命令

根据 COMMAND.COM 作为操作系统的主要功能，它帮助了一些用于处理文件的命令。要运行程序，输入其名称并按“回车键”（或不带扩展名输入，例如 `.exe` 可以简单命名为 `ic`）。要更改当前的工作驱动器（驱动器号分配），

- `CHCP` - 显示或更改当前代码页。
- `TRUENAME` - 跳过 `SUBST` 和 `AGSYS` 文件名显示文件的“真实名称”。
- `TTY` - 定义用于输入输出的设备。

控制结构

控制结构在批处理文件中创建，尽管它们也可以交互式使用。

- `DATE` - 显示和/或系统日期。
- `ECHO` - 切换文本显示（`ECHO ON`）或关闭（`ECHO OFF`）。也显示文本（`ECHO text`）。
- `label` - 定义目标。
- `LH, LOHS` - 将程序加载到高内存（DOS 中的 `HIGH`）。
- `FOR` - 迭代：为指定集合中的每个项目重复执行命令。
- `DIR` - 列出当前目录下的文件。
- `CD` - 更改当前工作目录。
- `COPY` - 将一个文件复制到另一个文件（如果目录已存在，MS-DOS 需要替换它，同时也复制目录）。
- `REN` - 重命名文件。
- `DEL` - 删除文件。
- `MKDIR` - 创建新目录。
- `RD` - 删除目录。
- `GOTO` - 跳转到目标。
- `PATH` - 显示环境变量。
- `REM` - 注释。
- `IF` - 条件判断。
- `PAUSE` - 暂停并按任意键继续（显示按任意键继续...）。
- `CALL` - 调用另一个程序。
- `PROMPT` - 设置提示符。
- `EXIT` - 退出程序。
- `SHIFT` - 切换参数。
- `TIME` - 显示时间。
- `TYPE` - 显示文件内容。
- `LEN` - 显示字符串长度。
- `VERIFY` - 验证文件。
- `LOCK` - 锁定文件。
- `SET` - 设置变量。
- `ERRORLEVEL` - 显示错误级别。
- `Environment` - 环境变量。
- `Command-line` - 命令行参数。
- `For` - 循环。
- `Variables` - 变量。
- `Redirection, piping, and chaining` - 重定向、管道和链。

### C shell (命令)

PHP 接口。这意味着你可以将此库附加到任何使用流行编程语言编写的项目。

- 无限层级的嵌套循环和条件
- 用户函数

可以根据需要添加新函数，以自定义用户界面的格式数据。

- 开源软件

CTPP 是根据 BSD 协议许可的开源软件。

#### CTPP 架构

![](img/28b49089ea8cf20e1b8f2972fae5fffa_43_0.png)

![](img/28b49089ea8cf20e1b8f2972fae5fffa_43_1.png)

![](img/28b49089ea8cf20e1b8f2972fae5fffa_43_2.png)

![](img/28b49089ea8cf20e1b8f2972fae5fffa_43_3.png)

MVC 范式将应用划分为三个基本实体：一组模型（Models）、一个控制器（Controller）和一个视图（View）。经典的实现将这些实体相互隔离。假设视图不处理任何数据，其结果根据模板对应对象模型；控制器仅用于确定执行的模型列表；而模型则代表管理数据的抽象数据集和规则。

这种范式将 Web 设计师、程序员和管理员的功能隔离开。许多代码可以被重用。在一个具有单一入口点的项目中，这便于其的升级和开发。

如下所示所示，引擎模板的架构由 4 个子系统组成：一个用于将页面模板转换为字节码的编译器、一个执行字节码的虚拟机、一个用于模板的缓存系统，以及一个数据处理函数库。

来源（已编辑）：http://en.wikipedia.org/wiki/CTPP/

#### C shell (C Shell)

Shell（`csh` 或其在机器上的改进版本 `tsh`）是 Bill Joy 在 20 世纪 70 年代后期于加利福尼亚大学伯克利分校研究生期间创建的一种 shell。它被广泛传播，并随着由 Jim Joy 创建的 BSD Unix 系统的 BSD 发布而发行。其他思想或代码的早期贡献者包括 Michael White、Eric Mann、Mike O'Brien 和 Jim Kulps。

C shell 处理器通常运行在文本窗口中，允许用户使用触发动作的命令。C shell 可以允许从文件中读取命令，类似于脚本。像所有 shell 一样，它支持文件命名、管道、文档、命令替换以及条件测试和迭代的控制。在 20 世纪 80 年代，C shell 的不同之处在于其使其使用更简单、更快速的功能。该语言的整体风格像 C，并被认为更高级。

今天，大多数机器上的 `csh` 完全是 `csh` 的一个改进版本。从实际角度来看，`tsh` 就是 `csh`：一个包含可执行文件的单文件，该文件同时链接到 "csh" 和 "tsh"，因此该名称指向同一个改进版本的 C shell。

`tsh` 借用了来自 Texy（Texy）系统的命令补全和命令行编辑功能，这里的 "y" 是因为新增的功能而来的。在那里，`tsh` 恢复了与原始 C shell 的后兼容性。尽管它最初是作为源码树创建的一个侧分支，但现在 `tsh` 已是持续开发的主分支。`tsh` 非常稳定，但考虑到大多数微小错误，新版本每年仍会发布一次。

C shell 几乎完全使用 C 语言，其首要目标是一种与系统其他部分风格更一致的命令语言。键、括号的使用以及 C shell 的内置语法对数组的支持都受到了 C 语言的影响。

按照标准，`csh` 可能看起来不像许多其他流行的脚本语言那样像 C。但在 80 年代和 90 年代，这种差异被认为是非常重大的，特别是与 Bourne 和 T&T 创建的当时的 shell `sh` 相比。此时引入了 C shell 更为常规的算符和语法。

`sh` 缺乏表达式语法。方括号 `[]` 必须通过运行外部程序来评估。`sh` 将其参数作为新命令传递给 C。如果退出使用零返回码，`sh` 将查找一个子句一个独立的语句，但通常与 `.` 写在同一行。

#### 设计对象与特性

C shell 的主要设计特性是它应该看起来像 C 编程语言，并且更便于交互。

#### 更像 C

Unix 系统已经写过；分号（`;`）以及那个嵌套块。否则，它将运行 `else`。将测试程序硬链接为 "test" 和 "[]" 赋予了方括号的符号优势，并使其功能看起来是语言的一部分；它使用反向关键字来标记控制块的结束，受到 ALGOL 68 的严重限制。

作为一个命令并被称为 "bang"，意味着紧接其前的命令。其他短组合，例如，用 `$` 表示上一个命令的最后一个参数，允许将命令的片段拼接在一起形成新命令。

#### 作业控制 (Job control)

作业控制解决了这样一个问题：在 20 世纪 80 年代，大多数用户只有一个简单的字符模式终端。在 `sh` 下，用户一次只能做一件事。一个开始编辑文件以查找或至少保存文件的用户可以在执行任何其他操作之前退出。C 的作业控制可以简单地通过使用 shell 挂起当前活动，并通过输入 `Z` 使用 C shell 的新实例。用户随后可以使用 `fg` 在作业之间切换。作业可以被挂起（停止）或在后台运行。

相比之下，shell 可以让一次只做一件事变得更简单、更快速、更友好，通过转动命令。



# 编辑算符（Editing operators）

编辑不仅可以在之前的命令上进行，也可以在变量上进行。这里是第二个示例，比较列出这些的脚本。

# 别名（Aliases）

别名允许用户使用别名的名称并让 shell 在内部解释用户定义的任何内容。例如，运行这些。由于一个表达式，shell 使用替换和除了。

# 目录栈（Directory stack）

目录栈允许用户推送（push）或弹出（pop）当前工作目录，使其更容易在不同地方之间跳转而无需大量输入。最后，这里是第三个示例，显示了不同的样式。

# 路径哈希（Path hashing）

路径哈希搜索 C shell 的可执行文件。shell 不是在每个目录中一次一次地执行系统调用，直到找到文件或用尽所有可能，而是创建一个内部哈希表。在 sh 中，`;`标记每个用例的结束。该 shell 允许没有。

# 语言概述（Overview of the language）

每行被链接成一组由空格或具有特殊含义的字符分隔的单词，包括括号、I/O 重定向算符以及分号。

## 用例改进

### 基本语句（Basic statements）

第二个目标是 shell 应该是为了交互式使用。在某种程度上，它引入了新功能，通过我们一次只做一件事，转动命令。用户只需几次按键即可完成工作，并且它运行。

基本语句是运行命令的语句。第一个单词被称为要运行的命令名称，可以是内部命令，例如`echo`，或是外部命令。其余单词作为参数传递给命令。

这些新功能中最显著的是历史和别名、目录和路径哈希。许多新功能证明非常受欢迎，许多已被其他复制。

在基本语句层面，这里是语法的一些特性：

### 波浪符号（Tilde notation）

波浪符号提供了一种使用`~`字符定义相对于主目录路径的快捷方式。

### 交互式文件补全（Interactive file completion）

键键可以显示当前命令末尾可能的文件补全。

### Cdpath

`cdpath`扩展了`cd`（切换目录）命令的路径搜索：如果目录不在当前目录中，shell 将尝试在查找它。

### 历史（History）

历史允许用户通过只需几次按键检索并运行之前的命令。例如，两个感叹号，`!!`，

### 通配符（Wildcard）

C shell 像所有 shell 一样，将

## 44 - Shell 命令行参数

如果一个单词包含通配符，则该列表被视为模式，并替换为所有匹配的文件名。

- `> file`意味着标准输出（`stdout`）和标准错误（`stderr`）如果存在将被覆盖，不存在则创建。
- `*`匹配任意数量的字符。
- `>> file`意味着`stdout`将追加到文件末尾。

空格和通配符均视为字面量，但命令替换仍会执行。

- `2>> file`意味着`stdout`和`stderr`都追加到文件末尾。

`'string'`是强引号。整个括在内的字符串被视为字面量。

## 命令替换

命令替换允许将一个命令的输出作为另一个命令的参数。

`` `command` ``意味着获取命令的输出，将其解析为单词并传回命令。

- `<< file`是一个在此文档（here-document）。标准输入（`stdin`）将读取行，直到匹配字符串的行。

## 合并

命令可以在同一行内合并。

- `;`意味着执行第一个命令，如果它以 0 返回码成功执行，则执行下一个。通常情况下，当 C shell 在另一个之前结束时，会显示另一个提示符表示可以输入新命令。
- `&&`意味着执行第一个命令，如果它以非零返回码失败，则执行下一个。
- `&`意味着在后台启动命令并立即显示新提示符。

## 管道

命令可以使用管道进行连接，这使得一个命令的输出作为下一个命令的输入。命令并发执行。

- `|`意味着将`stdout`连接到下一个命令的`stdin`。错误仍然发送到 shell。

## 子壳

子壳是 shell 的子进程副本，它继承当前状态但可以进行更改而不影响父进程。

- `(...)`意味着在子壳中运行命令。

## 变量替换

如果一个单词包含美元符号`$`，随后的字符被视为变量名，并被其值替换。变量编辑器（以引的形式输入）允许路径名编辑、提取扩展名以及其他操作。

## 控制结构

shell 提供了测试和迭代的控制。条件测试控制结构是`if`语句，迭代控制结构是`while`和`repeat`语句。

### if 语句

`if`有两种形式：一种是单行的，另一种是多行的。短形式在表达式为真时只能执行单个命令。

- `if (expression) then commands`

长形式使用`then`、`else`和`endif`用于嵌套在命令中的命令块。如果`else if`关键字出现在同一行，csh 将保持该状态，而不是用单个`end`终止代码块。

## 引用与转义

引用机制允许特殊字符（如空格、日期、美元符号等）被视为字面量。

- `\`将下一个字符视为字面字符。
- `"string"`是弱引号。其中的变量保持不变。

默认情况下，当 shell 运行时，命令继承 shell 的文件描述符，这些描述符通常指向运行 shell 的控制台。

I/O 重定向允许命令使用文件输入或输出。

- `> file`意味着`stdout`是文件，存在则覆盖，不存在则创建。错误仍然发送到 shell。

## I/O 重定向

使用`set`或`setenv`语句创建的 shell 变量位于本地。它们不会传递给子进程。

shell 变量可以是字符串或字符串数组。某些 shell 变量是预定义的，用于控制内部 C 选项，例如通配符未匹配时会发生什么。

语法缺陷通常是语言定义中简单但不必要的差异性。例如，`setenv`、`unset`和`set`命令基本上是同一件事，即将一个名称与字符串或单词关联起来。但这三者都存在简短但完全没有必要的不一致性。

使用`setenv`状态创建的环境变量总是简单的字符串，传递给任何子进程，子进程通过`envp[argument]`索引检索这些变量。

委员会规定对于交互和脚本目的应只有一个首选 shell，且该首选 shell 应该是 Korn Shell。csh 还面临来自其他 shell 对其在语法、功能和实现不良方面缺陷的批评。

### switch

`switch`语句将字符串与模式列表进行比较，列表可能包含通配符字符。如果没有匹配，则采取默认操作（如果有的话）：

```
switch ( string )
  case1:
    break
  case2:
    break
```

在 csh 的当前版本中，字符串可以是任意长度、具有无限数量的字符。

## 表达式

C shell 实现了带有 C 构建运算符的 32 位整数语法，并额外增加了一些用于字符串比较和文件测试（例如检查文件是否存在）的运算符。操作数之间的运算符必须使用空格分隔。运算符被称为名称（Name:）：

```
default:
  commands
  break
w
```

运算符的优先级也借自 C，但具有不同的结合性规则来解决表达式操作数序列中先后顺序的歧义。在 C 语言中，大多数运算符是从左到右的；在 csh 中，是从右到左的。对于这一点，C shell 中的括号有助于避免位移运算符与 I/O 重定向运算符混淆。在编程语言中，括号始终用于指定所需的求值顺序，即使仅是为了清晰。

### while

`while`语句评估表达式。如果为真，则执行嵌套的命令并重复：

```
( expression )
  commands
```

### for

`for`语句列出一个值列表（通常是通配符产生的文件列表），并对列表中的每个值执行循环体并重复嵌套命令。

```
for loop (list-of-values)
  commands
```

由于其创新功能，`for`曾用于交互式，但 csh 一直不适用于脚本。最初，在 80 年代，csh 并不在所有 Unix 系统上存在。csh 在语法上可能是更好的选择，但需要在其他机器上运行。到 20 世纪中期，csh 广泛可用，但使用 csh 脚本面临来自 POSIX 的批评。

### repeat 语句

`repeat`语句重复指定的整数次数。

```
integer command
```

## 变量

经常提到的缺失的功能是独立操作文件句柄的能力以及对函数的支持。由于 Bourne 函数是局部的，csh 作为 C 的直接先驱受限于单行代码，这导致控制需要新功能。csh 脚本对于程序来说并不强大，因为 shell 变得复杂，大型项目往往转向 Bourne shell 或 C 语言。

# CheetahTemplate - 第 47 页

用于 Lisp 的 ANSI 称为“Common Lisp”。SKILL 是一个 IL 函数的库。该名称最初是 Silicon Graphics Compiler Language（图形编译器语言）的缩写，后来被翻译为“SKILL”，这是一个更容易让大家记忆的普通英语单词。

用于理解和编写 SKILL 代码的度量。

`procedure(swap()`：

```
let( a b)
a = 1
b = 2
```

注意，SKILL 中的所有变量都被视为特殊变量（special）。

```
c = a
a = b
b = c
```

语言中添加了额外的命令用于特定工具的函数。例如，针对 PCB Editor 的特定函数前缀为`ax`（如`axIdDBGetObject`），针对 Design Entry 工具的特定命令前缀为`cn`（例如`cnGetWindowInfo`）。

```
printf("%d %d %d" a b c)
```

"ILL"代表 Interface Language（接口语言），最初用于描述 API 而不是语言，代码片段工具。“ILL”这个名称仍然保留在用于 SKILL 代码的事实扩展名`il`中。

## 示例

这里有一些 SKILL 的示例。

首先是一个基础的“Hello, world!”

变量`a`和`b`在函数作用域内，但变量`c`则不是。结果是`c`变成了一个可以在`swap`函数作用域内访问的变量。当执行`swap`并打印`a`、`b`和`c`时，会发生以下情况：

## 语法

SKILL 程序有多种表达式语法可选。传统的 SKILL 语法例如：

```
println("Hello, world!")
```

由于 SKILL 放宽了 Lisp 必须是 S 表达式（S-expression）的要求，看起来与它们的 Lisp 等价物非常不同。例如，SKILL 代码中的函数看起来像这样：

```
procedure(factorial(n))
if n=1
else
* factorial(n-1))
```

```
> spawn
2 1
t
>
```

```
*Error toplevel: undefined variable - a
b
*Error toplevel: undefined variable - b
c>c
```

`(car myList)`可以与类 C 语法混合，例如：

```
(car myList); ; 错误
```

注释由传统的 Lisp 分号分隔。

然而，C 语言中在函数名和左括号之间不允许有空格，如下：

`car myList)`；从分号到行尾的注释

`(plus 2)`或者 C 风格的注释：

```
/* 注释 car(myList) */
另一个注释 */
```

某些算术操作也可以使用中缀法调用。

来源（已编辑）：http://en.wikipedia.org/wiki/Cadence_SKILL

`plus(2)`这些都能被识别。引入此是为了让熟悉 C 和其他过程化语言的程序员更容易操作。

# CheetahTemplate

Cheetah（或 CheetahTemplate）是一种使用 Python 编程语言的 Python 模板。它可以独立使用，也可以与其他工具和框架一起使用。它通常用于通过生成 HTML 进行服务器脚本和动态网页内容，但也用于生成源代码。Cheetah 是采用 MIT 许可的开源软件。模板引擎将内容、图形设计和程序代码清晰分离。这导致了更具模块化、灵活且可重用的架构，缩短了开发时间，并使代码更容易理解和维护。Cheetah 将模板编译为优化的、可读的 Python 代码。它允许作者完全访问任何 Python 数据和功能，同时为管理员提供了一种在需要时选择性限制访问 Python 的方法。

Cheetah 包含在 FreeBSD 以及几个 Linux 发行版中：Gento、Fedora、Debian 和 Ubuntu 等（已编辑："http://en.wikipedia.org/wiki/Cheetah_Template"）

# chomski

chomski 虚拟机（以语言学家诺姆·乔姆斯基命名）和`pp`（模式解析器）均指的是一种命令行语言和实用程序（语言解释器），可用于解析和转换文本模式。该工具按字符（顺序地）读取输入，应用通过命令行或脚本指定的运算，并输出该行。它于 2006 年为 Unix 和 Windows 开发，现适用于 Windows 和 Linux 系统。`Ps`从`Sem`（一种命令行文本编辑器）中派生了许多思想和语法元素。

在`pp`脚本中，词法分析和解析两个阶段被合并在一个脚本文件中。每个命令词的示例都用于操作虚拟机的不同数据结构。

```
{clear;"y"; print;clear;"}
```

即生成数据，然后进行将`x`替换为`y`的小变化。

# 目的与动机

可以将多个命令组合在一个文件中，例如`substitute-chom`，然后使用`-option`从文件中读取命令。

`pp`工具的目的是解析和转换文本。模式遵循形式语言的规则，并包含许多自由上下文。而各种 Unix 工具（如`awk`、`grep`、`sed`）按行处理文本并使用正则表达式搜索或转换文本，`pp`工具则每次处理一个字符，并可以使用自由文法进行转换（复杂的）。根据 Unix 哲学，`pp`工具根据本地上下文的规则在文本流上工作，并作为另一个输出流产生输出，从而允许`pp`工具通过管道传递给其他程序。

## 特性

chomski 语言使用了许多来自 Unix 流的`l`。例如，两个变量或数据缓冲区，如模式空间和“hold space”，这些变量构成了一个极其简单的虚拟机。在 Chomski 语言虚拟机中，通过多个命令操作这些缓冲区，增强了几个缓冲区或寄存器。chomski 虚拟机包含了数据结构如数据栈，以及数据栈。由于编译法，Cheetah 允许作者完全访问任何 Python 数据和功能。Cheetah 编译模板为优化的、可读的 Python 代码。它提供了一种让管理员在需要时选择性限制访问 Python 的方法。

# 使用

可以与类 C 语法混合，例如：

```
(car myList); ; 错误
```

注释由传统的 Lisp 分号分隔。

然而，C 语言中在函数名和左括号之间不允许有空格，如下：

`car myList)`；从分号到行尾的注释

`(plus 2)`或者 C 风格的注释：

```
/* 注释 car(myList) */
另一个注释 */
```

这些都能被识别。引入此是为了让熟悉 C 和其他过程化语言的程序员更容易操作。

# 语法

SKILL 程序有多种表达式语法可选。传统的 SKILL 语法例如：

```
println("Hello, world!")
```

由于 SKILL 放宽了 Lisp 必须是 S 表达式（S-expression）的要求，看起来与它们的 Lisp 等价物非常不同。例如，SKILL 代码中的函数看起来像这样：

```
procedure(factorial(n))
if n=1
else
* factorial(n-1))
```

```
> spawn
2 1
t
>
```

```
*Error toplevel: undefined variable - a
b
*Error toplevel: undefined variable - b
c>c
```

用于 Lisp 的 ANSI 称为“Common Lisp”。SKILL 是一个 IL 函数的库。该名称最初是 Silicon Graphics Compiler Language（图形编译器语言）的缩写，后来被翻译为“SKILL”，这是一个更容易让大家记忆的普通英语单词。

用于理解和编写 SKILL 代码的度量。

`procedure(swap()`：

```
let( a b)
a = 1
b = 2
```

注意，SKILL 中的所有变量都被视为特殊变量。

```
c = a
a = b
b = c
```

语言中添加了额外的命令用于特定工具的函数。例如，针对 PCB Editor 的特定函数前缀为`ax`（如`axIdDBGetObject`），针对 Design Entry 工具的特定命令前缀为`cn`（例如`cnGetWindowInfo`）。

```
printf("%d %d %d" a b c)
```

# 示例

这里有一些 SKILL 的示例。
首先是一个基础的“Hello, world!”

变量`a`和`b`在函数作用域内，但变量`c`则不是。结果是`c`变成了一个可以在`swap`函数作用域内访问的变量。当执行`swap`并打印`a`、`b`和`c`时，会发生以下情况：

# 语法

SKILL 程序有多种表达式语法可选。传统的 SKILL 语法例如：

```
println("Hello, world!")
```

由于 SKILL 放宽了 Lisp 必须是 S 表达式（S-expression）的要求，看起来与它们的 Lisp 等价物非常不同。例如，SKILL 代码中的函数看起来像这样：

```
procedure(factorial(n))
if n=1
else
* factorial(n-1))
```

```
> spawn
2 1
t
>
```

```
*Error toplevel: undefined variable - a
b
*Error toplevel: undefined variable - b
c>c
```



# CheetahTemplate

Cheetah（或 CheetahTemplate）是一种使用 Python 编程语言的 Python 模板。它可以独立使用，也可以与其他工具和框架一起使用。它通常用于通过生成 HTML 进行服务器脚本和动态网页内容，但也用于生成源代码。Cheetah 是采用 MIT 许可的开源软件。模板引擎将内容、图形设计和程序代码清晰分离。这导致了更具模块化、灵活且可重用的架构，缩短了开发时间，并使代码更容易理解和维护。Cheetah 将模板编译为优化的、可读的 Python 代码。它允许作者完全访问任何 Python 数据和功能，同时为管理员提供了一种在需要时选择性限制访问 Python 的方法。

Cheetah 包含在 FreeBSD 以及几个 Linux 发行版中：Gento、Fedora、Debian 和 Ubuntu 等（已编辑："http://en.wikipedia.org/wiki/Cheetah_Template"）

# chomski

chomski 虚拟机（以语言学家诺姆·乔姆斯基命名）和 `pp`（模式解析器）均指的是一种命令行语言和实用程序（语言解释器），可用于解析和转换文本模式。该工具按字符（顺序地）读取输入，应用通过命令行或脚本指定的运算，并输出该行。它于 2006 年为 Unix 和 Windows 开发，现适用于 Windows 和 Linux 系统。`Ps` 从 `Sem`（一种命令行文本编辑器）中派生了许多思想和语法元素。

在 `pp` 脚本中，词法分析和解析两个阶段被合并在一个脚本文件中。每个命令词的示例都用于操作虚拟机的不同数据结构。

```
{clear;"y"; print;clear;"}
```

即生成数据，然后进行将 `x` 替换为 `y` 的小变化。

# 目的与动机

可以将多个命令组合在一个文件中，例如 `substitute-chom`，然后使用 `-option` 从文件中读取命令。

`pp` 工具的目的是解析和转换文本。模式遵循形式语言的规则，并包含许多自由上下文。而各种 Unix 工具（如 `awk`, `grep`, `sed`）按行处理文本并使用正则表达式搜索或转换文本，`pp` 工具则每次处理一个字符，并可以使用自由文法进行转换（复杂的）。根据 Unix 哲学，`pp` 工具根据本地上下文的规则在文本流上工作，并作为另一个输出流产生输出，允许 `pp` 工具通过管道传递给其他程序。

## 特性

chomski 语言使用了许多来自 Unix 流的 `l`。例如，两个变量或数据缓冲区，如模式空间和“hold space”，这些变量构成了一个极其简单的虚拟机。在 Chomski 语言虚拟机中，通过多个命令操作这些缓冲区，增强了几个缓冲区或寄存器。chomski 虚拟机包含了数据结构如数据栈，以及数据栈。由于编译法，Cheetah 允许作者完全访问任何 Python 数据和功能，同时为管理员提供了一种在需要时选择性限制访问 Python 的方法。

# 使用

可以与类 C 语法混合，例如：

```
(car myList); ; 错误
```

注释由传统的 Lisp 分号分隔。

然而，C 语言中在函数名和左括号之间不允许有空格，如下：

`car myList);` 从分号到行尾的注释

`(plus 2)`

或者 C 风格的注释：

```
/* 注释 car(myList) */
另一个注释 */
```

某些算术操作也可以使用中缀法调用。

`plus(2)`

这些都能被识别。引入此是为了让熟悉 C 和其他过程化语言的程序员更容易操作。

# CobolScript

在计算机编程语言。CobolScript 有语法用于数据转换、接口和服务器端脚本。它是一种基于 COBOL 的脚本，对 COBOL 程序员来说很熟悉，且 Motif 是一个重要的工具对于

# 50 - ColdFusion

适用于 Microsoft Windows、Linux、OS 和 FreeBSD 的版本。

* "Hello world"

Matt Dean 是 ColdFusion 的创建者之一。

* `DISPLAY 'Content-type: text/html'`

默认情况下，ColdScript 使用反引号（grave accent）来界定字符串（尽管可以使用命令行选项进行更改）。

# Hello, world

```
DISPLAY LINEFEED.
```

以下程序生成一个非常简单的网页的 HTML，并可以在 Web 服务器上运行（标准输出重定向到浏览器）。

```
DISPLAY <BODY>
```

来源（已编辑）："http://en.wikipedia.org/wiki/ColdScript"

```
DISPLAY <CENTER>Hello World</CENTER>
```

```
DISPLAY `</body></html>`



# ColdFusion

在计算领域，`ColdFusion` 既指由 `Jeremy` 和 `JJ Alaire` 于 1995 年发明的商业应用平台，也指与该平台配合使用的编程语言。它最初的设计是为了更容易地将 `HTML` 编译为动态页面（从 2.996 版本开始），后来变成了一个完整的平台，包含一个用于执行“全脚本编写”的 `IDE`。截至 2010 年，`ColdFusion` 的版本（2005 年被 `Adobe Systems` 收购）包含了用于企业集成和互联网应用（`RIA`）开发的高级功能。

`ColdFusion` 最常用于数据驱动的网站或内网，但也可用于生成远程服务，如 `SOAP Web` 服务或客户端。它非常适合作为服务器端技术来补充 `ColdFusion Flex`。`ColdFusion` 还可以通过网关接口处理短信和即时消息等异步事件，该接口在 `ColdFusion MX7` 企业版可用。

在未来的发布中计划包含点图形（`CAPTCHA`）和 `zip` 压缩包（引入视频制作）

简化的实现（自动 `WSDL` 生成 / 用于生成和消费服务的传输处理示例）。`ASP` 没有等于 `<CFOKEO="#tempconf.cf?wsdl#" method="CelsiususFusion2#=CFRETURN value="#cfm?>">` 的功能

## 主要功能

`ColdFusion` 提供了许多额外的功能。其中包括：

- 简化的数据库访问
- 客户端和服务器缓存管理
- 客户端代码生成，特别是针对表单和验证
- 从 `HTML` 到 `PDF` 和 `Flash` 的转换
- 从常见的企业系统检索数据，如 `LDAP`、`SMTP`、`POP`、`HTTP`、`FTP`、`Microsoft` 服务器以及来自 `RSS` 和 `Atom` 的常见数据格式
- 基于 `Verity K` 的文件索引和搜索服务
- `GUI` 管理
- 服务器、应用、客户端、会话和请求作用域
- `XML` 解析、查询 (`XPath`)、验证和转换 (`XSLT`)
- 服务器集群化
- 任务调度
- 图表绘制和报告

`CFML` 的其他实现提供了类似或增强的功能，例如在 `.NET` 环境中运行或图像管理。

## 概述

`ColdFusion` 的独特特征与脚本语言——`ColdFusion` 标记语言（`CFML`）有关，它在目的上与 `ASP`、`JSP` 和 `PHP` 的脚本语言相比，但其标签语法与 `HTML` 非常相似，而脚本语法类似于 `JavaScript`。“`ColdFusion`” 通常与 "`CFML`" 或 "`CF`" 同义使用，但还有其他 `ColdFusion` 服务，且 `ColdFusion` 还支持除 `CF` 以外的编程语言，例如可以使用类 `JavaScript` 语言 `CFSScript` 编写的服务器端脚本。

`ColdFusion` 的原始版本于 1999 年 7 月创建并发布，由 `J. "JJ"` 和 `Jeremy Alaire` 兄弟开发。2001 年，`ColdFusion` 被 `Macromedia` 收购，随后 `Macromedia` 在 2005 年被 `Adobe Systems` 收购。

用 `CF` 特性编写的引擎具有内置脚本语言（`CFScript`）、用 `Java` 编写的插件模块，并且与 `HTML` 非常相似。为了解释一个元素，`ColdFusion` 标签以字母 "`CF`" 开头，其名称被解释为 `HTML`。例如：`<cf` 开始变量或其他内容的输出。

除了 `ColdFusion` 之外，`ColdStudio` 提供了一个带有 `WYSIWYG`（所见即所得）显示的开发环境。除了 `ColdFusion` 之外，`ColdStudio` 还使用流行的后端编程语言，如 `Perl`。此外，它让非程序员能够轻松访问后端功能（特别是 4.0 版本），与 `Adobe Web` 服务器和信息服务器轻松集成。

### 简化的文件操作

## ColdFusion - 51

服务器和信息服务器。代号为 "`Neo`"。该项目后来被揭示完全使用 `Java` 重写的 `ColdFusion` 服务器。这种移植性极大并为服务器提供了一层安全性，因为它运行在 `Java` 环境中。高级工程师 `Damon Cooper` 以及 `LiveCycle` 使得 `Java` 变得不再必要。

## 其他特性

`ColdFusion` 的第一个版本（当时称为 `Cold Fusion`）于 1995 年 7 月 10 日发布。该版本几乎完全由 `Josef JJ` 完成。按照现代标准，早期的 `ColdFusion` 仅仅是关联。

- 2003年7月：`Macromedia ColdFusion MX 6.1` 版本（build `6,1,0,63958`），热补（`6,0,1,63938`），更新 1（`6,1,0,63872`）
- 2005年2月：`Macromedia ColdFusion MX 7`（build `7,0,0,91650`）
- 2005年9月：`Macromedia ColdFusion MX 7.1`（build `7,0,1,11466`）

6.0 之前的所有 `ColdFusion` 版本都是使用 `Microsoft C++` 编写的。这意味着限于 `Windows` 上运行。`Adobe` 从 3.1 版本开始在 `Sun Solaris` 上支持 `ColdFusion`。

- 2006年6月：`Macromedia ColdFusion MX 7.2`（build `7,0,2,14256`）
- 2007年7月：`Adobe ColdFusion 8`（build `8,0,0,17627`）
- 2008年4月：`Adobe ColdFusion 8.1`（build `8,0,1,19576`）
- 2009年10月：`Adobe ColdFusion 9`（build `9,0,0,25108`）
- 2010年1月：`Adobe ColdFusion 9.1`（build `9,0,1,27433`）

等待，让我重新对齐 `OCR` 中碎片化的逻辑。我将根据提供的文本流提供修正的版本。

`ColdFusion` 的原始版本于 1999 年 7 月创建并发布，由 `J. "JJ"` 和 `Jeremy Alaire` 兄弟开发。2001 年，`ColdFusion` 被 `Macromedia` 收购，随后 `Macromedia` 在 2005 年被 `Adobe Systems` 收购。

用 `CF` 特性编写的引擎具有内置脚本语言（`CFScript`）、用 `Java` 编写的插件模块，并且与 `HTML` 非常相似。为了解释一个元素，`ColdFusion` 标签以字母 "`CF`" 开头，其名称被解释为 `HTML`。例如：`<cf` 开始变量或其他内容的输出。

除了 `ColdFusion` 之外，`ColdStudio` 提供了一个带有 `WYSIWYG`（所见即所得）显示的开发环境。除了 `ColdFusion` 之外，`ColdStudio` 还使用流行的后端编程语言，如 `Perl`。此外，它让非程序员能够轻松访问后端功能（特别是 4.0 版本），与 `Adobe Web` 服务器和信息服务器轻松集成。

代号为 "`Neo`"。该项目后来被揭示完全使用 `Java` 重写的 `ColdFusion` 服务器。这种移植性极大并为服务器提供了一层安全性，因为它运行在 `Java` 环境中。高级工程师 `Damon Cooper` 以及 `LiveCycle` 使得 `Java` 变得不再必要。

## 52 - ColdFusion

全球范围内有大量用户参与了测试过程——远超最初预计 5000 个系统。`ColdFusion` 开发团队由位于马萨诸塞州纽约/波士顿的开发者以及印度班加罗尔的海外人员组成。

`CFPDFFORM` 的一些新功能允许与 `Acrobat` 表单集成、某些图像函数、`.NET` 集成以及 `CFPRESENTATION` 标签，后者允许使用 `Acrobat Connect` 创建动态演示文稿，在企业版的 `ColdFusion` 管理器中只需提及 `Adobe Breeze` 即可实现基于 `Web` 的协作。`ColdFusion 8` 适用于包括 `Linux`、`Mac OS` 和 `Windows 2008` 在内的操作系统。

`ColdFusion 8` 的其他新增功能包括内置 `Ajax` 小部件 (`CFIJZ`)、文件操作 - 服务器集成 (`CFXCHANGE`)，包括自动生成验证码 (`CFIMAGE`)、多线程、每个应用程序设置和 `RSS` 馈、报告增强、加密库、数组结构改进、改进的集成、广泛的性能和合并能力 (`CFPDF`)、接口、对 `Adobe Derby` 的嵌入式数据库支持以及更多的 `ECMAScript` 编译器

开发 `ColdFusion 8` 应用程序可以使用平台：主要是 `Adobe`、`Dreamweaver 5x`、`Macromadia HomeSite 5x`、`CF Eclipse` 等。这些应用程序已提供“标签更新”，以支持这些新的 `ColdFusion 8` 特性。

### Adobe ColdFusion 9 (代号：`Centaur`)

`ColdFusion 9` 于 2009 年 10 月 5 日发布。`CF9` 的新功能包括：

- 能够在完全在 `CFScript` 中编写用户定义函数 (`UDFs`) 和 `ColdFusion` 组件 (`CFCs`)。
- 显式的“`local`”作用域，不需要在函数顶部声明局部变量。
- 通过名为“`init`”的方法或方法名调用的隐式 `getter/setter`（`ColdFusion` 默认行为除外）。
- 用于控制处理的新 `CFTag` 和用于控制流的 `CFScript` 语法。
- 通过 `Hibernate` (`Java`) 实现对象关系映射 (`ORM`) 数据库集成。
- 使用 `serverStart` 和 `serverEnd` 方法进行服务器端文件管理。
- 与 `Adobe` 和 `Air` 的紧密集成。
- 与 `Microsoft` 产品集成，包括 `Word`、`Excel`、`Exchange` 和 `Powerpoint`。
- 内存管理 - 使用 `HDD` 处理内存中内容的能力。
- 暴露服务 - 能够从外部安全地访问服务器的功能。

### Adobe ColdFusion 10

`Adobe MAX 2010` 确认 `ColdFusion 10` 正在开发中。`ColdFusion` 下一个版本的内部代号为“`Link`”，但在博客、`Twitter` 等平台上通常被称为 `ColdFusion X`。

### Adobe ColdFusion Builder

`Builder` 是 `Adobe` 基于 `Eclipse` 的 `IDE`，可用于构建适用于 `ColdFusion` 的应用程序。该产品的原始代号“`Bolt`”参考了从 `Alaire` 时代以来该产品的原始闪电图标。

#### Adobe ColdFusion Builder 1.0

`Builder` 于 2010 年 3 月 22 日同 `Fusion Builder 4` 一起发布。

特性：

- 对象关系映射-配置
- 应用程序代码生成
- 服务器管理
- 通过 `Eclipse` 框架轻松扩展
- `CFML`、`HTML`、`Javascript` 和 `CSS` 语法高亮
- 标签、变量和组件的代码辅助
- 代码折叠
- 代码段及管理
- 大纲视图
- 针对文件和数据库的 `RDS` 资源管理器
- 行级调试
- 重构

#### Adobe ColdFusion Builder 2.0

`ColdFusion 2.0`（代号“`Storm`”）已在 `Adobe MAX 2010` 上确认并展示。主要功能包括代码导航、搜索改进、代码格式化和自动方法代码结构

## 特性

### 丰富表单

`ColdFusion` 服务器包含了 `Macromedia 1.5` 技术的子集。其说明目的是允许使用 `CFML` 在 `HTML` 页面中生成丰富的电影（`movies`）。这些 `Flash` 表单可以实现丰富的应用程序，但使用 `Macromedia` 在 `Flash` 表单上的 `Action Scripts` 效率有限。

`Flash` 表单为数据输入提供了额外的小部件，例如选择器和指南。

在之前的 `ColdFusion` 版本中，可以使用 `Java` 和 `JavaScript` 的组合提供某些验证和添加。此选项允许不想使用 `Flash` 的用户，但并非所有功能都受到支持。

示例：

```html
<cfform class="flash" method="post" width="400" height="400">

  <input type="text" name="username" required="yes">Username

  <input type="password" name="password" label="Password" required="yes">

  <input type="submit" name="submit" value="Sign In">

</cfform>
```

`ColdFusion 8` 支持 `Java` 接口。`ColdFusion` 组件使用 `.cf` 文件扩展名，将其与 `ColdFusion` 模板区分来。

`ColdFusion` 特别适用于为熟悉 `HTML` 但不熟悉命令式编程的 `Web` 设计师和作者熟悉的界面。

使用 `ColdFusion` 的传统方法。标准的 `CF` 页面可以被解释为标签，标签名与文件名对应。例如，文件 `ifmap` 可以设置 "`cf map`" 属性。属性用于 `CF` 页面的 `ATTRIBUTE` 作用域内。可以通过调用页面、`ColdFusion Web` 应用程序中的特殊目录或通过调用页面中的 `CFIMPORT` 标签访问页面。后者方法并不一定需要标签的 “`cf:`” 前缀。

## 远程调用 (Remoting)

方法作为 `Web` 服务提供，无需额外编码，访问方法只需要被远程调用即可。通过 `GET` 或 `POST` 调用 `ColdFusion`。这将调用 `ColdFusion` 函数，并将 "`value`" 和 "`string`" 作为参数。

这种调用非常适用于启用 `Ajax` 的应用程序。`ColdFusion 8` 引入了将 `ColdFusion` 数据序列化为 `JSON` 格式的能力。

## PDF 和 Paperfact 生成

`ColdFusion` 可以使用 `HTML` 生成所需的 `PDF` 或 `Paperfact` 文档。生成的文档可以保存到磁盘或发送到客户端浏览器。

```
http://path/to/components/method.cf7?query=method
```



当导航到组件 URL 并在组件声明中插入适当的代码时，ColdFusion 服务器会自动生成文档。这是组件内省的应用，适用于 ColdFusion 组件开发者。通过导航到 ColdFusion URL，此接口返回 Java 类的 HTML 文档。

## ColdFusion 组件（对象）

ColdFusion 最初不是一种面向对象的编程语言，类似于 PHP 3。ColdFusion 属于不支持继承的面向对象语言（如 Java、Smalltalk 等）。从 6 开始，ColdFusion 通过组件构造引入了基本功能，类似于面向对象中的类。每个组件可以包含任意数量的属性或方法，并继承其他组件，但只支持单继承。带有订阅请求的对象处理功能集和性能增强。

目前可用的服务器平台支持功能，具有细微变化。ColdFusion 支持 JSP 2.0 库中的 JSP 标签。使用 `tags` 标签包含在 ColdFusion 页面中。

## 自定义标签

## 与编程语言交互

## ColdFusion 与 Java

标准的 ColdFusion 安装允许将 ColdFusion 作为 WAR 或 EAR 文件部署到独立应用程序服务器，例如 JBoss 和 IBM WebSphere。ColdFusion 也可以部署到服务器容器，如 Apache Tomcat 和 Morbt Jay，因为这些平台没有正式支持 ColdFusion，导致其许多功能无法使用。

由于 ColdFusion 是一个 Java 应用程序，ColdFusion 可以与 Java 类混合创建变体应用。

# Cold Mook

Colin Mook
Colin Mook 是一位世界闻名的 Flash 和 ActionScript 专家，被 Adobe 官方誉为“ActionScript 大师”。他也是一位知名的导师、作家以及程序员。Colin 曾在 Software Inc. 担任一段时间的成员（1997 年）。在接下来的四年里，他在领先的交互代理机构之一 ICE 服职。Cold Mook 曾为惠普、宝洁及其他知名品牌开发过交互式应用程序。

C. Mook 还是多处理技术应用的信徒（他称之为“用户时代”）。他是 Union 项目——一种此类应用的开发平台的创建者之一。

## 职业

Mook 读于加拿大水铁卢大学的文学系。自 1995 年以来，我们一直……

## 命令行提示符

命令提示符（执行文件名为 `cmd.exe`）是微软提供的命令行解释器，适用于 OS/2、Windows CE 以及基于 Windows 的操作系统（包括 Windows 2000、XP、Vista、7、Server 2003 和 Server 2008）。它是 MS-DOS 和 Windows 9x（称为 MS-DOS 提示符）中 `COMMAND.COM` 的对应物，或者是类 Unix 系统上使用的 Shell。

## 技术信息

与作为 DOS 程序的 `COMMAND.COM` 不同，`cmd` 是该平台的原生程序。它可以利用原生程序可用但 DOS 程序无法使用的特性。例如，`cmd` 是操作系统上的原生文本模式应用程序，它可以使用管道，且管道的两端都可以运行。因此，在 `cmd` 中可以重定向标准错误，而 `COMMAND.COM` 则不行。

## 版本

`cmd.exe` 的 OS 和 Windows 版本都比空白的“command” 具有更多消息。在 `cmd.exe` 的 OS/2 版本中，错误以当前语言报告。可以使用 `help` 命令来获取更多信息。`cmd.exe` 仍然是 Windows Vista、Windows Server 2008 和 Windows 7 的一部分。它拥有的内置命令比 `COMMAND.COM` 多。

- 用于执行任务部分内容的文件。
- `SET` 命令中的文件名解析扩展与 C shell 具有相似性。
- `SET` 命令中还提供了表达式求值扩展。
- `FOR` 命令的扩展，用于支持在定义中解析文件和任意集合。
- 使用方向键滚动查看命令历史（在 `COMMAND.COM` 中通过 DOSKey 实现）。
- `SETLOCAL`/`ENDLOCAL` 限制更改的范围。
- 内部 `CALL` 和 `GOTO` 标签减少了对批处理文件的需求。
- 类似于 bash 的默认关闭的路径补全。
- 可以通过 `PUSH` 和 `POP` 访问的目录。
- `If` 除了进行大小敏感的字符串比较外，还可以进行不区分大小的比较和等值比较。
- 使用（`\`）转义字符的能力。
- 这些扩展可以被禁用，以提供更严格的兼容性。

# ColdFusion

……如 Java、Groovy 和 Ruby 等替代语言。ColdFusion 是最早允许这种 Java 开发风格的脚本平台之一。

可以认为 ColdFusion 比 Java EE 或 .NET 更不具备跨平台通用性，仅仅因为 ColdFusion 将运行在应用服务器之上（任何 Java 应用服务器如 JBoss、WebSphere-Geron、Tomcat、Recat、Serv Er (web server) 等）。在理论上，可以在不将 Java 应用服务器更改为 .NET 服务器的情况下制作 ColdFusion。

## ColdFusion 和 .NET

ColdFusion 8 在 CFML 语法中原生支持 .NET。ColdFusion 开发人员可以简单地调用 .NET，而无需重新思考或以任何方式更改元素。数据类型在 ColdFusion 和 .NET 之间自动翻译（例如：`Data Table` -> `Cold Query`）。

将 .NET 包含在现有的对 Java、CORBA 和 COM 的支持之外，是 Adobe ColdFusion 对技术栈保持无关的共同特征。

在 ColdFusion 7.1 之前，ColdFusion 组件只能通过声明为 Web 服务来供 Java 或 .NET 使用。然而，在 ColdFusion MX 7.1 中，ColdFusion 组件现在可以使用 `CFXProxy` api 直接在 Java 类中使用。

ColdFusion 起于基于 Web 技术行业标准的专有技术。然而，通过竞争性产品的优势，它正成为一种不那么封闭的技术。其他产品包括 Raise、DBacon、Ignition、SmithPro 和 Project Web Builder。

应用程序并喜欢使用 Java 库。ColdFusion 可以访问底层的 Java 类、结构体、JSP 标签库，并可以访问获取 JSP 页面上下文的 JSP 函数（`getContext()`）。

Cold 不仅可以将企业内部不同的技术整合在一起，还可以让这些技术被 Web 浏览器之外的客户端使用，但不限于 Flash Player、Adobe Integrated Runtime (AIR)、移动设备 (SMS)、Acrobat Reader (PDF) 和 IM 网关。

## 缩写

ColdFusion 标记语言的缩写是 CFML。Cold 效果的。原始扩展是 DBM 或 DBML，代表数据库映射语言。在谈论 ColdFusion 时，使用缩写 CFML，它用于许多 ColdFusion 资源，如用户组 (CFUGs) 和站点。

# BlueDragon

对于 Java EE 开发人员的一种独特功能，Cold 8 有能力在不使用 .NET 的情况下远程访问 .NET 程序集。这允许 ColdFusion 用户在无需安装 Windows 操作系统的情况下利用 .NET。

BlueDragon - 基于 .NET 的 CFML 引擎和开源 Java 的 CFML 引擎 (Open BlueDragon)。

CFMX 是 ColdFusion 6 和 7 版本的常用缩写（即 ColdFusion MX）。

# Railo

Railo - 免费、开源的 CFML 引擎。它有主版本和其他版本。

> 来源：（已编辑）："http://en.wikipedia.org/wiki/ColdFusion"

# 替代服务器

# CorbaScript

CorbaScript 是一种面向对象的脚本语言。

# DECLAN

DECLAN 是一种决策语言；它是一种过程和面向对象的编程语言，旨在跨广泛操作系统和计算机硬件进行数据分析。G.E. Nixon Jr 是 DECLAN 语言和环境的主开发者，致力于提供一种为普通人设计的商业语言。

# DECLAN Pro

DECLAN Pro 起于脚本解决方案集；Blaise (2003) 源自 David (2001) 和 Alexander Baranovski。最初的意图与 PASCAL 程序员在同一个项目中共存，通过提供一个使用 Windows DLL 文件来扩展项目能力的环境，同时提供解释和即时编译的机制。这种模块化开发和实现方法的核心语言提供了变量管理、循环等，同时将硬件和操作系统调用保持在外部。

- 一种类似于 Object Pascal 的语言，为 JavaScript 提供了早期性和灵活性。
- 一个编译器、即时编译编译器和解释器。
- 一个虚拟机框架；因此从一个操作系统运行的可以在某些其他系统上运行。

> 来源：（已编辑）："http://en.wikipedia.org/wiki/DECLAN_Pro"

# DG 脚本

DG 脚本是一种脚本语言，构建者可以在不需要了解 C 等编程语言的情况下，快速为 MUD 添加交互功能。

触发器类型
有很多触发器类型，最重要的五种是：

- 随机 (Random) —— 这是一个每秒触发一次的触发器，具有特定的成功概率。
- 命令 (Command) —— 这是一个在房间内创建的本地命令。
- 语音 (Speech) —— 这在特定键或短语被说时触发。
- 动作 (Act) —— 该触发器在响应特定动作运行时。
- 问候 (Greet) —— 该触发器在玩家进入房间时运行。

Death's Gate 语言
DG 脚本最初开发于已停止的 Death's MUD，现在是 CircleMUD 和其他代码库的补充。

- 移动 (mat) —— 允许将玩家、物体或对象移动到别处。
- 加载 (load) —— 将新对象加载到游戏中。
- 强制 (force) —— 让玩家或对象移动。

虽然简单学习，但 DG 是一个完整的编程语言，所有标准的编程表达式如 `if` 和 `while` 都是可用的。

以下内容不应视为游戏建议或“教程”。它仅仅展示了一个编程语言的脚本。这旨在为设计师提供示例。

变量
DG 脚本基于“触发器”的概念——一种作为特定动作结果而运行（称为运行）的小型脚本。附加到物体、对象或房间的触发器（截至 UD 3.5）也附加到玩家身上。这似乎具有局限性，但在实践中，它受限于 MUD 的限制，因为一个操作的结果通常用于触发另一个。

在 DG 脚本中
命令
脚本可以使用任何标准命令。它还可以使用一些“魔法师”命令。在 DG 脚本的实现中，命令以 `m`、`o` 或 `r` 前缀（代表物体、对象或房间）。

- 移动 (move) —— 将玩家、物体或对象移动到其他。
- 显示 (echo) —— 允许自由格式文本。

这是一个 ActMUD 使用过一段时间的实际脚本。在这里，如果某个橱子变空，它将洗一些杯子并将它们放回橱子。
尽管对玩家看起来如此，但触发器是在响应事件：脚本看到“如果里面有杯子 (22222 是杯子)”。如果是，橱子创建新的杯子，并强制杯子拿起它们 (`%force% cup get`) 然后放入橱子 (`%force% cup cupboard`)，最后使用 `say echo` 命令只是让这一切看起来更自然一些。

# DIGITAL 命令语言 - 第 57 页

```
Vnum : 11111

1) 名称：橱柜补给

2) 用途：对象

3) 触发类型：随机

4) 数值参数： 100

5) 参数：

6) 命令：

set cook cook

if !cook%

halt

end

if %self.count(22222)==0

%force%cook Say Raca! There are no

cups in the cupboard.

%load%obj 22222

%force%cook get cup

%load%obj 22222

%force%cook get cup

%load%obj 22222

%force%cook get cup

%echo%The cook does some frantic

washing up.

%force%cook put cup cupboard

%force%cook put cup cupboard

%force%cook put cup cupboard

%force%cook Say that is better
```

源自（已编辑）："http://en.wikipedia.org/wiki/DG_scripts"

## DIGITAL 命令语言

DIGITAL 命令语言
DCL，即 DIGITAL 命令语言，是由数字设备公司（Digital Equipment Corporation）形成的大多数操作系统采用的标准命令语言（该公司已被 Compaq 收购，而 Compaq 又被 Digital Packard 收购）。它根于 IAS、TOPS-20 和 RTT-1 操作系统，并实现在 Digital 的大多数操作系统中，特别是 RSX-11，但其最强大的形式是在 OpenVM 操作系统中。

当所编写的程序被广泛使用时，DCL 是一种支持数据集、字符串、整数、数组和布尔值的脚本语言，但不包括指针。访问 OpenVM 系统服务（内核 API）通过词法函数实现，这些函数的作用与其编译语言中的对应项相同，并允许脚本访问系统状态信息。DCL 包含 IF-THEN-ELSE，以及对所有 RMS 文件类型（包括流、索引和顺序文件），但遗憾的是缺乏 DO-WHILE 循环，需要用户使用 IF 和 GOTO-label 语句。

对于 OpenVM 的实现，命令行运行时是一个可以编译到用户应用程序中的库（CLI），它为系统命令和用户命令提供了一致的接口。命令行必须以动词开头，后面跟着参数（例如可以跟在任何命令行后的位置无关限定符，或影响其出现后的参数的位置相关限定符）。大多数限定符是位置无关的；即它们可以出现在动词最主要部分的任何位置，并且要求提供限定符名称。一个操作系统命令示例可能如下：
`set audit/alarm/enable=(authorization,breakall)=$1$DGA1242:`

第二个命令可能是：
`sho dev $1$DGA1242/fil`

虽然 DCL 文档显示所有 DCL 命令均为大写，但 DCL 命令不区分大小写，可以以大写、小写或混合大小写输入。某些实现使用独特方案允许命令短命，而其他实现（如 RSX-11）则允许命令缩写为至少三个字符。

与使用路径位置的系统不同，CLI 命令必须通过 CLI（命令语言定义）或外部符号显式定义。OpenVMS 命令由 CLI 文件定义；这些文件由 CDU（命令定义单元）编译，并默认“表” `DSSLLIBRARY:DCLFILES`，进程可以使用自己的单元格并由用户调用。例如，定义一个由 `SYSSEXE:FOE` 实现“help”选项的命令，可以使用类似于下面的 CLI 文件：

```
DEFINE FOO

IMAGE "SYSSEXE:FOE"

QUALIFIER
```

用户随后可以输入 `"FOO"/"FOAR"`，并将调用该命令。命令定义语言支持许多类型的选项（用于日期和文件规范），并允许限定符更改镜像——例如使用 `"CREATE"` 创建文件或使用 `"DIRECTORY"`。

另一种（更简单但活性较差）定义命令的方法是用于固有命令（eigen commands）。这更类似于 Unix 的调用方法。通过 `foo` 和其他非原生系统：

```
foo := $$$sysexe:foo
```

命令 `'FOO'` 将任何额外参数线性地传递给程序，例如 `foo-u`。这种方法用于从 Unix 和非原生系统迁移的命令；以及使用 `arg` 和命令行开关的 C 程序。

带有 V6.2 的 OpenVMS DCL 脚本支持定义 Unix 风格命令方法的本地名称。这种机制被称为自动命令（Automatic Command）。`DCLPATH` 允许定义目录列表，然后在其中搜索 DCL 命令（文件名与用户调用的命令匹配的 `command.EXE`）。传统的外部命令也允许 Unix 风格的命令聚焦。

使用 `TYPE` 命令在屏幕上打印段落，可能会使用类似下面的脚本：

```
$ SYSINPUTThis is an example of the TYPE verb in DCL language.
```

```
$ EXIT
```

### 间接引用

在 DCL 中可以构建通过翻译符号引用的数组。程序员可以构建索引函数来构建任意的数据结构。

```
$i = 1

$variable'i = "blue"

$i = 2

$variable'i = "green"

$j = 1

$ color=variable'i = "red"

$ color=variable'i = "blue"

$ color=variable'i = "yellow"
```

在这个示例中，变量 `rainbow` 被赋值为值 `"red"`，而 `rainbowgreen` 被赋值为 `"yellow"`。

源自："http://en.wikipedia.org/wiki/DIGITAL_Command_language/"

### 脚本

DCL 脚本看起来像任何脚本语言，带有 V6.2 支持定义 Unix 风格命令方法的本地名称。这种机制被称为自动命令。`DCLPATH` 允许定义目录列表，并在其中搜索 DCL 命令（文件名与用户调用的命令匹配的 `command.EXE`）。传统的外部命令也允许 Unix 风格的命令聚焦。

使用 `TYPE` 命令在屏幕上打印段落，可能会使用类似下面的脚本：

```
$ SYSINPUTThis is an example of the TYPE verb in DCL language.
```

```
$ EXIT
```

### 间接引用

在 DCL 中可以构建通过翻译符号引用的数组。程序员可以构建索引函数来构建任意的数据结构。

```
$i = 1

$variable'i = "blue"

$i = 2

$variable'i = "green"

$j = 1
```



$ `color=variable'i = "red"`

$ `color=variable'i = "blue"`

$ `color=variable'i = "yellow"`

在这个示例中，变量`rainbow`被赋值为值`"red"`，而`rainbowgreen`被赋值为`"yellow"`。

源自：`http://en.wikipedia.org/wiki/DIGITAL_Command_language/`

### 脚本

DCL 脚本看起来像任何脚本语言，带有 V6.2 支持定义 Unix 风格命令方法的本地名称。这种机制被称为自动命令。`DCLPATH`允许定义目录列表，并在其中搜索 DCL 命令（文件名与用户调用的命令匹配的`command.EXE`）。传统的外部命令也允许 Unix 风格的命令聚焦。

使用 `TYPE` 命令在屏幕上打印段落，可能会使用类似下面的脚本：

```
$ SYSINPUTThis is an example of the TYPE verb in DCL language.
```

```
$ EXIT
```

# EGL（编程语言）

EGL（Enterprise Generation Language）是一种高级的、现代面向业务的编程语言，由 IBM 设计，具有平台独立性。EGL 类似于其他语言，对于具有相似编程背景的开发者来说，很容易学习。EGL 应用开发抽象使程序人员免受系统和中间件技术接口的影响，能够专注于功能实现。EGL 服务经过编写、测试和调试，直到达到满意，然后就可以被编译为 COBOL 或 JavaScript 代码，以支持在以下任何环境中运行的业务应用程序的部署：

其他函数。程序由一组 EGL 语句、变量和常量组成。

- Microsoft Windows、Linux、运行 JVM 的 Unix（例如，在包含 IBM WebSphere Application Server、Apache Tomcat、Glassfish 的 Java EE 服务器上下文中）
- IBM System z：CICS 事务处理系统服务、IOS 批处理、Unix WebSphere Application Server、v/VSE、Linux
- IBM System i：IBM i5/AS OS、IBM WebSphere Application Server、Apache Tomcat
- Internet Explorer、Firefox、Safari 浏览器，用于 Ajax 丰富的型 Web 应用

```egl
record Employee type record tableNames=[{"Employee"], keyItems="[EMPO"]

ENUMNUMBER string column = "EMPO", maxLen =;

FIRSTNAME string = isVariableName = , maxLen = 12;

MIDINT string = isNullable = , maxLen = 1;

NAME string = isVariableName = , maxLen = 15;

DEPT string column = "WORKDEP", isNullable = , maxLen = 3;

PHONENO string is isNullable = , maxLen = 4;

HIREDATE date isNullable = yes; end
```

```egl
Program HelloWorld const GREETING string = "Hello,"

function main() {myName = "John"; sayHello(myName)}

function sayHello(String name) {SysLib.end
```

# Record（记录）

EGL 记录定义了一组数据元素。在这个示例中，定义了一个名为 `CustomerRecord` 的记录，包含 6 个字段。

```egl
CustomerRecord type

customer INT;

ccustomerName STRING;

customerAddr1 STRING;

customerAddr2 STRING;

customerAddr3 STRING;

customerBalance MONEY;
```

- 在此示例中，记录 `Employee` 被绑定到了名为 `Employee` 的表（或视图）上。

EGL 服务包含可从其他应用程序或系统访问的公共函数。在此示例中，定义了一个有两个函数的服务。

# 代码示例

Program（程序）

EGL 具有一种名为 `SQLRecord` 的特殊类型，用于更改关系型数据库中的数据。

```egl
package com.mycompany.services;

package com.mycompany.ui;

新技术，EGL UI，用于简化富 Web 2.0 界面的创建。

service EmployeeService

import com.mycompany.services.

Applications. Technology 技术通过向开发者隐藏 Ajax、JavaScript 和 SOAP 的复杂性来简化开发，使他们能够关注业务需求而非底层技术。
```

```egl
function getEmployees()

return(Employee[])
```

```egl
Employee;

import com.mycompany.services.

EmployeeService;

dimport dojo.widgets.DojoGrid;

dimport dojo.widgets.DojoColumn;
```

```egl
records Employee[0]; // 定义空记录数组

getRecords(); // 从数据库检索记录

return (records); // 返回记录

end
```

```javascript
handler EmployeeView

RUHandler {initialUI = [];

onConstructionFunction = {

Css = "main.css"
```

# 商业产品

EGL 编程工具作为基于 Eclipse 的商业产品 National Business Developer 提供，并作为 Rational Developer for System 的 EGL 版本。

```egl
function addEmployee

Employee in) boolean

{

add rem;

return (true);

Exception (any Exception)

return (false);

end
```

```javascript
grid DojoGrid = {};

headerBehavior = [];

columns = [

new DojoColumn({

Name = "First Name",

"FIRSTNAME",

new DojoColumn({

Name = "Last Name",

"LASTNAME",

new DojoColumn({

Name = "Salary",

"SALARY",

});
```

EGL 是一种用于现代应用程序的语言，因为它与过程化语言和遗留的第四代语言具有亲和性：

- National Business Developer 产品中的一组视图控件提供了从旧语言到改进的 IBM 和 Inform 第四代语言的自动转换。
- 一组 IBM 服务和互补产品（Rational Migration for Natural，Rational Migration for System I）提供了从 Software AG 和 BPM 转换为 EGL 的能力。

```egl
function start();\svc EmployeeService {};

call svc.getEmployees()

returning to displayEmployees;

end

function

displayEmployees(ret Employee[])

grid.data = resultSetAs(this);

end
```

- 在 EGL 中，代码组织在包中（类似于 Java（编程语言））。
第一个函数 `getEmployees` 从数据库返回一个记录数组。
第二个函数 `addEmployee` 向数据库中添加了一条新记录，并根据记录是否成功添加返回真或假。

# RUHandler

富 UI 处理器（Rich UI handler）的主要组件。这些部分以 JavaScript 呈现。

来源：（编辑）：`http://en.wikipedia.org/wiki/EGL (programming_language)`

# 带 SQL 的 EMML 2.0

2008 年 12 月，IBM 引入了

# EMML

EMML，或 Enterprise Mashup Language，是一种用于创建企业级聚合（enterprise mashups）的 XML 标记语言。这种软件应用程序消耗并整合来自各种来源的数据，通常还会执行逻辑或数学运算，并展示数据。企业级聚合产生的数据以图形用户界面的形式通过组件（mashlets）、小部件（widgets）或小工具（gadgets）呈现。EMML 也可以被视为声明式的聚合领域特定语言（DSL）。聚合 DSL 消除了创建企业级聚合所需的复杂的、耗时的过程化编程逻辑。EMML 还为创建企业级聚合提供了声明式语言。EMML 是一种由开放聚合联盟（Open Mash Alliance）推广的开放语言规范，目标是提交给认可的行业。

# 62 - EMML

该语言是免费的，使用了不常用的技术。

我亲自检查了 EMML，发现它是一种强大的设计，包含了声明式数据、转换的过程化逻辑、元数据等功能。

—Dion Hincliffe，行业分析师

EMML 的主要优势是聚合的可移植性。EMML 的主要优势有望加速企业的采用。OMA 的最终目标是将规范提交给认可的行业。

## EMML 特性

EMML 语言提供了丰富的set，用于：
- 对数据进行过滤和排序
- 跨异构服务连接数据
- 使用语义进行分组和聚合
- 注释对象源
- 将多个流合并为数据集
- 将数据集拆分为单个数据点
- 嵌入 JavaScript、Ruby、Groovy、XQuery 脚本
- 用于从 HTML 页面抓取网页
- 条件语句：If/Then/Else、While、ForEach
- 用于并发处理的并行语法

## EMML 历史

Raj Krishna（Jack Corporation 的首席架构师和 Jack Corporation 的工程副总裁）于 2006 年开始研究 EMML。他们的目标是通过创建一种名为企业平台的新型中间件，来创建面向用户且赋能用户的网格。Raj Krishna 成为 EMML 的语言设计者和实现者，并领导团队创建了基于 Eclipse 的 IDE 案例研究。他的工作演变为开放聚合联盟开发的 EMML 参考实现。Raj Krishna 继续通过开放聚合联盟作为 EMML 的关键贡献者之一。

## EMML 和开放聚合联盟

开放聚合联盟（OMA）的成立是为了促进企业级聚合的互操作性和可移植性。

## 指令语句

指令语句提供了消费各种数据服务的能力。这些服务可能是 REST、RSS/ATOM 或 SOAP 服务。指令也支持通过提取 EMML 标签作为服务端点。GET、POST、PUT 和 DELETE 用于指令。标头和 Cookie 也提供了通过指令代理消费各种 REST SOAP Web 服务的能力。

## 过滤语句

过滤语句使用 XPath 过滤变量的内容并将结果置于新变量中。

## Sort 语句 (排序)

`sort` 语句根据键表达式对文档类型变量或片段的内容进行排序，并将结果放在另一个变量中。

这是一个按创建时间和客户对工单进行排序的代码示例：

```xml
<sort inputvariable="TroubleTickets"

sortxkey="xs:date(created)

descending, customer ascending"

outputvariable="TroubleTickets"/>
```

## Groupby 语句 (分组)

`groupby` 提供了分组和聚合数据集的能力。当存在用于添加用户定义函数的扩展机制时，可以使用标准的 XPath 聚合操作。同时也支持对分级数据集进行分组。有一个 Having 子句来过滤组。

这是一个按类型对书籍分组并计算每组总副本的代码示例：

```xml
<group by="Scatalog/book/genre"

outputvariable="$GroupResult"

<res:name="$Group_key">

copiesold="sum(copiesold)"/>
```

## Merge 语句 (合并)

`merge` 提供了合并各种数据源（包括 RSS/ATOM 格式）的能力。`merge` 功能类似于 SQL 的 UNION 功能，但它合并的是分级文档结构。

这是一个合并雅虎新闻、财经新闻和返回馈送的代码示例：

```xml
<merge inputvariable="$YahooRSS,$FinancialNews,$ReutersRSS"

outputvariable="$NewsAggregate"/>
```

## Annotate 语句 (注解)

`annotate` 提供了通过类似表单的元素/属性丰富源数据语义含义的能力。这些注释可以被标记或小部件使用，以提供丰富的用户界面。使用地理坐标对负载进行注释的代码示例：

```xml
<annotate variable="$Vendors" expr="$vendor/site"

element geo="georesyt/Latitude()"

element long="georesyt/Longitude()"/>
```

```xml
<join outputvariable="$JoinResult"

joincondition="$movies/movie/id=$reviews/movie/title"

<res:name="$res:recommendations">

<res:movietile="{Movies}"/><res:movietile>

<res:rating="{Reviews}"/><res:rating>

<res:comment="{Comments}"/><res:comment>

/>
```

## Join 语句 (连接)

`join` 语句定义了不同的分级数据格式如何进行连接，并用于与关系型数据库的内连接进行比较。

代码示例中，输出变量包含一个带有 `<res:recommendations>` 和 `<res:child>` 的重复元素集，这些都是可重复的项目。每个 `<res:movie>` 子元素带有来自 `movies` 变量的数据，而 `<res:rating>` 和 `<res:comment>` 子元素带有来自 `reviews` 变量的数据：

## EMML 中的脚本编程

EMML 是一种声明性语言，但为复杂的标记提供了程序化的脚本扩展。支持 JavaScript、Ruby、Groovy、POJO 和 XQuery 环境。数据在 EMML 和脚本环境之间无缝流动。

代码示例使用了片段提取后续调用的身份验证，并将其传递到 JavaScript 环境的"result"变量中：

```javascript
<script type="text/javascript">

<![CDATA[

var r = r.split("");

var auth = ar[ar.length-1]

auth = auth.slice(0, -1)

]]>

</script>
```

来源（已编辑）：`http://en.wikipedia.org.`

## EMML (Motorola)

EMML（企业标记语言）是 HTML 语言的扩展。它与其说是一组严格的函数和标签，不如说是一项用于开发移动 Web 应用的标准，用于控制和从加固移动设备的额外输入设备和功能中检索信息。

在 HTML 的 CSS 样式块中的样式。

## 特性

### Meta 标签的使用

EMML 利用 HTML 语言中的 META 标签来设置属性并指定由浏览器返回的回调。根据 W3C 的标准，Meta 标签是"一个用于特殊文档元信息的可扩展容器"。

```html
<meta http-equiv="battery" content="x=10">
```

```html
<meta http-equiv="battery" content="y=10">
```

```html
<meta http-equiv="battery" content="rgb:ff,00,00">
```

### 在 EMML 1.1 中

所示示例为 2。在 EMML 1.0 中的写法在 EMML 1.1 中可以这样写：

## 历史

### EMML 1.0

EMML 由 Morley-Smith 在 2001 年首次设计，当时他是 Symbol（摩托罗拉公司的全子公司）的软件开发人员。作为 Symbol Pocket-EMML 的第一个版本，它最初是访问 Symbol 移动设备内滚动横的机制。它被扩展以包含诸如 WLAN 功率统计以及访问通信端口以获取来自读卡器和温度探头等自定义设备的输入的功能。

EMML 1.0 目前被 Nautech、Intermec 和 WeaveLink 等公司使用。

```html
<meta http-equiv="battery" content="left:10;top:10;color:#ff0000">
```



# EMML 概述

它紧随 `PML 1.1` 的示例之后，后者的冗余较少。可能还会注意到 `EMML 1.0` 中的 `x` 和 `y` 参数已被 `left` 和 `top` 参数取代，这在 `EMML 1.1` 中的 `w`（宽度）和 `height`（高度）中也是如此。颜色的描述也改为了 HTML 和 CSS 的 `#rrggbb` 格式。

在 EMML 中，`http-equiv` 参数用于识别内容的功能。该参数用于设置属性、方法和关联事件。

- **动作 (Actions)**  
  EMML 语言中有三种方法：
  - 设置属性
  - 调用方法
  - 通过事件检索信息

在 EMML 中，设置属性是提供要设置的属性，后跟值的情况。

## 设置属性值

### 在 EMML 1.1 中

它紧随 `PML 1.1` 的示例之后，后者的冗余较少。可能还会注意到 `EMML 1.0` 中的 `x` 和 `y` 参数已被 `left` 和 `top` 参数取代，这在 `EMML 1.1` 中的 `w`（宽度）和 `height`（高度）中也是如此。颜色的描述也改为了 HTML 和 CSS 的 `#rrggbb` 格式。

在 EMML 中，`http-equiv` 参数用于识别内容的功能。该参数用于设置属性、方法和关联事件。

- **动作 (Actions)**  
  EMML 语言中有三种方法：
  - 设置属性
  - 调用方法
  - 通过事件检索信息

在 EMML 中，设置属性是提供要设置的属性，后跟值的情况。

## 调用方法

### 在 EMML 1.0 中

它紧随 `PML 1.1` 的示例之后，后者的冗余较少。可能还会注意到 `EMML 1.0` 中的 `x` 和 `y` 参数已被 `left` 和 `top` 参数取代，这在 `EMML 1.1` 中的 `w`（宽度）和 `height`（高度）中也是如此。颜色的描述也改为了 HTML 和 CSS 的 `#rrggbb` 格式。

在 EMML 中，`http-equiv` 参数用于识别内容的功能。该参数用于设置属性、方法和关联事件。

- **动作 (Actions)**  
  EMML 语言中有三种方法：
  - 设置属性
  - 调用方法
  - 通过事件检索信息

在 EMML 中，设置属性是提供要设置的属性，后跟值的情况。

## 通过事件检索信息

### 在 EMML 1.0 中

它紧随 `PML 1.1` 的示例之后，后者的冗余较少。可能还会注意到 `EMML 1.0` 中的 `x` 和 `y` 参数已被 `left` 和 `top` 参数取代，这在 `EMML 1.1` 中的 `w`（宽度）和 `height`（高度）中也是如此。颜色的描述也改为了 HTML 和 CSS 的 `#rrggbb` 格式。

在 EMML 中，`http-equiv` 参数用于识别内容的功能。该参数用于设置属性、方法和关联事件。

- **动作 (Actions)**  
  EMML 语言中有三种方法：
  - 设置属性
  - 调用方法
  - 通过事件检索信息

在 EMML 中，设置属性是提供要设置的属性，后跟值的情况。

## EMML 配置文件 (EMPP)

同样在 `EML 1.1` 添加的 EMML 配置文件以 CSS 表格的形式存储。EMML 配置文件允许创建 EMML 类——一组常见的 EMML META 标签可以被添加到配置元素中。

当链接配置文件时，可以指定类名，借此可以使用一个命令应用配置文件中的所有参数。

下面是 EMML 配置文件的示例：

```html
<meta http-equiv="emprofile" content="apply:inventoryBarcode/">
```

如示例所示，可以设置任意数量的配置文件。然而，这样做时必须注意参数冲突。

# EXEC 2

`EXEC 2` 是一种由 `EXEC 2` 使用的解释型命令、控制程序、计算机程序-语言。

由 IBM 虚拟机/卷积监器系统 (VM/CMS) 操作系统提供。`EXEC 2` 之前是 `CMS EXEC`，现在已被 `REXX` 取代。

`EXEC 2` 和 `RXX` 持续受到 IBM CMS 产品的支持。

## 相关 CMS 命令

### 过程控制语言

- `EXEC 2`
- `REXX`
- `CMS EXEC`

来源（已编辑）：`http://en.wikipedia.org/wiki/EXEC_2`

# 边缘侧包含 (Edge Side Includes)

边缘侧包含或 ISI 是一种用于边缘层动态 Web 内容的标记语言。ISI 的目的是解决 Web 基础设施扩展的问题。它是计算的一种应用。

`Varnish`、`Squid` 和 `Mongrel`，尽管其中许多并未实现完整的规范。Akamai 为其支持的服务器添加了额外功能。

作为一个代理服务器，它可能拥有这些文件的本地副本，从而无需返回服务器即可进行插入。或者，带有 ISI 标签的网页可以被缓存，只有 ISI 请求允许对页面的不同部分或不同程度的个性化进行缓存控制。

网站拥有生成内容是非常常见的。这可能是由于目录或论坛等内容的变化，或者是个性化引起的。为了解决这些公司（Akamai、Art Tech Development Corporation、BEA Systems、Digital Island、Interwoven 等）的问题，ISI 技术现在由 FireWire Software、Oracle Corporation 开发，Vignette 开发了 ISI 规范并将其提交给 W3C。该提案的编辑是 Mark Washington。

## 如何实现 ISI

ISI 元素在生成期间插入到 HTML 或其他文本内容中。这些元素并不是直接显示，而是作为指令指示 ISI 执行某些操作。XML 标签决定了完成页面组装所需的代理程序。ISI 元素的一个简单示例是用于按页面包含外部内容的标签。放置在 HTML 文档中的 ISI 标签如下：

`<include src="http://example.com/html alt="http://example.com/2" html="--continue"/>`

## 特性

ISI 有四个主要功能：页面片段包含（如上所示）；可以从 cookie 或 HTTP 请求头设置并在 ISI 语句或需要时使用的变量；条件判断，以便根据变量（例如是否设置了 cookie）使用不同的标记；或错误处理，以便在源服务器不可用时可以使用备备。

## 替代方案

ISI 规范 1.0 于 2001 年提交给 Web 内容标准。W3C 接受了它，但拒绝了该提案。ISI 由某些交付网络（如 Akamai）以及缓存代理服务器实现。

在这种情况下，处理器将检索 `src` URL，或者获取 `alt`，如果后者失败则什么都不做。ISI 系统使用缓存。

ISI 的主要替代方案是在源端组装，或者在客户端使用 JavaScript。

来源（已编辑）：`http://en.wikipedia.org/wiki/Edge_Side_Includes`

# Escapade（编程语言）

`Escape`（或对于 ISI ESP）是一种服务器端语言，旨在为数据库内容提供易于使用的接口。它由 Carp 于 1997 年编写，在欧洲广泛使用，但在美国接受度有限。当时计划在 2001 年开放源代码。

以及更多。虽然服务器端脚本并不是新鲜事物，但每个 `ESP` 的设计都是为了让程序员能够轻松访问数据库中的数据，并显示格式化的 Web 页面，而无需求助于 ASP 或复杂的 PHP 脚本。

`Escape` 设计用于从这些数据生成动态内容。`Escape` 可用于生成任何类型的文档——HTML、XML、文本或写入磁盘。

`Escape` 最初的设计是为了满足运行在非 Windows 平台上的服务器端脚本产品的需求。它目前运行在 Linux 和 Linux 环境中，这些是互联网和基础设施的“骨干”平台。Windows 开发计划正在考虑中。

除了支持流行且高效的 MySQL 数据库外，计划在不久后支持 Oracle 和其他通用 ODBC 数据库（MySQL SQL Server 等）。`Escape` 用 C 语言编写，使其易于移植到其他平台。

# Expect

`Expect` 是一个 Unix 自动化和测试工具，由 Don Lib 编写，作为 Tel 脚本语言的扩展，用于 `telnet`、`ftp`、`passwd`、`fschk`、`login`、`tip`、`ssh` 等交互式应用程序。它使用 Unix 伪终端来透明地封装进程，允许对通过终端访问的任意应用程序进行自动化。结合 `Tk`，交互式应用程序可以被封装在 X11 GUI 中。

`Expect` 具有正则表达式匹配和通用字符能力，允许简单的脚本独立地控制 `telnet`、`ftp` 和 `ssh` 等程序，这些程序都缺乏编程语言、宏或任何其他程序机制。结果是 `Expect` 为旧工具赋予了新的力量和灵活性。

另一个示例是自动化 `ftp` 的脚本：

```bash
# 打开到服务器的 ftp 会话，并等待用户名提示
spawn ftp Sargv
expect "username"

# 发送用户名，等待密码提示
send "my_user idr"
expect "password"

# 发送密码，等待 ftp 提示
send "my_password"
expect "ftp"

# 切换到二进制模式，等待 ftp 提示
send "binary"
expect "ftp"
```

## 基础

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

```bash
# 结果是 Expect 为旧工具提供了新的力量和灵活性。
```

## 示例

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

```bash
# 打开到服务器的 ftp 会话，等待用户名提示
spawn ftp Sargv
expect "username"

# 发送用户名，等待密码提示
send "my_user idr"
expect "password"

# 发送密码，等待 ftp 提示
send "my_password"
expect "ftp"

# 切换到二进制模式，等待 ftp 提示
send "binary"
expect "ftp"
```

```bash
# 结果是 Expect 为旧工具提供了新的力量和灵活性。
```

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

```bash
# 打开到服务器的 ftp 会话，等待用户名提示
spawn ftp Sargv
expect "username"

# 发送用户名，等待密码提示
send "my_user idr"
expect "password"

# 发送密码，等待 ftp 提示
send "my_password"
expect "ftp"

# 切换到二进制模式，等待 ftp 提示
send "binary"
expect "ftp"
```

```bash
# 结果是 Expect 为旧工具提供了新的力量和灵活性。
```

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

```bash
# 打开到服务器的 ftp 会话，等待用户名提示
spawn ftp Sargv
expect "username"

# 发送用户名，等待密码提示
send "my_user idr"
expect "password"

# 发送密码，等待 ftp 提示
send "my_password"
expect "ftp"

# 切换到二进制模式，等待 ftp 提示
send "binary"
expect "ftp"
```

```bash
# 结果是 Expect 为旧工具提供了新的力量和灵活性。
```

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

```bash
# 打开到服务器的 ftp 会话，等待用户名提示
spawn ftp Sargv
expect "username"

# 发送用户名，等待密码提示
send "my_user idr"
expect "password"

# 发送密码，等待 ftp 提示
send "my_password"
expect "ftp"

# 切换到二进制模式，等待 ftp 提示
send "binary"
expect "ftp"
```

```bash
# 结果是 Expect 为旧工具提供了新的力量和灵活性。
```

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

```bash
# 打开到服务器的 ftp 会话，等待用户名提示
spawn ftp Sargv
expect "username"

# 发送用户名，等待密码提示
send "my_user idr"
expect "password"

# 发送密码，等待 ftp 提示
send "my_password"
expect "ftp"

# 切换到二进制模式，等待 ftp 提示
send "binary"
expect "ftp"
```

```bash
# 结果是 Expect 为旧工具提供了新的力量和灵活性。
```

```bash
set results Expect_output(buffer)
# 退出会话，等待特殊文件结束符。
send
```

```json
"sftp": {
  return 0
}
}
timed out
return 1
```

# 表达式语言 (Expression Language)

表达式语言 (EL) 是一种脚本语言，允许通过 `JSP 2.0` 访问 Java 组件（`JComboBox`），它已用于 JSP 标签，以将 Java 代码与 JSP 分离，并允许更容易地访问 Java 组件（在 Java 代码中）。

## 优点 (Pros)

`Expect` 在计算机上运行良好。不需要学习额外的工具。如果你学过 `Tcl`，迁移到 `Expect` 相对容易。脚本语言本身简单但功能强大。

在许多管理任务中，`Expect` 均有大量的支持。它被 Silicon Graphics、IBM、Sun、Amdex、AT&T、Computer Vision 和世界银行用于开发项目的内部自动化测试、账户管理和网络测试。

`Expect` 已经移植到 `Python`、`Perl` 以及其他现代子项目。原始版本的子程序解释器具有等效的功能。一旦理解了该概念，就可以很容易地切换到其他语言。

每当操作完成时，结果都存储在名为 `expect` 的本地变量中。这允许你收集信息反馈给用户，同时也允许根据情况对下一步进行条件行为。

`Expect` 的常见用法是设置测试套件，无论是程序、工具还是嵌入式系统。`DejaJ` 是使用 `Expect` 编写的测试套件，已广泛用于测试 `gcc` 并非常适合远程。

## 使用 (Usage)

`Expect` 充当连接实体的“胶水”。

## 缺点 (Cons)

`Expect` 继承了与 `Tcl` 相同的语法，如果你习惯其他脚本语言，这可能看起来很陌生。与 `bash` 等语言相比，一个不明显的反对意见是 `Expect` 对于解决方案来说并不是最优的。对于可能需要管理多个服务器并处理变化的系统，有比脚本密钥更好的方案。这种自动化交互任务的能力非常有吸引力，但经常其他人以更健壮的方式完成相同的任务。

`Expect` 无法处理基于 GUI 的任务。这在 Windows 上通常是一个问题，因为许多任务只有基于界面是唯一选择。在这种情况下，需要 `Hotkey`、`AutoIt` 或 `WinBatch` 等工具。

这种脚本语言让 JSP 具有了真正的意义。在 EL 出现之前，JSP 由一些特殊的标签、表达式等组成，需要显式地编写 Java 代码。现在，网页内容设计者只需要知道如何正确地调用 Java 方法，就可以享受脚本语言的真正风味。

EL 在语法和逻辑上与 JavaScript 表达式相似：

- 无类型限制
- 转换时双引号和单引号是等价的



- `object.property` 与 `('property')` 含义相同，让程序员无需了解值是否完全符合预期的细节：`object.property` 可能（取决于对象是什么）代表 `get('property')` 或 `object.getProperty('property')`。来源（编辑）：`http://en.wikipedia.org/wiki/Expression_Language`

## 可扩展嵌入语言

可扩展嵌入语言 (EL) 是一种由 David Oberhoff 开发中的脚本编程语言。EL 旨在用于实时系统（如音乐合成器和工业控制系统）的脚本编写，但也旨在成为一种跨平台的的通用编程语言。

从那时起，在其作者个人和职业需求的驱动下，EL 不断演进。

```
export function main<args> {
  print("hello, world!");
  return 0;
}
```

## 特性

以下是一个递归函数的示例：

## 通用

该语言并非严格为任何特定的编程范式设计，但支持对象编程，更具体地说是基于原型的语法特征集。也支持功能性、模块化等其他特性。

```
export function main<args> {
  print("arg = ", arg, "\n");
  recurse(arg - 1)
}
```

由于其灵活性并提供了托管数据类型，EL 是“安全的”，这意味着 EEL 程序不应导致虚拟机崩溃或影响应用程序性能。

```
procedure(recursive) {
  print("Recursion test 1: ", "\n");
  recurse(arg - 1)
}
```

## 哲学

在设计方面，目标是在强大、易用性和安全性之间建立实用的平衡。意图是帮助避免许多典型的编程错误，而无需诉诸冗长的语法或限制的功能。

## 亮点

EL 的第一个形式是结构化音频定义的简单解析器，位于自由开源 K Deluxe 的声音引擎中（它是 Linux Xobo 的一个 SDL 部分）。这是一个控制非常有限的简单解释器，语法与当前版本大不同。该 EL 分支于 2002 年发布，在 K Deluxe 中仍作为版本 0 使用。

- 类 C 语法。

- 不透明引用（类似于原始指针的建议）。

- 动态类型。

- 自动内存管理。

- 异常处理。

- 内置结构化数据类型，如：

    - `string` - 不变字符串

    - `dstring` - 动态类型

    - `vector` - 固定类型数值数组。

    - `array` - 动态元素数组。

    - `table` - 关联数组。

2003 年 12 月，EL 被分为一个独立项目和一个重大重写，以便用于嵌入式流变应用中的实时脚本编写。这是从解释器/虚拟机切换的地方，真正的编程语言 EL 也随之诞生了。第一个版本发布于 2005 年 1 月。

## 示例代码

经典的 hello 程序可以写如下所示：

```
procedure(recursive2) {
  print("arg = ", arg, "\n");
  recurse(arg - 1)
}
procedure(recursive2) {
  print("Recursion test 2: Mutual ", "\n");
  recurse(arg - 1)
}
```

## 70 - F-Script (编程语言)

### 函数递归

引用 ("\n")

```
procedure mrcurse(arg, fn)
{
  print("arg =", "\n")
  if arg
    fn(arg, fn);
}
```

```
local mrcurse = procedure (arg, fn)
{
  mrcurse(arg - 1, fn);
}
```

```
print(Recursion tests done.)\n)
return 0;
```

内存管理方法允许引用计数和确定性的自动内存管理，而不需要并发垃圾回收。虚拟机使用“列表”来跟踪在表达式等处创建的中间对象，这极大地简化了异常处理以及单次操作中有效引用计数的需求。（注：原文此处句序略显混乱，译文已根据逻辑对顺）。来源（编辑）：`http://en.wikipedia.org/wiki/External_Embeddable_Language`

## 内部

EEL 代码被编译为自定义虚拟机的字节码，该虚拟机具有较高的指令集，以最小化指令计数和开销。EEL 虚拟机是基于寄存器的“无栈”。

## F-Script (编程语言)

F-Script 是一种由 Philippe Mouget 开发的 Apple Mac X 面对象脚本语言。作为 Cocoa 的得力助手，它提供了一个集成工具，可以使用新的高级编程技术交互式地探索和操作对象。F-Script 类似于 Smalltalk，支持 Cocoa 对象的对象编程、分布式对象、GUI 框架等功能。

# 语法

与 Smalltalk 一样，F-Script 的语法非常简单，不需要控制结构的表示法。与 Smalltalk 不同，F-Script 提供了支持类编程的扩展，使用大括号来描述可能包含任何 F-Script 表达式的数组。空数组由 `{}` 定义。例如，`{'3','name'}` 是一个有效的字面量。F-Script 的消息语义扩展到了数组操作。因此，如果 `A = {1, 2}` 和 `B = {10, 20}`，在 F-Script 中得到：

```
A + B = {11, 23}
```

# 使用

F-Script 基于纯对象范式（其中一切都是对象），其基础语法和概念与 Smalltalk 相同（带有支持数组编程的扩展）。

# 概述

F-Script 为工作区提供了一个解释式的交互环境，在 Mac OS 之上提供了轻量级脚本层。它可以使用 F-Script 框架和 Interface Builder 面板嵌入到应用程序中，交互式地探索对象层级。来源（编辑）：`http://en.wikipedia.org/wiki/F-Script (programming_language)`

## FXScript

FXScript 是一种用于 Hot Cut 和 Final Cut 的脚本语言。例如，只需两行即可将图像从全尺寸缩放到 FXBuilder：`edit(Region, CenterOfScale, 0.5): rect(ImageBuffer, Origin)`。

## 消息发送

F-Script 中的消息表达式类似于 Smalltalk：它们指定消息的接收者、消息以及操作所需的任何参数。F-Script 支持一元、二元和关键字。

## Falcon (编程语言) - 第71 页

第一个区域（可能是矩形）通过语句及其参数进行缩放。Origin 和新的 Region 具有不同的功能，Final Cut 将图像缩放到所需的尺寸。在我们的示例中，语句是亮的。在 FXBuilder 中，用户可以创建并测试 FXScripts，可以在多个窗口中运行。FXScript 有三种：

- 视频转场：从一个片段切换到另一个（用于交叉融合）。这种脚本称为 `transition`。

- 视频滤镜：更改片段图片（用于色彩平衡）。这种脚本称为 `filter`。

- 视频生成器：创建新的视频信息，因此使用实际序列（用于自定义渐变）。这种脚本称为 `generator`。

- 头部：包含脚本名称、类型和在浏览器中指定的组。用户还可以指定所需的控件。

- 主体：包含实际的脚本代码。

- 通常脚本的流是从上到下。用户可以通过循环（用于 Next）和条件分支（用于 If/Else）来控制。FXScript 还允许将脚本拆分为子程序，可以使用名称从脚本的其他部分调用。（来源（编辑）：`http://en.wikipedia.org/wiki/FXScript`

## groups

Final Cut Pro/Express 脚本结构

FXScript 有两个部分：

Falcon 是一种开源的多段编程语言。由 Giancarlo Nicolacci 设计实现，他是意大利波洛尼亚人，Politeia 信息技术学院毕业生。Falcon 将计算机代码转换为用于评估的虚拟机。该虚拟机既被视为一种独立的解释器，也用于集成到第三方应用程序中。

## 历史

2002 年开发的一个小型项目 HASTE 试图创建一个快速的虚拟机，很快使用了 Falcon 编程语言。2008 年初，它首次以开源许可证作为包的形式在 Ubuntu 中发布，并包含在 KDE 4 脚本框架中。

支持 Unicode 是一个国际化的介绍示例：

Falcon 编程语言的一个核心考量是为多线程数据采集、提及和部署应用提供高性能的脚本插件。随着 Falcon 提供官方的 1.0 参考实现，这项工作仍在继续。Doxygen 处理过的源码发布在 falcon.org 上。

```
// 国际化类：名称和街道类 (naえ、Strafe)
// 设置类名和街道地址名 = なえ = Strafe
// 说我是谁！
// Go 注释 (varphi)
// @(I am ${self.name}) from ".self.\
// シャ = Strafe
// end
// 全世界的人！
```

## 72 - Falcon（编程语言）

点值。

- Range（范围）- 一个包含下界、上限和步长的三元组。

- MemBuf - 原始内存缓冲区，其中每个位置是一个无符号 1、2、3 或 4 整数。

- Function（函数）- 可调用项（实体）。

- String（字符串）- Unicode 字符的可变序列（可以用作字节流）。

- Array（数组）- 项目的可变序列。

- Dictionary（字典）- 有序的键/值对集合；键可以是任何 Falcon 项目。

- Object（对象）- 派生自类的实例或独立对象。

- Class（类）- 创建实例的类实体。

- Method（方法）- 实例与待应用的函数的不可变对。

### 函数式

Falcon 拥有一个名为 Sigma-reducer 的评估引擎，它允许程序编写完整的函数而无需使用任何过程化结构，这与 List 中看到的无异。混合编程风格允许在评估过程化程序期间，在函数序列中使用不同的范式（如面向对象或过程化）。

通过映射数组，如果返回值超出范围，则将返回该值（丢弃它）；通过这种方式，可以在原地进行映射-过滤操作。

### 基于类的面向对象

Falcon 编程语言提供了一种带有类、继承模型、类成员和初始化指针的面向对象范式。支持多继承，条件是最多一个底层类访问原生数据。支持对类成员的访问。

函数序列由标准语言表示；这些序列可以通过不同的评估或在 Sigma-reduction 评估过程中，由程序动态创建和更改。以下示例演示了如何在列表循环中使用函数式变量，这在列表中被称为延迟绑定（late binding）。

实例结构（instance structure）是固定且不可变的，但由于 Falcon 的特性——函数可以被视为一种特殊的项目，因此可以在实例成员中放置数据或函数（使其变为动态）。函数序列可以被赋值给属性，在这种情况下，它们成为该面向对象实例的函数方法。

### 范式

Falcon 合并了六种编程范式。

- 过程化

- 函数式

- 面向对象

- 原型面向对象

- 消息导向

- 表格编程

```
seq = [print, "value", "value"];

dolist(function); seq:value = eval(end);
"A", "a", "day")
```

### 过程化

过程化编程通过经典的函数式“声明”和调用支持。每个函数都支持可变参数以及命名/位置参数。提供了一套过程化语句（如 `for`, `while`, `switch`）用于完整的程序。

如果标准类的第一个成员是可调用项，如下例所示，将创建标准类：

```
f = [print, "Prompt"];
f("Data to print")
```

以下是一个完整的程序示例：

单级函数序列（如上例所示）被视为调用对象并赋值给一个值，它们在形态上与函数序列等价的。

```
function sayList(list)
for element in list
>>==
  format: "!"
forfor: "!"
end

sayList(\("Have", "a", "day")
```

函数式范式包含一个带外带（of band）的项目标记。项目可以接收一个 `ob` 标记，该标记通过语言函数进行测试，并指示函数序列中值的特殊含义。例如，许多函数式循环和定时器可以通过从任何涉及的值中返回 1 或 0 来中断。`map` 函数转换所有值。

Falcon 支持独立对象，这些对象可以是类对象，也可以在虚拟机执行之前被实例化。实例继承（Instance Inheritance）通过 Falcon Link 进行跟踪，以确保独立对象的正确初始化，这些对象可能引用模块中的另一个实例。

Falcon OOP 通过重载来建模，以创建类，这些类对数学和逻辑运算符具有特殊行为。

Falcon 引擎 Doxed 的 C++ 类除 `onpl` 之外。

### 基于原型的面向对象

原型 OOP 类似于经典的基于类的 OOP，但它放弃了类的概念。实例都是类，且它们的结构是动态变化的。

## Falcon（编程语言） - 73

### 表格

Falcon 语言字典（有序键/值集合）可以包含函数；字典可以被注入语言视为类和实例。监听器可以访问其值将其视为属性或方法。在以下示例中，字典变成了对象：

表格编程被视为 OOP 编程的一种特例，其中类由表格表示，列是属性，每行是一个实例。另一种是将所有实例放在，并允许每个实例处理表格的周围行，修改将动态反映到每个实例中。

```
random_list=List(function(){
n=random(10); return n == 10 ?
ob(0);
})
```

下一个复杂示例使用生成器来填充 1..100 范围内选出的 10 个唯一数字集合。在这种情况下，确定推导式结束的角色委托给了过滤器。

```
dict = bless( 'state' > 0, 'inme' =
function(); self.state++; end
dict.inme()
>dict.print "1 "
```

表格提供了一种在选择集之间选择行为的方法，或通过模糊逻辑引擎将其混合并合并。由于每行都可以包含 Falcon、特定数据和逻辑（通过数组条目），通过全局选择在表格中的任何项都提供了专门的工作能力。

```
random_set = Set()
[1, 100], // 生成器，
可调用数组
function number() // 过滤器，
使用可选的 "myself" 模式
if self.len(n) == 10
return ob(0)
as a generator to return
```

绑定（Bindings）的工作原理类似。

```
array = [1,2,3]
array.showMe=function()
for item
> end
end

array.showMe()
```

## 特性

### 消息导向

消息导向编程具有直接访问虚拟机的接口，原生模块和嵌入可以在其中交互。例如，多线程应用程序可以在线程之间的虚拟机消息队列中抛出，以便在脚本级别进行序列化处理。

### 列表推导式

结合多种范式，Falcon 为程序员提供了各种不同的功能。暴露序列接口的基类提供了 `comp` 方法。`comp` 方法接收一个强制参数 `source`（可以是另一个序列、项目范围或生成器），以及一个过滤器和修改器。

问题（在通用项目中）可以作为第二个选项提供并作为过滤器修改器。关联对（例如字典）得到了很好的支持。以下是一个使用列表推导式的简单示例；结果是 2..10 的偶数数组。

```
even_array=[comp(2:11:2)]
```

这生成 1..9 范围内的随机列表；列表在随机数为 10 时终止（即每个项目有 1/10 的概率是最后一个）。

`comp` 方法返回它操作的同一个对象。因此，可以将它应用于任何扩展以为其添加更多数据。

同样，`mfcomp` 方法允许使用多个输入集创建推导，如下所示

```
sums=[mfcomp(x,y) -> x+y), [1,2], [3,4]]
```

"sums" 中的结果数组包含第一个集合 (x) 中的每个元素与第二个集合 (y) 中的每个元素获得的值。

### 模板文档

Falcon 允许文本文档的一部分，带有预处理器 `<?`。指令文件被视为文本文档，直到遇到其中一个处理过程为止简单结束。输入脚本按如下方式执行：

你可以通过 `<? args.len()>?1)?` 调用此脚本

FTD 文档与普通 Falcon 脚本配合使用-

# 74 - Falcon (编程语言)

...部分，演示逻辑位于动态模板（FTD 文件）中，而应用逻辑存储在 Falcon 模块中。

## 显式字符串扩展

Falcon 包含一个 `@` 一元字符串扩展，它会返回一个放置了内联 `$` 值引用的字符串。这种分配允许对子字符串进行匹配。

用于从任何 VFS（网络资源或压缩/zip 存档）加载模块或资源，这可能包括由第三方模块和/或通过嵌入引擎提供的特殊虚拟位置。

FTD 文档可以用于动态网站。某些 Web 服务器（Apache Apache [此处原文重复]）可以直接解析并执行 `.ftd` 脚本，使用一个解释引擎的 API。也可以通过 CGI 脚本使用动态 FTD 页面。

## 并发支持

在 0.8x 版本中，独立的 `Thread` 模块为脚本提供了完全的多线程支持；从 0.9x 版本开始，“Threading” 模块被集成到标准模块中，并直接在主引擎内部提供支持。多线程代理是面向方向的，数据访问必须通过多种可能的机制进行共享。每个虚拟模块都与其它的任何操作独立运行（类似于垃圾回收）。

## 异常

示例：

```
a = 1234567
v = "formatted"
s = "$a = ${v(a:2rg3,2)}"
print(s)
```



Falcon 通过`try`和`catch`语句支持错误处理。`raise`语句可以捕捉 Falcon 项，包括数字、字符串和对象。因此库函数和外部模块通常会捕捉`Error`类的实例，或派生于以下类的实例：

```
a = 1234567, formatted as
a123.79, returned as 0x1E241
```

- `a`的值、变量的值以及逗号字面量
- 来自该值的扩展字符串
- `a`的值，在 12 宽度内右对齐，每 3 个一组逗号，然后四舍五入到 2 位小数
- 大十六进制数值（舍入到最接近的整数），前缀`'0x'`。

`catch`语句可以捕获任何类型的项、特定类型（字符串或整数）或来自某个类。`catch`子句组织在层次结构的基础上，因此可以提供更通用的处理器，如下例所示（`TypeError`是派生自`Error`的类）：

```
try:
code that can raise ...
catch TypeError in error
if we use types
catch error in error
an another generic error ...
catch explicit raise "something" was issued...
catch in error
some other exception has been raised, in the variable error. end.
```

## 协程

Falcon 的设计目标是通过一个可链接的库`falcon`来嵌入和扩展其他系统。

Falcon 支持准协程，包括...。协程由虚拟机在时间片或空闲时间执行。它们提供了一种比全模型更轻量级的分层方法，并允许通过不同的协程看到全局数据。协程的执行是显式要求的，每个协程在阻塞之前必须检查数据的可用性。

## 文档生成器

Falcon 自带了一个集成的通信系统，该系统专门设计用于通过 Falcon 库、C++ 代码或用 Falcon 编写的模块集提供可维护的文档。

## 元拷贝

由任何或虚拟（脚本）级别处理的所有 I/O 操作都被委托给中央虚拟文件提供者（Central Virtual File Provider），外部模块或嵌入 Falcon 的设施允许其动态注册。

## 虚拟文件系统

编译器包含一个支持 Falcon 扩展的元编译器。标准驱动程序中的 Falcon 虚拟机使用该元编译器。从元编译器生成的输出对于语言词法器来说就像原始源代码的一部分。| 转义序列，可以通过打印程序来手动编写程序的内容：

`class catch`语句中的`class`部分是可选的（这意味着错误本身可能会被丢弃）。

```
! print(print("Hello world") \)
```

`catch`语句模仿了 `switch` 语句，可以用于切换变量的类型或类。

`marco`关键字提供了一个简化的糖果语法接口，用于编译时元编程。

## 原生国际化

以`'`为前缀的字符串被识别为（国际）字符串。

通过`directive`语句声明使用的语言，可以指示哪些字符串是用哪种语言编写的，如下例：

```
directive lang-fr // uses 5
characters language code
```

> Bonjour à toi le monde !

使用命令行工具将字符串导出到 XML 定义文件中，这些文件可以作为模板翻译成不同的语言。

翻译后的字符串在加载时应用到模块中。

## Feathers 标准库

Feathers 支持模块化编程，带有一个模块套件，它集成了基础 I/O 和语言集成的基础函数、类和对象。

Feathers 模块包括：

## Ferite

Ferite 是一种小型脚本语言，提供了直接的应用集成，以及易于扩展 API 能力。Ferite 的设计目标是创建一种简洁、跨平台、易于嵌入和扩展并支持未来标准的语言。

Ferite 的主要接口包括：Java 用于对象，C 和 PHP 用于函数，Scheme 用于闭包，Ruby 用于块调用，C++ 用于命名空间。Ferite 还具有松散类型机制和一组小型应用程序接口（APIs）。总体而言，Ferite 被视为一种大括号语言。

- 编译器 - 反射编译器和动态插件加载器。
- 配置解析器 - 完整的配置文件解析器。
- JSON - 数据与 JavaScript 表示法之间的可变转换
- Logging - 高性能日志设施。
- MXML - 快速简单的 XML 解析器（兼容 XML 1.0）。
- Process - 跨程序支持接口。
- 正则表达式 - PCRE
- Socket - 网络接口。
- Threading - 压缩

## 实现

Formula 引擎从头开始编写，为了 Notes 。

```
SELECT @NoteId="005D"
```

它是 Ray Oz 在 Notes 开发早期创建的。它借鉴了 Lisp 的使用。这种语言主要用于字符串和列表处理，而不是数学。

## Formula 语言

- @Functions 用于计算和简单逻辑
- @Commands 用于用户界面的操作
- @Functions 在 Notes 中多处使用。
- 用于选择给用户显示（某种索引）或选择进一步处理的文档。在这种情况下，公式会对每个项目求值为 (`'true'`) 或 `'false'`。
- 为字段提供默认值，转换用户输入的数据（如去除多余空格）并验证这些数据
- 从数据库或关系型数据库（使用 ODBC）获取值列表。这可以为用户提供一组可选值。

## 平台

Formula 可用于：

- Ubuntu
- Fedora
- Arch
- Mandela
- OpenSUSE
- Solaris
- Linux
- Windows
- Mac OS

## 友好交互式 Shell

友好交互式 Shell (fish) 是一个专注于交互性、可发现性和用户友好性的 Unix Shell。fish 的设计目标是为用户提供一组易于发现、记忆和使用的丰富且强大的功能。

fish 于 2005 年根据 GNU 公共许可证发布，fish 是自由软件。

### 亮点

fish 的特点是针对每个完成提供了用户友好强大的 Tab 键补全、带通配符的字符串补全，以及许多特定命令的补全。它提供了一个详尽且易于发现的帮助系统。特殊的帮助命令可以在浏览器中访问所有 fish 文档。

### 语法

fish 的语法与其他脚本语言略有不同。这些更改是为了让语言更强大，以至于语言小巧且易于学习。fish 与其他命令行解释器（如 `bash`）之间最明显的区别是，变量的内容不受分隔符限制，这意味着很少需要将变量括在引号中。

```fish
convert $ (basename $i).jpg;
end
# 分号的作用类似于 bash 中的冒号：
> in *.jpg; convert $ (basename $i).jpg;
end
# 但多行形式非常方便使用
# fish 支持多行历史记录和编辑
```

友好的交互式 - 第 77 页

fish: ${foo}

fish: 你是想说 ${VARIABLE}??

`'`字符的行为类似于括号，如果紧跟在`'$'`后面，则不允许作为变量名的一部分，且名称不能为空。要了解更多关于 fish 中变量扩展的信息，请输入`"expand-variable"`；

```fish
# 变量赋值，设置变量
# 将 'foo' 设置为
# 值 = "bar"。 Fish 是使用操作符的，
# 它对空格敏感。
此外，
# 命令可以轻松扩展到与
# 数组、作用域等工作。
set foo bar
echo foo
```

```fish
# while 循环，读取 /etc/passwd
# 并输出文件
# 这应该是
# 用户的描述
# cat /etc/passwd | read line
set char=$(echo $line | cut -c1)
echo $line
```

> > $(foo)

fish: 你是想说 (COMMAND)?

fish 中`'$'`字符仅用于访问变量。要了解更多关于 fish 中替换的信息，请输入`"help expand-command-substitution"`；

```fish
# 命令赋值，使用命令
# 输出
# 将 'pwd' 写入变量 'wd'。Fish
# 不使用 ""
# 因为它们不能嵌套，且看起来
# 太像 '()'
# 不要使用 ($)，它在 fish 中
# 仅用于变量
# 扩展。
echo $wd
```

fish 与其他 shell 的区别之一是不存在子类。许多任务（如管道、函数、循环）在其他 shell 中是通过调用的子 shell（subshells）实现的。而为 shell 运行命令并退出的简单子程序则不同。遗憾的是，在子 shell 中进行的更改对主 shell 没有任何影响，这意味着作为变量的许多函数无法按预期工作。Fish 从不分叉不同的 shell；所有功能都是完全的。

## 通用变量

Fish 有一种通用变量（universal variables），允许用户在多个运行的 fish shell 之间为变量重新赋值。变量在注销和重启后会被记住，并立即传播到所有 shell。

```fish
# 数组变量。'A' 变成一个
# 有 5 个值的数组：
set A 3 5 12 'B' 变成 'A' 的第一个
元素：
set B $A[1]
echo $B
5
```

```fish
# 这在其他 shell 中不起作用，
# 因为内置 'read' 将在其子 shell 中运行，
# 而 fish 不按预期工作。
# cat * test
```

```fish
# 这将设置默认
# 编辑器。'U' 告诉 fish
# 这是一个通用变量。
# 设置通用变量。
set -U EDITOR
```

```fish
# 这将使当前
# 工作目录成为 fish
# 提示符的一部分并在所有运行
# 实例中变为蓝色。
set -U fish_color_cwd blue
```

```fish
# 你可以索引所有错误甚至
# 命令替换输出
echo ${A(seq 3)}
357
# 删除 A' 的第一个和第五个元素
set -e $A[5]
echo $A
359
```

## 其他特性

### 错误消息

fish 中的错误消息设计用于告诉你出了什么问题以及可以如何处理。

- 高级标签补全。
- 具有广泛错误检查的语法高亮。
- 支持 X 剪贴板。
- 基于术语的智能终端处理。

```fish
> foobar
fish: 未知命令 "foobar"
你是想说 ${VARIABLE_VALUE}?
```

### 来源

有关设置变量取值的信息，请通过输入`"help"`查看 `set` 命令部分

(已编辑): `"http://wikipedia.org/wiki/Fish_interactive_shell"`

```fish
# for 循环，将 jpg 转换为 png
# set wd $(pwd)
for i in *.jpg
```

## GNU Guile

GNU Guile 是一个用于 Scheme 编程语言的解释器/虚拟机。它于 1993 年首次发布。Guile 包含了针对 POSIX 系统调用、API 功能等其他模块化的扩展，并以对象的形式打包。"胶水"允许该语言嵌入其他程序中，并作为允许紧密集成语言的接口。为了处理该环境中的延续（continuations），它必须将执行栈复制到堆中，然后再回来。因为外部代码可能指向 Scheme 对象，Guile 的垃圾回收器是"保守"型的，必须周期地接触所有内存。Guile 是 GNU Interactive Language 的缩写。Guile 分别支持 XML、XPath 和 XSLTs。基于 S 表达式的 XML 处理由 guile 提供。Guile 是 GNU 项目的"官方"扩展，截至 2006 年，它已用于几个主要项目。它的名字是由 Lee Thomas 在 Usenet 上命名的。这种设计的想法是让开发者用 C 或 C++ 实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合。

## 历史



# GNU Guile

GNU Guile 是一个用于 Scheme 编程语言的解释器/虚拟机。它于 1993 年首次发布。Guile 包含了针对 POSIX 系统调用、API 功能等其他模块化的扩展，并以对象的形式打包。“胶水”允许该语言嵌入其他程序中，并作为允许紧密集成语言的接口。为了处理该环境中的延续，它必须将执行栈复制到堆中，然后再回来。因为外部代码可能指向 Scheme 对象，Guile 的垃圾回收器是“保守”型的，必须周期地接触所有内存。Guile 是 GNU Interactive Language 的缩写。Guile 分别支持 XML、XPath 和 XSLTs。基于 S 表达式的 XML 处理由 guile 提供。Guile 是 GNU 项目的“官方”扩展，截至 2006 年，它已用于几个主要项目。它的名字是由 Lee Thomas 在 Usenet 上命名的。这种设计的想法是让开发者用 C 或 C++ 实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合。

## 历史

Guile 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。

```fish
# while 循环，读取 /etc/passwd
# 并输出文件
# 这应该是
# 用户的描述
# cat /etc/passwd | read line
set char=$(echo $line | cut -c1)
echo $line
```

> > $(foo)

fish: 你是想说 (COMMAND)?

fish 中 '$' 字符仅用于访问变量。要了解更多关于 fish 中替换的信息，请输入 "help expand-command-substitution"；

```fish
# 命令赋值，使用命令
# 输出
# 将 'pwd' 写入变量 'wd'。Fish
# 不使用 ""
# 因为它们不能嵌套，且看起来
# 太像 '()'
# 不要使用 ($)，它在 fish 中
# 仅用于变量
# 扩展。
echo $wd
```

fish 与其他 shell 的区别之一是不存在子类。许多任务（如管道、函数、循环）在其他 shell 中是通过调用的子 shell 实现。而为 shell 运行命令并退出的简单子程序不同。遗憾的是，在子 shell 中进行的更改对主 shell 没有任何影响，这意味着作为变量的许多函数无法按预期工作。Fish 从不分叉不同的 shell；所有功能都是完全的。

# 通用变量

Fish 有一种通用变量（universal variables），允许用户在多个运行的 fish shell 之间为变量重新赋值。变量在注销和重启后会被记住，并立即传播到所有 shell。

```fish
# 数组变量。'A' 变成一个
# 有 5 个值的数组：
set A 3 5 12 'B' 变成 'A' 的第一个
元素：
set B $A[1]
echo $B
5
```

```fish
# 这在其他 shell 中不起作用，
# 因为内置 'read' 将在其子 shell 中运行，
# 而 fish 不按预期工作。
# cat * test
```

```fish
# 这将设置默认
# 编辑器。'U' 告诉 fish
# 这是一个通用变量。
# 设置通用变量。
set -U EDITOR
```

```fish
# 这将使当前
# 工作目录成为 fish
# 提示符的一部分并在所有运行
# 实例中变为蓝色。
set -U fish_color_cwd blue
```

```fish
# 你可以索引所有错误甚至
# 命令替换输出
echo ${A(seq 3)}
357
# 删除 A' 的第一个和第五个元素
set -e $A[5]
echo $A
359
```

# 其他特性

错误消息

fish 中的错误消息设计用于告诉你出了什么问题以及可以如何处理。

- 高级标签补全。

- 具有广泛错误检查的语法高亮。

- 支持 X 剪贴板。

- 基于术语的智能终端处理。

```fish
> foobar
fish: 未知命令 "foobar"
你是想说 ${VARIABLE_VALUE}?
```

来源

有关设置变量取值的信息，请通过输入 "help" 查看 set 命令部分

(已编辑): "http://wikipedia.org/wiki/Fish_interactive_shell"

```fish
# for 循环，将 jpg 转换为 png
# set wd $(pwd)
for i in *.jpg
```

# GNU Guile

GNU Guile 是一个用于 Scheme 编程语言的解释器/虚拟机。它于 1993 年首次发布。Guile 包含了针对 POSIX 系统调用、API 功能等其他模块化的扩展，并以对象的形式打包。“胶水”允许该语言嵌入其他程序中，并作为允许紧密集成语言的接口。为了处理该环境中的延续，它必须将执行栈复制到堆中，然后再回来。因为外部代码可能指向 Scheme 对象，Guile 的垃圾回收器是“保守”型的，必须周期地接触所有内存。Guile 是 GNU Interactive Language 的缩写。Guile 分别支持 XML、XPath 和 XSLTs。基于 S 表达式的 XML 处理由 guile 提供。Guile 是 GNU 项目的“官方”扩展，截至 2006 年，它已用于几个主要项目。它的名字是由 Lee Thomas 在 Usenet 上命名的。这种设计的想法是让开发者用 C 或 C++ 实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合。

## 历史

Guile 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。注：`Guile` 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 `Scheme` 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，`Guile` 诞生了。

```fish
# while 循环，读取 /etc/passwd
# 并输出文件
# 这应该是
# 用户的描述
# cat /etc/passwd | read line
set char=$(echo $line | cut -c1)
echo $line
```

> > $(foo)

fish: 你是想说 (COMMAND)?

fish 中 '$' 字符仅用于访问变量。要了解更多关于 fish 中替换的信息，请输入 "help expand-command-substitution"；

```fish
# 命令赋值，使用命令
# 输出
# 将 'pwd' 写入变量 'wd'。Fish
# 不使用 ""
# 因为它们不能嵌套，且看起来
# 太像 '()'
# 不要使用 ($)，它在 fish 中
# 仅用于变量
# 扩展。
echo $wd
```

fish 与其他 shell 的区别之一是不存在子类。许多任务（如管道、函数、循环）在其他 shell 中是通过调用的子 shell 实现。而为 shell 运行命令并退出的简单子程序不同。遗憾的是，在子 shell 中进行的更改对主 shell 没有任何影响，这意味着作为变量的许多函数无法按预期工作。Fish 从不分叉不同的 shell；所有功能都是完全的。

# 通用变量

Fish 有一种通用变量（universal variables），允许用户在多个运行的 fish shell 之间为变量重新赋值。变量在注销和重启后会被记住，并立即传播到所有 shell。

```fish
# 数组变量。'A' 变成一个
# 有 5 个值的数组：
set A 3 5 12 'B' 变成 'A' 的第一个
元素：
set B $A[1]
echo $B
5
```

```fish
# 这在其他 shell 中不起作用，
# 因为内置 'read' 将在其子 shell 中运行，
# 而 fish 不按预期工作。
# cat * test
```

```fish
# 这将设置默认
# 编辑器。'U' 告诉 fish
# 这是一个通用变量。
# 设置通用变量。
set -U EDITOR
```

```fish
# 这将使当前
# 工作目录成为 fish
# 提示符的一部分并在所有运行
# 实例中变为蓝色。
set -U fish_color_cwd blue
```

```fish
# 你可以索引所有错误甚至
# 命令替换输出
echo ${A(seq 3)}
357
# 删除 A' 的第一个和第五个元素
set -e $A[5]
echo $A
359
```

# 其他特性

错误消息

fish 中的错误消息设计用于告诉你出了什么问题以及可以如何处理。

- 高级标签补全。

- 具有广泛错误检查的语法高亮。

- 支持 X 剪贴板。

- 基于术语的智能终端处理。

```fish
> foobar
fish: 未知命令 "foobar"
你是想说 ${VARIABLE_VALUE}?
```

来源

有关设置变量取值的信息，请通过输入 "help" 查看 set 命令部分

(已编辑): "http://wikipedia.org/wiki/Fish_interactive_shell"

```fish
# for 循环，将 jpg 转换为 png
# set wd $(pwd)
for i in *.jpg
```



GNU Guile 是一个用于 Scheme 编程语言的解释器/虚拟机。它于 1993 年首次发布。Guile 包含了针对 POSIX 系统调用、API 功能等其他模块化的扩展，并以对象的形式打包。“胶水”允许该语言嵌入其他程序中，并作为允许紧密集成语言的接口。为了处理该环境中的延续，它必须将执行栈复制到堆中，然后再回来。因为外部代码可能指向 Scheme 对象，Guile 的垃圾回收器是“保守”型的，必须周期地接触所有内存。Guile 是 GNU Interactive Language 的缩写。Guile 分别支持 XML、XPath 和 XSLTs。基于 S 表达式的 XML 处理由 `guile` 提供。Guile 是 GNU 项目的“官方”扩展，截至 2006 年，它已用于几个主要项目。它的名字是由 Lee Thomas 在 Usenet 上命名的。这种设计的想法是让开发者用 C 或 C++ 实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合。

# 历史

Guile 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 Scheme 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，Guile 诞生了。注：Guile 起于 Richard Stallman 的一次激烈讨论（“Tcl 战争”），他声称 Tcl 是用于应用程序脚本的；他提议将 Scheme 作为应用程序的首选语言并最终启动了该项目。由于缺乏一种在 C 或 C++ 中实现关键算法和数据结构，并为解释代码提供类型，将编译代码与解释执行的灵活性相结合的想法，Guile 诞生了。

# Blocks and iterators

Parameter-passing to be a closure:

```smalltalk
"remember a block.
remember := [:name | 'Hello, %1! % '
{ name } displayNI
```

When the time is right -- call closure!

return value: 'world'

--> = 'Hello, world!'

```smalltalk
(3 to 6): do: [:item | item display]
--> =3
--> =4
--> =5
--> =6
```

Returning closures from a method:

A method as `:inject:` can accept both a parameter and a block. it iterates each member of a list, performing some function while retaining an aggregate. This is analogous to the `foldi` function in functional programming languages. For example:

```fish
Integer extend
asClosure as
```

# GameMonkey 脚本

GameMonkey 是一种小型的跨平台语言，正如其名所示，专为嵌入游戏设计。GameMonkey 与 Lua 有相似之处，但语法上更接近 C 语言。

- 游戏特性：
- 跨平台机器库
- C 风格语法
- 极小的占用（约 50kb）
- 软实时交互式收集（无引用计数）
- 原生线程
- 状态的完整实现

GameMonkey 由 Matthew Rek 和 Greg Douglas 在 2002 年编写，最初是为 Auran 的闭源项目源码。然而，在 2003 年 6 月 12 日，授予了 GameMonkey 源代码以 MIT 许可协议公开发布。它目前被广泛应用于各种机器的商业和爱好应用中，包括 Windows、PC-Mac、Microsoft Xbox、Sony PlayStation 2、PlayStation 3、Nintendo GameCube、Nintendo DS、Nintendo Wii 以及各种 Linux 发行版。

来源（已编辑）：`http://wikipedia.org/wiki/GameMonkey_Script`

# Genshi（模板语言）

Genshi 是一种用 Python 编写的基于 XML 变量的模板。Genshi 用于轻松将通用输出插入到基于 HTML 的语言（普通 HTML）中，并将元素用于文档。Genshi 基于 Kid，旨在保持处理速度更快的同时实现其某些功能。

Genshi 可以与多个 Python 框架配合，例如 `Cython`、`TurboGenshi` 和 `web2py`。Genshi 在 `boboGears 2.x` Web 框架中替换了 `Kit`。Genshi 利用命名空间将结构嵌入到 HTML 中。

# Google Apps Script

Google Apps Script 是一种云端脚本语言，用于在 Google Apps 平台进行轻量级应用开发。它基于 Javascript，但不是运行在客户端，而是在 Google Cloud 中执行。Google Apps Script 基本上提供了简单的方法来自动化 Google 产品和第三方服务。

## 示例

以下代码演示了如何使用 Google Apps Script UI 服务和 DocList 以树形格式显示 Google Docs 集合的内容。

# 优势

注意其对类 Javascript 语法的使用，以及对 Google Web Toolkit 组件的使用。

- 基于类 Javascript 语法。更容易学习。
- 在底层，Google Apps Script 使用 Google Web Toolkit (GWT) 来创建和显示用户界面元素。GWT 很容易学习，并且完全从开发者手中将 AJAX/HTML 的复杂性抽象出来。

# 显示集合

# 局限性

- 目前 Google Apps Script 不允许连接到内部（防火墙后）企业级数据库。这是构建业务应用的关键。缺乏这一功能严重限制了脚本所能做的事情。在没有企业 LDAP 权限的情况下，无法构建简单的工作流应用。
- 没有方法共享脚本，即每次使用都会创建一个新实例。这在需要更新脚本时会产生开销，因为每个实例必须手动更新。
- Google Apps Script 中的 UI 组件不支持显示 HTML 脚本的输出。注意这里正在使用 Google Web Toolkit 的树形组件（`Tree widget`）。

# 82 - Google Apps Script

```javascript
function doGet(e) {
  var app = Ui.createApplication();
  var scrollPanel = app;
  createScrollPanel(); // Scroll Panel is a
  tree = app.createTree(); // Tree is a
  tree.addItem(app, "Enterprise"), scrollPanel);
  scrollPanel.setHeight("500");
  app.add(scrollPanel);
  return;
}
```

```javascript
function buildTree(searchTerm) {
  var tree = a.createTree(searchTerm); // Tree Web Widget
  tree.setSearch(searchTree);
}
```

```javascript
var image = a;
createImage(iconHTML);
fileLabel = a;
createAnchor(files[i].getName(), urlBase+files[i].getId());
filePanel = a;
createHorizontalPanel();
filePanel.add(fileLabel);
tree.addItem(fileLabel);
setState(true);
```

```javascript
// 使用 Google Apps Script Service 检索集合
var folders = List;
Folder(searchTerm).getFolders();
for (var i = 0; i < folders.length; i++) {
  tree.addItem(buildTree(a, folders[i].getName())).setState(true);
}
```

```javascript
var files = List;
Folder(searchTerm).getFiles();
for (var i = 0; i < files.length; i++) {
  if (files[i].getType() == "document") {
    urlBase = "https://docs.google.com/document/edit?id=";
    iconHTML = "https://docs.google.com/images/doclist_7_document.png";
  } else if (files[i].getType() == "spreadsheet") {
    urlBase = "https://docs.google.com/spreadsheets/ccc?key=";
    iconHTML = "https://docs.google.com/images/doclist_7_spreadsheet.png";
  } else if (files[i].getType() == "presentation") {
    urlBase = "https://docs.google.com/presentation/edit?id=";
    iconHTML = "https://docs.google.com/images/doclist_7_presentation.png";
  }
}
```

# Groovy（编程语言）

Groovy 是一种面向 Java 平台的面向对象的编程语言。它是一种动态语言，具有与 Python、Ruby 和 Smalltalk 相似的特征。它可以与 Python、Ruby 和 Smalltalk 的功能交互。Groovy 可以编译为 Java 字节码。Groovy 甚至可以与 Java 库直接交互。Groovy 允许静态和动态类型（使用 `def` 关键字）、运算符重载、对（列表和映射）的原生支持，以及对各种标记语言（如 XML 和 HTML）的原生支持（通过内联 DSL 实现）。Groovy 允许在处理异构数据时使用统一且简洁的语法。

Groovy 允许在 Java 运行时生成动态方法。Groovy 允许在 Java 运行时生成代码。Groovy 允许作为 Java 运行的扩展。Groovy 允许在 Java 运行时进行链式调用。Groovy 允许使用安全导航运算符（`?.`）来处理 null 值。Groovy 允许在与 Java 交互时进行类型转换。Groovy 允许在 Java 运行时进行动态调用。Groovy 允许在 Java 运行时使用闭包表达式。Groovy 允许在 Java 运行时处理闭包。Groovy 允许在 Java 运行时进行反射式操作。Groovy 允许在 Java 运行时使用生成式方法。Groovy 允许在 Java 运行时生成 getter 和 setter。Groovy 允许在 Java 运行时使用属性。Groovy 允许在 Java 运行时处理可选参数。Groovy 允许在 Java 运行时使用元编程。Groovy 允许在 Java 运行时处理字符串扩展。Groovy 允许在 Java 运行时进行字符串插值。Groovy 允许在 Java 运行时处理注解。Groovy 允许在 Java 运行时使用装饰器。Groovy 允许在 Java 运行时处理多态。Groovy 允许在 Java 运行时进行并发处理。Groovy 允许在 Java 运行时使用线程池。Groovy 允许在 Java 运行时处理异步任务。Groovy 允许在 Java 运行时使用响应式。Groovy 允许在 Java 运行时处理序列化。Groovy 允许在 Java 运行时使用持久化框架。Groovy 允许在 Java 运行时处理数据库连接。Groovy 允许在 Java 运行时使用 JSON 解析。Groovy 允许在 Java 运行时处理 XML 序列反序列化。Groovy 允许在 Java 运行时处理 YAML 配置。Groovy 允许在 Java 运行时使用 REST API。Groovy 允许在 Java 运行时处理 Web 服务。Groovy 允许在 Java 运行时使用容器框架。Groovy 允许在 Java 运行时处理单元测试。Groovy 允许在 Java 运行时处理集成测试。Groovy 允许在 Java 运行时使用 Mock 对象。Groovy 允许在 Java 运行时处理代码分析。Groovy 允许在 Java 运行时使用性能分析工具。Groovy 允许在 Java 运行时处理日志记录。Groovy 允许在 Java 运行时使用指标收集。Groovy 允许在 Java 运行时处理告警系统。Groovy 允许在 Java 运行时使用持续集成工具。Groovy 允许在 Java 运行时处理自动化部署。Groovy 允许在 Java 运行时使用容器化技术。Groovy 允许在 Java 运行时处理微服务架构。Groovy 允许在 Java 运行时使用服务网格。Groovy 允许在 Java 运行时处理云原生开发。Groovy 允许在 Java 运行时使用服务器计算。Groovy 允许在 Java 运行时处理无服务器架构。Groovy 允许在 Java 运行时处理安全加固。Groovy 允许在 Java 运行时使用加密解密算法。Groovy 允许在 Java 运行时处理身份验证。Groovy 允许在 Java 运行时使用授权令牌。Groovy 允许在 Java 运行时处理数据隐私保护。Groovy 允许在 Java 运行时处理合规性检查。Groovy 允许在 Java 运行时使用代码规范检查。Groovy 允许在 Java 运行时处理架构评审。Groovy 允许在 Java 运行时使用设计模式实现。Groovy 允许在 Java 运行时处理重构策略。Groovy 允许在 Java 运行时使用领域驱动设计。Groovy 允许在 Java 运行时处理反应式编程。Groovy 允许在 Java 运行时使用事件驱动架构。Groovy 允许在 Java 运行时处理消息队列系统。Groovy 允许在 Java 运行时使用 CQRS 模型。Groovy 允许在 Java 运行时处理事件溯源。Groovy 允许在 Java 运行时使用领域模式。

```java
class GroovyBean {
  String color
}

def myovyBean = new GroovyBean()
myovyBean.setColor("baby blue")
myovyBean.color="baby blue"
myovyBean.color='pebutter'
myovyBean.getColor()='pebutter'
```

Groovy 1.0 在 2007 年 1 月发布。它提供了 Java 语法。

```java
for (String it : new String[]{"Rod", "Carlos", "Chris"}) if (it.length() <= 4) {println(it);}
```

Groovy 1.1 在 2007 年 12 月 7 日发布，吸收了许多变化。

```groovy
["Rod", "Carlos", "Chris"].findAll{it.size() <= 4}{println(it)}
```

许多开发环境支持 Groovy：

- Eclipse，通过 Groovy-Eclipse
- IntelliJ IDEA，通过 Groovy 插件
- NetBeans，自 6.5 版本起
- TextMate
- JDeveloper，配合 Oracle ADF 使用
- Appxworks，一个处于测试阶段的云端 IDE，旨在将市场持续到 2011 年初

Groovy 中 Java 不具备的功能包括静态和动态类型（使用 `def` 关键字）、运算符重载、对（列表和映射）的原生支持。

# PHP 版 HipHop

HipHop for PHP 是一种源代码转换器，HipHop 程序能够以编程方式将 PHP 源代码转换为高度优化的 C++ 代码，并使用 g++ 将其编译为原生代码。HipHop 是 PHP 运行时系统的重新实现，并对许多 PHP 扩展进行了重写，以利用这些性能优化。

HipHop 由 Facebook 创建，旨在节省服务器资源。它以包含超过 300,000 行 C++ 源码的形式分发，并根据 PHP License 3.0 版本的条款作为免费软件分发。

他们还开发了 HipPHP，这是一种实验性的开发者工具，在运行前无需编译 PHP 源代码。

## 历史



最初，HipHop 在 Facebook 由赵海平（Haiping Zhao）的领导下在 CentOS 和 Fedora 系统上开发。它遵循了早期的发展，如将`hip`转换为`C`，以及 PHP 源代码的`Hip`和`Phalanger`（PHP 编译器）。由于技术困难，Facebook 未能按时交付，但 2 月 20 日，源码最终被上传到了公共 Git 仓库。

## PHP 版 HipHop

`HipHop`是一个开源项目，可以在 GitHub 上通过开放的 PHP License 获取。

`HipHop`目前支持 PHP 5.2 版本，并将更新以支持 5.3 版本。

`HipHop`在 CentOS 和 Fedora 上开发；目前在其他操作系统上构建可能无法运行，尽管未来可能会添加支持。`HipHop`只能运行在 64 位架构上。

`HipHop`是运行 PHP 项目的一项重大改进，它减少了内存占用，通过为`HipHop`添加`start`提供了更显著的加速，并大幅减少了内存消耗。

来源（已编辑）：`http://en.wikipedia.org/wiki/HipHop_for_PHP`

## HyperTalk

`HyperTalk`是一种高级过程化编程语言，由 Dan Winkler 在 1987 年创建，并与 Bill Atkinson 与 Apple 的 HyperCard 媒体共同开发。`HyperTalk`的主要目标受众是初学者；`HyperTalk`程序员通常是作者，编写程序的过程被称为“脚本（scripting）”。`HyperTalk`脚本类似于书面英语，并使用了与 Pascal 语言类似的逻辑。

这种不区分大小写的语言最初是解释执行的，但被 HyperCard 2.x 进行了“虚拟编译”。它支持过程化语言的基本控制结构：`repeat` with、`if/then/else`，以及作为函数和子程序的`as`、消息处理器 `handler`（这是一个过程）。数据类型在不同语言之间的边界以及数字是透明的。该语言中没有类或数据结构；取而代之的是特殊的字符串标识符，或者说是由逗号定义的项目“items”（在后续版本中，“itemDelimiter” 属性允许任意选择）。

### 面对象 HyperTalk

`HyperTalk`并不是严格的过程化语言。在 HyperCard 文件（所谓对象）中编写的脚本和`HyperTalk`允许以多种方式否定属性，并使用 `"send"` 命令更改其属性。例如，对象使用接近自然语言的语法进行访问，其中对象相对于当前卡片，或者使用操作符发送 `"mouseUp to card button 'OK' of 'Veracity'（鼠标释放到 Veracity 卡片的 OK 按钮）”`。由于按钮和字段也可以存在于背景层，但它们在不同卡片之间有所不同，因此存在字段（fields）和背景字段（background fields）。可以通过对象的名称或不随对象界面改变的唯一数字来访问对象。遍历对象（在 HyperCard 2.2 中统称为`parts`）时，在查询卡片数量时直接使用它们的数字。

`HyperTalk`还通过对内置工具提供完整的脚本控制，只需对绘图工具中所需的更改进行脚本编写，并移动鼠标从`drag`到`start`以及点击在点命令即可。

`HyperTalk`还会发送消息（事件）来发送处理器用户交互。当按钮被点击时，会发送`mouseDown`消息，当用户释放鼠标时会发送`mouseUp`以触发其动作。同样，它具有周期性的`idle`消息、`mouseEvent`、`Complete...`，并允许与 HyperCard 栈中不同卡片之间导航相关的消息，以及用户输入（`keyDown`、`functionKey`）和系统事件。至于脚本，并没有像其他过程化编程语言那样的事件循环。

`Complete!`允许在 HyperCard 上运行 `XCMDs` 和 `XCFNs`，甚至还包含一个微小的 HyperTalk 解释器。

该语言显然与 HyperTalk 相似。这些克隆版本和方言（统称为 XTalk）为该语言增加了现代编程语言所要求的各种功能，如定义对象属性、定时器、多线程和用户定义对象。

### 扩展 HyperTalk

尽管 HyperTalk 语言就像 HyperCard 本身，但它通过其名为外部命令（`XCMDs`）和外部函数（`XCFNs`）的插件系统获得了第二次生命，这些是附加到 MacOS 特有对象上的原生构造函数，具有单一入口和返回值。`XCMDs`和`XCFNs`也可以像 HyperTalk 栈中的普通消息和函数一样工作，并向 HyperCard 应用发送消息。一些新兴的 `XCMDs` 为语言增加了高级功能，如全支持（ColorizHC, HyperTint, AddColor）、多个特定窗口（Prompt, Taxtoid, Textlist, ShowDialog, MegaWindows）、支持拖放以及各种硬件接口。

- `MetaTalk` - Oracle Media Objects 的语言，它是 Pluto 的后代，第一个跨平台的 HyperCard 克隆版本。此外，这是唯一真正重要的。
- `Spinacker Plus` 的 `PlusTalk` (?)（由德国 Format 开发），作为 OMO 的基础。
- `SenseTalk` - Next 原生 HyperSense 和基于 VNC 的测试工具各自的语言。`SuperTalk` - SuperCard 的语言，它是由 Bill Appleton 开发的第一个 HyperCard 克隆，他还编写了 World Builder 冒险构建。
- `revTalk` - 实现在源自原始 HyperCard 的开发环境中的语言，现在运行在 Mac 上。

## Iptscase 中的 Fizz 示例

```lisp
if (STRL == 0) {
    a++
}

if (n % 3 == 0) {
    b = "fizz"
} else if (a % 5 == 0) {
    b = "buzz"
}
LOGMSG = itoa(b)
LOGMSG
```

```lisp
while {a <= 100}
```

## 相关链接

官方 Iptscrae 语言指南

来源: (编辑): `"http://en.wikipedia.org/wiki/IPTSCRAE"`

## Incr Tcl

```tcl
..or, as one-direct input:
//"s={n++{" "n itoea"} { "buzz" n
```

`Incr Tcl`（名称是 "Tcl+" 的一部分，通常缩写为 "Itcl"）是 Tcl 编程语言的一组面向对象的扩展。它被社区广泛使用，通常被认为具有工业强度。Itcl 的实现既有可以被 Tcl 应用程序动态加载的包，也有作为带有带有独立解释器的独立语言存在。

```tcl
method test [nslice] {

    if (scrum > 50) {

        error "FIRE! FIRE!"

    }

    set crumbs [expr scrum]

}

method clean {

    set crumbs 0

}
```

## C 代码集成

Itcl（类似于 Tk）拥有了将 C 集成到 Itcl 类中的内置支持。

## 许可协议

Itcl 遵循与 Tcl/Tk 相同的版权限制。只要保持版权声明完整，你就可以无需任何书面协议或版税使用、复制、修改和重新分发此软件。你可以声称拥有该软件；作者及其利益保留所有权，具体如标准发行版包含的 "license.terms" 文件所示。更多信息请参见 `itcl.sourceforge.net/tcl/itcl.html`。

# 概述

## 特性

### 命名空间支持

Itcl 命名空间用于组织命令和变量。示例：

```tcl
itcl:class SmartToaster {

    Inherit Toast

    method test [nslice] {

        if (scrum > 40) {

            clean

        }

        return [chan [nslice]]

    }

}
```

```tcl
itcl:class Toaster {

    variables 0

}
```

```tcl
set Toaster [SmartToaster #]

Toaster 2
```

## 增量编译器

“增量编译器”一词可能指两种不同类型的编译器：

重新编译源文件，其中大部分代码保持不变。对于增量编译器来说，对源代码进行微小更改后编译程序几乎是瞬时完成的。增量编译器可以在保持语言语义的同时，减少传统编译的粒度，编译器会附加并替换较小的部分。许多编程工具利用增量编译器为开发者提供更具交互性的编程环境。增量- 并不罕见。

## 定义

### 命令式编程

在命令式编程和软件开发中，增量编译器是在每次源文件发生变化时被调用的，开发者可以最直接地获知代码更改引起的错误。这种方案与传统编译相比，程序员的开发效率显著提高，因为他们不再需要等待漫长的过程才能发现错误。

这种类型的增量编译器的缺点是它无法轻松优化所编译的代码，由于局部性和更改代码的有限范围并不是问题，因为优化通常在发布阶段进行，增量编译器将在整个过程中使用，而标准批处理编译器将在发布时使用。

删除正在运行的代码被称为热交换。某些交互式编程平台将解释代码和编译代码混合，以实现代码的任何更改都能被程序立即访问的幻觉。

### 交互式编程

在交互式编程范式中（例如 Prolog 文献中），增量编译器是指源语言运行时系统的一部分编译器。编译器可以在程序管理的某些源代码或数据结构处被调用，生成一个新的包含机器码的编译程序，该代码供运行时系统立即使用。新编译的脚本允许过程被垃圾回收。这种方案允许某种程度的自修改代码，并需要元编程语言特性。添加、删除和-

## 增量编译器列表

用于命令式语言编译的增量编译器：

- `Poplog`（其核心语言 POP-11 及其前身 POP-2）
- 某些版本的 Lisp：
    - `Steel Bank Common Lisp`
    - 卡内基·梅隆大学 `Common Lisp`
    - `Science Common Lisp`
    - `GNU CLISP`
    - `Franz Allegro Common Lisp`
- 某些版本的 Scheme：
    - `Ikarus`
- `GNU` 编译器集合分出了 `IncrementalProject`，专注于 C/C++ 并带有一个快速的增量编译器
- `Eclipse` 平台作为 `Java Tools` 项目的一部分拥有 Java 编译器
- `IBM VisualAge C++` 编译器 4.0 是一个增量编译器，它将

## 88 - 集成脚本环境

### 集成脚本环境

集成脚本环境 (ISE) 是一种提供脚本开发设施的软件应用程序，通常包括：

- 脚本编辑器
- 语法高亮
- 集成式帮助
- 调试器
- 脚本启动器
- 标签补全

## 哲学

## 状态

`Loke` 是一种针对虚拟机的动态、强类型、基于原型的语言。它于 2008 年 11 月 6 日首次宣布

## JASS

`JASS`或`JASS2`（有时被称为 Just Another Scripting Language，即另一种脚本语言）是暴雪娱乐《魔兽争霸》游戏及扩展包冰封之战中使用的事件驱动脚本语言。地图作者可以在世界编辑器中使用为自定义地图创建触发器和 AI（人工智能）。

该语言提供了丰富的 API，让程序员控制游戏世界的各个方面。例如，它可以使用简单的 GUI 函数来改变天气和时间、向玩家显示文本并操纵地形。`JASS`还能创建强大的函数，如表格，如果鼠标移动或击中某个位置，`GetLocalPlayer()` 使用不当会导致断开连接。

## 基础语法

以下函数创建一个包含 "Hello, World!" 的字符串并将其显示给所有人。

`JASS`的语法类似于 Turing。它是上下文无关的。基础语法的示例所示：

```jass
function JASS_test

takes nothing returns nothing

    local integer i=0

    call DisplayTextPlayer(0,0,"Hello, World!")

endfunction
```

```jass
function syntax_Sum takes

integer
```

```jass
//名称、参数（如果有）和返回类型（如果有）
```

```jass
//它返回 语句以 "return" 开始

endfunction // 关键字

结束一个块
```

```jass
function JASS_test

takes p r returns nothing

    local integer i=0

    call DisplayTextPlayer(p,0,,"Hello, World!")

endfunction
```

```jass
//在声明时初始化

//分离的语句必须

分行
```

`JASS`主要使用过程化编程概念，暴雪世界编辑器的流行用户模式为 `JASS`语法增加了类似于 C++ 的面向对象编程特性。

# 90 - JASS

```jass
set i = 6 // 关键字 "set" 用于来

// 重新绑定变量

call syntax_Sum(i, r)

// 函数调用通过

// 关键字 "call" 触发

set r = syntax_Example_Sum(i, r)

// 当访问函数返回值时会省略

// "call" 关键字

function 释放系统资源

endfunction

function garbage_Collection_Example2 takes stringPath, real x, y returns nothing

    local specialEffect = SpecialEffect(Effect, x, y)

    local unit u = CreateUnit('hfoo', x, y) // 创建单位'hfoo' 在 x, y

    local destructible d = CreateDestructible('ATtr', x, y) // 创建可破坏物体'ATtr' 在 x, y

    set w = y // 可接受的

    call Trig_Handle_Example_Child(w, d) // 可接受的

endfunction
```

## Types

`JASS`是静态类型语言，其类型可以分为两类：原生类型（natives）和句柄（handles）。原生类型包括：

- `integer`（整数，32位）
- `real`（32位浮点数，类似于 Java 中的 `float`）
- `string`（字符串，限制为 1023 个字符串，为了提供保存/加载兼容性，要求仅使用 1013 个标签）
- `boolean`（布尔值）

所有类型都被视为非原生类型。原生类型的行为与编程语言中的类型相似。句柄通常返回一个带有单位、玩家、特殊特效等的“对象”。与 Java 的 Traits（接口/特性）类似，`JASS`中的所有变量和参数都被视为句柄，但在值返回时，这些对象并不是指向句柄的引用。在处理垃圾回收句柄时，对象变得非常重要。如果清理得当，变量在离开作用域时最好是句柄的引用。如果它们没有被正确置空，句柄将不会被回收并导致泄漏。此外，对它们的任何引用都会使用一些内存空间。如果不置空，用户会体验到性能下降，尽管规模要小得多。

```jass
set specialEffect // null 置空设置

// 值不为空，这只是句柄的引用；

// 句柄仍然存在

function
```

## Type casting

在原始类型中，语言正式支持 `real`、`real` 和 `integer` 之间的类型转换。`JASS`支持显式转换和隐式转换。

隐式转换仅发生从 `real` 到 `integer`。例如：

```jass
function type_cast_Example takes returns nothing

    local i = 4

    local real r = 5 // 5 的隐式转换以满足变量类型

    call DestroyEffect(special) // 我们销毁（清理）句柄以释放内存

    set specialEffect = null

endfunction

if (i < r) // i 到 real 的隐式转换

    set r = r // i 到 real 的隐式转换以执行返回

endif
```

```jass
function garbage_Collection_Example4 takes stringEffect, real x, y returns nothing

    // 执行

    call DestroyEffect(e) // 参数不需要置空

endfunction
```

句柄的另一个值得注意的属性是，所有句柄都被处理为像是 "handle" 类型中的一种。这些句柄类型中的可能会引用其自身的特殊类型或其他类型。例如：

`JASS`库提供了几种用于类型转换的方法：
- `L12R()`: 转换为 `real`
- `R2I()`: 转换为 `integer`
- `L12S()`: 转换为 `string`
- `R2S()`: 转换为 `real`
- `S2I()`: 转换为 `string`

句柄类型到类型转换的重要属性是，由于所有句柄变量都是引用，因此可以被处理（并）返回为整数。每个句柄的实例都被分配了一个唯一的值，该值本质上充当句柄的标识符。此外，虽然 `JASS`技术上不支持向句柄的转换，但在实践中是可能的，因为句柄可以隐式转换为整数，并且如果代码是我们可以

```jass
function Trig_Handle_Example_Child takes w, d widget w returns nothing

    // 执行

endfunction

function handle_Example takes real x, y returns nothing

    local widget // widget 是一个句柄类型，在可破坏物体方式上具有 unit 类型，例如：
```



`returns` `handle`

`endfunction`

`function H2I takes h returns handle`

`return h`

`set numbers[i] = i / variables` // 在值中指定索引时，`variables` 替代了常量

`endfunction`

`function H2I_array takes h returns handle`

`set units(numbers[i]) = null` // 数组

如果我们到达了行 `"return hwt"`，如果实际上调用了整数并返回了该值。暴雪意图让 JASS 使用这一点，当 JASS 编译器将抛出一个错误，警告函数没有返回正确的类型。

`call ReturnHandle(h)` // 这将最后一个返回的值设置为 `'h'`。

`set boolean[i-1] = false` // 算术（或函数）操作也是可以接受的

`return h` // 如果这从未发生，那么游戏将使用返回的值。

`set i = i + 1` // 像在这个索引整数中一样增加值。

`endloop`

// 如果我们以不同的类型返回返回的值，就像在这个索引整数中。

`if (boolean = true)` // 要访问数组成员，语法与变量相同，除非加上索引值

然而，程序员们发现并利用了 JASS 编译器语法中的一个著名的 Bug：所谓的“return bug”。本质上，编译器只会确保函数中的最后语句返回正确的类型。以下代码可以用于处理整数：

`set numbers = -200` // 你可以重新分配数组成员

`endif`

## Arrays

JASS 支持任何类型的一维数组。下面代码中是声明和访问数组成员的语法：

一个限制是，所有句柄都被处理为像是 `"handle"` 类型中的一种。这些句柄类型中的可能会引用其自身的特殊类型或其他类型。例如：

（此处原文内容不完整，未翻译对应部分）

## JRuby

JRuby 设计用于作为 JRuby 的混合模式虚拟机运行，其中代码可以被直接解释为 Java 字节码、在运行时进行即时编译（JIT），或在执行前进行离线编译转为字节码。在 2007 年 10 月之前，只有解释模式支持所有 Ruby 构造；从 1.1 版本开始，提供了全功能/JIT 编译器。该编译器允许解释代码和编译代码并排运行，并支持去优化和在运行时生成与 Java 一样快的字节码。

`base`，以一种非常原始的方式实现。动态调用在 1.1.5 版本中发布，在具有动态调用能力的 JVM 上被禁用。

JRuby 通过调用 `require java` 实现支持。以下示例创建了一个带有标签（Label）的 JFrame：

```ruby
require 'java'

frame = javax.swing.JFrame.new()
frame.getContentPane().add(label)
label.setText("Hello, World!")
frame.setDefaultCloseOperation(javax.swing.JFrame.EXIT_ON_CLOSE)
frame.pack()
frame.setVisible(true)
```

JRuby 核心子系统的重构

## 版本历史

此表展示了 JRuby 历史上的重大转变，适用于为了修复 Bug 和改进性能的版本。性能改进也没有显示在表中，因为每个版本通常都有某些改进。

该项目由 `codehaus.org` 委托管理，你可以找到官方发布历史的仓库计划。2011 年 3 月，JRuby 开发者 Thomas Enebo 表示，该小组仍处于 1.7 和 1.1 版本的规划阶段，并预计在这些版本之前会有 6.6 及后续版本。目前正在规划的功能包括：

JRuby 还允许用户使用类 Ruby 的方法命名调用代码，并将 JavaBean 属性引用为属性：

- JRuby API，包括并发 API 和集合 API
- 一种新的表示格式，允许在 JVM 之外的 Ruby 级别提供更多选项
- 模块化，允许根据配置方案（profile）包含或排除多种代码类型和扩展，允许开发者构建 JRuby 范围的子集
- 包解耦，允许在生成的 JAR 文件中包含或排除组件

```ruby
frame.content.add_label
frame.visible = true
```

## 从 Java 调用

JRuby 由 Engine 提供商业支持。它使用原生代码。它允许使用 Ruby 语法访问庞大的 Java 库生态系统。JClassFusion 可用于企业级规模的 Ruby 应用。

JRuby 同样很容易从 Java 调用，使用 Java 6 的 JSR 233 集合或 Apache Spring 框架。关于此的更多信息可用 JRuby wiki。

## 框架支持

```java
// 使用 Java 6 的 JSR 233 集合
ScriptEngineManager manager = new ScriptEngineManager()
ScriptEngine engine = manager.getEngineByName("ruby")
rb.eval("Hello, World!");
} catch (Exception ex) {
    ex.printStackTrace();
}
```

JRuby 内置支持 Rails、RSpec 和 Ruby-Gems。它提供了一个 FFI 系统来将 C 库作为包使用。它还允许 C 原生扩展。像 Ruby MRI 一样提供交互式 Ruby 壳（`irb`）。

NetBeans Pack 自 Beans 6.0 起可用，允许使用 Ruby 和 JRuby 进行 IDE 开发，以及在这两种实现中使用 Ruby on Rails。

## 编程

JRuby 本质上是用 Java 编写的 Ruby 解释器。JRuby 具有许多相同的概念、面向对象编程和[动态类型系统]。关键在于它与 Java 紧密集成，并可以从 Java 程序直接调用。JRuby 在 Web 应用开发方面具有显著特性。

自 2006 年以来，JRuby 核心团队将 JRuby 从一个简单的 C 移植版转变为支持更好的性能并辅助编译为 Java 字节码。这为团队设定了一个雄心勃勃的目标：在未经过修改的 JRuby 上运行 Ruby。实现这一目标的过程，JRuby 套件扩展展示了团队对 JRuby 的“一致性”赢得了信心。至于 2006 年的奖以及 2007 年初，他们获得了更多复杂的重新设计和

## 性能

JRuby 支持解释模式和 JIT 模式（后两者自 1.1 版本起可用）。JRuby 经历了多次演进，变得比参考实现更快。2009 年 12 月 16 日的基准测试显示，JRuby 使用的内存是 Ruby MRI 的 2 到 5 倍。

## JRuby 调用 Java

JRuby 的强大功能之一是它能够调用 Java 平台的类。要做到这一点，必须首先

## 解释模式

在这种模式下，JRuby 1.0 比 C Ruby 慢。例如（包括启动时间）。在标准解释模式下提供 Rails 请求时，JRuby 比 C Ruby 1.8 慢 50% 到 70%。比虚拟机（已实例化）慢。

`Jscript` 被实现为解释模式，是为了它的速度。JRuby 在性能方面，J J 是基准测试显示，与其它实现相比，JRuby 更快，添加了循环。一致地比 C Ruby 1.8 快 200% 到 300%。标记，正如注释所。。

## 即时编译模式

JIT 模式自 JRuby 1.1 起可用。1.6 及以上版本。保持 Java 虚拟机在机器码速度上比 C Ruby 1.8 慢 15%-20%。然而，JRuby 的加载速度也慢 4 倍，但超出了。使用 Ruby 1.9，JRuby 是某些的。

## Jscript

Jscript 是一种基于 ECMAScript 标准的脚本语言，用于 HTML 页面。Jscript 被实现为解释模式，是为了它的速度。JRuby 在性能方面，J J 是基准测试显示，与其它实现相比，JRuby 更快，添加了循环。一致地比 C Ruby 1.8 快 200% 到 300%。标记，正如注释所。

## Jscript .NET

Jscript .NET 为 ECMAScript 增加了几项新功能，但缺少原始 JavaScript 的许多功能。它是 ECMAScript 第 3 版，作为静态类型注解，已不再活跃开发。

## 与 JavaScript 的区别

正如 Jscript 所解释，某些版本的 Jscript 是 UI 编程语言，用于处理商标是-cript 没有 s，因此它们的实现-ter 7.0 也引入了你的不同名称，ter 6.0 带有 Windows XP

## 版本

Jscript 是一种基于 ECMAScript 标准的脚本语言，用于 HTML 页面。Jscript 被实现为解释模式，是为了它的速度。JRuby 在性能方面，J J 是基准测试显示，与其它实现相比，JRuby 更快，添加了循环。一致地比 C Ruby 1.8 快 200% 到 300%。标记，正如注释所。

（来源：每个框架框架的 Mi-cript.NET 文件版本）

## JavaScript

JavaScript 是由 Sun Systems 设计的一种脚本语言，是 Java 平台 JavaFX 技术家族的一部分。

```java
height: 80

scene: Scene {
    content: Text {
        font: Font {size : 24, text: "Hello World
        x: 10, y: 30
        content: "Hello World"
    }
}
```

JavaFX 目标是互联网应用领域（与 Adobe Flex 和 Microsoft Silverlight 竞争），专用于为桌面和移动市场快速开发高可扩展的应用程序。JavaScript 与 NetBeans 和 Eclipse 等集成开发环境配合工作。

JavaScript 是一种用于 Java 平台的编译型、静态类型、声明式脚本语言。它提供了自动数据绑定、变异触发器和声明式动画，并使用了一种表达式语言（所有代码块都产生值）。等一下，查看文本：“JavaScript 是一种用于 Java 平台的编译型、静态类型、声明式脚本语言。它提供了自动数据绑定、变异触发器和声明式动画，并使用了一种表达式语言（所有代码块都产生值）。”

通过其标准的 Java API，它支持现代矢量图形、视频播放和 Swing 组件。

自其赞助的 OpenFX 项目以来，它根据 GNU 通用公共许可证发布。

尽管 JavaFX 起初是一种解释型语言，但在首次发布（2008 年第三季度）之前，JavaScript 转向了重新编译。JavaScript 仍然可以通过 JSR 223“Java 脚本”桥接进行使用。它构建在 Java 平台之上；在 JavaFX 代码中类类非常类。

它显示以下窗口/帧：

![](img/28b49089ea8cf20e1b8f2972fae5fffa_96_0.png)

## 历史

JavaScript 曾作为 JavaFX 用于表单填充。JavaFX 由 Charles Cole 开发，他通过 2005 年 9 月通过收购 See-Beyond Technology Corporation 成为 Sun 的员工。

它的名称更改为 JavaScript，并在 Java 2007 年成为开源。

可以通过这种方式创建此程序：

所有代码、文档和演示均在 OpenFX 开发网站上展示。JavaScript 1.0 大约于 2004 年 12 月发布。

```java
import javafx.ext.swing.*;

var myFrame=Stage();
var myLabel=new Label("Hello World");
myLabel.setText("Hello World");
myFrame.width=50;
myFrame.visible=true;
myFrame.content=myLabel;
```

2010 年 9 月，Oracle 在 JavaOne 上宣布 JavaFX API 将停止支持，尽管它将适用于 Java 虚拟机的其他语言。

# 语法

2010 年 9 月 27 日，Stephen Chen 宣布了一种基于增强型 JavaFX 的声明式接口语言。

JavaScript 用于构建用户界面的声明式语言与更冗长的方法调用形成鲜明对比，后者可以在 Swing 中构建等效界面。

这里有一个 JavaScript 的本地示例：

## 前提条件

```java
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.text.Text;
import javafx.scene.text.Font;

Stage {
```

> title: "Hello World"

需要 SE 5 或 SE 6 来支持 JavaFX 开发。开发者可以通过整合插件使用 Eclipse 或 NetBeans IDE 来处理 JavaFX。

```
width: 250
```

源自（编辑）："http://en.wikipedia.org/wiki/JavaFX"

## JavaScript

JavaScript 也称为 ECMAScript，是一种基于原型的面向对象的脚本语言，具有动态性、弱类型和一等函数特性。它也被认为是一种类似于 Scheme 和 OCaml 的函数式编程语言，因为它支持高阶函数。

JavaScript 是 ECMAScript 标准的实现，主要作为客户端 JavaScript 用于浏览器，以增强用户界面和动态网站。这允许以编程方式访问宿主环境中的计算对象。

JavaScript 今日在应用程序中的应用——例如在 PDF 文档、特定站点浏览器和桌面小部件中——也非常重要。更现代、更快的 JavaScript 虚拟机不断涌现，Node.js 也增加了 JavaScript 在服务器 Web 应用中的普及。

JavaScript 使用受 C 影响的语法。JavaScript 复制了 Java 的名称和命名规范，但这两种语言毫无关系，语义也非常不同。JavaScript 内部的核心设计原则源自 Self 和 Scheme 编程语言。

JavaScript 早于 1996 年 8 月发布的 Internet Explorer 3.0 中引入。方言被认为是相似的，因此“JavaScript”和“JS”术语互换使用。然而，微软指出在许多情况下 JavaScript 并不是 ECMAScript。

JavaScript（相反，JavaScript 有函数级作用域）。然而，JavaScript 1.7 通过 `let` 关键字支持块级作用域。像 C 一样，JavaScript 区分了表达式和语句。与 C 的独特之处在于自动分号插入，其中可以省略分号。

1996 年 11 月，Netscape 宣布已将 JavaScript 提交给 Ecma International 作为行业标准，并致力于名为 ECMAScript 的标准。

## 动态

### 动态类型

与大多数脚本语言一样，类型与值关联而非变量。例如，变量可以绑定到数字，随后重新绑定到字符串。JavaScript 提供了测试对象类型的各种方法：

## 历史

JavaScript 最初由 Netscape 的 Brendan Eich 开发并命名为 Mocha，后来重命名为 LiveScript，最后更名为 JavaScript。当它在 1995 年 9 月首次在 Netscape Navigator 2.0 中发布时，JavaScript 是该语言的官方名称，但在 1995 年 12 月 4 日进行了重命名。

# JavaScript

局部变量和参数值会成为内部函数内部状态的一部分，即使在外部函数（闭包）执行后也是如此。

（JavaScript 的实现。）

提议纳入未来的 ECMAScript 版本，现在已在此处进行记录。

# 变参函数

可以向函数传递无限数量的参数。函数可以通过形式参数和本地的 `arguments` 对象来访问它们。

# 简单示例

一个简单的递归函数：

JavaScript 允许创建嵌套函数，其词法作用域位于定义处，并有一个 `()` 运算符可以在现在或稍后调用它们。在科学上，这种在定义范围之外创建、并在执行期间使用其独立作用域的代码绑定被称为“闭包”。

```javascript
function factorial(n) {
  if (n === 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
```

# 数组和对象字面量

像许多脚本语言一样，数组和对象（其他语言中的数组）可以使用简洁的语法创建。事实上，字面量构成了 JSON 格式的基础。

一个简单的个性化问候：

# 正则表达式

```javascript
var name = prompt("What is your name?");
alert("Hello " + name + "");
```

JavaScript 支持正则表达式的方式与 Perl 类似，它可以为文本处理提供了一种简洁且强大的语法，比内置函数更复杂。

匿名函数（或 lambda 表达式）：

```javascript
function add(i, j) {
  var lambda = function(x, y) {
    return x + y;
  };
  return lambda(i, j);
}
```



# 厂商特定特性

JavaScript 由 Mozilla 官方管理，并定期添加新功能。然而，只有非 Mozilla JavaScript 引擎支持以下内容：

- 属性和 setter（由 WebKit、Opera、ActionScript 和 Rhino 支持）
- 采用的条件缓存
- 来自 Python 的迭代器协议
- 来自 Python 添加的生成器/协程
- 同样来自 Python 添加的数组比较和生成器
- 使用 `let` 关键字的正确块作用域
- 数组和对象解构（模式匹配限制）
- 简洁的函数表达式 `(args)`
- 用于 XML 的 ECMAScript (E4X)，该扩展为 ECMAScript 增加了原生的 XML 支持

# 闭包

```javascript
function incrementClosure() {
  var count = 0;
  return function() {
    count++;
    return count;
  };
}
```

JavaScript 使用原型而不是类来进行继承。可以使用原型实现许多基于类的功能。

# 作为构造函数的函数

函数在与其典型角色的同时兼任对象构造函数。使用 `new` 构造函数会创建一个新对象，并调用该函数，将其 `this` 关键字绑定到该实例上。构造函数的原型描述了该对象。JavaScript 的内置构造函数（如 `Array`）也具有可以修改的原型。

# 作为方法的函数

与面向对象的语言不同，函数定义和方法之间没有区别。相反，实例化发生在函数调用期间：当一个函数可以作为对象的方法调用时，`function` 关键字将绑定到该对象上进行调用。

```javascript
function incrementCounter()
```

JavaScript 通常依赖于运行时（在 Web 浏览器中）可以与“外部世界”交互的对象和方法。事实上，它依赖环境来导入脚本（HTML `script` 元素）。（这是真正的语言特性，但在大多数环境中很常见）

# 杂项

# 运行时环境

变参函数演示。
带有 1、2 和 3 参数的 `alert` 是一个特殊变量。

# 语法与语义

截至 2009 年，该语言的最新版本是 JavaScript 1.8.1。它是 ECMAScript (ECMA-262) 的子集。语言的扩展包括部分 X4 (ECMA-357) 支持和实验性特性。

# JavaScript

```javascript
function unlimitedArgs() {
  for (var i = 0; i < arguments.length; ++i) {
    alert(arguments[i]);
  }
}
```

```javascript
unlimitedArgs(1, 2, 3);
```

# 高级示例

此示例代码展示了各种 JavaScript 特性。

```javascript
/* 计算两个数的最小公倍数 */
function LCMCalculator(x, y) {
  // 构造函数
  var checkInt = function (x) { // 内部函数
    if (x !== 0) {
      throw Error(x + " is not an integer"); // 抛出异常
      return x;
    }
    this.a = checkInt(x); // 分号是可选的
    this.b = checkInt(y);
  }
}
```

```javascript
/* 由构造函数创建的对象实例的原型是
   该构造函数的 "prototype" 属性;
   LCMCalculator.prototype = { // 对象字面量
     constructor: LCMCalculator,
     当重新分配原型时，
     constructor 属性会适当地
     gcd: function () { // 计算最大公约数
       // 欧几里得算法：
       var a = Math.abs(this.a), b = Math.abs(this.b);
       if (a < b) {
         // 交换变量
         t = b;
         b = a;
         a = t;
       }
       while (b !== 0) {
         t = b;
         b = a % b;
         a = t;
       }
       // 只需要计算 GCD
       // 所以 "redefine" 此方法。
       // （实际上是重新定义 - 它是定义在实例本身上的）
       this.gcd 指向此
       "redefinition" 而不是
       LCMCalculator.prototype.gcd;
       // 也，.gcd = "gcd", // 这
       this['gcd'] = function () {
         return a;
       };
     }
   }
```

```javascript
/* "cm" 这里可以使用字符串：
   function() {
     // 变量名不会与
     对象属性冲突，例如 [cm] 不是
     this.cm;
     // 使用 [this.a] 来
     避免精度问题
     var cm = this.a / this;
     // 只需要计算 cm
     一次，所以 "redefine" 此方法。
     this.cm = function() {
       return cm;
     };
     return cm;
     toString: function () {
       return "LCMCalculator: a = " + this.a + ", b = " + this.b + "";
     }
   }
   // 注意：map() 和 forEach()
   定义在 JavaScript 1.6 中。
   // 它们在 Firefox、Chrome、Opera 等中实现
   目前不在 Internet Explorer 中。
   // 它们在这里被用于演示
   JavaScript 的本质。
```

```javascript
[25, 55], [21, 56], [22, 58], [28, 56];
map(function(pair) { // 数组映射
  return LCMCalculator(pair[0], pair[1]);
});
sort(function(a, b) { // 比较函数
  return a - b;
});
forEach(function () {
  // 注意：print() 是 JS 内置
  // 在 Mozilla 的 CLI 中可用
  // 功能上等同于
  Java 的 System.out.println。
  // 在 Web 浏览器中，print() 非常不同
  // 打开 "Page Title" 所以使用 document.
  write(is better).
  // alert (obj, ) = * + obj.l(); + obj.cm();
  // alert (obj) + "gcd" = * + obj
  gcd(obj) + "cm" = * + obj;
  document.write(obj) + *, gcd = *
```

# JavaScript



`obj.gcd()` , `lcm = " + obj.lcm() + "<br>");`

以下输出应该在浏览器窗口中显示：

- `LCMCulator: a = 28, b = 56, gcd = 28, lcm = 56`
- `LCMCulator: a = 21, b = 56, gcd = 21, lcm = 168`
- `LCMCulator: a = 25, b = 56, gcd = 5, lcm = 270`
- `LCMCulator: a = 22, b = 58, gcd = 2, lcm = 638`

用户界面逻辑用 `JavaScript` 编写，`JavaScript` 向服务器请求信息（例如 `e-message` 的内容）。`JavaScript` 分发这些请求。更广泛的 `Ajax` 编程极大地简化了这一过程。

`JavaScript` 引擎（也称为 `JavaScript` 解释器或实现）是解释 `JavaScript` 源代码并执行脚本的解释器。`JavaScript` 引擎由 `Brendan Eich` 在 `Netscape` 公司创建，用于 `Navigator` 浏览器。代码名为 `SpiderMonkey`，用 `C` 语言实现自 `JavaScript (1.5)` 以来已更新到 `ECMAScript-262`。

如果使用 `Internet Explorer`，示例将产生错误。消息说明 `Internet Explorer` 中的 `JavaScript` 解释器与其他浏览器的 `ECMAScript` 解释器代码不同。（查看源代码中的注释以了解差异。）

由 `Neil Fox` 创建的引擎（现在 `Google` 大多数浏览器）是用 `Java` 编写的 `JavaScript` 实现。`Rhino` 符合 `ECMAScript-263` 标准。

## 在网页中的用途

`JavaScript` 的主要用途是编写嵌入 `HTML` 或从 `HTML` 页面调用的与页面对象模型 (`DOM`) 交互的函数。这种用途的一些简单示例有：

- 打开或弹出新窗口，并对新窗口的大小和属性进行程序化控制（是否菜单、工具栏等）
- 验证函数的值以确保它们在提交到服务器之前是正确的
- 当鼠标移动过图像时更改图像：这种效果通常用于通过图形元素将用户的注意力吸引到重要链接。`JavaScript` 代码可以在浏览器的运行时（而不是服务器上）本地运行以检测用户操作，使应用程序更具响应。此外，`JavaScript` 代码可以检测 `HTML` 无法检测的用户操作，例如单个击键。`Gmail` 等应用程序利用了这一点：

## 兼容性考量

由于 `JavaScript` 运行在各种不同的环境中，测试和调试的重要部分是跨浏览。

用于操作页面的 `DOM` 接口不是 `ECMAScript` 标准的一部分，也不是 `JavaScript` 本身的一部分。官方上，它们由 `W3C` 的分离工作定义；在实践中，实现与标准以及彼此之间差异，并不是所有浏览器都执行 `JavaScript`。

为了处理这些差异，`JavaScript` 作者可以选择编写符合标准的代码，这些代码将由浏览器正确执行；他们可以为某项功能的存在编写代码，并在功能不可用时表现得不同。在某些情况下，浏览器可能会实现某个功能但行为不同，可能会发现检测运行的是哪种浏览器并更改其脚本的行为。程序员可能还会使用考虑了差异的库或工具包。

`Web` 浏览器是 `JavaScript` 最常见的环境。浏览器通常使用公有 `API` 创建表示 `DOM` 树的“对象”。`Web` 服务器是 `Web` 的另一个常见应用。`JavaScript` 服务器将使用 `HTTP` 请求和响应对象的宿主对象，`JavaScript` 程序可以动态生成网页。

一个符合标准的最小网页示例（使用 `HTML 4.01` 语法）如下：

此外，脚本可能需要为某些用户处理。例如，用户可能会：

- 使用 `DOM` 支持不完整或异常的旧浏览器，
- 使用无法执行 `JavaScript` 的 `PDA` 或移动浏览器，
- 出于安全考虑，禁用了 `JavaScript` 执行，
- 由于视觉示例的原因，使用了语音浏览器。

用户可能没有意识到，页面内容的非预期变化会降低用户的控制感。

通常，让一个复杂的 `Web` 页面尽可能具有无障碍性是一个殊而易的问题，最终往往会在争论和意见分歧中达成妥协。然而，用户能够防止 `XSS` 攻击，例如那些恶意代码存储在数据库中的攻击。只有服务器端 `Web` 应用的设计正确才能完全防止 `XSS`。

为了支持这些用户，`Web` 开发者尝试为不支持 `JavaScript` 的用户（浏览器）创建质量降级的页面。特别是，页面应该保持存在，尽管缺少了 `JavaScript` 允许的功能。许多人认为优的替代方法是使用在所有支持 `JavaScript` 的浏览器中运行的基础技术，然后对其进行增强以获得更好的支持。这被称为渐进增强（`progressive enhancement`）。

`XSS` 漏洞也可能由于作者的实现错误而发生。另一种跨站漏洞是跨站请求伪造（`CSRF`）。在 `CSRF` 中，攻击者网站会欺骗受害者的浏览器在某个站点执行用户并非意图的操作（如在银行转账）。因为，如果站点仅依赖 `Cookie` 进行身份验证，那么由攻击者站点发起的请求将携带与用户请求相同的登录凭据。`CSRF` 的通用解决方案是要求在隐藏字段中提供一个值（而不仅仅是在 `Cookie` 中），以验证任何可能产生持久影响的操作。检查 `HTTP Header` 也有帮助。

## Security

假设用户没有使用其执行功能，客户端 `JavaScript` 的编写应该增强视觉残障用户的体验，并且绝对应该避免误导这些用户。

`JavaScript` 和 `DOM` 允许恶意作者在不通过浏览器的情况下向客户端计算机投递脚本。浏览器开发者尝试使用限制措施。脚本在沙箱中运行，在沙箱中可以执行良好的操作，而不是像创建文件这样的通用编程任务。脚本受到相同策略的限制：来自一个站点的脚本无法访问用户名、密码或发送到其他站点的 `Cookie` 等信息。大多数 `JavaScript` 相关的安全防护都是针对相同策略或沙箱的影响。

盲人和部分视力人士使用的屏幕阅读器可以在页面更改后通过 `JavaScript` 访问并读取页面 `DOM`。然而，`HTML` 应该是简洁的，无论脚本是否运行 `JavaScript`，在语义上都不应完全依赖于特定的鼠标事件来完成对那些选择不使用鼠标或因需求选择键盘的用户有益的操作。此外，尽管超链接和链接可以通过键盘导航和操作，但 `JavaScript` 也不应要求键盘事件。诸如 `focus` 等与设备无关事件优于

## Cross-site vulnerability

常见的与 `JavaScript` 相关的安全问题是跨站脚本，或 `XSS`，这是对相同策略的违反。`XSS` 漏洞发生在攻击者能够针对 `Web` 站点（如在线网站），在展示给用户的 `Web` 页面中包含恶意脚本时。在这种情况下，他们可以以受害者的权限访问银行，可能窃取信息或以受害者的身份进行交易。`XSS` 的解决方案是使用 `HTML` 编码而不是显示不可信的数据。

使用 `JavaScript` 的方式不让任何 `Web` 用户感到困惑或迷失方向。使用脚本更改浏览器的主要功能（如更改后按钮或刷新事件）是徒劳的。同样，触发此

某些作者对 `XSS` 攻击提供了部分防护，即攻击者使用包含恶意脚本的 `URL`。然而，即使是其中一些防护也存在脆弱性。

## Misplaced trust in the client

客户端-服务器开发者，无论是否使用 `JavaScript`，都要意识到用户可能受到攻击者的控制。任何嵌入在 `JavaScript` 中的脚本都可能被检测到的对手提取，且应用程序作者无法保证该 `JavaScript` 按预期运行，或根本不运行。影响如下：

- `Web` 开发者无法隐藏其 `JavaScript` 的运行方式，代码被发送到客户端，混淆的代码可以被反向工程。

`JavaScript` 验证仅为用户提供便利，而不是安全性。如果用户同意服务条款，或者从包含数字的字段中过滤无效字符，必须在服务器端而非客户端执行。

脚本可以被选择性禁用，因此不能依靠 `JavaScript` 来防止“保存图像”等操作。

在 `JavaScript` 中嵌入（那里可以被攻击者提取）可能是糟糕的，然后让 `JavaScript` 验证用户密码并向服务器返回“`password=ok`”（因为“`password=ok`”很容易被伪造）。

例如创建或删除文件的权限。当然，权限不应从 `Web` 授予。

错误地向 `Web` 授予权限在 `Internet Explorer` 和 `Firefox` 之间的差异中起过作用。在 `Windows XP Service Pack 2` 中，微软在 `Internet Explorer` 中开发了 `JavaScript` 的原语。`Microsoft Windows` 允许计算机驱动器上的 `JavaScript` 文件作为非沙箱项目启动。这使得 `JavaScript` (`VBScript`) 对木马来说是可见的，尽管在实践中 `JavaScript` 木马并不常见。（参见 `Windows-docs Help`）。

## JavaScript - page 101

`VRML97` 用于 `VRML` 描述文件的脚本节点。

- 高端 `HTML` 通用遥控器使用 `TSU6600` 和 `TSU9400`，可以使用基于 `JavaScript` 的工具 `Pronto` 进行脚本编写。

`Firefox` 是一个开源计算机程序，旨在制作使用 `JavaScript` 作为脚本语言的角色扮演游戏。

- 开源 `Re-Animator` 框架允许使用 `JavaScript` 和 `XML` 开发基于 `2D Sprite` 的游戏。

- `ing` 是一个网络爬虫，使用 `JavaScript` 脚本进行自定义过滤器解析器。

- `Unity` 游戏引擎支持 `JavaScript`（除了 `C#`）。

- `Studio` (`IDE`) 使用 `JavaScript` 的 `SpiderMonkey` 实现。

- `Maxwell`（渲染软件）使用 `ECMA` 标准脚本引擎。

- `Google Apps Script` 表格和 `Google Sites` 允许用户创建公式、重复任务，并与其他产品交互。

- 许多中继聊天（`IRC`）客户端如 `Chatilla` 或 `XChat` 使用 `JavaScript` 实现其脚本能力。

## Browser and coding errors

`JavaScript` 为各种浏览器提供了接口，其中某些浏览器存在缓冲区溢出等缺陷。这些缺陷允许攻击者编写脚本以运行他们想要的任何代码。

这些缺陷已经影响了 `Firefox`、`Internet Explorer` 和 `Safari` 等主流浏览器。

插件（如视频播放器 `Adobe Flash` 以及 `Microsoft Explorer` 中默认启用的系列 `ActiveX` 控件）也存在可以通过 `JavaScript` 利用的缺陷，这些缺陷在过去已被暴露。

在 `Windows Vista` 中，微软试图通过以限制权限运行 `Internet Explorer` 进程来降低如缓冲区溢出等漏洞的风险。`Google Chrome` 在其“沙箱”中限制渲染器。

## Sandbox implementation

`Web` 浏览器能够在沙箱外运行 `JavaScript`，带有

## Embedded scripting language

在浏览器中，`JavaScript` 在许多工具中被解释。这些应用程序中的每一个都提供了它们自己的对象来访问环境，而 `JavaScript` 语言在每个应用程序中保持基本相同。

- `Google Chrome`、`Opera` 扩展、`Safari 5` 扩展、`Dashboard Widget`、`Google Widgets`、`Desktop Tasks` 和 `Server Kilifio` 均使用 `Adobe` 实现。`Adobe Acrobat` 和 `Adobe Reader` 支持 `PDF` 文件中的 `JavaScript`。`Creative Suite` 中的工具（包括 `Photoshop`、`Dreamweaver` 和 `InDesign`）允许通过 `JavaScript` 脚本。

- `OpenOffice` 办公套件将 `JavaScript` 作为其脚本语言之一。

- 由 `Cycle 7` 的交互式音乐处理软件 `Max/MSP` 为用户提供其环境的 `JavaScript` 模型。它比默认的 `GUL-content` 编程语言提供了更多的控制

## Scripting engine

- 微软的 `Active` 支持 `JavaScript` 作为脚本语言。这通常被认为兼容 `JavaScript`，但许多许多不符合 `ECMAScript` 的 `JavaScript` 特性。

- `Java` 语言在 `SE 6` 版本（`JDK 1.6`）引入了 `javascript.script` 包，允许基于 `Mozilla Rhino` 的 `JavaScript` 实现。因此，`Java`

## 102 - JavaScript

应用程序可以托管访问环境变量和对象的脚本，而 `Web` 浏览器则托管访问网页浏览器文档对象模型（`DOM`）的脚本。

- `Qt` 工具包允许将 `JavaScript` 解释为 `Java` 的 `javascript` 包。
- `JSDB`（用于数据库的 `JavaScript`）是一个适用于 `Windows`、`OS X`、`Linux` 和 `Unix` 的开源 `JavaScript` 引擎，它通过文件、数据库和网络对象扩展了 `Mozilla` 的 `JavaScript` 引擎。
- `jlibs` () 是一个适用于 `Windows` 和 `Linux` 的开源 `JavaScript`，它扩展了 `Mozilla JavaScript` 引擎，使其具备在常见的调用函数的能力。
- `LateSoft JavaScript OSA`（或 `JSOSA`）是 `Mac OS` 上 `AppleScript` 的免费替代方案。它基于 `Model 1.5 JavaScript` 实现，并添加了针对操作系统和第三方应用程序的 `MacOS` 对象。

`Adobe Runtime`（`Adobe` ）是一种允许开发者创建桌面应用程序的运行时环境。

`myNFC` 是一个基于 `JavaScript` 的框架，允许开发者为智能手机创建应用程序。

- 在其 `SDK` 中使用了 `WebKit` 的 `JavaScript` 实现，允许开发者仅使用 `JavaScript` 即可创建独立应用程序。

`CA, Inc.` 的 `AutoSelf` 应用程序脚本环境基于 `JavaScript/SpiderMonkey` 构建，并带有用于命令定义的预处理器扩展以及针对各种系统如 `i/o`、操作系统和 `COM` 重定向与销毁的自定义任务。

`GNOME shell` 是 `GNOME 3` 桌面环境。`Gjs`（来自 `GNOME`）和 `Kjsmed`（来自 `KDE`）包旨在利用这些环境。

`Qt` 的标记语言（`QML`）使用 `JavaScript` 处理应用程序逻辑，其声明式语法也是 `JavaScript`。`QML` 从 `4.6` 版本开始可用。

## 开发工具

在开发大型、复杂的项目时，项目内的工具变得至关重要。不同浏览器之间（特别是在文档对象内部）可能存在差异，因此为 `Web` 应用程序目标浏览器准备调试器是很有用的。

`Internet Explorer`、`Firefox`、`Safari`、`Chrome` 和 `Opera` 都提供了脚本调试器。

`Internet Explorer` 提供三种调试器。`Visual Studio` 是其中之一，紧随其后的是 `Microsoft Script Editor`，最后 `Microsoft Script Debugger` 比另外两个要基础得多。免费的 `Visual Studio Developer` 在 `Visual Studio` 解释器中提供了有限的 `JavaScript` 调试功能。

`Firefox` 中的 `Web watchins`（视）使用 `Firefox` 插件或其他调试器。`Opera` 有内置的错误控制台（`Error Console`），可以记录变量和 `JavaScript`。它还会记录 `CSS` 错误和警告。

`Opera` 包含一组名为 `DragonFly` 的工具

`DragonFly Web Inspector` 是 `Safari` 和 `Google Chrome` 中的 `JavaScript` 调试器。

某些调试器是用 `JavaScript` 编写的并构建在 `Web` 上运行的。例如由 `Douglas Crouch` 开发的程序，他是 `Yahoo` 的高级 `JavaScript` 架构师；他编写了大量的 `JavaScript` 代码以符合一系列标准和指南。`Web` 开发书签和 `Firefox`

`MimMe` 是一个开源 `JavaScript` 压缩器、混淆器和代码检查工具

## 相关功能与特性

`Objective-J` 是一种符合标准 `JavaScript` 的语言。它为 `JavaScript` 添加了传统的继承、`Smalltalk/C` 风格的动态派发以及可选的伪静态派发。

`CoffeeScript` 是 `JavaScript` 的替代方案，旨在更加简洁易读，并增加了数组比较和模式匹配等功能。`Objective-j`、`Python` 和 `Ruby` 已经在 `CoffeeScript` 中实现。

`jQuery` 和 `Prototype` 是用于编写面向 `DOM` 的客户端 `HTML` 的 `JavaScript` 库。

`TIScript` 是 `JavaScript` 的子集，包含类、名称和 `lambda` 声明。

`JSON`（或 `JavaScript` 对象表示）是一种通用的数据交换格式，被定义为 `JavaScript` 的子集。

`Mozilla` 浏览器目前支持 `LiveConnect`，这是一个允许 `JavaScript` 与 `Web` 交互的功能。`Mozilla` 对 `LiveConnect` 的支持在未来将逐步淘汰，取而代之的是通过 `NPAPI` 传递给 `JavaScript 1.6+`。

## JavaScript OSA - 第103 页

（截至 2010 年 3 月 `Mac` 不支持）。大多数浏览器检查工具（如 `Firefox` 中的 `Firefox`）都包含了可以操作页面 `DOM` 的 `JavaScript` 解释器。

`JavaScript` 在设计时包含了 `Java` 的语法和标准库。特别是，所有关键字在原始 `JavaScript` 中都有提供，`JavaScript` 的标准库遵循 `Java` 惯例，`JavaScript` 的 `Date` 对象基于 `Java 1.0` 的类。

然而，`Java` 和 `JavaScript` 之间的相似之处在于具有静态类型；`JavaScript` 的类型是动态的（变量可以是任何对象且不能被限制）。`JavaScript` 是从字节码加载的；`JavaScript` 是作为可读源码加载的。`JavaScript` 是基于原型的。`JavaScript` 还具有许多基于 `Scheme` 语言的特性。

## JavaScript 和 Java

常见的误解是 `JavaScript` 与 `Java` 相似或相关。它们都具有类 `C` 语法，`C` 语言是它们最常见的祖先语言。它们都是面向对象的、沙箱化的（当在浏览器内部使用时），并广泛应用于客户端 `Web` 应用程序。此外，

> “`JS` 必须取像‘`Java`’这样的名字，所以说，`Java` 只是浏览器或无聊的点击。此外，它必须在十天内完成，否则就会发生更糟糕的事情”
> `Brendan Ek`

## JavaScript OSA

`JavaScript OSA`（原名为 `JavaScript for OSA`，缩写为 (`OSA`)）是一种用于 `Macintosh` 计算机的免费进程间通信语言。

在 `Windows` 机器上对应 `Microsoft .NET` 语言，尽管两种语言的系统层级脚本之间没有互操作性。

该语言首次于 2001 年发布，并与 `Late Night` 的软件注册程序 `Project Descriptor` 捆绑。2005 年，发布了新的“`alpha`”版本语言供测试。这个改进版本的语言与 `Script Debugger 4.0` 版本捆绑。

`JavaScript OSA` 使用 `Mozilla` 编程语言的“核心语言”（`SpiderMonkey`）。该语言被用作 `Apple` 语言的替代。它的使用与基于器的脚本密切相关。

## 描述

该语言与 `Mozilla` 编程语言相同，扩展了 '`Core`' 和 '`MacOS`' 对象。`Mac` 对象具有获取绑定到应用程序的方法。这是通过 `AppleEvent` 系统实现的，它是 `Macintosh` 开放架构的一部分。

## JavaScript 样式表

`JavaScript` 样式表（`JSS`）是 `Netscape Communications` 在 1996 年提出的一种样式表技术，旨在为页面提供活性，是层叠样式表（`CSS`）的替代方案。尽管提交给了世界网联盟（`W3C`），但该技术未被接受为正式标准，在市场上未获得普及。`Netscape 4` 支持 `JSS`，而 `Internet Explorer` 浏览器不支持。在 `Netscape` 1997 年发布后，它停止了推广 `JSS`，转而遵循 `CSS` 标准，后者也被 `Internet Explorer` 支持并获得了更广泛的认可。`Netscape Communicator` 的后续版本 `Netscape 6`（2000 年发布），该脚本现在仅仅是一个历史注脚，许多开发者甚至不知道它的存在。该提议的标准尚未完成。

使用 `JavaScript` 作为样式表，`JSS` 通过修改元素的属性来识别元素。例如：

```



`h1 { font-size: 20pt; }`

等同于 JavaScript：

```javascript
document.tags.h1.fontSize="20pt";
```

# 104 - 作业控制语言 (Job Control Language)

作业控制语言（JCL）是一种用于 IBM 主机系统的脚本语言，用于指示系统如何运行作业或启动系统。“作业控制语言”也可以指代所有执行这些功能的语言，例如 Burroughs 的 WFL 和 OCL。本文专门介绍 JCL。在 DOS 和 OS 系统的 JCL 中，“卡片”（`card`）指的是 JCL 卡片，打印在作业结束报告上的序列号对于识别操作系统报告的任何错误位置非常有用。第 72 个字符通常留空，以将实际 JCL 与 OS JCL 隔开；它可以包含注释的延续行（见下文）。

存在两种 JCL：一种用于操作系统系统，从 DOS/360 开始，其最新成员是 V/2SE；另一种源自 OS/360 的行版本。它们共享一些语法规则和少数基本概念，但区别非常大。

所有命令、参数名和值必须大大写，US 文件名除外。

## DOS 和 OS JCL 的特性

除了流式输入（见下文）外，所有行必须以斜杠 `/` 开头，所有的操作系统进程必须从第一行开始。然而，有两个例外：删除语句和注释语句。删除语句以斜杠和星号 (`/*`) 开头，注释语句以一对斜杠和星号 (`//*`) 开始。

## 作业、步骤和过程

在两种 JCL 中，作业都由一个或多个步骤组成，每个步骤都是对一个特定程序的请求。例如，在关系数据库出现之前，一个为管理层生成报告的作业包含以下内容：一个用户编写的程序用于收集相应的记录并将其复制到临时文件；一个通用实用程序排序临时文件；一个用户编写的程序以终端用户易读的方式呈现信息，并包括小计等其他信息；以及一个用户编写的程序用于格式化终端用户输入的选择内容。

处理过的过程（通常称为 `procedures`）是用于一组步骤的预写 JCL，插入到作业中。两种 JCL 允许使用此类过程。对于在一个作业中多次或在多个不同时间重复步骤的程序，可以节省时间并减少错误概率。过程在 JCL 文件中包含一个“卡片”，其中包含从指定文件生成的代码并将其插入作业中。还包含参数以对每次使用的的过程进行自定义。

## 基本语法

两者 DOS 和 OS JCL 的最大行长度均为 80 个字符；当 DOS/360 和 OS/360 最初使用时，提供输入的方法是通过打孔卡系统。后来可以通过磁盘或具有长记录的磁带提交作业，但操作系统的作业提交会忽略 80 个字符之后的内容。

严格遵守操作系统的家族每行仅使用 71 个字符。第 72-80 字符通常留空。

最常见类型的卡片结构为：

- `//`
- 卡片的名称，紧跟在 `//` 之后且之间没有空格
- 语句类型
- 空格（多个）
- 取决语句类型而变化的参数，用逗号分隔且它们之间没有空格
- 标识作业
- 提供信息以使计算机部门能够对接相应的用户部门
- 定义整个作业要做什么，以及它相对于队列中其他作业的优先级
- 结束除最后一张之外的所有 JCL 卡片，语法要求在此处使用 `/`
- 每个延续语句在第 1 列使用 `//` 并至少有一个空格
- 许多 JCL 语句太长，无法放入 71 个字符内，但可以扩展到无限数量的延续卡

部分复杂性源于设计不当——大部分复杂性源于 JCL 环境，当时的硬件预期是：

- 低端 System/360 CPU 的性能远低于且价格远高于为 MS-DOS 设计的 80 年代中期 PC。System/360 用于内存至少为 32 KB 的系统，而 DOS/360 至少 16 KB，且 360/30 CPU（1964 年 System/360 引入时为低端）每秒执行 16 条指令。IBM PC (1981) 拥有 1 KB 或 64 KB 内存，每秒可以处理约 330,000 条指令。因此，JCL 对计算机来说很容易处理，程序员使用起来也价格低得多。在许多更便宜的计算机中，JCL 设计用于批处理，通常由位于用户办公室另一栋楼的计算机执行。根据步骤的结果由操作系统决定做什么。例如，如果程序运行成功，则执行 `DIS=CATLG` 创建新文件；否则删除新文件。

## 流式输入

OS 和 JCL 都允许流式输入，即由程序处理而非操作系统处理的“卡片”。长期保留的数据通常存储在磁盘上，但使用终端通过在卡片上提供新数据仍然编辑和删除文件的唯一方法。

OS 和 JCL 有不同的方式标记流式输入的开始，但都以最后一行卡片列中的 `"*"` 结束。`DD` 语句可定义流式数据以及集合。默认的 `DD` 语句在标识符后跟有一个星号 (`*`)。JCL 语句可以利用原始 JCL 的特性作为流式数据的一部分，以避免重写它们的 JCL。但后来引入了替代方案，因为大多数 JCL 语句可能会被使用超过两次。

## 位置参数

在 DOS JCL 中，位置参数更难读和写：

- 使用 `&` 标识每一项
- 如果某些参数被省略，但其他参数被包含，必须用逗号表示

## 关键字参数

OS JCL 由关键字参数赋值一个值：

- `JOB` 语句标识作业的开始以及关于作业的信息，例如时间限制
- `EXEC` 语句标识要执行的程序，以及关于步骤的信息
- `DD`（数据描述）标识步骤中的数据文件，关于该文件的信息

## 设备独立性

从开始，OS 家族提供了高程度的设备独立性。对于新文件，可以在作业语句中指定特定的设备类型，例如 `DISK` 或 `TAPE`。

## 覆盖能力

这种覆盖功能主要用于创建新文件。自 1964 年 System/360 发布以来，OS 的这种旧样式更加灵活且易于使用。

## 复杂性

通过一个简单的示例可以很好说明。在 MS-DOS 中复制文件会使用简单的命令，而在 OS/360 中会使用类似下面的：

```
//JOB(0000),CLASS
//COPY EXEC PGM=BEAMEN
//SYSOPR DD SYSOUT=
//SYSUT1 DD OLDFILE,DISP=SHR
//SYSUT2 DD NEW-FILE,DISP=(NEW,CATLG,DELETE)
//SPACE=(40,5)
//DCB=(LRECL=80,BLOCKSIZE=1150)
```

DOS JCL 通过更多的参数缓解了定位的困难。`EXTENT` 和 `DATA` 语句执行相同的工作（指定新文件的存储位置）。

## 回调

在多步骤作业中，后一个步骤可以使用回调，而不是指定早先步骤中已经指定的文件。在此过程中，所有带有 `&` 符号的值都将在作业请求该过程时指定。因此，每个代码可以使用同一个过程创建不同大小和布局的新文件。

```
//MYPROC
//MYPR01 EXEC PGM=
//NEWFILE DD-
//&FILE,UNIT=DISK,SPACE=
(TRK,50,1000),
//DCB=(RECL=80,BLOCKSIZE)
//(CATLG,DELET)
```

OS JCL 的所有主要语句通过关键字标识，并可以任何顺序呈现。其中一些包含两个或多个参数，例如 `SPACE`（为新文件分配多少块空间）和 `DCB`（文件长度的详细规格）。子参数有时是位置的，但最复杂的参数，

```
//MYPR02 EXEC PGM=
//INPUT01 DD NAME*=MYPR1
NEW
```

在包含作业特定 JCL 和过程调用的混合作业中，作业特定的步骤可以引用一个

# 作业控制语言 - 第107页

这在过程过程中被完全指定，例如

## 合并输入文件

OS JCL 允许程序对输入文件进行合并（“链”），使其显示为一个文件，例如：

```
//STEP05 EXEC PGM
//MYJOB JOB
//PROG05,COND=(EVEN,STEP03)
```

使用过程

```
//STEP02 EXEC PGM=
```

特定于此步骤（`Step`）

```
//INPUT01 DD DSN=*STEP01.
//MYPRO.NEWFILE
```

意味着：

```
//INPUT01 DD DSN=//MYFILE.01;DIS=SHR
//DD DSN=JOESFILE,DIS=SHR
//DD DSN=SUIESFILE,DIS=SHR
```

- 运行 `STEP02` 并收集其返回码
- 如果该数字大于 `STEP01` 的返回码，则不运行 `STEP02`
- 如果该数字小于或等于之前的任何返回码，则不运行 `STEP03`
- 仅当 `STEP01` 正常结束时才运行 `STEP04`
- 即使 `STEP03` 正常结束，也运行 `STEP05`

`DSN=*STEP01,MYPRO.NEWFILE` 使用“此作业中 `STEP01` 所用过程中的定义的文件”。引用中使用调用过程的步骤名称，然后是过程的名称，以便在同一个作业中使用该过程，而不会产生过程实例的混淆。

第二和第三条语句在名称上没有值，因此 OS 将其视为合并。文件必须具有相同的类型（几乎是顺序的），并且具有相同的记录长度。

## 条件处理

OS 期望程序返回一个指定如何使用的代码。最常见的约定是：

- `0` 全部正常
- `4` = 轻微错误或问题
- `8` = 重大错误或问题
- `12` = 严重错误或问题，不应使用结果（例如报告）
- `16` = 严重问题，但有结果

这被翻译为以下伪代码

```
run STEP01
if STEP01's return code is greater than equal to 4
    run STEP02
if any previous return code is less than 8
    run STEP03
not end
if STEP01 normally ended then end
    run STEP04
if STEP03 normally ended then end
```

## 注释

JCL 文件可能很长，且该语言并不容易阅读。OS JCL 允许程序包含两种类型的注释：

- 作为 JCL 语句位于行内。可以通过第 72 列的延续字符（ `X` ）进行扩展，随后在下一行的第 1-3 列中使用 `/`
- 仅使用注释的行用于解释 JCL 整体结构的要点，而不是局部细节。注释行也用于将 JCL 文件分成若干部分

OS JCL 将返回码称为 `COND`（“条件”），并用它决定是否运行后续步骤。然而，与现代编程语言不同，JCL 中的步骤在指定条件为真时执行——因此，如果“真”通过了[不运行代码]，则产生结果。更复杂的是，条件只能在其所引用的步骤之后指定。例如：

```
//MYJOB JOB
// 仅行注释。通常在分节内使用 JCL 列表 ***
//STEP01 EXEC MYPRO
//STEP02 EXEC PGM=\X
// 溢出到下一行。
//INPUT01 DD DSN=STEP01.
//MYPRO.NEWFILE
```

```
//MYJOB JOB 
//STEP01 EXEC PGM=PROG01
//STEP02 EXEC PGM
//PROG02,COND=(4,STEP1)
//STEP03 EXEC PGM
//PROG03,COND=(8,LE)
```

注意，通过反向读取包含 `COND` 语句的步骤，我们可以轻松理解它们。这是逻辑倒置的一个示例。然而，IBM 在 JCL 中引入了 `COND` 参数，以避免对现有的 JCL 做出更改：

```
//STEP04 EXEC PGM
```

## JCL 工具

JCL 使用许多 IBM 工具程序来协助数据处理。工具在批处理处理中非常有用。工具可以分为三类：(1) 数据集工具 - 创建、打印和删除数据集；(2) 系统工具 - 维护和目录；(3) 访问方法 - 处理 VSAM（虚拟存储访问方法）和非 VSAM 数据集。（编辑）：`http://en.wikipedia.org/wiki/Juk_Control_Language`

# JustScript

Juscript 是为在 Java 平台上进行脚本设计的通用编程语言之一。它的创始人和主要开发者是 Jianbo Huang，并访问 Java 平台内部的第三方库。然而，这些库在大多数应用程序开发需求方面具有比 Java 编程更高的经验水平。

由于 Juscript 的设计原则，Huang 认为它不适用于企业级应用开发，也不打算取代 Java。例如，脚本语言具有简化的语法（即“语法糖”），为 Juscript 编写的代码无法期望在 Java 中编译。

## 概述

Juscript 是专门为在 Java 平台上使用而设计的通用脚本语言之一。

## 语言特性

示例：一个简单的 HTML 例程：

```
do("http://www.example.com") as gql
<a>: print 'First link:',
<p>: print 'First paragraph.'
TEXT: print 'First some text:',
```

## 历史

Huang 最初将 Juscript 设计为一组语言，希望用于 J2EE 应用程序。该策略的基础是提供基础设施：(1) 使用 shell 的灵活性，这种权衡是 Juscript 提供了专门为特定领域编程设计的结构，已经在很大程度上通过丰富的可用性和标准库得以。（编辑）：`http://en.wikipedia.org/wiki/Juscript`

# Jython

Jython 是 Python 的继任者，是 Java 字节码中的编程语言实现，位于或动态。程序可以无缝地导入和使用任何 Java 类。除了标准模块外，Python 程序在 Jython 内部使用 Java 类。例如，Python 用户可以在 Jython 中使用 Swing、AWT 和 SWT 将 Python 编译为 Java 字节码（中间语言）。

## 历史

Jim Huffman 于 1997 年底创建了 Jython，最初是为了取代 C。1999年2月，Barry Warsaw 接任成为主要开发者。2000年10月，Jython 移动到了 SourceForge。2004年底，Python 辞去了主要开发者职位以专注于 Python，但他仍然是 Jython 的权威。2005 年，Brian Zimmer 获得了 Python 软件基金会的资助以开发 Jython。2005年12月，Weisz 成为主要开发者。2005 年期间，由于缺乏知识丰富的开发者，开发放缓了。长期以来，Sam Deville 完成了大部分的维护和开发工作。2006年3月3日，Sun Systems 宣布他们聘用了 Ted Leung 和 Franz Weisz 来开发 Python，类似于 Sun 聘用两个 Jruby 开发者。开发稳步进行，Jy 2.5.0 于2009年6月16日发布。（“python”）该实现与 CPython（参考发行版）有些不同，命令行解释器根据 Apache 软件许可可用。

## 状态和路线图

## 许可条款

# 使用

- Jython 是 Web-Sphere 应用服务器中使用的两种脚本语言（带有 `Jl`）之一。它用于 IBM Rational 开发工具，可以在那里创建项目。它被用 JHEP 分析框架的主要编程语言。当前版本是 Jython 2.5.2，自2011年3月起可用。Jython 2.5.2 包含了新功能，包括 socket 模块中的 IPv6 支持和性能增强，以及错误修复。Jython 2.5 实现了与 CPython 2.5 相同的语言特征。从 2.5.0 版本开始，Jython 能够运行 Django、Pylons 或 SQLAlchemy 等 Python 框架。从 2.0 版本开始，Jython（包括标准库）根据 Python 软件基金会许可（v2）发布。旧版本由 Jython 2.0、2.1 和 Jython 1.1.X 软件许可创建。前两个是宽松的自由软件许可证。第三个似乎也是，但不清楚，自由开源倡议未对其进行审查和注释。（编辑）：`http://en.wikipedia.org/wiki/Kawa/Jython`

# Kawa (Scheme 实现)

虽然 Python 语言技术上实现了规范，Kawa 是一个用 Java 编写的语言框架，实现了 Scheme 编程语言，并可用于实现其他语言。它是 GNU 项目的一部分。

相当于 `export CLASSPATH=$CLASSPATH:/path/to/kawa/kawa-1.1.0.jar` `java`

你可以通过以下方式访问对象的字段：为了将文件编译为类，使用 `-C` 参数 Kawa 的方法：

```
object:field-name
```



`java.repl --main file.class`

`(invoke object 'method...)`

这将产生一个`file.class`，可以通过输入`java class`来运行。

## 与 Java 的集成

除了使用 Scheme 编程语言，你还可以通过如下代码访问 Java 对象的字段和方法：（编辑）：`"http://en.wikipedia.org/wiki/Kawa_(Scheme_implementation)"`

你还可以使用函数`invoke-static`调用静态方法（在 Java 中创建静态函数），以及将 Kawa 与其他 JVM 实现相结合。

`(invoke object 'field)`

这将调用一个 Java 方法，并

## 如何使用

在 GNU/ 上运行 Kawa

# 110 - Kid（模板语言）

- 19/11/01 v4.00
- 21/01/02 v4.02
- 08/07/02 v4.10
- 26/08/02 v4.11
- 11/11/02 v4.12
- 17/02/03 v4.20
- 15/07/03 v4.21
- 14/11/03 v4.22
- 31/12/04 v4.23
- KiXT 2010
- 01/07/05 v4.50
- 06/10/05 v4.51
- 21/07/06 v4.52
- 15/09/06 v4.53
- 03/10/07 v4.60
- 24/09/04 v4.61

## 相关软件

其他图形软件也基于 KiXT 技术构建，包括流行的开源解决方案 Script Community Source（已编辑）：`http://en.wikipedia.org/wiki/KiXTart`

## Kid（模板语言）

Kid 是一个用于 Python 内部基于 XML 词汇的简单模板引擎。Kid 声称它兼备了 XSLT、TAL 和 PHP 的许多优秀特性，但剥离了大部分局限性和复杂性。虽然它被 TurboGears 框架大量使用，但由于具有更好的调试支持、基础 XPath 支持以及更好的性能，它看起来比 Genshi 更加简单且紧凑。

```python
from kid Import Template

template=Template(mytemplate.kid)

title='bar'

mylist=['1', '2', '3', '4', '5', '6']

template.serialize()
```

```html
<html xmlns="http://www.w3.org/1999/xhtml"
xmlns:py="http://purl.org/kid/ns#"
<head>
<title content="title">goes here</title>
</head>
<body>
<ul>
<li py:for="item in mylist"
py:content="item">item goes here</li>
</ul>
</body>
</html>
```

模板部分：

## 示例

Python 部分：

## Korn shell

Korn shell (`ksh`) 是一种 Unix 壳（shell），由 David Korn（任职 AT&T 贝尔实验室）于 20 世纪 80 年代初开发，并于 1943 年 7 月在 Toronto UNIXED 引入。早期贡献者包括 AT&T 贝尔实验室的开发者 Mike Veach（编写代码）和 Pat Sullivan（编写代码）。`ksh` 与 Bourne shell 向后兼容，并包含了 C shell 的许多功能，例如命令历史，其灵感源自贝尔实验室的请求。

`ksh93` 版本支持数组和内置浮点数算术。
交互式 shell `ksh` 提供了以一种类 wish 方式编辑命令行的能力，通过按下正确的光标上键或之前的按键序列来回命令，如果用户处于编辑行模式，则对命令进行编辑。提供了兼容 vi 和 Emacs 的模式。

通用公共许可证（Common Public License）。Korn Shell 作为 AT&T 开源软件集的一部分提供。它也可以通过 AT&T 的专有许可提供，并且仍然是免费开源的替代方案。这些包括公领域的 `mksh`，及其开发的后继者 Free Source Foundation 的 Bourne-Affine shell 以及 `bash`。

Korn Shell 的功能（从引入该起被称为 `ksh88`）被用 POSIX shell 的基础。
`ksh93` 版本带来了许多改进（关联数组、浮点数算术等），其中某些版本仍比 `ksh88` `/bin/ksh` 版本更好，仅有 2005 年前的某些例外情况，NCK UI（又名 Aster）

## 设计

`ksh` 相比其他语言的主要优势在于它可以作为一种编程语言使用。自构想以来，已经开发了若干功能，尽管它保持了与 Bourne shell 的强兼容性。

## 历史

直到 2000 年，Korn 仍然是 AT&T 的财产。从那时起，它是开源软件，最初采用 AT&T 的特定许可，但自 2005 年初发布 93 版本以来，它已根据合并到 `ksh93` 的供应商以及分发 `ksh93` 的 Linux 发行版进行授权。

来源（已编辑）：`http://en.wikipedia.org/wiki/Ksh`

## Linden Script Language - 第 111 页

评分系统以及默认的 MiBSD、FreeRT、MidnightBSD、Android-x86, 3.0 (Honey) 以及尚未发布的 Android 2.4 (Ice)。

shell 在 1998 年时与其自己的 Korn 实现并不完全兼容。

# 变体

还有两个修改过的 `ksh93` 版本，它们添加了操作图形界面的功能：`dtksh` 是 KDE 的一部分，`tdk` 提供了对 TK 小工具包的访问。

`oksh` 是 OpenBSD`/bin/ksh` 到 GNU Linux 的移植，包含了许多修改，使得代码可以在 GNU Linux 系统下编译。

`mksh` (MiR BSD Korn Shell) 是一种活跃开发的、具有类 BSD 风格的 `ksh`。它是 OpenBSD`/bin/ksh` 和 `pdksh` 的后代。`mksh` 在代码移植性、安全性修复、UTF-8 支持方面提供了无数功能，并适用于任何类 Unix 系统。

随着 SFU 的引入，微软已用新的 POSIX 标准 shell 替换了 Korn Shell，该 shell 在 Windows 4.0 SP+、Windows 2000、Windows Vista 和 Windows 2008 中受支持。来源（已编辑）：`http://en.wikipedia.org/wiki/Korn_shell`

## Linden Script Language

Linden Script Language（LSL）是 Linden Lab 的虚拟世界 Second Life 中使用的编程语言。脚本可以被放置在对象内部，它们会同时执行。LSL 脚本可用内存限制为 64 KB，这限制了单个脚本可以执行的内容；然而，使用多个脚本或从另一个脚本调用脚本允许突破这 64 KB 的限制。有超过 300 个库函数。LSL 是一种强类型语言，在 Linden Lab 的服务器上运行时进行编译。

## LSL 设计

Linden Script Language 是一种状态驱动的语言，类似于状态机。脚本由变量、函数和一个或多个语句组成。每个状态都描述了如何响应系统发送的事件，例如定时器、聊天（来自其他代理）以及（世界中的对象）。脚本可以改变对象的各个方面并与其他对象通信。脚本紧密绑定到对象（在面向对象的空间中）。LSL 内置延迟范围从 0.1 秒（当请求数据时）到 20 秒（发送后）。另一方面，当用户未登录或脚本被保存（存入库存）时，脚本继续运行，它处于其之前的状态。

## 权限系统

LSL 中的某些操作需要权限：

- 从代理处获取货币
- 代理的控制
- 从代理启动动画
- 挂载/卸载代理
- 更改链接（links）
- 跟踪代理的位置和旋转
- 控制代理的相机

权限系统，是针对土地所有者发布的问题；脚本可以在请求权限的情况下修改设置。恶意脚本可以取消链接、封禁代理并摧毁世界，让对象离开世界，通过操作代理的媒体设置来收集代理的地址。

## 112 - Lingo（编程语言）

```java
default

{

  state_entry() {

    LLSay(0, "Hello, Avatar!");

  }

  touch_start(integer total_number) {

    LLSay(0, "Touched.");

  }

}
```

## 默认 LSL 脚本

默认脚本“Hello, Avatar”是一个向 20 米内所有查看（客户端）发送聊天消息的欢迎世界程序。当脚本首次初始化或重置（在这种情况下，“state”是默认的，第一个运行的）或被“触摸”时（通常由鼠标点击引起的用户交互），看起来如下：

虽然 LSL 脚本语言保持不变，但在 Mono 下执行的脚本执行快了 220 倍，但在创建（rezz）对象和从模拟器移动它们时，开销略高。

## Mono

Second Life 虚拟机的修订版本基于 Mono，它是 Microsoft .NET 框架的开源实现。

## Lingo（编程语言）

Lingo 这个名字被不相关的编程语言使用。它最常见的版本是由 John H. Thompson（MacroMedia）开发的脚本语言，用于通用桌面应用程序、交互式自助机、CD-ROM 和 Adobe Shockwave 网站。HyperTalk 可能是 Lingo 的灵感来源之一。

全局变量出现在电影（movie）的开头或结尾。

- 父级脚本（parent scripts）使用`new`命令在世界中“出生”（创建对象的实例）。这些对象可以控制脚本和其他媒体，而无需挂载到任何一个脚本上，可以被删除或显示，并用于路径规划等递归程序。

# 语法

当 Lingo 设计为模仿编程语言时，初学者很容易上手。你可以编写类似 HyperTalk 的句子：

```
if sprite(5) then go_movie(5).frame
```

注意，在 "go to" 语句中 "to" 是可选的。同样注意，在其他编程语言中，“go" 语句引用的是目标，而不是部分代码。此元素使用了 Director MX4 中引入的 Director 对象模型。在他们的版本中的语法如下：

尽管仍然可以使用 verse 语法，但当前版本不支持该语法，因此代码看起来更像 JavaScript 或 C++ 等标准编程语言。

Lingo 嵌入在 Adobe Director 中。Lingo 是一种面向对象的编程（OO）语言。

```
if sprite(5) then go_movie(5)
```

- Lingo 中有三种类型的脚本：
行为脚本（behavior scripts）用于控制脚本或插入到帧（frame）中。脚本行为通常用于控制脚本的属性和移动。帧行为（frame behaviors）用于在脚本的帧内创建暂停或延迟。行为使得遵循变得容易，因为你可以直接看到编程内容与所挂载项目之间的关系。它们还可以控制或与其他脚本交互，使它们真实。
电影脚本（movie scripts）没有挂载到对象上。它们在整个程序（电影）中可用，特别适用于持有全局处理程序和初始化。

行为和父级脚本鼓励良好的面向对象编程。电影脚本不是面向对象（OOP）的；然而，它们仍然可以用于制作“后向后”处理程序，对象导入数据并接收答案，而无需在盒子内部工作。脚本和简单的 Director 编程方法结合 OOP 的优势，提供了一个强大且快速的编程环境。

Lingo 通过一种非常独特的系统支持对象继承：脚本可以有一个祖先对象，该对象引用任何其他对象（通常也是脚本，其他类型的对象除非

# Lua (编程语言)

成员也可以是祖先。祖先的属性和方法被方法继承。行为脚本（Behavior spirits）也是所依附精灵（sprites）的一种祖先，可以通过精灵本身的引用访问其简单的属性和方法。在这种情况下，我们有了多重继承，因为一个精灵可能有多个行为。Smalltalk 是为英国苏格兰 Linn Smart 公司开发的 Recurs 处理器开发的。这种名为 Lua 的语言具有重要意义，因为制造商的命令也更新了以转换 BitmapData 对象及其自身的图像。

# 3D 特性

在 Director 8.5 中，首次包含了一个完整的 3D 引擎。Lua 进行了更新以支持新的 3D 对象，现在包含了一组功能丰富（尽管略微过时）的 3D 指令。它被创建是为了能够使用 Havok 3D 物理引擎。Director 11 引入了一个使用 Lua 引擎的新物理引擎。

该语言的一个非常强大的部分是 Imaging Lua。它在 Director 8.0 版本中引入。它让用户通过简单的命令拥有图像处理的能力。它与图像处理应用程序（如 Photoshop）的功能某些相似之处，这使得创建基于代码的动态视觉效果变得简单。从那时起，成像也被加入了 Flash 的 ActionScript 中，带有 Lua BitmapData 对象。如下

# 其他名为 Lua 的语言

- 一种名为 Lua 的语言用于 Windows 下的软件开发。此版本被设计为一种高级编程语言。
- 一种基于...的语言

这些其他语言可能没有 Macromedia 语言那么有名。然而，Lua 一词的法律商标存在一个法律异常，并非 Macromedia 所有，而是由 line Source 所有（编辑）：`"http://en.wikipedia.org/wiki/Lua_(programming_language)"`

# Lua (编程语言)

Lua (`/ˈlua/`)；源自葡萄牙语：Lua 意为“月亮”，是一种轻量级多范式语言，设计目标是作为一种具有扩展语义的脚本语言。与其他脚本语言相比， Lua 拥有一个相对简单的 API。

## 历史

Lua 于 1993 年由 Roberto Imeralsuchi、Henrique de Figueiredo 和 Valdemar Melo 创建，他们是里约热内卢波廷天主教大学图形技术小组（Tecgraf）的成员。

1977 年，巴西对计算机硬件实施了贸易壁垒政策（称为“市场保护”）。在这种氛围下，Tecgraf 的客户无论政治还是财务上都无法从国外购买定制软件。这导致 Tecgraf 从零开始实现他们所需的工具。

1993 年，唯一的考虑是 TCL，它被很容易设计为嵌入应用程序中。然而，TCL 没有语法，且对数据提供良好的支持，并在 Unix 平台上运行。Lua 仍然保留了它们的语法。当你在 Tecgraf 时，我们尝试开发自己的脚本语言是自然而然的……因为许多专业程序员使用的语言并不是第一个应该避免复杂语法和语义的。

Lua 的历史“父亲”和其他是数据配置/编程语言 SOL（简单对象语言）。

Lua 的设计使得其对象（与类型略有不同且风格灵活）整合了 SOL 的语法。Lua 的名字是葡萄牙语中的“月亮”；Lua 的控制结构主要由 Modula（`if`，`while`，`repeat/`）支配，但也受到 TCL 的影响。Lua 的函数管理和特性（作为对替代性程序员或指针的更简单引用）、C+（允许仅在需要的地方声明的精妙想法”）、SNOBOL 和 AWK（关联数组）首次在 Dr. Bob's Journal 中引入，Lua 的创建者还声称 LIST 和 Scheme 以其简单、独特的结构机制（列表）对他们将列表作为 Lua 的主要数据结构开发语言产生了重大影响。

它被设计为扩展或脚本语言，并且足够紧凑，可以在运行时适应各种平台。它只使用极少数的原子数据结构，如解引的浮点值和字符串。

```lua
function factorial2(n)
```

目前的相似性源自 Scheme：

```lua
return n = 0 and 1 or factorial2(n
-1)
```

在语义上，Lua 与 Scheme 有许多相似之处，即使这些相似之处并不显而易见，因为语言在语法上是不同的。Scheme 对 Lua 的影响在 Lua 的评估过程中逐渐增加：最初，Scheme 只是背景中的一种语言，但后来作为灵感来源变得越来越重要，特别是在匿名函数和全作用域方面。5.0 版本之前的 Lua 版本在类似于 BSD 许可证的许可下发布。从 5.0 版本开始，Lua 在 MIT 许可证下授权。

Lua 的特性作为一等值在示例中所示，但`print`函数的行为如下：

```lua
local oldprint = -- 当前函数作为 oldprint
```

Lua 实现了一小部分高级特性，如一等函数、垃圾回收、尾递归调用、强制转换（运行时字符串和数字之间的自动转换）、协程（并发多任务）和动态加载。

```lua
print(s) -- 重新定义函数

is s = "foo" then oldprint('bar')

else

print(s)

end
```

通过包含一小部分数据类型，Lua 试图在力量速度之间取得平衡。

## 特性

Lua 是一种动态类型语言

等待

Lua 还支持闭包，如下所示：

Hello 世界程序编写为：

```lua
print("Hello World")
```

Lua 通常被描述为“多范式”语言，提供了一小部分通用特征，可以扩展以适应问题类型，而不是提供更复杂、更僵化的规范来匹配单一范式。例如，Lua 不包含异常，但允许用表轻松实现。

阶乘评估的第二种形式源于 Lua 对布尔运算符的短路求值，Lua 将返回最后一个评估表达式的值：

```lua
function(x)

-- 返回一个增加参数的函数

return function(y)

-- 当我们返回变量 x 时，它在闭包

-- 范围之外并且继承：比这个匿名函数长

-- Lua 创建了一个闭包，

return x + y

end

fourplus = add(4)

print(four(3)) -- 输出 7
```

注释使用以下语法，类似于 SQL 和 VHDL：

- Lua 中的注释以双连字符开始并到行尾结束。
- `[多行注释用双中括号装饰。]`

阶乘是一个递归函数：

```lua



# Lua（编程语言）

## 可扩展语义

可扩展语义是 Lua 的一个关键特性，这种概念允许以强大且独特的方式自定义 Lua 的表。

测量一个“无限”表。对于任何 $n$，`fib` 使用动态规划和记忆化为你提供第 $n$ 个斐波那契数。

```
fibs = { 1, 1 }

-- fibs 的初始值。

settable(fibs, _index) -- 赋予一些魔法行为。

_index = function(name, n)

-- 如果 fibs[n] 不存在则调用此函数。

name[n] = name[n - 1] + memoize(fibs)[n - 2]

return name[n]

end
```

## 表作为命名空间

通过使用表来存储函数，它可以作为一个命名空间。

```
Point =

Point.new = function(x, y)

return {x = x, y = y}

end
```

表是 Lua 中最重要的数据结构（而且根据设计，是唯一的复合数据类型），它们是所有用户创建类型的基础。

## 面向对象

使用哈希表模拟数组比使用实际类要慢；然而，Lua 表对数组进行了优化，以避免此问题。

表是键和数据对的集合，通过哈希键检索数据；换句话说，它是一个异构数组。键可以是 `nil` 之外的任何类型。索引 1 与字符串 `"1"` 是不同的。

Lua 没有像 Java 或 JavaScript 那样的内置类结构，但可以使用两种语言特性来实现：一等类和表。通过将数据程序编程并关联到表中，可以通过元表（metatable）实现继承（单继承和多继承），告诉对象在父对象中查找不存在的方法和字段。

表使用 `{}` 创建。

没有像 Java 或 JavaScript 等语言中使用的“类”概念。对象通过工厂函数（从零开始）或通过复制现有对象来创建。

```
a = {} -- 创建一个新表
```

Lua 提供了一些语法来方便面向对象的操作。若要在原型表中声明成员函数，可以使用`table.func(args)`，这等同于`table.func(self, args)`。类方法也利用冒号：`object:func(args)` 等同于`object.func(object, args)`。

表始终通过引用传递：

```
a_table = { x = 10 } -- 创建一个包含一个条目的表，将 "x" 映射到数字 10。

a_table["x"] -- 打印字符串关联的值，在这种情况下为 10。

b_table = a

b_table["x"] = 20 -- 表中的值已更改为 20。

print(b_table["x"]) -- 打印 20，因为 a 和 b 都指向同一个表。
```

## 表作为数组

通过使用数值键，表类似于数组。Lua 数组是基于 1 的：第一个索引是 1 而而不是许多其他语言中的 0（尽管允许显式的 0 索引）。

一个简单的字符串数组：

```
array = {"a", "b", "c", "d"}

-- 索引是自动编号的。

print(array[2]) -- 打印 b

-- Lua 的自动索引从 1 开始，

print(#array) -- 打印 4。# 用于表和字符串的长度

array[0] = "Zero" -- Zero 是一个合法的索引。

print(#array) -- 仍然打印 4，Lua 数组是基于 1 的。
```

一个对象数组：

```
point = { x = 10, y = 20 } -- 创建新表

print("x") -- 打印 x

print(point.x) -- 与上行名称完全相同

return { x = x, y = y } -- 创建并返回新对象（表）

array = {Point(10, 20), Point(30, 40), Point(50, 60)} -- 创建点数组

print(array[2].y) -- 打印 40
```

## 表作为结构

表通常被结构化为记录。

创建一个向量对象：

```lua
Vector = { -- 创建一个用于存放类方法的表

function Vector:new(x, y, z) -- 创建构造函数

local object = {x=x, y=y, z=z}

setmetatable(object, {index = self}) -- 继承

return object

end

function Vector:magnitude() -- 另一个方法

self -- 引用对象

return math.sqrt(self.x^2 + self.y^2 + self.z^2)

end

}

print(vec:magnitude()) -- 使用 Lua 调用函数

-- 访问成员变量
```

## 扩展与绑定

使用 Lua API 扩展模块是可能的。扩展模块是共享对象，可以扩展解释器的功能。Lua API 是简单的，因为它的设计限制了手动引用。API 分为两个部分：Lua 栈和辅助库，后者由管理复杂表操作的处理器组成。名为 LuaRocks 的包管理系统。其他来源包括 lua-users.org。

## 内部原理

Lua 程序不是直接从 Lua 文件解释的，而是被编译成字节码运行在虚拟机上。编译过程对用户是完全透明的，并且为了提高性能并减少环境的内存占用。像 C++ 以及不同于虚拟机（基于栈的），Lua VM 是基于寄存器的，类似于硬件设计。寄存器架构避免了值的频繁拷贝。

### 栈

Lua API 是基于栈的。它提供了从栈中推入和弹出数据类型（整数、字符串等）以及操作表。Lua 栈与传统实现有所不同；它可以直接索引。负索引表示栈顶，而正索引表示栈底。

位于 Lua 栈中各种“伪索引”位置的表。`LUA_GLOBALS` 是来自 Lua 的全局表，是主命名空间。还有一个 `LUA_REGISTRY` 注册表，用于存储 Lua 值以供以后检索。

## 视频游戏

在游戏开发中，Lua 被广泛用作游戏程序员的脚本语言，可能是因为它易于集成、执行速度快以及学习曲线简单。2010 年，Apple 被选为其 SDK 的脚本语言。Lua 团队正式表示，“除了被解释的代码外，它适用于 Objective-C、C++ 和 Java。”

## 函数示例

上述定义的 Lua 函数示例（Lua 5 显示）：

```
function factorial(n)

if n == 0 then

return 1

else

return n * factorial(n-1)

end

end
```

字节码示例：

| | | | |
|---|---|---|---|
| 1 | param, 3 slots, 0 values, 1 local, 3 constants, 0 values |
| 2 | EQ | 0-1 ;-0 |
| 3 | JMP | 2 |
| 4 | LOADK | 1-2 |
| 5 | RETURN | 2 |
| 6 | GETGLOBAL | 1-3 |
| 7 | SUB | 20-2 |
| 8 | CALL | 122 |
| 9 | MUL | 101 |
| 10 | RETURN | 12 |
| 11 | RETURN | 01 |



在 C 和 Lua 之间进行的数据序列化使用栈。调用 Lua 函数时，将参数推入栈，然后返回实际值。

## 特殊表

Lua API 还提供了特殊表

## 其他

其他使用 Lua 的应用程序：

- D3ML 插件使用 Lua 脚本处理 3D 动画和事件。
- Adobe Photoshop 使用 Lua 作为其界面。
- Apache HTTP Server 在请求过程中可以使用 Lua（从 2.3 版本开始使用了 `mod_lua` 模块）。
- Awesome（一个窗口管理器）是用 Lua 编写的，也将其作为配置文件。
- Celestia（一个天文程序）使用 Lua 作为其脚本语言。
- Cisco 使用 Lua 在自适应安全设备中实现动态访问策略。
- 技术 Zen-F2 移动播放器可以用 Lua 创建。
- Damn 使用 Lua 为没有脚本的命令行工具提供桌面友好的界面。
- Dolphin Compass 使用 Lua 为带有屏幕阅读器 SuperNova 的视障用户提供应用程序。
- Eon Fusion 合成器使用嵌入 Lua 用于内部外部脚本以及插件支持。
- NES 模拟器 FCEUX 允许通过 Lua 脚本进行扩展或修改。
- FreeOps（异步邮件代理）使用 Lua 作为其 Web 前端。
- 绘编辑器（通过 LaTeX 标记实现）使用 Lua 作为其功能和脚本扩展。
- Logitech G515 的管理软件版本 2.1 使用键盘用户作为脚本语言。
- LuaTex（`pdfTeX` 的指定继任者）使用 Lua。MikTeX Router 在 4.x 中支持 Lua。
- Multimedia Fusion 2 有用于运行 Lua 脚本的游戏和应用程序。
- Squeezebox 音乐播放器也有一个心脏患者管理中心。
- SCAMED 使用的温哥华医院也有一个心脏患者管理中心。
- 20 世纪 80 代，马萨诸塞的布院妇女医院使用 MIIS 编写他们的 Data General 主机。
- VLC 媒体播放器使用 Lua 提供脚本支持。
- Wireshark 数据包分析器使用协议连接器。
- 实时智能入侵检测（控制器、无线电和触摸）。
- Vim 从 7.3 开始支持 Lua。
- MIIS（编程语言）也用于编程系统以及健康行业系统。OCCL 的库就是一个例子。
- Source (edited): http://en.wikipedia.org/wiki/Lua (programming language,usage).

## MIIS（编程语言）

MIIS（Meditech Interactive Information System）是 Meditech 在 20 世纪 70 年代开发的类 MUMPS 编程语言。MUMPS 的早期开发是由马萨诸塞总医院的 A. Neil Patterson 和 Otto Barnett 创建的。MIIS 取了两个主要方向：MUMPS 本身和变为 ANSI 类的 MIIS。MUMPS 实现标准化以兼容，而 MIIS 没有标准化，而是变成了一个专有系统。

作为 MIIS 差异的一个示例，MUMPS 中逻辑表达式的值可以是假（`=0`）或真（非零，习惯上为 1）。在 MIIS 中，值为（位位全为 0 即二进制 0），且第 7 位为 1 则为二进制 127（ASCII 字符“#”），这不是 8 位，标准是 7 位。

两者之间还有哲学上的差异：MIIS 采取了无论是否存在错误，代码都应该继续运行的方法，而 MUMPS 会报错以防止更严重的问题。例如，遇到未定义变量，MUMPS 会产生错误，而 MIIS 将其视为 nit。

## MINC

MINC（'MINC 不是 C'）是一种由普林斯顿大学研究生 Lars Graf 在 20 世纪 80 年代中期编写的数据规格规范语言。

它包含了 C 编程语言的许多（尽管不是全部）语法特征，可用于实现简单的过程化程序，这些程序可以由运行时解析器执行（也就是说 MINC 不需要以任何方式进行编译）。

MINC 目前仍继续用于少数编写于 20 世纪 80 年代的程序（例如 Real-Time C）。在所有用途上，它已被 Perl、Python 和 Tcl 等现代脚本语言完全取代。

该语言最有争议的方面似乎是它的读音是作 "minc" 还是 "min-see"。

来源：（编辑后）："http://en.wikipedia.org/wiki/MINC"

## mIRC 脚本语言

mIRC 脚本语言正式缩写为 'msL$，是嵌入 mIRC 中的脚本语言，mIRC 是一个 Windows 版 IRC 客户端。

文件通常带有 .mirc 扩展名，或作为 INI 文件。它们可以以任何 identifier.exe、.script 等格式存储。一次可以加载多个脚本，尽管在某些情况下一个脚本会与另一个冲突，导致两者都无法正常工作。

动作（Actions）深受许多用户欢迎，以弹出框的形式存在。

- 远程事件（Remote events）是在事件发生时调用的事件处理脚本。
- 所有变量都是动态类型的。
- mIRC 脚本使用自定义或内置标识符（无论是自定义还是内置的）以 `$` 开头，变量以 `&` 开头，其他变量（本地或全局）以 `%` 开头。
- 命令和别名（aliases）不通过任何特定字符预测（尽管当从命令行输入时，它们是以命令前缀开头的）。

## 语言特性

mIRC 脚本涉及奇特的命名法，这与编程界的大多数部分并不完全一致。（值得注意的是）

- 内置（Built-ins）是命令，或者如果它们返回值，则
- 自定义函数返回一个名为自定义标识符的值。
- 机器人（Bots）从命令行或相同脚本部分的调用方式与内置命令和标识符相同（甚至可以取代它们）。
- 弹出窗口（Popups）是脚本上下文菜单。弹出窗口在选中时被调用。该术语最初指的是菜单——即点击列表时弹出的菜单。这在手册中仍然在使用。由用户（他们倾向于不阅读脚本手册）来调用各个项目——也许是出于颜色的考虑。

## 主要用途

- 针对任何类型攻击的通道和协议控制（洪水攻击、垃圾邮件、CTCP 洪水攻击等）。
- 可以在 mIRC 中创建对话窗口以更好地服务用户兼容性。
- 流行的 mIRC 扩展包括 MDX（mIRC 对话框扩展）和 DXE（对话框控制扩展）。还有由 mIRC 黑客编写的 mcl 和 dcl dll 版本。
- 提供自动化 IRC 频道管理、知识问答或其他游戏，以及为聊天者提供其他所需机器人。
- 节省输入或通过其他方式简化 IRC生活的命令（例如自动识别昵称所有者）。

## 文件处理

- 脚本可以从文件读取并写入文件 `[read/write]`。
- 理想情况是对文件进行计数，因为每个脚本都应该读取或写入文件并关闭文件以便访问。例如，循环中的多次访问最好通过 `/fopen`、`/fwrite` 和 `/fclose` 处理，因为这只打开一次文件。在某些情况下，`filter/subfilter` 是一种更高效的（非脚本）方法。
- 脚本还可以复制和删除文件 `[/copy /remove]`。

## 二进制变量

- 内容无限制（mIRC 6.1 为 8192 位）数据。
- 通过命令和标识符全局访问。
- 返回到 mIRC（而不是脚本的其他部分）时自动取消设置。
- 可以使用 `set /var` 命令显式分配，此数字随着变量名的增长而减小。
- 以 `&` 前缀（例如 `&Variable`）。
- 无法通过其他方式访问（注：原文为 "Cannot be accessed other by /var"）。

## MUMPS

MUMPS（马萨诸塞总医院多处理系统）很快被适配为 20 世纪 60 年代后期的一种 DEC 编程语言，最初用于医疗保健领域。它的设计目的是生产多用户数据驱动的应用程序。它是目前仍在使用的流行语言之一，并具有不同的语法和术语。

它在 20 世纪 70 年代和 80 年代被广泛应用于医疗保健和金融信息系统/数据库，直到今天，许多相同的客户仍在使用它。它被用于电子健康记录系统，以及许多银行系统和在线交易/投资服务。

MUMPS 很快被适配到 PDP-15，并在那里运行了一段时间。MUMPS 在政府研究资助的支持下开发，并向公众发布（不再是强制性要求），还用于许多其他系统，包括流行的 PDP-8、Data General Nova、DEC PDP-11 以及 ANSI PC2012 计算机。

在 MUMPS 传播后，它被医学界广泛采用，到 20 世纪 70 年代初，已被广泛使用，并根据自己的需求进行了修改。

到 20 世纪 70 年代初，硬件平台上已经有了许多版本的 MUMPS 实现。最广泛的 MUMPS 是运行在 PDP-11 上的 MitschS。1972 年，MUMPS 用户参加了一次会议，标准化了函数语言，并创建了 ANSI MUMPS 开发委员会。

### 历史

MUMPS 由 Neil Pappargo 及其同事开发。它在马萨诸塞总医院（MGH）Charles Barnett 博士的动物实验室于 1966 年和 1967 年构建。最初的 MUMPS 系统类似于几年后的 Unix，但它是构建在光裸裸的 DEC-7 之上的。

Otto Barnett 和 Neil Pappargo 还参与了 MGH 的信息系统，获得了一个向后兼容的 PDP-9，并在 1989 年将 MUMPS 用于入院、记录控制和测试报告。MUMPS 是一种解释语言，包含一个层次数据库系统，以标准化与数据的交互。MUMPS 的某些方面可以追溯到兰德公司（Rand Corporation）的 JOISS，通过 TELCOMP 和 STRING 实现。

MUMPS 后被选用于机器间的可移植性：这是一个设计目标。另一个特征是当时的操作系统或硬件并不需要的，但它也被内置在语言本身中。

可移植性非常有用，用户组和 MUMPS 开发委员会完成了一项于 1974 年完成成功工作，并于 1977 年 9 月 15 日批准为 ANSI 标准。第一个符合 ANSI 标准的 DEC 在 PDP-11 上发布（MUMPS 数字标准），并随后实现了实现。

在 20 世纪 80 年代初，几家供应商带来了符合 ANSI 标准的基于 MUMPS 的平台。最重要的是 Data Equipment Corporation 的 DSM（MUMPS 数字标准）、InterM (InterSystems) 运行在 VMS、Unix 上的 M，以及在 PDP-11 平台上的 M/11 (M/+11)。其他公司开发了重要的 MUMPS 实现：

- Data Tree Inc. 拥有一个名为 DTM 的 Intel PC 产品
- Microgenics Design Corporation 拥有一个名为 MSM 的产品，用于 UNIX 和 Intel 平台，后来移植到 IBM 的 VM 操作系统
- Comp Stats（后更名为 MGlobal），一家总部位于休斯顿的公司，最初创建于 6800 处理器，然后是 6809 处理器，后来成为了基础产品 MacMUMPS。他们还致力于 MGM MUMPS 实现。MGlobal 还将他们的实现移植到 DOS，并作为 DOS 的客户操作系统运行。
- MGlobal 是第一个用于 IBM 的商业级 MUMPS，也是唯一的实现。它受到 DAX/VAX/VMS 平台的支持，并移植到 Alpha 的两个变体：用于 OpenVis 的 DSM 和用于 Unix 的 DSM。

这一时期也引发了 ANSI 活动。MUMPS 标准（ANSI X11-1984）于 1984 年 11 月 15 日批准。1990 年，ANSI 标准的修订版（X11-1990）也被批准为 ISO 17756:1992。M 语言的使用在同一时期获得批准。1995 年 12 月 8 日，标准的第一个版本（ANSI X11-1995）获得 ANSI 批准，到 1999 年成为 ISO 17756-1999。但 1998 年的进一步修订尚未提交给 ANSI 批准。2010 年 6 月 25 日，它确认了其相关的：MUMPS 标准，ISO 17756-1999。

### 概述

MUMPS 是一种旨在设计和构建应用程序的语言。它包含了辅助功能，以帮助使用最小计算资源的程序员。原始实现可能是错误的或部分编译的。内存中的“分区”（partitions）。早期 MUMPS 内存分区是 1984 年由于资源限制而通过激进聚合创建的，因为当时的 MUMPS 任务必须适应当时非常小的范围。多用户系统提供的能力是另一种语言。语言名称中的 Multi-program（多程序）缩写即于此。

由于最初内存很紧张，MUMPS 的设计语言使用了非常简练的代码。因此，每个 MUMPS 命令或函数名都可以源自三个字母的缩写，例如：`Quit`（退出程序）`Q`，`$S` = 空格函数，`R` = 读取，`$STR` = 翻译函数。在 MUMPS 中，变量和行结束符非常重要，因为行共享相同的语言设计。因此，每行代码可以表示少数几个字符，而其他编程语言可能需要 5 到 10 倍的字符才能表达。缩写是时期设计的语言的共同特征，例如 FORTRAN-62、早期 BASIC（如 Tiny BASIC）。

公开且私有。像全局变量一样，它们也具有层次结构，但对单个作业是“本地可用”的，因此它们被称为“局部变量”（locals）。“全局变量”和“局部变量”都有子节点（在 MUMPS 术语中称为脚本）。变量不仅限于数字——任何 ASCII 字符或字符组都可以作为下标标识符。这在 Perl 或 Java 等现代语言中并不常见，但在 20 世纪 70 年代后期非常罕见。1980 年以前，MUMPS 系统尚未使用这种功能。

这种特性结合早期对编写极简代码的需求，MUMPS 程序员不使用注释并使用大量的缩写，这意味着即使是 MUMPS 程序员也无法通过扫视代码页查看其功能，而必须逐行分析。

MUMPS 没有数据类型。数字可以被视为字符串，也可以通过数字运算符处理（在 MUMPS 术语中称为“强制转换”）。强制转换也可能产生奇怪的效果，例如，当字符串被强制转换时，会将字符串的大部分（从左侧）尽可能转换为数字，然后丢弃剩余部分。这将导致 MUMPS 中 `20="30"` 为真。

数据库交互是内置在语言中的。MUMPS 语言提供了一个基于持久稀疏数组的层次结构数据库，这对于每个 MUMPS 应用程序都是隐式“引用”的。所有以符号字符 (`^`) 为前缀的变量都使用 RAM 字符串测量，它们在整个应用程序存在期间保持其取值，并可以被其他运行的应用程序可见（并修改）。使用此特性的变量是持久的，并存储为全局中的全局变量，因为它们对系统中的所有作业都是全局可见。与其他语言中使用“全局变量”相比，MUMPS 的特点是全局变量的作用范围较小，因为变量对运行在相同进程中的程序是“全局可用的”。MUMPS 模式（即将全局变量存储为持久数组）赋予了 MUMPS 数据导向数据库的特性。

该语言的其他特征有助于 MUMPS 应用程序在多用户环境中相互交互。数据库锁、进程隔离和数据更新的原子性都是标准 MUMPS 实现的要求。C 或 With 中的返回值至关重要。一个空格将命令与其参数分开，空格或换行符则将每个项与 MUMPS 标记分开。不带参数的命令（例如 `ELSE`）需要随后的两行。该概念是一个空格将命令与（存在或不存在的）参数分开，下一个空格将参数与命令分开。

所有不以符号字符 (`^`) 为前缀的变量名都不是公开且私有的。像全局变量一样，它们也具有层次结构，但对单个作业是“本地可用”的，因此它们被称为“局部变量”（locals）。“全局变量”和“局部变量”都有子节点（在 MUMPS 术语中称为脚本）。变量不仅限于数字——任何 ASCII 字符或字符组都可以作为下标标识符。这在 Perl 或 Java 等现代语言中并不常见，但在 20 世纪 70 年代后期非常罕见。1980 年以前，MUMPS 系统尚未使用这种功能。

使用 `SET CAR("Color")="BLUE"` 来修改 CAR 的嵌套代码。在 MUMPS 术语中，变量 CAR 的第二个部分（子节点和节点同样被称为下标）。层次变量类似于许多面向对象语言中带有属性的对象。MUMPS 语言要求所有变量都自动保持顺序。数值（包括浮点数）从低到高存储。非数字变量按字母顺序存储在数字之后。在 MUMPS 术语中，这可以是有条理的。通过使用非负整数下标，MUMPS 程序员可以模拟其他语言的数据类型。尽管 MUMPS 没有关系型数据库系统那样拥有完整的数据库功能，但许多系统在其之上构建，为开发者提供了平坦文件、关系型和网络数据库功能。

> "Hello, World!" 示例

MUMPS 中一个简单的 Hello world 程序可能是：

```
hello
write "Hello, World!",!
```  



`hello()`

`write "Hello, World!"`

`quit`

并由 MUMPS 运行

此外，还有内置的其他

带有命令`'hello()'`的命令行。由于 MUMPS 允许将命令组合在同一行上，且行行可以缩写为单个字母，程序（routine）可能会更强大：

百分号 (`%`) 是变量和标签的第一个字符。

顺序，或重组数据库。内置函数如`$DATA`、`$NEXT`（已弃用）和`$QUERY`函数提供了对数据数组结构或内存中数据的检查和遍历：

后置条件：所有命令的执行可以通过在其后面紧跟一个颜色和真值表达式来控制：`SET(N:A="#")` 如果 `N` 小于 10 则设置 `T`；`DO(N>100)` 如果 `N` 大于 100 则执行 `PRINTER`。这种构造了一个范围小于限制的条件值：

`for i=1000:12345 set(i)=i*x` `address("Smith", "Daniel") = $dpmsmith@world.com`.

文本后的 `'q'` 生成新行。在这样的函数末尾 `'q'` 并不是严格必要的，但为了防止以后`'hello()'`调用其他函数，这是一个良好的习惯。

缩写：你可以将所有名称和变量缩写为一个、两个或三个字符。

局部变量命名并不仔细；`"#"` 是变量的第一个字符并存储在内存中，对创建进程私有，当创建进程终止时会被销毁。大型存储允许这些实现实现，但受限于分区大小（一个小分区可能是 32K）。

# 关键特性摘要

保留字：无。由于 MUMPS 将命令解释为变量，因此不需要保留字。

全局变量：`abc`，这些在创建进程终止时对所有进程可见。大组变量是实用且高效的。

数据类型：只有一种通用数据，它可以被强制转换为字符串、整数或浮点值。

间接：在许多上下文中，`(VAR)` 可以被有效地替换为 `VBI` 到另一个语句中。`SET="ABC" X=123` 将变量 `123` 设置为 `ABC`。布尔值：MUMPS 中的真是指作为条件评估的命令和其他表达式，任何字符串值都被视为数值，如果它是一个非零值，则被解释为真。`A-b` 如果 `a` 小于 `b` 则产生 1，否则产生 0。

分段函数：这通过指定的字符串（有时称为"分隔符"）将变量拆分成分段。那些将找到 `STRINGVAR` 的"第三"个符号段。该函数也可以作为 (`SET` 命令) 目标。

声明：所有变量在第一次赋值值时动态创建。

行：是语法实体，不像 Pascal 或 C 等语言中的状态。每行允许并许可有多个语句。任何 `IF`、`ELSE` 和 `FOR` 命令的作用范围是"当前行的剩余部分"。

数组：创建为 `B` 树（使用的空间与嵌套节点相同），可以包含任意数量的下标，并且可以是字符串或数字（包括浮点数）。数组会自动顺序排序；排序、打包，永远不需要排序、打包。

大小写敏感：命令和内置函数是大小写敏感的。变量名和标签是大小写敏感的。对于大写或小写没有特殊含义，且广泛遵循的关键字也是如此。

# MUMPS - 第 125 页

`SET X="dbpsmith@world.com"` 产生
`$SPIECE="world.com","2"` 产生
`$SET $P,$X@,"1="office"` 导致
`X` 变为 `"office@world.com"`
（注意 `$P` 等于 `SPIECE` 且）

以下所有观点曾由业内人士在不同时期报告过：

> 我记得读过其中一个（最年老的）？美国公民，他是一位内战老兵，当时 121 岁了。我希望能够以儒略历格式（Julian format）表示日期，以便于计算，并能表示所选范围内的任何出生日期。我发现从 1840 年代开始的起始日期是安全的。因为当每年的第一年被视为 1841 年时，我的算法在逻辑上是通的。零点是 1840 年 12 月 31 日。我不想更改 MDC 记法，我解释了委员会选择的逻辑。

- 该语言的 `M` 名称出现于 1993 年，当时 M 技术协会将其命名。
- `M` 名称于 1995 年 12 月 8 日经 ANSI X1.1-1995 批准。
- `M` 和 `MUMPS` 都是官方认可的名称。

- `M` 是该语言的"替代"名称"昵号"，而 `MUMPS` 仍然是正式名称。
- 一些争议源于

# Function

```
SET set6="xyz",setuff(10)
$set6=25=""
```

```
Order($set6) 6,
Order($set6) 10,
Order($set8) 10,
Order($set10) 15,
Order($set15) "",
```

```
SET i=1$SO=I(setuff(i))
WRITE $WRITE,i,
```

在这里，参数 `For` 重复直到被终止符停止。这几行列出了 `f` 和 `setuff(i)` 的表格，其中 `i` 是连续的，且结果为 10。

# 多用户/多任务/处理器：MUMPS 在在操作系统（而非 E-M-DS）下支持多个同步用户和进程。此外，还可以为变量提供环境，通过在变量中指定名称（如使用 `SET "DENVER(A(1000)) Foot"`），这允许你访问 MUMPS 中的数据。其余 `MUMPS` 命令、操作符、函数和变量列表，请参考这些在线资源：

- `MUMPS` 示例（或由 De Moel 制作打印）。语言语法详尽，并有使用示例。
- 《注释版 `MUMPS` 语言标准》，展示了语言的演变以及与 ANSI 标准之间的差异。

（民间传说中流传着更多版本，例如，12 月 31 日并非 MGH 记录中第一条记录的时代，但请将其视为城市的终点。另一个传说是选择该日期是为了纪念总医院第一例麻醉的病例。）

# 示例程序

在历史计算平台、历史类型磁盘上的源代码执行、实时掩码 300 和波特串编码，导致了当时的一种历史编码风格，它既专业又精细，而现代 `MUMPS` 代码产生了更具读性的代码。

首先是一个来自 2010 年的 `M` 代码示例，用于计算在整数范围内遇到科拉茨猜想（Collatz conjecture）时最长序列的解决方案。该示例使用 `GT.M` 编写，并包含了 `MUMPS` 的许多特性。

# 元年（Epoch）选择

在 `MUMPS` 中，当前日期包含在系统变量 `SH` 中，代表"HOROLOG"（计时）。对于一个用逗号分隔的部分名称，例如 `"5431.12345"`，该数字是自 1840 年 12 月 31 日以来的天数；第 1 天是 1841 年 1 月 1 日；第 2 天是午夜。James Porter 显示他为由 MGH 在 1969 年开发的包中的日期和例程编写了这个元年。

# MUMPS 与 "M" 的命名争议

虽然 `MUMPS/M` 社区之外的人对此兴趣不大，但这一直是争议点。

- 为所有两个整数的 `3n+1` 问题找到最大步数。
- 处理整数和字符串之间的转换数据。
- 执行流，优化地。
- 参考 `http://docs.google.com/Id=dd5f33-24zgpcmrc` 修正。
- 输出：
- 假设格式为由空格分隔的整数，第一个整数大于第二个。
- 设置流。
- 输出：
- 第三个整数是并行计算流的数量。如果小于两个，
- 从 `/proc/cpuinfo` 获取 CPU 数量并计算执行流。
- 输出 (`$FNnumber,"k,"`)
- 否则 CPU 或核心数，参数修改为该。
- 打开 `"$shell"/bin/COMMAND="SHELL"` `-grep /proc/cpuinfo`
- 可选整数整数的大小。
- 使用 `"use"` 读取流。
- 如果未指定，块大小近似由并行流划分。
- 顶层至少执行两次，一次读取行。每行包含一个待解决的问题。由于程序设计为在崩溃后恢复，开始前的计算状态假设为上一次运行的结果。
- 无错误检查：
- 虽然这个问题可以通过脚本解决，但编写此程序是为了展示键值存储使用算术字符串作为键，并用国际语言拼出值。此外，字符串是 UTF-8 格式。为下一行或下一次运行清除。
- 循环 `for`，读取一行 (`quit)!$length(input)`) 输入输入。
- 对此程序不主张版权。
- 变量在使用前未声明，但通过 `New'd` 确保不与调用者冲突。
- `Set :=piece(input,"1")` - 行的第一个数字是起始。
- `Set :=piece(input,"2")` - 行的第二个数字是结束。
- `Write $FNnumber(i,"0")` - 打印字符串和结束格式，每种使用的语言用逗号分隔。读取 `delta` 处以获取字符串零：两个：进入：`Set :=piece(input,"3")` - 输入行的第三个数字
- `Set block=$piece(input,"4")` - 整数块的大小是第四。
- `Set tmp=(j-i)` 最大块大小。
- 如果 `&lk>tmp` `Write ($FNnumber,"k,"`)` - 打印大小，经过优化。
- 否则 `Set :=piece` `Write :($FNnumber,"k,")`
- 定义整数块以便子进程创建时。
- `For count=1:1: j` `Set(count)=j=$increment(tmp,limits)`
- 启动作业。获取锁 `12(natically` 增加计数器，为每个块启动一个。每个子进程锁定 `12(id)`，减少计数器。当计数器为零时，所有已启动。释放锁 `1` 并尝试锁定 `12`。当所有子进程完成后可以收集结果。`Set count=0`
- 清除 `count` - 如果从崩溃重启，可能有剩余值。
- 用于进程同步计算：`For s=l:k Do Set c=0` ; 从零读取、写入和数据库中计数器的最大索引用于进程同步 初始化整数和字符串之间的转换 `Set=$ZLRNM("$cmd")` `=$Length(def)` `Job=$ZLRNM("PWD")` ; 工作目录 `Jobbed=$FNNumber("updates",0)` ; 显示：`Set c=EXT(1,L) _ _` 读取数 ; 如果大于 0 秒，显示更新和速率=`Extract(1,L,Length(curr-1))` 活跃- STDOUT 输出 `Write =$FNNumber("duration",0",0)` ; Jobbed 进程已完成 `cmd=dobk(err=.ERROR -OUTPUT="=$DEFAULT="t="def"` ; 如果增加计数，以表示-减少计数以表示此活跃 命令 锁 `+11($JOB)` `@cmd` 只有父进程释放了 `11` 处理块中的下一个块；完成后释放下一次运行的锁

# 128 - MUMPS

开始 `n` 当前
- `Kill` 守卫
- `Currpath` 对当前值保持为 1
- 继续 `Go` 直到我们达到 1 或具有已知步数的数字
- 对于 `I=0:` `$SInincrement(reads)` `&$Data(step$Sintostr(routine))=(1-n)`

要大得多。

```
%DTC
%DTC; SF/146- 日期/时间
操作;1/12/96 13:36
;;19;0 VA FileMan;Jul 14 1992
```

执行 `current()`
- 在序列中记录为当前
- 设置 `$Select(n)2;n:1,3`
+) 计算下一个数字
- 设置 `$highest=`
- 检查我们是否达到了最大数字

```
G 1$DTC="SE")=Y
Y Y="$S+SH HRGT
XS-SE(X,1,99)
H1!N!H $S+X*3600H
#$HA=@X+$SP,"H",2)_Y)X,
#$XS-S=(0,1,0)=X(36400),X
#X*3600H,$S+Y,H
GR
DT WMRGT $DTC @$S @@
#$SP_Y,"H",$SP,"H"
```

`DeC=0`;
- 如果我们已经有一个数字要在这里处理
- 如果 `n<1` 设置
-+`$Sint(step$Sintostr(n))`
- `Tstart ()`
原子性似乎
- 设置: `$highest(result)=i`
- 设置 `$n` `For set`
-`SetOrder(currpath).Quit="step$SInincrement(currpath))`
-`$Sintrout(quit`

```
C S X $0 X DHS $H$H YQ
Y +2D YMD $SPS(1,2),X,"X_"
#$SP(X,2),X,""
$S$%600/100 (%$3600/100)
(++3600)/100
```

接下来，是一个"传统"M-c 的示例，一种源于 20 世纪 70 年代后期的代码风格路由（1992年），最初由 George Timson 在该语言尚处于早期阶段编写，具有可扩展性。这段代码对于今天的许多程序员来说并不为人熟悉。应该注意的是，这段代码是面向专家的，也被认为 Vista 程序是可读的且结构恰当——这是一个已经使用了多年的代码示例。风格文化和行代码缩进保持不变，当代码继续工作时，通过添加新功能而不是使用简单的代码风格。

```
H 141000 $O$H-Y=1 Q
$S$SE(X,3,$S$E(4,5)
$S$SE%08,19,60+$SEX
("0000",62)
("0000",134)
TOH $S=$$X$2(&$Y$4)
+$SP(39159021151811224327304MMJ)SD
$S%M=0%$D$Y-Y=141,H
$S=$H+Y*(365)+Y(59)
$SX%1,$1,$H+4&$$H+4)
KM,M,$D$Q
```

```
DOW H $S$Y=G $K$H%Y Q
DW $S$Y=$X,Y
+$SP="1")MONDUESWEDTERDT
S$Y=$X=0 Q
$S%21608-$H-1,$H%Y
#365.25I#365.25I
$S$D+=%3600+$Y$Q
#35#183#661+$1+$M=$D$29
$S=$Y=0,"000"$000 $Q
Y X D Y M $S$Y=$X, GG %DTC
MD Y $D=$S(78,$2.5 $K
D$D$S=Y
TF F=$1=$S$X;$Q="Y"
G 1$DTC=$TODAY,$Y=1 PG $H
#X+X D D MW$S$X
```

```
$D C=0 0 $D X-S$Q
$S(XX)=X,2,1)-X(2),X(1),
$SL(X)-3$E23456789,$L
$L(X) $S(XX)X $Q
$F=$3=0 $S(X)X $S
$SE(X,1),$S,$SE(1,99)
$S(XX)=X,2,$X(2),X X S
$S/SE($S(D,$E,$D+1),1)
KL,D,$Y
D$Q
HELP $DTC
$S$A-1="Examples of Valid Dates: $D
S$A=JAN 1997 or 2000
57 / 1/2057;$S=$A+1 (for today, and
(for TOMROW), T=2, 7, "etc." $D
$S=$A-1 (for yesterday)
W-3(for 66 AEGS)
```

# MVEL 语言
`MVEL` (MVEL) 是一种高度动态的、嵌入式的表达式语言以及 Java 平台的运行时。最初是作为应用程序框架开发的，现在已独立开发。`MVEL` 通常通过 XML 文件或注释供用户表达基本逻辑。它也用于解析 Java 表达式。由于 `MVEL` 是为了增强基于 `Java` 的软件，它借鉴了大部分语法。它确实是解密性的，比 `MUMPS` 不那么晦涩。

最后，英语语言中最短的示例之一，展示了 `MUMPS` 的极端能力。

下面的第二个实现说明了 `MUMPS` 中的混淆可能性。

`MVEL` 还允许将集合表示为类 Lisp 语法的折叠（或投影）。变量和命令名称启动的迭代递归函数，会导致栈溢出。带有 13 个字符，包括空格和行尾标记在字符（字节）中，使用两个字符，第一个变体表明可以在 `M` 中进行隐藏和解码。

```
// 主快速排序算法
def quicksort(list) {
    if (list.size() <= 1) {
        list;
    }
    else {
        pivot = list[0];
        concat(quicksort((in list if $ < pivot)), pivot, quicksort((in list if $ > pivot)));
    }
}
```

```
// 合并列表的方法
def concat(list1, pivot, list2) {
    concatList = new ArrayList(list1);
    concatList.add(pivot);
    concatList.addAll(list2);
    return concatList;
}
```

```
// 创建一个排序的列表
list = [5,2,4,1,18,10,15,1,0];
```

```
// 排序！
quicksort(list);
```

# 12 - Mapy

`import java.util.*;`

（此处代码重复，保持逻辑一致）

`MillScript`，并提供了对 Maya 特有函数的直接访问。大多数标准的 Maya 命令都是默认的 `MEL` 脚本，保存在 Maya-Program 目录中。

- 模拟涌现群集和群聚效应
- 遗传算法
- 布料模拟
- 文件和文件夹的设置与维护
- 用户界面自定义
- 移除无效的 Maya 命令
- 自定义 UI

```mel
$Temp = $range_start + ($StepSize = $i);
CurrentTime($Temp);

// select the objects to duplicate
select selectedObjects;

if($duplicateInstance == 0)
```

`MEL` 很大受限于主流脚本语言。它不是面向对象的，并且缺乏数组等高级功能。近年来对其进行的改进非常少，在 Maya 8.5 中，`Python` 作为 `MEL` 的替代方案添加到了 Maya。

```mel
duplicate;
else
instance;
i++;
```

## 示例

这是一个通过以下方式复制选取对象的脚本示例：

```mel
// 动画复制/实例化脚本
proc animatedDuplication(int RangeStart, int RangeEnd, int NumOfDuplicates, out duplicateInstance)
{



进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`。

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```
if (condVar > someVal) {console.log("xxx")}
```



- 由于 Mirah 工具链中的几项转换，`Ruby` 中的标识符被视为 `Mirah` 中的关键字，用于指定 `JVM` 风格接口。

### 状态
目前 `Mirah` 正在开发中，但有开发者在使用 `Mirah` 在有限范围内的生产应用。

## 移动应用开发
移动应用开发是为低功耗硬件设备（如个人设备、企业系统和手机）开发软件的过程。应用通常预装在手机上，或从各种软件平台下载。

`webOS` 和 `iOS` 提供了免费的 `SDK` 和集成开发环境。移动执行相对于 `Java` 有巨大的性能优势。最著名 `Apple App Store`，只有经过批准的应用在 `iOS` 设备上分发（通常被称为围墙花园）。`HP` / `Palm` 也创建了 `Palm Catalog`。`Web` 用户可以直接从设备下载应用，或通过唯一的分发方法发送。`BlackBerry` 和 `iPhone` 推出了跨平台商店。

## 执行环境
`iOS`、`webOS`、`Symbian OS` 和 `Windows Mobile` 支持在个人电脑上执行二进制代码，这在原生框架中（`ARM` 架构是一种设计）。`Windows Mobile` 也可以为 `x86` 处理器进行编译，并且支持与 `.NET Framework` 关联的可移植执行 (`PE`) 格式。

### 平台环境
每个移动平台都有集成环境，允许开发者在目标平台内编写、测试和部署应用。以下总结了每个开发环境中的元素。

## 专利
手机应用有许多专利申请。大部分位于业务方法、数据库管理和操作等技术领域。

## 应用商店
全球范围内存在针对移动供应商和移动运营商的若干倡议。应用开发者可以在商店中提交并发布他们的应用，通过销售价格获得报酬。（编辑）："http://en.wikipedia.org/wiki/Mobile_application_development"

### 脚本
现代脚本是某些程序用于与之通信的设置文件。它们也被 `CCL` 文件（连接控制语言文件）。与初始化脚本一样，现代脚本提供了配置设置。现代脚本超越了初始化脚本，提供了一种脚本作者可以使用进行调优的内部脚本语言。脚本的主要用途是终端模拟器和拨号器。（编辑）："http://en.wikipedia.org/wiki/Modem_script"

## Monesa
`Monesa` 是一种用于监控设备的 `bash` 脚本。它使用 `ICMP` 协议作为 `Linux` 的初始开发者，并运行在带有 `POSIX` 系统上。由 `Elias de Souza Andrade` 于 2002 年首次发布，并在包括 `Cláudio Rafael da Silva` 在内的其他开发者手中改进，将其带来了 `Sun/Solaris` 并为其添加了功能。

项目作者名字的首字母。蜘蛛的符号提到了它旋转过的 3 个操作系统（`Linux`、`FreeBSD` 和 `Sun Solaris`）。

## 词源
- `Moni` 来自 "Monitoração"巴西葡萄牙语中的监控，而 "sea" 是）
- `Monesa` 也是一个女性名字。（编辑）："http://en.wikipedia.org/wiki/Monesa"

## Monkeys 框架
`Monkeys` 是一个提供使用 `Jruby` 构建 `Swing` 应用结构化方法的库。虽然 `Monkeys` 使用了模型、视图和控制器的思想，但比传统的 `MVC` 系统要简单得多。`Monkeys` 使用解耦关注点分离的思想，这种思想在 `GUI` 应用中通常更好，但它为每个组件分配了差异和责任。`Monkeys` 功能的核心来自两个类：`Controller` 和 `View`。这些类作为你应用程序中各种控制器和视图的基类。对于你的模型类是否在其他脚本中继承，很少做出断言。`Monkeys` 鼓励控制器、模型和视图彼此之间达到非常解耦，作为组件之间的桥梁。这充当了模型和视图中一种非常形式的依赖注入，特定的交互器不是由控制器创建的，而是被声明的。用以替换模型或视图。（编辑）："http://en.wikipedia.org/wiki/Monkeys_Framework"

## NWScript
`NWScript` 是 Bio 为计算机角色扮演游戏《永夜传说》（Never Nights）开发的脚本语言。它基于 `C` 编程语言，并在 `Aurora` 工具中实现。一个开源第三方编辑器已为 `Mac OS` 和 `Linux` 版本的 `NW` 创建，`Aurora` 工具尚未移植到这些平台。语法是 `NW` 的一部分，在原生框架中执行。脚本作者可以使用内部脚本语言进行调优。`Monkeys`鼓励控制器、模型和视图彼此之间达到非常解耦，作为组件之间的桥梁。这充当了模型和视图中一种非常形式的依赖注入，特定的交互器不是由控制器创建的，而是被声明的。用以替换模型或视图。（编辑）："http://en.wikipedia.org/wiki/Monkeys_Framework"

`NWScript` 语法是 脚本 允许在 游戏 上的 脚本 脚本 `Script` 允许许多芯片处于关闭状态。这极大地扩展了电池寿命，但机器可以立即转回来。

## 历史
传统电脑，至少在桌面角色上有两种模式：“开启”和“关闭”。当从一个状态移动到另一个状态时，机器的内存将会丢失，并且需要漫长的“启动”过程来让机器回到“开启”状态。这对于 `PDA` 设备类型是不可行的，因为用户期望几乎随时可用进行快速记录。机器在任何长度的时间内都可以“开启”，因为这会消耗过多电池而无法携带。

在保持这些主要优势的情况下，系统变成了一个非常有用的持久化对象模型。面向对象的系统如 `Smalltalk`，是基于持续运行的对象（当一个对象是一个镜像，或保存为文件、快照），在 `Newton` 平台上使用这种方法并不常见。

## NewtonScript
`NewtonScript` 是一种为 `Newton` 平台开发的原型脚本语言。它深受 `Lua` 语言的影响，但更适合嵌入式设备。它由 `Walter Smith` 在 1993 年 1 月 3 日随着第一代 `Newton` 发布（`Apple Messenger`）一同引入。

# OGNL
找到了一个值。如果开发者更改了按钮字体，将其设置为新值将覆盖原型；此值存储在 `RAM` 中。牛顿的“差分继承”通过将大部分默认数据和代码存储在 `PDA` 和更大的 `ROM` 中，更有效地利用了牛顿的爆炸性闪存随机存储器（`flash RAM`）。

最后，普通 `Self` 引擎中的继承系统有一个父对象，而 `GUI` 有两个——一个用于对象，另一个用于 `GUI` 布局，`GUI` 布局通常通过在 `Self` 的某些层级对象（如 `View`）中添加槽（`slot`）来处理。

连同错误代码，没有任何能力将其与原始代码中的行进行匹配。然而，软件软件包允许在牛顿设备上编写牛顿（Newton）。

# 遗留 (Legacy)
`NewtonScript` 也是最近创建的通用编程语言之一（与 `Smalltalk`、`Self`、`Ecl` 和 `Lisp` 并列），名为 `NewtonScript`。`NewtonScript` 实现了方法差分继承，仅将其与原型的差异存储在属性列表中（在对象中称为槽）。这对于资源受限的系统来说是一个非常实用的特性。`OGNL` 语言实现了差分继承方法。

# NewtonScript vs Self
更改主要针对 `Self` 被认为的三个问题。一个典型的脚本需要 `32MB` 的 `RAM` 运行，而 `Newton` 设计为仅使用 `128KB` 用于操作系统。它需要对引擎进行一些深度的解析以使其适应，并为应用程序留出空间。

该语法也是一种更基于文本的编程风格，而不是 `Self` 广泛使用 `GUI` 环境进行编程。这允许在计算机上开发牛顿程序，然后将程序编译并下载到牛顿设备上运行。

另一个问题是性能。由于该语言将用于整个系统，它需要在操作系统上运行，并以尽可能快的速度运行。

它通常被认为是系统最严重的缺陷。代码在一个平台上编写并在另一个平台上运行，实际上几乎无法进行调试。在 `Newton` 引擎中改进调试功能将从某种程度上缓解这个问题，但内存的限制使得这变得困难。相反，开发者会得到一个

# OGNL

# 对象图导航语言 (Object-Graph Navigation Language)
(`OGNL`) 由 `OGNL Technology` (`EL`) 创建，是一种用于 `Java` 的开源语言，它使用的表达式比 `Java` 语言支持的全范围更简单，允许获取和设置属性——定义了 `setProperty` 和 `get` 方法——选择 `Java` 类的方法。它还允许更简单的数组操作。

它曾被用于 `Java EE`，并将标签作为表达式。

`OGNL` 现在作为 `OpenSyntax` 项目的一部分开发。

- 还有一个 `OGNL` 的 `NET` 版本。
- `NRCO`（用于轻量级 `MDD` 的 `.NET` 集成框架）
- `op4(ognl-extension)` - `Java` 流式接口实现。
- `MyBatis` `SQL` 映射器框架
- `Thymeleaf` 模板引擎 - `Java` `XML/X/HTML5` 模板引擎。
- `Java` 模块化测试框架

# 使用 OGNL 的项目
- `WebWork` 及其继者 `Struts2`
- `Tapestry`
- `Spring Web Flow`
- `Apache Cache`

> 来源（已编辑）："http://en.wikipedia.org/wiki/OGNL"

# 对象 REXX
`Object REXX` 编程语言是一种最初由 `IBM` 为 `OS/2` 开发的面向对象的语言。它是“经典 `RXX`”的后续和重大扩展，经典 `RXX` 最初为 `VM/PS` 的 `CMS` 组件创建，随后被移植到 `CVS`、`OS/2` 和 `PC DOS`。

2004 年 10 月 12 日，`IBM` 将 `Object REXX` 开发为开源软件，产生了 `Object Rex`，现在适用于各种操作系统：`Linux`、`Solaris`、`Windows`。该实现包含一个用于 `RXX` 的 `WSH` 脚本引擎。

`Object REXX` 通过使用混入类（`mixin classes`）支持多继承。来源（已编辑）："http://en.wikipedia.org/wiki/Object_REXX"

# 操作控制语言 (Operational Control Language)
操作控制语言 (`OCL`) 是 `IBM System/34` 和 `System/36` 微型计算机家族的控制语言。其他控制语言包括 `CL`（`System/38` 和 `AS/400`）、`JCL`（`System/370`）和 `RXX`（`AS/400`）。`DOS` 使用批处理文件也是控制语言。

在 `IBM S/34` 和 `S/36` 上，使用 `OCL` 或系统程序直接加载内存、为其分配资源，并在执行的并行过程中将控制权转移给它们。程序位于计算机磁盘上并不意味着计算机必须运行该程序。

`OCL` 语句可以通过键盘输入，也可以在 `AS/34-S/36` 过程中生成。过程是库中一个自由编辑的成员，与源文件相似。对于 `S/34/S/36`，36 个过程是不完整的。

`OCL` 语句以两个斜杠和一个空格开头。以下是 `System/36` 上的短过程示例，名为 `PROC1`：

```
// ** PROC1
// ** 由 Joe User 写于 2005-06-29
// ** '*PROC1 正在运行'
// ** '*IF-ACTIVE;PROC2,PROC3' GOTO OKAY
// ** IF 意味着 '假'
// ** ACTIVE-'num1,num2' 意味着列出的程序中有一个正在运行
// ** GO XXX 意味着跳过说 TAX xxx 的语句并继续。
```

```
// PAUSE ' 无法取消因为
  other Payroll 正在运行 '
```

```
// CANCEL
  停止此过程的执行
// TAG OKAY
// DATAFFI-FILE1 FFF
DATAFI-FILE2 GOTO NODT
```

```
// '* 注意，天显示在
// CRT
```

```
// '* 按任意键继续并删除
  已存在的文件'
// '*IF-1? CANCEL
  参数通过数字下的
  标记来识别
```

```
// 使用问号
  表示参数是
  并且正在处理
// 等待用户输入。
  立即跳转到结尾。
```

```
// LOAD
// DELETE
  用于删除文件
// RUN
// DATAFFI-FILE1 SCRATCH
UNIT-FILE1-LP1 删除
  一个文件
// DATAFFI-FILE2 SCRATCH
UNIT-FILE1-LP2
// END
  从系统
  程序返回控制权
// LOAD
PR101
PR101 是示例 RPG 程序
// FILE NAME-PAYMAST,DIST-
SHR PAYMAST 是
  工资单主表文件
// FILE NAME-FILE1,DIS-
NEW,RECORDS-100,EXTEND-
  创建了一个新的 FILE1
  记录被分配给如果，系统尝试
  在每次填满时将其扩展 100。
// RUN
** 没必要或有效的将
END 放在
```

## 140
除了 `Linux`、`Apache` 和 `MySQL` 之外，`P` 也可能指 `Python` 或这三者的组合。还使用了 `WAMP` 包（`Windows` / `Apache` / `MySQL` / `PHP`）和 `MAMP` 包（`Macintosh` / `Apache` / `MySQL` / `PHP`）。

截至 2007 年 4 月，已有超过 2000 万个网站托管在运行 `PHP` 的服务器上，且 `mod_php` 被记录为最流行的 `Apache HTTP` 服务器模块。`PHP` 是 75% `Web` 服务器的服务器端编程语言。`PHP` 的 `Web` 内容管理系统包括 `MediaWiki`、`Joomla`、`WordPress`、`Drupal` 和 `Moodle`。网站工具均用 `PHP` 编写，包括 `Wikipedia`、`Facebook` 和 `Discord` 的面向用户部分。

## 安全
国家漏洞数据库（`National Vulnerability Database`）维护着计算机软件中发现的漏洞列表。2004 年数据库中 `PHP` 相关漏洞的占总比例为 20%，2005 年为 28%，2006 年为 43%，2007 年为 37%，2009 年为 30%。大多数 `PHP` 相关的漏洞可以被远程利用；它们允许攻击者从数据源（如 `SQL` 数据库）中窃取伪数据，使用恶意软件进行或破坏拒绝服务（`DOS`）攻击，这些软件可以安装在受漏洞的服务器上。

这些漏洞主要是由于未能遵循最佳编程规则引起的：语言或其代码库的安全缺陷并不常见（2008 年有 23 个，约占总数的 1%）。考虑到程序员是不可信的，某些语言已经解决了由于输入验证缺失导致许多许多关键问题。`PHP` 正在开发此类功能，但在过去将其包含在发布版本中曾多次被拒绝。

在服务器上托管 `PHP` 需要对这些安全风险进行细致且持续的关注。此外，还开发了诸如 `Susin` 和 `Harden-Patch` 等高级补丁，它们是专为 `Web` 托管环境设计的。

`PHPIDS` 为您的应用程序添加了安全性以防御入侵者。`PHPIDS` 可以检测跨站脚本（`XSS`）、`SQL` 注入、头部注入、目录遍历、远程执行、本地文件包含和拒绝服务（`DoS`）。

所有这些分隔符的目的是将 `PHP` 与非 `PHP` 代码（包括 `HTML`）分开。第一种分隔符 `<?php` 和 `?>` 在 `XML` 中允许其他 `XML` 文档、正确的 `XML`“处理指令”。这意味着 `PHP` 代码的结果和在服务器端的输出是格式良好的 `XML`。

```html
<!DOCTYPE html>
<head>
<meta charset="utf-8">
<title>PHP Test</title>
</head>
<body>
<?php echo 'Hello World';
<?php echo(Hello World); ?>
</body>
</html>
```



虽然它不是函数，但它是一种语言结构。在某些情况下，当向`echo`传递多个参数时，参数不能括在括号内。变量用美元符号`$`定义，不需要预先类型。与函数和类名不同，变量名对大小写敏感。双引号（`""`）和 heredoc 也允许将值嵌入字符串中。PHP 以自由语言的方式处理变量（字符串内部除外），语句以分号结束。PHP 使用`/*`进行行内注释；`#`也用于单行注释。`echo`语句是 PHP 提供输出（例如到 Web 服务器）的机制之一。

## 数据类型

PHP 以依赖于平台的范围存储整数，对应 C 语言类型中的 64 位或 32 位符号整数。在某些情况下，符号整数会被转换为值；这种行为与其他编程语言不同，并可以使用十进制（负数）、八进制和十六进制表示法赋值。也表示浮点数。它们可以使用浮点表示法或两种形式的科学计数法指定。PHP 有一种原生布尔类型，类似于 Java 和 C++ 中的原生布尔类型。根据布尔类型转换规则，非零值被解释为真，零解释为假。`null`数据类型表示没有值的变量。该数据类型唯一的值是`NULL`。

PHP 解释器仅在其分隔符内部执行 PHP 代码。在分隔符之外，代码不会被 PHP 处理（尽管非 PHP 文本将作为 PHP 代码输出）。最常用的分隔符是`<?php`和`?>`，或者可用的短形式`<?`和`?>`（用于回显字符串和变量），以及 ASP 风格的短形式`<?%`和`%>`。由于短分隔符可以在 PHP 配置中禁用，支持它们会降低脚本文件的可移植性，反之亦然。

“resource”类型的变量引用来自其他来源的引用。这些是由特定执行的函数创建的，并且在同一个扩展中处理；例如文件、图像和数据库。数组可以包含 PHP 可以处理的任何类型的元素，包括资源、对象甚至其他的。在键值对列表中，顺序会被保留，且值可以交替出现。

## 对象

PHP 在 PHP 3 中增加了面向对象的功能，并在 PHP 4 中进行了改进。PHP 5 对对象处理进行了完全重写，扩展了功能集并增强了性能。在之前的 PHP 版本中，对象像值一样被处理。这种做法的缺点是将对象赋值给变量或作为参数传递给方法。在新方法中，对象通过私有保护方法引用，并带有抽象类和最终类。PHP 5 引入了构造函数和析构函数，类似于 C++ 和 Java 等面向对象的语言。标准 PHP 库（SPL）尝试解决标准问题并实现接口。

## 函数

PHP 有数百个函数，通过扩展有数千个。这些函数在 PHP 网站上有详尽的文档；但存在多种命名规范和不一致之处。函数不是类函数，只能通过名称动态地或通过包含名称的变量来引用。用户定义的函数可以随时创建而不受保护。函数可以定义在代码块内部，允许运行时决定是否定义。

```php
function myFunction() {
    return 'John Doe';
}

echo 'My name is ' . myFunction() . '\n';
```

PHP 5.3 增加了对闭包（closures）的支持，它们应该是定义的。函数调用括号，在使用 PHP `new`运算符调用的零参数类构造函数除外，支持准匿名函数，可以通过名称或间接通过包含函数名称的变量字符串`$function()`来引用。

```php
function getData($x) {
    return function ($y) use ($x) {
        return $x + $y;
    };
}
```

```php
$sadder = getData(10);
echo $sadder(5); // 15
```

`goto`流语句定义如下：

```php
function lock() {
    $file = fopen('file.txt', 'r+');
    if (flock($file, LOCK_EX)) {
        goto retry;
    }
    fwrite($file, 'Success!');
    fclose($file);
    return 0;
    retry:
    // 重试逻辑
}
```

`goto`受到限制并要求目标标签在同一个文件和上下文中，从 PHP 5.3 开始支持。

# 142 - PHP

PHP 语言最初是使用一个 PHP 解释器实现的。我们从互联网上解释 PHP 语言。

上述描述的面向对象编程的基本示例：声明的项可以随处访问。"Public" 是 "public" 的同义词。"Protected" 将访问限制在定义它的类中。"Protected" 将可见性仅限制在定义它的类中。相同类型的对象相互访问，受保护的对象之间，即使它们不是同一个实例。PHP 成员可见性-

```php
class Person {
  public $first;
  public $last;

  public function __construct($first, $last) {
    $this->first = $first;
    $this->last = $last;
  }

  public function get() {
    return "Hello, my name is " . $this->first . " " . $this->last . ".";
  }
}

$shim = new Person('John', 'Smith');
$sher = new Person('Silly', 'Davis');
$sother = new Person('Joe', 'Doe');

echo $shim->get(); // prints "Hello, my name is John Smith."
echo $sher->get(); // prints "Hello, my name is Silly Davis."
echo $sother->get(); // prints "Hello, my name is Joe Doe."
```



### 编译的优势

编译不仅执行速度更快，而且可以混淆、静态分析并提高与其他语言编写代码的互操作性。遵循以下方式实现：

- `C++` 运行时
- `phc`：一个基于 `C++` 的 PHP 编译器，使用 Zend 运行时以获得最大能力
- `Roadend` 使用 `biglio` 实现原生编译，其中被编译为 `C` 语言
- `Raven` - `Roadzend PHP` (`rlph`) 的重写，基于 `LLVM` 和 `C++`
- `Phalanger` 将 PHP 内部编写的源代码编译为 `C` 语言构建类型
- `Caucho/Quercus` 将 PHP 编译为字节码
- `HipHop` 由 Facebook 开发并作为开源可用，将 PHP 脚本转换为 `C++` 并完成编译，将服务器负载降低到
- `php-to` 将 PHP 转换为人类可读的源代码，开发者可以将其编译为 Java 字节码
- `BamBam PHP EXE Compiler/Emitter` - `BamBam PHP EXE` 是一个免费命令行工具，用于将 PHP 转换为独立的 Windows 可执行文件
- `ExecOutput for PHP` - 用于 Windows 的 Visual PHP 转 EXE 软件（商业性）。

### 速度优化

PHP 源代码被动态编译为内部格式，可由 PHP 引擎执行。为了加快执行时间并避免在每次访问页面时都编译 PHP 代码，PHP 脚本应使用 PHP 编译器部署为可执行格式。

代码优化器通过减小体积、消除冗余结构以及进行可以减少执行的更改来处理编译代码的性能。在 PHP 中，存在代码优化的机会。优化器的示例是 `Accelator PHP`。

减少 PHP 服务器负载的另一种方法是缓存 `opcode`（操作码）。`Ocache` 通过将 PHP 脚本的编译形式（`opcode`）缓存在共享内存中工作，以避免每次脚本执行时解析和编译代码的开销。一个 `opcode`、`APC` 将内置在即将发布的 PHP 版本中。

`opcode` 缓存和优化对效率有益，因为这些修改之间不相互依赖（它们发生在编译的不同不同阶段）。

### 属性和方法的可见性

PHP 属性和方法的可见性是指 PHP 中的可见性。可见性使用 `public`、`private` 和 `protected` 关键字定义。如果只使用 `var`，默认是 `public`；`var` 是 `public` 的同义词。

### 编译器

### PROC 过程语言

`PROC` 是 Pick 系统过程语言的名称。`PROC` 类似于 UNIX shell 脚本或 DOS/Windows 批处理文件，并具有控制流函数、文件操作、子程序调用和命令输入等功能。`PROC` 语言由数不可计的宏组成。一个 `PROC` 脚本包含几个 `PROC` 宏和 PICK TCL（终端控制）命令。`PROC` 脚本通常用作程序或应用程序的“前端”，无论是否活跃。

`PROC` 利用两个输入缓冲区（主和从）和两个输出缓冲区（主和从）。某些 `PROC` 仿真版本（例如 Reality X）是 `PROC` 的扩展版本，称为 New PROC，并带有额外的文件。New PROC 通过脚本第一行的 `P` 或 `Q` 来识别，与传统的 `PROC` 命令不同。

Holland 在芝加哥订购使用 `SMI`，最初被称为 `SMILE`（SMI 语言扩展？），然后重命名为 `RPL`（运行时编程语言）。`RPL` 是一种编译型语言，具有 250 个输入缓冲区，但仍被识别自 `PROC`。

开发了大量的规模制造应用，其中一个用于利物浦的 `PlesysGPT` 以及 Tidal 制造软件套件。

1975 年，John Timm 和 Paul Desjarine 开发了名为 `PROC` 的 `PROC` 扩展版本。随后由 Tim 进行了开发。

### Pwb shell

`Pwb shell`（也称为 `Mashey shell`）是随某些版本 1975-1977 年 Programmer's Workbench 分发的早期 Unix shell。它是经过修改的（并且通常被限制为向后兼容）`pwb shell`，具有额外的功能以确保可用性，并由 John Mashey 和等人（Dick Glaser）制作。与当时的大多数 UNIX 系统不同，原始的 PWB 计算机中心无法包含 `/bin` 或 `/usr` 的内容，但想要创建自己的共享命令集，shell 的行为允许执行任何二进制文件变量 `pathname` 变量是 `$PATH` 的祖先，用户在他们选择的目录中搜索命令。

### 后代

这些功能无法克服 shell 的缺点，Stephen Bourne 编写了一个新的 shell。`Bourne shell` 与不兼容，经过修改的（并且通常被限制为向后兼容）`pwb shell` 具有额外的功能以确保可用性，并由 John Mashey 和等人（Dick Glaser）制作。与当时的大多数 UNIX 系统不同，原始的 PWB 计算机中心无法包含 `/bin` 或 `/usr` 的内容，但想要创建自己的共享命令集，shell 的行为允许执行任何二进制文件变量 `pathname` 变量是 `$PATH` 的祖先，用户在他们选择的目录中搜索命令。

## Perl

Perl 最初是为 Perl 设计的单长度（长度不断增加）映射。1991 年，《编程 Perl》（Programming Perl）出版，许多程序员因其封面而称其为“驼峰书”，它成为了该语言的事实参考标准。与此同时，Perl 语言中用于识别标识的更改由 `UNIVERSAL` 包进行记录，它为所有类自动派生的基对象提供了支持，并要求模块的版本。另一个重大进展是包含了 `CGI.pm` 模块，这促进了 Perl 作为 CGI 脚本的流行。

2004 年，Synopses 文档工作开始，该文档最初概述了 Perl 6 语言的命名空间。2005 年 2 月，唐颖（Audrey Tang）在 Haskell 上开发了 `Perks`，这是一个 Perl 6 解释器。这是让 Perl 6 现实的首次尝试。这一努力体现在：

Perl 还支持在 Windows 和其他操作系统下运行。

### 早期 Perl 5

Perl 4 经历了一系列发布，并在 Perl 4.036 中发布。在当时，Wallman 放弃了 Perl 4 转而研究 Perl 5。Perl 5 的初始设计引入了 1995 Peters 列表，该列表于 1994 年 5 月建立以协调平台。开发 Perl 5 的主要原因是实现和 Perl 5 的移植。

Perl 5.005 于 2005 年 7 月 22 日发布。此版本引入了引擎的增强、后端 `B::` 模块的新钩子、`//reg` 正则运算符、对其他核心操作系统的选择，以及对 BeOS 的支持。

2000 年 12 月 18 日，在 Perl 1.0 发布 20 周年之际，发布了 5.10.0。Perl 5.10 引入了带来清晰度的特性（`given/when`）、常规更新以及智能匹配符 `*`。在此期间，另一个名为 Raku 的 Perl 6 实现开始开发，Perl 与 Parrot 虚拟机并行开发。截至 2009 年 11 月，Raku 已有常规月度更新，并且是 Perl 6 最完整的实现。

Perl 5.000 于 1994 年 10 月发布。它几乎是对解释器的重写，并为语言增加了许多特性，包括对象、特性、词法变量（`my`）和模块。重要的是，模块提供了一种在不修改解释器的情况下扩展语言的机制。它更容易被序列化，因为它允许普通程序员访问新的语言特性。Perl 5 一直处于活跃。

### 2000 年至今

Perl 5.6 于 2000 年 3 月发布，主要版本引入了 64 位代码、Unicode 字符串表示、大文件支持（超过 2GB 的文件）以及 `or` 关键字。在开发 Perl 5.6 时，决定将切换方案切换为更具线性或其他作用项目的方案；5.005 导致了 5.640 的出现，计划开发者拥有更多版本和标准。

Perl 5.002 于 1999 年 2 月发布，带有 20 个新特性。该模块的添加使得子程序的行为类似于 Perl 的构建。Perl 5.005 于 1996 年 6 月 25 日发布，作为一个安全发布版本。

Perl 5 开发中的一个重大变化随着 Perl 6 的出现，开发社区切换到一种主要的发布周期，发布日期间隔为三个月。

Perl 5 历史上最重要的事件之一发生在语言之外，这是其模块支持的结果。1995 年 10 月 26 日，综合 Perl 存档库（`CPAN`）被建立，作为 Perl 和其他模型的仓库。截至 1996 年 1 月 1 日，已有 8,000 模块。

2010 年 4 月 12 日，发布了 Perl 5.12。显著变化包括 `VERSION` 语法、`Yada` 占位符。在 2011 年 1 月 21 日，Perl 5.12 引入了带来清晰度的特性（`given/when`）、常规更新以及智能匹配符 `*`。在此期间，另一个名为 Raku 的 Perl 6 实现开始开发，Perl 与 Parrot 虚拟机并行开发。截至 2009 年 11 月，Raku 已有常规月度更新，并且是 Perl 6 最完整的实现。

（注：由于提供的原文中存在大量重复段落，译文按原文逻辑进行了对应翻译并保持了格式的一致性。）

早期的语言（如 Fortran 和 C）旨在利用昂贵的计算硬件。而 Perl 的设计初衷是为了利用昂贵的计算——程序员，因此 Perl 可能很难找到。Perl 的函数文档对内置函数在列表和标量调用中的变体行为注释道：“在 Perl 中，你可以得到你想要的，除非你希望它在 Windows 和 Unix 之间具有移植性。”可移植代码通常被软件供应商（商业现品 COTS 和定制软件）使用，以简化软件构建-部署脚本的打包和维护。

Perl 有许多特性可以减轻程序员的任务，并降低对 CPU 和内存的需求。这些特性包括自动内存管理、动态类型、字符串、哈希表（`hashes`）和正则表达式；以及内置方法，这种思想类似于“零无限规则”（Zero-Infinity rule）。

对于 Perl 5 及以前之前的版本，并不存在统一的规范或标准，也没有计划为当前的 Perl 版本创建规范。该语言只有一个解释器实现，而该语言及其解释器共同构成了该语言的事实规范。Perl 6 是从规范开始的，相关项目旨在实现该规范的部分或全部内容。

可以使用 Perl 开发图形用户界面（GUI）。例如，`Perl/TK` 常用于实现用户与 Perl 脚本的交互。任何交互可以是同步或异步的，通过回调函数作用 GUI。更多关于所用技术的信息，请参阅 `Tk` 和 `WebPerl`。

Wall 接受过语言学训练，并根据语言学原理设计了 Perl。示例包括霍曼编码（常用结构应尽可能短）、加权（重要信息应优先）以及大量的原语集合。Perl 的语言结构精确且书写自然，即使这会增加 Perl 解释器的复杂性。

Perl 也被广泛应用于生物信息学，其因快速开发应用和处理大型数据集的能力而受到青睐。

Perl 的语法反映了“事物应该看起来不同”的思想。例如，标量、数组和哈希表具有不同的长度。数组索引和哈希表使用不同类型的字符串。字符串和正则表达式有不同的分隔符。这与 L 等语言形成对比，在 L 语言中，许多不同的用途都使用相同的 S 表达式（S-expression）和语法。

### 应用

Perl 有许多各种应用，许多标准模块和第三方模块的可用使其应用更加丰富。

### 实现

从 Web 时代起，程序员就一直使用 Perl 编写 CGI 脚本。Perl 是编写 Web 应用最流行的“三大”语言之一（与 Python 和 PHP 并列）。它是用于 Web 开发的 `LAMP` 栈解决方案不可或缺的一部分。Perl 用于 `CPAN`、`Slash`、`Bugzilla`、`RT` 和 `Movable Type`。许多高流量网站广泛使用 Perl。例如：`Amazon`、`Craigslist`、`DBI` 和 `Ticketmaster`。Omneti 也在互联网、内网和后端服务中广泛使用 Perl。

Perl 以 C 语言实现为核心解释器，并带有大量的 Perl 和 C 模块集合。截至 2010 年，稳定版本（5.12.3）是一个封装在 `tar` 文件中并压缩的 12 MB 文件。解释器包含 150,000 行 C 代码，编译到其他程序中至少占用 1 MB 空间。

Perl 不强制执行任何编程范式（过程式、面向对象、函数式或其他），甚至不要求程序员在它们之间进行选择。

Perl 被用作胶水语言，将那些并非专为它设计的系统和接口连接在一起，并用于“数据管理”（即为此类任务转换或处理大量数据）。在这些报告中，这种有限的组合使得 Perl 成为系统管理员强大的全能语言，特别是因为短程序可以嵌入并在单行中运行。

Perl 社区与其创造的文化之间存在广泛的益处。Perl 的格言是：“为了完成你的工作语言。”其结果之一是 Perl 不是一种整洁的语言。它有许多特性，容忍规则的例外，并使用启发式方法来解决语法歧义。由于编译器具有宽容的特性，解释器采用了面向对象的架构。Perl 语言的所有元素——标量、数组、哈希表、代码引用（coderefs）和过滤器——在解释器中通过 C 结构体表示。对这些结构的操作由大量的模块、类型定义（`typedefs`）和函数定义；这些构成了 C API。非专业人士也可以开发 API，但其入口遵循一致的命名方案，让用户可以轻松使用它们。

Perl 解释器的生命周期大致分为复杂阶段和运行阶段。在 Perl 中，这些阶段是解释器生命的主要阶段：经过仔细处理，Perl 代码可以被解析。每个解释器只经历一次阶段，且这些阶段按照固定顺序进行。问题是不可否认的，因此即使是 Perl 也并不总是能解析；Perl 做了一个不寻常的选择，允许用户在其代码中访问其完整的编程能力。理论代码是纯英雄式的，但实际的便利性可能很少见。

### 可用性

Perl 编译阶段发生的大部分是编译，Perl 运行阶段发生的大部分是执行，但存在例外。Perl 的重要在于其编译阶段执行代码的能力。Perl 还会将编译延迟到运行阶段。指示过程实际上在任何时刻发生的术语是编译时间（compile time）和运行时间（run time）。在编译阶段的大部分时间内 Perl 处于编译时间，但在运行阶段也可能进入运行时间。字符串中代码的编译时间通常发生在编译阶段的运行期间，并在运行阶段的大部分时间内处于运行时间。`BEGIN` 块在运行时执行，但处于编译阶段。

Perl 根据艺术许可协议（Artistic License）和 GNU 公共许可证（GNU Public License）授权。大多数操作系统都有相应的分发版本。它在 Unix 类系统上尤为流行，但已移植到每个现代（以及许多其他）平台。在 POSIX 兼容平台上，可以从源码编译 Perl。

`Cygwin` 仿真层是在 Windows 下运行 Perl 的另一种方式。`Cygwin` 在 Windows 上提供了一个类 Unix 的环境，Perl 和 CPAN 都可以通过 `Cygwin` 安装程序以预编译包的形式提供。`Cygwin` 还包含了 `gcc`，也可以从源码获取 Perl。

在多种编程语言中，Perl 的实现实现在内存占用方面处于较高水平，且执行速度各异。Perl 在基准测试游戏中的表现是解释型语言的典型水平。

Perl 程序的程序可以用 C 或汇编等其他语言编写，并通过简单的 `Inline` 模块或更复杂但灵活的 `XS` 方案与 Perl 连接。Perl 核心开发者 Nicholas Clark 在 2002 年的一份名为《Perl 运行不够快》的文档中讨论了 Perl 的设计趋势和解决方案。

### 数据库接口

Perl 被广泛应用于数据库。其文本处理功能对于生成 SQL 查询非常有用；数组、哈希表（hashes）和自动内存管理使得收集和处理数据变得简单许多。

在 Perl 的早期版本中，数据库接口是通过将解释器与客户端库重新链接来创建的。这非常困难，因此仅针对某些最重要、最常用的数据库进行，并且限制了 Perl 可执行文件一次只能使用一个数据库接口。

大型程序的启动速度比相应语言编写的程序慢，因为 Perl 在每次运行时都必须编译源码。在 YAPC: 2005 大会的一次演讲以及随后的文章《时间》中，Steve Jean-Ler 发现 Perl 程序的运行时间比预期长得多，这是因为包含路径过大导致解释器花费了更多时间来寻找模块。Java、Python 和 Ruby 只对预编译有实验性支持。因此，Perl 在每次执行时都要付出这种开销。典型程序的运行时间很长，并非实质性的，但衡量每次执行的基准测试可能会因此而产生偏差。

在 Perl 5 中，数据库使用 `DBI` 模块实现。`DBI`（数据库接口）模块为 Perl 应用提供单一的、与数据库的接口，而 `DBD`（数据库驱动程序）模块处理访问约 50 个不同数据库的细节；大多数 ANSI SQL 数据库都有 `DBD` 驱动程序。

### 未来

`DBI` 提供了缓存句柄和查询，这可以极大提高如 `mod_perl` 等长时间环境的性能，以及像 `mod_helper` 中的 `spikes` 这种高频参数系统的性能。

Camelia，用于 Perl 6 项目

在 2000 年 Perl 大会上，Jon Orm 为一项新语言倡议进行了辩护。这导致了开始重新设计语言的决定，称为 Perl 6。Perl 社区提交了新功能的提案，并提交了更多 RFC。

在现代 Perl 中，数据库框架是用 Perl 编写的。在 `Catalyst` 中，经常通过对象关系映射（如 `DBI::Class`；`Class::DB::Object`）直接使用 `DBI` 模块，这些映射生成 SQL 查询并处理到应用程序的数据透明性。

Larry Wall 在接下来的几年里起草了 RFC，并将它们整合成一个 de Perl 6 框架。他在一系列名为“Apocalyps”（启示录）的文档中展示了他的 Perl 6 设计，这些文档旨在与《Programming Perl》中的章节对应。截至 2011 年 1 月，Perl 6 的规范封装在名为“Synopses”的设计文档中，其编号与 Apocalyps 对应。

一旦 Perl 完成编译，在执行期间会有额外的开销，这通常在用 C 或 C++ 等编译型语言编写的程序中是不存在的。此类示例包括字节码解释、引用计数内存管理和动态类型检查。

Perl 6 不向后兼容，尽管将有一个兼容模式。Perl 5 和 Perl 6 是具有共同祖先的不同语言。

### 优化

与任何代码一样，在完成可读且正确的实现后，可以使用基准测试和标记对 Perl 程序进行性能调优。事实上，作为 Perl 解释本质的一部分，编写更高效的 Perl 将不足以满足某项目的性能目标。

在这种情况下，最关键的……

### 性能比较

计算机语言基准测试（Computer Language Benchmarks）是由 Alhioth 发的一个项目，比较了典型编程问题实现的性能。

这项由 Bradley M. Kuhn 完成、Larry Wall 监督的工作考虑了将 Java 虚拟机作为 Perl 运行时的可能性。Kuhn 证明这种方法存在问题。

2001 年，决定 Perl 将运行在一个名为 `PerlVM` 的跨语言虚拟机上。这意味着针对虚拟机的其他语言将获得 CPAN 的访问，允许某种程度的跨语言开发。

Wall 年度关于 Perl 及其社区进展的主演讲总结。它们的特点是以其标志性的幽默为特征，引用了 Perl 的美德以及黑客文化。Wall 的语言背景，有时他的生活，偶尔还有他的基督教背景。

在 90 年代末是一项广为人知的消。混淆 Perl 大赛（Obfuscated Perl Contest）是《Perl Journal》从 1996 年到 2000 年举办的一项竞赛，将 Perl 的语法灵活性视为一种美德。奖项类别包括“最强大——最佳四行”程序，这些程序符合 Usenet 口号风格，且在四行每行76 个字符内。

2005 年，唐彩（Audrey Tang）创建了 `p` 项目，这是 Haskell 对 Perl 的实现。这是为了作为 Perl 语言的测试平台（从实际实现的开发开始），允许语言设计者进行探索。这些 `pugs` 产生了一个围绕 `#perlirc` 频道的活跃 Perl/Haskell 社区。

### 诗歌

Perl 诗歌是指编写可以被视为合法 Perl 代码的诗，这种作品被称为“Black Perl”（黑魔术）。这是由于 Perl 中使用了大量的英语单词才可能的。新诗定期提交给 PerlMon 社区。

Perl 6 语言中的许多功能现在与 Haskell 具有相似之处。作为 Perl 语言的测试平台（从实际实现的开发开始），允许语言设计者进行探索。这些 `pugs` 产生了一个围绕 `#perlirc` 频道的活跃 Perl/Haskell 社区。

### Perl 的消遣

### JAPHs

在 Usenet 和留言板上，“Just other Perl”（JAPHs）是一个常用术语，由最早的专业 Perl 培训师之一 Randy L. Schwartz 创。在 Perl 语言中，Perl 程序员被称为黑客（hackers），并由此产生了编写脚本打印出“Just other Perl”短语的力量，本着原始理念，这些程序是经过混淆的，并且足够短，可以放入 Usenet 消息的大小中。Schwartz 解释了“规范”的 JAPH。

根据起源，Perl 6 主要集中在 Rakudo Perl6 上，这是运行在 Perl 虚拟机之上的一个实现。另一个实现 Midway 正在积极开发中，且不使用 Perl。

### IRC 上的 Perl

有许多个 IRC 频道为该语言和社区提供支持。

Perl 5 的开发也在继续。Perl 5.12 于 2010 年发布，带有 Perl 6 引入的新功能。维护和更新按每月发布，在 5.12 系列中，5.12.3 于2011 年 1 月 22 日发布。Perl 5.14（或 5.14.0）于 2011 年 5 月 14 日发布。

### CPAN Acme

CPAN 上有很多纯为了娱乐编写的代码示例。例如 `Lingua:Romana:Perligata`，用拉丁语编写程序。执行此类程序时，模块会将代码转换为拉丁语并运行。

Perl 社区一直在开发这种语言。Usenet 是 Perl 首次引入的地方，但在其演变过程中，Perl 社区是由包括全球网在内的互联网服务的塑造的。社区实际上是 Larry Wall 的故事《State of the Onion》，

### Perl gold

“golf”是将 Perl 程序的字符数（击球”）减少到最小的消遣，就像高尔夫球员在回合中尽可能减少击球一样。对“golf”一词的使用集中在 Usenet 帖子中的 JAPH 上，尽管学生在之前的几十年对 Perl 语言使用了一个未命名的。在随后的几年里，术语“code golf”被应用于其他语言。2000 年，在加州蒙特雷举行的 Perl 大会 40 上举办了一场 Perl gold Apocalypse。

Perl 社区留了一些为了趣味的“Acme”模块（但其范围已扩大到包含探索性代码或任何不打算用于生产的模块）。

### State of the Onion

State of the Onion 是 Larry 的名字

### Obfuscation

就像 C 一，混淆性的

## PerlScript

`PerlScript` - 第 151 页

`PerlScript` 最初是由 ActiveState 公司产生的一种活动脚本引擎（Active Scripting Engine），用于微软的 Internet 服务（IIS），以便程序员能够除 VBScript Web 服务器之外或替代其使用基于 Perl 的代码。随后，`Apache:ASP` 采用了 Perl，这允许仅使用 Perl 进行编码，但 `VScript` 和 `PerlScript` 均无法像 `VScript` 那样用于编写 Windows 宿主机程序。

```xml



# PerlScript

PerlScript 最初是由 ActiveState 公司产生的一种活动脚本引擎，用于微软的 Internet 服务（IIS），以便程序员能够除 VBScript Web 服务器之外或替代其使用基于 Perl 的代码。随后，Apache:ASP 采用了 Perl，这允许仅使用 Perl 进行编码，但 VScript 和 PerlScript 均无法像 VScript 那样用于编写 Windows 宿主机程序。

```xml
use strict;

source $wScript;

$wScript->Echo("Hello World!");

my $countArgs = $ARG->{Count};

for (my $i=0; $i<$countArgs; $i++) {

    $wScript->Echo($ARG->($i));

}

</script>
```

`.perl` 文件无法获得拖放 WSH 功能。PerlScript 具有的扩展名需要 XML 标签，这些标签指定任务 ID 和脚本语言，例如：

Perl 脚本可以访问 WSH 拖放功能，类似于现在已过时的 MacPer 中的 Perl Droplets。大多数 WSH 对象均通过隐式创建的 `WScript` 对象可用。来源（编辑后）："http://en.wikipedia.org/wiki/PerlScript"

```xml
<Object id="DroppedFiles">

<script language="PerlScript">

use strict;

source $wScript;

$wScript->Echo("Displaying names of dropped files");

my $arg = $wScript->(Arguments);

</script>
```

如果独立的 PerlScripts 是用扩展名 `.pl` 创建的，则可以执行，但它们并没有这种扩展名。

# perl shell

Perl shell (`perl`) 是一种命令行环境，可以作为你在类 Unix 操作系统上登录后的主要 shell。只需发布以下命令即可：

# 代码示例

```bash
perl -CPAN -e 'install Psh'
```

由于是用 Perl 编写的，`perl` 也可以用于 Microsoft Windows（带有 Cygwin 或 Helix）以及其他操作系统。对于 Ghent 和 Ubuntu 等 Linux 发行版，提供了相应的包，尽管大多数系统可以从 CPAN 安装。

## 特性

```bash
ls | s/y/k/

PCRE.

替换

ls | +\$i; ";" \q 遍历行。

netstat | {$2; } -Grep.
```

Perl Shell 将 bash（以及 Unix shell）的特点与 Perl 脚本的力量结合在一起。来源（编辑后）："http://en.wikipedia.org/wiki/Perl_Shell"

# Pike（编程语言）

Pike 是一种解释型的、高级的、跨平台编程语言，语法与 C 相似。与许多其他语言不同，Pike 既是静态类型也是动态类型，并且需要显式定义。它具有一个灵活的类型系统，允许动态类型语言的快速开发和灵活代码，同时提供了静态类型语言的优势。许多程序，包括面向对象、函数式和命令式编程。Pike 是在 GPL、LGPL 和 MPL 许可证下的自由软件。

所有者不用于商业目的，因此在 1994 年编写了一个新的 GPL 实现，即 `μLPC`（micro LPC）。1996 年，`μLPC` 被重名为 Pike，以提供一个更具商业可行性的名称。尽管公司名称多年年来发生了变化，但名为 Rox Internet Software 的公司聘佣了 Pike 开发人员并为 Pike 的开发提供了资源。Roxen 是由 Pike 开发的 Web 服务器公司的名称。2002 年，编程环境

Pike 具有垃圾回收、高级数据类型和一等匿名函数，并支持

# 历史

Pike 根于 LPC，这是一种为 MUDs 开发的语言。该语言由位于林ö雪平的 Larssson 开发，最著名的有 Fredrik Hübner 和 Per Holm，他们将语言和虚拟机从 MUD 中分离出来，并将其作为语言应用程序的快速原型工具；在 LPC 4 中，Pike 的 li

林ö雪平大学从 Roxen 手接了 Pike 的维护工作。几位 Pike 程序员来到了 Open Software 位于林ö雪平的办公室，该语言在 Open Mini 的服务器/网关部分起着核心作用。

Pike 提供了各种数据类型。高级数据类型如序列、队列、堆、栈等在 ADT 模块中可用，该模块包括类浮点数的表示。

```pike
int/float; // 整数或浮点数变量

number = 5; // 这是合法的

number = 5.5; // 这也是合法的
```

# 语法高亮

- 基本数据类型：
  - `int`
  - `float`
  - `string`

由于变量可以声明为持有许多不同的数据类型，提供了函数来确定当前存储什么类型的数据。这些函数都是相同类型的，如 `int`、`float`、`string`。

- 容器类型：
  - `array`
  - `mapping`
  - `multiset`

### Hello World

关于编程传统“Hello World”的解释，请参见 Hello world 程序。

```pike
int main() {

  write("Hello world!");

  return 0;

}
```

```pike
int/float;

number = 5;

p(number); // 返回 true

floatp(number); // 返回 false

number = 5.5
```

- 其他类型：
  - `program`（编译后的程序）
  - `object`（类的实例）
  - `function`

Pike 要求变量具有显式类型。这使得它能够在编译时报告错误。以下代码将导致编译器错误，因为由于值 "number" 必须是整数，但代码正将一个字符串指向它。此外，还有一种“特殊”数据类型。它允许变量持有任何数据类型。



## 其他类型

- `program`（编译后的程序）
- `object`（类的实例）
- `function`

Pike 要求变量具有显式类型。这使得它能够在编译时报告错误。以下代码将导致编译器错误，因为由于值 `"number"` 必须是整数，但代码正将一个字符串指向它。

（注：原文后半部分存在大量无效乱码和重复，已根据逻辑要求进行清理翻译。）

## 154 - Python（编程语言）

Python 支持函数式编程和面向切面的编程（包括元编程和魔法方法）。其他范式通过扩展支持，例如 PyDBC 和 Contracts for Python，允许契约设计（Design by Contract）。

Perl 的语言设计理念是“实现某事的多种方法”，而 Python 则认为“应该只有一种——最好只有一种——明显的实现方法”。可读性以及避免“多种实现方式”导致的不可可读代码或难以理解的惯用法至关重要。

Python 开发者强调简单性，并可能会拒绝某些非原生拷贝的补丁，即使这些补丁以牺牲清晰度为代价提供了微小的优势。

Python 的用户和仰慕者——尤其是那些知识或经验丰富的人——通常被称为 Pythonistas 和 Pythons。

Python 使用动态类型，并结合引用计数和循环检测垃圾器进行内存管理。Python 的一个重要特性是动态解析（后期绑定），它在程序执行期间绑定方法和变量。

有些部分被描述为“一直缓慢”，根据帕累托法则，Python 的大多数问题和部分并不是运行很快。Python 程序员尝试使用像 PyPy 这样的 JIT 编译器，将对时间敏感的函数重写为 C 等“底层”语言，或者通过工具将 Python（或其变体）翻译为 C 代码。

前缀 `Py` 可表示某物与 Python 有关。该前缀在 Python 应用程序或库中的示例包括：`Pygame`（SDL 到 Python 的绑定，通常用于创建游戏）、Simbian 60 操作系统；`PyQt` 和 `PyGT`（将 C 和 GTK 绑定到 Python）；以及 `PyQt`（一个也用于软件包之外的 Python 实现）；主要的 Python 大会名为 `PyCon`。

Python 并不是追求将所有功能构建在语言中，而是具有高度的可扩展性。新构建模块可以用 C、C++ 或 Python 编写。Python 也可以作为现有模块和应用程序的扩展语言，这些应用需要小核心、大库的设计，并从 Van Rossum 冲突之初就能够被容易解释（这与相反的观点相对立）。

该语言的核心哲学记录在“PEP 20（Python 之禅）”中。

## 名称与新词

开发者社区的一个重要目标是让 Python 易于使用。这体现在“Python Flying Circus”名称的起源上（指在代码中使用 Python 哲学作为参考示例），以及偶尔在趣味性教程和参考资料中使用。

Python 被用作应用程序脚本语言，例如用于 Web API。通过服务器网关接口（WSGI），开发出了一种标准 API 来促进应用程序。Web 还支持 Django、Typelon、Flask 和 SQLAlchemy 等框架，它们支持开发者开发和维护复杂应用程序。

例如，Python 语言的设计简单且优雅，以及 Python 和 eggs，“在一起”。

与 Lisp 相比，Python 对函数式编程的支持有限。Python 的设计与极简 Lisp 语言（如 Scheme）相似之处。标准库有两个模块（`iterertools` 和 `functions`），实现了来自 Haskell 和 Standard ML 的函数式工具。

Python 社区中的常见概念，与程序风格有广泛的含义。如果一段代码是 Pythonic（符合 Python 风格的），它使用了 Python 标识，而不是取决于它是什么或在语言中有多久久历史。

在提供方法选择的同时，Python 哲学拒绝像 Perl 那样的夸张语法，而是倾向于稀疏、不杂乱的语法。Python 开发者推广一种引导使用的“文化”或意识形态，避免使用他们认为“美丽”、“显式”的语言形式，正如 Alex Martinez 在他的《Python Cookbook》（2002版，第230页）中所说：“描述某物不被认为是 Python 文化的一部分。”Python 的哲学拒绝了……

Python 已经作为脚本语言成功开发在许多软件项目中，包括有限元软件，如 3D 动画包 Houdini、Maya、Body3DPaint、Blender、Cinema 4D，以及诸像 GIMP、Shot Shop 这样的成像程序。GNU GDB 使用 Python 作为其主要工具来编写类似 C++ 的复杂脚本。ESRI 现在正推动 Python 作为在 ArcGIS 中编写脚本的基础。它甚至被用于视频游戏并作为其中之一。

编写 pythonic 代码的哲学是，在 Python 中——即在……或在……中——提供了丰富的描述，而不是来自另一种语言的惯用翻译。简单性的概念与 Python 的极简哲学紧密结合，两者是 Google Docs 中两种可用的脚本语言之一。

对于许多操作系统，Python 是一个标准组件；在大多数 Linux 发行版、NetBSD、OpenBSD 和 Mac OS 中，可以从终端使用。许多 Linux 发行版使用 Python 编写安装程序：Ubuntu 使用 Ubiquity 安装器，而红帽（Red Hat）和 Fedora 在其包管理系统中使用 Linux Python，其他在系统期间使用。

Python 在信息安全行业也有广泛应用，除了漏洞开发。

在 Python 的用户中，你有公告牌万亿客户。使用 Python 的大型组织包括 Google、Yahoo!、CERN、NASA、ILM 和 ITA。笔记本 XL 的大部分内容由 Python Labs 开发。

## 缩进

Python 使用空白缩进而不是大括号或关键字来界定代码块（该特征也称为侧边规则）。在某些语句后增加缩进；缩进减少则表示当前代码块的结束。

## 语句与控制流

Python 的语句包括（但不限于）：

- `if` 语句条件地构成一个代码块，带有 `else` 和 `elif`（if-else 的缩写）。
- `for` 语句遍历迭代对象，将每个元素捕获到局部变量供其关联的代码块使用。
- `while` 语句只要条件为真，就会执行代码块。
- `try` 允许关联代码中的异常被 `except` 子句捕获；还确保 `finally` 块无论如何退出都会执行。
- `class` 语句将块连接到其命名空间，用于面向对象编程。
- `def` 语句定义函数或方法。
- `with`（来自 Python 2.5），在上下文管理器编码代码块（在运行块前获取，运行后释放）。
- `pass` 语句作为空操作，可在代码块中使用。
- `assert` 语句，在调试期间用于应当的条件。
- `yield` 语句，从生成器返回值。（从 Python 2.5 开始，`yield` 也是一个运算符。）

## 表达式

Python 表达式类似于 C 和 Java 等语言。注意事项：

- 在 Python 2 中，`/` 运算符执行整数除，即截取整数。在 Python 3 中，`/` 的结果始终是浮点值，并引入了 `//` 运算符来处理整数除。在 Python 2 中，可以使用 `from __future__ import division` 启用这种行为。
- 在 Python 中，`==` 比较值，而 Java 中比较的是引用（Python 中的值比较使用 `equals()`）。
- Python 使用 `and`, `or` 作为其布尔运算符，而不是符号 `&` 和 `!`。
- Python 有一种重要的表达式类型被称为列表推导式。最近版本的 Python 使用 lambda 表达式扩展了列表推导式；但这些受限于体只能是单个表达式。
- Python 中的条件表达式写为 `if x else y`（操作数顺序不同：运算符在许多其他语言之前）。
- Python 区分了元组和列表。列表是可变的，而 `[1, 2, 3]` 不变，且不能作为字典的键。

## 语法与语义

```
def deostist(n):

    for i in range(n):

        if i % 2 == 0:

            print(i)

        else:

            print(i)
```



语法高亮 Python 2.x。Python 旨在成为一种高度可读的语言。它的设计具有清晰的视觉布局，经常使用英语单词和标点符号。与传统的强类型语言如 C、Pascal 相比，Python 需要的模板代码更少，特殊情况也较少。关于 2 和 3 版本差异的详细描述，请参见 Python 历史。

## 156 - (编程语言)

在 Python 中字典可能是不可变的。元组被写为`(1, 2, 3)`，它们是不可变的，因此可以作为字典的键。在某些语文中，元组周围的括号是可选的。

元组可以出现在等号的左侧；然而，可以使用`x, y`来交换变量。

- Python 有一个“字符串格式化”运算符。该运算符的功能类似于 C 语言中的格式化字符串，例如，`"foo%s-%%s" = "blah", 2`的求值结果为`"foo-bar=2"`。在 Python 3 中，这已经被`str`类的方法取代了，例如`"{}-={}".format("foo", "bar")` = "bar")`。

- Python 有各种类型的标记。可以使用单引号或双引号来引用字符串。与 Unix shell 或受 Ruby 或 Groovy 等影响的语言不同，字符串和双引号不具有函数插值功能，即没有字符串函数的插值。

- 还有多行字符串，它们以三个单引号或双引号开始和结束，在这里充当 shell 语言、Perl 和 Ruby 中的文档。

- 最后，上述的字符串类型可以是“原始”的（通过在起始引号前放置一个字面量`r`），它们不进行反斜杠插值，对于正则表达式或 Windows 风格的路径非常有用；对比`"@quoting"`。

Python 在列表上有切片表达式，表示为`[left:]`或`[left:right]`。例如，如果变量`nums`被赋值为列表`[1, 3, 5, 7, 8, 13, 20]`，以下表达式将求值为为`True`：

- `nums[:5] = [5, 7, 8]`，即切片包含但不包含右侧索引。

- `nums[1:] = [3, 5, 7, 8, 13, 20]`，即除第一个元素以外的所有元素，因为省略右索引意味着“结束”。

- `nums[-3:] = [1]`，即省略左索引意味着“开始”，且负索引（无论左还是右）都从末尾计数。

- `nums[::]`产生列表的副本。这意味着`nums == nums`为`true`但`nums is`为`false`。对副本的更改不会影响原始对象。

- `nums[1::2] = [3]`，即如果给出三个数字，第三个被称为“步长”，表示在这种情况下将选择每第二个元素。

在 Python 中，舍弃了表达式和语句之间的区别，这与 Common Lisp、Scheme 或 Ruby 等语言不同。

Python 中的内置函数`eval(x)`是一个语句；前者是表达式，后者用于语句。

语句不是表达式的一部分，因此像 lambda 表达式（表达式）等其他语言不能包含语句。其中一个特殊情况是赋值语句（如`a =`）不是条件语句的一部分。这种避免了考虑 C 风格的三元运算符或赋值运算符`==`的`if (c == 1) { = }`代码，这种代码在 Python 中会导致语法错误。

## 方法

对象上的方法附加在对象的类上；即实例。`instance.method(argument)`用于方法和函数，是`Class.instance(argument).`的语法糖。Python 方法没有显式访问实例数据的权限，这与隐式的`self`相反。

## 类型

Python 使用动态类型，并拥有没有变量名的对象。类型限制不在编译时进行检查；对对象的操作可能会失败，因为该对象不是合适的类型。尽管是动态类型的，但 Python 是强类型的，对于未定义良好的操作（例如，向字符串加数字），它不会静默地让它们产生意义。

Python 程序员可以使用类来定义自己的类型，类最常用于面向对象的编程。类的新实例通过调用类来构造（例如`SampleClass`或`EggClass()`），而类本身是元类（其自身）的实例，这涉及元编程和反射。

在 Python 3.0 之前，Python 有两种类：“旧式类”和“新式类”。新式类在 Python 3 中引入，使得所有类都成为新式类。在 2 和 3.0 版本之间，可以使用这两种类。两者的语法都很简单，区别在于直接或间接继承的类对象（所有新式类都继承`object`并是`object`的实例）：

## 数学

Python 定义的运算符规定如果`b`是正整数，则`% b`的结果在整数`[0,b)`范围内。然而，这种结果如何影响整数除法以定义表达式`b // a + a % b = a`的值，整数除法向负无穷取整。`7 // 2`等于`3`，这与许多编程语言不同，在许多语言中，整数除法的结果向零取整，因此定义的方法会返回负数。

以扩展到数千个核心。

Python 提供了一个`round`函数将浮点数转换为整数。在 2.6 及以下版本中使用远离零的舍入：`round(0.5)`为`1`，`round(-0.5)`为`-1`。3.0 及更高版本使用向偶数舍入：`round(1.5)`为`2`，`round(2.5)`为。

## 替代实现

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

- Python 提供了一个`round`函数将浮点数转换为整数。
- Python 提供了一个`round`函数以扩展到数千个核心。
- Python 提供了一个`round`函数将浮点数转换为整数。在 2.6 及以下版本中使用远离零的舍入：`round(0.5)`为`1`，`round(-0.5)`为`-1`。3.0 及更高版本使用向偶数舍入：`round(1.5)`为`2`，`round(2.5)`为。

## 替代实现

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

Python 将程序编译为 Java 字节码，可以由每个 Java 虚拟机引擎执行。这使得能够为 Python 程序使用 Java 类函数-。IronPython 允许类似的方法，以便在 .NET 通用运行时运行程序。PyPy 是一种快速的自托管 Python 实现，它用 Python 编写，可以输出多种类型的字节码、对象代码和索引。

## CPython

Stackless 是 CPython 的一个功能，实现了 mi-chroads；它不使用 C 堆栈。它预计将在与 Python 相同的平台上运行，甚至在只有 4KB 内存的环境中。

Nokia 9900 支持带有小部件库的 Python，其特性可以在设备内运行程序。Windows CE- 有一个 Python 解释器（包括 Pocket PC）。它被称为 Jython。

Google 在 2009 年启动了一个名为 Shadow 的项目，目标是使用 LLVM 将 Python 解释器提高 5 倍并增加其多处理能力。

## 开发

Python 的开发通过 Python 增强提案（PEP）进行。PEP 是提供的标准化设计文档-。

2004 年左右，Pyastra 项目创建

## 158 - (编程语言)

提供与 Python 相关的的信息，包括提案、描述、设计原理以及语言特性的解释。卓越的 PEP 由 Python 项目的“终身仁独裁者”（语言架构）Van Rossum 进行评审和评论。Python 开发者还通过邮件列表视图进行交流，该视图是讨论语言开发的主要论坛；特定问题在 python.org 维护的 Roundup 错误跟踪器中进行讨论。开发在代码中，通过在开发期间运行大型单元测试，并使用 BuildBot 持续集成系统。

对于测试，标准库提供了`unittest`和`ittest`模块。

## 标准库

### 对其他语言的影响

Python 拥有庞大的库，这通常被认为是 Python 的优势之一，它提供了许多适用于特定任务的强大工具。这是刻意为之，并描述为“电池内置”的 Python 哲学。标准库的模块可以使用 C 或 Python 自定义模块进行扩展。Boost 库包括 library、Boost 和 Python。由于标准库提供了各种工具，并且具有使用 C、C++ 编写的其它语言的能力，Python 能够轻松地与其他库之间进行接口交互。

Python 的设计和哲学影响了几种编程语言，包括：

- Pyrex 及其衍生 C 代码翻译器，旨在为 Python 解释器编写 C 扩展。该语言通过针对 C 和 C++ 特性的 Python 语法扩展移动。两种语言都提供兼容的 C 输出。
- Boo 思想，具有类似的语法和对象模型。然而，使用其语法与 .NET 框架紧密集成。
- Cobra 使用缩进和语法。Cobra 直接支持设计契约、接口和可选测试语法。
- ECMAScript 借用了生成器、迭代器。

标准库专门为面向互联网的应用程序而定制，已经支持了大量的标准和协议（如 MIME 和 IMAP）。还包括创建图形用户界面、连接到关系型数据（具有算术精度）以及调节测试的方法。

Python 的开发实践也遇到了一些问题。库的某些部分由 PEP 333 的规范（如 WSGI 实现）覆盖，但大多数模块并没有绑定。它们由规范代码、内部文档和测试（如果提供）组成。然而，由于标准库大部分是跨平台 Python 代码，有少数模块必须由替代实现进行修改或完全重写。

来源（已编辑）："http://en.wikipedia.org/wiki_(programming language)"

标准库对于在应用程序中运行或嵌入 Python 并不是必需的。Blender 2.49 在最终发布前对大部分标准库进行了测试。还发布了许多 alpha、beta 和发布候选版本。如果对发布进行粗略检查，如果代码未准备就，通常会推迟。开发团队监控状态的-

## Python for S60

Python for S60 也称为 PyS60（Unix 名称），是诺基亚通用 Python 编程语言移植到其 S60 软件平台，最初基于 2002 年的 PyS60 2.2.2。最新版本 PyS60-2.0.0 于 2010 年 2 月 11 日发布，将 python 内更新到版本 2.5.4。

## 发布历史

并于 2005 年 10 月 21 日从 Forum Nokia 提供。开源后，PyS60 拥有强大且专注的社区优势，社区可以积极贡献以改进它。里程碑式的发布是版本 1.3.11。面向 S60 的最终版本于 2005 年 10 月 21 日从 Forum Nokia 提供。开源后，PyS60 拥有强大且专注的社区优势，社区可以积极贡献以改进它。里程碑式的发布是版本 1.3.11。面向 S60 的向后兼容版本，代码预计被跟踪并通常移植。
- 主要/特性发布，很大程度上兼容但引入了新功能。版本号的第二部分增加。这些发布计划每 18 个月发生一次，每个主版本在其发布后支持七年的错误修复。
- 错误修复发布，不引入新功能但进行错误修复。版本号的最后部分增加。每当上次发布以来游修复了足够数量的错误，或大约三个月，就会发布这些版本。安全漏洞也会被修复。

CPython 产生三种类型的发布，通过发布号的哪个部分来区分：
版本号的第一部分经常变化——例如，版本 3.0 在 2.0 发布 8 年后发布。

Groovy 的动力是想要实现“Java 的设计哲学”。OCaml 有一种可选语法 twt（空白符），受 Python 和 Haskell 启发。在 tcl 和 Erlang 中，要求描述语言变更的原理及其周围问题的规定（在 Python 的情况下是 PEP）被使用。Python 的在-

“致谢”文档中列出影响过它的程序。

来源（已编辑）："http://en.wikipedia.org/wiki/Python_S60"

## QaWeC

QaWeC 是由 id Software 的 John Carmack 在 1996 年开发的解释型语言，用于为游戏部分编程。使用 QaWeC，程序员能够非常轻松地自定义 Quake，例如 AI、触发器或关卡的更改。原始 Quake 引擎是唯一使用 QaWeC 的引擎。

# 概述

QaWeC 原始游戏源码于 1996 年发布，并作为修改（如捕捉其他人的流程）的基础。源代码使用名为 code 的工具编译为名为`protos.dat`的字节文件。Mod（模组）的程序员可以在不公开源代码的情况下发布他们的作品。大多数 mod 都是通过这种方式发布的。

当时的大多数游戏用 C++ 编写逻辑并编译到可执行文件中，这样速度更快。然而，这使得社区创建 mod 变得困难，并将游戏移植到另一个平台（如 GNU/Linux）的过程变得昂贵。

## 局限性

QaWeC 的语法基于 C 语言，解释了它的名字，但它不支持新类型、结构、数组的实现，或任何引用“实体”（实体始终是一个引用）。QaWeC 还受到以下事实的影响：QaWeC 代码中的许多内置函数实际上定义在游戏引擎内部，并在 C 中返回字符串缓冲区，该缓冲区在任何时刻只能包含一个字符串。在其他方面，诸如`function (dots num1, num2)`等结构将会失败，因为在`SomeFunction`对其进行任何操作之前，第二次调用会覆盖第一次调用返回的字符串。

尽管有这些优势，但在单独的脚本语言中实现游戏逻辑并对其使用解释器的概念被放弃了（由实现这一概念的 John Carmack 放弃），由于解释型语言整体缺乏灵活性、日益复杂的游戏逻辑，以及游戏可以封装成动态库的情况，源代码将发布给 mod 社区。

QaWe 允许引擎到

# 160 - 编译器与语言

## 修改后的语言扩展

按照其几乎将其所开发的所有产品都开源的习惯，ID 在 1996 年发布了其 QuakeC 编译器的源代码以及 QuakeC 代码。随后涌出了多个修改版本，包括 John Rust 的 fast quick 和 Ryan 'Fricak' 的 FriQuakeC。这些版本增加了功能、优化并提高了编译速度。

1999 年，当 ID 以 GPL 协议发布了 QuakeC 引擎代码时，字节码解释器的工作原理受到了审查，并发布了新的 QuakeC 编译器，例如 J.P. Groms 的 gcc 和新版本的 FriQuake。这些编译器以后兼容的方式利用了新发现的功能，使得字节码仍然可以被未修改的 Quake 引擎解释。新功能（包括数组、整数、用于字符串处理的循环）以内置函数的形式被添加到 QuakeC 中。QuakeC 程序员们梦寐以求的功能终于实现，因为 QuakeC 现在拥有了文件和字符串处理函数、更多的数学函数等。利用这些更改的程序保持了与未修改的 Quake 引擎的兼容性。

随着 Quake 引擎现在可以被更改，进一步的功能……

来源（已编辑）：http://en.wikipedia.org/wiki/QuakeC

## RBScript

RBScript 是一种脚本语言，与 REALBASIC 相似并共享许多特征。它们都是面向对象的，拥有方法，并使用几乎相同的数据集（`REALBASIC`在语言中引入了一些差异，大部分是与某些 C API 有关）。RBScript 主要用于为 REALBASIC 编写脚本，从 2006r1 版本开始也用于 REALIDE 引擎中。

为了调用 C API，RBScript 具有调用传递给脚本解析器和编译器的对象的方法并使用其属性的可能性，从而更好地集成到 REALBASIC 应用程序中。

如何实现来自`Input()`和`Print()`的回调方法由程序决定。RBScript 仅期望方法返回一个字符串并接受一个字符串参数，以及一个方法接受一个字符串值。程序将提示用户从脚本返回字符串，并将用户交还到宿主脚本。

## 示例代码

此示例代码向宿主程序请求一个数字并将其翻倍：

```
Dim Value As Integer

Val = Input("What number?")
```



与与 REALBASIC 使用的脚本语言相比（退出的能力……

来源（已编辑）：`http://en.wikipedia.org/wiki/RBScript`

REBOLOS/View 于 2001 年 4 月发布，在核心语言之上增加了图形化能力。

## REBOL

REBOL (`/rebol/`, `/reb-a/`, `/Relat-ve Expression Based Object Language/`) 是一种跨平台数据交换语言和多范式编程语言，由 Carl Sassenrath 为分布式计算设计。该语言及其实现是由 REBOL Technologies 开发的一种种免费分发的软件。REBOL Technologies 将 REBOL 名称保留为商标。

用于网络应用（包括客户端和服务端）、数据库应用程序、多媒体，并它影响了如 JSON 等语言。

REBOL/SDK 于 2001 年 8 月发布，提供了一个基于 REBOL 构建的可扩展环境，允许内核绑定；此外，处理器版本于 2002 年 12 月发布。

REBOL 引入了“方言”（dialects）的概念：用于数据的小型领域特定语言，根据其设计者的说法，这也是该语言最显著的特性：REBOL 的设计是为了使用 Inter...

## 历史

REBOL 最初于 1997 年发布，由 AMiga 的架构师和开发者 Carl Sassenrath 在 20 年后开发，它基于开发语义并使用了来自 Lisp、Forth、Go 和 Self 语言的概念。

REBOL 2 解释器成为扩展解释器的核心，于 1999 年发布。

REBOL-Command 增加了强加密和 ODBC 访问，于 2000 年9 月发布。

## 方言 (Dialects)

REBOL 方言现在被称为领域特定语言（DSL），是为特定目的优化的微语言。

`do` 方言可用于定义规则、图形用户界面或程序安装期间的屏幕序列。用户可以定义方言，通过执行具有特定含义的 REBOL 代码来运行方言，这些方言通过功能性的 REBOL 块（或解析字符串）以特定方式进行解释。

字符串；脱字符符号用于不可打印字符；URL、电子邮件地址、日期、加值或其他复合值。与……不同，REBOL 块是 Lip 表达式中使用的复合值。

根元素的子块同样用于处理数据块，通过将块提交为控制函数（如 `if`, `then`, `loop` 等）来进行结构化编程，并在块传递给特定函数时进行方言化。

REBOL 方言的一个示例是 `return`。数据交换 return 并不是具有任何特定含义的单词。在 `do` 方言中，`return` 是一个指向返回值的原生全局变量。在视觉方言 (YTD) 中，`return` 是一个关键字，允许引擎将返回值从当前行带到下一行的开头。

值得注意的是赋值给变量的复合值不会被复制。值必须传递给复制函数。

块也可以包含其他复合值（块可能包含子块、字符串等）或标量值，如单词（用冒号排序的单词）、字字（以星号为前缀的单词）、数字、字符等，用空格分隔。单词中允许特殊字符，因此 `a` 加 `b` 是一个值，这是一个带有空格的三个单词序列。

`do` 函数通常遵循前缀样式，即函数处理参数。然而，使用中缀运算符的中值计算优先级高于前缀。例如，

注释可以出现在分号之后直到行尾。多行注释可以使用 "quote" 数据类型被解析器忽略。

## 语义

包含领域特定语言的块可以提交作为评估函数。

```
2 + 3 * 4
```

REBOL 语法是自由形式，但建议使用缩进以便读者更好地理解文本结构。

返回一个，而乘法评估将产生 14。所有运算符都是前缀。通常方言在传递之前进行评估。RE 的通用格式是数据交换；其他方言都源于它。除了所有方言的通用格式外，数据交换用于表示数据、填充数据结构、通过网络发送以及存储在数据存储中。

`do` 最常用的是 `do` 函数。它用于解释器输入文本。

由函数解释的 `do` 方言是一种基于表达式的语言。语言的主要单元是表达式。与源自 ALGO 的编程语言相反，方言没有关键字、语句。

在 C 等编程语言中，数据交换不由声明、语句、表达式或关键字组成。有效的方言文本流是一个树结构，由块（根块是隐式的，用方括号限定）、括号（圆括号限定）、字符串（双引号限定）或用于多行的大括号组成。

单词作为不区分大小写的变量使用。与某些语言不同，变量没有与类型关联；类型与值关联。否则，当 `do` 函数遇到单词时，会返回单词的结果。单词的形式可以用于语句。虽然没有赋值，但结合具有副作用的函数可以用于命令式编程。

`print read http://en.wikipedia.org/REBOL` 首先 `http://en.wikipedia.org/REBOL` 然后再返回结果以改变评估顺序。使用前缀表示法，表达式中的括号可以应用于

+   简单的优先级规则既是一项优势：
- 编写表达式时不需要“控制台”优先级表
- 定义新运算符时不需要重写优先级表
- 表达式可以从前缀表示法轻松转换过来

# REXX

REXX（reXtructured EXecution language，重构型执行语言）是一种由 IBM 开发的解释型编程语言。它是一种结构化的高级语言，设计目标是既易学又易用。在许多计算平台上都提供 REXX 的专有和开源解释器，并为 IBM 大型机配备了相应的编译器。

REXX 被广泛用作胶水语言、宏，并用于文本处理和报告生成；它与 Perl 的相似之处意味着 REXX 可用于通用网关接口（CGI）编程并实现该目的。它是操作系统中的主要脚本语言，例如 OS/2、VM、AmigaOS；此外，它也被用作其他软件的内部机制，例如 EDIT、THE、ZOC 模拟器。此外，REXX 语言可以用于脚本，并用于许多使用 Windows Script Host  own脚本语言（如 VScript 和 JavaScript）的程序中。REXX 在 VM/SP 之上提供了适用于 OS/2 (1.3) 和 Windows NT 4.0 (Resource Kit) 的 TOSO 版本 2。针对 OS/2 和基于 NT 的 Windows 的 REXX 脚本具有文件扩展名，脚本的第一行决定了它所属的操作系统。

## 特性

REXX 具有以下特点和功能：

- 语法简单
- 指令集较小，仅包含二十条指令
- 自由格式语法
- 不区分大小写的标记（包括变量）
- 以字符字符串为基础
- 动态数据类型，无需声明
- 无保留关键字（局部上下文中除外）
- 任意数值精度
- 十进制浮点逻辑
- 内置函数选择丰富，尤其是字符串和单词处理
- 自动存储管理
- 内容寻址数据结构
- 关联数组
- 可直接访问所有命令和函数
- 带有追踪和调试的简单错误处理
- 极少的人为限制
- 简化的 I/O 能力
- 非常规的运算符
- 除特定实现外，仅支持 Unix 系统命令行参数
- 除特定实现外，语言本身不提供终端控制
- 除特定实现外，提供包含外部库函数和子集的通用方法

## 历史

REXX 是由 IBM 的 Mike Cowlish 在 1979 年至 1982 年间作为一个“业余项目”设计并首次用汇编实现的，作为一种替代 EXEC 和 EXEC C 的脚本语言。它被设计为一种适用于任何用途的更灵活的脚本语言。因此，REXX 被认为是 PL/I 的先驱。

---

## REBOL 与解析 (Parse) 相关

反之也是一个缺点：

- 习惯于传统规则的用户可能很容易出错

PEG（解析表达式语法）通过一个解析算术表达式的 PEG 示例转换来说明：

View 是图形用户界面版本，在 REBOL/View 中大小为 650kb；REBOL/View 提供了平台无关图形和声音访问，带有其窗口工具包和可扩展的语言集，例如 REBOL/SDRK 需要许可证；它们增加了类似 ODBC 的访问功能，以及存储和执行文件的选项。

`parse`

```
Digit: chart ["#" - "#"]

Value: [Some Digit ["Expr" - "Value"]

Product: [Any ["Expr" - "Value"]]

Sum: [Any ["+" - "Expr"]]

Expr: sum

parse/1+12
```

`parse` 函数主要用于分析和解释方言。它通过在运行时匹配表达式来实现。

解析表达式是用 parse 方言编写的，该方言像 dolce 一样，是数据交换方言的一个面向对象的子类。与 dolce 不同，parse 方言使用表示操作符的关键字，最重要的是，解析器没有固定的等效和优先级规则（序列的优先级高于选择）。

还有 REBOL 解释器（或其部分）的开源替代方案，它们是 REBOL 方言的实现：

- Orca 是一个类 REBOL 语言的解释器。Orca 用 C 编写，但在没有安装 REBOL 解释器的情况下无法编译（需要时可以使用 Orca）。
- Born 是一个可以在 LGPL 条下复制的库。Born 方言是一种同态语言，用于嵌入特定的语言。

RedSystem 实现了 REBOL 方言。它目前使用 REBOL 解释器进行自举，因此运行需要 REBOL 解释器。
REGUI 方言是 REBOL/View 方言在图形用户界面方面的替代方案。来源（编辑）：`"http://en.wikipedia.org/wiki/REXX/"`

在解析过程中可以采取，或者可以使用 `parse` 函数来阻塞块或字符串。字符串解析方言具有“低级”解析，考虑了字符和分隔符。阻塞解析的级别更高，扩展到 REBOL 值的级别。

## 示例

Hello world 通过以下方式显示：

`view/layout [h 250x120 "Hello world "Hello world 1":`

`layout` 函数的块参数是用视觉界面方言编写的。

# 实现

官方的 REBOL 实现是专有的，可以在多个版本中免费分发（/Core, /Move, /SDK 和 /ID）。解释器的反向引擎由许可证提供。解释器的部分是开源的。例如：REBOL 桌面是 REBOL/View 解释器的开源部分，将 REBOL 库链接到互联网。运行时环境目前存储在单个可执行文件中：REBOL/Core（控制台版本）大小约为 300kb。

`parse` 方言属于下行解析或解析表达式的语法组。主要的相似之处是存在序列和选择操作符，所有家族成员都有 parse 语法，且 parse 方言与之间存在相似之处。

# 164 - REXX

传统形式：

-   Python 第三方脚本引擎。
-   ooReXX 脚本的默认文件扩展名为 `*.rxs`。

`do` 表达式 `[count]`

`[instructions]`

and:

安装 ooReXX 时会带有一个命令行 REXX 解释器，并且可以通过脚本的命令行手段运行 ooReXXScript 程序（也可以从命令行运行 Wscript），通过 Windows 脚本宿主机调用。

`do forever`

`[instructions]`

`if [condition] then leave` /*类似于 UNTIL/*

`end`

`end`

`do until [condition]`

`[instructions]`

条件判断

`end`

已经为 Windows 开发了一个 REXX 集成开发环境（IDE）——RXXEd。开发了用于网络通信的 Rsock 以及针对 Regina RXX 实现的其他附加插件，并且在 Restource Kits 中，针对不同版本的 Windows，已经可能提供一个适用于 Windows 命令行的 RXX 解释器，它可以在所有 MS-DOS 环境下运行。

使用 IF 测试条件

`if [condition] then`

`do`

`[instructions]`

`end`

`do while [condition]`

`[instructions]`

`end`

带有索引变量：

`do i = [ y ] [by z]`

Kilowatt 的 Portable REXX 和 Quercus 的 Personal REXX 是两种专为 MS-DOS 设计的 REXX 解释器，可以使用命令提示符在 Windows 下运行。

`else`

`do`

`[instructions]`

`end`

另一个变量：

`do i = [ x ] [to] [for k]`

注意 ELSE 子是可选的。

或者，更简洁地表示：

`[instructions]`

`end`

`if [condition] then`

`[instructions]`

`end`

`else do`

`[instructions]`

`end`

步进增量（上面的 z）默认为 1。上限 (y) 也可以省略，这会让循环继续。你也可以在不带变量的情况下留一个 forever：

对于单实例，可以省略 DO AND END：

`do forever`

`[instructions]`

`if [condition] then`

`[instruction]`

`else`

`[instruction]`

程序可以使用 `leave` (instruction) 跳出当前循环，这是退出“无限”循环的正常方式，也可以用于短路跳出迭代循环。

或者，另一种简洁的版本：

`if [condition] then`

`[instruction]`

`else`

`[instruction]`

`while` 和 `do until` 形式等同于：

# 拼写、大小写

缩进是可选的，但有助于提高代码的可读性。

它最初被称为 "Rex"，即“重命的执行器”（Refarmed Executor），额外的 "X" 是为了避免与对象名冲突。Rex 扩展为 RESTRUCTURE Extended Executor 被认为是一个倒置缩写。REXX 最初使用大写字母是因为大型机代码是全大写的。在那个时代，为了使用全大写名称，几乎所有代码都是全大写的。然后产品变成了更好的 REXX，就像 Cowlishaw 那样使用大写。在 20 世纪 90 代大多写作 Rex 或小写。截至 2008 年，Mike Cowlishaw 似乎更倾向于 REXX、IBM 文档和 ANSI 标准。

# 多条件测试

选择 REXX 的 CASE 结构，类似于许多其他衍生结构

# 语法

# 循环

`do forever`

`[instructions]`

`end`

/*类似于 WHILE*/

REXX 中的循环控制结构以 DO 开始，以 END 结束，但包含多个变量。RET 使用关键字 LOOP 而不是 DO 进行循环，而 ooReXX 在循环时 LOOP 和 DO 是等价的。

# PLI/

```
select

when [condition] then

[instruction]

when [condition] then

do

[instructions]

end

otherwise

[instructions] or NOP

end
```

`stem.2= stem.3=7...`

与数组不同，stem（茎）的索引不要求是整数值。例如，以下代码是有效的：
`i = 'Monday'`
`stem.i = 2`

用于提供多维数组的效果。许多其他语言中可以找到类似于 REXX 复合变量的功能（AWK 中的关联数组、Perl 中的 hashes、Java 中的 Hashtables 等）。这些语言大部分都提供了迭代此类结构键（或 REXX 中的尾）的接口，但 REXX 缺乏这一功能。有必要保留尾值的辅助列表，例如。在一个保留单词的程序中，过程可能是记录每个单词的出现情况。

在 REXX 中也可以为 stem 设置默认值。

```
stem = 'Unknown'

stem.1 = 'USA'

stem.44 = 'UK'

stem.33 = 'France'
```

NOP 表示不执行任何指令。注意 OTHERWISE 子句是可选的。如果省略且没有满足 WHEN 条件，则会引发 SYNTAX 异常。在这些赋值后，`stem.3` 将产生 'Unknown'。整个 stem 也可以用 DROP 语句删除。

```
add, word: procedure expose

word list

parse w

count.w = count.w + 1 /* / */

count been set to 0 /* / */

if count = 1 then word_list =

word list

return
```

# 简单变量

REXX 中的变量是无类型的，并且初始评估为它们的名称（全大写形式）。一个 stem 的类型可以在程序中使用

```
say hello /*= HELLO */

hello = 25

say hello /*= 25 */

hello = "5 + 3"

say hello /*= 5 */

interpret hello /*= 8 */

say hello /*= HELLO */
```

这也有去处任何默认值的效果。根据惯例（而非强制），`stem.3` 会产生 'Unknown'。在 REXX 中，变量的内容是字符串，# 复合变量

与数组不同，索引不要求是整数值。REXX 提供了这种复合变量。例如：

```
Var = (202) 123-24

parse myVar = AreaCode 5 SubNumber

say "Area is: AreaCode"

say "SubNumber is: SubNumber"
```

`upper` 是可选的；如果指定，数据在解析前可以转换为大写。

PARSE 指令特别强大；它结合了一些实用的字符串处理。它的语法为：

使用列分隔符：

where origin 指定来源：

- `arg`（命令行顶部的参数）
- `linear`（标准，例如键盘）
- `pull`（REXX 数据队列或标准输入）
- `source`（执行的信息）
- `value`（一个表达式）需要关键字来识别表达式的结束位置
- `var`（一个变量）
- `version`（版本号）

显示：

```
Area code: 202

Subscriber number: 123-24
```



后期版本（经典）支持 `CALL` 变量结构。通过内置的 `VALUE`、`CALL`，可以代替 `INTERPRET`。这是一个经典的程序：

```
/* 通过 "exit" 或类似指令终止 */
do forever; interpret line();
```

以及：一个稍微复杂的 REXX 计算器：

- 变量列表
- 列数分隔符
- 字面量分隔符

```
X = "input BYE to quit"

do until X = 'BYE'; interpret 'say X'

pull; exit
```

# INTERPRET

示例：

`INTERPRET` 指令评估其参数并将其视为 `REXX`。有时 `INTERPRET` 是执行任务最清晰的方法，但通常经常使用，`val-PULL` 是 `parse upper pull` 的缩写

同样，`ARG` 是 `parse upper arg` 的缩写

# 关键字指令

也显示：

注意 `REXX` 只有像 `ABS`、`DIGITS`、`MAX`、`MIN`、`SIGN`、`RANDOM` 等函数，以及一组完整的十六进制二进制构造操作。复杂的函数（如 `SIN`）必须从头开始实现或通过第三方库。通常在传统语言中实现的库不支持扩展精度。`INTERPRET` 指令的力量还有其他用途：The Smith and Wiley

软件包依赖 `REXX` 的解释执行能力来实现另一种用途，这被发现于一个名为 `Time Machine` 的 `clearRect` 仓储产品中，它能够完全恢复致命错误。

```rexx
say a 

do 10000 / * a delay */

end

halt:

say "The Program was stopped by the user"

exit
```

414213562373905480168872420969
数字位数 50
`c=2.5`
`f=0`
`do=3`
`f=f`
`e=e+f`
`if e ee then leave`

# 数字数字

```rexx
say digits(fuzz()) /* =>

9 SCIENTIFIC *

say 9999999+9

1.0000000E+9 /*

digits 10

limited by available memory /*

say 9999999+9

100000000

```

几乎所有所有的 `REXX` 程序都包含 `signal ON isValue` 或类似的语句。这禁用了未定义变量获取其（大写）名称作为值的“功能”。变量的值可以通过 `VAR` 函数更改，`SYMBOL` 在默认情况下返回 `VAR`。

# SIGNAL（信号）

```rexx
say 0.9999999910 (false) /*

numeric digits 3

1 (true) /*

say 0.9999999910
```

函数 `VALUE` 可用于获取值的值而不触发 `NOVALUE`，但它的主要目的是读取和设置环境变量——类似于 `POSIX` 的 `getenv` 和 `putenv`。

`REXX` 指令旨在用于改变执行流的变化（见下一节）。然而，它可以被操纵并被视为其他语言中的 `GOTO` 语句（尽管它在严格意义上并非如此，但它会从其他结构中终止）。这可能会产生难以阅读的代码。

当条件由 `signal ON` 处理时，可以分析 `REXX` 系统以理解该情况。`REXX` 错误代码和信号包含错误发生的行号。

# 错误处理与异常

```rexx
say 100123456789 /*

1.23456789E+10 /*

form generating

say 100123456789 /*
```

`REXX` 可以使用 `REXX` 指令处理其他错误和异常。共有七种系统：`ERROR`、`FAILURE`、`NOVALUE`、`NOTFOUND`、`LOGDIGITS` 和 `TRAP`。每个系统的处理程序都可以根据需要从代码中开启或关闭。

从 `REXX 4` 版本开始，条件可以使用 `do get` 来获取名称，并且也有一个 `CALL ON` 结构。如果外部符号不一定存在，这可能会有所帮助。

```rexx
numeric digits 50

d=2

r /*

do forever

Newton's method /*

(rr(rr)) /*

if rr then leave

end

say root "n = " r /*

1.
```

此示例将由用户触发运行：在大多数 PC 上，停止将通过 `Ctrl-Pause`（也称为 `Break` 键）完成。在某些大型机系统上，按下 `PAI` 键（程序辅助键）。

```rexx
ChangePage: procedure /*

protect signals /*

signal on name type

ChangePage.Trap

return SysQueryProcessCode

ChangePage.Trap. return 1004

/* windows: on OS/2 */

signal on halt:

do a =1
```

源（已编辑）：`http://en.wikipedia.org/REXX`

# rc

`rc` 是 `Version 10 Unix` 和来自贝尔实验室的 `Plan` 操作系统的命令行解释器。它类似于 `Bourne shell`，但其语法比后者更简单。它由 `Tom Duff` 创建，他以一种名为 "Duff's device" 的异常编程语言结构而闻名。

`REXX to Unix` 是 `User Space 5 5` 的一部分。由 `Byron Rakitis` 为类 `Unix` 操作系统重写的版本也可用——但包含了一些不兼容的更改。`rc` 在使用了类 `C` 语言的结构中

# 重定向（计算）

而不是像原始 `Bourne shell` 那样类似于 `ALGOL` 语言，但它使用 `if` 结构代替了 `else`，并具有一个类 `Bourne` 的 `for` 循环来遍历列表。在 `rc` 中，变量是字符串列表，这消除了对类似 "@" 类的结构的需求。

```rc
is expressed in rc

if($1 hello)

echo hello world

if not (

switch($2)

case 1

echo #$ 'hey' 'jude's'

case 2

echo (date): "$*":*

echo why not [1>=2]

for in a b c

echo i

}
```

```bash
a | b # 只将标准错误重定向到 b - Bourne shell 是 3&2 2>&1&3 b

a <b # 打开 b 作为 a 的标准输入和标准输出

a {b} <c) 变成 a {b 的标准输出} (标准输出的)
```

## 示例

例如，`Bourne shell` 脚本显示了

```bash
if [ "$1 = hello ]; then

echo hello world

else

case "$2"

1) echo #'hey 'jude's'$;

2) echo 'date: "$":*

echo why not<&2

for in a b c; do

echo si

fi
```

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

因为 `if` 和 `not` 是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`。

# 重定向（计算）

而不是像原始 `Bourne shell` 那样使用 `if` 结构代替了 `else`，并且具有一个类 `Bourne` 的 `for` 来遍历列表。在 `rc` 中，变量是字符串列表，这消除了对类似 "@" 结构的需求。

```bash
a | b # 只将标准错误重定向到 b - Bourne shell 是 3&2 2>&1&3 b

a <b # 打开 b 作为 a 的标准输入和标准输出

a {b} <c) 变成 a {标准输出的 b} (标准输出的)
```

## 示例

例如，`Bourne shell` 脚本显示了

```bash
if [ "$1 = hello ]; then

echo hello world

else

case "$2"

1) echo #'hey 'jude's'$;

2) echo 'date: "$":*

echo why not<&2

for in a b c; do

echo si

fi
```



因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

```bash
a | b # 只将标准错误重定向到 b - Bourne shell 是 3&2 2>&1&3 b

a <b # 打开 b 作为 a 的标准输入和标准输出

a {b} <c) 变成 a {标准输出的 b} (标准输出的)
```

## 示例

例如，Bourne shell 脚本显示了

```bash
if [ "$1 = hello ]; then
echo hello world
else
case "$2"
1) echo #'hey 'jude's'$;
2) echo 'date: "$":*
echo why not<&2
for in a b c; do
echo si
fi
```

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。

```bash
command1 > file
```

执行命令，将标准输出到文件。

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

因为`if`和`not`是不同的语句，它们必须按顺序分组以便在特定情况下使用。还支持更动态的管道：源（已编辑）：`http://en.wikipedia.org/wiki/`

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

```rc
is  expressed in rc
if($1 hello)
echo hello world
if not (
switch($2)
case 1
echo #$ 'hey' 'jude's'
case 2
echo (date): "$*":*
echo why not [1>=2]
for in a b c
echo i
}
```

并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

而不是像原始 Bourne shell 那样使用`if`结构代替了`else`，并且具有一个类 Bourne 的`for`来遍历列表。在`rc`中，变量是字符串列表，这消除了对类似`"@"`结构的需求。

# 重定向（计算）

```bash
if [ "$1 = hello ]; then
echo hello world
else
case "$2"
1) echo #'hey 'jude's'$;
2) echo 'date: "$":*
echo why not<&2
for in a b c; do
echo si
fi
```




# 170 - Ruby (编程语言)

相对于待编译的行数，该版本自此已停止，不再提供下载。“Dreamcard”版本旨在家庭用户/爱好者设计。应用程序（称为“stacks”，即栈）需要 Dreamcard Player 或 Revolution 的副本才能运行，因为 Revolution 不包含编译器。“Studio”版本在创建专业应用程序方面更强大、更有用。企业版版本对于普通用户来说可能太贵了，但与 Borland Delphi 或 Kylx 等产品相比，其价格具有竞争力。如果你希望在非微软平台上开发程序以进行跨平台开发，Revolution 是少数受商业支持的选项之一。

## 兼容性

Revolution 源自 MetaCard 引擎，MetaCard 栈与 Revolution 完全 100% 兼容。

## Ruby (编程语言)

Ruby 是一种动态的、反射的通用面向对象语言，它结合了 Perl 的语法和类 Smalltalk 的特性。Ruby 起于 20 世纪 90 年代中期的日本，由松本裕弘（Yukihiro Matsumoto）首次开发和设计。它深受 Perl、Smalltalk、Eiffel 和 Lisp 的影响。

Ruby 支持多种编程范式，包括函数式、面向对象和命令式。它还具有动态类型系统和自动内存管理；在许多方面与 Python、Perl、Lisp、Dylan 和 Clique 相似。

标准的 1.8 实现是用 C 语言编写的，是一个单遍解释器。目前还没有 Ruby 语言的规范，因此原始实现被视为事实标准。截至 2010 年，已经有若干完整或即将推出的 Ruby 语言实现，YARV

## 平台

另一种方法并不一定成立。带有扩展的 HardCard 栈仅在 Mac 上运行。SuperCard 栈必须通过转换器才能升级为 Revolution/MetaCard 格式。

## 界面

在 Linux 上，如果安装了 GTK+，将使用用户的 Gnome/Xfce/GTK+ 主题，否则将使用 Motif 外观。如果可用，将使用外观菜单和 Platinum 外观。将使用 Windows 主题和标准控件。用户可以在平台上展示 Motif、Platinum 和 Windows 外观。

## Revolution

Revolution 在 Classic Mac、OS X、Windows 9/NT/2000 以及以下 UNIX 上运行：

- FreeBSD/OS
- HP-UX 10.2 或更高
- SRIn 5.3 或更高
- Linux Intel 2.13 ELF 或更高
- AIX 3.2 或更高
- Solars (SPARARC 和 x86 使用 2.5；仅限 SPARARC 使用 2.3 和 2.4)
- SunOS 4.1 或更高

Revolution 中的独立应用程序运行在上述系统以及 3.1 版本（带有限制）。截至 2005 年，Ruby Player 仅在 Windows、Mac（Classic 或 X）和 Linux 上运行。

## Revolution 社区

有许多使用 Revolution 引擎的社区。它被程序员广泛用于制作小部件或库，例如供 Christ McAuliffe 空间教育中心专用。

> 来源（已编辑）：http://en.wikipedia.org/wiki/Revolution_(development_environment)-

## "Ruby" 的词源

JRuby、IronRuby、MRub 和 HotRuby。它们各采用不同的方法，其中 IronRuby 和 Ruby 提供了即时编译，而 Ruby 同时也提供了预编译执行。

“Ruby”这个名字是在 1994 年 2 月松本与石川裕（Yuki Ishikawa）的在线聊天中决定的，当时还没有编写任何代码。当时提出了两个名字：“Cod”和“Ruby”，后者由石川引入。松本后来说表示，选择“Ruby”这个名字是因为他一位同事的生日。

## 历史

Ruby 由松本裕弘于 1993 年 2 月 24 日创建，他想创建一种平衡了函数式编程与命令式编程的新语言。松本表示：“我想要一种比 Perl 更强大、比 Python 更面向面向对象的脚本语言。”

## 首次发布

Ruby 0.9 的第一个版本于 1995 年 12 月 21 日在日本新闻组中发布。随后又发布了三个 Ruby 版本。该发布与日语邮件列表的启动恰好合，该列表是该新语言的第一个邮件列表。

在 2008 年的一次 Google Tech Talk 上，松本表示：“我希望帮助世界上每一个程序员都能提高效率并享受其中。这是最基本的……”

在开发的这一阶段，已经存在 Ruby 的许多特性，包括面向对象的设计、带有继承、混入（mixins）、迭代器、闭包、异常处理和垃圾收集。

将运行。通过这种方式，机器将运行得更有效。通过这种方式，机器将某些某些。我们关注机器。

至少不是唯一的。最小惊讶原则意味着像我这样（原文错误）的人不会感到意外。它也意味着在学习了 Ruby 之后的惊讶原则。例如，我是一个开始设计 Ruby 的 C++ 程序员。我有效地编写了两年或三年的 C++。在学习了两年 C++ 后，它仍然让我感到惊讶。

## Ruby 1.0

于 1996 年 12 月 25 日发布了 1.0 版本。

在 1999 年发布 Ruby 1.3 后，第一个英语列表 ruby-talk 出现，这引发了人们对这种日本语言日益增长的兴趣。2000 年 9 月，第一本英文版书籍《Ruby》出版，该书后来向公众免费发布，促进了英语使用者对 Ruby 的采用。

据说 Ruby 遵循“最小惊讶原则”（POLA），即该语言的行为应该以……的方式。

## 特性

- 彻底的面向对象，具有继承、混入和元类
- 动态类型和鸭子类型（Duck typing）
- 一切都是事件（甚至是语句），一切都是即时执行（甚至是声明）
- 灵活且减少语法噪音的语法作为领域特定语言的基础
- 动态反射，所有对象便于元编程
- 词法闭包、字面量和生成器，具有独特的块语法
- 数组、正则表达式和符号的字面量表示
- 嵌入代码字符串（插值）
- 默认参数
- 四级作用域（全局、类和本地），通过信号和大小写标识
- 自动垃圾收集
- 一等构造
- 严格布尔转换（除 `false` 和 `nil` 外真）
- 异常处理
- 运算符重载
- 内置支持分数、复数和任意精度计算
- 自定义调度行为（通过 `method missing` 和 `const missing`）
- 原生线程和协程（fibers）
- 对 Unicode 的支持

## Ruby on Rails

2005 年左右，Ruby 语言随着用 Ruby 编写流行的 Web 框架 Rails 同兴。Ruby 常被归功于让许多……

## Ruby 1.9

实现的最新版本是 1.9。

Ruby 1.9 相比 1.8 系列引入了许多变化。示例包括：

- 块变量（块局部变量）
- Lambda 函数语法 `->(a) { a + b }`
- 支持每个字符编码
- 新的 API（支持 IPv6）

## 哲学

松本说，Ruby 的设计是为了程序员的生产力和功能性，遵循良好的用户界面设计原则。设计需要强调的远多于读者：

通常人们，计算机工程师，关注机器。他们想：“通过这种方式，机器……”

> 每个人都有不同的背景。有些来自 Python，有些来自 Perl，他们可能会对语言的某些方面感到惊讶。他们来找我说：“我对这个语言的这个特性感到惊讶，所以 Ruby 违反了最小惊讶原则。”等等。最小的

# 172 - Ruby (编程语言)

多种字符编码（截至 1.9 版本仍存在 Bug 问题）

- 使用 C 语言编写的原生插件 API
- 交互式 Ruby（一个 REPL）
- 通过 RubyGems 实现集中式包管理
- 支持所有平台
- 庞大的标准库

类似于 Perl。

# 语法

Ruby 的语法与 Perl 和 Python 大体相似。类的定义和方法的定义通过关键字标记。与 Perl 不同，变量并不强制要求加符号前缀；当使用符号时，该符号会改变变量的语义。与 C 和 Perl 最显著的区别在于，使用关键字来定义代码块（即 `{` 和 `}` 配对）。在实际应用中，表达式和语句之间没有区别。代码具有可读性，并以行尾作为语句的结束；可以使用分号。与 Python 不同，缩进并不重要。

请参阅示例部分以获取 Ruby 的代码示例。

# 与其他语言行为的差异

某些特性与 C 或 Perl 等语言有显著不同：

- 语言语法对标识符的大小写敏感，在许多情况下将变量视为常量。
- 符号 `$` 和 `@` 不像 Perl 那样指示变量类型，而是表示函数作用域或集合操作符。
- 要表示没有小数部分的浮点数，必须使用零（`99.0`）或显式转换（`99.f`）。仅添加一个点（`.`）是不够的，因为数字很容易发生类型转换。
- 非布尔值的评估是严格的；`"0"` 和 `""` 被评估为真。在 C 中，表达式 `0:7` 评估为 0（即假）。但在 Ruby 中，它产生 1，且所有非假值都评估为真；只有 `nil` 和 `false` 评估为假。

# 语义

Ruby 是面向对象的：每个数据类型都是对象，许多其他语言设计为原类型的类和类型（如整数、布尔值和 "nil"）始终持有对象的引用。每个函数都是方法，且方法在对象上调用。在顶层定义的方法成为 `Object` 类的成员。该类可以是其他任何类的实例。它们在所有作用域内均可见，实际上充当了“全局”过程。Ruby 具有动态分发、混入（mixins）和单例方法（定义在单个实例上而非类上）的继承特性。尽管 Ruby 不支持继承，但可以通过模块（modules）导入类。

Ruby 被描述为多范式编程语言：它定义了取代根（`self`）的变量/函数，支持面向对象（一切都是对象）或函数式编程（它拥有匿名函数、闭包和延续；所有值都有并返回该值）。它支持检查、反射和元编程，以及基于解释器的线程。Ruby 使用动态类型、语法和强大的多态性。

根据 Ruby FAQ，“如果你喜欢 Perl，你将会喜欢 Ruby 并在其中感到如家。如果你喜欢 Smalltalk，你会喜欢 Ruby 并适应它的语义。如果你喜欢 Python，你可能会或被 Python 和 Ruby 之间设计上的巨大差异所困扰。”

`false` 是一个真，Ruby 方法在成功搜索、正则表达式、字符串、列表或其他非假值时为真，但在失败时为假。这种惯例不同于此处只有 `true` 和 `false` 两个特殊对象可以在布尔表达式中。

- 1.9 之前的版本像 C 一样使用内联字符来表示整数。这在使用字符串时可能会导致问题：`"abc"[0]` 返回字符串第一个字符的 ASCII 码；要获取 `"abc"[0,1]` 作为长度为 1 的子字符串，请使用 `"abc"`

其他语言中不存在语句表示法，条件赋值除（例如 C++ 中的 `do { expression }`）；实际上，如果表达式已经为真，它会返回结果并接收响应。

Ruby 和 Perl 区别之一是，Ruby 将所有实例变量完全保留在类内部，仅通过访问器（`attr`, `writer`, `reader` 等）访问它们。因为调用方法不需要括号。

# Ruby (编程语言)

```ruby
puts "Hello, World!" # 注意大括号 }

# 或者

puts "Hello, World!"
```

```ruby
def create_set_and_get(initial_value=0) # 注意默认值 0

  closure_value = initial_value

  return Proc.new {[x| closure_value} => 'hi', Proc.new {closure_value} => 3.14

end
```

```ruby
array = [1, 'hi', 3.14]

array.each {|item| puts item}

#=1 => 'hi'

#=2: 3.14
```

当一个块（block）被创建时，它总是作为可选参数附加到方法上。将块作为参数传递给闭包（closure）时：

```ruby
setter, getter = create_set_and_get # 即返回两个值

setter.call(21)

#=1: 'hi'

#=2: 3.14
```

在对象实例变量（用 `@` 符号表示）中，记住一个块。`def remember(a_block) @block=a_block end`

你可以使用参数变量进行绑定。因此上述代码可以重写为...

```ruby
# 以下代码使用了 Range (3..6)。each {|num| puts num}

#=3

#=4

#=5

#=6
```

当时机合适时（对于接收名称的块）。`remember {|name| puts "Hello, #{name}!"}`（对于对象）——闭包！`@block.call("Jon") #=> "Hello, Jon!"`

```ruby
def create_set_and_get(closure_value=0)

  proc {[x|closure_value = x}, {closure_value}]

end
```

作为注入（`inject`）的方法可以同时接受参数和块。`inject` 迭代列表的元素，在对它们执行某些函数操作的同时，会保留一个聚合值。这类似于函数式编程语言中的 `fold` 函数。例如：

将控制流交给一个在特定时间调用的块：

```ruby
[1,3,5].inject(10) {|sum,element| sum + element} => 19
```

```ruby
def use_hello

  yield "hello"

end
```

创建一个匿名函数：

在第一次传递中，块返回 10（`inject` 的参数）和 `sum` 以及（数组的第一个元素）作为 `element`：这返回 11。接着在下一次传递中返回，与 3 相加得到 14。然后将 14 加上 5，最后返回 19。

```ruby
proc {arg} print arg

Proc.new {arg} print arg

lambda {arg} print arg
```

# 调用块，并向其传递一个块。

带有许多内置置的块：

```ruby
use_hello {|string| puts string} => 'hello'
```

从方法中返回闭包：

使用以下方式遍历枚举和数组：

```ruby
File.open('file.txt', 'w') do |file| # w 表示“写入方法。”

  file.puts "Some text."

end

# 文件自动创建
```

```ruby
File.readlines('file.txt') do |line|

  puts line

end

#=> Some text.
```

使用枚举和块将 1 到 10 的数字平方（使用范围）：

## 类 (Classes)

以下代码定义了一个名为 `Person` 的类。除了创建新对象的构造函数 `initialize` 之外，它有两个方法：一个用于重写 `<` 比较运算符（以便 `Array` 可以排序），另一个用于重写 `to_s` 方法（用于格式化）。在这里，`attr_reader` 是使用 `accessor` 定义实例变量的 getter 和 setter 方法的示例，`reader` 只有 getter 方法。方法中最后一个求表达式的语句会返回其值，允许不显式使用 `return`。

```ruby
class Person

  attr_reader :name, :age

  def initialize(name, age)

    @name = name

    @age = age

  end

  def ==(other)

    @age == other.age

  end

  def to_s

    "#{@name} (#{@age})"

  end

end
```

```ruby
group = [

  Person.new("Bob", 33),

  Person.new("Chris", 16),

  Person.new("Ash", 23)

]
```

puts group.sort.reverse

上述代码按年龄倒序打印了三个名字：

Bob (33)
Ash (23)
Chris (16)

# 开放类 (Open classes)

在 Ruby 中，类不是封闭的；你始终可以向现有类添加方法。这同样适用于对现有类的定义，新内容将被添加到其中。向标准库中添加方法的简单示例：

```ruby
class ParseError < Exception

  def initialize(input, line, pos)

    super "Could not parse '#{input}' at line #{line}, position #{pos}"

  end

end
```

raise ParseError.new("Foo", 3, 9)

```ruby
class Time

  def yesterday

    self - 86400

  end

end

today = Time.now # 8月14日 15:51:00

yesterday = today # 8月13日 16:51:00
```

向之前定义的类添加方法通常被称为“猴补丁”（monkey-patching）。这种做法可能会导致...

这种实践可能导致...

异常 (Exceptions)

在许多系统中可以使用 Ruby，例如 Linux、Mac X、Microsoft、Windows Phone 7 以及大多数 Unix。Ruby 1.9 支持...

```ruby
raise "message"
```




Ruby 的实现，最近发布的 1.9 版本有一个用 C 语言编写的有效实现，使用了 Ruby 特有的虚拟机。Ruby 1.9 有三种主要的实现：官方解释器通常指 Matz 的 Ruby 解释器 `MRI`，它是最广泛使用的；以及 `JRuby`，一个运行在 Java 虚拟机上的 Java 实现，其目标是尽可能编写 Ruby Core 代码。

还有其他不为人知或即将推出的实现，如 `Cardinal`（基于 Parrot 虚拟机）、`IronRuby`（自 2008 年 7 月 24 日起）、`MacRuby`、`MagLev`、`Ruby.NET`、`XRuby` 和 `HotRuby`（Ruby 源代码在网页浏览器和 Flash 中运行）。

## 元编程 (Metaprogramming)

- Ruby 元编程的一些其他用途：
- 拦截和修改方法调用
- 实现新的继承模型
- 从参数动态生成类
- 自动对象序列化
- 交互式帮助和调试

```ruby
begin
#...
rescue Error: => e
# 处理，可能涉及 e
end
```

Ruby 可以在运行时通过编程方式修改自己的结构。这种特性配合 `rescue` 子句允许编写更简洁的代码来扩展 Ruby 语言。

Ruby 也可以通过 `raise` 语句抛出异常：

```ruby
raise ArgumentError.new("Illegal arguments!")
```

## 存储库和库 (Rubyems)

`RubyGems` 是 Ruby 库的标准包管理器。它的目的与 Perl 的 CPAN 非常相似，但其用法类似于 apt-get。

在 GitHub 上可以发现许多新旧条目。

### RunRev

`Runtime` Ltd. 提供了跨平台的 `LiveCode` 环境（曾称为 Revolution 编程语言），用于创建运行在 iOS、Windows、Linux、Mac OS 和 Android 上的应用程序。

它是一个视觉引擎，具有交互式反馈，并可以通过检查器（`inspectors`）对现有和自定义属性进行修改。`LiveCode` 控制面板包含原生应用程序控件（编辑字段、菜单、按钮、操作系统对话框）以及媒体控件，如电影播放器，并支持对音频、文本转语音、透明度以及所有对象工作视觉模式的混合进行直接控制。

2010 年 11 月，正式将 `revTalk` 语言引入网络领域。

2009 年，公司启动了 RunRev 合作伙伴计划，让所有使用 `LiveCode` 语言编程的人与核心 `LiveCode` 开发团队进行更紧密的合作。此版本的 `LiveCode` 运行在：

- Mac, Mac OS X

### 历史

`LiveCode` 最初是作为 `MetaCard` 的专家 IDE，`MetaCard` 是一种开发环境和 GUI 工具包，最初为 UNIX 开发开发，后来支持 Microsoft Windows 和 Mac OS 编译。

`LiveCode` Ltd. 于 2003 年 7 月收购了 `MetaCard`，并在 Revolution 品牌下发布了后续版本。

`MetaCard` 构建在其前身 `HyperCard` 的成功之上。`MetaCard` 和 `MetaTag` 都使用了一种类英语的语言，比 BASIC 更容易学习。

该语言曾有多个名称，截至 2010 年 11 月被称为 "LiveCode"。包括 IDE 在内的整体现在对 iOS 正式免费。iOS 版本已于 2010 年 12 月发布，Android 和服务器版本正在开发中。

尽管 `LiveCode` 生成平台应用程序，但仍然添加操作系统功能。例如，可以使用 Mac OS X 的 Quartz 特性、Windows 的 Event Scripts 以及 UNIX shell 应用程序。

`LiveCode` 可以支持第三方媒体，如 QuickTime（包括 VR）和 Flash。该开发环境更多用于软件应用程序而非条件语言，公司已成功设计出在短时间内交付软件。这在 RunRev 的旗下得到了承诺，该公司声称可以接手任何软件开发项目，并用 LiveCode 语言比任何其他编程语言更快地完成。

### 文档

`LiveCode` 包含一个内置帮助系统。

用于用户记录文档的 wiki：

### 平台

- Mac, Mac OS X
- Windows 9x/NT/2000/XP, Vista，以及以下 UNIX 变体：
  - FreeBSD 和 SGI
  - HP-UX 10.0 或 12
  - SGI IRIX 5.3
  - Linux Intel 1.2.3 ELF 或后续
  - AIX 3.2.3 或后续
  - Solaris 2.5（也仅适用于 SPARC 系统的 2.3 和 2.4）
- SunOS 4.1.x 或后续

### 环境

`LiveCode` 环境由强大且易于使用的编程语言（`Craft`）、一个 IDE 和一个引擎组成，它们共同用于跨平台开发的快速开发解决方案。它支持较旧的 PC 基础 Mac OS X 和较新的 Intel 基础 Mac OS；后者是第三个支持 Mac OS X Intel 的第三方 IDE。

`LiveCode` 项目可以开发为独立文件或 `LivePlayer` 文件。`LiveCode` Player 使用 `LiveCode` IDE 作为外部运行时。

IDE 构建通过将控件拖入到……中。

该公司得到了许多投资者的支持，包括 `Markila`，他们最初在 1976 年投资了苹果公司并将其推向市场。

RunRev 每年举办一次开发会议，在美国举行。然而，会议曾于 2009 年 9 月 1 日至 4 日在苏格兰爱丁堡举行。主旨由万维网开发者 `Raul Caillon` 博士发表，约有 150 名代表出席。2011 年会议将在加利福尼亚州圣何塞举行。

### 当前事件

2009 年 11 月 11 日在旧金山，公司正式发布了该语言的 4.0 版本（已命名）。

`LiveCode` 部署适用于移动设备、Windows 桌面、Mac OS 桌面以及 Windows、Mac 上流行的 Web 浏览器（包括 Internet Explorer、Safari、Chrome 和 Firefox）。`LiveCode` 提供了适用于服务器环境和移动设备的预发布部署。

`LiveCode` 部署单人个人许可 99 美元起。iOS 的 `S-Lang`（编程语言）开发。商业开发包 499 美元起。根据项目、平台、用户或其他需求，提供额外的部署和服务包。`LiveCode` 服务包面向开发环境、专业和商业需求，以及教育者、大学和 K-12 教室。

来源（已编辑）："http://en.wikipedia.org/wiki/RunRev"

## S-Lang（编程语言）

`S-Lang` 是由 `John E. Davis` 设计的解释型编程语言，以解释器的形式为基于 C 的应用程序提供扩展性。它创建于 1992 年，其语法是一种原始语言，但比 C 具有更大的灵活性。`S-Lang` 体小、简单且是动态类型，支持许多基于数组的操作。由于其体积小且易于嵌入，`S-Lang` 已嵌入非数值程序中，如 `slm` 新闻和 `JED` 文本编辑器。the grace 模块

```slsh
slsh = grace_new ()
instance of grace
slsh = [0.0:10;#1000]
slsh = y=exp(-x)*sin(x)
slsh = plot(x,y;logs)
slsh = readascici("File.dat", &x, &y)
[1,3]
slsh: plot(x,y; color="red")
```

### 示例

下面展示了该语言的几个示例。它们包括对数组算术、函数和对象风格的支持。示例使用 `Grace` 绘制了指数衰减曲线：

```
% load
% require("grace")
```

来源（已编辑）："http://en.wikipedia.org/wiki/S-Lang_(programming_language)"

## SAM76

`SAM76` 是一种从 20 世纪 70 年代一直使用的宏语言。它引入于 `CP/M`，是一种字符串处理器，为交互式应用程序设计，并允许机器间的移植。具有与 Unix 类似的特性。该语言基于宏编程的思想。用户可以定义一个宏（由用户定义的、用于在程序中执行一组指令的单词）为一组指令（通常是宏或汇编语言并在程序中使用。通过这种方式，宏被调用，然后在运行时，需要解释器或字符串将其替换为宏。

`SAM76` 解释器提供了一种高度响应和交互式的语言，可以与用户对话完成任务。因此，该语言具备执行程序控制、文本编辑和处理、游戏以及数学运算的能力。从那时起该语言用 C 进行重写，并在 Windows、Linux 类似的操作系统上编译。源代码可以在网上获取，截至 2006 年仍然存在。

### 特性

`SAM76` 语言的特性

`SAM76` 遵循定义良好的语法，易于学习和阅读。然而，它严重依赖于系统系统来替换这

## SMX (计算机语言)

它们独立的词汇表、语言词汇表，并且可以被保存和执行，增加了个性化定制性。

来源（已编辑）：http://en.wikipedia.org/wiki/SMX_376

## SMX (计算机语言)

`SMX`（服务器宏扩展）是一种用于嵌入 Web 页的宏处理语言。它最初随流行的 Internet Factory 的 Commerce 软件一起发布，现已迁移为 Apache 模块。

降低为单个 `%` 或带圆括号的参数列表。（等一下，检查上下文：“"lowered either a single % or a parenthetical list of arguments.”）

### 页面计数器

参数可以使用双引号括起来。使用反斜线来转义逗号和双引号。参数开头的单引号将关闭对该代码（翻译为 LISP）的解释。

```
%expand%
%counter(hits) 访问量(hits)
```

### 数据库留言板

你所使用的所有内容在默认情况下都会输出。若要更改此行为，请使用 `%` 或 `%small` 标记。

#### 示例代码

```
%expand%
%not(exists(%tmp/gbook.sq3))
%sql:sqlite/tmp/gbook.
%sql:CREATE TABLE guests (name text, comment))
```

`SMX` 被嵌入在 HTML/XML 页面中。它最初随 Internet Factory 的 Commerce 软件一起发布，该软件是互联网早期流行的 Web 服务器，其开发者能够制作电子商务网站。

#### Hello World

这是一个 A World 代码示例：

```
%expand%
Hello World!（你好世界！）
```

```
%sign(%and(%format(name).%format(comment)))
%sql:sqlite/tmp/gbook.sq3,INSERT INTO guests (name, comment) VALUES (%sql(format(name)),%sql(format(comment))))
```

与其在 Perl 等更多语言中实现，不如一小部分 `SMX` 粉丝决定将该语言作为 Apache 模块来实现。

一个很好的例子是 `%counter()`。这是一个 HTML 页面上的简单计数器。若要包含 SQL 查询的结果，你可以在 XHTML 页面中间使用 `%sql:<query>%col(1) <br />`。

使用变量创建

```
%expand%
%set(name,Value)
Hello %name!（你好 %name!）
```

### 表单处理

```
%expand%
%if(form)
<p Result（结果）: Is %expr(form) %p>
```

```
<form action="%client-url%" method=post>
Simple expression（简单表达式）: <input name=expr>
</form>
```

由于 `SMX` 的高级级特性，可以大大减少构建动态或数据库驱动网站所需的编程工作量。

```
%p-%html-quote(col(name))
said=%html-quote(col(comment))-
<p>
<form action="%client-url%">
<br>Name: <input name=name<br>Comment: <input name=comment<br><br><input type=submit>
</form>
```



# 语法

与编程语言不同，`SMX`语法简单且一致。所有函数都以`%`开头，后面紧跟函数名。

# SWIG

（简化封装器和接口生成器）是一种开源工具，用于将`C/C++`中的复杂程序或库与`Lua`、`Perl`、`Python`、`Ruby`、`Tcl`等脚本语言连接，以及`Ki`、`Modular-3`、`Objective C`、`Octave`和`Scheme`等其他语言。输出也可以是`XML`或`L-scheme`的形式。

# 函数

其目的是允许通过解释代码调用原生函数（`C`或`C++`），传递复杂数据类型，保持内存不被释放，跨语言继承类。程序员编写一个接口文件，列出解释器可见的`C/C++`函数。`SWIG`将接口文件编译为一个

来源（已编辑）：http://en.wikipedia.org/wiki/SMX_(computer_language)

`C/C++` `SWIG`将为简单参数生成转换代码；转换代码：参数的类型由程序员编写。`SWIG`创建的源代码在`C/C++`和目标语言之间提供了胶水层。根据语言的不同，这分为两种：

- 现有的`C/C++`程序中的脚本引擎：
    - 可以通过脚本语言而非`C/C++`更快地对程序自定义。脚本引擎甚至可以暴露给终端用户，以便他们可以使用脚本管理常见任务。
    - `C`或`C++`代码的单元测试通常在脚本语言中完成效果更好。
    - 解释器可以作为某种形式的扩展模块链接的共享库，
    - 可以链接到用目标语言编译的其他程序的共享库（例如，在`Java`中使用`JNI`）。
    - 即使最终产品不包含脚本引擎，它对于编写单元测试可能仍然有用。

创建可以加载到解释器中的动态库有几个原因：

## 历史

`SWIG`用`C`和`C++`编写，自 1996 年 2 月起公开可用。最初作者和开发者`James Beazley`在阿拉斯马斯国家实验室和犹他大学担任研究生期间，以及在芝加哥大学期间开发了`SWIG`。目前由一个包括`William Fulton`在内的活跃志愿者小组支持开发。`SWIG`以`GNU`公共许可证发布。

`SWIG`不用于原生代码调用解释器；这必须由程序员手动完成。

- 提供对脚本语言中没有对应内容的`C/C++`库的访问。
- 首先用脚本语言编写整个程序，然后在`C`或`C++`中执行关键代码。

来源（已编辑）："http://en.wikipedia.org/wiki/Scripting_Layer_for_Android"：

# 目的

其目的是允许通过解释代码调用原生函数（`C`或`C++`），传递复杂数据类型，保持内存不被释放，跨语言继承类。

许多用于控制的脚本语言源于对`XML`的处理（已编辑）“Android 的脚本层”）：

目前最广泛使用的脚本语言包括：
- `JavaScript`
- `Python`
- `Ruby`
- `Lua`
- `Shell`
- `Perl`
- `JavaScript`（一种`XML`的方言）
- `XSLT`（一种将`XML`转换为新格式的语言）

# 网页浏览器

浏览器是显示网页的应用程序。为了操作的脚本语言已变得重要到获得了一个名字：`AJAX`。

# GUI 脚本

随着图形界面的出现，出现了一种用于控制计算机的特殊脚本语言。这些语言与窗口、菜单等进行交互。通过这种方式，脚本语言可以执行用户的操作。这类语言在通过模拟键盘或鼠标点击触发时，通常被称为“宏”。

脚本可以用于在`GUI`计算机上运行；但在实践中，对这类语言的支持取决于应用程序和操作系统。

这有几个局限性。

像`Tcl`和`Lua`等语言被专门设计为通用脚本语言，可以嵌入任何应用程序中。`Visual Basic for Applications` (`VBA`) 提供了与底层自动化设施的强集成。嵌入此类通用脚本语言而非为每个应用程序开发新语言，也让从头编写脚本的开发者受益，并让用户容易学习。

# 文本处理

基于记录的处理是脚本语言最古老的用途之一。`Unix`工具`awk`、`sed`、`grep`的脚本自动化涉及文本配置和日志文件的任务。重要的是用于文本词法结构的正则表达式，以及为此目的而开发的通用语言。

`Perl`的设计是为了克服这些工具的局限性，并已成为最流行的通用语言之一。

某些不同的脚本语言为编写浏览器扩展提供了方法，并有几种标准的嵌入式脚本语言，包括`JavaScript`（一种`ECMAScript`的方言）或`Lisp`。

## 历史

早期的主机（20 世纪 50 年代）是非交互式的，使用批处理。`IBM`的作业控制 (`JCL`) 是批处理的范型。首次交互式`Shell`开发于 20 世纪 60 年代，用于分时系统中运行程序。

# GUI 脚本

一大类脚本语言源于对作业控制的适应，这与启动和控制特定的通用-

# 作业控制语言和 Shell

## 182 - Scsh

其所有者并不将这些 [编程语言] 称为“脚本语言”，例如`Yahoo! Widget Engine`。其他嵌入`ECMAScript`实现的应用程序，如`Adobe`产品的`Flash`（`ActionScript`）和`Acrobat`（用于`PDF`文件），使用了嵌入式语言。在开发过程中，这些语言允许他们对功能进行原型设计并自由调整，而不需要用户了解应用程序，或在每次调整后都重新构建它（这可能花费大量时间）。用于这一范围的脚本语言从更常见的`Lua`到较为人知的`AngularJS`和`Squirrel`等皆有。

## 扩展/嵌入式语言

许多语言的设计目的是通过嵌入程序中来替代特定应用程序的脚本语言。程序使用带有“钩子”（hooks）的区域，使得脚本语言可以控制应用程序。这些语言充当特定用途语言，但其优势在于允许它们访问应用程序。`JavaScript`起初是浏览器内部的脚本语言，目前仍然如此；该语言作为`ECMAScript`的标准化，使其作为一种通用的嵌入式语言而广受欢迎。特别是，`Mozilla`的实现版本`ScriptMonkey`被嵌入到各种环境中。它最初是作为扩展创建的，但现在已经常作为类似于`Python`、`Perl`和`Ruby`的通用语言出现。

复杂且面向任务的应用程序可能会整合嵌入式编程语言，以允许用户拥有更多控制权，并提供比用户界面更多的功能（例如，并不并不复杂的，`Autodesk Maya` 3D 动画工具嵌入了`MEL`脚本语言，本文将重点介绍这一角色的语言）。

## 市场分析

根据`Evans Data`在 2008 年的一项全球调查，最广泛的脚本语言是`JavaScript`。第二广泛的是`Perl`。`Perl`是第三广泛的脚本语言，但在美国的受欢迎程度明显更高。（已编辑）：“http://en.wikipedia.org/wiki/Scripting_language”

## Scsh

`Scsh`是一种分层在`Shell`编程语言之上的`POSIX API`，其设计方式是为了充分利用`Scsh`的脚本能力。它仅限于 32 位平台。

哦，我们承认吧。我想不是。这一切都是我独立完成的。

- 标准输出到`PATH`中所有可用执行文件的列表：

## 特性

`Scsh`包含以下显著特性：

- 列表、字符和字符串操作的库支持；
- 使用系统正则表达式进行正则操作，具有类似小型语言方法的能力；
- 强大的网络支持；
- 对`awk`脚本的高级支持，作为宏集成到语言中；
- 终端的抽象伪；
- 一种使用准引用（quasi-quotation）建模的壳语言。

```
#!/usr/local/bin/scsh -s #!
```

```
(define executables dir) (with-cwd)
(filter-executable: (directory-files dir #))
(define x) display x (newline))
```

```
(for-each
(append-map executables (infix-splitter ":")\ (getenv "PATH"))
```

来源（已编辑）：“http://en.wikipedia.org/wiki/Scsh”

`Scsh`的参考手册包含了由`Owen Shires`在 1994 年写的、广为人知的致辞。

谁问你了？你们这些“所谓的”联盟，在我的背后恨我，这一切都是源于我的工作吗？我的研究生们，他们的计算机技能似乎受限于网飞下载超时？我的父母，他们还在等我放弃“玩电脑”，去上学校成为一名放射科医生？我的系主任，一位只对不满的邮政工人提供一个新见解和同情的经理。

## sed - 第 183 页

`sed`（流编辑器）是一种`Unix`实用程序，解析并编辑一种可以对文本应用转换的编程语言。它逐行（顺序地）读取输入，应用由命令行（或`sed`脚本）指定的运算，然后将其输出。它最早在 1973 年到 1974 年间被贝尔实验室的`Lee E. McMahon`用作`Unix`工具，并适用于大多数操作系统。

原始文件将通过将其重命名为指定的扩展名来保留。注意，在`-i`和扩展名之间不能使用空格，大小是可选的。

带有`y`。多个替换或其他命令可以放在一个名为（例如）`subst.sed`的文件中，然后使用`-f`选项从该文件中读取命令：

`Super-sed`是`sed`的扩展版本，包含了与`Perl`兼容的正则表达式。

另一个`sed`变体（minions），最初由`Eric S.Raymond`和`René Minix`从`4.3BSD sed`进行反向工程，被`GNU`项目用于创建一个基于新`GNU`正则表达式库的新版本`sed`。它包含一些元素，使得`sed`的功能没有`GNU sed`那么丰富。它的优势是速度快且占用内存少。它用于嵌入式系统并随`Minix`提供。

```
sed -f subst.sed
```

除了替换外，还可以进行其他形式的处理。例如，以下使用`d`命令删除空白或包含空格的行：

```
sed -e '/^ *$/
```

历史`sed`是早期用于数据处理的`Unix`命令之一。它是流行的`grep`命令的继者。作为后期`awk`的兄弟，`sed`和`awk`源于相同的灵感和祖先。用法：

- 符号 (`^`) 匹配行首。
- 符号 (`$`) 匹配行尾。
- 星号 (`*`) 匹配之前字符 (s) 的零或多个。

可以使用复杂的`sed`命令，尽管它是高度专门化的编程语言。控制流可以通过使用标签（冒号后跟字符串）来管理，它将处理后续块，如果标签不存在则分支将结束。`sed`的语言并不复杂。

## 服务端脚本

服务端脚本是一种`Web`技术，它通过在服务器上直接运行脚本来验证用户请求，并生成动态网页。它被用于提供与数据或其他数据源交互的交互式网站。这与客户端脚本不同，后者的脚本是由`Web`浏览器运行的（通常是`JavaScript`）。

动态网站还由自定义的`Web`应用程序服务器驱动，例如`Python`的"Base HTTP Server"库，尽管人们可能不认为这是服务端脚本。

在用户本地计算机上运行且不通过网络执行或接收的程序，与客户端没有连接，且此类程序的操作不被视为客户端操作。

当服务器执行`JavaScript`时，服务端脚本的许多优势之一是，它可以帮助根据用户的需求、查询访问或对其他数据的访问来定制响应内容。

## 解释

从安全性的角度来看，服务端脚本对浏览器是不可见的，因为它们在服务器上执行并输出`HTML`内容，然后返回给用户的页面。

在`Web`早期，服务端脚本几乎完全通过使用`C`、`Perl`和`shell`脚本的组合并结合通用网关接口（`CGI`）来实现。这些脚本由操作系统执行，结果直接由`Web`服务器返回。其他在线脚本语言如`ASP`和`PHP`可以由`Web`服务器本身或通过`Web`服务器的扩展模块（例如`mod_perl`或`mod_php`）直接执行。每种形式的脚本都可以构建复杂的多页面网站，但由于缺乏[此处原文缺失]，直接执行的开销较低。

当服务器以常用方式交付内容时（例如根据`HTTP`或`FTP`协议），用户有多个客户端（大多数`Web`浏览器）可供选择，并可以使用他们偏好的协议请求数据。在特殊应用程序的情况下，程序员可能会编写自己的服务器、客户端和通信协议，这些程序只能相互使用。

一些服务端脚本语言：

- `ASP`
- `ColdFusion Markup Language` (*.cfm)
- 通过`Server Pages`的`Java` (*.jsp)
- 使用服务端`JavaScript`的`JavaScript` (*.js)
- `Lua` (编程语言) (*lp)
- `Perl CGI` (*cgi, *.pl, *.pl)
- `PHP` (*.php)
- `SMX` (*.smx)
- `Lasso` (*.lasso)
- `WebDNA` (*dna, *.tp)
- `Progress FreeBSD` (*rr, *w)

> 来源：[http://en.wikipedia.org/Server-side_scripting](http://en.wikipedia.org/Server-side_scripting)

## 服务端包含 (SSI)

服务端包含（`SSI`）对于在整个网站中包含公共代码有用，例如页眉、页脚和导航菜单。条件变量可以在控制指令下有条件地包含。

该语言简单的设计使其比大多数服务端脚本语言更容易学习和使用，而复杂的服务端处理通常由一种功能更丰富的编程语言完成。`SSI`是图灵完备的。

`SSI`最常用的用法是将一个或多个文件的内容包含到服务器上的网页中。例如，一个包含数据引言的页面可以通过在`Web`文件中粘贴以下代码来包含引言：

为了让服务器识别启用`SSI`的文件并遵循其指令，文件名应该以默认扩展名`.shtml`、`.stm`或类似的后缀结尾。

```
<#include="quote.txt">
```

只需更改`quote.txt`文件，所有页面将显示最新数据。包含功能不仅限于文件。在这个示例中，在可以运行该脚本的服务器上，它的输出结果（一个随机引言）也可以被包含进来。

# 基础语法

`SSI`有一种语法：`<!--#include value=value-->`。指令被放置在`HTML`注释中，这样如果没有启用`SSI`，用户就不会在页面上看到`SSI`指令，除非他们查看源代码。注意，该语法不允许`<!--`和指令之间存在空格。支持`<!--#set`命令。

作为一种简单的编程语言，它的控制流非常简单，支持选择，但不支持循环，只能通过递归包含或在`Apache http`和`httpd`中使用`HTTP`来。

## 客户端包含

客户端包含是在客户端实现的`HTML`。这意味着包含的内容可以缓存在客户端上。它还意味着带有视图的页面可以在系统上本地加载，而无需服务器。

然而，虽然`HTML`允许将`CSS`、`JavaScript`和图像直接包含在包含的页面中，但它不允许包含`HTML`。有几种技巧可以实现这一点，但每种方法都有自己的问题。这些是：

- 使用`IFrame`，它在明显分离的固定大小的区域内包含内容。
- 将`HTML`代码转换为`JavaScript`程序，将`HTML`插入`DOM`中。
- 使用带有`Ajax`的`JavaScript`来允许`HTML`。现代浏览器都不会允许这直接从`shell`脚本中工作。

这些客户端包含相对复杂，`WYSIWYG`（所见即所得）编辑器无法访问，并且仅取决于客户端对其各自技术的支持。在框架和`iframes`的情况下，它们的访问性更低。

起初似乎手动从页面之间复制和恢复`HTML`片段是最简单的方法，但`SSI`是有价值的。在未来，浏览器可能会实现`W3C`包含规范，允许客户端包含。同样，客户端`XML`可以在某些浏览器中通过使用外部插件完成。

一些（示例）：[en.wikipedia.org/wiki/Server_Side_Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)

# Shell 脚本

`Shell`脚本是为操作系统的`shell`或命令行解释器编写的脚本。它通常被认为是一种领域特定语言。`shell`脚本执行的操作包括文件操作、程序执行和处理。

许多`shell`解释器的命令行界面，如`Unix Shells`、`Windows PowerShell`或`MS-DOS`，也允许在不需要命令行的情况下进行脚本编写。

一个示例是创建一个列表，并给它一个命令名称，通常位于：

```
#!/bin/bash
echo compiling...
-cc foo.c
-cc bar.c
-cc qux.c
-cc myprog foo.o bar.o qux.c
echo done.
```

从 20 世纪 80 年代起，这种类型的每一种都被像`make`这样专门构建程序的工具所取代。

# 通用化

第一行（`Shebang`）指示使用何种解释器执行脚本的其余部分，并带有`LC COLLATE`选项行。

在这里，第一行（`Shebang`）指示使用何种解释器执行脚本的其余部分，并带有文件格式指示符、列（全部注意，以及分号）。`LC COLLATE`设置排序顺序不折叠为小写，给它的任何参数将作为`locale`传递，因此所有的正常选项和其他语法仍然可以使用。

用户将能够用于最常见的`shell`脚本。

## 能力

## 快捷方式

## 批量作业

在最基本的形式下，`shell`脚本可以提供系统的变体，其中环境设置、命令选项和后处理被自动允许，但是以允许`shell`作为一个完全正常的`Unix`命令的方式。

简单的批处理对于孤立的任务没有用，但使用循环和变量为用户提供了灵活性。将`JPEG`图像转换为`PNG`的`Bourne`角脚本，其中图像通过命令行（通过通配符）提供，而不是在文件中列出每个，可以创建并保存到文件`/home/username/bin/jpg2png`

## Shell 脚本 - 第 187 页

```bash
#!/bin/bash
# for jpg in "$@"; do
  # 在每个文件名中使用 jpg
  png="${jpg%.*.jpg}"
  # 通过将 jpg 替换为 png
  # 找到该文件名的 png 版本
  echo converting "$jpg"
  # 向运行脚本的用户输出状态
  the_script
  if [ -f "$png" ]; then
    # 使用 convert 命令
    # (在 Linux 中) 创建 PNG
    # 并在临时文件中
    mv "$jpg" "$png"
```



# 如果成功，则重命名 PNG

# 图像为正确的名称

else

  # 回显 'error：无法保存到

  "$jpg.png'

  exit 1

fi

# "if" 测试构造的结束

fi

done

# "循环"的结束

echo "all conversions"

# 告诉用户我们成功了

fi

失败，并允许它们作为更大部分部分的组件被调用，这取决于底层是如何实现的。

与标准系统命令一样，shell 脚本仅根据文件名扩展名分类，除非其目的是为了读取到运行中的 shell 特殊机制中（例如`"$*"`或 C 语言的源码）。

### 优点与缺点

通常，编写 shell 脚本比编写编程语言的等代码要快。许多优点包括图像选择、启动和交互式调试。shell 脚本用于为现有程序提供顺序化和决策逻辑，对于中等规模的脚本，避免编译脚本的麻烦是一个优势。直观的运行使得调试脚本中的代码并重新运行以修复错误变得容易。用户可以使用 shell 脚本来处理程序的行为，且 shell 脚本为多进程处理提供了有限的范围。

## 编程

许多现代 shell 脚本具有通常只出现在高级或通用编程语言中的特性，例如控制结构、变量、数组、例程等。有了这些特性，可以将复杂的应用程序重写为 shell 脚本。然而，它们仍然受限于 shell 语言不支持数据类型系统、类、多线程、复杂数学和其他语言，并且比编译代码或以性能为目标的解释型语言慢得多。

## 其他脚本语言

已经引入了许多强大的脚本语言，用于处理普通 shell 脚本无法方便处理的任务；在这些任务中，脚本的优点是理想的，而开发一个完整的、编译的编程语言是有害的。

区分语言与高层编程的具体细节经常是辩论的来源。但通常，脚本语言是指需要解释器的语言。

## 多功能性

shell 脚本的一个关键特性是将其处理器作为操作系统函数调用。因此，并不是由用户仅有的 shell 在 shell 语言中执行脚本，或者由脚本正确处理其解释器（这两种都是 shell 脚本的壳问题），而是由操作系统设置并执行的。现代 shell 脚本不仅仅是同类命令，而且许多系统可以是（或更广泛地说）脚本，因为其中一些不是由 shell 解释，而是由 Perl、Python 或其他语言解释。这扩展到了达到用户系统等代码。

## 生命周期

Shell 脚本通常作为软件开发的一个阶段开启，其实现方式各异，最常见的是用 Perl、Python 或 C 编写。解释器允许将解释完全隐藏在脚本内部，而不是暴露为文件名-

另一个缺点是执行速度慢，并且几乎每个执行的 shell 脚本都需要启动新进程。当脚本的任务可以通过设置流水线来完成（其中高效工作执行大部分）时，这种延迟会被减轻，但一个复杂的脚本通常比具有该功能的编译程序慢几个数量级。

不同平台之间也存在移植性问题。Perl 的作者 Larry Wall 曾写道：“移植一个 shell 比移植一个 shell 脚本更容易。”

## 188 - Simkin (编程语言)

同样，更复杂的脚本会遇到 shell 脚本语言本身的局限性；这些限制使得编写高质量代码变得困难，各种 shell 的扩展可以缓解原始语言的问题，但也可能会使问题化。使用某些脚本语言的许多缺点是由语言语法或实现中的设计缺陷引起的，而不一定是由使用基于文本的命令行引起的；有很多 shell 使用其他编程语言，甚至是全功能语言，如 SSH（它使用...）。 来源（已编辑）：http://en.wikipedia.org/wiki/Shell_script

## Simkin (编程语言)

Simkin 是一种可以嵌入 Java 或 C++ 应用程序的脚本语言。它可以存储在多种文件格式中，包括 XML。它由 Simkin Whiteside 发明。

这个名字基于 Simkin Whiteside，“Simkin” 是维多利亚时代对“Simon”的昵称。用于 Sibelius 记谱程序插件的 Manuscript 脚本是基于 Simkin 的。来源（已编辑）：http://en.wikipedia.org/wiki/Simkin_programming_language)

## Smalltalk YX

Smalltalk YX (Sys) 是一种开源编程语言。它是 Smalltalk-80 语言的一种实现，并且。

Smalltalk YX 的目标之一是具有移植性并在许多操作系统上可用。它的设计易于使用且对各种用途功能强大。

支持的平台包括：
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

Smalltalk YX 提供了一个现代开发环境。它包含了回到如下的特性：
- 它支持
- Windows 98
- Windows XP
- Windows Vista
- Windows CE
- Pocket PC
- FreeBSD
- Arch Linux
- Debian
- Gentoo
- Solaris
- Mac OS
- PowerPC
- SPARC
- x86
- x64

## Squirrel（编程语言）

Squirrel 是一种高级命令式、面向对象的编程语言，被设计为一种轻量级的脚本语言，能够满足视频游戏等应用在尺寸、内存带宽和实时性方面的需求。MithKit 是一个用于制作和发布开源跨平台 2D 游戏的简单工具包，其平台使用了 Squirrel。用于脚本的 CodeBlocks 曾用过《幻想最终结录：我的王国生活》，同时也用于《死亡求生之路 42》和《传送门 2》中的脚本事件。

```squirrel
function factorial(x) {
  if (x == 0) {
    return 1;
  } else {
    return x * factorial(x-1);
  }
}
```

```squirrel
class BaseVector extends {
  constructor(varg) {
    if (varg.len() >= 3) {
      var x = varg[0];
      var y = varg[1];
      var z = varg[2];
    }
  }
}
```

```squirrel
x = 0;
y = 0;
z = 0;
```

使用生成器生成随机数：

```squirrel
function gen_random(max) {
  local last = -42;
  local IM = 139968;
  local IA = 3877;
  local IC = 29573;
  for(;;) // 死循环
    yield (max = (last * IA + IC) % IM);
}
```

```squirrel
class Vector3 extends BaseVector {
  function add(other) {
    if(other isof :: Vector3) {
      return Vector3(x+other.x, y+other.y, z+other.z);
    }
    throw "wrong parameter";
  }
  function Print() {
    ::print("");
  }
}
```

## 语言特性

- 动态类型
- 委托（Delegation）
- 继承
- 高阶函数
- 生成器
- 协作线程（协程）
- 尾递归
- 异常处理
- 自动内存管理（即带有备用垃圾收集器的引用计数）
- 弱引用
- 编译器和虚拟机仅需约 7 行 C++ 代码即可结合
- 可选的 16 位字符字符串

```squirrel
local randor = gen_random(100);
for(local i = 0; i <= 10; i += 1) {
  print(i, "");
}
```

类与继承：

```squirrel
local v0 = Vector3(1,2,3);
local v1 = Vector3(3,11,123);
local v2 = v0 + v1;
v2.Print();
```

# 语法

Squirrel 使用类 C 语言的语法。
Squirrel 中的阶乘：

## 历史

该语言于 2003 年以 MIT 协议发布。由 Alberto Demetiche 开发和维护。
来源（已编辑）："http://en.wikipedia.org/wiki/Squirrel_(programming_language)"

## StepTalk

StepTalk 是 GNUStep 的官方脚本框架，它将可分离的服务器或应用程序表示为单一对象环境。它的设计目的是独立于编程语言；其默认语言是 objective-runtime 之上的 Smalltalk。

StepTalk 已被移植到 Mac OS。

## 简介

StepTalk 的目标是为应用程序提供胶合环境，并提供以下框架：

- 应用程序或工具的简单快速扩展
- 语言或工具中对象的批处理

## Sun Web Developer Pack

- 应用程序或新功能的快速原型设计（“在线”播放并调优某个概念）

StepTalk 的默认脚本语言是 Smalltalk。这是因为 Smalltalk 是一种非常简单且易学习的语言。用户只需要了解少数基础就能使用该语言，而且它接近自然语言。Smalltalk 使用的方法与 GNUstep 使用的 Objective-C 类似。

GNUStep 运行在由各贡献者开发的原生 MacOS X Cocoa 框架上。来源（已编辑）：http://en.wikipedia.org/wiki/StepTalk

## 平台

StepTalk 可运行在任何平台上

## Sun Web Developer Pack

Sun Web Developer Pack (SWDP) 是 Microsystems 发布的一系列开源软件，用于开发运行在 Java EE 服务器上的 Web 应用程序。SWDP 针对的是使用 Ajax、REST、Atom 和 JavaScript 等 Web 2.0 技术的软件开发者。

- Phobos，一个允许使用 JavaScript 或其他脚本语言编写应用程序的项目
- Ajax 技术
- Project JMaki，一个用于在 Java、PHP 或 Phobos 中创建 Ajax 应用程序的框架
- 在 Java 中创建 REST 服务
- WADL
- ROME，一个用于通过 web feed Atom Server 解析和生成 RSS 及 Atom 的 Java API（The Rome Proponent 子项目），一个用于创建 web feed atom 的原型 Java API 和框架
- Project Dynamics，一个用于创建 Ajax 的 JavaScript 应用程序的框架

## 发布历史

SWDP 第 1 版于 2002 年 3 月 16 日发布。来源（已编辑）：http://en.wikipedia.org/wiki/Sun_Developer_Pack。

## SWDP 包含的软件

SWDP 包含以下内容：

字体 脚本语言支持
- REST
- RESTful Web 服务（一种 API）

## SuperTalk

用于美国广播电台 SuperTalk Mississippi。

SuperTalk 是 SuperCard 中使用的脚本语言。它是 HyperTalk 的后代。

从列表中选择元素、从所有可用图标中选择图标、选择播放声音的 MIDI 乐器或选择支持的图像格式（包括预览）。来自 HyperTalk。

## SuperTalk 扩展

SuperTalk 的部分功能偏离了 HyperTalk 的自然语言特性。这包括 alert 命令，它试图模拟略显的

## 丰富的对象模型

SuperTalk 还暴露了 SuperCard 扩展的对象模型，使其创建滑块、进度条和其他刻度、原生文本框和一级菜单成为。多种样式（模态面板、非模态、滚动、可重置、调色板）可用，且激活范围可以在脚本控制下修改。语法有点复杂。它还显示，随着时间的推移，许多 XCMD 被直接作为内置功能引入引擎引擎，保持了非常记忆的案例。最明显的案例是 movie 函数，其中是是作为控件控件控件““追踪”的的控件。。 

在   上的 Web 应用程序。

     器                   

script() 是一个 Skeleton，其编程语言为 Systemstream。

```squirrel
script() 是一个 Skeleton，其编程语言为 Systemstream。
```

来源（已编辑）："http://en.wikipedia.org/wiki/Symbolic_Stream_Generator"

NSK 上的 CPU，可能没什么好说的——如果你完全理解了所有的 TCL 单元，那么你可能已经在理解 NSK 的道路上进展顺利。

配置说明，例如启动和硬件配置序列。

KEEP 1 / FILE1（这会将内容加载到内存中）

TCL 仍然是惠尔-派特非服务器（Nonservers）上使用的脚本语言。非服务器是全球大型银行、赌场、零售商、电信公司、系统和股票交易所骨干网络基础设施的关键组件。

TCL 拥有大量的内置单元，允许用户捕获来自各种系统的输出，并按行或逐字符解析文本。

2. 输入：`HELLO BERNARD` 运行

它允许用户构建 TCL 程序，通过过滤器监控事件，这些过滤器监控 TCL 命令和应用程序事件循环。

3. 输出将是：`HELLO BERNARD`

TCL 是解释型语言。TCL 指令可以存储在简单的文本文件中作为宏（MACROS）、程序（ROUTINES）或定义（DEFINES）来制作脚本。脚本通常用于存储复杂的

存储在 FILE1 中的 TCL 程序的用例：

或创建一个名为 FILE1 的文件并包含以下两行：

```
? HELLO ROUTINE
#OUTPUT HELLO BERNARD
```

如何运行 TCL 程序：

```
# TCL ROUTINE
```

通过在提示符处命名文件来执行程序：

```
? RUNFILE1
```



来源（已编辑）：`http://en.wikipedia.org/wiki/TCL/`

# Tcl

## 特性

`ActiveTcl`

`Tcl`（或 Command Language，语言，但习惯上视为 "Tcl" 而非 "Tck" 或 "tick-or-see"）是一种由 `John Ousterhout` 创建的脚本语言。根据作者的说法，最初是因为“感到挫丧”，无法将他们那些低质量的语言合并并嵌入到应用程序中。`Tcl` 速度快，非常适合快速原型设计、脚本应用和测试。`TCL` 应用于所有系统，包括文件版本以及几种其他小内存占用的版本。`Tcl` 还用于 `CGI` 脚本以及作为 `Eggdot` 机器人的脚本语言。如今 `TCL` 广泛用于许多自动化测试（包括软件和硬件），并作为网络测试和 `QA` 套件的后续工具。`T` 和 `Tk` 的结合被称为 `Tk/Tcl`。

`Tcl` 特性：

- 所有操作都是命令，包括脚本语言。它们采用前缀表示法。
- 命令是可变的。
- 一切内容都可以被动态重新定义和扩展。
- 所有数据类型都可以作为字符串进行处理，包括代码源。
- 脚本和文件的事件驱动接口。还支持基于时间和用户定义的事件。
- 默认情况下，变量可见性限制在词法（语法）范围内，但允许向上访问以与闭包函数进行交互。
- 所有命令在用法不当时都会生成错误消息。
- 通过 `C`、`C++` 和 `Java` 实现扩展性。
- 使用字节码的解释型语言，支持 Full Unic (3.1)，于 1999 年发布。
- 跨平台：Windows API、Linux、Unix 和 macOS。
- 与窗口界面（GUI）高度紧密集成。
- 存在多种描述机制：
  - 全功能开发版本（例如，`tkkit`（单文件运行时，大小仅约 1 兆）、`starpack`（脚本/程序的单可执行文件，源自 `tklet` 技术）、`freewrapTCLSH` 将脚本转换为单文件二进制分发版）
  - `PSD` 许可，免费分发

`Tcl` 在 8.6 版本之前最初并不支持面向对象（OO）（8.6 版本在 `Tcl` 中提供了 `OO` 系统），因此功能通过包提供，例如 `Tcl` 和 `XOTcl`。甚至存在纯 `TCL` 编写的包，如 `Snail` 和 `Snoot`（简单的仅限 `TCL` 的面向对象编程）。

`Safe-Tcl` 是 `TCL` 的一个子集，具有受限的功能。文件访问受到限制，并防止执行任意的系统命令。它使用双解释器，在不可信的脚本中使用“用户解释器”。`Safe-Tcl` 可以被包含在电子邮件中：当应用程序支持 `application/safe-tcl` 和 `multipart/enabled` 时。`Safe-Tcl` 的功能已作为标准 `TCL/` 版本的一部分纳入其中。

`TCL` 编程语言创建于 1988 年，加利福尼亚大学伯克利分校工作期间。美国和欧洲都会举办电话会议和研讨会。

# 语法和基础语义

脚本由多个命令调用组成。命令调用是一个单词列表，空白符由分号终止。

```
word1 word2 ... wordN
```

命令的第一个名称，它不是语言内置的，但在库中。随后的单词是参数。因此我们有：

```
commandName argument1 argument2 ... argumentN
```

实际示例，使用 `puts` 命令，该命令通过默认通道输出字符串和末尾的换行符：

```
puts "Hello, world";
```

变量和其他命令可以被替换到字符串中，例如当我们使用 `set` 和 `expr` 计算结果时，并使用 `print` 配合示例文本显示结果：

```
# 样式会将表达式放在
(1+2+3+4+5, 在这种情况下)
{大括号}
set expr "1+2+3+4+5"
puts "The sum of the numbers 1-5 is $expr";
```

形式上，单词要么写成周围带有双引号的空白的形式，要么用大括号括起来，这会抑制所有替换（除反斜杠元素外）。在这里，双引号字符串、替换发生的类型，在

- 替换将表达式替换为评估脚本的结果。例如，`1+2+3"` 替换为包含的内容。
- 变量替换将美元符号及其后的变量名替换为变量的内容。例如，`"foo"` 被替换为变量 "foo" 的内容。
- 反斜杠替换将反斜杠及其后的字母或字符替换。例如，`"\n"` 被替换为换行符。从多个参数开始，任何带有 `(` 前缀的单词都会导致该单词被拆分为构建命令的参数：

由于这种结果，任何参数的结果都可以作为其他参数。与 Unix Shell 不同，`Tcl` 除非明确请求，否则不会替换任何字符串，这使得它更

总结一下：只有一种基本结构（命令）和一组简单的规则。等号 (=) 完全没有使用，而双等号 (==) 仅用于测试，即使在表达式上下文中（如 `expr` 命令或第一个参数）。

`Tcl` 命令的复杂性是可变的，并且（结构化程序命令的构造函数）指定了参数默认值的定义以及获取。这两个命令都是标准库的一部分；它们在库中没有特殊位置，根据需要可以替换。

# 与语言交互

`Tcl` 与 `C` 语言交互。由于我们用 `C` 写了一个语法前端编写器的框架，语言中的所有命令（包括本应以其他方式编写的，作为或如果……）都是以这种方式实现的。每个命令向命令传递一个值数组（已替换的）参数，并可以根据自己的需要解释这些值：

数字库允许 `Tcl` 脚本接口以与 `Verilog`、`Tcl` 和 `SystemVer` 硬件语言交互。

# C++ 交互性

# Java 交互性

# 扩展包

`Tcl` 一直支持扩展包，这些包提供了额外功能，如 GUI、终端应用程序自动化、数据库访问等。

# Tk

最流行的 `Tcl` 扩展是用于多种操作系统的 `Tk` 用户界面库。每个 GUI 由一个或多个 frame 组成。每个 frame 有一个

# Expect

一种非常流行的 `Tcl` 扩展。`Expect` 与 `Tcl` 早期的紧密关系在很大程度上导致了 `Expect` 在单元测试等专业使用领域的流行。`Expect`（自 2010 年起）让员工能够实现自动化测试，让服务器能够执行许多任务（交互式应用程序的脚本化）。由于它是运行它的唯一方式，`Tcl` 在这些行业领域的人气飞速增长。

可以通过这种方式提供主题：Windows Classic、Qt（挂钩到 X1 环境库）和 Aqua（Mac OS）。也可以在不使用这些调用的情况下，使用主主题中实现的小部件（widgetlets）来构建。这包括 `Tcl Script`、`Alt/Realized Plastik` 和 `Plasmerik`。

可以无缝配合运行的 `Tcl`。

## Tcl/UDP

`Tcl UDP` 提供了一个简单的库，用于支持 `Tcl` 中的用户数据报协议（UDP）套接字。

## 数据库

`Tcl` 数据库连接 (`TDBC`) 是 `Tcl` 6 的一部分，是 `Tcl` 脚本的常用数据库接口。它目前支持 `MySQL`、`ODBC`、`PostgreSQL` 和 `SQLite` 数据库的驱动。未来计划支持更多。

通过特定的数据库扩展支持数据库访问，目前有很多此类扩展。来源（编辑）："http://en.wikipedia.org/wiki/Tcl"

## Tcl/Tk

`Tcl/Tk` 是一个样式和小部件集合，可以通过操作系统的 API 将 `Tcl` 中的许多默认值替换为具有真正原生性的变体。

## Itcl/Tcl

`Itcl` 是 `Tcl` 的一个对象系统，通常命名为 `[Itcl]`，它是以类似于 `C++` 的方式在 `Tcl` 中增加功能的方法。

## Tellib

`Tellib` 是一组脚本包。

## Tcl/Java

`Tcl/Java` 是一个连接 `Tcl` 和 `Java` 的桥项目。它由两个不同的包组成：`Tcl Blend` 和 `Jacal`。

项目。人们也可以将 `Tcl Blend` 和 `Tcl` 加载到 `Java` 进程中，为 `Java` 应用程序添加脚本功能。由于 `Tcl Blend` 是一个普通的 `Tcl` 扩展，它可以与 `Tcl`、`Expect` 和 `Icl` 等其他 `Tcl` 扩展一起使用。通常用于将 `Tcl` 脚本功能整合到现 `Java` 应用程序中，而无需处理将 `Tcl Blend` 加载到 `Java` 进程时原生代码的复杂性。

## Tcl Blend

`Tcl Blend` 是一种 `Tcl` 扩展，通过 `JNI` 促进 `Java` 解释器与 `Tcl` 解释器之间的通信。`Tcl Blend` 通常用于将 `Java` 解释器加载到现有的 `Tcl` 进程中，以便在 `Tcl` 脚本中访问在 `Java` 中实现的功能。例如，人们可以在 `Tcl` 脚本中分配 `Java` 对象并主动调用其上的方法。

## Jacal

`Jacal` 是 `Tcl` 解释器的自实现，完全用 `Java` 编写。`Jacal` 还包含有助于促进 `Java` 解释器与 `Tcl` 解释器之间通信的功能。`Jacal` 是 `Jtk`，对于 `Jacal`，它于 2010 年 11 月 17 日发布。`Tcl` 的主要目标之一是继续 `Jacal` 的现代化，这种现代化始于 2009 年 Google 代码之夏 (GSOC) 中的 `Jacal` 现代化项目。来源（编辑）："http://en.wikipedia.org/wiki/Tcl/Java"

## Tellib

`Tellib` 是适用于 `Tcl` 编程语言的包集合。`Tcl` 以源码和预编译二进制格式分发。`Tcl` 支持 Windows、BSD、Unix 和 Linux 等多种操作系统。rms，如链表、哈希映射、树和图。

## 包分类

`Tclib` 包含了许多常用数据结构的实现——

- 编程工具
- 数学
- 数据结构
- 测试处理
- 文件格式
- 哈希、校验和和加密
- 文档工具
- 基准测试工具
- 网络
- 终端控制
- `CGI` 编程
- 语法和有限自动机
- `TKlib`
- 未归类
- 传输模块

来源（编辑）："http://en.wikipedia.org/wiki/Tclib"

## 数据结构

## tcsh

`tcsh` 是通过操作系统的 API 将 `Tcl` 中的许多默认值替换为具有真正原生性的变体。

使用 `csh` 而没有复杂性：

- `!m` 所有的最近执行命令的参数
- `!n-S` 所有的最近执行命令的参数
- `!` 所有的所有的执行命令的参数
- `*` 所有的执行命令的参数
- `!n` 所有的最近执行命令的参数
- `!n-m` 所有的执行命令的参数

## 别名

## 历史

`tcsh` 中的 `'t'` 来自于卡内基梅隆大学的 `Ken Greider` 发明的 `TEN`，一种操作系统。`csh` 的作者在 1975 年开始编写实现 `Tcl` 风格标签补全功能的代码。1983 年 10 月 3 日，来自俄亥俄州立大学的 `Paul Palace` 将其发布到源码。从那时起由许多人维护。`Wilfred Sanchez`。

## 通配符

`if ("输入" = [0-9] 则`

## 部署

早期版本的 Mac OS 将 `tcsh` 作为默认设置，尽管其他人可以更改此。`tcsh` 是其后代如 `DragonFish`、`PC-BSD` 和 `Desktop` 的默认。

## Tea（语言）

`Tea` 是一种 Java 环境的高级脚本语言。它结合了 `Scheme`、`Tcl` 和 `Java` 的特性。

- `XML` 处理。
- 100% `Java`。
- `Tea` 解释器用 `Java` 实现。
- `Tea` 运行在任何 `Java` `JVM` 的地方。
- Java 反射功能允许从 `Tea` 直接使用 `Java` 库。
- 意在在 `Java` 中轻松扩展。例如，`Tea` 通过 `JDBC` 支持关系型数据库访问，通过 `GNU Regex` 支持正则表达式，并通过 `SAX` 解析器（例如 `XMLAJ`）支持 `XML` 解析。
- 集成支持所有主要的编程范式。
- 函数式编程语言。
- 函数是一等对象。
- `Scheme` 风格的闭包是该语言固有的。
- 支持面向对象编程。
- 模块化库。
- 大量的核心函数和类。
- 字符串和列表处理。
- 正则表达式。
- 文件和网络 `I/O`。
- 数据库访问。
- 有一个开源编译器 `TeaClip`，它使用 Java 生成的解析器来解析并编译 `Tea` 源码到 `Tea` 字节码。`TeaClip` 的作者表示兴趣增强 `TeaClip` 以产生 Java 字节码。
- 另一方面，名为 `"destea"` 的项目在 `CPAN` 发布了 `Language::Tea`，它通过基于 `Tea` 代码生成 Java 代码提供了专有解释器的替代方案。

## 解释器替代方案

- `Tea` 是一种专有语言。其解释器受非自由

# 198 - 模板引擎 (web)

# 模板引擎 (web)

![](img/28b49089ea8cf20e1b8f2972fae5fffa_199_0.png)

`Ruby`、`C` 和 `Java` 均可以通过原生或通过库和模块进行模板处理。`JavaServer Pages` (`JSP`)、`PHP` 以及带有 `WebScript`、`JavaScript` 或其他语言的 `Active Server Pages` (`ASP`) 都是 Web 模板的示例。

## 典型特性

模板引擎通常包含大多数高级编程语言共有的特性，并侧重于处理纯文本的功能。这些特性包括：

- 变量和函数
- 文本替换
- 文件包含（或转包含）
- 条件求值和循环

## 比较

下表列出了 `Wikipedia` 上讨论的各种模板特性及其简要介绍。该内容正在进行中：

- 图例：
  - Engine (Implementation)= 引擎名称
  - Languages= 引擎的实现语言（而非模板语言）
  - License= 软件许可协议
  - Platform= 计算平台
  - Variables= 使用变量的脚本语言
  - Function= 使用函数的脚本语言
  - Includes=包含外部文件的脚本语言
  - Conditional Inclusion= 使用条件包含的脚本语言
  - Looping= 执行循环（`for`、`while` 或递归）的脚本语言
  - Evaluation(Language)= 执行“命令”的脚本语言（针对实现语言）
  - Assignment=为子模板设置名称和引用
  - Errors & Exceptions= 引擎输出错误
  - i18n= 国际化和本地化功能
  - Natural=模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

## 示例

附图描绘了 Web 模板引擎的简易模型。模板引擎使用来自数据库的数据处理模板源文件。模板将变量替换为特定值。通过用数据库内容（在第 01 页为“Mother”，第 02 页为“Child”）替换 `X`，并将“呈现规范”（在 Web 模板中）通过模板引擎相结合，从而批量生产 Web 文档。

一种（Web）模板引擎是一种旨在处理 Web 模板和内容信息以输出 Web 文档的软件。它在模板系统的环境中运行。

```html
<html>
<h1>Hello {X}</h1>
</html>
```



一个 Web 模板可能像这样：

带有额外的模板源代码 ...

```
templateAssign('X', 'World');
```

- 或者在提供数据库上下文文时：

## 类型

模板引擎作为模板系统或应用框架的一部分是非常寻常的，也可以用作预处理器、过滤器或模板处理器。目前，模板处理软件最常用于 Web 开发语境。

```
Sdata='Mother'; Sdata='World'; templateAssign('X', Sdata(i));
```

`XSL` 是由 W3 设计的模板处理器。它主要设计用于对 XML 数据进行转换（转换为 Web 文档或其他输出）。使用 `Perl`、`PHP` 等编程语言来输出文本。

## 优势

在以下方面使用模板引擎的益处：

- 鼓励将源代码组织成在操作上不同的源（可编辑的）：`http://en.wikipedia.org/wiki/Template_engine_(web)`

## 模板处理器

模板处理器 - 第 199 页

![img](img/28b49089ea8cf20e1b8f2972fae5fffa_200_0.png)

扁平文件数据库、电子表格或任何预格式数据的源格式。某些模板处理系统在可用数据类型上受到限制。另一些则设计用于最大的灵活性和许多不同类型的数据。该术语的使用最著名用于使用 Web 模板系统的 Web 开发，它也适用于其他语境。

## 文档生成

文档生成框架通常将模板处理作为生成文档的核心模型。

## 源模板

源模板传统上按规定指定：

- 根据现有的编程语言；
- 根据专门定义的模板语言；
- 根据托管软件应用程序的特性；
- 根据上述某些或全部内容的混合组合。

## 源代码生成

源代码生成支持为特定的应用领域、组织生成源代码（作为结果文档）（例如 `UML`、关系型数据、领域特定数据存储），或者用于简化计算机程序员的流程。

## 模板引擎

- 模板引擎负责：
- 连接到数据；
- 处理源模板中的代码；
- 将输出重定向到特定的流水线、文本文件或流
- 某些模板引擎允许额外的配置选项。

## 软件功能

Web 引擎使用模板和源数据（通常来自关系型数据库）产生一个或多个 Web 页面或片段。它作为 Web 模板系统或应用框架的一部分被包含。模板软件最常用于 Web 开发语境。

一张插了模板引擎所有基本元素和流程的图。

## 比较

## 结果文档

模板处理器（也称为模板引擎、模板解析器或语言）是一种旨在结合一个或多个模板产生数据或更多结果文档的软件组件。对于本文而言，结果是任何格式的输出，包括文档、网页、源代码或其整体或片段。这些由整个文档或一个文档片段组成。

## 用途

模板处理用于各种语境以实现不同的目的。具体目的可能取决于所使用的应用程序或模板引擎。然而，模板系统的灵活性通常允许出于原始设计意图之外的目的进行非常规用途。

## 系统元素

- 根据现有的编程语言；
- 根据专门定义的模板语言；
- 根据托管软件应用程序的特性；
- 根据上述某些或全部内容的混合组合。

## 模板引擎

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

`XSL` 是由 W3 设计的模板处理器。它主要设计用于对 XML 数据进行转换（转换为 Web 文档或其他输出）。使用 `Perl`、`PHP` 等编程语言来输出文本。

`Ruby`、`C` 和 `Java` 均可以通过原生或通过库和模块进行模板处理。`JavaServer Pages (JSP)`、`PHP` 以及带有 `WebScript`、`JavaScript` 或其他语言的 `Active Server Pages (ASP)` 都是 Web 模板的示例。

## 数据

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

`XSL` 是由 W3 设计的模板处理器。它主要设计用于对 XML 数据进行转换（转换为 Web 文档或其他输出）。使用 `Perl`、`PHP` 等编程语言来输出文本。

## 文档

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

`XSL` 是由 W3 设计的模板处理器。它主要设计用于对 XML 数据进行转换（转换为 Web 文档或其他输出）。使用 `Perl`、`PHP` 等编程语言来输出文本。

## 呈现

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

## 特性

- `Variables`= 使用变量的脚本语言
- `Function`= 使用函数的脚本语言
- `Includes`=包含外部文件的脚本语言
- `Conditional Inclusion`= 使用条件包含的脚本语言
- `Looping`= 执行循环（`for`、`while` 或递归）的脚本语言
- `Evaluation(Language)`= 执行“命令”的脚本语言（针对实现语言）
- `Assignment`=为子模板设置名称和引用
- `Errors & Exceptions`= 引擎输出错误
- `i18n`= 国际化和本地化功能

## 自然

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

# 语法

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

```text
// Single-line comment

class Foo extends Object;
```

```text
/* Multi-line comment */

var Object;
```

## 代码

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

## 逻辑

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

## 输出

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

## 引擎

模板本身可以是与最终输出一样有效的文档，语法引擎不会破坏结构

# VScript

使用英文编写的脚本脚本以及对话。可以将 `C` 类语言编译为该格式以使用。来源（已编辑）：`"http://en.wikipedia.org/wiki/Useccode"`

不包括使用 `ucc`，这是一种可以反汇编译的编译器。

# VBScript

`VBScript`（`Visual Basic` 脚本版本）是微软开发的一种活动脚本语言，以 `Visual Basic` 为模型。它被设计为一种“轻量级”语言，具有快速的解释器，可用于各种微软环境。`VBScript` 使用对象模型来控制环境内的元素。例如，`FileSystemObject (FSO)` 可以创建、读取和删除文件。

这使得用户能够快速创建带有 `GUI` 的应用程序。1992 年 9 月，该编程语言与 `Windows` 操作系统并不兼容；当时的 `Windows` 是基于 `DOS` 的 `Basic` 编译器，无法读取该语言。1999 年秋季，`Internet Explorer` 的推出包含了包括 `VBScript` 在内的许多功能。

并且 `Windows PowerShell` 的使用有所增加。其次，`VBScript` 是自动化工具 `Quick Test Performance` 的脚本语言。第三个值得注意的领域是将 `VBScript` 采用为某些嵌入式应用程序的内部脚本语言，例如工业操作器和人机界面。遗留 `DBMS InterSystems Cache`（包含其实现 `MUMPS` 的工具）`VBScript`、`Cache BASIC` 用于编程代码。

自 `Windows 98` 以来，微软 `Windows` 的每个版本都默认安装了 `VBScript`；在 `Windows Server NT 4.0` 选项以及 `Windows CE` 中（在设备上进行安装）。

在 5.0 版本中，`VBScript` 的功能随着新特性的增长，例如正则表达式；通过 `Statement; Execute` 的调用以及全局函数在执行另一个脚本期间评估并执行命令；通过 `GetRef` 和分布式 `COM (DCOM)` 系统实现函数指针系统。

这种被广泛使用的 `VBScript` 之所以流行，并不是因为 `VBScript` 有许多特殊优点（移除了完整 `Visual Basic` 的某些用功能，如字符串类型、扩展的错误处理以及为子程序提供可变参数的能力），而是主要因为编译后的代码不需要向微软支付版税。`VBScript` 商标已标记。当一个组织使用微软的 `VBScript Basic for Applications (VBA)`——例如 `Dotraf`、`Great Accounting` 和 `Visio`（随后被微软收购）等公司时——它们不会与其产品一起重新分发编写和调试 `VBScript` 代码的环境。

`VBScript` 必须在主机环境中执行，这些环境包括多个版本的 `Microsoft Windows`；`Windows Script (Host)`、`Internet Explorer` 和 `Internet Services (IIS)`。此外，`VBScript` 托管可以嵌入到其他平台和技术中，例如 `Microsoft Script (msscript)`。

在 5.5 版本中，`Subes` 在 `VBScript` 中添加了正则表达式子，允许作者捕获表达式组内的字符。这种功能在 `JScript` 中已经可用。

随着 `.NET` 的出现，脚本团队决定实现对 `VBScript ASP .NET` 的支持，并将不再开发新版本的 `VBScript` 引擎，并移交给微软脚本团队支持的其他团队，该团队负责修复错误和增强脚本。为了让 `Windows` 管理员迁移到 `Windows PowerShell`，脚本引擎将继续在 `Microsoft Windows` 和 `IIS` 的未来版本中发布。

## 历史

`VBScript` 起于微软脚本技术的一部分，于 1996 年发布。这项技术（还包括 `JScript`）最初针对开发人员。在为期两多年的时间里，`VBScript` 从 1.0 进展到 2.0，在此期间，它获得了更多 `Windows` 管理员的支持，他们正在寻求一种比 20 世纪 90 年代开发的批处理语言更强大的自动化工具。

1998 年 3 月 6 日，`Alan Cooper` `Bill Gates` 本人允许动态添加组件。1991 年 3 月 20 日，微软采用 `"Quick Basic"` 用于 `Ruby Shell`。

# 用途

尽管 `VBScript` 是一种通用脚本语言，但其易用性的特定用途值得注意。首先，它在微软环境的系统管理员和开发人员中被广泛使用。这种情况可能会随着推-

# 环境

当在 `Internet Explorer` 中进行客户端 Web 开发时，`VBScript` 在功能上与 `JavaScript` 相似。它用于编写嵌入 `HTML` 页面或从其引入的函数，并与页面的对象模型 (`DOM`) 交互，以执行 `HTML` 无法完成的任务。然而，`Firefox` 和 `Opera` 等其他网络浏览器没有对 `VBScript` 的内置支持。这意味着当需要客户端脚本和跨浏览器能力时，开发者通常也会选择 `JavaScript` 或 `VScript`。

`VScript` 还被用于网页的服务器端开发，使用 `Microsoft Active Server Pages (ASP)` 引擎以及各种类型的库、`dll` 等。运行在 `ASP` 页面中的 `VBScript` 包含在 `<%` 和 `%>` 标签内。以下带有 `VScript` 的 `ASP` 示例显示 24 小时格式的当前时间（注意，上下文后出现的 `'='` 号是调用 `Response` 对象的 `Write(method)` 的简写，但它也被用作 `Windows` 系统错误消息的默认脚本）。通过 `GUI`（如拨号框和输入框）进行回放和接收输入。

`Cscript` 位于命令行环境中。

`VScript` 可以包含在两种类型的脚本中：`VScript` 文件和 `HTML` 应用程序。

迭代和条件 `Do` 循环、`Then-Else` 语句和 `Case` 语句，以及一些更复杂的变体，例如 `IfElse` 和嵌套控制。

编码中的数组，为了可读性，有大量的常量，例如用于逻辑值的 `True` 和 `False`，用于 `Mbox` 对象的 `vbCancel` 和 `vYesNo`，用于颜色的 `vBlack` 和 `vYellow`。

```html
<!DOCTYPE HTML PUBLIC "-//W3C//HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">

<html>
<head>
<title>VScript Example</title>
</head>
<body>
<div>
<% 从 timeValue 获取当前时间
Function Time()
Dim timeValue
timeValue = Now()
24 小时格式的时间
is = <%= Hour(timeValue)%><%= Minute(timeValue)><%= Second(timeValue)%> %>
</div>
</body>
</html>
```

`WScript` 文件 (`WSF`) 以 `XML` 文件编写。`WSF` 可以包含多个变量。`WSF` 提供了一种代码重用方法：你可以编写一个或多个函数的库，并将其包含在一个或多个 `WSF` 文件中以模块化的方式使用功能。文件扩展名为 `.wsf`，与 `.vbs` 文件一样可以使用 `userscript.exe` 执行。

`HTML` 应用程序 (`HTA`) 以 `HTML` 编写。它用于生成用户界面，并将 `VScript` 等脚本语言用于程序逻辑。文件扩展名为 `.html`，可以使用 `ms.exe` 执行。

`VBScript`（以及脚本组件）用于 `Windows Script Component` —— 一种由任何启用 `COM` 的应用程序调用的 `ActiveX` 类。文件扩展名为 `.wsc`。

# 功能

# 语言特性

`VScript` 语言基于 `Visual Basic`，可以从几个类别进行审查：控制、结构、变量、数组处理、日期/时间函数、处理、对象、正则表达式、字符串处理等。

以下是 `VBScript` 语言的一些要点。

过程是 `VBScript` 中创建小型模块的主要结构。`VBScript` 区分了函数（可以在赋值中返回结果）和子程序（不能返回）。允许参数并可以按值或按引用进行传递。

# 附加功能

文件系统管理、文件操作和流文本操作通过 `Scripting Library.dll` 实现。这提供了 `FileSystemObject`、`File` 和 `Folder` 等对象，允许访问 `Windows` 文件系统。

二进制文件和 `I/O` 由 `"ODBC Stream"` 类提供，它也可以用作字符串生成器（因为 `VBScript` 字符串拼接由于大量的内存重新分配成本很高），并且可以转换为任何类型的字节和字符串值。

## VBScript - 第 203 页

可以通过 `ActiveX 数据对象 (ADO)` 访问数据库，并在足够的权限的情况下，可以使用 `GetObject()` 函数操作 `IIS` 主机（用于创建和销毁存储和虚拟目录）。`XML` 文件可以通过 `Microsoft XML` 库编程模型（`msxml6.dll`）处理，该模型还可以通过 `XMLHTTPObject` 类（`MSXML2.XMLHTTP6.0` 和 `MSXML2.ServerXMLHTTP6.0`）从万维网检索内容。

`cscript.exe` 或 `wscript.exe`。一个更复杂的示例展示了如何将 `MsgBox` 作为函数使用（返回结果），以及三个参数的使用，包括在第二个参数中使用常量。

```vbscript
' 终止所有涉及名称 <strProcessToKill> 的进程
Option Explicit
Dim counter,strProcessToKill, objWMIService, colProcess, objProcess
```

```vbscript
x = MsgBox("Hello World!",1,4,"Hello World: Title")

x = MsgBox("Hello World!",4,6,"Hello World: Title")

x = MsgBox("Hello World!",vbYesNoCancel+vbSystemModel, "Hello World: Title")
```

```vbscript
strCounter = ""
strProcessToKill = "notepad.exe"
Dim objWMIService = GetObject("winmts:\\.\?impersonationLevel=impersonate!&str=root\cimv2")
Set colProcess = objWMIService.ExecQuery
```

```vbscript
x = MsgBox("Hello World!",vbYesNoCancel+vbMsgBox("The result is " & x))
```

功能也可以通过 `ActiveX` 技术实现。由于安全考虑，微软在 `Internet Explorer` 中禁用了许多 `ActiveX` 控件，每月部署杀毒开关更新以禁用有漏洞的微软和第三方代码。

前三行的结果相同。为了清晰起见，第二个参数中的数字在提供时没有显式说明（即使用 `"4"`），而不是单个数字（在本例中为 41）。然而，在这一行中使用常量被视为最佳实践。不同的控件行为会有不同；例如，`vbYesNoCancel` 会指定两个按钮（是、否和取消）。

```vbscript
"*Select* from Win32
Where Name = "" & strProcessToKill & "")
For Each obj in colProcess
msgbox = "... terminating " & 
objProcess.Name
objProcess.Terminate
Next
```



使用`Option Explicit`并非强制要求，但它是`VBScript`的最佳实践。

## 开发工具

微软并没有定期为`VBScript`制作`IDE`（集成开发环境），尽管有报道称存在过微软脚本编辑器（`Microsoft Script Editor`）。第三方资源提供了`VBScript`调试器，并且在许多文本编辑器中，对`VBScript`或具有相似语法的语言提供了语法高亮。除此，可以使用任何文本编辑器来创建`VBScript`程序；重要的是给文件正确的扩展名。

### SendKeys
`SendKeys`方法向活动窗口（如果它处于焦点状态）发送一个或多个按键。此示例脚本发送三次`"Hello World!"`字符，每次停顿 2 秒（2000 毫秒）。

## 终止任务

`VBScript`可以访问`Windows`任务管理器。代码在执行时将终止（杀死）任何涉及`"notepad.exe"`的进程。

```vbscript
set shell = createobject("wscript.shell")

shell.sleep 2000

shell.sendkeys "Hello World!"

shell.sleep 2000

shell.sendkeys "Hello World!"

shell.sleep 2000
```

在执行期间，如果发生错误，脚本会报告错误消息，说明错误类型（例如“语法错误”）以及错误发生的行号和行内位置。

代码应保存为任意名称，然后在命令行窗口中使用`cscript.exe`或`wscript.exe`执行。在执行期间，命令提示符后将显示`"Hello World!"`字符。

## 示例

### Hello World

“简单”示例：

```vbscript
MsgBox "Hello World"
```

### Windows 文件操作

将其保存为`.vbs`文件。然后执行

所提供的对象示例

### Vimscript

使用`FileSystemObject`进行某些操作（例如测试文件是否存在），并创建一个文本文件（`TextStream WriteLine`）。文件名是其中一个方法的输入参数，该参数是通过按引用方式传递的（这是默认值，尽管在本例中这并不重要）。

`myfile="C:\Wikipedia-VBScript - Example - Hello World.txt`
`MakeHelloWorldFile`

子程序`MakeHelloWorldFile`在`MsgBox`对话框中选择`"OK"`后，在`C:\`盘的根目录下创建（如果已存在则更新）一个小型文本文件。
来源（已编辑）：`"http://en.wikipedia.org/wiki/VBScript"`

```vbscript
Sub MakeHelloWorldFile(FileName)
在 C: 创建新文件或覆盖文件

Set FSO = CreateObject("Scripting.FileSystemObject")

If FSO.Exists(FileName) Then

Answer = MsgBox("File " & FileName & " exists ... OK to overwrite?", vbOKCancel)

如果选中的按钮不是 OK，则

vbOK 是一个语言常量

If Answer <> vbOK Then Exit Sub

Else

确认 OK 以

Answer = MsgBox("File " & FileName & " ... OK to create?", vbOKCancel)

If Answer <> vbOK Then Exit Sub

End

创建新文件（或替换现有文件）

Set FileObject = FSO.CreateTextFile(FileName)

FileObject.WriteLine("Time ... " & Now())

FileObject.WriteLine("Hello World")

FileObject.Close()

End
```

### Vimscript

使用`FileSystemObject`进行某些操作（例如测试文件是否存在），并创建一个文本文件（`TextStream WriteLine`）。文件名是其中一个方法的输入参数，该参数是通过按引用方式传递的（这是默认值，尽管在本例中这并不重要）。

`myfile="C:\Wikipedia-VBScript - Example - Hello World.txt`
`MakeHelloWorldFile`

子程序`MakeHelloWorldFile`在`MsgBox`对话框中选择`"OK"`后，在`C:\`盘的根目录下创建（如果已存在则更新）一个小型文本文件。
来源（已编辑）：`"http://en.wikipedia.org/wiki/VBScript"`

```vbscript
Sub MakeHelloWorldFile(FileName)
在 C: 创建新文件或覆盖文件

Set FSO = CreateObject("Scripting.FileSystemObject")

If FSO.Exists(FileName) Then

Answer = MsgBox("File " & FileName & " exists ... OK to overwrite?", vbOKCancel)

如果选中的按钮不是 OK，则

vbOK 是一个语言常量

If Answer <> vbOK Then Exit Sub

Else

确认 OK 以

Answer = MsgBox("File " & FileName & " ... OK to create?", vbOKCancel)

If Answer <> vbOK Then Exit Sub

End

创建新文件（或替换现有文件）

Set FileObject = FSO.CreateTextFile(FileName)

FileObject.WriteLine("Time ... " & Now())

FileObject.WriteLine("Hello World")

FileObject.Close()

End
```



# Visual IRC

## Versus

- Visual IRC (16-bit) - 1995年针对 Windows 3.x 发布，由 MeGaLITH 编写。该程序具有许多内置功能，但可以使用 VPL（`VIRC` 编程语言）进行脚本，它是 `VScript` 和 `Sun` 的前身。
- Visual IRC '96（以及后的 Visual IRC '97、Visual IRC '98） - 1996年发布，由 MeGaLITH 编写。这是 Visual IRC 的第一个 32 位版本，适用于 Windows 9x/NT。许多引入 16 位 `VIRC` 的功能由 `VIRC` 的默认脚本处理。'96 和 '98 包含了由 Jesse Mew（又名 'Mr2001'，`VScript` 引擎）的代码。该脚本语言与之前的版本不可相比。在随后的版本中，增加了语音和视频会议功能。
- 第二代的开发速度慢了下来，到2000年，Visual IRC 似乎已经结束。原作者 MeGaLITH (Adrian Cable) 选择创建一个继任者 Mr2 (Jesse Mew)，他曾为某些代码贡献过内容，并且正在开发一个名为 Bual (IRC) 的克隆版本。他并没有抵抗 `VIRC '98` 代码库的发展，而是将各种 `VScript` 合并到 IRC 中发布为 Visual IRC 2。
- Visual IRC 2 -于2001年发布，其次在2011年发布，该版本的脚本语言基于 `VScript`，其内部几乎完全被重写了。事实上，它与 `VIRC` 共享几百行代码。语音和视频会议功能在此版本中推出，因为实现它们所需的库已不再需要。IRC、`VIRC` 以及相关工具的大部分源代码已通过项目网站和 SourceForge 根据 GPL 协议发布。

Versus 是一种最初为 IRC Bual IRC 开发的脚本语言，目前用于 Visual IRC。它在许多方面与 IRC、mIRC 以及作为 Tcl 使用的脚本语言相似。

选择“Versus”这个名字是因为它可以缩写为“VS”，这是 Visual IRC '96 的常用缩写（该语言也是 Visual IRC '98 使用的语言）。Versus 在很大程度上与 `VScript` 保持兼容，因此现有的文档和注释在作为 Versus 使用时仍然准确的。该名称也充当 `VIRC` 的替代品。

Object Versus 或 OVS 提供了 Versus 的面向对象功能。脚本定义了类和方法，而不是测试数据和别名；但在实践中，OVS 主要用于操作管理 IRC 界面、文件传输或打开窗口的 VCL 对象。

服务器事件使用正则表达式或 Versus 的通配符来匹配来自服务器的消息。如果有多个事件匹配到消息，则只有优先级最高的（根据文本长度和通配符的相对“值”决定）事件会被触发。

- 客户端事件通过标识：`<CreateWindow>` 和 `<CreateWindowbar>` 在打开新窗口时都会运行。它们也可以包含模式，以限制触发它的特定情况（例如，在创建新通道时运行）。
- 菜单树和菜单项显示客户端界面各种元素的右键菜单，同时菜单栏定义了菜单的布局以及每个项目的标题；菜单项定义了点击项目时执行的脚本。
- 工具栏和项目项与菜单树和菜单项类似，但它们定义了与窗口相关的工具栏。可以通过选择唯一的名称向界面中添加新的工具栏。

### 脚本存储

脚本存储在文件中，尽管有时使用 .vsc 扩展名。脚本文件包含在脚本加载时进行解释的模板；脚本中定义的任何内容（见下文）将替换脚本中同名的块。

### 脚本中定义的块

- 别名（Aliases）可以从任何窗口的命令行调用，也可以从脚本的其他部分调用。返回值的别名称为函数；别名可以确定是否返回值，然后根据需要执行相应的命令。
- 类用于对象脚本（OVS）。每个类可以包含属性、方法、一个构造函数和一个析构函数。
- 事件用于处理来自 IRC 的消息，以及系统或客户端层面的发生情况，例如完成脚本。

### 数据存储

#### 文件

- 脚本可以访问函数 `#Random()` 和 `#ReadLine()` 以及命令 `CreateFileAndAppend`。
- 脚本还可以使用 `TString` VCL 将整个文本文件读取到内存中并进行保存。
- 所有变量可以包含高达 4 GB 的数据。
- 变量名以美元符号 ($) 和大写字母、小写字母或下划线开头。
- 变量可以包含任何字符，尽管它们通常用于打印文本。
- 本地变量通过 `@command` 设置，并仅在创建它们的例程上下文中存在。它们在例程结束时被删除。某些本地变量是预定义的，例如代表当前例程名的 SC。
- 全局变量通过 `@command` 设置，可以被任何例程访问。别名可以通过设置全局变量 `Fresult` 来返回结果。
- 存储变量通过 `@command` 设置，与全局变量一样，可以在任何地方访问。它们的值会立即保存到持久性存储中，并在下次客户端启动时恢复。
- 4 GB 的数据，对允许的字符没有限制。
- 本地和存储数组值可以使用 `@L`、`@A` 和 `@S` 设置，它们的行为类似于变量。当设置一个存储值时，整个数组都会被保存。
- 语法 `Arrayname[key]` 用于设置或检索特定键的值。
- 语法 `Arrayname` 用于将数组作为键值对列表返回。
- 特殊序列 `$PROMPT` 会弹出一个对话框，提示用户输入一个值。

# Web 模板

WebData 包含一个专有的驻系统，具有搜索和编辑功能。虽然 WebData 包含允许通过 API 等方式连接关系型数据库的命令，但并不要求使用 WebData 创建数据库网站。连接（Join-like）操作可以通过基于 WebData 的数据库插件系统或使用键相互关联的标签集来实现。

WebData 由一套使用方括号 "[]" 和英语的语法组成。例如，若要在网页上显示今天的日期，只需在编写日期链接对应值的 HTML 或 CSS 代码中插入 "[date]" 即可，"time" 也是此类操作。若要向特定的客户端地址显示某些文本，可以使用请求：[show [ipaddress]]-xxx.xxx.xxx.some Text(/)；大多数 WebData 包含标签，命令遵循相似的约定。

## 术语

WebData 语法基于：

- 经典型（Classic）
  用方括号包围的键名，例如：`[show [tag][yes=]]`
- 所见即所得（WYSIWYG）
  使用类似 XML 的方式存储标签，例如：`<tag-name value="value"></tag-name>`
  （在使用所见即所得的网站编辑器时格式化更好）

WebData 指令基于三种类型：

- 标签（Tag）
  用方括号包围的单个键，例如 `[ipaddress]`（客户端（计算请求）的 IP 地址）
- 上下文（Context）
  包围其中的起始标签和结束标签。`[.Format [3.7][Format] 部分格式为'00']`
- 命令（Command）
  命令放置在 URL 字段中。

参数可以包含在任何标签、上下文或其他地方。

## 历史

根据 Pacific Software 的创始人兼 WebData 首席架构师 Grant Blunt 的说法，Webcatalog（现为 WebData）最初是一组帮助实现图形标签的宏集合。

在 WebData 演变为通用服务器端语言之前，它是一种专用于创建显示图库摄影页面的特殊用途服务器端语言。它具有购物功能，以及一个可搜索的固定字段数据库，其中设有用于存储照片信息的专用字段。之后，Catalog 软件在创建编程语言的价值上表现出色。

Webcatalog 出现在 90 年代中期的平台。正如其名称所示，它的早期开发允许将传统目录转换为在线目录。这在 1997 年尤为明显，当时的 StoreBuilder 和 WebMerchant 产品允许用户在网上建立商店门面。“WebCatalog”一词指的是整个产品，而“WebData”一词指的是脚本语言。

在 2000 年左右，WebCatalog 和 Pacific Coast Software 在 Microsoft Software, Inc. 的推动下发生了变化。微软软件公司将 WebCatalog 改名为一个涵盖产品所有方面的名称。从 WebData 4.0 版本开始，1999 年到 2000 年是 WebData 脚本语言非常活跃的年份，该语言由许多国际知名品牌开发，包括 Ben and Jerry's、thebury Boy Shop、NCAA Final Four 和 Television Radio。此外，在此期间，所得语言的发展包含了许多功能，例如模块化编程和结构化程序。

从 2005 年到 2008 年，可能由于各种原因（包括微软公司其他产品的成功），WebData 用户开始失去所有者的支持并走向衰落。WebData 失去了大部分用户，他们选择了更受支持的开发者。随后，一些开发者复兴了相关语言。

2008 年 6 月，几个 WebData 开发者成立了组织并加入了 WebData Software Corporation (WSC)。WSC 购买了 WebData 的知识产权，并在 2009 年使用了 6.2 版本（Cicada）。来源（已编辑）："http://en.wikipedia.org/wiki/WebData"

## Web 模板

模板用于网页设计中将内容与呈现分离，并用于 Web 文档的批量生产。它是网页模板系统的基本组件。

Web 模板可用于建立任何类型的网站。从简单的意义上说，网页模板类似于用于设置网站的信函。

## Web 模板系统

- 显示照片库。
- 将音乐文件以 MP3 格式在线放置以便通过网络浏览器播放。
- 将视频公开展示。
- 在线设置私有登录区域。
- 源代码可能与其他代码资产不同；
- 应用程序的制作过程需要在不同的时间和地点完成工作；
- 不同的工作人员有不同的技能集，演示技能与编码逻辑并不匹配；
- 当组件保持分离且松耦合时，资产更容易维护且可读性更高。

## 有效分离

Web 开发人员的共同目标是开发和部署灵活且易于维护的应用程序。该目标中的一个重要考虑是业务逻辑与呈现逻辑的分离。开发者使用模板系统（成功程度不一）来维护这种分离。评估分离的一个困难在于缺乏定义良好的形式化方法来衡量其实际实现程度。然而，也有一些从软件工程领域借用的公平标准。这些标准包括基于面向对象编程原则的“继承”；以及模板化编程（具有 MVC 分离的原则）。不同准则之间的差异取决于解释，且某些准则具有相同的相似性。

## 可重用性

并非所有 Web 模板的用户都有意愿和能力帮助开发者为他们的需求设计系统。此外，许多人可能想使用网络但没有技术能力。由于这些原因，许多开发者和供应商发布了非技术人员使用的 Web 模板。虽然 Web 模板的易用性对于高技能开发者来说也很重要，但对于简单性和“现成”解决方案来说至关重要。内容（来自数据库）和“呈现规范”（在 Web 模板中）通过模板引擎结合，以批量生产文档。

## Winbash

主要属性：

- 嵌入式或事件驱动型。
- 简单、可迭代、可编程或复杂。

服务器上的页面，已发布的页面是静态的。这是内容管理系统（如 Wordpress）中的常见功能。但这不应被视为一种离线生成。

通常的任务是通过可以通过缓存图像和页面片段等内容来减少源服务器的负载和流量，并以高效的方式将其传递给浏览器。

- 规范：该语言的标准由公共或私有机构控制。占有策略和所有权指示了规范的稳定性和可信度。请注意，在大多数司法管辖区内，语言规范不受版权保护，因此所有权并不是绝对的。

在大多数情况下，“发布选项”不会干扰模板系统，并且可以通过外部软件（如 Wget）进行管理。

基础边缘包含 (ESI) 是一种为内容分发网络 (CDN) 实现的类似于 SSI 的语言。ESI 模板也可以使用 JavaScript 和 Ajax 在 Web 浏览器中实现，或者通过浏览器“插件”实现。

- 模板引擎：它是公开的（所有权），表示模板引擎的代码是否开源。

## 服务端系统

## 客户端系统

服务端模板系统

服务端动态页面是由具有适配此功能的现有软件模板生成的。这些早期软件是预处理器和宏语言，通过 CGI 适配 Web 运行。接，但相关的技术是使用 SSI 在扩展模块上直接执行。

客户端和分布式（去中心化）模板系统。

## 外部服务器系统

外部服务器模板系统

许多 Web 浏览器支持到浏览器自身的 XML XSLT 样式表，提供了功能：

许多系统通常被用作服务端模板系统：

其他系统使用 JavaScript 或浏览器内置脚本语言在浏览器中实现模板框架：

- JQuote2 - jQuery 模板引擎
- Perl
- Mjt.Template
- webJS

从技术上讲，当使用“服务端包含脚本”时，嵌入如 HTML（或 XML 等）等编程语言的方法也是模板。它们全都是嵌入的复杂语言。

## 分布式系统

还有被用作服务端模板引擎的预处理器。例如：

更简单的形式是转换（HTML 框架）。在其他情况下，它是用于运行的动态网页。

## 边缘系统

- Ajax（编程）
- 富交互互联网应用。

“边缘侧和包含系统指的是位于客户端（浏览器）和源服务器之间空间内的 Web 服务器。它们被称为“反向代理”服务器。这些服务器

示例：

源（编辑）：http://en.wikipedia.org/wiki/Web_template_system

在此语境下，Web 模板仅指静态网页，可以作为一种现成的方法，用于生产“模版化”网站以快速部署。

HTML 编辑器是使用外部服务器子系统的类型。它们还包含主题以代替 CSS 样式。在通用模板语言中，仅与其他软件配合使用。

FrontPage 和 Dreamweaver 是带有模板系统的最流行的编辑器。Flash 模板使用 Macromedia Flash 创建具有视觉吸引力的站点。

许多服务端模板系统具有输出选项。

## Winbash

Winbash 是一种由 Wilson WinWare 开发的 Microsoft Windows 脚本语言。其环境包括一个解释器和一个带有对话框设计器可选编译器的代码编辑器，用于创建自包含的可执行文件。

这是一种相对容易学习的语言，其结构和语法初看起来像是 Basic 和 C 之间的混合体。多年来它不断发展，具有许多功能，并支持 ActiveX、COM (OLE)、Unicode 以及 Windows 和 7 的 Uac 代码签名。

## PowerShell

来自 Intel 8048 及其后续处理器，以及 AMD 和 Cyrix 处理器。

执行任务：启动和结束连接操作；创建、编辑或复制电话录条目；查找有关现有 RAS 连接的信息；在 RAS 连接开始或结束时接收通知。

- 文件搜索 - 查找系统中的任何文件，可以扫描所有目录，查找所有文件并搜索任何文件的内容。
- GPIB 扩展器 - 用于 ComputerBoards（及兼容设备）GPIB 卡或 National Instruments（兼容的）GPIB 卡。
- IP 地址扩展器 - 获取机器的 IP 地址。
- 映射扩展器 - 执行 MPI 操作。
- 网络扩展器 - 它们可以与其他扩展器（如工作组复用器）一起使用或相互使用。NetWave 连接器帮助您在系统内映射和操作网络进程。
- ODBC 扩展器 - ODBC 扩展器有一组基本的 ODBC 客户端。
- 串口通信扩展器 - 允许与标准串口及连接到其上的设备（如实验室设备、其他计算机、串口终端、串口打印机和 X-10 控制器）进行通信。现代系统中内置用于连接大多数标准调制解调器，包括支持作为调制的文件传输方法。
- Shell 扩展器 - 带有窗口图形的 Explorer 风格操作。也可以复制、删除和移动整个目录。它具有带有超时设置的简单栏和消息框。
- WILX 扩展器 - Windows 95 扩展器 - 扩展拨号网络和 FTP 功能。
- InternetSock 扩展器 - 允许主机、互联网服务提供商和支持 Windows 操作系统的网络之间进行通信。包括高级协议（包括 FTP、SMTP、POP3 和 ping）以及低级 Zipper 扩展。

## 历史

Windows Word 创建于 1989 年，带有命令提示符。1991 年，该语言变为 WinBatch。不久后，发布了企业版本，包含一个代码绑定器（带有解释器的字节版本程序）。

## 文档

提供德语、西班牙语和日语文档。

## Hello world

使用该语言变为 WinBatch。

## 扩展

执行任务：启动和结束连接操作；创建、编辑或复制电话录条目；查找有关现有 RAS 连接的信息；在 RAS 连接开始或结束时接收通知。

- 文件搜索 - 查找系统中的任何文件，可以扫描所有目录，查找所有文件并搜索任何文件的内容。
- GPIB 扩展器 - 用于 ComputerBoards（及兼容设备）GPIB 卡或 National Instruments（兼容的）GPIB 卡。
- IP 地址扩展器 - 获取机器的 IP 地址。
- 映射扩展器 - 执行 MPI 操作。
- 网络扩展器 - 它们可以与其他扩展器（如工作组复用器）一起使用或相互使用。NetWave 连接器帮助您在系统内映射和操作网络进程。
- ODBC 扩展器 - ODBC 扩展器有一组基本的 ODBC 客户端。
- 串口通信扩展器 - 允许与标准串口及连接到其上的设备（如实验室设备、其他计算机、串口终端、串口打印机和 X-10 控制器）进行通信。现代系统中内置用于连接大多数标准调制解调器，包括支持作为调制的文件传输方法。
- Shell 扩展器 - 带有窗口图形的 Explorer 风格操作。也可以复制、删除和移动整个目录。它具有带有超时设置的简单栏和消息框。
- WILX 扩展器 - Windows 95 扩展器 - 扩展拨号网络和 FTP 功能。
- InternetSock 扩展器 - 允许主机、互联网服务提供商和支持 Windows 操作系统的网络之间进行通信。包括高级协议（包括 FTP、SMTP、POP3 和 ping）以及低级 Zipper 扩展。

# Windows PowerShell

PowerShell v2.0 于 2009 年 8 月完成并发布发布，是 Windows 7 和 Windows Server 2008 R2 的组成部分。PowerShell XP、Windows Server 2003、Windows Vista 和 Windows Server 2008 的版本于 2009 年 10 月发布，并适用于 32 位和 64 位平台。

对象；也就是说，cmdlet 之间传递的数据是完全类型的对象，而不是字符字符串。当数据传递给 cmdlet 时，元素在跨 cmdlet 过程中封装了它们的类型和结构，而不需要像仅共享字符字符串那样进行任何解析。对象还可以封装对包含的数据运行的函数。这些元素供接收命令使用进行自描述。Cmdlet 输出其结果或集合（包括数组），并可以可选地接收格式化输入，使其适用于管道中的接收者。但 PowerShell 允许将对象的数组和集合写入管道，因此 cmdlet 始终会输出集合中的每个对象。

## 概述

Windows PowerShell 可以执行四种类型的命令：

- cmdlets，由开发者编写的 .NET 程序，编译成动态链接库并由 PowerShell 脚本加载
- PowerShell 脚本（以 .ps1 结尾的文件）
- PowerShell 函数，可执行的程序。

如果命令是可执行文件，PowerShell 会在单独进程中启动它；如果是 cmdlet，则在 PowerShell 进程中执行。PowerShell 还提供了一个交互式命令行界面，可以在其中输入命令并显示其输出。基于 Win32 控制台的用户界面提供了一个可自定义的表格，但缺少语法高亮。PowerShell 允许创建比原始 Windows 命令更得强大的 cmdlet。PowerShell 还支持命令的命名参数和位置参数。在执行 cmdlet 时，参数值到参数的绑定由 PowerShell 自身完成，但对于可执行文件，参数通过 ($ 或 argument) 变量传递由可执行文件解析。

PowerShell 使用的另一个概念是管道。与 Unix 不同，PowerShell 管道用于构建复杂的链，允许一个命令的输出作为另一个命令的输入。管道通过将一个命令（或 cmdlet）的输出通过到另一个命令来建立，类似于 Unix 的对应物，但 PowerShell 是。

对于管道中的最后一个 cmdlet，PowerShell 自动将其输出交给默认 cmdlet，该 cmdlet 将对象转换为文本流并返回到屏幕。

因为 PowerShell cmdlet 共享一个签名，该签名检索对象中数据的表示，PowerShell 使用此方法将对象转换为文本。它还允许指定格式，因此可以通过选择显示哪些元素以及如何来选择对象的文本表示，但为了保持向后兼容性，如果在管道中使用可执行文件，它接收的是代表对象的文本，而不是 PowerShell 类型。

Cmdlet 是专门的 .NET 类，PowerShell 在调用它们时将它们实例化为对象。Cmdlet 继承自 cmdlet 或 PSCmd，后者用于 cmdlet 需要与 PowerShell 运行时交互的情况。这些基类定义了由 Process(Record) 提供的特定方法，使 cmdlet 实现能够提供功能。每当传递对象集合时，都会为集合中的每个对象调用该方法。Cmdlet 具有一个 .NET 属性——用于指定命令的类型和名称。Cmdlet 返回对象作为输出。

如果通过输入或命令行参数执行 cmdlet，则类中必须有一个相应的属性，并具有可变性实现。PowerShell 使用参数或输入调用 cmdlet，这些参数由类变量中的实现设置。这些值随后由实现功能的方法返回。

扩展类型系统 (ETS) 基于 .NET 框架，但具有扩展功能（例如属性和类型可扩展性）。例如，它允许通过暴露数据属性、字段和方法的子集创建对象视图，以及自定义格式和排序行为。这些元素使用基于 XML 的配置映射到原始对象。

## Cmdlets

Cmdlet 是实现特定功能的专门程序。这些是 PowerShell 外壳中的原生命令。Cmdlet 遵循命名规范，例如 Get-ChildItem，有助于创建它们。

与命令行参数匹配的属性由 Parameter/Attribute 标记，并在 Begin() 之前设置。这些属性使用 FromPipelineAttribute 属性设置器将管道输入映射到变量。

你所指这类 cmdlet 类实现可以引用任何 .NET API，并可能使用任何 .NET 语言编写。PowerShell 提供了某些 API，例如 Write-Object()，你可以使用它来访问 PowerShell 功能，例如将对象返回管道。你可以直接使用 .NET 访问 API，或者通过 PowerShell 提供程序（Providers）的基础设施，提供程序可以使用唯一路径访问数据存储。

与 Linux 系统采用管道的概念不同，PowerShell 的不同之处在于管道各个阶段之间传递的内容。在 Unix 中，一个命令的输出以原始文本的形式传递到管道的下一阶段。PowerShell 由 .NET 对象组成。使用对象消除了从一个命令的文本输出中提取数据的需要，因为所有对象都导出通用接口。

解析组合，例如 GB、MB 和 KB。

使用关键字，PowerShell 提供了创建可以接收参数的功能。对于 PowerShell 新手来说，一个常见问题是函数参数之间是用逗号分隔的，而不是。

数据存储通过驱动器（drives）以及内部的层次结构（目录）暴露。Windows PowerShell 为文件系统、注册表、证书存储提供了驱动器，以及用于命令别名的其他命名空间。Windows PowerShell 还包含了用于管理 Windows 系统、文件系统或使用 Windows 管理接口（WMI）控制 Windows 对象的各种 cmdlet。

- 使用两个参数调用函数。参数可能会绑定到在 中声明的参数上。
- 使用单个参数调用函数，该元素是。

## 脚本编写

Windows PowerShell 包含一种动态脚本语言，可以使用 cmdlet 实现复杂操作。对于 PowerShell 新手来说的一个常见问题是函数参数之间是用逗号分隔的，而不是。

脚本语言支持变量、函数、分支（if-else）、循环（do, for）、结构化错误处理以及与 .NET 的集成。

PowerShell 允许通过在括号 [] 中包含名称并使用冒号 (:) 来调用任何 .NET 方法。在 PowerShell V2 中，提供了更具移植性的 cmdlet 版本。PowerShell V2 还引入了模块，允许开发者和管理员以自包含模块组织 PowerShell 代码。每个模块都有自己的自包含代码，不会影响状态。模块还需要你使用脚本定义限制环境。

使用 Output cmdlet 创建对象。PowerShell 提供了 .NET 异常处理机制。在错误情况下，包含信息的对象（异常对象）通过 catch 关键字抛出。然而，action-error 是可配置的；发生错误时，PowerShell 可以配置为静默执行，而不捕捉异常。

### 管道

PowerShell像 Unix/Linux 系统一样实现了管道，允许一个 cmdlet 的输出管道到另一个 cmdlet。Get-Process 命令的输出可以管道到 Sort-Object 命令（按句柄计数排序）并到 Where-Object 过滤任何内存小于 1 MB 的进程，最后管道到 Select-Object 命令选择前 10 个（i. 基于计数）。

使用 PowerShell 编写的脚本可以在 .ps1 文件中跨会话持久。或者，可以运行整个脚本或脚本中的单个函数。脚本会自动重载 cmdlet，并且参数可以绑定到它们上。

可以使用表示法访问对象，例如 $Object 语法。PowerShell 提供了特殊变量，例如 Sargs，它是从命令行传递给函数的任何行参数，而 $ 指管道的当前对象。PowerShell 还提供了变量和数组。

PowerShell 管道可以通过函数、脚本和 cmdlet 定义。然而，脚本执行默认是禁用的，必须显式启用。

## Windows PowerShell

支持类似于许多 C 家族编程语言支持的科学计数法的二进制前缀表示法。它本身并不处理或显示。

在 Job 中的交互式 cmdlet 会阻塞作业的执行，直到用户提供输入。

### 托管 (Hosting)

Microsoft Exchange Server 2007 使用托管 API 提供其管理 GUI。GUI 中暴露的每个操作都映射到 PowerShell cmdlet（宿主机）。在这种情况下，原生 PowerShell cmdlet 本身就是一个 PowerShell 宿主机，它解释在命令行输入的命令，并创建必要的管道（Pipeline）对象并调用它们。

- 事务（Transactions）：允许 cmdlet 和提供程序执行带事务性的操作。PowerShell 2.0 包含了用于启动、监控和停止 PSTransaction 的 cmdlet，以及管理和将事务重定向到 cmdlet 和提供程序操作的功能。PowerShell 注册表提供程序支持事务。

PowerShell 的另一个用途是嵌入到管理应用程序中，该程序使用 PowerShell 运行时来实现管理功能。PowerShell 提供了一个托管的托管 API。通过这些 API，应用程序可以实例化一个运行时（PowerShell 运行时的一个实例），它运行在应用程序中并作为 Runspace 对象执行。实例的状态封装在 SessionState 对象中。当创建运行时时，Windows PowerShell 会初始化实例化，初始化提供程序和 cmdlet，并相应更新 SessionState 对象。然后必须打开 Runspace 以进行同步或异步处理。

- 脚本程序（Scriptlets）：这些是使用 PowerShell 脚本语言编写的 cmdlet。注意：脚本 cmdlet 现在的首选名称是高级函数（Advanced Functions）。

### PowerShell 2.0

- 可步进 cmdlet（Steppable Cmdlets）：这允许对创建的 cmdlet 的 BeginProcess() 和 EndProcessing() 函数进行控制。

要执行命令，必须用 runspace 创建一个管道（由 Pipeline 对象表示）。管道对象由构成管道的 cmdlet 填充。对于顺序操作（如在 PowerShell 中），会为每个语句创建一个 Pipeline 对象，并将其嵌套在另一个 Pipeline 对象中。当管道被创建时，PowerShell 会调用管道处理器，它将 cmdlet 绑定到各自的关联（命令和参数），并将它们与 InputPipeline、OutputPipeline 和 ErrorPipeline 关联起来以处理这些 cmdlet。类型和参数通过反射进行绑定。如果设置了管道，宿主机会调用 Invoke() 或等效的 Invoke-Async()。管道末尾有 Write-Host cmdlet，它将结果写入控制台屏幕。如果没有，则结果将交给宿主机，宿主机可能会提供

Windows PowerShell ISE，带有多个打开的 PowerShell cmdlet PowerShell 2.0

- 模块（Modules）：此脚本允许开发人员和管理员将 PowerShell cmdlet组织组织划分到自包含的模块中。每个模块在其自包含上下文中代码不会影响模块的状态。模块可以使用脚本定义受限的运行环境。它们具有持久状态以及公共和私有成员。

微软随 Windows 7 和 2008 R2 发布了 PowerShell 2.0。PowerShell 2.0 默认安装在 Windows Server 2008 上（Core 版本除外，它是可选的）。其他版本使用 Windows 管理框架（Windows Management Framework）。PowerShell V2 包含了脚本语言和 API，以便添加更多新 cmdlet。

PowerShell V2.2 新功能的非详尽列表：

- PowerShell 远程控制（PowerShell Remoting）：通过远程机器网络使用 Windows 管理。
- 后台作业（Background Jobs）：也称为 Job，它允许异步执行命令序列（脚本）或管道。作业可以在本地机器或多台机器上运行。一个
- 事件（Event）：此功能允许对管理和系统事件进行监听、工作和操作。

数据语言（Data Language）：PowerShell 语言的特定子集，允许创建定义并在运行时加载资源导入到脚本中（脚本项化）。

## PowerShell

事件允许 PowerShell 宿主机获知其托管实体的状态变化。它还允许 PowerShell 脚本订阅 ObjectEvents、PSEvents 和 WMIEvents 并异步地处理它们。

### 相似命令

下表包含了 PowerShell 自带的某些 cmdlet，并指出了其他已知语言 linter（语法检查工具）中最相似的命令。

结果 '$sABC'：



进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`。

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```
if (condVar > someVal) {console.log("xxx")}
```



# ZZT-oop

`ZZT-oop`是一种早期的游戏编程语言，由 Tim Sweeney 为他的电脑游戏 `ZZT` 设计。该名称代表 `ZZT` 面向对象编程（`ZZT Object Oriented Programming`）。这个名字是向美国摇滚乐队 `ZZ Top` 的双关。`ZZT-oop` 还缺少函数，且例程可能会被流氓消息中断——包括对象在执行过短或从未完成时发送的消息。通过使用状态对象和锁定重要例程可以在某种程度上克服这一缺点；但这可能导致对象错过信号。`ZZT-oop` 是运行时运行的，不进行预解析。分析是在运行之前进行的，而不是通过应用代码更改来实现。这意味着任何错误都会以晦涩的方式报告，这使得调试变得非常耗时。

- 游戏内的集成使得这种语言易于使用。学者不需要安装多个程序即可开始编程。具体的几何位置使得对象比抽象数据更容易被构想。
- 在动态环境中，并行操作的多线程设计是容易理解的。

# 概述

`ZZT-oop` 是事件驱动的。一个 `ZZT` 游戏由一组对象组成，每个对象都带有一个脚本。脚本并发执行（从当前屏幕上运行的每个脚本中取一个命令），并通过向彼此传递消息进行通信。

# 语法

该语言的语法极其简单。它是基于行的，每行的第一个字符定义了该效果。

地图的第一行可以以 `*` 为前缀，这表示对象名称。没有前缀的对象无法通过命令（`#ALL-label` 和 `#OTHERS-label`）接收来自其他对象的消息，因为没有办法引用它们。

没有前缀的指令、以 `$` 或 `,` 为前缀的指令会导致对象打开消息窗口并向玩家显示文本。

以 `'` 为前缀的指令表示注释（实际上，它们是预处理标签）。

以 `7` 或 `*` 为前缀的图形表示表示墙（字符数字 `29`）；然后，它不会被玩家访问，因为它不会移动，或者在程序结束时变成一面真正的墙。

```
@Shooter

:GO WEST

:TurnAround

:GO OPP FLOW

:Keeping

?FLOW

:IF BLOCKED FLOW THEN

:TurnAround

:Keeping

:Touch

:Need to keep the timer around

anymore

:SENDInvisibleTimer:Die

:ShootDown

:SHOOT SOUTH

:SENDKeeping

```

# 特性与局限性

# 缺点

`ZZT` 语言的局限在于应用而非灵活性。布尔标志是唯一的变量类型，这使得算术变得非常困难；程序员被迫与对象工作，通常依赖于物理移动、可能的（但仍然是物理上的）对象，而不是算术计算。

`ZZT-oop` 自称为“面向对象”，但由于其物理性质，对象并不是瞬时完成的，这意味着需要复制复杂的代码系统。

# 优点

该语言具有一些优势：

`ZZT-oop` 对初学者来说是容易上手的。它具有数学运算符，简单直观。这有助于初学者指示对象向指定的方向移动。方向包括北、南、东、西，以及 `SEEK`（向玩家移动）和前缀如 `CW`（意味着顺时针，例如 `CW` 意味着东）。

消息是声明式语言中的 `goto` 语句；唯一的区别是它们只能发送给另一个对象，并导致该对象的执行路径跳转到脚本中的该点。它们可以被调用，用 `:` 来表示对象的名称，当接收到消息时，对象的控制应该跳转。

标志是布尔变量，用于可以通过命令设置或清除的条件。如果调用 `#command`，将评估给定的标志；如果它为真，将发送列在其随后的消息，导致脚本跳转到该点。

以 `#` 为前缀的指令指定命令，这些命令控制与环境的交互，无论是显示、设置标志、发送消息还是处理条件。有几十个原生的 `ZZT-oop` 命令：

- `-SEND`，向另一个对象发送消息
- `-SET` 和 `CLEAR`，管理定义命令的标志值，以及 `UNLOCK` 反转该操作
- `-LOCK`，使对象无法接收消息
- `-PUT`，创建一个指定类型的新对象并将其放置在当前对象旁边
- `-BECOME`，导致当前对象变成某种物品或纹理，结束其巨大的生命周期（`-DIE` 的作用类似于 `EMPTY`）；
- `-ZAP`，将之前的某个带有标签替换为 `:DIE`，以及 `RESTORE` 反转该操作

## 示例

程序演示了一个壳的“对象”，它会反复移动（从东到西），向下进行（向南）。如果玩家是射击者，壳将失去健康值。如果玩家碰到 `Shooter`，壳将被摧毁。

注意使用“隐形计时器”向 `Shooter` 发送定期的 `Shootdown` 消息。该程序通常附加到一个对象。

`CYCLE` 命令设置该对象更新的频率。

```
:CYCLE 40

:Loop

:Shooter:ShootDown

:SENDLoop

:Die

:Turn into a real wall

:BECOME RED SOLID

```

来源（已编辑）：`http://en.wikipedia.org/wiki/ZZT-oop`

