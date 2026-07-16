![](image_rsrc1AR.jpg)

# Introduction

## Welcome to the course!

Welcome to your JavaScript course! In this book you will learn everything you need to get started with JavaScript. JavaScript is a versatile and widely used programming language that is mainly used to create interactive websites. Whether you are a complete beginner or already have some programming experience, this book will help you build a solid foundation in JavaScript.

## Note for participants

Before we get started, here are a few tips to help you get started:

• Practice makes perfect: programming is a practical skill. The more you practise, the better you get.
• Mistakes are normal: everyone makes mistakes, especially at the beginning. They are an important part of the learning process. Learn from them and don't give up!
• Ask questions: If you don't understand something, look for answers. Use online resources, forums and communities to find support.
• Stay curious: JavaScript offers endless possibilities. Explore and experiment to constantly expand your skills.

## What will you learn in this course?

In this course you will learn the basics of JavaScript step by step. We will start with the basic concepts and work our way up to more advanced topics. Here is an overview of the topics that await you:

1\. Preparation: Installation and setup of the required software.
2\. The basics of JavaScript: Introduction and your first JavaScript program.
3\. Variables: Dealing with variables and data types.
4\. Operators: Mathematical and logical operations.
5\. Control structures: conditions and loops.
6\. Functions: Definition and use of functions.
7\. Objects: Working with objects and their methods.
8\. Arrays: Basics and advanced functions of arrays.
9\. DOM: Manipulation of the Document Object Model.
10. Events and event handling: Working with user input and events.
11. Asynchronous programming: Introduction to Promises and async/await.
12. Error handling and debugging: Dealing with errors in the code.
13. JavaScript libraries and frameworks: overview of popular tools.
14. Project work: Creation of a simple web application.
15. Further resources: Tips and resources for further learning.

This book is structured so that you can go back and revisit a topic at any time. Each section builds on the previous one, so make sure you understand the basics before moving on.

# Preparation

## Installing and setting up the code editor (Visual Studio Code)

Before you can start programming in JavaScript, you need a code editor. We recommend Visual Studio Code (VS Code) as it is powerful, free and very user-friendly. Here are the steps to install and set it up:

1\. Download and installation:
o Visit the Visual Studio Code website.
o Download the version for your operating system (Windows, macOS or Linux). o Follow the installation instructions.

2\. First installation:
o Start Visual Studio Code after the installation.
o Set up your preferred color scheme (light or dark).
o Install important extensions:

▪ ESLint: For checking your code for errors.
▪ Prettier: For the automatic formatting of your code.
▪ JavaScript (ES6) code snippets: For helpful code snippets.

3\. Create a new project:
o Open Visual Studio Code.
o Click on "File" > "Open" and create a new folder for your project. o Create a new file with the extension .js (e.g. index.js).

## Installation of the browser (Google Chrome)

A web browser is necessary to test your JavaScript programs. We recommend Google Chrome as it offers powerful developer tools that can help you with debugging and testing.

1\. Download and installation:
o Visit the Google Chrome website.
o Download and install the version for your operating system.

2\. Developer tools:
o Open Google Chrome.
o Press F12 or Ctrl + Shift + I (Windows/Linux) orCmd + Option + I

(macOS) to open the developer tools.
o Use the "Console" tab to execute and test JavaScript code directly in the
browser.

With these preparations, you are now ready to dive into the world of JavaScript. In the next chapter, we will look at the basics of JavaScript and write our first small program.

# Basics of JavaScript

## Introduction to JavaScript

JavaScript is one of the three core technologies of the World Wide Web, alongside HTML and CSS. While HTML is responsible for the structure and CSS for the design, JavaScript enables the interactivity of websites. It is supported in almost every modern web browser and is one of the most widely used programming languages in the world.

### Why JavaScript?

• Easy to learn: JavaScript is a beginner-friendly language.
• Widely used: There is a large community and many resources.
• Flexible: JavaScript can be used for both simple scripts and complex web applications.
• Interactive: Enables dynamic content and user interaction.

## Your first JavaScript program: Hello world!

Before we go into depth, we'll write a simple "Hello world!" program that will show you how to use JavaScript in an HTML file.
1\. Create an HTML file: Create a new file and name it index.html. Add the following HTML code:

<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initialscale=1.0">
<title>Hello world</title>
</head>
<body>
<h1>Hello world!
<script src="script.js"></script>
</body>
</html>

2\. Create a JavaScript file: Create a new file and name it script.js. Add the following JavaScript code:
alert('Hello world!');
3\. Run your program: Open the index.html file in your web browser. You should see a pop-up window that says "Hello world!".

## Final preparations, then off we go!

Before we dive into the deeper aspects of JavaScript, make sure you have understood and set up the following points:

1\. Directory structure: You should have a clear directory structure, e.g. a folder for your project with HTML, CSS and JavaScript files.
2\. Code editor: Make sure that your code editor (e.g. VS Code) is set up correctly and that you feel comfortable with it.
3\. Browser developer tools: Familiarize yourself with your browser's developer tools. These will help you to debug and test your code.

You have now laid the foundations for working with JavaScript. In the next chapter, we will look at variables, one of the fundamental concepts of every programming language.

# Variables

## Variables in JavaScript

Variables are storage locations in which you can save data that is used by your program. They are a fundamental component of every programming language. In JavaScript, you can declare variables with the keywords var, let and const.

### Example

let name = 'Max'; const pi = 3.14; var age = 25;

• let and const were introduced with ES6 and are more modern methods for declaring variables.
• var is older and has some differences in terms of scope.

## Naming of variables

Variables must be named according to certain rules:

• They may only contain letters, numbers, underscores and dollar signs.
• They must not begin with a number.
• They must not be reserved words (such as let, const, var, function, etc.).

### Example

let myName = 'Sarah'; let _age = 30;
let $currency = 'USD';

## Primitive data types - strings, numbers and booleans

There are various data types in JavaScript that you can save in variables. The most important primitive data types are

• Strings: Character strings that represent text.
• Numbers: Numbers, both whole numbers and floating point numbers.
• Booleans: Truth values that can be either true orfalse.

### Example

let firstName = 'John'; // String let age = 25; // Number
let isStudent = true; // Boolean

## Changing the values of variables

Once declared, variables can be changed later in JavaScript (except const).

### Example

let city = 'Berlin';
city = 'Hamburg'; // Value of the city variable is changed

## let vs. const

• let: Is used to declare changeable variables.
• const: Is used to declare unchangeable variables. The value can no longer be changed after initialization.

### Example

let age = 25;
age = 26; // This is allowed
const birthYear = 1995;
birthYear = 1996; // This will cause an error

## User input with prompt()

You can ask the user for input using the prompt() function.

### Example

let userName = prompt('What is your name?'); console.log('Hello, ' + userName + '!');

## Comments

Comments are useful for documenting the code and making it easier to understand. There are single-line and multi-line comments.

### Single-line comments

// This is a one-line comment

### Multiline comments

/*
This is a
multiline comment */

That's the basics of variables in JavaScript. In the next chapter, we will look at errors and how to search for answers and ask questions when you encounter problems.

# Excursus: Errors

## Looking for answers and asking questions

Errors are an inevitable part of programming, especially when learning a new language. The most important thing is how you deal with them and learn to fix them. Here are some tips and resources that can help you when you encounter bugs.

### Common error types

1\. Syntax errors: These occur when the code does not comply with the rules of the language.
o Example: let x = ; (missing value)

2\. Runtime errors: These occur when the code is executed but a problem occurs. o Example: Access to an undefined variable.
3\. Logic errors: These occur when the code is executed without errors but does not deliver the desired result.
o Example: Incorrect calculation due to an incorrect operator.

### Troubleshooting

1\. Read error messages: The error messages in the console often provide information about the problem and where it is occurring.
2\. Check the code step by step: Divide your code into small sections and check each step.
3\. Use the console: Useconsole.log() to check values and variables. o Example: console.log('The value of x is: ', x);

### Use online resources

There are many online resources that can help you find answers to your questions:
1\. Stack Overflow: One of the largest communities for programmers. Here you can ask questions and get answers from experienced developers.
o Stack Overflow 2\. Mozilla Developer Network (MDN): An excellent resource for documentation and examples of JavaScript.
o MDN Web Docs 3\. W3Schools: Another useful website for tutorials and references.
o W3Schools JavaScript Tutorial

### Ask questions

When you ask questions online, make sure that you formulate them clearly and precisely. Here are some tips on how to ask good questions:

1\. Describe the problem: Explain exactly what you want to achieve and what is not working.
2\. Code examples: Insert relevant code sections that show the problem.
3\. Error messages: Copy and paste the exact error message you receive.
4\. Previous attempts: Describe what you have already tried to solve the problem.

### Example of a good question

markdown

### Problem:
I am trying to write a simple JavaScript function that adds two numbers, but I get an error message.

### Code:
```javascript
function addNumbers(a, b) {

return a + b;
}
let result = addNumbers(5, '10'); console.log(result);

### Error message:

Uncaught TypeError: Cannot add property 'toString' of undefined

### What I have tried so far:

I have tried to convert both arguments to numbers, but the error persists.
yaml
--

Errors are part of programming and are a valuable learning opportunity. In the next chapter, we will look at operators, another important concept in JavaScript.

--

# Operators

## Mathematical operators

Mathematical operators are used to perform basic arithmetic operations. Here are the most important operators:

• + (addition): Adds two numbers together.
• - (subtraction): Subtracts one number from another.
• * (multiplication): Multiplies two numbers.
• / (division): Divides one number by another.
• % (modulus): Returns the remainder of a division.
• ** (exponentiation): Raises a number to a power.

### Example

let a = 10; let b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333333333333335 console.log(a % b); // 1
console.log(a ** b); // 1000

## Concatenation and multi-line strings

The concatenation (concatenation) of strings is also carried out with the+ operator.

### Example

let firstName = 'John';
let lastName = 'Doe';
let fullName = firstName + ' ' + lastName;

console.log(fullName); // John Doe

### Multiline strings

Multi-line strings can be created with backticks (`).

### Example

let message = `This is a multiline
String `;

console.log(message);

## Template strings and multi-line template strings

Template strings allow you to insert variables and expressions into strings by using ${}.

### Example

let name = 'Alice';
let greeting = `Hello, ${name}! console.log(greeting); // Hello, Alice!

## Comparison operators for numbers

Comparison operators are used to compare two values. They return a Boolean value (true or false).

• == (equal): Checks for equality.
• != (unequal): Checks for inequality.
• === (strictly equal): Checks for equality and equality of type.
• !== (strictly unequal): Checks for inequality and type inequality.
• > (greater than): Checks whether the left-hand value is greater than the right-hand value.
• < (less than): Checks whether the left-hand value is smaller than the right-hand value.
• >= (greater than or equal to): Checks whether the left-hand value is greater than or equal to the right-hand value.
• <= (less than or equal to): Checks whether the left-hand value is less than or equal to the right-hand value.

### Example

let x = 5; let y = 10;

console.log(x == y); // false console.log(x != y); // true console.log(x === y); // false console.log(x !== y); // true console.log(x > y); // false console.log(x < y); // true console.log(x >= y); // false console.log(x <= y); // true

## Comparison operators for strings

Comparison operators can also be applied to strings. The comparisons are based on the lexicographical (alphabetical) order.

### Example

let str1 = 'apple'; let str2 = 'banana';

console.log(str1 == str2); // false
console.log(str1 != str2); // true
console.log(str1 < str2); // true (apple comes before banana) console.log(str1 > str2); // false

## Type safety in JavaScript

JavaScript is a dynamically typed language, which means that the type of a variable is determined at runtime. It is therefore important to understand the difference between == and ===.

• == only checks for equality of values.
• === Checks both the equality of the values and the types.

### Example

let num = 5; let str = '5';
console.log(num == str); // true (only values are compared) console.log(num === str); // false (values and types are compared)

## Logical operators

Logical operators are used to combine Booleans and evaluate logical expressions.

• && (AND): Returns true if both operands aretrue.
• || (OR): Returns true if one of the operands is true.
• ! (NOT): Returns the opposite of the value.

### Example

let a = true; let b = false;

console.log(a && b); // false console.log(a || b); // true console.log(!a); // false console.log(!b); // true

Those were the basic operators in JavaScript. In the next chapter, we will look at control structures that allow you to create conditional statements in your code.

# Control structures I

## if statements

Theif statement is used to check a condition and only execute code if this condition is true.

### Syntax

if (condition) {
// Code that is executed if the condition is true
}

### Example

let age = 18;

if (age >= 18) {
console.log('You are of legal age.');
}

In this example, the message "You are of legal age." is only displayed if theage variable is greater than or equal to 18.

## if-else statements

With an if-else statement, you can execute code if the condition is true and other code if the condition is false.

### Syntax

if (condition) {
// Code that is executed if the condition is true
} else {
// Code that is executed if the condition is false
}

### Example

let age = 16;

if (age >= 18) {
console.log('You are of legal age.');
} else {
console.log('You are a minor.');
}

Here "You are underage." is displayed becauseage is less than 18.

## else-if statements

Theelse-if statement makes it possible to check multiple conditions. If the first condition is false, the next condition is checked, and so on.

### Syntax

if (condition1) {
// Code that is executed if condition1 is true
} else if (condition2) {
// Code that is executed if condition2 is true
} else {
// Code that is executed if none of the conditions is true
}

### Example

let score = 85;

if (score >= 90) {
console.log('Note: A');
} else if (score >= 80) { console.log('Note: B');
} else if (score >= 70) { console.log('Note: C');
} else {
console.log('Note: F');
}

In this example, "Score: B" is displayed because thescore is between 80 and 89.

## Nested if statements

You can nest if statements within otherif statements to check more complex conditions.

### Example

let age = 20;
let hasID = true;
if (age >= 18) {
if (hasID) {
console.log('You may enter.');

} else {
console.log('You need an ID card.');
}
} else {
console.log('You are too young.'); }

In this example, "You may enter." is displayed becauseage is greater than or equal to 18 and hasID is true.
That's the basics of control structures in JavaScript. In the next chapter, we will look at functions that allow you to write and organize reusable code.

# Functions

## Basics of functions

Functions are reusable blocks of code that perform a specific task. They help to keep the code modular and readable. There are various ways to define functions in JavaScript.

### Syntax

function name(parameters) { // Code that is executed
}

### Example

function greet() {
console.log('Hello, world!');
}

greet(); // Call the function

## Functions with parameters

Functions can have parameters that serve as input for the function.

### Syntax

function name(parameter1, parameter2) { // Code that is executed
}

### Example

function greet(name) {
console.log('Hello, ' + name + '!');
}

greet('Max'); // Output: Hello, Max!

## Functions with default parameters

Default parameters make it possible to define default values for parameters that are used if no arguments are passed.

### Syntax

function name(parameter1 = defaultValue1, parameter2 = defaultValue2) { // Code that is executed
}

### Example

function greet(name = 'World') { console.log('Hello, ' + name + '!');
}

greet(); // Output: Hello, world! greet('Max'); // Output: Hello, Max!

## The return statement

A function can return a value with the return statement.

### Syntax

function name(parameters) { // Code
return value;

}

### Example

function add(a, b) { return a + b;
}

let sum = add(5, 3);
console.log(sum); // Output: 8

## Areas of validity

The scope of variables determines where these variables are accessible. There are two main types of scopes: global and local.

### Global scope of validity

Variables that are declared outside a function have a global scope and are accessible everywhere in the code.

### Local area of validity

Variables that are declared within a function have a local scope of validity and are only accessible within this function.

### Example

let globalVar = 'I am global';

function myFunction() {
let localVar = 'I am local';
console.log(globalVar); // Access to global variable console.log(localVar); // Access to local variable

}
myFunction();
console.log(localVar); // Error: localVar is not defined

## Hoisting

Hoisting is a behavior in JavaScript in which declarations of variables and functions are moved to the beginning of their scope before the code is executed.

### Example

console.log(myVar); // undefined var myVar = 'Hello';
console.log(myFunc()); // Hello, world! function myFunc() {
return 'Hello, world!
}

## Function expressions vs. function declarations (hoisting)

There are two ways to define functions: Function declarations and function expressions. Function declarations are lifted (hoisted), but function expressions are not.

### Function declaration

console.log(greet()); // Hello

function greet() { return 'Hello';
}

### Functional expression

console.log(greet()); // Error: greet is not defined

let greet = function() { return 'Hello';
};

Those were the basics of functions in JavaScript. In the next chapter, we will look at objects that allow you to create more complex data structures.

# Objects

## Basics of objects

Objects are basic building blocks in JavaScript that make it possible to organize related data and functions in a structure. An object consists of properties and methods (functions).

### Syntax

let obj = {
key1: value1,
key2: value2,
// Method
methodName: function() {

// Code
}
};

### Example

let person = {
name: 'Max',
age: 30,
greet: function() {

console.log('Hello, I am ' + this.name); }
};

console.log(person.name); // Max console.log(person.age); // 30 person.greet(); // Hello, I'm Max

## Nested objects

Objects can have other objects as properties.

### Example

let address = {
city: 'Berlin',
postalCode: '12345'

};

let person = {
name: 'Max',
age: 30,
address: address

};
console.log(person.address.city); // Berlin

## Read and set values (dot notation)

You can access and change the properties of an object with the dot notation.

### Example

let person = {
name: 'Max',
age: 30

};

console.log(person.name); // Max
person.age = 31;
console.log(person.age); // 31

## Read and set values (bracket notation)

Alternatively, you can also use the square bracket notation to access properties.

### Example

let person = {
name: 'Max',
age: 30

};

console.log(person['name']); // Max
person['age'] = 31;
console.log(person['age']); // 31

## Add, change and remove properties

You can add, change or remove properties for an object.

### Example

let person = {
name: 'Max',
age: 30

};

// Add
person.gender = 'male';
console.log(person.gender); // male

// Change
person.age = 31;
console.log(person.age); // 31

// Remove
delete person.age;
console.log(person.age); // undefined

## Objects in functions

Objects can be passed as arguments to functions and returned by functions.

### Example

function printPerson(person) {
console.log('Name: ' + person.name + ', Age: ' + person.age);
}

let person = { name: 'Max', age: 30

};
printPerson(person); // Name: Max, Age: 30

## Call-by-value vs. call-by-reference

Primitive data types are transferred by value (call-by-value), while objects are transferred by reference (call-by-reference).

### Example

let x = 10;
let y = x; // Call-by-Value y = 20;
console.log(x); // 10

let person1 = { name: 'Max' };
let person2 = person1; // call-by-reference person2.name = 'Anna';
console.log(person1.name); // Anna

## Objects as return value

Functions can have objects as return values.

### Example

function createPerson(name, age) { return {
name: name,
age: age

};
}
let person = createPerson('Max', 30);
console.log(person); // { name: 'Max', age: 30 }

## Methods

Methods are functions that are defined as properties of an object.

### Example

let person = {
name: 'Max',
age: 30,
greet: function() {

console.log('Hello, I am ' + this.name); }
};
person.greet(); // Hello, I'm Max

## Objects as constants

Objects declared with const can still be changed as long as the reference is not changed.

### Example

const person = {
name: 'Max',
age: 30

};
person.age = 31; // This is allowed
console.log(person.age); // 31
// person = { name: 'Anna' }; // This causes an error

## Compare objects

Objects are compared by reference, not by value.

### Example

let person1 = { name: 'Max' }; let person2 = { name: 'Max' };
console.log(person1 === person2); // false
let person3 = person1;
console.log(person1 === person3); // true
That's the basics of objects in JavaScript. In the next chapter, we will look at other control structures that will make your programs even more powerful.

# Control structures II

## switch statements: Basics

Theswitch statement is another control structure that is used to check multiple conditions. It is a good alternative to long chains of if-else statements.

### Syntax

switch (expression) {
case Value1:
// Code that is executed when expression equals value1
break;

case Value2:
// Code that is executed when expression equals value2
break;

// Further case statements
default:
// Code that is executed if no case applies
}

### Example

let fruit = 'Banana';

switch (fruit) {
case 'Apple':
console.log('It's an apple.'); break;

case 'Banana':
console.log('It's a banana.'); break;

case 'Orange':
console.log('It's an orange.'); break;

default:
console.log('Unknown fruit.'); }
In this example, "It's a banana." is output becausefruit equals banana.

## switch statements: Example

Here is another example that shows how switch statements can be used to check days of the week.

### Example

let day = 3; let dayName;

switch (day) {
case 1:
dayName = 'Monday'; break;

case 2:
dayName = 'Tuesday'; break;

case 3:
dayName = 'Wednesday'; break;

case 4:
dayName = 'Thursday'; break;

case 5:
dayName = 'Friday'; break;

case 6:
dayName = 'Saturday'; break;

case 7:
dayName = 'Sunday'; break;

default:
dayName = 'Invalid day'; }
console.log(dayName); // Wednesday

## switch statements: several cases, one statement

Sometimes you want to handle multiple cases in the same way. You can write several case statements withoutbreak one after the other to execute the same code for different values.

### Example

let grade = 'B'; let message;

switch (grade) {
case 'A':
case 'B':
case 'C':

message = 'Passed';
break;
case 'D':
case 'F':
message = 'Failed';
break;
default:
message = 'Invalid note'; }

console.log(message); // Passed
In this example, grades A, B and C display the same message "Passed".
Those were the advanced control structures in JavaScript. In the next chapter, we'll look at arrays, another important concept that helps you organize and manipulate collections of data.

# Arrays I: The basics

## The basics of arrays

Arrays are data structures that are used to store multiple values in a single variable. Each value in the array has an index, starting at 0.

### Syntax

let arrayName = [element1, element2, element3];

### Example

let fruits = ['apple', 'banana', 'orange']; console.log(fruits[0]); // Apple
console.log(fruits[1]); // Banana
console.log(fruits[2]); // Orange

## Arrays are special objects

In JavaScript, arrays are special types of objects. They have additional methods and properties that have been specially developed for working with lists of values.

### Example

let fruits = ['apple', 'banana', 'orange']; console.log(typeof fruits); // object console.log(fruits.length); // 3

## Multidimensional arrays

Multidimensional arrays are arrays that contain other arrays as elements. This is useful for displaying matrices or tables.

### Example

let matrix = [ [1, 2, 3], [4, 5, 6], [7, 8, 9]

];
console.log(matrix[0][0]); // 1 console.log(matrix[1][2]); // 6

## Arrays and objects

Arrays and objects can be nested inside each other to create more complex data structures.

### Example

let person = {
name: 'Max',
age: 30,
hobbies: ['reading', 'swimming', 'traveling']

};
console.log(person.hobbies[1]); // Swimming

## Adding and removing elements

You can add or remove elements from an array by using different methods.

### push() and pop()

• push(element): Adds an element to the end of the array.
• pop(): Removes the last element of the array and returns it.

### Example

let fruits = ['apple', 'banana'];
fruits.push('Orange');
console.log(fruits); // ['apple', 'banana', 'orange']

let lastFruit = fruits.pop();
console.log(lastFruit); // Orange
console.log(fruits); // ['apple', 'banana']

### unshift() and shift()

• unshift(element): Adds an element to the beginning of the array.
• shift(): Removes the first element of the array and returns it.

### Example

let fruits = ['apple', 'banana'];
fruits.unshift('Orange');
console.log(fruits); // ['Orange', 'Apple', 'Banana']

let firstFruit = fruits.shift();
console.log(firstFruit); // Orange
console.log(fruits); // ['apple', 'banana']

## Search arrays with includes(), indexOf() and lastIndexOf()

• includes(element): Checks if a specific element is present in the array and returns true or false.
• indexOf(element): Returns the first index of an element in the array or -1 if it is not found.
• lastIndexOf(element): Returns the last index of an element in the array or -1 if it is not found.

### Example

let fruits = ['apple', 'banana', 'orange', 'apple'];

console.log(fruits.includes('banana')); // true console.log(fruits.indexOf('apple')); // 0 console.log(fruits.lastIndexOf('apple')); // 3

## Further methods in the documentation

JavaScript offers many other methods for manipulating arrays. It is helpful to consult the documentation to familiarize yourself with all available methods.

### Example

• MDN Array Documentation That's the basics of arrays in JavaScript. In the next chapter, we will look at loops to learn how to iterate through arrays and other data structures.

# Loops

## while loop

Thewhile loop repeats a code block as long as a certain condition is true.

### Syntax

while (condition) {
// Code that is executed
}

### Example

let i = 0;
while (i < 5) {
console.log(i);
i++;
}
// Output: 0, 1, 2, 3, 4

## The keywords continue andbreak

• continue: Ends the current iteration and continues with the next one.
• break: Ends the loop completely.

### Example

for (let i = 0; i < 5; i++) {
if (i === 2) {
continue; // Skips the current loop pass if i is equal to 2

}
console.log(i);
}
// Output: 0, 1, 3, 4

for (let i = 0; i < 5; i++) {
if (i === 2) {
break; // Ends the loop if i is equal to 2

}
console.log(i);
}
// Output: 0, 1

## for loop

Thefor loop is a compact loop structure that is typically used when the number of iterations is known.

### Syntax

for (initialization; condition; increment) { // Code that is executed
}

### Example

for (let i = 0; i < 5; i++) { console.log(i);
}
// Output: 0, 1, 2, 3, 4

## Run through arrays with the for loop

Thefor loop is useful for iterating through arrays.

### Example

let fruits = ['apple', 'banana', 'orange'];

for (let i = 0; i < fruits.length; i++) { console.log(fruits[i]);
}

## Running through multidimensional arrays with the for loop

You can use nested for loops to iterate through multidimensional arrays.

### Example

let matrix = [
[1, 2, 3],
[4, 5, 6],
[7, 8, 9]

];
for (let i = 0; i < matrix.length; i++) {
for (let j = 0; j < matrix[i].length; j++) {
console.log(matrix[i][j]);

}
}
// Output: 1, 2, 3, 4, 5, 6, 7, 8, 9

## Callback functions - Functions as parameters for functions

A callback function is a function that is passed as an argument to another function and is executed after a specific operation has been completed.

### Example

function greet(name, callback) {
console.log('Hello, ' + name + '!');
callback();

}

function sayGoodbye() {
console.log('Goodbye!');
}

greet('Max', sayGoodbye);
// Issue:
// Hello, Max!
// Goodbye!

## Arrays run through with the forEach method

TheforEach method executes a provided function once for each element in the array.

### Example

let fruits = ['apple', 'banana', 'orange'];

fruits.forEach(function(fruit) {
console.log(fruit);
});
// Edition: apple, banana, orange

## Loop through arrays and objects with the for-in and for-of loop

### for-in

Thefor-in loop is used to iterate over the properties of an object.

### Example

let person = {
name: 'Max',
age: 30,
city: 'Berlin'

};

for (let key in person) {
console.log(key + ': ' + person[key]);
}
// Issue:
// name: Max
// age: 30
// city: Berlin

### for-of

Thefor-of loop is used to iterate over iterable objects (such as arrays).

### Example

let fruits = ['apple', 'banana', 'orange'];

for (let fruit of fruits) {
console.log(fruit);
}

## The best way to go through objects

Thefor-in loop is usually suitable for objects, while thefor-of loop or theforEach method are more efficient for arrays.
That's the basics of loops in JavaScript. In the next chapter, we will look at the advanced functionality of arrays in order to perform even more powerful data manipulation.

# Arrays II: Functionality for advanced users

## Filter arrays

Thefilter method creates a new array that contains all elements that fulfill a certain condition. The condition is defined by a callback function.

### Syntax

let neuesArray = array.filter(callback);

### Example

let numbers = [1, 2, 3, 4, 5, 6];
let evenNumbers = numbers.filter(function(number) { return number % 2 === 0;
});
console.log(evenNumbers); // [2, 4, 6]

## Sort arrays

Thesort method sorts the elements of an array in place (i.e. the original array is changed) and returns the sorted array.

### Syntax

array.sort([compareFunction]);

### Example without compareFunction

let fruits = ['banana', 'apple', 'orange']; fruits.sort();
console.log(fruits); // ['apple', 'banana', 'orange']

### Example with compareFunction

let numbers = [4, 2, 5, 1, 3];
numbers.sort(function(a, b) {
return a - b; // For ascending sorting });
console.log(numbers); // [1, 2, 3, 4, 5]

## Maps

A map object saves key-value pairs and remembers the original insertion sequence of the keys.

### Create a map

let map = new Map();

### Adding values

map.set('key1', 'value1'); map.set('key2', 'value2');

### Access to values

console.log(map.get('key1')); // 'value1'

### Remove values

map.delete('key2');

### Iterate over a map

map.forEach(function(value, key) { console.log(key + ' = ' + value);
});
// Issue:
// key1 = value1

## Sets

A set is a collection of values in which each value can only occur once.

### Creating a set

let set = new Set();

### Adding values

set.add(1);
set.add(2);
set.add(1); // Is not added because 1 already exists

### Check whether a value is available

console.log(set.has(1)); // true console.log(set.has(3)); // false

### Removing values

set.delete(2);

### Iterate over a set

set.forEach(function(value) { console.log(value);
});
// Issue:
// 1

## Run through maps and sets

### Iterate over a map

let map = new Map();
map.set('key1', 'value1'); map.set('key2', 'value2');

for (let [key, value] of map) { console.log(key + ' = ' + value);
}
// Issue:
// key1 = value1
// key2 = value2

### Iterate over a set

let set = new Set([1, 2, 3]);

for (let value of set) { console.log(value);
}
// Issue:
// 1
// 2
// 3

These were the advanced functions for arrays in JavaScript. In the next chapter, we will look at time, date, intervals and timeouts.

# Time, date, intervals and timeouts

## The date object

TheDate object in JavaScript is used to create and edit date and time information.

### Creating a new date

let now = new Date();
console.log(now); // Current date and time
let specificDate = new Date('2023-01-01');
console.log(specificDate); // January 1, 2023

## Important methods of the Date object

getFullYear()
Returns the year of the date.
let now = new Date();
console.log(now.getFullYear()); // e.g. 2024 getMonth()
Returns the month of the date (0-11, where 0 is January and 11 is December).
let now = new Date();
console.log(now.getMonth()); // e.g. 6 for July getDate()
Returns the day of the month (1-31).
let now = new Date();
console.log(now.getDate()); // e.g. 5

### getHours(), getMinutes(), getSeconds(), getMilliseconds()

Returns the hour, minute, second or millisecond of the date.

let now = new Date();
console.log(now.getHours()); // e.g. 14
console.log(now.getMinutes()); // e.g. 30
console.log(now.getSeconds()); // e.g. 45
console.log(now.getMilliseconds()); // e.g. 123

getDay()
Returns the day of the week of the date (0-6, where 0 is Sunday and 6 is Saturday).
let now = new Date();
console.log(now.getDay()); // e.g. 3 for Wednesday

## Timeout and intervals

setTimeout()
You can use thesetTimeout function to execute a function after a certain delay in milliseconds.

### Syntax

setTimeout(function, delay);

### Example

function sayHello() {
console.log('Hello, world!');
}

setTimeout(sayHello, 2000); // Executes the function after 2 seconds setInterval()
You can use thesetInterval function to execute a function repeatedly at specific intervals.

### Syntax

setInterval(function, interval);

### Example

function sayHello() {
console.log('Hello, world!');
}

setInterval(sayHello, 2000); // Executes the function every 2 seconds

## clearTimeout() and clearInterval()

UseclearTimeout and clearInterval to stop scheduled timeout and interval operations.

### Example

let timeoutId = setTimeout(function() {
console.log('This text is not displayed.');
}, 2000);

clearTimeout(timeoutId); // Stops the timeout operation

let intervalId = setInterval(function() {
console.log('This text is displayed repeatedly.');
}, 2000);

clearInterval(intervalId); // Stops the interval operation

# Working with strings and numbers

## Working with strings: Basic methods

Strings are text data that can be manipulated in JavaScript in various ways. There are many built-in methods for editing strings.
length
Returns the length of a string.
let text = 'Hello, world!
console.log(text.length); // 12

### toUpperCase() andtoLowerCase()

Converts the entire string to upper or lower case letters.

let text = 'Hello, world!
console.log(text.toUpperCase()); // HELLO, WORLD!
console.log(text.toLowerCase()); // hello, world!

trim()
Removes spaces at the beginning and end of a string.
let text = ' Hello, world! ';
console.log(text.trim()); // 'Hello, world!

## Working with strings: searching and matching

### indexOf() andlastIndexOf()

Returns the index of the first or last occurrence of a specific substring. Returns -1 if the substring is not found.

let text = 'Hello, world!
console.log(text.indexOf('World')); // 7
console.log(text.lastIndexOf('l')); // 10

includes()
Checks whether a specific substring is contained in the string and returns true or false.

let text = 'Hello, world!
console.log(text.includes('World')); // true console.log(text.includes('foo')); // false

### substring() andsubstr()

Returns a substring based on start and end indices or the start position and length.

let text = 'Hello, world!
console.log(text.substring(0, 5)); // 'Hello' console.log(text.substr(7, 4)); // 'World'

## Working with Numbers: The Math object and more

TheMath object offers many useful mathematical functions and constants.
Math.PI
The constant Pi.
console.log(Math.PI); // 3.141592653589793

### Math.round(), Math.floor(), Math.ceil()

Rounding to the nearest whole number, rounding down and rounding up.

let num = 4.7;
console.log(Math.round(num)); // 5
console.log(Math.floor(num)); // 4
console.log(Math.ceil(num)); // 5

### Math.max() andMath.min()

Returns the largest or smallest value from a list of arguments.
console.log(Math.max(1, 2, 3)); // 3 console.log(Math.min(1, 2, 3)); // 1

## Working with Numbers: Random numbers

Math.random()
Returns a pseudorandomized number between 0 (inclusive) and 1 (exclusive).

### Example

let randomNum = Math.random();
console.log(randomNum); // e.g. 0.123456789

### Random numbers in a certain range

function getRandomInt(min, max) {
return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(getRandomInt(1, 10)); // Random number between 1 and 10 (inclusive)

## Working with Numbers: Problems with floating point numbers

JavaScript uses floating point numbers according to the IEEE 754 standard, which can lead to precision problems.

### Example

let result = 0.1 + 0.2;
console.log(result); // 0.30000000000000004

### Solution

You can control the precision by multiplication and division or by using thetoFixed() method.

### Example

let result = (0.1 * 10 + 0.2 * 10) / 10; console.log(result); // 0.3
let preciseResult = (0.1 + 0.2).toFixed(2); console.log(preciseResult); // '0.30'

# DOM I: Basics of the Document Object Model

## The Document Object Model (DOM)

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the document as a tree structure in which each element of the document is a node in the tree. With JavaScript, you can manipulate the DOM to dynamically change, create or remove content.

## The DOM starter template

To work with the DOM, you need an HTML file that serves as the basis.

### Example

html

<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>DOM basics</title>

</head>
<body>
<h1 id="title">Hello, world!</h1>
<p class="description">This is an introduction to the DOM.</p> <script src="script.js"></script>
</body>
</html>

## The document object: properties and methods

Thedocument object is the entry point for accessing the DOM. It offers various methods and properties for manipulating HTML elements.

### Example

console.log(document.title); // Returns the title of the document document.title = 'New title'; // Changes the title of the document

## Select elements: getElementById() method

You can use thegetElementById() method to select an element based on its ID.

### Example

let titleElement = document.getElementById('title'); console.log(titleElement.textContent); // Hello, world!

## Selecting elements: querySelector() andquerySelectorAll()

With querySelector() you can select the first element that corresponds to a CSS selector. With querySelectorAll() you can select all elements that correspond to a CSS selector.

### Example

let descriptionElement = document.querySelector('.description'); console.log(descriptionElement.textContent); // This is an introduction to the DOM

let allParagraphs = document.querySelectorAll('p'); allParagraphs.forEach(function(paragraph) { console.log(paragraph.textContent);
});

## Iterate over NodeLists and HTMLCollections

querySelectorAll() returns a NodeList that you can run through with forEach(). getElementsByClassName() and getElementsByTagName() return HTMLCollections that can be treated similarly to arrays.

### Example

let paragraphs = document.querySelectorAll('p'); paragraphs.forEach(function(paragraph) { console.log(paragraph.textContent);
});
let divs = document.getElementsByTagName('div'); for (let i = 0; i < divs.length; i++) { console.log(divs[i].textContent);
}

## The element object: properties and methods

Each HTML element in the DOM is an element object with various properties and methods.

### Example

let titleElement = document.getElementById('title'); console.log(titleElement.tagName); // H1
console.log(titleElement.id); // title
console.log(titleElement.className); // (empty, as no class)

titleElement.textContent = 'Hello, DOM!

## Navigating through the DOM

You can navigate through the DOM to find related elements.

### Example

let titleElement = document.getElementById('title');
console.log(titleElement.parentElement); // Returns the parent element console.log(titleElement.nextElementSibling); // Returns the next sibling element
console.log(titleElement.previousElementSibling); // Returns the previous sibling element (if available)

## Create elements, attributes and texts

You can create new elements, attributes and text nodes using methods such as createElement(), setAttribute() and createTextNode().

### Example

let newParagraph = document.createElement('p'); newParagraph.textContent = 'This is a new paragraph'; document.body.appendChild(newParagraph);

## The appendChild() method

You can use theappendChild() method to add an element as the last child of another element.

### Example

let newDiv = document.createElement('div'); newDiv.textContent = 'New div element'; document.body.appendChild(newDiv);

## The innerHTML, innerText andtextContent properties

These properties allow you to read or change the HTML or text content of an element.

### Example

let container = document.querySelector('.container'); container.innerHTML = '<p>New HTML content</p>'; container.innerText = 'New text content';
container.textContent = 'Another new text content';

## The insertAdjacent...() method

This method allows you to insert HTML content in relation to a specific element.

### Example

let referenceElement = document.querySelector('.reference'); referenceElement.insertAdjacentHTML('beforebegin', '<p>Before the element</p>');
referenceElement.insertAdjacentHTML('afterend', '<p>After the element</p>');
referenceElement.insertAdjacentHTML('afterbegin', '<p>At the beginning of the element</p>');
referenceElement.insertAdjacentHTML('beforeend', '<p>At the end of the element</p>');

## Remove elements

You can use theremove() method to remove an element from the DOM.

### Example

let elementToRemove = document.getElementById('remove-me'); elementToRemove.remove();

## The ID property

Each HTML element can have a unique ID that you can use to identify and manipulate specific elements.

### Example

let uniqueElement = document.getElementById('unique-id'); uniqueElement.style.color = 'red';

## The className property

You can use theclassName property to read and change the classes of an element.

### Example

let element = document.querySelector('.some-class'); element.className = 'new-class another-class';

## The classList property

With the classList property, you can add, remove and check classes without overwriting the existing classes.

### Example

let element = document.querySelector('.some-class'); element.classList.add('new-class');
element.classList.remove('some-class');
console.log(element.classList.contains('new-class')); // true

## Set, remove, read and request attributes

You can manipulate attributes of elements using methods such as setAttribute(), removeAttribute(), getAttribute() and hasAttribute().

### Example

let element = document.querySelector('img');
element.setAttribute('alt', 'Description');
console.log(element.getAttribute('alt')); // Description element.removeAttribute('alt');
console.log(element.hasAttribute('alt')); // false

## The style property

You can use thestyle property to set or change the inline styles of an element.

### Example

let element = document.querySelector('div'); element.style.backgroundColor = 'blue'; element.style.fontSize = '20px';

## The window object

Thewindow object represents the browser window and contains many useful properties and methods.

### Example

console.log(window.innerWidth); // Width of the window console.log(window.innerHeight); // Height of the window

## The getComputedStyles() method

With getComputedStyle() you can query the calculated styles of an element as they are applied by the browser.

### Example

let element = document.querySelector('p');
let styles = window.getComputedStyle(element);
console.log(styles.color); // Returns the text color of the element

## The location object

Thelocation object contains information about the current URL and allows you to navigate to new URLs.

### Example

console.log(window.location.href); // Current URL
window.location.href = 'https://www.example.com'; // Navigates to a new URL
These were the basics of the Document Object Model (DOM) in JavaScript. In the next chapter, we will look at advanced DOM manipulation and event handling.

# DOM II: Events and event listeners

## The basics of events and event listeners

An event is an action or event that takes place in the browser, such as a click, a keyboard input or the loading of a page. Event listeners are functions that react to these events and perform a specific task.

### Example

document.getElementById('myButton').addEventListener('click', function() { alert('Button was clicked!');
});

In this example, a message is displayed when the button with the ID myButton is clicked.

## Mouse events

Mouse events occur when the user interacts with the mouse.

### Important mouse events

• click: Occurs when an element is clicked.
• dblclick: Occurs when an element is double-clicked.
• mousedown: Occurs when a mouse button is pressed.
• mouseup: Occurs when a mouse button is released.
• mousemove: Occurs when the mouse is moved.
• mouseover: Occurs when the mouse pointer moves over an element.
• mouseout: Occurs when the mouse pointer leaves an element.

### Example

document.getElementById('myDiv').addEventListener('mouseover', function() { this.style.backgroundColor = 'yellow';
});

document.getElementById('myDiv').addEventListener('mouseout', function() { this.style.backgroundColor = '';

## Capturing and bubbling: preventDefault() andstopPropagation()

### Event bubbling

With event bubbling, the event is first propagated from the innermost to the outermost element.

### Event capturing

In event capturing, the event is propagated from the outermost to the innermost element.
preventDefault()
Prevents the default behavior of an event.
stopPropagation() Stops the further spread of the event in the event chain.

### Example

document.getElementById('myLink').addEventListener('click', function(event) {
event.preventDefault(); // Prevents the default behavior of the link alert('Link was clicked, but the page is not loaded!');
});

document.getElementById('parentDiv').addEventListener('click', function() { alert('Parent DIV was clicked!');
});

document.getElementById('childDiv').addEventListener('click', function(event) {
event.stopPropagation(); // Stops the propagation of the event
alert('Child DIV was clicked!');

## Keyboard events

Keyboard events occur when the user presses or releases a key.

### Important keyboard events

• keydown: Occurs when a button is pressed.
• keyup: Occurs when a key is released.
• keypress: Occurs when a key is pressed (obsolete, keydown and keyup are preferred).

### Example

document.addEventListener('keydown', function(event) { console.log('Key pressed: ' + event.key);
});

## Form events

Form events occur when the user interacts with forms.

### Important form events

• submit: Occurs when a form is submitted.
• change: Occurs when the value of a form field changes.
• input: Occurs when a form field is entered.

### Example

javascript

document.getElementById('myForm').addEventListener('submit', function(event) {
event.preventDefault(); // Prevents the default behavior of the form
alert('Form has been submitted!');
});

## Change events

Change events occur when the value of an element changes.

### Example

document.getElementById('myInput').addEventListener('change', function() { alert('The value of the input has changed!');

## Window events

Window events occur when certain events happen in the browser window.

### Important window events

• load: Occurs when the page is fully loaded.
• resize: Occurs when the size of the browser window is changed.
• scroll: Occurs when the page is scrolled.
• unload: Occurs when the page is left.

### Example

window.addEventListener('resize', function() { console.log('The window size has changed.');
});

## Trigger events

You can use thedispatchEvent method to trigger events manually.

### Example

let button = document.getElementById('myButton');

button.addEventListener('customEvent', function() { alert('Custom event triggered!');
});

let event = new Event('customEvent'); button.dispatchEvent(event);
That's the basics of events and event listeners in the DOM. In the next chapter, we will look at advanced JavaScript techniques and expert knowledge.

# Expert knowledge

## Arrow function ("fat arrow syntax")

Arrow functions are a compact syntax for creating functions and were introduced with ES6\. They also have differences in the behavior ofthis compared to normal functions.

### Syntax

const myFunction = (param1, param2) => { // Code
return result;

};

### Examples

const add = (a, b) => { return a + b;
};

console.log(add(5, 3)); // 8
// If the function only has one line, it can be shortened const multiply = (a, b) => a * b;
console.log(multiply(5, 3)); // 15

### Differences in the behavior ofthis

Arrow functions bind the this keyword from the surrounding context.
function Person() { this.age = 0;

setInterval(() => {
this.age++; // `this` refers to the object `person` console.log(this.age);

}, 1000);
}
let p = new Person();
// Outputs the current `age` every second

## Arrow functions and the this keyword

One of the main differences between arrow functions and conventional functions is the handling of the this keyword. In arrow functions, this is bound lexically, which means that it refers to the surrounding context in which the function was defined.

### Example

function Timer() { this.seconds = 0;

setInterval(() => {
this.seconds++;
console.log(this.seconds);

}, 1000);
}
let myTimer = new Timer();
// Outputs the current number of seconds every second

## The attributes async anddefer

These attributes are used to control the execution of scripts in HTML.
async
• The script is loaded asynchronously and executed as soon as it is available.
• The execution does not block the loading of the page.
html
<script src="script.js" async></script> defer

• The script is loaded asynchronously, but is only executed after the HTML document has been completely parsed.
• The order of thedefer scripts is retained.

html <script src="script.js" defer></script>

## The conditional ternary operator

The ternary operator offers a compact syntax for conditional expressions.

### Syntax

condition ? expr1 : expr2;

### Example

let age = 18;
let status = (age >= 18) ? 'Adult' : 'Minor';
console.log(status); // Of legal age

## The spread syntax

The spread syntax makes it possible to expand arrays or objects.

### Example with arrays

let arr1 = [1, 2, 3];
let arr2 = [...arr1, 4, 5, 6];
console.log(arr2); // [1, 2, 3, 4, 5, 6]

### Example with objects

let obj1 = {a: 1, b: 2};
let obj2 = {...obj1, c: 3};
console.log(obj2); // {a: 1, b: 2, c: 3}

## The rest parameter syntax

The rest parameter syntax makes it possible to receive a variable number of arguments as an array.

### Example

function sum(...numbers) {
return numbers.reduce((acc, curr) => acc + curr, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
That was the expert knowledge on advanced JavaScript techniques. In the next chapter, we will look at classes and object-oriented programming.

# Classes

## Object-oriented programming (OOP)

Object-oriented programming (OOP) is a programming paradigm based on the use of objects. An object contains both data (properties) and functions (methods) that can be applied to this data. JavaScript supports OOP through the use of classes.

## Introduction to the topic of classes

Classes are templates for objects. They define the properties and methods that the created objects have.

### Syntax

class ClassName {
constructor(parameter1, parameter2) { this.property1 = parameter1; this.property2 = parameter2;

}

method1() { // Method
}

method2() { // Method
}
}

### Example

class Person {
constructor(name, age) { this.name = name; this.age = age;

}
greet() {
console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
}
}
let person1 = new Person('Max', 30);
person1.greet(); // Hello, my name is Max and I am 30 years old.

## Classes and the constructor

Theconstructor is a special method that is called when a new object of the class is created. It initializes the properties of the object.

### Example

class Car {
constructor(make, model, year) { this.make = make;
this.model = model;
this.year = year;

}
displayInfo() {
console.log(`Auto: ${this.make} ${this.model}, year of manufacture

${this.year}`);
}
}

let car1 = new Car('Toyota', 'Corolla', 2020);
car1.displayInfo(); // Car: Toyota Corolla, year of manufacture 2020

## Methods

Methods are functions that are defined within a class and can be applied to the objects of this class.

### Example

class Rectangle {
constructor(width, height) { this.width = width;
this.height = height;

}

area() {
return this.width * this.height;
}
}

let rect = new Rectangle(5, 10); console.log(rect.area()); // 50

## Getter and setter

Getters and setters are special methods that enable the properties of an object to be read and written.

### Example

class Circle {
constructor(radius) { this._radius = radius; }

get radius() {
return this._radius;
}

set radius(value) {
if (value > 0) {
this._radius = value;

} else {
console.log('Radius must be positive.');
}
}

area() {
return Math.PI * this._radius * this._radius;
}
}

let circle = new Circle(5);
console.log(circle.radius); // 5
circle.radius = 10;
console.log(circle.area()); // 314.1592653589793 circle.radius = -1; // Radius must be positive.

## The alternative to getters and setters

You can also use normal methods to set and get properties.

### Example

class Square {
constructor(side) { this.side = side; }

getSide() {
return this.side;
}

setSide(value) {
if (value > 0) {
this.side = value;

} else {
console.log('Side length must be positive.');
}
}

area() {
return this.side * this.side;
}
}

let square = new Square(4);
console.log(square.getSide()); // 4
square.setSide(6);
console.log(square.area()); // 36
square.setSide(-2); // Side length must be positive.

## Extending classes I: extends andsuper()

With extends, you can let a class inherit from another class in order to take over its properties and methods. With super() you can call the constructor of the base class.

### Example

class Animal {
constructor(name) { this.name = name; }

speak() {
console.log(`${this.name} makes a noise.`);
}
}

class Dog extends Animal { constructor(name, breed) { super(name);
this.breed = breed;

}

speak() {
console.log(`${this.name}, the ${this.breed}, barks.`);
}
}

let dog = new Dog('Bella', 'Labrador'); dog.speak(); // Bella, the Labrador, barks.

## Extending classes II: Adding and overwriting properties and methods

Extended classes can add their own properties and methods or override the methods of the base class.

### Example

class Person {
constructor(name) { this.name = name; }

introduce() {
console.log(`Hello, I'm ${this.name}.`);
}
}

class Student extends Person { constructor(name, subject) { super(name);
this.subject = subject;

}
introduce() {
console.log(`Hello, I'm ${this.name} and I'm studying ${this.subject}.`);
}

study() {
console.log(`${this.name} is currently studying ${this.subject}.`);
}
}

let student = new Student('Anna', 'Informatik');
student.introduce(); // Hi, I'm Anna and I'm studying computer science. student.study(); // Anna is currently studying computer science.

That was the introduction to classes and object-oriented programming in JavaScript. In the next chapter, we will look at the installation of a local web server.

# Install local web server

## Installation and setup of XAMPP

XAMPP is a free and user-friendly solution for creating a local web server. It contains Apache, MySQL, PHP and Perl and is available for various operating systems.

### Step 1: Download XAMPP

1\. Visit the official XAMPP website.
2\. Download the version for your operating system (Windows, macOS or Linux).

### Step 2: Installation of XAMPP

1\. Open the downloaded file to start the installation.
2\. Follow the instructions of the installation wizard.
3\. Select the components you want to install (all are selected by default).
4\. Select the installation directory (by defaultC:\xampp on Windows).
5\. Click on "Next" and complete the installation.

### Step 3: Starting XAMPP

1\. Open the XAMPP Control Panel.
2\. Start the Apache web server by clicking on "Start" next to "Apache".
3\. Optional: Also start MySQL if you need a database.

### Step 4: Testing the local web server

1\. Open your web browser and enterhttp://localhost in the address bar.
2\. You should see the XAMPP start page. This means that your local web server is running successfully.

## Setting up a development directory

### Step 1: Create a new project folder

1\. Navigate to the XAMPP installation directory (e.g. C:\xampp on Windows).
2\. Open the htdocs folder.
3\. Create a new folder for your project (e.g. my-project).

### Step 2: Creating an HTML file

1\. Create a new file called index.html in your project folder.
2\. Add the following sample content:

<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initialscale=1.0">
<title>My project</title>
</head>
<body>
<h1>Welcome to my project!</h1>
<p>This is a local web server page.</p>
</body>
</html>

### Step 3: Test your site

1\. Open your web browser and enterhttp://localhost/mein-projekt in the address bar.
2\. You should see the contents of the index.html file.

## Advantages of a local web server

1\. Fast testing and development: Changes can be tested immediately without the need for an internet connection.
2\. Security: Your project is only available locally and is not accessible to the public.
3\. Complete control: You have complete control over the server environment and configurations.

## Next steps

Once you have set up a local web server, you can start developing and testing dynamic web applications. This is particularly useful for working with server-side technologies such as PHP and MySQL.

That was the installation and setup of a local web server with XAMPP. In the next chapter, we will look at cookies and saving data.

# Cookies and data storage

## Cookies

Cookies are small text files that are stored by a website on the user's computer. They are used to store user data between visits.

### Set cookies

You can set cookies with document.cookie.

### Example

document.cookie = "username=JohnDoe; expires=Fri, 31 Dec 2024 23:59:59 GMT; path=/";
In this example, a cookie with the name username and the value JohnDoe is set, which expires on December 31, 2024 and is available on the entire website.

## Cookies: Defining the shelf life of cookies

Theexpires property determines when the cookie expires.

### Example

document.cookie = "username=JohnDoe; expires=Fri, 31 Dec 2024 23:59:59 GMT; path=/";

### Max-Age

Alternatively, you can usemax-age to set the lifetime of a cookie in seconds.

### Example

document.cookie = "username=JohnDoe; max-age=3600; path=/"; // Cookie expires after 1 hour

## Overwrite and delete cookies

A cookie can be overwritten with a new value by setting the same name. To delete a cookie, set the expiration date in the past.

### Example

// Overwrite a cookie
document.cookie = "username=JaneDoe; path=/";

// Delete a cookie
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/";

## Check and read cookies

With document.cookie you can access all cookies as a string.

### Example

console.log(document.cookie); // username=JaneDoe

### Read cookies

To get the value of a specific cookie, you can write a function that searches the cookies.

### Example

function getCookie(name) {
let matches = document.cookie.match(new RegExp(

"(?:^|; )" + name.replace(/([.$?*|{}()[]\\\/+^])/g, '\\$1') + "=([^;]*)"
));
return matches ? decodeURIComponent(matches[1]) : undefined;

}
console.log(getCookie('username')); // JaneDoe

## The JSON.stringify() andJSON.parse() methods

These methods are used to convert JavaScript objects into JSON strings and vice versa.
JSON.stringify()
Converts a JavaScript object into a JSON string.

### Example

let user = { name: "John", age: 30

};
let jsonString = JSON.stringify(user);
console.log(jsonString); // {"name": "John", "age":30} JSON.parse() Converts a JSON string into a JavaScript object.

### Example

let jsonString = '{"name": "John", "age":30}'; let user = JSON.parse(jsonString);
console.log(user.name); // John console.log(user.age); // 30

## Local storage and session storage

Local Storage and Session Storage are web storage APIs that make it possible to store data in the browser.

### Local Storage

Local Storage stores data without an expiration date.

### Example

// Save
localStorage.setItem('username', 'JohnDoe');

// Read out
let username = localStorage.getItem('username'); console.log(username); // JohnDoe

// Delete
localStorage.removeItem('username');
// Delete all entries localStorage.clear();

### Session Storage

Session Storage stores data for the duration of the session. The data is deleted when the browser window is closed.

### Example

// Save
sessionStorage.setItem('username', 'JohnDoe');

// Read out
let username = sessionStorage.getItem('username'); console.log(username); // JohnDoe

// Delete
sessionStorage.removeItem('username');
// Delete all entries sessionStorage.clear();
That was an introduction to cookies and data storage in JavaScript. In the next chapter, we will look at modules and learn how to use them to better organize your code.

# Modules

## Introduction to the topic of modules

JavaScript modules allow code to be broken down into smaller, reusable and more maintainable parts. ES6 introduced the official module system in JavaScript, which makes it possible to export functions, objects or values from one module and import them into other modules.

## Integrate modules in HTML

To use JavaScript modules in HTML, the <script> tag must be provided with the attribute type="module".

### Example

html

<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Module example</title>

</head>
<body>

<script type="module" src="main.js"></script>
</body>
</html>

## Export features

You can export functions, objects or values with theexport keyword.

### Individual export

// utils.js
export function add(a, b) { return a + b;
}

### Several exports

// utils.js
export const PI = 3.14159; export function subtract(a, b) {

return a - b;
}

## Import features

Use the import keyword to use exported functions, objects or values in another module.

### Example

// main.js
import { add, subtract, PI } from './utils.js';

console.log(add(2, 3)); // 5 console.log(subtract(5, 2)); // 3 console.log(PI); // 3.14159

## Designated exports and imports

Named exports make it possible to export several values from one module and import them with the same names in other modules.

### Example

// math.js
export const PI = 3.14159; export function multiply(a, b) {

return a * b;
}
javascript

// main.js
import { PI, multiply } from './math.js';
console.log(PI); // 3.14159 console.log(multiply(2, 3)); // 6

## Default exports

A module can export a default value that is marked with thedefault keyword. There can only be one default export per module.

### Example

// logger.js
export default function log(message) { console.log(message);
}
javascript
// main.js
import log from './logger.js'; log('This is a message.'); // This is a message.

## Module objects

You can import all exports of a module as an object.

### Example

// math.js
export const PI = 3.14159; export function add(a, b) {

return a + b;
}
export function subtract(a, b) {

return a - b;
}
javascript

// main.js
import * as math from './math.js';

console.log(math.PI); // 3.14159 console.log(math.add(2, 3)); // 5 console.log(math.subtract(5, 2)); // 3

## Aggregate modules

You can aggregate several modules into a single module and export them again.

### Example

// geometry.js
export * from './circle.js'; export * from './rectangle.js'; javascript

// circle.js
export const PI = 3.14159;
export function area(radius) {

return PI * radius * radius;
}
// rectangle.js
export function area(width, height) {

return width * height;
}
// main.js
import { PI, area as circleArea } from './geometry.js'; import { area as rectangleArea } from './geometry.js';

console.log(PI); // 3.14159
console.log(circleArea(3)); // 28.27431 console.log(rectangleArea(4, 5)); // 20

## Dynamic loading of modules

You can use theimport() function to load modules dynamically. This is useful if you only want to load modules when required.

### Example

// main.js
import('./utils.js').then(module => {
console.log(module.add(2, 3)); // 5
});
That was the introduction to JavaScript modules. In the next chapter, we'll finish the book and congratulate you on completing it!

# Congratulations, you've made it!

## Review of what we have learned

You have now been given a comprehensive overview of JavaScript and its many possibilities. Here is a brief summary of what you have learned in this book:

1\. Introduction to JavaScript: Basic concepts and history.
2\. Preparation: Installation and setup of the development environment.
3\. The basics of JavaScript: First steps and syntax.
4\. Variables: Dealing with variables and data types.
5\. Operators: Mathematical and logical operators.
6\. Control structures: Conditional statements and loops.
7\. Functions: Definition and use of functions.
8\. Objects: Create and manipulate objects.
9\. Arrays: Working with arrays and their methods.
10. Time, date, intervals and timeouts: Handling date and time functions.
11. Working with strings and numbers: methods for string and number manipulation.
12. DOM I: Basics of the Document Object Model.
13. DOM II: Event handling and advanced DOM manipulations.
14. Expert knowledge: Advanced JavaScript techniques such as arrow functions and modules.
15. Classes: Object-oriented programming in JavaScript.
16. Installing a local web server: Setting up a local development server.
17. Cookies and data storage: Handling cookies and web storage.
18. Modules: Use and management of JavaScript modules.

## Your next step

Learning JavaScript is an ongoing journey. Here are some tips and resources to further deepen your knowledge:

### Online resources

• Mozilla Developer Network (MDN): MDN Web Docs offers comprehensive and upto-date documentation on JavaScript.
• W3Schools: JavaScript Tutorial offers easy-to-understand tutorials and examples.
• JavaScript.info: The Modern JavaScript Tutorial is a detailed resource for modern JavaScript practices.

### Online courses

• Codecademy: Learn JavaScript
• Udemy: The ultimate JavaScript complete course by Ruben Winkler
• freeCodeCamp: JavaScript Algorithms and Data Structures

### Books

• Eloquent JavaScript by Marijn Haverbeke
• You Don't Know JS (book series) by Kyle Simpson
• JavaScript: The Good Parts by Douglas Crockford

## Practical projects

To consolidate your knowledge, it is important to develop your own projects. Here are some ideas:

• To-do list: A simple application to manage tasks.
• Calculator: A basic calculator for mathematical operations.
• Weather app: An application that retrieves and displays weather data from an API.
• Quiz game: An interactive game in which the user answers questions.

## Community and support

• Stack Overflow: A large community to ask questions and find answers.
• GitHub: Host and share your projects to get feedback and participate in open source projects.
• Meetups: Search for local or virtual meetings of JavaScript developers to share experiences and learn.

## Further topics

Once you feel comfortable with the basics, you can delve deeper into specialized topics:
• Frameworks and libraries: Learn popular JavaScript frameworks such as React,

Angular or Vue.js.
• Backend development: Explore server-side JavaScript with Node.js.
• TypeScript: A superset of JavaScript that adds static typing and facilitates the

development of large applications.

Congratulations on your progress! JavaScript is a powerful and versatile language, and you have now mastered the basics and some advanced concepts. Stay curious and keep experimenting - the possibilities are endless!
Imprint :

Torsten May
May Media and Marketing P.O. Box 130507 42032 Wuppertal

E-Mail: Torstenmai@aol.com