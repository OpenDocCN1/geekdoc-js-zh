![](Images/cover00079.jpeg)

JAVASCRIPT CODING

EXERCISES:

BASICS FOR ABSOLUTE BEGINNERS

GUIDE FOR EXAMS AND INTERVIEWS

J NEWMAN

[Hours and minutes](#part0002.xhtml__Toc101357762)

[Count vowels](#part0003.xhtml__Toc101357763)

[Capitalize The First Letter](#part0004.xhtml__Toc101357764)

[Concatenate two strings](#part0005.xhtml__Toc101357765)

[Create a new string](#part0006.xhtml__Toc101357766)

[First not repeated character](#part0007.xhtml__Toc101357767)

[Counts the number of vowels](#part0008.xhtml__Toc101357768)

[Find the longest word](#part0009.xhtml__Toc101357769)

[Check a number is prime](#part0010.xhtml__Toc101357770)

[Find the second lowest and second greatest](#part0011.xhtml__Toc101357771)

[JavaScript: Get the data type](#part0012.xhtml__Toc101357772)

[Add two digits](#part0013.xhtml__Toc101357773)

[Check given positive number](#part0014.xhtml__Toc101357774)

[Leap Year Check](#part0015.xhtml__Toc101357775)

[string starts with 'Java' - Check](#part0016.xhtml__Toc101357776)

[Find a value which is nearest to 100](#part0017.xhtml__Toc101357777)

[Two given integer values - Check](#part0018.xhtml__Toc101357778)

[Positive number - Check](#part0019.xhtml__Toc101357779)

[Multiplication and division](#part0020.xhtml__Toc101357780)

[String starts with 'Java' - Check](#part0021.xhtml__Toc101357781)

[Convert temperatures](#part0022.xhtml__Toc101357782)

# Hours and minutes

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00058.jpeg) 

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function time_convert(num)

##### {

#####   var hours = Math.floor(num / 60); 

#####   var minutes = num % 60;

#####   return hours + ":" + minutes;        

##### }

##### console.log(time_convert(71));

##### console.log(time_convert(450));

##### console.log(time_convert(1441));

### OUTPUT

1:11

7:30

24:1

# Count vowels

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to count the number of vowels in a given string.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function vowel_Count(str)

##### {

#####   return str.replace(/[^aeiou]/g, "").length;

##### }

##### console.log(vowel_Count("Python"));

##### console.log(vowel_Count("htmlresource.com"));

### Output:

1

5

# Capitalize The First Letter

## Of Each Word

### Of A Given String

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00059.jpeg)

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function capital_letter(str)

##### {

#####     str = str.split(" ");

#####     for (var i = 0, x = str.length; i < x; i++) {

#####         str[i] = str[i][0].toUpperCase() + str[i].substr(1);

#####     }

#####     return str.join(" ");

##### }

### ![](Images/image00060.jpeg)

### OUTPUT

![](Images/image00061.jpeg)

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

# Create a new string 

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

 ![](Images/image00062.jpeg)

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

# First not repeated character

## ![](Images/image00063.jpeg)

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

# Counts the number of vowels

## within a string

### ![](Images/image00064.jpeg)

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

# Find the longest word

## within a string

![](Images/image00065.jpeg)

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

# Check a number is prime

![](Images/image00066.jpeg)

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

# Find the second lowest and second greatest

## numbers from an array

![](Images/image00067.jpeg)

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

# JavaScript: Get the data type

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

# Check given positive number

## ![](Images/image00068.jpeg)

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

# Leap Year Check

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

# string starts with 'Java' - Check

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

# Find a value which is nearest to 100

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00069.jpeg)

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

# Two given integer values - Check

### ![](Images/image00070.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00071.jpeg)

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

# Positive number - Check

### ![](Images/image00072.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00073.jpeg)

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

# Multiplication and division

## of two numbers

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### ![](Images/image00074.jpeg)

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

#### OUTPUT

![](Images/image00075.jpeg)

# String starts with 'Java' - Check

## And false otherwise

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00076.jpeg) 

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

# Convert temperatures

### ![](Images/image00077.jpeg)

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

![](Images/image00078.jpeg)