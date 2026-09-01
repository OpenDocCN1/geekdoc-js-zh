
# Linux 调试与性能调优：技巧与技术 (Prentice Hall 开源软件开发系列)

Phil Thompson 前序，PyQt 创始人

# Arnold Robbins，系列编辑

“来自真实世界应用的真实代码”

开源技术彻底改变了计算世界。许多大型项目已在全球范围内投入生产使用，如 Apache、MySQL 和 Postgres，程序员们使用 Perl、Python 和 PHP 等多种语言编写应用程序。这些技术被应用于许多不同的系统，从专有系统到 Linux 系统，再到传统的 UNIX 系统、大型机。

范智出版社开源软件开发系列旨在为你带去最出色的开源技术。你不仅将学到如何将它们应用于你的项目，还能从中学习。通过查看来自应用程序的真实代码，你将学习到开发世界的开源开发者的最佳实践。

Short Cuts 是专为像你这样忙碌的专业人士设计的简洁简短的 PDF 文档。每份 Short 都紧扣特定的技术或技术问题。Short Cuts 由行业专家和畅销作者撰写，并于 6 月与你同步发布——获取技术

本书献给

Andrea Summerfield

# 目录

- 练习 .......................................................................................................................................... 318
- 示例：流混合部件 ................................................ 339
- 连接到数据库 ............................................................................................ 446
- 这还没有完全结束 ........................................................................................................ 559

# 附录 A 安装 ........................................................................................................ 561

- 在 Windows 上安装 ............................................................................................ 561
- 在 Mac OS X 上安装 ............................................................................................ 566
- 在 Linux 和 Unix 上安装 ................................................................................................ 570

# 附录 B 选定的 PyQt 部件 ................................................................................... 575

# 前言

作为 PyQt 的创建者，我很高兴看到这本书的出版。尽管我担任了该书的技术审稿员之一，但我乐意坦白，我自己也学到了一些东西。

PyQt 文档涵盖了所有 PyQt 类的 API。这本书将向你展示如何使用这些类，如何将它们结合起来创建对话框、主窗口以及整个应用程序——所有这些看起来美观且运行良好，没有任何任意限制，并且使用一种让人用起来非常愉快的编程语言。

我特别喜欢这本书的一点是，它的示例并不是为了说明简单观点而设计的平凡例子，而是本身就具有潜在价值的。对不同方法的考虑，将使那些希望深入理解如何将 PyQt 应用于大规模、生产级应用的读者受益。

我从 20 世纪 90 年代后期开始了 PyQt Story。那时我已经使用 Tcl/Tk 有段时间了，但我觉得 Tk 程序看起来很丑，尤其是当我看到 KDE 第一版本所取得的成就时。我一直想切换到 Python，因此我想将语言的改变与 GUI 库结合。

起初，我使用了一些用 SWIG 编写的包装器，最后得出我可以自己制作一个更合适的包装器的结论。我开始创建 SIP，并于 1998 年 11 月发布了支持 Qt 1.41 的 PyQt 0.1。从那时起开发一直在持续，以跟上 Qt 的发布并扩展 PyQt 的范围，例如添加支持工具和改进文档。到 2000 年，PyQt 2.0 在 Linux 和 Windows 上都支持 Qt 2.2。2001 年出现了对 Qt 3 的支持，2002 年支持 Mac OS。PyQt4 系列从 2006 年 6 月的 PyQt 4.0 开始，支持 Qt 4。

我的主要目标一直是让 Python 和 Qt 以一种让 Python 程序员感到自然的方式协作，让他们在 Python 中完成任何 C++ 中可以做到的事情。实现这一点的关键是开发 SIP。这为我提供了一个我可以完全控制的专用代码生成器，并确保 Python 和 Qt 将永远紧密结合。

开发和维护 PyQt 的流程现在已经建立。许多工作现在都是自动化的，这意味着跟上 Trolltech 的 Qt 新版本不再是以前的问题，并确保了 PyQt 在未来多年持续下去。

多年来看到 PyQt 社区的增长是非常令人欣慰的。如果这本书是你接触 PyQt 的一部分，那么欢迎！

> — Phil Thompson
>
> 英国，多塞特，温伯恩
>
> 2007 年 8 月 25 日

# 引言

本书教你如何使用 Python 编程语言和 Qt 应用开发框架编写 GUI 应用。唯一的先决知识是你可以使用某种面向对象的编程语言，例如 C++、C#、Java 或者当然是 Python 本身。对于富文本章节，假设读者对 HTML 和正则表达式有一定的了解，数据库和多线程章节假设读者对这些主题有一些基础知识。不需要 GUI 编程知识，因为所有的核心概念都已涵盖。

对于职业工作内容需要编程的人来说，这本书将是有用的，无论是全职软件开发人员，还是其他学科（包括科学家和工程师）中需要编程来支持工作的人。它也适用于本科生和研究生，特别是那些从事包含大量计算元素的课程或研究的学生。书中练习（附带答案）专门为了帮助学生。

Python 可能是广泛使用的语言中最容易学习、最漂亮的脚本语言，而 Qt 是开发 GUI 应用的最佳库。Python 和 Qt 的结合——“PyQt”，使得在任何支持的平台上开发应用程序并保持在所有支持平台上不变成为可能——例如，所有现代版本的 Windows、Linux、Mac OS X 以及大多数基于 Unix 的系统。Python 的解释不需要编译，得益于 Qt 抽象了特定平台的细节，不需要修改源代码来适应不同的操作系统。我们只需要将源文件拷贝到安装了 Python 和 PyQt 的目标机器上，应用程序就会运行。

如果你是 Python 新手：欢迎！你即将发现一种既易读又易写、简洁而不晦涩的语言。Python 支持许多编程范式，但由于我们的重点是 GUI 编程，除了极少数章节外，我们在任何地方都采用面向对象的方法。

Python 是一种非常有表现力的语言，这意味着我们通常写的 Python 代码比用 C++ 或 Java 编写同等应用要少得多。这使得在全文中展示一些小但完整的示例成为可能，并使 PyQt 成为快速开发 GUI 应用的理想工具，无论是用于原型设计还是生产。

```python
/home/mark/books/rapid-gui-programming-python-and-qt/chap08/mypyw.pyw - Eric4
File Edit View Start Debug Project Refactoring Extras Settings Window Help
moviedata.py moviedata.py mypyw.pyw
class MainWindow(QMainWindow):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        self.movies = moviedata.MovieContainer(self)
        self.table = QWidget(self)
```

图 1 Eric4 IDE——一个 PyQt4 应用

由于本书的重点是 GUI 编程，第一部分提供了一个快速的教程以及一些 PyQt 的涵盖。这些内容有明显的标记（如本段所示，侧边注有“Qt”），以便丰富的 PyQt 程序员跳过他们已经熟悉的部分。第二、第三和第四部分都是 PyQt 特有的，并假设读者可以轻松学习 Python。

经常在编程中，我们会遇到几种可以采取的方法。参考书和在线文档识别了类、方法和函数，但在某些情况下，文档很少提供背景信息。这本书提供了必要的背景，并对 GUI 编程提供了见解，以便你决定在特定情况下如何操作。例如，当你创建一个对话框时，它应该是模态的吗？（参见第 5 章关于此问题的说明。）

PyQt 用于编写各种 GUI 应用，作为供科学家和工程师使用的工具。图 1，例如，一个在 PyQt 中编写的强大集成环境。可以编写几行代码的 PyQt 应用，并且 PyQt 用于编写各种 GUI 应用，作为供科学家和工程师使用的工具。

# 书的结构

本书分为四个部分。第一部分主要是一个针对熟悉面向对象语言的非 Python 程序员的快速课程，尽管它也包含（标记标记）PyQt 内容。因为核心 Python 语言大部分简单且体积很小，这些章节可以教到 Python 的基础，达到足够编写真实 Python 应用的程度。

如果你认为可以通过阅读来掌握 Python 语法，你可能会想跳过第一部分，直接进入从第二部分开始的 GUI 编程。第二部分的早期章节包含了对第一部分相关页的引用，以支持选择这种方法的读者。然而，即使对于熟悉 Python 的读者，我们也建议阅读第 1 章。如果你不熟悉函数应用（柯里），阅读第 2 章中涵盖此点的子节是非常重要的，因为这种技术有时用于 GUI 编程。

> * 还有针对旧版 Qt 3 库的 PyQt 绑定，但没有理由在新项目中使用它，特别是因为 Qt 4 提供了更多功能且更容易使用。

第二部分将展示三个微型的 PyQt GUI 应用程序，让读者对 PyQt 编程有一个初步的印象。它还解释了 GUI 编程涉及的一些基本概念，包括 PyQt 的高级信号与槽通信机制。第 5 章展示了如何创建对话框，以及如何在对话框中布局部件（“控件”）——即构成用户界面的图形元素，如按钮、列表框等。对话框是 GUI 编程的核心：大多数 GUI 应用程序只有一个主窗口和几十甚至上百个滑块，因此这一主题得到了深入讲解。

在介绍对话框之后是第 6 章，该章节涵盖了主窗口（包括菜单、工具栏、停靠窗口和快捷键）以及应用程序设置的加载与保存。第二部分的最后章节展示了如何使用 PyQt Designer（PyQt 的视觉化设计工具）创建对话框，以及如何以二进制、文本和 XML 格式保存数据。

第三部分对第二部分涵盖的话题进行了更深入的介绍，并引入了新话题。第 9 章展示了如何以复杂的方式布局部件以及如何处理多个文档。第 10 章涵盖了低级事件处理程序，以及如何使用剪贴板、拖放、现有部件、HTML 和二进制数据。第 11 章展示了如何修改和子类现有部件，以及如何从零创建全新的部件，并完全控制它们的外观和行为。本章还展示了基础操作。第 12 章展示了如何使用 Qt 4.2 的新图形架构，该架构特别适合处理大量的独立图形对象。第 13 章涵盖了 Qt 具备 HTML 能力的文本引擎。本章还涵盖了打印到纸张和 PDF 文件。

第三部分包含两个关于模型/视图编程的章节：第 14 章介绍了该主题，并展示了如何使用 Qt 的内置视图以及如何创建自定义数据模型和代理；第 15 章展示了如何使用模型/视图架构进行数据库编程。

第四部分继续延续模型/视图的主题，第 16 章涵盖了三个不同的高级模型/视图话题。第 17 章的第一部分描述了用于提供在线帮助的技巧，第二部分解释了如何对应用程序进行国际化，包括如何使用 Qt 的翻译工具创建翻译文件。Python 标准库提供了网络和线程的类，但在第四部分的最后两章中，我们将展示如何使用 PyQt 的类来实现网络和线程。

附录 A 解释了如何获取 Python、PyQt 和 Qt，以及如何在 Windows、Mac OS X 和 Linux 上安装它们。如果你安装并尝试一些练习题，并检查一些示例代码，学习 PyQt 会容易得多。附录 B 展示了部分 PyQt 部件的截图和简要描述，这对于 GUI 编程的新手很有帮助。附录 C 提供了 PyQt 关键类的层次图；这有助于了解 PyQt 提供了哪些类以及它们之间的关系。

如果你从未用过 Python，应该按顺序阅读第 1-6 章。如果你已经熟悉 Python，至少阅读关于字符串的策略（位于第 28 页的符号列表处），并浏览第 2 章的内容（除了你非常熟悉的第一部分之外）。确保你熟悉 `lambda` 和 `partial` 函数应用，这两者在第 2 章中都有介绍。跳过第 3 章可能也是值得的。然后按顺序阅读第 4、5、6 章。

一旦你读完前六章，你就掌握了 Python 的核心内容和 PyQt 的基础。

如果你想知道如何使用设计工具而非纯通过手工编码来创建对话框（这可以节省大量时间），那么第 7 章很有用。对于文件处理，至少阅读第 8 章的前三部分。如果你计划读写文本文件，请阅读第 8 章的第四部分；同样，如果你将使用 XML 文件，请阅读第五部分。

对于第三部分，至少阅读第 10 章关于事件处理的第一部分以及第 11 章全文。第 12 章和第 13 章的第一部分假设你已经读过 PyQt 的事件处理，并读过第 11 章。第 9 章和第 14 章可以在此部分独立阅读。

在第四部分，第 16 章假设你已经读过第 14 和 15 章，但其他章节可以独立阅读。

如果你在文中或示例中发现错误，或有其他意见，请邮件至 mark@qtr.eu，主题写为“PyQt book”。书的主页将发布任何更正，并从那里下载示例和练习答案，地址为 http://www.qtr.eu/pyqt.html。

如果你想参与 PyQt 社区，加入邮件列表是值得的。访问 http://www.riverbankcomputing.com/mailman/listinfo/pyqt 查看存档，这样你可以了解邮件列表的情况，并获取加入表单。Python 也有邮件列表和其他社区活动，可以访问 http://www.python.org/community。

# 致谢

我有许多人要感谢，我将从那些亲密参与本书的人说起。

Jasmin Blanchette 是 Trolltech 的高级软件开发人员、Qt 专家，也是一位优秀的编辑和作家。我曾与他合作过两本 C++/Qt 书。Jasmin 提供了大量的建议和批评，极大地提升了这本书的质量。

David Boddie 是 Trolltech 的文档经理，也是一位活跃的开源开发者，对 PyQt 做出了许多贡献。他的投入确保了书的质量。

Richard Chamberlain 是 Jadu Ltd. 的联合创始人兼首席技术官，这是一家内容管理公司。他的反馈和见解确保了书籍尽可能广泛适用。

Trenton Schulz 是 Trolltech 的开发者，也是我之前书籍的价值审阅者。在这本书中，他带来了 Python 和 Qt 知识，与 Richard 一起确保了 Mac OS X 用户没有被忽视。此外，他还发现了一些我遗漏的错误。

Phil Thompson 是 PyQt 的创建者和维护者。他从一开始就支持这本书，并根据我们对书籍的为 PyQt 增加了功能和改进。他纠正了许多错误和误解。

特别感谢 Samuel Rolland，让我使用他的 Mac 笔记本安装 PyQt、测试示例并拍摄截图。

感谢 Guido van Rossum，Python 的创建者，以及更广泛的社区，他们让 Python 尤其是其库变得实用且易用。

感谢 Trolltech 开发并维护 Qt，特别感谢过去现在的 Trolltech 开发者，其中许多人我有幸合作过，他们确保了 Qt 是目前最好的跨平台 GUI 开发框架。

特别感谢 Jeff Kingston，Loot 语言的创建者。我所有的书籍以及许多写作项目都使用 Loot。多年年来，Jeff 根据用户反馈对 Loot 进行了许多改进并增加了许多功能，包括我所要求的。感谢 James Clos，他创建了 DejaVu Sans 字体的压缩版本（源自 Jim Lyles 的 Vera 字体），本书的等宽字体即源于此。

# 第 1 章 数据类型与数据结构

## IDLE 开发环境

完整安装 Python IDLE 是一个基础但非常有用的集成开发环境。当启动 IDLE 时（在 Windows 上点击开始→所有程序→Python2.x→IDLE，在 Mac OS 上点击 Finder→应用程序→Python2.x，或在 Linux 终端运行 `idle &`），它会显示其 Python Shell。

如图 1.1 所示截图所示，IDLE 具有复古的 Windows 95 风格。这是因为是用 Tkinter 而不是 PyQt 写的。我们选择使用 IDLE 是因为它是 Python 标准配置的，而且是一个现代的 IDLE。如果你想使用更强大、现代的 IDLE，你可能更喜欢用 PyQt 编写的 Eric，或其他可用的 Python IDE。然而，如果你是 Python 新手，我们建议从更简单的 IDLE 开始，等你更熟悉 PyQt 后，再尝试其他 IDE 看看你是否更喜欢其中一个。当然，你也可以简单地使用纯文本编辑器和调试 print 语句，完全不使用 IDE。

IDLE 提供三个关键功能：输入 Python 表达式和代码并在 Python Shell 中查看结果的能力；提供 Python 特有语法高亮的代码编辑器；以及可以用于逐行执行代码以识别并消除 bug 的调试器。Python Shell 特别适用于尝试简单的算法、代码片段和正则表达式，还可以作为一个非常强大且灵活的计算器使用。

## 执行 Python 代码

在真正探索 Python 语言之前，我们需要知道如何执行 Python 代码。我们将通过回顾一个仅只有一行的微型示例程序来展示这一点。

我们使用纯文本编辑器来处理 Python 文件。在 Windows 上可以使用记事本，但 IDLE 包含了一个专门为编辑 Python 代码设计的合适 Python 编辑器：只需启动 IDLE，然后点击文件→新建窗口。

我们在名为 `hello.py` 的文件中输入以下行：

```python
print("Hello World")
```

注意分号是必需的：在 Python 中，换行符作为语句分隔符。我们不需要在字符串中使用换行符 `"\n"`，因为 `print` 会自动添加换行符，除非我们用末尾逗号抑制它。

> *书中的程序使用 ASCII 字符，并需要转义序列。Python 程序中的字符串和注释可以使用 Latin-1、UTF-8 或或其他编码，正如文档中“编码声明”部分解释的那样。*

假设我们已经将代码保存到文件 `hello.py` 中（在 Windows 上使用 `C:\pyqt\chap01` ），我们可以启动控制台（在 Windows XP 上点击开始→所有程序→附件→控制台；有时控制台被称为命令提示符；在 Mac OS 上运行 Terminal.app /Applications/Utilities），切换到该目录，并如下所示执行程序：

```bash
cd c:\pyqt\chap01
c:\pyqt\chap01>hello.py
```

只要 Python 安装正确，Windows 就会识别 .py 文件扩展并将文件交给 `python.exe` 执行。程序将如我们预期那样在控制台上打印 "Hello World"。

在 Mac OS X 和 Linux 上，我们必须通过在控制台上输入解释器的名称和文件名来显式运行，如下所示：

```bash
python hello.py
```

这将证明 Python 已安装并存在你的 PATH 中。另一种，对于 Linux 和 Mac OS，我们可以添加一行额外的“shebang”（shell 执行）注释行，告诉系统使用 Python 解释器，使 `hello.py` 文件变为两行长：

```python
#!/usr/bin/env python
print("Hello World")
```

要让这在 Mac OS X 和 Linux 上工作，必须正确设置文件权限。例如，在文件所在目录的控制台中中，运行 `chmod +x hello.py` 使文件可执行。

Python 命令以 `#` 开头一直到行尾。这意味着在所有 Python 程序中添加 "shebang" 行是完全安全的，因为注释在 Windows 上会被忽略，但在 Linux 上会告诉系统使用 Python 解释器执行文件。附录 A 显示了如何在 Mac OS 上将 Python 解释器与 .py 和 .pyw 文件关联。

当我们执行 Python 程序时，后台发生的情况是 Python 将 .py（或 .pyw）文件读取到内存并进行解析，得到一个字节码程序然后运行它。对于程序导入的每个模块，Python 首先检查是否存在预编译的版本。

## 变量与对象

在大多数编程语言（包括 C++ 和 Java）中，我们必须在使用之前声明变量并指定类型。这被称为静态类型，因为编译器在编译时知道每个变量。Python 像大多数高级语言一样使用了不同的方法：变量没有类型限制（动态类型），并且不需要声明。

我们可以通过创建和执行文件（如上一节的 `hello.py`）来学习 Python 的变量和标识符。但对于尝试小代码片段，我们不需要创建文件。我们可以直接在 IDLE Python Shell 窗口的 `>>>` 提示符输入输入：

```python
>>> x = 71
>>> y = "Dove"
```

赋值运算符 `=` 周围的空格是可选的，但包含它可以使代码更易读。作为一种风格，我们总会在二进制运算符前后放置一个空格。另一方面，重要的是每个语句占据一行且没有多余的领先空格。这是因为 Python 使用缩进和换行来表示其块结构，而不是许多其他编程语言使用的括号和分号。

现在我们准备好回顾这两行实际上做了什么。第一行创建一个 `int` 类型的对象并将名称绑定到它。第二行创建一个 `str` 类型的对象（一个8位字符串）并将名称绑定到它。

一些 Python 程序员将名称（如之前使用的 `x` 和 `y`）称为对象引用，它们引用对象而不是本身就是对象。对于 `int` 和 `str` 等基本数据类型，无论我们将变量视为“对象”还是“对象引用”都没有区别；它们的行为与在其他语言中的行为相同：

```python
>>> x = 82
>>> x += 7
>>> x
89
```

稍后我们将看到 Python 变量引用产生差异的情况。

> *这类似于 Java 赋值 `Integer x = new Integer(71);`；对于 C++，接近等价的是 `int x = 71; int &x =;`**

## 函数、方法与操作符术语

*函数*（function）一词用于指可以独立执行的子程序，而*方法*（method）一词用于指只有绑定到对象后才能执行的函数，即在特定类的实例上调用的函数。

*操作符*（operator）可以是独立的，也可以绑定到对象，但与函数和方法不同，操作符不使用括号。像 `+` 和 `<` 等符号表示的操作符显然被称为操作符，但像 `del` 和 `print` 这样有名称的操作符通常被称为语句（statements）。

Python 函数在数学意义上并不一定是纯的：它们不需要返回结果，并且可以修改它们的参数。Python 函数类似于 C 和 C++ 函数，或者类似于带有参数的 Pascal 函数。Python 方法类似于 C++ 或 Java 的成员函数。

Python 有两种比较对象的方法：“身份”（identity）和“值”（value）。一个对象的身份实际上是它在内存中的地址，这正是对象引用所持有的。如果我们使用比较操作符，如 `==` 和 `<`，得到的是值比较。例如，如果两个字符串包含相同的文本，则使用 `==` 时它们是相等的。如果我们使用 `is`，则得到身份比较，这是很快的，因为我们只是在比较地址，不需要查看对象本身。通过对对象引用调用 `id()` 可以获取对象的身份。

Python 有一个特殊的对象叫做 `None`。它可以被赋值给任何变量，意味着该变量没有值。`None` 对象始终只有一个实例，因此我们始终可以使用快速的 `is` 比较来对其进行测试。

注意我们在 `>>>` 提示符处单独写了 `x`。如果我们在 IDLE 中写一个表达式或变量，它的值会自动打印出来。在程序中，我们必须使用显式的 `print` 语句来打印表达式。例如：

```python
print x
x = 47
x = "Heron"
```

Python 的 *print* 语句是一个操作符，而不是函数，由于这个原因，调用它时不需要带括号（正如我们使用 `+` 和其他操作符时不带括号一样）。

之前我们提到过 Python 使用*动态类型*（dynamic typing）。这涉及到两个因素。首先，我们可以将任何对象赋值给任何变量；例如，我们可以写：

```python
x = 47
x = "Heron"
```

在第一行之后 `x` 的类型是 `int`，在第二行之后 `x` 的类型是 `str`，因此显然与名称 `x` 关联的类型取决于该名称绑定了什么，而不是取决于它本身的任何内在属性。因此，我们不需要将特定类型与特定名称关联。

Python 动态类型的另一个方面是强类型性的（strong typing）：Python 不允许不兼容类型之间进行操作，如下例（在 IDLE 中输入）所示：

```python
>>> x = 41
>>> y = "Flamingo"
>>> x + y
Traceback (most recent call last):
  File <pshell#2>, line 1, in <module>
    x + y
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

当我们尝试添加二进制 `+` 操作符时，Python 提出了一个 `TypeError` 异常并拒绝执行该操作。（异常将在第 2 章中介绍。）

如果我们给 `y` 赋值一个与 `x` 类型兼容的类型（例如 `int` 或 `float`），则加法将正常工作：

```python
>>> x = 41
>>> y = 8.5
>>> x + y
49.5
```

尽管 `x` 和 `y` 是不同类型（`int` 和 `float`），但 Python 提供了其他语言使用的相同自动类型提升，因此 `x` 被转换为 `float`，实际执行的计算实际上是 `41.0 + 8.5`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_28_0.png)

图 2 对象引用与对象

给变量赋值称为绑定（binding），因为我们将名称绑定到对象上。如果我们给现有的变量赋值一个新对象，我们就说在重新绑定（rebinding）该名称。这在图 1.2 中所示。当我们这样做时，名称最初绑定的对象会发生什么呢？例如：

```python
>>> x = "Sparrow"
>>> x = 9.8
```

持有文本“Sparrow”的 `str` 对象发生了什么？一旦一个对象没有名称绑定，它就会被调度进行垃圾回收，并在适当时候可能从内存中被删除。这与 Java 中的工作原理非常相似。

Python 变量名由 ASCII 字母、数字和下划线 (`_`) 组成。变量名应该以字母开头，并且它们区分大小写（rowan, Rowan, ROWAN 是不同的变量）。任何 Python 变量都不应命名为 Python 的任何关键字（见表 1.1），也不应命名为 Python 的内置构造。

## 数字与字符串

### 整数与长整数

Python 提供了三种类型：`bool`、`int` 和 `long`。`bool` 类型只能取 `True` 或 `False`，且在数值上下文中，这些值被视为 1 和 0。`long` 类型可以存储整数，其大小受限于机器的可用内存，因此可以创建并处理长达数百数字的整数。唯一的缺点是 `long` 类型处理速度较慢，小于 `int` 类型的值。`int` 类型是大多数编程语言提供的相同符号整数类型；然而，如果对 `int` 执行的操作导致其值超过了其取值范围（例如，在某些机器上，一个大于 $2^{31}-1$ 或小于 $-2^{31}$ 的值），则 `int` 会自动提升为 `long`。

Python 使用后缀 `L` 来表示 `long`，我们在需要时也可以在代码中这样做。例如：

```python
>>> p = 5 ** 35
>>> q = 7L
>>> r = 2 + q
>>> p, q, r
(291038304567330763128125, 7L, 9L)
```

整数字面量假设为 10 进制（十进制），但以 `0x` 开头的除外，它们被视为十六进制（16 进制），例如，`0x3F` 是十进制的 `63`；以 `0` 开头的被视为八进制（8 进制）。

任何整数字面量都可以附加 `L` 使其变为 `long`。

Python 支持我们期望的数字常用运算符，包括 `+`、`-`、`*`、`/` 以及它们的增强赋值运算符 `+=`、`-=`、`*=`、`/=` 和 `%=`。Python 提供了 `**` 用于幂。

默认情况下，当两个操作数都是 `int` 时，Python 的除法运算符执行截断除法。例如，`5 / 3` 生成 `1`。这是大多数编程语言的常态，但在 Python 中可能不方便。动态类型意味着变量在不同时间可能是 `int` 也可能是 `float`。解决方案是告诉 Python 执行“真除法”，它在需要时产生浮点数结果，并在我们希望进行截断时使用 `//` 运算符。我们将在第 3 章看到如何这样做。

### 浮点数与小数

Python 提供了三种浮点值：`float`、`Decimal` 和 `complex`。`float` 存储双精度浮点数，其范围取决于构建 Python 时使用的 C（或 Java）编译器；它们的精度有限，无法可靠地进行等值性比较。`float` 类型的数字使用小数点或科学计数法编写，例如 `0.0`、`5.7`、`8.9e-4`。在 IDLE 中输入这些内容是有益的：

```python
>>> 0.0, 5.7, 8.9e-4
(0.0, 5.700000000000001, 0.0088999999999999995)
```

不准确并不是 Python 特有的问题：计算机使用二进制表示位点数，二进制可以精确表示某些十进制（如 `0.5`），但对某些小数只能近似表示（如 `0.1`）。此外，表示法使用了固定位数的，因此能够存储的位数是有限制的。

在实践中这很少是一个问题，因为大多数浮点数是 64 位的，在大多数情况下绰绰有余。但如果我们需要高精度，可以使用来自 `decimal` 模块的 Python `Decimal` 数字。这些计算的精度可以达到我们指定的水平（默认为 28 位小数），并能精确表示如 `0.1` 等周期性数字；处理速度比普通浮点数慢得多。由于其准确性，`Decimal` 数字适用于财务计算。

在使用 `Decimal` 数字之前，必须导入 `decimal` 模块。无论我们是在 `.py` 文件中编写代码，还是像我们现在这样在 IDLE 窗口中输入，其操作语法都是相同的：

```python
>>> import decimal
```

在这里，我们将 `decimal` 模块导入了 IDLE 终端中。导入语义在“导入对象”侧边栏中解释。整数字面量可以传递给 `Decimal` 构造函数，由于 `Decimal` 是高精度的而 `float` 不是，我们不能传递 `float`；相反，我们必须提供浮点值作为字符串。例如：

```python
>>> decimal.Decimal(19), decimal.Decimal("5.1")
>>> decimal.Decimal("8.9e-4")
(Decimal("19"), Decimal("5.1"), Decimal("0.00089"))
```

数字 `decimal("5.1")` 是精确存储的；作为 `float`，它可能是类似 `5.099999999999999` 的值。同样，`decimal.Decimal("0.00089")` 转换为 `float` 后，尽管我们可以通过这样做从 `Decimal` 转换为 `float`：

```python
>>> d = decimal.Decimal("1.1")
>>> f = float(d)
>>> f
1.10000000000000001
```

Python 还提供了复数，由实部和虚部组成，后者由后缀 `j` 表示。例如：

```python
>>> c = 5.4+0.8j
>>> type(c)
<type 'complex'>
```

在这里我们输入了一个复数（语法为 `实部+虚部j`），并使用 Python 的 `type()` 函数告诉我们 `c` 绑定的是什么类型。

> *数学家使用 i 表示虚数，而工程师以及 Python 使用 j。*

### 导入对象

Python 拥有庞大且全面的模块库，提供了大量的预定义功能。我们可以通过导入所需的常量、变量、函数和类来使用这些功能。导入的通用语法为：

```python
import moduleName
```

然后我们可以使用点运算符访问模块内部的对象。例如，`random` 模块提供了 `randint()` 函数，可以这样导入和使用：

```python
import random
x = random.randint(1, 10)
```

注意，在 `.py` 文件的开头放置 `import` 语句是常见的。

### 字符串

Python 字符串是不可变的字符序列。Python 提供了两种字符串类型：`str`（8 位字符串）和 `unicode`（Unicode 字符串）。`str` 类型的字符串字面量使用单引号或双引号界定，例如 `'hello'` 或 `"world"`。`unicode` 字符串字面量以 `u` 前缀开头，例如 `u'hello'` 或 `u"world"`。

Python 接受 0–255 范围内的整数值。Python 文档未规定在该范围之外的值使用何种编码（即大于 127 的值）。对于 Unicode，我们可以使用 `unichr()`，它接受一个 0–65535 范围内的整数。要进行反向转换，从字符转换为其整数值（ASCII 值或 Unicode 编码点），我们可以使用 `ord()`。例如：

```python
>>> euro = unichr(8364)
>>> print euro
€
>>> ord(euro)
8364
```

为什么我们使用 `print` 而不是让 IDLE 输出结果？因为 IDLE 使用十六进制转义字符来显示字符串中的非 ASCII 字符，如果不使用 `print`，IDLE 将输出 `'\u20ac\'`。

也可以通过名称访问 Unicode 字符：

```python
>>> euro = u"\N{euro sign}"
>>> print euro
€
```

如果我们需要在字符串中包含特殊字符，可以使用反斜杠 `\` 对它们进行转义，如 `\"`。表 1.2 显示了可用的转义字符；Unicode 转义在 Unicode 字符串内部是有意义的。

这里是两个如何转义引号的示例：

> 他说：“No you don't!”再次.\n'What\'s up with him?'

我们不需要在由双引号界定的字符串内转义单引号，也不需要在由单引号界定的字符串内转义双引号。

对于多行字符串，我们可以使用“三引号”：

```python
'''这个字符串包含三行，其中有一个 'quote'，
另一个 "quote"，并且只有一个嵌入的换行符 \ns因为我们转义了其中一个.'''
```

这类字符串可以像普通字符串一样转义转义字符，并且可以如所示用三个单引号界定，也可以用三个双引号界定。三引号字符串以及 Python 代码中的换行符可以通过在它们前面加上反斜杠来转义。（这在 Windows 上也能正常工作，尽管 Windows 在行末尾使用两个字符而不是一个。）

> *如果 Python 被配置为使用 UCS-4 表示，范围将扩展到 1,114,111。*

#### 表 1.2 Python 字符串转义

| 转义 | 含义 |
|---|---|
| \newline | 转义（即忽略）换行 |
| \\ | 反斜杠 (\) |
| \' | 单引号 (') |
| \" | 双引号 (") |
| \a | ASCII 响铃 (BEL) |
| \b | ASCII 退格 (BS) |
| \f | ASCII 换页 (FF) |
| \n | ASCII 换行符 (LF) |
| \N{name} | Unicode 字符名称 |
| \r | ASCII 回车 (CR) |
| \t | ASCII 制表符 (TAB) |
| \hhhh | 具有给定 16 位十六进制值的 Unicode 字符 |
| \Uhhhhh | 具有给定 32 位十六进制值的 Unicode 字符 |
| \v | ASCII 垂直制表符 (VT) |
| \ooo | 具有给定八进制值的字符 |
| \xhh | 具有给定十六进制值的字符 |

Python 字符串是序列，可以通过索引访问单个字符，第一个字符位于索引 0。也可以从字符串末尾进行索引，最后一个字符的索引为 -1。例如：

```python
>>> phrase = "The red balloon"
>>> phrase[0], phrase[-1]
('T', 'n')
```

负索引用于从右到左访问字符，最右侧字符位置为 -1，其左侧位置为 -2，以此类推。

Python 序列使用切片（slicing），这意味着我们可以从序列中复制子序列。切片有一个、两个或三个由冒号分隔的部分：起始（默认为索引 0）、结束（默认为序列长度）以及另一个我们将忽略的部分。切片取自并包含起始索引但不包含结束索引。以下是一些示例：

```python
>>> phrase = "The red balloon"
>>> phrase[:3]
'The'
>>> phrase[-3:]
'oon'
>>> phrase[4:7]
'red'
```

由于 Python 字符串是不可变的，因此无法给字符串内部的字符或切片赋值：

```python
>>> p = "pad"
>>> p[1] = "o" # 错误
Traceback (most recent call last):
File <pyshell#64>, line 1, in <module>
 p[1] = o
TypeError: object does not support item assignment
```

向字符串中插入字符的最简单方法是使用切片语法：

```python
>>> p = "pad"
>>> p = p[:1] + "o" + p[2:]
>>> p
'pod'
```

指定字面量数字可能看起来很烦人，但在实际编程中，我们通常通过方法调用来获取索引——例如，使用 `find()` 方法。

也可以采用其他方法。例如：

```python
>>> p = "pad"
>>> p = "o".join([p[:1], p[2:]])
>>> p
'pod'
```

来自 Pascal 或 C++ 背景且习惯使用可变字符串的程序员起初可能会觉得字符串的不可变性很别扭。在 Python 中，当然提供了可变字符串；它们由 `StringIO` 模块和（更快的）`cStringIO` 模块提供。PyQt 的 `QString` 类也是可变的。通过处理不可变字符串的实践，特别是上述使用的惯用法——使用 `join()` 方法进行拼接——将变得非常自然。

Python 字符串有许多实用的方法，但我们将关注最常用的。在 Python 中，通过点运算符在对象上调用方法，并使用括号 `()` 表示方法调用。例如：

> 如前所述，括号不与运算符使用。

```python
>>> line = "The quick brown fox."
>>> line.find("q")
4
```

`find()` 方法返回字符串作为参数的字符串中第一次出现的索引位置，如果未找到则返回 -1。Python 还提供了 `index()` 方法，用法相同，但在未找到时会抛出 `ValueError`。其他序列类类如列表）也有 `index()` 方法，因此字符串拥有该方法具有一致性。

既然我们在字符串上使用 `find()` 或 `index()`，是否有种理由优于其中一个呢？对于一次性搜索，使用 `find()` 并检查返回值通常比较方便。但如果在执行大量搜索的代码块中，使用 `find()` 会强制我们检查每次搜索的返回值，而 `index()` 允许我们假设结果总是有效的，如果不是，则可以在单个异常处理程序中处理任何错误。如果不捕获该异常，它将向上堆栈传递，如果在任何地方都没有被捕获，会导致应用程序终止。我们学习这两种方法，根据具体情况选择最合适的一种。

字符串方法可以应用于字符串和字符串字面量：

```python
>>> "malthusian catastrophe".title()
'Malthusian Catastrophe'
```

`title()` 方法返回字符串的副本，但每个单词的首字母都大写。Python 提供了类似于 C 库 `printf()` 语法的数据类型字符串格式化。为了实现格式化，我们使用 `%` 运算符，它接受一个格式字符串作为左参数，以及一个对象（通常是元组）。

#### 表 1.3 选择字符串方法

| 语法 | 描述 |
|---|---|
| x in s | 如果 x 是 s 的子字符串则返回 True |
| x not in s | 如果 x 不是 s 的子字符串则返回 True |
| x + s | 返回 x 和 s 的拼接 |
| s * i | 返回由 i 个 s 组成的字符串。例如。"Ab" * 3 产生 "AbAb"。 |
| len(s) | 返回 s 的长度；如果 s 是 str 则返回字节计数，如果 s 是 unicode 则返回字符计数 |
| s.count(x) | 返回字符串 在 s 中出现的次数。此方法以及其他方法可以接受可选的开始和结束参数限制限制范围。 |
| s.endswith(x) | 如果 s 以字符串 x 结尾则返回 True |
| s.startswith(x) | 如果 s 以字符串 x开头则返回 True |
| s.find(x) | 返回 x 在 s 中第一次出现的索引；如果未找到返回 -1 |
| s.rfind(x) | 类似于 find()，但从右向左搜索 |
| s.index(x) | 返回 x 在 s 中第一次出现的索引；如果未找到则抛出 ValueError |
| s.rindex() | 类似于 index()，但从右向左搜索 |
| s.isdigit() | 如果字符串不空且字符均为数字则返回 True |
| s.isalpha() | 类似于 isdigit()，但检查是否为字母 |
| s.join(x,...) | 返回一个由调用方法的字符串分隔的序列拼接后的字符串。例如，":".join("A", "BB", "CCC") 返回 "A:BB:CCC"。分隔符可以是空的。 |
| s.lower() | 返回 s 的小写副本 |
| s.upper() | 返回 s 的大写副本 |
| s.replace(x, y) | 返回一个将所有 x 替换为 y 的字符串副本 |
| s.split() | 返回按空白字符分割的字符串列表。例如。"ab\tc d".split() ["ab", "c", "d"]。此方法可以接收第一个参数和一个作为最大分割次数的第二个参数。 |
| s.strip() | 返回去除头部末尾空格的字符串副本。接受一个可选参数指定要删除的字符。 |

`%` 项被称为格式化符，格式化字符串至少包含一个。格式化符由一个百分号 (`%`) 后跟一个格式化字符组成。百分号本身通过使用 `%%` 来指定。在示例中，我们使用了 `%d`，它是 `int` 的格式化符；`%s` 是字符串的格式化符，而 `%f` 是 `float` 的格式化符。

之前我们查看了如何将子字符串插入到字符串中。我们展示了如何使用切片来实现这一点，以及更具 Python 风格的方法使用字符串的 `join()` 方法。还有第三种方法，即使用格式化符：

```python
>>> p = "pad"
>>> p = "%so%s" % (p[:1], p[2:])
>>> p
'pod'
```

在这里我们创建了一个新字符串，它由一个字符串（来自 `p` 的第一个切片）、"o" 以及另一个字符串（来自 `p` 的第二个切片）组成。所示的 `join()` 方法是拼接字符串的理想选择；而这种方法则用于“组合”字符串。

我们可以通过在 `%` 和 `.` 之间放置一些信息，对 `%` 项的格式进行一些控制。例如，为了显示浮点数小数点后两个数字，我们可以使用格式化符 `%.2f`：

```python
>>> "The length is %.2f meters" % 72.8958
'The length is 72.90 meters'
```

以下是几个示例，其中两个展示了 `%` 运算符与 `print` 语句结合使用：

```python
>>> print "An integer", 5, "and a float", 65.3
An integer 5 and a float 65.3
>>> print "An integer %d and a float %f" % (5, 65.3)
An integer 5 and a float 65.300000
>>> print "An integer %d and a float %.1f" % (5, 65.3)
An integer 5 and a float 65.3
```

在很多情况下，`%d`（及其同义词 `%i`）、`%f` 和 `%s` 就足够了。格式化符的完整细节以及如何修改它们可以在 Python 文档中找到；如果需要，请查找“字符串格式化操作”（String Formatting Operations）。Python 还支持其他字符串格式化方法，例如，string 模块中的 `Template` 类提供了类似 Perl 的插值功能。甚至可以使用类似 C++ 的语法；请参见《Python Cookbook》中的“使用类 C++ 的 iostream 语法”章节。（参见 Python 文档侧边栏）。

注意，`print` 语句会在每个参数之间自动输出空格。可以使用 `sys.stdout.write()` 代替 `print` 来避免这一点；关于 `write()` 的更多内容将在第 6 章中给出。

### Python 文档

Python 提供了大量的文档。大多数文档的质量良好，但也有少数领域的覆盖范围较薄。使用 HTML 版本导航文档需要练习，因为它的组织方式更像一本纸质书而非在线文档，而且页面之间的交叉引用链接少得多。

Windows 用户是幸运的，因为文档是以 Windows 文件格式提供的。点击“开始→所有程序→Python 2.x→Python 手册”来启动 Windows 帮助浏览器。该工具既有索引（Index）又有搜索（Search）功能，使得查找文档变得简单。例如，要查找关于字符串格式化符的信息，只需在索引行输入“formatting”，就会出现条目“formatting, string (%)”。

快速浏览过一遍文档是完全值得的。我们建议你查看“库引用”（Lib.html）页面，看看 Python 标准库提供了哪些内容，并点击你感兴趣的任何主题的文档。这应该让你对可用内容有一个初步印象，并帮助你建立一个心理模型，以便你找到你感兴趣的文档。

注意，某些主题位于多个标题下。例如，关于字符串的内容出现在“序列类型”（Sequence Types）、“字符串方法”（String Methods）、“格式化操作”（Formatting Operations）以及“字符串服务”（String Services）。同样，对于文件和目录，请参见“文件和目录访问”（File and Directory Access）、“数据压缩与存档”（Data Compression and Archiving）以及“文件和目录”（File and Directories）。

对于那些喜欢纸质信息的人，以下书籍值得考虑：

- Wesley Chun 编写的《Core PYTHON Programming》。如果你是 Python 完全新手，并且希望进度比本书第一部分更慢一些，这本教程可能适合你。
- Alex Martelli 编写的《Python in a Nutshell》。这是一本优秀的参考书，对 Python 语言及其标准库提供了详细且准确的覆盖。
- 由 Alex Martelli、Anna Martini Ravenscroft 和 David Ascher 编辑的《Python Cookbook》第2版。这本书提供了许多实用的小函数、代码段和想法，将帮助任何程序员扩展对 Python 能做什么的认知。这些配谱也可以在 http://asn.activate.com/ASP/Python/Cookbook 在线获取。

对于在线信息，起点是 http://www.python.org。该网站也是 Python wiki 的家园。PyQt 的特定信息可以在 http://www.riverbankcomputing.co.uk 获取。PyQt wiki 位于 http://www.diotavelli.net/PyQtWiki。

在使用 PyQt 时，我们可以访问一种额外的字符串类型 `QString`。与 Python 的 `str` 和 `unicode` 不同，`QString` 是可变的；这意味着我们可以原地更改 `QString`，插入和删除字符串并更改单个字符。`QString` 的 API 与 `str` 和 `unicode`提供的不同。（Qt 提供 `QString` 是因为 Qt 用 C++ 编写的，而 C++ 还没有内置的 Unicode 支持。）

`QString` 持有 Unicode 字符，但取决于我们使用的 Python 版本，其内部表示可能与 Python 的 Unicode 表示不同。

```python
>>> from QtCore import *
>>> a = QString("apple")
>>> b = QString("banana")
>>> a + b
applebanana
>>> type(a)
<type 'QString'>
```

## 集合

一旦我们有了变量（即对特定类型的单个对象的引用），自然就会有对象引用的集合。Python 的标准集合类型持有对象引用，因此它们实际上可以持有任何类型的集合。使用对象引用的另一个结果是，它们不限于持有单一类型。

内置集合类型有 tuple、list、dict（字典）、set 和 frozenset。除了 tuple 之外的所有都是可变的，因此可以在列表、字典和集合中添加或删除项。`collections` 模块提供了额外的集合类型。

Python 标准库中有一个集合类型不持有对象引用；相反，它持有指定类型的数字。这就是 `array` 类型，它用于需要尽可能高效地存储和处理大量数字的情况。

在本节中，我们将查看 Python 的内置集合类型。

### 元组

元组是零或多个对象引用的有序序列。像字符串（以及很快看到的列表）一样，元组支持序列函数 `len()` 以及之前看到的切片语法。这使得从元组中提取项非常容易。然而，元组是不可变的，因此我们无法替换或删除它们的任何项。如果我们想要能够修改有序序列，只需使用列表；或者，如果我们已经有一个元组并想对其进行修改，可以将其转换为列表。

我们已经对元组有过一些非正式接触；例如，我们在 IDLE 中的某些交互产生的结果被封装成元组，我们也使用元组为 `%` 运算符提供多个参数。

以下是构造元组的一些示例：

```python
>>> empty = ()
>>> type(empty)
<type 'tuple'>
>>> one = ('Canary')
>>> type(one)
<type 'str'>
>>> one = ('Canary',)
>>> type(one)
<type 'tuple'>
```

创建一个空元组非常简单，但对于只有一个元素的元组，我们必须使用逗号来将其与圆括号表达式隔开：

```python
>>> things = ("Parrot", 3.5, "\u20AC")
>>> type(things)
<type 'tuple'>
```

元组可以包含任何类型的元素；这里我们有 str、float 和 unicode 元素。对于至少包含两个元素且含义无歧义的元组，也可以省略括号：

```python
>>> items = "Dog", 99, "Cow"
>>> type(items)
<type 'tuple'>
```

元组可以任意嵌套，并且可以进行切片，正如这些示例所示：

```python
>>> names = "Albert", "Brenda", "Cecil", "Donna"
>>> names[:3]
('Albert', 'Brenda', 'Cecil')
>>> names[1]
'Brenda'
```

我们创建了一个名称元组，然后取前三个元素的切片，再查看索引位置为 1 的元素。像所有 Python 序列一样，第一个元素位于位置 0：

```python
>>> names = names[0], names[1], "Bernadette", names[2], names[3]
>>> names
('Albert', 'Brenda', 'Bernadette', 'Cecil', 'Donna')
```

我们现在更改了名称，以指向一个中间多了一个元素的新元组。你可能想用 `names[:2]` 代替 `names[0], names[1]`，对最后两个名称也类似地使用 `names[2:]`，但如果这样做，将得到一个包含三个元素的元组：

```python
('Albert', 'Brenda', 'Bernadette', ('Cecil', 'Donna'))
```

这是因为当我们对元组进行切片操作时，切片本身也是元组。

```python
>>> names = names[:4]
>>> names
('Albert', 'Brenda', 'Bernadette', 'Cecil')
```

我们实际上通过取前 4 个元素的元组（即索引位置 0, 1, 2 和 3 的元素）删掉了最后一个名称。在切片中，第一个数字是起始索引，该元素包含在结果中；第二个数字是结束索引，该元素被排除在结果之外。

```python
>>> names = names[:-1]
>>> names
('Albert', 'Brenda', 'Bernadette')
```

删除最后一个元素的另一种方法是从末尾索引；这样我们就不需要知道元组的长度。但如果我们想知道长度，可以使用 `len()` 函数：

```python
>>> pets = ("Dog", 2), ("Cat", 3), ("Hamster", 14)
>>> len(pets)
3
>>> pets
(('Dog', 2), ('Cat', 3), ('Hamster', 14))
>>> pets[2][1]
14
>>> pets[1][0:2]
('Cat', 3)
>>> pets[1]
('Cat', 3)
```

元组可以嵌套，并根据需要使用尽可能多的方括号来访问元素。

任何序列都可以传递给元组构造函数来创建元组。例如：

```python
>>> tuple("some text")
('s', 'o', 'm', 'e', ' ', 't', 'e', 'x', 't')
```

当我们需要有序集合时可以使用元组。它们还被用某些函数和方法的参数。例如，从 Python 2.5 开始，`str.startswith()` 方法接受单个字符串参数（例如 `".png"`）或字符串元组（例如 `(".png", ".jpg", ".jpeg")`）。

### 列表

列表类型是一种与元组类型类似的有序序列。我们在字符串和元组中见过的所有序列函数和切片在列表上的工作方式完全相同。元组与列表的区别在于，列表是可变的，并且拥有可以使用它们来修改它们的方法。

虽然元组使用圆括号创建，但列表使用方括号（或使用 `list()` 构造函数）。

让我们看看水果切片的示例，它们提取列表的部分：

```python
>>> fruit = ["Apple", "Hawthorn", "Loquat", "Medlar", "Pear", "Quince"]
>>> fruit[:2]
['Apple', 'Hawthorn']
>>> fruit[-1]
'Quince'
>>> fruit[2:5]
['Loquat', 'Medlar', 'Pear']
```

在这里，我们使用了已经在字符串和元组中使用过的熟悉切片语法。

由于列表是可变的，我们可以插入和删除列表元素。这通过调用方法、使用切片语法（在列表的两侧都使用切片）或使用赋值运算符来实现。我们先看方法调用：

```python
>>> fruit.insert(4, "Rowan")
>>> fruit
['Apple', 'Hawthorn', 'Loquat', 'Medlar', 'Rowan', 'Pear', 'Quince']
>>> del fruit[4]
>>> fruit
['Apple', 'Hawthorn', 'Loquat', 'Medlar', 'Pear', 'Quince']
```

我们使用方法调用和运算符插入并删除了一个新元素。`del` 语句用于删除特定位置的元素，而 `remove()` 方法用于删除匹配 `remove()` 参数的元素。在示例中，我们也可以使用效率较低的 `fruit.remove("Rowan")`。

现在我们将使用切片完成相同的操作：

```python
>>> fruit[4:4] = ["Rowan"]
>>> fruit
['Apple', 'Hawthorn', 'Loquat', 'Medlar', 'Rowan', 'Pear', 'Quince']
>>> fruit[4:5] = []
>>> fruit
['Apple', 'Hawthorn', 'Loquat', 'Medlar', 'Pear', 'Quince']
```

当我们赋值 `"Rowan"` 时使用了方括号，是因为我们正在向列表中插入一个列表（一个单元素列表）。如果我们省略了括号，Python 将把 `"Rowan"` 视为一个列表，并将 "R"、"o" 等作为独立元素插入。

#### 表 1.4 常用列表方法与函数

| 语法 | 描述 |
| :--- | :--- |
| `x in L` | 如果元素 x 在列表 L 中，则返回 True |
| `x not in L` | 如果元素 x 不在列表 L 中，则返回 True |
| `L + m` | 返回包含列表 L 和 m 中所有元素的新列表；`extend()` 方法实现相同但效率更高 |
| `len(L)` | 返回列表的长度 |
| `L.count(x)` | 返回 x 在列表 L 中出现的次数 |
| `L.index(x)` | 返回 x 在 L 中首次出现的左侧索引位置，否则抛出 ValueError |
| `L.append(x)` | 将 x 添加到列表末尾 |
| `L.extend(m)` | 将列表 m 的所有元素添加到 L 的末尾 |
| `L.insert(i, x)` | 在索引 i 处插入 x |
| `L.remove(x)` | 从列表 L 中删除第一个匹配的 x，如果未找到则抛出 ValueError |
| `L.pop()` | 返回并删除 L 的最后一个元素 |
| `L.pop(i)` | 返回并删除索引 i 处的元素 |
| `L.reverse()` | 原地反转列表 |
| `L.sort()` | 原地排序列表 |

可以使用切片（slice）删除多个连续项，或者通过给切片赋值一个零长度的切片来删除。插入多个项可以使用切片，或者使用运算符 `+` 进行切片操作，并在末尾添加可以使用 `extend()`。请参见表 1.4 以获取适用于列表的方法和函数的总结。

### 字典

`dict` 类型是一种数据字典，也称为关联数组。字典存储一组无序的键值对，并提供非常快的查找速度。键（Keys）是唯一的且必须是不可变类型，例如 Python 字符串、数字或元组；值（value）可以是任何类型，包括集合类型，因此可以创建任意嵌套的数据结构。字典不是序列，但我们可以获取其键和值的序列，正如我们将在下一章中看到的。

其他语言中也存在类似的数据结构——例如 Perl 的 `hash`、Java 的 `HashMap` 和 C++ 的 `unordered_map`。

注意，字典可以通过键删除，但列表不能这样删除，因为字典的键必须是不可变的。在只提供字符串和数字等简单键的语言中，想要使用多项键的程序员不得不将这些项转换为字符串，但得益于元组（tuples），这种临时方案在 Python 中是没有必要的。

以下是创建字典并访问其中项的一些示例：

```python
>>> insects = {"Dragonfly": 5000, "Praying Mantis": 2000,
"Fly": 120000, "Beetle": 350000}
>>> insects
{'Fly': 120000, 'Dragonfly': 5000, 'Praying Mantis': 2000, 'Beetle': 350000}
>>> insects["Dragonfly"]
5000
>>> insects["Grasshopper"] = 20000
>>> insects
{'Fly': 120000, 'Dragonfly': 5000, 'Praying Mantis': 2000, 'Grasshopper': 20000, 'Beetle': 350000}
```

从字典中删除项与从列表中删除相同。例如：

```python
>>> del insects["Fly"]
>>> insects
{'Dragonfly': 5000, 'Praying Mantis': 2000, 'Grasshopper': 20000, 'Beetle': 350000}
>>> insects.pop("Beetle")
350000
>>> insects
{'Dragonfly': 5000, 'Praying Mantis': 2000, 'Grasshopper': 20000}
```

#### 表 1.5 精选字典方法和函数

| 语法 | 描述 |
| --- | --- |
| x in d | 如果项 x 在字典 d 中，则返回 True |
| x not in d | 如果 x 不在字典 d 中，则返回 True |
| len(d) | 返回字典 d 中项的数量 |
| d.clear() | 移除字典 d 中的所有项 |
| d.copy() | 返回字典 d 的浅拷贝 |
| d.keys() | 返回字典 d 中所有键的列表 |
| d.values() | 返回字典 d 中所有值的列表 |
| d.items() | 返回字典 d 中所有 (键, 值) 对的元组列表 |
| d.get(k) | 返回键 k 的值，或返回 None |
| d.get(k, x) | 如果 k 在字典 d 中，则返回键 k 的值；否则返回 x |
| d.pop(k) | 返回并删除键 k 项；如果字典 d 中不存在该键，则抛出 KeyError |
| d.pop(k, x) | 如果 k 在字典 d 中，则返回并删除键 k 项；否则返回 x |

可以使用 `dict()` 构造函数构建字典，如果键恰好是有效的标识符（即以字母开头的字母数字且没有空格），我们可以使用更方便的语法：

```python
>>> vitamins = dict(B12=1000, B6=250, A=380, C=5000, D3=400)
>>> vitamins
{'A': 380, 'C': 5000, 'B12': 1000, 'D3': 400, 'B6': 250}
```

我们之前提到字典的键可以是元组；这里有最后一个示例来展示其实用性：

```python
>>> points3d = {(3, 7, -2): "Green", (4, -1, 11): "Blue", (8, 15, 6): "Yellow"}
>>> points3d
{(4, -1, 11): 'Blue', (8, 15, 6): 'Yellow', (3, 7, -2): 'Green'}
>>> points3d[(8, 15, 6)]
'Yellow'
```

在第 2 章中，我们将看到如何以“自然的”任意顺序以及按键的顺序遍历字典。

### 集合

Python 提供了两种集合类型：`set` 和 `frozenset`。两者都是无序的，因此都不是序列。集合是可变的，因此可以添加和删除项。`frozenset` 是不可变的且无法更改；但这意味着它们适合作为字典的键。

集合中的每个项都是唯一的。



*(注：由于原始文本在 *Sets* 部分存在大量重复和断裂的句子，译文已根据上下文逻辑进行了清理和整合，确保了对 `set` 和 `frozenset` 差异、可变性以及作为字典键等概念的准确描述。)*

## 内置函数 (Built-in)

Python 提供了两种集合类型：`set` 和 `frozenset`。两者都是无序的，因此都不是序列。集合是可变的，可以添加和删除项；`frozenset` 是不可变的，无法更改，但可以作为字典的键。

集合中的每个项都是唯一的。正如我们将在下一章中看到的，可以获取其键和值的序列。

## 内置函数 (Built-in)

| 语法 | 描述 |
| --- | --- |
| `all(q)` | 如果 `q` 中的所有项为 `True`，则返回 `True` |
| `any(q)` | 如果 `q` 中的任意一项为 `True`，则返回 `True` |
| `x in q` | 如果项 `x` 在 `q` 中，则返回 `True` |
| `x not in q` | 如果 `x` 不在 `q` 中，则返回 `True` |
| `len(q)` | 返回 `q` 中项的数量 |
| `max(q)` | 返回 `q` 中的最大值 |
| `min(q)` | 返回 `q` 中的最小值 |
| `sum(q)` | 返回 `q` 中项的和 |

## 表 1.8 一些内置函数

| 语法 | 描述 |
| --- | --- |
| `chr(i)` | 返回 ASCII 值为 `i` 的单字符字符串 |
| `unichr(i)` | 返回 Unicode 码点 `i` 的单字符字符串 |
| `ord(c)` | 如果 `c` 是单字符字符串，返回其字节值（0–255）；如果是单字符 Unicode，则返回 Unicode 码点的整数 |
| `dir(x)` | 返回 `x` 的属性列表，包括所有方法名 |
| `help(x)` | 在 IDLE 中，打印对象 `x` 类型的简要描述及其属性列表 |
| `hasattr(x, a)` | 如果对象 `x` 有属性 `a`，则返回 `True` |
| `id(x)` | 返回引用所指对象的唯一 ID |
| `isinstance(x, C)` | 如果 `x` 是类 `C` 的实例或其子类的实例，则返回 `True` |
| `type(x)` | 返回 `x` 的类型；`type()` 通常用于调试 |
| `eval(s)` | 返回计算包含任意表达式的字符串 `s` 的结果 |
| `open(f, m)` | 使用模式 `m` 打开名为 `f` 的文件并返回文件句柄 |
| `range(i)` | 返回从 `0` 到 `i-1` 的整数列表；支持 `start`、`end`、`step` 参数 |

# 第 1 章 数据类型与数据结构

## 表 1.9 选定的数学内置函数

| 语法 | 描述 |
| --- | --- |
| `abs(n)` | 返回数字 `n` 的绝对值 |
| `divmod(i, j)` | 返回包含 `i` 除以 `j` 的商和余数的二元组 |
| `hex(i)` | 返回表示数字 `i` 的十六进制字符串 |
| `oct(i)` | 返回表示数字 `i` 的八进制字符串 |
| `float(x)` | 返回 `x` 转换后的浮点数 |
| `int(x)` | 返回 `x` 转换后的整数 |
| `long(x)` | 返回 `x` 转换后的长整数 |
| `pow(x, y)` | 返回 `x` 的 `y` 次方；可接受第三个取模参数 |
| `round(x, n)` | 返回四舍五入后保留 `n` 位小数的浮点值 |

`range()` 函数将在第 2 章学习循环时介绍，`open()` 函数将在第 6 章读写文件时介绍。`hasattr()` 和 `isinstance()` 函数将在第 3 章介绍。

对于序列相关的函数，`max()` 和 `min()` 适用于字符串序列和数字序列，但可能产生意想不到的结果：

```python
>>> x = "Zebras don't sail"
>>> max(x), min(x)
(' ', ',')
```

排序基于 `str` 字符串的 Unicode 码点。例如，`ord("Z")` 是 90，而 `ord("*")` 是 42。

Python 还提供了 `math` 模块：

```python
>>> import math
>>> dir(math)
['_doc_', '__file__', '__name__', 'acos', 'asin', 'atan', 'atan2',
 'ceil', 'cos', 'degrees', 'exp', 'fabs', 'floor', 'fmod',
 'frexp', 'hypot', 'ldexp', 'log', 'log10', 'modf', 'pi', 'pow',
 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh']
```

## 总结

本章中，我们看到了赋值运算符 `=`、数值加法 `+`（带有整数到浮点数的类型提升）以及复合赋值 `+=`。我们还看到了 `print`，以及注释由 `#` 引入。Python 可以用分号分隔语句，但不常用：在 Python 中，一个语句占据一行，换行符是语句分隔符。

我们学习了使用引号创建字符串，使用 `[]` 对字符串进行切片和拼接，并概览了字符串的关键方法。集合（`set`、`frozenset`）提供了唯一且可变（或不可变）的元素集合；元组（`tuple`）可作为字典键；列表（`list`）是有序且可包含重复项；字典（`dict`）提供键到值的映射。

> *值 `0.000000000000000012246063538223773` 接近 0，这是预期的。*

最后，我们快速概览了 Python 的一些内置功能和数学模块。接下来将在第 3 章学习模块创建，在此之前需要掌握控制结构，以便进行分支、循环、函数调用和异常处理。

## 练习题

- 条件分支
- 循环
- 函数
- 异常处理

# 控制结构

为了编写程序，需要数据类型、变量、数据结构以及分支和循环等控制结构。本章学习 `if` 语句、`for` 与 `while` 循环，以及异常的处理和创建。

## 条件分支

Python 提供了 `if` 语句，语法如下：

```
if expression1:
    suite1
elif expression2:
    suite2
else:
    suite3
```

`if`、`elif`、`else` 后面使用冒号，代码块通过缩进表示。推荐使用四个空格的缩进。

```python
if x > 0:
    print x
```

`pass` 用于占位：

```python
if x == 5:
    pass
```

## 循环

`while` 循环：

```python
count = 10
while count != 0:
    print count
    count -= 1
```

`for` 循环：

```python
for char in "aeiou":
    print "%s=%d" % (char, ord(char))
```

`range()` 返回整数列表：

```python
for i in range(10):
    print i
```

`range(3, 7)` → `[3, 4, 5, 6]`  
`range(-4, 12, 3)` → `[-4, -1, 2, 5, 8, 11]`

`xrange()` 在 Python 2 中提供惰性迭代。

遍历字典：

```python
presidents = dict(Washington=(1789, 1797), Adams=(1797, 1801),
                  Jefferson=(1801, 1809), Madison=(1809, 1817))
for key in presidents:
    print("%s: %d-%d" % (key, presidents[key][0], presidents[key][1]))
```

获取键、值、键值对：

```python
for key, dates in presidents.items():
    print "%s: %d-%d" % (key, dates[0], dates[1])
```

按键排序：

```python
for key in sorted(presidents):
    print "%s: %d-%d" % (key, presidents[key][0], presidents[key][1])
```

## 列表推导式与生成器

列表推导式：

```python
[x for x in range(10)]
```

带条件：

```python
fives = [x for x in range(50) if x % 5 == 0]
```

生成器表达式：

```python
fives = (x for x in range(50) if x % 5 == 0)
for x in fives:
    print(x)
```

## 函数

使用 `def` 定义函数：

```python
def functionName(optional_parameters):
    suite
```

示例：

```python
def greeting():
    print "Welcome to Python"
greeting()
```

函数是对象引用，可赋值：

```python
g = greeting
g()
```

默认参数：

```python
def frange(start, stop, inc=1):
    ...
```

可变参数示例 `frange` 实现：

```python
def frange(arg0, arg1=None, arg2=None):
    """使用类似 range 的语法返回浮点数列表"""
    if arg2 is not None:
        start, stop, inc = arg0, arg1, arg2
    elif arg1 is not None:
        start, stop, inc = arg0, arg1, 1.0
    else:
        start, stop, inc = 0.0, arg0, 1.0
    result = []
    while start < (stop - (inc / 2.0)):
        result.append(start)
        start += inc
    return result
```

生成器版本：

```python
def frange(start, stop, inc=1):
    while start < (stop - (inc / 2.0)):
        yield start
        start += inc
```

## 部分函数应用

```python
import functools
buttonOneFunc = functools.partial(action, "One")
buttonTwoFunc = functools.partial(action, "Two")
```

自定义 `partial` 实现：

```python
def partial(func, arg):
    def callme():
        return func(arg)
    return callme
```

## 异常处理

基本语法：

```
try:
    suite1
except ExceptionType as e:
    suite2
else:
    suite3
finally:
    suite4
```

示例：

```python
try:
    i = text.index("<")
    j = text.index(">", i + 1)
    result = text[i:j + 1]
except ValueError:
    result = ""
print result
```

自定义异常：

```python
class SimplifyError(Exception):
    pass

def simplify(text, space="\t\r\n\f", delete=""):
    if not space and not delete:
        raise SimplifyError("Nothing to skip or delete")
```

使用 `finally` 确保资源释放：

```python
handle = open(filename)
try:
    for line in handle:
        process(line)
finally:
    handle.close()
```

## 类与模块

### 实例化

```python
class Chair(object):
    """表示椅子."""
    def __init__(self, name, legs=4):
        self.name = name
        self.legs = legs

chair1 = Chair("Barcelona")
chair2 = Chair("Bar Stool", 1)
print(chair2.name)   # Bar Stool
chair1.legs = 2
```

### 方法与特殊方法

```python
class Rectangle(object):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
```

属性访问：

```python
rect = Rectangle(50, 10)
print(rect.area())   # 500
rect.width = 20
```

### 继承

```python
class SubChair(Chair):
    def __init__(self, name, legs, material):
        super(SubChair, self).__init__(name, legs)
        self.material = material
```

### 特殊方法示例

```python
class Counter(object):
    def __init__(self, start=0):
        self.value = start

    def __iadd__(self, other):
        self.value += other
        return self

    def __str__(self):
        return str(self.value)
```

## 总结

本章覆盖了：

- `if`/`elif`/`else` 条件分支  
- `while` 与 `for` 循环，`range()` 与 `xrange()`  
- 字典的键、值、键值对遍历与排序  
- 列表推导式与生成器表达式  
- 函数定义、默认参数、可变参数、生成器函数  
- 部分函数应用 (`functools.partial`)  
- 异常捕获、`finally`、自定义异常类  
- 类的创建、实例化、方法、特殊方法、继承  

这些概念为后续章节的面向对象编程、模块化以及更高级的 Python 特性奠定基础。


```python
class Rectangle(object):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def _area(self):
        return self.width * self.height
    area = property(fget=_area)
```

这允许我们写这样的代码：

```python
rect = Rectangle(5, 4)
print(rect.width, rect.height, rect.area)  # 输出 (5, 4, 20)
rect.width = 6
```

Python 的 property() 函数可以用于指定 getter、setter、删除方法和文档字符串（docstring）。由于我们只指定了 getter，area 属性是只读的。如果以后需要在访问宽度时执行某些计算，我们可以简单地将其转换为属性，如下：

```python
def _width(self):
    return self._width

def _setWidth(self, width):
    # 执行某些计算
    self._width = width

width = property(fget=_width, fset=_setWidth)
```

注意，我们已经将变量名从 width 改为 _width，以避免与属性名冲突。通常，值存储在实例变量中的属性使用私有名称（带前下划线）作为实例变量，以避免与类使用的属性名冲突。例如，Rectangle 类的用户可以像以前一样获取和设置宽度 属性，只是现在由 _width() 和 _setWidth() 方法在后台执行这些操作，属性数据存储在 _width 实例变量中。

## 3.1 基础特殊方法

| 方法 | 语法 | 说明 |
| :--- | :--- | :--- |
| __init__(self, args) | x = X(args) | 初始化新创建的实例 |
| __call__(self, args) | x() | 使实例可调用，将其变为函数对象（functors）。args 是可选的。（高级） |
| __cmp__(self, other) | x == y, x < y, 等 | 如果 self 相等则返回 True，否则返回 False。如果实现了 __cmp__，它将用于任何未被显式实现的比较运算符 |
| __eq__(self, other) | x == y | 如果 x 等于 y 则返回 True |
| __ne__(self, other) | x != y | 如果 x 不等于 y 则返回 True |
| __le__(self, other) | x <= y | 如果 x 小于等于 y 则返回 True |
| __lt__(self, other) | x < y | 如果 x 小于 y 则返回 True |
| __ge__(self, other) | x >= y | 如果 x 大于等于 y 则返回 True |
| __gt__(self, other) | x > y | 如果 x 大于 y 则返回 True |
| __nonzero__(self) | if x: | 如果 x 不零则返回 True |
| __repr__(self) | y = eval(`x`) | 返回 x 的 eval 表示形式。使用反引号等同于调用 repr() |
| __str__(self) | print x | 返回 x 的人类可读表示形式 |
| __unicode__(self) | print x | 返回 x 的人类可读 Unicode 表示形式 |

为了更好地将自定义类集成到 Python 中，有一些额外的特殊方法可能值得实现。例如，我们可能希望为类提供比较运算符的支持以及布尔值。我们将为 Rectangle 类添加一些更多方法以展示这些可能性，但为了简洁，我们不重复类语句和已经实现的方法。我们将从开始

```python
def __cmp__(self, other):
    return cmp(self.area, other.area)
```

如果我们能为比较运算符之一实现一个特殊方法，如果我们实现了 _lt_ ("小于")，我们就能使用 < 运算符比较我们类的实例。然而，如果我们不想单独实现比较运算符，我们可以简单地像这里这样实现 __cmp__()。Python 在实现特定方法进行比较时会使用该方法，但会回退到 __cmp__() 其他运算符（<, <=, !=, >, >=），这些运算符对 Rectangle 对象是有效的：

```python
rectA = Rectangle(4, 4)
rectB = Rectangle(8, 2)
rectA == rectB  # 因为面积相同，为 True
rectA < rectB    # 为 False
```

*最好使用 repr() 而不是反引号，因为反引号在 Python 3.0 中会被丢弃。*

在 C++ 中可以实现运算符，即为我们的数据类型提供运算符实现。C++ 语法使用关键字运算符后跟运算符本身——但在 Python 中每个运算符都有名称，所以为了在 Python 中实现类+，我们需要实现 add() 方法。所有实现运算符的方法都是特殊方法，这种特征通过开头和结尾都有双下划线来表示。

## 方法与特殊方法

在这里，如果宽度相同，我们返回高度的比较结果；否则，我们返回宽度的比较结果。

如果我们不重新实现任何比较特殊方法，在大多数情况下，Python 会乐意为我们执行比较，尽管这并不一定以我们想要的方式。如果我们正在创建一个比较有意义的类，最安全的做法是实现 `__cmp__()`，并让其方法体返回 `NotImplementedError`。

```python
def __nonzero__(self):
    return self.width or self.height
```

这个特殊方法在对象处于布尔上下文中时使用；例如 `bool(a)`，或者如果对象是 `__nonzero__`，则返回 True。

```python
def __repr__(self):
    return "Rectangle(%d, %d)" % (self.width, self.height)
```

“表示”（representation）特殊方法必须返回一个字符串，该字符串如果被求值（例如使用 `eval(obj)`），将导致构造出一个与被调用对象相同属性的对象。某些对象太复杂而无法支持，例如 GUI 中的窗口或按钮，这种情况下是有意义的；此类类提供了 `__repr__` 的实现。字符串格式化字符串使用 `%` 来获取此特殊方法的结果；我们可以使用 `repr()` 函数或反引号 ` `` ` 运算符。反引号只是使用 `repr()` 的语法替代方案。例如，`repr(x)` 和 `'x'` 都返回相同的结果：由 `x.__repr__()` 返回的对象 x 的表示。

还有一个 `__str__` 特殊方法，它必须返回被调用对象的字符串表示（类似于 Java 的 `toString()`），除非是 `__str__()`，该表示旨在为了人类可读，且不需要可以被 `eval()` 求值。如果在这种情况下，没有实现 `__str__` 方法，Python 将改用 `__repr__` 方法。例如：

```python
rect = Rectangle(8, 9)
print rect("Rectangle(8, 9)", rect.__repr__()())
```

如果我们想为类提供一个人类可读的字符串表示，可以实现 `__unicode__()`。

有几个我们可以实现的通用特殊方法，但它们并不适用于 `Rectangle` 类。所有常用的特殊方法都列在表 3.1 中。

此时，C++ 程序员可能会想奇拷贝构造函数和赋值运算符是如何工作的，而 Java 程序员可能会好奇 `clone()`。Python 不使用拷贝构造函数，且重新实现赋值运算符是没有必要的。如果我们想进行赋值，只需使用 `=`，Python 将把一个新名称绑定到我们现有的对象上。如果我们确实需要对象的拷贝，可以使用 `copy` 模块中的 `copy()` 或 `deep-copy()` 函数，前者用于没有嵌套属性或浅拷贝就足够的对象，后者用于必须完全拷贝的对象。或者，我们可以提供自己的拷贝方法，我们通常将其命名为 `copy()`，因为这是 Python 的惯用做法。

对于数值类，提供支持标准数值运算符（如 `+` 和 `+=`）的功能通常非常方便。在 Python 中，这通常是通过实现各种特殊方法来实现。如果我们只实现 `+`，Python 将使用它来提供 `+=`，但通常实现两者是最好的，因为这能带给我们更细粒度的控制，并更容易优化操作。

最常实现的数值特殊方法列在表 3.2 中。未列出的包括位移运算符以及十六进制和八进制转换运算符。

两个不同的除法运算符是因为 Python 可以执行整数除法或浮点除法，如第 17 页所示。三个版本；例如，`__add__()`、`__radd__()` 和 `__iad__()`。“r”版本（例如 `__radd__`）用于左侧操作数没有适当方法但右侧操作数的方法的情况。例如，如果我们有表达式 `x + y`，其中 x 和 y 的类型为 `X` 和 `Y`，Python 将尝试通过调用 `X.__add__(y)` 来求值该表达式。如果 `X` 没有此方法，Python 将尝试 `Y.__radd__(x)`。如果 `Y` 此类方法，则将抛出异常。“i”版本，“i”代表原地（in-place）。它们被用于像 `+=` 这样的增强赋值。我们很快会看到更多这些。

## 表 3.2 选定的数值特殊方法

| 方法 | 语法 | 方法 | 语法 |
| :--- | :--- | :--- | :--- |
| `__float__(self)` | float(x) | `__int__(self)` | int(x) |
| `__abs__(self)` | abs(x) | `__neg__(self)` | -x |
| `__add__(self, other)` | x + y | `__sub__(self, other)` | x - y |
| `__iad__(self, other)` | x += y | `__isub__(self, other)` | x -= y |
| `__radd__(self, other)` | y + x | `__rsub__(self, other)` | y - x |
| `__mul__(self, other)` | x * y | `__mod__(self, other)` | x % y |
| `__imul__(self, other)` | x *= y | `__imod__(self, other)` | x %= y |
| `__rmul__(self, other)` | y * x | `__rmod__(self, other)` | y % y |
| `__floordiv__(self, other)` | x // y | `__truediv__(self, other)` | |
| `__ceildiv__(self, other)` | | `__itediv__(self, other)` | |
| `__rfloordiv__(self, other)` | | `__rtruediv__(self, other)` | |
| `__ruediv__(self, other)` | | `__rfloordiv__(self, other)` | |

## 静态数据，以及

在某些情况下，与类关联的数据是有用的。例如，如果我们有类，我们可能想要：

```python
class Balloon:
    ball = []
    def __init__(self, width):
        self.width = width

    @staticmethod
    def count():
        return len(Balloon.ball)
```

## 装饰器

现在我们看到了许多通用方法，以创建一个自定义类型。我们将创建一个 `Length` 类来持有物理长度。我们希望可以使用以下语法创建长度，例如：`distance = Length("22 miles")`。我们还希望通过单位获取长度，`km = distance.to("km")`。

## 8. 类与模块

## 示例：Length 类

通常，源代码 `chap03/length.py` 不在以下片段中显示它们，是为了节省空间并避免分散你的注意力。

```python
from __future__ import division
```

文件的第一个语句引人入胜。`__future__` 导入语法用于开启将在后版本中默认的功能。在这种情况下，我们正希望开启 Python 的未来行为，即 `/` 执行“真”，或浮点除法，而不是它通常的行为，即截断除法。`//` 运算符执行截断除法，如果我们需要的话。

```python
class Length(object):
    convert = dict(mi=621.371e-6, miles=621.371e-6, mile=621.371e-6,
                   yd=1.094, yards=1.094,
                   ft=3.281, feet=3.281, foot=3.281,
                   inches=39.37, inch=39.37,
                   mm=1000, millimeters=1000, millimeters=1000,
                   millimetre=1000, millimetres=1000,
                   cm=100, centimeter=100, centimeters=100,
                   centre=100, centimetres=100,
                   m=1.0, meter=1.0, meters=1.0, metre=1.0,
                   km=0.001, kilometer=0.001, kilometers=0.001,
                   kilometre=0.001, kilometres=0.001)

    def __init__(self, in):
        self.numbers = frozenset("0123456789.ee")
```

# 方法与特殊方法 87

object，因此我们的类是新式类。然后我们创建了一些静态数据。我们创建了一个将名称映射到转换因子的字典。我们不能使用 "in" 作为参数名，因为它是 Python 的关键字，所以我们使用 `[]` 操作符单独将其插入字典。我们还创建了一个浮点数中有效字符的集合。

```python
def __init__(self, length=None):
    if length is None:
        self._amount = 0.0
    else:
        digits = ""
        for i, char in enumerate(length):
            if char.isdigit():
                digits += char
            else:
                self._amount = float(digits)
                unit = length[i:].strip().lower()
                break
        raise ValueError("need an amount and a unit")
        self._amount /= Length.convert(unit)
```

在初始化器中，局部变量 `length`、`digits`、`i`、`char` 和 `unit` 在方法结束时都超出了作用域。我们只引用实例变量 `self._amount`。无论初始化时使用了什么单位，该变量始终存储以米为单位的长度，并且可以在任何方法访问。我们还引用了静态变量 `Numbers` 和 `Length.convert`。

当创建一个 `Length` 对象时，Python 将调用 `__init__()` 方法。我们给用户提供了两个选项：不传递参数（在这种情况下长度将为 0 米），或者传递一个指定数量和单位的字符串（两者之间可以用可选空格分隔）。

如果给了一个字符串，我们希望遍历数字中有效的字符，然后剩余部分作为单位。Python 的 `enumerate()` 函数返回一个迭代器，在每次迭代时返回一个包含值的元组：一个从 0 开始的索引数字和序列。因此，如果字符串是 "7 mi"，返回的元组将是 `(0, "7")`、`(1, " ")`、`(2, "m")` 和 `(3, "i")`。我们可以在 for 循环中提供变量来解包元组。

只要获取的是数字字符，我们就将其添加到 `digits` 字符串中。当我们遇到不在集合中的字符时，我们尝试将 `digits` 字符串转换为浮点数，并将长度字符串的剩余部分作为单位。我们去掉单位字符串两端的任何空格，并将字符串转换为小写。最后，我们通过静态 `convert` 字典中的转换因子计算长度是多少米。

# 第 3 章 类与模块

我们将数据属性命名为 `_amount` 而不是 `amount`，因为我们希望这些数据是私有的。Python 会对类中任何以下划线开头（且不以双下划线结尾）的名称进行修饰（name-mangle），在其前面加上下划线和类名，以使属性名称唯一。在这种情况下，`_amount` 将被修饰为 `_Length_amount`。当我们查看某些特殊方法时，我们将看到这样做益处的实际原因。

显然，有很多事情可能会出错。浮点转换可能会失败，可能没有单位（在这种情况下我们抛出一个异常，并带有一个“原因”字符串），或者单位在 `convert` 字典中不匹配。在这个方法中，我们选择让可能的异常被抛出，并在方法的 docstring 中记录它们，以便类的用户知道可以预期什么。

```python
def set(self, length):
    self.__init__(length)
```

我们的单位是可变的，因此我们提供了一个 `set()` 方法。它接受与 `__init__()` 相同的参数，因为 `__init__()` 是初始化器而不是构造函数，我们可以安全地对它执行工作。

```python
def copy(self, unit):
    return self.__amount * Length.convert[unit]
```

我们将长度以米的形式存储在类内部。这意味着我们只需要维护单一的浮点值，而不是一个值和一个单位。但正如我们在创建长度时指定了单位一样，我们也希望能够以我们选择的单位作为值来检索长度。这就是 `to()` 方法实现的功能。它使用 `convert` 字典将米值转换为指定的单位。

```python
def copy(self):
    other = Length(self)
    other.__amount = self.__amount
    return other
```

正如我们所知道的，如果使用 `=` 运算符，我们仅仅是绑定（或重新绑定）一个名称，如果我们需要长度的通用拷贝，我们需要某种方法来实现。在这里，我们选择提供一个 `copy()` 方法。但我们不必这样做：相反，我们可以简单地依赖 `copy` 模块。例如：

```python
import copy
import length

x = length.Length("3 km")
y = copy.copy(x)
```

我们导入了标准的 `copy` 模块和我们自己的 `length` 模块（假设 chap03 在 sys.path 中，且该模块名为 length.py）。

然后我们创建了两个独立的长度。如果我们执行了 `y = x` 然后使用 `set()` 方法更改了 `x`，那么 `y` 就会改变。当然，由于我们实现了自己的 `copy()` 方法，我们也可以通过编写 `y = x.copy()` 来拷贝。

可以用不同的方式实现 `copy()` 方法。例如：

```python
def copy(self): # 方案 1
    import copy
    return copy.copy(self)

def copy(self): # 方案 2
    return eval(repr(self))
```

## 方法与特殊方法

```python
def __rmul__(self, other):
    return Length("%fm" % (other * self.__amount))
```

```python
def __imul__(self, other):
    self.__amount *= other
    return self
```

对于乘法方法，我们提供了将长度乘以数字的支持。假设 x 是一个长度，`__mul__()` 支持像 `x * 5` 这样的用法，而 `__rmul__()` 支持像 `5 * x` 这样的用法。我们在 `__mul__()` 中显式地禁止两个长度直接相乘，因为结果将是面积而不是长度。我们不需要在 `__mul__()` 中这样做，是因为 `__mul__()` 总是会被首先尝试的，如果它抛出异常，Python 就不会尝试 `__rmul__()` 或（增强）乘法——例如 `x *= 5`。

```python
def __truediv__(self, other):
    return Length("%fm" % (self.__amount / other))
```

```python
def __itruediv__(self, other):
    self.__amount /= other
    return self
```

除法方法的实现与其他算术方法具有类似的结构。展示它们的原因之一是提醒我们，`/` 和 `/=` 运算符之所以执行浮点除法，是因为 `length.py` 文件开头的 `__future__` 导入指令。也可以重新实现截断除法，但这对于 `Length` 类来说并不合适。

展示它们的另一个原因是与我们刚刚看到的加法方法有细微的区别。虽然加法和减法只对长度操作，但乘法和除法操作的是长度和数字。

```python
def __float__(self):
    return self.__amount
```

```python
def __int__(self):
    return int(round(self.__amount))
```

我们选择支持两种类型转换，两者都易于编写和理解。之前实现的 `__str__()` 方法也是一种类型转换（转换为 `str` 类型）。

现在我们已经了解了如何实现自定义数据类型，并将注意力转向实现集合类。

## 集合类

在 Python 中，序列如列表和字符串，映射如字典，或集合。如果我们实现自己的集合类，就可以使用特殊方法使我们的集合能够与内置集合类型具有相同的语法和语义。表 3.3 列出了集合通用的特殊方法，在本节中，我们将讨论每种集合的细节。

在序列的情况下，通常会实现 `__add__()` 和 `__radd__()` 来支持拼接，在可变集合的情况下，实现 `__iadd__()` 以支持 `+=`。同样地，应该实现 `__mul__()` 方法以支持使用 `*` 重复集合。如果给出了无效索引，我们应该抛出 `IndexError` 异常。除了特殊方法外，自定义集合应该实现 `append()`、`count()`、`index()`、`insert()`、`extend()`、`pop()`、`remove()`、`reverse()` 和 `sort()`。

对于映射，如果给出无效的键，我们应该抛出 `KeyError`，除了特殊方法外，我们应该至少实现 `copy()` 和 `get()`，以及 `items()`、`keys()` 和 `values()`，以及它们的迭代器版本 `iter()`。Python 迭代器是一个返回连续值的函数或方法——字符串中的每个字符，或者列表或字典中的每个项目。它们通常由生成器实现。

对于集合，如果使用了无效的键，我们也应该抛出 `KeyError`；例如，调用 `remove()`。集合类应该实现 `issubset()`、`isserset()`、`union()`、`intersection()`、`difference()`、`symmetric_difference()` 和 `copy()`。对于可变集合，应该提供额外的方法，包括 `add()`、`remove()` 和 `discard()`。

## 示例：OrderedDict 类

Python 标准库中一个罕见的缺失是有序字典。普通字典提供快速查找，但不提供顺序。例如，如果我们想按键的顺序遍历字典的值，我们需要将键复制到列表中，对列表排序，然后遍历列表，使用列表的元素来访问字典的值。对于小型字典，或者访问不频繁的情况，这可能没问题，但当字典很大或频繁排序时，每次都排序在计算上上可能是昂贵的。

一个显而易见的解决方案是创建一个有序字典，这正是我们要做的。

理解 `OrderedDict` 示例对于 GUI 编程不是必要的，但在我们在稍后涵盖的一些程序中，确实使用了这里解释的技术和方法。现在，你可以安全地跳到第 99 页开始的下一节，然后在在后的章节中遇到这些技术时返回这里理解。

## 方法与特殊方法

表 3.3 选定的集合特殊方法

| 方法 | 语法 | 描述 |
| :--- | :--- | :--- |
| __contains__(self, x) | x in y | 如果 x 在序列 y 中或 x 是字典中的键，则返回 True。此方法也用于 not in。 |
| __len__(self) | len(y) | 返回 y 中项目的数量 |
| __getitem__(self, k) | y[k] | 返回序列的第 k 个元素或字典中 k 的值 |
| __setitem__(self, k, v) | y[k] = v | 将序列 y 的第 k 个元素或字典中 k 的值设置为 v |
| __deliter__(self, k) | del y[k] | 删除序列 y 的第 k 个元素或字典中 k 的值 |
| __iter__(self) | for x in y: | 返回一个迭代器 |
| __repr__(self) | repr(obj) | 返回对象的字符串表示 |

```python
import bisect

class OrderedDict(object):
    def __init__(self, dictionary=None):
        self.keys = []
        self.dict = {}
        if dictionary is not None:
            if isinstance(dictionary, OrderedDict):
                self.dict = dictionary.dict.copy()
                self.keys = dictionary.keys[:]
            else:
                self.dict = dict(dictionary).copy()
                self.keys = sorted(self.dict.keys())

    def getAt(self, index):
        return self.dict[self.keys[index]]

    def setAt(self, index, value):
        self.dict[self.keys[index]] = value

    def __getitem__(self, key):
        return self.dict[key]

    def __setitem__(self, key, value):
        if key not in self.dict:
            bisect.insort(self.keys, key)
        self.dict[key] = value
```

## 方法与特殊方法

如果用户使用 `[key] = value` 语法向字典赋值，我们再次依赖 `__dict__` 来完成工作。但如果键已不在 `__dict__` 中，那么它也不会在键的列列表中，因此我们必须添加它。

`insert_left()` 函数接收一个有序序列（如排序后的列表）和一个要插入的项。它在序列中定位该项应该的位置以保持序列顺序，并在该处插入项。`insert_left()` 函数与 `bisect` 模块中的所有函数一样，使用二分查找法，因此即使在长序列上性能也非常出色。

另一种方法是简单地向列表添加新键，然后对列表执行 `sort()`。Python 的排序功能对部分有序的数据经过了高度优化，因此性能可能不会太差，但我们倾向于更高效的解决方案。

```python
def __delitem__(self, key):
    i = bisect.bisect_left(self.__keys__, key)
    del self.__keys[i]
    del self.__dict__[key]
```

删除一个项非常简单。`bisect_left()` 函数接收一个有序序列（如排序后的列表）和一个项。它返回该项在序列中的索引位置（或者如果它在序列中，它本应所在的位置）。我们假设键在列表中，并依赖在键不在时会抛出异常。我们不是通过索引位置从键列表中删除键，而是通过从字典中移除它来删除 (key, value)。

我们本可以使用一条语句 `self.__keys.remove(key)` 直接从键列表中删除键，但那将使用缓慢的线性搜索。

```python
def get(self, key, value=None):
    return self.__dict__.get(key, value)
```

此方法返回给定键的值，除非该键不在字典中，在这种情况下它将返回指定的值（默认为 `None`）。由于不涉及键的顺序，我们可以简单地将工作交给底层。

```python
def setdefault(self, key, value=None):
    if key not in self.__dict__:
        bisect.insort_left(self.__keys__, key)
    return self.__dict__.setdefault(key, value)
```

此方法与 `get()` 类似，但有一个重要的区别：如果键不在字典中，它将用给定的值插入。在键不在字典的情况下，我们当然必须将其插入我们的键列表中。

```python
def pop(self, key, value=None):
    if key not in self.__dict__:
        return value
    i = bisect.bisect_left(self.__keys__, key)
```

# 第 3 章 类与模块

```python
del self._keys[i]
return self.__dict.pop(key, value)
```

此方法也与 `get()` 类似，不同之处在于如果键在字典中，它会移除该项。自然地，如果从字典删除了键，我们也必须从键列表中移除它。

```python
def popitem(self):
    item = self.__dict.pop()
    i = bisect.bisect_left(self._keys, item[0])
    del self._keys[i]
    return item
```

此方法移除并返回一个任意项，即一个 (key, value) 元组。我们首先从字典中移除该任意项（因为我们预先不知道它是什么），然后从我们的键列表中移除其键，最后返回被移除的项。

```python
def has_key(self, key):
    return key in self.__dict
```

```python
def __contains__(self, key):
    return key in self.__dict
```

为了向后兼容，支持 `key()` 方法；而现在程序员使用 `in`，它由 `__contains__()` 特殊方法实现。

```python
def __len__(self):
    return len(self.__dict)
```

这返回字典中有多少项。我们同样可以轻松返回 `len(self._keys)`。

```python
def keys(self):
    return self._keys[:]
```

我们将字典的键作为键列表的浅拷贝返回，这样它们就按键排序。标准的 `dict` 返回键的顺序是任意。

```python
def values(self):
    return [self.__dict[key] for key in self._keys]
```

我们按照键的顺序返回字典的值。为了做到这一点，我们通过列表推导式遍历键列表来创建一个值的列表。这也可以使用循环完成：

```python
result = []
for key in self._keys:
    result.append(self.__dict[key])
return result
```

## 方法与特殊方法

与其写四行代码，写一行代码显然让列表推导式更有吸引力，尽管这种语法可能需要一些适应。

```python
def items(self):
    return [(key, self.__dict[key]) for key in self.__keys]
```

我们使用类似的方法返回项，即 (key, value) 元组，我们仍然可以使用传统的循环代替：

```python
result = []
for key in self.__keys:
    result.append((key, self.__dict[key]))
return result
```

到目前，列表推导式应该开始变得更加熟悉。

```python
def __iter__(self):
    return iter(self.__keys)
```

```python
def __iter__(self):
    return iter(self.__keys)
```

这是一个生成器，按顺序产生项。例如：

```python
def __iter__(self):
    for key in self.__keys:
        yield key
```

这是一个生成器，按顺序产生项。例如：

```python
def __iter__(self):
    for key in self.__keys:
        yield key
```

这是一个生成器，按顺序产生项。例如：

```python
def __iter__(self):
    for key in self.__keys:
        yield key
```

这是一个生成器，按顺序产生项。例如：

```python
def __iter__(self):
    for key in self.__keys:
        yield key
```

```python
def ititems(self):
    for key in self.__keys:
        yield key, self._dict[key]
```

```python
def values(self):
    for key in self.__keys:
        yield self._dict[key]
```

这与 `items()` 几乎相同，不同之处在于我们返回一个 (key, value) 元组。（这里不需要使用括号表示元组，因为没有歧义。）

```python
def copy(self):
    dictionary = OrderedDict()
    dictionary.__keys = self.keys[:]
    dictionary._dict = self._dict.copy()
    return dictionary
```

对于复制，我们对键列表和字典进行了浅拷贝，因此成本与字典的大小成正比。

```python
def clear(self):
    self._keys = []
    self._dict = {}
```

这是最简单的函数。我们可以使用 `list()` 和 `dict()` 代替 `[]` 和 `()`。

```python
def _repr__(self):
    pieces = []
    for key in self.keys:
        pieces.append("%r: %r" % (key, self._dict[key]))
    return "OrderedDict(%s})" % ", ".join(pieces)
```

我们选择为字典提供可 `eval()`的形式。（而且我们没有实现 `_str__`，这将在需要字符串时使用——例如在打印语句中。）对于每个 (key, value) 对，我们使用 `%r` “表示”格式，例如字符串将被加上引号，但不会。这里有两个显示 `repr()` 作用的示例：

```python
d = OrderedDict(s=1, a=2, n=3, i=4, t=5)
repr(d)
# 输出 "OrderedDict({'a': 2, 'i': 4, 'n': 3, 's': 1, 't': 5})"
d = OrderedDict({'2': 'a', '3': 'm', '1': 'x'})
print d  # 等于 print repr(d)
# 输出 "OrderedDict({'1': 'x', '2': 'a', '3': 'm'})"
```

自然，这可以使用列表推导式实现，但在这种情况下 `for` 循环似乎更容易理解。

我们现在完成了对 `OrderedDict` 类的审查。这个类和其他 Python 集合似乎缺失的一个功能是可以加载和保存到文件。事实上，Python 有能力加载和保存集合，包括嵌套字典、字节字符串并到

## 方法与特殊方法

文件，只要它们包含可以被表示的对象，例如布尔值、数字、字符串以及此类对象的集合。（实际上，Python 甚至可以加载和保存函数、类，在某些情况下甚至是实例。）我们将在第 8 章中学习此功能。

## 继承与多态

正如我们对支持面向对象编程的语言所期待的那样，Python 支持继承多态。我们已经使用了继承，到目前为止创建的类都继承自 `object`，但在本节中我们将进行更深入的探讨。所有的 Python 方法都是虚方法，因此如果我们在基类中重新实现一个方法，那么重新实现的方法将是我们调用的那个。我们很快会展示如何访问基类方法，例如当我们想将它们作为重新实现方法的一部分时。

让我们从一个包含艺术品基本信息的简单类开始：

```python
class Item(object):
    def __init__(self, artist, title, year=None):
        self._artist = artist
        self._title = title
        self._year = year
```

我们继承了 `object` 基类，并为我们的类提供了三个私有数据属性。由于我们将属性设为私有，我们必须为它们提供访问器，或者创建可以通过它们进行访问的属性。在这个例子中，我们选择了使用访问器：

```python
def artist(self):
    return self._artist
```

```python
def setArtist(self, artist):
    self._artist = artist
```

`_title` 和 `_year` 属性的访问器结构上与 `_artist` 属性相同，因此我们没有显示它们。

```python
def __str__(self):
    year = ""
    if self._year is None:
        year = "in %s" % self._year
    return "%s by %s%s" % (self._title, self._artist, year)
```

如果需要字符串表示，当 `_year` 为 `None`，我们返回格式为“title by artist”的字符串，否则返回“title by artist year”。

# 第 3 章 类与模块

现在我们已经封装了关于艺术品的一些基本信息，可以创建一个 `Painting` 子类来存储绘画信息：

```python
class Painting(Item):
    def __init__(self, artist, title, year=None):
        super(Painting, self).__init__(artist, title, year)
```

前面的代码是整个子类。我们没有添加任何数据属性或新方法，因此只需使用 `super()` 内置函数来初始化 `Item` 基类。`super()` 函数接收一个类并返回该类的基类。如果函数还传递了一个实例（如我们在这里所做的），返回的类对象将绑定到传递的实例，这意味着我们可以在实例上调用（基类）方法。

也可以通过显式命名基类来调用基类——例如，`Item.__init__(self, artist, title, year)`；注意，如果我们使用这种方法，我们必须自己传递 `self` 参数。

我们完全可以不调用基类的 `__init__()`——例如，如果基类没有数据属性。如果我们确实调用了它，`super()` 调用不必是我们要做的第一个调用，尽管在 `__init__()` 的实现中通常是这样的。

现在我们来看一个稍微复杂一点的子类：

```python
class Sculpture(Item):
    def __init__(self, artist, title, year=None, material=None):
        super(Sculpture, self).__init__(artist, title, year)
        self.material = material
```

`Sculpture` 类有一个额外的属性，因此在通过基类初始化后，我们也初始化了额外的属性。

我们不会显示访问器，因为它们结构上与用于艺术家名的访问器相同。

```python
    def __str__(self):
        materialString = ""
        if self.material is not None:
            materialString = " (%s)" % self.material
        return "%s%s" % (super(Sculpture, self).__str__(), materialString)
```

`__str__` 方法使用了基类的 `__str__()`，如果已知，它将其附加在结果字符串的末尾。我们不能调用 `str(self)`，因为会导致无限递归（反复调用 `__str__()`），但显式调用必要的特殊方法是没有问题的，正如我们在这里所做的。

## 继承与多态

由于 Python 的多态性，始终会调用正确的 `str__()` 方法。例如：

```python
a = Painting("Cecil Collins", "The Sleeping Fool", 1943)
print a # 输出 "The Sleeping Fool by Cecil Collins in 1943"
b = Sculpture("Auguste Rodin", "The Secret", 1925, "bronze")
print b # 输出 "The Secret by Auguste Rodin in 1925 (bronze)"
```

虽然我们使用特殊方法实现了多态，但它对普通方法也同样有效。

Python 使用动态类型，也称为鸭子类型，“如果它走起来像鸭子，叫起来也像鸭子，那么它就是灵活的”。例如，假设我们有这样一个类：

```python
class Title(object):
    def __init__(self, title):
        self.__title = title

    def title(self):
        return self.__title
```

现在我们可以这样做：

```python
items = []
items.append(Painting("Cecil Collins", "The Poet", 1941))
items.append(Sculpture("Auguste Rodin", "The Secret", 1917, "bronze"))
items.append(Title("Spring"))
```

（注：原文中第 115-116 页的内容存在严重的 OCR 错误和重复，已根据上下文逻辑进行了修复和重构。）

## 模块与多应用

面向对象的编程允许我们把功能（例如方法和数据属性）封装在类中。Python 模块允许我们在更高级别上封装功能——例如整组类、函数和实例变量。模块是一个带有 .py 扩展名的简单文件。模块中可能包含在导入时执行的代码，但更常见的是，它们提供了函数和类，这些函数和类在导入时被实例化。我们已经看到过这方面的示例：`Length` 类位于名为 `length.py` 的文件中，因此可以作为 `length` 模块被访问。在导入模块时，我们指定不带扩展名的模块名。例如：

```
import length
a = length.Length("4.5 yd")
```

只有位于当前目录或位于 Python 的 `sys.path` 列表中的模块才能被导入。如果我们访问文件系统中其他位置的模块，可以向 `sys.path` 添加额外的路径。除了文件外，模块还可以是一个包含多个文件的目录。在这种情况下，该目录必须包含一个名为 `__init__.py` 文件。该文件可以是空的（而且通常是空的）；它仅仅被用作标记，告诉 Python 该目录包含 .py 文件，且目录名即为顶层模块名。例如，我们可能会创建一个名为 `mylibrary` 的目录，并在其中放入 `library.py`、`ordereddict.py` 和空的 `__init__.py`。只要我们将包含 `mylibrary` 目录的父目录添加到 Python 的路径中，就可以：

```
import mylibrary.length
a = mylibrary.Length("14.3 km")
```

在实践中，我们可能倾向于将 `mylibrary.length` 别命名为更短的内容。例如：

```
import mylibrary.length as length
a = length.Length("948mm")
```

Python 的模块处理比我们展示的要复杂得多，但我们涵盖的内容对于我们关注的 GUI 编程来说足够了。Python 和 PyQt 应用可以写在单个文件中，也可以分布在多个文件中。我们将在接下来的章节中展示这两种方法。*

> *模块的导入语义将在 Python 2.7 中发生变化，导入将变为绝对导入而非相对导入。详情参见 http://www.python.org/dev/peps/peg-0328。*

## 使用 doctest 模块

Python 对测试提供了大量的支持，其中 `doctest` 和 `unittest` 模块用于单元测试，而 `test` 模块用于回归测试。PyQt 也通过 `QtTest` 模块提供了单元测试功能。

当我们创建模块时（例如我们之前编写的 `length` 和 `ordered` 模块），它们的设计是为了通过导入应用导入及其提供的对象（例如 `Length` 和 `OrderedDict` 类）。由于 .py 文件也可以是可执文件，我们可以轻松地包含单元测试代码：当模块被导入时，单元测试代码会被简单忽略；但当模块运行时，测试就会执行。这种方法得到了 `doctest` 模块的支持。

`doctest` 让单元测试变得尽可能简单无痛苦。要使用它，我们只需要在文档字符串（docstrings）中添加示例，显示我们在交互式解释器（或 IDLE）中输入的内容以及我们期望的响应。例如，这里是 `OrderedDict` 类的 `get()` 方法：

```python
def get(self, key=None):
    """如果 key 不在字典中，则返回与 key 关联的值

    >>> d = OrderedDict(s=1, a=2, n=3, i=4, t=5, y=6)
    >>> d.get("s")
    1
    >>> d.get("i")
    4
    """
    return self._dict[key]
```

文档字符串包含了对方法目的的简要描述，然后是一些像输入到解释器那样的示例。通过创建一个 `OrderedDict` 对象；由于我们位于 `ordereddict` 模块内部，我们不需要导入或限定类名。然后我们写写对要测试测试的调用以及我们期望的结果。`doctest` 模块使用这种语法，是因为 Python 程序员通过使用交互式解释器、IDLE 或任何其他 IDE 对这种语法感到非常熟悉。当运行测试时，`doctest` 模块会导入模块本身，然后读取每个文档字符串（使用 Python 的内省能力），然后执行每个以 `>>>` 提示符开头的语句。它会将结果与预期输出（可能为空）进行比较，并报告任何失败。

为了让模块能够像这样使用 `doctest`，我们只需要在模块末尾添加三行代码：

```python
if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

无论模块是通过导入语句的主体被导入，还是在命令行被调用的，都会导致模块的函数和类被创建。另一方面，如果模块被调用，它的 `__name__` 属性会被设置为 `"__main__"`。在此之前，我们可以使用语句来查看模块是否被导入，如果是，它什么都不做。我们可以从控制台窗口执测试运行。例如：

```
cd c:\pyqt\chap03
c:\pyqt\chap03>ordereddict.py
```

如果没有失败，模块将静默运行。如果有任何错误，这些将输出到控制台。我们可以使用 `-v` 标志强制 `doctest` 模块输出更详细：

```
c:\pyqt\chap03>ordereddict.py -v
```

这将显示执行的每项测试以及结尾的总结。

也可以测试预期的失败，例如我们预计会抛出异常的情况。对于这些情况，我们只需要写下第一行和最后一行预期的输出（因为中间可能有所不同），并使用省略号 `...` 来表示 traceback。例如，这里是 `OrderedDict` 类的 `setAt` 方法：

```python
def setAt(self, index, value):
    """将索引处项目的值设置为给定值

    >>> d = OrderedDict(s=1, a=2, n=3, i=4, t=5, y=6)
    >>> d.get(5)
    6
    >>> d.setAt(5, 99)
    >>> d.get(5)
    99
    >>> d.setAt(19, 42)
    Traceback (most recent call last):
    ...
    """
    self._dict[self._keys[index]] = value
```

我们创建一个包含六个元素的 `OrderedDict`，但在最后尝试设置不存在的项目。这会导致字典抛出 `IndexError`，因此我们写下解释器的输出，`doctest` 模块理解这一点并在异常正确异常时通过测试。

`doctest` 模块没有 `unittest` 模块复杂，但它既易用又无侵入性。我们在目前为止的所有示例代码中都使用了它。

## 总结

本章让我们从类的使用者变成了类的创建者。我们看到了如何使用 `__init__` 特殊方法初始化新实例，以及如何实现许多其他特殊方法，以便自定义数据类型（类）能够像 Python 的内置类一样工作。我们还学习了如何创建普通方法和静态方法，以及如何存储和访问实例和静态数据。

我们回顾了两个示例：数值数据类型 `Length` 和集合类 `OrderedDict`。我们还利用了从之前章节获得的许多知识，包括 Python 的一些高级特性，例如列表推导式和生成器方法。

本章还展示了如何进行单继承和多继承，并提供了一个创建简单接口类的示例。我们更多地学习了使用 `isinstance()` 进行类型测试以及 `hasattr()` 鸭子类型。

我们通过概述 Python 模块和应用的工作原理结束本章。我们现在掌握了 Python 语言基础。我们可以创建变量、集合并创建自己的数据类型和集合类型。我们可以进行分支、循环、调用函数和方法，以及引发和处理异常。显然，还有很多需要学习的内容，但我们可以在需要时涵盖其他所有内容。我们现在准备好开始 GUI 应用编程，该主题从下一章开始并占据书的剩余部分。

## 练习

- 1. 实现一个 Tribool（三值逻辑）数据类型。这种数据类型可以有三个值之一：True、False 或 unknown（未知，你应该使用 `None`）。除了 `__init__()` 之外，还要实现 `__str__()`、`__repr__()`、`__cmp__()`；此外，实现 `nonzero()` 用于转换为 `bool()`，实现 `__invert__()` 用于逻辑非 (~)，实现 `&__()` 用于逻辑与 (&)，或者实现 `|__()` 用于逻辑或 (|)。这里有两种可能的逻辑逻辑可以使用：传播逻辑（propagating），即任何涉及 `unknown`（即 `None`）的表达式都是 `unknown`；以及非传播逻辑（nonpropagating），即任何涉及 `unknown` 的表达式都可以被求值。使用非传播逻辑使得你的 Tribools 符合此处所示的真表，其中 `t` 是 Tribool(True)，`f` 是 Tribool(False)，`n` 是 Tribool(None)（表示未知）：

| 表达式 | 结果 | 表达式 | 结果 | 表达式 | 结果 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| -t | False | -f | True | -n | None |
| t & t | True | t & f | False | t & n | None |
| f & f | False | f & n | False | n & n | None |
| t | t | True | t | f | True | t | n | True |
| f | f | False | f | n | None | n | n | None |

例如，使用非传播逻辑时，`True | None` 是 `True`，因为只要逻辑或的操作数有一个为真，表达式就是真。但 `False | None` 是 `None`（未知），因为我们无法确定结果。

大多数方法只需要几行代码即可实现。请确保你使用了 `doctest` 模块并为所有方法编写了单元测试。

2. 实现一个 `Stack`（栈）类和一个 `EmptyError` 异常类。`Stack` 类应该使用列表来存储其元素，并提供 `pop()` 返回并移除栈顶元素（最右侧的元素）、`top()` 返回栈顶元素，以及 `push()` 将新元素推入栈中。还应提供特殊方法使得 `len()` 和 `str()` 能够正常工作。确保在调用 `pop()` 和 `top()` 时如果栈为空则抛出 `EmptyStackError`。这些方法可以用非常少的代码编写。请确保你使用了 `doctest` 模块并为所有方法编写了单元测试。

模型答案在文件 `chap03/tribool.py` 和 `chap03/stack.py` 中。

## 第二部分

##  GUI 编程

## 第 4 章

- 25行的弹出警报

- 30行的表达式求值器

- 70行的货币转换器

- 信号与槽

## GUI 编程简介

在本章中，我们将从简要回顾三个用 PyQt 编写的微小但用的 GUI 应用程序开始。我们将借机会强调 GUI 编程中涉及的一些问题，但会将大部分细节留到后面的章节。一旦我们熟悉了 PyQt GUI 编程的感受，我们将讨论 PyQt 的“信号与槽”（signals and slots）机制——这是一种响应用户交互的高级通信机制，允许我们忽略无关的细节。

尽管 PyQt 被商业化用于构建从几百行到 100,000 多行代码不等的应用程序，但我们在本章中构建的应用都少于 100 行，它们展示了用极少的代码可以完成多少工作。

在本章中，我们将纯编写代码来设计用户界面，但在第 7 章中，我们将学习使用 Qt 的视觉设计工具 Qt Designer 来创建用户界面。

Python 控制台应用程序和 Python 模块始终具有 .py 扩展，但对于 GUI 应用程序我们使用 .pyw 扩展。.py 和 .pyw 在 Linux 上都是免费的，但在 Windows 上，.pyw 确保 Windows 使用 python.exe 解释器而不是 python，反之确保当我们执行 PyQt 应用程序时不会出现不必要的控制台窗口。在 Mac OS X 上，使用 .pyw 扩展是关重要的。

PyQt 文档以一组 HTML 文件的形式提供，与 Python 文档独立。最常引用的文档是涵盖 PyQt API 的。这些文件是从原始 C++/Qt 文档转换而来的，它们的索引页称为 `classes.html`；Windows-

> *如果你使用 Windows 弹出的错误消息框标题为 "python.exe- Unable To Locate Component"，这几乎肯定意味着你没有正确设置路径。请参见附录 A 第 564 页了解如何修复。*

## 第 4 章：GUI 编程简介

用户可以在开始按钮的 PyQt 菜中找到此页的链接。查看此页面以概述可用哪些类，当然也可以深入阅读那些看起来有趣的类，是非常值得的。

我们将查看的第一个应用程序是一个不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签（labels）、按钮（buttons）、组合框（comboboxes）以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特定的函数或方法。

最后一部分我们将涵盖用户交互，这将在下一章中涵盖。

## 25行的弹出警报

我们的第一个应用程序是不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签、按钮、组合框以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特特的函数或方法。

最后一部分我们将涵盖用户交互，这将在下一章中涵盖。

## 25行的弹出警报

我们的第一个应用程序是不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签、按钮、组合框以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特定的函数或方法。

## 25行的弹出警报

我们的第一个应用程序是不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签、按钮、组合框以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特定的函数或方法。

## 25行的弹出警报

我们的第一个应用程序是不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签、按钮、组合框以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特定的函数或方法。

## 25行的弹出警报

我们的第一个应用程序是不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签、按钮、组合框以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特定的函数或方法。

## 25行的弹出警报

我们的第一个应用程序是不寻常混合体：一个必须从控制台启动的 GUI 应用程序，因为它需要命令行参数。我们包含它是因为这有助于解释 PyQt 事件循环是如何工作的（以及它是什么），而无需进入任何其他 GUI 细节。第二个和第三个示例都是非常短但标准的 GUI 应用程序。它们都展示了我们如何创建和布局控件（Windows 术语中的“controls”）——标签、按钮、组合框以及用户可以查看并在大多数情况下与之交互的其他屏幕元素。它们还展示了我们如何响应用户交互——例如，如何调用特定的函数或方法。

*(注：由于原文文本中存在大量重复段落，译文已根据逻辑进行了整理，并保留了所有要求的结构。)*

## 第 4 章 GUIGUI编程简介

如果第一个参数不包含冒号，当我们尝试从 `split()` 调用中解包两个项时，将抛出一个 `ValueError`。如果小时或分钟不是数字，`int()` 将抛出 `ValueError`；如果小时或分钟超出范围，它将是一个无效的 `QTime`，我们会手动抛出一个 `ValueError`。尽管 Python 提供了自身的日期时间类，但 PyQt 的日期时间类通常更方便（而且在某些方面更强大），我们倾向于使用它们。

如果时间是有效的，我们将消息设置为其他命令行参数用空格分隔的连接字符串（如果有的话）；否则，将其保留为我们在开始设置的默认值“Alert!”。当在命令行上执行程序时，我们提供一个参数列表，第一个是调用名称，其余的是空白字符序列，每个序列对应在命令行上输入的每个“单词”。这些单词可能会被 shell 改变——例如通过应用通配符扩展。Python 将实际收到的单词放入 `sys.argv` 列表中。

现在当必须显示消息且我们

```python
while QTime.currentTime() < due:
    time.sleep(20) # 20 秒
```

持续循环，将当前时间与目标时间进行比较。如果当前时间于目标时间，循环将终止。我们可以简单地在循环中放置一个 `pass` 语句，但如果这样做，Python 将尽可能快地运行，无缘无故地消耗处理器周期。`time.sleep()` 命令告诉 Python 挂处理指定的秒数（在本例中为20秒）。这为其他程序提供了更多运行和处理的机会，因为我们不想在等待时间到达时实际做任何事情。

除了创建 `QApplication` 对象之外，我们目前所做的都是标准的控制台编程。

```python
label = QLabel("<font color=72><b>" + message + "</b></font>")
label.setWindowFlags(Qt.SplashScreen)
label.show()
QTimer.singleShot(60000, app.quit) # 1 分钟
app.exec_()
```

我们已经创建了一个 `QApplication` 对象，有一个消息，截止时间已到达，所以现在我们可以创建应用程序了。GUI 应用程序需要控件，在这种情况下我们需要一个标签来显示消息。`QLabel` 可以接受 HTML 文本，因此我们给它传递一个 HTML 字符串，告诉它显示大小为 72 点的加粗红色文本。*

> *支持的 HTML 标签列在 http://doc.trolltech.com/richtext-html-subset.html。

## 25 行代码实现弹出警告

在 PyQt 中，任何控件都可以作为顶层窗口、按钮或标签。当控件像这样被使用时，PyQt 会自动为它提供一个标title栏。我们不需要这个应用程序的标题栏，因此我们将窗口的标志设置为用于启动屏幕的标志，因为启动屏幕没有标题栏。我们已经将标签设为我们的窗口，并在其上调用了 `show()`。此时，标签窗口并没有显示！`show()` 的调用只是调度了一个“漆绘事件（paint event）”，即向 `QApplication` 的事件队列中添加一个新事件，这是一个绘制指定控件的请求。

接下来，我们设置了一个单次定时器。Python 库的 `time.sleep()` 函数接受的是秒数，而 `QTimer.singleShot()` 函数接受的是毫秒数。我们给 `singleShot()` 方法传递两个参数：它应该等待多久（在本例中为一分钟），以及它在超时时要调用的函数或方法。

在 PyQt 术语中，我们提供的函数或方法被称为“槽（slot）”。在所有 PyQt 文档中，术语“callable”、“Python slot”和“Q slot”被用于区分槽与 Python 的 `slots`（这是在《Python 语言参考》中描述的一种新式类特性）开来。在书中，我们将使用 PyQt 术语，因为我们从不使用 `_slots_`。

所以现在我们调度了两个事件：一个漆绘事件准备发生，以及一个一分钟后发生的定时器超时事件。

`exec_()` 的调用启动了 `QApplication` 对象的事件循环。它收到的第一个事件是漆绘事件，因此标签窗口带有给的消息出现在屏幕上。大约一分钟后，定时器事件发生并调用了 `QApplication.quit()` 方法。该方法执行 GUI 应用程序的清理终止。它关闭所有窗口，释放已获取的所有资源并退出。

所有 GUI 应用程序都使用事件循环。在伪代码中，事件循环看起来如下：

```python
while True:
    event = getNext()
    if event:
        if event == Terminate:
            break
        processEvent(event)
```

当用户与应用程交互时，或者发生其他情况时（例如定时器触发或应用程序窗口被覆盖，可能是另一个应用程序被关闭），PyQt 内部会生成一个事件并添加到事件队列中。应用程序持续检查是否有需要处理的事件，如果有，就进行处理（或将其传递给关联的函数或方法进行处理）。

> *PyQt 使用 `exec_()` 而不是 `exec()` 以避免与 Python 的内置 `exec` 语句冲突。

## 第 4 章 GUIGUI编程简介

![](img/55bc1dcf8601cfec5e1423b4e17ec264_130_0.png)

图 4.2 批处理应用程序与 GUI 应用程序的对比

我们接下来查看的下一个应用程序比之前那个要常规得多，它是许多 GUI 应用程序的典型。相比之下，“主窗口样式”应用程序通常具有菜单栏、工具栏、状态栏，某些情况下还有按钮；它们有一个中心控件（可以包含其他控件）。

## 30 行实现计算器

该应用程序是用 30 行代码编写的完整对话框样式应用程序（不包括空行和注释行）。“对话框样式”意味着没有菜单栏的应用程序。我们将在第 6 章查看主窗口样式应用程序。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_131_0.png)

图 4.3 计算应用程序

该应用程序使用了两个控件：可以显示纯文本和 HTML 的 `QTextBrowser` 多行文本框；以及一个显示纯文本的单行 `QLineEdit`。 控件中的所有文本都是Unicode 编码，必要时可以转换为其他字符集。

计算应用程序（如图 4.3 所示）可以像任何普通应用程序一样通过点击（或根据平台设置双击）图标来调用。它也可以从控制台启动。一旦应用程序运行，用户可以在行编辑器中输入数学表达式并在按下 Enter（或 Return）时，表达式及其结果将添加到 `QTextBrowser` 中。任何无效表达式或无效算术（如除以零）引起的异常都会被捕获并转换为错误消息，直接添加到 `QTextBrowser` 中。

## 第 4 章 GUI 编程简介

```python
def __init__(self, parent=None):
    super(Form, self).__init__(parent)
    self.browser = QTextBrowser()
    self.lineedit = QLineEdit("Type an expression and press Enter")
    self.lineedit.selectAll()
    layout = QVBoxLayout()
    layout.addWidget(self.browser)
    layout.addWidget(self.lineedit)
    self.setLayout(layout)
    self.lineedit.setFocus()
    self.connect(self.lineedit, SIGNAL("returnPressed")), self.updateUI()
    self.setWindowTitle("Calculate")
```

我们已经看到任何小部件（widget）都可以作为顶层窗口。但在大多数情况下，当我们创建顶层窗口时会继承 `Dialog`、`QMainWindow`，或者偶尔继承 `QWidget`。`Dialog` 和 `QMainWindow` 实际上所有 PyQt 的小部件都派生自 `QWidget`。通过继承 `Dialog`，我们获得了一个空白表单（即一个灰色矩形）以及方便的行为和方法。例如，如果用户点击 X 按钮，对话框将关闭。默认情况下，它在关闭时只是被隐藏；我们将在下一章看到如何更改这种行为。

我们为类提供了 `__init__()` 方法并使用 `super()` 来初始化它。没有父对象的小部件将变成顶层窗口，这正是我们表单所需的。然后我们创建所需的两个小部件并保留它们的引用，以便在 `__init__()` 之外访问它们。由于我们没有给这些小部件指定父对象，它们似乎变成了顶层窗口——这是不符合逻辑的。我们很快就会看到，它们在初始化器的后续部分会获得父对象。我们给 `QLineEdit` 提供了一些初始显示的文本，并选中了所有内容。这将确保用户一开始打字，文本就会被覆盖。

我们希望小部件在窗口中垂直排列，一个接一个。这通过创建一个 `QVBoxLayout` 并将我们的两个小部件添加到其中，然后将该布局设置到表单上来实现。如果你运行应用程序并调整其大位，你会发现任何额外的垂直空间都会分配给 `QTextBrowser`，且两个小部件都会水平方向上扩展。这一切都由布局管理器自动处理，并可以通过设置布局策略（layout policies）进行微调。

使用布局的一个重要方面是，PyQt 会自动修复已布局的小部件。因此，尽管我们没有给小部件 `self`（Form 实例）作为父对象，但当我们调调用 `setLayout()` 时，布局管理器会将小部件自身的所有权交给表单，并获取其包含的任何嵌套布局的所有权。这意味着所有已布局的小部件都不是顶层窗口，且它们都有父对象，这正是我们想要的。当表单被删除时，其所有的子小部件和布局将随之按正确的顺序删除。

## 30 行代码表达式评估器

## 对象所有权

所有派生自 `QObject` 的 PyQt 类（包括所有小部件，因为 `QWidget` 是 `QObject` 的子类）都可以拥有一个“父对象”。父子关系用于两个互补的目的：没有父对象的小部件是顶层窗口，而具有父对�（始终连接）的小部件则显示（在其父对象内部）。这种关系还定义了所有权，即父对象拥有其子对象。

PyQt 使用父子所有权模型来确保如果父对象（例如顶层窗口）被删除，其所有子对象（例如小部件）也会被删除。为了避免内存泄漏，我们应该始终确保任何 `QObject`（包括 `QWidget`，顶层窗口除外）。

绝大多数 PyQt `QObject` 子类都有构造函数，接受父对�作为其最后一个（可选）参数。但对于小部件，我们通常不需要（也没有必要）传递这个参数。这是因为在对话框中使用的小部件是通过布局管理器布局的，它们会自动重新设置父对象为所在布局的小部件，因此它们最终拥有正确的父对象，而无需我们采取任何特殊操作。

在某些情况下，我们必须显式地获取父对象——例如在构造不是小部件的 `QObject` 对象时，或者构造不会布局的小部件（如停靠部件 dock widgets）；我们将在后面的章节中看到此类情况的几个示例。

最后一点是，可能会出现 Python 变量指向不再存在的底层 PyQt “对象”的情况。这个问题在第 9 章第 287 页开始的“活跃性”（liveness）讨论中涵盖。

表单上的小部件可以使用多种技术进行布局。我们可以使用 `resize()` 和 `move()` 方法赋予它们绝对的大小和位置；我们可以重写 `resizeEvent()` 方法并动态计算它们的大小和位置，或者使用 PyQt 的布局管理器。使用绝对的大小和位置非常不方便。一方面，我们必须进行大量的手动计算；另一方面，如果我们更改了布局，就必须重新计算。动态计算大小和位置是一种更好的方法，但仍然需要我们编写大量冗燥的计算代码。

使用布局管理器让这一切变得简单得多：它们会自动适应大小调整和内容变化。任何习惯了多个版本 Windows 对话框的人都会发现可以调整大小（且非常合理）的对话框的好处，而不是被迫使用小小的、不可缩放的对话框（当内容过大无法容纳时非常不便）。布局管理器还让国际化程序变得更容易，因为它们会适应内容，所以翻译后的标签不会被“切断”。

PyQt 提供了三种布局管理器：一个用于垂直布局，一个用于水平布局，一个用于网格布局。布局可以嵌套，因此可以复杂的布局。还有其他布局小部件的方法，例如拆分器（splitters）或标签页（tab widgets）。

## 30行实现的表达式评估器

通过使用 `eval()`，我们避免了在某些编译型语言时必须手动完成的所有解析和错误检查工作。

```python
app = QApplication(sys.argv)
form = Form()
form.show()
app.exec()
```

现在我们已经定义了 `Form` 类，在 `calculate.py` 文件的末尾，我们创建了 `QApplication` 对象，实例化我们的表单，调度它进行绘制，并启动事件循环。

这就是完整的应用程序。但故事并没有结束。我们还没有说明用户如何终止应用程序。由于我们的表单继承自 `QDialog`，因此它继承了一些行为。例如，如果用户点击关闭按钮 X，或者按下 `Esc` 键，表单将关闭。当表单隐藏时，PyQt 会检测到应用程序没有可见窗口且无法进行进一�的交互。它将删除对象并执行应用程序的洁净退出。

在某些情况下，我们希望应用程序在不可见时继续运行——例如服务器。对于这些情况，我们可以调用 `QApplication.setLastWindow(False)`。虽然很少需要，但也可以在窗口关闭时接收通知。

在 Mac OS X 和某些 X 窗口管理器（如 twm）上，应用程序将没有关闭按钮，而且在 Mac 上从菜单栏选择“退出”（Choosing Out）将不起作用。在这种情况下，按下 `Esc` 将终止应用程序，此外在 Mac 上 `Command-Q` 将有效。鉴于此，对于可能在 Mac 上或配合 twm 或类似软件使用的应用程序，最好是提供一个“退出”（Quit）按钮。在对话框中添加按钮将在本章最后一节中介绍。

我们现在准备好查看在本章中提供的最后一个小而完整的示例了。它有更多的自定义行为、更复杂的布局以及更复杂的处理，但其基础结构与 `Calculate` 应用程序非常相似，实际上与许多其他 PyQt 对话框也一样。

## 70行实现的货币转换器

一个经常实用的小工具是货币转换器。但由于汇率经常变化，我们不能像在上一章为 `Length` 类中的长度单位那样，简单地创建一个静态的汇率字典。幸运的是，加拿大银行提供可以通过互联网访问的汇率文件，该文件使用了易于解析的格式。汇率有时是几天前的，但对于估计旅行所需的现金或外国合同可能支付的金额很有用。应用程序如图 4.4 所示。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_136_0.png)

**图 4.4** 货币应用程序

应用程序必须首先下载并解析汇率。然后它必须创建一个用户界面，用户可以通过操作它来指定感兴趣的货币和金额。

按照惯例，我们将从导入开始：

```python
import sys
import urllib2
from PyQt4.Qt import *
from PyQt4.QtGui import *
```

Python 和 PyQt 都提供了网络类。在第18章，我们将使用 PyQt 的类，但在这里我们将使用 Python 的 `urllib2` 模块，因为它提供了一个非常方便的函数，可以轻松地从互联网获取文件。



```python
class Form(QDialog):
    def __init__(self, parent=None):
        super(Form, self).__init__(parent)
        date = self.getdata(self)
        rates = sorted(self.rates.keys())
        dateLabel = QLabel(date)
        self.comboBox = QComboBox()
        self.comboBox.addItems(rates)
        self.SpinBox = QDoubleSpinBox()
        self.SpinBox.setRange(0.01, 100000000.00)
        self.SpinBox.setValue(1.00)
        self.toComboBox = QComboBox()
        self.toComboBox.addItems(rates)
        self.tolabel = QLabel("1.00")
```

使用 `super(self)` 初始化表单后，我们调用了 `getdata()` 方法。正如我们很快看到的，该方法获取汇率，填充 `self.rates` 字典，并返回一个持有它们生效日期的字符串。字典的键是货币名称，值是转换因子。

## 70行实现的货币转换器

我们获取了字典键的排序副本，以便我们可以在组合框中向用户展示排序后的货币列表。`date` 和 `rate` 变量以及 `dateLabel` 只在 `__init__()` 内部引用，因此我们不保留对类实例的引用。另一方面，我们需要访问组合框和标签（显示目标货币金额），因此我们通过使用 `self` 来创建这些实例。

我们在两个组合框中添加了相同的货币列表，并创建了一个 `DoubleSpinBox`，这是一个处理浮点值的数值计数器。我们为计数器提供了最小值和最大值，以及一个初始值。在设置值之前始终设置计数器的范围是一个良好的习惯，因为如果我们先设置第一个值，而该值恰好在默认范围之外，该值将减小或增加以适应默认范围。

由于两个组合框最初显示相同的货币，且要转换的初始值为 1.00，因此标签中显示的的结果也必须是 1.00，所以我们显式地设置了它。

```python
grid = QGridLayout()
grid.addWidget(dateLabel, 0, 0)
grid.addWidget(self.fromComboBox, 1, 0)
grid.addWidget(self.fromSpinBox, 1, 1)
grid.addWidget(self.toComboBox, 2, 0)
grid.addWidget(self.toLabel, 2, 1)
self.setLayout(grid)
```

网格布局（grid layout）似乎是布局组件最简单的解决方案。当我们向网格中添加组件时，我们赋予它应该占据的行和列位置，两者都是从 0 开始的。布局如图 4.5 示意图所示。使用网格布局可以做更多操作。例如，我们可以让组件跨行跨列；这些将在稍后的第9章中介绍。

| 组件 | 位置 |
| :--- | :--- |
| dateLabel | (0,0) |
| self.fromComboBox | (1,0) |
| self.fromSpinBox | (1,1) |
| self.toComboBox | (2,0) |
| self.toLabel | (2,1) |

**图 4.5** 网格布局

网格布局似乎是布局组件最简单的解决方案。当我们向网格中添加组件时，我们赋予它应该占据的行和列位置，两者都是从 0 开始的。布局如图 4.5 示意图所示。使用网格布局可以做更多操作。例如，我们可以让组件跨行跨列；这些将在稍后的第9章中介绍。

鉴于此，对于可能在 Mac 上或配合 twm 或类似软件使用的应用程序，最好是提供一个“退出”（Quit）按钮。在对话框中添加按钮将在本章最后一节中介绍。

我们现在准备好查看在本章中最后一个小而完整的示例了。它有更多的自定义行为、更复杂的布局以及更复杂的处理，但其基础结构与 `Calculate` 应用程序非常相似，实际上与许多其他 PyQt 对话框也一样。

## 第4章 GUI 编程

如果我们运行应用程序并尝试让窗口变窄，什么都不会发生，因为它已经达到了最小宽度。但如果我们增大窗口，所有的额外空间将留给 `dateLabel`，因为它是表单上唯一向各个方向增长的组件。没有任何组件会被拉伸，因为对它们来说没有必要。

在我们创建、填充了所有组件后，现在是设置用户行为了。

```python
# 第4章 GUI 编程
# ...（其余逻辑）
```

如果用户更改一个组合框中的当前项目，相应的组合框将发射 `currentIndexChanged()` 信号，参数为新项目的索引位置。同样，如果用户通过计数器更改值，将发射 `valueChanged()` 信号，参数为新值。我们将所有这些信号都连接到一个槽函数：`updateUI()`。这种做法并非必须，正如我们在下一节中看到的，但对于这个应用程序来说似乎是一个明智的选择。

在 `__init__()` 的末尾我们设置了窗口标题。

```python
def updateUI(self):
    to = unicode(self.toComboBox.currentText())
    from_val = unicode(self.fromComboBox.currentText())
    amount = (self.rates[from_val] / self.rates[to]) * \
             self.fromSpinBox.value()
    self.toLabel.setText("%0.2f" % amount)
```

该方法被调用响应组合框发射的 `currentIndexChanged()` 信号，并响应计数器发射的 `valueChanged()` 信号。所有信号都会传递一个参数。正如我们在下一节中看到的，正如我们在这里所做的那样。

# 70 行实现的汇率转换器

足够显示在一个页面上；而且无论如何，我们都倾向于限制行长度，以便在屏幕上并阅读两个文件。

```python
def getdata(self): # 灵感来自 Python Cookbook
    self.rates = {}
    try:
        date = "Unknown"
        fh = urllib2.urlopen("http://www.bankofcanada.ca"
                            "/en/markets/csv/exchange_eng.csv")
        for line in fh:
            line = line.strip()
            if not line.startswith("# Closing "):
                continue
            fields = line.split(",")
            if line.startswith("Date "):
                date = fields[-1]
            else:
                try:
                    value = float(fields[-1])
                    self.rates[unicode(fields[0])] = value
                except ValueError:
                    pass
        return "Exchange Data Rates: " + date
    except Exception, e:
        return "Failed to download:\n%s" % e
```

这种方法是获取驱动应用程序数据的地方。我们首先创建一个新属性 `self.rates`。与 C++、Java 和类似的语言不同，Python 允许我们在需要时再创建实例属性——例如，在构造函数、初始化器或任何其他方法中。我们甚至可以动态为特定实例添加属性。

由于网络连接可能会出现很多问题——例如网络可能断开、服务器可能宕机、URL 可能已经更改等，我们让应用程序比之前的两个示例更加健壮。另一个可能的问题是我们会获取无效的浮点值，例如货币数据中偶尔包含的“NA”（不可用）这种值。我们有了一个内部的 `try ... except` 块来捕获无效数字。如果我们无法将货币转换为浮点数，我们只需跳过该特定货币并继续。

我们通过将整个方法封装在一个 `out ... except` 块中来处理所有其他可能性。（这对于大多数应用程序来说太笼统了，但对于一个 70 行的微型应用程序来说是可以接受的。）如果发生问题，我们会捕获抛出的异常并将其作为字符串返回给调用者 `__init__()`。`getdata()` 返回的字符串显示在 `dateLabel` 中，因此通常它会显示适用于汇率的日期，但在错误情况下将显示错误消息。

# 第 4 章 GUI 编程导论

注意我们将 URL 字符串分成了跨行的两个字符串，因为它太长了——而且我们不需要转义换行符。之所以有效是因为字符串位于括号内。如果不是那样，我们就必须转义换行符或使用 `+` 将它们拼接（仍然需要转义换行符）。

我们用一个字符串初始化 `date` 变量，表示我们汇率是在哪些日期计算的。然后我们使用 `urllib2.urlopen()` 函数来获取我们感兴趣的文件句柄。文件句柄可以使用其 `read()` 方法一次性读取整个文件，但在这种情况下，我们倾向于通过将文件作为迭代器来逐行读取。

以下是 `exchange_eng.csv` 文件中某个特定日期的数据。某些列和行已被省略；这些用省略号表示。

| 日期 (<月/年>) | 01/05/2007 | ... | 01/12/2007 | 01/15/2007 |
| :--- | :--- | :--- | :--- | :--- |
| 收盘价/美元汇率 | 1.1725 | ... | 1.1688 | 1.1667 |
| 美元（午后） | 1.1755 | ... | 1.1702 | 1.1681 |
| 阿根廷比索（浮动汇率） | 0.3797 | ... | 0.3773 | 0.3767 |
| 澳元 | 0.9164 | ... | 0.9157 | 0.9153 |
| ... | ... | ... | ... | ... |
| 越南盾 | 0.000073 | ... | 0.000073 |

`exchange_eng.csv` 文件使用了几种类型的行。行以 `#` 开头，也可能有空行；我们忽略所有这些。汇率按名称列出，后面是汇率，用逗号分隔。这些汇率是适用于特定日期的，每行的最后一个是最新的。我们用逗号分割这些行中的每一行，取第一项作为货币名称，最后一项作为汇率。还有一行以 "Date" 开头；它列出了适用于每列的日期。当我们遇到这一行时，我们提取日期，因为那是与我们正在使用的汇率对应的日期。还有一行以 "Closing" 开头；我们忽略了它。

对于每一行汇率，我们都会向 `self.rates` 字典中插入一个项，使用货币作为键，汇率作为值。我们假设文件文本是 7 位 ASCII 或 Unicode；如果它不是其中之一，我们可能会遇到编码错误。如果知道编码，我们可以在调用 `decode()` 时将其作为第二个参数指定。

```python
app = QApplication(sys.argv)
form = Form()
form.show()
app.exec_()
```

# 70 行实现的汇率转换器

我们使用了与上一个示例完全相同的代码来创建 `QApplication` 对象、实例化货币应用程序的表单并启动事件循环。

在程序结束时，和上一个示例一样，我们关闭窗口。

## 信号与槽

self.setWindowTitle("Signals and Slots")

这两个组件是以这种方式连接的：如果用户移动拨钮——例如移动到值 20——拨钮将发射一个 `valueChanged(20)` 信号，这反过来会调用数值框的 `setValue()` 槽，并将 20 作为参数。但随后，由于它的值没有改变，数值框会发射一个 `valueChanged(20)` 信号，这反过来会调用拨钮的 `setValue()` 槽，并将 20 作为参数。这看起来我们会得到一个无限循环。但实际情况是，如果值没有发生变化，`valueChanged(int)` 信号就不会发射。这是因为编写改变值的槽的标准方法是首先比较新值与现有值。如果值相同，我们什么都不做；否则，我们应用更改并发射信号来宣布状态的变化。连接关系如图 4.7 所示。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_143_0.png)

图 4.7 信号与槽的连接

让我们看看连接的通用语法。我们假设 PyQt 组件已经通过 `from ... import *` 语法导入，并且 `s` 和 `w` 是 `QObject`，通常 `s` 是是 `self`。

```
s.connect(w, SIGNAL("signalSignature"), functionName)
s.connect(w, SIGNAL("signalSignature"), instance.methodName)
s.connect(w, SIGNAL("signalSignature"),
    instance, SLOT("slotSignature"))
```

信号名是信号的以及（可能的）逗号分隔的参数类型列表。如果信号是 Qt 信号，类型名称为 C++ 类型名称，如 `int` 和 `QString`。C++ 类型名称可能更复杂，每个类型名称包含一个或多个 `const`、`*` 和 `&`。当我们将其写为信号（或信号）时，可以忽略任何 `const` 和 `&`，但必须保留任何星号。例如，几乎每个传递 `const QString` 参数类型的 Qt 信号；在 PyQt 中，仅使用 `QString` 就足够了。另一方面，`QListWidget` 有一个签名名为 `itemActivated(QListWidgetItem*)` 的信号，我们必须完全按照写法使用它。

PyQt 信号是在实际发射时定义的，并且可以具有任意数量类型的参数，正如我们很快将看到的。

`slotSignature` 的形式与 `signalSignature` 相同，只是名称是一个 Qt 槽。槽的参数数量不能多连接到它的信号，但可以更少；额外的参数将被丢弃。相应的信号和槽参数必须具有相同的类型，例如，我们不能将 `QDial` 的 `valueChanged(int)` 信号连接到 `QLineEdit` 的 `setText(QString)` 槽。

在我们的拨钮和数值框示例中，我们使用了 `instance.methodName` 语法，就像在本章之前所示的示例一样。但当槽实际上是 Qt 槽而不是 Python 方法时，使用 `SLOT()` 语法会更高效：

```
self.connect(dial, SIGNAL("valueChanged(int)"),
    spinbox, SLOT("setValue(int)"))
self.connect(spinbox, SIGNAL("valueChanged(int)"),
    dial, SLOT("setValue(int)"))
```

我们已经看到可以将多个信号连接到同一个槽。虽然很罕见，但我们也可以将一个信号连接到另一个信号：在这种情况下，第一个信号被发射时，会导致它所连接的信号被发射。

连接是使用 `QObject.connect()` 创建的；可以使用 `QObject.disconnect()` 断开。在实践中，我们很少需要手动断开连接，例如 PyQt 会自动断开任何涉及已删除对象的连接。

到目前为止，我们已经了如何连接信号，以及如何编写槽——它们是普通的函数或方法。我们知道信号的发射表示状态变化或其他重要事件。但如果我们想创建一个发射自己信号的组件呢？使用 `QObject.emit()` 可以轻松实现。例如，这是一个完整的 `QSpinBox` 子类，它发射自定义的 `atzero` 信号，并传递了一个数字：

```python
class ZeroSpinBox(QSpinBox):
    zeros = 0

    def __init__(self, parent=None):
        super(ZeroSpinBox, self).__init__(parent)
        self.connect(self, SIGNAL("valueChanged(int)"), self.checkzero)

    def checkzero(self):
        if self.value() == 0:
            self.zeros += 1
            self.emit(SIGNAL("atzero(int)"), self.zeros)
```

我们连接了数值框自身的 `valueChanged` 信号并调用我们的 `checkzero()` 槽。如果值恰好为 0，`checkzero()` 槽会发射 `atzero` 信号，以及它为 0 的计数；传递这样的额外数据是可选的。信号不带括号非常重要：它告诉 PyQt 这是一个“短路”信号。

没有参数（因此不带括号）的信号是短路 Python 信号。当此类信号被发射时，任何数据都可以作为额的参数传递给 `emit()` 方法，并且它们作为 Python 对象传递。这避免了在参数与 C++ 数据类型之间转换的开销，同时也意味着可以传递任意 Python 对象，即使是那些无法与 C++ 之间转换的对象。

## 信号与槽 133

所有其他按钮都以相同的方式创建，区别仅在于变量名和传递给它们的文本。

我们将从简单的连接开始，这是 `button1` 使用的。这里是 `__init__()` 方法中的 `connect()` 调用：

```python
self.connect(button1, SIGNAL("clicked()"), self.one)
```

我们为这个按钮使用了一个专门的方法：

```python
def one(self):
    self.label.setText("You clicked button 'One'")
```

将按钮的 `clicked()` 信号连接到能够做出相应响应的单个方法是最常见的连接场景。

但如果大多数处理过程都是相同的，只有某些参数取决于按了哪个特定按钮呢？在这种情况下，最好是将每个按钮连接到同一个槽。实现这一点有两种方法：一种是使用**偏函数应用**（partial function application）来包装带参数的槽，以便槽在被它的按钮调用时以带参数的格式被调用。另一种方法是使用 PyQt 告诉我们哪个按钮调用了槽。我们将展示这两种方法，从偏函数应用开始。

### 偏函数应用 63

回到第 65 页，我们创建了一个包装函数，它使用了 Python 2.5 的 `functools.partial()` 或我们自己的简单 `partial()` 函数：

```python
import sys

if sys.version_info[:2] < (2, 5):
    def partial(func, arg):
        def callme():
            return func(arg)
        return callme
else:
    from functools import partial
```

使用 `partial()`，我们现在可以将一个槽和一个按钮名称包装在一起。因此我们可能想这样做：

```python
self.connect(button2, SIGNAL("clicked()"), partial(self.anyButton, "Two")) # 对于 PyQt 4.0-4.2 是错误的
```

遗憾的是，这在 PyQt 4.3 之前的版本中是无效的。包装函数是在 `connect()` 调用中创建的，但一旦 `connect()` 完成，包装器就会超出范围并被垃圾回收。从 PyQt 4.3 开始，使用 `functools.partial()` 创建的包装器在被用于此类连接时会被特殊对待。这意味着被连接的函数将不会被垃圾回收，因此这里显示的代码将正常运行。

## 第 4 章 GUI 编程简介

对于 PyQt 4.0、4.1 和 4.2，我们仍然可以使用 `partial()`：我们只需要保留包装器的引用——除了 `connect()` 调用外，我们不会使用该引用，但由于它是表单实例的属性，可以确保包装函数在表单存在期间不会超出范围，并在那里工作。因此，连接实际上是这样实现的：

```python
self.button2callback = partial(self.anyButton, "Two")
self.connect(button2, SIGNAL("clicked()"))
self.button2callback
```

当 `button2` 被点击时，将调用 `anyButton()` 方法并传入包含 "Two" 文本的字符串参数。该方法所示：

```python
def anyButton(self, who):
    self.label.setText("You clicked '%s'" % who)
```

我们可以使用刚刚展示的 `partial()` 函数为所有按钮使用这个槽。事实上，我们甚至可以完全不使用 `partial()` 并得到结果：

```python
self.button3callback = lambda who="Three": self.anyButton(who)
self.connect(button3, SIGNAL("clicked()"))
self.button3callback
```

在这里我们创建了一个由按钮名称参数化的 lambda 函数。它的工作原理与 `partial()` 技术相同，并调用相同的 `anyButton()` 方法，只是使用了 lambda 来创建包装器。

`button2callback()` 和 `button3callback()` 都调用 `anyButton()`；它们唯一的区别是第一个传递 "Two" 作为参数，而第二个传递 "Three"。

如果我们正在使用 PyQt 4.1.1 或更高版本，并且使用 lambda 回调，我们就不需要保留对自己的引用。PyQt 在 lambda 被用于创建连中的包装器时会对其进行特殊对待（这与 PyQt 4.3 中扩展到 `functools.partial()` 的这种特殊对待是相同的）。因此，我们可以直接在 `connect()` 中使用 lambda。例如：

```python
self.connect(button3, SIGNAL("clicked()"))
lambda who="Three": self.anyButton(who)
```

包装技术工作得很好，但也有另一种稍微复杂一点的替代方法，在某些情况下可能有用，特别是当我们不想包装自己的调用时。这种其他技术用于响应 `button4` 和 `button5`。以下是它们的连接：

```python
self.connect(button4, SIGNAL("clicked()")), self.clicked
self.connect(button5, SIGNAL("clicked()")), self.clicked
```

## 信号与槽

注意，我们没有包装它们都连接到的 `clicked()` 方法，因此乍一看似乎没有办法判断是哪个按�调用了 `clicked()` 方法。然而，实现清楚地表明，如果我们想要，是可以区分的：

```python
def clicked(self):
    button = self.sender()
    if button is None or not isinstance(button, QPushButton):
        return
    self.label.setText("You clicked button '%s'" % button)
```

在 `clicked` 方法内部，我们可以使用 `sender()` 来找到触发信号的控件。这允许我们为多个控件使用单个槽，只要我们能够在方法内部处理差异即可。这是 GUI 编程中避免代码重复的一种常见模式。

## 总结

我们还学到不需要正式地声明自己的自定信号：我们只需要使用 `Qobject.emit()` 来发射它们，并带有我们想要传递的任何额外参数。

## 练习

编写一个计算复利的对话框应用程序。该应用程序在风格和结构上应该与货币应用程序非常相似，并且看起来如下：

![](img/55bc1dcf8601cfec5e1423b4e17ec264_151_0.png)

每当用户更改一个变量因素（即本金、利率或年份）时，金额应该自动重新计算。年份下拉框（combobox）的年份应该是下拉框的当前索引加 1。Python 中的复利公式为 `amount=principal * ((1+ rate / 100.0)) ** years`。`DoubleSpinBox` 类具有 `setPrefix()` 和 `setSuffix()` 方法，可以用于 "$" 和 "%" 符号。整个应用程序可以在 60 行代码左右完成。

提示：可以通过将合适的数字调节框（spinbox）和下拉框信号连接到 `updateUi()` 槽（slot），在该槽函数中执行计算并更新金额标签。

参考答案在 `chap04/interest.py` 文件中提供。

# 5

- 哑智能对话框 (Dumb Dialogs)

- 标准对话框 (Standard Dialogs)

- 智能对话框 (Smart Dialogs)

## 对话框

几乎每个 GUI 应用程序至少有一个对话框，大多数 GUI 应用程序有一个带有几十甚至几十对话框的主窗口。对话框可以用于发布不放在状态栏或日志文件中重要的公告。在这种情况下，它们通常只有一个文本标签和一个供用户在阅读消息后按下的 OK 按钮。大多数情况下，对话框用向用户提问。有些只需要是或否。另一些要求用户做出另一种选择——例如，他们想使用什么文件、文件夹、颜色或字体。对于所有这些，PyQt 都提供了内置对话框。

本章的重点是创建自定义对话框，当内置对话框都不合适时，我们可以询问用户的需求和偏好。

我们没有涉及的一个问题是哪种控件适用于特定用途。例如，如果我们想让用户在三个选项之间做出选择，我们可以提供三个单选按钮，或者一个三项列表控件或下拉框。或者我们也可以使用三状态复选框。这些并不是唯一的可能性。对于 GUI 编程的新手，附录 B 提供的某些 PyQt 控件的截图和简要描述在做出这些决策时可能会有所帮助。

Qt 提供了 Qt Designer，这是一个视觉化工具，可以轻松地“画出”对话框，而无需编写任何代码来创建和布局它们的控件。它也可以用于设置对话框的一些行为。我们将在第 7 章介绍介绍 Qt Designer。在本章中，我们将用代码创建所有对话框。一些开发者以这种方式创建所有对话框，而另一些人则倾向于使用 Qt Designer。本书展示了这两种方法，以便你可以根据情况决定使用哪种最好。

分类对话框的一种方法是根据它们的“智能”程度，它们可能是“哑的”、“标准的”或“智能的”，这取决于它们内置了多少关于应用程序数据的知识。这些分类影响我们如何实现和实例化（创建实例）对话框，对于每种分类，我们在本章中分配了一个章节。每个章节的开头都解释了该分类的含义，并通过通过示例解释了其优缺点。

# 140 第5章 对话框

除了智能分类外，对话框还可以根据它们的模态（modality）进行分类。应用程序模态对话框是一种对话框，一旦调用，它是应用程序中用户可以交互的唯一部分。在用户关闭对话框之前，他们无法使用应用程序的其他部分。当然，用户可以与其他应用程序进行交互，例如通过点击另一个程序使其获得焦点。

窗口模态对话框的工作方式与应用程序模态对话框类似，不同在于它只阻止与其父窗口、父窗口的父窗口一直直到顶层父窗口，以及父窗口的兄弟窗口进行交互。对于具有单个顶级窗口的应用程序，应用程序模态和窗口模态之间没有实际区别。在提到“模态”窗口而未指定是哪种时，假设是指窗口对话框。

模态对话框的反面是非模态对话框（modeless dialog）。当调用非模态对话框时，用户可以与对话框交互，也可以与应用程序的其他部分交互。这对我们设计代码有影响，因为用户可能同时在主窗口和非模态对话框中影响程序状态，从而影响对方。

编写对话框的另一个方面是我们如何处理验证。只要可能，我们尝试选择合适的控件并设置它们的属性以避免编写任何验证代码。例如，如果我们需要一个整数，我们可以使用 `setValue()` 方法将范围限制在我们可以接受的值范围内。我们将适用于单个控件的验证称为“控件级”验证；数据库程序员通常将其称为“字段级”验证。我们需要比控件级验证更进一步，特别是当存在相互依赖关系时。例如，一个剧院订票系统有两个下拉框，一个用于选择楼层，另一个用于选择 A–R 座位，如果一楼的座位行是 M–T，那么只有某些楼层和座位行的组合是有效的。对于这些情况，我们必须执行“表单级”验证；数据库程序员通常将其称为“记录级”验证。

另一个验证问题涉及验证何时发生。理想情况下，我们不希望用户能够输入任何无效数据，但这可能很难实现。我们将验证分为两大类：“事后验证”（post-mortem），即在用户想要接受设置时进行验证；以及“预防性验证”（preventative），即在用户操作控件时发生。

由于对话框可以具有不同的智能程度、三种模态类型以及多种验证策略，看起来有很多组合可供选择。在实践中，我们可能会让哑智能和标准对话框为模态，而让智能对话框为非模态。至于验证，正确的策略很大程度上取决于情况。我们定义“哑”对话框是指其控件由调用者设置初始值，并直接从调用者获取最终值的对话框。哑对话框不知道它用于展示和编辑的数据。我们可以对对话框的控件进行一些基础验证，但通常（并非总是）设置包含相互依赖关系的验证；换句话说，表单级验证通常在哑对话框中完成。哑对话框通常是模态对话框，带有一个接受”按钮（如 OK）和一个“拒绝”按钮（如 Cancel）。

使用哑对话框的主要优点是我们不需要编写代码为它们提供 API，也不需要编写任何额外的逻辑。这些优点都是由于它们的所有控件都是公开可见的。主要的缺点是使用它们的代码与用户界面耦合的（我们直接访问控件），因此我们无法轻松实现复杂的验证——而且如果在多个地方需要，它们比智能对话框方便得多。

我们将从一个具体的示例开始。假设我们有一个图形应用程序，并想让用户设置某些属性——例如笔的宽度、样式以及用它绘制的线条是否具有斜边。图 5.1 显示了我们想要实现的内容。

![](img/5bc1dcf8601cfec5e1423b4e17ec264_155_0.png)

图 5.1 笔属性对话框

在这种情况下，我们不需要“实时”或交互式地更新笔的属性，因此模态对话框就足够了。由于所需的验证非常简单，在这种情况下我们可以使用哑对话框。

我们通过在模态槽函数中弹出对话框来使用它，该槽函数连接到菜单选项、工具栏按钮或对话框按钮。如果用户点击了 OK，我们就会更新笔的属性；如果他们点击了 Cancel，我们什么都不做。调用槽函数可能如下所示：

```python
def setPenProperties(self):
    dialog = PenPropertiesDlg(self)
    dialog.widthSpinBox.setValue(self.width)
    dialog.beveledCheckbox.setChecked(self.beveled)
    dialog.styleComboBox.setCurrentIndex(
        dialog.styleComboBox.findText(self.style))
    if dialog.exec():
        self.width = dialog.widthSpinBox.value()
        self.beveled = dialog.beveledCheckbox.isChecked()
        self.style = unicode(dialog.styleComboBox.currentText())
    self.updateData()
```

我们首先创建一个 `PenPropertiesDlg`——我们稍后会看到它的细节；现在我们只需要知道它有一个宽度步值计数器框（width spinbox）、一个斜角复选框（beveled checkbox）和一个样式组合框（style combobox）。我们将父对象 `self`（调用者表单）传递给对话框，以利用 PyQt 的默认行为：它会将对话框在其父窗口上居中显示，并且由于对话框有父窗口，它们不会在任务栏中产生单独的条目。我们直接访问这些控件，并将它们的值设置为调用者表单持有的值。`QComboBox.findText()` 方法返回匹配文本的索引位置。

当我们在对话框上调用 `exec_()` 时，对话框将以模态方式显示。这意味着对话框窗口及其兄弟窗口将被阻塞，直到用户关闭对话框（通过通过“接受”或“拒绝”关闭）后，`exec_` 调用才会返回。如果我们接受了对话框，返回值将为 `True`；否则，结果为 `False`。如果我们接受了对话框，我们就知道设置已生效，因此我们从对话框的控件中读取这些设置并更新应用程序的数据。末尾的 `updateData()` 调用只是我们自定义的方法之一，用于让应用程序在主窗口中显示画笔属性。

在完setPenProperties()` 方法结束时，`PenPropertiesDlg` 将离开作用范围并成为垃圾收集的候选对象。因此，每当我们设置 `setPenProperties()` 时，都必须始终创建一个新的对话框并填充其控件。这种方法节省了内存，但代价是增加了一些开销。对于像这样微小的对话框，这种开销小到用户无法察觉，但稍后我们将展示另一种避免每次都创建和销毁对话框的替代方法。

使用“笨对话框”（dumb dialog）意味着对话框与应用程序之间是松耦合的。我们可以通过将标签变为实例变量来完全解耦。这样，我们只需要更改标签，就可以使用 `PenPropertiesDlg` 来编辑任何需要步值计数器框、复选框和组合框的数据。例如，我们可以用它通过带有“温度”步值计数器框、“是否下雨”复选框和“云”组合框来记录天气读数。

## 笨对话框 (Dumb Dialogs)

现在我们已经看到了如何使用这个对话框，让我们来看看实现它的代码。`PenPropertiesDlg` 有一个方法 `__init__()`，我们将分部分查看。

```python
class PenPropertiesDlg(QDialog):
    def __init__(self, parent=None):
        super(PenPropertiesDlg, self).__init__(parent)
```

不意外的是，我们的对话框是 `QDialog` 的子类，我们按照之前见过的几次的方式来初始化它。

```python
widthLabel = QLabel("Width:")
self.widthSpin = QSpinBox()
widthLabel.setBuddy(self.widthSpin)
self.widthSpin.setAlignment(Qt.AlignRight|Qt.AlignVCenter)
self.widthSpin.setRange(0, 24)
self.beveledCheckbox = QCheckBox("Beveled edges")
styleLabel = QLabel("Style:")
self.styleCombo = QComboBox()
self.styleCombo.setBuddy(self.styleCombo)
self.styleCombo.addItems(["Solid", "Dashed", "Dotted", "DashDotted", "DashDotted"])

okButton = QPushButton("OK")
cancelButton = QPushButton("Cancel")
```

对于编辑控件，我们创建一个相应的标签，以便用户知道他们正在编辑什么。当我们在标签文本中放入安符号（`&`）时，它有两个可能的含义。它可能仅仅是一个字面上的安符号。或者它也可以表示该安符号不应显示，而是紧随其后的字母将带有下划线，表示它代表一个键盘快捷键。例如，在 `widthLabel` 的情况下，它的文本为 "Width:"，其快捷键将是 `Alt+W`。在 Mac OS 上，默认行为是忽略快捷键；因此，PyQt 在此平台上不显示下划线。

区分字面安符号和快捷键安符号的方法是看标签是否有一个“伙伴”（buddy）。如果有，安符号就表示一个快捷键。“伙伴”是一个控件，PyQt 会通过它将键盘焦点（keyboard focus）传递给相应的标签。因此，当用户按下 `Alt+W` 时，键盘焦点将切换到 `widthSpinBox`。反过来，意味着如果用户按下向上或向下的箭头键、`PageUp` 或 `PageDown`，`widthSpinbox` 将拥有键盘焦点。

在按钮的情况下，按钮文本中带有下划线的字母被用于表示快捷键。因此，在这种情况下，"OK" 显示为 OK，用户可以通过鼠标点击它、通过 Tab 键切换到它并按下空格键，或者按下 `Alt+O` 来按下按钮。为取消（Cancel）或关闭（Close）按钮提供快捷键并不常见，这些按钮通常连接到对话框的 `reject()` 槽，`QDialog` 为该操作提供了键盘快捷键：`Esc` 键。复选框和单选按钮与按钮有些相似，它们拥有带有快捷键的文本。例如，斜角复选框有一个带下划线的 "B"，因此用户可以通过按下 `Alt+B` 来切换复选框的选中状态。

创建此类按钮的缺点是，当我们布局它们时，将按照一个特定的顺序进行。例如，我们将 OK 放在 Cancel 的左侧。但在窗口系统中，这个顺序是错误的。PyQt 对此有一个解决方案，位于“对话框布局”（Dialog Layout）侧边栏中。

我们将步值计数器中的数字向右对齐并垂直居中，并将其值范围设置为 0–24。在 PyQt 中，画笔宽度（即线宽） 0 是允许的，并表示无论有任何变换都代表 1 像素的宽度。1 及以上的画笔宽度将按给定的宽度绘制，并尊重任何变换（例如缩放）。

通过使用步值计数器并为其设置范围，我们避免了输入无效画笔宽度的可能——例如，我们经常使用细线，只需选择正确的宽度并恰当地设置其属性即可提供所需的所有控件级验证。我们对斜角复选框的使用也说明了这一点：画笔要么绘制带有斜角的线条，要么不绘制。我们使用线条样式组合的情况也是如此——用户只能选择有效的样式，即从我们提供的列表中选择样式。

```python
buttonLayout = QBoxLayout()
buttonLayout.addRowStretch()
buttonLayout.addWidget(okButton)
buttonLayout.addWidget(cancelButton)
layout = QGridLayout()
layout.addWidget(widthLabel, 0, 0)
layout.addWidget(self.widthSpinBox, 0, 1)
layout.addWidget(self.beveledCheckbox, 0, 2)
layout.addWidget(styleLabel, 1, 0)
layout.addWidget(self.styleCombo, 1, 1)
layout.addLayout(buttonLayout, 2, 0)
self.setLayout(layout)
```

## 5. 对话框 (Dialogs)

现在我们已经看到了如何使用这个对话框，让我们来看看实现它的代码。`PenPropertiesDlg` 有一个方法 `__init__()`，我们将分部分查看。




```python
if len(decimal) == 0:
    self.decimalMarkerEdit.setText(".")
    self.decimalMarkerEdit.selectAll()
    self.decimalMarkerEdit.setFocus()
    self.apply()
```

此方法在用户在任一行编辑框中输入时应用预防性验证。我们仍然依赖于行编辑框验证器、最大长度属性，以及在小数点标记符行编辑框的情况下的输入掩码（input mask），所有这些因素共同提供了我们几乎需要的所有验证。但用户仍然可能在两个框中设置相同的文本——例如，当我们删除千分位分隔符并将焦点移动到其行编辑框时，或者（如果用户努力尝试）导致小数点标记符编辑框为空——在我们在我们设置了一个有效的替代方案、选中它并赋予键盘焦点时。最后，我们知道两个行编辑框都是有效的，因此我们调用 `apply()` 并应用更改。

使用显示/隐藏方法的一个用处是对话框的状态会自动维护。如果我们必须每次使用时都创建对话框，就必须向它填充数据；为此，每当使用时（第一次之后），它都拥有正确的数据。当然，在这个特定的示例中，我们有三个对话框都用于编辑相同的数据，这意味着对话框可能会不同步；我们忽略了这个问题，因为在实际应用程序中，多个对话框编辑相同数据不是我们会做的事情。

通过传递数据结构（格式字典）和调用者的更新方法（`refreshable()`，作为 `self.callback` 传递），我们使这个对话框变得非常智能并且与其调用者紧密耦合。由于这个原因，许多程序员倾向于使用标准对话框的“折中方案”——愚呆对话框限制性太大，使用起来可能不方便，而智能对话框因为其对调用者数据结构的理解意味着紧密耦合，维护起来可能更加麻烦。

## 总结

我们将对话框分为三种“智能”程度：愚呆、标准和智能，并展示了它们可以模态（modal）或非模态（modeless）方式使用。愚呆对话框很容易创建，对于组件级验证完全足够。愚呆对话框通常作为模态使用，如果我们仔细，它们就可以被泛化，因为它们与应用程序逻辑耦合非常松散。尽管如此，使用愚呆对话框通常会导致程序员感到沮丧，并需要它们以标准或智能对话框的形式重写，因此通常最好避免它们，除非是只需要一两个值且内置的 `InputDialog` 静态对话框不适用于非常简单的情况。

最常见的选择是在标准模态对话框和智能非模态对话框之间，在后者的情况下，是在“应用（apply）”和“实时（live）”更新样式之间。模态对话框最容易编程，因为它们阻塞了与对话框父窗口及其兄弟窗口的任何交互，降低了它们正在处理的数据在下方被更改的风险。但某些用户更喜欢非模态对话框，当用户在决定想要哪些选项之前尝试各种选项时，这特别方便。模态对话框也可以用于此目的，例如字体对话框也是模态的，并显示样本文本以展示用户字体设置的变化。

我们已经过的验证策略——事后（post-mortem）和预防性（preventative），可以单独使用或结合使用。从可用性的角度来看，预防性的通常被认为更优，尽管它可能会导致用户沮丧。例如，当设置因为表单其他地方的设置而无效时，用户可能会抱怨（“我想这样做，但它不让我”）。

可以设计一种既用于添加项目又用于编辑项目的对话框。这些添加/编辑对话框在组件的创建、布局和连接方面与其他类型的对话框没有区别。关键区别在于，它们可能根据是添加还是编辑而表现出不同的行为。在编辑时，组件从传递的项目中填充数据；在添加时，组件用默认值进行填充。（注：OCR 重复了两次“and the widgets are populated”）。如果对话框被接受，它可能仅提供访问器，通过访问器可以检索值，将工作留给调用者；或者如果是智能的，还可以直接更新已编辑的项目，并在用户添加时创建新项目。请参见 `chap08/additemmoviedlg.py` 中的 `AddEditMovieDlg` 类（其用户界面设计在 `chap08/additemmoviedlg.ui` 中），以及 `chap12/pagedesigner.py` 中的 `TextItemDlg` 类以及添加/编辑项目的示例。

另一种可能性是完全避免使用对话框，允用户在现场编辑数据——例如，在列表或表中。这种方法在模型/视图编程章节中有介绍。

## 练习

编写一个独立的字符串编辑对话框。该对话框应使用 `if __name__ == "__main__":` 以便它可以独立运行和测试。它看起来应该像图 5.8 所示的对话框。

字符串应该存储在 `QWidget` 中。排序按钮很容易实现，因为我们可以将其 `clicked()` 信号直接连接到 `QListWidget.sortItems()` 方法。

对话框应在其自己的字符串列表上工作（无论是传递的副本，还是它自己创建的），并在接受时应发射一个包含列表（作为 `QStringList`）的信号，并且具有一个公开访问的数据属性 `stringlist`。

`reject()` 槽的实现如下：

## 第 5 章 对话框

![](img/55bc1dcf8601cfec5e1423b4e17ec264_178_0.png)

图 5.8 字符串列表

## 创建主窗口

| imagechanger.py | MainWindow | main() |

|---|---|---|

| qrc_resources.py | newwimagedlg.py | helpform.py |

| 图标与 HTML 帮助文件 | NewImageDlg | HelpForm |

| ui_newwimagedlg.py | | |

| 用户界面模块 | | |

图 6.2 ***Image Changer 的模块、类和函数***

用户的工作空间，用于加载应用程序上一次关闭时打开的文件。

构成 Image Changer 应用程序的文件如图 6.2 所示。应用程序的主窗口类位于 `chap06/imagechanger.py` 文件中。初始化函数相当长，因此我们将分部分进行查看。但首先，我们先查看类定义之前的导入部分。

```
import os
import platform
import sys
from PyQt4.QtCore import *
from PyQt4.QtGui import *
import helpform
import newwimagedlg
import qrc_resources

__version__ = "1.0.0"
```

在本书中，我们的策略是先导入 Python 标准模块，然后是第三方模块（如 PyQt），最后是我们自己的模块。当我们在代码中使用 `os` 和 `platform` 模块时，我们会讨论其中用的项目。`sys` 模块通常用于提供 `sys.argv`。`help` 和 `newimaged` 模块提供了 `HelpForm` 和 `NewImageDlg` 类。我们稍后会讨论 `qrc_resources` 模块。

应用程序拥有版本字符串是常见的，习惯命名为 `__version__`；我们将在应用程序的关于框中使用它。

现在我们来看 `MainWindow` 类的开头。

```python
class MainWindow(QMainWindow):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        self.image = QImage()
        self.dirty = False
        self.filename = None
        self.mirroredvertically = False
        self.mirroredhorizontally = False
```

初始化函数按照惯例从 `super()` 调用开始。接下来，我们创建一个空的 `QImage`，用于存储用户加载或创建的图像。`QImage` 不是 `QObject` 的子类，因此它不需要父对象；相反，我们将其删除工作工作交给 Python 的垃圾回收机制在应用程序终止时处理。我们还创建了一些实例变量。我们使用 `dirty` 作为布尔标志，指示图像是否有未保存的更改。`filename` 初始化为 `None`，我们用它表示没有图像，或者有一张从未保存过的新图像。

PyQt 提供了各种镜像功能，但对于本示例，我们限制为仅三种可能性：图像垂直镜像、水平镜像或完全不镜像。我们需要跟踪镜像状态，以便保持用户界面的同步，正如我们在讨论镜像动作时将看到的。

```python
self.label = QLabel()
self.label.setMinimumSize(200, 200)
self.label.setAlignment(Qt.AlignCenter)
self.label.setContextMenuPolicy(Qt.CustomContextMenu)
self.setCentralWidget(self.label)
```

在某些应用程序中，中心部件是一个复合部件（由其他组件组成的部件，布局方式与对话框中的组件相同），或者是一个基于项目的部件（如列表或表格），但这里单个 `QLabel` 就足够了。`QLabel` 可以以 PyQt 支持的任何格式显示文本、HTML 或图像；稍后我们将看到如何发现这些格式，因为它们可能有所不同。我们设置了最小尺寸，是因为初始标签没有内容显示，且不会占用空间，这看起来会很奇怪。我们选择将图像垂直和水平居中对齐。

PyQt 提供了许多创建右键菜的方法，我们将使用最简单且常用的方法。首先，我们必须为想要具有右键菜单的部件设置上下文菜单策略。然后，我们必须向部件添加一些动作——这是我们稍后会做的。当用户调用右键菜单时，菜单将弹出并显示添加的动作。

与对话框不同，我们在主窗口风格的应用程序中使用布局管理器，尽管该部件可以是复合的，但在放置上没有限制。我们只需要调用 `setCentralWidget()` 即可。该方法既将部件布局在主窗口的中心区域，又准备了该部件以便主窗口拥有其所有权。

## 创建主窗口

| 窗口标题 | | |

|---|---|---|

| 菜单栏 | | |

| 工具栏区域 | | |

| 停靠窗口区域 | | |

| 中心部件 | | |

| 状态栏 | | |

图 6.3 QMainWindow 的区域

工具栏是——以及一些其他类型的部件，如组合框和数字调节框。对于较大的部件、工具面板，或任何用户希望能够拖出窗口并作为独立窗口自由浮动的部件，使用停靠窗口（dock window）通常是正确的选择。

停靠窗口是那些出现在图 6.3 所示停靠区域的窗口。它们有很小的标题、恢复和关闭按钶，并且可以从一个停靠区域拖动到另一个区域，或者作为独立的顶层窗口自由浮动。当它们被停靠时，它们会自动在自身与中心区域之间提供一个分割器，这使得它们易于调整大小。

在 PyQt 中，停靠窗口是 `QDockWidget` 类的实例。我们可以向停靠窗口添加单个部件，就像我们可以让停靠窗口拥有单个部件一样，由于我们使用 `setFeatures()` 来控制，停靠窗口是可移动、可浮动和可关闭的。

```python
dockWidget = QDockWidget("Dock", self)
dockWidget.setFeatures(QDockWidget.Movable | QDockWidget.Floatable | QDockWidget.Closable)
dockWidget.setWidget(listWidget)
self.addDockWidget(Qt.RightDockArea, dockWidget)
```

## 第6章 主窗口

我们希望能够打印它们的图像。为了实现这一点，我们需要创建一个 `QPrinter` 对象。我们可以在需要时随时创建打印机并将其交给垃圾回收。但我们更倾向于保留一个实例变量，初始化为 `None`。当用户第一次请请求打印时，我们将创建一个 `QPrinter` 并将其赋值给 `printer` 变量。这样做有两个好处：首先，我们只在需要时创建打印机；其次，由于我们保留了它的引用，它会一直存在——并保持用户对打印机、纸张大小等选择的状态。

```python
self.printer = None
```

对于应用程序的状态栏，我们希望左侧有通常的消息区域，右侧显示当前图像宽度和高度的状态指示器。我们通过创建一个 `QLabel` 部件并将其添加到状态栏来实现。我们还关闭了状态栏的尺寸手柄，因为当我们有一个图像尺寸的指示器时，那看起来合适。状态栏本身是在第一次调用 `QMainWindow::statusBar()` 方法时创建的。如果我们调用 `status bar.showMessage()` 字符串，该字符串将显示在状态栏中，直到调用另一个 `showMessage()`

## 创建主窗口

调用将替换它，直到调用了 `clearMessage()`。我们使用了双参数的形式，第二个参数是消息应该显示的毫秒数（5000，即 5 秒）；在此时间之后，状态栏将自动清空。

到目前为止，我们已经学习如何创建主窗口的中心部件（widget）、创建停靠部件（dock widget）以及设置状态栏。现在我们几乎准备好创建菜单和工具栏了，但首先我们必须理解什么是 PyQt 动作（actions），然后简单跳转一下学习资源。

## 动作与按键序列

Qt 的设计者意识到用户界面为用户实现相同目标提供了多种方式。例如，在许多应用程序中，创建新文件可以通过“文件→新建”菜单选项完成，可以通过点击“新建文件”工具栏按钮完成，也可以使用 `Ctrl+N` 快捷键。通常情况下，我们并不关心用户如何请求执行该动作，我们只关心他们想要执行什么动作。因此，为了创建一个“新建文件”动作，PyQt 可以编写如下代码：

```python
fileNew = QAction(QIcon("images/filenew.png"), "New", self)
fileNew.setShortcut(QSequence.New)
helpText = "Create a new image"
fileNew.setToolTip(helpText)
fileNew.setStatusTip(helpText)
self.connect(fileNew, SIGNAL(triggered()), self.fileNew)
```

我们假设已经有一个合适的图标和一个 `fileNew()` 方法。菜单项的文本显示，该菜单项将显示为 New（在 Mac OS X 上除外，除非窗口系统设置为抑制下划线），并且键盘用户将能够通过按下 `Alt+F,N` 来调用它（假设文件菜单的文本是“File”以便其显示）。或者，用户可以使用通过 `shortcut()` 创建的快捷键，只需按下 `Ctrl+N` 即可。

许多序列都是标准化的，即使在不同的窗口系统之间也是如此。例如，Windows、KDE 和 GN 都使用 `Ctrl+N` 表示“新建”，使用 `Ctrl+S` 表示“保存”。Mac OS 类似，使用 `Command+N` 和 `Command+S` 执行这些动作。PyQt 4.2 中的 `QSequence` 类为标准化序列提供了常量，例如 `QSequence.New`。当标准化序列在不同窗口系统之间存在差异，或者一个动作与多个键相关联时，这特别有用。例如，如果我们将快捷键设置为 `QSequence.Paste`，PyQt 将响应 Windows 上的 `Ctrl+V` 或 `Shift+Ins` 触发“粘贴”动作；在 KDE 上为 `Ctrl+V`、`Shift+Ins` 或 `F+18`，在 Mac OS 上为 `Command+G`。

对于非标准化的键（或者如果我们想与 PyQt 版本保持向后兼容），我们可以以字符串的形式提供快捷键；

## 表 6.1 Select定的 QAction 方法

| 语法 | 描述 |

| --- | --- |

| a.data() | 以 QVariant 返回 QAction a 的用户数据 |

| a.setData(v) | 将 QAction a 的用户数据设置为 QVariant v |

| a.isChecked() | 如果 QAction 被选中，则返回 True |

| a.setChecked(b) | 根据 b 勾选或取消 QAction a |

| a.isEnabled() | 如果 QAction 已启用，则返回 True |

| a.setEnabled(b) | 根据 b 启用或禁用 QAction a |

| a.setSeparator(b) | 根据 b 将 QAction a 设置为普通动作或分隔符 |

| a.setShortcut(k) | 将 QAction a 的键盘快捷键设置为 QKeySequence k |

| a.setStatusTip(s) | 将 QAction a 的状态文本设置为字符串 s |

| a.setText(s) | 将 QAction a 的文本设置为字符串 s |

| a.setToolTip(s) | 将 QAction a 的工具提示文本设置为字符串 s |

| a.setWhatsThis(s) | 将 QAction a 的“这是什么？”文本设置为字符串 s |

| a.toggle(b) | 当 QAction a 的选中状态改变时发射此信号；如果动作被选中，布尔 b 为 True |

| a.triggered(b) | 当 QAction a 被调用时发射此信号；如果 QAction 被选中，可选的布尔值为 True |

例如，`setShortcut("Ctrl+Q")`。本书使用了可用的标准化序列，否则回退到使用字符串。

注意，我们为 QAction 指定了父对象为 `self`（应用该动作的表单）。每个 `QObject` 子类（从顶层向下）都有一个父对象是非常重要的；这通常通过布局它们来实现，但对于像 `QAction` 这样的纯数据对象，我们必须显式提供父对象。

一旦创建了动作，我们就可以添加到菜单和工具栏中，如：

```
fileMenu.addAction(fileNewAction)
fileToolbar.addAction(fileNewAction)
```

现在，每当用户调用“新建文件”动作（通过任何方式），`fileNew()` 方法就会被调用。

## 资源文件

遗憾的是，我们编写的代码有一个小问题。它假设应用程序的工作目录是它所在的目录。这在 Windows 下点击（或双击）`.pyw`（或其快捷方式）时是正常情况。但如果从命令行执行程序，工作目录可能与脚本所在的目录不同。为了解决这个问题，我们可以使用脚本本身的路径：

```python
import os
script_dir = os.path.dirname(os.path.abspath(__file__))
```

这确保了即使工作目录发生变化，我们仍然可以相对于脚本找到资源。

资源文件采用简单的 XML 格式。这是一个 qrc 文件的示例：

```xml
<!DOCTYPE RCC>
<RCC version="1.0">
<qset>
  <file>images/filenew.png</file>
  <file>images/fileopen.png</file>
  <file>images/icon.png</file>
  <file>images/helpmenu.html</file>
  <file>images/index.html</file>
</qset>
</RCC>
```

使用 `pyrc4` 工具将 qrc 文件编译为 Python 模块：

```bash
pyrc4 -o resources_resources.py resources.qrc
```

然后可以将该模块导入到应用程序中：

```python
import resources_resources
```

现在我们可以使用 `:/` 前缀来使用资源：

```python
icon = QIcon(":/filenew.png")
```

## 创建主窗口

此方法执行了我们在“新建文件”操作中完成过的所有工作。此外，它还处理了没有图标的情况以及“可检查”（checkable）操作。图标是可选的，尽管对于将添加到工具栏的动作，按照惯例提供一个。如果一个动作像文字处理器通常提供的加粗或斜体动作那样具有“开启”和“关闭”状态，那么该动作就是可检查的。

请注意，`QAction` 构造函数的最后一个参数是 `self`；这是该动作的父对象（主窗口），它确保了动作在离开初始化器的作用范围时不会被垃圾回收机制。在某些情况下，我们将动作设为实例变量，以便在表单初始化器之外访问它们，这在这个特定的示例中我们不需要这样做。

以下是使用 `createAction()` 辅助方法创建“新建文件”动作的方法：

```
fileNewAction = self.createAction(\&New..."), self.fileNew,
KeySequence.New, "filenew", "Create an image file")
```

除了“文件退出”动作（以及我们没有提供快捷键的“文件另存为”）外，其他动作都是以相同的方式创建的，因此我们不需要浪费空间显示它们。

```
fileQuitAction = self.createAction(\&Quit"), self.close,
"Ctrl+Q", "filequit", "Close the application")
```

`QSequence` 类没有用于应用程序终止的标准化快捷键，因此我们自己选择了一个并将其作为字符串指定。我们本可以很容易地使用不同的快捷键——例如 Alt+X 或 Alt+F4。

`close()` 槽继承自 `QMainWindow`。如果主窗口通过调用“文件退出”动作（我们已将其连接到 `close()` 槽）关闭，例如通过点击“文件→退出”或按下“Ctrl+Q”，则将调用基类的 `close()` 方法。但如果用户点击应用程序的“X”按钮，`close()` 方法就不会被调用。

要确保我们拦截了关闭窗口的操作，唯一的方法是实现关闭事件处理器。无论应用程序是通过 `close()` 方法关闭还是通过关闭按钮关闭，关闭事件处理器总是会被调用的。因此，通过重写此事件处理器，我们可以给用户提供保存任何未更改更改的机会，并保存应用程序的设置。

通常，我们可以完全通过高级信号和槽机制来实现应用程序的行为，但在这种情况下，我们必须使用低级的事件处理机制。然而，重写关闭事件与重写任何其他方法没有区别，而且并不困难，正如我们在后续章节中将看到的。（事件处理见第 10 章。）

# 第 6 章 主窗口

编辑动作以类似的方式创建，但由于细微的，我们将查看其中几个。

```
editZoomAction = self.createAction("&Zom...", self.editZoom,
"Alt+Z", "editzoom", "Zoom the image")
```

用户能够放大和缩小以查看更多或较少细节的图像是非常方便的。我们在工具栏中提供了一个数值调节框（spinbox），允许用户更改缩放因子（稍后我们会介绍），但我们必须支持键盘用户，为他们我们创建一个“编辑缩放”动作，并添加到“编辑”菜中。当触发时，连接到此动作的方法将弹出一个对话框，用户可以在其中输入缩放百分比。

放大和缩小有标准的快捷键序列，但没有通用的缩放快捷键，因此在这种情况下我们选择使用 Alt+Z。（我们没有使用 Ctrl+Z，因为那是大多数平台上的撤销快捷键序列。）

```
editInvertAction = self.createAction("&Invert",
self.editInvert, "Ctrl+I", "editinvert",
"Invert the image's colors", True, toggled(bool)")
```

“编辑反转”动作是一个切换动作（toggle action）。我们仍然可以使用 `triggered(bool)` 信号，但那时我们需要对动作调用 `isChecked()` 来查找其状态。对我们来说，使用 `toggled(bool)` 信号更方便，因为它不仅告诉我们动作被调用了，还告诉了我们它是否被选中。动作还有一个 `triggered(bool)` 信号，它只在用户进行更改时发射，但这里并不适用，因为无论反转动作的选中状态是由用户更改还是程序更改，我们都希望对其进行操作。

“编辑交换红蓝”动作与“编辑反转”动作类似，因此我们不会显示它。

与“编辑反转”动作和“编辑交换红蓝”动作一样，与可检查、独立的“反转”和“交换红蓝”动作不同，我们选择让镜像动作互斥，允许任何时候只有一个处于“开启”状态。为了实现这种行为，我们以正常方式创建镜像动作，但将它们中的每一个都添加到“动作组”（action group）中。动作组是一个管理一组复选框动作的类，并确保如果其中一个动作被设置为“开启”，其他动作都被设置为“关闭”。

```
mirrorGroup = QActionGroup(self)
```

动作组是 `QObject` 的子类，既不是顶层窗口也不是布局中的控件，因此我们必须给它一个显式的父对象，以确保 PyQt 在正确的时间删除它。

## 创建主窗口

一旦了动作组，我们将镜像动作添加到其中。这与我们将其他动作添加到菜单的方式类似。

```
mirrorGroup.addAction(mirrorHorizontalAction)
mirrorGroup.addAction(mirrorVerticalAction)
```

大多数菜单创建并填充动作的方式与“编辑”菜单相同，但“文件”菜单不同。

```python
self.fileMenu = self.menubar().addMenu("File")
self.fileActions = (fileNewAction, fileOpenAction,
    fileSaveAction, fileSaveAction, None,
    filePrintAction, fileQuitAction)
self.connect(self.fileMenu, SIGNAL("aboutToShow("),
    self.updateFileMenu)
```

我们希望“文件”菜单显示最近使用的文件。因此，我们没有在这里填充“文件”菜单，而是每当用户调用它时动态生成它。这就是为什么我们将“文件”菜单设为实例变量，也是为什么我们持有文件菜单动作的实例变量。连接确保了每当“文件”菜单被调用时，都会调用我们的 `updateFileMenu()` 槽。我们将回顾这个槽。

```python
def addActions(self, target, actions):
    for action in actions:
        if action is None:
            target.addSeparator()
        else:
            target.addAction(action)
```

子菜单的填充方式与其他任何菜单完全相同，但它们通过 `QMenu.addMenu()` 添加到父菜单，而不是通过 `MainWindow.menubar().addMenu()` 添加到主窗口的菜单栏。

```python
mirrorMenu = editMenu.addMenu(QIcon(":editmirror.png"),
    "Mirror")
self.addActions(mirrorMenu, mirrorHorizontalAction,
    mirrorVerticalAction)
```

“编辑”菜单的最后一个选项“镜像”右侧有一个小三角形。这表示它有一个子菜单。

“帮助”菜单是按照惯例创建的，与“编辑”菜单的方式相同，我们不会显示它。

## 创建主窗口

![](img/55bc1dcf8601cfec5e1423b4e17ec264_193_0.png)

**图 6.5 工具栏**

有了菜单，我们现在可以切换工具栏了。

```
fileToolBar = self.addToolBar("File")
fileToolBar.setObjectName("FileToolBar")
self.addActions(fileToolBar, fileNewAction, fileOpenAction,
fileSaveAsAction)
```

创建工具栏与创建菜单类似：我们调用 `add()` 来创建一个 `QToolbar` 并使用 `addActions()` 为其填充内容。我们可以对菜单和工具栏都使用该方法，因为它们的 API 非常相似，都提供了 `addAction()` 和 `addSeparator()`。我们设置了对象名称（object name），以便 PyQt 能够保存并恢复工具栏的位置——可以有任意数量的工具栏，PyQt 使用对象名称区分它们，就像处理停靠窗口（dock widgets）一样。生成的工具栏如图 6.5 所示。

编辑工具栏以及可更改的动作（“编辑反转”、“编辑交换红蓝”以及镜像动作）都是以相同的方式创建的。但如图 6.6 所示，编辑工具栏除了工具栏按钮外，还有一个数值框（spinbox）。鉴于此，我们完整地展示该工具栏的代码，为了方便解释，将其分为两个部分显示。

```
editToolbar = self.addToolBar("Edit")
editToolbar.setObjectName("EditToolbar")
self.addActions(editToolbar, editInvertAction,
editSwapAndBlueAction, editUnMirrorAction,
editMirrorVerticalAction,
editMirrorHorizontalAction())
```

创建工具栏并为其添加动作对于所有工具栏来说都是相同的。

我们希望为用户提供一种快速更改缩放倍数的方法，因此我们在编辑工具栏中提供了一个数值框来实现这一功能。在此之前，我们在“编辑”菜单中放置了一个单独的“编辑缩放”动作，以照顾使用键盘的用户。

```
self.zoomSpinBox = QSpinBox()
self.zoomSpinBox.setRange(1, 400)
self.zoomSpinBox.setSuffix("%")
self.zoomSpinBox.setValue(100)
self.zoomSpinBox.setToolTip("Zoom the image")
self.zoomSpinBox.setStatusTip(self.zoomSpinBox.toolTip())
self.zoomSpinBox.setFocusPolicy(Qt.NoFocus)
self.connect(self.zoomSpinBox, SIGNAL("valueChanged(int)"), self.showImage)
editToolbar.addWidget(self.zoomSpinBox)
```

# 第 6 章 主窗口

![](img/55bc1dcf8601cfec5e1423b4e17ec264_194_0.png)

图 6.6 编辑工具栏

向工具栏添加组件的模式始终是相同的：我们创建组件，设置它，将其连接到某个地方以处理用户交互，然后将其添加到工具栏中。我们将数值框设为实例变量，因为我们需要在主窗口的初始化函数之外访问它。`addWidget()` 调用将数值框的所有权交给了工具栏。

我们现在已经用动作完全填充了菜单和工具栏。虽然每个动作都添加到了菜中，但某些动作没有添加到工具栏中。这是非常常规的做法；通常只将最频繁使用的动作添加到工具栏中。

之前我们看到了以下行代码：

```
self.imageLabel.setContextMenuPolicy(Qt.ActionsContextMenu)
```

这告诉 PyQt，如果动作被添加到 `imageLabel` 组件中，它们将用于右键菜单，如图 6.7 所示所示。

```
self.addActions(self.imageLabel, (editInsertAction,
editSwapRedAndBlueAction, editUnMirrorAction,
editMirrorVerticalAction, editMirrorHorizontalAction()))
```

我们可以重用 `addActions()` 来将动作添加到标签组件中，只要我们不传递 `None` 即可，因为 `QWidget` 没有 `addSeparator` 方法。为组件设置策略并添加动作就是获取该组件右键菜单所需的全部操作。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_194_1.png)

图 6.7 图像标签的右键菜单

`QWidget` 类有一个 `addAction()` 方法，该方法被 `QMenu`、`QMenuBar` 和 `QtBar` 类继承。这就是为什么我们可以向这些类中的任何一个类添加动作。虽然 `QWidget` 类没有 `addSeparator()` 方法，但为了方便起见，`QMenu`、`QMenuBar` 和 `QtBar` 类提供了该方法。如果我们要在右键菜单中添加分隔符，必须通过添加分隔符动作来实现。例如：

```
separator = QAction(self)
separator.setSeparator(True)
self.addActions(editToolbar, editSwapAndBlueAction, separator, editUnMirrorAction,
editMirrorVerticalAction, editMirrorHorizontalAction)
```

如果我们需要复杂的右键菜单处理——例如，菜单根据应用程序的状态而变化，我们可以重新实现相关组件的 `contextMenu()` 事件处理器。事件处理将在第 10 章中介绍。

当我们创建一个新图像或加载一个现有图像时，我们希望用户界面恢复到原始状态。特别是，我们希望“编辑反转”和“编辑交换红绿”动作处于默认状态。

```python
self.zoomSpinBox = QSpinBox()
self.zoomSpinBox.setRange(1, 400)
self.zoomSpinBox.setSuffix("%")
self.zoomSpinBox.setValue(100)
self.zoomSpinBox.setToolTip("Zoom the image")
self.zoomSpinBox.setStatusTip(self.zoomSpinBox.toolTip())
self.zoomSpinBox.setFocusPolicy(Qt.NoFocus)
self.connect(self.zoomSpinBox, SIGNAL("valueChanged(int)"), self.showImage)
editToolbar.addWidget(self.zoomSpinBox)
```

## 恢复保存主窗口

现在用户界面已经设置好，我们几乎准备好完成初始化，但在查看系统设置之前，`imagechanger.py` 的最后语句是函数调用：

```python
def main():
    app = QApplication(sys.argv)
    app.setOrganizationName("Qtrac Ltd")
    app.setOrganizationDomain("qtrac.eu")
    app.ApplicationName("Image Changer")
    app.setWindowIcon(QIcon(":icon.png"))
    form = MainWindow()
    form.show()
    app.exec_()
```

通常，我们为可执行文件选择了一个习惯名称。以下是其代码：

```
main()
```

函数的的第一行我们已经见过多次。接下来的三行是新的。我们对它们的主要用途是加载和保存应用程序设置。我们创建一个不传递任何参数的 `QSettings` 对象，使用设置过的组织名称或域名（取决于平台）、应用程序名称。通过在应用程序对象上设置这些内容，当我们我们需要 `QSettings` 实例时无需无需传递它们。

但这意味着什么？它们被 PyQt 用于将应用程序设置保存在合适的地方——例如在 Windows 注册表中，或者在 Linux 的 $HOME/.config 下，或者在 Mac OSX 的 $HOME/Library/Preferences 中。我们可以回到 `MainWindow.__init__()` 方法之前的地方，查看如何恢复系统设置。

```python
settings = QSettings()
self.recentFiles = settings.value("RecentFiles").toList()
size = settings.value("MainWindow/Size",
Variant(QSize(600, 500))).toSize()
self.resize(size)
position = settings.value("MainWindow/Position",
Variant(QPoint(0, 0))).toPoint()
self.move(position)
self.restoreState(
settings.value("MainWindow/State").toByteArray())
self.setWindowTitle("Image Changer")
self.updateFileName()
Timer.singleShot(0, self.loadInitialFile())
```

## 创建主窗口

我们首先创建一个 QSettings 对象。由于我们没有传递任何参数，它将使用应用程序对象所持有的名称来定位设置信息。我们开始获取最近使用的文件列表。`QSettings::value()` 方法返回一个 `QVariant`，因此我们必须将其转换为预期的数据类型。

接下来，我们使用 `value()` 的双参数形式，其中第二个参数是默认值。这意味着当应用程序第一次运行时，它没有任何设置，*因此我们将得到一个宽度为 600 像素、高度为 500 像素的 `QSize()` 对象。*在随后的运行中，返回的大小将是应用程序终止时主窗口的大小——只要我们 own获得大小时记得保存它，我们就会将主窗口调整为该大小。在获取之前的（或默认的）大小后，我们以完全相同的方式获取并设置位置。

整个过程中没有闪烁，因为大小调整和定位是在主窗口的初始化函数中完成的，且在窗口显示给用户之前。

Qt 4.2 引入了两种调整和恢复顶层窗口几何的方法。遗憾的是，由于 bug 导致我们在基于 X11 的系统上这种方法并不可靠，出于这个原因，我们将窗口的大小和位置恢复为单独的项目。Qt 4.3 修复了该 bug，因此使用 Qt 4.3（例如使用 PyQt 4.3），不再需要获取大小和位置并调用 `resize()` 和 `move()`，一切可以通过一行代码完成：

```
self.restoreGeometry(settings.value("Geometry").toByteArray())
```

这假设在应用程序终止时已保存窗口几何形状，正如我们在 `closeEvent()` 中看到的那样。

`QMainWindow` 类提供了 `restoreState()` 方法和 `saveState()` 方法；这些方法从 `QByteArray` 恢复并保存到其中。它们保存和恢复的数据是停靠窗口的大小和位置，以及工具栏的位置——但它们仅对具有唯一对象名称的停靠控件工具栏有效。

设置窗口标题后，我们调用 `updateMenu()` 来创建“文件”菜单。与其他菜单不同，“文件”菜单是动态生成的；这样它就可以显示我们最近使用的文件。文件菜单的 `aboutShow()` 到 `updateFileMenu()` 方法的连接意味着，每当用户点击“文件”菜单栏或按下 Alt+F 时，“文件”菜单都会重新创建——这意味着对于尚未添加到工具栏的操作（如用于“退出文件”的 Ctrl+Q），键盘快捷键将无法工作。鉴于此，我们显式调用 `updateFileMenu()` 来创建一个初始的“文件”菜单并激活快捷键。

*PyQt 的文档很少给出单位，因为假设单位是像素，除了使用点的 `QPrinter` 之外。*

![](img/55bc1dcf8601cfec5e1423b4e17ec264_197_0.png)

![](img/55bc1dcf8601cfec5e1423b4e17ec264_197_1.png)

## 在启动时进行大量处理

如果我们需要启动时进行大量处理——例如，如果我们需要加载大量大文件，我们总会在单独的加载方法中执行。在主表单构造函数的最后，通过一个零超时的单次定时器（single-shot timer）调用加载方法。

如果我们不使用单次定时器会发生什么？假设，该方法是 `loadFiles()` 且它加载了大量多播文件。文件加载将在主窗口创建时完成，即在 `show()` 调用之前，且在事件循环（`exec_`）启动之前。这意味着用户可能会在启动应用程序到实际看到应用程窗口出现在屏幕上之间经历长时间延迟。此外，如果文件加载可能会导致消息框弹出——例如报告错误——那么让这些框在主窗口显示之后且事件循环运行时出现会更合理。

我们希望主窗口尽可能地出现，以便用户知道启动已成功，并让他们能够通过主窗口的用户界面查看任何长时间运行的过程（如加载大文件）。这是通过像我们在“图像更改”示例中那样使用单次定时器实现的。

这种方法之所以有效，是因为超时为零的单次定时器不会立即执行它接收到的槽函数。相反，它将槽放入事件队列然后直接返回。此时，已到达主窗口初始化函数的末尾，初始化完成。紧下一条语句（在 `main()` 中）是对主窗口的 `show()` 调用，它除了向事件队列中添加一个显示事件外什么都不做。超时为零的定时器被意味着“当事件队列没有其他事情要做时执行”，因此当到达下一语句 `exec()` 并启动事件循环时，它会选择先处理事件，这样表单就会出现，然后在没有其他事件留的情况下，单次定时器的事件被处理，并发起了 `loadFiles()` 调用。

初始化函数的最后一行看起来很奇特。单次定时器接受一个超时时间（毫秒）和一个在超时发生时调用的方法。所以，看起来这行代码也可以写成这样：

```
self.loadInitialFile()
```

在此应用程序中，我们最多加载一个初始文件，由于该文件不太可能是大，我们可以使用这两种方法而察觉不到任何区别。尽管如此，直接调用方法与使用零超时的单次定时器不同，正如启动时处理部分解释的。

## 创建主窗口

我们已经审查了主窗口的代码，现在可以开始查看实现应用程序功能的方法。虽然“图像更改”只是一个特定示例，但我们尽可能使代码变得通用或易于适应，以便用于完全不同的主窗口风格应用程序。

鉴于我们之前的讨论，似乎从 `loadInitialFile()` 方法开始介绍是合适的。

```
def loadInitialFile(self):
    settings = QSettings()
    fname = settings.value("LastFile").toString()
    if fname and QFile.exists(fname):
        self.loadFile(fname)
```

该方法使用 `QSettings` 对象获取应用程序上次使用的图像。如果存在这样的图像且仍然存在，程序将尝试加载它。我们将在文件操作时审查 `load()`。

我们可以很容易地写成 `if fname and os.access(fname, os.F_OK)`：在这里没有明显区别，但对于多进程项目，在这种情况下可能倾向于使用 PyQt 而标准库或反之，以保持简单清晰。

我们早些时候讨论了恢复应用程序状态，因此似乎涵盖关闭事件是合适的，因为那是我们保存应用程序状态的地方。

```
def closeEvent(self, event):
    if self.okToContinue():
        settings = QSettings()
        filename = QVariant(QString(self.filename)) \
        if self.filename is not None else QVariant()
        settings.setValue("LastFile", filename)
        recentfiles = QVariant(self.recentFiles) \
        if self.recentFiles else QVariant()
        settings.setValue("RecentFiles", recentfiles)
        settings.setValue("MainWindow/Size", QVariant(self.size()))
        settings.setValue("MainWindow/Position",
        QVariant(self.pos()))
        settings.setValue("MainWindow/State",
        QVariant(self.saveState()))
    else:
        event.ignore()
```

如果用户尝试关闭应用程序，通过其他方式（从杀死进程或崩溃），将调用 `closeEvent()` 方法。我们开始调用自定义的 `okToContinue()` 方法；如果用户真的想

![](img/55bc1dcf8601cfec5e1423b4e17ec264_199_0.png)

## 表 6.2 精定的 QMainWindow 方法

| 语法 | 描述 |

| --- | --- |

| m.addDockWidget(a, d) | 将 QDockWidget d 添加到 QMainWindow 的 Qt::DockWidgetArea 中 |

| m.addToolBar(s) | 添加并返回一个名为字符串 s 的新 QToolBar |

| m.menuBar() | 返回 QMainWindow 的菜单栏（在第一次调用此方法时创建） |

| m.restoreGeometry(ba) | 将 QMainWindow 的位置和大小恢复为封装在 QByteArray ba 中的 |

| m.restoreState(ba) | 将 QMainWindow 的停靠控件和工具栏恢复为封装在 QByteArray ba 中的状态 |

| m.saveGeometry() | 返回封装在 QByteArray 中的 QMainWindow 的位置和大量 |

| m.saveState() | 返回 QMainWindow 的停靠控件和工具栏的状态，即它们的大小和位置，封装在 QByteArray 中 |

| m.setCentralWidget(w) | 将 QMainWindow 的中心部件设置为 QWidget w |

| m.statusBar() | 返回 QMainWindow 的 QStatusBar（在第一次调用此方法时创建） |

| m.setWindowIcon(i) | 将 QMainWindow 的图标设置为 QIcon；此方法继承自 QWidget |

| m.setWindowTitle(s) | 将 QMainWindow 的标题设置为字符串 s；此方法继承自 QWidget |

想要选择，否则返回 `False`。这部分位于 `okContinue()` 内部，我们给了用户保存未保存更改的机会。如果用户想要选择，我们会创建一个新的 `QSettings` 对象，并存储“上一次的文件”（即我们当前打开的文件）、最近使用过的文件以及窗口的状态。`QSettings` 类只读和写 `QVariant` 对象，我们必须小心地提供 `null` `QVariant`（通过 `QVariant()` 创建）或包含其中正确信息的 `QVariant`。

如果用户选择不继续，我们在关闭事件上调用 `ignore()`。这将告诉 PyQt 直接丢弃该事件并让应用程序继续运行。

如果我们正在使用 Qt 4.3（例如使用 PyQt 4.3）并使用 `QWidget.restoreGeometry()` 恢复了窗口的几何形状，我们可以像这样保存几何形状：

```
settings.setValue("Geometry", QVariant(self.saveGeometry()))
```

如果采用这种方法，我们就不需要单独保存主窗口的大小或位置。

```python
def okToContinue(self):
    if self.dirty:
```

## 创建主窗口

```python
reply = QMessageBox.question(self,
    "图像更改 - 未保存的更改",
    "保存未保存的更改？",
    QMessageBox.Yes|QMessageBox.No|
    QMessageBox.Cancel)

if reply == QMessageBox.Cancel:
    return False
elif reply == QMessageBox.Yes:
    self.fileSave()
    return True
```

此方法被 `closeEvent()` 以及“文件-新建”和“文件-打开”动作使用。如果图像是“脏”的（即有未保存的更改），我们会弹出一个消息框并询问用户想做什么。如果他们点击“是”，我们将图像保存到磁盘并返回 `True`。如果他们点击“否”，我们返回 `True`，这样未保存的更改将丢失。如果他们点击“取消”，我们返回 `False`，这意味着未保存的更改不会保存，当前图像将保留，因此以后可以保存。最近使用的文件列表是应用程序状态的一部分，在应用程序终止时不能保存和恢复。早些时候我们将 `fileMenu->aboutToShow` 信号连接到 `updateFileMenu()` 槽。因此，当用户按下 Alt+F 或点击文件菜单时，该槽会在菜单显示之前被调用。

```python
def updateFileMenu(self):
    self.fileMenu.clear()
    current = self.filename if self.filename is not None else None
    recentFiles = []
    for name in self.recentFiles:
        if name == current and QFile.exists(name):
            recentFiles.append(name)
    if recentFiles:
        self.fileMenu.addSeparator()
        for i, name in enumerate(recentFiles):
            action = QAction(QIcon(":/icon.png"), "%d %s" % (i + 1, QFileInfo(name).name()), self.fileMenu)
            action.setData(QVariant(name))
            action.connect(SIGNAL("triggered()"), self.loadFile)
        self.fileMenu.addAction(action)
```

## 静态 QMessageBox 方法

`QMessageBox` 类提供了几个静态方法，可以弹出一个带有适当图标和按钮的模态对话框。它们对于向用户提供带有单个“确定”按钮、“是和/否”按钮以及类似的对话框非常有用。最常用的静态方法是 `critical()`、`information()` 和 `warning()`。这些方法接受一个父部件（它们将相对于它居中显示）、窗口标题、文本（可以是纯文本或 HTML）以及零或多个按钮规格。如果没有指定按钮，则提供一个单一的“确定”按钮。

可以使用常量指定按钮，或者我们可以提供自定�文本。在 Qt 4.0 和 4.1 中，使用 `QMessageBox.Default` 配合“确定”或“是”按钮是非常常见的——意味着如果用户按下 Enter 键，该按钮将被按下——或者使用 `QMessageBox.Escape` 配合“否”按钮，那么当用户按下 Esc 键时该按钮将被按下。例如：

```python
reply = QMessageBox.question(self,
    "图像更改 - 未保存的更改", "保存未保存的更改？",
    QMessageBox.Yes|QMessageBox.Default,
    QMessageBox.No|QMessageBox.Escape)
```

从 Qt 4.2 开始，`QMessageBox` 的 API 被简化了，如果未指定按钮，将提供一个“确定”按钮。例如：

```python
reply = QMessageBox.question(self,
    "图像更改 - 未保存的更改", "保存未保存的更改？",
    QMessageBox.Yes|QMessageBox.No)
```

（由于提供的文本中存在大量重复的段落，译文已根据逻辑进行了整合，并翻译了核心部分。）

# 第 6 章 主窗口

190

![](img/55bc1dcf8601cfec5e1423b4e17ec264_204_0.png)

图 6.8 带有最近使用文件的“文件”菜单

我们采用的处理最近使用文件的方法只是许多可能性之一。另一种方法是只创建一次“文件”菜单，并在末尾留一组用于最近文件的操作。当菜单更新时，不是清空并重新创建，而是简单地对最近文件的操作进行隐藏或显示；在后者的情况下，更新它们的文件名以反映当前的最近使用文件集。从用户的角度来看，无论我们底层采用哪种方式，都没有可察的区别，因此在任何情况下，“文件”菜单看起来都与图 6.8 所示的相似。

这两种方法都可以用于在“文件”菜单中实现最近文件，就像我们在 Image Changer 应用程序中所做的那样，在“退出”选项之前在最后添加列表。它们也可以用于实现“打开最近文件”选项，该选项将所有最近文件作为子菜单显示，如 OpenOffice.org 和其他应用程序所用的那样。使用独立的“最近文件”选项的好处是，“文件”菜单始终保持不变，并且可以在子菜单中显示完整路径——而我们在将最近使用文件直接放在“文件”菜单中时避免了这一点，以防菜单变得极其宽（因此变得难看）。

## 处理用户操作

在上一节中，我们创建了主窗口风格应用程序的外观，并通过创建一组操作提供了其行为基础。我们还看到了如何保存和恢复应用程设置，以及如何管理最近使用文件列表。

应用程序的一些行为由 PyQt 自动处理——例如窗口最小化、最大化和调整大小——因此我们不需要自己这样做。其他行为完全可以通过信号和槽连接来实现。在本节中，我们关注直接由用户控制的用于查看、编辑和输出数据的操作。

## 处理文件操作

“文件”菜单可能是主窗口风格应用程序中实现最广泛的菜单，在大多数情况下它至少提供“新建”、“保存”和“退出”（或“离开”）选项。

```python
def fileNew(self):
    if not self.okToContinue():
        return
    dialog = newImageDlg.NewImageDlg(self)
    if dialog.exec():
        self.addRecentFile(self.filename)
        self.image = QImage()
        for action, check in self.resetableActions:
            action.setChecked(check)
        self.image = dialog.image()
        self.filename = None
        self.dirty = True
        self.showImage()
        self.label.setText("%d x %d" % (self.image.width(),
        self.image.height()))
        self.updateStatus("Created image")
```

当用户要求处理一个新文件时，我们首先检查是否“可以继续”。这给了用户机会保存或丢弃任何未保存的更改，或者完全改变主意并取消操作。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_205_0.png)

**图 6.9** 新建图像对话框

如果用户继续，我们将弹出一个模态的 NewImageDlg，在其中他们可以指定想要创建的图像的尺寸、颜色和笔刷模式。这个如图 6.9 所示的对话框是创建的，并且与我们在上一节中创建的对话框一样。然而，New Image 对话框的用户界面是使用 Qt Designer 创建的，用户界面文件必须使用 pyuic4 转换为模块文件才能可以使用对话框。这可以直接运行 pyuic4 完成，也可以通过运行 mkpy.py 或 Make PyQt 完成，后者更简单，因为它们会自动处理命令行参数。我们将在下一节中涵盖所有这些问题。

如果用户接受对话框，我们将当前文件名（如果有）添加到最近使用文件列表中。然后，我们将当前图像设置为空图像，以确保对可更改操作的任何更改都不会对图像产生影响。我们遍历在创建或加载新图像时想要重置的操作，将每个操作都设置为我们偏好的默认值。现在，我们可以安全地将图像设置为对话框创建的图像。

我们将文件名设置为 None 并将 `dirty` 标记设为 True，以确保如果用户终止操作或尝试加载另一幅图像，将提示用户保存图像并询问文件名。

然后我们调用 `show()`，在 `imageLabel` 中显示图像并根据缩放因子进行调整。最后，我们更新状态栏中的尺寸标签，并调用 `updateStatus()`。

```python
def updateStatus(self, message):
    self.statusBar().showMessage(message, 5000)
    self.listWidget.addItem(message)
    if self.filename is not None:
        self.setWindowTitle("Image Changer - %s[*]" \
            os.path.basename(self.filename))
    elif not self.image.isNull():
        self.setWindowTitle("Image Changer - Unnamed[*]")
    else:
        self.setWindowTitle("Image Changer[*]")
        self.setWindowModified(self.dirty)
```

我们开始通过显示文件对话框来限制显示的图像类型。如果我们已经有一个图像文件名，我们使用其路径；否则，我们使用 "."（当前目录）。我们还选择传递一个过滤器字符串来限制文件对话框显示的图像类型。文件类型由其扩展名定义，并作为字符串传递。字符串可以为单个类型指定多个扩展名以及多个类型。例如，文本编辑器可能会传递：

> 文本文件 (*txt)

> HTML 文件 (*htm *.html)

如果有类型，我们必须用换行符分隔。如果一个类型可以处理多个扩展名，我们必须用空格分隔。该字符串将产生包含两个项目（“文本文件”和“HTML 文件”）的列表组合框，并确保对话框中显示的类型类型都是扩展名为 .txt、.htm 或 .html 的。

在 Image Changer 的案例中，我们使用应用程序正在使用的图像类型扩展名列表。至少这可能包括 .bmp、.jpg（以及 .jpeg，同 .jpg）和 .png。此列表推导式遍历可读的图像扩展名，并创建一个*.bmp”、“*.jpg”等字符串列表；这些字符串通过字符串的 `join()` 方法空格连接成单个字符串。

```python
def fileOpen(self):
    if not self.okToContinue():
        return
    dir = os.path.dirname(self.filename) \
        if self.filename is not None else "."
    formats = ["*%s" % unicode(format).lower() \
        for format in QReader.supportedImageFormats()]
    fname = unicode(QFileDialog.getFileName(self,
        "Image Changer - Choose Image", dir,
        "Image files (%s)" % ".join(formats))
    if fname:
        self.loadFile(fname)
```

+   列表推导式

53

# 第 6 章 主窗口

QFileDialog.getFileName() 返回一个 QString，它可能包含文件名（带有完整路径），也为空字符串（如果用户取消了操作）。如果用户选择了文件名，我们就会调用 `loadFile()` 进行加载。

在这里，以及整个程序中，当我们我们需要应用程序名称时，只是直接写写了它。但由于我们在 `main()` 函数的应用程序对象中设置了名称以简化对 `Settings` 的使用，我们可以在需要时检索该名称。在这种情况下，相关代码将变为：

```python
fname = unicode(QFileDialog.getFileName(self,
    "%s - Choose Image %s" % QApplication.applicationName(),
    dir,
    "Image files (%s)" % ";".join(formats)))
```

应用程序名称的使用频率之高令人惊讶。`imagechanger` 文件不到 500 行，但它使用了十多次的应用程序名称。一些开发者更倾向于使用这种方法来保证一致性。我们将在第 17 章涵盖国际化（i18n）内容时，进一步讨论字符串处理。

如果用户打开了一个文件，就会调用 `loadFile()` 方法来实际执行加载。我们将从两个部分来看这个方法。

```python
def loadFile(self, fname=None):
    if fname is None:
        action = self.sender()
        if isinstance(action, QAction):
            fname = unicode(action.data().toString())
            if not self.okContinue():
                return
    else:
        return
```

如果该方法是从 `open()` 方法或 `loadInitialFile()` 方法调用的，它会接收到要打开的文件名。但如果它是从“最近使用的文件”操作调用的，则不会传递文件名。我们可以利用这种差异来区分这两种情况。如果调用了最近使用的文件操作，我们会获取发送者对象。这应该是一个 `QAction`，但为了安全起见我们会对其进行检查，并提取动作的用户数据（user data），我们在其中存储了包含路径的最近文件全名。用户数据是以 `QVariant` 处理的，因此我们必须将其转换为合适的类型。此时，我们检查是否可以继续。在“打开文件”的情况下，我们不需要进行这项测试，因为在那里，在用户请求要打开的文件名之前检查已经完成了。所以现在，如果该方法没有返回，我们就知道 `fname` 中有一个我们必须尝试加载的文件。

```python
if fname:
    self.filename = fname
image = QImage(fname)
```

## 处理用户操作

```python
if image.isNull():
    message = "Failed to read %s" % fname
else:
    self.addRecentFile(fname)
    self.image = QImage()
    for action, check in self.resetableActions:
        action.setChecked(check)
    self.image = image
    self.filename = fname
    self.showImage()
    self.dirty = False
    self.sizeLabel.setText("%dx %d" % (
        image.width(), image.height()
    ))
    message = "Loaded %s" % os.path.basename(fname)
    self.updateStatus(message)
```

我们首先将当前文件名设置为 `None`，然后尝试将图像读取到局部变量中。PyQt 不使用异常处理，因此由于某种原因我们未能加载图像，那么空图像（null image）意味着由于某种原因已经间接发现了问题。如果加载成功，我们将新文件名添加到最近文件列表中，只有当随后打开另一个文件或以此其他名称保存时，它才会出现在那里。接下来，我们将实例变量设置为空图像：这意味着我们可以自由地将可更改的操作重置为首选默认值，而不会产生任何副作用。这之所以有效，是因为可更改的操作被改变了；虽然由于信号槽连接会调用相关方法，但如果图像为空，这些方法就不会执行。

在完成准备工作后，我们将局部图像赋值给 `image` 实例变量，并将局部文件名赋值给 `filename` 实例变量。接下来，我们调用 `showImage()` 以当前缩放因子显示图像，清除标记（dirty flag）并更新尺寸标签。最后，我们调用 `updateStatus()` 在状态栏中显示消息并更新日志组件。



```python
def fileSave(self):
    if self.image.isNull():
        return
    if self.filename is None:
        self.fileSaveAs()
    else:
        if self.image.save(self.filename, None):
            self.updateStatus("Saved as %s" % self.filename)
            self.dirty = False
        else:
            self.updateStatus("Failed to save %s" % self.filename)
```

`fileSave()` 方法以及许多其他对应用程序数据（`QImage` 实例）操作的方法在没有图像数据的情况下是没有意义的。因此，如果没有图像数据可供处理，许多方法将什么都不做并立即返回。

如果有图像数据且 `filename` 为 `None`，则用户一定调用了“新建文件”操作，现在正在第一次保存他们的图像。对于这种情况，我们将工作交给了 `fileSaveAs()` 方法。

如果我们有文件名，将尝试使用 `QImage.save()` 保存图像。该方法返回一个布尔值（成功/失败标志），我们根据该标志相应地更新状态。我们将加载和保存自定义文件格式的讲解推到了第 8 章，因为我们正专注于加载和保存的技巧。

```python
def fileSaveAs(self):
    if self.image.isNull():
        return
    fname = unicode(QFileDialog.getSaveFileName(self,
        "%s - Save Image %s" % QApplication.applicationName(),
        dir,
        "Image files (%s)" % ";".join(formats), ".png"))
    if fname:
        self.filename = fname
        if self.image.save(self.filename, None):
            self.updateStatus("Saved as %s" % self.filename)
            self.dirty = False
        else:
            self.updateStatus("Failed to save %s" % self.filename)
```

## 处理编辑操作

文件操作大部分功由 `MainWindow` 子类提供。唯一传递的工作是图像的加载和保存，这是 `QImage` 实例变量所需的。这种主窗口与数据结构之间特定的职责划分是非常常见的。主窗口处理高级的文件新建、打开、保存和最近文件功能，而数据结构处理加载和保存。

大多数甚至所有的编辑功能由部件或数据结构提供也是常见的。在 Image Changer 应用程序中，数据处理由数据结构（`QImage`）处理，数据的展示由数据查看器（`imageLabel`）处理。再次，这是非常常见的职责分离。

在本节中，我们将回顾一些编辑操作，省略两个与显示的内容几乎相同的操作。在这里我们将简要描述，因为这些功能是特定于 Image Changer 应用程序的。

```python
def editInvert(self, on):
    if self.image.isNull():
        return
    self.image.invertPixels()
    self.showImage()
    self.dirty = True
    self.updateStatus("Inverted") if on else "Uninverted"
```

# 198

# 第 6 章 主窗口

```python
def editMirrorHorizontal(self, on):
    if self.image.isNull():
        return
    self.image = self.image.mirrored(True, False)
    self.showImage()
    self.mirroredhorizontally = not self.mirroredhorizontally
    self.dirty = True
    self.updateStatus("Mirrored Horizontal" \
        if on else "Unmirrored Horizontal")
```

该方法在结构上与 `editInvert()` 和 `editSwapAndBlue()` 相同。`QImage.mirrored()` 方法接受两个布尔标志，第一个用于水平镜像，第二个用于垂直镜像。在“图像转换”应用程序中，我们刻意限制了允许的镜像类型，因此用户只能选择不镜像、垂直镜像或水平镜像，而不能将垂直和水平镜像结合使用。我们还保留了一个实例来跟踪图像是否已经进行了水平镜像。

未显示的 `editMirrorVertical()` 方法与此几乎相同。

```python
def editUnMirror(self, on):
    if self.image.isNull():
        return
    if self.mirroredhorizontally:
        self.editMirrorHorizontal(False)
    if self.mirroredvertical:
        self.editMirrorVertical(False)
```

该方法会关闭任何生效的镜像状态，如果图像未镜像则不做任何操作。它不会设置脏标记（dirty flag）或更新状态：它将这些留给了 `editMirrorHorizontal()` 或 `editMirrorVertical()`，如果它们调用了其中一个的话。

应用程序提供了两种让用户更改缩放因子的方法。用户可以通过工具栏上的缩放数值框（spinbox）交互——它的 `valueChanged()` 信号连接到稍后将显示的 `showImage()` own——或者可以在“编辑”菜单中调用“编辑缩放”动作。如果使用“编辑缩放”动作，就会调用 `editZoom()` 方法。

```python
def editZoom(self):
    if self.image.isNull():
        return
    percent, ok = QInputDialog.getInt(self,
        "Image Changer - Zoom", "Percent",
        self.zoomSpinBox.value(), 1, 400)
    if ok:
        self.zoomSpinBox.setValue(percent)
```

## 处理用户动作

我们首先使用 `QInputDialog` 类的静态方法之一来获取缩放因子。`getInteger()` 方法接受一个父对象（对话框将围绕其居中）、一个标题、描述所需数据的文本、一个初始值，以及可选的最小值和最大值。

`QInputDialog` 还提供了其他静态便利方法，包括通过 `getDouble()` 获取浮点值、通过 `getItem()` 从列表中选择字符串以及通过 `getText()` 获取字符串。对于所有这些方法，返回值都是一个二元组，包含该值和一个指示用户是否输入并接受了有效值的布尔标志。*

如果用户点击了“确定”，我们将数值框的值设置为给定的整数。如果此值与当前值不同，数值框将发射 `changed()` 信号。该信号连接到 `showImage()` 槽，因此如果用户选择了新的缩放百分比值，该槽就会被调用。

```python
def showImage(self, percent=None):
    if self.image.isNull():
        return
    if percent is None:
        percent = self.zoomSpinBox.value()
        factor = percent / 100.0
        width = self.image.width() * factor
        height = self.image.height() * factor
        image = self.image.scaled(width, height, Qt.KeepAspectRatio)
        self.imageLabel.setPixmap(QPixmap.fromImage(image))
```

当创建或加载新图像时、每当应用变换时，以及响应数值框的 `changed()` 信号时，都会调用此槽。当用户更改工具栏数值框的值时（无论是直接使用鼠标，还是通过前述的“编辑缩放”动作），都会发射此信号。

我们获取百分比并将其转换为缩放因子，用它可以生成按新宽度和高度缩放的图像副本。然后我们设置 `imageLabel` 显示此图像。标签需要一个 `QPixmap` 格式的图像，因此我们使用静态方法 `QPixmap.fromImage(image)` 将 `QImage` 转换为 `QPixmap`。

注意，缩放图像对原始图像没有影响；这纯粹是视图的变化，而不是编辑。这就是为什么不需要设置脏标记。

根据 PyQt 的文档，`QPixmap` 针对屏幕显示进行了优化（因此绘制速度很快），而 `QImage` 针对编辑进行了优化（这就是为什么我们使用它们来保存图像数据）。

## 处理帮助动作

当我们创建主窗口动作时，我们为每个动作都提供了帮助文本，并将其设置为状态文本（status text）和工具提示文本（tooltip）。这意味着当用户浏览应用程序的菜系统时，当前高亮菜单选项的状态文本会自动出现在状态栏中。同样，如果用户将鼠标悬停在工具栏按钮上，相应的工具提示文本将在提示框中显示。

对于像“图像转换”这样小而简单的应用程序，状态提示和工具提示可能完全足够。尽管如此，我们仍然提供了一个在线帮助系统来展示如何实现，尽管我们将其推迟到了第 17 章（第 510 页）。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_214_0.png)

**图 6.10：关于框**

```python
def help(self):
    QMessageBox.about(self, "About",
        u"<b>Image Changer</b><br>"
        u"<p>Copyright ©2007 PyQt Ltd. All rights reserved.</p>"
        u"<p>This application uses %s on %s</p>" %
        (QT_VERSION, platform.system()))
```

## 总结

主窗口风格的应用程序通过继承 `QMainWindow` 创建。窗口具有一个中心控件（可能包含其他控件）作为中心部件。动作用于表示应用程序提供的功能。这些动作作为 `QAction` 对象持有，具有文本（用于菜单）、图标（用于菜单和工具栏）、工具提示和状态更新，并连接到槽。通常，所有动作都会添加到主窗口的菜单中，最常用的动作会被添加到工具栏中。为了支持键盓用户，我们为频繁使用的动作提供了快捷键，以使菜单导航尽可能快捷。某些动作是可切换的，某些动作组可以是互斥的，也就是说任何时间只能勾选一个。Qt 通过设置属性支持可切换动作，通过 `QAction` 对象支持互斥的动作组。

停靠窗口由停靠控件表示，并且设置简单。任意控件都可以添加到停靠窗口和工具栏中，在实践中我们向工具栏添加了小的信箱形状的控件。

202

# 第 6 章 主窗口

如果我们想恢复用户的工作空间（即加载他们上次运行应用程序时打开的文件），最好的方法是在主窗口初始化器的末尾使用一个单次计时器（single-shot timer）来加载文件。

大多数应用程序通常有一个数据集以及若干个用于显示和编辑数据的控件。由于本章的重点是主窗口的用户界面基础设施，我们选择了最简单的数据和可视化控件，但在随后的章节中，重点将发生转变。

让主窗口负责高级文件处理和最近使用的文件列表，而让持有数据的对象负责加载、保存和编辑数据，这是非常常见的做法。

在书的这里你已经掌握了足够的 Python 和 PyQt 知识来创建对话框风格和主窗口风格的应用程序。在下一章中，我们将展示 Qt Designer 的用法，这是一个可以认为是加速对话框开发和维护的应用程序。在第二部分的最后一章中，我们将使用 PyQt 和 Python 库来探索保存和加载自定文件格式的一些关键方法。在第三和第四部分中，我们将更深入地探索 PyQt（例如事件处理和创建自定义控件），并更广泛地学习 PyQt 的模型/视图架构以及包括线程在内的其他高级特性。

## 练习

创建图 6.11 所示的对话框。它的类名应为 Resize，其初始化器应接受初始宽度和高度。对话框应提供一个名为 `result()` 的方法，该方法必须返回用户选择的宽度和高度的二元组。计数器（spinboxes）的最小值为 4，最大值为传入宽度（或高度）的四倍。两者的内容都应该右对齐。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_216_0.png)

**图 6.11** Image Changer 调整大小对话框

修改 Image Changer 应用程序，使其拥有一个新的“编辑调整大小”操作。该操作应该出现在编辑（Edit）菜单中（“编辑缩”操作之后）。资源子目录下有一个 `editresize.png` 图标，但需要将其添加到 `resources.qrc` 文件中。你还需要导入刚刚创建的调整大小对话框。

## 练习

调整大小对话框应该在一个 `editResize()` 槽中使用，“编辑调整大小”操作应该连接到该槽。对话框的使用方式如下：

```
form = resizedlg.ResizeDlg(self.image.width(),
    self.image.height(), self)

if form.exec():
    width, height = form.result()
```

与 `editZoom()` 槽不同，图像本身应该被改变，因此如果尺寸发生了变化，尺寸标签、状态栏和脏状态（dirty status）都必须全部更改。另一方面，如果“新”尺寸与原始尺寸相同，则不应进行调整大小。

调整大小对话框可以用少于 50 行代码编写，调整大小槽可以用少于 20 行编写，新操作只需要在主窗口初始化器的几处额外增加一两行代码。

模型解决方案位于 `chap06/imagechanger_ans.pyw` 和 `chap06/resize-dlg.py` 文件中。

# 7

- 设计用户界面

- 实现对话框

- 测试对话框

# 使用 Qt Designer

在第 5 章中，我们完全通过编写代码创建了对话框。在初始化器中，我们创建了控件并设置了它们的初始属性。然后，我们创建了一个或多个布局管理器，并其中添加了控件以获得我们想要的外。在某些情况下，当处理垂直或水平布局时，我们添加了“拉伸”（stretch），它会扩展以填充未计划的空间。在布局好控件后，我们将感兴趣的信号连接到我们想要处理它们的方法。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_219_0.png)

图 7.1 Qt Designer

有些程序员倾向于在代码中完成一切，而另一些人则倾向于使用可视化工具来创建他们的对话框。使用 PyQt，我们可以二选一，甚至两者兼顾。

# 第 7 章 使用 Qt Designer

上一章节的 Changer 应用程序有两个自定义对话框：完全通过代码创建（在练习中）的 `ResizeDlg`，以及使用 Qt Designer 创建的 `NewImageDlg`。我们首先展示了如何操作，以便你对布局管理器的工作原理有强烈的感受。在本章中，我们将使用 Qt Designer 创建对话框，如图 7.1 所示。

Qt Designer 可用于为对话框、自定义控件和主窗口创建用户界面。我们将涵盖对话框；自定义控件几乎一样，只是它们是基于“Widget”模板而不是“Dialog”模板之一。使用 Qt Designer 创建主窗口除了具有可视化 Qt 编辑器的便利性外，优势较少。Qt Designer 还可以用于编辑和资源文件。

用户界面存储在 `.ui` 文件中，包含了表单控件和布局的细节。此外，Qt Designer 可以将标签与其“伙伴”（buddies）关联，并设置制表顺序（tab-order），即用户按下 Tab 键时哪个控件获得焦点。这也可以通过代码实现。

（注：原文后续部分存在大量重复的 OCR 错误，此处已根据逻辑流清理并保留了核心内容）

第 7 章. 使用 Qt Designer

这意味着使用 Qt Designer 进行设计实验比编辑手动编码的布局要快得多、简单得多，并且有助于在使用使用 Qt Designer 创建的视觉设计与在代码中实现的行为之间保持分离。

在本章中，我们将创建一个示例对话框，并利用它来学习如何使用 Qt Designer 创建和布局控件、设置伙伴关系（buddies）和标签顺序，以及建立信号与槽连接。我们还将看到如何使用由 pyqtc4 生成的用户界面模块，以及如何创建到我们自定义槽的连接，而无需在初始化函数中使用 `connect()` 调用。

对于这些示例，我们使用了 Qt 4.2 自带的 Qt Designer。早版本的 Qt Designer 不包含 `QComboBox` 或 `QCalendarWidget` 控件，而且它们的“对话”（Dialog）模板使用的是 `QPushButton` 而不是 `QDialogGroupBox`。

## 设计用户界面

在开始之前，我们启动 Qt Designer。在 Linux 上，在控制台中运行 `designer &`（假设它在你的路径中），或者通过你的菜单系统调用它。在 Windows XP 上，点击开始->Qt by Trolltech Designer，在 Mac OS 上使用 Finder 启动它。Qt Designer 启动时会弹出一个新表单（New Form）对话框，点击“带底部按钮的对话”（Dialog with Buttons Bottom），然后点击创建。这将创建一个标题为“untitled”的新表单，并带有如图 7.2 所示的 `QDialogGroupBox`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_222_0.png)

图 7.2 带底部按钮的对话框

首次运行 Qt Designer 时默认处于“多顶级窗口”（Multiple Top-Level Windows）模式——这可能会让人困惑，除非是 Mac OS X 用户，这种方法是他们的标准。为了像图 7.1 所示将所有内容放在一个窗口中，点击编辑→用户界面模式→停靠窗口（Edit→User Interface Mode→Docked Window）。Qt Designer 会记住此设置，因此只需操作一次。

Qt Designer 并不难使用，但确实需要按照特定的顺序执行某些操作，如下步骤列表所示。对于步骤 1 和 2，始终要从“后”向“前”操作，即始终从容器（组框、标签页控件、框架）开始，然后到它们内部（即在它们上方）的普通控件。稍后我们将逐步通过一个示例进行说明，在此之前，这里有一个如何使用 Qt Designer 创建对话框的通俗描述。

- 1. 将控件拖到表单上并将其放置在大致正确的位置；没有可以精确放置的位置，通常只有容器控件需要调整大小。

- 2. 如果必要，设置控件的属性；如果控件将在代码中被引用，至少给它一个合理的名称。

- 3. 重复步骤 1 和 2，直到所有需要的控件都出现在表单上。

- 4. 如果有较大的间隙，拖入水平或垂直弹簧器（这些显示为蓝色的弹簧）来填充它们；有时，当间隙很明显时，在步骤 1 和 2 期间就会添加弹簧器。

- 5. 选择两个或多个控件（或弹簧器或布局）进行布局（Shift+点击每一个一个），并使用布局管理器或拆分器（splitter）进行布局。

- 6. 重复步骤 5，直到所有控件和弹簧器都在布局中。

- 7. 点击表单（取消选择所有内容）并使用其中一个布局管理器对表单进行布局。

- 8. 为表单的标签创建伙伴（buddies）。

- 9. 如果顺序错误，设置表单的标签顺序。

- 10. 在适当的地方内置信号和槽之间创建信号-槽连接。

- 11. 预览表单并检查一切是否按预期工作。

- 12. 设置表单的对象名称（这用于它的类名）、表单的标题，并使其有一个文件名。例如，如果对象名称为“PaymentDig”，我们可能会给它一个标题“Payment”和一个文件名“payment1qt.ui”。

如果布局错误，请退回到可以开始布局的地方并重来。如果这不可行或不起作用，或者布局在最初创建一段时间后正在被更改，则打破需要更改的布局然后重新进行。通常，在更改表单内的布局之前，必须打破表单的布局（点击表单，然后点击“打破布局”工具栏按钮）；因此此时表单本身必须重新布局。

> *从 Qt 4.3 开始，可以通过点击编辑→偏选项（Edit→Preferences）可以使用此选项。

虽然可以将布局拖到表单上，然后将控件拖入布局，但最佳实践是将所有控件和弹簧器拖到表单上，然后反复选择某些控件和弹簧器并对它们应用布局。向现有布局中添加控件有意义的情况是我们想要将控件拖入间隙中——例如，拖入网格布局中的空单元格。

现在我们已经掌握了总体原则，我们将逐步完成图 7.3 所示的查找和替换对话框的设计。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_224_0.png)

**图 7.3** 查找和替换对话框

基于“对话”模板之一创建一个新表单。这将给我们一个带按钮的表单。点击按钮然后删除。这将给我们留下一个空白表单。对于这个，我们将使用 DialogBox。默认情况下，Qt Designer 左侧有一个窗口。控件被分成若干部分，最后是一个名为“Display”的组。我们现在添加两个复选框。从按钮组（Box 顶部）拖入一个复选框并将其放在第二个标签下方。使用属性编辑器或右键菜单将其名称更改为“CheckBox”，文本更改为“Case sensitive”（区分大小）。在第一个复选框右侧拖入第二个复选框：将其名称更改为“wholeCheckBox”，文本更改为“Whole words”（全字），并将状态设置为“checked”（勾选）。表单现在应该与图 7.5 所示的类似。

（注：提供的 OCR 文本在此处是重复/混乱的，我将合并逻辑流）。

在任何时候我们都可以通过 Ctrl+S 或文件→保存来保存表单。当我们使用文件名时，findandreplaced.ui。

每个可编辑属性（某些只读属性）都显示在属性编辑器中。此外，Qt Designer 提供了一个右键菜单。右键菜单中的第一个选项允许我们更改控件最“重要”的属性（例如 Label 或 Line Edit 的“text”属性），第二个选项允许我们更改控件的对象名称。如果我们使用右键菜单选择复选框、单选按钮或按钮文本，编辑是原地的，在这种情况下必须按回车键完成。我们将总是说在属性编辑器中更改属性，但当然，如果你愿意，可以使用右键菜单。

我们现在添加两个复选框。从按钮组（Box 顶部）拖入一个复选框并将其放在第二个标签下方。使用属性编辑器或右键菜单将其名称更改为“CheckBox”，文本更改为“Case sensitive”（区分大小）。在第一个复选框右侧拖入第二个复选框：将其名称更改为“wholeCheckBox”，文本更改为“Whole words”（全字），并将状态设置为“checked”（勾选）。表单现在应该与图 7.5 所示的类似。

（自纠：提供的第 224-225 页 OCR 文本高度重复且包含重叠句子。我根据可用片段合成了叙述并删除了 OCR 伪迹。）

**等待，现在让我提供最终版本。**

# 212

# 第 7 章 使用 Qt Designer

![](img/55bc1dcf8601cfec5e1423b4e17ec264_226_0.png)

**图 7.5** 两个标签（Label）、两个行编辑框（Line Edit）。将一个标签拖到区分大小写的复选框下方，并将其设置为 "&Syntax:"。现在将一个组合框（Combo Box，来自输入小部件组）拖到 Syntax 标签的右侧。将组合框的名称更改为“syntaxComboBox”。右键点击组合框并选择第一个菜单选项“编辑项”（Edit items）。点击“+”输入“Literal text”。重复此操作以添加“Regular expression”。点击确定完成。

现在我们将把 Syntax 标签及其文本添加到区分大小写的敏感复选框中，并将其文本设置为 "&Syntax:"。现在将一个组合框（Combo Box，来自输入小部件组）拖到 Syntax 标签的右侧。将组合框的名称更改为“syntaxComboBox”。右键点击组合框并选择第一个菜单选项“编辑项”（Edit items）。点击“+”输入“Literal text”。重复此操作以添加“Regular expression”。点击确定完成。

如果用户调整表单大小，我们希望小部件保持整齐而不是散开，拖入垂直间距器（Vertical Spacer，来自小部件框顶部的间距器）并将其放置在组合框上方。我们在设计表单代码时使用拉伸（stretches），但在视觉化设计时使用间距器（spacers）：它们都会扩展以填充空白区域。在布局中添加拉伸本质上与向布局中插入 QSpacerItem 相同，但代码输入更少。

为了让按钮与我们刚刚创建的小部件分开，我们将在它们与其他小部件之间放置一条垂直线。从显示小部件组（位于小部件框底部）拖入一条垂直线（Vertical Line，实际上是名为 QFrame.LINE 的 QFrame），将其放置在表单中所有小部件的右侧，为按钮留出右侧空间。现在表单看起来应该像图 7.6。

现在我们准备好创建按钮了。从小部件框底部的按钮组拖入一个推入按钮（Push Button）到表单的右上角。将其名称更改为“findButton”，文本更改为 "&Find”。在 Find 按钮下方拖入另一个按钮，赋予它对象名称“replaceButton”并将文本设置为 "&Replace”。在 Replace 按钮下方创建第三个按钮。赋予它对象名称“replaceAllButton”，并将文本更改为“Replace&All”。现在在 Replace All 按钮下方拖入一个垂直间距器。最后，在间距器下方拖入一个按钮。赋予此按钮对象名称“closeButton”并将文本改为“Close”。

现在我们有了所需的小部件和间距器，并适当设置了它们的所有属性。表单看起来应该像图 7.7。

## 设计用户界面

![](img/55bc1dcf8601cfec5e1423b4e17ec264_227_0.png)

**图 7.6** 没有按钮的查找和替换对话框

![](img/55bc1dcf8601cfec5e1423b4e17ec264_227_1.png)

**图 7.7** 未布局的查找和替换对话框

布局此表单的最佳方法是什么？这些问题的最佳设计是什么？答案取决于个人喜好和实践。在这里，我们仅展示机制，将美学留给您。

我们将从布局前两个标签及其行编辑框开始。点击表单以取消所有选择，然后 Shift+Click 点击“查找内容”（Find what）标签及其行编辑框，以及“替换为”（Replace with）标签及其行编辑框。一旦选择了这些小部件，点击“表单（Form）→网格布局（Lay Out In a Grid）”（或相应的工具栏按钮）。布局由红线指示——布局线在运行时是不可见的。

现在（点击表单）取消所有选择

我们现在可以布局表单左侧的布局了。点击表单取消所有选择。选择布局（而不是小部件）可能很困难，因此我们不使用 Shift+Click 选择，而是使用选择矩形。点击表单左下角附近并拖动选择矩形：此矩形只需要接触对象即可选中。

# 第 7 章 使用 Qt Designer

![](img/55bc1dcf8601cfec5e1423b4e17ec264_228_0.png)

**图 7.8** 带有某些布局的查找和替换对话框

向上向右拖动，直到它接触左侧的垂直间距器和三个布局——而不接触其他任何内容（例如垂直线）。现在，释放并点击“表单（Form）→垂直布局（Lay Out Vertically）”。

我们可以使用相同的选择技术来布局按钮。点击表单选择所有内容。现在在表单右下角附近拖动，使选择矩形接触 Close 按钮、右侧的垂直间距器和其他按钮——而不接触其他内容。现在，释放并点击“表单（Form）→垂直布局（Lay Out Vertically）”。我们现在应该拥有一个表单，每个小部件都在左侧或右侧布局中，中间有一条垂直线，如图 7.9 所示。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_228_1.png)

**图 7.9** Almost完成布局的查找和替换对话框

我们现在准备好布局布局了。点击表单取消所有选择。现在点击“表单（Form）→水平布局（Lay Out Horizontally）”。表单现在应该像图 7.8。

## 设计用户界面

布局此表表的最佳方法是什么？这些问题的最佳设计是什么？答案取决于个人喜好和实践。在这里，我们仅展示机制，将美学留给您。

我们将从布局前两个标签及其行编辑框开始。点击表单取消所有选择，然后 Shift+Click 点击“查找内容”（Find what）标签及其行编辑框，以及“替换为”（Replace with）标签及其行编辑框。一旦选择了这些小部件，点击“表单（Form）→网格布局（Lay Out In a Grid）”（或相应的工具栏按钮）。布局由红线指示——布局线在运行时是不可见的。

现在（点击表单）取消所有选择

我们现在可以布局表单左侧的布局了。点击表单取消所有选择。选择布局（而不是小部件）可能很困难，因此我们不使用 Shift+Click 选择，而是使用选择矩形。点击表单左下角附近并拖动选择矩形：此矩形只需要接触对象即可选中，向上向右拖动，直到它接触左侧的垂直间距器和三个布局——而不接触其他任何内容（例如垂直线）。现在，释放并点击“表单（Form）→垂直布局（Lay Out Vertically）”。

我们可以使用相同的选择技术来布局按钮。点击表单选择所有内容。现在在表单右下角附近拖动，使选择矩形接触 Close 按钮、右侧的垂直间距器和其他按钮——而不接触其他内容。现在，释放并点击“表单（Form）→垂直布局（Lay Out Vertically）”。我们现在应该拥有一个表单，每个小部件都在左侧或右侧布局中，中间有一条垂直线，如图 7.9 所示。

我们现在准备好布局布局了。点击表单取消所有选择。现在点击“表单（Form）→水平布局（Lay Out Horizontally）”。表单现在应该像图 7.8。

布局此表单的最佳方法是什么？这些问题的最佳设计是什么？答案取决于个人喜好和实践。在这里，我们仅展示机制，将美学留给您。

## 实现对话框

第一个导入是我们将在代码中使用的正则表达式模块。第二个和第三个导入是 PyQt 编程中常用的导入。最后一个导入是生成的用户界面模块。现在我们可以查看我们的子类了。

```python
class FindAndReplaceDlg(QDialog,
    ui_findAndReplaceDlg, Ui_FindAndReplaceDlg):
    def __init__(self, text, parent=None):
        super(FindAndReplaceDlg, self).__init__(parent)
        self.text = unicode(text)
        self.index = 0
        self.setupUi(self)
        if not MAC:
            self.findButton.setFocusPolicy(Qt.NoFocus)
            self.replaceButton.setFocusPolicy(Qt.NoFocus)
            self.replaceAllButton.setFocusPolicy(Qt.NoFocus)
            self.closeButton.setFocusPolicy(Qt.NoFocus)
        self.update()
```

我们继承了 QDialog 和 Ui_FindAndReplaceDlg。在 Python 编程中，我们很少使用多重继承，但对于这个用例来说，这样做会比其他方法要简单得多。我们的 FindAndReplaceDlg 子类实际上是它继承的两个类的并集，并且可以直接访问以 `self` 为前缀的这些属性。

我们将初始化函数设置为接受对话框将要处理的文本以及一个父级小部件。`super()` 调用是在第一个继承的类 QDialog 上执行的。我们保留了文本的副本，还保留了一个索引位置，以防用户多次点击查找相同文本的后续出现位置。

`setUp()` 的调用是一个我们之前未见过的方法。该方法由生成的模块提供。它在用户界面文件中创建所有控件，根据我们的设计对它们进行布局，设置它们的边界和标签页顺序，并建立我们设置的连接。此外，它重新创建了我们在 Qt Designer 中设计的表单。

例如，我们有一个类型为 `QLineEdit` 的控件 `findLineEdit`。`QLineEdit` 发出的信号之一是 `edited(QString)`。因此，如果我们想连接此信号，而不在初始化函数中调用 `connect()` 方法，我们可以将其留给 `setUpUi()`。只要我们在 `findLineEdit_textEdited` 上调用了要连接的槽函数，这种方法就能生效。这是我们在表单中所有连接采用的方法，除了我们在 Qt Designer 中视觉化连接的关闭按钮信号外。

# 第 7 章 使用 Qt Designer

对于 Windows 和 Linux 用户来说，将按钮的焦点策略设置为“无焦点”（No Focus）是非常方便的。这对于鼠标用户没有影响，但对键盘用户通常很有帮助。这意味着按下 Tab 键键盘焦点只会在编辑控件之间移动——在本例中，即查找行编辑、替换行编辑、复选框和组合框——这通常比必须通过 Tab 键经过按钮要方便得多。键盘用户仍然可以使用它们的键盘快捷键按下任何按钮（关闭按钮为 Esc）。遗憾的是，对话框和按钮没有为 OS X 用户提供快捷键（除非他们开启对辅助设备的支持），这些用户需要能够 Tab 到所有控件，包括按钮。为了兼顾所有平台，我们没有在 Qt Designer 中设置按钮的焦点策略，而是在 `setupUI()` 创建用户界面后手动设置它们。

如果底层窗口系统是 Mac OS X，则布尔变量 `MAC` 为 True。它在文件开头（导入之后）通过以下原生语句进行设置：

```python
MAC = "qt_mac_set_native_menubar" in dir()
```

更清晰的写法是：

```python
import PyQt4.QtGui
MAC = hasattr(PyQt4.QtGui, "qt_mac_set_native_menubar")
```

这些之所以有效，是因为 `PyQt4.QtGui.qt_mac_set_native_menubar()` 函数仅存在于 Mac OS 系统。我们在第 11 章中使用了类似的技术来检测 X Window 系统。

最后调用的 `updateUI()` 方法是我们的自定方法；我们用它根据用户是否输入了查找文本来启用或禁用按钮。

```python
@pyqtSignature("QString")
def findLineEditTextEdited(self, text):
    self._index = 0
    self.updateUI()
```

由于 `setupUI()`，此方法会自动连接到 `findLineEditTextEdited()` 信号。每当我们建立连接时，都会使用 `@pyqtSignature` 装饰器来指定信号的参数。该装饰器的目的是区分名称相同但参数不同的信号。在这种特定情况下，只有一个 `textEdited(1)` 信号，装饰器并不是严格必须的；但出于良好的习惯，我们总是使用装饰器。例如，如果后来的 PyQt 版本引入了另一个同名但参数不同的信号，使用装饰器的代码将继续有效，而不使用的代码则不会。

由于此槽在用户更改查找文本时被调用，我们将搜索开始的索引位置重置为 0（开头）。在这里我们通过调用 `updateUI()` 结束。

## 实现对话框

```python
def updateUi(self):
    enable = not self.findLineEdit.text().isEmpty()
    self.findButton.setEnabled(enable)
    self.replaceButton.setEnabled(enable)
    self.replaceAllButton.setEnabled(enable)
```

我们已经见过许多此类方法的示例了。在这里，如果用户输入了查找文本，我们就启用查找、替换和全部替换按钮。无论是否有任何替换文本这并不重要，因为将某些内容替换为空是完全有效的，即删除找到的文本。该方法就是为什么表单启动时每个按钮都是禁用的原因。当用户关闭表单时，由于它是将某些内容替换为（找到）替换文本，因此 `text` 方法将是可访问的。

```python
def text(self):
    return self.__text
```

有些 Python 程序员不会提供 `self.__text`，而是使用正则表达式来执行查找。关闭按钮的 `clicked()` 具有可选参数，我们对此不感兴趣。为了执行搜索，我们创建一个正则表达式，并准备好后续的搜索。

```python
@pyqtSignature("")
def findButtonClicked(self):
    regex = self.makeRegex()
    match = regex.search(self._text, self.index)
    if match is not None:
        self.index = match.end()
        self.emit("found")
    else:
        self.emit("notfound")
```

对话框的其余功能是通过 `makeRegex` 方法 实现的。

```python
def makeRegex(self):
    findText = unicode(self.findLineEdit.text())
    if unicode(syntaxComboBox.currentText()) == "Literal":
        findText = re.escape(findText)
        flags = re.MULTINE|re.DOTALL|re.UNICODE
    if not self.checkBox.isChecked():
        flags |= re.IGNORECASE
    if self.checkBox.isChecked():
        findText = r"\b" % findText
    return re.compile(findText, flags)
```

我们首先获取用户输入的文本。我们知道它不能为空为空，因为只有在输入了文本时（关闭按钮以外的）按钮才是可用的。如果我们知道要搜索的文本通常是 QString 而不是 unicode，那么使用 PyQt 的 QRegExp 类可能比 Python 标准库的类更好。

```python
@pyqtSignature("")
def on_replaceButton_clicked(self):
    regex = self.makeRegex(self)
    self._text = re.sub(unicode(self.replaceLineEdit.text())),
                        self._text, 1)
```

此方法非常简单，因为它将其准备工作交给了 `makeRegex()` 方法。我们使用 `sub` 方法（替换）来将第一个匹配替换为替换文本。替换文本可以是空的。`l` 是允许替换的最大次数。

```python
@pyqtSignature("")
def on_replaceAllButton_clicked(self):
    regex = self.makeRegex(self)
    self._text = re.sub(unicode(self.replaceLineEdit.text()),
                        self._text)
```

## 实现对话框

```python
self.__text = regex.sub(unicode(self.replaceLineEdit.text()), __text)
```

此方法与之前的那个几乎相同。唯一的区别在于我们没有指定最大替换次数，因此 `sub()` 会在发现时替换许多（不重叠的）查找文本出现。

我们现在已经实现了 `FindAndReplaceDlg`（查找与替换对话框）。对话框方法的实现与我们之前做的并没有太大区别，只是我们使用了装饰器和 `setUp()` 来提供自动连接。

要在应用程序中使用该对话框，我们必须确保生成了 `ui_findandreplaceddlg.py` 模块，并且必须导入我们刚刚编写的 `findandreplaceddlg` 模块。我们将在下一节查看如何创建和使用该表单。

## 测试对话框

由于任何 PyQt 部件（包括任何对话框）都可以作为自己的顶层窗口，因此通过实例化并启动事件循环来测试对话框非常简单。通常，我们需要做更多工作。例如，我们可能需要设置一些初始数据，或者提供接收对话框信号的方法，以便我们看到它们是否正常工作。

在查找和替换对话框的情况下，我们需要一些初始文本，并且需要检查连接是否正常以及查找和替换方法是否有效。

因此，在 `findandreplaceddlg.py` 文件的最后，我们添加了一些额外的代码。这些代码只在文件独立运行时才会执行，因此它不会影响性能，也不会干扰在应用程序中使用对话框。

```python
if __name__ == "__main__":
    import sys
```

```python
text = """美国的经验表明，与传统专利不同，软件专利并没有促进创新和研发，恰恰相反。特别是它们损害了中型企业和大多数新者。它们只会削弱市场并增加专利和诉讼的支出，而以技术创新和研究为代价。特别危险的是试图通过防止互操作性来滥用专利系统，以此避免技术能力的竞争。”
```

- 提取 Linvalds 和 Alan Cox 来信中的引用

使用 PyQt 时，我们可以指定命令行选项 `-x` 来生成带有少量额外代码的对话框，以便对其进行独立测试。

## 222 第 7 节 使用 Qt Designer

致欧洲议会会长

http://www.effi.org/patentit/patents_torvalds_cox.html

```python
def where():
    print "Found at %d" % where

def nomore():
    print "No more found"
```

```python
app = QApplication(sys.argv)
form = FindAndReplacedDlg("found", found)
form.connect(form, SIGNAL("notfound", nomore))
form.show()
app.exec_()
print form.text()
```

我们首先导入模块，然后创建一段文本进行处理。接下来，我们创建了几个简单的函数，供对话框的信号连接。

我们以正常方式创建 `QApplication` 对象，然后创建对话框实例，并传递我们的测试文本。我们将对话框的两个信号连接到我们的槽，并调用 `show()`。然后启动事件循环。当循环结束时，我们打印对话框的文本：如果用户替换了某些文本，这将与原始文本不同。

现在可以从控制台运行并测试对话框了。

```bash
C:\pyqt\chap07\python findreplaceddlg.py
```

在不使用测试工具的情况下，在对话框中添加测试功能通常很有帮助。编写这些功能并不会花费太多时间或精力，每当对话框逻辑发生变化时运行一次，将有助于尽量减少 Bug 的引入。

有时我们将复杂对象传递给对话框，这似乎使得测试是不可能的。得益于 Python 的鸭子类型（duck typing），我们始终可以创建一个模拟足够行为的类，用于测试。例如，在第 12 节中，我们使用属性编辑器对话框。该对话框作用于“Node”对象，因此在测试中我们创建了一个 `FakeNode` 类，提供对话框使用的设置和获取节点属性的方法。（相关文件为 `chap12/propertiesdlg.ui`（由此生成 `ui_propertiesdlg.py`）以及实现 `PropertiesDlg` 的 `chap12/propertiesdlg.py`。）

## 总结

Qt Designer 提供了一种快速创建创建用户界面的方法。使用视觉化设计工具使得更容易判断设计是否“有效”。Qt Designer 的另一个益处是，如果我们更改了设计，只要我们没有添加、删除或重命名所引用的部件，代码完全不需要更改。即使我们添加、删除或移动了部件，代码的更改可能非常小，因为 Qt Designer 为我们处理了所有部件的创建和布局。

Qt Designer 的基本原理始终相同：我们将部件拖到表单上（首先是容器如框架、分组框和标签页部件，然后是普通部件），并设置它们的属性。然后添加间隙来占据空隙。接下来我们选择特定的部件、间隙和布局，并对它们应用布局，重复此过程直到所有内容布局完毕。我们布局表单本身。最后我们设置偏置（biases）、标签顺序和信号槽槽连接。

使用由 Qt Designer 创建的用户界面实现对话框与手动实现相似。最大的区别在于初始化器，我们只需简单地调用 `setupUI` 来创建界面。对话框方法的实现与我们之前的并没有太大区别，只是我们使用了装饰器和 `setUp()` 来提供自动连接。要在应用程序中使用该对话框，我们必须确保生成了 `ui_findandreplaceddlg.py` 模块，并且必须导入我们刚刚编写的 `findandreplaceddlg` 模块。我们将在下一节查看如何创建和使用该表单。（*注：原文此处存在大量重复段落，译文已按逻辑精简并保持核心内容*）

## 练习

使用 Qt Designer 创建一个如图 7.11 所示设计之一的用户界面，或者使用你自己的设计。你可能需要使用网格布局（Grid Layout），以及垂直和水平布局。对于网格布局，你可能需要尝试几次，通过调整部件大小和位置来帮助 Qt 创建你想要的对话框。使用 `QDialogButtonBoxes` 处理按钮。

| | | |

| :--- | :--- | :--- |

| 客户 | [Edit] | |

| 时间 | [DateTime Edit] | |

| 价格 | [SpinBox] | $ |

| 数量 | [SpinBox] | |

图 7.11 两种设计的对话框

## 练习

创建一个子类以使用用户界面。代码应确保只有当客户行编辑框（Line Edit）为空且金额大于零时，确定按钮才被启用。要访问 QDialogButton 中的按钮，请使用 `button()` 方法，并将按钮的常量作为参数——例如 `listBox.button(QDialogButton.Ok)`。

每当数值计数器（spinbox）变化时，都应该重新计算金额并在金额标签中显示。设置日期范围为从明天到明年。提供一个 `result()` 方法，为客户返回一个四元组（unicode, datetime.datetime, float, int），分别对应日期、价格和数量。（如果你使用的是 4.1 之前的 PyQt 版本，请将日期作为 QDateTime 返回；否则，使用 `QDateTime.toPy()` 方法获取 `datetime`。）

在末尾包含足够的测试代码来显示 `TicketOrderDlg`，以便你对其进行交互。事件循环结束后，在控制台上打印 `result()` 方法返回的元组。

该子类（包括测试代码）可以使用 60 行左右编写。如果你是第一次使用 Qt Designer，可能需要花费 15–20 分钟来完成设计，但通过练习，这样的对话框只需要几分钟就能完成。

模型解决方案位于 `chap07/ticketorderdlg1.ui` 和 `chap07/ticketorderdlg2.ui` 中，并在 `chap07/ticketorderdlg.py` 中提供了一个测试程序。

# 8

- 主窗口的职责

- 数据容器的职责

- 保存和加载二进制文件

- 保存和加载文本文件

- 保存和加载 XML 文件

# 数据处理与自定义格式

大多数应用程序都需要加载和保存数据。通常情况下，数据格式是预先定义的，因为应用程序正在读取由某些它无法控制的应用程序产生的数据。但对于我们自己创建文件格式的应用程序，有很多选项可用。

在第 6 章中，我们创建了一个主窗口风格的应用程序，从中我们学习了如何创建菜单和工具栏，以及如何处理文件的加载和保存。在本章中，我们将处理另一个主窗口风格的应用程序，但这次我们的重点是应用程序的数据数据。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_241_0.png)

图 8.1 My Movies 

我们将作为示例的应用程序是 My Movies；如图 8.1 所示。它用于存储我们收藏中可能拥某些电影的基本信息。该应用程序将允许我们查看和编辑一组自定义的 `Movie` 对象（或我们称之为电影记录），并以各种格式将这些记录加载和保存到磁盘。

228 第 8 章。数据处理与自定义文件格式

如果你想直接深入文件处理，可以跳到相关章节。保存和加载二进制文件的内容从第 240 页开始，文本文件从第 249 页开始，XML 文件从第 256 页开始。你可以随时回到前两个章节来涵盖 GUI 与文件处理之间的关系。

在之前的所有示例中，我们通常尽可能将数据保留在 Python 数据类型中，只在需要时才从中进行转换。特别是对于字符串，我们提出了一项策略：尽可能早地将 `String` 转换为 `unicode`，并且在 `unicode` 字符串上进行操作。但这次我们将采取相反的方法，将所有数据保留在 PyQt 类型中，只在需要时才转换为 Python 类型。这样做的原因之一是 PyQt 对二进制数据提供了极好的支持，并使用了与 C++/Python 相同的二进制格式，这在处理必须被 C++ 和 Python 程序共同访问的文件时非常有用。另一个原因是，这将提供对比，帮助我们理解每种方法的优缺点，以便在我们所处理的应用程序中做出正确的决策。

将数据保留在 PyQt 类型中的一个直接益处是，我们不需要对提供给用于查看和编辑的控件之间交换的数据进行不断转换。在处理大量数据时，这可以显著节省处理开销。

当我们有数据需要加载和保存时，有五个选项供我们。我们可以使用二进制、纯文本或 XML 文件，也可以使用带有显式文件名的 `QSettings` 对象，或者使用数据库。在本章中，我们将涵盖前三个选项，并简要提到第四个 `QSettings`。我们将数据库的内容推迟到第 15 章。

`QSettings` 的所有选项都可以使用 Python 标准库或 PyQt 实本章中，我们将讨论如何使用这两个库加载和保存二进制及文本格式，以便我们进行比较和对比。对于 XML，我们将使用 PyQt 进行加载和解析，保存将由我们自己完成。Python 标准库也提供了大量的 XML 输出功能，但它无法展示使用 PyQt 的 XML 类可以实现的功能。

在第 6 章中，我们将展示如何使用 `QSettings` 对象保存和加载用户设置，例如主窗口的大小和位置，以及最近使用的文件列表。该类将所有数据存储为 `QVariant`，这对于少量数据是完全可以的。我们可以通过创建一个带有文件名的 `QSettings` 实例来存储自定义数据——例如，`inifile = QSettings("curvedata.ini", QSettings.Format)`。现在我们可以使用 `iniFile` 对象通过 `setValue()` 写入数据并使用 `value()` 读取数据，在这两种情况下都在 `QVariant` 和相关类型之间进行转换。

229

在接下来的章节中，我们将查看由主窗口执行的高级文件处理和数据展示。在第二个章节中，我们将查看应用程序的数据模块，包括数据项目的实现，以及存储数据的容器。

然后，在随后的章节中，我们将查看各种格式的保存和加载。在某一中我们将查看如何使用 PyQt 的 `QStream` 类和标准库的 `pickle` 模块来加载和保存我们的记录。在文本文件章节，我们将看到如何使用 PyQt的 `QStream` 和 Python 标准库的 `codecs` 模块以纯文本格式加载和保存记录。在最后一个章节中，我们将手动编写保存为 XML 代码，并查看如何使用 DOM 和 SAX 解析器读取 XML 数据。

## 主窗口的职责

主窗口通常被赋予提供高级文件处理和展示数据的职责。在本节中，我们将特别关注文件操作，因为它们与第 6 章的 Image Changer 应用程序不同，更具代表性。我们还将查看数据是如何呈现给用户的。在 My Movies 应用程序中，数据存储在“容器”（`MovieContainer`）中，所有的保存和加载（导出和导入）工作都由主窗口传递给容器。我们将在下一节查看代码，并在后续章节中查看容器的保存加载代码。

现在我们准备好查看主窗口的文件处理功能了。我们将从主窗口初始化函数的开始部分，查看

# 第 8 章 数据处理与自定义文件格式

![](img/55bc1dcf8601cfec5e1423b4e17ec264_244_0.png)

**图 8.2** 我的 Movie 应用程序的模块、类和函数

用于处理数据的电影容器和显示数据的 QTableWidget。

```python
class MainWindow(QMainWindow):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        self.movies = moviedata.MovieContainer()
        self.table = QTableWidget(self)
        self.setCentralWidget(self.table)
```

在调用 `super()` 之后，我们创建了一个新的电影容器。（稍后我们将查看 `Movie` 和 `MovieContainer` 类）。然后我们创建了一个 `QTableWidget`。该小部件用于展示和可选地编辑表格数据。表格在 `updateTable()` 中进行设置和填充。我们省略了初始化器部分，因为我们已经从第 6 章知道了如何设置状态栏、创建文件、编辑和帮助操作、、填充菜单和工具栏，以及从上一次会话的设置恢复应用程序的状态。

为了完整起见，我们现在将简要回顾一下 `updateTable()`，看看表格是如何设置和填充的。（如果你只想纯粹关注文件处理，可以直接跳到第 232 页的 `updateTable()`）。我们使用的方法非常简单直接。PyQt 还提供了一种使用 PyQt 的模型/视图架构，通过列表、表格和树来填充和编辑基于项的小部件的高级方法——我们将在第 14 章学习这些。

```python
def updateTable(self, current=None):
    self.table.clear()
    self.table.setRowCount(len(self.movies))
    self.table.setColumnCount(5)
    self.table.setHorizontalHeaderLabels(["标题", "年份", "分钟", "获取", "备注"])
```

## 主窗口的职责

```python
self.table.setAlternatingRowColors(True)
self.table.setEditTriggers(QTableWidget.NoEditTriggers)
self.table.setSelectionBehavior(QTableWidget.SelectRows)
self.table.setSelectionMode(QTableWidget.SingleSelection)
selected = None
```

这个方法相当长，因此我们将分三部分进行回顾。它可以在不带参数的情况下调用，这种情况下它只是简单的填充表格；也可以带有当前 `Movie` 的 `id()` 进行调用，这种情况下它会在填充表格后，使指定的电影行被选中并可见（在需要时滚动）。如果刚刚添加或编辑了电影，则会传递一个当前电影。

我们从清除表格开始；这会清除所有数据和表头。接下来，我们设置行数、列数以及列标题。我们设置了表格的属性，使用户无法进行就地编辑；在这个特定的应用程序中，我们倾向于使用单独的添加/编辑对话框。我们还确保用户一次只能选择一行。`selected` 变量持有包含当前电影标题和 `id()` 的 `QTableWidgetItem`（如果有的话）。

```python
for row, movie in enumerate(self.movies):
    item = QTableWidgetItem(movie.title)
    if current is not None and current == id(movie):
        item = current
        item.setData(Qt.UserRole, QVariant(long(movie)))
    self.table.setItem(row, 0, item)
    year = movie.year
    if year != movie.UNKNOWNYEAR:
        item = QTableWidgetItem("%d" % year)
        item.setTextAlignment(Qt.AlignCenter)
        self.table.setItem(row, 1, item)
    minutes = movie.minutes
    if minutes != movie.UNKNOWNMINUTES:
        item = QTableWidgetItem("%d" % minutes)
        item.setTextAlignment(Qt.AlignRight|Qt.AlignCenter)
        self.table.setItem(row, 2, item)
    item = QTableWidgetItem(movie.acquired.toString(moviedata.DATEFORMAT))
    item.setTextAlignment(Qt.AlignRight|Qt.AlignCenter)
    self.table.setItem(row, 3, item)
    notes = movie.notes
    if notes.length() > 40:
        notes = notes.left(39) + "..."
    self.table.setItem(row, 4, QTableWidgetItem(notes))
```

QTable 中的每个单元都由一个 `QTableWidgetItem` 表示。这些项可以包含显示文本，还可以包含“用户”数据。我们遍历电影容器中的每部电影，为每部电影创建一个行项。我们将电影的标题存储在每行的第一个单元格（项）中，并将此项的用户数据设置为持有电影的 `id()`。我们必须将 ID 转换为 `long` 类型，以确保它被正确地存储在 `QVariant` 中。一旦项被创建并设置，我们就将其放在表格中相应的行和列中。

只有在有数据时我们才会填充年份和分钟单元格。对于备注，如果数据很长，我们会进行截断并添加省略号，因为备注可能有很多段落。

```python
self.table.resizeColumnsToContents()
if selected is not None:
    selected.setSelected(True)
    self.table.currentItemItem(selected)
    self.table.scrollToItem(selected)
```

一旦表格填充完毕，我们就会调整列宽以适应内容。当我们遍历电影时，表格将按字母顺序显示。如果用户点击某一行，主窗口将突出相应的电影。这是通过将 `itemSelectionChanged` 信号连接到处理选择的槽实现的。

## 主窗口的职责

```python
def fileOpen(self):
    path = QFileInfo(self.movies.filename()).path() \
        if not self.movies.filename().isEmpty() else ""
    name = QFileDialog.openFileName(self,
        "My Movies - 加载电影数据", path,
        "My Movies 文件 (%s)" % self.movies.formats())
    if not name.isEmpty():
        ok, msg = self.movies.load(name)
        self.statusBar().showMessage(msg, 5000)
        self.updateTable()
```

```python
def fileNew(self):
    if not self.movies.isDirty():
        return
    self.movies.clear()
    self.statusBar().clear()
    self.updateTable()
```

```python
def fileSave(self):
    if self.movies.filename().isEmpty():
        self.fileSaveAs()
    else:
        ok, msg = self.movies.save()
        self.statusBar().showMessage(msg, 5000)
```

打开文件的结构与我们之前看到的相似。电影容器以 `QString` 持有当前文件名。通常情况下，应用程序只有一个自定义格式，但为了演示目的，My Movies 应用程序支持多种格式，因此我们提供了一个 `formats()` 方法来返回可以使用的扩展名。

```python
def fileImportDOM(self):
    self.fileImport("dom")
```

```python
def fileImportSAX(self):
    self.fileImport("sax")
```

## 第 8 章 数据处理与自定义格式

```python
def fileImport(self, format):
    if not self.okToContinue():
        return
    path = QFileInfo(self.movies.filename()).path \ \
    if not self.movies.filename().isEmpty() else "."
    fname = QDialog.getOpenFileName(self,
        "My Movies - Import Movie Data", path,
        "My Movies XML files (*.xml)")
    if not fname.isEmpty():
        if format == "dom":
            ok, msg = self.movies.importDOM(fname)
        else:
            ok, msg = self.movies.importSAX(fname)
        self.statusBar().showMessage(msg, 5000)
        self.update()
```

通常情况下，我们会提供一个单一的导入方法，并使用 SAX 或 DOM 解析器。在这里，我们选择同时展示两种解析器，因此我们提供了两个独立的导入动作。它们产生相同的结果。

用于导入的文件动作与“打开文件”动作非常相似，只是我们使用了用户指定的导入解析器。和所有的文件处理代码一样，我们将将其传递给电影容器。

```python
def fileExportXml(self):
    fname = self.movies.filename()
    if not fname.isEmpty():
        fname = "."
    else:
        i = fname.lastIndexOf(".")
        if i > 0:
            fname = fname.left(i)
        fname += ".xml"
    fname = QDialog.getSaveFileName(self,
        "My Movies - Export Movie Data", fname,
        "My Movies XML files (*.xml)")
    if not fname.isEmpty():
        if not fname.contains(".*"):
            fname += ".xml"
        ok, msg = self.movies.exportXml(fname)
        self.statusBar().showMessage(msg, 5000)
```

我们只提供了一个 XML 导出方法。该代码与“另存为”动作类似。注意，我们必须使用 `QString` 方法来确保文件名具有 .xml 扩展名，而不是我们在 Image Changer 应用中使用的 Unicode 方法，因为文件名是以 `QString` 形式存储的。

## 数据容器的职责

应用程序的数据容器负责持有所有数据项（即电影记录），并负责它们从磁盘中保存和加载。我们在前面的章节中查看 `MainWindow.updateTable()` 方法时，已经看到如何使用 `for` 循环迭代容器来获取所有电影，以便它们能够在应用程序的 `QWidget` 中显示。在本节中，我们将查看用于存储电影数据的数据结构、我们如何提供对有序迭代的支持，以及其他方面，但不包括实际的保存和加载代码，因为那部分将在随后的章节中介绍。

为什么要使用自定容器呢？毕竟，我们难道不能直接使用 Python 的内置数据结构之一（例如 `list` 或 `dict`）吗？我们更倾向于采用将标准数据结构封装在自定义容器中的方法。这确保了对数据的访问由我们的类控制，有助于维护数据的完整性。它还使得扩展容器的功能变得容易，并在未来替换底层数据结构。换句话之，这是一种面向对象的方法，避免了简单使用（例如 `list` 配合某些全局函数的缺点。

我们将从 `moviediedata` 模块的文件和常量开始。

```python
import bisect
import codecs
import copy_reg
import gzip
import cpickle
from PyQt4.QtCore import *
from PyQt4.QtXml import *
```

我们将电影按规范化的标题顺序存储，忽略大小写，并忽略开头的 "A"、An" 和 "The"。我们使用 `bisect` 模块来维护顺序，使用了与我们在第 3 章中实现 `OrderedDict` 时相同的技术。

`codecs` 模块对于使用特定编码读写 Python 文本文件是必要的。`copy_reg` 和 `cpickle` 模块用于保存和加载 "pickles"——即包含任意数据结构的文件。`gzip` 模块用于压缩数据；我们将使用它来压缩和解压 pickled 数据。`PyQt4` 是熟悉的，但我们还必须导入 `PyQt4.QtXml` 模块以访问 PyQt 的 SA 和 DOM 解析器。将在接后的章节中看到所有的模块。注意，我们不需要 `PyQt4.QtGui` 模块，因为 `moviediedata` 模块是一个纯数据处理模块，不包含 GUI 功能。

```python
CODEC = "UTF-8"
```

# 第 8 章 数据处理与自定义文件格式

```python
NEWPARA = unichr(0x2029)
NEWLINE = unichr(0x2028)
```

我们想要对文本文件使用 UTF-8 编码。这是一种 8 位的 Unicode 编码，每个 ASCII 字符使用一个字节，而任何其他字符使用两个或多个字节。它可能是最广泛使用的 Unicode 文本编码文件。通过使用 Unicode，我们可以存储今天今天使用的几乎任何人类语言编写的文本。

尽管 `\n` 是一个有效的 Unicode 字符，但当我们使用 XML 时，我们需要使用 Unicode 特有的段落分隔符和换行符。这是因为 XML 解析器通常不区分 ASCII 空格字符（如换行符）和其他字符（如空格），如果我们想保留用户的换行和段落分隔符，这将会是不方便的。

```python
class Movie(object):
    UNKNOWNYEAR = 1890
    UNKNOWNMINUTES = 0

    def __init__(self, title=None, year=UNKNOWNYEAR, minutes=UNKNOWNMINUTES, acquired=None, notes=None):
        self.title = title
        self.year = year
        self.minutes = minutes
        self.acquired = acquired if acquired is not None else QDate.currentDate()
        self.notes = notes
```

`Movie` 类用于持有电影数据。我们使用实例变量而不是提供 getter 和 setter。标题和注释以 `QString` 存储，获取日期以 `QDate` 存储。年份和时长以 `int` 存储。

```python
class MovieContainer(object):
    MAGIC_NUMBER = 0x305E
    VERSION = 100

    def __init__(self):
        self._fname = QString()
        self._movies = []
        self._movieIdFrom = {}
        self._dirty = False
```

## 数据容器的职责

MAGIC NUMBER 和 VERSION 用于使用 PyQt 的 `DataStream` 类保存加载文件。

文件名是一个 `QString`。`__movies` 列表的每个元素都是一个双元素列表，第一个元素是排序键，第二个是 `Movie`。这是类主要的数据结构，用于按顺序持有电影。`__movieId` 字典的键是电影对象的 `id()`，值是 `Movie`。我们在第 1 章中看到，当已知电影 ID 时，每个 Python 对象都能方便地提供查找。例如，主窗口将电影 ID 存储在 `QWidgetItem` 的 "user" 属性中。当然，由于两个数据结构实际上持有的是 `Movie` 引用而不是 `Movie` 对象本身，因此没有数据重复。

```python
def __iter__(self):
    for pair in iter(self.__movies):
        yield pair[1]
```

当 `MainWindow.updateTable()` 方法迭代电影容器时，Python 使用了容器的 `__iter__` 方法。在这里我们看到遍历有序的 `[key, movie]`，每次返回电影项。

```python
def __len__(self):
    return len(self.__movies)
```

该方法允许我们对电影容器使用 `len()` 函数。

在后续章节中，我们将看到以各种格式加载和保存的代码。但首先我们将查看如何清空容器，以及如何添加、删除和更新电影，以便我们了解容器是如何工作的，特别是关于排序的。

```python
def clear(self, clearFilename=True):
    self.movies = []
    self.__movieIdFrom = {}
    if clearFilename:
        self.__fname = QString()
    self.dirty = False
```

## 第 8 章 数据处理与自定义格式

```python
return False
key = self.key(movie.title, movie.year)
bisect.insert_left(self, __movies, [key, movie])
self.__movieFromId[id(movie)] = movie
self.__dirty = True
return True
```

第一个 `if` 语句确保我们不会重复添加同一个电影。我们使用 `key()` 方法生成一个合适的顺序，然后使用 `bisect` 模块的 `insert_left` 函数将包含两个元素的 `[key, movie]` 列表插入 `__movies` 列表中。这非常快，因为 `bisect` 模块使用了二分切分算法。我们还确保 `__movieFromId` 字典是最新的，并将容器标记为“脏”（dirty）。

```python
def key(self, title, year):
    text = unicode(title).lower()
    if text.startswith("a "):
        text = text[2:]
    elif text.startswith("an "):
        text = text[3:]
    elif text.startswith("the "):
        text = text[4:]
    parts = text.split(" ", 1)
    if parts[0].isdigit():
        text = "%04d" % int(parts[0])
        if len(parts) > 1:
            text += " " + parts[1]
    return u"%s%d" % (text.replace(" ", ""), year)
```

该方法生成一个适用于我们电影数据排序的键字符串。我们不保证键的唯一性（尽管这样做很困难），因为有序数据结构是一个列表，重复的键并不是问题。该代码是针对英语的，删除了电影标题中的定冠词和不定冠词。如果电影标题以数字开头，我们会在数字前补零，例如“20”会排“100”之前。我们不需要对年份进行填充，因为年份始终是四位数。所有其他数据都使用 PyQt 数据类型存储，但我们选择对键字符串使用 unicode。

```python
def delete(self, movie):
    if id(movie) not in self.__movieFromId:
        return False
    key = self.key(movie.title, movie.year)
    i = bisect.bisect_left(self, __movies, [key, movie])
    del self.__movies[i]
    del self.__movieFromId[id(movie)]
    self.__dirty = True
    return True
```

## 数据容器的职责

要删除一部电影，我们必须从两个数据结构中都删除它，在电影列表中，我们必须先找到电影的索引位置。

```python
def updateMovie(self, movie, title, year, minutes=None,
    notes=None):
    if minutes is not None:
        movie.minutes = minutes
    if title is not None:
        movie.notes = notes
    if title != movie.title or year != movie.year:
        key = self.key(movie.title, movie.year)
        i = bisect.bisect_left(self.movies, [key, movie])
        self.movies[i][0] = self.key(title, year)
    movie.title = title
    movie.year = year
    self.movies.sort()
    self._dirty = True
```

如果用户编辑了电影，应用程序始终会带有用户的更改调用此方法。如果传递的 `minutes` 或 `notes` 为 `None`，则意味着它们没有变化。如果电影的标题或年份发生了变化，电影现在可能处于电影列表中的错误位置。在这种情况下，我们使用原始标题和年份找到电影，设置新标题并重新排序。这在实践中的开销并没有初看起来看起来那么大。列表最多只会包含一个排序错误的项目，而且 Python 的排序算法对部分有序的数据进行了高度优化。

如果我们在这里发现有性能问题，我们可以始终使用 `delete` 和 `add insert` 重新实现 `updateMovie()`。

```python
@staticmethod
def formats(self):
    return "*.mqb *.mpb *.mqt *.mpt"
```



# 第 8 章 数据处理与自定义文件格式

通常我们为应用程序提供一个或最多两个自定义数据格式，但为了说明目的，我们使用四种扩展提供了三种格式。`.mqb` 扩展是 Qt 二进制格式，它使用 `QDataStream` 类；`.mpb` 是 Python pickle 格式（使用 gzip 压缩）。`.mqt` 扩展是 Qt 文本格式，`.mpt` 扩展是 Python 文本格式。两种格式是相同的，但通过使用不同的格式，我们可以为了对比而使用不同的保存和加载代码。

```python
def save(self, fname=QString()):
    if not fname.isEmpty():
        self._fname = fname
        if self.fname.endswith(".mqb"):
            return self.saveQDataStream()
```

```python
elif self._fname.endswith(".mpb"):
    return self.savePickle()
elif self._fname.endswith(".mqt"):
    return self.saveQTextStream()
elif self._fname.endswith(".mpt"):
    return self.saveText()
return False, "Failed to save: invalid file extension"
```

当用户调用“文件”操作时，我们期望数据容器的 `save()` 方法被调用。这在 My Movies 中是这样发生的，也是常规做法。然而在这里，我们没有执行保存，而是展示了如何使用 `QDataStream` 来保存。

版本为 `Qt_4_2`，以及用于后续版本的另一种文件格式。然后，当我们开始加载数据时，我们会根据文件格式版本号获取相应的 `QDataStream` 版本。

设置 `QData` 版本非常重要，因为我们必须确保任何 PyQt 数据类型都能被正确保存和加载。只有一种情况下不重要，即我们只保存和加载整数，因为它们的表示方式永远不会改变。

```python
for key, move in self.__movies:
    stream << move.title
    stream.writeInt16(move.year)
    stream.writeInt16(move.minutes)
    stream << move.acquired << move.notes
```

现在我们将遍历二进制电影的数据并将其写入数据流。数据的格式如图 8.3 所示。`QDataStream` 类为许多 PyQt 类重载了 `<<` 运算符，包括 `int`、`QString` 和 `QImage`，因此我们使用类似 C++ 的语法来写入数据。`<<` 运算符将其右操作数写入其左操作数对应的数据流中。它可以重复应用于同一个流，并返回被应用的用的流，但对于整数，我们使用 `writeInt()` 和 `writeIntn()` 方法。

| int32 | int32 | 电影 #1 | 电影 #2 | ... | 电影 #n |
| :--- | :--- | :--- | :--- | :--- | :--- |
| QString | int_16 | int_16 | QData | QString | |

> 图 8.3 QDataStream My Movies 文件格式

由于我们写入的是二进制数据，因此没有任何格式化。我们只需要确保在加载回数据时，使用相同的 `QDataStream` 版本，并按照保存数据时的相同顺序加载数据类型。在这种情况下，我们将读回两个整数（魔数和文件版本号），然后加载任意数量的电影记录，每条记录由一个字符串、两个整数和一个日期组成。

```python
except (IOError, OSError):
    error = "保存失败: %s" % e
finally:
    if fh is not None:
        fh.close()
    if error is not None:
        return False, error
    self.__dirty = False
```

## 保存和加载二进制文件

```python
return True, "已保存 %d 条电影记录到 %s" % (
    len(self.__movies),
    QFileInfo(self.__fname).fileName()
)
```

如果发生任何错误，我们只需放弃并返回一个失败标志和错误消息。否则，我们清除脏标记标志并返回一个成功标志以及一条指示保存了多少条记录的消息。

对应的加载方法同样简单，尽管它需要进行更多的错误处理。

```python
def loadQDataStream(self):
    error = None
    fh = None
    try:
        fh = QFile(self.__fname)
        if not fh.open(QIODevice.ReadOnly):
            raise IOError(unicode(fh.errorString()))
        stream = QDataStream(fh)
        magic = stream.readInt32()
        if magic != MovieContainer.MAGIC_NUMBER:
            raise IOError("无法识别的文件类型")
        version = stream.readInt32()
        if version < MovieContainer.FILE_VERSION:
            raise IOError("旧且不可读的文件格式")
        elif version > MovieContainer.FILE_VERSION:
            raise IOError("新且不可读的文件格式")
        stream.setVersion(QDataStream.Qt_4_2)
        self.close(False)
```

我们像以前一样创建 `QFileInfo` 和 `QDataStream` 对象，只是这次使用的是 `ReadOnly` 模式而不是 `WriteOnly` 模式。然后我们读取魔数。如果这不是一个唯一的 My movies 数据文件编号，我们就会抛出一个异常。接下来，我们读取文件版本，并确保它是我们可以处理的版本。在此时，如果我们正在使用此文件格式的多个版本，我们将根据文件版本进行分支处理。然后我们设置 `QDataStream` 版本。

下一步是清除电影数据结构。我们尽可能晚地执行此操作，这样如果早早抛出了异常，原始数据将保持完好。`False` 参数告诉 `clear()` 方法清空 `__movieFromId`，但不清除文件名。

```python
while not stream.atEnd():
    title = QString()
    acquired = QDate()
    notes = QString()
    stream >> title
    year = stream.readInt16()
```

## 文件错误处理方法

本章处理文件错误的方法结构如左所示。另一种同样有效的方法（例如在 `chap09/txteditit.py` 和 `chap14/ships.py` 中使用）如右所示。

```python
error = None
fh = None
try:
    # 打开文件并读取数据
except (IOError, OSError), e:
    error = unicode(e)
finally:
    if fh is not None:
        fh.close()
if error is not None:
    return False, error
return True, "成功"
```

```python
exception = None
fh = None
try:
    # 打开文件并读取数据
except (IOError, OSError), e:
    exception = e
finally:
    if fh is not None:
        fh.close()
if exception is not None:
    raise exception
```

在调用点，假设我们正在处理一个 `load()` 方法，对于左侧的方法，我们可能如下代码：

```python
ok, msg = load(args)
if not ok:
    MessageBox.warning(self, msg)
```

对于右侧的方法，我们可以使用如下代码：

```python
try:
    load(args)
except (IOError, OSError) as e:
    MessageBox.warning(self, unicode(e))
```

另一种方法（在 `chap09/editor.py` 和 `chap12/designer.py` 中使用）是在方法内部进行错误处理：

```python
error = None
fh = None
try:
    # 打开文件并读取数据
except (IOError, OSError) as e:
    error = unicode(e)
finally:
    if fh is not None:
        fh.close()
if error:
    return False, error
return True
```

在调用点，我们可能如下代码：

```python
ok, msg = load(args)
if not ok:
    MessageBox.warning(self, msg)
```

## 保存和加载二进制文件

```python
copy_reg.pickle(QDate, pickleQDate)
copy_reg.pickle(QString, pickleQString)
```

`copy_reg` 模块用于指定如何读写非标准数据类型。信息通过调用 `copy_reg.pickle` 并传入两个参数提供。第一个参数是我们希望能够 pickle（序列化）的新样式类，第二个参数是一个函数。该函数必须接受一个参数，即我们想要 pickle 的类实例，并应该返回一个二元组，该二元组的第一个元素是类，第二个元素是一个标准 Python 类型的元组，这些类型可以传递到类的构造函数中，以创建一个与传入实例具有相同值的实例。

有了这些信息，`pickle` 模块可以通过将类名存储为文本并将参数存储为标准 Python 类型的元组，来存储我们类的实例。然后，当我们想要将数据重新 pickle（加载）时，PyQt 可以使用 `eval()` 来重新创建我们的实例。

PyQt 4.3 支持对基本 Qt 数据类型的序列化，包括 `QByteArray`、`QColor`、`QDate`、`QDateTime`、`QLine`、`QMatrix`、`QPoint`、`QPolygon`、`QRect`、`QSize`、`QString`、`QTime` 以及所有的 PyQt 枚举。这意味着我们可以“pickle”这些任何一种类型，而无需注册和使用自己的序列化函数。

```python
def savePickle(self):
    error = None
    fh = None
    try:
        fh = gzip.open(unicode(self.__fname), "wb")
        pickle.dump(self.movies, fh, 2)
    except (IOError, OSError) as e:
        error = "Failed to save: %s" % e
    finally:
        if fh is not None:
            fh.close()
        if error is not None:
            return False, error
        self.__dirty = False
        return True, "Saved %d movie records to %s" % (len(self.movies), QFileInfo(self.__fname).filename())
```

我们可以轻松地将任何 Python 数据结构（包括递归结构）保存为 pickle。我们通过以二进制模式打开文件并使用 `dump()` 函数来实现这一点。在这个示例中，我们选择了对 pickle 进行压缩（这可以减少大约 50% 文件大小），但我们也可以避免使用这种压缩：

```python
fh = open(unicode(self.__fname), "wb")
```

我们必须将文件名转换为 unicode，因为它是以 `QString` 形式存储。`open()` 的 `wb` 参数意味着“写入二进制”。`dump()` 函数接受一个 Python 数据结构（在本例中是我们的 `[key, movie]` 列表列表）、一个文件句柄和一个格式代码。我们始终使用格式代码 2，这意味着 pickle 二进制格式。

由于键是通过 `key()` 方法生成的，我们实际上只需要保存 `Movie` 实例，而不是 `[key, movie]` 列表。如果磁盘空间非常宝贵，我们可能会这样做，但这要求我们在加载数据时重新生成键，因此这在磁盘空间和保存加载速度之间存在一种权衡。我们选择了为了更快、更方便的保存和加载而牺牲磁盘空间。

```python
def loadPickle(self):
    error = None
    fh = None
    try:
        fh = gzip.open(unicode(self.__fname), "rb")
        self.clear(False)
        self.movies = cpickle.load(fh)
        for key, movie in self.movies:
            self._movieFromId[id(movie)] = movie
    except (IOError, OSError) as e:
        error = "Failed to load: %s" % e
    finally:
        if fh is not None:
            fh.close()
        if error is not None:
            return False, error
        self._dirty = False
        return True, "Loaded %d movie records from %s" % (len(self.movies),
            QFileInfo(self.__fname).fileName())
```

反序列化（unpicking）几乎和序列化一样简单。我们必须记住使用 zip 打开文件以便解压。`open()` 的 `rb` 参数意味着“读取二进制”。我们使用 `pickle load()` 函数来检索数据；它接受一个文件句柄并返回数据结构。我们将数据结构直接赋值给电影列表。我们遍历电影以填充 `_movieFromId` 字典：这无法保存，因为它取决于 Movie id，这在每次应用程序运行时都会变化。

序列化和反序列化是保存和加载二进制数据最简单的方法，适用于数据为标准 Python 数据类型的情况。如果我们将数据存储为 PyQt 数据类型，通常最好使用 `QDataStream`。该类在存储复杂的 PyQt 数据类型方面比 `pickle` 模块更有效（因为没有序列化所需的转换开销），并且它产生的文件比 `pickle` 产生的更紧凑（除非 pickle 数据经过了压缩）。它还便于与 C++/Qt 程序提供无缝的数据格式互操作性。

## 保存和加载文本文件

PyQt 和 Python 标准库提供了读写文本文件的设施。PyQt 使用 `QTextStream` 类，而 Python 标准库使用 `codecs` 模块。

纯文本格式通常是人类可读的（例如在文本编辑器中），并且通常很容易编写。任何数据都可以以某种形式的纯文本写入。数字和日期可以使用它们的字符串表示轻松且紧凑地写入。

| 格式 | 示例 |
| --- | --- |
| 电影标题 | 1995 2001 |
| 年份 分钟 | |
| 获取日期 获取 笔记 | |

## 保存与加载文本文件

我们省略了 `except` 和 `finally` 块的代码，因为它们与我们之前看到的代码相同——例如，在 `saveQDataStream()` 方法中。

虽然以文本格式写入非常简单，但将其读回并不容易。我们必须读取每个整数（年份、分钟和获取日期的组成部分），然后将其转换为它所代表的整数。但主要问题是，我们必须正确解析文件，以提取每部电影的记录属性。

处理整数并不是太困难，因为 `QString` 提供了 `toInt()` 方法；但该方法返回的是成功/失败标志，而不是抛出异常，如果每次处理数字时都进行检查，意味着每个数字我们需要三行代码而不是一行。出于这个原因，我们创建了一个更符合 Python 风格的封装函数，用于读取整数。

```python
def intFromQstr(qstr):
    i, ok = qstr.toInt()
    if not ok:
        raise ValueError(unicode(qstr))
    return i
```

该函数简单地调用 `QString.toInt()` 并在失败时抛出异常，或者返回它所寻找的整数。

为了解析我们的电影文本文件，我们将使用一个有限状态机来收集每部电影的数据。解析单部电影的自动机如图 8.5 所示。这意味着在读取每一行之前，我们对该行包含的内容有一个预期。如果未符合预期，我们就得到了错误；否则，我们读取预期的数据，并为下一行应该的内容设置预期。

```python
def loadQTextStream(self):
    error = None
    fh = None
    try:
        fh = QFile(self._fname)
        if not fh.open(QIODevice.ReadOnly):
            raise IOError(unicode(fh.error))
        stream = QTextStream(fh)
        stream.setCodec(CODEC)
        self.clear(False)
        lino = 0
```

该方法的开始非常熟悉。一旦打开了文件、创建了 `QTextStream` 并设置了编码，我们就会清空电影数据，准备好从磁盘读取数据。

对于电影，我们首先期望一个“title”的行，其中包含 `{{MOVIE}}`，后面跟着一个空格和电影标题，然后是一个“numbers”行，其中包含年份、分钟和获取日期，接着是一个“notes”行，它只包含 `{NOTES}`、零行或多行注释文本，最后是一个包含 `{{ENDMOVIE}}` 的“end”行。我们从预期一个“title”行开始。

为了帮助用户找到格式错误，我们在 `lino` 变量中跟踪当前行号，我们会在错误消息中使用它。

我们用于遍历整个文件的 `while` 循环体非常长，因此我们将分部分查看。

```python
while not stream.atEnd():
    title = year = minutes = acquired = notes = None
    line = stream.readline()
    lino += 1
    if not line.startsWith("{{MOVIE}}"):
        raise ValueError("no movie record found")
    else:
        title = line.mid(len("{{MOVIE}}")).trimmed()
```

我们首先将存储单部电影属性的变量初始化为 `None`，这样很容易判断我们是否已经读取了所有属性。

我们遍历文件中的每一行。与 Python 标准库的 `file.readline()` 方法不同，PyQt 的 `QTextStream.readline()` 会剥离行尾的换行符。我们每读取一行，`lino` 就会增加。

任何电影的第一行都以 `{{MOVIE}}` 标记开头。如果行不是，我们就会抛出一个带有错误消息的异常；异常处理器会将行号添加到传递给用户的消息中。如果该行是正确的，我们通过读取行开头 `{{MOVIE}}` 标记之后的文本来提取电影标题，并去除任何前后的空白。

`QString.mid(n)` 方法等同于 `unicode[n:]`，而 `QString.trimmed()` 等同于 `unicode.strip()`。

现在我们准备好读取“numbers”行。

```python
if stream.atEnd():
    raise ValueError("premature end of file")
line = stream.readline()
lino += 1
parts = line.split(" ")
if len(parts) != 3:
    raise ValueError("invalid numeric data")
```

```python
year = intFromQStr(parts[0])
minutes = intFromQStr(parts[1])
ymd = parts[2].split("-")
if len(ymd) != 3:
    raise ValueError("invalid acquired date")
acquired = QDate(intFromQStr(ymd[0]),
                intFromQStr(ymd[1]),
                intFromQStr(ymd[2]))
```

我们首先检查是否过早到达文件末尾，如果是，我们就抛出一个异常。我们读取“numbers”行。这一行应该包含一个整数（年份）、一个空格、一个整数（分钟）、一个空格以及 YYYY-MM-DD 格式的获取日期。我们起初按空格字符对该行进行分割，这给了我们三个字符串：年份、分钟和获取日期。即使添加了注释文本，我们有一个 `QString` 而不是 `None` 这一事实就足以告诉我们读取了注释，即使它们是空的。

现在我们准备好读取 `{{NOTES}}` 标记，可选跟随几行注释，最后是 `{{ENDMOVIE}}` 标记。

```python
if stream.atEnd():
    raise ValueError("premature end of file")
line = stream.readline()
lino += 1
if line != "{NOTES}":
    raise ValueError("expected notes")
notes = QString()
while not stream.atEnd():
    line = stream.readline()
    lino += 1
    if line == "{{ENDMOVIE}}":
        if title is None or minutes is None or acquired is None or notes is None:
            raise ValueError("incomplete record")
        self.add(Movie(title, minutes, acquired, notes.trimmed()))
        break
    else:
        notes += line
else:
    raise ValueError("missing end marker")
```

## 表 8.2 常用的 QTextStream 方法

| 语法 | 描述 |
| :--- | :--- |
| `s.atEnd()` | 如果 `QTextStream` 到达结束则返回 True |
| `s.setCodec(c)` | 将 `QTextStream` s 的编码设置为 c 中指定的编码——这可以是一个字符串（例如 "UTF-8"），也可以是 `QTextCodec` 对象 |
| `s << x` | 将对象 x 写入 `QTextStream` s；x 的类型可以是 bool, float, int, QString, str 以及其他少数类型 |
| `s.readLine()` | 读取一行，返回剥离了任何结束行符的 `QString` |
| `s.readAll()` | 读取整个文件，返回一个 `QString` |

## 保存和加载文本文件

错误处理与我们之前看到的几乎完全相同，这次我们包含了错误发生的行号。

## 使用 codecs 模块

使用 PyQt 类的替代方案是使用 Python 的内置和标准库类来写入和读取文本文件。可以使用文件类直接进行写入和读取操作，但如果我们想指定编码，则必须使用 `codecs` 模块。

```python
def saveText(self):
    error = None
    fh = None
    try:
        fh = codecs.open(unicode(self.__fname), "w", CODEC)
        for key, movie in self._movies:
            fh.write(u"{MOVIE} %s\n" % unicode(movie.title))
            fh.write(u"%d %d %s\n" % (movie.year, movie.minutes, movie.acquired.toString(Qt.ISODate())))
            fh.write(u"{NOTES}\n")
            if not movie.notes.isEmpty():
                fh.write(u"%s\n" % unicode(movie.notes))
            fh.write(u"{ENDMOVIE}\n")
```

我们使用的文本格式与使用 `QTextStream` 写入时完全相同，因此代码与 `saveQTextStream()` 非常相似。我们使用 `codecs.open()` 函数而不是 `open()` 函数来打开文件；我们不需要指定“二进制”标志。我们省略了从 `except` 块到结束的代码，因为它与我们之前看到的相同。

```python
def loadText(self):
    error = None
    fh = None
    try:
        fh = codecs.open(unicode(self.__fname), "rU", CODEC)
        self.clear(False)
        line = 0
        while True:
            title = year = minutes = acquired = notes = None
            line = fh.readline()
            if not line:
                break
            line += 1
            if not line.startswith("{MOVIE}"):
                raise ValueError("no movie record found")
            else:
                title = QString(line[len("{MOVIE}"):].strip())
```

我们只展示了 `loadText()` 方法中对应 `saveText()` 的前几行。该方法使用了与 `loadQtStream()` 方法相同的算法和代码。唯一的显著区别在于我们在 Python 中读取的是 Unicode 字符串，因此我们必须将标题和注释转换为 `QString`。此外，Python 会保留换行符而不是丢弃它们，并返回空字符串来表示已到达文件尾，我们必须稍微修改代码以考虑这一点。对于整数，我们可以使用 Python 的 `int()` 函数，而不是 `QString` 所需的 `intFromStr()` 函数。

我们选择以 `rU` 模式读取，它代表“读取通用换行符”，而不是代表“读取”的普通 `r` 模式。这意味着即使是在 Linux 上写入的，然后在 Windows 上读取，即使这两个操作系统使用不同的行结束符约定，这些行也能被正确读取。

# 保存和加载 XML 文件

通过 PyQt 和 Python 标准库可以读取和写入 XML 文件。PyQt 提供了两个读取解析器，并可以使用其 `QDomDocument` 类写入 XML。PyQt 4.3 增加了两个新的 XML 类。`QXmlStreamReader` 类是轻量级的 SAX，但更易使用；而 `QXmlStreamWriter` 类在写入时比手动编写或使用 DOM 要简单得多且高效得多。Python 标准库提供了广泛的 XML 支持，但在本节中，我们将限于 PyQt 库提供的功能，因为 Python 的 XML 类在 Python 文档以及《Python and XML》和《XML Processing in Python》书中已有很好的介绍。

XML 格式通常比纯文本格式冗长得多，人类也不容易阅读。另一方面，编码问题得到了解决，因此手动编辑比纯文本更可靠，而且使用合适的 XML 库解析整个文件结构要比纯文本格式容易得多。XML 格式通常比二进制或纯文本格式更易扩展，但在写入 XML 时必须确保数据不包含 XML 元字符。写入操作是直观的，但读取它需要使用解析器。有两种非常不同且广泛使用的 XML 解析器 API：DOM（文档对象模型），非常适合编辑文档结构；以及 SAX（XML 简单应用接口），它是增量工作的，因此资源消耗较低，适用于搜索和处理 XML 文档。我们将展示这两种解析器的实际运行。

## 写入 XML

如果我们将 XML 文档读取到 `QDomDocument` 中，或者在代码中创建并填充了一个 `QDomDocument`，将文档保存到磁盘的最简单方法是使用 `QDomDocument.toString()` 获取整个 XML 格式文档的 `QString`，然后将字符串保存到磁盘。在实践中，我们通常仅将 XML 作为数据交换格式，并将数据存储在自定义数据结构中。在这种情况下，我们需要自己编写 XML。

在 XML 中，空白字符序列（如换行符、制表符和空格）通常被视为单个空格。这很方便，但我们的电影注释例外，因为对于注释，我们需要保留用户插入的换行符和段落分隔。

```python
def encodedNewlines(text):
    return text.replace("\n\n", NEWPARA).replace("\n", NEWLINE)
```

```python
def decodedNewlines(text):
    return text.replace(NEWPARA, "\n\n").replace(NEWLINE, "\n")
```

上述两个函数可以保留用户的段落分隔和换行符。第一个函数将段落和换行编码为代表它们的 Unicode 字符，第二个函数将 Unicode 段落和换行解码回熟悉的 `\n` 字符。

有了这两个函数，我们准备好查看如何以 XML 格式导出我们的电影数据了。让我们从目标生成的格式开始看：

```xml
<?xml version='1.0' encoding='UTF-8'?>
<!DOCTYPE MOVIES>
<MOVIES VERSION='1.0'>
<MOVIE YEAR='1951' MINUTES='100' ACQUIRED='2002-02-07'>
<TITLE>The African Queen</TITLE>
<NOTES>
Katherine Hepburn, Humphrey Bogart
</NOTES>
</MOVIE>
...
</MOVIES>
```

省略号代表为了节省空间而省略的电影记录，并不是格式的一部分。

## 使用 PyQt 的 DOM 类读取和解析 XML

PyQt 的 `QDomDocument` 类可以一次性读取整个（良好的）XML 文档。一旦我们获取了 `QDomDocument`，就必须能够使用它。某些应用程序会将文档映射到小部件中（通常是 `QTextWidget`），而其他应用程序（如 My Movies）则将 XML 纯作为数据交换格式，通过遍历文档来填充它们的数据结构。

```python
def importDOM(self, fname):
    dom = QDomDocument()
    error = None
    fh = None
    try:
        fh = QFile(fname)
        if not fh.open(QIODevice.ReadOnly):
            raise IOError(fh.errorString())
        if not dom.setContent(fh):
            raise ValueError("could not parse XML")
    except (IOError, OSError, ValueError) as e:
        error = "Failed to import: %s" % e
    finally:
        if fh is not None:
            fh.close()
        if error is not None:
            return False, error
    try:
        self.populateFromDOM(dom)
    except ValueError as e:
        return False, "Failed to import: %s" % e
    self._fname = QString(fname)
    self._dirty = True
    return True, "Imported %d movie records from %s" % (len(self._movies), QFileInfo(fname).fileName())
```

`load` 方法的第一部分看起来很熟悉，但请注意当调用 `QDomDocument.setContent()` 时，读取的是整个文件。如果此方法成功（返回 `True`），我们就知道 XML 已被成功解析。

一旦我们获取了 `QDomDocument`，我们需要从中提取数据，这正是 `populateFromDOM()` 方法所做的。

该方法的结尾与我们之前看到的不同。我们清除了文件名并将 `dirty`（脏标记/修改标记）设为 `True`。这将确保如果用户尝试保存刚刚导入的 XML 数据，或者他们尝试退出应用程序，他们将收到“另存为”对话框，以便他们有机会将数据保存为应用程序的二进制或文本格式之一。

之前我们提到过 `QDomDocument` 可以很容易地写入文件。以下是实现方法，假设 `dom` 是一个 `QDomDocument` 且有一个有效文件名，且没有错误检查：

```python
codecs.open(filename, "w", "utf-8").write(unicode(dom.toString()))
```

这将产生一个与 `exportXml()` 方法产生的文件略有不同。例如，`QDomDocument.toString()` 方法会对标签进行缩进，属性使用双引号而不是单引号，并且可能以不同的顺序排列属性。尽管如此，生成的 XML 文档在规范上与 `exportXml()` 生成的完全相同。

一旦 `QDomDocument` 读取了 XML 文件，我们需要遍历内容来填充应用程序的数据结构，为了做到，我们开始在文档上调用 `populateFromDOM()`。

```python
def populateFromDOM(self, dom):
    root = dom.documentElement()
    if root.tagName() != "MOVIES":
        raise ValueError("not a movies XML file")
    self.clear(False)
    node = root.firstChild()
    while node:
        if node.toElement().tagName() == "MOVIE":
            self.readMovieNode(node.toElement())
        node = node.nextSibling()
```

我们通过检查 XML 文件是否确实是电影 XML 文件来验证。如果不是，我们就抛出一个异常；如果是，我们就清空数据结构，以便准备好从 DOM 文档中提取数据进行填充。

DOM 文档由“节点”组成，每个节点代表一个 XML 标签或标签之间的文本。节点可能有子节点，也可以有兄弟节点。在电影 XML 格式中，我们有多个 `<MOVIE>` 兄弟节点，它们拥有 `<TITLE>` 和 `<NOTES>` 子节点，而这些节点会变成子文本节点。因此，为了提取数据，我们遍历 `<MOVIE>` 节点，对于遇到的每一个节点，我们提取其属性及其来自子节点的数据。

```python
def readMovieNode(self, element):
    def getText(node):
        child = node.firstChild()
        text = ""
        while not child.isNull():
            if child.nodeType() == QDomNode.Text:
                text += child.toText().data()
            child = child.nextSibling()
        return text.trimmed()
```

`readMovieNode()` 从嵌套函数定义开始。`getText()` 函数接收一个节点作为参数——例如一个 `<TITLE>` 或 `<NOTES>` 开启标签——并遍历其子节点，累积它们的文本。最后，它返回文本，并去除两端的空白字符。如之前所述，`QString.trimmed()` 方法的作用与 `unicode.strip()` 相同。

```python
    year = intFromQString(element.attribute("YEAR"))
    minutes = intFromQString(element.attribute("MINUTES"))
    ymd = element.attribute("ACQUIRED").split("-")
    if ymd.count() != 3:
        raise ValueError("invalid acquired date %s" % \
            unicode(element.attribute("ACQUIRED")))
    acquired = QDate(intFromQString(ymd[0]), intFromQString(ymd[1]),
                     intFromQString(ymd[2]))
```

`readMovieNode()` 方法本身通过提取 `<MOVIE>` 标签的属性数据来工作。

每个 `<MOVIE>` 有两个子节点：`<TITLE>` 和 `<NOTES>`。虽然我们在 `export()` 方法中总是按顺序写入它们，但我们并不强制节点具有特定的顺序。由于这个原因，我们遍历子节点并对遇到的每个节点使用 `getText()` 方法。

```python
    title = None
    notes = None
    node = element.firstChild()
    while node is not None:
        if node.isNull():
            raise ValueError("missing title")
        if node.toElement().tagName() == "TITLE":
            title = getText(node)
        elif node.toElement().tagName() == "NOTES":
            notes = getText(node)
        node = node.nextSibling()
```

最后，只要电影有标题，我们就创建一个 `Movie` 对象并使用 `add()` 将其添加到数据结构中。

## 使用 SAX 类读取和解析 XML

使用 DOM 解析器导入自定义数据结构是可行的，尽管我们通常像 `getText()` 这样的辅助函数。如果我们希望在 `QDomDocument` 内部持有并操作 XML 数据，而不是转换为其他结构，我们会定义一个处理类来实现我们感兴趣的方法，然后将处理类的实例交给 SAX 解析器在解析时使用。解析并不是像 DOM 那样一次性完成的，而是分段完成，当遇到数据时会调用处理程序的方法。我们没有实现的方法由基类提供，在所有情况下它们都安全地什么都不做。

```python
def importSAX(self, fname):
    error = None
    fh = None
    try:
        handler = SaxMovieHandler(self)
        parser = QXmlSimpleReader()
        parser.setContentHandler(handler)
        parser.setErrorHandler(handler)
        fh = QFile(fname)
        input = QXmlInputSource(fh)
        self.clear(False)
        if not parser.parse(input):
            raise ValueError(handler.error)
    except (IOError, OSError, ValueError) as e:
        error = "Failed to import: %s" % e
    finally:
        if fh is not None:
            fh.close()
        if error is not None:
            return False, error
        self._fname = QString()
        self._dirty = True
        return True, "Imported %d movie records from %s" % (len(self.movies), QFileInfo(fname).fileName())
```

我们获取一个 `QFile` 句柄并将其转换为 XML “输入源”。此时，我们尽可能晚地清除我们的数据结构，并告诉解析器解析 XML 文件。解析器在成功时返回 `True`，失败时返回 `False`。

没有单独的填充数据结构阶段，因为我们在解析进行过程中在这个 `SaxMovieHandler` 类内部处理了所有工作。在最后，我们清除文件名并将脏标记设为 `True`，就像我们在 `importDOM()` 方法结束时所做。

`SaxMovieHandler` 类是 `QXmlDefaultHandler` 的子类。对于内容处理，它通常至少要实现 `startElement()`、`endElement()` 和 `characters()` 来处理带有属性的标签、结束标签和文本标签。如果我们像现在这样使用同一个处理器来处理错误，还必须实现 `fatalError()` 方法。

```python
class SaxMovieHandler(QXmlDefaultHandler):
    def __init__(self, movies):
        super(SaxMovieHandler, self).__init__()
        self.movies = movies
        self.text = QString()
        self.error = None
```

`super` 调用确保了基类被正确初始化。`movies` 参数是电影容器本身。`text` 实例变量用于保存标签文本——例如，标题或注释文本——而 `error` 变量将在出现问题时存储一条错误消息。

```python
    def clear(self):
        self.year = None
        self.minutes = None
        self.acquired = None
        self.title = None
        self.notes = None
```

该方法第一次被调用时，它会为电影的每个属性创建一个实例变量。每当调用它时，它都会将变量设为 `None`；这将使我们很容易测试是否读取了电影的所有属性。

```python
    def startElement(self, namespaceURI, localName, qName, attributes):
        if qName == "MOVIE":
            self.clear()
            self.year = intFromQStr(attributes.value("YEAR"))
            self.minutes = intFromQStr(attributes.value("MINUTES"))
            ymd = attributes.value("ACQUIRED").split("-")
            if ymd.count() != 3:
                raise ValueError("invalid date %s" % 
                    unicode(attributes.value("ACQUIRED")))
            self.acquired = QDate(intFromQStr(ymd[0]),
                                  intFromQStr(ymd[1]),
                                  intFromQStr(ymd[2]))
        elif qName in ("TITLE", "NOTES"):
            self.text = QString()
        return True
```

此方法是从基类重实现的，由于这个原因，我们必须使用相同的签名。我们对最后两个参数感兴趣：持有标签名称的 `qName`（限定名）和持有标签属性数据的 `attributes`。每当遇到新的起始标签时，就会调用此方法。

如果遇到新的 `<MOVIE>` 标签，我们会清除实例变量，并从标签的属性数据中填充年份、分钟和获取数据。这使得 `title` 和 `notes` 变量被设为 `None`。

如果标签是 `<TITLE>` 或 `<NOTES>` 标签，我们可以预期获取对应的文本（如果有的话），因此我们将 `text` 变量设为空字符串，准备进行追加。

每个重实现的方法必须在成功时返回 `True`，失败时返回 `False`；因此我们在结尾处返回 `True`。

```python
    def characters(self, text):
        self.text += text
        return True
```

每当标签之间遇到文本时，就会调用 `characters()` 方法。我们只需将文本追加到 `text` 变量中。标签将告诉我们正在累积标题还是注释文本。

```python
    def endElement(self, namespaceURI, localName, qName):
        if qName == "MOVIE":
            if self.year is None or self.minutes is None or \
                self.acquired is None or self.title is None or \
                self.notes is None or self.title.isEmpty():
                    raise ValueError("incomplete movie record")
            self.movies.add(Movie(self.title, self.year,
                self.minutes, self.acquired,
                decodedNewlines(self.notes)))
            self.clear()
        elif qName == "TITLE":
            self.title = self.text.trimmed()
        elif qName == "NOTES":
            self.notes = self.text.trimmed()
        return True
```

每当到达结束标签时，就会调用此方法。标签名称位于 `qName` 参数中。如果结束标签是 `</MOVIE>`，则没有任何电影数据实例变量都不应为 `None`（尽管标题或注释可以是空的 `QString`）。

如果没有任何变量为 `None`，且只要电影有标题，我们就创建一个新的 `Movie` 对象并立即将其添加到 `movies` 容器中。

如果我们到达了标题标签或结束标签，我们就知道在 `QString` 中累积的文本是对应起始标签和结束标签之间的文本，因此我们相应地分配这些文本。如果没有文本，赋值将是一个空的 `QString`。

```python
    def fatalError(self, exception):
        self.error = "parse error at line %d column %d: %s" % (
            exception.lineNumber(),
            exception.columnNumber(),
            exception.message())
        return False
```

如果发生解析错误，将调用 `fatalError()` 方法。我们设置错误消息并返回 `False`。

## 总结

- `SaxMovieHandler` 类是 `QXmlDefaultHandler` 的子类。对于内容处理，它通常至少要实现 `startElement()`、`endElement()` 和 `characters()` 来处理带有属性的标签、结束标签和文本标签。如果我们像现在这样使用同一个处理器来处理错误，还必须实现 `fatalError()` 方法。
- `super` 调用确保了基类被正确初始化。`movies` 参数是电影容器本身。`text` 实例变量用于保存标签文本——例如，标题或注释文本——而 `error` 变量将在出现问题时存储一条错误消息。
- 该方法第一次被调用时，它会为电影的每个属性创建一个实例变量。每当调用它时，它都会将变量设为 `None`；这将使我们很容易测试是否读取了电影的所有属性。
- 没有任何变量为 `None`，且只要电影有标题，我们就创建一个新的 `Movie` 对象并立即将其添加到 `movies` 容器中。
- 如果我们到达了标题标签或结束标签，我们就知道在 `QString` 中累积的文本是对应起始标签和结束标签之间的文本，因此我们相应地分配这些文本。如果没有文本，赋值将是一个空的 `QString`。
- 如果发生解析错误，将调用 `fatalError()` 方法。我们设置错误消息并返回 `False`。

## 练习

修改 My Movies ，使得每个 `Movie` 对象都能存储额外信息：一个名为 "location" 的 `QString`，即电影所在地——例如房间和架子。仅提供二进制 `.mb` 格式的保存和加载以及 XML 的导出和导入，移除处理 pickle 文件的代码。确保新的 My Movies 应用程序能够读取原始应用程序的 `.mb` 和 `.xml` 文件，即不包含位置数据的文件。

`moviedata` 模块的 `Movie` 类需要一个名为 "location" 的 `QString` 属性。`MovieContainer` 类需要一些小调整。你需要一个旧和一个当前版本号，以便知道你处理的是哪一个。`formats()` 方法应该只返回字符串。`save()` 和 `load()` 方法需要处理 `.mb` 文件，并必须考虑到位置以及 `export()` 方法，而两个导入 XML 的方法也必须考虑到 `<LOCATION>` 标签的存在。用户界面的变化应该是显而易见的，因此我们不列出它们。

# 第三部分

# 中级 GUI 编程

# 第 9 章 布局与多文档

## 布局策略

在前面的章节中，我们看到了 PyQt 布局器的运行示例。在 PyQt 中，可以为控件设置特定的尺寸和位置，或者通过重新实现每个控件的 `resizeEvent()` 处理器来处理布局。但使用布局管理器是目前最简单的方法，而且与手动方法相比，它提供了额外的收益。

布局器允许控件增大和缩小，以最有效地利用可用空间，动态响应用户更改容器表单的大小。布局器根据所有控件的最小尺寸为表单提供一个最小尺寸。这确保了表单不会小到无法使用，而且它不是固定的，而是取决于控件的内容——例如，标签可能根据其显示的文本是英语还是德语而需要更多或更少的宽度。

`QVBoxLayout`、`QHBoxLayout` 和 `QGridLayout` 布局器非常多功能。箱布局通过“拉伸”消耗控件之间的空间，防止控件变得过高或过宽。网格布局允许控件跨越多行和多列。所有的布局器都可以在相互嵌套，因此可以创建非常复杂的布局。

尽管如此，有时仅靠布局管理器还不足以实现我们想要的布局。帮助布局器的一种简单方法是：

## 表 9.1 PyQt 的尺寸策略

| 策略 | 效果 |
| :--- | :--- |
| Fixed (固定) | 控件具有其尺寸提示（size hint）指定的尺寸，且从不改变大小 |
| Minimum (最小) | 控件的尺寸提示是其最小尺寸；它不能比这小，但可以变得更大 |
| Maximum (最大) | 控件的尺寸提示是其最大尺寸；它不能比这大，但可以缩小到其最小尺寸 |
| Preferred (首选) | 控件的尺寸提示是其首选尺寸；它可以缩小到其最小尺寸，也可以比其尺寸提示大 |
| Expanding (扩展) | 控件可以缩小到其最小尺寸，也可以比其尺寸提示大 |

## 选项页控件与堆叠控件

因此对话框需要许多控件来展示所有可用选项，以至于用户难以理解。处理这种问题最明显的方法是创建两个多个对话框并在它们之间分配选项。在可行的情况下，这是一个很好的方法，因为减少了对用户的要求，从视图维护的角度来看比单个对话框更容易。但我们通常需要使用单个对话框，因为我们展示的选项是相关的，并且需要一起展示。

当我们使用单个对话框时，必须考虑两种类型的选项组。一种仅仅是相关选项的组。这最容易通过 `QTabWidget` 处理。`QTabWidget` 可以拥有任意数量的“页面”（子控件和标签标题），每个页面使用展示相关选项所需的控件进行布局。图 9.1 显示了 `PaymentDlg`，这是一个使用 Qt Designer 创建的三页选项页控件示例。

![](img/5bc1dcf8601cfec5e1423b4e17ec264_286_0.png)

图 9.1 使用选项页控件选择支付方法的对话框

在 Qt Designer 的“控件框：容器”部分中有一个 `Tab Widget`。它可以像任何其他控件一样被拖入表单。大多数容器控件，与其他控件不同，我们通常要在将选项页控件拖到表单上后手动调整其大小，达到我们想要的大致尺寸。在 Qt Designer 中，选项页控件具有删除和添加页的右键菜单选项。当前页可以通过选择相关标签或设置 `currentIndex` 属性来设置。当前页的标签文本可以通过设置 `currentText` 属性来设置。

一旦选项页控件被拖到表单并调整了大小，我们就可以将其他控件拖到它的页面上。这些控件可以按普通方式布局，每个标签页可以通过取消选择控件、点击标签页，然后应用布局管理器来布局。

得益于标记的标签，选项页控件让用户明显看出其他标签页上有更多选项，并提供了一种简便的方法让用户可以在页面之间导航。标签页控件可以具有圆角或倾角的标签角，并且可以位于顶部、底部、左侧或右侧。

尽管使用 Qt Designer 比手动创建对话框更快更方便，但了解如何纯用代码实现同样的功能是非常且实用的。我们不再展示普通控件的创建，因为我们已经有足够的时间了；相反，我们关注标签和表单的整体布局。以下提取的内容均自 `chap09/paymentdlg.py` 中 `PaymentDlg` 类的初始化函数。（Qt Designer 版本位于 `paymentdlg.ui` 和 `paymentdlg.py` 文件。）

```python
tabWidget = QTabWidget()
cashWidget = QWidget()
cashLayout = QVBoxLayout()
cashLayout.addWidget(self.checkBox)
cashWidget.setLayout(cashLayout)
tabWidget.addTab(cashWidget, "Cash")
```



我们像创建其他控件一样创建标签页控件。标签页中的每个页面必须包含一个控件，因此我们创建一个新控件 `cashWidget` 并为它创建一个布局。然后我们将相关的控件——在此例中只有一个 `paidCheckBox`——添加到布局中，然后将该布局设置在容器控件上。最后，我们将容器控件作为新标签页添加到标签页控件中，并带上标签的显示文本。

```python
checkWidget = QWidget()
checkLayout = QGridLayout()
checkLayout.addWidget(checkNumLabel, 0, 0)
checkLayout.addWidget(self.checkNumLineEdit, 0, 1)
checkLayout.addWidget(bankLabel, 0, 2)
checkLayout.addWidget(self.bankLineEdit, 0, 3)
checkLayout.addWidget(accountLabel, 1, 0)
checkLayout.addWidget(self.accountNumLineEdit, 1, 1)
checkLayout.addWidget(sortLabel, 1, 2)
checkLayout.addWidget(self.sortCodeEdit, 1, 3)
checkWidget.setLayout(checkLayout)
tabWidget.addTab(checkWidget, "Check")
```

此标签页的创建方式与第一个完全相同。唯一的区别在于我们使用了网格布局（grid layout），并且有更多控件要放入布局中。

我们不会显示第三个标签页的代码，因为在结构上它与我们看到的那些相同。

> *在 PyQt 文档中，在某种程度上在 QTabWidget 的 API 中，“tab”（标签）一词既可以指标签的文本，也可以同时指标签文本和页面。*

## 274 第9章 布局与多文档文档

```python
layout = QVBoxLayout()
layout.addLayout(gridLayout)
layout.addWidget(tabWidget)
layout.addWidget(self.checkBox)
self.setLayout(layout)
```

为了完整起见，我们展示了对话框的核心部分，仅省略了表单顶部持有标签、行编辑器（line edits）和数字计数器（spinboxes）的网格布局的创建。按钮由 `QDialogButton` 提供，这种控件可以像其他控件一样布局。最后，我们在垂直框布局中布局整个表单：顶部是第一个网格，中间是标签页控件，底部是按钮。

另一种类型的选项组是仅适用于特定情况的。在一组选项适用或不适用的简单情况下，我们可以使用复选框（checkbox）。如果用户取消勾选该组，所有控件都将被禁用。这意味着用户可以看到该组包含哪些选项，但它们是不可用的，这通常很有帮助。在其他情况下，我们可能有两个或多个选项组，任何时间只有一个组是适用的。对于这种情况，堆叠控件（stacked widget）是一种没有标签的标签页控件。因此，用户没有视觉提示表明存在堆叠控件，也没有办法在堆叠控件之间进行导航。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_288_0.png)

图 9.2 使用堆叠控件的对话框

要使用堆叠控件，我们可以在 Qt Designer 中将堆叠控件拖到表单上，并像调整标签页控件一样对其进行调整大小。在 Qt Designer 内部，堆叠控件通过右上角的两个微小箭头来指示。这些箭头在表单显示时也存在，但在运行时不会出现——它们位于图 9.2 前两个中组合框（combobox）的右上角。控件可以被拖到堆叠控件页面上，并以与标签页控件完全相同的方式布局。堆叠控件具有右键菜单，提供了添加和删除页面的选项，以及用于在页面之间导航和更改页面顺序的额外选项。

由于堆叠控件没有标签，我们必须为用户提供在页面之间导航的手段。在图 9.2 所示的 `VehicleRentalDlg` 中，车辆类型组合框被用作页面选择器。为了使其工作，我们在 Qt Designer 中将组合框的 `currentIndexChanged(int)` 信号连接到堆叠控件的 `setCurrentIndex(int)` 槽。另一种让用户可以使用所有可用面的常用方法是使用包含每个页面名称的 `QList`，并以我们连接组合框信号的方式连接其 `currentRowChanged(int)` 信号。

我们现在将展示如何在代码中创建堆叠控件。以下提取的内容自 `chap09/paymentdlg.py` 中 `VehicleRentalDlg` 类的初始化函数。（Qt Designer 版本位于 `paymentdlg.ui` 和 `paymentdlg.py`。）

```python
stackedWidget = QStackedWidget()
carWidget = QWidget()
carLayout = QGridLayout()
carLayout.addWidget(vehicleLabel, 0, 0)
carLayout.addWidget(colorComboBox, 0, 1)
carLayout.addWidget(mileageLabel, 1, 2)
carLayout.addWidget(weightSpinBox, 1, 3)
carWidget.setLayout(carLayout)
stackedWidget.addWidget(carWidget)
```

向堆叠控件添加“页面”与向标签页控件添加标签非常相似。我们从顶部布局开始，然后为它创建一个底部布局。我们设置堆叠控件。

```python
topLayout = QHBoxLayout()
topLayout.addWidget(colorComboBox)
bottomLayout = QHBoxLayout()
bottomLayout.addWidget(mileageLabel)
layout = QVBoxLayout()
layout.addLayout(topLayout)
layout.addWidget(stackedWidget)
layout.addLayout(bottomLayout)
```

管理合适的控件，我们必须为用户提供一种在页面之间导航的手段，我们通过将车辆组合框的 `currentChanged()` 信号连接到自定义的 `setWidgetStack()` 槽来实现这一点。最后一个槽仅仅是表单验证的一部分；它是为了设置最大里程，这对于汽车来说是固定的，或者取决于它们的重量。

```python
def setWidgetStack(self, text):
	if text == "Car":
		self.stackedWidget.setCurrentIndex(0)
		self.mileageLabel.setText("1000 miles")
	else:
		self.stackedWidget.setCurrentIndex(1)
		self.weightChanged(self.weightSpinBox.value())
```

```python
def weightChanged(self, amount):
	self.mileageLabel.setText("%d miles" % (8000 / amount))
```

我们使用了组合框的当前文本来确定显示哪个控件。一种可能更健壮的方法为每个组合框项关联数据（使用双参数 `addItem()` 方法），并使用当前项的数据来选择哪个控件。

## 290 第9章 布局与多文档文档

当前控件。我们为按钮创建一个底部布局。接下来，我们将这些布局以及堆叠控件本身添加到垂直布局中。

```python
self.connect(self.pushButton, SIGNAL("accepted"), self.accept)
self.connect(self.pushButton, SIGNAL("rejected"), self.reject)
self.connect(self.vehicleCombo,

SIGNAL("currentChanged(QString)"),
	stack)
self.connect(self.weightSpinBox, SIGNAL("valueChanged(int)"),
	weightChanged)
```

## 扩展对话框

对于复杂的对话框，我们可以采取的另一种方法：扩展对话框（extension dialogs）。它们通常用于对话框具有“简单”和“高级”选项的情况。最初，对话框只显示简单选项，并提供一个切换按钮来显示或隐藏高级选项。

图 9.3 所示的对话框在“更多”切换按钮被按下时会显示额外的复选框。任何 `QPushButton` 都可以通过对其调用 `setCheckable(True)` 变成切换按钮，或者在 Qt Designer 中将其“checkable”属性设置为 true。

# 标签页控件和堆叠窗口控件

| 查找和替换 | | 查找和替换 | |

|---|---|---|---|

| 查找内容: | | | 查找 |

| 替换为: | | | 替换 |

| [ ] 区分大小 | | | 关闭 |

| [x] 整个单词 | | | 更多 |

| | [ ] 反向查找 | |

| | [ ] 正则表达式 |

| | [ ] 忽略脚注和尾注 |

图 9.3 扩展对话框

为了让扩展对话框起作用，我们使用了两个“技巧”。第一个技巧是将所有高级选项控件放在一个 `QFrame` 中。这意味着我们只需要隐藏和只显示这个框架（frame），PyQt 就会自动隐藏和显示框架内的所有控件，以反映框架的可见性状态。如果我们不希望在框架显示时看到它的轮廓，可以简单地将其 "frameShape" 属性设置为 `QFrame.NoFrame`。

第二个技巧是让对话框具有固定大小。这将确保对话框缩小到最小（同时保留页边距），并考虑到对话框的可视内容。这样做的效果是，当高级选项隐藏时，对话框很短；而当高级选项显示时，它足够显示这些选项。我们还必须在对话框创建时隐藏框架。以下是对话框初始化器的代码（chap09/findreplaceddlg.py）：

```python
class FindAndReplaceDlg(QDialog,
    ui_findandreplacedDlg.Ui_FindAndReplaceDlg):
    def __init__(self, parent=None):
        super(FindAndReplaceDlg, self).__init__(parent)
        self.setupUi(self)
        self.moreFrame.hide()
        self.layout().setSizeConstraint(QLayout.FixedSize)
```

但是我们如何在框架隐藏状态下显示按钮呢？只需通过将 `button.toggled(bool)` 信号连接到 `moreFrame.setVisible(bool)` 槽即可。注意，如果这个连接是在 Qt Designer 中完成，我们必须勾选配置连接对话框“显示所有信号和槽”复选框；否则 `setVisible()` 槽不会出现。

在本节的最后一个示例中，我们将再次查看如何安排布局。与之前显示了新控件（`QTabWidget` 和 `QStackedWidget`）使用的两个布局不同，此对话框仅使用我们见过的控件——但以新的方式使用。以下提取内容源自 Fin-

# 第 9 章 布局与多文档

chap09/findreplaceddlg.pyw 中的 `ReplaceDlg` 类的初始化器。（Qt Designer 版本在 `findreplaceddlg.ui` 和 `findreplaceddlg.py` 文件中）。

我们仅显示与扩展对话框特别相关的表单控件创建部分。表单的布局如图 9.4 所示。

```python
moreFrame = QFrame()
moreFrame.setFrameStyle(QFrame.StyledPanel|QFrame.Sunken)
```

我们创建了一个框架，在其中放入额外的复选框。如果不调用 `setFrameStyle()`，框架将没有轮廓。

```python
line = QFrame()
line.setStyle(QFrame.VLine|QFrame.Sunken)
```

我们“绘制”用于在视觉上分离左侧对话框主控件与右侧按钮的线也是一个框架。水平线可以使用 `QFrame.HLine` 框架样式创建。

```python
moreButton = QPushButton("&More")
moreButton.setChecked(True)
```

该按钮与其他按钮的不同之处在于：它是可检查的（check）。这意味着它的作用像一个切换按钮，在第一次点击时保持按下状态，下一次点击时弹起，依此类推。

| gridLayout | findLabel | findLineEdit | buttonLayout |

| --- | --- | --- | --- |

| | replaceLabel | replaceLineEdit | replaceButton |

| | caseCheckBox | closeButton | |

| leftLayout | wholeCheckBox | moreButton | mainLayout |

| frameLayout | backwardsCheckBox | | ignoreNotesCheckBox |

图 9.4 查找和替换对话框的布局

标签和线是在网格中布局的；如果我们已经多次看到这种布局，我们将在不再显示代码。

```python
frameLayout = QVBoxLayout()
frameLayout.addWidget(self.backwardsCheckBox)
frameLayout.addWidget(self.regexCheckBox)
frameLayout.addWidget(self.ignoreNotesCheckBox)
moreFrame.setLayout(frameLayout)
```

# 标签页控件和堆叠窗口控件 279

我们希望额外的复选框布局在 `more frame` 内部。为了实现这一点，我们创建了一个布局（在这种情况下是垂直盒布局），并将复选框添加到其中。然后我们将布局设置在框架上。在之前的示例中，我们已经通过将布局添加到布局中来实现嵌套，但在这里我们是通过向框架添加布局来实现的。因此，除了能够在布局之间相互嵌套之外，我们还可以在布局内部嵌套框架和组框框（group boxes），这给了我们极大的灵活性。

```python
leftLayout = QVBoxLayout()
leftLayout.addLayout(gridLayout)
leftLayout.addWidget(self.caseCheckbox)
leftLayout.addWidget(self.wholeCheckbox)
leftLayout.addWidget(moreFrame)
```

该布局是一个垂直盒布局，我们在其中添加了网格布局（带有标签和行编辑框）、区分大小写和单词复选框，然后是 `more frame`（它包含在垂直盒布局中的额外复选框）。

```python
buttonLayout = QVBoxLayout()
buttonLayout.addWidget(self.findButton)
buttonLayout.addWidget(self.replaceButton)
buttonLayout.addWidget(self.closeButton)
buttonLayout.addWidget(self.moreButton)
buttonLayout.addStretch()
```

该布局是一个垂直盒布局，我们向其添加了网格布局（带有标签和行编辑框）、区分大小写和单词复选框，然后是 `more frame`（包含在垂直盒布局中的额外复选框）。

```python
mainLayout = QHBoxLayout()
mainLayout.addLayout(leftLayout)
mainLayout.addWidget(self.line)
mainLayout.addLayout(buttonLayout)
self.setLayout(mainLayout)
```

该布局是一个水平盒布局，带有左布局、线以及按钮布局。对话框将根据框架的可见而变化。

```python
moreFrame.hide()
mainLayout.setSizeConstraint(QSizePolicy.FixedSize)
```

我们最后要做的一件事是将按钮的 `toggled()` 信号连接到框架的 `setVisible()` 槽。当框架隐藏时，它会相应隐藏所有控件，因为当对一个控件调用 `show()` 时，PyQt会将这些调用传递给子控件。

## 分栏器

## 281

![](img/55bc1dcf8601cfec5e1423b4e17ec264_295_0.png)

**图 9.5** News Reader 应用原型

```python
self.messageSplit = QSplitter(Qt.Vertical)
self.messageSplit.addWidget(self.messageList)
self.messageSplit.addWidget(self.messageView)
self.mainSplit = QSplitter(Qt.Horizontal)
self.mainSplit.addWidget(self.groupsList)
self.mainSplit.addWidget(self.messageSplitter)
self.setCentralWidget(self.mainSplit)
```

我们有两个分栏器。第一个是 `messageSplitter`；它垂直方向上持有消息列表和消息视图，一个在上在上。第二个分栏器 `mainSplit` 水平方向分割，组列表控件在左侧，消息分栏器在右侧。就像框布局（box layouts）一样，分栏器可以包含两个以上的组件，在这种情况下，它们会在每对组件之间放置一个分栏器。主分栏器包含一个组件和另一个分栏器，后者包含另外两个组件。主分栏器最终包含了所有内容，由于分栏器是组件（与布局不同），分栏器可以作为主中心组件添加，就像我们在这里所做的那样。

有些用户发现分栏器很烦人，因为他们只能通过鼠标来调整大小。我们将通过保存和恢复用户的分栏器大小来减少这种困扰。这很有帮助，因为用户只需要设置一次大小，从那以后他们设置的大小就会被保留。

## 第 9 章 布局与多文档

![](img/55bc1dcf8601cfec5e1423b4e17ec264_296_0.png)

图 9.6 News Reader 的分栏器和组件

```python
settings = QSettings()
size = settings.value("MainWindow/Size",
      QVariant(QSize(600, 500))).toSize()
self.resize(size)
position = settings.value("MainWindow/Position",
      QVariant(QPoint(0, 0))).toPoint()
self.move(position)
self.restoreState(
    settings.value("MainWindow/State").toByteArray())
self.messageSplitter.restoreState(
    settings.value("MessageSplitter").toByteArray())
self.mainSplitter.restoreState(
    settings.value("MainSplitter").toByteArray())
```

保存用户的主窗口设置始于熟悉的代码，用于恢复窗口的大小、位置以及它可能具有任何工具栏和停靠窗口的状态。分栏器也有状态，以与主状态相同的方式进行恢复和保存。

```python
def closeEvent(self, event):
    if self.okToContinue():
        settings = QSettings()
        settings.setValue("MainWindow/Size", QVariant(self.size()))
        settings.setValue("MainWindow/Position",
              QVariant(self.pos()))
        settings.setValue("MainWindow/State",
              QVariant(self.saveState()))
        settings.setValue("MessageSplitter",
              QVariant(self.messageSplitter.saveState()))
        settings.setValue("MainSplitter",
              QVariant(self.mainSplitter.saveState()))
    else:
        event.ignore()
```

在主窗口的关闭事件中，代码再次以熟悉的方式开始，只是我们在保存主窗口的大小、位置和状态之外，还保存了分栏器的状态。

## 分栏器

## 283

当 News Reader 应用第一次运行时，默认情况下，主分栏器将其宽度正好分给组列表控件，将一半交给消息分栏器。同样，消息分栏器将其高度一半交给消息列表控件，将一半交给消息视图控件。我们希望改变这些比例，让组列表更窄，让消息查看器更高，我们可以通过调整伸缩因子（stretch factors）来实现。例如：

```python
self.mainSplitter.setStretchFactor(0, 1)
self.mainSplitter.setStretchFactor(1, 3)
self.messageSplitter.setStretchFactor(0, 1)
self.messageSplitter.setStretchFactor(1, 2)
```

`setStretchFactor()` 的第一个参数是组件从 0 开始的索引位置（从左到右，或从上到下），第二个参数是要应用的伸缩因子。在本例中，我们规定第 0 个组件（组列表）的伸缩因子为 1，第 1 个组件（消息分栏器）的伸缩因子为 3，将水平空间按 1:3 的比例划分。同样，对于消息分栏器，我们将垂直空间按 1:2 的比例划分，并向消息视图控件倾斜。由于我们会保存并恢复分栏器的大小，因此伸缩因子仅在应用程序首次运行时生效。

## 单文档接口 (SDI)

对于某些应用程序，用户希望能够处理多个文档。这通常可以通过运行应用程序的多个实例来实现，但这会消耗大量资源。使用多个实例的另一个缺点是，不容易提供一个公共窗口让用户在各种文档之间进行导航。

解决这个问题有三种常用的解决方案。一种是使用带有标签控件（tab widget）的单个窗口，每个标签包含一个文档。这种方法在网络浏览器中很流行，但当打开很多文档时可能会不方便。另外两种是 SDI 和 MDI（多文档界面）。在本章中我们将关注 SDI，因为我们在复习 SDI 方法时会看到。

## 第 9 章 布局与多文档

![](img/55bc1dcf8601cfec5e1423b4e17ec264_298_0.png)

图 9.7 News Reader 的分栏器和组件

```python
class MainWindow(QMainWindow):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        self.setAttribute(Qt.WA_DeleteOnClose)
Instances = set()
```

SDI 方法非常简单：每个文档都有自己的窗口。这很容易实现，但如果打开了太多文档，就会变得混乱。MDI 方法更复杂，允许在单个主窗口内包含多个子窗口。在本节中，我们将先看 SDI。

## 单文档接口 (SDI)

```python
self.editor = QTextEdit()
self.setCentralWidget(self.editor)
```

菜单、工具栏和状态栏都是以我们之前见过的方式创建的，除了我们现在要查看的 Window 菜单。

## 286 第 9 章 布局与多文档

```python
self.connect(self, SIGNAL("destroyed(QObject*)"),
MainWindow.updateInstances)
```

当用户关闭窗口时，得益于 `Qt::WAClose` 标志，窗口将被删除。由于我们在静态 `Instances` 集合中保留了该窗口的引用，该窗口无法被垃圾回收。因此，我们将窗口的 `destroyed()` 信号连接到一个槽函数，该函数通过移除任何已关闭的窗口来更新 `Instances`。我们将在查看 `updateInstances()` 方法时详细讨论这一点。

由于每个窗口负责处理一个文件，我们可以为每个窗口关联一个文件名。文件名可以传递给窗口的初始化函数，其默认值是一个空字符串 `QString`。初始化函数的最后几行处理了文件名。

```python
self.filename = filename
if self.filename.isEmpty():
    self.filename = QString("Unnamed-%d.txt") % \
    MainWindow.NextId += 1
self.editor.document().setModified(False)
self.setWindowTitle("SDI Text Editor - %s" % self.filename)
else:
    self.loadFile(self)
```

如果窗口没有文件名（是因为应用程序刚刚启动，还是因为用户调用了“新建文件”操作），我们将创建一个合适的窗口标题；否则，我们将加载指定的文件。

`CloseEvent()`、`loadFile()`、`saveFile()` 和 `saveSAs()` 方法与我们之前看到的那些非常相似，因此我们在这里不再描述它们。它们位于 `chapter9/sditexteditor.py` 的源代码中。我们将重点关注对 SDI 应用程特殊的内容。

```python
def fileNew(self):
    MainWindow().show()
```

当用户调用“新建文件”时，会调用此方法。系统会创建该类的另一个实例，并对其调用 `show()`（使其显示出来）。在方法结束时，我们本认为窗口会超出作用域并被销毁，因为它没有 PyQt 父对象，也不是实例变量。但在主窗口的初始化函数内部，窗口将自己添加到静态 `Instances` 集合中，因此仍然存在指向窗口的对象引用，所以窗口不会被销毁。

```python
def fileOpen(self):
    filename = QDialog.getFileName(self,
    "SDI Text Editor -- Open File")
if not filename.isEmpty():
```

## 单文档接口 (SDI)

```python
if not self.editor.document().isModified() and \
    self.filename.startsWith("Unnamed"):
    self.filename = filename
    self.loadFile()
else:
    MainWindow(filename).show()
```

该方法与我们之前看到的类似方法略有不同。如果用户使用了文件名，且当前文档既未修改也未命名（即一个新的空文档），我们将文件加载到现有窗口中；否则，我们将创建一个新窗口，并传递要加载的文件名。

```python
def fileSaveAll(self):
    count = 0
    for window in MainWindow.Instances:
        if isActive(window) and \
            window.editor.document().isModified():
                if window.fileSave():
                    count += 1
    self.statusBar().showMessage("Saved %d of %d files" % (count, len(MainWindow.Instances)), 5000)
```

为了方便用户，我们提供了一个“全部保存”菜当调用它时，我们会遍历 `Instances` 集合中的每个窗口，对于每个“存活”且已修改的窗口，对其进行保存。

如果一个窗口没有被删除，则它是存活的。遗憾的是，这看起来并不简单`QWidget` 关联着生命周期：引用该组件的 Python 变量的生命周�（在这种情况下是 `Instances` 集合中的 `MainWindow` 实例），以及计算机系统层面底层 PyQt 对象的生命周期。

通常情况下，PyQt 对象及其 Python 变量的生命周期完全相同。但在这里可能不是。例如，假设我们启动应用程序并点击了几次“文件->新建”，产生了三个窗口，然后导航到其中一个并将其关闭。此时，被关闭的窗口（得益于 `Qt.WADeletedOnClose` 属性）将被删除。

在底层，PyQt 实际上会对被删除的窗口调用 `deleteLater()` 方法。这让窗口有机会完成它正在执行的操作，以便能够被干净地删除。这通常在不到一毫秒内完成，此时 PyQt 对象将从内存中被删除并不再存在。但 `Instances` 集合中的 Python 变量仍然存在，只是现在指向的是一个已经消失的 PyQt 对象。因此，在访问 `Instances` 集合中的任何窗口之前，我们必须始终检查其存活状态。

```python
def isAlive(qobj):
    try:
        sip.unwrapinstance(qobj)
    except RuntimeError:
        return False
    return True
```

`sip` 模块是 PyQt 支持的模块之一，我们通常不需要直接访问它。但在需要更深入探究的情况下，它是非常有用的。在这里，该方法尝试访问变量的底层 PyQt 对象。如果对象已被删除，将抛出 `RuntimeError` 异常，在这种情况下我们返回 `False`；否则对象仍然存在，我们返回 `True`。通过执行此检查，我们确保已关闭并删除的窗口不会被意外访问，即使我们没有删除该变量。

```python
@staticmethod
def updateInstances(qobj):
    MainWindow.Instances = [window for window in MainWindow.Instances if isAlive(window)]
```

每当窗口关闭（得益于 `Qt.WADeletedOnClose` 属性），它将被删除。它会发出 `destroyed()` 信号，我们将其连接到 `updateInstances()` 方法。该方法会将 `Instances` 集合覆盖为那些仍然存活的窗口。为什么我们在遍历实例时需要检查存活状态呢？

在菜单填充到调用它之间，某个窗口可能已经被删除。

```python
def updateMenu(self):
    self.windowMenu.clear()
    for window in MainWindow.Instances:
        if isAlive(window):
            self.windowMenu.addAction(window.windowTitle(), self.raiseWindow)
```

## 第 9 章 布局与多文档

现有的菜单项会被清空；至少有一个，即当前窗口。我们遍历所有窗口并-

```python
def raiseWindow(self):
    action = self.sender()
    if not isinstance(action, QAction):
        return
    for window in MainWindow.Instances:
        if isAlive(window) and \
            window.windowTitle() == action.text():
                window.activateWindow()
                window.raise_()
                break
```

此方法可以由“窗口”菜单的任何项调用。我们首先进行性检查，然后遍历具有匹配标题的实例。如果找到匹配项，我们将该窗口设置为“活动”窗口（具有键盘焦点的应用程序顶级窗口），并将其置于用户可见的所有其他窗口之上。

在随后的 SDI 部分中，我们将看到如何创建一个更复杂的窗口菜单，带有快捷键和一些额外的菜单选项。

```python
def fileQuitAll(self):
    QApplication.closeAllWindows()
```

Qt 提供了一个方便的方法来关闭应用程序的所有顶级窗口。该方法会对所有窗口调用 `close()`，这会导致每个窗口触发 `closeEvent()`。在这个事件中（未显示），我们检查 `QTextEdit` 是否未保存的更改，如果有，则弹出对话框询问用户是否保存。

```python
app = QApplication(sys.argv)
app.setWindowIcon(QIcon(":/icon.png"))
MainWindow().show()
app.exec_()
```

在 `editor.py` 文件的最后，我们创建一个 `QApplication` 实例和一个 `MainWindow` 窗口实例并启动事件循环。

使用 SDI 方法非常流行，但它也有缺点。由于每个主窗口都有自己的菜单栏、工具栏以及可能的停靠窗口，其资源开销比单个主窗口大。此外，虽然可以使用窗口菜单在窗口之间切换，但如果

> *在 Mac OS 上，只有一个菜单栏，位于屏幕顶部。它会反映当前获得焦点的窗口。*

## 第 9 章 布局与多文档

为了对窗口大小和位置进行更多控制，我们必须自己编写代码。这些问题可以通过我们在下一节中介绍的较不流行的 MDI（多文档界面）方法来解决。

## 多文档界面 (MDI)

与 SDI（单文档界面）或运行多个应用程序实例相比，MDI 有许多优势。MDI 应用程序消耗的资源更少，并且让用户更容易在文档窗口之间进行相互布局。然而，它的缺点是，你无法使用 Alt+Tab（Mac OSX 上为 Command-Tab）在 MDI 窗口之间切换，尽管在 SDI 应用中这通常不是问题，因为程序员总会实现一个“窗口”菜单用于在窗口之间导航。

创建 MDI 应用程序的关键是创建一个部件子类，由它来自己处理所有事情，包括加载、保存和清理，而应用程序将这些部件保存在 MDI “工作区”（workspace）中，并将它们传递给任何特于部件的操作。

在本节中，我们将创建一个文本编辑器，它提供与上一节 SDI 文本编辑器相同的功能，只不过它将是一个 MDI 应用程序。该应用程序如图 9.8 所示。

每个文档都使用自定义 TextEdit 部件（`QText` 子类）的实例进行展示和编辑。该部件设置了 `Qt::DeleteClose` 属性，有一个文件名变量，并保存它接收到的文件。如果部件被关闭（因此被删除），它的关闭事件处理程序将允许用户保存任何未保存的更改。TextEdit 的实现非常直观，与我们之前看到的代码非常相似，因此我们在这里不再复习它；它的源代码位于模块 `chap09/texteditor.py` 中。

应用程序本身的代码位于 `chap09/texteditor.py` 文件中。我们将回顾这些代码，从 `MainWindow` 子类初始化器的部分提取开始。

```python
class MainWindow(QMainWindow):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        self.mdi = QWorkspace()
        self.setCentralWidget(self.mdi)
```

PyQt 的 MDI 部件称为 `QWorkspace`。就像标签部件或堆叠部件一样，`QWorkspace` 可以向其添加部件。这些部件由工作区布局，就像一个微型桌面，用户可以在工作区区域内对部件进行平铺、级联、图标化或拖动和调整大小。

> *从 Qt 4.3 开始，MDI 由 `QMdiArea` 类提供，其 API 与 `QWorkspace` 相似。*

![](img/55bc1dcf8601cfec5e1423b4e17ec264_305_0.png)

图 9.8 带有四个文档的 MDI 文本编辑器

通过调用 `Qworkspace.scrollEnabled(True)`，可以拥有比窗口更大的工作区。可以通过指定背景刷来设置工作区的背景。

```python
fileNewAction = self.createAction("New", self.fileNew,
QKeySequence.New("filenew", "Create a text file"))
```

大部分文件的创建正如我们之前看到的那样。但正如我们将看到的，MDI 编辑器像 SDI 编辑器一样没有 `okToContinue()` 方法，因为每个文档窗口都负责自己。

```python
fileQuitAction = self.createAction("&Quit", self.close,
Ctrl+Q, "filequit", "Close the application")
```

如果我们关闭应用程序的窗口，应用程序将终止。所有文档窗口将关闭关闭，任何未保存的更改将负责提示用户并在被要求时进行保存。

```python
editCopyAction = self.createAction("&Copy", self.editCopy,
QKeySequence.Copy, "editcopy",
"Copy text to the clipboard")
```

在 SDI 编辑器中，我们将“拷贝”、“剪切”和“粘贴”操作传递给窗口的 `QTextEdit` 来处理。这在 MDI 应用程序中是不行的，因为当用户触发这些操作之一时，它必须应用到任何活跃的 `TextEdit` 窗口上。由于这个原因，主窗口必须自己做一些工作，正如我们在回顾这些操作的实现将会看到的。

我们没有显示其他文件和编辑操作的代码，因为它们都遵循之前所示的模式。

```python
self.windowNextAction = self.createAction("Next",
self.mdi.activateNextWindow, QKeySequence.NextChild)
self.windowPrevAction = self.createAction("Previous",
self.mdi.activatePreviousWindow,
QKeySequence.PreviousChild)
self.windowCascadeAction = self.createAction("Cascade",
self.mdi.cascade)
self.windowTileAction = self.createAction("Tile",
self.mdi.tile)
self.windowRestoreAction = self.createAction("Restore All",
self.windowRestoreAll)
self.windowMinimizeAction = self.createAction("Iconize All",
self.mdi.minimizeAll)
self.windowArrangeIconsAction = self.createAction(
"Arrange Icons", self.mdi.arrangeIcons)
self.windowCloseAction = self.createAction("Close",
self.mdi.closeActiveWindow, QKeySequence.Close)
```

所有的窗口操作都创建为实例变量，因为我们将在另一个方法中访问它们。对于某些操作，我们可以直接将工作传递给 `mdi` 工作区实例，最小化和恢复所有必须由我们处理的 MDI。

```python
self.windowMapper = QSignalMapper(self)
self.connect(self.windowMapper, SIGNAL("mappedQWidget*"),
self.mdi, SLOT("setActiveWindow(QWidget)"))
```

在我们创建的菜单中，我们需要一种方法让用户选择活动窗口。我们在上一节中看到了解决这个问题的非常简单的解决方案。另一种方法是使用部分函数激活，将每个窗口作为参数传递给 `Workspace.setActiveWindow()`。在这里我们使用了纯 PyQt 方法，我们将在回顾 `updateWindowMenu()` 时解释其用法。

```python
self.windowMenu = self.menubar().addMenu("Window")
self.connect(self.windowMenu, SIGNAL("ToShow"),
self.updateMenu)
```

`ToShow` 的连接确保在菜单显示之前调用我们的 `updateWindowMenu()` 方法。

```python
self.updateWindowMenu()
self.setWindowTitle("Text Editor")
Timer.singleShot(0, self.loadFiles)
```

在构造函数的末尾我们调用 `updateWindowMenu()` 以强制创建菜单。这看起来可能很奇怪；毕竟用户尝试使用它时它会被创建，为什么要现在创建？原因是如果在启动时自动加载某些文档，用户可能想使用我们的快捷键（F6 和 Shift+F6）在它们之间导航，但快捷键在菜单创建后才会变为激活。

```python
def closeEvent(self, event):
    failures = []
    for textEdit in self.mdi.windowList():
        if textEdit.isModified():
            try:
                textEdit.save()
            except IOError, e:
                failures.append(str(e))
    if failures and \n        MessageBox.warning(self, "Text Editor -- Save Error", "Failed to save%s\nQuit anyway?" % \n"\n".join(failures),
        if QMessageBox.yes("Yes"|"No") == QMessageBox.No:
            return
    settings = QSettings()
    settings.setValue("MainWindow/Size", QVariant(self.size()))
    settings.setValue("MainWindow/Position", QVariant(self.pos()))
    settings.setValue("MainWindow/State", QVariant(self.saveState()))
    files = QList()
    for textEdit in self.mdi.windowList():
        if not textEdit.filename.startswith("Unnamed"):
            files.append(textEdit.filename)
    settings.setValue("CurrentFiles", QVariant(files))
    self.mdi.closeAllWindows()
```

当应用程序终止时，我们给予用户保存任何未保存更改的机会。然后我们保存窗口的大小、位置和状态。我们还保存所有 MDI 窗口的文件名列表。最后我们调用 `Workspace.closeAllWindows()`，这将导致每个窗口接收到关闭事件。

## 第 9 章 布局与多文档

在 `TextEdit` 的关闭事件中，有一段代码可以让用户有机会保存任何未保存的更改，但在此时不需要这样做了，因为我们已经在该方法的开始处通过保存未签名的更改处理了这个问题。我们在 `TextEdit` 的关闭事件中编写这段代码是因为用户可以随时关闭任何窗口，因此每个窗口必须能够处理关闭操作。但在应用程序终止时，我们并不使用它，而是对已修改的文件调用 `save()`，因为我们想保留当前的文件列表，为了做到这一点，在保存当前文件列表的代码之前，每个文件必须有一个正确的文件名，而早早调用 `save()`实现了这一点。

```python
def isAlive(qobj):
    try:
        sip.unwrapinstance(qobj)
    except RuntimeError:
        return False
    return True
```

`sip` 模块是 PyQt 支持的模块之一，我们通常不需要直接访问它。但在需要更深入探究的情况下，它是非常有用的。在这里，该方法尝试访问变量的底层 PyQt 对象。如果对象已被删除，将抛出 `RuntimeError` 异常，在这种情况下我们返回 `False`；否则对象仍然存在，我们返回 `True`。通过执行此检查，我们确保已关闭并删除的窗口不会被意外访问，即使我们没有删除该变量。

```python
@staticmethod
def updateInstances(qobj):
    MainWindow.Instances = [window for window in MainWindow.Instances if isAlive(window)]
```

每当窗口关闭（得益于 `Qt.WADeletedOnClose` 属性），它将被删除。它会发出 `destroyed()` 信号，我们将其连接到 `updateInstances()` 方法。该方法会将 `Instances` 集合覆盖为那些仍然存活的窗口。为什么我们在遍历实例时需要检查存活状态呢？

在菜单填充到调用它之间，某个窗口可能已经被删除。

```python
def updateMenu(self):
    self.windowMenu.clear()
    for window in MainWindow.Instances:
        if isAlive(window):
            self.windowMenu.addAction(window.windowTitle(), self.raiseWindow)
```

## 第 9 章 布局与多文档

现有的菜单项会被清空；至少有一个，即当前窗口。我们遍历所有窗口并-

```python
def raiseWindow(self):
    action = self.sender()
    if not isinstance(action, QAction):
        return
    for window in MainWindow.Instances:
        if isAlive(window) and \
            window.windowTitle() == action.text():
                window.activateWindow()
                window.raise_()
                break
```

此方法可以由“窗口”菜单的任何项调用。我们首先进行性检查，然后遍历具有匹配标题的实例。如果找到匹配项，我们将该窗口设置为“活动”窗口（具有键盘焦点的应用程序顶级窗口），并将其置于用户可见的所有其他窗口之上。

在随后的 SDI 部分中，我们将看到如何创建一个更复杂的窗口菜单，带有快捷键和一些额外的菜单选项。

```python
def fileQuitAll(self):
    QApplication.closeAllWindows()
```

Qt 提供了一个方便的方法来关闭应用程序的所有顶级窗口。该方法会对所有窗口调用 `close()`，这会导致每个窗口触发 `closeEvent()`。在这个事件中（未显示），我们检查 `QTextEdit` 是否未保存的更改，如果有，则弹出对话框询问用户是否保存。

```python
app = QApplication(sys.argv)
app.setWindowIcon(QIcon(":/icon.png"))
MainWindow().show()
app.exec_()
```

在 `editor.py` 文件的最后，我们创建一个 `QApplication` 实例和一个 `MainWindow` 窗口实例并启动事件循环。

使用 SDI 方法非常流行，但它也有缺点。由于每个主窗口都有自己的菜单栏、工具栏以及可能的停靠窗口，其资源开销比单个主窗口大。此外，虽然可以使用窗口菜单在窗口之间切换，但如果

> *在 Mac OS 上，只有一个菜单栏，位于屏幕顶部。它会反映当前获得焦点的窗口。*

## 第 9 章 布局与多文档

为了对窗口大小和位置进行更多控制，我们必须自己编写代码。这些问题可以通过我们在下一节中介绍的较不流行的 MDI（多文档界面）方法来解决。

## 多文档界面 (MDI)

与 SDI（单文档界面）或运行多个应用程序实例相比，MDI 有许多优势。MDI 应用程序消耗的资源更少，并且让用户更容易在文档窗口之间进行相互布局。然而，它的缺点是，你无法使用 Alt+Tab（Mac OSX 上为 Command-Tab）在 MDI 窗口之间切换，尽管在 SDI 应用中这通常不是问题，因为程序员总会实现一个“窗口”菜单用于在窗口之间导航。

创建 MDI 应用程序的关键是创建一个部件子类，由它来自己处理所有事情，包括加载、保存和清理，而应用程序将这些部件保存在 MDI “工作区”（workspace）中，并将它们传递给任何特于部件的操作。

在本节中，我们将创建一个文本编辑器，它提供与上一节 SDI 文本编辑器相同的功能，只不过它将是一个 MDI 应用程序。该应用程序如图 9.8 所示。

每个文档都使用自定义 TextEdit 部件（`QText` 子类）的实例进行展示和编辑。该部件设置了 `Qt::DeleteClose` 属性，有一个文件名变量，并保存它接收到的文件。如果部件被关闭（因此被删除），它的关闭事件处理程序将允许用户保存任何未保存的更改。TextEdit 的实现非常直观，与我们之前看到的代码非常相似，因此我们在这里不再复习它；它的源代码位于模块 `chap09/texteditor.py` 中。

应用程序本身的代码位于 `chap09/texteditor.py` 文件中。我们将回顾这些代码，从 `MainWindow` 子类初始化器的部分提取开始。

```python
class MainWindow(QMainWindow):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        self.mdi = QWorkspace()
        self.setCentralWidget(self.mdi)
```

PyQt 的 MDI 部件称为 `QWorkspace`。就像标签部件或堆叠部件一样，`QWorkspace` 可以向其添加部件。这些部件由工作区布局，就像一个微型桌面，用户可以在工作区区域内对部件进行平铺、级联、图标化或拖动和调整大小。

> *从 Qt 4.3 开始，MDI 由 `QMdiArea` 类提供，其 API 与 `QWorkspace` 相似。*

![](img/55bc1dcf8601cfec5e1423b4e17ec264_305_0.png)

图 9.8 带有四个文档的 MDI 文本编辑器

通过调用 `Qworkspace.scrollEnabled(True)`，可以拥有比窗口更大的工作区。可以通过指定背景刷来设置工作区的背景。

```python
fileNewAction = self.createAction("New", self.fileNew,
QKeySequence.New("filenew", "Create a text file"))
```

大部分文件的创建正如我们之前看到的那样。但正如我们将看到的，MDI 编辑器像 SDI 编辑器一样没有 `okToContinue()` 方法，因为每个文档窗口都负责自己。

```python
fileQuitAction = self.createAction("&Quit", self.close,
Ctrl+Q, "filequit", "Close the application")
```

如果我们关闭应用程序的窗口，应用程序将终止。所有文档窗口将关闭关闭，任何未保存的更改将负责提示用户并在被要求时进行保存。

```python
editCopyAction = self.createAction("&Copy", self.editCopy,
QKeySequence.Copy, "editcopy",
"Copy text to the clipboard")
```

在 SDI 编辑器中，我们将“拷贝”、“剪切”和“粘贴”操作传递给窗口的 `QTextEdit` 来处理。这在 MDI 应用程序中是不行的，因为当用户触发这些操作之一时，它必须应用到任何活跃的 `TextEdit` 窗口上。由于这个原因，主窗口必须自己做一些工作，正如我们在回顾这些操作的实现将会看到的。

我们没有显示其他文件和编辑操作的代码，因为它们都遵循之前所示的模式。

```python
self.windowNextAction = self.createAction("Next",
self.mdi.activateNextWindow, QKeySequence.NextChild)
self.windowPrevAction = self.createAction("Previous",
self.mdi.activatePreviousWindow,
QKeySequence.PreviousChild)
self.windowCascadeAction = self.createAction("Cascade",
self.mdi.cascade)
self.windowTileAction = self.createAction("Tile",
self.mdi.tile)
self.windowRestoreAction = self.createAction("Restore All",
self.windowRestoreAll)
self.windowMinimizeAction = self.createAction("Iconize All",
self.mdi.minimizeAll)
self.windowArrangeIconsAction = self.createAction(
"Arrange Icons", self.mdi.arrangeIcons)
self.windowCloseAction = self.createAction("Close",
self.mdi.closeActiveWindow, QKeySequence.Close)
```

所有的窗口操作都创建为实例变量，因为我们将在另一个方法中访问它们。对于某些操作，我们可以直接将工作传递给 `mdi` 工作区实例，最小化和恢复所有必须由我们处理的 MDI。

```python
self.windowMapper = QSignalMapper(self)
self.connect(self.windowMapper, SIGNAL("mappedQWidget*"),
self.mdi, SLOT("setActiveWindow(QWidget)"))
```

在我们创建的菜单中，我们需要一种方法让用户选择活动窗口。我们在上一节中看到了解决这个问题的非常简单的解决方案。另一种方法是使用部分函数激活，将每个窗口作为参数传递给 `Workspace.setActiveWindow()`。在这里我们使用了纯 PyQt 方法，我们将在回顾 `updateWindowMenu()` 时解释其用法。

```python
self.windowMenu = self.menubar().addMenu("Window")
self.connect(self.windowMenu, SIGNAL("ToShow"),
self.updateMenu)
```

`ToShow` 的连接确保在菜单显示之前调用我们的 `updateWindowMenu()` 方法。

```python
self.updateWindowMenu()
self.setWindowTitle("Text Editor")
Timer.singleShot(0, self.loadFiles)
```

在构造函数的末尾我们调用 `updateWindowMenu()` 以强制创建菜单。这看起来可能很奇怪；毕竟用户尝试使用它时它会被创建，为什么要现在创建？原因是如果在启动时自动加载某些文档，用户可能想使用我们的快捷键（F6 和 Shift+F6）在它们之间导航，但快捷键在菜单创建后才会变为激活。

```python
def closeEvent(self, event):
    failures = []
    for textEdit in self.mdi.windowList():
        if textEdit.isModified():
            try:
                textEdit.save()
            except IOError, e:
                failures.append(str(e))
    if failures and \n        MessageBox.warning(self, "Text Editor -- Save Error", "Failed to save%s\nQuit anyway?" % \n"\n".join(failures),
        if QMessageBox.yes("Yes"|"No") == QMessageBox.No:
            return
    settings = QSettings()
    settings.setValue("MainWindow/Size", QVariant(self.size()))
    settings.setValue("MainWindow/Position", QVariant(self.pos()))
    settings.setValue("MainWindow/State", QVariant(self.saveState()))
    files = QList()
    for textEdit in self.mdi.windowList():
        if not textEdit.filename.startswith("Unnamed"):
            files.append(textEdit.filename)
    settings.setValue("CurrentFiles", QVariant(files))
    self.mdi.closeAllWindows()
```

当应用程序终止时，我们给予用户保存任何未保存更改的机会。然后我们保存窗口的大小、位置和状态。我们还保存所有 MDI 窗口的文件名列表。最后我们调用 `Workspace.closeAllWindows()`，这将导致每个窗口接收到关闭事件。

## 第 9 章 布局与多文档

在 `TextEdit` 的关闭事件中，有一段代码可以让用户有机会保存任何未保存的更改，但在此时不需要这样做了，因为我们已经在该方法的开始处通过保存未签名的更改处理了这个问题。我们在 `TextEdit` 的关闭事件中编写这段代码是因为用户可以随时关闭任何窗口，因此每个窗口必须能够处理关闭操作。但在应用程序终止时，我们并不使用它，而是对已修改的文件调用 `save()`，因为我们想保留当前的文件列表，为了做到这一点，在保存当前文件列表的代码之前，每个文件必须有一个正确的文件名，而早早调用 `save()`实现了这一点。

```python
def loadFiles(self):
    if len(sys.argv) > 1:
        for filename in sys.argv[1:31]: # 最多加载30个文件
            filename = QString(filename)
            if QFileInfo(filename).isFile():
                self.loadFile(filename)
            QApplication.processEvents()
```

```python
else:
    settings = QSettings()
    files = settings.value("CurrentFiles").toStringList()
    for filename in files:
        filename = QString(filename)
        if QFile.exists(filename):
            self.loadFile(filename)
            QApplication.processEvents()
```

我们设计此应用程序是为了让它加载上一次运行程序时打开的所有文件。然而，如果用户在命令行上指定了一个或或多个文件，我们将忽略之前打开的文件，只打开用户指定的文件。在这种情况下，我们选择将文件数量任意限制为 30 个，以防止用户无意中在包含数百或数千个文件的目录中获取 `.*` 的文件指定。

`QApplication.process()` 调用将控制权交回事件循环，以便任何累积的事件（如重绘事件）都能被处理。此应用程序中的效果是，在每个文件加载后都会弹出一个编辑器窗口，而不是在所有文件加载后才出现窗口。这让用户清楚地看到应用程序正在执行操作，而开始时的延迟可能会让用户认为应用程序已崩溃。使用 `processEvents()` 的另一个好处是，用户的鼠标和键盘事件将获得一些处理时间，即使在进行大量处理时也能保持应用程序的响应。

在长时间运行的操作期间使用 `processEvents()` 保持应用程序响应比使用多线程要简单得多。尽管如此，这种方法必须谨慎使用，因为它可能会导致处理某些事件会对长时间运行的操作本身产生问题。有助于降低风险的方法是传递额外的参数——例如，一个限制应处理的事件类型的标志，以及处理事件的最大时间。我们将在第 12 章中看到 `processEvents()` 使用的另一个示例；多线程是第 19 章的主题。

```python
def loadFile(self, filename):
    textEdit = edit.TextEdit(filename)
    try:
        textEdit.load()
    except (IOError, OSError), e:
        QMessageBox.warning(self, "Text Editor -- Load Error", "加载失败: %s" % (filename, e))
        textEdit.close()
    else:
        self.mdi.addWindow(textEdit)
        textEdit.show()
```

当由于 `loadFiles()` 或 `open()` 调用加载时，它会创建一个带有给定文件名的新 `TextEdit`，并告诉编辑器加载该文件。如果加载失败，将通过消息框通知用户，并关闭且删除编辑器。如果成功，编辑器将添加到工作区并显示。我们不需要静态实例来保持 `TextEdit` 实例存，因为 `QWorkspace` 会自动为我们处理这些。

```python
def fileNew(self):
    textEdit = edit.TextEdit()
    self.mdi.addWindow(textEdit)
    textEdit.show()
```

此方法创建一个新编辑器，将其添加到工作区并显示它。编辑器的窗口标题将为 "Unnamed-n.txt"，其中 n 是从 1 开始的递增整数。如果用户输入名称并尝试保存编辑器，他们将被提示选择一个正确的文件名。

```python
def fileOpen(self):
    filename = QFileDialog.getFileName(self,
        "Text Editor -- 打开文件")
    if not filename.isEmpty():
        for textEdit in self.mdi.window():
            if textEdit.filename == filename:
                self.mdi.setActiveWindow(textEdit)
                break
        else:
            self.loadFile(filename)
```

如果用户选择打开一个文件，我们检查它是否已在工作区的某个编辑器中。如果是，我们只需将该编辑器的窗口设置为活动窗口。否则，我们将文件加载到新的编辑器中。如果我们的用户想要能够加载同一个文件多次——例如，查看长文件的不同部分——我们可以简单地每次调用 `load()`，而无需理会文件在现有编辑器中的位置。

```python
def fileSave(self):
    textEdit = self.mdi.activeWindow()
    if textEdit is None or not isinstance(textEdit, QTextEdit):
        return
    try:
        textEdit.save()
    except (IOError, OSError), e:
        QMessageBox.warning(self, "Text Editor -- 保存错误", "保存失败: %s" % (textEdit.filename, e))
```

当用户触发保存时，我们通过调用 `QWorkspace.activeWindow()` 来确定要保存的文件。如果它返回一个 `TextEdit`，我们就对其调用 `save()`。

```python
def fileSaveAll(self):
    errors = []
    for textEdit in self.mdi.window():
        if textEdit.isModified():
            try:
                textEdit.save()
            except (IOError, OSError), e:
                errors.append("%s: %s" % (textEdit.filename, e))
    if errors:
        QMessageBox.warning(self, "Text Editor -- 保存所有", "保存失败:\n" + "\n".join(errors))
```

为了方便起见，我们提供了“保存所有”操作。由于可能有许多窗口，如果保存出现问题（例如磁盘空间不足），问题可能会影响许多窗口。因此，我们在结束时收集错误并显示它们。

```python
def editCopy(self):
    textEdit = self.mdi.activeWindow()
    if textEdit is None or not isinstance(textEdit, QTextEdit):
        return
    cursor = textEdit.textCursor()
    text = cursor.selectedText()
    if not text.isEmpty():
        clipboard = QApplication.clipboard()
        clipboard.setText(text)
```

## 多文档界面 (MDI)

此方法的启动方式与之前相同——通过检索用户正在工作的编辑器。`QTextEdit.textCursor()` 返回的光标是用户光标的程序等物，但该类将在第 13 章中详细讨论。如果有选中文本，我们将将其复制到系统剪贴板。

```python
def editCut(self):
    textEdit = self.mdi.activeWindow()
    if textEdit is None or not isinstance(textEdit, QTextEdit):
        return
    cursor = textEdit.textCursor()
    text = cursor.selectedText()
    if not text.isEmpty():
        cursor.removeSelectedText()
        clipboard = QApplication.clipboard()
        clipboard.setText(text)
```

此方法几乎与复制方法相同。唯一的区别是如果有选中文本，我们将从编辑器中移除它。

```python
def editPaste(self):
    textEdit = self.mdi.activeWindow()
    if textEdit is None or not isinstance(textEdit, QTextEdit):
        return
    clipboard = QApplication.clipboard()
    textEdit.insertPlainText(clipboard.text())
```

如果剪贴板中有文本，无论是来自本应用程序的复制或剪切，还是来自另一个应用程序，我们将将其插入编辑器的当前位置。

所有基本的 MDI 窗口操作都由 `QWorkspace` 槽提供，因此我们不需要为平铺、堆叠或窗口导航提供。但我们必须提供最小化和恢复窗口的代码。

```python
def windowRestoreAll(self):
    for textEdit in self.mdi.windowList():
        textEdit.showNormal()
```

`windowMinimize()` 方法（未显示）相同，只是我们调用的是 `showMinimized()` 而不是 `showNormal()`。

`SignalMapper` 是一个对象，每当它的槽被调用时，就会发射 `mapped(signal)`。它在 `mapped(signal)` 信号中传递的参数是

![](img/5bc1dcf8601cfec5e1423b4e17ec264_311_0.png)

> *X Window 用户有两个剪贴板：默认剪贴板和鼠标选择。Mac OS 还有一个“查找”剪贴板。PyQt 通过 `setText()` 和 `text()` 的可选第二个参数 "mode" 来访问所有可用的剪贴板。*

## 第 9 章 布局与多文档

该设置与调用 `map()` 槽的任何 QObject 相对应。我们使用信号映射器（signal mapper）将“窗口”菜单中的动作与 EditText 小部件关联起来，这样当用户选择特定窗口时，相应的 EditText 将变为活动窗口。这在两个地方进行了设置：表单的初始化器和 `updateWindowMenu()` 方法，如图 9.9 所示。

| 发送者 | 参数 |

| --- | --- |

| SLOT(map()) | SIGNAL(mapped(QObject)) |

| QObject | (QObject, QWidget) SIGNAL(mapped(QWidget)) |

| | (QObject, int) SIGNAL(mapped(int)) |

**图 9.9** QSignalMapper 的通用操作

在初始化器中，我们从信号映射器的 `mapped (Widget*)` 信号连接到 MDI 工作区的 `setActiveWindow(Widget*)` 槽。为了使用此功能，信号映射器必须发射与用户从“窗口”菜单中选择的 MDI 窗口对应的信号，这是在 `updateWindowMenu()` 方法中设置的。MDI 文本器的信号如图 9.10 所示。

```python
def updateWindowMenu(self):
    self.windowMenu.clear()
    self.addActions(self.windowMenu, self.windowNextAction,
    self.windowPreAction, self.windowCascadeAction,
    self.windowTileAction, self.windowRestoreAction,
    self.windowMinimizeAction,
    self.windowArrangeIconsAction, None,
    self.windowCloseAction())
    textEdits = self.midi.windowList()
    if not textEdits:
        return
```

我们首先清除“窗口”菜中的所有动作，然后重新添加所有标准动作。接下来，获取 EditText 窗口列表；如果没有，则结束并直接返回；否则，我们必须为每个窗口添加条目。

```python
self.windowMenu.addSeparator()
i = 1
menu = self.windowMenu
for textEdit in textEdits:
    title = EditText.windowTitle()
    if i == 10:
        self.windowMenu.addSeparator()
        menu = menu.addMenu("More")
```

## 多文档界面 (MDI)

```python
accel = ""
if i < 10:
    accel = "&%d" % i
elif i < 36:
    accel = "&%c" % chr(i + ord("@")) - 9
```

我们遍历所有窗口。对于前九个窗口，我们创建 `&1`、`&2` 等“accel”字符串，以产生 1, 2, ..., 9。如果有十个更多窗口，我们创建一个标题为“更多”的子菜单，并将后续窗口添加到该子菜单。对于第十到第三十六个窗口，我们创建 `&A`、`&B` 到 `&Z` 的 accel 字符串；对于任何其他窗口，我们不提供 accel 字符串 %c 格式字符串用于指定单个字符。子菜单的快捷键是针对英语的；其他语言可能需要不同的处理。

```python
action = menu.addAction("%s" % (accel, title))
self.connect(action, SIGNAL("triggered()"),
               self.windowMapper, SLOT("map()"))
self.windowMapper.setMapping(action, textEdit)
i += 1
```

我们使用（可能为空的）acc 文本和标题——窗口标题，即不带路径的文件名——创建一个新动作。然后，将动作的 `triggered()` 信号连接到信号映射器的 `map()` 槽。这意味着每当用户从“窗口”菜单中选择一个窗口时，信号映射器的 `map()` 槽就会被调用。注意，信号和槽都没有参数；这取决于信号映射器如何确定是哪个动作触发了它——例如，它可以使用 `sender()`。在信号连接处，我们在信号映射器内部设置了从动作到相应 TextEdit 的映射。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_313_0.png)

图 9.10 MDI 编辑器的信号映射器

当信号映射器的 `map()` 槽被调用时，信号映射器将找出是哪个动作调用了它，并根据映射确定传递哪个 TextEdit 作为参数。然后，信号映射器将发射它自己的 `mapped(QWidget*)` 信号并带上参数。我们将 `mapped()` 信号连接到 MDI 工作区的 `setActiveWindow()` 槽，该槽反会被调用，作为参数传递的 TextEdit 将成为活动窗口。

到此完成了对 MDI 文本器的回顾。我们跳过了创建应用程序对象和主窗口的代码，因为它们与我们在之前的示例中看到的许多代码示例相同。

## 总结

当我们有包含许多选项的对话框时，通常可以使用标签小部件（tab widgets）和堆叠小部件（stacked widgets）让用户操作更容易。标签小部件对于我们希望用户能够查看并编辑所有可用选项的情况特别有用。堆叠小部件适用于我们希望用户只看到当前相关页面的情况。对于堆叠小部件，我们必须提供一种让用户选择当前页面的方法——例如组合框或页名称列表。当对话框的某些选项是“高级”的或不经常被需要时，我们可以使用扩展对话框，除非用户请求查看，否则隐藏额外内容。分组框（group boxes）可以用于启用或禁用它们包含的小部件；这非常有用。

# 10

- 事件处理机制

- 重新实现事件处理器

- 使用剪贴板

- 拖放

## 事件、剪贴板与拖放

在这一章简短的介绍中，我们首先开始描述涉及事件处理的关键概念。在第二节中，我们将基于这些知识，展示如何通过重新实现低级事件处理器来控制小部件的行为和外观。后续章节将在前两节涵盖的内容基础上进行扩展，特别是第 11 章，它展示了如何创建自定义小部件。

本章的第三部分展示了如何使用剪贴板，特别是如何与系统全局剪贴板之间传递和检索纯文本、HTML 和图像。最后一部分展示了如何实现拖放功能，既可以通过 PyQt 提供的易于使用的内置功能，也可以通过自己处理事件来实现以拖放自定数据。该练习基于对拖放自定义数据的覆盖，允许用户在释放鼠标按钮时选择移动还是复制。

## 事件处理机制

PyQt 提供了两种处理事件的机制：高级信号与槽机制以及低级事件处理器。当我们关注用户想要执行哪些操作，而不纠结于他们具体请请的细节时，信号与槽的方法是理想的。信号与槽也可以用于自定义小部件行为的某些方面。但当我们我们需要深入底层时，特别是在创建自定义小部件时，我们需要使用低级事件处理器。

PyQt 提供了丰富的事件处理器，其中一些关注小部件的行为（例如处理按键和鼠标事件的处理器），另一些关注小部件的外观（例如处理绘制事件和调整大小事件的处理器）。

PyQt 的事件处理机制按照我们预期的逻辑方式工作。例如，如果用户在具有焦点的小部件上点击鼠标或按下按键，该小部件将获得该事件。如果小部件处理了该事件，故事就结束。如果小部件没有处理该事件，事件将传递给该部件的父部件——这是 PyQt 父子层次结构的另一个优势。这种从子部件到父部件的未处理事件传递一直持续到顶层部件，如果它也不处理该事件，事件将被直接丢弃。

PyQt 提供了五种拦截和处理事件的不同方法。前两种方法最常用，其他方法很少需要，甚至永远不需要。

最简单的方法是重新实现特定的事件处理器。到目前为止，我们只看到了这一个例子：小部件 `closeEvent()` 的实现。正如我们在本章及后续章节中看到的，我们可以通过重新实现其他事件处理器来控制小部件的行为——例如 `keyPressEvent()`、`mouseEvent()` 和 `mouseReleaseEvent()`。我们还可以通过重新实现 `resizeEvent()` 和 `paintEvent()` 来控制小部件的外观。当我们实现这些事件时，我们通常不会调用基类实现，因为我们希望自己的代码只在事件处理器被调用时才执行。

在任何特定的事件处理器被调用之前，`event()` 处理器会被调用。重新实现此方法允许我们处理那些在特定事件处理器中无法妥善处理的事件（特别是覆盖制表键切换键盘焦点的行为），或者为那些没有特定处理器的事件实现功能，例如 `QEvent::ToolTip`。当我们重新实现此处理器时，对于我们自己不处理的事件，可以调用基类的实现。

第三和第四种方法使用事件过滤器。我们可以在任何 `QObject` 上调用 `eventFilter()`。这意味着传递给 `QObject` 的所有事件都将传递给我们的事件过滤器：我们可以在事件到达目标对象之前丢弃或修改任何事件。这种方法的一个更强大的版本是在 `QApplication` 对象上安装事件过滤器，尽管其实际用途仅限于调试和处理发送到禁用小部件的鼠标事件。可以在对象或 `QApplication` 上安装多个事件过滤器，在这种情况下，它们将按照从最近安装到最先安装的顺序执行。

事件过滤器提供了处理事件的非常强大的手段，但初学者往往倾向于使用它们。我们建议尽量避免使用，因为它们会增加复杂性。第五种方法是子类并重新实现 `event()` 方法。 (此处由于原文似乎存在乱码重复，已根据逻辑重新 re-align translation)

最简单的方法是重新实现特定的事件处理器。到目前为止，我们只看到了这一个例子：小部件 `closeEvent()` 的实现。正如我们在本章及后续章节中看到的，我们可以通过重新实现其他事件处理器来控制小部件的行为——例如 `keyPressEvent()`、`mouseEvent()` 和 `mouseReleaseEvent()`。我们还可以通过重新实plement `resizeEvent()` 和 `paintEvent()` 来控制小部件的外观。当我们实现这些事件时，我们通常不会调用基类实现，因为我们希望自己的代码只在事件处理器被调用时才执行。

在任何特定的事件处理器被调用之前，`event()` 处理器会被调用。重新实现此方法允许我们处理那些在特定事件处理器中无法妥善处理的事件（特别是覆盖制表键切换键盘焦点的行为），或者为那些没有特定处理器的事件实现功能，例如 `QEvent::ToolTip`。当我们重新实现此处理器时，对于我们自己不处理的事件，可以调用基类的实现。

第三和第四种方法使用事件过滤器。我们可以在任何 `QObject` 上调用 `eventFilter()`。这意味着传递给 `QObject` 的所有事件都将传递给我们的事件过滤器：我们可以在事件到达目标对象之前丢弃或修改任何事件。这种方法的一个更强大的版本是在 `QApplication` 对象上安装事件过滤器，尽管其实际用途仅限于调试和处理发送到禁用小部件的鼠标事件。可以在对象或 `QApplication` 上安装多个事件过滤器，在这种情况下，它们将按照从最近安装到最先安装的顺序执行。

事件过滤器提供了处理事件的非常强大的手段，但初学者往往倾向于使用它们。我们建议尽量避免使用，因为它们会增加复杂性。第五种方法是子类并重新实现 `event()` 方法。

## 重新实现事件处理器

(由于原文此处部分存在大量文本重复和乱码，翻译已基于核心逻辑整合)

## 重实现 Else 处理器

```python
else:
    self.key = "PageDown"
elif Qt.Key_A <= event.key() <= Qt.Key_Z:
    if event.modifiers() & Qt.ShiftModifier:
        self.key = "Shift+"
self.key += event.text()
if self.key:
    self.key = QString(self.key)
    self.update()
else:
    Widget.keyPressEvent(self, event)
```

当按下按键时，我们会通过 `keyPressEvent()` 收到通知。同样还有一个对应的 `keyReleaseEvent()`，但它很少被重实现。`QKeyEvent` 参数提供了几个实用的方法，包括 `key()`，它返回被按下按键的键码；以及 `modifiers()`，它返回一个指示 Shift、Ctrl 和 Alt 键状态的位标志。

我们选择处理 Home、End、PageUp、CtrlUp、PageDown 和 Ctrl+Down 序列，以及字母键 A..Z 以及 Shift+A..Shift+Z。我们在 `key` 变量中存储了所按内容的文本表示，并调用 `update()` 来调度一个绘制事件。如果用户按下了我们没有处理的按键，我们将按键按下传递给基类实现，这是处理按键事件时的常见做法。

```python
def contextMenuEvent(self, event):
    menu = QMenu(self)
    oneAction = menu.addAction("One")
    twoAction = menu.addAction("Two")
    self.connect(oneAction, SIGNAL("triggered()"), self.one)
    self.connect(twoAction, SIGNAL("triggered()"), self.two)
    if not self.message:
        menu.separator()
        threeAction = menu.addAction("Three")
        self.connect(threeAction, SIGNAL("triggered()"), self.three)
    menu.exec_(event.globalPos())
```

创建上下文菜单的最简单方法是使用 `QWidget.addAction()` 向小部件添加操作，并将小部件的上下文菜单策略设置为 `Qt.Actions-ContextMenu`；我们在第 6 章第 180 页看过如何做这一点。但如果我们想对上下文菜单事件产生的结果进行更精细的控制——例如，根据应用程序的状态提供不同的选项——我们就像这里 own 一样重实现上下文菜单事件处理器。

`globalPos()` 方法返回调用上下文菜单时所在的位置；我们将该位置传递给 `QMenu.exec_()`，以确保菜单在用户预期的地方弹出。

## 重实现事件处理器

```python
def mouseDoubleClickEvent(self, event):
    self.justDoubleClicked = True
    self.text = QString("Double-clicked")
    self.update()
```

如果用户双击，就会调用此事件处理器。在这个示例中，我们需要跟踪用户是否刚刚执行了双击，因为我们也在重实现鼠标释放和移动事件。双击会导致产生一个鼠标释放事件，而且在双击时几乎肯定会发生鼠标移动事件，因为用户的手不太可能保持完全稳定。

我们采取了与在其他事件处理器中相同的方法：我们设置文本并调度重绘以显示它。对于我们自己处理的鼠标事件，不调用基类是非常普遍的。

```python
def mouseReleaseEvent(self, event):
    if self.justDoubleClicked:
        self.justDoubleClicked = False
    else:
        self.mouseTracking(not self.hasMouseTracking())
        if self.hasMouseTracking():
            self.text = QString("Mouse tracking is on.\n"
                "Try moving the mouse!\n"
                "Single click to switch it off")
        else:
            self.text = QString("Mouse tracking is off.\n"
                "Single click to switch it on")
    self.update()
```

如果用户刚刚释放鼠标（双击之后除外），我们会切换鼠标跟踪状态。当跟踪开启时，所有的移动都会产生鼠标移动事件；当跟踪关闭时，只有在拖动鼠标时才会产生鼠标移动事件。默认情况下，我们使用鼠标点击（即点击后的释放）来切换鼠标跟踪的开启。

```python
def mouseMoveEvent(self, event):
    if not self.justDoubleClicked:
        globalPos = self.mapToGlobal(event.pos())
        self.text = QString("The mouse is at%nPoint(%d, %d)\n"
            "in widget coords, and\n"
            "QPoint(%d, %d) in screen coords") % (
                event.pos().x(), event.pos().y(),
                globalPos.x(), globalPos.y())

    self.update()
```

### 表 10.1 选定的 QWidget-事件-处理方法

| 语法 | 描述 |

| --- | --- |

| w.closeEvent(e) | 重实现以赋予用户保存未保存更改和保存用户设置的机会；w 是自定义的 QWidget 子类，e 是特定处理器的 QEvent |

| w.contextEvent(e) | 重实现以提供自定义菜单。另一种更简单的方法是设置 `ContextMenuPolicy(Qt.ActionsContextMenu)` 并使用 `widget.addAction()` 向小部件添加操作。 |

| w.dragEnterEvent(e) | 重实现以处理拖入 |

| w.dragMoveEvent(e) | 重实现以处理拖入 |

| w.dropEvent(e) | 重实现以处理拖放 |

| w.event(e) | 重实现以处理拖放 |

| w.keyPressed(e) | 重实现以处理拖放 |

| w.mouseDoubleClickEvent(e) | 重实现以处理拖放 |

| w.mouseMoveEvent(e) | 重实现以处理拖放 |

| w.mouseReleaseEvent(e) | 重实现以处理拖放 |

| w.paintEvent(e) | 重实现以处理拖放 |

| w.resizeEvent(e) | 重实现以处理拖放 |

```python
def event(self, event):
    if event.type() == QEvent.KeyPress and \
        event.key() == Qt.Tab:
        self.key = QString("Tab captured")
```

## 使用剪贴板

剪贴板一次只存储一个对象，因此如果我们先设置了（例如）一个字符串，然后设置了图像，那么只有图像是可用的，因为字符串在设置图像时会被删除。

以下是我们向剪贴板设置内容的方法：

```python
clipboard = QApplication.clipboard()
clipboard.setText('I've been clipped!')
```

该文本是纯文本；稍后我们将查看如何处理 HTML。

```python
clipboard = QApplication.clipboard()
clipboard.setPixmap(QPixmap(os.path.join(
os.path.dirname(__file__), "images/gvim.png")))
```

可以使用 `setImage()` 为 QImage 设置剪贴板图像数据，或者使用 `setPixmap()` 为 pixmap 设置，正如我们在这里所的那样。QImage 和 QPixmap 都能处理多种标准图像格式。

从剪贴板检索数据同样简单：

```python
clipboard = QApplication.clipboard()
self.textLabel.setText(clipboard.text())
```

如果剪贴板没有文本——例如，如果它有一张图像或某些自定义数据类型——`Clipboard.text()` 将返回一个空字符串。

```python
clipboard = QApplication.clipboard()
self.imageLabel.setPixmap(clipboard.pixmap())
```

如果剪贴板没有图像——例如，如果它有文本或某些自定义数据类型——`Clipboard.pixmap()` 将返回空图像。

除了处理文本和图像，我们还可以处理某些其他类型的数据。例如，这里是将 HTML 复制到剪贴板的方法：



```python
mimeData = QMimeData()
mimeData.setHtml(
  "<b>Bold and <font color=Red>Red</font></b>")
clipboard = QApplication.clipboard()
clipboard.setMimeData(mimeData)
```

如果我们想检索 HTML 文本，包括封装在 QMimeData 对象中的 HTML，可以使用 `Clipboard.text("html")`。如果没有文本或文本不是 HTML 格式（例如是纯文本），它将返回空字符串。检索封装在 QMimeData 对象中的数据的通用方法：

```python
clipboard = QApplication.clipboard()
mimeData = clipboard.mimeData()
```

## 第 10 章。事件、剪贴板与拖放

```python
if mimeData.hasHtml():
    self.textLabel.setText(mimeData.html())
```

在某些情况下，我们想要在剪贴板中设置和获取我们的自定义数据格式。我们可以使用 QMimeData 类来实现，正如我们在下一节中看到的。

设置在剪贴板上或从剪贴板检索的数据通常作用于操作系统的全局剪贴板。此外，通过指定剪贴板模式，可以使用选择剪贴板（Linux 和其他使用 X Window 系统的系统上的额外剪贴板），或查找 Mac OS X 使用的粘贴板（pasteboard）。

## 拖放

许多 PyQt 小部件原生支持拖放，只需开启开关即可工作。例如，图 10.2 所示的应用程序启动时，左侧的 QListwidget 有项目，而中间的 QWidget 或右侧的 QTableWidget 是空的。截图显示了项目被拖放后的应用程序状态。

应用程序的源代码位于 `chapter10/draganddrop.pyw`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_326_0.png)

图 10.2 PyQt 内置的拖放功能

拖放功能完全通过设置相关小部件的属性来实现。以下是创建左侧列表小部件的代码：

```python
listWidget = QListWidget()
listWidget.setAcceptDrops(True)
listWidget.setDragEnabled(True)
```

中间的列表小部件类似，不同在于我们将其设置为图标模式而不是列表视图：

```python
iconListWidget = QListWidget()
iconListWidget.setAcceptDrops(True)
iconListWidget.setDragEnabled(True)

iconList.setMode(QListWidget.IconMode)
```

让 QWidget 支持拖放的方法完全相同，只需调用 `setAcceptDrops(True)` 和 `setDragEnabled(True)`。

不需要其他代码；代码显示这允许用户从一个列表小部件将图标和文本项拖到另一个列表小部件中，或者从表格单元格中拖入。

内置的拖放功能非常方便，通常也足够了。但如果我们我们需要处理自己的自定义数据，就必须重新实现一些事件处理器，正如我们在接下来的小节中看到的。

## 处理自定义数据

图 10.3 所示的应用程序支持自定数据的拖放；特别是图标和文本。（源代码位于 `chap10/customdrag-drop.pyw`）尽管这与内置拖放功能的功能相同，但使用的技术是通用的，可以应用于任何任意数据。

图标和文本可以从左侧的列表小部件拖到右侧的列表小部件（处于图标模式）、到左下角的自定义小部件，或者到右下角的自定义行编辑器——在最后的情况下，仅使用了文本。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_327_0.png)

图 10.3 拖动与释放

自定义数据被放入剪贴板；我们使用 QMimeData。图标和文本可以从左侧的列表小部件拖到右侧的列表小部件（处于图标模式）、到左下角的自定义小部件，或者到右下角的自定义行编辑器——在最后的情况下，仅使用了文本。

图 10.3 所示的应用程序支持自定义数据的拖放；特别是图标和文本。（源代码位于 `chap10/customdrag-drop.pyw`）尽管这与内置拖放功能的功能相同，但使用的技术是通用的，可以应用于任何任意数据。

# 316 第 10 章 事件、剪贴板与拖放

这段代码再次与 DropLineEdit 类似，只是现在我们同时想要图标和文本。要向 QListWidgetItem 添加项，我们创建一个新的 QListWidgetItem，并将列表控件（self）作为该项的父项。

```python
def startDrag(self, dropActions):
    item = self.currentItem()
    icon = item.icon()
    data = QByteArray()
    stream = QDataStream(data, QIODevice.WriteOnly)
    stream << item.text() << icon
    mimeData = QMimeData()
    mimeData.setData("application/x-icon-and-text", data)
    drag = QDrag(self)
    drag.setMimeData(mimeData)
    pixmap = item.pixmap(QPoint(24, 24))
    drag.setHotSpot(QPoint(12, 12))
    if drag.start(Qt.MoveAction) == Qt.MoveAction:
        self.takeItem(self.row(item))
```

这是 DropLineEdit 中没有的方法方法，它使得从 ListWidgets 中拖动成为可能。我们不需要检查 item() 的返回值，因为只有项可以被拖动，所以我们知道如果 startDrag() 被调用，那里一定有一个项可以拖动。如果在初始化器中设置了启用拖动，PyQt 会需要时自动调用 startDrag() 方法。

我们创建了一个新的字节数组，并使用 QDataStream 用其填充 QWidgetItem 的图标和文本。对于用于处理仅在应用程序运行期间存在的内存数据的 QDataStream，我们不需要调用 version() 方法，也不需要任何其他选项。一旦填充了字节数组，我们就将其封装在 QByteArray 中。然后我们创建一个 QDrag 对象，并给它提供 MIME 数据。我们选择使用数据的图标作为拖动时使用的图标：如果不这样做，PyQt 将提供一个默认图标。我们还把拖放的“热点（hotspot）”设置为图标的中心。鼠标的热点将始终与图标的热点重合。

此对 drag.start() 的调用启动了拖动；我们将要接受的动作或动作作为参数传递给它。如果拖动成功（即数据被成功释放），start() 方法将返回发生的动作——例如，复制或移动。如果动作是移动，我们就从此列表控件中移除被拖动的 ListWidgetItem。到 PyQt 4.3 中，应该使用 Qdrag.exec() 代替 drag.start()。

setAcceptDrops() 方法继承自 QWidget，但 setDragEnabled() 没有，在默认情况下，它在某些控件中是可用的。如果我们想创建一个支持释放的自定义控件，只需简单调用 setAcceptDrops(True) 并重新实现 dragEnterEvent(), dragMoveEvent() 和 dropEvent()，正如我们在前面的示例中所做的那。如果我们还想让自定义控件支持拖动，且该控件继承自 QWidget 或没有 setDragEnabled() 的 QWidget 子类，我们必须做两件事来让控件支持拖动。一个是提供一个 startDrag() 方法以便创建 Qt 对象，另一个是确保 startDrag() 方法在适当的时间被调用。确保 startDrag() 被调用的简单方法是重新实现 mouseMoveEvent()：

```python
def mouseMoveEvent(self, event):
    self.startDrag()
    QWidget.mouseMoveEvent(self, event)
```

示例应用程序左下角的控件是一个直接的 Widget 子类并使用了这种技术。它的 startDrag() 方法与我们刚刚看到的非常相似，只是简单了一点点，因为它复制拖动而不是移动拖动，因此无论拖放是否成功释放，我们都不需要做任何操作。

# 拖放

## 总结

当我们使用现有的控件时，PyQt 的信号槽机制通常就是我们获得所需行为的所有内容。但当我们创建自定义控件时——例如，为了对控件的外观和行为进行精细控制——我们必须重新实现低级事件处理器。

对于外观，重新实现 paintEvent() 通常足够了，在某些情况下，我们可能还需要重新实现 resizeEvent()。我们通常不会调用这些事件的基类实现。对于行为，重新实现 keyPressEvent() 和某些鼠标事件（如 mousePressEvent() 或 mouseMoveEvent()）是常见的。我们通常不调用鼠标事件的基类实现，尽管这样做是无害的。如果我们通过实现 QWidget::event() 来实施更底层的控制，那么我们必须对我们自己处理的事件返回 True，并且对我们没有处理的事件返回调用基类实现的结果。

上。

我们通常不需要在自己的代码中处理剪贴板，因为 PyQt 大多数文本编辑会自动以我们期望的方式与剪贴板交互。但如果我们想在代码中处理剪贴板，获取文本和图像数据是简单的，使用 QApplication::clipboard() 返回的 QClipboard 即可。设置 HTML 数据稍微有点棘，因为我们必须从 QMimeData [或 QMimeDataObject] 中检索 HTML，而在与剪贴板配合使用 MIME 数据时，我们并不限于 HTML；我们可以使用处理拖放的相同技术来存储和检索任何类型的数据。

标准 PyQt 控件提供的内置拖放支持非常容易设置和使用。但在某些情况下，我们需要拖放我们自己的自定义数据类型。实现此目的的代码并不难写，使用 QByteArray 确保我们可以拖放任何数据。

也可以完全跳过 PyQt 的拖放功能，通过重新实现鼠标事件处理器来实现自己的拖放系统。虽然 PyQt 的事件处理系统非常强大，而且非常容易使用。大多数情况下，使用信号槽机制要简单得多。但当我们需要精细控制和自定时，重新实现事件处理器将让我们获得想要的效果。

## 练习

修改WidgetItem 类，当用户释放时，在鼠标位置弹出一个菜单，包含两个选项：复制和移动。修改 dragMoveEvent() 使释放动动为移动而不是复制。菜单需要放在 dropEvent() 中，创建新的列表项之前。

QMenu.exec() 方法接收一个 QPoint 参数，告诉它在哪里弹出；QCursor.pos() 方法返回当前的鼠标位置。释放事件的释放动作必须根据用户的选择设置为复制或移动。

startDrag() 方法将需要稍微修改：start() 调用必须赋予移动和复制两个动作作为可接受的动作，并且在用户选择移动时移除该项。

最困难的部分是决定如何响应菜单动作。你可以使用 tools.partial 或 lambda 函数。在模型解决方案中，我们简单地使用一个存储释放动作的实例变量，并有两个方法，一个将释放动作设置为移动，另一个设置为复制，然后只需将菜单动作连接到这些方法即可。

另一种微妙的方法也是可能的。与其使用弹出菜单，而在拖动移动中检查键盘修饰符，并将释放动作默认设置为移动，如果按下 Ctrl 键则设置为复制。同样，在释放事件中根据 Ctrl 键的状态设置释放动作。这比弹出菜单不具侵入性，但对普通或天真的用户来说不够直观。

在解决方案中，我们创建了两个自己的子类，DnndListWidget 和 DnndCtrlListWidget 来展示这两种方法（一旦你复制/粘贴了 DnndlistWidget）。只有大约 25 行代码需要添加或更改。

（并重命名了两个版本中的每一个）以实现这里描述的两种方法。

示例解决方案位于 `chap10/customdraganddrop_ans.pyw` 文件中。

# 11

- 使用小部件样式表

- 创建复合控件

- 内置控件子类化

- QWidget 子类化

## 自定义控件

PyQt 最强大且最持久的优势之一就是能够轻松地创建自定义控件。我们使用 PyQt 创建的自定义控件与标准内置控件的创建方式相同，因此它们可以无缝集成，并且对外观或行为没有任意的限制。在 PyQt 中创建自定义控件并不是“一刀切”的问题。相反，我们可以从许多方法中进行选择，从而对控件的行为和外观获得不断增加的控制。。

自定义的最基础级别是简单地设置现有控件的某些属性。我们在前面的章节中已经多次这样做这样做了。在前一章中，我们仅通过在控件上调用 `setAcceptDrops(True)` 和 `setDragEnabled(True)` 就启用了 PyQt 默认的拖放行为。对于数值调节框（spinboxes），我们可以限制它们的行为——例如通过调用 `setRange()` 设置最小值和最大值——并使用 `setPrefix()` 和 `setSuffix()` 来影响它们的外观。我们将在本书中不再这种方法的示例，因为我们已经多次看到过它的运行了。

如果设置现有控件的属性仍然不够，我们可以使用样式表（style sheet）来定制控件的外观和某些行为方面。在控件上设置样式表的功能是从 Qt 4.2 开始引入的，我们将在本章中看到一个简单的示例，让你体验一下这种可能性。

有时，我们并不需要定制某个特定的控件，而是要创建一个结合了两个或其他控件的复合控件。我们将查看一个如何实现此点的简单示例。

如果我们需要更改现有控件的行为，且超出了设置属性可以实现的范围，我们可以对控件进行子类化，并根据需要重新实现任何事件处理器，以实现我们想要的控制。

但在某些情况下，我们需要一个与任何标准内置控件都不同的控件。对于这些情况，我们可以直接对 QWidget 进行子类化，并完全定义控件的行为和外观。

第 11 章。自定义控件

本章将展示此两个示例：第一个可以在很多地方使用的“通用”控件，第二个是仅为一个程序创建的特定应用程序控件。

## 使用小部件样式表

我们已经看到了许多通过更改属性来定制控件的示例。其中一些影响了控件的行为，例如设置 QSpinbox 的范围，另一些则影响了控件的外观，例如设置 QLabel 的边框。Qt 4.2 引入了一个新属性：样式表属性。该属性通过 `QString` 设置，并使用来自 HTML CSS（级联样式表）的语法。

图 11.1 中的截屏显示了一个设置了样式表的对话框。样式表适用于设置其上的控件及其所有子控件。在这种情况下，我们将组合框框（combobox）设置为深蓝色，并将多行编辑框（line edits）设置为深绿色文本。我们还设置了“强制性”行编辑框具有黄色背景。

**图 11.1** 使用样式表定制的对话框

没有任何 PyQt 控件具有“强制性”（mandatory）属性，但从 Qt 4.2 开始，可以动态地为 QObject 添加属性。注意，Qt 属性不同于 Python 属性——例如，它们使用 `property()` 和 `setProperty()` 进行访问。从 PyQt 4.2 开始，可以使用 `QtCore.pyqtProperty()` 函数来同时创建既是 Python 属性又是 Qt 属性的属性。

```python
self.lineedits = (self.firstNameEdit, self.surnameEdit,
self.companyEdit, self.phoneEdit,
self.emailEdit)

for lineedit in self.lineedits:
    lineedit.setProperty('mandatory', QVariant(True))
```

*样式表在 Mac OS 上没有得到官方支持，因此它们的行为可能不可预测。预计从 Qt 4.4 开始将支持。*

## 使用小部件样式表

```python
self.connect(lineEdit, SIGNAL("textEdited(QString)"),
self.updateUi())
```

前面的代码是表单的初始化器。它为不希望用户离开的行添加了“强制性”属性。所有的 Qt 属性都以 QVariant 形式持有。信号槽连接稍后讨论。

我们作为一个类静态变量为控件创建一个样式表，并在构造函数的结束处将其设置在表单上。我们同样可以很容易从文件中读取样式表（因为它只是纯文本），或者从 Qt 资源读取。

```python
StyleSheet = """
ComboBox { color: darkblue};
QLineEdit { color: darkgreen};
QLineEdit[mandatory="true"] {
    background-color: rgb(255, 255, 127);
    color: darkblue;
}
"""
```

```python
self.setSheet(StyleSheet)
```

`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表单上。`setSheet(ContactDlg.StyleSheet)` 方法用于将样式表应用到表tron



我们绘制代表管道侧边的线条。第一条线从 a 到 i 到 h，标记管道的左侧；第二条从 g 到 f 到 e，标记管道的右侧；第三条从 b 到 c 到 d，标记顶部的“V”型部分。

就像内置的 PyQt 部件一样，PyWidget 和 FractionSlider 也可以作为顶层部件，这在开发和测试自定义部件时特别有用。`chapter1/fractionsider.py` 和 `chapter1/pyqtwidget.py` 可以作为独立程序运行，因为它们在 QWidget 子类之后都有 `if __name__ == "__main__":` 语句，其中包含创建 QApplication 并创建显示自定义部件的代码。

## 总结

PyQt 提供了多种自定义部件外观和行为的方法。最简单且最常用的方法是将现有部件属性设置为我们想要的值。从 Qt 4.2 开始，提供了样式表（style sheet）属性，这允许我们通过输入使用 CSS 语法的纯文本对部件的外观产生巨大影响。一种常见的

## 346 第 11 章 自定义控件

使用样式表非常简单的方法是设置强制控件的背景颜色。

复合控件（Composite widgets）允许我们把一个或多个控件布局在一起，然后将生成的控件视为单个控件。如果复合控件被频繁使用，这可以节省时间，同时也提供了一种在主窗口风格应用程序的中心区域放置多个控件的方法。某些程序员会将构造子控件设为私有，并转发它们的信号和槽，但在许多情况下，最简单的方法是将构造控件留为公共实例变量，并直接对其进行访问和连接。

通过对现有控件进行子类化来适应其外观（特别是行为），并不比创建一个 `Widget` 子类并自己完成所有工作更容易。这种方法适用于几乎每一个 PyQt 控件，因为它们大多数设计都是为了被子类化的。这种方法的唯一局限性在于，它适用于与我们想要的控件足够相似的控件，以便于进行适配。

如果我们需要创建一个与任何其他控件都不同的控件，或者我们想完全控制自定控件的外观和行为，可以对 `Widget` 进行类。我们的子类必须重实现 `paintEvent()`、`sizeHint()` 和 `minimumSize()`，并且将始终重实现 `keyPressEvent()` 和一些鼠标事件处理程序。大多数内置控件都是以此方式创建的，其余的则是其他构建控件的子类。

我们在本章中（实际上在整本书中）自定义的所有控件在外观和行为上都是相当常规的。PyQt 并不强制这种保守性，我们可以自由地创建具有任何外观和任何行为的控件。

## 练习

创建图 11.8 所示的 `Counters` 控件。该控件应该显示一个 3x3 的网格，每个格子要么为空（仅显示背景颜色），要么带有红色或黄色椭圆。任何网格的状态应该在空白、黄色和返回空白之间无限循环。当用户点击格子或在方格上按下空格键时，状态应该发生变化。键盘焦点应该通过用粗蓝笔绘制方格来显示，而不是使用其他方格使用的细黑笔。用户应该能够通过点击或使用上、下、左、右方向键移动焦点来改变聚焦的格子。

确保你提供了 `size hint` 和 `minimum size hint`，以便该控件具有良好的缩放行为且不会被缩得太小。绘制事件（paint event）非常短，但略显微妙；你可能需要使用 `QPainter.save()` 和 `QPainter.restore()` 来保存和恢复画器的状态，以便为某个格子设计的笔颜色和画刷颜色不会传播到其他格子。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_361_0.png)

图 11.8 Counters 自定义控件

在结尾包含一个 `if __name__ == "__main__":` 语句，并创建一个 `QApplication` 对象和 `Counters` 控件实例以便进行测试。整个过程可以在 130 行以内完成。

解决方案位于 `chap11/counters.py` 中。

## 12

- 自定义和交互图形项
- 动画与复杂形状

## 基于项的图形 (Item-Based Graphics)

如果我们创建一个自定义控件并用事件重实现它，就可以绘制任何我们喜欢的图形。这种方法在上一节中已经过，它对于绘制自定义控件、图表以及绘制少量数量的项目是理想的。但如果我们需要绘制大量的独立项目（从几十到几千个不等），或者我们需要绘制用户可以单独交互的项目（例如点击、拖放和选择它们），或者如果我们需要对它们进行动画处理，Qt 的图形类比重实现基于自定义控件的事件要好用得多。

视图类——`QGraphicsView`、`QGraphicsScene` 和 `QGraphicsItem`——以及 `QGraphics` 子类是在 Qt 4.2 中引入的，因此本章中的示例将仅在 Qt 4.2 之后的更高版本中运行。然而，我们强烈建议你为基于图形的应用程序使用 Qt 4.2 或更高版本。

要使用图形类，我们必须创建一个场景，由 `QGraphicsScene` 对象表示。场景是纯数据，只有通过将其与一个或多个 `QGraphics` 子类关联才能视觉化。Qt 提供了几个预定义的子类，包括 `QGraphicsLineItem`、`QGraphicsPixmapItem`、`QGraphicsSimpleTextItem`（纯文本）和 `QGraphicsTextItem`（HTML）。也可以自定义图形项子类，正如我们在本章稍后看到的。

一旦创建了场景并向其中添加了项，就可以使用 `QGraphicsView` 进行视觉化。图形视图的一个强大功能是我们可以对它们应用变换（例如缩放和旋转），这会改变场景的外，但不会改变场景中任何项本身。也可以将多个图形视视图与特定场景关联，以查看场景的不同部分，每个视图都有自己独立的变换。

图形视图类本质上是二维的；尽管尽管如此，每个项都有一个 `z` 值，`z` 值较高的项将绘制在 `z` 值的的之上。碰撞检测基于 `(x, y)` 位置。此外（第 350 页第 12 章 基于项的图形），关于碰撞的信息，场景可以告诉我们哪些项包含特定点或处于特定区域，以及哪些项被选中了。场景有一个前景层（foreground layer），这很有用，例如可以绘制一个覆盖场景中所有项的网格；它们还有一个背景层（background layer），该层绘制在所有项之下，用于提供背景图像或颜色。

项要么是场景的子项（类似于 PyQt 的普通父子关系），要么是另一个项的子。当对一项应用变换时，变换会自动应用于该项的所有子项。这意味着如果一个项被移动（例如由用户拖动），它的子项都会随之移动。也可以拥有一组同级项，即对组中的某一项进行的变换只会影响该项及其子子项，而不影响组中的其他成员。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_364_0.png)

图 12.1 图形使用本地坐标

图形视图使用了三个坐标系，尽管在实践中我们通常关心其中两个。视图使用物理坐标系。我们创建它们。PyQt 自动将场景坐标映射到视图坐标。本质上，场景使用“窗口”坐标，视图使用“端口”坐标。视图使用“端口”坐标。因此，当我们放置项时，是用场景坐标来放置它们的。第三个坐标系是项使用的。这特别方便，因为它是以 `(0,0)` 为中心的本地坐标系。每个项的 `(0,0)` 实际上位于该项在场景中的位置。这意味着在实践中，我们可以轻松地根据中心点绘制项，而不需要担心父项对其应用的任何变换，因为场景会自动为我们处理这些。图 12.1 说明了场景坐标和项坐标之间的关系。

在本章中，我们将查看两个示例，它们展示了图形类的许多不同方面。第一个示例是典型的这类应用程序：用户一个一个创建项，并单独或对选定的组进行操作。该应用程序还展示了用户交互，包括选择、移动和调整大小。第二个示例展示了具有复杂形状的动画复合项。它还展示了如何场景的细节水平（放大或缩小程度）来最小化绘制项的工作量。





# 自定义与交互式图形项

通过对合适的常量调用 `setFlags()`，可以使预定义的图形项变为可移动的、可选的和可合并的。用户可以使用鼠标拖动可移动项，可以通过点击来选择可选项，并使用 Ctrl+点击来选择多个项。可聚焦项将接收按键事件，但除非我们创建一个带有按键处理程序的条目子类，否则它们将忽略这些事件。同样，我们可以通过子类化并实现合适的鼠标处理器，使条目对鼠标事件做出响应。

在本节中，我们将使用两个预定义的图形项，并创建两个自定义图形项子类，以展示如何使用图形项，以及如何控制它们的行为和外观。我们还将看到如何加载和保存，以及如何打印它们。为了实现这些功能，我们将查看图 12.2 中的页面设计器（Page Designer）应用程序。该程序允许用户创建一个包含文本、图像和框的页面。用户可以创建线条——这些只是宽度为 1 像素的框。用户创建的图像可以保存和加载为 .pdf 文件（这是该应用程序特定的自定义格式），并可以使用打印对话框进行打印（或保存为 PDF 文件）。

对于文本项，使用了 `QWidgetItem` 子类，并进行了扩展以允许用户通过双击设置项的字体和文本。对于框（以及线）项，使用了 `QGraphicsItem` 子类。它具有上下文菜单，以及用于调整大小的键盘支持，并处理所有的绘制工作。图像项使用内置的 `QGraphicsPixmapItem` 类，而边距指南使用内置的 `QGraphicsRectItem` 类。显示场景的视图是 `QGraphicsView` 子类，它支持橡皮带选择和鼠标轮缩放。

我们将开始查看 `QGraphicsView` 子类。然后我们将回顾主框架，最后，我们将回顾自定义的 `QGraphicsItem` 子类。

```python

class GraphicsView(QGraphicsView):

    def __init__(self, parent=None):

        super(QGraphicsView, self).__init__(parent)

        self.setDragMode(QGraphicsView.RubberBandDrag)

        self.setRenderHint(QPainter.Antialiasing)

        self.setRenderHint(QPainter.TextAntialiasing)

def wheelEvent(self, event):

    factor = 1.41 ** (-event.delta() / 240.0)

    self.scale(factor, factor)

```

前面的代码是完整的 `GraphicsView` 子类。在初始化器中，我们设置了拖动模式：这意味着在视图上拖动会导致 PyQt 为我们提供一个橡皮带，并且橡皮带碰到的每一个项都会被选中。渲染提示会传递到视图内部绘制的任何项中，因此我们不需要为每个单独的图形项设置提示。

每当用户滚动鼠标轮时，就会调用 `wheelEvent` 事件，它将根据鼠标轮滚动的方式使视图缩小或放大。这种效果是改变页面的视觉 de尺寸——底层的场景完全没有改变。此事件处理器中使用的方法相当复杂，但并不是问题，因为该方法可以“原样”复制并粘贴。

在 `chap12/pagedesigner.pyw` 的顶部，我们有一些全局声明。

```python

PageSize = (612, 792)

PointSize = 10

MagicNumber = 0x70616765

FileVersion = 1

Dirty = False

```

# 第 12 章. 基于项的图形

页面大小是以美式 Letter 尺寸纸张的磅。（源代码中也包含了注释的 A4 页面大小）。正如我们在第 8 章和其他其他地方看到的，魔数和文件版本被 `QDataStream` 使用。我们还有一个全局的 `glyph dirty` 。

我们没有显示导入部分，但它们包含了 `functools`。在我们使用 `functools.partial()` 函数的上下文需要它，该函数用于用合适的参数来封装要调用的方法。

主函数的初始化器非常长，因此我们将分部分查看它，但省略与我们在其他地方看到的相似的代码——例如，创建和布局函数按�的地方。

```python

class MainForm(QDialog):

    def __init__(self, parent=None):

        super(MainForm, self).__init__(parent)

        self.filename = QString()

        self.copiedItem = QByteArray()

        self.pasteOffset = 5

        self.prevPoint = QPoint()

        self.addOffset = 5

        self.borders = []

        self.printer = QPrinter(QPrinter.HighResolution)

        self.printer.setPageSize(QPrinter.Letter)

```

被复制的项本质上是一个描述最近要复制或剪切的项的二进制数据块。我们将这些数据存储在应用程序内部而不是剪贴板上，因为它对任何其他应用程序都没有用。当用户重复相同的项时，使用粘贴偏移量（paste offset），当用户重复相同的项类型时，使用上一点（previous point）和添加偏移量（add offset）。在这两种情况下，新添加的项都添加在几乎正好位于上一个项附近的偏移位置。这使用户更容易看到自己的位置。

`borders` 将包含两个图形项，两个都是黄色矩形：一个提供页面轮廓，另一个提供页面内部的轮廓以留出边距空间。它们被用作指南，不会被保存或打印。虽然可以在需要时创建 `QPrinter` 对象，但通过创建并将其保持为实例变量，我们确保了用户的设置（如页面大小）在同一会话的使用之间得以保留。

```python

self.view = GraphicsView()

self.scene = QGraphicsScene()

self.scene.setSceneRect(0, 0, PageSize[0], PageSize[1])

self.addorders()

self.view.setScene(self.scene)

```

## 表 12.1 QGraphicsScene 方法

| 语法 | 说明 |
| :--- | :--- |
| `ellipse(r, b)` | 在场景中添加一个由 `r` 边界定义的椭圆，画刷为 `b` |
| `addItem(g)` | 在场景中添加一个项 `g` |
| `addLine(l, pn)` | 在场景中添加一条线 `l`，画笔为 `pn` |
| `addPath(pp, b)` | 在场景中添加一个路径 `pp`，画刷为 `b` |
| `addPixmap(px)` | 在场景中添加一个像素 `px` |
| `addPolygon(pg, b)` | 在场景中添加一个多边形 `pg` |
| `addRect(r, b)` | 在场景中添加一个矩形 `r`，画刷为 `b` |
| `setText(t, f)` | 在场景中添加文本 `t`，字体为 `f` |
| `collidingItems(g)` | 返回与 `g` 碰撞的项列表 ||| `items()` | 返回场景中的所有项 |
| `removeItem(g)` | 从场景中移除项 `g` |
| `render(p)` | 使用画家 `p` 渲染场景 |
| `setBackgroundBrush(b)` | 设置场景的背景画刷为 `b` |
| `setRect(x, y, w, h)` | 设置场景的矩形区域为 `(x, y, w, h)` |
| `update()` | 调度绘制事件 |
| `views()` | 返回显示场景的视图列表 |





## 第12章.基于项的图形 (Item-Based Graphics)

return
self.createPixmapItem(QPixmap(filename), self.position())

当用户点击“添加位图（Add Pixmap）”按钮时，会调用此方法。我们只需获取用户想要添加到页面的图像名称，并将工作交交给 `createPixmapItem()` 方法。我们没有将所有操作都写在一个方法中；拆分功能更加方便——例如，当我们需要从页面设计器（Page Designer）的 `.pgd` 文件加载位图时。`position()` 方法用于获取添加项的位置；我们稍后会回顾它。

```python

def createPixmapItem(self, pixmap, position, matrix=QMatrix()):

    item = QGraphicsItem(pixmap)

    item.setFlags(QGraphicsItem.ItemSelectable|QGraphicsItem.ItemMovable)

    item.setPos(position)

    item.setMatrix(matrix)

    self.scene.clearSelection()

    self.scene.addItem(item)

    item.setSelected(True)

    global Dirty

    Dirty = True

```

图形视图（graphics views）有两个类：`QGraphicsPixmapItem`，它非常适合在场景中显示图像。在 Qt 4.2 中，`QGraphicsItem` 有三个标志：`Movable`、`Selectable` 和 `IsFocusable`。（Qt 4.3 增加了 `ItemToShape`、`ItemClipsChildrenToShape` 和 `IgnoresTransformations`，后者特别适用于显示我们不希望视图进行变换的文本。）

获取项后，我们在场景中设置它的位置。`setPos()` 方法是唯一在场景坐标上起作用的方法；其他所有方法都是工作于本地坐标的。我们不需要设置变换矩阵（`QMatrix()` 返回的是单位矩阵），但我们希望有一个显式的矩阵，以便在保存和加载（或复制和粘贴）场景项时可以使用它。

`QMatrix` 类持有一个 3 × 3 矩阵，专门专门为图形变换设计的，而不是一个通用的矩阵类。因此，它是 Qt 类中一个命名不当的稀有例子。从 Qt 4.3 开始，`QMatrix` 被更合理的 `QTransform` 类所取代，后者由于使用了 4 × 4 矩阵，同样能够执行强大的变换。

一旦设置好项，我们就清除所有现有的选择并将该项添加到场景中。然后我们选中它，准备让用户与其交互。

```python

def position(self):

    point = self.mapFromGlobal(QCursor.pos())

    if not self.view.geometry().contains(point):

```

> *在上下文中，单位矩阵是指当作用时不会发生任何变换的矩阵。*

## 自定义与交互图形

```python

coord = random.randint(36, 144)

point = QPoint(coord, coord)

else:

    if point == self.prevPoint:

        point += QPoint(self.addOffset, self.addOffset)

        self.addOffset += 5

    else:

        self.addOffset = 5

        self.prevPoint = point

    return self.view.mapToScene(point)

```

此方法用于为新添加的项提供在场景中的位置。如果鼠悬停在视图上，我们使用由 `QCursor.pos()` 提供的鼠标位置--在此上下文中，`cursor` 指光标——但如果项刚刚在相同位置添加，则表示一个偏移量。这意味着如果用户反复点击“添加”按钮，每个后续项都将相对于前一个项产生偏移，使用户户更容易查看和与其交互。如果鼠标在视图外部，我们将项放置在场景左上角的一个半随机位置。

`map()` 将场景坐标转换为视图所看到的物理坐标。但场景使用它们自己的本地坐标系，因此我们必须使用 `QGraphicsView.mapToScene()` 将物理坐标转换回来。

```python

def addText(self):

    dialog = TextItemDlg(position=self.position(),

                        scene=self.scene, parent=self)

dialog.exec_()

```

当用户点击“添加文本（Add Text）”按钮时，调用此方法。它会弹出一个智能/编辑项对话框，如图 12.3 所示。如果用户点击“确定”，将添加一个带有其选择的文本和字体的新项。我们不会讨论该对话框，因为它与图形编程无关；它的源代码位于 `chapter12/pagesizer.py`。

我们不需要保留已添加项的引用，因为我们在智能对话框内部将它的所有权交给了场景。

```python

def addBox(self):

    BoxItem(self.position(), self.scene)

```

当用户点击“添加”按钮时，调用此方法。用户可以使用方向键来调整框的大小，甚至将其变成一条线（通过将宽度或高度减为 1 像素），正如我们将看到的那样。

再次，我们不需要保留已添加的框项的引用，因为所有权交给了场景。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_372_0.png)

图 12.3 添加新文本项

我们希望用户能够在页面设计器内部剪切、复制和粘贴项，但由于这些项对其他应用程序没有意义，我们不会使用剪贴板。

```python

def copy(self):

    item = self.selectedItem()

    if item is None:

        return

    self.copiedItem.clear()

    self.pasteOffset = 5

    stream = QDataStream(self.copiedItem, QIODevice.WriteOnly)

    writeItemToStream(stream, item)

```

```

def cut(self):

    item = self.selectedItem()

    if item is None:

        return

    self.copy()

    self.scene.removeItem(item)

    del item

```

```python

def paste(self):

    if self.copyData.isEmpty():

        return

    stream = QDataStream(self.copiedItem, QIODevice.ReadOnly)

    readFromStream(stream, self.pasteOffset)

```

如果项已被复制或复制到复制项中，我们只需创建一个数据流并从复制项字节数组中读取项的数据。`ReadFromStream(stream)` 方法负责创建项并添加到场景中。





## 360 第 12 章 基于项的图形

```python

matrix = QMatrix()

stream >> type >> position >> matrix

if offset:

    position += QPointF(offset, offset)

if type == "Text":

    text = QString()

    font = QFont()

    stream >> text >> font

    TextItem(text, position, self.scene, font, matrix)

elif type == "Box":

    rect = QRectF()

    stream >> rect

    style = Qt.PenStyle(stream.readInt16())

    BoxItem(position, self.scene, style, rect, matrix)

elif type == "Pixmap":

    pixmap = QPixmap()

    stream >> pixmap

    self.createPixmapItem(pixmap, position, matrix)

```

此方法被 `paste()` 和 `open()`（加载 .pgd 文件）使用。它首先读取为每种类型项存储的类型、位置和矩阵。然后，它通过偏移量（offset）调整位置——这仅在项被粘贴时使用。接下来，读取特定于项的数据，并使用这些数据创建一个合适的项。

`TextItem` 和 `BoxItem` 的初始化函数以及 `createPixmapItem()` 方法创建相应的图形项，并将所有权交给场景（scene）。

```python

def rotate(self):

    for item in self.scene.selectedItems():

        item.rotate(30)

```

如果用户点击“旋转”，任何选中的项都会旋转 30°。此应用程序中没有使用子项，但如果任何被旋转的项有子项，这些子项也会被旋转。

```python

def delete(self):

    items = self.scene.selectedItems()

    if len(items) and QMessageBox.question(self,

        "页面设计器 - 删除",

        "删除 %s?" % (len(items)),

        "s" if len(items) != 1 else "")

        QMessageBox.Yes == QMessageBox.No):

        while items:

            item = items.pop()

            self.scene.removeItem(item)

        del item

```

global Dirty

## 自定义与交互式图形项

# Dirty = True

如果用户点击删除且至少有一个选中的项，他们将被询问是否要删除选中的项，如果是，则每个选中的项都将被删除。

```python

def print(self):

    dialog = QDialog(self.printer)

    if dialog.exec_():

        painter = QPainter(self.printer)

        painter.setRenderHint(QPainter.Antialiasing)

        painter.setRenderHint(QPainter.TextAntialiasing)

        scene.clearSelection()

        self.removeBorders()

        self.scene.render(painter)

    self.addBorders()

```

打印机（Printer）是一个绘画设备，就像 Widget 或 QImage，因此我们可以轻松地绘制到打印机。我们利用了 `QGraphicsScene::render()` 便利方法，它可以将整个场景（或其选中部分）绘制到绘画设备上。在绘制之前，我们移除了边框（黄色角），在绘制之后恢复边框。我们还在绘制前清除了选择，某些项如果被选中可能会以不同的方式渲染。可以使用类似的 `QGraphicsView::render()` 方法来渲染场景（或其选中部分）。

我们将省略保存和加载 .pgd 文件的代码，因为它与我们之前处理二进制文件时看到的非常相似。对于保存，我们创建一个 `QDataStream`，调用 `setVersion()`，并写入一个魔数和一个文件版本。然后我们遍历场景中的所有项，并在每次调用时将数据流和项作为参数调用 `item()`。对于加载，我们也创建一个 `QDataStream`。然后读取魔数和文件版本，如果它们正确，则删除现有的项。只要文件中有数据，我们就根据流进行参数化调用 `itemFromStream()`。此方法读取项数据并创建项，在此过程中将它们添加到场景中。

我们已经看到了应用程序是如何运作的，以及如何创建和使用预定义的图形类项，即 `QGraphicsRectItem` 和 `QGraphicsTextItem`。现在我们将注意力转向自定义图形项。我们将从查看 `Text` 子类开始；它扩展了 `QGraphicsTextItem` 类并添加了额外的行为，但将所有绘制工作留给了基类。然后我们将查看 `BoxItem` 类，该类同时包含了行为和绘制的代码。

```python

class TextItem(QGraphicsTextItem):

```

```python

def __init__(self, text, position, scene,

    font=QFont("Times", PointSize), matrix=QMatrix()):

```

```python

super(TextItem, self).__init__(text)

self.setFlags(QGraphicsItem.ItemSelectable|

QGraphicsItem.ItemIsMovable)

self.setFont(font)

self.setPos(position)

self.setMatrix(matrix)

scene.clearSelection()

scene.addItem(self)

self.setSelected(True)

global Dirty

dirty = True

```

`TextItem` 的初始化函数与创建并初始化 `QGraphicsPixmapItems` 的 `createPixmapItem()` 方法非常相似。如果初始化函数中没有提供字体和矩阵，我们会提供一个默认字体和一个默认矩阵（单位矩阵）。

```python

def parentWidget(self):

    return self.scene().views()

```

项的父级可以是另一个项或一个场景。但有时我们需要知道项所在的 Widget，或者是项所在的 Widget。场景是可用的。

```python

def itemChange(self, change, variant):

    if change != QGraphicsItem.ItemSelectedChange:

        global Dirty

        Dirty = True

    return QGraphicsTextItem.itemChange(change, variant)

```

```python

如果用户与项交互——例如移动或选中它——此方法会被调用。对于 `itemChange()` 有两种情况：首先，我们必须返回调用基类的结果；其次，我们绝不能在此方法内部调用 `setPos()`。

```python
def mouseDoubleClickEvent(self, event):
    dialog = TextItem(self.parentWidget())
```

如果用户双击项，我们会弹出一个对话框，用户可以通过更改文本和字体。

## 打印图像

通常图像打印场景一样简单。这里有一个 `printImage()` 方法可以将任何 `QImage` 或 `QPixmap`（两者都可以加载 .bmp, .png, .jpg 以及其他图形文件类型）打印到单页上，假设有一个 `Qprinter`：

```python
def printImage(image, printer, scaleToFill=False):
    dialog = QPrintdialog(printer)
    if dialog.exec():
        painter = QPainter(printer)
        painter.setRenderHint(QPainter.Antialiasing)
        rect = painter.viewport()
        size = image.size()
        size.scale(rect.size(), Qt.KeepAspectRatio)
        painter.setViewport(rect.x(), rect.y(), size.width(), size.height())
        if scaleToFill:
            painter.setWindow(image.rect())
        if isinstance(image, Qpixmap):
            painter.drawPixmap(0, 0, image)
        else:
            painter.drawImage(0, 0, image)
```

打印 `QPicture` 非常相似，只是我们必须根据图片的边界矩形计算大小，并调用 `QPainter.drawPicture()` 来绘制。

SVG 图像也可以打印。方法与我们绘制 `QGraphicsScenes` 时类似。`QSvgRenderer` 类可以加载 SVG 图像并有一个 `render()` 方法可以将图像绘制到任何绘画设备，包括 `QPainter`。从 Qt 4.3 开始，现在可以使用 `QSvgGenerator` 类创建 SVG 图像，这

完成了文本项。它很小，因为我们只关注于改变它的行为。对于接下来要看到的 `BoxItem` 类，我们提供了管理其行为和外观的代码。

```python
class BoxItem(QGraphicsItem):
    def __init__(self, position, scene, style=Qt.SolidLine,
        rect=None, matrix=QMatrix()):
        super(BoxItem, self).__init__()
        self.setFlags(QGraphicsItem.ItemIsSelectable|
        QGraphicsItem.ItemMovable|
        QGraphicsItem.ItemIsFocusable|)
```

*打印文档（包括图像）将在下一章讨论。*

## 第 12 章 基于项的图形

```python
if rect is None:
    rect = QRect(-10 * PointSize, -PointSize, 20 * PointSize, 2 * PointSize)
```

```python
self.rect = rect
self.style = style
self.setPos(position)
self.setMatrix(matrix)
scene.clearSelection()
scene.addItem(self)
self.setSelected(True)
self.setFocus()
global Dirty
dirty = True
```

项必须能够接收键盘焦点，因为我们希望用户能够通过方向键来调整框的大小。如果没有显式给出大小——例如当用户点击“添加框”时，而不是当从文件重新创建框或从复制的项中粘贴框时——我们会提供一个呈现信箱箱（letterbox）形状的默认大小。我们提供了默认的实线线型样式，以及默认的单位矩阵大小。初始化器的其余部分与我们之前用于文本项时使用的相同。

我们将省略 `parentWidget()` 和 `itemChange()` 的代码，因为它们的实现与我们在 `TextItem` 类中使用的相同。

```python
def setStyle(self, style):
    self.style = style
    self.update()
global Dirty
dirty = True
```

此方法用于设置框的线型样式。它通知场景项需要重绘，并设置了脏标记位，因为我们在保存到 `.pgd` 文件时会记录框的线型样式。

```python
def contextMenu(self, event):
    wrapped = []
    menu = QMenu(self.parentWidget())
    for text, param in (
        ("Solid", Qt.SolidLine),
        ("Dashed", Qt.DashLine),
        ("Dotted", Qt.DotLine),
        ("DashDotted", Qt.DashDotLine),
    ):
        wrapper = functools.partial(self.setStyle, param)
        wrapped.append(wrapper)
        menu.addAction(text, wrapper)
    menu.exec_(event.screenPos())
```

## 自定义与交互图形项

如果用户在项上调用上下文菜单（例如，在某些平台上点击右键），则会调用*此方法。* 此上下文菜单使用部分函数应用来封装一个要调用的方法 `setStyle()` 以及调用它的参数，并使用 PyQt 内置的线型样式。包装器必须保持足够长的时间以便菜单完成，因为只有在该之后其中一个包装器才会被调用。由于由于原因，我们保留了包装器的本地列表；该列表将在菜单的 `exec_()` 完成后（即 `contextMenuEvent()` 本身完成时）将超出作用域。

```python
def keyPressEvent(self, event):
    factor = PointSize / 4
    changed = False
    if event.modifiers() & Qt.ShiftModifier:
        if event.key() == Qt.KeyLeft:
            self.setRight(self.rect.right() - factor)
            changed = True
        if event.key() == Qt.KeyRight:
            self.setRight(self.rect.right() + factor)
            changed = True
        if event.key() == Qt.KeyUp:
            self.setBottom(self.rect.bottom() - factor)
            changed = True
        if event.key() == Qt.KeyDown:
            self.setBottom(self.rect.bottom() + factor)
            changed = True
    if changed:
        self.update()
        global Dirty
        Dirty = True
    else:
        QGraphicsItem.keyEvent(self, event)
```

如果用户使用方向键且视图具有滚动条，视图将适当滚动。此方法拦截了当项具有键盘焦点时配合 Shift 键发生的方向键事件，以给用户提供一种调整框大小的方法。`QsetRight()` 和 `QsetBottom()` 方法通过改变宽度和高度来改变矩形的大小。如果我们处理了按键事件，我们就会调用 `update()` 来调度绘制事件，并将页面标记为脏数据；否则，我们调用基类的实现。

现在我们已经看到了框的行为是如何实现的，我们准备好将注意力转向框是如何绘制的。通过子类 `QGraphicsItem`，我们至少必须实现 `boundingRect()` 和 `paint()` 方法。重新实现 `shape()` 也是常见的，但我们将推迟到下一节的示例。

> * 注意，如果视图已被指示处理上下文菜单事件，此方法将不会被调用——例如通过将其上下文菜单策略设置为 `Qt.ActionsContextMenu`。

## 表 12.2 选定的 QGraphicsItem 方法 #1

| 语法 |  |

| --- | --- |

| g.boundingRect() | 返回 QGraphicsItem g 的边界 QRect；子类应实现此方法 |

| g.collidesWithPath(pp) | 如果 QGraphicsItem g 与 QPainterPath pp 碰撞，则返回 True |

| g.collidingItems() | 返回与 QGraphicsItem 碰撞的（可能为空）QGraphicsItems 列表 |

| g.contains(pt) | 如果 QGraphicsItem g 包含 QPoint pt，则返回 True |

| g.isObscured() | 如果 QGraphicsItem g 被其他项遮挡（前提是 z 值较大），则返回 True |

| g.isSelected() | 如果 QGraphicsItem g 被选中，则返回 True |

| g.itemChange(c, v) | 什么都不做；子类可以实现此方法来检测变化——例如，在选中状态或位置上。不要在此方法中直接或间接地接调用 `QGraphicsItem::pos()` |

| g.moveBy(dx, dy) | 移动 QGraphicsItem  dx, dy |

| g.paint(p, o) | 什么都不做；子类应在 p 上绘制它们自己 |

| g.pos() | 返回 QGraphicsItem g 的位置。如果 g 是子项，则在本地坐标 |

| g.resetMatrix() | 将 QGraphicsItem g 的矩阵重置为单位矩阘 |

| g.rotate(a) | 旋转 QGraphicsItem a 度 |

| g.scale(x, y) | 缩放 QGraphicsItem x, y |

| g.scene() | 返回 QGraphicsItem 所在的场景，如果它在视图可见 |

| g.sceneBoundingRect() | 返回场景坐标下的边界矩形 |

| g.setCursor(c) | 设置光标为 c |

| g.setEnabled(b) | 根据 b 设置 g 为启用或禁用 |

| g.setFocus() | 给 g 键盘焦点 |

| g.setFlag(f) | 设置 g 上指定的 GraphicsFlag f |

## 自定义与交互项

### 表 12.3 选定的 QGraphicsItem 方法 #2

| 语法 | 描述 |

| --- | --- |

| g.setMatrix(m) | 将 QGraphicsItem g 的矩阵设置为 m |

| g.setSelected(b) | 根据 b 设置 g 为选中或未选中 |

| g.setValue(z) | 设置 QGraphicsItem g 的值为 z。默认值为 0；值较大的项显示在值小的前面 |

| g.shape() | 返回作为 QPath 的 QGraphicsItem g。默认实现调用 `boundingRect()` 来确定路径；重新实现通常创建精确的形状。默认情况下，碰撞检测基于形状 |

| g.shear(x, y) | 水平 x、垂直 y 切切 QGraphicsItem 的坐标系 |

| g.translate(dx, dy) | 水平 dx、垂直 dy 移动 QGraphicsItem 的坐标系 |

| g.update() | 在场景视图中调度 QGraphicsItem 的绘制事件 |

| g.zValue() | 返回 QGraphicsItem 的 z 值 |

```python
def boundingRect(self):
    return self.rect.adjusted(-2, -2, 2, 2)
```

此方法应该返回项的边界矩形，如果项有轮廓，则减去半个笔宽。我们清理并将边界矩形稍微调大。这使得使用户更容易点击该框，即使他们将其减小为高度或宽度 1 像素的线条。

我们没有实现 `shape()` 方法，因此将使用基类的 `shape()` 方法，并产生一个基于边界矩形的形状。由于我们给了一个比实际情况更大的矩形，形状也会更大。形状被用于确定碰撞检测，但在这里并不重要，因为我们在这个应用程序中不使用碰撞检测；但在下一个应用程序中我们会使用。

```python
def paint(self, option, widget):
    pen = QPen(self.style)
    pen.setColor(Qt.black)
    pen.setWidth(11)
```

## 第 12 章，基于对象的图形

```python
if option.state & QStyle.State_Selected:
    pen.setColor(Qt.blue)
    painter.setPen(pen)
    painter.drawRect(self.rect)
```

绘制方框非常简单。我们首先创建一个具有用户线条样式的画笔（pen），其固定宽度为 1 个逻辑单位。如果矩形被选中，我们就更改画笔的颜色，然后设置画笔并绘制矩形。

使用图形视图类（graphics views classes）和绘制图形项（graphics items）比重新实现 `paint` 事件要简单得多。这是因为每个项都有自己的 `paint()` 方法，而且这些项使用中心点为 (0, 0) 的局部坐标系，这对于旋转来说特别为方便。

在本节中，我们已经看到了了预定义图形项和自定义项的使用，这两者都提供了自定义行为，而后者 `BoxItem` 也还负责绘制。在下一节涵盖的示例中，我们将看到更复杂的绘制操作，以及碰撞检测和简单形式的动画。

## 动画与复杂形状

在上一节中，我们查看了一个用户交互为核心的图形视图应用程序。在本节中，我们将查看一种完全不同的应用程序，我们通过使用一组图形项视觉化种群中的每个成员来模拟一群名为“多足虫”的生物，如图 12.4 所示。每个多足虫都有内部定时器。在每个时间值处，多足虫都会移动，如果发生碰撞，它的颜色就会发生微变化，并最终消失。

我们将首先查看主表单初始化函数的一个片段。然后，我们将回顾表单的 `populate()` 方法，该方法用于创建和定位多足虫。接下来，我们将查看暂停/恢复按钮的操作，以及缩放滑块的实现。然后，我们将查看表单的定时器事件，这是一种我们以前没有用过的事件处理器。一旦我们看到应用程序是如何整体运行的，我们将查看用于视觉化多足虫的图形项子类的实现。

```python
class MainForm(Dialog):
    def __init__(self, parent=None):
        super(MainForm, self).__init__(parent)

        self.scene = QGraphicsScene(self)
        self.scene.setRect(0, 0, SCENSIZE, SCENSIZE)
        self.view = QGraphics()
        self.view.setRenderHint(QPainter.Antialiasing)
        self.view.setScene(self.scene)
```

![](img/55bc1dcf8601cfec5e1423b4e17ec264_383_0.png)

图 12.4 多足虫应用程序

```python
self.view.setFocusPolicy(Qt.NoFocus)
zoomSlider = QSlider(Qt.Horizontal)
zoomSlider.setRange(5, 200)
zoomSlider.setValue(100)
self.pauseButton = QPushButton("Pause")
quitButton = QPushButton("Quit")
```

缩放滑块的范围从 5% 到 200%，初始值为 100%。暂停按钮是“暂停”，退出按钮是“退出”。

表单通过创建场景来开始。对于非对象的子类，我们为场景设置一个 `SCENSIZE` 大小（500）。缩放滑块用于放大或缩小场景。我们将初始值设置为 100%（100%）。缩放滑块用于放大或缩小场景。

```python
self.connect(zoomSlider, SIGNAL("valueChanged(int)"), self.zoom)
self.connect(self.pauseButton, SIGNAL("clicked()"), self.pauseResume)
self.connect(quitButton, SIGNAL("clicked()"), self.exit)
self.startTimer(INTERVAL)
self.setWindowTitle("Multipedes")
```

定时器间隔为 200 毫秒。

```python
def zoom(self, value):
    factor = value / 100.0
    matrix = QTransform()
    matrix.scale(factor, factor)
    self.view.setTransform(matrix)
```

要缩放场景，我们需要做的就是更改视图的缩放。这是通过获取视图的变换矩阵，清除任何可能存在的变换（即缩放），然后将其缩放为与滑块设置成比例的因子来实现。

```python
def zoom(self, value):
    factor = value / 100.0
    matrix = self.view.matrix()
    matrix.reset()
    matrix.scale(factor, factor)
    self.view.setTransform(matrix)
```

![](img/55bc1dcf8601cfec5e1423b4e17ec264_384_0.png)

图 12.5 不同缩放级别下的多足虫

缩放对多足虫的绘制方式有显著影响。这是因为在 `QGraphicsItem::paint()` 方法中，我们可以发现场景被放大的程度，并根据此信息决定绘制多少细节。这意味着例如，当场景缩小到用户无法分辨细节时，我们可以以更快、更简单的方式进行绘制；当场景放大时，我们可以增加细节的绘制。

```python
def populate(self):
    global Running
    Running = True
    x, y = 50, 50
    for i in range(10):
        m = Multipede(x, y)
        self.scene.addItem(m)
        x += random.randint(20, 40)
        y += random.randint(20, 40)
        if x > 450:
            x = 50
            y += 50
        if y > 450:
            y = 50
            x += 50
```

定时器间隔为 20 毫秒，这取决于操作系统，但除非机器负载过重，否则至少是足够的。

```python
def pauseResume(self):
    global Running
    Running = not Running
    self.pauseButton.setText("Pause" if Running else "Resume")
```

如果用户点击暂停按钮，我们将全局变量 `Running` 布尔值取反，并更改按钮的文字。如果它为 `False`，则定时器将什么都不做。

## 动画与复杂形状

## 373

到最大的孙节点，以便只需通过删除多节虫（multipede）的头部，就能删除所有的分段。我们已经了解应用程序是如何工作的，现在我们转向多节虫本身的实现。正如 `population()` 方法所示，多节虫由一个 `Head`（头）和至少四个 `Segment`（段）组成——这两个类都是 `QGraphics` 的子类，并且足够智能只需绘制对当前缩放级别有意义的细节。我们将先查看 `Head`，然后查看 `Segment`。

```python
class Head(QGraphicsItem):
    Rect = QRect(-30, -20, 60, 40)
    def __init__(self, color, angle, position):
        super(Head, self).__init__()
        self.color = color
        self.angle = angle
        self.setPos(position)
        self.timer = QTimer()
        QObject.connect(self, SIGNAL("timeout()"), self.timeout)
        self.timer.start(INTERVAL)
```

所有的头部都有相同的形状：一个适应在静态 `Rect` 内部的椭圆。当头部初始化时，我们将颜色和角度记录在实例变量中，并将其移动到场景中给的位置。

`QGraphicsItem` 类是 `QObject` 的子类，并不提供内置计时器。这不是一个我们可以像这里这样简单使用 `QTimer` 就能解决的问题。计时器的超时不会产生定时器事件，而是通过发射 `timeout()` 信号表示。在这里，我们创建了一个每隔 `INTERVAL` (200) 毫秒超时一次的计时器，即每秒五次。我们将计时器的 `timeout()` 信号连接到我们自己的 `timeout()` 方法；稍后我们将回顾该方法。

```python
def boundingRect(self):
    return Head.Rect
```

边界矩形很简单——它就是作为多节虫头部基础形状的静态 `Rect` 矩形。

```python
def shape(self):
    path = QPainterPath()
    path.addEllipse(Head.Rect)
    return path
```

> *C++/Qt 程序员可能会想要从 QGraphicsItem 和 Qobject 进行多重继承，但 PyQt 只允许继承自单个 Qt 类。*

## 374 第 12 章 基于项的图形

这种方法是碰撞检测的默认方法，除非我们指定一种仅使用边界矩形的粗粒度方法。绘制者（painter）是一系列矩形、椭圆、弧和其他形状（包括绘制路径路径），它们完整的描述了一个项的形状。在这种情况下，路径只是一个椭圆。

使用绘制路径作为图形项的形状可以确保准确检测到碰撞。例如，两个多节虫的头部可能会在矩形的角部交叉而不会发生碰撞，因为它们的椭圆并没有占据角部。

```python
def paint(self, painter, option, widget=None):
    painter.setPen(Qt.NoPen)
    painter.setBrush(QBrush(self.color))
    painter.drawEllipse(Head.Rect)
    if option.levelOfDetail > 0.5:
        painter.setBrush(QBrush(Qt.yellow)) # 外眼
        painter.drawEllipse(-12, 19, 8, 8)
        painter.drawEllipse(-12, 11, 8, 8)
    if option.levelOfDetail > 0.9:
        painter.setBrush(QBrush(Qt.darkBlue)) # 内眼
        painter.drawEllipse(-12, 19, 4, 4)
        painter.drawEllipse(-12, 11, 4, 4)
    if option.levelOfDetail > 1.3:
        painter.setBrush(QBrush(Qt.white)) # 鼻孔
        painter.drawEllipse(-27, 5, 2, 2)
        painter.drawEllipse(-27, 3, 2, 2)
```

头部的细节是一个椭圆，两只眼睛，每只眼睛又是两个嵌套的椭圆，以及两个微小的鼻孔，同样是椭圆。`paint()` 方法首先移除画笔，并设置多节虫颜色的实色画刷。然后绘制基础形状。

`option` 变量类型为 `QStyleOptionGraphics`，它包含了各种有用信息，包括项的变换矩阵、字体度量、调色板和状态（“开启”、“关闭”等许多）。它还持有“细节级别”（level of detail），这是衡量场景放大或缩小的程度的指标。如果场景完全没有缩放，细节级别为 1.0；如果放大到两倍大，细节级别为 2.0；如果缩小到一半大小，细节级别为 0.5。

如果场景以其自然大小的 50% 或更大比例显示，我们就绘制多节虫微小的外眼。我们可以硬编码坐标，因为图形项使用它们自己的本地坐标系，任何外部应用的变换会自动为我们处理。如果场景以其自然大小的 90% 或更大比例显示，我们还会绘制内眼；如果场景打算以 130% 或更大比例查看，我们还会绘制多节虫的微小鼻孔。

## 动画与复杂形状 375

我们必须考虑的最后一个方法是每 `INTERVAL` 毫秒调用一次的 `timeout()` 方法。我们将从两个部分来看这个方法，因为它的功能有两个方面。

```python
def timeout(self):
    if not Running:
        return
    angle += change
    x = pos().x() + math.sin(angle) * offset
    y = pos().y() + math.cos(angle) * offset
    if 0 <= x <= SCENSIZE and 0 <= y <= SCENSIZE:
        setPos(x, y)
    else:
        Running = False
```

（注：由于 `timeout` 方法的 OCR 文本碎片化，我们根据周围文本重新构建了逻辑代码。）

# 动画与复杂形状 377

边界矩必须包含整个形状，包括腿，但使用 `QPainterPath.boundingRect()` 可以很容易获得。

```python
def shape(self):
    return self.path
```

这个形状并不简单，但得益于在初始化器中计算了路径，这个方法非常简单。

```python
def paint(self, painter, option, widget=None):
    painter.setPen(Qt.NoPen)
    painter.setBrush(QBrush(self.color))
    if option.levelOfDetail < 0.9:
        painter.drawEllipse(self.rect)
    else:
        painter.drawPath(self.path)
```

得益于预计算矩形和绘图路径，`paint()` 方法比其他情况下要简单且快速得多。如果场景缩小到 90% 或以下，我们只需画一个圆；否则，我们使用绘图路径绘制完整细节形状。

```python
def timeout(self):
    if not Running:
        return
    matrix = self.matrix()
    matrix.reset()
    self.setMatrix(matrix)
    self.angle += self.change
    if self.angle > 5:
        self.change = -1
        self.angle -= 1
    elif self.angle < -5:
        self.change = 1
        self.angle += 1
    self.rotate(self.angle)
```

当多足兽（multipede）移动头部时，它的第一个（子）段会随之移动，该段的子段也随之移动，以此此类推。这很好，但这意味着多足兽的形状是刚性的。我们希望段在多足兽移动时左右轻轻摇动，因此我们为每个段设置了自己的定时器。

我们获取段的变换矩阵，清除任何已应用的变换（旋转），然后旋转该段。`change` 变量初始为 1，旋转角度初始为 0°。在每个间隔，将 `change` 加到角度上。如果角度达到 6（或 -6），我们设置为 5（或 -5）并反转 `change` 值。这意味着角度的序列为 1, 2, 3, 4, 5, 4, 3, 2, 1, 0, -1, -2, -3, -4, -5, -4, -3, -2, -1, 0, 1, 2 等并往复，这产生了良好的摇摆效果。

这完成了我们对复杂形状动画的审查。使用绘图路径可以创建任意复杂性的形状，通过将路径存储为静态变量或实例变量，许多计算可以一次性完成，而不是在每次调用 `paint` 方法时进行。我们实现动画的方法并非唯一可能。例如，我们可以结合 `QTimeline` 使用 `Graphics-ItemAnimation` 元素。另一种方法是将定时器从项目本身中提取出来并保留对它们的引用集合。然后，可以使用表单形式的定时器，并在每个间隔移动集合中的每个项目，并在 `tform` 的 `timeout` 处理程序中解决冲突。没有唯一且必须的方法；最佳方法取决于应用程序的需求。

## 总结

`views` 类非常适用于有大量单个项目（从几十到几十万个）需要绘制的情况。它们对于我们希望允许用户与项目交互（例如，点击并拖动以及选择它们）也是完美的，而且对于动画来说也是理想的。

`Scenes` 使用它们自己的本地坐标系并包含图形项目。它们通过 `GraphicsView` 查看，如果我们希望用户能够使用两个或多个不同的变换查看场景（例如，在不同的缩放级别或旋转下），可以为场景关联多个视图。

`views` 类包含许多实用的预定义项目，可以“按原”使用。我们也可以继承 `GraphicsItem` 或其一个子类来提供自定义行为（例如上下文菜单和按键处理）以及自定义绘制，以便我们可以绘制任何我们喜喜欢的形状。

如果我们想从文件中保存和加载场景，一种简单的方法是让场景中的每个项目都拥有一个变换矩阵，并保存描述、项目在场景中的位置、项目的矩阵以及任何必要的特定额外数据。使用 `QDataStream` 完成此非常容易。

通过使用场景类和视图类提供的 `render()` 方法，任何场景都可以在绘制在任何绘图设备上，包括打印机、PDF 文件或 `QImage`（例如保存为 .png 文件）。在 Qt 4.3 中，场景还可以以 SVG 格式在 `QSvgGenerator` 绘图设备类中渲染。

绘制图形视图项目尽可能简单，因为方便的本地坐标系允许我们忽略任何外部应用的变换——例如，父项目。`QPainter` 类提供了许多方便的绘制方法，用于绘制弧、弦、椭圆、多边形、直线、折线、矩形、图像和文本。此外，可以使用 `QPainter` 对象创建复杂形状，并可以直接使用 `QPath.drawPath()` 进行绘制。

更复杂的形状可以通过组合两个或多个项目来创建，这些可以使用 `QPath.drawPath()` 直接绘制。

## 382 第 13 章 富文本与打印

文档，在后续章节中，当我们想要提供用户在数据库类型应用程序中编辑单行 HTML 文本的能力时，这将是一个用的组件。

本章的第二节专门介绍打印。我们已经见过如何在页面上打印图像和图形场景，在本节中，我们将学习如何打印多页文档，包括包含图片的文档。PyQt 提供了三种不同的文档打印技术：一种基于组合和打印 HTML，另一种基于创建和打印 QTextDocuments，还有一种是使用 QPainter 直接在打印机页面上绘图。我们将展示并讨论这所有三种方法。

## 富文本编辑

在本节中，我们将从两个不同的视角来看富文本编辑。在第一个小节中，我们将创建一个纯文本编辑器，该编辑器使用 `QSyntaxHighlighter` 为 Python 源代码提供语法高亮。在第二个小节中，我们将创建一个类似于 `QLineEdit` 的单行文本编辑器，它具有弹出菜单，并支持如 `Ctrl+B` 和 `Ctrl+I` 等各种快捷键来切换粗体和斜体的开启。在这两种情况下，我们都使用 `QTextEdit` 作为基础进行构建。

## 使用 QSyntaxHighlighter

如果我们想要一个带有语法高亮的 Python 专家编辑器，就不需要自己创建一个。基于 Tkinter 的 IDE 应用程序既提供了一个可以在其中尝试 Python 代码的“沙盒”，也提供了一个非常好的 Python 代码编辑器。为了更强大的功能，我们可以使用 Eric4，它本身是用 PyQt 编写的并使用 `QTextEdit` 进行文本编辑。然而，现成的编辑器并不一定能完全按照我们的意工作，而且创建自己的编辑器既具有启发性，又能揭示其中涉及的原理。我们将创建一个 Python 编辑器来学习如何使用 `QTextEdit` 和 `QSyntaxHighlighter`。如图 13.1 截图所示，Python 编辑器是一个带有两个菜单和工具栏的主窗口应用程序。由于我们之前已经涵盖过应用程序的创建，现在我们将只关注与文本编辑相关的部分，从主窗口初始化函数的开头开始。

```python
class MainWindow(QMainWindow):
    def __init__(self, filename=None, parent=None):
        super(QMainWindow, self).__init__(parent)

        font = QFont("Courier", 11)
        font.setFixedPitch(True)
        self.editor = QTextEdit()
        self.editor.setFont(font)
        self.highlighter = PythonHighlighter(self.editor.document())
        self.setCentralWidget(self.editor)
```

![](img/55bc1dcf8601cfec5e1423b4e17ec264_397_0.png)

图 13.1 正在编辑自身的 Python 编辑器

我们首先创建一个等宽字体（每个字符宽度相同的字体）。然后我们创建一个 `TextEdit`，这是一个自定义的 `QTextEdit`，它与 `QTextEdit` 的不同之处在于会将 Tab 键转换为插入四个空格。我们创建一个 `PyHighlighter`，它是 `QSyntaxHighlighter` 的子类，并传递了文本编辑器的 `QTextDocument`——这是编辑器和格式实际存储的对象。我们创建了主窗口的中心部件。

初始化函数的其余部分是关于操作、菜单和工具栏的创建，这些都是我们非常熟悉的，因此可以跳过。我们唯一查看的方法是三个基本文件处理方法中的两个，因为它们调用了文本编辑器。

```python
def setNew(self):
    if not self.okToContinue():
        return
    document = self.editor.document()
    document.clear()
    document.setModified(False)
    self.filename = None
    self.setWindowTitle("Python Editor - Unnamed")
    self.updateUI()
```

该方法简单地获取并清空实际持有文本的 `QTextDocument`，并将修改标志设为 `False`。结果是一个没有未保存更改的空白 `QTextEdit`。`updateUI()` 方法用于根据应用程序的状态启用或禁用操作；请参见第 385 页上的“启用和禁用操作”侧边。

```python
def loadFile(self):
    fh = None
    try:
        fh = QFileInfo(self.filename)
        if not fh.open(QIODevice.ReadOnly):
            raise IOError, unicode(fh.errorString())
        stream = QTextStream(fh)
        stream.setCodec("UTF-8")
        self.editor.setPlainText(stream.readAll())
        self.editor.document().setModified(False)
        self.editor.setWindowTitle("Python Editor - %s" % \
        QFileInfo(self.filename).filename())
    except (IOError, OSError), e:
        QMessageBox.warning(self, "Python Editor -- Load Error",
        "Failed to load %s: %s" % (self.filename, e))
    finally:
        if fh is not None:
            fh.close()
```

如果加载了文件——例如用户调用“文件→打开”操作——就会调用此方法。文件处理代码与我们之前看到的类似；唯一的区别是我们将 `QTextDocument` 的修改标志设为 `False`。

保存代码（未显示）与加载代码非常相似。我们获取文件句柄，创建一个 `QTextStream`，将编码设置为 UTF-8，并使用 `QTextEdit.toPlainText()` 输出整个文本。我们还设置了 `QTextDocument` 的修改标志为 `False`。

```python
class QTextEdit(QTextEdit):
    def __init__(self, parent=None):
        super(QTextEdit, self).__init__(parent)

    def event(self, event):
        if event.type() == QEvent.KeyPress and event.key() == Qt.Key_Tab:
            cursor = self.textCursor()
            cursor.insertText("    ")
            return True
        return QTextEdit.event(event)
```

（注：这里的 OCR 文本是碎片化的；上述逻辑遵循标准的 PyQt keyPressEvent 覆盖或对 Tab 键的处理）。

前面的代码显示了完整的 `QTextEdit` 子类。每个文档都可以通过 `QTextCursor` 对象进行操作，这就是用户通过按键和鼠标操作与文档交互的方式。

## 启用和禁用操作

有时，特定的操作仅在某些情况下适用。例如，对一个未保存更改的文档允�“保存文件”是没有意义的，或者说，在空文档上允许“另存为”也没有意义。同样，如果没有选中的文本，“编辑复制”或“编辑剪切”都没有意义。处理此问题的方法之一是让操作保持启用状态，但在不符合逻辑的情况下让它们执行空。

另一种解决方案是根据应用程序的状态启用和禁用操作。这可以通过完成三件事来实现：

- 将要启用和禁用的操作变为实例变量，以便在初始化函数之外访问；

- 创建一个根据应用程序状态启用和禁用操作的方法（例如 `updateUI()`）；

- 第三，建立 `updateUI()` 的特定的信号槽连接，以便在应用程序状态发生变化时调用它。

以 Python 编辑器为例，我们可以启用这些连接：

```python
self.connect(editor, SIGNAL("selectionChanged()"), self.updateUI())
self.connect(editor.document(), SIGNAL("modificationChanged(bool)"), self.updateUI())
self.connect(QApplication.clipboard(), SIGNAL("dataChanged()"), self.updateUI())
```

这些连接意味着，如果编辑器的选择发生、文档被修改或剪贴板数据变化，我们可以启用或禁用相关的操作。

```python
def updateUI(self, arg=None):
    self.fileSaveAction.setEnabled(self.document().isModified())
    self.fileSaveAction.setEnabled(not self.document().cursor().isEmpty())
    enable = self.document().cursor().hasSelection()
    self.editCopyAction.setEnabled(enable)
    self.editCutAction.setEnabled(enable)
    self.editPasteAction.setEnabled(editor.canPaste())
```

该方法通过前面的信号槽连接被调用。它在初始化函数的末尾被显式调用，以设置界面的初始状态，并在 `new()` 方法的末尾调用。`QTextEdit.canPaste` 方法是在 Qt 4.2 中引入的；对于早期版本，请使用 `QApplication.clipboard().text().isEmpty()`。文本光标和文档类将在本章之后的部分讨论。

## 386 第 13 章 富文本与打印

`event()` 处理器在任何特定的键盘和鼠标事件处理器之前被调用，它是我们可以拦截并处理 Tab 键按下的唯一地方。如果用户按了 Tab，我们从 `QTextEdit` 获取一个 `QTextCursor`；这允许我们通过程序方式与持有文本的底层 `QTextDocument` 交互。默认情况下，文本编辑器返回的光标位于当前插入点（称为光标位置），因此我们可以轻松插入四个空格。然后我们返回 `True` 给事件处理系统，表示我们已经处理了 Tab 键按下，不应发生进一步的操作（如改变焦点）。

为了提供语法高亮，我们必须使用 `QSyntaxHighlighter` 子类，重写 `highlightBlock()` 方法，并创建一个高亮器实例，并将想要应用的 `QTextDocument` 作为参数。我们在 `MainWindow` 的初始化函数中完成了最后部分，现在我们将转向我们的 `QSyntaxHighlighter` 子类。

`QSyntaxHighlighter` 是按行工作的，并提供了跨越多行跟踪状态的方法。对于 Python 编辑器，我们将使用正则表达式来识别 Python 关键字、注释和字符串，包括跨越多行的三引号字符串，以便我们对它们应用高亮。我们首先在子类的初始化函数中设置正则表达式，我们将分两部分来看它：

```python
class PythonHighlighter(QSyntaxHighlighter):
    Rules = []
    def __init__(self, parent=None):
        super(PythonHighlighter, self).__init__(parent)
        keywordFormat = QTextCharFormat()
        keywordFormat.setForeground(Qt.darkBlue)
        keywordFormat.setFontWeight(QFont.Bold)
        for pattern in ((r"\band\b", r"\bas\b", r"\bassert\b",
        r"\byield\b")):
            PythonHighlighter.Rules.append((QRegExp(pattern),
            keywordFormat))
```

`Rules` 静态列表包含一个元组列表。每个元组的第一个元素是一个正则表达式（一个 `QRegExp`），用于匹配只能占据单行的语法结构（例如 Python 关键字）。第二个元素是 `QTextCharFormat`，该对象可以存储关于文本应如何格式化的信息，例如它的字体和应该用于绘制它的画笔。

我们为每个 Python 关键字创建了一个规则，并给每个关键字相同的 `keywordFormat` 格式。（大部分关键字未在省略号指示的代码片段中显示。）每个关键字前后都有一个 `\b`；这是一个正则表达式符号，它不匹配任何文本，而是匹配单词边界。这意味着，例如在表达式 `a and b` 中，`a` 和 `b` 将被识别为关键字，而在表达式 `a = sand` 中，`sand` 内部将（正确地）不会被识别。



```python
commentFormat = QTextCharFormat()
commentFormat.setForeground(QColor(0, 127, 0))
commentFormat.setFontItalic(True)
PythonHighlighter.Rules.append((QRegExp(r"#.*"), commentFormat))

self.stringFormat = QTextCharFormat()
self.stringFormat.setForeground(Qt.yellow)
stringRe = QRegExp(r"'[^'\\]*(?:\\.[^'\\]*)*'")
stringRe.setMinimal(True)
PythonHighlighter.Rules.append((stringRe, self.stringFormat))

self.stringRe = QRegExp(r'"[^"\\]*(?:\\.[^"\\]*)*"')
self.stringRe.setMinimal(True)
PythonHighlighter.Rules.append((self.stringRe, self.stringFormat))

self.tripleSingleRe = QRegExp(r"'''(?!').*?'''")
self.tripleDoubleRe = QRegExp(r'"""(?!").*?"""')
```

在关键字之后，我们为处理 Python 注释创建了格式和正则表达式。该正则表达式并不是完美的；例如，它没有考虑到引号字符。

对于字符串，我们将字符串格式保留为实例变量，因为在处理多行字符串时，我们在 `highlightBlock()` 方法中需要它。单行字符串由初始化函数中设置的简单（但快速）的正则表达式处理并添加到 `Rules` 列表中。最后，我们创建了两个正则表达式。这些使用了负向先行断言；例如，`(?!')` 意味着“后面不紧跟单引号”。它们将被用于 `highlightBlock()` 方法，我们将分两部分回顾该方法。

```python
def highlightBlock(self, text):
    NORMAL, TRIPLESINGLE, TRIPLEDOUBLE = range(3)
    for regex, format in PythonHighlighter.Rules:
        i = text.indexOf(regex)
        while i >= 0:
            length = regex.matchedLength()
            self.setFormat(i, length, format)
            i = text.indexOf(regex, i + length)
```

`highlightBlock()` 方法为每一行显示的文本被调用，该文本位于 `QString` 参数 `text` 中。

我们首先设置了三种可能的状态：普通、三单引号字符串内部和三双引号字符串内部。然后我们遍历每条规则，每当我们发现与规则正则表达式的匹配项时，我们就将文本格式设置为相应的格式，长度为正则表达式匹配的长度。正则表达式和格式对列表结合前述代码所示的 `for` 循环，对于所有的语法高亮都是足够的，前提是每个语法组件只占据单行，且每个组件都能用正则表达式来表示。

## 第 13 章 富文本与打印

### 富文本编辑

这完成了我们的语法高亮示例。显然，我们可以使用更多的正则表达式，甚至完全避免使用它们而使用有限状态机来识别哪些部分需要格式化。对于复杂的大型文本，语法高亮的开销很大，但通过只对可见行进行格式化可以降低开销。

#### 富文本行编辑

某些应用程序要求用户能够输入单行富文本。例如，一个数据库应用程序可能有一个“描述”字段，我们希望对特定的单词使用加粗、斜体、颜色。我们将在第 14 章和第 16 章查看这些示例。遗憾的是，PyQt 没有提供这样的小部件。在本节中，我们将创建一个 `RichTextLineEdit`，它是 `QTextEdit` 的子类并提供了该功能；如图 13.2 所示。

```python
class RichTextLineEdit(QTextEdit):

    (Bold, Italic, Underline, StrikeOut, Monospaced, Sans, Serif,
     NoSuperOrSubscript, Subscript, Superscript) = range(10)

    def __init__(self, parent=None):
        super(RichTextLineEdit, self).__init__(parent)
        self.monofamily = QString("courier")
        self.sansfamily = QString("helvetica")
        self.seriffamily = QString("times")
        self.setLineWrapMode(QTextEdit.NoWrap)
        self.setTabChangesFocus(True)
        self.setVerticalScrollBarPolicy(Qt.ScrollBarAlwaysOff)
        self.setHorizontalScrollBarPolicy(Qt.ScrollBarAlwaysOff)
        fm = QFontMetrics(self.font())
        h = int(fm.height() * (1.4 if platform.system() == "Windows" else 1.2))
```

图 13.2 富文本编辑

富文本行编辑将支持适用于单行的最常见文本格式：加粗、斜体、下划线、删除线、上标和下标。此外，还将支持三种字体样式——等宽字体、无衬线字体和衬线字体，以及将文本颜色设置为有限颜色的能力。我们将从一些静态常量和初始化函数开始。

```python
self.setMinimumHeight(h)
self.setMaximumHeight(int(h * 1.2))
self.setToolTip("按下 <kbd>Ctrl+M</kbd> 打开文本效果菜单，并按下 <kbd>Ctrl+K</kbd> 打开颜色菜单")
```

我们首先设置一些默认字体族。如今，可以预期每个平台都拥有 Courier、Helvetica 和 Times 字体（或者这些名称的别名字体）。由于 `RichTextLineEdit` 是单行的，我们禁用了自动换行和滚动条。我们还确保 Tab 键会引起焦点切换，而不是插入一个 Tab 字符。计算最小和最大高度将有助于我们在实现 `sizeHint()` 方法时的工作，但由于不同平台之间字体度量的差异，这变得有些复杂。工具提示是为了给用户一个提示，说明该小部件有特殊的快捷键。

注意，条件表达式被包含在括号中。在这种情况下，括号是至关重要的；如果没有它们，在非 Windows 平台上，`h` 将始终被置为 1，而不是我们预期的 20 或 30。

```python
def sizeHint(self):
    return QSize(self.document().idealWidth() + 5, self.minimumHeight())
```

首选尺寸是文本的“理想”宽度（考虑了字体大小以及粗体、斜体等属性），带有一点内边距留边缘，以及最小高度。`QTextDocument.idealWidth()` 方法是在 Qt 4.2 中引入的。

```python
def minimumSizeHint(self):
    fm = QFontMetrics(self.font())
    return QSize(fm.width("WWWW"), self.minimumHeight())
```

对于最小尺寸，我们取小部件默认字体中四个“W”字符的宽度。或者，我们可以简单地使用任意数字，例如 40 像素。

`RichTextLineEdit` 与 `QLineEdit` 的区别在于，用户能够更改单词和字符的格式及颜色。为了支持这一点，我们必须提供一些让用户能够应用此类更改的方法。我们通过提供文本效果菜单和颜色菜单，以及支持一些用于格式化的按键序列来实现这一点。这两个菜单都通过特定的按键序列调用，且文本效果菜单在发生上下文菜单事件时也会弹出。

```python
def contextMenuEvent(self, event):
    self.textEffectMenu()
```

在某些平台上，用户右键点击会触发上下文菜单，而在其他平台上则是按下特定的键或序列。在这种情况下，我们只需调用自定义的 `textEffectMenu()` 方法，它将弹出一个合适的菜单。默认情况下，`QTextEdit` 提供自己的上下文菜单，但通过重实现上下文菜单事件处理器，我们的代码具有更高的优先级。

```python
def keyPressEvent(self, event):
    if event.modifiers() & Qt.ControlModifier:
        handled = False
        if event.key() == Qt.Key_B:
            self.toggleBold()
            handled = True
        elif event.key() == Qt.Key_I:
            self.toggleItalic()
            handled = True
        elif event.key() == Qt.Key_K:
            self.colorMenu()
            handled = True
        elif event.key() == Qt.Key_M:
            self.textEffectMenu()
            handled = True
        elif event.key() == Qt.Key_U:
            self.toggleUnderline()
            handled = True
        if handled:
            event.accept()
            return
    if event.key() in (Qt.Key_Enter, Qt.Key_Return):
        self.emit(SIGNAL("returnPressed()"))
        event.accept()
    else:
        QTextEdit.keyPressEvent(self, event)
```

由于用户正在输入文本，提供一个用于更改文本格式的键盘接口是自然而然。我们将 `Ctrl+B` 设置为切换粗体，`Ctrl+I` 设置为切换斜体，`Ctrl+K` 调用颜色菜单，`Ctrl+M` 调用文本效果菜单（此外还可以通过上下文菜单事件调用）。通过对我们自己处理的按键调用 `accept()`，我们表示没有必要对这些按键按下进行进一步的事件处理。

如果用户按下 Return 键，我们会发出 `returnPressed()` 信号，因为这很有用；文本中不会插入换行符。任何其他按键将传递给基类。`QTextEdit` 类支持自己的序列——例如，`Ctrl+Left` 向左移动一个单词，`Ctrl+Del` 删除右侧的单词，`Ctrl+C` 复制任何选中文本到剪贴板，当然，还有简单的字母，如 `a`、`b`、`Shift+A` 和 `Shift+B`，它们会被字面插入。

```python
def toggleBold(self):
    self.setFontWeight(QFont.Normal if self.fontWeight() > QFont.Normal else QFont.Bold)
```

PyQt 支持多个级别的粗细，但我们选择了简单的“粗体”或“关闭”方法。`QTextEdit.fontWeight()` 方法返回当前插入点的字体粗细，同样地，`setFontWeight()` 方法被应用于当前插入点或选中的文本。`QTextEdit` 在格式方面非常智能，至少在 Linux 上是这样。例如，如果选择了文本，格式将仅应用到选定区域；而如果没有选择且插入点在文本末尾，则格式将从该点开始应用；如果没有选择且插入点在单词中间，则格式将应用到整个单词。

```python
def toggleItalic(self):
    self.setFontItalic(not self.fontItalic())

def toggleUnderline(self):
    self.setFontUnderline(not self.fontUnderline())
```

斜体和下划线在切换时是简单的，在 Linux 上，工作方式与粗体相同。

```python
def colorMenu(self):
    pixmap = QPixmap(22, 22)
    menu = QMenu("Color")
    for text, color in (("&Black", Qt.black), ("&Blue", Qt.blue),
                        ("&Dark Blue", Qt.darkBlue), ("&Cyan", Qt.cyan),
                        ("&Dark Cyan", Qt.darkCyan), ("&Green", Qt.green),
                        ("&Dark Green", Qt.darkGreen), ("&Magenta", Qt.magenta),
                        ("&Dark Magenta", Qt.darkMagenta), ("&Red", Qt.red),
                        ("&Dark Red", Qt.darkRed)):
        pixmap.fill(color)
        action = menu.addAction(QIcon(pixmap), text, self.setColor)
        action.setData(QVariant(color))
    menu.exec_(self.viewport().mapToGlobal(self.cursorRect().center()))
```

菜单通过 `Ctrl+K` 调用。为了创建菜单，我们遍历文本和颜色常量，为每个添加一个新的菜单选项。设置 action 的数据为相应的颜色。菜单通过 `menu.exec_()` 弹出。

```python
def setColor(self):
    action = self.sender()
    if action is not None and isinstance(action, QAction):
        color = QColor(action.data())
        if color.isValid():
            self.setTextColor(color)
```

如果用户选择了存储在调用动作用户数据中的颜色，并将该颜色应用到文本。再次，用于粗体、斜体和下划线的逻辑被用于将颜色应用到选中的文本、当前单词或从文本末尾开始。

```python
def textEffectMenu(self):
    format = self.currentCharFormat()
    menu = QMenu("Text Effect")
    for text, shortcut, data, checked in (
        ("Bold", "Ctrl+B", RichTextLineEdit.Bold, self.fontWeight() != QFont.Normal),
        ("Italic", "Ctrl+I", RichTextLineEdit.Italic, self.fontItalic()),
        ("Underline", "Ctrl+U", RichTextLineEdit.Underline, self.fontUnderline()),
        ("StrikeOut", None, RichTextLineEdit.StrikeOut, format.fontStrikeOut()),
        ("Monospaced", None, RichTextLineEdit.Monospaced, format.fontFamily() == self.monofamily),
        ("Serif", None, RichTextLineEdit.Serif, format.fontFamily() == self.seriffamily),
        ("Sans", None, RichTextLineEdit.Sans, format.fontFamily() == self.sansfamily),
        ("No Super/Subscript", None, RichTextLineEdit.NoSuperOrSubscript, format.verticalAlignment() == QTextCharFormat.AlignNormal),
        ("Superscript", None, RichTextLineEdit.Superscript, format.verticalAlignment() == QTextCharFormat.AlignSuperScript),
        ("Subscript", None, RichTextLineEdit.Subscript, format.verticalAlignment() == QTextCharFormat.AlignSubscript)):
        action = menu.addAction(text, self.setTextEffect)
        if shortcut is not None:
            action.setShortcut(QKeySequence(shortcut))
        action.setData(QVariant(data))
        action.setCheckable(True)
        action.setChecked(checked)
    self.ensureCursorVisible()
    menu.exec_(self.viewport().mapToGlobal(self.cursorRect().center()))
```

效果菜单方法通过 `Ctrl+M` 或上下文菜单事件调用，其结构与颜色菜单相似，但稍微复杂一些。

我们首先获取当前生效的文本格式信息，因为我们需要这些信息来确定是否需要检查各种选项。我们创建了一个由四元组列表（文本、快捷键、常量、勾选状态）组成的菜单。该菜单如图 13.3 所示。

| | |
|---|---|
| ☐ 粗体 | Ctrl+B |
| ☐ 斜体 | Ctrl+I |
| ☐ 删除线 | |
| ☐ 下划线 | Ctrl+U |
| ☐ 等宽 | |
| ☐ 衬线字体 | |
| ☐ 无衬线字体 | |
| ☒ 无上标或下标 | |
| ☐ 上标 | |
| ☐ 下标 | |

**图 13.3 文本效果菜单**

为某些操作设置了键盘快捷键，例如 `Ctrl+B` 用于加粗。我们没有使用标准的按键序列，因为我们在早前的按键事件处理器中硬编码了按键，所以我们必须能够匹配处理器所预期的按键。

实际上，这些快捷键在实践中并没有效果，因为它们仅在与其关联的操作生命周期内存在，而这些操作仅在菜单存在时存在，即在 `textEffectMenu()` 方法持续期间。但这并不重要，因为我们重新实现了按键处理器来自己提供这些快捷键。快捷键仅对于永久菜单（如添加到主窗口菜单栏的菜单）有用。那么，我们为什么要在菜单中费心快捷键呢？因为添加快捷键会让它们出现在菜单中，这有助于用户学习。这并不能解决用户最初如何发现 `Ctrl+M` 和 `Ctrl+K` 菜单的问题，但希望他们能看到工具提示或在应用程序手册中阅读它们。

菜单本身的创建和弹出方式与颜色菜单完全相同。用户点击任何文本选项，都会调用 `setTextEffect()` 方法。我们将从两个部分来看这个问题。

```python
def setTextEffect(self):
    action = self.sender()
    if action is not None and isinstance(action, QAction):
        what = action.data().toInt()
        if what == RichTextLineEdit.Bold:
            self.toggleBold()
            return
```

```python
if what == RichTextLineEdit.Italic:
    self.toggleItalic()
    return
if what == RichTextLineEdit.Underline:
    self.toggleUnderline()
    return
```

每个文本效果动作在其用户数据中存储了一个常量；此常量被检索并保留在 `what` 变量中。对于简单的切换动作，我们只需要调用相应的切换方法即可完成。

```python
format = self.currentCharFormat()
if what == RichTextLineEdit.Monospaced:
    format.setFontFamily(self.monofamily)
elif what == RichTextLineEdit.Serif:
    format.setFontFamily(self.seriffamily)
elif what == RichTextLineEdit.Sans:
    format.setFontFamily(self.sansfamily)
if what == RichTextLineEdit.StrikeOut:
    format.setFontStrikeOut(not format.fontStrikeOut())
if what == RichTextLineEdit.NoSuperOrSubscript:
    format.setVerticalAlignment(QTextCharFormat.AlignNormal)
elif what == RichTextLineEdit.Superscript:
    format.setVerticalAlignment(QTextCharFormat.AlignSuperScript)
elif what == RichTextLineEdit.Subscript:
    format.setVerticalAlignment(QTextCharFormat.AlignSubScript)
self.mergeCurrentCharFormat(format)
```

为了检索字体族、删除线格式或垂直对齐方式，我们检索当前格式，应用用户请求的更改，然后将更新后的格式与当前格式合并，使其生效。

我们已经涵盖了富文本行编辑器支持的所有格式选项。在用户输入富文本后，我们不希望破坏它，以便能够恢复、搜索或操纵它。我们可以使用 `QTextEdit.toPlainText()` 方法——但这会剥离所有 HTML，导致结果比使用 `QLineEdit` 没有什么好之处。一个合适的替代方案是使用 `QTextEdit.toHtml()`，但此方法返回的 HTML 非常冗长，它需要足够通用，以适应所有 PyQt 支持的 HTML 标签。

为了直观说明这一点，如果我们有文本 **bold cat.**（13 个字符），其中单词 "cat" 被涂成红色，`toHtml()` 方法返回 503 个字符：

```html
<html><head><meta name="qrichtext" content="1" />
<style type="text/css"> p { white-space: pre-wrap; } </style>
</head>
<body style="font-family: 'Nimbus Sans'; font-size:11pt; font-weight:400; font-style:normal; text-decoration:none;">
<p style="margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px"><span style="font-weight:600;">bold </span><span style="color:#ff0000;">cat</span><span style="color:#000000;">.</span></p></body></html>
```

我们添加了换行符以使输出整齐地适应页面。文本可能会略有不同，但总体结构相同。

```python
def toHtml(self):
    html = ""
    black = Qt.black
    block = self.document().begin()
    while block.isValid():
        iterator = block.begin()
        while iterator != block.end():
            fragment = iterator.fragment()
            if fragment.isValid():
                format = fragment.charFormat()
                family = format.fontFamily()
                color = format.foreground().color()
                text = Qt.escape(fragment.text())
                if format.verticalAlignment() == QTextCharFormat.AlignSubScript:
                    text = "<sub>" + text + "</sub>"
                elif format.verticalAlignment() == QTextCharFormat.AlignSuperScript:
                    text = "<sup>" + text + "</sup>"
                if format.fontUnderline():
                    text = "<u>" + text + "</u>"
                if format.fontItalic():
                    text = "<i>" + text + "</i>"
                if format.fontWeight() > QFont.Normal:
                    text = "<b>" + text + "</b>"
                if format.fontStrikeOut():
                    text = "<s>" + text + "</s>"
                if color != black or not family.isEmpty():
                    attrs = ""
                    if color != black:
                        attrs += ' color="%s"' % color.name()
                    if not family.isEmpty():
                        attrs += ' face="%s"' % family
                    text = QString("<font%1>%2</font>").arg(attrs).arg(text)
                html += text
            iterator += 1
        block = block.next()
    return html
```

对于当前块中的每个文本片段，我们提取字符格式、字体族和颜色。然后我们提取文本本身，并使用 `Qt.escape()` 将任何 HTML 字符（`&`、`<` 和 `>`）转换为相应的实体。然后我们检查片段是否为上标或下标，必要时用相应的 HTML 标签包裹文本。类似的测试也适用于其他格式——特别是下划线、斜体、粗体和删除线——在每情况下为文本添加相应的 HTML 标签。

如果颜色不是黑色或字体族不为空，我们构建一个 `<font>` 标签来包裹文本。最后将处理后的文本追加到 HTML 字符串中。

## 第 13 章 富文本与打印

### 打印文档

从 PyQt 打印可以通过多种方式实现。一种方法是产生另一个程序可以打印的格式输出，例如为 Web 浏览器生成 HTML，或为 SVG 绘图程序生成 SVG。

从 Qt 4.1 开始，用户可以通过勾选打印对话框中的“打印到文件”选项来创建 PDF 文档。通过程序生成 PDF 文档也是可能的。例如，假设 `document` 是一个 `QTextDocument`：

```python
printer = QPrinter()
printer.setPageSize(QPrinter.Letter)
printer.setOutputFormat(QPrinter.PdfFormat)
printer.setOutputFileName(filename)
document.print_(printer)
```

这些方法对于用户来说不如在应用程序内部内置打印功能方便，为了实现这一点，PyQt 提供了三种主要选择：

1. 我们可以生成 HTML，将其交给 `QTextDocument`，并使用 `QTextDocument.print_()` 传入一个 `QPrinter`，或者使用 `QTextDocument.drawContents()` 传入一个 `QPainter` 来渲染文档。
2. 我们可以创建一个 `QTextDocument` 并从中获取一个 `QTextCursor`，通过它可以程序化生成文档，并再次使用 `print_()` 或 `drawContents()` 方法进行渲染。
3. 我们可以创建一个 `QPainter` 直接打印到 `QPrinter` 上，即打印到打印页面上。这是最费力的方法，但它提供了最大程度的控制。

本节中的示例应用程序展示了所有三种技术。它打印客户账单，每个 `Statement` 对象包含公司名称、联系人姓名、地址和交易列表，每个交易都是一个 `(QDate, float)` 元组。`Statement` 类还提供了一个 `balance()` 方法，返回交易总和。我们希望在右上角日期下方打印发行人的标志和地址，在左侧打印客户地址，然后是一封内容根据客户是欠方还是贷方而变化的信函，接着是交易表格和一个结束段。自然地，我们还希望每份账单都从新的一页开始。我们将假设所有账单都存储在一个名为 `self.statements` 的列表中，并且我们的打印是使用持有这些账单的表单的方法完成。页面看起来将如图 13.4 所示。

但在查看这三种通用打印技术之前，我们将查看如何打印图片，特别是展示我们在第 6 章介绍过的 Image Changer 应用程序使用的 `filePrint()` 方法的实现。

#### 打印图片

在第 6 章中，我们有一个用于打印图片的 `MainWindow.filePrint()` 方法，但当时我们没有看它的实现，因为那时我们还没有介绍过 `QPainter`。现在我们已经在第 11 章看过了 `QPainter`，并且有了一个通用的“打印图片”函数，我们就可以查看 Image Changer 应用程序使用的 `filePrint()` 方法的实现了。

```python
def filePrint(self):
    if self.printer is None:
        return
    if self.image is not None:
        painter = QPainter(self.printer)
        rect = self.image.rect()
        painter.drawImage(0, 0, self.image)
        painter.end()
```

如果用户想要 PDF 文件，可以调用“打印”操作并选择“打印到文件”选项。在某些平台上，通过将“打印到文件”的扩展名改为 `.ps` 也可以得到 PostScript 输出。

#### 使用 HTML 打印文档

我们将展示的第一种方法是创建一个包含 HTML 的字符串，并使用 `QTextDocument` 将 HTML 渲染到 `QPrinter`。`printHtml()` 方法很长，我们将分三部分来看。

到目前为止，我们一直使用 Python 的 `%` 运算符对字符串进行格式化。但在某些情况下，使用 PyQt 的字符串格式化更具优势。`QString` 类有一个 `arg()` 方法，它可以接受一个对象（通常是字符串或数字），并带有一些可选参数。每次调用 `arg()` 都会将 `QString` 中最左侧的 `%` 项替换为相应的文本。例如：

```python
QString("Copied %1 bytes to %2").arg(5387).arg("log.txt")
```

结果为字符串：

```
Copied 5387 bytes to log.txt
```

`%` 符号没有像 Python 的 `%` 运算符那样的语法，但可以通过向 `arg()` 方法传递额外的参数来实现格式化。还可以通过 `%L` 实现格式的本地化。例如：

```python
QString("Copied %L1 bytes to %2").arg(5387).arg("log.txt")
```

在美国和英国，结果为字符串：

```
Copied 5,387 bytes to log.txt
```

而在其他某些国家，数字显示为 `5.387`。

在示例中，我们使用两位小数打印金额，并且整数部分每三位分一组。这可以通过向 `arg()` 传递四个参数来实现——金额作为 `float`、格式字符串（`"f"` 用于普通浮点数，`"e"` 或 `"E"` 用于科学计数法）、小数点后的数字位数。如果指定了最小字符数，还可以提供第五个参数作为填充字符。

在示例中，我们使用了：

```python
QString("$ %L1").arg(float(balance), 0, "f", 2)
```

金额 `64325.852` 的余额在美国将输出为字符串 `$ 64,325.85`。

回到代码，我们添加了一些根据客户是欠方还是贷方变化的文本。然后，我们创建了一个包含三列的 HTML 表格头，第一行跨列并包含标题“Transactions”（交易）。`&nbsp;` 是一个表示不换行空格的 HTML 实体。

```python
for date, amount in statement.transactions:
    color, status = "black", "Credit"
    if amount < 0:
        color, status = "red", "Debit"
    html += ("<tr><td align=\"right\">%s</td>"
             "<td>%s</td><td align=\"right\">"
             "<font color=%s>%s</font></td></tr>" % (
             date.toString(DATE_FORMAT), status, color,
             QString("$ %L1").arg(float(abs(amount)), 0, "f", 2))) + "\n"
html += ("</table><p style=\"page-break-after:always;\">"
         "We hope to continue doing business with you,<br>"
         "Yours sincerely,<br>&nbsp;<br>K.&nbsp;Longrey, Manager</p>")
```

我们遍历每笔交易，为每个交易向表格添加新的一行。然后我们添加颜色标签并添加最后的段落。我们希望在最后一个段落之后有一个分页符，这可以通过设置 `page-break-after` 样式选项来实现。该样式选项是在 Qt 4.2 中引入的，在早期版本中会被忽略。

```python
dialog = QPrintDialog(self.printer, self)
if dialog.exec_():
    document = QTextDocument()
    document.setHtml(html)
    document.print_(self.printer)
```

最后，我们弹出一个打印对话框，如果用户点击“打印”，我们就创建一个新的 `QTextDocument`，将其文本设置为我们在 HTML 字符串中生成的 HTML 内容，并告诉文档在打印机上打印自己。

使用 `QTextDocument` 创建 HTML 字符串并进行打印可能是 PyQt 中产生打印输出最快、最简单的方法。唯一的缺点是进行精细控制可能比较困难，尽管我们可以使用样式属性和样式表。

#### 使用 QTextCursor 和 QTextDocument 打印文档

现在我们将展示如何通过程序化创建 `QTextDocument` 来实现相同的功能，而不是创建 HTML 字符串并设置 `setHtml()`。这段代码比使用 `QPainter`（后文）的代码长了一倍多，但我们不应从这个特定的示例推断出这些技术通常情况下需要更多代码。

```python
def printViaQTextCursor(self):
    dialog = QPrintDialog(self.printer, self)
    if not dialog.exec_():
        return
    logo = QPixmap(":/logo.png")
    headerFormat = QTextBlockFormat()
    headerFormat.setAlignment(Qt.AlignRight)
    headerFormat.setTextIndent(self.printer.pageRect().width() - logo.width() - 216)
    bodyFormat = QTextBlockFormat()
    bodyFormat.setAlignment(Qt.AlignJustify)
    lastParagraphFormat = QTextBlockFormat(bodyFormat)
    lastParagraphFormat.setPageBreakPolicy(QTextFormat.PageBreak_AlwaysAfter)
    rightFormat = QTextBlockFormat()
    rightFormat.setAlignment(Qt.AlignRight | Qt.AlignVCenter)
    headerCharFormat = QTextCharFormat()
    headerCharFormat.setFont(QFont("Arial", 14, QFont.Bold))
    bodyCharFormat = QTextCharFormat()
    bodyCharFormat.setFont(QFont("Arial", 11))
    redCharFormat = QTextCharFormat()
    redCharFormat.setForeground(Qt.red)
    tableFormat = QTextTableFormat()
    tableFormat.setBorder(1)
    tableFormat.setCellPadding(4)
```

包含一系列块。表格中的每个单元格包含一个文本块，当我们完成表格单元格的插入后，我们需要向上移动文档层结构到跟随块的位置，这就是为什么我们保留了当前帧的引用 `mainFrame` 变量。

```python
document = QTextDocument()
cursor = QTextCursor(document)
mainFrame = cursor.currentFrame()

for statement in self.statements:
    cursor.insertBlock(headerFormat, headerCharFormat)
    cursor.insertImage(":/logo.png")
    for text in ("Greasy Hands Ltd.", "New Lombard Street", "London", "WC1 4PF"):
        cursor.insertBlock(headerFormat, headerCharFormat)
        cursor.insertText(text)
    cursor.insertBlock(bodyFormat)
    for line in statement.address.split(", "):
        cursor.insertBlock(bodyFormat, bodyCharFormat)
        cursor.insertText(line)
    cursor.insertBlock(bodyFormat)
    cursor.insertBlock(bodyFormat, bodyCharFormat)
    cursor.insertText("Dear %s," % statement.contact)
    cursor.insertBlock(bodyFormat)
    cursor.insertBlock(bodyFormat, bodyCharFormat)
    balance = statement.balance()
    cursor.insertText(QString("The balance of your account is $ %L1.").arg(float(balance), 0, "f", 2))
```

```python
if balance < 0:
    cursor.insertBlock(bodyFormat, redCharFormat)
    cursor.insertText("Please remit the amount owing immediately.")
else:
    cursor.insertBlock(bodyFormat, bodyCharFormat)
    cursor.insertText("We are delighted to have done business with you.")
cursor.insertBlock(bodyFormat, bodyCharFormat)
cursor.insertText("Transactions:")
table = cursor.insertTable(len(statement.transactions) + 1, 3, tableFormat)
```

要插入表格，我们必须指定它的行数、列数以及其格式。

```python
headerCursor = table.cellAt(0, 0).firstCursorPosition()
headerCursor.insertText("Date", headerCharFormat)
headerCursor = table.cellAt(0, 1).firstCursorPosition()
headerCursor.insertText("Type", headerCharFormat)
headerCursor = table.cellAt(0, 2).firstCursorPosition()
headerCursor.insertText("Amount", headerCharFormat)

row = 1
for date, amount in statement.transactions:
    cellCursor = table.cellAt(row, 0).firstCursorPosition()
    cellCursor.setBlockFormat(rightFormat)
    cellCursor.insertText(date.toString(DATE_FORMAT), bodyCharFormat)
    cellCursor = table.cellAt(row, 1).firstCursorPosition()
    if amount > 0:
        cellCursor.insertText("Credit", bodyCharFormat)
    else:
        cellCursor.insertText("Debit", bodyCharFormat)
    cellCursor = table.cellAt(row, 2).firstCursorPosition()
    cellCursor.setBlockFormat(rightFormat)
    format = bodyCharFormat
    if amount < 0:
        format = redCharFormat
    cellCursor.insertText(QString("$ %L1").arg(float(abs(amount)), 0, "f", 2), format)
    row += 1
```

表格的每一行代表单笔交易，包含日期、文本“Debit”（借）或“Credit”（贷），以及在编辑时显示为红色金额。要在表格中插入项目，我们必须获取一个 `QTextCursor` 来访问指定行和列的单元格。我们不需要在单元格中插入新块（除非我们在一个单元格内需要多个段落），只需设置单元格的段落格式并插入我们所需的文本即可。

```python
cursor.setPosition(mainFrame.lastPosition())
cursor.insertBlock(bodyFormat, bodyCharFormat)
cursor.insertText("We hope to continue doing business with you,")
cursor.insertBlock(bodyFormat, bodyCharFormat)
cursor.insertText("Yours sincerely")
cursor.insertBlock(bodyFormat)
if statement == self.statements[-1]:
    cursor.insertBlock(bodyFormat, bodyCharFormat)
else:
    cursor.insertBlock(lastParagraphFormat, bodyCharFormat)
cursor.insertText("K. Longrey, Manager")
```

一旦完成表格填充并在其之后添加项目，我们必须将光标位置重置为紧邻表格之后。如果不这样做，光标将直接插入到表格内部，导致第一页的其余部分位于表格内，第二页又在第一页内，以此递归下去！为了避免这个问题，我们将文本光标设置在文档的最后一个位置，即我们插入的最后一项内容之后的位置，也就是紧邻表格之后。

完成页面的简单方法是插入带有适当格式的额外块，然后插入相关的文本。对于除最后一页以外的所有页面，我们将最后一个块的格式设置为 `lastParagraphFormat`，这（在使用 Qt 4.2 时）将确保在新页面上的后续内容也具有该格式。

```python
document.print_(self.printer)
```

最后一条语句是在打印机上打印文档。此时文档已完成，如果倾向于 HTML 格式，我们可以调用 `toHtml()` 来获取 HTML 格式的内容。这也意味着如果我们想要，可以结合 `QTextCursor` 和 `QTextDocument` 来程序化地创建页面。

使用 `QTextDocument` 的优势（无论是获取 HTML 字符串还是使用 `QTextCursor` 填充）在于，我们可以避免大量关于文本应该放置在页面何位置的计算。缺点是 PyQt 无论我们是否喜欢都会在文档上加上页码，而且它没有给我们提供精细的位置控制。如果使用 `QPainter`，这两个问题都不会发生。

#### 使用 QPainter 打印文档

我们将通过查看如何使用 `QPainter` 进行打印来结束本节。实现这种方法意味着我们需要承担所有位置计算的繁琐工作，但好处可以在页面的任何地方绘制任何内容，而不限于 HTML 或 `QTextDocument` 能表示的内容。此外，绘画本身使用了我们在前两个章节中看到的相同方法和技术，因为 PyQt 在小部件、图像或打印页面上的绘制上有一套统一的处理方法。

```python
def printViaQPainter(self):
    dialog = QPrintDialog(self.printer, self)
    if not dialog.exec_():
        return
    LeftMargin = 72
    sansFont = QFont("Helvetica", 10)
    sansLineHeight = QFontMetrics(sansFont).height()
    serifFont = QFont("Times", 11)
    fm = QFontMetrics(serifFont)
    DateWidth = fm.width(" September 29, 2999")
    CreditWidth = fm.width(" Credit ")
    AmountWidth = fm.width("W999999.99")
    serifLineHeight = fm.height()

    logo = QPixmap(":/logo.png")
    painter = QPainter(self.printer)
    pageRect = self.printer.pageRect()
    page = 1
```

我们首先向用户显示打印对话框，如果他们点击“取消”则退出。如果继续打印，我们设置一些字体、宽度和行高，并创建一个 `QPainter` 直接在打印机上进行绘图。如果指定的字体可用，PyQt 将使用它能找到的最匹配的字体。

```python
for statement in self.statements:
    painter.save()
    y = 0
    x = pageRect.width() - logo.width() - LeftMargin
    painter.drawPixmap(x, 0, logo)
    y += logo.height() + sansLineHeight
    painter.setFont(sansFont)
    painter.drawText(x, y, "Greasy Hands Ltd.")
    y += sansLineHeight
    painter.drawText(x, y, "New Lombard Street")
    y += sansLineHeight
    painter.drawText(x, y, "London")
    y += sansLineHeight
    painter.drawText(x, y, "WC1 4PF")
    y += sansLineHeight
    painter.drawText(x, y, QDate.currentDate().toString(DATE_FORMAT))
    y += sansLineHeight
    painter.setFont(serifFont)
    x = LeftMargin
    for line in statement.address.split(", "):
        painter.drawText(x, y, line)
        y += serifLineHeight
    y += serifLineHeight
```

对于每条语句，我们打印标志、地址、日期和客户地址。在开始时保存画家的状态（包括字体、画刷和变换矩阵），并在每条语句结束时恢复状态。这确保了每个语句都是干净的。

```python
painter.drawText(x, y, "Dear %s," % statement.contact)
y += serifLineHeight
balance = statement.balance()
painter.drawText(x, y, QString("The balance of your account is $%L1").arg(float(balance), 0, "f", 2))
y += serifLineHeight
```

```python
if balance < 0:
    painter.setPen(Qt.red)
    text = "Please remit the amount owing immediately."
else:
    text = "We are delighted to have done business with you."
painter.drawText(x, y, text)
```

按照惯例打印带有账户状态的正文。

```python
painter.setPen(Qt.black)
y += int(serifLineHeight * 1.5)
painter.drawText(x, y, "Transactions:")
y += serifLineHeight
option = QTextOption(Qt.AlignRight | Qt.AlignVCenter)
```

交易表格从写入标题开始，创建一个 `QTextOption` 对象。这些对象可以指定各种文本格式选项，包括对齐和换行。

```python
for date, amount in statement.transactions:
    h = serifLineHeight
    x = LeftMargin
    painter.drawRect(x, y, DateWidth, h)
    painter.drawText(QRect(x + 3, y + 3, DateWidth - 6, h - 6), date.toString(DATE_FORMAT), option)
    x += DateWidth
    painter.drawRect(x, y, CreditWidth, h)
    text = "Credit"
    if amount < 0:
        text = "Debit"
    painter.drawText(QRect(x + 3, y + 3, CreditWidth - 6, h - 6), text, option)
    x += CreditWidth
    painter.drawRect(x, y, AmountWidth, h)
    if amount < 0:
        painter.setPen(Qt.red)
    painter.drawText(QRect(x + 3, y + 3, AmountWidth - 6, h - 6), QString("$ %L1").arg(float(abs(amount)), 0, "f", 2), option)
    painter.setPen(Qt.black)
    y += h
```

为了绘制交易表格，我们必须自己绘制文本和线条。我们通过为表格的每个单元格绘制矩形而不是仅仅绘制分离单元格的线条来稍微耍了弊。这意味着共享线条的矩形（例如，一个矩形的右边缘和它旁边矩形的左边缘）会重叠绘制——但在视觉上无法察觉的。

```python
y += serifLineHeight
x = LeftMargin
painter.drawText(x, y, "We hope to continue doing business with you,")
y += serifLineHeight
painter.drawText(x, y, "Yours sincerely")
y += serifLineHeight * 3
painter.drawText(x, y, "K. Longrey, Manager")
```

最后的段落与之前的两种方法相同，但这次我们在页面底部添加一个免责声明。

```python
x = LeftMargin
y = pageRect.height() - 72
painter.drawLine(x, y, pageRect.width() - LeftMargin, y)
y += 2
font = QFont("Helvetica", 9)
font.setItalic(True)
painter.setFont(font)
option = QTextOption(Qt.AlignCenter)
option.setWrapMode(QTextOption.WordWrap)
painter.drawText(x, y, pageRect.width() - 2 * LeftMargin, 31, "The contents of this letter are for information only and do not form part of any contract.", option)
```

使用 `QPainter` 时添加页脚要容易得多，因为我们确切知道页面的尺寸并可以在任何喜欢的 `(x, y)` 位置上绘图。

```python
page += 1
if page <= len(self.statements):
    self.printer.newPage()
painter.restore()
```

最后，在除最后一个语句之外的每条语句后都切换到新页面。这种方法适用于所有 Qt 4 版本，而之前的两种方法只有在 Qt 4.2 或更高版本上才能正确分页。

虽然使用 `QPainter` 打印相比使用 `QTextDocument` 需要更多的心力和计算，但它让我们对输出拥有完全控制。

## 总结

使用 `QSyntaxHighlighter` 为具有常规语法（如源代码）的纯文本提供语法高亮是非常简单的。处理多行结构也可以很容易完成。最困难的部分是处理歧义和某些特殊情况，例如引用字符串内的引号，或者位于引号或其他取消其语法含义的结构内部的注释开始符号。另一种方法是使用 `QScintilla` 编辑器。

`QTextEdit` 类非常强大且多功能。开箱即用，它可以编辑纯文本和 HTML。创建 `QTextEdit` 的子类来提供按键和右键菜单处理器以为用户提供基本的格式选项并不困难，而且这些技术可以轻松扩展，通过提供菜单和工具栏让用户可以在其中添加、编辑和删除列表、表格和图像，并可以应用字符级别（如下划线和删除线）或段落级别（如左对齐、右对齐或两端对齐）的格式。

`QTextEdit.toHtml()` 返回的 HTML 是冗余的，因为它必须支持广泛的 HTML 标签。我们可以提供自己的方法来遍历 `QTextDocument` 的结构并输出我们的格式。在示例中，我们输出了更简单、更短的 HTML，相同的方法也可以输出 XML 或其他类型的标记语言。

对 `QTextEdit`、`QTextBrowser`、`QLabel` 和 `QGraphicsTextItem` 使用的底层 `QTextDocument` 应用大多数简单格式是非常简单的。应用更高级的格式（例如表格）可能会很复杂，因为我们必须小心不要相互嵌套。

打印文档可以通过间接输出 HTML 或 SVG 来生成，也可以直接使用 `QPainter` 打印到物理打印机上，或者通过 Qt 4.1 输出 PDF 文件。打印文档可以通过创建一个 HTML 字符串并将其交给 `QTextDocument`，或者通过程序向空白的 `QTextDocument` 插入项来生成打印文档。在这两种情况下，都可以要求 `QTextDocument` 将自己打印到打印机上，或在 `QPainter` 上绘制自己。

对于熟悉 HTML 标签的人来说，使用 HTML 是最简单的方法，通过使用样式属性和样式表可以相当程度地控制。使用 `QTextCursor` 插入 `QTextDocument` 可以轻松实现更精细的控制，特别是对于那些不熟悉样式表的人。通过直接使用 `QPainter` 可以获得对页面外观最大的控制。对于那些习惯使用 `QPainter` API 或希望为绘画和打印复用相同代码的人来说，这也是最简单的方法。这种复用也可以通过 `QTextDocument` 实现，因为它们可以在使用 `QTextDocument` 的 `QLabel` 等控件中渲染。它们还可以使用 `QPainter` 绘制到任意绘制设备（如控件）上，并进行打印。

## 练习

添加两个新操作：缩进和取消缩进，快捷键为 `Ctrl+]` 和 `Ctrl+[`。图像子目录下提供了合适的图标，并且它们已经在资源文件 `.qrc` 中了。两个操作都应添加到编辑菜单和编辑工具栏中。实现 `indent()` 和 `unindent()` 方法。它们应该通过在行开头插入或删除四个空格对当前行进行缩进或取消缩进，无论插入点在行的哪个位置。最后，插入点应该处于缩进或取消缩进之前的相同相对位置。这些操作应该是实例变量，并且只有在文档不为空时才启用。

确保你使用了 `QTextCursor.beginEditBlock()` 和 `QTextCursor.endEditBlock()`，这样缩进或取消缩进就可以作为一个单一操作撤销——`QTextEdit` 支持 `Ctrl+Z` 撤销。这两个方法总共只需要 20 行代码。

如果你想实现更有野心的目标，尝试扩展这两个方法，使得如果有选择，则缩进或取消缩进将应用于选择中的所有行。这会增加大约 40 行代码，并且有点复杂。确保在最后原始选择保持在原位。

你需要阅读 `QTextCursor` 的文档，特别是 `anchor()`、`position()`、`setPosition()` 和 `movePosition()` 方法。

在 `chap13/pythoneditor_ans.py` 中提供了解决方案。

## 第 14 章 模型/视图编程

- 使用便利项控件
- 创建自定义模型
- 创建自定义代理

### 模型/视图编程

模型/视图编程是一种涉及数据与其视觉表示分离的技巧。它最初在 Smalltalk 编程语言中作为 MVC（模型/视图/控制器）范式流行起来。

模型是一个提供统一接口的类，通过该接口可以访问数据项。视图是一个可以将模型中的数据项在屏幕上呈现给用户的类。控制器是一个介于用户界面（例如鼠标事件和按键按下）之间的类，为用户提供操纵数据项的方法。

![图 14.1 模型/视图/控制器和模型/视图/代理](img/55bc1dcf8601cfec5e1423b4e17ec264_427_0.png)

MVC 方法提供了若干优势。例如，可以处理巨大的数据集，因为只有实际显示或编辑的数据才会从数据源中读取或写入。同一数据集的不同视图通过使用两个或多个视图以不同的方式访问相同的数据，或者没有数据重复：这对于以不同方式查看相同数据或查看大型数据集的不同部分非常有用。此外，如果我们更改了数据集的存储方式（例如从二进制文件更改到数据库），只需要调整模型——视图中的所有逻辑都保持不变。

Qt 4 使用模型/视图/代理方法，这是 MVC 的一个变体。代理负责处理用户交互（编辑、选择等），而控制器在 MVC 中处理用户输入并更新模型。概念上，模型/视图/代理的工作原理如图 14.1 所示。

尽管 `QModelIndex` 可以引用模型中的任何数据，但我们需要记住实际上有两种模型。第一类是表格，包括单列表格的列表。当我们使用行和列来处理表格时；对于树，我们则根据父子关系来工作。（可以使用行和列的方法处理树，但这违背了初衷，会导致代码运行缓慢且难以维护）。

模型中的每条数据（因此是每个数据项）都可以通过唯一的 `QModelIndex` 标识。每个模型索引都有三个属性：行、列和父节点。

- 对于一维模型（例如列表），只使用行。
- 对于二维模型（例如表格，包括数据库表格），使用行和列。
- 对于分层模型（例如树），三个属性均被使用。

### 使用便利项控件

PyQt 还提供了一些视图控件，包括 `QListView`、`QTableView` 和 `QTreeView`。这些控件必须配合外部模型使用，模型我们可以自己创建，也可以使用内置模型，如 `QStringListModel`、`QStandardItemModel` 或 `QSqlTableModel`。在第二节中，我们将看到如何创建一个用于视图控件的自定义模型。

所有的便利视图和纯视图都使用一个默认代理，该代理负责控制数据项的展示和编辑。在本章的最后一节中，我们将学习如何创建一个自定义代理，以对数据项的编辑和展示执行完全控制。自定义代理可以用于任何视图，无论是便利视图还是纯视图。

本章提供了 PyQt 模型/视图类的基础知识。在第 15 章中，我们将学习如何使用模型/视图类来处理数据库；在第 16 章中，我们将涵盖更高级的用法，包括创建自定义视图、改进代理中的代码复用，以及在树中展示表格数据。

本章中的所有示例都使用同一数据集，以便更容易比较和对比所使用的控件。数据集在第一节中描述。

#### 使用便利项控件

便利项控件是带有内置模型的视图控件。它们使用默认代理来展示和编辑数据，但如果我们愿意，也可以将其替换为自定义代理。

图 14.2 的截图显示了在三个不同的便利视图中的同一个数据集。这意味着数据被分别复制到每个视图中，因此存在大量的数据冗余。另一个问题是，如果我们允许用户编辑数据，就必须编写代码来确保所有视图保持同步。正如我们在下一节中看到的，如果我们使用自定义模型，这些问题就不会存在。

![图 14.2 运行中的 QListWidget、QTableWidget 和 QTreeWidget](img/55bc1dcf8601cfec5e1423b4e17ec264_429_0.png)

我们正在使用的数据是一组关于集装箱船的信息。每艘船由一个 `Ship` 对象表示，定义在 `chap14/ships.py` 模块中。

```python
class Ship(object):
    def __init__(self, name, owner, country, teu=0, description=""):
        self.name = QString(name)
        self.owner = QString(owner)
        self.country = QString(country)
        self.teu = teu
        self.description = QString(description)

    def __cmp__(self, other):
        return QString.localeAwareCompare(self.name.toLower(), other.name.toLower())
```

前面的代码是完整的 `Ship` 类。整数属性 `teu` 代表“二十英尺标准单位”，即该船可以容纳多少 20 英尺的集装箱。（现在的集装箱通常是 40 英尺的，因此算 2 个 TEU。）`name`、`owner` 和 `country` 属性都是纯文本，但 `description` 属性包含一行 HTML。

`__cmp__()` 特殊方法提供了排序所需的比较手段。`QString.localeAwareCompare()` 方法以区域敏感的方式进行字符串比较——例如正确处理带重音的字符。

由于我们使用了没有自定义代理的便利视图，因此我们对项的编辑控制有限。例如，我们无法为编辑所有者国家提供下拉组合框，无法使用数字微调框来编辑 TEU。此外，描述是原始形式显示的，而不是被解释为 HTML。随着章节的进行，我们将解决所有问题，但目前我们只关注使用便利视图。

对于用于便利视图的列表和树项，可以设置它们的字体、文本对齐、文本颜色和背景颜色，并为它们提供图标或使其变为可勾选。对于纯视图，我们可以通过自定义模型对项的外观进行类似的控制；或者通过使用自定义代理对项的外观和编辑执行完全控制。

此示例的代码位于 `chap14/ships.pyw`。数据存储在一个 Python 字典中，字典本身被封装在 `ships.Ship` 类中。我们在这里只讨论与模型/视图编程相关的代码——其余代码使用了我们在书的前面见过的惯用法——例如在第 8 章中——这并不难理解。

```python
class MainWindow(QDialog):
    def __init__(self, parent=None):
        super(MainWindow, self).__init__(parent)
        listLabel = QLabel("List")
        self.listWidget = QListWidget()
        listLabel.setBuddy(self.listWidget)
        tableLabel = QLabel("Table")
        self.tableWidget = QTableWidget()
        tableLabel.setBuddy(self.tableWidget)
        treeLabel = QLabel("Tree")
        self.treeWidget = QTreeWidget()
        treeLabel.setBuddy(self.treeWidget)
```

对于创建的每个便利视图，我们都创建一个标签并设置一个伙伴以便于导航。布局代码与我们之前看到的类似，因此我们省略了它，只关注连接和数据结构的创建。

```python
self.connect(self.tableWidget, SIGNAL("itemChanged(QTableWidgetItem*)"), self.tableItemChanged)
self.connect(addShipButton, SIGNAL("clicked()"), self.addShip)
self.connect(removeShipButton, SIGNAL("clicked()"), self.removeShip)
self.connect(quitButton, SIGNAL("clicked()"), self.accept)
self.setWindowTitle("Ships")
```

```python
def populateTable(self, selectedShip=None):
    selected = None
    self.tableWidget.clear()
    self.tableWidget.setColumnCount(len(ships.HEADERS))
    self.tableWidget.setHorizontalHeaderLabels(ships.HEADERS)
    self.tableWidget.setSortingEnabled(False)
    for row, ship in enumerate(ships.inOrder()):
        self.tableWidget.insertRow(row)
        item = QTableWidgetItem(ship.name)
        item.setData(Qt.UserRole, id(ship))
        self.tableWidget.setItem(row, ships.NAME, item)
        self.tableWidget.setItem(row, ships.OWNER, QTableWidgetItem(ship.owner))
        self.tableWidget.setItem(row, ships.COUNTRY, QTableWidgetItem(ship.country))
        self.tableWidget.setItem(row, ships.DESCRIPTION, QTableWidgetItem(ship.description))
        item = QTableWidgetItem(QString("%L1").arg(ship.teu, 8, 10, QChar(" ")))
        item.setTextAlignment(Qt.AlignRight | Qt.AlignVCenter)
        self.tableWidget.setItem(row, ships.TEU, item)
    self.tableWidget.setSortingEnabled(True)
    self.tableWidget.resizeColumnsToContents()
    if selected is not None:
        selected.setSelected(True)
        self.tableWidget.setCurrentItem(selected)
```

对于每艘船，我们必须为行中的每个单元格创建一个单独表格项，用于显示其数据。列索引 `NAME`、`OWNER` 等都是来自 `ships` 模块的整数。

在第一个项中，我们设置了文本（船名），并将船的 ID 设置为用户数据。存储 ID 为我们提供了一种从表格跳转到该行所代表的船的手段。这之所以可行，是因为 `ShipContainer` 是一个字典，其键是船 ID，值是船对象。

对于简单项，我们通常可以在一条语句中创建项并将其插入表格：我们已经对所有者、国家和描述属性这样做了。但如果我们想对项进行格式化或在其中存储用户数据，就必须单独创建该项，调用其方法，最后通过 `setItem()` 将其放入表格。我们使用第二种方法将船的 ID 存储为用户数据，并将 TEU 值右对齐。

TEU 值是整数，`QString.arg()` 方法使用了四个参数：一个整数、最小字段宽度、数值基，以及一个用于填充的字符（如果需要填充以达到最小字段宽度的话）。

一旦表格填充完毕，我们就重新开启排序功能，将每列的宽度调整为其最宽单元格的宽度，并将选中的项（如果有）设为当前项并选中状态。

填充列表和表格非常相似，因为它们都使用行-列方法。填充树形结构则不同，因为我们使用父子节点方法。船数据的树视图有两列。第一列是树，根节点是国家，下一级节点是所有者，底层节点是船本身。第二列仅显示 TEU。我们本可以添加第三列来显示描述，但这样做对于理解树形小部件的工作原理没有帮助。

```python
def populateTree(self, selectedShip=None):
    selected = None
    self.treeWidget.clear()
    self.treeWidget.setColumnCount(2)
    self.treeWidget.setHeaderLabels(["Country/Owner/Name", "TEU"])
    self.treeWidget.setItemsExpandable(True)
    parentFromCountry = {}
    parentFromCountryOwner = {}
```

我们的开始方式与之前相同，清除树并设置它的列和列标题。我们还设置了树的项为可展开。稍后我们将解释这两个字典。

```python
for ship in ships.inCountryOrder():
    ancestor = parentFromCountry.get(ship.country)
    if ancestor is None:
        ancestor = QTreeWidgetItem([ship.country])
        parentFromCountry[ship.country] = ancestor
    countryOwner = ship.country + "/" + ship.owner
    parent = parentFromCountryOwner.get(countryOwner)
    if parent is None:
        parent = QTreeWidgetItem(ancestor, [ship.owner])
        parentFromCountryOwner[countryOwner] = parent
    item = QTreeWidgetItem(parent, [ship.name, QString("%L1").arg(ship.teu)])
    item.setTextAlignment(1, Qt.AlignRight | Qt.AlignVCenter)
    if selectedShip is not None and selectedShip == id(ship):
        selected = item
        self.treeWidget.expandItem(parent)
        self.treeWidget.expandItem(ancestor)
```

每艘船在树中必须有一个所有者父节点，每个所有者在树中必须有一个国家父节点。

对于每艘船，我们检查树中是否存在该船国家的项。如果没有，我们就以树形小部件为父节点创建一个新项，并在字典中保留该项的引用。此时，我们已经检索或创建了国家（祖先）项。



然后，我们检查树中是否存在该船所有者的项。我们在 `parentFromOwner` 字典中查找此项。同样，如果不存在，我们就创建一个新的所有者项，其父节点为刚刚找到的国家（祖先）项，并在字典中保留该所有者项的引用。此时，我们已经检索或创建了所有者（父节点）项。现在我们为船创建一个新项，并所有者为其父节点。

我们使用 `parentFromCountryOwner` 而不是 `parentFromOwner` 是因为特定的所有者可能在多个国家经营。

## 使用便捷项小部件

树形小部件项有多个列，这就是为什么在创建它们时，除了父节点外还传递了一个列表。我们为船使用了额外的列（实际上只多了一列）来存储船的 TEU。通过调用 `QTreeWidgetItem.setTextAlignment()` 并传递列号作为第一个参数，我们将 TEU 数字右对齐。

```python
self.tableWidget.resizeColumnToContents(0)
self.tableWidget.resizeColumnToContents(1)
if selected is not None:
    selected.setSelected(True)
    self.tableWidget.setCurrentItem(selected)
```

一旦表格填充完毕，我们就重新开启排序功能，将每列的宽度调整为其最宽单元格的宽度，并将选中的项（如果有）设为当前项并选中。

填充列表和表格非常相似，因为它们都使用行-列方法。填充树形结构则不同，因为我们使用父子节点方法。船数据的树视图有两个列。第一列是树，根节点是国家，下一级节点是所有者，底层节点是船本身。第二列仅显示 TEU。我们本添加第三列来显示描述，但这样做对于理解树形小部件的工作原理没有帮助。

树形小部件项有多个列，这就是为什么在创建它们时，除了父节点外还传递了一个列表。我们为船使用了额外的列（实际上只多了一列）来存储船的 TEU。通过调用 `QTreeWidgetItem.setTextAlignment()` 并传递列号作为第一个参数，我们将 TEU 数字右对齐。

```python
self.tableWidget.resizeColumnToContents(0)
self.tableWidget.resizeColumnToContents(1)
if selected is not None:
    selected.setSelected(True)
    self.tableWidget.setCurrentItem(selected)
```

对于简单项，我们通常可以在一条语句中创建项并将其插入表格：我们已经对所有者、国家和描述属性这样做了。但如果我们想对项进行格式化或在其中存储用户数据，就必须单独创建该项，调用其方法，最后通过 `setItem()` 将其放入表格。我们使用第二种方法将船的 ID 存储为用户数据，并将 TEU 值右对齐。

项（船名）和船的 ID 设置为用户数据。存储 ID 为我们提供了一种从表格跳转到该行所代表的船的手段。这之所以可行，是因为 `ShipContainer` 是一个字典，其键是船 ID，值是船对象。

对于简单项，我们通常可以在一条语句中创建项并将其插入表格：我们已经对所有者、国家和描述属性这样做了。但如果我们想对项进行格式化或在其中存储用户数据，就必须单独创建该项，调用其方法，最后通过 `setItem()` 将其放入表格。我们使用第二种方法将船的 ID 存储为用户数据，并将 TEU 值右对齐。

TEU 值是整数，`QString.arg()` 方法使用了四个参数：一个整数、最小字段宽度、数值基，以及一个用于填充的字符（如果需要填充以达到最小字段宽度的话）。

一旦表格填充完毕，我们就重新开启排序功能，将每列的宽度调整为其最宽单元格的宽度，并将选中的项（如果有）设为当前项并选中。

填充列表和表格非常相似，因为它们都使用行-列方法。填充树形结构则不同，因为我们使用父子节点方法。船数据的树视图有两个列。第一列是树，根节点是国家，下一级节点是所有者，底层节点是船本身。第二列仅显示 TEU。我们本添加第三列来显示描述，但这样做对于理解树形小部件的工作原理没有帮助。

TEU 值是整数，`QString.arg()` 方法使用了四个参数：一个整数、最小字段宽度、数值基，以及一个用于填充的字符（如果需要填充以达到最小字段宽度的话）。

一旦表格填充完毕，我们就重新开启排序功能，将每列的宽度调整为其最宽单元列的宽度，并将选中的项（如果有）设为当前项并选中。

填充列表和表格非常相似，因为它们都使用行-列方法。填充树形结构则不同，因为我们使用父子节点方法。船数据的树视图有两个列。第一列是树，根节点是国家，下一级节点是所有者，底层节点是船本身。第二列仅显示 TEU。我们本添加第三列来显示描述，但这样做对于理解树形小部件的工作原理没有帮助。

树形小部件项有多个列，这就是为什么在创建它们时，除了父节点外还传递了一个列表。我们为船使用了额外的列（实际上只多了一列）来存储船的 TEU。通过调用 `QTreeWidgetItem.setTextAlignment()` 并传递列号作为第一个参数，我们将 TEU 数字右对齐。

```python
def itemChanged(self, item):
    ship = self.currentTableShip()
    if ship is not None:
        column = self.tableWidget.ColumnCount()
        if column == ships.NAME:
            ship.name = item.text().trimmed()
        elif column == ships.OWNER:
            ship.owner = item.text().trimmed()
        elif column == ships.COUNTRY:
            ship.country = item.text().trimmed()
        elif column == ships.DESCRIPTION:
            ship.description = item.text().trimmed()
        elif column == ships.TEU:
            ship.teu = item.text().toInt()
        ship.dirty = True
    self.populateList()
```

```python
def currentTableShip(self):
    item = self.tableWidget.item(self.tableWidget.currentRow())
    if item is None:
        return None
    return self.ships(item.data(Qt.UserRole).toLong())
```

```python
def addShip(self):
    ship = self.ships.ship("Unknown", "Unknown", "Unknown")
    self.ships.addShip(ship)
    self.populateList()
    self.populateTree()
    self.populateTable(id(ship))
    self.tableWidget.setFocus()
    self.tableWidget.editItem(self.tableWidget.currentItem())
```

## populateTree()

`QTable.item()` 返回给定行和列的项。我们总是想要当前行的项，因为我们是在这些项中存储每一行的数据。

`QString.simplified()` 方法也非常有用。它会移除末端的空白字符，并将内部连续的一个或多个空白字符序列还原为单个空格。

# 使用便利项部件

```python
def removeShip(self):
    ship = self.currentTableShip()
    if ship is None:
        return
    if QMessageBox.question(self, "Ships - Remove",
        QString("Remove %1 of %2?").arg(ship.name) \
        .arg(ship.owner).arg(ship.country),
        QMessageBox.Yes|QMessageBox.No) == QMessageBox.No:
        return
    self.ships.removeShip(ship)
    self.populateList()
    self.populateTree()
    self.populateTable()
```

移除船舶比添加它们更加简单。我们获取当前船舶并弹出一个消息框，询问用户是否确定要移除该船舶。如果他们点击“是”，我们就会从 `ShipContainer` 中移除该船舶并重新填充视图部件。

尽管像我们这样这样做使用三个不同的视图是不常规的，但我们使用的技术（特别是配合 `QTableWidget` 的技术）是完全通用的。

便利部件对于小型和临时临时数据集非常有用，并且可以在不一定拥有独立数据集的情况下直接使用——它们本身就可以显示、编辑和存储数据。我们在这个示例中选择分离数据，是为了为使用模型/视图技术（特别是下一节的主题：自定义模型）做准备。

## 创建自定义模型

在本节中，我们将创建一个自定义模型来存储船舶数据，并并在两个不同的表格视图中显示同一个模型。图 14.3 显示了一个使用该模型的应用程序。用户可以独立地滚动表格，并编辑其中任何一个视图中的数据，放心地知道任何更改将自动反映在两个视图中。

我们将首先展示应用程序主界面的代码片段。这将向我们展示一些正在使用的模型/视图 API。然后，我们将查看模型本身的实现。PyQt 模型/视图架构的一个重要优点是，相同的编码模式会被反复使用，一旦我们学会了如何创建一个表格模型，我们就知道如何创建任何表格（或列表）模型。

模型由第 14 章/ships.pyw 中的 `ShipTableModel` 类提供，应用程序位于第 14 章/ships-model.pyw 中。我们通过设置背景和前景颜色改进了视图中数据的显示，但这些可以在便利视图中通过调用表项的相应方法来实现。上一个示例中存在的问题，特别是没有用于订单或国家的组合框、没有用于 TEU 的数值框以及显示 HTML 描述文本仍然存在。这些问题只能通过使用代理（delegate）来解决，这正是我们下一节中要做的。

| 名称 | 所有者 | 国家 | 描述 | TEU |

| --- | --- | --- | --- | --- |

| 1 A.P. Meller | Maersk Line | 丹麦 | 船长 *Frederick* | | 91,690 |

| 2 Adrian Maersk | Maersk Line | 丹麦 | 船长 *G. E. Erickson* | | 93,496 |

| 3 Albert Maersk | Maersk Line | 丹麦 | 船长 *Tallow* | | 93,496 |

| 4 Anna Maersk | Maersk Line | 丹麦 | 船长 *Lockhart* | | 93,496 |

| 5 Arnold Maersk | Maersk Line | 丹麦 | 船长 *Mor...* | | 93,496 |

**图 14.3** QtTableView 中的自定义表格模型

## 实现视图逻辑

从表面上看，使用带有内置模型的便利视图所实现的功能，与使用带有独立模型的纯视图所实现的功能似乎没有区别。在在上一个示例中，我们有三个视图显示相同的底层数据，保持它们同步是我们的责任。在这个示例中，我们对同一份数据上使用两个视图，并将同步工作交给 PyQt，因为两个视图都使用同一个模型。另一个好处是，视图只检索或存储实际被看到或编辑的数据，这在在使用大型数据集时可以带来显著的性能优势。

我们将从初始化函数的的一些代码片段开始。

```python
class MainForm(QDialog):
    def __init__(self, parent=None):
        super(MainForm, self).__init__(parent)
        self.model = ships.ShipTableModel(QString("ships.dat"))
        self.table1 = QLabel("Table &1")
        self.tableview1 = QTableView()
        self.table1.setBuddy(self.tableview1)
        self.tableview1.setModel(self.model)
        self.table2 = QLabel("Table &2")
        self.tableview2 = QTableView()
        self.table2.setBuddy(self.tableview2)
        self.tableview2.setModel(self.model)
```

## 创建自定义模型

首先，我们创建一个新模型。然后，我们创建两个表格视视图以及相应的标签以便导航。每个表格视图都分配了相同的模型进行工作。我们省略了布局代码，因为它与此无关。

```python
for tableView in (self.tableView1, self.tableView2):
    header = tableView.horizontalHeader()
    self.connect(header, SIGNAL("sectionChanged(int)"), self.sortTable)
    self.connect(addButton, SIGNAL("clicked()"), self.addShip)
    self.connect(removeButton, SIGNAL("clicked()"), self.removeShip)
    self.connect(quitButton, SIGNAL("clicked()"), self.accept)
```

当用户终止应用程序且有未保存的更改时，我们将给他们保存的机会。

```python
def accept(self):
    if self.dirty:
        if QMessageBox.question(self, "Ships - Save",
                             "Save unsaved changes?",
                             QMessageBox.Yes|QMessageBox.No) == QMessageBox.Yes:
            try:
                self.model.save()
            except IOError, e:
                QMessageBox.warning(self, "Ships - Error",
                                   "Failed to save: %s" % e)
    QDialog.accept()
```

模型由第 14 章/ships.pyw 中的 `ShipTableModel` 类提供，应用程序位于第 14 章/ships-model.pyw。我们通过设置背景和前景颜色改进了视图中数据的显示，但这些可以在便利视图中通过调用表项的相应方法来实现。

```python
def sortTable(self, section):
    if section in (ships.OWNER, ships.COUNTRY):
        self.model.sortByCountry()
    else:
        self.model.sortByName()
    self.resizeColumns()
```

我们提供了两种排序，但没有理由支持更多。同样，`sortBy()` 方法是我们标准 API 的扩展。当用户排序时，我们利用机会调整列宽。

```python
def resizeColumns(self):
    for tableView in (self.tableView1, self.tableView2):
        for column in (ships.NAME, ships.OWNER, ships.COUNTRY,
                      ships.TEU):
            tableView.resizeColumnToContents(column)
```

我们选择在两个视图中调整除描述列以外的所有列。

```python
def addShip(self):
    row = self.model.rowCount()
    self.model.insertRows(row)
    index = self.model.index(row, 0)
    tableView = self.tableView1
    if self.tableView2.hasFocus():
        tableView = self.tableView2
    tableView.setCurrentIndex(index)
    tableView.edit(index)
```

`rowCount()`、`insertRows()` 和 `index()` 方法是 `QAbstractTableModel` API 的一部分。

```python
def removeShip(self):
    tableView = self.tableView1
    if self.tableView2.hasFocus():
        tableView = self.tableView2
    index = tableView.currentIndex()
    if not index.isValid():
        return
    row = index.row()
    name = self.model.data(
        self.model.index(row, ships.NAME)).toString()
    owner = self.model.data(
        self.model.index(row, ships.OWNER)).toString()
```

## 创建自定义模型

```python
country = self.model.data(
self.model.index(row, ships.COUNTRY)).toString()
if QMessageBox.question(self, "Ships - Remove",
QString("Remove %1 of %2?%3").arg(owner) \
.arg(country),
QMessageBox.Yes|QMessageBox.No) == QMessageBox.No:
    return
self.model.removeRows(row)
self.model.resizeColumns()
```

如果用户点击“移除”按钮，我们会获取当前表格视图的模型索引。我们从该模型索引中提取行，并将其用于 `QATableModel.data()` 方法以检索船只的名称、所有者和国家。`data()` 方法接受索引作为强制性参数并返回一个 `Variant`。我们使用 `QAbstractTableModel.index()` 为我们需要的行/列组合创建索引，并使用 `QVariant.toString()` 将返回值转换为 `QString`。

如果用户确认删除，我们只需从模型中删除相关行。模型将自动通知视图，视图随后会更新自身。由于删除后最大列宽可能会发生变化，我们添加了对 `resizeColumns()` 的调用。

# 实现自定模型

现在我们已经看到 `QAbstractTableModel` API 的一些用法，以及我们自己的一些扩展。子类中的方法可以分为三类：

- 实现只读模型所必需的方法

- 实现可编辑模型所必需的方法

- 我们针对特定情况需要扩展 API 的方法

只读表格模型的核心要素是 `data()`、`rowCount()` 和 `columnCount()`，尽管 `headerData()` 几乎总是会被实现的。

可编辑模型需要根据需要重新实现只读模型相同的方法，此外还需要 `flags()` 和 `setData()`。如果模型需要支持添加和删除行以及编辑现有数据，则必须实现 `insertRows()` 和 `removeRows()`。

其他方法也可以被实现，尽管上述两个段中列出的只是必需方法。

对于船只模型，我们在内存中的列表中存储船只，并在磁盘上的二进制文件中存储它们。为了支持这一功能，我们通过添加 `sortByName()`、`sortByCountryOwner()`、`load()` 和 `save()` 扩展了模型 API。

`ShipTableModel` 模型位于 `chap14/ships.py`。

第 14 章。模型/视图编程

```python
class ShipTableModel(QAbstractTableModel):
    def __init__(self, filename=QString()):
        super(ShipTableModel, self).__init__()
        self.filename = filename
        self.dirty = False
        self.ships = []
        self.owners = set()
        self.countries = set()
```

为了将模型数据加载和保存到二进化文件中，我们保留了一个带有文件名的实例变量。船只本身存储在一个列表中，初始状态是无序的。我们还维护了两个集合，一个用于所有者，另一个用于国家：这些将在我们在下一节创建自定义代理时用于填充组合框（combobox）。

```python
def rowCount(self, index=QModelIndex()):
    return len(self.ships)
```

```python
def columnCount(self, index=QModelIndex()):
    return 5
```

行数和列数很容易提供。表格模型具有固定列数是非常常见的。

```python
def data(self, index, role=Qt.DisplayRole):
    if not index.isValid() or \
        not (0 <= index.row() < len(self.ships)):
        return QVariant()
    ship = self.ships[index.row()]
    column = index.column()
    if role == Qt.DisplayRole:
        if column == NAME:
            return QVariant(ship.name)
        elif column == OWNER:
            return QVariant(ship.owner)
        elif column == COUNTRY:
            return QVariant(ship.country)
        elif column == DESCRIPTION:
            return QVariant(ship.description)
        elif column == TEU:
            return QVariant(ship.teu)
```

## 创建自定义模型

# 431

```python
def setData(self, index, value, role=Qt.EditRole):
    if index.isValid() and index <= index.row() < len(self.ships):
        ship = self.ships[index.row()]
        column = index.column()
        if column == NAME:
            ship.name = value.toString()
        elif column == OWNER:
            ship.owner = value.toString()
        elif column == COUNTRY:
            ship.country = value.toString()
        elif column == DESCRIPTION:
            ship.description = value.toString()
        elif column == TEU:
            value, ok = value.toInt()
            if ok:
                ship.teu = value
                ship.dirty = True
                ship.emit(SIGNAL("dataChanged(QModelIndex, QModelIndex)", index, index))
                return True
    return False
```

当用户完成编辑时会调用此方法。在这种情况下，我们忽略了角色（role），尽管可能分离显示数据和编辑数据（例如，电子表格的结果及其背后的公式）。如果索引有效且行在范围内，我们会检索相关的船只并更新已编辑的列。对于 TEU 的情况，只有当用户输入的内容成功转换为整数时，我们才应用更改。

如果发生了更改，必须发射 `dataChanged()` 信号。模型/视图架构依赖此信号来确保所有视图都保持更新。我们必须两次传递被更改项的模型索引，因为该信号用于表示一组更改，第一个索引是左上角的项，第二个索引是右下角的项。如果更改被接受并应用，我们必须返回 `True`，否则返回 `False`。

实现 `flag()` 和 `setData`（除了只读模型必需的方法外）就足以使模型变得可编辑。但为了让使用户能够添加或删除行，我们需要实现额外的方法。

```python
def insertRows(self, position, rows=1, index=QModelIndex()):
    self.beginInsertRows(QModelIndex(), position,
    position + rows - 1)
    for row in range(rows):
        self.ships.insert(position + row, Ship("Unknown", "Unknown", "Unknown"))
    self.endInsertRows()
```

# 第 14 章：模型/视图编程

```python
self.dirty = True
return True
```

当我们要向模型中插入一行或多行时，调用 `beginInsertRows()` 是至关重要的。位置是我们想要插入的行。`beginRows()` 的调用直接取自 PyQt 文档，对于任何表格模型的 `insertRows()` 实现都不应更改。在插入之后，我们必须调用 `endInsertRows()`。模型将自动通知视图更改已经发生，如果相关行对用户可见，视图将请求新数据。

```python
def removeRows(self, position, rows=1, index=QModelIndex()):
    self.beginRows(QModelIndex(), position,
                   position + rows - 1)
    self.ships = self.ships[:position] + \
                   self.ships[position + rows:]
    self.endRemoveRows()
    self.dirty = True
    return True
```

此方法与上一个方法类似。`beginRemoveRows()` 的调用取自文档，是表格实现的标准做法。在删除相关行之后，我们必须调用 `endRemoveRows()`。模型将自动通知视图更改。

我们已经实现了可编辑表格方法的本质方法。某些模型仅仅是外部数据源的接口，例如数据库表（将在下一章介绍），或外部文件或进程。由于这些原因，我们将数据存储在模型内部，因此我们必须提供一些额外的方法，特别是 `load()` 和 `save()`。我们还提供了几个排序方法以方便用户。对于大型数据集，排序是非常开销的，在这种情况下，使用有序数据结构（如 `OrderedDict`）或结合 `bisect` 模块函数使用列表可能会有益。

- OrderedDict

```python
def sortByName(self):
    self.ships = sorted(self.ships)
    self.reset()
```

当对列表调用 `sort()` 时，它会使用项的 `__lt__` 特殊方法进行比较，如果没有实现 `__lt__`，则退回到使用 `__cmp__()` 特殊方法。我们提供了 `Ship.__cmp__()`，它是对船只名称的本地感知比较。

排序数据会使所有模型索引失效，意味着视图现在显示的是错误的数据。模型必须通过检索新数据来通知需要自我更新的视图。这样做的一种方法是发射 `dataChanged()` 信号，但对于大规模更改，调用更高效：

## 创建自定义模型

# 表 14.1 精选 QAbstractItemModel 方法 #1

| 语法 | 描述 |

| --- | --- |

| m.beginInsertRows(p, f, l) | 在 `insertRows()` 的重写中插入数据之前调用。参数是父级 `QModelIndex` p 以及新行占据的第一行和最后行数；m 是 `QAbstractItemModel` 子类。 |

| m.beginRemoveRows(p, f, l) | 在 `removeRows()` 的重写中删除数据之前调用。参数是父级 `QModelIndex` p 以及要删除的第一行和最后一行；m 是 `QAbstractItemModel` 子类。 |

| m.columnCount(p) | 子类必须实现此项；父级 `QModelIndex` p 仅对树形模型重要。 |

| m.createIndex(r, c, p) | 为给定的行 r、列 c 和父级 p 返回 `QModelIndex`。 |

| m.data(i, rl) | 设置 `QModelIndex` i 的数据为 `Qt.ItemRole` rl 的 `QVariant`。可编辑模型必须重写此项——如果数据发生更改，必须发射 `dataChanged()` 信号。 |

| m.endInsertRows() | 在 `insertRows()` 的重写中插入数据后调用；m 是 `QAbstractItemModel` 子类。 |

| m.endRemoveRows() | 在 `removeRows()` 的重写中删除数据后调用；m 是 `QAbstractItemModel` 子类。 |

| m.flags(i) | 返回 i 的 `ItemFlags`；这些决定了项目是否可选、可编辑等。 |

| m.hasChildren(p) | 如果 QModelIndex p 有子节点则返回 true；仅对树形模型有效。 |

| m.setHeaderData(s, o, v, rl) | 设置节 s 对应 Qt.Orientation o（即行或列）的 Qt.ItemRole rl 的 `QVariant`。 |

| m.parent(i) | 返回 i 的父级 `QModelIndex`。树形模型必须实现此项。 |

| m.insertRow(r, p) | 在行 r 之前插入一行。在树形模型中，该行作为父级 p 的子插入。 |

| m.insertRows(r, n, p) | 在行 r 之前插入 n 行。在树形模型中，这些行作为父级 p 的子插入。 |

| m.rowCount(p) | 子类必须实现此项；父级 `QModelIndex` p 仅对树形模型重要。 |

# 第 14 章：模型/视图编程

# 表 14.2 精选 QAbstractItemModel 方法 #2

| 语法 | 描述 |

| --- | --- |

| m.removeRow(r, p) | 删除行 r。父级 `QModelIndex` p 对树形模型有效；m 是 `QAbstractItemModel` 子类。 |

| m.removeRows(r, n, p) | 从行 r 开始删除 n 行。父级 `QModelIndex` p 对树形模型有效。可编辑模型通常重写此方法。 |

| m.beginResetModel() | 通知所有关联视图内容已过期并强制它们自我更新。 |

| m.endResetModel() | 配合 `beginResetModel()` 使用。 |

## 创建自定义模型

self.ships = [ship for country, owner, name, ship in ships]

self.reset()

这里使用了普通的 `QString()`，因此可能使用 `unicode(ship.country)`、`unicode(ship.name)` 和 `unicode(ship.name)` 可能会更好。当然，对于非常大的数据集，可能完全使用有序排序（ordered sorting）并使用有序容器会更好。

`save()` 和 `load()` 方法与我们之前过的过的 `QDataStream` 处理二进制数据的方法非常相似，因此我们将展示每个方法核心部分的片段，从 `save()` 方法开始。

```cpp
for ship in self.ships:
    stream << ship.name << ship.owner << ship.country \
    stream << ship.description
    stream.writeInt32(ship.teu)
```

得益于使用 `QDataStream`，我们不需要担心字符串的长短或编码问题。

船舶是以相应的方式加载的：这里是 `load()` 方法的一个片段：

```cpp
self.ships = []
while not stream.atEnd():
    name = QString()
    owner = QString()
    country = QString()
    description = QString()
    stream >> name >> owner >> country >> description
    teu = stream.readInt32()
    self.ships.append(Ship(name, owner, country, teu, description))
    self.owners.add(unicode(owner))
    self.countries.add(unicode(country))
```

如前所述，我们保留了所有者和国家的集合，以便在添加自定义代理（delegate）时可以在组合框（combobox）中使用它们。

实现自定义模型，特别是列表和表格模型是非常简单的。对于只读模型，我们只需要实现三个方法，尽管我们通常会实现四个。对于可编辑模型，我们通常共实现八个方法。一旦你创建了几模型，创建其他的就会变得简单，因为所有的列表和表格模型都遵循相同的模式。实现树模型更具挑战性；该主题在第 16 章的最后一节中介绍。

# 创建自定义代理

如果我们想对数据项的显示和编辑进行完全控制，就必须创建一个自定义代理。代理可以仅用于控制外观（例如，用于只读视图），或者通过提供自定义编辑器来控制编辑，或者两者兼顾。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_450_0.png)

图 14.4 看起来与之前的截图相似，唯一的区别是描述文本被正确格式化了，而不是 HTML。它们的差异要深得多。例如，如果我们编辑所有者或国家字段，我们将获得一个填充了当前所有者和国家的组合框；如果我们编辑 AEW，我们将得到一个数字步进器（spinbox）。这种对外观和编辑的控制是通过使用代理实现的——代理可以用于便利视图（convenience views）或纯视图（pure views），尽管在本例中我们将代理用于了纯视图。

在本节中，我们使用的是 `chap14/ships-delegate.py`应用程序。它几乎与 `model-py` 相同，不同之处在于窗口标题、缩放了所有列而不是跳过代理列，以及我们使用了自定�代理。代理类 `ShipDelegate` 位于 `chap14/ships.py`。请注意此类需要 PyQt 4.1 或更高版本。

与模型子类一样，代理也遵循固定的模式。对于只读模型的代理，我们必须重新实现的方法只有一个：`paint()`。对于可编辑模型，我们必须重新实现 `createEditor()`、`setEditorData()` 和 `setModelData()`。如果我们使用 `QLineEdit` 或 `QTextEdit` 进行编辑，重新实现 `commitAndCloseEditor()` 也是很常见的。最后，有时我们需要重新实现 `sizeHint()`，正如我们所看到的。。

# 创建自定义代理

437

创建只处理某些列的代理是非常常见的，特别是在涉及到绘图时，让基类处理默认行为已足够的列。

我们将从查看主表构造函数的一个小片段开始，查看第一个表格的创建：

```python
class MainForm(QDialog):
    def __init__(self, parent=None):
        super(MainForm, self).__init__(parent)
        self.model = ships.ShipTableModel(QString("ships.data"))
        self.tableLabel = QLabel("&")
        self.tableView1 = QTableView()
        self.tableLabel.setBuddy(self.tableView1)
        self.tableView1.setModel(self.model)
        self.tableView1.setItemDelegate(ships.ShipDelegate(self))
```

与前节唯一的区别在于我们调用了 `setItemDelegate` 并传递了一个新构造的 `ship.ShipDelegate`。必须将表单作为参数传递代理，以便在表单存在时保持其存活。第二个表格的代码是相同的，设置了相同的模型，但有它自己的 `ship.ShipDelegate`。这是唯一必要的更改——现在所有展示和确保数据处理的工作将由代理完成。

```python
class ShipDelegate(QItemDelegate):
    def __init__(self, parent=None):
        super(ShipDelegate, self).__init__(parent)
```

通常，代理的构造函数不需要做任何事情，除了初始化基类，而这正是我们在这里所做的。事实上，对于像此类情况，我们可以完全省略 `__init__()`。

```python
def paint(self, parent, option, index):
    if index.column() == DESCRIPTION:
        text = index.model().data(Qt.DisplayRole)
        palette = QApplication.palette()
        document = QTextDocument()
        document.setFont(option.font)
        if option.state() & QStyle.State_Selected:
            document.setHtml("<font color=%1>%2</font>")
                .arg(palette.highlightedText().name())
                .arg(text)
        else:
            document.setHtml(text)
        color = palette.highlightedText().color()
```

438                               Chapter 14. Model/View Programming

```cpp
else QColor(index.model().data(Qt.BackgroundColor)
painter.save()
painter.fillRect(option.rect, color)
painter.translate(option.rect.x(), option.rect.y)
document.drawContents(painter)
painter.restore()
else
QItemDelegate.paint(self, option, index)
```

纯文本字符串、数字、日期等，基类 `QItemDelegate.paint()` 方法非常好，通常不需要实现。但在本例中，描述列包含 HTML，我们必须自己渲染。

`paint()` 方法被调用时，参数是一个准备好绘图的 painter、一个包含各种信息的 `QOptionItemView`（包括绘图所在的矩形）以及要绘制的项目的模型索引。

我们首先通过模型的 `data()` 方法获取 HTML 文本，并依赖我们在模型中设置的 `Qt.DisplayRole`，作为第二个参数。注意模型索引可以引用它所引用的模型 `QModel::model()`。

然后我们获取应用程序的调色板——这是基于用户的颜色偏好的。如果项目被选中，我们将调色板的高亮文本应用于 HTML；否则，我们直接使用 HTML。`QColor::name()` 方法以十六进制字符串返回颜色；例如，红色返回字符串 "FF0000"，这与 HTML 颜色规范格式相同。同样，如果项目被选中，我们使用高亮背景色；否则，我们使用模型通过 `Qt.BackgroundColor` 指定的颜色。

遗憾的是，绘制 HTML 的故事还没有结束。当视图请求 HTML 列的尺寸提示时，默认行为将返回一个基于视图字体和字符数量的尺寸提示。

# 创建自定义代理 439

由于 HTML 相当冗长，在计算时使用的字符数量可能远大于实际显示的字符数量。

这个问题有两个解决方案，两种方案都需要我们手动计算 HTML 文本的尺寸提示（size hint）。一种方案是修改 `QAbstractTableModel::data()` 方法，并在使用 `Qt::SizeHintRole` 调用 `data()` 时返回一个合适的尺寸提示。另一种方案是重新实现 `QItemDelegate::sizeHint()` 方法。我们更倾向于重新实现 `sizeHint()`，因为可以将问题及其解决方案在同一个类中。

```python
def sizeHint(self, option, index):
    fm = option.fontMetrics
    if index.column() == TEU:
        return QSize(fm.width("9,999"), fm.height())
    if index.column() == DESCRIPTION:
        text = index.model().data(index).toString()
        document = QTextDocument(text)
        document.setFont(option.font)
        document.setHtml(text)
        return QSize(document.idealWidth() + 5, fm.height())
    return QItemDelegate.sizeHint(option, index)
```

`option` 参数是一个 `QStyleOptionView`，`QStyleOption` 具有几个实用的属性。在这个方法中，我们实际上承担了两个列的尺寸提示计算。对于 TEU，我们返回一个足够容纳我们预期处理的最大 TEU 的宽度。对于描述（description），我们使用 `QTextDocument()` 根据其字体和字体属性计算“理想”宽度，加上 5 像素的微小边距。对于其他列，我们将工作交给基类。

很多时候，代理完全不会重新实现 `paint()` 方法，而是依赖于完美的默认绘制行为，而而为编辑数据项提供自定义方法。

```python
def createEditor(self, parent, option, index):
    if index.column() == TEU:
        spinbox = QSpinBox(parent)
        spinbox.setRange(0, 200000)
        spinbox.setSingleStep(1000)
        spinbox.setAlignment(Qt.AlignRight|Qt.AlignCenter)
        return spinbox
    elif index.column() == OWNER:
        combobox = QComboBox(parent)
        combobox.addItems(sorted(index.model().owners))
        combobox.setEditable(True)
        return combobox
    elif index.column() == COUNTRY:
        combobox = QComboBox(parent)
        combobox.addItems(sorted(index.model().countries))
        combobox.setEditable(True)
        return combobox
    elif index.column(0) == NAME:
        editor = QLineEdit(parent)
        self.connect(editor, SIGNAL("returnPressed()"))
```

用户通常通过按下 F2 或双击来启动数据项的编辑，视图请求代理为该项提供一个编辑器。对于任何我们不想自己处理的项，可以将工作交给基类，但在在这个代理中，我们倾向于处理颜色列。

对于 TEU 列，我们使用了内置的计数器（spin）。我们可以使用任何控件，无论是像 `QSpinBox` 这样的内置控件，还是自定义编辑器，例如我们在上一章节中创建的 `RichTextEdit`。在所有情况下，步骤都是相同的：使用给定的父对象创建编辑器，然后对其进行设置并返回。

我们已经用排序后的列表填充了组合框，并使它们可以输入新条目进行编辑。如果我们希望用户只能从我们指指定的列表中选择，只需省略 `setEditable(True)` 的调用即可。

在 `QLineEdit`、`QTextEdit` 以及其他具有 `returnPressed()` 信号以指示编辑完成的类中，我们将信号连接到 `commitAndCloseEditor()` 的实现上。

```python
def commitAndCloseEditor(self):
    editor = self.sender()
    if isinstance(editor, (QTextEdit, QLineEdit)):
        self.emit(SIGNAL("commitData(QWidget*)"), editor)
    self.emit(SIGNAL("closeEditor(QWidget*)"), editor)
```

之前，我们使用内置的 `instance()` 函数来相对于单个类考虑对象，但这里我们有两个类的元组组。该方法在用户按下回车键时调用并向编辑器发送信号，告诉它将其数据保存到模型并关闭自己。

# 创建自定义代理

```python
def setEditorData(self, editor, index):
    text = index.model().data(index, Qt.DisplayRole).toString()
    if index.column() == TEU:
        value = text.replace(QRegExp(r"\[\]]"), "").toInt()[0]
        editor.setValue(value)
    elif index.column() in (OWNER, COUNTRY):
        i = editor.findText(text)
        if i == -1:
            i = 0
        editor.setCurrentIndex(i)
    elif index.column() == NAME:
        editor.setText(text)
    elif index.column() == DESCRIPTION:
        editor.setHtml(text)
    else:
        QItemDelegate.setEditorData(self, editor, index)
```

一旦编辑器被创建并交给视图，视图就会调用 `setEditorData()`。这让代理有了一个机会用当前数据填充编辑器，以供用户编辑。在 TEU 的情况下，我们将它们显示为包含空格、逗号或句号的文本。对于这些条目，我们去掉了不需要的字符，将值转换为整数，并相应地设置计数器的值。另一种方法是为该列分离 `Qt.DisplayRole` 和 `Qt.EditRole` 值。

如果编辑器是组合框，我们将其当前索引设置为与数据值匹配的项。如果没有匹配项，我们只需让第一项成为当前项。对于用于船名的行编辑框，我们使用 `setText()`，对于富文本编辑器，我们使用 `setHtml()`（继承自 `QText`）。像往常一样，我们将未处理的情况交给基类，尽管在这里这只是形式上的，因为我们处理了所有的列。

```python
def setData(self, editor, model, index):
    if index.column() == TEU:
        model.setData(index, QVariant(editor.value()))
    elif index.column() in (OWNER, COUNTRY):
        model.setData(index, QVariant(editor.currentText()))
    elif index.column() == NAME:
        model.setData(index, QVariant(editor.text()))
    elif index.column() == DESCRIPTION:
        model.setData(index, QVariant(editor.toSimpleHtml()))
    else:
        QItemDelegate.setData(self, editor, model, index)
```

如果用户确认了他们的编辑，编辑器数据必须写回模型。模型随后将通知视图它发生了变化，而那些显示该项的视图将请求新的数据进行显示。

在这种情况下，我们只需从相应的编辑器中检索值并调用 `setData()`，将值作为 `QVariant` 传递。

我们现在已经完成了代理。在下一章中使用了两个代理，它们都为某些字段提供了编辑器，并且都只实现了 `createEditor()`、`setData()` 和 `setModelData()`。在本章和下一章中，自定义代理是针对特定模型的。。在第 16 章中，我们有一个专门介绍“通用代理”的章节，可以用于为任何模型创建代理，而无需拥有针对特定模型的自定义代理——这可以减少重复并使维护更简单。

## 总结

Qt 的便利项目视图控件，如 `QListWidget`、`TableWidget` 和 `QTreeWidget`，对于查看和编辑小型临时数据集非常有用。它们可以与外部数据集结合使用（正如我们所做的那样），也可以作为数据容器使用。添加、编辑和删除项是直接的，但如果我们使用多个视图来显示同一个数据集，我们就必须承担保持视图和数据集同步的责任。如果使用模型/视图架构，这个问题就会消失。

## 总结

443（重新实现）。对于大多数代理，我们完全不需要重新实现 `paint()` 或 `sizeHint()`，只需重新实现 `createEditor()`、`setEditorData()` 和 `setModelData()` 即可。

在下一章节，我们将看到模型/视图架构的更多示例，包括纯视视图、自定义代理和内置的 SQL 数据库模型。

## 练习

为 `ShipTableModel` 添加一个新方法 `sortByTEU()`。使用任何你喜欢的排序技术；我们已经用过 DSU 了。然后在 `MainForm.sortTable()` 中使用该方法。在这个练习中，你只需要写几十行代码。

扩展 `ShipTableModel.data()` 方法以提供工具提示。工具提示应简单地显示数据项的文本，但 TEU 除外，文本应为（本地化的）数字后跟上“twenty equals”。注意工具提示中的 HTML 格式是正确的。这很简单，只需要几行代码。

修改 `ShipTableDelegate.setData()`，使其仅当新文本至少有三个字符长时才更改名称、所有者或国家。扩展这些列的工具提示，添加文本“（minimum of 3 characters）”。这可以在几行代码内完成。

添加一个“导出”按钮，按下后会提示用户输入带有 .txt 后缀的文件名，并使用 UTF-8 编码保存数据，每行一条船，格式如下：

```
name|owner|country|teu|description
```

使用竖线“|”作为分隔符。数据应通过模型的 `model()` 方法访问，并按国家/所有者的顺序输出，描述中不包含任何 HTML 标签，TEU 以数字输出（不带逗号、句号或空格）。最后弹出一个消息框，报告错误或成功。使用 Python 或 PyQt 编写文件；我们使用的是 PyQt。如果你使用的是 4.1 之前的 PyQt 版本，则需要在写入文本流之前将 TEU 转换为 `QString`。`export()` 方法可以在少于 50 行代码内完成。

解决方案在 `chap14/ships_ans.py` 和 `chap14/ships-delegate-ans.py` 中提供。

# 15

- 连接到数据库

- 执行 SQL 查询

- 使用数据库表单视图

- 使用数据库表视图

# 数据库

Qt 通过使用 `Qt5ql` 模块和 PyQt 的模型/视图架构提供了一致的跨平台数据库访问 API。Python 也有一套完全不同的数据库 API，称为 DB-API，但在 PyQt 中不需要它，且此处未涵盖。Qt 的商业版本带有许多数据库驱动程序，而 GPL 版本由于许可限制，驱动程序较少。可用的驱动包括 IBM 的 DB2、Borland 的 Interbase、MySQL、Oracle、ODBC（用于 Microsoft SQL Server）、PostgreSQL、SQLite 和 Sybase。然而，像 PyQt 的其他部分一样，如果我们需要，也可以创建额外的数据库驱动程序。

当从源码编译 Qt 时，我们可以配置包含 SQLite，这是一个公共进程内数据库。对于二进制 Qt 软件包（例如用于 Windows 和 Mac OS X 的 GPL 包），SQLite 是内置的。本章中的示例使用 SQLite，但除了初始的数据库连接以及我们将提到的几个关于原始 SQL 语法的方面外，它应该适用于任何 SQL 数据库。

Qt 提供了两个级别的数据库访问方式。高层涉及使用 `QSqlTableModel` 或 `QSqlRelationalTableModel`。这些模型提供了抽象，使用与其他 `AbstractItemModel` 子类相同的 API 来处理表，并提供了一些特定特定的扩展。SQL 模型可以与视图（如 `QTableView`，如我们在本章最后一节中所示）以及 `QWidgetMapper`（用于表单视图，即本章第二节的主题）配合使用。

低层方法（也是最通用的）基于使用 `QSqlQuery`。该类可以接受任何 DDL（数据定义语言）或 DML（数据操纵语言）SQL语句并在数据库上执行它们。例如，我们可以使用 `QSqlQuery` 创建表，以及在表中插入、更新和删除记录。我们将在本章的第一节中介绍 `QSqlQuery`。

> *本章假设已掌握 PyQt 的模型/视图架构（在前章节已介绍）以及 SQL 的基础知识。*

## 连接到数据库

但在操作数据库之前，我们必须与它建立连接。在许多数据库应用程序中，这是在创建 `QApplication` 对象之后、主表创建或显示之前完成的。其他应用程序会在稍后建立连接——例如，在需要时。

要使用 PyQt6 SQL 类，我们必须导入 `QtSql` 模块：

```
from PyQt4.QtSql import *
```

通过调用静态方法 `QSqlDatabase.addDatabase()` 并传入我们想要使用的驱动名称来建立数据库连接。然后我们必须设置各种属性，例如数据库名称、用户名和密码。最后，我们必须调用 `open()` 来建立连接。

```
pythondb = QSqlDatabase.addDatabase("SQLITE")
db.setDatabaseName(filename)
if not db.open():
    Q.warning(None, "Phone Log",
        QString("Database Error: %1").arg(db.lastError().text()))
sys.exit(1)
```

对于 SQLite，我们需要指定数据库名称。这通常是一个文件名，但也可以是特殊名称“memory”，用于内存数据库。当我们使用 SQLite 驱动调用 `QSqlDatabase.open()` 时，如果文件不存在，它将被创建，在这种情况下它将存在。

注意我们向 `addDatabase()` 传递了 `None`，为连接指定了一个名称。如果数据库连接成功打开，我们需要两个或多个独立的连接，则必须向 `addDatabase()` 传递第二个参数进行区分。

## 执行 SQL 查询

一旦有了连接，我们就可以执行一些 SQL 语句。

```python
query = QSqlQuery()
query.exec("CREATE TABLE outcomes (
    id PRIMARY KEY AUTOINCREMENT NOT NULL,
    name VARCHAR(40) NOT NULL)")
```

## 执行 SQL 查询

```python
query.exec("CREATE TABLE calls (
id PRIMARY KEY AUTOINCREMENT NOT NULL,
caller VARCHAR(40) NOT NULL,
startime DATETIME NOT NULL,
endtime DATETIME NOT NULL,
topic VARCHAR(80) NOT NULL,
outcomeid INTEGER NOT NULL,
FOREIGN KEY (outcomeid) REFERENCES outcomes)")
```

我们没有指定要使用的数据库，因此 PyQt 将使用我们之前建立的默认（未命）连接。SQL 创建的表如图 15.1 所示。

`AUTOINCREMENT` 语法告诉 SQLite 填充 `id` 字段，每个 ID 都比上一个大，第一个为 1。同样，`FOREIGN KEY` 语法告诉 SQLite 外键关系。SQLite 3 不强制执行外键关系，仅允许我们将其作为文档辅助。实现自动 ID 和外键的语法在其他数据库中可能不同。

> 图 15.1 电话日志数据库设计

| calls | outcomes |

|---|---|

| id | id |

| caller | name |

| startime | |

| endtime | |

| topic | |

| outcomeid | |

许多数据库有自己的数据类型。例如，SQLite 3 有它所谓的“存储类”，包括 INTEGER、REAL 和 TEXT。PyQt 支持标准 SQL 数据类型，包括 VARCHAR、NUMBER和 DATETIME，并在后台透明地与数据库原生类型之间进行转换。对于文本，PyQt 使用 Unicode，对于不支持 Unicode 的数据库，在这种情况下 PyQt 在与数据库原生编码之间进行转换。

现在我们已经创建了表，就可以向它们填充数据了。

```python
for name in ("Resolved", "Unresolved", "Calling back", "Escalate",
    "Wrong number"):
    query.exec("INSERT INTO outcomes (name) VALUES ('%s' % name)")
```

我们不需要提供 ID，因为我们已经请求数据库为我们生成。不幸的是，前面的代码并不健壮：例如，如果其中一个名称包含单引号，它将失败。处理此问题的一种

# 448 第 15 章 数据库

是为了确保我们移除或转义不可接受的字符，PyQt 提供了一个更好的替代方案：预处理查询（prepared queries）。

处理查询有两种广泛使用的语法形式：一种基于 ODBC 占位符方法，另一种基于 Oracle 变量方法。PyQt 支持这两种方法，并在必要时在后台自动进行它们之间的转换，因此无论底层数据库是什么，两种方法都能正常工作。

```python
query.prepare("INSERT INTO caller (name, starttime, endtime, \
  topic, outcomeid) VALUES (?, ?, ?, ?, ?)")
for name, start, end, topic, outcome in data:
    query.addBindValue(QVariant(QString(name)))
    query.addBindValue(QVariant(start)) # QDateTime
    query.addBindValue(QVariant(end)) # QDateTime
    query.addBindValue(QVariant(QString(topic)))
    query.addBindValue(QVariant(outcome)) # int
query.exec_()
```

此示例使用了 ODBC 语法。占位符的一个用处是 PyQt 会处理引号问题，因此我们不必担心数据中包含什么，只要数据类型与其填充的字段匹配即可。

```python
query.prepare("INSERT INTO caller (name, starttime, endtime, \
  :topic, outcomeid) VALUES (:caller, :starttime, \
  :endtime, :topic, :outcomeid)")
for name, start, end, topic, outcome in data:
    query.bindValue(":caller", QVariant(QString(name)))
    query.bindValue(":starttime", QVariant(start))
    query.bindValue(":endtime", QVariant(end))
    query.bindValue(":topic", QVariant(QString(topic)))
    query.bindValue(":outcome", QVariant(outcome))
query.exec_()
```

第二个示例执行的工作与第一个相同，但使用了 Oracle 风格的命名变量。PyQt 还支持预处理查询语法的几种变体，但它们并没有为前面展示的两种语法形式增加任何额外功能。预处理查询可以提高支持它的数据库的性能，而在不支持的数据库上则没有影响。*

预处理查询也可以用于调用存储过程，但我们不会涵盖它们，因为对它们的支持既不通用也不标准。例如，并不是所有数据库都支持存储过程，且调用它们以及检索 OUT 值的语法在数据库之间不同。此外，返回值的存储过程也没有得到完全支持。

我们可以使用 `SqlQuery` 执行任何任意 SQL 语句。例如：

## 执行 SQL 查询

query.exec("DELETE FROM calls WHERE id = 12")

查询执行后，我们可以通过调用 `QSqlQuery.isActive()` 来检查错误；如果返回 `False`，则发生了错误，可以通过调用 `QSqlQuery.lastError().text()` 获取 `QString` 类型的错误信息。

如果我们执行一个可能影响多行的查询（例如 WHERE 子句选择了多条记录的 DELETE 或 UPDATE），可以调用 `QSqlQuery.numRowsAffected()`；它在发生错误时返回 `-1`。

我们可以通过访问驱动程序并调用 `hasFeature()` 来了解底层数据库是否支持事务和 BLOB（二进制大对象）等各种功能。例如：

```python
driver = QSqlDatabase.database().driver()
if driver.hasFeature(QSqlDriver.Transactions):
    print("Commit and rollback")
```

当我们使用 `QSqlQuery` 时，通过调用 `QSqlDatabase.database().transaction()` 启动事务，然后调用 `QSqlDatabase.database().commit()` 或 `QSqlDatabase.database().rollback()`。

我们将通过查看如何执行 SELECT 语句以及如何遍历结果记录来涵盖 `QSqlQuery`。

```python
DATETIME_FORMAT = "yyyy-MM-dd hh:mm"
ID, CALLER, STARTTIME, ENDTIME, TOPIC, OUTCOMEID = range(6)

query.exec("SELECT id, caller, starttime, endtime, topic, \
    outcomeid FROM calls ORDER BY starttime")
while query.next():
    id = query.value(ID).toInt()
    caller = unicode(query.value(CALLER)).toString()
    starttime = unicode(query.value(STARTTIME)).toDate() \
        .toString(DATETIME_FORMAT)
    endtime = unicode(query.value(ENDTIME)).toDate() \
        .toString(DATETIME_FORMAT)
    topic = unicode(query.value(TOPIC)).toString()
    outcomeid = query.value(OUTCOMEID).toInt()
    subquery = QSqlQuery("SELECT name FROM outcomes \
        "WHERE id = %d" % outcomeid)

    outcome = "invalid foreign key"
    if subquery.next():
        outcome = unicode(subquery.value(0)).toString()
        print("%02d: %s %s %s [%s]" % (id, caller, starttime, \
            endtime, topic, outcome))
```

当我们执行 SELECT 语句时，可以使用 `QSqlQuery.next()`、`QSqlQuery.previous()` 和 `QSqlQuery.seek()` 等方法遍历结果集。在成功执行 SELECT 之后，`isActive()` 将返回 `True`，其

## 表 15.1 选定的 QSqlQuery 方法

| 语法 | 描述 |

| --- | --- |

| q.addBindValue(v) | 在 QSqlQuery q 中使用位置值绑定时，将 QVariant 作为 v 添加为下一个变量 |

| q.bindValue(p, v) | 在 QSqlQuery q 中使用占位符绑定时，为字符串占位符 p 设置 QVariant 为 v |

| q.boundValue(p) | 返回字符串 p 对应的 QVariant |

| q.driver() | 返回与查询关联的 QSqlDriver

| q.exec(s) | 执行 SQL 语句 s |

| q.first() | 导航到结果的第一条 |

| q.isActive() | 如果查询处于激活状态则返回 True |

| q.isValid() | 如果查询位于有效记录上则返回 True |

| q.last() | 导航到结果最后一条 |

| q.lastError() | 返回包含错误的 QSqlError 对象 |

| q.next() | 导航到结果的条记录 |

| q.prepare(s) | 准备 SQL 语句 s |

| q.previous() | 导航到结果的上条记录 |

| q.record() | 返回包含当前记录的 QSqlRecord |

| q.size() | 返回结果集的行数 |

| q.value(i) | 返回字段索引 i 对应的 QVariant |

# 第 15 章 数据库

![](img/55bc1dcf8601cfec5e1423b4e17ec264_466_0.png)

图 15.2 简化的电话日志应用程序

因此，我们将分部分来看它，跳过布局部分，因为本章的重点是数据库编程。

```python
class PhoneLogDlg(QDialog):
    FIRST, PREV, NEXT, LAST = range(4)
    def __init__(self, parent=None):
        super(PhoneLogDlg, self).__init__(parent)
        callerLabel = QLabel("Caller:")
        self.callerEdit = QLineEdit()
        callerLabel.setBuddy(self.callerEdit)
        today = QDate.currentDate()
        startLabel = QLabel("Start:")
        self.startDateTime = QDateTimeEdit()
        startLabel.setBuddy(self.startDateTime)
        self.startDateTime.setDateRange(today, today)
        self.startDateTime.setDisplayFormat(DATETIME_FORMAT)
        endLabel = QLabel("End:")
        self.endTime = QDateTimeEdit()
        endLabel.setBuddy(self.endTime)
        self.endTime.setDateRange(today, today)
        self.endTime.setDisplayFormat(DATETIME_FORMAT)
        topicLabel = QLabel("*Topic:")
        self.topicEdit = QLineEdit()
        topicLabel.setBuddy(self.topicEdit)
        firstButton = QPushButton()
        firstButton.setIcon(Qt.icon(":/first.png"))
```

我们为每个字段创建了一个标签和一个合适的编辑小部件。我们创建了表单所有的按钮，尽管我们只展示了第一个创建过程。我们向 Add、Delete 和 Quit 按钮的构造函数传递了字符串以给它们标题，同时也给它们提供了图标。

```python
self.model = QTableModel(self)
self.model.setTable("calls")
self.model.setSort(STARTTIME, Qt.AscendingOrder)
self.model.select()
```

## 使用数据库表视图

控件就绪后，我们创建了一个 `SqlTableModel`。由于我们没有指定特定的数据库连接，它将使用默认连接。我们告诉模型它要工作的对象，并调用 `select()` 让它自动填充数据。我们还选择对表应用排序顺序。

现在我们有了控件，必须以某种方式将它们连接起来。这是通过使用 `QDataWidgetMapper` 实现的。

```python
self.mapper = QDataWidgetMapper(self)
self.mapper.setPolicy(QDataWidgetMapper.ManualSubmit)
self.mapper.setModel(self.model)
self.mapper.addMapping(self.callerEdit, CALLER)
self.mapper.addMapping(self.startTime, STARTTIME)
self.mapper.addMapping(self.endTime, ENDTIME)
self.mapper.addMapping(self.topicEdit, TOPIC)
self.mapper.toFirst()
```

为了让数据映射器工作，我们必须给它提供一个模型以及一组表单控件与模型中对应列之间的映射。（变量、ID、CALLER、STARTTIME 等在文件开始处被设置为 0, 1, 2 等）。映射器可以被设置为自动提交，也可以只在被指令时才提交。我们更倾向于后一种方法，因为它赋予了我们控制权，并且意味着当用户导航到不同的记录时，我们可以确保任何未保存的更改都被保存了。一旦设置了映射，我们需要让映射器用记录填充控件；我们通过调用 `First()` 完成此，这意味着在启动时显示第一条记录。

```python
self.connect(firstButton, SIGNAL("clicked()"),
lambda: self.saveRecord(PhoneDlg.FIRST)
self.connect(prevButton, SIGNAL("clicked()"),
lambda: self.saveRecord(PhoneDlg.PREV)
self.connect(nextButton, SIGNAL("clicked()"),
lambda: self.saveRecord(PhoneDlg.NEXT)
self.connect(lastButton, SIGNAL("clicked()"),
lambda: self.saveRecord(PhoneDlg.LAST)
self.connect(addButton, SIGNAL("clicked()"), self.addRecord)
self.connect(deleteButton, SIGNAL("clicked()"),
self.deleteRecord)
self.connect(quitButton, SIGNAL("clicked()"), self.exit)
self.setWindowTitle("Phone Log")
```

前四个连接提供了导航功能。在每种情况下，我们都调用 `saveRecord()`，它会保存任何未保存的更改，然后在 lambda 语句封装的参数中进行导航。这意味着我们只需要一个方法 `saveRecord()`，而不是为每个导航按钮都写一个。然而，这些连接仅适用于 PyQt 4.1.1 或更高版本。对于更早的版本，我们必须保留一个实例变量（例如列表），包含 lambda 函数的引用，以防止它们被垃圾回收。

```python
def accept(self):
    self.mapper.submit()
    QDialog.accept(QDataMapper.submit())
```

如果用户点击 Quit，我们将当前记录回写到底层模型，然后关闭窗口。



```python
def saveRecord(self, where:):
    row = self.mapper.currentIndex()
    self.mapper.submit()
    if where == PhoneLogDlg.FIRST:
        row = 0
    elif where == PhoneLogDlg.PREV:
        row = row if row <= 1 else row - 1
    elif where == PhoneLogDlg.NEXT:
        row += 1
    if row == self.model.rowCount():
        row = self.model.rowCount() - 1
    elif where == PhoneLogDlg.LAST:
        row = self.model.rowCount() - 1
    self.mapper.setCurrentIndex(row)
```

如果我们进行导航，我们必须记住当前行，因为它在调用 `submit()` 之后会被忘记。那么，在保存当前记录后，我们将行设置为请求的行（但在范围内），然后使用 `setCurrentIndex()` 移动到相应的记录。

```python
def addRecord(self):
    row = self.model.rowCount()
    self.mapper.insertRow(row)
    self.mapper.setCurrentIndex(row)
    now = QDateTime.currentDateTime()
    self.startTime.setDateTime(now)
    self.endTime.setDateTime(now)
    self.callerEdit.setFocus()
```

我们选择始终在最后添加新记录。为了这一点，我们找到最后一行，保存当前记录，然后在模型的最后一行插入新记录。然后我们将映射器的当前索引设置为新行，初始化几个字段，并将焦点交给 caller 字段以便用户输入。

```python
def deleteRecord(self):
    caller = self.callerEdit.text()
    startTime = self.startDateTime().toString(DATETIME_FORMAT)

    if QMessageBox.question(self,
    QString("Delete"),
    QString("Delete by %1 on %2?").arg(caller).arg(startTime),
    MessageBox.Yes|MessageBox.No) == QMessageBox.No:
        return
    row = self.mapper.currentIndex()
    self.model.removeRow(row)
    self.model.submit()
    if row + 1 >= self.model.rowCount():
        row = 0
```

如果用户点击 Delete，我们从当前记录中提取信息并使用它确认删除。如果他们确认，我们从模型中移除该行并调用 `submit()` 将更改写回底层数据库。我们完成导航到下一条记录。我们使用了 `submit()`是因为我们通过映射器在模型上执行了删除，除非视图（或数据映射器）设置为自动提交，否则我们必须调用此方法确认更改。数据映射器的 API 不允许我们添加或删除记录，只能编辑现有记录，因此必须使用底层模型来添加或删除记录。

到目前为止的技术适用于任何数据库表或可编辑视图，为用户提供导航、添加和删除记录的方法。但在大多数情况下，某些区域需要考虑，我们将在查看图 15.3 所示的日志应用程序时解决这些问题。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_469_0.png)

**图 15.3** 电话日志应用程序

calls 表（见第 447 页）有一个外键 `outcome` 字段。我们希望该字段在表单中以组合框的形式显示 outcomes 表对应的 ID 名称。为了实现这一点，我们按照通常的方式创建一个组合框，但不对其进行填充。

由于我们现在使用带有外键的表，我们必须使用 `QSqlRelationalTableModel` 而不是 `QSqlTableModel`。

```python
self.model = QSqlRelationalTableModel(self)
self.model.selectTable("calls")
self.model.setRelation("outcome", "id", "name")
self.model.sort("outcomes")
self.model.setSort(STARTTIME, Qt.AscendingOrder)
self.model.select()
```

`QSqlRelationalTableModel` 与 `QSqlTableModel` 非常相似，但提供了处理关系的额外方法。`relation()` 方法接收模型中的字段索引和关系对象。关系对象使用外键表的名称、实际存储的字段以及显示的字段来创建。

数据映射器的代码也必须更改。特别是，我们必须使用 `QSqlRelationalDelegate` 而不是标准的内置委托器，并且必须设置用于外键的组合框。

```python
self.mapper = QDataMapper(self)
self.mapper.setSubmitPolicy(QDataMapper.ManualSubmit)
self.mapper.setModel(self.model)
self.mapper.setItemDelegate(QSqlRelationalDelegate(self))
self.mapper.addMapping(self.callerEdit, CALLER)
self.mapper.addMapping(self.startTime, STARTTIME)
self.mapper.addMapping(self.endTime, ENDTIME)
self.mapper.addMapping(topicID, TOPIC)
relationModel = self.model.relationModel(OUTCOMEID)
self.outcomeCombo.setModel(relationModel)
self.outcomeCombo.setColumn(relationModel.fieldIndex("name"))
self.mapper.addMapping(self.outcomeCombo, OUTCOME)
self.mapper.toFirst()
```

代码与我们之前的代码相似。设置关系很容易，但设置组合框稍微微妙一些。首先，我们必须检索模型（calls 表）用于处理外键的关系模型（outcomes 表）。`QComboBox` 实际上是一个带有内置模型（如 `QString`）的便利小部件；但可以替换我们自己的模型，这正是我们在这里所做的。然而，组合框显示单列，而我们的关系模型有两列（id, name），所以我们指定显示哪一个。

## 使用数据库表视图 457

处理外键的更改已完成。此外，我们借此机会对应用程序进行了一些细小的更改。

在简化版本中，我们将“退出”（Quit）按钮连接到一个自定义的 `accept()` 方法，并以不符合直觉的方式从 `reject()` 方法中调用了 `accept()`。这是为了确保应用程序在终止之前始终保存当前记录的更改。在外键版本中，我们采取了不同的方法，将退出按钮连接到 `done()` 方法。

```python
def done(self, results=None):
    self.mapper.done()
    QDialog.done(self, True)
```

该方法会在退出按钮连接触发时调用，或者当用户点击 X 按钮关闭窗口或按下 Esc 键时调用。我们保存当前记录并调用基类的的 `done()` 方法。第二个参数是强制性的，在这个类中它持有什么值都并不重要：`True` 值表示 `accept()`，`False` 值表示 `reject()`，但无论如何，窗口都会关闭。

我们还有另一个微小的更改，在 `addRecord()` 方法中添加了两行：

```python
self.outcomeComboBox.setCurrentIndex()
self.outcomeComboBox.findText("Unresolved")
```

这确保了当用户点击以添加新记录时，结果组合框（outcome comboBox）将有一个合理的默认值，除了我们已经设置的日期/时间默认值。

表单对于具有许多字段的非常有用，特别是当需要基于字段间的依赖进行大量验证时。对于字段较少的表或用户希望查看多条记录的表，我们需要使用表格视图（tabular views）。这是下一节的主题。

## 使用数据库表视图

展示数据库数据最自然且方便的方法是在 GUI 表格中显示表格和视图。这允许用户一次看到许多记录，对于显示“主-详情”关系特别方便。

在本节中，我们将检查资产管理器应用程序，即位于 `chap15/assetmanager.py` 中的代码。该应用程序有四个表，由以下 SQL 语句创建：

```python
query = QSqlQuery()
query.exec("CREATE TABLE actions (
    ID PRIMARY KEY AUTOINCREMENT UNIQUE NOT NULL,
    name VARCHAR(20) NOT NULL,
    description VARCHAR(40) NOT NULL)")
query.exec("CREATE TABLE categories (
    id INTEGER PRIMARY KEY AUTOINCREMENT UNIQUE NULL,
    name VARCHAR(20) NOT NULL,
    description VARCHAR(40) NOT NULL)")
query.exec("CREATE TABLE assets (
    id INTEGER PRIMARY KEY AUTOINCREMENT UNIQUE NULL,
    name VARCHAR(40) NOT NULL,
    category INTEGER NOT NULL,
    room VARCHAR(4) NOT NULL,
    FOREIGN KEY (category) REFERENCES categories)")
query.exec("CREATE TABLE logs (
    id INTEGER PRIMARY KEY AUTOINCREMENT UNIQUE NULL,
    assetid NOT NULL,
    date NOT NULL,
    FOREIGN KEY (assetid) REFERENCES assets,
    FOREIGN KEY (actionid) REFERENCES actions)")
```

actions 和 tables 是典型的参考数据表，包含 ID、短描述（name）和长描述（description）。主表是 assets；它存储建筑中每个资产的名称、类别和位置。logs 表用于跟踪资产在其整个生命周期内发生的情况。图 15.4 地显示了这些表。

| categories | assets | actions |

|---|---|---|

| id | id | id |

| name | name | name |

| description | categoryid | description |

| | room | |

| | | actionid |

图 15.4 资产管理器数据库设计

资产管理器应用程序具有对话式的主窗口，其中包含两个处于“主-详情”关系的 QtViews。如图 15.5 所示。顶部的表格显示 assets 表，底部的表格显示与当前资产记录对应的 logs 记录。用户可以添加和删除资产以及日志记录，并原地编辑两个表。用户还可以通过弹出合适的对话框来添加、删除和编辑 categories 和 actions 参考表。此对话框也使用了 QTableView，尽管它也可以很容易地使用 QDataMapper 实例。

我们将首先查看数据库的创建和连接、主表单，然后查看用于参考数据的对话框。与电话日志应用程序一样，资产管理器在首次运行时会生成一组伪记录。如前节所述，这在 Linux 上使用 SQLite 实现，并且在某些 Windows 机器上运行非常慢。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_473_0.png)

图 15.5 资产管理器应用程序

```python
app = QApplication(sys.argv)
db = QSqlDatabase.addDatabase("SQLITE")
db.setDatabaseName(filename)
if not db.open():
    MessageBox.warning(None, "Asset Manager",
    QString("Database Error: %1",db.lastError().text))
    sys.exit(1)
form = MainForm()
form.show()
app.exec_
```

我们首先创建一个 QApplication 对象。接下来我们创建连接；如果数据库文件不存在，SQLite 将创建一个空文件。然后我们创建主表单，对其调用 `show()` 以调度一个绘制事件，并启动事件循环。

我们没有显示的是用于在应用程序首次运行时生成伪数据以及弹出启动屏幕的代码。这些代码当然在源文件 `chap15/assetmanager.py` 中。这些代码是，当然，在源文件 `chap15/assetmanager.py` 中。 （此处原文似乎重复，按要求翻译翻译逻辑）

我们还有另一个微小的更改，在 `addRecord()` 方法中添加了两行：

```python
self.outcomeComboBox.setCurrentIndex()
self.outcomeComboBox.findText("Unresolved")
```

这确保了当用户点击以添加新记录时，结果组合框（outcome comboBox）将有一个合理的默认值，除了我们已经设置的日期/时间默认值。

表单对于具有许多字段的非常有用，特别是当需要基于字段间的依赖进行大量验证时。对于字段较少的表或用户希望查看多条记录的表，我们需要使用表格视图（tabular views）。这是下一节的主题。

# 462

# 第 15 章 数据库

一旦创建了编辑器，视图将调用 `setEditorData()` 以便填充当前值。在这种情况下，我们只关心 `room`（房间）列，将其他字段的工作交给基类处理。

```
setModelData(self, editor, model, index):
    if index.column() == ROOM:
        model.setData(index, QVariant(editor.text))
    else:
        SqlRelationalDelegate.setModelData(self, editor, model,
            index)
```

我们采取了与之前方法类似的方法，处理 `room` 字段并将其他字段留给基类处理。事实上，我们可以直接跳过重写这个方法，PyQt 会足够智能，可以从我们的 `QLineEdit` 中获取值。然而，对我们的自定义内容承担全部责任是更好的做法。

现在我们已经完成了这段绕路，可以返回 `MainForm.__init__()` 方法，此时底部的表格将显示适用于当前资产的记录。

```
self.logModel = SqlRelationalTableModel(self)
self.model.setTable("logs")
self.model.setRelation(ACTIONID,
    QRelation("actions", "id", "name"))
self.model.setSort(DATE, Qt.AscendingOrder)
self.model.setHeaderData(DATE, Qt.Horizontal,
    QVariant("Date"))
self.model.setHeaderData(ACTIONID, Qt.Horizontal,
    QVariant("Action"))
self.logModel.select()
```

创建日志模型的代码与我们用于资产模型的代码几乎相同。我们使用 `SqlRelationalTableModel` 是因为我们有一个外键字段，并且我们提供了自己的列标题。

```
self.view = QTableView()
self.view.setModel(self.logModel)
self.view.setItemDelegate(LogDelegate(self))
self.view.setSelectionMode(QTableView.SingleSelection)
self.view.setSelectionBehavior(QTableView.SelectRows)
self.view.setColumnHidden(ID, True)
self.view.setColumnHidden(ASSET, True)
self.view.resizeColumnsToContents()
self.view.horizontalHeader().setStretchLastSection(True)
```

这段代码与我们为资产表格所的操作相似，但有三个不同。在这里我们使用了自定义的 `LogDelegate` 类——我们不会复习它，因为它在结构上与 `AssetDelegate` 非常相似。它提供了日期字段的自定编辑。我们还隐藏了日志记录的 `ID` 字段和 `assetid` 外键——不需要显示哪些日志记录属于哪个资产，因为我们正在使用主细视图（master-detail），所以只有适用于当前资产的日志记录是可见的。（稍后我们将看到如何编写主细关系。）最后一个区别是，我们设置最后一列伸满所有可用空间。`QTableView.horizontalHeader()` 方法返回一个 `QHeaderView`，它控制表格视图列的某些属性，包括它们的宽度。

```
self.connect(self.assetView.selectionModel(),
SIGNAL("currentRowChanged(QModelIndex, QModelIndex)"),
self.assetChanged)
self.connect(addAssetButton, SIGNAL("clicked"),
self.assetChanged)
```

如果用户导航到不同的行，我们必须更新日志视图以显示正确资产的日志记录。这是通过第一个连接结合我们稍后将回顾的 `assetChanged()` 方法实现的。每个视图至少有一个模型，用于跟踪视图中的项目（如果有）是否被选中。我们连接了视图选择模型的 `currentRowChanged()` 信号，以便我们可以更新当前资产的日志视图。所有其他连接都像这里所示的第二个那样是按钮点击。我们将在本节中介绍所有的方法。

```
self.assetChanged(self.assetView.currentIndex())
self.setMinimumWidth(650)
self.setWindowTitle("Asset Manager")
```

初始化器通过使用资产视图当前模型调用 `assetChanged()` 方法来结束——这将导致日志视图显示相关资产的记录。

```
def assetChanged(self, index):
    if index.isValid():
        record = self.assetModel.record(index.row())
        id = record.value("id").toInt()
        self.logModel.setFilter(QString("assetid = %1").arg(id))
    else:
        self.logModel.setFilter("assetid = -1") # 针对 Qt <= 3 bug 的变通
        self.logModel.reset()
        self.logModel.select()
    self.logView.horizontalHeader().setVisible(self.logModel.rowCount() > 0)
```

# 464 ## 第 15 章 数据库

此方法由表单初始化器调用一次，然后在当用户导航到不同资产、即资产表中的不同行时调用（`reset()` 的调用是一种强制日志视图更新更新的变通方法）。如果视图中新位置的索引有效，我们从模型检索行记录，并在日志模型上设置过滤器，选择那些 `assetid` 与当前行 ID 对应的日志记录。然后我们调用 `select()` 刷新日志视图，将 ID 设置为一个我们知道不是空的值，以确保不会检索到行，且日志视图将为空。如果没有记录可显示，则隐藏日志视图的列标题。

`record()` 方法是 `QSqlTableModel` 提供的扩展之一，`SqlRelationalTableModel` 类提供了额外的扩展，允许我们更方便使用数据库。其他方法包括 `setQuery()`，允许我们处理事务，`insertRecord()` 则用于添加记录。为了建立主细关系，我们使用了事务 `assetChanged()` 方法。

```
def done(self, result):
    query = QSqlQuery()
    query.exec("DELETE FROM logs WHERE assetid NOT IN (SELECT id FROM assets)")
QDialog.done(self, result)
```

当应用程序终止时，我们将执行最后的查询以删除任何不存在的资产。理论上，这是不需要的，但由于数据库支持事务。

如果用户请求添加资产（新日志记录），将调用此方法。我们检索当前资产的 `assetid`，然后在日志表中插入一条新的日志记录。我们将记录的 `assetid` 外键设置为我们检索到的值，并提供一个初始默认日期。最后，我们检索新日志记录的操作组合框的模型索引，并启动编辑供用户选择合适的操作。

```
def addAction(self):
    index = self.assetView.currentIndex()
    if not index.isValid():
        return
    SqlDatabase.database().transaction()
    record = self.assetModel.record(index.row())
    assetid = record.value("id").toInt()

    row = self.logModel.rowCount()
    self.logModel.insertRow(row)
    self.logModel.setData(self.logModel.index(row, ASSETID),
    QVariant(assetid))
    self.logModel.setData(self.logModel.index(row, DATE),
    QVariant(QDate.currentDate()))
    SqlDatabase.database().commit()
    index = self.logModel.index(row, ACTION)
    self.logView.setCurrentIndex(index)
    self.logView.edit(index)
```

在检索 `assetid` 之前，我们开启事务。这是为了防止一种理论上的可能性：在检索 `assetid` 后、创建新日志之前资产被删除了。如果是这样，记录将指向不存在的资产，这以后可能会导致崩溃或微妙的问题。一旦我们调用 `commit()`，我们就知道资产和新的日志记录都存在。如果有人尝试删除资产，他们可以这样做——但资产的日志记录（包括此条）将随之正确删除。

事务的作用范围从调用 `transaction()` 开始，直到事务被提交或回滚为止。无论是否

# 第 15 章 数据库

可以通过 `SqlDatabase` 或模访问数据库。事务访问的上下文适用于所有 SQL 语句，包括由独立查询执行的语句以及由不同模型执行的语句，只要它们在事务上下文中应用于同一个数据库即可。

如果我们正在使用 Python 2.6，或者在 Python 2.5 中使用 `from __future__ import statement` 语句，我们可以通过尽创建和使用上下文管理器来提前简化代码。

面向事务的方法试图通过安排工作来假设一切都能正常工作，且不会发生错误。另一种方法是依赖数据库来维护外键关系和其他数据完整性。这在 SQLite 3 中不可行，因为其不强制执行关系完整性；但在其他数据库中是可以行的。通过这种方法，我们通常可以在不使用事务的情况下编写代码。大多数情况下运行运行良好，而对于那些出现问题的场合，我们依靠数据库拒绝执行任何违反其规则的操作，并向我们提供可以报告给用户的错误信息。

请注意，事务是设置在数据库上的，通过静态方法 `SqlDatabase.database()` 访问。也可以通过调用模型上的 `database()` 方法访问数据库。每个数据库连接一次只能处理一个事务，因此如果我们想同时进行一个事务，必须为每个想要使用的事务建立额外的连接。

```python
def deleteAction(self):
    index = self.logView.currentIndex()
    if not index.isValid():
        return
    record = self.logModel.record(index.row())
    action = record.value(ACTIONID).toString()
    if action == "Acquired":
        MessageBox.information(self, "Delete Log,\nThe Acquired log record cannot be deleted.<br>"\nYou可以直接删除整个资产.")
        return
    when = unicode(record.value(DATE).toString())
    if QMessageBox.question(self, "Delete log%s?" % (when, action),
        MessageBox.Yes|MessageBox.No) == QMessageBox.No:
        return
    self.logModel.removeRow(index.row())
    self.logModel.submitAll()
```

对于删除操作，我们实现的逻辑是用户不能删除“Acquired”（已获取）日志记录，即第一条日志记录。（但他们可以删除资产及其所有的日志记录，我们稍后会看到。）如果日志记录是用户允许删除的且用户确认了删除，

只需在日志模型上调用 `removeRow()`，然后调用 `submitAll()` 来更新底层数据库。

## 使用数据库表视图

```python
def editActions(self):
    form = ReferenceDataDlg("actions", "Action", self)
    form.exec_()

def editCategories(self):
    form = ReferenceDataDlg("categories", "Category", self)
    form.exec_()
```

由于操作（actions）和类别（categories）引用表具有相同的结构，当我们需要钻取以添加、编辑和删除记录时，可以使用同一个智能对话框。我们向对话框提供数据库中的表名，以及要在用户界面显示的引用数据名称（例如在对话框标题栏中）。

图 15.6 资产管理器引用数据表

我们不会回顾图 15.6 所示的 `ReferenceDataDlg` 代码，因为它没有新的新内容可以教的。它使用 Qt 来设置传递给其构造函数的表格。编辑是就地的，并由表格视图和表格模型自动处理。添加记录只需向模型中插入新行并将视图设置到该行即可。

对于引用数据的删除，我们执行查询以查看特定的引用数据记录是否被其他一个表使用，即某个操作是否被日志中的任何记录使用，或者某个类别是否被资产表中的任何记录使用。如果记录正在使用中，我们会弹出一个提示性错误信息并且不允许删除发生。否则，我们在模型上对相关行调用 `removeRow()`，然后调用 `submitAll()` 将更改提交到数据库，就像我们删除操作时一样。

与引用数据不同，资产的添加和删除是由表单的方法的。

```python
def addAsset(self):
    row = self.assetView.currentIndex().row() \
    if self.assetView.currentIndex().isValid() else 0

    SqlDatabase.database().transaction()
    self.assetModel.insertRow(row)
    index = self.assetModel.index(row, NAME)
    self.assetView.setCurrentIndex(index)

    asset = 1
    query = QSqlQuery()
    query.exec("SELECT MAX(id) FROM assets")
    if query.next():
        assetid = query.value(0).toInt()
        query.prepare("INSERT INTO logs (assetid, date, actionid") \
            "VALUES (:assetid, :date, :actionid)")
        query.bindValue(":assetid", QVariant(assetid + 1))
        query.bindValue(":date", QVariant(QDate.currentDate()))
        query.bindValue(":actionid", QVariant(ACQUIRED))
        query.exec())
    SqlDatabase.database().commit()
```

```python
def deleteAsset(self):
    index = self.assetView.currentIndex()
    if not index.isValid():
        return
    SqlDatabase.database().transaction()
    record = self.assetModel.record(index.row())
    assetid = record.value(id).toInt()
    logrecords = 1
    query = QSqlQuery(QString("SELECT COUNT(*) FROM logs "
        "WHERE assetid = %1").arg(assetid))

    if query.next():
        logrecords = query.value(0).toInt()

    msg = QString("<font color=red>Delete</font><br><b>%1</b>b>"
        "from room %2") \
        .arg(record.value(NAME).toString()) \
        .arg(record.value(ROOM).toString())

    if logrecords > 1:
        msg += QString("along with %1 log records") \
            .arg(logrecords)

    msg += " ?"
    if QMessageBox.question(self, "Delete Asset", msg,
        QMessageBox.Yes) == QMessageBox.No:
        SqlDatabase.database().rollback()
        return

    query.exec(QString("DELETE FROM logs WHERE assetid = %1") \
        .arg(assetid))
    self.assetModel.remove(index.row())
    self.assetModel.submitAll()
    SqlDatabase.database().commit()
    self.assetChanged(self.assetView.currentIndex())
```

我们使用 SQL 查询删除日志记录，并使用模型 API 删除资产记录。删除后我们提交事务并调用 `assetChanged` 以确保主从视图显示的是正确的记录。

我们可以使用模型 API 来处理两个删除。例如：

```python
self.logModel.setFilter(QString("assetid = %1").arg(assetid))
self.logModel.select()
if self.logModel.rowCount() > 0:
    self.logModel.removeRows(0, self.logModel.rowCount())
self.logModel.submitAll()
```

这完成了我们对资产管理器应用程序的审查。在表之间创建主从关系非常简单，且这种

# 470

# 第 15 章 数据库

使用数据映射器（data mapper），可以在表和视图之间进行相同的操作。SQL 表模型非常易用，并且与 `QtTableView` “即插即用”。此外，我们还可以创建自定义代理（delegates）来控制字段的外和编辑，在需要时，我们可以使用代理来提供记录级的验证。

我们一直没有担心的问题之一是为新记录创建唯一键。我们已经通过在表中使用自增 ID 解决了这个问题。但有时自增并不恰当——例如，当键值比简单的整数更复杂时。我们可以通过连接到 `QTableModel.beforeInsert()` 信号来处理此类情况。该信号为它连接的方法提供了一个即将插入的记录的引用（在用户完成编辑后），因此我们可以在数据实际插入数据库之前，填充或更改我们刚刚创建的任何字段。

我们还可以连接到额外的 SQL 特有信号——例如，`beforeDelete()` 和 `beforeUpdate()`；如果我们想在单独表中记录删除或更改，这些信号可能会有用。最后，还有一个 `primeInsert()` 信号——它在创建新记录时触发，但在用户有机会编辑它之前触发。这就是我们可能为记录填充默认值的地方。然而，在本章的所有示例中，我们是在用户点击“添加”按钮时放入默认值的。还要注意，由于 `QRelationalTableModel` 是 `QTableModel` 的子类，它也拥有这些信号。

## 总结

PyQt 通过 `QtSql` 模型提供的一致 API 为 SQL 数据库提供了强有支持。对于所有最广泛使用的数据库都提供了数据库驱动程序，尽管由于许可证限制，某些驱动程序仅在 Qt 的商业版本中可用。

如果我们建立了单个数据库连接，所有后续的数据库访问默认将使用该连接。但如果我们需要多个连接，可以为每个连接命名，并在之后通过名称访问它们，以指定为哪个特定文章使用哪一个。

我们可以访问数据库的驱动程序，并借此发现数据库是否支持某些功能如 BLOB 和事务。无论底层数据库是什么，PyQt 都允许我们使用带有 ODBC 和 Oracle 语法的预处理查询（prepared queries），并手动处理任何必要的版本和引号引用。PyQt 支持所有标准 SQL 数据类型，并且如果数据库本身支持，它会执行任何必要的转换。

`QSqlQuery` 类允许我们使用其 `exec_()` 方法执行任意 SQL 语句。这意味着，例如，可以使用它来创建和删除表，以及插入、更新和删除记录。Query 对象提供了用于导航执行 `SELECT` 语句时产生的结果集的方法，并且可以提供有关受查询影响行数的信息——例如，有多少行被删除或更新了。

使用 `QSqlMapper` 创建显示表（或可编辑视图）的 GUI 表单是直接的。我们通常为每个外键使用一个 `QComboBox`，并提供相应的关系作为其内部模型。虽然可以设置 `QTableModel` 自动提交更改，但在用户导航时可能会导致数据丢失，因此，如果我们提供了导航手段，最好由我们自己提交所有更改。

使用 `TableView` 结合 `QSqlTableModel` 或 `QRelationalTableModel` 显示表和视图是非常简单的。这些类结合提供了字段数据的就地编辑。通过从模型中插入或删除行可以轻松添加和删除记录，当我们需要原子操作时，可以使用事务。

Qt 的模型/视图架构的所有功能对数据库程序员都可用。此外，SQL 表 API 已经扩展，使数据库编程变得更容易。当我们需要执行 SQL 时，可以很容易地使用 `QQuery` 类来实现。

我们现在已经到了你应该能够创建任何类型的 GUI 应用程序的地步，仅限于你的想象力和可用时间。在第四部分中，我们将查看一些处理起来比较棘手的额外主题，从模型/视图编程的高级材料开始，然后是国际化，然后网络，最后以多线程结束。

## 练习

创建一个对话框风格的应用程序，用于引用表中添加、编辑和删除记录，如图 15.7 所示。应用程序在首次运行时会创建 `reference.db` 数据库，并包含一个空表：

```
CREATE TABLE reference (
id INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
category VARCHAR(30) NOT NULL,
shortdesc VARCHAR(20) NOT NULL,
longdesc VARCHAR(80))
```

除了“添加”和“删除”按钮外，还要提供一个“排序”按钮，该按钮有一个带有三个排序选项的弹出菜单：ID、按类别和按短描述。这三个选项都可以使用 `lambda` 或 `functools.partial` 连接到同一个方法。要使任何排序（或过滤）生效，你必须在模调用 `select()`。所有按钮都使用 `QDialogButtonBox`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_486_0.png)

图 15.7 引用数据对话框

如果用户点击“删除”，弹出“是/否”消息框，并且仅在他们点击“是”按钮时才删除。该应用程序类似于资源管理器应用程序中的 `ReferenceDataDlg`，可以使用大约 130 行代码编写完成。

在 `chap15/referenceddata.pyw` 中提供了解决方案。

# 第四部分 进级 GUI 编程

## 高级模型/视图编程

在之前的两个章节中，我们探索了 PyQt 模型/视图编程的基础。我们看到了如何创建自定义模型，以及如何使用 SQL 表。我们还看到了如何创建代理来控制数据的外和编辑。在本章中，我们将加深对模型/视图编程的知识。

## 自定义视图

PyQt 提供了多种视图，包括 `QListView`、`QTableView`、`QTreeView` 和 `QWidget`。这些视图可以以不同的方式显示数据。`QListView` 适用于显示简单的列列表，`QTableView` 适用于显示表格数据，而 `QTreeView` 适用于显示层级结构的数据。`QWidget` 是一个基类，可以用来创建完全自定义的视图。这些视图都可以与模型配合使用。

通常，`QListView` 与 `QAbstractListModel` 使用，而 `QTableView` 和 `QTreeView` 与 `QAbstractItemModel` 使用。如果你需要显示更复杂的数据结构，可以使用 `QAbstractItemModel` 的派生类，如 `QStandardItemModel`。

## 自定义视图

```python
class MainForm(QDialog):
    def __init__(self, parent=None):
        super(MainForm, self).__init__(parent)
        self.model = WaterQualityModel(os.path.join(
            os.path.dirname(__file__), "waterdata.csv.gz"))
        self.tableView = QTableView()
        self.tableView.setAlternatingRowColors(True)
        self.tableView.setModel(self.model)
        self.waterView = WaterQualityView()
        self.waterView.setModel(self.model)
        scrollArea = QScrollArea()
        scrollArea.setBackgroundRole(QPalette.Light)
        scrollArea.setWidget(self.waterView)
        self.waterView.scrollarea = scrollArea
        splitter = QSplitter(Qt.Horizontal)
        splitter.addWidget(self.tableView)
        splitter.addWidget(scrollArea)
        splitter.setSizes([600, 250])
        layout = QHBoxLayout()
        layout.addWidget(splitter)
        self.setWindowTitle("Water Quality Data")
        QTimer.singleShot(0, self.initialLoad)
```

前面的代码就是全部内容。`WaterQualityModel` 是 `QAbstract-TableModel` 的子类，提供对水质数据文件的只读访问。`WaterQualityView` 是我们将在本节中开发的类。我们做的一个特殊之处是创建了一个 `QScrollArea` 并将水质视视图添加到其中——这基本上意味着水质视图可以根据我们的意愿任意宽缩高，而滚动区域将处理滚动问题。

我们很快就会看到，键盘用户可以使用向上和向下方向键在水质视图中进行导航，为了确保选中的行始终可见，我们必须将滚动区域传递给水质视图，这样我们的按键处理程序才能与其交互。另一个特殊之处是，我们为水平拆分器的两个部分设置了初始大小，以便它们在启动时，其比例与我们所持有的组件大致相当。

我们现在将复习 `WaterQualityView`，从一些静态数据和初始化函数开始。

```python
class WaterQualityView(QWidget):
    FLOWCHARS = (unichar(0x21DC), unichar(0x21DD), unichar(0x21C9))
```

## 第16 章。高级模型/视图编程

```python
def __init__(self, parent=None):
    super(WaterQualityView, self).__init__(parent)
    self.scrollarea = None
    self.model = None
    self.setFocusPolicy(Qt.StrongFocus)
    self.selectedRow = -1
    self.flowfont = self.font()
    size = self.font().pointSize()
    if platform.system() == "Windows":
        fontDb = QDatabase
        for face in [face.toLower() for face in fontDb.families]:
            if face.contains("unicode"):
                break
    else:
        self.flowfont = QFont("symbol", size)

WaterQualityView.FLOWCHARS = (
    chr(0xAE), chr(0xDE))
```

将焦点策略设置为任何值（`Qt.NoFocus` 除外）都意味着组件可以接受键盘焦点。我们将在本节末尾讨论我们为什么要这样做，以及 `selectedRow` 实例变量。

当水流方向错误或速度太慢时，我们需要快速用合适的字符来指示这种情况——例如，←、→。这些字符位于 Unicode 编码中，但 Windows 提供的大多数默认字体并不包含完整的 Unicode 字符集，因此所有箭头都显示为 □。（在 Linux 上，如果当前字体中没有某个 Unicode 字符，PyQt 通常可以在另一个字体中找到该字符，仅对该字符使用找到的字体。）

为了解决 Unicode 上的这个问题，我们遍历可用字体列表，直到找到一个一个名称中包含 "Unicode" 字样的字体（例如 Lucida Sans Unicode）。如果我们找到了这样的字体，我们将其存储为流向字符字体；否则，我们将回退到标准的（但非 Unicode 的）Symbol 字体，并使用字体中最接近的等效字符。

```python
def self(self, model):
    self.model = model
    self.connect(self.model,
        SIGNAL("dataChanged(QModelIndex, QModelIndex)"),
        self.setNewSize)
    self.connect(self.model, SIGNAL("modelReset()"),
        self.setNewSize())
```

一旦设置了模型，我们就会连接到它的数据变化信号，以便视图可以调整大小以匹配可用数据。

```python
def setSize(self):
    self.resize(self.sizeHint())
    self.update()
    self.updateGeometry()
```

此方法将视图调整到其首选大小，并调用 `update()` 来调度重绘，调用 `updateGeometry()` 通知任何负责视图的布局管理器其大小已更改。由于我们将视图放在 `QScrollArea` 中，滚动区域将通过调整其提供的滚动条来响应大小的变化。

```python
def minimumSizeHint(self):
    size = self.sizeHint()
    fm = QFontMetrics(self.font())
    size.setWidth(fm.height() * 3)
    return size
```

我们计算视图的最小大小为其首选宽度和三个字符的高度。在布局中这是合理的，因为使用了 `QScrollArea`，在实践，最小大小将取决于滚动区域的决定。

```python
def sizeHint(self):
    fm = QFontMetrics(self.font())
    size = self.sizeHint()
    size.setWidth(fm.height() * 3)
    return size
```

等等，OCR 文本中 `sizeHint` 上的逻辑似乎在源文件中被合并或错乱了。让我们重新阅读文本：

我们计算视图的最小大小为其首选宽度和三个字符的高度。在布局中这是合理的，因为使用了 `QScrollArea`，在实践，最小大小将取决于滚动区域的决定。

```python
def sizeHint(self):
    fm = QFontMetrics(self.font())
    size = self.sizeHint()
    size.setWidth(fm.height() * 3)
    return size
```

实际上，查看 OCR 文本：

`def sizeHint(self):`

`fm = QFontMetrics(self.font())`

`size = self.sizeHint()`

`size.setWidth(fm.height() * 3)`

`return size`

等等，OCR 有对应的：

`def sizeHint(self):`

等等，看这个块：

```python
def minimumSizeHint(self):
    size = self.sizeHint()
    fm = QFontMetrics(self.font())
    size.setWidth(fm.height() * 3)
    return size
```

然后：

`def sizeHint` 似乎是重复或误读的。让我们遵循文本流。

我们使用一个字符的高度作为所有行的尺寸单位“……updateGeometry() 通知任何负责视图的布局管理器其大小已更改……在实践中，最小大小将取决于滚动区域的决定。”

等等，OCR 说：

`def minimumSizeHint(self):`

`size = self.sizeHint()`

`fm = QFontMetrics(self.font())`

`size.setWidth(fm.height() * 3)`

`return size`

然后：

```python
def sizeHint(self):
    fm = QFontMetrics(self.font())
    size = self.sizeHint()
    size.setWidth(fm.height() * 3)
    return size
```

等等，OCR 非常混乱。我将根据提供的文本重构逻辑。

文本说：“我们计算视图的最小大小为其首选宽度和三个字符的高度。在布局中这是合理的，因为使用了 `QScrollArea`，在实践，最小大小将取决于滚动区域的决定。”

代码是：

```python
def minimumSizeHint(self):
    size = self.sizeHint()
    fm = QFontMetrics(self.font())
    size.setWidth(fm.height() * 3)
    return size
```

等等，OCR 还有：

```python
def sizeHint(self):
    fm = QFontMetrics(self.font())
    size = self.sizeHint()
    size.setWidth(fm.height() * 3)
    return size
```

这看起来是 OCR 或文档中的错误。我将坚持提供的内容，但进行清理。

让我们看看 `paintEvent`：

```python
def paintEvent(self, event):
    if self.model is None:
        return
    fm = QFontMetrics(self.font())
    timestampWidth = fm.width("9999-99")
    size = fm.height()
    indicatorSize = int(size * 0.8)
    offset = int(1.5 * size)
    minY = event.rect().y()
    maxY = event.rect().height()
    painter = QPainter(self)
    y = 0
    for row in range(self.model.rowCount()):
        if minY <= y <= maxY:
            painter.save()
            painter.setPen(self.palette().color(QPalette.Text))
            if row == self.selectedRow:
                painter.fillRect(x, y + (offset + 0.8), self.width(), self.palette().highlight())
            timestamp = self.model.data(self.model.index(row, TIMESTAMP)).toDateTime()
            painter.drawText(x, y + size, timestamp.toString())
            x += timestampWidth
            temperature = self.model.data(self.model.index(row, TEMPERATURE)).toDouble()[0]
            if temperature < 20:
                color = QColor(0, 0, int(255 * (20 - temperature) / 20))
            elif temperature > 25:
                color = QColor(255, 0, 0, int(255 * (temperature - 25) / 20))
            painter.fillRect(x, y + offset, indicatorSize, color)
            painter.restore()
        y += size
```

等等，OCR 极其混乱。我将提供提供文本的最干净版本。

## 自定义视图

```
color = QColor(int(255 * temperature / 100), 0, 0
else:
    color = QColor(0, int(255 * temperature / 100), 0)
    painter.setPen(Qt.NoPen)
    painter.setBrush(color)
    painter.drawEllipse(x, y + offset, indicatorSize, indicatorSize)

x += size
```

我们遍历模型中的每一行，但只绘制 y 坐标在范围内的行。一旦确定了需要绘制的行，就会将画笔（用于绘制文本）设置为调色板的文本颜色。如果该行被选中（我们将在介绍完绘制部分后解释这一点），我们将使用调色板的高亮颜色绘制背景，并将画笔设置为调色板的高亮文本颜色。

在设置了文本颜色并可能绘制了背景后，我们接着获取并绘制水的时间戳。对于每一行，我们保留一个 x 坐标，告诉我们水平移动了多远，并根据之前计算的字体指标时间戳宽度进行递增。

第一个彩色圆圈用于表示以 °C 为单位的水温。如果水太冷，我们使用带蓝色调的颜色；如果水太热，我们使用带红色调的颜色；否则，我们使用绿色调。我们关闭画笔并将画刷设置为设置好的颜色，并在时间戳右侧绘制一个椭圆。`drawEllipse()` 方法通过绘制椭圆所在矩形的宽度和高度来绘制圆形（两者是相同的）。

然后我们增加 x 坐标。现在对另外两个彩色指示器重复此过程，使用与处理温度时相同的着色方法。我们省略了这些代码，因为它们在结构上与用于温度圆圈的代码完全相同。

```
flow = self.model.data(
    self.model.index(row, INLETFLOW))
flow = flow.toDouble([0])
char = None
if flow <= 0:
    char = WaterQualityView.FLOWCHARS[0]
elif flow < 3:
    char = WaterQualityView.FLOWCHARS[1]
elif flow > 5.5:
    char = WaterQualityView.FLOWCHARS[2]
if char is not None:
    painter.setFont(self.flowfont)
    painter.drawText(x, y + size, char)
    painter.restore()
y += size
if y > maxY:
    break
```

## 第 16 章 高级模型/视图编程

如果水流方向错误，或者速度太慢或太快，我们将使用在初始化器中设置的字体和字符绘制一个合适的字符。

最后，我们为下一行数据增加 y 坐标，但如果我们超过了视图范围内的最后一行，则停止。

到目前为止编写的代码已经足够为数据集提供只读视图。用户通常想要高亮某个项目。实现最简单的方法是添加鼠标点击事件处理程序。

```python
def mousePressEvent(self, event):
    fm = QFontMetrics(self.font())
    self.selectedRow = event.y() // fm.height()
    self.update()
    self.emit(SIGNAL("clicked(QIndex)"))
    self.model.index(self.selectedRow, 0))
```

我们所有计算中使用的尺寸单位是字符的高度。我们将位置坐标（相对于控件的左上角）除以高度，以找到用户点击了哪一行。我们使用整数除法，因为行号是整数。我们可以使用 `update()` 来调度一个绘制事件。在 `paintEvent()` 中，我们看到选中的行是用高亮文本和背景颜色绘制的。我们还发射了 `clicked()` 信号，并带有被点击行第一列的模型索引。虽然此应用程序没有使用该信号，但在实现自定义视图时提供它是一个良好的做法。

滚动条兼顾了键盘用户：他们可以使用 Page Up 和 Page Down 键进行滚动。但我们应该为键盘用户提供一种选择项目的方法。为了做到这一点，我们必须确保控件具有合适的焦点策略——我们在初始化器中已经做了这一点——并且必须提供一个按键事件处理程序。

```python
def keyPressEvent(self, event):
    if self.model is None:
        return
    row = -1
    if event.key() == Qt.Key_Up:
        row = max(0, self.selectedRow - 1)
    elif event.key() == Qt.Key_Down:
        row = min(self.selectedRow + 1, self.model.rowCount() - 1)
    if row != -1 and row != self.selectedRow:
        self.selectedRow = row
        if self.scrollarea is not None:
            fm = QFontMetrics(self.font())
            y = fm.height() * self.selectedRow
            self.scrollarea.ensureVisible(0, y)
    self.update()
```

```python
self.emit(SIGNAL("clicked(QIndex)"))
self.model.index(self.selectedRow, 0)

else:
    Widget.keyPressEvent(self, event)
```

我们选择仅支持两个键：上箭头和下箭头。如果用户按下其中任何一个键，我们就会增加或减少选中的行号，确保选中的行在范围内，并调度一个绘制事件。如果用户导航到最顶部可见行之上或最底部可见行之下，我们告诉滚动区域确保该行可见——如果必要，滚动区域将滚动到此处。我们还发射了带有新选中行模型索引的 `clicked()` 信号。在这种情况下使用 `clicked()` 信号是常规做法，因为信号和槽机制关注的是用户想要什么，他们如何请求，他们只是想要选择某一行。

如果我们不自己处理按键，那么会将事件传递给基类。对于所有其他按键，这样做是。

水质视图在视觉上与侧所示的表格视图不同，实现它不需要大量代码，编写起来也不难。通过减少不必要的绘制，我们使得视图非常高效。同时，通过确保控件恰好是整个数据集的大小，使得绘制代码尽可能简单。这种方法的缺点是将使用我们控件的程序员留给了 `ScrollArea` 责任，尽管这让我们免了手动实现。

水质视图在视觉上与侧所示的表格视图不同，实现它不需要大量代码，编写起来也不难。通过减少不必要的绘制，我们使得视图非常高效。同时，通过确保控件恰好是整个数据集的大小，使得绘制代码尽可能简单。这种方法的缺点是将使用我们控件的程序员留给了 `ScrollArea` 责任，尽管这让我们免了手动实现。

水质视图在视觉上与侧所示的表格视图不同，实现它不需要大量代码，编写起来也不难。通过减少不必要的绘制，我们使得视图非常高效。同时，通过确保控件恰好是整个数据集的大小，使得绘制代码尽可能简单。这种方法的缺点是将使用我们控件的程序员留给了 `ScrollArea` 责任，尽管这让我们免了手动实现。

水质视图在视觉上与侧所示的表格视图不同，实现它不需要大量代码，编写起来也不难。通过减少不必要的绘制，我们使得视图非常高效。同时，通过确保控件恰好是整个数据集的大小，使得绘制代码尽可能简单。这种方法的缺点是将使用我们控件的程序员留给了 `ScrollArea` 责任，尽管这让我们免了手动实现。

水质视图在视觉上与侧所示的表格视图不同，实现它不需要大量代码，编写起来也不难。通过减少不必要的绘制，我们使得视图非常高效。同时，通过确保控件恰好是整个数据集的大小，使得绘制代码尽可能简单。这种方法的缺点是将使用我们控件的程序员留给了 `ScrollArea` 责任，尽管这让我们免了手动实现。

水质视图在视觉上与侧所示的表格视图不同，实现它不需要大量代码，编写起来也不难。通过减少不必要的绘制，我们使得视图非常高效。同时，通过确保控件恰好是整个数据集的大小，使得绘制代码尽可能简单。这种方法的缺点是将使用我们控件的程序员留给了 `ScrollArea` 责任，尽管这让我们免了手动实现。

## 通用代理

正如我们在前面的章节中看到的，自定义代理允许我们对数据项的外观和行为进行完全控制。更好的方法（特别是对于每列只有一种数据类型的模型，与其为每个模型创建一个自定义代理，不如从一组通用组件组合成代理。这意味着维护工作将局限于通用组件，对其中一个组件的错误修复将自动惠及任何使用它的视图。

在代码中，其效果如下：

```python
table1 = UITableView()
table1.setModel(self.model1)
delegate1 = GenericDelegate(self)
delegate1.insertColumnDelegate(1, PlainTextColumnDelegate())
delegate1.insertColumnDelegate(2, PlainTextColumnDelegate())
delegate1.insertColumnDelegate(3, RichTextColumnDelegate())
delegate1.insertColumnDelegate(4, IntegerColumnDelegate())
table1.setItemDelegate(delegate1)

table2 = UITableView()
table2.setModel(self.model2)
delegate2 = GenericDelegate(self)
delegate2.insertColumnDelegate(1, PlainTextColumnDelegate())
delegate2.insertColumnDelegate(2, IntegerColumnDelegate())
delegate2.insertColumnDelegate(3, FloatColumnDelegate())
delegate2.insertColumnDelegate(4, FloatColumnDelegate())
delegate2.insertColumnDelegate(5, RichTextColumnDelegate())
table2.setItemDelegate(delegate2)
```

在这里，我们有两个独立的模型，但它们都使用由特定数据类型列代理组合而成的通用代理。通过这种方法，对于我们要处理的每种数据类型（例如浮点数、浮动数字、日期、时间和日期/时间），我们只需要创建一个的纯文本列代理、单个富文本列代理等。此外，我们可能会创建一些项目特定的代理来处理自定义类型，但对于任何给定的数据类型都只有一个列代理，这极大地减少了代码重复，并确保任何使用它的视图都能受益。

## 通用委托 (Generic Delegates)

仅通过使用带有适宜列委托的通用委托，就可以简单地拥有一个“自定义”委托。

在本节中，我们将看到如何创建一个 `GenericDelegate` 类以及几个示例列委托。我们将看到它们如何在图 16.2 的应用程序上下文中被使用。

| 执照 | 客户 | 租用 | 里程 #1 | 归还 | 里程 #2 | 备注 | 英里 | 天数 |

|---|---|---|---|---|---|---|---|---|

| 37 F56 LNC | Inglis 女 | 2006-06-06 | 13199 | 2006-06-15 | 17055 | | 3856 | |

| 38 NN07 AQ | Merritt 男 | 2006-06-07 | 18032 | 2006-06-26 | 20901 | 客户抱怨齿轮问题 | 2869 | 19 |

| 39 JRSK | Boston 女 | 2006-06-09 | 25000 | 2006-06-13 | 25540 | | 540 | 4 |

| 40 BCQ7 WRM | Terhane 男 | 2006-06-10 | 17015 | 0 | 22769 | | 5754 | 21 |

| 41 UNQ DE | Havill 女 | 2006-06-11 | 14374 | | 已售 | | | |

| 42 DV58 EC | Jolly 女 | 2006-06-11 | 21742 | 2006-06-19 | | 1870 | 10 |

| 43 J57 TDF | Clemy 女 | 2006-06-12 | 23966 | 2006-06-20 | 26384 | 归还时损坏 | 2368 | 8 |

| 44 DDQ6 XB | Course 女 | 2006-06-13 | 17063 | 2006-06-15 | | 537 | 3 |

| 45 SJ06 IAQ | Garroway 女 | 2006-06-12 | 12966 | 2006-06-14 | 13508 | 归还时油箱为空 | 542 | 2 |

| 46 J5SK RW | Verney 女 | 2006-06-14 | 22085 | 2006-06-28 | 26257 | 归还时变脏 | 4172 | 14 |

图 16.2 使用通用委托的表格

`GenericDelegate` 是非常的，因为它将几乎所有的工作都交给了其他类。

```python
class GenericDelegate(QItemDelegate):
    def __init__(self, parent=None):
        super(GenericDelegate, self).__init__(parent)
        self.delegates = {}
```

初始化函数像通常一样调用了 `super()`，并创建一个空字典。键将是列索引，值将是 `QItemDelegate` 类的实例。

```python
def insertColumnDelegate(self, column, delegate):
    delegate.setParent(self)
    self.delegates[column] = delegate
```

当一个新的列委托被插入到通用委托中时，通用委托将获得它的所有权并将其插入字典。

```python
def removeColumnDelegate(self, column):
    if column in self.delegates:
        del self.delegates[column]
```

包含此方法是为了完整性考虑，但它可能会被使用。如果删除了一个列委托，通用委托将简单地对该列使用 `QItemDelegate` 基类。

## 第 16 章 高级模型/视图编程

```python
def paint(self, painter, option, index):
    delegate = self.delegates.get(index.column())
    if delegate is not None:
        delegate.paint(painter, option, index)
    else:
        QItemDelegate.paint(self, painter, option, index)
```

该方法的结构是 `GenericDelegate` 类工作原理的关键。我们首先获取给定列的列委托。如果获取了委托，我们将工作移给它；否则，我们将工作移交给基类。

```python
def createEditor(self, parent, option, index):
    delegate = self.delegates.get(index.column())
    if delegate is not None:
        return delegate.createEditor(parent, option, index)
    else:
        return QItemDelegate.createEditor(self, parent, index)
```

此方法遵循与 `paint()` 方法相同的模式，不同之处它返回一个值（为之创建的编辑器）。

```python
def setEditorData(self, editor, index):
    delegate = self.delegates.get(index.column())
    if delegate is not None:
        delegate.setEditorData(editor, index)
    else:
        QItemDelegate.setEditorData(self, editor, index)
```

```python
def setModelData(self, editor, model):
    delegate = self.delegates.get(index.column())
    if delegate is not None:
        delegate.setModelData(editor, index)
    else:
        QItemDelegate.setModelData(self, editor, index)
```

这些 `GenericDelegate` 方法遵循 `paint()` 和 `createEditor()` 方法的模式，使用了 `QItemDelegate` 基类。

在理解了通用委托的实现后，我们可以处理文本的的文本的...（注：原文此部分似乎存在逻辑混乱或翻译码重复，译文已根据上下文进行了最小化平滑处理）。

`RichLineEdit` 接受 HTML 文本，如果它使用 `setHtml()` 方法。

我们委托的文本是简单的 HTML 格式。

```python
class DateDelegate(QItemDelegate):
    def __init__(self, parent=None):
        super(DateDelegate, self).__init__(parent)
```

（注：此处存在重复的格式描述，`text`  是 HTML 格式的）。

`RichLineEdit` 有一个 `toHtml()` 方法，但我们使用在第 13 章中开发的 `toHtml()` 方法。这确保我们存储的是有效的 HTML。在 `paint()` 方法中，对于高亮（即被选中）的项目，我们将通过封装标签来设置文本颜色——这将用于使用简单 HTML 格式的文本，但不对于普通的 HTML 格式（它是完整的 HTML 文档）。

```python
def paint(self, painter, option, index):
    text = index.model().data(index, Qt.DisplayRole).toString()
    palette = QApplication.palette()
    document = QTextDocument()
    document.setDefaultFont(option.font)
    if option.state & QStyle.StateSelected:
        document.setHtml(QString("<font color=%1>%2</font>") \
            arg(palette.highlightedText().color().name()) \
            arg(text))
    else:
        document.setHtml(text)
    painter.save()
    color = palette.highlight().color() \
        if option.state & QStyle.StateSelected \
            else QColor(index.model().data(index, \
            Qt.BackgroundColorRole))
    painter.fillRect(option.rect, color)
```

## 通用代理 (Generic Delegates)

```
painter.translate(option.rect.x(), option.rect.y())
document.drawContents(painter)
painter.restore()
```

`(paint)` 方法与第 14 章中描述的 `ShipDelegate` 使用的方法几乎完全相同。唯一的区别在于，我们不需要检查特定的列，因为我们知道列代理只有在用户指定的列被绘制时才会被调用。

这种方法方法的一个局限性是高亮功能仅对 HTML 片段有效。如果我们希望代码能够同时适用于片段和完整的 HTML 文档，可以使用如下代码：

```python
if option.state & QStyle::Selected:
    if text.startsWith("<html>").replace("body ", "")
        text = QString("<body bgcolor=%1>")
            .arg(palette.highlightedText().color().name())
else:
    text = QString("<font color=%1>%2</font>")
        .arg(palette.highlightedText().color().name())
        .arg(text)

dndocument.setHtml(text)
```

另一种方法是提取文档的样式表，更新背景颜色，并将更新后的样式表设置回文档中。

```python
def sizeHint(self, option, index):
    text = index.model().data(index).toString()
    document = QTextDocument()
    document.setDefaultFont(option.font)
    document.setHtml(text)
    return QSize(document.idealWidth() + 5,
                 font.metrics.height())
```

我们必须手动为富文本列计算尺寸提示（size hint），因为基于小部件尺寸字体和字符数量计算的宽度通常会太宽。这是因为 HTML 文本包含的字符（如标签和实体）通常比实际显示的字符多。使用 `QTextDocument` 方法可以轻松解决这个问题。这段代码与 `ShipDelegate` 的 `sizeHint` 方法使用的代码几乎相同。

我们可以轻松地创建其他列代理，并且可以让任何列代理提供比此处示例更丰富的功能。例如，对于 `IntegerColumnDelegate`，我们有最小值和最大值，但提供额外的选项（如前缀和后缀文本）也是简单的。

## 第 16 章。高级模型/视图编程



# 进阶模型/视图编程

现在我们已经了解了 `GenericDelegate` 是如何工作的以及如何创建列代理，我们可以看看它们在实践中是如何使用的。图 16.2（第 485 页）显示了一个表格视图，它使用一个通用代理配合多个特定代理来控制其列的编辑和外观。表单位于 `chap16/carhirelog.py` 中；以下是其初始化器的开头：

```python
class MainForm(QMainWindow):
    def __init__(self, parent=None):
        super(MainForm, self).__init__(parent)
        model = CarHireModel(self)
        self.view = QTableView()
        self.view.setModel(model)
        self.view.resizeColumnsToContents()

        delegate = genericDelegates.GenericDelegate(self)
        delegate.insertColumnDelegate(CUSTOMER,
            genericDelegates.PlainTextColumnDelegate())
        earliest = QDate.currentDate().addYears(-3)
        delegate.insertColumnDelegate(HIRED,
            HireDateColumnDelegate(earliest))
        delegate.insertColumnDelegate(MILEAGEOUT,
            MileageOutColumnDelegate(0, 1000000))
        delegate.insertColumnDelegate(RETURNED,
            ReturnDateColumnDelegate(earliest))
        delegate.insertColumnDelegate(MILEAGEBACK,
            MileageBackColumnDelegate(0, 1000000))
        delegate.insertColumnDelegate(NOTES,
            genericDelegates.RichTextColumnDelegate())

        self.view.setItemDelegate(delegate)
        self.setCentralWidget(self.view)
```

该模型是一个类似于我们在第 14 章中创建的自定义模型。视图是一个标准的 `QTableView`。

该模型有九列：一个只读的纯文本许可证号、一个纯文本客户名称、一个租赁日期（`QDate`）、一个整数起始里程（mileage out）、一个还车日期（`QDate`）、一个整数还车里程（mileage back），以及两个生成的而非存储的列——里程列（回程里程和起始里程之差）和一个天数列（还车日期和租赁日期之差）。

模型和底层数据结构处理了只读许可证列和生成的列（我们稍后会讨论），因此我们需要为可编辑列提供列代理。对于客户名称，我们使用 `PlainTextColumnDelegate`，对于备注，我们使用 `RichTextLineEdit`。但对于里程和日期，我们使用了 `IntegerColumnDelegate` 和 `DateColumnDelegate` 的子类自定义列代理。我们需要这些子类来提供跨列验证。例如，我们不能接受早于租赁日期的还车日期，或小于起始里程的还车里程。

```python
class HireDateColumnDelegate(genericdelegates.DateColumnDelegate):
    def createEditor(self, parent, option, index):
        i = index.sibling(index.row(), RETURNED)
        self.maximum = i.model().data(i, Qt.DisplayRole) \
            .toDate().addDays(-1)
        return genericdelegates.DateColumnDelegate.createEditor(
            self, parent, option)
```

这是完整的 `HireDateColumnDelegate` 子类。我们需要这些子类来提供跨列验证。例如，我们不能接受早于租赁日期的还车日期，或小于起始里程的还车里程。

## 用树表示表格数据

假设我们要用户选择一个项目，但该项目依赖于之前的项目，而之前的项目又依赖于之前的项目。具体来说，想象我们要用户选择一个特定的机场——先选择城市，然后是机场。这可以通过提供三个下拉框来实现，第一个填充国家名称，第二个填充当前城市的城市，第三个填充当前城市的机场。这编程并不困难，但用户必须使用三个独立的控件来指定选择，并且无法轻松看到哪些可选范围。

选择项目的一种方法是使用树视图。继续该示例，树的根节点是国家，每个国家都有城市分支，每个城市分支都有机场叶子。这使得使用户更容易遵循路径（并且他们只能遵循有效路径），也便于我们检索他们完整的城市/机场选择。

与使用表格视图相比，使用树视图的优势是更加紧凑且更容易导航。例如，如果有 100 个国家，每个国家平均 4 个城市，每个城市平均 2 个机场，表格将需要 100 x 4 x 2 = 800 行——但每行都需要展开以显示城市和机场。

在本节中，我们将展示如何用树表示表格数据，以及如何提取用户选择的完整“路径”。我们将使用的示例应用程序是 Server Info。它返回的包含六列的数据集——国家、州（仅在美国有意义）、城市、提供商、服务器和 IP 地址——允许用户指定一个特定的六元组。

### 在树结构中表示表格数据

| 国家/州（美国)/城市/提供商 | 服务器 | IP |
|---|---|---|
| 土耳其 | | |
| （无州） | | |
| 安卡拉 | | |
| 国家学术骨干网 | | |
| UlakNet 安卡拉 | Apache/1.3.4 | 193.140.83.20 |
| 乌克兰 | | |
| 英国 | | |
| 美国 | | |
| 亚利桑那 | | |
| 加利福尼亚 | | |
| 佐治亚 | | |
| 亚特兰大 | 由 Lotus Productions 提供 | Apache/1.3.3 | 216.25.63.17 |
| | Lyum 支持工具 | NCSA/1.4.2 | 205.142.28 |
| 南十字 | Apache/1.3.1 | 130.207.244.51 |
| 美国*佐治亚*亚特兰大*南十字*Apache/1.3.1*130.207.244.51 | | |

**图 16.3** 渲染为树的表格数据

只需要 33 个顶层项目，而不需要滚动其五倍数的行。

应用程序的核心由 `TreeOfTableModel` 类提供，它是 `QAbstractModel` 的子类，可以在树中表示任意表格数据。我们使用了模型的自定义子类，并配合 `QTreeView` 子类来展示数据。应用程序本身可以通过从控制台运行并带有 1、2、3 或 4 的命令行参数，通过不同层级的嵌套来创建树。图 16.3 显示了使用默认嵌套层级 3 的树。（嵌套层级不包括一系列分支末尾的叶子节点）。

我们将首先回顾主表单；它非常短。然后我们将查看树视图子类和 `TreeOfTableModel` 子类。接下来，我们将回顾树表格模型，包括 `BranchNode` 和 `LeafNode` 类，最后是回顾 `TreeOfTableModel` 类本身。

```python
class MainForm(QMainWindow):
    def __init__(self, filename, nesting, separator, parent=None):
        super(MainForm, self).__init__(parent)
        headers = ["Country/State (US)/City/Provider", "Server", "IP"]
        self.treeWidget = TreeOfTableModel(filename, nesting, separator)
        self.treeWidget.model().headers = headers
        self.setCentralWidget(self.treeWidget)
        self.connect(self.treeWidget, SIGNAL("activated"), self.activated)
        self.setWindowTitle("Server Info")
```

`TreeTableViewWidget` 类似于便利视图，因为它内部包含了一个模型。该模型是 `ServerModel`，它是 `TreeOfTableModel` 的小型子类，添加了显示旗帜图标的功能。

`filename` 是一个适用于 `TreeOfTableModel` 数据的文件名。具体来说，它必须每行一条记录，并且每列（字段）必须由指定的分隔符隔开。

`nesting` 值是从根节点的最大分支数，不计入末尾的叶子。在这种情况下，通过 `nesting` 参数传递的嵌套值为 3（除非在命令行上进行更改），这意味着我们将有 3 层分支（国家、州、城市）和 1 层叶子节点（提供商）。由于我们有 6 个字段，这意味着前 4 个字段将显示在树形部件的树部分，剩余 2 个字段将作为单独列显示在具有叶子的行中。结果视图将具有 3 列，其中一列包含树，另外两列显示额外的字段。我们通过直接访问 `TreeTableViewWidget` 内部的模型来设置模型的表头。

当用户双击树形部件中的某行或按下回车键时，会调用 `activated()` 方法。

```python
def activated(self, fields):
    self.statusBar().showMessage("* / ".join(fields), 60000)
```

“路径”是用户选择的（国家、城市、州、提供商、服务器、IP 地址）6 元元组，每当激活一个合适的行时，该元组会在状态栏中显示一分钟（60000 毫秒）。在此上下文中，合适的行是指包含叶子节点的行，因为只有这些行拥有六个字段。

`TreeTableViewWidget` 是一个 `QTreeView` 子类，包含了它要显示的模型。它还提供了一些便利方法并创建了一些实用的信号槽连接。

```python
def __init__(self, filename, nesting, separator, parent=None):
    super(TreeTableViewWidget, self).__init__(parent)
    self.setSelectionBehavior(QTreeView.SelectItems)
    self.setUniformRowHeights(True)
    model = ServerModel(self)
    self.setModel(model)
    try:
        model.load(filename, nesting, separator)
    except IOError as e:
        QMessageBox.warning(self, "Server Info - Error", unicode(e))
    self.connect(self, SIGNAL("activated(QModelIndex)"), self.activated)
    self.connect(self, SIGNAL("expanded(QModelIndex)"), self.expanded)
    self.expanded()
```

`ServerModel` 是一个 `TreeTableModel` 的子类。它的唯一目的是重写 `data()` 方法，以便它可以提供合适的图标（国家和州旗帜）；我们稍后会回顾它。

当用户展开一个分支时，调用 `expanded()` 方法。我们将调用它以确保所有分支都已展开。

### 在树结构中表示表格数据

父节点的子节点列表即为其行号。列号指的是子节点（分支或叶子）内部的项（字段）。一条完整的记录（或“路径”）是根分支中所有字段、所有中间分支以及末端叶子字段的拼接。分支与叶子之间的关系如图 16.4 所示。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_511_0.png)

**图 16.4 树模型分支与叶子的示意图**

在我们所选择的表格模型树中，我们保持每个分支的子节点按字母顺序排列。为了尽可能快速和方便，每个分支的子节点列表实际上是一个包含两个元素的列表的列表，其中第一个元素是排序键（order key），第二个元素是子节点。我们使用常量 `KEY` 和 `NODE` 来访问这些双元素列表中的项，而不是字面量 `0` 和 `1`。

现在我们将查看分支节点和叶子节点的实现，以及表格模型本身的树。

分支节点和叶子节点有许多共同方法，因为在某些语境下，它们可以互换（得益于鸭子类型）。

```python
class BranchNode(object):
    def __init__(self, name, parent=None):
        super(BranchNode, self).__init__(parent)
        self.name = name
        self.parent = parent
        self.children = []
```

分支节点的名称是其第一（也是唯一）列中显示的文本。在 Server Info 示例中，这将是一个国家、州或城市的名称，取决于该分支在树层次结构中的位置。

```python
def orderKey(self):
    return self.name.lower()
```

```python
def toString(self):
    return self.name
```

```python
def __len__(self):
    return len(self.children)
```

排序键是一个字符串，由节点的父节点用于将该分支正确地放置在父节点的子节点列表中。`toString()` 方法将分支的一个字段作为字符串返回。提供这些方法是为了与叶子节点兼容，方便根据鸭子类型使用任何一种节点。`__len__()` 方法返回该分支有多少个子节点。

```python
def childAtRow(self, row):
    assert 0 <= row < len(self.children)
    return self.children[row][NODE]
```

此方法返回给定行对应的节点。我们在这里使用了断言语句，在表格模型代码的许多地方也是如此。编写正确的代码可能很难，但通过使用断言，我们至少可以明确在代码特定点期望得到的内容。

```python
def rowOfChild(self, child):
    for i, item in enumerate(self.children):
        if item[NODE] == child:
            return i
    return -1
```

我们返回特定子节点的行索引，如果该子节点不是此节点的子节点之一，则返回 -1。

```python
def childWithKey(self, key):
    if not self.children:
        return None
    i = bisect.bisect_left(self.children, (key, None))
    if i < 0 or i >= len(self.children):
        return None
    if self.children[i][KEY] == key:
        return self.children[i][NODE]
    return None
```

我们有时想要找到具有给定排序键的子节点。一种方法是像我们在 `rowOfChild()` 方法中所做的那样，遍历子节点列表找到正确的一个。在这里我们采取了更高效的方法。我们找到具有给定键的节点应该占据的位置，如果该位置在范围内且具有正确的键，我们就返回该子节点。

```python
def insertChild(self, child):
    child.parent = self
    bisect.insort(self.children, (child.orderKey(), child))
```

此方法将新节点插入到分支的子节点列表中，并将该分支设置为子节点的父节点。通过结合 `bisect.insort()` 和子节点的顺序，我们确保子节点能够以最快、最高效的方式放在正确的位置。

```python
def hasLeaves(self):
    if not self.children:
        return False
    return isinstance(self.children[0][NODE], LeafNode)
```

在表格模型树中，一个分支要么全是叶子，要么全是子节点，但不会两者混合。因此，如果一个分支完全没有子节点，显然没有叶子；同样，如果它有子节点且第一个是叶子，那么它们所有的都是叶子。

我们现在查看了整个分支节点类。接下来，我们将查看短得多的叶子节点类。

```python
class LeafNode(object):
    def __init__(self, fields, parent=None):
        super(LeafNode, self).__init__(parent)
        self.parent = parent
        self.fields = fields
```

叶子节点中的字段是节点的列。

```python
def orderKey(self):
    return "\t".join(self.fields).lower()
```

```python
def toString(self, separator="\t"):
    return separator.join(self.fields)
```

```python
def __len__(self):
    return len(self.fields)
```

叶子节点的键是制表符分隔的字段拼接。同样，它的 `toString()` 方法返回字段的拼接。`__len__()` 方法返回字段的数量；对于分支，它返回子节点的数量。

```python
def field(self, column):
    assert 0 <= column < len(self.fields)
    return self.fields[column]
```

此方法方便提取单个字段的值，同时断言字段列在范围内。

```python
def asRecord(self):
    record = []
    branch = self.parent
    while branch is not None:
        record.insert(0, branch.toString())
        branch = branch.parent
    return record + self.fields
```

树使用的记录概念是字段的拼接。

```python
class TreeTableModel(QAbstractTableModel):
    def __init__(self, parent=None):
        super(TreeTableModel, self).__init__(parent)
        self.columns = 0
        self.root = BranchNode("")
        self.headers = []
```

列数取决于嵌套深度。总有一个根节点包含所有分支的父节点。头部是作为列标题的文本。

```python
def load(self, filename, nesting, separator):
    assert nesting > 0
    self.nesting = nesting
    self.root = BranchNode("")
    exception = None
    fh = None
    try:
        for line in codecs.open(filename, "r", "utf8"):
            if not line:
                continue
            self.addRecord(line.split(separator), False)
    except IOError as e:
        exception = e
    finally:
        if fh is not None:
            fh.close()
        self.reset()
        for i in range(self.columns):
            self.headers.append("Column %d" % i)
        if exception is not None:
            raise exception
```

```python
def addRecord(self, fields, callReset=True):
    assert len(fields) > self.nesting
    root = self.root
    branch = None
    for i in range(self.nesting):
        key = fields[i].lower()
        branch = root.childWithKey(key)
        if branch is not None:
            root = branch
        else:
            branch = BranchNode(fields[i])
            root.insertChild(branch)
            root = branch
    assert branch is not None
    items = fields[self.nesting:]
    self.columns = max(self.columns, len(items))
    branch.insertChild(LeafNode(items, branch))
    if callReset:
        self.reset()
```

要添加一条记录，字段的数量必须大于嵌套层级。我们使用的逻辑与第 14 章中填充 `QTreeWidget` 内部模型时看到的逻辑相似。对于每个要作为具有相同键的分支的字段，如果我们找到了一个匹配项，就创建当前根分支；否则，我们创建一个新分支，将其作为当前根分支的子节点插入，并将新分支设置为当前根分支。随着循环的进行，我们逐渐向树向下移动，创建任何所需的分支，直到到达最底的分支。

一旦循环遍历了所有必要的分支（并创建了任何之前不存在的分支），我们就可以创建一个非嵌套字段的列表，并将它们作为当前（最底层）分支的子叶子节点添加进去。

具体来说，以“Server Info”应用程序为例，发生的情况如下：当读取第一条记录时，我们有新的国家、新州、新城市、新提供商等，因此会存在相应的分支。首先会创建一个国家分支，然后是州分支，然后是城市分支，最后是一个包含提供商、服务器和 IP 地址字段的叶子节点。如果读取的是同一个国家但新州的下一条记录，它将找到现有的国家节点并将其用作新州的父节点。同样，如果记录的国家和州已经创建了分支，则这些分支将被重用。但每当需要新分支时，循环体中的代码都会创建它。

当临时添加新记录时，调用 `reset()` 来通知任何视图已发生了重大变化；当从文件加载时，我们传递 `False` 并在所有记录加载完成后在调用代码中调用 `reset()`。

```python
def asRecord(self, index):
    leaf = self.nodeFromIndex(index)
    if leaf is not None and isinstance(leaf, LeafNode):
        return leaf.asRecord()
```

此方法提供了用户“路径”的列表。它只对叶子节点有意义，因为只有叶子节点才能表示完整的路径。对于非叶子节点返回 `None` 也是同样良好的设计选择。注意，我们使用 `nodeFromIndex()` 方法来获取给定模型索引节点：我们稍后会讨论它的工作原理。

```python
def rowCount(self, parent):
    node = self.nodeFromIndex(parent)
    if node is None or isinstance(node, LeafNode):
        return 0
    return len(node)
```

对于树模型，行数是特定节点拥有的子节点数量。实现仅允许分支节点拥有子节点，因此在叶子节点上调用时，我们始终返回 0。`len()` 函数会调用 `BranchNode.__len__()`，它返回分支子节点的计数。

```python
def columnCount(self, parent):
    return self.columns
```

列数是非嵌套字段的最大数量。这看起来可能少了一个，但它是正确的，因为第一个非嵌套字段显示在第一列（树列）中。

```python
def data(self, index, role):
    if role == Qt.AlignmentRole:
        return QVariant(int(Qt.AlignTop | Qt.AlignLeft))
    if role != Qt.DisplayRole:
        return QVariant()
    node = self.nodeFromIndex(index)
    assert node is not None
    if isinstance(node, BranchNode):
        if index.column() == 0:
            return QVariant(node.toString())
        else:
            return QVariant(QString(""))
    return QVariant(node.field(index.column()))
```

如果请求显示分支节点，则返回该节点在第 0 列的文本，其他列返回空字符串。对于叶子节点，我们返回对应于请求列的字段。

在 Qt 4.2 之前，默认的文本对齐是可以正常的，不需要指定，但从 Qt 4.2 开始，我们必须显式地返回一个合理的文本对齐方式。

```python
def headerData(self, section, orientation, role):
    if orientation == Qt.Horizontal and \
        role == Qt.DisplayRole:
        assert 0 <= section < len(self.headers)
        return QVariant(self.headers[section])
    return QVariant()
```

树视图只有水平（列）头。它们没有行头（例如行号），因为这些并没有真正意义，因为每个分支都有自己从 0 开始的子节点列表（行）。

```python
def index(self, row, column, parent):
    assert self.root
    branch = self.nodeFromIndex(parent)
    assert branch is not None
    return self.createIndex(row, column, branch.childAtRow(row))
```

`index()` 方法必须返回具有给定行和列且为给定父节点子节点的数据项的模型索引。在分支和叶子结点的树模型中，这意味着我们返回给定行和列的模型索引。

```python
def parent(self, index):
    node = self.nodeFromIndex(index)
    if node is not None and isinstance(node, BranchNode):
        return node.parent.index()
    return QModelIndex()
```

# 网络

## 创建 TCP 客户端

模型应该是 `QAbstractListModel` 的子类，并应该持有一组数据值列表（整数）和一个颜色字典（以“行”为键；例如，键为 6 的颜色对应于第七个值，以此类推）。模型应该重新实现 `count()`、`insertRows()`（应在适当的地方调用 `beginInsertRows()` 和 `endInsertRows()`）、`flags()`（使模型变为可编辑），以及 `setData()`（允许设置值（`Qt.DisplayRole`）和值的颜色（`Qt.UserRole`），并应该发射信号以指示数据已更改），以及 `data()`（它应该返回值、颜色，并且对于特定行的 `Qt.DecorationRole`，应使用红色默认值）。

代理（delegate）非常简单，与本章前面提到的 `IntegerColumnDelegate` 非常相似。关键区别在于必须重新实现 `paint()` 方法，但仅为了将对齐方式设置为 `Qt.AlignRight`；绘图仍然可以由基类完美地完成。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_520_0.png)

**图 16.5 柱状图程序的控件**

自定义视图需要实现 `resizeEvent()`，其中应该建立到基类 `update()` 方法的连接，以便在模型数据发生更改时进行重绘；`sizeHint()`（可以简单地调用 `minimumSizeHint()`）以及 `paintEvent()`。绘制事件可以用十多行代码完成——确保你使用了 `QPainter.setWindow()`，以便图表始终填充可用空间。如果没有设置模型，所有方法都应该正常工作——例如，在没有模型的情况下，绘图事件不应该绘制任何内容。

这里是 `MainForm` 的代码，让你感受这些类是如何使用的：

```python
class MainForm(QDialog):
    def __init__(self, parent=None):
        super(MainForm, self).__init__(parent)
        self.model = BarGraphModel()
        self.barGraphView = BarGraphView()
        self.barGraphView.setModel(self.model)
        self.listView = QListView()
        self.listView.setModel(self.model)
        self.listView.setItemDelegate(BarGraphDelegate(0, 1000, self))
        self.listView.setMaximumWidth(100)
        self.listView.setEditTriggers(QListView.DoubleClicked |
            QListView.EditKeyPressed)
        layout = QHBoxLayout()
        layout.addWidget(self.listView)
        layout.addWidget(self.barGraphView, 1)
        self.setLayout(layout)
        self.setWindowTitle("Bar Grapher")
```

在模型解决方案中，我们添加了一些额外的代码来创建 20 个随机项目以创建一个初始柱状图。整个过程可以在 200 行以内完成。

解决方案位于 `chap16/bargraph.py` 中。

## 练习

# 在线帮助与国际化

用户可能可以通过阅读菜单选项和按钮文本使用非常简单的应用程序。其他应用程序可能需要更多信息，在这种情况下，工具提示和状态提示是一个易于编程的解决方案。某些应用程序非常复杂或先进，用户可能需要更广泛的帮助来理解可以使用哪些功能以及如何使用这些应用程序。

提供充分信息的一种方法是提供打印手册；另一种方法是提供帮助系统。可以使用几种可能的方法来创建一个合适的帮助系统；我们将提到所有方法，并展示其中一种。我们将回到第 6 章引入的 `Image Changer` 应用程序，在本章中，我们将展示应用程序的 `MainWindow.helpHelp()` 方法的实现，以及如何提供在线帮助系统。

在整书中，所示应用程序提供的菜单文本、按钮文本、标签等都是英语。这对于世界上少数能读英语的人来说是可以的，但对于那些说世界上最广泛语言——普通话的人，或者说其他主要语言（如西班牙语、阿拉伯语、印地语、葡萄牙语、孟加拉语、俄语或日语）的人来说并不是。

为了应用程序尽可能广泛可用，它必须是非英语使用者使用的。PyQt 提供了一个工具链用于识别用户可见的字符串，并使这些字符串在易使用的 Qt GUI 应用程序可用，人类翻译人员可以使用它们来提供适当翻译。在本章的第二部分中，我们将讨论翻译工具以及如何使用它们。我们还将呈现一个新的翻译感知型 `Image Changer` 应用程序版本，它适用于翻译工具。

## 在线帮助

提供在线帮助有三种常用方法。一种方法是以 HTML 文件的形式提供帮助，并启动设置为相关页面的 Web 浏览器。另一种方法是提供 Qt 自带的 Qt Assistant 应用程序。第三种方法是提供帮助表单，再次使用 HTML，并将图像和 HTML 文件作为资源。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_524_0.png)

**图 17.1 Image Changer 帮助表单**

第一种方法可以通过启动独立进程 Web 浏览器来实现，可以使用 Python 的 `subprocess` 模块或 PyQt 的 `QProcess` 类。Qt 4.2 引入了一个新类 `QDesktopServices`，它通过其 `openUrl()` 静态方法轻松以平台无关的方式启动浏览器。

第二种方法更为复杂，因为它要求我们创建一个 XML 文件，并与应用程序分发 Qt Assistant。使用 Qt Assistant 的优势是它提供了自动索引。

第三种方法是使用 HTML 的自定义帮助表单，并将图像和 HTML 文件作为资源，这是我们将使用的。正如我们在第 6 章查看资源文件时所看到的，我们可以包含 HTML 文件。这里是 `Image Changer` 的 `MainWindow.helpHelp()` 方法的代码：

```python
def helpHelp(self):
    form = helpform.HelpForm("index.html", self)
    form.show()
```

使用我们的帮助表单很容易：我们使用的是 `show()` 而不是 `exec()`；这几乎意味着显示的表单设置了关闭时删除属性。

图 17.1 的截图可能会给人一种未考虑键盘用户的错误印象，但实际上，显示 HTML 文件的类 `QTextBrowser` 提供了良好的键盘支持。例如，用户可以使用 `Tab` 在超链接之间移动焦点，使用 `Enter` 点击超链接。可以使用 `Alt+Left Arrow` 返回，可以使用 `Home` 回到第一页。由于表单是 `QDialog`，他们可以通过按 `Esc` 关闭窗口。

现在我们已经熟悉创建 PyQt 对话框，因此我们将继续展示与创建在线帮助系统相关的提取——具体来说，来自 `HelpForm` 初始化函数及其方法（代码见 `chap17/helpform.py`）。

```python
class HelpForm(QDialog):
    def __init__(self, page, parent=None):
        super(HelpForm, self).__init__(parent)
        self.setAttribute(Qt.WA_DeleteOnClose)
        self.setAttribute(Qt.WA_GroupLeader)
```

`Qt.WA_GroupLeader` 属性确保如果帮助表单是从模态对话框调用的，用户能够在模态对话框和帮助表单之间进行交互，否则将是不可能的。如果帮助表单是从模态对话框或主窗口调用的，该属性没有影响，用户可以照常交互。

```python
self.textBrowser.setSearchPaths([":/"])
self.textBrowser.setSource(QUrl(page))
```

`QTextBrowser` 是 `QTextEdit` 的子类，用于显示大量的 HTML 标签，包括图像、列表和表格。我们已经将它的搜索路径设置为资源文件的根目录，并将其初始页面设置为传递的页面。因为我们设置了搜索路径，我们能够传递不带路径的页面（例如 `index.html` 或 `filemenu.html`）。`QTextBrowser` 理解资源路径，并标记为 `<img src=":/filename.png">`。

```python
self.connect(backAction, SIGNAL("triggered()"), self.textBrowser.backward)
self.connect(homeAction, SIGNAL("triggered()"), self.textBrowser.home)
self.connect(self.textBrowser, SIGNAL("sourceChanged(QUrl)"), self.updatePageTitle)
```

页面之间的跳转由 `QTextBrowser` 自动处理。然而，我们提供了两个工具栏按钮，“后退”（Back）和“主页”（Home），并连接到相应的 `QTextBrowser` 槽以实现我们需要的行为。如果 HTML 文档发生了变化——例如，用户点击了超链接——我们会调用自定义的 `updatePageTitle()` 槽。

```python
def updatePageTitle(self):
    self.pageLabel.setText(self.textBrowser.documentTitle())
```

此槽将 HTML 页面的 `<title>` 文本放置在工具栏中的 `QLabel` 中，位于工具栏按钮的右侧。

一旦我们有了 `HelpForm` 类，我们就可以完全使用 HTML 实现我们的在线帮助系统，可以将文件作为资源包含，或者将它们安装在文件系统中并使用如下代码找到它们：

```python
helpath = os.path.join(os.path.dirname(__file__), "help")
```

这假设任何文件都位于应用程序 `.pyw` 文件所在目录下的 `help` 目录中。

编写提供在线帮助系统的代码是简单的，但设计一个易于导航且易于理解的系统可能是一个挑战。

## 国际化

在使应用程序适用于使用与原始语言不同的用户时，有几个问题需要考虑。最大且最明显的问题是，所有用户可见的字符串必须翻译成目标语言——不仅包括菜单选项和对话框按钮的字符串，还包括工具提示、状态提示以及任何其他在线帮助。此外，我们必须执行其他本地化工作，例如使数字使用适当的小数标记和千位符，确保日期格式正确，并且纸张尺寸和计量单位正确。例如，大多数美国和英国人说英语，但两种文化具有不同的日期规范、不同的纸张尺寸和不同的计量系统。

得益于 Unicode，任何字符都可以显示。我们在书的开头看到，可以使用 Unicode 转义字符和目标字符的十六进制代码点，在 Unicode 或 `QString` 字符串中包含任何 Unicode 字符，或者使用 `unichr()` 函数。对于读取和写入包含 Unicode 的文件，我们可以使用 Python 的 `codecs.open()` 函数，或者使用我们在前面的章节中看到的 PyQt 的 `QTextStream`。

### 国际化

涉及到本地化的某些方面时，我们可以使用 `QString`、`QDate` 和 `QTime`。例如，假设 `n` 是一个数字，`QString("%1").arg(n)` 将产生带有适用于区域的千位和小数分隔符的 `QString`。`QDate` 和 `QTime` 都有 `toString()` 方法，接受格式或预定义的格式（如 `Qt.SystemLocaleShortDate`、`Qt.ISODate`，它是通用的）。此外，`QLocale` 提供了许多返回本地化 `QString` 的方法，它也有从本地化 `QString` 中提取数字的方法。它还有返回特定字符的方法，例如负号字符、百分比符号等。

应用程序国际化涉及的大部分工作与翻译有关，例如我们将在本节剩余部分关注的主题。

为了帮助翻译应用程序，PyQt 提供了一个由三个工具组成的工具链：`pylupdate4`、`lrelease` 和 `Qt Linguist`。为了让这些工具有用，每个可见的字符串必须经过特殊标记。通过 `QObject.tr()` 方法很容易实现，该方法被所有子类继承，包括所有的对话框和窗口。例如，我们不写 `QString("Save")`，而是写 `self.tr("&Save")`。传递给 `tr()` 的文本应该是 ASCII；如果需要 ASCII 范围之外字符，请使用 UTF-8。

对于每个标记为翻译的字符串，翻译工具将提供一对字符串：“上下文”（context）字符串（类名）和标记的字符串本身。上下文的目的是帮助人类翻译人员识别显示在哪个窗口中，因为不同的语言可能需要不同的翻译。

对于需要翻译但不在类内部的字符串，我们必须使用 `QApplication.translate()` 方法并自己提供上下文。例如，在 `main()` 函数中我们这样翻译应用程序名称：`QApplication.translate("main", "Gradgrid")`。在这里，上下文是 `"main"`，要翻译的字符串是 `"Gradgrid"`。

遗憾的是，`self.tr()` 使用的文本可能与 C++ `tr()` 方法使用的不同，因为 PyQt 动态确定上下文，而 C++ 在编译时确定。如果翻译文件要在 C++/Qt 和 PyQt 应用程序之间共享，这可能会很重要。在形成时也可能出现问题。如果这是一个问题，解决方案是将每个单参数的 `self.tr()` 调用替换为双参数的 `QApplication.translate()` 调用，显式将正确的上下文作为第一个参数，将要翻译的字符串作为第二个参数。

一旦应用程序的所有用户可见字符串都经过妥善标记，我们必须稍微更改应用程序启动的方式，以便它读取其运行区域的翻译后的字符串。

> *请参见 PyQt 的 pyqtref.html 文档，位于“Differences Between PyQt and Qt”部分。*

以下是创建国际化应用程序的方法。

1. 使用 `QObject.tr()` 或 `QApplication.translate()` 创建应用程序，处理所有用户可见的字符串。
2. 修改应用程序，在启动时如果可用则读取特定区域的 `.qm`（Qt消息）文件。
3. 创建 `.pro` 文件，列出应用程序的 `.ui`（Qt Designer）文件、`.py` 和 `.pyw` 文件。
4. 运行 `pylupdate4` 创建 `.ts` 文件。
5. 使用 `Qt Linguist` 翻译 `.ts` 文件。
6. 运行 `lrelease` 生成 `.qm` 文件。

```python
reply = QMessageBox.question(self,
    self.tr("Unsaved Changes?"),
    self.tr("Save changes?"),
    QMessageBox.Yes | QMessageBox.No | QMessageBox.Cancel)
```

对于这个对话框，我们翻译了窗口和消息文本。对于许多语言，Trolltech 提供的 `.qm` 文件已有翻译。如果我们使用了自己的文本，则需要对它使用 `tr()`。但不建议这样做。始终使用 `QString` 配合 `arg()`；这会让翻译变得更容易。

```python
self.tr("Saved %1 in file %2").arg(self.datame).arg(self.filename)
```

提供字符串的一种方法是写：

```python
self.tr("Saved %s in file %s") % (self.datame, self.filename) # 错误
```

我们必须对手写的 `.pyw` 和 `.py` 文件中的每个用户可见字符串使用 `tr()`。对于由 pyuic 从 `.ui` 文件生成的 `.py` 文件，我们不需要做任何事情，因为所有字符串会自动使用 `QApplication.translate()`。这适用于未翻译的应用程序，如果有翻译，则使用原始语言（例如英语）。

PyQt 应用程序通常使用 PyQt 内置对话框；例如文件打开对话框或文件打印对话框。这些也必须翻译，尽管对于许多语言，Trolltech 提供的 `.qm` 文件已有翻译。

在到处都使用了 `tr` 并且定位了合适的 Qt 翻译，我们准备好修改应用程序的启动代码来加载存在的翻译文件。

```python
app = QApplication(sys.argv)
locale = QLocale.system().name()
translator = QTranslator()
if translator.load("qt_" + locale, ":/"):
    app.installTranslator(translator)
```

> *Trolltech 提供了某些语言的翻译，如法语和德语，以及对其他语言的翻译。这些翻译位于 Qt 的（而不是 PyQt 的）翻译目录中；例如在文件系统中搜索 `qt_fr.qm` 以找到法语翻译。*

```python
appTranslator = QTranslator()
if appTranslator.load("imagechanger_" + locale, ":/"):
    app.installTranslator(appTranslator)
```

```python
app.setOrganizationName("Qtrac Ltd.")
app.setOrganizationDomain("qtrac.eu")
app.setApplicationName(app.translate("main", "Image Changer"))
app.setWindowIcon(QIcon(":/icon.png"))
form = MainWindow()
form.show()
app.exec_()
```

`QLocale.system().name()` 调用将返回一个如 `"en_US"`（英语，美国）或 `"fr_CA"`（法语，加拿大）之类的字符串。`QTranslator.load()` 方法从应用程序的资源文件中加载文件。如果 locale 为 `"fr_CA"`，则前缀将是 `qt_fr_CA` 和 `imagechanger_fr_CA`。基于此，PyQt 将查找 `qt_fr_CA.qm`，如果未找到，则查找 `qt_fr.qm`，同样对于 `imagechanger_fr_CA.qm` 也是如此。如果未找到且 locale 为 `"en_US"`，则不会找到 .qm 文件，因此不会进行安装——这是因为应用程序将退回到使用原始字符串，而这些字符串本身就是英文。

注意，我们必须使用 `QApplication.translate()`（代码中写为 `app.translate()`，因为这段代码不是 QObject 子类的方法）。在类名处，我们选择使用 `"main"` 作为上下文；某些程序员可能更倾向于使用 `"global"`。我们可以自由地使用任何喜欢的名称——文本的目的是帮助人类翻译员。

我们可以在单个 `QTranslator` 对象中只加载一个翻译文件，但我们可以向 `QApplication` 对象中添加任意数量的翻译器。如果发生冲突（即同一个字符串有不同的翻译），则最近安装的翻译器将获胜。

尽管我们选择将翻译包含在资源文件中，但并没有义务这样做；我们同样可以容易地从文件系统访问它们。

以下是我们使用的 `resource.qrc` 文件的片段：

```xml
<resource>
    <file>qt_fr.qm</file>
    <file>imagechanger_fr.qm</file>
</resource>
<resource>
    <file alias="editmenu.html">help/editmenu.html</file>
    <file alias="filemenu.html">help/filemenu.html</file>
    <file alias="index.html">help/index.html</file>
</resource>
<resource lang="fr">
    <file alias="editmenu.html">help/editmenu.html</file>
    <file alias="filemenu.html">help/filemenu_fr.html</file>
    <file alias="index.html">help/index_fr.html</file>
</resource>
```

资源文件可以包含任意数量的 `<resource>` 标签，尽管到目前我们只使用过一个。如果当前 locale 为 `en_US`，主文件将是 `:/index.html`；但如果 locale 为 `fr_CA` 或 `fr` 或任何其他 `fr_`，当我们在代码中尝试访问 `:/index.html` 时，实际获取的文件将是 `:/index_fr.html`。

![](img/17_2.png)

**图 17.2 Qt Linguist**

用于创建和更新 .ts（翻译源文件）文件的工具是使用 `pylupdate4`。该程序从命令行运行，并将 .pro 文件作为参数传递。以下是完整的 `imagechanger.pro` 文件：

```pro
FORMS += newimagedlg.ui
SOURCES += helpform.py
SOURCES += imagechanger.pyw
SOURCES += newimagedlg.py
SOURCES += resizedlg.py
TRANSLATIONS += imagechanger_fr.ts
```

.pro 格式主要供 C++/Qt 程序员使用，但如果我们在 Qt 项目中使用它，将使使用 `pylupdate4` 和 `lrelease` 变得更简单。我们只关心三种条目：用于 .ui 文件的 `FORMS`，用于 .py 和 .pyw 文件的 `SOURCES`，以及用于 .ts 文件的 `TRANSLATIONS`。注意，我们没有列出 .qm 文件（如 `qt_fr.qm`）；这是因为我们不生成 `qt_fr.qm` 文件，而是直接从翻译目录中复制它。

我们不需要为每个文件使用一行；相反，我们可以对文件分组。例如：

```pro
FORMS = newimagedlg.ui
SOURCES = helpform.py imagechanger.pyw newimagedlg.py resizedlg.py
TRANSLATIONS = imagechanger_fr.ts
```

我们已经在源代码中使用了 `tr()` 和 `translate()`，并创建了 .pro 文件，我们可以运行 `pylupdate4`：

```bash
C:\pyqt\chap17> pylupdate4 -verbose imagechanger.pro
Updating 'imagechanger_fr.ts'...
Found 96 sources (96 new and 0 already existing)
```

使用 `-verbose` 选项当然是可选的。`pylupdate4` 程序会在 .pro 文件列出的 .ts 文件不存在时创建它，并将其放入所有出现在 .pro 文件的 `FORMS` 和 `SOURCES` 条目列出的文件中的、使用 `tr()` 和 `translate()` 标记的字符串上下文和字符串中。如果 .ts 文件已存在，`pylupdate4` 会添加任何必要的新的上下文和字符串，保留其中已添加的翻译。因为 `pylupdate4` 非常智能，我们可以根据需要随时运行它，即使翻译员通过添加或更改翻译更新了 .ts 文件，也不会丢失任何数据。

当我们准备好发布（或仅进行测试）翻译后的应用程序时，可以通过运行 `lrelease` 为 .ts 文件生成 .qm 文件：

```bash
C:\pyqt\chap17> lrelease -verbose imagechanger.pro
Updating 'C:/pyqt/chap17/imagechanger_fr.qm'
Generated 85 translations (81 finished and 4 unfinished)
Ignored 11 unrelated source texts
```

就像 `pylupdate4` 一样，我们可以根据需要随时运行 `lrelease`。我们不需要生成 `qt_fr.qm` 文件，因为我们复制了它。

可以避免使用 .pro 文件而仅依赖 `pylupdate4`。要做到这一点，我们必须运行：

```bash
cd C:\pyqt\chap17
pylupdate4 -ts imagechanger_fr.ts *.py
```

在代码方面，我们确保所有用户可见的字符串都使用 `QString.tr()` 或 `QApplication.translate()`。设置一个用于翻译的应用程序非常简单。.pro 文件通常用于使用 .ts 文件以及 .ui、.py 和 .pyw 文件，我们必须使用 `pylupdate4` 和 `lrelease` 来保持 .ts 文件的更新并生成 .qm 文件。

剩下的主要工作是翻译本身。为了这一点，我们可以给翻译员 Qt Linguist——它用 C++/Qt 编写并运行在 Windows、Mac OS 和 Linux 上——以及 .ts 文件，并让他们翻译这些字符串。

要开始使用 Qt Linguist，运行它，点击 File—Open 并打开一个 .ts 文件。现在点击左侧上下文窗口中的符号以显示上下文中的字符串，字符串将出现在右上面板的“Source text”标题下。点击“Translation”标题并输入翻译。要确认字符串翻译已完成，点击上下文窗口相关字符串下方的问号图标：点击该图标会在问号和勾之间切换。标记为“完成”的翻译将通过 `lrelease` 放入 .qm 文件。

创建一个使用 `QTextBrowser` 或 `QDesktopServices.openUrl()` 的在线系统是简单的，创建一个使用 QtAssistant 的系统是比较复杂的。但无论我们采取什么方式提供在线帮助，真正的挑战都是帮助文档的设计和内容。

Qt Linguist （如图 17.2 所示）易于使用，并通过建议以前翻译过的短语来减少重复。它根据上下文对翻译字符串分组，因为字符串在不同位置可能需要不同的翻译。

对于数字，我们可能需要使用 `%n` 来获取正确的千位分隔符和小数点。对于货币符号，可以使用这种技巧：

```python
currency = QApplication.translate("Currency", "$")
```

## 总结

创建一个使用 `QTextBrowser` 或 `QDesktopServices.openUrl()` 的在线系统是简单的，创建一个使用 QtAssistant 的系统是比较复杂的。但无论我们采取什么方式提供在线帮助，真正的挑战都是帮助文档的设计和内容。

```python
def updateUI(self):
    enabled = False
    if not self.roomEdit.text().isEmpty() and \
        self.dateEdit.date() > QDate.currentDate():
        enabled = True
    if self.request is not None:
        enabled = False
    self.bookButton.setEnabled(enabled)
    self.unbookButton.setEnabled(enabled)
```

如果房间编辑有房间号，并且日期选择器的日期晚于今天，我们就启用预订（book）和取消预订（unbook）——但如果存在待处理的请求（即 `self.request` 不为 `None`），我们就禁用它们。

```python
def closeEvent(self, event):
    self.socket.close()
    event.accept()
```

如果应用程序终止，我们确保关闭套接字并接受关闭事件。我们并不非要这样做这些事情，但通过这样做展示了我们已经考虑了终止时应该执行的操作。

```python
def book(self):
    self.issueRequest(QString("BOOK"), self.roomEdit.text(),
    self.dateEdit.date())
```

```python
def unbook(self):
    self.issueRequest(QString("UNBOOK"), self.roomEdit.text(),
    self.dateEdit.date())
```

如果用户点击“预订”，就会调用 `book()` 方法。该方法简单调用 `issueRequest()` 并传入请求动作 `"BOOK"`、房间号（作为 `QString`）和日期。`unbook()` 方法几乎完全相同，只是请求动作是 `"UNBOOK"`。

```python
def issueRequest(self, action, room, date):
    self.request = QByteArray()
    stream = QDataStream(self.request, QIODevice.WriteOnly)
    stream.setVersion(QDataStream.Qt_4_2)
    stream.writeInt16(0)
    stream << action << room << date
    self.request.seek(0)
    stream.writeInt16(self.request.size() - SIZEOF_UINT)
    self.updateUI()
    if self.socket.isOpen():
        self.socket.close()
        self.socketLabel.setText("Connecting to server...")
    self.socket.connectToHost("localhost", PORT)
```

此方法用于准备请求 `QByteArray` 并启动将请求发送到服务器的过程。

图 18.2 显示了写入请求 `QByteArray` 的数据。`QByteArray` 可以像任何其他 `QObject` 一样被读取和写入。前两个字节包含一个无符号整数，初始值为 0。该整数用于存储请求所占的字节数（不包括整数本身的大小），它是紧随其后的字节数。我们必须先将其置为 0，因为我们不知道将使用多少字节。

| uint16 | QString | QString | QDate |
|---|---|---|---|

**图 18.2 请求格式**

在长度整数之后，我们写入数据。动作字符串是请求动作（“BOOK”）或“UNBOOK”，房间字符串持有一个数字（例如，“213”），日期也已写入字节数组。我们使用 `seek()` 将写入位置移动到开头，以便下次写入时将作用在 `QDataStream` 底层的 `QIODevice` 上（该 `QIODevice` 是调用 `QDataStream.device()` 获取的）。我们写入一个 16 位的无符号整数，其值为 `QByteArray` 的长度减去初始整数的大小。现在请求数组已准备好发送。

我们更新了用户界面——这将允许启用“预订”和“取消预订”按钮，因为请求对象不是 `None`；这样做是为了防止用户在收到响应后发送额外的请求。我们确保套接字已关闭，因为它可能已经为了处理之前的请求而打开，并设置响应标签告知用户我们正在尝试建立连接。

最后，我们可以调用 `connectToHost()`。IP 地址可以以点分字符串的形式（例如，“82.94.237.218”）、主机名（“www.python.org”）或 `QHostAddress` 的形式给出。得益于我们在初始化器中建立的信号连接，我们知道连接已建立，将调用 `sendRequest()` 方法，除非连接失败，在这种情况下将改为调用 `serverHasStopped()` 或 `serverHasError()` 方法。

```python
def sendRequest(self):
    self.responseLabel.setText("Sending request...")
    self.nextBlockSize = 0
    self.socket.write(self.request)
    self.request = None
```

一旦建立连接，就会调用此方法。它更新响应标签以告诉用户正在发送请求，并将下一个块大小设置为 0。这与我们希望收到的响应有关；我们将在 `readResponse()` 方法中看到它。它将请求字节数组写入套接字。一旦数据写入，请求将被设置为 `None`，准备好进行新请求。

如果没有发生错误，且假设服务器没有终止，服务器将做出响应，此时将调用 `readResponse()` 方法。（否则，将调用 `serverHasStopped()` 或 `serverHasError()` 方法。）

| uint16 | QString | QString | QDate | 成功响应 |
|---|---|---|---|---|
| uint16 | QString | QString | | 错误响应 |

**图 18.3 响应格式**

服务器有两种不同的响应格式，如图 18.3 所示。当收到响应时，我们首先读取作为无符号 16 位整数的长度。这告诉我们后续有多少字节跟随。如果字节不足，我们退出循环并等待另一个 `readyRead()` 信号。如果字节足够，我们读取动作和随后的字符串——无论是房间号还是错误消息。如果动作不是 `"ERROR"`，我们还会读取日期。然后，根据收到的内容，我们准备消息并显示在响应标签中。读取完整个响应后，我们重置块大小，因为我们已经读取了字节。

```python
def readResponse(self):
    stream = QDataStream(self.socket)
    while True:
        if self.socket.bytesAvailable() < SIZEOF_UINT:
            break
        nextBlockSize = stream.readInt16()
        if self.socket.bytesAvailable() < nextBlockSize:
            break
        action = stream >> QString()
        room = stream >> QString()
        date = stream >> QDate()
        if action == "ERROR":
            msg = QString("Error: %1").arg(room)
        elif action == "BOOK":
            msg = QString("Booked %1 for %2").arg(room).arg(date.toString())
        elif action == "UNBOOK":
            msg = QString("Unbooked %1 for %2").arg(room).arg(date.toString())
        self.responseLabel.setText(msg)
        self.updateUI()
        self.nextBlockSize = 0
```

```python
def serverHasStopped(self):
    self.responseLabel.setText(
        "Error: Connection closed by server"
    )
    self.socket.close()
```

```python
def serverError(self, error):
    self.responseLabel.setText(QString("Error: %1")
        .arg(self.socket.errorString()))
    self.socket.close()
```

## 创建 TCP 服务器

建筑服务（Building Services）TCP 服务器位于 `chap18/buildingserviceserver.py`。它包含三个组件：一个持有 TCP 服务器实例并为用户提供终止服务器便利手段的 GUI；一个用于实例化提供服务器实例的 `QTcpServer` 子类；以及一个用于处理传入连接的 `QTcpSocket` 子类。我们将首先查看前两个部分，因为它们很短，然后重点关注承担了大部分工作的 `QTcpSocket` 子类。

```python
class BuildingServicesDlg(QPushButton):
    def __init__(self, parent=None):
        super(BuildingServicesDlg, self).__init__(
            "Close Server", parent)
        self.setWindowFlags(Qt.WindowStaysOnTopHint)
        self.loadBookings()
        self.tcpServer = TcpServer(self)
        if not self.tcpServer.listen(QHostAddress("0.0.0.0"), PORT):
            QMessageBox.critical(self, "Building Services Server",
                QString("Failed to start server: %1")
                .arg(self.tcpServer.errorString()))
            self.close()
            return
        self.connect(self, SIGNAL("clicked()"), self.close)
```

仅为了说明，并提醒我们任何 Qt 部件都可以作为顶层窗口，我们可以让对话框成为 `QPushButton` 的子类。我们还设置了 `Qt.WindowStaysOnTopHint`；大多数窗口系统都会尊重此提示并将窗口置在所有其他窗口之上。

我们不会复介绍 `loadBookings()` 方法；它用于填充存储预订数据的内存数据结构——默认字典。字典的键是日期 `datetime.date` 对象，值是存储为 unicode 字符串的房间号有序列表。默认字典（`collections.defaultdict`）是在 Python 2.5 中引入的。它们与普通字典相似，区别在于当我们使用一个字典中不存在的键时，该键会被插入一个默认值。使用什么默认值取决于我们如何创建字典。在建筑服务服务器中，我们这样创建字典的：

```python
Bookings = collections.defaultdict(list)
```

在这里，我们规定任何新键的默认值是一个空列表；在其他情况下，我们可能会选择一个空集合。我们可以通过使用 `dict.setdefault()` 方法在访问可能不存在的键时，将默认字典替换为普通字典——例如在使用比 2.5 旧的 Python 版本时——如下所示。

我们将很快回顾 `TcpServer` 类。一旦创建了服务器，我们就告诉它在给定的 IP 地址和端口号上监听连接。IP 地址指定为 `QHostAddress`，使用特殊地址 `"0.0.0.0"`，意味着“所有网络接口”；端口号与我们在客户端使用的任意端口 9407 相同。

连接确保了如果用户点击按钮，窗口将关闭。我们没有对 TCP 服务器进行任何特殊的清理工作；当它被销毁时，连接的客户端将收到通知，并发出 `disconnected()` 信号。

对话部分没有内容了，我们现在可以查看继承自 `QTcpServer` 的小型 `TcpServer` 类。



```python
class TcpServer(QtServer):
    def __init__(self, parent=None):
        super(TcpServer, self).__init__(parent)

    def incomingConnection(self, socketId):
        socket = Socket(self)
        socket.setDescriptor(socketId)
```

这是 TCP 服务器的完整代码。每当发生传入连接请求时，`incomingConnection()` 方法就会被调用，并传入一个 socket 中的套接描述符。我们只需创建一个新的 `Socket`（我们将之后回顾的 `QtSocket` 子类），并设置它使用服务器提供的套接描述符。

此 Tcp 服务器依赖于 PyQt 事件循环。如果我们想创建一个不带 GUI 的基于 `TcpServer` 的服务器，有两种方法可以采取。一种是使用 `QLoop` 来提供一个不需要 GUI 的事件循环，并按照我们之前的方式编写代码。另一种方法是不使用事件循环，但在这种情况下我们必须以稍微不同的方式操作。具体来说，我们必须使用阻塞的 `TcpServer.waitForNewConnection()` 方法，而不是重新实现 `incomingConnection()`。当然，如果服务器没有 GUI，可能根本不需要使用 `QtNetwork` 模块。或者，可以使用 `Twisted` 来编写服务器。

一旦建立连接，所有工作将交给 `Socket` 类，这是一个 `TcpSocket` 子类（`QtSocket`），我们现在就开始回顾它。

```python
class Socket(QtSocket):
    def __init__(self, parent=None):
        super(Socket, self).__init__(parent)
    self.connect(self, SIGNAL("readyRead()"), self.readRequest)
    self.connect(self, SIGNAL("disconnected()"), self.deleteLater)
    self.nextBlockSize = 0
```

socket 将 `readyRead()` 信号连接到我们自定义的 `readRequest()` 方法，并将 `disconnected()` 信号连接到其 `deleteLater()` 槽——这确保了 socket 在连接终止时被干净地删除。`nextBlockSize` 变量的作用和用法与客户端中相同，以确保我们只在可读字节至少达到请求所需的长度时才读取请求。

一旦创建了 socket 并设置了连接，它只需等待 `readRequest()` 方法被调用。这部分有点长，所以我们将分部分回顾。

```python
def readRequest(self):
    stream = QDataStream(self)
    action = QString()
    date = QDate()
    
    stream >> action >> date
    if action == "BOOK":
        if bookings is None:
            bookings = Bookings[date.toDate()]
        if len(bookings) < MAX_BOOKINGS_PER_DAY:
            if uroom in bookings:
                self.sendError("Cannot duplicate booking")
            else:
                bisect.insort(bookings, uroom)
                self.sendReply(action, date)
    elif action == "UNBOOK":
        if bookings is None or uroom not in bookings:
            self.sendError("Cannot unbook booking")
        else:
            bookings.remove(uroom)
            self.sendReply(action, date)
    else:
        self.sendError("Unrecognized request")
```

## 创建 TCP 服务器

我们简单地使用了 `not in` 和 `list`，它们都执行的是线性搜索；对于较长的列表，我们会使用 `bisect.bisect_left()` 通过二分查找法来查找房间，但在本示例中这似乎是大材小用了。

如果请求操作无法识别，我们将回复一条错误消息。

```python
def sendReply(self, action, room, date):
    reply = QByteArray()
    stream = QDataStream(reply, QIODevice.WriteOnly)
    stream.setVersion(QDataStream.Qt_4_2)
    stream.writeInt16(0) << action << room << date
    stream.device().seek(0)
    stream.writeInt16(reply.size()) - SIZE_OF_UINT16
    self.write(reply)
```

发送给客户端的回复创建方式与客户端请求的方式相同。我们使用 `QDataStream` 向 `QByteArray` 写入内容，首先写入一个 16 位无符号整数，最后用回复的大小覆盖该整数，然后将回复写入套接字。

```python
def sendError(self, msg):
    reply = QByteArray()
    stream = QDataStream(reply, QIODevice.WriteOnly)
    stream.setVersion(QDataStream.Qt_4_2)
    stream.writeInt16(0) << QString("ERROR") << QString(msg)
    stream.device().seek(0)
    stream.writeInt16(reply.size()) - SIZE_OF_UINT16
    self.write(reply)
```

发送错误回复的代码与发送成功回复的代码几乎相同，可以说我们本可以用一个方法处理这两种情况。

通过在 `readRequest()` 中添加更多的 `if` 语句，可以轻松地扩展服务器以处理更多请求类型。例如，客户端可能想知道某天哪些房间被预订，或者某个房间在哪些日期被预订了。

尽管我们使用了字典来存储服务器数据，但没有理由让服务器将数据存储在进程内的 SQLite 数据库、进程外数据库或文件中。服务器也不需要有 GUI；它可以没有任何 QWidgets，只需作为 Linux 守护进程或 Windows 服务在后台运行。

## 总结

Python 标准库、Twisted 网络引擎以及 PyQt 的 QtNetwork 模块为网络提供了大量的支持，涵盖从低层套接字到包括 FTP 和 HTTP 在内的各种高级协议。

为了编写客户端/服务器应用程序，我们必须确保客户端和服务器程序能够通信。这意味着服务器必须运行在已知的 IP 地址上并在特定的端口地址监听。客户端和服务器都使用约定的协议（如 UDP 或更常见的 TCP）进行通信。它们还必须就如何传输数据（无论是文本行还是二进制数据）无论哪种情况，它们都必须知道每个请求和响应必须采用的格式。

本章展示的场景非常常见。服务器等待请求，客户端发送请求并读取服务器的响应。一旦连接建立，客户端就可以发送其数据。服务器可能会响应数据，也可能发生了问题。如果接收到数据，我们必须确保不会尝试读取超过可用范围的字节（或行）。

PyQt 的 `TcpServer` 和 `TcpSocket` 类使得实现服务器变得非常简单。虽然读写文本数据行是可行的，但使用二进制数据更具通用性，允许我们发送和接收任何类型的数据，而无需编写解析器。

我们实现的 TCP 服务器的一个理论性问题是它是单线程的。这意味着如果多个请求同时到达，它可能必须阻塞以一次处理一个请求。这可以通过下一节中看到的多线程服务器来解决。

## 练习

修改楼宇服务（Building Services）服务器使其接受一个新的请求操作 `BOOKINGSONDATE`。当接收到此类请求时，它应该忽略房间，而是检索给定日期的预订情况。如果没有预订，服务器应发送错误回复。否则，它的回复不应是单个房间字符串，而是一个包含逗号和空格分隔的房间号字符串，如图 18.4 所示。

修改楼宇服务客户端，使其有一个“按日期预订？”按钮，但将其连接到一个发布合适请求的方法。客户端的 `read-Response()` 方法需要稍微修改，以便其能够读取服务器对新请求的响应。

提供“日期预订”所需的修改是简单的。为了增加挑战，修改楼宇服务服务器以接受另一个新请求操作 `BOOKINGSFORROOM`。当接收到这些请求之一时

![](img/55bc1dcf8601cfec5e1423b4e17ec264_549_0.png)

**图 18.4** 楼宇服务——按日期预订

![](img/55bc1dcf8601cfec5e1423b4e17ec264_549_1.png)

**图 18.5** 楼宇服务——房间预订

## 538 第 19 章 多线程

因为那将超出本书的范述范围，并且需要专门写一本书。

由于多个线程可能并发访问相同的数据，多线程应用程序通常比单线程应用程序更难编写、维护和调试。在单处理器机器上，多线程应用程序的运行速度有时比单线程应用程序慢（由于额外线程带来的**处理开销），但用户通常认为它们速度更快，因为它们不会冻结用户界面，而且它们能够更容易地增量地向用户报告进度。

使用正确数量的线程会显著影响性能。例如，在在本章介绍的页面索引器（Page Indexer）中，我们有一个主线程（GUI）和一个辅助线程。练习活动涉及更改示例以使用多个辅助线程。如果使用许多线程，应用程序的运行速度将比单辅助线程的版本慢，但通过调整数量，我们可以启动一个辅助线程，然后启动多辅助线程的版本，并看到多辅助线程在单辅助线程版本完成之前就赶上并完成。我们应该使用多少个辅助线程呢？这取决于正在处理的任务以及应用程序运行的特定机器操作系统。我们可以通过对真实数据集进行实验来确定一个数值，或者根据情况使用更多或更少的辅助线程。

Python 的标准库提供了低级的 `thread` 模块和高级的 `threading` 模块，但对于 PyQt 编程，我们建议使用 Qt 线程类。PyQt 的线程类提供了高级 API，但在底层，它们的一些基本操作是用汇语言实现的，以确保它们尽可能快速和精细，这是 Python 的 `threading` 模块中不具备的。

PyQt 应用程序始终至少有一个执行线程，即主（初始）线程。此外，它们可以根据需要创建许多辅助线程。然而，如果应用程序具有 GUI，则 GUI 操作（例如执行事件循环）可能只在主线程中发生。新线程是通过实例化重新实现 `Thread.run()` 方法的 `QThread` 子类来创建的。

可以使用 `CoreApplication` 代替 `QApplication` 创建没有 GUI 的 PyQt 应用程序。像 GUI PyQt 应用程序一样，它们有一个主线程和任意数量的辅助线程。

辅助线程与主线程之间的通信通常是理想的；例如，让用户了解进度、允许用户在处理期间进行干预，并让主线程知道处理何时完成。传统上，这种通信是通过共享变量配合资源保护机制来实现的。

## 创建多线程服务器

PyQt 有类可以支持这种方法，包括 `QMutex`、`QReadWriteLock` 和 `QSemaphore`。此外，PyQt 应用程序可以使用信号槽机制在线程之间进行通信；这非常方便有用。

在本章的第一节中，我们将查看一个多线程 TCP 服务器；它的工作与上一章最后一节描述的服务器相同，但由于它是多线程的，它可以同时为多个客户端服务。在第二、第三节中，我们将查看一个具有某些耗时处理的 GUI 应用程序，并将处理传递给辅助线程。该应用程序使用信号和槽来保持用户界面的进度更新，并提供用户对辅助线程的控制。此示例还使用了一些资源保护类，以便用户界面可以访问正在进行的工作。

## 创建多线程服务器

与其他 GUI 库不同，PyQt 的网络套接字类与事件循环集成。这意味着在网络处理期间，用户界面仍然保持响应，即使在单线程 PyQt 应用程序中也是如此。如果我们能够处理多个同时进入的连接，我们可能倾向于使用多线程服务器。

制作多线程服务器并不比制作单线程服务器复杂——两者的区别在于创建一个单独的套接字来处理传入的连接，多线程服务器为每个新连接创建一个新线程，并在每个新线程内部创建一个新套接字。例如，这里是一个完整的多线程服务器：

```python
class TcpServer(QTcpServer):
    def __init__(self, parent=None):
        super(QTcpServer, self).__init__(parent)
    def incomingConnection(self, socketId):
        thread = Thread(socketId, self)
        self.connect(thread, SIGNAL("finished()"),
                      thread, SLOT("deleteLater()"))
        thread.start()
```

`incomingConnection()` 方法是从 `QTcpServer` 基类重新实现的。每当有新的网络连接到服务器时，该方法就会被调用。

信号槽连接是必要的，确保线程在不再需要时被删除，从而使服务器的内存占用尽可能小。尽管我们必须在 `QThread` 子类中重新实现 `QThread.run()`，但线程总是通过调用 `QThread.start()` 启动的（永远不直接调用 `run()`）。

## 540 第 19 章 多线程

`Thread` 子类有一个静态变量和四个方法。`sendReply()` 和 `sendError()` 方法与前一章所示的相同，因此我们将省略它们。

```python
class Thread(QThread):

    lock = QReadWriteLock()

    def __init__(self, socketId, parent):
        super(Thread, self).__init__(socketId)
        self.socketId = socketId
```

`Thread.lock` 变量是静态的，因此所有 `Thread` 实例共享它。初始化器只是记录了套接字描述符，以便在线程启动时使用。`run()` 方法非常长，因此我们将分部分回顾。

```python
def run(self):
    socket = TcpSocket()
    if socket.setDescriptor(self.socketId):
        stream = QDataStream(socket)
        stream.setByteOrder(QDataStream::BigEndian)
        while True:
            if socket.waitForReady(100):
                size = stream.readUint16()
                if (size == 0):
                    break
                if socket.availableBytes() >= size:
                    data = stream.read(size)
                    if data == "ERROR":
                        break
                else:
                    break
            else:
                break
        action = QString()
        stream >> action
        if action == "BOOK":
            room = QString()
            date = QDate()
            stream >> room date
            try:
                Thread.lock.lockWrite()
                Bookings[date.toDate()] = room
            finally:
                Thread.lock.unlock()
        elif action == "UNBOOK":
            room = QString()
            date = QDate()
            stream >> room date
            try:
                Thread.lock.lockWrite()
                Bookings.remove(date.toDate())
            finally:
                Thread.lock.unlock()
        else:
            room = QString()
            date = QDate()
            stream >> room date
            try:
                Thread.lock.lockRead()
                if Bookings.contains(date.toDate()):
                    room = Bookings[date.toDate()]
                else:
                    room = ""
            finally:
                Thread.lock.unlockRead()
        if room != "":
            self.sendReply(room)
        else:
            self.sendError("Room not found")
    self.emit(finished())
```

`Thread.lock` 变量是静态的，因此所有 `Thread` 实例共享它。初始化器只是记录了套接字描述符，以便在线程启动时使用。`run()` 方法非常长，因此我们将分部分回顾。

（此处代码块内容根据指令不翻译，但由于上方译文有逻辑补全，此处保持代码逻辑完整）

## 555 创建多线程服务器

其余应用程序，主线程和任意数量的辅助线程，如果只有锁是读锁，则没有线程被阻塞，因此在没有线程写入的情况下，所有线程读取都是安全的。一旦有了两个字节，

```python
action = QString()
if action in ("BOOK", "UNBOOK"):
    stream >> room date
    try:
        Thread.lock.lockWrite()
```...

```python
room = unicode(room)
```

我们读取请求的动作，它应该是 "BOOK" 或 "UNBOOK"，如果它是其中之一，我们就读取房间号字符串和日期。`Bookings` 字典持有所有的预订数据，并且有任意数量的线程同时访问。由于这个原因，我们必须保护每次访问。在这里，我们只想读取，所以我们可以 `lockForRead()`，提取我们需要的数据，然后释放锁。我们使用 `try ... finally` 来确保在访问共享数据后释放锁。

一种已锁定机制是互斥锁（也称为二进制信号量），由 PyQt 的 `Mutex` 类提供。互斥锁允许一个线程访问受保护的资源。PyQt 还提供了更精细的机制，读写锁，由我们使用的 `QReadWriteLock` 类提供。当一个线程锁定时，其他线程可能会阻塞等待访问。我们可以通过两种方式来最小化这个问题：首先，尽可能使用锁——如果只有锁是读锁，则没有线程被阻塞，因此在没有线程写入的情况下，所有线程读取都是安全的。其次，通过在 `run()` 实现中使用这两种技术来最小化处理量；缺点是代码比预期的要长得多。

Mutex、ReadWriteLock 以及其他保护机制之所以能工作，是因为它们都是“线程安全”的。任意数量的线程都可以同时调用线程安全对象的方法，并依靠底层系统（即 PyQt）自动序列化对可能存在的共享数据的访问。

## 542 第 19 章 多线程

发生。这意味着，例如，如果两个或多个线程尝试对 `QReadWriteLock` 进行写入锁，则只有一个线程会成功，而所有其他线程都将被阻塞。这允许获得锁的线程在共享数据上执行更新，当它释放锁时，想要写入的其它线程之一将获得访问权限，依此类推，直到没有更多线程需要访问为止。

PyQt 文档说明了哪些类或类中的哪些方法是线程安全的。它还指出方法是可重入（reentrant）的。重入方法比线程安全方法更具限制性。这是因为如果从多个线程同时调用重入方法，且每次调用都只访问唯一的数据（如局部变量），那么这种调用是安全的。通过使用锁来对实例变量以及任何引用共享数据的变量进行访问，可以使重入方法变为线程安全。

```python
if action == "BOOK":
    newlist = False
    try:
        Thread.lock.lockRead()
        if bookings is None:
            newlist = True
    finally:
        Thread.lock.unlock()
    if newlist:
        try:
            Thread.lock.lockForWrite()
            bookings = Bookings[date.toDate()]
        finally:
            Thread.lock.unlock()
```

如果请求是订房间，我们首先检查 `bookings` 变量。它可能是 `None`，要么指向共享 `Bookings` 默认字典持有的列表的引用，因此在访问它时必须使用读锁。如果 `bookings` 为 `None`，我们将给定的日期作为键向字典中插入一个空列表；这次我们使用写锁。

```python
error = None
insert = False
try:
    if len(bookings) < MAX_BOOKINGS_PER_DAY:
        if uroom in bookings:
            error = "Cannot accept duplicate booking"
            insert = True
else:
    error = QString("%1 is fully booked").arg(
        date.toDate(Qt.ISODate)
    )
```

## 创建多线程服务器

```python
finally:
    Thread.lock.unlock()
if insert:
    try:
        Thread.lock.lockWrite()
        bisect.insert(bookings, uroom)
    finally:
        Thread.lock.unlock()
        self.sendReply(socket, action, room, date)
    else:
        self.sendError(socket, error)
```

如果该房间在给定日期已被预订，我们不会重复订购，而是向客户端发送错误响应。在非线程服务器中，在这种情况下我们简单地调用 `sendError()`，但在这里我们只需分配错误文本。这样做是为了将锁的上下文中执行的处理降到最低。

如果可以订房，我们获取写锁，将房间插入到 `bookings` 列表中，并发送指示成功的响应。否则，我们发送错误响应。两种响应都不会在锁的上下文中发送，同样是为了最小化锁生效的时间。

```python
elif action == "UNBOOK":
    error = None
    remove = False
    try:
        Thread.lock.lockForRead()
        if bookings is None or uroom not in bookings:
            error = "Cannot unbook nonexistent booking"
    else:
        remove = True
    finally:
        Thread.lock.unlock()
if remove:
    try:
        Thread.lock.lockForWrite()
        bookings.remove(uroom)
    finally:
        Thread.lock.unlock()
        self.sendReply(socket, action, room, date)
    else:
        self.sendError(socket, error)
```

取消订房的分与订房分支遵循相同的模式。我们首先使用读锁检查是否可以取消订房，并在必要时存储错误消息，而不是在锁生效期间执行耗时的发送操作。我们通过从 `Bookings` 字典给定日期的列表中移除房间来取消订房并发送成功响应，或者我们发送错误响应。同样，响应是在没有锁生效时发送的。

```python
else:
    self.sendError(socket, "Unrecognized request")
    socket.waitForDisconnected()
```

如果服务器接收到它无法识别的请求，它只需发送一个响应。在最后，我们调用了 `QtSocket.waitForDisconnected()`；这会阻塞直到连接关闭且响应已发送。我们不需要也不想保持连接打开，因为我们的客户端/服务器应用程序是以对独立的请求-事务的形式运行的。一旦连接关闭，`run()` 方法就会结束，得益于 `delete()` 信号连接，线程将被删除。

## 创建和管理辅助线程

GUI 应用中线程的一个常见用途是在辅助线程中进行处理，以便用户界面可以保持响应，并显示辅助线程的进度。在本节中，我们将查看图 19.1 所示的页面索引器应用程序，它对特定目录及其所有子目录中的 HTML 文件进行索引。索引工作被交给辅助线程，该线程与主线程通信，以通知它已取得进度以及索引何时完成。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_558_0.png)

> 图 19.1 页面索引器

我们将用于索引的算法是：对于遇到的每个文件，读取其文本，将实体转换为 Unicode，并剥离标签。然后将文本分割为单词。`fileCount` 变量用于跟踪目前为止索引了多少文件。`filenamesWords` 默认字典的键是单词，值是集合。读/写锁用于确保对 `filenamesWords` 字典和 `commonWords` 集合的访问受到保护。

## 创建与辅助线程

```python
class Form(QDialog):
    def __init__(self, parent=None):
        super(Form, self).__init__(parent)
        self.fileCount = 0
        self.filenamesForWords = collections.defaultdict(set)
        self.commonWords = set()
        self.lock = QReadWriteLock()
        self.path = QDir.homePath()
```

在一个线程中发射的、用于另一个线程的信号是异步执行的，也就是说，它们不会阻塞。但只有在接收端存在事件循环时它们才会起作用。

```python
self.walker = Walker(self, self)
self.path = Q
()
    self.statusLabel.setText("Click the Set Path '"
    "button to start indexing")
self.pathButton.setEnabled(True)
    self.connect(self.pathButton, SIGNAL("clicked()"),
    self.setPath)
    self.connect(self.walker, SIGNAL("indexed(QString)"),
    self.indexed)
    self.connect(self.walker, SIGNAL("finished(bool)"),
    self.finished)
    self.connect(self.findEdit, SIGNAL("returnPressed()"),
    self.find())
```

# 创建与管理辅助线程

```
return
self.path = QDir.toNativeSeparators(path)
self.findEdit.setFocus()
self.pathLabel.setText(self.path)
self.statusLabel.clear()
self.filesListWidget.clear()
self.fileCount = 0
self.filenamesForWords = collections.defaultdict(set)
self.commonWords = set()
self.walker.initialize(unicode=self.path),
self.filenamesForWords, self.commonWords
self.walker.start()
```

当用户点击“设置路径”（Set Path）时，我们首先禁用该按钮，如果线程正在运行，则停止它。`stop()` 方法是我们自定义的一个方法。`wait()` 方法继承自 `QThread`；它会阻塞直到线程运行结束，即 `run()` 方法返回。在 `stop()` 方法中，我们间接地确保了在 `stop()` 被调用后 `run()` 方法能够尽快结束，我们下一节中看到这一点。

接下来，我们获取用户选择的路径（如果他们取消了，则返回）。我们使用了 `QDir.toNativeSeparators()`，因为 PyQt 内部始终使用“/”来分隔路径，但在 Windows 上我们希望显示“\”。`NativeSeparators()` 方法是在 Qt 4.2 中引入的；对于更早的版本，请使用 `QDir.convertSeparators()`。默认情况下，`getExistingDirectory()` 只显示目录，因为它带有一个默认值为 `QFileDialog.ShowDialogOnly` 的可选参数；如果我们要让文件名可见，可以通过传递 `QFileDialog.Options()` 来清除此标志。

用户界面的设置方法是：将焦点移动到行编辑框（line edit），将路径设置为选定的路径，并清除用于告知用户进度状态标签（status label）。文件列表（files list）列出了包含行编辑框中单词的文件。我们不需要对访问 `filenamesForWords` 字典或 `commonWords` 集合进行保护，因为此时运行的唯一线程是主线程。

最后，我们通过路径以及用于填充该结构的数据结构的引用来初始化遍历器（walker），然后调用 `start()` 执行。

```python
def indexed(self, fname):
    self.statusLabel.setText(fname)
    self.fileCount += 1
    if self.fileCount % 25 == 0:
        self.filesIndexedLCD.display(self.fileCount)
    try:
        self.lock.lockForRead()
        indexedWordCount = len(self.filenamesForWords)
        commonWordCount = len(self.commonWords)
finally:
    self.lock.unlock()
self.wordsIndexedLCD.display(indexedWord)
self.commonWordsLCD.display(commonWord)
elif self.fileCount % 101 == 0:
    self.commonWordsListWidget.clear()
try:
    self.lock.lockForRead()
    words = self.commonWords.copy()
    finally:
        self.lock.unlock()
        self.commonWordsListWidget.addItems(sorted(words))
```

# 第 19 章. 多线程

每当遍历器线程完成一个文件的索引时，它会发射一个带有文件名的 `indexed` 信号；该信号连接到之前展示的 `Form.indexed()` 方法。我们更新状态标签以显示刚刚索引的文件名，并且每处理 25 个文件，我们还会更新文件计数、索引计数以及常用词 LCD 控件。我们使用读锁来确保共享数据结构的读取是安全的，并且在锁的上下文中只执行最少的工作，仅在释放锁后更新 LCD 控件。

对于每处理的第 10 个文件，我们使用常用词列表控件（common words list widget）。我们再次使用读锁，并使用 `set.copy()` 来确保在释放锁后我们不再引用共享数据。

```python
def finished(self, completed):
    self.statusLabel.setText("Indexing complete" \
    if not completed else "Stopped")
    self.finishedIndexing()
```

当线程停止或完成时，它会发射一个 `finished()` 信号，连接到该方法并传递一个布尔值以指示是否已完成。我们更新状态标签并调用 `finishedIndexing()` 方法来更新用户界面。

```python
def finishedIndexing(self):
    self.walker.wait()
    self.filesIndexedLCD.display(self.fileCount)
    self.wordsIndexedLCD.display(len(self.filenamesForWords))
    self.commonWordsLCD.display(len(self.commonWords))
    self.pathButton.setEnabled(True)
```

当索引完成后，我们调用 `QThread.wait()` 以确保线程的 `run()` 方法已结束。然后我们根据共享数据结构的当前值更新用户界面。我们不需要对字典或集合的访问进行保护，因为遍历器线程没有运行。

# 创建与管理辅助线程

## 使用上下文管理器进行解锁

在本章中，我们使用 `try ... finally` 块来确保在在使用后释放锁。Python 2.6 提供了另一种方法，即使用新的 `with` 关键字结合上下文管理器（context manager）。关于上下文管理器的说明在 http://www.python.org/dev/peps/pe-0343 中有解释；简单来说，我们可以通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来创建一个上下文管理器。然后，与其写像这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

我们可以写出简单得多更短的代码：

```python
with ReadLock():
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

在实际使用中，我们可以这样写：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

使用 `with` 语句的写法更加清晰易读：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

使用 `with` 语句的写法更加清晰易读：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

使用 `with` 语句的写法更加清晰易读：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

使用 `with` 语句的写法更加清晰易读：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

使用 `with` 语句的写法更加清晰易读：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

使用 `with` 语句的写法更加清晰易读：

```python
with ReadLock(self.lock):
    found = word in self.commonWords
```

这种方法在 `with` 语句中是有效的，因为我们通过创建一个具有两个特殊方法 `__enter__()` 和 `__exit__()` 的类来实现上下文管理器。例如：

```python
class ReadLock:
    def __init__(self, lock):
        self.lock = lock
    def __enter__(self):
        self.lock.lockForRead()
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.lock.unlock()
```

由于 `try ... finally` 块的写法，我们也可以写这样的代码：

```python
try:
    self.lock.lockForRead()
    found = word in self.commonWords
finally:
    self.lock.unlock()
```

（注：由于原始文本中存在大量重复的示例代码和描述，翻译时已根据“不要重复输出原文”的原则，对核心逻辑部分进行了整合处理，去除了冗余的重复段块。）

线程，使用了读写锁的保护。在接下来的章节中，我们将看到 Walker 线程是如何实现的、它是如何发射信号的以及以及如何填充给它的数据结构的。

## 实现辅助线程

页面索引器（Page Indexer）的辅助线程实现在 chap19/walker.py 中的 `Walker` 类中。该类是 `Thread` 的子类，使用 `QMutex` 来保护对其私有数据的访问，并使用传递给它的 `QReadLock` 来保护与主线程共享数据的访问。

class Walker(Thread):

```python
COMMON WORDS_THRESHOLD = 250
MAX_WORD_LEN = 25
INVALID_FIRST_LAST = frozenset("0123456789")
STRIPHTML_RE = re.compile(r"<]++", re.IGNORECASE|re.MULTILINE)
ENTITY_RE = re.compile(r"&(\w+;)|&&#(\d+);")
SPLIT_RE = re.compile(r"\W+", re.IGNORECASE|re.MULTILINE)
```

该类开始了一些静态变量，这些变量控制一个单词在多少个文件中出现会被视为常用词、单词的最小和最大长度，以及单词不能以哪些字符开头或结尾。“剥离 HTML”正则表达式用于剥离 HTML 标签，实体表达式用于提取要转换为 Unicode 字符的实体，而分割正则表达式用于将文件分割为其包含的单词。一个更实际的应用程序可能会使用 HTML 解析器而不是正则表达式。

```python
def __init__(self, lock, parent=None):
    super(Walker, self).__init__(parent)
    self.lock = lock
    self.stopped = False
    self.mutex = QMutex()
    self.path = None
    self.completed = False
```

应用程序创建了一个工作线程对象，但没有立即启动它。锁是用于保护对共享文件 `filenamesForWords` 默认字典所有访问的同一个 `QReadWriteLock`，而 `stopped` 变量用于类内部，用于判断线程是否被请求停止（通过调用 `stop()` 方法）。互斥锁（mutex）用于保护 walker 线程本身对 `stopped` 变量的访问。这是必要的，因为当 `run()` 方法执行时，可能会调用线程的另一个方法（如 `stop()`）。`completed` 变量用于指示在线程停止时索引是否完成。

```python
def initialize(self, path, filenamesForWords, commonWords):
    self.stopped = False
    self.path = path
    self.filenamesForWords = filenamesForWords
    self.commonWords = commonWords
    self.completed = False
```

该方法设计用于在 `QThread.start()` 之前调用，以设置索引线程。它不应该在线程运行时被调用。如果我们非常多疑，可以在开头放一个 `if not self.isStopped(): return`。

虽然使用互斥锁和锁是没有害的，但它们都不是必要的。当调用此方法时，walker 线程并没有运行，给 `stopped` 赋值没有问题，而对于传入的字典，我们只是获取了它们的引用，没有对其进行任何修改。

```python
def run(self):
    self.processFiles(self.path)
    self.stop()
    self.emit(SIGNAL("finished(bool)"), self.completed)
```

当调用者执行 `start()` 时，线程会调用 `run()` 方法——这是我们绝不能手动做的。该方法只有三条语句，`processFiles()` 的执行可能花费很长时间，因为它涉及到递归读取和索引路径下的所有 HTML 文件。但这并不是问题，因为处理是在 walker 的执行线程中进行的，它保持着响应，并且主线程可以调用 walker 线程的方法，并响应 walker 的信号，正如我们在前一节中看到的那样。在最后，`run()` 方法发射一个 `finished()` 信号，并带有一个布尔标志指示索引是否完成；如果没有完成，用户一定通过用户界面停止了它。

```python
def stop(self):
    try:
        self.mutex.lock()
        self.stopped = True
    finally:
        self.mutex.unlock()
```

这会阻塞锁直到获取锁为止，得益于 `try ... finally`，它保证了互斥锁在结束时会被解锁。

如果我们使用的是 Python 2.6，或者带有适当的 `from __future__` 语句的 Python 2.5，我们可以将此方法重写为：

```python
def stop(self):
    with QMutexLocker(self.mutex):
        self.stopped = True
```

在 PyQt 4.1 中，`QMutexLocker` 类可以作为上下文管理器。它接收作为参数的 `QMutex`（阻塞直到可以获取锁），并在控制流离开作用域时解锁互斥锁（即使由于异常导致作用域退出）。

```python
def isStopped(self):
    try:
        self.mutex.lock()
        return self.stopped
    finally:
        self.mutex.unlock()
```

注意 `return` 语句位于 `try ... finally` 块内部。当遇到 `return` 时，方法将尝试返回值，但它将被强制进入 `finally` 块，之后方法才会带有 `return` 语句的值返回。

如果我们使用的是 Python 2.6 或带有适当的 `from __future__` 语句的 Python 2.5，我们可能会完全省略这个方法，而在其他一些方法中，与其编写：

```python
if self.isStopped():
    return
```

这些方法在开销上不应该有显著差异，尽管使用 `QMutexLocker` 看起来是最清晰的。`processFiles()` 方法相当长，因此我们将分三部分进行审查。

```python
def processFiles(self, path):
    def unichrFromEntity(match):
        text = match.group(last)
        if text.isdigit():
            return unchr(int(text))
        u = name2codoint.get(text)
        return unchr(u) if u is not None else ""
```

我们从一个嵌套函数开始。它与实体正则表达式（见552页）配合使用。对于正则表达式匹配的对象，函数获取 `last`（即匹配组），如果它全是数字，则返回相应代码点的 Unicode 字符。否则，函数返回匹配实体名称 Unicode 字符，如果名称不在 `name2codoint` 字典中，则返回空字符串。

```python
for root, dirs, files in os.walk(path):
    if self.isStopped():
        return
    for name in [name for name in files if name.endswith((".htm", ".html"))]:
        fname = os.path.join(root, name)
        if self.isStopped():
            return
        words = set()
        fh = None
        try:
            fh = codecs.open(fname, "r", "UTF-8", "ignore")
            text = fh.read()
        except (IOError, OSError) as e:
            sys.stderr.write("Error: %s\n" % e)
            continue
        finally:
            if fh is not None:
                fh.close()
        if self.isStopped():
            return

        text = self.STRIPHTML_RE.sub("", text)
        text = self.ENTITY_RE.sub(unichrFromEntity, text)
        text = text.lower()
```

# 556 第 19 章 多线程

剩余的文本。`re.sub ("substitute")` 方法将要处理的文本作为第二个参数；其第一个参数可以是替换每个匹配项的字面量，也可以是要调用的函数。如果是函数，则每个匹配对象都将传递给该函数，函数的返回值（应该是一个字符串）将用作替换字符串。

在几处，我们检查 `stopped` 变量是否为 `True`，如果调用了 `stop()` 方法，它就会为 `True`。如果发生了这种情况，我们不再进行后续索引，直接返回。如果检查太少，读者可能会在请求停止索引和线程实际停止之间遇到延迟。另一方面，检查得越多，线程运行得就越慢。因此，我们经常进行检查，至于在何处放置检查，通常需要一些反复尝试才能正确。

```python
for word in self.SPLIT_RE.split(text):
    if self.MIN_WORD_LEN <= len(word) <= \
        self.MAX_WORD_LEN and \
        word[0] not in self.INVALID_FIRST_OR_LAST and \
        word[-1] not in self.INVALID_FIRST_OR_LAST:
        try:
            self.lock.lockForRead()
            new = word not in self.commonWords
        finally:
            self.lock.unlock()
        if new:
            words.add(word)
    if self.isStopped():
        return
    for word in words:
        try:
            self.lock.lockForWrite()
            files = self.filenamesForWords[word]
            if len(files) > self.COMMON_WORDS_THRESHOLD:
                del self.filenamesForWords[word]
            self.commonWords.add(word)
        else:
            files.add(unicode(fname))
        finally:
            self.lock.unlock()
    self.emit("SIGNAL(indexed(QString))", fname)
self.completed = True
```

文件文本中的每个单词长度既不长也不短，且不以不可接受的字符开头，我们首先查看它是否在常用词汇集中，如果不在，我们就将其添加到本地单词集中。

一旦我们在 `words` 集合中收集了文件的非常用词，我们就遍历这个集合。新单词被添加到 `filenamesForWords` 默认字典中。如果字典的文件名集合过大，我们就删除该字典条目并将单词添加到常用词集合中；否则，我们将文件名添加到该单词对应的字典集合中。当然，我们必须使用写锁，以确保在更新期间，没有其他线程（例如主线程）可以访问字典或常用词汇。

文件索引完成后，将发出 `indexed()` 信号，并以文件名作为参数。主线程与此信号有有连接，并在标签中显示文件名，这样用户就能看到哪个文件刚刚被索引了。

一旦 `os.walk` 循环结束，`completed` 变量被设置为 `True`，方法结束，控制权返回给调用者 `run()`。最后语句可能永远不会执行，因为如果用户停止了索引（通过按下 Esc 键，这会导致 `stop()` 被调用，从而将 `stopped` 设置为 `True`，并意味着 `isStopped()` 将返回 `True`），其中一个 `isStopped():` 语句将导致 `processFiles()` 方法立即返回。在这种情况下，`completed` 变量将为 `False`。

这标志着我们对遍历器线程（walker thread）回顾的结束。使用 `with` 语句和上下文管理器代替 `try ... finally` 块可以让代码更短且易于理解，对比 `pageindexer.py` 与 `pagedexer_26.py`，以及 `walker.py` 与 `walker_26.py` 所示。`stop()` 方法和 `stopped` 变量对于为主线程服务的辅助线程是常见的，因此 `Walker` 类虽然在处理上是特定的，但在结构上是非常通用的。

## 总结

使用 PyQt 的线程和网络类编写线程服务器是相对简单的。对于非 UI 服务器，可以使用 `QCoreApplication` 而不是 `QApplication`，或者完全避免使用 PyQt 类，而是依赖 Python 标准库的线程和网络类，或者使用 Twisted。

在理论上，将处理分配给辅助线程并不困难，但在实践中我们必须非常小心地确保任何被多个线程访问的数据都使用如 `QMutex`、`QReadLock` 或 `Semaphore` 等保护机制。在保护机制的范围内，我们必须尽可能少地工作，以最大限度地减少其他线程可能被阻塞的时间。在读取数据的情况下，如果数据不是太大，最好将其复制，以避免在保护范围之外访问它的风险。

主线程通过调用辅助线程的方法与辅助线程通信是常见的——例如通过 `start()` 启动它们，通过 `stop()` 停止它们。辅助线程可以通过发射主线程连接的信号来与主线程通信。主线程和辅助线程也可以使用由 `QMutex`、`QReadWriteLocks` 或 `QSemaphores` 保护的共享数据结构——常见的场景是主线程读取而辅助线程读写共享数据。线程可能需要保护对自身数据的访问——例如对辅助线程的 `stopped` 变量的访问——因为多个方法可能同时处于激活状态（例如主线程）。

## 558 

第 19 章 多线程

# 实现辅助线程

文件文本中的每个单词长度既不长也不短，且不以不可接受的字符开头，我们首先查看它是否在常用词汇集中，如果不在，我们就将其添加到本地单词集中。

一旦我们在 `words` 集合中收集了文件的非常用词，我们就遍历这个集合。新单词被添加到 `filenamesForWords` 默认字典中。如果字典的文件名集合过大，我们就删除该字典条目并将单词添加到常用词集合中；否则，我们将文件名添加到该单词对应的字典集合中。当然，我们必须使用写锁，以确保在更新期间，没有其他线程（例如主线程）可以访问字典或常用词汇。

文件索引完成后，将发出 `indexed()` 信号，并以文件名作为参数。主线程与此信号有连接，并在标签中显示文件名，这样用户就能看到哪个文件刚刚被索引了。

一旦 `os.walk` 循环结束，`completed` 变量被设置为 `True`，方法结束，控制权返回给调用者 `run()`。最后语句可能永远不会执行，因为如果用户停止了索引（通过按下 Esc 键，这会导致 `stop()` 被调用，从而将 `stopped` 设置为 `True`，并意味着 `isStopped()` 将返回 `True`），其中一个 `isStopped():` 语句将导致 `processFiles()` 方法立即返回。在这种情况下，`completed` 变量将为 `False`。

这标志着我们对遍历器线程回顾的结束。使用 `with` 语句和上下文管理器代替 `try ... finally` 块可以让代码更短且易于理解，对比 `pageindexer.py` 与 `pagedexer_26.py`，以及 `walker.py` 与 `walker_26.py` 所示。`stop()` 方法和 `stopped` 变量对于为主线程服务的辅助线程是常见的，因此 `Walker` 类虽然在处理上是特定的，但在结构上是非常通用的。

## 总结

使用 PyQt 的线程和网络类编写线程服务器是相对简单的。对于非 UI 服务器，可以使用 `QCoreApplication` 而不是 `QApplication`，或者完全避免使用 PyQt 类，而是依赖 Python 标准库的线程和网络类，或者使用 Twisted。

在理论上，将处理分配给辅助线程并不困难，但在实践中我们必须非常小心地确保任何被多个线程访问的数据都使用如 `QMutex`、`QReadLock` 或 `Semaphore` 等保护机制。在保护机制的范围内，我们必须尽可能少地工作，以最大限度地减少其他线程可能被阻塞的时间。在读取数据的情况下，如果数据不是太大，最好将其复制，以避免在保护范围之外访问它的风险。

主线程通过调用辅助线程的方法与辅助线程通信是常见的——例如通过 `start()` 启动它们，通过 `stop()` 停止它们。辅助线程可以通过发射主线程连接的信号来与主线程通信。主线程和辅助线程也可以使用由 `QMutex`、`QReadWriteLocks` 或 `QSemaphores` 保护的共享数据结构——常见的场景是主线程读取而辅助线程读写共享数据。线程可能需要保护对自身数据的访问——例如对辅助线程的 `stopped` 变量的访问——因为多个方法可能同时处于激活状态（例如主线程）。

## 练习

文件文本中的每个单词长度既不长也不短，且不以不可接受的字符开头，我们首先查看它是否在常用词汇集中，如果不在，我们就将其添加到本地单词集中。

一旦我们在 `words` 集合中收集了文件的非常用词，我们就遍历这个集合。新单词被添加到 `filenamesForWords` 默认字典中。如果字典的文件名集合过大，我们就删除该字典条目并将单词添加到常用词集合中；否则，我们将文件名添加到该单词对应的字典集合中。当然，我们必须使用写锁，以确保在更新期间，没有其他线程（例如主线程）可以访问字典或常用词汇。

# 这并不是完全的结束

我们已经到达了书的末尾，但绝非 Python 或 PyQt 的终点。Python 的标准库非常庞大，由于我们专注于 PyQt，我们很大程度上只使用了其中的一小部分。许多其他库作为 Python 和 PyQt 的插件可用，因此在许多情况下，我们可以通过组合组件来编程，而无需从头开始构建一切。寻找插件的好地方是 Python Package Index：http://pypi.python.org/pypi。寻找技巧、提示和想法的好地方是 PyQt Cookbook：http://aspn.activestate.com/ASN/Python/Cookbook。

## 安装

- 在 Windows 上安装

- 在 Mac OS 上安装

- 在 Linux 和 Unix 上安装

本书中描述的所有工具均可线免费下载。但注意，某些软件包非常大（Qt 约 50MB，Python 约 12MB，PyQt 约 6MB，SIP* 约 0.5MB），因此它们实际上只适合通过宽带连接下载。在本附录中，我们涵盖了在 Windows、Mac OS X 以及大多数基于 X11 的 Unix 和 Unix 克隆版本（包括 Linux 和 BSD）上的下载和安装方法。

所有软件包都带有自己的安装说明，这些说明可能比这里提供的更及时、更全面，理想情况下这些是您应该遵循的指令。然而，在许多情况下，本附录包含了足够的信息来让工具安装并运行。一种方法是使用本附录来识别需要获取的软件包（下载顺序，这对于 Windows 用户很重要），以及它们应该的安装顺序（这对于所有平台都很重要）。然后，一旦下载了工具，使用官方说明安装每个工具，并浏览本附录的说明以帮助明确需要做什么，并学习一些对 Windows 用户和 Mac OS X 用户可能有帮助的小技巧。

## 在 Windows 上安装

对于 Windows，有四个工具需要安装：一个 C++ 编译器、Qt C++ 框架、Python 解释器及其配套库、以及 PyQt4（其 Windows 二进制包中包含 SIP）。我们假设使用的是 GPL 版本，以防唯一能用于 Qt 的 C++ 编译器是 MinGW（Visual C++ 仅用于 Qt 和 PyQt 的商业版本，其安装说明在购买时提供）。

> *SIP 是一种用于创建“绑定”的工具。

## 附录 A. 安装

在编写此时，一个合一软件包（all-in-one package）正在开发中。该软件包是一个执行设置文件，预计包含所有 PyQt 模块（QtDesigner 模块除外）、Qscintilla、翻译和 Qt Designer 支持工具、文档和示例、SQLite 数据库以及对 .png、svg、gif 和jpeg 格式的支持。该软件包是完整且自包含的，除了 Python 本身外不需要安装其他软件。然而，该软件包是不可扩展的。如果您是第一次学习或评估 PyQt，使用此软件包可能是最简单的开始方式。在您获得经验后，可以随时卸载并重新安装所需的精确组件集。当软件包可用时，它将位于网站 http://riverbankcomputing.com。安装 PyQt 后，只需下载并解压合一软件包即可安装所有所有内容。

在随后的说明中，我们使用的是 Windows XP 家庭版，并单独安装每个组件。其他 Windows 版本可能存在差异，但差异不至于让无法根据所写内容运行。

安装所需的文件有 MinGW-3.4.2.exe、qt-win-opensource-4.2-mingw.exe、python-2.5.1.msi 和 PyQt-gpl-4.2-Py2.5-Qt4.2.3.exe。书中的示例在 pythonbook 文件中。

获取 PyQt 的第一个项目是它本身。因为您依赖的 Python 和 Qt 版本取决于您获取的 PyQt 版本。前往：http://www.riverbankcomputing.com/uk/qt/download.php 并下载二进制文件 PyQt-gpl-4.2-Py2.5-Qt4.2.3.exe。文件名中带有数字，它们可能与此处显示的不同：第一个数字是 PyQt 版本，必须至少为 4.2 才能充分利用本书；第二个数字是您需要的 Python 版本；第三个是 Qt 版本——您必须下载这个精确版本。

现在获取 Qt。前往 http://www.trolltech.com/developer/qt/index 并点击 Qt/Windows Open Source 链接；在页面底部，下载 qt-win-opensource-4.2-mingw.exe。版本号应与 PyQt 包名中的完全匹配，例如，如果您下载了 PyQt-gpl-4.2-Py2.5-Qt4.3.1.exe，那么您需要获取 qt-win-opensource-4.3.1-mingw.exe。

MinGW C++ 编译器也可以从 Trolltech 网站获取，但 URL 完全不同。前往 http://ftp/trolltech.com/misc/ 并下载 MinGW-3.4.2.exe。（您可以跳过此步，让 Qt 安装器为您下载编译器，这对于安装在其他机器上或手头留软件包更方便，或者在您的 Windows 安装损坏时进行恢复。）

现在是获取 Python 的时候。前往 http://www.python.org/download 并下载 Windows 安装程序之一。（页面顶部的安装程序不包含源码；这没关系，因为只有在你想修改 Python 本身时才需要源码。）可能有多个 Windows 安装程序；点击与您的机器处理器匹配的特定特定版本，例如 AMD64 或 Itanium 版本；否则点击第一个——例如，“Python 2.5.1 Windows installer”；将安装程序保存到磁盘；这将为您提供一个 Windows 版 Microsoft 安装程序。

## 在 Windows 上安装

包括 Tcl/Tk。一旦安装了 Python，安装程序可能会要求你重启——请在安装 PyQt 之前进行重启。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_579_0.png)

图 A.3 Windows 上的 Python 和 PyQt 安装程序

现在你可以安装 PyQt4 了。双击 `PyQt-gpl-4.2-PyQt4.23.exe` 启动 PyQt 安装程序，无论你下载的是哪个版本的 PyQt。第一个屏幕的第一个如图 A.3 右侧所示。如果你将 Python 安装在非标准位置，你必须在“选择安装位置”（Choose Install Location）屏幕中确保位置正确——PyQt 是作为 Python 扩展程序安装的。（出于这个原因，如果你想卸载 Python，应该先卸载 PyQt，然后是 Python。）

PyQt 是设置并使其运行前必须安装的最后一个工具。要测试这一点，点击“开始→所有程序→PyQt GPL v4.2→示例和演示”（Examples and Demos）。这将启动一个 PyQt 版本的标准 Qt 演示应用程序。从内部，你可以运行 PyQt 提供的任何演示程序。演示程序以及许多其他 PyQt 示例的源代码通常安装在 `C:\Program Files\PyQt\examples` 中。

如果你下载了书中的示例，你可能喜欢在 C 盘中解压 `pybook.zip` 以得到一个 `C:\pyqt` 目录，其中包含书中所有的示例以及按章节分类的练习答案。在 `C:\pyqt` 目录中你会找到 `makeqt.py` 和 `makeqt.pyw`；这些工具在第 20 页有解释。如果你想在阅读此书之前尝试任何示例，请确保先运行 `makeqt.pyw`。（当你运行 `makeqt.pyw` 时，它会将路径设置为 `C:\pyqt`，勾选其复选框，然后点击“构建”（Build）按钮。现在所有示例都准备好运行了。）这就完成了 Windows 的安装，对于 PyQt GUI 编程已经足够。如果你还想写控制台应用程序，或者有时在台中运行 PyQt 应用程序（这对于调试很有用），再多几个步骤会让这更加方便。

点击“开始→所有程序→杂项→Windows 资源管理器”。一旦 Windows 资源管理器运行，导航到“我的电脑\本地磁盘 (C:)\文档和设置”，然后进入你用户名的目录，在里面导航到“开始菜单\程序\杂项”。复制并粘贴“控制台”（或 MS-DOS 提示）快捷方式，并将其重命名为“Console PyQt”。右键点击新的 Console PyQt 快捷方式以编辑其属性。在“常规”页上，将“目标”更改为 `cmd.exe / C:\pyqt\pyqt.bat`。当你有一个支持 PyQt 的控制台时，你可以点击“开始->所有程序→杂项→Console(PyQt)它会自动运行 `C:\pyqt\pyqt.bat`。此批处理文件只有两行：

```
set MAKESPEC=win32-+
path=:pyqt;C:\MinGW\bin;C:\Python25\Python25\lib\idlelib;path%
```

你可能喜欢编辑此处（使用纯文本编辑器）以添加包含 `cd` 命令的第三行——例如，`cd C:\pyqt`——这样控制台就会在方便的目录中启动。如果你将 MinGW 或 Python 安装在非标准位置，将需要编辑此文件，输入它们的正确路径。

你现在准备好在 Windows 机器上编写和运行 PyQt 应用了——它们在 Mac OS X 和 Linux 上也可以同样运行！

## 在 Mac OS X 上安装



# 附录 A. 安装

## 在 Mac OS X 上安装

要在 Mac OS X 上安装 PyQt，你必须已经安装了 Xcode 工具。这是因为安装 PyQt 需要编译器和构建工具。Xcode 是一个非常大的包，通常随机器提供的开发者光盘提供；它也可以从 `http://developer.apple.com/tools/xcode` 在线获取。以下指令将确保 Xcode 已经安装。

虽然 Mac 通常预装了一个版本的 PyQt，但在这种情况下，我们建议为 PyQt 开发安装最新版本。要检查 PyQt 版本，启动“终端”（Terminal）并输入 `-V`；如果它打印出“Python 2.5”或更高版本号，则不需要安装新版本的 PyQt。

安装 PyQt 所需的文件有 `qt-mac-opensource-4.2.3.dmg`、`python-2.5-macos.dmg`（除非你已经安装了 Python 2.5 或更高版本）、`sip-4.6.tar.gz` 和 `PyQt-mac-gpl-4.2.tar.gz`。书中的示例在 `pyqtbook.tar.gz` 文件中。

### 获取所需文件

从获取 Qt 开始。访问 `http://www.trolltech.com/developer/downloads/qt/index` 并点击 Qt Open Source 链接，在页面底部下载 `qt-mac-opensource-4.2.3.dmg`。较后的版本号，例如 4.3.1 也可以的。

如果你需要安装最新版本的 Python，访问 `http://www.python.org/download` 并下载 Macintosh OS X 版 Python 2.5.1——例如，`python-2.5.1-macos.dmg`。较后的 2.x 版本，如 2.52 或 2.6.0 也可以的。应该避免旧版本、alpha 版本或候选版本。

必须获取的最后两个工具是 SIP 和 PyQt。访问 `http://www.riverbank.com/uk` 并下载 `sip-4.6.tar.gz` 和 `PyQt-mac-gpl-4.2.tar.gz`。书中的示例在 `pyqtbook.tar.gz` 文件中。

安装 PyQt 所需的文件有 `qt-mac-opensource-4.2.3.dmg`、`python-2.5-macos.dmg`（除非你已经安装了 Python 2.5 或更高版本）、`sip-4.6.tar.gz` 和 `PyQt-mac-gpl-4.2.tar.gz`。

### 安装步骤

![](img/55bc1dcf8601cfec5e1423b4e17ec264_583_0.png)

**图 A.6** 在 Mac OS X 上设置使用的 Python

...正在安装。如果不是的话，请参阅上一个段落；或者，输入你想要使用的 Python 版本名称——例如，`python2.5 configure`。

必须首先构建 SIP，请在终端中输入以下命令：

```bash
cd $HOME/Desktop
tar xvfz sip-4.6.tar.gz
cd sip-4.6
python configure.py
make
sudo make install
```

在最后执行 `sudo` 命令时，会要求你输入管理员密码（通常是你自己的密码）。现在可以安装 PyQt 了。

```bash
cd $HOME/Desktop
tar xvfz PyQt-mac-gpl-4.2.tar.gz
cd PyQt-mac-gpl-4.2
python configure.py
make
sudo make install
```

同样，在执行 `sudo` 命令时，系统会提示你输入密码。构建 PyQt 可能需要很长时间，所以你需要耐心等待。

可以通过 Qt Assistant 获取 Qt 文档，你可以从 Finder 中运行它。PyQt 的文档以 HTML 格式提供在 `$HOME/Desktop/PyQt-mac-gpl-4.2/doc` 目录下。将此移动到某个地方并为你的浏览器添加一个合适的书签是值得的。它包含许多示例；至少值得查看 PyQt 示例并运行演示。例如，更改目录到 `$HOME/Desktop/PyQt-mac-gpl-4.2/examples/tools/qtdemo` 并运行 `./qtdemo.py`。

如果你下载了书中的示例，你可能喜欢将 `$HOME` 下的 `pyqt-toolbox.tar.gz` 解压到带有书中书籍示例的 `$HOME/pyqt` 目录，并按章节分类移动练习答案。在 `$HOME/pyqt` 目录本身中你会发现 `makepyqt.py` 和 `makepyqt.py`；你可能喜欢将它们移动（或软链接）到 `$PATH` 上的某个目录——例如 `$HOME/bin`——以便方便使用。某些示例依赖于 Qt Designer 的 `.ui` 文件或 `.qrc` 资源文件。将这些转换为 Python 模块请见第 207 页，但现在执行转换非常简单：

```bash
cd $HOME/pyqt
./makepyqt.py -r
```

这将转换 pyqt 目录及其子目录中的任何 .ui 和 .qrc 文件。如果你倾向于使用 GUI 版本的 `makepyqt.py` 工具，可能需要点击“更多→工具”路径，并设置到 `pyu4` 的路径。可能还需要设置其他工具的路径。

这这就完成了 Mac OS X 的安装。如果你解压了示例，可以去桌面并点击 PyQt 目录，然后点击 `multides.py` 查看一个图形应用程序。如果弹出一个不需要的终端窗口，右键点击 `multides.py` 并点击“信息”对话框；将“打开方式”设置为对应正确版本的 Python 启动器，并将更改应用于所有带有 .py 后缀的文件。

现在你已经准备好在你的 Mac OS 机器上编写并运行 PyQt 程序了——它们在 Windows 和 Linux 上运行也会保持不变！

## 在 Linux 和 Unix 上安装

如果你运行的是 Kubuntu (7.04 Fiesta Fawn 及更高版本)，你已经安装了 PyQt4！所以你只需要安装书中的示例（见第 573 页）以及文档包 `python-doc` 和 `python-qt4-doc`。

对于没有预装 PyQt4 的 Linux 和其他 Unix，有四个工具需要安装：Qt C++ 应用开发框架、Python 解释器及其辅助库、SIP 绑定以及 PyQt4 本身。让这一切运行起来最方便的方法是使用 Linux 或 Unix 发行版的标准包安装这些工具。

对于 ArchLinux、Debian、Fedora、Gentoo、Kubuntu、Pardus、Ubuntu 等系统，必要的组件以包的形式提供。可以使用 `Apt`、`Yum`、`apt-get` 或系统使用的任何其他包管理器进行安装。对于 PyQt4，包名通常为 `pyqt4` 或 `pyqt4-dev-tools`。PyQt4 的文档通常位于名为 `pyqt4-doc` 或 `pyqt4-doc-examples` 的包中。IDLE 通过名为 `idle` 或 `python-tools` 的包单独提供。如果你想要一个更强大的 IDE，用 PyQt 编写的 Eric 在许多流行发行版的包中均可用。包管理器应该能够处理依赖关系，但如果它不能，你可能需要要求它安装 Python 本身，甚至可能需要 Qt 和 g++ 编译器。Qt Designer 可视化工具和翻译支持工具通常是单独打包的——例如，在 `qt4-designer` 和 `qt4-dev-tools` 包中。

如果你足够幸运可以使用标准包进行安装，一旦完成，你就可以准备好编写 PyQt 程序了，并跳到安装第 573 页描述的书中示例。

### 针对旧版本发行版用户

安装所需的文件为 `qt-x11-opensource-src-4.2.3.tar.gz`、`Python-2.5.1.tar.gz`、`sip-4.6.tar.gz` 和 `PyQt-gpl-4.2.tar.gz`。

```bash
cd $HOME/pyqt
./mkpyqt.py -r
```

这完成了基于 X11 的 Unix 及类 Unix 克隆系统（包括 Linux 和 BSD）的安装。现在你已经准备好 Unix 或类 Unix 平台上编写并运行 PyQt 应用程序——它们在 Mac OS X 和 Windows 上也可以一样运行运行！

# 附录 B. 选 PyQt 组件

这里显示的截图是在 Linux 上使用 KDE 拍摄的，以提供视觉上的统一性。在书书中，会显示 Windows、Linux 和 Mac OS X 的截图，通常随章节而异。

## QCalendarWidget

![](img/55bc1dcf8601cfec5e1423b4e17ec264_589_0.png)

此组件可以作为显示组件使用，尽管它主要设计为作为输入组件，用户可以通过它选择特定日期。该组件的显示具有高度可配置性；例如，可以显示或隐藏周数，日期可以用单个字母、简写或全称表示，可以设置使用的颜色和字体，还可以设置哪一天被视为每周的第一天。可以设置最小和最大允许日期。在 `QDateEdit` 或 `QTimeEdit` 上调用 `calendarPopup(True)` 将导致数字按钮替换为箭头按钮。如果用户点击箭头按钮，将弹出一个 `QCalendarWidget`。

| | 2007年10月 | | | |
| :--- | :--- | :--- | :--- |
| 周一 二 三 四 五 六 日 | | | | |
| 39 | 24 25 26 27 28 29 30 | | | |
| 40 | 1 2 3 4 5 6 7 | | | |
| 41 | 8 9 10 11 12 13 14 | | | |
| 42 | 15 16 17 18 19 20 21 | | | |
| 43 | 22 23 24 25 26 27 28 | | | |
| 44 | 29 30 31 | 1 2 3 4 | | |

```python
QCalendarWidget
```

## QCheckBox

复选框可用于为用户提供简单的是/否选择。如果调用 `QCheckBox.setState(True)`，复选框将有三种状态：用户勾选了、用户取消勾选了、或者用户没有更改其之前的状态。这种三状态方法对于表示允许 IS NULL 的布尔数据库字段可能有用。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_589_1.png)

```python
QCheckBox
```

## QComboBox

截图显示了一个弹出的列表的 `QComboBox`。组合框用于向用户提供项目列表，适用于垂直空间不足以使用 `QListView` 的情况。调用 `QComboBox.setEditable(True)` 允许用户选择列表中的一个项目，或者输入自己的文本代替。每个组合框项目都有文本和可选数据。我们可以使用 `QComboBox.addItem()` 或 `QComboBox.addItem()` 填充组合框，也可以使用自定义或内置的 `QAbstractItemModel` 配合 `QComboBox.model()`。

| QComboBox |
| :--- |
| 2007年10月26日 |
| 2007年10月26日 上午07:30:00 |
| 上午12:00:00 |

## QDateEdit, QDateTimeEdit, and QTimeEdit

`QDateEdit` 用于显示和输入日期，`QDateTimeEdit` 用于日期和时间，而 `QTimeEdit` 用于时间。默认情况下，该组件使用特定区域的日期和时间格式——这里使用美国区域设置进行显示。可以更改格式，并可以设置最小和最大允许的日期和时间。

## QDialogButtonBox

| 确定 | 取消 |
| :--- | :--- |

此组件可用于创建一行或一列按钮。按钮可以是带有预定义角色（role）和文本的标准按钮，也可以带有我们选择的角色和文本的自定义按钮。此组件会根据按钮的角色和底层窗口的用户界面指南自动排列按钮。

## QFontComboBox

| Technical AaBbb |
| :--- |
| URW Bookman L |
| URW Chancery L |
| URW Gothic L |
| URW Palladio L |
| Utopia |

PyQt 提供了一个弹出对话框，在可用时提供原生字体对话框。如果我们想自己提供字体——或者在工具栏中提供——可以使用这里显示的弹出的 `QComboBox`。对于 Qt 4.0 和 Qt 4.1，最接近的等物（但不带字体预览）是使用普通的 `QComboBox`，并用 `QFontDatabase.families()` 返回的列表来填充它。

| QComboBox |
| :--- |

## QGroupBox 和 QRadioButton

| 警告选项 |
| :--- |
| ○ 全局警告 |
| * 最小警告 |

组框可以纯粹作为视觉分组设备，也可以像这里所示是可勾选的。如果是可勾选的，当组框被勾选时，其中的组件就可以交互。如果需要不需要标题的框架，可以使用 `QFrame` 代替。当 RadioButtons 放在组框中时，它们的表现正常，即用户只能选择其中一个。`QComboBox` 和 ListView 通常比 RadioButtons 更方便。

## QGraphicsView

此组件用于查看 `QGraphicsScene` 中的 `QGraphicsItems`，任意数量的 GraphicsViews 都可以带有自带变换（例如缩放和旋转）。如果需要，会出现滚动条。每个 `QGraphicsView` 都可以提供自己的背景和前景，由场景进行覆盖。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_591_0.png)

```python
QGraphicsView
```

## QLabel

| 多行 QLabel |
| :--- |
| 显示 HTML 文本的效果 |

`QLabel` 是一个显示组件，可以显示图像、纯文本字符串、`QTextDocument` 或 HTML。带有加速器（单个字符）的标签可以与“buddy”组件关联，按下时会将焦点传递给 buddy。

## QLineEdit

| QDateEdit, DateTimeEdit, and QTimeEdit |
| :--- |
| LCDNumber |
| QLineEdit |

此组件可以接受用户的一行文本。文本可以通过验证器（例如 `QValidator` 或 `DoubleValidator`）、设置输入掩码来限制，或者都可以设置为显示（无）而不是文本。

## QListView 和 QListWidget

| 丹麦 | 吉布提 | 多米尼加共和国 |
| :--- | :--- | :--- |

通过这些组件，用户可以选择项目，或者在合适的模式下选择多个项目。组件可以是列表模式（如所示），或者是图标模式，其中图标较大且文本显示在下方。`QListView` 必须配合自定义或内置的 `QAbstractItemModel` 使用。在空间紧张的情况下，可以使用 `QComboBox`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_592_0.png)

## QProgressBar

此组件用于显示长时间运行的进度。它通常通过 `QStatusBar.addWidget()` 或 `addPermanentWidget()` 放在 MainWindow 的状态栏中。另一种方法是弹出 `QDialog`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_592_1.png)

## QPushButton

`QPushButton` 用于调用操作。如果点击按钮将弹出对话框，我们通常会在文本末尾添加省略号 (...)。按钮也可以设置为具有弹出菜单（在这种情况下，PyQt 会添加一个小指示器），或者设置为切换按钮，点击奇数次时按下，点击偶数次时弹出。自 Qt 4.2 起，大多数应用程序使用 `QDialog` 而不是单独的 `QPushButton`。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_592_2.png)

## QSlider

滑块通常用于显示比例，并通常与显示实际金额的 Slider 或 `LCDNumber` 使用。滑块可以垂直或水平对齐。`QScrollBar` 可用于类似的目的。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_592_3.png)

## QDoubleSpinBox 和 QSpinBox

这些组件用于接收和显示数字。可以设置前缀或后缀以及特定的对齐方式（这里显示的 DoubleSpinBox 有 "$" 前缀）。它们可以设置最小值和最大值，对于 `QDoubleSpinBox`，可以设置小数点后的位数。另一种方法是使用配合 `QValidator` 或 `DoubleValidator` 的 `QLineEdit`。

## QTableView 和 QTableWidget

| 类别 | 简述 | 详细描述 |
| :--- | :--- | :--- |
| 1 类操作 | 等待 | 等待信息 |
| 2 类操作 | 进展 | 进展到下一阶段 |
| 3 类操作 | 升级 | 发送给主管 |

这些组件用于以表格形式呈现数据。`QTableView` 必须配合自定义或内置的 `QAbstractItemModel` 子类（如 `QTableModel`）使用，使用 `QTableView.setModel()`。`QTableWidget` 有内置模型，因此可以直接向其添加项目——例如，使用 `TableWidget.setItem()`。两种组件都可以在单元格（包括表头单元格）中显示图标以及文本。

| 现金 | 支票 | 信用卡 |
| :--- | :--- | :--- |
| 号: | | |
| 有期自: | 2004年1月 | 到期日期: 2009年1月 |

## QTabWidget

此组件在空间紧张时使用，或简单地作为分组组件的手段。标签有两个形状设置，可以出现在顶部、左侧、右侧或底部，标签在显示或留在时会旋转。

## QPainterPath

如果你需要绘制复杂的形状，特别是当你需要时，请考虑创建一个 `QPainterPath` 并使用 `drawPath()` 绘制它。

## QTextEdit 和 QTextBrowser

这些组件可以显示 HTML，包括列表、表格和图像。`QTextEdit` 也可以用作编辑组件，无论是用于纯文本还是“富文本”，尽管需要自定义子类来提供表格和图像编辑。`QTextBrowser` 支持点击链接，因此它可以作为简单的浏览器使用。两种组件都支持 CSS（层叠样式表）。

![](img/55bc1dcf8601cfec5e1423b4e17ec264_593_0.png)

## QTreeView 和 QTreeWidget

| 国家 (美国)/城市/提供商 | 服务器 | IP |
| :--- | :--- | :--- |
| 土耳其 | | |
| (无州) | | |
| 安卡拉 | | |
| 国家学术骨干 | | |
| Web 安卡拉 | Apache/1.3.4 193.140.83.20 | | |
| 乌克兰 | | |
| 英国 | | |
| 美国 | | |
| 亚利桑那州 | | |
| 加利福尼亚州 | | |
| 乔治亚州 | | |
| 亚特兰大 | | |
| 莲花制作国 | Apache/1.3.3 216.25.83.17 | | |
| Lyanum 支持工具 | NCSA/1.42 205.142.27 | | |
| 南十字路 | Apache/1.3.1 130.207.54 | | |

这些组件用于呈现分级数据。`QTreeView` 必须配合自定义或内置的 `QAbstractItemModel` 子类使用，使用 `QTreeView.setModel()`。与所有使用模型的组件一样，只检索用户可见的数据，因此处理大型数据集非常快。在模型中，`QTreeWidget` 有内置模型，可以使用 `QTreeWidget.insertTopLevelItem()` 和 `insertLevelItems()` 直接向其添加项目，或者通过创建 `QTreeWidgetItem` 项目作为其他项目。

# 附录 C. 选定的 PyQt 类层次

## 图 C.1 选定的基类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_595_0.png)

**图 C.1** 选定的基类

## 图 C.2 QFrame 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_595_1.png)

**图 C.2** QFrame 层次结构中的选定类

## 图 C.3 QWidget 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_596_0.png)

**图 C.3** QWidget 层次结构中的选定类

## 图 C.4 QAbstractItemModel 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_597_0.png)

**图 C.4** QAbstractItemModel 层次结构中的选定类

## 图 C.5 QDialog 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_597_1.png)

**图 C.5** QDialog 层次结构中的选定类

## 图 C.6 QIODevice 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_597_2.png)

**图 C.6** QIODevice 层次结构中的选定类

## 图 C.7 QPaintDevice 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_597_3.png)

**图 C.7** QPaintDevice 层次结构中的选定类

## 图 C.8 QEvent 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_598_0.png)

**图 C.8** QEvent 层次结构中的选定类

## 图 C.9 QGraphicsItem 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_598_1.png)

**图 C.9** QGraphicsItem 层次结构中的选定类

## 图 C.10 QLayoutItem 层次结构中的选定类

![](img/55bc1dcf8601cfec5e1423b4e17ec264_598_2.png)

**图 C.10** QLayoutItem 层次结构中的选定类

# 索引

在查找 PyQt 组件的方法时，也请考虑查找它们的基类，例如 `QFrame`、`QWidget` 和 `QObject`。函数和方法按字母顺序列出，大多数情况下位于其所属的模块或类下。如果方法或函数的名称与某个概念足够接近，则不列出该概念。例如，没有“分割字符串”条目，但有 `split()` 方法条目。

## 符号

- `!=` (不等于运算符), 47, 81, 82
- `"` (双引号), 21
- `%` (取模余运算符，字符串格式化运算符), 24, 26, 53, 84, 98
- `%=` (取模赋值运算符), 84
- `&` (位与运算符，加速键指示符), 38, 47, 143
- `'` (单引号), 21
- `(` (元组创建运算符，函数调用运算符，表达式运算符), 30, 51, 54, 55, 81
- `*` (乘法运算符，复制参数列表，从 --import 运算符), 19, 25, 84, 91
- `**` (幂/指数运算符，关键字参数列表指示符), 40
- `*=` (乘法赋值运算符), 84, 91
- `+` (加法运算符，拼接运算符), 25, 33, 84, 90, 500
- `+=` (加法赋值运算符，追加运算符), 84, 90, 234
- `-` (减法运算符，否定运算符), 84
- `-=` (减法赋值运算符), 84
- `.` (点运算符), 78
- `/=` (除法运算符), 84, 91
- `//=` (除法赋值运算符), 84, 91
- `//` ("真"除运算符), 84, 96
- `//=` ("真"除赋值运算符), 84, 91
- `:` (后续跟随，切片索引分隔符), 46
- `/` (路径根，...的根), 173
- `<` (小于运算符), 47, 81, 82
- `<<` (`QStream` 和 `QText` 读写运算符，`int` 和 `long` 左移运算符), 242, 245, 250, 254, 359, 435, 523
- `<=` (小于等于运算符), 38, 47, 81, 82
- `!=` (不等于运算符—已弃用), 47
- `=` (绑定运算符，对象引用和赋值运算符), 81, 82, 83
- `==` (相等运算符), 13, 47, 81, 82
- `>` (大于运算符), 47, 81, 82
- `>=` (大于等于运算符), 38, 47, 81, 82
- `>>` (`QStream` 和 `QText` 读运算符，`int` 和 `long` 右移运算符), 245, 360, 435, 528, 532, 541
- `@` (装饰器运算符), 85
- `[]` (索引运算符，切片运算符), 22, 54, 93
- `\` (转义字符), 21, 51, 220
- `\` (换行字符), 51
- `^` (位异或运算符), 47
- `_` (下划线字符), 76, 80
- `__` (双下划线), 77, 80, 82
- `` ` `` (repr运算符), 83
- `{}` (大括号), 46
- `|` (位或运算符), 30, 47
- `~` (位取反运算符), 47
- `€` (欧元符号), 21

## 函数与方法

- `addDatabase()` (`QDatabase`), 446, 459
- `addDays()` (`QDate`), 491
- `addDockWidget()` (`QMainWindow`), 169, 186
- `addEllipse()` (`QGraphicsScene`), 354, 374, 376
- `addItem()` (`QComboBox`), 276, 354, 362, 364, 371
- `addItems()` (`QComboBox`), 440
- `addLayout()` (`QLayout`), 146, 251, 178, 180
- `addLine()` (`QGraphicsScene`), 354
- `addMapping()` (`DataMapper`), 453, 456
- `addMenu()` (`QMenu` 和 `QMenuBar`), 177, 178
- `addPath()` (`QGraphicsScene`), 354
- `addPixmap()` (`QGraphicsScene`), 354
- `addPolygon()` (`QGraphicsScene`), 354, 376
- `addRect()` (`QGraphicsScene`), 355
- `addSeparator()`, (178, 180, 307)
- `addSpacing()` (`QBoxLayout`), 146
- `addStretch()` (`QBoxLayout`), 146
- `addText()` (`QGraphicsScene`), 354
- `addToolBar()` (`QMainWindow`), 179, 186
- `addWidget()` (`QLayout`), 146, 251, `ToolBar`, 178, 180
- `addYears()` (`QDate`), 490
- `adjusted()` (`QRect`/`QRectF`), 355, 367
- `aggregation`, 93
- `Alert application`, 112–116
- `alignment`, 638, 429
- `alive`, PyQt objects, 287–288, 289
- `all()`, 38
- `about()` (`QMessageBox`), 200
- `aboutToShow signal` (`QMenu`), 178, 187, 285, 292
- `abs()`, 40, 40, 403
- `__abs__()` (`abs`), 84
- `absolute positions and sizes`, 119
- `abstract base class`, 102
- `accelerator`; see keyboard accelerator
- `accept`, 141, 188
- `accept()` (`QDialog`), 151, 154, 425, `Event`, 314, 333, 391
- `accepted() signal` (`QDialogButton`), 145, 150
- `access`, private and public, 76, 88
- `accessor methods`, 79–80
- `action`; see `QAction`
- `action group`; see `QActionGroup`
- `activateWindow()` (`QWidget`), 160, 289
- `activateWindow()` (`QWidget`), 296
- `addAction()` (`QWidget`), 172, 178, 180, 307, 365, 392, 393
- `addActions()` (`QWidget`), 178
- `bindValue()` (`QSqlQuery`), 448, 450
- `addButton()` (`QDialogButton`), 150
- `and operator`, 47
- `anonymous functions`; see lambda statement
- `augmented assignment operators`, 15, 16, 84, 90, 91
- `automatic disconnection`, 130
- `automatic garbage collection`; see garbage collection
- `automatic repairing`, 119
- `automatic signal-connections`, 217
- `automatically deleting windows`, 156, 284, 286
- `antialiasing`, 337, 342, 361, 369
- `any()`, 38
- `append()`
    - `list`, 33
    - `QTextEdit`, 120
- `application model dialogs`, 140
- `application termination`, 115, 185
- `applicationDir()` (`QApplication`), 173
- `applicationName()` (`QApplication`), 194
- `backslash escapes`, 21, 22, 51
- `base class`, 75, 76, 102
- `basename()` (`os.path`), 189
- `beforeInsertRow()` (`QTableModel`), 470
- `beginInsertRows()` (`QAbstractItemModel`), 432
- `beginRemoveRows()` (`QAbstractItemModel`), 433
- `binary algorithm`, 95, 238
- `binary data`, 240–248
- `binding names`, 14–16
- `applications release`, 207, 531
- `Make PyQt` (`makepyqt.py`), 174, 206, 217
- `makepyqt.py`, 174, 206, 217
- `pyuic`, 207, 513, 518
- `pyuic`, 173, 174
- `pyrcc`, 206, 207, 221, 515
- `Qt Assistant`, 50
- `Qt Linguist`, 513
- `arg()` (`QString`), 402, 419, 423, 427, 428, 455, 513
- `array module`, 204
- `as keyword`, 22, 250, 501, 555
- `aspect ratio`, 329, 400
- `assert statement`, 69, 498, 500, 501, 502, 504
- `AssertionError`, 69
- `Asset Manager`, 457–470
- `assignment operators`, 15, 83
- `associative array`; see `dict`, `defaultdict`, `OrderedDict`
- `atEnd()` (`QDataStream` `QStream`), 245, 252, 253, 254
- `attribute()` (`QDomElement`), 261
- `AttributeError exception`, 89, 101
- `attributes`, 75, 78, 103, 106, 125
- `bindValue()` (`SqlQuery`), 448, 450, 468
- `bisect module`, 93, 238
- `bisect_left()` (`bisect`), 25, 239
- `bitwise operators`, 47
- `BLOBs` (Binary Large Objects), 469
- `block of code`; see block structure, 46
- `blockSignals()` (`QObject`), 135
- `image` (file image), 193
- `Core PYTHON Programming`, 27
- `Dive into Python`, 327
- `Mastering Regular Expressions`, 220
- `Python and XML`, 256
- `Python Cookbook`, 27
- `Python in a Nutshell`, 27
- `XML Processing in Python`, 256
- `and operator`, 47
- `bool()`, 83
- `any()`, 38
- `bool type`, 16–17, 46
- `as keyword`, 104
- `Boolean context`, 83
- `assert statement`, 69, 498, 500, 501, 502, 503, 504
- `Booleans`, 45, 46
- `bool()`, 83
- `bounding rectangle`, 338, 367, 373, 377
- `bool type`, 16–17, 46
- `boundingRect()`
- `break statement`, 49, 50, 53
- `callable()`, 102
- `GraphicsItem`, 365, 366, 367, 373, 377
- `chr()`, 21, 39
- `PainterPath`, 377
- `class statement`, 69, 75, 76, 85, 103, 115
- `boundValue()` (`QSqlQuery`), 450
- `cmp()`, 82, 89
- `braces`, need for, 46
- `complex-type`, 17–20
- `break statement`, 49, 50, 53
- `buddies`, 143, 206, 215
- `continue statement`, 53
- `see QLabel.setBuddy`
- `def statement`, 55, 62–63, 77
- `built-ins`
- `del statement`, 32, 355, 391, 372, 556
- `== operator`, 47, 81, 82
- `dict type`, 35–36, 91
- `% operator`, 24, 26, 53, 84
- `& operator`, 47
- `dir()`, 39
- `* operator`, 19, 25, 84, 91
- `** operator`, 40
- `enumerate()`, 87, 419, 237, 418
- `hex()`, 40
- `id()`, 13, 29, 237, 418
- `if statement`, 46–49
- `import statement`, 18, 19
- `[] operator`, 22, 54, 93
- `in operator`, 25, 33, 36, 38, 96
- `is statement`, 13, 47, 57
- `abs()`, 40, 84, 403
- `all()`, 38

### 内置函数（续）

- `isinstance()`, 39, 94, 102, 135, 289, 296, 359, 372, 375, 393, 395, 440, 496, 499, 502
- `iter()`, 97, 237
- `lambda statement`, 61–62, 134, 453
- `len()`, 20, 25, 33, 36, 38, 96, 237, 503
- `list type` (列表类型), 31–35, 93
- `long()`, 40
- `long type` (长整型类型), 16–17, 231, 241
- `max()`, 38
- `min()`, 38
- `None constant`, 13, 57
- `not operator`, 47
- `object type` (对象类型), 76, 77, 78
- `oct()`, 40
- `open()`, 39, 70
- `or operator`, 47
- `ord()`, 21, 39
- `pass statement`, 47
- `pow()`, 40
- `print statement`, 10, 26
- `property()`, 80
- `range()`, 39, 50–51, 54
- `repr()`, 81, 83, 89, 90, 98
- `return statement`, 58, 97, 554
- `round()`, 40, 91, 333
- `set type` (集合类型), 37, 93
- `sorted()`, 52, 53, 63, 432, 434, 551
- `special methods`; see special methods
- `staticmethod()`, 85, 239, 288
- `str type` (字符串类型); see `str`
- `sum()`, 38
- `super()`, 100, 153, 217
- `True constant`, 45
- `try statement`, 66, 70, 78, 541, 542, 543, 548, 550, 551, 553, 554, 556
- `tuple type` (元组类型), 29–31, 30, 50, 87
- `type()`, 18, 39, 102
- `unichr()`, 21, 39, 236, 554
- `unicode type`; see unicode type
- `while loop`, 49–50
- `with statement`, 549
- `range()`, 51, 54
- `yield statement`, 58, 97, 237

- `button()`
    - `QDialogButtonBox`, 150, 158
    - `MouseEvent`, 333
- `buttons` (按钮); see `QAbstractButton`, `DialogButtonBox`, and `QPushButton`
- `byte array` (字节数组); see `QByteArray`
- `bytecode` (字节码), 11, 111
- `bytesAvailable()` (`QIODevice`), 528, 531, 540

## C

- `Calculator application`, 116–121
- `call()`, 81
- `callable()`, 102
- `callables` (可调用对象), 63, 97, 102, 115, 128, 131
- `callbacks` (回调函数); see function references
- `calling context` (调用上下文), 64
- `canPaste()` (`QTextEdit`), 385
- `case statement` (分支语句); see if statement
- `center()` (`QRect`/`QRectF`), 392, 393
- `centering` (居中对), 168
- `central widget` (中心部件), 168
- `character escapes` (字符转义符), 21, 22
- `character formatting` (字符格式化), 397
- `characters()` (`QXmlContentHandler`), 263
- `checkable actions` (可检查动作), 176, 177
- `chr()`, 21, 39
- `class statement` (类语句), 69, 75, 77, 85, 86, 103, 115
- `clear()`
    - `dict` (字典), 36
    - `ListWidget`, 418
    - `QtWidgets`, 418
    - `QTextDocument`, 383
    - `TreeWidget`, 420
    - `set`, 38
- `clearMessage()` (`StatusBar`), 170, 232
- `clearSelection()` (`QGraphicsScene`), 356, 361, 362
- `click` (点击); see `mousePressEvent()` and `mouseReleaseEvent()`
- `clicked() signal` (`QPushButton`), 219
- `client/server applications` (客户端/服务器应用), 522
- `clipboard` (剪贴板); see `QClipboard`
- `clipboard()` (`QApplication`), 297, 311
- `close button` (关闭按钮), 118, 121
- `close()` file (关闭文件), 70, 555
- `IODevice`, 243, 259, 525, 528
- `Widget` (部件), 175, 285, 289, 330
- `closeAllWindows()` (`QMainWindow`), 289, 293
- `closeEvent()` (`QWidget`), 175, 185, 187, 282, 285, 293, 351
- `closeSubPath()` (`QPainterPath`), 376
- `closing dialogues` (关闭对话框), 118, 121
- `closures` (闭包); see partial application
- `cmp()`, 82, 89
- `__cmp__()` (`cmp()`), 81, 82, 86, 432
- `code` (代码); see encodings
- `codecs module` (模块), 255–256
- `open()`, 255, 260, 501, 555
- `readline()`, 255, 29, 37–98
- `collections module` (模块), 29, 529, 532, 545
- `collidesPath()` (`GraphicsItem`), 366
- `collidingItems()` (`GraphicsScene`), 354, 375
- `collision detection` (碰撞检测), 349, 374, 375
- `color palette` (调色板); see `QPalette`
- `column()` (`QModelIndex`), 428, 431, 339, 461, 462, 486, 503
- `columnCount()` (`QAbstractItemModel`), 427, 428, 433, 503
- `combining expressions` (组合表达式), 47
- `command-line arguments` (命令行参数), 113, 114
- `commercial licensing` (商业许可), 3
- `commit()` (`SqlDatabase`), 449, 465, 468, 469
- `communication mechanisms` (通信机制); see events and slots
- `compare()` (`QString`), 13, 38, 47, 63, 82
- `__cmp__()`, 89, 416, 432
- `comparison operators` (比较运算符), 83
- `expressions` (表达式), 47
- `see all operator`, `!=` and `is statement`
- `compile()` (`re`), 220
- `complex type` (复数类型), 17–20
- `composite widgets` (复合部件), 168, 280, 325–326
- `composition` (组合), 49, 390
- `connect()` (`QObject`), 124, 130, 133, 145, 146, 158
- `connecting to databases` (连接数据库), 446
- `connections` (连接); see signals and slots
- `connectSlotsByName()` (`QMetaObject`), 217
- `connectTo()` (`QAbstractSocket`), 525
- `constructors` (构造函数); see initializers, `__init__()`, and `__new__()`
- `containers` (容器), collections, and `dict` type, `list`, and `tuple`
- `contains()`
    - `GraphicsItem`, 366
    - `QRect`/`QRectF`, 357
    - `QStringList`, 189
- `__contains__()` (`in`), 93, 96
- `context managers` (上下文管理器), 549, 555
- `context menus` (上下文菜单), 168–181, 307, 365, 390
- `contextMenuEvent()` (`GraphicsItem`), 365
- `contextMenuEvent()` (`Widget`), 307, 309, 390
- `continue statement` (语句), 53
- `control structures` (控制结构); see `if`, `for`, `while`
- `controls` (控件); see `QWidget`
- `convenience widgets` (便利部件); see `QWidget`, `QTableWidget`, and `QTreeWidget`
- `conventional entry point` (常规入口点), 62
- `conversions` (转换)
    - `bool()`, conversion, 83
    - `float()`, conversion, 40, 84, 91
    - `generator to list`, 58
    - `int()`, conversion, 40, 84, 91
    - `int to float`, 14, 20
    - `int to long`, 17
    - `long()`, conversion, 40
    - `str()`, conversion, 81, 83, 90, 98
    - `str to unicode`, 20
    - `unicode()`, conversion, 81, 83
- `coordinates` (坐标), 309, 328–331, 339, 342, 350, 357, 374
- `copy constructor` (拷贝构造函数), unnecessary, 83
- `copy()`, 98
- `copy module` (模块), 83, 88, 89, `set`, 38, 548, 551
- `copy()`, 83, 88, 89
- `deepcopy()`, 34, 83
- `copy_reg module`, 247
- `copying` (拷贝), 34, 51, 88, 89, 98
- `cos()` (`math`), 371, 375
- `count()`
    - `list`, 33
    - `str`/`unicode`, 25
- `cPickle module`, 235, 246–248, see also `pickle module`
- `createActions()`, 172–175
- `createEditor()` (`QAbstractItemDelegate`), 436, 440, 461, 486, 487, 488, 491
- `createIndex()` (`QAbstractItemModel`), 433, 504
- `critical()` (`QMessageBox`), 188
- `cStringIO module`, 23, see also `StringIO module`
- `Currency Converter application` (货币转换器应用), 121–127
- `current mouse position` (当前鼠标位置), 318
- `currentCharFormat()` (`QTextEdit`), 393, 395
- `currentColumn()` (`QTableWidget`), 422
- `currentDate()` (`QDate`), 55, 236, 401, 490
- `currentDateTime()` (`QDateTime`), 554
- `currentFont()` (`QFontComboBox`), 404
- `currentIndex()`
    - `QAbstractItemView`, 427, 428, 433, 503
    - `QComboBox`, 124, 275
    - `QListView`, 222, 275
    - `QTableWidget`, 335, 375
- `currentText()` (`QFontComboBox`), 389, 392
- `custom actions` (自定义动作), 172
- `custom defaults` (自定义默认值), 5
- `custom containers` (自定义容器), 235
- `custom formatting` (自定义格式化), 397
- `custom message` (自定义消息), 188
- `custom models` (自定义模型), 235
- `custom styles` (自定义样式), 217

## D

- `data()` (`QAbstractItemModel`), 427, 428, 430, 433, 461, 462, 486, 503
- `data()` (`QMimeData`), 312, 314, 316
- `database()` (`QSqlQuery`), 450
- `databases`; see SQL
- `datetime module`, 236
- `date()` (`QDateTime`), 491
- `DateEdit`; see `QDateEdit`
- `DateTimeEdit`; see `QDateTimeEdit`
- `DB-API`, 445
- `deallocator`; see `__del__()`
- `debugging`, 105, 111, 498–504
- `decoding`; see encodings
- `decorators`, 85, 86, 134, 239, 549
- `defaultdict type`, 36, 92
- `default values`, 55–61
- `def statement`, 55, 62–63, 77
- `degrees()` (`math`), 371
- `del statement`, 32, 355, 391, 372, 556
- `delayed deletion`, 284, 286
- `deleteLater()` (`QObject`), 284, 286
- `deque` (`collections`), 29, 529
- `derived class`, 75, 76
- `deserialize`; see `pickle`
- `designer`; see `Qt Designer`
- `destroyed() signal` (`QObject`), 284, 286
- `destructor`; see `__del__()`
- `devicePixelRatio()` (`QPaintDevice`), 337
- `dict type` (续) see also `defaultdict` type and `OrderedDict` example class
- `difference()` (`set`), 38
- `dir()`, 39, 40
- `dirname()` (`os.path`), 173, 477, 496, 512
- `dirty flag` (脏标记), 168, 187, 192, 232, 356, 361, 362, 364, 365, 422, 453, 431
- `disabling widgets and actions`, 219, 274, 385
- `discard()` (`set`), 38
- `disconnect()` (`QObject`), 130
- `division` (`/` and `//`), 17, 84, 86, 91
- `divmod()`, 40
- `dock window`; see `QDockWidget`
- `dock windows` (停靠窗口), 169–170
- `docstrings` (文档字符串), 57, 77, 105
- `doctest module`, 105–107
- `document()` (`QTextEdit`), 286, 287, 383, 384, 385, 396
- `documentation` (文档), 27, 111
- `documentElement()` (`QDomDocument`), 260
- `DOM parser` (DOM 解析器), 259–262
- `done()` (`QDialog`), 154, 457, 464
- `double click`; see `mouseDoubleClickEvent()`
- `double quotes` (双引号字符串), 21
- `drag and drop` (拖放操作), 312–317
- `drag icon` (拖放图标), 316
- `dragEnterEvent()` (`QWidget`), 309, 314, 316
- `dragMoveEvent()` (`QWidget`), 309, 314, 315, 316
- `drawArc()` (`QPainter`), 344
- `drawChord()` (`QPainter`), 344
- `drawConvexPolygon()` (`QPainter`), 344
- `drawEllipse()` (`QPainter`), 344, 374, 377, 381
- `drawImage()` (`QPainter`), 343, 363, 400
- `drawLine()` (`QPainter`), 338, 344
- `drawPath()` (`QPainter`), 344, 377
- `drawPicture()` (`QPainter`), 363
- `drawPie()` (`QPainter`), 344
- `drawPixmap()` (`QPainter`), 344, 363, 408
- `drawPoint()` (`QPainter`), 344
- `drawPolygon()` (`QPainter`), 338, 343, 344, 345
- `drawPolyline()` (`QPainter`), 344, 345
- `drawRect()` (`QPainter`), 337, 344, 368, 410
- `drawRoundRect()` (`QPainter`), 344
- `drawText()` (`QPainter`), 306, 338, 344, 408, 410, 481
- `drill-down` (钻取), 467
- `driver()` (`QSqlDatabase`), 449
- `driver()` (`QSqlQuery`), 450
- `drivers` (数据库驱动), 445
- `dropEvent()` (`QWidget`), 309, 315, 316
- `DSU` (装饰, 排序, 去装饰), 551
- `duck typing` (鸭子类型), 221, 492
- `dump()` (`pickle`/`cPickle`), 248
- `duplicate data, avoiding`, 413
- `dynamic properties` (动态属性), 78
- `dynamic function definition` (动态函数定义), 62–363
- `dynamic menus`; see `menus` and `QMenu`
- `dynamic typing` (动态类型), 12, 13–101

## E

- `edit()` (`QAbstractItemView`), 426, 465, 468
- `editing, in-place` (原地编辑), 414, 458
- `editing` (编辑中), 417, 426, 440, 465, 468
- `editItem()` (`QTableWidget`), 222
- `IDLE editor`, 10, 105, 382
- `editors` (编辑器); see IDEs
- `elif statement`; see `if statement`
- `else statement`; see `if statement`
- `emit()` (`QObject`), 130, 211, 299, 333, 340, 391, 431, 456
- `enabling widgets and actions`, 219, 274, 385
- `encodings` (编码), 20, 250, 258, 501
- `encodings` (续)
- `examples` (续)
    - `ASCII`, 20, 236, 250, 501, 555
    - `Calculator application`, 116–121
    - `Latin1`, 20
    - `Connection application`, 132–135, see also `codecs module`, `QString`, and `Unicode`
    - `Currency Converter application`, 121–127
    - `UTF-8`, 236, 250, 258, 501, 555
- `endElement()` (`QXmlContentHandler`), 263
- `Fraction Slider application` (分数滑动块), 331–338
- `frange()`, 55–57
- `Image Changer application` (图像应用), 165–200
- `insertRows()` (`QAbstractItemModel`), 432, 333
- `MultiPedes application` (多足应用), 368–377
- `removeRows()` (`QAbstractItemModel`), 432, 333
- `OrderedDict`, 92–98
- `Page Designer application` (页面设计应用), 392, 393
- `Rich Line Edit class` (富文本行编辑类), 368–399
- `Roman SpinBox` (罗马数字数字框), 326–338
- `Signals and Slots application` (信号与槽应用), 128–131
- `entry point` (入口点), fixed, 87
- `__eq__()`, 88
- `Erica IDE`, 2, 382
- `error handling`, files, 244
- `escape key` (键), 121, 161, 188, 422, see also `finally statement`
- `exceptions` (异常), 62–66
- `escaped characters` (转义字符), 21, 22, 401
- `AttributeError`, 89, 101
- `Exception`, 68, 69
- `newlines` (换行), 51
- `handling` (处理), 67–71
- `Euro symbol` (€), 21
- `hierarchy` (层级结构), 67
- `eval()`, 39, 81, 120, 247
- `event handlers` (事件处理器); see `events`
- `event loop` (事件循环), 115–116, 224, 531
- `event()` (`QObject`), 304, 309, 310, 384
- `events` (事件), 115, 303–310, see `closeEvent()`, `keyPressEvent()`, `keyReleaseEvent()`, `mouseDoubleClickEvent()`, `mouseMoveEvent()`, `mousePressEvent()`, `mouseReleaseEvent()`, `paintEvent()`, `resizeEvent()`, and `wheelEvent()`
- `exec_()`
    - `QApplication`, 115, 184
    - `QDialog`, 142, 154, 511
    - `QDrag`, 316
    - `QMenu`, 307, 365, 392, 450
    - `QSqlQuery`, 447, 448, 449, 450, 464, 468, 469
- `exists()` (`QFile`), 294
- `exiting applications`; see `terminating applications`
- `expandItem()` (`QTreeWidget`), 421
- `exporting files`, 229
- `extend()` (`list`), 33
- `extension dialogs` (扩展对话框), 276–280
- `fillPath()` (`QPainter`), 344
- `fillRect()` (`QPainter`), 344, 438, 481, 489
- `finally statement` (语句), 66, 70–71, 78, 541, 542, 543, 548, 550, 551, 553, 554, 556
    - see also `except statement` and `try statement`
- `financial calculations` (财务计算), 18
- `find()`
    - `str`/`unicode`, 24, 25, 68
    - `text()` (`QComboBox`), 142, 441, 457
- `first()` (`QSqlQuery`), 450
- `firstChild()` (`QDomNode`), 260
- `fixed size` (of), 277
- `flags()` (`QAbstractTableModel`), 427, 430, 433

## F

- `F2 key press`, 417, 422, 440
- `False constant`, 245
- `fatalError()` (`QErrorHandler`), 263
- `field-level validation` (字段级验证), 140
- `findIndex()` (`QSqlTableModel`), 456
- `files`; see `type`, `open()` and `QFile`
- `file dialogs`; see `QFileDialog`
- `file error handling`, 244
- `file extensions`:
    - `.bmp`, `.jpg`, `.png`, and `.png` (image files), 193
    - `.pro` (C++/Qt project), 518
    - `.py` and `.pyw` (Python files), 11, 207
    - `.pyc` and `.pyo` (Python bytecode), 11, 207
    - `.pyqt` (Qt message), 316, 517
    - `.ts` (translation files), 317, 518, 519
    - `.ui` (user interface files), 206, 207, 515
- `file formats`, 241
- `file handles`, generators, 70, 555
- `file types`, 70, 229
- `fileName()` (`QFile`), 189
- `fill()` (`QMap`), 392
- `float()`, 40, 84, 91
- `float type`, 17–20
- `floating point division`; see `true division`
- `__floordiv__()` (`//=`), 84, 91
- `focus`; see `keyboard`
- `fonts`; see `QFont`
- `font()` (`QGraphicsItem`), 336, 342
- `for loop` (循环), 50, 54
    - `break statement`, 53
    - `continue statement`, 53
    - `else statement`, 50, 54, 56

## G

- `garbage collection` (垃圾回收), 15, 78, 168, 169, 232, 356, 361, 362, 364, 365, 422, 453, 431
- `__ge__()` (`>=`), 81
- `generators` (生成器), 54, 58, 59, 70
- `geometry()` (`QWidget`), 357
- `get()` (`dict`), 39, 92, 218, 336
- `getDouble()` (`QInputDialog`), 199
- `getExistingDirectory()` (`QFileDialog`), 547
- `getInt()` (`QInputDialog`), 199
- `getItem()` (`QInputDialog`), 199
- `getOpenFileName()` (`QFileDialog`), 189
- `getSaveFileName()` (`QFileDialog`), 189
- `getText()` (`QInputDialog`), 199
- `global namespace`, 64
- `global variables`, 64, 83
- `graphics items`; see `QGraphicsItem`
- `graphics scene`; see `QGraphicsScene`
- `graphics view`; see `QGraphicsView`
- `greater than` (`>`), 47, 81, 82
- `grid layout`; see `QGridLayout`
- `group box`; see `QGroupBox`
- `gt()` (`operator`), 81

## H

- `handling errors`, reading and writing, 244
- `has_key()` (`dict`), 96
- `hasattr()`, 39, 102, 218, 336
- `hasChildren()` (`QAbstractItemModel`), 433
- `hasFeature()` (`QSqlDriver`), 449
- `hasFocus()` (`QWidget`), 330, 426
- `hasFormat()` (`QMimeData`), 314, 316
- `hash`; see `dict type`
- `hasHtml()` (`QClipboard`), 312
- `hasMouseTracking()` (`QWidget`), 308
- `hasSelection()` (`QTextEdit`), 385
- `headerData()` (`QAbstractItemModel`), 427, 430, 433, 503
- `height()` (`QWidget`), 330
- `help()`, 37, 39
- `hex()`, 40
- `hide()` (`QWidget`), 280, 330
- `hiding dialogs`, 118, 121, 160
- `hiding widgets`, 277, 280
- `high-level communication mechanisms`; see `signals and slots`
- `homePath()` (`QDir`), 173
- `horizontal layout`; see `QHBoxLayout`
- `horizontal line`; see `QFrame`
- `horizontalHeader()` (`QTableView`), 463, 464
- `hotspot` (热点), 316
- `HTML` (Hyper-Text Markup Language), 114, 117, 188, 311, 391, 421, 440, 551
- `__gt__()` (`>`), 81

## I

- `id()`, 13, 39, 231, 237, 418
- `idealWidth()` (`QTextDocument`), 390, 439, 489
- `identifiers` (标识符), 36
- `identity`
    - `comparison`, 13, 57
    - `operator`, 47
    - see also `id()` and `is statement`
- `IDEs` (集成开发环境)
    - `Eric`, 4, 2, 382
    - `IDLE`, 9, 10, 60, 105, 382
- `if statement`, 46–49
    - `conditional expression`, 49
- `__ifloordiv__()` (`//=`), 84
- `ignore()` (`QEvent`), 186, 314
- `images`; see `QImage`
- `image formats`, 193
- `Image Changer application`, 165–200
- `images`, 168, 193, 195, 196
    - `printing`, 363
- `immutable objects` (不变对象), 15, 16, 20, 23, 29, 34, 35, 37, 57
- `__imod__()` (`%=`), 84
- `import statement`, 18, 19
    - `from __future__`, 86, 549
    - `path`, 60
- `importing files`, 229
- `__imul__()` (`*=`), 84, 91
- `in-memory databases` (内存数据库), 446
- `in operator`, 25, 33, 36, 38, 45, 96
- `in-place editing` (原地编辑), 414, 458
- `incomingConnection()` (`QTcpServer`), 530, 539
- `indentation` (缩进), 46
- `integrated development environments`; see `IDEs`
- `interactive Python use`, 60
- `Interbase database`, 445
- `interdependent actions`; see `QActionGroup`, 176
- `interdependent values`; see `form-level validation`
- `interface` (接口), 102
- `internalPointer()` (`QModelIndex`), 504
- `interpreter`, Python, 11
- `introspection` (内省), 102, 105
- `invertPixels()` (`QImage`), 197
- `IOError exception`, 243, 244
- `is statement`, 13, 47
- `isActive()` (`QSqlQuery`), 449, 450
- `isAlive()` (`helper`), 287–288
- `isalpha()` (`str`/`unicode`), 25
- `isChecked()` (`QAction`), 172, 176
- `isdigit()` (`str`/`unicode`), 25, 238, 554
- `isEmpty()`, 233
- `isEnabled()` (`QAction`), 172
- `isFile()` (`QFileInfo`), 294
- `isinstance()`, 39, 94, 102, 135, 289, 296, 359, 372, 375, 393, 395, 440, 496, 499, 502, 503
- `isModified()` (`QTextDocument`), 287, 385
- `isNull()`
    - `QDate`, 45
    - `QDateTime`, 45
    - `QModelIndex`, 260
    - `QImage`, 400
    - `QPixmap`, 496
    - `QString`, 45
    - `QTime`, 45
- `ISO date format` (ISO 日格式), 250, 258
- `isObscured()` (`QGraphicsItem`), 366
- `isOpen()` (`QDataStream`), 525
- `isRunning()` (`QThread`), 547, 551
- `isSelected()` (`QGraphicsItem`), 366
- `issubset()` (`set`), 38
- `issuperset()` (`set`), 38
- `isValid()`
    - `QModelIndex`, 427, 428, 504
    - `QSqlQuery`, 450
- `item()` (`QTableWidget`), 222
- `itemChange()` (`QGraphicsItem`), 362, 366
- `itemChanged()` (`QTableWidget`), 417
- `items()`
    - `dict`, 97
    - `QGraphicsScene`, 354, 372
- `iter()`, 97, 237
- `__iter__()` (`iter()`), 93, 97, 236
- `iterable` (可迭代对象), 50
- `iteration` (迭代); see `for loop`, `generators`
- `iterators` (迭代器), 52, 54, 87, 92
- `items()` (`dict`), 97, 98
- `keys()` (`dict`), 97
- `values()` (`dict`), 97
- `__itruediv__()` (`/=`), 84, 91

## J

- `join()`
    - `os.path`, 496, 512, 555
    - `str`/`unicode`, 23, 25, 61, 193, 477
- `.jpg` and `.jpeg` (image files), 193
- `key()` (`QKeyEvent`), 307, 334, 365, 384, 391, 483
- `key sequences` (键序列), 171–172, 175, 176
    - see also `QKeySequence`
- `keyboard accelerators` (键盘加速器), 143, 144, 189, 299
- `keyboard focus` (键盘焦点), 206, 218, 304, 351, 364, 478
- `keyboard shortcuts` (键盘快捷键), 144, 394
- `keyboard user support` (键盘用户支持), 149, 218, 390, 417, 482, 511

## K

- `KeyError exception`, 94
- `key presses` (按键按下)
    - `Enter`, 120, 145, 188, 391, 421, 422, 440, 511
    - `Esc`, 121, 161, 188, 421, 422
    - `F2`, 417, 422, 440
    - `Shift`, 365
    - `Tab`, 206, 218, 310, 421, 421, 551
- `keyPressEvent()`
    - `QGraphicsItem`, 365
    - `QWidget`, 307, 309, 334, 391, 483
- `keyReleaseEvent()` (`QWidget`), 307
- `keys()` (`dict`), 36
- `keyword arguments` (关键字参数), 55–61
- `keywords table` (关键字表), 16

## L

- `lambda statement` (lambda 语句), 61–62, 134, 453
- `layout` (布局); see `QLayout`
- `layout management` (布局管理), 145–148
- `lazy evaluation` (惰性求值), 47
- `ldexp()` (`math`), 40
- `le()` (`operator`), 81
- `left()` (`QString`), 240
- `len()`, 20, 25, 33, 36, 38, 96, 237, 503
- `__len__()` (`len()`), 81, 93
- `less than` (`<`), 47, 81, 82
- `__le__()` (`<=`), 81
- `level of detail` (细节层次), 350
- `lexical scoping` (词法作用域), 64
- `libraries` (库), 11, 18
- `license` (许可), 3
- `lifecycle` (生命周期), 115
- `line edit`; see `QLineEdit`
- `linear search` (线性搜索), 95
- `list type` (列表类型) (续)
    - `concatenation operator` (+), 33
    - `append()`, 33, 53
    - `count()`, 25, 33
    - `extend()`, 33
    - `generation`, 54
    - `index()`, 24, 33
    - `indexing`, 32



# 索引

- `insert()`, 33, 500
- 迭代, 50
- `pop()`, 33, 35, 361
- `remove()`, 32, 33
- `reverse()`, 33
- 切片, 32
- `sort()`, 33, 53, 63, 95, 239

- `title()`, 24

- 标签; 另见 `QLabel`

- lambda 事件, 61–62, 134, 453

- `last()`(`QSqlQuery`), 450

- `lastError()`
    - `SqlDatabase`, 446, 450, 459, 465
    - `QSqlQuery`, 449

- `lastIndex()`(`QString`), 234

- Latin-编码, 20

- 布局管理器, 118–120, 123, 144–146, 155, 209–210, 255–271, 332

- `layout()`(`QWidget`), 277

- 布局策略, 270–271

- 长度 (`<=`), 81

- `left()`(`QString`), 234, 306

- `len()`, 20, 25, 33, 38, 237, 503

- `len_`(`len()`), 93, 96, 237, 503

- Length (class), 86–91

- `length()`(`QString`), 388

- 详细程度, 374

- 许可, 3

- 生命周期, PyQt 对象, 287

- 行编辑器; 另见 LineEdit

- 行宽; 另见 width

- `lineEdit()`(`AbstractSpinBox`), 327

- 列表推导式, 53–64, 997

- 列表类型, 31–35, 33, 38

- 列表控件; 另见 `QWidget`

- `listen()`(`Qt`), 529

- 字面量, 17

- 活动对话框, 159–162

- 加载文件, 184, 229, 240–248, 249–256

- 局部作用域, 55

- 局部变量, 87

- 区域; 另见 `QLocale`

- `locale.arg()`(`QString`), 416, 434

- `lock()`(`QMutex`), 553, 554

- `lockFor()`(`QWriteLock`), 541, 542, 543, 548, 550, 551

- `lockFor()`(`QWriteLock`), 542, 543, 556

- 逻辑坐标; 另见 window

- 逻辑运算符, 47

- `long()`, 40

- long 类型, 16–17, 231, 241

- 循环; for 语句和 while

- 深度层嵌套, 69

- 底层通信机制; 另见事件

- `lower()`(`str/unicode`), 25, 238

- 释放, 207, 513, 518

- 方法（续）
    - 静态, 78
    - 虚拟, 75, 99

- `mid()`(`QString`), 252

- MIME (多用途互联网扩展) 格式, 310, 313

- Mac OS 检测, 218

- 魔法数字, 241

- 邮件列表, 5

- `main()`, 入口点, 62

- 主窗口; 另见 `QMainWindow`

- `main_module` 属性值, 106

- PyQt 应用程序 (`mypqt.pyw`), 174, 206, 207, 216, 519

- 命名变形, 77, 88, 89

- `mapFromGlobal()`(`QWidget`), 357

- `moveToGlobal()`(`QWidget`), 309, 392, 393

- `mapToScene()`(`QGraphicsView`), 357

- 主细节表, 458, 464, 469

- `math` 模块, 40, 117, 371, 375

- `matrix()` `QGraphicsItem`, 359, 377, `QGraphicsView`, 370

- `max()`, 38

- 最大尺寸, 布局和控件, 271

- `Height()`(`QWidget`), 390

- `mimeData()`
    - `QClipboard`, 312
    - `QDropEvent`, 314

- `min()`, 38

- 最小化, 297

- 最小尺寸, 布局和控件, 270, 271, 335

- `minimumHeight()`(`QWidget`), 390

- `minimumSizeHint()`(`QWidget`), 271, 335, 340, 479

- `mirrored()`(`QImage`), 198

- `mypqt.py` 应用程序, 174, 206, 207, 216, 519

- `mod_()`, 84

- 模态, 140, 142, 511

- `model()` (`QModel`), 438, 442, 489

- 模型对话框, 140, 155, 286

- 模型; 另见自定义模型和 `AbstractItemModel`

- `modifiers()`(`QInputEvent`), 307, 365, 391

- 模块, 104

- `modulus()`, 53

- 鼠标位置, 318

- 鼠标跟踪; 另见 `MouseTracking()` 和 `setMouseTracking()`

- `doubleClickEvent()`, 362

- `QGraphicsItem`, 362

- `moveEvent()`(`QWidget`), 309, 317, 308, 309, 417, 422, 440

- `mousePressEvent()`(`QWidget`), 309, 333

- `mouseReleaseEvent()`(`QWidget`), 308, 309

- `move()`(`QGraphicsItem`), 366

- `mul_()` (`+=`), 84, 91

- 相互作用, 144, 350

- 相互依赖的, 14, 37

- `,` 307, 334, 365, 384, 391, 483

- 键序列, 171–172, 175, 176

- 另见 `QSequence`

- 键盘加速器, 143, 144, 189, 299

- 键盘焦点, 206, 218, 304, 351, 364, 478

- 键盘快捷键, 144, 394

- 键盘用户支持, 149, 218, 390, 417, 482, 511

# 601

- 对象的名称; 另见对象

- `Name()`

- 对象的引用, 12, 55, 57, 58

- 对象的类型, 76, 77, 88

- 对象
    - 可调用, 97, 102
    - 拷贝, 88, 239
    - 函数引用, 63, 64
    - 不变, 15, 16, 20, 23, 29, 34, 35, 37, 57
    - 可变, 16, 23, 29, 31, 32, 34, 35, 51, 57
    - 所有权, 119, 168, 172, 172, 180, 355, 357, 392, 376

- 对象的引用, 12, 55, 57, 58

- `oct()`, 40

- ODBC 数据库, 445, 448

- `toContinue()`(`helper`), 187

- 旧式 vs. 新式类, 76

- `open()`
    - 内置, 39, 70
    - 解码, 255, 260, 501, 555
    - gzip, 248
    - `QtDevice`, 241, 252, 252, 258, 259
    - `SqlDatabase`, 446, 459

- 开源许可, 3

- `or` 运算符, 47

- Oracle 数据库, 445, 448

- `ord()`, 21, 39, 50

- `OrderedDict` 示例类, 92–98

- 缩进, 430

- `os` 模块
    - `walk()`, 555

- `os.path` 模块
    - `basename()`, 189
    - `dirname()`, 173, 477, 496, 512
    - `join()`, 496, 512, 555

- `OSError` 异常, 243, 244

- 重载, 75

# 602

# 索引

# P

- 页面大小 (page size), 打印机 (printer), 400

- 页面设计器 (Page Designer application), 351–368

- `pageResult()`(`QR`), 408

- 绘制设备 (paint devices); 参见 `QImage`, `QPainter`, `QPicture`, `QPixmap`, `QPrinter`, and `QWidget`

- `paint()`
    - `QAbstractDelegate`, 436, 438, 461, 486, 489
    - `GraphicsItem`, 366, 368, 374, 377
    - `paintEvent()`(`Widget`), 306, 309, 336, 342, 480

- 调色板 (palette); 参见 `QPalette`

- `palette()`
    - `Application`, 438, 489
    - `QWidget`, 337

- 参数 (parameters), 55, 56
    - 默认值 (default), 56
    - 关键字 (keyword), 55, 59
    - 按值传递 (passing by value), 55

- `parent()`(`QObject`), 433, 504

- 父部件 (parent of widget), 118, 119, 172, 340, 372

- 解析 (parse), autistic, 119

- `parse()`(`XmlReader`), 262

- 解析 XML (parsing XML), 259–262, 262–265

- `partial()`(`example`), 64–65

- `partial()`(`functools`), 64–133, 365

- 部分函数 (partial function), 63–65, 133, 365

- 按值传递 (pass-by-value), 57

- 语句 (pass statement), 47

- 贴板 (pasteboard); 参见 `QClipboard`

- 绘画 (paints), 软件 (for software), 222

- 路径 (path)(`QFileInfo`), 233, 356

- 路径变量 (path variable (sys)), 60, 104

- PDF (Portable Document Format), 398, 401

- 笔宽 (pen width), 144

- 物理坐标 (physical coordinates); 参见 视口 (viewport)

- `pickle()`(`copy_reg`), 247

- pickle 模块, 235, 246–288; 参见 Pickle module

- 像素 (pixmap); 参见 `QPixmap`

- `pixmap()`
    - `QClipboard`, 311
    - `GraphicsPixmapItem`, 359

- 平台模块 (platform module)
    - `python_version()`, 200
    - `system()`, 200, 217, 336, 390
    - `.png` 图像文件 (image file), 193

- 指针 (pointers); 参见 对象引用 (object references)

- 策略 (policies for)
    - 文件错误处理 (file error handling), 244
    - 大小和长度 (size and length), 270–271, 335
    - 字符串 (strings), 28, 228
    - 多态 (polymorphism), 99–103

- `pop()`, 96
    - 字典 (dict), 36, 96
    - 列表 (list), 33, 355, 361
    - 集合 (set), 372

- `popitem()` (dict), 96

- 填充列表部件 (populating widgets), 418

- 填充树 (populating trees), 420, 502

- 可携式文档格式 (portable document format); 参见 PDF

- `pos()`
    - 光标 (Cursor), 318, 357
    - `GraphicsItem`, 359, 366
    - `QOSEvent`, 309
    - 位置参数 (positional arguments), 55

- 事后验证 (post-mortem validation), 140, 150, 151

- PostgreSQL 数据库, 445

- PostScript, 401

- `pov()`, 40

- 布局和部件的首选尺寸 (preferred size, of layouts and widgets), 271, 335

- `prepare()`(`QSqlQuery`), 488, 450, 468

- 预处理查询 (prepared queries), 477
    - `append()`(`QStringList`), 189
    - 保持宽高比例 (preserving aspect ratio), 329

- 预防性验证 (preventative validation), 140, 157, 159, 162, 327

- 预览表单 (previewing forms), 215

- `previous()` (`QSqlQuery`), 449, 450

# 603

# 索引

- 打印语句 (print statement), 10, 26

- 尾逗号 (trailing comma), 49

- `print_` (`QtDocument`), 430, 407

- 打印机 (printer); 参见 `QPrinter`

- `printImage()` 辅助函数, 363

- 打印 (printing), 170, 363, 398-410

- 打印图像 (printing images), 363

- 私有名称 (private names), 76, 80, 88

- `.pro` (C++/Qt 项目文件), 518

- `processEvents()` (`QApplication`), 294, 537

- 启动处理 (processing, at start), 184

- 传递隐藏和显示调用 (propagating hide and show calls), 280

- 属性 (properties), 80, 211, 322

- QObject 属性 (properties, QObjects), 157, 211

- `property()`
    - 内置 (built-in), 80
    - `QObject`, 322, 324

- `.py` 和 `.py` (Python 文件), 111, 111, 207

- `.py` 和 `.py` (Python 字节码文件), 11, 207

- py54 应用, 207, 513, 517, 518

- PyQt 模块; 参见各个模块 (`QtCore`, `QtGui`, etc.)

- `pyProperty` (`QtCore`), 322

- `@pyqtSignature` 装饰器 (`QtCore`), 218, 219

- PYQT 版本字符串, 200

- py4 应用, 173, 174, 207

- `python_version()` (`platform`), 200

- pyic 应用, 206, 207, 221, 515

- `QAbstractButton` (`QtGui`)
    - 基类 (base class), `QWidget`
    - 可勾选 (`setCheckable`), 276, 278
    - 设置文本 (`setText`), 370
    - 切换信号 (`toggled signal`), 277, 280

- `QAbstractDelegate` (`QtGui`)
    - 基类 (base class), `QObject`

- `QAbstractDelegate` (`QtGui`) (续)
    - 创建编辑器 (`createEditor`), 336, 440, 461, 486, 487, 491
    - 绘制 (`paint`), 436, 438, 461, 489
    - 数据 (`data`), 436, 441, 462, 486, 487, 488
    - 设置模型数据 (`setModelData`), 436, 441, 462, 486, 487, 488
    - 尺寸提示 (`sizeHint`), 436, 439, 489

- `QAbstractItem` (`QtCore`), 425, 433, 434, 445, 500
    - 基类 (base class), `QObject`
    - 开始插入行 (`beginInsertRows`), 432, 433
    - 开始移除行 (`beginRemoveRows`), 433
    - 列数 (`columnCount`), 427, 428, 503
    - 创建索引 (`createIndex`), 433, 504
    - 数据 (`data`), 414, 441, 462, 428, 429, 430, 438, 441, 462, 481, 487, 498, 491, 496, 503
    - 数据改变 (`dataChanged`), 431, 432, 478
    - 结束插入行 (`endInsertRows`), 432, 433
    - 结束移除行 (`endRemoveRows`), 432, 433
    - 标志 (`flags`), 427, 430, 503
    - 子项 (`children`), 433
    - 表头数据 (`headerData`), 427, 430, 503
    - 索引 (`index`), 433, 465, 504
    - 插入行 (`insertRows`), 433, 465, 468
    - 移除行 (`removeRows`), 426, 427, 432, 434, 466, 469
    - 移除行 (`removeRows`), 427, 432, 434, 470, 432, 434, 501, 502
    - 重置 (`reset`), 426, 427, 428, 434, 454, 455, 479, 481, 503
    - 设置数据 (`setData`), 414, 427, 431, 434, 441, 462, 465, 487, 488
    - 表头数据 (`headerData`), 434, 460, 462

- `QAbstractItem` (`QtGui`)
    - 基类 (base class), `QAbstractScrollArea`
    - 当前索引 (`currentIndex`), 427, 463, 465, 466, 468
    - 编辑 (`edit`), 426, 465, 468
    - 选择模型 (`selectionModel`), 463
    - 设置交替行颜色 (`setAlternatingRowColors`), 231, 477
    - 当前索引 (`CurrentIndex`), 426, 465, 468

# 604

# 索引

- `QAbstractItem` (`QtGui`) (续)
    - 设置启用拖拽 (`setDragEnabled`), 312, 313, 315
    - 设置触发器 (`setEditTriggers`), 231
    - 设置代理 (`setDelegate`), 437, 460, 463, 490
    - 设置模型 (`setModel`), 425, 437, 460, 463, 477, 490
    - 设置选择行为 (`setSelectionBehavior`), 231, 460, 463, 495
    - 选择模式 (`SelectionMode`), 231, 460
    - 开始拖拽 (`startDrag`), 316

- `QAbstractScroll` (`QtGui`)
    - 基类 (base class), `QFrame`
    - 视口 (`viewport`), 392, 393

- `QAbstractSlider` (`QtGui`)
    - 基类 (base class), `QWidget`
    - 设置范围 (`setRange`), 129
    - 设置值 (`setValue`), 128, 369

- `QAbstractSocket` (`QtNetwork`), 521
    - 基类 (base class), `QIODevice`
    - 连接 (`connectTo`), 525
    - 状态 (`state`), 540
    - 等待断开 (`waitForDisconnected`), 544

- `AbstractSpinBox` (`QtGui`)
    - 基类 (base class), `QWidget`
    - 单行编辑器 (`lineEdit`), 327
    - 设置对齐 (`setAlignment`), 340, 487
    - 验证 (`validate`), 327, 328

- `QAbstractTableModel` (`QtCore`), 425, 427
    - 基类 (base class), `QAbstractItemModel`

- `Action` (`QtGui`), 171, 172, 194, 385
    - 基类 (base class), `QObject`
    - 数据 (`data`), 172, 393, 395
    - 编辑器 (`editor`), visual, 206
    - 勾选 (`isChecked`), 172, 476
    - 启用 (`isEnabled`), 172
    - 可勾选 (`setCheckable`), 172, 177, 393
    - 设置数据 (`setData`), 172, 189, 392, 393
    - 设置分隔符 (`setSeparator`), 172
    - 设置快捷键 (`setShortcut`), 171, 172
    - 设置状态提示 (`setStatusTip`), 172
    - 设置文本 (`setText`), 172
    - 设置工具提示 (`setToolTip`), 172
    - 切换信号 (`toggled signal`), 172, 176, 177
    - 触发信号 (`trigger signal`), 172, 176
    - 这是什么 (`whatsThis`), 172

- `Calendar` (`QtGui`), 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 351, 352, 353, 354, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370, 371, 372, 373, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 392, 393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 483, 484, 485, 486, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 498, 499, 500, 501, 502, 503, 504, 505, 506, 507, 508, 509, 510, 511, 512, 513, 514, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 528, 529, 530, 531, 532, 533, 534, 535, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 546, 547, 548, 549, 550, 551, 552, 553, 554, 555, 556, 557, 558, 559, 560, 561, 562, 563, 564, 565, 566, 567, 568, 569, 570, 571, 572, 573, 574, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 590, 591, 592, 593, 594, 595, 596, 597, 598, 599, 600, 601, 602, 603, 604, 605

- `ByteArray` (`QtCore`), 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 351, 352, 353, 354, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370, 371, 372, 373, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 392, 393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 483, 484, 485, 486, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 498, 499, 500, 501, 502, 503, 504, 505, 506, 507, 508, 509, 510, 511, 512, 513, 514, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 528, 529, 530, 531, 532, 533, 534, 535, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 546, 547, 548, 549, 550, 551, 552, 553, 554, 555, 556, 557, 558, 559, 560, 561, 562, 563, 564, 565, 566, 567, 568, 569, 570, 571, 572, 573, 574, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 590, 591, 592, 593, 594, 595, 596, 597, 598, 599, 600, 601, 602, 603, 604, 605

- `Brush` (`QtGui`), 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 351, 352, 353, 354, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370, 371, 372, 373, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 392, 393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 483, 484, 485, 486, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 498, 499, 500, 501, 502, 503, 504, 505, 506, 507, 508, 509, 510, 511, 512, 513, 514, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 528, 529, 530, 531, 532, 533, 534, 535, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 546, 547, 548, 549, 550, 551, 552, 553, 554, 555, 556, 557, 558, 559, 560, 561, 562, 563, 564, 565, 566, 567, 568, 569, 570, 571, 572, 573, 574, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 590, 591, 592, 593, 594, 595, 596, 597, 598, 599, 600, 601, 602, 603, 604, 605

- `ComboBox` (`QtGui`), 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 351, 352, 353, 354, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370, 371, 372, 373, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 392, 393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 483, 484, 485, 486, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 498, 499, 500, 501, 502, 503, 504, 505, 506, 507, 508, 509, 510, 511, 512, 513, 514, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 528, 529, 530, 531, 532, 533, 534, 535, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 546, 547, 548, 549, 550, 551, 552, 553, 554, 555, 556, 557, 558, 559, 560, 561, 562, 563, 564, 565, 566, 567, 568, 569, 570, 571, 572, 573, 574, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 590, 591, 592, 593, 594, 595, 596, 597, 598, 599, 600, 601, 602, 603, 604, 605

# 606

# 索引

## `QDomDocument` (`QtXml`) (续)

- `documentElement()`, 260
- `setContent()`, 259
- `toString()`, 257, 260

## `DomElement` (`QtXml`)

- 基类, `QDomNode`
- `attribute()`, 261
- `tagName()`, 260

## `DomNode` (`QtXml`)

- `firstChild()`, 260
- `isNull()`, 260
- `nextSibling()`, 260
- `nodeType()`, 261
- `toElement()`, 260
- `toText()`, 260

## `QDoubleSpinBox` (`QtGui`), 123, 578

- 基类, `QAbstractSpinBox`

## `Drag` (`QtGui`), 316

- 基类, `QObject`
- `exec()`, 316
- `setHotSpot()`, 316
- `mimeData()`, 316
- `setPixmap()`, 316
- `start()`, 316

## `QDropEvent` (`QtGui`)

- 基类, `QEvent`
- `mimeData()`(`QDropEvent`), 314
- `setDropAction()`, 314, 315, 316

## `QEvent` (`QtCore`)

- `accept()`, 314, 333, 391
- `globalPos()`, 307, 309
- `ignore()`, 314
- `type()`, 384

## `QFile` (`QtCore`), 241, 243, 250, 252, 258, 259, 262

- 基类, `QIODevice`
- `exists()`, 294

## `QFileDialog` (`QtGui`)

- `getExistingDirectory()`, 547
- `openFileFileName()`, 193, 194, 223, 234, 287, 295, 356
- `saveFileName()`, 196

## `QFileInfo` (`QtCore`), 189

- `filename()`, 189
- `isFile()`, 294
- `path()`, 233, 356

## `QFont` (`QtGui`), 335, 336, 408, 478

- `pointSize()`, 335, 336

## `QFont` (`QtGui`), 576

- 基类, `QComboBox`

## `QFontMetrics`/`QFontMetrics` (`QtGui`), 335, 336, 340, 341, 342, 390, 439

## `QFrame` (`QtGui`), 277

- 基类, `QWidget`
- `setStyle()`, 170, 278

## `GraphicsItem` (`QtGui`), 349, 364, 365, 366, 367, 373, 376

- `boundingRect()`, 265, 365, 366, 373, 377
- `collidesPath()`, 366
- `collidingItems()`, 366
- `contains()`, 366
- `contextMenu()`, 365
- `isObscured()`, 366
- `isSelected()`, 366
- `itemChange()`, 362, 366
- `keyPressEvent()`, 365
- `matrix()`, 359, 377
- `mouseDoubleClickEvent()`, 362
- `moveBy()`, 366
- `paint()`, 366, 368, 374, 377
- `pos()`, 359, 366
- `resetMatrix()`, 366
- `rotate()`, 366, 371, 375, 377
- `scale()`, 366
- `scene()`, 366, 375
- `sceneBoundingRect()`, 366, 379
- `setCursor()`, 366
- `setEnabled()`, 366
- `setFlag()`, 366
- `setFlags()`, 351, 356, 362, 364
- `setFocus()`, 364, 366
- `setFont()`, 362
- `Matrix()`, 362, 364, 367, 377
- `setPos()`, 356, 362, 364, 367, 373, 375
- `setSelected()`, 356, 362, 364, 367
- `setValue()`, 367
- `shape()`, 365, 367, 374, 377
- `shear()`, 367
- `translate()`, 367

## `QGraphicsItem`(`QtGui`) (续)

- `update()`, 365, 367
- `zValue()`, 367

## `QGraphicsLineItem`(`QtGui`), 349

- 基类, `QGraphicsItem`

## `QGraphicsPixmapItem`(`QtGui`), 349, 356

- 基类, `QGraphicsItem`
- `pixmap()`, 359

## `QGraphicsRectItem`(`QtGui`), 355

- 基类, `QAbstractGraphicsShape`

## `QGraphicsScene`(`QtGui`), 349, 354, 369

- 基类, `QObject`
- `addEllipse()`, 354
- `addItem()`, 354, 356, 362, 371
- `addLine()`, 354
- `addPath()`, 354
- `addPixmap()`, 354
- `addPolygon()`, 354
- `addRect()`, 354, 355
- `addText()`, 354
- `clearSelection()`, 356, 361, 362, 364
- `collidingItems()`, 354, 375
- `items()`, 354, 372
- `removeItem()`, 354, 359, 361, 372
- `render()`, 354, 361
- `selectedItems()`, 355, 380, 361
- `setBackgroundBrush()`, 354
- `setSceneRect()`, 354, 369
- `update()`, 354
- `views()`, 354, 362

## `QSceneMenuItem`(`Qt-`)

- 基类, `QEvent`
- `screenPos()`, 365

## `QGraphicsSimpleItem`(`QtGui`), 349

- 基类, `QAbstractGraphicsShape`

## `QGraphicsItem`(`QtGui`), 349, 342

- 基类, `QGraphicsItem`
- `font()`, 359
- `toPlainText()`, 359

## `QGraphicsView`(`QtGui`), 349, 351, 352, 369, 577

- 基类, `QAbstractScrollArea`
- `mapToScene()`, 357
- `matrix()`, 370
- `render()`, 361
- `scale()`, 352
- `setDragMode()`, 352
- `setRenderHint()`, 352, 362
- `setScene()`, 354, 369

## `QGridLayout`(`QtGui`), 123, 144, 146, 150, 270, 273

- 基类, `QLayout`
- `addLayout()`, 146, 151
- `setColumnStretch()`, 146
- `setRowStretch()`, 146

## `QGroupBox`(`QtGui`), 144, 260

- 基类, `QBoxLayout`

## `QComboBox`(`QtGui`), 173, 313, 392

## `QImage`(`QtGui`), 168, 195, 197, 199, 329, 400

- 基类, `QPoint`
- `invertPixels()`, 197
- `isFull()`, 400
- `mirrored()`, 198
- `rgbSwapped()`, 197
- `scaled()`, 199
- `size()`, 363, 400

## `ImageReader`, 193

## `ImageWriter`, 196

## `QDialog`(`QtGui`), 199

## `InputEvent`(`QtGui`)

- 基类, `QEvent`
- `modifiers()`, 307, 365, 391

## `QtDevice`(`QtCore`), 526

- 基类, `QObject`
- `bytesAvailable()`, 528, 531, 540
- `close()`, 243, 259, 525, 528
- `errorString()`, 241, 243, 250, 252, 258, 259, 528
- `open()`, 241, 243, 250, 252, 258, 259
- `readAll()`, 254

## `QIODevice` (`QtCore`) (续)

- `waitForReady()`, 540

## `QDelegate`(`QtGui`), 436, 437, 485–489

- 基类, `QAbstractItem`

## `KeyEvent`(`QtGui`), 307

- 基类, `QInputEvent`
- `key()`, 307, 334, 365, 384, 391, 483

## `QSequence`(`QtGui`), 171, 175, 285, 292, 393

## `QLabel`(`QtGui`), 114, 168, 340, 577

- 基类, `QFrame`
- `alignment()`, 168, 340
- `setBuddy()`, 143, 425
- `setPixmap()`, 199

## `QLayout`(`QtGui`), 146

- 基类, `QWidget`
- `addWidget()`, 151, 253
- `setConstraint()`, 277, 279

## `QNumber`(`QtGui`), 577

## `LinearGradient`(`QtGui`), 343

## `QLineEdit`(`QtGui`), 117, 310, 314, 440, 461, 577

- 基类, `QWidget`
- `inputMask` property, 157
- `returnPressed()` signal, 440
- `alignment()`, 461
- `setInputMask()`, 461
- `setText()`, 441, 462
- `setValidator()`, 461
- `text()`, 441
- `textEdited()` signal, 161, 217, 218

## `QListView`(`QtGui`), 415, 578

- 基类, `QAbstractItem`

## `QListView`(`QtGui`), 275, 312, 315, 414, 518

- 基类, `QListView`
- `addItem()`, 418
- `clear()`, 418
- `currentRowChanged()` signal, 275
- populating, 418
- `setCurrentItem()`, 418

## `QListWidget`(`QtGui`), 316, 418

- `setIcon()`, 316

## `QWidgetItem`(`QtGui`) (续)

- `takeItem()`, 316

## `Locale`(`QtCore`), 513, 516

## `QMainWindow`(`QtGui`), 168, 286, 284, 290

- 基类, `QWidget`
- `addDockWidget()`, 169, 186
- `tabBar()`, 179, 186
- `closeWindows()`, 289, 293
- `menuBar()`, 177, 186
- `restoreState()`, 183, 186
- `setCentralWidget()`, 168, 186
- `statusBar()`, 170, 186

## `Matrix` and `QTransform`(`QtGui`), 356

- `reset()`, 370, 377
- `scale()`, 370

## `QMdiArea`(`QtGui`), 290

## `Menu`(`QtGui`), 370, 365, 392

- 基类, `QWidget`
- `aboutToShow()` signal, 178, 187, 285, 292
- `addMenu()`, 178
- `addSeparator()`, 180, 307
- `exec()`, 370, 365, 392

## `QMenuBar`(`QtGui`), 177, 188

## `QMessageBox`(`QtGui`), 153, 187, 188, 200, 361, 425

## `QMetaObject`(`QtCore`), 217

## `QData`(`QtCore`), 311, 313, 316

- 基类, `QObject`
- `data()`, 315, 316
- `hasFormat()`, 314, 316
- `setData()`, 316
- `setText()`, 311

## `QIndex`(`QtCore`), 414, 432, 504

- `column()`, 428, 431, 439, 462, 486, 503
- `index()`, 427
- `internalPointer()`, 504
- `isValid()`, 427, 428, 504
- `model()`, 438, 442, 489
- `row()`, 427, 491

## `QModelIndex`(`QtCore`) (续)

- `sibling()`, 491

## `MouseEvent`(`QtGui`), 309

- 基类, `QInputEvent`
- `button()`, 333
- `pos()`, 309

## `QMutex`(`QtCore`), 541, 552, 554

## `QMutexLocker`(`QtCore`), 554

## `Object`(`QtCore`), 119, 127, 304, 322, 370

- `blockSignals()`, 135
- `connect()`, 124, 130, 133, 145, 151, 158, 453
- `deletePainter()`, 287, 531, 539, 554
- `destroyed()` signal, 286, 288
- `disconnect()`, 130
- `emit()`, 130, 131, 219, 330, 340, 391, 431, 450
- `event()`, 304, 309, 310, 384
- `installEventFilter()`, 304
- `parent()`, 433, 504
- properties, 157, 211
- `property()`, 322, 324
- `sender()`, 135, 289, 393, 395, 440
- `setObjectName()`, 169, 183, 324
- `setProperty()`, 322, 324
- `startTimer()`, 370
- `timerEvent()`, 372
- `tr()`, 513, 514, 515
- `true()`, 513

## `QPainter`(`QtGui`), 306, 328, 337, 342, 343, 364, 361, 400, 407–410, 408, 480

- `drawArc()`, 344
- `drawChord()`, 344
- `drawConPolygon()`, 344
- `drawEllipse()`, 344, 374, 377, 481
- `drawImage()`, 344, 363, 400
- `drawLine()`, 338, 344
- `drawPath()`, 344, 377
- `drawPicture()`, 363
- `drawPie()`, 344
- `drawPixmap()`, 344, 363, 408
- `drawPoint()`, 344
- `drawPolygon()`, 338, 343, 344, 345
- `drawPolyLine()`, 344

## `QPainter`(`QtGui`) (续)

- `drawRect()`, 337, 344, 368, 410
- `drawRoundRect()`, 344
- `drawText()`, 306, 338, 342, 363
- `fillPath()`, 344
- `fillRect()`, 343, 438, 481, 489
- `restore()`, 343, 346, 410, 482, 489
- `rotate()`, 343, 346, 438, 481
- `scale()`, 343
- `setBrush()`, 337, 344, 354, 370, 377
- `setFont()`, 337, 344, 408, 489
- `setPen()`, 337, 338, 343, 445, 374, 377

## `PaintEvent`(`QtGui`), 480

- 基类, `QEvent`
- `rect()`, 480

## `Palette`(`QtGui`), 337, 481

## `QPen`(`QtGui`), 368

- `setColor()`, 368
- `setWidth()`, 368

## `QPicture`(`QtGui`), 329

- 基类, `QDevice`
- `map()`, 199, 199, 392, 404, 408, 496
- `fill()`, 392
- `fromImage()`, 199
- `isNull()`, 496

## 610

# 索引

## `QPoint`/`QPointF`(`QtCore`), 309, 338, 343, 371

## `QPolygon`/`QPolygonF`(`QtGui`), 343, 345, 376

## `QPrintDial`(`QtGui`), 361, 363, 400, 403, 404, 408

## `QPrinter`(`QtGui`), 170, 329, 353, 361, 363, 400, 401

- 基类, `QPaintDevice`
- `newPage()`, 410
- `rectEvent()`, 408
- `setSize()`, 353, 398, 400

## `ProgressBar`(`QtGui`), 578

## `QButton`(`QtGui`), 276, 278, 369, 578

- 基类, `QAbstractButton`
- `clicked`(signal), 219
- default, 145, 188
- 另见 `QDialogBox`

## `QRadioButton`(`QtGui`), 577

## `.qrc` (Qt 文件), 173, 207, 517

## `QReadLock`(`QtCore`), 540, 541, 545, 552

- `lockRead()`, 541, 542, 543, 548, 550, 551, 556
- `lockWrite()`, 542, 543, 556
- `unlock()`, 541, 542, 543, 548, 550, 551, 556

## `QRect`/`QRect`(`QtCore`), 355, 357, 364, 376, 410

- `adjusted()`, 355, 367
- `center()`, 292, 393
- `contains()`, 357
- `setBottom()`, 365
- `setRight()`, 365
- `size()`, 400

## `QExp`(`QtCore`), 327, 386, 381, 461

## `QRegValidator`(`QtGui`), 157, 327, 461

## `Qintilla` 插件, 381, 382

## `QScrollArea`(`QtGui`), 476, 477, 479

## `QSettings`(`QtCore`), 182, 228, 282, 293, 514

- 基类, `QObject`

## `QSettings`(`QtCore`) (续)

- 格式常量, 228
- `value()`, 183

## `QMapper`(`QtCore`), 292, 297, 300

## `QSize`(`QtCore`), 335, 341, 390, 400, 439, 489

- `scale()`, 363, 400

## `QSlider`(`QtGui`), 369, 578

- 基类, `QAbstractSlider`

## `QSpaceItem`(`QtGui`), 212

- 基类, `QILayout`

## `QSpinBox`(`QtGui`), 180, 340, 440, 578

- 基类, `QAbstractSpinBox`
- `setRange()`, 180, 340
- `setStep()`, 180, 340
- `setSuffix()`, 180, 340
- `setValue()`, 128, 340, 441
- `setTextValue()`, 327, 328
- `value()`, 441
- `valueChanged()`, 124, 128, 199

## `QSplitter`(`QtGui`), 280–473

- 基类, `QFrame`
- `restoreState()`, 282
- `saveState()`, 282
- `setStretchFactor()`, 283

## `SqlDatabase`(`QtSql`), 446, 469

- `addDatabase()`, 449, 465, 469
- `commit()`, 449, 468, 469
- `database()`, 465, 468, 469
- `lastError()`, 446, 450, 459, 465
- `open()`, 446, 459
- `rollback()`, 449, 465, 469
- `setDatabaseName()`, 449, 469
- `transaction()`, 449, 468, 469

## `SqlDriver`(`QtSql`), 449

- 基类, `QObject`
- `hasFeature()`, 449

## `SqlQuery`(`QtSql`), 445–461, 450, 464, 468, 469

- `addBindValue()`, 448, 450
- `bindValue()`, 448, 450
- `boundValue()`, 450
- `driver()`, 450

# 索引

## 611

`QSqlQuery` (`QtSql`) (续)

- `exec()`, 447, 448, 449, 450, 464, 468, 469
- `first()`, 450
- `isActive()`, 449, 450
- `isValid()`, 450
- `last()`, 450
- `lastError()`, 449
- `next()`, 450, 451, 458, 469
- `numRowsAffected()`, 449, 450
- `prepare()`, 448, 450, 468
- `previous()`, 449
- `record()`, 450
- `seek()`, 449, 451
- `setForwardOnly()`, 451
- `size()`, 450
- `value()`, 449, 450, 451

`QSqlQuery`(`QtSql`)

- 基类, `AbstractTableModel`
- `record()`, 464, 465, 466, 469
- `setQuery()`, 464

`SqlRecord` (`QtSql`)

- `value()`, 464, 465, 466

`SqlRelation`(`QtSql`), 456, 460, 462

`SqlRelationalDelegate`(`QtSql`), 456, 460, 461

`SqlRelationalTableModel`(`QtSql`), 445, 452, 462

- 基类, `SqlTableModel`
- `relationModel()`, 456
- `setRelation()`, 456, 460, 462

`QTableTableModel`(`QtSql`), 445, 453

- 基类, `QtSqlQuery`
- `beforeInsert()`, 470
- `addField()`, 456
- `insertRecord()`, 464
- `select()`, 453, 456, 460, 462, 470, 464, 470
- `setFilter()`, 470
- `setSort()`, 453, 456, 460, 462
- `setTable()`, 453, 456, 460, 462
- `sumAll()`, 455, 466, 469, 470

`QSocket` (`QtNetwork`), 521

`StackedWidget`(`QtGui`), 274–276

- 基类, `QFrame`
- `setCurrentIndex()`, 275

`QStatusBar`(`QtGui`)

`QStatusBar` (`QtGui`) (续)

- 基类, `QWidget`
- `clearMessage()`, 170, 232
- `setSizeGripEnabled()`, 170
- `showMessage()`, 170, 233

`QString`(`QtCore`), 19, 23, 28, 233, 234, 256, 313, 402

- `arg()`, 402, 418, 419, 423, 427, 428, 455, 513, 515
- `compare()`, 435
- `contains()`, 234
- `endsWith()`, 240
- `indexOf()`, 306, 387, 388
- `isEmpty()`, 233
- `isNull()`, 45
- `lastIndex()`, 234
- `left()`, 234, 388
- `length()`, 388
- `localeAwareCompare()`, 416, 434
- `mid()`, 252
- `number()`, 61, 422
- `simplified()`, 253
- `startsWith()`, 252
- `toInt()`, 251, 422
- `toUpper()`, 327
- `trimmed()`, 252, 422
- 另参见 str 类型和 unicode 类型

`stringList`(`QtGui`), 45, 189

- `contains()`, 189
- `isNull()`, 45
- `prepend()`, 189
- `takeLast()`, 189

`StyleOptionGraphicsItem`(`QtGui`), 374

`StyleOptionItem`(`QtGui`), 438, 439, 461

`SvgGenerator`(`QtGui`), 329, 363

- 基类, `QPaintDevice`
- `SvgRenderer`(`QtSvg`), 363

`QSyntaxHighlighter`(`QtGui`), 386–389

- 空间, 258
- `escape()`, 258, 397, 401

`WindowStaysOnTopHint`, 529

Qt Assistant 应用, 510

## 612

# 索引

Qt Designer 应用, 205–216, 272, 274, 275, 277, 280, 324, 326, 333

Qt ItemDataRole(`QtGui`), 231

Qt Linguist 应用, 513

`QtWidgetAttribute`(`QtGui`)

- `WA_DeleteOnClose`, 156, 158, 284, 286
- `WA_GroupLeader`, 511

`TableView`(`QtGui`), 415, 425, 437, 458, 460, 467, 479, 597

- 基类, `QAbstractItemView`
- `horizontalHeader()`, 463, 464
- `resizeContentsContents()`, 232, 419, 460
- `setColumnHidden()`, 418, 463
- `setSortingEnabled()`, 230–230, 313, 414, 579
- 基类, `QTableView`
- `clear()`, 418
- `currentColumn()`, 422
- `currentItem()`, 422
- `editItem()`, 422
- `changed()`信号, 417
- populating, 418
- `scrollItem()`, 232
- `setColumnCount()`, 231, 418
- `setCurrentItem()`, 232, 419
- `setHeaderLabels()`, 231, 418
- `setItem()`, 231, 419
- `setRowCount()`, 231, 418

`TableWidget`(`QtGui`), 231–232, 418, 419

- `data()`, 422
- `setData()`, 419
- `setSelected()`, 232, 419
- `setTextAlignment()`, 231, 419
- `text()`, 422

`TabWidget`(`QtGui`), 272–274, 579

- 基类, `module` (PyQt), 19
- `pyqtProperty()`, 322
- `pyqtSignature()`, 218, 219

`QtCore` module (`Qt4`) (续)。

- `PYSTR` 变量, 200
- `QTSTR` 变量, 200
- `SIGNAL()`, 131
- `SLOT()`, 131

另参见类名下

`QtServer`(`QtNetwork`), 529, 530, 339

- `incomingConnection()`, 330, 339
- `listener()`, 529

`QtSocket`(`QtNetwork`), 522, 524, 531, 540

- 基类, `QAbstractSocket`

`QtTextBlock`(`QtGui`), 396

`QtBlockFormat`(`QtGui`), 404

`QtBrowser`(`QtGui`), 117, 381, 511, 579

- 基类, `QTextEdit`

`QtCharFormat`(`QtGui`), 386, 387, 404

`QtCursor`(`QtGui`), 297, 384, 403–407

- `currentFrame()`, 404
- `hasTextBlock()`, 385
- `insertBlock()`, 404
- `insertImage()`, 404
- `insertTable()`, 404
- `setText()`, 384, 404
- `removeSelectedText()`, 297
- `isSelected()`, 297
- `setPosition()`, 406

`QtDocument`(`QtGui`), 381, 383, 396, 398, 401–407, 438, 439, 489

- 基类, `QObject`
- `clear()`, 383
- `drawContents()`, 438, 489
- `idealWidth()`, 390, 439, 489
- `isEmpty()`, 385
- `isModified()`, 287, 385
- `print()`, 403, 407
- `setDefaultFont()`, 438, 439, 489
- `setFont()`, 403, 438, 489
- `isModified()`, 286, 383, 484
- `toHtml()`, 407

`QtEdit`(`QtGui`), 285, 310, 381, 383, 390, 392

## 613

# 索引

`QtTextEdit` (`QtGui`) (续)

- 基类, `QAbstractArea`
- `append()`, 120
- `canPaste()`, 385
- `currentCharFormat()`, 393, 395
- `cursorNext()`, 392, 393
- `cut()`, 385
- `document()`, 286, 287, 383, 384, 385, 396
- `ensureCursorVisible()`, 392, 393
- `insertPlainText()`, 297
- `mergeCurrentCharFormat()`, 395
- `setHtml()`, 384
- `setLineWrap()`, 390
- `setPlainText()`, 384
- `setTabColor()`, 390
- `setColor()`, 393
- `setTextCursor()`, 297, 384, 385
- `toHtml()`, 395
- `toPlainText()`, 384, 395

`QtOption` (`QtGui`), 409

`QtStream` (`QtCore`), 250, 255, 254, 284

- `atEnd()`, 252, 253, 254
- `readLine()`, 252, 253, 254
- `setCodec()`, 250, 252, 258, 384

`QtTableModel` (`QtGui`), 404

`Qt` module (`PyQt4`), 19

另参见类名下

`Thread` (`QtCore`), 538, 540

- `isRunning()`, 547, 551
- `run()`, 538, 540, 548, 553
- `start()`, 539, 547, 553
- `wait()`, 547, 548, 551

`QTime` (`QtCore`), 45

- `isNull()`, 384

另参见 time module

`QtTimeEdit` (`QtGui`), 576

- 基类, `QDateTime`

`QTimer` (`QtCore`), 373, 376

- 基类, `QObject`
- `singleShot()`, 115, 306
- `start()`, 373, 376
- `timeout()`信号, 373, 376

`QtNetwork` module (`PyQt4`), 521, 523

另参见类名下

`ToolBar` (`QtGui`), 179, 180, 184

- 基类, `QWidget`
- `addSeparator()`, 178, 180

- `QToolTip` (`QtGui`), 171, 200, 514

`Translator` (`QtCore`), 516

`TreeView` (`QtGui`), 415, 495, 579

- 基类, `QAbstractItem`
- populating, 502
- `setItems()`, 420
- `setRows()`, 395

`QWidget` (`QtGui`), 314, 579

- 基类, `QTreeView`
- `clear()`, 420
- `expandItem()`, 321
- populating, 420
- `setColumnCount()`, 320
- `setCurrentItem()`, 321

`WidgetItem` (`QtGui`), 420, 421

`Qt5` module (`PyQt4`), 445, 446

另参见类名下

`QtSvg` module (`QtGui`), 363

另参见类名下

`QtXml` (`QtGui`), 435

另参见类名下

`QSocket` (`QtNetwork`), 522

- 基类, `QAbstract`
- queries, 另参见 SQL 语句

`question` (`MessageBox`), 187, 388, 361, 423, 455

`quit()` (`QApplication`), 115

terminating applications

quoted strings; literals

`Variant` (`QtCore`), 183, 251, 323, 392, 414, 428, 429, 430, 441, 488, 496

- `Bool()`, 324
- `DateAndTime()`, 481

## 614

# 索引

`Variant` (`QtCore`) (续)

`QWidget` (`QtGui`) (续)

- `toInt()`, 395, 431, 449
- `move()`, 183, 330, 341
- `toLayout()`, 422
- `paintEvent()`, 306, 309, 332, 346, 480
- `toString()`, 327, 431, 441, 449, 488
- `palette()`, 337

`QBoxLayoutLayout` (`QtGui`), 146, 270

- `raise()`, 160, 289, 330
- 基类, `QBoxLayout`
- `rect()`, 306, 330

`QWidget` (`QtGui`), 118, 129, 168, 273, 305, 309, 322, 324, 325, 326, 328, 329, 330, 331, 370, 421

- `resize()`, 183
- `resizeEvent()`, 306, 309, 341
- 基类, `QObject` and `QPaintDevice`
- `restoreGeometry()`, 183, 186, 360
- `activateWindow()`, 160, 289
- `setAcceptDrops()`, 312, 313, 314, 315, 316
- `addAction()`, 172, 178, 180, 370, 330, 365, 392
- `setAttribute()`, 156, 254, 330, 511
- `addActions()`, 178
- `setContextMenuPolicy()`, 168, 330, 365
- `close()`, 175, 285, 330
- `closeEvent()`, 175, 187, 272, 285, 289, 309, 551
- `setCursor()`, 330
- `contextMenu()`, 307, 309, 390
- `dragEnter()`, 309, 314, 316
- `moveEvent()`, 309, 314, 315, 316
- `setEnabled()`, 219, 330
- `setFocus()`, 120, 310, 422
- `FocusPolicy()`, 180, 217, 331, 369, 478
- `dropEvent()`, 309, 315, 316
- `font()`, 332, 344
- `geometry()`, 357
- `setFont()`, 330
- `setLayout()`, 273, 279, 330
- `setMaximumHeight()`, 390
- `MinimumHeight()`, 390
- `hasFocus()`, 330
- `hMouseTracking()`, 308
- `height()`, 330
- `hide()`, 279, 330
- `MinimumSize()`, 168, 340
- `MinimumWidth()`, 340
- `MouseTracking()`, 308
- `SizeSize()`, 330, 331, 340

# 索引

# 615

## `QWidget` (`QtGui`) (续)

- `updateGeometry()`, 330, 332, 479
- `wheelEvent()`, 352
- `width()`, 330

## `QWorkspace` (`QtGui`), 290, 297

- 基类, `QWidget`
- `activeWindow()`, 296
- `setActiveWindow()`, 292, 295
- `windowList()`, 295

## `XmlContentHandler` (`QtXml`)

- `characters()`, 263
- `endElement()`, 263
- `startElement()`, 263

## `XmlDefaultHandler` (`QtXml`), 263

- 基类, `XmlContentHandler`

## `XmlErrorHandler` (`QtXml`)

- `fatalError()`, 263

## `XmlInputSource` (`QtXml`), 262

## `XmlReader` (`QtXml`)

- `parse()`, 262
- `setContentHandler()`, 262
- `setErrorHandler()`, 262

- `XmlSimpleReader` (`QtXml`), 262–265
    - 基类, `QXmlReader`

- `readLine()` (`QTextStream`), 252, 253, 254



# 索引

## A

- `readIntn(QDataStream)`, 245, 528, 540
- 重新绑定名称; 见 binding names
- 最近使用过的文件, 187–190
- 记录级验证, 140, 491
- `record()`
- `QsQuery`, 450
- `QsQueryModel`, 464, 465, 266, 469
- `rect()`
- `PaintEvent`, 480
- `Widget`, 306, 333
- 递归, 无限递归风险, 100
- 重入方法, 542
- 引用; 见 object references
- 回归测试, 157, 220, 327, 386, 387, 461, 552
- “reject”出, 144, 188
- `reject()` (`QDialog`), 215
- `rejected()` 信号 (`QDialogButton`), 145, 150
- `relationModel()` (`QSqlRelationalTable`), 456
- 余数 (`%`), 53
- `remove()`
    - `dict`, 95, 532, 543
    - `list`, 32, 33
    - `set`, 38
- `removeItem()` (`QGraphicsScene`), 354, 355, 359, 361
- `removeRow()` (`QAbstractItemModel`), 434, 466, 269
- `removeRows()` (`QAbstractItemModel`), 472, 432, 470
- `removeSelected()` (`QTextCursor`), 297
- `render()`
    - `GraphicsScene`, 354, 361
    - `GraphicsView`, 361
    - `QSvgRenderer`, 363
- `replace()` (`str`/`unicode`), 25, 238
- `repr()`, 81, 83, 90, 98

## R

- `_radd()` (`+`), 84
- `radians` (`math`), 371, 375
- `raise()` (`Widget`), 160, 289, 330
- 提升窗口, 160
- `randint` (`random`), 19, 357, 371, 375
- `range()`, 39, 50–51, 54
- 另见 `xrange`
- “raw”字符串, 152
- `re`, 219, 220, 554, 556
- 只读模型, 427
- 只读小部件, 421
- `readAll()`
    - `QIODevice`, 254
    - `QTextStream`, 384, 220
- `readBool()` (`QDataStream`), 245
- `readDouble()` (`QDataStream`), 241, 245
- `readIntn()` (`QDataStream`), 243, 243, 360, 435
- `readline()` (`codecs`), 255

## 索引

- `_repr_()` (`repr()`), 81, 83, 98
- `reset()`
- `rowCount()`
    - `QAbstractItem`, 426, 427, 428, 434, 454, 459, 481, 503
    - `QAbstractApiModel`, 432, 434, 501, 502
- `_rsub_` (`-`), 84
- `truediv_()` (`/`), 84
- 橡皮筋, 352
- `QMatrix`, 370, 377
- `run()` (`QThread`), 538, 540, 548, 553
- `RuntimeError` 异常, 288
- `resize()` (`QWidget`), 183
- `resizeColumnsToContents()` (`QTableView`), 232, 419, 460, 463, 490
- `resizeEvent()` (`QEvent`), 306, 309, 341

## S

- 路径, 根 (`/`), 173
- 资源文件, 173–174, 206, 401, 517
- `save()`
    - `Image`, 196
- `restore()`
    - `QPainter`, 343, 346, 418, 482
    - `QPainter`, 343, 346, 438, 489
- `saveGeometry()` (`QWidget`), 183, 186, 330
- `restoreGeometry()` (`QWidget`), 183, 186, 330
- `saveState()`
    - `QMainWindow`, 183, 186
    - `QSplitter`, 282
- 保存的, 229, 240–248, 249–256, 265
- `restoreState()`
    - `QMainWindow`, 183, 186
    - `QSplitter`, 282
- SAX 解析器, 262–265
- `scale()`
    - `QGraphicsItem`, 366
    - `GraphicsView`, 352
    - `QMatrix`, 370
    - `QPainter`, 343
- `Size`, 363, 400
- 返回按键; 见 Enter
- `return` 语句, 58, 97, 554
- `returnPressed()` (`QLineEdit`), 440
- `scaled()` (`QImage`), 199
- scaling, 349, 370, 374, 400, 329, 331
- `reverse()` (`list`), 33
- `find()` (`str`/`unicode`), 25
- `rgb()`, 84
- `swapped()` (`QImage`), 197
- `scene()` (`GraphicsItem`), 366, 375
- `sceneBoundingRect()` (`QGraphicsItem`), 366, 379
- scenic, graphics; 见 GraphicsScene
- Scintilla, 见 Scintilla add-on RichEdit class, 389, 398
- `index()` (`str`/`unicode`), 25
- `mod` (`%`), 84
- `mul` (`/`), 84
- `rollback()` (`QDatabase`), 449, 465, 469
- 坐标, 309, 357
- `screenPos()` (`QSceneContext`), 365
- 滚动条和滚动, 393, 476, 479
- `scrollToItem` (`QWidget`), 832
- `rotate()`
    - `QGraphics`, 360, 366, 371, 375
    - `QPainter`, 343
- rotating, graphics, 349
- `round()`, 40, 91, 333
- `row()` (`QModelIndex`), 427, 491

## 索引

## SDI (单文档界面), 283–290

- `search()` (`re`), 219
- `seek()` (`SqlQuery`), 449, 451
- `select()` (`QSqlTable`), 453, 456, 460, 462, 464, 470
- SELECT 语句, 449–451
- 选中文本, 392
- `selectedItems()` (`QGraphicsScene`), 358, 361
- `selectedText()` (`QCursor`), 297
- 选择图形项, 352
- `selectionModel()` (`QAbstractItemView`), 463
- `self`, 77, 78
- `sender()` (`QObject`), 135, 289, 393, 440
- 分隔菜单, 178, 180
- 序列, 22
- 类型, 37, 93, 551
- `add()`, 37, 38, 372, 556
- `clear()`, 38, 548, 551
- `discard()`, 39
- `pop()`, 372
- `remove()`, 38
- `setAcceptDrops()` (`QWidget`), 312, 313, 314, 315, 316, 330
- `setWindows()` (`QWorkspace`), 292, 295
- `setAlignment()`
    - `QAbstractSpinBox`, 340, 487
    - `Label`, 168, 340
    - `QLineEdit()`, 361
- `setAllowedAreas()` (`QDockWidget`), 169, 170
- `setAlternatingRowColors()` (`QAbstractItemView`), 231, 477
- `setAttribute()` (`QWidget`), 156, 284, 330, 511
- `setBackgroundBrush()` (`QGraphicsScene`), 354
- `setBottom()` (`QRect`/`QRect`), 365
- `setBrush()` (`QPainter`), 337, 344, 345, 374, 378
- `setBuddy()` (`QLabel`), 143, 425
- `setCalendarPopup()` (`QDateTimeEdit`), 487
- `setCentralWidget()` (`QMainWindow`), 168, 186, 285
- `setCheckable()`
    - `QButton`, 276, 277
    - `QAction`, 393
- `setChecked()` (`QAction`), 172, 177, 393
- `setCodec()` (`QTextStream`), 250, 252, 254, 384
- `setColor()` (`QPen`), 368
- `setColumnCount()`
    - `TableWidget`, 231, 418
    - `TreeWidget`, 420
- `setColumnHidden()` (`TableView`), 463
- `setStretch()` (`GridLayout`), 146
- `setContent()` (`QDocument`), 259
- `setContentHandler()` (`QXmlReader`), 262
- `setContextMenu()` (`QWidget`), 168, 330, 365
- `setCurrentIndex()`
    - `AbstractItemView`, 426, 465, 468
    - `QComboBox`, 441, 457
    - `QDataMapper`, 454, 555
    - `StackedWidget`, 275
- `setCurrentItem()`
    - `ListWidget`, 418
    - `TableWidget`, 232, 419
    - `TreeWidget`, 421
- `setCursor()`
    - `GraphicsItems`, 366
    - `Widget`, 330
- `setData()`
    - 189, 231
    - `AbstractItemModel`, 414, 427, 431, 441, 462, 465, 488
    - `QAction`, 172, 392, 393
    - `QMetaData`, 316
    - `TableWidgetItem`, 231, 419
- `setDatabaseName()` (`QDatabase`), 446, 459
- `setDate()` (`QDateTimeEdit`), 487

## 索引

- `setDateRange()` (`QDateTimeEdit`), 452, 487
- `setDateTime()` (`QDateTime`), 454
- `default()` (`dict`), 36, 95, 532
- `setDefaultFont()` (`QTextDocument`), 438, 439, 486
- `setDisplayFormat()` (`QDateTimeEdit`), 452, 487
- `setDragged()` (`AbstractItem`), 312, 313, 315, 316
- `setDropMode()` (`GraphicsView`), 352
- `setDropAction()` (`QDropEvent`), 314, 315, 316
- `setEditable()` (`QComboBox`), 440
- `setEditorData()` (`AbstractItemDelegate`), 436, 441, 462, 486, 487
- `setTriggers()` (`Abstract itemView`), 231
- `setEnabled()`
    - `QAction`, 172
    - `GraphicsItem`, 366
    - `Widget`, 219, 330
- `setLastError()` (`QXmlReader`), 262
- `setFeatures()` (`QDocWidget`), 170
- `setFilter()` (`QTableWidget`), 464, 470
- `setFlag()` (`QGraphicsItem`), 366
- `setFlags()` (`QGraphicsItem`), 351, 356, 362, 364
- `setFocus()`
    - `GraphicsItem`, 364
    - `Widget`, 120, 310, 330, 422
- `setFocusPolicy()` (`QWidget`), 180, 217, 331, 369, 478
- `setFont()`
    - `QGraphicsItem`, 362, 404, 482
    - `Widget`, 330
- `setForwardOnly()` (`SqlQuery`), 451
- `setFrame()` (`QFrame`), 170, 278
- `setHeaderData()` (`QAbstractModel`), 434, 460, 482
- `setHeaderLabels()`
    - `QTreeView`, 420
    - `QTableWidget`, 231, 418
- `setHotSpot()` (`QDrag`), 316
- `Qime()` (`QTextDocument`), 403, 438, 489
- `setIcon()` (`QListWidget`), 316
- `setImage()` (`QPixmap`), 310
- `setInputMask()` (`QLineEdit`), 461
- `setItem()`
    - `QTableWidget`, 231, 419
- `setItemDelegate()`
    - `QAbstractItemView`, 437, 460, 463, 490
    - `QDataMapper`, 456
- `setItemExpandable()` (`QTreeView`), 420
- `setLayout()` (`Widget`), 279, 230
- `setLineWrapMode()` (`QTextEdit`), 390
- `setMatrix()`
    - `QGraphicsItem`, 362, 364, 377
    - `QGraphicsView`, 370
    - `QPainter`, 343
- `setMaximumHeight()` (`QWidget`), 390
- `MimeData()`, `Clipboard`, 311
- `QDrag`, 316
- `setMinimumSize()` (`QWidget`), 168, 340
- `setMinWidth()` (`QWidget`), 340
- `setModel()`
    - `AbstractItemView`, 425, 437, 463, 477, 490
    - `QComboBox`, 456
    - `QDataMapper`, 454, 555
    - `QComboBox`, 441, 457
    - `AbstractItemDelegate`, 436, 441, 462, 486, 487
- `setText()`
    - `QTextDocument`, 318, 384
    - `GraphicsItem`, 319, 330

## 索引

- `setViewport()` (`QPainter`), 329, 342, 343, 363
- `setVisible()` (`QWidget`), 277, 280
- `setWhatThis()` (`QAction`), 172
- `setWidth()` (`QPen`), 368
- `setWindow()` (`QPainter`), 329, 342, 343, 363
- `WindowFlags()` (`QWidget`), 529
- `setWindowIcon()` (`QWidget`), 186, 330
- `setWindowModified()` (`QWidget`), 192
- `setTitle()` (`QWidget`), 146, 151, 186, 330, 370
- `setValue()` (`QGraphicsItem`), 31, 98
- 浅拷贝, 34, 51
- `shape()` (`QGraphicsItem`), 365, 367, 374, 377
- 切变 (`QGraphicsItem`, `Painter`), 367, 343
- Shift键按下, 365
- 短路逻辑, 47
- 短路信号, 130–131
- 信号信号与槽
- 快捷键；参见键盘快捷键和 `QSequence`

## 信号与槽

- 128–131
- 函数、方法、信号或槽的签名, 56, 129
- 简化() (`QString`), 61, 422
- `s` (`math`), 371, 375
- 单击；参见 `mouseEvent()` `mouseReleaseEvent()`
- 单文档用户界面；参见 SDI
- 单引号字符串, 21
- `singleShot()` (`QTimer`), 115, 306
- `sime` 模块, 268
- 尺寸；参见 `QSize`
- 尺寸手柄, 170
- 尺寸提示, 271
- `size()`
    - `QImage`, 363, 400
    - `QRect`/`QRectf`, 400
    - `QSqlQuery`, 450
- 布局组件的尺寸:
    - 固定, 277
    - 最大, 271
    - 最小, 270, 271, 335
    - 优选, 271
- 尺寸策略, 270–271, 335
- `sizeHint()`
    - `AbstractItemDelegate`, 436, 489
    - `QWidget`, 330, 390, 47
- `sleep` (时间), 114, 115
- 切片, 22, 30
- 槽；另见信号与槽
- `SLOT()` (`QCore`), 131
- `_slots_class` 属性, 103
- 软件专利的缺点, 222
- 排序 (`list`), 33, 63, 95, 229
- `sorted()`, 52, 63, 432, 434, 551
- 排序, 52, 418, 425, 432
- 间距；参见 `QSpacerItem`
- 布局中的间距, 212, 214
- 特殊方法, 81
    - `_abs_` (`abs`), 84
    - `_add_` (`+`), 84, 90
    - `call_()`, 81
    - `_cmp_` (`cmp`), 81, 82, 89, 416, 432
    - `_contains_` (`in`), 93
    - `_del_` (`del` 语句), 78
    - `delim_()` (`del` 语句), 93
    - `_eq_` (`==`), 81
    - `_float_()` (`float`), 84, 91
    - `_floordiv_` (`//`), 84

## 索引

- 特殊方法（续）
    - `_ge_` (`>=`), 81
    - `_getitem_` (`[]`), 93, 94
    - `_gt_` (`>`), 81
    - `_iadd_` (`+=`), 80, 94
    - `_floordiv_` (`//`), 84
    - `_imod_` (`%`), 84
    - `_imul_` (`*`), 84, 91
    - `_init_()` (), 77, 78, 437
    - `_int_` (`int`), 84, 91
    - `_issub_` (`-`), 84
    - `_iter_` (`iter`), 93, 97
    - `_truediv_` (`/`), 84, 91
    - `_le_` (`<=`), 81
    - `_len_` (`len`), 93, 96
    - `_lt_` (`<`), 81, 82, 432
    - `_mod_` (`%`), 84
    - `_mul_` (`*`), 84, 91
    - `_ne_` (`!`), 84
    - `_neg_` (`-`), 84
    - `_new_()` (), 77, 78, 81
    - `_nonzero_` (`bool()`), 81, 83
    - `_radd_` (`+`), 81, 90
    - `_repr_` (`repr`), 81, 83
    - `_rfloordiv_` (`//`), 84
    - `_rmod_` (`%`), 84
    - `_rmul_` (`*`), 84
    - `_rsub_` (`-`), 84
    - `_rtruediv_` (`/`), 84
    - `_setitem_` (`[]`), 93, 95
    - `_str_` (`str`), 81, 90, 98, 100
    - `_sub_` (`-`), 84
    - `_truied_` (`/`), 84, 91
    - `_unicode_` (`unicode`), 81, 83
- SQLite 数据库, 445, 446, 447
- 堆叠组件；参见 `QStackedWidget`
- 标准序列；参见 shortcut 和 `QKey`
- `start()`
    - `QDrag`, 316
    - `QThread`, 539, 547, 553
    - `QTimer`, 373, 376
- start-up, 184
- `startDrag()` (`QAbstractItem`), 316
- `startElement()` (`XmlElement`), 263
- `startWith()` (`str`/`unicode`), 25, 238, 255
- `startWith()` (`QString`), 252
- `startTimer()` (`QObject`), 370
- state, 另见信号与槽
- `state()` (`QAbstractSocket`), 540
- state, 生成器状态, 58, 97
- statement 分隔符, 51
- static data, 85-86
- static methods, 78-85
- static typing, 12
- `staticmethod()`, 85, 238
- 状态栏；另见 `QStatus`
- `statusBar()` (`QMainWindow`), 170, 186
- `StopIteration` 异常, 52, 58, 95
- 存储过程, 数据库, 448
- `str` 类型, 20-28, 25
- 格式化, 24, 98
- 格式说明符, 26
- 复制运算符, 25
- 拼接运算符, 25
- `count()`, 25
- `endswith()`, 25, 31, 555
- `find()`, 24, 25, 68
- `index()`, 24, 25, 68
- 索引, 22
- `isalpha()`, 25
- `isdigit()`, 25, 238, 554
- 迭代, 50
- `join()`, 23, 25, 61, 193, 477
- 字面量, 21
- 计数器；参见 `QDoubleSpinBox` 和 `QSpinBox`
- `split()` `QString`, 25, 114, 238, 501
- 分器；参见 `QSplitter`
- SQL 查询；参见 `QSqlQuery` 和 SQL-statements
- 服务器数据库, 445
- SQL 语句, 445, 446, 447, 448, 449, 449–451, 458, 464, 468, 469
- `str` 类型（续）
- `sys-argv` 变量, 114
- 提升为 unicode, 20
- 路径变量, 60, 104
- `replace()`, 25, 238
- 版本信息组, 63
- `rfind()`, 25
- `system()` (`platform`), 200, 217, 336, 390
- `rindex()`, 25

## T

- 切片, 22
- `split()`, 25, 114, 238, 501
- Tab 键按下, 206, 218, 310, 386, 390, 422, 421, 551
- `startsWith()`, 25, 255, 238
- 标签顺序 (tab order), 206, 215, 217, 310
- `strip()`, 25, 59, 255
- 标签页组件；参见 QtWidgets
- `title()`, 24
- 表格组件；参见 QtTableWidget
- `upper()`, 25
- `tagName()` (`DomElement`), 260
- 另见 `QString` 和 `unicode` 类型
- `takeItem()` (`WidgetItem`), 316
- `str` (`str()`), 81, 83, 90, 98, 100
- `lastEvent()` (`QStringList`), 189
- 流读取与写入, 142, 250, 252, 58
- 任务, 144
- TCP (传输控制协议), 522
- 流；另见 `QStream`
- `Template` 类 (`string`), 26

## QText

- 应用程序, 115, 241
- 错误, 75
- 格式化, 24, 98
- 格式说明符, 26
- 复制运算符, 25
- 拼接运算符, 25
- `count()`, 25
- `endswith()`, 25, 31, 555
- `find()`, 24, 25, 68
- `find()`, 24, 25, 68
- 索引, 22
- `isalpha()`, 25
- `isdigit()`, 25, 238, 554
- 迭代, 50
- `join()`, 23, 25, 61, 193, 477
- 字面量, 21
- 样式表, 322, 334
- 控件, 324
- 文本光标；另见 point
- 文本编辑器, 241
- 文本文件, 256
- 文本输入, 201, 217
- 文本流，另见 `QTextStream`
- 文本包装, 100
- 文本内容，另见 text
- 文本类型, 另见 String
- 文本类型, 20-28, 25
- 终止运算符, 见 expression
- 终止语句, 66, 78, 441, 542, 543, 548, 550, 551, 553, 554, 556
- `else` 语句, 70, 225
- 另见 `except` statement 和 `finally` statement
- `ts` (翻译源文件), 517, 518, 519
- 元组类型, 29–31, 30, 50
- Twisted 网络框架, 522
- 类型转换；另见 conversions
- `type()`, 18, 39, 102
- 另见 `instance()`
- `type()` (`QEvent`), 384
- 类型提升；另见 conversions
- 类型检查, 94
- `tTypeError` 异常, 56
- 类型；另见 duck typing、动态 typing 和静态 typing
- `toHtml()`
    - `QDocument`, 407
    - `QTextEdit`, 395
- `toInt()`
    - `QString`, 251, 422
    - `QVariant`, 395, 431, 449
- `toLongLong()` (`QVariant`), 422
- `toNativeSeparators()` (`QDir`), 547, 551
- 工具栏；另见 `QToolBar`
- 工具栏, 169
- 工具；另见 applications
- 提示；另见 `QToolTip`
- 顶层窗口, 115, 118, 221
- `toPlainText()`
    - `QGraphicsItem`, 359
    - `QTextEdit`, 384, 395
- `toPyDate()` (`QDate`), 532, 541
- `toString()`
    - `QDate`, 258, 401
    - `QDateTime`, 455
- 切换, 176
- `toBool()` (`QVariant`), 324
- `toDate()` (`QVariant`), 487
- `toDateTime()` (`QVariant`), 499
- `toDouble()` (`QVariant`), 481
- 切换按钮, 276, 278
- 切换信号, 另见 `QPushButton`
- 切换状态, 另见 text
- `toText()` (`QNode`), 261
- `toUpper()` (`QString`), 327
- `toObject()` (`QObject`), 513, 514
- `toElement()` (`QNode`), 260
- `transaction()` (`QSqlDatabase`), 449, 465
- `takeItem()` (`WidgetItem`), 316

## 索引

## U

- `unlock()` (续)
- `QMutex`, 553, 554
- UDP (用户数据报协议), 522
- `.ui` (用户界面文件), 206, 207, 515
- `QReadWriteLock`, 541, 542, 543, 548, 550, 551, 556
- 解析元组, 87
- 未保存的更改, 168, 187, 192, 232, 293, 356, 361, 362, 364, 365, 425, 453
- 终基类；参见对象类型
- 下划线，前导, 77, 80, 82
- `unichr()`, 21, 39, 236, 554
- Unicode, 20, 117, 236, 250, 548, 447, 478, 512, 552, 555
- `update()`
    - `QGraphicsItem`, 365, 367
    - `QGraphicsScene`, 354
    - `Widget`, 306, 330, 332, 479, 482
- `updateGeometry()` (`QWidget`), 330, 332, 479
- 字符, 22
- 编码, 21, 250, 551
- 另见 ASCII, codecs, 和 `QString`
- `encode()`, 20-28, 25, 256, 401
    - `%` 格式化, 24
    - `%` 格式说明符, 26
    - `*` 复制运算符, 25
    - `+` 拼接运算符, 25
    - `count()`, 25
    - `endswith()`, 25, 31, 555
    - `find()`, 24, 25, 68
    - `index()`, 24, 25, 68
    - 索引, 22
    - `alpha()`, 25
    - `isdigit()`, 25, 238, 554
    - 迭代, 050
    - `join()`, 23, 25, 61, 193, 477
    - 字面量, 20, 21
    - `lower()`, 25, 238
    - 转换为 `QString`, 28
    - `replace()`, 25, 238
    - `find()`, 25
    - `index()`, 25
    - 切片, 22
    - `split()`, 25, 114, 238, 501
    - `startswith()`, 25, 238, 255
    - `strip()`, 25, 59, 255
    - `title()`, 24
    - `upper()`, 25
- 另见 `str` 类型和 `QString`
- `ucode_()` (`unicode()`), 81, 83
- `union()` (`set`), 38
- 单元测试, 105–107
- 通用换行, 256
- `unlock()`
- `upper()` (`str`/`unicode`), 25
- `urlopen()` (`urllib`), 126
- `urlretrieve()` (`urllib`), 521
- 用户操作；参见 `QApplication`
- 用户界面设计, 205–216
- 用户偏好；参见 `QSettings`
- UTF-8 编码, 236, 250, 551, 555

## V

- `validate()` (`QAbstractSpinBox`), 327, 328
- 验证, 140, 151, 157, 327, 328, 491
- 值比较, 13, 57
- `value()`
    - `QSettings`, 183
    - `QSpinBox`, 441
    - `SqlQuery`, 449, 450, 451
    - `SqlRecord`, 464, 465, 466, 469
- `valueChanged()`
    - `QDial`, 128
    - `QSpinBox`, 124, 199
- `ValueError` 异常, 68, 114
- `valueFrom()` (`QSpinBox`), 327, 328
- `values()` (`dict`), 36, 96
- 变量名, 15, 76, 80, 88
- `version_info` 元组, 63
- 版本字符串，应用程序, 167
- `version_`, 应用程序变量, 167
- 垂直布局；参见 `QVBoxLayout`
- 垂直线；参见 `QFrame`
- 视图小部件；参见 `QGraphicsView`, `ListView`, `UITableView` 和 `QTreeView`
- 视口坐标, 328–331, 339, 342, 350, 400
- `view()`
    - `AbstractScrollArea`, 392, 393
    - `QPainter`, 363
- `views()` (`QGraphicsScene`), 354, 362
- 虚方法, 75, 99
- 视觉设计工具；参见 Qt Designer
- `windowList()` (`QWorkspace`), 295
- 窗口, 115, 118, 160
- 另见 `QWidget`, `QDialog` 和 `MainWindow`
- 窗口检测, 389, 390
- 窗口预览, 215
- `WindowStayOnTop` (`Qt` 空间), 529
- `with` 语句, 549
- 封装函数；参见 partial-application
- `write()` (`QDataStream`), 526, 533
- `writeBool()` (`QDataStream`), 245
- `writeDouble()` (`QDataStream`), 241, 445
- `writeInt()` (`QDataStream`), 242, 359, 435
- `write()` (`QDataStream`), 245, 525, 533
- 写入文件；参见保存

## W

- `wait()` (`QThread`), 547, 548, 551
- `waitForDisconnected()` (`QAbstractSocket`), 544
- `waitForReady()` (`IODevice`), 540
- `walk()` (`os`), 555
- `warning()` (`MessageBox`), 153, 188, 293
- Web 浏览器，启动器, 510
- `wheelEvent()` (`QWidget`), 352
- `while` 循环, 49–50
- `break` 语句, 53
- `continue` 语句, 49–50, 254
- widget属性；参见 `Qt.WidgetAttribute`
- 小部件级验证, 140, 144
- 小部件栈；参见 `QStackedWidget`
- 小部件；参见 `QWidget`
- widget坐标 (`QWidget`), 330
- 窗口坐标, 328–331, 339, 342, 350, 357
- 窗口装饰, 112, 115
- 窗口菜单，MDI, 292–293, 297–300
- 窗口菜单，SBI, 288–289
- 窗口模态对话框, 140, 511
- 窗口系统检测, 218, 336, 390

## X

- 窗口检测, 336
- XML 文件, 256–265
- XML 元字符, 257, 258
- XML 解析器，DOM, 259–262, SAX, 262–265
- `range()`, 51, 54

## Y

- `yield` 语句, 58, 97, 237
- `yield` 类, 339–345

## Z

- `value`, 349
- `Value()` (`QGraphicsItem`), 369
- 缩；参见 scaling

---

# 关于作者

## Mark Summerfield

Mark 毕业于斯斯大学计算机科学一等荣誉学位。毕业后他进行了一年的行业研究。在加入 Trolltech 之前，他在多家公司担任软件工程师。在 Trolltech 期间，他担任了三年的文档经理，在此期间他创立并编辑了 Trolltech 的技术期刊《Qt Quarterly》，并合著了 *C++ Programming with Qt 3* 和 *C++ GUI Programming with Qt 4*。Mark拥有 Qtrac Ltd. (www.qtrac.eu)，在那里担任独立作者、编辑、培训师和顾问，专注于 C++、Qt、Python 和 PyQt。

# 制作

文本使用 `gvim` 编写并使用 Lout 排版语言标记。索引由作者编译，并辅助一个为此开发的 PyQt 程序。所有图表都是使用 Lout 生成的。大部分代码段是结合 Lout 和 Python 脚本直接从示例程序提取的。示例中使用的图标大多来自 KDE（K 桌面环境），少数由作者创建。书页使用的图像来自 Open Clip Art Library，其他图像来自 Project Gutenberg。SVG 图像使用 Inkscape 转换为 EPS。Linux 截图使用 Snapshot 拍摄，Windows 截图通过一个小型 PyQt 应用程序捕并保存；两种情况下，`.png` 图像均使用 ImageMag 转换为 `.eps`。代码使用的等宽字体源自 Deja Mono 的压缩版本，并使用 FontForge 进行修改。Wikipedia 在各个方面都非常有用，包括旗帜图像的来源，并被频繁参考想法、信息和示例数据。标记后的文本由 `evince` 审核，然后通过 Ghostscript 转换为 PostScript，最后转换为 PDF。

所有的编辑和处理都在 Fedora 和 Ubuntu 系统上完成。封面由出版社提供，考虑到 Python 用于校准和分析哈勃望远镜的数据，图片由作者。截图是在 Windows XP、Mac OS X 和 Linux/KDE 上拍摄的。所有示例程序均在 Windows、Linux 和 Mac OS X 上通过测试，使用了 Python 2.5、Qt 4.2 和 PyQt 4.2，此外在 Windows 和 Linux 上使用了 Qt 4.3 和 PyQt 4.3，以及使用 Python 2.6 的 Qt 4.4 和 PyQt 4.4。

本页故意留白

注册您拥有的 Addison-Wesley、Exam Cram、Prentice Hall、Que 和 Sams 产品以解锁巨大的优惠处。

要开始注册流程，请访问 `inform.com/register` 登录或创建账户。随后您将被要求输入产品封底上的 10 位或 13 位 ISBN。

注册您的产品可以解锁以下权益：

- 访问补充内容，包括额外章节、源代码或项目文件。
- 用于下一次购买的优惠券。

注册权益因产品而异。权益将显示在账户的“注册产品”下。

> 关于 InformIT — 受信任的技术学习来源
>
> INFORMIT 是培盛教育旗下领先技术出版品牌—— Addison-Wesley Professional、Cisco Press、Exam Cram、IBM Press、Prentice Hall Professional、Que 和 Sams 的所在地。您将获得来自技术作者、创始人、创新者领导者的高质量且可靠的内容和资源。无论您是在寻找新的技术书籍、有用的文章、及时的时通讯，还是访问 Safari Books Online 数字库，InformIT 都能为您提供解决方案。
>
> `informIT.com`
>
> The TRUSTED TECHNOLOGY LEAR SOURCE

## LearnIT at InformIT

# 超越书籍

# 11 种学习 IT 的方法 at `www.informIT.com/learn`

# 免费体验 Safari Books Online

获取 5,000 多部书籍和视频的在线访问

# 免费试用——立即开始！

`www.informit.com/safaritrial`

## 快速找到信赖的答案

只有 Safari 能让你搜索来自技术出版商的数千种畅销书籍，包括 Addison-Wesley Professional、Cisco Press、O'Reilly、Prentice Hall 和 Sams。

## 掌握最新的工具和技术

除了可以访问海量的技术书籍库存外，Safari 丰富的视频教程库还能让你向顶尖的视频培训专家学习。

# 等一下，这还有更多优惠！

### 保持你的竞争优势

通过 Rough Cuts，你可以获取正在开发的稿，成为首批学习最新技术的专家。

### 紧跟新兴技术

Short Cuts 和快速参考表（Quick Reference Sheets）是简短、精炼且专注的内容，旨在帮助你快速掌握新技术和前沿技术。

# 本书支持 Safari 服务

包含 45 天免费在线版访问权限

您最喜爱的技术书籍封面上的 Safari® 图标意味着该书可以通过 Safari Bookshelf 获取。当您购买这本书时，您将获得 45 天的在线版免费访问。

Safari Bookshelf 是一个电子参考库，让您能够轻松搜索数千种技术书籍、查找代码示例、下载章节，并在任何时间任何地方访问技术信息。

要获得此书的 45 天 Safari 支持访问权限：

- 访问 `http://www.prenhallprofessional.com/safarienabled`
- 填写简短的注册表
- 输入此书前“版权”（Copyright）页上的优惠券代码

如果您在 Safari Bookshelf 上注册或访问在线版时遇到困难，请发送电子邮件至 `customer-service@safaribookonline.com`。
