![](images/00013.jpeg)

# Table of Contents

[WHAT IS JAVASCRIPT?](#part0001_split_002.html_pAt0)

[EMBEDDING JAVASCRIPT IN A WEB PAGE](#part0001_split_003.html_pATY)

[KEY TERMS](#part0001_split_004.html_pAPhMh)

[WORKING WITH JAVASCRIPT](#part0001_split_005.html_pA3tR)

[VALUES](#part0001_split_006.html_pAYp)

[OPERATORS](#part0001_split_007.html_pAqy)

[KEYWORDS AND COMMENTS](#part0001_split_008.html_pAPiEB)

[JAVASCRIPT DATA TYPES](#part0001_split_009.html_pAPef)

[OBJECTS](#part0001_split_010.html_pAXt_)

[HTML DOM](#part0001_split_011.html_pAMH)

[JAVASCRIPT OBJECT HIERARCHY](#part0001_split_012.html_pAUzc)

[JAVASCRIPT ARRAYS](#part0001_split_013.html_pANE)

[JAVASCRIPT EVENTS](#part0001_split_014.html_pAst8)

[AJAX AND CSS](#part0001_split_015.html_pA_ij)

[ONLINE RESOURCES](#part0001_split_016.html_pAqLi)

![images/img-2-1.png](images/00001.jpeg)

* * *

# JavaScript Fundamentals

* * *

## WHAT IS JAVASCRIPT?

JavaScript is a cross-platform, interpreted, object-based scripting language originally developed by Netscape Communications Corporation (now Oracle Corporation) to add multimedia elements, dynamic pages, and interactive content to a website. JavaScript allows web developers to dynamically change the content of a web page, as well as add form validation, manipulate images, open new windows, and much more. JavaScript can also be used to get information about the Internet browser and HTML page. JavaScript can be used together with Cascading Style Sheets to create Dynamic HTML. It is supported by most Internet browsers and enables interactive functions to be added to web pages.

### Two Types of JavaScript

*   **Client-side**
    *   Enables enhancement and manipulation of web pages and client browsers
    *   Parsed and executed on client machine
*   **Server-side** (also known as "LiveWire")
    *   Enables back-end access to databases, file systems, and servers
    *   Stored and executed on server machine

### JavaScript versus Java

JavaScript is not part of the Java platform, nor does it create applets or standalone applications. It is embedded inside HTML files and adds interactivity to otherwise static HTML web pages. Java is an object-oriented programming language while Java Script is an object-based scripting language. Java creates applications that run on a virtual machine or browser while JavaScript code is run on a browser only. Java code needs to be compiled while JavaScript code is all in text. Both require different plug-ins.

### Differences between JavaScript and Java

| **JavaScript** | **Java** |
| Interpreted by client (executes without compiling) | Compiled on server |
| Object-based | Object-oriented |
| Variable data types are not declared Dynamic binding | Variable data types should be declared Static binding |
| Dynamic binding | Static binding |
| Code embedded in HTML | Code runs only on systems with installed Java platform |

**Did you know?**

When JavaScript was developed by Netscape Communications Corporation back in 1995, it was originally named Mocha, then renamed to LiveScript since it was intended to be used as a server-side language similar to PHP. It was later renamed to JavaScript in Netscape 3.0 as a marketing move in order to promote Sun Microsystems’ programming language called Java.

### JavaScript Version History

| **Release Date** | **Version** | **Browser** | **Remarks** |
| 1996 | 1.0-1.1 | Netscape Navigator 2.0-3.0 and Internet Explorer 2.0. | Added new objects such as array, Boolean, function, and number |
| 1997 | 1.2 | Netscape Navigator 4.0-4.05 | Added ability to nest functions within functions and regular expressions, as well as ability to create objects and arrays using literal notation |
| 1998 | 1.3 | Netscape Navigator 4.06-4.7x | Includes Unicode support, JavaScript console, several changes to data.prototype methods, and strict equality operators |
| 1999 | 1.4 | Server-side JavaScript | Changes to LiveConnect, exception handling (throw and try… catch) |

| **Release Date** | **Version** | **Browser** | **Remarks** |
| 2000 | 1.5 | Netscape Navigator 6.0 and Firefox 1.0 | Included standardization for ECMA-262 3^(rd) Edition compliance |
| 2005 | 1.6 | Firefox 1.5 | Includes ECMAScript for XML (E4X), Array methods plus string and array generics |
| 2006 | 1.7 | Firefox 2 | Includes generators, iterators, array comprehensions, let expressions, and destructuring assignment |
| 2008 | 1.8 | Firefox 3 | Includes expression closures, generator expressions, array. prototype.reduce(), and array.prototype.reduceRight() |
| 2009 | 1.8.1-1.8.2 | Firefox 3.5-3.6 | Includes the TraceMonkey JIT and supports native JSON |
| 2010 | 1.8.5 | Firefox 4 | Includes many new features for ECMA-262 Edition 5 compliance |

### Parts of JavaScript

*   **Basic Syntax**: JavaScript is based on the ECMAScript 262 standard, which defines how the core part of the language works. This includes the definition of how variables are defined, how calculations on those variables are performed, how loops and functions are set up, and how objects are defined.

![images/himg-2-1.png](images/00002.jpeg)

*   **Document Object Model:** Defines how JavaScript communicates with a web page to extract content from the page for processing, adding content, or accessing the stylesheet to change the appearance of a page.
*   **Browser Object Model:** Defines how the scripts obtain information from the browser and pass information back to it.

## EMBEDDING JAVASCRIPT IN A WEB PAGE

There are two ways to embed JavaScript in an HTML file:

**Steps**

*   Link to external file(s) with the file extension .js

1.  Enter the following code to notepad or any text editor and then save it as FirstCode htm

    ![images/himg-2-2.png](images/00003.jpeg)

2.  Enter the following code to notepad or any text editor and then save it as MyFirstJavaScriptFile.js

    ![images/himg-2-3.png](images/00004.jpeg)

3.  Open your web browser, such as Internet Explorer, Mozilla Firefox, and Google Chrome, to see the result:

    ![images/himg-3-1.png](images/00005.jpeg)

*   Write blocks of code in HTML documents with the <script> tag

    **Steps**

1.  Copy and paste the following code to notepad or any text editor and then save it as FirstCode.htm

    ![images/himg-3-2.png](images/00006.jpeg)

2.  Open your web browser, such as Internet Explorer, Mozilla Firefox, and Google Chrome, to see the result:

    ![images/himg-3-3.png](images/00007.jpeg)

## KEY TERMS

| **Terms** | **Description** | **Terms** | **Description** |
| Class | Defines the characteristics of an object | Namespace | A container which is used to bundle all functionality under a unique, application-specific name |
| Cookie | An object containing information about the client that can be accessed by the server | Objects | Refers to windows, documents, images, tables, forms, buttons or links, etc. |
| Events | Occurrences that happen in the context of the interaction between the web server, user and the browser | Operators | Used to handle variables |
| Expressions | Commands that assign values to variables | Properties | Refers to object attributes |
| Functions | Statements that perform tasks and include built-in and user-defined functions | Values | Refers to bits of information, such as number, string, boolean, null, object, and function |
| Methods | Actions applied to particular objects | Variables | A named location in memory that is used to hold a value that can be changed by the program |

## WORKING WITH JAVASCRIPT

**Statements**

JavaScript statements consist of values, operators, expressions, keywords, and comments.

| **Statements** |
| **Statement** | **Description** |
| const | Defines a read-only **constant** whose value cannot be changed (unlike a variable using “var”). It also cannot be re-declared once initially defined. |
| **const mysalary =3000 //start** (with a letter or underscore, then alphabetic) |
| var | The **var** statement is used to explicitly declare a variable in JavaScipt. While technically it is not necessary to insert the var statement in front of a variable to create it, it is a good programming practice. Once a variable is declared, that variable can continue to be referenced without including the var statement. |
| var x=5 x=x+10//
(x now contains 15) |
| with | The **with** statement is a time-saving statement to “cache” an object so that for statements that follow it is no longer necessary to reference the object again when referring to it. |
| with (document form 1)[field1 value=”test” field 2 value=”test2”] |

| **Conditional Statements** |
| **Statement** | **Description** |
| if | Specifies a block of code to be executed if the condition is true. |
| <html> <body>
<script type=”text/javascript”>
var age=28;
if (age > 18){document.write (<b>Qualifies for a driving
license</b>”;}
<script>
<body>
<html> |
| **Result:** Qualifies for a driving license |
| if/else | Specifies a new condition to test if the first condition is false. |
| <html> <body>
<script type=”text/javascript”>
var age=17; if (age > 18){document.write (<b>Qualifies for a driving
license</b>”;}
else {document.write (<b>Does not qualify for a driving
license</b>”;}
<script>
<body>
<html> |
| **Result:** Qualifies for a driving license or does not qualify for a driving license |
| switch case break default | **“Switch”** executes a different statement depending on the value of an expression. **“Break”** is an optional statement that instructs “switch” to exit should the preceding statement be executed. **“Default”** instructs the statement to execute if none of the statements are executed. |
| <html> <body>
<script type=”text/javascript”>
var grade=’A’;
document.write (“Entering switch block=<br/>);
switch (grade)
{case ‘A’: document.write(“Excellent<br/>);break;
case ‘B’ document.write(“Good<br/>);break;
case ‘C’ document.write(“Average<br/>);break;
case ‘D’ document.write(“Below average<br/>);break;
case ‘F’ document.write(“Poor<br/>);break;
default: document.write(“No grade<br/>);break; }
document.write (“Exiting switch block);
<script>
<body>
<html> |
| **Result:** Entering switch block/ Excellent/ Exiting switch block |
| ?: | “?:” or the conditional operator is used for constructing an evaluation and executing two different assignments depending on the result. |
| <html> <body>
<script type=”text/javascript”>
var a = 15;
var b = 30;
var linebreak = “<br />”;
document.write (“((a > b) ? 150 : 300) => “);
result = (a > b) ? 150 : 300;
document.write (result);
document.write (linebreak);
document.write (“((a < b) ? 150 : 300) => “);
result = (a < b) ? 150 : 300;
document.write (result);
document.write (linebreak);
</script>
</body>
</html> |
| **Result:** ((a > b) ? 150 : 300) => 300 ((a < b) ? 150 : 300) => 150 |
| return | “Return” exits a function and optionally returns a value. It is used inside functions. |
| <html> <head>
<script type=”text/javascript”>
function concatenate(first, last)
{
var full;
full = first + last;
return full;
}
function second Function()
{
var result;
result = concatenate (‘Book’, ‘Dog’);
alert(result );
}
</script>
</head>
<body>
<p>Click the following button to call the function</p>
<form>
<input type=”button” onclick=”second Function()” value=”Call
Function”>
</form>
</body>
</html> |
| **Result:** BookDog |

| **Looping Statements** |
| **Statement** | **Description** |
| for | The statement **for** executes the enclosed statements multiple times based on three conditions **initial, limit,** and **increment** defined inside the “for” parenthesis ( ). |
| <html> <body>
<script type=”text/javascript”>
var count;
document.write (“Start Loop…”
+”<br/>);
for(count=0;count=6; count++)
{document.write(“Current Count :”
+ count );
a document.write(<br/>);}
document.write(“…End loop!”);
<script>
<body>
<html> |
| while | A **while** loop continuously executes the enclosed statements as long as the tested expression evaluates to true. If the expression is false, the entire while loop is skipped. |
| <html> <body>
<script type=”text/javascript”>
var count = 0;
document.write(“Start loop...”);
while (count < 6){
document.write(“Current
Count : “ + count + “<br />”);
count++;
}
document.write(“... End loop!”);
</script>
</body>
</html> |
| Do/while | This statement differs from the standard **while** statement in that the expression tested for is placed at the end, ensuring that a **do/while** loop is always executed at least once. |
| <html> <body>
<script type=”text/javascript”>
<!--
var count = 1;
document.write(“Starting
Loop” + “<br />”);
do{
document.write(“Current
 Count : “ + count + “<br />”);
count++;
}while (count < 0);
document.write(“Loop
stopped!”);
//-->
</script>
</body>
</html> |
| for/in | Loops through the properties of an object; applies to built-in or custom objects. |
| <html> <body>
<script type=”text/javascript”>
var aProperty;
document.write(“Navigator
Object Properties<br /> “);
for (aProperty in navigator)
{
document.write(aProperty);
document.write(“<br />”);
}
document.write(“... End loop!”);
</script>
</body>
</html> |
| break | Causes an exit of the innermost loop in which the statement is contained. It is used to prematurely end a loop. |
| <html> <body>
<script type=”text/javascript”>
var x = 0;
document.write(“Start
 loop...<br /> “);
while (x < 20)
{
if (x == 5){
break; // breaks out of loop
completely
}
x = x + 1;
}
document.write(“... End
loop!<br /> “);
</script>
</body>
</html> |
| continue | Causes JavaScript to skip the rest of the statements that may follow in a loop, and continue with the next iteration. Unlike in a break statement, the loop is not exited. |
| <html> <body>
<script type=”text/javascript”>
var x = 0;
document.write(“Start
loop...<br /> “);
while (x < 6)
{
x = x + 1;
if (x == 5){
continue; // skill rest of the
loop body
}
document.write( x + “<br />”);
}
document.write(“... End
loop!<br /> “);
</script>
</body>
</html> |

## VALUES

The two types of **values** used in the JavaScript syntax are fixed and variable values.

*   **Literals:** Fixed values are called **literals**. In JavaScript, numeric values are written with or without decimals such as:

    9.5
    9

    while text strings are written either with double or single quotes such as

    study guide”
    Harvard University’

    Fixed values can also refer to expressions written as:

    5 + 7
    5 * 7

*   **Variables:** Non-fixed values are called **variables**, which are used to store values. In JavaScript, the keyword **var** is used to define variables. The equal sign (=) is used to assign values to variables such as:

    var myName = “John”

**Rules When Naming Variables**

*   Variables cannot be reserved words.
*   Variables should start with a letter or an underscore (e.g., “myName” or “ _myName”).
*   Numbers can be used in variable name as long as it is not the first character (e.g., “myName01” or “myName$”).
*   Spaces are not allowed in variable names (e.g., “my Name” should be “myName”).
*   The first letter of every word should be capitalized, except the first (e.g., “myName” or “myFirstName”).
*   To declare variables, the keyword **var** and the variable name is used (e.g., “var myName”).
*   To assign values to variables, the equal sign and the value are added (e.g., “var myProduct = “Laser” var price = 400).
*   Variable names are case sensitive, so **y** does not equal **Y**.

## OPERATORS

An **operator** acts on a variable and changes its value. JavaScript language supports the following type of operators: arithmetic, assignment, bitwise, comparison, conditional, and logical.

| **Arithmetic Operators** |
| **Operator** | **Description** | **Given Variables** A = **15** and B = **30** |
| **+** | Adds two operands |  |
|  | A + B | **Result =** 45 |
| **-** | Subtracts second operand from first |  |
|  | A - B | **Result = -**15 |
| ***** | Multiplies both operands |  |
|  | A * B | **Result =** 450 |
| **/** | Divides numerator by denominator |  |
|  | B / A | **Result =** 2 |
| **%** | **Modulus** operator; finds the remainder |  |
|  | after division of one number by another |  |
|  | B % A | **Result =** 0 |
| **++** | **Increment** operator; increases integer |  |
|  | value by one |  |
|  | A++ | **Result =** 16 |
| **--** | **Decrement** operator; decreases integer |  |
|  | value by one |  |
|  | A-- | **Result =** 14 |

| **Assignment Operators** |
| **Operator** | **Description** | **Result** |
| **=** | **Simple assignment** operator assigns values from right side operands to left side operand |  |
|  | C = A + B | Assigns value of A+B into C |
| **+=** | **Add AND** assignment operator adds right operand to the left operands and assigns the result to the left operand |  |
|  | C += A | Equivalent to C = C + A |
| **-=** | **Subtract AND** assignment operator subtracts right operand from left operand and assigns the result to left operand |  |
|  | C -= A | Equivalent to C = C-A |
| ***=** | **Multiply AND** assignment operator multiplies right operand with the left operand and assigns the result to left operand |  |
|  | C *= A | Equivalent to C = C * A |
| **/=** | **Divide AND** assignment operator divides left operand with the right operand and assigns the result to left operand |  |
|  | C /= A | Equivalent to C = C / A |
| **%=** | **Modulus AND** assignment operator takes modulus using two operands and assigns the result to left operand |  |
|  | C %= A | Equivalent to C = C % A |

| **Bitwise Operators** |
| **Operator** | **Description** | **Given Variables** A = **2** and B = **3** |
| **&** | Bitwise **AND** operator performs a Boolean AND operation on each bit of its integer arguments |  |
|  | (A & B) | **Result =** 2 |
| **&#124;** | Bitwise **OR** operator performs a Boolean OR operation on each bit of its integer arguments |  |
|  | (A &#124; B) | **Result =** 3 |
| **^** | Bitwise **XOR** operator performs a Boolean OR operation on each bit of its integer arguments |  |
|  | (A ^ B) | **Result =** 1 |
| **~** | Bitwise **NOT** operator is a unary operator that reverses all bits in the operand |  |
|  | (~ B) | **Result = -**4 |
| **<<** | Bitwise **Shift Left** operator moves all bits in its first operand to the left by the number of places specified in the second operand |  |
|  | A << 1 | **Result =** 4 |
| **>>** | Bitwise **Shift Right** operator moves all bits in its first operand to the right by the number of places specified in the second operand |  |
|  | A >> 1 | **Result =** 1 |
| **>>>** | Bitwise **Shift Right with Zero** operator; similar to the >> operator except that the bits shifted in on the left are always zero (0) |  |
|  | A >>> 1 | **Result =** 1 |

| **Comparison Operators** |
| **Operator** | **Description** | **Given Variables** A = **15** and B = **30** |
| **==** | Checks if the value of two operands are equal or not; if yes, then the condition becomes true |  |
|  | (A == B) | **Result =** Not true |
| **!=** | Checks if the value of two operands are equal or not; if values are not equal then the condition becomes true |  |
|  | (A != B) | **Result =** True |
| **>** | Checks if the value of the left operand is greater than the value of the right operand, then the condition becomes true |  |
|  | (A > B) | **Result =** Not true |
| **<** | Checks if the value of the left operand is less than the value of the right operand, then the condition becomes true |  |
|  | (A <= B) | **Result =** True |
| **>=** | Checks if the value of the left operand is greater than or equal to the value of the right operand, then the condition becomes true |  |
|  | (A >= B) | **Result =** Not true |
| **<=** | Checks if the value of the left operand is less than or equal to the value of the right operand, then the condition becomes true |  |
|  | (A <= B) | **Result =** True |

| **Conditional Operators** |
| **Operator** | **Description** |
| **?:** | Conditional expression |
|  | If Condition is true, then value = X, otherwise value =Y |

| **Logical Operators** |
| **Operator** | **Description** | **Given Variables** A = **15** and B = **30** |
| **&&** | **Logical AND operator.** If both the operands are non-zero, then the condition becomes true |  |
|  | (A && B) | **Result =** True |
| **&#124;&#124;** | **Logical OR operators.** If any of the two operands are non-zero, then the condition becomes true |  |
|  | (A &#124; &#124; B) | **Result =** True |
| **!** | **Logical NOT operator.** Use to reverse the logical state of its operand. If a condition is true, then the Logical NOT operator will make it false. |  |
|  | (A && B) | **Result =** False |

## KEYWORDS AND COMMENTS

JavaScript Keywords

Keywords in JavaScript are utilized to identify actions to be performed. For example, the var keyword instructs the browser to create a new keyword:

var x = 1 + 2;
var y = x * 15;

### Reserved Words

In JavaScript, several identifiers are reserved words. These keywords cannot be used as variables, functions, methods, loop labels, or any object names when programming with JavaScript.

| abstract | else | instanceof | switch |
| boolean | enum | int | synchronized |
| break | export | interface | this |
| byte | extends | long | throw |
| case | false | native | throws |
| catch | final | new | transient |
| char | finally | null | true |
| class | float | package | try |
| const | for | private | typeof |
| continue | function | protected | var |
| debugger | goto | public | void |
| default | if | return | volatile |
| delete | implements | short | while |
| do | import | static | with |
| double | in | super |  |

### Comments

JavaScript supports C-, C++-, and HTML comments. Text entered between “//” and the end of a line is treated as a comment and is ignored by JavaScript. Another comment formatting recognized by JavaScript is the tag “/*”. Text that is entered between “/*” and “*/” (may span multiple lines) is ignored, as is the opening and closing tags “<!—“ and “//-->”.

**Example:**

![images/himg-6-1.png](images/00008.jpeg)

**Tips When Writing JavaScript**

*   Line breaks are ignored except within a statement.
*   JavaScript is case sensitive—keywords, variables, function names, and other identifiers should use consistent capitalizaton.
*   White spaces between words and tabs are ignored.
*   JavaScript statements end with a semicolon, unless they are placed on a separate line.

## JAVASCRIPT DATA TYPES

Data types are the classification of values based on the specific categories where they are stored. There are two types:

*   Primitive Types – refer to String, Boolean, Integer, Floating Point, Null, Void
*   Composite Types – refer to Object, Array, Function

### JavaScript Numeric

| Integer | Positive or negative numerical values that have no fractional parts or decimal places |
| Floating Point | Positive or negative numerical values that have a decimal point or exponential notations |
| String | Characters or text surrounded by single or double quotes |
| Boolean | Logical values True or False |
| Null | Variable that does not have a value |
| Casting | Moving the contents of a variable from one type to another |

### JavaScript String

JavaScript strings are used for storing and manipulating text. The JavaScript string stores a series of characters like “study guides.” A string can be any text inside quotes. You can use single or double quotes. You can also use quotes inside a string, as long as they do not match the quotes surrounding the string.

**Escape Sequences**

String escape sequences allow the user to parse string literals in JavaScript for special characters/ formatting, such as newlines within a TEXTATEA’s input.

| **Escape Sequences** |
| **Properties** | **Description** |
| \b | Backspace |
| \f | Form feed |
| \n | Newline |
| \O | Null character |
| \r | Carriage return |
| \t | Horizontal tab |
| \v | Vertical tab |
| \’ | Single quote or apostrophe |
| \” | Double quote |
| \\ | Backslash |
| \ddd | The Latin-1 character specified by the three octal digits between 0 and 377\. i.e. copyright symbol is \251 |
| \xdd | The Latin-1 character specified by the two hexadecimal digits dd between 00 and FF. i.e. copyright symbol is \xA9 |
| \udddd | The Unicode character specified by the four hexadecimal digits dddd. i.e. copyright symbol is \u00A9 |

### JavaScript Boolean

Boolean (15 >10) // returns true
(5>10) 1 ………// returns true
11>10…… …….// returns true

Extra large or extra small numbers can be written with scientific (exponent) notation:

var x = 124e5; // 12400000
var y = 124e-5; // 0.00124

### JavaScript Numbers

JavaScript has only one type of number. Numbers can be written with or without the decimal point such as:

var x – 39.00 // A number with a decimal point
var y = 39…// A number without a decimal point

**Tip On Numbers**

*   Numbers always use 64-bit floating point.
*   Unlike many other programming languages, JavaScript does not define defferent types of numbers, such as integers, short, long, floating point, etc.
*   JavaScript numbers are always stored as double precision floating point numbers, following the international IEEE 754 standard.

### JavaScript Null

Null is considered something without value, nothing, or simply does not exist. In JavaScript, the data type of null is an object. An object can be emptied by setting it to null, like this:

var person = null; // Value is null, but type is still an object

### JavaScript Void

The void keyword in JavaScript is used as a unary operator that appears before its single operand. This operator specifies an expression to be evaluated without returning a value.

<html>
<head>
<script type="text/javascript">
</script>
</head>
<body>
<p>Please click the following, This won't affect me at
all...</p>
<a href="javascript:void(alert(0))">Please click me!</a>
</body>
</html>

The above script produces the following result when the **Please click me** link is clicked:

![images/himg-7-1.png](images/00009.jpeg)

### Composite Types

**Functions**

A function is a block of JavaScript code that performs a specific task whenever it is executed or invoked. It is defined with the **function keyword,** followed by the function name and parenthesis ( ). It may contain letters, digits, underscore symbol, and dollar signs. The parentheses may include parameter names separated by commas such as parameter1, parameter2, etc. The code to be executed is placed inside the curly brackets { }.

![images/himg-7-2.png](images/00010.jpeg)

**Example:**

function convertDataToCentrigrade (degFarenheit)

{

var degCentigrade;

degCentigrade = 5/9 * (degFarenheit – 32);

return degCentigrade;

}

## OBJECTS

Objects are composite data types that contain properties and methods. Screen elements such as web pages, text boxes, forms, buttons, and images are considered as objects. In JavaScript, all values, except **primitive values**, are considered as objects.

Properties define the characteristics of an object.

### Properties

| **Object Properties** |
| **Property** | **Value** |
| firstName | Clark |
| lastName | Mays |
| age | 18 |
| eyeColor | Green |

### Methods

Actions that can be performed on objects are called **methods**. An **object method** is an object property containing a function definition.

| **Object Methods** |
| **Property** | **Value** |
| firstName | Clark |
| lastName | Mays |
| age | 18 |
| eyeColor | Green |
| fullName | function() {
return this.firstName + “ “ + this.
lastName;
} |

| **Object Names** |
| **Description** | **Name** |
| When an **objec**t is being referred to | objectName |
| When a **property** of an object is being referred to | objectName.propertyName |
| When a method of an object is being referred to | objectName.methodName() |

| **Built-In Objects** |
| **Object Name** | **Description** | **Format** |
| Math Object | Provides methods for various mathematical operations , including abs (), log (), pow(), random(), round(), sqrt() | Math.method(#) |
| <SCRIPT language = “JavaScript”> Var theValue =3.14
myAns = Math.round (the value)
</SCRIPT> |
| **Object Name** | **Description** | **Format** |
| Date Object | Provides date and time information | dateObject. method() |
| <SCRIPT language = “JavaScript”> var valDat = new Date()
theYr = valDat.getFullYear()
</SCRIPT> |
| **Object Name** | **Description** | **Format** |
| String Object | Provides methods and properties for string manipulation and formatting | stringName. method() |
| <SCRIPT language = “JavaScript”> var theStringValue = “my name”
var printString = theString.bold()
var numChars = theStringValue.
length
</SCRIPT> |
| **Object Name** | **Description** | **Format** |
| Array Object | Used to store multiple values called **elements** in a single variable | var array.name =[item1, item2…]; |
| <SCRIPT language = “JavaScript”> var cars = [“Toyota”, “Isuzu”, “Kia”];
document.getElementById(“demo”).
innerHTML = cars;
</SCRIPT> |
| **Object Name** | **Description** | **Format** |
| Boolean Object | Represents either true or false | var val = new Boolean (value); |
| <SCRIPT language = “JavaScript”> function myFunction() {
var x = 0; document.
getElementById(“demo”).
innerHTML = Boolean(x);
}
</SCRIPT> |

| **Document Methods** |
| **Property/Method** | **Description** | **Syntax** |
| document.body | Retrieves the document’s body <body> | document.body |
| document.body.style backgroundColor = “red”; |
| document.close () | Closes the document | document.close() |
| document.open(); document.write(“<h1> Hello Earth </h1>);
document.close(); |
| document.cookie | Retrieves the name/ value pairs of cookies | document.cookie |
| var y = document.cookie; |
| document.domain | Retrieves the domain name of the server | document.domain |
| var y = document.domain; |
| document.links | Retrieves all the <a> and <area> elements in the document that have a href attribute | document.links |
| var y = document.links. length; |
| document.open() | Opens the document | document.open (MIMEtype, replace) |
| document.open(); document.write(“<h1> Hello Earth</h1>”); document.close(); |
| document. renameNode() | Renames the specified node | document.rename Node(node,namesp aceURI,nodename) |
| var y = document. getElementsByTag Name(“P”)[0]; document.renameNode(p, null, “h1”); |
| document.scripts | Retrieves the <script> elements in the document | document.scripts |
| var y = document. scripts.length; |
| document.title | Retrieves the document title | document.title |
| var y = document.title; |
| document.URL | Retrieves the URL | document.URL |
| var y = document.URL; |
| document.write() | Writes HTML expressions or JavaScript code | document. write(exp1,exp2,exp3…) |
| document.write(“Hello Earth”); |

## HTML DOM

The HTML Document Object Model (DOM) is a standard object model and programming interface for HTML and XML. It defines the logical structure of documents and the way they are accessed and manipulated. DOM can be used and accessed with JavaScript or other programming languages. All HTML elements are defined as objects in DOM. Examples of document methods are provided below:

| **Property/ Method** | **Description** | **Syntax** | **Example** |
| document. body | Retrieves the document’s body <body> | document. body | document.body.style. backgroundColor = “red”; |
| document. close() | Closes the document | document. close() | document.open(); document.write(“<h1> Hello Earth</h1>”); document.close(); |
| document. cookie | Retrieves the name/ value pairs of cookies | document. cookie | var y = document. cookie; |
| document. domain | Retrieves the domain name of the server | document. domain | var y = document. domain; |
| document. links | Retrieves all the <a> and <area> elements in the document that have a href attribute | document. links | var y = document.links. length; |
| document. open() | Opens the document | document. open(MIME type,replace) | document.open(); document.write(“<h1> Hello Earth</h1>”); document.close(); |
| document. rename Node() | Renames the specified node | document. rename Node(node,n amespaceUR I,nodename) | var y = document. getElementsByTag Name(“P”)[0]; document.rename Node(p, null, “h1”); |
| document. scripts | Retrieves the <script> elements in the document | document. scripts | var y = document. scripts.length; |
| document. title | Retrieves the document title | document. title | var y = document.title; |
| document. URL | Retrieves the URL | document. URL | var y = document.URL; |
| document. write() | Writes HTML expressions or JavaScript code | document. write(exp1, exp2,exp3,...) | document.write(“Hello Earth”); |

## JavaScript Object Hierarchy

When the user loads a document in a browser, JavaScript objects with property values based on the HTML in the document and other information are created. These objects exist in a **hierarchy** that is based on the structure of the HTML page. DOM made it possible to change a web page dynamically. Through DOM, the user can locate any element in the HTML document and use JavaScript to change the element’s properties. The DOM hierarchy is illustrated below:

![images/himg-8-1.png](images/00011.jpeg)

### Window Object

The window object refers to an open window in a browser. It is used to open a web page in a new window and to set the attributes for the window. The two main window properties are:

| **Window Properties** |
| **Property** | **Value** |
| Status | Sets the message for the status |
| Self | Stores the name of the current window |

### Window Methods

The window methods are used for opening and closing new windows.
The main window methods are:

| **Window Methods** |
| **Method** | **Description** |
| alert() | Displays a message box |
| confirm() | Displays a confirmation box |
| prompt() | Displays a prompt box |
| open() | Opens a new window |
| close() | Closes a window |

## JAVASCRIPT ARRAYS

In JavaScript, an **array** is a special variable that can hold multiple values in a single variable. To create an array, an **array literal** is used.

**Syntax:**

var array-name = [item1, item2, ...];

**Example:**

var car = [“Toyota”, “Mazda”, “Isuzu”];

Arrays use numbers to access elements. In the example below, person[0] returns Harry:

**Example:**

var person = [“Harry”, “Crawford”, 45]);

## JAVASCRIPT EVENTS

Events refer to how feedback is elicited from the web user. Interaction with HTML is being handled through events that happen when the user interacts with the browser by clicking, loading, closing, resizing, or manipulating a web page. Events are a part of DOM Level 3 and every HTML element has a certain set of events which trigger a JavaScript code. Examples of these are included below:

| **Types of Events** |
| **Event** | **Description** |
| onblur | Executed when the element loses focus |
| onchange | Executed when the element changes |
| onclick | Executed when an object is clicked |
| ondblclick | Executed when an object is double-clicked |
| onfocus | Executed when the element gets focus |
| onkeydown | Executed when key is pressed |
| onkeypress | Executed when key is pressed and released |
| onkeyup | Executed when key is released |
| onmousedown | Executed when mouse button is pressed |
| onmousemove | Executed when mouse pointer moves |
| onmouseout | Executed when mouse pointer moves out of an element |
| onmouseover | Executed when mouse pointer moves over an element |
| onmouseup | Executed when mouse button is released |
| onreset | Executed when the form is reset |
| onselect | Executed when the element is selected |
| onsubmit | Executed when the form is submitted |

## AJAX AND CSS

JavaScript can be used with AJAX and CSS.

*   **AJAX:** AJAX is short for **Asynchronous JavaScript** and XML. By updating a segment of the page without the need to reload the entire page, AJAX provides a much faster and easier way to create interactive web applications. It uses XHTML for the content, CSS for the style and presentation, and the Document Object Model and JavaScript for displaying dynamic content. To know more about AJAX, please visit this site:
    [https://developer.mozilla.org/en-US/docs/AJAX/Getting_Started](https://developer.mozilla.org/en-US/docs/AJAX/Getting_Started)
*   **CSS:** CSS stands for **Cascading Style Sheets**. It is a style sheet language that is used to specify how documents written in a markup language are presented to users. With CSS, web developers and designers and users can create style sheets that define how HTML elements such as headers and links are displayed. To get know more about CSS, please visit this site:
    [http://www.echoecho.com/cssintroduction.htm](http://www.echoecho.com/cssintroduction.htm)

## ONLINE RESOURCES

*   **Mozilla Developer Network**

    [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

    Resource for JavaScript documentation for beginners and advanced users. This site contains the official and complete JavaScript reference, including guides, tutorials and articles on JavaScript basics, as well as best practices and design patterns.

*   **Eloquent JavaScript**

    [http://eloquentjavascript.net](http://eloquentjavascript.net)

    A free ebook by programmer and tech writer Marijn Haverbeke. Fundamentals of JavaScript are taught, and includes mini exercises after each chapter. This book covers how JavaScript works in a browser, as well as two chapters on Node.js.

*   **Douglas Crockford’s JavaScript Videos**

    [http://javascript.crockford.com](http://javascript.crockford.com)

    Douglas Crockford is a Yahoo JavaScript programmer and is instrumental in the planning, development and growth of JavaScript. On the website are Crockford’s videos and transcripts on the Yahoo User Interface blog.

*   **WebPlatform.org**

    [http://docs.webplatform.org/wiki/javascript](http://docs.webplatform.org/wiki/javascript)

    This site contains documentations for learning web programming languages such as HTML, CSS, and JavaScript.

*   **Khan Academy**

    [https://www.khanacademy.org/computing/cs](https://www.khanacademy.org/computing/cs)

    A site where users can learn JavaScript to create drawings and animations through screencasts, code games, and create web pages with HTML and CSS.

*   **Tutorials Point**

    [http://www.tutorialspoint.com/javascript/index.htm](http://www.tutorialspoint.com/javascript/index.htm)

    A comprehensive online resource, not only for JavaScript, but also for other technologies, such as SIP, Pay Per Click (PPC), Awk, HBase, XStream, Java8, Guava, Memcached, EasyMock, CICS, Object Oriented Analysis & Design, Tika, DOM, etc.

*   **W3Schools Online Web Tutorials**

    [http://www.w3schools.com/js](http://www.w3schools.com/js)

    Online tutorial, not only for JavaScript but also for HTML, CSS, XML, DOM, jQuery, ASP.NET, PHP, SQL, and others.

*   **Code Combat**

    [https://codecombat.com/](https://codecombat.com/)

    An interactive site to quickly learn programming such as JavaScript or Python. It is a live coding strategy game for beginners.

*   **JS Fiddle**

    [http://jsfiddle.net/](http://jsfiddle.net/)

    A site where users can create, share, execute, and test JavaScript codes right in the browser. This is useful for collaborative debugging or for sharing code snippets. Users can combine JavaScript, HTML, and CSS.

![images/himg-9-1.png](images/00012.jpeg)
**NOTICE AND DISCLAIMER.**

The information contained herein is meant to supplement, but not replace, primary resources. It is not a comprehensive treatment of the subject and is intended for informational purposes only. The publisher, writers and editors: (a) do not guaranty, represent or warrant that any information herein is accurate, complete or current or that anyone who utilizes this publication will achieve certain results as a result of such use; (b) are not responsible for the use or misuse of such information; and (c) expressly disclaim all legal liability (including money damages) arising from the reference to, reliance on or use of this publication. No one may reproduce or transmit any part of this publication - in any form or by any means – without publisher’s prior written permission.

© 2015 Little Green Apples Publishing, LLC