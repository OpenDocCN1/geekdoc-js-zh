![](cover.jpeg)

JAVASCRIPT

CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

JJ TAM

[JavaScript functions – Exercises](#text00002.html__Toc68199568)

[JavaScript: Find the first not repeated character](#text00002.html__Toc68199569)

[JavaScript: Find the longest word within a string](#text00003.html__Toc68199570)

[JavaScript: Counts the number of vowels within a string](#text00004.html__Toc68199571)

[JavaScript: Check a number is prime or not](#text00005.html__Toc68199572)

[JavaScript: Get the data type](#text00006.html__Toc68199573)

[JavaScript: Find the second lowest and second greatest](#text00007.html__Toc68199574)

[JAVASCRIPT BASICS](#text00008.html__Toc68199575)

[Calculate multiplication and division](#text00008.html__Toc68199576)

[Convert temperatures](#text00009.html__Toc68199577)

[Find the largest](#text00010.html__Toc68199578)

[Reverse a given string](#text00011.html__Toc68199579)

[Replace every character](#text00012.html__Toc68199580)

[Create a new string](#text00013.html__Toc68199581)

[Concatenate two strings](#text00014.html__Toc68199582)

[Move last three character](#text00015.html__Toc68199583)

[Compute the sum](#text00016.html__Toc68199584)

[Add two digits](#text00017.html__Toc68199585)

[Check whether a given year is a leap](#text00018.html__Toc68199586)

[Check given positive number](#text00019.html__Toc68199587)

[Check a string starts with 'Java'](#text00020.html__Toc68199588)

[Check two given integer values](#text00021.html__Toc68199589)

[Find a value which is nearest to 100](#text00022.html__Toc68199590)

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