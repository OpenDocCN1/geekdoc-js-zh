

# JavaScript 正则表达式使用指南

## 修饰符

### `i`

#### 描述

执行不区分大小写的匹配。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行不区分大小写的搜索 "Youtube"。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Visit youtube";
    var pattern = /Youtube/i;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

Youtube

### `g`

#### 描述

执行全局匹配（查找所有匹配项，而不是在第一个匹配后停止）。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索 "Welcome"。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books! Again welcome";
    var pattern = /Welcome/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

Welcome

### `m`

#### 描述

执行多行匹配。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串的每一行开头执行多行搜索 "Welcome"。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "\nWelcome to my books! \nWelcome again!";
    var pattern = /^Welcome/m;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

Welcome

## 方括号

### `[abc]`

#### 描述

查找方括号内的任意字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索字符 "o"。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /[o]/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

o,o,o,o

### `[^abc]`

#### 描述

查找不在方括号内的任意字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索不在方括号 [o] 内的字符。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /[^o]/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

W,e,l,c,m,e, ,t, ,m,y, ,b,k,s,!

### `[0-9]`

#### 描述

查找方括号内的任意数字。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索数字 1 到 4。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "1234567890";
    var pattern = /[3-5]/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

3,4,5

### `[^0-9]`

#### 描述

查找不在方括号内的任意数字。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索不是 1 到 4 的数字。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "1234567890";
    var pattern = /[^3-5]/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

1,2,6,7,8,9,0

### `(x|y)`

#### 描述

查找指定的任意一个选项。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索指定的任意一个选项 (2|0)。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "123456789024680";
    var pattern = /(2|0)/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

2,0,2,0

## 元字符

### `.`

#### 描述

查找单个字符，除了换行或行终止符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索 "W.l"。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books! Welcome again!";
    var pattern = /W.l/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

Wel,Wel

### `\w`

#### 描述

查找单词字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索单词字符。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!.";
    var pattern = /\w/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

W,e,l,c,o,m,e,t,o,m,y,b,o,o,k,s

### `\W`

#### 描述

查找非单词字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮在字符串中执行全局搜索非单词字符。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!.";
    var pattern = /\W/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

, , ,!,.

### `\d`

#### 描述

查找一个数字。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮对字符串中的数字进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books! 2nd 3rd 4th";
    var pattern = /\d/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

2,3,4

### `\D`

#### 描述

查找一个非数字字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo">点击按钮对字符串中的非数字字符进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<script>
function myFunction() {
    var str = "Welcome to my books! 2nd 3rd 4th";
    var pattern = /\D/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML=result;
}
</script>
</body>
</html>
```

#### 输出

W,e,l,c,o,m,e, ,t,o, ,m,y, ,b,o,o,k,s,!, ,n,d, ,r,d, ,t,h

### `\s`

#### 描述

查找一个空白字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮对字符串中的空白字符进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /\s/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

, ,

### `\S`

#### 描述

查找一个非空白字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮搜索字符串中的非空白字符。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /\S/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

W,e,l,c,o,m,e,t,o,m,y,b,o,o,k,s,!

### `\b`

#### 描述

查找单词开头或结尾处的匹配。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮对字符串中单词开头或结尾处的 "boo" 进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books! books.";
    var pattern = /\bboo/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

boo,boo

### `\B`

#### 描述

查找不在单词开头或结尾处的匹配。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo">点击按钮对字符串中不在单词开头或结尾处的 "ok" 进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /\Bok/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML=result;
}
</script>
</body>
</html>
```

#### 输出

ok

### `\0`

#### 描述

查找 NUL 字符。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮返回字符串中 NUL 字符的位置。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Hello JavaScript.\0It is awesome!";
    var pattern = /\0/;
    var result = str.search(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

#### 输出

17

### 换行符

#### 描述

查找换行符。

#### 示例代码




```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮返回字符串中换行符的位置。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "JavaScript.\nIt is awesome!";
    var pattern = /\n/;
    var result = str.search(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

11

## `\f`

### 描述

查找换页符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮返回字符串中换页符的位置。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "JavaScript.\fIt is awesome!";
    var pattern = /\f/;
    var result = str.search(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

11

## `\r`

### 描述

查找回车符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮返回字符串中回车符的位置。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "JavaScript.\rIt is awesome!";
    var pattern = /\r/;
    var result = str.search(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

11

## `\t`

### 描述

查找制表符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮返回字符串中制表符的位置。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "JavaScript.\tIt is awesome!";
    var pattern = /\t/;
    var result = str.search(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

11

## `\v`

### 描述

查找垂直制表符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮返回字符串中垂直制表符的位置。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "JavaScript.\vIt is awesome!";
    var pattern = /\v/;
    var result = str.search(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

11

## `\xxx`

### 描述

查找由八进制数 `xxx` 指定的字符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮对字符串中的八进制数 127 (W) 进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /\127/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

W

## `\xdd`

### 描述

查找由十六进制数 `dd` 指定的字符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮对字符串中的十六进制数 57 (W) 进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /\x57/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

W

## `\uxxxx`

### 描述

查找由十六进制数 `xxxx` 指定的 Unicode 字符。

### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>点击按钮对字符串中的十六进制数 0057 (W) 进行全局搜索。</p>
<button onclick="myFunction()">测试</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /\u0057/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

W

## 量词

### `n+`

#### 描述

匹配任何包含至少一个 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to do a global search for at least one "o" in a string.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /o+/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
o,o,oo
```

### `n*`

#### 描述

匹配任何包含零个或多个 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to do a global search for an "b", followed by zero or more "o" characters.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books! book";
    var pattern = /bo*/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
boo,boo
```

### `n?`

#### 描述

匹配任何包含零个或一个 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to do a global search for a "5", followed by zero or one "0" characters.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "51, 5000, 350, 35";
    var pattern = /50?/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
5,50,50,5
```

### `n{X}`

#### 描述

匹配任何包含连续 `X` 个 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to do a global search for a substring that contains a sequence of three digits.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "5,555,5555,555555";
    var pattern = /\d{3}/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
555,555,555,555
```

### `n{X,Y}`

#### 描述

匹配任何包含连续 `X` 到 `Y` 个 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to global search for a substring that contains a sequence of three to five digits.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "5,55,555,5555,55555,5555555";
    var pattern = /\d{3,5}/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
555,5555,55555,55555
```

### `n{X,}`

#### 描述

匹配任何包含至少 `X` 个连续 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to global search for a substring that contains a sequence of at least two digits.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "5,55,555,5555";
    var pattern = /\d{2,}/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
55,555,5555
```

### `n$`

#### 描述

匹配任何以 `n` 结尾的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to global search for "me" at the end of a string.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books! Welcome";
    var pattern = /me$/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
me
```

### `^n`

#### 描述

匹配任何以 `n` 开头的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to do a global search for "Welcome" at the beginning of a string.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
    var pattern = /^Welcome/g;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
Welcome
```

### `?=n`

#### 描述

匹配任何后面跟着特定字符串 `n` 的字符串。

#### 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to global search for "is" followed by " all".</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Is this all you want?";
    var pattern = /is(?= all)/;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```text
is
```

### `?!n`

#### 描述

匹配任何后面不跟着特定字符串 `n` 的字符串。

#### 示例代码



```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to do a global, case insensitive search for "is" not followed by " all".</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Is this all, there is another...";
    var pattern = /is(?! all)/gi;
    var result = str.match(pattern);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```
Is,is
```

## RegExp 对象方法

### ♥ `exec()`

#### ☺ 描述

在字符串中测试匹配。返回第一个匹配项。

#### ☺ 语法

`RegExpObject.exec(string)`

#### ☺ 参数

`string`：必需，要搜索的字符串。

#### ☺ 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>The exec() method returns the matched text if it finds a match, otherwise it returns null.</p>
<p>Click the button to search a string for the character "o".</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
   var pattern = new RegExp("o");
    var result = pattern.exec(str);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```
o
```

### ♥ `test()`

#### ☺ 描述

在字符串中测试匹配。返回 `true` 或 `false`。

#### ☺ 语法

`RegExpObject.test(string)`

#### ☺ 参数

`string`：必需，要搜索的字符串。

#### ☺ 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>The test() method returns true if it finds a match, otherwise it returns false.</p>
<p>Click the button to search a string for the character "o".</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var str = "Welcome to my books!";
   var pattern = new RegExp("o");
    var result = pattern.test(str);
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```
true
```

### ♥ `toString()`

#### ☺ 描述

返回正则表达式的字符串值。

#### ☺ 语法

`RegExpObject.toString()`

#### ☺ 参数

无。

#### ☺ 示例代码

```html
<!DOCTYPE html>
<html>
<body>
<p>Click the button to return the string value of the regular expression.</p>
<button onclick="myFunction()">Test</button>
<p id="demo"></p>
<script>
function myFunction() {
    var pattern = new RegExp("Welcome to my books!", "g");
    var result = pattern.toString();
    document.getElementById("demo").innerHTML = result;
}
</script>
</body>
</html>
```

♣ 输出

```
/Welcome to my books!/g
```
