
# 前端 JavaScript 和 jQuery 速查表

## 简介

JavaScript 是前端 Web 应用的基本构建块。

jQuery 是一个流行的用于操作 DOM 的库。

在本书中，我们将探讨如何将两者结合使用。

## JavaScript

JavaScript 是世界上最流行的编程语言之一。要有效使用它，我们需要了解其基础知识。

在本节中，我们将介绍 JavaScript 的基础知识。

### 警告框

`alert` 函数会显示一个包含我们传入文本的警告框。

文本来自字符串参数。

例如，可以这样写：

```javascript
alert("hello world!");
```

然后会显示“hello world”。

它是一个全局函数，因此是 `window` 的一个属性。`window.alert` 与 `alert` 相同。

简写形式在代码中使用没有问题。

### 变量与字符串

字符串是 JavaScript 代码的基本元素。它们存储文本数据。

具有给定名称的变量只能声明一次。

字符串可以存储在变量中。变量是我们选择并赋值的名称，以便存储数据供以后使用。

例如，我们可以这样写：

```javascript
let name = "james";
```

来存储名字。

我们可以将用 `let` 声明的变量设置为新值。

例如，我们可以这样写：

```javascript
let name = "james";
name = "mark";
```

那么 `name` 的值将是 `"mark"`。

我们可以声明一个变量而不给它赋值，此时它是未定义的。

例如，我们可以这样写：

```javascript
let name;
name = "james";
```

用 `let` 声明的变量可以这样操作。

变量可以使用任何不在保留关键字列表中的名称来声明。

该列表位于 [`developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords)。

变量不用引号括起来，而文本字符串需要用引号括起来。

JavaScript 字符串可以用单引号或双引号括起来。

也可以用反引号括起来。

如果用反引号括起来，则字符串中必须嵌入变量。

例如，我们可以这样写：

```javascript
let firstName = 'james';
let lastName = 'smith';
let name = `${firstName} ${lastName}`;
```

我们将 `firstName` 和 `lastName` 的值插值到字符串中。因此 `name` 应该是 `'james smith'`。

这就是模板字面量。我们可以在字符串中放入任何表达式。

这是一种将各种表达式组合成字符串的非常方便的方式。

现在我们可以赋值变量，也可以将变量传递给 `alert`，而不是传递整个字符串。

例如，我们可以这样写：

```javascript
let text = "hello world!"
alert(text);
```

我们将 `text` 作为参数传递给 `alert` 来显示警告框。

在 `text` 定义之后，我们可以在任何地方引用它。

### 变量与数字

数字是 JavaScript 中的另一种原始数据类型。

我们也可以将它们赋值给变量。

例如，我们可以这样写：

```javascript
let length = 100;
```

这使得对数字进行操作变得容易。例如，我们可以给 `length` 加上一个数字：

```javascript
length + 10
```

那么 `length` 与 10 的和是 110。

我们知道 `length` 不是变量，因为它没有用引号括起来。

而单独的数字可以用作变量名，因此 JavaScript 知道它是一个数字。

我们可以将 10 赋值给一个变量，然后用变量替换它。

例如，我们可以这样写：

```javascript
let length = 100;
let additionalLength = 10;
let totalLength = length + additionalLength;
```

我们有一个 `additionalLength` 变量，将其加到 `length` 上，并将和赋值给 `totalLength` 变量。

### 遍历数组

我们可以使用数组的 `length` 属性作为结束条件来遍历数组。

例如，我们可以这样写：

```javascript
let matchFound = false;
for (let i = 0; i < cleanestCities.length; i++) {
  if (city === cleanestCities[i]) {
    matchFound = true;
    console.log("It's one of the cleanest cities");
  }
}
```

我们使用 `cleanestCities` 数组的 `length` 属性作为结束条件。

我们从 0 循环到 `cleanestCities.length — 1`。这样，我们从头到尾遍历所有项，而无需为结束条件设置固定的数值。

如果我们想提前停止循环，可以使用 `break` 关键字。

例如，我们可以这样写：

```javascript
for (let i = 0; i < cleanestCities.length; i++) {
  if (city === cleanestCities[i]) {
    console.log("It's one of the cleanest cities");
    break;
  }
}
```

如果 `city` 等于 `cleanestCities[i]`，则用 `break` 结束循环。

我们可以在代码中嵌套循环。例如，我们可以这样写：

```javascript
let firstNames = ['james', 'mary', 'alex'];
let lastNames = ['jones', 'wong', 'green'];
let fullNames = [];
for (let i = 0; i < firstNames.length; i++) {
  for (let j = 0; j < lastNames.length; j++) {
    fullNames.push(`${firstNames[i]} ${ lastNames[j]}`);
  }
}
```

我们在一个 `for` 循环内部嵌套了另一个 `for` 循环。

外层循环遍历 `firstNames` 数组。

每次迭代中，内层循环都会运行，遍历 `lastNames` 数组。

在内层循环中，我们将 `firstNames[i]` 和 `lastNames[j]` 的组合推入 `fullNames` 数组。

结果是 `firstNames` 和 `lastNames` 条目的所有组合都被添加到 `fullNames` 数组中。

我们可以根据需要设置任意多层嵌套。然而，嵌套越多，代码越难阅读。

### 改变大小写

我们可以使用 `toUpperCase` 和 `toLowerCase` 方法来改变字符串的大小写。

`toUpperCase` 将字符串中的所有字母转换为大写。

`toLowerCase` 将字符串中的所有字母转换为小写。

例如，我们可以这样写：

```javascript
"Santa Fe".toLowerCase()
```

然后得到：

```javascript
"santa fe"
```

返回。

而如果我们写：

```javascript
"Santa Fe".toUpperCase()
```

则会得到：

```javascript
"SANTA FE"
```

### 字符串长度与部分提取

我们可以使用 `length` 属性获取字符串的字符数。

例如，我们可以这样写：

```javascript
"Santa Fe".length
```

返回 8。

要获取字符串的一部分，可以使用 `slice` 方法。

它接受要提取的起始索引和结束索引。

结束索引本身不包含在内。

例如，如果我们写：

```javascript
"Santa Fe".slice(2, 4)
```

则会返回 `"nt"`。

### 查找字符串片段

我们可以使用 `indexOf` 方法查找字符串片段。如果传入的字符串存在于调用 `indexOf` 的字符串中，它会返回该字符串的起始索引。

例如，我们可以这样写：

```javascript
"Santa Fe".indexOf('Fe')
```

返回 6，因为字符 `'F'` 位于索引 6。

### if 语句

`if` 语句让我们有条件地执行代码。

例如，我们可以这样写：

```javascript
const answer = prompt("Where's the capital of Italy?");
if (answer === "Rome") {
  alert("Correct!");
}
```

添加一个提示框来接收问题的答案。

然后在 `if` 语句中检查答案。如果 `answer` 是 `'Rome'`，则显示 `'Correct!'` 警告框。

`if` 语句后面跟着一个我们正在检查的布尔表达式。

如果布尔表达式返回 `true`，则执行花括号之间的代码。

我们应该始终使用 `===` 来检查值相等，因为它会检查类型和值。

简单的 `if` 语句可以不写花括号，或者将语句写在一行。

但使用花括号更便于阅读，因为更清晰。

### 比较运算符

`===` 运算符是比较运算符。

它是相等运算符。

用于比较两个事物是否相等。

我们可以使用相等运算符来比较任意两个表达式的返回值。

例如，我们可以这样写：

```javascript
if (totalCost === 81.50 + 100) {
```

或者：

```javascript
if (fullName === firstName + " " + "wong") {
```

字符串比较区分大小写，因此只有大小写完全相同时，字符串才被视为相等。

如果我们想检查两个表达式是否不相等，可以使用 `!==` 不等比较运算符。

例如：

```javascript
"Rose" !== "rose"
```

这会返回 `true`，因为它们的字母大小写不同。

JavaScript 还提供了更多运算符，包括：

- `>` 表示大于运算符。
- `<` 表示小于运算符。
- `>=` 表示大于或等于运算符。
- `<=` 表示小于或等于运算符。

我们可以这样使用它们：

```javascript
if (2 > 0) {
if (0 < 2) {
if (2 >= 0) {
if (2 >= 1) {
if (0 <= 2) {
if (1 <= 2) {
```

### if…else 和 else if 语句

如果有多个条件需要检查，可以使用 `else` 关键字来添加更多分支。

例如，我们可以这样写：

```javascript
const answer = prompt("意大利的首都在哪里？");
if (answer === "罗马") {
  alert("正确！");
} else {
  alert("错误！");
}
```

`else` 关键字位于当 `answer` 不是 `'罗马'` 时执行的代码块之前。

如果有更多分支，可以添加 `else if` 语句。

例如，我们可以这样写：

```javascript
const answer = prompt("意大利的首都在哪里？");
if (answer === "罗马") {
  alert("正确！");
} else if (answer === "梵蒂冈") {
  alert("很接近！");
} else {
  alert("错误！");
}
```

当 `answer` 是 `'梵蒂冈'` 时，会执行相应代码。

如果 `answer` 既不是 `'罗马'` 也不是 `'梵蒂冈'`，则执行最后一个代码块。

### 测试条件组合

我们可以用 `if` 语句测试多个条件。

要组合它们，可以使用 `&&` 或 `||` 运算符。

`&&` 是逻辑与运算符，`||` 是逻辑或运算符。

例如，我们可以这样写：

```javascript
if (weight > 300 && time < 6) {
  alert("运动员");
} else {
  alert("厨师");
}
```

同时检查 `weight` 和 `time` 的值。

如果 `weight` 小于 300 且 `time` 小于 6，则执行第一个代码块。

否则，执行第二个代码块。

我们可以链式组合更多条件：

```javascript
if (weight > 300 && time < 6 && age > 17 && gender === "male") {
  alert("运动员");
} else {
  alert("厨师");
}
```

这会检查所有条件是否都为 `true`。如果全部为 `true`，则执行第一个代码块。

否则，执行第二个代码块。

`||` 运算符的使用方式类似。

例如，我们可以这样写：

```javascript
if (SAT > avg || GPA > 2.5 || sport === "football") {
  alert("录取");
} else {
  alert("未录取");
}
```

如果任意一个条件返回 `true`，`||` 运算符就会返回 `true`。

我们可以混合使用 `||` 和 `&&`。

例如，我们可以这样写：

```javascript
if (age > 65 || age < 21 && res === "U.S.")
```

`&&` 优先级更高，因此先计算 `res === "U.S."`。

然后计算 `||` 运算符。

为了更清晰，应该用括号将表达式括起来，方便所有人阅读：

```javascript
if ((age > 65 || age < 21) && res === "U.S.")
```

### 嵌套 if 语句

我们可以嵌套 `if` 语句。例如，我们可以这样写：

```javascript
if (c === d) {
  if (x === y) {
    g = h;
  } else if (a === b) {
    g = h;
  } else {
    v = u;
  }
} else {
  v = u;
}
```

我们将内部表达式缩进两个空格，使其易于输入和阅读。

嵌套层级不宜过多，否则难以阅读。

### 数组

程序中经常需要存储多个值。

为了简化操作，我们可以使用数组。

例如，与其重复声明变量来存储相似的值：

```javascript
let city0 = "奥斯陆";
let city1 = "罗马";
let city2 = "多伦多";
let city3 = "丹佛";
let city4 = "洛杉矶";
let city5 = "西雅图";
```

我们可以将它们全部放入一个数组中：

```javascript
let cities = ["奥斯陆", "罗马", "多伦多", "丹佛", "洛杉矶", "西雅图"];
```

数组对于存储固定大小或动态大小的数据列表非常有用。

我们可以通过索引访问数组元素。

例如，我们可以这样写：

```javascript
cities[2]
```

JavaScript 数组可以包含不同类型。例如，我们可以这样写：

```javascript
let mixedArray = [1, "james", "mary", true];
```

第一个元素的索引是 0。变量的命名规则同样适用于数组。

数组和其他变量一样，只能声明一次。

### 查找字符串中某个位置的字符

我们可以使用 `charAt` 方法或方括号表示法来查找字符串中某个位置的字符。

例如，我们可以这样写：

```javascript
let firstChar = 'james'.charAt(0)
```

那么 `firstChar` 就是 `'j'`。

这与以下写法相同：

```javascript
let firstChar = 'james'[0]
```

两者效果相同，但由于方括号更简洁，使用更频繁。

### 替换字符

`replace` 方法允许我们替换字符。

例如，我们可以这样写：

```javascript
let newText = text.replace("第二次世界大战", "二战");
```

将 `"第二次世界大战"` 替换为 `"二战"`。

它会搜索第一个匹配项并进行替换。

要搜索所有匹配项并全部替换，需要使用正则表达式：

```javascript
let newText = text.replace(/第二次世界大战/g, "二战");
```

`g` 标志表示全局匹配，即替换所有匹配项。

### 数字取整

我们可以使用 `Math.round` 方法对数字进行四舍五入。

例如，我们可以这样写：

```javascript
let score = Math.round(11.1);
```

这样 `Math.round` 会将 11.1 四舍五入为 11。

它会四舍五入到最接近的整数。

当小数部分为 .5 时，函数会向上取整。

要始终向上取整到最接近的整数，可以使用 `Math.ceil` 方法：

```javascript
let score = Math.ceil(11.1);
```

得到 12。

要始终向下取整到最接近的整数，可以使用 `Math.floor` 方法：

```javascript
let score = Math.floor(11.1);
```

### 生成随机数

JavaScript 自带生成随机数的函数。

`Math.random` 方法可以生成 0 到 1 之间的随机数。

例如，我们可以这样写：

```javascript
let randomNumber = Math.random();
```

返回的数字有 16 位小数。

### 将字符串转换为整数和小数

将包含数字的字符串转换为整数或小数是我们经常需要做的事情。

我们可以使用 `parseInt` 方法将字符串转换为整数。

使用 `parseFloat` 方法将字符串转换为小数。

例如，我们可以这样写：

```javascript
let currentAge = prompt("请输入你的年龄。");
let age = parseInt(currentAge);
```

我们使用 `parseInt` 方法将输入的数字转换为整数。

`prompt` 总是返回字符串，因此我们需要将其转换为整数。

要将输入的文本转换为小数，可以使用 `parseFloat`：



```javascript
let currentAge = prompt("请输入你的年龄。");
let age = parseFloat(currentAge);
```

## 字符串与数字的相互转换

要将字符串转换为数字，可以使用全局函数`Number`：

```javascript
let num = Number('123');
```

那么`num`就是`123`。

要将数字转换为字符串，可以使用`toString`方法：

```javascript
let num = 1234;
let numberAsString = num.toString();
```

`numberAsString`就是`'1234'`。

## 添加和删除元素

使用 JavaScript 可以轻松地添加和删除数组元素。

要添加元素，只需将值赋给所需的数组索引。

例如，我们可以这样写：

```javascript
let animals = [];
animals[0] = "狗";
animals[1] = "猫";
animals[2] = "老鼠";
```

我们通过创建变量并赋值为空数组来创建`animals`数组。

然后为`animals`的指定索引赋值。

我们可以对任何索引执行此操作，索引不必连续或按顺序。

要删除数组中的最后一个元素，可以调用`pop`方法：

```javascript
animals.pop()
```

另一种添加元素的方法是使用`push`方法：

```javascript
animals.push("鱼", "鸟");
```

`push`将元素添加到数组末尾。

要删除数组的第一个元素，可以使用`shift`：

```javascript
animals.shift();
```

要在数组开头添加一个或多个元素，可以调用`unshift`：

```javascript
animals.unshift("鱼", "鸟");
```

`splice`方法可以在数组中的任意位置插入一个或多个元素：

```javascript
pets.splice(2, 2, "pig", "duck", "emu");
```

第一个参数是要插入的起始索引。

第二个参数是要删除的元素数量。

后续参数是我们想要替换被删除元素而插入的元素。

`slice`方法允许我们复制任意位置的一个或多个连续元素，并将它们放入一个新数组中。

例如，我们可以这样写：

```javascript
let pets = animals.slice(2, 4);
```

从`animals`中复制索引 2 到 3 的元素，并返回该数组。

第一个参数是要复制的起始索引。第二个参数是结束索引的后一个位置。

第二个索引本身不包含在范围内。

## `for`循环

JavaScript 提供了循环，以便我们可以重复运行代码。

为此，我们可以使用`for`循环：

```javascript
for (let i = 0; i <= 10; i++) {
  if (city === cleanestCities[i]) {
    console.log("It's one of the cleanest cities");
  }
}
```

`for`循环由头部组成，头部包含起始索引、继续运行循环的条件以及更新索引的语句。

在循环体中，我们可以执行想要的操作。

在上面的例子中，我们检查`city`是否等于`cleanestCities[i]`。

如果为`true`，则通过`console.log`输出一条消息。

循环索引用于访问数组元素，同时也用于使循环向结束条件（即`i <= 10`）推进。

如果`i`大于 10，则循环停止。

我们还可以在`for`循环中设置标志，以便记录某些信息。

例如，我们可以这样写：

```javascript
let matchFound = false;
for (let i = 0; i <= 10; i++) {
  if (city === cleanestCities[i]) {
    matchFound = true;
    console.log("It's one of the cleanest cities");
  }
}
```

一旦我们从`cleanestCities`中找到等于`city`的值，就将`matchFound`设置为`true`。

## 数学表达式

我们应该消除 JavaScript 数学表达式中的歧义。

例如，如果我们有：

```javascript
let totalCost = 1 + 3 * 10;
```

那么读者可能会对哪个运算先执行感到困惑。

JavaScript 对运算符有优先级规则。它们通常遵循与普通数学相同的规则。

然而，我们可以通过将具有更高优先级的表达式用括号括起来，让每个人的生活更轻松。

例如，我们可以这样写：

```javascript
let totalCost = 1 + (3 * 10);
```

这样我们将乘法表达式括起来。

现在我们知道乘法运算先执行。

如果我们移动括号，那么运算顺序就会不同。

例如，如果我们有：

```javascript
let totalCost = (1 + 3) * 10;
```

那么加法会在乘法之前执行。

## 拼接字符串

字符串是文本值，可以通过拼接组合在一起。

例如，我们可以这样写：

```javascript
alert("Thanks, " + userName + "!");
```

使用`+`运算符将 3 个表达式组合成 1 个。

如果`userName`是`'james'`，那么我们会得到：

```javascript
'Thanks, james!'
```

这三个部分组合在一起，作为一个字符串返回。

我们可以将字符串与任何其他 JavaScript 表达式拼接。

它们会自动转换为字符串，以便可以拼接在一起。

所以如果我们有：

```javascript
alert("2 plus 3 equals " + 2 + 3);
```

那么我们会得到`'2 plus 3 equals 23'`。

这是因为 2 和 3 在拼接之前被转换成了字符串。

一种更便捷的组合字符串和其他表达式的方法是使用模板字面量。

例如，我们可以这样写：

```javascript
alert(`2 plus 3 equals ${2 + 3}`);
```

我们将引号替换为反引号。

然后使用`${}`符号包围 JavaScript 表达式，以插入这些表达式。

这样，`2 + 3`返回一个数字，因为它们与字符串拼接在一起。

所以我们得到`'2 plus 3 equals 5'`。

## 提示框

提示框允许我们向用户询问一些信息，并提供一个用于回答的输入字段。

例如，我们可以这样写：

```javascript
let name = prompt("Your name?", "mary");
```

我们调用`prompt`，第一个参数是问题字符串。

第二个参数是返回的默认答案。

如果调用它，浏览器会显示一个带有输入框的提示框，让我们输入答案。

然后当我们点击确定时，如果输入了内容，则返回该响应。

否则，返回默认答案。

如果我们在第二个参数中省略了默认答案，并且没有输入任何内容，则返回`null`。

`prompt`是一个全局函数，所以`window.prompt`与`prompt`相同。

但我们只需写`prompt`即可。

## 变量命名

变量名不能以数字开头，但可以在中间包含数字。

例如，我们可以这样写：

```javascript
let name1 = "james";
```

但不能这样写：

```javascript
let 1name = "james";
```

JavaScript 变量命名还有更多规则。

变量名不能包含空格。

变量名只能包含字母、数字、美元符号和下划线。

变量名不能是 JavaScript 保留关键字，但可以包含它们。

可以使用大写字母，但必须注意变量名是区分大小写的。

所以`name`与`Name`不同。

JavaScript 变量名通常采用驼峰命名法。它们让我们可以形成由多个单词组成的变量，并且可以轻松阅读。

因此，我们可以编写像`firstName`这样的变量名，使变量名中的两个单词清晰明了。

## 数学表达式

大多数 JavaScript 程序都会进行数学运算。因此，JavaScript 提供了各种常见数学运算的运算符。

例如，我们可以使用`+`运算符进行加法：

```javascript
let num = 2 + 2;
```

要执行减法，可以使用`-`运算符：

```javascript
let num = 2 - 2;
```

乘法使用`*`运算符：

```javascript
let num = 2 * 2;
```

除法使用`/`运算符：

```javascript
let num = 2 / 2;
```

还有`%`取模运算符，用于求左操作数除以右操作数的余数。

例如，我们可以这样写：

```javascript
let num = 2 % 2;
```

我们得到 0，因为 2 可以被自身整除。

指数运算符用`**`表示。例如，我们可以这样使用它：

```javascript
let num = 2 ** 2;
```

这样将 2 提升到 2 次幂。

`++`运算符将变量的值加 1，并将结果赋给该变量。

例如：

```javascript
num++;
```

等同于：

```javascript
num = num + 1;
```

我们可以将表达式与赋值运算符一起使用，但可能会得到意想不到的结果。

例如，如果我们有：

```javascript
let num = 1;
let newNum = num++;
```

那么`newNum`是 1，因为返回的是`num`的原始值。

另一方面，如果我们有：

```javascript
let num = 1;
let newNum = ++num;
```

那么`newNum`是 2，因为如果`++`在`num`之前，则返回`num`的最新值。

同样，JavaScript 有`--`运算符，用于将变量减 1，并将最新值赋给该变量。

例如，我们可以这样写：

```javascript
let num = 1;
let newNum = num--;
```

对于`newNum`我们得到 1，而：

```javascript
let num = 1;
let newNum = --num;
```

则对于`newNum`我们得到 0。

值的返回方式与`++`相同。

## 控制小数位数

我们可以使用`toFixed`方法控制小数位数。

例如，如果我们有：

```javascript
let total = (8.8888).toFixed(2);
```

那么`total`是`'8.89'`。`toFixed`接受要四舍五入的位数，并返回一个包含四舍五入后数字的字符串。

如果小数以 5 结尾，通常向上舍入。

但某些浏览器可能会向下舍入。

## 获取当前日期和时间

要获取当前日期和时间，我们可以使用`new Date()`创建一个新的`Date`实例。

然后我们可以通过编写以下代码将`Date`实例转换为字符串：

```javascript
let now = new Date();
let dateString = now.toString();
```

要获取星期几，我们调用`getDay`方法：

```javascript
let now = new Date();
let day = now.getDay();
```

它返回一个从 0 到 6 的数字，其中 0 表示星期日，6 表示星期六。

如果我们想显示更易读的日期，可以这样写：

```javascript
let dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]
let now = new Date();
let day = now.getDay();
let dayName = dayNames[day];
```

我们可以使用`day`作为`dayNames`的索引来获取星期几的英文版本。

## 提取日期和时间的各个部分

`Date`实例提供了多种方法来获取日期和时间的各个部分。

`getMonth`返回日期中的月份，范围从 0 到 11，其中 0 表示一月，11 表示十二月。

`getDate`返回月份中的日期数字。

`getFullYear`返回四位数的年份。

`getHours`返回 0 到 23 之间的数字，对应午夜和晚上 11 点。

`getMinutes`返回小时中的分钟数，范围从 0 到 59。

`getSeconds`返回分钟中的秒数，范围从 0 到 59。

而`getMilliseconds`返回 0 到 999 之间的数字。

`getTime`返回自 1970 年 1 月 1 日午夜 UTC 以来经过的毫秒数。

我们可以从日期实例中调用所有这些方法。例如，我们可以这样写：

```javascript
let now = new Date();
let day = now.getMilliseconds();
```

## 指定日期和时间

我们可以使用`Date`构造函数来指定日期和时间。

要返回当前日期和时间，我们可以这样写：

```javascript
let today = new Date();
```

我们可以通过计算两个日期的时间戳差来得到天数差：

```javascript
let msToday = new Date().getTime();
let msAnotherDay = new Date(2029, 1, 1).getTime()
let msDiff = msAnotherDay - msToday;
```

然后，要得到天数差，我们可以这样写：

```javascript
let daysDiff = msDiff / (1000 * 60 * 60 * 24);
```

如果我们想将天数取整为整数，可以使用`Math.floor`向下取整：

```javascript
daysDiff = Math.floor(daysDiff);
```

## 更改日期和时间

`Date`实例允许我们更改日期和时间的各个部分。

`setFullYear`允许我们设置`Date`实例的年份。

`setMonth`允许我们设置`Date`实例的月份。它接受 0 到 11 之间的数字，其中 0 表示一月，11 表示十二月。

`setDate`允许我们设置月份中的日期。

`setHours`允许我们设置小时后的分钟数。

`setSeconds`允许我们设置分钟后的秒数。

而`setMilliseconds`允许我们设置秒后的毫秒数。

例如，我们可以通过以下方式调用`setFullYear`：

```javascript
let d = new Date();
d.setFullYear(2040);
```

或者：

```javascript
let d = new Date();
d.setMonth(11);
```

其余的方法可以以相同的方式调用。

## 函数

函数是可以重复使用以完成我们想要的操作的代码块。

我们之前调用过`setFullYear`、`setMonth`等函数。

它们可以接受零个或多个参数。

例如，我们可以通过以下方式创建自己的`tellTime`函数：

```javascript
function tellTime() {
  let now = new Date();
  let jr = now.getHours();
  let min = now.getMinutes();
  alert(`${hr}:${min}`);
}
```

我们调用了`getHours`来获取小时，`getMinutes`来获取分钟。

## 向函数传递数据

函数可以有参数，这样我们就可以向它们传递数据。

例如，我们可以这样写：

```javascript
function greetUser(greeting) {
  alert(greeting);
}
```

`greetUser`方法接受`greeting`参数，我们将该值用作`alert`函数的参数。

这样，我们就可以指定警告框的消息。

我们可以通过以下方式调用函数：

```javascript
greetUser('hello james');
```

现在我们应该会看到一个显示“hello james”文本的警告框。

我们可以用逗号分隔多个参数和实参。例如，我们可以这样写：

```javascript
function showMessage(greeting, name) {
  alert(`${greeting}, ${name}`);
}
```

`showMessage`函数有`greeting`和`name`参数。

然后我们可以通过以下方式调用`showMessage`：

```javascript
showMessage('hello', 'mary');
```

有了参数，我们可以自定义函数的调用方式。

## 在函数中返回数据

如果我们想获取函数计算出的数据，可以在函数中添加`return`语句来返回我们想要的数据。

例如，我们可以这样写：

```javascript
function getTotal(subtTotal, taxRate) {
  return subTotal * (1 + taxRate);
}
```

我们创建了`getTotal`函数，它接受`subTotal`和`taxRate`参数。

然后通过`return`语句返回计算结果。

我们可以通过以下方式调用`getTotal`函数：

```javascript
const total = getTotal(100, 0.05);
```

我们为`subTotal`和`taxRate`传入数字，并将返回值赋给`total`。

因此，`total`的值为 105。

## `do…while`循环

我们可以使用`do...while`循环来重复执行代码。

`do`块总是会执行，因此第一次迭代总是会运行。

例如，我们可以这样写：

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i <= 3);
```

`do`块总是会执行，因为`while`条件是在循环迭代完成后才进行检查的。

## 脚本标签

要在浏览器中运行 JavaScript 代码，我们需要在代码中添加脚本标签。

例如，我们可以这样写：



```html
<script>
  function sayHi() {
    alert("hi");
  }

  function sayBye() {
    alert("bye");
  }
</script>
```

我们在脚本标签中定义了`sayHi`和`sayBye`函数。

我们可以在脚本标签中放置任何 JavaScript 代码。

JavaScript 代码只是文本，因此我们可以轻松地将它们添加到 HTML 文件中，因为 HTML 文件也是文本。

如果脚本标签之间的代码很多，那么我们应该将它们移到单独的文件中。

例如，我们可以这样写：

```html
<script src="script.js"></script>
```

我们创建一个`script.js`文件，然后通过`src`属性引用它。

这样，我们就可以保持代码文件简短。

## 注释

我们可以在 JavaScript 代码中添加注释来解释代码的作用。

例如，我们可以这样写：

```javascript
// 这是一个注释
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

`//`表示注释的开始。浏览器会忽略它。

我们可以通过以下方式编写多行注释：

```javascript
/*
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas at volutpat ipsum, dapibus tincidunt nisl. Donec vestibulum ultricies laoreet. Suspendisse sit amet faucibus justo.
*/
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

我们有一个跨越多行的长注释。它由`/*`和`*/`分隔。

## 链接事件

当我们点击链接时，可以监听链接在点击等操作时发出的事件。

这对于在允许我们点击跳转到不同页面之外，还用于执行其他操作非常方便。

例如，我们可以这样写：

```html
<a href="#" onClick="alert('hello');">点击</a>
```

我们在`a`标签中添加了`onClick`属性，以便在其中运行 JavaScript 代码。

`onClick`不区分大小写。

`href='#'`告诉浏览器重新加载页面，这在我们希望点击链接时运行 JavaScript 代码的情况下可能不是我们想要的。

为了防止页面刷新，我们可以这样写：

```html
<a href="javaScript:void(0)" onClick="alert('hello');">点击</a>
```

我们添加了`javaScript:void(0)`代码来避免刷新。

如果我们想编写多条语句，可以这样写：

```html
<a href="javaScript:void(0)" onClick="let greeting='hi'; alert(greeting);">点击</a>
```

我们用分号分隔语句。

## 局部变量与全局变量

JavaScript 有局部变量和全局变量。

局部变量只能在块内访问。

而全局变量在整个应用程序中都可以使用。

在 JavaScript 中，我们使用`let`和`const`关键字创建局部变量。

它们都是块级作用域，因此只能在函数、`if`块等块内使用。

`let`创建变量，`const`创建常量。

常量在赋值后不能重新赋值。

但其内容可能仍然会改变。

常量在创建时必须赋予初始值。

例如，如果我们有：

```javascript
function addNumbers() {
  let theSum = 2 + 2;
}
```

`theSum`只能在`addNumbers`函数内使用。

但如果我们有：

```javascript
function addNumbers() {
  theSum = 2 + 2;
}
```

那么`theSum`就是一个全局变量。

我们可以在任何地方访问这个值。

如果一个变量是全局的，那么它就是`window`全局对象的一个附加属性。

我们应该避免使用全局变量，因为很容易创建同名的全局变量。

因此，很容易产生冲突。

而且很难追踪变量是如何被修改的。

## `switch`语句

`switch`语句让我们可以在一个语句中针对不同情况执行不同操作。

例如，我们可以这样写：

```javascript
switch (dayOfWk) {
  case "Sat":
    alert("very happy");
    break;
  case "Sun":
    alert("happy");
    break;
  case "Fri":
    alert("happy friday");
    break;
  default:
    alert("sad");
}
```

我们检查`dayOfWk`的值，当它具有给定值时，让我们执行不同的操作。

如果`dayOfWk`是`'Sat'`，则显示一个`'very happy'`的提示框。

如果`dayOfWk`是`'Sun'`，则显示一个`'happy'`的提示框。

如果`dayOfWk`是`'Fri'`，则显示一个`'happy friday'`的提示框。

当`dayOfWk`有其他任何值时，会执行`default`子句，并显示`'sad'`提示框。

`break`关键字是必需的，这样在找到匹配的`case`后，`switch`语句的其余部分就不会执行。

上面的`switch`语句等同于：

```javascript
if (dayOfWk === "Sat") {
  alert("very happy");
} else if (dayOfWk === "Sun") {
  alert("happy");
} else if (dayOfWk === "Fri") {
  alert("hapopy friday");
} else {
  alert("sad");
}
```

`switch`语句中的`default`等同于`if`语句中的`else`。

## `while`循环

JavaScript 的`while`循环是我们可以使用的另一种循环。

它允许我们在给定条件为`true`时运行循环。

例如，我们可以这样写：

```javascript
let i = 0;
while (i <= 3) {
  console.log(i);
  i++;
}
```

在上面的循环中，当`i`小于或等于 3 时，我们运行循环。

在循环体内，我们更新`i`，以便朝着结束循环的方向努力。

我们将循环块缩进 2 个空格，以便于输入和阅读。

## 按钮事件

我们可以为按钮添加事件处理代码，这样点击按钮时就能执行某些操作。

例如，我们可以这样写：

```html
<input type="button" value="Click Me" onClick="alert('Hello world!');">
```

我们有一个按钮，其`onClick`属性包含调用`alert`的 JavaScript 代码。

因此，当我们点击它时，会看到一个提示框显示出来。

`value`属性包含按钮文本。

我们也可以对其他元素做同样的事情。

例如，我们可以这样写：

```html
<a href="http://google.com"><img onClick="alert('Hello world!');" src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo"></a>
```

当我们点击图片时，会看到提示框显示出来。

如果我们想让代码更整洁，可以将`alert`调用放到一个单独的函数中。

我们可以编写以下 HTML：

```html
<a href="http://google.com"><img onClick="greet()" src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo"></a>
```

以及以下 JavaScript：

```javascript
const greet = () => {
  alert('Hello world!');
}
```

## 鼠标事件

我们可以通过使用属性并将其值设置为 JavaScript 代码来监听鼠标事件。

例如，我们可以这样写：

```html
<h1 onMouseover="alert('hello world.');">hello world</h1>
```

当鼠标悬停在 h1 元素上时，显示一个提示框。

我们还可以添加`onMouseout`事件处理程序，在鼠标悬停时执行某些操作，并在鼠标移开时恢复：

```html
<h1 onMouseover="this.style.color='green'" onMouseout="this.style.color='black'">hello world</h1>
```

上面代码中的`this`指的是 h1 元素。

当鼠标悬停在 h1 元素上时，我们将`color`样式设置为`'green'`。

然后当鼠标移开时，我们将`color`设置回黑色。

## 输入事件

同样，我们可以监听 input 元素发出的事件。

例如，我们可以这样写：

```html
<input type="text" size="30" onFocus="this.style.backgroundColor = 'yellow';" onBlur="this.style.backgroundColor = 'white';">
```

我们添加了`onFocus`和`onBlur`处理程序，当聚焦到 input 元素时，将`backgroundColor`样式设置为`'yellow'`。

然后当光标移出输入框时，背景恢复为白色。

## 读取字段值

我们可以在提交表单时读取输入字段中输入的值。

我们可以编写以下 HTML：

```html
<form onSubmit="checkAddress('email'); return false;">
  Email:
  <input type="text" id="email">
  <input type="submit" value="Submit">
</form>
```

以及以下 JavaScript 来检查 email 字段：

```javascript
const checkAddress = (fieldId) => {
  if (document.getElementById(fieldId).value === "") {
    alert("Email is required.");
  }
  return false;
}
```

`checkAddress`函数获取 ID 为`email`的输入框的值。

如果为空，我们会在提示框中看到`'Email is required'`消息。

我们需要在`onSubmit`属性和`checkAddress`函数中加上`return false`，以防止默认的提交行为。

我们可以通过以下方式简化函数：

```javascript
const checkAddress = (fieldId) => {
  const {
    value
  } = document.getElementById(fieldId)
  if (value === "") {
    alert("Email is required.");
  }
  return false;
}
```

## 设置字段值

我们可以使用 JavaScript 设置输入字段的值。

例如，我们可以编写以下 HTML：

```html
<form>
  fruit:<br>
  <input type="text" id="fruit" onBlur="fillColor();"><br>
  color:<br>
  <input type="text" id="color">
</form>
```

然后我们可以编写以下 JavaScript 代码：

```javascript
const fillColor = () => {
  let color;
  const {
    value
  } = document.getElementById("fruit");
  switch (value) {
    case "apple":
      color = "red";
      break;
    case "orange":
      color = "orange";
      break;
    case "grape":
      color = "purple";
  }
  document.getElementById("color").value = color;
}
```

我们在第一个输入框上添加了`onBlur`属性。

因此，当光标移出第一个输入框时，会调用`fillColor`函数。

然后我们通过`value`属性获取 ID 为`fruit`的输入框的值。

接着根据`value`的值设置`color`变量的值。

最后将 ID 为`color`的输入框的值设置为`color`变量的值。

## 读取和设置段落文本

我们可以读取和设置段落文本。

例如，我们可以编写以下 HTML：

```html
<p id="text">
  Lorem ipsum dolor sit amet.
  <a href="javascript:void(0);" onClick="expandText();">
    <em>Click for more.</em>
  </a>
</p>
```

然后我们可以添加`expandText`函数如下：

```javascript
const expandText = () => {
  const expandedParagraph = `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras id lorem eget erat vestibulum consectetur. Donec vehicula porta est ut vestibulum. Mauris et nisl a sem iaculis laoreet. Nunc eleifend facilisis massa ut luctus. Nullam sollicitudin non lorem non eleifend. Curabitur elementum felis quis enim malesuada varius.`;
  document.getElementById("text").innerHTML = expandedParagraph;
}
```

`a`元素具有`onClick`属性，其值设置为`expandText()`表达式。

因此，当我们点击“Click for more”文本时，会在屏幕上看到展开的文本。

这是因为我们将`expandedParagraph`变量的值设置为 ID 为`text`的元素的`innerHTML`属性的值。

我们可以通过设置`innerHTML`属性向元素中插入任何内容。

例如，我们可以保留现有的 HTML，并将 JavaScript 改为：

```javascript
const expandText = () => {
  const expandedParagraph = `
    <ol>
      <li>Slow</li>
      <li>Fast</li>
      <li>Just-right</li>
     </ol>
   `;
  document.getElementById("text").innerHTML = expandedParagraph;
}
```

我们将 ID 为`text`的元素的内容设置为一个有序列表。

因此，当我们点击“Click for more”时，就会看到这个列表。

## 操作图像和文本

我们可以使用 JavaScript 操作图像。

例如，我们可以编写以下 HTML：

```html
<img src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo" id="image" onClick="makeInvisible();">
```

然后我们可以添加以下 CSS：

```css
.hidden {
  visibility: hidden;
}
```

接着`makeInvisible`函数如下：

```javascript
const makeInvisible = () => {
  document.getElementById("image").className = "hidden";
}
```

`hidden`类将`visibility`属性设置为`hidden`。

因此，当我们点击图片时，会执行`makeInvisible`函数。

然后`hidden`类会被添加到`img`元素上。

于是图片就会隐藏。

## 添加类名

我们可以使用 JavaScript 的类名 API 为 HTML 元素添加类名。

例如，我们可以编写以下 HTML：

```html
<img src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo" id="image" onClick="expand();">
```

然后我们可以编写以下 CSS：

```css
.big {
  width: 500px;
}
```

接着我们可以通过编写以下代码来添加`expand`函数：



```javascript
const expand = () => {
  document.getElementById("image").classList.add('big');
}
```

`big` 类将宽度设置为 500px。

在 `expand` 函数中，我们调用 `classList.add` 方法，将 `'big'` 类添加到 ID 为 `image` 的元素上。

并且我们将 `onClick` 属性设置为 `expand()`，以便在点击图片时调用 `expand` 函数。

这样，当我们点击图片时，图片就会放大。

## 交换图片

我们可以在鼠标悬停时交换图片。

例如，我们可以编写以下 HTML：

```html
<img src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo" id="image" onMouseover="swap(1);" onMouseout="swap(0)">
```

以及以下 JavaScript 代码：

```javascript
const swap = (index) => {
  const images = [
    'https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo',
    'https://i.picsum.photos/id/25/200/300.jpg?hmac=ScdLbPfGd_kI3MUHvJUb12Fsg1meDQEaHY_mM613BVM'
  ]
  const image = document.querySelector('#image');
  image.src = images[index];
}
```

当我们悬停在图片上时，会执行 `swap(1)` 表达式。

它被设置为 `onMouseover` 属性的值，因此当我们悬停在图片元素上时就会执行。

如果我们将鼠标移出图片，则会执行 `swap(0)` 来显示原始图片。

这是因为 `swap(0)` 被设置为 `onMouseout` 属性的值。

## 设置样式

我们可以使用 `className` 或 `style` 属性来设置样式。

例如，我们可以编写以下 HTML：

```html
<p>
  hello world
</p>
```

并编写以下 CSS：

```css
.big {
  font-size: 2em
}
```

然后编写以下代码，用 JavaScript 将文本放大：

```javascript
document.querySelector("p").classList.add("big");
```

我们通过 `document.querySelector` 方法获取 `p` 元素。

然后通过 `classList.add` 方法将 `big` 类添加到 `p` 元素上。

或者，我们可以将 `style` 属性设置为我们想要的值：

```javascript
document.querySelector("p").style.fontSize = '2em'
```

`style.fontSize` 属性等同于 CSS 的 `font-size` 属性。

不过，最好使用 CSS 和类名，因为这样比用 JavaScript 设置样式更快。

此外，CSS 代码的可复用性也更高。

我们可以设置的其他 `style` 属性包括：

```javascript
document.querySelector("p").style.cssFloat = "left";
```

用于将 CSS 的 `float` 属性设置为 `left`。

我们可以通过编写以下代码来设置 CSS 的 `visibility` 属性：

```javascript
document.querySelector("p").style.visibility = "hidden";
```

而外边距可以通过编写以下代码来设置：

```javascript
document.querySelector("p").style.margin = "0 10px 0 10px;";
```

## 按标签名获取所有元素

我们可以通过标签名获取所有元素。

这比通过 ID 获取单个元素或使用 `querySelector` 获取第一个匹配选择器的元素更方便。

例如，我们可以编写以下 HTML：

```html
<p>foo.</p>
<p>bar.</p>
<p>baz.</p>
```

然后我们可以通过编写以下代码获取所有 `p` 元素并遍历它们：

```javascript
const pars = document.getElementsByTagName('p')
for (const p of pars) {
  p.style.fontFamily = "Verdana, Geneva, sans-serif";
}
```

我们获取 `p` 元素，然后使用 `for-of` 循环遍历它们。

在循环体中，我们设置 `fontFamily` 样式来改变文本的字体。

## 构造函数方法

我们可以向构造函数或类中添加方法。

例如，我们可以编写：

```javascript
class Plan {
  constructor(name, price, space, pages) {
    this.name = name;
    this.price = price;
    this.space = space;
    this.pages = pages;
  }

  calcAnnualPrice() {
    return this.price * 12;
  }
}
```

我们添加了 `calcAnnualPrice` 方法，用于返回 `this.price * 12` 的值。

`this` 是类的实例，即当我们调用 `Plan` 类时创建并返回的对象。

因此，我们从类创建的对象中获取 `price` 属性，并将其乘以 12。

要调用构造函数并在创建的对象上调用方法，我们可以编写：

```javascript
const plan = new Plan('basic', 3, 100, 10)
console.log(plan.calcAnnualPrice())
```

我们使用 `new` 关键字调用 `Plan` 构造函数。

然后我们在 `plan` 对象上调用 `calcAnnualPrice` 来获取年费。

类语法只是原型继承之上的语法糖。

`calcAnnualPrice` 方法只是 `Plan` 的 `prototype` 属性的一个属性。

`prototype` 是 `Plan` 类的原型，即它继承的对象。

如果我们打印 `Plan.prototype.calcAnnualPrice` 的值：

```javascript
console.log(Plan.prototype.calcAnnualPrice)
```

我们会看到 `calcAnnualPrice` 方法的代码被打印出来。

## 检查属性和方法

要检查某个属性或方法是否真正存在于对象本身而非其原型中，我们可以使用 `hasOwnProperty` 方法。

例如，如果我们从 `Plan` 类创建了一个对象：

```javascript
const plan = new Plan('basic', 3, 100, 10)
```

那么我们可以通过编写以下代码来调用 `hasOwnProperty`：

```javascript
console.log(plan.hasOwnProperty('name'))
```

我们应该会看到 `true` 被打印出来，因为 `name` 是 `plan` 对象自身的属性。

`hasOwnProperty` 方法来自 `Object.prototype`，这是几乎所有 JavaScript 对象都有的属性。

如果我们想列出对象的属性，可以编写：

```javascript
for (const prop in plan) {
  if (plan.hasOwnProperty(prop)) {
    console.log(prop);
  }
}
```

我们使用 `for-in` 循环遍历 `plan` 的属性键。

`for-in` 循环会遍历所有属性及其原型上的属性，因此我们必须使用 `hasOwnProperty` 方法来检查某个属性是否真正存在于 `plan` 对象本身。

`prop` 是属性名本身。

因此，我们应该看到：

```text
name
price
space
pages
```

被打印出来。

## 获取 URL

我们可以使用 JavaScript 获取和设置页面的 URL。

要获取 URL，我们可以使用 `window.location.href` 属性。

如果我们在浏览器开发者控制台中输入该属性，应该会得到页面的完整 URL。

`window.location.hostname` 包含主机名，即 URL 的第一部分。

例如，如果 URL 是 `"https://jsfiddle.net/09t6La27/10/"`，那么 `window.location.hostname` 返回 `"jsfiddle.net"`。

`window.location.hash` 返回 URL 中 `#` 符号之后的部分。

例如，如果 URL 是 `http://example.com/#foo`，那么 `window.location.hash` 返回 `"#foo"`。

## 对象

我们需要对象来存储除原始值（如数字、字符串、布尔值等）之外的值。

它作为我们想要存储的所有项目的容器。

例如，我们可以通过编写以下代码来定义一个对象：

```javascript
const plan = {
  name: "Basic",
  price: 3,
  space: 100,
  transfer: 1000,
  pages: 10
};
```

我们创建了带有多个属性的 `plan` 对象。

`name`、`price`、`space`、`transfer` 和 `pages` 是属性名。

冒号后面的表达式是它们的值。

属性之间用逗号分隔。

要访问一个属性，我们可以这样写：

```javascript
plan.name
```

`plan.name` 的值应为 `'Basic'`。

我们可以为属性赋予不同的值。

例如，我们可以这样写：

```javascript
plan.name = 'Deluxe';
```

那么 `name` 属性的新值就是 `'Deluxe'`。

我们可以使用赋值运算符为属性赋予任意数据类型的值。

要检查一个属性是否存在于对象中，可以使用 `in` 运算符。

例如，如果我们有：

```javascript
'name' in plan
```

那么它应该返回 `true`，因为 `name` 是 `plan` 的一个属性。

但如果我们有：

```javascript
'foo' in plan
```

那么它会返回 `false`，因为 `foo` 不是 `plan` 的属性。

我们需要将属性名用引号括起来，因为左操作数是一个字符串。

## 对象方法

对象可以拥有方法。

例如，我们可以这样写：

```javascript
const plan = {
  name: "Basic",
  price: 3,
  space: 100,
  transfer: 1000,
  pages: 10,
  calcAnnualPrice() {
    return this.price * 12;
  }
};
```

将 `calcAnnualPrice` 方法添加到 `plan` 对象中。

`this` 指向对象本身，因此 `this.price * 12` 返回 `price` 属性的值乘以 12 的结果。

## 构造函数

我们可以使用构造函数创建具有相同结构的对象。

它们是对象的模板。

要创建一个构造函数，我们可以这样写：

```javascript
function Plan(name, price, space, pages) {
  this.name = name;
  this.price = price;
  this.space = space;
  this.pages = pages;
}
```

我们创建了 `Plan` 构造函数，它接受 `name`、`price`、`space` 和 `pages` 参数。

然后我们将它们赋值给 `this` 的同名属性。

当我们调用构造函数时，`this` 会返回我们赋值的所有属性。

要调用它，我们可以这样写：

```javascript
const plan = new Plan('basic', 3, 100, 10)
```

我们使用 `new` 关键字来调用构造函数并创建对象。

`plan` 的值是：

```javascript
{
  name: "basic"
  pages: 10
  price: 3
  space: 100
}
```

编写构造函数的更好方式是使用类语法。

例如，我们可以这样写：

```javascript
class Plan {
  constructor(name, price, space, pages) {
    this.name = name;
    this.price = price;
    this.space = space;
    this.pages = pages;
  }
}
```

`constructor` 方法与我们之前使用的构造函数函数相同。

只是写法不同。这是创建构造函数的首选方式，因为它与其他流行的面向对象语言一致。

## 使用 `querySelectorAll` 按标签名定位所有元素

`document.querySelectorAll` 方法允许我们获取所有匹配给定选择器的元素。

因此，要获取所有具有给定标签名的元素，我们可以编写以下 HTML：

```html
<p>foo.</p>
<p>bar.</p>
<p>baz.</p>
```

然后我们可以通过以下代码获取所有元素并设置它们的样式：

```javascript
const pars = document.querySelectorAll('p')
for (const p of pars) {
  p.style.fontFamily = "Verdana, Geneva, sans-serif";
}
```

我们使用 `document.querySelectorAll` 获取所有 `p` 元素。

然后使用 `for-of` 循环遍历每个元素，并设置 `style.fontFamily` 属性来指定字体。

## 按标签名定位部分元素

我们可以使用 `document.querySelectorAll` 方法按标签名定位部分元素，因为它接受任何选择器字符串作为参数。

例如，如果我们有以下 HTML 表格：

```html
<table>
  <tr>
    <td>foo</td>
    <td>bar</td>
    <td>baz</td>
  </tr>
</table>
```

并且我们想要获取表格中的所有 `td` 元素，我们可以这样写：

```javascript
const tds = document.querySelectorAll('table td')
for (const t of tds) {
  t.style.backgroundColor = "pink";
}
```

我们使用 `table td` 选择器获取 `table` 元素内的 `td` 元素。

然后遍历 `td` 元素并将 `backgroundColor` 设置为 `'pink'`。

## DOM

DOM 代表文档对象模型（Document Object Model）。它是浏览器用 JavaScript 表示 HTML 元素的方式。

HTML 元素在 DOM 中以树形结构组织。

每个层级通过缩进表示。

例如，如果我们有：

```html
<html>

  <head>
    <title>
      Simple document
    </title>
  </head>

  <body>
    <p>
      hello world
    </p>
  </body>

</html>
```

那么 `html` 元素是树的根节点。

`head` 和 `body` 位于第二层。

`title` 和 `p` 元素位于第三层。

最顶层的元素是 `document` 对象。

因此，`html` 元素是 `head` 和 `body` 元素的父节点。

`title` 元素是 `head` 元素的子节点。

`p` 元素是 `body` 元素的子节点。

我们可以使用之前用过的 DOM 方法（如 `querySelector`、`querySelectorAll`、`getElementById` 和 `getElementByTagName`）来查找子元素。

例如，如果我们有以下 HTML：

```html
<html>

<head>
    <title>
      Simple document
    </title>
  </head>

  <body>
    <div id="weather">
      <p>Today is sunny.</p>
      <p>Yesterday is rainy.</p>
    </div>
    <div id="density">
      <p>City is crowded.</p>
      <p>Desert is sparse.</p>
    </div>
  </body>
</html>
```

那么如果我们想获取 "Today is sunny" 文本，可以这样写：

```javascript
const sunny = document.querySelector('#weather p');
console.log(sunny.innerHTML)
```

我们使用 `#weather p` 选择器与 `querySelector` 方法，从 ID 为 `weather` 的 div 中获取第一个 p 元素。

然后通过 `innerHTML` 属性获取其内容。

## 节点对象类型

节点类型有几种。

它们包括：

- `DOCUMENT_NODE` — `window.document`
- `ELEMENT_NODE` — body、a、p、h1 等
- `ATTRIBUTE_NODE` — `id='foo'`、`class='foo'`



- `TEXT_NODE` — 标签之间的文本
- `DOCUMENT_FRAGMENT_NODE` — 由 `document.createDocumentFragment()` 返回的任何内容
- `DOCUMENT_TYPE_NODE` — `<!doctype html>`

例如，我们可以写：

```javascript
document.ELEMENT_NODE
```

来获取 `ELEMENT_NODE` 的值，即 1。

`Node` 对象包含所有节点常量值。

从 `Node` 对象中，我们可以看到 `ELEMENT_NODE` 是 1。

`TEXT_NODE` 是 3，`ATTRIBUTE_NODE` 是 2，`DOCUMENT_NODE` 是 9，`DOCUMENT_FRAGMENT_NODE` 是 11，`DOCUMENT_TYPE_NODE` 是 10。

## 子节点对象

`HTMLElement` 对象通过 `Element` 对象继承自 `Node` 对象。

其他如 `Attr`、`Text`、`HTMLDocument` 和 `DocumentFragment` 都继承自 `Node`。

例如，我们可以写：

```javascript
const body = document.querySelector('body');
```

然后我们可以像这样遍历键：

```javascript
for (const key in body) {
  console.log(key);
}
```

除了 `HTMLElement` 的属性外，我们还应该看到节点属性。

## 节点的属性和方法

每个节点都有以下属性：

- `childNodes`
- `firstChild`
- `lastChild`
- `nextSibling`
- `nodeName`
- `nodeType`
- `nodeValue`
- `parentNode`
- `previousSibling`

它们允许我们在不同节点之间遍历。

`childNodes` 包含子节点。

`firstChild` 包含第一个子节点。

`lastChild` 包含最后一个子节点。

`nextSibling` 包含下一个兄弟节点。

`nodeName` 包含节点的名称。

`nodeType` 包含节点的类型。

`parentNode` 包含当前节点的父节点。

`previousSibling` 包含当前节点的上一个兄弟节点。

方法包括：

- `appendChild()`
- `cloneNode()`
- `compareDocumentPosition()`
- `contains()`
- `hasChildNodes()`
- `insertBefore()`
- `isEqualNode()`
- `removeChild()`
- `replaceChild()`

`appendChild` 添加一个新的子节点。

`cloneNode` 克隆当前节点并返回它。

`compareDocumentPosition` 比较每个节点的位置。

`contains` 检查节点是否包含另一个节点作为子节点。

`insertBefore` 在当前节点之前添加一个节点。

`isEqualNode` 检查是否相等。

`removeChild` 移除一个给定的子节点。

`replaceChild` 用一个子元素替换另一个子元素。

文档方法包括：

- `document.createElement()`
- `document.createTextNode()`

`createElement` 顾名思义会创建一个新元素，`createTextNode` 则创建一个可放入元素的文本节点。

HTML 元素属性包括：

- `innerHTML`
- `outerHTML`
- `textContent`
- `innerText`
- `outerText`
- `firstElementChild`
- `lastElementChild`
- `nextElementChild`
- `previousElementChild`
- `children`

`innerHTML` 包含元素内部的 HTML 内容。

`outerHTML` 除了包含 `innerHTML` 的所有 HTML 内容外，还包含外层标签。

`textContent` 包含元素内部的文本内容。

`innerText` 包含元素内部的文本内容。

`outerText` 包含 `innerText` 的内容以及外层标签。

`firstElementChild` 是第一个为 HTML 元素的子节点。

`lastElementChild` 是最后一个为 HTML 元素的子节点。

`nextElementChild` 是当前节点之后的下一个元素节点。

`previousElementChild` 是当前节点之前的元素节点。

`children` 是当前节点的子节点。

HTML 元素对象拥有 `insertAdjacentHTML` 方法，用于根据指定位置插入节点。

## 识别节点的类型和名称

我们可以通过 `nodeType` 属性识别类型，通过 `nodeName` 识别名称。

例如，`document.nodeName` 返回 `'#document'`，`document.nodeType` 返回 9，表示它是一个 `DOCUMENT_NODE`。

## 获取节点的值

对于大多数类型的节点，`nodeValue` 属性返回 `null`。

但我们可以用它从 `Text` 和 `Comment` 节点中提取文本。

例如，如果我们有以下代码：

```html
<a>hi</a>
```

那么：

```javascript
console.log(document.querySelector('a').firstChild.nodeValue);
```

会输出 `'hi'`。

## DocumentFragment

`DocumentFragment` 是一种节点类型，它提供了一个轻量级的文档 DOM，独立于活动 DOM 树之外。

它是一个文档模板，行为类似于真实 DOM，但存在于内存中。

它的子节点可以轻松地在内存中操作，并追加到活动 DOM 中。

## 创建 DocumentFragment

`createDocumentFragment` 方法允许我们创建文档片段。

例如，我们可以这样写：

```javascript
const frag = document.createDocumentFragment();
for (const s of ['foo', 'bar', 'baz']) {
  const p = document.createElement("p");
  p.textContent = s;
  frag.appendChild(p);
}
```

我们使用 `createDocumentFragment` 创建了一个文档片段。

然后遍历字符串数组，创建 `p` 元素，并将它们作为子元素追加到片段中。

创建文档片段的好处是我们可以将其存储在内存中。

它可以包含除 `body` 或 `html` 之外的任何类型的节点。

当我们追加片段时，片段本身不会添加到 DOM 中。

只有其中的节点会被添加。

当文档片段被追加到 DOM 时，它会从文档转移到被追加的位置。

它会被从内存中移除。

而元素则始终存在于内存中。

## 将 DocumentFragment 添加到 DOM

我们可以将文档片段传递给另一个元素的 `appendChild` 和 `insertBefore` 方法。

例如，我们可以通过以下代码将前面示例中的内容追加到 body：

```javascript
const frag = document.createDocumentFragment();
for (const s of ['foo', 'bar', 'baz']) {
  const p = document.createElement("p");
  p.textContent = s;
  frag.appendChild(p);
}
document.body.appendChild(frag);
```

现在我们将创建的 `p` 元素添加到了 body 中。

## 在 DocumentFragment 上使用 innerHTML

我们可以使用 `innerHTML` 通过字符串设置片段的内容。

例如，我们可以这样创建一个文档片段：

```javascript
const frag = document.createDocumentFragment();
const div = document.createElement('div');
frag.appendChild(div);
frag.querySelector('div').innerHTML = '<p>foo</p><p>bar</p>';
document.body.appendChild(frag);
```

我们使用 `createFragment` 创建了一个片段。然后创建一个 `div` 来容纳内容。

接着用我们自己的 HTML 设置 `div` 的内容。

最后，使用 `appendChild` 将片段内容追加到 body。

## 将包含节点的片段保留在内存中

如果我们想保留片段的内容，可以克隆它。

例如，如果我们有以下片段：

```javascript
const frag = document.createDocumentFragment();
for (const s of ['foo', 'bar', 'baz']) {
  const p = document.createElement("p");
  p.textContent = s;
  frag.appendChild(p);
}
```

我们可以通过以下代码克隆它：

```javascript
document.body.appendChild(frag.cloneNode(true));
```

这样我们在将文档片段内容追加到 body 的同时，保留了它。

## CSS 样式表

我们可以通过使用 `link` 标签向页面添加样式。

此外，我们还可以向文档添加 `style` 标签或 `style` 属性。

每个添加到 HTML 文档的样式表都由 `CSSStyleSheet` 对象表示。

如果我们有一个 `style` 元素：

```html
<style>
  body {
    background-color: green;
  }
</style>
```

我们可以通过 JavaScript 获取样式表，代码如下：

```javascript
console.log(document.querySelector('style').sheet);
```

我们会得到一个包含样式表的对象。

## 访问所有样式表

我们可以使用 `styleSheets` 属性获取所有样式表。

例如，如果我们有以下 CSS：

```html
<!doctype html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <style>
      body {
        background-color: #fff;
      }
    </style>
  </head>
  <body>
  </body>
</html>
```

那么我们可以通过以下方式获取样式表：

```javascript
console.log(document.styleSheets);
```

我们也可以像下面这样使用 `link` 元素的 `sheet` 属性：

```javascript
console.log(document.querySelector('link').sheet);
```

## CSSStyleSheet 的属性和方法

`CSSStyleSheet` 拥有属性和方法。

它们包括：

- `disabled` — 指示样式表是否被禁用
- `href` — `href` 属性的值
- `media` — 样式信息的目标媒体
- `ownerNode` — 将样式表与文档关联的节点
- `parentStylesheet` — 父样式表
- `title` — `title` 属性的值
- `type` — `type` 属性的值
- `cssRules` — 一个类数组对象，用于保存组成样式表的规则
- `ownerRule` — 保存导入样式表的 import 规则
- `deleteRule` — 从样式表对象中移除规则的方法
- `insertRule` — 向样式表插入规则的方法

## 将 NodeList 或 HTMLCollection 转换为数组

要将 `NodeList` 或 `HTMLCollection` 转换为数组，我们可以使用展开运算符或 `Array.from` 方法。

我们可以这样写：

```javascript
const arr = [...document.querySelectorAll('p')];
```

或者这样写：

```javascript
const arr = Array.from(document.querySelectorAll('p'));
```

现在我们可以对 `NodeList` 或 `HTMLCollection` 对象使用我们想要的数组方法，比如 `map`、`filter`、`pop`、`push` 等。

## 遍历 DOM 中的节点

我们可以使用各种属性遍历 DOM 中的节点。

这些属性包括：

- `parentNode`
- `firstChild`
- `lastChild`
- `nextSibling`
- `previousSibling`

`parentNode` 包含当前节点的父节点。

`firstChild` 包含当前节点的第一个子节点。

`lastChild` 包含最后一个子节点。

`nextSibling` 包含当前节点之后紧邻的节点。

`previousSibling` 包含当前节点之前紧邻的节点。

要遍历 DOM 但忽略文本和注释节点，我们可以使用以下属性：

- `firstElementChild`
- `lastElementChild`
- `nextElementSibling`
- `previousElementSibling`
- `children`

`firstElementChild` 包含当前元素的第一个子元素。

`lastElementChild` 包含当前元素的最后一个子元素。

`nextElementChild` 包含当前元素之后紧邻的兄弟元素。

`previousElementSibling` 表示当前元素的前一个兄弟元素。

`children` 表示当前元素的子元素。

例如，我们可以使用：

```javascript
document.body.children
```

来获取 body 元素的所有子节点。

## 检查节点在 DOM 树中的位置

我们可以使用 `contains` 方法来检查一个元素是否位于另一个元素内部。

例如，我们可以这样写：

```javascript
const isInside = document.querySelector('html').contains(document.querySelector('body'));
```

这将返回 `true`，因为 `body` 始终位于 `html` 元素内部。

`compareDocumentPosition` 返回一个数字，表示所比较元素之间的相对位置。

返回值为 0 表示元素相同。

1 表示节点不在同一文档中。

2 表示该节点位于所选节点之前。

3 表示该节点位于所选节点之后。

8 表示传入的节点是所选节点的祖先。

16 或十六进制的 10 表示传入的节点是所选节点的后代。

一个节点可能与另一个节点存在多种关系。

在这种情况下，这些数字会被相加后返回。

给定以下 HTML：

```html
<div id='foo'>
  <p>
    foo
  </p>
  <p>
    bar
  </p>
</div>
```

我们可以这样使用它：

```javascript
const div = document.querySelector('div');
const p = document.querySelector('p');
const result = div.compareDocumentPosition(p);
console.log(result);
```

我们得到 20，因为一个节点包含并位于另一个节点之前，这意味着 16 + 4 等于 20。

## HTMLElement

`HTMLElement` 是一个构造函数，用于创建表示 HTML 文档中节点的对象。

它包含以下子构造函数：

- `HTMLHtmlElement`
- `HTMLHeadElement`
- `HTMLLinkElement`
- `HTMLTitleElement`
- `HTMLMetaElement`

以及更多。

它们代表页面上的各种元素。

## HTMLElement 对象的属性和方法

`HTMLElement` 实例有许多属性和方法供我们操作。

我们可以使用 `createElement` 来创建元素。

使用 `tagName` 获取标签名。

使用 `children` 获取子元素。

使用 `getAttributes` 获取子属性。

使用 `setAttribute` 设置属性。

使用 `hasAttribute` 检查元素是否存在。

使用 `removeAttribute` 移除属性。

`classList` 是一个用于操作类集合的对象。

`dataset` 返回所有以 `data-` 开头的属性。



`attributes`包含属性列表。

完整列表请参见[`developer.mozilla.org/en-US/docs/Web/API/element`](https://developer.mozilla.org/en-US/docs/Web/API/element)。

## 创建元素

我们可以使用`createElement`方法创建元素。

例如，我们可以通过以下代码创建一个输入框：

```javascript
const input = document.createElement('input');
document.body.appendChild(input);
```

然后我们会在屏幕上看到一个输入元素。

## 获取元素的标签名

`tagName`属性返回元素的名称。

它返回的值与`nodeName`相同。

标签名会以大写形式返回。

例如，如果我们有：

```html
<a href="http://example.com">hello</a>
```

那么：

```javascript
console.log(document.querySelector('a').tagName);
```

会输出`'A'`。

## 获取元素属性的列表或集合

`attributes`属性返回元素当前已定义的属性节点集合。

如果我们有：

```html
<a href="http://example.com" title="example" data-foo="dataFoo" class="example">hello</a>
```

那么我们可以通过以下代码将所有节点放入数组：

```javascript
const attrs = [...document.querySelector('a').attributes];
```

我们使用展开运算符将类数组对象转换为数组。

返回的属性是动态的，意味着内容可以随时更改。

`attributes`实际返回的对象是`NameNodeMap`，它是一个类数组对象。

它有一个`length`属性。

布尔属性会出现在`attributes`列表中，但没有值。

## 获取、设置和移除元素的属性值

我们可以使用`getAttribute()`、`setAttribute()`和`removeAttribute()`方法来操作属性。

例如，如果我们有：

```html
<a href="http://example.com" title="example" data-foo="dataFoo" class="example">hello</a>
```

那么我们可以调用：

```javascript
const a = document.querySelector('a');
a.removeAttribute('href');
```

来移除`href`属性。

我们也可以这样写：

```javascript
a.setAttribute('href', '#');
```

来设置`href`属性。

## 验证元素是否具有特定属性

要检查元素是否具有特定属性，我们可以使用`hasAttribute`方法。

例如，如果我们有：

```html
<a href='http://example.com' title="example" data-foo='bar' class="example"></a>
```

那么我们可以通过以下代码检查它是否具有给定属性：

```javascript
const a = document.querySelector('a');
a.hasAttribute('title');
```

如果属性存在（无论是否有值），该方法将返回`true`。

## 获取类属性值的列表

我们可以使用`classList`属性来获取类属性的值。

例如，如果我们有：

```html
<div class="foo bar baz"></div>
```

我们可以通过以下代码获取类名：

```javascript
const div = document.querySelector('div');
console.log(div.classList);
```

这将在一个类数组对象中分别返回每个类名。

还有`className`属性可以将它们全部以字符串形式返回：

```javascript
console.log(div.className);
```

## 在 class 属性中添加和删除子值

`classList`对象有一个`add`方法用于向类属性添加类名。

它也有`remove`方法用于移除类名。

例如，如果我们有：

```html
<div class="foo"></div>​
```

那么我们可以这样写：

```javascript
const div = document.querySelector('div');
div.classList.add('bar');
```

来将`bar`与`foo`一起添加。

以及：

```javascript
div.classList.remove('foo');
```

来移除`foo`，并在类属性中保留`bar`。

## 切换类属性值

`classList`还有一个`toggle`方法用于切换类名。

例如，如果我们有：

```html
<div class="foo"></div>​
```

那么我们可以这样写：

```javascript
const div = document.querySelector('div');
div.classList.toggle('foo');
```

来关闭它，然后再次调用`toggle`并传入相同的类名可以重新添加它。

## 检查两个节点是否相同

我们可以根据 DOM 3 规范检查两个节点是否相同。根据规范，两个节点被视为相同，必须满足以下条件：两个节点类型相同。

`nodeName`、`localName`、`namespaceURI`、`prefix`和`nodeValue`必须具有相同的值。

`NameNodeMaps`属性必须相等。`children`NodeList也必须相等。

规范化可能会影响`children`中的条目，因此在比较之前应进行规范化。

`isEqualNode`方法可以为我们完成所有检查。

例如，如果我们有：

```html
<div id='foo'>
  <p>
    foo
  </p>
  <p>
    bar
  </p>
</div>
```

我们可以这样写：

```javascript
const p = document.querySelectorAll('div > p')
console.log(p[0].isEqualNode(p[1]));
```

来检查两个 p 元素是否相同。

它们不相同，因为内容不同，所以输出`false`。

如果我们有：

```html
<div id='foo'>
  <p>
    foo
  </p>
  <p>
    foo
  </p>
</div>
```

那么相同的代码会输出`true`，因为 p 元素相同。

## 文档节点

`HTMLDocument`构造函数继承自`document`，表示一个特定的文档节点。

## 文档属性和方法

`HTMLDocument`实例的属性和方法包括以下内容：

- `doctype`
- `documentElement`
- `implementation`
- `activeElement`
- `body`
- `head`
- `title`
- `lastModified`
- `referrer`
- `URL`
- `defaultview`
- `compatMode`
- `ownerDocument`
- `hasFocus()`

`doctype`包含文档的文档类型。

`documentElement`包含整个文档。

## 文档对象属性

- `implementation`包含`DOMImpkementation`对象，该对象提供一些不依赖于特定文档的方法。
- `activeElement`包含当前激活的元素。
- `body`包含文档的 body 元素。
- `title`包含`title`元素。
- `lastModified`包含最后修改日期。
- `referrer`包含链接到当前页面的 URL。
- `URL`是当前页面的 URL。
- `defaultView`指向与文档关联的`window`对象。
- `compatMode`指示文档处于怪异模式还是标准模式。
- `ownerDocument`包含节点的顶层文档对象。
- `hasFocus`返回元素是否获得焦点。

### 获取常规 HTML 文档信息

我们可以通过编写以下代码来获取文档的常规信息：

```javascript
const {
  title,
  URL,
  referrer,
  lastModified,
  compatMode
} = document;console.log(
  title,
  URL,
  referrer,
  lastModified,
  compatMode
)
```

我们从`document`对象本身获取常规信息。

### document 的子节点

`document`可以包含一个`DocumentType`节点对象和一个`Element`节点对象。

对于大多数文档，`DocumentType`应为`<!doctype html>`。

子元素应为`html`元素本身。

我们可以使用`document.childNodes`来获取这些元素。

### 访问 DOCTYPE、html、head 和 body 的快捷方式

`document`对象具有直接获取这些节点的属性。

`document.doctype`指向`<!doctype html>`。

`document.documentElement`指向`<html>`元素。

`document.head`指向`<head>`，而`document.body`指向`<body>`。

### 检测 DOM 规范或特性

`document.implement.hasFeatures`方法允许我们检查 DOM API 是否支持某个特性。

例如，我们可以编写：

```javascript
document.implementation.hasFeature('Core','3.0');
```

来检查浏览器是否实现了 DOM Core 3.0 规范。

支持以下特性：

- Core — 支持版本 1.0、2.0 和 3.0
- XML — 1.0、2.0、3.0
- HTML — 1.0、2.0
- Views — 2.0
- StyleSheets — 2.0
- CSS — 2.0
- CSS2–2.0
- Events — 2.0、3.0
- UIEvents — 2.0、3.0
- MouseEvents — 2.0、3.0
- MutationEvents — 2.0、3.0
- HTMLEvents — 2.0
- Range — 2.0
- Traversal — 2.0
- Validation — 3.0

我们不应依赖`hasFeature`来检测特性。

`isSupported`也可以对支持节点进行相同的检查，同时检查支持的特性：

```javascript
element.isSupported(feature, version)
```

其中`element`是我们想要检查的特定元素。

### 获取焦点/活动节点的引用

我们可以使用`document.activeElement`属性来获取当前获得焦点的元素。

### 检查文档或其内部任何节点是否获得焦点

我们可以调用`document.hasFocus()`方法来检查页面内是否有任何元素获得焦点。

### document.defaultview

`document.defaultview`是浏览器中全局 JavaScript 对象的快捷方式。

这意味着`document.defaultView`就是浏览器中的`window`对象。

### 检查类属性值是否包含特定值

我们可以使用`classList.contains`方法来检查某个类名是否存在于类属性的类名列表中。

例如，如果我们有以下代码：

```html
<div class="foo bar baz"></div>​
```

那么我们可以编写：

```javascript
const div = document.querySelector('div');
console.log(elm.classList.contains('foo'));
```

它会输出`true`，因为`foo`存在于类属性中。

### 获取和设置 data- 属性

我们可以使用`dataset`属性来设置任何以`data-`开头的属性。

例如，如果我们有以下代码：

```html
<div data-foo-bar='foo'></div>​
```

那么我们可以编写：

```javascript
const div = document.querySelector('div');
console.log(elm.dataset.fooBar);
```

来返回`data-foo-bar`的值。

HTML 中的连字符命名（kebab case）会被转换为驼峰命名（camelCase）。

要设置它，我们可以编写：

```javascript
elm.dataset.baz = 'baz'
```

这样就会在 div 上添加一个值为`baz`的`data-baz`属性。

### 选择特定的元素节点

获取单个元素节点引用最常用的方法是`querySelector`或`getElementById`。

`querySelector`用于通过任意 CSS 选择器获取单个元素。

例如，我们可以编写：

```javascript
const div = document.querySelector('div');
```

来获取页面上的第一个 div。

我们可以使用`getElementById`来获取设置了`id`属性的元素。

例如，如果我们有以下代码：

```html
<p id='foo'>foo</p>
```

那么我们可以通过编写以下代码来使用`getElementById`获取该 p 元素：

```javascript
const foo = document.getElementById('foo');
```

### 选择或创建元素节点的 NodeList

我们可以使用`querySelectorAll`、`getElementsByTagName`或`getElementsByClassName`来分别获取具有给定选择器、标签名或类名的多个元素。

例如，如果我们有以下代码：

```html
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

那么我们可以使用`querySelectorAll`来获取所有 li 元素，编写如下：

```javascript
const lis = document.querySelectorAll('li');
```

要使用`getElementsByTagName`实现相同功能，我们编写：

```javascript
const lis = document.getElementsByTagName('li');
```

此外，我们还可以使用`getElementsByClassName`来获取相同的元素，如下所示：

```javascript
const lis = document.getElementsByTagName('item');
```

由`getElementsByTagName`和`getElementsByClassName`创建的`NodeList`始终是动态的（live）。

这意味着即使文档被更新，它们也始终反映文档的当前状态。

`querySelectorAll`不会返回动态的元素列表。

它返回的是创建时文档的快照。

所有这些方法也定义在元素节点上。

因此我们可以链式调用它们。

例如，我们可以编写：

```javascript
const lis = document.getElementById('list').getElementsByTagName('li');
```

我们可以将`'*'`传递给`querySelectorAll`或`getElementsByTagName`来获取页面上的所有元素。

`childNodes`也会返回一个`NodeList`。

### 选择所有直接子元素节点

我们可以使用`children`来选择给定节点的所有子节点。

如果我们有以下代码：

```html
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

那么我们可以通过编写以下代码来获取 li 元素：

```javascript
const lis = document.querySelector('ul').children;
```

`children`返回所有直接元素节点，不包括其他类型的节点。

它们按照在 DOM 中出现的顺序返回。

### 上下文元素选择

我们可以在元素节点上调用`querySelector()`、`querySelectorAll()`、`getElementsByTagName()`和`getElementsByClassName()`。

例如，如果我们有以下代码：

```html
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

我们可以编写：

```javascript
const lis = document.querySelector('ul').getElementsByTagName('li');
```

来获取 li 元素。

### 预配置的选择/元素节点列表

`document`对象中有许多属性可以直接返回选定的节点，而无需调用上述方法。



`document.all` 返回 HTML 文档中的所有元素。

`document.forms` 返回 HTML 文档中的所有表单元素。

`document.images` 返回文档中的所有 `img` 元素。

`document.links` 返回文档中的所有 `a` 元素。

`document.scripts` 返回文档中的所有 `script` 元素。

`document.styleSheets` 返回 HTML 文档中的所有 `link` 和 `style` 对象。

它们返回 `HTMLCollection` 对象，因此是动态的。

`document.all` 由 `HTMLAllCollection` 构造函数创建，在 Firefox 中不受支持。

### 使用 `matches()` 验证元素是否会被选中

我们可以使用 `matches()` 来检查元素的 CSS 选择器是否与给定的选择器匹配。

例如，如果我们有以下代码：

```html
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

我们可以通过编写以下代码来调用它：

```javascript
console.log(document.querySelector('.item').matches('li:first-child'));
```

它应返回 `true`，因为第一个带有类 `item` 的元素与 `li` 相同。

### 创建元素和文本节点

有两种方法可以让我们创建节点。一种是 `createElement()`，用于创建元素节点。还有 `createTextNode()` 方法，用于创建文本节点。

我们可以使用 `createAttribute()` 方法创建属性，使用 `createComment()` 创建注释。

要创建一个元素，我们可以这样写：

```javascript
const elementNode = document.createElement('div');
```

然后我们创建了一个 `div`。

要创建一个文本节点，我们这样写：

```javascript
const textNode = document.createTextNode('hello');
```

### 使用 JavaScript 字符串创建并添加元素和文本节点

我们可以通过将 `innerHTML` 属性设置为一个字符串来添加节点。

例如，我们可以这样写：

```javascript
document.getElementById('foo').innerHTML = '<strong>foo</strong>';
```

将节点放入以下 `div` 中：

```html
<div id="foo"></div>
```

我们有一个 ID 为 `foo` 的 `div`。

设置 `innerHTML` 属性会创建 `strong` 元素节点并将其放入 `div` 中。

要替换外层节点，我们可以这样写：

```javascript
document.getElementById('foo').outerText = 'foo';
```

将 `div` 替换为文本节点 `'foo'`。

`insertAdjacentHTML()` 方法仅适用于元素节点。它比设置 `innerHTML` 或创建新节点更精确。

例如，如果我们有以下 HTML：

```html
<div id="foo">
  <p>
    foo
  </p>
</div>
```

我们可以这样写：

```javascript
const foo = document.getElementById('foo');
foo.insertAdjacentHTML('beforebegin', '<p>bar</p>');
```

然后我们在包含文本 `foo` 的 `p` 元素之前添加一个 `p` 标签。第一个参数是位置，第二个参数是内容。

其他位置包括 `'afterbegin'`、`'beforeend'` 和 `'afterend'`。

`innerHTML` 会将字符串中的 HTML 元素转换为实际的 DOM 节点。

`textContent` 只能构造文本节点。

### 将 DOM 树的部分提取为 JavaScript 字符串

`innerHTML`、`outerHTML` 和 `textContent` 是我们用来创建和添加节点的工具。

我们也可以使用它们来获取内容。

例如，如果我们有：

```html
<div id="foo">
  <p>
    foo
  </p>
</div>
```

那么我们可以这样写：

```javascript
console.log(document.getElementById('foo').innerHTML);
```

来获取 `div` 的内容。

`innerText` 会给我们文本节点。例如，我们可以这样写：

```javascript
console.log(document.getElementById('foo').innerText);
```

来获取 `foo`。

### 将节点对象添加到 DOM

`appendChild()` 和 `insertBefore()` 可用于将节点对象添加到 DOM。

`appendChild()` 用于向给定元素添加子元素。

`insertBefore()` 允许我们在当前元素之前添加一个元素。

例如，我们可以这样使用 `appendChild()`：

```javascript
const elementNode = document.createElement('p');
elementNode.innerText = 'hello';
document.getElementById('foo').appendChild(elementNode);
```

假设我们有以下 HTML：

```html
<div id="foo">
  foo
</div>
```

我们在文本 `foo` 之后添加了一个新节点作为子节点。

`insertBefore()` 接受两个参数。第一个是要插入的元素。

第二个是我们希望在其之前插入第一个参数中节点的元素。

我们插入之前的节点必须是调用 `insertBefore()` 的节点的子节点。

因此，给定以下 HTML：

```html
<div id="foo">
  <p>
    foo
  </p>
</div>
```

我们可以通过以下方式在 `p` 元素之前插入一个元素：

```javascript
const elementNode = document.createElement('p');
elementNode.innerText = 'hello';
const foo = document.getElementById('foo');
foo.insertBefore(elementNode, foo.firstChild);
```

我们创建了一个 `p` 元素，然后将其传递给 `insertBefore()` 方法。

`foo.firstChild` 是 `p` 元素，因为父 `div` 是 `foo`。

然后我们在 `foo` 之前显示 `hello`。

### 使用 `removeChild()` 移除节点

要移除子元素，我们可以使用 `removeChild()` 方法。

例如，给定以下 HTML：

```html
<div id="foo">
  <p>
    foo
  </p>
</div>
```

我们可以这样写：

```javascript
const p = document.querySelector('p');
p.parentNode.removeChild(p);
```

从 `div` 中移除 `p` 元素。

我们获取要移除元素的直接父元素，然后移除目标元素。

### 使用 `replaceChild()` 替换子元素

`replaceChild()` 方法的工作方式与 `removeChild()` 类似。我们获取父元素，然后调用 `replaceChild()` 来替换项目。

例如，如果我们有：

```html
<div id="foo">
  <p>
    foo
  </p>
</div>
```

我们可以这样写：

```javascript
const p = document.querySelector('p');
const bar = document.createTextNode('bar');
p.parentNode.replaceChild(bar, p);
```

将 `p` 元素替换为包含 `bar` 的文本节点。

第一个参数是我们想要用来替换现有节点的新节点。

第二个参数是我们要替换的原始节点。

### 获取元素的 `offsetTop` 和 `offsetLeft` 值

`offsetTop` 和 `offsetLeft` 用于获取元素节点相对于 `offsetParent` 的像素值。

这些元素节点属性给出了从 `offsetParent` 左上边框外部到内部左上边框的像素距离。

`offsetParent` 是通过搜索最近的、CSS 位置不为 `static` 的祖先元素来确定的。

如果未找到，则使用 `body` 位置作为 `offsetParent` 的值。

例如，如果我们在 `body` 内有一个 `div`：

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <div></div>
  </body>
</html>
```

那么我们可以通过以下方式获取 `div` 的位置：

```javascript
const div = document.querySelector('div');
console.log(div.offsetLeft);
console.log(div.offsetTop);
console.log(div.offsetParent);
```

我们得到 `body` 作为 `offsetParent`，其他属性得到数值。

### 获取元素的上、右、下、左边框边缘

`getBoundingClientRect()` 方法获取元素外部边框边缘相对于视口顶部和左侧的位置。

例如，如果我们有：

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <div></div>
  </body>
</html>
```

我们这样写：

```javascript
const rect = document.querySelector('div').getBoundingClientRect();
console.log(rect);
```

然后我们得到 `top`、`left`、`right` 和 `bottom` 属性，其尺寸以像素为单位，相对于视口。

### 获取元素在视口中的大小

`getBoundingClientRect()` 方法还返回 `height` 和 `width` 属性。

例如，如果我们有：

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <div></div>
  </body>
</html>
```

我们这样写：

```javascript
const rect = document.querySelector('div').getBoundingClientRect();
console.log(rect);
```

我们得到 `height` 和 `width` 属性，它们包含总高度和宽度，包括内边距和边框。

### 获取元素在视口中的大小（排除边框）

`clientHeight` 和 `clientWidth` 包含元素的大小，不包括边框。

但内边距和内容包含在内。

如果我们有：

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <div></div>
  </body>
</html>
```

我们可以这样写：

```javascript
const div = document.querySelector('div');
console.log(div.clientHeight, div.clientWidth);
```

### 获取视口中特定点的最顶层元素

`elementFromPoint()` 获取 HTML 文档中特定点的最顶层元素的引用。

例如，如果我们有：

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <div></div>
  </body>
</html>
```

那么我们可以这样使用它：

```javascript
console.log(document.elementFromPoint(10, 12));
```

我们得到 `html` 元素。

### 使用 `scrollHeight` 和 `scrollWidth` 获取正在滚动的元素的大小

`scrollHeight` 和 `scrollWidth` 给出了正在滚动的节点的高度和宽度。

例如，如果我们有一个滚动 `html` 元素的 HTML，那么我们会得到正在滚动的 `html` 元素的大小。

如果我们有以下代码：

```html
<p></p>
```

以及：

```css
p {
  height: 1000px;
  width: 1000px;
  background-color: green;
}
```

那么，通过编写以下代码，我们可以获取正在滚动的 `p` 元素的宽度：

```javascript
const p = document.querySelector('p');

console.log(p.scrollHeight, p.scrollWidth);
```

并且每个属性都会返回 1000。

### 获取和设置从顶部和左侧滚动的像素数

`scrollTop` 和 `scrollLeft` 是读写属性，它们返回由于滚动而在可滚动视口中当前不可见的左侧或顶部的像素数。

例如，如果我们有以下代码：

```html
<p></p>
```

以及：

```css
p {
  height: 1000px;
  width: 1000px;
  background-color: green;
}
```

那么我们可以通过编写以下代码来设置它们：

```javascript
const p = document.querySelector('p');
p.scrollTop = 750;
p.scrollLeft = 750;
```

然后，当我们记录这些值时，应该会看到这些数值。

### 将元素滚动到视图中

我们可以调用 `scrollIntoView()` 方法将元素滚动到视图中。

例如，如果我们有以下代码：

```javascript
for (let i = 0; i < 50; i++) {
  const p = document.createElement('p');
  p.innerText = i;
  document.body.appendChild(p);
}
```

生成 50 个 `p` 元素并将它们附加到 `body`，然后通过编写以下代码将第 41 个元素滚动到视图中：

```javascript
document.querySelectorAll('p')[40].scrollIntoView(true);
```

### 样式属性

DOM 节点对象具有 `style` 属性，用于设置我们选择的元素的样式。

它也会返回元素的样式。

例如，如果我们有以下代码：

```html
<div></div>
```

那么我们可以通过编写以下代码来获取样式：

```javascript
const styles = document.querySelector('div').style;
```

然后 `styles` 将包含所有样式。

### 获取、设置和移除内联 CSS 属性

我们可以使用 `style` 属性来设置 CSS 样式。

例如，如果我们有一个 `div`：

```html
<div></div>
```

我们可以编写：

```javascript
const divStyle = document.querySelector('div').style;
divStyle.backgroundColor = 'yellow';
divStyle.border = '1px solid green';
divStyle.width = '200px';
divStyle.height = '200px';
```

然后我们会得到一个带有绿色边框的黄色盒子，高度和宽度各为 200px。

在 CSS 中为 `kebab-case` 的属性在 JavaScript 中会转换为 `camelCase`。

例如，如果在 CSS 中有 `background-color`，那么在 JavaScript 中就是 `backgroundColor`。

这适用于所有多词属性。

我们也可以使用 `setProperty()` 方法来设置样式，使用 `getPropertyValue()` 来获取样式。

例如，我们可以用以下代码重写上面的代码：

```javascript
const divStyle = document.querySelector('div').style;
divStyle.setProperty('background-color', 'yellow');
divStyle.setProperty('border', '1px solid green');
divStyle.setProperty('height', '200px');
divStyle.setProperty('width', '200px');
```

这里我们调用 `setProperty()` 而不是直接设置 `style` 属性。

要获取样式，我们可以使用 `getPropertyValue()` 方法：

```javascript
console.log(divStyle.getPropertyValue('background-color'));
```

### 获取、设置和移除所有内联 CSS 属性

我们可以使用 `getAttribute()` 和 `setAttribute()` 来获取或设置所有 CSS 属性。

例如，我们可以编写：

```javascript
const div = document.querySelector('div');
div.setAttribute('style', 'background-color: yellow; height: 200px; width: 200px');
```

然后通过设置 `div` 的 `style` 属性，在字符串中设置所有样式。



要获取样式，我们可以使用`getAttribute()``，如下：

```javascript
console.log(div.getAttribute('style'));
```

### 获取元素的计算样式

我们可以使用`getComputedStyle()`获取元素的所有样式。

它包括所有样式，包括内联样式、来自样式表的样式以及`style`标签中的样式。

例如，如果我们有以下代码：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <style>
      div {
        background-color: green;
        border: 1px solid yellow;
        height: 150px;
        width: 150px;
      }
    </style>
  </head>

  <body>
    <div style="background-color:orange;"></div>
  </body>
</html>
```

我们可以这样使用它：

```javascript
const div = document.querySelector('div');
console.log(window.getComputedStyle(div).backgroundColor);
```

内联样式会覆盖其他样式，因此它会返回`rgb(255, 165, 0)`，即橙色。

对于颜色，它总是返回`rgb`格式。

### 使用 class 和 id 属性应用和移除 CSS 属性

我们可以将样式放在 ID 或类 CSS 选择器中，并使用它们来应用样式。

例如，如果我们有一个`div`：

```html
<div></div>
```

以及一些 CSS：

```css
.foo{
  background-color: green;
  width: 100px;
  height: 100px;
}

#bar{
  border:10px solid red;
  width: 100px;
  height: 100px;
}
```

我们可以编写：

```javascript
const div = document.querySelector('div');
div.setAttribute('id','bar');
```

然后我们会得到一个带有红色边框的盒子。

我们可以通过编写以下代码将`foo`类添加到`div`：

```javascript
const div = document.querySelector('div');
div.classList.add('foo');
```

然后盒子将添加绿色背景色。

### 文本节点

HTML 文档中的文本节点是`Text`构造函数的实例。

它们返回文本节点。

例如，如果我们有以下代码：

```html
<p>hello</p>
```

那么我们可以通过以下方式获取`p`元素内部的文本：

```javascript
const hello = document.querySelector('p').firstChild;
```

### 文本对象和属性

`Text`实例具有各种对象和属性。

它们具有以下属性和方法：

- `textContent` — 文本节点的内容
- `splitText()` — 按指定的偏移量将文本拆分为两个节点
- `appendData()` — 向节点追加数据
- `deleteData()` — 从节点删除数据
- `insertData()` — 在所需位置向节点添加数据
- `replaceData()` — 替换给定位置的数据
- `subStringData()` — 从文本节点中提取部分文本
- `normalize()` — 将节点和子节点规范化为标准形式。这意味着移除空节点
- `data` — 返回节点的数据
- `createTextNode()` — 创建一个新的文本节点

### 空白会创建文本节点

空白会创建文本节点。

如果它们是空的，那么字符串中会包含空格。

例如，如果我们有以下代码：

```html
<p> </p>
```

然后我们编写：

```javascript
document.querySelector('p').firstChild.nodeName
```

然后我们会得到`#text`，表明它是一个文本节点。

### 向元素节点添加事件监听器

我们可以使用`addEventListener()`向元素节点添加事件监听器。

例如，我们可以编写：

```javascript
window.addEventListener('mousemove', (e) => {
  console.log(e.clientX, e.clientY);
}, false);
```

来监听`mousemove`事件，并在鼠标移动时记录鼠标坐标。

同样的操作也可以应用于元素。如果我们有以下代码：

```html
<button>
  click me
</button>
```

那么我们可以编写：

```javascript
const button = document.querySelector('button');

button.addEventListener('click', () => {
  console.log('clicked');
}, false);
```

来监听按钮的点击事件。

### 移除事件监听器

如果原始监听器是一个命名函数，我们可以使用`removeEventListener()`来移除事件监听器。

例如，如果我们有以下代码：

```html
<button>
  click me
</button>
```

那么我们可以编写：

```javascript
const button = document.querySelector('button');

const listener = () => {
  console.log('clicked');
  button.removeEventListener('click', listener);
}

button.addEventListener('click', listener, false);
```

这样只在第一次点击时记录`'clicked'`。

这是因为我们在第一次调用监听器后，对`button`的`click`事件调用了`removeEventListener()`来移除该监听器。

### 从事件对象获取事件属性

我们可以从事件对象中获取事件属性。

它是监听器的第一个参数。

例如，我们可以编写：

```javascript
window.addEventListener('load', (event) => {
  console.log(event);
});
```

来记录`event`对象，该对象具有各种属性。

它有许多属性，以及`stopPropagation()`、`stopImmediatePropagation()`和`preventDefault()`方法。

`stopPropagation()`会阻止事件传播到所有祖先元素。

`stopImmediatePropagation`阻止同一事件的其他监听器被调用。

`preventDefault`阻止元素的默认行为被执行。

### addEventListener 中 this 的值

我们传递给`addEventListener`的事件监听器函数中，`this`的值指向事件所附加到的节点或对象的引用。

这仅适用于传统函数。

例如，如果我们有一个按钮：

```html
<button>
  click me
</button>
```

那么如果我们编写：

```javascript
const button = document.querySelector('button');

button.addEventListener('click', function(event) {
  console.log(this);
});
```

`this`将指向注册了该监听器的按钮。

我们可以使用`event.currentTarget`来获取相同的引用。

它比`this`更可靠，因为箭头函数也能使用它。

### 引用事件的目标

我们可以使用`event.target`属性来获取作为事件目标的元素。

这可能与调用事件的节点不同。

例如，我们可以编写：

```javascript
document.body.addEventListener('click', (event) => {
  console.log(event.target);
}, false);
```

来获取被点击的元素。

### 取消浏览器默认事件

我们可以使用`preventDefault`来取消浏览器默认事件。

例如，我们可以通过此方法阻止链接的默认行为。

如果我们有以下 HTML：

```html
<a href="http://example.com">don't go</a>
```

那么我们可以通过编写以下代码来阻止用户点击链接时跳转到[`example.com`](http://example.com)：

```javascript
document.querySelector('a').addEventListener('click', (event) => {
  event.preventDefault();
}, false);
```

点击链接时它将不会执行任何操作。

`preventDefault`不会阻止事件在冒泡或捕获阶段传播。

在事件监听器函数体末尾添加`return false`与`preventDefault`效果相同。

事件对象具有`cancelable`属性，用于指示事件是否会对`preventDefault`做出响应。

### 停止事件流

要阻止事件流向祖先元素或反向流动，我们可以使用`stopPropagation`方法。

例如，我们可以编写：

```javascript
const button = document.querySelector('button')

button.addEventListener('click', (e) => {
  e.stopPropagation();
}, false);
```

来阻止事件从起源元素向祖先元素传播。

### 停止事件流及同一目标上的其他同类事件

`stopImmediatePropagation`会停止事件流阶段，以及事件目标上在该事件监听器之后附加的任何其他同类事件。

例如，我们可以编写：

```javascript
const button = document.querySelector('button')

button.addEventListener('click', (e) => {
  e.stopImmediatePropagation();
}, false);
```

那么如果我们有：

```javascript
const button = document.querySelector('button')

button.addEventListener('click', (e) => {
  e.stopImmediatePropagation();
}, false);

document.querySelector('button').addEventListener('click', () => {
  //...
}, false);

document.body.addEventListener('click', () => {
  //...
}, false);
```

第一个监听器之后的所有监听器都不会被调用，因为我们在第一个监听器中调用了`stopImmediatePropagation`。

### DOM 事件类型

我们可以监听的事件种类繁多。

以下是用户事件：

- `load` — 当某内容加载完成时触发
- `unload` — 当用户代理移除资源时触发
- `abort` — 当资源在加载完成前停止加载时触发
- `error` — 当某内容加载失败时触发
- `resize` — 当文档视图大小改变时触发
- `scroll` — 当用户滚动时触发
- `contextmenu` — 通过右键点击元素触发

以下是焦点事件：

- `blur` — 当元素失去焦点时触发（通过点击其他地方或按 Tab 键）
- `focus` — 当元素获得焦点时触发
- `focusin` — 当事件目标即将获得焦点但在焦点转移之前触发
- `focusout` — 当事件目标即将失去焦点时触发

表单事件包括：

- `change` — 当控件失去输入焦点时触发
- `reset` — 当表单重置时触发
- `submit` — 当表单提交时触发
- `select` — 当用户在字段中选择一些文本时触发

鼠标事件包括：

- `click` — 当鼠标指针点击元素时触发
- `dblclick` — 当鼠标指针双击元素时触发
- `mousedown` — 当鼠标指针在元素上按下时触发
- `mouseenter` — 当鼠标指针移入元素时触发
- `mouseleave` — 当鼠标指针移出元素及其所有子元素的边界时触发
- `mousemove` — 当鼠标指针在元素上移动时触发
- `mouseup` — 当鼠标指针在元素上释放时触发
- `mouseover` — 当鼠标指针移过元素时触发

滚轮事件包括：

- `wheel` — 当鼠标滚轮旋转时触发

键盘事件包括：

- `keydown` — 当按键最初被按下时触发
- `keypress` — 当按键最初被按下时触发
- `keyup` — 当按键被释放时触发

触摸事件包括：

- `touchstart` — 指示用户将触摸点放在触摸表面上时触发
- `touchend` — 指示用户从触摸表面移除触摸点时触发
- `touchmove` — 当用户沿触摸表面移动触摸点时触发
- `touchenter` — 当触摸点移入 DOM 元素定义的交互区域时触发
- `touchleave` — 指示触摸点移出 DOM 元素定义的区域时触发
- `touchcancel` — 当触摸点被中断时触发

窗口/主体事件包括：

- `afterprint` — 当打印完成后触发
- `beforeprint` — 在打印之前触发
- `beforeunload` — 在文档卸载之前触发
- `hashchange` — 当 URL 中`#`后面的部分发生变化时触发
- `message` — 当用户向 worker 发送消息时触发
- `offline` — 当浏览器离线时触发
- `online` — 当浏览器在线时触发
- `pagehide` — 当从会话历史记录条目中遍历时触发
- `pageshow` — 当从会话历史记录条目中进入时触发

文档事件包括：

- `readystatechange` — 当就绪状态改变时触发
- `DOMContentLoaded` — 当网页加载完成但所有资源尚未下载时触发

拖拽事件包括：

- `drag` — 当源对象被拖拽时触发
- `dragstart` — 当源对象开始被拖拽时触发
- `dragend` — 当用户释放被拖拽对象上的鼠标时在源对象上触发
- `dragenter` — 当被拖拽元素进入放置目标时触发
- `dragleave` — 当对象移出放置目标时触发
- `dragover` — 当对象被拖拽经过放置目标时触发
- `drop` — 当对象被放置时触发

### 事件流

事件在 DOM 中传播。

它们从起源元素一直传播到根元素对象。这被称为冒泡阶段。

因此，当我们在祖先对象上注册监听器时，它们也会运行。

还有捕获阶段，它与冒泡阶段相反。

### 自定义事件

我们可以在 JavaScript 代码中触发自定义事件。

为此，我们可以使用`createEvent`方法，然后使用`addEventListener`来监听该事件。

例如，如果我们有一个按钮：

```html
<button>
  click me
</button>
```

我们可以编写：

```javascript
const button = document.querySelector('button');
const customEvent = document.createEvent('CustomEvent');
button.addEventListener('hello', (event) => {
  console.log(event.detail.foo)
}, false);

customEvent.initCustomEvent('hello', true, false, {
  foo: 'bar'
});

button.dispatchEvent(customEvent);
```

我们调用`createEvent`来创建一个自定义事件。传入`'CustomEvent'`以创建自定义事件。

然后调用`initCustomEvent`用数据初始化该自定义事件。

接着，调用`dispatchEvent`来触发该事件。

随后，在传入`addEventListener`的事件处理函数中，我们记录`detail`属性中的数据。

因此，当我们访问`foo`属性时，得到`'bar'`。

### 模拟或触发鼠标事件

我们可以使用`initMouseEvent`方法来触发鼠标事件。

例如，如果我们有以下代码：

```html
<button>
  点击我
</button>
```

我们可以这样写：



```javascript
const button = document.querySelector('button');
button.addEventListener('click', (event) => {
  console.log(event);
}, false);

const simulatedClick = document.createEvent('MouseEvents');

simulatedClick.initMouseEvent('click', true, true, document.defaultView, 0, 0, 0, 0, 0, false, false, false, 0, null, null);

button.dispatchEvent(simulatedClick);
```

我们调用`createEvent`并传入`'MouseEvents'`。

然后调用`initMouse`事件，它接受多个参数。

这些参数按以下顺序排列：

- `type` — 要触发的鼠标事件类型
- `canBubble` — 指示事件是否冒泡
- `cancelable` — 指示事件是否可取消
- `view` — 事件的抽象视图，应为`window`
- `detail` — 点击次数
- `screenX` — 事件的屏幕 x 坐标
- `screenY` — 事件的屏幕 y 坐标
- `clientX` — 事件客户区的 x 坐标
- `clientY` — 事件客户区的 y 坐标
- `ctrlKey` — 事件期间是否按下了 Ctrl 键
- `altKey` — 事件期间是否按下了 Alt 键
- `shiftKey` — 事件期间是否按下了 Shift 键
- `metaKey` — 事件期间是否按下了 meta（Windows / Command）键
- `button` — 鼠标按钮
- `relatedTarget` — 相关事件目标

这是一个已弃用的 API，因此应考虑其他解决方案。

### 事件委托

我们可以使用一个事件处理函数来监听来自不同源的事件。

例如，如果我们有以下代码：

```html
<button>
  按钮 1
</button>
<button>
  按钮 2
</button>
<button>
  按钮 3
</button>
```

我们可以这样写：

```javascript
document.addEventListener('click', (event) => {
  if (event.target.tagName.toLowerCase() === 'button') {
    console.log(event.target.textContent);
  }
}, false);
```

我们通过`document.addEventListener`监听整个页面上的点击事件。

然后通过`event.target`获取事件起源的元素。

如果点击了一个按钮，则记录其文本内容。

### CSSStyleRule 概述

`CSSStyleRule`对象表示样式表中的每条 CSS 规则。

它是与选择器关联的 CSS 属性和值的接口。

要访问它们，如果我们有以下代码：

```html
<style id='styles'>
  body {
    background-color: orange;
    margin: 20px;
  }

  p {
    font-weight: 20px;
    color: blue;
  }
</style>
```

那么我们可以这样写：

```javascript
const styles = document.querySelector('#styles');
console.dir(styles.sheet.cssRules);
```

以从`style`元素中获取 CSS 规则。

### CSSStyleRule 的属性和方法

`CSSStyleRule`拥有自己的属性和方法。

它具有以下属性：

- `cssText` — CSS 规则的文本
- `parentRule` — 给定样式块的父规则
- `parentStylesSheet` — 父样式表对象
- `selectorText` — 规则的选择器
- `style` — 规则的样式
- `type` — 规则的类型，即 CSS 规则，值为 1

例如，我们可以这样写：

```javascript
const styles = document.querySelector('#styles');
console.dir(styles.sheet.cssRules[0].cssText);
```

然后我们得到 body 元素的样式，因为它是第一个条目。

### 获取样式表中的 CSS 规则列表

`cssRules`包含样式表的 CSS 规则列表。

例如，如果我们有与前一个示例相同的 style 元素，我们可以这样写：

```javascript
const styles = document.querySelector('#styles');
console.dir(styles.sheet.cssRules);
```

以获取所有`cssRules`。

### 插入或删除 CSS 规则

`insertRule`允许我们在样式表中插入一条 CSS 规则。

`deleteRule`允许我们删除它们。

例如，如果我们有一个 style 元素：

```html
<style id='styles'>
  body {
    background-color: orange;
    margin: 20px;
  }

  p {
    font-weight: 20px;
    color: blue;
  }
</style>
```

我们可以这样写：

```javascript
const styles = document.querySelector('#styles');
styles.sheet.insertRule('p { color:green }', 1);
```

然后我们为 p 标签添加了一条新的 CSS 规则，该规则会被现有规则覆盖。

我们可以通过以下方式删除旧规则：

```javascript
styles.sheet.deleteRule(1);
```

现在我们的新规则成为页面上 p 元素的规则。

我们只需传入要删除的规则的索引即可。

### 编辑 CSSStyleRule 的值

我们可以为`style`属性赋值来更改样式值。

例如，如果我们有以下代码：

```html
<style id='styles'>
  body {
    background-color: orange;
    margin: 20px;
  }

  p {
    font-weight: 20px;
    color: blue;
  }
</style>
<p>
  foo
</p>
```

我们可以这样写：

```javascript
const styles = document.querySelector('#styles');
styles.sheet.cssRules[1].style.color = 'green';
```

将 p 元素的颜色设置为绿色。

### 创建新的内联 CSS 样式表

我们可以使用`innerHTML`属性向 style 元素添加新样式。

例如，如果我们有以下代码：

```javascript
const style = document.createElement('style');
style.innerHTML = 'body { color: orange }';document.querySelector('head').appendChild(style);
```

现在 body 的所有内容都将变为橙色，因为我们添加了包含该样式的 style 元素。

### 以编程方式添加外部样式表

以编程方式添加外部样式表的方法与添加 style 标签类似。

为此，我们只需使用`createElement`：

```javascript
const link = document.createElement('link');
link.setAttribute('rel', 'stylesheet');
link.setAttribute('type', 'text/css');
link.setAttribute('id', 'link');
link.setAttribute('href', 'https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css');
```

我们添加了一个包含 Bootstrap 样式表的新 link 元素。

### 禁用或启用样式表

`disabled`属性是我们可以设置在样式表上以切换样式表开启或关闭的属性。

如果我们有一个 link 元素：

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
```

那么我们可以通过以下方式切换：

```javascript
document.querySelector('link').disabled = true;
```

现在禁用了它。要启用，我们可以写：

```javascript
document.querySelector('link').disabled = false;
```

### 插入并运行 JavaScript

我们可以将 JavaScript 插入到 HTML 文档中。

JavaScript 代码始终位于 script 标签内，可以是外部文件或内联代码。

script 元素没有必需的属性。

也应避免使用自闭合 script 标签。

尝试包含一个操作页面上 script 元素的外部脚本文件会导致页面上的 script 被忽略。

例如，我们可以这样写：

```html
<script>
console.log('hello');
</script>
```

以包含一个 script 标签。

### JavaScript 同步加载

加载脚本的默认选项是同步加载。

这意味着如果存在其他脚本，它们会阻塞渲染和下载。

如果脚本是外部文档，并且阻塞了其他所有内容的加载，那么必须先下载脚本才能解析，这意味着速度会更慢。

### 打开弹出窗口

我们可以使用`window.open`方法打开弹出窗口。

例如，我们可以这样写：

```javascript
const monkeyWindow = window.open();
```

要向窗口添加一些内容，我们可以写：

```javascript
const monkeyWindow = window.open();
const windowContent = `<h1>hello world</h1>`;
monkeyWindow.document.write(windowContent);
```

我们在`monkeyWindow`上调用`document.write`来显示内容。

此外，我们还可以使用`location.assign`方法显示某个 URL 的内容：

```javascript
const monkeyWindow = window.open();
monkeyWindow.location.assign("https://www.google.com");
```

现在我们应该能看到新窗口中显示了 Google 页面。

我们也可以这样写：

```javascript
const monkeyWindow = window.open();
monkeyWindow.location.href = "https://www.google.com";
```

来实现同样的效果。

要关闭窗口，我们可以这样写：

```javascript
const monkeyWindow = window.open();
monkeyWindow.location.href = "https://www.google.com";
monkeyWindow.close();
```

## 控制窗口的大小和位置

我们可以通过`window.open`的第三个参数中的字符串来设置弹出窗口的大小和位置。

例如，我们可以这样写：

```javascript
const monkeyWindow = window.open("https://www.google.com", "win1", "width=420,height=380");
```

现在窗口的宽度为 420px，高度为 380px。

要改变它的位置，我们可以这样写：

```javascript
const monkeyWindow = window.open("https://www.google.com", "win1", "width=420,height=380,left=200,top=100");
```

通过添加`left`和`top`键来设置位置。

## 表单验证

我们可以为表单添加表单验证。

例如，我们可以编写以下 HTML：

```html
<form onSubmit="return checkForLastName();">
  Please enter your last name.<br>
  <input type="text" id="lastNameField">
  <input type="submit" value="Submit">
</form>
```

然后添加以下 JavaScript 来实现验证：

```javascript
const checkForLastName = () => {
  if (document.getElementById("lastNameField").value.length === 0) {
    alert("Please enter your last name");
    return false;
  }
}
```

在`checkForLastName`函数中，我们获取 ID 为`lastNameField`的输入框的值。

如果`value`的`length`为 0，则弹出提示。

`onSubmit`属性值中的`return`确保我们阻止了默认的提交行为，同时`checkForLastName`中的`return false`也起到了同样的作用，这样我们就可以运行 JavaScript 验证。

为了改善用户体验，我们可以在元素上调用`focus`：

```javascript
const checkForLastName = () => {
  const lastNameField = document.getElementById("lastNameField")
  if (lastNameField.value.length === 0) {
    alert("Please enter your last name");
    lastNameField.focus();
    return false;
  }
}
```

我们在输入元素上调用`focus`，这样用户无需点击输入框即可直接输入文本。

此外，我们还可以添加背景颜色，让用户更容易看到输入框：

```javascript
const checkForLastName = () => {
  const lastNameField = document.getElementById("lastNameField")
  if (lastNameField.value.length === 0) {
    alert("Please enter your last name");
    lastNameField.focus();
    lastNameField.style.background = "yellow";
    return false;
  }
  lastNameField.style.background = "white";
}
```

我们通过设置`lastNameField.style.background`属性来设置背景颜色。

### 下拉菜单验证

我们可以为选择下拉菜单字段添加验证。

例如，我们可以编写以下 HTML：

```html
<form onSubmit="return checkForSelection();">
  <select id="fruits">
    <option value="" selected="selected">
      SELECT A FRUIT</option>
    <option value="apple">apple</option>
    <option value="orange">orange</option>
    <option value="grape">grape</option>
  </select>
  <br>
  <input type="submit" value="Submit Form">
</form>
```

然后添加以下 JavaScript：

```javascript
const checkForSelection = () => {
  if (document.getElementById("fruits").selectedIndex === 0) {
    alert("Please select a fruit.");
    return false;
  }
}
```

我们添加了一个 select 元素，当点击“Submit Form”时，会运行`checkForSelection`函数。

我们添加了`return`关键字，以便阻止默认的提交行为，并让`checkForSelection`运行。

### 单选按钮验证

此外，我们还可以为一组单选按钮添加验证。

例如，我们可以编写以下 HTML：



```html
<form onSubmit="return validateRadios();">
  <input type="radio" name="r1" value="apple"> apple<br>
  <input type="radio" name="r1" value="orange"> orange<br>
  <input type="radio" name="r1" value="grape"> grape<br>
  <input type="submit" value="Submit Form">
</form>
```

以及以下 JavaScript：

```javascript
const validateRadios = () => {
  const radios = document.getElementsByName("r1");
  for (const r of radios) {
    if (r.checked) {
      return true;
    }
  }
  alert("Please check one.");
  return false;
}
```

我们有一个表单，其中包含一组具有相同 `name` 属性值的单选按钮。

它们应该具有相同的名称，这样它们才会被视为同一组。

当我们点击“Submit Form”按钮时，`validateRadios` 函数会运行。

在函数中，我们通过调用 `getElementsByName` 并传入单选按钮的 `name` 属性值来获取所有单选按钮。

我们使用 `for-of` 循环遍历这些单选按钮。

如果其中一个被选中，则返回 `true`。

否则，弹出提示，如果没有任何一个被选中，则返回 `false`。

### 电子邮件验证

我们可以通过使用正则表达式检查输入文本的格式来验证表单字段中的电子邮件地址。

例如，我们可以编写以下 HTML：

```html
<form onSubmit="return validateEmail();">
  Please enter your email.<br>
  <input type="text" id="emailField">
  <input type="submit" value="Submit">
</form>
```

并编写以下 JavaScript 代码：

```javascript
const validateEmail = () => {
  const emailField = document.getElementById("emailField");
  const regex = /^[w-.+]+@[a-zA-Z0-9\. -]+.[a-zA-z0-9]{2,4}$/;
  if (!(regex.test(emailField.value))) {
    alert("Please correct email address");
    return false;
  }
}
```

我们有一个 `validateEmail` 函数，它获取 ID 为 `emailField` 的输入框的值。

然后我们调用 `regex.test` 方法来检查输入的值是否匹配正则表达式格式。

如果不匹配，则弹出提示并返回 `false`。

`return` 关键字让我们阻止默认的提交行为。

## 处理事件

我们可以为 HTML 元素附加事件监听器。

例如，我们可以编写以下 HTML：

```html
<input type="button" value="Click" id='button1'>
```

并编写以下 JavaScript：

```javascript
const b1 = document.getElementById("button1");
const sayHello = () => {
  alert('hello');
}
b1.onclick = sayHello;
```

我们通过 `getElementById` 获取按钮。

然后将 `onclick` 属性设置为 `sayHello` 事件处理函数。

该函数通过 `alert` 函数显示一个提示框。

现在当我们点击按钮时，就会显示提示框。

# jQuery

jQuery 是一个流行的 JavaScript 库，用于创建动态网页。

在本节中，我们将了解如何在我们的 Web 应用中使用 jQuery。

## 添加 jQuery

我们可以通过添加一个 script 标签来添加 jQuery：

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```

我们也可以通过运行以下命令来安装 `jquery` 包：

```bash
npm install jquery
```

使用 NPM，或者：

```bash
yarn add jquery
```

此外，我们还可以使用 Bower 安装它：

```bash
bower install jquery
```

安装完成后，我们就可以开始使用它了。

## `.add()`

`.add()` 方法允许我们从父元素中获取子元素。

例如，如果我们有以下代码：

```html
<p>
  <div>
    foo
  </div>
</p>
```

那么我们可以调用：

```javascript
$("p").add("div").addClass("widget");
```

来获取 `p` 元素内部的 `div`。

然后我们调用 `addClass` 来为 `p` 元素内部的 `div` 添加一个类。

## `.addBack()`

`.addBack()` 方法允许我们从父元素中获取子元素。

例如，如果我们有以下 HTML：

```html
<div class="after-addback">
  <p>First Paragraph</p>
  <p>Second Paragraph</p>
</div>
```

以及以下 CSS：

```css
.background {
  background: yellow;
}
```

那么我们可以获取 `div` 中的 `p` 元素。

然后使用 `addBack` 再次获取 `div`。

最后，我们调用 `addClass` 来添加 `background` 类。

## `.addClass()`

`.addClass()` 方法允许我们向一个元素添加一个或多个类。

例如，我们可以这样写：

```javascript
$("p").addClass("myClass yourClass");
```

来向 `p` 元素添加 `myClass` 和 `yourClass` 类。

## `.after()`

`.after()` 方法在匹配元素集合中的每个元素之后插入内容。

例如，如果我们有以下 HTML：

```html
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

那么我们可以获取带有 `inner` 类的元素，并通过以下代码向它添加 HTML：

```javascript
$(".inner").after("<p>Test</p>");
```

## `.ajaxComplete()`

`.ajaxComplete()` 允许我们添加一个回调函数，该函数在 Ajax 请求完成时被调用。

例如，我们可以这样写：

```javascript
$(document).ajaxComplete(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

我们调用了 `ajaxComplete`，并传入一个回调函数，该函数在使用 `$.ajax` 发起请求时被调用。

然后我们调用 `$.ajax` 来发起 Ajax 请求。

`settings` 包含 `url` 属性，即请求的 URL。

`settings.type` 属性包含请求方法名称。

`xhr` 包含 XHR 对象。`readyState` 属性包含就绪状态。

## `.ajaxError()`

`.ajaxError()` 方法允许我们添加一个回调函数，该函数在发生错误时被调用。

例如，我们可以这样使用它：

```javascript
$(document).ajaxError(function(event, xhr, settings, thrownError) {
  console.log(event, xhr, settings, thrownError)
});

$.ajax({
  url: "bad-url",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

我们将一个无效的 URL 设置为 `url` 属性的值。

然后 `ajaxError` 回调函数会被调用。

它包含 `thrownError` 参数，而 `ajaxComplete` 回调中没有这个参数。

## `.ajaxSend()`

`ajaxSend` 方法允许我们添加一个回调函数，该函数在请求发送时被调用。

例如，我们可以这样写：

```javascript
$(document).ajaxSend(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

我们使用了与其他 Ajax 方法相同的回调函数。

内容也相同。

## `.ajaxStop()`

`.ajaxStop()` 方法允许我们添加一个回调函数，该函数在 Ajax 请求完成时被调用。

例如，我们可以这样写：

```javascript
$(document).ajaxStop(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

我们传入了一个带有 `event`、`xhr` 和 `settings` 参数的回调函数。

`settings` 包含请求数据，如 URL 和请求方法。

`xhr` 是一个包含请求状态的对象。

## `.ajaxSuccess()`

`.ajaxSuccess()` 方法允许我们添加一个回调函数，该函数在 Ajax 请求成功完成时运行。

例如，我们可以这样写：

```javascript
$(document).ajaxSuccess(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

我们有一个回调函数，其参数与其他 Ajax 方法相同。

## 全部选择器

我们可以使用 `*` 选择器获取另一个元素内的所有元素。

例如，如果我们有以下代码：

```html
<div id="test">
  <div>DIV</div>
  <span>SPAN</span>
  <p>P <button>Button</button></p>
</div>
```

那么我们可以通过以下代码获取 ID 为 `test` 的 `div` 内的所有元素：

```javascript
$("#test").find("*").css("border", "3px solid red")
```

然后我们调用 `css` 为所有元素添加红色边框。

## `.animate()`

`.animate()` 方法允许我们对一组 CSS 属性执行自定义动画。

例如，如果我们有以下 HTML：

```html
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/25/300/300.jpg?hmac=hXirsaKumNCLu7iGSrMI_RkAEfXF01DGx6c4wzBUpXs" alt="" width="100" height="123"
  style="position: relative; left: 10px;">
```

我们可以通过以下代码在点击“Click here”时为图片添加动画：

```javascript
$("#clickme").click(function() {
  $("#book").animate({
    opacity: 0.25,
    left: "+=50",
    height: "toggle"
  }, 5000, function() {
    // 动画完成。
  });
});
```

我们获取 ID 为 `clickme` 的 `div`，然后调用 `click` 监听其点击事件。

接着调用 `animate` 通过改变 `left` 属性来为图片添加动画。

## `:animated` 选择器

我们可以使用 `:animated` 选择器选择正在动画中的元素。

例如，如果我们有以下 HTML：

```html
<button id="run">Run</button>

<div></div>
<div id="mover"></div>
<div></div>
```

以及以下 CSS：

```css
div {
   background: yellow;
   border: 1px solid #AAA;
   width: 80px;
   height: 80px;
   margin: 0 5px;
   float: left;
 }

div.colored {
   background: green;
}
```

那么我们可以通过以下代码切换正在动画的 `div`（ID 为 `mover`）的颜色：

```javascript
$("#run").click(function() {
  $("div:animated").toggleClass("colored");
});

function animate() {
  $("#mover").slideToggle("slow", animate);
}

animate();
```

当我们点击 Run 时，`toggleClass` 方法被调用来改变其颜色。

## `.append()`

我们可以使用 `.append` 方法在另一个元素之后添加元素。

例如，如果我们有以下代码：

```html
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

那么我们可以通过以下代码获取带有 `inner` 类的元素：

```javascript
$(".inner").append("<p>Test</p>");
```

然后两个 `div` 都会附加 `<p>Test</p>` HTML。

## `.attr()`

`.attr()` 方法允许我们获取或设置每个匹配元素的属性。

例如，如果我们有以下代码：

```html
<p>Once there was a <em title="huge, gigantic">large</em> cat</p>
<div></div>
```

那么我们可以通过以下代码从 `em` 元素获取 `title` 属性并将其放入 `div` 中：

```javascript
const title = $("em").attr("title");
$("div").text(title);
```

我们也可以用它来设置 `title` 属性：

```javascript
const title = $("em").attr("title", "big");
```

## 属性包含前缀选择器 `[name|="value"]`

我们可以通过属性和名称及值来获取元素。`|` 会匹配值等于给定字符串或以该字符串后跟连字符的值。

例如，如果我们有以下代码：

```html
<a href="example.html" hreflang="en">Some text</a>
```

那么我们可以通过以下代码获取这个元素：

```javascript
$("a[hreflang|='en']").css("border", "3px dotted green");
```

`hreflang` 是属性名称，`'en'` 是值。

## 属性包含选择器 `[name*="value"]`

此选择器选择具有指定属性且属性值包含给定子字符串的元素。

例如，如果我们有以下 HTML：

```html
<input name="man-news">
<input name="milkman">
<input name="letterman2">
<input name="newmilk">
```

那么我们可以通过以下代码获取所有 `name` 属性值包含子字符串 `man` 的 `input` 元素：

```javascript
$("input[name*='man']").val("has man");
```

现在前三个输入框的值都是 `'has man'`。

## 属性包含单词选择器 `[name~="value"]`

我们可以获取具有指定属性且属性值包含给定单词（以空格分隔）的元素。

例如，如果我们有以下代码：



```html
<input name="man-news">
<input name="milk man">
<input name="letterman2">
<input name="newmilk">
```

那么我们可以这样写：

```javascript
$("input[name~='man']").val("has man");
```

来获取 `name` 属性值中包含单词 `man`（以空格分隔）的 `input` 元素。

只有第二个 `input` 满足条件，因此该 `input` 中会出现 `has man`。

## 属性结尾选择器 `[name$="value"]`

我们可以获取具有指定属性且属性值以给定字符串结尾的元素。

例如，如果我们有以下 HTML：

```html
<input name="newsletter">
<input name="milkman">
<input name="jobletter">
```

那么我们可以这样使用这个选择器：

```javascript
$("input[name$='letter']").val("a letter");
```

我们获取所有 `name` 属性值以 `letter` 结尾的输入元素。

然后通过调用 `val` 将前两个输入框填充为 `a letter`。

## 属性等于选择器 `[name="value"]`

我们可以使用此选择器获取属性等于某个值的元素。

例如，如果我们有以下 HTML：

```html
<div>
  <label>
    <input type="radio" name="newsletter" value="Hot Fuzz">
    <span>name?</span>
  </label>
</div>
<div>
  <label>
    <input type="radio" name="newsletter" value="Cold Fusion">
    <span>value?</span>
  </label>
</div>
<div>
  <label>
    <input type="radio" name="newsletter" value="Evil Plans">
    <span>value?</span>
  </label>
</div>
```

我们获取 `value` 设置为 `Hot Fuzz` 的 `span`，并通过编写以下代码用文本内容填充名称：

```javascript
$("input[value='Hot Fuzz']").next().text("Hot Fuzz");
```

现在第一个单选按钮旁边应该显示文本 `Hot Fuzz`。

## 属性不等于选择器 `[name!="value"]`

我们可以使用此选择器选择属性不等于给定值的元素。

例如，如果我们有以下 HTML：

```html
<div>
  <label>
    <input type="radio" name="newsletter" value="Hot Fuzz">
    <span>name?</span>
  </label>
</div>
<div>
  <input type="radio" value="Cold Fusion">
  <span>no name</span>
</div>
<div>
  <label>
    <input type="radio" name="newsletter" value="Evil Plans">
    <span>value?</span>
  </label>
</div>
```

然后我们可以获取 `name` 属性未设置为 `newsletter` 的单选按钮，并通过编写以下代码在其旁边的 `span` 中添加文本：

```javascript
$("input[name!='newsletter']").next().append("<b>; not newsletter</b>");
```

现在第二个单选按钮旁边显示：

```text
no name**; not newsletter**
```

## 属性以指定值开头选择器 `[name^="value"]`

此选择器允许我们选择具有指定属性且属性值以给定字符串开头的元素。

例如，如果我们有以下代码：

```html
<input name="newsletter">
<input name="milkman">
<input name="newsboy">
```

然后我们获取所有 `name` 属性以 `news` 开头的输入元素，并通过编写以下代码为它们设置值：

```javascript
$("input[name^='news']").val("news here!");
```

因此，第一个和最后一个输入框将添加 `news here` 输入。

## `.before()`

`.before()` 方法允许我们在匹配元素集合中的每个元素之前插入内容。

例如，如果我们有以下代码：

```html
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">foo</div>
  <div class="inner">bar</div>
</div>
```

然后我们可以通过编写以下代码在每个 class 为 `inner` 的 `div` 之前添加一个元素：

```javascript
$(".inner").before("<p>Test</p>");
```

然后我们会看到：

```text
Test

foo

Test

bar
```

显示出来。

## `.bind()`

`.bind()` 方法允许我们为元素的某个事件添加处理程序。

例如，如果我们有以下 HTML：

```html
<div id="foo">
  foo
</div>
```

我们可以通过编写以下代码为其添加点击监听器：

```javascript
$("#foo").bind("click", function() {
  alert("User clicked on 'foo.'");
});
```

第一个参数是事件名称。

第二个参数是事件触发时运行的回调函数。

## `.blur()`

`.blur()` 方法将一个事件处理程序绑定到 `blur` JavaScript 事件。

例如，如果我们有以下 HTML：

```html
<form>
  <input id="target" type="text" value="Field 1">
  <input type="text" value="Field 2">
</form>
```

然后我们可以通过编写以下代码监听 ID 为 `target` 的输入字段上的 `blur` 事件：

```javascript
$("#target").blur(function() {
  alert("Handler for .blur() called.");
});
```

我们获取元素，然后传入回调函数，当我们离开第一个输入框时显示一个警告。

## `:button` 选择器

`:button` 选择器选择所有按钮元素以及 `type` 设置为 `button` 的元素。

例如，如果我们有以下 HTML：

```html
<form>
  <fieldset>
    <input type="button" value="Input Button">
    <input type="checkbox">

    <input type="file">
    <input type="submit">
    <input type="text">
    <select>
      <option>Option</option>
    </select>

    <textarea></textarea>
    <button>Button</button>
  </fieldset>
</form>
```

以及以下 CSS：

```css
.marked {
  background-color: yellow;
  border: 3px red solid;
}
```

然后我们可以获取按钮并为其添加 `marked` 类，通过编写以下代码：

```javascript
const input = $(":button").addClass("marked");
console.log(input.length)
```

`type` 设置为 `button` 的输入元素和 `button` 元素将被选中。

## `callbacks.add()`

`callbacks.add` 方法允许我们向回调列表中添加回调函数。

例如，我们可以编写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const bar = function(value) {
  console.log(`bar: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.add(bar);
callbacks.fire("world");
```

我们调用 `$.Callbacks` 方法获取一个回调列表。

然后我们调用 `add` 方法将 `foo` 和 `bar` 方法添加到回调列表中。

`callbacks.fire` 方法将使用给定的参数调用列表中的每个回调函数。

因此，我们在控制台日志中看到：

```text
foo: hello
foo: world
bar: world
```

## `callbacks.disable()`

我们可以调用 `callbacks.disable` 来禁用一个回调列表。

例如，如果我们有以下代码：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.disable();
callbacks.fire("world");
```

然后我们调用 `callbacks.disable` 来阻止回调列表再次被调用。

因此，我们只看到：

```text
foo: hello
```

被记录。

## `callbacks.disabled()`

我们可以使用 `callbacks.disabled()` 方法来检查回调是否已被禁用。

例如，我们可以编写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.disable();
console.log(callbacks.disabled());
callbacks.fire("world");
```

由于我们调用了 `callbacks.disable`，`callbacks.disabled` 应该记录 `true`。

## `callbacks.empty()`

`callbacks.empty()` 方法从列表中移除所有回调。

例如，我们可以编写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const bar = function(value) {
  console.log(`bar: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.add(bar);
callbacks.empty();
console.log(callbacks.has(foo));
console.log(callbacks.has(bar));
```

由于我们调用了 `callbacks.empty` 来移除所有回调，因此两个控制台日志都应该记录 `false`，因为两个回调都已被 `empty` 移除。

## `callbacks.fire()`

`callbacks.fire()` 方法允许我们使用给定的参数调用列表中的所有回调。

例如，我们可以编写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const bar = function(value) {
  console.log(`bar: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.fire("world");
callbacks.add(bar);
callbacks.fire("hello again");
```

我们添加了 `foo` 回调，并分别用 `'hello'` 和 `'world'` 调用了 `fire`，因此我们应该看到：

```text
foo: hello
foo: world
```

被记录。

然后我们将 `bar` 添加到回调列表，并用 `'hello again'` 调用了 `fire`。

因此我们看到：

```text
foo: hello again
bar: hello again
```

被记录。

## `callbacks.fired()`

我们可以使用 `callbacks.fired()` 方法检查回调是否至少被触发过一次。

例如，我们可以编写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.fire("world");
console.log(callbacks.fired());
```

以记录是否有任何回调被 `fired` 调用过。

由于它已被调用，应该记录 `true`。

## `callbacks.fireWith()`

`callbacks.fireWith()` 方法允许我们使用给定的上下文和参数来调用回调函数。

例如，如果我们有以下代码：

```javascript
const log = function(value1, value2) {
  console.log(this, value1, value2);
};

const callbacks = $.Callbacks();
callbacks.add(log);
callbacks.fireWith(window, ["foo", "bar"]);
```

那么 `this` 就是 `window`，`value1` 是 `foo`，`value2` 是 `bar`。

## `callbacks.has()`

`callbacks.has()` 方法允许我们检查回调列表中是否已添加任何回调。

例如，我们可以这样写：

```javascript
const log = function(value1, value2) {
  console.log(this, value1, value2);
};

const callbacks = $.Callbacks();
callbacks.add(log);
console.log(callbacks.has(log));
```

控制台应输出 `true`，因为我们已通过 `add` 添加了它。

## `callbacks.lock()`

`callbacks.lock()` 方法将回调列表锁定在当前状态。

例如，我们可以这样使用它：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.lock();
callbacks.fire("world");
```

我们调用 `callbacks.lock` 方法来阻止任何回调被调用。

因此，我们只会看到：

```text
foo: hello
```

被输出。

## `callbacks.locked()`

我们可以使用 `callbacks.locked()` 方法来检查回调列表是否已被锁定。

例如，如果我们这样写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.lock();
console.log(callbacks.locked());
```

那么最后一个控制台输出应为 `true`，因为我们调用了 `lock` 来锁定回调列表。

## `callbacks.remove()`

我们可以使用 `callback.remove` 方法移除一个回调。

例如，我们可以这样写：

```javascript
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.remove(foo);
callbacks.fire("world");
```

我们在 `foo` 上调用了 `remove`，以从回调列表中移除 `foo`。

因此，第二次 `fire` 回调不会调用 `foo`。

## `.change()`

`.change()` 方法将一个事件处理程序绑定到 `change` JavaScript 事件上。

它也可以用于触发元素上的 `change` 事件。



例如，如果我们有以下 HTML：

```html
<form>
  <input class="target" type="text" value="Field 1">
  <select class="target">
    <option value="option1" selected="selected">Option 1</option>
    <option value="option2">Option 2</option>
  </select>
</form>
```

那么我们可以通过以下代码监听类为 `target` 的元素上触发的 `change` 事件：

```javascript
$(".target").change(function() {
  alert("Handler for .change() called.");
});
```

我们也可以触发元素上的 `change` 事件。

例如，如果我们有以下 HTML：

```html
<form>
  <input class="target" type="text" value="Field 1">
  <select class="target">
    <option value="option1" selected="selected">Option 1</option>
    <option value="option2">Option 2</option>
  </select>
</form>
<div id="other">
  click me
</div>
```

那么我们可以为 ID 为 `other` 的 `div` 添加一个点击监听。

当我们点击该 `div` 时，可以通过以下代码触发所有类为 `target` 的元素上的 `change` 事件：

```javascript
$(".target").change(function() {
  alert("Handler for .change() called.");
});

$("#other").click(function() {
  $(".target").change();
});
```

现在，当我们点击“click me”按钮时，每个类为 `target` 的元素都会弹出警告框。

## `:checkbox` 选择器

`:checkbox` 选择器允许我们选择所有类型为 `checkbox` 的元素。

例如，如果我们有以下 HTML：

```html
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">

  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio">

  <input type="reset">
  <input type="submit">
  <input type="text">

  <select>
    <option>Option</option>
  </select>

  <textarea></textarea>
  <button>Button</button>
</form>
```

那么我们可以通过以下代码高亮所有复选框：

```javascript
$("form input:checkbox")
  .wrap("<span></span>")
  .parent()
  .css({
    background: "yellow",
    border: "3px red solid"
  });
```

我们使用 `:checkbox` 选择器获取复选框，并设置所有选中元素的背景和边框。

## `:checked` 选择器

我们可以使用 `:checked` 选择器获取所有被选中的复选框。

例如，如果我们有以下 HTML：

```html
<form>
  <p>
    <input type="checkbox" name="newsletter" value="Hourly" checked="checked">

    <input type="checkbox" name="newsletter" value="Daily">
    <input type="checkbox" name="newsletter" value="Weekly">

    <input type="checkbox" name="newsletter" value="Monthly" checked>
    <input type="checkbox" name="newsletter" value="Yearly">
  </p>
</form>
```

那么我们可以通过以下代码高亮被选中的复选框：

```javascript
$("input:checked")
  .wrap("<span></span>")
  .parent()
  .css({
    background: "yellow",
    border: "3px red solid"
  });
```

## 子选择器（`parent > child`）

我们可以使用此选择器获取子元素。

例如，如果我们有以下 HTML：

```html
<ul class="topnav">
  <li>Item 1</li>
  <li>Item 2
    <ul>
      <li>Nested item 1</li>
      <li>Nested item 2</li>
      <li>Nested item 3</li>
    </ul>
  </li>
  <li>Item 3</li>
</ul>
```

我们可以通过以下代码获取类为 `topnav` 的 `ul` 的 `li` 元素：

```javascript
$("ul.topnav > li").css("border", "3px double red");
```

我们调用 `css` 为所有匹配的元素添加边框。

## `.children()`

我们可以使用 `children` 方法获取选中元素的子元素。

例如，如果我们有以下 HTML：

```html
<ul class="topnav">
  <li>Item 1</li>
  <li>Item 2
    <ul>
      <li>Nested item 1</li>
      <li>Nested item 2</li>
      <li>Nested item 3</li>
    </ul>
  </li>
  <li>Item 3</li>
</ul>
```

那么我们可以通过以下代码获取 `ul` 的所有子元素：

```javascript
$("ul.topnav").children().css("background-color", "red");
```

我们调用 `css` 将背景设为红色。

## 类选择器（`.class`）

我们可以使用类选择器选择元素。

例如，如果我们有以下 HTML：

```html
<div class="notMe">div class="notMe"</div>
<div class="myClass">div class="myClass"</div>
<span class="myClass">span class="myClass"</span>
```

那么我们可以通过以下代码高亮类为 `myClass` 的元素：

```javascript
$(".myClass").css("border", "3px solid red");
```

## `.clearQueue()`

`.clearQueue()` 方法从队列中移除尚未运行的项目。

例如，如果我们有以下 HTML：

```html
<button id="start">Start</button>
<button id="stop">Stop</button>
<div></div>
```

以及 CSS：

```css
div {
  margin: 3px;
  width: 40px;
  height: 40px;
  position: absolute;
  left: 0px;
  top: 30px;
  background: green;
  display: none;
}

div.newcolor {
  background: blue;
}
```

那么我们可以通过以下代码添加启动和停止动画的方式：

```javascript
$("#start").click(function() {
  const myDiv = $("div");
  myDiv.show("slow");
  myDiv.animate({
    left: "+=200"
  }, 5000);
  myDiv.queue(function() {
    const that = $(this);
    that.addClass("newcolor");
    that.dequeue();
  });
  myDiv.animate({
    left: "-=200"
  }, 1500);
  myDiv.queue(function() {
    const that = $(this);
    that.removeClass("newcolor");
    that.dequeue();
  });
  myDiv.slideUp();
});

$("#stop").click(function() {
  const myDiv = $("div");
  myDiv.clearQueue();
  myDiv.stop();
});
```

在 ID 为 `start` 的按钮的 `click` 回调中，我们使用回调调用 `queue` 来为 `div` 添加动画。

然后在 ID 为 `stop` 的按钮的 `click` 回调中，我们调用 `clearQueue` 来清除队列，然后使用 `stop` 方法停止动画。

## `.click()`

`click` 方法允许我们为 `click` 事件添加事件处理程序，或触发元素上的事件。

例如，如果我们有以下 HTML：

```html
<div id="target">
  Click here
</div>
<div id="other">
  触发处理程序
</div>
```

```javascript
$("#target").click(function() {
  alert("Handler for .click() called.");
});
```

现在，当我们点击它时，会看到弹出警告框。

此外，我们也可以通过编程方式触发 `click` 事件，代码如下：

```javascript
$("#target").click(function() {
  alert("Handler for .click() called.");
});

$("#other").click(function() {
  $("#target").click();
});
```

当我们点击 ID 为 `other` 的 `div` 时，会触发 ID 为 `target` 的 `div` 上的 `click` 事件。

## `.clone()`

`.clone()` 方法会创建匹配元素集合的深拷贝。

例如，如果我们有以下 HTML：

```html
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">Goodbye</div>
</div>
```

那么我们可以通过以下代码获取 class 为 `hello` 的 `div`，复制它，并将其追加到 class 为 `goodbye` 的 `div` 中：

```javascript
$(".hello").clone().appendTo(".goodbye");
```

## `.closest()`

`.closest()` 方法用于获取与给定选择器匹配的最近元素。

例如，如果我们有以下 HTML：

```html
<ul id="one" class="level-1">
  <li class="item-i">I</li>
  <li id="ii" class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

我们可以通过以下代码获取与 class 为 `item-a` 的元素最近的 `ul`：

```javascript
$("li.item-a")
  .closest("ul")
  .css("background-color", "red");
```

这样会同时获取 class 为 `level-2` 和 `level-3` 的 `ul`，并为它们添加红色背景。

## `:contains()` 选择器

我们可以使用 `:contains` 选择器来匹配包含指定文本的元素。

例如，如果我们有以下内容：

```html
<div>John Smith</div>
<div>George Martin</div>
<div>Malcom John Sinclair</div>
<div>J. Ohn</div>
```

那么我们可以通过以下代码获取所有包含文本 `'John'` 的 `div`，并为其应用样式：

```javascript
$("div:contains('John')").css("text-decoration", "underline");
```

这样会给所有包含文本 `'John'` 的 `div` 添加下划线。

因此，第一个和第三个 `div` 会带有下划线。

## `.contents()`

`.contents()` 方法会返回元素的内容。

例如，如果我们有以下内容：

```html
<div class="container">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
  do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  <br><br>
  Ut enim ad minim veniam, quis nostrud exercitation ullamco
  laboris nisi ut aliquip ex ea commodo consequat.
  <br><br>
  Duis aute irure dolor in reprehenderit in voluptate velit
  esse cillum dolore eu fugiat nulla pariatur.
</div>
```

那么我们可以通过以下代码获取文本节点：

```javascript
const els = $(".container")
  .contents()
  .filter(function() {
    return this.nodeType === 3;
  });

console.log(els);
```

`nodeType` 值为 3 的节点即为文本节点。

## `.contextmenu()`

我们可以使用 `.contextmenu()` 方法绑定 `contextmenu` 事件。

例如，如果我们有以下 HTML：

```html
<div id="target">
  Right-click here
</div>
```

那么我们可以通过以下代码监听右键点击：

```javascript
$("#target").contextmenu(function() {
  alert("Handler for .contextmenu() called.");
});
```

当我们右键点击该 `div` 时，会看到弹出警告框。

## `.css()`

我们也可以使用 `css` 方法获取计算样式的值，该方法还能为选中的元素设置样式。

例如，如果我们有以下 HTML：

```html
<div style="background-color:blue;"></div>
<div style="background-color:rgb(15,99,30);"></div>
<div style="background-color:#123456;"></div>
<div style="background-color:#f11;"></div>
```

以及以下 CSS：

```css
div {
  width: 60px;
  height: 60px;
  margin: 5px;
  float: left;
}
```

那么我们可以通过以下代码监听点击事件，并在点击 `div` 时获取样式：

```javascript
$("div").click(function() {
  const color = $(this).css("background-color");
  console.log(color);
});
```

这样就能获取 `background-color` 属性的值。

此外，我们还可以通过以下代码获取多个样式：

```javascript
$("div").click(function() {
  const styles = $(this).css([
    "width", "height", "color", "background-color"
  ]);
  console.log(styles);
});
```

只需传入一个包含属性名的数组即可。

## `.data()`

我们可以使用 `data` 方法在匹配的元素中存储数据。

例如，我们可以编写以下 HTML：

```html
<span></span>
```

然后使用 `data` 存储和获取数据，如下所示：



```javascript
$("body").data("foo", 52);
$("span").first().text($("body").data("foo"));
```

第一行中，我们以键 `'foo'` 和值 52 存储了 `data`。

然后在第二行中，我们获取该数据并将其放入 `span` 中。

## `.dblclick()`

`.dblclick()` 方法用于绑定 `dblclick` 事件的处理程序，或触发元素上的该事件。

例如，如果我们有以下 HTML：

```html
<div id="target">
  Double-click here
</div>
<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过以下代码监听 ID 为 `target` 的 `div` 上的双击事件：

```javascript
$("#target").dblclick(function() {
  alert("Handler for .dblclick() called.");
});
```

我们还可以在点击 ID 为 `other` 的 `div` 时，触发 ID 为 `target` 的 `div` 上的双击事件，代码如下：

```javascript
$("#target").dblclick(function() {
  alert("Handler for .dblclick() called.");
});
$("#other").click(function() {
  $("#target").dblclick();
});
```

## `deferred.always()`

`deferred.always()` 用于添加一个回调，该回调在 deferred 对象被解决或拒绝时都会被调用。

例如，我们可以编写：

```javascript
$.get("foo.php").always(function() {
  alert("$.get completed");
});
```

这样，当我们向 `foo.php` 发起 GET 请求时，就会调用 `alert`。

## `deferred.catch()`

`deferred.catch` 方法用于添加一个回调，该回调在 deferred 对象被拒绝时被调用。

例如，我们可以编写：

```javascript
$.get("foo.php")
  .then(function() {
    alert("$.get succeeded");
  })
  .catch(function() {
    alert("$.get failed!");
  });
```

或者：

```javascript
(async () => {
  try {
    const res = await $.get("foo.php")
  } catch (error) {
    alert("$.get failed!");
  }
})()
```

`$.get` 返回一个 thenable 对象，因此它可以与 `async` 和 `await` 一起使用。

## `deferred.done()`

`deferred.done()` 方法允许我们添加一个回调，该回调在 deferred 对象被解决时被调用。

例如，我们可以编写：

```javascript
$.get("https://jsonplaceholder.typicode.com/todos/1")
  .done(function() {
    alert("$.get succeeded");
  });
```

这样会向 [`jsonplaceholder.typicode.com/todos/1`](https://jsonplaceholder.typicode.com/todos/1) 发起 GET 请求，并在之后执行某些操作。

## `deferred.fail()`

`deferred.fail()` 方法允许我们添加一个回调，该回调在 deferred 对象被拒绝时被调用。

例如，我们可以编写：

```javascript
$.get("test.php")
  .done(function() {
    alert("$.get succeeded");
  })
  .fail(function() {
    alert("$.get failed!");
  });
```

来添加该回调。

## `deferred.pipe()`

我们可以使用 `deferred.pipe()` 方法来过滤和链式处理 deferred 对象。

它会返回另一个 deferred 对象。

我们可以这样使用它：

```javascript
const defer = $.Deferred(),
  filtered = defer.pipe(function(value) {
    return value * 2;
  });

defer.resolve(5);

filtered.done(function(value) {
  alert(value);
});
```

我们调用 `defer.pipe` 并传入一个回调函数，该函数从 `defer` 对象获取解析后的值，将其乘以 2，然后在回调中返回。

然后我们调用 `defer.resolve(5)` 将 5 作为 `value` 的值传递给 `pipe` 回调。

最终我们在 `done` 回调中获取到最终的 `value`，即 10。

我们可以通过编写以下代码来链式调用 deferred：

```javascript
const url = 'https://jsonplaceholder.typicode.com/posts/1';

const url2 = 'https://jsonplaceholder.typicode.com/posts/2';

const request = $.ajax(url, {
    dataType: "json"
  })
  .pipe(function(data) {
    console.log(data);
    return $.ajax(url2);
  })
  .done(function(data) {
    console.log(data);
  });
```

我们在 `$.ajax` 返回的第一个 deferred 对象上调用 `pipe`，然后调用 `done` 从第二个 `$.ajax` 调用中获取数据。

## `:eq()` 选择器

`:eq` 选择器允许我们在匹配集合中选取指定索引处的元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

那么我们可以编写：

```javascript
$("li:eq(2)").css("background-color", "red");
```

来获取第三个 `li` 并为其添加红色背景。

## `.even()`

我们可以使用 `even` 方法获取匹配集合中索引为偶数的元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

那么我们可以通过编写以下代码来调用它：

```javascript
$("li").even().css("background-color", "red");
```

为索引为偶数的 `li` 元素添加红色背景。

## `event.currentTarget`

我们可以使用 `event.currentTarget` 属性获取事件冒泡阶段中的当前 DOM 元素。

例如，如果我们有以下代码：

```html
<p>
  click me
</p>
```

我们可以通过编写以下代码获取点击的 `p` 元素：

```javascript
$("p").click(function(event) {
  alert(event.currentTarget === this);
});
```

`alert` 应该显示 `true`，因为 `this` 就是我们点击的 `p` 元素，与 `event.currentTarget` 相同。

## `event.data`

`event.data` 是一个属性，包含传递给事件的数据。

例如，如果我们有以下 HTML：

```html
<button> 0 </button>
<button> 1 </button>
<button> 2 </button>
<button> 3 </button>
<button> 4 </button>
```

那么我们可以为每个元素添加点击监听器，并通过编写以下代码获取数据：

```javascript
for (let i = 0; i < 5; i++) {
  $("button").eq(i).on("click", {
    value: i
  }, function(event) {
    console.log('value: ', event.data.value);
  });
}
```

我们在点击回调中获取 `event.data.value` 属性的值。

该值应与我们作为第二个参数传入的 `value` 属性值相同。

## `event.delegateTarget`

`event.delegateTarget` 属性包含当前调用的 jQuery 事件处理程序所附加到的元素。

例如，如果我们有以下代码：

```html
<div class='box'>
  <button>
    0
  </button>
</div>
<div class='box'>
  <button>
    1
  </button>
</div>
<div class='box'>
  <button>
    2
  </button>
</div>
```

那么我们可以通过编写以下代码，在点击按钮时，将类为 `box` 的 `div` 设置为红色背景：

```javascript
$(".box").on("click", "button", function(event) {
  $(event.delegateTarget).css("background-color", "red");
});
```

## `event.isDefaultPrevented()`

我们可以调用 `event.isDefaultPrevented()` 来检查是否在某个对象上调用了 `event.preventDefault()`。

例如，如果我们有以下代码：

```html
<a>hello</a>
```

那么我们可以通过编写以下代码来调用此方法：

```javascript
$("a").click(function(event) {
  alert(event.isDefaultPrevented());
  event.preventDefault();
  alert(event.isDefaultPrevented());
});
```

我们调用该方法并在警告框中显示其返回值。

## `event.isPropagationStopped()`

我们可以调用 `event.isPropagationStopped()` 方法来检查是否调用了 `event.stopPropagation()`。

例如，如果我们有以下代码：

```html
<button>click me</button>
```

那么我们可以通过编写以下代码来调用此方法：

```javascript
$("button").click(function(event) {
  alert(event.isPropagationStopped());
  event.stopPropagation();
  alert(event.isPropagationStopped());
});
```

## `event.metaKey`

我们可以使用 `event.metaKey` 属性检查事件触发时是否按下了 meta 键。

在 Windows 中，meta 键是 Windows 键。

在 macOS 中，meta 键是 command 键。

例如，如果我们有以下代码：

```html
<button value="Test" name="Test" id="checkMetaKey">Click me!</button>
```

那么我们可以通过编写以下代码来检查点击按钮时是否按下了 meta 键：

```javascript
$("#checkMetaKey").click(function(event) {
  console.log(event.metaKey);
});
```

## `event.namespace`

我们可以通过 `event.namespace` 属性获取事件的命名空间。

例如，如果我们有以下代码：

```html
<button>display event.namespace</button>
<p>
</p>
```

那么我们可以通过编写以下代码来触发带有命名空间的事件：

```javascript
$("p").on("test.something", function(event) {
  alert(event.namespace);
});

$("button").click(function(event) {
  $("p").trigger("test.something");
});
```

当我们点击按钮时，我们在 `p` 元素上触发 `test.something` 事件。

然后 `event.namespace` 应该是 `something`，并在警告框中显示。

## `event.pageX` 和 `event.pageY`

我们可以分别使用 `event.pageX` 和 `event.pageY` 属性获取鼠标位置相对于文档左边缘的 x 和 y 坐标。

例如，我们可以通过编写以下 HTML 来记录鼠标移动时的坐标：

```html
<div id="log"></div>
```

以及 JavaScript：

```javascript
$(document).on("mousemove", function({
  pageX,
  pageY
}) {
  $("#log").text(`${pageX}, ${pageY}`);
});
```

我们监听 `mousemove` 事件，并从 `event` 对象中获取 `pageX` 和 `pageY` 属性。

## `event.preventDefault()`

我们调用 `event.preventDefault()` 方法来阻止事件的默认行为被执行。

例如，如果我们有以下代码：

```html
<a href='https://google.com'>hello</a>Then
```

那么我们可以通过编写以下代码来阻止用户访问 [`google.com`](https://google.com)：

```javascript
$("a").click(function(event) {
  event.preventDefault();
});
```

## `event.relatedTarget`

`event.relatedTarget` 属性获取事件中涉及的其他 DOM 元素。

例如，如果我们有以下代码：

```html
<div>
  <a href='https://google.com'>hello</a>
</div>
```

那么当鼠标移出 `a` 元素时，我们可以通过此属性获取鼠标移动到的元素：

```javascript
$("a").mouseout(function(event) {
  alert(event.relatedTarget.nodeName);
});
```

由于鼠标移动到了 `div`，我们应在警告框中看到 `DIV`。

## `event.result`

`event.result` 属性返回由事件触发的事件处理程序最后返回的值。

例如，如果我们有以下代码：

```html
<button>display event.result</button>
```

那么我们可以在一个点击监听函数中返回一个值，并通过 `event.result` 获取该值：

```javascript
$("button").click(function(event) {
  return "hello";
});

$("button").click(function(event) {
  console.log(event.result);
});
```

我们在第一个点击监听器中返回 `'hello'`。

然后在第二个点击监听器中记录 `event.result`。

由于这是第一个点击监听器的返回值，因此应记录 `'hello'`。

## `event.stopImmediatePropagation()`

我们可以调用 `event.stopImmediatePropagation()` 方法来停止事件传播。

例如，如果我们有以下 HTML：

```html
<p>paragraph</p>
<div>division</div>
```

以及 CSS：

```css
p {
   height: 30px;
   width: 150px;
   background-color: #ccf;
}

div {
   height: 30px;
   width: 150px;
   background-color: #cfc;
}
```

那么我们可以通过编写以下代码来调用 `stopImmediatePropagation` 以停止在 `p` 上触发的点击事件的传播：

```javascript
$("p").click(function(event) {
  event.stopImmediatePropagation();
});

$("p").click(function(event) {
```



```javascript
$(this).css("background-color", "#f00");

});

$("div").click(function(event) {

  $(this).css("background-color", "#f00");

});
```

在第一个点击监听器中调用了 `event.stopImmediatePropagation()`，因此第二个监听器不会运行。

`div` 的点击监听器不受影响。

## `event.stopPropagation()`

我们可以调用 `event.stopPropagation` 来阻止事件传播到元素的父级和祖先选择器。

例如，如果我们有以下代码：

```html
<p>段落</p>
```

我们可以这样写：

```javascript
$("p").click(function(event) {

  event.stopPropagation();

  // 执行某些操作

});
```

来阻止点击事件的传播。

## `event.target`

我们可以通过 `event.target` 属性获取触发事件的元素。

例如，如果我们有以下代码：

```html
<p>段落</p>
```

那么我们可以通过以下方式获取在 `body` 中被点击的元素：

```javascript
$("body").click(function(event) {

  console.log("点击了：", event.target.nodeName);

});
```

`nodeName` 获取被点击元素的标签名。

## `event.timeStamp`

我们可以通过 `timestamp` 属性获取事件触发的时间。

例如，如果我们有以下代码：

```html
<p>段落</p>
```

那么我们可以这样写：

```javascript
$("body").click(function(event) {

  console.log(event.timeStamp);

});
```

当我们点击段落时，会看到记录的时间戳。

## `event.type`

`event.type` 属性允许我们获取触发的事件类型。

例如，如果我们有以下代码：

```html
<p>段落</p>
```

那么我们可以这样写：

```javascript
$("p").click(function(event) {

  alert(event.type);

});
```

通过 `event.type` 获取触发的事件类型。

## `event.which`

`event.which` 属性允许我们获取按下的键盘键或鼠标键。

例如，如果我们有以下代码：

```html
<input id="whichkey" value="输入一些内容">
```

那么我们可以通过以下方式获取按下的键盘键的键码：

```javascript
$("#whichkey").on("keydown", function(event) {

  console.log(event.type, event.which);

});
```

`which` 返回一个与按键对应的数字。

## `.fadeIn()`

`.fadeIn()` 方法将元素淡入至不透明。

例如，如果我们有以下 HTML：

```html
<div id="clickme">
  点击这里
</div>

<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

以及 CSS：

```css
#book {
  display: none;
}
```

我们可以通过以下方式让图片在点击“点击这里”时缓慢出现：

```javascript
$("#clickme").click(function() {

  $("#fork").fadeIn("slow");

});
```

## `.fadeOut()`

`.fadeOut()` 方法允许我们让元素消失。

例如，如果我们有以下代码：

```html
<div id="clickme">
  点击这里
</div>

<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

那么我们可以通过以下方式让图片在点击“点击这里”时淡出：

```javascript
$("#clickme").click(function() {

  $("#fork").fadeOut("slow");

});
```

## `.fadeTo()`

`.fadeTo()` 方法允许我们设置要淡入到的透明度。

例如，我们可以这样写：

```html
<div id="clickme">
  点击这里
</div>

<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

然后我们可以这样写：

```javascript
$("#clickme").click(function() {

  $("#fork").fadeTo("slow", 0.5);

});
```

第二个参数是要淡入到的透明度。

## `.fadeToggle()`

`.fadeToggle()` 允许我们通过动画改变透明度来显示或隐藏匹配的元素。

例如，如果我们有以下代码：

```html
<button>fadeToggle 1</button>

<button>fadeToggle 2</button>

<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

那么我们可以通过以下方式调用 `fadeToggle` 方法：

```javascript
$("button").click(function() {

  $("#fork").first().fadeToggle("slow", "linear");

});

$("button").last().click(function() {

  $("#fork").first().fadeToggle("fast", "linear");

});
```

我们为按钮添加点击监听器，以便在点击按钮时在内部调用 `fadeToggle` 来切换淡入淡出效果。

## `:file` 选择器

我们可以使用 `:file` 选择器获取类型为 `file` 的输入元素。

例如，如果我们有以下代码：

```html
<form>
  <input type="button" value="输入按钮">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio">
  <input type="reset">
  <input type="submit">
  <input type="text">

  <select>
    <option>选项</option>
  </select>

  <textarea></textarea>

  <button>按钮</button>
</form>
```

我们可以这样写：

```javascript
$("input:file").css({
  background: "yellow",
  border: "3px red solid"
});
```

## `.filter()`

`filter` 方法允许我们从一组匹配的元素中获取符合选择器或通过函数测试的元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>列表项 1</li>
  <li>列表项 2</li>
  <li>列表项 3</li>
  <li>列表项 4</li>
  <li>列表项 5</li>
  <li>列表项 6</li>
</ul>
```

我们可以通过以下方式获取位于偶数位置的 `li` 元素，并为它们添加红色背景：

```javascript
$("li").filter(":nth-child(2n)").css("background-color", "red");
```

因此第 2、4、6 个 `li` 元素会有红色背景。

## `.find()`

`.find()` 方法获取当前匹配元素集合中每个元素的后代，这些后代通过选择器、jQuery 对象或元素进行过滤。

例如，如果我们有以下代码：

```html
<ul class="level-1">
  <li class="item-i">I</li>

  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>

      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>

      <li class="item-c">C</li>
    </ul>
  </li>

  <li class="item-iii">III</li>
</ul>
```

那么我们可以从带有类 `item-ii` 的 `li` 中获取所有 `li` 元素，并为它们添加红色背景：

```javascript
$("li.item-ii").find("li").css("background-color", "red");
```

## `.finish()`

`.finish()` 方法停止当前正在运行的动画，移除所有排队的动画，并完成匹配元素的所有动画。

例如，如果我们有以下 HTML：

```html
<div class="box"></div>

<div id="path">
  <button id="go">Go</button>
  <br>
  <button id="bf" class="b" onclick="finish()">finish</button>
</div>
```

以及 CSS：

```css
.box {
  position: absolute;
  top: 10px;
  left: 10px;
  width: 15px;
  height: 15px;
  background: black;
}
```

那么我们可以通过以下方式为带有类 `box` 的 `div` 创建一个动画，当点击 Go 按钮时触发：

```javascript
const horiz = $("#path").width() - 20,
  vert = $("#path").height() - 20;

$("#go").on("click", function() {
  $(".box")
    .clearQueue()
    .stop()
    .css({
      left: 10,
      top: 10
    })
    .animate({
      top: vert
    }, 3000)
    .animate({
      left: horiz
    }, 3000)
    .animate({
      top: 10
    }, 3000);
});

const finish = () => {
  $("div.box").finish();
}
```

当我们点击 finish 按钮时，会调用 `finish` 函数，将动画跳转到结束状态。

## `.first()`

`.first()` 方法从一组匹配的元素中获取第一个元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>列表项 1</li>
  <li>列表项 2</li>
  <li>列表项 3</li>
  <li>列表项 4</li>
  <li>列表项 5</li>
</ul>
```

那么我们可以获取第一个 `li` 并为其添加红色背景：

```javascript
$("li").first().css("background-color", "red");
```

## `deferred.promise()`

`deferred.promise()` 方法返回 deferred 对象的 promise 对象。

例如，我们可以这样使用它：

```javascript
function asyncEvent() {
  const dfd = jQuery.Deferred();

  setTimeout(function() {
    dfd.resolve("hurray");
  }, Math.floor(400 + Math.random() * 2000));

  setTimeout(function() {
    dfd.reject("error");
  }, Math.floor(400 + Math.random() * 2000));

  setTimeout(function working() {
    if (dfd.state() === "pending") {
      dfd.notify("working... ");
      setTimeout(working, 500);
    }
  }, 1);

  return dfd.promise();
}

(async () => {
  try {
    const res = await $.when(asyncEvent());
    cosole.log(res);
  } catch (err) {
    console.log(err);
  }
})();
```

我们有一个 `asyncEvent` 函数，它在最后一行返回一个来自 deferred 对象的 promise。

它会随机地 resolve 或 reject。

然后在 `async` 函数中，我们调用由 `asyncEvent` 函数返回的 promise。

## `deferred.reject()`

`deferred.reject()` 方法用一个参数拒绝一个 deferred 对象，并调用所有失败回调。

例如，我们可以这样使用它：

```javascript
const deferred = jQuery.Deferred();

deferred.reject("error");
```

## `deferred.rejectWith()`

`deferred.rejectWith()` 方法使用上下文对象和参数拒绝一个 deferred 对象，并调用所有失败回调。

例如，我们可以这样写：

```javascript
const deferred = jQuery.Deferred();

deferred.rejectWith({
    foo: "bar"
  }, [1])
  .catch(function(err) {
    console.log(this, err);
  });
```

我们调用 `rejectWith`，传入 `{ foo: "bar" }` 作为 `this` 值，`[1]` 作为参数数组。

然后我们可以在 `catch` 回调中获取它们。

`this` 是 `{ foo: "bar" }`，`err` 是 1。

## `deferred.resolve()`

我们可以调用 `deferred.resolve()` 来 resolve 一个 deferred 对象，并使用给定的参数调用所有完成回调。

例如，我们可以这样写：

```javascript
(async () => {
  try {
    const deferred = jQuery.Deferred();

    const res = await deferred.resolve(1);

    console.log(res);
  } catch (error) {
    console.log(error);
  }
})();
```

我们创建了 `deferred` 对象。然后我们调用 `deferred.resolve` 方法，传入 resolve 的值。

然后 `res` 就拥有了 resolve 的值，因为我们在 `deferred.resolve` 前加了 `await`。

它能工作是因为它返回一个带有 `then` 方法的对象，该方法接受一个回调，回调参数就是 resolve 的值。

## `deferred.resolveWith()`

`deferred.resolveWith()` 允许我们使用上下文对象和参数 resolve 一个 deferred 对象，并调用所有完成回调。

例如，我们可以这样使用它：

```javascript
const deferred = jQuery.Deferred();

deferred.resolveWith({
    foo: "bar"
  }, [1])
  .then(function(val) {
    console.log(this, val);
  });
```



我们调用`resolveWith`，传入`this`值和一个参数数组。

然后我们在返回的对象上调用`then`，传入一个回调，并获取`this`和`val`的值。

`this`是`{ foo: 'bar' }`，`val`是`1`。

## `deferred.state()`

`deferred.state()`方法返回 deferred 对象的状态。

它可以返回`'pending'`、`'resolved'`或`'rejected'`。

`'pending'`表示 deferred 对象尚未完成。

`'resolved'`表示 deferred 对象已通过`deferred.resolve()`或`deferred.resolveWith()`调用。

`'rejected'`表示 deferred 对象处于拒绝状态。调用`deferred.reject()`或`deferred.rejectedWith()`会使其变为`'rejected'`。

例如，我们可以这样使用它：

```javascript
const deferred = jQuery.Deferred();

deferred.resolveWith({
  foo: 'bar'
}, [1])
  .then(function(val) {
    console.log(deferred.state());
  });
```

然后控制台应该会输出`'resolved'`。

## `:disabled`选择器

我们可以使用`:disabled`选择器获取被禁用的输入元素。

例如，如果我们有以下 HTML：

```html
<form>
  <input name="email" disabled="disabled">
  <input name="id">
</form>
```

那么我们可以这样设置禁用输入的值：

```javascript
$("input:disabled").val("this is it");
```

## `.each()`

`.each()`方法允许我们遍历一个 jQuery 对象。

例如，如果我们有以下 HTML：

```html
<ul>
  <li>foo</li>
  <li>bar</li>
</ul>
```

那么我们可以这样获取所有`li`元素：

```javascript
$("li").each(function(index) {
  console.log(index, $(this).text());
});
```

## 元素选择器

我们可以使用元素选择器获取具有给定标签名的元素。

例如，如果我们有以下 HTML：

```html
<div>DIV1</div>
<div>DIV2</div>
<span>SPAN</span>
```

那么我们可以这样给所有 div 添加红色边框：

```javascript
$("div").css("border", "9px solid red");
```

## `.empty()`

`.empty()`方法移除 DOM 中匹配元素集合的所有子节点。

例如，如果我们有以下 HTML：

```html
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">bye</div>
</div>
```

那么我们可以这样调用`empty`：

```javascript
$(".hello").empty();
```

现在，class 为`hello`的 div 内部将不再有文本。

## `:empty`选择器

我们可以使用`:empty`选择器获取所有没有子元素的元素。

例如，如果我们有以下内容：

```html
<table>
  <tr>
    <td>TD #0</td>
    <td></td>
  </tr>
  <tr>
    <td>TD #2</td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>TD#5</td>
  </tr>
</table>
```

那么我们可以这样向空的`td`元素添加文本：

```javascript
$("td:empty")
  .text("Was empty")
  .css("background", "green");
```

我们将`'Was empty'`文本添加到空的`td`元素中，并为其添加绿色背景。

## `:enabled`选择器

我们可以使用`:enabled`选择器获取所有启用的输入元素。

例如，如果我们有以下 HTML：

```html
<form>
  <input name="email" disabled>
  <input name="id">
</form>
```

那么我们可以获取启用的输入并设置其值：

```javascript
$("input:enabled").val("this is it");
```

## `.end()`

`.end()`方法结束当前链中最近的一次过滤操作，并将匹配元素集合恢复到之前的状态。

例如，如果我们有以下 HTML：

```html
<ul class="first">
  <li class="foo">list item 1</li>
  <li>list item 2</li>
  <li class="bar">list item 3</li>
</ul>
<ul class="second">
  <li class="foo">list item 1</li>
  <li>list item 2</li>
  <li class="bar">list item 3</li>
</ul>
```

我们可以通过以下方式在同一个方法链中为 class 为`foo`的`li`和 class 为`bar`的`li`应用样式：

```javascript
$("ul.first")
  .find(".foo")
  .css("background-color", "red")
  .end()
  .find(".bar")
  .css("background-color", "green");
```

`end`方法让我们结束对 class 为`foo`的`li`的操作，然后我们调用`find`来查找另一个元素。

## `.eq()`

`.eq()`方法将匹配元素集合缩减为指定索引的那个元素。

例如，如果我们有以下内容：

```html
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

那么我们可以获取索引为`2`的`li`（即第三个），并为其添加红色背景：

```javascript
$("li").eq(2).css("background-color", "red");
```

## `deferred.then()`

`deferred.then()`允许我们添加处理程序，这些处理程序在 deferred 对象被 resolve、reject 或仍在进行中时被调用。

例如，我们可以这样写：

```javascript
$.get("https://jsonplaceholder.typicode.com/posts/1")
  .then(
    function() {
      alert("$.get succeeded");
    },
    function() {
      alert("$.get failed!");
    }
  );
```

我们使用`$.get`发起请求，它返回一个 deferred 对象。

然后我们调用`then`，第一个参数是成功回调，第二个参数是失败回调。

## `.delay()`

`.delay()`方法设置一个定时器，延迟队列中后续项目的执行。

例如，如果我们有以下 HTML：

```html
<div id="foo"></div>
```

和 CSS：

```css
#foo {
  width: 200px;
  height: 200px;
  min-height: 100px;
  background-color: green
}
```

我们可以通过以下方式添加上滑效果，然后延迟后显示淡入效果：

```javascript
$("#foo").slideUp(300).delay(800).fadeIn(400);
```

`delay(800)`添加了 800 毫秒的延迟。

## `.dequeue()`

`.dequeue()`方法在匹配元素上运行队列中的下一个函数。

例如，如果我们有以下 HTML：

```html
<button>Start</button>
<div></div>
```

和 CSS：

```css
div {
  margin: 3px;
  width: 50px;
  position: absolute;
  height: 50px;
  left: 10px;
  top: 30px;
  background-color: yellow;
}

div.red {
  background-color: red;
}
```

我们可以通过编写以下代码让`div`滑动并变红：

```javascript
$("button").click(function() {
  $("div")
    .animate({
      left: "+=200px"
    }, 2000)
    .animate({
      top: "0px"
    }, 600)
    .queue(function() {
      $(this).toggleClass("red").dequeue();
    })
    .animate({
      left: "10px",
      top: "30px"
    }, 700);
});
```

在`queue`回调中，我们调用：

```javascript
$(this).toggleClass("red").dequeue();
```

来为`div`添加`red`类。

## 后代选择器

我们可以选择给定选择器的所有后代元素。

例如，如果我们有以下 HTML：

```html
<form>
  <div>Form is surrounded by the green border.</div>
  <label for="name">Child of form:</label>
  <input name="name" id="name">
  <fieldset>
    <label for="newsletter">Newsletter</label>
    <input name="newsletter" id="newsletter">
  </fieldset>
</form>
```

那么我们可以通过编写以下代码来获取`form`元素中的 input 元素：

```javascript
$("form input").css("border", "2px dotted blue");
```

## `.detach()`

`.detach()`方法从 DOM 中移除匹配的元素集合。

例如，如果我们有以下 HTML：

```html
<p>Hello</p>
how are
<p>you?</p>
<button>Attach/detach paragraphs</button>
```

那么我们可以通过编写以下代码在点击按钮时附加或分离段落：

```javascript
let p;

$("button").click(function() {
  if (p) {
    p.appendTo("body");
    p = null;
  } else {
    p = $("p").detach();
  }
});
```

在`click`处理函数中，我们检查是否存在任何`p`元素。

如果存在，则调用`detach`移除它们。被移除的元素由`detach`返回。

如果不存在，则将`p`元素附加到`body`并将`p`设置为`null`。

## `.die()`

`die`方法移除之前使用`live`方法附加的事件处理程序。

例如，我们可以编写：

```javascript
$("p").die();
```

来解除绑定到`p`元素上的所有事件处理程序。

我们也可以只解除`click`事件处理程序，通过编写：

```javascript
$("p").die('click');
```

此外，我们可以通过编写以下代码来解除单个事件处理程序：

```javascript
const foo = function() {
};

$("p").live("click", foo);
$("p").die("click", foo);
```

我们使用`die`方法移除了`foo`点击处理程序。

## `:first-child`选择器

我们可以使用`:first-child`选择器来获取第一个子元素。

例如，如果我们有以下 HTML：

```html
<div>
  <span>Glen,</span>
  <span>Jane,</span>
  <span>Ralph</span>
</div>
```

以及以下 CSS：

```css
.green {
  color: green
}
```

那么我们可以编写：

```javascript
$("div span:first-child")
  .css("text-decoration", "underline")
  .hover(function() {
    $(this).addClass("green");
  }, function() {
    $(this).removeClass("green");
  });
```

使用`:first-child`选择器获取`div`中的第一个`span`。

然后我们调用`css`为第一个`span`添加下划线。

最后我们使用`hover`为其添加悬停效果。

第一个回调在鼠标悬停到元素上时调用，第二个回调在鼠标移开时调用。

## `:first-of-type`选择器

我们可以使用`:first-of-type`选择器来选择所有在其同辈元素中具有相同元素名称的第一个元素。

例如，如果我们有以下 HTML：

```html
<div>
  <span>Glen,</span>
  <span>Tane,</span>
  <span>Ralph</span>
</div>
<div>
  <b>Nobody,</b>
  <span>John,</span>
  <span>Scott,</span>
  <span>Tim</span>
</div>
```

以及以下 CSS：

```css
.green {
  color: green
}
```

那么我们可以通过编写以下代码为每个`div`中的第一个`span`添加`green`类：

```javascript
$("span:first-of-type").addClass("green");
```

## `:first`选择器

`:first`选择器允许我们选择第一个匹配的 DOM 元素。

例如，如果我们有以下内容：

```html
<table>
  <tr>
    <td>Row 1</td>
  </tr>
  <tr>
    <td>Row 2</td>
  </tr>
  <tr>
    <td>Row 3</td>
  </tr>
</table>
```

那么我们可以通过编写以下代码让第一个`tr`变为斜体：

```javascript
$("tr:first").css("font-style", "italic");
```

现在`tr`中的所有内容都变为斜体。

## `.focus()`

`focus`方法允许我们为`focus`事件添加事件处理程序，或在元素上触发该事件。

例如，如果我们有以下内容：

```html
<form>
  <input id="target" type="text" value="Field 1">
  <input type="text" value="Field 2">
</form>
<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过编写以下代码为 ID 为`target`的输入框添加一个在`focus`事件触发时调用的回调：

```javascript
$("#target").focus(function() {
  console.log("Handler for .focus() called.");
});
```

## `:focus`选择器

`:focus`选择器用于选择当前获得焦点的元素。

例如，如果我们有以下 HTML：

```html
<div id="content">
  <input tabIndex="1">
  <input tabIndex="2">
  <select tabIndex="3">
    <option>select menu</option>
  </select>
  <div tabIndex="4">
    a div
  </div>
</div>
```

以及以下 CSS：

```css
.focused {
  background: green;
}
```

那么我们可以通过编写以下代码为获得焦点的元素添加`green`类：



```javascript
$("#content").delegate("*", "focus blur", function() {
  const elem = $(this);

  setTimeout(function() {
    elem.toggleClass("focused", elem.is(":focus"));
  }, 0);
});
```

`delegate` 方法的回调中，`this` 的值是 ID 为 `content` 的 `div` 的子元素。

当任何子元素上触发 `focus` 或 `blur` 事件时，该回调被调用。

因此我们可以使用 `toggleClass` 在元素获得焦点时切换 `green` 类的开启状态。

第一个参数是类名，第二个参数是切换第一个参数中类的条件。

## `.focusin()`

`.focusin()` 方法将一个事件处理程序绑定到 `focusin` 事件。

例如，如果我们有以下内容：

```html
<p><input type="text"> <span>focusin fire</span></p>
<p><input type="text"> <span>focusin fire</span></p>
```

那么我们可以编写：

```javascript
$("p").focusin(function() {
  $(this).find("span").css("display", "inline").fadeOut(1000);
});
```

我们获取 `span` 并在聚焦到 `p` 元素内的输入框时将其淡出。

## `.focusout()`

`focusout` 方法允许我们将一个事件处理程序绑定到 `focusout` JavaScript 事件。

例如，如果我们有以下内容：

```html
<p><input type="text"> <span>focusout fire</span></p>
<p><input type="text"> <span>focusin fire</span></p>
```

我们可以编写：

```javascript
let focus = 0;

$("p")
  .focusout(function() {
    focus++;
    console.log(focus);
  });
```

来统计 `focusout` 事件被触发的次数。

当焦点移出 `p` 元素时，该事件将被触发。

## `.get()`

`get` 方法检索由 jQuery 对象匹配的 DOM 元素。

例如，如果我们有以下内容：

```html
<ul>
  <li id="foo">foo</li>
  <li id="bar">bar</li>
</ul>
```

我们通过编写以下代码获取第一个 `li` 元素：

```javascript
console.log($("li").get(0));
```

## `.has()`

`has` 方法允许我们将匹配的元素集合缩减为那些拥有与选择器或 DOM 元素匹配的后代的元素。

例如，如果我们有以下内容：

```html
<ul>
  <li>list item 1</li>
  <li>
    list item 2
    <ul>
      <li>list item 2-a</li>
      <li>list item 2-b</li>
    </ul>
  </li>
  <li>list item 3</li>
  <li>list item 4</li>
</ul>
```

我们可以编写：

```javascript
$("li").has("ul").css("background-color", "red");
```

来获取所有内部包含 `ul` 的 `li`，并为其添加红色背景。

## 属性选择器 `[name]`

我们可以使用属性选择器来获取所有设置了给定属性的元素。

例如，如果我们有以下内容：

```html
<div>no id</div>
<div id="hey">with id</div>
<div id="there">has an id</div>
<div>nope</div>
```

那么我们可以通过编写以下代码获取所有设置了 `id` 属性的元素：

```javascript
$("div[id]").one("click", function() {
  const idString = $(this).attr("id");
  $(this).text(idString);
});
```

在回调中，我们将当前点击元素的文本内容设置为 `id` 属性的值。

## `:has()` 选择器

`:has` 选择器允许我们获取所有包含至少一个匹配指定选择器的元素的元素。

例如，如果我们有以下 HTML：

```html
<div>
  <p>paragraph</p>
</div>
<div>Hello again! (with no paragraph)</div>
```

以及以下 CSS：

```css
.test {
  border: 3px inset red;
}
```

那么我们可以通过以下代码为包含 `p` 元素的 `div` 添加边框：

```javascript
$("div:has(p)").addClass("test");
```

## `.hasClass()`

`.hasClass()` 方法用于判断任何匹配的元素是否被赋予了指定的类。

例如，如果我们有以下内容：

```html
<div id="mydiv" class="foo bar"></div>
```

那么我们可以通过以下代码检查 ID 为 `mydiv` 的 `div` 是否添加了 `foo` 类：

```javascript
$("#mydiv").hasClass("foo");
```

## `:header` 选择器

`:header` 选择器用于选取所有标题元素（例如 `h1`、`h2` 等）。

例如，如果我们有以下内容：

```html
<h1>Header 1</h1>
<p>Contents 1</p>
<h2>Header 2</h2>
<p>Contents 2</p>
```

那么我们可以编写：

```javascript
$(":header").css({
  background: "gray",
  color: "blue"
});
```

为 `h1` 和 `h2` 元素添加灰色背景并将文字颜色设为蓝色。

## `.height()`

`.height()` 方法获取匹配元素集合中第一个元素的当前计算高度。

它也可以设置每个匹配元素的高度。

例如，我们可以通过以下代码获取 `window` 的高度：

```javascript
console.log($(window).height());
```

如果我们有一个 `div`：

```html
<div></div>
```

以及以下 CSS：

```css
div {
  width: 50px;
  height: 70px;
  float: left;
  margin: 5px;
  background: red;
  cursor: pointer;
}
```

我们可以通过以下代码在点击时设置其高度：

```javascript
$("div").one("click", function() {
  $(this).height(30).css({
    cursor: "auto",
    backgroundColor: "green"
  });
});
```

高度以像素为单位。

## `:hidden` 选择器

我们可以使用 `:hidden` 选择器选取所有隐藏的元素。

例如，如果我们有以下内容：

```html
<div></div>
<div style="display:none;">Hidden</div>
<div></div>
<div class="starthidden">Hidden</div>
<div></div>
<form>
  <input type="hidden">
  <input type="hidden">
  <input type="hidden">
</form>
```

以及以下 CSS：

```css
.starthidden {
  display: none;
}
```

那么我们可以通过以下代码获取所有非 `script` 元素的隐藏元素：

```javascript
const hiddenElements = $("body").find(":hidden").not("script");
console.log(hiddenElements);
```

我们也可以通过以下代码显示隐藏的 `div`：

```javascript
$("div:hidden").show(3000);
```

## `.hide()`

`.hide()` 方法用于隐藏匹配的元素。

例如，如果我们有以下内容：

```html
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c" alt="">
```

那么我们可以通过以下代码在点击“Click here”时隐藏图片：

```javascript
$("#clickme").click(function() {
  $("#book").hide("slow", function() {
    alert("Animation complete.");
  });
});
```

`hide` 的第一个参数是动画类型。

第二个参数是动画完成时调用的回调函数。

## `.hover()`

`hover` 方法允许我们绑定鼠标悬停和移出元素的事件处理程序。

例如，如果我们有以下内容：

```html
<ul>
  <li>Milk</li>
  <li>Bread</li>
  <li class="fade">Chips</li>
  <li class="fade">Socks</li>
</ul>
```

那么我们可以通过以下代码在鼠标悬停时向 `li` 文本添加 `***`：

```javascript
$("li").hover(
  function() {
    $(this).append($("<span> ***</span>"));
  },
  function() {
    $(this).find("span").last().remove();
  }
);

$("li.fade").hover(function() {
  $(this).fadeOut(100);
  $(this).fadeIn(500);
});
```

当鼠标移出时，`***` 会消失。

## `.html()`

`.html()` 方法获取匹配元素集合中第一个元素的 HTML 内容。

它也可以用于设置每个匹配元素的 HTML。

例如，如果我们有以下内容：

```html
<p>
  <b>Click</b> to change the <span id="tag">html</span>
</p>
```

那么我们可以通过以下代码点击 `p` 元素将其文本更改为原始 HTML 形式：

```javascript
$("p").click(function() {
  const htmlString = $(this).html();
  $(this).text(htmlString);
});
```

我们在第一行调用 `html` 获取 HTML 代码，然后将其设置为 `text` 值。

当设置为文本内容时，它会被转义，因此我们会看到原始代码显示出来。

## ID 选择器（`#id`）

我们可以使用 ID 选择器选取单个元素。

例如，如果我们有以下内容：

```html
<div id="myDiv">id="myDiv"</div>
```

那么我们可以通过以下代码为 `div` 添加红色边框：

```javascript
$("#myDiv").css("border", "3px solid red");
```

## `jQuery.globalEval()`

我们可以使用 `jQuery.globalEval()` 方法在全局范围内执行一些 JavaScript 代码。

例如，我们可以编写：

```javascript
jQuery.globalEval("let newVar = true;");
```

来执行一些代码。

## `jQuery.grep()`

`jQuery.grep()` 方法用于查找数组中满足过滤函数的元素。

例如，我们可以编写：

```javascript
const arr = [1, 9, 3, 8, 6, 1, 5, 9, 4, 7, 3, 8, 6, 9, 1];

const filteredArr = jQuery.grep(arr, function(n, i) {
  return (n !== 5 && i > 4);
});

console.log(filteredArr);
```

然后我们返回一个数组，其中包含满足传入 `grep` 的回调中条件的元素。

`n` 是数组条目，`i` 是其索引。

## `jQuery.hasData()`

`jQuery.hasData()` 方法允许我们检查是否有数据保存到元素中。

例如，如果我们有以下内容：

```html
<p></p>
```

那么我们可以通过以下代码使用它：

```javascript
const p = jQuery("p")[0];

console.log(jQuery.hasData(p));

$.data(p, "testing", 123);

console.log(jQuery.hasData(p));
```

我们在 `p` 元素上调用 `hasData` 来检查是否有任何数据保存到其中。

因此，第一个控制台日志应输出 `false`，第二个应输出 `true`。

## `jQuery.inArray()`

`jQuery.inArray()` 方法允许我们检查一个元素是否在数组中。

如果找到，则返回其索引，否则返回 -1。

例如，我们可以编写：

```javascript
console.log($.inArray(5 + 5, ["8", "9", "10", 10 + ""]));
```

来检查 10 是否在数组中。

由于它不在数组中，应返回 -1。

## `jQuery.isEmptyObject()`

我们可以使用 `jQuery.isEmptyObject()` 检查一个元素是否为空对象。

例如，如果我们有以下内容：

```javascript
console.log(jQuery.isEmptyObject({}));
```

由于我们向方法传递了一个空对象，这应输出 `true`。

## `jQuery.isPlainObject()`

`jQuery.isPlainObject()` 方法允许我们检查一个 JavaScript 对象是否为普通对象。

普通对象是对象字面量。

例如，如果我们有以下内容：

```javascript
console.log(jQuery.isPlainObject({}));
console.log(jQuery.isPlainObject("test"));
```

那么第一个控制台日志输出 `true`，第二个输出 `false`。

## `jQuery.isXMLDoc()`

我们可以使用 `jQuery.isXMLDoc()` 方法检查一个文档对象是否为 XML 文档。

例如，我们可以编写：

```javascript
console.log(jQuery.isXMLDoc(document));
```

那么控制台日志输出 `false`。

## `jQuery.makeArray()`

我们可以使用 `jQuery.makeArray()` 方法将元素列表转换为数组。

例如，如果我们有以下内容：

```html
<div>First</div>
<div>Second</div>
<div>Third</div>
<div>Fourth</div>
```

那么我们可以编写：

```javascript
const elems = document.getElementsByTagName("div");
const arr = jQuery.makeArray(elems);

console.log(arr);
```

我们使用 `getElementsByTagName` 获取 `div` 元素。

然后调用 `jQuery.makeArray` 将元素列表转换为数组。

## `jQuery.map()`

`jQuery.map()` 方法将数组或对象中的所有项转换为一个新的项数组。

例如，我们可以编写：

```javascript
const fakeArray = {
  "length": 2,
  0: "foo",
  1: "bar"
};

const realArray = $.makeArray(fakeArray);
```

```javascript
const mapped = $.map(realArray, function(val, i) {
  return val + val;
});

console.log(mapped);
```

`fakeArray` 是一个带有数字键和 `length` 属性的对象。

我们调用 `$.makeArray` 将其转换为真正的数组。

然后调用 `$.map` 将数组条目映射为新值。

因此 `mapped` 是 `["foofoo", "barbar"]`。

## `jQuery.Callbacks()`

`jQuery.Callbacks()` 方法允许我们创建一个回调列表来管理回调函数。

例如，我们可以这样写：

```javascript
const fn1 = (val) => console.log('fn1', val);
const fn2 = (val) => console.log('fn2', val);

const callbacks = $.Callbacks();
```



```javascript
callbacks.add(fn1);

callbacks.fire("foo!");

callbacks.add(fn2);

callbacks.fire("bar!");
```

我们调用 `$.Callbacks()` 来返回回调列表对象。

然后调用 `add` 来添加回调函数。

再调用 `fire` 来使用给定的参数调用回调函数。

因此，我们会得到：

```text
fn1 foo!

fn1 bar!

fn2 bar!
```

输出在控制台中。

## `jQuery.contains()`

`jQuery.contains()` 方法允许我们检查一个 DOM 元素是否是另一个 DOM 元素的子元素。

例如，我们可以这样写：

```javascript
console.log($.contains(document.documentElement, document.body));
```

来检查 `body` 元素是否在 `document` 元素内。

由于 `body` 在 `document` 中，这应该返回 `true`。

## `jQuery.cssHooks`

`jQuery.cssHooks` 允许我们直接挂钩到 jQuery，以覆盖 CSS 属性的获取或设置方式。

我们还可以更改 CSS 属性的规范化方式、属性命名，或创建自定义属性。

例如，如果我们有以下 HTML：

```html
<div id='element'>
  foo
</div>

<div id='another'>
  bar
</div>
```

那么我们可以通过以下方式指定如何获取和设置 `border-radius` CSS 属性：

```javascript
const borderRadius = "borderRadius";

$.cssHooks.borderRadius = {
  get(elem, computed, extra) {
    return $.css(elem, borderRadius);
  },

  set(elem, value) {
    elem.style[borderRadius] = value;
  }
};

$("#element").css("borderRadius", "10px");

$("#another").css("border-radius", "20px");
```

## `jQuery.cssNumber`

`jQuery.cssNumber` 对象包含所有可以不带单位使用的 CSS 属性。

例如，我们可以通过以下方式设置 `borderRadius` CSS 属性不带单位使用：

```javascript
jQuery.cssNumber.borderRadius = true;
```

默认对象包含以下设置为 `true` 的属性：

- `zIndex`
- `fontWeight`
- `opacity`
- `zoom`
- `lineHeight`
- `widows`
- `orphans`
- `fillOpacity`
- `columnCount`
- `order`
- `flexGrow`
- `flexShrink`

## `jQuery.data()`

我们可以使用 `jQuery.data()` 方法保存与指定元素关联的任意数据，并返回设置的值。

例如，如果我们有以下 HTML：

```html
<div>
  The values stored were
  <span></span>
  and
  <span></span>
</div>
```

那么我们可以通过以下方式将数据保存到 `div` 中并获取它：

```javascript
const div = $("div")[0];

jQuery.data(div, "test", {
  first: 16,
  last: "pizza!"
});

$("span").first().text(jQuery.data(div, "test").first);

$("span").last().text(jQuery.data(div, "test").last);
```

我们调用 `jQuery.data` 并传入 `div` 来保存数据。

第一个参数是要保存数据的元素。

第二个参数是获取数据的键。

最后一个参数是我们正在保存的对象。

然后在最后两行中获取数据，并将其设置为 `span` 的文本内容。

## `jQuery.Deferred()`

`jQuery.Deferred()` 方法是一个工厂函数，返回一个可链式调用的实用对象，该对象具有注册回调、调用回调以及传递任何同步或异步操作的成功或失败状态的方法。

## `jQuery.dequeue()`

`jQuery.dequeue()` 方法允许我们在匹配元素的队列上运行下一个函数。

例如，如果我们有以下 HTML：

```html
<button>Start</button>

<div></div>
```

以及以下 CSS：

```css
div {
  margin: 3px;
  width: 50px;
  position: absolute;
  height: 50px;
  left: 10px;
  top: 30px;
  background-color: yellow;
}

div.red {
  background-color: red;
}
```

那么当我们点击 Start 按钮时，通过以下代码对 `div` 进行动画：

```javascript
$("button").click(function() {
  $("div")
    .animate({
      left: '+=200px'
    }, 2000)
    .animate({
      top: '0px'
    }, 600)
    .queue(function() {
      $(this).toggleClass("red");
      $.dequeue(this);
    })
    .animate({
      left: '10px',
      top: '30px'
    }, 700);
});
```

我们调用 `$.dequeue` 来调用 `animate` 方法中的动画。

## `.is()`

`is` 方法允许我们检查当前匹配的元素集合是否与选择器、元素或 jQuery 对象匹配。

如果至少有一个元素与给定元素匹配，则返回 `true`。

例如，如果我们有以下 HTML：

```html
<ul>
  <li>list <strong>item 1</strong></li>
  <li><span>list item 2</span></li>
  <li>list item 3</li>
</ul>
```

那么我们可以通过以下方式检查当前点击的元素是否是 `li`，并为其添加红色背景：

```javascript
$("ul").click(function(event) {
  const target = $(event.target);

  if (target.is("li")) {
    target.css("background-color", "red");
  }
});
```

## `jQuery()`

`jQuery()` 函数接受一个包含 CSS 选择器的字符串，以匹配一组元素。

例如，如果我们有以下 HTML：

```html
<div class='foo'>
  <span>foo</span>
</div>

<div>
  bar
</div>
```

以及 CSS：

```css
.bar {
  background: green
}
```

我们可以通过以下方式将 `bar` 类添加到 class 为 `foo` 的 `div` 内的 `span` 中：

```javascript
$("div.foo").click(function() {
  $("span", this).addClass("bar");
});
```

## `.jquery`

`.jquery` 属性允许我们获取包含 jQuery 版本号的字符串。

因此我们可以这样写：

```javascript
console.log($.fn.jquery)
```

来获取它。

## `jQuery.ajax()`

我们可以使用 `jQuery.ajax()` 方法发起 Ajax 请求。

例如，我们可以通过以下方式发起 GET 请求：

```javascript
const jqxhr = $.ajax("https://jsonplaceholder.typicode.com/posts/1")
  .done(function() {
    alert("success");
  })
  .fail(function() {
    alert("error");
  })
  .always(function() {
    alert("complete");
  });

jqxhr.always(function() {
  alert("second complete");
});
```

我们调用 `done` 并传入一个回调函数，在请求成功后执行某些操作。

`fail` 回调在请求失败时执行。

`always` 回调在请求完成时执行，无论结果如何。

`jqxhr.always` 的回调在请求完成时执行，无论结果如何。

## `jQuery.ajaxPrefilter()`

`jQuery.ajaxPrefilter()` 方法用于处理自定义 Ajax 选项，或在每个请求发送之前以及被 `$.ajax()` 处理之前修改现有选项。

例如，我们可以这样写：

```javascript
const currentRequests = {};

$.ajaxPrefilter(function(options, originalOptions, jqXHR) {
  if (options.abortOnRetry) {
    if (currentRequests[options.url]) {
      currentRequests[options.url].abort();
    }

    currentRequests[options.url] = jqXHR;
  }
});

$.ajax("https://jsonplaceholder.typicode.com/posts/1")
  .done(function() {
    alert("success");
  });
```

来检查 `abortOnRetry` 选项是否启用，如果请求 URL 在 `currentRequests` 对象中，则调用 `abort`。

这样，在已经尝试过之后就不会再重试。

## `jQuery.ajaxSetup()`

`jQuery.ajaxSetup()` 方法允许我们为未来的 Ajax 请求设置默认值。

但不推荐使用它。

例如，我们可以这样写：

```javascript
$.ajaxSetup({
  url: "https://jsonplaceholder.typicode.com/posts/1"
});

$.ajax()
  .done(function() {
    alert("success");
  });
```

那么发起请求的默认 URL 就是 `"https://jsonplaceholder.typicode.com/posts/1"`。

## `jQuery.ajaxTransport()`

我们调用 `jQuery.ajaxTransport()` 方法来创建一个处理 Ajax 数据传输的对象。

例如，我们可以这样写：

```javascript
jQuery.ajaxSetup({
  accepts: {
    script: "application/json"
  },

  contents: {
    script: /json/
  },

  converters: {
    "text script": jQuery.globalEval
  }
});
```

```javascript
$.ajax("https://jsonplaceholder.typicode.com/posts/1")
  .done(function() {
    alert("success");
  });
```

为我们的请求添加 `application/json` 标头。

## `:image` 选择器

我们可以使用 `:image` 选择器选择任何类型为 `image` 的元素。

例如，如果我们有以下代码：

```html
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="image">
</form>
```

那么我们可以编写：

```javascript
$("input:image").css({
  background: "yellow",
  border: "3px red solid"
});
```

为图片输入框添加黄色背景和红色边框。

## `.index()`

`index` 方法允许我们获取元素的索引。

例如，如果我们有以下代码：

```html
<ul>
  <li id="foo">foo</li>
  <li id="bar">bar</li>
  <li id="baz">baz</li>
</ul>
```

那么我们可以这样使用它：

```javascript
const listItems = $("li").slice(1);

console.log($("li").index(listItems));
```

控制台应输出 1，因为我们获取了列表中的第一个项目。

## `.innerHeight()`

`innerHeight` 方法获取匹配元素集合中第一个元素的当前计算内高度。

它也可以设置每个匹配元素的内高度。

例如，如果我们有以下代码：

```html
<p>Hello</p>
```

那么我们可以通过编写以下代码获取 `p` 元素的内高度：

```javascript
console.log($("p").first().innerHeight());
```

如果我们有以下代码：

```html
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

那么我们可以通过编写以下代码设置内高度：

```javascript
const modHeight = 70;

$("div").one("click", function() {
  $(this).innerHeight(modHeight).addClass("mod");
});
```

## `.innerWidth()`

`innerWidth` 方法允许我们设置匹配元素集合中第一个元素的内宽度。

它也可以用于设置每个匹配元素的内宽度。

例如，如果我们有以下代码：

```html
<p>Hello</p>
```

那么我们可以通过编写以下代码获取 `p` 元素的内宽度：

```javascript
const p = $("p").first();

console.log(p.innerWidth());
```

如果我们有以下代码：

```html
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

以及以下 CSS：

```css
.mod {
  background: blue;
  cursor: default;
}
```

那么我们可以编写：

```javascript
const modWidth = 70;

$("div").one("click", function() {
  $(this).innerHeight(modWidth).addClass("mod");
});
```

在点击 `div` 时设置其内宽度。

## `:input` 选择器

`:input` 选择器允许我们选择所有 `input`、`textarea`、`select` 和 `button` 元素。

例如，如果我们有以下代码：

```html
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="image">
  <input type="password">
  <input type="radio">
  <input type="reset">
  <input type="submit">
  <input type="text">

  <select>
    <option>Option</option>
  </select>

  <textarea></textarea>
  <button>Button</button>
</form>
```

那么我们可以编写：

```javascript
const allInputs = $(":input");

console.log(allInputs);
```



获取表单中的所有元素。

## `.insertAfter()`

`.insertAfter()` 方法将匹配元素集合中的每个元素插入到目标元素之后。

例如，如果我们有以下代码：

```html
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

那么我们可以通过编写以下代码在每个带有 `inner` 类的 `div` 之后添加一个元素：

```javascript
$("<p>Test</p>").insertAfter(".inner");
```

## `.insertBefore()`

我们可以调用 `insertBefore` 方法将匹配元素集合中的每个元素插入到目标元素之前。

例如，如果我们有以下代码：

```html
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

我们可以通过编写以下代码在每个带有 `inner` 类的 `div` 之前插入一个元素：

```javascript
$("<p>Test</p>").insertBefore(".inner");
```

## `jQuery.each()`

我们可以使用 `each` 方法遍历对象、数组以及具有 `length` 属性的类数组对象。

例如，如果我们有以下代码：

```javascript
$.each([52, 97], function(index, value) {
  console.log(index, value);
});
```

那么我们会记录数组中每个条目的 `index` 和 `value`。

## `jQuery.escapeSelector()`

我们可以使用 `escapeSelector` 方法转义 CSS 选择器中具有特殊含义的任何字符。

例如，我们可以编写：

```javascript
console.log($.escapeSelector("#target"));
```

返回转义后的字符串。

因此我们会看到输出：

```text
'#target'
```

## `jQuery.extend()`

`jQuery.extend()` 方法允许我们将两个或多个对象合并到第一个对象中。

例如，我们可以编写：

```javascript
const object1 = {
  apple: 0,
  banana: {
    weight: 52,
    price: 100
  },
  cherry: 97
};

const object2 = {
  banana: {
    price: 200
  },
  durian: 100
};

$.extend(object1, object2);
console.log(object1);
```

那么我们会得到：

```json
{
  "apple": 0,
  "banana": {
    "price": 200
  },
  "cherry": 97,
  "durian": 100
}
```

作为 `object1` 的值。

## `jQuery.fn.extend()`

`jQuery.fn.extend()` 方法允许我们将对象的内容合并到 jQuery 原型中，以添加新的 jQuery 实例方法。

例如，如果我们有以下代码：

```html
<label><input type="checkbox" name="foo"> Foo</label>
<label><input type="checkbox" name="bar"> Bar</label>
```

那么我们可以通过编写以下代码添加 `check` 和 `uncheck` 实例方法：

```javascript
jQuery.fn.extend({
  check() {
    return this.each(function() {
      this.checked = true;
    });
  },

  uncheck() {
    return this.each(function() {
      this.checked = false;
    });
  }
});

$("input[type='checkbox']").check();
```

它们分别将 `checked` 属性设置为 `true` 和 `false`。

现在我们可以像最后一行那样调用它来选中和取消选中复选框。

## `jQuery.fx.off`

`jQuery.fx.off` 方法全局禁用所有动画。

例如，如果我们有以下 HTML：

```html
<input type="button" value="Run">
<button>Toggle fx</button>
<div></div>
```

以及 CSS：

```css
div {
  width: 50px;
  height: 30px;
  margin: 5px;
  float: left;
  background: green;
}
```

那么我们可以通过编写以下代码切换 `div` 的动画效果：

```javascript
const toggleFx = function() {
  $.fx.off = !$.fx.off;
};

toggleFx();

$("button").click(toggleFx);

$("input").click(function() {
  $("div").toggle("slow");
});
```

`toggleFx` 方法切换动画状态。

然后我们在点击按钮时运行 `toggle` 方法。

## `jQuery.get()`

`jQuery.get()` 方法允许我们发起 GET 请求。

例如，我们可以编写：

```javascript
$.get("https://jsonplaceholder.typicode.com/posts/1", function(data) {
  console.log(data);
});
```

使用给定的 URL 发起 GET 请求。

回调函数的 `data` 参数包含响应数据。

## `jQuery.getJSON()`

`jQuery.getJSON()` 方法允许我们发起请求并从中获取 JSON 响应。

例如，我们可以编写：

```javascript
$.getJSON("https://jsonplaceholder.typicode.com/posts/1", function(data) {
  console.log(data);
});
```

像使用 `get` 方法一样发起请求。

## `jQuery.getScript()`

`jQuery.getScript()` 方法允许我们从服务器获取脚本。

例如，我们可以这样使用它：

```javascript
$.getScript(
  "https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js",
  function(data, textStatus, jqxhr) {
    console.log(data);
    console.log(textStatus);
    console.log(jqxhr.status);
  }
);
```

然后我们获取 `textStatus` 和 `jqxhr.status` 来获取请求状态。

`data` 包含响应数据。

## `.keypress()`

我们可以使用 `keypress` 方法来监听按键事件或触发它。

例如，如果我们有以下代码：

```html
<form>
  <fieldset>
    <input id="target" type="text" value="Hello there">
  </fieldset>
</form>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过编写以下代码监听输入框上的按键事件：

```javascript
$("#target").keypress(function() {
  console.log("Handler for .keypress() called.");
});
```

我们还可以在点击 ID 为 `other` 的 `div` 时触发 `keypress` 事件，代码如下：

```javascript
$("#target").keypress(function() {
  console.log("Handler for .keypress() called.");
});

$("#other").click(function() {
  $("#target").keypress();
});
```

## `.keyup()`

`.keyup()` 方法允许我们监听 `keyup` 事件或触发它。

例如，如果我们有以下代码：

```html
<form>
  <fieldset>
    <input id="target" type="text" value="Hello there">
  </fieldset>
</form>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过以下代码监听输入框上的 `keyup` 事件：

```javascript
$("#target").keyup(function() {
  console.log("Handler for .keypress() called.");
});
```

我们还可以在点击 ID 为 `other` 的 `div` 时触发 `keyup` 事件，代码如下：

```javascript
$("#target").keyup(function() {
  console.log("Handler for .keypress() called.");
});

$("#other").click(function() {
  $("#target").keyup();
});
```

## `:lang()` 选择器

`:lang` 选择器允许我们选择所有指定语言的元素。

例如，如果我们有以下 HTML：

```html
<div lang="en-us">
  red
  <div>
    white
    <div>and blue</div>
  </div>
</div>

<div lang="es-es">
  rojo
  <div>
    amarillo
    <div>y rojo</div>
  </div>
</div>
```

以及 CSS：

```css
.spain {
  background-color: red;
  color: #ff0;
}

.usa {
  background-color: red;
  color: #fff;
}
```

那么我们可以通过以下代码为具有不同 `lang` 属性值的 `div` 添加不同的类：

```javascript
$("div:lang(en-us)").addClass("usa");
$("div:lang(es-es)").addClass("spain");
```

## `.last()`

我们可以使用 `.last` 方法获取一组匹配元素中的最后一个元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过以下代码为最后一个 `li` 添加红色背景：

```javascript
$("li").last().css("background-color", "red");
```

我们获取所有 `li`，然后调用 `last` 获取最后一个。

## `:last-child` 选择器

`:last-child` 选择器选择所有作为父元素最后一个子元素的元素。

例如，如果我们有以下 HTML：

```html
<div>
  <span>John,</span>
  <span>Karl,</span>
  <span>Brandon,</span>
  <span>Sam</span>
</div>

<div>
  <span>James,</span>
  <span>Mary,</span>
  <span>Ralph,</span>
  <span>David</span>
</div>
```

以及 CSS：

```css
span.solast {
  text-decoration: line-through;
}
```

那么我们可以通过以下代码将每个 `div` 中的最后一个 `span` 设置为红色，并在鼠标悬停时添加删除线：

```javascript
$("div span:last-child")
  .css({
    color: "red",
    fontSize: "80%"
  })
  .hover(
    function() {
      $(this).addClass("solast");
    },
    function() {
      $(this).removeClass("solast");
    }
  );
```

## `:last-of-type` 选择器

我们可以使用 `:last-of-type` 选择器获取给定类型的最后一个元素。

例如，如果我们有以下 HTML：

```html
<div>
  <span>Corey,</span>
  <span>Yehuda,</span>
  <span>Adam,</span>
  <span>Todd</span>
</div>

<div>
  <span>James,</span>
  <span>Mary,</span>
  <span>Tim,</span>
  <b>Nobody</b>
</div>
```

以及 CSS：

```css
span.solast {
  text-decoration: line-through;
}
```

那么我们可以通过以下代码将每个 `div` 中的最后一个 `span` 设置为红色，并在鼠标悬停时添加删除线：

```javascript
$("span:last-of-type")
  .css({
    color: "red",
    fontSize: "80%"
  })
  .hover(
    function() {
      $(this).addClass("solast");
    },
    function() {
      $(this).removeClass("solast");
    }
  );
```

## `.length`

我们可以使用 `.length` 属性获取 jQuery 对象中的元素数量。

例如，如果我们有以下代码：

```html
<div></div>
```

那么我们可以通过以下代码添加一个 `div` 并获取 `div` 的总数：

```javascript
$(document.body).append($("<div>"));

const n = $("div").length;

console.log(n);
```

控制台应输出 2。

## `.load()`

`.load()` 方法允许我们从服务器加载数据，并将返回的 HTML 放入匹配的元素中。

例如，如果我们有以下代码：

```html
<div id="result"></div>
```

那么我们可以编写：

```javascript
$("#result").load("https://jsfiddle.net");
```

将 [`jsfiddle.net`](https://jsfiddle.net) 的内容加载到 ID 为 `result` 的 `div` 中。

## `.map()`

`.map()` 方法允许我们将每个项的值映射为一个新值。

例如，如果我们有以下代码：

```html
<form method="post" action="">
  <fieldset>
    <div>
      <label for="two">2</label>
      <input type="checkbox" value="2" id="two" name="number[]">
    </div>

    <div>
      <label for="four">4</label>
      <input type="checkbox" value="4" id="four" name="number[]">
    </div>

    <div>
      <label for="six">6</label>
      <input type="checkbox" value="6" id="six" name="number[]">
    </div>

    <div>
      <label for="eight">8</label>
      <input type="checkbox" value="8" id="eight" name="number[]">
    </div>
  </fieldset>
</form>
```

那么我们可以通过以下代码获取所有复选框的 ID，然后将它们连接成一个字符串：

```javascript
const str = $(":checkbox")
  .map(function() {
```



```javascript
return this.id;
})

.get()

.join();

console.log(str);
```

此时 `str` 的值为 `'two,four,six,eight'`。

## `.mousedown()`

`.mousedown()` 方法允许我们为 `mousedown` 事件添加事件监听器或触发它。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过以下代码监听 ID 为 `target` 的 `div` 上的 `mousedown` 事件：

```javascript
$("#target").mousedown(function() {
  console.log("Handler for .mousedown() called.");
});
```

此外，我们还可以在点击 ID 为 `other` 的 `div` 时触发 ID 为 `target` 的 `div` 上的 `mousedown` 事件，代码如下：

```javascript
$("#target").mousedown(function() {
  console.log("Handler for .mousedown() called.");
});

$("#other").click(function() {
  $("#target").mousedown();
});
```

## `.mouseenter()`

`.mouseenter()` 方法允许我们为 `mouseenter` 事件添加事件监听器或触发它。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过以下代码监听 ID 为 `target` 的 `div` 上的 `mouseenter` 事件：

```javascript
$("#target").mouseenter(function() {
  console.log("Handler for .mouseenter() called.");
});
```

此外，我们还可以在点击 ID 为 `other` 的 `div` 时触发 ID 为 `target` 的 `div` 上的 `mouseenter` 事件，代码如下：

```javascript
$("#target").mouseenter(function() {
  console.log("Handler for .mouseenter() called.");
});

$("#other").click(function() {
  $("#target").mouseenter();
});
```

## `.mouseleave()`

`.mouseleave()` 方法允许我们为 `mouseleave` 事件添加事件监听器或触发它。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过以下代码监听 ID 为 `target` 的 `div` 上的 `mouseleave` 事件：

```javascript
$("#target").mouseleave(function() {
  console.log("Handler for .mouseleave() called.");
});
```

此外，我们还可以在点击 ID 为 `other` 的 `div` 时触发 ID 为 `target` 的 `div` 上的 `mouseleave` 事件，代码如下：

```javascript
$("#target").mouseleave(function() {
  console.log("Handler for .mouseleave() called.");
});

$("#other").click(function() {
  $("#target").mouseleave();
});
```

## `.mousemove()`

`.mousemove()` 方法允许我们为 `mousemove` 事件添加事件监听器或触发它。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过以下代码监听 ID 为 `target` 的 `div` 上的 `mousemove` 事件：

```javascript
$("#target").mousemove(function() {
  console.log("Handler for .mouseleave() called.");
});
```

此外，我们还可以通过编写以下代码，在点击 ID 为 `other` 的 `div` 时，触发 ID 为 `target` 的 `mousedown` 事件：

```javascript
$("#target").mousemove(function() {
  console.log("Handler for .mouseleave() called.");
});

$("#other").click(function() {
  $("#target").mousemove();
});
```

## `.mouseout()`

`.mouseout()` 方法允许我们为 `mouseout` 事件添加事件监听器，或触发该事件。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过编写以下代码来监听 ID 为 `target` 的 `div` 上的 `mouswdown` 事件：

```javascript
$("#target").mouseout(function() {
  console.log("Handler for .mouseout() called.");
});
```

此外，我们还可以通过编写以下代码，在点击 ID 为 `other` 的 `div` 时，触发 ID 为 `target` 的 `div` 上的 `mousedown` 事件：

```javascript
$("#target").mouseout(function() {
  console.log("Handler for .mouseleave() called.");
});

$("#other").click(function() {
  $("#target").mouseout();
});
```

## `.mouseover()`

`.mouseover()` 方法允许我们为 `mouseover` 事件添加事件监听器，或触发该事件。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过编写以下代码来监听 ID 为 `target` 的 `div` 上的 `mouswdown` 事件：

```javascript
$("#target").mouseover(function() {
  console.log("Handler for .mouseover() called.");
});
```

此外，我们还可以通过编写以下代码，在点击 ID 为 `other` 的 `div` 时，触发 ID 为 `target` 的 `div` 上的 `mousedown` 事件：

```javascript
$("#target").mouseover(function() {
  console.log("Handler for .mouseover() called.");
});

$("#other").click(function() {
  $("#target").mouseover();
});
```

## `.mouseup()`

`.mouseup()` 方法允许我们为 `mouseup` 事件添加事件监听器，或触发该事件。

例如，如果我们有以下代码：

```html
<div id="target">
  Click here
</div>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以通过编写以下代码来监听 ID 为 `target` 的 `div` 上的 `mouswdown` 事件：

```javascript
$("#target").mouseup(function() {
  console.log("Handler for .mouseup() called.");
});
```

此外，我们还可以通过编写以下代码，在点击 ID 为 `other` 的 `div` 时，触发 ID 为 `target` 的 `div` 上的 `mouseup` 事件：

```javascript
$("#target").mouseup(function() {
  console.log("Handler for .mouseup() called.");
});

$("#other").click(function() {
  $("#target").mouseup();
});
```

## 多重属性选择器 `[name="value"][name2="value2"]`

我们可以使用多重属性选择器来选择具有多个属性的元素。

例如，如果我们有以下代码：

```html
<input id="man-news" name="man-news">

<input name="milkman">

<input id="letterman" name="new-letterman">

<input name="newmilk">
```

那么我们可以通过编写以下代码来获取 ID 为 `letterman` 且 `name` 属性值为 `new-letterman` 的输入框：

```javascript
$("input[id][name$='man']").val("only this one");
```

获取元素后，我们调用 `val` 来设置输入框的值。

## 多重选择器（`"selector1, selector2, selectorN"`）

多重选择器允许我们获取匹配任意给定选择器的元素。

例如，如果我们有以下代码：

```html
<div>div</div>

<p class="myClass">p class="myClass"</p>

<p class="notMyClass">p class="notMyClass"</p>

<span>span</span>
```

那么我们可以通过编写以下代码，为 `div`、`span` 以及 class 为 `myClass` 的 `p` 元素添加红色边框：

```javascript
$("div, span, p.myClass").css("border", "3px solid red");
```

## `.next()`

`.next()` 方法获取紧跟在给定元素之后的同级元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过编写以下代码，获取 class 为 `third-item` 的 `li` 元素紧邻的下一个 `li` 元素：

```javascript
$("li.third-item").next().css("background-color", "red");
```

然后我们调用 `css` 为其添加红色背景。

## 下一个相邻选择器（`"prev + next"`）

我们可以使用下一个相邻选择器来获取给定元素之后的下一个同级元素。

例如，如果我们有以下代码：

```html
<form>
  <label for="name">Name:</label>

  <input name="name" id="name">

  <fieldset>
    <label for="newsletter">Newsletter:</label>

    <input name="newsletter" id="newsletter">
  </fieldset>
</form>

<input name="none">
```

那么我们可以通过编写以下代码，获取 `label` 元素之后紧邻的 `input` 元素，并为其添加样式和设置值：

```javascript
$("label + input").css("color", "blue").val("Labeled!");
```

## 下一个兄弟选择器（`"prev ~ siblings"`）

下一个兄弟选择器允许我们选择所有跟在 `prev` 元素之后的同级元素。

这些兄弟元素必须具有相同的父元素。

例如，如果我们有以下代码：

```html
<div>div (doesn't match since before #prev)</div>

<span id="prev">span#prev</span>

<div>div sibling</div>

<div>
  div sibling
  <div id="small">div niece</div>
</div>

<span>span sibling (not div)</span>

<div>div sibling</div>
```

那么我们可以通过编写以下代码，获取所有跟在 ID 为 `prev` 的 `span` 元素之后的 `div` 元素：

```javascript
$("#prev ~ div").css("border", "3px groove blue");
```

我们调用 `css` 为匹配的元素添加蓝色边框。

## `.nextAll()`

`.nextAll()` 方法获取匹配元素集合中每个元素之后的所有同级元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过编写以下代码，获取 class 为 `third-item` 的 `li` 元素之后的所有 `li` 元素，并为它们添加红色背景：

```javascript
$("li.third-item").nextAll().css("background-color", "red");
```

## `.nextUntil()`

`.nextUntil()` 方法获取每个元素之后的所有同级元素，直到（但不包括）由选择器、DOM 节点或 jQuery 对象匹配的元素。

例如，如果我们有以下代码：

```html
<dl>
  <dt id="term-1">term 1</dt>
  <dd>definition 1-a</dd>
  <dd>definition 1-b</dd>
  <dd>definition 1-c</dd>
  <dd>definition 1-d</dd>

  <dt id="term-2">term 2</dt>
  <dd>definition 2-a</dd>
  <dd>definition 2-b</dd>
  <dd>definition 2-c</dd>

  <dt id="term-3">term 3</dt>
  <dd>definition 3-a</dd>
  <dd>definition 3-b</dd>
</dl>
```

那么我们可以通过编写以下代码，获取 ID 为 `term-2` 的 `dt` 元素之后直到（但不包括）ID 为 `term-3` 的 `dt` 元素之间的所有元素：

```javascript
$("#term-2")
  .nextUntil("dt")
  .css("background-color", "red");
```

然后我们为其添加红色背景。

## `.not()`

我们调用 `not` 来从匹配的元素集合中移除某些元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过编写以下代码，获取所有奇数位置的 `li` 元素：

```javascript
$("li").not(":nth-child(2n)").css("background-color", "red");
```

然后我们调用 `css` 为其添加红色背景。

## `jQuery.ready`

`jQuery.ready` 是一个 thenable 对象，当文档准备就绪时，它会 resolve。

例如，我们可以编写：

```javascript
(async () => {
  const data = await $.when(
    $.getJSON("https://jsonplaceholder.typicode.com/posts/1"),
    $.ready
  );

  console.log(data);
})();
```



我们调用`getJSON`来获取 JSON 数据。

然后我们调用`$.ready`来等待`document`准备就绪。

当两个操作都完成后，我们获取`data`。

## `jQuery.readyException()`

`jQuery.readyException`方法用于处理在 jQuery 包装的函数中同步抛出的错误。

例如，我们可以编写：

```javascript
jQuery.readyException = function(error) {
  console.error(error);
};
```

将`error`对象传递给`console.error`方法并记录它。

## `jQuery.removeData()`

`jQuery.removeData()`方法允许我们从元素中移除数据。

例如，如果我们有以下代码：

```html
<div></div>
```

那么我们可以使用`removeData`从`div`中移除数据：

```javascript
const div = $("div")[0];
```

```javascript
jQuery.data(div, "test1", "value");

console.log(jQuery.data(div, "test1"));

jQuery.removeData(div, "test1");

console.log(jQuery.data(div, "test1"));
```

我们获取`div`，然后调用`jQuery.data`来获取数据。

接着调用`removeData`来移除数据。

因此，第一个`console.log`输出`'value'`，第二个输出`undefined`。

## `jQuery.support`

`jQuery.support`属性包含一个对象，用于显示浏览器支持哪些特性。

## `jQuery.uniqueSort()`

`jQuery.uniqueSort()`方法会对 DOM 元素数组进行原地排序，并移除重复项。

例如，如果我们有以下 HTML：

```html
<div></div>
<div class="dup"></div>
<div class="dup"></div>
<div class="dup"></div>
<div></div>
```

那么我们可以这样使用它：

```javascript
let divs = $("div").get();

divs = divs.concat($(".dup").get());

console.log(divs.length);

divs = jQuery.uniqueSort(divs);

console.log(divs.length);
```

我们获取所有`div`，然后将 class 为`dup`的`div`添加到 div 元素列表中。

接着调用`uniqueSort`进行排序并移除重复项。

因此，第一个`console.log`输出 8，第二个输出 5。

## `jQuery.when()`

我们可以使用`jQuery.when()`方法，基于零个或多个 thenable 对象来运行回调函数。

例如，我们可以这样写：

```javascript
(async () => {
  const data = await $.when(
    $.ajax("https://jsonplaceholder.typicode.com/posts")
  );

  console.log(data);
})();
```

发起一个 GET 请求，然后输出数据。

## `.keydown()`

`.keydown()`方法允许我们监听元素上的 keydown 事件。

例如，如果我们有以下 HTML：

```html
<form>
  <input id="target" type="text" value="Hello there">
</form>

<div id="other">
  Trigger the handler
</div>
```

那么我们可以这样监听输入元素上的`keydown`事件：

```javascript
$("#target").keydown(function() {
  console.log("Handler for .keydown() called.");
});
```

我们也可以用它来触发另一个元素上的`keydown`事件。

例如，使用相同的 HTML，我们可以这样写：

```javascript
$("#target").keydown(function() {
  console.log("Handler for .keydown() called.");
});

$("#other").click(function() {
  $("#target").keydown();
});
```

当点击 ID 为`other`的`div`时，触发输入框上的`keydown`事件。本文中，我们将探讨如何在 Web 应用中使用 jQuery。

## `.parents()`

`.parents()`方法允许我们获取当前匹配元素集合中每个元素的祖先元素。

我们可以通过选择器来过滤这些祖先元素。

例如，如果我们有以下 HTML：

```html
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

那么我们可以通过以下代码获取 class 为`item-a`的`li`的所有祖先元素：

```javascript
$("li.item-a").parents().css("background-color", "red");
```

然后为它们添加红色背景。

## `.parentsUntil()`

`.parentsUntil()`方法获取当前匹配元素集合中每个元素的祖先元素，直到（但不包括）由选择器、DOM 节点或 jQuery 对象匹配的元素。

例如，如果我们有以下 HTML：

```html
<ul class="level-1 yes">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2 yes">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

那么我们可以获取 class 为`item-a`的`li`的祖先元素，直到（但不包括）class 为`level-1`的`li`，并为它们添加背景色：

```javascript
$("li.item-a")
  .parentsUntil(".level-1")
  .css("background-color", "red");
```

## `:password`选择器

`:password`选择器允许我们选择所有`type`为 password 的元素。

例如，如果我们有以下 HTML：

```html
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
```

那么我们可以这样写：

```javascript
$("input:password").css({
  background: "yellow",
  border: "3px red solid"
});
```

为`type`为 password 的输入框添加黄色背景和红色边框。

## `.position()`

`.position()`方法获取匹配元素集合中第一个元素相对于其偏移父元素的当前坐标。

例如，如果我们有以下 HTML：

```html
<p>Hello</p>
```

那么我们可以通过以下代码获取`p`元素的位置：

```javascript
const p = $("p").first();
const position = p.position();

console.log(position);
```

得到的结果为：

```javascript
{top: 0, left: 8}
```

作为`position`的值。

## `.prepend()`

`.prepend()`方法将内容插入到匹配元素集合中每个元素的开头。

例如，如果我们有以下 HTML：

```html
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

那么我们可以通过以下代码在每个 class 为`inner`的`div`的文本节点之前添加一个元素：

```javascript
$(".inner").prepend("<p>Test</p>");
```

## `.prependTo()`

`.prependTo()`方法允许我们将一个元素前置到匹配元素集合中。

例如，如果我们有以下 HTML：

```html
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

那么我们可以通过以下代码将一个`p`元素作为子元素前置到每个 class 为`inner`的`div`中：

```javascript
$("<p>Test</p>").prependTo(".inner");
```

## `jQuery.merge()`

`jQuery.merge()`方法将两个数组的内容合并到第一个数组中。

例如，我们可以这样使用它：

```javascript
const arr = $.merge([0, 1, 2], [2, 3, 4]);

console.log(arr);
```

那么`arr`的值为：

```javascript
[0, 1, 2, 2, 3, 4]
```

## `jQuery.noConflict()`

`jQuery.noConflict()`方法放弃 jQuery 对`$`变量的控制。

我们可以这样使用它：

```javascript
jQuery.noConflict();

jQuery("div p").hide();
```

调用`noConflict`。

然后我们可以用`jQuery`代替`$`来调用 jQuery。

## `jQuery.noop()`

`jQuery.noop()`方法返回一个空函数。

## `jQuery.param()`

`jQuery.param()`方法将对象的键值对转换为查询字符串。

例如，我们可以这样写：

```javascript
const params = {
  width: 1680,
  height: 1050
};

const str = jQuery.param(params);

console.log(str);
```

那么`str`的值为`'width=1680&height=1050'`。

## `jQuery.parseHTML()`

`jQuery.parseHTML()`方法允许我们将字符串解析为 DOM 节点数组。

例如，如果我们有以下 HTML：

```html
<div id="log">
  <h3>Content:</h3>
</div>
```

那么我们可以通过以下代码将解析后的 HTML 追加到 ID 为`log`的`div`中：

```javascript
const str = "hello, <b>my name is</b> jQuery.";
const html = $.parseHTML(str);

$("#log").append(html);
```

我们使用`$.parseHTML`解析 HTML 字符串，然后调用`append`追加内容。

## `jQuery.parseJSON()`

我们可以使用`jQuery.parseJSON()`方法将 JSON 字符串解析为对象。

例如，如果我们有以下代码：

```javascript
const obj = jQuery.parseJSON('{ "name": "John" }');

console.log(obj.name === "John");
```

那么我们将字符串解析为`obj`对象。

`obj.name`的值为`'John'`。

因此`console.log`输出`true`。

## `jQuery.parseXML()`

`jQuery.parseXML()`方法允许我们将 XML 解析为对象。

例如，我们可以这样使用它：

```javascript
const xml = "<rss version='2.0'><channel><title>RSS Title</title></channel></rss>",
  xmlDoc = $.parseXML(xml),
  $xml = $(xmlDoc),
  title = $xml.find("title");

console.log(title.text());
```

我们使用 XML 字符串调用`parseXML`。

然后将其放入`$`函数中，以便调用`find`来查找我们想要的元素。

接着，我们可以通过`text`方法获取匹配元素的文本内容。

## `jQuery.post()`

`jQuery.post()`方法允许我们向指定 URL 发起 POST 请求。

例如，我们可以编写：

```javascript
const jqxhr = $.post(
  "https://jsonplaceholder.typicode.com/posts",
  {
    title: "title",
    body: "body"
  },
  function() {
    console.log("success");
  },
  "json"
)
  .done(function() {
    console.log("second success");
  })
  .fail(function() {
    console.log("error");
  })
  .always(function() {
    console.log("finished");
  });

jqxhr.always(function() {
  console.log("second finished");
});
```

来发起一个 POST 请求。

第二个参数是我们要随请求发送的表单数据键值对。

`done`回调在请求成功时被调用。

`fail`回调在请求失败时被调用。

`always`回调在请求完成时被调用，无论结果如何。

## `jQuery.queue()`

`jQuery.queue()`方法用于显示或操作要在匹配元素上运行的函数队列。

例如，如果我们有以下 HTML：

```html
<div></div>
```

以及 CSS：

```css
div {
  margin: 3px;
  width: 40px;
  height: 40px;
  position: absolute;
  left: 0px;
  top: 30px;
  background: green;
  display: none;
}

div.newcolor {
  background: blue;
}

span {
  color: red;
}
```

那么我们可以通过编写以下代码来对`div`进行动画：

```javascript
$("div")
  .show("slow")
  .animate({
    left: "+=200"
  }, 2000)
  .slideToggle(1000)
  .slideToggle("fast")
  .animate({
    left: "-=200"
  }, 1500)
  .hide("slow")
  .show(1200);

console.log(jQuery.queue($("div")[0], "fx"));
```



我们获取 `div` 并将其作为 `jQuery.queue` 的参数，以检查队列中的项目。

## `:not()` 选择器

`:not` 选择器选取所有不匹配给定选择器的元素。

例如，如果我们有以下内容：

```html
<div>
  <input type="checkbox" name="a">
  <span>Mary</span>
</div>

<div>
  <input type="checkbox" name="b">
  <span>lcm</span>
</div>

<div>
  <input type="checkbox" name="c" checked="checked">
  <span>Peter</span>
</div>
```

那么我们可以通过编写以下代码，为所有未选中的复选框添加黄色背景：

```javascript
$("input:not(:checked) + span").css("background-color", "yellow");
```

## `:nth-child()` 选择器

`:nth-child()` 选择器允许我们选取所有作为其父元素第 n 个子元素的元素。

例如，如果我们有以下内容：

```html
<div>
  <ul>
    <li>John</li>
    <li>Karl</li>
    <li>Brandon</li>
  </ul>
</div>

<div>
  <ul>
    <li>Sam</li>
  </ul>
</div>

<div>
  <ul>
    <li>John</li>
    <li>Jane</li>
    <li>Ralph</li>
    <li>David</li>
  </ul>
</div>
```

那么我们可以通过编写以下代码，为每个 `ul` 中的第二个 `li` 添加一个 `span`：

```javascript
$("ul li:nth-child(2)").append("<span> - 2nd!</span>");
```

## `:nth-last-child()` 选择器

`:nth-last-child` 选择器允许我们选取所有作为其父元素倒数第 n 个子元素的元素。

例如，如果我们有以下内容：

```html
<div>
  <ul>
    <li>John</li>
    <li>Karl</li>
    <li>Brandon</li>
  </ul>
</div>

<div>
  <ul>
    <li>Sam</li>
  </ul>
</div>

<div>
  <ul>
    <li>John</li>
    <li>Jane</li>
    <li>Ralph</li>
    <li>David</li>
  </ul>
</div>
```

那么我们可以获取每个 `ul` 中倒数第二个 `li`，并为其添加一个子 `span`，通过编写：

```javascript
$("ul li:nth-last-child(2)").append("<span> - 2nd to last!</span>");
```

## `:nth-last-of-type()` 选择器

`:nth-last-of-type` 选择器允许我们获取指定类型的最后一个元素。

例如，如果我们有以下内容：

```html
<div>
  <ul>
    <li>John</li>
    <li>Karl</li>
    <li>Brandon</li>
  </ul>
</div>

<div>
  <ul>
    <li>Sam</li>
  </ul>
</div>

<div>
  <ul>
    <li>John</li>
    <li>Jane</li>
    <li>Ralph</li>
    <li>David</li>
  </ul>
</div>
```

那么我们可以获取 `ul` 中倒数第二个 `li`，并在其中添加一个 `span`，通过编写：

```javascript
$("ul li:nth-last-of-type(2)").append("<span> - 2nd to last!</span>");
```

## `:nth-of-type()` 选择器

`:nth-of-type` 选择器选取所有作为其父元素第 n 个子元素且与同元素名称的兄弟元素相关的元素。

例如，如果我们有以下内容：

```html
<div>
  <span>John</span>,
  <b>Kim</b>,
  <span>Adam</span>,
  <b>Rafael</b>,
  <span>Oleg</span>
</div>

<div>
  <b>Dave</b>,
  <span>Ann</span>
</div>

<div>
  <i><span>Maurice</span></i>,
  <span>Richard</span>,
  <span>Ralph</span>,
  <span>Jason</span>
</div>
```

那么我们可以获取第二个兄弟 `span`，并向其中添加另一个 `span`，通过编写：

```javascript
$("span:nth-of-type(2)")
  .append("<span> is 2nd sibling span</span>")
  .addClass("nth");
```

## `.odd()`

我们可以使用 `odd` 选择器将匹配元素集缩减为其中的奇数元素。

例如，如果我们有以下内容：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过编写以下代码，选择索引为奇数的 `li`：

```javascript
$("li").odd().css("background-color", "red");
```

由于索引从 0 开始，我们为第 2 个和第 4 个 `li` 添加了红色背景。

## `.off()`

`.off()` 方法用于移除事件处理程序。

例如，如果我们有以下内容：

```html
<button id="theone">Does nothing...</button>
<button id="bind">Add Click</button>
<button id="unbind">Remove Click</button>
<div style="display:none;">Click!</div>
```

那么我们可以通过编写以下代码，使用 `off` 方法移除 `click` 处理程序：

```javascript
function flash() {
  $("div").show().fadeOut("slow");
}

$("#bind").click(function() {
  $("body")
    .on("click", "#theone", flash)
    .find("#theone")
    .text("Can Click!");
});

$("#unbind").click(function() {
  $("body")
    .off("click", "#theone", flash)
    .find("#theone")
    .text("Does nothing...");
});
```

ID 为 `unbind` 的按钮的点击监听器使用了 `off` 方法，将 `flash` 函数作为 `body` 的 `click` 处理程序移除。

## `.offset()`

`.offset()` 方法获取匹配元素集中第一个元素相对于文档的当前坐标。

例如，如果我们有以下内容：

```html
<p>Hello</p>
<p>2nd Paragraph</p>
```

那么我们可以通过编写以下代码，获取最后一个 `p` 元素的偏移量：

```javascript
const p = $("p").last();
const offset = p.offset();
console.log(offset);
```

然后我们得到：

```json
{
  "top": 50,
  "left": 8
}
```

作为 `offset` 的值。

## `.offsetParent()`

`.offsetParent()` 方法获取最近的已定位祖先元素。

例如，如果我们有以下内容：

```html
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii" style="position: relative;">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

那么我们可以通过编写以下代码，获取类为 `item-a` 的 `li` 的父元素，并为其添加背景：

```javascript
$("li.item-a").offsetParent().css("background-color", "red");
```

## `.on()`

`.on()` 方法为选定的元素附加一个或多个事件的事件处理函数。

例如，如果我们有以下内容：

```html
<p>Has an attached custom event.</p>
<button>Trigger custom event</button>
<span style="display:none;"></span>
```

那么我们可以通过编写以下代码，在点击按钮时触发一个自定义事件：

```javascript
$("p").on("myCustomEvent", function(event, myName) {
  $(this).text(`${myName}, hi there`);

  $("span")
    .stop()
    .css("opacity", 1)
    .text(`myName = ${myName}`)
    .fadeIn(30)
    .fadeOut(1000);
});

$("button").click(function() {
  $("p").trigger("myCustomEvent", ["John"]);
});
```

我们调用 `trigger`，第一个参数是事件名称，第二个参数是一个数组，包含我们想要随事件发送的数据。

要监听 `myCustomEvent` 事件，我们调用 `on`，第一个参数是相同的事件名称。

第二个参数是一个回调函数，在事件触发时运行。

`myName` 的值是 `'John'`，所以我们看到它被添加到了 `p` 元素中。

## `.one()`

`.one()` 方法为元素上的事件附加一个处理程序。

该处理程序在每个元素上，针对每种事件类型，最多运行一次。

例如，如果我们有以下代码：

```html
<p id="foo">foo</p>
```

那么我们可以这样写：

```javascript
$("#foo").one("click mouseover", function(event) {
  alert("The " + event.type + " event happened!");
});
```

使用 `one` 方法为 ID 为 `foo` 的 `p` 元素上的 `click` 和 `mouseover` 事件添加监听器。

## `:only-child` 选择器

`:only-child` 选择器选取所有作为其父元素唯一子元素的元素。

例如，如果我们有以下代码：

```html
<div>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>

<div>
  None
</div>

<div>
  <button>Sibling</button>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>
```

那么我们可以通过编写以下代码，为 `div` 中唯一的按钮添加边框并更改文本：

```javascript
$("div button:only-child").text("Alone").css("border", "2px blue solid");
```

因此，第二个和最后一个 `div` 中的按钮文本会被更改，并添加边框。

## `:only-of-type` 选择器

我们可以使用 `:only-of-type` 选择器选取所有没有相同元素名称兄弟元素的元素。

例如，如果我们有以下代码：

```html
<div>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>

<div>
  None
</div>

<div>
  <button>Sibling</button>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>
```

那么我们可以通过编写以下代码，获取 `div` 中唯一的按钮：

```javascript
$("button:only-of-type").text("Alone").css("border", "2px blue solid");
```

然后更改它们的文本并添加边框。

## `.outerHeight()`

`.outerHeight()` 方法允许我们获取计算后的外部高度，包括内边距、边框，以及可选的边距，适用于匹配元素集合中的第一个元素。

它也可以用于设置每个匹配元素的外部高度。

例如，如果我们有以下代码：

```html
<p>Hello</p>
```

那么我们可以通过编写以下代码，获取包含边距的外部高度：

```javascript
const p = $("p").first();
console.log(p.outerHeight(true));
```

`true` 表示包含边距。

如果我们有以下代码：

```html
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

那么我们可以通过编写以下代码，在点击 `div` 时设置其外部高度：

```javascript
const modHeight = 60;

$("div").one("click", function() {
  $(this).outerHeight(modHeight);
});
```

## `.outerWidth()`

`.outerWidth()` 方法获取当前计算后的外部宽度，包括内边距、边框，以及可选的边距，适用于匹配元素集合中的第一个元素。

它也可以用于设置所有匹配元素的外部宽度。

它也可以用于设置每个匹配元素的外部高度。

例如，如果我们有以下代码：

```html
<p>Hello</p>
```

那么我们可以通过编写以下代码，获取包含边距的外部宽度：

```javascript
const p = $("p").first();
console.log(p.outerWidth(true));
```

`true` 表示包含边距。

如果我们有以下 HTML：

```html
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

以及 CSS：

```css
.mod {
  background: blue;
  cursor: default;
}
```

那么我们可以通过编写以下代码，在点击 `div` 时设置其外部宽度：

```javascript
const modHeight = 60;

$("div").one("click", function() {
  $(this).outerWidth(modHeight).addClass("mod");;
});
```

我们调用 `addClass` 来添加带有蓝色背景的 `mod` 类。

## `.parent()`

`.parent()` 方法允许我们获取给定元素的父元素。

例如，如果我们有以下代码：

```html
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>



```html
<li class="item-3">3</li>
</ul>
</li>
<li class="item-c">C</li>
</ul>
</li>
<li class="item-iii">III</li>
</ul>
```

那么我们可以获取带有`item-a`类的`li`的父元素，并为其添加背景色：

```javascript
$("li.item-a").parent().css("background-color", "red");
```

## `:parent`选择器

`:parent`选择器允许我们获取给定元素的父元素。

例如，如果我们有以下代码：

```html
<table border="1">
  <tr>
    <td>Value 1</td>
    <td></td>
  </tr>
  <tr>
    <td>Value 2</td>
    <td></td>
  </tr>
</table>
```

那么我们可以通过编写以下代码，淡出`tr`：

```javascript
$("td:parent").fadeTo(1500, 0.3);
```

## `.prev()`

我们调用`.prev()`方法来获取匹配元素集合中每个元素的前一个兄弟元素。

如果提供了选择器，则仅当该兄弟元素匹配该选择器时才会被获取。

例如，如果我们有以下代码：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过编写以下代码，获取紧邻带有`third-item`类的`li`之前的`li`：

```javascript
$("li.third-item").prev().css("background-color", "red");
```

然后为其添加红色背景。

## `.prevAll()`

`.prevAll()`方法获取匹配元素集合中每个元素的所有前兄弟元素。

例如，如果我们有以下代码：

```html
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

那么我们可以通过编写以下代码，获取带有`third-item`类的`li`的所有前兄弟元素，并为它们添加背景色：

```javascript
$("li.third-item").prevAll().css("background-color", "red");
```

## `.prevUntil()`

`.prevUntil()`方法获取每个元素的所有前兄弟元素，直到但不包括由选择器、DOM 节点或 jQuery 对象匹配的元素。

例如，如果我们有以下代码：

```html
<dl>
  <dt id="term-1">term 1</dt>
  <dd>definition 1-a</dd>
  <dd>definition 1-b</dd>
  <dd>definition 1-c</dd>
  <dd>definition 1-d</dd>
  <dt id="term-2">term 2</dt>
  <dd>definition 2-a</dd>
  <dd>definition 2-b</dd>
  <dd>definition 2-c</dd>
  <dt id="term-3">term 3</dt>
  <dd>definition 3-a</dd>
  <dd>definition 3-b</dd>
</dl>
```

那么我们可以通过编写以下代码，获取 ID 为`term-2`的`dt`之前的所有`dd`，直到但不包括第一个`dt`：

```javascript
$("#term-2").prevUntil("dt")
  .css("background-color", "red");
```

并将它们的背景色设置为红色。

## `.promise()`

`.promise()`方法返回一个 Promise，用于观察绑定到集合的某种类型的所有操作何时完成。

例如，如果我们有以下代码：

```html
<button>Go</button>
<p>Ready...</p>
<div></div>
<div></div>
<div></div>
<div></div>
```

那么我们可以通过编写以下代码，在点击按钮时显示一些文本：

```javascript
$("button").on("click", function() {
  $("p").append("Started...");

  $("div").each(function(i) {
    $(this).fadeIn().fadeOut(1000 * (i + 1));
  });

  $("div").promise().done(function() {
    $("p").append(" Finished! ");
  });
});
```

我们遍历每个`div`，并使用`fadeIn`和`fadeOut`应用一些淡入淡出效果。

然后我们调用`promise`，并在所有方法调用完成时通过`promise().done()`方法运行代码。

## `.prop()`

我们可以使用`prop`方法获取属性值。

例如，如果我们有以下代码：

```html
<input id="check1" type="checkbox" checked="checked">
```

那么我们可以这样写：

```javascript
$("input").change(function() {
  const $input = $(this);

  console.log($input.prop("checked"));
}).change();
```

用于监听复选框输入的变化。

我们通过`prop`方法获取`checked`属性的值。

## `.pushStack()`

我们调用`pushStack`方法将一组 DOM 元素添加到 jQuery 栈中。

例如，如果我们有以下代码：

```html
<div>
  foo
</div>
```

那么我们可以通过编写以下代码来调用`pushStack`将`div`添加到栈中，然后将其移除：

```javascript
jQuery([])
  .pushStack(document.getElementsByTagName("div"))
  .remove()
  .end();
```

## `.queue()`

`.queue()`方法显示要在匹配元素上执行的函数队列。

例如，如果我们有以下代码：

```html
<p>队列长度为：<span></span></p>
<div></div>
```

那么我们可以通过编写以下代码来显示队列中的项目数量：

```javascript
const div = $("div");

function runIt() {
  div
    .show("slow")
    .animate({
      left: "+=200"
    }, 2000)
    .slideToggle(1000)
    .slideToggle("fast")
    .animate({
      left: "-=200"
    }, 1500)
    .hide("slow")
    .show(1200)
    .slideUp("normal", runIt);
}

function showIt() {
  const n = div.queue("fx");

  $("span").text(n.length);
  setTimeout(showIt, 100);
}

runIt();
showIt();
```

带有`'fx'`参数的`queue`方法用于获取动画队列中的项目数量。

## `:radio`选择器

`:radio`选择器允许我们获取单选按钮元素。

例如，如果我们有以下代码：

```html
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio" name="asdf">
  <input type="radio" name="asdf">
  <input type="reset">
  <input type="submit">
  <input type="text">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
```

那么我们可以通过编写以下代码为单选按钮添加背景和边框：

```javascript
$("form input:radio")
  .wrap("<span></span>")
  .parent()
  .css({
    background: "yellow",
    border: "3px red solid"
  });
```

## `.ready()`

`ready`方法指定一个在 DOM 完全加载后执行的函数。

我们可以这样写：

```javascript
$(document).ready(function() {
  // .ready() 的处理程序被调用。
});
```

或者：

```javascript
$(function() {
  // .ready() 的处理程序被调用。
});
```

当`document`加载完成后，我们在回调中执行代码。

## `.remove()`

`.remove()`方法允许我们移除 DOM 中的一组匹配元素。

例如，如果我们有以下代码：

```html
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">Goodbye</div>
</div>
```

那么我们可以通过编写以下代码来移除带有`hello`类的`div`：

```javascript
$(".hello").remove();
```

## `.removeAttr()`

`.removeAttr()`方法从匹配元素集合中的每个元素中移除一个属性。

例如，如果我们有以下代码：

```html
<input type="text" title="hello there">
<button>Change title</button>
```

那么我们可以通过编写以下代码在点击按钮时切换`title`属性的开启和关闭：

```javascript
const inputTitle = $("input").attr("title");

$("button").click(function() {
  const input = $(this).next();

  if (input.attr("title") === inputTitle) {
    input.removeAttr("title");
  } else {
    input.attr("title", inputTitle);
  }
});
```

## `.removeClass()`

我们可以调用`.removeClass()`方法来移除元素上的一个或多个类。

例如，如果我们有以下代码：

```html
<p class="blue under">Hello</p>
```

那么我们可以通过编写以下代码来移除`blue`和`under`类：

```javascript
$("p").removeClass("blue under");
```

## `.removeData()`

`.removeData()`方法用于移除之前存储的数据。

例如，如果我们有以下代码：

```html
<div>hello</div>
```

那么我们可以通过编写以下代码向`div`添加数据并移除它：

```javascript
$("div").data("test1", "value");

console.log($("div").data("test1"));

$("div").removeData("test1");

console.log($("div").data("test1"));
```

我们调用`removeData`通过键来移除一条数据。

## `.removeProp()`

我们可以对匹配元素集合使用`removeProp`属性。

例如，如果我们有以下代码：

```html
<p></p>
```

那么我们可以通过编写以下代码添加一个属性并移除它：

```javascript
const para = $("p");

para
  .prop("code", 1234)
  .append(String(para.prop("code")))
  .removeProp("code")
  .append(String(para.prop("code")));
```

第一个参数是属性名。

第二个参数是它的值。

`removeProp`接受我们要移除的属性名。

## `.replaceAll()`

我们调用`.replaceAll()`来用匹配元素集合替换每个目标元素。

例如，如果我们有以下代码：

```html
<div class="container">
  <div class="inner first">Hello</div>
  <div class="inner second">And</div>
  <div class="inner third">Goodbye</div>
</div>
```

那么我们可以通过编写以下代码将所有带有`inner`类的`div`替换为一个`h2`元素：

```javascript
$("<h2>New heading</h2>").replaceAll(".inner");
```

## `.replaceWith()`

`.replaceWith()`方法允许我们用提供的新内容替换匹配元素集合中的每个元素，并返回被移除的元素集合。

例如，如果我们有以下代码：

```html
<div class="container">
  <div class="inner first">Hello</div>
  <div class="inner second">And</div>
  <div class="inner third">Goodbye</div>
</div>
```

那么我们可以通过编写以下代码将带有`second`类的`div`替换为一个`h2`：

```javascript
$("div.second").replaceWith("<h2>New heading</h2>");
```

## `:reset`选择器

`:reset`选择器允许我们选择所有类型为 reset 的元素。

例如，如果我们有以下代码：

```html
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio">
  <input type="reset">
  <input type="submit">
  <input type="text">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
<div></div>
```

那么我们可以获取类型为`reset`的输入，并通过编写以下代码为其添加背景和边框：

```javascript
$("input:reset").css({
  background: "yellow",
  border: "3px red solid"
});
```

## `.resize()`

`.resize()`方法允许我们监听 resize JavaScript 事件，或在元素上触发该事件。

例如，我们可以这样使用它：

```javascript
$(window).resize(function() {
  console.log(".resize() 的处理程序被调用。");
});
```

当`window`调整大小时，我们会记录日志。

## `:root`选择器

`:root`选择器选择作为文档根元素的元素。

例如，我们可以这样使用它：

```javascript
console.log($(":root")[0].nodeName);
```

然后我们会看到`'HTML'`被记录。

## `.scroll()`

`.scroll()`方法将一个事件处理程序绑定到 scroll JavaScript 事件，或者允许我们触发该事件。

例如，如果我们有以下代码：

```html
<div id="target" style="overflow: scroll; width: 200px; height: 100px;">
```



Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

```html
</div>

<div id="other">

  触发处理程序

</div>
```

那么我们可以通过编写以下代码来监听 ID 为 `target` 的 `div` 上的滚动事件：

```javascript
$("#target").scroll(function() {

  console.log('正在滚动');

});
```

我们还可以通过编写以下代码在点击 ID 为 `other` 的 `div` 时触发滚动：

```javascript
$("#target").scroll(function() {

  console.log('正在滚动');

});

$("#other").click(function() {

  $("#target").scroll();

});
```

## `.scrollLeft()`

`.scrollLeft()` 方法获取匹配元素集合中第一个元素的滚动条当前水平位置。

例如，如果我们有以下代码：

```html
<p>Hello</p>

<p></p>
```

那么我们可以通过编写以下代码获取滚动条的水平位置：

```javascript
const p = $("p").first();

console.log(p.scrollLeft())
```

## `.scrollTop()`

`.scrollTop()` 方法获取匹配元素集合中第一个元素的滚动条当前垂直位置，或设置每个匹配元素的滚动条垂直位置。

例如，如果我们有以下代码：

```html
<p>Hello</p>

<p></p>
```

那么我们可以通过以下代码获取滚动条的垂直位置：

```javascript
const p = $("p").first();

$("p").last().text(p.scrollTop());
```

## `.select()`

`.select()` 方法为 `select` JavaScript 事件绑定一个事件处理函数。

我们也可以用它来触发元素上的事件。

例如，如果我们有以下代码：

```html
<form>

  <input id="target" type="text" value="Hello there">

</form>

<div id="other">

  Trigger the handler

</div>
```

我们可以通过以下代码监听输入框上触发的 `select` 事件：

```javascript
$("#target").select(function() {

  console.log("Handler for .select() called.");

});
```

此外，我们还可以在点击 ID 为 `other` 的 `div` 时触发输入框的 `select` 事件：

```javascript
$("#target").select(function() {

  console.log("Handler for .select() called.");

});

$("#other").click(function() {

  $("#target").select();

});
```

## `:selected` 选择器

`:selected` 选择器允许我们选择所有被选中的元素。

例如，如果我们有以下代码：

```html
<select name="garden" multiple="multiple">

  <option>Flowers</option>

  <option selected="selected">Shrubs</option>

  <option>Trees</option>

  <option selected="selected">Bushes</option>

  <option>Grass</option>

  <option>Dirt</option>

</select>

<div></div>
```

那么我们可以通过以下代码监听 `select` 元素上的 `select` 事件：

```javascript
$("select")

  .change(function() {

    let str = "";

    $("select option:selected").each(function() {

      str += $(this).text();

    });

    $("div").text(str);

  })

  .trigger("change");
```

我们在 `change` 回调中获取所有选中的项，并将它们放入 `div` 中。

## `.serialize()`

我们可以使用 `.serialize()` 方法将表单的值转换为键值对。

例如，如果我们有以下代码：

```html
<form>

  <select name="single">

    <option>Single</option>

    <option>Single2</option>

  </select>

  <br>

  <select name="multiple" multiple="multiple">

    <option selected="selected">Multiple</option>

    <option>Multiple2</option>

    <option selected="selected">Multiple3</option>

  </select>

  <br>

  <input type="checkbox" name="check" value="check1" id="ch1">

  <label for="ch1">check1</label>

  <input type="checkbox" name="check" value="check2" checked="checked" id="ch2">

  <label for="ch2">check2</label>

  <br>

  <input type="radio" name="radio" value="radio1" checked="checked" id="r1">

  <label for="r1">radio1</label>

  <input type="radio" name="radio" value="radio2" id="r2">

  <label for="r2">radio2</label>

</form>
```

那么我们可以通过以下代码在控件值改变时记录表单的值：

```javascript
const showValues = () => {

  const str = $("form").serialize();

  console.log(str);

}

$("input[type='checkbox'], input[type='radio']").on("click", showValues);

$("select").on("change", showValues);

showValues();
```

我们监听点击和 `change` 事件，并在表单发生任何操作时调用 `showValues` 方法。

那么 `str` 的值类似于：

```text
single=Single&multiple=Multiple&multiple=Multiple3&check=check2&radio=radio1
```

## `.serializeArray()`

我们可以调用 `serializeArray` 将一组表单元素编码为名称和值的数组。

例如，如果我们有以下代码：

```html
<form>

  <div><input type="text" name="a" value="1" id="a"></div>

  <div><input type="text" name="b" value="2" id="b"></div>

  <div><input type="hidden" name="c" value="3" id="c"></div>

  <div>

    <textarea name="d" rows="8" cols="40">4</textarea>

  </div>

  <div><select name="e">

      <option value="5" selected="selected">5</option>

      <option value="6">6</option>

      <option value="7">7</option>

    </select></div>

  <div>

    <input type="checkbox" name="f" value="8" id="f">

  </div>

  <div>

    <input type="submit" name="g" value="Submit" id="g">

  </div>

</form>
```

那么我们可以通过以下代码将表单值序列化为对象数组：

```javascript
$("form").submit(function(event) {

  console.log($(this).serializeArray());

  event.preventDefault();

});
```

当我们点击 Submit 时，会得到类似以下的内容：

```json
[
  {
    "name": "a",
    "value": "1"
  },
  {
    "name": "b",
    "value": "2"
  },
  {
    "name": "c",
    "value": "3"
  },
  {
    "name": "d",
    "value": "4"
  },
  {
    "name": "e",
    "value": "5"
  }
]
```

被记录。

## `.show()`

`show` 方法显示匹配的元素。

例如，如果我们有以下 HTML：

```html
<div id="clickme">

  Click here

</div>

<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

以及 CSS：

```css
img {

  display: none;

}
```

那么我们可以通过以下代码在点击“Click here”时调用 `show` 方法显示图片：

```javascript
$("#clickme").click(function() {

  $("#book").show("slow", function() {

    // Animation complete.

  });

});
```

## `.siblings()`

`siblings` 方法允许我们获取匹配元素集合中每个元素的兄弟元素。

我们可以选择性地向该方法传递一个选择器。

例如，如果我们有以下代码：

```html
<ul>

  <li>list item 1</li>

  <li>list item 2</li>

  <li class="third-item">list item 3</li>

  <li>list item 4</li>

  <li>list item 5</li>

</ul>
```

那么我们可以获取所有与 class 为 `third-item` 的 `li` 元素是兄弟关系的 `li` 元素，并为其添加背景色：

```javascript
$("li.third-item").siblings().css("background-color", "red");
```

## `.slice()`

`slice` 方法允许我们将匹配的元素集合缩减为索引范围指定的子集。

例如，如果我们有以下代码：

```html
<ul>

  <li>list item 1</li>

  <li>list item 2</li>

  <li>list item 3</li>

  <li>list item 4</li>

  <li>list item 5</li>

</ul>
```

那么我们可以通过以下代码获取从索引 2 开始到索引 4（不包括 4）的 `li` 元素：

```javascript
$("li").slice(2, 4).css("background-color", "red");
```

## `.slideDown()`

`.slideDown()` 方法以滑动动画显示匹配的元素。

例如，如果我们有以下 HTML：

```html
<div id="clickme">

  Click here

</div>

<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

以及 CSS：

```css
img {

  display: none;

}
```

那么我们可以通过以下代码在点击“Click here”时以向下滑动动画显示图片：

```javascript
$( "#clickme" ).click(function() {

  $( "#book" ).slideDown( "slow", function() {

    // Animation complete.

  });

});
```

## `.slideToggle()`

`.slideToggle()` 方法允许我们以滑动动画显示或隐藏匹配的元素。

例如，如果我们有以下 HTML：

```html
<div id="clickme">

  Click here

</div>

<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

以及 CSS：

```css
img {

  display: none;

}
```

那么我们可以通过以下代码在点击“Click here”时以滑动动画切换图片的显示状态：

```javascript
$( "#clickme" ).click(function() {

  $( "#book" ).slideToggle( "slow", function() {

    // Animation complete.

  });

});
```

## `.slideUp()`

`.slideUp()` 方法以滑动动画隐藏匹配的元素。

例如，如果我们有以下 HTML：

```html
<div id="clickme">

  Click here

</div>

<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

那么我们可以通过以下代码在点击“Click here”时以向上滑动动画隐藏图片：

```javascript
$( "#clickme" ).click(function() {

  $( "#book" ).slideUp( "slow", function() {

    // Animation complete.

  });

});
```

## `.stop()`

`stop` 方法用于停止匹配元素上当前正在运行的动画。

例如，如果我们有以下代码：

```html
<div id="hoverme">

  Hover me

  <img id="hoverme" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">

</div>
```

那么我们可以通过以下代码停止匹配元素上的动画：

```javascript
$("#hoverme").hover(function() {

  $(this).find("img").stop(true, true).fadeOut();

}, function() {

  $(this).find("img").stop(true, true).fadeIn();

});
```

当鼠标悬停在 ID 为 `hover` 的 `img` 上时，图片淡出；否则图片淡入。

## `.submit()`

`.submit()` 方法允许我们为 `submit` JavaScript 事件绑定事件处理程序，或在元素上触发该事件。

例如，如果我们有以下代码：

```html
<form id="target" action="destination.html">

  <input type="text" value="Hello there">
```



```html
<input type="submit" value="Go">

</form>

<div id="other">

  Trigger the handler

</div>
```

那么我们可以通过以下代码监听表单的 `submit` 事件：

```javascript
$("#target").submit(function(event) {

  console.log("Handler for .submit() called.");

  event.preventDefault();

});
```

我们也可以通过以下代码触发 `submit` 事件：

```javascript
$("#other").click(function() {

  $("#target").submit();

});
```

## `:submit` 选择器

`:submit` 选择器允许我们选择所有类型为 `submit` 的元素。

例如，如果我们有以下代码：

```html
<form id="target" action="destination.html">

  <input type="text" value="Hello there">

  <input type="submit" value="Go">

</form>
```

那么我们可以通过以下代码为提交按钮添加背景和边框：

```javascript
$("input:submit")

  .css({

    background: "yellow",

    border: "3px red solid"

  })

  .end();
```

## `:target` 选择器

`:target` 选择器用于选择文档 URI 的片段标识符所指示的目标元素。

例如，如果我们访问 [`example.com/#foo`](https://medium.com/r/?url=https%3A%2F%2Fexample.com%2F%23foo)，那么 `$("p:target")` 会选择 ID 为 `foo` 的 `p` 元素。

## `.text()`

`.text()` 方法获取匹配元素集合中每个元素（包括其后代）的合并文本内容。

例如，如果我们有以下代码：

```html
<p><b>Test</b> Paragraph.</p>

<p></p>
```

那么如果我们编写：

```javascript
console.log($("p").first().text())
```

控制台会输出 `'Test Paragraph.'`。

## `:text` 选择器

`:text` 选择器允许我们选择所有类型为 `text` 的 `input` 元素。

例如，如果我们有以下代码：

```html
<form id="target" action="destination.html">

  <input type="text" value="Hello there">

  <input type="submit" value="Go">

</form>

<div id="other">

  Trigger the handler

</div>
```

那么我们可以通过以下代码为文本输入框添加背景和边框：

```javascript
$("form input:text").css({

  background: "yellow",

  border: "3px red solid"

});
```

## `.toArray()`

`.toArray()` 方法将 jQuery 集合中包含的所有元素以数组形式返回。

例如，如果我们有以下代码：

```html
<div>One</div>

<div>Two</div>

<div>Three</div>
```

那么我们可以通过以下代码获取 `div` 并将其放入数组：

```javascript
console.log($("div").toArray());
```

## `.toggle()`

`.toggle()` 方法用于显示或隐藏匹配的元素。

例如，如果我们有以下代码：

```html
<div id="clickme">

  Click here

</div>

<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

那么我们可以通过以下代码在点击“Click here”按钮时让图片在显示和隐藏之间切换：

```javascript
$("#clickme").click(function() {

  $("#book").toggle("slow", function() {

    // Animation complete.

  });

});
```

## `.toggleClass()`

`.toggleClass()` 方法允许我们在匹配元素集合中的每个元素上添加或删除一个或多个类。

例如，如果我们有以下 HTML：

```html
<p class="blue">Click to toggle</p>
```

以及 CSS：

```css
p {

  margin: 4px;

  font-size: 16px;

  font-weight: bolder;

  cursor: pointer;

}

.blue {

  color: blue;

}

.highlight {

  background: yellow;

}
```

那么我们可以通过以下代码在 `p` 元素上切换 `highlight` 类：

```javascript
$("p").click(function() {

  $(this).toggleClass("highlight");

});
```

## `.trigger()`

`.trigger()` 方法会运行所有附加到匹配元素上、针对给定事件类型的处理程序和行为。

例如，如果我们有以下代码：

```html
<button>Button #1</button>

<button>Button #2</button>
```

那么我们可以通过以下代码在点击第二个按钮时触发第一个按钮的点击事件：

```javascript
$("button").first().click(function() {

  console.log('first button clicked');

});

$("button").last().click(function() {

  $("button").first().trigger("click");

});
```

## `.triggerHandler()`

`.triggerHandler()` 方法允许我们运行所有附加到元素某个事件上的处理程序。

例如，如果我们有以下代码：

```html
<button id="new">.triggerHandler( "focus" )</button><br><br>

<input type="text" value="To Be Focused">
```

那么我们可以通过以下代码在点击按钮时触发 `focus` 事件：

```javascript
$("#new").click(function() {

  $("input").triggerHandler("focus");

});

$("input").focus(function() {

  $("<span>Focused!</span>").appendTo("body").fadeOut(1000);

});
```

点击按钮时，输入框获得焦点，并显示 `Focused!` 文本。

## `.unbind()`

`.unbind()` 方法用于移除元素上之前绑定的事件处理程序。

例如，如果我们有以下代码：

```html
<button id="bind">Bind Click</button>

<button id="unbind">Unbind Click</button>

<div id="theone"></div>
```

那么我们可以通过以下代码为 ID 为 `theone` 的 `div` 绑定和解绑点击处理程序：

```javascript
function aClick() {

  $("div").show().fadeOut("slow");

}

$("#bind").click(function() {

  $("#theone")

    .bind("click", aClick)

    .text("Can Click!");

});

$("#unbind").click(function() {

  $("#theone")

    .unbind("click", aClick)

    .text("Does nothing...");

});
```

我们在按钮的 `click` 处理程序中为 `div` 绑定和解绑点击事件。

## `.undelegate()`

`.undelegate()` 方法用于从所有匹配当前选择器（基于根元素）的元素上移除事件处理程序。

例如，如果我们有以下代码：

```html
<button id="bind">Bind Click</button>

<button id="unbind">Unbind Click</button>

<div id="theone"></div>
```

那么我们可以通过以下代码为 ID 为 `theone` 的 `div` 绑定和解绑 `click` 处理程序：

```javascript
function aClick() {

  $("div").show().fadeOut("slow");

}

$("#bind").click(function() {

  $("body")

    .delegate("#theone", "click", aClick)

    .find("#theone")

    .text("Can Click!");

});

$("#unbind").click(function() {

  $("body")

    .undelegate("#theone", "click", aClick)

    .find("#theone")

    .text("Does nothing...");

});
```

## `.unwrap()`

`.unwrap()` 方法用于从 DOM 中移除匹配元素集合的父元素。

例如，如果我们有以下代码：

```html
<button>wrap/unwrap</button>

<p>Hello</p>

<p>World</p>
```

我们可以通过以下代码在 `p` 元素周围切换 `div` 的包裹和解除包裹：

```javascript
const pTags = $("p");

$("button").click(function() {

  if (pTags.parent().is("div")) {

    pTags.unwrap();

  } else {

    pTags.wrap("<div></div>");

  }

})
```

`wrap` 会将每个 `p` 元素分别包裹在自己的 `div` 中。

## `.val()`

`.val()` 方法获取匹配元素集合中第一个元素的当前值。我们也可以用它来设置每个匹配元素的值。

例如，如果我们有以下代码：

```html
<select id="single">

  <option>Single</option>

  <option>Single2</option>

</select>

<select id="multiple" multiple="multiple">

  <option selected="selected">Multiple</option>

  <option>Multiple2</option>

  <option selected="selected">Multiple3</option>

</select>
```

那么我们可以通过以下代码获取 `select` 元素中选中的值：

```javascript
function displayVals() {

  const singleValues = $("#single").val();

  const multipleValues = $("#multiple").val() || [];

  console.log(singleValues, multipleValues)

}

$("select").change(displayVals);
```

例如，如果我们有：

```html
<input type="text" value="some text">
```

然后，我们可以通过编写以下代码在输入时获取输入框的值：

```javascript
$("input")

  .keyup(function() {

    const value = $(this).val();

    console.log(value);

  })

  .keyup();
```

## `:visible` 选择器

`:visible` 选择器允许我们选择所有可见的元素。

例如，如果我们有以下 HTML：

```html
<button>Show hidden</button>

<div></div>

<div class="starthidden"></div>

<div></div>

<div></div>

<div style="display:none;"></div>
```

以及 CSS：

```css
div {

  width: 50px;

  height: 40px;

  margin: 5px;

  border: 3px outset green;

  float: left;

}

.starthidden {

  display: none;

}
```

然后，我们可以通过编写以下代码在点击按钮时显示所有隐藏的 `div`：

```javascript
$("div:visible").click(function() {

  $(this).css("background", "yellow");

});

$("button").click(function() {

  $("div:hidden").show("fast");

});
```

当我们点击可见的 `div` 时，会看到黄色背景。

## `.width()`

`.width()` 方法获取匹配元素集合中第一个元素的当前计算宽度，或设置每个匹配元素的宽度。

例如，我们可以编写：

```javascript
console.log($(window).width());
```

来记录窗口的宽度。

要设置以下 HTML 中 `div` 的宽度：

```html
<div>d</div>

<div>d</div>

<div>d</div>

<div>d</div>

<div>d</div>
```

以及 CSS：

```css
div {

  width: 70px;

  height: 50px;

  float: left;

  margin: 5px;

  background: red;

  cursor: pointer;

}
```

我们可以通过编写以下代码为 `div` 添加点击处理程序并更改其宽度：

```javascript
const modWidth = 50;

$("div").one("click", function() {

  $(this).width(modWidth)

});
```

## `.wrap()`

`.wrap()` 方法允许我们用包装元素包裹一个元素。

例如，如果我们有：

```html
<div class="container">

  <div class="inner">Hello</div>

  <div class="inner">Goodbye</div>

</div>
```

然后，我们可以通过编写以下代码，用类名为 `new` 的 `div` 包裹每个类名为 `inner` 的 `div`：

```javascript
$(".inner").wrap("<div class='new'></div>");
```

## `.wrapAll()`

`.wrapAll()` 方法允许我们在匹配元素集合中的所有元素周围包裹一个 HTML 结构。

例如，如果我们有：

```html
<div class="container">

  <div class="inner">Hello</div>

  <div class="inner">Goodbye</div>

</div>
```

然后，我们可以通过编写以下代码，用类名为 `new` 的 `div` 包裹所有类名为 `inner` 的 `div`：

```javascript
$(".inner").wrapAll("<div class='new' />");
```

## `.wrapInner()`

我们可以使用 `wrapInner` 方法在匹配元素集合中每个元素的内容周围包裹一个 HTML 结构。

例如，如果我们有：

```html
<div class="container">

  <div class="inner">Hello</div>

  <div class="inner">Goodbye</div>

</div>
```

然后，我们可以通过编写以下代码，用类名为 `new` 的 `div` 包裹每个类名为 `inner` 的 `div` 的内容：

```javascript
$(".inner").wrapInner("<div class='new'></div>");
```

# 结论

JavaScript 是世界上最流行的编程语言之一。要有效地使用它，我们需要了解它的基础知识。

它拥有任何语言的所有基本特性。

它也是网络的语言。

我们可以使用 jQuery 操作 DOM、发起 Ajax 请求等。
