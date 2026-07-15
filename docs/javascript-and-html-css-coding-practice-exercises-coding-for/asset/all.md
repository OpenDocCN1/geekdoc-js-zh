![](cover.jpeg)

JAVASCRIPT AND HTML CSS

CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

JJ TAM

[JavaScript functions – Exercises](#text00003.html__Toc68630659)

[JavaScript: Find the first not repeated character](#text00003.html__Toc68630660)

[JavaScript: Find the longest word within a string](#text00004.html__Toc68630661)

[JavaScript: Counts the number of vowels within a string](#text00005.html__Toc68630662)

[JavaScript: Check a number is prime or not](#text00006.html__Toc68630663)

[JavaScript: Get the data type](#text00007.html__Toc68630664)

[JavaScript: Find the second lowest and second greatest](#text00008.html__Toc68630665)

[JAVASCRIPT BASICS](#text00009.html__Toc68630666)

[Calculate multiplication and division](#text00009.html__Toc68630667)

[Convert temperatures](#text00010.html__Toc68630668)

[Find the largest](#text00011.html__Toc68630669)

[Reverse a given string](#text00012.html__Toc68630670)

[Replace every character](#text00013.html__Toc68630671)

[Create a new string](#text00014.html__Toc68630672)

[Concatenate two strings](#text00015.html__Toc68630673)

[Move last three character](#text00016.html__Toc68630674)

[Compute the sum](#text00017.html__Toc68630675)

[Add two digits](#text00018.html__Toc68630676)

[Check whether a given year is a leap](#text00019.html__Toc68630677)

[Check given positive number](#text00020.html__Toc68630678)

[Check a string starts with 'Java'](#text00021.html__Toc68630679)

[Check two given integer values](#text00022.html__Toc68630680)

[Find a value which is nearest to 100](#text00023.html__Toc68630681)

[HTML CSS CODING PRACTICE](#text00025.html__Toc68630682)

[Create a link](#text00025.html__Toc68630683)

[Create a nofollow link](#text00026.html__Toc68630684)

[Open a linked document](#text00027.html__Toc68630685)

[Correct way to write address](#text00028.html__Toc68630686)

[Specify an alternate text](#text00029.html__Toc68630687)

[Create an HTML document](#text00030.html__Toc68630688)

[Create an HTML document](#text00031.html__Toc68630689)

[To add controls to an audio](#text00032.html__Toc68630690)

[Write bold text using HTML tags](#text00033.html__Toc68630691)

[To specify the base URL](#text00034.html__Toc68630692)

[Isolate a part of text](#text00035.html__Toc68630693)

[HTML CSS Exercise: HTML table](#text00036.html__Toc68630694)

[HTML CSS Exercise: CSS Navigation bar](#text00037.html__Toc68630695)

[HTML CSS Exercise: HTML Form](#text00038.html__Toc68630696)

[HTML CSS Exercise: HTML5 Audio & Video](#text00039.html__Toc68630697)

[HTML CSS Exercise: CSS Button](#text00040.html__Toc68630698)

[HTML CSS Exercise: Create Stitched looks with css3](#text00041.html__Toc68630699)

[HTML CSS Exercise: Create corner ribbon with CSS3](#text00042.html__Toc68630700)

[HTML CSS Exercise: Blurry text with CSS3](#text00043.html__Toc68630701)

[Create a speech bubble shape with CSS3](#text00044.html__Toc68630702)

[Select elements by attribute](#text00045.html__Toc68630703)

[Set style for link, hover, active and visited states of hyperlink](#text00046.html__Toc68630704)

[HTML CSS Exercise: Type selector](#text00047.html__Toc68630705)

[This is heading one](#text00047.html__Toc68630706)

[HTML CSS Exercise: Descendant selector](#text00048.html__Toc68630707)

[Style placeholder text](#text00049.html__Toc68630708)

[Specify where to send the form-data](#text00050.html__Toc68630709)

[Send the form-data](#text00051.html__Toc68630710)

[Specify where to display](#text00052.html__Toc68630711)

[Specify a name for the button](#text00053.html__Toc68630712)

[Specify the type of button](#text00054.html__Toc68630713)

[Draw graphics, on the fly,](#text00055.html__Toc68630714)

[Define a table caption](#text00056.html__Toc68630715)

[Specify the column properties](#text00057.html__Toc68630716)

JAVASCRIPT

CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

JJ TAM

# JavaScript functions – Exercises

# JavaScript: Find the first not repeated character

Sample arguments  : 'abacddbec'
Expected output  : 'e'

## HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>find the first not repeated character.</title>

##### </head>

##### <body>

##### </body>

##### </html>

## JAVASCRIPT CODE

function find_FirstNotRepeatedChar(str) {

  var arra1 = str.split('');

  var result = '';

  var ctr = 0;

  for (var x = 0; x < arra1.length; x++) {

    ctr = 0;

    for (var y = 0; y < arra1.length; y++)

    {

      if (arra1[x] === arra1[y]) {

        ctr+= 1;

      }

    }

    if (ctr < 2) {

      result = arra1[x];

      break;

    }

  }

  return result;

}

console.log(find_FirstNotRepeatedChar('abacddbec'));

### OUTPUT

e

### FLOWCHART

![](OEBPS/Image00000.jpg)

# JavaScript: Find the longest word within a string

Example string : 'Web Development Tutorial'
Expected Output:  'Development'

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Find the longest word within a string</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function find_longest_word(str)

##### {

#####   var array1 = str.match(/\w[a-z]{0,}/gi);

#####   var result = array1[0];

#####   for(var x = 1 ; x < array1.length ; x++)

#####   {

#####     if(result.length < array1[x].length)

#####     {

#####     result = array1[x];

#####     }

#####   }

#####   return result;

##### }

##### console.log(find_longest_word('Web Development Tutorial'));

### OUTPUT

Development

### EXPLANATION

Assume that str equals '@Web Production #Tutorial'.

When a string is matched against a regular expression, the match() method is used to obtain the matches.

As a result of str.match(/w[a-z]0,/gi), ["Web", "Development", "Tutorial"] will be returned.

The for loop compares the length of each array element to the previous one and returns the longest string.

The length property is a 32-bit unsigned integer that is always numerically greater than the array's highest index.

Syntax -> arr.length

#### FLOWCHART

![](OEBPS/Image00001.jpg)

# JavaScript: Counts the number of vowels within a string

Example string : 'The quick brown fox'
Expected Output:  5

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Counts the number of vowels within a string</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function vowel_count(str1)

##### {

#####   var vowel_list = 'aeiouAEIOU';

#####   var vcount = 0;

#####   for(var x = 0; x < str1.length ; x++)

#####   {

#####     if (vowel_list.indexOf(str1[x]) !== -1)

#####     {

#####       vcount += 1;

#####     }

#####   }

#####   return vcount;

##### }

##### console.log(vowel_count("The quick brown fox"));

#### OUTPUT

5

### EXPLANATION

The indexOf() method returns the index of the first occurrence of the defined value within the calling String object, starting at fromIndex. If the value cannot be found, it returns -1.

Syntax -> str.indexOf(searchValue[, fromIndex])

Parameters include:

searchValue : A string that represents the value to be sought.

fromIndex(Optional)-> The index at which the string's forward search should begin. Any integer can be used.

If the condition (vowel list.indexOf(str1[x])!== -1) is met, the character(s) of the string will be counted as vowels.

### FLOWCHART

![](OEBPS/Image00002.jpg)

# JavaScript: Check a number is prime or not

![](OEBPS/Image00003.jpg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Check a number is prime or not</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function test_prime(n)

##### {

#####   if (n===1)

#####   {

#####     return false;

#####   }

#####   else if(n === 2)

#####   {

#####     return true;

#####   }else

#####   {

#####     for(var x = 2; x < n; x++)

#####     {

#####       if(n % x === 0)

#####       {

#####         return false;

#####       }

#####     }

#####     return true; 

#####   }

##### }

##### console.log(test_prime(37));

### OUTPUT

True

FLOWCHART

![](OEBPS/Image00004.jpg)

# JavaScript: Get the data type

#### We going to Create a JavaScript function which takes an argument and returns the type.

#### Note six possible values: object, boolean, method, number, string, or undefined.

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Detect JavaScript Data Types</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function detect_data_type(value)

##### {

##### var dtypes = [Function, RegExp, Number, String, Boolean, Object], x, len;

##### if (typeof value === "object" || typeof value === "function")

#####     {

#####      for (x = 0, len = dtypes.length; x < len; x++)

#####      {

#####             if (value instanceof dtypes[x])

#####             {

#####                 return dtypes[x];

#####             }

#####       }

#####     }

#####     return typeof value;

##### }

##### console.log(detect_data_type(12));

##### console.log(detect_data_type('w3resource'));

##### console.log(detect_data_type(false));

#### OUTPUT

number

string

Boolean

# JavaScript: Find the second lowest and second greatest

## numbers from an array

![](OEBPS/Image00005.jpg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Find the second lowest and second greatest numbers from an array</title>

##### </head>

##### <body>

##### </body>

### JAVASCRIPT CODE

##### function Second_Greatest_Lowest(arr_num)

##### {

#####   arr_num.sort(function(x,y)

#####            {

#####            return x-y;

#####            });

#####   var uniqa = [arr_num[0]];

#####   var result = [];

#####   for(var j=1; j < arr_num.length; j++)

#####   {

#####     if(arr_num[j-1] !== arr_num[j])

#####     {

#####       uniqa.push(arr_num[j]);

#####     }

#####   }

#####     result.push(uniqa[1],uniqa[uniqa.length-2]);

#####   return result.join(',');

#####   }

##### console.log(Second_Greatest_Lowest([1,2,3,4,5]));

#### OUTPUT

2,4

### FLOWCHART

![](OEBPS/Image00006.jpg)

# JAVASCRIPT BASICS

# Calculate multiplication and division

## of two numbers

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>JavaScript program to calculate multiplication and division of two numbers </title>

##### <style type="text/css">

##### body {margin: 30px;}

##### </style>

##### </head>

##### <body>

##### <form>

##### 1st Number : <input type="text" id="firstNumber" /><br>

##### 2nd Number: <input type="text" id="secondNumber" /><br>

##### <input type="button" onClick="multiplyBy()" Value="Multiply" />

##### <input type="button" onClick="divideBy()" Value="Divide" />

##### </form>

##### <p>The Result is : <br>

##### <span id = "result"></span>

##### </p>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function multiplyBy()

##### {

#####         num1 = document.getElementById("firstNumber").value;

#####         num2 = document.getElementById("secondNumber").value;

#####         document.getElementById("result").innerHTML = num1 * num2;

##### }

##### function divideBy()

##### {

#####         num1 = document.getElementById("firstNumber").value;

#####         num2 = document.getElementById("secondNumber").value;

##### document.getElementById("result").innerHTML = num1 / num2;

##### }

### EXPLANATION

document.getElementById(id).value: The value property of a text field sets or returns the value of the value attribute.

document.getElementById("result").innerHTM : The innerHTML property of an element sets or returns the HTML content (inner HTML).

#### OUTPUT

![](OEBPS/Image00007.jpg)

# Convert temperatures

## To and from celsius, Fahrenheit in JAVASCRIPT

### HTML CODE

##### <!DOCTYPE html>

#####   <html>

#####   <head>

#####   <meta charset="utf-8">

#####   <title>Write a JavaScript program to convert temperatures to and from celsius, fahrenheit</title>

#####   </head>

#####   <body>

##### </body>

#####   </html>

### JAVASCRIPT CODE

##### function cToF(celsius)

##### {

#####   var cTemp = celsius;

#####   var cToFahr = cTemp * 9 / 5 + 32;

#####   var message = cTemp+'\xB0C is ' + cToFahr + ' \xB0F.';

#####     console.log(message);

##### }

##### function fToC(fahrenheit)

##### {

#####   var fTemp = fahrenheit;

#####   var fToCel = (fTemp - 32) * 5 / 9;

#####   var message = fTemp+'\xB0F is ' + fToCel + '\xB0C.';

#####     console.log(message);

##### }

##### cToF(60);

##### fToC(45);

### OUTPUT

60°C is 140 °F.

45°F is 7.222222222222222°C.

### EXPLANATION

The following formulas can be used to make an exact conversion (Fahrenheit to Celsius / Celsius to Fahrenheit):

Fahrenheit to Celsius : (°F − 32) ÷ 1.8 = °C
Celsius to Fahrenheit : (°C × 1.8) + 32 = °F

The following is a rough conversion between degrees Celsius and degrees Fahrenheit:

To convert from Fahrenheit to Celsius, deduct 30 and divide by two.

To convert from Celsius to Fahrenheit, multiply the number by two and add 30.

# Find the largest

## Of three given integers

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to find the largest of three given integers.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function max_of_three(x, y, z)

##### {

#####   max_val = 0;

#####   if (x > y)

#####   {

#####     max_val = x;

#####   } else

#####   {

#####     max_val = y;

#####   }

#####   if (z > max_val)

#####   {

#####     max_val = z;

#####   }

#####   return max_val;

##### }

##### console.log(max_of_three(1,0,1));

##### console.log(max_of_three(0,-10,-20));

##### console.log(max_of_three(1000,510,440));

Output:

1

0

1000

### FLOWCHART

![](OEBPS/Image00008.jpg)

# Reverse a given string

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to reverse a given string.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function string_reverse(str)

##### {

#####     return str.split("").reverse().join("");

##### }

##### console.log(string_reverse("jsresource"));

##### console.log(string_reverse("www"));

##### console.log(string_reverse("JavaScript"));

### OUTPUT

ecruosersj

www

tpircSavaJ

# Replace every character

## with the character following it in the alphabet

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to replace every character in a given string with the character following it in the alphabet.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function string_reverse(str)

##### function LetterChanges(text) {

##### //https://goo.gl/R8gn7u

##### var s = text.split('');

##### for (var i = 0; i < s.length; i++) {

##### // Caesar cipher

##### switch(s[i]) {

##### case ' ':

##### break;

##### case 'z':

##### s[i] = 'a';

##### break;

##### case 'Z':

##### s[i] = 'A';

##### break;

##### default:

##### s[i] = String.fromCharCode(1 + s[i].charCodeAt(0));

##### }

##### // Upper-case vowels

##### switch(s[i]) {

##### case 'a': case 'e': case 'i': case 'o': case 'u':

##### s[i] = s[i].toUpperCase();

##### }

##### }

##### return s.join('');

##### }

##### console.log(LetterChanges("PYTHON"));

##### console.log(LetterChanges("W3R"));

##### console.log(LetterChanges("php"));

### Output:

QZUIPO

X4S

qIq

# Create a new string  

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to create a new string without the first and last character.</title>

</head>

<body>

</body>

</html>

### JAVASCRIPT CODE

function without_first_end(str) {

  return str.substring(1, str.length - 1);

}

console.log(without_first_end('JavaScript'));

console.log(without_first_end('JS'));

console.log(without_first_end('PHP'));

### Output:

avaScrip

H

# Concatenate two strings

## Except their first character

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to concatenate two strings except their first character.</title>

</head>

<body>

</body>

</html>

### JAVASCRIPT CODE

function concatenate(str1, str2) {

  str1 = str1.substring(1, str1.length);

  str2 = str2.substring(1, str2.length);

  return str1 + str2;

}

console.log(concatenate("PHP","JS"));

console.log(concatenate("A","B"));

console.log(concatenate("AA","BB"));

### Output:

HPS

AB

# Move last three character

## start of a specified string

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to move last three character to the start of a given string. The string length must be 3.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function right_three(str) {

#####      if (str.length > 1)

#####        {

#####          return str.slice(-3) + str.slice(0, -3);

#####        }

#####   return str;

##### }

##### console.log(right_three("Python"));

##### console.log(right_three("JavaScript"));

##### console.log(right_three("Hi"));

### Output:

honPyt

iptJavaScr

Hi

# Compute the sum

## Of three elements of a given array

### Of integers of length 3

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to compute the sum of three elements of an given integers of length 3.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function sum_three(nums)

##### {

#####   return nums[0] + nums[1] + nums[2];

##### }

##### console.log(sum_three([10, 32, 20])); 

##### console.log(sum_three([5, 7, 9]));

##### console.log(sum_three([0, 8, -11]));

### Output:

62

21

-3

# Add two digits

## Of a given positive integer

### Of length two

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to add two digits of a given positive integer of length two.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function add_two_digits(n)

#####    {

#####       return n % 10 + Math.floor(n / 10);

#####    }

##### console.log(add_two_digits(25))

##### console.log(add_two_digits(50))

### Output:

7

5

# Check whether a given year is a leap

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Find Leap Year</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function leapyear(year)

##### {

##### return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);

##### }

##### console.log(leapyear(2016));

##### console.log(leapyear(2000));

##### console.log(leapyear(1700));

##### console.log(leapyear(1800));

##### console.log(leapyear(100));

### OUTPUT

true

true

false

false

false

# Check given positive number

## Multiple of 3 or a multiple of 7

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to check whether a given positive number is a multiple of 3 or a multiple of 7\. </title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function test37(x)

##### {

#####   if (x % 3 == 0 || x % 7 == 0)

#####   {

#####     return true;

#####   }

#####   else {

#####     return false;

#####   }

##### }

##### console.log(test37(12));

##### console.log(test37(14));

##### console.log(test37(10));

##### console.log(test37(11));

### Output:

true

true

false

false

# Check a string starts with 'Java'

## And false otherwise

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to check whether a string starts with 'Java' and false otherwise.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function start_spec_str(str)

##### {

#####   if (str.length < 4)

#####   {

#####     return false;

#####   }

#####   front = str.substring(0, 4);

#####   if (front == 'Java')

#####   {

#####     return true;

#####   }

#####    else

#####    {

#####     return false;

#####   }

##### }

##### console.log(start_spec_str("JavaScript"));

##### console.log(start_spec_str("Java"));

##### console.log(start_spec_str("Python"));

### Output:

true

true

false

# Check two given integer values

## In the range 50..99

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to check whether two given integer values are in the range 50..99 (inclusive). Return true if either of them are in the said range.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function check_numbers(x, y)

#####   {

#####   if ((x >= 50 && x <= 99) || (y >= 50 && y <= 99))

#####   {

#####     return true;

#####   }

#####   else

#####   {

#####     return false;

#####   }

##### }

##### console.log(check_numbers(12, 101));

##### console.log(check_numbers(52, 80));

##### console.log(check_numbers(15, 99));

### OUTPUT

false

true

true

# Find a value which is nearest to 100

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to find a value which is nearest to 100 from two different given integer values.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function near_100(x, y) {

#####   if (x != y)

#####   {

#####   x1 = Math.abs(x - 100);

#####   y1 = Math.abs(y - 100);

#####   if (x1 < y1)

#####   {

#####     return x;

#####   }

#####   if (y1 < x1)

#####   {

#####     return y;

#####   }

#####   return 0;

#####   }

#####   else

#####     return false;

##### }

##### console.log(near_100(90, 89));

##### console.log(near_100(-90, -89));

##### console.log(near_100(90, 90));

### Output:

90

-89

false

HTML CSS

CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

JJ TAM

# HTML CSS CODING PRACTICE

# Create a link

## with a media attribute

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>Create a link with a media attribute</title>

</head>

<body>

  <a href="https://www.htmlresource.com" media="print, handheld">Media Attribute</a>

</body>

</html>

# Create a nofollow link

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>How to create a nofollow link</title>

</head>

<body>

  <a rel="nofollow" href="http://htmlexample.com">Example.com</a>

</body>

</html>

# Open a linked document

## in a separate browser tab

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>How to open a linked document in a separate browser tab</title>

</head>

<body>

  <p><a href="https://htmlresource.com" target="_blank">Target HTML5 EXCECISES</a></p>

</body>

</html>

# Correct way to write address

## in a HTML document

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>What is the correct way to write address in a HTML document</title>

</head>

<body>

  <address>

    Address: 21,MG Road<br>

Burdwan<br>

West Bengal.

  </address>

</body>

</html>

# Specify an alternate text

## for the area

### if the href attribute is present

### HTML CODE

##### <body> 

##### <img src="https://www.htmlresource.com/htmlr_images/html-area-element.png" alt="area example"  border="0" usemap="#Map"/> 

##### <map name="Map"> 

##### <area shape="rect" coords="8,5,100,77" href="https://www.htmlresource.com/mysql/mysql-tutorials.php" target="_blank" alt="mysql tutorial"> 

##### <area shape="circle" coords="155,93,59" href="https://www.htmlresource.com/php/php-home.php" target="_blank" alt="php tutorial"> 

##### <area shape="rect" coords="197,136,306,188" href="https://www.htmlresource.com/sql/sql-tutorials.php" alt="sql tutorials"> 

##### </map> 

##### </body>

# Create an HTML document

## which uses article element

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>Create an HTML document which uses article element</title>

##### </head>

##### <body>

##### <article> 

##### <h1>Tutorial of HTML5 article element</h1> 

##### <p>HTML5 article element represents independent item like a blog entry in an web document.</p> 

##### </article> 

##### </body>

##### </html>

# Create an HTML document

## which uses aside element

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to create an HTML document which uses aside element</title>

##### </head>

##### <body>

##### <p> I visited the HTML5 tutorial of htmlresource</p>

##### <aside>

#####   <h4>HTML5 tutorial</h4>

#####   <p>I can develop excellent web applications with HTML5 and related APIs (like GeoLocation, Drag and Drop, WebSocket etc.)in HTML5 tutorial.</p>

##### </aside>

##### </body>

##### </html>

#### OUTPUT

I visited the HTML5 tutorial of htmlresource

#### HTML5 tutorial

I can develop excellent web applications with HTML5 and related APIs (like GeoLocation, Drag and Drop, WebSocket etc.)in HTML5 tutorial.

# To add controls to an audio

### HTML CODE

<body>

<audio controls>

    <source src="https://www.htmlresource.com/html-css-exercise/basic/solution/beach.ogg" type="audio/ogg">

<source src="https://www.htmlresource.com/html-css-exercise/basic/solution/beach.mp3" type="audio/mpeg">

</audio>

</body>

# Write bold text using HTML tags

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>How to write bold text using HTML tags</title>

</head>

<body>

  <p>"htmlresource" is normal text - and <b>"htmlresource"</b> is bold text.

</body>

</html>

#### OUTPUT

"htmlresource" is normal text - and  "htmlresource"  is bold text.

# To specify the base URL

#### HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset="utf-8">

<title>How to specifie the base URL/target for all relative URLs in a document</title> 

<base href="https://www.htmlresource.com/"> 

</head> 

<body> 

<ul> 

<li><a href="php/php-home.php">PHP Tutorial</a></li> 

<li><a href="javascript/javascript.php">JavaScript Tutorial</a></li> 

<li><a href="mysql/mysql-tutorials.php">MySQL Tutorial</a></li> 

</body>

</html>

# Isolate a part of text

## That might be formatted

### In a different direction

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title><span class="heading">How to isolate a part of text that might be formatted in a different direction from other text outside it</span></title>

</head>

<body>

<p>

In the example below, usernames are shown along with the number of points in a contest.

If the bdi element is not supported in the browser, the username of the Arabic user would confuse the text (the bidirectional algorithm would put the colon and the number "80" next to the word "User" rather than next to the word "points").

</p>

<ul>

<li>User <bdi>hrefs</bdi>: 40 points</li>

<li>User <bdi>jdoe</bdi>: 60 points</li>

<li>User <bdi > ترحي ب </bdi>:80 points</li>

</ul>

<p><b>Note:</b> The bdi element is currently supported only in Firefox and Chrome.</p>

</body>

</html>

#### OUTPUT

In the example below, usernames are shown along with the number of points in a contest. If the bdi element is not supported in the browser, the username of the Arabic user would confuse the text (the bidirectional algorithm would put the colon and the number "80" next to the word "User" rather than next to the word "points").

*   User hrefs: 40 points
*   User jdoe: 60 points
*   User ترحيب:80 points

Note:  The bdi element is currently supported only in Firefox and Chrome.

# HTML CSS Exercise: HTML table

## HTML CODE

##### <table border="1">

##### <tr>

##### <td>Quick</td>

##### <td colspan="2">brown fox</td>

##### <td>jumps</td>

##### </tr>

##### <tr>

##### <td rowspan="3">over the</td>

##### <td>lazy</td>

##### <td>dog</td>

##### <td>and</td>

##### </tr>

##### <tr>

##### <td>then</td>

##### <td>it</td>

##### <td>fall</td>

##### </tr>

##### <tr>

##### <td colspan="3">prey to a hunter</td>

##### </tr>

##### </table>

### OUTPUT

![](OEBPS/Image00009.jpg)

# HTML CSS Exercise: CSS Navigation bar

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>HTML CSS exercise - create a simple navigaiton bar</title>

##### <style type="text/css">

##### nav {

##### display: block;

##### position: absolute;

##### top: 0;

##### width: 100%;

##### background-color: green;

##### }

##### li{

##### list-style-type: none;

##### display: inline;

##### margin-right: 20px;

##### font-size:25px

##### }

##### a:link {

##### color: #fff;

##### text-decoration: none;

##### }

##### a:hover {

##### color: orange;

##### text-decoration: none;

##### }

##### li > ul {

##### display: none

##### }

##### li:hover ul {display: block; position: absolute; left:200px;background-color:green;margin:0;}

##### li:hover ul li a:link{display: block;margin-left:-30px;}

##### </style>

##### </head>

##### <body>

##### <nav>

##### <ul>

##### <li><a href="#">Home</a></li>

##### <li><a href="#">About</a></li>

##### <li>

##### <a href="#">Products</a>

##### <ul>

##### <li><a href="#">Engineering</a></li>

##### <li><a href="#">Telecom</a></li>

##### <li><a href="#">Energy</a></li>

##### <li><a href="#">Finance</a></li>

##### <li><a href="#">Consultancy</a></li>

##### </ul>

##### </li>

##### <li><a href="#">Services</a></li>

##### <li><a href="#">Contact</a></li>

##### </ul>

##### </nav>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00010.jpg)

# HTML CSS Exercise: HTML Form

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>HTML CSS Form exercise</title>

##### </head>

##### <body>

##### <div class="container">

##### <h1>Travel reservation form</h1>

##### <h3>* denotes mandotory</h3>

##### <form id="registration_form" method="POST">

#####   <label>Full name*:</label><br>

#####   <input type="text" name="full_name" placeholder="FirstName LastName" autofocus="autofocus" value=""><br>  

#####   <label>Email address*:</label><br>

#####   <input type="text" name="email_addr" value=""><br>

#####   <label>Select Tour Package* :</label><br>

#####    <select name="package">

##### <option value="Goa" >Goa</options>

##### <option value="Kashmir" >Kashmir</options>

##### <option value="Rajasthan" >Rajasthan</options>

#####    </select><br>

#####   <label>Arrival date*:</label><br>

#####   <input type="text" name="arv_dt" placeholder="m/d/y" value=""><br>

#####         <label>Number of persons*:</label><br>

#####   <input type="text" name="persons" value=""s><br>

#####      <label>What would you want to avail?*</label> <br>

##### Boarding<input type="checkbox" name="facilities[]" value="boarding"  ><br>

##### Fooding<input type="checkbox" name="facilities[]" value="fooding"  ><br>

##### Sight seeing<input type="checkbox" name="facilities[]" value="sightseeing"  ><br>

#####    <label>Discount Coupon code:</label><br>

#####   <input type="text" name="dis_code" value=""><br>

#####       <label>Terms and conditions*</label><br>

#####   <input type="radio" name="tnc" value="agree" checked>I agree

#####   <input type="radio" name="tnc" value="disagree" >I disagree<br>

#####   <button type="submit" class="btn btn-large btn-primary" name="submit">Complete reservation</button>

##### </form>

##### </div>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00011.jpg)

# HTML CSS Exercise: HTML5 Audio & Video

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>HTML CSS Audio/Video exercise</title>

##### </head>

##### <body>

##### <video controls>

#####   <source src="big_buck_bunny.mp4" type="video/ogv">

#####   <source src="big_buck_bunny.mp4" type="video/mp4">

#####   Your browser does not support the <code>video</code> element.

##### </video>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00012.jpg)

# HTML CSS Exercise: CSS Button

### HTML CODE

##### <!doctype html>

##### <html>

##### <head>

##### <title>HTML CSS Exercise - create button with CSS3</title>

##### <style>

##### button {

##### width: 200px;

##### padding:8px;

##### background-color: #428bca;

##### border-color: #357ebd;

##### color: #fff;

##### -moz-border-radius: 10px;

##### -webkit-border-radius: 10px;

##### border-radius: 10px; /* future proofing */

##### -khtml-border-radius: 10px; /* for old Konqueror browsers */

##### text-align: center;

##### vertical-align: middle;

##### border: 1px solid transparent;

##### font-weight: 900;

##### font-size:125%

##### }

##### </style>

##### <title>Untitled Document</title>

##### </head>

##### <body>

##### <button>Subscribe Now</button>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00013.jpg)

# HTML CSS Exercise: Create Stitched looks with css3

### HTML CODE

##### <!DOCTYPE html>

##### <html lang="en">

##### <head>

#####     <meta charset="utf-8">

#####     <title>Create a Stiched Look with CSS3</title>

#####     <style>

#####     .stitched {

#####    width: 200px;

#####    padding: 20px;

#####    margin: 10px;

#####    background: #0d90df;

#####    color: #fff;

#####    font-size: 21px;

#####    font-weight: bold;

#####    line-height: 1.3em;

#####    border: 2px dashed #fff;

#####    border-radius: 10px;

#####    box-shadow: 0 0 0 4px #0d90df, 2px 1px 6px 4px rgba(10, 10, 0, 0.5);

#####    text-shadow: -1px -1px #aa3030;

#####    font-weight: normal;

##### }

#####     </style>

##### </head>

##### <body>

#####     <div class="stitched"></div>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00014.jpg)

# HTML CSS Exercise: Create corner ribbon with CSS3

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>Corner Ribbon with CSS3 Example</title>

##### <style type="text/css">

##### .ribbon {

#####   background-color: #a00;

#####   overflow: hidden;

#####   white-space: nowrap;

#####   /* top left corner */

#####   position: absolute;

#####   left: -50px;

#####   top: 40px;

#####   /* for 45 deg rotation */

#####   -webkit-transform: rotate(-45deg);

#####      -moz-transform: rotate(-45deg);

#####       -ms-transform: rotate(-45deg);

#####        -o-transform: rotate(-45deg);

#####           transform: rotate(-45deg);

#####   /* for creating shadow */

#####   -webkit-box-shadow: 0 0 10px #888;

#####      -moz-box-shadow: 0 0 10px #888;

#####           box-shadow: 0 0 10px #888;

##### }

##### .ribbon a {

#####   border: 1px solid #faa;

#####   color: #fff;

#####   display: block;

#####   font: bold 100% 'Helvetica Neue', Helvetica, Arial, sans-serif;

#####   margin: 1px 0;

#####   padding: 10px 50px;

#####   text-align: center;

#####   text-decoration: none;

#####   /* for creating shadow */

#####   text-shadow: 0 0 5px #444;

##### }

#####   </style>

##### </head>

##### <body>

##### <div class="ribbon">

#####   <a href="#">Best value pack</a>

##### </div>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00015.jpg)

# HTML CSS Exercise: Blurry text with CSS3

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>Blurry text with CSS3</title>

##### <style type="text/css">

##### p{

##### color:#000000;  /* this is for old browsers */

##### font-size:50px;

##### font-family:arial;

##### text-shadow:   0 0 3px #000000, 

##### 3px 0 3px #000000,

##### 0 3px 3px #000000,

##### -3px 0 3px #000000,

##### 0 -3px 3px #000000;

##### }

##### </style>

##### </head>

##### <body>

##### <p>This text is blurred</p>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00016.jpg)

# Create a speech bubble shape with CSS3

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>Create a speech bubble shape with CSS3</title>

##### <style type="text/css">

##### #speech-bubble {

#####    width: 120px;

#####    height: 80px;

#####    background: #5ac4ed;

#####    position: absolute;

#####    left:100px;

#####    -moz-border-radius: 10px;

#####    -webkit-border-radius: 10px;

#####    border-radius: 10px;

##### }

##### #speech-bubble:before {

#####    content:"";

#####    position: absolute;

#####    width: 0;

#####    height: 0;

#####    border-top: 13px solid transparent;

#####    border-right: 26px solid #5ac4ed;

#####    border-bottom: 13px solid transparent;

#####    margin: 13px 0 0 -25px;

##### }

##### </style>

##### </head>

##### <body>

##### <div id="speech-bubble"></div>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00017.jpg)

# Select elements by attribute

### HTML CODE

##### <!doctype html>

##### <html>

##### <head>

##### <title>HTML CSS Exercise - Select elements by attribute</title>

##### <style>

##### .container[data-name=w3r]{

##### color:#5ac4ed;

##### }

##### </style>

##### </head>

##### <body>

##### <div class="container" data-name="w3r">Web developemnt tutorials.</div>

##### <div class="container">HTML, CSS, JS, PHP...</div>

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00018.jpg)

# Set style for link, hover, active and visited states of hyperlink

### HTML CODE

##### <!doctype html>

##### <html>

##### <head>

##### <title>HTML CSS Exercise - set style for link, hover, active and visited states of hyperlink</title>

##### <style>

##### a:link {

##### color: #0e630f

##### }

##### a:hover {

##### color: #ec8007

##### }

##### a:active {

##### color:#602206

##### }

##### a:visited {

##### color:#4f628e

##### }

##### </style>

##### </head>

##### <body>

##### <a href="http://www.example.com">This is a hyperlink</a>

##### </body>

##### </html>

### OUTPUT

[This is a hyperlink](http://www.example.com/)

# HTML CSS Exercise: Type selector

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>CSS Type selector example</title>

##### <style type="text/css">

##### h1{

##### color:#4b6c9c; 

##### }

##### </style>

##### </head>

##### <body>

##### <h1>This is heading one</h1>

##### </body>

##### </html>

### OUTPUT

# This is heading one

# HTML CSS Exercise: Descendant selector

### HTML CODE

##### <!DOCTYPE HTML>

##### <html lang="en">

##### <head>

##### <meta charset=utf-8>

##### <title>CSS Descendant selectors example</title>

##### <style type="text/css">

##### p span{

##### color:#4b6c9c; 

##### }

##### </style>

##### </head>

##### <body>

##### <p>Only run of <span>text within span</span> will be of different color</p>

##### </body>

##### </html>

#### OUTPUT

Only run of  text within span  will be of different color

# Style placeholder text

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>HTML CSS Exercises - Style Placeholder text</title>

##### <style type="text/css">

##### input[type="text"]::-webkit-input-placeholder {

#####   color: orange;

##### }

##### </style>

##### </head>

##### <body>

##### //insert this within html section. within body of codepen

##### <form action="">

##### <div>

#####     <label for="email">Email:</label>

#####     <input id="email" name="email" type="text" placeholder="yourname@yourdomain.com">

#####   </div>

##### </form>

##### //insert this within css section. within body of codepen

##### </body>

##### </html>

### OUTPUT

![](OEBPS/Image00019.jpg)

# Specify where to send the form-data

## when a form is submitted

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>How to Specify where to send the form-data when a form is submitted.</title>

</head>

<body>

<form action="https://www.htmlresource.com/html-css-exercise/basic/solution/button-formaction-

answer-demo.php" method="post">

  First name: <input type="text" name="fname"><br>

  Last name: <input type="text" name="lname"><br>

  <button type="submit">Submit</button><br>

  <button type="submit" formaction="https://www.htmlresource.com/html-css-

exercise/basic/solution/button-formaction-admin-demo.php">Submit as admin</button>

</form>

</body>

</html>

#### OUTPUT

![](OEBPS/Image00020.jpg)

# Send the form-data

## (which HTTP method to use)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to send the form-data,which HTTP method to use</title>

##### </head>

##### <body>

##### <form action="https://www.htmlresource.com/html-css-exercise/basic/solution/button-formmethod-answer-demo.php">

#####   First name: <input type="text" name="fname"><br>

#####   Last name: <input type="text" name="lname"><br>

#####   Address: <input type="text" name="place"><br>

#####   <button type="submit">Submit</button>

#####   <button type="submit" formmethod="post" formaction="http://localhost/html-css-exercise/basic/solution/button-formmethod-post-answer.php">Submit using POST</button>

##### </form>

##### </body>

##### </html>

#### OUTPUT

![](OEBPS/Image00021.jpg)

# Specify where to display

## the response after submitting the form

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to specify where to display the response after submitting the form</title>

##### </head>

##### <body>

##### <form action="https://www.htmlresource.com/html-css-exercise/basic/solution/button-formtarget-answer-demo.php" method="POST">

#####   First name: <input type="text" name="fname"><br>

#####   Last name: <input type="text" name="lname"><br>

#####   <button type="submit">Submit</button>

#####   <button type="submit" formtarget="_blank">Submit to a new window/tab</button>

##### </form>

##### </body>

##### </html>

#### OUTPUT

![](OEBPS/Image00022.jpg)

# Specify a name for the button

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

##### <title>How to specify a name for the button</title> 

##### </head> 

##### <body> 

##### <form action="https://www.htmlresource.com/html-css-exercise/basic/solution/button-name-answer-demo.php" method="post">

##### Choose your favorite topic:

##### <button name="topic" type="submit" value="JavaScript">JavaScript</button>

##### <button name="topic" type="submit" value="PHP">PHP</button>

##### </form>

##### </body>

##### </html>

#### OUTPUT

![](OEBPS/Image00023.jpg)

# Specify the type of button

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to specify the type of button</title>

##### </head>

##### <body>

##### <form action="https://www.htmlresource.com/html-css-exercise/basic/solution/button-type-answer-demo.php" method="post"id="nameform">

##### First name: <input type="text" name="fname"><br>

##### Last name: <input type="text" name="lname"><br>

##### Address: <input type="text" name="add"><br>

##### <button type="submit" value="Submit">Submit</button>

##### <button type="reset" value="Reset">Reset</button>

##### </form>

##### </body>

##### </html>

#### OUTPUT

![](OEBPS/Image00024.jpg)

# Draw graphics, on the fly,

## via scripting

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to use to draw graphics, on the fly, via scripting</title>

##### </head>

##### <body>

##### Canvas

##### <style> 

##### #FirstCanvas{ 

##### width: 500px; 

##### height: 300px; 

##### border: 3px solid red; 

##### background-color: blue; 

##### } 

##### </style>

##### <body> 

##### <canvas id="FirstCanvas"></canvas> 

##### </body>

##### </html>

#### OUTPUT

![](OEBPS/Image00025.jpg)

# Define a table caption

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to define a table caption</title>

##### </head>

##### <body>

##### <table border="1"> 

##### <caption>First column holds Student code and second column holds percentage of marks obtained by the student</caption> 

##### <tr>  

##### <th>Student code </th> 

##### <th>% of marks </th> 

##### </tr> 

##### <tr>  

##### <td>S001</td> 

##### <td>85</td> 

##### </tr> 

##### <tr>  

##### <td>S002</td> 

##### <td>86</td> 

##### </tr> 

##### <tr>  

##### <td>S003</td> 

##### <td>72</td> 

##### </tr> 

##### <tr>  

##### <td>S004</td> 

##### <td>89</td> 

##### </tr> 

##### </table

##### </body>

##### </html>

#### OUTPUT

![](OEBPS/Image00026.jpg)

# Specify the column properties

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>How to specify the column properties of each column within a column group element</title>

##### </head>

##### <body>

##### <table class="table table-bordered">

#####   <colgroup>

#####     <col span="3" style="background-color:#cc66Ff">

##### <col style="background-color:#cc66Ff">

#####   </colgroup>

#####   <tr>

#####     <th>COL-1</th>

#####     <th>COL-2</th>

#####     <th>COL-3</th>

#####   </tr>

#####   <tr>

#####     <td>MySQL</td>

#####     <td>PHP</td>

#####     <td>SQL</td>

#####   </tr>

#####   <tr>

#####     <td>MySQL Exercise</td>

#####     <td>PHP Exercise</td>

#####     <td>SQL Exercise</td>

#####   </tr>

##### </table>

##### </body>

##### </html>

#### OUTPUT

#### ![](OEBPS/Image00027.jpg)