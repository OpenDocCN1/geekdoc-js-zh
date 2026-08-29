
# JavaScript 任务 (Mission: Code (Alternator Books))

要下载“你的任务：来代码吧！”活动所需的文件，请访问 [`qrs.lernerbooks.com/JS`](http://qrs.lernerbooks.com/JS/)。你需要使用 Google Chrome 浏览器来完成书中各处的“你的任务：来代码吧！”活动。要下载 Google Chrome 浏览器，请访问 [`www.google.com/chrome/`](https://www.google.com/chrome/)。

# 引言

## 屏幕后的语言

想写视频游戏甚至控制机器人吗？JavaScript 是学习实现这些目标的极佳编程语言。

JavaScript 无处不在！Facebook、Twitter、Amazon 和 YouTube 等流行网站都使用 JavaScript 来让他们的网站变得有趣且具有互动性。动画、声音和带有位置标记的地图都是 JavaScript 应用的一些示例。创建你喜爱的网站的程序员们使用 JavaScript 制作了它们。

# 字符串与布尔值

## 数据类型与操作

像你狗的名字和眼睛颜色这样的数据在 JavaScript 中用字符串（`strings`）表示。字符串是字母、数字和标点符号的序列。字符串必须包含在引号中，例如：`“I am a string.”`

`.length` 命令告诉你字符串中有多少个字符。

最后，只能取两个可能值之一（`true` 或 `false`）的数据被称为 `Boolean`（布尔值）。布尔值可以表示你是否喜欢某本书。

每种数据类型都有其自己的一组可能的操作，或者处理它们的方法。你可以将两个数字相乘，但不能相乘两个字符串。你可以找到字符串的长度或字符数量。对于布尔，你可以检查两个值是否都为真。当你处理每种数据类型时，你将学习哪些运算符可以用它们。

你可以将任何内容转换为数据，从你是否喜欢某本书到你读了多少页，再到你喜欢的角色名字。

## 变量

变量存储了你以后要用的数据。当数据存储在变量中时，它被称为值（`value`）。每个变量可以有一个唯一的名称，并恰好存储一个值。要创建一个变量，使用关键字 `var`。

```javascript
var myDogsName = "Rover";
var myEyeColor = "brown";
var myAge = 11;
var isBookGood = true;
```

选择有意义且自明其意的变量名是有帮助的，这样你的代码易于阅读。变量名不能有空格，也不能是关键字。

许多 JavaScript 控制台使用不同的颜色来帮助显示代码的每个部分。代码在你的屏幕上可能是这样的。

在上一页的示例中，`var myDogsName` 告诉 JavaScript `myDogsName` 是一个变量。`=` 是告诉 JavaScript `myDogsName` 应该存储值 `Rover` 的方式。注意 `“Rover”` 被包含在引号中，表示它是一个字符串。

同样，`myAge` 是存储数值 `11` 的变量名。`isBookGood` 存储了布尔值 `true`。如果你的家里有宠物，当你使用 JavaScript 时，它的名字可以是一个变量。

## 重新赋值变量

你可以更改已创建的变量的值。当你这样做时，不需要关键字 `var`，因为你不是在第一次创建变量。例如：

```javascript
myDogsName = "Fido";
myEyeColor = "green";
```

是时候尝试一个有趣的活动了！首先，打开你的控制台。创建一个名为 `myFruit` 的新变量并给它赋值 `“Strawberry.”`。然后输入 `console.log(myFruit)`。你看到了什么？现在，通过分配一个新值 `“apple.”` 来更改 `myFruit` 的值。再次使用 `console.log(myFruit)`。你看到了什么？

## 比较运算符

人类在生活中会这样做，计算机需要比较两个事物以查看它们是否相同。这种检查使用比较运算符完成。比较运算符的结果为 `true` 或 `false`。

### 存储数据

一个比较运算符是 `===`。该运算符检查值和类型是否相同。例如，虽然数字 `12` 和字符串 `“12”` 有相同的值，但它们的类型不同。

```javascript
var numericValue = 12;
var stringValue = "12";
numericValue == stringValue // true
numericValue === stringValue // false
```

有很多常见的比较运算符。让我们为下面的示例创建一个变量 `x = 10`。在这里，字母 `x` 代表数字 `10`。

| 运算符 | 操作 | 示例 | 结果 |
| :--- | :--- | :--- | :--- |
| `==` | 等于 | `x == 11` | false |
| `!=` | 不等于 | `x != 11` | true |
| `>` | 大于 | `x > 12` | false |
| `<` | 小于 | `x < 12` | true |
| `>=` | 大于等于 | `x >= 10` | true |
| `<=` | 小于等于 | `x <= 10` | true |

## 数组

数组在 JavaScript 中也很重要。假设你正在写生日愿望清单。你在一张纸上写下第一个项目（或变量）。在另一张纸上写第二个项目（变量）。你继续这样写下去，直到每个项目都写下来。

但你不想跟踪很多张带有愿望清单项的纸。你想制作一个大列表，将所有变量写在一张纸上。这就是数组派上用场的地方。数组用于表示各种事物的列表。

与其在像下面的列表中拥有五个不同的变量：

```javascript
var myFirstItem = "bicycle";
var mySecondItem = "bike helmet";
var myThirdItem = "bike bell";
var myFourthItem = "bike mudguard";
var myFifthItem = "bike basket";
```

JavaScript 允许你使用方括号创建一个包含许多项的数组。

```javascript
var myWishList = ["bicycle", "bike helmet", "bike bell", "bike mudguard", "bike basket"];
```

JavaScript 会记住数组中元素的顺序。这种顺序被称为 `index`（索引）。如果你忘记了数组中的第一个元素是什么（例如），你可以询问 JavaScript。然而，索引有点小技巧，因为第一个元素被标记为 0，而不是 1。在例例中，“bicycle”是第 0 个元素，“bike helmet”是第 1 个，以此类推。

以下是如何使用索引在数组中查找特定元素的示例：

```javascript
console.log(myWishList[3]); // bike mudguard
console.log(myWishList[4]); // bike basket
```

## 对象

假设你想存储关于你猫咪的信息，比如它的昵称、年龄、颜色、品种、最喜欢的玩具和最喜爱的食物。你还想为你朋友的猫和你表哥的猫存储相同的信息。这意味着有大量的变量需要记录。为了帮助你记录所有信息，你可以创建一个对象。

对象是另一种存储数据的方式。对象不像数组那样使用索引来访问数据，而是使用被称为 `keys`（键）的字符串。每个键都对应一个值。在我们的猫对象中有六个键值对——每个信息各对应一个。

```javascript
var myCat = {
  "nickname": "Fluffy",
  "age": 2,
  "color": "white",
  "breed": "Persian",
  "toy": "paper ball",
  "food": "yummy yums"
};
```

JavaScript 几乎可以完成任何你想让它做的事情，包括存储猫颜色、品种、最喜欢的玩具等更多信息！

对象也可以由数组组成。键可以引用一个数组，而不是单个值。请看下例：

```javascript
var iceCreamsike = ["rock", "chocolate"];
var myFavoriteThings = {
  "authors": ["Judy Blume", "J. Rowling", "Walter Dean Myers"],
  "iceCream": iceCreamsike,
  "petsIHave": ["cat", "goldfish", "tarantula"]
};
```

### Mission: Code It!

在 Chrome 中打开 JavaScript 控制台。

1. 创建一个数组 `myTopFiveBooks`，由你最喜欢的五本书名组成。
2. 创建一个数组 `myTopFiveGames`，由你最喜欢的五种桌游组成。
3. 创建一个数组 `myTopFiveSnacks`，由你最喜欢的五种零食组成。
4. 最后，创建一个对象 `topFiveThings`，由你在步骤 1-3 中创建的数组组成。
5. 对你的对象 `topFiveThings` 使用 `console.log`。你看到了什么？

# Chapter 4 条件语句与函数

每天都会根据某些条件是否成立来做出决定。这种决策在编程中可以通过条件语句来实现。最简单的条件语句是 `if`：如果某事为真，则执行操作。

如果你想在条件为真执行某件事，而在假时不做另一件事怎么办？在这种情况下，你可以使用 `if...else`。例如，如果你今天觉得不舒服就留在家，否则就去学校。

```javascript
var feelsSick = false;
if (feelsSick == true) {
  console.log("Stay home.");
} else {
  console.log("Go to school.");
}
```

当你想要反复执行同一个任务时，你可以编写函数。函数是一组你命名的指令。函数就像快捷方式。每当你把函数放入代码中，JavaScript 就知道运行所有的指令，而不需要你每次都重写它们。

函数的写法如下：

```javascript
function myFirstFunction(){
  console.log("Hi, Coder!");
}
```

使用名称 `myFirstFunction()` 来指示电脑显示“Hi, Coder!”。

```javascript
myFirstFunction(); // Hi, Coder!
```

函数旁边的括号可以包含参数（`arguments`）。参数可以是数字、字符串、布尔值甚至是变量。例如，如果你写了一个检查数字是否为偶数的函数，你可以测试不同的数字作为参数。

现在你已经掌握了一些 JavaScript 的基础知识。继续磨练你的技能吧。谁知道呢？也许你可能会开发出下一个伟大的 JavaScript 作品！

### Mission: Code It!

在 Chrome 中打开控制台。定义一个函数 `guessTheNumber`，接收数字 `myGuessNumber` 作为唯一参数。在函数内部，创建一个变量 `myRandomNumber` 并赋值一个 1 到 10 之间的数字。使用条件语句 `if...else` 检查 `myGuessNumber` 是否等于 `myRandomNumber`。如果是，函数应该显示“You guessed it!”；否则（else），它应该显示“Nope, try again.”。

看看你的朋友能否猜中那个数字！使用这段代码作为示例来帮助完成活动。

# Glossary

- **arguments**: 传递给函数的值，以便它们执行任务
- **arrays**: 存储项目列表的变量
- **conditional statements**: 根据条件的真假告诉计算机执行不同任务的代码行
- **index**: 数组中元素的数字顺序
- **keywords**: 编程语言中只能以特定方式使用的单词
- **object**: 描述某物的键的集合
- **programming language**: 一组告诉计算机如何理解程序的规则

# 定义

- **程序 (programs)**: 计算机执行的特定有序命令集
- **字符串 (strings)**: 用引号括起来的字母、数字和符号序列
- **语法 (syntax)**: 规定编写程序时符号、关键字和允许单词的规则
- **变量 (variable)**: 用于存储数据的容器

## 更多信息

- JavaScript 简介 [`www.codecademy.com/learn/introduction-to-javascript`](https://www.codecademy.com/learn/introduction-to-javascript)
- JavaScript 教程 [`www.w3schools.com/js/`](https://www.w3schools.com/js/)
- 学习 JavaScript [`www.learn-js.org`](https://www.learn-js.org)
- Morgan, Nick. 《JavaScript for Kids：编程的趣味介绍》。San Francisco: No Starch, 2015.
- Preuitt, Sheela. 《Mission HTML》。Minneapolis: Lerner Publications, 2020.
- Young Rewired State. 《Get Coding!学习 HTML, CSS 和 JavaScript 并构建网站、App 和游戏》。Somerville, MA: Candlewick, 2017.

## 图片致谢

图片来源：Sheela Preuit 的各种截图。其他图片：Caiaimage/Robert Daly/Getty Images, 第 5 页；Tuan Tran/Getty Images, 第 7 页；matejmo/Getty Images, 第 8 页；vgajic/Getty Images, 第 9 页；Hero Images/Getty Images, 第 13 页；Phil McDonald/Shutterstock.com, 第 15 页；Kasabutskaya/Shutterstock.com, 第 19 页；rukawajung/Shutterstock.com, 第 23 页。封面及内设计元素：HuHu/Shutterstock.com（跑步）；Vankad/Shutterstock.com（电路）；Bro Studio/Shutterstock.com（圆形图案）；Leremy/Shutterstock.com（人物）。

## 索引

- **动画 (animations)**, 5, 9
- **数组 (arrays)**, 20–24
- **布尔值 (Booleans)**, 11, 13, 15, 28
- **比较运算符 (comparison operators)**, 18–20
- **计算机 (computers)**, 6, 7, 10, 28
- **条件语句 (conditional statements)**, 26
- **控制台 (console)**, 17, 25, 29
- **数据 (data)**, 8, 10, 14, 23
- **函数 (functions)**, 27–29
- **键 (keys)**, 23–24
- **对象 (objects)**, 23–25
- **程序 (programs)**, 6
- **标点符号 (punctuation)**, 7, 12
- **机器人 (robots)**, 4
- **字符串 (strings)**, 11, 13, 15, 19, 23, 28
- **语法 (syntax)**, 7
- **真或假 (true or false)**, 13, 18, 27
- **变量 (variables)**, 14–17, 19–22, 28–29
- **视频游戏 (video games)**, 4, 9
- **网站 (websites)**, 5, 8, 18
