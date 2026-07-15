![](cover.jpeg)

How to use Regular Expressions in JavaScript

VLIGHT

Table of Contents

[Modifiers](#part0000_split_002.html__Toc474090472)

[♥ i](#part0000_split_002.html__Toc474090473)

[♥ g](#part0000_split_003.html__Toc474090474)

[♥ m](#part0000_split_004.html__Toc474090475)

[Brackets](#part0000_split_005.html__Toc474090476)

[♥ [abc]](#part0000_split_005.html__Toc474090477)

[♥ [^abc]](#part0000_split_006.html__Toc474090478)

[♥ [0-9]](#part0000_split_007.html__Toc474090479)

[♥ [^0-9]](#part0000_split_008.html__Toc474090480)

[♥ (x|y)](#part0000_split_009.html__Toc474090481)

[Metacharacters](#part0000_split_010.html__Toc474090482)

[♥ .](#part0000_split_010.html__Toc474090483)

[♥ \w](#part0000_split_011.html__Toc474090484)

[♥ \W](#part0000_split_012.html__Toc474090485)

[♥ \d](#part0000_split_013.html__Toc474090486)

[♥ \D](#part0000_split_014.html__Toc474090487)

[♥ \s](#part0000_split_015.html__Toc474090488)

[♥ \S](#part0000_split_016.html__Toc474090489)

[♥ \b](#part0000_split_017.html__Toc474090490)

[♥ \B](#part0000_split_018.html__Toc474090491)

[♥ \0](#part0000_split_019.html__Toc474090492)

[♥ \n](#part0000_split_020.html__Toc474090493)

[♥ \f](#part0000_split_021.html__Toc474090494)

[♥ \r](#part0000_split_022.html__Toc474090495)

[♥ \t](#part0000_split_023.html__Toc474090496)

[♥ \v](#part0000_split_024.html__Toc474090497)

[♥ \xxx](#part0000_split_025.html__Toc474090498)

[♥ \xdd](#part0000_split_026.html__Toc474090499)

[♥ \uxxxx](#part0000_split_027.html__Toc474090500)

[Quantifiers](#part0000_split_028.html__Toc474090501)

[♥ n+](#part0000_split_028.html__Toc474090502)

[♥ n*](#part0000_split_029.html__Toc474090503)

[♥ n?](#part0000_split_030.html__Toc474090504)

[♥ n{X}](#part0000_split_031.html__Toc474090505)

[♥ n{X,Y}](#part0000_split_032.html__Toc474090506)

[♥ n{X,}](#part0000_split_033.html__Toc474090507)

[♥ n$](#part0000_split_034.html__Toc474090508)

[♥ ^n](#part0000_split_035.html__Toc474090509)

[♥ ?=n](#part0000_split_036.html__Toc474090510)

[♥ ?!n](#part0000_split_037.html__Toc474090511)

[RegExp Object Methods](#part0000_split_038.html__Toc474090512)

[♥ exec()](#part0000_split_038.html__Toc474090513)

[♥ test()](#part0000_split_039.html__Toc474090514)

[♥ toString()](#part0000_split_040.html__Toc474090515)

# 
Modifiers

## ♥  i

☺  Description

Perform case-insensitive matching

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a case-insensitive search for "Youtube" in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

Youtube

## 
♥  g

☺  Description

Perform a global match (find all matches rather than stopping after the first match)

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for "Welcome" in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

Welcome

## 
♥  m

☺  Description

Perform multiline matching

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a multiline search for "Welcome" at the beginning of each line in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

Welcome

# 
Brackets

## ♥  [abc]

☺  Description

Find any character between the brackets

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for the character "o" in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

o,o,o,o

## 
♥  [^abc]

☺  Description

Find any character NOT between the brackets

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for characters NOT inside the brackets [o] in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W,e,l,c,m,e, ,t, ,m,y, ,b,k,s,!

## 
♥  [0-9]

☺  Description

Find any digit between the brackets

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for the numbers 1 to 4 in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

3,4,5

## 
♥  [^0-9]

☺  Description

Find any digit NOT between the brackets

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for numbers that are NOT 1 to 4 in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

1,2,6,7,8,9,0

## 
♥  (x|y)

☺  Description

Find any of the alternatives specified

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for any of the specified alternatives (2|0).</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

2,0,2,0

# 
Metacharacters

## ♥  .

☺  Description

Find a single character, except newline or line terminator

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for "W.l" in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

Wel,Wel

## 
♥  \w

☺  Description

Find a word character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for word characters in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W,e,l,c,o,m,e,t,o,m,y,b,o,o,k,s

## 
♥  \W

☺  Description

Find a non-word character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for non-word characters in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

, , ,!,.

## 
♥  \d

☺  Description

Find a digit

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for digits in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

2,3,4

## 
♥  \D

☺  Description

Find a non-digit character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p id="demo">Click the button to do a global search for non-digit characters in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W,e,l,c,o,m,e, ,t,o, ,m,y, ,b,o,o,k,s,!, ,n,d, ,r,d, ,t,h

## 
♥  \s

☺  Description

Find a whitespace character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for whitespace characters in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

, ,

## 
♥  \S

☺  Description

Find a non-whitespace character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to search for non-whitespace characters in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W,e,l,c,o,m,e,t,o,m,y,b,o,o,k,s,!

## 
♥  \b

☺  Description

Find a match at the beginning/end of a word

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for "boo" at the beginning or end of a word in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

boo,boo

## 
♥  \B

☺  Description

Find a match not at the beginning/end of a word

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p id="demo">Click the button to do a global search for "ok"

NOT at the beginning or end of a word in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

ok

## 
♥  \0

☺  Description

Find a NUL character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to return the position where the NUL character was found in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

17

## 
♥  \n

☺  Description

Find a new line character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to return the position where the newline character was found in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

11

## 
♥  \f

☺  Description

Find a form feed character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to return the position where the form feed character was found in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

11

## 
♥  \r

☺  Description

Find a carriage return character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to return the position where the carriage return character was found in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

11

## 
♥  \t

☺  Description

Find a tab character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to return the position where the tab character was found in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

11

## 
♥  \v

☺  Description

Find a vertical tab character

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to return the position where the vertical tab character was found in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

11

## 
♥  \xxx

☺  Description

Find the character specified by an octal number xxx

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for octal number 127 (W) in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W

## 
♥  \xdd

☺  Description

Find the character specified by a hexadecimal number dd

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for the hexadecimal number 57 (W) in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W

## 
♥  \uxxxx

☺  Description

Find the Unicode character specified by a hexadecimal number xxxx

☺  Sample Code

<!DOCTYPE html>

<html>

<body>

<p>Click the button to do a global search for the hexadecimal number 0057 (W) in a string.</p>

<button onclick="myFunction()">Test</button>

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

♣  Output

W

# 
Quantifiers

## ♥  n+

☺  Description

Matches any string that contains at least one n

☺  Sample Code

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

♣  Output

o,o,oo

## 
♥  n*

☺  Description

Matches any string that contains zero or more occurrences of n

☺  Sample Code

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

♣  Output

boo,boo

## 
♥  n?

☺  Description

Matches any string that contains zero or one occurrences of n

☺  Sample Code

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

♣  Output

5,50,50,5

## 
♥  n{X}

☺  Description

Matches any string that contains a sequence of X n's

☺  Sample Code

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

♣  Output

555,555,555,555

## 
♥  n{X,Y}

☺  Description

Matches any string that contains a sequence of X to Y n's

☺  Sample Code

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

♣  Output

555,5555,55555,55555

## 
♥  n{X,}

☺  Description

Matches any string that contains a sequence of at least X n's

☺  Sample Code

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

♣  Output

55,555,5555

## 
♥  n$

☺  Description

Matches any string with n at the end of it

☺  Sample Code

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

♣  Output

me

## 
♥  ^n

☺  Description

Matches any string with n at the beginning of it

☺  Sample Code

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

♣  Output

Welcome

## 
♥  ?=n

☺  Description

Matches any string that is followed by a specific string n

☺  Sample Code

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

♣  Output

is

## 
♥  ?!n

☺  Description

Matches any string that is not followed by a specific string n

☺  Sample Code

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

♣  Output

Is,is

# 
RegExp Object Methods

## ♥  exec()

☺  Description

Tests for a match in a string. Returns the first match

☺  Syntax

RegExpObject.exec(string)

☺  Parameters

string: Required, the string to be searched

☺  Sample Code

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

♣  Output

o

## 
♥  test()

☺  Description

Tests for a match in a string. Returns true or false

☺  Syntax

RegExpObject.test(string)

☺  Parameters

string: Required, the string to be searched

☺  Sample Code

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

♣  Output

true

## 
♥  toString()

☺  Description

Returns the string value of the regular expression

☺  Syntax

RegExpObject.toString()

☺  Parameters

None

☺  Sample Code

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

♣  Output

/Welcome to my books!/g