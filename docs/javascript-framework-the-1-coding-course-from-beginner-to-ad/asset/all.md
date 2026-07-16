![](cover.jpeg)

JAVASCRIPT

FRAMEWORK

In This Book You Will Learn Explanation with Diagramme and

Working Exercises with Successfull Execution of Exercises and Output

Readymade Solution With Step By Step Explanation      

AMIT K

Contents

Beginners Guide to Learn Javascript Programming Step by Step

Introduction

Chapter 1 : Introduction

Introduction

Chapter 2 : Bitwise Operations

Bitwise

Bitwise operation on numbers

What is Bitwise used for

Chapter 3 : JavaScript Arrays

JavaScript Arrays

Chapter 4 : JavaScript Loops

Overview of the loops

while loop

for loop

For .. in loop

For .. of loop

do...while loop

Use the break statement in the loop

Use the continue statement in the loop

Labelled Loop

Chapter 5 : JavaScript Functions

What is Function

Function with default parameter

Varargs parameter

Anonymous Function

Function Constructor

Generator Function

Chapter 6 : JavaScript Number

JavaScript Number

Chapter 7 : JavaScript Boolean

JavaScript Boolean

Chapter 8 : JavaScript Strings

JavaScript Strings

Chapter 9 : JavaScript if else Statement

if statment

if - else statement

if - else if - else statement

Operators involved in conditional expression

Chapter 10 : JavaScript Switch Statement

The structure of switch statement

switch Example

break statement in switch

Chapter 11 : JavaScript Error Handling

1  What is Error

2  Handling error with try-catch

3  try-catch-finally

4  Built-in Errors

5  Throw Error

6  The properties of Error

7  Re-throw Error

8  Exceptions when catching errors

Chapter 12 : JavaScript Form Validation

1  Form Validation

2  Simple example

3  Access the form data

4  Submit through Javascript

5  Validate automatically

Chapter 13 : JavaScript Web Cookies

1  What is Web Cookie

2  Where is Cookie stored

3  See Cookie on browser

4  ECMAScript Cookie

Chapter 14 : JavaScript void Keyword

1  Void Keyword

2  Void and JavaScript URIs

3  One-time use function

Chapter 15 : Classes and Objects

1  Your First Class

2  Getter & Setter

3  Static Field

4  Static method

5  Object Comparison operators

Chapter 16 : Class and inheritance

1  Class in Javascript

2  Class and inheritance in ES3

3  Class and Inheritance in ES5      

Chapter 17 : Inheritance and polymorphism

1  Inheritance in ECMAScript

2  Override method

3  Abstract Method

4  Operators - instanceof, typeof

5  Polymorphism with function

Chapter 18 : JavaScript Set Collection

1  Collections - Set

2  The methods of Set

3  WeakSet

Chapter 19 : JavaScript Map Collection

1  Collections - Map

2  Map Methods

3  WeakMap

Chapter 20 : Undertanding JavaScript Iterables and Iterators

1  Iteration

2  Concept of Iterator

3  Concept of Iterable

Chapter 21 : Javascript Menubar

1  window.menubar

Chapter 22 : JavaScript JSON

1  What is JSON

2  JSON.parse(..)

3  JSON.stringify(..)

Chapter 23 : JavaScript Event Handling

1  Javascript Events

2  Example with events

Chapter 24 : Javascript MouseEvent

1  MouseEvent

2  Properties & Methods

Chapter 25 : Javascript WheelEvent

1  WheelEvent

Chapter 26 : Javascript KeyboardEvent

1  KeyboardEvent

2  Properties & Methods

3  Table: Key, KeyCode

Chapter 27 : Javascript FocusEvent

1  FocusEvent

2  focus in, focusout

Chapter 28 : Javascript InputEvent

1  InputEvent

2  Properties, Methods

Chapter 29 : Javascript ChangeEvent

1  ChangeEvent

Chapter 30 : Javascript DragEvent

1  DragEvent

Chapter 31 : Javascript HashChangeEvent

1  HashChangeEvent

Chapter 32 : Javascript URL Encoding

1  Javascript URL Encoding

2  encodeURI(), decodeURI()

3  encodeURIComponent(), decodeURIComponent()

4  Encode all characters

Chapter 33 : Javascript FileReader

1  FileReader

2  Example with FileReader

Introduction

Learning Javascript step by step.

A developer's resource to learning one of the most-used scripting languages

JavaScript Beginners saves you shelf space by offering a complete introduction to JavaScript and how it's used in the real world.

This book serves up JavaScript coding basics before diving into the libraries, frameworks, and runtime environments new and experienced coders need to know. Start by learning the basics of JavaScript—anyone can do it, even if you've never written code before. Then go into the details of today's hottest frameworks—React.js, Vue.js, Svelte, and Node.js. Cozy up and learn some JavaScript!

*   Learn the basics of web and application development with the JavaScript language
*   Work with React, Vue, Svelte, Node.js, and the real-world tools that professionals use
*   Gain a highly marketable skill, with one of the most popular coding languages
*   Launch or further your career as a coder with easy-to-follow instruction

This book will guide for future and current coders who need an all-inclusive guide JavaScript.

Chapter 1 :

Introduction

Javascript Engine, JScript Engine

Javascript Engine means a program that reads JavaScript code snippets written and executed by the programmers.

They are also often known as Javascript Interpreter. This program is included in the browser like Firefox, Chrome, ...

Most browsers use Javascript Engine. Only IE  (Internet Explorer) uses JScript Engine.

Javascript

Javascript is a programming language. Javascript code snippets embedded in HTML help the website be able to interact with users.   

Write Javascript in HTMLThe

Javascript code can be written inside HTML, specifically it is written inside the <script></script> tag:

| ![](OEBPS/image_rsrc8P8.jpg) |

The <script> tags can be placed into the <head> tag or into the <body> tag. First of all, let's look at a simple following example:

Create a helloworld.html file with the content:

helloworld.html

| <!DOCTYPE html><html><head><title>Hello Javascript</title><script type = "text/javascript">function sayHello()  {alert("Hello Everyone!");}</script></head><body><button onclick="sayHello()">Click me!</button></body></html> |

In the <script></script> tag, I create the sayHello() function. When the user clicks Button, the sayHello() function is called, and it displays a dialog with "Hello Everyone!" content.

Don't worry if you don't know what the function is, temporarily ignore that.

| ![](OEBPS/image_rsrc8P9.jpg) |

Write Javascript in a separate fileThe

Write Javascript code in a separate file, and then HTML will import this file to use.

This is the way that helps you manage your Javascript code better, and Javascript file can be shared for many HTML files.

Javascript code is written in a file with extension such as js. The HTML files will import the aforesaid Javascript file to use.

| ![](OEBPS/image_rsrc8PA.jpg) |

Alert, Confirm, Prompt Dialog Box in Javascript

1  Javascript Dialog Box

2  Alert Dialog Box

3  Confirmation Dialog Box

4  Prompt Dialog BoxThe

1  Javascript Dialog Box

Javascript Javascript provides three important Dialog Boxes, which include Alert Dialog Box for users, Confirmation DialogBox, and Prompt Dialog Box.

2  Alert Dialog Box

Alert Dialog Box is mainly used to display a notice, warning, or error to users.

Basically, you cannot customize dialog box icon or title, ... you can only provide the message that the dialog box will display. In addition, Alert Dialog Box has only one OK button to close a dialog box.

| ![](OEBPS/image_rsrc8PB.jpg) |

| ![](OEBPS/image_rsrc8PC.jpg) |

To display a Alert Dialog Box, you call the alert(message) function, in which the message is the content that the dialog box will display.

alert-example.js

| <!DOCTYPE html><html><head><title>Alert Dialog Box</title><script type="text/javascript">function testAlertDialog()  {alert("Something Error!");}</script></head><body><h2>Alert Dialog Box</h2><button onclick="testAlertDialog()">Click me!</button></body></html> |

| ![](OEBPS/image_rsrc8PD.jpg) |

3  Confirmation Dialog Box

Confirmation Dialog Box is used to ask the user to confirm something. This dialog is very simple, you cannot customize the icon or the title of the dialog box, you can only provide a message asking the user to confirm. This dialog box has 2 OK and Cancel buttons.

| ![](OEBPS/image_rsrc8PE.jpg) |

To display a Confirmation Dialog Box you call the confirm(message) function, in which the message is one requesting an user to confirm. If the user clicks the OK button, this function returns true, otherwise if the user clicks the No button, this function returns false.

| ![](OEBPS/image_rsrc8PF.jpg) |

| ![](OEBPS/image_rsrc8PE.jpg) |

| ![](OEBPS/image_rsrc8PG.jpg) |

confirm-example.js

| <!DOCTYPE html><html><head><title>Confirmation Dialog Box</title><script type="text/javascript">function testConfirmDialog()  {var result = confirm("Do you wantto continue?");if(result)  {alert("OK Next lesson!");} else {alert("Bye!");}}</script></head><body><h2>Confirmation Dialog Box</h2><button onclick="testConfirmDialog()">Click me!</button></body></html> |

| ![](OEBPS/image_rsrc8PH.jpg) |

4  Prompt Dialog BoxThe

Prompt Dialog Box is used for users to enter an information. This dialog box is very simple. It includes a Text Field for users to enter information. The dialog box has 2 OK and Cancel buttons.

To display a Prompt Dialog Box you call the prompt(message, defaultValue) function in which the message is one for user. defaultValue is default value prefilled in the Text Field.

If an user clicks OK, the function returns contents on Text Field, otherwise, if the user clicks Cancel, the function returns null.

prompt-example.js

| <!DOCTYPE html><html><head><title>Prompt Dialog Box</title><script type="text/javascript">function testPromptDialog()  {var result = prompt("Enter youage:", "20");if(result != null)  {alert("Your age is " + result);}}</script></head><body><h2>Prompt Dialog Box</h2><button onclick="testPromptDialog()">Click me!</button></body></html> |

| ![](OEBPS/image_rsrc8PJ.jpg) |

JavaScript Variables

What is Variable

A variable means a "Memory location" which a program uses to store values. Variable name is called an identifier.

Variable name has to be given by a principle. Below are principles to give a name for a variable:

*   Variable names are not allowed to be the same as keywords
*   Variable names may contain alphabets or numbers but not start with a number.
*   Variable names may not contain white spaces or special characters except for underscore (_) and dolar character ($).

Declare variable

Declaring variable is necessary because you have to do so before using it.

| // Declare variables:var a1;console.log(a1); // undefinedvar a2 = 100;console.log(a2); // 100var a3, a4;var a5, a6 = 200;console.log(a5); // undefinedconsole.log(a6); // 200var a7= 100, a8 = 300;let b1;console.log(b1); // undefinedlet b2 = "Hello";console.log(b2); // Helloconst c = 100;console.log(c); // 100 |

block

A block means a set of commands located in a "curly brackets" {}.

let

The let keyword is used to declare a block scope variable, which means that this variable will be realized by the program in such block or inside the sub-block, but is not realized by the program outside the block defining it.

| if(true) {let a = 200;console.log(a); // 200}  // Program will ignore this statement:console.log(a); |

If you use the let keyword to define two variables with the same name, one variable declared in the parent block, one variable declared in the sub-block, the program will treat it as two different variables.

| let i = 1000;let j = 2000;if(true)  {i = 100; // Assign new value to 'i'let j = 200; // A new variable (***)console.log("Test1: " + i + " : " + j); //Test1: 100 : 200}console.log("Test2: "+ i + " : " + j); //Test2: 100 : 2000 |

var

The var keyword is used to declare a variable, which has a broader scope than the let variable. It is realized by the program inside the block defining it, in sub-blocks, even realized outside the block having declared it.

| if(true) {var a = 200;console.log(a); // 200}   console.log(a); // 200 |

If you declare two variables with the same name with the var keyword, a variable declared in the parent block, a variable in the sub-block, the program considers the two variables to be the same (Same position in memory).

| var i = 1000;var j = 2000;if(true)  {i = 100; // Assign new valuevar j = 200; // Assign new valueconsole.log("Test1: " + i + " : " + j); //Test1: 100 : 200}console.log("Test2: "+ i + " : " + j); //Test2: 100 : 200 |

The variables declared with the var keyword in a function will only be recognized by the program in such function. It is not recognized outside the function.

| // A functionvar test = function()  {var a = 200;console.log(a); // 200}// Call function.test();console.log(a); // Not work!! |

const

The const keyword is used to declare a constant. When declaring a constant, you have to always assign a value to it. But you can not assign a new value to this variable. Note: Like the let variable, the const variable has a block scope.

| // Declare a constant with a valueconst greeting = "Hello";// Assign new value to 'greeting'greeting = "Hi"; // ==> Error!!// Declare a constant without a valueconst i  ; // ==> Error!! |

A variable declared with the const keyword, it will be a constant in the sense that you can not assign a new value to it, but it is not immutable, you can still change its properties.

Chapter 2 :

Bitwise Operations

1  Bitwise

2  Bitwise operation on numbers

3  What is Bitwise used for

1  Bitwise

In digital computer programming. The bitwise operation works on one or more binary numerals, or binary numerals-like strings.

This is a simple and fast operation, directly supported by processor. Normally, bitwise operations are much faster than multiplication, division, sometimes significantly faster than addition. bitwise calculations use less energy because it rarely uses resources.

There are 7 bitwise operations :

| Operator | Name | Description |
| & | AND | If both bits are 1, the return value is 1, otherwise it returns 0. |
| &#124; | OR | If one of two bits is 1, the return value is 1, otherwise it returns 0. |
| ^ | XOR | If 2 bits are different, the return value is 1, otherwise it returns 0. |
| ~ | NOT | Inverts all the bits, 0 to 1 and 1 to 0. |
| << | Zero fill left shift | Shifts all bits to the left. |
| >> | Signed right shift | Shifts all bits to the right except the first bit. |
| >>> | Zero fill right shift | Shifts all bits to the right. |

Bitwise AND

When a bitwise AND is performed on a pair of bits, it returns 1 if both bits are 1, otherwise returns 0.

Bitwise OR:

When a bitwise OR is performed on a pair of bits, it returns 1 if one of the bits are 1, otherwise returns 0.

Bitwise XOR

When a bitwise XOR is performed on a pair of bits, it returns 1 if the bits are different, otherwise returns 0.

Bitwise NOT

When a Bitwise NOT is used, it will reverse all bits, 1 to 0, and 0 to 1.

2  Bitwise operation on numbers

Different languages can have multiple data types to represent numbers.

*   Java: byte, short, int, long, double.
*   C#:byte, sbyte, short, ushort, int, uint, long, ulong, float, double
*   Javascript: double
*   .....

Javascript stores numbers as 64 bits floating point numbers. But bitwise operations are performed on 32-bit integers. Other languages such as Java, C#,.. bitwise operations are also performed on 32-bit integers.

Therefore, before carrying out the bitwise operations with numbers, you have to convert each number into a sequence of 32 binary numbers.

Note: Of 32 bits, the first bit is used to determine the sign of number. If this bit is 1, it corresponds to the ( - ) sign. If this bit is 0 , it corresponds to the ( + ) sign

| ![](OEBPS/image_rsrc8PK.jpg) |

Bitwise Left Shift (<<)

The Bitwise Left Shift ( << ) Operator can change the sign of number.

| ![](OEBPS/image_rsrc8PM.jpg) |

Bitwise Right Shift (>>) [Unsigned Right Shift]

The Bitwise Right Shift ( >> ) operator doesn't change the sign of number because the first bit is not moved.

| ![](OEBPS/image_rsrc8PN.jpg) |

Bitwise Right Shift (>>>) [Zero fill right Shift]

The Bitwise Right Shift ( >>> ) operator can change the number sign.

| ![](OEBPS/image_rsrc8PP.jpg) |

3  What is Bitwise used for

The bitwise calculations are directly supported by the computer processor, it performs very fast. Below, I list some examples of using these calculations.

Use the bitwise operations on Strings (characters) in the Java, C#, C/C++ ...languages. Note: some languages such as Javascript don't support the bitwise operation with String type.

Convert an Uppercase into Lowercase:

| // Rule: x &#124; ' '('A' &#124; ' ') ==> 'a'('B' &#124; ' ') ==> 'b'('a' &#124; ' ') => 'a' |

Convert Lowercase into Uppercase:

| // Rule: x & '_'('a' & '_') ==> 'A'('b' & '_') ==> 'B'('A' & '_') ==> 'A' |

Chapter 3 :

JavaScript Arrays

1  What is Array

An array is a collection of consecutive positions in memory to store data. Each memory position is called an element.

| ![](OEBPS/image_rsrc8PR.jpg) |

Below are array characteristics:

*   Elements are indexed (0, 1, 2,..) starting by 0, and you can can access an element by its index.
*   Arrays are also like variables. You must declare it before using it.
*   You can update or edit the value of an element in an array.

Why is an array necessary

Instead of declaring an array with N elements, you can declare N variables, but it has the following weakpoints:

*   If N is a large number, it is not feasible to declare N variables manually
*   When you declare N variables, the program doesn't manage the order of variables for you because there is no concept of index for variables.

2  Declare array

Like variables, you have to declare an array before using it.

Syntax

| // Declarationvar myArray;// InitializationmyArray = [val1, val2, .., valN] // Orvar myArray = [val1,val2, .., valN] |

| ![](OEBPS/image_rsrc8PS.jpg) |

array-example1.js

| var myArray = [ 4, 8, 13, 6, 55, 41, 42, 99, 1 ];console.log("Length of myArray: " + myArray.length); // 9 Elementsconsole.log("Element at index 0: " + myArray[0]); // 4console.log("Element at index 1: " + myArray[1]); // 8console.log("Element at index 4: " + myArray[4]); // 55 |

You can assign a new value to an array element

array-example2.js

| var names = [ "A", "B", 100 ];console.log("Length of array: " + names.length); // 3Elementsconsole.log("Element at index 0: " + names[0]); // Aconsole.log("Element at index 1: " + names[1]); // Bconsole.log("Element at index 2: " + names[2]); // 100// Assign new value to element at index 2:names[2] = "D";console.log("Element at index 2: " + names[2]); |

Using loops, you can access array elements respectively:

array-loop-example.js

| var fruits = ["Acerola", "Apple", "Banana", "Breadfruit", "Carambola" ];for( var index = 0; index < fruits.length; index++) {console.log("Index: " + index+" Element value: " +fruits[index]);} |

Output

| Index: 0 Element value: AcerolaIndex: 1 Element value: AppleIndex: 2 Element value: BananaIndex: 3 Element value: BreadfruitIndex: 4 Element value: Carambola |

3  Array Object

An array can also be created via the Array class:

| // Create an array has 4 elementsvar myArray1 = new Array(4);// Create an array with 3 elements:var myArray2 = new Array("Acerola", "Apple", "Banana"); |

Example:

array-object-example.js

| // Create an array has 4 elements:var salaries = new Array(4);for(var i = 0; i < salaries.length; i++) {console.log(salaries[i]); // undefined}for(var i = 0; i < salaries.length; i++) {// Assign new value to element:salaries[i] = 1000 + 20 * i;}console.log(salaries[2]); // 1040. |

Output

| undefinedundefinedundefinedundefined1040 |

4  Array methods

An array is an object. It will have methods. Below is the list of its methods:

concat()

every()

some()

filter()

forEach()

map()

indexOf()

join()

lastIndexOf()

pop()

push()

reduce()

reduceRight()

reverse()

shift()

slice()

toSource()

sort()

splice()

toString()

unshift()

concat()

The concat() method returns a new array including its elements joining with the elements of arrays (or values) in parameters .

| // Example:array.concat(arrayOrValue1, arrayOrValue2, ..., arrayOrValueN); |

Parameters:

arrayOrValueN: An array or a value.

array-concat-example.js

| var alpha = ["a", "b", "c"];var numeric = [1, 2, 3];var results = alpha.concat(numeric, "!");console.log(alpha); // ["a", "b", "c"];console.log(results); // [ 'a', 'b', 'c', 1, 2, 3, '!' ] |

every()

This method returns true if all elements of this aray satisfy a test function provided .

| array.every(callback[, thisObject]); |

Parameters:

callback − Function to test for each element.

thisObject − Object to use as this when executing callback.

For example, you have an array of values of employees' ages, let's use the every() method to test whether all elements of the array are located within 18-60 or not.

array-every-example.js

| // Test if value between 18 and 60.testAge = function(value, index, testArray)  {return value >= 18 && value <= 60;}var ages = [18, 22, 59];// Or: var okAll = ages.every(testAge);var okAll = ages.every(testAge, ages);console.log("OK ALL? " + okAll); |

forEach()

This method will call a function for each element of array.

| array.forEach(callback[, thisObject]); |

Parameters:

callback − A function to do something for each element.

thisObject − Object to use as this when executing callback.

array-forEach-example.js

| // Check value between 18 and 60.// (callback function)showTestResult = function(value, index, testArray)  {if(value >= 18 && value <= 60) {console.log("Age " + value + " valid!");} else  {console.log("Sorry, Age " + value + " invalid!");}}var ages = [5, 6, 18, 22, 59, 15 ];// Or: ages.filter(showTestResult);ages.forEach(showTestResult, ages); |

Output

| Sorry, Age 5 invalid!Sorry, Age 6 invalid!Age 18 valid!Age 22 valid!Age 59 valid!Sorry, Age 15 invalid! |

Chapter 4 :

JavaScript Loops

1  Overview of the loops

2  while loop

3  for loop

4  For .. in loop

5  For .. of loop

6  do...while loop

7  Use the break statement in the loop

8  Use the continue statement in the loop

9  Labelled Loop

1  Overview of the loops

Statements are executed sequentially from top to bottom. However, when you want to execute a sequence of statements multiple times, you can use loop.

| ![](OEBPS/image_rsrc8PT.jpg) |

3 types of loops:

while loop

for loop

do .. while loop

Statements can be used within a loop:

continue

breakThe

| Control Statement | Description |
| break | Terminates the loop statement. |
| continue | Causes the loop to skip the remainder of its body and immediately retest its condition prior to reiterating. |

2  while loop

The syntax of a while loop:

| while (condition)  {// Do something here// ....} |

Example:

while-loop-example.js

| console.log("While loop example");// Declare a variable, and assign value of 2.let x = 2;// Condition is x < 10// If x < 10 is true then run blockwhile (x < 10) {console.log("Value of x = ", x);x = x + 3;}// This statment is out of while block.console.log("Finish"); |

Output

| While loop exampleValue of x = 2Value of x = 5Value of x = 8Finish |

3  for loop

The standard for loop has the syntax as follows:

| for(InitialValues; condition; updateValues ){// Statements} |

InitialValues: Initialize values for the related variables in the loop.

condition: Defines the conditions for executing command blocks.

updateValues: Update new values for variables

for-loop-example.js

| console.log("For loop example");for( let i = 0; i < 10; i= i + 3)  {console.log("i= "+ i);} |

Output

| For loop examplei= 0i= 3i= 6i= 9 |

for-loop-example2.js

| console.log("For loop example");for(let i = 0, j = 0; i + j < 10; i = i+1, j = j+2)  {console.log("i = " + i +", j = " + j);} |

Output

| For loop examplei = 0, j = 0i = 1, j = 2i = 2, j = 4i = 3, j = 6 |

Using the for loop can help you traverse on the elements of the array.

for-loop-example3.js

| console.log("For loop example");// Arraylet names =["Tom","Jerry", "Donald"];for (let i = 0; i < names.length; i++ ) {console.log("Name = ", names[i]);}console.log("End of example"); |

Output

| For loop exampleName = TomName = JerryName = DonaldEnd of example |

4  For .. in loop

The for..in loop helps you iterate over the properties of an object.

| for (prop in object) { // Do something} |

Example:

for-in-loop-example.js

| // An object has 4 properties (name, age, gender,greeing)var myObject = {name : "John",age: 25,gender: "Male",greeting : function() {return "Hello";}};for(myProp in myObject)  {console.log(myProp);} |

Output

| nameagegendergreeting |

5  For .. of loop

The for..of loop helps you iterate over a Collection, for example, Map, Set.

Example:

for-of-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );for(let fruit of fruits)  {console.log(fruit);} |

Output

| AppleBananaPapaya |

for-of-example2.js

| // Create a Map object.var myContacts = new Map();myContacts.set("0100-1111", "Tom");myContacts.set("0100-5555", "Jerry");myContacts.set("0100-2222", "Donald");for( let arr of myContacts)  {console.log(arr);console.log(" - Phone: " + arr[0]);console.log(" - Name: " + arr[1]);} |

Output

| [ '0100-1111', 'Tom' ]- Phone: 0100-1111- Name: Tom[ '0100-5555', 'Jerry' ]- Phone: 0100-5555- Name: Jerry[ '0100-2222', 'Donald' ]- Phone: 0100-2222- Name: Donald |

6  do...while loop

The do-while loop is used to execute a section of program many times.The characteristics of the do-while is that the block of statement is always executed at least once. After each iteration, the program will check the condition, if the condition is still correct, the statement block will be executed again.

| do {// Do something}while (expression); |

Example:

do-while-loop-example.js

| let value = 3;do {console.log("Value = " + value);value = value + 3;} while (value < 10); |

Output

| Value = 3Value = 6Value = 9 |

7  Use the break statement in the loop

break is a statement that may be located in a loop. This statement ends the loop unconditionally.

| ![](OEBPS/image_rsrc8PU.jpg) |

loop-break-example.js

| console.log("Break example");// Declare a variable and assign value of 2.let x = 2;while (x < 15) {console.log("----------------------");console.log("x = ", x);// If x = 5 then exit the loop.if (x == 5) {break;}// Increase value of x by 1x = x + 1;console.log("x after + 1 = ", x);}console.log("End of example"); |

Output

| Break example----------------------x = 2x after + 1 = 3----------------------x = 3x after + 1 = 4----------------------x = 4x after + 1 = 5----------------------x = 5End of example |

8  Use the continue statement in the loop

continue is a statement which may be located in a loop. When caught the continue statement, the program will ignore the command lines in block, below of continue and start of a new loop.

| ![](OEBPS/image_rsrc8PV.jpg) |

loop-continue-example.js

| console.log("Continue example");// Declare a variable and assign value of 2x = 2while (x < 7) {console.log("----------------------")console.log("x = ", x)// % is used for calculating remainder// If x is even, then ignore the command line below of continue// and start new iteration.if (x % 2 == 0) {// Increase x by 1.x = x + 1;continue;}else {// Increase x by 1.x = x + 1console.log("x after + 1 =", x)}}console.log("End of example"); |

Output

| Continue example----------------------x = 2----------------------x = 3x after + 1 = 4----------------------x = 4----------------------x = 5x after + 1 = 6----------------------x = 6End of example |

9  Labelled Loop

Allows you to stick a label to a loop. It is like you name a loop, which is useful when you use multiple nested loops in a program.

You can use break labelX statement;to break a loop is attached labelX.

You can use continue labelX statement; to continue a loop is attached labelX.

| ![](OEBPS/image_rsrc8PW.jpg) |

Syntax:

| // for loop with Label.label1: for( ... )  {}// while loop with Label.label2: while ( ... )  {}// do-while loop with Label.label3: do  {} while ( ... ); |

Example of using nested loops, labelled and labelled break statement.

labelled-loop-break-example.js

| console.log("Labelled Loop Break example");let i = 0;label1: while (i < 5) {console.log("----------------------\n");console.log("i = " + i);i++;label2: for (let j = 0; j < 3; j++) {console.log("  --> " + j);if (j > 0) {// Exit the loop with label1.break label1;}}}console.log("Done!"); |

Output

| Labelled Loop Break example----------------------i = 0--> 0--> 1Done! |

Example of using nested labelled loops and labelled continue statement.

labelled-loop-continue-example.js

| let i = 0;label1: while (i < 5) {console.log("outer i= " + i);i++;label2: for (let j = 0; j < 3; j++) {if (j > 0) {continue label2;}if (i > 1) {continue label1;}console.log("inner i= " + i + ", j= " + j);}} |

Output

| outer i= 0inner i= 1, j= 0outer i= 1outer i= 2outer i= 3outer i= 4 |

Chapter 5 :

JavaScript Functions

1  What is Function

2  Function with default parameter

3  Varargs parameter

4  Anonymous Function

5  Function Constructor

6  Generator Function

1  What is Function

A function means a subprogram, which includes commands to perform a duty. And when you want to do such duty somewhere in the application, you only need to call this function. The function helps you maintain the application and reuse code easily.

Below is the syntax for defining a simple function without parameters:

| function function_name() {// function body} |

For example:

my-first-function-example.js

| // Define a function:function greeting()  {console.log("Hello World!");}// Call function.greeting(); |

Output

| Hello World! |

A standard function is defined by the following syntax:

| function function_name(parameter1, parameter2, .., parameterN) {// Function body// return ....} |

Use the function keyword to define a function.

Functions can have 0 or many parameters.

The function always returns a value, if this value is not indicated, it will return underfined. To return a value we use the return keyword.

standard-function-example.js

| function calculateTax(salary)  {if(salary >= 1000) {// The function will end herereturn salary * 20 / 100;}if(salary >= 500)  {// The function will end herereturn salary * 10 / 100;}return 0;}let tax = calculateTax(2000);console.log("Salary: 2000, tax: " + tax);tax = calculateTax(800);console.log("Salary: 800, tax: " + tax);tax = calculateTax(300);console.log("Salary: 300, tax: " + tax); |

Output

| Salary: 2000, tax: 400Salary: 800, tax: 80Salary: 300, tax: 0 |

2  Function with default parameter

A function allows parameters to be initialized with default values. These default values will be used if you do not pass values to these parameters. (Or pass an undefined value when calling a function like the following example:

default-params-example1.js

| function add(a, b = 1) {return a+b;}// Testlet value = add(2, 3);console.log(value); // 5// Testvalue = add(9);console.log(value); // 10 |

default-params-example2.js

| function calculateTax(salary = 1000, rate = 0.2) {return salary * rate;}// Testconsole.log (calculateTax() ) ; // 1000 * 0.2 = 200console.log (calculateTax(2000) ) ; // 2000 * 0.2 = 400console.log (calculateTax(3000, 0.5) ) ; // 3000 * 0.5 = 1500console.log (calculateTax(undefined, 0.5) ) ; // 1000 * 0.5 = 500 |

3  Varargs parameter

Varargs parameter (Or also refered to as "Rest Parameters" means a special parameter of a function. You can pass 0, 1 or more values to the Varargs parameters.

characteristics of Varargs parameter:

*   If a function has a Varargs parameter, this parameter has to be the last parameter of the function.
*   A function has at maximum 1 Varargs parameter.

Syntax

| function myFunction(param1, param2, ... paramVarargs)  {} |

varargs-param-example.js

| function showInfo(name, ... points)  {console.log("------------ ");console.log("Name: " + name);console.log("Array length: "+ points.length);for(let i=0; i< points.length; i++)  {console.log( points[i] );}}showInfo("Tom", 52, 82, 93);showInfo("Jerry", 10, 50);showInfo("Donald"); |

Output

| ------------Name: TomArray length: 3528293------------Name: JerryArray length: 21050------------Name: DonaldArray length: 0 |

4  Anonymous Function

A function having no name is called an anonymous function. Anonymous functions are dynamically created at runtime of the program. It also has parameters and returns like a common function.

You can also declare a variable with value as an anonymous function. Such an expression is called Function Expression.

| var myVar = function( parameters ) {// ....} |

Example:

anonymos-function-example.js

| // Function expressionvar f = function(name){return "Hello " + name;}// Call it.var value = f("Tom");console.log( value ); // Hello Tom. |

For example, create an anonymous function and call it immediately. In this case the anonymous function is created for only one use.

anonymous-function-example2.js

| // Create anonymous function and call immediately(function()  {var now = new Date();console.log("Now is " + now);}) () ;// Create anonymous function and call immediately(function(name)  {console.log("Hello " + name);}) ("Tom") ; |

Output

| Now is Mon Nov 05 2023 00:44:47Hello Tom |

5  Function Constructor

We have a Function class, so you can create a function through the constructors of this class.

| var variableName = new Function(paramName1, paramName2, ..., paramNameN, "Function Body"); |

For example:

function-constructor-example.js

| var myMultiple = new Function( "x", "y", "return x * y");console.log( myMultiple (3, 4) ); // 12function showTotal()  {let quantity = 4;let price = 5;console.log("Total: " + myMultiple(quantity, price) );}showTotal(); |

Output

| 12Total: 20 |

6  Generator Function

To declare a Function Generator we use the function* keyword.

| function* functionName( param1, param2, ..., paramN) {// Statements} |

Basically, Generator Function means a function that is able to suspend execution, and continue running at any time. The Function Generator returns an Iterator object in an implicit manner. In the contents of this function you only need to define the values for the elements in such iterator.

Maybe you will feel really confused with the above explanation. We will see an example:

| ![](OEBPS/image_rsrc8PX.jpg) |

generator-function-example.js

| function* season()  {yield "Spring";yield "Summer";yield "Autumn";yield "Winter";}// This method return an Iterator.var seasonIterator = season();let value1 = seasonIterator.next().value;console.log(value1); // Springlet value2 = seasonIterator.next().value;console.log(value2); // Summerlet value3 = seasonIterator.next().value;console.log(value3); // Autumnlet value4 = seasonIterator.next().value;console.log(value4); // Winter |

Shorter example:

| function* season()  {yield "Spring";yield "Summer";yield "Autumn";yield "Winter";}// This method return an Iterator.var seasonIterator = season();let e;while( !(e = seasonIterator.next()).done ) {console.log(e.value);} |

When a common function is called, it will execute until the value is returned or the function finishes. During that time the Caller Function can not control the execution of the Called Function.

Caller Function can control the execution of the Called Function if the Called Function is a Generator Function. Below is such example:

generator-function-example3.js

| function* season()  {console.log("Do something in Spring");yield "Spring";// Spring Stop here!console.log("Do something in Summer");yield "Summer";// Summer Stop here!console.log("Do something in Autumn");yield "Autumn";// Autumn Stop here!console.log("Do something in Winter");yield "Winter";// Winter Stop here!}// This method returns an Iterator.var seasonIterator = season();let e;while( !(e = seasonIterator.next()).done ) {console.log(e.value);if(e.value === "Autumn") {console.log("OK Stop after Autumn");break;}} |

Output

| Do something in SpringSpringDo something in SummerSummerDo something in AutumnAutumnOK Stop after Autumn |

Chapter 6 :

JavaScript Number

ECMAScript Number

In ECMAScript, the Number data type represents for a number, which can be an Integer, or a Floating-point Number.

Based on memory-based management way, Number is divided into the 2 kinds: Number Object and Number Primitive:

Number Primitive:

Normally, to create a number, you should use the Primitive syntax:

| // Primitive Syntax:var myNumber1 = 100;var myNumber2 = 55.1; |

Number primitives are managed in Common Pool, which means when you declare 2 or more Number primitives with the same value. They will point to the same memory location in the Common Pool.

The === operator is used to check if two variables point to the same address on memory or not.

| ![](OEBPS/image_rsrc8PY.jpg) |

number-primitive-example1.js

| let a = 100;let b = 150.1;let c = 150.1;// a, b: Same address?console.log( a === b); // false// b, c: Same address?console.log( b === c); // true |

You can also create a number by using the Number(value) function. The result received by you is a Number primitive:

number-primitive-example2.js

| let a = 100;let b = 150.1;// Using Number() functionlet c = Number(150.1);// a, b: Same address?console.log( a === b); // false// b, c: Same address?console.log( b === c); // true |

Number object:

You can create a number through the constructor of Number class. In this case, you will receive a Number object.

| // Syntax:var aNumber = new Number(number);// Example:var myNumber1 = new Number(100);var myNumber2 = new Number(150.1); |

The new operator always creates a new entity on the Heap memory.

| ![](OEBPS/image_rsrc8PZ.jpg) |

When you assign the new value which is variable aa to the variable bb . The variable bb will point to the address on memory to which the variable aa is pointing. No entity will be created on memory in this case.

| ![](OEBPS/image_rsrc8R0.jpg) |

Chapter 7 :

JavaScript Boolean

ECMAScript Boolean

Boolean is the simplest data type in ECMAScript. It only has two primitive values: true and false.

Boolean-primitive

Below is the primitive syntax which is the simplest one for you to create a variable with the data type of Boolean:

boolean-primitive-example.js

| let a = true;let b = false;console.log( a ); // trueconsole.log( b ); // false |

Boolean Common Pool is a pool. It has only two values: true, false. When you create a variable based on the primitive syntax, it will point to the address of true or false in the pool.

The === operator is used to compare 2 addresses that two variables are pointing to.

| ![](OEBPS/image_rsrc8R1.jpg) |

Boolean-object:

You can also create a Boolean object through the constructor of Boolean class. In essence you will create a object wrapping a primitive value: true or false .

| var myObj = new Boolean(value); |

Parameter:

value: If this parameter has the value such as false, 0, "", null, undefined, NaN, Number.Infinite , it will create a Boolean {false} object. In other cases it will create Boolean {true} object.

boolean-object-example.js

| console.log( new Boolean(false) );           // [Boolean: false]console.log( new Boolean("") );              // [Boolean: false]console.log( new Boolean(null) );            // [Boolean: false]console.log( new Boolean() );                // [Boolean: false]console.log( new Boolean(undefined) );       // [Boolean: false]console.log( new Boolean(0) );               // [Boolean: false]console.log( new Boolean(NaN) );             // [Boolean: false]console.log( new Boolean(Number.Infinite) ); // [Boolean: false]console.log( new Boolean(-Number.Infinite) );// [Boolean: false]console.log(" ------------------- ");console.log( new Boolean("0") );       // [Boolean: true]console.log( new Boolean("false") );   // [Boolean: true]console.log( new Boolean(1) );         // [Boolean: true]console.log( new Boolean(100) );       // [Boolean: true]console.log( new Boolean( {} ) );      // [Boolean: true] |

Everytime you use the new operator, a new object will be created on the Heap memory. So, creating a Boolean object through the new operator will cost more to store them.

| ![](OEBPS/image_rsrc8R2.jpg) |

When you assign the new value which is variable aa to the variable bb. The bb variable will point to the address on memory to which the variable aa is pointing. No entity will be created on memory in this case.

| ![](OEBPS/image_rsrc8R3.jpg) |

Chapter 8 :

JavaScript Strings

ECMAScript String

In ECMAScript, String is a special data type, because it is used frequently in a program, therefore, it is required to have performance and flexibility. That's reason why the String is both objective and primitive.

String Literal

You can create a string literal. The string literal is stored in a stack, requiring less storage space, and cheaper to manipulate.

| let aStringLiteral = "Hello World"; |

string literals are contained in a Common Pool. When you declare two String Literal variables with the same content, they will point to the same address stored on the pool.

| ![](OEBPS/image_rsrc8R4.jpg) |

string-literal-example.js

| let a = "Tom";let b = "Jerry";let c = "Jerry";console.log(a); // Tomconsole.log(b); // Jerryconsole.log(c); // Jerry// a, b: Same address?console.log( a === b); // false// b, c: Same address?console.log( b === c); // true |

String Object

You can create a string through the constructor of the String class. In this case, you will receive a String object.

| let myStringObj = new String(value); |

Parameters:

value: A value to convert to string

string-object-example.js

| let a = new String("Hello World");console.log(a); // [String: 'Hello World']let b = new String(true);console.log(b); // [String: 'true']let c = new String(100.20);console.log(c); // [String: '100.2'] |

The new operator always creates a new entity on the Heap memory, which explains why you have to spend more money using String Objects.

| ![](OEBPS/image_rsrc8R5.jpg) |

When you assign a new value that is variable aa to variable bb. The variable bb will point to the address on memory to which the variable aa is pointing. There will not be an entity created on memory in this case.

| ![](OEBPS/image_rsrc8R6.jpg) |

String is Imutable

In the ECMAScript, the String data type is imutable, which means that any action you do on the strings such as string concatenation, string cutting, etc. creates a new string on memory, or return another string.

| ![](OEBPS/image_rsrc8R7.jpg) |

The concat(string) method is used to concatenate a string into the current string. But in fact the current string does not change, and a new string (the result of concatenating) is created. The following figure illustrates program behavior:

| ![](OEBPS/image_rsrc8R8.jpg) |

concat-example2.js

| let a = "Hello";let b = "World";let c = a.concat(b);console.log(c); // HelloWorldconsole.log(a); // Helloconsole.log( a === c); // false |

Properties of String

constructor

length

prototype

length

This property returns the number of characters in a string.

length-example.js

| let s1 = "Tom";console.log(s1); // Tomconsole.log("Length "+ s1.length); // 3let s2 = "Tom & Jerry";console.log(s2); // Tom & Jerryconsole.log("Length "+ s2.length); // 11 |

Methods of String

charAt(index)

Returns the character at the specified index.

| ![](OEBPS/image_rsrc8R9.jpg) |

charAt-example.js

| let str = "This is a String";console.log("str.charAt(0) is:" + str.charAt(0)); // Tconsole.log("str.charAt(1) is:" + str.charAt(1)); // hconsole.log("str.charAt(2) is:" + str.charAt(2)); // iconsole.log("str.charAt(3) is:" + str.charAt(3)); // sconsole.log("str.charAt(4) is:" + str.charAt(4)); //console.log("str.charAt(5) is:" + str.charAt(5)); // i |

charCodeAt(index)

| ![](OEBPS/image_rsrc8RA.jpg) |

charCodeAt-example.js

| let str = "This is a String";console.log("str.charCodeAt(0) is:" + str.charCodeAt(0)); // 84console.log("str.charCodeAt(1) is:" + str.charCodeAt(1)); // 104console.log("str.charCodeAt(2) is:" + str.charCodeAt(2)); // 105console.log("str.charCodeAt(3) is:" + str.charCodeAt(3)); // 115console.log("str.charCodeAt(4) is:" + str.charCodeAt(4)); // 32console.log("str.charCodeAt(5) is:" + str.charCodeAt(5)); // 105 |

concat(string2[,string3[, ..., stringN]]

indexOf(searchValue[, fromIndex])

| ![](OEBPS/image_rsrc8RB.jpg) |

indexOf-example.js

| let str = "This is a String";let idx = str.indexOf("is", 3);console.log( idx ); // 5let idx2 = str.indexOf("is");console.log( idx2 ); // 2 |

lastIndexOf(searchValue[, toIndex])

| ![](OEBPS/image_rsrc8RC.jpg) |

lastIndexOf-example.js

| let str = "This is a String";let idx = str.lastIndexOf("is", 10);console.log( idx ); // 5let idx2 = str.lastIndexOf("is", 5);console.log( idx2 ); // 5let idx3 = str.lastIndexOf("is", 4);console.log( idx3 ); // 4 |

str.slice( beginIndex [, endIndex] )

The method returns a substring determined by the two positions such as beginIndex and endIndex. If the beginIndex position is located on the right hand side and the endIndex is located on the left hand side, the returned string is always empty.

| ![](OEBPS/image_rsrc8RD.jpg) |

slice-example.js

| var str = "This is a String";var result = str.slice(3, -2);console.log(result);// s is a Strivar result2 = str.slice(3);console.log(result2);// s is a String// IMPORTANT!!var result3 = str.slice(5, 1); // ==> Empty Stringconsole.log(result3);//// IMPORTANT!!var result4 = str.slice(5, -13); // ==> Empty Stringconsole.log(result4);// |

str.substr(start[, length])

| ![](OEBPS/image_rsrc8RE.jpg) |

substr-example.js

| var str = "This is a String";var result = str.substr(3, 8);console.log(result);// s is a Svar result2 = str.substr(3);console.log(result2);// s is a String |

str.substring(beginIndex[, endIndex])

The method returns a substring defined by the two positions such as beginIndex and endIndex.. Note: substring(a, b) & substring(b, a) will return the same result.

| ![](OEBPS/image_rsrc8RF.jpg) |

substring-example.js

| var str = "This is a String";var result = str.substring(3, -2);console.log(result);// s is a Strivar result2 = str.substring(3);console.log(result2);// s is a String// IMPORTANT:// result3 same as result4:var result3 = str.substring(4, 1);var result4 = str.substring(1, 4);console.log(result3);// hisconsole.log(result4);// his |

Chapter 9 :

JavaScript if else Statement

1  if statment

2  if - else statement

3  if - else if - else statement

4  Operators involved in conditional expression

1  if statment

The if(condition) statement evaluates a condition to decide whether its block is executed or not.

Below is the structure of if statement:

| if (condition)  {// Do something here!} |

condition can be any value, any type or any expression. ECMAScript uses the Boolean(condition) function to evaluate. This function returns true or false.

The following figure illustrates how to evaluate a condition of ECMAScript:

| ![](OEBPS/image_rsrc8RG.jpg) |

Example:

simple-if-example.js

| if(true)  { // Workconsole.log("Test 1");}if(false) { // Not work!console.log("Test 2");} |

Output

| Test 1 |

if-example.js

| if(true)  { // Workconsole.log("if(true)");}if(false)  { // Not work!console.log("if(false)");}if('true')  { // Workconsole.log("if('true')");}if('false')  { // Workconsole.log("if('false')");}var obj = new Object();if(obj)  { // Workconsole.log("if(obj)");}if('') { // Not work!console.log("if('')");}if(undefined) { // Not work!console.log("if(undefined)");}if(0)  { // Not work!console.log("if(0)");} |

Output

| if(true)if('true')if('false')if(obj) |

if-example2.js

| var number0 = 0;if(number0)  { // Not work!console.log("number 0 (primitive)");}if(false)  { // Not work!console.log("boolean false (primitive)");}// A not null Objectvar myObj = {};if(myObj)  { // Work!console.log("A not null Object");}// A not null Objectvar numberObject = new Number(0);if(numberObject)  { // Work!console.log("A not null Object (Number)");}// A not null Objectvar booleanObject = new Boolean(false);if(booleanObject)  { // Work!console.log("A not null Object (Boolean)");} |

Output

| A not null ObjectA not null Object (Number)A not null Object (Boolean) |

if-example3.js

| // Declare a variable, representing your agelet age = 30;console.log("Your age: " + age);// The condition to test is 'age> 20'if (age > 20) {console.log("Okey!");console.log("Age is greater than 20");}// The code blow the 'if' block.console.log("Done!"); |

Output

| Your age: 30Okey!Age is greater than 20Done! |

2  if - else statement

The if-else command is also used to check a condition. Uses the Boolean(condition) function to evaluate conditions. If the evaluation result is true, the if block will be executed. On the contrary, the else block will be executed.

| if( condition )  {// Do something here}// Elseelse  {// Do something here} |

| ![](OEBPS/image_rsrc8RH.jpg) |

Example:

if-else-example.js

| // Declare a variable, representing your agelet age = 15;console.log("Your age: " + age);// The condition to test is 'age> 18'if (age >= 18) {console.log("Okey!");console.log("You are accepted!");} else {console.log("Sorry!");console.log("Age is less than 18");}// The code after the 'if' block and 'else' block.console.log("Done!"); |

Output

| Your age: 15Sorry!Age is less than 18Done! |

3  if - else if - else statement

The structure of an if - else if - else statement is:

| if(condition 1)  {// Do something here} else if(condition 2) {// Do something here} else if(condition 3) {// Do something here}// Elseelse  {// Do something here} |

| ![](OEBPS/image_rsrc8RJ.jpg) |

if-elseif-else-example.js

| // Declaring a varible// Represent your test scores.let score = 70;console.log("Your score =" + score);// If the score is less than 50if (score < 50) {console.log("You are not pass");}// Else if the score more than or equal to 50 and less than 80.else if (score >= 50 && score < 80) {console.log("You are pass");}// Remaining cases (that is greater than or equal to 80)else {console.log("You are pass, good student!");} |

Output

| Your age: 15Sorry!Age is less than 18Done! |

4  Operators involved in conditional expression

This is a list of operators, commonly used in conditional expressions.

> Greater Than

< Less Than

>= Greater Than or Equal To

<= Less Than or Equal To

&& AND

|| OR

== HAS A VALUE OF

!= Not Equal To

! NOT

Example:

if-elseif-else-example2.js

| // Declare a variable, represents your age.let age = 20;// Test if age less than or equal 17if (age <= 17) {console.log("You are 17 or younger");}// Test age equals 18else if (age == 18) {console.log("You are 18 year old");}// Test if age greater than 18 and less than 40else if (age > 18 && age < 40) {console.log("You are between 19 and 39");}// Remaining cases (Greater than or equal to 40)else {// Nested if statements// Test age not equals 50.if (age != 50) {console.log("You are not 50 year old");}// Negative statementsif (!(age == 50)) {console.log("You are not 50 year old");}// If age is 60 or 70if (age == 60 &#124;&#124; age == 70) {console.log("You are 60 or 70 year old");}} |

Output

| You are between 19 and 39 |

Chapter 10 :

JavaScript Switch Statement

1  The structure of switch statement

2  switch Example

3  break statement in switch

1  The structure of switch statement

Syntax

| // variable_to_test: A varible to test.switch ( variable_to_test ) {case value1:// Do something here ...break;case value2:// Do something here ...break;default:// Do something here ...} |

The characteristics of switch statement:

The switch will check the value of a variable and compare that variable with each different value from top to bottom. Each value to be compared is called a case. When a case is true, the statement block of that case will be executed.

| ![](OEBPS/image_rsrc8RK.jpg) |

If all cases are false, the default statement block will be executed. Note: in the structure of the switch statement, there is probably or not a default statement block.

| ![](OEBPS/image_rsrc8RM.jpg) |

When finding a true case, the statement block of such case will be executed. If not meeting the break statement in this block, the program will continue performing the blocks below until it meets the break statement or no statement block is executed.

The break statement makes the program exit the switch. (See the illustration below).

| ![](OEBPS/image_rsrc8RN.jpg) |

Note that the case statement is a specific value you can not do the following:

| // This is not allowed !!case (age < 18) :// case only accept a specific value, eg:case 18:// Do something here ..break; |

2  switch Example

switch-example.js

| // Declare a variable agelet age = 20;// Check the value of ageswitch (age) {// Case age = 18case 18:console.log("You are 18 year old");break;// Case age = 20case 20:console.log("You are 20 year old");break;// Remaining casesdefault:console.log("You are not 18, 20 year old");} |

Output

| You are 20 year old |

3  break statement in switch

break means a statement to be able to appear in the case block, or default block of switch. When meeting the break statement, the program will exit the switch.

| ![](OEBPS/image_rsrc8RP.jpg) |

When the program meets a switch statement, it will check cases from top to bottom. When finding a true case, the block of that case will be executed. If it doesn't meet the break statement in this block, it will continue to execute the blocks below until it meets the break statement or there is no longer block to execute.

Example:

switch-example2.js

| // Declare a variable age.let age = 30;// Check the value of age.switch (age) {// Case age = 18case 18:console.log("You are 18 year old");break;// Case age in 20, 30, 40case 20:case 30:case 40:console.log("You are " + age);break;// Remaining case:default:console.log("Other age");} |

Output

| You are 30 |

Chapter 11 :

JavaScript Error Handling

1  What is Error

2  Handling error with try-catch

3  try-catch-finally

4  Built-in Errors

5  Throw Error

6  The properties of Error

7  Re-throw Error

8  Exceptions when catching errors

1  What is Error

First of all, let's look at an example, in which I call a method of an object, but this object actually does not have this method, and the error occurs.

hello-error-example.js

| console.log("Three");let myObj = {};console.log("Two");console.log("One");// Object myObj has no showMe() method.// But we call showMe().// And error occur here.myObj.showMe(); // ==> Error!!!!!!!!!// And the following code will not be executed.console.log("Let's go!"); |

Please have a look at the flow of the program through the following illustration.

| ![](OEBPS/image_rsrc8RR.jpg) |

*   The program runs completely normally in steps (1), (2), (3), (4)
*   In step (5) an error occurs when you are trying to call an object method while this object doesn't have that method .
*   Code in step (6) will not be executed.

2  Handling error with try-catch

Errors may occur in the runtime of the program. it may be an unexpected error. Use try-catch helps you catch and handle errors when they happen.

Come back to the above example, we add try-catch to catch and handle errors.

hello-catch-example.js

| console.log("Three");let myObj = {};console.log("Two");console.log("One");try {// Object myObj has no showMe() method.// But we call showMe().// And error occur here.myObj.showMe(); // ==> Error!// This code will be ignoredconsole.log ("!!!");} catch (e) {console.log("Catched error: " + e);console.log("OK continue...");}console.log("Let's go!"); |

And the results of running the example:

Output

| ThreeTwoOneCatched error: TypeError: myObj.showMe is not a functionOK continue...Let's go! |

The following illustration explains the flow of the program:

| ![](OEBPS/image_rsrc8RS.jpg) |

*   The steps (1)-(4) are completely normal.
*   An exception occurs in step (5), when you try to call a method of an object, while this object does not have this method.
*   Immediately it jumps in to execute the command in the catch block. Step (6) is ignored.
*   Steps (7), (8) will be executed.
*   Step (9 will be executed.

3  try-catch-finally

We have got accustomed with catching error through try-catch block. try-catch-finally is used to fully handle error. The finally block is always executed, regardless of whether the error occurs in the try block or not.

| try {// Do something here.} catch (e ) {// Do something here.} finally  {// The finally block is always executed.// Do something here.} |

Example:

try-catch-finally-example.js

| function getGreeting(language) {try {console.log("Code in try block (*)");// Call greeting() method of object 'language'// An Exception can throw here if this object has no greeting() method.let v = language.greeting();console.log("Code in try block (**)");return v;} catch (e) {console.log("Code in catch block. Something Error: " + e);} finally {// The finally block is always executed.console.log("Code in finally block");}return " !! ";}// ----------------------- TEST ---------------------------------// Test 1:console.log("----- Call getGreeting(null) -----");let v1 = getGreeting(null);console.log("Greeting: " + v1); // Test 2:console.log("------ Call getGreeting(language) ------");let language = new Object();language.greeting = function() {return "Hello Everybody";}let v2 = getGreeting(language);console.log("Greeting: " + v2); |

Running the example:

Output

| ----- Call getGreeting(null) -----Code in try block (*)Code in catch block. Something Error: TypeError: Cannot read property 'greeting' of nullCode in finally blockGreeting: !!----- Call getGreeting(language) -----Code in try block (*)Code in try block (**)Code in finally blockGreeting: Hello Everybody |

The following illustration is the flow of program if an error occurs in the try block, the finally block is always executed.

| ![](OEBPS/image_rsrc8RT.jpg) |

The following figure shows the flow of the program when no errors occur in the try block. In this case the finally block will be executed immediately before the return command of the try block is executed.

| ![](OEBPS/image_rsrc8RU.jpg) |

4  Built-in Errors

ECMAScript has several available classes to represent an error. Below is their hierarchy.

| ![](OEBPS/image_rsrc8RV.jpg) |

RangeError

A RangeError is thrown if you use a number outside the allowable range.

error-RangeError-example.js

| let num = 1;try {// A number cannot have 500 significant digitsnum.toPrecision(500); // ==> RangeError!!}catch(err) {console.log(err.name);console.log(err);} |

ReferenceError

A ReferenceError is thrown if you use a variable that has not been declared:

error-ReferenceError-example.js

| var x;try {x = y + 1;   // y cannot be referenced (used)}catch(err) {console.log("Error Name: "+ err.name);console.log(err);} |

SyntaxError

A SyntaxError is thrown if you try to evaluate code with a syntax error.

error-SyntaxError-example.js

| try {let x;eval(" x  = 'Hello  ");   // Missing ' will produce an error  try {let x;eval(" x  = 'Hello  ");   // Missing ' will produce an error}catch(err) {console.log("Error Name: " + err.name);console.log(err);}}catch(err) {console.log("Error Name: " + err.name);console.log(err);} |

TypeError

A TypeError is thrown if you use a value that is not of the expected type. For example, an error occurs when you call a method of an object, while this object does not have that method.

error-TypeError-example.js

| var num = 1;try {num.toUpperCase(); // Number has no method toUpperCase()}catch(err) {console.log("Error Name: " + err.name);console.log(err);} |

URIError

A URIError is thrown if you use illegal characters in a URI function:

error-URIError-example.js

| try {decodeURI("%%%");   // You cannot URI decode percent signs}catch(err) {console.log("Error Name: " + err.name);console.log(err);} |

5  Throw Error

ECMAScript allows you to throw anything in the runtime of the program. The program will consider an error has just happened.

throw-any-example.js

| console.log(" -------- Test throw any object ------------");try {let myObj = {};throw myObj;} catch(e)  {console.log("Catch error: ");console.log(e);}console.log(" -------- Test throw a Symbol ------------");try {let mySymbol = Symbol();throw mySymbol;} catch(e)  {console.log("Catch error: ");console.log(e);}console.log(" -------- Test throw a Number ------------");try {let myNumber = 100;throw myNumber;} catch(e)  {console.log("Catch error: ");console.log(e);}console.log(" -------- Test throw a String ------------");try {let myString = "Some error";throw myString;} catch(e)  {console.log("Catched error: ");console.log(e);} |

Output

| -------- Test throw any object ------------Catch errorr:{}-------- Test throw a Symbol ------------Catch error:Symbol()-------- Test throw a Number ------------Catch error:100-------- Test throw a String ------------Catched error:Some error |

Normally, you will use an Error class to create an error object. Other classes, such as SyntaxError, InternalError, RangeError, ReferenceError, SyntaxError, TypeError, URIError can also be used in a suitable context.

An error object is created through the Error class (or its child classes). When being thrown, it will contain important information like the file where the error occurs, the location of the error, and the information helps you detect errors.

throw-error-example.js

| console.log("Three");// Create an Errorlet myError = new Error("Something error!");console.log("Two");// Throw it!throw myError;console.log("One"); |

In the simple case, you can throw any object, not the object of the Error class (or its childclasses). However, when catching these types of errors, you will not have the information such as the file of the error, the location of the error, etc.

throw-string-error-example.js

| console.log("Three");try {console.log("Two");// Throw a String!throw "Some error!!";} catch(e)  {console.log("typeof e = " + (typeof e));// Log the errorconsole.log(e); // Some error!!}console.log("One"); |

Output

| ThreeTwotypeof e = stringSome error!!One |

In the ECMAScript, each try block has a corresponding cache block. But there may be many types of errors in the try block, in which case you need to check the error caught in the catch block to provide appropriate handlings corresponding to each type of error.

catch-complex-example.js

| let err = new Error("My Error");let rangeErr = new RangeError();let evalErr = new EvalError("My Eval Error");// A random value in [0.. 9]let randomValue = Math.floor(Math.random() * 10);// [0,1,2,3]let random0123 = randomValue % 4;console.log("random0123 = " + random0123);try {if(random0123 == 0) {throw err;} else if(random0123 == 1){throw rangeErr;} else if(random0123 == 2)  {throw evalErr;} else if(random0123 == 3)  {throw "A String Error";}} catch(e)  {console.log("typeof e = " + (typeof e));// 'object' or 'string'if(e instanceof RangeError) {console.log("--> RangeError!!");} else if(e instanceof EvalError) {console.log("--> EvalError!!");} else if(e instanceof Error) {console.log("--> Error!!");} else if (typeof e == "string"){console.log("--> String Error!!");} else  {console.log("--> Error!!");}console.log(e);} |

6  The properties of Error

In the ECMAScript, the error caught by you may be a "Error object" or any error type. If it is a "Error object" you will obtain the important information such as the name of file of error, error position, Stack Trace,..

There are some important properties of the Error class:

*   name: Name of error
*   message: Content of error
*   stack (Readonly): a string containing information helping you detect the position of error.

error-properties-example.js

| // Create an Errorlet myError = new Error();myError.name = "MyError";myError.message = "My Error String";try {throw myError;} catch(err)  {console.log("Error Name: " + err.name);console.log("Error Message: " + err.message);console.log("Type of err.stack: " + (typeof err.stack));console.log("--- Stack Trace: ---");console.log(err.stack);} |

7  Re-throw Error

While handling the exception, you can catch that exception and handle it or you can re-throw it.

rethrow-example.js

| function checkScore(score) {if (score < 0 &#124;&#124; score > 100) {throw "Invalid Score " + score;}}function checkPlayer(name, score) {try {checkScore(score)} catch (e) {// Do something with the Exceptionconsole.log("Something invalid with player: " + name + " >> " + e);// Then re-throw this Exception.throw e;}console.log("OK Player " + name + " has score: " + score );}// --------------- TEST --------------checkPlayer("Tom", 90);checkPlayer("Jerry", -10); |

For example, catch an exception and throw an other exception.

rethrow-example2.js

| function checkScore(score) {if (score < 0 &#124;&#124; score > 100) {throw "Invalid Score " + score;}}function checkPlayer(name, score) {try {checkScore(score)} catch (e) {// Do something with the Exceptionconsole.log("Something invalid with player: " + name + " >> " + e);// Then throw other exceptionthrow ("Score " + score +" invalid for player " + name);}console.log("OK Player " + name + " has score: " + score );}// --------------- TEST --------------checkPlayer("Tom", 90);checkPlayer("Jerry", -10); |

8  Exceptions when catching errors

In the ECMAScript there are the situations that you think that a error will occur but it doesn't happen. For example, a numberdivided by 0 will not cause an error, the result returns Infinity or -Infinity.

ex-Infinity-example.js

| console.log( typeof Infinity ); // numberlet a = 1 / 0;console.log(a); // Infinitylet b = -1 / 0;console.log(b); // -Infinity |

Divide a value other than a number by a number, the result is NaN (Not a Number).

ex-NaN-example.js

| console.log( typeof NaN ); // numberconsole.log( isNaN(1) ); // falseconsole.log( isNaN( NaN ) ); // truelet a = "A String" / 2;console.log(a); // NaNlet obj = {};let b = obj / 2;console.log(b); // NaN |

You can access an element with any index of an array without causing an error.

ex-array-index-example.js

| let myArray = [1, 100, 20];console.log( myArray[1]); // 100console.log( myArray[10] ); // undefinedconsole.log( myArray[-10] ); // undefined |

Chapter 12 :

JavaScript Error Handling

1  Form Validation

2  Simple example

3  Access the form data

4  Submit through Javascript

5  Validate automatically

1  Form Validation

Quite regularly, you meet a website where users enter information into a form before sending it to the server, for example, the account registration form. The information that the user enters into the form needs to be validated to ensure data rationality.

| ![](OEBPS/image_rsrc8RW.jpg) |

Some examples of authentication:

*   Check to ensure that the data is not empty.
*   Check email format
*   Check telephone number format
*   ..

There are basically 3 ways for data validation:

*   form data will be sent to the server, and validation will be done on the server side.
*   form data will be validated on the client side by using Javascript, which helps server not have to work too much and increase performance for the application.
*   Use both above methods to validate form.

In this lesson, I will discuss using Javascript to validate form. Below is the illustration of the program's behavior when the user clicks the Submit button.

| ![](OEBPS/image_rsrc8RX.jpg) |

*   You have to register a function in combination with the onsubmit event of form. The duty of this function is to check the data which an user has entered in form, and return true if all the information entered by the user is valid and vice versa return false.
*   When the user clicks Submit, the function in combination with the onsubmit event will be called.
*   Ifthe function in combination with the onsubmit event returns true, the data of form will be sent to the server and vice versa the Submit action will be cancelled.

2  Simple example

OK, this is a simple example helping you understand the operating rules of Form before practising more complex examples.

| ![](OEBPS/image_rsrc8RY.jpg) |

The action attribute of <form> is used to specify the page to which data will be given or in other words, this is the page that will process the data sent from the <form> of the current page.

Note : The pages processing the data sent from form are usually written by Servlet/JSP, PHP technology or a technology on the Server side instead of an HTML page. However, I do not mention data processing in this lesson.

simple-validation-example.html

| <!DOCTYPE html><html><head><title>Hello Javascript</title><script type = "text/java script">function validateForm()  {var u = document.getElementById("username").value;var p = document.getElementById("password").value;if(u== "") {alert("Please enter your Username");return false;}if(p == "") {alert("Please enter you Password");return false;}alert("All datas are valid!, send it to the server!")return true;}</script></head><body><h2>Enter your Username and Password</h2><div style="border:1px solid #ddd; padding: 5px;"><form method="GET" action="process-action.html" onsubmit = "return validateForm()">Username: <input type="text" name="username" id="username"/><br><br>Password: <input type="password" name = "password" id="password"/><br><br><button type="submit">Submit</button></form></div></body></html> |

process-action.html

| <!DOCTYPE html><html><head><title>Process Action</title></head><body><h3>Process Action Page</h3>OK, I got data!<br/><br/><a href="javascript:history.back();">[Go Back]</a></body></html> |

| ![](OEBPS/image_rsrc8RZ.jpg) |

| ![](OEBPS/image_rsrc8S0.jpg) |

| ![](OEBPS/image_rsrc8S1.jpg) |

| ![](OEBPS/image_rsrc8S2.jpg) |

| ![](OEBPS/image_rsrc8S3.jpg) |

| ![](OEBPS/image_rsrc8S4.jpg) |

| ![](OEBPS/image_rsrc8S5.jpg) |

| ![](OEBPS/image_rsrc8RZ.jpg) |

3  Access the form data

Access a field data through the field ID.

| <input type="text"  id="username"/><input type="password"  id="password"/> |

| // Access field via ID:var field =  document.getElementById("fieldId");var value = field.value; |

Access Form fields through the name attribute:

| <form name="myForm" ...><input type="text" name="username"/><input type="password" name = "password"/><button type="submit">Submit</button></form> |

| // Get form via form name:var myForm = document.forms["myForm"];var u = myForm["username"].value;var p = myForm["password"].value; |

When a user enters inaccurate data on a form field, you should notify the user and focus on that field.

validation-example1.html

| <!DOCTYPE html><html><head><title>Validation</title><script type = "text/javascript">function validateForm()  {// Get form via form name:var myForm = document.forms["myForm"];var u = myForm["username"].value;var p = myForm["password"].value;if(u== "") {alert("Please enter your Username");myForm["username"].focus(); // Focusreturn false;}if(p == "") {alert("Please enter you Password");myForm["password"].focus(); // Focusreturn false;}alert("All datas are valid!, send it to the server!")return true;}</script></head><body><h2>Enter your Username and Password</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" method="GET" action="process-action.html" onsubmit = "return validateForm()">Username: <input type="text" name="username"/><br><br>Password: <input type="password" name = "password"/><br><br><button type="submit">Submit</button></form></div></body></html> |

Example: Ask an user to enter a number between 0 and 10.

validation-number-example.html

| <!DOCTYPE html><html><head><title>Validation</title><script type = "text/javascript">function validateForm()  {var myField = document.getElementById("myNumber");var value = myField.value;if( value == "" &#124;&#124; isNaN(value) &#124;&#124; value < 0 &#124;&#124; value > 10)  {alert("Invalid input!");myField.focus();return false;}return true;}</script></head><body><h2>Enter a Number between 0 and 10</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html" onsubmit = "return validateForm()">Number: <input type="text" id= "myNumber"/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

| ![](OEBPS/image_rsrc8S6.jpg) |

| ![](OEBPS/image_rsrc8S7.jpg) |

| ![](OEBPS/image_rsrc8S8.jpg) |

| ![](OEBPS/image_rsrc8S9.jpg) |

| ![](OEBPS/image_rsrc8SA.jpg) |

| ![](OEBPS/image_rsrc8SB.jpg) |

4  Submit through Javascript

Clicking <button type="submit"> or <input type="submit"> inside form helps you to send the data of this form to the server, however, you can also do it through Javascript.

javascript-submit-example.html

| <!DOCTYPE html><html><head><title>Javascript Submit</title><script type = "text/javascript">function validateForm() {var name = document.forms["myForm"]["fullName"].value;if(name == "") {alert("Please enter your name");return false;}return true;}function submitByJavascript()  {var valid = validateForm();if(!valid)  {return;}var myForm = document.forms["myForm"];myForm.submit();}</script></head><body><h2>Submit a from with Javascript</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html" onsubmit = "return validateForm()">Your Name: <input type="text" name = "fullName" value =""/><br/><br/><button type="submit">Submit</button></form></div><br/><!-- A Button outside the form -->Button outside the form:<button onclick="submitByJavascript()">Click Me to submit form</button></body></html> |

5  Validate automatically

The browser can automatically validate several types of data on the form, such as adding a required attribute to a form field to tell the browser that this field is mandatory. The browser will automatically check and notify an user if an user does not enter that field.

| ![](OEBPS/image_rsrc8SC.jpg) |

| ![](OEBPS/image_rsrc8SD.jpg) |

required-example.html

| <!DOCTYPE html><html><head><title>Required</title></head><body><h2>Required attribute</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html" onsubmit = "return validateForm()">Your Name: <input type="text" name = "fullName" value ="" required/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

Some <input> elements newly introduced in HTML 5, for example color, date, datetime-local, email, month, number, range, search, tel, time, url, week,. These elements have special attributes to help the browser to know how to validate its data automatically. Below is list of some such attributes:

| Attribute | Description |
| disabled | Specifies that the Input element should be disabled |
| max | Specifies the maximum value of an Input element |
| min | Specifies the minimum value of an Input element |
| pattern | Specifies the value pattern of an Input element |
| required | Specifies that the Input field requires an element |
| type | Specifies the type of an Input element |

Example: A <input type="number"> with min, max attributes, the browser will notify an user if he/she enters a number beyond the allowed range.

attr-min-max-example.html

| <!DOCTYPE html><html><head><title>Min Max Attributes</title></head><body><h2>Attribute min, max</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html">Enter your score (0-100):<input type="number" name = "score" min= "0" max = "100"/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

| ![](OEBPS/image_rsrc8SE.jpg) |

| ![](OEBPS/image_rsrc8SF.jpg) |

| ![](OEBPS/image_rsrc8SG.jpg) |

Example: Require an user to enter a country code with 2 characters.

attr-pattern-example.html

| <!DOCTYPE html><html><head><title>pattern attribute</title></head><body><h2>Attribute: pattern</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html">Country code:<input type="text" name = "countryCode" pattern="[A-Za-z]{2}"title="Two letter country code"/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

| ![](OEBPS/image_rsrc8SH.jpg) |

| ![](OEBPS/image_rsrc8SJ.jpg) |

| ![](OEBPS/image_rsrc8SK.jpg) |

| ![](OEBPS/image_rsrc8SM.jpg) |

Example: Ask an user to enter a password having at least 8 characters.

attr-pattern-example2.html

| <!DOCTYPE html><html><head><title>pattern attribute</title></head><body><h2>Attribute: pattern</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html">Password:<input type="password" name = "password" pattern=".{8,}"title="8 or more characters"/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

| ![](OEBPS/image_rsrc8SN.jpg) |

| ![](OEBPS/image_rsrc8SP.jpg) |

Example: Ask an user to enter a strong password, having at least 8 characters, at least one uppercase, and at least one lowercase.

attr-pattern-password-example.html

| <!DOCTYPE html><html><head><title>pattern attribute</title></head><body><h2>Attribute: pattern</h2>Password must contain 8 or more characters that are of at least one number,and one uppercase and lowercase letter:<br/><br/><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html">Password:<input type="password" name = "password"pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}"title="Invalid password!"/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

Example: Ask an user to enter an email address, use the pattern attribute to ensure that the user enters an email in the correct format.

attr-pattern-email-example.html

| <!DOCTYPE html><html><head><title>pattern attribute</title></head><body><h2>Attribute: pattern</h2><div style="border:1px solid #ddd; padding: 5px;"><form name="myForm" action="process-action.html">Email:<input type="password" name = "password"pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$"title="Invalid password!"/><br/><br/><button type="submit">Submit</button></form></div></body></html> |

Chapter 13 :

JavaScript Web Cookies

1  What is Web Cookie

2  Where is Cookie stored

3  See Cookie on browser

4  ECMAScript Cookie

1  What is Web Cookie

As you know, Web browsers and Server communicate each other through HTTP protocol. When you use access to a website from the browser, your request will be sent to the server and the server returns the content to the browser for displaying.

| ![](OEBPS/image_rsrc8SR.jpg) |

Cookie is a technique that helps a website store some information on your computer. It will save the information and traces you have ever accessed to that website.

| ![](OEBPS/image_rsrc8SS.jpg) |

For simplicity, see the following situation:

| ![](OEBPS/image_rsrc8ST.jpg) |

You access to a website that you have not ever visited. Suppose this website supports 2 languages: English, French. Because you have never visited this website before, the default English interface will be displayed. You reset other language such as French to display. The server responds to your request, and it also sends the browser a Cookie containing your preferred language - French.

You turn off the computer and visit this website the next day. When the request is sent to the server, the Cookies saved on your computer will be sent with the request, which will help the server determine your preferred language and return the content in such language.

What is Web Cookie

*   Cookie means a small piece of text, generated by the Web Server sent to your browser. The Cookie can be stored on memory or as files on a user's computer. Cookies may also be generated by Javascript running on your browser.
*   Cookies stored on the client side will be included with the request every time when a user accesses any page of that website.

The main information of Cookie is a pair of Name/Value; for example:

| SessionID = AAA22311languagePreference = FRheaderColor = BLUE |

| ![](OEBPS/image_rsrc8SU.jpg) |

Cookie used in e-commerce websites. Users buy goods on this website. The commodities bought by users are stored on a Cart. In the first access, the buyer (Browser) will receive a unique SessionId (not coinciding with other users).

Each SesionId is attached to a cart managed on Web Server. The SessionId/Value information piece is a Cookie stored on the user's computer. Each time a user creates a new request, this Cookie is always attached to the request, which helps the Web Server distinguish different users.

What does a Cookie include

A Cookie means a simple data record transmitted from the browser to the Web Server and vice versa, it has the structure as follows:

| SSID=Ap4P…GTEq; Domain=amazon.com; Path=/; Expires=Wed, 13 Jan 2023 22:23:01 GMT; Secure;HSID=AYQEVn…DKrdst; Domain=.amazon.com; Path=/; Expires=Wed, 13 Jan 2023 22:23:01 GMT; HttpOnlyHSID=AYQEVn…DKrdst; Domain=amazon.com; Path=/; Max-Age=300; HttpOnly |

| Attribute | Meaning |
| Name=Value | Name of Cookie and its value |
| Domain | Domain Name of website. |
| Expires | Specify date and time when this Cookie expires. If Cookie cannot set Expires & Max-Age, it will expire immediately after the user exits the browser. |
| Max-Age | The time is calculated in seconds when this Cookie will exist since it is created. If Cookie has both Expires & Max-Age information then Max-Age will be given priority. |
| Path | This is the path to a directory or a page that set this Cookie. It can be blank if you want to access this Cookie at every directory or every page. |
| Secure | If this attribute is available, i.e. only secured servers can access this Cookie |
| HttpOnly | If this attribute is available, i.e. this Cookie can be only manipulated at the Server side, but it is impossible to manipulate with this Cookie by Javascript on the browser. |

2  Where is Cookie stored

Cookies can be stored on memory or on files. In this section, I mention only Cookies stored in files on the user's computer.

IE (Internet Explorer)

With the IE browser, Cookies of the samewebsite are stored in the same file. and you can find them in the directory like below:

C:\Users\{CurrentUser}\AppData\Roaming\Microsoft\Windows\Cookies

3  See Cookie on browser

Seeing the Cookie on the browser is very simple, for example, with the Chrome browser:

| ![](OEBPS/image_rsrc8SV.jpg) |

4  ECMAScript Cookie

Basically, there are 2 ways for you to work with Cookies:

*   Manipulate Cookies at the Server.
*   Manipulate Cookies by Javascript running on user's browser

In the user's browser, using Javascript (ECMAScript) , you can manipulate with the Cookies without HttpOnly attribute.

Below is an example handling Cookie using the Javascript.

cookie-example.html

| <!DOCTYPE html><html><head><meta charset="UTF-8"><title>Cookie example</title><script type="text/javascript" src="cookie-example.js"></script></head><body onload="readCookie()">Your Name: <input type="text" name="fullName" id="fullName" /><br/>Fovorite Color:<select name="favoriteColor" id="favoriteColor"><option value="red">Red</option><option value="blue">Blue</option><option value="green">Green</option></select><br><button onclick="writeCookies()">Write Cookies</button><button onclick="killCookies()">Kill Cookies</button><br/><br/><!--  Read Cookie Results: --><hr />Read Cookie Results:<div id="logArea" style="border:1px solid #ccc;padding: 5px;height:150px;"></div><button  value = "Get Cookie" onclick = "readCookie()">Read cookies</button></body></html> |

cookie-example.js

| // maxAge: Secondsfunction writeCookies(maxAge) {let expires = new Date();expires.setSeconds(expires.getSeconds() + maxAge);let selectedColor = document.getElementById("favoriteColor").value;let cookie1 = "favoriteColor=" + selectedColor + ";";cookie1 += "Expires=" + expires.toUTCString() + ";";cookie1 += "Path=/"; // Path: Required in Chrome!!// Write Cookie 1document.cookie = cookie1;let fullName = document.getElementById("fullName").value;let cookie2 = "fullName=" + fullName + ";";cookie2 += "Max-Age=" + maxAge + ";"; // Secondscookie2 += "Path=/"; // Path: Required in Chrome!!// Write Cookie 2document.cookie = cookie2;alert("Write Successful!");}function killCookies() {writeCookies(0);}function readCookie() {var allCookies = document.cookie;let logText = "All Cookies : " + allCookies + "<br/>";// Get all the cookies pairs in an arraylet cookieArray = allCookies.split(';');// Now take key value pair out of this arrayfor (var i = 0; i < cookieArray.length; i++) {let kvArray = cookieArray[i].split('=');logText += "Cookie name: " + kvArray[0] + "<br/>";logText += "Cookie value: " + kvArray[1] + "<br/>";}document.getElementById("logArea").innerHTML = logText;} |

You can test this example by running cookie-example.html directly on Firefox. With Chrome browser, you have to run this file on a HTTP Server.

http://localhost:8080/cookies/cookie-example.html

| ![](OEBPS/image_rsrc8SW.jpg) |

Enter a name and select your favorite color on the Form, then press the "Write Cookies" button. Cookies will be generated and saved into the user's computer.

| ![](OEBPS/image_rsrc8SX.jpg) |

| ![](OEBPS/image_rsrc8SY.jpg) |

| ![](OEBPS/image_rsrc8SZ.jpg) |

Chapter 14 :

JavaScript void Keyword

1  Void Keyword

2  Void and JavaScript URIs

3  One-time use function

1  Void Keyword

void is an important keyword in ECMAScript. It has the following characteristics:

*   void acts as an operator, standing before a single operand with any type.
*   void is used to evaluate an expression. It will not return any value, or in other words it returns undefined value.

The void operator precedes any expression to get an undefined value

void-expression-example.js

| void console.log("Test1");  // Test1console.log( void ("Test2") ); // undefinedconsole.log( void (2 == "2") );  // undefinedconsole.log( void (2) == "2" ); // falseconsole.log( void (2) == undefined); // true |

2  Void and JavaScript URIs

<a href ="javascript:URI">..</a> is common in HTML. Browsers will evaluate the URI and take the value returned by the URI to replace the content on the current page.

| ![](OEBPS/image_rsrc8T0.jpg) |

| ![](OEBPS/image_rsrc8T1.jpg) |

| ![](OEBPS/image_rsrc8T2.jpg) |

href-javascript-example.html

| <!DOCTYPE html><html><head><meta charset="UTF-8"><title>Href Javascript</title><script>function getHtmlContentToShow()  {console.log("Do something here...");alert("Do something here...");// Return new HTML content to replace current Page.return "<h1 style='color:red;'>Other HTML Content!</h1>";}</script></head><body><h1>Href:javascript example</h1><a href="javascript:getHtmlContentToShow()">Click me!</a></body></html> |

If the URI returns undefined the browser will not replace the content of the current page.

href-javascript-void-example.html

| <!DOCTYPE html><html><head><meta charset="UTF-8"><title>Href Javascript Void</title><script>function getHtmlContentToShow()  {console.log("Do something here...");alert("Do something here..");// Return new HTML content to replace current Page.return "<h1 style='color:red;'>Other HTML Content!</h1>";}</script></head><body><h1>Href:javascript void example</h1><a href="javascript:void getHtmlContentToShow()">Click me!</a></body></html> |

3  One-time use function

Normally, you need to define a function and then call it.

function-example.js

| // Defind a functionfunction sayHello()  {console.log("Hello Everyone");}// Call functionsayHello(); |

The following example shows you how to create a function only for one time use purpose. It is called immediately. You will not be able to use this function anywhere else in the program because it does not exist after being used.

used-once-function-example.js

| // Defind a function, and call it.(function sayHello()  {console.log("Hello Everyone");}) ();try  {// This function does not exist.sayHello();}catch(e)  {console.log(e); // ReferenceError: sayHello is not defined} |

You can also create a function to use only one time with the void keyword. It is called immediately, and no longer exists after being called.

void-function-example.js

| // Defind a function, and call it.void function sayHello()  {console.log("Hello Everyone");}();try  {// This function does not exist.sayHello();}catch(e)  {console.log(e); // ReferenceError: sayHello is not defined} |

Chapter 15 :

Classes and Objects

1  Your First Class

2  Getter & Setter

3  Static Field

4  Static method

5  Object Comparison operators

1  Your First Class

Below, I have a Rectangle, which has 2 important properties such as width and height. We will define a class named Rectangle to simulate it with the ES6 syntax.

| ![](OEBPS/image_rsrc8T3.jpg) |

Create a resource file rectangle.js:

rectangle.js

| // Define a class.class Rectangle  {// Contructor with 2 parameters.// (Used to create instance)// this.width refers to the width property of the classconstructor (width = 5 , height = 10)  {this.width = width;this.height = height;}// A method calculates the area of the rectangle.getArea() {var area = this.width * this.heightreturn area}}// Create an object of Rectangle via Constructor.var rect = new Rectangle(3, 5);console.log("Height "+ rect.height);console.log("Width "+ rect.width);// Call methodlet area = rect.getArea();console.log("Area "+ area ); |

Running the example:

Output

| Height 5Width 3Area 15 |

What will happen when you create an object from the constructor of the class

| ![](OEBPS/image_rsrc8T4.jpg) |

When you call the Constructor of class, a new object will be created and the properties of the object will be assigned values from parameters.

In the ECMAScript, each class has at most only one constructor. Like a function, the parameters of the constructor can also have a default value. So you can create objects in different ways.

| // width = 3, height = 5let rect = new Rectangle(3, 5);// width = 15, height = 10 (Default)let rect2 = new Rectangle(15);// width = 5 (Default), height = 50let rect3 = new Rectangle(undefined, 50);// width = 5 (Default), height = 10 (Default)let rect4 = new Rectangle(); |

2  Getter & Setter

Before giving the concepts of Getter & Setter, let's analyze a situation:

Assume that we have a Person class and this class has a property which is name.

Class Person

| class Person  {constructor(name) {this.name = name;}} |

And you can access the properties of the object, or assign a new value to it without having any problems.

| // Create an objectlet person = new Person("Tom");// Access to property name.console.log( person.name); // Tom// Assign new value to property name.person.name = "Jerry"; // !!!console.log( person.name ); // Jerry |

Accessing freely to a property and changing its value from the outside of the class are really dangerous. Sometimes, you want to have a property that it is not possible to access, or assign a new value to from the outside of the class. Getter/Setter allows you to create such a property.

Okay, we write the Person class again. get keyword put in front of a method without the class parameters helps create a property with the name which is the method name. This method will be called every time when the program accesses this property.

getter-example1.js

| class Person  { |

| constructor (name)  {// property: __namethis.__name = name;}// Getter of property nameget name()  {console.log("Call getter of property 'name'!!");return this.__name;}}// ------------ TEST -----------------let person = new Person("Tom");// Access to property 'name' ==> Call getterconsole.log( person.name); // Tom// Assign new value to property name.person.name = "Jerry"; // Not Working!!!!// Access to property 'name' ==> Call getterconsole.log( person.name); // Tom |

set keyword put in front of a method with one parameter of class helps create a property with the name which is the method name. This method will be called everytime the program assigns a new value to this property.

setter-example1.js

| class Person  {constructor (name)  {// property: __namethis.__name = name;}// Setter of property nameset name(newName)  {console.log("Call setter of property 'name'!!");this.__name = newName;}// A methodshowInfo()  {console.log("Person: " + this.__name);}}// ------------ TEST -----------------let person = new Person("Tom");// Can not access to property 'name'console.log( person.name); // undefined// Set new value to property 'name' ==> Call setterperson.name = "Jerry";person.showInfo(); // Person: Tom |

Example of a property with Getter & Setter:

getter-setter-example.js

| class Rectangle  {constructor (width = 5 , height = 10)  {this.__width = width;this.height = height;}// Getter of property 'width'get width()  {return this.__width;}// Setter of property 'width'set width(newWidth)  {if(newWidth > 0) {this.__width = newWidth;} else {console.log("Invalid width " + newWidth);}}}// ------------ TEST ------------------var rect = new Rectangle(3, 5);console.log("Height "+ rect.height); // Height: 5console.log("Width "+ rect.width); // Width: 3rect.width = -100;console.log("Height "+ rect.height); // Height: 5console.log("Width "+ rect.width); // Width: 3rect.width = 100;console.log("Height "+ rect.height); // Height: 5console.log("Width "+ rect.width); // Width: 100 |

Output

| Height 5Width 3Invalid width -100Height 5Width 3Height 5Width 100 |

Private property

| class Something {constructor(){this.#someProperty = "test";}}const instance = new Something();console.log(instance.#someProperty); // undefined |

getter-example2.js

| class Person  {constructor (name)  {// Private property: #namethis.#name = name;}// Getter of property nameget name()  {console.log("Call getter of property 'name'!!");return this.#name;}} |

3  Static Field

The static keyword appears in the Getter or Setter declarations to help you define a static field. You can access static fields through a class name.

static fields with fixed value (unchangeable) are called constant static fields.

static-field-example1.js

| class Employee {constructor (fullName, age)  {this.fullName = fullName;if(age < Employee.MIN_AGE &#124;&#124; age > Employee.MAX_AGE)  {throw "Invalid Age " + age;}this.age = age;}// A static field: MIN_AGEstatic get MIN_AGE() {return 18;}// A static field: MAX_AGEstatic get MAX_AGE() {if(!Employee.__MAXA)  {Employee.__MAXA = 60;}return Employee.__MAXA;}static set MAX_AGE(newMaxAge)  {Employee.__MAXA = newMaxAge;}}// ---- TEST ---------console.log("Mininum Age Allowed: " + Employee.MIN_AGE);console.log("Maximum Age Allowed: " + Employee.MAX_AGE);// Set new Maximum Age:Employee.MAX_AGE = 65;console.log("Maximum Age Allowed: " + Employee.MAX_AGE);let baby = new Employee("Some Baby", 1); // Error!! |

You have another way for declaring a static field for a class, however, static fields created by this way will not be a Constant because its value can change. Below is an example:

static-field-example2.js

| class Employee {constructor (fullName, age)  {this.fullName = fullName;if(age < Employee.MIN_AGE &#124;&#124; age > Employee.MAX_AGE)  {throw "Invalid Age " + age;}this.age = age;}}Employee.MIN_AGE = 18;Employee.MAX_AGE = 60;// ---- TEST ---------console.log("Mininum Age Allowed: " + Employee.MIN_AGE);console.log("Maximum Age Allowed: " + Employee.MAX_AGE);// Set new Maximum Age:Employee.MAX_AGE = 65;console.log("Maximum Age Allowed: " + Employee.MAX_AGE);let baby = new Employee("Some Baby", 1); // Error!! |

4  Static method

The Static keyword which appears in declaration of a class method helps you define a static method. You can call static methods through the class name. Static methods can not be called through the object of the class. A static method is often used as an utility function of an application.

| ![](OEBPS/image_rsrc8T5.jpg) |

point.js

| class Point {constructor(x, y) {this.x = x;this.y = y;}// Calulatesthe distance between 2 pointsstatic distance( point1, point2) {const dx = point1.x - point2.x;const dy = point1.y - point2.y;return Math.hypot(dx, dy);}}// --- TEST ---let point1 = new Point( 5, 10);let point2 = new Point( 15, 20);// Distancelet d = Point.distance(point1, point2);console.log("Distance between 2 points: " + d); |

Output

| Distance between 2 points: 14.142135623730951 |

5  Object Comparison operators

In ECMAScript, when you create an object through constructor will be a real entity is created in memory, it has a specified address.

An operator assigned AA object by an BB object does not create new entity on the memory, it's just pointing to address of AA to BB's address.

| ![](OEBPS/image_rsrc8T6.jpg) |

=== Operator used to compare two objects that is pointing to, it returns true if the two objects refer to the same address in memory. Operators !== is used to compare the two addresses of two objects that is pointing to, it returns true if the two objects that point to two different addresses.

identify-operator-example.js

| // Define a class.class Rectangle  {constructor (width = 5 , height = 10)  {this.width = width;this.height = height;}getArea() {var area = this.width * this.height;return area;}}// Create object: r1let r1 = new Rectangle( 20,  10);// Create object: r2let r2 = new Rectangle( 20, 10);let r3 = r1;let  b12  =   r1 === r2; // falselet  b13  =   r1 === r3; // trueconsole.log("r1 === r2 ? " + b12); // falseconsole.log("r1 === r3 ? " + b13); // truevar bb12  = r1 !== r2; // truevar bb13  = r1 !== r3; // falseconsole.log("r1 !== r2 ? " + bb12); // trueconsole.log("r1 !== r3 ? " + bb13); // false |

Running the example:

Output

| r1 === r2 ? falser1 === r3 ? truer1 !== r2 ? truer1 !== r3 ? false |

Chapter 16 :

Class and inheritance

1  Class in Javascript

2  Class and inheritance in ES3

3  Class and Inheritance in ES5

1  Class in Javascript

Javascript means in fact a world of functions and objects. It is originally designed simply, with no clear concept of classes. Perhaps, the Javascript creators cannot think that one day this language is used so widely.

The object in Javascript means an entity with multiple "Key/Value" pairs, and you can access values via objects and keys.

object-example1.js

| var tom =  {name: "Tom",country: "USA"};// Access:console.log( tom.name ); // Tomconsole.log( tom.country ); // USAconsole.log( tom["name"] ); // Tomconsole.log( tom["country"] ); // USA |

You can add new "Key/Value" pairs to an available object or remove its "Key/Value" pairs

object-example2.js

| var tom =  {name: "Tom",country: "USA"};// Delete property - countrydelete tom["country"]; // Same as: delete tom.country;// Add property - gendertom["gender"] = "Male"; // Same as: tom.gender = "Male";// Access:console.log( tom.name ); // Tomconsole.log( tom["name"] ); // Tomconsole.log( tom["country"] ); // undefinedconsole.log( tom.country ); // undefinedconsole.log( tom["gender"] ); // Maleconsole.log( tom.gender ); // Male |

First of all, for simplification, see a modern syntax introduced in ECMAScript 6 to create the Rectangle class, with 2 properties such as width and height . This class has a getArea() method that returns the area of this rectangle.

| ![](OEBPS/image_rsrc8T7.jpg) |

es6-class-example.js

| // ECMAScript 6 class:class Rectangle  {constructor (width , height)  {this.width = width;this.height = height;}getArea()  {return this.width * this.height;}}// ------------- TEST -------------------var rect = new Rectangle(10, 5);var area = rect.getArea();console.log("Width: " + rect.width);console.log("Height: " + rect.height);console.log("Area: " + area); |

Creating a subclass of a class is very simple with ES6:

es6-inheritance-example.js

| class Shape  {constructor( x, y) {this.setLocation(x, y);}setLocation(x, y) {this.x = x;this.y = y;}}// Subclass:class Circle extends Shape {constructor(x, y, radius) {// Call Shape's constructor via supersuper(x, y);this.radius = radius;}getArea() {return Math.PI * this.radius * this.radius;}}// ----- TEST ----var circle = new Circle(0, 2, 5);console.log( circle.getArea() ); |

2  Class and inheritance in ES3

ES3 uses the function keyword to define a "object constructor". You will create a new object when you call this function with the new operator:

| // ECMAScript 3 class.function Rectangle(width, height)  {this.width = width;this.height = height;}// Create an Object:var rect = new Rectangle(10, 5); |

The following figure illustrates the action performed by the Javascript executing machine:

| ![](OEBPS/image_rsrc8T8.jpg) |

*   The 'rect' object is created (it's just a normal object. Nothing is special)
*   Add property __proto__ for the 'rect' object. This is a hidden property.
*   This variable will be pointed to the address of the 'rect' object.
*   Add the width property to the "rect' object.
*   Add the height property for 'rect' object.

Prototype concepts are also introduced in ES3. Let's see what is its purpose?

| / ECMAScript 3 class.function Rectangle(width, height)  {this.width = width;this.height = height;}Rectangle.prototype.bgColor = "red";Rectangle.prototype.borderColor = "blue";// Create an Object:var rect = new Rectangle(10, 5);console.log(rect); // Rectangle { width: 10, height: 5 }console.log(rect.__proto__); // Rectangle { bgColor: 'red',borderColor: 'blue' }console.log(rect.__proto__.bgColor); // redconsole.log(rect.__proto__.borderColor); // blue// (Read the explanation**)console.log(rect.bgColor); // redconsole.log(rect.borderColor); // blue |

| ![](OEBPS/image_rsrc8T9.jpg) |

What happens when the JavaScript runtime encounters the myObject.myProperty expression.

The answer is that it will check if the myObject object has myProperty property or not. If any, it accesses to this property, vice versa it accesses myObject.__proto__.myProperty.

es3-proto-example3.js

| var rect =  {__proto__ : { bgColor : "red", borderColor : "blue" },width: 10,height: 5}console.log(rect.width); // 10console.log(rect.__proto__.bgColor); // redconsole.log(rect.bgColor); // red |

new AFunction(args) vs AFunction.call(anObj, args)

| ![](OEBPS/image_rsrc8TA.jpg) |

Inheritance

For ES3, you can simulate a class that inherits another class in many different ways, certainly, it's not as easy as you do in ES6, and it's quite confusing for many programmers.

For simplicity, I give an example of inheritance, and analyze the operating rule of the Javascript runtime n this case.

*   The Animal class has the 2 name & gender properties.
*   The Cat class inherits from the Animal class. It has 1 color property.

| ![](OEBPS/image_rsrc8TB.jpg) |

es3-inheritance-example1.js

| function Animal(n, g) {this.name = n;this.gender = g;}function Cat(n, g, c) {Animal.call(this, n, g);this.color = c;}var tom = new Cat("Male", "Tom", "Black");// Cat { gender: 'Male', name: 'Tom', color: 'Black' }console.log(tom); |

| ![](OEBPS/image_rsrc8TC.jpg) |

Inheritance and role of prototype (ES3)

es3-inheritance-example2.js

| // Class: Animalfunction Animal(n, g) {this.name = n;this.gender = g;}Animal.prototype.sleep = function()  {console.log("Animal sleeping..");}Animal.prototype.move = function()  {console.log("Animal moving..");}// Class: Catfunction Cat(n, g, c) {Animal.call(this, n, g); // IMPORTANT!!this.color = c;}// IMPORTANT!!var TempFunc = function() {}; // Temporary class.TempFunc.prototype = Animal.prototype;Cat.prototype = new TempFunc();// ------------------Cat.prototype.cry = function()  {console.log("Meo meo");}// Override 'move' method of Animal.Cat.prototype.move = function() {console.log("Cat moving..");}var tom = new Cat("Male", "Tom", "Black");// Cat { gender: 'Male', name: 'Tom', color: 'Black' }console.log(tom);tom.move(); // Cat moving..tom.sleep(); // Animal sleeping..tom.cry(); // Meo meo |

3  Class and Inheritance in ES5

Object.create(srcObject)

The Object.create(srcObject) method creates a new newObject object, in which newObject.__proto__ is copy of srcObject.

| ![](OEBPS/image_rsrc8TD.jpg) |

method-object-create-example.js

| var john = {name: "John",gender: "Male"};var other = Object.create(john);console.log(other.__proto__); // { name: 'John', gender: 'Male' } |

Inheritance (ES5 + Object.create)

Using the Object.create(srcObject) method of ES5 helps you simulate class and inheritance more easily than ES3.

es5-inheritance-example1.js

| // Class: Animalfunction Animal(n, g) {this.name = n;this.gender = g;}Animal.prototype.sleep = function()  {console.log("Animal sleeping..");}Animal.prototype.move = function()  {console.log("Animal moving..");}// Class: Catfunction Cat(n, g, c) {Animal.call(this, n, g); // IMPORTANT!!this.color = c;}Cat.prototype = Object.create(Animal.prototype); // IMPORTANT!!Cat.prototype.cry = function()  {console.log("Meo meo");}// Override 'move' method of Animal.Cat.prototype.move = function() {console.log("Cat moving..");}var tom = new Cat("Male", "Tom", "Black");// Cat { gender: 'Male', name: 'Tom', color: 'Black' }console.log(tom);tom.move(); // Cat moving..tom.sleep(); // Animal sleeping..tom.cry(); // Meo meo |

Chapter 17 :

Inheritance and polymorphism

1  Inheritance in ECMAScript

2  Override method

3  Abstract Method

4  Operators - instanceof, typeof

5  Polymorphism with function

1  Inheritance in ECMAScript

ECMAScript allows you to create a class extended from one or more other classes. This class is called a derived class, or a subclass.

A child class will inherit properties, methods, and other members from a parent class. It can also override methods from the parent class. In ECMAScript, each class has only one constructor. If a class itself does not define its own constructor, it inherits the constructor of the parent class. Contrarily, if the child class defines a constructor, it will not inherit the constructor of the parent class.

We need a few classes to participate in examples.

*   Animal: Class simulate an animal.
*   Duck: Subclass of Animal.
*   Cat: Subclass of Animal.
*   Mouse: Subclass of Animal.

| ![](OEBPS/image_rsrc8TE.jpg) |

In ECMAScript, constructor of class used to create an object (instance), and assign the value for the properties. Constructor of subclasses always called to a constructor of parent class to initialize value for the properties in the parent class, then it assign value for its properties.

Example:

Cat is the class that inherits from the Animal class, it also has its properties.

inherit-example1.js

| class Animal {constructor(name)  {this.name = name;}showInfo()  {console.log("I'm " + this.name);}move()  {console.log("Moving..");}}class Cat extends Animal {constructor(name, age, height) {super(name);// Cat's properties:this.age = age;this.height = height;}// Override method of parent class.showInfo()  {console.log("My name is " + this.name);}// Other method...sleep()  {console.log("Sleeping..");}}// ------------- TEST --------------------let tom = new Cat("Tom", 3, 20);console.log("Call move() method");tom.move();console.log("\n");console.log("Call showInfo() method");tom.showInfo(); |

Output

| Call move() methodMoving..Call showInfo() methodMy name is Tom |

What's happened when you create an object from constructor . How does it call up a constructor of the parent class? Please see the illustration below:

| ![](OEBPS/image_rsrc8TF.jpg) |

With the above illustration you see that, constructor of parent class is called in constructor of subclass, it will assign values to the properties of the parent class, then the properties of the subclass.

2  Override method

By default, child classes inherit methods from the parent class, but parent classes can override the method of the parent class.

inheritance-example2.js

| class Animal {constructor(name)  {this.name = name;}showInfo()  {console.log("I'm " + this.name);}move()  {console.log("Moving..");}}class Mouse extends Animal {constructor(name, age, height) {super(name);this.age = age;this.height = height;}// Override method of parent class.showInfo()  {// Call showInfo() method of parent class.super.showInfo();console.log ("Age: " + this.age);console.log ("Height: " + this.height);}// Override method of parent class.move()  {console.log("Mouse Moving..");}}// ------------- TEST --------------------let jerry = new Mouse("Jerry", 3, 5);console.log("Call move() method");jerry.move();console.log("\n");console.log("Call showInfo() method");jerry.showInfo(); |

Output

| Call move() methodMouse Moving..Call showInfo() methodI'm JerryAge: 3Height: 5 |

3  Abstract Method

The concept of an abstract method or abstract class is defined in languages such as Java, C#. But it is not clearly defined in ECMAScript. However, we have a way to define it.

A class called as abstract defines abstract methods and child class must override these methods if you want to use them. The abstract methods always throw the exception "Not Implemented Error".

abstract-example.js

| // An abstract class.class AbstractDocument {constructor(name) {this.name = name}// A method can not be used, because it always throws an error.show() {// Not Implemented Errorthrow "Subclass must implement abstract method";}}class PDF extends AbstractDocument {// Override method of parent classshow() {console.log("Show PDF document:", this.name);}}class Word extends AbstractDocument {show() {console.log("Show Word document:", this.name)}}// -------------------- TEST -------------------------let doc1 = new PDF("Python tutorial");let doc2 = new Word("Java IO Tutorial");let doc3 = new PDF("ECMAScript Date & Time Tutorial");let documents = [doc1, doc2, doc3];for (let i = 0; i < documents.length; i++) {documents[i].show();}let doc4 = new AbstractDocument("An Abstract Document");doc4.show(); // Throw Error!!! |

4  Operators - instanceof, typeof

instanceof

The instanceof operator helps you to check whether "something" is an object of a certain class or not.

instanceof-example.js

| class Person {}// A Child class of Personclass AsianPerson extends Person {}class Triangle {}let person = new Person();let asianPerson = new AsianPerson();let triangle = new Triangle();let isPerson = person instanceof Person;console.log( isPerson ); // trueconsole.log( asianPerson instanceof Person ); // trueconsole.log( person instanceof AsianPerson ); // falseconsole.log( triangle instanceof Person ); // falseconsole.log( triangle instanceof AsianPerson ); // false |

typeof

The typeof operator is used to check the type of "something". The result obtained is the name of the type.

typeof-example.js

| // A Class:class Person {}// An Object:let person = new Person();console.log( typeof Person ); // functionconsole.log( typeof person ); // object// null:console.log( typeof null ); // object// A Number:let intValue = 100;console.log( typeof intValue ); // number// NaN (Not a Number)console.log( typeof NaN); // number// A Stringlet strValue = "Hello";console.log( typeof strValue ); // string// A Boolean:let boolValue = true;console.log( typeof boolValue ); // boolean// undefinedconsole.log( typeof undefined); // undefined// An Arraylet years = [1980, 2003, 2018];console.log( typeof years ); // object// A Functionlet myFunc = function()  {}console.log( typeof myFunc ); // function// A Symbollet mySymbol =   Symbol();console.log( typeof mySymbol ); // symbol |

Is Sub Class

Suppose you have two classes, A & B. The following example helps you check whether A is a child class of B or not.

let isChild = A === B || A.prototype instanceof B;

issubclass-example.js

| class Animal {}class Cat extends Animal {}class AsianCat extends Cat {}// ------------- TEST --------------------console.log("AsianCat === Animal? " + (AsianCat === Animal)); // falselet isSubClass1 = AsianCat === Animal &#124;&#124; AsianCat.prototype instanceof Animal;console.log("AsianCat is child of Animal? " + isSubClass1); // truelet isSubClass2 = AsianCat === Animal &#124;&#124; Animal.prototype instanceof AsianCat;console.log("Animal is child of AsianCat? " + isSubClass2); // false |

Output

| isinstance('abc', object): Trueininstance(123, object): Trueb = B()a = A()isinstance(b, A): Trueisinstance(b, B): Trueisinstance(a, B): Falseisinstance(B, A): Trueisinstance(A, B): False |

5  Polymorphism with function

Here I create two classes such as English and French. Both of the classes have the greeting() method. Both create different greetings. Create two corresponding objects from the two classes above and call the actions of these two objects in the same function (intro function).

polymorphism-example.js

| class English {greeting() {console.log("Hello");}}class French {greeting() {console.log("Bonjour");}}function intro(language) {language.greeting();}// -------------- TEST ----------------------let flora = new English();let aalase = new French();// Call function:intro(flora);intro(aalase);let someObject = {};intro(someObject);// Error!!! |

OK, Correct the code of the above example, add necessary checks to avoid risks for your application:

polymorphism-example2.js

| class English {greeting() {console.log("Hello");}}class French {greeting() {console.log("Bonjour");}}function intro(language) {// Check type of 'language' object.if(language instanceof English &#124;&#124; language instanceof French)  {language.greeting();}}// -------------- TEST ----------------------let flora = new English();let aalase = new French();// Call function:intro(flora);intro(aalase);let someObject = {};intro(someObject); |

Applying the "Classes & Inheritance" architecture helps your application be easier to be managed and avoid errors.

polymorphism-example3.js

| // A Base classclass Language {}class English extends Language {greeting() {console.log("Hello");}}class French  extends Language {greeting() {console.log("Bonjour");}}function intro(language) {// Check type of 'language' object.if(language instanceof Language)  {language.greeting();}}// -------------- TEST ----------------------let flora = new English();let aalase = new French();// Call function:intro(flora);intro(aalase);let someObject = {};intro(someObject); |

Chapter 18 :

JavaScript Set Collection

1  Collections - Set

2  The methods of Set

3  WeakSet

1  Collections - Set

ECMAScript 6 introduces the 2 new data structures such as Map & Set. They are part of ECMAScript Collections Framework).

Maps - This data structure allows you to store the "Key/Value". And you can access the value through the key or update a new value corresponding to a key.

Sets - This data structure stores a list of elements not allowing duplicate, and not indexing elements.

In this post, I will introduce the Set to you.

Set

The Set is a data structure introduced in the ECMAScript6. The following is Set characteristics.

*   Set is a list of elements not allowing iteration.
*   Set doesn't index elements.
*   Set is an ordered list, which means that an element which is added first will come first and an element that is added second will come second.

Constructors:

Create Set object through the constructor of the Set: class

| new Set( [iterable] ) |

Parameters:

*   iterable - If this object is passed to the constructor of the Set, all its elements will be added to the Set. On the contrary, if you don't specify this parameter, or its value is null, the Set object created will be empty.

Properties:

set-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' } |

set-size-example.js

| // Create a Set from an Arrayvar fruits = new Set( ['Apple','Banana','Papaya'] );var size = fruits.size;console.log(size); // 3 |

for..of

You can use the for...of loop to loop through elements of Set.

set-for-of-loop-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );for(let fruit of fruits)  {console.log(fruit);} |

Output

| AppleBananaPapaya |

2  The methods of Set

add(value)

Add an element to the end of Set if this element doesn't exists in Set and return this Set object.

set-add-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );// Append an Element to the Set and returns this Set.var thisFruits = fruits.add("Cherry");console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya', 'Cherry' }// 'Set' does not allow duplicatesfruits.add("Banana");console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya', 'Cherry' } |

Output

| Set { 'Apple', 'Banana', 'Papaya', 'Cherry' }Set { 'Apple', 'Banana', 'Papaya', 'Cherry' } |

delete(value)

This method is used to remove an element out of the Set. The method returns true if it finds an element to be removed and on the contrary, it returns false.

set-delete-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }// Delete an element:var deleted = fruits.delete("Banana");console.log("Deleted? " + deleted); // trueconsole.log(fruits); // Set { 'Apple', 'Papaya' } |

clear()

Remove all elements out of Set.

set-clear-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }// Remove all elements.fruits.clear();console.log(fruits); // Set { }console.log("Size after clear: " + fruits.size); |

entries()

This method returns a new Iterator object of which each entry contains an array with the 2 elements such as [value, value]. The order of entries still be kept unchanged like the order of elements in the Set object. (See the following illustration)

| ![](OEBPS/image_rsrc8TG.jpg) |

set-entries-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }// Iterator Object:var iteratorEntries = fruits.entries();var entry;while( !(entry = iteratorEntries.next() ).done )  {console.log(entry.value); // [ 'Apple', 'Apple' ]} |

has(value)

This method tests whether a value given by a parameter exists in Set or not. Return true if existing, on the contrary, return false.

set-has-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );var has = fruits.has("Banana");console.log(has); // true |

forEach(callbackFn[, thisArg])

This method will call the callbackFn function one time for each element of Set.

| mySet.forEach(callbackFn [, thisArg]) |

Parameters:

*   callbackFn - This function will be called one time corresponding to each element of the Set object.
*   thisArg - Parameter that is used as this when executing the callbackFn function.

set-forEach-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }function showFruit(fruit, thisSet) {console.log("Fruit: " + fruit);}// Or Call: fruits.forEach(showFruit);fruits.forEach(showFruit, fruits); |

key() & values()

The key() & values() method returns a new Iterator of which each element has the shape {value: aValue, done: false}.

| ![](OEBPS/image_rsrc8TH.jpg) |

set-values-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );var fruitIterator = fruits.values();var entry;while ( !(entry = fruitIterator.next()).done)  {console.log(entry); // { value: 'Apple', done: false }console.log(entry.value); // Apple} |

Running the example:

Output

| { value: 'Apple', done: false }Apple{ value: 'Banana', done: false }Banana{ value: 'Papaya', done: false }Papaya |

mySet[Symbol.iterator]

Symbol.iterator is a special property of Set. By default, the value of mySet[Symbol.iterator] is the values() method of mySet.

set-symbol-iterator-example.js

| // Create a Set from an Arrayvar fruits = new Set( ["Apple","Banana","Papaya"] );// Same as: fruits.values()var fruitIterator = fruits[Symbol.iterator]();var entry;while ( !(entry = fruitIterator.next()).done)  {console.log(entry); // { value: 'Apple', done: false }console.log(entry.value); // Apple |

3  WeakSet

Basically, the WeakSet is quite the same as Set, but it has the following differences:

*   The WeakSet elements have to be objects, they can not be a primitive type.
*   The WeakSet elements can be removed in the process of Garbage collection, which is an independent process to remove the objects no longer used in the program.
*   WeakSet doesn't support property: size, therefore, you can not know how many elements it has.
*   Many methods may be available in Set class but have no WeakSet, for example, values(), keys(), clear(),..

Create a WeakSet object.

| new Set( [iterable] ) |

Parameters:

*   iterable - If this object is passed to the constructor of the WeakSet, all its elements will be added to the Set. On the contrary, if you don't specify this parameter, or its value is null, the Set object created will be empty.

Methods:

The quantity of WeakSet methods is less than the quantity of Set methods:

*   WeakSet.add(element)
*   WeakSet.delete(element)
*   WeakSet.has(element)

The elements in the WeakSet have to be objects, they can not be primitive types.

| let w = new WeakSet();w.add('a'); // TypeError: Invalid value used in weak setlet s = new Set();s.add('a'); // Works |

weakset-example.js

| var element1 = {}; // An Objectvar element2 = {foo: "bar"};var element3 = {bar: "foo"};var myWeakSet = new WeakSet( [element1, element2] );myWeakSet.add(element3);console.log(myWeakSet.has(element2)); // true |

Chapter 19 :

JavaScript Map Collection

1  Collections - Map

2  Map Methods

3  WeakMap

1  Collections - Map

ECMAScript 6 introduces the 2 new data structures such as Map & Set. They are part of ECMAScript Collections Framework .

*   Maps - This data structure allows you to store "Key/Value" pairs. And you can access the value through the key, or update a new value corresponding to a key.
*   Sets - This data structure stores a list of elements not allowing duplicate and not indexing elements.

Map:

A Map object stores "Key/Value", of which the Key and the Value can be Primitive types or objects.

*   In the Map object, keys are not iterated.
*   The Map is an ordered data type, which means that the "Key/Value" pair which is added first, will come first. the second fair which will come second.

| ![](OEBPS/image_rsrc8TJ.jpg) |

Create a Map object through the constructor of Map class:

| new Map( [iteratorObject] ) |

Parameters:

*   iteratorObject - any object which is iterable.

map-size-example.js

| var myContacts = new Map();myContacts.set("0100-1111", "Tom");myContacts.set("0100-5555", "Jerry");myContacts.set("0100-2222", "Donald");console.log(myContacts.size); // 3 |

for..of

You can use the for..of loop to loop through Map's key/value pairs.

map-for-of-loop-example.js

| / Create a Map object.var myContacts = new Map();myContacts.set("0100-1111", "Tom");myContacts.set("0100-5555", "Jerry");myContacts.set("0100-2222", "Donald");for( let arr of myContacts)  {console.log(arr);console.log(" - Phone: " + arr[0]);console.log(" - Name: " + arr[1]);} |

Running the example:

Output

| [ '0100-1111', 'Tom'  ]- Phone: 0100-1111- Name: Tom[ '0100-5555', 'Jerry'  ]- Phone: 0100-5555- Name: Jerry[ '0100-2222', 'Donald'  ]- Phone: 0100-2222- Name: Donald |

2  Map Methods

set(key, value)

The set(key, newValue) method will add a key/newValue pair to Map object if no pair with such key exists, on the contrary, it will update a new value for the key/value pair found in the Map.

map-set-example.js

| var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);console.log(myContacts);// Add new Key/Value pair to MapmyContacts.set("0100-9999", "Mickey");console.log(myContacts);// UpdatemyContacts.set("0100-5555", "Bugs Bunny");console.log(myContacts); |

Running the example:

Output

| Map {'0100-1111' => 'Tom','0100-5555' => 'Jerry','0100-2222' => 'Donald' }Map {'0100-1111' => 'Tom','0100-5555' => 'Jerry','0100-2222' => 'Donald','0100-9999' => 'Mickey' }Map {'0100-1111' => 'Tom','0100-5555' => 'Bugs Bunny','0100-2222' => 'Donald','0100-9999' => 'Mickey' } |

has(key)

This method tests whether a key exists in the Map or not. It returns true if existing, on the contrary, it returns false.

map-has-example.js

| var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);var has = myContacts.has("0100-5555");console.log("Has key 0100-5555? " + has); // true |

clear()

Remove all "Key/Value" pairs out of the Map object.

map-clear-example.js

| var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);console.log("Size: " + myContacts.size); // 3myContacts.clear();console.log("Size after clearing: " + myContacts.size); // 0 |

delete(key)

Remove a "Key/Value" pair out of the Map object, return true if a pair is removed out of the Map, return false if this key doesn't exist in the Map.

map-delete-example.js

| var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);console.log("Size: " + myContacts.size); // 3var deleted = myContacts.delete("0100-5555");console.log("Deleted? " + deleted); // trueconsole.log("Size after delete: " + myContacts.size); // 2 |

entries()

Return the Iterator, of which each entry contains an array with the 2 elements such as [key, value]. The order of entries is still kept unchanged, like the one of the Key/Value pairs in the Map object. (See the following illustration)

| ![](OEBPS/image_rsrc8TK.jpg) |

map-entries-example.js

| var myContacts = new Map();myContacts.set("0100-1111", "Tom");myContacts.set("0100-5555", "Jerry");myContacts.set("0100-2222", "Donald");var entries = myContacts.entries();var entry;while( !(entry = entries.next()).done )  {var array = entry.value;console.log(array); // [ '0100-1111', 'Tom' ]} |

Running the example:

Output

| [ '0100-1111', 'Tom' ][ '0100-5555', 'Jerry' ][ '0100-2222', 'Donald' ] |

keys()

This method returns a new Iterator object helping you access Map keys.

| ![](OEBPS/image_rsrc8TM.jpg) |

map-keys-example.js

| var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);var iteratorPhones= myContacts.keys();var entry;while( !(entry = iteratorPhones.next()).done )  {var phone = entry.value;console.log(phone); // 0100-1111} |

Running the example:

Output

| 0100-11110100-55550100-2222 |

values()

This method returns a new Iterator object helping you access Map values.

| ![](OEBPS/image_rsrc8TN.jpg) |

map-values-example.js

| var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);var iteratorNames = myContacts.values();var entry;while( !(entry = iteratorNames.next()).done )  {var name = entry.value;console.log(name); // Tom} |

forEach(callbackFn [, thisArg])

This method will call the callbackFn function one time corresponding to each "Key/Value" pair of the Map object.

| myMap.forEach(callback[, thisArg]) |

Parameters:

*   callbackFn -This function will be called one time corresponding to each "Key/Value" pair of the Map object.
*   thisArg - The parameter is used like this when executingcallbackFn.

map-forEach-example.js

| var showContact = function(key, value, thisMap)  {console.log("Phone: " + key +". Name: " + value);}var data = [["0100-1111", "Tom"],["0100-5555", "Jerry"],["0100-2222", "Donald"]];var myContacts = new Map(data);// or call: myContacts.forEach(showContact)myContacts.forEach(showContact, myContacts); |

Running the example:

Output

| Phone: 0100-1111\. Name: TomPhone: 0100-5555\. Name: JerryPhone: 0100-2222\. Name: Donald |

3  WeakMap

Basically, the WeakMap is quite the same as Map, but it has the following differences:

*   Its keys have to be objects
*   The keys of WeakMap can be eliminated in the garbage collection process, which is an independent process to remove objects that are no longer used in the program.
*   WeakMap doesn't support property: size, therefore, you can not how many elements it has.
*   Many methods may be available in the Map class but there is no WeakMap class, for example,values(), keys(), entries(), clear(),..

Create a WeakMap object.

| var map2 = new WeakMap( [iteratorObject] ) |

Parameters:

*   iteratorObject - any object which is iterable.

Methods:

The quantity of WeakMap methods is less than the quantity of the Map methods:

*   WeakMap.delete(key)
*   WeakMap.get(key)
*   WeakMap.has(key)
*   WeakMap.set(key, value)

The keys in the WeakMap have to be an object. It can not be a Primitive type.

| let w = new WeakMap();w.set('a', 'b'); // Uncaught TypeError: Invalid value used as weak map keylet m = new Map();m.set('a', 'b'); // Works |

weakmap-example.js

| var key1 = {}; // An Objectvar key2 = {foo: "bar"};var key3 = {bar: "foo"};var data = [[key1, "Tom"],[key2, "Jerry"],[key3, "Donald"]];var myWeakMap = new WeakMap(data);console.log(myWeakMap.get(key1)); |

Chapter 20 :

Undertanding JavaScript Iterables and Iterators

1  Iteration

2  Concept of Iterator

3  Concept of Iterable

1  Iteration

ECMAScript 6 provides you with a new way to interact with data structure, which is Iteration. Now, we will clarify it.

There are two concepts that you need to distinguish:

*   Iterator
*   Iterable

2  Concept of Iterator

Iterator: An object called Iterator if it contains a pointer to next element in Iteration.

Technically, an object in ECMAScript is called an Iterator if it has a method with the next() name, and this method returns an object with the form {value:SomeValue,done:booleanValue}. done has true value if the Iteration has been completed, otherwise it has false value.

| ![](OEBPS/image_rsrc8TP.jpg) |

iterator-object-example.js

| // An Iterator Object:let myIterator = {someProp: "Some Prop",//next : function()  {return  {value: "Tom",done: false}}}// ----------- TEST -------------------let entry = myIterator.next();console.log(entry); // { value: 'Tom', done: false }console.log(entry.value); // Tom |

3  Concept of Iterable

Iterable - In terms of language, an object is called Iterable if it contains a collection of data, and it provides a way to publicize its data. For example, an array can be called Iterable because it contains a collection of data, and you can access its elements.

Technically, in the ECMAScript, an object that is called Iterable must have a method with the key of Symbol.iterator and this method returns an Iterator object.

object-with-properties.js

| // An Object:let myObject = {// A propertymyProp1 : "Some Value 1",// A property'myProp2' : "Some Value 2",// A property100 : "One hundred",// A property (Method)myProp3 :  function()  {console.log("I'm a method");},// A property (Method)[Symbol.iterator] : function() {console.log("I'm a [Symbol.iterator] method");}}// ----------- TEST --------------console.log( myObject["myProp1"] ); // Some Value 1console.log( myObject["myProp2"] ); // Some Value 2console.log( myObject[100] ); // One hundredmyObject["myProp3"](); // I'm a methodmyObject[Symbol.iterator]();// I'm a [Symbol.iterator] method |

Running the example:

Output

| Some Value 1Some Value 2One hundredI'm a methodI'm a [Symbol.iterator] method |

Iterable

To sum up, an object is called Iterable if it has a method with a Symbol.iterable key, and this method returns an Iterator object.

iterable-object-example.js

| // An Iterator Objectlet myIterator = {next : function()  {return  {value: Math.random(), done: false};}}// A Iterable object:let myIterable = {myProp : "Some value",// A Method returns an Iterator object.[Symbol.iterator] :  function() {return myIterator;}}// ------ TEST -----------// An iterator object.let it = myIterable[Symbol.iterator]();let entry = it.next();console.log(entry);entry = it.next();console.log(entry); |

Running the example:

Output

| { value: 0.6026736348993575, done: false }{ value: 0.1790056262472559, done: false } |

Chapter 21 :

Javascript Menubar

1  window.menubar

The window.menubar property returns a Menubar object representing the menu bar on browser. However, you can hardly interact with Menubar through Javascript because it has very few APIs for you.

| window.menubar// Or simple:menubar |

The tendency of modern browsers is to make the Viewport window as wide as possible, therefore, they remove other components like Statusbar, or made Menubar smaller.

menubar.visible

The menubar.visible property returns true if menu bar is displayed on browser. On the contrary, it returns false.

Note: For modern browsers, you can set new values for menubar.visible. If you do it on purpose, it doesn't work.

| ![](OEBPS/image_rsrc8TR.jpg) |

| ![](OEBPS/image_rsrc8TS.jpg) |

menubar-example.html

| <!DOCTYPE html><html><head><title>Menubar</title><meta charset="UTF-8"></head><body><h3>menubar.visible</h3><br/><br/><button onclick="alert(menubar.visible)">alert(menubar.visible)</button></body></html> |

Example, use window.open(..) to open a new window without menu bar.

| ![](OEBPS/image_rsrc8TT.jpg)![](OEBPS/image_rsrc8TU.jpg)![](OEBPS/image_rsrc8TV.jpg) |

open-new-window-example.html

| <!DOCTYPE html><html><head><title>Menubar</title><meta charset="UTF-8"><script>function openNewWindow()  {var winFeature = 'menubar=no,resizable=yes';// Open a New Windows.window.open('some-page.html','MyWinName',winFeature);}</script></head><body><h3>Menubar</h3><button onclick="openNewWindow()">Open a New Window without menubar</button></body></html> |

some-page.html

| <!DOCTYPE html><html><head><title>Some Page</title><meta charset="UTF-8"></head><body onload="alert('menubar.visible? ' + menubar.visible)"><h3>Some Page</h3><p>1</p><p>1 2</p><p>1 2 3</p></body></html> |

Chapter 22 :

JavaScript JSON

1  What is JSON

2  JSON.parse(..)

3  JSON.stringify(..)

1  What is JSON

As you know data is always transmitted from one computer to the other through the Internet environment, and it is packaged in a certain format before sending it. Recipients must understand this format to analyze the original data.

XML is a quite common format for storing and transporting data.

| ![](OEBPS/image_rsrc8TW.jpg) |

JSON stands for JavaScript Object Notation. It is also a format for storing and transporting data. The JSON format is derived from the object syntax of Javascript, therefore, it inherits simplicity, and is completely based on text.

| ![](OEBPS/image_rsrc8TX.jpg) |

Below is a code snippet that declares an object in Javascript:

Javascript Object

| var aCompany = {name : "Amazon",ceo : "Jeff Bezos",employees: [{firstName: "John", lastName: "Doe"},{firstName: "Anna", lastName: "Smith"},{firstName: "Peter", lastName: "Jones"}]}; |

And a data is stored in JSON format:

JSON Data

| {"name" : "Amazon","ceo" : "Jeff Bezos","employees":[{"firstName":"John", "lastName":"Doe"},{"firstName":"Anna", "lastName":"Smith"},{"firstName":"Peter", "lastName":"Jones"}]} |

Strong points of JSON:

*   JSON is a Lightweight format for data exchange.
*   The JSON data describes itself, therefore, is easy to understand for everyone.
*   JSON is an independent language, and a text. You can use any language to read or create JSON data. Most programming languages have libraries to read and write JSON data.

Example:

| // JSON Object:{"firstName":"John", "lastName":"Doe"}// JSON Array:[{"firstName":"John", "lastName":"Doe"},{"firstName":"Anna", "lastName":"Smith"},{"firstName":"Peter", "lastName":"Jones"}] |

Note:

JSON is purely a data format — it contains only properties, no methods.

JSON requires double quotes to be used around strings and property names. Single quotes are not valid.

Even a single misplaced comma or colon can cause a JSON file to go wrong, and not work. You should be careful to validate any data you are attempting to use.

2  JSON.parse(..)

Using the JSON.parse(text) method helps you parse a JSON data and convert it into an object.

json-parse-example.js

| var text = '{ '+ ' "name": "Amazon", '+ ' "ceo" : "Jeff Bezos", '+ ' "employees" : ['+ '    { "firstName":"John" , "lastName":"Doe" },'+ '    { "firstName":"Anna" , "lastName":"Smith" },'+ '    { "firstName":"Peter" , "lastName":"Jones" } '+ '  ] '+ '}';var obj = JSON.parse(text);console.log(obj.employees);console.log(obj.ceo); // Jeff Bezosconsole.log(obj.employees[0].firstName); // Johnconsole.log(obj.employees[1].firstName); // Annaconsole.log(obj.employees[2].firstName); // Peter |

| ![](OEBPS/image_rsrc8TY.jpg) |

json-parse-example.html

| <!DOCTYPE html><html><head><title>JSON.parse</title></head><body><div style="border:1px solid #ccc;padding:5px;"><h3 id="name"></h3><i id="location"></i></div><script>var s = '{"firstName" : "Sammy", "lastName" : "Shark", "location" : "Ocean"}';var obj = JSON.parse(s);document.getElementById("name").innerHTML = obj.firstName + " " + obj.lastName;document.getElementById("location").innerHTML = obj.location;</script></body></html> |

| ![](OEBPS/image_rsrc8TZ.jpg) |

3  JSON.stringify(..)

Using the JSON.stringify(obj) method helps you convert a Javascript object into a text in JSON format.

json-stringify-example1.js

| var obj = {name : "tran", age : 39};var text = JSON.stringify(obj);console.log(text); // {"name":"tran","age":39} |

JSON.stringify(obj)

The JSON.stringify(obj) method is used to convert obj into a String. If the obj object has the toJSON() method, this method will be called to return String. On the contrary, it will be converted by default rules:

*   Number, Boolean, String will be converted into primitive values.
*   Infinity, NaN will be converted into null.
*   If obj is undefined, Function, Symbol, it will be converted into undefined.
*   If undefined, Function, Symbol appear in the object, they will be skipped.
*   If undefined, Function, Symbol appear in array, they will be converted into null.
*   All the properties that have the key such as Symbol will be skipped.
*   The Date object has the toJSON() method, String is returned, like date.toISOString(), therefore, it is treated like a string.

json-stringify-example2.js

| var obj = {name : "tran",age : 39,// function in object will be ignoredsayHello : function()  {console.log("Hello");},// undefined, Symbol, function in Array will be converted to null."others": ["1", Symbol(), undefined, function(){}, "2"]};var text = JSON.stringify(obj);console.log(text); // {"name":"tran","age":39,"others":["1",null,null,null,"2"]} |

Example:

json-stringify-example.js

| JSON.stringify({});                    // '{}'JSON.stringify(true);                  // 'true'JSON.stringify('foo');                 // '"foo"'JSON.stringify([1, 'false', false]);   // '[1,"false",false]'JSON.stringify([NaN, null, Infinity]); // '[null,null,null]'JSON.stringify({ x: 5 });              // '{"x":5}'JSON.stringify(new Date(2006, 0, 2, 15, 4, 5)); // '"2006-01-02T15:04:05.000Z"'JSON.stringify({ x: 5, y: 6 }); // '{"x":5,"y":6}'JSON.stringify([new Number(3), new String('false'), new Boolean(false)]);// '[3,"false",false]'// String-keyed array elements are not enumerable and make no sense in JSONlet a = ['foo', 'bar'];a['baz'] = 'quux';      // a: [ 0: 'foo', 1: 'bar', baz: 'quux' ]JSON.stringify(a);      // '["foo","bar"]'JSON.stringify({ x: [10, undefined, function(){}, Symbol('')] });// '{"x":[10,null,null,null]}'// Standard data structuresJSON.stringify([new Set([1]), new Map([[1, 2]]), new WeakSet([{a: 1}]), new WeakMap([[{a: 1}, 2]])]);// '[{},{},{},{}]'// TypedArrayJSON.stringify([new Int8Array([1]), new Int16Array([1]), new Int32Array([1])]);// '[{"0":1},{"0":1},{"0":1}]'JSON.stringify([new Uint8Array([1]), new Uint8ClampedArray([1]), new Uint16Array([1]), new Uint32Array([1])]);// '[{"0":1},{"0":1},{"0":1},{"0":1}]'JSON.stringify([new Float32Array([1]), new Float64Array([1])]);// '[{"0":1},{"0":1}]'// toJSON()JSON.stringify({ x: 5, y: 6, toJSON(){ return this.x + this.y; } }); // '11'// Symbols:JSON.stringify({ x: undefined, y: Object, z: Symbol('') }); // '{}'JSON.stringify({ [Symbol('foo')]: 'foo' }); // '{}'JSON.stringify({ [Symbol.for('foo')]: 'foo' }, [Symbol.for('foo')]); // '{}'JSON.stringify({ [Symbol.for('foo')]: 'foo' }, function(k, v) {if (typeof k === 'symbol') {return 'a symbol';}});// undefined// Non-enumerable properties:JSON.stringify( Object.create(null, { x: { value: 'x', enumerable: false }, y: { value: 'y', enumerable: true } }) );// '{"y":"y"}' |

JSON.stringify(obj [, replacer[, space]])

The JSON.stringify(..) method actually has 3 parameters of which, the second and third parameters are not mandatory.

Parameters:

obj

An object will be converted to a JSON string.

replacer

*   replacer can be a function to adjust behavior in converting objects into JSON strings.
*   replacer can be an array of Strings. It helps to specify a whitelist of properties which will appear in the JSON string.

space

*   space can be a string (if it is longer than 10 characters, it will be truncated to 10 characters). Used to insert to the JSON to help the JSON more beautiful and easier to see.
*   space can be a number less than or equal to 10 (if it is greater than 10, it will be considered 10). Used to specify a string, consisting of 'space' -blank character. This string will be inserted into the JSON to make the JSON more beautiful and easier to see.

Examples:

Example with the replacer parameter which is an array of Strings:

json-stringify-replacer-example1.js

| var obj = {name: "Tom",gender: "Male",company:"Walt Disney",friends: [{name:"Jerry", gender:"Male"},{name:"Donald", gender: "Male"}]};var replacer = ["name", "friends"];var json = JSON.stringify(obj, replacer);console.log(json); // {"name":"Tom","friends":[{"name":"Jerry"},{"name":"Donald"}]} |

Example with the replacer placer parameter which is a function:

json-stringify-replacer-example2.js

| function replacer(key, value) {console.log(typeof key);console.log(key);// Filtering out propertiesif (typeof value === 'string') {return undefined;}return value;}var obj = {foundation: 'Mozilla',model: 'box',week: 45,transport: 'car',month: 7};var json = JSON.stringify(obj, replacer);console.log(json); // '{"week":45,"month":7}' |

Chapter 23 :

JavaScript Event Handling

1  Javascript Events

2  Example with events

1  Javascript Events

Event is a signal that something has happened. For example, you click on a button, or you close the browser, .. All DOM nodes generate such signals, but there are events other than the DOM for example, your event of closing the browser window.

Below is a list of most useful DOM events:

Mouse Events:

| Event | Description |
| click | The event occurs when the user clicks on an element |
| contextmenu | The event occurs when the user right-clicks on an element to open a context menu |
| dblclick | The event occurs when the user double-clicks on an element |
| mousedown | The event occurs when the user presses a mouse button over an element |
| mouseup | The event occurs when a user releases a mouse button over an element |
| mouseenter | The event occurs when the pointer is moved onto an element |
| mouseleave | The event occurs when the pointer is moved out of an element |

| mousemove | The event occurs when the pointer is moving while it is over an element |
| mouseout | The event occurs when a user moves the mouse pointer out of an element, or out of one of its children |
| mouseover | The event occurs when the pointer is moved onto an element, or onto one of its children |

Form elements events:

| Event | Description |
| submit | When user submit a <form>. |
| focus | When user focus on an Element, for example <input>. |
| blur | When user leaves an Element, for example <input>. |

Keyboard Events:

| Event | Description |
| keydown | The event occurs when the user is pressing a key |
| keyup | The event occurs when the user releases a key |
| keypress | The event occurs when the user presses a key. |

Document Events.

| Event | Description |
| DOMContentLoaded | When HTML content has loaded and processed. The DOM model has been created completely. |

CSS Events:

| Event | Description |
| animationstart | The event occurs when a CSS animation has started |
| animationend | The event occurs when a CSS animation has completed |
| animationiteration | The event occurs when a CSS animation is repeated |

Event Handling:

To handle the event, you need to attach the event to a handler. the handler can be a function. When the event occurs the handler will be called to operate. The handler is a way for running Javascript codes that corresponds to user's actions.

The handler can be set in the HTML with the on{event} attribute. For example, click event:

| <input value="Click me" onclick="alert('Click!')" type="button"><input value="Click me" onclick="someFunction()" type="button"> |

The this object represents for the element generating the event.

| <input value="Click me" onclick="someFunction(this)" type="button"> |

When the event occurs, Javascript creates theevent object and you can use it as a value of parameter.

| <input value="Click me" onclick="someFunction(event)" type="button"> |

You can also access the event generating event through the event object.

| var target =  event.target; |

2  Example with events

Simple and often encountered event is the event that users click on an element. Below is a simple example. The user clicks the "=" button to sum two numbers.

| ![](OEBPS/image_rsrc8U0.jpg) |

onclick-example.html

| <!DOCTYPE html><html><head><title>Hello Javascript</title><script type = "text/javascript">function doCalculate()  {var a = document.getElementById("a").value; // A String valuevar b = document.getElementById("b").value; // A String valuevar c = Number(a) + Number(b);document.getElementById("c").value = c;}</script></head><body><h3>Click Event example</h3><input id = "a" type="text" value= "100"/> <br/>+ <br/><input id = "b" type="text" value = "200"/> <br/><button onclick="doCalculate()"> = </button> <br/><input id = "c" type="text" value = ""/></body></html> |

The this object is the element that emits the event. You can pass this object into the event handling function.

this-obj-example.html

| <!DOCTYPE html><html><head><title>Event Example</title><script type = "text/javascript">function changeSize(target)  {var random = Math.round(Math.random() * 100) + 200;target.style.width  = random + "px";target.style.height  = random + "px";}</script></head><body><h3>Event with 'this' object</h3><button onclick="changeSize(this)">Click Me to Change Size</button></body></html> |

| ![](OEBPS/image_rsrc8U1.jpg) |

When the event occurs, an event object is created by Javascript. it contains tje information related to the event. For example, for the mouse event, the event object may contain the information such as the mouse position relative to the browser, the position of mouse relative to the element that emits the event, ... You can use the event object to pass in the event handling function.

| <input value="Click me" onclick="someFunction(event)" type="button"> |

| ![](OEBPS/image_rsrc8U2.jpg) |

mouse-events-example.html

| <!DOCTYPE html><html><head><title>Javascript Mouse Events</title><script src="mouse-events-example.js"></script><style>.my-div {width: 290px;height: 100px;background: blue;}</style></head><body><h3>Mouse Events (Enter, Move, Leave)</h3><div class="my-div"onmouseenter="mouseenterHandler(event)"onmouseleave="mouseleaveHandler(event)"onmousemove="mousemoveHandler(event)"></div><h3>Mouse position</h3><div style="color:red;" id="position-div"></div><h3>Statistics</h3><div style="color:red;" id="statistics-div"></div></body></html> |

mouse-events-example.js

| var enterCount = 0;var moveCount = 0;var leaveCount = 0;function mouseleaveHandler(evt) {leaveCount += 1;showPosition(evt);showStatistics();}function mouseenterHandler(evt) {enterCount += 1;showPosition(evt);showStatistics();}function mousemoveHandler(evt) {moveCount += 1;showPosition(evt);showStatistics();}function showPosition(evt) {var html = "offsetX: " + evt.offsetX +"<br/>" //+"offsetY: " + evt.offsetY;document.getElementById("position-div").innerHTML = html;}function showStatistics() {var html ="enterCount:" + enterCount + "<br/>" //+"moveCount:" + moveCount + "<br/>" //+"leaveCount:" + leaveCount;document.getElementById("statistics-div").innerHTML = html;} |

You can access the element emitting event via the event object.

event-obj-example.html

| <!DOCTYPE html><html><head><title>Event Example</title><script type = "text/javascript">function changeSize(evt)  {var target = evt.target;var random = Math.round(Math.random() * 100) + 100;target.style.width  = random + "px";target.style.height  = random + "px";}</script></head><body><h3>Access 'target' object via 'event' object</h3><button onclick="changeSize(event)">Click Me to Change Size</button></body></html> |

Example of a handler with multiple parameters.

multi-params-example.html

| <!DOCTYPE html><html><head><title>Event Example</title><script type = "text/javascript">function changeSize(borderColor, target, evt, bgColor)  {var random = Math.round(Math.random() * 100) + 100;target.style.width  = random + "px";target.style.height  = random + "px";target.style.borderColor = borderColor;target.style.backgroundColor = bgColor;}</script></head><body><h3>A Handler has multiple parameters</h3><a href="">Reset</a> <br/><br/><button onclick="changeSize('red', this, event, 'green')">Click Me</button></body></html> |

Chapter 24 :

Javascript MouseEvent

1  MouseEvent

2  Properties & Methods

1  MouseEvent

MouseEvent is an interface that represents for the events occurring when users interact with pointing devices, such as mouse, common events such as click, dbclick, mousedown, mouseup,...

MouseEvent is an sub-interface of UIEvent.

| ![](OEBPS/image_rsrc8U3.jpg) |

Event types of MouseEvent:

| Event | Description |
| click | The event occurs when the user clicks on an element |
| contextmenu | The event occurs when the user right-clicks on an element to open a context menu |
| dblclick | The event occurs when the user double-clicks on an element |
| mousedown | The event occurs when the user presses a mouse button over an element |
| mouseup | The event occurs when a user releases a mouse button over an element |
| mouseenter | The event occurs when the pointer is moved onto an element |
| mouseleave | The event occurs when the pointer is moved out of an element |

| mousemove | The event occurs when the pointer is moving while it is over an element or its children. |
| mouseout | The event occurs when a user moves the mouse pointer out of an element, or out of one of its children |
| mouseover | The event occurs when the pointer is moved onto an element, or onto one of its children |

mousedown, mouseup, click

Let's start with the most common event out of the mouse events that is click. It is formed from pressing down and releasing. The click event is illustrated as below:

| ![](OEBPS/image_rsrc8U4.jpg) |

dbclick

If you click 2 times quickly, it will create a dbclick event.

mouseover vs mouseenter

The mouseenter event occurs when the cursor enters an element. The mouseover event occurs when the cursor enters an element or one of its child elements.

| ![](OEBPS/image_rsrc8U5.jpg) |

mouseleave vs mouseout

The mouseleave element occurs when the cursor moves out of an element. The mouseout event happens when the cursor moves out of an element or one of its child elements.

| ![](OEBPS/image_rsrc8U6.jpg) |

The following example helps you compare mouseenter vs mouseover, mouseleave vs mouseout:

| ![](OEBPS/image_rsrc8U7.jpg) |

enter-vs-over-leave-vs-out.html

| <!DOCTYPE html><html><head><title>Javascript Mouse Events</title><script src="enter-vs-over-leave-vs-out.js"></script><style>#target-div {width: 320px;height: 150px;background: blue;}#target-div > div  {width: 50px;height: 80px;margin: 40px 0 0 40px;padding: 5px 0 0 5px;float: left;background: yellow;}</style></head><body><h3>mouseenter vs mouseover</h3><h3>mouseleave vs mouseout</h3><div id="target-div"onmouseenter="mouseenterHandler(event)"onmouseover="mouseoverHandler(event)"onmouseleave="mouseleaveHandler(event)"onmouseout="mouseoutHandler(event)"><div>Child</div><div>Child</div><div>Child</div></div><h3>Statistics:</h3><div style="color:red;" id="statistics-div"></div></body></html> |

enter-vs-over-leave-vs-out.js

| var enterCount = 0;var overCount = 0;var leaveCount = 0;var outCount = 0;function mouseenterHandler(evt) {enterCount += 1;showStatistics();}function mouseoverHandler(evt) {overCount += 1;showStatistics();}function mouseleaveHandler(evt) {leaveCount += 1;showStatistics();}function mouseoutHandler(evt) {outCount += 1;showStatistics();}function showStatistics() {var html ="enterCount:" + enterCount + "<br/>" //+"overCount:" + overCount  + "<hr/>" //+"leaveCount:" + leaveCount + "<br/>" //+"outCount:" + outCount ;document.getElementById("statistics-div").innerHTML = html;} |

mousemove

| ![](OEBPS/image_rsrc8U8.jpg) |

mousemove-example.html

| <!DOCTYPE html><html><head><title>Javascript Mouse Events</title><script src="mousemove-example.js"></script><style>#target-div {width: 320px;height: 150px;background: blue;margin-bottom: 50px;}#target-div > div  {width: 50px;height: 150px;margin: 40px 0 0 40px;padding: 5px 0 0 5px;float: left;background: yellow;}</style></head><body><h3>mousemove example</h3><div id="target-div" onmousemove="mousemoveHandler(event)"><div>Child</div><div>Child</div><div>Child</div></div><h3>Statistics:</h3><div style="color:red;" id="statistics-div"></div></body></html> |

mousemove-example.js

| var moveCount = 0;function mousemoveHandler(evt) {moveCount += 1;showStatistics();}function showStatistics() {var html = "moveCount:" + moveCount;document.getElementById("statistics-div").innerHTML = html;} |

2  Properties & Methods

MouseEvent is the sub- interface of UIEvent, therefore, it inherits the properties and methods from this interface.

Key

| Property | Description |
| altKey | Returns true if "ALT" key was pressed when the mouse event was triggered, otherwise returns false. |
| ctrlKey | Returns true if "CTRL" key was pressed when the mouse event was triggered, otherwise returns false. |
| shiftKey | Returns true if "SHIFT" key was pressed when an event was triggered, otherwise returns false. |
| metaKey | Returns true if "META" key was pressed when an event was triggered, otherwise returns false. |

Example with the ctrlKey property:

| ![](OEBPS/image_rsrc8U9.jpg) |

prop-ctrlKey-example.html

| <!DOCTYPE html><html><head><title>Javascript Mouse Events</title><style>#target-div {width: 320px;height: 150px;background: blue;margin-bottom: 10px;}</style><script>function clickHandler(evt) {var html = "evt.ctrlKey=" + evt.ctrlKey;document.getElementById("log-div").innerHTML = html;}</script></head><body><h3>Press Ctrl key and Click</h3><div id="target-div" onclick="clickHandler(event)" ></div><div style="color:red;" id="log-div"></div></body></html> |

Position:

| Property | Description |
| clientX | Returns the horizontal coordinate of the mouse pointer, relative to the current window. |
| clientY | Returns the vertical coordinate of the mouse pointer, relative to the current window. |
| offsetX | Returns the horizontal coordinate of the mouse pointer relative to the position of the edge of the target element |
| offsetY | Returns the vertical coordinate of the mouse pointer relative to the position of the edge of the target element |
| pageX | Returns the horizontal coordinate of the mouse pointer, relative to the document. |
| pageY | Returns the vertical coordinate of the mouse pointer, relative to the document. |
| screenX | Returns the horizontal coordinate of the mouse pointer, relative to the screen (Computer or device) |

| screenY | Returns the vertical coordinate of the mouse pointer, relative to the screen (Computer or device) |
| movementX | Returns the horizontal coordinate of the mouse pointer relative to the position of the last mousemove event |
| movementY | Returns the vertical coordinate of the mouse pointer relative to the position of the last mousemove event |

| ![](OEBPS/image_rsrc8UA.jpg) |

| ![](OEBPS/image_rsrc8UB.jpg) |

prop-positions-example.html

| <!DOCTYPE html><html><head><title>Javascript Mouse Events</title><script src="prop-positions-example.js"></script><style>#target-div {width: 300px;height: 210px;background: #ccc;margin: 0px 0px 10px 20px;padding: 5px;}</style></head><body style="height:450px; width:1000px;"><h3>Positions</h3><div id="target-div" onmousemove="mousemoveHandler(event)" ></div></body></html> |

prop-positions-example.js

| function mousemoveHandler(evt) {var html =  "offsetX = " + evt.offsetX +"<br/>"+ "offsetY = " + evt.offsetY +"<br/>"+ "clientX = " + evt.clientX +"<br/>"+ "clientY = " + evt.clientY +"<br/>"+ "pageX = " + evt.pageX +"<br/>"+ "pageY = " + evt.pageY +"<br/>"+ "screenX = " + evt.screenX +"<br/>"+ "screenY = " + evt.screenY +"<br/>"+ "movementX = " + evt.movementX +"<br/>"+ "movementY = " + evt.movementY;document.getElementById("target-div").innerHTML = html;} |

Button

| Property | Description |
| button | Returns a number that describes which mouse button was pressed when the mouse event was triggered |
| buttons | Returns a number that describes which mouse buttons were pressed when the mouse event was triggered |

event.button:

*   0: Main button, usually the left button or the un-initialized state
*   1: Auxiliary button, usually the wheel button or the middle button (if present)
*   2: Secondary button, usually the right button
*   3: Fourth button, typically the Browser Back button
*   4: Fifth button, typically the Browser Forward button

event.buttons:

*   0 : No button or un-initialized
*   1 : Primary button, usually the left button.
*   2 : Secondary button, usually the right button.
*   4 : Auxilary button, usually the mouse wheel button or middle button.
*   8 : 4th button, typically the "Browser Back" button.
*   16 : 5th button, typically the "Browser Forward" button.

event.buttons may return a different value other than the above values. For example, event.buttons returns 3 if you press both the left mouse and right mouse at the same time.

prop-button-buttons-example.html

| <!DOCTYPE html><html><head><title>MouseEvent Example</title><script>function mousedownHandler(evt) {var logDiv = document.getElementById("log-div");logDiv.innerHTML = "event.button= " + evt.button +"<br/>"+ "event.buttons= "+ evt.buttons;}</script></head><body><h3>event.button, event.buttons</h3><button onmousedown="mousedownHandler(event)">Click Me!</button><br/><br/><div id="log-div" style="color:red;"></div></body></html> |

| ![](OEBPS/image_rsrc8UC.jpg) |

Chapter 25 :

Javascript WheelEvent

1  WheelEvent

WheelEvent is an interface representing for the events occurring when an user moves mouse wheel or similar equipment.

WheelEvent means sub-interface of MouseEvent. It will inherit all properties and methods of parent interface.

| ![](OEBPS/image_rsrc8UD.jpg) |

| Event | Description |
| wheel | The event occurs when the mouse wheel rolls up or down over an element |

The properties of WheelEvent:

| Property | Description |
| deltaX | Returns the horizontal scroll amount of a mouse wheel (x-axis) |
| deltaY | Returns the vertical scroll amount of a mouse wheel (y-axis) |
| deltaZ | Returns the scroll amount of a mouse wheel for the z-axis |
| deltaMode | Returns a number that represents the unit of measurements for delta values (DOM_DELTA_PIXEL, DOM_DELTA_PIXEL, DOM_DELTA_PAGE) |

Example with WheelEvent:

| ![](OEBPS/image_rsrc8UE.jpg) |

| ![](OEBPS/image_rsrc8UF.jpg) |

wheelevents-example.html

| <!DOCTYPE html><html><head><title>WheelEvent Example</title><script src="wheelevents-example.js"></script></head><body><h3>WheelEvent example</h3><div style="font-size:12px; padding:5px; border:1px solid #ccc;"onwheel="wheelHandler(event)">Hello Everyone!<div></body></html> |

wheelevents-example.js

| function wheelHandler(evt)  {var fontSize = evt.target.style.fontSize;// 12px, 13px,...var value = Number(fontSize.substr(0, fontSize.length-2)); // 12, 13,..// Scrolling upif (evt.deltaY < 0) {if(value < 50)  {value++;}}// Scrolling downif(evt.deltaY > 0)  {if(value > 5)  {value--;}}evt.target.style.fontSize = value+"px";} |

| ![](OEBPS/image_rsrc8UG.jpg) |

Chapter 26 :

Javascript KeyboardEvent

1  KeyboardEvent

2  Properties & Methods

3  Table: Key, KeyCode

1  KeyboardEvent

KeyboardEvent is an interface that represents events occurring when users interact with a keyboard, including keydown, keypress, keyup events.

KeyboardEvent is subinterface of UIEvent.

| ![](OEBPS/image_rsrc8UH.jpg) |

| Order | Event |
| 1 | onkeydown |
| 2 | onkeypress |
| 3 | onkeyup |

keydown

The keydown event occurs when you press down a key. In Windows OS, If you continue to keep the key pressed, it will constantly emit keydown & keypress events. But in MacOS, If you continue to keep the key pressed, it will constantly emit keydown events. Like the following illustration.

| ![](OEBPS/image_rsrc8UJ.jpg) |

keypress

There are 2 cases of occurence of the keypress, in which case 1 is explained above by me (View the keydown event). Case 2 is that you press down a key and quickly release it, and at this time there will be 2 events such as keypress, keyup emitted in the order.

| ![](OEBPS/image_rsrc8UK.jpg) |

keyup

The keyup event occurs when you release a key.

Note: The keypress event will not be emitted for the keys such as ALT, SHIFT, CTRL, META-KEY, ESC. If you want to detect whether those keys are being pressed, you can use the properties such as altKey, shiftKey, ctrlKey, metaKey of the event object.

keyevents-example.html

| <!DOCTYPE html><html><head><title>KeyEvent Example</title><script src="keyevents-example.js"></script></head><body><h3>KeyEvent example</h3><input type="text"onkeydown="keydownHandler(event)"onkeyup="keyupHandler(event)"onkeypress="keypressHandler(event)"/><br/><br/><textarea id="log-div" rows = "10" disabled></textarea><br/><button onclick="clearLog()">Clear</button></body></html> |

keyevents-example.js

| function keydownHandler(evt)  {appendLog("Keydown!");}function keyupHandler(evt)  {appendLog("Keyup!");}function keypressHandler(evt)  {appendLog("Keypress!");}function appendLog(text)  {var oldText = document.getElementById("log-div").value;document.getElementById("log-div").value = oldText+"\n"+ text;}function clearLog()  {document.getElementById("log-div").value = "";} |

| ![](OEBPS/image_rsrc8UM.jpg) |

2  Properties & Methods

KeyEvent is the sub-interface of UIEvent, therefore, it inherits the properties and methods from this interface.

| Property | Description |
| altKey | Returns true if the "ALT" key is being pressed when a key event occurs. |
| ctrlKey | Returns true if the "CTRL" key is being pressed when a key event occurs. |
| shiftKey | Returns true if the "SHIFT" key is being pressed when a key event occurs. |
| metaKey | Returns true if the "META" đkey is being pressed when a key event occurs. |

Eample: Press the 'SHIFT' key and keep it unchanged and then press any key.

| ![](OEBPS/image_rsrc8UN.jpg) |

prop-shiftKey-example.html

| <!DOCTYPE html><html><head><title>KeyEvent Example</title><script src="prop-shiftKey-example.js"></script></head><body><h3>Hold key 'SHIFT' and press any key!</h3><input type="text"onkeydown="keydownHandler(event)"/><br/><br/><div id="log-div" style="color:red;"></div></body></html> |

prop-shiftKey-example.js

| function keydownHandler(evt)  {if(evt.shiftKey) {document.getElementById("log-div").innerHTML ="evt.shiftKey = true";} else {document.getElementById("log-div").innerHTML ="evt.shiftKey = false";}} |

Chapter 27 :

Javascript FocusEvent

1  FocusEvent

2  focusin, focusout

1  FocusEvent

FocusEvent is an interface that represents the events related to focus, namely, the 4 events such as focus, focusin, blur, focusout.

| ![](OEBPS/image_rsrc8UP.jpg) |

Properties:

| Property | Description |
| relatedTarget | Returns the element related to the element that triggered the event |

If you jump to an element and then jump outside (focus to another element), there will be 4 events that occur in sequence respectively:

*   focus
*   focusin
*   blue
*   focusout

| ![](OEBPS/image_rsrc8UR.jpg) |

The focus event occurs before focusin. In fact, they happen very close to each other, which can be considered as occurring at the same time. Similarly, the blur event occurs before focusout, iIn fact, they happen very close to each other, which can be considered as occurring at the same time.

focus

The focus event occurs when you are in other place and jumps into an element, such as the <input> element to prepare to enter content for this element.

blur

The blur event occurs when you jump out of an element (focus on another element).

focusevent-example.html

| <!DOCTYPE html><html><head><title>FocusEvent</title><script>function focusHandler(evt)  {showLog("focus");}function blurHandler(evt)  {showLog("blur");}function showLog(msg)  {var oldHtml= document.getElementById("log-div").innerHTML;document.getElementById("log-div").innerHTML=oldHtml + " .. "+ msg;}</script></head><body><h3>Test events: focus, blur</h3><input type="text"onfocus="focusHandler(event)"onblur="blurHandler(event)"  /><br><br><div id="log-div" style="padding:10px;border:1px solid #ccd;"></div></body></html> |

| ![](OEBPS/image_rsrc8US.jpg) |

2  focusin, focusout

The focus, blur events are designed for the elements are "focusable", for example, <input>, <textarea>,.. While the focusin, focusout events are designed for the elements that can contain other elements for example, <div>, <span>, <form>,..

focus vs focusin

| ![](OEBPS/image_rsrc8UT.jpg) |

Suppose you have a <form> with 2 <input> child elements. When an user jumps into one of the <input> elements then the focus event will occur. The focus event at the child element will create the focusin event at the parent elements. Thus this focusin event will occur at the <form> element.

Note: Although the focusin event occurs on the parent element, but event.target returns the child element (The element that fires the focus event).

blur vs focusout

| ![](OEBPS/image_rsrc8UU.jpg) |

Suppose you have a <form> with 2 <input> child elements. When an user jumps out of the <input> element, the blur event will happen.The blur event at the child element will create the focusout event at the parent elements. Thus this focusout event will occur at the <form> element.

Note: Although the focusout event occurs on the parent element, but event.target returns the child element (The element that fires the blur event).

Example: focusin & focusout

focusin-focusout-example.html

| <!DOCTYPE html><html><head><title>FocusEvent</title><meta charset="utf-8" /><script src="focusin-focusout-example.js"></script><style>form {border: 1px solid #ccc;padding: 10px;display: inline-block;}</style></head><body><h3>Events: focusin & focusout</h3><p>Focus to 'input' and Blur to it</p><form onfocusin="focusinHandler(event)" onfocusout="focusoutHandler(event)">User Name<input type="text" name="username" /><br><br> Email<input type="text" name="email" /></form></body></html> |

focusin-focusout-example.js

| function focusinHandler(evt) {// <input>evt.target.style.border="1px solid blue";// <form>evt.target.parentElement.style.border="1px solid red";}function focusoutHandler(evt) {// <input>evt.target.style.border="1px solid black";// <form>evt.target.parentElement.style.border="1px solid black";} |

| ![](OEBPS/image_rsrc8UV.jpg) |

Do you have problem with onfocusout (???)

For the <input>, <textarea>,.. elements, you need only to handle the focus, blur events. The onfocusout attribute doesn't work with this element on some browsers (I have checked this problem on the Firefox, Chrome browsers).

attr-onfocusout-not-working.html

| <!DOCTYPE html><html><head><title>FocusEvent</title><script>function focusHandler(evt)  {showLog("focus");}function focusinHandler(evt)  {showLog("focusin");}function focusoutHandler(evt)  {showLog("focusout");}function blurHandler(evt)  {showLog("blur");}function showLog(msg)  {var oldHtml= document.getElementById("log-div").innerHTML;document.getElementById("log-div").innerHTML=oldHtml + " .. "+ msg;}</script></head><body><h3>Why does the 'onfocusout' attribute not work with 'input'?</h3><input type="text"onfocus="focusHandler(event)"onblur="blurHandler(event)"onfocusin="focusinHandler(event)"onforcusout="focusoutHandler(event)" /><br><br><div id="log-div" style="padding:10px;border:1px solid #ccd;"></div></body></html> |

| ![](OEBPS/image_rsrc8UW.jpg) |

Althought the onfocusout attribute doesn't work with the <input>, <textarea>,.. elements on some browsers. But, if desiring, you can still register the focusout event for them in the following way:

| // Javascript Code:var myInput = document.getElementById("my-input");myInput.addEventListener("focus", focusHandler);myInput.addEventListener("focusin", focusinHandler);myInput.addEventListener("focusout", focusoutHandler);myInput.addEventListener("blur", blurHandler); |

See full example:

focusevents-addEventListener-example.html

| <!DOCTYPE html><html><head><title>FocusEvent</title><meta charset="utf-8"/></head><body><h3>Test events: focus, focusin, focusout, blur</h3><input id="my-input" type="text" /><br><br><div id="log-div" style="padding:10px;border:1px solid #ccd;"></div><script src="focusevents-addEventListener-example.js"></script></body></html> |

focusevents-addEventListener-example.js

| function focusHandler(evt)  {showLog("focus");}function focusinHandler(evt)  {showLog("focusin");}function focusoutHandler(evt)  {showLog("focusout");}function blurHandler(evt)  {showLog("blur");}function showLog(msg)  {var oldHtml= document.getElementById("log-div").innerHTML;document.getElementById("log-div").innerHTML=oldHtml + " .. "+ msg;}// Javascript Code:var myInput = document.getElementById("my-input");myInput.addEventListener("focus", focusHandler);myInput.addEventListener("focusin", focusinHandler);myInput.addEventListener("focusout", focusoutHandler);myInput.addEventListener("blur", blurHandler); |

| ![](OEBPS/image_rsrc8UX.jpg) |

Chapter 28 :

Javascript InputEvent

1  InputEvent

2  Properties, Methods

1  InputEvent

InputEvent is an interface that represents events occurring when a user enters data on the editable elements such as <input>, <textarea> or the elements with contenteditable="true" attributes.

InputEvent is a sub-interface of UIEvent.

| ![](OEBPS/image_rsrc8UY.jpg) |

Events:

| Event | Description |
| input | The event occurs when an element gets user input |

Example of elements that support the input event:

inputevents-elements-example.html

| <!DOCTYPE html><html><head><title>InputEvent Example</title><meta charset="UTF-8"><style>*[contenteditable='true']   {height:30px;padding:5px;border:1px solid #ccd;}</style><script>// Note: event.data is not supported in Firefox, IEfunction inputHandler(evt)  {showLog(evt.data);}function showLog(text)  {var logDiv = document.getElementById("log-div");logDiv.innerHTML = logDiv.innerHTML + " .. " + text;}</script></head><body><h3>InputEvent example</h3><p style="color:red">Note: event.data is not supported in Firefox, IE</p><h3>Input element</h3><input type="text" oninput ="inputHandler(event)"/><h3>Textarea element</h3><textarea oninput ="inputHandler(event)" rows="5" cols="30"></textarea><h3>Elements with contenteditable='true'</h3><div oninput ="inputHandler(event)" contenteditable="true"></div><p id="log-div"></p></body></html> |

| ![](OEBPS/image_rsrc8UZ.jpg) |

Events: input vs change

You also can consider using the change event because it is quite similar to the input event:

*   The change event supports the <select> element. It occurs when users change the option on <select>.
*   For the <input> (text, number, email, password, tel, time, week, month, date, datetime-local, search, url), <textarea> elements: The input event occurs immediately after the value of element changes. While the change event occurs when the value of element changes and the element loses focus.

2  Properties, Methods

InputEvent is the sub-interface of UIEvent so it inherits all methods and properties from UIEvent. In addition, it has its own methods and properties.

Properties:

| Property | Description |
| data | Returns the inserted characters. This may be an empty string if the change doesn't insert text (such as when deleting characters, for example). |
| dataTransfer | Returns a DataTransfer object containing information about richtext or plaintext data being added to or removed from editable content. |
| inputType | Returns the type of change for editable content such as, for example, 'inserting', 'deleting', 'formatting', ... |
| isComposing | Returns true/false indicating if the event is fired after compositionstart and before compositionend. |

Chapter 29 :

Javascript ChangeEvent

1  ChangeEvent

The change event fires in the following situations:

*   Users check/uncheck on <input type="checkbox">.
*   Users make changes on <input type="radio">.
*   Users change the value of <input> (file, color, range).
*   Users change the contents of <input> (text, number, email, password, tel, time, week, month, date, datetime-local, search, url), then focus on other place.
*   Users change the contents of <textarea>, then focus on other place.
*   Users change the option on the <select> element.

Example with the change event:

changeevents-elements-example.html

| <!DOCTYPE html><html><head><title>ChangeEvent Example</title><meta charset="UTF-8"><style>.title {font-weight:bold;}</style><script>function changeHandler(evt)  {alert("Changed!");}</script></head><body><h2>ChangeEvent example</h2><p class="title">Input (checkbox, radio):</p><input type="checkbox"  onchange ="changeHandler(event)"/><input type="radio" name ="gender" value="M" onchange ="changeHandler(event)"/><input type="radio" name ="gender" value="F" onchange ="changeHandler(event)"/><p class="title">Input (range):</p><input type="range" min ="1" max="10" onchange ="changeHandler(event)"/><p class="title">Input (color):</p><input type="color" onchange ="changeHandler(event)"/><p class="title">Input (file):</p><input type="file" onchange ="changeHandler(event)"/><p class="title">Input (image, hidden, buton, submit, reset):</p>- (Not support 'change' event)<p class="title">Input (text, number, email, password, tel, time, week, month, date, datetime-local, search, url):</p><input type="text" onchange ="changeHandler(event)"/><p class="title">Textarea element</p><textarea onchange ="changeHandler(event)" rows="3" cols="30"></textarea><p class="title">Select:</p><select onchange ="changeHandler(event)"><option value ="en">English</option><option value ="de">German</option><option value ="vi">Vietnamese</option></select><p id="log-div"></p></body></html> |

| ![](OEBPS/image_rsrc8V0.jpg) |

Example with the change event on the <select> element:

changeevents-select-example.html

| <!DOCTYPE html><html><head><title>ChangeEvent Example</title><meta charset="UTF-8"><script>function changeHandler(evt)  {alert("Language: " + evt.target.value);}</script></head><body><h2>ChangeEvent example</h2><p class="title">Select Language:</p><select onchange ="changeHandler(event)"><option value ="en">English</option><option value ="de">German</option><option value ="vi">Vietnamese</option></select></body></html> |

| ![](OEBPS/image_rsrc8V1.jpg) |

Chapter 30 :

Javascript DragEvent

1  DragEvent

DragEvent is an interface that represents events occurring during drag & drop of an object from one place to another. An user initiates a drag by putting a pointer device (such as a mouse) on the surface of an object, press down, and move the pointer device to another place, then release the pointer device, to drop the object into a new location.

| ![](OEBPS/image_rsrc8V2.jpg) |

| ![](OEBPS/image_rsrc8V3.jpg) |

DragEvent is a sub-interface of MouseEvent, therefore, it inherits all the properties and methods of MouseEvent.

| ![](OEBPS/image_rsrc8V4.jpg) |

Below is the list of the types of events that will occur during drag and drop

| Event | Element Type | Description |
| dragstart | Dragged Element | The event occurs when the user starts to drag an element |
| drag | Dragged Element | The event occurs when an element is being dragged |
| dragend | Dragged Element | The event occurs when the user has finished dragging an element |
| dragenter | Drop Target | The event occurs when the dragged element enters the drop target |
| dragover | Drop Target | The event occurs when the dragged element is over the drop target |
| dragleave | Drop Target | The event occurs when the dragged element leaves the drop target |
| drop | Drop Target | The event occurs when the dragged element is dropped on the drop target |

| ![](OEBPS/image_rsrc8V5.jpg) |

| Property | Description |
| dataTransfer | Returns the data that is dragged/dropped |

See a simple example:

| ![](OEBPS/image_rsrc8V6.jpg) |

dragevents-example.html

| <!DOCTYPE html><html><head><title>DragEvent Example</title><script src="dragevents-example.js"></script><style>.droptarget-div {float: left;width: 100px;height: 55px;margin: 25px 25px 5px 5px;padding: 10px;border: 1px solid black;}#dragtarget-div {background: #eee;padding: 5px;}</style></head><body><h3>DragEvent example</h3><p id="log-div">..</p><!-- Drop Target 1 --><div class="droptarget-div"ondragenter= "ondragenterHandler(event)"ondragover="dragoverHandler(event)"ondrop="dropHandler(event)"><p id="dragtarget-div"ondragstart="dragstartHandler(event)"ondrag="dragHandler(event)"draggable="true">Drag me!</p></div><!-- Drop Target 2 --><div class="droptarget-div"ondragenter= "ondragenterHandler(event)"ondragover="dragoverHandler(event)"ondrop="dropHandler(event)"></div></body></html> |

dragevents-example.js

| // --------- Handlers for 'Dragged Element' ------------------function dragstartHandler(evt) {evt.dataTransfer.setData("MyDraggedElementId", evt.target.id);}// dragging ...function dragHandler(evt) {showLog("The p element is being dragged");}// --------- Handlers for 'Drop Target' ------------------function ondragenterHandler()  {showLog("The p element enter drop-target");}// When 'over' you can 'release mouse' to 'drop'.function dragoverHandler(evt) {evt.preventDefault(); // Important!!}function dropHandler(evt) {evt.preventDefault(); // Important!!var elementId = evt.dataTransfer.getData("MyDraggedElementId");evt.target.appendChild(document.getElementById(elementId));showLog("The p element was dropped");}// -------------------------------------------------------function showLog(text)  {document.getElementById("log-div").innerHTML = text;} |

For example, users drag files on their computer and drop into a <div> element, you can read the basic information, and the content of the files that the user has dropped.

When the drop event occurs, event.dataTransfer.files returns a FileList object, which contains a list of File objects.

| ![](OEBPS/image_rsrc8V7.jpg) |

Chapter 31 :

Javascript HashChangeEvent

1  HashChangeEvent

Hash is "Anchor part" of an URL. It tells the browser to scroll the browser scrollbar to display the content area corresponding to Hash.

| ![](OEBPS/image_rsrc8V8.jpg) |

hash-example.html

| <!DOCTYPE html><html><head><title>Hash Example</title><meta charset="UTF-8"><style>.content {margin-top: 30px;padding: 5px;border: 1px solid #ddd;}</style></head><body><a href="#chapter1">Go to Chapter 1</a>&#124;&#124;<a href="#chapter2">Go to Chapter 2</a>&#124;&#124;<a href="#chapter3">Go to Chapter 3</a><div class="content"><!-- Anchor 1 --><a id="chapter1"></a><h3>Chapter 1</h3>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/>Chapter 1 content <br/><!-- Anchor 2 --><a id="chapter2"></a><h3>Chapter 2</h3>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/>Chapter 2 content <br/><!-- Anchor 3 --><a id="chapter3"></a><h3>Chapter 3</h3>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/>Chapter 3 content <br/></div><p id="log-div"></p></body></html> |

Chapter 32 :

Javascript URL Encoding

1  Javascript URL Encoding

In this article, I will show you how to encode and decode a URL using Javascript.

Let's begin with the question, "How do we do to encode a URL with Javascript?".

Actually, it depends on what you want to do. Javascript provides you with two functions which are encodeURI() and encodeURIComponent(). The difference between these two functions is that which characters will be encoded.

*   The encodeURI () function encodes all the characters except for the ~!@#$&*()=:/,;?+
*   The encodeURIComponent() function encodes all the characters except for the -_.!~*'()

Therefore, the encodeURI() function will be a good choice if you want to entirely encode a URL, because the ( http:// ) will not be encoded. Otherwise, you can use the encodeURIComponent() function if you intend to encode the value of a parameter.

But if you use the encodeURIComponent () function to entirely encode a URL, you will get an unwanted result.

Chapter 33 :

Javascript FileReader

1  FileReader

2  Example with FileReader

1  FileReader

Interface FileReader in Javascript is designed to read data sources on users' computers.

Note: In fact, Javascript can read only resources on the user's computer if the user has actions to allow, for example, the user clicks the <input type="file"> element to select the file on the computer, or drag and drop the files into the browser.

FileReader can read the File, Blob or DataTransfer objects (This object is obtained when users drug and drop a file into the browser).

The API of FileReader is designed with the same main purpose as XMLHttpRequest because both of them have the goal such as loading external resource. Data is read asynchronously to avoid blocking browser while the process is being carried out.

Constructor

| // Create a FileReader object:var fileReader = new FileReader(); |

Properties

| Property | Description |
| error | A the DOMException object that describe errors happening during reading data sources. |
| readyState | A number that describes the status of FileReader. Values may be: 0, 1, 2. |
| result | Content of data source after reading successfully. Its format depends on which method is used when starting reading. |

Events

During loading data source with FileReader, the events described in ProgressEvent will be fired, specifically:

| Event | Description |
| loadstart | Indicates that the process of loading data has begun. This event always fires first. |
| progress | Event fires multiple times as data is being loaded, giving access to intermediate data. |
| error | Event fires when loading has failed. |
| abort | Event fires when data loading has been canceled by calling abort() method (Method available on both XMLHttpRequest & FileReader). |
| load | Event fires only when all data has been successfully read. |
| loadend | Event fires when the object has finished transferring data. Always fires after error, abort, or load. |

Event Handlers

| Handler | Description |
| onloadstart(progressEvt) | A handler for the loadstart event. |
| onprogress(progressEvt) | A handler for the progress event. |
| onerror(progressEvt) | A handler for the error event. |
| onabort(progressEvt) | A handler for the abort event. |
| onload(progressEvt) | A handler for the load event. |
| onloadend(progressEvt) | A handler for the loadend event. |

| ![](OEBPS/image_rsrc8V9.jpg) |

2  Example with FileReader

In this example, users drag and drop a file into a <div> element. FileReader will be used to read the basic information and contents of the file dropped by the user.

| ![](OEBPS/image_rsrc8VA.jpg) |

| ![](OEBPS/image_rsrc8VB.jpg) |

| ![](OEBPS/image_rsrc8VC.jpg) |

filereader-drop-example.html

| <!DOCTYPE html><html><head><title>FileReader Example</title><meta charset="UTF-8"><script src="filereader-drop-example.js"></script><style>#drop-area {border: 1px solid blue;padding: 15px;margin-top:5px;}</style></head><body><h3>FileReader example</h3><a href="">Reset</a><div id="drop-area" ondragover="dragoverHandler(event)" ondrop="dropHandler(event)">Drop one file here</div><output id="log-div"></output></body></html> |

filereader-drop-example.js

| function dropHandler(evt) {evt.stopPropagation();evt.preventDefault();// FileList object.var files = evt.dataTransfer.files;if (files.length != 1) {resetLog();appendLog("Please drag and drop 1 file!");return;}var file = files[0];var fileReader = new FileReader();fileReader.onloadstart = function(progressEvent) {resetLog();appendLog("onloadstart!");var msg = "File Name: " + file.name + "<br>" +"File Size: " + file.size + "<br>" +"File Type: " + file.type;appendLog(msg);}fileReader.onload = function(progressEvent) {appendLog("onload!");var stringData = fileReader.result;appendLog(" ---------------- File Content ----------------: ");appendLog(stringData);}fileReader.onloadend = function(progressEvent) {appendLog("onloadend!");// FileReader.EMPTY, FileReader.LOADING, FileReader.DONEappendLog("readyState = " + fileReader.readyState);}fileReader.onerror = function(progressEvent) {appendLog("onerror!");appendLog("Has Error!");}// Read file asynchronously.fileReader.readAsText(file, "UTF-8"); // fileReader.result -> String.}function dragoverHandler(evt) {evt.stopPropagation();evt.preventDefault();// Explicitly show this is a copy.evt.dataTransfer.dropEffect = 'copy';}function resetLog() {document.getElementById('log-div').innerHTML = "";}function appendLog(msg) {document.getElementById('log-div').innerHTML += "<br>" + msg;} |