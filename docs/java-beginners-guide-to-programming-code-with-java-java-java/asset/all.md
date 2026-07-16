![image-I0354B7T.jpg](Images/image-I0354B7T.jpg)![image-I0354B7T.jpg](Images/image-I0354B7T.jpg)

## Java:

## Beginner’s Guide to

## Programming Code

## with Java

#### Charlie Masterson

### Table of Contents

[Introduction](#chapter0001.html)

[Chapter 1: Java](#chapter0002.html)

[Chapter 2: Variables](#chapter0003.html)

[Chapter 3: Control Flow for Java](#chapter0004.html)

[Chapter 4: Arrays](#chapter0005.html)

[Chapter 5: Strings](#chapter0006.html)

[Conclusion](#chapter0007.html)

#### © Copyright 2017 by Charlie Masterson - All rights reserved.

The following eBook is reproduced below with the goal of providing information that is as accurate and reliable as possible. Regardless, purchasing this eBook can be seen as consent to the fact that both the publisher and the author of this book are in no way experts on the topics discussed within and that any recommendations or suggestions that are made herein are for entertainment purposes only. Professionals should be consulted as needed prior to undertaking any of the action endorsed herein.

This declaration is deemed fair and valid by both the American Bar Association and the Committee of Publishers Association and is legally binding throughout the United States.

Furthermore, the transmission, duplication or reproduction of any of the following work including specific information will be considered an illegal act irrespective of if it is done electronically or in print. This extends to creating a secondary or tertiary copy of the work or a recorded copy and is only allowed with express written consent from the Publisher. All additional right reserved.

The information in the following pages is broadly considered to be a truthful and accurate account of facts and as such any inattention, use or misuse of the information in question by the reader will render any resulting actions solely under their purview. There are no scenarios in which the publisher or the original author of this work can be in any fashion deemed liable for any hardship or damages that may befall them after undertaking information described herein.

Additionally, the information in the following pages is intended only for informational purposes and should thus be thought of as universal. As befitting its nature, it is presented without assurance regarding its prolonged validity or interim quality. Trademarks that are mentioned are done without written consent and can in no way be considered an endorsement from the trademark holder.

## Introduction

Congratulations on downloading Java: Beginner’s Guide to Programming Code with Java and thanks for doing so.

The following chapters will discuss what Java is and what it is used for.

By the end of this book, you should be able to use Java as you would any other programming language.  

Keep in mind that Java is not going to be the same as JavaScript. They are two completely different languages.

There are plenty of books on this subject on the market, thanks again for choosing this one! Every effort was made to ensure it is full of as much useful information as possible, please enjoy!

### Chapter 1:

## Java

The hardest thing about starting with Java is ensuring that you have everything installed that you are going to use with Java. Before you are able to write code, you have to have all of these programs or else you are going to set yourself up for a headache.

Virtual machine

The Java platform is going to be independent from any other program. So, it is going to be able to run on any operating system that you may be working with. It can work on any system thanks to the Java Virtual Machine. This machine is going to help in programming so that your code is processed correctly. The virtual machine program has to be installed before any Java code can be run.

A company called Oracle owns Java and on their website you are going to find the download link for the virtual machine which is also known as the Java Runtime Environment or JRE.

When you check to see if your computer already has JRE, you can click on the link on the Oracle page that says “Do I have Java?” This link can be located under the download button that is on the top of the page. When this link is clicked, the computer is going to be scanned and then you are going to get your result for if you have it or not. If you do not, then you will have the chance to download it from this page.

Once the virtual machine has been downloaded, you need to restart your system so that the program can run properly.

Software development kit

Now that the software has been installed, Java is going to be able to run on your computer. But, before you can write code, you will need to install the Software development kit off of the Oracle website as well.

This kit is known as the standard edition, and the one that you are going to want to use is known as NetBeans. The download will be rather large, but once it has been downloaded, you are going to be able to write Java code.

How things work with Java

The code for Java will be written in a text editor and the code is known as source code. Any code that you write is going to be saved in a file with the extension of .java. the Javac program has the ability to turn any source code that you write into Java Byte Code which is known as compiling. Once the file has been compiled, a new file is going to be created with a new extension of .class.

At the point in time that the class file is created, the virtual machine is going to be able to run the file. NetBeans is a program that will handle the creation and compiling of files for you. But, looking behind the curtain, you are going to notice that your source code will be created into a Java file which will then launch Javac to create your class file. NetBeans has the capacity to run the program with its own software so that you are saved the hassle of opening up different windows when you are entering commands.

NetBeans

When first entering NetBeans you are going to have to wait for a minute because this program is not that fast. But, when you finally get it loaded, you are going to go to file and then new project so that you can create a new application.

After you have clicked on Java Application, you are going to click the next button to go on to the next section. Obviously you are going to need to name your project which is going to change the text at the bottom of the window so that it matches what you have named your project.

A class is going to be created with your files name. If you name it as firstproject.FirstProject. the class is going to capitalize the F and P while the package is going to be lowercased.

NetBeans automatically defaults the save, but you can change it if you are going to be able to find it elsewhere better. A folder is also going to be created that will contain your projects name. Once you click the finish button, you are going to have all the files that you need created.

After you have been returned to the IDE you are going to be able to look at your projects to see if there are any projects that you are working on. When you hit the plus symbol that is located next to the project name, you are going to see all the folders that are associated with that project. Each folder is going to expand further so that you can see the file where your source code is stored.

Your source code should be displayed to the right inside of the text area. In the event that you do not see the code window, you are going to need to double click on your project so that the code appears and you can begin your work.

Your file name and your class name are going to have to match or else Java is not going to allow it to work properly and you will end up getting an error when it comes time to compile.

Comments

After you have created a new project, you are going to realize that there is some text in your text window that is grayed out and contains asterisks or slashes. These areas are going to be your comments and when the program is run, the comments are going to be ignored. You are going to be able to type anything that you want to in the comments but most of the time a comment is going to explain what you are doing with your code. A single line of comment is going to be typed by having two slashes in front of it

Code

// this is a comment

When you want more than one line of comments you have two options

Code

// your comment

//and it is going to continue here

Or

/*

your comment

And it is going to continue here

*/

You can also choose to use something known as a Javadoc comment where you will see a forward slash with two asterisks while it ends with a single asterisk and one slash. But, every line is going to have an asterisk in front of it. Javadoc comments are typically used in the document code. This code is going to be turned into an HTML page that will help others.

If you click on run at the menu found at the top of NetBeans, you can choose Generate Javadoc. However, you are not going to see anything since you have not written any code yet. You can delete comments that NetBean generates

Java structure

The package name is going to come first in your code. The line will end with a semicolon, and if you happen to miss that semicolon, the program is not going to be compiled. After your package name, the class name is going to be listed.

Think of your class name as a segment of code. Java has to be told where the code starts and where it ends with the use of curly brackets. The code is going to start with a left bracket and end with a right one. Whenever something is placed in these brackets, you are going to have a code segment.

When you are writing code, you will need to include the word main so that Java knows where it needs to start. This method is going to be a chunk of code but it is going to assist in executed any code that is inside of the curly brackets for your main. An error message is going to occur if you forget to put a main entry point into the programs that you write.

––––––––

Running a Java program

Whenever a program is run, it is going to be run in an output window that will be seen at the bottom of your screen. You are not going to need to start any terminals or console windows because the output window is your console.

You will have a multitude of ways that you can run your program when it comes to NetBeans. But, the easiest way for you to do it is to just press F6\. If you do not want to do that, you can also go to the menu and select the run project button.

There is also a green button that you will find on your tool bar that is going to run your program. Yet another way that you can run your program is to go to the projects window. You are going to be able to make sure that the proper code is going run by right clicking on the project that you want to be run and selecting run file.  This method can also be used inside of the actual text window by clicking somewhere that there is code.

Any way that you choose is going to run your program in the output window if you have written your code properly.

### Chapter 2:

## Variables

Most programs are going to work through the manipulation of data that has been placed into the program’s memory. This data is going to be objects, amounts, text, and any other pointers that are in the memory area. When you give the data a name, it can be renamed when you need to, but the name and value are going to be considered to be variables.

Amounts

When an amount needs to be stored in Java, there are going to be several options that you can use. There are whole amounts like 8 or 12 that can be stored as int variables. Int is going to stand for integer.

Then there are floating point amounts such as 8.4 or 10.5 that are stored as double variables. When you are storing these ones, you are going to need to use an equals sign.

Code

public static void main(String [ ] args) {

int last_amount;

System.out.println (“My Last Project”);

}

The program will require the developer communicate with it what the developer want to save an integer, so you are going to need to type int with a space following it. You will then be allowed to enter whatever you want the variable to be named. Variables can be named anything that you desire them to be named, however, there are a specific set of rules that you must abide by.

-  The name of the variables can mean different things. Being that the name will be case sensitive, names like firstname or FirstName are going to be two different names.  

-  A variables name cannot have a amount as the first character. Using the words to spell out the amount is going to be fine, but using the actual amount is going to cause Java to throw out an error message. The amounts are going to be used in other places of Java.

-  Variable names are not allowed to have spaces. The variables declaration of int first amount is going to throw an error message at you. You can use underscores or subsequent uppercases.

-  No keywords are allowed to be used as variable names. There are several keywords that are used in Java and NetBeans is going to turn these words blue in your coding.

At the point that you want to store a variable with the name of last_amount, you are going to enter an equals sign before you put the value that you want to store.

––––––––

Code

public static void main(String[] args) {

int last_amount;

last_amount = 10;

System.out.println (“My First Project”);

}

The program has to understand that the amount 10 needs to be stored as the Last_amount. You can also do all of this coding in a single line if you prefer to.

Code

public static void main(String[] args) {

int last_amount = 10;

System.out.println(“My Last Project”) ;

}

In order for the code to be put into action, the developer will need to manipulate the last line of the script to something similar to this:

System.out.printIn( “Last amount =” + last_amount) ;

The information that is between the round brackets is going to be direct text that has to be placed inside of double quotes. A plus sign is going to join the two halves of the expression together so that the text for the expression and the variable’s name are concatenated.

Once you have gotten all this code written out, you are going to be able to run it so that you can see it in the window at the bottom where your output is going to be displayed.

The integer that has been saved will be known as the last_amount.

When you are adding two integers together, one will store the amount for the two that you are adding together while a different one is going to store the result. Every variable will be separated by commas.

Code

last_amount = 30 ;

third_amount = 60 ;

result = last_amount + third_amount;

Your result is going to be the last and third amounts added together. The addition is going to be done with the use of a plus sign. When you have finished with the equation, your amount is going to be stored on the side of the equals that has the result variable. The first and third amounts being assigned, the amount is not going to be assigned until it has been added up.

Code

result = 30 + 60 ;

Java understands that there are two variables and you are not going to need to use the names. Your print in method is going to change too

System.out.println( “Addition Total =” + result) ;

Once more, the plain text is going to be combined and there are going to be double quotes around the variable’s name. You are going to be able to run the program and get it in the output window to see how it performs. 

Amounts can also be used directly so that the result is changed.

Code

result = last_amount + third_amount + 12 ;

When the program is run again, the result is going to going to be different as is your print in.

Large amounts can be stored in the int variable, but the limit is going to be 2147483647\. You can also do negative amounts, the lowest you will be able to go is -2147483648\. Larger or smaller amounts are going to use a double variable type.

Double variables

Double variables can be extremely large amounts to extremely small amounts. The highest and lowest amount you can reach is going to be 17 followed by about three hundred and seven zeros. A double variable is going to be used in holding floating point amounts. Should you be trying to store floating point values into any int variable, the program is going underline where the code is faulty so that you can change it before you run it and receive an error message.

Code

int last_amount, third_amount, result;

double last_amount, third_amount, result;

last_amount = 11.5;

third_amount = 22.8;

result = last_amount + third_amount ;

The program can now be run to show you what it is going to look like.

Short and float

Short variables will save smaller amounts that are going to be between -32768 and 32767\. You are not going to use in for the code like you have been, instead you are going to use short. When you use short, you need to ensure that the amounts that you are using are going to fall between the two amounts.

Double values are going to be used in storing the bigger amounts from floating points. You are not going to use a double but a float instead. When you go to store a float variable, the letter f is going to need to be at the end of your amount.

Code

float last_amount, third_amount, result ;

last_amount = 10.5f;

second_number = 20.8f;

Simple arithmetic

When you are doing math with the variables you are going to use basic symbols to do your calculations.

Addition (+)

Subtraction (-)

Multiplication (*)

Division (/)

Operation Precedence

More than two amounts can be calculated in Java, but you have to be sure to be careful when it comes to what is being calculated.

Code

last_amount = 200;

third_amount = 85;

fourth_amount = 45;

result = last_amount – third_amount + fourth_amount;

The calculation is going to need to be done in the order that it appears. So what you are going to do is subtract 85 from 200 to get 115. Then you are going to add the third amount to get 160.

To make sure that Java does what you want to do, you can use brackets.

––––––––

Code

result = (last_amount – third_amount) + fourth_amount

result = last_amount – (third_amount + fourth_amount)

With multiplication, you are going to do the multiplication will come over doing any addition or any other operation.

The order of precedence is going to be that multiplication and division are going to cover over addition or subtraction.

String variables

Amounts are not the only things that can be stored, variables can also store text. When you want to store a character, you are going to need to use the char keyword so that Java knows you are using a character instead of a amount. As you are storing more than one character, you are going to use a string variable.

Start a new project like you did with the first chapter, label the project something like StringVars. The box needs to be ticked so that a main class is created. You can delete main that comes after stringvars and enter StringVariables instead.

Deleting all of the comments, you are going to have a code window that is going to look similar to the one earlier. In order to create a string you are going to use the word string for your keyword which will then be followed by the variable name. semicolons are still going to be used.

Code

String middle_name;

The value is going to be assigned to the new variable by using an equals sign again. The text that comes after the equals sign, is going to be stored inside of a set of double quotes.

middle_name = “William” ;

This code can also be placed in a single line

Code

String middle_name = “William” ;

In a different string, you are going to enter the family name of the client.

––––––––

Code

String inherited_name = “Shakespeare” ;

In your print statement you are going to get both of them together

Code

System.out.println (middle_name + “ “ + inherited_name) ;

The information that sits inside of the parentheses is going to be whatever our variables are. The plus sign is followed by a space and that space has double quotes. The double quotes help Java to recognize that there needs to be a space between these two characters.

Your code is going to look messy, but you are only going to get a print out of the name and the family name whenever the code is run.

The keyword char is going to use a lowercase c whenever a single character is being stored. Single quotes are also going to be used instead of double quotes. When you surround the char character with double quotes, the code is going to be underlined thus giving you an error code.  Single characters are going to use double quotes when creating a string variable.

Code

String middle_name = “W”;

While the syntax above will be the proper way

String middle_name = ‘W’;

This is not.

Client input

With Java, there are huge libraries that you are going to be able to use so that you can see what codes are supposed to do. Should you need to reference the library, you will need to use a method that has been called into action. One of the more useful classes is going to handle the input that you get from your client called Scanner. The class can be acquired in the java.util library. The Scanner that is used has to have a reference inside of your code. The keyword that you are going to use is import.

Code

import java.util.Scanner ;

The statement that carries the most weight needs to be the one that is settled in before the statement containing the section with the class.

Code

import java.util.Scanner ;

public class StringVariables {

}

The program has been told that there is a certain class listed inside of the library and that it is inside of the java.util library. After that has been done, you have to establish an item in the Scanner class. This group is nothing more than a series of code but it is not going to do anything until a new object has been created from it.

When you are creating a new object with Scanner, you are going to use a particular piece of coding.

Code

Scanner client_input = new Scanner( System.in) ;

An int variable is not going to be set up and neither is the String variable. Instead, you are setting up a Scanner variable with the name client_input. The keyword that goes after the equals sign is going to be new. You are going to use this keyword when you are creating new objects from the class that you have chosen. The object that you have created is going to be located between two parentheses. Java will then have to be told that it is the system’s input (System.in).

For the client input, an action is going to have to be called upon with one of the methods that you can use with the new object that you have created. One method that you can use is called the next method. This is going to take the string that comes next from what the client types into the program.

Code

String middle_name;

middle_name = client_input.next() ;

Once your client enters data, you are going to enter a dot. There is a popup list of methods that you are going to have available to you. Simply double click on the next before you type the semicolon into the end of your line. You are also going to be able to print some of your text in so that you can prompt the client to enter in data that you want.

––––––––

Code

String middle_name;

System.out.print (“ Enter your middle name: “ ) ;

middle_name = client_input.next () ;

When you put in your prompt for your client, you are not going to use println but you are going to use print. If you use println you are going to move the cursor into a new line once there is an output. But with print, it is going to stay in the same line.

Code

String inherited_name ;

System.out.print (“Enter your family name: “);

inherited_name = client_input.next() ;

The code is identical, but Java is going to keep any input the client gives you inside of a new variable.

Should you want to print the input out that you get, you are going to do this:

String complete_name;

complete_name = middle_name + “” + family_name ;

System.out.println (“You are” + complete_name);

When this program is run, Java is going to pause so that the data can be entered by the client. Once all the data that is needed has been entered, the proper output is going to be displayed on the screen.

Ultimately, the Scanner class is going to be used in getting input from the client. Anything that client types in is going to be stored into the appropriate variables.

Option Panes

Like the Scanner class, there is the JOptionPane class that is going to be useful when you are trying to get input from your client. This class is going to pop up input windows for the client to enter in the proper data along with windows that say things like “Hello”.

Code

import javax.swing.JOptionPane;

Java is going to be told that you want the JOptionPane class to be used and that it is inside of the javax.swing library.

A new project can be started again for the practice of this if you don’t want to change any of your previous code. When you enter in your code, you may notice that the import javax.swing.JOptionPane; is going to be underlined. This happens because this code has not been used yet. Once it has been, the underline is going to vanish.

In order to get a box that allows the client to input some type of data you are going to select the showInputDialog method from the JOptionPane. This will cause the data that is inputted to be stored straight to its proper variable.

Code

String middle_name;

middle_name = JOptionPane.showInputDialog (“ Middle Name “) ;

After you have typed a full stop with your JOptionPane a list is going to pop up. From here you are going be able to double click on the showInputDialog so that between your brackets you are going to type a message that you want to be displayed. Like anything else, it should fall between a set of double quotes.

Code

String inherited_name;

inherited_name = JOptionPane.showInputDialog (“Family Name”) ;

String complete_name;

complete_name = “You are” + middle_name +”” + inherited_name;

JOptionPane.showMessageDialog (null, complete_name );

At this point you are going to want the showMessageDialog from your option list. The word null is now going to appear between your brackets and this keyword lets Java know that the dialogue box will have little to do with the program. The puncuation is going to come in the text that you want to be displayed inside of the message box.

At the bottom of your code you may notice that there is a new bit of code. The system.exit(0); makes sure that the program is able to exit while removing any objects from the memory.

When your code is run, you are going to get pop up boxes that are going to ask for the data that you have specified that you would like the client to input. Once the okay button has been clicked your input is going to be displayed. Clicking okay again will cause the program to end.

### Chapter 3:

## Control Flow for Java

Any programming that you have done before this point is going to be known as sequential programming which basically means that the code you have entered was read from top to bottom, every line being read the way that it is written. However, not all programs are going to work like that.

Some code has to be run but only in the event that a condition has been met. For code, you may want your client to be of a certain age. This is going to be where you will control the flow of how the program operates through conditional logic.

Conditional statements are going to use the word if mostly, but there are other words that can be used to create conditional statements.

If statement

The code is going to be executed whenever something happens instead of waiting for something else, which is going to be most common when it comes to programming, therefore the if statement was created.

An if statement is going to look like this:

if ( statement ) {

}

The word if is going to be lowercased before your condition is paced in a set of brackets. The curly brackets are going to be used to divide the chunks of code. This code is going to be executed only in the case that the condition has been met.

Code

if( client < 18) {

}

This condition states that if the client is less than 18\. Instead of typing it all out, a shorthand method is going to be used so that the chunk of code is shorter and easier to read.

Code

if( client < 18) {

// display message

}

Therefore, should the client be over 18, the code set in the two sets of curly brackets is going to be jumped over while Java proceeds how it is supposed to. Anything that is in the middle of the curly brackets will be carried out only if the condition has been met.

Another shorthand notion is going to be to point the triangle to the right which means greater than.

Code

if( client > 18) {

//display message

}

The code is the exact same except that the condition is going to apply to those who are over 18.

If ... else

Instead of an if statement being used, an if else statement can be used.

if( condition_to_test) {

}

else {

}

The first line will still start with if while being followed by the condition. The curly brackets are going to divide different parts of the code. The second choice is going to go after the else with its own curly brackets.

There are only two choices that you are going to have, either your client is going to be younger than 18 or older than 18\. Your code will have to match what you want to happen.

If ... else if

More than two conditions can be tested at once. If you want to test a certain range of ages, you are going to use an if else if statement. The syntax is going to be:

if(condition_one) {

}

else if ( condition_ two ) {

}

else {

}

The newest part of the code is going to be the else if ( condition_two) {

}

When the if statement is sent, the next is going to be followed by round brackets. The second condition is going to be in between two new brackets but it is not going to be caught by the first condition. The code is still going to be sectioned off with curly brackets with every if else if statement that you have each having its own curly brackets. If you miss one then you are going to get an error message.

The conditional operators that you need to use are

Greater than (>)

Less than (<)

Greater than or equal to (>=)

Less than or equal to ( <=)

AND (&&)

OR ( ||)

Equal ( ==)

NOT (!)

The two ampersand symbols are going to be used to test for more than one condition at the same time.

Code

else if ( client > 18 && client < 40)

With this code, you are going to want to have the knowledge need to know the age of the client and to see if they are older than 18 but younger than 40\. You are only trying to see what is inside of the variable that the client inputs. The client has to be older than 18 but younger than 40\. Your client has to meet both conditions since the AND operator was used.

Nested if

If statements can be nested just like if else and if else if statements. An if statement that has been nested is going to be putting one if statement with another.

Code

if( client < 19) {

System.out.println ( “ 18 or younger”) ;

}

To check and see if your client is over sixteen there has to be another if statement placed inside of the if statement that you have already created.

Code

if( client < 20) {

if( client > 20 && client < 23 ) {

System.out.println (“ You are 21 or 22”) ;

}

}

The first if statement will be where the client is going to be caught if they are less than 19 and the second one will narrow it down so that they are over 16\. When you want to print a different message, you can use an if else statement.

Code

if( client < 20) {

if( client > 20 && client < 23 ) {

System.out.println( “You are 21 or 22”) ;

}

else {

System.out.println (“22 or younger”) ;

}

}

The curly brackets that are placed in the code have to be exact or the program is not going to be run. Nested if statements are tricky to learn, but they can be narrowed down.

Boolean values

Boolean values are only going to be true or false, 1 or 0 or even yes or no. Java has a variable that is done for Boolean values:

Boolean client = true;

You are not going to need to type int, string, or double you are going to need to type Boolean by using a lower case b. the name of the variable will come after it has been assigned to the value of true or false. The assignment is going to have one equals sign. However, should you evaluate the variable and it has a value of something then you are going to need to use two equals signs.

Code

Boolean client = true;

if ( client == true) {

System.out.println (“it’s true”) ;

}

else {

System.out.println(“it’s false”) ;

The if statement is going to see if the variable entered by the client is true. the else will check to see if it is false. You are not going to need to say “else if ( client == false)”. When something turns out to not be true, it is going to obviously be false. You are going to use else since there are only going to be two choices when it comes to Boolean values.

The other operator that is used for conditions is the NOT operator, this is used with Boolean values.

Code

Boolean client = true ;

if( !client) {

System.out.println (“it’s false”) ;

}

else {

System.out.println (“it’s true”) ;

}

––––––––

The NOT operator is going to come before the client’s variable. This operator will use a single exclamation mark but it will fall before the variable that has to be tested. The code is going to be tested for negation which means that it is not what it actually is.

Since the client variable has been set to true, the !client will end up testing for false values. If the condition is set to false, then the NOT operator will test for values that are true.

Switch statements

To manage the workings of our script, the developer can use a switch statement. The switch statement is going to give you the options that are in the range of values that have been set for your variable. Essentially these are long and complex if else if statements

So the syntax for this is going to be:

Switch ( variable_to_test) {

Case value:

//Code_here;

Break;

Case value:

//Code_here;

Break;

Default:

// The values_that_were_not_caught_from_the _conditions_above;

}

This code is going to begin with the keyword switch before being trailed by a set of parentheses. Any variable that you want to evaluate on will go in the middle the brackets of the switch. The curly brackets are going to contain all the other parts of your switch statement. With every power that you need to review, the developer will be using a keyword known as case so that they can check the worth of the case.

The case value is going to come with a colon. Whatever you want to happen is going to but only in the event that the value corresponds correctly. You code that you want to be carry out is going to be executed. The word break will be used whenever the break is needed in every case of switch statements.

A default value is going to be used but it is completely optional. You can include other values with your variables if you have not checked it elsewhere that is in your switch statement.

Code

public static void main(String[] args) {

int client = 17;

switch ( client ) {

case 19:

System.out.println(“ You are 19”) ;

break ;

case 20:

System.out.println (“ You are 20”) ;

break ;

case 21: 

System.out.println (“ You are 21”) ;

break ;

default:

System.out.println (“ You are  not 19, 20, or 21”) ;

}

}

The code is going to set a value that has to be tested for. An integer variable is going to be called client. In this code the value has been set to 18\. With the switch statement, the variable is going to be checked to see what is inside of it. Every case is going to be checked in its own right until it finds one that matches. Once it has found the proper one, the code is going to be stopped and a switch statement will be broken out.

You are not going to be able to test out a range of values that have been placed in a case so you are not going to be able to complete this action:

case ( client <= 19):

However, you may place your code in a line such as this:

case 1: case 2: case 3: case 4:

Every value will be checked, but you are going to have to spell every value out.

Loops

With the flow being sequential and the flow going downwards you are going to have to tell Java to do it differently if that is not how you want it to be. So to interrupt this flow, what you can do is create a loop. As it this called, the loop will force the program to go back and re-execute the lines of code repeatedly.

Code

int addition = 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10;

Because of how long this can end up being, you are not necessarily going to want to use this method. You can use a loop instead so that the code is repeated until it has reached a specific condition. Once it has reached that point, you are going to exit the loop and move on with the next bit of code.

For loops

For loops will be one of the single most commonly used loops that you will see. The loop is going to go for a specific amount of loops. The syntax for a “for” loop is:

for ( beginning_value; last_value ; increment_amount) {

//this is where your code will appear

}

In a set of round brackets you are going to be placing three different items: The beginning amount for your loop, the ending amount for the loop, and the path that it will follow to get from one amount to the next. Normally the increment amount is going to be one. However, it does not have to be, if you want it to be ten, you can make it ten.

Following the parentheses a set of curly brackets is going to be placed so that the code that will be repeated is sectioned off.

Code

package loops ;

public class ForLoops {

public static void main (String[] args) {

int loopVal;

int last_value = 15;

for (loopVal = 0; loopVal < last_value; loopVal++) {

System.out.println ( “Loop Value = “ + loopVal) ;

}

}

}

Whenever an integer value has been set up, it is going to be called a loopVal. The next line that has to be set up is another variable for an integer. This variable is going to be used as the value where the loop is going to end.

Inside of the brackets you are going to have:

loopVal = 0; loopVal < last_value ; loopVal++

Java is going to be told what amount starts the loop. This is also where the value is going to be assigned from zero to the variable of the loopVal. The second part is going to be the conditional logic:

loopVal  < last_value

the loopVal is going to be a smaller amount than what the last_value is. The “for” loop will go until the value is going to be of lesser value than the value of the variable at the end. Just as long as the value stays true, Java is going to continue to loop the code that is placed between the curly brackets.

The final loop part of loopVal++ says that the value is going to go up by one every time.

While loops

While loops are simper to have knowledge of than the for loops. The syntax for a while loop will be:

while ( condition) {

}

The word while is going to be lowercased and your condition is going to be placed between the parentheses. The curly brackets are will have code

Code

int loopVal = 0;

while (loopVal < 5) {

System.out.println (“Printing some text”);

loopVal++ ;

}

The condition in the parentheses is going to be less than fine and the code in the curly brackets will be the code that has to be printed out. The loop is going to go on forever because there is not any value of 0.

Counter loopVal is going to get to the end of the condition. While loops are good to use when you do not need to count a value but are checking a value instead. For code, it can keep looping when a key is not being pressed on a keyboard. But, the letter x is going to exit the loop.

Do while

––––––––

A do while loop is just like a while loop but it looks different.

int loopVal = 0;

do {

System.out.println( “Printing some text”) ;

loopVal++;

}

while ( loopVal < 5 ) ;

The loop is going to continue up until the condition has been met. The biggest distinction between the two loops is going to happen with the code that you place in the brackets. The code for the do while loop is going to be examined at least once, but with a while loop it is going to happen until the condition has been satisfied.

Java is going to bail out of the loop and not carry out the code inside the brackets. When you are want to test this out, you are going to need to use a while loop first. The value has to be changed for the loopVal variable before the code is run. The text is not going to be printed.

### Chapter 4:

## Arrays

An array is going to hold more than a single value at a time; it is more of a list of items. When you are thinking of arrays, you should think of a spread sheet and how there are columns. You can have one column or a bunch of columns.

––––––––

An array that is in one column is going to look like this:

0 – 10

1 – 14

2 – 36

3 – 27

4 – 43

5 – 18

Just like a spread sheet, every row is going to have a position amount. The positions are going to start at zero and go up by one every time. Each position will hold a value just like the code above.

When you want to set up an array, you are going to need to let Java know what sort of data you are putting into the array. You are also going to need to say exactly how many positions the array is going to have.

The syntax will be: int [ ] aryNums;

The difference is going to be that the normal integer variable is going to be in square brackets once the data type has been set. The brackets will let Java know that you have set an array up. The name for the array is going to be aryNums. But, like any normal variable, you are going to be able to call them anything that you want.

When you are telling Java how many positions the array is going to have, you have to set up a new object for the array.

Code

aryNums = new int[ 6 ];

At first you are going to be starting with the array’s name then followed by an equals sign. The equals sign is going to have a new keyword before you get to your data type. The type of data that is being used is going to be followed by the array’s size. The size will let Java know how many positions the array needs to have.

You can also put it all in one line if that is how you prefer your code to look.

Code

int[ ] aryNums = new int[ 6 ] ;

Java is going to know that you are using an array that has six positions in it and that the data type is integers. Therefore, the default values are going to be zero to six.

When you want to assign the values to a various amount of positions, you are going to do it like normal.

Code

aryNum[ 0 ] = 10 ;

The value of ten will be assigned to the zero in the array.

Remember that the array is always going to start at zero and the third position is going to be the index of the amount two.

To make it easier to set your array up, you can do it like this:

int[ ] aryNums = { 1, 2, 3, 4 } ;

With this method, you are going to place your values for the array in the curly brackets. The first value as always is going to be zero. There are going to be square brackets after int but there is not going to be a new keyword nor will there be any data type that has been repeated. You can only use this method with in, char, and string values unless you want to use a new keyword.

String[ ] aryStrings = { “ Autumn”, “Spring”, “Summer”, “Winter” } ;

This is okay

Boolean[ ] aryBools = { false, true, false, true } ;

This is not okay!

In setting up a Boolean array, you are going to have to use a new keyword

Code

Boolean[ ]  aryBools = new Boolean[ ]  { false, true, false, true } ;

––––––––

Loops and arrays

Arrays are going to have their own loops. When a value has been assigned to an array you are going to use the syntax that you saw in the last section. While this is not entirely practical, it can work in the event that you have a lot of amounts that need to be assigned to the array.

Code

package prjarrays ;

public class ArrayTest {

public static void main (String[]  args) {

int[ ] lottery_amounts = new int [ 49 ] ;

int I ;

for ( I = 0; I < lottery_amounts.length ; i++) {

lottery_amounts[ I ] = I +1;

System.out.println ( lottery_amounts[ 1 ] ) ;

}

}

}

This array is going to have 49 different integers. The end of the loop has a length which is going to note how many positions the array will have. This loop is going to continue to go until the value of I is a smaller amount than the array’s size.

In order to appoint a amount to the positons the developer will use this:

lottery_amounts[ I ] = I + 1 ;

Instead of a hard coded value that is set between the square brackets, there is going to be a variable that will increase every by one every time that the loop goes around. Each array is going to be accessed by the loop’s value. The value being assigned here is I + 1. Since the loop value starts at zero you are going to have the amounts one through forty-nine.

The next line for the loop will print out the value for every array position. Should you want to, you can write out the code so that it is jumbled up with the amounts in the array. After the values, have been jumbled, you are going to us the first six as the lottery amounts.

Sorting Arrays in Java

With Java methods, you are going to be able to sort out the arrays that you create. Using the sorting method is going to mean that you have to have a reference to the Array’s in the Java library. This can be done with an import statement. Your syntax will be:

Code

import java.util.Arrays ;

package prjarrays;

import java.util.Arrays ;

public class ArraysTest {

public static void main ( String[]  args) {

int[]  aryNums;

aryNums = new int [ 6 ] ;

aryNums[ 0 ] = 20 ;

aryNums[ 1 ] = 16 ;

aryNums[ 2 ] = 38 ;

aryNums[ 3 ] = 29 ;

aryNums[ 4 ] = 45 ;

aryNums[ 5 ] = 12 ;

With the Arrays library being imported, you are now going to be able to use the sort method. Arrays.sort( aryNums ) ;

The first word you are going to enter is Arrays before you add in a dot. After the dot, NetBeans is going to show you a list of everything that you are able to do with an array. The word sort come next before the array’s name is placed inside of the parentheses. You are not going to need to have square brackets after what you have named the array.

Code

package prjarrays;

import java.util.Arrays ;

public class ArraysTest {

public static void main( String[]  args) {

int[ ]  aryNums;

aryNums = new int[ 6 ] ;

aryNums[ 0 ] = 20 ;

aryNums[ 1 ] = 16 ;

aryNums[ 2 ] = 38 ;

aryNums[ 3 ] = 29 ;

aryNums[ 4 ] = 45 ;

aryNums[ 5 ] = 12 ;

Arrays.sort(aryNums) ;

int I;

for ( I = 0 ; I < aryNums.length ; i++) {

System.out.println(“num: “ + aryNums[ I ] ) ;

}

}

}

When you are using the sorting method, you are going to sort it in descending order, but this is only going to happen if you write out your own sorting code, or if you go to converting the array into integer objects that have been imported from the Collections library.

Code

package prjarrays;

import java.util.Arrays ;

import java.util.Collections ;

public class SortDescending {

public class ArraysTest {

public static void main( String[]  args) {

int[ ]  aryNums;

aryNums = new int[ 6 ] ;

aryNums[ 0 ] = 20 ;  aryNums[ 1 ] = 19 ; aryNums[ 2 ] = 39 ;

aryNums[ 3 ] = 26 ; aryNums[ 4 ] = 45 ; aryNums[ 5 ] = 12 ;

Arrays.sort(aryNums) ;

int I;

for ( I = 0 ; I < aryNums.length ; i++) {

System.out.println (“num: “ + aryNums[ I ] ) ;

}

}

}

Strings and arrays

Arrays can be put into strings just like integers

Code

String[ ]  aryString = new String[ 5 ] ;

aryString[ 0 ] = “this” ;

aryString[ 1 ] = “is” ;

aryString[ 2 ] = “a” ;

aryString[ 3 ] = “string” ;

aryString[ 4 ] = “array” ;

This code has five different positions and every bit of text has been placed into the array where it belongs.

Here is a loop that is going to use all the positions of the array, but it is going to print out every position.

int I ;

for ( I = 0 ; I < aryString.length ; i++ ) {

System.out.println( aryString[ I ] ) ;

}

This loop will repeat until the value is of lesser value than what the range of the array has been called for.

Arrays can also be sorted alphabetically therefore aa is going to be before ab. But, since Java uses a set of characters known as Unicode, in order to contrast the letters in the string to other letters, the uppercase letters are going to come before the lower cased ones.

Code

package strings1 ;

import java.util.Arrays ;

public class StringArrays {

public static void main(String[]  args) {

String[ ]  aryString= new String[ 5 ] ;

aryString[ 0 ] = “This” ;

aryString[ 1 ] = “is” ;

aryString[ 2 ] = “a” ;

aryString[ 3 ] = “string” ;

aryString[ 4 ] = “array” ;

Arrays.sort( aryString ) ;

int I ;

for ( I = 0; I < aryString.length ; i++) {

System.out.println ( aryString[ I ] ) ;

}

}

}

Arrays that are Multi-Dimensional

The arrays that were talked about previously in the chapter have only been single columns of data, but, you are able to set up arrays that have multiple columns. These arrays are known as multi-dimensional arrays.

Code

0 – 10 – 12 -43 – 11 - 22

1 – 20 – 45 -56 – 1 - 33

2 – 30 – 67 – 32 – 14 – 44

3 – 40 – 12 – 87 – 14 - 55

4 – 50 – 86 – 66 – 13 – 66

5- 60 – 53 – 44 – 12 – 11

A multi-dimensional array is arranged in this fashion:

int[ ] [ ] aryAmounts = new int[ 6 ] [ 5 ] ;

The array is going to be set up exactly like a normal array, but there are going to be two square bracket sets. The first set is going to tell Java how many rows there are going to be while the second set tells how many columns.

Code

aryAmounts[0][0] = 10;

aryAmounts[0][1] = 12;

aryAmounts[0][2] = 43;

aryAmounts[0][3] = 11;

aryAmounts[0][4] = 22;

The first row is going to be zero like always, then the columns are going to go to four which is going to result in five items being placed on the array.

Code

Your second row is:

aryAmounts[1][0] = 20;

aryAmounts[1][1] = 45;

aryAmounts[1][2] = 56;

aryAmounts[1][3] = 1;

aryAmounts[1][4] = 33;

The first for loop is going to use the position of the amounts in rows while the second loop uses the position based on columns. The first loop is going to be the value of I which is zero. The code that is nested inside of the loop will be used for a different loop. The next loop is going to be evaluated as long as the variable of I is zero.

Lists for Arrays

It is hard to tell the exact amount of items that are going to be inside of an array, so it is going to be easier for you to use an ArrayList. The ArrayList is a data structure that is going to be dynamic. Therefore, your items can be added and removed. Normal arrays have data that is static since you are not going to be able to change the original size of the array that you have created.

When you are setting up ArrayList, you are going to have to make sure that you pull the package from the library with the following syntax.

import java.util.ArrayList;

Once it has been imported, you are going to be able to create new objects on the list with this syntax:

ArrayList listTest = new ArrayList( );

You are not going to need to have square brackets when you are using an Array List.

Code

listTest.add( "first item" );

listTest.add( "second item" );

listTest.add( "third item" );

listTest.add( 7 );

What falls in the middle of the parentheses is going to be added to the list. You are only going to be able to add objects. The first three items on this list is going to be added as objects of a string. The last item is an amount because of the amount object for the integer.

The items that you put on your list are going to be referenced by their index amounts.

Code

listTest.get( 3 );

This means that the line is going to get its item at index three. The index amounts are still going to start at zero. Therefore, this is going to be your fourth item.

Items can also be removed from your list with their index amounts.

Code

listTest.remove(2);

the value that is assigned in the list may also be used

Code

listTest.remove( "second item" );

Whenever an item is removed, the list is going to be resized, this means that you are going to need to be careful before you try and get an item from your list with the use of its index amount. If you remove the second object, then the list is going to contain three items once that item is gone.

When you want to go through each item on the list so that you design an iterator, this is another section that you are going to be able to locate in the java.util library.

import java.util.Iterator;

From here, the developer is going to be able to attach the ArrayList to the new Iterator object:

Iterator it = listTest.iterator( );

After the iterator has been set up, it is going to be used when items have to be gone through on the list which is called a listTest. The explanation for why iterator is used is because the techniques that are called next and hasNext, these are going to be used in a loop:

while ( it.hasNext( ) ) {

System.out.println( it.next( ) );

}

The hasNext strategy is going to return a Boolean value to you. This item will be untrue since no other objects on the ArrayList. At this point the next technique to be used is going to scan all of the objects that are on the record.

Code

public static void main (String[] args ) {

ArrayList listTest = new ArrayList( ) ;

listTest.add( “first item” ) ;

listTest.add( “second item” ) ;

listTest.add( “third item” ) ;

listTest.add( “8” ) ;

Iterator it = listTest.iterator( ) ;

while ( it.hasNext( ) ) {

System.out println( it.Next( ) ) ;

}

// remove the item from the list

listTest.remove ( “second item” ) ;

// print out a new list

System.out.println(“Whole list = “ + listTest) ;

//get the item at the index of position one

System.out.println(“Position 1 = “ + listTest.get( 1 ) ) ;

}

The line that prints out the entire list is going to be helpful if your list is going to be too long. This can be achieved with the syntax of:

System.out.println( "Whole list=" + listTest );

The code that has been run is going to display this in the output window:

first item

second item

third item

7

Whole list=[first item, third item, 7]

Position 1=third item

### Chapter 5:

## Strings

Strings are going to be different than the variables used for integers or variables for the double integers. The strings are actually items.

Storing strings

Strings use Unicode characters that are under the variable name.

Code

String someText = "Bill";

Java is now informed that the string’s object is going to be four characters. The Unicode character sets are \u0042, \u0069, \u006c, \u006c. The values for the Unicode will be stored inside of hexadecimals. Any capital letters are going to be stored with the value of \u0041 to \u005a, at the same time lowercase letters are kept using the values \u0061 to \u007a.

Code

package strings1 ;

import java.util.Arrays ;

public class StringArrays {

public static void main(String[]  args) {

String[] aryString = new String [ 5 ] ;

aryString[ 0 ] = “This” ;

aryString[ 1 ] = “is” ;

aryString[ 2 ] = “a” ;

aryString[ 3 ] = “string” ;

aryString[ 4 ] = “array” ;

arrays. Sort( aryString ) ;

int I ;

for ( I = 0; I < aryString.length ; i++) {

System.out.println( aryString[ I ] ) ;

}

}

}

When this code is sorted alphabetically, a is not going to come first because it is lowercase. Therefore, a is going to have a value of u\ 0061\. The T that is capitalized will have a value of u\0054.

In manipulating strings of different texts, there are some methods that you can use:

toUpperCasse

toLowerCase

compareTo

IndexOf

endWith, startsWith

Substring

Equals

charAt

trim

valueOf

Lower and Upper case letters

Java is going to convert the text to either lowercase or uppercase in a manner that is straightforward and will use the methods that are built into the toUpperCase and toLowerCase.

Code

Package prjstrings;

Public class StringManipulation {

Public static void main (String[] args) {

String changeCase = “text to change” ;

String result ;

Result = changeCase. toUpperCase( ) ;

System. out. printIn( result ) ;

}

}

The very beginning lines tell where the variable has been set up for the string while holding on to the text that has to be changed before it is printed. The third line calls for the result of the variable. Finally, in the fourth line, it is converted.

result = changeCase.toUpperCase( );

The string method is going to work on any string. You will just need to type a dot after the variable so that you can see what you can do with the string for your changeCase. If you want it to be uppercase, then you are going to select it, but keep in mind that the uppercase should have a set of empty brackets that come after it.

Once the result has been converted, it is going to be stored as the new result. If you do not want the result stored, you can use this:

System.out.println( changeCase.toUpperCase( ) )

The same method is going to be used when you want to do toLowerCase.

String comparison

Strings can be compared to each other through the use of hexadecimal values. You will just need to use the compareTo method.

Code

package prjstrings ;

public class StringManipulation {

public static void main (String[] args) {

int result ;

String Word1 = ‘Ape” ;

String Word2 = “App” ;

result = word 1.compareTo( Word2 ) ;

if (result < 1 ) {

System.out.println (“Word1 is less than word2” ) ;

}

else if (result > 0 ) {

System.out.println(“Word 1 is more than word 2” ) ;

}

else if (result == 0 ) {

System.out.println (“the same word”) ;

}

}

}

When these two words were being compared the compareTo method was used with this syntax:

result = Word1.compareTo( Word2 );

A value is going to be returned that will be greater than zero, less than zero, and have a value that equals zero.

It is going to be up to you to make sure that the proper value is assigned so that the compareTo is returned to the variable. If statements are going to be in the code to test and see what the result is going to be.

But, when two strings are compared, Java is going to compare the hexadecimal values instead of the word’s letters. Since both have uppercase letters the A for App is going to be used before ape.

indexOf

The indexOf is going to locate a character inside of the current string or any other string.

Code

package prjstrings ;

public class StringManipulation {

public static void main (String[] args) {

char ampersand = ‘ @ ‘ ;

String email_address = “meme@me.com” ;

int result ;

result = email_address.indexOf( ampersand ) ;

System.out.println(result) ;

}

}

This code is checking to see if the @ symbol is located in the email address that was provided. Because of the single quotes it is a char variable. Once the email has been set up, you are going to have your result which will be an int variable. Therefore, your result is going to be an integer thanks to the indexOf method.

The position for your ampersand is going to be the result for this code because of this line:

result = email_address.indexOf( ampersand );

The string that you want searched first is going to come after the dot when you specify that you want to use the indexOf method. Between the parentheses is going to be where you will have several options. First, you can type in a single character. With this, Java will tell you the position of the character in the string before it stores the value for the result of the variable.

When the code is run, the output is going to be four. Since indexOf starts at zero like everything else, the ampersand is going to be the fourth character in the email string.

Should the character that you are looking for not exist, then indexOf will give you a result of negative one.

Code

package prjstrings ;

public class StringManipulation {

public static void main(String[] args) {

char ampersand = ‘ @ ‘ ;

String email_address = “mememe.com” ;

int result ;

result = email_address.indexOf( ampersand ) ;

if ( result == -1 ) {

System.out.println( “invalid email address” ) ;

}

else {

System.out.println( “email address is okay” ) ;

}

}

}

Your result of negative one is going to allow the client to continue.

IndexOf can also be used to test for multiple characters.

public static void main (String[] args) {

String dotcom = “ .com “ ;

String email_address = “ meme@me.com “ ;

int result ;

result = email_address.indexOf( dotcom ) ;

if (result == -1( {

System.out.println( “invalid email address” ) ;

}

else {

System.out.println(“email address is okay”) ; 

}

}

While this code looks exactly the same, you are now going to be using the variable from the string in order to hold the text that you want to check for instead of the char variable.

With another result of negative one being returned, the text that was searched for could not be found in the string that comes before the dot for the indexOf method. If it had, then the indexOf would have returned the character that first matched what you were searching for.

In the code listed above, the dot is going to be the seventh character inside of the email address whenever you start counting from zero.

## Conclusion

Thank for making it through to the end of Java: Beginner’s Guide to Programming Code with Java, let’s hope it was informative and able to provide you with all of the tools you need to achieve your goals whatever it may be.

The next step is to download Java like it was stated in the first chapter and to begin writing out your code. Java is going to have a lot of different rules that are going to confuse you, however, this is not something that should discourage you. In the event that you get confused when you are going through your practice, you can always go back and reread what has been written.

You are bound to mess up, but it is going to happen. Do not worry about any mistakes that you make, you can erase them and start over when an error code has been given to you. Be patient with your coding abilities because they are not going to be spot on the first time. It will take you some time before you are an expert in Java or any other language that you decide to learn along the way.

Thanks again and good luck!

![Charlie Masterson](Images/image-DOT1I4H3.jpg)

## About the Author

Charlie Masterson is a computer programmer and instructor who has developed several applications and computer programs.

As a computer science student, he got interested in programming early but got frustrated learning the highly complex subject matter.

Charlie wanted a teaching method that he could easily learn from and develop his programming skills. He soon discovered a teaching series that made him learn faster and better.

Applying the same approach, Charlie successfully learned different programming languages and is now teaching the subject matter through writing books.

With the books that he writes on computer programming, he hopes to provide great value and help readers interested to learn computer-related topics.