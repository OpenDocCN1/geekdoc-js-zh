![](Images/cover00242.jpeg)

PYTHON AND JAVASCRIPT CODING:

BASICS FOR ABSOLUTE BEGINNERS

STEP BY STEP GUIDE TO LEARN CODING QUICKLY

J NEWMAN

[Introduction to Python](#part0002.xhtml__Toc99965571)

[Install Python](#part0003.xhtml__Toc99965572)

[First Python Program](#part0004.xhtml__Toc99965573)

[Python Variables](#part0005.xhtml__Toc99965574)

[Python Data Types](#part0006.xhtml__Toc99965575)

[Python Keywords](#part0007.xhtml__Toc99965576)

[Python Literals](#part0008.xhtml__Toc99965577)

[Python Operators](#part0009.xhtml__Toc99965578)

[Python Comments](#part0010.xhtml__Toc99965579)

[Python If-else statements](#part0011.xhtml__Toc99965580)

[Python Loops](#part0012.xhtml__Toc99965581)

[Python for loop](#part0013.xhtml__Toc99965582)

[Python While loop](#part0014.xhtml__Toc99965583)

[Python break statement](#part0015.xhtml__Toc99965584)

[Python String](#part0016.xhtml__Toc99965585)

[Python List](#part0017.xhtml__Toc99965586)

[Python Tuple](#part0018.xhtml__Toc99965587)

[Learn JavaScript](#part0020.xhtml__Toc99965588)

[JavaScript Comment](#part0021.xhtml__Toc99965589)

[JavaScript Variable](#part0022.xhtml__Toc99965590)

[JavaScript Global Variable](#part0023.xhtml__Toc99965591)

[Javascript Data Types](#part0024.xhtml__Toc99965592)

[JavaScript Operators](#part0025.xhtml__Toc99965593)

[JavaScript If-else](#part0026.xhtml__Toc99965594)

[JavaScript Switch](#part0027.xhtml__Toc99965595)

[JavaScript Loops](#part0028.xhtml__Toc99965596)

[JavaScript Functions](#part0029.xhtml__Toc99965597)

[JavaScript Objects](#part0030.xhtml__Toc99965598)

[JavaScript Array](#part0031.xhtml__Toc99965599)

[JavaScript String](#part0032.xhtml__Toc99965600)

[JavaScript Date Object](#part0033.xhtml__Toc99965601)

[JavaScript Math](#part0034.xhtml__Toc99965602)

[JavaScript Number Object](#part0035.xhtml__Toc99965603)

[JavaScript Boolean](#part0036.xhtml__Toc99965604)

# Introduction to Python

Python has a variety of beneficial features that distinguish it from other programming languages. It enables object-oriented programming, procedural programming, and memory allocation that is dynamic. A few crucial aspects are described below.

### 1) Easy to Learn

Python is a simple programming language to learn when compared to other programming languages. Its syntax is simple and similar to that of the English language. The semicolon and curly brackets are not used; instead, the indentation defines the code block. For novices, it is the suggested programming language.

### 2) Expressive Language

Python is capable of performing complex tasks with just a few lines of code. For example, to run the hello world program, simply type print ("Hello World"). It will just require one line of code to run, whereas Java or C will require numerous lines.

### 3) Interpreted Language

Python is an interpreted language, which implies that each line of a Python program is executed separately. The benefit of being an interpreted language is that debugging is simple and portable.

### 4) Cross-platform Language

Python can operate on a variety of platforms, including Windows, Linux, UNIX, and Macintosh. As a result, we may conclude that Python is a portable programming language. It allows programmers to create software for several rival platforms by creating only one program.

### 5) Free and Open Source

Python is a free programming language that anyone can use. On its official website, www.python.org, it is freely available. It has a vast community all around the world working hard to create new Python modules and functions. The Python community welcomes contributions from everyone. "Anyone can get its source code without paying a penny," says open-source.

### 6) Object-Oriented Language

Python enables object-oriented programming, which introduces the notions of classes and objects. It allows for inheritance, polymorphism, and encapsulation, among other things. The object-oriented method aids programmers in writing reusable code and developing applications with fewer code.

### 7) Extensible

It means that other languages, such as C/C++, can be used to compile the code, allowing us to use it in our Python work. It converts the program to byte code, which may be run on any platform.

### 8) Large Standard Library

It offers a diverse set of libraries for a variety of domains, including machine learning, web development, and scripting. Tensor flow, Pandas, Numpy, Keras, and Pytorch are just a few examples of machine learning libraries. Python web development frameworks include Django, Flask, and Pyramids.

### 9) GUI Programming Support

For the development of a desktop program, a graphical user interface is used. The libraries used to construct the web application include PyQT5, Tkinter, and Kivy.

### 10) Integrated

It's simple to integrate with languages like C, C++, and JAVA, among others. Python, like C, C++, and Java, executes code line by line. It makes debugging the code much easier.

### 11. Embeddable

Other programming languages' code can be used in the Python source code. Python source code can also be used in other computer languages. It has the ability to embed additional languages into our programs.

### 12\. Dynamic Memory Allocation

We don't need to specify the variable's data type in Python. When we assign a value to a variable, the variable's memory is automatically allocated at run time. If the integer value 15 is assigned to x, we don't need to write int x = 15. Simply write x = 15 on a piece of paper.

# Install Python

The first step toward becoming a Python developer is to understand how to install and update Python on a local system or computer. We'll go over how to install Python on various operating systems in this topic.

## Installation on Windows

To get the newest version of Python, go to https://www.python.org/downloads/. We will install Python 3.8.6 on our Windows operating system during this procedure. When we click the link above, we will be sent to the following website.

Step - 1: Select - Python's version - download.

![](Images/image00161.jpeg)

Step - 2: Click - Install Now

Double-click the downloaded executable file to bring up the following window. Proceed by selecting Customize installation. When you select the Add Path check box, the Python path will be automatically configured.

![](Images/image00162.jpeg)

We may also select the required location and features by clicking on the customise installation button. Another key factor to consider is whether or not to install a launcher for all users.

Step - 3 Installation in Process

![](Images/image00163.jpeg)

Try running python from the command prompt now. If you're using Python 3, type python -version.

![](Images/image00164.jpeg)

We're all set to work with Python.

# First Python Program

In this section, we'll go through Python's fundamental syntax and run a simple program that prints Hello World to the terminal.

Python gives us two options for running a program:

*   Using a prompt from an interactive interpreter
*   Making use of a script file

Let's take a closer look at each of them.

## Interactive interpreter prompt

At the interactive prompt, Python allows us to execute each Python statement one by one. When we are concerned with the output of each line of our Python program, it is preferable.

To enter interactive mode, type python on the terminal (or command prompt) (python3 in case if you have Python2 and Python3 both installed on your system).

It will open the prompt below, where we can run the Python statement and see how it affects the terminal.

![](Images/image00165.jpeg)

Press the Enter key after finishing the print statement.

![](Images/image00166.jpeg)

## Multi-line Statements

Multi-line statements are typed into a notepad like text editor and saved as.py files. We've used the Python script to describe the execution of numerous code lines in the following example.

Code:

1.  name = "Andrew Venis"  
2.  branch = "Computer Science"  
3.  age = "25"  
4.  print("My name is: ", name, )  
5.  print("My age is: ", age)  

Script File:

![](Images/image00167.jpeg)

![](Images/image00168.jpeg)

# Python Variables

A variable is a term that refers to a memory region. A Python variable, often known as an identifier, is a container for data.

Because Python is an infer language, we don't need to describe the type of variable because it is smart enough to figure it out.

Variable names can consist of a combination of letters and digits, but they must start with a letter or underscore.

The variable name should be written in lowercase letters. Both rahul and rahul are two distinct variables.

## Identifier Naming

Identifiers are examples of variables. The literals in the program are identified using an Identifier. The following are the rules for naming an identifier.

*   The variable's initial character must be an alphabet or underscore ( ).
*   All characters except the first may be a lower-case (a-z), upper-case (A-Z), underscore, or digit alphabet (0-9).
*   There must be no whitespace or special characters in the identifier name (!, @, #, percent,,, &, *).
*   The name of the identifier must not be identical to any of the language's keywords.
*   Case matters when it comes to identifier names; for example, my name and MyName are not the same thing.
*   Valid identifiers include a123, _n, n 9, and others.
*   1a, n percent 4, n 9, and other incorrect identifiers are examples.

## Declaring Variable

Python does not require us to declare variables before utilising them in our code. It enables us to construct a variable at a certain point in time.

In Python, we don't need to declare variables explicitly. Any time we assign a value to a variable, it is automatically defined.

A variable's value is assigned using the equal (=) operator.

## Object References

When declaring a variable, it's important to understand how the Python interpreter works. The way variables are handled differs from that of many other programming languages.

Because Python is an object-oriented programming language, each data item belongs to a specific type of class. Consider the following illustration.

1.  print("John")  

Output:

John

The Python object builds and displays an integer object on the terminal. We created a string object in the print command above. Let's see what type it is using the built-in type() function in Python.

1.  type("John")  

Output:

<class 'str'>

Variables are a symbolic term for a reference or pointer to an object in Python. The variables are used to represent objects with the same name.

Let's take a look at the following example.

a = 50 

![](Images/image00169.jpeg)

The variable an in the illustration above corresponds to an integer object.

Assume we give a new variable b the integer value 50.

a = 50

b = a

![](Images/image00170.jpeg)

Because Python does not generate new objects, the variable b refers to the same object as a.

Let's change the value of b. Both variables will now relate to distinct objects.

a = 50

b =100

![](Images/image00171.jpeg)

If we assign the same variable to two different values, Python maintains memory efficiently.

## Object Identity

Every created object in Python has a unique identifier. Python ensures that no two objects share the same identifier. The object identification is identified using the built-in id() function. Consider the following illustration.

1.  a = 50  
2.  b = a  
3.  print(id(a))  
4.  print(id(b))  
5.  # Reassigned variable a  
6.  a = 500  
7.  print(id(a))

Output:

140734982691168

140734982691168

2822056960944

We set b = a because a and b both refer to the same thing. The id() function returned the same number when we examined it. We changed the value of a to 500, and it now refers to the new object identification.

# Python Data Types

Values can be stored in variables, and each value has a data type. Because Python is a dynamically typed language, we don't need to specify the variable's type when declaring it. The value is implicitly bound to its type by the interpreter.

1.  a = 5  

We didn't define the type of the variable a, which has the integer value of five. Variable a will be automatically interpreted as an integer type by the Python interpreter.

The type of a variable used in a program can be checked using Python. The type() method in Python returns the type of the variable supplied to it.

Consider the following scenario for defining the values of various data kinds and determining their type.

1.  a=10  
2.  b="Hi Python"  
3.  c = 10.5  
4.  print(type(a))  
5.  print(type(b))  
6.  print(type(c))  

Output:

<type 'int'>

<type 'str'>

<type 'float'>

## Standard data types

Different types of values can be stored in a variable. A person's name, for example, must be saved as a string, whereas his or her id must be recorded as an integer.

Python supports a number of standard data types, each with its own storage technique. The following is a list of Python data types.

1.  Numbers
2.  Sequence Type
3.  Boolean
4.  Set
5.  Dictionary

![](Images/image00172.jpeg)

We'll give a quick overview of the above data types in this section of the lesson. Later in this course, we'll go over each of them in depth.

### Numbers

Number is a type of data that stores numerical values. A Python Numbers data-type has integer, float, and complex values. The type() method in Python can be used to determine the data type of a variable. The isinstance() function is used to determine whether an object belongs to a specific class.

When a variable is assigned a number, Python produces Number objects. As an example;

1.  a = 5  
2.  print("The type of a", type(a))  

4.  b = 40.5  
5.  print("The type of b", type(b))  

7.  c = 1+3j  
8.  print("The type of c", type(c))  
9.  print(" c is a complex number", isinstance(1+3j,complex)) 

Output:

The type of a <class 'int'>

The type of b <class 'float'>

The type of c <class 'complex'>

c is complex number: True

Python recognises three types of numerical data.

Integer values can be any length, such as 10, 2, 29, -20, -150, and so on. An integer's length is not limited in Python. Its value is an int.

Float is used to store floating-point numbers such as 1.9, 9.902, 15.2, and so on. It has a precision of up to 15 decimal places.

A complex number is made up of an ordered pair, i.e., x + iy, where x and y represent the real and imaginary parts, respectively. Complex numbers such as 2.14j, 2.0 + 2.3j, and so on.

# Python Keywords

Python keywords are reserved words that communicate a specific meaning to the compiler/interpreter. Each keyword has a distinct meaning and a distinct operation. These keywords are ineligible for use as variables. The list of Python keywords is as follows.

![](Images/image00173.jpeg)

True - It represents the Boolean true, which means that if the given condition is true, it returns "True." Non-zero values are assumed to be true.

False - It represents the Boolean false; it returns "False" if the given condition is false. A value of zero is interpreted as false.

None - It denotes a null or void value. An empty list or Zero cannot be used to represent None.

And - It is also a logical operator. It's used to test for multiple conditions. If both conditions are met, it returns true. Consider the truth table below.

![](Images/image00174.jpeg)

or - In Python, it is a logical operator. If one of the conditions is met, it returns true. Consider the truth table below.

![](Images/image00175.jpeg)

not - It's a logical operator that flips the truth value. Consider the truth table below.

![](Images/image00176.jpeg)

assert - In Python, this keyword is used as a debugging tool. It verifies the code's correctness. If an error is found in the code, it raises an AssertionError and prints an error message.

Example:

1.  a = 10  
2.  b = 0  
3.  print('a is dividing by Zero')  
4.  assert b != 0  
5.  print(a / b)

Output:

a is dividing by Zero

Runtime Exception:

Traceback (most recent call last):

  File "/home/40545678b342ce3b70beb1224bed345f.py", line 4, in 

    assert b != 0, "Divide by 0 error"

AssertionError: Divide by 0 error

Def - In Python, this keyword is used to declare the function. If it is followed by the name of the function.

1.  def my_func(a,b):  
2.  c = a+b  
3.  print(c)  
4.  my_func(10,20)  

Output:

30

class - In Python, it is used to represent a class. The class serves as the objects' blueprint. It is a grouping of variables and methods. Consider the class below.

1.  class Myclass:  
2.  #Variables……..  
3.  def function_name(self):  
4.  #statements………  

continue - This command is used to halt the current iteration's execution. Consider the following scenario.

1.  a = 0  
2.  while a < 4:  
3.  a += 1   
4.  if a == 2:  
5.  continue  
6.  print(a)  

Output:

1

3

4

# Python Literals

Literals in Python are data that is stored in a variable or constant.

Python supports - following literals:

### 1\. String literals:

String literals are created by enclosing text in quotes. To make a string, we can use both single and double quotes.

Example:

1.  "Aman" , '12345'  

### 2. Numeric literals

Numeric Literals are unchangeable. Numeric literals can be classified into one of four numerical types.

![](Images/image00177.jpeg)

Example - Numeric Literals

1.  x = 0b10100 #Binary Literals  
2.  y = 100 #Decimal Literal   
3.  z = 0o215 #Octal Literal  
4.  u = 0x12d #Hexadecimal Literal  

6.  #Float Literal  
7.  float_1 = 100.5   
8.  float_2 = 1.5e2  

10.  #Complex Literal   
11.  a = 5+3.14j  

13.  print(x, y, z, u)  
14.  print(float_1, float_2)  
15.  print(a, a.imag, a.real)  

Output:

20 100 141 301

100.5 150.0

(5+3.14j) 3.14 5.0

### 3. Boolean literals:

A Boolean literal can have either True or False as its value.

Example - Boolean Literals

1.  x = (1 == True)  
2.  y = (2 == False)  
3.  z = (3 == True)  
4.  a = True + 10  
5.  b = False + 10  

7.  print("x is", x)  
8.  print("y is", y)  
9.  print("z is", z)  
10.  print("a:", a)  
11.  print("b:", b)  

Output:

x is True

y is False

z is False

a: 11

b: 10

### 4\. Special literals.

Python has a single special literal, None.

None is used to specify a field that has not yet been created. In Python, it is also used to indicate the end of a list. A Boolean literal can have either True or False as its value.

Example - Special Literals

1.  val1=10    
2.  val2=None    
3.  print(val1)     
4.  print(val2)  

Output:

10

None

### 5. Literal Collections.

Python supports four different types of literal collections:

*   List literals,
*   Tuple literals,
*   Dict literals, and
*   Set literals.

List:

*   The items in a list are of various data types. Lists are mutable, which means they can be changed.
*   List values are separated by commas (,) and enclosed in square brackets ([]). A List can hold various types of data. Python supports four different types of literal collections: List literals, Tuple literals, Dict literals, and Set literals.

Example - List literals

1.  list=['John',678,20.4,'Peter']    
2.  list1=[456,'Andrew']    
3.  print(list)    
4.  print(list + list1)  

Output:

['John', 678, 20.4, 'Peter']

['John', 678, 20.4, 'Peter', 456, 'Andrew']

Dictionary:

*   The data is stored in a Python dictionary as a key-value pair.
*   It is surrounded by curly braces, and each pair is separated by commas (,).

Example

1.  dict = {'name': 'Pater', 'Age':18,'Roll_nu':101}  
2.  print(dict)  

Output:

{'name': 'Pater', 'Age': 18, 'Roll_nu': 101}

Tuple:

A tuple in Python is a collection of different data types. It is immutable, which means it cannot be changed after it is created.

It is surrounded by parentheses (), and each element is separated by a comma (,).

Example

1.  tup = (10,20,"Dev",[2,3,4])  
2.  print(tup)  

Output:

(10, 20, 'Dev', [2, 3, 4])

Set:

The Python set is a collection of unordered datasets.

It is surrounded by and each element is separated by a comma (,).

Example: - Set Literals

1.  set = {'apple','grapes','guava','papaya'}  
2.  print(set)  

Output:

{'guava', 'apple', 'papaya', 'grapes'}

# Python Operators

The operator is a symbol that is in charge of a specific operation between two operands. Operators are the foundations of a program, upon which the logic is built in a particular programming language. Python has a number of operators, which are listed below.

*   Arithmetic operators
*   Comparison operators
*   Assignment Operators
*   Logical Operators
*   Bitwise Operators
*   Membership Operators
*   Identity Operators

## Arithmetic Operators

Arithmetic operators are used to perform operations on two operands. It has the operators + (addition), - (subtraction), *(multiplication), /(divide), percent (reminder), /(floor division), and exponent (**).

Consider the table below for a more in-depth explanation of arithmetic operators.

![](Images/image00178.jpeg)

## Comparison operator

Comparison operators are used to compare the values of two operands and return a Boolean true or false result. The comparison operators are listed in the table below.

![](Images/image00179.jpeg)

## Assignment Operators

The assignment operators are used to assign the right expression's value to the left operand. The assignment operators are listed in the table below.

![](Images/image00180.jpeg)

![](Images/image00181.jpeg)

## Bitwise Operators

The bitwise operators operate on the values of the two operands bit by bit. Consider the following scenario.

For example,

1.  if a = 7   
2.  b = 6     
3.  then, binary (a) = 0111    
4.  binary (b) = 0110    

6.  hence, a & b = 0011    
7.  a | b = 0111    
8.  a ^ b = 0100    
9.  ~ a = 1000  

![](Images/image00182.jpeg)

## Logical Operators

To make a decision, logical operators are primarily used in expression evaluation. Python supports the logical operators listed below.

![](Images/image00183.jpeg)

## Membership Operators

Python membership operators are used to determine whether a value is a member of a Python data structure. If the value exists in the data structure, the result is true; otherwise, it returns false.

![](Images/image00184.jpeg)

## Identity Operators

The identity operators are used to determine whether an element belongs to a specific class or type.

![](Images/image00185.jpeg)

## Operator Precedence

The precedence of the operators is critical to determining because it tells us which operator should be evaluated first. The precedence table of Python operators is shown below.

![](Images/image00186.jpeg)

![](Images/image00187.jpeg)

# Python Comments

Python Comment is a must-have tool for programmers. In general, comments are used to explain the code. If the code is properly explained, we can easily understand it. A good programmer should use comments because if anyone wants to modify the code or implement a new module in the future, it will be much easier to do so.

Other programming languages, such as C++, use the / for single-lined comments and /*.... */ for multiple-lined comments, whereas Python only uses the / for single-lined Python comments. To include a comment in code, place a hash(#) at the beginning of the statement or code.

Let's take a look at an example.

1.  # This is the print statement  
2.  print("Hello Python")  

Using the hash(#), we have added a comment to the print statement. It will have no effect on our print statement.

## Multiline Python Comment

To use the multiline Python comment, we must use hash(#) at the beginning of each line of code. Consider the following scenario.

1.  # First line of the comment   
2.  # Second line of the comment  
3.  # Third line of the comment  

Example:

1.  # Variable a holds value 5  
2.  # Variable b holds value 10  
3.  # Variable c holds sum of a and b  
4.  # Print the result  
5.  a = 5  
6.  b = 10  
7.  c = a+b  
8.  print("The sum is:", c)  

Output:

The sum is: 15

The above code is very readable, and even complete beginners can understand what is going on in each line of code. This is one of the benefits of using comments in code.

For multiline comments, we can also use triple quotes ("""). String formatting is also done with triple quotes. Consider the following scenario.

## Docstrings Python Comment

The docstring comment is typically found in a module, function, class, or method. It's a Python documentation string. In subsequent tutorials, we will explain the class/method.

Example:

1.  def intro():  
2.  """ 
3.  This function prints Hello Joseph 
4.  """  
5.  print("Hi Joseph")              
6.  intro()  

Output:

Hello Joseph

Using the __doc__ attribute, we can inspect a function's docstring.

In most cases, four whitespaces are used as indentation. The amount of indentation is up to the user, but it must be consistent across the block.

1.  def intro():  
2.  """ 
3.  This function prints Hello Joseph 
4.  """  
5.  print("Hello Joseph")              
6.  intro.__doc__  

Output:

Output:

'\n  This function prints Hello Joseph\n  '

## Python indentation

Python indentation is used to define code blocks. Curly braces are used in other programming languages such as C, C++, and Java, whereas Python uses indentation. In Python, whitespaces are used to indicate indentation.

Indentation is used at the start of the code and ends with an unexpected line. The code block is defined by the same line indentation (body of a function, loop, etc.)

In most cases, four whitespaces are used as indentation. The amount of indentation is up to the user, but it must be consistent across the block.

1.  for i in range(5):  
2.  print(i)  
3.  if(i == 3):  
4.  break

We used the same whitespaces to indent each line of code to indicate a block of code.

Consider the following scenario.

1.  dn = int(input("Enter the number:"))  
2.  if(n%2 == 0):  
3.  print("Even Number")  
4.  else:  
5.  print("Odd Number")  

7.  print("Task Complete")  

Output:

Enter the number: 10

Even Number

Task Complete

If and else are two separate code blocks in the preceding code. Both code blocks are four spaces indented. The print("Task Complete") statement is out of the if-else block and is not indented four whitespaces.

IndentationError will be thrown if the indentation is not used correctly.

# Python If-else statements

The most important aspect of almost all programming languages is decision making. Decision making, as the name implies, allows us to run a specific block of code for a specific decision. Decisions on the validity of specific conditions are made here. The foundation of decision making is condition checking.

The following statements in Python are used to make decisions.

![](Images/image00188.jpeg)

## Indentation in Python

Python does not allow the use of parentheses in block level code for the sake of simplicity and ease of programming. To declare a block in Python, use indentation. If two statements have the same indentation level, they are in the same block.

In general, four spaces are used to indent the statements, which is the standard amount of indentation in Python.

Because it declares the block of code, indentation is the most commonly used feature of the Python programming language. All of the statements in a block are intended to be indented at the same level. We'll look at how actual indentation occurs in Python decision making and other areas.

## The if statement

The if statement is used to test a condition, and if the condition is true, it executes an if-block of code. Any valid logical expression that can be evaluated to true or false can be used as the condition of an if statement.

![](Images/image00189.jpeg)

The if-statement syntax is shown below.

1.  if expression:  
2.  statement  

### Example 1

1.  num = int(input("enter the number?"))  
2.  if num%2 == 0:  
3.  print("Number is even")  

Output:

enter the number?10

Number is even

### Example 2

Print the largest of the three numbers using the program

1.  a = int(input("Enter a? "));  
2.  b = int(input("Enter b? "));  
3.  c = int(input("Enter c? "));  
4.  if a>b and a>c:  
5.  print("a is largest");  
6.  if b>a and b>c:  
7.  print("b is largest");  
8.  if c>a and c>b:  
9.  print("c is largest");  

Output:

Enter a? 100

Enter b? 120

Enter c? 130

c is largest

## The if-else statement

The if-else statement combines an else block with the if statement, which is executed when the condition is false.

If the condition is met, the if-block is run. If not, the else-block is executed.

![](Images/image00190.jpeg)

The if-else statement syntax is shown below.

1.  if condition:  
2.  #block of statements   
3.  else:   
4.  #another block of statements (else-block)  

EXAMPLE

A program that determines whether or not a person is eligible to vote.

1.  age = int (input("Enter your age? "))  
2.  if age>=18:  
3.  print("You are eligible to vote !!");  
4.  else:  
5.  print("Sorry! you have to wait !!");  

Output:

Enter your age? 90

You are eligible to vote !!

## The elif statement

The elif statement allows us to check multiple conditions and execute a specific block of statements based on the true condition of those conditions. Depending on our needs, we can include as many elif statements as we want in our program. Using elif, on the other hand, is optional.

In C, the elif statement functions similarly to an if-else-if ladder statement. It has to be followed by an if statement.

The elif statement's syntax is shown below.

1.  if expression 1:   
2.  # block of statements   

4.  elif expression 2:   
5.  # block of statements   

7.  elif expression 3:   
8.  # block of statements   

10.  else:   
11.  # block of statements  

![](Images/image00191.jpeg)

EXAMPLE

1.  number = int(input("Enter the number?"))  
2.  if number==10:  
3.  print("number is equals to 10")  
4.  elif number==50:  
5.  print("number is equal to 50");  
6.  elif number==100:  
7.  print("number is equal to 100");  
8.  else:  
9.  print("number is not equal to 10, 50 or 100");  

Output:

Enter the number?15

number is not equal to 10, 50 or 100

# Python Loops

By default, the flow of programs written in any programming language is sequential. We may need to change the program's flow from time to time. The execution of a particular code may need to be repeated several times.

The programming languages provide various types of loops for this purpose, which are capable of repeating some specific code a number of times. Consider the diagram below to better understand how a loop statement works.

![](Images/image00192.jpeg)

![](Images/image00193.jpeg)

# Python for loop

In Python, the for loop is used to iterate over statements or parts of a program several times. It is commonly used to traverse data structures such as a list, tuple, or dictionary.

Python's for loop syntax is shown below.

1.  for iterating_var in sequence:    
2.  statement(s)

FLOW CHART

![](Images/image00194.jpeg)

### For loop - Using Sequence

EXAMPLE - Using a for loop to iterate over a string

1.  str = "Python"  
2.  for i in str:  
3.  print(i)  

Output:

P

y

t

h

o

n

Example- 2

Print the table of the given number using this program.

1.  list = [1,2,3,4,5,6,7,8,9,10]  
2.  n = 5  
3.  for i in list:  
4.  c = n*i  
5.  print(c)  

Output:

5

10

15

20

25

30

35

40

45

50s

# Python While loop

The Python while loop executes a section of code until the given condition returns false. It is also referred to as a pre-tested loop.

It can be thought of as a looping if statement. When we don't know how many iterations we'll need, the while loop is the best option.

The syntax is provided below.

1.  while expression:    
2.  statements 

FLOW CHART

![](Images/image00195.jpeg)

## Loop Control Statements

Using the loop control statement, we can change the normal sequence of execution of the while loop. When the while loop is finished, all automatic objects defined in that scope are destroyed. Within the while loop, Python provides the following control statement.

1.  Continue Statement - When the continue statement is encountered, control returns to the start of the loop. Let's take a look at an example.

Example:

1.  # prints all letters except 'a' and 't'   
2.  i = 0  
3.  str1 = 'javapoint'  

5.  while i < len(str1):   
6.  if str1[i] == 'a' or str1[i] == 't':   
7.  i += 1  
8.  continue  
9.  print('Current Letter :', a[i])   
10.  i += 1  

Output:

Current Letter : j

Current Letter : v

Current Letter : p

Current Letter : o

Current Letter : i

Current Letter : n

2.  Break Statement - When the break statement is encountered, control is removed from the loop.

Example:

1.  # The control transfer is transfered  
2.  # when break statement soon it sees t  
3.  i = 0  
4.  str1 = 'javapoint'  

6.  while i < len(str1):   
7.  if str1[i] == 't':   
8.  i += 1  
9.  break  
10.  print('Current Letter :', str1[i])   
11.  i += 1  

Output:

Current Letter : j

Current Letter : a

Current Letter : v

Current Letter : a

3\. Pass Statement - The empty loop is declared using the pass statement. It can also be used to define an empty class, function, or control statement. Let's take a look at an example.

Example -

1.  # An empty loop   
2.  str1 = 'javapoint'  
3.  i = 0  

5.  while i < len(str1):   
6.  i += 1  
7.  pass  
8.  print('Value of i :', i)  

Output:

Value of i : 9

### Example

Print a table of given numbers using this program.

1.  i=1    
2.  number=0    
3.  b=9    
4.  number = int(input("Enter the number:"))    
5.  while i<=10:    
6.  print("%d X %d = %d \n"%(number,i,number*i))    
7.  i = i+1    

Output:

Enter the number:10

10 X 1 = 10

10 X 2 = 20

10 X 3 = 30

10 X 4 = 40

10 X 5 = 50

10 X 6 = 60

10 X 7 = 70

10 X 8 = 80

10 X 9 = 90

10 X 10 = 100

## Using else with while loop

Python allows us to use the else statement in conjunction with the while loop.

When the condition in the while statement fails, the else block is executed.

If the while loop is broken using the break statement, the else block is not executed, and the statement following the else block is executed.

When using the while loop, the else statement is optional. Consider the following scenario.

### Example 1

1.  i=1   
2.  while(i<=5):    
3.  print(i)    
4.  i=i+1    
5.  else:  
6.  print("The while loop exhausted")    

### Example 2

1.  i=1    
2.  while(i<=5):    
3.  print(i)    
4.  i=i+1    
5.  if(i==3):    
6.  break   
7.  else:  
8.  print("The while loop exhausted")  

Output:

1

2

# Python break statement

In Python, the break keyword is used to remove the program control from the loop. The break statement breaks the loops one at a time, so in the case of nested loops, it breaks the inner loop first and then moves on to the outer loops. In other words, break is used to abort the current execution of the program, and control is transferred to the next line after the loop.

The break is commonly used when we need to break the loop for a specific condition.

The break syntax is shown below.

1.  #loop statements  
2.  break;   

## Example 1

1.  list =[1,2,3,4]  
2.  count = 1;  
3.  for i in list:  
4.  if i == 4:  
5.  print("item matched")  
6.  count = count + 1;  
7.  break  
8.  print("found at",count,"location");  

Output:

item matched

found at 2 location

## Example 2

1.  str = "python"  
2.  for i in str:  
3.  if i == 'o':  
4.  break  
5.  print(i);  

Output:

p

y

t

h

# Python String

So far, we've covered numbers as the most common data types in Python. In this section of the tutorial, we'll go over the most common data type in Python: strings.

A Python string is a collection of characters surrounded by single, double, or triple quotes. The computer does not understand the characters; instead, it stores the manipulated character as a combination of 0's and 1's internally.

Each character is encoded in either ASCII or Unicode. As a result, Python strings can also be referred to as a collection of Unicode characters.

Strings can be created in Python by enclosing the character or sequence of characters in quotes. Python allows us to create the using single quotes, double quotes, or triple quotes.

### Syntax:

1.  str = "Hi Python !"    

In this case, we can use a Python script to determine the type of the variable str.

1.  print(type(str)), then it will print a string (str).   

Strings are considered as a succession of characters in Python, which implies the character data-type isn't supported; instead, a single character typed as 'p' is treated as a one-length string.

## Creating String

By surrounding the characters in single-quotes or double-quotes, we can form a string. Triple-quotes are another way to express a string in Python, but they're usually reserved for multiline strings or docstrings.

1.  #Using single quotes  
2.  str1 = 'Hello Python'  
3.  print(str1)  
4.  #Using double quotes  
5.  str2 = "Hello Python"  
6.  print(str2)  

8.  #Using triple quotes  
9.  str3 = '''''Triple quotes are generally used for  
10.  represent the multiline or 
11.  docstring'''   
12.  print(str3)  

Output:

Hello Python

Hello Python

Triple quotes are generally used for

    represent the multiline or

    docstring

## Strings indexing and splitting

The indexing of Python strings begins at 0 like it does in other languages. The string "HELLO," for example, is indexed as shown in the diagram below.

![](Images/image00196.jpeg)

EXAMPLE

1.  str = "HELLO"  
2.  print(str[0])  
3.  print(str[1])  
4.  print(str[2])  
5.  print(str[3])  
6.  print(str[4])  
7.  # It returns the IndexError because 6th index doesn't exist  
8.  print(str[6])  

Output:

H

E

L

L

O

IndexError: string index out of range

The slice operator [] is used to access the individual characters of the string, as demonstrated in Python. In Python, however, we can obtain the substring from the given string by using the: (colon) operator. Consider the following illustration.

![](Images/image00197.jpeg)

# Python List

In Python, a list is used to store the sequence of different types of data. Python lists are changeable, which means we can change their elements after they've been formed. However, Python has six data types that can be used to store sequences, with the list being the most common and stable.

A list can be defined as a collection of distinct types of values or items. The comma (,) separates the elements in the list, which are enclosed in square brackets [].

The following is an example of a list.

1.  L1 = ["John", 102, "USA"]    
2.  L2 = [1, 2, 3, 4, 5, 6] 

When we try to print the type of L1, L2, and L3 using the type() method, we get a list.

1.  print(type(L1))  
2.  print(type(L2))  

Output:

<class 'list'>

<class 'list'>

![](Images/image00198.jpeg)

Let's look at the first statement, which states that lists are ordered.

1.  a = [1,2,"Peter",4.50,"Ricky",5,6]  
2.  b = [1,2,5,"Peter",4.50,"Ricky",6]  
3.  a ==b  

Output:

False

Both lists had the same elements, but the second list modified the index position of the fifth member, which went against the list's order. When the two lists are compared, the result is false.

Lists keep the element's order for the duration of their existence. That is why it is a collection of objects in a specific arrangement.

1.  a = [1, 2,"Peter", 4.50,"Ricky",5, 6]  
2.  b = [1, 2,"Peter", 4.50,"Ricky",5, 6]  
3.  a == b  

Output:

True

Let's take a closer look at the list example.

1.  emp = ["John", 102, "USA"]     
2.  Dep1 = ["CS",10]  
3.  Dep2 = ["IT",11]    
4.  HOD_CS = [10,"Mr. Holding"]    
5.  HOD_IT = [11, "Mr. Bewon"]    
6.  print("printing employee data...")    
7.  print("Name : %s, ID: %d, Country: %s"%(emp[0],emp[1],emp[2]))    
8.  print("printing departments...")   
9.  print("Department 1:\nName: %s, ID: %d\nDepartment 2:\nName: %s, ID: %s"%(Dep1[0],Dep2[1],Dep2[0],Dep2[1]))    
10.  print("HOD Details ....")    
11.  print("CS HOD Name: %s, Id: %d"%(HOD_CS[1],HOD_CS[0]))    
12.  print("IT HOD Name: %s, Id: %d"%(HOD_IT[1],HOD_IT[0]))    
13.  print(type(emp),type(Dep1),type(Dep2),type(HOD_CS),type(HOD_IT))  

Output:

printing employee data...

Name : John, ID: 102, Country: USA

printing departments...

Department 1:

Name: CS, ID: 11

Department 2:

Name: IT, ID: 11

HOD Details ....

CS HOD Name: Mr. Holding, Id: 10

IT HOD Name: Mr. Bewon, Id: 11

<class 'list'> <class 'list'> <class 'list'> <class 'list'> <class 'list'>

In the preceding example, we built lists containing employee and department information and printed the related information. Examine the code above to gain a better understanding of the list notion.

# Python Tuple

Python Tuple is a data structure for storing a sequence of immutable Python objects. The tuple is similar to lists in that the value of the items placed in the list can be modified, however the tuple is immutable and its value cannot be changed.

Creating a tuple

The collection of comma-separated (,) values contained by small () brackets is known as a tuple. The use of parentheses is optional, however it is recommended. The following is a definition of a tuple.

1.  T1 = (101, "Peter", 22)    
2.  T2 = ("Apple", "Banana", "Orange")     
3.  T3 = 10,20,30,40,50  

5.  print(type(T1))  
6.  print(type(T2))  
7.  print(type(T3))  

Output:

<class 'tuple'>

<class 'tuple'>

<class 'tuple'>

Creating a tuple with a single element is a little more complicated. To declare the tuple, we must use a comma after the element.

1.  tup1 = ("JavaTpoint")  
2.  print(type(tup1))  
3.  #Creating a tuple with single element   
4.  tup2 = ("JavaTpoint",)  
5.  print(type(tup2))  

Output:

<class 'str'>

<class 'tuple'>

In the same way that lists are indexed, tuples are indexed as well. The index value of each item in the tuple can be used to access it.

Take the following tuple as an example:

### Example

1.  tuple1 = (10, 20, 30, 40, 50, 60)    
2.  print(tuple1)    
3.  count = 0    
4.  for i in tuple1:    
5.  print("tuple1[%d] = %d"%(count, i))   
6.  count = count+1  

Output:

(10, 20, 30, 40, 50, 60)

tuple1[0] = 10

tuple1[1] = 20

tuple1[2] = 30

tuple1[3] = 40

tuple1[4] = 50

tuple1[5] = 60

### Example - 2

1.  tuple1 = tuple(input("Enter the tuple elements ..."))  
2.  print(tuple1)    
3.  count = 0    
4.  for i in tuple1:    
5.  print("tuple1[%d] = %s"%(count, i))   
6.  count = count+1  

Output:

Enter the tuple elements ...123456

('1', '2', '3', '4', '5', '6')

tuple1[0] = 1

tuple1[1] = 2

tuple1[2] = 3

tuple1[3] = 4

tuple1[4] = 5

tuple1[5] = 6

In the same way that lists are indexed, tuples are indexed as well. The index value of each item in the tuple can be used to access it.

## Tuple indexing and slicing

The tuple's indexing and slicing are analogous to lists. The tuple's indexing begins at 0 and ends at length(tuple) - 1.

The index [] operator can be used to access the items in the tuple. The colon operator in Python can also be used to access multiple items in a tuple.

To further comprehend indexing and slicing, look at the image below.

![](Images/image00199.jpeg)

1.  tup = (1,2,3,4,5,6,7)  
2.  print(tup[0])  
3.  print(tup[1])  
4.  print(tup[2])  
5.  # It will give the IndexError  
6.  print(tup[8])  

Output:

1

2

3

tuple index out of range

The tuple in the above code has seven items that represent the numbers 0 through 6\. We attempted to retrieve a non-tuple element, which resulted in an IndexError.

1.  tuple = (1,2,3,4,5,6,7)  
2.  #element 1 to end  
3.  print(tuple[1:])  
4.  #element 0 to 3 element   
5.  print(tuple[:4])  
6.  #element 1 to 4 element  
7.  print(tuple[1:5])   
8.  # element 0 to 6 and take step of 2  
9.  print(tuple[0:6:2])  

Output:

(2, 3, 4, 5, 6, 7)

(1, 2, 3, 4)

(1, 2, 3, 4)

(1, 3, 5)

## Negative Indexing

Negative indexing can also be used to reach the tuple element. The rightmost element has an index of -1, while the second last item has an index of -2, and so on.

Negative indexing is used to navigate the items from left to right. Consider the following illustration:

1.  tuple1 = (1, 2, 3, 4, 5)    
2.  print(tuple1[-1])    
3.  print(tuple1[-4])    
4.  print(tuple1[-3:-1])  
5.  print(tuple1[:-1])  
6.  print(tuple1[-2:])  

Output:

5

2

(3, 4)

(1, 2, 3, 4)

(4, 5)

## Deleting Tuple

Tuple items, unlike lists, cannot be erased with the del keyword because tuples are immutable. We can use the del keyword with the tuple name to delete an entire tuple.

Consider the following illustration.

1.  tuple1 = (1, 2, 3, 4, 5, 6)    
2.  print(tuple1)    
3.  del tuple1[0]    
4.  print(tuple1)    
5.  del tuple1    
6.  print(tuple1)    

Output:

(1, 2, 3, 4, 5, 6)

Traceback (most recent call last):

  File "tuple.py", line 4, in <module>

    print(tuple1)

NameError: name 'tuple1' is not defined

JAVASCRIPT CODING:

BASICS FOR ABSOLUTE BEGINNERS

STEP BY STEP GUIDE TO LEARN CODING QUICKLY

J NEWMAN

Learn JavaScript

JavaScript is a lightweight, cross-platform object-based scripting language.

JavaScript is a translated language, not a compiled language. The JavaScript Translator (which is built within the browser) is in charge of translating JavaScript code for web browsers.

JavaScript (js) is a lightweight object-oriented programming language that is used to script webpages by a number of websites.

When applied to an HTML document, it is an interpreted, full-featured programming language that enables dynamic interactivity on websites. It was first released in 1995 to allow users to add programs to webpages in the Netscape Navigator browser.

Since then, all other graphical web browsers have embraced it. Users can use JavaScript to create modern web applications that interact immediately without having to reload the page every time. Js is used on a standard website to provide many sorts of interactivity and simplicity.

JavaScript, on the other hand, has no connection to the Java programming language.

Features of JavaScript

Because they have built-in execution environments, all popular web browsers support JavaScript.

The grammar and structure of JavaScript are based on the C programming language. As a result, it is classified as a structured programming language.

JavaScript is a weakly typed language with implicit casting of certain types (depending on the operation).

JavaScript is an object-oriented programming language that inherits through prototypes rather than classes.

It's a simple and interpretable language.

The language is case-sensitive.

JavaScript is compatible with a variety of operating systems, including Windows, macOS, and Linux.

It gives consumers complete control over their web browsers.

![](Images/image00200.jpeg)

JavaScript Example

1.  <script>  
2.  document.write("Hello JavaScript by JavaScript");  
3.  </script>  

JavaScript Comment

JavaScript comments are an effective means of conveying information. It's used to include code-related information, such as warnings or suggestions, so that the end user can understand it.

The JavaScript engine, which is incorporated in the browser, ignores the JavaScript comment.

Advantages - JavaScript comments

To make coding more understandable It can be used to explain the code so that the end user can understand it.

To avoid having to write unneeded code It can also be used to prevent the code from running. We sometimes add code to do a certain action. However, the code may need to be disabled after some time. It is preferable to utilise comments in this situation.

JavaScript Comments - Types

1.  Single-line Comment
2.  Multi-line Comment

Single line Comment

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

Multi line Comment

It can be used to create both single and multi-line comments. As a result, it is more practical.

It's symbolised by a forward slash followed by an asterisk, then another forward slash. Consider the following scenario:

1.  /* your code here  */  

It might appear before, after, or in the middle of a statement.

1.  <script>  
2.  /* It is multi line comment.  
3.  It will not be displayed */  
4.  document.write("example of javascript multiline comment");  
5.  </script>  

JavaScript Variable

A JavaScript variable is nothing more than a storage location's name. In JavaScript, there are two sorts of variables: local variables and global variables.

When declaring a JavaScript variable, there are some guidelines to follow (also known as identifiers).

A letter (a to z or A to Z), underscore(_), or dollar($) sign must begin the name.

We can put numerals (0 to 9) after the initial letter, for example value1.

Variables in JavaScript are case sensitive, so x and X are two separate variables.

Correct JavaScript variables

1.  var x = 10;  
2.  var _value="sonoo";  

Incorrect JavaScript variables

1.  var  123=30;  
2.  var *aa=320;  

Example - JavaScript variable

1.  <script>  
2.  var x = 10;  
3.  var y = 20;  
4.  var z=x+y;  
5.  document.write(z);  
6.  </script>  

Output

30

JavaScript local variable

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

JavaScript global variable

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

JavaScript Global Variable

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

Declaring a global variable in JavaScript within a function

You must utilise the window object to declare JavaScript global variables inside a function. Consider the following scenario:

1.  window.value=90;  

It can now be declared within any function and accessed from within any function. Consider the following scenario:

1.  function m(){  
2.  window.value=100;//declaring global variable by window object  
3.  }  
4.  function n(){  
5.  alert(window.value);//accessing global variable from other function  
6.  } 

In JavaScript, the internals of a global variable

When you declare a variable outside of a function, it is automatically added to the window object. You can also use the window object to get to it. Consider the following scenario:

1.  var value=50;  
2.  function a(){  
3.  alert(window.value);//accessing global variable   
4.  } 

Javascript Data Types

Different data types are available in JavaScript to hold various types of values. In JavaScript, there are two sorts of data types.

1.  Primitive data type
2.  Non-primitive (reference) data type

JavaScript is a dynamic type language, which means you don't have to specify the type of a variable because the JavaScript engine uses it dynamically. To specify the data type, you must use var. It may store any type of value, including numbers, strings, and so on. Consider the following scenario:

1.  var a=40;//holding number  
2.  var b="Rahul";//holding string  

![](Images/image00201.jpeg)

![](Images/image00202.jpeg)

JavaScript Operators

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

JavaScript Arithmetic Operators

To conduct arithmetic operations on the operands, arithmetic operators are employed. JavaScript arithmetic operators are the operators listed below.

![](Images/image00203.jpeg)

JavaScript Comparison Operators

The comparison operator in JavaScript compares the two operands. The following are the comparison operators:

![](Images/image00204.jpeg)

JavaScript Bitwise Operators

On operands, the bitwise operators perform bitwise operations. The following are the bitwise operators:

![](Images/image00205.jpeg)

JavaScript Logical Operators

JavaScript logical operators are the operators listed below.

![](Images/image00206.jpeg)

JavaScript Assignment Operators

![](Images/image00207.jpeg)

JavaScript Special Operators

![](Images/image00208.jpeg)

JavaScript If-else

![](Images/image00209.jpeg)

JavaScript If statement

Only if expression is true does it assess the content. The if statement in JavaScript has the following signature.

1.  if(expression){  
2.  //content to be evaluated  
3.  }  

![](Images/image00210.jpeg)

EXAMPLE

1.  <script>  
2.  var a=20;  
3.  if(a>10){  
4.  document.write("value of a is greater than 10");  
5.  }  
6.  </script>

OUTPUT

value of a is greater than 10

JavaScript If...else Statement

It determines if the condition is true or false by evaluating the content. The syntax for the if-else statement in JavaScript is shown below.

1.  if(expression){  
2.  //content to be evaluated if condition is true  
3.  }  
4.  else{  
5.  //content to be evaluated if condition is false  
6.  }  

![](Images/image00211.jpeg)

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

If...else if statement – in Javascript

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

JavaScript Switch

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

JavaScript Loops

The for, while, do while, and for-in loops are used to iterate the piece of code in JavaScript. It reduces the size of the code. It's most commonly found in arrays.

1.  for loop
2.  while loop
3.  do-while loop
4.  for-in loop

1) JavaScript For loop

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

2) JavaScript while loop

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

3) Do while loop

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

4) JavaScript for in loop

The JavaScript for in loop is used to cycle through an object's properties.

JavaScript Functions

To conduct operations, JavaScript functions are needed. To reuse the code, we can call the JavaScript function many times.

Benefits of Using JavaScript

JavaScript functions have primarily two advantages.

Reusability of code: Because we can call a function multiple times, we can save time coding.

Less coding means our program is more compact. To accomplish a common task, we don't need to write many lines of code each time.

JavaScript Function Syntax

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

JavaScript Function Arguments

1.  <script>  
2.  function getcube(number){  
3.  alert(number*number*number);  
4.  }  
5.  </script>  
6.  <form>  
7.  <input type="button" value="click" onclick="getcube(4)"/>  
8.  </form>  

Function with Return Value

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

JavaScript Function Object

The Function function Object() { [native code] } in JavaScript is used to generate a new Function object. It runs the code on a global scale. When we call the function Object() { [native code] } directly, however, a function is constructed dynamically but insecurely.

Syntax

1.  new Function ([arg1[, arg2[, ....argn]],] functionBody)  

![](Images/image00212.jpeg)

![](Images/image00213.jpeg)

JavaScript Function Object

Example

1.  <script>  
2.  var add=new Function("num1","num2","return num1+num2");  
3.  document.writeln(add(2,5));  
4.  </script>  

Output:

7

Example 2

1.  <script>  
2.  var pow=new Function("num1","num2","return Math.pow(num1,num2)");  
3.  document.writeln(pow(2,3));  
4.  </script>

Output:

8

JavaScript Objects

A javaScript object is a state and behavior-based entity (properties and method). For example, a car, a pen, a bicycle, a chair, a glass, a keyboard, and a monitor.

JavaScript is an object-oriented programming language. In JavaScript, everything is an object.

JavaScript is a template-based language, not a class-based one. To get the object, we don't need to build a class. However, we direct the creation of objects.

![](Images/image00214.jpeg)

![](Images/image00215.jpeg)

EXAMPLE

1.  <script>  
2.  emp={id:102,name:"Shyam Kumar",salary:40000}  
3.  document.write(emp.id+" "+emp.name+" "+emp.salary);  
4.  </script> 

OUTPUT

102 Shyam Kumar 40000

![](Images/image00216.jpeg)

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

![](Images/image00217.jpeg)

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

Defining method - JavaScript Object

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

JavaScript Object Methods

![](Images/image00218.jpeg)

![](Images/image00219.jpeg)

![](Images/image00220.jpeg)

![](Images/image00221.jpeg)

JavaScript Array

A JavaScript array is an object that represents a group of objects of the same type.

In JavaScript, there are three ways to create an array.

1.  By array literal
2.  By creating instance of Array directly (using new keyword)
3.  By using an Array constructor (using new keyword)

1) JavaScript array literal

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

2) JavaScript Array directly 

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

3) JavaScript array constructor

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

JavaScript Array Methods

![](Images/image00222.jpeg)

![](Images/image00223.jpeg)

![](Images/image00224.jpeg)

![](Images/image00225.jpeg)

![](Images/image00226.jpeg)

JavaScript String

A string in JavaScript is an object that represents a string of characters.

In JavaScript, there are two ways to make a string.

1.  By string literal
2.  By string object (using new keyword)

1) By string literal

Double quotations are used to construct the string literal. The following is the syntax for creating a string using a string literal:

1.  var stringname="string value";  

EXAMPLE

1.  <script>  
2.  var str="This is string literal";  
3.  document.write(str);  
4.  </script> 

Output:

This is string literal

2) By string object (using new keyword)

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

JavaScript String Methods

![](Images/image00227.jpeg)

![](Images/image00228.jpeg)

![](Images/image00229.jpeg)

JavaScript Date Object

You may get the year, month, and day using the JavaScript date object. The JavaScript date object can be used to display a timer on a webpage.

To generate a date object, you can use a variety of Date constructors. It has methods for retrieving and setting the day, month, year, hour, minute, and second.

Constructor

4 variant of Date constructor

1.  Date()
2.  Date(milliseconds)
3.  Date(dateString)
4.  Date(year, month, day, hours, minutes, seconds, milliseconds)

JavaScript Date Methods

![](Images/image00230.jpeg)

![](Images/image00231.jpeg)

![](Images/image00232.jpeg)

![](Images/image00233.jpeg)

![](Images/image00234.jpeg)

JavaScript Date Example

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

JavaScript Current Time Example

1.  Current Time: <span id="txt"></span>  
2.  <script>  
3.  var today=new Date();  
4.  var h=today.getHours();  
5.  var m=today.getMinutes();  
6.  var s=today.getSeconds();  
7.  document.getElementById('txt').innerHTML=h+":"+m+":"+s;  
8.  </script>

Digital Clock Example

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

JavaScript Math

To conduct mathematical operations, the JavaScript math object exposes various constants and methods. It does not have constructors, unlike the date object.

JavaScript Math Methods

![](Images/image00235.jpeg)

![](Images/image00236.jpeg)

![](Images/image00237.jpeg)

Math.sqrt(n)

The square root of a number is returned by the JavaScript math.sqrt(n) method.

1.  Square Root of 17 is: <span id="p1"></span>    
2.  <script>    
3.  document.getElementById('p1').innerHTML=Math.sqrt(17);    
4.  </script>  

Output:

Square Root of 17 is: 4.123105625617661

Math.random()

The math.random() method in JavaScript returns a random number between 0 and 1.

1.  Random Number is: <span id="p2"></span>    
2.  <script>    
3.  document.getElementById('p2').innerHTML=Math.random();    
4.  </script> 

Output:

Random Number is: 0.02157876559753591

Math.pow(m,n)

1.  3 to the power of 4 is: <span id="p3"></span>    
2.  <script>    
3.  document.getElementById('p3').innerHTML=Math.pow(3,4);    
4.  </script>

Output:

3 to the power of 4 is: 81

Math.floor(n)

The JavaScript math.floor(n) method returns the number's lowest integer. For instance, 3 for 3.7, 5 for 5.9, and so on.

1.  Floor of 4.6 is: <span id="p4"></span>    
2.  <script>    
3.  document.getElementById('p4').innerHTML=Math.floor(4.6);    
4.  </script>  

Output:

Floor of 4.6 is: 4

Math.ceil(n)

The math.ceil(n) method in JavaScript returns the largest integer for a given value. For instance, 4 for 3.7, 6 for 5.9, and so on.

1.  Ceil of 4.6 is: <span id="p5"></span>    
2.  <script>    
3.  document.getElementById('p5').innerHTML=Math.ceil(4.6);    
4.  </script> 

Output:

Ceil of 4.6 is: 5

Math.round(n)

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

JavaScript Number Object

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

JavaScript Number Constants

![](Images/image00238.jpeg)

JavaScript Number Methods

![](Images/image00239.jpeg)

JavaScript Boolean

A Boolean object in JavaScript represents a value in one of two states: true or false. The Boolean() function Object() { [native code] } in JavaScript can be used to build a JavaScript Boolean object, as seen below.

1.  Boolean b=new Boolean(value);  

JavaScript Boolean Example

1.  <script>  
2.  document.write(10<20);//true  
3.  document.write(10<5);//false  
4.  </script>

Boolean Properties

![](Images/image00240.jpeg)

Boolean Methods

![](Images/image00241.jpeg)