# Python：Python 编程代码高级指南





















# 引言

感谢你的阅读，并祝贺你选择了《Python：使用 Python 编写代码的最佳实践》。这本书包含了关于如何更有效地进行 Python 编程的经过的步骤和策略。当你第一次学习 Python 时，他们会教你如何编写代码，但在很多情况下，他们不会教你如何编写整洁的代码。

如果你和任何 Python 程序员交流，问问他们 Python 是什么样的。我保证他们会告诉你，主要原因之一是因为它易于阅读。事实上，这是 Python 语言绝对的核心，因为计算机代码被阅读的次数远大于编写的次数。这在很大程度上归功于 Python 代码遵循一套指南和“Python 式”（Pythonic）习惯——如果你听到程序员提到代码的某部分不“Pythonic”，意味着它没有遵循这些指南，并且没有以任何方式表达意图。

代码风格和布局至关重要，你所使用的风格的一致性也是如此。尽管如此，有时一致性并不是正确的选择，而指南简单并不适用——你必须知道什么时候是那个时候，以及何时在进行 Python 编程时该做出最佳判断。

通过本指南，我将向你展示编写代码的绝对最佳方法，整理你的程序并使其变得更加有效、高效。我不会只给你基础知识。我将深入探讨你需要了解的一切，从代码布局到如何编写函数、习惯和命名。

我将谈论空格和制表符、字符串和方法。我还会为你提供一些关于 Python 编程的通用建议以及通用概念。简而言之，当你读完我的最佳实践指南时，你将成为你能可能的最优秀的 Python 程序员。

我的书假设你对 Python 编程有一定的先验知识，所以如果你是编程领域的完全新手，请在阅读本书之前熟悉 Python 代码。我的目标是帮助你产生没有复杂性或至少极少复杂性或明显问题的 Python 代码，并使其对他人更具可读性。

再次感谢阅读本书，希望你喜欢它！

# 第 1 章：Python 编码通用概念

在我们正式进入书籍内容之前，这些是你应该注意的编码通用概念；这些概念将让你的生活变得更轻松。

## 显式代码

虽然你可以用 Python 做各种奇奇百妙的事情，但最好保持简单直接和显式。

### 一个糟糕的示例：

```python
def make_complex(*args):
    x, y = args
    return dict(**locals())
```

### 一个良好的示例：

```python
def make_complex(x, y):
    return {'x': x, 'y': y}
```

比较这些示例；在后者的代码示例中，我们显式地从调用者处接收 x 和 y，返回是一个显式的字典。

编写这段代码的开发者通过第一行和最后一行就知道要做什么；而糟糕的示例并非如此。

## 一行一个语句

虽然允许并且在很多情况下受到欢迎的复合语句（如列表推导式），但在同一行代码上有两个互不关联的语句并不是好的做法。

### 一个糟糕的示例：

```python
print 'one'; print 'two'

if x == 1: print 'one'

if <complex comparison> and <other complex comparison>:
## do something
```

### 一个良好的示例：

```python
print 'one'
print 'two'

if x == 1:
    print 'one'

cond1 = <complex comparison>
cond2 = <other complex comparison>
if cond1 and cond2:
    # do something
```

## 返回值

当你获得一个不断增长复杂的函数时，使用 return 语句并不是罕见的。然而，如果你想保持清晰的意图和良好的可读性，你应该尽量不要从多个点返回值。

在函数内部返回值时，有两种这样做的情况：正常的结果，以及任何导致函数无法正常完成的原因。在这种情况下，最佳实践是在注意到错误后立即返回。

这将有助于整洁函数结构，因为返回 之后的所有代码都假设条件已满足，从而得到主结果。

### 示例：

```python
def complex_function(c, b, a):
    if c:
        return None # 抛异常可能更好
    if b:
        return None # 抛异常可能更好
    # 尝试从 c, b 和 a 创建 x 的复杂代码
    # 如果成功则不要返回 x
    if a:
        # x 的方案 B 计算
        return x # 为 x 提供单一出口点将很有帮助
        # 在维护代码时
```

# 第 2 章：编程建议

这些是编写 Python 代码的基础建议，如果你希望你的代码更有效、高效且具有可读性，你应该遵循这些建议。

- 你的代码编写方式不能让其他 Python 实现（如 IronPython, Jython, PyPy, Psyco 和 Cython）处于不利地位。

例如，你不应该依赖 CPython 中高效的字符串拼接（形式为 a+b 或 a+=b）。这是一种相当脆弱的优化，尽管它在 CPython 中超级高效，但在任何不使用引用数的 Python 实现中都无法工作。

相反，当你在对拼接性能敏感的库部分时，你应该使用 .join() 形式。这将确保拼接在所有不同的 Python 实现中都是线性的。

- 永远不要使用等值运算符与 None 等单例进行比较。相反，使用 `is not`。




你也应该警惕使用 `if`，而你实际上应该使用 `is not None`。这种情况的一个例子是，当你测试一个默认值为 `None` 的参数或变量是否实际上被设置了不同的值时。该值在布尔上下文中可能为 `false`。

-   与其使用 `not...is` 运算符，你应该使用 `is not`。虽然两者在功能上是相同的，但前者的可读性分级较低，因此后者更受青睐。例如：

## 使用这种：
```python
if foo is not None:
```

## 不要使用这种：
```python
if not foo is None
```

-   当你在使用富比较（rich comparison）实现排序操作时，你应该实现所有的 6 个操作，而不是依赖其他代码来执行比较。这些操作是 `(__eq__, __lt__, __ne__, __ge__, __gt__, __le__)`。

为了减少工作量，有一个特定的装饰器可以生成任何缺失的比较方法。该装饰器是 `functools.total_ordering()`。

指南表明 Python 使用反射性规则。因此，Python 解释器可能会通过交换 `y > x` 与 `x < y`，或者交换 `y >= x` 与 `x <= y` 来改变内容。

你可能还会发现参数 `x == y` 被交换成了 `x != y`。`min()` 和 `sort()` 操作也肯定会使用 `<` 运算符，而 `max()` 函数将使用 `>` 运算符。然而，作为最佳实践指南，你应该使用所有的操作以避免混淆。

-   与其使用将 lambda 表达式绑定到标识符的赋值语句，不如使用 `def` 语句。

# 一个良的示例：
```python
def f(x): return 2*x
```

### 一个糟糕的示例：
```python
f = lambda x: 2*x
```

第一个示例显示，赋予函数对象的名称是 'f' 而不是通用的 `<lambda>`。这对于字符串表示以及回溯跟踪（tracebacks）最为有用，而且通过使用赋值语句，你放弃了 lambda 表达式相比普通语句提供的唯一优势——即它可以被嵌入到更大的语句中。

当你想要派生异常时，请使用 `Exception` 而不是 `BaseException`。后者的继承保留给那些捕获它们几乎总是错误的异常。

在设计异常层次结构时，应根据捕获异常时可能需要的性质来构建，而不是根据异常抛出的位置。始终回答一个问题——“出了什么问题？”而不是仅仅说某事出错了。遵循类命名的约定，但请记住为产生错误的异常类添加 “Error” 后缀。

对于那些不是错误且用作流程控制或其他信号形式的异常，没有必要在其添加任何特殊后缀。

-   当你使用异常链（exception chaining）时，请仅在需要的地方使用它。

当你刻意替换内部异常时，请确保将正确的细节重新定位到新异常中。这些示例包括在将 `KeyError` 转换为 `AttributeError` 时，或将原始异常文本嵌入新异常的消息中时，确保属性名称被保留。

-   当使用 Python 2 且抛出异常时，请始终使用 `raise ValueError('message')` 而不是 `raise ValueError('message')`（注：原文此处存在重复，意指不同格式的差异）。

这是因为第二个示例在 Python 3 中既不是有效的也不是合法的语法。此外，使用包含括号意味着，在添加字符串格式化或异常参数过长时，不需要在行尾使用续行符。

-   当你捕获异常时，尽可能在任何地方提及具体的异常，而不是使用裸露 `except:` 子句。

### 例如：
```python
try:
    import platform_specific_module
except ImportError:
    platform_specific_module = None
```
`KeyboardInterrupt` 和 `SystemExit` 异常会被裸露的 except 子句捕获，这使得使用 CTRL+C 中断程序变得困难得多，并且还可能掩盖可能其他问题。

如果你想要捕获程序中信号错误的每个异常，请使用 `except Exception:`。

通用规则是仅在以下两种情况使用裸露 `except:` 子句：

1. 如果回溯跟踪是由异常处理器打印的；这样用户就能感知到任何错误。
2. 如果需要清理工作，代码允许 `raise` 异常向上传播。实现此点的更有效方法是使用 `try...finally`。

当你将捕获的异常绑定到名称时，使用 Python 2.6 的显式绑定语法：

```python
try:
    process_data()
except Exception as exc:
    raise DataProcessingFailedError(str(exc))
```

这是 Python 3 支持的唯一语法，并消除了与旧式逗号分隔语法相关的任何歧义问题。

-   当你捕获系统错误时，使用 Python 3.3 的异常层次结构而不是 `errno` 值。同样，当使用 any/except 子句时，将 `try` 子句的使用限制在最少的代码。这将减少错误被隐藏的风险。

# 一个良的示例：
```python
try:
    value = collection[key]
except KeyError:
    return key_not_found(key)
else:
    return handle_value(value)
```

### 一个糟糕的示例：
```python
try:
    # 太宽了！
    return handle_value(collection[key])
except KeyError:
    # 将捕获由 handle_value() 抛出的 KeyError
    return key_not_found(key)
```




## 第 3 章：代码布局

显而易见的起点是如何布局你的代码。我将为你提供代码布局的最佳实践指南，并给出关于如何做以及不应该如何做的示例：

## 缩进与对齐

每个缩进层级都应该是 4 个空格。

当你使用延续行时，它们应该使用以下两种方法之一对折行的元素进行对齐：

- 垂直方向，类似于 Python 在花括号、括号和圆括号内部隐式连接行的方式，或者
- 悬缩进（hanging indents）

当你使用悬挂缩进时，请考虑第一行不应该有任何参数，并且为了标记延续行，必须使用缩进。

考虑以下示例：

### 正确的方法：

```python
### 与起始分隔符对齐
foo = long_function_name(var_four, var_three,
var_two, var_one)
```

```python
### 并包含一些缩进，以便与代码的其他部分区分
def long_function_name(
    var_four, var_three, var_two,
    var_one):
    print(var_four)
```

```python
### 使用悬缩进来增加一个级别。
foo = long_function_name(
    var_four, var_three,
    var_two, var_one)
```

### 错误的方法：

```python
### 当不使用垂直对齐时，第一行不允许有参数。
foo = long_function_name(var_four, var_three,
var_two, var_one)
```

```python
### 需要更多的缩进，因为缩进与其他部分无法区分。
def long_function_name(
    var_four, var_three, var_two,
    var_one):
    print(var_four)
```

对于延续行，4 个空格缩进的规则是可选的：

```python
### 悬缩进的缩进可以多于或少于 4 个空格。
foo = long_function_name(
    var_four, var_three,
    var_two, var_one)
```

当你使用带有可以分多行的长条件的 `if` 语句时，请注意，条件中的其余行很容易缩进 4 个空格——使用一个 2 个字符的关键字（例如 `if`）后跟一个空格和一个起始括号。然而，在视觉上，这看起来可能与 `if` 语句内部的缩进代码不兼容，因为内部已经有了 4 个空格的缩进。虽然没有特定的位置来将这些条件行与嵌套内部的代码区分开，但有几种可以接受的选项可以使用，包括但不限于：

```python
### 没有使用额外缩进。
if (this_is_one_thing and
    that_is_something_else):
    do_this()

### 添加注释，这将在支持语法高亮的编辑器中提供一些帮助。
if (this_is_one_thing and
    that_is_something_else):
    # 因为两个条件都为真，我们可以进行调整。
    do_this()

### 为条件延续行添加更多缩进。
if (this_is_one_thing
    and that_is_something_else):
    do_this()
```

现在，当你有一个多行结构时，闭合的花括号、括号或中括号可以对齐在以下位置之一——位于列表末尾行非空格的起始字符下方：

```python
my_list = [
    6, 5, 4,
    3, 2, 1,
]

result = a_function_that_will_take_arguments(
    'r', 'e', 'd',
    'c', 'b', 'a'
)
```

或者可以对齐在多行结构第一行的起始字符下方：

```python
my_list = [
    6, 5, 4,
    3, 2, 1,
]

result = a_function_that_will_take_arguments(
    'r', 'e', 'd',
    'c', 'b', 'a'
)
```

# 第 4 章：惯用法

编程惯用法（Idioms）简单来说 Python 代码应该的编写方式。我们通常将惯用代码称为 Python 代码，尽管编写某些内容往往只有一种非常明显的方法，但对于 Python 新手来说，Python 代码的实际编写方式可能有些晦涩。因此，你需要学习良好的惯用法，其中一些常见的惯用法包括：

## 解包（Unpacking）

只要你知道元组或列表的长度，包（packing）就允许你给每个元素命名。例如，`enumerate()` 会为列表中的每个项提供一个包含 2 个元素的元组：

```python
for index, each item in enumerate(this_list):
    # 对 index 和 each item 执行某些处理
```

你也可以使用解包来交换变量：

```python
b, a = a, b
```

你还可以使用嵌套解包：

```python
c, (b, a) = 3, (2, 1)
```

当 Python 3 实现时，它带来了一种新的扩展解包方法：

```python
c*_rest = [3, 2, 1]
### c = 3, the_rest = [2, 1]
c*_the_middle, c = [4, 3]
```

## 创建变量

如果你知道元组或列表的长度，包允许你给每个元素命名。例如，`enumerate()` 会为列表中的每个项提供一个包含 2 个元素的元组：

```python
for index, each item in enumerate(this_list):
    # 对 index 和 each item 执行某些处理
```

你也可以使用解包来交换变量：

```python
b, a = a, b
```

你还可以使用嵌套解包：

```python
c, (b, a) = 3, (2, 1)
```

当 Python 3 实现时，它带来了一种新的扩展解包方法：

```python
c*_rest = [3, 2, 1]
### c = 3, the_rest = [2, 1]
c*_the_middle, c = [4, 3]
```

（注：此处原文中存在大量重复内容，已根据文档工程师原则进行去重处理）





## 块注释：

块注释通常适用于其后的某些部分或全部代码。注释的缩进方式必须与它所指的代码完全一致，且块注释的每一行必须以一个 `#` 后面跟一个空格开头。唯一的例外是你在注释中使用了缩进的文本。每个块注释中的所有段落之间必须用一个包含单个 `#` 的行来隔开。

### 行内注释

这些注释应该越少越好。回顾一下，行内注释是指放置在与语句同一行上的注释。行内注释与语句之间至少要有两个空格隔开，并且它们必须以一个 `#` 后面跟一个空格开头。

从坦率地说，你应该避免使用行内注释，因为它们并不是真正必要的，并且可能会引起不必要的注意力分散。

例如，你永远不要这样做：

```
x = x + 1    # 将 x 加 1
```

但是，有时，这可能是很有用的：

```
x = x + 1    # 补偿边界值
```

# 第 6 章：约定

为了让你的 Python 代码更具可读性，请遵循这些约定：

查看你的变量是否等于一个常量。没有必要将值与 0、None 或 True 进行显式比较；相反，你可以将其直接放入 `if` 语句中。看下面的示例：

### 一个糟糕的示例：

```python
if attr == None:
    print 'True'
```

```python
if attr == None:
    print 'attr is None!'
```

### 一个良好的示例：

```python
### 直接看值
if attr:
    print 'attr is the best!'
```

```python
### 或者检查相反的情况
if not attr:
    print 'attr is the worst!'
```

```python
### 或者，由于 None 被视为假，确保你对它运行了显式检查
if attr == None:
    print 'attr is None!'
```

## 如何访问字典元素：

不要使用 `dict.has_key()` 方法，请使用语法 `x in d` 或使用 `dict.get()` 来传递默认参数。

### 一个糟糕的示例：

```python
d = {'hello': 'world'}
if d.has_key('hello'):
    print d['hello'] # 打印 'world'
else:
    print the_default_value'
```

### 一个良好的示例：

```python
d = {'hello': 'world'}

print d.get('hello', 'default_value') # 打印 'world'
print d.get('thingy', 'default_value') # 打印 'default_value'
```

### 或者：

```python
if 'hello' in d:
    print d['hello']
```

## 用短方法操作列表

在操作列表时，你不需要长篇大论；当你想要对列表执行操作操作时，使用列表推导式或 `filter()` 或 `map()` 函数来使用简洁的语法。

### 一个糟糕的示例：

```python
### 过滤所有大于 4 的元素
a = [5, 4, 3]
b = []
for i in a:
    if i > 4:
        b.append(i)
```

### 一个良好的示例：

```python
a = [5, 4, 3]
b = [i for i in a if i > 4]
### 或者：
b = filter(lambda x: x > 4, a)
```

### 另一个糟糕的示例：

```python
### 给列表中的所有成员加 3。
a = [5, 4, 3]
for i in range(len(a)):
    a[i] += 3
```

### 另一个良好的示例：

```python
a = [5, 4, 3]
a = [i + 3 for i in a]
### 或者：
a = map(lambda i: i + 3, a)
```

你也可以使用 `enumerate()` 函数来记录你在列表中的位置：

```python
a = [5, 4, 3]
for i, item in enumerate(a):
    print i, item
    # 打印
    # 0
    # 1
    # 2
```

这个函数比手动处理计数器更易读，而且对于迭代器来说高效得多。

## 从文件读取

当你想要从文件中读取内容时，最好使用 `with open` 语法，因为它会自动为你关闭文件。

### 一个糟糕的示例：

```python
f = open('file.txt')
a = f.read()
print a
f.close()
```

### 一个良好的示例：

```python
with open('file.txt') as f:
    for line in f:
        print line
```

使用 `with` 语句要高效得多，因为它可以确保在块包含异常时文件始终被关闭。

## 换行

逻辑行是有接受限制的，当你有一个较长的行时，应该将其分成几行。你的 Python 解释器会处理连续的行，只要每行的最后一个字符是反斜杠 (\)，它就会连接这些行。然而，尽管这很有用，但真的要避免这样做，因为它是脆弱的。如果在反斜杠后添加空格，可能会破坏你的代码，结果可能不符合预期。此事的更好的方法是将元素封装在括号内。如果行尾有一个未闭合的括号，下一行将被连接，依此类推，直到遇到闭合的括号。

### 一个糟糕的示例：

```python
my_string = "这是一个非常长的字符串" \
它跨越了行"
```

### 一个良好的示例：

```python
my_string = ("这是一个非常长的字符串"
"它跨越了行")
```




然而，你应该应该非常谨慎地使用包含参数的列表，因为它具有一些缺点。如果一个函数的参数具有相同或相似的性质，更好的定义是使用带有单个参数的函数；该单个参数将是一个序列或列表。例如，如果你发送多个接收者，使用显式定义会更好：`send('Hello', 'God', 'Dad', 'Galactus')`，然后使用 `send('Hello', 'God', 'Dad', 'Galactus')` 来调用它。这样一来，函数用户可以提前更改接收者列表，并为任何可以解包并传递的序列提供了可能，包括迭代器。

- 4. 任意关键字参数字典 - 这是向函数传递参数的最后一种方法。如果函数需要未知数量的命名参数数组，你可以使用 `**kwargs` 。在函数体内，`**kwargs` 是一个字典，包含了所有已传递且未被函数签名中其他关键字参数捕获的命名参数。

然而，你应该像对待任意参数列表一样以同样的谨慎程度对待它们，因为原因基本相同。这些是强大的技术，只有在你证明有必要使用它们时才应该使用。如果有更清晰、更简单的结构可以完成工作，则绝对不应该使用它们。

决定哪些函数参数是可选关键字、哪些是位置参数，以及确定是否应该使用更高级的技术来传递参数，这真的取决于你，这个程序员。

保持简单并遵循以下编写 Python 函数的规则：

- 可读性 – 变量名和参数不需要任何解释
- 易于更改 – 你可以添加关键字参数而不会导致其他代码崩溃。

# 第 8 章：命名规范

老实说，Python 库的命名规范有些混乱，因此我们永远无法做到完全一致。然而，有一些推荐的命名标准适用于所有新的包和模块，这些模块（包括任何第三方框架）都必须符合这些标准。尽管如此，如果你正在使用具有不同风格现有库，请坚持该风格，因为一致性是优的，特别是在可读性方面。

要学习的第一条也是最重要的原则是：当你使用作为公共 API可见部分的名称时，你必须使用反映名称用途的约定，而不是其实现方式。

## 描述性

有很多不同的命名风格，因此识别在使用哪种风格（独立于使用方式）很有帮助。这些是最常见的区分命名风格：

- B – 单个大写字母
- b – 单个小写字母
- 小写字母加下划线
- 小写字母
- 大写字母加下划线
- 全大写字母
- CapitalizedWords – 通常称为 CamelCase（驼峰命名法），因为字母看起来有些*起不平的*
- mixedCase – 与 CamelCase 不同，因为首字母是小写的
- Capital_Words_With_Underscore – 不是一种美观的风格！

* 当你在 CamelCase 中使用缩写词时，你应该确保所有的缩写字母都是大写的。例如，与其使用 `HttpServlet`，不如使用 `HTTPServer`。

你还可以使用另一种风格，即添加一个唯一的前缀（短短的），将一组相关的名称放在一起。这在 Python 中并没有很大用，但我提到是为了让你知道它。一个例子是 `os.stat()` 函数 – 它将返回一个包含名称如 `st_size`、`st_mode`、`st_mtime` 等项的元组。

这些是一些使用尾部或头部下划线的形式，通常可以与任何大小写约定结合：

- `_one_leading_underscore` – 这通常是“内部使用”的指示，但并不强。
- `_one_trailing_underscore` – 通常用于防止与 Python 关键字发生冲突，例如：`Apiter.Toplevel(master,class='ClassName')`
- `__two_leading_underscores` – 当你创建一个类属性时，这会触发名称变形（mangling），例如：（在类 `FootBar` 内部，`_boo` 会变成 `_FootBar__boo`
- `__two_leading_and_two_trailing_underscores` 是位于用户控制的命名空间中的属性或“魔法”对象。例如：`__init__`、`__file__` 或 `__import__`。

## 规范性

这些是你应该避免的名称：

在编写单字符变量名时，永远不要使用‘O’（大写字母）、‘l’（小写 L）或‘I’（大写 i）。取决于你正在使用的字体，这些可能与数字‘0’和‘1’产生混淆——如果你发现自己正在考虑使用‘l’，请改用大写的‘L’。

## 模块和包的命名

所有模块名称应该是短且小写的。你可以在模块名称中使用下划线，但只有在它使其更易读时才行。Python 包也是如此短且小写的名称但不要使用下划线。

当你有一个用 C 或 C++ 编写的扩展模块，并带有一个具有面向对象接口的 Python 模块时，C 或 C++ 模块将具有头部下划线，例如 `_socket`。

## 类名

类名通常使用 CapWords 或 CamelCase 约定。

内置名称有它们独立的约定，通常是单单词或两个单词合并为一个词，例如 'Hello' 或 'HelloWorld'。CamelCase 约定倾向于用于内置常量和异常名称。

## 类型变量

变量名通常使用 CamelCase，尽管如此，你应该添加后缀 `_co` 或 `_contra` 来声明行为。例如：

```python
VT_co = TypeVar('VT_co')
KT_contra = TypeVar('KT_contra')
```

## 异常命名

异常是类，因此请确保在名称上使用 'Error' 后缀。

## 全局变量

只要变量在模块内部使用，命名规范与函数相同。

## 函数

所有函数名均为小写，并在需要的地方用下划线分隔。

## 实例变量和方法名

再次，这里的命名规范适用于函数——使用小写字母。如果你在使用实例变量或非公开方法，应该使用单个下划线。

## 常量

这些通常定义在模块层级，并且全大写并用下划线分隔，例如 `MAX_OVERFLOW`。

## 继承设计

另一个属性类别是那些专门设计用于继承的类，作为扩展或修改某些方面的方式。始终对属性做出显式决定——它们是公共的、仅供基类使用的，还是属于子类的 API？





# 第 9 章：
在语句和表达式中使用空格

首先，是一些关于空格的禁忌：

在以下情况下请勿使用额外的空格：

- 紧邻大括号、方括号或圆括号内部

### 良好的示例：
`ham(spam[1], (eggs: 2))`

### 糟糕的示例：
`ham(spam[ 1 ], ( eggs: 2 ))`

- 位于冒号、分号或逗号之前：

### 良好的示例：
`if x == 4; print x, y; x = y, x`

### 糟糕的示例：
`if x == 4 : print x , y ; x = y, x`

然而，在你使用切片（slice）时，冒号类似于二元运算符，两边应该包含等量的空格。当你使用扩展切片时，两个冒号必须包含完全相同的间距。例外情况是省略了切片参数以及相应的空格。

### 良好的示例：
`spam[1:8], spam[3:2]; spam[8:2], spam[1:8]`
`spam[lower:upper]; spam[lower:upper]; spam[lower:step]`
`spam[lower+offset:upper+offset]`
`spam[:upper_fn(x) : step_fn(x)]`
`spam[lower + offset : upper + offset]`

### 糟糕的示例：
`spam[lower+offset:upper + offset]`
`spam[ 1:8], ham[1:8], ham[1:8:2]`
`spam[ : upper]`
`spam[: upper]`

- 紧邻开始函数调用参数列表的左圆括号之前

### 良好的示例：
`ham(1 )`

### 糟糕的示例：
`ham (1)`

- 紧邻开始切片或索引的左括号之前

### 良好的示例：
`dct['key'] = lst[index]`

### 糟糕的示例：
`dct['key'] = lst [index]`

- 当运算符（如赋值运算符）周围有多个空格时，将其与另一个运算符对齐

### 良好的示例：
```python
x = 1
y = 2
long_variable = 3
```

### 糟糕的示例：
```python
x = 1
y = 2
long_variable = 3
```

# 其他建议

避免在整个代码中出现行尾空格（trailing whitespace），因为它是不可见的，并且可能会导致混惑。例如，如果你输入一个反斜杠，后面跟一个空格然后换行——这不会被算作行延续。事实上，某些文本编辑器不会保留它，而且有些项目包含了预提交钩子（pre-commit hooks），它们会直接拒绝此类代码——其中之一就是 CPython。

以下二元运算符应该被单个空格包围——每侧各一个：

- 赋值 (=)
- 复合赋值 (+=, = 等)

以下比较运算符的对待方式相同：

- =
- <
- >
- !=
- <>
- <=
- in
- not in
- is
- is not

以及这些布尔值：

- and
- or
- not

如果你使用了优先级不同的运算符，请考虑在优先级最低的运算符周围添加空格——在此处请根据你的最佳判断来操作。然而，你使用的空格不应超过一个，并确保运算符的每一侧都有等量的空格——不要在一侧放 1 个在另一侧放 2 个：

### 良好的示例：
```python
i = i + 1
submitted += 1
x = x*2 - 1
hypot = x*x + y*y
c = (a+b) * (a-b)
```

### 糟糕的示例：
```python
i=i+1
ubmitted+=1
x = x*2 - 1
hypot2 = x*x + y*y
```

