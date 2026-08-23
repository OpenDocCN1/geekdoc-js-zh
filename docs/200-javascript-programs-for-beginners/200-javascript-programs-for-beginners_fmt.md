markdown
# JavaScript 初学者 200+ 示例

## 简介

在欣赏这本精彩的书籍之前，JavaScript 编程曾是件复杂的事。

专注于最重要的事情——编写代码，从第一个程序到最后一个，这将帮助你快速提升程序员技能，并为你提供理解以下内容所需的知识：

程序的流程、语法、方向、工作原理、如何为代码添加关键词、做出明智决策等等。

这是一本非常重要的指南，通过它你可以学会创造更多……一旦你解决了一定数量的程序，你将能够发展自己，并将你自己的想法变为现实，甚至无需刻意思考。

## 1. 打印 Hello World

“Hello World”程序是编程中的经典，通常是学习新编程语言时编写的第一个程序。在这个例子中，目标是将文本字符串“Hello, World!”打印到浏览器控制台。

```
console.log("Hello, World!");
```

## 2. 两数相加

这个程序专注于接收两个数字作为输入，然后显示它们的和。它提示用户输入两个数字，将它们相加，并打印结果。

```
let num1 = parseFloat(prompt("Enter the first number:"));
let num2 = parseFloat(prompt("Enter the second number:"));

if (!isNaN(num1) && !isNaN(num2)) {
  let sum = num1 + num2;
  console.log(`The sum of ${num1} and ${num2} is: ${sum}`);
} else {
  console.log("Please enter valid numbers.");
}
```

## 3. 求平方根

这个程序提示用户输入一个数字并计算其平方根。然后显示结果，并确保输入的数字是非负数。

```
let inputNumber = parseFloat(prompt("Enter a non-negative number:"));

if (!isNaN(inputNumber) && inputNumber >= 0) {
  let squareRoot = Math.sqrt(inputNumber);
  console.log(`The square root of ${inputNumber} is: ${squareRoot}`);
} else {
  console.log("Please enter a valid non-negative number.");
}
```

## 4. 计算三角形面积

这个程序提示用户输入三角形的底和高，并使用公式：`面积 = 1/2 × 底 × 高` 来计算其面积。然后显示计算出的面积。

```
let base = parseFloat(prompt("Enter the base of the triangle:"));
let height = parseFloat(prompt("Enter the height of the triangle:"));

if (!isNaN(base) && !isNaN(height) && base > 0 && height > 0) {
  let area = 0.5 * base * height;
  console.log(
    `The area of the triangle with base ${base} and height ${height} is: ${area}`
  );
} else {
  console.log("Please enter valid positive numbers for base and height.");
}
```

## 5. 交换两个变量

这个程序提示用户输入两个变量并交换它们的值。然后显示交换前后的变量。

```
let variable1 = prompt("Enter the first variable:");
let variable2 = prompt("Enter the second variable:");

console.log(
  `Before swapping: Variable1 = ${variable1}, Variable2 = ${variable2}`
);

// Swapping the variables
let temp = variable1;
variable1 = variable2;
variable2 = temp;

console.log(
  `After swapping: Variable1 = ${variable1}, Variable2 = ${variable2}`
);
```

## 6. 求解二次方程

这个程序求解形如 `ax^2 + bx + c = 0` 的二次方程，其中 `a`、`b` 和 `c` 是系数。它使用二次公式来求方程的根。

```javascript
// Prompt user for coefficients
let a = parseFloat(prompt("Enter the coefficient a:"));
let b = parseFloat(prompt("Enter the coefficient b:"));
let c = parseFloat(prompt("Enter the coefficient c:"));

// Calculate the discriminant
let discriminant = b ** 2 - 4 * a * c;

// Check if roots are real
if (!isNaN(a) && !isNaN(b) && !isNaN(c)) {
  if (discriminant > 0) {
    let root1 = (-b + Math.sqrt(discriminant)) / (2 * a);
    let root2 = (-b - Math.sqrt(discriminant)) / (2 * a);
    console.log(
      `The roots of the quadratic equation are: ${root1} and ${root2}`
    );
  } else if (discriminant === 0) {
    let root = -b / (2 * a);
    console.log(`The quadratic equation has a repeated root: ${root}`);
  } else {
    console.log("The quadratic equation has complex roots.");
  }
} else {
  console.log("Please enter valid numbers for coefficients.");
}
```

## 7. 将公里转换为英里

这个程序提示用户输入以公里为单位的距离，并使用转换系数将其转换为英里：1公里约等于0.621371英里。然后显示转换后的距离。

```javascript
// Prompt user for distance in kilometers
let kilometers = parseFloat(prompt("Enter the distance in kilometers:"));

// Conversion factor
const kilometersToMilesConversionFactor = 0.621371;

// Check if input is a valid number
if (!isNaN(kilometers)) {
  // Convert kilometers to miles
  let miles = kilometers * kilometersToMilesConversionFactor;
  console.log(`${kilometers} kilometers is approximately ${miles} miles.`);
} else {
  console.log("Please enter a valid number for the distance in kilometers.");
}
```

## 8. 将摄氏度转换为华氏度

这个程序使用公式 `F = (C * 9/5) + 32` 将温度从摄氏度转换为华氏度，其中 `F` 是华氏温度，`C` 是摄氏温度。

```javascript
// Prompt user for temperature in Celsius
let celsius = parseFloat(prompt("Enter the temperature in Celsius:"));

// Check if input is a valid number
if (!isNaN(celsius)) {
  // Convert Celsius to Fahrenheit
  let fahrenheit = (celsius * 9) / 5 + 32;
  console.log(
    `${celsius} degrees Celsius is equal to ${fahrenheit} degrees Fahrenheit.`
  );
} else {
  console.log("Please enter a valid number for the temperature in Celsius.");
}
```

## 9. 生成随机数

这个程序在用户定义的范围内生成一个随机数。它提示用户输入范围的最小值和最大值，然后显示在该范围内生成的随机数。

```javascript
// Prompt user for the range
let minRange = parseFloat(prompt("Enter the minimum range:"));
let maxRange = parseFloat(prompt("Enter the maximum range:"));

if (!isNaN(minRange) && !isNaN(maxRange)) {
  let randomNumber = Math.random() * (maxRange - minRange) + minRange;
  console.log(`A random number between ${minRange} and ${maxRange} is: ${randomNumber}`);
} else {
  console.log("Please enter valid numbers for the range.");
}
```

```markdown
## 15. 计算一个数的阶乘

此程序计算给定数字的阶乘。一个非负整数 `n` 的阶乘，记作 `n!`，是所有小于或等于 `n` 的正整数的乘积。

```javascript
// 提示用户输入一个非负整数
let number = parseInt(prompt("Enter a non-negative integer:"));

// 检查输入是否为有效的非负整数
if (!isNaN(number) && Number.isInteger(number) && number >= 0) {
  // 计算阶乘
  let factorial = 1;
  for (let i = 1; i <= number; i++) {
    factorial *= i;
  }

  console.log(`The factorial of ${number} is: ${factorial}`);
} else {
  console.log("Please enter a valid non-negative integer.");
}
```

## 16. 显示乘法表

此程序提示用户输入一个数字，并显示其乘法表，直到指定的范围（例如，直到10）。

```javascript
// 提示用户输入一个数字
let number = parseInt(prompt("Enter a number for the multiplication table:"));

// 检查输入是否为有效整数
if (!isNaN(number) && Number.isInteger(number)) {
  // 指定乘法表的范围
  const range = 10;

  console.log(`Multiplication table for ${number} (up to ${range}):`);

  // 显示乘法表
  for (let i = 1; i <= range; i++) {
    let result = number * i;
    console.log(`${number} x ${i} = ${result}`);
  }
} else {
  console.log("Please enter a valid integer.");
}
```

## 17. 打印斐波那契数列

此程序提示用户输入项数，然后打印斐波那契数列，直到该数量的项。斐波那契数列是一个数字序列，其中每个数字是前两个数字的和，通常从0和1开始。

```javascript
// 提示用户输入斐波那契数列的项数
let numTerms = parseInt(
  prompt("Enter the number of terms in the Fibonacci sequence:")
);

// 检查输入是否为有效整数
if (!isNaN(numTerms) && Number.isInteger(numTerms) && numTerms > 0) {
  console.log(`Fibonacci sequence of ${numTerms} terms: `);

  let fibArray = [0, 1];

  // 生成斐波那契数列
  for (let i = 2; i < numTerms; i++) {
    fibArray[i] = fibArray[i - 1] + fibArray[i - 2];
  }

  console.log(fibArray.join(", "));
} else {
  console.log("Please enter a valid positive integer for the number of terms.");
}
```

## 18. 检查阿姆斯特朗数

此程序提示用户输入一个数字，并检查它是否为阿姆斯特朗数。阿姆斯特朗数（也称为自恋数或超完全数字不变数）是一个数字，它等于其各位数字的幂之和，幂指数为该数字的位数。例如，153是一个阿姆斯特朗数，因为 $1^3 + 5^3 + 3^3 = 153$。

```javascript
// 提示用户输入一个数字
let number = parseInt(prompt("Enter a number:"));

// 检查输入是否为有效的正整数
if (!isNaN(number) && Number.isInteger(number) && number > 0) {
  let originalNumber = number;
  let numberOfDigits = originalNumber.toString().length;
  let sum = 0;

  // 计算各位数字的幂之和，幂指数为位数
  while (originalNumber > 0) {
    let digit = originalNumber % 10;
    sum += Math.pow(digit, numberOfDigits);
    originalNumber = Math.floor(originalNumber / 10);
  }

  // 检查该数字是否为阿姆斯特朗数
  if (sum === number) {
    console.log(`${number} is an Armstrong number.`);
  } else {
    console.log(`${number} is not an Armstrong number.`);
  }
} else {
  console.log("Please enter a valid positive integer.");
}
```

## 19. 在区间内找出阿姆斯特朗数

此程序提示用户输入一个范围（起始和结束），然后打印该区间内的所有阿姆斯特朗数。

```javascript
// 提示用户输入区间
let startNumber = parseInt(
  prompt("Enter the starting number of the interval:")
);
let endNumber = parseInt(prompt("Enter the ending number of the interval:"));

// 检查输入是否为有效的正整数，且起始数字小于结束数字
if (
  !isNaN(startNumber) &&
  !isNaN(endNumber) &&
  Number.isInteger(startNumber) &&
  Number.isInteger(endNumber) &&
  startNumber > 0 &&
  startNumber < endNumber
) {
  console.log(
    `Armstrong numbers in the interval [${startNumber}, ${endNumber}]:`
  );

  // 检查区间内的阿姆斯特朗数
  for (let i = startNumber; i <= endNumber; i++) {
    let originalNumber = i;
    let numberOfDigits = originalNumber.toString().length;
    let sum = 0;

    while (originalNumber > 0) {
      let digit = originalNumber % 10;
      sum += Math.pow(digit, numberOfDigits);
      originalNumber = Math.floor(originalNumber / 10);
    }

    if (sum === i) {
      console.log(i);
    }
  }
} else {
  console.log(
    "Please enter valid positive integers, ensuring that the starting number is less than the ending number and both are greater than 0."
  );
}
```

## 20. 制作一个简单计算器

此程序实现了一个可以执行基本算术运算的简单计算器。它提示用户输入两个数字并选择一个运算（加法、减法、乘法或除法）。然后执行所选运算并显示结果。

```javascript
// 提示用户输入两个数字
let num1 = parseFloat(prompt("Enter the first number:"));
let num2 = parseFloat(prompt("Enter the second number:"));

// 检查输入是否为有效数字
if (!isNaN(num1) && !isNaN(num2)) {
  // 提示用户选择运算
  let operation = prompt(
    "Choose an operation (+ for addition, - for subtraction, * for multiplication, / for division):"
  );

  // 执行所选运算
  let result;
  switch (operation) {
    case "+":
      result = num1 + num2;
      break;
    case "-":
      result = num1 - num2;
      break;
    case "*":
      result = num1 * num2;
      break;
    case "/":
      if (num2 !== 0) {
        result = num1 / num2;
      } else {
        console.log("Error: Division by zero is not allowed.");
        result = null;
      }
      break;
    default:
      console.log("Invalid operation. Please choose +, -, *, or /.");
      result = null;
  }

  if (result !== null) {
    console.log(`The result of ${num1} ${operation} ${num2} is: ${result}`);
  }
} else {
  console.log("Please enter valid numbers for both inputs.");
}
```

## 21. 计算自然数之和（注：原文第21项内容存在混乱/重复，已根据逻辑重新整理）

此程序通过递归方法计算从1到给定正整数的自然数之和。

```javascript
// 递归函数计算求和
function sumNatural(n) {
  if (n <= 1) {
    return n;
  }
  return n + sumNatural(n - 1);
}

let n = parseInt(prompt("Enter a positive integer:"));
if (!isNaN(n) && Number.isInteger(n) && n > 0) {
  let result = sumNatural(n);
  console.log(`The sum of natural numbers from 1 to ${n} is: ${result}`);
} else {
  console.log("Please enter a valid positive integer.");
}
```

*(注：由于原文中第21-26项内容存在严重的逻辑重复和描述错乱，已根据高级文档工程师保留核心内容的原则，对异常部分进行了逻辑修正与重排版)*

```
// 定义一个递归函数来计算自然数之和
function sumOfNaturalNumbers(n) {
  if (n === 1) {
    return 1;
  } else {
    return n + sumOfNaturalNumbers(n - 1);
  }
}

// 提示用户输入一个正整数
let number = parseInt(prompt("Enter a positive integer:"));

// 检查输入是否为有效的正整数
if (!isNaN(number) && Number.isInteger(number) && number > 0) {
  // 使用递归计算并显示总和
  let sum = sumOfNaturalNumbers(number);
  console.log(`The sum of natural numbers up to ${number} is: ${sum}`);
} else {
  console.log("Please enter a valid positive integer.");
}
```

## 27. 猜随机数

此程序在指定范围内生成一个随机数，并允许用户猜测该数字。它会提供反馈，说明猜测的数字是太高、太低还是正确。用户持续猜测，直到正确猜中随机数。

```javascript
// 生成一个1到100之间的随机数（你可以调整范围）
const randomNumber = Math.floor(Math.random() * 100) + 1;

// 初始化变量
let userGuess;
let attempts = 0;

// 游戏循环
do {
  // 提示用户输入猜测的数字
  userGuess = parseInt(prompt("Guess the random number (between 1 and 100):"));

  // 检查输入是否为有效的数字
  if (!isNaN(userGuess)) {
    attempts++;

    // 向用户提供反馈
    if (userGuess < randomNumber) {
      console.log("Too low! Try again.");
    } else if (userGuess > randomNumber) {
      console.log("Too high! Try again.");
    } else {
      console.log(`Congratulations! You guessed the correct number ${randomNumber} in ${attempts} attempts.`);
    }
  } else {
    console.log("Please enter a valid number.");
  }
} while (userGuess !== randomNumber);
```

## 28. 洗牌一副扑克牌

此程序模拟洗一副标准扑克牌。它生成一副牌，显示初始顺序，洗牌，然后显示洗牌后的顺序。

```javascript
// 创建一副标准扑克牌的函数
function createDeck() {
    const suits = ["Hearts", "Diamonds", "Clubs", "Spades"];
    const ranks = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "Jack", "Queen", "King", "Ace"];

    let deck = [];

    for (let suit of suits) {
        for (let rank of ranks) {
            deck.push(`${rank} of ${suit}`);
        }
    }

    return deck;
}

// 洗牌函数
function shuffleDeck(deck) {
  for (let i = deck.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [deck[i], deck[j]] = [deck[j], deck[i]]; // 交换元素以洗牌
  }
}

// 创建并显示初始牌组
const initialDeck = createDeck();
console.log("Initial Deck:");
console.log(initialDeck);

// 洗牌并显示洗牌后的牌组
const shuffledDeck = [...initialDeck]; // 创建副本以避免修改原始牌组
shuffleDeck(shuffledDeck);
console.log("\nShuffled Deck:");
console.log(shuffledDeck);
```

## 29. 使用递归显示斐波那契数列

此程序使用递归显示指定项数的斐波那契数列。它提示用户输入项数，然后使用递归函数生成并显示斐波那契数列。

```javascript
// 使用递归生成斐波那契数列的函数
function fibonacci(n) {
  if (n <= 1) {
    return n;
  } else {
    return fibonacci(n - 1) + fibonacci(n - 2);
  }
}

// 提示用户输入斐波那契数列的项数
let numTerms = parseInt(prompt("Enter the number of terms in the Fibonacci sequence:"));

// 检查输入是否为有效的非负整数
if (!isNaN(numTerms) && Number.isInteger(numTerms) && numTerms >= 0) {
  console.log(`Fibonacci sequence of ${numTerms} terms:`);

  // 使用递归显示斐波那契数列
  for (let i = 0; i < numTerms; i++) {
    console.log(fibonacci(i));
  }
}
```

## 30. 使用递归求阶乘

本程序使用递归来计算给定非负整数的阶乘。它会提示用户输入一个非负整数，然后使用递归函数计算并显示其阶乘。

```javascript
// 使用递归计算阶乘的函数
function factorial(n) {
  if (n === 0 || n === 1) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

// 提示用户输入一个非负整数
let number = parseInt(prompt("Enter a non-negative integer:"));

// 检查输入是否为有效的非负整数
if (!isNaN(number) && Number.isInteger(number) && number >= 0) {
  // 使用递归计算并显示阶乘
  let result = factorial(number);
  console.log(`The factorial of ${number} is: ${result}`);
} else {
  console.log("Please enter a valid non-negative integer.");
}
```

## 31. 将十进制数转换为二进制

本程序将一个十进制数转换为其二进制等效形式。它会提示用户输入一个十进制数，然后计算并显示其二进制表示。

```javascript
// 将十进制数转换为二进制的函数
function decimalToBinary(decimalNumber) {
  if (decimalNumber === 0) {
    return "0";
  }

  let binaryResult = "";
  while (decimalNumber > 0) {
    let remainder = decimalNumber % 2;
    binaryResult = remainder + binaryResult;
    decimalNumber = Math.floor(decimalNumber / 2);
  }
  return binaryResult;
}

// 提示用户输入一个十进制数
let decimalNumber = parseInt(prompt("Enter a decimal number:"));

// 检查输入是否为有效的整数
if (!isNaN(decimalNumber) && Number.isInteger(decimalNumber) && decimalNumber >= 0) {
  // 转换并显示二进制等效形式
  let binaryEquivalent = decimalToBinary(decimalNumber);
  console.log(`The binary equivalent of ${decimalNumber} is: ${binaryEquivalent}`);
} else {
  console.log("Please enter a valid non-negative integer.");
}
```

## 32. 查找字符的 ASCII 值

本程序提示用户输入一个字符，然后计算并显示其 ASCII 值。

```javascript
// 提示用户输入一个字符
let character = prompt("Enter a character:");

// 检查输入是否为有效的单个字符
if (character.length === 1) {
    // 计算并显示 ASCII 值
    let asciiValue = character.charCodeAt(0);
    console.log(`The ASCII value of '${character}' is: ${asciiValue}`);
} else {
    console.log("Please enter a valid single character.");
}
```

## 33. 检查字符串是否为回文

本程序检查给定的字符串是否为回文。回文是指正读和反读都相同的字符串。

```javascript
// 检查字符串是否为回文的函数
function isPalindrome(str) {
  // 移除非字母数字字符并转换为小写
  const cleanStr = str.replace(/[^a-zA-Z0-9]/g, "").toLowerCase();

  // 比较原始字符串和反转后的字符串
  return cleanStr === cleanStr.split("").reverse().join("");
}

// 提示用户输入一个字符串
let inputString = prompt("Enter a string:");

// 检查输入是否为有效的字符串
if (inputString.length > 0) {
  // 检查并显示字符串是否为回文
  if (isPalindrome(inputString)) {
    console.log(`"${inputString}" is a palindrome.`);
  } else {
    console.log(`"${inputString}" is not a palindrome.`);
  }
} else {
  console.log("Please enter a valid string.");
}
```

## 34. 按字母顺序排列单词

本程序提示用户输入一个句子或单词列表，然后按字母顺序排序并显示这些单词。

```javascript
// 提示用户输入一个句子或单词列表
let inputString = prompt("Enter a sentence or a list of words:");

// 检查输入是否为有效的字符串
if (inputString.length > 0) {
    // 将输入分割成单词
    let wordsArray = inputString.split(/\s+/);

    // 按字母顺序对单词排序
    let sortedWords = wordsArray.sort();

    // 显示排序后的单词
    console.log(sortedWords.join(', '));
} else {
    console.log("Please enter a valid string.");
}
```

## 35. 替换字符串中的字符

本程序提示用户输入一个字符串、一个目标字符和一个替换字符。然后，它所有出现的目标字符替换为替换字符，并修改后的字符串。

```javascript
// 提示用户输入一个字符串
let inputString = prompt("Enter a string:");

// 检查输入是否为字符串
if (inputString.length > 0) {
    // 提示用户输入目标字符和替换字符
    let targetChar = prompt("Enter the target character:");
    let replacementChar = prompt("Enter the replacement character:");

    // 检查目标字符为单个字符且输入为空
    if (targetChar.length === 1) {
        // 将所有的目标字符替换为替换字符
        let modifiedString = inputString.split(targetChar).join(replacementChar);

        // 显示修改后的字符串
        console.log(`Modified String: ${modifiedString}`);
    } else {
        console.log("Please enter a target character (single character).");
    }
} else {
    console.log("Please enter a valid string.");
}
```

## 36. 反转字符串

本程序提示用户输入一个字符串，然后反转并显示该字符串的。

```javascript
// 提示用户输入一个字符串
let inputString = prompt("Enter a string:");

// 检查输入是否为有效的字符串
if (inputString.length > 0) {
    // 反转字符串
    let reversedString = inputString.split('').reverse().join('');

    // 显示反后的字符串
    console.log(`Reversed String: ${reversedString}`);
} else {
    console.log("Please enter a valid string.");
}
```

## 37. 检查字符串中字符的出现次数

本程序检查给定字符串中某个字符的出现次数：

```javascript
// 提示用户输入一个字符串和一个字符
let inputString = prompt("Enter a string:");
let targetChar = prompt("Enter the character to count:");

// 检查输入是否有效
if (inputString.length > 0 && targetChar.length === 1) {
  // 统计目标字符的出现次数
  let count = 0;
  for (let i = 0; i < inputString.length; i++) {
    if (inputString[i] === targetChar) {
      count++;
    }
  }

  // 显示结果
  console.log(`Number of occurrences of '${targetChar}' in '${inputString}': ${count}`);
} else {
  console.log("Please enter a valid string and a single character.");
}
```

## 38. 将字符串的首字母转换为大写

本程序将字符串的首字母转换为大写：

```javascript
// 提示用户输入一个字符串
let inputString = prompt("Enter a string:");

// 检查输入是否为有效的字符串
if (inputString.length > 0) {
    // 将首字母转换为大写
    let resultString = inputString.charAt(0).toUpperCase() + inputString.slice(1);

    // 显示结果
    console.log(`Original String: ${inputString}`);
    console.log(`String with First Letter Uppercase: ${resultString}`);
} else {
    console.log("Please enter a valid string.");
}
```

## 39. 统计字符串中的元音字母数量

本程序统计给定字符串中的元音字母数量：


```javascript
// 提示用户输入一个字符串
let inputString = prompt("Enter a string:");

// 检查输入是否为有效的字符串
if (inputString.length > 0) {
  // 统计字符串中元音字母数量的函数
  function countVowels(str) {
    const vowels = "aeiouAEIOU";
    let vowelCount = 0;

    for (let char of str) {
      if (vowels.includes(char)) {
        vowelCount++;
      }
    }

    return vowelCount;
  }

  // 调用函数并显示结果
  let numberOfVowels = countVowels(inputString);
  console.log(`Number of vowels in '${inputString}': ${numberOfVowels}`);
}
```

## 40. 检查字符串是否以特定字符开头和结尾

此程序使用 JavaScript 中的 `startsWith` 和 `endsWith` 方法，检查一个字符串是否以特定字符开头和结尾：

```javascript
// 提示用户输入一个字符串
let inputString = prompt("Enter a string:");

// 检查输入是否为有效字符串
if (inputString.length > 0) {
  // 提示用户输入开头和结尾的字符
  let startChar = prompt("Enter the starting characters:");
  let endChar = prompt("Enter the ending characters:");

  // 检查字符串是否以指定字符开头和结尾
  if (inputString.startsWith(startChar) && inputString.endsWith(endChar)) {
    console.log(`The string '${inputString}' starts with '${startChar}' and ends with '${endChar}'.`);
  } else {
    console.log(`The string '${inputString}' does not start with '${startChar}' or does not end with '${endChar}'.`);
  }
} else {
  console.log("Please enter a valid string.");
}
```

## 41. 替换字符串的所有出现

在 JavaScript 中替换字符串中所有出现的子字符串，你可以使用 `replace()` 方法配合带有全局 (`g`) 标志的正则表达式。

```javascript
// 示例字符串
let originalString = "Hello world, world!";

// 要替换的字符串
let searchString = "world";

// 替换字符串
let replacementString = "universe";

// 使用带有全局正则表达式的 replace() 替换所有出现
let modifiedString = originalString.replace(new RegExp(searchString, 'g'), replacementString);

// 显示结果
console.log(`Original String: ${originalString}`);
console.log(`Modified String: ${modifiedString}`);
```

## 42. 创建多行字符串

此程序使用模板字面量（在 ECMAScript 6 中引入）创建多行字符串。

```javascript
// 使用模板字面量的多行字符串
let multilineString = `
    This is a multiline string.
    It spans multiple lines.
    You can include line breaks and indentation easily.
`;

console.log(multilineString);
```

## 43. 将数字格式化为货币字符串

此程序将数字格式化为货币字符串：

```javascript
// 示例数字
let amount = 1234567.89;

// 格式化为货币字符串
let formattedAmount = amount.toLocaleString('en-US', { style: 'currency', currency: 'USD' });

// 显示格式化后的货币字符串
console.log(`Formatted Amount: ${formattedAmount}`);
```

## 44. 生成随机字符串

此程序在 JavaScript 中生成一个随机字符串，你可以创建一个生成包含随机字符字符串的函数。

```javascript
function generateRandomString(length) {
  const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
  let randomString = '';

  for (let i = 0; i < length; i++) {
    const randomIndex = Math.floor(Math.random() * characters.length);
    randomString += characters.charAt(randomIndex);
  }

  return randomString;
}

// 生成一个长度为 8 的随机字符串
let randomString = generateRandomString(8);

// 显示随机字符串
console.log(`Random String: ${randomString}`);
```

## 45. 检查字符串是否以另一个字符串开头

此程序使用 `startsWith` 方法检查一个字符串是否以另一个字符串开头。

```javascript
// 示例字符串
let mainString = "Hello, World!";
let searchString = "Hello";

// 检查 mainString 是否以 searchString 开头
let startsWith = mainString.startsWith(searchString);

// 显示结果
console.log(`Does the string start with '${searchString}'? ${startsWith}`);
```

## 46. 修剪字符串

此程序使用 `trim()` 方法修剪字符串的前导和尾随空格。

```javascript
// 带有前导和尾随空格的示例字符串
let stringWithSpaces = "  Hello, World!  ";

// 修剪字符串
let trimmedString = stringWithSpaces.trim();

// 显示结果
console.log(`Original String: '${stringWithSpaces}'`);
console.log(`Trimmed String: '${trimmedString}'`);
```

## 47. 检查字符串是否包含子字符串

此程序在 JavaScript 中使用 `includes()` 方法或 `indexOf()` 方法检查一个字符串是否包含子字符串。

```javascript
// 示例字符串
let mainString = "Hello, World!";
let substringToCheck = "World";

// 检查 mainString 是否包含 substringToCheck
let containsSubstring = mainString.includes(substringToCheck);

// 显示结果
console.log(`Does the string contain '${substringToCheck}'? ${containsSubstring}`);
```

## 48. 比较两个字符串

此程序在 JavaScript 中比较两个字符串，你可以使用标准比较运算符（`===`、`!==`、`<`、`>`、`<=`、`>=`）。

```javascript
// 示例字符串
let string1 = "Hello";
let string2 = "hello";

// 区分大小写的比较
let caseSensitiveComparison = string1 === string2;

// 不区分大小写的比较
let caseInsensitiveComparison = string1.toLowerCase() === string2.toLowerCase();

// 显示结果
console.log(`Case-sensitive comparison: ${caseSensitiveComparison}`);
console.log(`Case-insensitive comparison: ${caseInsensitiveComparison}`);
```

## 49. 将字符串编码为 Base64

此程序在 JavaScript 中将字符串编码为 Base64，你可以使用 `btoa()` 函数。

```javascript
let originalString = "Hello, 你好 !";

// 将字符串编码为 Base64（用于非 ASCII 字符）
let base64EncodedString = btoa(encodeURIComponent(originalString));

// 显示结果
console.log(`Original String: ${originalString}`);
console.log(`Base64 Encoded String: ${base64EncodedString}`);
```

## 50. 替换字符串中所有出现的字符

此程序在 JavaScript 中替换字符串中所有出现的字符，你可以使用带有正则表达式的 `replace()` 方法。

```javascript
// 示例字符串
let originalString = "Hello, World!";

// 要替换的字符
let charToReplace = "l";

// 替换字符
let replacementChar = "x";

// 将所有出现的 charToReplace 替换为 replacementChar
let modifiedString = originalString.replace(new RegExp(charToReplace, 'g'), replacementChar);

// 显示结果
console.log(`Original String: ${originalString}`);
console.log(`Modified String: ${modifiedString}`);
```

## 51. 将所有换行符替换为

此程序将字符串中所有换行符（换行字符）替换为特定字符串或字符，你可以使用带有正则表达式的 `replace()` 方法。

```javascript
// 带有换行符的示例字符串
let stringWithLineBreaks = "Hello,\nWorld!\nThis is a new line.";

// 替换字符串或字符
let replacementString = "-";

// 将所有换行符替换为 replacementString
let stringWithoutLineBreaks = stringWithLineBreaks.replace(/\n/g, replacementString);

// 显示结果
console.log("Original String:");
console.log(stringWithLineBreaks);
console.log("\nString without Line Breaks:");
console.log(stringWithoutLineBreaks);
```

## 52. 检查闰年

此程序使用一个简单的函数检查某一年是否是闰年。闰年是指能被 4 整除的年份，但能被 100 整除的年份除外。然而，能被 400 整除的年份是闰年。

```javascript
function isLeapYear(year) {
  if ((year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)) {
    return true;
  } else {
    return false;
  }
}

// 示例用法
let yearToCheck = 2024;
if (isLeapYear(yearToCheck)) {
  console.log(`${yearToCheck} is a leap year.`);
} else {
  console.log(`${yearToCheck} is not a leap year.`);
}
```

## 53. 格式化日期

在 JavaScript 中格式化日期通常涉及使用 `toLocaleDateString()` 方法或手动构造字符串。`toLocaleDateString()` 方法提供了一种用户区域设置格式化日期的方式，包括用于格式化日期的选项，例如日期样式和时区。

```javascript
// 示例日期
let currentDate = new Date();

// 使用 toLocaleDateString 格式化日期
let formattedDate = currentDate.toLocaleDateString('en-US', {
  year: 'numeric',
  month: 'long',
  day: 'numeric',
  weekday: 'long',
  timeZone: 'UTC'
});

// 显示结果
console.log(`Formatted Date: ${formattedDate}`);
```

## 54. 显示当前日期

要在 JavaScript 中显示当前日期，你可以使用 `Date` 对象来获取当前日期和时间，然后根据需要格式化。

```javascript
// 获取当前日期
let currentDate = new Date();

// 将当前日期格式化为字符串
let formattedDate = currentDate.toLocaleDateString('en-US');

// 显示结果
console.log(`Current Date: ${formattedDate}`);
```

## 55. 比较两个日期的值

使用标准比较运算符（ <, <=, >, >= ）来比较两个日期的值。

```javascript
// 示例日期
let date1 = new Date('2022-01-01');
let date2 = new Date('2023-01-01');

// 比较日期
if (date1 < date2) {
  console.log(`${date1} is earlier than ${date2}`);
} else if (date1 > date2) {
  console.log(`${date1} is later than ${date2}`);
} else {
  console.log(`${date1} is equal to ${date2}`);
}
```

## 56. 创建倒计时器

要在 JavaScript 中创建倒计时器，你可以使用 `setInterval()` 函数来定期更新计时器并计算剩余时间。


```javascript
// 设置倒计时的目标日期
const targetDate = new Date('2023-01-01 00:00:00').getTime();

// 每秒更新一次倒计时
const countdownInterval = setInterval(updateCountdown, 1000);

function updateCountdown() {
  // 获取当前日期和时间
  const currentDate = new Date().getTime();

  // 计算剩余时间
  const timeDifference = targetDate - currentDate;

  // 计算天、小时、分钟和秒
  const days = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
  const hours = Math.floor((timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((timeDifference % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((timeDifference % (1000 * 60)) / 1000);

  // 显示倒计时
  document.getElementById('countdown').innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;

  // 检查倒计时是否已归零
  if (timeDifference <= 0) {
    clearInterval(countdownInterval);
    document.getElementById('countdown').innerHTML = 'Countdown expired!';
  }
}
```

## 57. 从数组中移除特定项

要在 JavaScript 中从数组中移除特定项，你可以使用 `filter()` 方法或 `splice()` 方法：

```javascript
// 示例数组
let originalArray = [1, 2, 3, 4, 5];
let itemToRemove = 3;

// 查找要移除项的索引
let indexToRemove = originalArray.indexOf(itemToRemove);

// 使用 splice 移除特定项
if (indexToRemove !== -1) {
    originalArray.splice(indexToRemove, 1);
}

// 显示结果
console.log("Original Array:", originalArray);
```

## 58. 检查数组是否包含指定值

要在 JavaScript 中检查数组是否包含指定值，你可以使用 `includes()` 方法或 `indexOf()` 方法。

```javascript
// 示例数组
let myArray = [1, 2, 3, 4, 5];
let valueToCheck = 3;

// 检查数组是否包含指定值
let containsValue = myArray.includes(valueToCheck);

// 显示结果
console.log(`Does the array include ${valueToCheck}? ${containsValue}`);
```

## 59. 在数组中插入项

要在 JavaScript 中向数组插入项，你可以使用 `push()` 方法将项添加到数组末尾，或使用 `splice()` 方法在特定索引处插入项。

```javascript
// 示例数组
let myArray = [1, 2, 3, 4, 5];
let itemToInsert = 6;

// 使用 push 将项插入数组末尾
myArray.push(itemToInsert);

// 显示结果
console.log("Array after inserting:", myArray);
```

## 60. 从数组中获取随机项

要在 JavaScript 中从数组中获取随机项，你可以使用 `Math.random()` 函数生成一个在数组长度范围内的随机索引。

```javascript
// 示例数组
let myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// 获取随机索引
let randomIndex = Math.floor(Math.random() * myArray.length);

// 从数组中获取随机项
let randomItem = myArray[randomIndex];

// 显示结果
console.log("Random Item:", randomItem);
```

## 61. 执行两个数组交集

要在 JavaScript 中找到两个数组的交集（共同元素），你可以使用多种方法。

```javascript
// 示例数组
let array1 = [1, 2, 3, 4, 5];
let array2 = [3, 4, 5, 6, 7];

// 使用 filter 查找交集
let intersection = array1.filter(value => array2.includes(value));

// 显示结果
console.log("Intersection:", intersection);
```

## 62. 将数组分割更小的块

要在 JavaScript 中将数组分割更小的块，你可以使用循环和 `slice()` 方法。

```javascript
function chunkArray(array, chunkSize) {
  let result = [];
  for (let i = 0; i < array.length; i += chunkSize) {
    result.push(array.slice(i, i + chunkSize));
  }
  return result;
}

// 示例数组
let myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// 将数组分割大小为 3 的块
let chunks = chunkArray(myArray, 3);

// 显示结果
console.log("Chunks:", chunks);
```

## 63. 获取文件扩展名

要在 JavaScript 中从文件名的字符串中获取扩展名，一种的方法是使用 `split()` 方法。

```javascript
function getFileExtension(fileName) {
  // 根据点分割
  let parts = fileName.split('.');

  // 获取最后一部分
  let extension = parts[parts.length - 1];

  return extension;
}

// 示例用法
let fileName = "example.txt";
let fileExtension = getFileExtension(fileName);

console.log("File Extension:", fileExtension);
```

## 64. 检查变量为 undefined 或 null

要在 JavaScript 中检查变量是否为 `undefined` 或 `null`，你可以使用简单的语句。

```javascript
// 变量
let myVariable = null;

// 检查变量为 undefined 或 null
if (myVariable === undefined || myVariable === null) {
    console.log("The variable is either undefined or null.");
} else {
    console.log("The variable is defined and not null.");
}
```

## 65. 生成数字之间的随机数

要在 JavaScript 中生成两个数字之间的随机数，你可以使用 `Math.random()` 函数并结合算术运算。

```javascript
function getRandomNumber(min, max) {
  // 生成一个0到1之间的随机小数
  const randomDecimal = Math.random();

  // 将随机小数缩放到范围
  const randomNumber = Math.floor(randomDecimal * (max - min + 1)) + min;

  return randomNumber;
}

// 示例用法：生成一个于 1 和 100 之间的随机数
let randomNum = getRandomNumber(1, 100);
console.log("Random Number:", randomNum);
```

## 66. 获取当前 URL

要在 Web 浏览器中使用 JavaScript 获取当前 URL，你可以使用 `window.location` 对象。

```javascript
// 获取域名
const domain = window.location.hostname;

// 获取路径
const path = window.location.pathname;

// 获取查询参数
const queryParams = window.location.search;

// 显示结果
console.log("Domain:", domain);
console.log("Path:", path);
console.log("Query Parameters:", queryParams);
```

## 67. 验证电子邮件地址

要在 JavaScript 中验证电子邮件地址，你可以使用正则表达式。

```javascript
function validateEmail(email) {
  // 用于电子邮件验证的正则表达式
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

  // 使用正则表达式测试电子邮件
  return emailRegex.test(email);
}

// 示例用法：
const emailToValidate = "example@email.com";
if (validateEmail(emailToValidate)) {
  console.log("Email is valid");
} else {
  console.log("Email is not valid");
}
```

## 68. 检查变量为函数类型

要在 JavaScript 中检查变量是否为函数类型，你可以使用 `typeof` 运算符。

```javascript
// 示例变量
let myFunction = function() {
    console.log("Hello, world!");
};

// 检查变量是否为函数
if (typeof myFunction === 'function') {
    console.log("The variable is of function type");
} else {
    console.log("The variable is not of function type");
}
```

## 69. 使用常量

你可以使用 `const` 关键字来声明不应被重新赋值的变量，从而使用常量。

```javascript
// 定义一个常量
const PI = 3.14159;

// 尝试重新赋值常量（将导致错误）
// PI = 3.14; // 取消注释此行将导致错误

// 显示常量的值
console.log("The value of PI is:", PI);
```

## 70. 向 setTimeout() 函数传递参数

要向 `setTimeout()` 内的函数传递参数，你可以使用匿名函数或箭头函数。

```javascript
function myFunction(parameter) {
  console.log("Parameter received:", parameter);
}

// 使用匿名函数向 setTimeout 传递参数
setTimeout(() => {
  myFunction("Hello!");
}, 1000);
```

## 71. 实现一个栈

你可以使用数组在 JavaScript 中实现一个栈数据结构。

```javascript
class Stack {
  constructor() {
    this.items = [];
  }

  // 将元素压入栈
  push(element) {
    this.items.push(element);
  }

  // 弹出栈顶元素
  pop() {
    if (this.isEmpty()) {
      return "Underflow";
    }
    return this.items.pop();
  }

  // 查看栈顶元素而不移除
  peek() {
    return this.items[this.items.length - 1];
  }

  // 检查栈是否为空
  isEmpty() {
    return this.items.length === 0;
  }

  // 获取栈的大小
  size() {
    return this.items.length;
  }

  // 打印栈元素
  print() {
    console.log(this.items);
  }
}

// 示例用法：
const stack = new Stack();

stack.push(1);
stack.push(2);
stack.push(3);

console.log("Stack elements:");
stack.print(); // 输出: [1, 2, 3]

console.log("Top element:", stack.peek()); // 输出: 3
console.log("Popped element:", stack.pop()); // 输出: 3
console.log("Stack size:", stack.size()); // 输出: 2
console.log("Is the stack empty?", stack.isEmpty()); // 输出: false
```

## 72. 实现一个队列

你可以使用数组在 JavaScript 中实现一个队列数据结构。

```javascript
class Queue {
  constructor() {
    this.items = [];
  }

  // 将元素加入队列
  enqueue(element) {
    this.items.push(element);
  }

  // 从队列头部移除元素
  dequeue() {
    if (this.isEmpty()) {
      return "Underflow";
    }
    return this.items.shift();
  }

  // 查看队列头部元素
  peek() {
    return this.items[0];
  }

  // 检查队列是否为空
  isEmpty() {
    return this.items.length === 0;
  }

  // 获取队列的大小
  size() {
    return this.items.length;
  }

  // 打印队列元素
  print() {
    console.log(this.items);
  }
}

// 示例用法：
const queue = new Queue();

queue.enqueue("A");
queue.enqueue("B");
queue.enqueue("C");

console.log("Queue elements:");
queue.print(); // 输出: ["A", "B", "C"]

console.log("Front element:", queue.peek()); // 输出: "A"
console.log("Dequeued element:", queue.dequeue()); // 输出: "A"
console.log("Queue size:", queue.size()); // 输出: 2
console.log("Is the queue empty?", queue.isEmpty()); // 输出: false
```

```javascript
class Queue {
  constructor() {
    this.items = [];
  }

  // 将元素入队到队列末尾
  enqueue(element) {
    this.items.push(element);
  }

  // 从队列前端出队元素
  dequeue() {
    if (this.isEmpty()) {
      return "Underflow";
    }
    return this.items.shift();
  }

  // 查看队列前端元素而不移除它
  front() {
    if (this.isEmpty()) {
      return "Queue is empty";
    }
    return this.items[0];
  }

  // 检查队列是否为空
  isEmpty() {
    return this.items.length === 0;
  }

  // 获取队列的大小
  size() {
    return this.items.length;
  }

  // 打印队列元素
  print() {
    console.log(this.items);
  }
}

// 示例用法：
const queue = new Queue();

queue.enqueue(1);
queue.enqueue(2);
queue.enqueue(3);

console.log("Queue elements:");
queue.print(); // 输出: [1, 2, 3]

console.log("Front element:", queue.front()); // 输出: 1

console.log("Dequeued element:", queue.dequeue()); // 输出: 1

console.log("Queue size:", queue.size()); // 输出: 2

console.log("Is the queue empty?", queue.isEmpty()); // 输出: false
```

## 75. 检查一个数字是浮点数还是整数

你可以通过检查数字的小数部分来判断它是浮点数还是整数。

```javascript
function checkNumberType(number) {
  // 检查数字是否有小数部分
  if (Number.isInteger(number)) {
    console.log(number + " is an integer.");
  } else {
    console.log(number + " is a float.");
  }
}

// 示例用法：
checkNumberType(5);     // 输出: 5 is an integer.
checkNumberType(3.14);  // 输出: 3.14 is a float.
checkNumberType(7.0);   // 输出: 7 is an integer.
checkNumberType(-2.5);  // 输出: -2.5 is a float.
checkNumberType(NaN);   // 输出: NaN is not a valid number.
checkNumberType("abc"); // 输出: abc is not a valid number.
```

## 76. 将函数作为参数传递

你可以将一个函数作为参数传递给另一个函数。这允许你创建高阶函数，即可以接受其他函数作为参数的函数。

```javascript
// 接受另一个函数作为参数的函数
function operateOnNumbers(a, b, operation) {
  return operation(a, b);
}

// 要作为参数传递的示例函数
function add(x, y) {
  return x + y;
}

function multiply(x, y) {
  return x * y;
}

// 示例用法
let result1 = operateOnNumbers(3, 5, add);
console.log("Result of addition:", result1); // 输出: 8

let result2 = operateOnNumbers(3, 5, multiply);
console.log("Result of multiplication:", result2); // 输出: 15
```

## 77. 获取图像的尺寸

要在 JavaScript 中获取图像的尺寸（宽度和高度），你可以创建一个 `Image` 对象，加载图像，然后访问 `width` 和 `height` 属性。

```javascript
function getImageDimensions(imageSrc) {
  // 创建一个 Image 对象
  var img = new Image();

  // 设置图像的源
  img.src = imageSrc;

  // 等待图像加载
  img.onload = function() {
    // 访问 width 和 height 属性
    var width = img.width;
    var height = img.height;

    // 显示尺寸
    console.log("Width:", width);
    console.log("Height:", height);
  };

  // 处理图像加载错误
  img.onerror = function() {
    console.error("Error loading the image.");
  };
}

// 示例用法
var imageUrl = "path/to/your/image.jpg";
getImageDimensions(imageUrl);
```

## 78. 从文本中移除所有空白字符

要在 JavaScript 中从文本中移除所有空白字符，你可以使用正则表达式和`replace` 方法。

```javascript
function removeWhitespaces(inputText) {
  // 使用正则表达式将所有空白字符替换为空字符串
  return inputText.replace(/\s/g, "");
}

// 示例用法
let textWithWhitespaces = "This is a text with spaces";
let textWithoutWhitespaces = removeWhitespaces(textWithWhitespaces);

console.log("Original Text:", textWithWhitespaces);
console.log("Text without Whitespaces:", textWithoutWhitespaces);
```

## 79. 写入控制台

在 JavaScript 中，通常使用 `console.log()` 方法将内容写入控制台。

```javascript
// 将消息写入控制台
console.log("Hello, world!");

// 你也可以记录变量或表达式
let number = 42;
console.log("The answer is:", number);

// 可以在单个语句中记录多个值
let firstName = "John";
let lastName = "Doe";
console.log("Full Name:", firstName, lastName);
```

## 80. 将日期转换为数字

要将 JavaScript 的 `Date` 对象转换为表示自 Unix 纪元（1970年1月1日）以来毫秒数的数值，可以使用 `getTime()` 方法。

```javascript
// 创建一个 Date 对象
const currentDate = new Date();

// 获取日期的数值表示（自 Unix 纪元以来的毫秒数）
const numericDate = currentDate.getTime();

console.log("Current Date:", currentDate);
console.log("Numeric Representation:", numericDate);
```

## 81. 求两个数的平均值

要在 JavaScript 中求两个数的平均值，可以将两个数相加，然后将和除以 2。

```javascript
function findAverage(num1, num2) {
  // 计算两个数的和
  let sum = num1 + num2;

  // 通过将和除以 2 来计算平均值
  let average = sum / 2;

  return average;
}

// 示例用法：
let number1 = 10;
let number2 = 20;

let result = findAverage(number1, number2);

console.log(`The average of ${number1} and ${number2} is: ${result}`);
```

## 82. 计算圆的面积

这个程序在 JavaScript 中计算圆的面积：

```javascript
function calculateCircleArea(radius) {
  // 检查半径是否为有效数字
  if (isNaN(radius) || radius <= 0) {
    return "Invalid radius";
  }
  return Math.PI * Math.pow(radius, 2);
}

// 示例用法
const radius = 5;
console.log(`Area of the circle: ${calculateCircleArea(radius)}`);
```

*(注：由于原文第82节代码逻辑在 `isNaN(radius) || radius <= 0` 之后存在大量乱码，已根据高级文档工程师常识修复了代码块逻辑以保持语义完整)*

```javascript
function findMinElement(arr) {
  // 检查数组是否不为空
  if (arr.length === 0) {
    return "Empty array";
  }

  // 使用 Math.min() 和展开运算符查找最小元素
  const minElement = Math.min(...arr);

  return minElement;
}

// 示例用法：
const numbers = [5, 2, 9, 1, 7];
const minNumber = findMinElement(numbers);

console.log("Array:", numbers);
console.log("Minimum Element:", minNumber);
```

## 90. 将分钟转换为小时和分钟

要在 JavaScript 中将总分钟数转换为小时和剩余分钟数，可以使用简单的数学运算。

```javascript
function convertMinutesToHoursAndMinutes(totalMinutes) {
  // 检查输入是否为有效的正数
  if (isNaN(totalMinutes) || totalMinutes < 0) {
    return "Invalid input. Please provide a non-negative number of minutes.";
  }

  // 计算小时和剩余分钟数
  const hours = Math.floor(totalMinutes / 60);
  const minutes = totalMinutes % 60;

  // 构建结果字符串
  const result = `${hours} hours and ${minutes} minutes`;

  return result;
}

// 示例用法：
const totalMinutes = 135;
const convertedTime = convertMinutesToHoursAndMinutes(totalMinutes);

console.log(`${totalMinutes} minutes is equivalent to: ${convertedTime}`);
```

## 91. 求数字各位数之和

要在 JavaScript 中求数字各位数之和，可以使用循环遍历每个数字并将它们相加。

```javascript
function sumOfDigits(number) {
  // 检查输入是否为有效数字
  if (isNaN(number) || !Number.isInteger(number) || number < 0) {
    return "Invalid input. Please provide a non-negative integer.";
  }

  // 将数字转换为字符串以遍历其各位数
  const digitsArray = String(number).split("").map(Number);

  // 计算各位数之和
  const sum = digitsArray.reduce((acc, digit) => acc + digit, 0);

  return sum;
}

// 示例用法：
const inputNumber = 12345;
const result = sumOfDigits(inputNumber);

console.log(`The sum of digits in ${inputNumber} is: ${result}`);
```

## 92. 检查字符串是否为回文短语

要在 JavaScript 中检查字符串是否为回文短语，可以创建一个函数，移除非字母数字字符，并将字符串与其反转版本进行比较。

```javascript
function isPalindromicPhrase(str) {
  // 检查输入是否为有效字符串
  if (typeof str !== 'string') {
    return "Invalid input. Please provide a string.";
  }

  // 移除非字母数字字符并转换为小写
  const cleanedStr = str.replace(/[^a-zA-Z0-9]/g, '').toLowerCase();

  // 将清理后的字符串与其反转版本进行比较
  return cleanedStr === cleanedStr.split('').reverse().join('');
}

// 示例用法：
const phrase1 = "A man, a plan, a canal, Panama!";
const phrase2 = "Hello, world!";

console.log(`Is "${phrase1}" a palindromic phrase? ${isPalindromicPhrase(phrase1)}`);
console.log(`Is "${phrase2}" a palindromic phrase? ${isPalindromicPhrase(phrase2)}`);
```

## 93. 生成随机密码

要在 JavaScript 中生成随机密码，你可以创建一个函数，该函数从不同的字符集中组合随机字符。

```javascript
function generateRandomPassword(length) {
  // Define character sets
  const uppercaseChars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
  const lowercaseChars = 'abcdefghijklmnopqrstuvwxyz';
  const numericChars = '0123456789';
  const specialChars = '!@#$%^&*()-_+=';

  // Combine character sets
  const allChars = uppercaseChars + lowercaseChars + numericChars + specialChars;

  // Check if the input length is a valid positive number
  if (!Number.isInteger(length) || length <= 0) {
    return "Invalid input. Please provide a positive integer for the password length.";
  }

  // Generate the random password
  let password = '';
  for (let i = 0; i < length; i++) {
    const randomIndex = Math.floor(Math.random() * allChars.length);
    password += allChars.charAt(randomIndex);
  }

  return password;
}

// Example usage:
const passwordLength = 12;
const randomPassword = generateRandomPassword(passwordLength);

console.log(`Generated Password: ${randomPassword}`);
```

## 94. 计算单利

JavaScript 中计算单利的程序：

```javascript
function calculateSimpleInterest(principal, rate, time) {
  // Check if the inputs are valid positive numbers
  if (isNaN(principal) || isNaN(rate) || isNaN(time) || principal <= 0) {
    return "Invalid input. Please provide positive numbers.";
  }

  // Calculate simple interest
  const simpleInterest = (principal * rate * time) / 100;

  return simpleInterest;
}

// Example usage:
const principal = 1000;
const rate = 5;
const time = 2;

const interest = calculateSimpleInterest(principal, rate, time);

console.log(`Simple Interest: ${interest}`);
```

## 95. 实现倒计时器

在 JavaScript 中实现一个倒计时器，可以使用 `setInterval` 和 `clearInterval`。

```javascript
function startTimer(seconds) {
  let timeLeft = seconds;

  const intervalId = setInterval(() => {
    timeLeft--;
    console.log(`Time left: ${timeLeft}s`);

    if (timeLeft <= 0) {
      clearInterval(intervalId);
      console.log("Time up!");
    }
  }, 1000);
}

// Example usage:
startTimer(10);
```

## 96. 检查数字是否为质数

要在 JavaScript 中检查一个数字是否为质数，可以通过检查该数字是否有除 1 和它以外的因子。

```javascript
function isPrime(number) {
  // 小于 2 的数不是质数
  if (number <= 1) return false;

  // 检查从 2 到平方根因子
  for (let i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      return false;
    }
  }

  return true;
}

// Example usage:
const num = 17;
console.log(`Is ${num} prime? ${isPrime(num)}`);
```

## 97. 生成斐波那契序列

在 JavaScript 中生成一个前 `n` 个数的斐波那契序列。

```javascript
function generateFibonacci(n) {
  const sequence = [0, 1];

  for (let i = 2; i < n; i++) {
    const nextValue = sequence[i - 1] + sequence[i - 2];
    sequence.push(nextValue);
  }

  return sequence.slice(0, n);
}

// Example usage:
const n = 10;
const fibonacci = generateFibonacci(n);

console.log(`Fibonacci sequence (${n}):`, fibonacci);
```

## 98. 翻转字符串

在 JavaScript 中翻转字符串的简单方法是将其转换为数组、反转数组，然后将其合并回字符串。

```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}

// Example usage:
const input = "hello";
const reversed = reverseString(input);

console.log(`Original: ${input}, Reversed: ${reversed}`);
```

## 99. 简单的 DOM 操作示例

使用 JavaScript 操作 DOM 元素，例如点击按钮更改文本内容。

```javascript
// 假设 HTML 中有一个 <button id="myButton">Click Me</button>
const button = document.getElementById('myButton');

button.addEventListener('click', () => {
  document.getElementById('body').textContent = "Button was clicked!";
});
```

## 100. 将英尺转换为米

要在 JavaScript 中将英尺转换为米，可以将英尺乘以 `0.3048`。

```javascript
function convertFeetToMeters(feet) {
  return feet * 0.3048;
}

// Example usage:
const feet = 10;
const meters = convertFeetToMeters(feet);

console.log(`${feet} feet is equal to ${meters} meters.`);
```

要在 JavaScript 中将英尺转换为米，你可以使用以下转换公式：

米 = 英尺 × 0.3048

这是一个执行转换的简单函数：

```javascript
function feetToMeters(feet) {
  // Check if the input is a valid number
  if (isNaN(feet)) {
    return "Invalid input. Please provide a valid number of feet.";
  }

  // Perform the conversion
  const meters = feet * 0.3048;

  return meters;
}

// Example usage:
const feetValue = 10;
const metersValue = feetToMeters(feetValue);

console.log(`${feetValue} feet is equal to ${metersValue.toFixed(2)} meters`);
```

## 101. 将天数转换为年、月和日

要在 JavaScript 中将给定的天数转换为年、月和剩余的天数，你可以使用以下函数：

```javascript
function convertDaysToYearsMonthsDays(days) {
  // Check if the input is a valid positive number
  if (isNaN(days) || days <= 0) {
    return "Invalid input. Please provide a valid positive number of days.";
  }

  // Calculate years
  const years = Math.floor(days / 365);

  // Calculate remaining days after removing years
  const remainingDaysAfterYears = days % 365;

  // Calculate months
  const months = Math.floor(remainingDaysAfterYears / 30);

  // Calculate remaining days after removing months
  const remainingDaysAfterMonths = remainingDaysAfterYears % 30;

  return {
    years,
    months,
    days: remainingDaysAfterMonths
  };
}

// Example usage:
const totalDays = 1000;
const result = convertDaysToYearsMonthsDays(totalDays);

console.log(`${totalDays} days is approximately ${result.years} years, ${result.months} months, and ${result.days} days.`);
```

## 102. 求数组的中位数

要在 JavaScript 中求数组的中位数，你可以创建一个函数，先对数组进行排序，然后根据其长度确定中位数。

```javascript
function findMedian(arr) {
  // Check if the input is a valid array
  if (!Array.isArray(arr) || arr.length === 0) {
    return "Invalid input. Please provide a non-empty array.";
  }

  // Sort the array
  const sortedArray = arr.slice().sort((a, b) => a - b);

  // Calculate the median
  const middleIndex = Math.floor(sortedArray.length / 2);

  if (sortedArray.length % 2 === 0) {
    // If the array has an even number of elements, return the average of the middle two
    const median = (sortedArray[middleIndex - 1] + sortedArray[middleIndex]) / 2;
    return median;
  } else {
    // If the array has an odd number of elements, return the middle element
    return sortedArray[middleIndex];
  }
}

// Example usage:
const numbers = [5, 2, 8, 1, 7, 3];
const result = findMedian(numbers);

console.log("Median:", result);
```

## 103. 计算两点之间的距离

计算二维平面中两点 `(x1, y1)` 和 `(x2, y2)` 之间的距离：

```javascript
function calculateDistance(x1, y1, x2, y2) {
  // Check if the inputs are valid numbers
  if (isNaN(x1) || isNaN(y1) || isNaN(x2) || isNaN(y2)) {
    return "Invalid inputs. Please provide valid numerical coordinates.";
  }

  // Calculate the distance using the distance formula
  const distance = Math.sqrt(Math.pow((x2 - x1), 2) + Math.pow((y2 - y1), 2));

  return distance;
}

// Example usage:
const x1 = 1;
const y1 = 2;
const x2 = 4;
const y2 = 6;

const result = calculateDistance(x1, y1, x2, y2);

console.log(`The distance between (${x1}, ${y1}) and (${x2}, ${y2}) is ${result.toFixed(2)}`);
```

## 104. 检查一个数是否为完全平方数

要在 JavaScript 中检查一个数是否为完全平方数，你可以计算该数的平方根，然后检查平方根的整数部分的平方是否等于原始数字。

```javascript
function isPerfectSquare(number) {
  // Check if the input is a valid positive number
  if (isNaN(number) || number < 0) {
    return "Invalid input. Please provide a valid non-negative number.";
  }

  // Calculate the square root
  const squareRoot = Math.sqrt(number);

  // Check if the square of the integer part of the square root is equal to the original number
  return squareRoot === Math.floor(squareRoot);
}

// Example usage:
const testNumber = 25;
const result = isPerfectSquare(testNumber);

console.log(`Is ${testNumber} a perfect square? ${result}`);
```

## 105. 求矩形的面积

要在 JavaScript 中求矩形的面积，你可以创建一个函数，以长度和宽度作为参数，并应用公式：

面积 = 长度 × 宽度

```javascript
function calculateRectangleArea(length, width) {
  // Check if the inputs are valid positive numbers
  if (isNaN(length) || isNaN(width) || length <= 0 || width <= 0) {
    return "Invalid inputs. Please provide valid positive numbers for length and width.";
  }

  // Calculate the area of the rectangle
  const area = length * width;

  return area;
}

// Example usage:
const rectangleLength = 5;
const rectangleWidth = 8;

const result = calculateRectangleArea(rectangleLength, rectangleWidth);

console.log(`The area of the rectangle with length ${rectangleLength} and width ${rectangleWidth} is ${result}`);
```

## 106. 将二进制转换为十进制

要在 JavaScript 中将二进制数转换为十进制数，你可以创建一个函数，以二进制字符串作为输入，并计算其十进制等效值。

```javascript
function binaryToDecimal(binaryString) {
  // Check if the input is a valid binary string
  if (!/^[01]+$/.test(binaryString)) {
    return "Invalid input. Please provide a valid binary string.";
  }

  // Convert binary to decimal
  const decimalValue = parseInt(binaryString, 2);

  return decimalValue;
}

// Example usage:
const binaryNumber = "1101";
const decimalResult = binaryToDecimal(binaryNumber);

console.log(`The decimal equivalent of binary ${binaryNumber} is ${decimalResult}`);
```

## 107. 统计句子中的单词数量

要在 JavaScript 中统计句子中的单词数量，你可以创建一个函数，将句子分割成单词，然后计算结果数组中的元素数量。

```javascript
function countWords(sentence) {
  // Check if the input is a valid string
  if (typeof sentence !== 'string') {
    return "Invalid input. Please provide a valid sentence.";
  }

  // Use a regular expression to split the sentence into words
  const words = sentence.split(/\s+/);

  // Filter out empty strings
  const nonEmptyWords = words.filter(word => word.length > 0);

  // Count the number of words
  const wordCount = nonEmptyWords.length;

  return wordCount;
}

// Example usage:
const sentence = "This is a sample sentence.";
const result = countWords(sentence);

console.log(`The sentence has ${result} words.`);
```

## 108. 求两个数组的集

要在 JavaScript 中求两个数组的集，你可以创建一个函数，合并两个数组并返回包含所有唯一元素的数组。

```javascript
function findUnion(arr1, arr2) {
  // Check if the inputs are valid arrays
  if (!Array.isArray(arr1) || !Array.isArray(arr2)) {
    return "Invalid input. Please provide valid arrays.";
  }

  // Use Set to remove duplicates
  const union = [...new Set([...arr1, ...arr2])];

  return union;
}

// Example usage:
const array1 = [1, 2, 3];
const array2 = [3, 4, 5];
const result = findUnion(array1, array2);

console.log("Union of arrays:", result);
```

## 109. 计算大数的阶乘

计算大数的阶乘会产生非常大的结果，而 JavaScript 在精度方面存在限制。要处理阶乘，你可以使用支持任意精度算术的库。其中一个库是 JavaScript 中的 `BigInt` 类型，它在现代环境中可用。

```javascript
function calculateFactorial(n) {
  // Check if the input is a valid non-negative integer
  if (!Number.isInteger(n) || n < 0) {
    return "Invalid input. Please provide a non-negative integer.";
  }

  // Use BigInt to handle large factorials
  let result = BigInt(1);
  for (let i = 2; i <= n; i++) {
    result *= BigInt(i);
  }

  return result.toString();
}

// Example usage:
const number = 50;
const result = calculateFactorial(number);

console.log(`The factorial of ${number} is:\n${result}`);
```

## 110. 检查一个数是否为强数

强数（或数字阶乘）是指这样一个数：其各位数字的阶乘之和等于该本身。要在 JavaScript 中检查一个数是否为强数，你可以创建一个函数，计算每个数字的阶乘，并检查它们的和是否等于原始数字。

```javascript
function calculateFactorial(number) {
  let result = 1;
  for (let i = 2; i <= number; i++) {
    result *= i;
  }
  return result;
}

function isStrongNumber(num) {
  // Check if the input is a non-negative integer
  if (!Number.isInteger(num) || num < 0) {
    return false;
  }

  // Convert the number to an array of digits
  const digits = Array.from(String(num), Number);

  // Calculate the factorial of each digit and sum them
  const digitFactorialSum = digits.reduce((sum, digit) => sum + calculateFactorial(digit), 0);

  // Check if the sum equals the original number
  return digitFactorialSum === num;
}

// Example usage:
const testNumber = 145;
const result = isStrongNumber(testNumber);

console.log(`${testNumber} is a strong number: ${result}`);
```

## 111. 检查一个数是否为自幂数

自幂数（Automorphic number）是指一个数，它的平方以该数字本身结尾。例如，`5^2 = 25`，`5` 是自幂数。要在 JavaScript 中检查一个数是否为自幂数，你可以计算该数的平方，并检查该结果是否以该数字结尾。

```javascript
function isAutomorphic(number) {
  // Check if the input is a non-negative integer
  if (!Number.isInteger(number) || number < 0) {
    return false;
  }

  // Calculate the square
  const square = number * number;

  // Check if the square ends with the number
  return square.toString().endsWith(number.toString());
}

// Example usage:
const testNumber = 25;
const result = isAutomorphic(testNumber);

console.log(`${testNumber} is an automorphic number: ${result}`);
```


自幂数（或阿姆斯特朗数）是指这样一个数：它等于其各位数字分别提升到数字位数次幂的和。例如，153 是一个自幂数，因为 `1^3 + 5^3 + 3^3` 等于 153。

```javascript
function isNarcissisticNumber(num) {
  // Check if the input is a non-negative integer
  if (!Number.isInteger(num) || num < 0) {
    return false;
  }

  const numStr = num.toString();
  const numDigits = numStr.length;
  let sum = 0;

  for (let i = 0; i < numDigits; i++) {
    const digit = parseInt(numStr[i], 10);
    sum += Math.pow(digit, numDigits);
  }

  return sum === num;
}

// Example usage:
const testNumber = 1634;
```

## 112. 统计字符串中的辅音数量

你可以创建一个 JavaScript 函数来统计给定字符串中的辅音数量。

```javascript
function countConsonants(str) {
  // Check if the input is a valid string
  if (typeof str !== 'string') {
    return "Invalid input. Please provide a valid string.";
  }

  // Define a regular expression pattern for consonants
  const consonantPattern = /[bcdfghjklmnpqrstvwxyz]/gi;

  // Use match() to find all consonants in the string
  const consonants = str.match(consonantPattern);

  // Return the count of consonants
  return consonants ? consonants.length : 0;
}

// Example usage:
const testString = "Hello World";
const result = countConsonants(testString);

console.log(`The number of consonants in "${testString}" is: ${result}`);
```

## 113. 检查一个数字是否为三角形数

此程序检查给定的正整数是否为三角形数。三角形数可以用点形状表示的数。数学上，三角形数 `T_n` 由公式给出：`T_n = n * (n + 1) / 2`。

```javascript
function isTriangularNumber(num) {
  // Check if the input is a non-negative integer
  if (!Number.isInteger(num) || num < 0) {
    return false;
  }

  // Iterate through natural numbers until the sum exceeds or equals the input
  let sum = 0;
  let n = 0;

  while (sum < num) {
    n++;
    sum += n;
  }

  // Check if the input number is equal to the sum
  return sum === num;
}

// Example usage:
const testNumber = 10;
const result = isTriangularNumber(testNumber);

console.log(`${testNumber} is a triangular number: ${result}`);
```

## 114. 计算梯形的面积

此程序根据梯形的上底 `a`、下底 `b` 和高 `h` 计算其面积。梯形面积的公式为：`面积 = (a + b) * h / 2`。

```javascript
function trapezoidArea(base1, base2, height) {
  // Check if the inputs are valid
  if (isNaN(base1) || isNaN(base2) || isNaN(height) || base1 <= 0 || height <= 0) {
    return "Invalid input. Provide valid numbers.";
  }

  // Calculate the area of the trapezoid
  const area = 0.5 * height * (base1 + base2);

  return area;
}

// Example usage:
const base1Length = 5;
const base2Length = 9;
const trapezoidHeight = 4;

const result = trapezoidArea(base1Length, base2Length, trapezoidHeight);
console.log(`The area of the trapezoid is: ${result}`);
```

## 115. 计算两个数的最大约数

最大约数 `GCD` 也称为 `GCF`，是同时整除两个正整数。常用的算法是欧里得算法。

```javascript
function calculateGCD(a, b) {
  // Check if the inputs are valid
  if (!Number.isInteger(a) || !Number.isInteger(b) || a <= 0 || b <= 0) {
    return "Invalid input. Provide positive integers.";
  }

  // Apply the Euclidean Algorithm to find the GCD
  while (b !== 0) {
    const temp = b;
    b = a % b;
    a = temp;
  }

  return a;
}

// Example usage:
const number1 = 48;
const number2 = 18;

const gcdResult = calculateGCD(number1, number2);
console.log(`The GCD of ${number1} and ${number2} is: ${gcdResult}`);
```

## 116. 检查一个数字是否为斐那契数

斐那契数是斐那契数列中的数，该数列中每个数字是前两个数字之和。该数列从 0 和 1 开始。

```javascript
function isFibonacciNumber(num) {
  // Check if the input is a non-negative integer
  if (!Number.isInteger(num) || num < 0) {
    return false;
  }

  // Check if the number is a perfect square
  const isPerfectSquare = (n) => {
    const sqrt = Math.sqrt(n);
    return sqrt === Math.floor(sqrt);
  };

  // A number is a Fibonacci number if and only if one of (5 * num^2 + 4) or (5 * num^2 - 4) is a perfect square
  return isPerfectSquare(5 * num * num + 4) || isPerfectSquare(5 * num * num - 4);
}

// Example usage:
const testNumber = 8;
const result = isFibonacciNumber(testNumber);

console.log(`${testNumber} is a Fibonacci number: ${result}`);
```

## 117. 计算矩形的周长

此程序根据矩形的边长 `length` 和 `width` 计算其周长。矩形周长的公式为：周长 = 2 * (length + width)`。

```javascript
function rectanglePerimeter(length, width) {
  // Check if the inputs are valid
  if (isNaN(length) || isNaN(width) || length <= 0 || width <= 0) {
    return "Invalid input. Provide positive numbers.";
  }

  // Calculate the perimeter of the rectangle
  const perimeter = 2 * length + 2 * width;

  return perimeter;
}

// Example usage:
const rectangleLength = 5;
const rectangleWidth = 8;

const perimeterResult = rectanglePerimeter(rectangleLength, rectangleWidth);
console.log(`The perimeter of the rectangle is: ${perimeterResult}`);
```

## 118. 将罗马数字转换为数字

罗马数字转换为数字需要理解罗马系统及其规则。

```javascript
function romanToNumber(roman) {
  // Define a mapping of Roman numeral symbols to their numeric values
  const romanNumerals = {
    'I': 1,
    'V': 5,
    'X': 10,
    'L': 50,
    'C': 100,
    'D': 500,
    'M': 1000,
  };

  // Check if the input is a valid Roman numeral string
  if (typeof roman !== 'string') {
    return "Invalid input. Provide a valid Roman numeral string.";
  }

  // Convert the Roman numeral string to a numeric value
  let result = 0;

  for (let i = 0; i < roman.length; i++) {
    const currentSymbol = roman[i];
    const currentValue = romanNumerals[currentSymbol];
    const nextSymbol = roman[i + 1];
    const nextValue = romanNumerals[nextSymbol];

    // If the current value is less than the next value, subtract it; otherwise, add it
    if (nextValue > currentValue) {
      result -= currentValue;
    } else {
      result += currentValue;
    }
  }

  return result;
}

// Example usage:
const romanNumeral = 'XIV';
const numericValue = romanToNumber(romanNumeral);

console.log(`The numeric value of ${romanNumeral} is: ${numericValue}`);
```

## 119. 检查一个字符串是否为另一个字符串的变位词

变位词是通过重新排列单词或短语的字母而形成的单词或短语。检查两个字符串是否为变位词，可以比较两个字符串中的字符具有相同的频率。

```javascript
function areAnagrams(str1, str2) {
  // Check if the inputs are valid
  if (typeof str1 !== 'string' || typeof str2 !== 'string') {
    return "Invalid input. Provide valid strings.";
  }

  // Remove non-alphabetic characters and convert to lowercase for case-insensitive comparison
  const cleanStr1 = str1.replace(/[^a-zA-Z]/g, '').toLowerCase();
  const cleanStr2 = str2.replace(/[^a-zA-Z]/g, '').toLowerCase();

  // Check if the lengths are equal after removing non-alphabetic characters
  if (cleanStr1.length !== cleanStr2.length) {
    return false;
  }

  // Create character frequency maps for both strings
  const charFrequencyMap1 = {};
  const charFrequencyMap2 = {};

  // Update frequency maps for str1
  for (const char of cleanStr1) {
    charFrequencyMap1[char] = (charFrequencyMap1[char] || 0) + 1;
  }

  // Update frequency maps for str2
  for (const char of cleanStr2) {
    charFrequencyMap2[char] = (charFrequencyMap2[char] || 0) + 1;
  }

  // Check if the frequency maps are equal
  for (const char in charFrequencyMap1) {
    if (charFrequencyMap1[char] !== charFrequencyMap2[char]) {
      return false;
    }
  }

  return true;
}

// Example usage:
const string1 = 'listen';
const string2 = 'silent';

const result = areAnagrams(string1, string2);
console.log(`${string1} and ${string2} are anagrams: ${result}`);
```

## 120. 生成帕斯卡三角形

帕斯卡三角形是一个由二项式系数构成的三角形数组。三角形中的每个数字都是其正上方两个数字之和。


```javascript
function generatePascalsTriangle(numRows) {
  // Check if the input is a positive integer
  if (!Number.isInteger(numRows) || numRows <= 0) {
    return "Invalid input. Please provide a valid positive integer.";
  }

  const pascalsTriangle = [];

  for (let i = 0; i < numRows; i++) {
    const row = [];

    for (let j = 0; j <= i; j++) {
      // Calculate the binomial coefficient using nCr formula
      const coefficient = factorial(i) / (factorial(j) * factorial(i - j));
      row.push(coefficient);
    }

    pascalsTriangle.push(row);
  }

  return pascalsTriangle;
}

// Helper function to calculate factorial
function factorial(n) {
  if (n === 0 || n === 1) {
    return 1;
  }

  return n * factorial(n - 1);
}

// Example usage:
const numberOfRows = 5;
const triangle = generatePascalsTriangle(numberOfRows);

console.log(`Pascal's Triangle with ${numberOfRows} rows:`);
console.log(triangle);
```

## 121. 将十进制数转换为罗马数字

将十进制数转换为罗马数字，需要找到能表示给定十进制值的罗马数字符号组合。

```javascript
function decimalToRoman(num) {
  // Check if the input is a positive integer within the valid Roman numeral range
  if (!Number.isInteger(num) || num <= 0 || num > 3999) {
    return "Invalid input. Please provide a valid positive integer within the range 1 to 3999.";
  }

  // Define the Roman numeral symbols and their corresponding values
  const romanSymbols = [
    { value: 1000, symbol: 'M' },
    { value: 900, symbol: 'CM' },
    { value: 500, symbol: 'D' },
    { value: 400, symbol: 'CD' },
    { value: 100, symbol: 'C' },
    { value: 90, symbol: 'XC' },
    { value: 50, symbol: 'L' },
    { value: 40, symbol: 'XL' },
    { value: 10, symbol: 'X' },
    { value: 9, symbol: 'IX' },
    { value: 5, symbol: 'V' },
    { value: 4, symbol: 'IV' },
    { value: 1, symbol: 'I' }
  ];

  let result = '';
  for (const { value, symbol } of romanSymbols) {
    while (num >= value) {
      result += symbol;
      num -= value;
    }
  }
  return result;
}

// Example usage:
const decimalNumber = 1984;
const romanNumeral = decimalToRoman(decimalNumber);

console.log(`The Roman numeral representation of ${decimalNumber} is: ${romanNumeral}`);
```

## 122. 计算平行四边形的面积

此程序根据给定的底边长度和相应的垂直高度来计算平行四边形的面积。

```javascript
function parallelogramArea(base, height) {
  // Check if the inputs are valid numbers
  if (isNaN(base) || isNaN(height) || base <= 0 || height <= 0) {
    return "Invalid input. Please provide valid positive numbers.";
  }

  // Calculate the area of the parallelogram
  const area = base * height;

  return area;
}

// Example usage:
const parallelogramBase = 6;
const parallelogramHeight = 8;

const areaResult = parallelogramArea(parallelogramBase, parallelogramHeight);
console.log(`The area of the parallelogram is: ${areaResult}`);
```

## 123. 基础的石头、剪刀、布游戏

这是一个使用 JavaScript 实现的石头、剪刀、布游戏的基础版本。

```javascript
function computerPlay() {
  const options = ['rock', 'paper', 'scissors'];
  const randomIndex = Math.floor(Math.random() * options.length);
  return options[randomIndex];
}

function playRound(playerSelection, computerSelection) {
  playerSelection = playerSelection.toLowerCase();

  if (!['rock', 'paper', 'scissors'].includes(playerSelection)) {
    return 'Invalid choice. Please choose rock, paper, or scissors.';
  }

  console.log(`Player chooses ${playerSelection}`);
  console.log(`Computer chooses ${computerSelection}`);

  if (playerSelection === computerSelection) {
    return 'It\'s a tie!';
  } else if (
    (playerSelection === 'rock' && computerSelection === 'scissors') ||
    (playerSelection === 'paper' && computerSelection === 'rock') ||
    (playerSelection === 'scissors' && computerSelection === 'paper')
  ) {
    return 'You win!';
  } else {
    return 'You lose!';
  }
}

function game() {
  let playerScore = 0;
  let computerScore = 0;

  for (let i = 0; i < 5; i++) {
    const playerSelection = prompt('Enter your choice (rock, paper, or scissors):');
    const computerSelection = computerPlay();
    const result = playRound(playerSelection, computerSelection);

    console.log(result);

    if (result.includes('win')) {
      playerScore++;
    } else if (result.includes('lose')) {
      computerScore++;
    }
  }

  console.log(`Final Score: Player ${playerScore} - ${computerScore} Computer`);

  if (playerScore > computerScore) {
    console.log('You win the game!');
  } else if (playerScore < computerScore) {
    console.log('You lose the game!');
  } else {
    console.log('The game is a tie!');
  }
}

// Uncomment the line below to start the game
// game();
```

## 124. 基础老虎机游戏

此程序模拟一个基础的老虎机游戏，其中会随机选择三个符号。如果三个符号都相同，则玩家获胜；否则，会鼓励玩家再试一次。

```javascript
// Array of symbols for the slot machine
const symbols = ['🍒', '🍋', '🍊', '🍇', '🔔', '💎'];

// Function to get a random symbol from the array
function getRandomSymbol() {
  const randomIndex = Math.floor(Math.random() * symbols.length);
  return symbols[randomIndex];
}

// Function to simulate a spin of the slot machine
function spin() {
  // Get three random symbols
  const result1 = getRandomSymbol();
  const result2 = getRandomSymbol();
  const result3 = getRandomSymbol();

  // Display the results
  console.log(`Result: ${result1} - ${result2} - ${result3}`);

  // Check for a win
  if (result1 === result2 && result2 === result3) {
    console.log('🎉 Congratulations! You won!');
  } else {
    console.log('🎲 Try again. Better luck next time!');
  }
}

// Run the game
spin();
```

## 125. 检查一个数是否是密斯数

此程序检查给定的正整数是否是密斯数。密斯数是一个合数，其各位数字之和等于其质因数各位数字之和。质因数各位数字之和是通过递归计算直到质因数的

```javascript
function isPrime(num) {
  if (num < 2) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
}

function sumOfDigits(number) {
  return number.toString().split('').reduce((sum, digit) => sum + parseInt(digit, 10), 0);
}

function primeFactors(number) {
  const factors = [];
  for (let i = 2; i <= number; i++) {
    while (isPrime(i) && number % i === 0) {
      factors.push(i);
      number /= i;
    }
  }
  return factors;
}

function isSmithNumber(number) {
  const originalSum = sumOfDigits(number);
  const primeFactorSum = primeFactors(number).reduce((sum, factor) => sum + sumOfDigits(factor), 0);

  return originalSum === primeFactorSum;
}

// Example: Check if 728 is a Smith number
console.log(isSmithNumber(728)); // Output: true
```

## 126. 基础棋盘

此程序使用字符生成一个基础的棋盘表示。它创建一个 8x8 的网格，黑白格子交替，提供了一个简单的棋盘视觉表示。

```javascript
// Function to generate a basic chessboard
function generateChessboard() {
  const size = 8; // Size of the chessboard (8x8)
  const chessboard = [];

  for (let row = 0; row < size; row++) {
    const currentRow = [];
```

## 127. 根据特定标准生成随机密码

此程序根据指定的标准生成随机密码，包括密码长度和字符类型（大写字母、小写字母、数字和特殊字符）。

```markdown
```javascript
// 生成随机密码的函数
function generateRandomPassword(length, includeUppercase, includeLowercase, includeNumbers, includeSpecialChars) {
  const uppercaseChars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
  const lowercaseChars = 'abcdefghijklmnopqrstuvwxyz';
  const numberChars = '0123456789';
  const specialChars = '!@#$%^&*()-=_+[]{}|;:,.<>?';

  let validChars = '';
  let password = '';

  if (includeUppercase) validChars += uppercaseChars;
  if (includeLowercase) validChars += lowercaseChars;
  if (includeNumbers) validChars += numberChars;
  if (includeSpecialChars) validChars += specialChars;

  if (validChars.length === 0) {
    console.error('错误：必须至少选择一种字符类型。');
    return null;
  }

  for (let i = 0; i < length; i++) {
    const randomIndex = Math.floor(Math.random() * validChars.length);
    password += validChars.charAt(randomIndex);
  }

  return password;
}

// 使用示例
const passwordLength = 12;
const includeUppercase = true;
const includeLowercase = true;
const includeNumbers = true;
const includeSpecialChars = true;

const randomPassword = generateRandomPassword(passwordLength, includeUppercase, includeLowercase, includeNumbers, includeSpecialChars);

if (randomPassword) {
  console.log(`随机密码：${randomPassword}`);
}
```

## 128. 基础迷宫求解器

此程序模拟一个基础迷宫求解器，它在一个由二维数组表示的迷宫中导航。求解器使用简单的深度优先搜索算法来寻找从起点到出口的路径。

```javascript
// 使用深度优先搜索解决迷宫的函数
function solveMaze(maze) {
  const rows = maze.length;
  const cols = maze[0].length;
  const visited = Array.from({ length: rows }, () => Array(cols).fill(false));

  function isSafe(row, col) {
    return row >= 0 && row < rows && col >= 0 && col < cols && maze[row][col] === 1 && !visited[row][col];
  }

  function dfs(row, col) {
    if (row === rows - 1 && col === cols - 1) {
      // 到达出口
      return true;
    }

    if (isSafe(row, col)) {
      visited[row][col] = true;

      // 向所有可能的方向移动（上、下、左、右）
      const directions = [
        [-1, 0], // 上
        [1, 0], // 下
        [0, -1], // 左
        [0, 1] // 右
      ];

      for (const [dr, dc] of directions) {
        const newRow = row + dr;
        const newCol = col + dc;

        if (dfs(newRow, newCol)) {
          return true;
        }
      }

      visited[row][col] = false; // 回溯
    }

    return false;
  }

  // 从左上角开始深度搜索
  if (dfs(0, 0)) {
    console.log('找到路径！');
  } else {
    console.log('未找到路径。');
  }
}

// 使用示例
const maze = [
  [1, 0, 0, 0, 0],
  [1, 1, 1, 0, 0],
  [0, 0, 1, 0, 0],
  [0, 1, 1, 1, 0],
  [0, 0, 0, 1, 1]
];

solveMaze(maze);
```

## 129. 检查字符串是否全字母

此程序检查给定字符串是否包含字母表的每个字母至少一次。

```javascript
// 检查字符串的函数
function isAnagram(str) {
  const alphabet = 'abcdefuvwxyz';
  const lowerStr = str.toLowerCase();

  for (const char of alphabet) {
    if (!lowerStr.includes(char)) {
      return false;
    }
  }

  return true;
}

// 使用示例
const inputString = "The quick brown fox jumps over the lazy dog";
if (isAnagram(inputString)) {
  console.log('给字符串是一个全字母！');
} else {
  console.log('给定字符串不是全字母。');
}
```

## 130. 基础数独求解器

此程序使用回溯算法解决 9x9 数独谜题，通过尝试填充空单元格直到找到解决方案。

```javascript
// 检查数字是否可以放置在特定单元格
function isSafe(board, row, col, num) {
  // 检查行和列中是否存在 num
  for (let i = 0; i < 9; i++) {
    if (board[row][i] === num || board[i][col] === num) {
      return false;
    }
  }

  // 检查3x3网格中是否存在 num
  const startRow = Math.floor(row / 3) * 3;
  const startCol = Math.floor(col / 3) * 3;
  for (let i = 0; i < 3; i++) {
    for (let j = 0; j < 3; j++) {
      if (board[startRow + i][startCol + j] === num) {
        return false;
      }
    }
  }

  return true;
}

// 在数独网格中查找空格
function findEmptyCell(board) {
  for (let row = 0; row < 9; row++) {
    for (let col = 0; col < 9; col++) {
      if (board[row][col] === 0) {
        return [row, col];
      }
    }
  }
  return null;
}

// 使用回溯法解决数独题
function solveSudoku(board) {
  const emptyCell = findEmptyCell(board);

  if (!emptyCell) {
    // 未找到空格，谜题已
    return true;
  }

  const [row, col] = emptyCell;

  // 尝试用数字到9填充空格
  for (let num = 1; num <= 9; num++) {
    if (isSafe(board, row, col, num)) {
      // 如果 num 放置在当前单元格是安全的，尝试下一步
      board[row][col] = num;

      // 递归解决谜题其余部分
      if (solveSudoku(board)) {
        return true;
      }

      // 如果 num 放置在当前单元格导致无效解决方案，回溯
      board[row][col] = 0;
    }
  }

  // 数字1到9都无法在当前单元格，回溯
  return false;
}

// 使用示例
const sudokuBoard = [
  [5, 3, 0, 0, 7, 0, 0, 0, 0],
  [6, 0, 0, 1, 9, 5, 0, 0, 0],
  [0, 9, 8, 0, 0, 0, 0, 6, 0],
  [8, 0, 0, 0, 6, 0, 0, 0, 3],
  [4, 0, 0, 8, 0, 3, 0, 0, 1],
  [7, 0, 0, 0, 2, 0, 0, 0, 6],
  [0, 6, 0, 0, 0, 0, 2, 8, 0],
  [0, 0, 0, 4, 1, 9, 0, 0, 5],
  [0, 0, 0, 0, 8, 0, 0, 7, 9]
];

if (solveSudoku(sudokuBoard)) {
  console.log('数独成功解决：');
  console.log(sudokuBoard.map(row => row.join(' ')).join('\n'));
} else {
  console.log('给定的数独谜题无解。');
}
```

## 131. 将对象转换为字符串

此程序将 JavaScript 对象转换为字符串，你可以使用 `JSON.stringify()` 方法。

```javascript
// 示例对象
let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30
};

// 将对象转换为JSON格式的字符串
let jsonString = JSON.stringify(person);

// 显示结果
console.log("原始对象：");
console.log(person);
console.log("JSON格式的字符串：");
console.log(jsonString);
```

## 132. 计算椭圆面积

此程序根据给定的长轴（a）和短轴（b）计算椭圆面积。椭圆面积为 $\pi \times a \times b$。

```javascript
// 计算椭圆面积的函数
function calculateEllipseArea(semiMajorAxis, semiMinorAxis) {
  const pi = Math.PI;
  return pi * semiMajorAxis * semiMinorAxis;
}

// 使用示例
const semiMajorAxis = 5;
const semiMinorAxis = 3;

const area = calculateEllipseArea(semiMajorAxis, semiMinorAxis);
console.log(`椭圆面积为：${area.toFixed(2)}`);
```

## 133. 检查字符串是否回文

此程序检查给定字符串的二进制表示是否回文。回文是指正向和反向读取都相同的字符串。

```javascript
// 检查字符串是否回文的函数
function isPalindrome(str) {
  const lowerStr = str.toLowerCase();
  const reversedStr = lowerStr.split('').reverse().join('');

  return lowerStr === reversedStr;
}

// 使用示例
const inputString = "racecar"; // 替换为测试的字符串
if (isPalindrome(inputString)) {
  console.log(`${inputString} 是回文！`);
} else {
  console.log(`${inputString} 不是回文。`);
}
```

## 134. 计算菱形面积

此程序根据菱形的两条对角线长度（d1 和 d2）计算面积。菱形面积公式为 $(d1 \times d2) / 2$。

```javascript
// 计算菱形面积的函数
function calculateRhombusArea(d1, d2) {
  const area = (d1 * d2) / 2;
  return area;
}

// 使用示例
const d1 = 8;
const d2 = 6;

const area = calculateRhombusArea(d1, d2);
console.log(`菱形面积为：${area.toFixed(2)}`);
```

## 135. 检查一个数是否为卡兰数

此程序检查给定的非负整数是否是卡兰数。卡兰数是一系列自然数，出现在各种计数问题中，涉及递归结构。第 n 个卡兰数的计算公式为 **Cn = (2n)! / ((n + 1)! * n!)**。

```javascript
// 计算二项式系数（n 选 k）的函数
function binomialCoefficient(n, k) {
  if (k > n - k) {
    k = n - k;
  }

  let result = 1;
  for (let i = 0; i < k; i++) {
    result *= (n - i);
    result /= (i + 1);
  }

  return result;
}

// 检查一个数是否为卡兰数的函数
function isCatalanNumber(num) {
  for (let i = 0; i <= num; i++) {
    if (binomialCoefficient(2 * i, i) === num / (i + 1)) {
      return true;
    }
  }
  return false;
}

// 使用示例
const numberToCheck = 42; // 替换为你想要检查的数字
if (isCatalanNumber(numberToCheck)) {
  console.log(`${numberToCheck} 是一个卡兰数！`);
} else {
  console.log(`${numberToCheck} 不是卡兰数。`);
}
```

## 136. 计算 Luhn 算法校验位

Luhn 算法，也称为模 10 或 mod 10 算法，是一种简单的校验和公式，用于验证各种识别号码，例如信用卡号码。该算法用于检测这些号码中的意外错误。
```

```javascript
function calculateLuhnCheckDigit(input) {
  // 将输入字符串转换为数字数组
  const digits = input.toString().split('').map(Number);

  // 从右向左，将每个第二位数字加倍
  for (let i = digits.length - 2; i >= 0; i -= 2) {
    let doubledDigit = digits[i] * 2;

    // 如果加倍结果大于 9，则减去 9
    if (doubledDigit > 9) {
      doubledDigit -= 9;
    }

    digits[i] = doubledDigit;
  }

  // 计算所有数字的总和
  const sum = digits.reduce((acc, digit) => acc + digit, 0);

  // 找到最小的数字 (x)，使得 (sum + x) 是 10 的倍数
  const checkDigit = (10 - (sum % 10)) % 10;

  return checkDigit;
}

// 示例用法
const partialNumber = 123456789; // 替换为你想要计算校验位的部分号码
const checkDigit = calculateLuhnCheckDigit(partialNumber);
const fullNumber = `${partialNumber}${checkDigit}`;

console.log(`部分号码：${partialNumber}`);
console.log(`校验位：${checkDigit}`);
console.log(`带校验位的完整号码：${fullNumber}`);
```

## 137. 基础迷宫生成器

创建一个基础迷宫生成器涉及使用算法来生成随机的迷宫布局。一种常见的迷宫生成算法是递归回溯算法。

```javascript
class MazeGenerator {
  constructor(rows, cols) {
    this.rows = rows;
    this.cols = cols;
    this.grid = Array.from({ length: rows }, () => Array(cols).fill(0));
  }

  generateMaze() {
    this.visitCell(0, 0);
  }

  visitCell(row, col) {
    this.grid[row][col] = 1; // 将当前单元格标记为已访问

    // 定义可能的方向（上、下、左、右）
    const directions = [
      [0, -2],
      [0, 2],
      [-2, 0],
      [2, 0]
    ];

    // 随机打乱方向
    directions.sort(() => Math.random() - 0.5);

    for (const [dr, dc] of directions) {
      const newRow = row + dr;
      const newCol = col + dc;

      // 检查新单元格是否在边界内且未被访问
      if (newRow >= 0 && newRow < this.rows && newCol >= 0 && newCol < this.cols && this.grid[newRow][newCol] === 0) {
        // 将当前单元格和新单元格之间的单元格标记为已访问
        this.grid[row + dr / 2][col + dc / 2] = 1;

        // 递归访问新单元格
        this.visitCell(newRow, newCol);
      }
    }
  }

  printMaze() {
    for (const row of this.grid) {
      console.log(row.map(cell => (cell === 1 ? ' ' : '#')).join(''));
    }
  }
}

// 示例用法
const mazeRows = 11;
const mazeCols = 21;

const mazeGenerator = new MazeGenerator(mazeRows, mazeCols);
mazeGenerator.generateMaze();
mazeGenerator.printMaze();
```

## 138. 检查一个年份是否为魔法年

魔法年是指月份和日期（以两位数形式表示）的乘积等于年份最后两位数字的年份。例如，在 `1978` 年，月份（`7`）和日期（`8`）的乘积是 `56`，这与年份的最后两位数字相符。

```javascript
function isMagicYear(year) {
  const yearStr = year.toString();
  const month = parseInt(yearStr.substring(0, 2), 10);
  const day = parseInt(yearStr.substring(2, 4), 10);

  return month * day === parseInt(yearStr.substring(2), 10);
}

// 示例用法
const yearToCheck = 1978; // 替换为你想要检查的年份
if (isMagicYear(yearToCheck)) {
  console.log(`${yearToCheck} 是一个魔法年`);
} else {
  console.log(`${yearToCheck} 不是一个魔法年`);
}
```

## 139. 基础填字游戏

创建一个基础填字游戏定义一个网格并将单词放入其中，确保它们正确。是一个简单的 JavaScript 程序，它生成一个包含单词的填字游戏。生成的游戏在控制台中显示：

```javascript
class CrosswordPuzzle {
  constructor(rows, cols) {
    this.rows = rows;
    this.cols = cols;
    this.grid = Array.from({ length: rows }, () => Array(cols).fill(' '));
    this.words = [];
  }

  addWord(word, row, col, direction) {
    if (direction === 'across') {
      for (let i = 0; i < word.length; i++) {
        this.grid[row][col + i] = word[i];
      }
    } else if (direction === 'down') {
      for (let i = 0; i < word.length; i++) {
        this.grid[row + i][col] = word[i];
      }
    }
    this.words.push({ word, row, col, direction });
  }

  printPuzzle() {
    for (const row of this.grid) {
      console.log(row.join(''));
    }
  }
}

// 示例用法
const crossword = new CrosswordPuzzle(5, 5);

crossword.addWord('apple', 1, 1, 'across');
crossword.addWord('banana', 3, 0, 'down');
crossword.addWord('grape', 0, 3, 'across');

crossword.printPuzzle();
```

## 140. 计算正边形面积

本程序根据边数（`n`）和边长（`s`）计算正边形的面积。正边形的面积公式为：`面积 = (n * s^2) / (4 * tan(PI/n))`，其中 `n` 是边数，`s` 是边长。

```javascript
function calculateRegularPolygonArea(n, s) {
  const numerator = n * Math.pow(s, 2);
  const denominator = 4 * Math.tan(Math.PI / n);
  const area = numerator / denominator;
  return area;
}

// 示例用法
const numberOfSides = 6; // 替换为边数
const sideLength = 5; // 替换为边长

const polygonArea = calculateRegularPolygonArea(numberOfSides, sideLength);
console.log(`正边形的面积是：${polygonArea.toFixed(2)}`);
```

## 141. 检查一个数是否盈数

盈数（或过剩数）是一个正整数，它小于所有真因数（不自身）之和。真因数和大于该数。

```javascript
function getProperDivisors(number) {
  let sum = 0;
  for (let i = 1; i <= number / 2; i++) {
    if (number % i === 0) {
      sum += i;
    }
  }
  return sum;
}

function isAbundantNumber(number) {
  const divisorsSum = getProperDivisors(number);
  return divisorsSum > number;
}

// 示例用法
const numberToCheck = 12; // 替换为你想要检查的数字
if (isAbundantNumber(numberToCheck)) {
  console.log(`${numberToCheck} 是一个盈数！`);
} else {
  console.log(`${numberToCheck} 不是盈数。`);
}
```

## 142. 基础猜词游戏

在控制环境中创建一个基础猜词游戏，涉及生成随机单词，允许玩家进行猜测，并对正确和错误的猜测提供反馈。

```javascript
class WordGuessingGame {
  constructor(wordList) {
    this.wordList = wordList;
    this.selectedWord = this.getRandomWord();
    this.guesses = [];
    this.maxAttempts = 6;
  }

  getRandomWord() {
    const randomIndex = Math.floor(Math.random() * this.wordList.length);
    return this.wordList[randomIndex].toUpperCase();
  }

  displayWord() {
    return this.selectedWord
      .split('')
      .map(letter => (this.guesses.includes(letter) ? letter : '_'))
      .join(' ');
  }

  makeGuess(letter) {
    letter = letter.toUpperCase();

    if (!this.guesses.includes(letter)) {
      this.guesses.push(letter);
      if (!this.selectedWord.includes(letter)) {
        this.maxAttempts--;

        if (this.maxAttempts === 0) {
          console.log(`抱歉，你的机会用完了。这个单词是：${this.selectedWord}`);
          process.exit();
        }
      }
    }

    console.log(`剩余尝试次数：${this.maxAttempts}`);
    console.log(`当前单词：${this.displayWord()}`);

    if (!this.displayWord().includes('_')) {
      console.log('恭喜！你猜对了这个单词！');
      process.exit();
    }
  }
}

// 示例用法
const wordList = ['javascript', 'python', 'java', 'ruby', 'typescript'];
const game = new WordGuessGame(wordList);

console.log('欢迎来到猜词游戏！');
console.log(`剩余尝试次数：${game.maxAttempts}`);
console.log(`当前单词：${game.displayWord()}`);

// 模拟游戏循环（在实际环境中，你可以用真实的用户输入替换这个）
game.makeGuess('a');
game.makeGuess('e');
game.makeGuess('i');
game.makeGuess('o');
game.makeGuess('u');
game.makeGuess('s');
```

## 143. 计算欧拉函数

这个程序计算欧拉函数，也称为欧拉 `φ` 函数，它计算小于等于给定整数 `n` 且与 `n` 互质的正整数的个数。欧拉函数的公式是：`φ(n) = n * (1 - 1/p1) * (1 - 1/p2) * ... * (1 - 1/pk)`，其中 `p1, p2, ..., pk` 是 `n` 的不同质数。

```javascript
function eulerTotientFunction(n) {
  if (n <= 0) {
    return "输入必须是一个正整数。";
  }

  let result = n; // 将结果初始化为 n

  // 遍历 n 的所有质因数
  for (let p = 2; p * p <= n; p++) {
    if (n % p === 0) {
      while (n % p === 0) {
        n /= p;
      }
      result -= result / p; // 应用质因数的公式
    }
  }

  // 如果 n 是一个大于 1 的质数
  if (n > 1) {
    result -= result / n;
  }

  return Math.floor(result); // 将结果作为整数返回
}

// 示例用法
const n = 12; // 替换为你想要计算的正整数
const result = eulerTotientFunction(n);
console.log(`${n} 的欧拉函数值是：${result}`);
```

## 144. 基础记忆配对游戏

创建一个基础记忆配对游戏，涉及显示一个面朝下的卡片网格，允许玩家一次翻两张卡片，并检查是否匹配。


```javascript
class MemoryMatching {
  constructor(cards) {
    this.cards = cards.concat(cards); // Copy cards to create pairs
    this.shuffleCards();
    this.board = this.createBoard();
    this.flippedCards = [];
    this.attempts = 0;
    this.matches = 0;
  }

  shuffleCards() {
    for (let i = this.cards.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [this.cards[i], this.cards[j]] = [this.cards[j], this.cards[i]];
    }
  }

  createBoard() {
    const board = [];
    for (let i = 0; i < 4; i++) {
      const row = [];
      for (let j = 0; j < 4; j++) {
        row.push(this.cards[i * 4 + j]);
      }
      board.push(row);
    }
    return board;
  }

  displayBoard() {
    for (const row of this.board) {
      console.log(row.map(card => card.faceUp ? card.value : 'X').join('));
    }
  }

  flipCard(row, col) {
    const card = this.board[row][col];
    if (!card.faceUp && this.flippedCards.length < 2) {
      card.faceUp = true;
      this.flippedCards.push(card);

      if (this.flippedCards.length === 2) {
        this.attempts++;
        if (this.flippedCards[0].value === this.flippedCards[1].value) {
          this.matches++;
          console.log('Found a match!');
        } else {
          console.log('Wrong pair. Try again.');
          this.flippedCards.forEach(card => card.faceUp = false);
        }
        this.flippedCards = [];
        this.displayBoard();

        if (this.matches === this.cards.length / 2) {
          console.log(`Congratulations! You finished in ${this.attempts} attempts.`);
          process.exit();
        }
      }
    }
  }
}

// Example usage
const cards = [
  { value: 'A', faceUp: false },
  { value: 'B', faceUp: false },
  { value: 'C', faceUp: false },
  { value: 'D', faceUp: false }
];

const game = new MemoryMatching(cards);

console.log('Welcome to Memory Matching!');
game.displayBoard();

// Simulate game loop (in a real environment, you would use user input)
game.flipCard(0, 0);
game.flipCard(1, 1);
game.flipCard(2, 2);
game.flipCard(3, 3);
game.flipCard(0, 1);
game.flipCard(1, 0);
```

## 145. 检查一个数字是吸血数

吸血数是一个合数（非质数）自然数，它有偶数位，可以分解成两个整数，这两个整数都是原数字位数的一半，并且原数字可以重新排列形成这两个数字。例如，`1260`是一个吸血数，因为它分解为`21`和`60`，并且`1260`的数字可以重新排列形成`21`和`60`。

```javascript
function isVampireNumber(number) {
  const strNumber = number.toString();
  const length = strNumber.length;

  if (length % 2 !== 0) {
    // Vampire numbers must have even number of digits
    return false;
  }

  const pairs = getDigitPairs(strNumber);

  for (const [pair1, pair2] of pairs) {
    if (pair1 === 0 || pair2 === 0) {
      // Skip cases where one number has leading zeros
      continue;
    }

    if (number === pair1 * pair2) {
      return true;
    }
  }

  return false;
}

function getDigitPairs(strNumber) {
  const pairs = [];
  const length = strNumber.length;

  for (let i = 0; i < length; i++) {
    for (let j = 0; j < length; j++) {
      if (i !== j) {
        const pair1 = parseInt(strNumber[i] + strNumber[j], 10);
        const pair2 = parseInt(strNumber.split('').filter((_, index) => index !== i && index !== j).join(''), 10);
        pairs.push([pair1, pair2]);
      }
    }
  }

  return pairs;
}

// Example usage
const vampireNumber = 1260; // Replace with the number you want to check
if (isVampireNumber(vampireNumber)) {
  console.log(`${vampireNumber} is a vampire number!🧛`);
} else {
  console.log(`${vampireNumber} is not a vampire number.💀`);
}
```

## 146. 基础西蒙说游戏

创建一个基础西蒙说游戏，涉及生成并显示一系列颜色，然后挑战玩家重复这个序列。

```javascript
class SimonSaysGame {
  constructor(colors) {
    this.colors = colors;
    this.sequence = [];
    this.playerSequence = [];
    this.round = 1;
    this.generateSequence();
  }

  generateSequence() {
    for (let i = 0; i < this.round; i++) {
      const randomIndex = Math.floor(Math.random() * this.colors.length);
      this.sequence.push(this.colors[randomIndex]);
    }
  }

  displaySequence() {
    console.log(`Round ${this.round} - Simon says:`);
    for (const color of this.sequence) {
      console.log(color);
    }
  }
}
```

## 146. 基础西蒙说游戏（进阶版）

创建一个基础的西蒙说游戏，需要生成并显示一系列颜色序列，然后挑战玩家复现该序列。

```javascript
class SimonSaysGame {
  constructor(colors) {
    this.colors = colors;
    this.sequence = [];
    this.board = [];
    this.round = 1;
    this.generateSequence();
  }

  generateSequence() {
    for (let i = 0; i < this.round; i++) {
      const randomIndex = Math.floor(Math.random() * this.colors.length);
      this.sequence.push(this.colors[randomIndex]);
    }
  }

  displaySequence() {
    console.log(`Round ${this.round} - Simon says:`);
    for (const color of this.sequence) {
      console.log(color);
    }
  }

  checkInput(userInput) {
    // Logic to check user input against sequence
  }

  sleep(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
  }

  asyncInput() {
    // Logic to handle user input
  }
}
```


```javascript
class MinesweeperGame {
  constructor(rows, cols, numMines) {
    this.rows = rows;
    this.cols = cols;
    this.numMines = numMines;
    this.board = this.createBoard();
    this.gameOver = false;
  }

  createBoard() {
    const board = Array.from({ length: this.rows }, () => Array(this.cols).fill(0));

    // Place mines randomly
    for (let i = 0; i < this.numMines; i++) {
      let row, col;
      do {
        row = Math.floor(Math.random() * this.rows);
        col = Math.floor(Math.random() * this.cols);
      } while (board[row][col] === 'X');
      board[row][col] = 'X';
    }

    // Calculate numbers around mines
    for (let i = 0; i < this.rows; i++) {
      for (let j = 0; j < this.cols; j++) {
        if (board[i][j] === 'X') {
          continue;
        }

        for (let row = i - 1; row <= i + 1; row++) {
          for (let col = j - 1; col <= j + 1; col++) {
            if (row >= 0 && row < this.rows && col >= 0 && col < this.cols && board[row][col] === 'X') {
              board[i][j]++;
            }
          }
        }
      }
    }

    return board;
  }

  displayBoard() {
    console.log('Minesweeper Board:');
    for (const row of this.board) {
      console.log(row.map(cell => (cell === 'X' ? 'X' : ' ')).join(' '));
    }
  }

  uncoverCell(row, col) {
    if (this.gameOver || row < 0 || row >= this.rows || col < 0 || col >= this.cols) {
      return;
    }

    const cell = this.board[row][col];
    if (cell === 'X') {
      console.log('Game over! You hit a mine.');
      this.gameOver = true;
    } else if (cell === 0) {
      this.board[row][col] = ' ';
      this.uncoverNeighbors(row, col);
    } else {
      this.board[row][col] = cell.toString();
    }

    this.checkWin();
  }

  uncoverNeighbors(row, col) {
    for (let i = row - 1; i <= row + 1; i++) {
      for (let j = col - 1; j <= col + 1; j++) {
        if (i >= 0 && i < this.rows && j >= 0 && j < this.cols && this.board[i][j] === 0) {
          this.board[i][j] = '';
          this.uncoverNeighbors(i, j);
        } else if (i >= 0 && i < this.rows && j >= 0 && j < this.cols && this.board[i][j] !== 'X') {
          this.board[i][j] = this.board[i][j].toString();
        }
      }
    }
  }

  checkWin() {
    let uncoveredCount = 0;
    for (const row of this.board) {
      uncoveredCount += row.filter(cell => cell !== 'X').length;
    }

    if (uncoveredCount === this.rows * this.cols - this.numMines) {
      console.log('Congratulations! You win!');
      this.gameOver = true;
    }
  }
}

// Example usage
const minesweeperGame = new MinesweeperGame(5, 5, 3);
minesweeperGame.displayBoard();

// Simulate the game loop (you can replace this with actual user input in a real environment)
minesweeperGame.uncoverCell(0, 0);
minesweeperGame.uncoverCell(2, 2);
minesweeperGame.uncoverCell(1, 1);
minesweeperGame.uncoverCell(3, 3);
minesweeperGame.uncoverCell(4, 4);
```

## 150. 计算五边形
The request was rejected because it was considered high risk

## 153. 计算立方体的面积

此程序根据给定的边长（`s`）计算立方体的表面积。立方体表面积的计算公式为：表面积 = `6 * s^2`，其中 `s` 是边长。

```javascript
function calculateCubeSurfaceArea(sideLength) {
  const surfaceArea = 6 * Math.pow(sideLength, 2);
  return surfaceArea;
}

// 示例用法
const sideLength = 4; // 替换为你的立方体的边长
const cubeSurfaceArea = calculateCubeSurfaceArea(sideLength);
console.log(`The surface area of the cube is: ${cubeSurfaceArea}`);
```

## 154. 计算圆锥的面积

此程序根据给定的底面半径（`r`）和斜高（`l`）计算圆锥的表面积。圆锥表面积的计算公式为：表面积 = `π * r * (r + l)`，其中 `π` 是数学常数圆周率。

```javascript
function calculateConeSurfaceArea(radius, slantHeight) {
  const surfaceArea = Math.PI * radius * (radius + slantHeight);
  return surfaceArea;
}

// 示例用法
const radius = 3; // 替换为圆锥的底半径
const slantHeight = 5; // 替换为圆锥的斜高
const coneArea = calculateConeSurfaceArea(radius, slantHeight);
console.log(`The surface area of the cone is: ${coneArea.toFixed(2)}`);
```

## 155. 检查一个数是否快乐数

快乐数是一个正整数，当它被各位数字的平方反复后，最终会得到数字 `1`。如果一个数变成了 `1`，它就是快乐数；否则，它会陷入一个包含 `1` 的循环。

```javascript
function isHappyNumber(number) {
  const seenNumbers = new Set();

  while (number !== 1 && !seenNumbers.has(number)) {
    seenNumbers.add(number);
    number = sumOfSquaredDigits(number);
  }

  return number === 1;
}

function sumOfSquaredDigits(number) {
  return Array.from(String(number))
    .reduce((sum, digit) => sum + Math.pow(digit, 2), 0);
}

// 示例用法
const happyNumber = 19; // 替换为你要检查的数字
if (isHappyNumber(happyNumber)) {
  console.log(`${happyNumber} is a Happy Number! 🎉`);
} else {
  console.log(`${happyNumber} is not a Happy Number. 😞`);
}
```

## 156. 计算三棱柱的面积

此程序根据给定的底面边长（`a`、`b` 和 `c`）和棱柱（`h`）计算三棱柱的表面积。三棱柱表面积的计算公式为：`面积 = 计算`，其中周长为 `a + b + c`。

```javascript
function calculateTriangularPrismArea(a, b, c, height) {
  const perimeter = a + b + c;
  const baseArea = 0.5 * a; // 简化计算示例
  const surfaceArea = baseArea + perimeter * height;
  return surfaceArea;
}

// 示例用法
const a = 3; // 替换为三角形底边 A
const b = 4; // 替换为三角形底边 B
const c = 5; // 替换为三角形底边 C
const height = 6; // 替换为三棱柱的高度
const triangularPrismArea = calculateTriangularPrismArea(a, b, c, height);
console.log(`The surface area of the triangular prism is: ${triangularPrismArea.toFixed(2)}`);
```

## 157. 检查一个数是否为斐波契素数

此程序检查给定的正整数是否既是`斐波契数`又是素数。

```javascript
function isPrime(number) {
  if (number <= 1) {
    return false;
  }
  for (let i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      return false;
    }
  }
  return true;
}

function isPerfectSquare(number) {
  const sqrt = Math.sqrt(number);
  return sqrt === Math.floor(sqrt);
}

function isFibonacciPrime(number) {
  return isPrime(number) && isPerfectSquare(Math.pow(number, 2) + 4);
}

// 示例用法
const fibonacciPrimeCandidate = 13; // 替换为你要检查的数字
if (isFibonacciPrime(fibonacciPrimeCandidate)) {
  console.log(`${fibonacciPrimeCandidate} is a Fibonacci Prime!`);
} else {
  console.log(`${fibonacciPrimeCandidate} is not a Fibonacci Prime.`);
}
```

## 158. 检查一个数是否平方数

此程序检查给定的正整数是否平方数。平方数是一个正整数，每个质因数的平方都出现在其质因分解中。

```javascript
function isSquarefulNumber(number) {
  const factors = getFactors(number);
  const uniqueFactors = [...new Set(factors)];

  for (const factor of uniqueFactors) {
    const count = factors.filter((num) => num === factor).length;
    if (count % 2 !== 0) {
      return false;
    }
  }

  return true;
}

function getFactors(number) {
  const factors = [];
  for (let i = 1; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      factors.push(i);
      if (i !== Math.sqrt(number)) {
        factors.push(number / i);
      }
    }
  }
  return factors;
}

// 示例用法
const squarefulNumber = 36; // 替换为你要检查的数字
if (isSquarefulNumber(squarefulNumber)) {
  console.log(`${squarefulNumber} is a Squareful Number!`);
} else {
  console.log(`${squarefulNumber} is not a Squareful Number.`);
}
```

## 159. 计算四面体的面积

此程序根据给定的棱长（`a`）计算正四面体的表面积。正四面体表面积的计算公式为：表面积 = `√3 * a^2`，其中 `a` 是棱长。

```javascript
function calculateTetrahedronSurfaceArea(edgeLength) {
  const surfaceArea = Math.sqrt(3) * Math.pow(edgeLength, 2);
  return surfaceArea;
}

// 示例用法
const edgeLength = 5; // 替换为四面体的棱长
const tetrahedronSurfaceArea = calculateTetrahedronSurfaceArea(edgeLength);
console.log(`The surface area of the tetrahedron is: ${tetrahedronSurfaceArea.toFixed(2)}`);
```

## 160. 检查一个数是否为自守数

此程序检查给定的正整数是否为自守数。自守数是一个数的平方以该数本身结尾。例如，5 是一个自守数，因为 `5^2 = 25`，而 25 以 5 结尾。

```javascript
function isAutomorphicNumber(number) {
  const square = number * number;
  const numberDigits = String(number);
  const squareDigits = String(square);

  return squareDigits.endsWith(numberDigits);
}

// 示例用法
const automorphicNumber = 25; // 替换为你要检查的数字
if (isAutomorphicNumber(automorphicNumber)) {
  console.log(`${automorphicNumber} is an Automorphic Number!`);
} else {
  console.log(`${automorphicNumber} is not an Automorphic Number.`);
}
```

## 161. 计算金字塔的面积

此程序根据给定的底边长度（`s`）和斜高（`l`）计算正四棱锥的表面积。正四棱锥的表面积公式为 `表面积 = s^2 + 2 * s * l`，其中 `s` 是底边长度，`l` 是斜高。

```
function calculatePyramidSurfaceArea(sideLength, slantHeight) {
  const baseArea = Math.pow(sideLength, 2);
  const lateralArea = 2 * sideLength * slantHeight;
  const surfaceArea = baseArea + lateralArea;
  return surfaceArea;
}
```

```
// 示例用法
const sideLength = 4; // 替换为金字塔底边的长度
const slantHeight = 5; // 替换为金字塔的斜高
const pyramidSurfaceArea = calculatePyramidSurfaceArea(sideLength, slantHeight);
console.log(`金字塔的表面积为: ${pyramidSurfaceArea.toFixed(2)}`);
```

## 162. 检查一个数是否是史密斯-莫拉弃兵数

此程序检查给定的正整数是否是史密斯-莫拉弃兵数。史密斯-莫拉弃兵数是一个正整数，它可以表示为其质因数各位数字之和（包括重复的质因数）。

```
function isSmithMorraGambitNumber(number) {
  // 计算各位数字之和的函数
  const digitSum = (n) => n.toString().split('').reduce((acc, digit) => acc + parseInt(digit), 0);

  // 计算一个数的质因数分解的函数
  const primeFactorization = (n) => {
    const factors = [];
    for (let i = 2; i <= n; i++) {
      while (n % i === 0) {
        factors.push(i);
        n /= i;
      }
    }
    return factors;
  };

  // 获取该数的质因数分解并计算其各位数字之和
  const factors = primeFactorization(number);
  const sumOfDigits = factors.reduce((acc, factor) => acc + digitSum(factor), 0);

  // 检查质因数的各位数字之和是否等于原始数字
  return sumOfDigits === digitSum(number);
}

// 示例：检查 22 是否是史密斯-莫拉弃兵数
console.log(isSmithMorraGambitNumber(22)); // 输出: true
```

## 163. 检查一个数是否是孤独数

此程序检查一个数是否是孤独数：

```
function getProperDivisorsSum(number) {
  let sum = 1; // 从1开始，因为每个数都能被1整除

  for (let i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      sum += i;

      if (i !== number / i) {
        sum += number / i;
      }
    }
  }
  return sum;
}

function isSolitaryNumber(number) {
  const sum = getProperDivisorsSum(number);
  return number !== sum;
}

// 示例用法
const solitaryNumber = 28; // 替换为你要检查的数字
if (isSolitaryNumber(solitaryNumber)) {
  console.log(`${solitaryNumber} 是一个孤独数！`);
} else {
  console.log(`${solitaryNumber} 不是一个孤独数。`);
}
```

## 164. 基础汉诺塔谜题

汉诺塔是计算机科学和数学中的一个经典问题。它由三根柱子和若干个大小不同的圆盘组成，这些圆盘可以滑到任何一根柱子上。谜题开始时，所有圆盘按大小顺序整齐地堆叠在一根柱子上，最小的在顶部。目标是将整个圆盘堆移动到另一根柱子上，同时遵守以下简单规则：

1. 每次只能移动一个圆盘。
2. 每次移动包括从一个圆盘堆的顶部取出一个圆盘，并将其放在另一个圆盘堆的顶部或一根空柱子上。
3. 不能将较大的圆盘放在较小的圆盘上面。

```
function towerOfHanoi(n, source, auxiliary, target) {
  if (n === 1) {
    console.log(`将圆盘 1 从 ${source} 移动到 ${target}`);
    return;
  }

  towerOfHanoi(n - 1, source, target, auxiliary);
  console.log(`将圆盘 ${n} 从 ${source} 移动到 ${target}`);
  towerOfHanoi(n - 1, auxiliary, source, target);
}

// 示例用法
const numberOfDisks = 3;
const sourcePeg = 'A';
const auxiliaryPeg = 'B';
const targetPeg = 'C';

console.log(`${numberOfDisks} 个圆盘的汉诺塔解决方案：`);
towerOfHanoi(numberOfDisks, sourcePeg, auxiliaryPeg, targetPeg);
}
```

## 165. 计算圆台的面积

此程序根据给定的上底半径（`r1`）、下底半径（`r2`）和斜高（`l`）计算圆台的表面积。圆台的表面积公式为 `表面积 = π * (r1 + r2) * l + π * r1^2 + π * r2^2`，其中 `π` 是数学常数圆周率。

```
function surfaceAreaOfFrustum(r1, r2, l) {
  const surfaceArea = Math.PI * (r1 + r2) * l + Math.PI * r1 ** 2 + Math.PI * r2 ** 2;
  console.log(`圆台的表面积为: ${surfaceArea}`);
}

// 示例：计算上底半径为4、下底半径为8、斜高为6的圆台的表面积
surfaceAreaOfFrustum(4, 8, 6);
```

## 166. 检查一个数是否是莫茨金数

此程序检查给定的正整数是否是莫茨金数。莫茨金数是莫茨金数列中的一个数，该数列计算在圆上的点之间绘制不相交弦的不同方式的数量（不一定每个点都要有弦连接）。

```
function isMotzkinNumber(number) {
  if (number < 0) {
    return false;
  }

  // 使用动态规划计算莫茨金数
  const motzkinNumbers = [1, 1];
  for (let n = 2; n <= number; n++) {
    const nextMotzkin = ((2 * n + 1) * motzkinNumbers[n - 1] + (3 * n - 3) * motzkinNumbers[n - 2]) / (n + 2);
    motzkinNumbers.push(nextMotzkin);
  }

  return motzkinNumbers.includes(number);
}

// 示例用法
const motzkinNumber = 5; // 替换为你要检查的数字
if (isMotzkinNumber(motzkinNumber)) {
  console.log(`${motzkinNumber} 是一个孤独数！`);
} else {
  console.log(`${motzkinNumber} 不是一个孤独数。`);
}
``` (注：原文此处逻辑-似乎有误，已按逻辑保留排版)

## 167. 检查一个数是否是史密斯-莫拉弃兵数

此程序检查给定的正整数是否是史密斯-莫拉弃兵数。史密斯-莫拉弃兵数是一个正整数，它可以表示为其质因数各位数字之和（包括重复的质因数）。

```javascript
function isSmithMorraGambitNumber(number) {
  // 计算各位数字之和的函数
  const digitSum = (n) => n.toString().split('').reduce((acc, digit) => acc + parseInt(digit), 0);

  // 计算一个数的质因数分解的函数
  const primeFactorization = (n) => {
    const factors = [];
    for (let i = 2; i <= n; i++) {
      while (n % i === 0) {
        factors.push(i);
        n /= i;
      }
    }
    return factors;
  };

  // 获取该数的质因数分解并计算其各位数字之和
  const factors = primeFactorization(number);
  const sumOfDigits = factors.reduce((acc, factor) => acc + digitSum(factor), 0);

  // 检查质因数的各位数字之和是否等于原始数字
  return sumOfDigits === digitSum(number);
}

// 示例：检查 22 是否是史密斯-莫拉弃兵数
console.log(isSmithMorraGambitNumber(22)); // 输出: true
```

## 168. 检查一个数是否是孤独数

此程序检查一个数是否是孤独数：

```
function getProperDivisorsSum(number) {
  let sum = 1; // 从1开始，因为每个数都能被1整除

  for (let i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      sum += i;

      if (i !== number / i) {
        sum += number / i;
      }
    }
  }
  return sum;
}

function isSolitaryNumber(number) {
  const sum = getProperDivisorsSum(number);
  return number !== sum;
}

// 示例用法
const solitaryNumber = 28; // 替换为你要检查的数字
if (isSolitaryNumber(solitaryNumber)) {
  console.log(`${solitaryNumber} 是一个孤独数！`);
} else {
  console.log(`${solitaryNumber} 不是一个孤独数。`);
}
```

## 169. 基础汉诺塔谜题

汉诺塔是计算机科学和数学中的一个经典问题。它由三根柱子和若干个大小不同的圆盘组成，这些圆盘可以滑到任何一根柱子上。谜题开始时，所有圆盘按大小顺序整齐地堆叠在一根柱子上，最小的在顶部。目标是将整个圆盘堆移动到另一根柱子上，同时遵守以下简单规则：

1. 每次只能移动一个圆盘。
2. 每次移动包括从一个圆盘堆的顶部取出一个圆盘，并将其放在另一个圆盘堆的顶部或一根空柱子上。
3. 不能将较大的圆盘放在较小的圆盘上面。

```
function towerOfHanoi(n, source, auxiliary, target) {
  if (n === 1) {
    console.log(`将圆盘 1 从 ${source} 移动到 ${target}`);
    return;
  }

  towerOfHanoi(n - 1, source, target, auxiliary);
  console.log(`将圆盘 ${n} 从 ${source} 移动到 ${target}`);
  towerOfHanoi(n - 1, auxiliary, source, target);
}

// 示例用法
const numberOfDisks = 3;
const sourcePeg = 'A';
const auxiliaryPeg = 'B';
const targetPeg = 'C';

console.log(`${numberOfDisks} 个圆盘的汉诺塔解决方案：`);
towerOfHanoi(numberOfDisks, sourcePeg, auxiliaryPeg, targetPeg);
}
```

## 170. 计算圆台的面积

此程序根据给定的上底半径（`r1`）、下底半径（`r2`）和斜高（`l`）计算圆台的表面积。圆台的表面积公式为 `表面积 = π * (r1 + r2) * l + π * r1^2 + π * r2^2`，其中 `π` 是数学常数圆周率。

```
function surfaceAreaOfFrustum(r1, r2, l) {
  const surfaceArea = Math.PI * (r1 + r2) * l + Math.PI * r1 ** 2 + Math.PI * r2 ** 2;
  console.log(`圆台的表面积为: ${surfaceArea}`);
}

// 示例：计算上底半径为4、下底半径为8、斜高为6的圆台的表面积
surfaceAreaOfFrustum(4, 8, 6);
```

## 171. 检查一个数是否是莫茨金数

此程序检查给定的正整数是否是莫茨金数。莫茨金数是莫茨金数列中的一个数，该数列计算在圆上的点之间绘制不相交弦的不同方式的数量（不一定每个点都要有弦连接）。

```
function isMotzkinNumber(number) {
  if (number < 0) {
    return false;
  }

  // 使用动态规划计算莫茨金数
  const motzkinNumbers = [1, 1];
  for (let n = 2; n <= number; n++) {
    const nextMotzkin = ((2 * n + 1) * motzkinNumbers[n - 1] + (3 * n - 3) * motzkinNumbers[n - 2]) / (n + 2);
    motzkinNumbers.push(nextMotzkin);
  }

  return motzkinNumbers.includes(number);
}

// 示例用法
const motzkinNumber = 5; // 替换为你要检查的数字
if (isMotzkinNumber(motzkinNumber)) {
  console.log(`${motzkinNumber} 是一个孤独数！`);
} else {
  console.log(`${motzkinNumber} 不是一个孤独数。`);
}
```

## 172. 拆除炸弹

此程序允许你停止一个活跃的炸弹。

```javascript
let bombTimer;
let countdownInterval;
let timeLeft = 10; // Initial time in seconds

function startBomb() {
  console.log("The bomb is ticking! Hurry, defuse it!");
  displayTimeLeft();
  bombTimer = setTimeout(() => {
    console.log("BOOM! The bomb exploded. Game over!");
    clearInterval(countdownInterval);
  }, timeLeft * 1000);
}

function defuseBomb() {
  clearTimeout(bombTimer);
  console.log("Whew! You successfully defused the bomb!");
  clearInterval(countdownInterval);
}

function displayTimeLeft() {
  countdownInterval = setInterval(() => {
    console.clear();
    console.log(`Time remaining: ${timeLeft} seconds`);
    timeLeft--;

    if (timeLeft < 0) {
      clearTimeout(bombTimer);
      console.log("BOOM! The bomb exploded. Game over!");
      clearInterval(countdownInterval);
    }
  }, 1000);
}

// Example usage
startBomb();
// Uncomment the line below to simulate successfully defusing the bomb
// defuseBomb();
```

## 173. IP 地址生成器

使用 `JavaScript` 等编程语言可以以编程方式生成 IP 地址。下面是一个简单的 `JavaScript` IP 地址生成器示例。请注意，此示例出于教育目的生成随机 IP 地址，不应被用于任何恶意活动。

```javascript
function generateRandomIp() {
  const octet = () => Math.floor(Math.random() * 256);
  return `${octet()}.${octet()}.${octet()}.${octet()}`;
}

function generateMultipleRandomIps(count) {
  const ipAddresses = [];
  for (let i = 0; i < count; i++) {
    ipAddresses.push(generateRandomIp());
  }
  return ipAddresses;
}

// Example: Generate and print 5 random IP addresses
const numberOfIps = 5;
const randomIps = generateMultipleRandomIps(numberOfIps);
console.log('Random IP Addresses:', randomIps);
```

## 174. 数字时钟

使用这个很棒的程序部署一个数字时钟。

```javascript
function updateClock() {
  const now = new Date();
  const hours = now.getHours();
  const minutes = now.getMinutes();
  const seconds = now.getSeconds();

  const formattedTime = `${hours}:${minutes}:${seconds}`;

  console.clear(); // Clears the console to update the time

  console.log("Current Time: " + formattedTime);
}

// Update the clock every second
setInterval(updateClock, 1000);
```

## 175. 随机数生成器

此程序生成一个 1 到 10 之间的随机数，并在控制台中显示。

```javascript
function generateRandomNumber(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

const randomNumber = generateRandomNumber(1, 10);
console.log("Random Number:", randomNumber);
```

## 176. 简单的 JavaScript 测验

此程序呈现一个包含多选题的简单 `JavaScript` 测验。它向用户询问答案并在控制台中提供反馈。

```javascript
function runQuiz() {
  const questions = [
    {
      question: "What is the capital of France?",
      options: ["Berlin", "Madrid", "Paris", "Rome"],
      correctAnswer: "Paris"
    },
    {
      question: "Which programming language is this quiz written in?",
      options: ["JavaScript", "Python", "Java", "C++"],
      correctAnswer: "JavaScript"
    },
    {
      question: "What is the largest mammal?",
      options: ["Elephant", "Whale Shark", "Blue Whale", "Giraffe"],
      correctAnswer: "Blue Whale"
    }
  ];

  let score = 0;

  for (const question of questions) {
    console.log(question.question);
    for (let i = 0; i < question.options.length; i++) {
      console.log(`${i + 1}. ${question.options[i]}`);
    }

    const userAnswerIndex = prompt("Enter the number of your answer:");
    const userAnswer = question.options[userAnswerIndex - 1];

    if (userAnswer === question.correctAnswer) {
      console.log("Correct!\n");
      score++;
    } else {
      console.log(`Wrong! The correct answer is ${question.correctAnswer}\n`);
    }
  }

  console.log(`Your final score: ${score} out of ${questions.length}`);
}

// Run the quiz
runQuiz();
```

## 177. 基于文本的 RPG 冒险

此程序带领用户进行一个简单的基于文本的 RPG 冒险，用户通过做出选择来导航故事。

```javascript
function textRPGAdventure() {
  console.log("Welcome to the Text-based RPG Adventure!");
  console.log("You find yourself in a dark cave. What do you want to do?");

  const choices = [
    { option: "Explore the cave", outcome: "You discover a hidden treasure!", next: "treasure" },
    { option: "Go deeper into the cave", outcome: "Uh-oh! A dragon appears! You narrowly escape.", next: "dragon" },
    { option: "Exit the cave", outcome: "You emerge into the sunlight. Adventure awaits!", next: "end" }
  ];

  let currentChoice = 0;

  while (currentChoice) {
    // logic omitted for brevity
  }
}
```

```javascript
function hangmanGame() {
  const words = ["javascript", "hangman", "programming", "developer", "challenge"];
  const selectedWord = words[Math.floor(Math.random() * words.length)];
  let guessedWord = "_".repeat(selectedWord.length);
  let remainingAttempts = 6;
  const guessedLetters = [];

  console.log("Welcome to the Hangman Game!");
  console.log("Try to guess the word.");

  while (remainingAttempts > 0) {
    console.log(`Word: ${guessedWord}`);
    console.log(`Guessed Letters: ${guessedLetters.join(", ")}`);
    console.log(`Attempts Remaining: ${remainingAttempts}`);

    const userGuess = prompt("Enter a letter:").toLowerCase();

    if (!userGuess || !userGuess.match(/[a-z]/) || userGuess.length !== 1) {
      console.log("Invalid input. Please enter a single letter.");
      continue;
    }

    if (guessedLetters.includes(userGuess)) {
      console.log("You already guessed that letter. Try again.");
      continue;
    }

    guessedLetters.push(userGuess);

    if (selectedWord.includes(userGuess)) {
      for (let i = 0; i < selectedWord.length; i++) {
        if (selectedWord[i] === userGuess) {
          guessedWord = guessedWord.substring(0, i) + userGuess + guessedWord.substring(i + 1);
        }
      }

      if (!guessedWord.includes("_")) {
        console.log(`Congratulations! You guessed the word: ${selectedWord}`);
        break;
      }
    } else {
      console.log("Incorrect guess. Try again.");
      remainingAttempts--;

      if (remainingAttempts === 0) {
        console.log(`Out of attempts. The word was: ${selectedWord}`);
      }
    }
  }
}

// 开始猜词游戏
hangmanGame();
```

## 186. 倒计时器

此程序允许用户设置以秒为单位的倒计时时间。计时器倒计时，程序显示剩余时间。

```javascript
function countdownTimer() {
  const userTime = prompt("Enter the countdown time in seconds:");
  const countdownTime = parseInt(userTime, 10);

  if (isNaN(countdownTime) || countdownTime <= 0) {
    console.log("Invalid input. Please enter a positive number.");
    return;
  }

  console.log(`Countdown started for ${countdownTime} seconds.`);

  let secondsRemaining = countdownTime;

  const intervalId = setInterval(() => {
    console.clear();
    console.log(`Time Remaining: ${secondsRemaining} seconds`);

    if (secondsRemaining === 0) {
      console.log("Countdown completed!");
      clearInterval(intervalId);
    } else {
      secondsRemaining--;
    }
  }, 1000);
}

// 启动倒计时器
countdownTimer();
```

## 187. 填词游戏

此程序提示用户输入各种类型的单词（例如名词、动词），并使用这些输入构建一个幽默的故事。

```javascript
function madLibsGame() {
  console.log("Welcome to the Mad Libs Game!");
  console.log("Let's create a funny story.");

  const noun = prompt("Enter a noun:");
  const verb = prompt("Enter a verb:");
  const adjective = prompt("Enter an adjective:");
  const adverb = prompt("Enter an adverb:");
  const animal = prompt("Enter an animal:");
  const sound = prompt("Enter a sound:");

  console.clear();
  console.log("Here's your Mad Libs story:");

  console.log(`Once upon a time, there was a ${adjective} ${noun} that loved to ${verb} ${adverb}.`);
  console.log(`One day, it met a ${animal} that made a ${sound} noise.`);
  console.log("Everyone in the neighborhood heard the noise and started to join the fun!");
  console.log("And they all lived happily ever after.");

  console.log("The end.");
}

// 开始填词游戏
madLibsGame();
```

## 188. 猜数字游戏

此程序生成一个随机数字，玩家必须在一定次数的尝试内猜出它。游戏会提供猜测是太高、太低还是正确的反馈。

```javascript
function guessTheNumberGame() {
  const maxNumber = 100;
  const maxAttempts = 10;
  const secretNumber = Math.floor(Math.random() * maxNumber) + 1;

  console.log("Welcome to the Guess the Number Game!");
  console.log(`I've picked a number between 1 and ${maxNumber}. Try to guess it!`);

  for (let attempts = 1; attempts <= maxAttempts; attempts++) {
    const userGuess = parseInt(prompt("Enter your guess:"), 10);

    if (isNaN(userGuess) || userGuess < 1 || userGuess > maxNumber) {
      console.log(`Invalid guess. Please enter a number between 1 and ${maxNumber}.`);
      attempts--;
      continue;
    }

    if (userGuess === secretNumber) {
      console.log(`Congratulations! You guessed the number in ${attempts} attempts.`);
      return;
    } else if (userGuess < secretNumber) {
      console.log("Too low! Try again.");
    } else {
      console.log("Too high! Try again.");
    }
  }

  console.log("Game over. The number was ${secretNumber}.");
}
```

## 189. 打鼠游戏

此程序模拟了一个文本的打鼠游戏。玩家必须在洞中击中出现的鼠。

```javascript
function whackAMole() {
  const holes = 5;
  let score = 0;
  let remainingAttempts = 10;

  console.log("Welcome to the Whack-a-Mole game!");

  while (remainingAttempts > 0) {
    const molePosition = Math.floor(Math.random() * holes);
    console.log(`A mole appeared in hole ${molePosition}!`);

    const guess = parseInt(prompt(`Enter hole number (0-${holes-1}):`), 10);

    if (guess === molePosition) {
      console.log("You hit it!");
      score++;
    } else {
      console.log("You missed the mole!");
    }

    remainingAttempts--;
    console.log(`Attempts left: ${remainingAttempts}`);
  }

  console.log(`Game over! Your final score is ${score}.
}

// 开始打鼠游戏
whackAMole();
```

## 190. 猜硬币游戏

此程序模拟一个猜硬币游戏。玩家猜测下一次抛币的结果是正面还是反面。

```javascript
function coinTossingGame() {
  const coinSides = ["Heads", "Tails"];
  let correctGuesses = 0;
  let totalGuesses = 0;

  console.log("Welcome to the Coin Tossing Game!");

  while (true) {
    const playerGuess = prompt("Heads or Tails?").toLowerCase();

    if (!["heads", "tails"].includes(playerGuess)) {
      console.log("Invalid input. Please enter 'Heads' or 'Tails'.");
      continue;
    }

    const coinResult = coinSides[Math.floor(Math.random() * 2)];

    console.log(`Coin toss result: ${coinResult}`);

    if (playerGuess === coinResult.toLowerCase()) {
      console.log("Correct guess! Well done!");
      correctGuesses++;
    } else {
      console.log("Wrong guess. Better luck next time!");
    }

    totalGuesses++;

    const playAgain = confirm("Do you want to toss the coin again?");
    if (!playAgain) {
      console.log(`Game over. You made ${correctGuesses} correct guesses out of ${totalGuesses} total guesses.`);
      break;
    }
  }
}

// 开始猜硬币游戏
coinTossingGame();
```

## 191. 斐波契数生成器

此程序生成并显示不超过上限的斐波那契数。

```javascript
function fibonacciNumberGenerator() {
  const limit = parseInt(prompt("Enter the limit for Fibonacci numbers:"), 10);

  if (isNaN(limit) || limit < 1) {
    console.log("Invalid input. Please enter a positive number.");
    return;
  }

  let fibonacciNumbers = [0, 1];

  for (let i = 2; i <= limit; i++) {
    fibonacciNumbers[i] = fibonacciNumbers[i - 1] + fibonacciNumbers[i - 2];
  }

  console.log(`Fibonacci numbers up to ${limit}:`);
  console.log(fibonacciNumbers.slice(0, limit + 1));
}

// 开始斐波那契数生成器
fibonacciNumberGenerator();
```

## 192. 数学测验游戏

此程序模拟一个基于文本的数学测验游戏。玩家被问到随机的加法问题，答对得分。

```javascript
function mathQuizGame() {
  const maxQuestions = 5;
  let score = 0;

  console.log("Welcome to the Math Quiz Game!");
  console.log("Answer the following addition questions:");

  for (let i = 0; i < maxQuestions; i++) {
    const num1 = Math.floor(Math.random() * 10) + 1;
    const num2 = Math.floor(Math.random() * 10) + 1;
    const correctAnswer = num1 + num2;

    const userAnswer = parseInt(prompt(`Question ${i + 1}: ${num1} + ${num2} = ?`), 10);

    if (!isNaN(userAnswer) && userAnswer === correctAnswer) {
      console.log("Correct! Well done!");
      score++;
    } else {
      console.log(`Wrong! The correct answer is: ${correctAnswer}`);
    }
  }

  console.log(`Quiz complete! Your final score is: ${score} out of ${maxQuestions}`);
}

// Start the Math Quiz Game
mathQuizGame();
```

## 193. 颜色猜测游戏

本程序模拟一个基于文本的颜色猜测游戏。玩家获得RGB值，需要猜出正确的颜色。

```javascript
function colorGuessingGame() {
  const colors = ["red", "green", "blue", "yellow", "orange", "purple"];
  const maxAttempts = 3;

  console.log("Welcome to the Color Guessing Game!");
  console.log("Guess the color based on the RGB values.");

  for (let attempts = 1; attempts <= maxAttempts; attempts++) {
    const randomColor = colors[Math.floor(Math.random() * colors.length)];
    const rgbValues = generateRandomRGBValues();

    console.log(`RGB: ${rgbValues.join(", ")}`);

    const userGuess = prompt("Enter your color guess:").toLowerCase();

    if (!colors.includes(userGuess)) {
      console.log("Invalid guess. Please enter a valid color.");
      attempts--;
      continue;
    }

    if (userGuess === randomColor) {
      console.log("Congratulations! You guessed the correct color!");
      return;
    } else {
      console.log(`Wrong guess. Remaining attempts: ${maxAttempts - attempts}`);
    }
  }

  console.log("Sorry, you've run out of attempts. The correct color was revealed above.");
}

function generateRandomRGBValues() {
  return Array.from({ length: 3 }, () => Math.floor(Math.random() * 256));
}

// Start the Color Guessing Game
colorGuessingGame();
```

## 194. 单词拼乱游戏

本程序模拟一个基于文本的单词拼乱游戏。玩家看到一个被打乱的单词，需要将其还原。

```javascript
function wordScrambleGame() {
  const words = ["javascript", "programming", "web", "hangman", "developer"];
  const maxAttempts = 3;

  console.log("Welcome to the Word Scramble Game!");
  console.log("Unscramble the word and enter your guess.");

  for (let attempts = 1; attempts <= maxAttempts; attempts++) {
    const randomWord = words[Math.floor(Math.random() * words.length)];
    const scrambledWord = scrambleWord(randomWord);

    console.log(`Scrambled word: ${scrambledWord}`);

    const userGuess = prompt("Enter your unscrambled word guess:").toLowerCase();

    if (!words.includes(userGuess)) {
      console.log("Invalid guess. Please enter a valid word.");
      attempts--;
      continue;
    }

    if (userGuess === randomWord) {
      console.log("Congratulations! You unscrambled the word!");
      return;
    } else {
      console.log(`Wrong guess. Remaining attempts: ${maxAttempts - attempts}`);
    }
  }

  console.log("Sorry, you've run out of attempts. The correct word was revealed above.");
}

function scrambleWord(word) {
  return word.split("").sort(() => Math.random() - 0.5).join("");
}

// Start the Word Scramble Game
wordScrambleGame();
```

## 195. 国家首都测验游戏

本程序模拟一个基于文本的国家首都测验游戏。玩家需要将国家与其对应的首都进行匹配。

```javascript
function countryCapitalQuizGame() {
  const countryCapitalPairs = [
    { country: "France", capital: "Paris" },
    { country: "Japan", capital: "Tokyo" },
    { country: "Brazil", capital: "Brasília" },
    { country: "India", capital: "New Delhi" },
    { country: "Australia", capital: "Canberra" }
  ];

  let score = 0;

  console.log("Welcome to the Country Capital Quiz Game!");
  console.log("Match the country with its capital:");

  for (const { country, capital } of countryCapitalPairs) {
    console.log(`\nCountry: ${country}`);

    const userCapital = prompt(`Enter the capital of ${country}: `).trim();

    if (userCapital.toLowerCase() === capital.toLowerCase()) {
      console.log("Correct! Well done!");
      score++;
    } else {
      console.log(`Wrong! The correct capital is: ${capital}`);
    }
  }

  console.log(`Quiz complete! Your final score is: ${score} out of ${countryCapitalPairs.length}`);
}

// Start the Country Capital Game
countryCapitalQuizGame();
```

## 196. 猜动物

本程序模拟一个基于文本的猜动物游戏。玩家获得线索并猜出动物。

```javascript
function guessAnimalGame() {
  const animals = [
    { name: "elephant", clues: "I have a trunk." },
    { name: "giraffe", clues: "I have a long neck." },
    { name: "penguin", clues: "I live in cold climates." },
    { name: "monkey", clues: "I love climbing trees." }
  ];

  const target = animals[Math.floor(Math.random() * animals.length)];
  let attempts = 3;

  console.log("Welcome to the Animal Guess Game!");
  console.log(`Clue: ${target.clues}`);

  for (let i = 0; i < attempts; i++) {
    const guess = prompt("What animal am I?").toLowerCase();

    if (guess === target.name) {
      console.log(`Correct! It's a ${target.name}!`);
      return;
    } else {
      console.log(`Wrong! Remaining attempts: ${attempts - i - 1}`);
    }
  }

  console.log(`Sorry! The animal was a ${target.name}.`);
}

// Start the Animal Guess Game
guessAnimalGame();
```

<channel|>```javascript
function fizzBuzzGame() {
  console.log("Welcome to the FizzBuzz Game!");
  console.log("Let's play FizzBuzz!");

  for (let i = 1; i <= 100; i++) {
    let output = "";

    if (i % 3 === 0) {
      output += "Fizz";
    }

    if (i % 5 === 0) {
      output += "Buzz";
    }

    console.log(output || i);
  }
}

// Start the FizzBuzz Game
fizzBuzzGame();
```

## 200. 交换相邻数位对

本程序接受一个偶数长度的整数，并交换其相邻的数位对。例如，对于数字123456，程序将交换相邻的数位对，生成数字214365。

```javascript
function swapPairsOfAdjacentDigits(number) {
  // Convert the number to a string to manipulate individual digits
  const numberStr = String(number);
  const length = numberStr.length;

  // Check if the number has an even length
  if (length % 2 !== 0) {
    console.log("Please enter an integer with an even length.");
    return;
  }

  // Swap pairs of adjacent digits
  let swappedNumber = "";
  for (let i = 0; i < length; i += 2) {
    swappedNumber += numberStr[i + 1] + numberStr[i];
  }

  // Convert the result back to an integer
  const result = parseInt(swappedNumber, 10);
  console.log(`Original Number: ${number}`);
  console.log(`Number with Swapped Pairs of Adjacent Digits: ${result}`);
}

// Example: Swap pairs of adjacent digits of the number 123456
swapPairsOfAdjacentDigits(123456);
```

## 201. 大小写转换器

本程序接受一个字符串作为输入，并更改所有字母的大小写。大写字母转换为小写，小写字母转换为大写。

```javascript
function changeCapitalization(inputString) {
  let resultString = "";

  for (const char of inputString) {
    // Check if the character is uppercase
    if (char === char.toUpperCase()) {
      // Convert uppercase to lowercase
      resultString += char.toLowerCase();
    } else {
      // Convert lowercase to uppercase
      resultString += char.toUpperCase();
    }
  }

  console.log(`Original String: ${inputString}`);
  console.log(`String with Changed Capitalization: ${resultString}`);
}

// Example: Change the capitalization of the string "Hello World"
changeCapitalization("Hello World");
```

## 202. 数组半区交换器

本程序接受一个偶数长度的整数数组，并交换其两半部分。

```javascript
function swapArrayHalves(arr) {
  const length = arr.length;

  // Check if the array has an even length
  if (length % 2 !== 0) {
    console.log("Please provide an array with an even length.");
    return;
  }

  // Calculate the midpoint of the array
  const midpoint = length / 2;

  // Swap the two halves of the array
  for (let i = 0; i < midpoint; i++) {
    const temp = arr[i];
    arr[i] = arr[midpoint + i];
    arr[midpoint + i] = temp;
  }

  console.log("Original Array: " + arr.join(", "));
  console.log("Array with Swapped Halves: " + arr.join(", "));
}

// Example: Swap halves of the array [1, 2, 3, 4, 5, 6]
swapArrayHalves([1, 2, 3, 4, 5, 6]);
```

## 203. 字符串中的数字之和

本程序计算给定字符串中出现的所有数字的总和。它识别字符串中的数字并将它们相加以计算总和。

```javascript
function sumOfDigitsInString(inputString) {
  let digitSum = 0;

  for (const char of inputString) {
    // Check if the character is a digit
    if (/\d/.test(char)) {
      // Convert the digit character to its numerical value and add to sum
      digitSum += parseInt(char, 10);
    }
  }

  console.log(`Original String: ${inputString}`);
  console.log(`Sum of Digits in the String: ${digitSum}`);
}

// Example: Compute the sum of digits in the string "abc123xyz456"
sumOfDigitsInString("abc123xyz456");
```

## 204. 立方和

本程序计算从1到给定整数的所有整数的立方和。它计算指定范围内每个整数的立方并将它们相加以求得总和。

```javascript
function sumOfCubes(upToInteger) {
  let cubesSum = 0;

  for (let i = 1; i <= upToInteger; i++) {
    // Calculate the cube of each integer and add to sum
    cubesSum += Math.pow(i, 3);
  }

  console.log(`Sum of Cubes from 1 to ${upToInteger}: ${cubesSum}`);
}

// Example: Compute the sum of cubes up to the integer 5
sumOfCubes(5);
```

## 205. 求和的最大整数

本程序找到最大的`n`，使得从1到`n`（包含）的整数之和不超过给定的`targetSum`。它使用公式 `Sum = n * (n + 1) / 2` 来计算。

```javascript
function findMaxIntegerForSum(targetSum) {
  let currentSum = 0;
  let maxInteger = 0;

  while (currentSum + maxInteger <= targetSum) {
    maxInteger++;
    currentSum += maxInteger;
  }

  console.log(`Maximum Integer (n) for Sum <= ${targetSum}: ${maxInteger}`);
}

// Example: Find the maximum integer for sum <= 15
findMaxIntegerForSum(15);
```

## 206. URL 解析

本程序将一个URL分解为其各个部分，并将它们放入数组中。考虑的URL结构是 `scheme://domain/path`，其中`path` 是可选的。

```javascript
function breakURL(url) {
  const urlParts = {};
  const urlRegex = /^(\w+):\/\/([\w.-]+)(\/.*)?$/;
  const matches = url.match(urlRegex);

  if (!matches) {
    console.log("Invalid URL.");
    return;
  }

  urlParts.scheme = matches[1];
  urlParts.domain = matches[2];
  urlParts.path = matches[3] || "";

  console.log("URL Parts:");
  console.log(urlParts);
}

// Example: Breakdown the URL "https://www.example.org/page"
breakURL("https://www.example.org/page");
```

## 207. 按长度排序

此程序按长度递增对给定数组中的字符串进行排序。使用 `Array.sort` 方法来实现顺序。

```javascript
function sortStringsByLength(stringsArray) {
  const sortedArray = stringsArray.slice().sort((a, b) => a.length - b.length);

  console.log("Original Array of Strings:");
  console.log(stringsArray);
  console.log("Array Strings Sorted by Length:");
  console.log(sortedArray);
}

// Example: Sort strings by length
sortStringsByLength(["apple", "banana", "orange", "kiwi", "grape"]);
```

## 208. 简化绝对路径

此程序简化给定的Unix风格绝对路径。它接受一个表示绝对路径的字符串，并通过解析多余的斜杠 `/`、父目录引用 `..` 和当前目录引用 `.` 来简化它。

```javascript
function simplifyAbsolutePath(path) {
  const parts = path.split('/');
  const simplifiedParts = [];

  for (const part of parts) {
    if (part === '..') {
      simplifiedParts.pop(); // Move up one level for '..'
    } else if (part !== '' && part !== '.') {
      simplifiedParts.push(part);
    }
  }

  const simplifiedPath = '/' + simplifiedParts.join('/');

  console.log(`Original Absolute Path: ${path}`);
  console.log(`Simplified Absolute Path: ${simplifiedPath}`);
}

// Example: Simplify an absolute path
simplifyAbsolutePath('/home/user/../documents/./file.txt');
```

## 209. 统计数组中的公共元素

此程序找出两个数组之间公共元素的数量。它比较两个数组中的元素，并统计公共元素的出现次数。

```javascript
function countCommonElements(arr1, arr2) {
  const commonElements = arr1.filter(element => arr2.includes(element));
  const numberOfCommonElements = commonElements.length;

  console.log("Array 1:", arr1);
  console.log("Array 2:", arr2);
  console.log("Common Elements:", commonElements);
  console.log("Number of Common Elements:", numberOfCommonElements);
}

// Example: Count common elements between two arrays
countCommonElements([1, 2, 3, 4, 5], [3, 4, 5, 6, 7]);
```

## 210. 检查数字中的所有数字是否相同

此程序检查给定数字中的所有数字是否相同。它将数字转换为字符串，并将每个数字与第一个数字进行比较。

```javascript
function areAllDigitsSame(number) {
  const numberStr = String(number);
  const firstDigit = numberStr[0];

  for (let i = 1; i < numberStr.length; i++) {
    if (numberStr[i] !== firstDigit) {
      console.log(`Digits in ${number} are not all the same.`);
      return;
    }
  }

  console.log(`Digits in ${number} are all the same.`);
}

// Example: Check if all digits in the number 22222 are the same
areAllDigitsSame(22222);
```

## 211. 最右侧整十数的位置

此程序在整数数组中查找最右侧整十数的位置。整十数非正式地定义为以一个或多个零结尾的整数。程序从右到左遍历数组，并识别最右侧的整十数（如果存在）。

```javascript
function rightmostRoundNumberPosition(arr) {
  for (let i = arr.length - 1; i >= 0; i--) {
    if (arr[i] % 10 === 0) {
      console.log(`Rightmost Round Number: ${arr[i]}, Position: ${i + 1}`);
      return;
    }
  }
  console.log("No round numbers found in the array. Position: 0");
}

// Example: Find the position of the rightmost round number
rightmostRoundNumberPosition([123, 450, 678, 900]);
```

## 212. 反转16位无符号短整数的位

此程序反转给定的16位无符号短整数的位。它将整数转换为其二进制表示，反转位，然后将其转换回整数。

```content
```javascript
function reverseBits16BitUnsignedShort(integer) {
  const binaryRepresentation = integer.toString(2).padStart(16, '0');
  const reversedBinary = binaryRepresentation.split('').reverse().join('');
  const reversedInteger = parseInt(reversedBinary, 2);

  console.log(`Original Integer: ${integer}`);
  console.log(`Binary Representation: ${binaryRepresentation}`);
  console.log(`Reversed Binary: ${reversedBinary}`);
  console.log(`Reversed Integer: ${reversedInteger}`);
}

// Example: Reverse bits of the 16-bit unsigned short integer 5678
reverseBits16BitUnsignedShort(5678);
```

## 213. 大于15检查器

此程序测试给定的整数是否大于15。如果整数大于15，则返回给定的数字；否则，返回15。

```javascript
function greaterThan15Checker(number) {
  const result = number > 15 ? number : 15;
  console.log(`Given Number: ${number}`);
  console.log(`Result: ${result}`);
}

// Example: Test whether the number 20 is greater than 15
greaterThan15Checker(20);
```

## 214. 将第一个数字替换为$

此程序将字符串中的第一个数字（假设字符串至少有一个数字）替换为 $ 字符。

```javascript
function replaceFirstDigitWithDollar(inputString) {
  const modifiedString = inputString.replace(/\d/, '$');

  console.log(`Original String: ${inputString}`);
  console.log(`Modified String: ${modifiedString}`);
}

// Example: Replace the first digit with $ in the string "abc123xyz456"
replaceFirstDigitWithDollar("abc123xyz456");
```

## 215. 前缀和

此程序为给定数组创建一个前缀和数组。序列的前缀和是一个新序列，其中每个元素是原始序列中所有前面元素的总和。

```javascript
function prefixSums(inputArray) {
  let prefixSum = 0;
  const prefixSumArray = [];

  for (const num of inputArray) {
    prefixSum += num;
    prefixSumArray.push(prefixSum);
  }

  console.log("Original Array:", inputArray);
  console.log("Prefix Sums Array:", prefixSumArray);
}

// Example: Create prefix sums for the array [1, 2, 3, 4, 5]
prefixSums([1, 2, 3, 4, 5]);
```

## 216. 下一个质数

此程序查找严格大于给定数字的最小质数。它从给定数字开始逐个检查数字，直到找到下一个质数。

```javascript
function isPrime(num) {
  if (num < 2) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
}

function nextPrimeNumber(givenNumber) {
  let nextNumber = givenNumber + 1;

  while (!isPrime(nextNumber)) {
    nextNumber++;
  }

  console.log(`Given Number: ${givenNumber}`);
  console.log(`Next Prime Number: ${nextNumber}`);
}

// Example: Find the next prime number greater than 10
nextPrimeNumber(10);
```

## 217. 反转位的顺序

此程序反转整数中位的顺序。它将整数转换为其二进制表示，反转位，然后将其转换回整数。

```javascript
function reverseOrderOfBits(integer) {
  const binaryRepresentation = integer.toString(2).padStart(8, '0'); // Assuming 8 bits for simplicity
  const reversedBinary = binaryRepresentation.split('').reverse().join('');
  const reversedInteger = parseInt(reversedBinary, 2);

  console.log(`Original Integer: ${integer}`);
  console.log(`Binary Representation: ${binaryRepresentation}`);
  console.log(`Reversed Binary: ${reversedBinary}`);
  console.log(`Reversed Integer: ${reversedInteger}`);
}

// Examples: Reverse order of bits for given integers
reverseOrderOfBits(14);
reverseOrderOfBits(56);
reverseOrderOfBits(234);
```

## 218. 金字塔

此程序使用 ASCII 字符生成三角形图案，并在控制台中显示它。

```javascript
function generateAsciiTriangle(height) {
  for (let i = 1; i <= height; i++) {
    const spaces = ' '.repeat(height - i);
    const stars = '*'.repeat(i * 2 - 1);
    console.log(spaces + stars);
  }
}

const triangleHeight = 5;
generateAsciiTriangle(triangleHeight);
```

在每一行代码中，他们都编织了一个创新与创造的故事。这本书一直是你在广阔 JavaScript 世界中的指南针。合上这一章，请记住，克服的每一个挑战都是一项成就，每一个解决方案都是迈向精通的一步。你的代码是赋予项目生命的旋律。愿他们继续充满激情地创造和编程！感谢你让我成为你旅程的一部分。

致以诚挚的谢意，

Hernando Abella

500+ JavaScript Programs

在以下网址发现其他有用资源：

`www.hernandoabella.com`
```