
# 考试与面试Javascript练习：初学者代码示例

![](`img/9e93faabf29d7f96ad3dab9b04710783_0_0.png`)

## 初学者编码示例

JAKE BOND

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>将给定字符串的每个单词首字母大写的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

```javascript
function capital_letter(str) {
  str = str.split(" ");
  for (var i = 0, x = str.length; i < x; i++) {
    str[i] = str[i][0].toUpperCase() + str[i].substr(1);
  }
  return str.join(" ");
}

console.log(capital_letter("Write a JavaScript program to capitalize the first letter of each word of a given string."));
```

Write A JavaScript Program To Capitalize The First Letter Of Each Word Of A Given String.

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>将给定数字转换为小时和分钟的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

```javascript
function time_convert(num) {
  var hours = Math.floor(num / 60);
  var minutes = num % 60;
  return hours + ":" + minutes;
}

console.log(time_convert(71));
console.log(time_convert(450));
console.log(time_convert(1441));
```

1:11

7:30

24:1

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>统计给定字符串中元音数量的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

```javascript
function vowel_Count(str) {
    return str.replace(/[^aeiou]/gi, "").length;
}

console.log(vowel_Count("Python"));
console.log(vowel_Count("htmlresource.com"));
```

1

5

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>创建一个不包含第一个和最后一个字符的字符串的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

```javascript
function without_first_last(str) {
    return str.substring(1, str.length - 1);
}

console.log(without_first_last("JavaScript"));
console.log(without_first_last("abc"));
console.log(without_first_last("abcde"));
```

### 输出

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>拼接除第一个字符外的两个字符串的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

```javascript
function concatenate(str1, str2) {
  str1 = str1.substring(1, str1.length);
  str2 = str2.substring(1, str2.length);
  return str1 + str2;
}

console.log(concatenate("ABC", "DEF"));
console.log(concatenate("HELLO", "WORLD"));
```

BCDEF

elloorld

预期输出：'e'

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>找到第一个重复的字符</title>
</head>
<body>
</body>
</html>
```

```javascript
function findFirstRepeatedChar(str) {
  var arr1 = str.split("");
  var result = "";
  for (var x = 0; x < arr1.length; x++) {
    var ctr = 0;
    for (var y = 0; y < arr1.length; y++) {
      if (arr1[x] === arr1[y]) {
        ctr++;
      }
    }
    if (ctr < 2) {
      result = arr1[x];
      break;
    }
  }
}
console.log(findFirstRepeatedChar("abac"));
```

示例字符串："Web Development"

预期输出：'Development'

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>找到字符串中的长单词</title>
</head>
<body>
</body>
</html>
```

```javascript
function longest_word(str) {
  var arr1 = str.split(/\s/);
  var result = "";
  for (var x = 0; x < arr1.length; x++) {
    if (arr1[x].length > result.length) {
      result = arr1[x];
    }
  }
  return result;
}
console.log(longest_word("Web Development"));
```

Development

示例字符串：'quick fox'

预期输出：4

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>统计字符串中元音数量的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function vowel_count(str) {
  var v_list = "aeiouIOU";
  var vcount = 0;

  for (var x = 0; x < str.length; x++) {
    if (v_list.indexOf(str[x]) !== -1) {
      vcount++;
    }
  }
  return vcount;
}
console.log(vowel_count("quick fox"));
```

4

质数是一个只有1和自身两个因数的正整数

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>检查一个数字是否为质数的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function is_prime(n) {
  if (n <= 1) {
    return false;
  } else if (n === 2) {
    return true;
  } else {
    for (var x = 2; x < n; x++) {
      if (n % x === 0) {
        return false;
      }
    }
    return true;
  }
}
console.log(is_prime(37));
```

true

### 获取数据类型

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>获取数据类型的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function get_data_type(value) {
  var dtypes = [Function, RegExp, Number, String, Boolean], x, len;

  if (typeof value === "object" || typeof value === "function") {
    for (x = 0, len = dtypes.length; x < len; x++) {
      if (value instanceof dtypes[x]) {
        return dtypes[x];
      }
    }
  }
  return typeof value;
}
console.log(get_data_type(12));
console.log(get_data_type("w3resource"));
console.log(get_data_type(false));
```

number

string

Boolean

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>找到数组中第二小和第二大的数</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function find_second_lowest_second_largest(arr_num) {
  arr_num.sort(function(x,y) {
    return x-y;
  });
  var uniqua = [arr_num[0]];
  var result = [];

  for (var j=1; j < arr_num.length; j++) {
    if (arr_num[j-1] !== arr_num[j]) {
      uniqua.push(arr_num[j]);
    }
  }
  result.push(uniqua[1], uniqua[uniqua.length-2]);
  return result.join(',');
}

console.log(find_second_lowest_second_largest([1,2,3,4]));
```

2,3

### 求一个长度为二的正整数的两个数字

### HTML 代码

```html
<!DOCTYPE html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>计算一个长度为二的正整数两个数字之和的 JavaScript 程序</title>
</head>
<body>
</body>
```

### JAVASCRIPT 代码

```javascript
function add_two_digits(n)
{
  return n % 10 + Math.floor(n / 10);
}
console.log(add_two_digits(25))
console.log(add_two_digits(50))
```

### 输出

7

5

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8 />
<title>查找闰年</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function leapyear(year)
{
return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);
}
console.log(leapyear(2016));
console.log(leapyear(2000));
console.log(leapyear(1700));
console.log(leapyear(1800));
console.log(leapyear(100));
```

true

true

false

false

false

### 检查给定的正整数是否为 3 的倍数或 7 的倍数

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>检查给定正整数是否为 3 的倍数或 7 的倍数的 JavaScript 程序</title>
</head>
<body>

</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function test37(x)
{
  if (x % 3 == 0 || x % 7 == 0)
  {
    return true;
  }
  else {
    return false;
  }
}

console.log(test37(12));
console.log(test37(14));
console.log(test37(10));
console.log(test37(11));
```

true

true

false

false

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>检查字符串是否以 'Java' 开头，否则返回 false 的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function start_spec_str(str)
{
  if (str.length < 4)
  {
    return false;
  }
  var front = str.substring(0, 4);
  if (front == 'Java')
  {
    return true;
  } else
  {
    return false;
  }
}

console.log(start_spec_str("JavaScript"));
console.log(start_spec_str("Java"));
console.log(start_spec_str("Python"));
```

true

true

### 两个给定的整数 - 检查是否在 50..99 范围内

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>检查两个给定的整数是否在 50..99 范围内（包含）的 JavaScript 程序。如果其中一个在范围内，则返回 true</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function check_numbers(x, y)
{
    if ((x >= 50 && x <= 99) || (y >= 50 && y <= 99))
    {
      return true;
    }
    else
    {
      return false;
    }
}
console.log(check_numbers(12, 101));
console.log(check_numbers(52, 80));
console.log(check_numbers(15, 99));
```

false

true

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>从不同的整数中找到距离 100 最近值的 JavaScript 程序</title>
</head>
<body>
</html>
```

### JAVASCRIPT 代码

```javascript
function near_100(x, y) {
    if (x !== y) {
        var x1 = Math.abs(x - 100);
        var y1 = Math.abs(y - 100);
        if (x1 < y1)
        {
            return x;
        }
        if (y1 < x1)
        {
            return y;
        }
        else
        {
            return 0;
        }
    }
}
console.log(near_100(90, 89));
console.log(near_100(90, -89));
console.log(near_100(90, 90));
```

90

89

false

### 正整数 - 检查是否为 3 的倍数或 7 的倍数

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>检查正整数是否为 3 的倍数或 7 的倍数的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function test37(x)
{
  if (x % 3 == 0 || x % 7 == 0) {
    return true;
  } else {
    return false;
  }
}
console.log(test37(12));
console.log(test37(14));
console.log(test37(10));
console.log(test37(11));
```

true

true

false

false

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>检查字符串是否以 'Java' 开头，否则返回 false 的 JavaScript 程序</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function start_spec_str(str)
{
  if (str.length < 4)
  {
    return false;
  }
  var front = str.substring(0, 4);
  if (front == 'Java')
  {
    return true;
  }
  else
  {
    return false;
  }
}
console.log(start_spec_str("JavaScript"));
console.log(start_spec_str("Java"));
console.log(start_spec_str("Python"));
```

true

true

false

### 两个数的乘法和除法

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8 />
<title>计算两个数乘法和除法的 JavaScript 程序</title>
<style type="text/css">
body {margin: 30px;}
</style>
</head>
<body>
<form>
第一个数字: <input type="text" id="firstNumber" /><br>
第二个数字: <input type="text" id="secondNumber" /><br>
<input type="button" onClick="multiplyBy()" Value="乘法" />
<input type="button" onclick="divideBy()" Value="除法" />
</form>
<p>结果是 : <br>
<span id="result</span>
</p>
</body>
</html>
```

```javascript
function multiplyBy()
{
    var num1 = document.getElementById("firstNumber").value;
    var num2 = document.getElementById("secondNumber").value;
    document.getElementById("result").innerHTML = num1 * num2;
}

function divideBy()
{
    var num1 = document.getElementById("firstNumber").value;
    var num2 = document.getElementById("secondNumber").value;
    document.getElementById("result").innerHTML = num1 / num2;
}
```

### 输出

![](`img/9e93faabf29d7f96addab9b04710783_46_0.png`)

### 使用 JavaScript 将温度在摄氏和华氏之间转换

### HTML 代码

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>编写一个 JavaScript 程序将温度在摄氏和华氏之间转换</title>
</head>
<body>
</body>
</html>
```

### JAVASCRIPT 代码

```javascript
function cToF(celsius)
{
  var cTemp = celsius;
  var cToFahr = cTemp * 9 / 5 + 32;
  var message = cTemp + "°C 是 " + cToFahr + "°F.";
  console.log(message);
}

function fToC(fahrenheit)
{
  var fTemp = fahrenheit;
  var fToCel = (fTemp - 32) * 5 / 9;
  var message = fTemp + "°F 是 " + fToCel + "°C.";
  console.log(message);
}
cToF(60);
fToC(45);
```

60°C 是 140 °F。
