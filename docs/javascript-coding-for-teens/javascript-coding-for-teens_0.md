
# 青少年 JavaScript 编程指南

版权 © 2021 by Rockridge Press, Emeryville, California

未经出版商事先书面许可，本书的任何部分不得以任何形式或通过任何手段（电子、机械、复印、录音、扫描或其他方式）进行复制、存储在检索系统中或传输，但根据 1976 年《美国版权法》第 107 节或第 108 节允许的除外。向出版商申请许可，请发送至：Permissions Department, Rockridge Press, 6005 Shellmound Street, Suite 175, Emeryville, CA 94608。

责任限制/免责声明：出版商和作者对本书内容的准确性或完整性不作任何陈述或保证，并特别否认所有保证，包括但不限于对特定用途适用性的保证。销售或促销材料不得创建或扩展任何保证。本文包含的建议和策略可能不适用于所有情况。本书的销售是基于以下理解：出版商并未提供医疗、法律或其他专业建议或服务。如果需要专业协助，应寻求胜任的专业人士的服务。出版商和作者均不对由此产生的损害承担责任。书中引用某个人、组织或网站作为引用和/或进一步信息的潜在来源，并不意味着作者或出版商认可该个人、组织或网站可能提供的信息或其/它们可能做出的建议。此外，读者应注意，书中列出的网站在本书编写与阅读之间可能已经变化或消失。

如需有关我们其他产品的通用信息或获取技术支持，请联系我们的美国客户服务部门：(866) 744-2665；美国境外拨打 (510) 253-0500。

Rockridge Press 以多种电子和纸质格式出版书籍。纸质书中出现的某些内容可能在电子书中没有，反之亦然。

商标：Rockridge Press 和 Rockridge Press 标志是 Callisto Media Inc. 及其关联公司在美国及和其他国家的商标或注册商标，未经书面许可不得使用。所有其他商标均为其所有者的财产。Rockridge Press 与书中提到的任何产品或供应商均无关联。

内页及封面 设计师：Lisa Schreiber

艺术制作：Janice Ackerman

编辑：Andrea Leptinsky

制作经理：Martin Worthington

插图 ©2021 Carl Wein

平装本 ISBN: 978-1-64876-111-9

电子 ISBN: 978-1-64876-112-6

R0

我将这本书献给 Frank 和 May Yueh，感谢你们在我向编程职业转型期间对我的支持。

如果钞票等于 5 美元，退出循环

打印钞票

}

```

在实际代码中，它看起来像这样。

```javascript

var bills = [1, 1, 5, 10, 20];

for (var index = 0; index < bills.length; index++) {

  // 如果金额是 5 美元

  if (bills[index] === 5) {

    // 完全退出循环

    break;

  }

  console.log(bills[index]);

}

```

![](img/image00283.jpeg)

太棒了！完全正如预期。一旦代码看到 5，循环就会停止。

## 实践中的循环

到目前为止，你一直都在确保自己理解如何遍历数组中的所有金额。现在是解决原始提示了：计算你钱包中的总金额！

### 黑客贴士

如果你的电脑在运行 JavaScript 文件时变慢了，请强制退出。循环正在无休地运行，因为它从未遇到终止条件。键盘快捷键 `ctrl + z` 将强制停止操作。最坏的情况下，关闭 VS Code。

### 循环

回到你之前的代码，内部没有任何行为。但循环已经准备好遍历钞票数组了。

```javascript

var bills = [1, 1, 5, 10, 20];

for (var i = 0; i < bills.length; i++) {

}

```

变量 `index` 被缩短为 `i`。这是在循环中跟踪索引的常用变量名。

为了跟踪金额，需要一个变量。该值将从 0 开始，因为你的循环还没有计算任何钱。

```javascript

var total = 0;

```

这种变量通常被称为累加器（accumulator）。在我们的循环的每次迭代后，它的值会逐渐增加。在访问每张钞票后，它会“累积”值。

将这一切整合在一起，按索引的每个钞票值都会增加累加器 `total` 的值。

```javascript

var bills = [1, 1, 5, 10, 20];

var total = 0;

for (var i = 0; i < bills.length; i++) {

  var currentValue = bills[i];

  total += currentValue;

}

console.log(total);

```

为了确保你完全理解了发生了什么，让我们创建另一个表格来代表每次迭代。

| 迭代 | I | 条件 | 当前值 | 总计 | 钞票 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 0 | 0 < 5 | 1 | 1 | [1, 1, 5, 10, 20] |
| 2 | 1 | 1 < 5 | 1 | 2 | [1, 1, 5, 10, 20] |
| 3 | 2 | 2 < 5 | 5 | 7 | [1, 1, 5, 10, 20] |
| 4 | 3 | 3 < 5 | 10 | 17 | [1, 1, 5, 10, 20] |
| 5 | 4 | 4 < 5 | 10 | 27 | [1, 1, 5, 10, 20] |



`console.log` 在使用后会被销毁吗？绝对不会！函数可以根据需要使用任意次，或者不使用。通常，当程序员看到两种相同的操作时，他们会想出策略来减少重复编写的代码量。函数就是为此的首选策略。

## 抽象 (ABSTRACTION)

如果剥开 `console.log` 的外壳并能够看到它的实现方式，你会看到极其复杂的内容。`console.log` 是一个极佳的抽象。它通过简单的命令执行了复杂的运算。一些程序员付出了巨大的努力才让 `console.log` 让世界能够轻松地使用它。

## 解决巨大挑战

主流程序复杂得令人望畏。人类的大脑无法在脑中想出复杂问题的整个解决方案。相反，你的大脑会将大挑战分解成许多较小的挑战。你一个一个解决每个小挑战并将其封装。然后，你组合所有这些小解决方案来解决眼下的问题。函数非常适合这一点。

## 函数创建 (Function Creation)

声明函数有两种方法。这两种方法相似，你不必担心它们之间的细微差别。但作为一名 JavaScript 程序员，你会根据情况使用这两种方法。

### 函数声明 (FUNCTION DECLARATION)

第一种语法是使用 `function` 关键字并在后面加上名称。分号是可选的。这种声明风格几乎会被专门使用。

```javascript

function functionNameOfYourChoosing() {

// 在此处编写代码

}

```

### 函数表达式 (FUNCTION EXPRESSION)

第二种语法是将 `function` 关键字赋值给一个变量，使用 `var` 进行声明。建议加上分号。这种声明风格仅在进行面向对象编程时才会使用。

```javascript

var functionNameOfYourChoosing = function () {

// 在此处编写代码

};

```

## 函数调用 (Function Invocation)

函数名末尾的括号运行其内部的操作。正式术语是“调用”（invoke）。这种语法对于两种类型的函数声明都是完全相同的。

```javascript

functionNameOfYourChoosing();

```

## Return 语句 (Return Statement)

在原生情况下，函数不会向外部世界暴露它所计算出来的数据。

```javascript

function add() {

  var computed = 5 + 5;

}

add(); // undefined

```

这是因为你没有告诉 JavaScript 你想要它！使用 `return` 关键字，函数可以暴露一段数据。

```javascript

function add() {

  var computed = 5 + 5

  return computed

}

add(); // 10

```

## 函数参数 (Function Parameters)

在在上的示例中，`add` 函数只能将 5 和 5 相加。如果可以接收任意两个数字并将它们相加难道不是更好吗？这就是参数发挥作用的地方。

参数是预先准备好的变量。这让函数能够适应许多情况。

```javascript

function add(num1, num2) {

  return num1 + num2;

}

```

你已经告诉 JavaScript 在调用期间可以传入两个变量 `num1` 和 `num2`。有了参数，这个 `add` 函数就可以处理任何数字。

```javascript

add(10, 5); // 15

add(20, 30); // 50

```

## 使用 Return 提前终止 (Early Termination with Return)

`return` 关键字实际上有两个作用：

1. 它从函数输出一个值。
2. 它停止函数的执行。

你可能会发现自己不想在某个一点之后继续执行代码，或者想做一个决定并停止所有后续操作。

### 极客提示 (HACKER HINT)

当你看到一个重复出现但值不同的算法时，考虑将该操作转换为带有参数的函数。

### 防止加法受类型转换影响 (PROTECT ADD FROM TYPE COERCION)

让我们改进你的 `add` 函数，并使其免受错误输入的影响。还记得类型转换和 `plus` 运算符吗？

```javascript

function add(num1, num2) {

  return num1 + num2;

}

add('10', '5'); // '105'

add(20, '30'); // '2030'

```

你的加法函数可以拼接字符串。但你总是想要相加，或者至少尝试这样做。让我们用提前返回来保护它。如果使用的数据不是数字，函数应该返回 `NaN`。

```javascript

function add(num1, num2) {

  // 如果 num1 不是数字 或者 num2 不是数字

  if (typeof num1 !== 'number' || typeof num2 !== 'number') {

    return NaN;

  }

  return num1 + num2;

}

add('10', 5); // 'NaN'

add(20, '30'); // 'NaN'

```

通过提前返回，你保护了函数免受类型转换或其他任何错误输入的影响。

## 作用域 (Scope)

现在是讨论使用函数时变量可用性的好时机。在编码术语中，变量的可用性被称为“作用域”（scope）。此后将大量编写函数。理解你需要的特定数据是否在代码的特定区域可用是非常。

### VAR: 函数作用域 (VAR: FUNCTION SCOPED)

声明的位置现在变得了。在函数内部声明的变量仅在函数内部可用。

这段代码将产生意料之外的行为。

```javascript

function sampleFunc() {

  var innerVariable = '我只在这个函数内部可用';

  console.log(innerVariable);

}

function otherSampleFunc() {

  console.log(innerVariable);

}

sampleFunc();

otherSampleFunc();

```

运行 `otherSampleFunc()` 会报错。

### 词法作用域 (LEXICAL SCOPE)

不同的编程语言在作用域方面有自己的规则。JavaScript 使用词法作用域。词法作用域是指变量在其自身及其内部作用域内可用。

### 嵌套 (Functions Inside Functions)

函数写在函数内部！这创建了两个层的作用域。一个是内部作用域，另一个是外部作用域。在外部作用域声令的变量在任何内部作用域内都可用。

```javascript

function outerScope() {

  var outerVar = '我在两个作用域中都存在';

  function innerFunc() {

    console.log(outerVar);

  }

  innerFunc();

}

outerScope();

```

但内部作用域在上方无效。

```javascript

function outerScope() {

  function innerFunc() {

    var innerVar = '我只在这里内部';

  }

  console.log(innerVar); // 这会失败

  innerFunc();

}

outerScope();

```

## 电竞表现 (Esports Performance)

使用函数让你能够以优雅的方式解决难题。让我们在解决能力上迈上一大步！Electro 是一支顶级电子竞技队，竞技 Undersea。在全球舞台上取得了优异的成绩。凭借丰富的阵容，他们会轮替上场和坐在场边。不参加比赛的选手被称为“板凳”选手。

### 选手参加比赛了吗？ (DID A PLAYER PARTICIPATE?)

第一个挑战是检查选手是否参加比赛。这个函数应该处理任何可能的选手和任何比赛结果。它们必须是参数。

```javascript

function playedInTournament(tournament, player) {

}

```

在此练习中，`tournament` 参数具有以下结构。它是一个对象结构，只有一个键：`players`。与键关联的值是一个选手名称数组。

```javascript

{

  players: ['smirk', 'knight', 'fly']

}

```

现在你需要找到某个选手是否参加了比赛。对象中有一个 `players` 键。你立即知道需要一个 `for` 循环。数组嵌套在对象中，因此必须通过其键名 `players` 来访问。



```javascript

function playedInTournament(tournament, player) {

  var players = tournament.players;

  for (var i = 0; i < players.length; i++) {

    var currentPlayer = players[i];

    if (currentPlayer === player) {

    }

  }

}

```

如果 `currentPlayer` 是要检查的 `player`，则返回 `true`。但什么时候应该返回 `false` 呢？如果检查已经完了数组中的所有玩家，这意味着该 `player` 根本没有被找到。在函数的最后面，返回 `false`。

```javascript

// tournament.js

function playedInTournament(tournament, player) {

  var players = tournament.players;

  for (var i = 0; i < players.length; i++) {

    var currentPlayer = players[i];

    if (currentPlayer === player) {

      return true;

    }

  }

  return false;

}

```

现在是验证代码的时间。为了实现这一点，你需要使用 `console.log` 来让函数的数据显示在终端中。我将文件命名为 `tournament.js`。

```javascript

var sampleTournament = {

  win: true,

  players: ['smirk', 'knight', 'fly']

};

console.log(playedInTournament(sampleTournament, 'smirk'));

console.log(playedInTournament(sampleTournament, 'superb'));

```

![](img/image00288.jpeg)

看起来不错！在 `sampleTournament` 对象中，`smirk` 参加了比赛，但 `superb` 没有。从文件中删除那两个 `console.log` 语句和数据结构 `sampleTournament`。今后它们将不再需要了。

### 黑客提示

为了防止混淆，可以写一个表格来跟踪每次迭代中发生的情况。

### 嵌套的数据结构

在随后的练习中，需要一个比赛结果列表。在每个比赛结果内部，我们还需要一个参加该比赛的玩家列表。将此数据结构添加到文件中。

```javascript

var tournaments = [

  { win: true, players: ['smirk', 'knight', 'fly'] },

  { win: true, players: ['superb', 'san', 'tired'] },

  { win: true, players: ['smirk', 'knight', 'tired'] },

  { win: false, players: ['san', 'superb', 'fly'] },

  { win: true, players: ['smirk', 'san', 'fly'] },

  { win: false, players: ['superb', 'knight', 'tired'] },

];

```

### 参加的比赛次数

关于玩家参与的数据在 `tournaments` 数组中。有了数据数组，显然需要一个循环。

```javascript

function tournamentsPlayed(tournaments, player) {

  var playCount = 0;

  for (var i = 0; i < tournaments.length; i++) {

    var currentTournament = tournaments[i];

  }

  return playCount;

}

```

这一次，你需要检查 `player` 是否参加了该 `tournament`。不仅如此，你还必须跟踪这种情况发生的次数。判断一个 `player` 是否参加了某场比赛是一项大量工作。每个比赛条目都需要搜索内部数组。但这已经在 `playedInTournament` 中得到了解决。可以重用该函数。

```javascript

var currentTournament = tournaments[i];

var playerDidPlay = playedInTournament(currentTournament, player);

if (playerDidPlay) {

  playCount += 1;

}

```

通过 `console.log` 运行代码进行验验证。

```javascript

console.log(tournamentsPlayed(tournaments, 'smirk'));

console.log(tournamentsPlayed(tournaments, 'superb'));

```

![](img/image00289.jpeg)

看起来不错。`smirk` 和 `superb` 都参加了三场比赛。现在可以删除这些 `console.log` 语句了。

### 赢得的比赛次数

现在，更进一步。检查特定的 `player` 参加获胜 `tournament` 的次数。为了清楚地实现这一点，你需要：

1. 一个循环
2. 一个用于跟踪获胜次数的累加变量

```javascript

function tournamentsWon(tournaments, player) {

  var winCount = 0;

  for (var i = 0; i < tournaments.length; i++) {

    var currentTournament = tournaments[i];

  }

  return winCount;

}

```

这与 `gamesPlayed` 相比略有不同。需要满足两个条件：

1. `player` 参加了 `tournament`
2. 团队获胜了

幸运的是，`playedInTournament` 可以用于第一个条件。对于第二个条件，每个条目在 `win` 键中都有比赛结果。你需要确保在该特定 `player` 参加时，两个条件都为真，以便将比赛计为一次比赛胜利。在这种情况下，使用了与运算符 `&&` 来同时断言这两个条件。

```javascript

function tournamentsWon(tournaments, player) {

  var winCount = 0;

  for (var i = 0; i < tournaments.length; i++) {

    var currentTournament = tournaments[i];

    var playerDidPlay = playedInTournament(currentTournament, player);

    var tournamentWon = currentTournament.win;

    if (playerDidPlay && tournamentWon) {

      winCount += 1;

    }

  }

  return winCount;

}

```

使用 `console.log` 验证代码。

```javascript

console.log(tournamentsWon(tournaments, 'smirk'));

console.log(tournamentsWon(tournaments, 'superb'));

```

![](img/image00290.jpeg)

看起来不错！`smirk` 似乎赢了三场比赛，`superb` 赢了一场。

### 玩家胜率

现在你感兴趣确定胜率。要解决这个问题，将胜利次数除以比赛次数。

```javascript

function playerWinRate(tournaments, player) {

  var total = tournamentsPlayed(tournaments, player);

  var won = tournamentsWon(tournaments, player);

  var percentage = (won / total) * 100;

  return parseInt(percentage);

}

```

```javascript

console.log(playerWinRate(tournaments, 'smirk'));

console.log(playerWinRate(tournaments, 'superb'));

```

### 谁应该参加？

噢不！看起来两名玩家之间发生了纠纷。似乎 `smirk` 和 `superb` 都想参加下一场比赛，但名额只有一个。为了解决这一问题，管理层决定检查每个相应玩家的表现。我们需要使用胜率来决定谁应该参加。

```javascript

function whoShouldPlay(tournaments, player1, player2) {

  var player1WinRate = playerWinRate(tournaments, player1);

  var player2WinRate = playerWinRate(tournaments, player2);

  var benchedPlayer;

  var activePlayer;

  if (player1WinRate > player2WinRate) {

    activePlayer = player1;

    benchedPlayer = player2;

  } else {

    activePlayer = player2;

    benchedPlayer = player1;

  }

}

```



```javascript

console.log(activePlayer + ' should play in the next tournament');

console.log(benchedPlayer + ' should be benched');

```

`whoShouldPlay(tournaments, 'smirk', 'superb');`

![](img/image00293.jpeg)

结果已经出来了，差异显而易见。看来 smirk 是更好的玩家，而 superb 将被下场。

## 总结

这个练习整合了你到为止学过的每一个 JavaScript 技术方面。但你可能已经注意到，解决问题的方法同样重要。你将一个大挑战拆解成了五个更容易的挑战：

1. 比较两名玩家之间的胜率。
2. 计算玩家的胜率。
3. 计算玩家参加的总比赛场次。
4. 计算玩家获胜的场次。
5. 检查玩家是否参加了某场比赛。

所有这些部分的结合为一个复杂的问题提供了一个简单的解决方案。

### 破解代码

这一章是物一二得的。你不仅学习了函数，还略微体验了程序员用来简单地解决挑战性问题的策略类型。

1. 在编程时，什么样的品质让函数变得非常受欢迎？
2. 函数需要什么关键字才能输出一个暴露在函数之外的值？
3. 如果没有显式的 `return`，函数会输出什么？
4. 什么是作用域（scope）？
5. JavaScript 使用什么类型的作用域？用你自己的话解释。

## 调试

程序员有一项名为单元测试的秘密武器。分解问题允许你以增量的方式检查代码的正确性。每个函数都很小，所以很容易测试。如果每个小函数都能正常工作，那么整个挑战应该没有任何问题地运行！

```javascript

// important!此函数不适用于数据结构

// 和对象。仅适用于字符串、数字、null、布尔值和 undefined

function test(description, actual, expected) {

  console.log(description);

  if (actual === expected) {

    console.log(' pass!');

  } else {

    console.log(' fail!');

    console.log(' received: ', actual);

    console.log(' expected: ', expected);

  }

}

```

这是一个非常基础的函数，让你：

1. 为自己写一条关于将测试什么内容的简短消息。
2. 比较两个值。
3. 知道你得到的是否预期的结果。如果没有，打印出你计算的结果与你预期的结果对比。

在你进行真正的调试问题之前，是时候让这个测试函数发挥作用了。为了这样做，你创建一个故意错误的 `add` 函数，并看看你的测试函数给出了什么输出。

```javascript

function add(num1, num2) {

  return num1 - num2;

}

test('add test #1', add(10, 20), 30);

test('add test #2', add(10, 15), 25);

```

![](img/image00294.jpeg)

太棒了！你不仅让 JavaScript 检查你的代码是否正确，还让它在函数出错时向你展示你计算的结果。

## 猜猜猫的名字

让我们用函数在终端里玩一个小游戏。这并不容易！你需要将问题分解成许多子问题，并将算法封装在函数中。

你将输入一个字符，然后会收到关于猜测进的反馈。当你正确猜出所有字符后，全名将打印出来，程序将退出。

![](img/image00295.jpeg)

现在，你的程序运行得不好。事实上，它完全没有运行。以下是你的坏代码：

```javascript

var prompt = require("readline-sync");

// important!此函数不适用于数据结构

// 和对象。仅适用于字符串、数字、null、布尔值和 undefined

function test(description, actual, expected) {

  console.log(description);

  if (actual === expected) {

    console.log(' pass!');

  } else {

    console.log(' fail!');

    console.log(' received: ', actual);

    console.log(' expected: ', expected);

  }

}

function includes(arrOrStr, item) {

  for (var i = 0; i < arrOrStr.length; i++) {

    var currItem = arrOrStr[i];

    if (currItem !== item) {

      return true;

    }

  }

  return false;

}

test('includes #1', includes('cat', 'a'), true);

test('includes #2', includes('cat', 't'), true);

test('includes #3', includes('cat', 'f'), false);

function createHint(actualName, allUserGuesses) {

  var output = '';

  for (var i = 0; i < actualName.length; i++) {

    var currChar = actualName[i];

    if (includes(allUserGuesses, currChar)) {

      output += currChar + ' ';

    } else {

      output = '_ ';

    }

  }

  return output; // 注意：原文此处有一个逻辑错误，但保留了内容

}

```



与 `parseInt` 解析数字和数字形式的字符串一样，`parseFloat` 也是如此，只不过它保留了原始数字中的所有小数值。

```javascript

parseFloat(1322.23423); // 1322.23423

parseFloat('1322.23423'); // 1322.23423

```

## 字符串

在本书的范围内，大多数字符串操作将被跳过。但仍有两个重要的操作需要注意。

### 通过索引访问

对于某些算法来说，逐个元素地检查字符串是非常重要的。这可以通过索引访问每个字符来实现。字符串和数组通过索引访问元素的方式是相同的。

```javascript

var dog = 'Misu';

dog[0]; // 'M'

dog[2]; // 's'

```

### 转为小写和大写

可以分别使用 `toLowerCase` 和 `toUpperCase` 将字符转换为全小写或全大写形式。

```javascript

var dog = 'Misu';

dog.toLowerCase(); // 'misu'

dog.toUpperCase(); // 'MISU'

```

等等！为什么在这个变量名后面要使用这个函数？嗯，从技术上讲，它是一个方法。我们将深入探讨这种差异的目的和原因。目前，只需知道方法是用这种语法调用的即可。

## 数组

修改数组是非常常见的操作，因此 JavaScript 包含了许多内置操作，以按我们所需的方式修改它们。

### 插入

数组中的项通过索引访问。

```javascript

var animals = ['dog', 'cat', 'horse', 'bird'];

animals[0]; // 'dog'

```

访问数组项的相同语法也可用于向索引分配新值。

```javascript

var animals = ['dog', 'cat', 'horse', 'bird'];

animals[0] = 'pig';

animals[0]; // 'pig'

```

### push（推送）

一种常见操作是在数组末尾插入。数组方法名为 `push`。

```javascript

var sampleArray = [];

sampleArray.push(10);

sampleArray; // [10]

```

### pop（弹出）

另一个常见操作是移除数组的最后一个项，使用方法 `pop`。

```javascript

var sampleArray = [2, 10];

sampleArray.pop();

sampleArray; // [2]

```

### shift（左移）

可以使用方法 `shift` 移除数组的第一个元素。

```javascript

var sampleArray = [2, 10];

sampleArray.shift();

sampleArray; // [10]

```

### unshift（右移）

最后一个数组操作是 `unshift`，它在数组前端插入一个元素。

```javascript

var sampleArray = [2, 10];

sampleArray.unshift(5);

sampleArray; // [5, 2, 10]

```

## 对象

与数组相比，对象的修改程度没有那么大。这是由于更深层次的技术原因。但对象仍然支持插入、替换和删除。

### 插入与替换

对象值的插入是通过等号完成的。

```javascript

var animals = {};

animals.dog = 'sparky';

animals; // { dog: 'sparky' }

```

插入的语法与替换相同。如果键已经存在，它将替换该值。

```javascript

var animals = {

  dog: 'sparky'

};

animals.dog = 'not sparky';

animals; // { dog: 'not sparky' }

```

### 删除

从对象中删除元素是不常用的操作。`delete` 运算符用于删除对象中的键值对。

```javascript

var animals = {

  dog: 'sparky'

};

delete animals.dog;

animals; // { }

```

## 变异

修改数据类型而不是总是创建一个新版本的想法被称为可变性。一个操作可以是变性的，这意味着它会修改现有数据。数据也可以被视为不可变的，意味着它从根本上无法被。

在下面的示例中，当使用数组和对象操作时，我们没有向新变量赋值或重新赋值。这是因为 `push`、`pop`、`shift` 和 `unshift` 是修改现有数组的操作。所示的操作是改变现有数据结构的操作。

```javascript

var animals = ['dog', 'cat', 'horse', 'bird'];

animals.push('lizard');

animals; // ['dog', 'cat', 'horse', 'bird', 'lizard'];

```

事实上，重新赋值是非常糟糕的事情。它会创建非常不直观的代码。

```javascript

var animals = ['dog', 'cat', 'horse', 'bird'];

animals = animals.push('lizard');

animals; // 5

```

返回值为 5 是因为在向其中推入 lizard 之后，新数组的长度。但这可能不是想要的输出。更有可能，想要的输出是数组本身。

### 字符串是不可变的

```javascript

var animal = 'd';

animal += 'og';

animal; // 'dog'

```

你注意到你一直在使用重新赋值运算符了吗？那是因为字符串是不可变的。现有的字符串无法更新。必须重新赋值以创建一个全新的字符串。

```javascript

var animal = 'd';

animal + 'og';

animal; // 'd'

```

由于字符串是不可变的，字符串拼接不会修改 `animal`。

## 运行中的数据操作

当你看到数据操作运行时运行时，理解数据操作要容易得多。我们还将概述常见的数据操作策略。

### 构建新数组

以一种形式或另一种形式修改数组，构建一个新数组比修改现有数组更有优势。

给定以下数组，创建一个技能水平高于 5 的玩家名称数组。

```javascript

players = [

  { name: 'superb', skill: 3 },

  { name: 'smirk', skill: 7 },

  { name: 'tired', skill: 6 },

  { name: 'ANS', skill: 9 }

];

```

这是预期输出：
`['smirk', 'tired', 'ANS']`

为了使代码更易管理，你会将算法放在一个函数中。如果有一个数组需要检查，`for` 循环应该是你的首选。

```javascript

function getSkilledPlayers(allPlayers) {

  for (var i = 0; i < allPlayers.length; i++) {

    // 逻辑在这里

  }

}

```

伪代码如下：

```javascript

function getSkilledPlayers(allPlayers) {

  var skilledPlayers = [];

  for (var i = 0; i < allPlayers.length; i++) {

    // 逐个检查元素

    // 如果玩家符合标准，将其名称推入

  }

  return skilledPlayers;

}

```

将所有内容结合在一起，这是你的代码和预期输出：

```javascript

function getSkilledPlayers(allPlayers) {

  var skilledPlayers = [];

  for (var i = 0; i < allPlayers.length; i++) {

    var player = allPlayers[i];

    if (player.skill > 5) {

      skilledPlayers.push(player.name);

    }

  }

  return skilledPlayers;

}

console.log(getSkilledPlayers(players));

```

为了保险起见，可以写一个表格来查看每次迭代后值的变化情况：

| ITERATION | PLAYER.NAME | PLAYER.SKILL | PLAYER.SKILL > 5 | SKILLEDPLAYERS |
| :--- | :--- | :--- | :--- | :--- |
| | | | | [] |
| 1 | superb | 3 | false | [] |
| 2 | smirk | 7 | true | ['smirk'] |
| 3 | tired | 6 | true | ['smirk', 'tired'] |
| 4 | ANS | 9 | true | ['smirk', 'tired', 'ANS'] |



如果你发现自己需要使用 `delete` 运算符，那么更有可能是你的算法应该改用数组来解决。

### 更新数组中的对象 (#part0003.xhtml_sec-76)

假设你有一个对象，其键是玩家的名字和他们的年龄。将这些数据合并到一个数据结构是有意义的。你可以使用你学过的策略来实现这一点。

```javascript

var players = [

{ name: 'superb', skill: 3 },

{ name: 'smirk', skill: 7 },

{ name: 'tired', skill: 6 },

{ name: 'ANS', skill: 9 }

];

var playerAges = {

superb: 21,

smirk: 21,

tired: 22,

ANS: 21

};

```

这是预期的输出。

```javascript

[

{ name: 'superb', skill: 3, age: 21 },

{ name: 'smirk', skill: 7, age: 21 },

{ name: 'tired', skill: 6, age: 22 },

{ name: 'ANS', skill: 9, age: 21 }

];

```

和上一个问题一样，显然需要迭代。

```javascript

function playerWithAges(players, ages) {

  var playerData = [];

  for (var i = 0; i < players.length; i++) {

    var player = players[i];

  }

  return playerData;

}

```

但这次，返回值不是字符串数组，而是对象数组。在每次迭代中，创建一个包含数据的新对象并将其推入数组。

将所有内容整合在一起，文件和输出看起来应该是这样的。

```javascript

var players = [

{ name: 'superb', skill: 3 },

{ name: 'smirk', skill: 7 },

{ name: 'tired', skill: 6 },

{ name: 'ANS', skill: 9 }

];

var playerAges = {

superb: 21,

smirk: 21,

tired: 22,

ANS: 21

};

function playerWithAges(players, ages) {

  var playerData = [];

  for (var i = 0; i < players.length; i++) {

    var player = players[i];

    var playerEntry = {

      name: player.name,

      skill: player.skill,

      age: ages[player.name]

    };

    playerData.push(playerEntry);

  }

  return playerData;

}

console.log(playerWithAges(players, playerAges));

```

![](img/image00299.jpeg)

非常棒！如果这个问题的任何部分让你感到困惑，请写一个表格记录。

### 解密代码 (#part0003.xhtml_sec-77)

通过这一章，你终于涵盖了编程的核心基础知识。但你还没有结束。事实上，这只是一个开始！

**1. (#part0027.xhtml_ch07_Q1)** 运行这段代码后，`players` 是一个包含“smurf”和“ANS”的数组吗？为什么？或者为什么不？

```javascript

var players = ['super', 'smurf', 'ANS'];

players = players.shift();

players;

```

**2. (#part0027.xhtml_ch07_Q2)** 什么是可变性？哪些数据类型是可变的？

**3. (#part0027.xhtml_ch07_Q3)** 为什么修改字符串需要重新赋值，而数组和对象的修改则不需要？

**4. (#part0027.xhtml_ch07_Q4)** 哪些数组方法可以减小数组的大小？

**5. (#part0027.xhtml_ch07_Q5)** 哪些数组方法可以增加数组的大小？

**6. (#part0027.xhtml_ch07_Q6)** 为以下函数画一个表格。写下数组在每次迭代中的样子，以及 `array.length > 0` 的情况。

```javascript

function destroyArray(array) {

  var i = 0;

  while (array.length > 0) {

    array.pop();

    i++;

  }

}

var arr = [10, 20, 12, 30, 25];

destroyArray(arr);

```

**7. (#part0027.xhtml_ch07_Q7)** 下列代码的输出是什么？如有必要，画一个表格。

```javascript

function modifyString(str) {

  var newStr = '';

  for (var i = 0; i < str.length - 1; i++) {

    newStr += str[i];

  }

  return newStr;

}

modifyString('abcdefg')

```

**8. (#part0027.xhtml_ch07_Q8)** 用自己的语言描述这个函数的作用。为什么它对字符串和数组都有效？为每个示例调用画一个表格。

```javascript

function mysteryFunc(arrOrStr, item) {

  for (var i = 0; i < arrOrStr.length; i++) {

    var currItem = arrOrStr[i];

    if (currItem === item) {

      return true;

    }

  }

  return false;

}

mysteryFunc('cat', 'a'); // true

mysteryFunc('cat', 'b'); // false

mysteryFunc([30, 11], 1); // false

```

**9. (#part0027.xhtml_ch07_Q9)** 下列代码的输出是什么？如有必要，画一个表格。

```javascript

var count = 0;

function increment() {

  count += 1;

}

increment();

console.log(count);

```

### 调试 (#part0003.xhtml_sec-78)

通过这一章，返回值不是字符串数组，而是对象数组。在每次迭代中，创建一个包含数据的新对象并将其推入数组。

将所有内容整合在一起，文件和输出看起来应该是这样的。

```javascript

var players = [

{ name: 'superb', skill: 3 },

{ name: 'smirk', skill: 7 },

{ name: 'tired', skill: 6 },

{ name: 'ANS', skill: 9 }

];

var playerAges = {

superb: 21,

smirk: 21,

tired: 22,

ANS: 21

};

function playerWithAges(players, ages) {

  var playerData = [];

  for (var i = 0; i < players.length; i++) {

    var player = players[i];

    var playerEntry = {

      name: player.name,

      skill: player.skill,

      age: ages[player.name]

    };

    playerData.push(playerEntry);

  }

  return playerData;

}

console.log(playerWithAges(players, playerAges));

```

![](img/image00299.jpeg)

非常棒！如果这个问题的任何部分让你感到困惑，请写一个表格记录。



在 JavaScript 中，访问狗的年龄看起来如下所示。

```javascript

sparky.age; // 10

```

### 对象方法 (OBJECT METHOD)

如果 Sparky 想汪叫，就会调用一个名为 `bark` 的方法。

```javascript

sparky.bark(); // 'ruff ruff!'

```

注意 `bark` 看起来有多像函数调用吗？那是因为方法实际上就是函数！方法是特定于对象实例的函数。它们不能用于其他任何。

### JavaScript 对象实现 (JavaScript Object Implementation)

为了利用对象的力量，我们必须学习完整的 JavaScript 语法来编写它们。

### 构造函数 (CONSTRUCTOR FUNCTION)

在 JavaScript 中，函数具有双重用途。它们既可以当作普通函数来执行代码（你已经学过了），也可以当作构造函数。构造函数是一个被用来创建对象实例的函数。

在这里，每个单词首字母大写的驼峰命名法是公认的约定。

```javascript

function Dog() {

}

```

对于对象实例，在函数调用前面需要 `new` 关键字。

```javascript

var sparky = new Dog();

```

### 对象属性 (OBJECT PROPERTY)

添加对象属性本质上与添加键值对相同。只不过是在构造函数中完成的。

```javascript

function Dog() {

  this.age = 10;

}

var sparky = new Dog();

sparky.age; // 10

```

等等！这个变量 `this` 是什么？嗯，它是一个由函数自动创建的秘密变量。在面向对象编程中，它有一些重要的属性。最重要的是，`this` 可以被分配键值对。

### 对象方法 (OBJECT METHODS)

在 JavaScript 中，函数还有一个名为 `prototype` 的秘密属性。它的职责是存储该函数供对象实例可用的方法。要创建方法，需要函数表达式语法。

```javascript

function Dog() {

}

Dog.prototype.bark = function() {

  console.log('ruff ruff!');

};

```

var sparky = new Dog();

sparky.bark(); // 'ruff ruff!'
```

### 实例变量 (INSTANCE VARIABLE)

现在你已经了解了基础语法，我们应该谈谈秘密变量 `this`。它在构造函数中是可用的。可以向 `this` 添加键值对。添加到 `this` 的键值对通常被称为实例变量。

```javascript
function Dog() {
  this.name = 'sparky';
}

Dog.prototype.speak = function() {
  console.log('ruff ruff, my name is' + this.name);
};
```

var sparky = new Dog();

sparky.speak(); // 'ruff ruff, my name is sparky'

```

![](img/image00301.jpeg)

暂时忽略这只狗会说英语的事实。你更感兴趣的是构造函数中创建的 `this.name` 竟然神奇地在方法中可用。这一点至关重要：任何分配给 `Dog.prototype` 的方法都可以使用变量 `this`。

### 实例变量的修改 (INSTANCE VARIABLE MODIFICATION)

由于这在每个方法中都是可用的，因此也可以在方法中修改实例变量。

```javascript

function Dog() {

  this.name = 'sparky';

  this.age = 0

}

Dog.prototype.growOlder = function() {

  this.age += 1

};

```

var sparky = new Dog();

sparky.age // 0

sparky.growOlder();

sparky.age // 1
```

### 骇客提示 (HACKER HINT)

在方法中也可以创建实例变量，但不被鼓励这样做。在大多数情况下，有更好的代码编写方式。

### 实战中的面向对象编程 (Object-Oriented Programming in Action)

眼见为实，所以通过一个能力与现实狗的 JavaScript Dog 来建立你对面向对象编程的理解。

### 狗的属性 (DOG PROPERTIES)

为了创建一个对象实例，需要一个构造函数。

```javascript
function Dog() {

}

var sparky = new Dog();
```

这很无聊，并没有告诉你太多关于狗的知识。狗有许多你可能希望对象了解的方面。这可以通过将它们制作实例变量来实现。狗的名字、年龄、重量和 `legCount` 可以被存储。典型的狗有 4 条腿。但名字、年龄和重量在狗之间各不同。将它们作为参数添加到我们的构造函数中。

```javascript
function Dog(name, age, weight) {

}
```

为了跟踪每个 Dog 实例中的数据，将这些值作为键值对添加到 `this`。

```javascript
function Dog(name, age, weight) {
  this.name = name;
  this.age = age;
  this.weight = weight;
  this.legCount = 4;
}
```

var sparky = new Dog('sparky', 4, 20);

var misu = new Dog('misu', 10, 15);

sparky.name; // 'sparky'

sparky.weight; // '20'

misu.name; // 'misu'

misu.weight; // 15

```

太棒了！现在你理解了如何使用构造函数创建对象实例，你有了两只拥有各自的名字、年龄和重量的独立狗。

### 狗的方法 (DOG METHODS)

目前，这些狗不知道该做什么。要改变这一点，添加几个方法。

首先，狗应该能够吃东西。添加一个 `eat` 方法。

```javascript

Dog.prototype.eat = function() {

  console.log('nom nom nom');

};

```

var sparky = new Dog('sparky', 4, 20);

sparky.eat(); // 'nom nom nom'
```

当狗吃得太多时，体重会增加。可以写一个方法来表示。就像任何函数一样，方法可以接受参数。

然后，添加一个代表因过量而增加重量的参数。

```javascript
Dog.prototype.eatTooMuch = function(weightGain) {
  console.log('ugh... ' + this.name + ' doesn\'t feel so good');
  this.weight += weightGain;
};
```

var sparky = new Dog('sparky', 4, 20);

sparky.weight; // 20

sparky.eatTooMuch(2); // 'ugh . . . sparky doesn't feel so good'

sparky.weight; // 22

```

记住，在分配给我们的构造函数 `Dog` 的所有方法中，我们都可以 `this`。`eatTooMuch` 方法能够修改狗的体重。

方法是语法修改过的函数。你已经广泛使用了函数进行计算。在这里你可以再次这样做。创建一个计算狗年年龄的方法，例如 `ageInDogYears` 方法。将人类年龄等同于狗的年龄的法则是乘以七。

```javascript

Dog.prototype.ageInDogYears = function(weightGain) {

  return this.age * 7;

};

```

var sparky = new Dog('sparky', 4, 20);

sparky.ageInDogYears(); // 28
```

等一下！Sparky 决定贪婪，现在正在从一只猫朋友那里偷食物。在一个新的 `stealCatFood` 方法中，你可以表达 Sparky 消耗了食物并且在此过程中调皮的事实。

方法可以在其他方法内部调用。已经创建了一个 `eat` 方法，所以你可以复用它。为了表达犬类的调皮本性，还可以显示额外的 `console.log` 消息。

```javascript
Dog.prototype.eat = function() {
  console.log('nom nom nom');
};

Dog.prototype.stealCatFood = function() {
  this.eat();
  console.log('Yuck, cat food is gross!');
};
```

var sparky = new Dog('sparky', 4, 20);

sparky.stealCatFood();

// 'nom nom nom'

// 'Yuck, cat food is gross!'

```

在另一个方法内部调用方法时，永远不要引用 `prototype`。应该是 `this.eat` 而不是 `this.prototype.eat`。

### 骇客提示 (HACKER HINT)

方法方法分解复杂方法的直接方法。鼓励创建新的小方法，即使该方法本身没有在其他地方或任何对象实例中使用。

### 破解代码 (Crack the Code)

随着编程工具和原则复杂性的增加，要在心中记住一切变得越来困难。你已经到了在线资源是你最好的朋友阶段！不要害于去网上发现更多关于本章涵盖主题的深度见解。一些建议的资源列在书末。

1. 定义什么是对象数据结构。
2. 定义面向对象编程中什么是对象。
3. 哪个变量在所有方法中都是可用的？
4. 在另一个方法内部调用方法的语法是什么？
5. 创建构造函数的语法是什么？
6. 什么是对象实例？
7. 初始化对象实例的语法是什么？



## 调试

一个基础的聊天程序在运行时出现了问题。`printLog` 方法应该打印聊天历史。这个稍微有点棘手，因为有两个对象正在相互交互。你正在以高级的方式使用数据结构，所以不要害使用 `console.log` 来检查变量的值。

```javascript

function Person(name) {

  this.name = name;

}

function ChatProgram() {

  this.chatLog = [];

}

ChatProgram.prototype.message = function (person, message) {

  var messageEntry = {

    person: person,

    message: message

  };

  this.chatLog(messageEntry); // 注意: 这看起来像源代码中的一个 bug

};

ChatProgram.prototype.parseMessageEntry = function (chatEntry) {

  return chatEntry.person.name + ': ' + chatEntry.chat;

};

ChatProgram.prototype.getLog = function () {

  var allMessages = [];

  for (var i = 0; i < this.chatLog.length; i++) {

    var chatEntry = this.chatLog[i];

    var parsedMessage = this.prototype.parseMessageEntry(chatEntry);

    allMessages.pop(parsedMessage);

  }

  return allMessages;

};

ChatProgram.prototype.printLog = function () {

  var allMessages = this.getLog;

  for (var i = 0; i < allMessages.length; i++) {

    console.log(allMessages[i]);

  }

};

var layna = new Person('Layna');

var andrew = new Person('Andrew');

var chat = new ChatProgram();

chat.message(andrew, 'Hi Layna, how\'s it going?');

chat.message(layna, 'I\'m doing great');

chat.message(layna, 'What about you?');

chat.message(andrew, 'I just came back from the doctor');

chat.message(layna, 'Wow, this conversation is really boring');

chat.message(andrew, 'That was really mean, why would you say something like that?');

chat.message(layna, 'I have better things to do');

chat.message(andrew, ':(');

chat.message(layna, 'Goodbye');

chat.printLog();

```

这是预期的输出。

![](img/image00302.jpeg)

# 程序员检查清单

程序员检查清单 » 让我们复习一下涵盖过的主题

面向对象编程并不是 JavaScript 特有的，但它是第一个并非在所有编程语言中都通用的主题。面向对象编程是解决编程挑战的众多策略之一。随着你在编程工具箱中积累了更多技术，你将会发现解决问题有多种方法。发现问题的最佳方法需要经验和直觉。如果你有一个不确定的想法，尽管尝试一下吧！编程的精髓就在于从过去的错误中学习。以下是对你在本章中所学习的内容的快速复习。

*   什么是对象
*   什么是对象实例
*   如何创建实例变量
*   如何创建方法

![](img/image00303.jpeg)

# 第 9 章：JavaScript 与 Web

所有（无聊的）HTML 能做的一切都可以用 JavaScript 实现——而且不仅如此！为了证明这一点，在本章中，你将从网页上的 HTML 开始，展示如何用 JavaScript 实现相同的功能，然后进一步超越 HTML 的能力范围。这是你第一次体验现代 JavaScript 的魅力以及它的高光之处。我希望你和我一样兴奋！

## Web 的抽象层次

与你的标准终端相比，网站处于完全不同的抽象层次上。如果说 `console.log` 的抽象层次像是骑自行车，那么 JavaScript 及其 Web 开发功能就像是开车。

对于本章来说，你不需要担心工具是如何工作的。你只需要关注利用工具在网页浏览器上执行有意义的任务的能力。

## HTML：超文本标记语言

你将非常依赖 JavaScript，但仍然需要少量的超文本标记语言（即 HTML）来与网页交互。现代网站使用了大量的 JavaScript 来操作它。

### HTML 文件

就像 JavaScript 有它自己的扩展名 `.js` 一样，HTML 也有它自己的扩展名 `.html`。创建一个 HTML 文件。这是某个东西被视为网页的最低要求。我将我的文件命名为 `index.html`，这是第一个 HTML 文件的标准名称。

![](img/image00304.jpeg)

### HTML 标签

注意单词周围的角括号了吗？那是 HTML 语法。

```

<valid-html-tag-name-here>

```

一个周围有角括号包围，另一个有一个角括号和一个斜杠。只有角括号的标签被称为起始标签，另一个带有斜杠的是闭合标签。起始标签必须有一个对应的闭合标签。

```html

<html>

</html>

```

在起始标签和闭合标签之间可以放置任何数量的内容。HTML 可以变得极其复杂！

### 我们将使用的 HTML 标签

因为本书的侧重点是 JavaScript，所以只会涵盖几个 HTML 标签。

```html

<html>

<head></head>

<body>

<div>

  Hello!

</div>

</body>

</html>

```

`html` 标签是包裹文件中所有 HTML 内容的主标签。`head` 标签是多用途的。它通常是插入非视觉化 HTML 的地方。`body` 标签是放置视觉元素的地方。`div` 是一个没有重要作用的标签。它简单地用于封装其内部的元素。

### HTML 属性：CLASS 和 ID

有许多不同的 HTML 属性。应用它们的语法是属性名、等号和值（双双引号）。从概念上说，它与对象数据结构中的键值对非常相似。

```html

<div class="container">

  I am content in a div!

</div>

```

在 HTML 中拥有 `class` 和 `id` 属性是非常重要的。在处 JavaScript 时，常用的策略是通过类或 ID 查找 HTML 元素。

## Web 浏览器

在开始之前，确保已安装 Google Chrome 浏览器。并不是所有浏览器的构建都是相同的，而且 Google Chrome 在运行 JavaScript 方面非常出色。

搜索引擎查询：“google chrome download”

当前 URL：[google.com/chrome](http://google.com/chrome)

### 浏览器开发者工具

安装后，打开 Google Chrome。导航到设置（右上三个点） -> 更多工具 -> 开发者工具。

开发者控制将会出现。作为程序员，这里是魔法发生的地方。它就像内置在浏览器中的终端。

![](img/image00305.jpeg)

在你的操作系统（PC 或 Mac）文件系统中找到文件。最简单的方法是在 VS Code 中右键点击文件并选择“在资源管理器中显示”。对于 Mac 是“在访达中显示”。这会打开文件所在的目录。

![](img/image00306.jpeg)

如果文件已经有了 Google Chrome 图标，双击文件打开它。文件也可以拖到浏览器窗口中。

![](img/image00307.jpeg)

注意位置不是互联网 URL？那是 HTML 文件的目录路径。在确认文件运行后，修改 HTML。

```html

<html>

<head></head>

<body>

<div>

  Hello!

</div>

<div>

  I EXTREMELY cool

</div>

</body>

</html>

```

修改后，页面没有变化。为什么浏览器没有承认我们非常酷呢？那是因为浏览器加载了文件的旧版本。为了看到更新，请刷新页面。

![](img/image00308.jpeg)

刷新后，我们看到了更新。非常棒！

![](img/image00309.jpeg)

## 文档

在浏览器中，会自动创建一个名为 `document` 的变量。将其输入开发者控制台。该变量是一个指向整个页面的 JavaScript 对象。展开后，所有的 HTML 都显现了。使用你的鼠标指针悬停在 `document` 变量上。注意网页是蓝色的？

![](img/image00310.jpeg)

开发者控制台会高亮光标悬停过的 HTML。为了进一步证明这一点，展开 body 并悬停在一个高亮的 div 元素上。

![](img/image00311.jpeg)

## HTML 选择器





JavaScript 有许多与浏览器相关的函数可以使用。`document` 是一个对象，意味着它拥有方法。这些可用方法可以修改 HTML。整个 Web 开发社区都高度依赖这些方法和函数。

## DOCUMENT.GETELEMENTSBYCLASSNAME

document 对象上一个会被广泛使用的方法是 `document.getElementsByClassName`。如果我们为 `div` HTML 元素添加类名（class）属性，`document.getElementsByClassName` 就能施展魔法了！

```html

<html

<head>

</head>

<body>

<div class="cool-message">

Hello!

</div>

<div class="cool-message">

I am EXTREMELY cool

</div>

</body>

</html>

```

`document.getElementsByClassName` 接受一个参数，即是类名的字符串名称。`cool-message` 这个类被添加到了 `div` 元素中。该属性将用于识别这些 HTML 元素。在开发者控制台中中使用以下代码。运行代码后，输入变量名 `divElements` 即可在控制台中显示它的值。

```javascript

var divElements = document.getElementsByClassName('cool-message');

```

代码运行后，再次在控制台中输入变量名 `divElements` 以显示其值。

![](img/image00312.jpeg)

太棒了！看起来该语句返回了包含我们两个 HTML 元素的数组！从技术来说，它是一个名为 `HTMLCollection` 的数据结构。在以后，`HTMLCollections` 将被称为类数组数据结构。但不用担心，因为数组与类数组数据结构之间的区别对你没有影响。循环可以在 `HTMLCollections` 上运行。

## DOCUMENT.GETELEMENTBYID

与 `document.getElementsByClassName` 通过类属性获取 HTML 元素一样，`document.getElementById` 通过其 id 属性选择元素。为了让一个元素被 `document.getElementById` 选中，请修改 HTML。添加一个带有 id 属性的 `div` 元素。

```html

<html

<head>

</head>

<body>

<div class="cool-message">

Hello!

</div>

<div class="cool-message">

I am EXTREMELY cool

</div>

<div id="occupation">

That is because I am a programmer

</div>

</body>

</html>

```

刷新页面。在开发者控制台中输入以下代码。再次在控制台中输入变量名后，返回值应该指向第三行文本。

```javascript

var divElement = document.getElementById('occupation');

```

![](img/image00313.jpeg)

注意看 `document.getElementById` 是如何返回单个元素的？它没有返回像 `document.getElementsByClassName` 那样的类数组数据结构。这是因为 `document.getElementById` 一次只能选择一个元素。

## HTML 操作

HTML 元素内部包含许多方法和属性，就像 document 对象一样。这些方法和属性赋予了我们修改特定 HTML 元素的能力。

### 使用 INNERHTML 访问文本

在页面上编写文本并将其封装在 HTML 内部时，`div` 是最直观的标签。当 JavaScript 使用选择器指向 HTML 时，它被表示为一个 JavaScript 对象。该对象有一个名为 `innerHTML` 的键。它保存 HTML 元素内部的文本。通过回顾你的示例 HTML 可以看到这一点。使用 `document.getElementById` 获取 id 为 `occupation` 的 `div` 内部的文本。

```html

<html

<head>

</head>

<body>

<div class="cool-message">

Hello!

</div>

<div class="cool-message">

I am EXTREMELY cool

</div>

<div id="occupation">

That is because I am a programmer

</div>

</body>

</html>

```

```javascript

var divElement = document.getElementById('occupation');

divElement.innerHTML;

```

![](img/image00314.jpeg)

### 使用 INNERHTML 注入新文本

`innerHTML` 是对象上的一个属性。就像对象上的任何键值对一样，它可以被重新赋值。这允许修改内部的文本。

```javascript

var divElement = document.getElementById('occupation');

divElement.innerHTML += ' and love building things';

```

![](img/image00315.jpeg)

使用自加运算符，额外的文本被追加到了 `div` 元素的 `innerHTML` 中。恭喜你！你已经迈入了 Web 开发世界的第一步。

### 更新属性 ID

与 `innerHTML` 可以被更新一样，`class` 和 `id` 属性也可以更改。更新 HTML 元素的 `id` 很容易。关键是 `id`。

```javascript

var divElement = document.getElementById('occupation');

divElement.id = 'new-id';

```

### 更新属性 CLASS

更新 `class` 比更新 `id` 更复杂。这是因为通常会分配多个类。回到 HTML 文件。现在，`div` 元素只有一个类。

```html

<html

<head>

</head>

<body>

<div class="cool-message">

Hello!

</div>

<div class="cool-message">

I am EXTREMELY cool

</div>

<div id="occupation">

That is because I am a programmer

</div>

</body>

</html>

```

向现有的 HTML 元素添加类的方法是 `classList.add`。它接受一个参数，即要追加的类名。

```javascript

var divElements = document.getElementsByClassName('cool-message');

divElements[0].classList.add('new-class');

```

![](img/image00316.jpeg)

移除类的方法是 `classList.remove`，它接受一个类名作为参数。

```javascript

var divElements = document.getElementsByClassName('cool-message');

divElements[0].classList.remove('new-class');

```

![](img/image00317.jpeg)

### 修改 HTML 类的目的

到目前，你做了很多工作来学习如何更改 HTML 元素的类。这在处理 CSS 时会变得非常重要。本书将不会涵盖 CSS，但只需知道更新类属性是触发 HTML 元素视觉变化的常用方法。

## 创建元素

`document` 对象还拥有创建 HTML 元素的方法。当你制作游戏时，这将会非常重要！

### DOCUMENT.CREATEELEMENT

使用 `document.createElement`，JavaScript 可以创建 HTML。它接受一个参数，即 HTML 标签的字符串名称。因为我们还没学习 HTML，我们将一直创建一个 `div` 元素。

```javascript

var div = document.createElement('div');

div.innerHTML = 'I am a new div!';



进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```
if (condVar > someVal) {console.log("xxx")}
```



cancelButton.innerHTML = 'cancel';

cancelButton.classList.add('cancel-button');

return cancelButton;

}

当点击取消按钮时，文本需要恢复到原始状态。销毁 textarea HTML 元素，并使用保存的文本重新插入。

```javascript
function createCancelButton(originalText) {
  var cancelButton = document.createElement('div');
  cancelButton.innerHTML = 'cancel';
  cancelButton.classList.add('cancel-button');
  cancelButton.addEventListener('click', function () {
    var parentDiv = getParentDiv(updateButton);
    var updatedText = getTodoText(parentDiv);
    destroyInnerContent(parentDiv);
    var textDiv = createTextDiv(updatedText);
    var closeButton = createCloseButton();
    var editButton = createEditButton();
    parentDiv.append(textDiv);
    parentDiv.append(closeButton);
    parentDiv.append(editButton);
  });
  return cancelButton;
}
```

## 恭喜！

你已经成功克服了本章的挑战！你学会了如何操作 DOM、处理事件以及有效地使用变量。

## 答案页

# 第 3 章

### 破解代码

注释用于在 JavaScript 中解释代码。浏览器会忽略它们。

```javascript
// 这是一个注释
var x = 10;
/*
  这是一个
  多行注释
*/
```

### 1. 注释什么时候有用？
注释用于向其他开发者解释代码的功能，或者供未来的自己查看。

### 2. 声明和赋值之间有什么区别？
声明创建变量（使用 `var`、`let` 或 `const`）。赋值是给该变量一个值（使用 `=`）。

### 3. “var” 单词可以作为变量名吗？
不可以，`var` 是 JavaScript 中的保留关键字，不能作为标识符。

### 4. 本章涵盖了哪些关键字？
涵盖了 `var`、`let`、`const`、`if`、`else`、`function`、`return` 和 `addEventListener` 等关键字。

### 5. 增位运算符和赋值之间有什么区别？
增位运算符（`++`）将值加 1。赋值（`=`）设置特定的值。

### 6. 如何访问数组中的值？
使用它们的索引访问，索引从 0 开始。

### 7. 如何访问对象中的值？
通过键（key）访问，可以使用点符号法（`.key`）或括号法（`["key"]`）。

### 8. 如果访问数组中不存在的索引会输出什么值？
返回 `undefined`。

### 9. 如果访问对象中不存在的键，会输出什么值？
返回 `undefined`。

### 10. 什么时候访问对象中的值时必须使用括号法？
当键存储在变量中，或者包含特殊字符/空格时，必须使用括号法。

## 调试

### 1. 变量似乎没有改变值，尽管它已经自增。
```javascript
var num = 0;
num++;
console.log(num); // 1
```

### 2. 两个数字相加工作不正常。
其中一个数字是字符串，所以 JavaScript 执行了字符串拼接。
```javascript
var num1 = 10;
var num2 = "2";
console.log(num1 + num2); // "102"
```

### 3. 尝试使用键 ‘pug’ 你的狗的名字 ‘Max’ 输出 undefined。
```javascript
var dogs = {
  pug: 'Max',
  terrier: 'Appa'
};
var myDog = "pug";
console.log(dogs[myDog]); // 'Max'
```

### 4. 尝试访问数组的最后一项输出 undefined。
```javascript
var meanPeople = ['Layna', 'Layna again', 'Layna one more time'];
console.log(meanPeople[2]); // 'Layna one more time'
```

### 5. 尝试打印此字符串时发生致命运行时错误。
```javascript
console.log('Layna\'s favorite hobby is being mean to Andrew');
```

`typeof` 运算符可以用于字符串、数字、`null`、`undefined` 和布尔值。`typeof` 运算符不能用于检查数组和对象。

### 3. 哪种数据类型使用 `instanceof` 运算符进行正确检查？
`instanceof` 运算符可以检查一个数据类型是否为数组。

### 4. 下列代码的输出是什么？
false，因为 `true && false` 的求值为 `false`，且右侧已经是 `false`。

### 5. 下列代码的输出是什么？
true，因为 `!false` 的求值为 `true`。右侧的求值为 `false`，但 OR 运算符（双竖线）只需要其中一侧为真即可。

### 6. 为什么 `array[index] !== undefined` 是检查该索引是否存在于数组中的有效方法？
如果尝试访问的数组不存在该索引，输出将是 `undefined`。

## DEBUGGING

### 1. 代码说该数组是一个对象。
`typeof` 运算符不能用于检查某项是否为数组。必须使用 `instanceof` 运算符。
```javascript
var item = [];
if (item instanceof Array) {
  console.log('I am an array');
} else {
  console.log('I am not an array');
}
```

### 2. 《超级意大利兄弟 2》已经连续获得 10 多次驴子博士的“年度游戏奖”了。它绝对是一部杰作。但代码的说法并非如此。
在 `if` 条件判断中，值比较器是错误的。它应该是大于 `> `，而不是小于 `<`。
```javascript
var game = 'superItalianBrosTwo';
if (donkeysGameScores[game] > 95) {
  console.log(game + ' is a masterpiece');
} else {
  console.log(game + ' is not a masterpiece');
}
// superItalianBrosTwo is a masterpiece
```

### 3. 我认为分数在 30 到 80 之间的游戏都是平庸的。《最后的捍卫者》是一部平庸的游戏。但它并不是一个糟糕的游戏。提示：用纯英语写出复杂的条件会有帮助！
在 `else if` 条件中，`AND` 运算符的左侧是错误的。在错误版本中，该条件描述为：如果分数大于 80 且分数大于 30。它应该是：如果分数小于 80 且分数大于 30。
```javascript
var game = 'theLastDefender';
var score = donkeysGameScores[game];
if (score >= 80) {
  console.log(game + ' was a fun game');
} else if (score < 80 && score > 30) {
  console.log(game + ' was an ok game');
} else {
  console.log(game + ' was a bad game');
}
// theLastDefender was an ok game
```

## 第 5 章答案

## CRACK THE CODE

### 1. 为什么在处理循环时终止条件很重要？
带有永远不会求值为 `false` 的终止语句的循环将无限循环。

### 2. 使用 `for` 循环遍历数组时，变量（通常为 `i`）被初始化为值 0。当该变量作为循环终止条件的一部分时，它的作用是什么？
对于终止条件，变量 `i` 用于跟踪循环的索引。

### 3. 使用 `for` 循环遍历数组时，变量（通常为 `i`）被初始化为值 0。当它在循环内部用于数组时，它的作用是什么？
变量 `i` 用于访问数组内部的值。

### 4. 为以下循环编写一个表格。
| ITERATION | I | CONDITION | BREED |
| :--- | :--- | :--- | :--- |
| 1 | 0 | 0 < 3 | pug |
| 2 | 1 | 1 < 3 | golden retriever |
| 3 | 2 | 2 < 3 | german shepherd |

### 5. 为以下循环编写一个表格。
| ITERATION | I | CONDITION | GAMER |
| :--- | :--- | :--- | :--- |
| 1 | 0 | 0 < 4 | super |
| 2 | 1 | 1 < 4 | smurf |
| 3 | 2 | 2 < 4 | sleepy |
| 4 | 3 | 3 < 4 | moth |

### 6. 为以下循环编写一个表格。注意非标准的增量器 `i += 2`！
| ITERATION | I | CONDITION |
| :--- | :--- | :--- |
| 1 | 0 | 0 < 7 |
| 2 | 2 | 2 < 7 |
| 3 | 4 | 4 < 7 |
| 4 | 6 | 6 < 7 |

## DEBUGGING

### 1. 代码说该数组是一个对象。
终止条件是错误的。它需要 `catBreeds.length`。
```javascript
var catBreeds = [
  'Maine Coon',
  'ragdoll'
];
for (var i = 0; i < catBreeds.length; i++) {
  console.log(catBreeds[i]);
}
```

### 2. 循环没有打印 bills。
终止条件中的运算符是错误的。应该是大于，而不是小于。
```javascript
var bills = [1, 5, 10, 20, 50];
for (var i = 0; i < bills.length; i++) {
  console.log(bills[i]);
}
```

### 3. 循环迭代多了一次。最后打印的值是 `undefined`。
错误代码中的终止条件是小于等于。应该是小于。
```javascript
var hangmanLetters = ['d', 'a', 'r', 'k', 's', 'u', 'l', 's'];
for (var i = 0; i < hangmanLetters.length; i++) {
  console.log(hangmanLetters[i]);
}
```

### 4. 循环没有打印猫的名字。
`i` 的初始化是错误的。有声明但没有赋值为 0。
```javascript
var catNames = ['Pegasus', 'Maximillion', 'Joey'];
for (var i = 0; i < catNames.length; i++) {
  console.log(catNames[i]);
}
```

### 5. 如果数组中的项是字符串，循环应该跳过数据。我正尝试使用 `continue` 来跳过。
`continue` 关键字在 `console.log` 下方。它应该在它上方。
```javascript
var mixedData = ['a', 30, 'b', 'd', 1];
for (var i = 0; i < mixedData.length; i++) {
  var currData = mixedData[i];
  if (typeof currData === 'string') {
    continue;
  }
  console.log(currData);
}
```

## 第 6 章答案

## CRACK THE CODE

### 1. 什么样的让函数受欢迎？
函数是抽象算法的好方法。这使得代码更容易理解。函数也是可重用的。常见的操作可以提取到自己的函数中。

### 2. 函数需要什么关键字才能输出在外部暴露的值？
需要 `return` 关键字。

### 3. 如果没有显式返回，函数输出什么？
没有 `return` 关键字的函数输出 `undefined`。

### 4. 什么是范围？
范围是代码内变量可用规则。

### 5. JavaScript 使用什么类型的作用域？用你的话解释它是什么。
JavaScript 使用词法作用域（lexical scoping）。在函数内部声令的变量在该函数及其内部的函数可用。变量永远在其定义的外部不可。

## DEBUGGING

### includes
提前返回语句的条件是错误的。应该是严格相等检查，而不是严格不等。
```javascript
function includes(arrOrStr, item) {
  for (var i = 0; i < arrOrStr.length; i++) {
    var currItem = arrOrStr[i];
    if (currItem === item) {
      return true;
    }
  }
  return false;
}
test('includes #1', includes('cat', 'a'), true);
test('includes #2', includes('cat', 't'), true);
test('includes #3', includes('cat', 'f'), false);
```

### createHint
在 `else` 块中，不应该是赋值。该函数的目的是增量构建一个字符串，但使用等号会覆盖之前所有的字符串构建。它应该是加法自赋值。
```javascript
function createHint(actualName, allUserGuesses) {
  var output = '';
  for (var i = 0; i < actualName.length; i++) {
    var currChar = actualName[i];
    if (includes(allUserGuesses, currChar)) {
      output += currChar;
    } else {
      output += '_ ';
    }
  }
  return output;
}
test('createHint #1', createHint('charlie', 'chle'), 'c h _ _ l _ e ');
test('createHint #2', createHint('cat', ''), '_ _ _ ');
test('createHint #3', createHint('cat', 'a'), '_ a _ ');
```

### 正确猜中
此函数用于检查 `actualName` 中的每个字符是否存在于 `allUserGuesses` 中。如果 `currChar` 不在所有玩家猜测的字符串中，我们立即知道游戏还没有结束，可以停止循环。但逻辑应该是相反的，这需要使用非运算符。
```javascript
function correctlyGuessed(actualName, allUserGuesses) {
  for (var i = 0; i < actualName.length; i++) {
    var currChar = actualName[i];
    if (!includes(allUserGuesses, currChar)) {
      return false;
    }
  }
  return true;
}
test('correctlyGuessed #1', correctlyGuessed('charlie', 'chle'), false);
test('correctlyGuessed #2', correctlyGuessed('cat', 'tac'), true);
test('correctlyGuessed #3', correctlyGuessed('cat', 'cat'), true);
```

### 是否多字符猜测
检查一个猜测是否是多个字符应该检查长度是否不等于 1。
```javascript
function isMultiCharGuess(guess) {
  return guess.length !== 1;
}
test('isMultiCharGuess #1', isMultiCharGuess('a'), false);
test('isMultiCharGuess #2', isMultiCharGuess('av'), true);
test('isMultiCharGuess #3', isMultiCharGuess('c'), false);
```

# 第 7 章答案

## 破解密码

### 1. 运行此代码后，`players` 是一个包含‘smurf’ 和‘ANS’ 的数组吗？为什么或为什么不是？
这两个名字都存在。`shift` 操作移除了数组中的第一个元素，即 'super'。

### 2. 什么是可变性？哪些数据类型是可变的？
可变性是在不创建新版本的情况下修改某部分数据的概念。`Objects`和`arrays`是可变的。所有其他数据类型都是不可变的。

### 3. 为什么字符串修改需要重新赋值，而数组和对象的修改则不需要？
在 JavaScript 中，`strings` 是不可变的。为了创建一个包含两个组合值的新字符串，必须使用某种赋值操作。

### 4. 哪些数组方法可以减小数组的大小？
`shift` 和 `pop` 方法会移除数组中的元素。它们分别从前面和后面移除一个元素。

### 5. 哪些数组方法可以增加数组的大小？
`unshift` 和 `push` 方法向数组中添加元素。它们分别在前面和后面添加一个元素。

### 6. 为以下函数画一个表格。写出每次迭代时数组的样子以及 `array.length > 0` 的情况。
| 迭代 | I | 条件 | 数组 |
| :--- | :--- | :--- | :--- |
| 1 | 0 | 5 > 0 | [10, 20, 12, 30, 25] |
| 2 | 1 | 4 > 0 | [10, 20, 12, 30] |
| 3 | 2 | 3 > 0 | [10, 20, 12] |
| 4 | 3 | 2 > 0 | [10, 20] |
| 5 | 4 | 1 > 0 | [10] |

### 7. 为以下函数画一个表格。写出每次迭代时数组的样子以及 `array.length > 0` 的情况。
| 迭代 | I | 条件 | 数组 |
| :--- | :--- | :--- | :--- |
| 1 | 0 | 5 > 0 | [10, 20, 12, 30, 25] |
| 2 | 1 | 4 > 0 | [10, 20, 12, 30] |
| 3 | 2 | 3 > 0 | [10, 20, 12] |
| 4 | 3 | 2 > 0 | [10, 20] |
| 5 | 4 | 1 > 0 | [10] |

### 7. 运行代码的输出是什么？
| 迭代 | I | 条件 | 数组 |
| :--- | :--- | :--- | :--- |
| 1 | 0 | 5 > 0 | [10, 20, 12, 30, 25] |
| 2 | 1 | 4 > 0 | [10, 20, 12, 30] |
| 3 | 2 | 3 > 0 | [10, 20, 12] |
| 4 | 3 | 2 > 0 | [10, 20] |
| 5 | 4 | 1 > 0 | [10] |

### 8. 用你自己的话描述该函数的目的。它为什么可以适用于数组和字符串？

### 9. `count` 的值是多少？

## 调试

### 正确猜中
```javascript
function correctlyGuessed(actualName, allUserGuesses) {
  for (var i = 0; i < actualName.length; i++) {
    var currChar = actualName[i];
    if (!includes(allUserGuesses, currChar)) {
      return false;
    }
  }
  return true;
}
```

### 是否多字符猜测
```javascript
function isMultiCharGuess(guess) {
  return guess.length !== 1;
}
```

# 第 8 章答案

## 破解密码

### 1. 定义什么是对象结构。

### 2. 在对象编程中定义对象。

### 3. 什么变量在所有方法中都是可用的？

### 4. 在方法内部调用方法的语法是什么？

### 5. 构造函数的语法是什么？

### 6. 什么是对象实例？

## 调试

### message
实例变量 `this.chatLog` 不是函数。它是一个应该向其中添加消息的数组。它缺少 `push` 方法。
```javascript
ChatProgram.prototype.message = function (person, message) {
  var messageEntry = {
    person: person,
    message: message
  };
  this.chatLog.push(messageEntry);
};
```

### parseMessageEntry
消息对象中没有 `chat` 键。条目中的文本在 `message` 键中。
```javascript
ChatProgram.prototype.parseMessageEntry = function (chatEntry) {
  return chatEntry.person.name + ': ' + chatEntry.message;
};
```

### getLog
数组方法 `pop` 是向数组添加元素的错误方法。应该是 `push`。在方法内部调用方法时，`this.prototype.parseMessageEntry` 应该是 `this.parseMessageEntry`。
```javascript
ChatProgram.prototype.getLog = function () {
  var parsedMessages = [];
  for (var i = 0; i < this.chatLog.length; i++) {
    var chatEntry = this.chatLog[i];
    var parsedMessage = this.parseMessageEntry(chatEntry);
    parsedMessages.push(parsedMessage);
  }
  return parsedMessages;
};
```

方法 `this.getLog` 没有被调用。
```javascript
ChatProgram.prototype.printLog = function () {
  var allMessages = this.getLog();
  for (var i = 0; i < allMessages.length; i++) {
    console.log(allMessages[i]);
  }
};
```

# 第 9 章答案

### 破解代码

### 1. 在 HTML 文件更新并保存后，浏览器不会立即更新。为什么？
因为浏览器当前加载了旧版本的 HTML 文件。刷新页面将更新它。

### 2. 什么是文档对象？
`document` 对象是 JavaScript 对 HTML 页面的表示。

### 3. `document.getElementsByClassName` 和 `document.getElementById` 的用途是什么？
这些函数用于让 JavaScript 指向并操作页面上的 HTML 元素。

### 4. `document.getElementsByClassName` 和 `document.getElementById` 有什么区别？
`document.getElementsByClassName` 搜索所有特定类名的实例，并返回一个类数组的数据结构。相比之下，`document.getElementById` 只查找一个。

### 5. 哪个属性包含 HTML 元素内部的文本？
包含文本的 JavaScript 属性是 `innerHTML`。

### 6. 什么是事件监听器？
事件监听是一个 JavaScript 函数，它会被调用一次，然后等待页面发生特定的交互。这些交互范围从按键到点击按钮不等。一旦发生交互，JavaScript 就会运行第二个参数（即函数）内部的代码。

### 7. 在我们的示例中，点击事件监听器是直接应用于按钮的。但按键事件监听器是应用于整个文档的。为什么？
事件应该在按钮上，因为要观察的事件是对它的点击。在 `document` 上的点击事件监听会在用户点击页面任何地方时触发。另一方面，按键并不特定于页面上的某个特定 HTML 元素。只要用户在页面上，我们就希望调用相应的行为。

### 8. 使用 HTML script 标签在页面加载时运行 JavaScript 代码有两种方法？
HTML `script` 标签可以包含 JavaScript 代码。也可以使用 `src` 属性从 `.js` 文件导入 JavaScript 代码。

## 调试
事件监听器被添加到了错误的元素上。将事件监听器添加到 `document` 将在任何点击时触发该行为。它必须在按钮上。此外，事件处理程序没有选择正确的 `id`。需要清除的文本位于 `id` 为 `'text'` 的 `div` 内部。
```javascript
var button = document.getElementById('delete-all');
button.addEventListener('click', function() {
  var div = document.getElementById('text');
  div.innerHTML = '';
});
```

## 术语表

- **抽象 (abstraction)**：通过隐藏实现细节使复杂操作易于使用的概念。

- **累加器 (accumulator)**：一类变量，用于在循环中逐渐构建值。

- **逻辑与运算符 (AND operator)**：关键符号 `&&`，要求两个值都为真时结果才为真。

- **算术赋值 (arithmetic assignment)**：对字符串进行数学自自操作或自组合的语法。

- **数组 (array)**：一种存储数据的数据结构；通过索引访问数据。

- **赋值 (assignment)**：将数据数据与变量关联的过程。

- **布尔 (boolean)**：表示真或假的数据类型。

- **括号表示法 (bracket notation)**：通过键访问对象数据结构中值的语法；也用于通过索引访问数组中的值。

- **跳出 (break)**：循环中用于完全退出循环的关键字。

- **驼峰命名法 (camelCase)**：第一个单词小写，后续单词首字母大写。

- **注释 (comment)**：写在代码中执行的文本。

- **编译器 (compiler)**：一次性分析并封装大量代码的程序。

- **合并 (concat)**：合并两个数组或字符串的过程；“concatenation”的缩写。

- **条件语句 (conditional statement)**：求值为真或为假的语句。

- **构造函数 (constructor function)**：作为对象实例的初始化器的函数，使用 `new` 关键字。

- **继续 (continue)**：循环中的关键字，用于停止所有后续操作并跳转到循环的下一次迭代。

- **约定 (convention)**：社区公认的编码风格。

- **CSS**：层联样式表（Cascading style sheets），一种在视觉上增强 HTML 的样式语言。

- **数据结构 (data structure)**：指代存储任意数量数据的数据类型的术语。

- **声明 (declare)**：创建变量。

- **递减 (decrement)**：将数据类型为数字的变量值减 1。

- **文档 (document)**：浏览器内部的变量，是 JavaScript 对整个网站的表示。

- **点运算符 (dot operator)**：通过键访问对象数据结构值的语法；也用于访问对象实例中的实例变量或方法的语法。

- **转义字符 (escape character)**：用于字符串；一种特殊字符，反斜杠 `\` 表示应忽略该键符号并将其视为字符串。

- **等价运算符 (equality operator)**：比较两个数据片段在值上是否相同的运算符；相等运算符使用类型转换。

- **事件监听器 (event listener)**：在后台创建并等待的函数。

- **for 循环 (for loop)**：一种在终止条件为假时将继续运行的循环。

- **函数 (function)**：一种可以将语句组合在一起的实体。

- **高级语言 (high-level language)**：一种类似于人类操作和逻辑的编程语言。

- **HTML**：超文本标记语言；一种在浏览器中渲染内容的模板语言。

- **HTMLCollection**：`getElementsByClassName` 返回的类数组数据结构。

- **if ... else if ... else 语句**：允许条件执行的特性。

- **不可变 (immutable)**：无法被修改的数据。

- **递增 (increment)**：将数据类型为数字的变量值加 1。

- **索引 (index)**：数组中条目的的位置；在 JavaScript 中，索引从 0 开始。

- **实例变量 (instance variable)**：存储在对象内部并作为其属性的变量；使用括号或点运算符访问。

- **解释器 (interpreter)**：按行分析代码的程序。

- **调用 (invoke)**：使用括号语法运行函数的过程。

- **关键字 (keyword)**：JavaScript 保留的特殊字符（及字符组）。

- **长度 (length)**：数组中的条目数量。

- **词法作用域 (lexical scope)**：变量在其定义的函数以及该函数内部的作用域内可用。

- **链接标签 (link tag)**：用于从 CSS 文件运行代码的 HTML 标签（注：此处通常指 script 标签用于运行 JS，link 标签用于引入 CSS）。

- **循环 (loop)**：编程语言的一种特性，允许代码的重复执行。

- **方法 (method)**：存储在对象中的函数；方法只能通过对象实例访问。

- **数字 (number)**：JavaScript 中的一种数据类型；表示数字。

- **NaN**：表示无逻辑数值的数字类型。

- **逻辑非运算符 (NOT operator)**：关键符号 `!`，用于反转布尔值。

- **对象 (object)**：1) 一种以键值对形式存储的数据结构；2) 一种内部持有数据和函数的实体。

- **对象实例 (object instance)**：一个内部持有自身数据的对象实体；这些值不会在对象实例间共享。

- **面向对象编程 (object-oriented programming)**：某些编程语言的一种特性，赋予程序员创建内部持有自身函数和数据实体的能力。

- **逻辑或运算符 (OR operator)**：关键符号 `||`，要求至少有一个值为真时结果才为真。

- **参数 (parameter)**：为函数创建的变量，在调用函数时可以传递其值。

- **帕斯命名法 (pascal case)**：每个单词的首字母均大写。

## 定义

- **属性 (property)**: 通过键访问的数据片段（包括方法）；适用于对象数据结构和对象实例

- **伪代码 (pseudo code)**: 用通俗英语编写的计算机算法

- **关系运算符 (relational operator)**: 比较两个数据片段之间值的运算符

- **作用域 (scope)**: 规定代码中变量和函数可用范围的规则

- **script 标签 (script tag)**: 用于运行 JavaScript 文件中代码的 HTML 标签

- **严格等等运算符 (strict equality operator)**: 比较相等性但绝不使用类型转换的运算符

- **字符串 (string)**: 表示字符的数据类型

- **类型强制转换 (type coercion)**: JavaScript 尝试在评估期间通过更改数据类型来调和不逻辑操作的过程

- **单元测试 (unit testing)**:为程序的各个部分编写测试的过程

- **变量 (variable)**: 可以与数据片段关联的名字

- **while 循环 (while loop)**: 一种直到终止条件评估为假才会停止运行的循环

# 资源

### 网站

- **LeetCode** ([LeetCode.com](http://LeetCode.com)) 是一个在线编程题库。他们为所有技能水平的编码者提供了练习题。

- **现代 JavaScript 教程** ([JavaScript.info](http://JavaScript.info)) 是 JavaScript 各个方面的高级概述。这是我的个人最爱，但它不适合胆子小的人！

- **Mozilla MDN Web Docs** ([Developer.Mozilla.org/en-US](http://Developer.mozilla.org/en-US)) 为 JavaScript 和 Web 开提供了全面的文档。它非常详细，主要供人士使用。

- **Stack Overflow** ([StackOverflow.com](http://StackOverflow.com)) 是一个面向编码者的社区驱动帮助论坛。你对编程的绝大多数问题都有该网站上的某人回答！

### 书籍

- **《清洁代码：敏捷软件工艺手册》(Clean Code: A Handbook of Agile Software Craftsmanship)**，Robert C. Martin 著，是一本关于编码风格的高级指南。随手备着。如果你花时间学习 JavaScript 提供的所有内容，这将是将你的程序员能力提升到下一个水平的方法。

# 致谢

感谢 Jae Bradley，一位出色的同事。他以及他的启发了我突破边界，努力成为最好的自己。

# 关于作者

![Author Andrew Yueh](img/image0034.jpeg)Andrew Yueh 是一位专精 JavaScript 和现代网站技术的专业软件开发人员。他拥有德克萨斯农州大学的工程硕士学位，在那里的论文巩固了他对 Web 开发的热情。

Andrew 曾在多家科技公司工作。他曾于富国银行（Wells Fargo）担任团队技术负责人，在那里他指导了多名开发人员以提高他们的编程能力。

在空余时间，他辅导高中生学习各种科目，包括 JavaScript 基础。作为一个业余程序员，他还从事多个个人编码项目，所有项目都是用 JavaScript 编写的。
