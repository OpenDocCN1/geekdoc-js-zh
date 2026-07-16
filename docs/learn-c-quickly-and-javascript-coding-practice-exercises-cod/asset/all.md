![](Image00014.jpg)

LEARN C# QUICKLY

AND

JAVASCRIPT

CODING PRACTICE EXERCISES

CODING FOR BEGINNERS

WITH HANDS ON PROJECTS

BY

J J TAM

[Introduction to C#](#text00003.html__Toc82098328)

[C#: Hello World Program](#text00004.html__Toc82098329)

[C#: Read input from console](#text00005.html__Toc82098330)

[C#: Built in Types](#text00006.html__Toc82098331)

[C#: Strings and Escape Sequences](#text00007.html__Toc82098332)

[C#: Verbatim Literal](#text00008.html__Toc82098333)

[C#: Operators](#text00009.html__Toc82098334)

[C#: Arithmetic Operators](#text00010.html__Toc82098335)

[C#: Arithmetic Operators: ++, --](#text00011.html__Toc82098336)

[C#: Conditional operators](#text00012.html__Toc82098337)

[C#: Logical Operators](#text00013.html__Toc82098338)

[C#: Shift Operators](#text00014.html__Toc82098339)

[C#: Bitwise Operators](#text00015.html__Toc82098340)

[C#: Compound Assignment Operators](#text00016.html__Toc82098341)

[C#: Ternary operator( ?: )](#text00017.html__Toc82098342)

[C#: Arrays](#text00018.html__Toc82098343)

[C#: Comments](#text00019.html__Toc82098344)

[C#: if, else : Conditional statements](#text00020.html__Toc82098345)

[C#: Switch statement](#text00021.html__Toc82098346)

[C#: goto statement](#text00022.html__Toc82098347)

[C#: while loop](#text00023.html__Toc82098348)

[C#: do-while loop](#text00024.html__Toc82098349)

[C#: for loop](#text00025.html__Toc82098350)

[C#: for-each loop](#text00026.html__Toc82098351)

[C#: break statement](#text00027.html__Toc82098352)

[C#: continue statement](#text00028.html__Toc82098353)

[C#: Methods](#text00029.html__Toc82098354)

[JAVASCRIPT CODING EXERCISES](#text00031.html__Toc82098355)

[JavaScript functions – Exercises](#text00031.html__Toc82098356)

[JavaScript: Find the first not repeated character](#text00031.html__Toc82098357)

[JavaScript: Find the longest word within a string](#text00032.html__Toc82098358)

[JavaScript: Counts the number of vowels within a string](#text00033.html__Toc82098359)

[JavaScript: Check a number is prime or not](#text00034.html__Toc82098360)

[JavaScript: Get the data type](#text00035.html__Toc82098361)

[JavaScript: Find the second lowest and second greatest](#text00036.html__Toc82098362)

[JAVASCRIPT BASICS](#text00037.html__Toc82098363)

[Calculate multiplication and division](#text00037.html__Toc82098364)

[Convert temperatures](#text00038.html__Toc82098365)

[Find the largest](#text00039.html__Toc82098366)

[Reverse a given string](#text00040.html__Toc82098367)

[Replace every character](#text00041.html__Toc82098368)

[Create a new string](#text00042.html__Toc82098369)

[Concatenate two strings](#text00043.html__Toc82098370)

[Move last three character](#text00044.html__Toc82098371)

[Compute the sum](#text00045.html__Toc82098372)

[Add two digits](#text00046.html__Toc82098373)

[Check whether a given year is a leap](#text00047.html__Toc82098374)

[Check given positive number](#text00048.html__Toc82098375)

[Check a string starts with 'Java'](#text00049.html__Toc82098376)

[Check two given integer values](#text00050.html__Toc82098377)

[Find a value which is nearest to 100](#text00051.html__Toc82098378)

[OUR OTHER PUBLISHING](#text00052.html__Toc82098379)

LEARN C# QUICKLY

CODING FOR BEGINNERS

BY

J J TAM

# Introduction to C#

C# is a programming language that supports more than one programming paradigm. The basic syntax of C# is similar to that of C, C++ and Java. So if you are familiar with any one of these languages, you can learn C# just like that.

## What is multi-paradigm programming language?

A Language that supports more than one programming paradigm is called multi-paradigm programming language. C# is a multi-paradigm programming language, it supports both imperative and object-oriented paradigms. C# support some level of functional programming also.

## C# Vs .net

C# is a programming language, and ‘.NET’ is a framework. ‘.NET’ has various languages under it. C# is one of the language in ‘.NET’.

What is the latest version of C#?

At the time of writing this article, the most recent version is C# 6.0 which was released in 2015.

Prerequisites to work with C#

Install Visual studio. You can get the community edition from following link.

https://www.visualstudio.com/vs/community/

# C#: Hello World Program

I hope, you installed Visual studio. Following step-by-step procedure explains simple ‘Hello World’ application.

Step 1:  Open Visual studio

[![https://2.bp.blogspot.com/-k1u5i75B59Q/W3bIOR6l6rI/AAAAAAAAK6E/GQI1hkAGvWIJQvBdar3U7GJAUfU159eHACEwYBhgL/s400/Visual_studion_create_project.png](Image00000.jpg)](https://2.bp.blogspot.com/-k1u5i75B59Q/W3bIOR6l6rI/AAAAAAAAK6E/GQI1hkAGvWIJQvBdar3U7GJAUfU159eHACEwYBhgL/s1600/Visual_studion_create_project.png)

Step 2:  Go to File -> New -> Project.

Select “Console Application”, give the project name as “HelloWorld”.

Press OK.

It creates a file ‘Program.cs’, with some default data.

Update the program like below.

using System ;

namespace HelloWorld

{

    class Program

    {

        static void Main ( string [] args)

        {

            Console.WriteLine("Hello World");

            Console.WriteLine("Welcome To C# Programming.........");

        }

    }

}

Press ‘CTRL + F5’, it opens command prompt and show the strings that we passed to 'Console.WriteLine' method.

Let’s analyze the program

‘using System’

Above statement loads a names space ‘System’. Name spaces are used to organize the code. A name space is a collection of classes, interfaces, enums, structs & delegates.

namespace HelloWorld

Above statement gives the name space ‘HelloWorld’ to this program. It is optional. You can even run the program without this statement.

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Hello World");

        Console.WriteLine("Welcome To C# Programming.........");

    }

}

class Program

Class is used to encapsulate methods and properties as single entity. Ignore this for time being, I will explain about this in later posts.

static void Main(string[] args)

Main method is the entry point of your C# application. Application executions starts from here.

Console.WriteLine("Hello World");
Above statement writes the message "Hello World" to console. Console is the class resides in name space System. WriteLine is the method of class Console.

# C#: Read input from console

‘Console’ class provides ‘ReadLine’ method to read input from console. ReadLine method reads the information from console and return the input in string format.

String name = Console.ReadLine();

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Welcome to C#, Please Enter Basic Informaiton");

        Console.WriteLine("Enter Your Name");

        String name = Console.ReadLine();

        Console.WriteLine("Enter Your Age");

        String age = Console.ReadLine();

        Console.WriteLine("Hello " + name + " You are " + age + " years old");

    }

}

Output

Welcome to C#, Please Enter Basic Informaiton

Enter Your Name

JJ TAM

Enter Your Age

26

Hello JJ TAM You are 26 years old

## Place Holder Syntax

While concatenating the strings, place holder syntax is very convenient than using ‘+’ operator.

Following is the example of place holder syntax.

Console.WriteLine("Hello {0}. You are {1} years old", name, age);

Above statement is equivalent of following statement.

Console.WriteLine("Hello " + name + " You are " + age + " years old");

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Welcome to C#, Please Enter Basic Informaiton");

        Console.WriteLine("Enter Your Name");

        String name = Console.ReadLine();

        Console.WriteLine("Enter Your Age");

        String age = Console.ReadLine();

        Console.WriteLine("Hello {0}", name);

        Console.WriteLine("You are {0} years old", age);

        Console.WriteLine("Hello {1}. You are {0} years old", name, age);

    }

}

Output

Welcome to C#, Please Enter Basic Informaiton

Enter Your Name

JJ TAM

Enter Your Age

26

Hello JJ TAM

You are 26 years old

Hello 26\. You are JJ TAM years old

Press any key to continue . . .

# C#: Built in Types

C# support almost all kind of data types to work with. All data types are represented as classes in System namespace. Data types can be categorized into following types.

a.   Boolean : bool

b.   Integer: byte, sbyte, int, uint, short, ushort, long, ulong

c.   Float: double, float, decimal

d.   Character : char

e.   String

Following table summarizes all the data types

| Short Name | Class | Min value | Max value |
| byte | Byte | 0 | 255 |
| sbyte | SByte | -128 | 127 |
| int | Int32 | -2,147,483,648 | 2,147,483,647 |
| uint | UInt32 | 0 | 4294967295 |
| short | Int16 | -32,768 | 32767 |
| ushort | UInt16 | 0 | 65535 |
| long | Int64 | - 9223372036854775808 | 9223372036854775807 |
| ulong | UInt64 | 0 | 18446744073709551615 |
| float | Single | -3.402823e38 | 3.402823e38 |
| double | Double | -1.79769313486232e308 | 1.79769313486232e308 |
| decimal | Decimal | ±1.0 × 10e−28 | ±7.9 × 10e28 |
| char | Char |  | Represent Unicode character. It take 16 bits. |
| string | String |  | Sequence of characters |

Note

a. Suffix Float variables by f.

         Ex:  float floatVar = 18.18f;

b. Suffix Decimal variables by m.

         Ex: decimal decimalVar = 20.20m;

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        byte byteVar = 10 ;

        sbyte sbyteVar = 11 ;

        int intVar = 12 ;

        uint uintVar = 13 ;

        short shortVar = 14 ;

        ushort ushortVar = 15 ;

        long longVar = 16 ;

        ulong ulongVar = 17 ;

        float floatVar = 18.18f ;

        double doubleVar = 19.19 ;

        decimal decimalVar = 20.20 m;

        char charVar = 'S';

        string stringVar = "Hello World";

        Console.WriteLine("byteVar = {0}", byteVar);

        Console.WriteLine("sbyteVar = {0}", sbyteVar);

        Console.WriteLine("intVar = {0}", intVar);

        Console.WriteLine("uintVar = {0}", uintVar);

        Console.WriteLine("shortVar = {0}", shortVar);

        Console.WriteLine("ushortVar = {0}", ushortVar);

        Console.WriteLine("longVar = {0}", longVar);

        Console.WriteLine("ulongVar = {0}", ulongVar);

        Console.WriteLine("floatVar = {0}", floatVar);

        Console.WriteLine("doubleVar = {0}", doubleVar);

        Console.WriteLine("decimalVar = {0}", decimalVar);

        Console.WriteLine("charVar = {0}", charVar);

        Console.WriteLine("stringVar = {0}", stringVar);

    }

}

# C#: Strings and Escape Sequences

String is a Collection of characters. Strings are enclosed in double quotes.

Ex:

String firstName = "JJ TAM";

String lastName = "Delhi";

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        String firstName = "JJ TAM";

        String lastName = "Delhi";

        Console.WriteLine("Hello Mr {0} {1}", firstName, lastName);

    }

}

Output

Hello Mr JJ TAM Delhi

## Escape Sequences

Escape sequences in programing languages has special meaning, For example, \n prints string in new line, \t is a tab character etc., Following tables summarizes some of the escape characters in C#.

| Escape Sequence | Description |
| \a | Bell alert |
| \b | Backspace |
| \f | Form feed |
| \n | New Line |
| \r | Carriage Return |
| \t | Horizontal tab |
| \v | Vertical tab |
| \’ | Single Quote |
| \" | Double Quote |
| \\ | Backslash |
| \? | Question Mark |
| \ooo | ASCII Character in Octal Notation |
| \xhh | ASCII Character in hexadecimal notation |
| \xhhhh | Unicode character in hexadecimal notation |

[![https://2.bp.blogspot.com/-JnrYXOJxEVU/W3bgyFF1heI/AAAAAAAAK6s/IFNPn_v3oXAyEWzTqcO7T1nT0z-mkkG5QCLcBGAs/s400/C%2523%2BString%2Band%2Bescape%2Bsequences.jpg](Image00001.jpg)](https://2.bp.blogspot.com/-JnrYXOJxEVU/W3bgyFF1heI/AAAAAAAAK6s/IFNPn_v3oXAyEWzTqcO7T1nT0z-mkkG5QCLcBGAs/s1600/C#+String+and+escape+sequences.jpg)

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        String quote = "Life is an \"Open Secret\". \nEverything is avialble, you can't hidden";

        Console.WriteLine(quote);

    }

}

Output

Life is an "Open Secret".

Everything is avialble, you can't hidden

# C#: Verbatim Literal

A verbatim string literal consists of an @ character followed by a string in double quotes. The escape sequences in verbatim string literal are not processed.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        String withoutVerbatim = @"1\n2\n3\t4";

        String withoutVerbatim = "1\n2\n3\t4";

        Console.WriteLine(withVerbatim);

        Console.WriteLine("******************");

        Console.WriteLine(withoutVerbatim );

    }

}

Output

1\n2\n3\t4

******************

1

2

3       4

As you see the ouput, @ symbol don’t interpret the escape sequences \n, \t. Where as the string withOutVerbatim interpreted \n as new line and \t as tab.

# C#: Operators

An operator is a symbol which perform an operation

An operator is said to be unary, if it performs operation on single operand.

   Ex:

      int a = 10;

      a++;

An operator is said to be binary, if it performs operation on two operands

   Ex:

      int a=10, b=20;

      int c = a-b;

An Operator is said to be ternary if it perform operation on three operands

   Ex:

      int a = 10, b=20, c;

      c= (a>b) ? a : b;

Operators in C# are divided into 4 major categories

   Arithmetic

   Conditional

   Logical

   Bitwise

# C#: Arithmetic Operators

Arithmetic operators are used to perform arithmetic operation on operands.

[![https://3.bp.blogspot.com/-AnQfNYwim9o/W3bkn0rb28I/AAAAAAAAK64/9qVl8WCFUfcP6uzosIFhS1_QfdGpkvr4ACLcBGAs/s400/C%2523%2BArithmetic%2BOperators.jpg](Image00002.jpg)](https://3.bp.blogspot.com/-AnQfNYwim9o/W3bkn0rb28I/AAAAAAAAK64/9qVl8WCFUfcP6uzosIFhS1_QfdGpkvr4ACLcBGAs/s1600/C#+Arithmetic+Operators.jpg)

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int operand1 = 30 ;

        int operand2 = 10 ;

        Console.WriteLine("operand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("Addition of operand1 and operand2 is {0}", (operand1 + operand2));

        Console.WriteLine("Subtraction of operand1 and operand2 is {0}", (operand1 - operand2));

        Console.WriteLine("Multiplication of operand1 and operand2 is {0}", (operand1 * operand2));

        Console.WriteLine("Division of operand1 and operand2 is {0}", (operand1 / operand2));

        Console.WriteLine("Remainder of operand1 and operand2 is {0}", (operand1 % operand2));

    }

}

Output

operand1 = 30

operand2 = 10

Addition of operand1 and operand2 is 40

Subtraction of operand1 and operand2 is 20

Multiplication of operand1 and operand2 is 300

Division of operand1 and operand2 is 3

Remainder of operand1 and operand2 is 0

# C#: Arithmetic Operators: ++, --

++ Increment operator; increments a value by 1

-- Decrement operator; decrements a value by 1

Pre increment

    Syntax:

    ++variable

      pre increment operator increments the variable value by 1 immediately.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var = 10 ;

        Console.WriteLine("var = {0}", ++ var );

    }

}

Output

var = 11

Post increment

    Syntax:

        variable++

    Post increment operator increments the variable value by 1 after executing the current statement.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var = 10 ;

        Console.WriteLine("var = {0}", var ++);

        Console.WriteLine("var = {0}", var );

    }

}

Output

var = 10

var = 11

Pre Decrement

    Syntax:

        --variable

    Pre decrement operator decrements the variable value by 1 immediately.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var = 10 ;

        Console.WriteLine("var = {0}", -- var );

    }

}

Output

var = 9

Post Decrement

    Syntax:

        variable--

Post decrement operator decrements the variable value by 1 after executing the current statement.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var = 10 ;

        Console.WriteLine("var = {0}", var --);

        Console.WriteLine("var = {0}", var );

    }

}

Output

var = 10

var = 9

# C#: Conditional operators

Conditional operators determine whether one operand is greater than, less than, equal to, or not equal to another operand.

[![https://4.bp.blogspot.com/-L0p6MK64YEg/W3bnD8IFVLI/AAAAAAAAK7E/mqCH_nXaXWsY-VvmKP-hR-xFUA0zLgwKwCLcBGAs/s400/C%2523%2BConditional%2Boperators.jpg](Image00003.jpg)](https://4.bp.blogspot.com/-L0p6MK64YEg/W3bnD8IFVLI/AAAAAAAAK7E/mqCH_nXaXWsY-VvmKP-hR-xFUA0zLgwKwCLcBGAs/s1600/C#+Conditional+operators.jpg)

Conditional operators take two operands and return true, if the condition evaluates to true, otherwise return false.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int a = 10 , b = 11 ;

        Console.WriteLine("is a equals to a {0}", (a == a));

        Console.WriteLine("is a equals to b {0}", (a == b));

        Console.WriteLine("is a not equals to a {0}", (a != a));

        Console.WriteLine("is a not equals to b {0}", (a != b));

        Console.WriteLine("is a less than a {0}", (a < a));

        Console.WriteLine("is a less than b {0}", (a < b));

        Console.WriteLine("is a less than or equal to a {0}", (a <= a));

        Console.WriteLine("is a less than or equal b {0}", (a <= b));

        Console.WriteLine("is a greater than a {0}", (a > a));

        Console.WriteLine("is a greater than b {0}", (a > b));

        Console.WriteLine("is a greater than or equal to a {0}", (a >= a));

        Console.WriteLine("is a greater than or equal to b {0}", (a >= b));

    }

}

Output

is a equals to a True

is a equals to b False

is a not equals to a False

is a not equals to b True

is a less than a False

is a less than b True

is a less than or equal to a True

is a less than or equal b True

is a greater than a False

is a greater than b False

is a greater than or equal to a True

is a greater than or equal to b False

# C#: Logical Operators

C# provides three logical operators, These are &&(AND), || (OR), and !(NOT)

Logical AND is also called Conditional AND

Logical OR is also called Conditional OR

Logical AND, OR are called Short circuit operators, will see why these are called short circuit soon.

## Logical AND Operator

Operand1 - Operand2 - Evaluates To

TRUE-TRUE-TRUE

TRUE-FALSE-FALSE

FALSE-TRUE-FALSE

FALSE-FALSE-FALSE

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        bool operand1 = true ;

        bool operand2 = true ;

        Console.WriteLine("operand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 && operand2 = {0}", (operand1 && operand2));

        operand1 = true ;

        operand2 = false ;

        Console.WriteLine("\noperand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 && operand2 = {0}",(operand1 && operand2));

        operand1 = false ;

        operand2 = true ;

        Console.WriteLine("\noperand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 && operand2 = {0}", (operand1 && operand2));

        operand1 = false ;

        operand2 = false ;

        Console.WriteLine("\noperand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 && operand2 = {0}", (operand1 && operand2));

    }

}

Output

operand1 = True

operand2 = True

operand1 && operand2 = True

operand1 = True

operand2 = False

operand1 && operand2 = False

operand1 = False

operand2 = True

operand1 && operand2 = False

operand1 = False

operand2 = False

operand1 && operand2 = False

Why Logical AND is called short circuit operator?

Since if the first statement in the expression evaluates to false, then java won't evaluate the entire expression. So Logical AND is called short circuit AND.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int a = 10 , b = 21 ;

        if ((a > b) && (a++ > b))

        {

            Console.WriteLine("This statement not evaluated");

        }

        Console.WriteLine("a is not incremented " + a);

        if ((a < b) && (a++ < b))

        {

            Console.WriteLine("This statement is evaluated");

        }

        Console.WriteLine("a is incremented " + a);

    }

}

Output

a is not incremented 10

This statement is evaluated

a is incremented 11

Observation

In the expression (a>b) && (a++ > b), a>b is false, so && operator won't evaluate second statement in the expression, so a is not incremented.

## Logical OR Operator

Operand1-Operand2-Evaluates To

TRUE-TRUE-TRUE

TRUE-FALSE-TRUE

FALSE-TRUE-TRUE

FALSE-FALSE-FALSE

As shown in the above table, || operator returns true if any of the operand evaluates to true, otherwise returns false.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        bool operand1 = true ;

        bool operand2 = true ;

        Console.WriteLine("operand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 || operand2 = {0}", (operand1 || operand2));

        operand1 = true ;

        operand2 = false ;

        Console.WriteLine("\noperand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 || operand2 = {0}", (operand1 || operand2));

        operand1 = false ;

        operand2 = true ;

        Console.WriteLine("\noperand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 || operand2 = {0}", (operand1 || operand2));

        operand1 = false ;

        operand2 = false ;

        Console.WriteLine("\noperand1 = {0}", operand1);

        Console.WriteLine("operand2 = {0}", operand2);

        Console.WriteLine("operand1 || operand2 = {0}", (operand1 || operand2));

    }

}

Output

operand1 = True

operand2 = True

operand1 || operand2 = True

operand1 = True

operand2 = False

operand1 || operand2 = True

operand1 = False

operand2 = True

operand1 || operand2 = True

operand1 = False

operand2 = False

operand1 || operand2 = False

Why Logical OR is called short circuit operator?

Since if the first statement evaluates to true, then java won't evaluates the entire expression. So Logial OR is called short circuit OR.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int a = 10 , b = 21 ;

        if ((a < b) || (a++ < b))

        {

            Console.WriteLine("This statement evaluated");

        }

        Console.WriteLine("a is not incremented " + a);

        if ((a > b) || (a++ > b))

        {

            Console.WriteLine("This statement is evaluated");

        }

        Console.WriteLine("a is incremented " + a);

    }

}

Output

This statement evaluated

a is not incremented 10

a is incremented 11

## Logical (!)NOT operator

Operand -Evaluates To

FALSE-TRUE

TRUE-FALSE

If the operand is FALSE, ! Operator evaluates it to TRUE

If the operand is TRUE, ! Operator evaluates it to FALSE.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        bool a = true ;

        Console.WriteLine("a = {0}, !a = {1}", a, !a);

        a = false ;

        Console.WriteLine("a = {0}, !a = {1}", a, !a);

    }

}

Output

operand1 = True

operand2 = True

operand1 || operand2 = True

operand1 = True

operand2 = False

operand1 || operand2 = True

operand1 = False

operand2 = True

operand1 || operand2 = True

operand1 = False

operand2 = False

operand1 || operand2 = False

# C#: Shift Operators

## Bit Wise Left Shift(<<)

Left shift operator shifts all the bits to one bit left, i.e, it simply doubles the value.

Syntax:

    variable << n

    left shift the variable by 'n' number of times.

    Variable << n is equals to variable = variable * 2 power n

        int var = 2;

        var << 1 = 2 * 2 power 1 = 4

        var << 2 = 2 * 2 power 2 = 8

        var << 9 = 2 * 2 power 9 = 1024

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        byte byteVar = 7 ;

        Console.WriteLine("Value of Byte variable is " + byteVar);

        Console.WriteLine("After shifting 1 bit left " + (byteVar << 1 ));

        Console.WriteLine("After shifting 2 bits left " + (byteVar << 2 ));

        Console.WriteLine("After shifting 3 bits left " + (byteVar << 3 ));

        Console.WriteLine("After shifting 4 bits left " + (byteVar << 4 ));

        Console.WriteLine("After shifting 5 bits left " + (byteVar << 5 ));

        Console.WriteLine("After shifting 6 bits left " + (byteVar << 6 ));

        Console.WriteLine("Value of Byte variable is " + byteVar);

    }

}

Output

Value of Byte variable is 7

After shifting 1 bit left 14

After shifting 2 bits left 28

After shifting 3 bits left 56

After shifting 4 bits left 112

After shifting 5 bits left 224

After shifting 6 bits left 448

Value of Byte variable is 7

## Bit Wise Right Shift(>>)

Right shift operator shifts all the bits to one bit right, i.e, it simply half (divide by 2) the value

   Syntax:

   variable >> n

      right shift the variable by 'n' number of times.

   Variable >> n is equals to variable = variable / 2 power n

   int var = 128;

   var >> 1 = 128 / (2 power 1) = 64

   var >> 2 = 128 / (2 power 2) = 32

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int intVar = 128 ;

        Console.WriteLine("Value of int variable is " + intVar);

        Console.WriteLine("After shifting 1 bit Right " + (intVar >> 1 ));

        Console.WriteLine("After shifting 2 bits Right " + (intVar >> 2 ));

        Console.WriteLine("After shifting 3 bits Right " + (intVar >> 3 ));

        Console.WriteLine("After shifting 4 bits Right " + (intVar >> 4 ));

        Console.WriteLine("After shifting 5 bits Right " + (intVar >> 5 ));

        Console.WriteLine("After shifting 6 bits Right " + (intVar >> 6 ));

        Console.WriteLine("After shifting 6 bits Right " + (intVar >> 7 ));

        Console.WriteLine("Value of int variable is " + intVar);

    }

}

Output

Value of int variable is 128

After shifting 1 bit Right 64

After shifting 2 bits Right 32

After shifting 3 bits Right 16

After shifting 4 bits Right 8

After shifting 5 bits Right 4

After shifting 6 bits Right 2

After shifting 6 bits Right 1

Value of int variable is 128

# C#: Bitwise Operators

## Bit Wise AND(&), OR(|), Exclusive OR(^)

[![https://2.bp.blogspot.com/-wEe4ZZqVpR8/W3buYtzc-RI/AAAAAAAAK7o/-YxiPSfPXhMAjgh-qX20Dd3KsUNCB1uyACLcBGAs/s400/C%2523%2Bbitwise%2Boperators.jpg](Image00004.jpg)](https://2.bp.blogspot.com/-wEe4ZZqVpR8/W3buYtzc-RI/AAAAAAAAK7o/-YxiPSfPXhMAjgh-qX20Dd3KsUNCB1uyACLcBGAs/s1600/C#+bitwise+operators.jpg)

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        byte a = 8 ;

        byte b = 9 ;

        Console.WriteLine("a & b is " + (a & b));

        Console.WriteLine("a | b is " + (a | b));

        Console.WriteLine("a ^ b is " + (a ^ b));

    }

}

Output

a & b is 8

a | b is 9

a ^ b is 1

Explanation

   a    = 0000 1000

   b    = 0000 1001

   a&b = 0000 1000

   a    = 0000 1000

   b    = 0000 1001

   a|b = 0000 10001

   a     = 0000 1000

   b     = 0000 1001
   a^b = 0000 0001

# C#: Compound Assignment Operators

## Compound Assignment

      Syntax:

         variable operator= value

       Example:

         int a = 10;

         a+=10 evaluates to a=a+10

| Compound Operator | Example | Description |
| += | a+=10 | a=a+10 |
| -= | a-=10 | a=a-10 |
| *= | a*=10 | a=a*10 |
| /= | a/=10 | a=a/10 |

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var1 = 100 ;

        int sum = 10 , sub = 10 , mul = 10 , div = 1000 ;

        Console.WriteLine("sum+var1 is " + (sum += var1));

        Console.WriteLine("sub-var1 is " + (sub -= var1));

        Console.WriteLine("mul*var1 is " + (mul *= var1));

        Console.WriteLine("div/var1 is " + (div /= var1));

    }

}

Output

sum+var1 is 110

sub-var1 is -90

mul*var1 is 1000

div/var1 is10

# C#: Ternary operator( ?: )

Returns one of two expressions depending on a condition.

Syntax

test ? expression1 : expression2

Returns expression1 if the “test” condition evaluates to true other wise returns expression2.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int a = 100 ;

        bool flag = a > 10 ? true : false ;

        Console.WriteLine("flag = {0}", flag);

    }

}

Output

flag = True

# C#: Arrays

An array is a series of elements of the same type placed in contiguous memory locations. Elements in the array are accessed using index positions.

Syntax

datatype[] arrayName = new datatype[sizeOfTheArray];

Ex:

int[] evenNumbers = new int[10];

Suppose if you want to calculate sum of 9 integers, you have to define 9 variables like below

    int var1, var2, var3, var4, var5, var6, var7, var8, var9;

    var1 = 5;

    var2 = -10;

    var3 = 7;

    var4 = 8

    var5 = 11;

    var6 = 12;

    var7 = 14;

    var8 = 21;

    var9 = 0;

By using arrays we can declare like below

    int var[] = new int[9];

    var[0] = 5;

    var[1] = -10;

    var[2] = 7;

    var[3] = 8

    var[4] = 11;

    var[5] = 12;

    var[6] = 14;

    var[7] = 21;

    var[8] = 0;

As you see, Array indexes starts from 0\. var[0] represents 5, var[2] represents 7 and so on.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int [] var = new int [ 9 ];

        var [ 0 ] = 5 ;

        var [ 1 ] = - 10 ;

        var [ 2 ] = 7 ;

        var [ 3 ] = 8 ;

        var [ 4 ] = 11 ;

        var [ 5 ] = 12 ;

        var [ 6 ] = 14 ;

        var [ 7 ] = 21 ;

        var [ 8 ] = 0 ;

        Console.WriteLine("var[0] = {0}", var [ 0 ]);

        Console.WriteLine("var[1] = {0}", var [ 1 ]);

        Console.WriteLine("var[2] = {0}", var [ 2 ]);

        Console.WriteLine("var[3] = {0}", var [ 3 ]);

        Console.WriteLine("var[4] = {0}", var [ 4 ]);

        Console.WriteLine("var[5] = {0}", var [ 5 ]);

        Console.WriteLine("var[6] = {0}", var [ 6 ]);

        Console.WriteLine("var[7] = {0}", var [ 7 ]);

        Console.WriteLine("var[8] = {0}", var [ 8 ]);

    }

}

Output

var[0] = 5

var[1] = -10

var[2] = 7

var[3] = 8

var[4] = 11

var[5] = 12

var[6] = 14

var[7] = 21

var[8] = 0

# C#: Comments

Comments make the program more readable. Comments are used to document your code.

Suppose you written thousand lines of program, without proper documentation, after some time, for the owner of the application also, it is very difficult to figure out what was written.

Comments solve this problem:

By using comments, you can document your code at the time of writing program. Comments don't affect your program execution. Comments simply document your code.

C# supports 3 types of comments

## Single line comment :

Single line comments starts with //

// It is a single line comment

## Multi Line comment

Multi line comments are place in between /* */

 /* I am a mulltiline comment */

XML Documentation Comments

XML Documentation comments are used to provide help to given class, function, namespace etc.,

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int marks; /* variable marks represents the marks

                  obtained by a student */

        marks = 70 ;

        Console.WriteLine("Marks : {0}", marks); //printing to console

    }

}

Output

Marks : 70

XML Documentation Comments Example

Update Program.cs like below.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        IntresetCalculator calc;

    }

}

/// <summary>

/// Class Calculates simple intrest

/// </summary>

class IntresetCalculator

{

}

When you hover the mouse on ‘IntresetCalculator’, you can able to see the summary of ‘IntresetCalculator’ class.

# C#: if, else : Conditional statements

C# provides control flow statements for decision making.

Decision making statements

## if statement

“if” statement execute the section of code when the condition evaluates to true.

Syntax

if(condition){

// Executes if the condition true

}

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Please Enter Your Marks");

        int marks = int .Parse(Console.ReadLine());

        if (marks < 35 )

        {

            Console.WriteLine("You failed in the Exam. Better luck next time");

        }

        if (marks >= 35 )

        {

            Console.WriteLine("Congrats, you passed in the Exam");

        }

    }

}

Sample Output1

Please Enter Your Marks

85

Congrats, you passed in the Exam

Sample Output2

Please Enter Your Marks

20

You failed in the Exam. Better luck next time

## if-else statement

Syntax:

    if(condition){

    }

    else{

    }

If the condition true, then if block code executed, otherwise else block code executed.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Please Enter Your Marks");

        int marks = int .Parse(Console.ReadLine());

        if (marks < 35 )

        {

            Console.WriteLine("You failed in the Exam. Better luck next time");

        }

        else

        {

            Console.WriteLine("Congrats, you passed in the Exam");

        }

    }

}

Sample Output1

Please Enter Your Marks

85

Congrats, you passed in the Exam

Sample Output2

Please Enter Your Marks

20

You failed in the Exam. Better luck next time

## if-else if-else ladder

By using if-else if-else construct, you can choose number of alternatives.

An if statement can be followed by an optional else if...else statement, which is very useful to test various conditions.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Please Enter Your Marks");

        int marks = int .Parse(Console.ReadLine());

        if (marks < 35 )

        {

            Console.WriteLine("You are failed");

        }    

        else if (marks < 50 )

        {

            Console.WriteLine("You are passed and got third class");

        } 

        else if (marks < 60 )

        {

            Console.WriteLine("You are passed and got second class");

        }   

        else if (marks < 70 )

        {

            Console.WriteLine("You are passed and got first class");

        }

        else

        {

           Console.WriteLine("You are passed and got distinction");

        }

    }

}

Sample Output1

Please Enter Your Marks

20

You are failed

Sample Output2

Please Enter Your Marks

40

You are passed and got third class

Sample Output3

Please Enter Your Marks

60

You are passed and got first class

Sample Output4

Please Enter Your Marks

80

You are passed and got distinction

# C#: Switch statement

switch statement evaluates its expression, then executes all statements that follow the matching case label. The body of a switch statement is known as a switch block. A statement in the switch block can be labelled with one or more case or default labels.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Enter a Number");

        int number = int .Parse(Console.ReadLine());

        switch (number)

        {

            case 1 :

                Console.WriteLine("Sunday");

                break ;

            case 2 :

                Console.WriteLine("Monday");

                break ;

            case 3 :

                Console.WriteLine("Tueday");

                break ;

            case 4 :

                Console.WriteLine("Wednesday");

                break ;

            case 5 :

                Console.WriteLine("ThursDay");

                break ;

            case 6 :

                Console.WriteLine("Friday");

                break ;

            case 7 :

                Console.WriteLine("Saturday");

                break ;

            default :

                Console.WriteLine("You entered wrong day number");

                break ;

        }

    }

}

Sample Output

Enter a Number

5

ThursDay

Sample Output

Enter a Number

15

You entered wrong day number

# C#: goto statement

By using goto statement, we can transfer the control to a label. Label is a marker in the program, where your code can jump there directly.

Syntax

goto label;

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Console.WriteLine("Enter a Number");

        int num = int .Parse(Console.ReadLine());

        if (num == 5 )

        {

            goto error;

        } else

        {

            Console.WriteLine("You Entered {0}", num);

            goto exit;

        }

        error:

        Console.WriteLine("Wrong Choice");

        System.Environment.Exit( 1 );

        exit:

        Console.WriteLine("Exiting Successfully");

        System.Environment.Exit( 0 );

    }

}

Sample Output1

Enter a Number

5

Wrong Choice

Sample Output2

Enter a Number

10

You Entered 10

Exiting Successfully

# C#: while loop

while statement executes a block of statements until a particular condition is true

Syntax

while (expression) {

      //statements

}

The expression in the while statement must evaluates to a Boolean value, otherwise compiler throws an error. While statement first evaluates the expression, until the expression evaluates to true, it executes the code inside the while block, otherwise it comes out of the while loop.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var1 = 0 ;

        while (var1 < 10 )

        {

            Console.WriteLine(var1);

            var1++;

        }

    }

}

Output

0

1

2

3

4

5

6

7

8

9

# C#: do-while loop

do-while is a loop construct like while loop, but evaluates its expression at the end of the loop.

Syntax

do {

//statement(s)

} while (expression);

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int var1 = 0 ;

        do

        {

            Console.WriteLine(var1);

            var1++;

        } while (var1 < 10 );

    }

}

Output

0

1

2

3

4

5

6

7

8

9

# C#: for loop

‘for’ statement provides a compact way to iterate over a range of values.

Syntax

    for(initialization; condition; update){

        //statements to be executed

    }

‘for’ loop execute the statements until the condition evaluates to false.

Initialization  section executed only once, at the starting of loop.

Condition  section evaluated every time, before executing the loop statements

Update  section executes immediately after every execution of loop finishes.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        for ( int var1 = 0 ; var1 < 10 ; var1++)

        {

            Console.WriteLine(var1);

        }

    }

}

Output

0

1

2

3

4

5

6

7

8

9

# C#: for-each loop

‘for-each’ loop is used to iterate over a collection of elements.

Syntax

foreach(datatype variable in collection){

}

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        int [] primeNumbers = new int [ 10 ];

        primeNumbers[ 0 ] = 2 ;

        primeNumbers[ 1 ] = 3 ;

        primeNumbers[ 2 ] = 5 ;

        primeNumbers[ 3 ] = 7 ;

        primeNumbers[ 4 ] = 11 ;

        primeNumbers[ 5 ] = 13 ;

        foreach ( int num in primeNumbers)

        {

            Console.WriteLine(num);

        }

    }

}

Output

2

3

5

7

11

13

0

0

0

0

# C#: break statement

‘break’ statement is used to come out of the loop.

Syntax

break;

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        for ( int i = 0 ; i < 10 ; i++)

        {

            if (i == 5 ) break ;

            Console.WriteLine(i);

        }

        Console.WriteLine("I am out of the loop");

    }

}

Output

0

1

2

3

4

I am out of the loop

# C#: continue statement

‘continue’ statement skips the current iteration of for, while, do-while, for-each loops.

Syntax

continue;

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        for ( int i = 0 ; i < 10 ; i++)

        {

            if (i % 2 == 0 ) continue ;

            Console.WriteLine(i);

        }

        Console.WriteLine("I am out of the loop");

    }

}

Output

1

3

5

7

9

I am out of the loop

# C#: Methods

Method is a block of statements, you can define method once and execute it any number of times.

Syntax

accessModifier returnType methodName(arguments){

         //Body Of the method

}

Don’t worry about accessModifier now, I will explain about this, after explaining about classes.

returnType is the value returned by the method, this can be any valid predefined (or) custom data type. If you don’t want to return any value from the method, make the return type as ‘void’.

methodName is any valid name which is not a C# keyword.

You can pass zero (or) more arguments to the method.

Example

int sum(int a, int b)

    {

        return a + b;

    }

int : Return type of the method sum

sum: Method name

int a, int b : Arguments to the method sum

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Program obj = new Program();

        int result1 = obj.sum( 10 , 5 );

        int result2 = obj.sub( 10 , 5 );

        int result3 = obj.mul( 10 , 5 );

        int result4 = obj.div( 10 , 5 );

        Console.WriteLine("Sum of 10 and 5 is {0}", result1);

        Console.WriteLine("Subtraction of 10 and 5 is {0}", result2);

        Console.WriteLine("Multiplication of 10 and 5 is {0}", result3);

        Console.WriteLine("Division of 10 and 5 is {0}", result4);

        obj.printEvenNumbers();

    }

    int sum ( int a, int b)

    {

        return a + b;

    }

    int sub ( int a, int b)

    {

        return a - b;

    }

    int mul ( int a, int b)

    {

        return a * b;

    }

    int div ( int a, int b)

    {

        return a/ b;

    }

    void printEvenNumbers ()

    {

        Console.WriteLine("Even Numbers from 0 to 10 are : ");

        for ( int i= 0 ; i< 10 ; i += 2 )

        {

            Console.WriteLine(i);

        }

    }

}

Output

Sum of 10 and 5 is 15

Subtraction of 10 and 5 is 5

Multiplication of 10 and 5 is 50

Division of 10 and 5 is 2

Even Numbers from 0 to 10 are :

0

2

4

6

8

Notify above snippet, methods are called using the instance (object) of the class Program.

        Program obj = new Program();

        int result1 = obj.sum(10, 5);

        int result2 = obj.sub(10, 5);

        int result3 = obj.mul(10, 5);

        int result4 = obj.div(10, 5);

Methods defined without ‘static’ keyword are called instance methods. Instance methods must be called by defining the object to a class. In the above example, sum, sub, mul, div, printEvenNumbers are the instance methods.

Following statement defines the objects to the class Program.

        Program obj = new Program();

## Static Methods

Methods defined using static keyword are called static methods. These are called class level methods. Static methods are called by class name.

Ex:

    static int sum(int a, int b)

    {

        return a + b;

    }

You can call above method by using ‘Program.sum(10, 5)’, where Program is the class name.

Program.cs

using System ;

class Program

{

    static void Main ( string [] args)

    {

        Program obj = new Program();

        int result1 = Program.sum( 10 , 5 );

        int result2 = Program.sub( 10 , 5 );

        int result3 = Program.mul( 10 , 5 );

        int result4 = Program.div( 10 , 5 );

        Console.WriteLine("Sum of 10 and 5 is {0}", result1);

        Console.WriteLine("Subtraction of 10 and 5 is {0}", result2);

        Console.WriteLine("Multiplication of 10 and 5 is {0}", result3);

        Console.WriteLine("Division of 10 and 5 is {0}", result4);

        Program.printEvenNumbers();

    }

    static int sum ( int a, int b)

    {

        return a + b;

    }

    static int sub ( int a, int b)

    {

        return a - b;

    }

    static int mul ( int a, int b)

    {

        return a * b;

    }

    static int div ( int a, int b)

    {

        return a/ b;

    }

    static void printEvenNumbers ()

    {

        Console.WriteLine("Even Numbers from 0 to 10 are : ");

        for ( int i= 0 ; i< 10 ; i += 2 )

        {

            Console.WriteLine(i);

        }

    }

}

Output

Sum of 10 and 5 is 15

Subtraction of 10 and 5 is 5

Multiplication of 10 and 5 is 50

Division of 10 and 5 is 2

Even Numbers from 0 to 10 are :

0

2

4

6

8

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

![](Image00005.jpg)

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

![](Image00006.jpg)

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

![](Image00007.jpg)

JavaScript: Check a number is prime or not

![](Image00008.jpg)

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

![](Image00009.jpg)

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

![](Image00010.jpg)

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

![](Image00011.jpg)

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

![](Image00012.jpg)

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

![](Image00013.jpg)

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