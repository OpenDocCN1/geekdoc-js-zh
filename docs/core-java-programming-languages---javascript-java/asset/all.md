![](image_rsrc2MY.jpg)

# Content

# [Preface](#part0002.xhtml)

# [Chapter 1: Introduction to Core Java](#part0003.xhtml)

# [1.1 Overview of Core Java](#part0004.xhtml)

# [1.2 Java program execution environment](#part0005.xhtml)

# [Chapter 2: Basic elements of Core Java programming](#part0006.xhtml)

# [2.1 Variables and Data types](#part0007.xhtml)

# [2.2 Arithmetic and Logical operators](#part0008.xhtml)

# [2.3 Java libraries](#part0009.xhtml)

# [Chapter 3: Input-output programming in Core Java](#part0010.xhtml)

# [3.1 Input statement](#part0011.xhtml)

# [3.2 Output statement](#part0012.xhtml)

# [3.3 I/O program](#part0013.xhtml)

# [Chapter 4: Decision-making programming in Core Java](#part0014.xhtml)

# [4.1 Decision-making](#part0015.xhtml)

# [4.2 if statement](#part0016.xhtml)

# [4.3 if…else statement](#part0017.xhtml)

# [4.4 Nested if statement](#part0018.xhtml)

# [4.5 else if ladder](#part0019.xhtml)

# [4.6 Switch case statement](#part0020.xhtml)

# [Chapter 5: Looping in Core Java](#part0021.xhtml)

# [5.1 Looping](#part0022.xhtml)

# [5.2 For loop](#part0023.xhtml)

# [5.3 While loop](#part0024.xhtml)

# [5.4 do while loop](#part0025.xhtml)

# [Chapter 6: Array in Core Java](#part0026.xhtml)

# [6.1 Array](#part0027.xhtml)

# [6.2 One-dimensional array](#part0028.xhtml)

# [6.3 Two-dimensional array](#part0029.xhtml)

# [Chapter 7: Methods in Core Java](#part0030.xhtml)

# [7.1 Methods](#part0031.xhtml)

# [7.2](#part0032.xhtml) [](#part0032.xhtml)[Built-in methods](#part0032.xhtml)

# [7.3 User-defined methods](#part0033.xhtml)

# [7.4 Abstract methods](#part0034.xhtml)

# [Chapter 8: Applet in Core Java](#part0035.xhtml)

# [8.1 Applet execution](#part0036.xhtml)

# [8.2 Examples of Applet](#part0037.xhtml)

# [Chapter 9: AWT in Core Java](#part0038.xhtml)

# [9.1 Components of AWT](#part0039.xhtml)

# [9.2 AWT programming](#part0040.xhtml)

# [9.3 Event handling](#part0041.xhtml)

# [Chapter 10: Swing in Core Java](#part0042.xhtml)

# [10.1 Components of Swing](#part0043.xhtml)

# [10.2 Java Swing programming](#part0044.xhtml)

# [Chapter 11: Java data base connectivity](#part0045.xhtml)

# [11.1 Configuration and Connectivity](#part0046.xhtml)

# [11.2 JDBC programming](#part0047.xhtml)

# [Chapter 12: Programming in Core Java](#part0048.xhtml)

Preface

# Core Java is a subset of versatile programming language JAVA which allows the developer to develop windows desktop application as well as mobile application. It is a most popular programming language and best fit for beginners who wants to learn object-oriented programming.

# Core Java Programming is using syntax like C++ which is easy to learn, write and compile. Core Java and C++ both are object-oriented language but C++ is a flavoured object-oriented whereas Core JAVA is a pure object- oriented programming language.

# If one who is not familiar with Core Java, he would not be able to understand advance JAVA. So, if you want mastering in JAVA than Core Java will be your first step. To learn all basics and object-oriented environment.

# This eBook teaches you JAVA application, Applet, Object orientation, as well as data base connectivity Hence it would be an amazing reference for beginners as well as web developers, Android app developers and software developers.

Chapter 1

# Introduction to Core Java

1.1 Overview of Core Java

# Java was developed in Sun Microsystem by James Gosling in early 1990s as a pure object-oriented language. Core Java is considered as subset of Java. Core Java also known as J2SE (Java standard edition). The core component of Java was officially introduced by Sun Microsystem on May, 1995.  Later in 2009 Java merged with Oracle Corporation, nowadays Java is the most popular language among all.

# Coding in Core Java is very clean and easy to understand. It is much faster than other programming language. A compiled Java code can run in any compatible platform. Core Java allows us to dynamically link with new class libraries, methods and objects. Runtime environment of Core Java is Operating Systems like Unix, Windows, Linux, macOS.

# The scope of Core Java is very wide, we can use Core Java for Android app development, corporate solutions, Web development and many more.

# Following are the top ten uses of Core Java: -

# •          Software development

# •          Mobile app development

# •          Web development

# •          Games development

# •          Desktop GUI application development

# •          Artificial Intelligence

# •          Business application

# •          Cloud application

# •          Embedded systems

1.2 Java program execution environment

# ![](image_rsrc2MZ.jpg)

# ![](image_rsrc2N0.jpg)

# ![](image_rsrc2N1.jpg)

# Figure shows the pictorial representation of Java program execution environment. Here JDK (Java development kit) is a software used to execute JAVA application program. It is divided in two parts- JAVAC (Java compiler) & JRE (Java runtime environment). The JAVAC translates the incoming source code to object code known as Byte code. Object code file will be transferred to JVM (Java virtual machine) which depends on JRE (Java runtime environment) such as Windows, Linux, Unix, MacOS etc. So we call Java as platform independent language. Finally, output will be generated by JVM with the help of JRE.

# A programmer must set the path from command prompt then compile and execute the program using commands given below.

# 1\. Command to set class path

# Go to command prompt →type and press enter

# (Set path = c:\ program files\ java\ jdk1.8\ bin)

# 2\. Command for compilation

# javac filename.java (press enter)

# 3\. Command for execution

# java filename (press enter)

# Note: A programmer can also use the several Development environments such as BlueJ, Apache, NetBeans IDE 8.0.2 to execute Java application program.

Chapter 2

# Basic elements of Core Java programming

2.1 Variables and Datatypes

# Variable is an entity to store data during program execution. Java allows us to use alphabetic, alphanumeric, words as a variable.

# Example

# Alphabetic – a- z

# Alphanumeric – a1, b1, c1

# Words – num, result

# Note: We must use lowercase at beginning of any variable because JAVA is a case sensitive language.

# Data is a raw fact and figure used in a program. There are five types of data used in Java programming known as Data types.

# 1\. Integer: A number without decimals known as Integer. Java uses shortcut “int” to declare integer variables.

# Example

# int a=5, b1, result;

# Note: We use “int” for 4 bytes number and “long” for 8 bytes number.  

# 2\. Float: A number with decimals known as float. Java uses shortcut “float” to declare integer variables.

# Example

# float b=3.145, c1, result;

# Note: We use “float” for 4 bytes number and “double” for 8 bytes number. 

# 3\. Character: All keyboard characters are considered as character in programming. Java uses shortcut “char” to declare character variables. We must use single quote ‘ ‘ to store a character.

# Example

# char myChar = ‘c’;

# 4\. String: A sequence of character known as String. Java uses shortcut “string” to declare character variables. We have to use double quotes “ “ to store a string.

# Example

# string txt = “John”;

# 5\. Boolean: It stores either true or false values. Java uses shortcut “Boolean” to declare Boolean variables.

# Example

# char myNum = true;

# Note: Any statement in a Java program can be closed by semicolon (;).

2.2 Arithmetic and logical operator

# Arithmetic operators allow us to do the common mathematical operations.

# There are seven types of arithmetic operators used in Java programming.

# 1\. Addition (+) – To add two values, For example (a + b)

# 2\. Subtraction (-) – To subtract a value from another, For example (a – b)

# 3\. Multiplication (*) – To multiply two values, For example (a * b)

# 4\. Division (/) – It returns the division remainder, For example (a / b)

# 5\. Modulus (%) – It returns the remainder of division, For example (a % b)

# 6\. Increment (++) - It increases the variable’s value by 1, For example (a++)

# 7\. Decrement (--) – It decreases the variable’s value by 1, For example (b--)

# Pre and Post operators – If we use the operator after variable known as post operator and if we use before the variable known as pre operator.

# Example

# a++       =>      a= a+1      => a+=1 ​=> ++a

# Logical operators allow us to determine the logic between two variables.

# There are eight types of logical operators used in Java programming

# 1\. Greater than (>) – For example x is greater than y (x > y)

# 2\. Less than (<) – For example x is less than y (x < y)

# 3\. Not equal (!=) - For example x is not equal to y (x != y)

# 4\. Equal to (==) – For example x is equal to y (x == y)

# 5\. Greater than or equal to (>=) – For example x is greater than or equal to y (x>=y)

# 6\. Logical and (&&) – For example (x < 2 && x < 8) if both statements are true, it returns true else false.

# 7\. Logical or (||) – For example (x < 7 || x < 9) if any one of statement is true , it returns true.

# 8\. Logical not (!) – For example !( x< 2 && x < 4) it returns false if result is true.

2.3 Java Libraries

# There are many libraries used in Java program but some of them are commonly used by JVM during run time for program execution. A programmer must be aware of commonly used library.

# Following are the commonly used libraries in Core Java programming

# 1\. import java.util.*;

# 2\. import java.awt.*;

# 3\. import java.awt.event.*;

# 4\. import java.io.*;

# 5.  import java.lang.*;

# 6\. import javax.swing.*;

Chapter 3

# Input-Output Programming in Core Java

3.1 Input statement

# A process of inserting data in program known as input statement. Almost all programming language uses the input statement to insert data. Being an object-oriented programming language Java considers input as an object. We can use one or more input statements according to requirements in a program. A programmer must add the input-output library to program before using input statements. Let us see the rules of writing input statement in JAVA.

# Syntax:

# Scanner var = new Scanner(System.in);

# Input variable = var.nextInt(); // for integer input

# var.close();

# Implementation:

# Scanner a = new Scanner(System.in); // import java.util.scanner; in order to execute 

# number = a.nextInt();

# a.close();

# Note: We can use nextFloat() method to input real number.

3.2 Output statement

# A process of getting result from the program known as Output statement. We can use one or more output statements according to requirements in a program. Let us see the rules of writing output statement in JAVA.

# Syntax: System.out.println (“string” + var); //variables can be added after or before string

# Implementation: System.out.println (“The result is “+ c); 

# If we write “println” cursor moves to next line after printing and if we write “print” cursor remains in same line.

# Note: The value of c will be displayed along with given string.

# Let us write a program in Java to display the given text on output.

| Program to Display the given string | Output |
|  
# public class Main

# {

# public static void main(String[] args)

# {

# System.out.println("Hi!, Welcome to Core Java");

# }

# }

 | Hi!, Welcome to Core Java |

3.3 I/O program

# A program which uses both input and output statements known as I/O program. Let us see some examples of I/O programming in Java.

# Example: Write a program to add two numbers using input statement.

| Java program to add two numbers | Output |
|  
# import java.util.Scanner;

# public class InputOutput {

# public static void main(String[] args)

# {

# int a, b, result;

# Scanner sc = new Scanner(System.in);

# a = sc.nextInt();

# b = sc.nextInt();

# sc.close();

# result = a + b;

# System.out.println("Sum of given two numbers: "+result);   

# }

# }

 |  
# 2

# 3

# Sum of given two numbers: 5

# Note: Here 2 and 3 are user inputs.

 |

# Example: Write a program in Java to perform all arithmetic operation using input statement.

| Java program to perform all arithmetic | Output |
|  
# import java.util.Scanner;

# public class InputOutput {

# public static void main(String[] args)

# {

# int a, b, add, sub, mul, div, mod;

# Scanner sc = new Scanner(System.in);

# a = sc.nextInt();

# b = sc.nextInt();

# sc.close();

# add = a + b;

# sub = a - b;

# mul = a * b;

# div = a / b;

# mod = a % b;

# System.out.println("Addition= "+add);

# System.out.println("Subtraction= "+sub);

# System.out.println("Multiplication= "+mul);

# System.out.println("Division= "+div);

# System.out.println("Remainder= "+mod);   

# }

# }

 |  
# 6

# 2

# Addition= 8

# Subtraction= 4

# Multiplication= 12

# Division= 3

# Remainder= 0

# Note: Here 6 and 2 are user inputs.

 |

# Note: If we write input statements in program than user can enter or test any data.

Chapter 4

# Decision-making Programming in Core Java

4.1 Decision-making

# Decision-making statements in a program gives us choices by identifying a decision and accessing the resolution. An evaluated result of Boolean value true or false will be produced by program as output. Most of the programming language uses decision-making statements.

# Following are the decision-making statements used in Core Java

# 1\. if statements

# 2\. if…else statement

# 3\. Nested if statement

# 4\. else if ladder

# 5\. switch-case statement

4.2 if statement

# A block of statement is executed if the condition is true known as “if statement”.

# Syntax:

# if (condition)

# ​true statement;

# Implementation:

# If(a>b)

# ​System.out.println(“a is larger than b”);

# Note: We can make any condition using logical operator.

# Example:

| Java program to check the value of variables using “if statement” | Output |
|  
# public class DecisionMaking

# {

# public static void main(String[] args)

# {

# int a=5, b=5;

# if(a==b)

# System.out.println("Both are equal");

# }   

# }

 | Both are equal |

4.3 if…else statement

# If the condition is true than a block of true statement will be executed and if the condition is false than a block of else statement will be executed known as “if…else” statement.

# Syntax:

# if (condition)

# ​true statement;

# else

# ​false statement;

# Implementation:

# If(a>b)

# ​System.out.println(“a is larger than b”);

# else

# ​System.out.println(“b is larger than a”);

# Example:

| Java program to find even or odd using if..else statement | Output |
|  
# public class DecisionMaking

# {

# public static void main(String[] args)

# {

# int n=8;  

# if(n%2==0)

# System.out.println("Given number is even");

# else

# System.out.println("Given number is odd");

# }

# }

 | Given number is even |

4.4 Nested if statement

# If we use another if statement in if..else than it is known as “ Nested if statement”.

# Syntax:

# if (condition)

# if (condition)

# true statement;

# else

# ​false statement;

# Let us implement the syntax in Java programming

# Example:

| Java program to find the number is between 1 to 10 using nested if statement. | Output |
|  
# public class DecisionMaking

# {

# public static void main(String[] args)

# {

# int n=9;

# if(n<=10)

# if(n>=1)

# System.out.println("Given number is between 1 to 10");        

# else

# System.out.println("Given number is not between 1 to 10");        

# }  

# }

 | Given number is between 1 to 10 |

# Note: Here if both the conditions are true than only true statement will be executed, else false statement.

4.5 else if ladder

# If we have two or more decisions than we can use else if ladder to interpret all.

# Syntax

# If(condition)

# ​statement 1;

# elseif(condition)

# ​statement 2;

# elseif(condition)

# ​statement 3;

# …………………..

# …………………..

# else

# ​statement n;

# Example:

| Java program to compute largest among three numbers using else if ladder. | Output |
|  
# public class DecisionMaking

# {

# public static void main(String[] args)

# {

# int a=10, b=30, c=20;

# if (a>=b && a>=c) 

# System.out.println(a+" is the largest Number"); 

# else if (b>=a && b>=c) 

# System.out.println(b+" is the largest Number"); 

# else

# System.out.println(c+" is the largest number");           

# }  

# }

 | 30 is the largest number |

4.6 switch-case statement

# If we want to select one of many block of code than we can use switch-case statement.

# Syntax

# switch(expression)

# {

# case 1:

# // block of code

# break;

# case 2:

# // block of code

# break;

# …………………….

# …………………….

# default:

# // block of code

# }

# Let us see how it is implemented in Java programming. A programmer is allowed to consider as many cases as required.

# This program performs the case testing, as soon as the match is found code execution is terminated using break keyword.

# Example: A program in Java to convert the given number in words using switch case statement.

| Java code to convert number to word | Output |
|  
# public class DecisionMaking

# {

# public static void main(String[] args)

# {

# int num = 3; // User can write any number from 1-5

# switch (num)

# {

# case 1:

# System.out.println("One");

# break;

# case 2:

# System.out.println("Two");

# break;

# case 3:

# System.out.println("Three");

# break;

# case 4:

# System.out.println("Four");

# break;

# case 5:

# System.out.println("Five");

# break;

# }         

# }  

# }

 | Three |

# Note: We have given only five cases so user can initialise and check the number (1-5).

Chapter 5

# Looping in Core Java

5.1 Looping

# A code segment is executed again and again until the given condition is true known as looping. We can apply looping only in sequential items. Almost all programming language uses looping. It gives us facility to handle huge sequential data.

# There are three types of looping used in Core Java

# 1\. for loop

# 2\. while loop

# 3\. do while loop

5.2 for loop

# A specific block of code is executed until the given condition is met.

# Syntax

# for (Initialisation; condition; inc or dec)

# {

# //Segment of code

# …………

# ………….

# }

# Let us make a “for loop” for sequential number 1 to 10\. First, we take a loop variable (int i;). In initialisation section first number must be initialised (i=1). Next, we must make a “Condition” so that entire number (1-10) get covered (i<=10). Since the numbers (1-10) is in incrementing order so in (inc or dec) section we write (i=i+1). Finally, we get for loop as shown below.

# for (i=1; i<=10; i=i+1)

# Now let us write a program in Java to display the table of 2 using for loop.

# Example

| Java code for table of 2 using for loop | Output |
|  
# public class Looping

# {  

# public static void main(String[] args)

# {

# int i;

# for (i=2; i<=20; i=i+2)

# {

# System.out.println( i );

# }

# }  

# }

 |  
# 2

# 4

# 6

# 8

# 10

# 12

# 14

# 16

# 18

# 20

 |

# Nested for loop

# If we use another for loop inside the for loop known as nested for loop. A user must be aware that during execution upper for loop is once executed than lower for loop will complete entire iteration.

# Example

# for(i = 1; i >= 3; i++)

# {

# for(j = 1; j >= 3; j++)

# {

# }

# }

# Note: Nested for loops are used for two-dimensional array and many more applications.

5.3 while loop

# A set of given instruction is executed while the Boolean condition is met.

# Syntax

# while(condition)

# {

# …………

# //Segment of code

# …………

# }

# Let us make a “while loop” for sequential number 1 to 10\. First, we take a loop variable (int i=1;) in variable declaration section. Next, we must make a “Condition” so that entire number (1-10) get covered (i<=10). Since the numbers (1-10) is in incrementing order so in (inc or dec) section we write (i=i+1). Finally, we get while loop as shown below.

# Int i=1;

# while(i<=10)

# {

# i = i+1;

# }

# Let us write a program in Java for table of 5 using while loop.

# Example

| Java code for table of 5 using while loop | Output |
|  
# public class Looping

# {  

# public static void main(String[] args)

# {

# int i=5;

# while(i<=50)

# {

# System.out.println(i);

# i=i+5;

# }

# }

# }

 |  
# 5

# 10

# 15

# 20

# 25

# 30

# 35

# 40

# 45

# 50

 |

5.4 do while loop

# A set of statements are executed at least once, even if the condition is not met.

# Syntax

# do

# {

# ………..

# Segment of code

# ………..

# } while(condition);

# Let us make a “do loop” for sequential number 1 to 10\. First, we take a loop variable (int i=1;) in variable declaration section. Next, we must make a “Condition” so that entire number (1-10) get covered (i<=10). Since the numbers (1-10) is in incrementing order so in (inc or dec) section we write (i=i+1). Finally, we get do loop as shown below.

# do

# {

# i = i + 1;

# }while(i<=10);

# Example

| Java code for table of 7 using do while loop | Output |
|  
# public class Looping {  

# public static void main(String[] args) {

# int i=7;

# do

# {

# System.out.println(i);

# i=i+7;

# } while(i<=70);

# }  

# }

 |  
# 7

# 14

# 21

# 28

# 35

# 42

# 49

# 56

# 63

# 70

 |

Chapter 6

# Array in Core Java

6.1 Array

# A group of elements sharing the common name such that each element is identified by its position known as Array. It is used to handle both sequential or nonsequential items. An array is a type of object in Java which is also known as a container object. Java provides dynamic allocation facility for Array.

# Example:

# num

# num[0]​​10

# num[1]​​30

# num[2]​​40

# num[3]​​60

# Here, name of the array is “num”, each and every element is identified by its position so element 60 is in position 3, as we start with 0.

# Note: We have used one-dimensional array in example.

# There are three types of arrays in Java:

# 1\. One-dimensional array

# 2\. Two-dimensional array

# 3\. Multidimensional array

6.2 One-dimensional array

# A group of elements stored in a single line known as One-dimensional array. Syntax for declaration of an array is shown below.

# Syntax:

# Data type name of array[ ] = { element 1,element 2……….., element n};

# Implementation:

# int array[ ] = {10,30,50,60};

# Let us create an array, there are four elements which is stored in position (0-3) so we must use looping for position (0-3) and merge array elements with each and every position.

# Example

| Java code to display the elements of given array | Output |
|  
# public class Array {

# public static void main(String[] args)

# {

# int num[]={10,20,30,40,50};

# int i;

# for(i=0; i<=4; i++)

# {

# System.out.println(num[i]);

# }

# }

# }

 |  
# 10

# 20

# 30

# 40

# 50

 |

# Example

| Java code to reverse the element of given array | Output |
|  
# public class Array

# {

# public static void main(String[] args)

# {

# int num[]={10,20,30,40,50};

# int i;

# for(i=4; i>=0; i--)

# {

# System.out.println(num[i]);

# }

# }

# }

 |  
# 50

# 40

# 30

# 20

# 10

 |

# Note: To reverse the element of an array, we must make a loop in decrementing order and merge array elements

# Now let us see how to handle more than one dimensions of array in Java programming. An array with more than two dimensions are not easy to visualize but applications are only increasing by the day. They can also hold large amounts of data, which is a useful feature when it comes to data analysis.

# We are going to discuss about two-dimensional array.

6.3 Two-dimensional array

# A group of elements stored in rows and columns known as Two-dimensional array. They form a matrix of rows and columns. Syntax for declaration of an array is shown below.

# Syntax:

# Data type name of array [ ] [ ] = { {row 1}, {row2}……….., {row n}};

# Implementation:

# int mat [ ] [ ] = {{1,3,6}, {2,7,3}, {4,5,8}};

# Note: We have used 3X3 matrix to declare two-dimensional array.

# If we want to display the elements of two-dimensional array than we got to make “nested for loop” and merge the elements of an array. Let us implement the logic in Java programming.

# Example:

| Java code to display the element of given two-dimensional array | Output |
|  
# public class Array {

# public static void main(String[] args)

# {

# int mat [ ][ ]={{1,3,6}, {2,7,3}, {4,5,8}};

# int i, j;

# for (i=0; i<=2; i++)

# {

# for (j=0; j<=2; j++)

# {

# System.out.print(mat[i][j]);

# }

# System.out.println("");

# }

# }  

# }

 |  
# 1 3 6

# 2 7 3

# 4 5 8

 |

Chapter 7

# Methods in Core Java

7.1 Methods

# A block of code used for specific action is known as methods in Java programming. In other programming language such as c, c++ we call it function.

# There are three types of method used in Java programming:

# 1\. Built-in methods

# 2\. User-defined methods

# 3\. Abstract methods

7.2 Built-in methods

# A method built by a language developer for specific language known as built-in method. A programmer can import the specific package and use the built-in method at any point of the program. Java built-in methods are used with string, number, character, and array.

# Let us use one of the built-in methods in Java programming.

| Java program to change the given string to uppercase and lowercase using built-in method | Output |
|  
# public class Method

# {

# public static void main(String[ ] args)

# {

# String txt = "John";

# System.out.println(txt.toUpperCase());

# System.out.println(txt.toLowerCase());

# }

# }

 |  
# JOHN

# john

 |

7.3 User defined methods

# A block of code created by user or programmer for specific purpose known as user-defined method. A user-defined method can be called at any point of the program.

# Example

| Java code to add two numbers using user-defined method | Output |
|  
# class Method {

# // create a user-defined method

# public int addNumbers(int a, int b)

# {

# int sum = a + b;

# return sum;    // return value to main

# }

# public static void main(String[ ] args)

# {

# int num1 = 20;

# int num2 = 10;

# // create an object of Method

# Method obj = new Method();

# // calling user-defined method

# int result = obj.addNumbers(num1, num2);

# System.out.println("Sum is: " + result);

# }

# }

 | Sum is: 30 |

# Note: Above program passes two parameters (num1, num2) to user-defined method(addNumbers) to calculate sum of two numbers. The user defined method returns the result as argument.

7.4 Abstract methods

# A method without body or implementation is called abstract method. This type of method hides the details from user and focuses on action. It is declared through keyword “abstract”.

| Java code using abstract method to multiply two and three given numbers |
|  
# abstract class Multiply {   

# public abstract int MultiplyTwoNum (int n1, int n2); 

# public abstract int MultiplyThreeNum (int n1, int n2, int n3);  

# public void show() {

# System.out.println ("Method of abstract class Multiply");

# }

# }

# // Regular class extends abstract class 

# class AbstractMethod extends Multiply { 

# public int MultiplyTwoNum (int num1, int num2) { 

# return num1 * num2;

# }

# public int MultiplyThreeNum (int num1, int num2, int num3) { 

# return num1 * num2 * num3;

# }

# public static void main (String[] args)

# {

# Multiply obj = new AbstractMethod();

# System.out.println ("Multiplication of two numbers: " + obj.MultiplyTwoNum (10, 40)); 

# System.out.println ("Multiplication of three numbers: " + obj.MultiplyThreeNum (5, 10, 100)); 

# obj.show();

# }

# }

 |

# Output:​Multiplication of two numbers: 400

# Multiplication of three numbers: 500

# Method of abstract class Multiply

Chapter 8

# Applet in Core Java

# Applet in Java makes it more powerful language. In this the output of program will be integrated into a webpage. A programmer writes a Java application program and saves in a (.java) file after than a HTML file is created which contains an Applet tag to call the (.class) file. Finally, the output will be displayed on existing browser or appletviewer. So, Applets are hosted on a Web server. Every applet will run quickly and reliably without demanding a lot of system resources.  It functions as a front-end in web computer.

# Following are the lifecycle of Applet.

# 1\. init() : This is where we initialize the variable. It will be called once during the applet runtime.

# 2\. start() :  This method is called after ini(). This technique is called to restart an applet.

# 3\. stop() : It is called to suspend threads that do not need to operate.

# 4\. destroy() :It is called if you need to remove your applet from memory.

8.1 Applet execution

# First, we must write an application program for specific purpose and save it in (.java) file. Let us write a program to display “Welcome to Applet world” in Notepad of Windows and save it in demo.java file. We must import Applet and AWS in application program. Here we have used method (Graphics g).

# import java.applet.*;

# import java.awt.*;

# public class demo extends Applet

# {

# public void paint(Graphics g)

# {

# g.drawString("Welcome to Applet world",100,100);

# }

# Note: demo.java file must be shifted to the proper location before compilation. Copy the file, go to C:\ => Program files => Java =>jdk1.8.0 => bin and paste the file.

# Now we must create HTML file (any.html) which calls (demo.class) to display the string on Web page. Save it in the same location where demo.java file is saved.

# Let us write HTML tag.

# <html>

# <body>

# <applet code="demo.class" width=400 height=400>

# </applet>

# </body>

# </html>

# Compile and run the existing program. Go to command prompt as an administrator. Change the directory and compile using javac.

# c:\program files\java\jdk1.8.0\bin\javac demo.java (press enter)

# c:\program files\java\jdk1.8.0\bin\appletviewer any.html (press enter)

# Here as soon as we compile demo.java, another file(demo.class) will be automatically created and stored in bin. Hereafter appletviewer will call the class to display the string as shown below.

# ![](image_rsrc2N2.jpg)

8.2 Examples of Applet

# 1\. Write an applet program to display the today’s date.

# import java.applet.*;//to access showStatus()

# import java.awt.*;//Graphic class is available in this package

# import java.util.Date;//to access Date object

# public class demo2 extends Applet

# {

# public void paint(Graphics g)

# {

# Date d = new Date();

# showStatus("Today is" + d);

# }

# }

# HTML tag for demo2.class

# <html>

# <body>

# <applet code="demo2.class" align="right" height="200" width="300">

# </applet>

# </body>

# </html>  Output

# ![](image_rsrc2N3.jpg)

# 2\. Applet program to draw a rectangle of given size.

# import java.applet.*;

# import java.awt.*;

# public class demo3 extends Applet

# {

# int height, width;

# public void init()

# {

# height = getSize().height;

# width = getSize().width;

# setName("MyApplet");

# }

# public void paint(Graphics g)

# {

# g.drawRoundRect(10, 30, 120, 120, 2, 3);

# }

# }

# HTML tag for demo3.class

# <html>

# <body>

# <applet code="demo3.class" width=400 height=400>

# </applet>

# </body>

# </html>

# Output

![](image_rsrc2N4.jpg)

Chapter 9

# AWT in Core Java

# AWT (Abstract Window Toolkit) is an application program which contains a rich sets of Java libraries to create a GUI (Graphical User Interface). The components of AWT allows us to develop windows-based applications. We can create an Event, draw shapes, insert images using AWT GUI programming. AWT components are platform-dependent.

9.1 Components of AWT

# In this section we will discuss about the different components used in AWT. We can see all these components while operating windows or web surfing. Components are used as an object in Java GUI programming.

# Following are the list of components used in AWT.

# 1\. Button – It is a class to create a labelled button. AWT gives us facility to include action to button.

# 2\. Label – It is an object for placing text in to a container.

# 3\. Check Box – It is a graphical component having two states either on(true) or off(false).

# 4\. Check Box Group – A set of checkboxes.

# 5\. List – It is a component which contains a list of scrolling text items.

# 6\. Text Field – It allows us to edit single line of text.

# 7\. Text Area – It allows us to edit multiple line of text.

# 8\. Choices – It is a pop-up menu of choices where selected choice will be shown on the top.

# 9\. Canvas – It is an area to draw something.

# 10\. Image – It represents graphical image.

# 11\. Scroll Bar- It allows user to select the range of values.

# 12\. Dialog Box – The user can insert some form of input.

# 13\. File Dialog – The user can select a particular file.

9.2 AWT Programming

# Let us create some of the components in a single application program using AWT rich libraries. We must import java.awt library to access all facilities. To inherit all the methods and fields of parent class we must extend the user created class.

# For example: public class Myclass extends Frame

# All the components are initialized as well as created within user class  for e.g. Myclass().

# A programmer must create the components, set size and position in Frame or Container, and add the created components to the frame.

# Let us create a component (Button)

# Syntax: Component var = new Component(“Label”);

# Implementation: Button b = new Button("Click me");  

# Now, set size and position of Component (Button)

# Syntax: component’s variable.setBounds(x-coordinate, y-coordinate, width, height);

# Implementation: b.setBounds(70,140,50,20);    

# We must add the component (Button) to frame

# Syntax: add(Component’s variable);

# Implementation: add(b);

# Following are the essential instructions for a programmer to use during components creation.

# 1\. setSize(height, width) – To set the size of a frame or container.

# 2\. setTitle(“Title of Frame”) – To set the title of the frame according to environment.

# 3\. setLayout(null) – If layout not required than programmer must set it to null. If we need Layout in any other application than this instruction is avoided.

# 4\. setVisible(true) – Visibility must be set to true.

# While keeping in mind aforementioned all discussion, let us create some components of AWT.

# 1\. AWT program to create and display button, label and Text field.

# import java.awt.*;

# public class Component extends Frame {

# Component() {

# // creating a button, label, text field  

# Button b = new Button("Submit");  

# Label l = new Label("Employee");

# TextField t = new TextField();

# // set size and position in container

# b.setBounds(70,140,50,20);    

# l.setBounds(60, 70, 60, 30);

# t.setBounds(40, 100, 80, 30);

# // add the components to container

# add(b);    

# add(l);

# add(t);   

# setSize(300,300);  

# setTitle("Label, text field and button");   

# setLayout(null);    

# setVisible(true);

# }    

# public static void main(String args[]) {    

# Component f = new Component();   

# }

# }    Output

# ![](image_rsrc2N5.jpg)

# 2\. AWT program to create and display multiple check Box, any one must be selected.

# import java.awt.*;

# public class Component {

# Component() {

# // creating the frame with the title

# Frame f = new Frame("Checkbox Example");   

# // creating the checkboxes 

# Checkbox checkbox1 = new Checkbox("JavaScript");   

# checkbox1.setBounds(100, 100, 80, 80);   

# Checkbox checkbox2 = new Checkbox("CoreJava", true);   

# checkbox2.setBounds(100, 150, 80, 80);   

# // adding checkboxes to frame 

# f.add(checkbox1);   

# f.add(checkbox2);     

# f.setSize(400,400);   

# f.setLayout(null);   

# f.setVisible(true);   

# }   

# public static void main(String args[]) {    

# new Component();   

# }   

# }       Output

![](image_rsrc2N6.jpg)

# 3\. AWT program to create and display Choice menu of fruits.

# import java.awt.*;

# public class Component {

# Component() {

# Frame f = new Frame();     

# // creating a choice component

# Choice c = new Choice();  

# c.setBounds(100, 100, 75, 75);     

# // adding items to the choice menu

# c.add("Apple");   

# c.add("Banana");   

# c.add("Orange");   

# c.add("Grapes");   

# c.add("Mango");     

# f.add(c);     

# f.setSize(400, 400);   

# f.setLayout(null);   

# f.setVisible(true);   

# }   

# public static void main(String args[]) {    

# new Component();     

# }   

# }    Output

![](image_rsrc2N7.jpg)

# 4\. AWT program to create and display the List of fruits with scrolling facility.

# import java.awt.*;

# public class Component {

# Component() {

# Frame f = new Frame();  

# // creating the list of 5 rows  

# List l1 = new List(5);     

# l1.setBounds(100, 100, 75, 75);    

# // adding list items into the list

# l1.add("Apple");   

# l1.add("Banana");   

# l1.add("Orange");   

# l1.add("Grapes");   

# l1.add("Mango");     

# f.add(l1);     

# f.setSize(400, 400);   

# f.setLayout(null);   

# f.setVisible(true);   

# }   

# public static void main(String args[]) {    

# new Component();     

# }   

# }   Output

![](image_rsrc2N8.jpg)

9.3 Event handling

# A group of Object interacting with each other known as event, Java gives us facility to handle the event. A mechanism to control the event and decide what should happen known as Event handling. Each and every component of AWT are treated as an object.

# Let us create an event, when a user clicks on button, text field will display “Welcome to Core Java.”

# import java.awt.*;

# import java.awt.event.*;

# public class Component extends Frame implements ActionListener {

# TextField tf;

# Component(){

# tf=new TextField();  //create components

# tf.setBounds(60,50,170,20);

# Button b=new Button("click me"); 

# b.setBounds(100,120,80,30);   

# //register listener

# b.addActionListener(this);//passing current instance

# add(b);add(tf);

# setSize(300,300);

# setLayout(null);

# setVisible(true);

# }

# public void actionPerformed(ActionEvent e){ 

# tf.setText("Welcome to Core Java"); 

# }

# public static void main(String args[]){ 

# new Component();

# }

# }

# Output

# ![](image_rsrc2N9.jpg)

# Output after clicking the button.

# ![](image_rsrc2NA.jpg)

Chapter 10

# Swing in Core Java

# Java swing is a sophisticated toolkit for creating desktop applications. Swing is more sophisticated than AWT. It uses rich set of components. We can easily develop lightweight desktop applications using Java Swing.  The package of Java Swing provides more component than AWT such as Combo Box, Spinner, Slider and many more.

10.1 Components of Swing

# Swing components are basic building block for developing windows-based application.  It gives us much-improved functionality over AWT.

# Following are the components used in Java Swing:

# 1\. JButton - The ‘JButton’ class creates a labeled button..

# 2\. JColorChooser - It offers a pane of controls that enable the user to manipulate and select a color.

# 3\. JcheckBox - It is a GUI component that can be in either an on-(true) or off-(false) state.

# 4\. JRadioButton - It can be in either an on-(true) or off-(false) state. in the group

# 5\. JList – This class provides the user with the scrolling list of text items.

# 6\. JComboBox – This component presents the user with a pop up menu of list or choices.

# 7\. JTextField - It is a text component that allows to edit single line of text.

# 8\. JpasswordField - It is a text component used for password entry.

# 9\. JTextArea - It is a text component that allows the editing of multiple lines of text.

# 10\. Imagelcon – It paints Icons from Images.

# 11\. JScrollbar - It represents a scroll bar component that enables users to select from range values.

# 12\. JOptionPane - It provides a set of standard dialog boxes that prompt users for a value.

# 13\. JFileChooser - It represents a dialog window that allows the user can select a file.

# 14\. JProgressBar - It displays the tasks percentage upon completion.

# 15\. JSlider – The user can select a value by sliding a knob within a defined interval.

# 16\. JSpinner – It is a single-line input field that allows the user to select a number or an object value from an ordered sequence.

10.2 Java Swing programming

# Let us create some sophisticated components using Java swing libraries. We must import javax.swing. Next create a user class For e.g. public class Myclass. We can use entire methods within “public static void main(String args[])” block.

# A programmer must create the frame than create components, set size and position in Frame or Container, and add the created components to frame.

# Let us create a frame

# Syntax: JFrame var = new JFrame(“Title of frame”);

# Implementation: JFrame f = new JFrame(“My frame”);

# Create a component (Button)

# Syntax: Component var = new Component(“Label”);

# Implementation: JButton b = new JButton("Click me");  

# Now, set size and position of Component (Button)

# Syntax: component’s variable.setBounds(x-coordinate, y-coordinate, width, height);

# Implementation: b.setBounds(70,140,50,20);    

# We must add the component (Button) to frame

# Syntax: frame variable.add(Component’s variable);

# Implementation: f.add(b);

# While keeping in mind aforementioned all discussion, let us create some components of Java Swing.

# 1\. Java Swing program to create and display button, label and Text field.

# import javax.swing.*;

# public class Component {

# public static void main(String args[]) {       

# JFrame f=new JFrame("Java Swing components"); 

# // creating a button, label, text field  

# JButton b = new JButton("Submit");  

# JLabel l = new JLabel("Student's name");

# JTextField t = new JTextField();

# b.setBounds(20,120,95,30);    

# l.setBounds(30, 80, 100, 30);

# t.setBounds(10, 60, 150, 30);

# // adding all created components to frame     

# f.add(b);    

# f.add(l);

# f.add(t);   

# f.setSize(400,400);    

# f.setLayout(null);    

# f.setVisible(true);    

# }

# } Output

# ![](image_rsrc2NB.jpg)

# 2\. Java swing program to create and display Radio buttons of Male and Female

# import javax.swing.*;

# public class Component {

# public static void main(String args[]) {   

# JFrame f=new JFrame("Java Swing components"); 

# JRadioButton r1=new JRadioButton("Male");   

# JRadioButton r2=new JRadioButton("Female");   

# r1.setBounds(75,50,100,30);   

# r2.setBounds(75,100,100,30);   

# ButtonGroup bg=new ButtonGroup();   

# bg.add(r1);bg.add(r2);   

# f.add(r1);f.add(r2);     

# f.setSize(300,300);   

# f.setLayout(null);   

# f.setVisible(true);   

# }

# }

# Output

# ![](image_rsrc2NC.jpg)

# 3\. Java swing program to create and display Combo Box of country.

# import javax.swing.*;

# public class Component {

# public static void main(String args[]) {   

# JFrame f=new JFrame("Java Swing components"); 

# String country[]={"India","Aust","U.S.A","Newzealand"};       

# JComboBox cb=new JComboBox(country);   

# cb.setBounds(50, 50,90,20);   

# f.add(cb);       

# f.setLayout(null);   

# f.setSize(400,500);   

# f.setVisible(true);    

# }

# }

# Output

# ![](image_rsrc2ND.jpg)

# 4\. Java swing program to create and display the Option Pane with given string.

# import javax.swing.*;

# public class Component {

# public static void main(String args[]) {       

# JFrame f=new JFrame("Java Swing components"); 

# JOptionPane.showMessageDialog(f,"Hello, Welcome to Core Java");  

# }

# }

# Output

# ![](image_rsrc2NE.jpg)

# 5\. Java Swing program to create and display the password field.

# import javax.swing.*;

# public class Component {

# public static void main(String args[]) {         

# JFrame f=new JFrame("Java Swing components"); 

# JPasswordField value = new JPasswordField();  

# JLabel l1=new JLabel("Password:");   

# l1.setBounds(20,100, 80,30);   

# value.setBounds(100,100,100,30);   

# f.add(value);  f.add(l1);

# f.setSize(300,300);   f.setLayout(null);  f.setVisible(true);    

# }  } Output

# ![](image_rsrc2NF.jpg)

# 6\. A program to create and display the calculator which performs addition and substation using Java Swing components and AWT features.

# import javax.swing.*;

# import java.awt.event.*;

# public class Component implements ActionListener{ 

# JTextField tf1,tf2,tf3;

# JButton b1,b2;

# Component(){

# JFrame f= new JFrame();

# tf1=new JTextField();

# tf1.setBounds(50,50,150,20);

# tf2=new JTextField();

# tf2.setBounds(50,100,150,20);

# tf3=new JTextField();

# tf3.setBounds(50,150,150,20);

# tf3.setEditable(false);  

# b1=new JButton("Add");

# b1.setBounds(50,200,50,50);

# b2=new JButton("Sub");

# b2.setBounds(120,200,50,50);

# b1.addActionListener(this);

# b2.addActionListener(this);

# f.add(tf1);f.add(tf2);f.add(tf3);f.add(b1);f.add(b2);

# f.setSize(300,300);

# f.setLayout(null);

# f.setVisible(true);

# }        

# public void actionPerformed(ActionEvent e) {

# String s1=tf1.getText();

# String s2=tf2.getText();

# int a=Integer.parseInt(s1);

# int b=Integer.parseInt(s2);

# int c=0;

# if(e.getSource()==b1){

# c=a+b;

# }else if(e.getSource()==b2){

# c=a-b;

# }

# String result=String.valueOf(c);

# tf3.setText(result);

# }

# public static void main(String[] args) { 

# new Component();

# } }

# ![](image_rsrc2NG.jpg)

Chapter 11

# Java Data Base Connectivity

# JDBC is an application program which creates an environment for a client to access the backend data base. JDBC is a part of Java Standard Edition of Oracle Corporation. JDBC gives us facility to create, Configure and link the database. If we want to create an environment, first we must make a table of database in Excel or using MySQL, next we got to write an application program using swing, AWT or Java code for front end client to interact with data base, so we must link data base file to application program file.

11.1 Configuration and Connectivity

# In this section we will discuss about how to create DSN (Data source name) and link the program to data base. A user must be aware of all these before writing an application program. Let us take an example of Microsoft Excel database.

# Following are the steps to create a DSN as well as linking

# Step 1: Create an Excel sheet

# Step2: Go to Administrative tools either through proper path or control panel and select ODBC (Oracle data base connectivity).

# Step3: Select user DSN or System DSN and click on Add tab and add the (.xls) file, click next.

# Step 4: Select “Driver do Microsoft Excel(.xls)”.

# Step 5: Give the Data Source name as in (.xls) created file.

# Step 6: Select workbook tab and click ok

11.2 JDBC Programming

# Let us write a program in JDBC. We must import java.sql library because we are using SQL commands for e.g. ("Select * from [Sheet1$]") to do the necessary with data base. A user must be aware of Java exceptional handling. This program is linking with data base through ODBC.

# Example: JDBC program to access Excel file (demo.xls) and display the content.

# import java.sql.*;

# public class JdbcDemo

# {

# public static void main(String[] args)

# {

# try

# {

# Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");

# Connection con = DriverManager.getConnection("jdbc:odbc:demo");

# Statement st = con.createStatement();

# ResultSet rs = st.executeQuery("Select * from [Sheet1$]");

# ResultSetMetaData rsmd = rs.getMetaData();

# int numberOfColumns = rsmd.getColumnCount();

# while (rs.next())

# {

# for (int i = 1; i <= numberOfColumns; i++)

# {

# if (i > 1)

# System.out.print(", ");

# String columnValue = rs.getString(i);

# System.out.print(columnValue);

# }

# System.out.println("");

# }

# st.close();

# con.close();

# } catch (Exception ex) {

# System.err.print("Exception: ");

# System.err.println(ex.getMessage());

# }

# }

# }

# Output

# Here user must create an Excel file (demo.xls) and configure ODBC using steps to create DSN than compile and run the program to get access of Excel file.

Chapter 12

# Programming in Core Java

# Let us write program from all sides of Core Java (Applications and Applets). A user must try to do yourself.

1\. Example (Input-Output programming): Application program in Core Java to computer all arithmetic of two Number.

# import java.util.Scanner;

# public class ArithmeticOp {

# public static void main(String[] args) {

# Scanner s = new Scanner(System.in);

# System.out.println("Enter the two numbers to perform operations ");

# System.out.print("Enter the first number : ");

# int x = s.nextInt();

# System.out.print("Enter the second number : ");

# int y = s.nextInt();         

# int add;

# add = x + y;

# System.out.println("Addition of Two Numbers : "+add);             

# int sub;

# sub = x - y;

# System.out.println("Subtraction of Two Numbers : "+sub);              

# int mul;

# mul = x * y;

# System.out.println("Multiplication of Two Numbers  : "+mul);            

# float div;

# div = (float) x / y;

# System.out.print("Division of Two Numbers  : "+div);

# int mod;              

# mod = x % y;

# System.out.println("Modulus of Two Numbers  : "+mod);

# break;

# }

# }

# Output

# ![](image_rsrc2NH.jpg)

# Note: Here user must enter first and second number accordingly he will get the output.

2\. Example (Decision Making): Application program to compute rank of student i.e. if students obtained above 60% than first class, between 50-59% than second class and below 50% failed.

# import java.util.Scanner;

# public class DecisionMaking {

# public static void main(String[] args) {

# Scanner marks = new Scanner(System.in);

# System.out.println("Enter the percentage marks obtained: ");

# int x = marks.nextInt();

# if (x>=60 && x<=100)

# System.out.println("First class");

# else if (x>=50 && x<60) 

# System.out.println("Second class");

# else

# System.out.println(" Failed");           

# }  

# }

# Output

# ![](image_rsrc2NJ.jpg)

3\. Example (Looping): Application program to sum of all even numbers and odd numbers from 1 to 10.

# public class Looping {

# public static void main(String[] args) {

# int i, evensum=0, oddsum=0;

# for(i=1; i<=10;i++)

# {

# if(i%2==0)

# evensum=evensum + i;

# else  

# oddsum=oddsum + i;

# }       

# System.out.println("Evensum from (1-10) =" + evensum);

# System.out.println("Oddsum from (1-10) =" + oddsum);

# }  

# }

# Output

# ![](image_rsrc2NK.jpg)

4\. Example (One-dimensional Array): Application program to sort the given Array in ascending order.

# public class SortArray {

# public static void main(String[] args) {

# int arr[] = {50, 20, 80, 70, 10, 30};

# int temp = 0;

# int a, b;

# System.out.println("Elements of original array: ");

# for (a = 0; a < 6; a++) {   // length of array=6

# System.out.print(arr[a] + " ");

# }

# for (a = 0; a < 6; a++) {

# for (b = a+1; b < 6; b++) {

# if(arr[a] > arr[b]) {

# temp = arr[a];

# arr[a] = arr[b];

# arr[b] = temp;

# } } }

# System.out.println();

# System.out.println("Elements of array sorted in ascending order: ");

# for (a = 0; a < 6; a++) {

# System.out.print(arr[a] + " ");

# } } }

# Output

# ![](image_rsrc2NM.jpg)

5\. Example (Two-dimensional Array): Application program to transpose the given matrix.

# public class TransposeMat {

# public static void main(String[] args) {        

# int original[][]={{1,3,4},{2,4,3},{3,4,5}};   

# int transpose[][]=new int[3][3];  //3 rows and 3 columns  

# for(int i=0;i<3;i++){   

# for(int j=0;j<3;j++){   

# transpose[i][j]=original[j][i];

# }   

# }    

# System.out.println("Printing the given Matrix:"); 

# for(int i=0;i<3;i++){   

# for(int j=0;j<3;j++){   

# System.out.print(original[i][j]+" ");   

# }   

# System.out.println();//new line   

# }   

# System.out.println("Printing Matrix After Transpose:"); 

# for(int i=0;i<3;i++){   

# for(int j=0;j<3;j++){   

# System.out.print(transpose[i][j]+" ");   

# }   

# System.out.println(); //new line   

# } }}  Output

# ![](image_rsrc2NN.jpg)

6\. Example (AWT): Application program to create popup menu and submenu of File.

# import java.awt.*;

# public class PopupMenu{

# PopupMenu (){

# Frame f= new Frame("Menu and Submenu");

# MenuBar mb=new MenuBar();

# Menu menu=new Menu("File");

# Menu submenu=new Menu("Recent");

# MenuItem i1=new MenuItem("Open");

# MenuItem i2=new MenuItem("Save");

# MenuItem i3=new MenuItem("Save as");

# MenuItem i4=new MenuItem("File 1");

# MenuItem i5=new MenuItem("File 2");

# menu.add(i1);

# menu.add(i2);

# menu.add(i3);

# submenu.add(i4);

# submenu.add(i5);

# menu.add(submenu);

# mb.add(menu);

# f.setMenuBar(mb);

# f.setSize(400,400);

# f.setLayout(null);

# f.setVisible(true);

# }

# public static void main(String args[]) 

# {

# new PopupMenu ();

# }

# }

# Output

# ![](image_rsrc2NP.jpg)

7\. Example (Java AWT ): Application program to create a Canvas and draw oval in that.

# import java.awt.*;

# public class CanvasCreation{

# public CanvasCreation ()   

# {   

# Frame c = new Frame("Canvas of AWT");  

# c.add(new MyCanvas());   

# c.setLayout(null);   

# c.setSize(400, 400);   

# c.setVisible(true);   

# }   

# public static void main(String args[])   

# {   

# new CanvasCreation ();   

# }   

# }    

# // to create Canvas 

# class MyCanvas extends Canvas   

# {           

# public MyCanvas() {   

# setBackground (Color.BLACK);   

# setSize(300, 200);   

# }   

# public void paint(Graphics g)   

# {   

# g.setColor(Color.red);   

# g.fillOval(75, 75, 150, 75);   

# }   

# }      

# Output

# ![](image_rsrc2NR.jpg)

8\. Example (Java AWT and Swing event): Application program to create a calculator to perform Addition, Subtraction, Multiplication, Division.

# import javax.swing.*;

# import java.awt.event.*;

# public class MyCalculator implements ActionListener{ 

# JTextField tf1,tf2,tf3;

# JButton b1,b2,b3,b4;

# MyCalculator(){

# JFrame f= new JFrame();

# tf1=new JTextField();

# tf1.setBounds(50,50,150,20);

# tf2=new JTextField();

# tf2.setBounds(50,100,150,20);

# tf3=new JTextField();

# tf3.setBounds(50,150,150,20);

# tf3.setEditable(false);  

# b1=new JButton("+");

# b1.setBounds(50,200,50,50);

# b2=new JButton("-");

# b2.setBounds(120,200,50,50);

# b3=new JButton("*");

# b3.setBounds(190,200,50,50);

# b4=new JButton("/");

# b4.setBounds(260,200,50,50);

# b1.addActionListener(this);

# b2.addActionListener(this);

# b3.addActionListener(this);

# b4.addActionListener(this);

# f.add(tf1);f.add(tf2);f.add(tf3);f.add(b1);f.add(b2);f.add(b3);

# f.add(b4);

# f.setSize(300,300);

# f.setLayout(null);

# f.setVisible(true);

# }        

# public void actionPerformed(ActionEvent e) {

# String s1=tf1.getText();

# String s2=tf2.getText();

# int a=Integer.parseInt(s1);

# int b=Integer.parseInt(s2);

# int c=0;

# if(e.getSource()==b1){

# c=a+b;

# }else if(e.getSource()==b2){

# c=a-b;

# }else if(e.getSource()==b3){

# c=a*b;

# }else if(e.getSource()==b4){

# c=a/b;

# }            

# String result=String.valueOf(c);

# tf3.setText(result);

# }

# public static void main(String[] args) { 

# new MyCalculator ();

# } }

# Output

# ![](image_rsrc2NS.jpg)

# Note: Here user must enter two numbers in first two text box, click on button to calculate finally the result will be shown in third text box.

9\. Example (Java Swing): Application program to create a table of fruits.

# import javax.swing.*;

# public class FruitTable{

# JFrame f;   

# FruitTable (){   

# f=new JFrame();   

# String data[][]={ {"1","Apple"},   

# {"2","Banana"},   

# {"3","Orange"},

# {"4","Grapes"},

# {"5","Mango"},};   

# String column[]={"Sl No.","Name of fruits"};        

# JTable jt=new JTable

# (data,column);   

# jt.setBounds(30,40,200,300);         

# JScrollPane sp=new JScrollPane(jt);   

# f.add(sp);         

# f.setSize(300,400);   

# f.setVisible(true);   

# }    

# public static void main(String[] args) {   

# new FruitTable ();   

# }    }  Output

# ![](image_rsrc2NT.jpg)

10\. Example (Java Swing): Application program to create toolbar of File, Edit and View.

# import java.awt.BorderLayout;

# import java.awt.Container;

# import javax.swing.JButton;  

# import javax.swing.JFrame;

# import javax.swing.JScrollPane;

# import javax.swing.JTextArea;

# import javax.swing.JToolBar;

# public class Component{

# public static void main( String args[]) { 

# JFrame f = new JFrame("Java Swing ToolBar");

# f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

# JToolBar toolbar = new JToolBar();

# toolbar.setRollover(true);

# JButton button = new JButton("File");

# toolbar.add(button);

# toolbar.addSeparator();

# toolbar.add(new JButton("Edit"));

# toolbar.addSeparator();

# toolbar.add(new JButton("View"));      

# Container contentPane = f.getContentPane();

# contentPane.add(toolbar, BorderLayout.NORTH);

# JTextArea textArea = new JTextArea();

# JScrollPane mypane = new JScrollPane(textArea);

# contentPane.add(mypane, BorderLayout.EAST);

# f.setSize(450, 250);

# f.setVisible(true);

# }

# }

# Output

# ![](image_rsrc2NU.jpg)

11\. Example (Java Swing): Application program to create Desktop.

# import java.awt.BorderLayout;

# import java.awt.Container;

# import javax.swing.JDesktopPane;

# import javax.swing.JFrame;

# import javax.swing.JInternalFrame;

# import javax.swing.JLabel;

# public class Component extends JFrame{ 

# public Component()  

# {

# CustomDesktopPane desktopPane = new CustomDesktopPane();

# Container contentPane = getContentPane();

# contentPane.add(desktopPane, BorderLayout.CENTER);

# desktopPane.display(desktopPane);

# setTitle("Java Swing Desktop");

# setSize(300,350);

# setVisible(true);

# }

# public static void  main(String args[])

# {

# new Component();

# }

# }

# class CustomDesktopPane extends JDesktopPane 

# {   

# public void display(CustomDesktopPane dp)  

# {

# JInternalFrame f = new JInternalFrame("My Desktop " ,  true);   

# f.setBounds(30, 30, 250, 85);

# Container c1 = f.getContentPane( ) ;

# c1.add(new JLabel("Hi! User, Welcome to Java Swing "));

# dp.add( jframe );

# f.setVisible(true);        

# }

# }

# Output

# ![](image_rsrc2NV.jpg)

12\. Example (Java Swing): Application program to create a Canvas to draw graphics according to requirement. Here user can draw any shape but accordingly he must give instructions.

# import java.awt.*;

# import javax.swing.JFrame;    

# public class UserGraphics  extends Canvas{

# public void paint(Graphics g) { 

# g.drawString("Hello",40,40);

# setBackground(Color.BLUE);

# g.fillRect(130, 30,100, 80);

# g.drawOval(30,130,50, 60);

# setForeground(Color.GREEN);

# g.fillOval(130,130,50, 60);

# g.drawArc(30, 200, 40,50,90,60);

# g.fillArc(30, 130, 40,50,180,40);    

# }

# public static void main(String[] args) {

# UserGraphics m=new UserGraphics ();

# JFrame f=new JFrame();

# f.add(m);

# f.setSize(400,400);

# //f.setLayout(null);

# f.setVisible(true);

# }  }  Output

# ![](image_rsrc2NW.jpg)

13\. Example (Java AWT, Swing and Applet): Applet program to handle event of AWT and Swing.

# import java.applet.*;

# import javax.swing.*;

# import java.awt.event.*;

# public class EventApplet extends JApplet implements ActionListener{ 

# JButton b;

# JTextField tf;

# public void init(){

# tf=new JTextField();

# tf.setBounds(30,40,150,20);

# b=new JButton("Click");

# b.setBounds(80,150,70,40);

# add(b);add(tf);

# b.addActionListener(this);

# setLayout(null);

# }

# public void actionPerformed(ActionEvent e){ 

# tf.setText("Hi!, Welcome to Applet Event"); 

# }

# }

# Let us create HTML file (Event.html) to handle above program Event.

# <html>

# <body>

# <applet code="EventApplet.class" width="300" height="300"> 

# </applet>

# </body>

# </html>

# Note: Here user has to save the application program file and HTML file in appropriate location then compile the program from command prompt and use appletviewer command to view the output

# The End