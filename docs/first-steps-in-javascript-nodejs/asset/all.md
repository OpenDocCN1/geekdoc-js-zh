![](image_rsrcJJ.jpg)

First Steps in JavaScript (Node.js)

Ruhan Avila da Conceição

# Summary

[Summary](#part0002.xhtml)

[Notes on the Book](#part0003.xhtml)

[A brief history of JavaScript](#part0004.xhtml)

[Preparing the Programming Setup](#part0005.xhtml)

[Modules in JavaScript](#part0006.xhtml)

[NPM e NPX](#part0007.xhtml)

[First Steps in JavaScript](#part0008.xhtml)

[Advantages of Node.js](#part0009.xhtml)

[Storing Values in JavaScript](#part0010.xhtml)

[Data Types in JavaScript](#part0011.xhtml)

[Mathematics in JavaScript](#part0012.xhtml)

[Strings in JavaScript](#part0013.xhtml)

[Control Structures](#part0014.xhtml)

[Functions](#part0015.xhtml)

[Arrays in JavaScript](#part0016.xhtml)

[Objects in JavaScript](#part0017.xhtml)

[Functional Programming in JavaScript](#part0018.xhtml)

[Short-circuit Evaluation](#part0019.xhtml)

[About the Author](#part0020.xhtml)

# Notes on the Book

This book was written using ChatGPT as an aid tool in the development of this material. All content produced by this tool was carefully reviewed and properly organized by the author. It is important to note that the use of intelligent tools for text creation is welcome, as long as the quality, truthfulness, and correctness of what was produced are always observed.

# A brief history of JavaScript

JavaScript is a high-level programming language that was created in 1995 by Brendan Eich, then an engineer at Netscape. The initial idea was to create a programming language that could be executed in the browser and allow developers to add interactivity and dynamism to web pages.

The first version of JavaScript was released along with the Netscape Navigator 2.0 browser in September 1995\. The language was quickly adopted by other browsers, such as Microsoft's Internet Explorer, and became one of the main technologies used in creating dynamic web pages.

Over the years, JavaScript has evolved and become an increasingly powerful language capable of performing complex tasks both in the browser and on the server. In 2009, Ryan Dahl created Node.js, a platform that allows developers to run JavaScript code on the server, opening up a host of new possibilities for the language.

Currently, JavaScript is one of the most popular programming languages in the world, widely used in web applications, mobile apps, games, and other areas. The language continues to evolve, with new features and functionalities being regularly added to its specifications.

# Preparing the Programming Setup

Installing Node.js

To install Node.js, first go to the website https://nodejs.org/ and download the LTS (Long Time Support) version.

The image below shows a screenshot of the Node.js page, and the arrow indicates the option to be selected to download the LTS version.

After downloading, the installation process of Node.js is very similar to any other application, without any major mysteries (:

![](image_rsrcJK.jpg)

Installing Visual Studio Code

As a source code editor, I suggest Visual Studio Code (VS Code) because it is cross-platform, free, and extensible.

To download this editor, go to https://code.visualstudio.com/ and click on the button as indicated in the figure below.

Like Node.js, the installation process of VS Code does not require any knowledge beyond the conventional to install the new program on your computer.

![](image_rsrcJM.jpg)

# Modules in JavaScript

In Node.js, modules are files that contain JavaScript code that can be reused in different parts of a program. Each module is an independent unit of code that can be imported or exported to other parts of the program, making the code more modular and easy to maintain.

Modules in Node.js are organized in a CommonJS module system, which defines how modules can be defined, loaded, and exported. Each module has its own scope, meaning the variables and functions defined in a module are not visible outside of it unless they are explicitly exported.

To use a module in a Node.js program, it is necessary to import it using the require() function. For example, to use the fs module, which is used to perform file read and write operations, simply use the following code:

![](image_rsrcJN.jpg)

The require() function is a synchronous function that loads the specified module and returns the object exported by it. It is possible to export values from a module using the module.exports variable, which is a special property of the module object. For example, to export a function in a module, simply do the following:

![](image_rsrcJP.jpg)

To import the sayHello() function in another file, just use the require() and access the sayHello property of the imported object:

![](image_rsrcJR.jpg)

This way, modules in Node.js allow developers to organize and reuse code more efficiently, making it easier to maintain and develop more complex applications.

# NPM e NPX

The Node.js package manager is NPM (Node Package Manager), which is used to install, manage, and share software packages and modules written in JavaScript. It comes included with Node.js and is used by developers around the world to manage their project dependencies.

NPM allows you to install packages globally or locally to a specific project. To install a package locally, simply navigate to the root directory of your project and run the following command in the terminal:

![](image_rsrcJS.jpg)

This will install the package in the node_modules directory of your project and add an entry in the package.json file to track your project's dependencies.

On the other hand, npx is a utility that was introduced in NPM from version 5.2.0\. It allows you to run packages directly without having to install them globally on your system or locally in the project.

npx downloads the requested package and runs it immediately, instead of installing it permanently in your system or project. This is useful when you need to run a package only once or when you want to test a package without installing it permanently.

For example, if you want to run a script in the create-react-app package using npx, simply type the following command:

![](image_rsrcJT.jpg)

This will download and execute the create-react-app package with the argument my-app, creating a new React application in the my-app directory.

In summary, NPM is used to manage the dependencies of your project, while npx is used to execute packages without installing them globally or locally. Both are useful tools for JavaScript development.

# First Steps in JavaScript

First, create a folder to develop your Node.js project and then launch VS Code. In the editor, click on File > Open Folder and open the folder you just created. In the example, the folder I created is called ProjetoNode.

On the left, click New File and then name it helloworld.js. In this file, add the following code:

console.log("Hello World")

Then, click Terminal > New Terminal to open a new terminal instance within VS Code, and enter the following command:

node helloworld.js

If everything goes well, the following sentence will appear in the terminal: Hello World.

# Advantages of Node.js

One of the major advantages of Node.js is the ease of developing server-side applications. To see this in action, create a new file in VS Code called server.js and insert the following code lines:

![](image_rsrcJU.jpg)

So, in the terminal, run the following command:

node server.js

You are now running an HTTP server in Node.js that will listen for requests on port 8080\. To access the local server, simply go to the following link http://localhost:8080 in your browser.

# Storing Values in JavaScript

In JavaScript, variables are used to store values that can be used in different parts of a program. To declare a variable in JavaScript, you can use the keywords var, let, or const, followed by the variable name:

![](image_rsrcJV.jpg)

The var keyword was the old way of declaring variables in JavaScript, but it is still supported in newer versions of the language. Variables declared with var have function or global scope.

The let keyword is used to declare variables with block scope, which means they can only be accessed within the block they were declared in.

The const keyword is used to declare constants, which are values that cannot be changed after they are assigned.

It is important to remember that in JavaScript, variables are dynamically typed, which means you do not need to declare the variable type beforehand. The variable type is automatically defined during program execution, based on the value assigned to the variable.

# Data Types in JavaScript

In JavaScript, there are six primitive data types:

number: represents numbers, including integers and floating point numbers. For example, 10, 3.14, -5.

string: represents a sequence of characters. It can be delimited by single or double quotes. For example, "Hello, world!", 'JavaScript'.

boolean: represents a logical value true or false.

null: represents a null value, i.e., absence of value.

undefined: represents a variable that has been declared but not yet assigned a value.

symbol: represents a unique and immutable value that can be used as an identifier for object properties.

In addition to these six primitive types, in JavaScript, there are also two complex data types:

object: represents a collection of key-value pairs. Objects in JavaScript can contain properties and methods. For example, { name: 'John', age: 25 }.

function: is a special type of object that can be called and can have properties and methods associated with it. Functions in JavaScript are used to define blocks of code that can be called anywhere in the program.

It is important to remember that in JavaScript, variables are dynamically typed, which means that the type of the variable is automatically defined during program execution, based on the value assigned to the variable. Additionally, variables can change type during program execution. For example, a variable that contains a number can be later assigned with a string.

# Mathematics in JavaScript

JavaScript supports a wide variety of mathematical operations, including basic arithmetic operations such as addition, subtraction, multiplication, and division. Additionally, it is also possible to perform more complex operations such as trigonometric, exponential, and logarithmic calculations.

Here are some examples of mathematical operations in JavaScript:

![](image_rsrcJW.jpg)

In addition, JavaScript also provides a variety of predefined mathematical functions in the Math object. These functions include, among others, Math.floor() for rounding down, Math.ceil() for rounding up, and Math.random() for generating a random number between 0 and 1.

![](image_rsrcJX.jpg)

These are just a few examples of the many mathematical operations that can be performed in JavaScript.

# Strings in JavaScript

In JavaScript, a string is a sequence of characters, such as "Hello, world!". Strings are one of the primitive data types in JavaScript and are created using single or double quotes.

Here's an example of a string in JavaScript:

![](image_rsrcJY.jpg)

Representation of Strings

In JavaScript, there are two main ways to represent strings: with double quotes and with single quotes. Both forms are equivalent and you can choose which one to use according to your personal preferences or the conventions adopted by the project or team.

For example, the following lines of code create a string with double quotes and a string with single quotes:

![](image_rsrcJZ.jpg)

Additionally, you can use the escape character \ to insert special characters into a string, such as single or double quotes, backslashes, new lines, and others. For example:

![](image_rsrcK0.jpg)

Another way to represent strings in JavaScript is by using the backtick (`), which is known as a template string. Template strings allow for the incorporation of JavaScript expressions in a string using the syntax ${expression}. For example:

![](image_rsrcK1.jpg)

In this case, the variable fullName contains the string "John Sullivan", which is composed by concatenating the variables firstName and lastName using the template string syntax.

In summary, in JavaScript, you can represent strings with single quotes, double quotes or template strings, and you can use the escape character to insert special characters in a string.

Operations with Strings

In JavaScript, it is possible to perform several operations on strings. Some of these operations include:

Concatenation: the operation of joining two or more strings into a single string. This is done using the addition operator (+) or the concat() method. Here is an example:

![](image_rsrcK2.jpg)

Length: the operation of counting the number of characters in a string. This is done using the length property. Here is an example:

![](image_rsrcK3.jpg)

Access to individual characters: it is possible to access individual characters in a string using brackets ([]). Here is an example:

![](image_rsrcK4.jpg)

Character substitution: it is possible to substitute characters in a string using the replace() method. Here is an example:

![](image_rsrcK5.jpg)

These are just a few of the operations that can be performed on strings in JavaScript. There are many others, including string comparison, conversion to uppercase and lowercase letters, and much more.

# Control Structures

Conditional - IF/Else

"If/else" is one of the most commonly used control structures in JavaScript. It is used to execute different blocks of code based on a condition.

The basic syntax of "if/else" is as follows:

![](image_rsrcK6.jpg)

The condition is an expression that returns a boolean value (true or false). If the condition is true, the code block inside the first set of curly braces will be executed. If the condition is false, the code block inside the second set of curly braces will be executed.

Additionally, it is possible to chain multiple "if/else" structures using the "else if" keyword. Here is an example:

![](image_rsrcK7.jpg)

In this case, the first condition to be evaluated is "condition1". If it is true, the first code block will be executed and the rest will be ignored. Otherwise, "condition2" will be evaluated and so on.

"If/else" is a very useful control structure in JavaScript, allowing you to create complex logic in your programs.

Inline Conditional - IF/Else Inline

The inline "if" in JavaScript is a way to write a conditional statement in a single line of code. Instead of using the conventional syntax of an "if" block with curly braces and an optional "else" statement, you can use the ternary operator to create a more compact statement.

The basic syntax of the inline "if" is as follows:

![](image_rsrcK8.jpg)

In this example, the "condition" is evaluated first. If it is true, the "true expression" is returned. Otherwise, the "false expression" is returned.

Here's a practical example:

![](image_rsrcK9.jpg)

In this example, the condition evaluates if the age is greater than or equal to 18\. If it's true, the variable status is set to "adult". Otherwise, the variable status is set to "minor".

The inline "if" is a convenient and readable way to write simple conditional statements in JavaScript, especially when you need more concise code. However, for more complex statements or multiple conditions, using the conventional "if" syntax may be more appropriate.

Looping Structures

The looping structures in JavaScript allow a block of code to be executed multiple times based on a certain condition. The two main looping structures are "while" and "for".

While is a looping structure that executes a block of code while a specific condition is true. The basic syntax of "while" is as follows:

![](image_rsrcKA.jpg)

In this example, the block of code will be executed while the condition is true. The condition is checked at the beginning of each loop iteration.

On the other hand, for is another looping structure that executes a block of code several times based on a fixed number of iterations. The basic syntax of "for" is as follows:

![](image_rsrcKB.jpg)

In this example, the initialization is executed before the first loop iteration. The condition is checked before each loop iteration and, if it is true, the block of code is executed. After each loop iteration, the final expression is executed.

In addition, JavaScript also has the do/while structure, which is similar to "while", but checks the condition at the end of each loop iteration instead of at the beginning. The basic syntax of "do/while" is as follows:

![](image_rsrcKC.jpg)

Finally, JavaScript has the break statement, which allows you to exit a loop prematurely, and the continue statement, which allows you to skip to the next iteration of the loop. These statements are useful for controlling the flow of execution within the loop.

# Functions

In JavaScript, functions are first-class objects, which means they can be treated like any other object. Functions can be stored in variables, passed as arguments to other functions, returned as values from other functions, and more. Here is a simple example of how to create a function in JavaScript:

![](image_rsrcKD.jpg)

In this example, the function "sum" takes two arguments, a and b, and returns their sum.

It is also possible to create anonymous functions in JavaScript, which are nameless functions that are stored in variables or passed as arguments to other functions. Here is an example:

![](image_rsrcKE.jpg)

In this example, the anonymous function is stored in a variable called "sum".

Functions in JavaScript can also be defined using arrow function expressions. Arrow functions were introduced in ECMAScript 6 and are a more concise way to create functions in JavaScript. Here is an example:

![](image_rsrcKF.jpg)

In this example, the arrow function takes two arguments, a and b, and returns their sum.

Functions in JavaScript can also have default arguments, which are used when no value is provided for that argument. Here is an example:

![](image_rsrcKG.jpg)

# Arrays in JavaScript

In JavaScript, an array is a collection of values that can be accessed through a numeric index. Arrays are one of the primitive data types in JavaScript and can contain any type of data, including other arrays.

Here is an example of how to create an array in JavaScript:

![](image_rsrcKH.jpg)

In this example, numbers is an array of numbers that contains the values 1, 2, 3, 4, and 5\. The elements of an array can be accessed using brackets ([]). The index of the first element of an array is 0\. Here is an example:

![](image_rsrcKJ.jpg)

Arrays in JavaScript also have several methods that can be used to perform operations on their elements. Here are some examples:

push():adds one or more elements to the end of the array. Here's an example:

![](image_rsrcKK.jpg)

pop(): removes the last element of the array and returns that element. Here's an example:

![](image_rsrcKM.jpg)

slice(): returns a copy of a portion of the array. Here's an example:

![](image_rsrcKN.jpg)

join(): returns all elements of an array in a single string

![](image_rsrcKP.jpg)

These are just a few examples of the methods available in arrays in JavaScript. There are many others, including shift(), unshift(), splice(), concat(), reverse(), sort(), among others.

Multidimensional Arrays

A multidimensional array in JavaScript is an array that contains other arrays. It is a way to store data in multiple dimensions, allowing you to create complex data structures.

To create a multidimensional array, you need to create an array inside another array. For example, to create a 2x3 array (two rows and three columns), you can use the following syntax:

![](image_rsrcKR.jpg)

In this example, matrix is a multidimensional array that contains two nested arrays, each with three values.

You can access the values of a multidimensional array using the same syntax you would use to access values in a one-dimensional array, but specifying the index for each dimension. For example, to access the value 5 in the array matrix, you can use the following line of code:

![](image_rsrcKS.jpg)

In this case, matrix[1] returns the second nested array, and matrix[1][1] returns the second value in the second nested array, which is 5.

You can also create multidimensional arrays with more than two dimensions by simply nesting more arrays inside the array. However, arrays with more than two or three dimensions can become difficult to work with and are generally avoided in JavaScript programming.

# Objects in JavaScript

In JavaScript, an object is a collection of key-value pairs. Each key is a string that identifies a value in the object. The value can be any type of JavaScript data, including other objects.

To create an object in JavaScript, we can use the object literal syntax, which consists of curly braces {} with key-value pairs separated by commas:

![](image_rsrcKT.jpg)

In this example, person is an object that has three properties: name, age, and address. The address property is another object with its own properties. We can access the properties of an object using either dot notation or bracket notation:

![](image_rsrcKU.jpg)

We can also add, modify, and delete properties of an object using dot or bracket notation:

![](image_rsrcKV.jpg)

In addition, we can loop through the properties of an object using a for...in loop:

![](image_rsrcKW.jpg)

This loop will display all properties and their values in the person object.

In summary, objects are a fundamental part of JavaScript and are widely used in programming to represent complex and structured data.

# Functional Programming in JavaScript

ForEach

The forEach function is one of the most useful functions for iterating through arrays in JavaScript. The forEach function executes a callback function for each element in the array, but it doesn't return a new array. Instead, it simply iterates through the array and executes the function on each element.

Here is a simple example:

![](image_rsrcKX.jpg)

This code displays each element of the numbers array in the console.

The callback function that is passed to forEach receives three arguments: the current element, the index of the element, and the array itself. For example:

![](image_rsrcKY.jpg)

This code displays each element of the array, the index of the element, and the array itself in the console.

The forEach function is useful for performing an action on each element of an array. However, if you need to create a new array from the original array, it's better to use the map, filter, or reduce functions.

Map

The map function is used to create a new array with the result of applying a function to each element of the original array. The map function does not modify the original array, but returns a new array with the same number of elements.

Here's a simple example:

![](image_rsrcKZ.jpg)

In this example, the map function is used to create a new array square that contains the square of each number in the numeros array.

The map function takes a callback function as an argument. This function is called for each element of the array and should return the value to be added to the new array. The callback function can have up to three arguments: the current element, the index of the element, and the array itself. For example:

![](image_rsrcM0.jpg)

In this example, the map function is used to create a new array upperFruits that contains all the fruits from the fruits array in uppercase letters. The callback function prints each fruit and its index before transforming the fruit into uppercase and returning it.

The map function is one of the most useful and powerful functions in JavaScript, and is widely used in functional programming to transform data.

Filter

The filter function is used to create a new array with all elements of the original array that pass a test specified by a callback function. The new array will only contain elements that satisfy the condition specified in the callback function.

Here's a simple example:

![](image_rsrcM1.jpg)

In this example, the filter function is used to create a new array evenNumbers that contains only the even numbers from the numbers array.

The filter function takes a callback function as an argument. This function is called for each element in the array and should return a boolean value that indicates whether the element should be included in the new array. The callback function can have up to three arguments: the current element, the index of the element, and the array itself. For example:

![](image_rsrcM2.jpg)

In this example, the filter function is used to create a new array fruitsWithE that contains only the fruits from the fruits array that contain the letter "e". The callback function prints each fruit and its index before testing whether the fruit contains the letter "e" and returning a boolean value.

The filter function is one of the most useful and powerful functions in JavaScript and is widely used in functional programming to filter data.

Reduce

The reduce function is used to reduce all the elements of an array to a single value. It executes a callback function for each element of the array, passing an accumulator and the current element as arguments, and returns an accumulated value that results from the execution of the callback function on each element.

Here's a simple example:

![](image_rsrcM3.jpg)

In this example, the reduce function is used to sum all the numbers in the numbers array. The callback function takes two arguments: the accumulator and the current element. In the first iteration, the accumulator is the initial value passed as the second argument (zero) and the current element is the first element of the array (1). In the second iteration, the accumulator is the sum of the initial value and the first element (1+2=3) and the current element is the second element of the array (2), and so on. The final result is the sum of all the elements in the array.

The reduce function can also take an optional third argument, which is the initial value of the accumulator. If this argument is not provided, the first element of the array will be used as the initial value.

![](image_rsrcM4.jpg)

In this example, the reduce function is used to calculate the product of all the numbers in the numbers array. Since no initial value is provided, the first element of the array (1) is used as the initial value of the accumulator.

The reduce function is one of the most powerful and flexible functions in JavaScript, and it is widely used in functional programming to transform data and perform complex operations on arrays.

# Short-circuit Evaluation

Short-circuit evaluation is a technique in JavaScript (and other programming languages) that allows for evaluating a logical expression by stopping as soon as the result can be determined, without the need to evaluate the entire expression. This is possible because the logical operators AND (&&) and OR (||) are implemented this way in JavaScript.

The logical operator AND returns true only if both expressions are true. If the first expression is false, the result is false and the second expression is not evaluated. For example:

![](image_rsrcM5.jpg)

In this case, the second expression is not evaluated if the first expression is false (if x is not greater than 0).

The logical operator OR returns true if at least one of the expressions is true. If the first expression is true, the result is true and the second expression is not evaluated. For example:

![](image_rsrcM6.jpg)

In this case, the second expression is not evaluated because the first expression (y) is false (null).

The short-circuit evaluation technique can be useful for improving code performance and making it more readable in certain situations. However, it is important to use it with care and ensure that the program logic is correct.

Short-circuit Evaluation em Funções

Short-circuit evaluation can also be used with functions in JavaScript. In some cases, it is possible to use this technique to improve code performance or avoid errors.

For example, imagine you have a function that receives an object as a parameter and needs to check if a certain property exists in the object before accessing it. You could write the following code:

![](image_rsrcM7.jpg)

In this case, the logical expression object && object.property uses short-circuit evaluation to ensure that the code inside the if statement is only executed if the object exists and the property also exists.

Another example where short-circuit evaluation can be useful is when you need to set a default value for a variable or function parameter. Instead of using an if/else statement to check if the variable or parameter is undefined, you can use the logical OR operator to set a default value:

![](image_rsrcM8.jpg)

In this case, if the value of options.defaultValue is undefined, the default value will be used instead.

# About the Author

Ruhan Conceição graduated in Computer Engineering (2015) from the Federal University of Pelotas and has a Master's degree in Computing (2016) from the same university. Since 2018, he has been a professor at the Federal Institute of Education, Science and Technology of Rio Grande do Sul in the field of Informatics, where he teaches, among other subjects, Object Oriented Programming, Visual Programming, and Mobile Devices Programming.

In 2014, while still an undergraduate student, Ruhan received the title of Gaúcho Researcher in the Young Innovator category due to his academic and scientific trajectory during his years at the university. His research topic has always been related to the algorithmic development of efficient solutions for real-time video coding. Regarding scientific research, Ruhan has accumulated dozens of papers published in national and international conferences, as well as articles in highly relevant scientific journals, and two computer programs registered in the National Institute of Intellectual Property.

Among his hobbies, Ruhan Conceição has a podcast called R-Cast (@rcasttv on social media), where he invites guests to talk about various topics, including technology, politics, education, health, culture, music, etc.