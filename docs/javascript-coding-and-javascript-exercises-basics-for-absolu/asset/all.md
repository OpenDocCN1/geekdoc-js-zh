![](Images/cover00189.jpeg)

JAVASCRIPT CODING AND JAVASCRIPT EXERCISES

BASICS FOR ABSOLUTE BEGINNERS

STEP BY STEP GUIDE TO LEARN CODING QUICKLY

J NEWMAN

[Learn JavaScript](#part0003.xhtml__Toc105334627)

[JavaScript Comment](#part0004.xhtml__Toc105334628)

[JavaScript Variable](#part0005.xhtml__Toc105334629)

[JavaScript Global Variable](#part0006.xhtml__Toc105334630)

[Javascript Data Types](#part0007.xhtml__Toc105334631)

[JavaScript Operators](#part0008.xhtml__Toc105334632)

[JavaScript If-else](#part0009.xhtml__Toc105334633)

[JavaScript Switch](#part0010.xhtml__Toc105334634)

[JavaScript Loops](#part0011.xhtml__Toc105334635)

[JavaScript Functions](#part0012.xhtml__Toc105334636)

[JavaScript Objects](#part0013.xhtml__Toc105334637)

[JavaScript Array](#part0014.xhtml__Toc105334638)

[JavaScript String](#part0015.xhtml__Toc105334639)

[JavaScript Date Object](#part0016.xhtml__Toc105334640)

[JavaScript Math](#part0017.xhtml__Toc105334641)

[JavaScript Number Object](#part0018.xhtml__Toc105334642)

[JavaScript Boolean](#part0019.xhtml__Toc105334643)

[JAVASCRIPT EXERCISES](#part0021.xhtml__Toc105334644)

[Hours and minutes](#part0021.xhtml__Toc105334645)

[Count vowels](#part0022.xhtml__Toc105334646)

[Capitalize The First Letter](#part0023.xhtml__Toc105334647)

[Concatenate two strings](#part0024.xhtml__Toc105334648)

[Create a new string](#part0025.xhtml__Toc105334649)

[First not repeated character](#part0026.xhtml__Toc105334650)

[Counts the number of vowels](#part0027.xhtml__Toc105334651)

[Find the longest word](#part0028.xhtml__Toc105334652)

[Check a number is prime](#part0029.xhtml__Toc105334653)

[Find the second lowest and second greatest](#part0030.xhtml__Toc105334654)

[JavaScript: Get the data type](#part0031.xhtml__Toc105334655)

[Add two digits](#part0032.xhtml__Toc105334656)

[Check given positive number](#part0033.xhtml__Toc105334657)

[Leap Year Check](#part0034.xhtml__Toc105334658)

[string starts with 'Java' - Check](#part0035.xhtml__Toc105334659)

[Find a value which is nearest to 100](#part0036.xhtml__Toc105334660)

[Two given integer values - Check](#part0037.xhtml__Toc105334661)

[Positive number - Check](#part0038.xhtml__Toc105334662)

[Multiplication and division](#part0039.xhtml__Toc105334663)

[String starts with 'Java' - Check](#part0040.xhtml__Toc105334664)

[Convert temperatures](#part0041.xhtml__Toc105334665)

JAVASCRIPT CODING:

BASICS FOR ABSOLUTE BEGINNERS

STEP BY STEP GUIDE TO LEARN CODING QUICKLY

# Learn JavaScript

JavaScript is a lightweight, cross-platform object-based scripting language.

JavaScript is a translated language, not a compiled language. The JavaScript Translator (which is built within the browser) is in charge of translating JavaScript code for web browsers.

JavaScript (js) is a lightweight object-oriented programming language that is used to script webpages by a number of websites.

When applied to an HTML document, it is an interpreted, full-featured programming language that enables dynamic interactivity on websites. It was first released in 1995 to allow users to add programs to webpages in the Netscape Navigator browser.

Since then, all other graphical web browsers have embraced it. Users can use JavaScript to create modern web applications that interact immediately without having to reload the page every time. Js is used on a standard website to provide many sorts of interactivity and simplicity.

JavaScript, on the other hand, has no connection to the Java programming language.

## Features of JavaScript

Because they have built-in execution environments, all popular web browsers support JavaScript.

The grammar and structure of JavaScript are based on the C programming language. As a result, it is classified as a structured programming language.

JavaScript is a weakly typed language with implicit casting of certain types (depending on the operation).

JavaScript is an object-oriented programming language that inherits through prototypes rather than classes.

It's a simple and interpretable language.

The language is case-sensitive.

JavaScript is compatible with a variety of operating systems, including Windows, macOS, and Linux.

It gives consumers complete control over their web browsers.

![](Images/image00126.jpeg)

### JavaScript Example

1.  <script>  
2.  document.write("Hello JavaScript by JavaScript");  
3.  </script>  

# JavaScript Comment

JavaScript comments are an effective means of conveying information. It's used to include code-related information, such as warnings or suggestions, so that the end user can understand it.

The JavaScript engine, which is incorporated in the browser, ignores the JavaScript comment.

#### Advantages - JavaScript comments

To make coding more understandable It can be used to explain the code so that the end user can understand it.

To avoid having to write unneeded code It can also be used to prevent the code from running. We sometimes add code to do a certain action. However, the code may need to be disabled after some time. It is preferable to utilise comments in this situation.

## JavaScript Comments - Types

1.  Single-line Comment
2.  Multi-line Comment

## Single line Comment

Double forward slashes (//) are used to indicate it. It's appropriate to use it both before and after the sentence.

Let's look at an example of a single-line comment, which is one that is placed before the statement.

1.  <script>  
2.  // It is single line comment  
3.  document.write("hello javascript");  
4.  </script>

EXAMPLE

1.  <script>  
2.  var a=10;  
3.  var b=20;  
4.  var c=a+b;//It adds values of a and b variable  
5.  document.write(c);//prints sum of 10 and 20  
6.  </script>

## Multi line Comment

It can be used to create both single and multi-line comments. As a result, it is more practical.

It's symbolised by a forward slash followed by an asterisk, then another forward slash. Consider the following scenario:

1.  /* your code here  */  

It might appear before, after, or in the middle of a statement.

1.  <script>  
2.  /* It is multi line comment.  
3.  It will not be displayed */  
4.  document.write("example of javascript multiline comment");  
5.  </script>  

# JavaScript Variable

A JavaScript variable is nothing more than a storage location's name. In JavaScript, there are two sorts of variables: local variables and global variables.

When declaring a JavaScript variable, there are some guidelines to follow (also known as identifiers).

A letter (a to z or A to Z), underscore(_), or dollar($) sign must begin the name.

We can put numerals (0 to 9) after the initial letter, for example value1.

Variables in JavaScript are case sensitive, so x and X are two separate variables.

## Correct JavaScript variables

1.  var x = 10;  
2.  var _value="sonoo";  

## Incorrect JavaScript variables

1.  var  123=30;  
2.  var *aa=320;  

## Example - JavaScript variable

1.  <script>  
2.  var x = 10;  
3.  var y = 20;  
4.  var z=x+y;  
5.  document.write(z);  
6.  </script>  

#### Output

30

## JavaScript local variable

A local variable in JavaScript is declared within a block or function. It can only be accessed from within the function or block. Consider the following scenario:

1.  <script>  
2.  function abc(){  
3.  var x=10;//local variable  
4.  }  
5.  </script>  

Or,

1.  <script>  
2.  If(10<13){  
3.  var y=20;//JavaScript local variable  
4.  }  
5.  </script>  

## JavaScript global variable

A global variable in JavaScript can be accessed from any function. A global variable is one that is declared outside of the function or with the window object. Consider the following scenario:

1.  <script>  
2.  var data=200;//gloabal variable  
3.  function a(){  
4.  document.writeln(data);  
5.  }  
6.  function b(){  
7.  document.writeln(data);  
8.  }  
9.  a();//calling JavaScript function  
10.  b();  
11.  </script>

# JavaScript Global Variable

A global variable in JavaScript is declared outside of the function or with the window object. It's possible to go to it from any function.

Let's look at a simple JavaScript example of a global variable.

1.  <script>  
2.  var value=50;//global variable  
3.  function a(){  
4.  alert(value);  
5.  }  
6.  function b(){  
7.  alert(value);  
8.  }  
9.  </script> 

### Declaring a global variable in JavaScript within a function

You must utilise the window object to declare JavaScript global variables inside a function. Consider the following scenario:

1.  window.value=90;  

It can now be declared within any function and accessed from within any function. Consider the following scenario:

1.  function m(){  
2.  window.value=100;//declaring global variable by window object  
3.  }  
4.  function n(){  
5.  alert(window.value);//accessing global variable from other function  
6.  } 

#### In JavaScript, the internals of a global variable

When you declare a variable outside of a function, it is automatically added to the window object. You can also use the window object to get to it. Consider the following scenario:

1.  var value=50;  
2.  function a(){  
3.  alert(window.value);//accessing global variable   
4.  } 

# Javascript Data Types

Different data types are available in JavaScript to hold various types of values. In JavaScript, there are two sorts of data types.

1.  Primitive data type
2.  Non-primitive (reference) data type

JavaScript is a dynamic type language, which means you don't have to specify the type of a variable because the JavaScript engine uses it dynamically. To specify the data type, you must use var. It may store any type of value, including numbers, strings, and so on. Consider the following scenario:

1.  var a=40;//holding number  
2.  var b="Rahul";//holding string  

![](Images/image00127.jpeg)

![](Images/image00128.jpeg)

# JavaScript Operators

Operators in JavaScript are symbols that perform operations on operands. Consider the following scenario:

1.  var sum=10+20;  

Here, + is the arithmetic operator

And = is the assignment operator.

Types of operators in JavaScript.

1.  Arithmetic Operators
2.  Comparison (Relational) Operators
3.  Bitwise Operators
4.  Logical Operators
5.  Assignment Operators
6.  Special Operators

## JavaScript Arithmetic Operators

To conduct arithmetic operations on the operands, arithmetic operators are employed. JavaScript arithmetic operators are the operators listed below.

![](Images/image00129.jpeg)

## JavaScript Comparison Operators

The comparison operator in JavaScript compares the two operands. The following are the comparison operators:

![](Images/image00130.jpeg)

## JavaScript Bitwise Operators

On operands, the bitwise operators perform bitwise operations. The following are the bitwise operators:

![](Images/image00131.jpeg)

## JavaScript Logical Operators

JavaScript logical operators are the operators listed below.

![](Images/image00132.jpeg)

## JavaScript Assignment Operators

![](Images/image00133.jpeg)

## JavaScript Special Operators

![](Images/image00134.jpeg)

# JavaScript If-else

![](Images/image00135.jpeg)

### JavaScript If statement

Only if expression is true does it assess the content. The if statement in JavaScript has the following signature.

1.  if(expression){  
2.  //content to be evaluated  
3.  }  

![](Images/image00136.jpeg)

EXAMPLE

1.  <script>  
2.  var a=20;  
3.  if(a>10){  
4.  document.write("value of a is greater than 10");  
5.  }  
6.  </script>

OUTPUT

value of a is greater than 10

### JavaScript If...else Statement

It determines if the condition is true or false by evaluating the content. The syntax for the if-else statement in JavaScript is shown below.

1.  if(expression){  
2.  //content to be evaluated if condition is true  
3.  }  
4.  else{  
5.  //content to be evaluated if condition is false  
6.  }  

![](Images/image00137.jpeg)

EXAMPLE

1.  <script>  
2.  var a=20;  
3.  if(a%2==0){  
4.  document.write("a is even number");  
5.  }  
6.  else{  
7.  document.write("a is odd number");  
8.  }  
9.  </script>

OUTPUT

a is even number

### If...else if statement – in Javascript

It only analyses the content if one or more expressions are true. The if else if statement in JavaScript has the following signature.

1.  if(expression1){  
2.  //content to be evaluated if expression1 is true  
3.  }  
4.  else if(expression2){  
5.  //content to be evaluated if expression2 is true  
6.  }  
7.  else if(expression3){  
8.  //content to be evaluated if expression3 is true  
9.  }  
10.  else{  
11.  //content to be evaluated if no expression is true  
12.  }  

EXAMPLE

1.  <script>  
2.  var a=20;  
3.  if(a==10){  
4.  document.write("a is equal to 10");  
5.  }  
6.  else if(a==15){  
7.  document.write("a is equal to 15");  
8.  }  
9.  else if(a==20){  
10.  document.write("a is equal to 20");  
11.  }  
12.  else{  
13.  document.write("a is not equal to 10, 15 or 20");  
14.  }  
15.  </script>  

OUTPUT

a is equal to 20

# JavaScript Switch

The JavaScript switch statement is used to combine numerous expressions into a single code. It's the same as the else if statement we learnt on the previous page. It is, however, more useful than if..else..if because it may be used with integers, characters, and other variables.

The JavaScript switch statement's signature is shown below.

1.  switch(expression){  
2.  case value1:  
3.  code to be executed;  
4.  break;  
5.  case value2:  
6.  code to be executed;  
7.  break;  
8.  ......  

10.  default:   
11.  code to be executed if above values are not matched;  
12.  }  

Simple example - switch statement - javascript.

1.  <script>  
2.  var grade='B';  
3.  var result;  
4.  switch(grade){  
5.  case 'A':  result="A Grade";  
6.  break;  
7.  case 'B':  
8.  result="B Grade";  
9.  break;  
10.  case 'C':  
11.  result="C Grade";  
12.  break;  
13.  default:  
14.  result="No Grade";  
15.  }  
16.  document.write(result);  
17.  </script>  

OUTPUT

B Grade

Behaviour of switch statement

1.  <script>  
2.  var grade='B';  
3.  var result;  
4.  switch(grade){  
5.  case 'A':  
6.  result+=" A Grade";  
7.  case 'B':  
8.  result+=" B Grade";  
9.  case 'C':  
10.  result+=" C Grade";  
11.  default:  
12.  result+=" No Grade";  
13.  }  
14.  document.write(result);  
15.  </script>  

OUTPUT

undefined B Grade C Grade No Grade

# JavaScript Loops

The for, while, do while, and for-in loops are used to iterate the piece of code in JavaScript. It reduces the size of the code. It's most commonly found in arrays.

1.  for loop
2.  while loop
3.  do-while loop
4.  for-in loop

## 1) JavaScript For loop

The loop in JavaScript iterates the components for a set number of times. If the number of iterations is known, it should be used. The for loop's syntax is seen below.

1.  for (initialization; condition; increment)  
2.  {  
3.  code to be executed  
4.  }  

EXAMPLE

1.  <script>  
2.  for (i=1; i<=5; i++)  
3.  {  
4.  document.write(i + "<br/>")  
5.  }  
6.  </script>  

Output:

1
2
3
4
5

## 2) JavaScript while loop

The while loop in JavaScript iterates the components an infinite amount of times. If the number of iterations is unknown, it should be utilised. The while loop's syntax is seen below.

1.  while (condition)  
2.  {  
3.  code to be executed  
4.  }  

EXAMPLE

1.  <script>  
2.  var i=11;  
3.  while (i<=15)  
4.  {  
5.  document.write(i + "<br/>");  
6.  i++;  
7.  }  
8.  </script>

Output:

11
12
13
14
15

## 3) Do while loop

The JavaScript do while loop, like the while loop, iterates the elements indefinitely. Regardless of whether the condition is true or false, the code is performed at least once. The following is the syntax for the do while loop.

1.  do{  
2.  code to be executed  
3.  }while (condition);  

EXAMPLE

1.  <script>  
2.  var i=21;  
3.  do{  
4.  document.write(i + "<br/>");  
5.  i++;  
6.  }while (i<=25);  
7.  </script>  

Output:

21
22
23
24
25

## 4) JavaScript for in loop

The JavaScript for in loop is used to cycle through an object's properties.

# JavaScript Functions

To conduct operations, JavaScript functions are needed. To reuse the code, we can call the JavaScript function many times.

Benefits of Using JavaScript

JavaScript functions have primarily two advantages.

Reusability of code: Because we can call a function multiple times, we can save time coding.

Less coding means our program is more compact. To accomplish a common task, we don't need to write many lines of code each time.

## JavaScript Function Syntax

1.  function functionName([arg1, arg2, ...argN]){  
2.  //code to be executed  
3.  }  

EXAMPLE

1.  <script>  
2.  function msg(){  
3.  alert("hello! this is message");  
4.  }  
5.  </script>  
6.  <input type="button" onclick="msg()" value="call function"/>

## JavaScript Function Arguments

1.  <script>  
2.  function getcube(number){  
3.  alert(number*number*number);  
4.  }  
5.  </script>  
6.  <form>  
7.  <input type="button" value="click" onclick="getcube(4)"/>  
8.  </form>  

## Function with Return Value

We can use a function that returns a value in our program by calling it. Let's look at a function that returns a value as an example.

1.  <script>  
2.  function getInfo(){  
3.  return "hello javatpoint! How r u?";  
4.  }  
5.  </script>  
6.  <script>  
7.  document.write(getInfo());  
8.  </script>

OUTPUT

hello javatpoint! How r u?

## JavaScript Function Object

The Function function Object() { [native code] } in JavaScript is used to generate a new Function object. It runs the code on a global scale. When we call the function Object() { [native code] } directly, however, a function is constructed dynamically but insecurely.

## Syntax

1.  new Function ([arg1[, arg2[, ....argn]],] functionBody)  

![](Images/image00138.jpeg)

![](Images/image00139.jpeg)

## JavaScript Function Object

## Example

1.  <script>  
2.  var add=new Function("num1","num2","return num1+num2");  
3.  document.writeln(add(2,5));  
4.  </script>  

Output:

7

### Example 2

1.  <script>  
2.  var pow=new Function("num1","num2","return Math.pow(num1,num2)");  
3.  document.writeln(pow(2,3));  
4.  </script>

Output:

8

# JavaScript Objects

A javaScript object is a state and behavior-based entity (properties and method). For example, a car, a pen, a bicycle, a chair, a glass, a keyboard, and a monitor.

JavaScript is an object-oriented programming language. In JavaScript, everything is an object.

JavaScript is a template-based language, not a class-based one. To get the object, we don't need to build a class. However, we direct the creation of objects.

![](Images/image00140.jpeg)

![](Images/image00141.jpeg)

EXAMPLE

1.  <script>  
2.  emp={id:102,name:"Shyam Kumar",salary:40000}  
3.  document.write(emp.id+" "+emp.name+" "+emp.salary);  
4.  </script> 

OUTPUT

102 Shyam Kumar 40000

![](Images/image00142.jpeg)

EXAMPLE

1.  <script>  
2.  var emp=new Object();  
3.  emp.id=101;  
4.  emp.name="Ravi Malik";  
5.  emp.salary=50000;  
6.  document.write(emp.id+" "+emp.name+" "+emp.salary);  
7.  </script>  

OUTPUT

101 Ravi 50000

![](Images/image00143.jpeg)

EXAMPLE

1.  <script>  
2.  function emp(id,name,salary){  
3.  this.id=id;  
4.  this.name=name;  
5.  this.salary=salary;  
6.  }  
7.  e=new emp(103,"Vimal Jaiswal",30000);  

9.  document.write(e.id+" "+e.name+" "+e.salary);  
10.  </script>  

OUTPUT

103 Vimal Jaiswal 30000

## Defining method - JavaScript Object

In a JavaScript object, we can specify methods. However, before we define the method, we must add a property to the function with the same name as the method.

EXAMPLE

1.  <script>  
2.  function emp(id,name,salary){  
3.  this.id=id;  
4.  this.name=name;  
5.  this.salary=salary;  

7.  this.changeSalary=changeSalary;  
8.  function changeSalary(otherSalary){  
9.  this.salary=otherSalary;  
10.  }  
11.  }  
12.  e=new emp(103,"Sonoo Jaiswal",30000);  
13.  document.write(e.id+" "+e.name+" "+e.salary);  
14.  e.changeSalary(45000);  
15.  document.write("<br>"+e.id+" "+e.name+" "+e.salary);  
16.  </script>

OUTPUT

103 Sonoo Jaiswal 30000
103 Sonoo Jaiswal 45000

## JavaScript Object Methods

![](Images/image00144.jpeg)

![](Images/image00145.jpeg)

![](Images/image00146.jpeg)

![](Images/image00147.jpeg)

# JavaScript Array

A JavaScript array is an object that represents a group of objects of the same type.

In JavaScript, there are three ways to create an array.

1.  By array literal
2.  By creating instance of Array directly (using new keyword)
3.  By using an Array constructor (using new keyword)

## 1) JavaScript array literal

The following is the syntax for generating an array with an array literal:

1.  var arrayname=[value1,value2.....valueN];  

Values are contained within [] and separated by, as you can see (comma).

Let's have a look at a simple example of how to create and use an array in JavaScript.

1.  <script>  
2.  var emp=["Sonoo","Vimal","Ratan"];  
3.  for (i=0;i<emp.length;i++){  
4.  document.write(emp[i] + "<br/>");  
5.  }  
6.  </script>

Output

Sonoo
Vimal
Ratan

## 2) JavaScript Array directly 

The following is the syntax for directly creating an array:

1.  var arrayname=new Array();  

In this case, the new keyword is used to create an array object.

Let's look at an example of generating an array from scratch.

1.  <script>  
2.  var i;  
3.  var emp = new Array();  
4.  emp[0] = "Arun";  
5.  emp[1] = "Varun";  
6.  emp[2] = "John";  

8.  for (i=0;i<emp.length;i++){  
9.  document.write(emp[i] + "<br>");  
10.  }  
11.  </script>  

Output

Arun
Varun
John

## 3) JavaScript array constructor

So that we don't have to provide value explicitly, you must create an instance of array by passing arguments to the function Object() { [native code] }.

The following is an example of using the array function Object() { [native code] } to create an object.

1.  <script>  
2.  var emp=new Array("Jai","Vijay","Smith");  
3.  for (i=0;i<emp.length;i++){  
4.  document.write(emp[i] + "<br>");  
5.  }  
6.  </script> 

Output

Jai
Vijay
Smith

## JavaScript Array Methods

![](Images/image00148.jpeg)

![](Images/image00149.jpeg)

![](Images/image00150.jpeg)

![](Images/image00151.jpeg)

![](Images/image00152.jpeg)

# JavaScript String

A string in JavaScript is an object that represents a string of characters.

In JavaScript, there are two ways to make a string.

1.  By string literal
2.  By string object (using new keyword)

## 1) By string literal

Double quotations are used to construct the string literal. The following is the syntax for creating a string using a string literal:

1.  var stringname="string value";  

EXAMPLE

1.  <script>  
2.  var str="This is string literal";  
3.  document.write(str);  
4.  </script> 

Output:

This is string literal

## 2) By string object (using new keyword)

The following is the syntax for creating a string object with the new keyword:

1.  var stringname=new String("string literal");  

The new keyword is used to create a string instance.

Let's look at an example of using the new keyword in JavaScript to create a string.

1.  <script>  
2.  var stringname=new String("hello javascript string");  
3.  document.write(stringname);  
4.  </script>

OUTPUT

hello javascript string

## JavaScript String Methods

![](Images/image00153.jpeg)

![](Images/image00154.jpeg)

![](Images/image00155.jpeg)

# JavaScript Date Object

You may get the year, month, and day using the JavaScript date object. The JavaScript date object can be used to display a timer on a webpage.

To generate a date object, you can use a variety of Date constructors. It has methods for retrieving and setting the day, month, year, hour, minute, and second.

## Constructor

4 variant of Date constructor

1.  Date()
2.  Date(milliseconds)
3.  Date(dateString)
4.  Date(year, month, day, hours, minutes, seconds, milliseconds)

## JavaScript Date Methods

![](Images/image00156.jpeg)

![](Images/image00157.jpeg)

![](Images/image00158.jpeg)

![](Images/image00159.jpeg)

![](Images/image00160.jpeg)

### JavaScript Date Example

1.  Current Date and Time: <span id="txt"></span>  
2.  <script>  
3.  var today=new Date();  
4.  document.getElementById('txt').innerHTML=today;  
5.  </script>

OUTPUT

Current Date and Time: Sat Feb 12 2022 23:47:52 GMT+0530 (India Standard Time)

EXAMPLE 2

1.  <script>  
2.  var date=new Date();  
3.  var day=date.getDate();  
4.  var month=date.getMonth()+1;  
5.  var year=date.getFullYear();  
6.  document.write("<br>Date is: "+day+"/"+month+"/"+year);  
7.  </script>

### JavaScript Current Time Example

1.  Current Time: <span id="txt"></span>  
2.  <script>  
3.  var today=new Date();  
4.  var h=today.getHours();  
5.  var m=today.getMinutes();  
6.  var s=today.getSeconds();  
7.  document.getElementById('txt').innerHTML=h+":"+m+":"+s;  
8.  </script>

### Digital Clock Example

Let's look at a simple example of using the JavaScript date object to display a digital clock.

In JavaScript, you can specify interval using the setTimeout() or setInterval() methods.

EXAMPLE

1.  Current Time: <span id="txt"></span>  
2.  <script>  
3.  window.onload=function(){getTime();}  
4.  function getTime(){  
5.  var today=new Date();  
6.  var h=today.getHours();  
7.  var m=today.getMinutes();  
8.  var s=today.getSeconds();  
9.  // add a zero in front of numbers<10  
10.  m=checkTime(m);  
11.  s=checkTime(s);  
12.  document.getElementById('txt').innerHTML=h+":"+m+":"+s;  
13.  setTimeout(function(){getTime()},1000);  
14.  }  
15.  //setInterval("getTime()",1000);//another way  
16.  function checkTime(i){  
17.  if (i<10){  
18.  i="0" + i;  
19.  }  
20.  return i;  
21.  }  
22.  </script>  

# JavaScript Math

To conduct mathematical operations, the JavaScript math object exposes various constants and methods. It does not have constructors, unlike the date object.

## JavaScript Math Methods

![](Images/image00161.jpeg)

![](Images/image00162.jpeg)

![](Images/image00163.jpeg)

## Math.sqrt(n)

The square root of a number is returned by the JavaScript math.sqrt(n) method.

1.  Square Root of 17 is: <span id="p1"></span>    
2.  <script>    
3.  document.getElementById('p1').innerHTML=Math.sqrt(17);    
4.  </script>  

Output:

Square Root of 17 is: 4.123105625617661

## Math.random()

The math.random() method in JavaScript returns a random number between 0 and 1.

1.  Random Number is: <span id="p2"></span>    
2.  <script>    
3.  document.getElementById('p2').innerHTML=Math.random();    
4.  </script> 

Output:

Random Number is: 0.02157876559753591

## Math.pow(m,n)

1.  3 to the power of 4 is: <span id="p3"></span>    
2.  <script>    
3.  document.getElementById('p3').innerHTML=Math.pow(3,4);    
4.  </script>

Output:

3 to the power of 4 is: 81

## Math.floor(n)

The JavaScript math.floor(n) method returns the number's lowest integer. For instance, 3 for 3.7, 5 for 5.9, and so on.

1.  Floor of 4.6 is: <span id="p4"></span>    
2.  <script>    
3.  document.getElementById('p4').innerHTML=Math.floor(4.6);    
4.  </script>  

Output:

Floor of 4.6 is: 4

## Math.ceil(n)

The math.ceil(n) method in JavaScript returns the largest integer for a given value. For instance, 4 for 3.7, 6 for 5.9, and so on.

1.  Ceil of 4.6 is: <span id="p5"></span>    
2.  <script>    
3.  document.getElementById('p5').innerHTML=Math.ceil(4.6);    
4.  </script> 

Output:

Ceil of 4.6 is: 5

## Math.round(n)

The math in JavaScript. The round(n) method gives the nearest rounded integer for a supplied number. If the fractional component is equal to or higher than 0.5, it is assigned to the upper value 1; otherwise, it is assigned to the lower value 0\. For instance, 4 for 3.7, 3 for 3.3, 6 for 5.9, and so on.

1.  Round of 4.3 is: <span id="p6"></span><br>    
2.  Round of 4.7 is: <span id="p7"></span>    
3.  <script>    
4.  document.getElementById('p6').innerHTML=Math.round(4.3);   
5.  document.getElementById('p7').innerHTML=Math.round(4.7);    
6.  </script>   

Output:

Round of 4.3 is: 4
Round of 4.7 is: 5

# JavaScript Number Object

You can represent a numeric value with the JavaScript number object. It could be either an integer or a floating-point number. The IEEE standard for representing floating-point numbers is followed by the JavaScript number object.

In JavaScript, you can make a number object with the Number() function Object() { [native code] }. Consider the following scenario:

1.  var n=new Number(value);  

If the value cannot be converted to a number, it returns NaN (Not a Number), which the isNaN() method can validate.

You can also assign a number directly to a variable. Consider the following scenario:

1.  var x=102;//integer value  
2.  var y=102.7;//floating point value  
3.  var z=13e4;//exponent value, output: 130000  
4.  var n=new Number(16);//integer value by number object  

Output:

102 102.7 130000 16

## JavaScript Number Constants

![](Images/image00164.jpeg)

## JavaScript Number Methods

![](Images/image00165.jpeg)

# JavaScript Boolean

A Boolean object in JavaScript represents a value in one of two states: true or false. The Boolean() function Object() { [native code] } in JavaScript can be used to build a JavaScript Boolean object, as seen below.

1.  Boolean b=new Boolean(value);  

## JavaScript Boolean Example

1.  <script>  
2.  document.write(10<20);//true  
3.  document.write(10<5);//false  
4.  </script>

## Boolean Properties

![](Images/image00166.jpeg)

## Boolean Methods

![](Images/image00167.jpeg)

JAVASCRIPT CODING

EXERCISES:

BASICS FOR ABSOLUTE BEGINNERS

GUIDE FOR EXAMS AND INTERVIEWS

J NEWMAN

# JAVASCRIPT EXERCISES

# Hours and minutes

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00168.jpeg) 

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

#####  ![](Images/image00169.jpeg)

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

### ![](Images/image00170.jpeg)

### OUTPUT

![](Images/image00171.jpeg)

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

 ![](Images/image00172.jpeg)

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

## ![](Images/image00173.jpeg)

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

### ![](Images/image00174.jpeg)

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

![](Images/image00175.jpeg)

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

![](Images/image00176.jpeg)

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

![](Images/image00177.jpeg)

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

## ![](Images/image00178.jpeg)

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

#####  ![](Images/image00179.jpeg)

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

### ![](Images/image00180.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00181.jpeg)

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

### ![](Images/image00182.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00183.jpeg)

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

##### ![](Images/image00184.jpeg)

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

![](Images/image00185.jpeg)

# String starts with 'Java' - Check

## And false otherwise

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00186.jpeg) 

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

### ![](Images/image00187.jpeg)

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

![](Images/image00188.jpeg)