![](Images/cover00118.jpeg)

JAVASCRIPT

CODING BASICS

FOR ABSOLUTE BEGINNERS

BY

TAM SEL

[JAVASCRIPT](#part0002.xhtml__Toc67538290)

[JAVASCRIPT EXAMPLE](#part0002.xhtml__Toc67538291)

[Javascript comment](#part0003.xhtml__Toc67538292)

[Javascript Variable](#part0004.xhtml__Toc67538293)

[Javascript Data Types](#part0005.xhtml__Toc67538294)

[Javascript If Else](#part0006.xhtml__Toc67538295)

[Javascript Switch Statement](#part0007.xhtml__Toc67538296)

[JavaScript Function](#part0008.xhtml__Toc67538297)

[Javascript Object](#part0009.xhtml__Toc67538298)

[Javascript array](#part0010.xhtml__Toc67538299)

[Javascript String](#part0011.xhtml__Toc67538300)

[Javascript Date](#part0012.xhtml__Toc67538301)

[JavaScript Math](#part0013.xhtml__Toc67538302)

[Javascript Number](#part0014.xhtml__Toc67538303)

# JAVASCRIPT

This JavaScript tutorial makes it easy for both beginners and experts to learn JavaScript.

To learn JavaScript, you only need a basic understanding of computers.

# JAVASCRIPT EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <h2>Welcome to JavaScript</h2>  

##### <script>  

##### document.write("Hello Friends");  

##### </script>  

##### </body>  

##### </html>

JavaScript can be implemented by adding JavaScript statements in the code.

<script>…</script>.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script type= "text/javascript">  

##### document.write("Hello World");  

##### </script>  

##### </body>  

##### </html>

### JavaScript code can be written in 3 places in JavaScript

1.  Between the <body>……</body> tag of HTML.
2.  Between the <head>……</head> tag of HTML.
3.  In .jsfile(external JavaScript).

### Example (code between the body tags)

##### In the example below, the body tag contains JavaScript code.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script type="text/javascript">  

##### alert("Hello world");  

##### </script>  

##### </body>  

##### </html>

### Example2 (code between the head tag)

##### We'll create the function msg() in the example below . In JavaScript, you must write function in function name to construct a function. To call a method, we must first create a case. We're using the one-click event to call the msg() function in this case.

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script type="text/javascript">  

##### function msg(){  

##### alert("Hello world");  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <p>Welcome to Javascript</p>  

##### <form>  

##### <input type="button" value="click" onclick="msg()"/>  

##### </form>  

##### </body>  

##### </html>

### External JavaScript file

### We can build a JavaScript file that we can use in HTML files.

### Since a single JavaScript file can be used in several HTML pages, it allows for code reuse.

### It improves the web page's efficiency.

### The file must have a .js extension.

### Example

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script type="text/javascript" src="message.js"></script>  

##### </head>  

##### <body>  

##### <p>Hello world</p>  

##### <form>  

##### <input type="button" value="click" onclick="msg()"/>  

##### </form>  

##### </body>  

##### </html>

# Javascript comment

## Comments in JavaScript are used to describe the code. It's used to add code-related content, such as warnings or recommendations, so that end users can understand it.

## Types of JavaScript comments

There are two kinds of JavaScript comments:

1.  Single-line Comment
2.  Multi-line Comment

### Single-line Comment

Double forward slashes (//) are used to represent single-line comments. While the program is running, any text between the double forward slashes (//) and the end of the line will be ignored.

eg. Comment added before the statement.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### // single-line comment //  

##### document.write("hello world");  

##### </script>  

##### </body>  

##### </html>

eg. Comment added after the statement.

##### 
<!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var a=10;  

##### var b=20;  

##### var c=a+b; //It add values of a and b variable  

##### document.write(c); // print sum of 10 and 20  

##### </script>  

##### </body>  

##### </html>

### Output

30

## Multi-line comment

### Single and multi-line comments can also be made for multi-line comments. Comments that span multi lines begin with /* and end with */. JavaScript will ignore the text in between them.

### /* Write comment here */

#### Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### /* It is multi-line comment.  

##### It will not be displayed */  

##### document.write ("Example of JavaScript multi line comment");  

##### </script>  

##### </body>  

##### </html

# Javascript Variable

Values (name=”Ram”) and expressions (Sum=x+y) are stored in variables.

We must first declare a variable before using it. To declare a variable, we use the keyword var as follows:

##### var name;

There are two types of variables:

1.  Local Variable
2.  Global Variable

Local Variable– It's declared within a function or a block.

#### Example

##### <script>  

##### functionabc(){  

##### var x=10; //local variable  

##### </script>

Global Variable- It has a global scope, meaning that it can be specified anywhere in JavaScript code.

Outside of the function, a variable is declared.

#### Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var data =200; //global variable  

##### function a(){  

##### document.writeln(data);  

##### }  

##### function b(){  

##### document.writeln(data);  

##### }  

##### a();//calling javascript function  

##### b();  

##### </script>  

##### </body>  

##### </html>

### Declaring JavaScript global variable within function

We need to use the window object to declare a JavaScript global variable within a function.

#### Example

##### window.value=90;

#### It can now be declared within any function and accessed from within any function.

#### Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function a(){  

##### window.value=50; //declare global variable by use of window object  

##### }  

##### function b(){  

##### alert(window.value);//access global variable from other function  

##### }  

##### a();  

##### b();      

##### </script>  

##### </body>  

##### </html>

# Javascript Data Types

It has a variety of data types to store various types of values.

In Javascript, there are two kinds of data types.

1.  Primitive data types.
2.  Non-primitive data types.

### Since JavaScript is a dynamic style language, we don't need to define the type of variable because the JavaScript engine uses it dynamically. The data type is defined using var in this case. It can store any sort of value, including numbers, strings, and objects.

### Example

##### var a=Ram; //String   

##### var b=20; //Number  

##### var x= {FirstName:''Ram'', lastName:''Doe''}; //Object

### JavaScript primitive data types

There are 5 types of primitive data types in JavaScript.

![](Images/image00105.jpeg)

## JavaScript non-primitive data types

There is 3 non-primitive data types are as follows:

![](Images/image00106.jpeg)

Operators are symbols in JavaScript that are used to execute operations on operands. 3+2 equals 5 in plain terms. The operands here are 3 and 2, and the operator is +.

Following are the operators used in JavaScript:

1.  Arithmetic Operators.
2.  Comparison (relational) Operators.
3.  Bitwise Operators.
4.  Logical Operators.
5.  Assignment Operators.
6.  Special Operators.

## Arithmetic Operators

We use arithmetic operations on the operands in arithmetic operators.

![](Images/image00107.jpeg)

## Comparison Operators

In the Comparison Operator, two operands A and B are compared.

![](Images/image00108.jpeg)

## Assignment operator

The following assign operators are supported by JavaScript.

![](Images/image00109.jpeg)

### Bitwise Operators

The following bitwise operators are provided by JavaScript:

![](Images/image00110.jpeg)

## Logical Operators

#### Boolean values are commonly used for logical operators.

#### The logical operators are as follows:

![](Images/image00111.jpeg)

# Javascript If Else

A conditional statement in JavaScript is used to perform various tasks depending on the conditions.

In JavaScript, there are three types of statements.

1.  if Statement.
2.  if else Statement.
3.  if else if Statement.

## if statement

##### If the condition is true or false, the if statement is used in JavaScript to execute the code.

##### if (condition){ //   

#####     //content to be evaluated

##### }

![](Images/image00112.jpeg)

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=50;  

##### if(x>30){  

##### document.write("value of x is greater than 30");  

##### }  

##### </script >  

##### </body>  

##### </html>

#### OUTPUT

##### Value of x is greater than 30

## if else statement

### If either condition is true or false, the if else statement is used.

### Syntax

##### if(condition)  

##### {  

##### // set of statements  

##### }  

##### else  

##### {  

##### // set of statements  

##### }

![](Images/image00113.jpeg)

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=20;  

##### if(x%2==0){  

##### document.write("x is even number");  

##### }  

##### else{  

##### document.write("a is odd number")  

##### }  

##### </script>  

##### </body>  

##### </html>

### OUTPUT

##### X is even number

## If else if

### It just looks at the material to see if the expression is valid through several expressions. If else if is a more advanced version of the if else statement.

### Syntax

##### If (condition1)  

##### {  

##### Statement(s) to be executed if condition 1 is true  

##### }  

##### else if (condition 2)  

##### {  

##### Statement(s) to be executed if condition 2 is true  

##### }  

##### else if (condition 3)  

##### {  

##### Statement(s) to be executed if condition 3 is true  

##### }  

##### else  

##### {     

##### Statement(s) to be executed if no condition is true  

##### }

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=50;  

##### if (x==10){  

##### document.write("x is equal to 10");  

##### }  

##### else if(x==50){  

##### document.write("x is equal to 50");  

##### }  

##### else if(x==30){  

##### document.write("x is equal to 30");  

##### }  

##### else{  

##### document.write("a is not equal to 10, 50 or 30");  

##### }     

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### x is equal to 50

# Javascript Switch Statement

In JavaScript, the switch statement is used to execute a single code under different conditions. It's the same as the else if statement.

![](Images/image00114.jpeg)

### SYNTAX

##### switch (expression)  

##### {  

##### case 1: statement(s)  

##### break;  

##### case 2: statement(s)  

##### break;  

##### â€¦..  

##### case n: statement(s)  

##### break;  

##### default: statements(s)  

##### }

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var grade='B';  

##### var result;  

##### switch(grade){  

##### case 'A':  

##### result="A Grade";  

##### break;  

##### case 'B':  

##### result="B Grade";  

##### break;  

##### case 'C':  

##### result="C Grade";  

##### break;  

##### default:  

##### result="No Grade";  

##### }  

##### document.write(result);  

##### </script>  

##### </body>  

##### </html>

## OUTPUT

##### B Grade

# JavaScript Function

## The ability to build new functions inside the <Script>.....</script> tag is an essential feature of JavaScript. The function keyword is used to declare a function in JavaScript.

## To reuse the file, we call the JavaScript function multiple times.

## Advantages - JavaScript functions

1\. Code reusability: We use the same feature several times to save time and code.

2\. Less coding: Our software is compressed as a result of this. When we perform a routine mission, we don't write a lot of code.

### Syntax

##### function functionName(parameter or not)  

##### {  

##### statements  

##### }

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function msg()  

##### {  

##### alert("Hello! world");  

##### }  

##### </script>  

##### <input type="button" onclick="msg()" value="click here"/>  

##### </body>  

##### </html>

#### OUTPUT

##### Hello world!

## Function with arguments

#### Call function by passing arguments.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function getcube(number)  

##### {  

##### alert(number* number* number);  

##### }  

##### </script>  

##### <form>  

##### <input type="button" value="click" onclick="getcube(3)"/>  

##### </form>  

##### </body>  

##### </html>

#### OUTPUT

27

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function getname()  

##### {  

##### name=prompt("Enter the Name");  

##### alert("Welcome Mr/Mrs " + name);  

##### }  

##### </script>  

##### </body>  

##### <form>  

##### <input type="button" value="Click" onclick="getname()"/>  

##### </form>  

##### </html>

## Function with return value

#### Call function that return value and use it in program.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function getInfo()  

##### {  

##### return "Hello Raj! How are you?";  

##### }  

##### </script>  

##### <script>  

##### document.write(getInfo());  

##### </script>  

##### </body>  

##### </html>

### OUTPUT

##### Hello Raj! How are you?

## The Function() Constructor

### A function statement isn't only for defining new functions; it can also be used to define functions dynamically using the Function() constructor and the new operator.

### Syntax

##### <script>  

#####     var variablename = new Function(Arg1, Arg2...,  "Function Body" );   

##### </script>

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script>  

##### var func = new Function("a", "b", "return a+b;");  

##### function secondFunction(){  

##### var result;  

##### result = func(50,50);  

##### document.write ( result );  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <p>Click button to call the function</p>  

##### <form>  

##### <input type="button" onclick="secondFunction()" value="Call Function">  

##### </form>  

##### <p>Use different parameters inside the function and try yourself...</p>  

##### </body>  

##### </html>

## Function Literals

### The definition of function literals, which is another way to describe functions, is introduced in JavaScript 1.2\. It's an expression that describes a function that doesn't have a name.

### The syntax for a function literal is similar to that of a function statement, except that it is used as an expression rather than a statement, and there is no need for a function name.

### Syntax

##### <script>  

##### var variablename = function (Argument List){  

#####           Function Body  

##### };    

##### </script>

### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script>  

##### var func = function(a,b){ return a+b };  

##### function secondFunction(){  

##### var result;  

##### result = func(10,20);  

##### document.write ( result );  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <p>Click the button to call the function</p>  

##### <form>  

##### <input type="button" onclick="secondFunction()" value="Call Function">  

##### </form>  

##### <p>Use different parameters inside the function and try yourself...</p>  

##### </body>  

##### </html>

# Javascript Object

An object is a state-and-behavioral entity. JavaScript is a scripting language that focuses on objects. While JavaScript is template-based rather than class-based, it allows us to build objects directly.

#### SYNTAX

##### objectName.objectProperty = propertyValue;

To write some content on the text, we use the write() method on document properties.

##### Document.write("Hello world")

#### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <title>User-defined objects</title>  

##### <script type="text/javascript">  

##### var book = new Object();   // Object created  

##### book.subject = "5 points someone"; // Properties assign to the object  

##### book.author  = "ChetanBhagat";  

##### </script>  

##### </head>  

##### <body>  

##### <script type="text/javascript">  

##### document.write("Book Name is : " + book.subject + "<br>");  

##### document.write("Book Author is : " + book.author + "<br>");  

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### Book Name is: 5 points someone

##### Book Author is: Chetan Bhagat

### Methods of  Object

#### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <title>User-defined objects</title>  

##### <script type="text/javascript">// Define a function which will work as a method  

##### function addPrice(amount){  

##### this.price = amount;   

##### }  

##### function book(title, author){  

##### this.itle = title;  

##### this.author  = author;  

##### this.addPrice = addPrice; // Assign that method as property.  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <script type="text/javascript">  

##### varmyBook = new book("5 Points Someone", "ChetanBhagat");  

##### myBook.addPrice(150);  

##### document.write("Book Title is : " + myBook.title + "<br>");  

##### document.write("Book Author is : " + myBook.author + "<br>");  

##### document.write("Book Price is : " + myBook.price + "<br>");  

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

Book Title is: 5 Points Someone

Book Author is :ChetanBhagat

Book Price is : 150

# Javascript array

Arrays are used to describe a set of elements in a single unit or memory place.

Any element that enters the array will be stored in the array with a unique index starting at zero. We can store data with the aid of indexes.

In JavaScript, we must use the new keyword to declare an array. We use new Array to generate an array (n).

The number of slots in the sequence is denoted by n.

#### SYNTAX

##### myarray = new array(n);

NOTE: If we generate an array in JavaScript without specifying the size, the array object will have a size of zero.

#### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var i;  

##### var emp = new Array();  

##### emp[0] = "Ajay";  

##### emp[1] = "Abhay";  

##### emp[2] = "Arun";  

##### emp[3] = "Shipra";  

##### for (i=0; i<emp.length; i++)  

##### {  

##### document.write(emp[i] + "<br>");  

##### }  

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### Ajay

##### Abhay

##### Arun

##### Shipra

#### EXAMPLE 2

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script type="text/javascript">  

##### function array()  

##### {  

##### num = new Array(5)  

##### num[0] = 10  

##### num[1] = 20  

##### num[2] = 30  

##### num[3] = 40  

##### num[4] = 50  

##### sum = 0;  

##### for (i=0; i<num.length; i++)  

##### {  

##### sumsum = sum + num[i];  

##### }  

##### alert(sum)  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <input type="button" onclick="array()" value="click here">  

##### </body>  

##### </html>

### FUNCTIONS IN ARRAY

![](Images/image00115.jpeg)

# Javascript String

The String object is used to interact with a string of characters. It's a tool for storing and manipulating text.

In JavaScript, there are two ways to make a string:

1.  String literal.
2.  Using new keyword.

String literals are formed by using double quotes.

#### SYNTAX

##### var stringname="string value";

#### EXAMPLE

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var str="Hello String Literal";  

##### document.write(str);   

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### Hello String Literal

## Using new keyword

#### SYNTAX

##### var stringname=new String("new keyword")

#### OUTPUT

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var stringname=new String("Hello String");  

##### document.write(stringname);  

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### Hello String

## String properties

There is a list of string object properties as well as their descriptions.

1.  constructor.
2.  length.
3.  prototype.

Constructor– This method returns a reference to the object's string function.

#### SYNTAX

##### string.constructor

Length - The number of characters in a string is returned.

#### SYNTAX

##### string.length

Prototype - It allowed any object to have properties and methods applied to it (Number, Boolean, string, and data etc.).

#### SYNTAX

##### object.prototype.name = value

#### METHODS

![](Images/image00116.jpeg)

## charAt()

It's a method for getting the character from a given index.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var str = new String( "Hello" );  

##### document.writeln("str.charAt(0) is: " + str.charAt(0));   

##### document.writeln("<br />str.charAt(1) is: " + str.charAt(1));   

##### document.writeln("<br />str.charAt(2) is: " + str.charAt(2));   

##### document.writeln("<br />str.charAt(3) is: " + str.charAt(3));   

##### document.writeln("<br />str.charAt(4) is: " + str.charAt(4));   

##### </script>  

##### </body>  

##### </html>

## concat(str)

This method returns a new string after adding two or more strings.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>    

##### var x="Hello";    

##### var y="World";    

##### var z=x+y;    

##### document.write(z);    

##### </script>    

##### </body>  

##### </html>

## indexOf(str)

index of a string The index position of the given string is returned by the Of(str) procedure.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>    

##### var x="Tutorial provide by tutorialandexample";    

##### var y=x.indexOf("by");    

##### document.write(y);    

##### </script>    

##### </body>  

##### </html>

## lastindexOf(str)

The string lastIndexOf(str) method returns the string's last index position.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>    

##### var x="Tutorial provide by tutorialandExamole";    

##### var y=x.lastIndexOf("by");    

##### document.write(n);    

##### </script>    

##### </body>  

##### </html>

## match()

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var str = "To more detail, see Chapter 2.5.4.1";  

##### var re = /(chapter \d+(\.\d)*)/i;  

##### var find = str.match( re );  

##### document.write(find );   

##### </script>  

##### </body>  

##### </html>

## toLowerCase()

It returns a lowercase version of the given string.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>    

##### var x="HELLO WORLD";    

##### var y=x.toLowerCase();    

##### document.write(y);    

##### </script>    

##### </body>  

##### </html>

## toUpperCase()

The provided string is returned in uppercase letters.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>    

##### var x="hello world";    

##### var y=x.toUpperCase();    

##### document.write(y);    

##### </script>    

##### </body>  

##### </html>

## valueOf()

It returns the string object's primitive value.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var str = new String("Hello world");  

##### document.write(str.valueOf( ));  

##### </script>  

##### </body>  

##### </html>

# Javascript Date

Date Object is a data form that is built into the JavaScript language. The new Date object is used to construct data objects (). A single moment in time is represented by a JavaScript Date case. The only way to create a JavaScript date object is to use JavaScript as a constructor.

#### SYNTAX

The Date() constructor can be used to generate a Date object using the following syntaxes.

##### new Date();  

##### new Date(value);  

##### new Date(dateString);  

##### new Date(year, month, day, hours, minutes, seconds, milliseconds);

#### NOTE: Bracketed parameters are always optional.

### Descriptions

### year

The year is represented by an integer number. Map of values ranging from 0 to 99 for the years 2000 to 2099.

### Month

Beginning with 0 for January and ending with 11 for December, this integer value represents the month.

### Date

It's an option. The month's day is represented by an integer value.

### Hours

It's an option. The hours of the day are represented by an integer value.

### Minutes

It's an option. The minute section of time is represented by an integer value.

### Seconds

It's an option. The second time segment is represented by an integer value.

### Milliseconds

It's an option. A millisecond segment of time is represented by an integer value.

### Example of Date

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var date=new Date();    

##### var day=date.getDate();    

##### var month=date.getMonth()+1;    

##### var year=date.getFullYear();    

##### document.write("<br>Date: "+day+"/"+month+"/"+year);    

##### </script>  

##### </body>  

##### </html

### Current Time  - Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### Current Time: <span id="txt"></span>  

##### <script>  

##### var today=new Date();    

##### var h=today.getHours();    

##### var m=today.getMinutes();    

##### var s=today.getSeconds();    

##### document.getElementById('txt').innerHTML=h+":"+m+":"+s;    

##### </script>  

##### </body>  

##### </html>

# JavaScript Math

Math is a built-in object with properties and methods for mathematical functions and constants.

It enables you to carry out mathematical operations on numbers.

#### Syntax

1.  varpi_val = Math.PI;
2.  varsin_val = Math.sin(30);

### Examples

### Math.pow()

The value of x to the power of y is returned by Math.pow(x,y):

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <h2>JavaScript Math.pow()</h2>  

##### <p>Math.pow(x,y) returns the value of x to the power of y:</p>  

##### <p id="demo"></p>  

##### <script>  

##### document.getElementById("demo").innerHTML = Math.pow(6,2);  

##### </script>  

##### </body>  

##### </html>

### Math.sqrt()

#### The square root of x is returned by Math.sqrt(x).

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <h2>JavaScript Math.sqrt()</h2>  

##### <p>Math.sqrt(x) returns the square root of x:</p>  

##### <p id="demo"></p>  

##### <script>  

##### document.getElementById("demo").innerHTML = Math.sqrt(81);  

##### </script>  

##### </body>  

##### </html>

### Math.ceil()

#### The value of x rounded up to the nearest integer is returned by Math.ceil(x):

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <h2>JavaScript Math.ceil()</h2>  

##### <p>Math.ceil() rounds a number <strong>up</strong> to its nearest integer:</p>  

##### <p id="demo"></p>  

##### <script>  

##### document.getElementById("demo").innerHTML = Math.ceil(6.8);  

##### </script>  

##### </body>  

##### </html>

# Javascript Number

The Number object is a wrapper object that lets you manipulate numerical values.

The Number() constructor is used to build the number object.

It could be either an integer or a floating-point number.

#### SYNTAX

##### var n=new Number(value);

#### EXAMPLES

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=100;//integer value  

##### var y=100.7;//floating point value  

##### var z=12e5;//exponent value, output: 1200000  

##### var n=new Number(20);//integer value by number object    

##### document.write(x+" "+y+" "+z+" "+n);  

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### 100 100.7 1200000 20

### Description

The number object is most commonly used for the following purposes:

1.  It returns NaN if the claim cannot be converted to a number (Not a Number).
2.  Number can be used to perform a type conversion in a non-constructor context (i.e., without the new operator).

### JavaScript Number Constants

![](Images/image00117.jpeg)