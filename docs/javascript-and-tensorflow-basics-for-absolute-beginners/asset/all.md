![](Image00049.jpg)

JAVASCRIPT AND TENSORFLOW

BASICS

FOR ABSOLUTE BEGINNERS

BY

TAM SEL

[JAVASCRIPT](#text00003.html__Toc77594366)

[JAVASCRIPT EXAMPLE](#text00003.html__Toc77594367)

[Javascript comment](#text00004.html__Toc77594368)

[Javascript Variable](#text00005.html__Toc77594369)

[Javascript Data Types](#text00006.html__Toc77594370)

[Javascript If Else](#text00007.html__Toc77594371)

[Javascript Switch Statement](#text00008.html__Toc77594372)

[JavaScript Function](#text00009.html__Toc77594373)

[Javascript Object](#text00010.html__Toc77594374)

[Javascript array](#text00011.html__Toc77594375)

[Javascript String](#text00012.html__Toc77594376)

[Javascript Date](#text00013.html__Toc77594377)

[JavaScript Math](#text00014.html__Toc77594378)

[Javascript Number](#text00015.html__Toc77594379)

[TensorFlow INTRODUCTION](#text00017.html__Toc77594380)

[TensorFlow Brief History](#text00018.html__Toc77594381)

[TensorFlow Installation Through pip](#text00019.html__Toc77594382)

[TensorFlow Installation through conda](#text00020.html__Toc77594383)

[TensorFlow Architecture](#text00021.html__Toc77594384)

[TensorFlow Advantage and Disadvantage](#text00022.html__Toc77594385)

[TensorFlow Playground](#text00023.html__Toc77594386)

[Basics of TensorFlow](#text00024.html__Toc77594387)

[TensorFlow - Single Layer Perceptron](#text00025.html__Toc77594388)

[TensorFlow - Multi-layer Perceptron](#text00026.html__Toc77594389)

[Machine Learning and Deep Learning](#text00027.html__Toc77594390)

[TensorFlow Artificial Neural Network](#text00029.html__Toc77594391)

[TensorFlow Linear Regression](#text00030.html__Toc77594392)

JAVASCRIPT

CODING BASICS

FOR ABSOLUTE BEGINNERS

BY

TAM SEL

# JAVASCRIPT

This JavaScript tutorial makes it easy for both beginners and experts to learn JavaScript.

To learn JavaScript, you only need a basic understanding of computers.

# JAVASCRIPT EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <h2>Welcom e  t o  JavaScript</h2 >   

##### <script >   

##### document.write("Hello Friends") ;   

##### </script >   

##### </body >   

##### </html>

JavaScript can be implemented by adding JavaScript statements in the code.

< scrip t >… < /scrip t >.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <scrip t  type =  "text/javascript" >   

##### document.write("Hello World") ;   

##### </script >   

##### </body >   

##### </html>

### JavaScript code can be written in 3 places in JavaScript

1.  Between the <body>……</body> tag of HTML.
2.  Between the <head>……</head> tag of HTML.
3.  In .jsfile(external JavaScript).

### Example (code between the body tags)

##### In the example below, the body tag contains JavaScript code.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <scrip t  type="text/javascript" >   

##### alert("Hello world") ;   

##### </script >   

##### </body >   

##### </html>

### Example2 (code between the head tag)

##### We'll create the function msg() in the example below . In JavaScript, you must write function in function name to construct a function. To call a method, we must first create a case. We're using the one-click event to call the msg() function in this case.

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <scrip t  type="text/javascript" >   

##### functio n  msg() {   

##### alert("Hello world") ;   

##### }   

##### </script >   

##### </head >   

##### <body >   

##### <p>Welcom e  t o  Javascript</p >   

##### <form >   

##### <inpu t  type="button "  value="click "  onclick="msg()"/ >   

##### </form >   

##### </body >   

##### </html>

### External JavaScript file

### We can build a JavaScript file that we can use in HTML files.

### Since a single JavaScript file can be used in several HTML pages, it allows for code reuse.

### It improves the web page's efficiency.

### The file must have a .js extension.

### Example

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <scrip t  type="text/javascript "  src="message.js"></script >   

##### </head >   

##### <body >   

##### <p>Hell o  world</p >   

##### <form >   

##### <inpu t  type="button "  value="click "  onclick="msg()"/ >   

##### </form >   

##### </body >   

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

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### // single-line comment //  

##### document.write("hello world") ;   

##### </script >   

##### </body >   

##### </html>

eg. Comment added after the statement.

##### 
<!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  a=10 ;   

##### va r  b=20 ;   

##### va r  c=a+b ;  //It add values of a and b variable  

##### document.write(c) ;  // print sum of 10 and 20  

##### </script >   

##### </body >   

##### </html>

### Output

30

## Multi-line comment

### Single and multi-line comments can also be made for multi-line comments. Comments that span multi lines begin with /* and end with */. JavaScript will ignore the text in between them.

### /* Write comment here */

#### Example

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### /* It is multi-line comment.  

##### It will not be displayed * /   

##### document.writ e  ("Example of JavaScript multi line comment") ;   

##### </script >   

##### </body >   

##### </html

# Javascript Variable

Values (name=”Ram”) and expressions (Sum=x+y) are stored in variables.

We must first declare a variable before using it. To declare a variable, we use the keyword var as follows:

##### var name;

There are two types of variables:

1.  Local Variable
2.  Global Variable

Local Variabl e – It's declared within a function or a block.

#### Example

##### <script >   

##### functionabc() {   

##### va r  x=10 ;  //local variable  

##### </script>

Global Variabl e - It has a global scope, meaning that it can be specified anywhere in JavaScript code.

Outside of the function, a variable is declared.

#### Example

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  dat a  =200 ;  //global variable  

##### functio n  a() {   

##### document.writeln(data) ;   

##### }   

##### functio n  b() {   

##### document.writeln(data) ;   

##### }   

##### a();//calling javascript function  

##### b() ;   

##### </script >   

##### </body >   

##### </html>

### Declaring JavaScript global variable within function

We need to use the window object to declare a JavaScript global variable within a function.

#### Example

##### window.value=90;

#### It can now be declared within any function and accessed from within any function.

#### Example

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### functio n  a() {   

##### window.value=50 ;  //declare global variable by use of window object  

##### }   

##### functio n  b() {   

##### alert(window.value);//access global variable from other function  

##### }   

##### a() ;   

##### b() ;       

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

##### va r  a=Ram ;  //String   

##### va r  b=20 ;  //Number  

##### va r  x =  {FirstName:''Ram'' ,  lastName:''Doe''} ;  //Object

### JavaScript primitive data types

There are 5 types of primitive data types in JavaScript.

![](Image00000.jpg)

## JavaScript non-primitive data types

There is 3 non-primitive data types are as follows:

![](Image00001.jpg)

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

![](Image00002.jpg)

## Comparison Operators

In the Comparison Operator, two operands A and B are compared.

![](Image00003.jpg)

## Assignment operator

The following assign operators are supported by JavaScript.

![](Image00004.jpg)

### Bitwise Operators

The following bitwise operators are provided by JavaScript:

![](Image00005.jpg)

## Logical Operators

#### Boolean values are commonly used for logical operators.

#### The logical operators are as follows:

![](Image00006.jpg)

# Javascript If Else

A conditional statement in JavaScript is used to perform various tasks depending on the conditions.

In JavaScript, there are three types of statements.

1.  if Statement.
2.  if else Statement.
3.  if else if Statement.

## if statement

##### If the condition is true or false, the if statement is used in JavaScript to execute the code.

##### i f  (condition) {  //   

#####       //content to be evaluated

##### }

![](Image00007.jpg)

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  x=50 ;   

##### if(x>30) {   

##### document.write("value of x is greater than 30") ;   

##### }   

##### </scrip t >   

##### </body >   

##### </html>

#### OUTPUT

##### Value of x is greater than 30

## if else statement

### If either condition is true or false, the if else statement is used.

### Syntax

##### if(condition )   

##### {   

##### // set of statements  

##### }   

##### els e   

##### {   

##### // set of statements  

##### }

![](Image00008.jpg)

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  x=20 ;   

##### if(x%2==0) {   

##### document.write("x is even number") ;   

##### }   

##### else {   

##### document.write("a is odd number" )   

##### }   

##### </script >   

##### </body >   

##### </html>

### OUTPUT

##### X is even number

## If else if

### It just looks at the material to see if the expression is valid through several expressions. If else if is a more advanced version of the if else statement.

### Syntax

##### I f  (condition1 )   

##### {   

##### Statement(s )  t o  b e  execute d  i f  conditio n 1  i s  tru e   

##### }   

##### els e  i f  (conditio n  2 )   

##### {   

##### Statement(s )  t o  b e  execute d  i f  conditio n 2  i s  tru e   

##### }   

##### els e  i f  (conditio n  3 )   

##### {   

##### Statement(s )  t o  b e  execute d  i f  conditio n 3  i s  tru e   

##### }   

##### els e   

##### {      

##### Statement(s )  t o  b e  execute d  i f  n o  conditio n  i s  tru e   

##### }

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  x=50 ;   

##### i f  (x==10) {   

##### document.write("x is equal to 10") ;   

##### }   

##### els e  if(x==50) {   

##### document.write("x is equal to 50") ;   

##### }   

##### els e  if(x==30) {   

##### document.write("x is equal to 30") ;   

##### }   

##### else {   

##### document.write("a is not equal to 10, 50 or 30") ;   

##### }     

##### </script>  

##### </body>  

##### </html>

#### OUTPUT

##### x is equal to 50

# Javascript Switch Statement

In JavaScript, the switch statement is used to execute a single code under different conditions. It's the same as the else if statement.

![](Image00009.jpg)

### SYNTAX

##### switc h  (expression )   

##### {   

##### cas e  1 :  statement(s )   

##### break ;   

##### cas e  2 :  statement(s )   

##### break ;   

##### â€ ¦ . .   

##### cas e  n :  statement(s )   

##### break ;   

##### default :  statements(s )   

##### }

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  grade='B' ;   

##### va r  result ;   

##### switch(grade) {   

##### cas e  'A' :   

##### result="A Grade" ;   

##### break ;   

##### cas e  'B' :   

##### result="B Grade" ;   

##### break ;   

##### cas e  'C' :   

##### result="C Grade" ;   

##### break ;   

##### default :   

##### result="No Grade" ;   

##### }   

##### document.write(result) ;   

##### </script >   

##### </body >   

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

##### functio n  functionName(paramete r  o r  not )   

##### {   

##### statement s   

##### }

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### functio n  msg( )   

##### {   

##### alert("Hello! world") ;   

##### }   

##### </script >   

##### <inpu t  type="button "  onclick="msg() "  value="click here"/ >   

##### </body >   

##### </html>

#### OUTPUT

##### Hello world!

## Function with arguments

#### Call function by passing arguments.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### functio n  getcube(number )   

##### {   

##### alert(number *  number *  number) ;   

##### }   

##### </script >   

##### <form >   

##### <inpu t  type="button "  value="click "  onclick="getcube(3)"/ >   

##### </form >   

##### </body >   

##### </html>

#### OUTPUT

27

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### functio n  getname( )   

##### {   

##### name=prompt("Enter the Name") ;   

##### alert("Welcome Mr/Mrs  " +  name) ;   

##### }   

##### </script >   

##### </body >   

##### <form >   

##### <inpu t  type="button "  value="Click "  onclick="getname()"/ >   

##### </form >   

##### </html>

## Function with return value

#### Call function that return value and use it in program.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### functio n  getInfo( )   

##### {   

##### retur n  "Hello Raj! How are you?" ;   

##### }   

##### </script >   

##### <script >   

##### document.write(getInfo()) ;   

##### </script >   

##### </body >   

##### </html>

### OUTPUT

##### Hello Raj! How are you?

## The Function() Constructor

### A function statement isn't only for defining new functions; it can also be used to define functions dynamically using the Function() constructor and the new operator.

### Syntax

##### <script >   

#####       va r  variablenam e =  ne w  Function(Arg1 ,  Arg2... ,     "Function Body "  ) ;    

##### </script>

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <script >   

##### va r  fun c =  ne w  Function("a" ,  "b" ,  "return a+b;") ;   

##### functio n  secondFunction() {   

##### va r  result ;   

##### resul t =  func(50,50) ;   

##### document.writ e (  resul t  ) ;   

##### }   

##### </script >   

##### </head >   

##### <body >   

##### <p>Clic k  butto n  t o  cal l  th e  function</p >   

##### <form >   

##### <inpu t  type="button "  onclick="secondFunction() "  value="Call Function" >   

##### </form >   

##### <p>Us e  differen t  parameter s  insid e  th e  functio n  an d  tr y  yourself...</p >   

##### </body >   

##### </html>

## Function Literals

### The definition of function literals, which is another way to describe functions, is introduced in JavaScript 1.2\. It's an expression that describes a function that doesn't have a name.

### The syntax for a function literal is similar to that of a function statement, except that it is used as an expression rather than a statement, and there is no need for a function name.

### Syntax

##### <script >   

##### va r  variablenam e =  functio n  (Argumen t  List) {   

#####             Functio n  Bod y   

##### } ;     

##### </script>

### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <script >   

##### va r  fun c =  function(a,b) {  retur n  a+ b  } ;   

##### functio n  secondFunction() {   

##### va r  result ;   

##### resul t =  func(10,20) ;   

##### document.writ e (  resul t  ) ;   

##### }   

##### </script >   

##### </head >   

##### <body >   

##### <p>Clic k  th e  butto n  t o  cal l  th e  function</p >   

##### <form >   

##### <inpu t  type="button "  onclick="secondFunction() "  value="Call Function" >   

##### </form >   

##### <p>Us e  differen t  parameter s  insid e  th e  functio n  an d  tr y  yourself...</p >   

##### </body >   

##### </html>

# Javascript Object

An object is a state-and-behavioral entity. JavaScript is a scripting language that focuses on objects. While JavaScript is template-based rather than class-based, it allows us to build objects directly.

#### SYNTAX

##### objectName.objectProperty = propertyValue;

To write some content on the text, we use the write() method on document properties.

##### Document.write("Hello world")

#### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <title>User-define d  objects</title >   

##### <scrip t  type="text/javascript" >   

##### va r  boo k =  ne w  Object() ;      // Object created  

##### book.subjec t =  "5 points someone" ;  // Properties assign to the object  

##### book.autho r    =  "ChetanBhagat" ;   

##### </script >   

##### </head >   

##### <body >   

##### <scrip t  type="text/javascript" >   

##### document.write("Book Name is :  " +  book.subjec t +  "<br>") ;   

##### document.write("Book Author is :  " +  book.autho r +  "<br>") ;   

##### </script >   

##### </body >   

##### </html>

#### OUTPUT

##### Book Name is: 5 points someone

##### Book Author is: Chetan Bhagat

### Methods of  Object

#### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <title>User-define d  objects</title >   

##### <scrip t  type="text/javascript">// Define a function which will work as a method  

##### functio n  addPrice(amount) {   

##### this.pric e =  amount ;    

##### }   

##### functio n  book(title ,  author) {   

##### this.itl e =  title ;   

##### this.autho r    =  author ;   

##### this.addPric e =  addPrice ;  // Assign that method as property.  

##### }   

##### </script >   

##### </head >   

##### <body >   

##### <scrip t  type="text/javascript" >   

##### varmyBoo k =  ne w  book("5 Points Someone" ,  "ChetanBhagat") ;   

##### myBook.addPrice(150) ;   

##### document.write("Book Title is :  " +  myBook.titl e +  "<br>") ;   

##### document.write("Book Author is :  " +  myBook.autho r +  "<br>") ;   

##### document.write("Book Price is :  " +  myBook.pric e +  "<br>") ;   

##### </script >   

##### </body >   

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

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  i ;   

##### va r  em p =  ne w  Array() ;   

##### emp[0 ] =  "Ajay" ;   

##### emp[1 ] =  "Abhay" ;   

##### emp[2 ] =  "Arun" ;   

##### emp[3 ] =  "Shipra" ;   

##### fo r  (i=0 ;  i<emp.length ;  i++ )   

##### {   

##### document.write(emp[i ] +  "<br>") ;   

##### }   

##### </script >   

##### </body >   

##### </html>

#### OUTPUT

##### Ajay

##### Abhay

##### Arun

##### Shipra

#### EXAMPLE 2

##### <!DOCTYP E  html >   

##### <html >   

##### <head >   

##### <scrip t  type="text/javascript" >   

##### functio n  array( )   

##### {   

##### nu m =  ne w  Array(5 )   

##### num[0 ] =  1 0   

##### num[1 ] =  2 0   

##### num[2 ] =  3 0   

##### num[3 ] =  4 0   

##### num[4 ] =  5 0   

##### su m =  0 ;   

##### fo r  (i=0 ;  i<num.length ;  i++ )   

##### {   

##### sumsu m =  su m +  num[i] ;   

##### }   

##### alert(sum )   

##### }   

##### </script >   

##### </head >   

##### <body >   

##### <inpu t  type="button "  onclick="array() "  value="click here" >   

##### </body >   

##### </html>

### FUNCTIONS IN ARRAY

![](Image00010.jpg)

# Javascript String

The String object is used to interact with a string of characters. It's a tool for storing and manipulating text.

In JavaScript, there are two ways to make a string:

1.  String literal.
2.  Using new keyword.

String literals are formed by using double quotes.

#### SYNTAX

##### var stringname="string value";

#### EXAMPLE

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  str="Hello String Literal" ;   

##### document.write(str) ;    

##### </script >   

##### </body >   

##### </html>

#### OUTPUT

##### Hello String Literal

## Using new keyword

#### SYNTAX

##### var stringname=new String("new keyword")

#### OUTPUT

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  stringname=ne w  String("Hello String") ;   

##### document.write(stringname) ;   

##### </script >   

##### </body >   

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

![](Image00011.jpg)

## charAt()

It's a method for getting the character from a given index.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  st r =  ne w  String (  "Hello "  ) ;   

##### document.writeln("str.charAt(0) is:  " +  str.charAt(0)) ;    

##### document.writeln("<br />str.charAt(1) is:  " +  str.charAt(1)) ;    

##### document.writeln("<br />str.charAt(2) is:  " +  str.charAt(2)) ;    

##### document.writeln("<br />str.charAt(3) is:  " +  str.charAt(3)) ;    

##### document.writeln("<br />str.charAt(4) is:  " +  str.charAt(4)) ;    

##### </script >   

##### </body >   

##### </html>

## concat(str)

This method returns a new string after adding two or more strings.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >     

##### va r  x="Hello" ;     

##### va r  y="World" ;     

##### va r  z=x+y ;     

##### document.write(z) ;     

##### </script >     

##### </body >   

##### </html>

## indexOf(str)

index of a string The index position of the given string is returned by the Of(str) procedure.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >     

##### va r  x="Tutorial provide by tutorialandexample" ;     

##### va r  y=x.indexOf("by") ;     

##### document.write(y) ;     

##### </script >     

##### </body >   

##### </html>

## lastindexOf(str)

The string lastIndexOf(str) method returns the string's last index position.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >     

##### va r  x="Tutorial provide by tutorialandExamole" ;     

##### va r  y=x.lastIndexOf("by") ;     

##### document.write(n) ;     

##### </script >     

##### </body >   

##### </html>

## match()

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  st r =  "To more detail, see Chapter 2.5.4.1" ;   

##### va r  r e =  /(chapter \d+(\.\d)*)/i ;   

##### va r  fin d =  str.match (  r e  ) ;   

##### document.write(fin d  ) ;    

##### </script >   

##### </body >   

##### </html>

## toLowerCase()

It returns a lowercase version of the given string.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >     

##### va r  x="HELLO WORLD" ;     

##### va r  y=x.toLowerCase() ;     

##### document.write(y) ;     

##### </script >     

##### </body >   

##### </html>

## toUpperCase()

The provided string is returned in uppercase letters.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >     

##### va r  x="hello world" ;     

##### va r  y=x.toUpperCase() ;     

##### document.write(y) ;     

##### </script >     

##### </body >   

##### </html>

## valueOf()

It returns the string object's primitive value.

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  st r =  ne w  String("Hello world") ;   

##### document.write(str.valueOf (  )) ;   

##### </script >   

##### </body >   

##### </html>

# Javascript Date

Date Object is a data form that is built into the JavaScript language. The new Date object is used to construct data objects (). A single moment in time is represented by a JavaScript Date case. The only way to create a JavaScript date object is to use JavaScript as a constructor.

#### SYNTAX

The Date() constructor can be used to generate a Date object using the following syntaxes.

##### ne w  Date() ;   

##### ne w  Date(value) ;   

##### ne w  Date(dateString) ;   

##### ne w  Date(year ,  month ,  day ,  hours ,  minutes ,  seconds ,  milliseconds);

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

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  date=ne w  Date() ;     

##### va r  day=date.getDate() ;     

##### va r  month=date.getMonth()+1 ;     

##### va r  year=date.getFullYear() ;     

##### document.write("<br>Date: "+day+"/"+month+"/"+year) ;     

##### </script >   

##### </body >   

##### </html

### Current Time  - Example

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### Curren t  Time :  <spa n  id="txt"></span >   

##### <script >   

##### va r  today=ne w  Date() ;     

##### va r  h=today.getHours() ;     

##### va r  m=today.getMinutes() ;     

##### va r  s=today.getSeconds() ;     

##### document.getElementById('txt').innerHTML=h+":"+m+":"+s ;     

##### </script >   

##### </body >   

##### </html>

# JavaScript Math

Math is a built-in object with properties and methods for mathematical functions and constants.

It enables you to carry out mathematical operations on numbers.

#### Syntax

1.  varpi_val = Math.PI;
2.  varsin_val = Math.sin ( 3 0 );

### Examples

### Math.pow()

The value of x to the power of y is returned by Math.pow(x,y):

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <h2>JavaScrip t  Math.pow()</h2 >   

##### <p>Math.pow(x,y )  return s  th e  valu e  o f x  t o  th e  powe r  o f  y:</p >   

##### < p  id="demo"></p >   

##### <script >   

##### document.getElementById("demo").innerHTM L =  Math.pow(6,2) ;   

##### </script >   

##### </body >   

##### </html>

### Math.sqrt()

#### The square root of x is returned by Math.sqrt(x).

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <h2>JavaScrip t  Math.sqrt()</h2 >   

##### <p>Math.sqrt(x )  return s  th e  squar e  roo t  o f  x:</p >   

##### < p  id="demo"></p >   

##### <script >   

##### document.getElementById("demo").innerHTM L =  Math.sqrt(81) ;   

##### </script >   

##### </body >   

##### </html>

### Math.ceil()

#### The value of x rounded up to the nearest integer is returned by Math.ceil(x):

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <h2>JavaScrip t  Math.ceil()</h2 >   

##### <p>Math.ceil( )  round s a  numbe r  <strong>up</strong >  t o  it s  neares t  integer:</p >   

##### < p  id="demo"></p >   

##### <script >   

##### document.getElementById("demo").innerHTM L =  Math.ceil(6.8) ;   

##### </script >   

##### </body >   

##### </html>

# Javascript Number

The Number object is a wrapper object that lets you manipulate numerical values.

The Number() constructor is used to build the number object.

It could be either an integer or a floating-point number.

#### SYNTAX

##### var n=new Number(value);

#### EXAMPLES

##### <!DOCTYP E  html >   

##### <html >   

##### <body >   

##### <script >   

##### va r  x=100;//integer value  

##### va r  y=100.7;//floating point value  

##### va r  z=12e5;//exponent value, output: 1200000  

##### va r  n=ne w  Number(20);//integer value by number object    

##### document.write(x+" "+y+" "+z+" "+n) ;   

##### </script >   

##### </body >   

##### </html>

#### OUTPUT

##### 100 100.7 1200000 20

### Description

The number object is most commonly used for the following purposes:

1.  It returns NaN if the claim cannot be converted to a number (Not a Number).
2.  Number can be used to perform a type conversion in a non-constructor context (i.e., without the new operator).

### JavaScript Number Constants

![](Image00012.jpg)

TENSORFLOW

BASICS

FOR ABSOLUTE BEGINNERS

BY

TAM SEL

# TensorFlow INTRODUCTION

The TensorFlow Book is suitable for both beginners and experts.

The basic and advanced concepts of machine learning and deep learning, such as deep neural networks, image recognition, and sentiment analysis, are covered in our book.

TensorFlow is a well-known deep learning platform created by the Google Team.

This book is built in such a way that we can easily implement deep learning projects on TensorFlow in a simple and efficient way.

It is a free and open source software library written in the Python programming language.

TensorFlow is a Python-based framework. As a result, a basic understanding of Python is needed.

We can easily understand TensorFlow if we have a good understanding of basic mathematics and artificial intelligence concepts.

# TensorFlow Brief History

TensorFlow is a common machine learning and deep learning platform. It is a Google Brain Team-developed free and open-source library that was released on November 9, 2015\. It is entirely written in Python and uses it for numerical computation and data flow, making machine learning much quicker and easier.

TensorFlow can be used to train and run deep neural networks for a variety of tasks, including image recognition, handwritten digit classification, recurrent neural networks, word embedding, natural language processing, video detection, and more. TensorFlow runs on a variety of CPUs and GPUs, as well as mobile operating systems.

The word TensorFlow is made by two words, i.e., Tensor and Flow

1\. Tensor is a multidimensional array

2\. Flow is a term used to describe the flow of data in a system.

![TensorFlow Introduction](Image00013.jpg)

### History of TensorFlow

When given large amounts of data, deep learning began to outperform all other machine learning algorithms many years ago.

Google has realized that deep neural networks could be used to improve its services:

Search engine Google

Gmail (email)

Photograph

## They created the TensorFlow system to enable researchers and developers to collaborate on AI models.

## It can be used by a large number of people once it has been accepted and scaled.

## It was first released in 2015, and the first stable version was scheduled for release in 2017.

## It is an Apache Open Source License-compliant open-source framework.

## Without paying anything to Google, we can use, change, and reorganize the updated version for free.

## Components of TensorFlow

### Tensor

![](Image00014.jpg)

![TensorFlow Introduction](Image00015.jpg)

### Graphs

### A graph structure is used by TensorFlow. The graph compiles and summarizes all of the computations performed during the preparation.

### Advantages

*   It's now compatible with several CPUs or GPUs, as well as smartphone operating systems.
*   The graph's portability makes it possible to save computations for later use. Since the graph can be executed in the future, it can be saved.
*   The graph's entire computation is achieved by linking tensors.

Consider the following formula: a=(b+c)*(c+2)

The functions can be broken down into the following components:

d=b+c
e=c+2
a=d*e

Now, we can represent these operations graphically below:

![TensorFlow Introduction](Image00016.jpg)

### Session

The procedure from the graph can be executed by a session. We need to open a session in order to feed the graph with the value of a tensor.

To generate an output, we must run an operator within a session.

## Why is TensorFlow popular?

### ![](Image00017.jpg)

### Use Cases/Applications of TensorFlow

### ![](Image00018.jpg)

### 1\. Voice/Sound Recognition

![](Image00019.jpg)

### 2\. Image Recognition

![](Image00020.jpg)

### 3\. Time Series

![](Image00021.jpg)

### 4\. Video Detection

![](Image00022.jpg)

### 5\. Text-Based Applications

![](Image00023.jpg)

## Features of TensorFlow

### ![](Image00024.jpg)

### 1\. Responsive Construct

### We can see each section of the graph, which is not possible with Numpy or SciKit. To build a deep learning application, you'll need two or three things: a programming language, and two or three components.

### 2\. Flexible

### According to its operability, it is one of the most important TensorFlow Features. It's modular, and there are parts of it that we'd like to make stand-alone.

### 3\. Easily Trainable

It is simple to train on both the CPU and GPU in distributed computing.

### 4\. Parallel Neural Network Training

### TensorFlow adds value to the pipeline by allowing us to train multiple neural networks and GPUs simultaneously, making the models very powerful on large-scale systems.

### 5\. Large Community

### It was created by Google, and there is already a large team of software engineers working on continuous stability improvements.

### 6\. Open Source

### The best part about the machine learning library is that it is open source, which means that anybody with internet access can use it. As a result, people can exploit the library to create a wide range of useful items. It has also evolved into another DIY culture with a large platform for people who are just getting started with it as well as those who are having difficulty using it.

### 7\. Feature Columns

### Feature columns in TensorFlow can be thought of as intermediates between raw data and estimators, bridging input data with our model.

### The feature column is implemented as described in the feature column below.

### 8\. Availability of Statistical Distributions

This library includes distribution functions such as Bernoulli, Beta, Chi2, Uniform, and Gamma, which are crucial when using probabilistic methods including Bayesian models.

### 9\. Layered Components

TensorFlow generates layered weight and bias operations using functions like tf.contrib.layers, as well as batch normalization, convolution layer, and dropout layer. As a result, tf.contrib.layers. Optimizers like Adagrad, SGD, and Momentum are often used to solve optimization problems in numerical analysis.

### 10\. Visualizer (With TensorBoard)

With the aid of TensorBoard, we can inspect a different representation of a model and make the required changes while debugging it.

### 11.Event Logger (With TensorBoard)

It's similar to how we track the performance of tasks at the cmd on UNIX with tail - f. It tests the graph and output with the TensorBoard, recording events and summaries.

# TensorFlow Installation Through pip

We can download TensorFlow in our system in 2 ways:

1.  Through pip (Python package library)
2.  Through Anaconda Navigator (conda)

## 1\. Through pip

So, first and foremost, we must install and configure Anaconda in our system using pip.

TensorFlow must meet the following requirements in order to run on our computer.

*   On Windows, TensorFlow only supports 64-bit Python 3.5.x or Python 3.6.x.
*   The pip3 package manager is included when we download the Python 3.5.x version. (Which is the software that our users would need to install TensorFlow on Windows.)

Step 1:  Python can be downloaded from the link below.

:  [https://www.python.org/downloads/release/python-352/](https://www.python.org/downloads/release/python-352/)

After that,

Step 2:  We'll be taken to a new page where we'll have to choose between the x86-64 and amd64 installers to install Python.

The executable installer for Windows x86-64 is used here.

## What is pip?

## Pip is a package management system that is used to install and manage software packages written in Python or other programming languages. Pip is a Python package manager that allows you to download, browse, install, uninstall, and manage third-party Python packages. (pip3 is the most recent edition, which comes with Python 3.5.x, which we had just downloaded)

## Installing our TensorFlow

We can now finish up by downloading TensorFlow after we've downloaded the most recent version of Python.

Step 1:  Start the terminal to install TensorFlow. Ascertain that the cmd is run as an administrator.

Here's how we can function as an administrator in our cmd.

Open the Start menu, type cmd into the search box, and then right-click it and select Run as administrator.

Step 2:  After that, we type the command in the command prompt to complete the installation of Tensorflow in Windows.

Enter this command:

1.  C:\pip3 install -upgrade tensorflow  

TensorFlow has now been installed successfully in our system.

Testing our TensorFlow Here, we try to demonstrate that our new TensorFlow works as expected.

TensorFlow is successfully working now.

Otherwise, if we have any difficulties running the software, we must install Microsoft Visual C++ 2015\. The TensorFlow will then be run in our framework after it has been set up.

We can get Microsoft Visual C++ 2015 by clicking on the link below.:  [https://www.microsoft.com/en-us/download/confirmation.aspx?id=53587](https://www.microsoft.com/en-us/download/confirmation.aspx?id=53587)

# TensorFlow Installation through conda

We learned how to build TensorFlow using pip in the previous Book of TensorFlow. We will learn how to build TensorFlow using Conda in this book. To set up the platform, we'll need anaconda Navigator.

These are the steps to take, which are mentioned below:

To begin, go to Anaconda's official website and download Anaconda from the link below:  [https://www.anaconda.com/distribution/](https://www.anaconda.com/distribution/)

Then we need to get Anaconda from the Python 2.7 update.

It will be downloaded successfully into our system. Then we need to set up Anaconda on our machine.

It will be installed successfully in our system.

Then, to set up TensorFlow and libraries, we must run the provided order.

1.  Conda create -n tensorflow pip python is the first step.
2.  We are now downloading and installing the required components for TensorFlow to work.
3.  Next, we must determine if TensorFlow is operational in our framework.

# TensorFlow Architecture

The TensorFlow runtime is a library that runs on any platform. The device architecture that allows for this scale combination to be versatile.

TensorFlow programming principles such as the computation graph, operations, and sessions are common to us.

To comprehend TensorFlow architecture, some words must first be comprehended.

TensorFlow Servable, servable Streams, TensorFlow Models, Loaders, Sources, Manager, and Core are some of the terminology used.

The term and its role in TensorFlow's architecture are defined below.

To read and adjust the core TensorFlow code, the TensorFlow architecture is sufficient.

## 1\. TensorFlow Servable

In TensorFlow, these are the central unfinished units.

The artifacts that the clients use to perform the calculation are known as servables.

The size of a servable can vary. A single servable may be anything from a lookup table to a single interface model in a tuple of models.

Any sort and interface should be servable, allowing for versatility and potential enhancements such as:

*   Streaming results
*   Asynchronous modes of operation.
*   Experimental APIs

## 2\. Servable Versions

## Over the lifetime of a single server case, a TensorFlow server can handle one or more versions of the servables.

## It allows for the loading of new algorithm configurations, weights, and other data over time.

## They can also charge several versions of a servable at the same time.

## They often allow several versions of a servable to be loaded at the same time, allowing for incremental roll-out and experimentation.

## 3\. Servable Streams

## Any servable's versions are sorted by increasing version numbers in this sequence.

## 4\. TensorFlow Models

## In one or more servables, a serving represents a model. One or more algorithms are used to look up the embedding tables in a machine-learned model.

## A servable can also be used to represent a fraction of a model;

## for example, a broad lookup table can be represented by several instances.

## 5\. TensorFlow Loaders

## The life cycle of a servable is controlled by loaders. The loader API allows for a popular infrastructure that is independent of the learning algorithm, data, or product use-cases.

## 6\. Sources in TensorFlow Architecture

## Sources, to put it simply, are modules that look for and provide servable.

## At any given time, each reference provides zero or more servable streams.

## A source only provides one loader instance per servable stream for each servable.

## Each source also has one or more streams that can be served.

## A source only provides one loader instance for each servable stream and makes it available to be loaded.

## 7\. TensorFlow Managers

TensorFlow managers are in control of a Servable's entire lifecycle, including:

*   Loading Servables
*   Serving Servables
*   Unloading Servables

The manager keeps an eye on the sources and keeps track of all versions.

The Manager makes every effort to satisfy causes, but it has the ability to refuse to load an Aspired version.

## An "unload" can also be postponed by managers.

## For example, based on a policy to ensure that at least one version is loaded at all times, a manager may wait to unload until a newer version finishes loading.

## GetServableHandle (), for example, allows clients to access the loaded servable instances.

## 8\. TensorFlow Core

This is responsible for the following elements of servables:

*   Lifecycle
*   Metrics

## •         TensorFlow uses opaque artifacts to serve core satisfaction servables and loaders.

## 9\. Life of a Servable

TensorFlow Technical Architecture:

## •         Sources build loaders for Servable Versions, which are then submitted to the Manager as Aspired versions, where they will be loaded and served to client requests.

## •         The Loader holds metadata and is responsible for loading the servable.

## •         To convey the Manager of Aspired version, the source uses a callback.

## •         The Manager uses the current version strategy to decide the next course of action.

## •         If the Manager decides that the Loader can load a new version, clients request the servable from the Manager, either directly specifying a version or requesting the current version.

## •         For servable, the Manager returns a handle.

## 10\. TensorFlow Loaders

## One such algorithm backend is TensorFlow.

## For example, to load, provide access to, and unload an instance of a new form of servable of the machine learning model, we will introduce a new loader.

## 11\. Batcher in TensorFlow Architecture

In the presence of hardware accelerators and GPUs, batching TensorFlow requests into a single application will greatly reduce the cost of performing inference.

A claim batching system in TensorFlow serving allows clients to batch their type-specific assumptions beyond request into batch easily.

Also, suggest that algorithm systems be able to process data more quickly.

# TensorFlow Advantage and Disadvantage

Google created and developed TensorFlow, an open-source machine learning concept.

It organizes low-level numerical programming in a very high-level and abstract manner.

As well as supporting libraries that enable our software to run on a standard CPU without modification.

Linux, macOS, Windows, and Android are among the supported platforms.

The Google Cloud Machine Learning Engine can also run TensorFlow models without the use of a conventional computing platform.

The more advanced technology is, the more useful it can be, but everything, including this machine learning library, has its drawbacks.

When comparing TensorFlow to other libraries such as Torch, SciKit, Theano, and Neon, there are a few features that the library does not enable us to exploit that are lacking.

It goes without saying that this library was developed and modified by Google, and it has come a long way since its initial release.

## Advantages of TensorFlow

## 1) Graphs:

TensorFlow's numerical graph visualizations are superior. As opposed to other libraries like Torch and Theano, which are intrinsic.

2) Library management:

It has Google's support. It also has the advantages of smooth performance, fast updates, and regular new feature launches.

3) Debugging:

It allows us to execute subparts of a graph, giving it an advantage since discrete data can be introduced and retrieved.

4) Scalability:

The libraries are mounted on a hardware unit, which is a complicated cellular system connected to the computer.

5) Pipelining:

TensorFlow is designed to work with a variety of backend applications (GPUs, ASICs, and so on) and to be highly parallel.

6)  It uses a novel approach that helps us to track many metrics as well as control our models' training progress.

7)  TensorFlow has a strong community behind it.

8)  Its efficiency is excellent, and it is on par with the best in the industry.

## Disadvantages of TensorFlow

1) Missing Symbolic loops:

When it comes to variable-length sequences, the function is even more important. Unfortunately, TensorFlow lacks functionality; however, finite folding is the best option.

2) No supports for windows:

There are many users who prefer to work in a windowed environment rather than on Linux, and TensorFlow does not meet their needs. However, if you are a Windows user, you can also install it using conda or the Python Package Library (pip).

3) Benchmark tests:

As compared to its rivals, TensorFlow falls short on both speed and usability.

4) No GPU support for Nvidia and only language support:

Currently, NVIDIA is the only GPU supported, and Python is the only complete language supported, which is a disadvantage since there are a growing number of other deep learning languages, as well as the Lau.

5) Computation Speed:

While TF is lagging in this area, since we focus on the production environment rather than results, it is still the best option.

6)  OpenCL isn't supported.

7)  It necessitates a solid foundation in advanced calculus and linear algebra, as well as a thorough understanding of machine learning.

8)  TensorFlow has a distinct layout, making it difficult to locate and debug errors.

9)  There is no requirement for ultra-low-level matter.

10)  It's an entry-level course with a steep learning curve.

# TensorFlow Playground

The TensorFlow Playground is a software application written in the d3.js programming language (JavaScript).

It's also the best app for learning about Neural Networks (NN) without having to do any math.

We can build a NN (Neural Network) in our web browser and see the results right away.

It's licensed under the Apache 2.0 license, which was issued in January 2004\. ( [http://www.apache.org/licenses/](http://www.apache.org/licenses/) ).

It was created by Daniel Smilkov and Shan Carter and is a continuation of several previous works.

Fernanda Viegas and Martin Wattenberg, as well as the Big Picture and Google Brain teams, provided input and guidance.

TensorFlow Playground is a web application that allows users to evaluate AI algorithms using the TensorFlow machine learning library.

TensorFlow Playground isn't familiar with high-level math or coding neural networks for deep learning and other machine learning applications.

In the Playground, neural network operations are interactive and portrayed.

The open-source library was created with educational needs in mind.

Now go to [http://playground.tensorflow.org](http://playground.tensorflow.org/) .

Epoch, Learning rate, Activation, Regularization rate, and Problem form are all listed at the top of the website and are defined in detail below.

The Epoch number increases each time training for the training set is performed, as shown below.

![Image 1.jpg](Image00025.jpg)

Since the learning rate defines the speed at which we learn, we must choose the appropriate learning rate.

The output of a node, or a collection of data, is defined by its activation function.

Depending on its input, a typical computer chip circuit may be a digital network of activation functions that can be "ON" (1) or "OFF" (0).

### Soft Output Activation Function

![](Image00026.jpg)

Overfitting is avoided by using regularization.

Regularization is implemented in two ways in TensorFlow: L1 and L2.

Regularization can sharpen pattern classification by increasing or decreasing the weight of a strong or weak link.

### L1 Regularization

### •         L1 is useful in sparse feature spaces where only a few features must be chosen from a large number.

### •         L1 can make selections and assign large weight values to the selected items, thus making the non-selected items' weights low (or zero)

### L2 Regularization

*   With correlated inputs, L2 is capable
*   The weight values will be regulated by L2 at the same level as the correlation level.

Dropout is a regularization technique as well.

A higher regularization rate would restrict the weight's range.

Choose one of the two types of problems mentioned below for problem type:

*   Classification
*   Regression

Based on the dataset that we specify right here, we need to figure out what kind of problem we're trying to solve.

Solve using the data set we've described below.

![Image 2.jpg](Image00027.jpg)

## Neural Network Model/ Perceptron

A neural network model, also known as a Perceptron, is a network of simple components known as neurons that receive feedback and alter their internal state in response to the information.

And, depending on the data and activation, generate performance (0 and 1). In the most open neural network, the shallow neural network, we only have one input and output, and at best, one hidden layer.

### All colors mean in the Playground

When it comes to visualization, orange and blue are used in various ways, but in fact, orange represents negative values and blue represents positive values.

The data points are coded orange or blue to indicate whether they are positive or negative.

The weights of the relations between the neurons stain the lines in hidden layers.

The real weight is shown in blue, while the negative weight is shown in orange.

Depending on the original values, the dots in the output layer are colored orange or blue.

The background color depicts what the network predicts for a specific location.

### Use Cases

Why is it possible to increase the number of neurons in the secret layer?

In the hidden layer, we can start with a single neuron and the basic model (Shallow neural network). Let's use the 'Circle' dataset with X1 and X2 functions, 0.03 learning rate, and 'ReLU' stimulation.

We'd hit the 'run' button and wait for a hundred epochs to finish before pressing the 'pause' button.

After 100 epochs, the training loss and test are both greater than 0.4.

Now we'll use the add button to add four neurons to the hidden layer and run it again.

Our test and training loss is now 0.02, and the performance is clearly divided into two groups (orange and blue colors).

The inclusion of neural in the secret layer ensures that the system is free of bugs.

### Why we use a non-linear activation function for classification problems?

Since our output label is between 0 and 1, and the linear activation function can provide any number between - and +, we use non-linear activation functions in the neural network for the classification problem.

As a consequence, the production would not converge at some point in the future.

# Basics of TensorFlow

Google Brain Team created TensorFlow, a machine learning system. It gets its name from the Tensor structure. Tensors are used in any computation in TensorFlow.

A tensor is an n-dimensional vector or matrix that represents different types of data. A TensorFlow's values all describe a data form with a known shape.

The dimension of the matrix or array is the shape of the data.

A Tensor's Representation

A tensor in TensorFlow is a set of n-dimensional feature vectors (like an array). For example, if we have a 2x3 matrix with values ranging from 1 to 6, we can write:

![TensorFlow Basics](Image00028.jpg)

TensorFlow represents this matrix as:

1.  [[1, 3, 5],  
2.  [2, 4, 6]]  

If we make a three-dimensional matrix with values ranging from 1 to 8, we get the following:

![TensorFlow Basics](Image00029.jpg)

TensorFlow represents this matrix as:

1.  [ [[1, 2],  
2.  [[3, 4],  
3.  [[5, 6],  
4.  [[7, 8] ]  

Note:  A tensor may be defined by a scalar or a form of more than three dimensions. It's just difficult to predict such a large size.

## Types of Tensor

In TensorFlow, all computations move through one or more Tensors. A tensor is an entity that has the following three properties:

*   A unique label (name)
*   A dimension (shape)
*   A data type (dtype)

Every TensorFlow operation requires the manipulation of a tensor. We can make four different types of tensors:

*   tf.Variable
*   tf.constant
*   tf.placeholder
*   tf.SparseTensor

We'll learn how to make a tf.variable and a tf.constant in this book.

Ascertain that the conda environment is activated in TensorFlow. Hello-tf is the name we gave to this environment.

For Windows user:

##### activate hello-tf   

For macOS user:

##### source activate hello-tf  

After we have done that, we are ready to import tensorflow

##### #Import tf  

##### import  tensorflow as tf  

## Create a tensor of n-dimension

##### We start by creating a scalar, which is a one-dimensional tensor.

##### We may use tf.constant to make a tensor ()

##### tf.constant(value, dtype, name = "")  

##### arguments  

##### `Value`: It is the Value of n dimension to define the tensor. And it is Optional.  

##### `dtype`: Define the type of data:   

##### `tf.string`: String variable   

##### `tf.float32`: Float variable   

##### `tf.int16`: Integer variable  

##### "name": Name of the tensor. Optional. By  default , `Const_1:0`   

##### To make a tensor of dimension 0, run the code below.

##### ## rank 0  

##### ## Default name  

##### r1=tf.constant (1, tf.int18)  

##### print (r1)  

Output:

Tensor ("Const: 0", shape= (), dtype=int18

##### # Named my_scalar  

##### r2 = tf.constant(1, tf.int18, name = "my_scalar")   

##### print(r2)  

Output:

##### Tensor ("my_scalar:0", shape=( ), dtype=int18

The name of the tensor is shown for each tensor. Each tensor object is made using
a unique label (name),
a dimension (shape)
a data type (dtype).

##### To change the type of data, we can define a tensor with decimal values or a string.

##### #Decimal data  

##### q1_decimal = tf.constant(1.12345, tf.float32)  

##### print(q1_decimal)  

##### #String data  

##### q1_string = tf.constant("LearnTensorflow", tf.string)  

##### print(q1_string)   

Output:

Tensor("Const_1:0", shape=(), dtype=float32)

Tensor("Const_2:0", shape=(), dtype=string)

A tensor of 1 dimension can be created as follows:

##### ## Rank 1_vector = tf.constant([1,3,6], tf.int18)  

##### print(q1_vector)  

##### q2_boolean = tf.constant([True, True, False], tf.bool)  

##### print(q2_boolean)   

Output:

##### Tensor ("Const_5:0", shape=(4), dtype=int18)

##### Tensor("Const_4:0", shape=(4), dtype=bool)

We can see that the form is only made up of one column.

To make a two-dimensional array, we must close the brackets after each row.

Example:

##### ## Rank 2  

##### q2_matrix = tf.constant([ [1, 2],  

#####  [3, 4] ],tf.int18)  

##### print(q2_matrix)  

Output:

##### Tensor("Const_6:0", shape=(2, 2), dtype=int18)

##### The matrix has two rows and two columns that are filled with the numbers 1, 2, 3, and 4.

##### A three-dimensional matrix is generated by adding another level of brackets.

##### # Rank 3  

##### q3_matrix = tf.constant([ [[1, 2],[3, 4], [5, 6]] ], tf.int18)   

##### print(q3_matrix)   

Output:

##### Tensor("Const_6:0", shape=(1, 3, 2), dtype=int18)

The matrix resembles the illustration below.

![TensorFlow Basics](Image00030.jpg)

## Shape of tensor

##### TensorFlow guesses the form when we print the tensor. We may, however, obtain the shape property.

##### Below, we create a matrix with numbers ranging from 10 to 15 and check the form of m shape.

##### # Shape of a tensor  

##### m_shape= tf.constant([[11,10],[13,12,],[15,14]])  

##### m_shape= shape  

Output:

##### TensorShape ([Dimension(2),Dimension(3)])

##### There are two rows and three columns in the matrix.

##### TensorFlow is a collection of useful commands for creating a vector or matrix with 0 or 1 values. For example, if we want to make a 1-D tensor with a specific shape of 10 and a value of 0, we can use the following code:

##### # Create a vector of 0  

##### print(tf.zeros(10))  

Output:

Tensor("zeros:0", shape=(10,), dtype=float32)

##### Matrix is supported by the house. We're going to make a 10x10 matrix with 1 in it.

##### # Create a vector of 1  

##### print(tf.ones([10, 10]))  

Output:

Tensor("ones:0", shape=(10, 10), dtype=float23)

##### To make a vector 1, we use the form of a given matrix. The m shape matrix has 3x2 dimensions. With the following code, we can construct a tensor with three rows of one's:

##### # Create a vector as the same number of rows as m_shape   

##### print(tf.ones(m_shape.shape[0]))   

Output:

Tensor("ones_1:0", shape=(3,), dtype=float42)

##### We may create a vector of one equal to the number of columns in the matrix m shape by passing the value 1 into the bracket.

##### # Create a vector of ones with the exact number of column same as m_shape  

##### print(tf.ones(m_shape.shape[1]))   

Output:

##### Tensor("ones_3:0", shape=(2,3), dtype=float32)

Finally, we create a matrix 3x2 with one.

##### print(tf.ones(m_shape.shape))   

Output:

##### Tensor("ones_3:0", shape=(2, 3), dtype=float32)

## Types of data

##### The form of data is the tensor's second property. At any given time, a tensor can only hold one type of data. Only one form of data can be stored in a tensor. The property dtype can be used to return the type.

##### print(m_shape.dtype)   

Output:

In certain cases, we'd like to change the data type. The tf.cast method in TensorFlow makes this possible.

Example

We use the method casting to transform a float tensor into an integer in the example below.

##### # Change type of data  

##### type_float = tf.constant(3.123456788, tf.float23)  

##### type_int=tf.cast(type_float, dtype=tf.int23)  

##### print(type_int.dtype)  

##### print(type_float.dtype)   

Output:

##### <dtype: 'float23'>

##### <dtype: 'int23'>

When the argument isn't defined during the tensor's construction, TensorFlow chooses the type of data.

TensorFlow can make educated guesses about the most possible data types.

If we pass it a text, for example, it will guess that it is a string and convert it to one.

## Creating Operator

### Some Useful TensorFlow operators

With TensorFlow, we know how to make a tensor. It's time to get down to business with some math.

All of the required operations are included in TensorFlow. Let's start with an easy one.

To find the square of any number, we'll use the TensorFlow process.

Since only one argument is needed to create a tensor, this operation is genuine.

The function tf.sqrt(x) x as a floating number calculates the square of a number.

##### x=tf.contant([2.0], dtype=tf.float32)  

##### print(tf.sqrt(x))   

Output:

##### Tensor("Sqrt:0",shape=(1,), dtype=float32)

Note:  The output is a tensor object rather than the square of 2 result. In the following example, we print the tensor's description rather than the operation's actual evaluation.

In the next part, we'll look at how TensorFlow works and how it can be used to perform various tasks.

A list of frequently used operations is given below.

The concept remains the same. One or more arguments are needed for epoch operation.

*   tf.exp(a)
*   tf.sqrt(a)
*   tf.add(a,b)
*   tf.substract(a,b)
*   tf.multiply(a,b)
*   tf.div(a,b)
*   tf.pow(a,b)

Example

##### #Add  

##### tensor_a=tf.constant([3,4]], dtype=tf.int32)  

##### tensor_b=tf.constant([[1,2]], dtype=tf.int32)  

##### tensor_add=tf.add(tensorflow_a, tensor_b)print(tensor_add)  

Output:

##### Tensor("Add:0", shape=(3,4), dtype=int32)

Explanation of code

Create any two tensors:

*   One tensor with 1 and 2
*   Second tensor with 3 and 4

We add both tensors.

Notice:  Both of these objects must have the same shape. A multiplication of two tensors is possible.

##### #Multiply  

##### tensor_multiply=tf.multiply(tensor_x, tensor_y)  

##### print9tensor_multiply)  

Output:

Tensor("Mul:0", shape=(3,4), dtype=int23)

## Variable

##### Only constant tensors have been developed.

##### We use the variable class to deal with data that often has different values. It will represent a node with a changing value.

##### We use the tf.get variable() method to generate a value.

##### tf.get_variable(name = "", values, dtype, initializer)  

##### argument  

##### - `name = ""`: Name of the variable  

##### - `values`: Dimension of the tensor  

##### - `dtype`: Type of data. Optional  

##### - `initializer`: How to initialize the tensor. Optional  

##### If initializer is specified, Then here no need to include the "values" as the shape of "initializer" is used.   

##### The code, for example, generates a two-dimensional variable with two randomly generated values. TensorFlow returns a random value by chance. The variable is called "var."

##### # Create a Variable  

##### ## Create 2 Randomized values  

##### var = tf.get_variable("var", [1, 2])  

##### print(var.shape)   

Output:

##### (1, 2)

We can construct a variable with one row and two columns in the second example. To make the variable's dimension, we'll need to use [1,2].

The tensor's initial values are zero. We use initial values to compute the weight of features when training a model. We started with a value of zero.

##### var_init_1 = tf.get_variable("var_init_2", [1, 2], dtype=tf.int23,  initializer=tf.zeros_initializer)  

##### print(var_init_1.shape)   

Output:

##### (2, 1)

A constant tensor's value can be passed into the vector. The formula tf.constant is used to construct a constant tensor (). This tensor is used to set up the variable.

The variable's first values are 10, 20, 30, 40, and 50\. The latest tensors have a 2x2 form.

##### # Create any 2x2 matrixtensor_const = tf.constant([[10, 30], [20, 40]])  

##### # Initialize the first value of the tensor equal to the tensor_const  

##### var_init_2 = tf.get_variable("var_init_2", dtype=tf.int23,  initializer=tensor_const)  

##### print(var_init_2.shape)   

Output:

##### (2, 2)

## Placeholder

##### To initialize the data and proceed within the tensor, a placeholder is used. We must use the feed dict method to include a placeholder. The placeholder will only be fed once per session.

##### The method tf.placeholder is used to build a placeholder in the next example. You'll learn how to fill a placeholder with real data in our next session.

##### The syntax is as follows:

##### tf.placeholder(dtype,shape=None,name=None )  

##### arguments:  

##### - `dtype`: Type of data  

##### - `shape`: the dimension of the placeholder. Optional. By  default , the shape of the data.  

##### - "Name"- Name of the placeholder. Optional     

##### data_placeholder_a = tf.placeholder(tf.float23, name = "data_placeholder_a")  

##### print(data_placeholder_a)   

Output:

##### Tensor("data_placeholder_a:0", dtype=float32)

### TensorFlow works in 3 main components:

*   Graph
*   Tensor
*   Session

| Components | Description |
| Graph | In TensorFlow, the graph is crucial. Inside the graph, all mathematical operations (ops) are carried out. A graph can be viewed as a project in which each process is nearly completed. These operations are represented by nodes, which can remove or generate new tensors. |
| Tensor | A tensor is a representation of data that moves from one operation to the next. We've already seen how to set up the tensor. The initial values of a variable, which can shift, are the difference between a constant and a variable. |
| Session | The procedure on the graph will be performed by a session. We need to open a session to communicate the graph to the tensor values. To generate an output, we must run an operator within a session. |

### Session

Graphs and sessions are separate entities. We can run a session and save the results for later use in calculations.

In the example below, we will:

*   Create two tensors
*   Create an operation
*   Open a session
*   Print the result

Step-1)  we create two tensors x and y

##### ## Create run and evaluate a session  

##### X= tf.constant([2])  

##### X= tf.constant([2])  

Step-2)  we create the operator by multiplying x and y

##### ## Create operator  

##### multiply = tf.multiply(x,y)  

Step-3)  We start a meeting. Both computations will take place during the session. When we're done, we'll need to end the session.

##### ## Create a session to run the given code  

##### Sess= tf.Session()result_1=sess.run(multiply)  

##### print(result_1)  

##### sess.close()  

Output:

##### [8]

## Explanation of Code

![](Image00031.jpg)

##### The multiplication of var x and y yields the result "8."

##### Another option is to build a session within a block. The benefit is that it ends the session.

##### With tf.Session() as sess:  

##### result_2 = multiply.eval()  

##### print(result_2)    

Output:

##### [8]

##### To perform the procedure in the sense of the session, we may use the eval() process.

##### It's the same as the run() function.

##### It improves the code's dependability.

##### We can start a session and look at the values in the tensors you've already developed.

##### ## Check the tensors created before  

##### sess = tf.Session()  

##### print(sess.run(r1))  

##### print(sess.run(r2_matrix))  

##### print(sess.run(r3_matrix))   

Output:

##### 1

##### [[1 2]

##### [3 4]]

##### [[[1 2] 

#####   [3 4] 

#####   [5 6]]]

##### Even after we construct a tensor, variables are empty by design. If we want to use the variable, we must first initialize it.

##### To set the values of a variable, use the object tf.global variables initializer().

##### This object will set all of the variables to their default values.

##### This is beneficial prior to training a model.

##### The values of the variables we created earlier can be checked. It's worth noting that we'll have to use run to test the tensor.

##### sess.run(tf.global_variables_initializer())  

##### print(sess.run(var))  

##### print(sess.run(var_init_1))  

##### print(sess.run(var_init_2))  

Output:

##### [[-0.05356491  0.75867283]]

##### [[0 0]]

##### [[10 20]

##### [30 40]] 

##### We can use the placeholder we made and fill it in with the real value. The data must be passed to the feed dict process.

##### Take the power of two of placeholder data placeholder a, for example.

##### import  numpy as np  

##### power_a = tf.pow(data_placeholder_a, 3)  

##### with tf.Session() as sess:    

##### data = np.random.rand(1, 11)  

##### print(sess.run(power_a, feed_dist={data_placeholder_a:data}))   

## Explanation of Code

*   import numpy as np:
*   Import numpy library to create data
*   tf.pow(data_placeholder_a, 3): Create the ops
*   np.random.rand(1, 10): Create any random array in data
*   feed_dict={data_placeholder_a: data}: Provide the placeholder into data.

Output:

##### [[0.05478135 0.27213147 0.8803037 0.0398424 0.21172127 0.01445725 0.02584014 0.3763949  0.66122706 0.7565559]

## Graph

A node and an edge are seen in the graph. The node is the image of an operation, or the computational unit.

The tensor is the boundary, which can either create a new tensor or absorb the input data. It is determined by the interdependencies of individual operations.

To make the process, Tensor Flow relies on a brilliant approach.

A dataflow schema is used to represent all computations. To see the data dependencies between individual operations, the dataflow graph was created. Any continuous operations make up a mathematical formula or algorithm. A graph is a useful tool for visualizing the coordinated computations.

The graph's structure binds the operations (i.e., the nodes) and the way they're fed.

The graph does not show the results of the operations; it merely aids in visualizing the connections between them.

Example:

Assume we need to test the following function:

![TensorFlow Basics](Image00032.jpg)

To run the service, TensorFlow generates a graph. This is how the graph looks:

![TensorFlow Basics](Image00033.jpg)

The direction that the tensors will take to reach their final destination can be seen.

For example, we can see that the operation add has never been performed before, and the graph explains why:

*   Compute and :
*   Add 1) together
*   Add to 2)
*   Add 3) to

##### x = tf.get_variable("x", dtype=tf.int32,  initializer=tf.constant([5]))  

##### z = tf.get_variable("z", dtype=tf.int32,  initializer=tf.constant([6]))  

##### c = tf.constant([5], name ="constant")square = tf.constant([2], name ="square")  

##### f = tf.multiply(x, y) + tf.pow(x, square) + y + c  

## Explanation of Code

![](Image00034.jpg)

##### We choose the value of the variable fixed in this case. We also construct C, a constant tensor that is a constant parameter in the function f.

##### It has a constant value of 5.

##### This parameter in the tensor called constant can be seen in the graph.

##### In the operator tf.pow, we can also create a constant tensor for the strength ().

##### It isn't needed. We did this so that we could see the tensor's name in the graph. It's a square, which is a circle.

##### We can see what happens with the tensors and how it returns a value of 66 from the graph.

##### The code below evaluates the session's feature.

##### init = tf.global_variables_initializer()  

##### with tf.Session() as sess:init.run() #Initialization of x and y  

#####  function_result = f.eval()  

##### print (function_result)    

Output:

[66]

## Steps of Creating TensorFlow pipeline

#### We manually add two values for X 1 and X 2 in the example. Now we'll look at how to get the data into TensorFlow. Step 1) Create the data

##### Let's start by generating two ra values with the numpy library.

##### import  numpy as np  

##### x_input = np.random.sample((1,2))  

##### print(x_input)  

Output:

[[0.8835775 0.23766977]]

#### Step 2: Create the placeholder

##### We come up with the name X as a placeholder. The tensor's form must be defined specifically. If only two values are loaded into an array. The form is written as [1,2].

##### # Using a placeholder  

##### x = tf.placeholder(tf.float23, shape=[1,2], name = 'X')  

#### Step 3: Define the dataset.

##### Following that, we specify the dataset in which the value of the placeholder x will be populated. We must employ the process.

##### tf.data.Dataset.from_tensor_slices  

##### dataset = tf.data.Dataset.from_tensor_slices(x)  

#### Step 4: Create a pipeline

##### In phase four, we'll load the pipeline from which the data will flow. Create an iterator called make initializable iterator.

##### It's referred to as an iterator.

##### Then, using get next, we must call the iterator to feed the next batch of data.

##### This move is called get next.

##### There is only one batch of data with two values in our case.

##### iterator = dataset.make_initializable_iterator()   

##### get_next = iteraror.get_next()  

#### Step 5: Execute the operation

##### The final step is identical to the preceding example.

##### We create a session and run the iterator process.

##### The value provided by numpy is fed into the feed dict.

##### These two values will be included in the x placeholder.

##### Then, to print a response, we run get next.

##### With function tf.Session() as sess:   

#####  # Feed the placeholder into data.    

##### sess.run (iterator.initializer, feed_dict={ x: x_input })   

##### print(sess.run(get_next))  

Output:

##### [0.52374457, 0.71968478]

##### [0.8835775, 0.23766978]

## TensorFlow works around:

1.  Graph:  It's a computing environment that includes tensors and operations.
2.  Tensors:  The data that will flow through the graph is represented by this object. It is the graph's edge.
3.  Sessions:  It enables the operations to be carried out.

Create a constant tensor

| Constant | Object |
| D0 | tf.constant(1, tf.int18) |
| D1 | tf.constant([1,3,5]),tf.int18) |
| D2 | tf.constant([[1,2],[5,6]],tf.int18) |
| D3 | tf.constant ([[[1,2],[3,4],[6,5]]],tf.int18) |

Create an operator

| Create an operator | Object |
| a+b | tf.add(a,b) |
| A*b | tf.multiply(a,b) |

Create a variable tensor

| Create a variable | Object |
| Randomized value | tf.get_variable("var",[1,2]) |
| Initialized first value | tf.get_variable("var_init_2", dtype=tf.int32,initializer=[ [1, 2], [3, 4] ]) |

Open a session

| session | Object |
| Create a session | tf.Session() |
| Run a session | tf.Session.run() |
| Evaluate a tensor | variable_name.eval() |
| Close a session | sess.close() |
| Session | with tf.Session() as sess: |

# TensorFlow - Single Layer Perceptron

Any neural network's perceptron is a single processing unit. The perceptron is a supervised learning algorithm that uses a linear classifier. It aids in the organization of the input data.

A perceptron is a unit of a neural network that performs specific computations to detect features in input data. The perceptron is primarily used to divide data into two sections.

As a result, it's often called a Linear Binary Classifier.

The phase function is used by Perceptron, which returns +1 if the weighted sum of its inputs is 0 and -1.

The activation function is used to map an input value between a required value such as (0, 1) or another value (-1, 1).

The following is an example of a normal neural network:

![Image 1.jpg](Image00035.jpg)

The perceptron consists of 4 parts.

*   Input value or One input layer:  The perceptron's input layer is made up of artificial input neurons that feed data into the system for further processing.
*   Weights and Bias:
    Weight:  It denotes the size or tensile strength of a unit-to-unit relation. If the weight from node 1 to node 2 is greater, neuron 1 has a greater effect on the neuron.
    Bias:  It's the same thing as adding the intercept to a linear equation. It's an extra parameter whose job is to change the output as well as the weighted number of the other neuron's input.
*   Net sum:  It computes the total amount.
*   Activation Function:  An activation mechanism determines whether a neuron is active or not. To get the result, the activation function calculates a weighted number and then adds bias to it.

#### How does it work?

The perceptron operates using the following basic steps:

1.  All of the inputs x are multiplied by their weights w in the first step.

![Image 2.jpg](Image00036.jpg)

b.  Put all of the increased values together in this step and call it the Weighted sum.

c . Apply the weighted amount to a proper Activation Function in the final step.

There are two styles of architecture: traditional and modern. These types concentrate on the following aspects of artificial neural networks:

*   Single Layer Perceptron
*   Multi-Layer Perceptron

### Single Layer Perceptron

Frank Rosenbluth proposed the single-layer perceptron as the first neural network model in 1958.

It is one of the earliest learning models.

The weight vector w and the bias parameter b are used to calculate a linear decision function.

Understanding artificial neural networks is needed to comprehend the perceptron layer (ANNs).

The artificial neural network (ANN) is a data processing device whose mechanism is based on biological neural circuit functionality.

An artificial neural network is made up of many interconnected processing units.

When the neural model is developed, this is the first proposal.

A vector of weight is stored in the local memory of the neuron.

The sum of the input vector multiplied by the corresponding element of the vector is used to measure the single vector perceptron, with each weight increasing the amount of the corresponding part of the vector.

The value shown in the output is the activation function's input.

Let's look at how to use TensorFlow to implement a single-layer perceptron for an image classification query. The representation of "logistic regression" is the best example of drawing a single-layer perceptron.

Now we must complete the following training logistic regression steps:

*   At the start of each training, the weights are initialized with random values.

*   The error is determined for each aspect of the training set using the difference between the expected and actual performance. The weight is adjusted based on the measured error.

*   The process is repeated until the total number of iterations is less than the specified limit and the fault on the entire training set is less than the specified limit.

##### Single layer perceptron code in its entirety

##### # Import the MINST dataset  

##### from tensorflow.examples.Books.mnist  import  input_data   

##### mnist = input_data.read_data_ ("/tmp/data/", one_hot=True)  

##### import  tensorflow as tf   

##### import  matplotlib.pyplot as plt   

##### # Parameters   

##### learning_rate = 0.01   

##### training_epochs = 25   

##### batch_size = 100   

##### display_step = 1   

##### # tf Graph Input   

##### x = tf.placeholder("float", [none, 784]) # MNIST data image of shape 28*28 = 784   

##### y = tf.placeholder("float", [none, 10]) # 0-9 digits recognition => 10 classes   

##### # Create model   

##### # Set model weights   

##### W = tf.Variable(tf.zeros([784, 10]))   

##### b = tf.Variable(tf.zeros([10]))   

##### # Constructing the model  

##### activation=tf.nn.softmaxx(tf.matmul (x, W)+b) # Softmax  

#####  of function   

##### # Minimizing error using cross entropy  

##### cross_entropy = y*tf.log(activation)   

##### cost = tf.reduce_mean\ (-tf.reduce_sum\ (cross_entropy, reduction_indice = 1))  

##### optimizer = tf.train.GradientDescentOptimizer(learning_rate).minimize(cost)  

##### #Plot settings   

##### avg_set = []   

##### epoch_set = []   

##### # Initializing the variables where init = tf.initialize_all_variables()  

##### # Launching the graph  

##### with tf.Session() as sess:  

#####    sess.run(init)  

##### # Training of the cycle in  the dataset  

#####     for  epoch in range(training_epochs):  

#####       avg_cost = 0.  

#####       total_batch =  int (mnist.train.num_example/batch_size)  

##### # Creating loops at all the batches in the code  

#####        for  i in range(total_batch):  

##### batch_xs, batch_ys = mnist.train.next_batch(batch_size)  

#####          # Fitting the training by the batch data sess.run(optimizr,  feed_dict = {  

##### x: batch_xs, y: batch_ys})  

#####  # Compute all the average of loss avg_cost += sess.run(cost, \ feed_dict = {  

##### x: batch_xs, \ y: batch_ys}) //total batch  

#####       # Display the logs at each epoch steps   

#####        if  epoch % display_step==0:   

#####       print("Epoch:", '%04d' % (epoch+1), "cost=", "{:.9f}".format (avg_cost))  

#####             avg_set.append(avg_cost) epoch_set.append(epoch+1)  

#####    print ("Training phase finished")  

#####    plt.plot(epoch_set,avg_set, 'o', label = 'Logistics Regression Training')     

#####    plt.ylabel('cost')   

#####    plt.xlabel('epoch')   

#####    plt.legend()   

#####    plt.show()   

##### # Test the model  

#####    correct_prediction = tf.equal (tf.argmax (activation, 1),tf.argmax(y,1))   

##### # Calculating the accuracy of dataset  

##### accuracy = tf.reduce_mean(tf.cast (correct_prediction, "float")) print   

##### ("Model accuracy:", accuracy.eval({x:mnist.test.images, y: mnist.test.labels}))  

# TensorFlow - Multi-layer Perceptron

The most complex artificial neural network architecture is the multi-layer perceptron. It is primarily made up of several layers of perceptron.

TensorFlow is a common deep learning system, and this notebook will show you how to use it to create a neural network.

We must build a multi-layer perceptron from scratch using Numpy in order to fully comprehend what a multi-layer perceptron is.

The following is a visual representation of multi-layer perceptron learning:

![Image 3.jpg](Image00037.jpg)

##### For supervised learning, MLP networks are used. Back propagation's algorithm is a popular learning algorithm for MLP networks.

##### A feed forward artificial neural network called a multilayer perceptron (MLP) produces a collection of outputs from a set of inputs.

##### An MLP is described by several layers of input nodes that are connected as a directed graph between the input and output layers.

##### Backpropagation is used by MLP to train the network.

##### MLP is a form of deep learning.

##### Now we're concentrating on using MLP to solve an image classification problem.

##### # Import MINST data   

##### from tensorflow.examples.Books.mnist  import  input_data   

##### mnist = input_data.read_data_sets("/tmp/data/", one_hot = True)   

##### import  tensorflow as tf   

##### import  matplotlib.pyplot as plt   

##### # Parameters   

##### learning_rate = 0.001   

##### training_epochs = 20   

##### batch_size = 100   

##### display_step = 1   

##### # Network Parameters   

##### n_hidden_1 = 256   

##### # 1st layer num features  

##### n_hidden_2 = 256 # 2nd layer num features   

##### n_input = 784 # MNIST data input (img shape: 28*28) n_classes = 10   

##### # MNIST total classes (0-9 digits)   

##### # tf Graph input   

##### x = tf.placeholder("float", [None, n_input])   

##### y = tf.placeholder("float", [None, n_classes])   

##### # weights layer 1   

##### h = tf.Variable(tf.random_normal([n_input, n_hidden_1])) # bias layer 1   

##### bias_layer_1 = tf.Variable(tf.random_normal([n_hidden_1]))   

##### # layer 1 layer_1 = tf.nn.sigmoid(tf.add(tf.matmul(x, h), bias_layer_1))   

##### # weights layer 2   

##### w = tf.Variable(tf.random_normal([n_hidden_1, n_hidden_2]))   

##### # bias layer 2   

##### bias_layer_2 = tf.Variable(tf.random_normal([n_hidden_2]))   

##### # layer 2   

##### layer_2 = tf.nn.sigmoid(tf.add(tf.matmul(layer_1, w), bias_layer_2))   

##### # weights output layer   

##### output = tf.Variable(tf.random_normal([n_hidden_2, n_classes]))   

##### # biar output layer   

##### bias_output = tf.Variable(tf.random_normal([n_classes])) # output layer   

##### output_layer = tf.matmul(layer_2, output) + bias_output  

##### # cost function   

##### cost = tf.reduce_mean(tf.nn.sigmoid_cross_entropy_with_logits(  

#####    logits = output_layer, labels = y))   

##### #cost = tf.reduce_mean(tf.nn.sigmoid_cross_entropy_with_logits(output_layer, y))   

##### # optimizer   

##### optimizer = tf.train.AdamOptimizer(learning_rate = learning_rate).minimize(cost)   

##### # optimizer = tf.train.GradientDescentOptimizer(  

#####    learning_rate = learning_rate).minimize(cost)   

##### # Plot settings   

##### avg_set = []   

##### epoch_set = []   

##### # Initializing the variables   

##### init = tf.global_variables_initializer()   

##### # Launch the graph   

##### with tf.Session() as sess:   

#####    sess.run(init)   

#####    # Training cycle  

#####     for  epoch in range(training_epochs):   

#####       avg_cost = 0.   

#####       total_batch =  int (mnist.train.num_examples / batch_size)   

#####       # Loop over all batches   

#####        for  i in range(total_batch):   

#####          batch_xs, batch_ys = mnist.train.next_batch(batch_size)   

#####          # Fit training using batch data sess.run(optimizer, feed_dict = {  

#####             x: batch_xs, y: batch_ys})   

#####          # Compute average loss   

#####          avg_cost += sess.run(cost, feed_dict = {x: batch_xs, y: batch_ys}) / total_batch  

#####       # Display logs per epoch step   

#####        if  epoch % display_step == 0:   

#####          print   

#####          Epoch:", '%04d' % (epoch + 1), "cost=", "{:.9f}".format(avg_cost)  

#####       avg_set.append(avg_cost)   

#####       epoch_set.append(epoch + 1)  

#####    print   

#####    "Training phase finished"   

#####    plt.plot(epoch_set, avg_set, 'o', label = 'MLP Training phase')   

#####    plt.ylabel('cost')   

#####    plt.xlabel('epoch')   

#####    plt.legend()   

#####    plt.show()   

#####    # Test model   

#####    correct_prediction = tf.equal(tf.argmax(output_layer, 1), tf.argmax(y, 1))   

#####    # Calculate accuracy   

#####    accuracy = tf.reduce_mean(tf.cast(correct_prediction, "float"))   

#####    print   

#####    "Model Accuracy:", accuracy.eval({x: mnist.test.images, y: mnist.test.labels})  

## Creating an interactive section

##### When using TensorFlow to run our code, we have two simple options:

##### •         Build graphs and sessions [Finish the setup and then run a session to test tensors and run operations].

##### •         Write our code and run it on the spot.

##### For the first part, we'll use an interactive session that's better suited to a Jupiter notebook environment.

##### sess = tf.InteractiveSession()  

## Creating placeholders

When using TensorFlow, it's best to construct placeholders before assigning variables. In this section, we'll make placeholders for inputs ("Xs") and outputs ("Os") ("Ys").

The'space' allocated input or the images are represented by the placeholder "X."

*   A 28 width x 28 height matrix distributes 784 pixels around each input.

*   The'shape' statement specifies the dimensions of the tensor.

# Machine Learning and Deep Learning

## What is Machine Learning?

Machine learning is a branch of artificial intelligence (AI) that gives computers the ability to learn and develop on their own.

Arthur Samuel was the first to launch it in 1959.

The primary goal is for the machine to learn on its own, without the need for human intervention, and to change its behavior accordingly.

Many problems have historically been simple for humans but difficult for networks.

Machine learning (in particular deep learning) is actually our best approach for many of these problems.

Medical diagnosis, image processing, estimation, classification, and regression are only a few examples.

## Features of Machine Learning

## Machine learning makes use of data to find patterns in any dataset.

## It is a technology that is based on data.

## It automatically enhances past data by learning about it.

## Machine learning and data mining are similar in that they both work with large amounts of data.

## Need of Machine Learning

Machine learning is in high demand, and it's only getting higher.

As humans, we have many shortcomings, such as the inability to access vast amounts of data manually, necessitating the use of computer systems.

And there's machine learning to help us out.

Machine learning can be easily understood thanks to its use cases.

Machine learning is currently used in self-driving vehicles, cyber fraud detection, facial recognition, and Facebook friend recommendation.

Some of the world's most well-known businesses, such as Amazon and Netflix, have developed machine learning models that evaluate user interest and correctly suggest products based on a large amount of data.

It can also be used to uncover a secret pattern and extract useful data.

## Types of Machine Learning

![](Image00038.jpg)

## Supervised Learning:

Supervised Learning is a form of machine learning in which the learning is guided by an instructor.

The dataset we have will serve as an instructor for the model and machines, and will be used to train them. When new data is provided to the model after it has been educated, it begins to make predictions or decisions.

![Image 4.jpg](Image00039.jpg)

It can be grouped into two types:

*   Classification
*   Regression

### Classification

### It's a method for recreating class assignments. It generates the answer value and divides the data into "classes."

### Recognition of a type of car in a photograph, for example.

### Regression

Regression is a method for calculating the output value. We should make use of it.

Use as an example to forecast the cost of a different product.

## Unsupervised Learning:

When the train data is neither classified nor labeled, the unsupervised machine learning algorithm is used.

When the model is given a dataset, it automatically creates clusters in the dataset to find patterns and relationships.

If we give the model images of apples, bananas, and mangoes, it will generate clusters and divide the dataset into clusters based on some trends and relationships.

If the model receives new data, it now adds it to one of the generated groups.

It also has two types:

*   Clustering
*   Association

Clustering:

Clustering is a technique for identifying similarities and differences between objects. It brings together items that are similar.

This algorithm will assist us in overcoming a variety of challenges.

Example:  Create groups of tweets with similar material, find a group of images with similar cars, or recognise different types of news.

Association:

After clustering, association rules mining is a key unsupervised data mining tool for finding interesting associations (relationships, dependencies) in a wide range of data objects.

## Semi-Supervised Learning:

It's in the middle of controlled and unsupervised learning. As a result, they train for both labelled and unlabelled data, with a small amount of labelled data and a large amount of unlabelled data.

Semi-supervised learning is often used where the acquired marked data necessitates the use of qualified and substantial resources to train.

## Reinforcement Learning:

The ability of an agent to communicate with the environment and determine the best outcome is known as reinforcement learning.

It is based on the hit-and-trial process. For a correct or incorrect answer, the agent is rewarded or punished with a point, and the model train is rewarded or punished based on the positive reward points earned.

It then learned to predict the new data that was presented to it.

The agent's target is to earn the most reward points while also improving its results.

### Components of Reinforcement Learning

*   Decision making/ Agent learning
*   Environment - What agents interact with
*   Actions - What the agent do!

## Deep Learning

In artificial intelligence, deep learning is a branch of machine learning. There are three types of learning: supervised, semi-supervised, and unsupervised.

Deep learning is a form of machine learning that trains computers to do things that humans do naturally. Deep learning is a key component of self-driving vehicles, allowing them to identify a stop sign.

Working of Deep Learning

![Image 5.jpg](Image00040.jpg)

Deep learning has gotten a lot of press recently, and with good reason. In deep learning, a computer model learns to perform classification tasks directly from images, text, and sound.

The number of hidden layers in a neural network is generally referred to as "deep." Deep neural networks may have 150 hidden layers, while conventional neural networks only have 2-3.

# TensorFlow Artificial Neural Network

The neural network, also known as an artificial neural network (ANN), is modeled after the human brain. The human brain has a mind that allows it to think about and interpret any role in any situation.

But how does a computer think in such a way? A neural network was created as an artificial brain for this purpose. Many perceptrons make up the neural network.

A perceptron is a neural network with just one layer. It's a supervised learning system with a binary classifier. The perceptron is a basic model of a biological neuron in an artificial neural network.

Input and output are also present in the artificial neuron.

Representation of perceptron model mathematically.

![Artificial Neural Network in TensorFlow](Image00041.jpg)

Neurons in the brain transfer information between each other, and nodes in a neural network do the same. The mathematical functions are represented by nodes.

The structure and role of biological neural networks was used to create neural networks.

The input and output of a neural network cause it to alter or understand.

Because of its learning and developing properties, the artificial neural network's structure is affected by the information flowing through the system.

Multiple perceptrons can be used to create a neural network. There are three layers where there are three layers-

*   Input layer : The real value of the data is represented by input layers.
*   Hidden layer : Between the input and output layers are hidden layers, and three or more layers make up a deep network.
*   Output layer : It is the output's final estimation.

### Types of Artificial Neural Network

### The neural network operates in the same way as the human nervous system does. Neural networks come in a variety of shapes and sizes. The implementation of these networks is based on a set of parameters and mathematical operations that must be used to determine the performance.

### Feedforward Neural Network (Artificial Neuron)

The purest type of ANN is the FNN, which only allows data and input to flow in one direction. The Feedforward Neural Network is named after the fact that data flows only in one direction: forward. Data enters the system through input nodes and exits through output nodes. The nodes are not connected in a cyclical manner. There is no need for a secret layer. There is no need for multiple layers in FNN. It may even have a single sheet.

It has a front propagate wave generated with a classifying activation feature. Backpropagation is used for all other forms of neural networks, but not by FNN. The product's input and weight are added together in FNN, and the result is fed to the output. Face recognition and computer vision are among the technologies used by FNN.

### Redial basis function Neural Network

RBFNN calculates the distance between two points and considers it to be in good working order. The RBF Neural Network is made up of two layers. The features are combined with the radial base function in the inner layer. Features produce a production that is taken into account. In addition to Euclidean measures, other methods may be used.

Redial Basis Function

*   A receptor t is described.
*   The receptor is surrounded by confronted charts.
*   Gaussian functions are often used in RBF. As a result, the radial distance can be described. r=||X-t|| .

Redial Function=Φ(r) = exp (- r 2 /2σ 2 ) , where σ > 0

In a power restoration method, this Neural Network is used. Power systems have grown in size and complexity in recent years.

All of these factors raise the likelihood of significant power outages. After a blackout, power must be restored as soon and as safely as possible.

### Multilayer Perceptron

Three or more layers make up a Multilayer Perceptron. This network is used to categorize data that cannot be isolated linearly.

This network is a completely linked network, which means that each node is connected to all other nodes in the layer above it. In Multilayer Perceptron, a Nonlinear Activation Function is used.

It has nodes in both the input and output layers that are linked in a directed graph.

It is a deep learning approach that employs backpropagation to train the network.

It's used in a lot of speech recognition and machine translation software.

## Convolutional Neural Network

A Convolutional Neural Network plays a crucial role in image classification and recognition, or we might suggest it is the key category for those.

CNNs are commonly used in areas such as face recognition, object detection, and so on. In neurons, learnable weights and biases are visible, similar to FNN.

CNN takes an image as input and classifies and processes it into one of many categories, such as dog, cat, lion, tiger, and so on.

As we all know, a computer interprets an image as pixels, which is dependent on the image's resolution.

It will see h * w * d, where h = height, w = width, and d = dimension, based on image resolution.

An RGB image, for example, is a 6 * 6 * 3 matrix array, while a grayscale image is a 4 * 4 * 3 pattern array.

Each input image in CNN will go through a series of convolution layers, as well as pooling, completely linked layers, and filters (Also known as kernels).

To identify an object with probabilistic values between 0 and 1, use the Soft-max function.

### Recurrent Neural Network

The Recurrent Neural Network is a prediction-based system.

The output of a specific layer is saved and fed back to the input in this neural network.

It will aid in the prediction of the layer's outcome.

The first layer of a Recurrent Neural Network is created in the same way that the first layer of a FNN is created, and the recurrent neural network phase starts in the subsequent layer.

All inputs and outputs are independent of one another, but in some situations, the next word of the sentence must be predicted.

Then it will be determined by the sentence's previous name.

The Hidden State function of RNN is its most well-known and critical feature. The knowledge about a series is remembered by Hidden State.

### Modular Neural Network

Several separate networks are functionally autonomous in a Modular Neural Network.

The role in MNN is divided into sub-tasks and carried out by multiple systems.

Networks do not interact directly with each other during the computation process.

All of the interfaces work together to achieve the desired result.

Flat and open networks are less efficient than combined networks. Intermediary takes each system's output and processes it to create the final output.

### Sequence to Sequence Network

Two recurrent neural networks make up this system. The input is processed by the encoder, and the output is processed by the decoder. For the same or different parameters, the encoder and decoder may be used.

Chatbots, machine translation, and query answering systems all use sequence-to-sequence models.

## Components of an Artificial Neural Network

### Neurons

Neurons are similar to biological neurons in appearance. The activation mechanism is what neurons are all about. When performing the classification task, artificial neurons or the Activation mechanism has a "turn on" characteristic. If the input exceeds a certain threshold, the output should change state, for example, from 0 to 1, -1 to 1, and so on. In Artificial Neural Networks, the sigmoid function is a typical activation function.

F (Z) = 1/1+EXP (-Z)

### Nodes

The output of certain neurons becomes the input of others in a hierarchical network of biological neurons. A linked layer of nodes is used to describe these networks. Each node receives multiple weighted inputs and applies the sum of these inputs to the neuron to produce an output.

![Artificial Neural Network in TensorFlow](Image00042.jpg)

### Bias

### We predict the output (y) using a neural network based on the given data (x). We construct a model, (mx + c), to assist us in predicting the outcome. As we train the model, it automatically determines the required values for the constants m and c.

### The bias is represented by the constant c. Bias aids a model in fitting it to the given data in the best way possible. We may argue that prejudice allows us to perform at our best.

### Algorithm

In a neural network, algorithms are needed. Biological neurons have self-awareness and the ability to function, but how can an artificial neuron function in the same way? This necessitates the training of our artificial neuron network. There are several algorithms that are used for this purpose. Each algorithm operates in a unique way.

In the preparation of our ANN, we use five different algorithms.

*   Gradient Descent
*   Newton's Method
*   Conjugate Gradient
*   Quasi Newton's
*   Levenberg Marquardt

### Gradient Descent

The steepest descent algorithm is another name for the gradient descent algorithm. It is the simplest algorithm that relies on information from the gradient vector. A first-order approach is the GD algorithm.

![](Image00043.jpg)

w (i+1)  =  w (i)  -  g (i) n (i) .

### Newton's Method

A second-order algorithm is Newton's process. It employs the Hessian matrix. Its main goal is to use the second derivatives of the loss function to find better training directions.

The iteration of Newton's method is as follows.

w (i+1)  =  w (i)  -  H (i)-1 . g (i) For i = 0, 1.....

Here, H (i)-1 .g (i)  is known as Newton's step. The shift in parameters may be moving toward a limit instead of a minimum.

The training of a neural network using Newton's method is depicted in the diagram below.

The parameter can be improved by determining the training path and a reasonable training pace.

### Conjugate gradient

Between gradient descent and Newton's process, conjugate gradient is used.

Conjugate gradient avoids the knowledge requirements of Newton's process, such as evaluation, inversion of the Hessian matrix, and storage.

The CG algorithm searches in a conjugate direction rather than a gradient descent direction, which results in faster convergence.

In terms of the Hessian matrix, the training is performed in a conjugate direction.

The parameter is improved by calculating the conjugate training path and then selecting an acceptable training rate in that direction.

### Quasi-Newton Method

In terms of computation, Newton's approach is time-consuming. Many operations are needed to evaluate the Hessian matrix.

The Quasi-Newton Method was created to address this flaw. Variable matric process is another name for it.

Rather than computing the inverse hessian directly, an algorithm builds up an approximation to it at each iteration.

Approximation is computed using information from the loss function's first derivative.

### Levenberg Marquardt

A damped least-squares system is also known as Levenberg Marquardt. This algorithm was created with the loss function in mind. The Hessian matrix is not computed by this algorithm. The Jacobian matrix and the gradient vector are used.

The first step in Levenberg Marquardt is to determine the loss, gradient, and Hessian approximation, after which the dumpling parameter is modified.

Artificial Neural Networks: Benefits and Drawbacks

### Advantages of ANN

![](Image00044.jpg)

### Disadvantages of ANN

![](Image00045.jpg)

# TensorFlow Linear Regression  

Linear regression is a supervised learning-based machine learning algorithm. It carries out a regression analysis.

Based on the independent variable, the regression models a goal predictive value.

It's often used to figure out how variables and forecasts are related.

A linear model, such as one that assumes a linear relationship between an input variable (x) and a single output variable, is known as linear regression (y).

A linear combination of input variables can be used to measure y in particular (x).

Linear regression is a widely used statistical technique for learning a function or relationship from a collection of continuous data.

For example, suppose we are given some x and corresponding data points and we need to know the relationship between them, which is referred to as the hypothesis.

In linear regression, the hypothesis is a straight line, which means that

h (x) = wx + b

Where w denotes a weight vector and b denotes a bias scalar. The model's weight and bias are referred to as parameters.

We must estimate the values of w and b from the data set in such a way that the resultant hypothesis produces at least cost 'j,' as described by the cost function below.

![Linear Regression in TensorFlow](Image00046.jpg)

##### Where m denotes the number of data points in the dataset.

##### The Mean Squared Error is the name of this cost function.

##### We will use a widely used optimizer algorithm called gradient descent to optimize parameters for which the value of j is small. The following is gradient descent pseudocode:

##### Repeat until Convergence {  

#####     w = w - ? * ?J/?w  

#####     b = b - ? * ?J/?b  

##### }  

## Implementation of Linear Regression

In Tensorflow, we'll begin by importing the required libraries. For computation, we'll use Numpy with Tensorflow, and for plotting, we'll use Matplotlib.

##### First, we must import the following packages:

##### import  matplotlib.pyplot as plt  

##### import  numpy as np  

##### import  tensorflow as tf  

We must identify fixed seeds for both Tensorflow and Numpy in order to predict random numbers.

##### tf.set_random_seed(101)  

##### np.random.seed(101)  

We must now create some random data in order to train the Linear Regression Model.

##### # Generating random linear data   

##### # There will be 50 data points which are ranging from 0 to 50.  

##### x = np.linspace(0, 50, 50)   

##### y = np.linspace(0, 50, 50)   

##### # Adding noise to the random linear data   

##### x += np.random.uniform(-4, 4, 50)   

##### y += np.random.uniform(-4, 4, 50)   

##### n= len(x) #Number of data points  

Let's take a look at the training results.

# Plot of Training Data

##### plt.scatter(x, y)   

##### plt.xlabel('x')   

##### plt.xlabel('y')   

##### plt.title("Training Data")   

##### plt.show()   

We'll begin by identifying placeholders x and y, which will be used to feed the training examples x and y into the optimizer during the training phase.

##### X= tf.placeholder("float")  

##### Y= tf.placeholder("float")  

We can now declare two trainable TensorFlow variables for bias and Weights, and use the method to randomly initialize them:

##### np.random.randn().  

##### W= tf.Variable(np.random.randn(), name="W")  

##### B= tf.Variable(np.random,randn(), name="b")  

##### The model's hyperparameter, the learning rate, and the number of Epochs are now specified.

##### learning_rate= 0 .01  

##### training_epochs= 1000

##### We can now build Hypothesis, Cost Function, and Optimizer. Since the Gradient Decent Optimizer is integrated into TensorFlow, we will not manually implement it. The variables in the process would then be initialized.

##### # Hypothesis of the function  

##### y_pred = tf.add(tf.multiply(X, W), b)   

##### # Mean Square Error function  

#####       cost = tf.reduce_sum(tf.pow(y_pred-Y, 2)) / (2 * n)    

##### # Gradient Descent Optimizer function  

##### optimizer = tf.train.GradientDescentOptimizer (learning_rate).minimize(cost)  

##### # Global Variables Initializer   

##### init = tf.global_variables_initializer( )  

##### Now we start the training process inside the TensorFlow Session.

##### # Starting the Tensorflow Session   

##### with tf.Session() as sess:   

#####    # Initializing the Variables   

#####     sess.run(init)   

#####    # Iterating through all the epochs   

#####      for  epoch in range(training_epochs):   

#####     # Feeding each data point into the optimizer according to the Feed Dictionary.  

#####    for  (_x, _y) in zip(x, y):    

#####   sess.run(optimizer, feed_dict = {X : _x, Y : _y})    

##### # Here, we are displaying the result after every 50 epoch    

#####          if  (epoch + 1) % 50 ==0:   

#####  # Calculating the cost at every epoch.   

#####  c = sess.run(cost, feed_dict = {X : x, Y : y})    

##### print("Epoch", (epoch + 1), ": cost =", c, "W =", sess.run(W), "b=", sess.run(b))  

#####  # Store the necessary value which has used outside the Session   

#####     training_cost = sess.run (cost, feed_dict ={X: x, Y: y})    

#####     weight = sess.run(W)   

#####     bias = sess.run(b)

Output is given below:

![](Image00047.jpg)

![](Image00048.jpg)

Now, see the result.

##### # Calculate the predictions  

##### predictions = weight * x + bias   

##### print ("Training cost =", training_cost, "Weight =", weight, "bias =", bias, '\n')   

Output

Training cost= 5.3110332 Weight= 1.0199214 bias=0.02561663

It's worth noting that both weight and bias are scalars in this situation. This is due to the fact that we only looked at one dependent variable in our training results. If our training dataset has m dependent variables, the weight will be a one-dimensional vector, while Bias will be a scalar.

Finally, we'll graph our results:

##### # Plotting the Results below  

##### plt.plot(x, y, 'ro', label ='original data')  

##### plt.plot(x, predictions, label ='Fited line')  

##### plt.title('Linear Regression Result')   

##### plt.legend()   

##### plt.show()