![](cover.jpeg)

Programming: C ++ Programming

Programming Language

For Beginners

LEARN IN A DAY!

2nd Edition

By Os Swift

© Copyright 2015 by Oswal Swift- All rights reserved.

In no way is it legal to reproduce, duplicate, or transmit any part of this document in either electronic means or in printed format. Recording of this publication is strictly prohibited and any storage of this document is not allowed unless with written permission from the publisher. All rights reserved.

The information provided herein is stated to be truthful and consistent, in that any liability, in terms of inattention or otherwise, by any usage or abuse of any policies, processes, or directions contained within is the solitary and utter responsibility of the recipient reader. Under no circumstances will any legal responsibility or blame be held against the publisher for any reparation, damages, or monetary loss due to the information herein, either directly or indirectly.

Respective authors own all copyrights not held by the publisher.

Legal Notice:

This book is copyright protected. This is only for personal use. You cannot amend, distribute, sell, use, quote or paraphrase any part or the content within this book without the consent of the author or copyright owner. Legal action will be pursued if this is breached.

Disclaimer Notice:

Please note the information contained within this document is for educational and entertainment purposes only. Every attempt has been made to provide accurate, up to date and reliable complete information. No warranties of any kind are expressed or implied. Readers acknowledge that the author is not engaging in the rendering of legal, financial, medical or professional advice.

By reading this document, the reader agrees that under no circumstances are we responsible for any losses, direct or indirect, which are incurred as a result of the use of information contained within this document, including, but not limited to, —errors, omissions, or inaccuracies.

Contents

Introduction

Chapter 1 - What is C++?

Introduction to programming languages

Machine language

Assembly language

High level language

What does this all mean to me?

Linux/Unix

Mac OS X

Windows

Is there anything else I should know?

Chapter 2: Basics of C++

Structure of C++ program

Functions

Libraries and the C++ standard library

Syntax and syntax errors

Compiling your first program

Size Changers

Sign Changers

Other Prefixes

Combining Types

Enumeration in C++

Chapter 3: Expanding ‘Hello, World!’

The New Program

Variables

Uninitialized variables

Chapter 4: Pointers

Pointers

What Are Pointers?

Using Pointers

C++ Pointers in Detail

Chapter 5: Functions

Return values

Returning to Main

Reusing functions

Nested functions

Function parameters

Revisiting expressions

Operators

Variable sizes and the sizeof operator

Char variable

Printing Chars as Integers (type casting)

Chapter 6: More About Operators

Arithmetic operators

Chapter 7: Control Flow Introduction

Conditionals

Loops

If statement:

If statements with logical operators

Switch statements

Break statement

Goto

While

The do-while loop

For loop

Break and continue

Using continue and break

Random number generation

Chapter 8: Storage classes

The auto Storage Class

The register Storage Class

The Static Storage Class

The extern Storage Class

Chapter 9: Arrays

int a[5]

Chapter 10: Classes ,objects and interfaces

Classes and Objects

Encapsulation

C++ Class Definitions

Define C++ Objects

Accessing the Data Members

Classes & Objects in Detail

Interfaces

Chapter 11: Templates

Templates

Function Template

Class Template

Chapter 12: Namespaces

Defining a Namespace

The using directive

Inside first_space

Discontiguous Namespaces

Nested Namespaces

Chapter 13: Inheritance

Base & Derived Classes

Access Control and Inheritance

Types of Inheritance

Multiple Inheritances

Chapter 14: Exception handling

Exception

Throwing Exceptions

Catching Exceptions

Flow of Control in the try/catch blocks

C++ Standard Exceptions

Define New Exceptions

Chapter 15: Preprocessor

The #define Preprocessor

Function-Like Macros

Conditional Compilation

The # and ## Operators

Predefined C++ Macros

Chapter 16: Multi-Threading

Creating Threads

Terminating Threads

Passing Arguments to Threads

Joining and Detaching Threads

Conclusion

# Introduction

C++ is perhaps one of the most formidable of all the computer languages but, with the right level of enthusiasm, and the right attitude, you can tame it and you can make it work for you. If you have already dabbled in the word of computer programming then you will already have heard of C++ and you will no doubt have heard people talking about how hard it is to learn, how you should never choose it as your first foray into learning computer-programming language.

Both of those statements are wrong. C++ is not all that difficult to learn once you understand the basics and it should absolutely be the first one you choose to get started on your journey to becoming a computer programmer. Yes, you are going to find some things that are difficult but there’s no fun in learning something that is so easy you can do it with your eyes shut. You need a challenge for it to sink in and, the more challenging the language is, the easier it will be to learn. 

There are other, much easier languages for you to start on, but none of them has the power or the flexibility of C++. To be fair, most operating systems, compilers, apps, drivers and a lot of other software are all written in C++, so why not make it your first port of call in learning a new computer programming language.

I’ll teach you to be a programmer in less than one day!

# Chapter 1 - What is C++?

## Introduction to programming languages

As you already know, the program is nothing but a set of instructions. These instructions are executed by the hardware that is the physical computer machinery. Though the modern computers are fast, they have their own limitations. Computers can only understand a set of instructions given in their native language. For this you should understand the concepts of machine language, assembly language and high-level languages.

## Machine language

Though the computers are very advanced machines, they cannot understand languages like C++ directly. A computer only understands 0s and 1s. They are called bits. And they can only understand instructions given in the binary format. Every set of instructions that we give to sleep you are translated into a set of instructions that tell the processor to do a particular job. You should understand that different types of processors have different types of instruction sets. For example, the Pentium processors will only understand their own instructions set. It is a similar case with Macintosh. In the very beginning, programmers had to write their instructions in the binary language. It was very time-consuming and difficult. Luckily, we don't have to go through all of that.

## Assembly language

As the machine language is very hard to deal with, a new language called the assembly language was invented. Here every instruction is given a short name and the variables are replaced by names and not by binary digits making it easy for a programmer to write code. You may ask that how you can understand and assembly language. It cannot. The assembly language will be converted into machine language with the help of an assembler. You should remember that each CPU has its own assembly language. So, the assembly language of a CPU cannot be run on a different CPU. Even assembly language has got its own drawbacks. They require large sets of instructions even for simple tasks.

## High level language

The high-level programming languages came into existence to solve those problems that the assembly and machine languages were causing. These can run on any computer. High-level languages come with a program called a compiler. The role of a compiler is to generate an executable file or a program that a CPU can directly understand. These programs are stand-alone programs. The modern compilers that are available today are very efficient and fast and converting the code into an executable format. Some of the programming languages use the interpreter. The job of an interpreter is to execute the code but without compiling it to the machine code. But here we won’t learn about an interpreter. Any given programming language can be interpreted or compiled. Languages like C, C++ and PASCAL are compiled while scripting languages like JavaScript and Perl are interpreted.

Ask this question and you will get a dozen different answers but, put simply, C++ is a compiled, object-orientated computer-programming language. If you are new to programming, even that has probably left you somewhat confused so let’s break it down a bit more.

There are two types of programming language – one is interpreted and the other is compiled. Interpreted languages are run on an interpreter – this reads the code and executes the commands inside one at a time. Compiled languages are read by the CPU in your computer instead of a program. Computers cannot read letters; they can only read binary numbers so, when you write your code, it has to be translated into binary first. This is called compiling. 

The object-orientated part of the explanation just describes how the code is structured but I will be going into more detail on that later on.

## What does this all mean to me?

To be successful at learning C++, you need to use both a text editor and a compiler. If you are using a Windows PC to do this on, you can use Notepad, which is already installed, on your computer as your text editor and, as your compiler, which is going to convert your code into a format that is executable, you should use GNU C/C++.

### Linux/Unix

A simple way to check whether GCC is installed on your Linux/Unix computer is to bring up the command line and type in:

*   $  g++  -v

If GCC is installed you will get the following message, or something very like it:

Using built-in specs

Target: i386-redhat-linux

Configured with: ../configure --prefix=/usr .......

Thread model: POSIX

gcc version 4.1.2 20080704 (Red Hat 4.1.2-46)

If GCC is not installed, you can follow the instructions on [http://gcc.gnu.org/install/](http://gcc.gnu.org/install/) to do so.

### Mac OS X

The best way to get GCC for Mac OS X is to go to [http://developer.apple.com/technologies/tools](http://developer.apple.com/technologies/tools), download xCode and follow the installation instructions.

### Windows

To get GCC on your Windows PC, you must first download MinGW from [http://www.mingw.org](http://www.mingw.org). Make sure you download the latest version of MinGW, as well as installing gcc-core, binutils, gcc-g++ and MinGW runtime – these are minimum requirements.

One more thing you could consider is an IDE – Integrated Developments Environment. This text editor features an integrated compiler and syntax highlighting. The best one to use is Code::Blocks.

## Is there anything else I should know?

Yes. C++ is very rigid in its syntax and everything is case sensitive so be careful what you are typing. In C++, the word “Hello” means something different to “hello” but this is something you will learn more about later on in the book. For now, let’s get straight on with the programming.

Before we go into too much detail, let’s get you started in writing a simple code. This is a common example for all types of computer programming tutorials, so, without further ado, let’s break it down. First of all, the code is written as such:

![](images/00001.jpeg)

Line 1 is telling your computer that you want to link iostream library to your program. The library is a repository where little bits of code are stored, along with variables and operators on occasion. The iostream library has code in it that lets us move characters to a text stream, which then appears on the screen.

Line 2 tells the computer that we want to use the standard namespace – this is where your code will be stored, useful if you write two bits of code with the same name,

Line 4 is the start of the code. Everything that goes inside the braces is what the compiler reads and translates – this line must go in very single program your write otherwise nothing is going to happen.

The next stage is the printing of the program, which, in this case is “Hello, World!” This is where we use some of the code stored in iostream – a piece of code called cout. The << that comes after the code is an operator and this one translates to “output” which means we are telling the computer to send the code to a specified stream. The printing “Hello, World!” is called a string, which is nothing more than a character sequence enclosed in double quotations. Notice that the line ends with a semi-colon – this is telling the computer that the code is finished and if it is not used, the program cannot be compiled.

Line 8 is always placed at the end of main and it is to inform the computer that the block is completed

Now that you have the source code for the program, it has to be compiled using your compiler. More detail later, first I want to start going over what makes up your code. The next chapter details all that you will need to learn to become a successful C++ programmer.

# Chapter 2: Basics of C++

## 
Structure of C++ program

As we have already discussed, a computer program is nothing but a set of instructions in sequence that tell the CPU what to do.

Statements and expressions:

In C++, the statement is nothing but the smallest and an independent unit in the program. It is also the most common form of instruction in a programming language. In C++, statements are away to convey your instructions to the compilers to carry out a specific task. We use ' ; ' to terminate a statement. In C++, there are many kinds of statements and some of the most common type of statements are given below.

int x;  

x = 5;

std::cout << x;

We will discuss about the functions of the above statements in the later chapters.

## Functions

Functions are nothing but statements in a sequence, which are executed in a sequential order. There is a function called the main function and it is a must in every C++ program. When any given C++ program is run, the execution of the program starts within the main function. Functions basically have very specific jobs to perform. And they can perform only those jobs. For you to become a good C++ programmer you need to know how to use functions efficiently. In the next chapter you’ll learn more about functions.

## Libraries and the C++ standard library

Libraries are nothing but a collection of code, which is pre-compiled. They can be used within different programs. If you wish to extend the capabilities of your program you can add libraries.

The core C++ language is a simple and minimalistic, but it also comes with the built-in library called the C++ standard library. The C++ standard library provides the user with additional functionalities.

## Syntax and syntax errors

We all know that in any language, sentences are constructed following the grammatical rules of that particular language. Take the example of the English language where you normally end of sentences in a period. All the rules, which govern the construction of sentences in a language, is called a syntax. Similarly, C++ also has a syntax. Not following the syntax will simply leave your code invalid. It is the responsibility of the compiler to see that the basic syntax of the C++ language is followed. If you violate the basic syntax, the compiler will compile the code and will complain the syntax violation. That issue is called as syntax error. The C++ compilers only compile the program if there are no syntax errors found. It will display all the errors that are found and suggests for you to make them valid so that it could execute the code without any errors.

## Compiling your first program

There are two important things that you should know before you can go to your first program.

1.  Your programs will be written in the .cpp files, which will be added to your project later. Projects are also called as workspaces or solutions. The code files and the IDE settings will be saved to your project.
2.  You should start a new project by creating one as there are many kinds of projects. Before starting you need to specify the type of project you wish to work on.
    What makes the C++ code?

A variable is something that stores a value. It’s like a box, each box has a name and category on it and the category is the type of item stored in it – the name is the specific variable. Each variable has a specific type, name and size and these govern exactly what can be stored inside of it. Before we go any further, here is a list of the variables that you will use:

*   Int - Whole numbers (integers)
*   Bool -               True or False (0 or 1)
*   Float -               Fractional number (reals)
*   Double - float with twice the precision
*   Char - A single ASCII character

Using Variables

The following code demonstrates how to use them:

![](images/00002.jpeg)

Most of this you saw with the last cod, the only bit you won’t have seen are lines 4 and 7 – line 4 declares the variable, in this case an integer. Declaring is simply telling the compiler that we are going to use this variable and we follow that with the name of the variable. You can call your variable whatever you like but keep it simple and relevant and make sure it is not a reserved keyword, which already has a meaning in C++. Start it with a lower case letter. The end of the statement is finished with the semi-colon.

Line 7 is called an assignment. This assigns a value to the variable and the = is the operator – this is what does the assigning. The value after the = is called a binary operator.

Note that there are no quotation marks around the cout statement this time. This is because, rather than displaying the string, we are outputting the value. Compiling the program now would print “42” on the screen.

As well as having a type a variable can also have a prefix added to the declaration and these change how the variable behaves. Some will change the size of the variable while others let you use or block you from using negative numbers, while others do a completely different job. Almost all of the will be talked about here.

## Size Changers

There are two specific prefixes that change the byte size of the variable – short and long. The idea behind this is to allow the variable to store more vales and bigger numbers. How big depends on the architecture of the computer that you are using:

*   On a 32-bit computer int and long int are both 4 bytes
*   On a 64-bit computer int is 4 bytes and long int is 8 bytes
*   On both architectures  short int is 2 bytes

There is nothing that dictates the size of the modifier for those particular keywords, except:

*   Short must be equal to or smaller than a normal variable
*   The normal variable must, in turn, be equal to or smaller than a long.
*   The only variable that can take a prefix is int

Even more confusing, you can actually omit int and just use long or short, for example:

1.  short int s = 0;
2.  int i = 0;
3.  long int l = 0;

5.  short s2 = 0;
6.  long l2 = 0;

## Sign Changers

There are two other prefixes that can restrict the values that are stored by a type – signed and unsigned. A signed variable can store negative and positive values, while an unsigned variable can only take positives. 

## Other Prefixes

There are some other prefixes that you can use in C++, not so common and most of which we are not going to use and will not cover in this book. There are two very useful ones though – const and static. The former are constant, never changing their value and the latter keeps the value of the variable the same but only in between function calls; that’s a topic for later on.

## Combining Types

Prefixes can be used in a chain together, so it wouldn’t be uncommon to see something like

1.  static unsigned long int, or
2.  signed const char

You can put the prefixes in any order you like provided they are before the variable type.

One more thing about variables – you can only use them in the area that they are declared in

## Enumeration in C++

In C++, an enumeration can be defined as a user defined type which can contain any one of the several name to constants (enumerators) given explicitly. The keyword enum is used for defining enumeration. The syntax for this is given below.

Syntax:

enum seasons { spring, summer, autumn, winter };

The above code is a declaration for enums. You can define your own variables after the declaration. Now we will consider an example of seasons where the variable of type seasons is declared and it can have any one of the four values (summer, spring, autumn and winter). Here is an example program in which the enumeration type is a defined and values can be assigned to the variable of that type.

Example:

#include <iostream>
using namespace std;

enum seasons { spring, summer, autumn, winter };

int main() {

   seasons s;
   s = autumn;   // Correct
   s = rainy;    // Error
   return 0;
}

In this program, there are four enumerators (spring, summer, autumn and winter) declared as the enum type seasons. A variable s is defined of the type seasons within the main () function and this variable is only capable of storing anyone of the given four variables (spring, summer, autumn and winter) and not others.

The default value of the first enumerator is 0, 1 for the second and so on. In this program the value of spring is equal to 0 and summer is 1 and the value of autumn is 2 and the value of winter is 3\.

Here, there is one thing that you should keep in mind is that spring, summer, autumn and winter are not variables. The compiler will treat them as integers. The values cannot be changed once the enumerators are defined in program. Consider this example.

Example 1: C++ Enumeration

#include <iostream>
using namespace std;

enum seasons { spring, summer, autumn, winter };

int main() {

   seasons s;

   s = spring;
   cout >> "spring = " >> s >> endl;

   s = summer;
   cout >> "summer = " >> s >> endl;

   s = autumn;
   cout >> "autumn = " >> s >> endl;

   s = winter;
   cout >> "winter = " >> s >> endl;

   return 0;
}

Output

spring = 0
summer = 1
autumn = 2
winter = 3

The default value can be changed during the enumeration declaration and you can give your desired value. Consider the example given below.

Example 2: C++ Enumeration

#include <iostream>
using namespace std;

enum seasons { spring = 34, summer = 4, autumn = 9, winter = 32};

int main() {

   seasons s;

   s = summer;
   cout << "summer = " << s << endl;

   return 0;
}

Output

summer = 4

In this program, the integer value given by the enumeration is different from the default value.

#  Chapter 3: Expanding ‘Hello, World!’

Now that we know how variables work, it is time to start using them in a program. Right now though, all we can do is set the value of a variable and output it, which isn’t all that useful when it comes to creating proper C++ programs. What we need is a way to manipulate the variables and get input, which is where the iostream library comes in.

We know that this library is capable of outputting data but it is also able to receive input data. The command that allows it to do this is cin, opposite of cout. The difference is, the operator after cin is reversed – instead of <<, we type >>.

1.  cout << "string";
2.  cout << var;

4.  cin >> var;

iostream is more powerful that that though and allows you to combine multiple statements. For example, if you wanted to output two strings or variables, you would write two statements. With iostream, you can combine multiple cout statements together to produce code that is much shorter:

1.  cout << "Hello, " << "World!";

You can do the same with cin statements but remember that you cannot mix inputs and outputs on one line.

## The New Program

Now we know how to input and output data we can write programs that are a bit more useful. With this example, we are going to improve on the “Hello, World!” program:

![](images/00003.jpeg)

You can see that we have declared iostream in the standard namespace and we have then declared some variables but in a slightly different way to before by combining and assignment with the declaration – this is called initialization.

The rest is the code and, in this case, the computer program is going to ask the user how old they are, inviting user input into the program. It goes on to ask what the users favorite letter of the alphabet is. Note the use of the \ followed by n – this indicates a new line is needed.

## Variables

In C++, available is nothing but a piece of memory which can be used for storing information. Information can be stored and retrieve using variables. Whenever a new variable is assigned, some part of the RAM memory is allocated to that variable. There are different types of variables that have a specific purpose for each. For characters there a character variables, for numbers there are integer variables, for decimals we have float variable etc.

You should use a declaration statement if you wish to define a variable.

We will have a look at the int variable for your better understanding of variables.

int x;

This is nothing but defining x with an integer variable. The purpose of an integer variable is to store numerical data.

Here is an example of assignment statements

int y;                    // define y as an integer variable

y = 4;                    // 4 evaluates to 4, which is then assigned to y

y = 2 + 5;                // 2 + 5 evaluates to 7, which is then assigned to y

int x;                   // define x as an integer variable

x = y;                    // y evaluates to 7 (from before), which is then assigned to x.

x = x;                    // x evaluates to 7, which is then assigned to x (useless!)

x = x + 1;                // x + 1 evaluates to 8, which is then assigned to x.

## Uninitialized variables

In languages like C and C++, a variable does not initialize with a standard value like 0\. It will have a default garbage value assigned to it. And this kind of variable is called as an uninitialized variable.

# Chapter 4: Pointers

## Pointers

Pointers in C++ are easy and interesting to learn. Some tasks can be performed easily in C++ using pointers and there are some other tasks that cannot be done without using pointers.

As you already know, in C++ every variable is given a memory location and an address is defined for every memory location. Every variable can be accessed using its memory location by using the ‘&’ operator. The ‘&’ operator is used for denoting a memory address. Here, in the following example, the addresses of the variables will be defined.

Example:

#include <iostream>

using namespace std;

int main ()
{
  int  var1;
  char var2[10];

  cout << "Address of var1 variable: ";
  cout << &var1 << endl;

  cout << "Address of var2 variable: ";
  cout << &var2 << endl;

  return 0;
}

When you compile and execute the above code, it will produce the following output.

Address of var1 variable: 0xbfebd5c0
Address of var2 variable: 0xbfebd5b6

## What Are Pointers?

Appointed can be defined as a variable that contains the address of another variable. Before working with pointers, it should be declared just like any other variable or constant. The general syntax for declaring a pointer variable is given below.

Syntax:

type *var-name;

Here, the base of the pointer should be given and it should be a valid type in C++. The pointer variable's name is var-name. The asterisk that is used for declaring a pointer is the same that is used for the multiplication operations. The function of the asterisk varies here. It is used for designating given variable as a pointer. Some of the valid pointer declarations are given below.

int    *ip;    // this is a pointer to an integer

double *dp;    // this is a pointer to a double

float  *fp;    // this is a pointer to a float

char   *ch     // this is a pointer to a character

The data type of the given variable or a constant which given pointer points to is the only difference between the pointers of different data types.

## Using Pointers

Using pointers, there are a few of the important and frequently used operations. (a) The pointer variables will be defined. (b) The pointer will be assigned with the address of a given variable and (c) now, the value of the pointer variable at the given address can be accessed. For doing this, we use the unary operator asterisk (*). The * operator Will return the value of the pointer variable that is located at the specified address. Here are a few examples.

Examples:

#include <iostream>

using namespace std;

int main ()
{
  int  var = 20;   // actual variable declaration.
  int  *ip;        // pointer variable

  ip = &var;       // store address of var in pointer variable

  cout << "Value of var variable: ";
  cout << var << endl;

  // print the address stored in ip pointer variable
  cout << "Address stored in ip variable: ";
  cout << ip << endl;

  // access the value at the address available in pointer
  cout << "Value of *ip variable: ";
  cout << *ip << endl;

  return 0;
}

When you compile and execute the above code, it will produce the following output.

Value of var variable: 20
Address stored in ip variable: 0xbfc601ac
Value of *ip variable: 20

## C++ Pointers in Detail

Now, let us go into the details of pointers in C++. In C++ programming, pointers are very important. The concepts of pointers are many but easy. If you wish to become a good C++ programmer, you should know the important pointer concepts given below.

| Concept | Description |
| [C++ Null Pointers](http://www.tutorialspoint.com/cplusplus/cpp_null_pointers.htm) | The null pointer is supported by C++. The value of a null pointer is zero and it is defined in several of the standard libraries. . |
| [C++ pointer arithmetic](http://www.tutorialspoint.com/cplusplus/cpp_pointer_arithmatic.htm) | You can use for arithmetic operations on pointers. They are +,-,++ and -- |
| [C++ pointers vs. arrays](http://www.tutorialspoint.com/cplusplus/cpp_pointers_vs_arrays.htm) | Pointers and arrays share a close relationship between them. We will see how. |
| [C++ array of pointers](http://www.tutorialspoint.com/cplusplus/cpp_array_of_pointers.htm) | Arrays can be defined for holding a set of pointers. |
| [C++ pointer to pointer](http://www.tutorialspoint.com/cplusplus/cpp_pointer_to_pointer.htm) | In C++, you are allowed to have a pointer on a different pointer and this continues. |
| [Passing pointers to functions](http://www.tutorialspoint.com/cplusplus/cpp_passing_pointers_to_functions.htm) | By passing an argument by address or an argument by reference, The argument passed can be changed by the called function in the calling function. |
| [Return pointer from functions](http://www.tutorialspoint.com/cplusplus/cpp_return_pointer_from_functions.htm) | in C++, a pointer can be returned by a function to a static variable, local variable and to dynamically allocated memories too. |

Chapter 5: Functions

Functions are nothing but statements that can be reused for doing a particular job, as you are already aware of using the main () function. Sometimes you will need your program to stop what it is doing and do something else in order to work efficiently. This is something that we always do. For example you might be working on something and pause it to grab some coffee. This is a similar case in case of C++ programming when using functions.

It will continue to run the statements in a sequential manner until it encounters a function call. A function call is nothing but an expression, which instructs the CPU to pause the current function in order to execute a different function. The CPU will just interrupt the current function and will carry on with the execution of the function, which is mentioned in the function called. Once the function in the functional call is terminated, the CPU will go back to the execution of the previous function on which it was working.

Here, there is an example programme, which shows you how you functions are defined and called.

![](images/00004.jpeg)

The above code will display the following output:

![](images/00005.jpeg)

## Return values

After the main finishes the execution of the code, it will return the value back to the caller. This can be done by making use of a return statement. If the return type of function is void, it will not return any value. If the return type is int, it will return an integer value.

For example:

![](images/00006.jpeg)

Here is an example where these functions are used in a program.

![](images/00007.jpeg)

As you can see, in the first function call, the value 5 is returned using the return5() statement. There, the value 5 will be returned to the caller and the same value will be passed to the cout statement.

When it comes to the second function call, return5 () is executed and 5 is returned. Then 5+2 is carried out and 7 is sent to the cout statement.

When coming to the third statement, returnNothing () is called and it will simply not return anything.

When it comes with fourth function call, the function returns nothing and the control goes back to the main ().

## Returning to Main

When a program is executed, the OS will make the function call to the main () function. Then the execution will jump back to the top of the name and the statements that are present in the main will be executed in a sequential manner. Finally, an integer value will be returned back to the main. This is the reason why the main() is defined as int main(). Always be careful not to use ' ; ' next to the main function as it will terminate the main function and will not I love the execution of the program to go any further. When you are using void main(), the compiler doesn't care about the return function and only will return nothing.

## Reusing functions

Functions in C++ not confined by the number of times that they can be used. The same function can be used over and over again. In fact, in most of the programs, the functions will have to be reused.

Here is an example

![](images/00008.jpeg)

The output of the above program is

![](images/00009.gif)

You should remember that the main() function is not the only function that can call its other functions. Any function can call on a different function.

Here is an example function showing that

![](images/00010.jpeg)

The output is:

![](images/00011.jpeg)

## Nested functions

Nested functions are nothing but functions, which have other functions within them. In simple words, a function in the function is a nested function.

The below example will show you a simple nested function:

![](images/00012.jpeg)

## Function parameters

You will need to pass formation into function sometimes. In such cases, parameters will allow you to pass information to a function.

Here is an example that would explain the role of parameters in the function.

![](images/00013.jpeg)

The output is 9\.

Now we will have a look at some other calls to functions():

![](images/00014.jpeg)

The output is

![](images/00015.jpeg)

## Revisiting expressions

An expression can be defined as a combination of variables, letters, functions, and operators that evaluate to a value.

We will talk about each in detail.

*   Literals: A literal is nothing but a value that is generally fixed, that is directly inserted into the source code. Literals will have no memory representation and they always evaluate to themselves.

Example:

![](images/00016.jpeg)

## Operators

We now know how to output text, declare a variable and receive inputs but, at the moment, we cannot do anything with the variables. What we need to be able to do is manipulate the variables without having to do too much work and that’s where operators come in.

Operators are the last of the expressions. These are the ones that tells the expression the ways of combining the operands within the intention of producing new results. For example, 3+4 is an expression where we use the + operator. The operands 3 and 4 combine and produce 7\. Similarly there are all standard arithmetic operators in C++. They are addition (+), multiplication(*) , subtraction(-), division(/) and assignment(=).

The operators usually come in three different types

*   Unary: these operators, which act on a single operand. Eg. -being applied to a number 2\. This gives -2\.
*   Binary: these operators, which act on two different or same operands. Here the above example we used the expression 3+4\. There to operands combine and produce a result.
*   Ternary: these are operators, which act on three operands. There is only one of these in C++

## Variable sizes and the sizeof operator

The memory in a computer is basically organized into units of the byte size. Each of those memory blocks will have its own address, which is unique. Some variables take just 1 byte of memory. Some take 2, 4, 8 and so on. It is only wise to use the variable of the required size. As each bit can only represent 0 or 1, we can say that it can only store two possible values. In the same way, three bits can hold eight possible values. This way there will be a limit on the data that can be stored in a given variable. As all the computers have limited amount of data that they can store, we use variables with different sizes so that there won't be memory wastage.

The sizes of the basic data types in C++

| Category | Type | Minimum Size |
| Boolean | bool | 1 byte |
| character | char | 1 byte |
|  | wchar_t | 1 byte |
|  | char16_t | 2 bytes |
|  | char32_t | 4 bytes |
| integer | short | 2 bytes |
|  | int | 2 bytes |
|  | long | 4 bytes |
|  | long long | 8 bytes |
| floating point | float | 4 bytes |
|  | double | 8 bytes |
|  | long double | 8 bytes |

We cannot say that the size of all the variables is same on all computers. The sizes of variables vary from machine to machine. You can know the size of the variables on your machine with the help of the operator called the sizeof operator in c++.

For finding the size of the variables on your computer you can use the following code.

![](images/00017.jpeg)

The results will mostly turn out to be:

![](images/00018.jpeg)

Here even look at some of the variables.

Integers: as per the definition, an integer datatype variable is something which can hold only non-factional numbers. There are five different types of fundamental integers.

| Category | Type | Minimum Size |
| character | char | 1 byte |
| integer | short | 2 bytes |
|  | int | 2 bytes |
|  | long | 4 bytes |
|  | long long | 8 bytes |

Defining integers:

char c;

short int si; // valid

short s;      // preferred

int i;

long int li; // valid

long l;      // preferred

long long int lli; // valid

long long ll;      // preferred

There are two types of variables. They are 'signed' and 'unsigned'. With the following table, you will have a better understanding of signed and unsigned variables.

| Size/Type | Range |
| 1 byte signed | -128 to 127 |
| 1 byte unsigned | 0 to 255 |
| 2 byte signed | -32,768 to 32,767 |
| 2 byte unsigned | 0 to 65,535 |
| 4 byte signed | -2,147,483,648 to 2,147,483,647 |
| 4 byte unsigned | 0 to 4,294,967,295 |
| 8 byte signed | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| 8 byte unsigned | 0 to 18,446,744,073,709,551,615 |

Booleans: Boolean is also a type in C++. It can hold only two possible values, true or false. We use the keyword bool for declaring the Boolean variable. Eg: bool b;

We use this data type for decision making algorithms where the machine will decide the result basing on the given conditions. Here is an example where we use the Boolean datatype.

![](images/00019.jpeg)

The outputs are:

![](images/00020.jpeg)

You can also print the values 'true' or 'false' in place of 0 or 1 by using the std::boolalpha in the iomanip header. For example:

![](images/00021.jpeg)

This will display

![](images/00022.jpeg)

You can also use Booleans with the ‘if’ statement. Here is a sample code.

![](images/00023.jpeg)

Result: b is True

![](images/00024.jpeg)

You should keep in mind that in C++, ‘=’ means an assignment operator and ‘==’ means it is an comparator operator testing for equity.

## Char variable

Though char is a type of an integer datatype, it is different from other integer variables. Each char holds 1 byte of memory. We won't represent it as an integer, but in the form of an ASCII character. Given below is the full table of the ASCII characters.

| Code | Symbol | Code | Symbol | Code | Symbol | Code | Symbol |
| 0 | NUL (null) | 32 | (space) | 64 | @ | 96 | ` |
| 1 | SOH (start of header) | 33 | ! | 65 | A | 97 | a |
| 2 | STX (start of text) | 34 | ” | 66 | B | 98 | b |
| 3 | ETX (end of text) | 35 | # | 67 | C | 99 | c |
| 4 | EOT (end of transmission) | 36 | $ | 68 | D | 100 | d |
| 5 | ENQ (enquiry) | 37 | % | 69 | E | 101 | e |
| 6 | ACK (acknowledge) | 38 | & | 70 | F | 102 | f |
| 7 | BEL (bell) | 39 | ’ | 71 | G | 103 | g |
| 8 | BS (backspace) | 40 | ( | 72 | H | 104 | h |
| 9 | HT (horizontal tab) | 41 | ) | 73 | I | 105 | i |
| 10 | LF (line feed/new line) | 42 | * | 74 | J | 106 | j |
| 11 | VT (vertical tab) | 43 | + | 75 | K | 107 | k |
| 12 | FF (form feed / new page) | 44 | , | 76 | L | 108 | l |
| 13 | CR (carriage return) | 45 | - | 77 | M | 109 | m |
| 14 | SO (shift out) | 46 | . | 78 | N | 110 | n |
| 15 | SI (shift in) | 47 | / | 79 | O | 111 | o |
| 16 | DLE (data link escape) | 48 | 0 | 80 | P | 112 | p |
| 17 | DC1 (data control 1) | 49 | 1 | 81 | Q | 113 | q |
| 18 | DC2 (data control 2) | 50 | 2 | 82 | R | 114 | r |
| 19 | DC3 (data control 3) | 51 | 3 | 83 | S | 115 | s |
| 20 | DC4 (data control 4) | 52 | 4 | 84 | T | 116 | t |
| 21 | NAK (negative acknowledge) | 53 | 5 | 85 | U | 117 | u |
| 22 | SYN (synchronous idle) | 54 | 6 | 86 | V | 118 | v |
| 23 | ETB (end of transmission block) | 55 | 7 | 87 | W | 119 | w |
| 24 | CAN (cancel) | 56 | 8 | 88 | X | 120 | x |
| 25 | EM (end of medium) | 57 | 9 | 89 | Y | 121 | y |
| 26 | SUB (substitute) | 58 | : | 90 | Z | 122 | z |
| 27 | ESC (escape) | 59 | ; | 91 | [ | 123 | { |
| 28 | FS (file separator) | 60 | < | 92 | \ | 124 | &#124; |
| 29 | GS (group separator) | 61 | = | 93 | ] | 125 | } |
| 30 | RS (record separator) | 62 | > | 94 | ^ | 126 | ~ |
| 31 | US (unit separator) | 63 | ? | 95 | _ | 127 | DEL (delete) |

Printing Chars:

![](images/00025.jpeg)

Output: a

## Printing Chars as Integers (type casting)

If you wish to print char as numbers you'll have to type cast them. Typecasting is nothing but changing the datatype of a variable.

![](images/00026.jpeg)

We use the static cast for creating an integer value from a given char value

![](images/00027.jpeg)

Result

:  ![](images/00028.jpeg)

# 
Chapter 6: More About Operators

For you to become a good programmer, you must understand the order and application of the operators. For example 2+3*4 gives you 20 and 2+(3*4) will give you 24\. So you should know the correct order in which you can use the operators. For making it easy all operators were given precedence. Here is the table that gives you the precedence of all the operators that we use in C++. The precedence level 1 is the greatest of all and the precedence level of 18 is the lowest of all.

| Prec/Ass | Operator | Description | Pattern |
| 1 None | :::: | Global scope (unary)Class scope (binary) | ::nameclass_name::member_name |
| 2 L->R | ()()()type()[].->++––typeidconst_castdynamic_castreinterpret_caststatic_cast | ParenthesisFunction callInitializationValue constructionArray subscriptMember access from objectMember access from object ptrPost-incrementPost-decrementRun-time type informationCast away constRun-time type-checked castCast one type to anotherCompile-time type-checked cast | (expression)function_name(parameters)type name(expression)type(expression)pointer[expression]object.member_nameobject_pointer->member_namelvalue++lvalue––typeid(type) or typeid(expression)const_cast<type>(expression)dynamic_cast<type>(expression)reinterpret_cast<type>(expression)static_cast<type>(expression) |
| 3 R->L | +-++––!~(type)sizeof&*newnew[]deletedelete[] | Unary plusUnary minusPre-incrementPre-decrementLogical NOTBitwise NOTC-style castSize in bytesAddress ofDereferenceDynamic memory allocationDynamic array allocationDynamic memory deletionDynamic array deletion | +expression-expression++lvalue––lvalue!expression~expression(type)expressionsizeof(type) or sizeof(expression)&lvalue*expressionnew typenew type[expression]delete pointerdelete[] pointer |
| 4 L->R | ->*.* | Member pointer selectorMember object selector | object_pointer->*pointer_to_memberobject.*pointer_to_member |
| 5 L->R | */% | MultiplicationDivisionModulus | expression * expressionexpression / expressionexpression % expression |
| 6 L->R | +- | AdditionSubtraction | expression + expressionexpression - expression |
| 7 L->R | <<>> | Bitwise shift leftBitwise shift right | expression << expressionexpression >> expression |
| 8 L->R | <<=>>= | Comparison less thanComparison less than or equalsComparison greater thanComparison greater than or equals | expression < expressionexpression <= expressionexpression > expressionexpression >= expression |
| 9 L->R | ==!= | EqualityInequality | expression == expressionexpression != expression |
| 10 L->R | & | Bitwise AND | expression & expression |
| 11 L->R | ^ | Bitwise XOR | expression ^ expression |
| 12 L->R | &#124; | Bitwise OR | expression &#124; expression |
| 13 L->R | && | Logical AND | expression && expression |
| 14 L->R | &#124;&#124; | Logical OR | expression &#124;&#124; expression |
| 15 L->R | ?: | Conditional | expression ? expression : expression |
| 16 R->L | =*=/=%=+=-=<<=>>=&=&#124;=^= | AssignmentMultiplication assignmentDivision assignmentModulus assignmentAddition assignmentSubtraction assignmentBitwise shift left assignmentBitwise shift right assignmentBitwise AND assignmentBitwise OR assignmentBitwise XOR assignment | lvalue = expressionlvalue *= expressionlvalue /= expressionlvalue %= expressionlvalue += expressionlvalue -= expressionlvalue <<= expressionlvalue >>= expressionlvalue &= expressionlvalue &#124;= expressionlvalue ^= expression |
| 17 R->L | throw | Throw expression | throw expression |
| 18 L->R | , | Comma operator | expression, expression |

## Arithmetic operators

Unary arithmetic operators: these are arithmetic operators which take only one operand. Here is the table of unary operators.

| Operator | Symbol | Form | Operation |
| Unary plus | + | +x | Value of x |
| Unary minus | - | -x | Negation of x |

Binary operators

When it comes to operators, there are basically five types. They are addition, subtraction, division, multiplication and modulus. Each of them is explained in the table given below.

| Operator | Symbol | Form | Operation |
| Addition | + | x + y | x plus y |
| Subtraction | - | x - y | x minus y |
| Multiplication | * | x * y | x multiplied by y |
| Division | / | x / y | x divided by y |
| Modulus (Remainder) | % | x % y | The remainder of x divided by y |

We already know about the basic arithmetic operators like addition, subtraction, division and multiplication. But most of us may not have an idea about modulus. The modulus operator is also known by the name remainder operator. This operator will return the reminder on the integer operands. We use this operator for testing if a number is even or odd. If the remainder is 0 the number is even and if the remainder is 1 the number is an odd number.

Here is an example where every number from 1 to 100 are printed with 20 numbers in a line.

![](images/00029.jpeg)

Result

![](images/00030.jpeg)

Relational operators (comparisons)

The relational operators are used for comparison between variables. There are a total of six relational operators in C++. They are given in the table below.

| Operator | Symbol | Form | Operation |
| Greater than | > | x > y | true if x is greater than y, false otherwise |
| Less than | < | x < y | true if x is less than y, false otherwise |
| Greater than or equals | >= | x >= y | true if x is greater than or equal to y, false otherwise |
| Less than or equals | <= | x <= y | true if x is less than or equal to y, false otherwise |
| Equality | == | x == y | true if x equals y, false otherwise |
| Inequality | != | x != y | true if x does not equal y, false otherwise |

These operators operate on the Boolean values true or false. For your better understanding of operators, a sample code is given below which has integers and relational operators.

![](images/00031.jpeg)

The output for the above code is:

![](images/00032.gif)

Bitwise operators

Within a given variable, the bit manipulation operators are used to manipulate the bits of data. Earlier days computers did not have much storage capacities and memory was very expensive. So to bitwise operators were created to solve this problem. In total, we have six bit manipulation operators. They explained in the table below.

| Operator | Symbol | Form | Operation |
| left shift | << | x << y | all bits in x shifted left y bits |
| right shift | >> | x >> y | all bits in x shifted right y bits |
| bitwise NOT | ~ | ~x | all bits in x flipped |
| bitwise AND | & | x & y | each bit in x AND each bit in y |
| bitwise OR | &#124; | x &#124; y | each bit in x OR each bit in y |
| bitwise XOR | ^ | x ^ y | each bit in x XOR each bit in y |

In C++, we also have Bitwise assignment operators. These help the users with easy variable modifications.

| Operator | Symbol | Form | Operation |
| Left shift assignment | <<= | x <<= y | Shift x left by y bits |
| Right shift assignment | >>= | x >>= y | Shift x right by y bits |
| Bitwise OR assignment | &#124;= | x &#124;= y | Assign x &#124; y to x |
| Bitwise AND assignment | &= | x &= y | Assign x & y to x |
| Bitwise XOR assignment | ^= | x ^= y | Assign x ^ y to x |

Blocks

A block is nothing but a block of statements. The block is also known by the name compound statement. It is nothing but a group of statements that are considered to be a single statement by the compilers. They begin and end with {and} symbols. These compound statements can be used anywhere in place of the statements. These do not need a; to terminate the statement. These blocks can be placed separately or they can also be placed inside another block. These kinds of blocks are called as nested blocks. Here are some examples of blocks in the sample code given below.

![](images/00033.jpeg)

Here is an example of a nested block.

![](images/00034.jpeg)

Using blocks is really simple. You can place blocks inside the block which is in turn inside another block. Here is an example to show a block in a block in a block.

![](images/00035.jpeg)

There is no limit for how many blocks you can place inside a block. But it is advised to only keep three or four blocks deep.

In simple words, operators can be described as-

Operators are little characters that make the program functional. We have already looked at two operators that are linked to iostream library - >> and << - or input and output operators but there are lots more, most of them extremely useful. The operators can be categorized, the first ones of which are arithmetic operators. These do exactly what it says on the box – perform arithmetic. They are, quite simply, the +, -, / and * signs and you use them in the same way as you do in written math’s. For example, you can add two numbers together:

![](images/00036.jpeg)

The other signs are used the same way and you can combine them together in one statement if you like, as such:

*   var = 6 + 5 * 9 - 33 / 2;

What you do have to be aware of is that C++ processed the commands in a specific order so be sure, when you are writing your code, that it will end in the result that you want. It is easier not to mix your arithmetic operators in a single statement or to not use parentheses – these are what tell C++ to do things in a certain order and C++ will always action what is inside the parentheses first.

There are other arithmetic operators you can use, such as %, or ++, or --. The first is called a modulo and is similar to division but returns the remainder instead of the answer. This is a specialized operator, more for advanced programming so not really for this book. The remaining two operators do as they say – one is a decrement and one is an increment and they either decrease or increase a number by 1.

# Chapter 7: Control Flow Introduction

Went to sleep you starts execution of the program code, it starts from the main function and terminates at the end of the code, which is usually the end of main function. The statements that are executed in sequence are nothing but the part of the program. Most of the programs, which we have learned until now are simple straight line programs. These programs have a steady and sequential flow.

To break the flow of control, we have control flow statements in C++. Please control flow statements help the programmer to change the path of the CPU. Some of the control flow statements discussed below.

*   Halt: this is the most widely used and the basic control statement in C++. You can perform a halt with the exit function. The exit functional is defined in the header cstdlib. Here is a small example showing the use of exit function.

![](images/00037.jpeg)

In the above sample code the flow of control is broken and it will never reach the statements that are written below the exit statement. These types of statements give the programmer the authority to stop the program when required.

Jumps: Jump is also a basic controls statement in C++. Using this statement will make the CPU to jump to a different statement. Continue, break and goto are used to perform different types of jumping operations.

Conditional branches: these are flow control statements which change the part of the flow of control depending on the value of a given expression. The ‘if’ statement is the most basic type of the conditional branch statements. Example:

![](images/00038.jpeg)

In the sample code given above, there are two possible paths the flow of control can take. If it is it true the CPU will go and execute A, B and D. But if the condition turns out to be false the flow of control will go and execute A, C and D statements.

## Conditionals

Conditionals allow you to form a junction in the code and send it off on various paths, rather than keeping it as a linear code. C++ conditionals are if statements - if something is false, the program should execute one piece of code, another if it is true:

![](images/00039.jpeg)

You know what lines 1 and 5 mean but line 3 is a little different – this is an if statement. What it is doing is checking to see if the integer variable is less than 2\. If it is, it will run one piece of code, if not, it will carry on as normal. If you compile and run what is written here, you will see printed on your screen “a is less than 2!”.

## Loops

Loops are used in the programs where the code is to be used repeatedly. They will put the code into a loop till the condition is satisfied. Imagine if you have to write a code, which prints numbers from 1 to 100 in a new line each. Writing the code for such programs will be very difficult and time taking. For such situations we use loops. Loops keep the flow of control in the loop till the condition is satisfied.

So our code now reads user inputs, it can do a variety of different things based on those inputs but now we are going to look at making that code do the same things over and over again but with slightly different parameters. To do this, we need to use a loop, which is a piece of code that is repeated a number of different times until it’s achieved what it needed to do and a specific C++ condition has been met. C++ has three different types of loop:

*   while
*   for
*   do

The while loop is the easiest and looks very similar to an if statement:

![](images/00040.gif)

What the while loop is doing here is saying that while whatever the user input variable is not equal to 10, the ode needs to get some input from the user. In C++, the exclamation mark (!) means not, so ! = means not equal.

In this case, if the user input had already been 10 then the code would not have been executed and the loop will be ignored. In all truthfulness, the while loop is just seen as an extended if statement that goes back inside of itself after the code is run.

Before we move on, I want to show what an infinite loop looks like, a loop that just keeps on going:

![](images/00041.gif)

As you can see, it is saying that if 1 is equal to 1, print an a, and so on.

The next easiest loop is the do while loop, as it is similar to the while loop.

![](images/00042.gif)

While it looks somewhat different to the while loop, it is doing essentially the same job with one important difference – the while loop checks a conditional and looks to see if it is true but the do while loop runs code and then checks if the conditional is true or not. Because of this, all of the code is guaranteed to run.

The third type of C++ loop is for and this one is the most complicated one. Once you understand it though, you will find that it is the most powerful. Here, we are just going to look at simple usage:

![](images/00043.gif)

What this code is saying is, start off by setting the value of i to 2\. Then it goes on to say that, as long as i is less than 10 it should output the value onto the screen and then increment i. You must bear one thing in mind – all of the variables that are used in the first line of a for loop have to be the same variable. It is also important to remember that, unlike a while loop, the first statement is an assignment and not a conditional.

This sort of loop is useful if you want to get through a number of pieces of data and I’ll talk more about that in the next section. For now, as you can see, the most useful thing it can do is chuck out a sequence of numbers. That is a useful talks and it brings us neatly on to the next section.

## If statement:

The ‘if’ statement is the most basic condition right statement in C++. It will check for a given condition and will change the flow of control depending on the outcome of the condition.

Here is a simple code which has an ‘if’ statement and it.

![](images/00044.gif)

We already know that if statement takes a statement as the condition. We also know that we can use a block in place of a single statement. This means we can use a Block inside an if statement as a condition. The following example shows a Block being used in an if statement as a condition.

![](images/00045.jpeg)

You can also place one if statement inside another if statement. An if statement which has another if statement in it is called a nested if.

Here are two examples, which will help you to understand the nested if better.

Example 1:

![](images/00046.jpeg)

Example 2:

![](images/00047.jpeg)

You can encase an if statement into a block and you can attach an else statement to it. You can see how with the below example.

![](images/00048.jpeg)

## If statements with logical operators

You can use if statements with logical operators for checking multiple conditions at the same time. The sample code is given below.

Example:

![](images/00049.jpeg)

‘if’ statements can be used for performing early returns. Early returns are nothing but getting the control back to the caller before the Flood control reaches the end of the function.

![](images/00050.jpeg)

## Switch statements

Switch statements are also no control statements that change the flow of control of the program. Switch statement uses the multi-way branch.

When compared to the ‘if else if’ statements, switch statements are superior because of the following reasons.

*   Switch statements are easier to debug.
*   These are easy to maintain
*   Switch statements have a faster execution capacity
*   There are easy to read
*   The depth in case of the switch statement is fixed.
*   Can be used for exception handling

The basic syntax of the switch statement is given below.

case constant1:

  code/s to be executed if n equals to constant1;

  break;

case constant2:

  code/s to be executed if n equals to constant2;

  break;

  .

  .

  .

default:

  code/s to be executed if n doesn't match to any cases;

The following program shows you why the switch case is easier to use when compared to the if-else statements.

Example:

![](images/00051.jpeg)

Now look at the same problem done using the switch statement.

![](images/00052.jpeg)

## Break statement

We often use the break statement for terminating the case statement without the entire function been terminated. This will give an instruction to the compiler to abandon the current switch case and proceed with the execution of the next statement. So after a break statement the flow of control goes to the statement that is after the switch block. Here is an example showing the break statements attached after the case statements.

![](images/00053.jpeg)

## Goto

For making the CPU to jump to a different spot in the code we make use of the flow control statement called the goto statement. For this we need to set a spot which we goto statement can identify it as a statement label. The following example if there is a negative number entered the goto statement will take the flow of control to the tryAgain label where they will have to choose nonnegative number.

Example 1:

![](images/00054.jpeg)

Example 2:

![](images/00055.jpeg)

## While

Of all the three loops, while is the simplest of all. The while loop is very much similar to the ‘if’ statement. Here the condition will be given after the while statement. This will take the flow of control to the beginning of the program and will put it in a loop till the condition is satisfied.

Every time the loop goes back to the beginning after a successful execution of the code, it is said that and iteration is done.

Example:

![](images/00056.jpeg)

The output will be:

![](images/00057.jpeg)

Here is another simple example of a while loop.

![](images/00058.jpeg)

Output:

![](images/00059.jpeg)

Like the ‘if’ condition, you can use a loop inside another loop. If you place a loop inside another loop it is called a nested loop.

Example of a nested loop:

![](images/00060.gif)

The above program will display.

![](images/00061.jpeg)

## The do-while loop

The do-while loop is similar to the while loop except at one part. If the condition in the while loop is not satisfied, we know that it won't execute the loop. But if we want our code to run at least once even if the condition is not satisfied, we can make use of the do-while loop in C++. Using this loop will execute the code once even if the condition is not satisfied. Following example shows us the do-while loop.

![](images/00062.jpeg)

## For loop

The ‘for’ loop is the most widely used statement for looping in C++. This is a perfect option to use if you know how many times to iterate. This is easy to use because it allows the user to change the variables after every iteration. This is really simple to use as you declare everything in a single go at the same place.

Here is a simple example for a ‘for’ loop.

Example 1:

![](images/00063.jpeg)

The output of the above code is:

![](images/00064.jpeg)

Example 2:

![](images/00065.gif)

Output:

![](images/00066.jpeg)

## Break and continue

We have already seen about the break statement in our previous examples. Here we will use break statement with the continue statement. We know that the break statement can be used to terminate this which statement and looping statements like while loop and do while loop. But when you use it with switch statement at the end of the function, it signifies that the case is completed or finished. Here is an example showing the combination of switch and a break.

Example:

![](images/00067.jpeg)

When we use the break statement with a loop, we can terminate the loop early. The following example shows you how.

![](images/00068.jpeg)

In the above program, the user can type up to 40 characters. The loop can be terminated if the user presses the enter key. By pressing the enter key, the user can choose an early termination of the loop.

Continue statement

There will be situations where you will need to jump back to the beginning of the loop even earlier than the normal time. This can be useful for bypassing the rest of the loop for that iteration. The following example shows is the usage of the continue statement.

![](images/00069.jpeg)

Here in the above program, we have used the continue statement with the for loop and it will print all the numbers between 0 and 19 that are not divisible by 4\.

## Using continue and break

Usually it is not advised to pair up continue with break. This is so because it will cause deviations in the flow of execution of the program code. But if used carefully, the continue and break combination can be proved efficient. Here is a small example showing it.

![](images/00070.jpeg)

## Random number generation

Some programs will need to generate random numbers. A computer cannot generate a random number on its own unless you give it a certain code to execute. These random numbers are particularly used in programs related to statistics and games. Games like online poker or dice rolling games use a random number generation algorithm for generating random numbers.

What fun would it be if a game keeps on generating the same numbers for every player? And for machines like computers which know only values that are either true or false, cannot generate these random numbers on their own. For such cases, we use the pseudo random number generator algorithms. Here, the computer will take a random number which is actually a non-random number called the seed, and performs mathematical operations to transform the given seed into a different number which seems to be random.

Efficient random number generators will continue to execute the process over and over and will generate a number that is completely unrelated to the seed. These random numbers are also used in ATM machines for security purposes.

Generating a pseudo random number is not that hard. Here you’ll understand it with the following example. This program generates 100 pseudo random numbers.

![](images/00071.jpeg)

Output

![](images/00072.jpeg)

You can see that from the above output, all the numbers are random and there is no relation between them. If there was any, that would be random too.

You can actually generate random numbers in C++ by using the built in pseudo a random number generator. Here, you will make use of two functions. They are srand() and rand().

srand() will set the initial value or in other words, the seed value. While the rand() takes the srand() value and will start generating random numbers basing on the srand() value. You can understand it better with the following example.

![](images/00073.jpeg)

This will generate 100 random numbers

![](images/00074.jpeg)

Hear from the about generated random numbers, you can see that no number is less than the srand() value given. That is because that value is taken as the base and the other numbers are generated from it.

# Chapter 8: Storage classes

Within a given C++ program, the scope and the lifetime of the functions of variables defined by the storage class. The specifiers placed in front of the type which they modify. In C++, the following storage classes can be used.

*   auto
*   static
*   register
*   mutable
*   extern

## The auto Storage Class

For all of the local variables, the default of storage class is the auto storage class.

Example:

{
  int mount;
  auto int month;
}

In the examples given above there are two variables defined in a storage class which is the same for both. The auto can only be used with local variables.

## The register Storage Class

If you wish to define the local variables and store them in the RAM instead of the register, you can use of the register storage class. This implies that the size of the variable will be equal to the maximum size of the register. This cannot have the & operator to it as there is no memory location for it.

Syntax:

{
  register int  miles;
}

You should only use these registers for the variables which require a quick access, like counters. You should keep in mind that when you define a register, it doesn't imply that the variable is stored in that register. The variable might get stored in that register basing on the implementation and hardware restrictions.

## The Static Storage Class

Instead of creating and destroying local variable whenever it goes in and out of the scope, the static storage class will tell the compiler to store the local variable during its lifetime. So, if you want your local variables to keep their values during function calls, you should make those are local variables static.

The static modifier is not just limited to local variables, it can be applied to global variables as well. After this, the scope of that variable will be restricted to the file in which that variable is declared.

When you use a static on a data member of a class, only one copy of it will be shared by all the objects of that class. Here is an example.

Example:

#include <iostream>

// Function declaration
void func(void);

static int count = 10; /* Global variable */

main()
{
   while(count--)
   {
      func();
   }
   return 0;
}
// Function definition
void func( void )
{
   static int i = 5; // local static variable
   i++;
   std::cout << "i is " << i ;
   std::cout << " and count is " << count << std::endl;
}

When you compile and execute the above code, it will produce the following output.

i is 6 and count is 9
i is 7 and count is 8
i is 8 and count is 7
i is 9 and count is 6
i is 10 and count is 5
i is 11 and count is 4
i is 12 and count is 3
i is 13 and count is 2
i is 14 and count is 1
i is 15 and count is 0

## The extern Storage Class

There are some global variables which are visible to all of the program files. The extern storage class can be used for giving the reference of these global variables which are visible to the program files. You cannot initialise the variable using the 'extern' because it will only point debatable name to a predefined storage location.

In cases where you have more than one files and you define a function or a global variable which other files can use, the extern where do you stay in a different file for giving the reference of The function or variable. In simple words, we use the extern for declaring a function or a global variables that is present in another file.

In cases where multiple files share the same functions or global variables, the extern modifier is used. Here is an example program.

Example:

First File: main.cpp

#include <iostream>

int count ;
extern void write_extern();

main()
{
  count = 5;
  write_extern();
}

Second File: support.cpp

#include <iostream>

extern int count;

void write_extern(void)
{
  std::cout << "Count is " << count << std::endl;
}

Here, in this program the count is declared in another file using the extern keyword. Now if you combine both of these files as given below.

$g++ main.cpp support.cpp -o write

A right executable program will be produced. Now try to execute it and check the result as given below.

$./write
5

# 
Chapter 9: Arrays

An array is nothing more than a list of variables, all grouped together because they share common uses. It’s more a way of keeping everything neat and tidy, as you can see from the following code:

## int a[5]

It looks like a standard variable but note the use of square brackets. These brackets contain the size of the array that you want in your declaration, or the number of variables, in this case, 5 integer variables. Arrays can be whatever size you want them to be, provided your computer has the RAM to take it but they can only have one type of variable in them at any one time. 

When you want to access a certain variable, you simply put the number inside the square brackets. Just keep in mind that, when C++ labels variables, or anything, it starts at 0 and not 1. This does make a kind of sense, when you consider how a computer understands numbers. If your array had 8 items in it and you started it with the number 1, your computer can only read the first 7 places (Binary – 1-7). You could let it use the 0 as well but then 0 would be the first variable. The following code shows how you would handle accessing the variable that is before the first one in your list:

![](images/00075.jpeg)

One thing you should keep in mind is that you should not try to access a variable that is non-existent, for example, the 9th variable in an array that has 6 places or that hast actually had a variable assigned. In this case you would get what is known as a “garbage” Value since what the computer returns will be just that – garbage.

In the first case, you would get a segmentation fault, called as such because the computer is trying to get into a segment of memory that it isn’t allowed to get into. This may result in the program terminating unexpectedly, couple with an error report. To avoid any of this happening, get into the practice of initializing every place in the array before you begin. As with a normal variable, it would look something like this:

*   int a[5] = { 0, 0, 0, 0, 0 };

Important – note the curly brackets. Each item that is inside these brackets, marked off with a comma between them, is assigned to a specific variable in the array. The first one is set to the value that is first inside the brackets, the second to the second, and so on. If the array is not filled, every unassigned variable will come back as 0:

*   int a[5] = { 1 };

You have declared that there will be 5 variables but only specified 1 so the others will be shown as 0.

One of the most common uses for an array is to show a list, maybe ages in a group, or, as I will show you in a while, using them to co-ordinate spaces in big tables and maps.

The array above is known as a one-dimensional array. This is useful for lists but what about maps? In this case, you would need a two-dimensional array and the easiest way to do that is simply to add a second set of square brackets:

*   int array[4][5];

So, the first dimension shows 4 integers and the second is 5 integers. Thinking in terms of arrays as a physical map, we could say that this one is 4 X 5 or it could be 5 X 4\. Accessing the array is the same as accessing the one-dimensional array except for the number of square brackets we are using:

*   cout << array[0][1];

In the same way that you do a one-dimensional array, you can mass define a t dimensional array – all you do is add in a second set of curly brackets:

*   int array[2][2] = { {0, 0}, {1, 1} };

That isn’t as complicated as it looks – All it is doing is setting row 1 as 0, 0 and row 2 as 1, 1\. So long as you remember to pair the brackets, it will all come together. If you wanted to iterate through the 2-dimensional array, you would simply put two for  loops inside of each other:

![](images/00076.gif)

You will probably have spotted that I didn’t follow the convention I just talked about and there is a technical reason for this. Because of the way C++ handles arrays that are 2-dimensional, it is far more efficient to increment the right array index in the inner loop – put simply, the loops are saying that for each row, go through each column and move on to the next row. 

I have increased y in the outer loop and x in the inner loop and, because of this, x should be in the right array index making point (0, 1) into point [1][0]. Although this is somewhat counterintuitive, it is important that you remember it.

C++ has a very neat ability to let you not specify a particular array size, instead letting you insert square brackets with nothing between them. At the time of compiling, the size of the array should be known so the compiler will simply count the initialized elements and set the array size according to that. This is quite useful if you have a large array and you really don’t want to count all of them:

1.  // This array will be 5 elements long
2.  int array[] = { 0, 1, 2, 3, 4 };

Although this means that your array can have an unknown size at the time of compiling, this kind of array cannot be created at runtime. That would be known as a dynamic array and is somewhat more advanced than this.

Remember that C++ is a very powerful language and is able to support n-dimensional arrays – this means that you can add as many dimensions as you need to. It is highly unlikely that you will ever go above 3-dimensional, simply because the human brain is not able to see any more than that accurately.

# 
Chapter 10: Classes ,objects and interfaces 

## Classes and Objects

The main purpose of designing C++ is to add the concepts of object-oriented programming in C language. In object oriented programming, classes make the central feature. These classes are called as the user-defined types.

A class can be considered as a neat package that combines the data presentation and manipulating methods for that data. The form of an object is specified by a class. The functions and the data inside a class form the members of the class.

## Encapsulation

Every program in C++ will have the following two fundamental elements.

*   Program statements (code): Program statements are the part of the program which is used to perform specific actions. These are called as functions.
*   Program data: Data can be considered as the information of the given program which is affected by the functions in that program.

Encapsulation is a concept in object oriented programming which binds the functions and the data that manipulate the data. Encapsulation protects the data from the interference and misuse by outer elements. The data encapsulation gave rise to an important object oriented programming concept called data hiding.

Data encapsulation can be defined as a mechanism that bundles the data and the functions that use the data. Data abstraction can be defined as a mechanism that exposes the interfaces and hides the implementation details.

By creating user defined types called classes, encapsulation and data hiding can be performed. As we already know, a class can contain private, public or protected members. The items that are defined in a class without access specifiers will by default to be private. Here is an example.

Example:

class Box
{
  public:
     double getVolume(void)
     {
        return length * breadth * height;
     }
  private:
     double length;      // Length of a box
     double breadth;     // Breadth of a box
     double height;      // Height of a box
};

Here, the variables length, breadth, and height are private. This means that only the members of the class Box are allowed to access them. Please variables cannot be accessed by any other part of the program. This is one of the methods in which encapsulation can be performed.

If you wish that some parts of your class be public, you should define them using the public keyword. All the functions and variables that are defined after the public specifiers will be defined as public and any function in the program can access them.

By making a particular class a friend of another class will expose the implementation details and results in the reduction of encapsulation. It is always wise to keep the details of the class hidden from other classes. As many classes as possible should be hidden.

Any C++ program where class is implemented with private and public members can be considered as an example for data abstraction and data encapsulation. Consider this example below.

Here is an example on data encapsulation.

Example:

#include <iostream>
using namespace std;

class Adder{
  public:
     // constructor
     Adder(int i = 0)
     {
       total = i;
     }
     // interface to outside world
     void addNum(int number)
     {
         total += number;
     }
     // interface to outside world
     int getTotal()
     {
         return total;
     };
  private:
     // hidden data from outside world
     int total;
};
int main( )
{
  Adder a;

  a.addNum(10);
  a.addNum(20);
  a.addNum(30);

  cout << "Total " << a.getTotal() <<endl;
  return 0;
}

When you compile and execute the above code, it will produce the following output.

Total 60

The above class will add the numbers and will return their sum. Here the members addNum and getTotal are public and they are the interfaces which the user should know for use the class. Though the private members in the class are hidden, they are needed for the proper operation of the class.

Designing Strategy

It is always wise to hide the contents of a class by making it private unless we wish to expose them. This is good encapsulation.

Mostly the data members kept hidden but this equally applies to other members also which include virtual functions too.

## C++ Class Definitions

Whenever you are defining a class, you are basically defining a blueprint for a given data type. Though this won't define any data, defines what the name of the class means, which is, the objects that the class consists of and the operations that can be implemented on those objects.

The definition of a class begins with the keyword class, which is then followed by the name of the class and the body of the class enclosed inside curly braces. A list of declarations or a semicolon should be placed after the name of the class. Consider the following example in which the Box is defined by using the class keyword.

Example:

class Box
{
  public:
     double length;   // Length of a box
     double breadth;  // Breadth of a box
     double height;   // Height of a box
};

The public keyword will determine the access attributes of the class members following it. The public members of the class can be accessed by anyone outside the class within the scope of that particular class object. The class members can also be specified as private or protected and we will discuss it in later sections.

## Define C++ Objects

Every class provides a blueprint for its objects, which implies that objects can be created from a class. The declaration of objects in a class is the same kind of declaration with which variables of the basic type are declare. For example, for declaring two objects of the Box class, we use the following statements.

Box Box1;          // Declare Box1 of type Box
Box Box2;          // Declare Box2 of type Box

The objects Box1 and a Box2 will have their own set of data members.

## Accessing the Data Members

With the help of the direct member access operator (.), you can access the data members of an object of a class that are public. Here is an example that will help you to get a better understanding on this.

Example:

#include <iostream>

using namespace std;

class Box
{
  public:
     double length;   // Length of a box
     double breadth;  // Breadth of a box
     double height;   // Height of a box
};

int main( )
{
  Box Box1;        // Declare Box1 of type Box
  Box Box2;        // Declare Box2 of type Box
  double volume = 0.0;     // Store the volume of a box here

  // box 1 specification
  Box1.height = 5.0;
  Box1.length = 6.0;
  Box1.breadth = 7.0;

  // box 2 specification
  Box2.height = 10.0;
  Box2.length = 12.0;
  Box2.breadth = 13.0;
  // volume of box 1
  volume = Box1.height * Box1.length * Box1.breadth;
  cout << "Volume of Box1 : " << volume <<endl;

  // volume of box 2
  volume = Box2.height * Box2.length * Box2.breadth;
  cout << "Volume of Box2 : " << volume <<endl;
  return 0;
}

When you compile and execute the above code, it will produce the following output.

Volume of Box1 : 210
Volume of Box2 : 1560

You should always keep in mind that the protected and private members of the class cannot be directly accessed with the director member access operator (.). Now, we will see how the protected and private members are accessed.

## Classes & Objects in Detail

Till now, we have dealt with the basic concepts of the classes and objects in C++. We will discuss some more concerts in the subsections given below.

| Concept | Description |
| [Class member functions](http://www.tutorialspoint.com/cplusplus/cpp_class_member_functions.htm) | A A section of the class can be defined as a function which has its prototype or its definition inside the class the definition which is similar to any other variable. |
| [Class access modifiers](http://www.tutorialspoint.com/cplusplus/cpp_class_access_modifiers.htm) | The members of the class can be declared as public, protected or private. The default access definition for the members is always private. |
| [Constructor & destructor](http://www.tutorialspoint.com/cplusplus/cpp_constructor_destructor.htm) | A class constructor can be defined as a special function within a class which is called whenever there is a new object is created in that class. A destructor is similar to a constructor but it is called whenever you delete created object. |
| [C++ copy constructor](http://www.tutorialspoint.com/cplusplus/cpp_copy_constructor.htm) | A copy constructor is a type of constructor which is used for creating objects by using an object of that class which is already created. |
| [C++ friend functions](http://www.tutorialspoint.com/cplusplus/cpp_friend_functions.htm) | A friend to function is something which can access the private and the protected members of a given class. |
| [C++ inline functions](http://www.tutorialspoint.com/cplusplus/cpp_inline_functions.htm) | In an in-line function the compiler will expand record within the function's body in the place of a call to that function. |
| [The this pointer in C++](http://www.tutorialspoint.com/cplusplus/cpp_this_pointer.htm) | In C++, every object will have a special pointer which points itself. |
| [Pointer to C++ classes](http://www.tutorialspoint.com/cplusplus/cpp_pointer_to_class.htm) | A pointer to a class is similar to a pointer to a structure. In fact, a class can be considered as a structure which has functions in it. |
| [Static members of a class](http://www.tutorialspoint.com/cplusplus/cpp_static_members.htm) | The function members and the data members of any class can be declared static. |

## Interfaces

The capabilities or behavior of a class in C++ without committing  to an implementation of its class can be described by an interface.

The interfaces in C++ are implemented with the abstract classes. Do not confuse Data abstraction with the abstract classes. The data abstraction is it different concept where the implementation details separated from the associated data.

By declaring any one function of a class as a pure virtual function, that class can be made abstract. You can specify a pure virtual function by adding "= 0" in its declaration. It is given in the example below.

class Box
{
  public:
     // pure virtual function
     virtual double getVolume() = 0;
  private:
     double length;      // Length of a box
     double breadth;     // Breadth of a box
     double height;      // Height of a box
};

The main purpose of any abstract class is to provide a proper base class so that other classes can inherit this base class. Objects cannot be instantiated using abstract classes. Abstract classes can only serve as interfaces. A compilation error will be raised when an object of an abstract class is tried to instantiated.

If you wish to instantiate a subclass of an abstract class, each of its virtual functions should be implemented. This implies that it will support the interface declared by the abstract class. When the pure virtual function override fails in a derived class and then trying to instantiate the objects that class will give a compilation error.

In C++, the classes used for instantiating objects are defined as concrete classes.

Abstract Class Example

In the following example, The parent class gives an interface for the base class to implement the function getArea().

Example:

#include <iostream>

using namespace std;

// Base class
class Shape
{
public:
  // pure virtual function providing interface framework.
  virtual int getArea() = 0;
  void setWidth(int w)
  {
     width = w;
  }
  void setHeight(int h)
  {
     height = h;
  }
protected:
  int width;
  int height;
};

// Derived classes
class Rectangle: public Shape
{
public:
  int getArea()
  {
     return (width * height);
  }
};
class Triangle: public Shape
{
public:
  int getArea()
  {
     return (width * height)/2;
  }
};

int main(void)
{
  Rectangle Rect;
  Triangle  Tri;

  Rect.setWidth(5);
  Rect.setHeight(7);
  // Print the area of the object.
  cout << "Total Rectangle area: " << Rect.getArea() << endl;

  Tri.setWidth(5);
  Tri.setHeight(7);
  // Print the area of the object.
  cout << "Total Triangle area: " << Tri.getArea() << endl;

  return 0;
}

When you compile and execute the above code, it will produce the following output.

Total Rectangle area: 35
Total Triangle area: 17

In the above example, an interface is defined by an abstract class in terms of getArea(). The same function was implemented by two other classes but with different for calculating the area that is specific to the given shape.

Designing Strategy

An abstract base class can be used by an object oriented system for providing a standardized and a common interface that is appropriate for all of the external applications. Then, the classes can be inherited from the abstract base class and these classes will all operate similarly.

All the capabilities (public functions) better offered by the external applications will be provided as pure virtual functions from the given abstract base class. The derive the classes will provide the implementations of these pure virtual functions. Each of these are derived classes correspond to a specific type of application.

With this architecture you are allowed to add new applications to a system even after  it being defined.

# 
Chapter 11: Templates

## Templates

Templates can be considered as the foundation of generic programming. Generic programming involves coding in a where that is independent from any particular type.

You can think of a template as a formula or a blueprint with which generic classes or functions can be created. A few examples of the genetic programming are the library containers which are developed using the concept of template.

Every container such as vector has a single definitions. But different kinds of ver cord can be defined. For example vector <string> or vector <int>.

Using templates, apart from classes functions can be defined as well. Now we will see how it works.

## Function Template

The general syntax of a template function definition is given below.

template <class type> ret-type func-name(parameter list)
{
  // body of function
}

Here, the typeface of placeholder name for a data type that is used by the function. Within the definition of the function, this name can be used. Here is an example.

Example:

The function template in the following examples will return a maximum of two values.

#include <iostream>
#include <string>

using namespace std;

template <typename T>
inline T const& Max (T const& a, T const& b)
{
   return a < b ? b:a;
}
int main ()
{

   int i = 39;
   int j = 20;
   cout << "Max(i, j): " << Max(i, j) << endl;

   double f1 = 13.5;
   double f2 = 20.7;
   cout << "Max(f1, f2): " << Max(f1, f2) << endl;

   string s1 = "Hello";
   string s2 = "World";
   cout << "Max(s1, s2): " << Max(s1, s2) << endl;

  return 0;
}

If you compile and execute the given code, it will produce the following output.

Max(i, j): 39
Max(f1, f2): 20.7
Max(s1, s2): World

## Class Template

In C++, apart from defining function template you can define class templates as well. The generic class declaration syntax is given below.

Syntax:

template <class type> class class-name {
.
.
.
}

From the syntax given above, type is the placeholder type name. This type a name will be specified during the instantiation of a class. Multiple generic data types can be defined by separating them with a (, ).

In the following example, a class Stack<> is defined. Generic method to push and pop the stack elements will be implemented.

Example:

#include <iostream>
#include <vector>
#include <cstdlib>
#include <string>
#include <stdexcept>

using namespace std;

template <class T>
class Stack {
 private:
   vector<T> elems;     // elements

 public:
   void push(T const&);  // push element
   void pop();               // pop element
   T top() const;            // return top element
   bool empty() const{       // return true if empty.
       return elems.empty();
   }
};

template <class T>
void Stack<T>::push (T const& elem)
{
   // append copy of passed element
   elems.push_back(elem);    
}

template <class T>
void Stack<T>::pop ()
{
   if (elems.empty()) {
       throw out_of_range("Stack<>::pop(): empty stack");
   }
              // remove last element
   elems.pop_back();         
}

template <class T>
T Stack<T>::top () const
{
   if (elems.empty()) {
       throw out_of_range("Stack<>::top(): empty stack");
   }
              // return copy of last element
   return elems.back();      
}

int main()
{
   try {
       Stack<int>         intStack;  // stack of ints
       Stack<string> stringStack;    // stack of strings

       // manipulate int stack
       intStack.push(7);
       cout << intStack.top() <<endl;

       // manipulate string stack
       stringStack.push("hello");
       cout << stringStack.top() << std::endl;
       stringStack.pop();
       stringStack.pop();
   }
   catch (exception const& ex) {
       cerr << "Exception: " << ex.what() <<endl;
       return -1;
   }
}

After compiling and running the above code, it will produce the following output.

7
hello
Exception: Stack<>::pop(): empty stack

# 
Chapter 12: Namespaces

In real-time programming, you will encounter situations where you will have two objects with the same name in a given class. For differentiating the members of the same class having the same name we will have to add some additional information to them along with their names. For example if there are two persons with the name Charles, you can differentiate them using their area in which they live in or any such information like that.

Now consider a situation where this happens in your applications. For example, if there is a given function with a particular name defined and there is another function with the same name in a different directory. In such cases, the compiler cannot differentiate between the two functions and eight may not call the function which you are referring inside your code.

For overcoming this difficulty, will username spaces which are specifically designed to be used as the additional information that can be added to functions, variables, and classes etc. which share the same name in different libraries. By using namespaces, The context in which the names are defined can be defined. A namespace is used for defining a scope.

## Defining a Namespace

You can define a namespace by using the keyword namespace which will be followed by the name of the namespace. The syntax for a defining a namespace is given below.

Syntax:

namespace namespace_name {
  // code declarations
}

For calling the name space version of a function or a variable, the namespace name should be added in front of that function as given below.

name::code;  // code could be variable or function.

Now we will have a look at how namespace scope the entities which include functions and variables.

Example:

#include <iostream>
using namespace std;

// first name space
namespace first_space{
  void func(){
     cout << "Inside first_space" << endl;
  }
}
// second name space
namespace second_space{
  void func(){
     cout << "Inside second_space" << endl;
  }
}
int main ()
{

  // Calls function from first name space.
  first_space::func();

  // Calls function from second name space.
  second_space::func();

  return 0;
}

When you compile and run this code, it will produce the following output.

Inside first_space
Inside second_space

## The using directive

With the using namespace directive, prepending of namespaces can be avoided. This directive will instruct the compiler that the following code is using the names in that specified namespace.

You can also avoid prepending of namespaces with the using namespace directive. This directive tells the compiler that the subsequent code is making use of names in the specified namespace. The namespace is used in the following example.

Example:

#include <iostream>
using namespace std;

// first name space
namespace first_space{
  void func(){
     cout << "Inside first_space" << endl;
  }
}
// second name space
namespace second_space{
  void func(){
     cout << "Inside second_space" << endl;
  }
}
using namespace first_space;
int main ()
{

  // This calls function from first name space.
  func();

  return 0;
}

When the above code is compiled and run, it will produce the following output.

## Inside first_space

A particular item in a namespace can be referred by the  using directive. For example if you only intend to use the cout as the std namespace, it can be referred as given below.

using std::cout;

Without prepending the given namespace, cout can be referred by the subsequent code. This only implies to the cout and the other items present in the std namespace will be explicit. It is given in the small example below.

Example:

#include <iostream>
using std::cout;

int main ()
{

  cout << "std::endl is used with std!" << std::endl;

  return 0;
}

If the above code is compiled and run, it will produce the following output.

std::endl is used with std!

All the names that are introduced in the using directive will always obey the normal scope rules.

All the entities which have the same name defined in the scope that are outside will be hidden. And from the point of using directive, the name is visible to the end of the given scope. This is the score in which the directive is present.

## Discontiguous Namespaces

You can define a namespace in several parts. This implies that I name space is made up of several parts that are defined separately. It is not necessary for all the separate files to be in a single place. These parts can be spread over many files.

So if there is a part of the new space which requires a defined name in some other file, that a particular name should be declared. In the following example, either a new namespace will be defined or new elements will be added to an existing namespace with the following namespace definition.

Example:

namespace namespace_name {
  // code declarations
}

## Nested Namespaces

In C++, nesting of namespaces is allowed where one namespace can be defined inside another namespace. The syntax for nested namespaces is given below.

Syntax:

namespace namespace_name1 {
  // code declarations
  namespace namespace_name2 {
     // code declarations
  }
}

By using the resolution operator, the members of the nested namespace can be accessed. The syntax for using the resolution operator is given below.

Syntax:

// to access members of namespace_name2
using namespace namespace_name1::namespace_name2;

// to access members of namespace:name1
using namespace namespace_name1;

If you use of the namespace_name1 from the above statements, the elements of the namespace_name2 will be made available for the scope as follows.

Example:

#include <iostream>
using namespace std;

// first name space
namespace first_space{
  void func(){
     cout << "Inside first_space" << endl;
  }
  // second name space
  namespace second_space{
     void func(){
        cout << "Inside second_space" << endl;
     }
  }
}
using namespace first_space::second_space;
int main ()
{

  // This calls function from second name space.
  func();

  return 0;
}

If the above code is compiled and run, it will produce the following output.

Inside second_space

# 
Chapter 13: Inheritance

In object oriented programming, inheritance is considered as an important concept. With inheritance, class can be defined in terms of another class. With inheritance creation and maintenance of applications is easy. Inheritance provides faster implementation time and it also reduces the code reusability.

When creating a class, the programmer can inherit the class members of an already exist in class avoiding the city of creating new member functions and new data members. The class from which the class members are inherited is referred as the base class and the new class is called as they derived class.

With inheritance, the is-a relationship is implemented. For examples, reptile is-a animal, snake is-a reptile and hence snake is-a animal.

## Base & Derived Classes

When creating a class, the class is not limited to be derived from a single class. In C++, a class can be derived from multiple base classes from which it inherits the data and functions of all those classes. The class interrogation list can be used for specifying a derived class. The class derivation list can contain the names of one or more base classes. The syntax is given below.

Syntax:

class derived-class: access-specifiers base-class

Here, the access specifiers can either be of the public, private or a protected. The base class is an already defined class. If there is no access specifiers used, it will be considered as private by default.

In the example given below, let us consider a base class named Shape and a class Rectangle derived from the base class.

Example:

#include <iostream>

using namespace std;

// Base class
class Shape
{
  public:
     void setWidth(int w)
     {
        width = w;
     }
     void setHeight(int h)
     {
        height = h;
     }
  protected:
     int width;
     int height;
};

// Derived class
class Rectangle: public Shape
{
  public:
     int getArea()
     {
        return (width * height);
     }
};

int main(void)
{
  Rectangle Rect;

  Rect.setWidth(5);
  Rect.setHeight(7);

  // Print the area of the object.
  cout << "Total area: " << Rect.getArea() << endl;

  return 0;
}

When you compile and execute the above code, it will produce the following output.

Total area: 35

## Access Control and Inheritance

When a class is derived from a base class, the non-private members of the base class from which it is derived from can be accessed. If the class members of the base class declared private, they derive the class cannot access them. So in cases where you don't want your derived class to access the class members or functions of the base class, you can declare them private.

The different access types are summarized in the table below based on who can access them.

| Access | public | protected | private |
| Same class | yes | yes | yes |
| Derived classes | yes | yes | no |
| Outside classes | yes | no | no |

Though a derived class inherits all the class methods of its base class, there are some exceptions.

*   The constructors, copy constructors and destructors cannot be inherited by the derived class.
*   The overloaded operators of a given base class cannot be inherited by the derived class.
*   The derived class cannot inherit the friend functions of its base class.

## Types of Inheritance

When a base class is used for deriving a class, the base class maybe inherited either through the public inheritance, protected inheritance or private inheritance. The access specifiers are used for specifying the type of inheritance. If the access specifiers are not used, the inheritance will by default to be a private inheritance.

The private or protected inheritances are hardly used when programming. On the other hand, public inheritance is the most commonly used type of inheritance. The following rules will be applied when using different type of inheritance.

*   Public Inheritance: When a class is inherited from a base class, the public members of the base class will be public members in the derived class as well. This is the same for the protected members of the base class. But in the case of the private members of the base class, they cannot be inherited as they can never be accessed by a derived class directly. The private members can be accessed through calls to the protected and public members of the given base class.
*   Protected Inheritance: When a class is derived from a base class with protected members, all the public and protected members of the class will become they derive the class' protected members.
*   Private Inheritance: when a class is derived from a base class with private members, they derive the class will have all its class members as private.

## Multiple Inheritances

In C++, the class is allowed to inherit members from multiple base classes. The syntax for multiple inheritances is given below.

Syntax:

class derived-class: access baseA, access baseB....

Here, the access can be anyone of public, private or protected and it can be declared for each of the base class separated by a comma. Here is an example.

Example:

#include <iostream>

using namespace std;

// Base class Shape
class Shape
{
  public:
     void setWidth(int w)
     {
        width = w;
     }
     void setHeight(int h)
     {
        height = h;
     }
  protected:
     int width;
     int height;
};

// Base class PaintCost
class PaintCost
{
  public:
     int getCost(int area)
     {
        return area * 70;
     }
};

// Derived class
class Rectangle: public Shape, public PaintCost
{
  public:
     int getArea()
     {
        return (width * height);
     }
};

int main(void)
{
  Rectangle Rect;
  int area;

  Rect.setWidth(5);
  Rect.setHeight(7);

  area = Rect.getArea();

  // Print the area of the object.
  cout << "Total area: " << Rect.getArea() << endl;

  // Print the total cost of painting
  cout << "Total paint cost: $" << Rect.getCost(area) << endl;

  return 0;
}

When you compile and execute the above code, it will produce the following output.

Total area: 35
Total paint cost: $2450

# 
Chapter 14: Exception handling

## Exception

An exception an object oriented programming can be defined as an interruption in the normal flow of execution of a program. It is the same in the C++. An exception in C++ can be defined as a response for an exceptional circumstance that occurred during the running of a program. Division by zero is an example for an exception.

When an exception is raised, the control will transfer from a part of a program to another part of the program. Exception handling in C++ is based upon the keywords try, catch and throws. We will discuss about them in detail.

*   throw: Whenever a problem arises, the program will throw an exception. This can be done by using the throw keyword.
*   catch: The exception thrown will be caught by the exception and let that is placed where you want the problem to be handed in your program. The catching of an exception is indicated by the catch keyword.
*   try: The purpose of the trial block is to identify the block of code where particular exceptions are activated. One or more catch blocks will follow the try block.

A method will catch an exception with the help of the try and catch combination of keywords by ensuring block which might raise an exception. The block of code which might possibly raise an exception will be placed inside the try/catch block. Any quarter that is placed inside the try/catch block will be considered as protected code. The syntax for the try/catch block is given below.

Syntax:

try
{
  // protected code
}catch( ExceptionName e1 )
{
  // catch block
}catch( ExceptionName e2 )
{
  // catch block
}catch( ExceptionName eN )
{
  // catch block
}

In cases where multiple exceptions are expected, multiple catch statements can be added for catching different types of exceptions raised in different situations.

## Throwing Exceptions

By using the throw statements, exceptions can be thrown anywhere inside the given block of code. The type of the exception will be determined by the operand of that true statement. This can be any expression and the result of that expression will determine the expression thrown.

Here is an example where an exception is thrown when they give an integer is divided by zero.

Example:

double division(int a, int b)
{
  if( b == 0 )
  {
     throw "Division by zero condition!";
  }
  return (a/b);
}

## Catching Exceptions

Any exceptions raised will be caught by the catch block that follows the try block. The type of exception that you want to catch can be specified by determining the exception declaration inside the parentheses that follow the catch keyword.

Here is an example.

try
{
  // protected code
}catch( ExceptionName e )
{
 // code to handle ExceptionName exception
}

An exception of the type ExceptionName will be caught in the above code. You can specify the type of exception that you wish to handle with the catch block by putting an ellipsis, (…) inside the parenthesis that enclose the exception declaration. It is shown in the sample code given below.

try
{
  // protected code
}catch(...)
{
 // code to handle any exception
}

The below example will throw an exception raised due to division by zero. This raised exception will be caught in the catch block.

#include <iostream>
using namespace std;

double division(int a, int b)
{
  if( b == 0 )
  {
     throw "Division by zero condition!";
  }
  return (a/b);
}

int main ()
{
  int x = 50;
  int y = 0;
  double z = 0;

  try {
    z = division(x, y);
    cout << z << endl;
  }catch (const char* msg) {
    cerr << msg << endl;
  }

  return 0;
}

Here, the exception raised is of the type const char* and for catching this exception should use the const char* inside the catch block. If the above code is compiled and run, it will produce the following output.

Division by zero condition!

## Flow of Control in the try/catch blocks

Here is a simple example program in which exception handling of C++ is shown. This will help you to get a better understanding the try/catch block flow of execution.

Example:

#include <iostream>

using namespace std;

int main()

{

  int x = -1;

  // Some code

  cout << "Before try block \n";

  try {

     cout << "Inside try block \n";

     if (x < 0)

     {

        throw x;

        cout << "After throw (Never executed) \n";

     }

  }

  catch (int x ) {

     cout << "Exception is caught here \n";

  }

  cout << "After catch block (Will be executed) \n";

  return 0;

}

When the above code is executed, it will produce the following output.

Before try block

Inside try block

Exception caught here

After catch block (Will be executed)

## C++ Standard Exceptions

In C++, the list of all the standard exceptions are defined in the <exception> and it can be used in programs. These exceptions are listed in a parent-child hierarchy as given below.

The descriptions for the above exceptions are given in the table below.

| Exception | Description |
| std::exception | This exception is the parent class for all of the exceptions in C++. |
| std::bad_alloc | This exception will be thrown by new operator which has failed to allocate to the requested space. |
| std::bad_cast | This exception will be raised whenever the dynamic_cast for a given reference type of fails. |
| std::bad_exception | This exception will be raised when there is an unexpected exception. |
| std::bad_typeid | This exception can be thrown by a typeid. |
| std::logic_error | This is shown when there is an exception which can be detected theoretically by reading the code. |
| std::domain_error | This exception will be thrown in cases where mathematically invalid domains are used. |
| std::invalid_argument | This exception well with thrown when invalid arguments are used. |
| std::length_error | This exception will be thrown in cases where a std::string that is too big is created. |
| std::out_of_range | This can be thrown by the at method from for example a std::vector and std::bitset<>::operator[](). |
| std::runtime_error | This is shown when there is an exception which cannot be detected theoretically by reading the code. |
| std::overflow_error | This exception will be thrown in cases where the mathematical overflow occurs. |
| std::range_error | This exception will be raised in cases where the value tried to store is out of range. |
| std::underflow_error | This exception will be thrown in cases where the mathematical underflow occurs. |

## Define New Exceptions

In C++, you are allowed to define your own exceptions. This can be done by inheriting and overriding the functionalities of the exception class. In the example given below, you can see how the std::exception class can be used for implementing your own exceptions.

Example:

#include <iostream>
#include <exception>
using namespace std;

struct MyException : public exception
{
 const char * what () const throw ()
 {
   return "C++ Exception";
 }
};

int main()
{
 try
 {
   throw MyException();
 }
 catch(MyException& e)
 {
   std::cout << "MyException caught" << std::endl;
   std::cout << e.what() << std::endl;
 }
 catch(std::exception& e)
 {
   //Other errors
 }
}

This code will produce the following output.

MyException caught
C++ Exception

The what() is a public method that is provided by the exception class. The what() is overridden by every child exception class and because of an exception will be returned by this.

# 
Chapter 15: Preprocessor

In C++, the preprocessors directives instruct the compiler to pre-process the information before the start of actual compilation.

Every preprocessor directive will begin with the #, and on the line of the preprocess the directive, only whitespace characters may appear. As the preprocessor directives do not belong to C++, there is no need for adding a semicolon (;) at the end of the line.

As you have already seen, in all of the examples we have used the #include directive. This micro is used for including a header file into the source file.

In C++, there are a number of preprocessor directives. Some of them #include, #line, #define, #else, #if etc. Here, we will have a look at the important directives.

## The #define Preprocessor

The #define preprocessor directive is used for creating symbolic constants. My crew is another name for the symbolic constant and the syntax for using the directive is given below.

#define macro-name replacement-text

Whenever the above line is seen in a file, the replacement text will replace all the subsequent occurrences of macro in that particular file. This will be done before the compilation of the program. Here is an example.

Example:

#include <iostream>
using namespace std;

#define PI 3.14159

int main ()
{

   cout << "Value of PI :" << PI << endl;

   return 0;
}

Now, we will perform the preprocessing for this code. We will assume that the source code is there with us. We will compile the code with the -E option and the result will be redirected to test.p. If you open test.p, you can find a lot of information on the bottom and you will see that the value is replaced.

$gcc -E test.cpp > test.p

...
int main ()
{

   cout << "Value of PI :" << 3.14159 << endl;

   return 0;
}

## Function-Like Macros

You can define macros which take arguments by using the #define preprocessor as given below.

#include <iostream>
using namespace std;

#define MIN(a,b) (((a)<(b)) ? a : b)

int main ()
{
  int i, j;
  i = 100;
  j = 30;
  cout <<"The minimum is " << MIN(i, j) << endl;

   return 0;
}

When the above code is compiled and run, it will produce the following output.

The minimum is 30

## Conditional Compilation

You can actually compile selective parts of your code instead of compiling the whole program. In C++ there are several directives which will allow you to compile selected parts of your source code. This process of compiling a selected part in your source code is called the conditional compilation.

The construct of the conditional preprocessor is similar to the selection structure. Consider the following example.

#ifndef NULL
  #define NULL 0
#endif

Programs can be compiled for debugging purposes and the debugging can be turned on or turned off with a single macro. The syntax for it is given below.

#ifdef DEBUG
  cerr <<"Variable x = " << x << endl;
#endif

From the above code, the statement cerr will be compiled if the DEBUG symbolic constant is defined prior to the  #ifdef DEBUG directive. You can comment out a part of the program by using the #if 0 statement. It is shown below.

#if 0
  code prevented from compiling
#endif

Here is an example which will help you to get a better understanding.

Example:

#include <iostream>
using namespace std;
#define DEBUG

#define MIN(a,b) (((a)<(b)) ? a : b)

int main ()
{
  int i, j;
  i = 100;
  j = 30;
#ifdef DEBUG
  cerr <<"Trace: Inside main function" << endl;
#endif

#if 0
  /* This is commented part */
  cout << MKSTR(HELLO C++) << endl;
#endif

  cout <<"The minimum is " << MIN(i, j) << endl;

#ifdef DEBUG
  cerr <<"Trace: Coming out of main function" << endl;
#endif
   return 0;
}

When the above code is compiled and run, it will produce the following output.

Trace: Inside main function
The minimum is 30
Trace: Coming out of main function

## The # and ## Operators

The # and ## preprocessor operators in C++. You can convert a replacement text talking into a string surrounded by quotes by using the # operator.

Have a look at the macro definition given below.

#include <iostream>
using namespace std;

#define MKSTR( x ) #x

int main ()
{
   cout << MKSTR(HELLO C++) << endl;

   return 0;
}

If the above code is compiled and run, it will produce the following output.

HELLO C++

## Predefined C++ Macros

C++ provides its users with a wide range of predefined macros. These macros are described below.

C++ provides a number of predefined macros mentioned below:

| Macro | Description |
| __LINE__ | This macro contains the line number of the line which the compiler is currently on. |
| __FILE__ | This macro contains the name of the file which is being compiled. |
| __DATE__ | This macro contains the translation date of the source file to the object code in a string with the form month/date/year. |
| __TIME__ | This macro contains the time when the program was compiled. This time is stored in a string with the form hour:minute:second. |

Now, we will have a look at an example in which the above macros are used.

Example:

#include <iostream>
using namespace std;

int main ()
{
   cout << "Value of __LINE__ : " << __LINE__ << endl;
   cout << "Value of __FILE__ : " << __FILE__ << endl;
   cout << "Value of __DATE__ : " << __DATE__ << endl;
   cout << "Value of __TIME__ : " << __TIME__ << endl;

   return 0;
}

When the above code is compiled and run, it will produce the following output.

Value of __LINE__ : 6
Value of __FILE__ : test.cpp
Value of __DATE__ : Feb 28 2011
Value of __TIME__ : 18:52:48

# 
Chapter 16: Multi-Threading

Multithreading can be considered as a specialized form of multitasking and multitasking can be defined as the feature that allows your system to run multiple programs concurrently. There are two types of multitasking in general. They are 1.Process based and 2\. Thread based.

In process based multitasking, the execution of different programs will be done concurrently. The thread based multitasking will take care of the concurrent execution of the individual pieces of that very program.

In a multithreaded program, two or more parts will run concurrently. Each of those parts is called a thread and every thread defines a part of execution which is separate to others.

There are no built-in applications for multithreading in C++. For multithreading, it completely relies upon the OS.

## Creating Threads

For creating a POSIX thread, we will use the following routine.

#include <pthread.h>
pthread_create (thread, attr, start_routine, arg)

Here, pthread_create will create a new executable thread. There is no limitation for calling this routine and it can be called multiple times and anyway from your code. The description of the parameters is given below.

| Parameter | Description |
| thread | It is an open it and unique identifier for the new thread that is returned by subroutine. |
| attr | An opaque attribute object that may be used to set thread attributes. You can specify a thread attributes object, or NULL for the default values. |
| start_routine | This is a C++ thread parameter with which the new thread will execute after its creation. |
| arg | A single argument that may be passed to start_routine. It must be passed by reference as a pointer cast of type void. NULL may be used if no argument is to be passed. |

The maximum number of threads that a process can create depends on its implementation. A thread can create another thread and after their creation, threads act like peers. Implied hierarchy or a dependency cannot be found between threads.

The maximum number of threads that may be created by a process is implementation dependent. Once created, threads are peers, and may create other threads. There is no implied hierarchy or dependency between threads.

## Terminating Threads

You can use the following routine for terminating a POSIX thread.

#include <pthread.h>
pthread_exit (status)

For explicitly exiting a thread, the pthread_exit is used here. The pthread_exit() routine is difficulty called after a thread completing its work and when it is not required any longer.

If the main() function ends with pthread_exit(), before the the threads that it has created, the other threads will not terminate and will still continue to execute. They will be terminated automatically when the main() function ends otherwise. Here is an example.

Example:

In this example, five threads will be created by the pthread_create() routine. Each of those are five threads will print a message "Hello World!" and will terminate by calling the pthread_exit().

#include <iostream>
#include <cstdlib>
#include <pthread.h>

using namespace std;

#define NUM_THREADS     5

void *PrintHello(void *threadid)
{
  long tid;
  tid = (long)threadid;
  cout << "Hello World! Thread ID, " << tid << endl;
  pthread_exit(NULL);
}

int main ()
{
  pthread_t threads[NUM_THREADS];
  int rc;
  int i;
  for( i=0; i < NUM_THREADS; i++ ){
     cout << "main() : creating thread, " << i << endl;
     rc = pthread_create(&threads[i], NULL,
                         PrintHello, (void *)i);
     if (rc){
        cout << "Error:unable to create thread," << rc << endl;
        exit(-1);
     }
  }
  pthread_exit(NULL);
}

Using the -lpthread library, compile the program as given below.

$gcc test.cpp -lpthread

Now, if you execute the above program, it will generate the following output.

main() : creating thread, 0
main() : creating thread, 1
main() : creating thread, 2
main() : creating thread, 3
main() : creating thread, 4
Hello World! Thread ID, 0
Hello World! Thread ID, 1
Hello World! Thread ID, 2
Hello World! Thread ID, 3
Hello World! Thread ID, 4

## Passing Arguments to Threads

This example will show you how multiple arguments are passed via a structure. As the thread callback points to void, any data type can be passed in a thread. This will be explained in the example given below.

Example:

#include <iostream>
#include <cstdlib>
#include <pthread.h>

using namespace std;

#define NUM_THREADS     5

struct thread_data{
  int  thread_id;
  char *message;
};

void *PrintHello(void *threadarg)
{
  struct thread_data *my_data;

  my_data = (struct thread_data *) threadarg;

  cout << "Thread ID : " << my_data->thread_id ;
  cout << " Message : " << my_data->message << endl;

  pthread_exit(NULL);
}

int main ()
{
  pthread_t threads[NUM_THREADS];
  struct thread_data td[NUM_THREADS];
  int rc;
  int i;

  for( i=0; i < NUM_THREADS; i++ ){
     cout <<"main() : creating thread, " << i << endl;
     td[i].thread_id = i;
     td[i].message = "This is message";
     rc = pthread_create(&threads[i], NULL,
                         PrintHello, (void *)&td[i]);
     if (rc){
        cout << "Error:unable to create thread," << rc << endl;
        exit(-1);
     }
  }
  pthread_exit(NULL);
}

When you compile and execute the above code, it will produce the following output.

main() : creating thread, 0
main() : creating thread, 1
main() : creating thread, 2
main() : creating thread, 3
main() : creating thread, 4
Thread ID : 3 Message : This is message
Thread ID : 2 Message : This is message
Thread ID : 0 Message : This is message
Thread ID : 1 Message : This is message
Thread ID : 4 Message : This is message

## Joining and Detaching Threads

C++ provides its users with two routines with which they can join or detach threads. They are given below.

pthread_join (threadid, status)
pthread_detach (threadid)

The pthread_join() subroutine will block the calling thread until the thread with the specified threaded is terminated. When a new thread is created, an attribute of that thread will define if that thread is joinable or detached. You can only join the threads that are created as joinable threads and a detachable thread cannot be joined in any case.

In this example, it is shown how to wait for the thread completions with the Pthread join routine.

Example:

#include <iostream>
#include <cstdlib>
#include <pthread.h>
#include <unistd.h>

using namespace std;

#define NUM_THREADS     5

void *wait(void *t)
{
  int i;
  long tid;

  tid = (long)t;

  sleep(1);
  cout << "Sleeping in thread " << endl;
  cout << "Thread with id : " << tid << "  ...exiting " << endl;
  pthread_exit(NULL);
}

int main ()
{
  int rc;
  int i;
  pthread_t threads[NUM_THREADS];
  pthread_attr_t attr;
  void *status;

  // Initialize and set thread joinable
  pthread_attr_init(&attr);
  pthread_attr_setdetachstate(&attr, PTHREAD_CREATE_JOINABLE);

  for( i=0; i < NUM_THREADS; i++ ){
     cout << "main() : creating thread, " << i << endl;
     rc = pthread_create(&threads[i], NULL, wait, (void *)i );
     if (rc){
        cout << "Error:unable to create thread," << rc << endl;
        exit(-1);
     }
  }

  // free attribute and wait for the other threads
  pthread_attr_destroy(&attr);
  for( i=0; i < NUM_THREADS; i++ ){
     rc = pthread_join(threads[i], &status);
     if (rc){
        cout << "Error:unable to join," << rc << endl;
        exit(-1);
     }
     cout << "Main: completed thread id :" << i ;
     cout << "  exiting with status :" << status << endl;
  }

  cout << "Main: program exiting." << endl;
  pthread_exit(NULL);
}

When you compile and execute the above code, it will produce the following output.

main() : creating thread, 0
main() : creating thread, 1
main() : creating thread, 2
main() : creating thread, 3
main() : creating thread, 4
Sleeping in thread
Thread with id : 0 .... exiting
Sleeping in thread
Thread with id : 1 .... exiting
Sleeping in thread
Thread with id : 2 .... exiting
Sleeping in thread
Thread with id : 3 .... exiting
Sleeping in thread
Thread with id : 4 .... exiting
Main: completed thread id :0  exiting with status :0
Main: completed thread id :1  exiting with status :0
Main: completed thread id :2  exiting with status :0
Main: completed thread id :3  exiting with status :0
Main: completed thread id :4  exiting with status :0
Main: program exiting.

# Conclusion

That concludes my run through of C++ computer language. I hope that I have been able to give you some idea of how to get started with C++ computer programming. Once you get the hang of the basics and learn how to apply each rule, the world really is your oyster when it comes to programming.

It is important that you learn how each operator, variable, loop and conditional works independently and how to put them together to produce the code for the program you are aiming to write.  It is not too difficult a language to learn, but it will require your undivided attention to get it right otherwise, your compiler will be throwing up all sorts of errors and your programs just won’t run.

Enjoy your programming adventures and good luck!

You May Enjoy My Other Books!

[PYTHON: Programming Guide For Beginners: LEARN IN A DAY!](http://hyperurl.co/python)

hyperurl.co/python

[JAVA: Java Programming, JavaScript, Coding: Programming Guide: LEARN IN A DAY!](http://hyperurl.co/javaos)

hyperurl.co/javaos

[SQL: Programming Guide: Javascript and Coding: LEARN IN A DAY!](http://smarturl.it/sql)

hyperurl.co/sql

Programming: HTML: Programming Guide: Computer Programming: LEARN IN A DAY!

[hyperurl.co/html](http://hyperurl.co/html)

Programming: Swift: Create A Fully Functioning App: Learn In A Day!

[hyperurl.co/swift](http://hyperurl.co/swift)