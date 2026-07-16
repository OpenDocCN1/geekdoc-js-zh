# Python 编程最佳实践












## 引言

我想感谢你并祝贺你阅读《Python：Python 编程最佳实践》一书。本书包含了如何更有效地编写 Python 代码的成熟步骤和策略。当你初学 Python 时，人们会教你如何编写代码，但在很多情况下，他们不会教你如何写出整洁的代码。

如果你接触任何 Python 程序员，问问他们喜欢 Python 的地方是什么。我保证他们会告诉你，主要原因之一是它易于阅读。事实上，这是 Python 语言的核心所在，因为计算机代码被阅读的次数远多于编写的次数。这很大程度上是因为 Python 代码遵循了一系列指南和“Pythonic”（Python 风格）惯用用法——如果你听到程序员说某部分代码不“Pythonic”，就意味着它没有遵循这些指南，并且没有以任何可读的方式表达其意图。

代码风格和布局至关重要，你所使用的风格的一致性也是如此。尽管如此，有时一致性并不是正确的选择，而指南也简单并不适用——你必须知道何时是这种情况，而这就是进行 Python 编程时最佳判断所在。

通过本指南，我将向你展示编写代码的绝对最佳方式，整理你的程序并使其更加有效、高效率。我不会只给你基础知识。我将深入探讨你需要了解的一切，从代码布局到如何编写函数、惯用用法和命名。

我将谈到空白符和制表符、字符串和方法。我还将针对 Python 编程提供一些通用建议以及通用概念。简而言之，当你读完我的最佳实践指南时，你将成为最优秀的 Python 程序员。

# 第 1 章：Python 编码通用概念

在我们正式进入书籍内容之前，这些是你应该注意的通用概念。

## 显式代码
虽然你可以用 Python 做一些奇怪的事情，但最好保持显式。

**糟糕的示例：**
```python
def make_complex(*args):
    x, y = args
    return locals()
```

**良好的示例：**
```python
def make_complex(x, y):
    return {'x': x, 'y': y}
```
对比这些示例；在后一个示例中，我们显式地返回字典。

### 一行一条
虽然允许复合语句（如列表推导式），并且在很多情况下受到推崇，但在同一行内有两个不连续的语句并不是好的做法。

**糟糕的示例：**
```python
print 'one'; print 'two'
if x == 1: print 'one'
```

**良好的示例：**
```python
print 'one'
print 'two'
if x == 1:
    print 'one'
```
```python
if cond1 and cond2:
    # 执行某些操作
```

### 返回值
当你得到一个复杂度不断增长的函数时，在体中使用多个 `return` 语句并非罕见。然而，如果你想保持清晰的意图良好的可读性，你应该尽量避免从函数的多个点返回值。

在函数内部返回值，有两种情况：来自正常处理的函数返回的结果，以及指示输入参数错误或由于任何原因函数无法完成计算的错误。

如果你不想在后一种情况下抛出异常，那么可能需要返回诸如 `False` 或 `None` 等值，作为函数未能正常执行的指示。在这样的情况下，最佳实践是在注意到错误上下文后立即返回。

这将有助于整洁函数结构，因为错误返回之后的所有代码都假设条件已经满足，以便计算主函数的结果。因此，有时需要像这样的多个 `return` 语句。尽管如此，如果一个函数包含多个不同的路径，调试结果将变得非常困难，因此最好只维护一条路径。这有助于理清代码路径，而且如果你有多个路径，这可能表明你需要重新审视你的代码并整理它。

**示例：**
```python
def complex_function(c, b, a):
    if not c:
        return None  # 抛出异常可能更好
    if not b:
        return None  # 抛出异常可能更好
    # 尝试从 c, b 和 a 生成 x 的复杂代码
```




### 如果成功则不要返回 x

```python
if not x:
    # 对 x 的备选计算
    return x  # 在尝试维护代码时，为 x 提供一个出口点会有帮助。
```

# 第 2 章：编程建议

这些是编写 Python 代码的基本建议。如果你希望你的代码更加有效、高效且具有可读性，就应该遵循这些建议。

- 你的代码编写方式不能对其他 Python 实现造成不利，例如 `IronPython`、`Jython`、`PyPy`、`Psyco` 和 `Cython`。

例如，你永远不要依赖 `CPython` 中高效的字符串拼接（其形式为 `a=a+b` 或 `a+=b`）。这是一种相当脆弱的优化，尽管在 `CPython` 中极其高效，但因为它无法在所有类型上运行，而这些类型在任何不使用引用计数的 Python 实现中都不存在。

相反，当你使用库中性能敏感的某部分时，你应该使用 `.join()` 形式。这将确保拼接在所有不同的 Python 实现中都是线性的。

- 永远不要使用相等运算符与单例（如 `None`）进行比较。相反，请使用 `is` 或 `not`。

你还应该警惕在应该使用 `if is not None` 的地方使用 `if x`。一个例子是，当你测试一个默认值为 `None` 的参数或变量是否真的被设置为了不同的值时。另一个值的类型可能在布尔上下文中是假的。

- 与其使用 `not...is` 运算符，你应该使用 `is not`。虽然它们在功能上是等等的，但前者在可读性量级上较低，因此后者更受青睐。例如：

使用这种：
```python
if foo is not None:
```

不要使用这种：
```python
if not foo is None
```

- 当你使用富比较（rich comparison）实现排序操作时，你应该实现所有的 6 个操作，而不是依赖其他代码来触发比较。这些操作是（`__eq__`、`__lt__`、`__ne__`、`__ge__`、`__gt__`、`__le__`）。

为了减少工作量，一个特定的装饰器有助于生成任何缺失的比较方法。该装饰器是 `functools.total_ordering()`。

风格指南指出 Python 假设了反射性规则。因此，Python 解释器可能会通过交换 `y > x` 和 `x < y`，或者交换 `y >= x` 和 `x <= y` 来改变内容。

你可能还会发现参数 `x == y` 被交换成了 `x != y`。`min()` 和 `sort()` 操作也将确无疑地使用 `<` 运算符，而 `max()` 函数将使用 `>` 运算符。然而，作为最佳实践指南，你应该使用所有的操作以防产生混淆。

- 与其使用将 lambda 表达式绑定到标识符的赋值语句，不如使用 `def` 语句。

良好的示例：
```python
def f(x): return 2*x
```

一个糟糕的示例：
```python
f = lambda x: 2*x
```

第一个示例显示给函数对象的名称是 `f` 而不是总体的 `<lambda>`。这对于字符串表示以及回溯追踪（tracebacks）最有有用，而且通过使用赋值语句，你放弃了 lambda 表达式相比 `def` 语句提供的唯一优势——即它可以被嵌入更大的语句中。

当你想要派生异常时，使用 `Exception` 而不是 `BaseException`。后者的继承留给那些捕获它们几乎总是错误的错误的异常。

在设计异常层次结构时，应根据捕获异常可能需要的性质来构建，而不是根据异常抛出的位置。始终回答一个问题——“发生了什么错误？”而不是仅仅说某事错了。使用类命名的规范，但记得为产生错误的异常类加上 “Error” 后缀。

对于不是错误且用于流程控制或其他信号形式的异常，不需要添加任何特殊后缀。

- 当你使用异常链（exception chaining）时，仅在需要的地方使用。

当你故意替换内部异常时，确保将正确的细节迁移到新的异常中。示例包括在将 `KeyError` 转换为 `AttributeError` 时确保属性名称被保留，或者将原始异常文本嵌入到新异常的消息中。

- 当使用 Python 2 抛出异常时，始终使用 `raise ValueError('message')` 而不是 `raise ValueError 'message'`。

这是因为第二个示例在 Python 3 中既不是有效的也不是合法的语法。此外，使用包含括号意味着当添加字符串格式化或异常参数过长时，不需要在行尾使用续行符。

- 当你捕获异常时，尽可能提到具体的异常，而不是使用裸露的 `except:` 子句。

例如：
```python
try:
    import platform_specific_module
except ImportError:
    platform_specific_module = None
```

`KeyboardInterrupt` 和 `SystemExit` 异常会被裸露 `except:` 子句捕获，这使得使用 CTRL+C 中断程序变得困难得多，而且它们还会掩盖可能存在的其他问题。

如果你想要捕捉程序中信号错误的每个异常，请使用 `except Exception:`。

通常规则是仅在以下两种情况之一使用裸露 `except:` 子句：
1. 如果回溯追踪是由异常处理程序打印的；这样用户就能感知到错误。
2. 需要清理工作但允许异常向上通过 `raise`。

当你将捕获的异常绑定到名称时，使用 Python 2.6 的语法：
```python
try:
    process_data()
except Exception as exc:
    raise DataFailedError(str(exc))
```

这是 Python 支持的唯一语法，它消除了与旧风格相关的逗号问题。

- 当你捕获系统错误时，使用 Python 3 的异常层次而不是 `errno` 值。同样，当你使用任何 `try/except` 子句时，尽量将 `try` 子句限制在尽可能少的代码范围内。这将减少隐藏错误的风险。

良好的示例：
```python
try:
    value = collection[key]
except KeyError:
    return key_not_found(key)
else:
    return handle_value(value)
```

一个糟糕的示例：
```python
try:
    # 范围太广了！
    return handle_value(collection[key])
except KeyError:
    # 会捕获 handle_value() 的 KeyError
    return key_not_found(key)
```

- 当你使用特定代码段局部资源工具时，使用语句在使用后立即清理。你也可以使用 `try/finally` 语句。

- 当目的是获取和释放资源时，始终通过单独的方法调用上下文管理器。

良好的示例：
```python
with conn.start_transaction():
    do_something_in_transaction(conn)
```

一个糟糕的示例：
```python
with conn:
    do_something_in_transaction(conn)
```

第二个示例没有提供任何信息表明 `__enter__` 和 `__exit__` 方法除了关闭事务之外的操作。在这种情况下，显式化是重要的。

- 返回语句的一致性很重要。函数的所有返回语句或一个返回语句都应该返回表达式或值。如果某个返回语句返回了表达式，那么任何不返回值的语句都应该显式说明返回 `None`，并且在该函数的末尾有一个返回语句。

良好的示例：
```python
def foo(x):
    if x >= 0:
        return math.sqrt(x)
    else:
        return None

def bar(x):
    if x < 0:
        return None
    return math.sqrt(x)
```

一个糟糕的示例：
```python
def foo(x):
    if x >= 0:
        return math.sqrt(x)
```




```python
def bar(x):
    if x < 0:
        return
    return math.sqrt(x)
```

- 不要使用字符串模块（string modules）；请使用字符串方法（string methods）。
这些方法总是更快，并且与 Unicode 字符串共享 API。如果你需要与早于 2.0 的 Python 实现向后兼容，则可以忽略这条规则。

- 不要使用字符串切片来检查后缀和前缀，而应使用 `.startswith()` 和 `.endswith()`。
这些方法要清晰得多，而且更不容易出错。

### 良好的示例：
```python
if foo.beginswith('bar'):
```

### 错误的示例：
```python
if foo[:3] == 'bar':
```

- 在比较对象类型时，使用 `isinstance()` 而不是直接比较。

### 良好的示例：
```python
if isinstance(obj, int):
```

### 错误的示例：
```python
if type(obj) is type(1):
```

当你检查一个对象是否实际上是字符串时，记住它也可能是一个 Unicode 字符串。在 Python 2.0 中，Unicode 和 `str` 共享名为 `basestring` 的基类，因此你可以：

```python
if isinstance(obj, basestring):
```

然而，在 Python 3 中，你找不到 `basestring` 或 `Unicode`，只有 `str` 和 `bytes` 对象不再是字符串，它们是整数序列。

对于序列——元组、列表、字符串等——请利用空序列为假（false）的特性。

### 良好的示例：
```python
if not seq:
    if seq:
```

### 错误的示例：
```python
if len(seq):
    if not len(seq):
```

不要包含任何需要大量尾部空格的字符串字面量，因为这些是无法区分的，某些文本编辑器会删除它们。

不要使用 `==` 来比较布尔值 True 或 False：

### 良好的示例：
```python
if greeting:
```

### 错误的示例：
```python
if the greeting == True:
```

### 更糟糕的示例：
```python
if the greeting is True:
```

# 第 3 章：代码布局

最明显的入门点是如何布局你的代码。我将为你提供代码布局的最佳实践指南，以及关于如何做和如何不做的示例：

## 缩进与对齐

每个缩进层级应该是 4 个空格。

当你使用延续行时，它们应该使用以下两种方法之一对齐折行后的元素：

- 使用 Python 在花括号、括号和圆括号内部隐式连接行的垂直对齐，或
- 使用悬挂缩进（hanging indents）

当你使用悬挂缩进时，考虑第一行不应该有任何参数，并且为了标记延续行，必须使用缩进。

考虑以下示例：

### 正确的方法：

```python
### 与起始分隔符对齐。
foo = long_function_name(var_four, var_three,
                         var_two, var_one)
# 包含了更多缩进，以便与代码其余部分区分来
def long_function_name(
    var_four, var_three, var_two,
    var_one):
    print(var_four)

### 应该使用悬挂缩进来增加层次。
foo = long_function_name(
    var_four, var_three,
    var_two, var_one)
```

### 错误的方法：

```python
### 当你不使用垂直对齐时，第一行不允许有参数。
foo = long_function_name(var_four, var_three,
    var_two, var_one)
### 需要更多的缩进，因为缩进无法与其余部分区分。
def long_function_name(
    var_four, var_three, var_two,
    var_one):
    print(var_four)
```

当涉及到延续行时，4 个空格缩进规则是可选的：

```python
### 悬挂缩进*可以*缩进多于或少于 4 个空格。
foo = long_function_name(
    var_four, var_three,
    var_two, var_one)
```

当你使用带有可以跨多行的长条件的 `if` 语句时，请注意，条件语句中的其余行可以轻松创建一个 4 个空格的自然缩进——使用一个 2 个字符的关键字（例如 `if`）配合一个空格和一个左圆括号。然而，在视觉上，这看起来可能与 `if` 语句内部缩进的代码某种不兼容，因为内部已经有了 4 个空格的缩进。关于是否要将这些条件行与嵌套内部的代码区分开，并没有一个真正的标准，但有几个你可以使用的接受选项，包括但不限于：

```python
### 没有使用额外的缩进。
if (this_is_one_thing and
    that_is_something_else):
    do_this()

### 添加注释，这将在支持语法高亮的编辑器中提供一些帮助。
if (this_is_one_thing and
    that_is_something_else):
    # 因为两个条件都为真，我们可以进行调整。
    do_this()

### 给条件延续行增加更多缩进。
if (this_is_one_thing
        and that_is_something_else):
    do_this()
```

现在，当你有一个多行结构时，闭合的花括号、括号或中括号可以对齐在两个位置之一——要么在列表末尾行非空格的起始字符之下方：

```python
my_list = [
    6, 5, 4,
    3, 2, 1,
    ]
result = a_function_that_will_take_arguments(
    'f', 'e', 'd',
    'c', 'b', 'a',
    )
```

或者它可以对齐在多行结构第一行的起始字符之下方：

```python
my_list = [
    6, 5, 4,
    3, 2, 1,
]
result = a_function_that_will_take_arguments(
    'f', 'e', 'd',
    'c', 'b', 'a',
)
```

# 第 4 章：惯用法（Idioms）

简单来说，编程惯用法是 Python 代码应该编写的方式。我们通常将惯用代码称为 Pythonic 代码（Pythonic），尽管编写某事通常有一种非常明显的方法，但 Pythonic 代码的实际编写方式对于 Python 的初学者来说可能稍微有些晦涩。因此，你需要学习良好的惯用法，其中一些常见的惯用法包括：

## 解包（Unpacking）

只要你知道元组或列表的长度，解包允许你为每个元素命名。例如，`enumerate()` 为列表中的每个项目都提供一个包含 2 个元素的元组：

```python
for the index, each item in enumerate(this_list):
    # 对 index 和 each item 执行操作
```

你也可以使用解包来交换变量：

```python
b, a = a, b
```

你还可以使用嵌套解包：

```python
c, (b, a) = 3, (2, 1)
```

当 Python 3 实现时，它带有一个新的扩展解包方法：

```python
c *the_rest = [3, 2, 1]
### c = 3, the_rest = [2, 1]
c, *the_middle, c = [4, 3, 2, 1]
### c = 4, the_middle = [3, 2, 1]
```

### 创建忽略变量

如果你想赋值某些内容但不需要该变量，你会使用 `__`。例如：

```python
filename = 'footbar.txt'
basename, __, ext = filename.rpartition('.')
```

**注意**

你经常看到建议使用单划线 `_` 来丢弃变量，而不是使用双划线 `__`。这样做的问题是，单划线 `-` 经常在 `gettext()` 函数中作为别名。它还用于存储交互式提示符的上一次操作值。当你使用双划线 `__` 时，它既清晰又方便，还能消除干扰单划线其他用例的风险。

### 创建长度 N 的列表

要创建一个相同内容的长度 N 列表，你会使用 `*` 列表运算符：

```python
four_zeros = [Zero] * 4
```

要创建一个列表不应该使用 `*` 运算符。该运算符创建引用同一个列表列表，这并不是我们想要的。相反，我们使用列表推导式：

```python
four_lists = [[] for __ in xrange(4)]
```

注意——如果你正在使用 Python 3，请使用 `range()` 而不是 `xrange()`。

### 从列表创建字符串

创建字符串最常用的惯用法是在空字符串上使用 `.join()`：

```python
letters = ['c', 'l', o, 't']
word = ''.join(letters)
```

这会将“clot”的值赋值给变量 `word`。你可以将这种惯用法应用于元组和列表。

### 在集合中查找项

有时，你需要在集合中查找特定选项，有两种方法——使用列表或集合。

看这个示例：

```python
s = set(['c', 'l', 'o', 't'])
l = ['c', 'l', 'o', 't']

def lookup_set(s):
    return 's' in s

def lookup_list(l):
    return 's' in l
```





现在，这两个函数看起来完全一样，仅仅是因为 `lookup_set` 利用了 Python 集合是哈希表的这一事实。然而，每个示例中 `lookup` 的性能是不同的。为了判断一个特定项目是否在列表中，Python 必须搜索每一个项目，直到找到匹配的项。这非常耗时，特别是当列表很长时。使用集合，每个项目都有一个哈希告诉 Python 在哪里查找，这使得搜索快得多。你也可以以相同的方式搜索字典。由于性能存在差异，在以下情况下，使用集合比列表是更好的主：

*   集合包含大量项目
*   你需要经常在集合中查找项目

在集合较小或不需要频繁查找的情况下，哈希表所需的额外内存和时间通过使用列表是可以节省的。

# 第 5 章：注释

由于你已经有一些 Python 编程经验，你会知道注释在运行时是不可见的。注释是为了帮助其他开发者或未来的自己理解代码做了什么以及为什么这么做。有些人认为注释毫无意义，但在编写代码时，写注释比不写注释要好得多。当你修改代码时，必须确保更新注释。正确的做法是在写注释时，确保它是一个完整的句子。

当你使用内联注释时，尽可能少用。作为复习，内联注释是放在语句同一行的注释，它们通常不是必要的，并且会引起分心。例如，你不应该这样做：

```python
x = x + 1 # 增加 x
```

然而，有时这可能是有用的：

```python
x = x + 1 # 补偿
```

更好的方法是将将会元素包含在括号内。如果行尾有一个未闭合的括号，下一行就会被连接，直到出现闭合括号。你也可以使用方括号或大括号来实现相同的功能，只要你保持一致性——你用什么开始，就必须用什么结束。

### 错误示例
```python
### 过滤所有大于 4 的元素
a = [5, 4, 3]
b = []
for i in a:
    if i > 4:
        b.append(i)
```

### 正确示例
```python
a = [5, 4, 3]
b = [i for i in a if i > 4]

### 或者：
b = filter(lambda x: x > 4, a)
```

### 另一个错误示例
```python
### 给列表的所有成员加 3。
a = [5, 4, 3]
for i in range(len(a)):
    a[i] += 3
```

### 另一个正确示例
```python
a = [5, 4, 3]
a = [i + 3 for i in a]

### 或者：
a = map(lambda i: i + 3, a)
```

你还可以使用 `enumerate()` 函数来记录你在列表中的位置：

```python
a = [5, 4, 3]
for i, item in enumerate(a):
    print i, item
### 输出：
### 0 5
### 1 4
### 2 3
```
这个函数比手动处理计数器读性更好，而且对于迭代器来说优化得多。

### 从文件读取

当你想要从文件中读取内容时，最好使用 `with open` 语法，因为这会自动为你关闭文件。

### 错误示例
```python
f = open('file.txt')
a = f.read()
print a
f.close()
```

### 正确示例
```python
with open('file.txt') as f:
    for line in f:
        print line
```
使用 `with` 语句要高效得多，因为它确保即使在 `with` 块包含异常时文件总是关闭。

### 换行

逻辑代码行有接受的限制，当你有一行代码过长时，应该将其拆分成几行。你的 Python 解释器会获取连续的行，只要每行的最后一个字符是反斜杠 `\`，它就会连接这些行。然而，尽管这有时有用，但你真的应该避免，因为它是脆弱的。如果你在反斜杠后添加了空格，可能会破坏你的代码，结果可能不是你预期的。

此更好的方法是将元素包含在括号内。如果行尾有一个未闭合的括号，下一行就会被连接，依此类推，直到出现闭合括号。你也可以使用方括号或大括号来实现相同的功能，只要你保持一致。

### 错误示例
```python
if attr == True:
    print 'True!'

if attr == None:
    print 'None!'
```

### 正确示例
```python
if attr:
    print 'True!'

if not attr:
    print 'None!'
```

### 如何访问字典元素

与其使用 `dict.has_key()` 方法，不如使用 `x in d` 语法或使用 `dict.get()` 来传递参数。

### 错误示例
```python
d = {'hello': 'world'}

if d.has_key('hello'):
    print d['hello']
else:
    print 'default_value'
```

### 正确示例
```python
d = {'hello': 'world'}
print d.get('hello', 'default_value') # 输出 'world'
print d.get('thingy', 'default_value') # 输出 'default_value'

### 或者：
if 'hello' in d:
    print d['hello']
```

### 快捷方式操作列表

在操作列表时，不需要长篇大论；当你想要对列表执行操作时，使用列表推导式或 `filter()` 或 `map()` 函数来使用简洁语法。

### 错误示例
```python
### 过滤所有大于 4 的元素
a = [5, 4, 3]
b = []
for i in a:
    if i > 4:
        b.append(i)
```

### 正确示例
```python
a = [5, 4, 3]
b = [i for i in a if i > 4]

### 或者：
b = filter(lambda x: x > 4, a)
```

### 另一个错误示例
```python
### 给列表的所有成员加 3。
a = [5, 4, 3]
for i in range(len(a)):
    a[i] += 3
```

### 另一个正确示例
```python
a = [5, 4, 3]
a = [i + 3 for i in a]

### 或者：
a = map(lambda i: i + 3, a)
```




尽管如此，如果你发现自己必须不断拆分长行，这说明你正试图做太多的事情，这将会影响代码的可读性。

# 第 7 章：方法和函数参数

对于任何实例方法中的第一个参数，始终使用 `self`；对于任何类方法中的第一个参数，始终使用 `cls`。

如果函数参数的名称与某个保留关键字相同，那么在名称末尾添加一个下划线会比使用错误的拼写或缩写要好。因此，你应该使用 `class_` 而不是 `clss`。也许比引起冲突更好的方法是——使用同义词。

## 函数参数

你可以通过 4 种向函数传递参数的方法：

1. **位置参数 (Positional Argument)** – 这些是强制性的，且不包含任何默认值。位置参数是最简单的参数形式，用于作为函数含义完整组成部分的参数；它们具有自然的顺序，因此，在下面的示例中，`user` 函数应该很容易记住该函数需要 2 个参数，并且应该记住它们的顺序：

   `Send(message, recipient)` 和 `point(x, y)`

   在这两种情况下，你可以在调用函数时使用参数名称，通过这样做，你可以更改参数的顺序。例如，你可以调用 `send(recipient='world', message='Hello')` 和 `point(y=2, x=1)`。然而，正如你所看到的，这并不非常可读，而且里面的单词比我们需要的得多。将该版本与更直观的版本 `send('Hello', 'World')` 和 `point(1,2)` 进行比较，你可以立即看出可读性的差异。

2. **关键字参数 (Keyword Argument)** – 这些包含默认值，且不是强制性的。关键字参数有时用于发送到函数的可选参数。当一个函数包含至少 2 或 3 个（最好是更多）位置参数时，很难记忆。使用带有默认值的关键字参数会更有帮助。例如，你可以定义一个完整的 `send` 函数为 `send(message, to, cc=None, bcc=None)`。`cc` 和 `bcc` 的使用是可选的，如果给它们赋予其他值，它们的值均为 `None`。

   在 Python 中，有几种方法可以使用关键字参数调用函数。例如，你可以遵循定义中的参数顺序，而不显式地命名这些参数；例如，`send('Hello', 'World', 'Galactus', 'God')`。在这种情况下，你向 Galactus 发送了消息的副本，向 God 发送了密抄。你也可以以不同的顺序命名参数，例如，`send('Helloagain', 'World', bcc='God', cc='Galactus')`。除非你有非常充分的理由不尽可能地遵循正确的语法，否则最好避免这两个示例；它们既冗长又不可可读。最好的方法，即最接近函数定义的方法，是 `send('Hello', 'World', cc='Galactus', bcc='God')`。

3. **任意参数列表 (Arbitrary Argument List)** - 这是向函数传递参数的另一种方法。有时，函数的意图通过具有数量可扩展的位置参数数量的签名来表达得更好。在这种情况下，你最好使用 `*args` 结构来定义它。在参数体中，`args` 是所有剩余位置参数的元组。例如，你可以使用 `send(message, *args)`并将所有接收者列为单独参数：`send('Hello', 'Galactus', 'Dad', 'God')` —— 在函数体内，`*args` 等于 `('Galactus', 'Dad', 'God')`。

   然而，你应该非常谨慎地使用这种结构，因为它确实存在一些缺点。如果向函数发送了一个包含具有相同或相似性质参数的列表，更好的定义是使用带有单个参数的函数；该单个参数将是一个序列或列表。例如，如果 `send` 有多个接收者，你最好使用显式定义：`send('Hello', 'God', 'Dad', 'Galactus')`，然后通过 `send('Hello', ['God', 'Dad', 'Galactus'])` 调用它。通过这种方式，函数用户可以提前更改接收者列表，这为传递任何无法解包的序列打开了可能性，包括迭代器。

4. **任意关键字参数字典 (Arbitrary Keyword Argument Dictionary)** - 这是向函数传递参数的最后一种方法。如果函数需要未知的命名参数数组，你可以使用 `**kwargs` 结构。在函数体内，`**kwargs` 是一个字典，包含了所有已传递且未被函数签名中另一个关键字参数捕获的命名参数。

   然而，你应该像对待任意参数列表时那样保持同样的谨慎，因为原因基本相同。这些是强大的技术，只有在你能证明有必要使用它们时才应该使用。如果存在更清晰更简单的结构可以完成工作，则绝对不应该使用它们。

这真的取决于你，程序员，来决定哪些函数参数是可选关键字，哪些是位置参数，并确定是否应该使用更高级的技术来传递参数。

保持简单并遵循这些编写 Python 函数的规则：

* 具有可读性 – 名称和参数不需要任何解释
* 易于更改 – 你可以在不影响其他部分的情况下添加关键字参数

# 第 8 章：命名规范

坦率地说，Python 的命名规范有些混乱。但是，有一些建议的命名标准，所有新的包和模块（包括任何第三方框架）必须遵循这些标准。要学习的第一且最重要的原则是，当你使用作为公共 API 的名称时，必须使用反映其用途的规范，而不是其实现方式。

## 描述性 (Descriptive)

有许多不同的命名风格，因此独立识别使用的是哪种风格是有帮助的。这些是最常见的样式：

* `B` – 单字母大写
* `b` – 单字母小写
* `lowercase_with_underscores`
* `lowercase`
* `UPPERCASE_WITH_UNDCORES`
* `UPPERCASE`
* `CapitalizedWords` – 通常被称为 CamelCase，因为字母看起来有起伏
* `mixedCase` – 与 CamelCase 不同，首字母是小写的
* `Capital_Words_With_Underscore` – 不是漂亮的样式！
* 在 CamelCase 中使用缩写时，你应该确保所有的缩写字母都大写。例如，与其使用 `HttpServerError`，不如使用 `HTTPSError`。

你还可以使用另一种风格，即通过一个唯一的短前缀将一组相关的名称放在一起。这并不常用，但我提到它是为了让你知道它的存在。一个例子是 `os.stat()` 函数 —— 它将返回一个包含 `st_size`、`st_mode`、`st_mtime` 等名称的元组。

这些是使用后划线或前划线的格式，通常可以与任何大小写规范结合：

* `_one_leading_underscore` – 这通常是“内部使用”的指示，但力道并不强。
* `One_trailing_underscore_` – 通常用于防止与 Python 关键字冲突，例如：`tkinter.Toplevel(master, class_='ClassName')`
* `__two_leading_underscores` – 当你命名类属性时，这会引起修饰（mangling），例如：（在类 FootBar 内部，`__boo`）将变为 `_FootBar__boo`。




*   `two_leading_and_two_trailing_underscores` 是存在于用户控制命名空间中的属性或“魔法”对象。例如：`__init__`、`__file__` 或 `__import__`。

## 规范性

这些是你应该避免的名称：

在编写单字符变量名时，永远不要使用‘O’（大写字母）、‘l’（小写 L）或‘I’（大写 i）。取决于你使用的字体，这些字符可能与数字‘0’和‘1’混淆——如果你发现自己正在考虑使用 `l`，请改用大写的 `L`。

## 模块和包的命名

所有模块名称都应该是短且小写的。你可以在模块名中使用下划线，但仅在它能提高可读性时才这样做。Python 包也是如此——使用短且小写的名称，但不要使用下划线。

当你有一个用 C 或 C++ 编写的扩展模块，并且配有一个具有更面向对象接口的 Python 模块时，C 或 C++ 模块将以下划线开头，例如 `_socket`。

## 类名

类名通常使用 `CapWords` 或 `CamelCase` 约定。

内置名称有自己独立的约定，通常是单个单词或两个单词合并为一个词，例如‘Hello’或 `HelloWorld`。`CamelCase` 约定倾向于用于内置常量和异常名称。

## 类型变量

类型变量的名称通常使用 `CamelCase`，并且偏于使用短名称，例如 `Num`、`AnyStr`。你应该为变量添加后缀（`_co` 或 `_contra`）来声明逆变或协变行为。例如：

```python
Import TypeVar
```

变为

```python
VT_co = TypeVar('VT_co', covariant=True)
KT_contra = TypeVar('KT_contra', contravariant=True)
```

## 异常命名

异常是类，因此，你应该使用类的命名约定进行命名。尽管如此，如果异常是一个错误，请确保在名称上加上‘Error’ 后缀。

## 全局变量

只要变量在单个模块内部使用，其命名约定与函数命名约定相同。

## 函数

所有函数名均为小写，并在需要的地方用下划线分隔单词以提高可读性。`mixedCase` 约定仅在已经是这种风格的上下文中使用，以保持向后兼容。

## 实例变量和方法名

再次，函数的命名约定也适用于这里——使用带有间歇下划线的小写。如果你使用实例变量或非公共方法，应该使用单个前下划线。为了防止名称与子类冲突，应使用两个前下划线来触发 Python 的名称修饰（name mangling）规则。

当这些规则被触发时，名称将与类名一起修饰。例如，`class Foo` 包含一个名为 `__a` 的属性。无法通过 `Foo.__a` 访问。按照规则，只有当名称可能与设计为子类的类属性冲突时，才应该使用双前下划线。

## 常量

这些通常定义在模块级，全部大大写并用下划线分隔，例如 `MAX_OVERFLOW`。

## 继承设计

必须遵守的规则之一是确定实例变量或类方法是非公共还是公有的。如果你无法决定，请选择非公共，因为你以后可以轻松将其改为公共，而将公共改为非公共则没那么容易。

公共属性是指与类无关的客户端会使用的属性，而非公共属性是指不供第三方使用的属性。对于公共属性，你保证了从开始到结束的向后兼容；而对于非公共属性，你不保证，可以删除或更改该属性。注意，没有使用“private”（私有）一词，这是因为 Python 语言中没有真正的私有属性。

另一个属性类别是保护属性。在 Python 中，它们属于子类 API。有些类专门设计为供继承的类，无论是为了扩展还是修改某些行为方面。当你设计这样的类时，始终要确保对属性做出显式决定——它们是公有的、还是仅供基类使用的，还是属于子类 API？

结合以上所有内容，这些是 Pythonic 的指南：

*   公共属性不能不能有前下划线。
*   如果公共属性与关键字（保留字）冲突，请在属性名称末尾添加一个下划线。这是比使用拼写错误或缩写更优的方法。
*   对于公共数据属性，最好的方法是只暴露属性名称，而不使用任何复杂的修改器（mutator）或访问器（accessor）方法。如果简单的属性需要扩展其功能行为，Python 使得这很容易。
*   如果你正在使用一个将被子类的类，并且你也使用了不会被子类的属性，请考虑添加 2 个前下划线，但不要添加任何后下划线。这将触发名称修饰，并有助于降低子类具有相同名称属性时发生冲突的风险。

# 第 9 章：在语句和表达式中使用空格

首先，关于空格的一些反感点：

在以下情况下不要使用不必要的空格：

*   紧邻大括号、中括号或圆括号内部

良好的示例：
```python
ham(spam[1], {eggs: 2})
```

一个错误的示例：
```python
ham( spam[ 1 ], { eggs: 2 } )
```

*   紧邻冒号、分号或逗号之前：

一个良好的示例：
```python
if x == 4: print x, y; x, y = y, x
```

一个错误的示例：
```python
if x == 4 : print x , y ; x , y = y , x
```

然而，在涉及切片（slice）时，冒号类似于二进制运算符，两边应包含相同数量的空格。在使用扩展切片时，两个冒号必须包含完全相同的间距级别。唯一的例外是省略了切片参数以及对应的空格。

一个良好的示例：
```python
spam[1:8], spam[1:8:2], spam[:8:2], spam[1::2], spam[1:8:]
spam[lower:upper], spam[lower:upper:], spam[lower::step]
spam[lower+offset : upper+offset]
spam[: upper_fn(x) : step_fn(x)], ham[:: step_fn(x)]
spam[lower + offset : upper + offset]
```

一个错误的示例：
```python
spam[lower + offset:upper + offset]
spam[1: 8], ham[1 :8], ham[1:8 :2]
spam[lower : : upper]
spam[ : upper]
```

*   在位于函数调用参数列表的起始圆括号之前：

一个良好的示例：
```python
ham(1)
```

一个错误的示例：
```python
ham (1)
```

*   紧邻开始切片或索引的左括号之前：

一个良好的示例：
```python
dct['key'] = lst[index]
```

一个错误的示例：
```python
dct ['key'] = lst [index]
```

*   当运算符（如赋值运算符）周围有多个空格时，且这些空格是为了使其与另一个运算符对齐。

一个良好的示例：
```python
x = 1
y = 2
long_variable = 3
```

一个错误的示例：
```python
x               = 1
y               = 2
long_variable = 3
```

## 其他建议

避免在整个代码代码中使用行尾空格，因为它是不可见的且可能会导致混淆。例如，如果你输入了一个反斜杠，后面跟着一个空格然后换行——这不会被视为行延续。事实上，某些文本编辑器不会保留它，有些项目包含的 pre-commit hooks 也会直接拒绝它——其中之一就是 CPython。

以下二进制运算符应该被单个空格包围——每侧一个：

*   赋值 (`=`)
*   复合赋值 (`+=`, `-=` 等）

以下比较运算符的处理方式相同：

*   `==` 
*   `<`
*   `>`
*   `!=` 
*   `<>`
*   `<=`
*   `>=`
*   `in`
*   `not in`
*   `is`
*   `is not`

以及布尔值：

*   `and`
*   `or`
*   `not`





如果你使用了优先级不同的运算符，请考虑在优先级最低的运算符周围加上空格——请根据你的最佳判断来决定。然而，你使用的空格不应多于一个，并确保运算符两侧的空格数量相同——不要在一侧放 1 个空格而在另一侧放 2 个：

### 良好的示例：

```
i = i + 1
submitted += 1
x = x*2 - 1
hypot2 = x*x + y*y
c = (a+b) * (a-b)
```

### 不良的示例：

```
i=i+1
submitted +=1
x = x * 2 - 1
hypot2 = x * x + y * y
c = (a + b) * (a - b)
```

当你使用 `=` 符号来指示参数或关键字参数的默认值时，不要在符号符号周围使用空格：

### 良好的示例：

```python
def complex(real, imag=0.0):
    return magic(r=real, i=imag)
```

### 不良的示例：

```python
def complex(real, imag = 0.0):
    return magic(r = real, i = imag)
```

对于函数注解中的冒号，使用标准规则，并确保在使用 `->` 时其周围有空格：

### 良好的示例：

```python
def munge(input: AnyStr): ...
def munge() -> AnyStr: ...
```

### 不良的示例：

```python
def munge(input:AnyStr): ...
def munge()->PosInt: ...
```

当你结合使用默认值和参数注解时，`=` 符号周围应该有空格——除非该参数同时具有默认值和注解，否则不要这样做：

### 良好的示例：

```python
def munge(sep: AnyStr = None): ...
def munge(input: AnyStr, sep: AnyStr = None, limit=1000): ...
```

### 不良的示例：

```python
def munge(input: AnyStr=None): ...
def munge(input: AnyStr, limit = 1000): ...
```

使用复合语句（在同一行上写多个语句）不是良好的做法：

### 良好的示例：

```python
if foo == 'that':
    do_that_thing()
do_one()
do_two()
do_three()
```

### 尽量不要这样做：

```python
if foo == 'that': do_that_thing()
do_one(); do_two(); do_three()
```

偶尔情况下，如果语句体很小，在一行内使用 `if`、`for` 和 `while` 语句是可以接受的，但对于包含多个子句的语句，永远不要这样做。此外，永远不要折叠非常长的行：

### 尽量不要这样做：

```python
if foo == 'that': do_that_thing()
for x in lst: total += x
while t < 10: t = delay()
```

### 绝对不要：

```python
if foo == 'that': do_that_thing()
else: do_non_that_thing()
try: something()
finally: cleanup()
do_one(); do_two(); do_three(long, argument,
                             list, like, this)
if foo == 'that': one(); two(); three()
```

# 结论

再次感谢阅读我的书，我真心希望它能够帮助你理解如何编写更有效高效的 Python 代码。

从这里开始，下一步简单来说就是实践。你做得越多，进步得越快，最终你将像专业人士一样编写 Python 代码！通过研究、加入在线 Python 论坛和加入 Python 社区来学习更多并提升你的技能。

最后，如果你觉得这本书有帮助，可以请你帮个忙吗？请考虑在 `Amamzon.com` 上给我留评论；这不仅对我有帮助，对潜在读者也有益。

祝你成为更好的 Python 程序员的道路一路顺利

# 关于作者

Charlie Masterson 是一位计算机程序员和导师，开发过多个应用程序和计算机程序。

作为一名计算机科学学生，他很早就对编程感兴趣，但对学习极其复杂的课题感到沮丧。

Charlie 想要一种能够轻松学习并提高编程技能的教学方法。他很快发现了一系列让他学得更快、更好的课程。

通过同样的方法，Charlie 成功学习了不同的编程语言，现在通过写书来教授这些知识。

通过他编写关于计算机编程的书，他希望提供巨大的价值，并帮助对学习计算机主题感兴趣的读者。

