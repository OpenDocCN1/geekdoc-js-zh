![](Image00010.jpg)

LEARN PYTHON

QUICKLY

AND

JAVASCRIPT CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

WITH HANDS ON PROJECTS

BY

J J TAM

[LEARN PYTHON QUICKLY](#text00003.html__Toc82326971)

[Python: Hello World program](#text00004.html__Toc82326972)

[Python interactive command line](#text00005.html__Toc82326973)

[Python: Operators](#text00006.html__Toc82326974)

[Arithmetic Operators in python](#text00007.html__Toc82326975)

[Relational Operators in python](#text00007.html__Toc82326976)

[Assignment operators in python](#text00007.html__Toc82326977)

[Logical Operators in python](#text00007.html__Toc82326978)

[Bitwise Operators in python](#text00007.html__Toc82326979)

[Membership operators in python](#text00007.html__Toc82326980)

[Identity operators in python](#text00007.html__Toc82326981)

[Python: Short circuit operators](#text00007.html__Toc82326982)

[Strings in python](#text00008.html__Toc82326983)

[Python: if condition](#text00009.html__Toc82326984)

[Python: while statement](#text00010.html__Toc82326985)

[Python: for statement](#text00011.html__Toc82326986)

[Python: break statement](#text00012.html__Toc82326987)

[Python: continue statement](#text00013.html__Toc82326988)

[Python: functions](#text00014.html__Toc82326989)

[Python: functions: return statement](#text00015.html__Toc82326990)

[Python lists](#text00016.html__Toc82326991)

[Python: tuples](#text00017.html__Toc82326992)

[Python: Class Vs Instance variables](#text00018.html__Toc82326993)

[Python: Inheritance](#text00019.html__Toc82326994)

[Python: Exceptions](#text00020.html__Toc82326995)

[Python: Handling Exceptions](#text00020.html__Toc82326996)

[Python global keyword](#text00020.html__Toc82326997)

[Python: Get type of variable](#text00021.html__Toc82326998)

[JAVASCRIPT CODING EXERCISES](#text00023.html__Toc82326999)

[JavaScript functions – Exercises](#text00023.html__Toc82327000)

[JavaScript: Find the first not repeated character](#text00023.html__Toc82327001)

[JavaScript: Find the longest word within a string](#text00024.html__Toc82327002)

[JavaScript: Counts the number of vowels within a string](#text00025.html__Toc82327003)

[JavaScript: Check a number is prime or not](#text00026.html__Toc82327004)

[JavaScript: Get the data type](#text00027.html__Toc82327005)

[JavaScript: Find the second lowest and second greatest](#text00028.html__Toc82327006)

[JAVASCRIPT BASICS](#text00029.html__Toc82327007)

[Calculate multiplication and division](#text00029.html__Toc82327008)

[Convert temperatures](#text00030.html__Toc82327009)

[Find the largest](#text00031.html__Toc82327010)

[Reverse a given string](#text00032.html__Toc82327011)

[Replace every character](#text00033.html__Toc82327012)

[Create a new string](#text00034.html__Toc82327013)

[Concatenate two strings](#text00035.html__Toc82327014)

[Move last three character](#text00036.html__Toc82327015)

[Compute the sum](#text00037.html__Toc82327016)

[Add two digits](#text00038.html__Toc82327017)

[Check whether a given year is a leap](#text00039.html__Toc82327018)

[Check given positive number](#text00040.html__Toc82327019)

[Check a string starts with 'Java'](#text00041.html__Toc82327020)

[Check two given integer values](#text00042.html__Toc82327021)

[Find a value which is nearest to 100](#text00043.html__Toc82327022)

[OUR OTHER PUBLISHING](#text00044.html__Toc82327023)

 LEARN PYTHON

QUICKLY

CODING FOR BEGINNERS

WITH HANDS ON PROJECTS

BY

J J TAM

# LEARN PYTHON QUICKLY

Well it is almost 5 years I started my IT career, I love to work in Java, and explore open source packages. Now a day I felt bored to work in Java, so want to learn new language, one of my friend suggested me to learn python. Immediately I thought, why should I learn python?

Following are some of the reasons that forced me to learn python…(First and best reason is I am fed up in working with same language for 5 years……….:))

a.   Python is open source and is available on Windows, Mac OS X, and Unix operating systems. You can download and work with python for free.

b.   Python is fun to experiment and easy to learn. Python provides interpreter that can be used interactively, which makes it easy to experiment with features of the language.

c.    You can extend the python interpreter with new functions and data types implemented in C or C++

d.   Python improves developer productivity many times as compared to C, C++ and Java.

e.   No need to compile python program, it runs immediately after development.

f.     We can easily port python project from one platform to another (Of course Java also provides this feature)

g.   Rich in built library. Many third party open source libraries are available for logging, web development (Django — the popular open source web application framework written in Python), networking, database access etc.

h.   Python has very great community, whatever the problem you faced in python, you will get quick help.

# Python: Hello World program

Open any text editor and copy the statement “print ('hello world')” and save the file name as hello.py.

hello.py

print ('hello world')

Open terminal (or) command prompt, use the command ‘python3 hello.py’ to run the file hello.py. You will get output like below

$ python3 hello.py

hello world

What happens when you instruct python to run your script?

Python first compiles your source code to byte code and sends it to python virtual machine (PVM). Byte code is the platform independent representation of your source code. PVM reads the byte code one by one and execute them.

![https://2.bp.blogspot.com/-4SrPn1e0H1A/VmFSCiufP1I/AAAAAAAACtw/bnSNuKricpw/s400/python%2Bexecution%2Bprocess.png](Image00000.jpg)

Note:
Byte code is not machine understandable code, it is python specific representation.

# Python interactive command line

Open command prompt (or) terminal and type ‘python3’ command. It opens python interactive session.

$ python3

Python 3.5.0 (v3.5.0:374f501f4567, Sep 12 2015, 11:00:19)

[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin

Type "help", "copyright", "credits" or "license" for more information.

>>>

How to exit from python interpreter

On Windows, a Ctrl-Z gets you out of this session; on Unix, try Ctrl-D instead. Another way is simply call the quit() function to quit from python.

$ python3

Python 3.5.0 (v3.5.0:374f501f4567, Sep 12 2015, 11:00:19)

[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin

Type "help", "copyright", "credits" or "license" for more information.

>>> quit()

$

You can type any statement (or) expressions in python interpreter, interpreter execute those statements and gives you the result.

>>> 10+20

30

>>> 20*20

400

>>> print('Hello World')

Hello World

Note:

On Unix, the Python 3.x interpreter is not installed by default with name python, so that it does not conflict with other installed Python 2.x executable.

# Python: Operators

An operator is a symbol, which perform an operation. Following are the operators that python supports.

Arithmetic Operators

Relational Operators

Assignment Operators

Logical Operators

Bitwise Operators

Membership Operators

Identity Operators

# Arithmetic Operators in python

Following are the arithmetic operators supported by python.

| Operator | Description | Example |
| + | Addition | 2+3 |
| - | Subtraction | 2-3 |
| * | Multiplication | 2*3 |
| / | Division always returns a float value. To get only integer result use //. | 2/3 returns 0.6666666666666666 |
| // | Floor division discards the fractional part | 2//3 returns 0 |
| % | Returns the remainder of the division. | 2%3 |
| ** | Power | 2**3 returns 2 power 3  = 8 |

>>> 4 + 2

6

>>> 4 - 2

2

>>> 4 / 2

2.0

>>> 4 * 2

8

>>> 4 // 2

2

>>> 4 ** 2

16

# Relational Operators in python

Relational operators determine if one operand is greater than, less than, equal to, or not equal to another operand.

| Operator | Description | Example |
| == | Equal to | a==b returns true if a is equal to b, else false |
| != | Not equal to | a!=b returns true if a is not equal to b, else false. |
| >  | Greater than | a>b returns true, if a is > b, else false. |
| >= | Greater than or equal to | a>=b returns true, if a is >= b, else false. |
| <  | Less than | a<b returns true, if a is < b, else false. |
| <= | Less than or equal to | a<=b returns true, if a is <= b, else false. |

>>> a = 10

>>> b = 12

>>> a = = b

False

>>> a ! = b

True

>>> a > b

False

>>> a > = b

False

>>> a < b

True

>>> a < = b

True

>>>

# Assignment operators in python

Assignment operators are used to assign value to a variable. Following are the assignment operators provided by python.

| Operator | Description |
| = | a=10 assigns 10 to variable a |
| += | a+=10 is same as a=a+10 |
| -= | a-=10 is same as a=a-10 |
| *= | a*=10 is same as a=a*10 |
| /= | a/=10 is same as a=a/10 |
| //= | a//=10 is same as a=a//10 |
| %= | a%=10 is same as a=a%10 |
| **= | a**=10 is same as a=a**10 |

>>> a = 10

>>> a

10

>>>

>>> a += 10

>>> a

20

>>>

>>> a -= 10

>>> a

10

>>>

>>> a *= 10

>>> a

100

>>>

>>> a /= 10

>>> a

10.0

>>>

>>> a //= 10

>>> a

1.0

>>>

>>> a **= 10

>>> a

1.0

Multiple Assignments

You can assign values to multiple variables simultaneously.

>>> a, b, c = 1 0 , 'hello ' , 12.345

>>> a

10

>>> b

'hello'

>>> c

12.345

# Logical Operators in python

Following are the logical operators supported by python.

| Operator | Description |
| and | ‘a and b’ returns true if both a, b are true. Else false. |
| or | ‘a or b’ return false, if both a and b are false, else true. |
| not | ‘not a’ Returns True if a is false, true otherwise |

>>> a = bool ( 0 )

>>> b = bool ( 1 )

>>>

>>> a

False

>>> b

True

>>>

>>> a an d b

False

>>>

>>> a o r b

True

>>>

>>> no t a

True

>>>

>>> no t (a an d b)

True

>>>

>>> no t ( a o r b)

False

# Bitwise Operators in python

Python supports following bitwise operators, to perform bit wise operations on integers.

| Operator | Description |
| >>  | bitwise right shift |
| <<  | bitwise left shift |
| & | bitwise and |
| ^ | Bitwise Ex-OR |
| &#124; | Bitwise or |
| ~ | Bitwise not |

Following post, explains bitwise operators clearly.

http://self-learning-java-tutorial.blogspot.in/2014/02/bit-wise-operators.html

>>> a = 2

>>> a >> 1

1

>>>

>>> a << 1

4

>>>

>>> a & 3

2

>>> a | 3

3

>>>

>>> ~ a

-3

# Membership operators in python

Membership operators are used to test whether a value or variable is found in a sequence (string, list, tuple, set and dictionary).

| Operator | Description |
| in | Return true if value/variable is found in the sequence, else false. |
| not in | Return True if value/variable is not found in the sequence, else false |

>>> primeNumbers = [ 2 , 3 , 5 , 7 , 1 1 ]

>>> 2 i n primeNumbers

True

>>> 4 i n primeNumbers

False

>>> 4 no t i n primeNumbers

True

# Identity operators in python

Identity operators are used to compare the memory locations of two objects.

| Operator | Description |
| is | a is b returns true, if both a and b point to the same object, else false. |
| is not | a is not b returns true, if both a and b not point to the same object, else false. |

>>> name 1 = "Hari Krishna"

>>> name 2 = name1

>>> name 3 = "Hari Krishna"

>>> name 4 = "abc"

>>>

>>> name1 i s name2

True

>>> name1 i s name3

False

>>> name1 i s name4

False

>>> name1 i s no t name3

True

# Python: Short circuit operators

Boolean operators and, or are called short circuit operators, it Is because evaluation of expression stops, whenever the outcome determined.

Why Boolean and is called short circuit operator?

Since if the first statement in the expression evaluates to false, then python won't evaluates the entire expression. So boolean and is called short circuit and.

Why Boolean OR is called short circuit operator?

Since if the first statement evaluates to true, then Python won't evaluates the entire expression.

# Strings in python

String is a sequence of character specified in single quotes('…'), double quotes("…"), (or) triple quotes ("""…"""  or ''' …  '''). Strings in python are immutable, i.e., an object with a fixed value.

>>> str 1 = 'Hello World'

>>> str 2 = "Hello World"

>>> str 3 = """Hello

... World

... """

>>> str1

'Hello World'

>>> str2

'Hello World'

>>> str3

'Hello\nWorld\n'

Special characters are escaped with backslash.

>>> messag e = 'He don \' t know about this'

>>> message

"He don't know about this"

‘print’ method treat characters preceded by \ (backslash) as special characters.

>>> prin t ( 'firstline \n secondline ' )

firstline

secondline

As you observe output, \n prints new line. If you don’t want characters prefaced by \ to be interpreted as special characters, you can use raw strings by adding an r before the first quote

>>> prin t ( r'firstline\nsecondline ' )

firstline\nsecondline

Concatenate strings

'+' operator is used to concatenate strings.

>>> hell o = "Hello,"

>>> messag e = "How are you"

>>> inf o = hell o + message

>>> info

'Hello,How are you'

Two or more string literals next to each other are automatically concatenated.

>>> 'Hello ' "How " 'are ' 'you'

'HelloHowareyou'

Repeat strings

By using ‘*’, we can repeat the strings.

>>> 'hi' * 2

'hihi'

>>> 'hi' * 2 + 'hello' * 3

'hihihellohellohello'

Access specific character from strings

You can access, specific character of string using index position.

>>> nam e = "Hello World"

>>> name [ 0 ]

'H'

>>> name [ 6 ]

'W'

Index 0 represents 1 st  character, 1 represents 2 nd  character etc.,

You can also use negative numbers for indexing.

-1 represents last character; -2 represents second-last character etc.,

>>> name

'Hello World'

>>> name [ - 1 ]

'd'

>>> name [ - 2 ]

'l'

>>> name [ - 7 ]

'o'

Slicing

Slicing is used to get sub string of given string.

| Example | Description |
| string[start:end] | Returns sub string from index start (included) to end index (excluded). |
| string[:end] | Returns sub string from index 0(included) to end index (excluded). |
| string[start:] | Return sub string from index start to till end. |
| string[-2:] | Return characters from 2 nd  last to end. |

>>> messag e = "Hello World"

>>>

>>> message [ 0 : 5 ]

'Hello'

>>> message [ 5 :]

' World'

>>> message[:]

'Hello World'

>>> message [ - 2 :]

'ld'

>>> message [ - 5 : - 2 ]

'Wor'

Get length of the string

Function ‘len(str)’ is used to get the length of the string.     

>>> message

'Hello World'

>>> len(message)

11

>>> len ( "How are you " )

11

# Python: if condition

“if” statement

"if" tell the program execute the section of code when the condition evaluates to true.

Syntax

if_stmt ::=  "if" expression ":" suite

test.py

a = 10

if (a < 10 ) :

  print ( "a is less than 10" )

if (a == 10 ) :

  print ( "a is equal to 10" )

if ( a > 10 ) :

  print ( "a is greater than 10" )

$ python3 test.py

a is equal to 10

if-else statement

If the condition true, then if block code executed. other wise else block code executed.

Syntax

if_stmt ::=  "if" expression ":" suite

                   ["else" ":" suite]

test.py

a = 10

if (a != 10 ) :

  print ( "a is not equal to 10" )

else :

  print ( "a is equal to 10" )

if-elif-else statement

By using if-elif-else construct, you can choose number of alternatives. An if statement can be followed by an optional elif...else statement.

Syntax

if_stmt ::=  "if" expression ":" suite

             ( "elif" expression ":" suite )*

             ["else" ":" suite]

test.py

a = 10

if (a > 10 ) :

  print ( "a is greater than 10" )

elif (a < 10 ) :

  print ( "a is less than 10" )

else :

  print ( "a is equal to 10" )

$ python3 test.py

a is equal to 10

Note:

a. In python, any non-zero integer value is treated as true; zero is false.

test.py

if ( 100 ) :

  print ( "Hello" )

else :

  print ( "Bye" )

$ python3 test.py

Hello

b. Any sequence (string, list etc.,) with a non-zero length is true, empty sequences are false.

test.py

list = []

data = "abc"

if ( list ) :

  print ( "list is not empty" )

else :

  print ( "list is empty" )

if (data) :

  print ( "data is not empty" )

else :

  print ( "data is empty" )

$ python3 test.py

list is empty

data is not empty

# Python: while statement

‘while’ statement executes a block of statements until a particular condition is true

Syntax

while_stmt ::=  "while" expression ":" suite

                           ["else" ":" suite]

‘else’ clause is optional. If the expression evaluates to false, then else clause will execute (if else present), and terminates.

test.py

a = 2

prin t ( "Even numbers are " )

while (a < 10 ) :

  print (a, end = ' ' )

a += 2

else :

  print ( " \n Exit from loop" )

prin t ( "Done " )

$ python3 test.py

Even numbers are

2 4 6 8

Exit from loop
Done

# Python: for statement

Python’s for statement is used to iterate over the items of any sequence like a list, string.

Syntax

for_stmt ::=  "for" target_list "in" expression_list ":" suite

              ["else" ":" suite]

‘else’ clause is optional, it is executes, once the loop terminates.

test.py

name s = [ "Phalgun " , "Sambith " , "Mahesh " , "swapna " ]

for name in names:

  print (name)

else :

  print ( "Exiting from loop" )

prin t ( "Finsihed Execution " )

$ python3 test.py

Phalgun

Sambith

Mahesh

swapna

Exiting from loop

Finsihed Execution

# Python: break statement

'break' statement is used to come out of loop like for, while.

test.py

i = 0

while ( 1 ):

i += 2

  print (i)

  if (i == 10 ):

  break

else :

  print ( "Exiting loop" )

print ( "Finished Execution " )

$ python3 test.py

2

4

6

8

10

Finished Execution

As you observe the output, print statement in else clause is not printed. It is because, else clause will not execute, when a break statement terminates the loop.

# Python: continue statement

‘continue’ statement skips the current iteration of loops like for, while.

test.py

i = 2

while (i < 20 ):

i += 2

  if (i % 2 != 0 ):

  continue

  print (i)

else :

  print ( "Exiting loop" )

print ( "Finished Execution " )

Above program prints all the even numbers up to 20 (exclusive).

$ python3 test.py

4

6

8

10

12

14

16

18

20

Exiting loop

Finished Execution

# Python: functions

A function is a block of statements identified by a name. The keyword 'def' is used to define a function. Functions are mainly used for two reasons.

a .      To make code easier to build and understand

b .      To reuse the code

Syntax

def functionName(argument1, argument2 …. argumentN):

test.py

def factorial (n):

  if (n <= 1 ):

  return 1

resul t = 1

  for i in range ( 2 , n + 1 ):

  result *= i

  return result

print(factorial ( 1 ))

print(factorial ( 2 ))

print(factorial ( 3 ))

print(factorial ( 4 ))

print(factorial ( 5 ))

$ python3 test.py

1

2

6

24

120

Variables created before function definition may be read inside of the function only if the function does not change the value.

test.py

# Create the x variable and set to 44

x = 44

# Define a simple function that prints x

def f ():

x += 1

  print (x)

# Call the function

f()

Run above program, you will get following error.

$ python3 test.py

Traceback (most recent call last):

  File "test.py", line 11, in <module>

    f()

  File "test.py", line 7, in f

    x += 1

UnboundLocalError: local variable 'x' referenced before assignment

Remove ‘x+=1’ statement and re run the above program, value of x is printed to console.

# Python: functions: return statement

‘return’ statement is used to return a value from function to the caller.

test.py

def factorial (n):

  if (n <= 1 ):

  return 1

resul t = 1

  for i in range ( 2 , n + 1 ):

  result *= i

  return result

print(factorial ( 1 ))

print(factorial ( 2 ))

print(factorial ( 3 ))

print(factorial ( 4 ))

print(factorial ( 5 ))

$ python3 test.py

1

2

6

24

120

‘return’ without an expression argument returns None.

def hello():

         print("Hello")

print(hello())

$ python3 test.py

Hello
None

# Python lists

List is group of values in between square brackets separated by commas.

>>> prime s = [ 2 , 3 , 5 , 7 , 1 1 , 1 3 , 1 7 , 1 9 , 2 3 ]

>>> primes

[2, 3, 5, 7, 11, 13, 17, 19, 23]

‘primes’ is a list that contain prime numbers.

>>> student s = [ "Hari " , "Krishna " , "Kiran " , "Ravi " ]

>>> students

['Hari', 'Krishna', 'Kiran', 'Ravi']

‘students’ is a list that contain all student names.

List can contain any type of data.

>>> object s = [ 1 , 3 , "Hello " , 10.2 3 ]

>>> objects

[1, 3, 'Hello', 10.23]

You can access elements of list by using index.

>>> objects

[1, 3, 'Hello', 10.23]

>>> objects [ 0 ]

1

>>> objects [ 2 ]

'Hello'

objects[0] return the first element of list objects.

objects[1] return the second element of list objects.

-ve indexes also used to access elements of a list.

>>> objects

[1, 3, 'Hello', 10.23]

>>> objects [ - 1 ]

10.23

>>> objects [ - 3 ]

3

Slicing

Slicing is used to get sub list.

| Example | Description |
| list[start:end] | Returns sub list from index start (included) to end index (excluded). |
| list[:end] | Returns sub list from index 0(included) to end index (excluded). |
| list[start:] | Return sub list from index start to till end. |
| list[-2:] | Return list from 2 nd  last to end. |

>>> objects

[1, 3, 'Hello', 10.23]

>>> objects [ - 1 ]

10.23

>>> objects [ - 3 ]

3

>>> objects

[1, 3, 'Hello', 10.23]

>>>

>>> objects[:]

[1, 3, 'Hello', 10.23]

>>>

>>> objects [ 2 :]

['Hello', 10.23]

>>>

>>> objects[ : 3 ]

[1, 3, 'Hello']

>>>

>>> objects [ - 2 :]

['Hello', 10.23]

Concatenate two lists

'+' Operator is used to concatenate two lists.

>>> eve n = [ 2 , 4 , 6 , 8 , 1 0 ]

>>> od d = [ 1 , 3 , 5 , 7 , 9 ]

>>> numbers = eve n + odd

>>> numbers

[2, 4, 6, 8, 10, 1, 3, 5, 7, 9]

Lists are mutable; you can change the values of list.    

>>> numbers

[2, 4, 6, 8, 10, 1, 3, 5, 7, 9]

>>> numbers [ 0 ] = 12

>>> numbers [ 1 ] = 14

>>> numbers

[12, 14, 6, 8, 10, 1, 3, 5, 7, 9]

Add elements to end of list

List provides ‘append’ method to add new elements to the end of a list.    

>>> numbers

[12, 14, 6, 8, 10, 1, 3, 5, 7, 9]

>>>

>>> number s . append ( 1 1 )

>>> number s . append ( 1 3 )

>>>

>>> numbers

[12, 14, 6, 8, 10, 1, 3, 5, 7, 9, 11, 13]

Assignment to slices

If you want to replace sequence of elements in a list, you can use slice notation.

numbers[2:5] = [21, 22, 23]

Above statement replace elements at index 2, 3, 4 with 21, 22, 23 respectively.

numbers[:] = []

Above statement clear the list by replacing all the elements with an empty list. 

>>> numbers

[12, 14, 6, 8, 10, 1, 3, 5, 7, 9, 11, 13]

>>>

>>> numbers [ 2 : 5 ] = [ 2 1 , 2 2 , 2 3 ]

>>> numbers

[12, 14, 21, 22, 23, 1, 3, 5, 7, 9, 11, 13]

>>>

>>> numbers[:] = []

>>> numbers

[]

Get length of the list

By using ‘len’ function, you can get the length of the list.

>>> vowel s = [ 'a ' , 'e ' , 'i ' , 'o ' , 'u ' ]

>>> len(vowels)

5

Nested lists

A list can be nested in other list. For example, in below example, numbers contains 3 lists, first list represent odd numbers, second list represent even numbers and third list represent prime numbers.

>>> number s = [ [ 1 , 3 , 5 , 7 ], [ 2 , 4 , 6 , 8 ], [ 2 , 3 , 5 , 7 , 1 1 ]]

>>> numbers

[[1, 3, 5, 7], [2, 4, 6, 8], [2, 3, 5, 7, 11]]

>>>

>>> numbers [ 0 ]

[1, 3, 5, 7]

>>>

>>> numbers [ 1 ]

[2, 4, 6, 8]

>>>

>>> numbers [ 2 ]

[2, 3, 5, 7, 11]

>>>

>>>

>>> len(numbers)

3

>>> len(numbers [ 0 ])

4

>>> len(numbers [ 1 ])

4

>>> len(numbers [ 2 ])

5

>>>

>>> numbers [ 0 ] [ 1 ] = 9

>>> numbers [ 1 ] [ 1 : 4 ] = [ 1 0 , 1 2 , 1 4 ]

>>> numbers

[[1, 9, 5, 7], [2, 10, 12, 14], [2, 3, 5, 7, 11]]

# Python: tuples

A tuple is just like a list, consist of number of values separated by commas.

Differences between tuple and list

a .      List is mutable, where as tuple is immutable

b .      Tuple can contain heterogeneous data, where as list usually contains homogeneous data.

test.py

employe e = ( 1 , "Hari Krihsna " , "Gurram " , 12345.67 8 )

print(employee)

print(employee [ 0 ])

print(employee [ 1 ])

print(employee [ 2 ])

print(employee [ 3 ])

$ python3 test.py

(1, 'Hari Krihsna', 'Gurram', 12345.678)

1

Hari Krihsna

Gurram

12345.678

As you observe above example, elements in tuple are enclosed in parenthesis. Eventhough tuples are immutable, you can create tuples which contain mutable objects, such as lists.

test.py

employe e = ( 1 , [])

print(employee)

employee[ 1 ] . append( 2 )

employee[ 1 ] . append( 4 )

employee[ 1 ] . append( 6 )

print(employee)

$ python3 test.py

(1, [])

(1, [2, 4, 6])

Packing and unpacking

You can define tuples, without using parenthesis.

For example,

employee=1, "Hari Krihsna", "Gurram", 12345.678

Above one is the example of tuple packing.

id, firstName, lastName, salary = employee

Above one is an example of tuple unpacking. Sequence unpacking requires that there are as many variables on the left side of the equals sign as there are elements in the sequence.

test.py

employe e = 1 , "Hari Krihsna " , "Gurram " , 12345.678

id, firstName, lastName, salary = employee

print(id)

print(firstName)

print(lastName)

print(salary)

$ python3 test.py

1

Hari Krihsna

Gurram

12345.678

Concatenate tuples

‘+’ operator is used to concatenate tuples.

>> > tuple 1 = ( 1 , "HI " , 2 , 45.6 5 )

>> > tuple 2 = ( "abcdef " , 5 4 , 6 7 )

>> > tuple 3 = tuple 1 + tuple2

>>> tuple3

( 1 , 'HI' , 2 , 45.65 , 'abcdef' , 54 , 67 )

Slicing

Just like lists, you can access tuples using slice notation.

| Example | Description |
| tuple[start:end] | Returns tuple from index start (included) to end index (excluded). |
| tuple[:end] | Returns tuple from index 0(included) to end index (excluded). |
| tuple[start:] | Return tuple from index start to till end. |
| tuple[-2:] | Return elements from 2 nd  last to end. |

>>> tuple1

(1, 'HI', 2, 45.65)

>>> tuple1 [ 0 :]

(1, 'HI', 2, 45.65)

>>> tuple1[:]

(1, 'HI', 2, 45.65)

>>> tuple1[ : 3 ]

(1, 'HI', 2)

>>> tuple1 [ 2 : 5 ]

(2, 45.65)

‘*’: Repeat tuple elements

‘*’  is the repetition operator, used to repeat the elements of tuple.

>>> tuple1

(1, 'HI', 2, 45.65)

>>>

>>> tuple 1 * 3

(1, 'HI', 2, 45.65, 1, 'HI', 2, 45.65, 1, 'HI', 2, 45.65)

>>>

Remove tuple elements

As I said, tuples are immutable, so it is not possible to remove elements from tuple. But you can remove the entire tuple using del statement.

>>> tuple 1 = ( 1 , "HI " , 2 , 45.6 5 )

>>>

>>> de l tuple1

>>> tuple1

Traceback (most recent call last):

  File "<stdin>" , line 1 , in <module>

NameErro r : name 'tuple1' is not defined

Observe the output, an exception raised; this is because after deletion, tuple does not exist any more.

# Python: Class Vs Instance variables

Class variables are associated with class and available to all the instances (objects) of the class, where as instance variables are unique to objects, used to uniquely identify the object.

Employee.py

class Employee :

  """ Blue print for all employees """

  # Class level variables

noOfEmployees = 0

organization = "abcde corporation"

  def __init__ ( self , id =- 1 , firstName = "Nil" , lastName = "Nil" ):

  self . id = - 1

  self . firstName = firstName

  self . lastName = lastName

  Employee . noOfEmployees += 1

  def displayEmployee ( self ):

  print ( self . id, self . firstName, self . lastName)

emp1 = Employee( id = 1 , firstName = "Hari Krishna" , lastName = "Gurram" )

emp1 . displayEmployee()

print ( "Total Employees : " , Employe e . noOfEmployees)

print ( "Organization : " , Employe e . organization)

emp2 = Employee( id = 3 , firstName = "PTR" )

emp2 . displayEmployee()

print ( "Total Employees : " , Employe e . noOfEmployees)

print ( "Organization : " , Employe e . organization)

$ python3 Employee.py

-1 Hari Krishna Gurram

Total Employees :  1

Organization :  abcde corporation

-1 PTR Nil

Total Employees :  2

Organization :  abcde corporation

# Python: Inheritance

Inheritance is the concept of re usability.

Object of one class can get the properties and methods of object of another class by using inheritance.

Syntax

class DerivedClassName (BaseClassName1, BaseClassName2 ... BaseClassNameN):

    < statement - 1 >

    .

    .

    .

    < statement - N >

inheritance.py

class Parent :

  def printLastName ( self ):

  print ( "Gurram" )

  def printPermAddress ( self ):

  print ( "State : Andhra Pradesh" )

  print ( "Country : India" )

class Child (Parent):

  def printName ( self ):

  print ( "Hari Krishna Gurram" )

child1 = Child()

child1 . printName()

child1 . printLastName()

child1 . printPermAddress()

$ python3 inheritance.py

Hari Krishna Gurram

Gurram

State : Andhra Pradesh

Country : India

Observe above program, two classes parent and child are defined. Parent class defines two methods printLastName, printPermAddress.

Child class defines one method printName.

Child class inheriting the methods printLastName, printPermAddress from parent class.

Overriding the methods of Parent class

You can override the properties, methods of parent class in child class.

For example, following application overrides ‘printPermAddress’ method of Parent class.

inheritance.py

class Parent :

  def printLastName ( self ):

  print ( "Gurram" )

  def printPermAddress ( self ):

  print ( "State : Andhra Pradesh" )

  print ( "Country : India" )

class Child (Parent):

  def printName ( self ):

  print ( "Hari Krishna" )

  def printPermAddress ( self ):

  print ( "City : Bangalore" )

  print ( "State : Karnataka" )

  print ( "Country : India" )

child1 = Child()

child1 . printName()

child1 . printLastName()

child1 . printPermAddress()

$ python3 inheritance.py

Hari Krishna

Gurram

City : Bangalore

State : Karnataka

Country : India

# Python: Exceptions

Exception is an event that disrupts the normal flow of execution.

Even though statements in your program are syntactically correct, they may cause an error.

>>> 10 / 0

Traceback (most recent call last):

  File "<stdin>" , line 1 , in <module>

ZeroDivisionErro r : division by zero

>>>

>>> tempLis t = []

>>> tempList [ 2 0 ]

Traceback (most recent call last):

  File "<stdin>" , line 1 , in <module>

IndexErro r : list index out of range

Observer above snippet, ‘10/0’ causes ZeroDivisionError. When program tries to access 20 th  element of tempList it causes IndexError.

# Python: Handling Exceptions

Python provide keywords try, except to handle exceptions.

test.py

while True :

  try :

  x = int ( input ( "Enter input " ))

  print (x)

  break ;

  except ValueError :

  print ( "Please enter valid number" )

$ python3 test.py

Enter input an

Please enter valid number

Enter input ana

Please enter valid number

Enter input ptr

Please enter valid number

Enter input 10

10

Try block can be followed by multiple except clauses

test.py

while True :

  try :

  x = int ( input ( "Enter divisor " ))

  y = int ( input ( "Enter dividend " ))

  print (x / y)

  break ;

  except ValueError :

  print ( "Please enter valid number" )

  except ZeroDivisionError :

  print ( "y should be non zero" )

$ python3 test.py

Enter divisor 2

Enter dividend 0

y should be non zero

Enter divisor 4

Enter dividend 0

y should be non zero

Enter divisor 4

Enter dividend 2

2.0

Handling multiple exceptions in single except clause

An except clause can catch more than one exception.

For example ‘except (ValueError, ZeroDivisionError)’ can handle both ValueError and ZeroDivisionError.

test.py

while True :

  try :

  x = int ( input ( "Enter divisor " ))

  y = int ( input ( "Enter dividend " ))

  print (x / y)

  break ;

  except ( ValueError , ZeroDivisionError ):

  print ( "Please enter valid number (or) y should be greater than 0" )

$ python3 test.py

Enter divisor 2

Enter dividend 0

Please enter valid number (or) y should be greater than 0

Enter divisor aa

Please enter valid number (or) y should be greater than 0

Enter divisor 2

Enter dividend 4

0.5

Last except clause can omit exception name. It is used as global exception handler.

test.py

while True :

  try :

  tempList = []

  print (tempList[ 10 ])

  break

  except ValueError :

  print ( "Please enter valid number" )

  except ZeroDivisionError :

  print ( "y should be non zero" )

  except Exception as inst:

  print ( "Global handler" , inst)

  break

$ python3 test.py

Global handler list index out of range

try…except…else clause

‘try…except’ statement can have optional else clause, it is followed by except clause. If try block doesn’t throw any exception, else clause will be executed.

test.py

while True :

  try :

  x = int ( input ( "Enter divisor " ))

  y = int ( input ( "Enter dividend " ))

  print (x / y)

  except ValueError :

  print ( "Please enter valid number" )

  except ZeroDivisionError :

  print ( "y should be non zero" )

  else :

  print ( "Program executed successfully" )

  break

$ python3 test.py

Enter divisor 4

Enter dividend 2

2.0

Program executed successfully

Exception argument

Whenever an exception occurs, it is associated with a variable called exception argument.

test.py

while True :

  try :

  x = int ( input ( "Enter divisor " ))

  y = int ( input ( "Enter dividend " ))

  print (x / y)

  except ValueError as inst:

  print (inst)

  except ZeroDivisionError as inst:

  print (inst)

  else :

  print ( "Program executed successfully" )

  break

$ python3 test.py

Enter divisor qwerty

invalid literal for int() with base 10: 'qwerty'

Enter divisor 4

Enter dividend 0

division by zero

Enter divisor 2

Enter dividend 4

0.5

Program executed successfully

The except clause can specify a variable after the exception name. The variable is bound to an exception instance with the arguments stored in instance.args.

test.py

while True :

  try :

  x = int ( input ( "Enter divisor " ))

  y = int ( input ( "Enter dividend " ))

  if y == 0 :

   raise Exception (x, y)

  print ( "x/y = " ,x / y)

  break

  except Exception as inst:

  arg1, arg2 = inst . args

  print ( "arg1=" , arg1)

  print ( "arg2=" , arg2)

$ python3 test.py

Enter divisor 2

Enter dividend 0

arg1= 2

arg2= 0

Enter divisor 2

Enter dividend 4

x/y =  0.5

If an exception has arguments associated with it, those are printed as last part of the exception message.

test.py

while True :

  try :

  x = int ( input ( "Enter divisor " ))

  y = int ( input ( "Enter dividend " ))

  if y == 0 :

   raise Exception (x, y)

  print ( "x/y = " ,x / y)

  break

  except Exception as inst:

  print (inst)

$ python3 test.py

Enter divisor 2

Enter dividend 0

(2, 0)

Enter divisor 2

Enter dividend 4

x/y =  0.5

# Python global keyword

‘global’ keyword is used to create/change a global variables (You can declare functions, classes etc. also) from local context.

test.py

def function1 ():

  global data

data = "Hello World"

def function2 ():

  print (data)

function1()

function2()

$ python3 test.py

Hello World

Observe ‘test.py’, even though data is declared in function1, it is accessed by function2\. It is because, data is declared in global scope.

# Python: Get type of variable

You can get the type of a variable using ‘type()’ function or __class__ property.

>>> dat a = [ 1 , 2 , 3 , 4 ]

>>> type(data)

<class 'list'>

>>> dat a . __class__

<class 'list'>

>>>

>>> dat a = { 1 : "hari " , 2 : "Krishna " }

>>> type(data)

<class 'dict'>

>>> dat a . __class__

<class 'dict'>

Checking the type using if statement

dat a = { 1 : "hari " , 2 : "Krishna " }

#Approach 1

if (data . __class__ . __name__ == 'dict' ):

    print ( "data is of type dictionary" )

else :

    print ( "data is not dictionary type" )

#Approach 2

if ( type (data) . __name__ == 'dict' ):

    print ( "data is of type dictionary" )

else :

    print ( "data is not dictionary type" )

#Approach 3

if type (data) == type ( dict ()):

    print ( "data is of type dictionary" )

else :

    print ( "data is not dictionary type" )

Run above program, you will get following output.

data is of type dictionary

data is of type dictionary

data is of type dictionary

Check whether an object is instance of class or not

‘isinstance(object, classinfo)’ method is used to check whether an object is instance of given class or not.

Return true if the object argument is an instance of the classinfo argument, or of a subclass thereof, else false.

dat a = { 1 : "hari " , 2 : "Krishna " }

class Employee :

    def __init__ ( self , id , firstName, lastName):

     self . id = id

     self . firstName = firstName

     self . lastName = lastName

em p = Employee ( 1 , "Hari " , "Krishna " )

print(isinstance(emp, Employee))

print(isinstance(emp, dict))

print(isinstance(data, dict))

Run above program, you will get following output.

True

False

True

JAVASCRIPT

CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

JJ TAM

JAVASCRIPT CODING EXERCISES

JavaScript functions – Exercises

JavaScript: Find the first not repeated character

Sample arguments  : 'abacddbec'
Expected output  : 'e'

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <title>find the first not repeated character.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

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

OUTPUT

e

FLOWCHART

![](Image00001.jpg)

JavaScript: Find the longest word within a string

Example string : 'Web Development Tutorial'
Expected Output:  'Development'

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>Find the longest word within a string</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function find_longest_word(str)

{

  var array1 = str.match(/\w[a-z]{0,}/gi);

  var result = array1[0];

  for(var x = 1 ; x < array1.length ; x++)

  {

    if(result.length < array1[x].length)

    {

    result = array1[x];

    }

  }

  return result;

}

console.log(find_longest_word('Web Development Tutorial'));

OUTPUT

Development

EXPLANATION

Assume that str equals '@Web Production #Tutorial'.

When a string is matched against a regular expression, the match() method is used to obtain the matches.

As a result of str.match(/w[a-z]0,/gi), ["Web", "Development", "Tutorial"] will be returned.

The for loop compares the length of each array element to the previous one and returns the longest string.

The length property is a 32-bit unsigned integer that is always numerically greater than the array's highest index.

Syntax -> arr.length

FLOWCHART

![](Image00002.jpg)

JavaScript: Counts the number of vowels within a string

Example string : 'The quick brown fox'
Expected Output:  5

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>Counts the number of vowels within a string</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function vowel_count(str1)

{

  var vowel_list = 'aeiouAEIOU';

  var vcount = 0;

  for(var x = 0; x < str1.length ; x++)

  {

    if (vowel_list.indexOf(str1[x]) !== -1)

    {

      vcount += 1;

    }

  }

  return vcount;

}

console.log(vowel_count("The quick brown fox"));

OUTPUT

5

EXPLANATION

The indexOf() method returns the index of the first occurrence of the defined value within the calling String object, starting at fromIndex. If the value cannot be found, it returns -1.

Syntax -> str.indexOf(searchValue[, fromIndex])

Parameters include:

searchValue : A string that represents the value to be sought.

fromIndex(Optional)-> The index at which the string's forward search should begin. Any integer can be used.

If the condition (vowel list.indexOf(str1[x])!== -1) is met, the character(s) of the string will be counted as vowels.

FLOWCHART

![](Image00003.jpg)

JavaScript: Check a number is prime or not

![](Image00004.jpg)

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>Check a number is prime or not</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function test_prime(n)

{

  if (n===1)

  {

    return false;

  }

  else if(n === 2)

  {

    return true;

  }else

  {

    for(var x = 2; x < n; x++)

    {

      if(n % x === 0)

      {

        return false;

      }

    }

    return true; 

  }

}

console.log(test_prime(37));

OUTPUT

True

FLOWCHART

![](Image00005.jpg)

JavaScript: Get the data type

We going to Create a JavaScript function which takes an argument and returns the type.

Note six possible values: object, boolean, method, number, string, or undefined.

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>Detect JavaScript Data Types</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function detect_data_type(value)

{

var dtypes = [Function, RegExp, Number, String, Boolean, Object], x, len;

if (typeof value === "object" || typeof value === "function")

    {

     for (x = 0, len = dtypes.length; x < len; x++)

     {

            if (value instanceof dtypes[x])

            {

                return dtypes[x];

            }

      }

    }

    return typeof value;

}

console.log(detect_data_type(12));

console.log(detect_data_type('w3resource'));

console.log(detect_data_type(false));

OUTPUT

number

string

Boolean

JavaScript: Find the second lowest and second greatest

numbers from an array

![](Image00006.jpg)

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>Find the second lowest and second greatest numbers from an array</title>

</head>

<body>

</body>

JAVASCRIPT CODE

function Second_Greatest_Lowest(arr_num)

{

  arr_num.sort(function(x,y)

           {

           return x-y;

           });

  var uniqa = [arr_num[0]];

  var result = [];

  for(var j=1; j < arr_num.length; j++)

  {

    if(arr_num[j-1] !== arr_num[j])

    {

      uniqa.push(arr_num[j]);

    }

  }

    result.push(uniqa[1],uniqa[uniqa.length-2]);

  return result.join(',');

  }

console.log(Second_Greatest_Lowest([1,2,3,4,5]));

OUTPUT

2,4

FLOWCHART

![](Image00007.jpg)

JAVASCRIPT BASICS

Calculate multiplication and division

of two numbers

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>JavaScript program to calculate multiplication and division of two numbers </title>

<style type="text/css">

body {margin: 30px;}

</style>

</head>

<body>

<form>

1st Number : <input type="text" id="firstNumber" /><br>

2nd Number: <input type="text" id="secondNumber" /><br>

<input type="button" onClick="multiplyBy()" Value="Multiply" />

<input type="button" onClick="divideBy()" Value="Divide" />

</form>

<p>The Result is : <br>

<span id = "result"></span>

</p>

</body>

</html>

JAVASCRIPT CODE

function multiplyBy()

{

        num1 = document.getElementById("firstNumber").value;

        num2 = document.getElementById("secondNumber").value;

        document.getElementById("result").innerHTML = num1 * num2;

}

function divideBy()

{

        num1 = document.getElementById("firstNumber").value;

        num2 = document.getElementById("secondNumber").value;

document.getElementById("result").innerHTML = num1 / num2;

}

EXPLANATION

document.getElementById(id).value: The value property of a text field sets or returns the value of the value attribute.

document.getElementById("result").innerHTM : The innerHTML property of an element sets or returns the HTML content (inner HTML).

OUTPUT

![](Image00008.jpg)

Convert temperatures

To and from celsius, Fahrenheit in JAVASCRIPT

HTML CODE

<!DOCTYPE html>

  <html>

  <head>

  <meta charset="utf-8">

  <title>Write a JavaScript program to convert temperatures to and from celsius, fahrenheit</title>

  </head>

  <body>

</body>

  </html>

JAVASCRIPT CODE

function cToF(celsius)

{

  var cTemp = celsius;

  var cToFahr = cTemp * 9 / 5 + 32;

  var message = cTemp+'\xB0C is ' + cToFahr + ' \xB0F.';

    console.log(message);

}

function fToC(fahrenheit)

{

  var fTemp = fahrenheit;

  var fToCel = (fTemp - 32) * 5 / 9;

  var message = fTemp+'\xB0F is ' + fToCel + '\xB0C.';

    console.log(message);

}

cToF(60);

fToC(45);

OUTPUT

60°C is 140 °F.

45°F is 7.222222222222222°C.

EXPLANATION

The following formulas can be used to make an exact conversion (Fahrenheit to Celsius / Celsius to Fahrenheit):

Fahrenheit to Celsius : (°F − 32) ÷ 1.8 = °C
Celsius to Fahrenheit : (°C × 1.8) + 32 = °F

The following is a rough conversion between degrees Celsius and degrees Fahrenheit:

To convert from Fahrenheit to Celsius, deduct 30 and divide by two.

To convert from Celsius to Fahrenheit, multiply the number by two and add 30.

Find the largest

Of three given integers

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to find the largest of three given integers.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function max_of_three(x, y, z)

{

  max_val = 0;

  if (x > y)

  {

    max_val = x;

  } else

  {

    max_val = y;

  }

  if (z > max_val)

  {

    max_val = z;

  }

  return max_val;

}

console.log(max_of_three(1,0,1));

console.log(max_of_three(0,-10,-20));

console.log(max_of_three(1000,510,440));

Output:

1

0

1000

FLOWCHART

![](Image00009.jpg)

Reverse a given string

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to reverse a given string.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function string_reverse(str)

{

    return str.split("").reverse().join("");

}

console.log(string_reverse("jsresource"));

console.log(string_reverse("www"));

console.log(string_reverse("JavaScript"));

OUTPUT

ecruosersj

www

tpircSavaJ

Replace every character

with the character following it in the alphabet

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to replace every character in a given string with the character following it in the alphabet.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function string_reverse(str)

function LetterChanges(text) {

//https://goo.gl/R8gn7u

var s = text.split('');

for (var i = 0; i < s.length; i++) {

// Caesar cipher

switch(s[i]) {

case ' ':

break;

case 'z':

s[i] = 'a';

break;

case 'Z':

s[i] = 'A';

break;

default:

s[i] = String.fromCharCode(1 + s[i].charCodeAt(0));

}

// Upper-case vowels

switch(s[i]) {

case 'a': case 'e': case 'i': case 'o': case 'u':

s[i] = s[i].toUpperCase();

}

}

return s.join('');

}

console.log(LetterChanges("PYTHON"));

console.log(LetterChanges("W3R"));

console.log(LetterChanges("php"));

Output:

QZUIPO

X4S

qIq

Create a new string  

HTML CODE

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

JAVASCRIPT CODE

function without_first_end(str) {

  return str.substring(1, str.length - 1);

}

console.log(without_first_end('JavaScript'));

console.log(without_first_end('JS'));

console.log(without_first_end('PHP'));

Output:

avaScrip

H

Concatenate two strings

Except their first character

HTML CODE

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

JAVASCRIPT CODE

function concatenate(str1, str2) {

  str1 = str1.substring(1, str1.length);

  str2 = str2.substring(1, str2.length);

  return str1 + str2;

}

console.log(concatenate("PHP","JS"));

console.log(concatenate("A","B"));

console.log(concatenate("AA","BB"));

Output:

HPS

AB

Move last three character

start of a specified string

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to move last three character to the start of a given string. The string length must be 3.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function right_three(str) {

     if (str.length > 1)

       {

         return str.slice(-3) + str.slice(0, -3);

       }

  return str;

}

console.log(right_three("Python"));

console.log(right_three("JavaScript"));

console.log(right_three("Hi"));

Output:

honPyt

iptJavaScr

Hi

Compute the sum

Of three elements of a given array

Of integers of length 3

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to compute the sum of three elements of an given integers of length 3.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function sum_three(nums)

{

  return nums[0] + nums[1] + nums[2];

}

console.log(sum_three([10, 32, 20])); 

console.log(sum_three([5, 7, 9]));

console.log(sum_three([0, 8, -11]));

Output:

62

21

-3

Add two digits

Of a given positive integer

Of length two

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to add two digits of a given positive integer of length two.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function add_two_digits(n)

   {

      return n % 10 + Math.floor(n / 10);

   }

console.log(add_two_digits(25))

console.log(add_two_digits(50))

Output:

7

5

Check whether a given year is a leap

HTML CODE

<!DOCTYPE html>

<html>

<head>

<meta charset=utf-8 />

<title>Find Leap Year</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function leapyear(year)

{

return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);

}

console.log(leapyear(2016));

console.log(leapyear(2000));

console.log(leapyear(1700));

console.log(leapyear(1800));

console.log(leapyear(100));

OUTPUT

true

true

false

false

false

Check given positive number

Multiple of 3 or a multiple of 7

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to check whether a given positive number is a multiple of 3 or a multiple of 7\. </title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function test37(x)

{

  if (x % 3 == 0 || x % 7 == 0)

  {

    return true;

  }

  else {

    return false;

  }

}

console.log(test37(12));

console.log(test37(14));

console.log(test37(10));

console.log(test37(11));

Output:

true

true

false

false

Check a string starts with 'Java'

And false otherwise

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to check whether a string starts with 'Java' and false otherwise.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function start_spec_str(str)

{

  if (str.length < 4)

  {

    return false;

  }

  front = str.substring(0, 4);

  if (front == 'Java')

  {

    return true;

  }

   else

   {

    return false;

  }

}

console.log(start_spec_str("JavaScript"));

console.log(start_spec_str("Java"));

console.log(start_spec_str("Python"));

Output:

true

true

false

Check two given integer values

In the range 50..99

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to check whether two given integer values are in the range 50..99 (inclusive). Return true if either of them are in the said range.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function check_numbers(x, y)

  {

  if ((x >= 50 && x <= 99) || (y >= 50 && y <= 99))

  {

    return true;

  }

  else

  {

    return false;

  }

}

console.log(check_numbers(12, 101));

console.log(check_numbers(52, 80));

console.log(check_numbers(15, 99));

OUTPUT

false

true

true

Find a value which is nearest to 100

HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to find a value which is nearest to 100 from two different given integer values.</title>

</head>

<body>

</body>

</html>

JAVASCRIPT CODE

function near_100(x, y) {

  if (x != y)

  {

  x1 = Math.abs(x - 100);

  y1 = Math.abs(y - 100);

  if (x1 < y1)

  {

    return x;

  }

  if (y1 < x1)

  {

    return y;

  }

  return 0;

  }

  else

    return false;

}

console.log(near_100(90, 89));

console.log(near_100(-90, -89));

console.log(near_100(90, 90));

Output:

90

-89

false

OUR OTHER PUBLISHING

TAM SEL

[APACHE SPARK AND SCALA FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast!](https://www.amazon.com/APACHE-SPARK-SCALA-BEGINNERS-QuickStart-ebook/dp/B084SGW51Y/ref=sr_1_1?dchild=1&keywords=APACHE+SPARK+AND+SCALA+FOR+BEGINNERS%3A+2+BOOKS+IN+1+-+Learn+Coding+Fast%21&qid=1627653411&s=digital-text&sr=1-1)

[PYTHON AND JAVASCRIPT CODING BASICS: FOR ABSOLUTE BEGINNERS](https://www.amazon.com/PYTHON-JAVASCRIPT-CODING-BASICS-BEGINNERS-ebook/dp/B09756TC9M/ref=sr_1_1?dchild=1&keywords=PYTHON+AND+JAVASCRIPT+CODING+BASICS%3A+FOR+ABSOLUTE+BEGINNERS&qid=1627653589&s=digital-text&sr=1-1)

[LARAVEL FOR BEGINNERS: Learn Coding Fast](https://www.amazon.com/LARAVEL-BEGINNERS-Framework-Hands-Beginners-ebook/dp/B08779PRGD/ref=sr_1_1?dchild=1&keywords=LARAVEL+FOR+BEGINNERS%3A+Learn+Coding+Fast%3A&qid=1627653650&s=digital-text&sr=1-1)

[HTML FOR BEGINNERS: Html CSS Programming Language Crash Course, Web Design Quick Start Script Tutorial Book in Easy Steps](https://www.amazon.com/HTML-BEGINNERS-Programming-Language-Tutorial-ebook/dp/B07SBFC4TG/ref=sr_1_1?dchild=1&keywords=HTML+FOR+BEGINNERS%3A+Html+CSS+Programming+Language+Crash+Course%2C+Web+Design+Quick+Start+Script+Tutorial+Book+in+Easy+Steps+-+LEARN+TO+CODE+FAST&qid=1627653769&s=digital-text&sr=1-1)

[DART PROGRAMMING BASICS: FOR ABSOLUTE BEGINNERS](https://www.amazon.com/DART-PROGRAMMING-BASICS-ABSOLUTE-BEGINNERS-ebook/dp/B08ZHVYV2L/ref=sr_1_1?dchild=1&keywords=DART+PROGRAMMING+BASICS%3A+FOR+ABSOLUTE+BEGINNERS&qid=1627653907&s=digital-text&sr=1-1)

[RUST AND GOLANG FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast! RUST AND GOLANG](https://www.amazon.com/RUST-GOLANG-BEGINNERS-QuickStart-Tutorial-ebook/dp/B085417G1F/ref=sr_1_1?dchild=1&keywords=RUST+AND+GOLANG+FOR+BEGINNERS%3A+2+BOOKS+IN+1+-+Learn+Coding+Fast%21&qid=1627654027&s=digital-text&sr=1-1)

[APACHE SPARK AND HADOOP FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast!](https://www.amazon.com/APACHE-SPARK-HADOOP-BEGINNERS-QuickStart-ebook/dp/B083KDVCKQ/ref=sr_1_1?dchild=1&keywords=APACHE+SPARK+AND+HADOOP+FOR+BEGINNERS%3A&qid=1627654125&s=digital-text&sr=1-1)

[TENSORFLOW FOR BEGINNERS: LEARN CODING FAST](https://www.amazon.com/TensorFlow-Beginners-Framework-learning-Hands-ebook/dp/B0872T7GS1/ref=sr_1_1?dchild=1&keywords=TensorFlow+For+Beginners%3A+Learn+Coding+Fast%3A&qid=1627654182&s=digital-text&sr=1-1)

[DJANGO AND PYTHON FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast!](https://www.amazon.com/DJANGO-PYTHON-BEGINNERS-Programming-QuickStart-ebook/dp/B07Y58ZGVS/ref=sr_1_1?dchild=1&keywords=DJANGO+AND+PYTHON+FOR+BEGINNERS%3A+2+BOOKS+IN+1+-+Learn+Coding+Fast%21&qid=1627654258&s=digital-text&sr=1-1)

[JAVASCRIPT AND DART CODING BASICS: FOR ABSOLUTE BEGINNER](https://www.amazon.com/JAVASCRIPT-DART-CODING-BASICS-BEGINNERS-ebook/dp/B092DKX7S9/ref=sr_1_1?dchild=1&keywords=JAVASCRIPT+AND+DART+CODING+BASICS%3A+FOR+ABSOLUTE+BEGINNERS&qid=1627654541&s=digital-text&sr=1-1)

[TENSORFLOW FOR BEGINNERS AND PYTHON CODING BASICS: FOR ABSOLUTE BEGINNERS](https://www.amazon.com/TENSORFLOW-BEGINNERS-PYTHON-CODING-BASICS-ebook/dp/B08RVGF33C/ref=sr_1_2?dchild=1&keywords=TENSORFLOW+FOR+BEGINNERS+AND+PYTHON+CODING+BASICS%3A+FOR+ABSOLUTE+BEGINNERS&qid=1627654724&s=digital-text&sr=1-2)

[RUST Programming Language: For Beginners, Learn Coding Fast!](https://www.amazon.com/RUST-Programming-Language-Beginners-QuickStart-ebook/dp/B07VRXQ2PR/ref=sr_1_2?dchild=1&keywords=RUST+Programming+Language+TAM+SEL&qid=1627653241&s=digital-text&sr=1-2)

[HADOOP AND PYTHON FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast!](https://www.amazon.com/HADOOP-PYTHON-BEGINNERS-QuickStart-Tutorial-ebook/dp/B082WH5Y1X/ref=sr_1_1?dchild=1&keywords=HADOOP+AND+PYTHON+FOR+BEGINNERS%3A+2+BOOKS+IN+1+-+Learn+Coding+Fast%21&qid=1627654833&s=digital-text&sr=1-1)

[SELENIUM AND JAVA FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast!](https://www.amazon.com/SELENIUM-JAVA-BEGINNERS-framework-QuickStart-ebook/dp/B08533D6L9/ref=sr_1_1?dchild=1&keywords=SELENIUM+AND+JAVA+FOR+BEGINNERS%3A+2+BOOKS+IN+1+-+Learn+Coding+Fast%21&qid=1627654994&s=digital-text&sr=1-1)

[ANDROID AND JAVA FOR BEGINNERS: 2 BOOKS IN 1 - Learn Coding Fast!](https://www.amazon.com/ANDROID-JAVA-BEGINNERS-QuickStart-Tutorial-ebook/dp/B087F54VY2/ref=sr_1_1?dchild=1&keywords=ANDROID+AND+JAVA+FOR+BEGINNERS%3A+2+BOOKS+IN+1+-+Learn+Coding+Fast%21&qid=1627655061&s=digital-text&sr=1-1)

J KING

[PYTHON AND HADOOP BASICS](https://www.amazon.com/PYTHON-HADOOP-BASICS-PROGRAMMING-QuickStart-ebook/dp/B08CQYCVZZ/ref=sr_1_1?dchild=1&keywords=PYTHON+AND+HADOOP+BASICS&qid=1627631650&s=digital-text&sr=1-1)

[PYTHON BASICS AND PYTHON CODING EXAMPLES](https://www.amazon.com/PYTHON-BASICS-CODING-EXAMPLES-PROGRAMMING-ebook/dp/B08FL5QJCF/ref=sr_1_10?dchild=1&keywords=PYTHON+BASICS+AND+PYTHON+CODING+EXAMPLES+J+KING&qid=1627633161&s=digital-text&sr=1-10)

[C# AND C++ CODING EXAMPLES](https://www.amazon.com/CODING-EXAMPLES-PROGRAMMING-BEGINNERS-ebook/dp/B08KNG5629/ref=sr_1_1?dchild=1&keywords=C%23+AND+C%2B%2B+CODING+EXAMPLES&qid=1627631323&s=digital-text&sr=1-1)

[PYTHON CODING AND C PROGRAMMING EXAMPLES](https://www.amazon.com/PYTHON-CODING-PROGRAMMING-EXAMPLES-BEGINNERS-ebook/dp/B08L27PLYH/ref=sr_1_3?dchild=1&keywords=PYTHON+CODING+AND+C+PROGRAMMING+EXAMPLES&qid=1627631395&s=digital-text&sr=1-3)

[C++ AND JAVA CODING EXAMPLES](https://www.amazon.com/JAVA-CODING-EXAMPLES-PROGRAMMING-BEGINNERS-ebook/dp/B08P3SVG4G/ref=sr_1_1?dchild=1&keywords=C%2B%2B+AND+JAVA+CODING+EXAMPLES&qid=1627631477&s=digital-text&sr=1-1)

[ANDROID BASICS AND PYTHON CODING EXAMPLES](https://www.amazon.com/ANDROID-BASICS-PYTHON-CODING-EXAMPLES-ebook/dp/B09B5DX2ZV/ref=sr_1_3?dchild=1&qid=1627629803&refinements=p_27%3AJ+KING&s=digital-text&sr=1-3&text=J+KING)

[C# BASICS AND PYTHON CODING EXAMPLES](https://www.amazon.com/BASICS-PYTHON-CODING-EXAMPLES-PROGRAMMING-ebook/dp/B0999PMF22/ref=sr_1_10?dchild=1&qid=1627629803&refinements=p_27%3AJ+KING&s=digital-text&sr=1-10&text=J+KING)

[ANGULAR AND PYTHON BASICS](https://www.amazon.com/ANGULAR-PYTHON-BASICS-PROGRAMMING-QuickStart-ebook/dp/B08G8H59P4/ref=sr_1_1?dchild=1&keywords=ANGULAR+AND+PYTHON+BASICS+J+KING&qid=1627633307&s=digital-text&sr=1-1)

[PYTHON BASICS AND SCALA CODING EXAMPLES](https://www.amazon.com/PYTHON-BASICS-SCALA-CODING-EXAMPLES-ebook/dp/B0995DJ1SZ/ref=sr_1_19?dchild=1&qid=1627630555&refinements=p_27%3AJ+KING&s=digital-text&sr=1-19&text=J+KING)

[JAVA BASICS AND PYTHON CODING EXAMPLES](https://www.amazon.com/JAVA-BASICS-PYTHON-CODING-EXAMPLES-ebook/dp/B098LVH4GK/ref=sr_1_21?dchild=1&qid=1627630555&refinements=p_27%3AJ+KING&s=digital-text&sr=1-21&text=J+KING)

[PYTHON BASICS AND C# CODING EXAMPLES](https://www.amazon.com/PYTHON-BASICS-CODING-EXAMPLES-PROGRAMMING-ebook/dp/B098FMBC9Z/ref=sr_1_20?dchild=1&qid=1627630555&refinements=p_27%3AJ+KING&s=digital-text&sr=1-20&text=J+KING)

[ANDROID BASICS AND JAVA CODING EXAMPLES](https://www.amazon.com/ANDROID-BASICS-JAVA-CODING-EXAMPLES-ebook/dp/B098PKHZD3/ref=sr_1_24?dchild=1&qid=1627630555&refinements=p_27%3AJ+KING&s=digital-text&sr=1-24&text=J+KING)

[C# BASICS AND C# CODING EXAMPLES](https://www.amazon.com/BASICS-CODING-EXAMPLES-PROGRAMMING-QuickStart-ebook/dp/B08GZL6NW6/ref=sr_1_6?dchild=1&keywords=C%23+BASICS+AND+C%23+CODING+EXAMPLES&qid=1627631068&s=digital-text&sr=1-6)

[JAVASCRIPT AND HTML BASICS](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

[HTML AND JAVASCRIPT CODING EXAMPLES](https://www.amazon.com/HTML-JAVASCRIPT-CODING-EXAMPLES-PROGRAMMING-ebook/dp/B08STNKT5M/ref=sr_1_1?dchild=1&keywords=HTML+AND+JAVASCRIPT+CODING+EXAMPLES&qid=1627631214&s=digital-text&sr=1-1)