![](Images/cover00153.jpeg)

1.  [Cover](kindle:embed:0001?mime=image/jpg)
2.  [Table of contents](#part0001.xhtml_toc-title)

# Introduction

JavaScript is the basic building block of front end web apps.

jQuery is a library that is popular for manipulating the DOM.

In this book, we'll look at how to use both together.

# JavaScript

JavaScript is one of the most popular programming languages in the world. To use it effectively, we’ve to know about the basics of it.

In this section, we’ll look at the basics of JavaScript.

## Alerts

The `alert` function displays an alert box with some text we pass in.

The text comes from the string argument.

For instance, can write:

```
alert("hello world!");
```

and ‘hello world’ would be displayed.

It is a global function, so it’s a property of `window` . `window.alert` is the same as `alert` .

The short form is fine for inclusion in our code.

## Variables and Strings

Strings are basic elements of JavaScript code. They store text data.

A variable with the given name can only be declared once.

They can be stored in variables. Variables are names that we choose and assign values to so that we can store them for use later.

For example, we can write:

```
let name = "james";
```

to store names.

We can set a variable declared with `let` to a new value.

For example, we can write:

```
let name = "james";
name = "mark";
```

Then the value of `name` will be `"mark"` .

We can declare a variable and leave it undefined.

For instance, we can write:

```
let name;
name = "james";
```

We can do this with variables declared with `let` .

Variables can be declared with any name that isn’t in the reserved keywords list.

The list is at [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords).

Variables aren’t enclosed in quotes and text strings are enclosed in quotes.

JavaScript strings can be enclosed in single or double-quotes.

They can also be enclosed with backticks.

If they’re enclosed with backticks, then they have to have variables embedded in them.

For example, we can write:

```
let firstName = 'james';
let lastName = 'smith';
let name = `${firstName} ${lastName}`;
```

We interpolate the value of `firstName` and `lastName` into the string. So `name` should be `'james smith'` .

This is a template literal. We can put any expression inside the strings.

This is a very convenient way to combine various expressions into a string.

Now we can assign variables, we can pass variables into `alert` instead of passing the whole string.

For example, we can write:

```
let text = "hello world!"
alert(text);
```

We pass in `text` into `alert` as an argument to display the alert.

We can reference `text` anywhere after it’s defined.

## Variables and Numbers

Numbers are another primitive data type with JavaScript.

We can also assign them to variables.

For example, we can write:

```
let length = 100;
```

This makes doing operations on it easy. For example, we can add a number to `length` :

```
length + 10
```

then the sum of `length` and 10 is 110.

We know that `length` isn’t a variable because it’s not enclosed in quotes.

And numbers alone can be used variable names, so JavaScript knows it’s a number.

We can replace 10 with a variable by assigning it to a variable.

For example, we can write:

```
let length = 100;
let additionalLength = 10;
let totalLength = length + additionaLength;
```

We have the `additionalLength` variable that we add to the `length` and assign the sum to the `totalLength` variable.

## Looping Through an Array

We can loop through an array with by using the `length` property of an array for the ending condition.

For example, we can write:

```
let matchFound = false;
for (let i = 0; i < cleanestCities.length; i++) {
  if (city === cleanestCities[i]) {
    matchFound = true;
    console.log("It's one of the cleanest cities");
  }
}
```

We get the `length` property of the `cleanestCities` array for the ending condition.

We loop from 0 to `cleanestCities.length — 1` . This way, we loop through the items from start to end without setting comparing a fixed number value for the ending condition.

If we want to stop a loop early, we can use the `break` keyword.

For example, we can write:

```
for (let i = 0; i < cleanestCities.length; i++) {
  if (city === cleanestCities[i]) {
    console.log("It's one of the cleanest cities");
    break;
  }
}
```

If `city` is equal to `clesnestCities[i]` , then we end the loop with `break` .

We can nest loops in our code. For example, we can write:

```
let firstNames = ['james', 'mary', 'alex'];
let lastNames = ['jones', 'wong', 'green'];
let fullNames = [];
for (let i = 0; i < firstNames.length; i++) {
  for (let j = 0; j < lastNames.length; j++) {
    fullNames.push(`${firstNames[i]} ${ lastNames[j]}`);
  }
}
```

We have a `for` loop inside another `for` loop.

The outer loop loops through the `firstNames` array.

In each iteration, the inner loop is run to loop through the `lastNames` array.

And inside the inner loop, we push the combination of `firstNames[i]` and `lastNames[j]` into the `fullNames` array.

The result is all the combinations of `firstNames` and `lastNames` entries added to the `fullNames` array.

We can have as many levels of nesting as we like. However, the more nesting we have, the harder the code is to read.

## Changing Case

We can change the case of strings with the `toUpperCase` and `toLowerCase` methods.

`toUpperCase` changes a string’s letters all to upper case.

And `toLowerCase` changes a string’s letters all to lower case.

For example, we can write:

```
"Santa Fe".toLowerCase()
```

Then we get:

```
"santa fe"
```

returned.

And if we write:

```
"Santa Fe".toUpperCase()
```

And we get:

```
"SANTA FE"
```

## Strings Length and Parts

We can get the number of characters of a string with the `length` property.

For example, we can write:

```
"Santa Fe".length
```

and have 8 returned.

To get the parts of a string, we can use the `slice` method.

It takes the start and end indexes that we want to extract.

The end index itself is excluded.

For example, if we write:

```
"Santa Fe".slice(2, 4)
```

Then we have `“nt”` returned.

## Finding String Segments

We can find string segments with the `indexOf` method. It’ll return the starting index of the string that we pass in as the argument if the string is inside the string we call `indexOf` with.

For example, we can write:

```
"Santa Fe".indexOf('Fe')
```

then 6 is returned since The ‘F’ character is in index 6.

## if Statements

If statements let us run code conditionally.

For example, we can write:

```
const answer = prompt("Where's the capital of Italy?");
if (answer === "Rome") {
  alert("Correct!");
}
```

to add a prompt to take in an answer to the question.

Then we check for it in th `if` statement. If `answer` is `'Rome'` , then we show the `'Correct!'` alert.

An `if` statement if followed by a boolean expression we’re checking for.

If the boolean expression returns `true` , then we run the code between the curly brace.

We should always use `===` to check for value equality since it checks for the type and value.

Simple `if` statements may be written without curtly brackets or the statement may be written all in one line.

But it’s more convenient to read to have the curly braces because it’s clearer.

## Comparison Operators

The `===` operator is the comparison operator.

It’s the equality operator.

It’s used to compare 2 things to see if they’re equal.

We can use the equality operator to compare the return value of any 2 expressions.

For example, we can write:

```
if (totalCost === 81.50 + 100) {
```

or

```
if (fullName === firstName + " " + "wong") {
```

String comparisons are case-sensitive, so only if both cases are the same then the strings are considered the same.

If we want to check if 2 expressions aren’t the same, then we can use the `!==` inequality comparison operator.

So if we have:

```
"Rose" !== "rose"
```

then that returns `true` since they have letters with different cases.

JavaScript comes with more operators.

They include `>` for the greater-than operator.

`<` is the less-than operator.

`>=` is the greater than or equal to operator.

`<=` is the less than or equal to operator.

We can use them by writing:

```
if (2 > 0) {
if (0 < 2) {
if (2 >= 0) {
if (2 >= 1) {
if (0 <= 2) {
if (1 <= 2) {
```

## if…else and else if Statements

If we have more than one case to check for then we can use the `else` keyword to add more cases.

For example, we can write:

```
const answer = prompt("Where's the capital of Italy?");
if (answer === "Rome") {
  alert("Correct!");
} else {
  alert("Wrong!");
}
```

The `else` keyword is before the block that’s run when `answer` isn’t `'Rome'` .

If we have more cases, then we can add the `else if` statement.

For example, we can write:

```
const answer = prompt("Where's the capital of Italy?");
if (answer === "Rome") {
  alert("Correct!");
} else if (answer === "Vatican") {
  alert("Close!");
} else {
  alert("Wrong!");
}
```

We run something is `answer` is `'Vatican'` .

If `answer` isn’t `'Rome'` or `'Vatican'` , then we run the last block.

## Testing Sets of Conditions

We can test more than one condition with an `if` statement.

To combine them, we can use the `&&` or `||` operators.

`&&` is the logical AND operator and `||` is the logical OR operator.

For example, we can write:

```
if (weight > 300 && time < 6) {
  alert("athlete");
} else {
  alert("chef");
}
```

to check the value of `weight` and `time` together.

If `weight` is less than 300 and `time` is less than 6, then the first block is run.

Otherwise, then 2nd block is run.

We can chain more conditional together:

```
if (weight > 300 && time < 6 && age > 17 && gender === "male") {
  alert("athlete");
} else {
  alert("chef");
}
```

This will test if all the conditional are `true` . If they’re all `true` , then the first block is run,

Otherwise, the 2nd block is run.

The `||` operator can be used in a similar way.

For example, we can write:

```
if (SAT > avg || GPA > 2.5 || sport === "football") {
  alert("accepted");
} else {
  alert("not accepted");
}
```

The `||` operator returns `true` if any of the conditional returns `true` .

We can mix `||` and `&&` together.

For example, we can write:

```
if (age > 65 || age < 21 && res === "U.S.")
```

The `&&` takes precedence, so `res === “U.S.”` is evaluated first.

And the `||` operator is evaluated next.

To make this clearer, we should surround the expressions with parentheses so everyone can read it easily:

```
if ((age > 65 || age < 21) && res === "U.S.")
```

## Nested if Statements

We can nest `if` statements. For example, we can write:

```
if (c === d) {
  if (x === y) {
    g = h;
  } else if (a === b) {
    g = h;
  } else {
    v = u;
  }
} else {
  v = u;
}
```

We nest the inner expressions with 2 spaces to make them easy to type and readable.

We shouldn't have too many levels of nesting since it’s hard to read.

## Arrays

There’s often a need to store many values in our programs.

To make this easier, we can use arrays.

For example, instead of repeatedly declaring variables to store similar values:

```
let city0 = "Oslo";
let city1 = "Rome";
let city2 = "Toronto";
let city3 = "Denver";
let city4 = "Los Angeles";
let city5 = "Seattle";
```

We can put them all into an array by writing:

```
let cities = ["Oslo", "Rome", "Toronto", "Denver", "Los Angeles", "Seattle"];
```

Arrays are very useful for storing a list of data that are fixed size or dynamic size.

We can access an array entry by its index.

For example, we can write:

```
cities[2]
```

JavaScript can be an array with different types. For example, we can write:

```
let mixedArray = [1, "james", "mary", true];
```

The index of the first entry is 0\. The same naming rules for variables apply to arrays.

Arrays can only be declared once like other variables.

## Finding a Character at a Location in a String

We can find a character at a location in a string with the `charAt` method or the square brackets notation.

For example, we can write:

```
let firstChar = 'james'.charAt(0)
```

then `firstChar` is `'j'` .

This is the same as:

```
let firstChar = 'james'[0]
```

They’re the same, so the square brackets are used more often since it’s shorter.

## Replacing Characters

The `replace` method lets us replace characters.

For example, we can write:

```
let newText = text.replace("World War II", "the Second World War");
```

to replace `“World War II”` with the `“the Second World War”` .

It’ll search for the first instance of it and replace it.

To search all instances of it and replace all of them, we need to use a regex:

```
let newText = text.replace(/World War II/g, "the Second World War");
```

The `g` flag stands for global. This means it’ll replace all of them.

## Rounding Numbers

We can use the `Math.round` method to round numbers.

For example, we can write:

```
let score = Math.round(11.1);
```

Then we round 11.1 to 11 with `Math.round` .

It rounds to the nearest integer.

The function rounds up when the decimal is .5.

To always round up to the nearest integer, we can use the `Math.ceil` method:

```
let score = Math.ceil(11.1);
```

Then we get 12.

To always round down to the nearest integer, we can use the `Math.floor` method:

```
let score = Math.floor(11.1);
```

## Generating Random Numbers

JavaScript comes with a function to generate random numbers.

The `Math.random` method lets us create a random number between 0 and 1.

For example, we can write:

```
let randomNumber = Math.random();
```

The returned number has 16 decimal places.

## Converting Strings to Integers and Decimals

Convert strings with numbers to an integer or decimal number is something that we often have to do.

We can use the `parseInt` method to convert a string into an integer.

And we can use the `parseFloat` method to convert a string into a decimal number.

For example, we can write:

```
let currentAge = prompt("Enter your age.");
let age = parseInt(currentAge);
```

We have the `parseInt` method to convert the entered number into an integer.

`prompt` always returns a string, so we’ll have to convert it to an integer.

To convert the entered text into a decimal number, we can use `parseFloat` :

```
let currentAge = prompt("Enter your age.");
let age = parseFloat(currentAge);
```

## Converting Strings to Numbers and Vice Versa

To convert a string to a number, we can use the `Number` global function:

```
let num = Number('123');
```

Then `num` is `123` .

To convert a number to a string, we can use the `toString` method:

```
let num = 1234;
let numberAsString = num.toString();
```

The `numberAsString` is `'1234'` .

## Adding and Removing elements

We can add and remove array elements easily with JavaScript.

To add elements, we just assign a value to the array index we want.

For example, we can write:

```
let animals = [];
animals[0] = "dog";
animals[1] = "cat";
animals[2] = "mouse";
```

We created the `animals` array by creating a variable and assigning it to an empty array.

Then we assign values to the given index of `animals` .

We can do this for any index and the indexes don’t have to be consecutive or in order.

To remove the last item from the array, we call the `pop` method:

```
animals.pop()
```

An alternative to add elements to an array is to use the `push` method:

```
animals.push("fish", "bird");
```

`push` adds elements to the end of the array.

To remove the first element of an array, we can `shift` :

```
animals.shift();
```

To add one more elements to the beginning of an array, we call `unshift` :

```
animals.shift("fish", "bird");
```

The `splice` method insert one or more elements anywhere in the array:

```
pets.splice(2, 2, "pig", "duck", "emu");
```

The first argument is the starting index to insert.

The 2nd is number of items to remove.

The subsequent arguments are the items we want to insert in place of the removed items.

The `slice` method lets us copy one or more consecutive elements in any position and put them in a new array.

For example, we can write:

```
let pets = animals.slice(2, 4);
```

to copy the items from index 2 to 3 from `animals` and return that array.

The first argument is the starting index copy. The 2nd is 1 after the ending index to copy.

The 2nd index itself isn’t included in the range.

## for loops

Loops are provided by JavaScript so we can run code repeatedly.

To do this, we can use the `for` loop:

```
for (let i = 0; i <= 10; i++) {
  if (city === cleanestCities[i]) {
    console.log("It's one of the cleanest cities");
  }
}
```

A `for` loop is composed of the heading, which has the starting index, the condition to continue running the loop, and a statement to update the index.

In the loop body, we can do what we want.

In the example above, we check it `city` is equal to `cleanestCities[i]` .

And if it’s `true` , we console log a message.

The loop index is used for accessing the array item and also to move the loop towards the ending condition, which is `i <= 10` .

If `i` is bigger than 10, then the loop stops.

We can also set flags in `for` loops so that we can record some information/

For example, we can write:

```
let matchFound = false;
for (let i = 0; i <= 10; i++) {
  if (city === cleanestCities[i]) {
    matchFound = true;
    console.log("It's one of the cleanest cities");
  }
}
```

We set `matchFound` to `true` once we found a value from `cleanesCities` that’s equal to `city` .

## Math Expressions

We should eliminate ambiguity with JavaScript math expressions.

For example, if we have:

```
let totalCost = 1 + 3 * 10;
```

then readers may be confused about which operation comes first.

JavaScript has precedence rules for operators. They generally follow the same rules as normal math.

However, we can make everyone’s lives easier by wrapping parentheses around expressions that have higher precedence.

For example, we can write:

```
let totalCost = 1 + (3 * 10);
```

then we wrap the expressions around the multiplication.

Now we know the multiplication operation comes first.

If we move the parentheses, then the operations would be done in a different order.

For instance, if we have:

```
let totalCost = (1 + 3) * 10;
```

then the addition is done before the multiplication.

## Concatenating Strings

Strings are text values and they can be combined with concatenation.

For example, we can write:

```
alert("Thanks, " + userName + "!");
```

to combine the 3 expressions into 1 with the `+` operator.

If `userName` is `'james'` , then we have:

```
'Thanks, james!'
```

The 3 parts are combined together and returned as one string.

We can concatenate strings with any other JavaScript expressions.

They’ll be converted to strings automatically so that they can be concatenated together.

So if we have:

```
alert("2 plus 3 equals " + 2 + 3);
```

Then we get `'2 plus 3 equals 23'` .

This is because 2 and 3 are converted to strings before they’re concatenated.

A more convenient way to combine strings and other expressions is to use template literals.

For example, we can write:

```
alert(`2 plus 3 equals ${2 + 3}`);
```

We replaced the quotes with the backticks.

Then we use the `${}` symbols to surround the JavaScripot expressions to interpolate the expressions.

This way, we have `2 + 3` returning a number since they’re concatenated with strings.

So we get `'2 plus 3 equals 5'` .

## Prompts

A prompt box lets us ask use for some information and provide a response field for the answer.

For example, we can write:

```
let name = prompt("Your name?", "mary");
```

We call `prompt` with the question string as the first argument.

The 2nd argument is the default answer returned.

If we call that, the browser will show an alert box with an input box to let us enter our answer.

Then when we click OK, then the response is returned if it’s entered.

Otherwise, the default answer is returned.

If we omit the default answer in the 2nd argument and we entered nothing, then it returned `null` .

`prompt` is a global function, so `window.prompt` is the same as `prompt` .

But we can just write `prompt` .

## Variable Naming

We can’t have variable names that start with a number, but we can have variables that have numbers in the middle.

For example, we can write:

```
let name1 = "james";
```

but not:

```
let 1name = "james";
```

There are more rules to JavaScript variable naming.

A variable name can’t have any spaces.

Variable names can only have letters, numbers, dollar signs and underscores.

Variable names can’t be a reserved JavaScript keyword, but they can contain them.

Capital letters can be used, but we must be aware that variable names are case sensitive.

So `name` isn’t the same as `Name` .

JavaScript variable names are usually camelCase. They let us form variables with multiple words and we can read them all easily.

So we can write variable names like `firstName` to make the 2 words in the variable name clear.

## Math Expressions

Most JavaScript programs will do math. Therefore, JavaScript comes with operators for various common math operations.

For example, we can add with the `+` operator:

```
let num = 2 + 2;
```

To subtract, we can use the `-` operator:

```
let num = 2 - 2;
```

Multiplication is done with the `*` operator:

```
let num = 2 * 2;
```

And division is done with the `/` operator:

```
let num = 2 / 2;
```

There’s also the `%` modulus operator to find the remainder of the left operand divided by the right one.

For example, we can write:

```
let num = 2 % 2;
```

We get 0 because 2 is evenly divisible by itself.

The exponentiation operator is denoted by `**` . For example, we can use it by writing:

```
let num =  2 ** 2;
```

Then we raise 2 to the 2nd power.

The `++` operator adds the variable’s value by 1 and assign it to the variable.

For example:

```
num++;
```

is the same as:

```
num = num + 1;
```

We can use the expressions with the assignment operator, but we may get results that we don’t expect.

For example, if we have:

```
let num = 1;
let newNum = num++;
```

Then `newNum` is 1 since the original value of `num` is returned.

On the other hand, if we have:

```
let num = 1;
let newNum = ++num;
```

Then `newNum` is 1 since the latest value of `num` is returned if `++` is before the `num` .

Likewise, JavaScript has the `--` operator to subtract a variable by 1 and assign the latest value to the variable.

For example, we can write:

```
let num = 1;
let newNum = num--;
```

And we get 1 for `newNum` and:

```
let num = 1;
let newNum = --num;
```

then we get 0 for `newNum` .

How the values are returned work the same way as `++` .

## Controlling the Length of Decimals

We can control the length of decimals by using the `toFixed` method.

For example, if we have:

```
let total = (8.8888).toFixed(2);
```

Then `total` is `'8.89'` . `toFixed` takes the number of digits to round to and returns string with the rounded number.

If the decimal ends with a 5, it usually rounded up.

But some browsers kay round down.

## Get the Current Date and Time

To get the current date and time, we can create a new `Date` instance with `new Date()` .

Then we can convert the `Date` instance to a string by writing:

```
let now = new Date();
let dateString = now.toString();
```

To get the day of the week, we call the `getDay` method:

```
let now = new Date();
let day = now.getDay();
```

It returns a number from 0 to 6, with 0 being Sunday, and 6 being Saturday.

If we want to show a more human-readable date, we can write:

```
let dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]
let now = new Date();
let day = now.getDay();
let dayName = dayNames[day];
```

We can use `day` as the index of `dayNames` to get the English version of the day of the week.

## Extracting Parts of Date and Time

The `Date` instance comes with various methods to get various parts of a date and time.

`getMonth` returns the month of the date from 0 to 11, with 0 being January and 11 being December.

`getDate` gives us the number for the dat of the month.

`getFullYear` returns the 4 digit version of the year.

`getHours` gives us a number from 0 to 23, which corresponds to midnight and 11pm.

`getMinutes` returns the minutes of the hour from 0 to 59.

`getSeconds` returns the seconds of the minute from 0 to 59.

And `getMilliseconds` returns a number from 0 to 999.

`getTime` gives us the number of milliseconds that have elapsed since Jan 1, 1970 midnight UTC.

We can call them all from a date instance. For example, we can write:

```
let now = new Date();
let day = now.`getMilliseconds`();
```

## Specify Date and Time

We can specify date and time with the `Date` constructor.

To return the current date and time, we write:

```
let today = new Date();
```

And we can calculate the number of days difference by subtracting the timestamp between 2 dates:

```
let msToday = new Date().getTime();
let msAnotherDay = new Date(2029, 1, 1).getTime()
let msDiff = msAnotherDay - msToday;
```

Then to get the number of days difference, we can write:

```
let daysDiff = msDiff / (1000 * 60 * 60 * 24);
```

If we want to return the round the days to a whole number, we round down with `Math.floor` :

```
daysDiff = Math.floor(daysDiff);
```

## Change Date and Time

The `Date` instance lets us change various parts of the date and time.

`setFullYear` lets us set the year of a `Date` instance.

`setMonth` lets us set the month of a `Date` instance. It accepts a number from 0 to 11, with 0 being January and 11 being December.

`setDate` lets us set the day of the month.

`setHours` lets us set the minutes past an hour.

`setSeconds` lets us set the seconds past the minute.

And `setMilliseconds` lets us set the milliseconds past the second.

For example, we can call `setFullYear` by writing:

```
let d = new Date();
d.setFullYear(2040);
```

or:

```
let d = new Date();
d.setMonth(11);
```

The rest can be called the same way.

## Functions

Functions are blocks of code that we can use repeatedly to do what we want.

We called functions before with `setFullYear` , `setMonth` , etc.

They may take 0 or more arguments.

For example, we can create our own `tellTime` function by writing:

```
function tellTime() {
  let now = new Date();
  let jr = now.getHours();
  let min = now.getMinutes();
  alert(`${hr}:${min}`);
}
```

We called `getHours` to get the hours and `getMinutes` to get the minutes.

## Pass Data to Functions

Functions can have parameters so we can pass data to them.

For example, we can write:

```
function greetUser(greeting) {
  alert(greeting);
}
```

The `greetUser` method accepts the `greeting` parameter, and we use the value as the argument for the `alert` function.

This way, we can specify the message for the alert.

We can call our function by writing:

```
greetUser('hello james');
```

Now we should see an alert with the ‘hello james’ text displayed.

We can separate multiple parameters and arguments with commas. For example, we can write:

```
function showMessage(greeting, name) {
  alert(`${greeting}, ${name}`);
}
```

The `showMessage` function has the `greeting` and `name` parameters.

Then we can call `showMessage` by writing:

```
showMessage('hello', 'mary');
```

With parameters, we can customize how functions can be called.

## Return Data in Functions

If we want to get the data computed by functions, then we add the `return` statement to return the data we want from the function.

For example, we can write:

```
function getTotal(subtTotal, taxRate) {
  return subTotal * (1 + taxRate);
}
```

We created the `getTotal` function that takes the `subTotal` and `taxRate` parameters.

Then we return the computed result by using the `return` statement.

We can call the `getTotal` function by writing:

```
const total = getTotal(100, 0.05);
```

We pass in the numbers for the `subTotal` and `taxRate` and assign the returned value to `total` .

Therefore, `total` is 105.

## do…while Loops

We can use the `do...while` loop to repeatedly run code.

The `do` block is always run, so the first iteration is always run.

For example, we can write:

```
let i = 0;
do {
  console.log(i);
  i++;
} while (i <= 3);
```

The `do` block is always run because the `while` condition is checked after the iteration of a loop is done.

## Script Tags

To run JavaScript code in the browser, we have to add script tags to our code.

For example, we can write:

```
<script>
  function sayHi() {
    alert("hi");
  }

  function sayBye() {
    alert("bye");
  }
</script>
```

We define the `sayHi` and `sayBye` functions in the script tag.

We can have any JavaScript code in our script tags.

JavaScript code is just text, so we can add them to HTML files easily, since they’re also text.

If we have lots of code in between the script tags, then we should move them to their own file.

For example, we can write:

```
<script src="script.js"></script>
```

We create a `script.js` file and then reference it with the `src` attribute.

This way, we can keep our code files short.

## Comments

We can add comments to our JavaScript code to explain what we’re doing what our code.

For example, we can write:

```
// This is a comment
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

The `//` indicates the start of a comment. It’ll be ignored by the browser.

We can write multiline comments by writing:

```
/*
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas at volutpat ipsum, dapibus tincidunt nisl. Donec vestibulum ultricies laoreet. Suspendisse sit amet faucibus justo.
*/
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

We have a long comment that spans multiple lines. It’s delimited by `/*` and `*/` .

## Link Events

When we click links, we can listen to events emitted by the links when we do something to them like clicking it.

This is handy for using it to do something in addition to letting us click to go to a different page.

For example, we can write:

```
<a href="#" onClick="alert('hello');">Click</a>
```

We add the `onClick` attribute to an `a` tag so that we can run JavaScript code in it.

`onClick` isn’t case sensitive.

`href='#'` tells the browser to reload the page, which is probably not what we want when we want to run JavaScript code when we click the link.

To prevent the page from being refreshed, we can write:

```
<a href="javaScript:void(0)" onClick="alert('hello');">Click</a>
```

We add the `javaScript.void(0)` code to avoid the refresh.

If we want to write multiple statements, we can write:

```
<a href="javaScript:void(0)" onClick="let greeting='hi'; alert(greeting);">Click</a>
```

We separate the statements with a semicolon.

## Local vs Global Variables

JavaScript has local and global variables.

Local variables are accessible only within a block.

And global variables are available throughout the app.

With JavaScript, we create local variables with the `let` and `const` keywords.

They are all block-level, so they’re all only available within a block like functions, and `if` blocks.

`let` creates a variable, and `const` creates constants.

Constants can’t be reassigned a new after it’s assigned a value. 

But the content may still change.

Constants must have an initial value assigned to it when it’s created.

For example, if we have:

```
function addNumbers() {
  let theSum = 2 + 2;
}
```

The `theSum` is only available within the `addNumbers` function.

But if we have:

```
function addNumbers() {
  theSum = 2 + 2;
}
```

then `theSum` is a global variable.

We can access the value anywhere.

If a variable is global, then it’s attached property of the `window` global object.

We should avoid global variables since it’s easy to create global variables with the same name.

Therefore, it’s easy to have conflicts.

And it’s hard to track how variables are changed.

## Switch Statements

The `switch` statement lets us do different things for different cases in one statement.

For example, we can write:

```
switch (dayOfWk) {
  case "Sat":
    alert("very happy");
    break;
  case "Sun":
    alert("happy");
    break;
  case "Fri":
    alert("happy friday");
    break;
  default:
    alert("sad");
}
```

We check the value of `dayOfWk` to let us do different things when it has the given values.

If `dayOfWk` is `'Sat'` , then we show a `'very happy'` alert.

If `dayOfWk` is `'Sun'` , then we show a `'happy'` alert.

If `dayOfWk` is `'Fri'` , then we show a `'happy friday'` alert.

The `default` clause is run when `dayOfWk` has any other value, and we show the `'sad'` alert.

The `break` keyword is required so that the rest of the `switch` statement won’t run after a case is found.

The `switch` statement above is the same as:

```
if (dayOfWk === "Sat") {
  alert("very happy");
} else if (dayOfWk === "Sun") {
  alert("happy");
} else if (dayOfWk === "Fri") {
  alert("hapopy friday");
} else {
  alert("sad");
}
```

`default` in the `switch` statement is the same as the `else` in the `if` statement.

## While Loops

The JavaScript `while` loop is another kind of loop that we may use.

It lets us run a loop when a given condition is `true` .

For example, we can write:

```
let i = 0;
while (i <= 3) {
  console.log(i);
  i++;
}
```

In the loop above, when `i` is less than or equal to 3, then we run the loop.

Inside the loop body, we update `i` so that we work toward ending the loop.

We indent the loop block with 2 spaces for easy typing and readability.

## Button Events

We can add event handling code to buttons so that it can do something when we click it.

For example, we can write:

```
<input type="button" value="Click Me" onClick="alert('Hello world!');">
```

We have a button that has the `onClick` attribute with JavaScript code to call `alert` .

Therefore, we’ll see an alert box displayed when we click it.

The `value` attribute has the button text.

We can do the same for other elements.

For example, we can write:

```
<a href="http://google.com"><img onClick="alert('Hello world!');" src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo"></a>
```

When we click on the image, we see the alert box displayed.

If we want to make the code cleaner, we can put the `alert` call into its own function.

We can write the following HTML:

```
<a href="http://google.com"><img onClick="greet()" src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo"></a>
```

And the following JavaScript:

```
const greet = () => {
  alert('Hello world!');
}
```

## Mouse Events

We can listen to mouse events by using attributes and set their values to JavaScript code.

For example, we can write:

```
<h1 onMouseover="alert('hello world.');">hello world</h1>
```

to show an alert box when we hover over the h1 element.

We can also add the `onMouseout` event handler to do something when we hover over the element and then reverse it when we move the mouse away from it:

```
<h1 onMouseover="this.style.color='green'" onMouseout="this.style.color='black'">hello world</h1>
```

`this` in the code above is the h1 element.

We set the `color` style to `'green'` when we hover over the h1 element.

Then when we move the mouse away, then we set the `color` back to black.

## Input Events

Likewise, we can listen to events emitted by the input element.

For example, we can write:

```
<input type="text" size="30" onFocus="this.style.backgroundColor = 'yellow';" onBlur="this.style.backgroundColor = 'white';">
```

We added the `onFocus` and `onBlur` handlers to set the `backgroundColor` style to `'yellow'` when we focus on the input element.

Then when we move the cursor away from the input, it goes back to a white background.

## Reading Field Values

We can read the value entered into the input field when we submit the form.

We can write the following HTML:

```
<form onSubmit="checkAddress('email'); return false;">
  Email:
  <input type="text" id="email">
  <input type="submit" value="Submit">
</form>
```

And the following JavaScript to check the email field:

```
const checkAddress = (fieldId) => {
  if (document.getElementById(fieldId).value === "") {
    alert("Email is required.");
  }
  return false;
}
```

The `checkAddress` function gets the value of the input with ID `email` .

Then if it’s empty, we see the `'Email is required'` message in the alert.

We need the `return false` in the `onSubmit` attribute and the `checkAddress` function to prevent the default submit behavior.

We can clean up the function by writing:

```
const checkAddress = (fieldId) => {
  const {
    value
  } = document.getElementById(fieldId)
  if (value === "") {
    alert("Email is required.");
  }
  return false;
}
```

## Setting Field Values

We can set input field values by using JavaScript.

For example, we can write the following HTML:

```
<form>
  fruit:<br>
  <input type="text" id="fruit" onBlur="fillColor();"><br>
  color:<br>
  <input type="text" id="color">
</form>
```

Then we can write the following JavaScript code:

```
const fillColor = () => {
  let color;
  const {
    value
  } = document.getElementById("fruit");
  switch (value) {
    case "apple":
      color = "red";
      break;
    case "orange":
      color = "orange";
      break;
    case "grape":
      color = "purple";
  }
  document.getElementById("color").value = color;
}
```

We added the `onBlur` attribute to the first input box.

So when we move the cursor away from the first input, the `fillColor` function is called.

Them we get the value if the input with ID `fruit` ‘s value with the `value` property.

Then we set the `color` variable’s value with according to the value of `value` .

We then set the input with ID `color` ‘s value with the value of the `color` variable.

## Reading and Setting Paragraph Text

We can read and set paragraph text.

For example, we can write the following HTML:

```
<p id="text">
  Lorem ipsum dolor sit amet.
  <a href="javascript:void(0);" onClick="expandText();">
    <em>Click for more.</em>
  </a>
</p>
```

Then we can add the `expandText` function as follows:

```
const expandText = () => {
  const expandedParagraph = `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras id lorem eget erat vestibulum consectetur. Donec vehicula porta est ut vestibulum. Mauris et nisl a sem iaculis laoreet. Nunc eleifend facilisis massa ut luctus. Nullam sollicitudin non lorem non eleifend. Curabitur elementum felis quis enim malesuada varius.`;
  document.getElementById("text").innerHTML = expandedParagraph;
}
```

The `a` element has the `onClick` attribute that is set to the `expandText()` expression.

So when we click on the ‘Click for more’ text, we’ll see the expanded text displayed on the screen.

This is because we set the `expandedParagraph` variable’s value as the value of the `innerHTML` property of the element with ID `text` .

We can insert anything into an element by setting the `innerHTML` property.

For example, we can keep the existing HTML and change the JavaScript to:

```
const expandText = () => {
  const expandedParagraph = `
    <ol>
      <li>Slow</li>
      <li>Fast</li>
      <li>Just-right</li>
     </ol>
   `;
  document.getElementById("text").innerHTML = expandedParagraph;
}
```

We set the content of the element with ID `text` to an ordered list.

So that’s what we’ll see when we click on Click for more.

## Manipulating Images and Text

We can manipulate images with JavaScript.

For example, we can write the following HTML:

```
<img src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo" id="image" onClick="makeInvisible();">
```

Then we can add the following CSS:

```
.hidden {
  visibility: hidden;
}
```

Then the `makeInvisible` function is:

```
const makeInvisible = () => {
  document.getElementById("image").className = "hidden";
}
```

The `hidden` class has the `visibility` property set to `hidden` .

Therefore, when we click on the image, the `makeInvisible` function is run.

Then the `hidden` class is added to the `img` element.

So the image will be hidden.

## Adding Class Names

We can add a class name to an HTML element with the JavaScript class names API.

For example, we can write the following HTML:

```
<img src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo" id="image" onClick="expand();">
```

Then we can write the following CSS:

```
.big {
  width: 500px;
}
```

Then we can add the `expand` function by writing:

```
const expand = () => {
  document.getElementById("image").classList.add('big');
}
```

The `big` class has the width set to 500px.

In the `expand` function, we call the `class:ist.add` method to add the `'big'` class to the element with the ID `image` .

And we set the `onClick` attribute with `expand()` to call the `expand` function when we click the image.

The image will then be expanded when we click on the image.

## Swapping Images

We can swap an image for another when we hover over the image.

For example, we can write the following HTML:

```
<img src="https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo" id="image" onMouseover="swap(1);" onMouseout="swap(0)">
```

And the following JavaScript code:

```
const swap = (index) => {
  const images = [
    'https://i.picsum.photos/id/23/200/300.jpg?hmac=NFze_vylqSEkX21kuRKSe8pp6Em-4ETfOE-oyLVCvJo',
    'https://i.picsum.photos/id/25/200/300.jpg?hmac=ScdLbPfGd_kI3MUHvJUb12Fsg1meDQEaHY_mM613BVM'
  ]
  const image = document.querySelector('#image');
  image.src = images[index];
}
```

When we hover over the image, the `swap(1)` expression is run.

It’s set as the value of the `onMouseover` attribute, so it’ll run when we hover over the image element.

If we move our mouse out of the image, then `swap(0)` is run to show the original image.

This is because `swap(0)` is set as the value of the `onMouseout` attribute.

## Setting Styles

We can set styles with the `className` or `style` property.

For example, we can write the following HTML:

```
<p>
  hello world
</p>
```

And write the following CSS:

```
.big {
  font-size: 2em
}
```

Then write the following to make the text big with JavaScript:

```
document.querySelector("p").classList.add("big");
```

We get the p element with the `document.querySelector` method.

Then we add the `big` class to the `p` element with the `classList.add` method.

Alternatively, we can set the `style` property to the value we want:

```
document.querySelector("p").style.fontSize = '2em'
```

The `style.fontSize` property is the same as the `font-size` CSS property.

However, it’s better to use CSS and class names since it’s faster than setting styles with JavaScript.

Also, CSS code is more reusable.

Other `style` properties we can set include:

```
document.querySelector("p").style.cssFloat = "left";
```

to set the CSS`float` property to `left` .

We can set the `visibility` CSS property by writing:

```
document.querySelector("p").style.visibility = "hidden";
```

And the margin can be set by writing”:

```
document.querySelector("p").style.margin = "0 10px 0 10px;";
```

## Target All Elements by Tag Name

We can get all elements by tag name.

This is more convenient than getting a single element with its ID or using `querySelector` to get the first element with the given selector.

For example, we can write the following HTML:

```
<p>foo.</p>
<p>bar.</p>
<p>baz.</p>
```

Then we can get all the `p` elements and loop through them by writing:

```
const pars = document.getElementsByTagName('p')
for (const p of pars) {
  p.style.fontFamily = "Verdana, Geneva, sans-serif";
}
```

We get the `p` elements, then loop through them with the for-of loop.

In the loop body, we set the `fontFamily` style to change the font of the text.

## Constructor Methods

We can add methods to constructors or classes.

For example, we can write:

```
class Plan {
  constructor(name, price, space, pages) {
    this.name = name;
    this.price = price;
    this.space = space;
    this.pages = pages;
  }

  calcAnnualPrice() {
    return this.price * 12;
  }
}
```

We add the `calcAnnualPrice` method to return the value of `this.price * 12` .

`this` is the class instance, which is the object that’s created and returned when we invoke the `Plan` class.

So we get the `price` property from the object we create from the class and multiply it by 12.

To invoke the constructor and call the method on the created object, we can write:

```
const plan = new Plan('basic', 3, 100, 10)
console.log(plan.calcAnnualPrice())
```

We invoke the `Plan` constructor with the `new` keyword.

Then we call `calcAnnualPrice` on the `plan` object to get the annual price.

The class syntax is just syntactic sugar on top of prototype inheritance.

The `calcAnnualPrice` method is just a property of the `Plan` ‘s `prototype` property.

The `prototype` is the prototype of the `Plan` class, which is the object that it inherits from.

If we log the value of `Plan.prototype.calcAnnualPrice` :

```
console.log(Plan.prototype.calcAnnualPrice)
```

we see the code of the `calcAnnualPrice` method logged.

## Checking for Properties and Methods

To check if a property or method is actually in the object itself rather than its prototype, we can use the `hasOwnProperty` method.

For example, if we created an object from the `Plan` class:

```
const plan = new Plan('basic', 3, 100, 10)
```

Then we can call `hasOwnProperty` by writing:

```
console.log(plan.hasOwnProperty('name'))
```

Then we should see `true` logged since `name` is a property of the `plan` object itself.

The `hasOwnProperty` method comes from `Object.prototype` , which is a property of almost all JavaScript objects.

If we want to list an object’s properties, we can write:

```
for (const prop in plan) {
  if (plan.hasOwnProperty(prop)) {
    console.log(prop);
  }
}
```

We loop through the `plan` ‘s property keys with the for-in loop.

The for-in loop loops through all then properties and its prototypes, so we have to use the `hasOwnProperty` method to check if a property is actually in the `plan` object itself.

`prop` is the property name itself.

Therefore, we should see:

```
name
price
space
pages
```

logged.

## Getting the URL

We can get and set the URL of the page with JavaScript.

To get the URL, we can use the `window.location.href` property.

If we type that into the browser dev console, we should get the full URL of the page.

`window.location.hostname` has the hostname which is the first part of the URL.

For example, if we have the URL`“https://jsfiddle.net/09t6La27/10/"` , then `window.location.hostname` returns `“jsfiddle.net”` .

`window.location.hash` returns the part of the URL after the `#` sign.

For example, if we have `http://example.com/#foo` , `window.location.hash` returns `“#foo”` .

## Objects

We need objects to store values other than primitive values like numbers, strings, booleans, etc.

It servers as a container for all the items we want to store.

For example, we can define an object by writing:

```
const plan = {
  name: "Basic",
  price: 3,
  space: 100,
  transfer: 1000,
  pages: 10
};
```

We created the `plan` object with various properties.

`name` , `price` , `space` , `transfer` , and `pages` are property names.

The expressions after the colon are their values.

Properties are separated by a comma.

To access a property, we can write:

```
plan.name
```

`plan.name` ‘s value should be `'Basic'` .

We can assign properties with different values.

For example, we can write:

```
plan.name = 'Deluxe';
```

Then `name` property’s new value is `'Deluxe'` .

We can assign values with any data type with the assignment operator.

To check if a property is in an object, we can use the `in` operator.

For example, if we have:

```
'name' in plan
```

then that should return `true` since `name` is a property of `plan` .

But if we have:

```
'foo' in plan
```

then that returns `false` since `foo` isn’t a property of `plan` .

We need the property name in quotes since the left operand is a string.

## Object Methods

Objects can have methods.

For example, we can write:

```
const plan = {
  name: "Basic",
  price: 3,
  space: 100,
  transfer: 1000,
  pages: 10,
  calcAnnualPrice() {
    return this.price * 12;
  }
};
```

to add the `calcAnnualPrice` method into the `plan` object.

`this` is the object itself, so `this.price * 12` returns the value of the `price` property multiplied by 12.

## Constructors

We can create objects with the same structure with constructors.

They’re the templates for objects.

To create a constructor, we can write:

```
function Plan(name, price, space, pages) {
  this.name = name;
  this.price = price;
  this.space = space;
  this.pages = pages;
}
```

We created the `Plan` constructor that takes the `name` , `price` , `space` , and `pages` parameters.

Then we assign them to properties of `this` with the same name.

When we invoke the constructor, `this` will be returned with all the properties we assigned.

To invoke it, we can write:

```
const plan = new Plan('basic', 3, 100, 10)
```

We use the `new` keyword to call the constructor and create the object.

The value of `plan` is:

```
{
  name: "basic"
  pages: 10
  price: 3
  space: 100
}
```

A better way to write the constructor is to use the class syntax.

For example, we can write:

```
class Plan {
  constructor(name, price, space, pages) {
    this.name = name;
    this.price = price;
    this.space = space;
    this.pages = pages;
  }
}
```

The `constructor` method is the same as the constructor function we have before.

It just looks different. This is the preferred way to create constructors since it’s consistent with other popular object-oriented languages.

## Target All Elements by Tag Name with querySelectorAll

The `document.querySelectorAll` method lets us get all the elements with the given selector.

So to get all the elements with the given tag name, we can write the following HTML:

```
<p>foo.</p>
<p>bar.</p>
<p>baz.</p>
```

Then we can get all of them and style them by writing:

```
const pars = document.querySelectorAll('p')
for (const p of pars) {
  p.style.fontFamily = "Verdana, Geneva, sans-serif";
}
```

We get all the `p` elements with `document.querySelectorAll` .

Then we loop through each item with the for-of loop and set the `style.fontFamily` property to set the font family.

## Target Some Elements by Tag Name

We can target some elements by tag name with the `document.querySelectorAll` method since it takes any selector string as an argument.

For example, if we have the following HTML table:

```
<table>
  <tr>
    <td>foo</td>
    <td>bar</td>
    <td>baz</td>
  </tr>
</table>
```

and we want to get all the `td` elements in the table, we can write:

```
const tds = document.querySelectorAll('table td')
for (const t of tds) {
  t.style.backgroundColor = "pink";
}
```

We get the `td` elements within the `table` element with the `table td` selector.

Then we loop through the `td` elements and set the `backgroundColor` to `'pink'` .

## The DOM

The DOM stands for Document Object Model. It’s the way that browsers represent the HTML elements with JavaScript.

HTML elements are organized in a tree structure in the DOM.

Each level is indicated by the indentation.

For example, if we have:

```
<html>

  <head>
    <title>
      Simple document
    </title>
  </head>

  <body>
    <p>
      hello world
    </p>
  </body>

</html>
```

Then the `html` element is the root of the tree.

The `head` and `body` are at the 2nd level.

The `title` and `p` elements are at the 3rd level.

The topmost element is the `document` object.

Therefore `html` element is the parent of the `head` and `body` elements.

The `title` element is the child of the `head` element.

And the `p` element is the child of the `body` element.

We can find child elements with the DOM methods that we used before like `querySelector` , `querySelectorAll` , `getElementById` and `getElementByTagName` .

For example, if we have the following HTML:

```
<html>

<head>
    <title>
      Simple document
    </title>
  </head>

  <body>
    <div id="weather">
      <p>Today is sunny.</p>
      <p>Yesterday is rainy.</p>
    </div>
    <div id="density">
      <p>City is crowded.</p>
      <p>Desert is sparse.</p>
    </div>
  </body>
</html>
```

Then if we want to get the ‘Today is sunny’ text, we can write:

```
const sunny = document.querySelector('#weather p');
console.log(sunny.innerHTML)
```

We use the `#weather p` selector with the `querySelector` method to get the first p element from the div with the ID `weather` .

Then we get its content with the `innerHTML` property.

## Node Object Types

There are several kinds of node types.

They include:

*   `DOCUMENT_NODE` — `window.document`
*   `ELEMENT_NODE` — body, a, p, h1, etc.
*   `ATTRIBUTE_NODE` — `id='foo'` , `class='foo'`
*   `TEXT_NODE` — text that is between the tags.
*   `DOCUMENT_FRAGMENT_NODE` — anything returned by `document.createDocumentFragment()`
*   `DOCUMENT_TYPE_NODE` — `<!doctype html>`

Not instance, we can write:

```
document.ELEMENT_NODE
```

to get the value for `ELEMENT_NODE` which is 1.

The `Node` object has all the node constant values.

From the `Node` object, we can see that `ELEMENT_NODE` is 1.

`TEXT_NODE` is 3, `ATTRIBUTE_NODE` is 2, `DOCUMENT_NODE` is 9, `DOCUMENT_FRAGMENT_NODE` is 11, and `DOCUMENT_TYPE_NODE` is 10.

## Sub-Node Objects

The `HTMLElement` object inherits from the `Node` object via the `Element` object.

Other things like `Attr` , `Text` , `HTMLDocument` , and `DocumentFragment` all insert from `Node` .

For instance, we can write:

```
const body = document.querySelector('body');
```

And we can loop through the keys as follows:

```
for (const key in body) {
  console.log(key);
}
```

We should see the node properties in addition to the `HTMLElement` propeties.

## Properties and Methods for Nodes

Each node has the following properties:

*   `childNodes`
*   `firstChild`
*   `lastChild`
*   `nextSibling`
*   `nodeName`
*   `nodeType`
*   `nodeValue`
*   `parentNode`
*   `previousSibling`

They allow us to traverse between different nodes.

`childNodes` has the child nodes.

`firstChild` has the first child.

`lastChild` has the last child.

`nextSibling` has the next sibling node.

`nodeName` has the name of the node.

`nodeType` has the type of the node.

`parentNode` has the parent of the current node.

`previousSibling` has the previous sibling of the current node.

Methods include:

*   `appendChild()`
*   `cloneNode()`
*   `compareDocumentPosition()`
*   `contains()`
*   `hasChildNodes()`
*   `insertBefore()`
*   `isEqualNode()`
*   `removeChild()`
*   `replaceChild()`

`appendChild` adds a new child.

`cloneNode` clones the current node and returns it.

`compareDocumentPosition` compares the position of each node.

`contains` check if the node has another node as a child.

`insertBefore` adds a node before the current node.

`isEqualNode` checks if it’s the same.

`removeChild` removes a given child node.

`replaceChild` replaces one child element with another.

Document methods include:

*   `document.createElement()`
*   `document.createTextNode()`

`createElement` creates a new element as the name suggests, `createTextNode` creates a text node that can be put into an element.

HTML Element Properties include:

*   `innerHTML`
*   `outerHTML`
*   `textContent`
*   `innerText`
*   `outerText`
*   `firstElementChild`
*   `lastElementChild`
*   `nextElementChild`
*   `previousElementChild`
*   `children`

`innerHTML` has the HTML content inside an element.

`outerHTML` has all the HTML content of `innerHTML` in addition to the enclosing tags.

`textContent` has the text content inside an element.

`innerText` has the text content inside an element.

`outerText` include the content from `innerText` plus the enclosing tags.

`firstElementChild` has the first child node that’s an HTML element.

`lastElementChild` has the last child node that’s an HTML element.

`nextElementChild` has the element node after the current node.

`previousElementChild` has the element node before the current node.

`children` has the child nodes of the current node.

HTML element objects have the `insertAdjacentHTML` method to insert a node according to the position specified.

## Identifying the Type and Name of a Node

We can identify the type with the `nodeType` property and `nodeName` identifies the name.

For instance, `document.nodeName` return `'#document` , and `document.nodeType` returns 9, which means it’s a `DOCUMENT_NODE` .

## Getting a Node’s Value

The `nodeValue` property returns `null` for most types of nodes.

But we can use it to extract the text from `Text` and `Comment` nodes.

For instance, if we have:

```
<a>hi</a>
```

Then:

```
console.log(document.querySelector('a').firstChild.nodeValue);
```

logs `'hi'` .

## DocumentFragment

A `DocumentFragment` is a type of node that provides a lightweight document DOM that’ external to the live DOM tree.

It’s a document template that acts like the real one but lives in memory.

Its child nodes can easily be manipulated in memory and appended to the live DOM.

## Creating DocumentFragments

The `createDocumentFragment` method lets us create document fragments.

For instance, we can write:

```
const frag = document.createDocumentFragment();for (const s of ['foo', 'bar', 'baz']) {
  const p = document.createElement("p");
  p.textContent = s;
  frag.appendChild(p);
}
```

We created a document fragment with `createDocumentFragment` .

Then we loop through the array strings to create p elements and append them as child elements of the fragment.

The advantage of creating a document fragment is that we can store it in memory.

It may contain any kind of node except `body` or `html`.

The fragment itself isn’t added to the DOM when we append a fragment.

Only the node in it is added.

When a document fragment is appended to the DOM, it transfers from the document to the place where it’s appended.

It’ll be removed from memory.

Elements, on the other hand, are always in memory.

## Adding a DocumentFragment to the DOM

We can pass a document fragment to the `appendchild` and `insertBefore` to another element.

For instance, we can append what we have in the previous example to the body by writing:

```
const frag = document.createDocumentFragment();for (const s of ['foo', 'bar', 'baz']) {
  const p = document.createElement("p");
  p.textContent = s;
  frag.appendChild(p);
}document.body.appendChild(frag);
```

Now we add the p elements created to the body.

## Using innerHTML on a Document Fragment

We can use `innerHTML` to set the content of the fragment with a string.

For instance, we can create a document fragment by writing:

```
const frag = document.createDocumentFragment();const div = document.createElement('div');
frag.appendChild(div);
frag.querySelector('div').innerHTML = '<p>foo</p><p>bar</p>';document.body.appendChild(frag);
```

We create a fragment with `createFragment` . Then we create a div to hold the contents.

And then we set the content of the div our own HTML.

Finally, append the fragment content to body with `appendChild` .

## Leaving Fragments Containing Nodes in Memory

If we want to keep the contents of the fragment, we can clone it.

For instance,e if we have the following fragment:

```
const frag = document.createDocumentFragment();for (const s of ['foo', 'bar', 'baz']) {
  const p = document.createElement("p");
  p.textContent = s;
  frag.appendChild(p);
}
```

We can clone it by writing:

```
document.body.appendChild(frag.cloneNode(true));
```

Then we keep the document fragment content while appending it to the body.

## CSS Stylesheets

We can add styles to a page by using the link tag.

Also, we can add style tags or style attributes to documents.

Each style sheet is added to an HTML document is represented by the `CSSStylesheer` object.

If we have a style element:

```
<style>
  body {
    background-color: green;
  }
</style>
```

We can retrieve a stylesheet with JavaScript by writing:

```
console.log(document.querySelector('style').sheet);
```

And we get an object with the style sheet.

## Accessing All Style Sheets

We can use the `styleSheets` property to get all the style sheets.

For example, if we have the following CSS:

```
<!doctype html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <style>
      body {
        background-color: #fff;
      }
    </style>
  </head>
  <body>
  </body>
</html>
```

Then we can get the style sheets with:

```
console.log(document.styleSheets);
```

We can also use the `sheet` property of a link element as follows:

```
console.log(document.querySelector('link').sheet);
```

## CSSStyleSheet Properties and Methods

A `CSSStyleSheet` has properties and methods.

They have the following:

*   `disabled` — indicates whether the style sheet is disabled
*   `href` — value of the `href` attribute
*   `media` — destination media for the style information
*   `ownerNode` — the node that associates the stylesheet with the document
*   `parentStylesheet` — the parent style sheet
*   `title` — value of the `title` attribute
*   `type` — value of the `type` attribute
*   `cssRules` — an array-like object for holding rules that compose the stylesheet
*   `ownerRule` — holds the import rule which imported the stylesheet
*   `deleteRule` — method to remove a rule from the stylesheet object
*   `insertRule` — method to insert a rule into the stylesheet

## Convert a NodeList or HTMLCollection to an Array

To convert a NodeList or HTMLCollection to an array, we can use the spread operator or the `Array.from` method to do it.

We can write:

```
const arr = [...document.querySelectorAll('p')];
```

or we can write:

```
const arr = Array.from(document.querySelectorAll('p'));
```

Now we can use the array method that we want to use like `map` , `filter` , `pop` , `push` , etc. on a NodeList of HTMLCollection object.

## Traversing Nodes in the DOM

We can traverse nodes in the DOM with various properties.

They include:

*   `parentNode`
*   `firstChild`
*   `lastChild`
*   `nextSibling`
*   `previousSibling`

`parentNode` has the parent nodes of the current node.

`firstChild` has the first child of the current node.

`lastChild` has the last one.

`nextSibling` has the node immediately after the current node.

`previousSibling` has the node immediately before the current node.

To traverse the DOM but ignore the text and comment nodes, we can use the following properties:

*   `firstElementChild`
*   `lastElementChild`
*   `nextElementSibling`
*   `previousElementSibling`
*   `children`

The `firstElementChild` has the first child element of the current element.

`lastElementChild` has the last child element of the current element.

`nextElementChild` has the sibling element immediately after the current one.

`previousElementSibling` has the sibling element immediately before the current one.

`children` has the children of the current element.

For instance, we can use:

```
document.body.children
```

to get all the child nodes of the body element.

## Check the Node Position in the DOM Tree

We can use the `contains` method to check if an element is inside another element.

For instance, we can write:

```
const isInside = document.querySelector('html').contains(document.querySelector('body'));
```

Then that should return `true` since `body` is always inside the `html` element.

`compareDocumentPosition` returns a number that indicates where the position is of the elements we’re comparing relative to each other.

The return value 0 means that the elements are identical.

1 means the nodes aren’t in the same document.

2 means that the node precedes the selected node.

3 means the node follows the selected node.

8 means the passed node is the ancestor of the selected node.

16 or 10 in hex means the passed node is a descendant of the selected node.

It’s possible for a node to have more than one type of relationship with another node.

In that case, the numbers will be added together and returned.

Given the following HTML:

```
<div id='foo'>
  <p>
    foo
  </p>
  <p>
    bar
  </p>
</div>
```

We can use it as follows:

```
const div = document.querySelector('div')
const p = document.querySelector('p')const result = div.compareDocumentPosition(p);
console.log(result);
```

We get 20 since a node contains and precedes a node, this means it’s 16 + 4 which is 20.

## HTMLElement

`HTMLElement` is a constructor that’s used to create objects that represent nodes in a HTML document.

It includes the following child constructors:

*   `HTMLHtmlElement`
*   `HTMLHeadElement`
*   `HTMLLinkElement`
*   `HTMLTitleElement`
*   `HTMLMetaElement`

and many more.

They represent various elements on the page.

## HTMLElement Object Properties and Methods

`HTMLElement` instances have many properties and methods to let us manipulate them.

We can use `createElement` to create an element.

`tagName` to get the tag name.

`children` to get the child elements.

`getAttributes` to get the child attributes

`setAttribute` to set an attribute.

`hasAttribute` to check if an element exists.

`removeAttribute` to remove an attribute.

`classList` is an object used to manipulate the set of classes.

`dataset` returns any attribute that starts with `data-` .

`attributes` has the attribute list.

The full list is at [https://developer.mozilla.org/en-US/docs/Web/API/element](https://developer.mozilla.org/en-US/docs/Web/API/element).

## Creating Elements

We can create elements with the `createElement` method.

For example, we can create an input by writing:

```
const input = document.createElement('input');
document.body.appendChild(input);
```

Then we see an input element on the screen.

## Getting the Tag Name of an Element

The `tagName` property returns the name of an element.

It returns the same value that `nodeName` would return.

The tag name would be returned in upper case.

For instance, if we have:

```
<a href="http://example.com">hello</a>
```

Then:

```
console.log(document.querySelector('a').tagName);
```

logs `'A'` .

## Getting a List or Collection of element Attributes

The `attributes` property returns a collection of attribute nodes that an element currently has defined.

If we have:

```
<a href="http://example.com" title="example" data-foo="dataFoo" class="example">hello</a>
```

Then we can get all the nodes into an array by writing:

```
const attrs = [...document.querySelector('a').attributes];
```

We convert the attributes array-like object into an array using the spread operator.

The attributes returned are live which means the content can be changed at any time.

The actual object return by `attributes` is a `NameNodeMap` , which is an array-like object.

It has a `length` property.

Boolean attributes show up in the `attributes` list but have no value.

## Getting, Setting, & Removing an Element’s Attribute Value

We can use the `getAttribute()` , `setAttribute()` , and `removeAttribute()` methods to manipulate attributes.

For example, if we have:

```
<a href="http://example.com" title="example" data-foo="dataFoo" class="example">hello</a>
```

Then we can call:

```
const a = document.querySelector('a');
a.removeAttribute('href');
```

to remove the `href` attribute.

And we can write:

```
a.setAttribute('href', '#');
```

to set the `href` attribute.

## Verify an Element has Specific Attribute

To check if an element has a specific attribute, we can use the `hasAttribute` method.

For instance, if we have:

```
<a href='http://example.com' title="example" data-foo='bar' class="example"></a>
```

Then we can check if it has a given attribute by writing:

```
const a = document.querySelector('a');
a.hasAttribute('title');
```

The method will return `true` if the attribute exists whether if it has a value or not.

## Getting a List of Class Attribute Values

We can use the `classList` property to get the values of the class attribute.

For instance, if we have:

```
<div class="foo bar baz"></div>
```

We can get the class names by writing:

```
const div = document.querySelector('div');
console.log(div.classList);
```

This will return each class’s name separately in an array-like object

There’s also the `className` property to return them all in one string:

```
console.log(div.className);
```

## Adding and Removing Subvalues in the class Attribute

The `classList` object has an `add` to add a class name to the class attribute.

It also has the `remove` method to remove it.

For instance, if we have:

```
<div class="foo"></div>​
```

Then we can write:

```
const div = document.querySelector('div');
div.classList.add('bar');
```

to add `bar` with `foo` .

and:

```
div.classList.remove('foo');
```

to remove `foo` and leave `bar` in the class attribute.

## Toggle a Class Attribute Value

`classList` also has a `toggle` method to toggle a class name.

For instance, if we have:

```
<div class="foo"></div>​
```

Then we can write:

```
const div = document.querySelector('div');
div.classList.toggle('foo');
```

to turn it off, and we can call `toggle` again with the same class name to add it back.

## Check if 2 Nodes are Identical

We can check if 2 nodes are identical according to the DOM 3 specification. According to the spec, for 2 nodes to be considered identical, the 2 nodes have to be of the same type.

The `nodeName`, `localName`, `namespaceURI`, `prefix` and `nodeValue` must have the same values.

The `NameNodeMaps` attribute must be equal. The `children` NodeList must also be equal.

Normalization may affect what entries are in `children` so that should be done before comparing them.

The `isEqualNode` method can do all the checks for us.

For instance, if we have:

```
<div id='foo'>
  <p>
    foo
  </p>
  <p>
    bar
  </p>
</div>
```

We can write:

```
const p = document.querySelectorAll('div > p')
console.log(p[0].isEqualNode(p[1]));
```

to check if both p elements are the same.

They aren’t since they have different content, so it logs`false` .

If we have:

```
<div id='foo'>
  <p>
    foo
  </p>
  <p>
    foo
  </p>
</div>
```

Then the same code logs `true` since the p elements are the same.

## Document Nodes

The `HTMLDocument` constructor inherits from `document` and represents a specific document node.

## Document Properties and Methods

Properties and methods of the `HTMLDocument` instance includes the following:

*   `doctype`
*   `documentElement`
*   `implementation`
*   `activeElement`
*   `body`
*   `head`
*   `title`
*   `lastModified`
*   `referrer`
*   `URL`
*   `defaultview`
*   `compatMode`
*   `ownerDocument`
*   `hasFocus()`

`doctype` has the doctype of the document.

`documentElement` has the whole document.

`implementation` has the `DOMImpkementation` object which has some methods that don’t depend on any particular document.

`activeElement` has the active element.

`body` has the body of the document.

`title` has the `title` element.

`lastModified` has the last modified date.

`referrer` has the URL that linked to the page.

`URL` is the URL of the current page.

`defaultView` refers to the `window` object associated with a document.

`compatMode` indicates whether a document is in quirks or standard mode,

`ownerDocument` has the top-level document object of the node.

`hasFocus` returns whether an element has focus.

## Getting General HTML Document Information

We can get general information about a document by writing the following:

```
const {
  title,
  URL,
  referrer,
  lastModified,
  compatMode
} = document;console.log(
  title,
  URL,
  referrer,
  lastModified,
  compatMode
)
```

We get general information from the `document` object itself.

## document Child Nodes

`document` can contain one `DocumentType` node object and one `Element` node object.

The `DocumentType` should be `<!doctype html>` for most documents.

The child element should be the `html` element itself.

We can use `document.childNodes` to get those elements.

## Shortcuts to DOCTYPE, html, head and body

The `document` object has properties to get those nodes directly.

`document.doctype` refers to `<!doctype html>` .

`document.documentElement` refers to the `<html>` element.

`document.head` refers to `<head>` , and `document.body` refers to `<body>` .

## Detecting DOM Specifications or Features

The `document.implement.hasFeatures` method lets us check if some feature is supported by the DOM API.

For instance, we can write:

```
document.implementation.hasFeature('Core','3.0');
```

to check if the DOM Core 3.0 specs are implemented in our browser.

The following features are supported:

*   Core — supported in version 1.0, 2.0, and 3.0
*   XML — 1.0, 2.0, 3.0
*   HTML — 1.0, 2.0
*   Views — 2.0
*   StyleSheets — 2.0
*   CSS — 2.0
*   CSS2–2.0
*   Events — 2.0, 3.0
*   UIEvents — 2.0, 3.0
*   MouseEvents — 2.0, 3.0
*   MutationEvents — 2.0, 3.0
*   HTMLEvents — 2.0
*   Range — 2.0
*   Traversal — 2.0
*   Validation — 3.0

We shouldn’t trust `hasFeature` to detect features.

`isSupported` can also do the same check together supported features for the supporting node:

```
element.isSupported(feature, version)
```

where `element` is the specific element we want to check for.

## Get Reference to he Focused/Active Node

We can use the `document.activeElement` property to get the element currently in focus.

## Check if the document or Any Node Inside it has Focus

We can call the `document.hasFocus()` method to check if any element is focused inside the page.

## document.defaultview

`document.defaultview` is the shortcut to the global JavaScript object in the browser.

This means that `document.defaultView` is the `window` object in the browser.

## Check if a Class Attribute Value has a Specific Value

We can use the `classList.contains` method to check if a class name is in the list of class names in the class attribute.

For instance, if we have:

```
<div class="foo bar baz"></div>​
```

Then we can write:

```
const div = document.querySelector('div');
console.log(elm.classList.contains('foo'));
```

Then it logs `true` since `foo` is in the class attribute.

## Getting and Setting data- Attributes

We can use the `datset` property to set any attribute that starts with `data-` .

For example, if we have:

```
<div data-foo-bar='foo'></div>​
```

Then we can write:

```
const div = document.querySelector('div');
console.log(elm.dataset.fooBar);
```

to return the value of `data-foo-bar` .

Anything with kebab case in HTML is transformed to camelCase.

To set it, we can write:

```
elm.dataset.baz = 'baz'
```

Then we get a `data-baz` attribute on the div with value `baz` .

## Selecting a Specific Element Node

The most common methods for getting a reference to single element node is `querySelector` or `getElementById` .

`querySelector` is used for getting a single element with any CSS selector.

For instance, we can write:

```
const div = document.querySelector('div');
```

to get the first div on the page,

We can use `getElementById` to get an element that has an `id` attribute set.

For example, if we have:

```
<p id='foo'>foo</p>
```

Then we can use `getElementById` to get the p element by writing:

```
const foo = document.getElementById('foo');
```

## Selecting or Creating a NodeList of Element Nodes

We can use the `querySelectorAll` , `getElementsByTagName` or `getElementsByClassName` to get multiple elements with a given selector, tag name, or class name respectively.

For instance, if we have:

```
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

Then we can use `querySelectorAll` to get all the li’s by writing:

```
const lis = document.querySelectorAll('li');
```

To use `getElementsByTagName` to do the same thing, we write:

```
const lis = document.getElementsByTagName('li');
```

Also, we can use the `getElementsByClassName` as follows to get the same elements:

```
const lis = document.getElementsByTagName('item');
```

`NodeList` s created from `getElementsByTagName` and `getElementsByClassName` are always live.

This means that they always reflect the state of the document even if the document is updated.

`querySelectorAll` doesn’t return a live list of elements.

It returns a snapshot of a document at the time it was created.

All the methods are also defined on the element node.

So we can chain them.

For example, we can write:

```
const lis = document.getElementById('list').getElementsByTagName('li');
```

We can pass in `'*'` to `querySelectorAll` or `getElementsByTagName` to get all elements on a page.

`childNodes` will also return a `NodeList` .

## Selecting All Immediate Child Elements Nodes

We can use `children` to select all child nodes of a given node.

If we have:

```
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

So we can get the li elements by writing:

```
const lis = document.querySelector('ul').children;
```

`children` gives us all the immediate elements nodes excluding other kinds of nodes.

They are returned in the order that they appear in the DOM.

## Contextual Element Selection

We can call `querySelector()` , `querySelectorAll()` , `getElementsByTagBName()` , and `getElementsByClassName()` on an element node.

For instance, if we have:

```
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

We can write:

```
const lis = document.querySelector('ul').getElementsByTagName('li');
```

to get the li elements.

## Preconfigured Selections/List of Element Nodes

There are many properties in the `document` object that can return select nodes without calling the methods above.

`document.all` returns all elements in an HTML document.

`document.forms` returns all the form elements in an HTML document.

`document.images` returns all img elements in the document.

`document.links` returns all `a` elements in the document.

`document.scripts` returns all script elements in a document.

`document.styleSheets` returns all link and style objects in an HTML document.

They return `HTMLCollection` objects, so they’re live.

`document.all` is created from the `HTMLAllCollection` constructor and isn’t supported in Firefox.

## Verify an Element will be Selected Using matches()

We can use `matches` to check if an element's selector matches one of the given element.

For example, if we have:

```
<ul>
  <li class="item">foo</li>
  <li class="item">bar</li>
  <li class="item">baz</li>
</ul>
```

We can call it by writing:

```
console.log(document.querySelector('.item').matches('li:first-child'));
```

It should return `true` since the first element with the class `item` is the same as the `li` .

## Creating Elements and Text Nodes

There are 2 methods to let us create nodes. One is the `createElement` to create element nodes. There’s also the `createTextNode` method to create a text node.

We can use the `createAttribute` method for creating attributes and `createComment` for creating comments.

To create an element, we can create one by writing:

```
const elementNode = document.createElement('div');
```

Then we create a div.

To create a text node, we write:

```
const textNode = document.createTextNode('hello');
```

## Creating and Adding Element and Text Nodes Using JavaScript Strings

We can add nodes by setting the `innerHTML` method with a string.

For instance, we can write:

```
document.getElementById('foo').innerHTML = '<strong>foo</strong>';
```

To put a node into the following div:

```
<div id="foo"></div>
```

We have the div with ID `foo` .

And setting the `innerHTML` property would create the `strong` element node and put it into the div.

To replace the enclosing node, we can write:

```
document.getElementById('foo').outerText = 'foo';
```

to replace the div with the text node `'foo'` .

The `insertAdjancentHTML` method only works with element nodes. It’s more precise than setting `innerHTML` or creating a new node.

For instance, if we have the following HTML:

```
<div id='foo'>
  <p>
    foo
  </p>
</div>
```

We can write:

```
const foo = document.getElementById('foo');foo.insertAdjacentHTML('beforebegin', '<p>bar</p>');
```

Then we add a p tag before the p element with the text `foo`. The position is the first argument and the content is the second argument.

Other positions include `'afterbwegin'`, `'beforeend'`, and `'afterend'`.

`innerHTML` will convert HTML elements found in the string to actual DOM nodes.

`textContent` can only construct text nodes.

## Extracting Parts of a DOM Tree as JavaScript Strings

`innerHTML`, `outerHTML`, and `textContent` are what we use to create and add nodes.

We can also use them to get the content.

For instance, if we have:

```
<div id='foo'>
  <p>
    foo
  </p>
</div>
```

Then we can write:

```
console.log(document.getElementById('foo').innerHTML);
```

to get the content of the div.

`innerText` will give us the text nodes. For instance, we can write:

```
console.log(document.getElementById('foo').innerText);
```

to get `foo` .

## Adding Node Objects to the DOM

`appendChild` and `insertBefore` can be used to add node objects to the DOM.

`appendChild` is for adding a child element to the given element.

`insetBefore` lets us add an element before the current element.

For example, we can use `appendChild` by writing:

```
const elementNode = document.createElement('p');
elementNode.innerText = 'hello';
document.getElementById('foo').appendChild(elementNode);
```

Given that we have the following HTML:

```
<div id='foo'>
  foo
</div>
```

We have added a new node after the text `foo` as a child node.

`insertBefore` takes 2 arguments. The first is the element to insert.

The 2nd is the element that we want to insert before the node in the first argument.

The node that we’re inserting before must be a child node of the node that we call `insertBefore` on.

So given the following HTML:

```
<div id='foo'>
  <p>
    foo
  </p>
</div>
```

We can insert an element before the p element by writing:

```
const elementNode = document.createElement('p');
elementNode.innerText = 'hello';
const foo = document.getElementById('foo')
foo.insertBefore(elementNode, foo.firstChild);
```

We created a p element with the p element and then we pass it into the `insertBefore` method.

`foo.firstChild` is the p element since the parent div is `foo`.

Then we get `hello` displayed before `foo`.

## Removing a Node with removeChild()

To remove a child element, we can use the `removeChild` method to remove a child element.

For instance, given the following HTML:

```
<div id='foo'>
  <p>
    foo
  </p>
</div>
```

We can write:

```
const p = document.querySelector('p');
p.parentNode.removeChild(p);
```

to remove the p element from the div.

We got the direct parent of the element we want to remove and then we can remove the element we want.

## Replacing a Child Element with replaceChild()

The `replaceChild` method works similarly to `removeChild` . We get the parent and then we call `replaceChild` to replace the item.

For instance, if we have:

```
<div id='foo'>
  <p>
    foo
  </p>
</div>
```

We can write:

```
const p = document.querySelector('p');
const bar = document.createTextNode('bar');
p.parentNode.replaceChild(bar, p);
```

to replace the p element with the text node with `bar` in it.

The first argument is the new node that we want to replace the existing node with.

The 2nd argument has the original node that we want to replace.

## Getting an elements offsetTop and offsetLeft Values

The `offsetTop` and `offsetLeft` to get the pixel value of an element node from the `offsetParent` .

The element node properties give us the distance in pixels from elements outside the top left border and inside the top left border of the `offserParent` .

`offsetParent` is determined by searching the nearest ancestor that has a CSS position that’s not static.

If none is found, then the `body` position is used for the values of `offsetParent` .

For instance, if we have a div inside the body:

```
<!DOCTYPE html>
<html>
  <head> </head>
  <body>
    <div></div>
  </body>
</html>
```

Then we can get the position of the div with:

```
const div = document.querySelector('div');console.log(div.offsetLeft);
console.log(div.offsetTop);
console.log(div.offsetParent);
```

We get `body` for `offsetparent` and numbers for the other properties.

## Get an Element’s Top, Right, Bottom, and Left Border Edge

The `getBoundingClientRect()` method gets the position of an element’s outside border edges relative to the top and left edge of the viewport.

For example, if we have:

```
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <div></div>
  </body>
</html>
```

We write:

```
const rect = document.querySelector('div').getBoundingClientRect();
console.log(rect);
```

Then we get the `top` , `left` , `right` , and `bottom` properties with the dimensions in pixels relative to the viewport.

## Getting an Element’s Size in the Viewport

The `getBoundingClientRect()` method also returns the `height` and `width` properties.

For instance, if we have:

```
<!DOCTYPE html>
<html>
  <head> </head>
  <body>
    <div></div>
  </body>
</html>
```

We write:

```
const rect = document.querySelector('div').getBoundingClientRect();console.log(rect);
```

And we get the `height` and `width` properties that have the total height and width including the padding and the borders together.

## Getting an Element’s Size in the Viewport Excluding Borders

The `clientHeight` and `clientWidth` have the size of the element excluding the border.

But the padding and content are included.

If we have:

```
<!DOCTYPE html>
<html>
  <head> </head>
  <body>
    <div></div>
  </body>
</html>
```

We can write:

```
const div = document.querySelector('div');console.log(div.clientHeight, div.clientWidth)
```

## Get the Topmost Element in Viewport at a Specific Point

`elementFromPoint()` gets a reference to the topmost element in an HTML document at a specific point in the document.

For instance, if we have:

```
<!DOCTYPE html>
<html>
  <head> </head>
  <body>
    <div></div>
  </body>
</html>
```

Then we can use it by writing:

```
console.log(document.elementFromPoint(10, 12));
```

and we get the `html` element.

## Get the Size of the Element Being Scrolled Using scrollHeight and scrollWidth

`scrollHeight` and `scrolLWidtgh` gives us the height and width of the node being scrolled.

For example, if we have an HTML that scrolls the `html` element, then we get the size of the `html` element, which is being scrolled.

If we have:

```
<p></p>
```

and:

```
p {
  height: 1000px;
  width: 1000px;
  background-color: green;
}
```

Then we get the width of the p element which is being scrolled by writing:

```
const p = document.querySelector('p');

console.log(p.scrollHeight, p.scrollWidth);
```

and we get 1000 for each property.

## Getting and Setting Pixels Scrolled from the Top and Left

`scrollTop` and `scrollLeft` are read-write properties that return the pixels to the left or top that aren’t currently viewable in the scrollable viewport because of scrolling.

For instance, if we have:

```
<p></p>
```

and:

```
p {
  height: 1000px;
  width: 1000px;
  background-color: green;
}
```

Then we can set them by writing:

```
const p = document.querySelector('p');
p.scrollTop = 750;
p.scrollLeft = 750;
```

Then we should see those values logged when we log them.

## Scrolling an Element into View

We can call the `scrollIntoView` method to scroll an item into view.

For instance, if we have:

```
for (let i = 0; i < 50; i++) {
  const p = document.createElement('p');
  p.innerText = i;
  document.body.appendChild(p);
}
```

to generate 50 p elements an attach them to the body, then we scroll the 41st one into view by writing:

```
document.querySelectorAll('p')[40].scrollIntoView(true);
```

## Style Attributes

DOM node objects have the `style` attribute which is used to style the elements of our choice.

It also returns the style of the element.

For instance, if we have:

```
<div></div>
```

Then we can get the styles by writing:

```
const styles = document.querySelector('div').style;
```

And then `styles` will have all the styles.

## Getting, Setting, and Removing Inline CSS Properties

We can set the CSS styles by using the `style` property.

For instance, if we have a div:

```
<div></div>
```

We can write:

```
const divStyle = document.querySelector('div').style;
divStyle.backgroundColor = 'yellow';
divStyle.border = '1px solid green';
divStyle.width = '200px';
divStyle.height = '200px';
```

Then we get a yellow box with a green border, with heights and widths 200px each.

CSS attributes that are kebab case are transformed to camelCase in JavaScript.

For instance, if we have `background-color` in CSS, then it’ll be `backgroundColor` in JavaScript.

This applies to all attributes with multiple words.

We can also use the `setProperty` method to set the styles and `getPropertyValue` to get them.

For instance, we can rewrite the code above with:

```
const divStyle = document.querySelector('div').style;
divStyle.setProperty('background-color', 'yellow');
divStyle.setProperty('border', '1px solid green');
divStyle.setProperty('height', '200px');
divStyle.setProperty('width', '200px');
```

Instead of setting the `style` property, we call `setProperty` instead.

To get the styles, we can use the `getPropertyValue` method:

```
console.log(divStyle.getPropertyValue('background-color'));
```

## Getting, Setting and Removing all Inline CSS Properties

We can use the `getAttribute` and `setAttribute` to get or set all CSS properties.

For instance, we can write:

```
const div = document.querySelector('div');
div.setAttribute('style', 'background-color: yellow; height: 200px; width: 200px');
```

Then we all the styles in the string by setting the `style` attribute of the div.

To get the styles, we can use `getAttribute` as follows:

```
console.log(div.getAttribute('style'));
```

## Getting an Element’s Computed Styles

We can get all the styles of an element with `getComputedStyle` .

It includes all the styles including inline styles, styles from stylesheets, and style tags.

For example, if we have:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <style>
      div {
        background-color: green;
        border: 1px solid yellow;
        height: 150px;
        width: 150px;
      }
     </style>
  </head>

  <body>
    <div style="background-color:orange;"></div>
   </body>
</html>
```

we can use it as follows:

```
const div = document.querySelector('div');
console.log(window.getComputedStyle(div).backgroundColor);
```

The inline styles override the other styles, so it’ll return `rgb(255, 165, 0)` which is orange.

It always return `rgb` format for colors.

## Apply and Remove CSS Properties Using class and id Attributes

We can put our styles in ID or class CSS selectors and apply the styles with it.

For instance, if we have a div:

```
<div></div>
```

and some CSS:

```
.foo{
  background-color: green;
  width: 100px;
  height: 100px;
}

#bar{
  border:10px solid red;
  width: 100px;
  height: 100px;
}
```

We can write:

```
const div = document.querySelector('div');
div.setAttribute('id','bar');
```

Then we get a box with a red border.

We can add the `foo` class to the div by writing:

```
const div = document.querySelector('div');
div.classList.add('foo');
```

Then the box will have a green background color added.

## Text Nodes

Text node in an HTML document are instances of the `Text` constructor.

They return text nodes.

For instance, if we have:

```
<p>hello</p>
```

Then we can get the text inside the p element as follows:

```
const hello = document.querySelector('p').firstChild;
```

## Text Objects and Properties

A `Text` instance has various objects and properties.

They have the following properties and methods:

*   `textContent` — content of the text node
*   `splitText` — split the text into 2 nodes by a specified offset
*   `appendData` — append data into the node
*   `deleteData` — delete data from the node
*   `insertData` — add data to the node at the position we want.
*   `replaceData` — replace data at the given position
*   `subStringData` — extracts part of the text from a text node
*   `normalize` — put the node and the child nodes unto a normalized form. This means removing empty nodes
*   `data` — returns the data of the node.
*   `createTextNode` — create a new text node

## White Space Create Text Nodes

White spaces create text nodes.

If they’re empty then the string will have spaces in it.

For instance, if we have:

```
<p> </p>
```

Then we write:

```
document.querySelector('p').firstChild.nodeName
```

Then we get `#text` , which indicates that it’s a text node.

## Add Event Listeners to Element Nodes

We can add event listeners to element nodes by using `addEventListener` .

For example, we can write:

```
window.addEventListener('mousemove', (e) => {
  console.log(e.clientX, e.clientY);
}, false);
```

to listen to the `mousemove` event and log the mouse coordinates as the mouse moves.

The same can be done to an element. If we have:

```
<button>
  click me
</button>
```

Then we can write:

```
const button = document.querySelector('button');

button.addEventListener('click', () => {
  console.log('clicked');
}, false);
```

to listen to clicks on the button.

## Remove Event Listeners

We can use `removeEventListenr` to remove event listeners if the original listener is a named function.

For instance, if we have:

```
<button>
  click me
</button>
```

Then we can write:

```
const button = document.querySelector('button');

const listener = () => {
  console.log('clicked');
  button.removeEventListener('click', listener);
}

button.addEventListener('click', listener, false);
```

to only log `'clicked'` on the first click.

This is because we called `removeListener` on the `button` ‘s `click` event to remove the listener once we called it once.

## Get Event Properties from the Event Object

We can get event properties from the event object.

It’s the first parameter of the listener.

For instance, we can write:

```
window.addEventListener('load', (event) => {
  console.log(event);
});
```

To log the `event` object, which has various properties.

It has many properties and the `stopPropgation` , `stopImmediatePropagation` , and `preventDefault` method.

`stopPropgation` stops event propagation to all ancestor elements.

`stopImmediatePropagation` stop other listeners of the same event from being called.

`preventDefault` stops the default action of the element from being run.

## Value of this Inside addEventListener

The value of `this` inside the event listener function that we pass into `addEventListener` is the reference to the node or object the event is attached to.

This only applies to traditional functions.

For instance, if we have a button:

```
<button>
  click me
</button>
```

Then if we write:

```
const button = document.querySelector('button');

button.addEventListener('click', function(event) {
  console.log(this);
});
```

`this` would the button that the listener is registered to.

We can use `event.currentTarget` to get the same reference.

It’s more reliable than `this` since that works with arrow functions as well.

## Referencing the target of an Event

We can use the `event.target` property to get the element that’s the target of the event.

This can be different from the node that the event is invoked on.

For instance, we can write:

```
document.body.addEventListener('click', (event) => {
  console.log(event.target);
}, false);
```

to get the element that’s clicked.

## Canceling Default Browser Events

We can cancel default browser events using `preventDefault` .

For instance, we can stop the default behavior of a link by using this method.

If we have the following HTML:

```
<a href="http://example.com">don't go</a>
```

Then we can stop users from going to [http://example.com](http://example.com) when users click on the link by writing:

```
document.querySelector('a').addEventListener('click', (event) => {
  event.preventDefault();
}, false);
```

The link will do nothing when we click it.

`preventDefault` doesn’t stop events from propagating either in the bubbling or capture phase.

Adding `return false` at the end of the event listener function body has the same result as `preventDefault` .

An event object has the `cancelable` property to indicate if an event will respond to `preventDefault` .

## Stop Event Flow

To stop events from flowing to ancestor elements or vice versa, we can use the `stopPropagation` method.

For instance, we can write:

```
const button = document.querySelector('button')

button.addEventListener('click', (e) => {
  e.stopPropagation();
}, false);
```

to stop propagation from the element where the event originated to the ancestor.

## Stop the Event Flow and Other Like Events on the Same Target

`stopImmediatePropagation` stops the event flow phase as well as any other like events attached to the event target that are attached after the event listener.

For instance, we can write:

```
const button = document.querySelector('button')

button.addEventListener('click', (e) => {
  e.stopImmediatePropagation();
}, false);
```

Then if we have:

```
const button = document.querySelector('button')

button.addEventListener('click', (e) => {
  e.stopImmediatePropagation();
}, false);

document.querySelector('button').addEventListener('click', () => {
  //...
}, false);

document.body.addEventListener('click', () => {
  //...
}, false);
```

None of the listeners below the first one will be called because we called `stopImmediatePropagation` in the first listener.

## DOM Event Types

There are many kinds of events that we can listen to.

The following are user events:

*   `load` — fired when something is loaded
*   `unload` — fires when a user agent removes the resource
*   `abort` — fires when a resource stopped from loading before it finished loading
*   `error` — fires when something fails to load
*   `resize` — fires when a document view has been resized
*   `scroll` —fires when user scrolls
*   `contextmenu` — fires by right-clicking and element

There are focus events:

*   `blur` — fires when an element loses focus by firing the most or pressing tab
*   `focus` — fires when an element receives focus
*   `focusin` — fires when an event target is about to receive focus but before focus is shifted
*   `focusout` — fires when an event target is about to lose focus

Form events include:

*   `change` — fires when control lose input focus
*   `reset` — fires when a form is reset
*   `submit` — fires when a form is submitted
*   `select` — fires when a user selects some text in a field

Mouse events include:

*   `click` — fires when a mouse pointer is clicked over an element
*   `dblclick` — fires when a mouse pointer is liked twice over an element
*   `mousedown` — fires when a mouse pointer is pressed over an element
*   `mouseenter` — fires when a mouse pointer is moved onto an element
*   `mouseleave` — fires when the mouse pointer is moved off of the boundaries of an element all of its children elements.
*   `mousemove` — fires when the mouse pointer is moved while it’s over an element
*   `mouseup` — fire when the mouse pointer is released over an element
*   `mouseover` — fires when the mouse pointer is moved over an element

Wheel events include:

*   `wheel` — fires when a mouse wheel is rotated

Keyword events include:

*   `keydown` — fires when a key is initially pressed
*   `keypress` — fires when a key is initially pressed
*   `keyup` — fires when a key is released

Touch events include:

*   `touchstart` — fires event to indicate when the user places a touchpoint on the touch surface
*   `touchend` — fires to indicate when a user removes a touchpoint from the touch surface
*   `touchmove` — fires when the user moves a touchpoint along the touch surface
*   `toucheneter` — fires when a touchpoint moves onto the interactive area defined by a DOM element
*   `touchleave` — fires to indicate when a touchpoint moves off the area defined by a DOM element
*   `touchcancel` — fires when a touchpoint is disrupted

Window /body events include:

*   `afterprint` — fire when something is printed
*   `beforeprint` — fires before something prints
*   `beforeunload` — fires before a document are unloaded
*   `hashchange` — fires when the part of the URL followed by `#` changes
*   `message` — fires when a user sends a message to a worker
*   `offline` — fires when the browser is offline
*   `online` — fires when the browser is online
*   `pagehide` — fires when traversing from a session history entry
*   `pageshow` — fired when traveling from a session history entry

Document events include:

*   `readystatechange` — fires when the ready state is changed
*   `DOMContentLoaded` — firs when a webpage is loaded but before all resources are downloaded

Drag events include:

*   `drag` — fires when the source object is dragged
*   `dragstart` — fires when the source object begins to be dragged
*   `dragend` — fires on the source object when the user releases the mouse on the dragged object
*   `dragenter` — fires when the dragged element enters the drop target
*   `dragleave` — fires hen the object moves to the drop target
*   `dragover` — fires when the object is dragged over a drop target
*   `drop` — fires when the object is dropped

## Event Flow

Events propagate through the DOM.

They go from the originating element all the way to the root element object. This is called the bubbling phase

Therefore. when we register listeners on the ancestor objects, they’ll also run.

There’s also the capture phase, which is the reverse of the bubbling phase.

## Custom Events

We can emit custom events in our JavaScript code.

Th do that we can use the `createEvent` method and then use `addEventListener` to listen to the event.

For instance, if we have a button:

```
<button>
  click me
</button>
```

We can write:

```
const button = document.querySelector('button');
const customEvent = document.createEvent('CustomEvent');
button.addEventListener('hello', (event) => {
  console.log(event.detail.foo)
}, false);

customEvent.initCustomEvent('hello', true, false, {
  foo: 'bar'
});

button.dispatchEvent(customEvent);
```

We called `createEvent` to create a custom event. We pass in `'CustomEvent'` to create a custom event.

Then we called `initCustomEvent` to initialize the custom event with data.

Next, we called `dispatchEvent` to trigger the event.

Then in the event handler we passed into `addEventListener` , we log the data which in the `detail` property.

So we get `'bar'` when we access the `foo` property.

## Simulating or Trigger Mouse Events

We can trigger mouse events by using the `initMouseEvent` method.

For instance, if we have:

```
<button>
  click me
</button>
```

We can write:

```
const button = document.querySelector('button');
button.addEventListener('click', (event) => {
  console.log(event);
}, false);

const simulatedClick = document.createEvent('MouseEvents');

simulatedClick.initMouseEvent('click', true, true, document.defaultView, 0, 0, 0, 0, 0, false, false, false, 0, null, null);

button.dispatchEvent(simulatedClick);
```

We called `createEvent` with the `'MouseEvents'` .

Then we call the `initMouse` event with it. It takes many arguments.

They the arguments are in the following order:

*   `type` — type of mouse event we want to trigger
*   `canBubble` — indicates whether the event bubbles or not
*   `cancelable` — indicates whether the event is cancelable or not
*   `view` — the abstract view of the event, which should be `window`
*   `detail` — click count
*   `screenX` — the event’s x coordinate
*   `screenY` — the event’s y coordinate
*   `clientX` — the event client’s x coordinate
*   `clientY` — the event client’s y coordinate
*   `ctrlKey` — whether the Ctrl key is pressed during the event
*   `altKey` — whether the Alt key is pressed during the event
*   `shiftKey` — whether the Shift key is pressed during the event
*   `metaKey` — whether the meta (Windows / Command) key is pressed during the event
*   `button` — mouse button
*   `relatedTarget` — related event target

This is a deprecated API so other solutions should be considered.

## Event Delegation

We can use one event handler to listen to events originating from a different sources.

For instance, if we have:

```
<button>
  button 1
</button>
<button>
  button 2
</button>
<button>
  button 3
</button>
```

We can write:

```
document.addEventListener('click', (event) => {
  if (event.target.tagName.toLowerCase() === 'button') {
    console.log(event.target.textContent);
  }
}, false);
```

We listen to the click event on the whole page with `document.addEventListener` .

Then get the element where the event originated with `event.target` .

If we clicked a button, then we log the text content.

## CSSStyleRule Overview

A `CSSStyleRule` object represents each CSS rule in a style sheet,

It’s the interface to the CSS properties and values attached to the selector.

To access them, if we have:

```
<style id='styles'>
  body {
    background-color: orange;
    margin: 20px;
  }

  p {
    font-weight: 20px;
    color: blue;
  }
</style>
```

Then we can write:

```
const styles = document.querySelector('#styles');
console.dir(styles.sheet.cssRules);
```

to get the CSS rules from the `style` element.

## CSSStyleRule Properties and Methods

A `CSSStyleRule` has properties and methods of its own.

It has the following properties:

*   `cssText` — the text of the CSS rule
*   `parentRule` — the rule that’s the parent of the given style block
*   `parentStylesSheet` — parent style sheet object
*   `selectorText` — the selector for the rule
*   `style` — the style for the rule
*   `type` — the type of rule, which is CSS rule, and the value is 1

For instance, we can write:

```
const styles = document.querySelector('#styles');
console.dir(styles.sheet.cssRules[0].cssText);
```

Then we get the styles for the body element since that’s the first entry.

## Getting a List of CSS Rules in a Style Sheet

The `cssRules` has the list of CSS rules of the style sheet.

For instance, if we have the same style elements as the previous example, we write:

```
const styles = document.querySelector('#styles');
console.dir(styles.sheet.cssRules);
```

to get all the `cssRules` .

## Inserting or Deleting CSS Rules

`insertRule` lets us insert a CSS rule in the style sheet.

`deleteRule` lets us remove them.

For example, if we have a style element:

```
<style id='styles'>
  body {
    background-color: orange;
    margin: 20px;
  }

  p {
    font-weight: 20px;
    color: blue;
  }
</style>
```

We can write:

```
const styles = document.querySelector('#styles');
styles.sheet.insertRule('p { color:green }', 1);
```

Then we added a new CSS rule for p tags, which is overridden by the existing rule.

We can delete the old rule by writing:

```
styles.sheet.deleteRule(1);
```

Now our new rule is the rule for p elements on the page.

All we did is to pass in the index for the rule to remove.

## Editing the Value of a CSSStyleRule

We can assign a value to the `style` property to change the style value.

For example, if we have:

```
<style id='styles'>
  body {
    background-color: orange;
    margin: 20px;
  }

  p {
    font-weight: 20px;
    color: blue;
  }
</style>
<p>
  foo
</p>
```

We can write:

```
const styles = document.querySelector('#styles');
styles.sheet.cssRules[1].style.color = 'green';
```

to set the p elements’ color to green.

## Create a New Inline CSS Style Sheets

We can add new styles to a style element by using the `innerHTML` property.

For example, if we have:

```
const style = document.createElement('style');
style.innerHTML = 'body { color: orange }';document.querySelector('head').appendChild(style);
```

Now all the content of the body will be orange since we have a style element with that style added.

## Add External Style Sheets Programmatically

Adding external style sheets programmatically can be done as we did with adding style tags.

To do it, we just use `createElement` :

```
const link = document.createElement('link');
link.setAttribute('rel', 'stylesheet');
link.setAttribute('type', 'text/css');
link.setAttribute('id', 'link');
link.setAttribute('href', 'https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css');
```

We added a new link element with the Bootstrap stylesheet.

## Disabling or Enabling Stylesheets

`disabled` property is a property that we can set on stylesheets to toggle on and off stylesheets.

If we have a link element:

```
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
```

Then we can toggle on or off by writing:

```
document.querySelector('link').disabled = true;
```

Now we disabled it. To enable it, we can write:

```
document.querySelector('link').disabled = false;
```

## Inserting and Running JavaScript

We can insert JavaScript into an HTML document.

JavaScript code are always inside script tags as an external file or inline code.

script elements don’t have any required attributes.

Self-closing script tags should also be avoided.

Trying to include an external script file that manipulates a script element on the page will result in the one on the page being ignored.

For instance, we can write:

```
<script>
console.log('hello');
</script>
```

to include a script tag.

## JavaScript Loads Synchronously

The default option for loading scripts is to load them synchronously.

This means that they’ll block the rendering and downloading of other scripts if they exist.

If a script is eternal to the document is blocking the loading of everything else, then the script has to be downloaded first before parsing, which means it’ll be slower.

## Opening Popup Windows

We can open popup windows with the `window.open` method.

For example, we can write:

```
const monkeyWindow = window.open();
```

To add some content to the window, we can write:

```
const monkeyWindow = window.open();
const windowContent = `<h1>hello world</h1>`;
monkeyWindow.document.write(windowContent);
```

We call `document.write` on the `monkeyWindow` to show the content.

Also, we can show the content of a URL with the `location.assign` method:

```
const monkeyWindow = window.open();
monkeyWindow.location.assign("https://www.google.com");
```

Now we should see Google displayed in the new window.

We can also write:

```
const monkeyWindow = window.open();
monkeyWindow.location.href = "https://www.google.com";
```

to do the same thing.

To close a window, we can write:

```
const monkeyWindow = window.open();
monkeyWindow.location.href = "https://www.google.com";
monkeyWindow.close();
```

## Controlling the Window’s Size and Location

We can set the popup window’s size and location with a string in the 3rd argument of `window.open` .

For example, we can write:

```
const monkeyWindow = window.open("https://www.google.com", "win1", "width=420,height=380");
```

Now the window is 420px in width and 380px for height.

To change its location, we can write:

```
const monkeyWindow = window.open("https://www.google.com", "win1", "width=420,height=380,left=200,top=100");
```

to add the `left` and `top` keys to set the position.

## Form Validation

We can add form validation to a form.

For example, we can write the following HTML:

```
<form onSubmit="return checkForLastName();">
  Please enter your last name.<br>
  <input type="text" id="lastNameField">
  <input type="submit" value="Submit">
</form>
```

And we can add the following JavaScript to add the validation:

```
const checkForLastName = () => {
  if (document.getElementById("lastNameField").value.length === 0) {
    alert("Please enter your last name");
    return false;
  }
}
```

In the `checkForLastName` function, we get the value of the input with the ID `lastNameField` .

If the `value` ‘s `length` is 0, then we show the alert.

The `return` in the `onSubmit` attribute value makes sure that we prevent the default submit behavior along with the `return false` in `checkForLastName` so that we can run the JavaScript validation.

To improve the user experience, we can call `focus` on the element:

```
const checkForLastName = () => {
  const lastNameField = document.getElementById("lastNameField")
  if (lastNameField.value.length === 0) {
    alert("Please enter your last name");
    lastNameField.focus();
    return false;
  }
}
```

We call `focus` on the input element so that the user can type in the text without clicking on the input.

Also, we can add background color so that the user can see the input field more easily:

```
const checkForLastName = () => {
  const lastNameField = document.getElementById("lastNameField")
  if (lastNameField.value.length === 0) {
    alert("Please enter your last name");
    lastNameField.focus();
    lastNameField.style.background = "yellow";
    return false;
  }
  lastNameField.style.background = "white";
}
```

We set the background color by setting the `lastNameField.style.background` property.

## Dropdown Validation

We can add validation to select dropdown fields.

For example, we can write the following HTML:

```
<form onSubmit="return checkForSelection();">
  <select id="fruits">
    <option value="" selected="selected">
      SELECT A FRUIT</option>
    <option value="apple">apple</option>
    <option value="orange">orange</option>
    <option value="grape">grape</option>
  </select>
  <br>
  <input type="submit" value="Submit Form">
</form>
```

And then add the following JavaScript:

```
const checkForSelection = () => {
  if (document.getElementById("fruits").selectedIndex === 0) {
    alert("Please select a fruit.");
    return false;
  }
}
```

We added a select element and when we click on Submit Form, the `checkForSelection` function is run.

We add the `return` keyword so that we stop the default submit behavior and let the `checkForSelection` run.

## Radio Button Validation

Also, we can add validation to a group of radio buttons.

For instance, we can write the following HTML:

```
<form onSubmit="return validateRadios();">
  <input type="radio" name="r1" value="apple"> apple<br>
  <input type="radio" name="r1" value="orange"> orange<br>
  <input type="radio" name="r1" value="grape"> grape<br>
  <input type="submit" value="Submit Form">
</form>
```

And the following JavaScript:

```
const validateRadios = () => {
  const radios = document.getElementsByName("r1");
  for (const r of radios) {
    if (r.checked) {
      return true;
    }
  }
  alert("Please check one.");
  return false;
}
```

We have a form with a bunch of radio buttons with the same `name` attribute value.

They should have the same name so that they’re considered to be in the same group.

When we click the Submit Form button, the `validateRadios` function runs.

In the function, we get all the radio buttons by calling `getElementsByName` with the `name` attribute value of the radio buttons.

We loop through the radio buttons with the for-of loop.

Then if one is checked, we return `true` .

Otherwise, we show an alert and return `false` is none of them are checked.

## Email Validation

We can validate email address in a form field by checking the format of the entered text with a regex.

For example, we can write the following HTML:

```
<form onSubmit="return validateEmail();">
  Please enter your email.<br>
  <input type="text" id="emailField">
  <input type="submit" value="Submit">
</form>
```

And write the following JavaScript code:

```
const validateEmail = () => {
  const emailField = document.getElementById("emailField");
  const regex = /^[w-.+]+@[a-zA-Z0-9\. -]+.[a-zA-z0-9]{2,4}$/;
  if (!(regex.test(emailField.value))) {
    alert("Please correct email address");
    return false;
  }
}
```

We have the `validateEmail` function that gets the value of the input with ID `emailField` .

Then we call the `regex.test` method to check if the inputted value matches the regex format.

If it doesn’t then we show an alert and return `false` .

The `return` keyword lets us prevent the default submit behavior from running.

## Handling Events

We can attach event listeners to HTML elements.

For example, we can write the following HTML:

```
<input type="button" value="Click" id='button1'>
```

And write the following JavaScript:

```
const b1 = document.getElementById("button1");
const sayHello = () => {
  alert('hello');
}
b1.onclick = sayHello;
```

We get the button with `getElementById` .

Then we set the `onclick` property to the `sayHello` event handler function.

The functions show an alert with the `alert` function.

Now when we click on the button, we show the alert.

# jQuery

jQuery is a popular JavaScript for creating dynamic web pages.

In this section, we’ll look at how to using jQuery in our web apps.

## Adding jQuery

We can add jQuery by adding a script tag:

```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```

We can also install the `jquery` package by running:

```
npm install jquery
```

with NPM or:

```
yarn add jquery
```

Also, we can install it with Bower:

```
bower install jquery
```

After installing it, we can start using it.

## .add()

The `.add()` method lets us get a child element from a parent.

For example, if we have:

```
<p>
  <div>
    foo
  </div>
</p>
```

Then we call:

```
$("p").add("div").addClass("widget");
```

to get the `div` that’s inside the `p` element.

Then we call `addClass` to add a class to the `div` inside the `p` element.

## .addBack()

The `.addBack()` method lets us get the child elements from the parent element.

For example, if we have the following HTML:

```
<div class="after-addback">
  <p>First Paragraph</p>
  <p>Second Paragraph</p>
</div>
```

and the following CSS:

```
.background {
  background: yellow;
}
```

Then we get the `p` elements in the `div` .

Then we use `addBack` to get the `div` again.

And finally, we call `addClass` to add the `background` class.

## .addClass()

The `.addClass()` method lets us add one or more classes to an element.

For example, we can write:

```
$("p").addClass("myClass yourClass");
```

to add the `myClass` and `yourClass` classes to the `p` element.

## .after()

The `.after()` method inserts content after each element in the set of matched elements.

For example, if we have the following HTML:

```
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we get the item with the `inner` class and add the HTML TO it by writing:

```
$(".inner").after("<p>Test</p>");
```

## .ajaxComplete()

The `.ajaxComplete()` lets us add a callback that’s called when the Ajax request is completed.

For example, we can write:

```
$(document).ajaxComplete(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

We called `ajaxComplete` with the callback that’s called when we make a request with `$.ajax` .

Then we call `$.ajax` to make the Ajax request.

`settings` has the `url` property with the request URL.

The `settings.type` property has the request method name.

`xhr` has the XHR object. The `readyState` property has the ready state.

## .ajaxError()

The `.ajaxError()` method lets us add a callback that’s called when there’s an error.

For example, we can use it by writing:

```
$(document).ajaxError(function(event, xhr, settings, thrownError) {
  console.log(event, xhr, settings, thrownError)
});

$.ajax({
  url: "bad-url",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

We have an invalid URL set as the value of the `url` property.

Then the `ajaxError` callback will be called.

It has the `thrownError` parameter which isn’t in the `ajaxComplete` callback.

## .ajaxSend()

The `ajaxSend` method lets us add a callback that’s called when the request is sent.

For example, we can write:

```
$(document).ajaxSend(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

We have the same callback as the other ajax methods.

And the content is the same.

## .ajaxStop()

The `.ajaxStop()` method lets us add a callback that’s called when the Ajax request is done.

For example, we can write:

```
$(document).ajaxStop(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

We passed in a callback with the `event` , `xhr` , and `settings` parameter.

`settings` has the request data like the URL and request method.

`xhr` is an object with the request state.

## .ajaxSuccess()

The `.ajaxSuccess()` method lets us add a callback that’s run when an Ajax request completes successfully.

For example, we can write:

```
$(document).ajaxSuccess(function(event, xhr, settings) {
  console.log(event, xhr, settings)
});

$.ajax({
  url: "https://yesno.wtf/api",
  context: document.body
}).done(function() {
  $(this).addClass("done");
});
```

We have a callback with the same parameters as the other Ajax methods.

## All Selector

We can get all elements within another element with the `*` selector.

For example, if we have:

```
<div id="test">
  <div>DIV</div>
  <span>SPAN</span>
  <p>P <button>Button</button></p>
</div>
```

Then we can get all the elements inside the `div` with ID `test` by writing:

```
$("#test").find("*").css("border", "3px solid red")
```

Then we call `css` to add a red border in all the elements.

## .animate()

The `.animate()` method lets us perform custom animation of a set of CSS properties.

For example, if we have the following HTML:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/25/300/300.jpg?hmac=hXirsaKumNCLu7iGSrMI_RkAEfXF01DGx6c4wzBUpXs" alt="" width="100" height="123"
  style="position: relative; left: 10px;">
```

We can add an animation to the when we click on Click here by writing:

```
$("#clickme").click(function() {
  $("#book").animate({
    opacity: 0.25,
    left: "+=50",
    height: "toggle"
  }, 5000, function() {
    // Animation complete.
  });
});
```

We get the div with ID `clickme` , then we call `click` to listen to clicks on it.

Then we call `animate` to animate the image by changing the `left` property.

## :animated Selector

We can select the element that’s animated with the `:animated` selector.

For example, if we have the following HTML:

```
<button id="run">Run</button>

<div></div>
<div id="mover"></div>
<div></div>
```

And the following CSS:

```
div {
   background: yellow;
   border: 1px solid #AAA;
   width: 80px;
   height: 80px;
   margin: 0 5px;
   float: left;
 }

div.colored {
   background: green;
}
```

Then we can toggle the color of the animate div, which has the ID `mover` by writing:

```
$("#run").click(function() {
  $("div:animated").toggleClass("colored");
});

function animate() {
  $("#mover").slideToggle("slow", animate);
}

animate();
```

When we click Run, the `toggleClass` method is called to change its color.

## .append()

We can use the `.append` method to add elements after another element.

For example, if we have:

```
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we can get the elements with the `inner` class by writing:

```
$(".inner").append("<p>Test</p>");
```

Then both divs will have `<p>Test</p>` HTML attached to it.

## .attr()

The `.attr()` method lets us get or set an attribute for every matched element.

For example, if we have:

```
<p>Once there was a <em title="huge, gigantic">large</em> cat</p>
<div></div>
```

Then we can get the `title` attribute from the `em` element and put that in the `div` by writing:

```
const title = $("em").attr("title");
$("div").text(title);
```

We can also use it to set the `title` attribute:

```
const title = $("em").attr("title", "big");
```

## Attribute Contains Prefix Selector [name|=”value”]

We can get elements by the attribute and name and value. `|` will get the value equal to the given string or the string followed by a hyphen.

For example, if we have:

```
<a href="example.html" hreflang="en">Some text</a>
```

Then we can get this element by writing:

```
$("a[hreflang|='en']").css("border", "3px dotted green");
```

`hreflang` is the attribute name and `'en'` is the value.

## Attribute Contains Selector [name*=”value”]

This selector selects elements that have specified attribute with a value having a given substring.

For example, if we have the following HTML:

```
<input name="man-news">
<input name="milkman">
<input name="letterman2">
<input name="newmilk">
```

Then we get all the inputs with the `name` attribute having the `man` substring as the value by writing:

```
$("input[name*='man']").val("has man");
```

Now the value of the first 3 input boxes are `'has man'` .

## Attribute Contains Word Selector [name~=”value”]

We can get the elements that have a specified attribute with a value containing the given word, delimited by spaces.

For example, if we have:

```
<input name="man-news">
<input name="milk man">
<input name="letterman2">
<input name="newmilk">
```

Then we can write:

```
$("input[name~='man']").val("has man");
```

to get the inputs with the `name` attribute with the word `man` in it separated by a space.

Only the 2nd input meets that condition, so `has man` will be in that input.

## Attribute Ends With Selector [name$=”value”]

We can get elements that have the specified attribute with a value ending with the given string.

For example, if we have the following HTML:

```
<input name="newsletter">
<input name="milkman">
<input name="jobletter">
```

Then we use this selector by writing:

```
$("input[name$='letter']").val("a letter");
```

We get all the inputs with the `name` attribute with values ending with `letter` .

Then the first 2 inputs are filled with `a letter` by calling `val` .

## Attribute Equals Selector [name=”value”]

We can get the elements with the attribute equal to a value with this selector.

For example, if we have the following HTML:

```
<div>
  <label>
    <input type="radio" name="newsletter" value="Hot Fuzz">
    <span>name?</span>
  </label>
</div>
<div>
  <label>
    <input type="radio" name="newsletter" value="Cold Fusion">
    <span>value?</span>
  </label>
</div>
<div>
  <label>
    <input type="radio" name="newsletter" value="Evil Plans">
    <span>value?</span>
  </label>
</div>
```

We get the `span` with the `value` set to `Hot Fuzz` and populate the name by text content by writing:

```
$("input[value='Hot Fuzz']").next().text("Hot Fuzz");
```

Now the first radio button should have the text Hot Fuzz beside it.

## Attribute Not Equal Selector [name!=”value”]

We can use this selector to select an attribute that doesn’t equal to the given value.

For example, if we have the following HTML:

```
<div>
  <label>
    <input type="radio" name="newsletter" value="Hot Fuzz">
    <span>name?</span>
  </label>
</div>
<div>
  <input type="radio" value="Cold Fusion">
  <span>no name</span>
</div>
<div>
  <label>
    <input type="radio" name="newsletter" value="Evil Plans">
    <span>value?</span>
  </label>
</div>
```

Then we can get the radio button that doesn’t have `name` attribute set to `newsletter` and add text to the span beside it by writing:

```
$("input[name!='newsletter']").next().append("<b>; not newsletter</b>");
```

Now the second radio button has:

```
no name**; not newsletter**
```

beside the radio button.

## Attribute Starts With Selector [name^=”value”]

This selector let us select elements that have the specified attribute with a value starting exactly with a given string.

For example, if we have:

```
<input name="newsletter">
<input name="milkman">
<input name="newsboy">
```

Then we get all the inputs with the `name` attribute starting with `news` and setting the value for them by writing:

```
$("input[name^='news']").val("news here!");
```

Therefore, the first and last inputs will have the `news here` input added.

## .before()

The `.before()` method lets us insert content before each element in the set of matched elements.

For example, if we have:

```
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">foo</div>
  <div class="inner">bar</div>
</div>
```

Then we can add an elements before each div with class `inner` by writing:

```
$(".inner").before("<p>Test</p>");
```

Then we get:

```
Test

foo

Test

bar
```

displayed.

## .bind()

The `.bind()` method lets us add a handler to an event for the elements.

For example, if we have the following HTML:

```
<div id="foo">
  foo
</div>
```

We can add a click listener to it by writing:

```
$("#foo").bind("click", function() {
  alert("User clicked on 'foo.'");
});
```

The first argument is the event name.

The 2nd argument is the callback that’s run when the event is triggered.

## .blur()

The `.blur()` method binds an event handler to the `blur` JavaScript event.

For example, if we have the following HTML:

```
<form>
  <input id="target" type="text" value="Field 1">
  <input type="text" value="Field 2">
</form>
```

Then we can listen to the `blur` event on the input field with ID `target` by writing:

```
$("#target").blur(function() {
  alert("Handler for .blur() called.");
});
```

We get the element and then pass in the callback to show an alert when we move away from the first input.

## :button Selector

The `:button` select selects all button elements and elements with `type` set to `button` .

For example, if we have the following HTML:

```
<form>
  <fieldset>
    <input type="button" value="Input Button">
    <input type="checkbox">

    <input type="file">
    <input type="submit">
    <input type="text">
    <select>
      <option>Option</option>
    </select>

    <textarea></textarea>
    <button>Button</button>
  </fieldset>
</form>
```

And the following CSS:

```
.marked {
  background-color: yellow;
  border: 3px red solid;
}
```

Then we can get the buttons and add the `marked` class to them by writing:

```
const input = $(":button").addClass("marked");
console.log(input.length)
```

The input with type set to `button` and the `button` element will be selected.

## callbacks.add()

The `callbacks.add` method lets us add callbacks to a callback list.

For example, we can write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const bar = function(value) {
  console.log(`bar: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.add(bar);
callbacks.fire("world");
```

We call the `$.Callbacks` method to get a list of callbacks.

Then we call the `add` method to add the `foo` and `bar` methods to add to the callback list.

The `callbacks.fire` method will call each callback on the list with the given argument.

Therefore, we get:

```
foo: hello
foo: world
bar: world
```

from the console log.

## callbacks.disable()

We can call `callbacks.disable` to disable a callback.

For example, if we have:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.disable();
callbacks.fire("world");
```

Then we call `callbacks.disable` to stop the list of callbacks from being called again.

Therefore, we only see:

```
foo: hello
```

logged.

## callbacks.disabled()

We can use the `callbacks.disabled()` method to check if callbacks have been disabled.

For example, we can write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.disable();
console.log(callbacks.disabled());
callbacks.fire("world");
```

Since we called `callbacks.disable` , `callbacks.disabled` should log `true` .

## callbacks.empty()

The `callbacks.empty()` method removes all callbacks from the list.

For example, we can write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const bar = function(value) {
  console.log(`bar: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.add(bar);
callbacks.empty();
console.log(callbacks.has(foo));
console.log(callbacks.has(bar));
```

Since we called `callbacks.empty` to remove all callbacks, then both console logs should log `false` since both callbacks have been removed by `empty` .

## callbacks.fire()

The `callbacks.fire()` method lets us call all callbacks on the list with the given argument.

For example, we can write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const bar = function(value) {
  console.log(`bar: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.fire("world");
callbacks.add(bar);
callbacks.fire("hello again");
```

We added the `foo` callback and called `fire` with `'hello'` and `'world'` , so we should get:

```
foo: hello
foo: world
```

logged.

Then we added `bar` to the callbacks list and called `fire` with `'hello again'` .

So we get:

```
foo: hello again
bar: hello again
```

logged.

## callbacks.fired()

We can check is the callback has been fired at least once with the `callbacks.fired()` method.

For example, we can write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.fire("world");
console.log(callbacks.fired());
```

to log is any callbacks have been called with `fired` .

Since it’s been called, it should log `true` .

## callbacks.fireWith()

The `callbacks.fireWith()` method lets us call a callback with the given context and arguments.

For example, if we have:

```
const log = function(value1, value2) {
  console.log(this, value1, value2);
};

const callbacks = $.Callbacks();
callbacks.add(log);
callbacks.fireWith(window, ["foo", "bar"]);
```

Then `this` is `window` , `value1` is `foo` and `value2` is `bar` .

## callbacks.has()

The `callbacks.has()` method lets us check whether the callbacks list has any callbacks attached.

For example, we can write:

```
const log = function(value1, value2) {
  console.log(this, value1, value2);
};

const callbacks = $.Callbacks();
callbacks.add(log);
console.log(callbacks.has(log));
```

The console log should log `true` since we added it with `add` .

## callbacks.lock()

The `callbacks.lock()` method locks the callbacks list in its current state.

For example, we can use it by writing:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.lock();
callbacks.fire("world");
```

We call the `callbacks.lock` method to prevent any callbacks from being called.

So we only have:

```
foo: hello
```

logged.

## callbacks.locked()

We can use the `callbacks.locked()` method to check if the callbacks list has been locked.

For example, if we write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.lock();
console.log(callbacks.locked());
```

Then the last console log should be `true` since we called `lock` to lock the callbacks list.

## callbacks.remove()

We can remove a callback with the `callback.remove` method.

For example, we can write:

```
const foo = function(value) {
  console.log(`foo: ${value}`);
};

const callbacks = $.Callbacks();
callbacks.add(foo);
callbacks.fire("hello");
callbacks.remove(foo);
callbacks.fire("world");
```

We called `remove` on `foo` to remove `foo` from the callbacks list.

Therefore, then 2nd `fire` callback won’t call `foo` .

## .change()

The `.change()` method binds an event handler to the `change` JavaScript event.

It can also be used to trigger an the `change` event on an element.

For example, if we have the following HTML:

```
<form>
  <input class="target" type="text" value="Field 1">
  <select class="target">
    <option value="option1" selected="selected">Option 1</option>
    <option value="option2">Option 2</option>
  </select>
</form>
```

Then we can listen to the `change` event triggered on the elements with the class `target` by writing:

```
$(".target").change(function() {
  alert("Handler for .change() called.");
});
```

We can also trigger the change ebent on the element.

For example, if we have the following HTML:

```
<form>
  <input class="target" type="text" value="Field 1">
  <select class="target">
    <option value="option1" selected="selected">Option 1</option>
    <option value="option2">Option 2</option>
  </select>
</form>
<div id="other">
  click me
</div>
```

Then we can add a click listen to the div with ID `other` .

When we click the div, we can trigger by `change` event on all the elements with class `target` by writing:

```
$(".target").change(function() {
  alert("Handler for .change() called.");
});

$("#other").click(function() {
  $(".target").change();
});
```

Now when we click the click me button, we’ll see the alert pop up for each element with class `target` .

## :checkbox Selector

The `:checkbox` selector lets us select all elements with type `checkbox` .

For example, if we have the following HTML:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">

  <input type="checkbox">
  <input type="file">
  <input type="hidden">
   <input type="password">
  <input type="radio">

  <input type="reset">
  <input type="submit">
  <input type="text">

  <select>
    <option>Option</option>
  </select>

  <textarea></textarea>
  <button>Button</button>
</form>
```

Then we can highlight all the checkboxes by writing:

```
$("form input:checkbox")
  .wrap("<span></span>")
  .parent()
  .css({
    background: "yellow",
    border: "3px red solid"
  });
```

We get the checkboxes with the `:checkbox` selector and set the background and border of all the selected elements.

## :checked Selector

We can get all the checked checkboxes with the `:checked` selector.

For example, if we have the following HTML:

```
<form>
  <p>
    <input type="checkbox" name="newsletter" value="Hourly" checked="checked">

    <input type="checkbox" name="newsletter" value="Daily">
    <input type="checkbox" name="newsletter" value="Weekly">

    <input type="checkbox" name="newsletter" value="Monthly" checked>
    <input type="checkbox" name="newsletter" value="Yearly">
  </p>
</form>
```

Then we can highlight the checked checkboxes by writing:

```
$("input:checked")
  .wrap("<span></span>")
  .parent()
  .css({
    background: "yellow",
    border: "3px red solid"
  });
`

## Child Selector (“parent > child”)

We can get the child elements with this selector.

For example, if we have the following HTML: 
```

*   Item 1
*   Item 2
    *   Nested item 1
    *   Nested item 2
    *   Nested item 3
*   Item 3

```

We get the `ul` with the class `topnav` ‘s `li` elements bu writing:

```
$("ul.topnav > li").css("border", "3px double red");
```

We call `css` to add a border to all the matched elements.

## .children()

We can get the child elements of a selected element with the `children` method.

For example, if we have the following HTML:”

```
<ul class="topnav">
  <li>Item 1</li>
  <li>Item 2
    <ul>
      <li>Nested item 1</li>
      <li>Nested item 2</li>
      <li>Nested item 3</li>
    </ul>
  </li>
  <li>Item 3</li>
</ul>
```

Then we get all the child elements of the `ul` by writing:

```
$("ul.topnav").children().css("background-color", "red");
```

We called `css` to make the background red.

## Class Selector (“.class”)

We can select items with the class selector.

For example, if we have the following HTML:

```
<div class="notMe">div class="notMe"</div>
<div class="myClass">div class="myClass"</div>
<span class="myClass">span class="myClass"</span>
```

Then we can highlight the elements with the class `myClass` by writing:

```
$(".myClass").css("border", "3px solid red");
```

## .clearQueue()

The `.clearQueue()` method removes from the queue items that haven’t been run.

For example, if we have the following HTML:

```
<button id="start">Start</button>
<button id="stop">Stop</button>
<div></div>
```

And CSS:

```
div {
  margin: 3px;
  width: 40px;
  height: 40px;
  position: absolute;
  left: 0px;
  top: 30px;
  background: green;
  display: none;
}

div.newcolor {
  background: blue;
}
```

Then we can add a way to start and stop animation by writing:

```
$("#start").click(function() {
  const myDiv = $("div");
  myDiv.show("slow");
  myDiv.animate({
    left: "+=200"
  }, 5000);

  myDiv.queue(function() {
    const that = $(this);
    that.addClass("newcolor");
    that.dequeue();
  });

  myDiv.animate({
    left: "-=200"
  }, 1500);
  myDiv.queue(function() {
    const that = $(this);
    that.removeClass("newcolor");
    that.dequeue();
  });
  myDiv.slideUp();
});

$("#stop").click(function() {
  const myDiv = $("div");
  myDiv.clearQueue();
  myDiv.stop();
});
```

In the `click` callback for the button with ID `start`, we call `queue` with callbacks to add animation to the div.

Then in the `click` callback for the button with ID `stop` , we call `clearQueue` to clear the queue then stop the animation with the `stop` method.

## .click()

The `click` method lets us add an event handler for the `click` event or trigger the event on an element.

For example, if we have the following HTML:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `click` event triggered on the div with ID `target` by writing:

```
$("#target").click(function() {
  alert("Handler for .click() called.");
});
```

Now when we click it, we’ll see the alert popup.

Also, we can trigger the `click` event programmatically by writing:

```
$("#target").click(function() {
  alert("Handler for .click() called.");
});

$("#other").click(function() {
  $("#target").click();
});
```

When we click the div with ID `other` , we trigger the `click` event on the div with ID `target` .

## .clone()

The `.clone()` method creates a deep copy of the set of matched elements.

For example, if we have the following HTML:

```
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">Goodbye</div>
</div>
```

Then we can get the div with class `hello` , make a copy of it and append it to the div with class `goodbye` by writing:

```
$(".hello").clone().appendTo(".goodbye");
```

## .closest()

The `.closest()` method gets the closest element with the given selector.

For example, if we have the following HTML:

```
<ul id="one" class="level-1">
  <li class="item-i">I</li>
  <li id="ii" class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

We get the `ul` that’s closest to the element with the class `item-a` by writing:

```
$("li.item-a")
  .closest("ul")
  .css("background-color", "red");
```

We get both the `ul` with class `level-2` and the `ul` with class `level-3` and add a red background to them.

## :contains() Selector

We can use the `:contains` selector to match elements with the given text.

For example, if we have:

```
<div>John Smith</div>
<div>George Martin</div>
<div>Malcom John Sinclair</div>
<div>J. Ohn</div>
```

Then we get all the divs with text `'John'` in it and apply styles to it by writing:

```
$("div:contains('John')").css("text-decoration", "underline");
```

We add underline to all the divs with text `'John'` in it.

So the 1st and 3rd div will have the underline.

## .contents()

The `.contents()` method gives us the content of the element.

For example, if we have:

```
<div class="container">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
  do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  <br><br>
  Ut enim ad minim veniam, quis nostrud exercitation ullamco
  laboris nisi ut aliquip ex ea commodo consequat.
  <br><br>
  Duis aute irure dolor in reprehenderit in voluptate velit
  esse cillum dolore eu fugiat nulla pariatur.
</div>
```

Then we get the text nodes by writing:

```
const els = $(".container")
  .contents()
  .filter(function() {
    return this.nodeType === 3;
  })
console.log(els);
```

`nodeType` with value 3 is the text nodes.

## .contextmenu()

We can bind to the `contextmenu` event with the `.contextmenu()` method.

For example, if we have the given HTML:

```
<div id="target">
  Right-click here
</div>
```

Then we can listen to right-clicks by writing:

```
$("#target").contextmenu(function() {
  alert("Handler for .contextmenu() called.");
});
```

When we right-click the div, then we see the alert displayed.

## .css()

We can also use it to get the value of computed styles with the `css` method lets us set styles for the select elements.

For example, if we have the following HTML:

```
<div style="background-color:blue;"></div>
<div style="background-color:rgb(15,99,30);"></div>
<div style="background-color:#123456;"></div>
<div style="background-color:#f11;"></div>
```

And the following CSS:

```
div {
   width: 60px;
   height: 60px;
   margin: 5px;
   float: left;
}
```

Then we can listen to clicks and get the style when we click on the div by wiring:

```
$("div").click(function() {
  const color = $(this).css("background-color");
  console.log(color)
});
```

We get the `background-color` property’s value with this.

Also, we can get multiple styles by writing:

```
$("div").click(function() {
  const styles = $(this).css([
    "width", "height", "color", "background-color"
  ]);
  console.log(styles)
});
```

We just pass in an array with the property names.

## .data()

We can store data within matched elements with the `data` method.

For example, we can write the following HTML:

```
<span></span>
```

Then use `data` to store and get the data as follows:

```
$("body").data("foo", 52);
$("span").first().text($("body").data("foo"));
```

We save the `data` with key `'foo'` and value 52 in the first line.

Then in the 2nd line, we get the data and put it in the `span` .

## .dblclick()

The `.dblclick()` method binds an event handler to the `dblclick` event or trigger the event on an element.

For example, if we have the following HTML:

```
<div id="target">
  Double-click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to double clicks on the div with ID `target` by writing:

```
$("#target").dblclick(function() {
  alert("Handler for .dblclick() called.");
});
```

We can also trigger a double click on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").dblclick(function() {
  alert("Handler for .dblclick() called.");
});

$("#other").click(function() {
  $("#target").dblclick();
});
```

## deferred.always()

`deferred.always()` adds a callback to be called when the deferred object is resolved or rejected.

For example, we can write:

```
[](#cb446-1)$.get("foo.php").always(function() {
[](#cb446-2)  alert("$.get completed");
[](#cb446-3)});
```

to call the `alert` when we make a GET request for `foo.php` .

## deferred.catch()

The `deferred.catch` method adds a callback that’s called when the deferred object is rejected.

For example, we can write:

```
[](#cb447-1)$.get("foo.php")
[](#cb447-2)  .then(function() {
[](#cb447-3)    alert("$.get succeeded");
[](#cb447-4)  })
[](#cb447-5)  .catch(function() {
[](#cb447-6)    alert("$.get failed!");
[](#cb447-7)  });
```

or:

```
(async () => {
  try {
    const res = await $.get("foo.php")
  } catch (error) {
    alert("$.get failed!");
  }
})()
```

`$.get` returns a thenable object so it works with `async` and `await` .

## deferred.done()

The `deferred.done()` method lets us add a callback that’s called when the deferred object is resolved.

For example, we can write:

```
$.get("https://jsonplaceholder.typicode.com/todos/1")
  .done(function() {
    alert("$.get succeeded");
  });
```

to make a GET request [https://jsonplaceholder.typicode.com/todos/1](https://jsonplaceholder.typicode.com/todos/1) and add run something after that.

## deferred.fail()

The `deferred.fail()` method lets us add a callback that’s called when the deferred object is rejected.

For example, we can write:

```
[](#cb450-1)$.get("test.php")
[](#cb450-2)  .done(function() {
[](#cb450-3)    alert("$.get succeeded");
[](#cb450-4)  })
[](#cb450-5)  .fail(function() {
[](#cb450-6)    alert("$.get failed!");
[](#cb450-7)  });
```

to add that.

## deferred.pipe()

We can use the `deferred.pipe()` method to filter and chain deferred objects.

It returns another deferred object.

We can use it by writing:

```
const defer = $.Deferred(),
  filtered = defer.pipe(function(value) {
    return value * 2;
  });

defer.resolve(5);
filtered.done(function(value) {
  alert(value);
});
```

We call `defer.pipe` with a callback that takes the resolved value from the `defer` object, multipole by it by 2, and return it in the callback.

Then we call `defer.resolve(5)` to pass 5 as the value of `value` in the `pipe` callback.

And we get the final`value` in the `done` callback, which is 10.

We can chain deferred by writing:

```
const url = 'https://jsonplaceholder.typicode.com/posts/1';
const url2 = 'https://jsonplaceholder.typicode.com/posts/2';
const request = $.ajax(url, {
    dataType: "json"
  })
  .pipe(function(data) {
    console.log(data)
    return $.ajax(url2);
  })
  .done(function(data) {
    console.log(data)
  });
```

We call `pipe` on the first deferred object returned by `$.ajax` and then call `done` to get the data from the 2nd `$.ajax` call.

## :eq() Selector

The `:eq` selector lets us select an element at the given index within the matched set.

For example, if we have:

```
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

Then we can write:

```
$("li:eq(2)").css("background-color", "red");
```

to get the 3rd `li` and add a red background to it.

## .even()

We can get the elements that are the ones with an even number index in the matched set with the `even` method.

For example, if we have:

```
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

Then we call it by writing:

```
$("li").even().css("background-color", "red");
```

to add a red background to the `li` elements with an even index.

## event.currentTarget

We can use the `event.currentTarget` property to get the current DOM element within the event bubbling phase.

For example, if we have:

```
<p>
  click me
</p>
```

We can get the `p` element that we clicked on by writing:

```
$("p").click(function(event) {
  alert(event.currentTarget === this);
});
```

The `alert` should be `true` since `this` is the `p` element that we clicked on, which is the same as `event.currentTarget` .

## event.data

The `event.data` is a property with the data that as pass into an event.

For example, if we have the following HTML:

```
<button> 0 </button>
<button> 1 </button>
<button> 2 </button>
<button> 3 </button>
<button> 4 </button>
```

Then we can add click listeners to each element and get the data by writing:

```
for (let i = 0; i < 5; i++) {
  $("button").eq(i).on("click", {
    value: i
  }, function(event) {
    console.log('value: ', event.data.value)
  });
}
```

We get the `event.data.value` property’s value in the click callback.

This should be the same value as the `value` property we pass in as the 2nd argument.

## event.delegateTarget

The `event.delegateTarget` property has the element where the currently called jQuery event handler was attached.

For example, if we have:

```
<div class='box'>
  <button>
    0
  </button>
</div>
<div class='box'>
  <button>
    1
  </button>
</div>
<div class='box'>
  <button>
    2
  </button>
</div>
```

Then we can set the div with the class `box` to have a red background when we click on the button inside by writing:

```
$(".box").on("click", "button", function(event) {
  $(event.delegateTarget).css("background-color", "red");
});
```

## event.isDefaultPrevented()

We can call `event.isDefaultPrevented()` to check whether `event.preventDefault()` is called on an object.

For example, if we have:

```
<a>hello</a>
```

Then we can call this method by writing:

```
$("a").click(function(event) {
  alert(event.isDefaultPrevented());
  event.preventDefault();
  alert(event.isDefaultPrevented());
});
```

We call the method and show its return value in the alert box.

## event.isPropagationStopped()

We can call the `event.isPropagationStopped()` method to check if we called `event.stopPropagation()` .

For example, if we have:

```
<button>click me</button>
```

Then we can call this method by writing:

```
$("button").click(function(event) {
  alert(event.isPropagationStopped());
  event.stopPropagation();
  alert(event.isPropagationStopped());
});
```

## event.metaKey

We can check whether the meta key is pressed when an event is fired with the `event.metaKey` property.

In Windows, the meta key is the Windows key.

In macOS, the meta key is the command key.

For example, if we have:

```
<button value="Test" name="Test" id="checkMetaKey">Click me!</button>
```

Then we can check if the meta key is pressed when we click on the click me button by writing:

```
$("#checkMetaKey").click(function(event) {
  console.log(event.metaKey);
});
```

## event.namespace

We can get the namespace of the event by using the `event.namespace` property.

For example, if we have:

```
<button>display event.namespace</button>
<p>

</p>
```

Then we can trigger an event with a namespace by writing:

```
$("p").on("test.something", function(event) {
  alert(event.namespace);
});
$("button").click(function(event) {
  $("p").trigger("test.something");
});
```

We trigger the `test.something` event on thr `p` element when we click on a button.

Then `event.namespace` should be `something` and that’s displayed in the alert.

## event.pageX and event.pageY

We can get the x and y-coordinates of the mouse position relative to the left edge of the document with the `event.pageX` and `event.pageY` properties respectively.

For example, we can log the mouse coordinate as the mouse moves by writing HTML:

```
<div id="log"></div>
```

and JavaScript:

```
[](#cb472-1)$(document).on("mousemove", function({
[](#cb472-2)  pageX,
[](#cb472-3)  pageY
[](#cb472-4)}) {
[](#cb472-5)  $("#log").text(`${pageX}, ${pageY}`);
[](#cb472-6)});
```

We listen to the `mousemove` event and get the `pageX` and `pageY` properties from the `event` object.

## event.preventDefault()

We call the `event.preventDefault()` method to prevent the default action from being run in our event.

For example, if we have:

```
<a href='https://google.com'>hello</a>Then
```

Then we can prevent users from going to [https://google.com](https://google.com) by writing:

```
$("a").click(function(event) {
  event.preventDefault();
});
```

## event.relatedTarget

The `event.relatedTarget` property gets the other DOM elements involved in an event.

For example, if we have:

```
<div>
  <a href='https://google.com'>hello</a>
</div>
```

Then when we move the mouse of of the `a` element, we can get the element that the mouse moved to with this property:

```
$("a").mouseout(function(event) {
  alert(event.relatedTarget.nodeName);
});
```

We should see `DIV` in the alert since the mouse moved to the div.

## event.result

The `event.result` property returns the last value returned by an event handler that’s triggered by the event.

For example, if we have:

```
<button>display event.result</button>
```

Then we can return a value in a click listener function and get its value with `event.result` :

```
$("button").click(function(event) {
  return "hello";
});
$("button").click(function(event) {
  console.log(event.result);
});
```

We return `'hello'` in the first click listener.

Then we log `event.result` in the 2nd click listener.

It should log `'hello'` since that’s the return value of the first click listener.

## event.stopImmediatePropagation()

We can call the `event.stopImmediatePropagation()` method to stop event propagation.

For example, if we have the following HTML:

```
<p>paragraph</p>
<div>division</div>
```

and CSS:

```
p {
   height: 30px;
   width: 150px;
   background-color: #ccf;
}

div {
   height: 30px;
   width: 150px;
   background-color: #cfc;
}
```

Then we can call `stopImmediatePropagation` to stop the propagation of the click event trigger on the `p` by writing:

```
$("p").click(function(event) {
  event.stopImmediatePropagation();
});
$("p").click(function(event) {
  $(this).css("background-color", "#f00");
});
$("div").click(function(event) {
  $(this).css("background-color", "#f00");
});
```

`event.stopImmediatePropagation()` is called on the first click listener, so the 2nd one won’t run.

The `div` ‘s click listener isn’t affected.

## event.stopPropagation()

We can call `event.stopPropagation` to stop event propagation to an element’s parent and ancestor selectors.

For example, if we have:

```
<p>paragraph</p>
```

We can write:

```
$("p").click(function(event) {
  event.stopPropagation();
  // Do something
});
```

to stop the click event’s propagation.

## event.target

We can get the element that an event is triggered on with the `event.target` property.

For example, if we have:

```
<p>paragraph</p>
```

Then we can get which element is clicked in the `body` by writing:

```
$("body").click(function(event) {
  console.log("clicked: ", event.target.nodeName);
});
```

The `nodeName` gets the tag name of the element that’s clicked.

## event.timeStamp

We can get when the event is triggered with the `timestamp` property.

For example, if we have:

```
<p>paragraph</p>
```

Then we can write:

```
$("body").click(function(event) {
  console.log(event.timeStamp);
});
```

Then when we click on the paragraph, we see the timestamp logged.

## event.type

The `event.type` property lets us get the type of event that’s triggered.

For example, if we have:

```
<p>paragraph</p>
```

Then we can write:

```
$("p").click(function(event) {
  alert(event.type);
});
```

to get the type of event that’s triggered with `event.type` .

## event.which

The `event.which` property lets us get the key on the keyboard or mouse that’s pressed.

For example, if we have:

```
<input id="whichkey" value="type something">
```

Then we can get the key code of the keyboard key that's pressed by writing:

```
$("#whichkey").on("keydown", function(event) {
  console.log(event.type, event.which);
});
```

`which` returns a number that corresponds to the key.

## .fadeIn()

The `.fadeIn()` method fades an item to opaque.

For example, if we have the following HTML:

```
<div id="clickme">
  Click here
</div>
<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

and CSS:

```
#book {
  display: none;
}
```

We can make the photo appear slowly when we click on Click here by writing:

```
$("#clickme").click(function() {
  $("#fork").fadeIn("slow");
});
```

## .fadeOut()

The `.fadeOut()` method lets us make an element disappear.

For example, if we have:

```
<div id="clickme">
  Click here
</div>
<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

Then we can make the photo fade out when we click on Click here by writing:

```
$("#clickme").click(function() {
  $("#fork").fadeOut("slow");
});
```

## .fadeTo()

The `.fadeTo()` method lets us set the opacity to fade to.

For example, we can write:

```
<div id="clickme">
  Click here
</div>
<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

Then we can write:

```
$("#clickme").click(function() {
  $("#fork").fadeTo("slow", 0.5);
});
```

The 2nd argument is the opacity to fade to.

## .fadeToggle()

The `.fadeToggle()` lets us display or hide the matched elements by animating their opacity.

For example, if we have:

```
<button>fadeToggle 1</button>
<button>fadeToggle 2</button>
<img id="fork" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

Then we can call the `fadeToggle` method by writing:

```
$("button").click(function() {
  $("#fork").first().fadeToggle("slow", "linear");
});

$("button").last().click(function() {
  $("#fork").first().fadeToggle("fast", "linear");
});
```

We add click listeners for the buttons so that we can call `fadeToggle` inside to toggle the fading when we click the buttons.

## :file Selector

We can get the input with type `file` with the `:file` selector.

For example, if we have:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio">
  <input type="reset">
  <input type="submit">
  <input type="text">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
```

We can write:

```
$("input:file").css({
  background: "yellow",
  border: "3px red solid"
});
```

## .filter()

The `filter` method lets us get the elements that match the select or pass a function test from a set of matched elements.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
  <li>list item 6</li>
</ul>
```

We can get the `li` s that are in an even number position and add a red background to them by writing:

```
$("li").filter(":nth-child(2n)").css("background-color", "red");
```

So the 2nd, 4th, and 6th `li` elements have a red background.

## .find()

The `.find()` method gets the descendants of each element in the current set of matched elements filtered by a selector, jQuery object, or element.

For example, if we have:

```
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

Then we can get the `li` ‘s from the `li` with the class `item-ii` and add a red background to them by writing:

```
$("li.item-ii").find("li").css("background-color", "red");
```

## .finish()

The `.finish()` method stops the currently-running animation, remove all queued animations, and complete all animations for the matched elements.

For example, if we have the following HTML:

```
<div class="box"></div>
<div id="path">
  <button id="go">Go</button>
  <br>
  <button id="bf" class="b" onclick="finish()">finish</button>
</div>
```

And CSS:

```
.box {
  position: absolute;
  top: 10px;
  left: 10px;
  width: 15px;
  height: 15px;
  background: black;
}
```

Then we can create an animation for the div withn class `box` when we click on the Go button by writing:

```
const horiz = $("#path").width() - 20,
  vert = $("#path").height() - 20;
$("#go").on("click", function() {
  $(".box")
    .clearQueue()
    .stop()
    .css({
      left: 10,
      top: 10
    })
    .animate({
      top: vert
    }, 3000)
    .animate({
      left: horiz
    }, 3000)
    .animate({
      top: 10
    }, 3000);
});

const finish = () => {
  $("div.box").finish();
}
```

The `finish` function is called when we click on the finish button to skip the animation to the end.

## .first()

The `.first()` method gets the first element from a set of matched elements.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get the first `li` and add a red background to it by wiring:

```
$("li").first().css("background-color", "red");
```

## deferred.promise()

The `deferred.promise()` method returns the deferred object’s promise object.

For example, we can use it by writing:

```
function asyncEvent() {
  const dfd = jQuery.Deferred();
  setTimeout(function() {
    dfd.resolve("hurray");
  }, Math.floor(400 + Math.random() * 2000));

  setTimeout(function() {
    dfd.reject("error");
  }, Math.floor(400 + Math.random() * 2000));

  setTimeout(function working() {
    if (dfd.state() === "pending") {
      dfd.notify("working... ");
      setTimeout(working, 500);
    }
  }, 1);

  return dfd.promise();
}

(async () => {
  try {
    const res = await $.when(asyncEvent())
    cosole.log(res)
  } catch (err) {
    console.log(err);
  }
})()
```

We have an `asyncEvent` function that returns a promise from the deferred object in the last line.

It resolves or rejects randomly.

Then in the `async` function we invoke the promise returned by the `asyncEvent` function.

## deferred.reject()

The `deferred.reject()` method rejects a deferred object with an argument and calls any failure callbacks.

For example, we can use it by writing:

```
const deferred = jQuery.Deferred();
deferred.reject('error');
```

## deferred.rejectWith()

The `deferred.rejectWith()` method rejects a deferred object with the context object and arguments and calls any failure callbacks.

For example, we can write:

```
const deferred = jQuery.Deferred();
deferred.rejectWith({
    foo: 'bar'
  }, [1])
  .catch(function(err) {
    console.log(this, err);
  })
```

We call `rejectWith` with `{ foo: ‘bar’ }` as the `this` value and `[1]` as the arguments array.

Then we can get them all in the `catch` callback.

`this` is `{ foo: ‘bar’ }` and `err` is 1.

## deferred.resolve()

We can call `deferred.resolve()` to resolve a deferred object and call any done callbacks with the given arguments.

For example, we can write:

```
(async () => {
  try {
    const deferred = jQuery.Deferred();
    const res = await deferred.resolve(1)
    console.log(res);
  } catch (error) {
    console.log(error);
  }
})()
```

We create the `deferred` object. Then we call `deferred.resolve` method with the resolved value.

Then we `res` has the resolved value since we added `await` before `deferred.resolve` .

It works because it returns an object with a `then` method that takes a callback with the resolved value as the parameter.

## deferred.resolveWith()

The `deferred.resolveWith()` lets us resolve a deferred object and call any done callbacks with a context object and arguments.

For example, we can use it by writing:

```
const deferred = jQuery.Deferred();
deferred.resolveWith({
    foo: 'bar'
  }, [1])
  .then(function(val) {
    console.log(this, val);
  })
```

We call `resolveWith` with the `this` value and an array of arguments.

Then we call `then` on the returned object with a callback and get the `this` and `val` values.

`this` is `{ foo: ‘bar’ }` and `val` is 1.

## deferred.state()

The `deferred.state()` method returns the state of the deferred object.

It can return `'pending'` , `'resolved'` or `'rejected'` .

`'pending'` means the deferred object isn’t completed.

`'resolved'` means the deferred object is called with `deferred.resolve()` or `deferred.resolveWith()`.

`'rejected'` means the deferred object is in a rejected state. Calling `deferred.reject()` or `deferred.rejectedWith()` will make it `'rejected'` .

For example, we can use it by writing:

```
const deferred = jQuery.Deferred();
deferred.resolveWith({
    foo: 'bar'
  }, [1])
  .then(function(val) {
    console.log(deferred.state())
  })
```

Then the console log should log `'resolved'` .

## :disabled Selector

We can get inputs that are disabled with the `:disabled` selector.

For example, if we have the following HTML:

```
<form>
  <input name="email" disabled="disabled">
  <input name="id">
</form>
```

Then we can set the value of the disabled input by writing:

```
$("input:disabled").val("this is it");
```

## .each()

The `.each()` method lets us iterate over a jQuery object.

For example, if we have the following HTML:

```
<ul>
  <li>foo</li>
  <li>bar</li>
</ul>
```

Then we can get all the `li` elements by writing:

```
$("li").each(function(index) {
  console.log(index, $(this).text());
});
```

## Element Selector

We can get elements with the given tag name with the element selector.

For example, if we have the following HTML:

```
<div>DIV1</div>
<div>DIV2</div>
<span>SPAN</span>
```

Then we can add a red border to all the divs by writing:

```
$("div").css("border", "9px solid red");
```

## .empty()

The `.empty()` method removes all child nodes of the set of matched elements in the DOM.

For example, if we have the following HTML:

```
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">bye</div>
</div>
```

Then we can call `empty` by writing:

```
$(".hello").empty();
```

Now the div with class `hello` will no longer have the text inside it.

## :empty Selector

We can use the `:empty` selector to get all elements that have no children.

For example, if we have:

```
<table>
  <tr>
    <td>TD #0</td>
    <td></td>
  </tr>
  <tr>
    <td>TD #2</td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>TD#5</td>
  </tr>
</table>
```

Then we can add text to the empty `td` elements by writing:

```
$("td:empty")
  .text("Was empty")
  .css("background", "green");
```

We add the `'Was empty'` text into the empty `td` element and add a green background to it.

## :enabled Selector

We can use the `:enabled` selector to get all the enabled input elements.

For example, if we have the following HTML:

```
<form>
  <input name="email" disabled>
  <input name="id">
</form>
```

Then we get the enabled input and set its value by writing:

```
$("input:enabled").val("this is it");
```

## .end()

The `.end` method ends the most recent filtering operation in the current chain and return the set of matched elements to its previous state.

For example, if we have the following HTML:

```
<ul class="first">
  <li class="foo">list item 1</li>
  <li>list item 2</li>
  <li class="bar">list item 3</li>
</ul>
<ul class="second">
  <li class="foo">list item 1</li>
  <li>list item 2</li>
  <li class="bar">list item 3</li>
</ul>
```

We can apply styles on the `li` with class `foo` and the `li` with class `bar` in the same method chain by writing:

```
$("ul.first")
  .find(".foo")
  .css("background-color", "red")
  .end()
  .find(".bar")
  .css("background-color", "green");
```

The `end` method lets us end working with `li` with class `foo` and then we call `find` to find another element.

## .eq()

The `.eq()` method reduces a set of matched elements to the one with the given index.

For example, if we have:

```
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

Then we can get the `li` with index 2, which is the 3rd one and add a red background to it by writing:

```
$("li").eq(2).css("background-color", "red");
```

## deferred.then()

The `deferred.then()` lets us add handlers that are called when the deferred object is resolved, rejected, or still in progress.

For example, we can write:

```
$.get("https://jsonplaceholder.typicode.com/posts/1")
  .then(
    function() {
      alert("$.get succeeded");
    },
    function() {
      alert("$.get failed!");
    }
  );
```

We make a request with `$.get` , which returns a deferred object.

Then we call `then` with the success callback as the first argument and the failure callback as the 2nd argument.

## .delay()

The `.delay()` method sets a timer to delay the execution of subsequent items in the queue.

For example, if we have the following HTML:

```
<div id="foo"></div>
```

and CSS:

```
#foo {
  width: 200px;
  height: 200px;
  min-height: 100px;
  background-color: green
}
```

We can add a slide up effect, then show the fade-in effect after a delay by writing:

```
$("#foo").slideUp(300).delay(800).fadeIn(400);
```

`delay(800)` adds a 800ms delay.

## .dequeue()

The `.dequeue()` method runs the next function on the queue with the matched elements.

For example, if we have the following HTML:

```
<button>Start</button>
<div></div>
```

and CSS:

```
div {
   margin: 3px;
   width: 50px;
   position: absolute;
   height: 50px;
   left: 10px;
   top: 30px;
   background-color: yellow;
 }

div.red {
   background-color: red;
}
```

We can make the div slide around and turn red by writing:

```
$("button").click(function() {
  $("div")
    .animate({
      left: "+=200px"
    }, 2000)
    .animate({
      top: "0px"
    }, 600)
    .queue(function() {
      $(this).toggleClass("red").dequeue();
    })
    .animate({
      left: "10px",
      top: "30px"
    }, 700);
});
```

In the `queue` callback, we call:

```
$(this).toggleClass("red").dequeue();
```

to add the `red` class on the div.

## Descendant Selector

We can select all elements that are descendants of a given selector.

For example, if we have the following HTML:

```
<form>
  <div>Form is surrounded by the green border.</div>
  <label for="name">Child of form:</label>
  <input name="name" id="name">

  <fieldset>
    <label for="newsletter">Newsletter</label>
    <input name="newsletter" id="newsletter">
  </fieldset>
</form>
```

Then we can get the input elements in the `form` element by writing:

```
$("form input").css("border", "2px dotted blue");
```

## .detach()

The `.detach()` remove the set of matched elements from the DOM.

For example, if we have the following HTML:

```
<p>Hello</p>
how are
<p>you?</p>
<button>Attach/detach paragraphs</button>
```

Then we can attach or detach the paragraphs when we click the button by writing:

```
let p;
$("button").click(function() {
  if (p) {
    p.appendTo("body");
    p = null;
  } else {
    p = $("p").detach();
  }
});
```

In the `click` handler, we check if there’s any `p` elements.

If there are any, then we call `detach` to remove them. The remove elements are returned by `detach` .

If there isn’t then we attach the `p` elements to the `body` and set `p` to `null` .

## .die()

The `die` method removes event handlers previous attached using the `live` method.

For example, we can write:

```
$("p").die();
```

to unbind all event handlers bound to `p` elements.

We can also unbind only `click` event handlers by writing:

```
$("p").die('click');
```

Also, we can unbind a single event handler by writing:

```
const foo = function() {

};
$("p").live("click", foo);
$("p").die("click", foo);
```

We remove the `foo` click handler with the `die` method.

## :first-child Selector

We can use the `:first-child` selector to get the first child element.

For example, if we have the following HTML:

```
<div>
  <span>Glen,</span>
  <span>Jane,</span>
  <span>Ralph</span>
</div>
```

And the following CSS:

```
.green {
  color: green
}
```

Then we can write:

```
$("div span:first-child")
  .css("text-decoration", "underline")
  .hover(function() {
    $(this).addClass("green");
  }, function() {
    $(this).removeClass("green");
  });
```

to get the first `span` in the `div` with the `:first-child` selector.

Then we called `css` to add the underline to the first span.

And finally we add hover to it with `hover` .

The first callback is called when we hover over the element, and the second one is called when we hover away from it.

## :first-of-type Selector

We can use the `:first-of-type` selector to select all elements that are the first among the siblings with the same element name.

For example, if we have the following HTML:

```
<div>
  <span>Glen,</span>
  <span>Tane,</span>
  <span>Ralph</span>
</div>
<div>
  <b>Nobody,</b>
  <span>John,</span>
  <span>Scott,</span>
  <span>Tim</span>
</div>
```

and the following CSS:

```
.green {
  color: green
}
```

Then we can add the `green` class to the first `span` in each div by writing:

```
$("span:first-of-type").addClass("green");
```

## :first Selector

The `:first` select lets us select the first matched DOM element.

For example, if we have:

```
<table>
  <tr>
    <td>Row 1</td>
  </tr>
  <tr>
    <td>Row 2</td>
  </tr>
  <tr>
    <td>Row 3</td>
  </tr>
</table>
```

Then we can make the first `tr` italic by writing:

```
$("tr:first").css("font-style", "italic");
```

Now everything in the `tr` is italic.

## .focus()

The `focus` method lets us add an event handler for the `focus` event or trigger the event on an element.

For example, if we have:

```
<form>
  <input id="target" type="text" value="Field 1">
  <input type="text" value="Field 2">
</form>
<div id="other">
  Trigger the handler
</div>
```

Then we can add a callback that’s called when the `focus` event is triggered on the input with ID `target` by writing:

```
$("#target").focus(function() {
  console.log("Handler for .focus() called.");
});
```

## :focus Selector

The `:focus` selector selects an element if it’s currently focused.

For example, if we have the following HTML:

```
<div id="content">
  <input tabIndex="1">
  <input tabIndex="2">
  <select tabIndex="3">
    <option>select menu</option>
  </select>
  <div tabIndex="4">
    a div
  </div>
</div>
```

And the following CSS:

```
.focused {
  background: green;
}
```

Then we can add the `green` class to element that’s focused by writing:

```
$("#content").delegate("*", "focus blur", function() {
  const elem = $(this);
  setTimeout(function() {
    elem.toggleClass("focused", elem.is(":focus"));
  }, 0);
});
```

The `delegate` method’s callback has the child elements of the div with ID `content` as the value of `this` .

And the callback is called when `focus` or `blur` event is triggered on any child element in it.

So we can use `toggleClass` to toggle the `green` class on when the element is focused.

The first argument is the class name and the second argument is the condition that toggles on the class in the first argument.

## .focusin()

The `.focusin()` method binds an event handler to the `focusin` event.

For example, if we have:

```
<p><input type="text"> <span>focusin fire</span></p>
<p><input type="text"> <span>focusin fire</span></p>
```

Then we can write:

```
$("p").focusin(function() {
  $(this).find("span").css("display", "inline").fadeOut(1000);
});
```

We get the `span` and fade it out when we focus on the input inside the `p` element.

## .focusout()

The `focusout` method lets us bind an event handler to the `focusout` JavaScript event.

For example, if we have:

```
<p><input type="text"> <span>focusout fire</span></p>
<p><input type="text"> <span>focusin fire</span></p>
```

We can write:

```
let focus = 0;
$("p")
  .focusout(function() {
    focus++;
    console.log(focus);
  })
```

to count the number of times the `focusout` event is triggered.

It’ll be triggered when we move focus on out of the `p` element.

## .get()

The `get` method retrieves the DOM element matched by the jQuery object.

For example, if we have:

```
<ul>
  <li id="foo">foo</li>
  <li id="bar">bar</li>
</ul>
```

We get the first `li` element by writing:

```
console.log($("li").get(0));
```

## .has()

The `has` method lets us reduce the set of matched elements to those that have a descendant that matches the selector or DOM element.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2
    <ul>
      <li>list item 2-a</li>
      <li>list item 2-b</li>
    </ul>
  </li>
  <li>list item 3</li>
  <li>list item 4</li>
</ul>
```

We can write:

```
$("li").has("ul").css("background-color", "red");
```

to get all the `li` ‘s that have `ul` ‘s inside and add a red background to it.

## Has Attribute Selector [name]

We can use the has attribute selector to get all the elements with the given attribute set.

For example, if we have:

```
<div>no id</div>
<div id="hey">with id</div>
<div id="there">has an id</div>
<div>nope</div>
```

Then we can get all the elements with the `id` attribute set by writing:

```
$("div[id]").one("click", function() {
  const idString = $(this).attr("id");
  $(this).text(idString);
});
```

In the callback, we set the text of the currently clicked on element’s text content to the value of the `id` attribute.

## :has() Selector

The `:has` selector lets us get all the elements that has at least one element that matches the specified selector.

For example, if we have the following HTML:

```
<div>
  <p>paragraph</p>
</div>
<div>Hello again! (with no paragraph)</div>
```

and the following CSS:

```
.test {
  border: 3px inset red;
}
```

Then we can add a border to the div with a `p` element in it by writing:

```
$("div:has(p)").addClass("test");
```

## .hasClass()

The `.hasClass()` method determines whether any matched elements are assigned the given class.

For example, if we have:

```
<div id="mydiv" class="foo bar"></div>
```

Then we can check if the div with ID `mydiv` has the `foo` class added to it by writing:

```
$("#mydiv").hasClass("foo")
```

## :header Selector

The `:header` selector selects all elements that are headers (e.g. h1, h2, etc.)

For example, if we have:

```
<h1>Header 1</h1>
<p>Contents 1</p>
<h2>Header 2</h2>
<p>Contents 2</p>
```

Then we can write:

```
$(":header").css({
  background: "gray",
  color: "blue"
});
```

to add a gray background and make the text blue to the h1 and h2 elements.

## .height()

The `.height()` method gets the current computed height for the first element in the set of matched elements.

It can also ser the height of every matched element.

For example, we can get the height of `window` by writing:

```
console.log($(window).height())
```

And if we have a div:

```
<div></div>
```

with the following CSS:

```
div {
  width: 50px;
  height: 70px;
  float: left;
  margin: 5px;
  background: red;
  cursor: pointer;
}
```

We can set its height when we click it by writing:

```
$("div").one("click", function() {
  $(this).height(30).css({
    cursor: "auto",
    backgroundColor: "green"
  });
});
```

The height is in pixels.

## :hidden Selector

We can use the `:hidden` select to select all elements that are hidden.

For example, if we have:

```
<div></div>
<div style="display:none;">Hidden</div>
<div></div>

<div class="starthidden">Hidden</div>
<div></div>

<form>
  <input type="hidden">
  <input type="hidden">
  <input type="hidden">
</form>
```

and the following CSS:

```
.starthidden {
  display: none;
}
```

Then we can get all the hidden elements that aren’t `script` elements buy writing:

```
const hiddenElements = $("body").find(":hidden").not("script");
console.log(hiddenElements)
```

We can also show the hidden divs by writing:

```
$("div:hidden").show(3000);
```

## .hide()

The `.hide()` method hides the matched elements.

For example, if we have:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c" alt="">
```

Then we can hide the image when we click Click here by writing:

```
$("#clickme").click(function() {
  $("#book").hide("slow", function() {
    alert("Animation complete.");
  });
});
```

The first argument of `hide` is the animation tup;e.

And the 2nd argument is the callback that’s called when the animation is done.

## .hover()

The `hover` method lets us bind event handlers for hovering over and hover out of the element.

For example, if we have:

```
<ul>
  <li>Milk</li>
  <li>Bread</li>
  <li class="fade">Chips</li>
  <li class="fade">Socks</li>
</ul>
```

Then we can add `***` to the `li` text when we hover over it by writing:

```
$("li").hover(
  function() {
    $(this).append($("<span> ***</span>"));
  },
  function() {
    $(this).find("span").last().remove();
  }
);

$("li.fade").hover(function() {
  $(this).fadeOut(100);
  $(this).fadeIn(500);
});
```

The `***` will disappear when we move our mouse outside.

## .html()

The `.html()` method gets the HTML content of the first element in the set of matched elements.

It can also be used to set the HTML of every matched element.

For example, if we have:

```
<p>
  <b>Click</b> to change the <span id="tag">html</span>
</p>
```

Then we can click on the `p` element to change the text to its raw HTML form by writing:

```
$("p").click(function() {
  const htmlString = $(this).html();
  $(this).text(htmlString);
});
```

We call `html` in the first line to get the HTML code, then we set that as the `text` value.

It’ll be escaped when we set it as the text content so that we’ll see the raw code displayed.

## ID Selector (“#id”)

We can select a single element with the ID selector.

For example, if we have:

```
<div id="myDiv">id="myDiv"</div>
```

Then we can add a red border to the div by writing:

```
$("#myDiv").css("border", "3px solid red");
```

## jQuery.globalEval()

We can use the `jQuery.globalEval()` method to run some JavaScript code globally.

For example, we can write:

```
jQuery.globalEval("let newVar = true;");
```

to run some code.

## jQuery.grep()

The `jQuery.grep()` method finds the element of an array that satisfies the filter function.

For example, we can write:

```
const arr = [1, 9, 3, 8, 6, 1, 5, 9, 4, 7, 3, 8, 6, 9, 1];
const filteredArr = jQuery.grep(arr, function(n, i) {
  return (n !== 5 && i > 4);
});

console.log(filteredArr)
```

Then we returned an array that has the result that satisfies the condition in the callback we passed into `grep` .

`n` has the array entry. `i` has its index.

## jQuery.hasData()

The `jQuery.hasData()` method lets us check if a piece of data is saved into an element.

For example, if we have:

```
<p> </p>
```

Then we can use it by writing:

```
const p = jQuery("p")[0];
console.log(jQuery.hasData(p));
$.data(p, "testing", 123);
console.log(jQuery.hasData(p))
```

We call `hasData` on the `p` element to check if there are any data saved into it.

So the first console log should log `false` and the 2nd one should log `true` .

## jQuery.inArray()

The `jQuery.inArray()` method lets us check if an element is in the array.

It returns the index of it if it’s found and -1 otherwise.

For example, we can write:

```
console.log($.inArray(5 + 5, ["8", "9", "10", 10 + ""]));
```

to check if 10 is in the array.

It should return -1 since it’s not in the array.

## jQuery.isEmptyObject()

We can check if an element is an empty object with the `jQuery.isEmptyObject()` .

For example, if we have:

```
console.log(jQuery.isEmptyObject({}));
```

This should log `true` since we passed in an empty object into the method.

## jQuery.isPlainObject()

The `jQuery.isPlainObject()` method lets us check if a JavaScript object is a plain object.

A plain object is an object literal.

For example, if we have:

```
console.log(jQuery.isPlainObject({}))
console.log(jQuery.isPlainObject("test"))
```

Then the first console log logs `true` and the 2nd one logs `false` .

## jQuery.isXMLDoc()

We can check if a document object is an XML document with the`jQuery.isXMLDoc()` method.

For example, we can write:

```
console.log(jQuery.isXMLDoc(document))
```

Then the console log logs `false` .

## jQuery.makeArray()

We can use the `jQuery.makeArray()` method to convert an element list to an array.

For example, if we have:

```
<div>First</div>
<div>Second</div>
<div>Third</div>
<div>Fourth</div>
```

Then we can write:

```
const elems = document.getElementsByTagName("div");
const arr = jQuery.makeArray(elems);
console.log(arr)
```

We get the divs with `getElementsByTagName` .

Then we call `jQuery.makeArray` to convert the element list to an array.

## jQuery.map()

The `jQuery.map()` method translates all items in an array or object to a new array of items.

For example, we can write:

```
const fakeArray = {
  "length": 2,
  0: "foo",
  1: "bar"
};
const realArray = $.makeArray(fakeArray)
const mapped = $.map(realArray, function(val, i) {
  return val + val;
});

console.log(mapped);
```

`fakeArray` is an object with numeric keys and a `length` property.

We call `$.makeArray` to convert that into a real array.

Then we call `$.map` to map the array entries into new values.

So `mapped` is `[“foofoo”, “barbar”]` .

## jQuery.Callbacks()

The `jQuery.Callbacks()` method lets us create a callback list to manage callbacks.

For example, we can write:

```
const fn1 = (val) => console.log('fn1', val);
const fn2 = (val) => console.log('fn2', val);
const callbacks = $.Callbacks();
callbacks.add(fn1);
callbacks.fire("foo!");
callbacks.add(fn2);
callbacks.fire("bar!");
```

We call `$.Callbacks()` to returns the callbacks list object.

Then we call `add` to add the callback functions.

And we call `fire` to call the callbacks with the given argument.

So, we’ll get:

```
fn1 foo!
fn1 bar!
fn2 bar!
```

logged in the console.

## jQuery.contains()

The `jQuery.contains()` method lets us check to see if a DOM element is a descendant of another DOM element.

For example, we can write:

```
console.log($.contains(document.documentElement, document.body));
```

to check if the `body` element is in the `document` element.

This should return `true` since `body` is in `document`.

## jQuery.cssHooks

The `jQuery.cssHooks` lets us hook directly into jQuery to override how CSS properties are retrieved or set.

We can also change how CSS properties are normalized, property naming, or create custom properties.

For example, if we have:

```
<div id='element'>
  foo
</div>
<div id='another'>
  bar
</div>
```

Then we can specify how the `border-radius` CSS property is get and set by writing:

```
const borderRadius = "borderRadius";
`
$.cssHooks.borderRadius = {
  get(elem, computed, extra) {
    return $.css(elem, borderRadius);
  },
  set(elem, value) {
    elem.style[borderRadius] = value;
  }
};
`
$("#element").css("borderRadius", "10px");
$("#another").css("border-radius", "20px");
```

## jQuery.cssNumber

The `jQuery.cssNumber` object has all the CSS properties that may be used without a unit.

For example, we can set the `borderRadius` CSS property to be used without a unit by writing:

```
jQuery.cssNumber.borderRadius = true;
```

The default object has the following properties set to `true` :

*   `zIndex`
*   `fontWeight`
*   `opacity`
*   `zoom`
*   `lineHeight`
*   `widows` 
*   `orphans` 
*   `fillOpacity` 
*   `columnCount` 
*   `order` 
*   `flexGrow` 
*   `flexShrink`

## jQuery.data()

We can save arbitrary data associated with the specified element and returned what value was set with the `jQuery.data()` method.

For example, if we have:

```
<div>
  The values stored were
  <span></span>
  and
  <span></span>
</div>
```

Then we can save data into the `div` and get it by writing:

```
const div = $("div")[0];
jQuery.data(div, "test", {
  first: 16,
  last: "pizza!"
});
$("span").first().text(jQuery.data(div, "test").first);
$("span").last().text(jQuery.data(div, "test").last);
```

We call `jQuery.data` with the `div` to save the data.

The first argument is the element to save the data.

The 2nd argument is the key to get the data.

And the last argument is the object we’re saving.

Then we get the data in the last 2 lines and set them as the text content of the span.

## jQuery.Deferred()

The `jQuery.Deferred()` method is a factory function that returns a chainable utility object with methods to register callbacks, invoke callbacks, and relay success or failure states of any sync or async operation.

## jQuery.dequeue()

The `jQuery.dequeue()` method lets us run the next function on the queue for the matched element.

For example, if we have the following HTML:

```
<button>Start</button>
<div></div>
```

and the following CSS:

```
div {
  margin: 3px;
  width: 50px;
  position: absolute;
  height: 50px;
  left: 10px;
  top: 30px;
  background-color: yellow;
}
`
div.red {
  background-color: red;
}
```

Then when we click on the Start button, we animate the div by writing

```
$("button").click(function() {
  $("div")
    .animate({
      left: '+=200px'
    }, 2000)
    .animate({
      top: '0px'
    }, 600)
    .queue(function() {
      $(this).toggleClass("red");
      $.dequeue(this);
    })
    .animate({
      left: '10px',
      top: '30px'
    }, 700);
});
```

We call `$.dequeue` to call invoke the animation in the `animate` method.

## .is()

The `is` method lets us check the current matched set of elements against a selector, element, or jQuery object.

It returns `true` if at least one of thee elements matches the given elements.

For example, if we have:

```
<ul>
  <li>list <strong>item 1</strong></li>
  <li><span>list item 2</span></li>
  <li>list item 3</li>
</ul>
```

Then we can check if the element we currently clicked on is an `li` and add a red background to it by writing:

```
$("ul").click(function(event) {
  const target = $(event.target);
  if (target.is("li")) {
    target.css("background-color", "red");
  }
});
```

## jQuery()

The `jQuery()` function takes a string with a CSS selector to match a set of elements.

For example, if we have the following HTML:

```
<div class='foo'>
  <span>foo</span>
</div>
<div>
  bar
</div>
```

and CSS:

```
.bar {
  background: green
}
```

We can add the `bar` class to a `span` inside the div with class `foo` by writing:

```
$("div.foo").click(function() {
  $("span", this).addClass("bar");
});
```

## .jquery

The `.jquery` property lets us get a string containing the jQuery version number.

So we can write:

```
console.log($.fn.jquery)
```

to get that.

## jQuery.ajax()

We can make an Ajax request with the `jQuery.ajax()` method.

For example, we can make a GET request by writing:

```
const jqxhr = $.ajax("https://jsonplaceholder.typicode.com/posts/1")
  .done(function() {
    alert("success");
  })
  .fail(function() {
    alert("error");
  })
  .always(function() {
    alert("complete");
  });
`
jqxhr.always(function() {
  alert("second complete");
});
```

We call `done` with a callback to run something after the request is successful.

The `fail` callback is run when the request fails.

The `always` callback is run whenever the request is done regardless of outcome.

`jqxhr.always` ‘s callback is run whenever the request is done regardless of outcome.

## jQuery.ajaxPrefilter()

The `jQuery.ajaxPrefilter()` method handles custom Ajax options or modifies existing options before each request is sent and before they’re processed by `$.ajax()` .

For example, we can write:

```
const currentRequests = {};
`
$.ajaxPrefilter(function(options, originalOptions, jqXHR) {
  if (options.abortOnRetry) {
    if (currentRequests[options.url]) {
      currentRequests[options.url].abort();
    }
    currentRequests[options.url] = jqXHR;
  }
});
`
$.ajax("https://jsonplaceholder.typicode.com/posts/1")
  .done(function() {
    alert("success");
  })
```

to check if the `abortOnRetry` option is enabled and call `abort` if the request URL is in the `currentRequests` object.

This way, it won’t retry after it’s already been tried.

## jQuery.ajaxSetup()

The `jQuery.ajaxSetup()` method lets us add set default values for future Ajax requests.

But its use isn’t recommended.

For example, we can write:

```
$.ajaxSetup({
  url: "https://jsonplaceholder.typicode.com/posts/1"
});
`
$.ajax()
  .done(function() {
    alert("success");
  })
```

Then the default URL to make the request to is `”https://jsonplaceholder.typicode.com/posts/1"` .

## jQuery.ajaxTransport()

We call the `jQuery.ajaxTransport()` method to create an object that handles the transmission of Ajax data.

For example, we can write:

```
jQuery.ajaxSetup({
  accepts: {
    script: "application/json"
  },
  contents: {
    script: /json/
  },
  converters: {
    "text script": jQuery.globalEval
  }
});
`
$.ajax("https://jsonplaceholder.typicode.com/posts/1")
  .done(function() {
    alert("success");
  })
```

to add the `application/json` header to our request.

## :image Selector

We can select any element with type `image` with the `:image` selector.

For example, if we have:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="image">
</form>
```

Then we can write:

```
$("input:image").css({
  background: "yellow",
  border: "3px red solid"
});
```

to add a yellow background and a red border to the image input.

## .index()

The `index` method lets us get the index of an element.

For example, if we have:

```
<ul>
  <li id="foo">foo</li>
  <li id="bar">bar</li>
  <li id="baz">baz</li>
</ul>
```

Then we can use it by writing:

```
const listItems = $("li").slice(1);
console.log($("li").index(listItems));
```

Then the console log should log 1 since we got the first item on the list.

## .innerHeight()

The `innerHeight` method gets the current computed inner height for the first element in the set of matched elements.

It can also set the inner height of every matched element.

For example, if we have:

```
<p>Hello</p>
```

Then we can get the inner height of the `p` element by writing:

```
console.log($("p").first().innerHeight());
```

If we have:

```
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

Then we can set the inner height by writing:

```
const modHeight = 70;
$("div").one("click", function() {
  $(this).innerHeight(modHeight).addClass("mod");
});
```

## .innerWidth()

The `innerWidth` method lets us set the inner width of an element for the first element in a set of matched elements.

It can also be used to set the inner width of every matched element.

For example, if we have:

```
<p>Hello</p>
```

Then we can get the inner width of the `p` element by writing:

```
const p = $("p").first();
console.log(p.innerWidth())
```

If we have:

```
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

And the following CSS:

```
.mod {
  background: blue;
  cursor: default;
}
```

Then we can write:

```
const modWidth = 70;
$("div").one("click", function() {
  $(this).innerHeight(modWidth).addClass("mod");
});
```

to set the inner width of the div when we click it.

## :input Selector

The `:input` selector lets us select all input, textarea, select, and button elements.

For example, if we have:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="image">
  <input type="password">
  <input type="radio">
  <input type="reset">
  <input type="submit">
  <input type="text">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
```

Then we can write:

```
const allInputs = $(":input");
console.log(allInputs)
```

to get all the elements in the form.

## .insertAfter()

The `.insertAfter()` method inserts every element in the set of the matched elements after the target.

For example, if we have:

```
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we can add an element after each div with the class `inner` by writing:

```
$("<p>Test</p>").insertAfter(".inner");
```

## .insertBefore()

We can call the `insertBefore` method to insert every element in the set of matched elements before the target.

For example, if we have:

```
<div class="container">
  <h2>Greetings</h2>
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

We can insert an element before each div with the class `inner` by writing:

```
$("<p>Test</p>").insertBefore(".inner");
```

## jQuery.each()

We can iterate over objects, arrays, and array-like objects with the `length` property with the `each` method.

For example, if we have:

```
$.each([52, 97], function(index, value) {
  console.log(index, value);
});
```

Then we log the `index` and `value` for each entry in the array.

## jQuery.escapeSelector()

We can escape any character that has special meaning in a CSS selector with the `escapeSelector` method.

For example, we can write:

```
console.log($.escapeSelector( "#target" ))
```

to return the escaped string.

So we see:

```
'#target'
```

logged.

## jQuery.extend()

The `jQuery.extend()` method lets us merge 2 or more objects together into the first object.

For example, we can write:

```
const object1 = {
  apple: 0,
  banana: {
    weight: 52,
    price: 100
  },
  cherry: 97
};
const object2 = {
  banana: {
    price: 200
  },
  durian: 100
};

$.extend(object1, object2);
console.log(object1)
```

Then we get:

```
{
  "apple": 0,
  "banana": {
    "price": 200
  },
  "cherry": 97,
  "durian": 100
}
```

as the value of `object1` .

## jQuery.fn.extend()

The `jQuery.fn.extend()` method lets us merge the content of an object into the jQuery prototype to add new jQuery instance methods.

For instance, if we have:

```
<label><input type="checkbox" name="foo"> Foo</label>
<label><input type="checkbox" name="bar"> Bar</label>
```

Then we can add the `check` and `uncheck` instance methods by writing:

```
jQuery.fn.extend({
  check() {
    return this.each(function() {
      this.checked = true;
    });
  },
  uncheck() {
    return this.each(function() {
      this.checked = false;
    });
  }
});

$("input[type='checkbox']").check();
```

They set the `checked` property to `true` and `false` respectively.

Now we can call it as we do in the last line to get check and uncheck the checkboxes.

## jQuery.fx.off

The `jQuery.fx.off` method globally disables all animations.

For example, if we have the following HTML:

```
<input type="button" value="Run">
<button>Toggle fx</button>
<div></div>
```

and CSS:

```
div {
  width: 50px;
  height: 30px;
  margin: 5px;
  float: left;
  background: green;
}
```

Then we can toggle the animation effect for the div bu writing:

```
const toggleFx = function() {
  $.fx.off = !$.fx.off;
};
toggleFx();
$("button").click(toggleFx);
$("input").click(function() {
  $("div").toggle("slow");
});
```

The `toggleFx` method toggles the animation.

Then we run the `toggle` method when we click the button.

## jQuery.get()

The `jQuery.get()` method lets us make a GET request.

For example, we can write:

```
$.get("https://jsonplaceholder.typicode.com/posts/1", function(data) {
  console.log(data)
});
```

to make a GET request with the given URL.

The callback’s `data` parameter has the data from the response.

## jQuery.getJSON()

The `jQuery.getJSON()` method lets us make a request and get the JHSON response from it.

For example, we can write:

```
$.getJSON("https://jsonplaceholder.typicode.com/posts/1", function(data) {
  console.log(data)
});
```

to make a request as we do with the `get` method.

## jQuery.getScript()

The `jQuery.getScript()` method lets us get a script from a server/

For example, we can use it by writing:

```
$.getScript("https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js", function(data, textStatus, jqxhr) {
  console.log(data);
  console.log(textStatus);
  console.log(jqxhr.status);
});
```

Then we get the `textStatus` and `jqxhr.status` to get the request status.

`data` has the response data.

## .keypress()

We can use the `keypress` method to listen to keypress events or trigger it.

For example, if we have:

```
<form>
  <fieldset>
    <input id="target" type="text" value="Hello there">
  </fieldset>
</form>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the keypress event on the input by writing:

```
$("#target").keypress(function() {
  console.log("Handler for .keypress() called.");
});
```

We can also trigger the keypress event when we click on the div with ID `other` by writing:

```
$("#target").keypress(function() {
  console.log("Handler for .keypress() called.");
});

$("#other").click(function() {
  $("#target").keypress();
});
```

## .keyup()

The `.keyup()` method lets us listen to the `keyup` event or trigger it.

For instance, if we have:

```
<form>
  <fieldset>
    <input id="target" type="text" value="Hello there">
  </fieldset>
</form>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `keyup` event on the input by writing:

```
$("#target").keyup(function() {
  console.log("Handler for .keypress() called.");
});
```

We can also trigger the `keyup` event when we click on the div with ID `other` by writing:

```
$("#target").keyup(function() {
  console.log("Handler for .keypress() called.");
});

$("#other").click(function() {
  $("#target").keyup();
});
```

## :lang() Selector

The `:lang` selector lets us select all elements of the specified language.

For example, if we have the following HTML:

```
<div lang="en-us">red
  <div>white
    <div>and blue</div>
  </div>
</div>
<div lang="es-es">rojo
  <div>amarillo
    <div>y rojo</div>
  </div>
</div>
```

And CSS:

```
.spain {
  background-color: red;
  color: #ff0;
}

.usa {
  background-color: red;
  color: #fff;
}
```

Then we can add the different classes to the div with different `lang` attribute values by writing:

```
$("div:lang(en-us)").addClass("usa");
$("div:lang(es-es)").addClass("spain");
```

## .last()

We can get the last element in a set of matched elements with the `.last` method.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we add a red background to the last `li` by writing:

```
$("li").last().css("background-color", "red");
```

We get the `li's` and then call `last` to get the last one.

## :last-child Selector

The `:last-child` selector selects all elements that are the last child of the parent.

For example, if we have the following HTML:

```
<div>
  <span>John,</span>
  <span>Karl,</span>
  <span>Brandon,</span>
  <span>Sam</span>
</div>
<div>
  <span>James,</span>
  <span>Mary,</span>
  <span>Ralph,</span>
  <span>David</span>
</div>
```

and CSS:

```
span.solast {
  text-decoration: line-through;
}
```

Then we can make the last `span` of each `div` red and add a strikethrough when web hover over them by writing:

```
$("div span:last-child")
  .css({
    color: "red",
    fontSize: "80%"
  })
  .hover(function() {
    $(this).addClass("solast");
  }, function() {
    $(this).removeClass("solast");
  });
```

## :last-of-type Selector

We can get the last element of a given type with the `:last-pf-type` selector.

For example, if we have the following HTML:

```
<div>
  <span>Corey,</span>
  <span>Yehuda,</span>
  <span>Adam,</span>
  <span>Todd</span>
</div>
<div>
  <span>James,</span>
  <span>Mary,</span>
  <span>Tim,</span>
  <b>Nobody</b>
</div>
```

and CSS:

```
span.solast {
  text-decoration: line-through;
}
```

Then we can make the last `span` of each `div` red and add a strikethrough when web hover over them by writing:

```
$("span:last-of-type")
  .css({
    color: "red",
    fontSize: "80%"
  })
  .hover(function() {
    $(this).addClass("solast");
  }, function() {
    $(this).removeClass("solast");
  });
```

## .length

We can get the number of elements in the jQuery object with the `.length` property.

For example, if we have:

```
<div></div>
```

Then we add a div and get the total number of divs by writing:

```
$(document.body).append($("<div>"));
const n = $("div").length;
console.log(n);
```

The console log should log 2.

## .load()

The `.load()` method lets us load data from the server and place the returned HTML into matched elements.

For example, if we have:

```
<div id='result'></div>
```

Then we can write:

```
$("#result").load("https://jsfiddle.net");
```

to load the content of [https://jsfiddle.net](https://jsfiddle.net) into the div with ID `result` .

## .map()

The `.map()` method lets us map the values of each item into a new value.

For example, if we have:

```
<form method="post" action="">
  <fieldset>
    <div>
      <label for="two">2</label>
      <input type="checkbox" value="2" id="two" name="number[]">
    </div>
    <div>
      <label for="four">4</label>
      <input type="checkbox" value="4" id="four" name="number[]">
    </div>
    <div>
      <label for="six">6</label>
      <input type="checkbox" value="6" id="six" name="number[]">
    </div>
    <div>
      <label for="eight">8</label>
      <input type="checkbox" value="8" id="eight" name="number[]">
    </div>
  </fieldset>
</form>
```

Then we get all the checkboxes’ IDs and then join them into a string by writing:

```
const str = $(":checkbox")
  .map(function() {
    return this.id;
  })
  .get()
  .join();
console.log(str);
```

Then `str` is `‘two,four,six,eight’` .

## .mousedown()

The `.mousedown()` method lets us add an event listener to the `mousedown` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mousedown(function() {
  console.log("Handler for .mousedown() called.");
});
```

Also, we can trigger then `mousedown` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mousedown(function() {
  console.log("Handler for .mousedown() called.");
});

$("#other").click(function() {
  $("#target").mousedown();
});
```

## .mouseenter()

The `.mouseenter()` method lets us add an event listener for the `mousedown` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mouseenter(function() {
  console.log("Handler for .mouseenter() called.");
});
```

Also, we can trigger then `mousedown` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mouseenter(function() {
  console.log("Handler for .mouseenter() called.");
});

$("#other").click(function() {
  $("#target").mouseenter();
});
```

## .mouseleave()

The `.mouseleave()` method lets us add an event listener for the `mouseleave` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mouseleave(function() {
  console.log("Handler for .mouseleave() called.");
});
```

Also, we can trigger then `mousedown` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mouseleave(function() {
  console.log("Handler for .mouseleave() called.");
});

$("#other").click(function() {
  $("#target").mouseleave();
});
```

## .mousemove()

The `.mousemove()` method lets us add an event listener for the `mousemove` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mousemove(function() {
  console.log("Handler for .mouseleave() called.");
});
```

Also, we can trigger then `mousedown` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mousemove(function() {
  console.log("Handler for .mouseleave() called.");
});

$("#other").click(function() {
  $("#target").mousemove();
});
```

## .mouseout()

The `.mouseout()` method lets us add an event listener for the `mouseout` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mouseout(function() {
  console.log("Handler for .mouseout() called.");
});
```

Also, we can trigger then `mousedown` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mouseout(function() {
  console.log("Handler for .mouseleave() called.");
});

$("#other").click(function() {
  $("#target").mouseout();
});
```

## .mouseover()

The `.mouseover()` method lets us add an event listener for the `mouseover` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mouseover(function() {
  console.log("Handler for .mouseover() called.");
});
```

Also, we can trigger then `mousedown` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mouseover(function() {
  console.log("Handler for .mouseover() called.");
});

$("#other").click(function() {
  $("#target").mouseover();
});
```

## .mouseup()

The `.mouseup()` method lets us add an event listener for the `mouseup` event or trigger it.

For example, if we have:

```
<div id="target">
  Click here
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `mouswdown` event on the div with ID `target` by writing:

```
$("#target").mouseup(function() {
  console.log("Handler for .mouseup() called.");
});
```

Also, we can trigger then `mouseup` event on the div with ID `target` when we click on the div with ID `other` by writing:

```
$("#target").mouseup(function() {
  console.log("Handler for .mouseup() called.");
});

$("#other").click(function() {
  $("#target").mouseup();
});
```

## Multiple Attribute Selector [name=”value”][name2=”value2″]

We can select items with multiple attributes with the multiple attribute selector.

For example, if we have:

```
<input id="man-news" name="man-news">
<input name="milkman">
<input id="letterman" name="new-letterman">
<input name="newmilk">
```

Then we can get the input with ID `letterman` and `name` value `new-letterman` by writing:

```
$("input[id][name$='man']").val("only this one");
```

After we got the element, we call `val` to set the input value.

## Multiple Selector (“selector1, selector2, selectorN”)

The multiple selector selector lets us get elements that match any of the given selectors.

For example, if we have:

```
<div>div</div>
<p class="myClass">p class="myClass"</p>
<p class="notMyClass">p class="notMyClass"</p>
<span>span</span>
```

Then we can add a red border to the `div` , `span` , and the `p` element with class `myClass` by writing:

```
$("div, span, p.myClass").css("border", "3px solid red");
```

## .next()

The `.next()` method get the element sibling element that immediately follows a given element.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get the `li` that’s immediately next to the `li` with class `third-item` by writing:

```
$("li.third-item").next().css("background-color", "red");
```

Then we call `css` to add a red background color to it.

## Next Adjacent Selector (“prev + next”)

We can use the next adjacent selector to add the adjacent selector to get the sibling element next to the given element.

For example, if we have:

```
<form>
  <label for="name">Name:</label>
  <input name="name" id="name">
  <fieldset>
    <label for="newsletter">Newsletter:</label>
    <input name="newsletter" id="newsletter">
  </fieldset>
</form>
<input name="none">
```

Then we can get the input next to the label and add some styles and set their value by writing:

```
$("label + input").css("color", "blue").val("Labeled!");
```

## Next Siblings Selector (“prev ~ siblings”)

The next sibling selector lets us select all sibling elements that follow the prev element.

The siblings must have the same parent.

For example, if we have:

```
<div>div (doesn't match since before #prev)</div>
<span id="prev">span#prev</span>
<div>div sibling</div>
<div>div sibling <div id="small">div niece</div>
</div>
<span>span sibling (not div)</span>
<div>div sibling</div>
```

Then we can get all the divs that comes with the span with ID `prev` by writing:

```
$("#prev ~ div").css("border", "3px groove blue");
```

We call `css` to add a blue border to the matching elements.

## .nextAll()

The `.nextAll()` method gets all the following siblings of each element in the set of matched elements.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get all the `li` s that comes after the `li` with the class `third-item` and add a red background to them by writing:

```
$("li.third-item").nextAll().css("background-color", "red");
```

## .nextUntil()

The `.nextUntil()` method gets all the following siblings of each element up to but not including the element matched by a selector, DOM node, or jQuery object passed in.

For example, if we have:

```
<dl>
  <dt id="term-1">term 1</dt>
  <dd>definition 1-a</dd>
  <dd>definition 1-b</dd>
  <dd>definition 1-c</dd>
  <dd>definition 1-d</dd>
  <dt id="term-2">term 2</dt>
  <dd>definition 2-a</dd>
  <dd>definition 2-b</dd>
  <dd>definition 2-c</dd>
  <dt id="term-3">term 3</dt>
  <dd>definition 3-a</dd>
  <dd>definition 3-b</dd>
</dl>
```

Then we get the `dt` element with ID `term-2` up to the `dt` with ID `term-3` by writing:

```
$("#term-2")
  .nextUntil("dt")
  .css("background-color", "red");
```

Then we add a red background to it.

## .not()

We call `not` to remove elements from a set of matched elements.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get all the `li` s in odd-numbered positions by writing:

```
$("li").not(":nth-child(2n)").css("background-color", "red");
```

Then we call `css` to add a red background to it.

## jQuery.ready

The `jQuery.ready` is a thenable object that resolves when the document is ready.

For example, we can write:

```
(async () => {
  const data = await $.when(
    $.getJSON("https://jsonplaceholder.typicode.com/posts/1"),
    $.ready
  )
  console.log(data);
})()
```

We call `getJSON` to get JSON data.

Then we call `$.ready` to wait for the `document` to be ready.

Then we get the `data` after both operations are done.

## jQuery.readyException()

The `jQuery.readyException` method handles errors that are thrown synchronously in functions wrapped in jQuery.

For example, we can write:

```
jQuery.readyException = function(error) {
  console.error(error);
};
```

to pass the `error` object into the `console.error` method and log it.

## jQuery.removeData()

The `jQuery.removeData()` method lets us remove data from an element.

For example, if we have:

```
<div></div>
```

Then we can use `removeData` to remove data from the div:

```
const div = $("div")[0];
jQuery.data(div, "test1", "value");
console.log(jQuery.data(div, "test1"))
jQuery.removeData(div, "test1");
console.log(jQuery.data(div, "test1"))
```

We get the div and then call `jQuery.data` to get the data.

Then we call `removeData` to remove the data.

So the first console log logs `‘value’` and the 2nd one logs `undefined` .

## jQuery.support

The `jQuery.support` property has an object that shows what browser features are supported.

## jQuery.uniqueSort()

The `jQuery.uniqueSort()` method sorts an array of DOM elements in place with the duplicates removed.

For example, if we have:

```
<div></div>
<div class="dup"></div>
<div class="dup"></div>
<div class="dup"></div>
<div></div>
```

Then we can use it as follows:

```
let divs = $("div").get();
divs = divs.concat($(".dup").get());
console.log(divs.length)
divs = jQuery.uniqueSort(divs);
console.log(divs.length)
```

We get the divs. Then we add the divs with class `dup` into the divs element list.

Then we call `uniqueSort` to sort them and remove the duplicates.

Therefore, the first console log logs 8 and the 2nd one logs 5.

## jQuery.when()

We can use the `jQuery.when()` method to run callback functions based on 0 or more thenable objects.

For example, we can write:

```
(async () => {
  const data = await $.when($.ajax("https://jsonplaceholder.typicode.com/posts"))
  console.log(data);
})()
```

to make a GET request and then log the data.

## .keydown()

The `.keydown()` method lets us listen to the keydown event on an element.

For example, if we have:

```
<form>
  <input id="target" type="text" value="Hello there">
</form>
<div id="other">
  Trigger the handler
</div>
```

Then we can use it to listen to the `keydown` events on the input element by writing:

```
$("#target").keydown(function() {
  console.log("Handler for .keydown() called.");
});
```

We can also use it to trigger a `keydown` event on another element.

For example, if we have the same HTML, then we can write:

```
$("#target").keydown(function() {
  console.log("Handler for .keydown() called.");
});

$("#other").click(function() {
  $("#target").keydown();
});
```

to trigger the `keydown` event on the input when we click on the div with ID `other` . this article, we’ll look at how to using jQuery in our web apps.

## .parents()

The `.parents()` method lets us get the ancestors of each element in the current set of matched elements.

We can optionally filter that with a selector.

For example, if we have:

```
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

Then we get all the ancestors of the `li` with the `item-a` class by writing:

```
$("li.item-a").parents().css("background-color", "red");
```

Then we add a red background to it.

## .parentsUntil()

The `.parentsUntil()` method gets the ancestors of each element in the current set of matched elements up to but nor including the element matched bu the selector, DOM node, or jQuery object.

For example, if we have:

```
<ul class="level-1 yes">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2 yes">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

Then we can get the parents of the `li` with the `item-a` class up to but not including the `li` with class `level-1` and add a background to them by writing:

```
$("li.item-a")
  .parentsUntil(".level-1")
  .css("background-color", "red");
```

## :password Selector

The `:password` selector lets us select all elements with `type` password.

For example, if we have:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
```

Then we write:

```
$("input:password").css({
  background: "yellow",
  border: "3px red solid"
});
```

to add a yellow background and a red border to the input with `type` password.

## .position()

The `.position()` method gets the current coordinates of the first element in the set of matched elements relative to the offset parent.

For example, if we have:

```
<p>Hello</p>
```

Then we can get the position of the `p` element by writing:

```
const p = $("p").first();
const position = p.position();
console.log(position)
```

And we get:

```
{top: 0, left: 8}
```

as the value of the `position` .

## .prepend()

The `.prepend()` method inserts the content to the beginning of each element in the set of matched elements.

For example, if we have:

```
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we add an element before the text node of each div with the class `inner` by writing:

```
$(".inner").prepend("<p>Test</p>");
```

## .prependTo()

The `.prependTo()` method lets us prepend an element in a set of matched elements.

For example, if we have:

```
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we can prepend a `p` element to each div with the class `inner` as their child by writing:

```
$("<p>Test</p>").prependTo(".inner");
```

## jQuery.merge()

The `jQuery.merge()` method merges the contents of 2 arrays together into the first array.

For example, we can use it by writing:

```
const arr = $.merge([0, 1, 2], [2, 3, 4])
console.log(arr);
```

Then `arr` is:

```
[0, 1, 2, 2, 3, 4]
```

## jQuery.noConflict()

The `jQuery.noConflict()` method relinquishes jQuery’s control of the `$` variables.

We can use it by writing:

```
jQuery.noConflict();
jQuery( "div p" ).hide();
```

We call `noConflict` .

Then we can invoke jQuery with `jQuery` instead of `$` .

## jQuery.noop()

The `jQuery.noop()` method returns an empty function.

## jQuery.param()

The `jQuery.param()` method converts an object’s key-value pairs into a query string.

For example, we can write:

```
const params = {
  width: 1680,
  height: 1050
};
const str = jQuery.param(params);
console.log(str)
```

Then `str` is `‘width=1680&height=1050’` .

## jQuery.parseHTML()

The `jQuery.parseHTML()` method lets us parse a string into an array of DOM nodes.

For example, if we have:

```
<div id="log">
  <h3>Content:</h3>
</div>
```

Then we can append the parsed HTML into the div with ID `log` by writing:

```
const str = "hello, <b>my name is</b> jQuery.";
const html = $.parseHTML(str);
$("#log").append(html);
```

We parse the HTML string with `$.parseHTML` and then call `append` to append the item.

## jQuery.parseJSON()

We can parse JSON string into an object with the `jQuery.parseJSON()` the method.

For example, if we have:

```
const obj = jQuery.parseJSON('{ "name": "John" }');
console.log(obj.name === "John");
```

Then we parse the string into the `obj` object.

The `obj.name` value is `'John'` .

So the console log logs `true` .

## jQuery.parseXML()

The `jQuery.parseXML()` method lets us parse XML into an object.

For example, we can use it by writing:

```
const xml = "<rss version='2.0'><channel><title>RSS Title</title></channel></rss>",
  xmlDoc = $.parseXML(xml),
  $xml = $(xmlDoc),
  title = $xml.find("title");
console.log(title.text())
```

We call `parseXML` with the XML string.

Then we put that into the `$` function so that we can call `find` to find the element we want.

Then we can get the text of the matched element with the `text` method.

## jQuery.post()

The `jQuery.post()` method lets us make a POST request to a given URL.

For example, we can write:

```
const jqxhr = $.post("https://jsonplaceholder.typicode.com/posts", {
    title: "title",
    body: "body"
  }, function() {
    console.log("success");
  }, "json")
  .done(function() {
    console.log("second success");
  })
  .fail(function() {
    console.log("error");
  })
  .always(function() {
    console.log("finished");
  });

jqxhr.always(function() {
  console.log("second finished");
});
```

to make a POST request.

The 2nd argument is the form data keys and values we want to send with the request.

The `done` callback is called when the request is successful.

The `fail` callback is called when the request failed.

`always` callback is called when the request is finished regardless of the result.

## jQuery.queue()

The `jQuery.queue()` method show or manipulate the queue of functions to be run on the matched element.

For example, if we have the following HTML:

```
<div></div>
```

and CSS:

```
div {
  margin: 3px;
  width: 40px;
  height: 40px;
  position: absolute;
  left: 0px;
  top: 30px;
  background: green;
  display: none;
}

div.newcolor {
  background: blue;
}

span {
  color: red;
}
```

Then we can animate the div by writing:

```
$("div")
  .show("slow")
  .animate({
    left: "+=200"
  }, 2000)
  .slideToggle(1000)
  .slideToggle("fast")
  .animate({
    left: "-=200"
  }, 1500)
  .hide("slow")
  .show(1200)

console.log(jQuery.queue($("div")[0], "fx"))
```

We get the div and use that as the argument of `jQuery.queue` to check the items that are queued.

## :not() Selector

The `:not` selector selects all elements that don't match a given selector.

For example, if we have:

```
<div>
  <input type="checkbox" name="a">
  <span>Mary</span>
</div>
<div>
  <input type="checkbox" name="b">
  <span>lcm</span>
</div>
<div>
  <input type="checkbox" name="c" checked="checked">
  <span>Peter</span>
</div>
```

Then we add a yellow background to all the checkboxes that are unchecked by writing:

```
$("input:not(:checked) + span").css("background-color", "yellow");
```

## :nth-child() Selector

The `:nth-child()` selector lets us select all elements that are the nth-child of their parent.

For example, if we have:

```
<div>
  <ul>
    <li>John</li>
    <li>Karl</li>
    <li>Brandon</li>
  </ul>
</div>
<div>
  <ul>
    <li>Sam</li>
  </ul>
</div>
<div>
  <ul>
    <li>John</li>
    <li>Jane</li>
    <li>Ralph</li>
    <li>David</li>
  </ul>
</div>
```

Then we add a `span` to the name that is in the 2nd `li` of each `ul` by writing:

```
$("ul li:nth-child(2)").append("<span> - 2nd!</span>");
```

## :nth-last-child() Selector

The `:nth-last-child` selector lets us select all elements that are the nth-child of their parent.

For example, if we have:

```
<div>
  <ul>
    <li>John</li>
    <li>Karl</li>
    <li>Brandon</li>
  </ul>
</div>
<div>
  <ul>
    <li>Sam</li>
  </ul>
</div>
<div>
  <ul>
    <li>John</li>
    <li>Jane</li>
    <li>Ralph</li>
    <li>David</li>
  </ul>
</div>
```

Then we get the 2nd last `li` in each `ul` and add a child span to it by writing:

```
$("ul li:nth-last-child(2)").append("<span> - 2nd to last!</span>");
```

## :nth-last-of-type() Selector

The `:nth-last-of-type` selector lets get the last element of the given type.

For example, if we have:

```
<div>
  <ul>
    <li>John</li>
    <li>Karl</li>
    <li>Brandon</li>
  </ul>
</div>
<div>
  <ul>
    <li>Sam</li>
  </ul>
</div>
<div>
  <ul>
    <li>John</li>
    <li>Jane</li>
    <li>Ralph</li>
    <li>David</li>
  </ul>
</div>
```

Then we can get the 2nd last `li` s in the `ul` and add a `span` in them by writing:

```
$("ul li:nth-last-of-type(2)").append("<span> - 2nd to last!</span>");
```

## :nth-of-type() Selector

The `:nth-of-type` selector selects all elements that are the nth child of their parent in relation to siblings with the same element name.

For example, if we have:

```
<div>
  <span>John</span>,
  <b>Kim</b>,
  <span>Adam</span>,
  <b>Rafael</b>,
  <span>Oleg</span>
</div>
<div>
  <b>Dave</b>,
  <span>Ann</span>
</div>
<div>
  <i><span>Maurice</span></i>,
  <span>Richard</span>,
  <span>Ralph</span>,
  <span>Jason</span>
</div>
```

Then we get the 2nd sibling `span` and add another `span` into it by writing:

```
$("span:nth-of-type(2)")
  .append("<span> is 2nd sibling span</span>")
  .addClass("nth");
```

## .odd()

We can reduce the set of matched elements to the odd ones in the set with the `odd` selector.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we select the `li` ‘s with an odd index by writing:

```
$("li").odd().css("background-color", "red");
```

We add a red background to the 2nd and 4th `li` since the index starts at 0.

## .off()

The `.off()` select removes an event handler.

For example, if we have:

```
<button id="theone">Does nothing...</button>
<button id="bind">Add Click</button>
<button id="unbind">Remove Click</button>
<div style="display:none;">Click!</div>
```

Then we can use the `off` method to remove a `click` handler by writing:

```
function flash() {
  $("div").show().fadeOut("slow");
}

$("#bind").click(function() {
  $("body")
    .on("click", "#theone", flash)
    .find("#theone")
    .text("Can Click!");
});
$("#unbind").click(function() {
  $("body")
    .off("click", "#theone", flash)
    .find("#theone")
    .text("Does nothing...");
});
```

The click listener for the button with ID `unbind` has the `off` method to remove the `flash` function as the body’s `click` handler.

## .offset()

The `.offset()` method gets the current coordinates of the first element in the set of matched elements relative to the document.

For example, if we have:

```
<p>Hello</p>
<p>2nd Paragraph</p>
```

Then we can get the last `p` element’s offset by writing:

```
const p = $("p").last();
const offset = p.offset();
console.log(offset);
```

Then we get:

```
{
  "top": 50,
  "left": 8
}
```

as the value of `offset` .

## .offsetParent()

The `.offsetParent()` method gets the closes ancestor element that’s positioned.

For example, if we have:

```
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii" style="position: relative;">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

Then we get the `li` with class `item-a` ‘s parent with the `offsetParent` method and add a background to it by writing:

```
$("li.item-a").offsetParent().css("background-color", "red");
```

## .on()

The `.on()` method attaches an event handler function for one or more events to the selected elements.

For example, if we have:

```
<p>Has an attached custom event.</p>
<button>Trigger custom event</button>
<span style="display:none;"></span>
```

Then we can trigger a custom event when we click on the button by writing:

```
$("p").on("myCustomEvent", function(event, myName) {
  $(this).text(`${myName}, hi there`);
  $("span")
    .stop()
    .css("opacity", 1)
    .text(`myName = ${myName}`)
    .fadeIn(30)
    .fadeOut(1000);
});

$("button").click(function() {
  $("p").trigger("myCustomEvent", ["John"]);
});
```

We call `trigger` with the event name as the first argument and the data we want to send with the event in an array.

To listen to the `myCustomEvent` event, we call `on` with the same event name as the first argument.

The 2nd argument is a callback that runs when the event is triggered.

`myName` is `'John'` so we see that added to the `p` element.

## .one()

The `.one()` method attaches a handler to an event for the elements.

The handler is run at most once per element per event type.

For example, if we have:

```
<p id='foo'>foo</p>
```

Then we write:

```
$("#foo").one("click mouseover", function(event) {
  alert("The " + event.type + " event happened!");
});
```

to add a listener for the `click` and `mouseover` events on the `p` element wiuth ID `foo`with the `one` method.

## :only-child Selector

The `:only-child` selector selects all elements that are the only child of their parent.

For example, if we have:

```
<div>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>

<div>
  None
</div>

<div>
  <button>Sibling</button>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>
```

Then we add a border and change the text of the buttons that are the only in the div by writing:

```
$("div button:only-child").text("Alone").css("border", "2px blue solid");
```

So the 2nd and last div will have the text changed and the border added.

## :only-of-type Selector

We can use the `:only-of-type` selector to select all elements that have no siblings with the same element name.

For example, if we have:

```
<div>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>

<div>
  None
</div>

<div>
  <button>Sibling</button>
  <button>Sibling</button>
  <button>Sibling</button>
</div>

<div>
  <button>Sibling</button>
</div>
```

Then we can get buttons that are the only child in the div by writing:

```
$("button:only-of-type").text("Alone").css("border", "2px blue solid");
```

Then we change their text and add a border to them.

## .outerHeight()

The `.outerHeight()` method lets us get the computed outer height, which includes the padding, border, and optionally margin, for the first element in the set of matched elements.

It can also be used to set the outer height of every matched element.

For example, if we have:

```
<p>Hello</p>
```

Then we get the outer height with the margin by writing:

```
const p = $("p").first();
console.log(p.outerHeight(true));
```

`true` means we include the margin.

If we have:

```
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

Then we can set the outer height of the div when we click it by writing:

```
const modHeight = 60;
$("div").one("click", function() {
  $(this).outerHeight(modHeight);
});
```

## .outerWidth()

The `.outerWidth()` method gets the current computed outer width, including the padding, border, and optionally the margin, for the first element of the set of matched elements.

It can also be used to set the outer width of all matched elements.

It can also be used to set the outer height of every matched element.

For example, if we have:

```
<p>Hello</p>
```

Then we get the outer height with the margin by writing:

```
const p = $("p").first();
console.log(p.outerWidth(true));
```

`true` means we include the margin.

If we have the following HTML:

```
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

and CSS:

```
.mod {
  background: blue;
  cursor: default;
}
```

Then we can set the outer height of the div when we click it by writing:

```
const modHeight = 60;
$("div").one("click", function() {
  $(this).outerWidth(modHeight).addClass("mod");;
});
```

We call `addClass` to add the `mod` class with a blue background.

## .parent()

The `.parent()` method lets us get the parent element of the given element.

For example, if we have:

```
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
      <li class="item-b">B
        <ul class="level-3">
          <li class="item-1">1</li>
          <li class="item-2">2</li>
          <li class="item-3">3</li>
        </ul>
      </li>
      <li class="item-c">C</li>
    </ul>
  </li>
  <li class="item-iii">III</li>
</ul>
```

Then the `li` with the `item-a` class’s parent and add a background to it by writing:

```
$("li.item-a").parent().css("background-color", "red");
```

## :parent Selector

The `:parent` selector lets us get the parent of a given element.

For example, if we have:

```
<table border="1">
  <tr>
    <td>Value 1</td>
    <td></td>
  </tr>
  <tr>
    <td>Value 2</td>
    <td></td>
  </tr>
</table>
```

Then we can fade the `tr` by writing:

```
$("td:parent").fadeTo(1500, 0.3);
```

## .prev()

We call the `.prev()` method to get the immediately preceding sibling of each element in the set of matched elements.

If a selector is provided, it gets the precious siblings only if it matches that selector.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get the `li` that’s immediately before the `li` with the class `third-item` by writing:

```
$("li.third-item").prev().css("background-color", "red");
```

Then we add a red background to it.

## .prevAll()

The `.prevAll()` method gets all preceding siblings of each element in the set of matched elements.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get all the preceding siblings of the `li` that has the class `third-item` and add a background to them by writing:

```
$("li.third-item").prevAll().css("background-color", "red");
```

## .prevUntil()

The `.prevUntil()` gets all preceding siblings of each element up to but not including the element matched by the selector, DOM node, or jQuery object.

For example, if we have:

```
<dl>
  <dt id="term-1">term 1</dt>
  <dd>definition 1-a</dd>
  <dd>definition 1-b</dd>
  <dd>definition 1-c</dd>
  <dd>definition 1-d</dd>

  <dt id="term-2">term 2</dt>
  <dd>definition 2-a</dd>
  <dd>definition 2-b</dd>
  <dd>definition 2-c</dd>

  <dt id="term-3">term 3</dt>
  <dd>definition 3-a</dd>
  <dd>definition 3-b</dd>
</dl>
```

Then we get all the `dd` before the `dt` with ID `term-2` and up to but not including the first `dt` by writing:

```
$("#term-2").prevUntil("dt")
  .css("background-color", "red");
```

and we set their background to red.

## .promise()

The `.promise()` method returns a promise to observe when all actions of a certain type bound to the collection have finished.

For instance, if we have:

```
<button>Go</button>
<p>Ready...</p>
<div></div>
<div></div>
<div></div>
<div></div>
```

Then we can show some text when we click on a button by writing:

```
$("button").on("click", function() {
  $("p").append("Started...");

  $("div").each(function(i) {
    $(this).fadeIn().fadeOut(1000 * (i + 1));
  });

  $("div").promise().done(function() {
    $("p").append(" Finished! ");
  });
});
```

We loop through each `div` and apply some fade effects with `fadeIn` and `fadeOut` .

Then we call `promise` and run code when all the method calls are done with the `promise().done()` method.

## .prop()

We can use the `prop` method to get the attribute value.

For example, if we have:

```
<input id="check1" type="checkbox" checked="checked">
```

Then we can write:

```
$("input").change(function() {
  const $input = $(this);
  console.log($input.prop("checked"));
}).change();
```

to watch for the changes to the checkbox input.

We get the `checked` attribute’s value with the `prop` method.

## .pushStack()

We call the `pushStack` method to add a collection of DOM elements onto the jQuery stack.

For example, if we have:

```
<div>
  foo
</div>
```

Then we call `pushStack` to add the div to the stack and remove it by writing:

```
jQuery([])
  .pushStack(document.getElementsByTagName("div"))
  .remove()
  .end();
```

## .queue()

The `.queue()` method shows the queue of functions to be executed on the matched elements.

For example, if we have:

```
<p>The queue length is: <span></span></p>
<div></div>
```

Then we can show the number of queued items by writing:

```
const div = $("div");

function runIt() {
  div
    .show("slow")
    .animate({
      left: "+=200"
    }, 2000)
    .slideToggle(1000)
    .slideToggle("fast")
    .animate({
      left: "-=200"
    }, 1500)
    .hide("slow")
    .show(1200)
    .slideUp("normal", runIt);
}

function showIt() {
  const n = div.queue("fx");
  $("span").text(n.length);
  setTimeout(showIt, 100);
}

runIt();
showIt();
```

The `queue` method with `'fx'` gets the number of queued items for animations.

## :radio Selector

The `:radio` selector lets us get radio button eleements.

For example, if we have:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio" name="asdf">
  <input type="radio" name="asdf">
  <input type="reset">
  <input type="submit">
  <input type="text">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
```

Then we can add a background and border to a radio button by writing:

```
$("form input:radio")
  .wrap("<span></span>")
  .parent()
  .css({
    background: "yellow",
    border: "3px red solid"
  });
```

## .ready()

The `ready` method specifies a function to run when the DOM is fully loaded.

We can write:

```
$(document).ready(function() {
  // Handler for .ready() called.
});
```

or:

```
$(function() {
  // Handler for .ready() called.
});
```

We run code in the callback when `document` is loaded.

## .remove()

The `.remove()` method lets us remove a set of matched elements in the DOM.

For example, if we have:

```
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">Goodbye</div>
</div>
```

Then we remove the div with the class `hello` by writing:

```
$(".hello").remove();
```

## .removeAttr()

The `.removeAttr()` method removes an attribute from each element in the set of matched elements.

For example, if we have:

```
<input type="text" title="hello there">
<button>Change title</button>
```

Then we can toggle the `title` attribute on and off when we click the button by writing:

```
const inputTitle = $("input").attr("title");
$("button").click(function() {
  const input = $(this).next();
  if (input.attr("title") === inputTitle) {
    input.removeAttr("title")
  } else {
    input.attr("title", inputTitle);
  }
});
```

## .removeClass()

We can call the `.removeClass()` method to remove one or more classes on an element.

For example, if we have:

```
<p class="blue under">Hello</p>
```

Then we can remove the `blue` and `under` classes by writing:

```
$("p").removeClass("blue under")
```

## .removeData()

The `.removeData()` method to remove a previously-stored piece of data.

For example, if we have:

```
<div>hello</div>
```

Then we can add data to the div and remove it by writing:

```
$("div").data("test1", "value");
console.log($("div").data("test1"));
$("div").removeData("test1");
console.log($("div").data("test1"));
```

We call `removeData` to remove a piece of data by its key.

## .removeProp()

We can use the `removeProp` propety for the set of matched elements.

For example, if we have:

```
<p></p>
```

Then we can add a property and remove it by writing:

```
const para = $("p");
para
  .prop("code", 1234)
  .append(String(para.prop("code")))
  .removeProp("code")
  .append(String(para.prop("code")));
```

The first argument is the property name.

And the 2nd argument is the value of it.

`removeProp` takes the name of the property we want to remove.

## .replaceAll()

We call `.replaceAll()` to replace each target element with the set of matched elements.

For example, if we have:

```
<div class="container">
  <div class="inner first">Hello</div>
  <div class="inner second">And</div>
  <div class="inner third">Goodbye</div>
</div>
```

Then we can replace all the divs with class `inner` with an `h2` element by writing:

```
$("<h2>New heading</h2>").replaceAll(".inner");
```

## .replaceWith()

The `.replaceWith()` method lets us replace each element in the set of matched elements with the provided new content and return the set of elements that were removed.

For example, if we have:

```
<div class="container">
  <div class="inner first">Hello</div>
  <div class="inner second">And</div>
  <div class="inner third">Goodbye</div>
</div>
```

Then we can replace the div with the class `second` with an `h2` by writing:

```
$("div.second").replaceWith("<h2>New heading</h2>");
```

## :reset Selector

The `:reset` selector lets us select all elements of type reset.

For example, if we have:

```
<form>
  <input type="button" value="Input Button">
  <input type="checkbox">
  <input type="file">
  <input type="hidden">
  <input type="password">
  <input type="radio">
  <input type="reset">
  <input type="submit">
  <input type="text">
  <select>
    <option>Option</option>
  </select>
  <textarea></textarea>
  <button>Button</button>
</form>
<div></div>
```

Then we get input with type `reset` and add a background and border to it by writing:

```
$("input:reset").css({
  background: "yellow",
  border: "3px red solid"
});
```

## .resize()

The `.resize()` method lets us watch for resize JavaScript event or trigger it on an element.

For instance, we can use it by writing:

```
$(window).resize(function() {
  console.log("Handler for .resize() called.");
})
```

We log when `window` is resized.

## :root Selector

The `:root` selector selects the element that’s the root of the element.

For example, we can use it by writing:

```
console.log($(":root")[0].nodeName)
```

Then we get `'HTML’` logged.

## .scroll()

The `.scroll()` method binds an event handler to the scroll JavaScript event or lets us trigger it.

For example, if we have:

```
<div id="target" style="overflow: scroll; width: 200px; height: 100px;">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit,
  sed do eiusmod tempor incididunt ut labore et dolore magna
  aliqua. Ut enim ad minim veniam, quis nostrud exercitation
  ullamco laboris nisi ut aliquip ex ea commodo consequat.
  Duis aute irure dolor in reprehenderit in voluptate velit
  esse cillum dolore eu fugiat nulla pariatur. Excepteur
  sint occaecat cupidatat non proident, sunt in culpa qui
  officia deserunt mollit anim id est laborum.
</div>
<div id="other">
  Trigger the handler
</div>
```

Then we can watch for scrolling on the div with the ID `target` by writing:

```
$("#target").scroll(function() {
  console.log('scrolling');
});
```

We can also trigger scrolling when we click on the div with ID `other` by writing:

```
$("#target").scroll(function() {
  console.log('scrolling');
});

$("#other").click(function() {
  $("#target").scroll();
});
```

## .scrollLeft()

The `.scrollLeft()` method gets the current horizontal position of the scroll bar for the first element in the set of matched elements.

For example, if we have:

```
<p>Hello</p>
<p></p>
```

Then we get the horizontal positon of the scrollbar by writing:

```
const p = $("p").first();
console.log(p.scrollLeft())
```

## .scrollTop()

The `.scrollTop()` method gets the current vertical position of the scroll bar for the first element in the set of matched elements or set the vertical position of the scroll bar for each matched element.

For example, if we have:

```
<p>Hello</p>
<p></p>
```

Then we get the vertical positon of the scrollbar by writing:

```
const p = $("p").first();
$("p").last().text(p.scrollTop());
```

## .select()

The `.select()` method binds to an event handler for the select JavaScript event.

We can also use it to trigger the event on an element.

For example, if we have:

```
<form>
  <input id="target" type="text" value="Hello there">
</form>
<div id="other">
  Trigger the handler
</div>
```

We can watch for select events triggered on the input by writing:

```
$("#target").select(function() {
  console.log("Handler for .select() called.");
});
```

Also, we can trigger select on the input when we click on the div with ID `other` by writing:

```
$("#target").select(function() {
  console.log("Handler for .select() called.");
});

$("#other").click(function() {
  $("#target").select();
});
```

## :selected Selector

The `:selected` selector lets us select all elements that are selected.

For example, if we have:

```
<select name="garden" multiple="multiple">
  <option>Flowers</option>
  <option selected="selected">Shrubs</option>
  <option>Trees</option>
  <option selected="selected">Bushes</option>
  <option>Grass</option>
  <option>Dirt</option>
</select>
<div></div>
```

Then we can watch the `select` event on the `select` element by writing:

```
$("select")
  .change(function() {
    let str = "";
    $("select option:selected").each(function() {
      str += $(this).text();
    });
    $("div").text(str);
  })
  .trigger("change");
```

We get all the selected items in the `change` callback and put them all in the div.

## .serialize()

We can use the `.serialize()` method to convert the form’s values into key-value pairs.

For example, if we have:

```
<form>
  <select name="single">
    <option>Single</option>
    <option>Single2</option>
  </select>

  <br>
  <select name="multiple" multiple="multiple">
    <option selected="selected">Multiple</option>
    <option>Multiple2</option>
    <option selected="selected">Multiple3</option>
  </select>

  <br>
  <input type="checkbox" name="check" value="check1" id="ch1">
  <label for="ch1">check1</label>
  <input type="checkbox" name="check" value="check2" checked="checked" id="ch2">
  <label for="ch2">check2</label>

  <br>
  <input type="radio" name="radio" value="radio1" checked="checked" id="r1">
  <label for="r1">radio1</label>
  <input type="radio" name="radio" value="radio2" id="r2">
  <label for="r2">radio2</label>
</form>
```

Then we can log the values of the form whenever we change the value of the controls by writing:

```
const showValues = () => {
  const str = $("form").serialize();
  console.log(str);
}

$("input[type='checkbox'], input[type='radio']").on("click", showValues);
$("select").on("change", showValues);
showValues();
```

We watch for clicks and change events and call the `showValues` method whenever something is done to the form.

Then `str` is something like:

```
single=Single&multiple=Multiple&multiple=Multiple3&check=check2&radio=radio1
```

## .serializeArray()

We can call `serializeArray` to encode a set of form elements as an array of names and values.

For example, if we have:

```
<form>
  <div><input type="text" name="a" value="1" id="a"></div>
  <div><input type="text" name="b" value="2" id="b"></div>
  <div><input type="hidden" name="c" value="3" id="c"></div>
  <div>
    <textarea name="d" rows="8" cols="40">4</textarea>
  </div>
  <div><select name="e">
      <option value="5" selected="selected">5</option>
      <option value="6">6</option>
      <option value="7">7</option>
    </select></div>
  <div>
    <input type="checkbox" name="f" value="8" id="f">
  </div>
  <div>
    <input type="submit" name="g" value="Submit" id="g">
  </div>
</form>
```

Then we can serialize the form values to an array of objects by writing:

```
$("form").submit(function(event) {
  console.log($(this).serializeArray());
  event.preventDefault();
});
```

When we click Submit, we get something like:

```
[
  {
    "name": "a",
    "value": "1"
  },
  {
    "name": "b",
    "value": "2"
  },
  {
    "name": "c",
    "value": "3"
  },
  {
    "name": "d",
    "value": "4"
  },
  {
    "name": "e",
    "value": "5"
  }
]
```

logged.

## .show()

The `show` displays the matched elements.

For example, if we have the following HTML:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

And CSS:

```
img {
  display: none;
}
```

Then we can call the `show` method to show the image when we click on Click here by writing:

```
$("#clickme").click(function() {
  $("#book").show("slow", function() {
    // Animation complete.
  });
});
```

## .siblings()

The `siblings` method lets us get the siblings of each element in the set of matched elements.

We can optionally pass in a selector into this method.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li class="third-item">list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we can get all the `li` s that are sibling of the one with the class `third-item` and add a background to it:

```
$("li.third-item").siblings().css("background-color", "red");
```

## .slice()

The `slice` method lets us reduce a set of matched elements to a subset specified by the range of indexes.

For example, if we have:

```
<ul>
  <li>list item 1</li>
  <li>list item 2</li>
  <li>list item 3</li>
  <li>list item 4</li>
  <li>list item 5</li>
</ul>
```

Then we get the `li` starting with index 2 and up to and not including 4 by writing:

```
$("li").slice(2, 4).css("background-color", "red");
```

## .slideDown()

The `.slideDown()` method displays the matched elements with a sliding motion.

For example, if we have the following HTML:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

And CSS:

```
img {
  display: none;
}
```

Then we can get show the image with a slide down animation when we click on Click here by writing:

```
$( "#clickme" ).click(function() {
  $( "#book" ).slideDown( "slow", function() {
    // Animation complete.
  });
});
```

## .slideToggle()

The `.slideToggle()` method lets us display or hide the matched elements with the sliding motion.

For example, if we have the following HTML:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

And CSS:

```
img {
  display: none;
}
```

Then we can get toggle the image with a slide animation when we click on Click here by writing:

```
$( "#clickme" ).click(function() {
  $( "#book" ).slideToggle( "slow", function() {
    // Animation complete.
  });
});
```

## .slideUp()

The `.slideUp()` method hides the matched elements with a sliding motion.

For example, if we have the following HTML:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

Then we can get hide the image with a slide up animation when we click on Click here by writing:

```
$( "#clickme" ).click(function() {
  $( "#book" ).slideUp( "slow", function() {
    // Animation complete.
  });
});
```

## .stop()

The `stop` method stops the currently running animation on the matched elements.

For example, if we have:

```
<div id="hoverme">
  Hover me
  <img id="hoverme" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
</div>
```

Then we can stop the animation on the matched element by writing:

```
$("#hoverme").hover(function() {
  $(this).find("img").stop(true, true).fadeOut();
}, function() {
  $(this).find("img").stop(true, true).fadeIn();
});
```

When we hover over the img with ID `hover` , then we fade out the image.

Otherwise, we fade in the image.

## .submit()

The `.submit()` method lets us bind an event handler to the `submit` JavaScript event or trigger the event on an element.

For example, if we have:

```
<form id="target" action="destination.html">
  <input type="text" value="Hello there">
  <input type="submit" value="Go">
</form>
<div id="other">
  Trigger the handler
</div>
```

Then we can listen to the `submit` event on the form by writing:

```
$("#target").submit(function(event) {
  console.log("Handler for .submit() called.");
  event.preventDefault();
});
```

We can also trigger the submit event by writing:

```
$("#other").click(function() {
  $("#target").submit();
});
```

## :submit Selector

The `:submit` selector lets us select all elements of type submit.

For example, if we have:

```
<form id="target" action="destination.html">
  <input type="text" value="Hello there">
  <input type="submit" value="Go">
</form>
```

Then we can add a background and border on the submit button by writing:

```
$("input:submit")
  .css({
    background: "yellow",
    border: "3px red solid"
  })
  .end();
```

## :target Selector

The `:target` selector selects the target element indicated by the fragment identifier of the document’s URI.

For example, if we go to [https://example.com/#foo](https://medium.com/r/?url=https%3A%2F%2Fexample.com%2F%23foo), then, `$(“p:target”)` selects the `p` element with ID `foo` .

## .text()

The `.text` method gets the combined text contents of each element in the set of matched elements, including their descendants.

For example, if we have:

```
<p><b>Test</b> Paragraph.</p>
<p></p>
```

Then if we write:

```
console.log($("p").first().text())
```

We get `'Test Paragraph.’` logged.

## :text Selector

The `:text` selector lets us select all input elements of type `text` .

For example, if we have:

```
<form id="target" action="destination.html">
  <input type="text" value="Hello there">
  <input type="submit" value="Go">
</form>
<div id="other">
  Trigger the handler
</div>
```

Then we can add a background and border to the text input box by writing:

```
$("form input:text").css({
  background: "yellow",
  border: "3px red solid"
});
```

## .toArray()

The `.toArray()` method retrieves all elements contained in the jQuery set as an array.

For example, if we have:

```
<div>One</div>
<div>Two</div>
<div>Three</div>
```

Then we can get the divs and put them into an array by writing:

```
console.log($("div").toArray());
```

## .toggle()

The `.toggle()` method displays or hide the matched elements.

For example, if we have:

```
<div id="clickme">
  Click here
</div>
<img id="book" src="https://i.picsum.photos/id/23/200/200.jpg?hmac=IMR2f77CBqpauCb5W6kGzhwbKatX_r9IvgWj6n7FQ7c">
```

Then we can make the image toggle between on and off when we click the Click here button by writing:

```
$("#clickme").click(function() {
  $("#book").toggle("slow", function() {
    // Animation complete.
  });
});
```

## .toggleClass()

The `.toggleClass()` method lets us add or remove one or more classes from each element in the set of matched elements.

For example, if we have the following HTML:

```
<p class="blue">Click to toggle</p>
```

And CSS:

```
p {
  margin: 4px;
  font-size: 16px;
  font-weight: bolder;
  cursor: pointer;
}

.blue {
  color: blue;
}

.highlight {
  background: yellow;
}
```

Then we can toggle the `highlight` class on the `p` element by writing:

```
$("p").click(function() {
  $(this).toggleClass("highlight");
});
```

## .trigger()

The `.trigger()` method runs all handlers and behaviors attached to the matched elements for the given event type.

For example, if we have:

```
<button>Button #1</button>
<button>Button #2</button>
```

Then we can trigger the click on the first button when we click on the second button by writing:

```
$("button").first().click(function() {
  console.log('first button clicked');
});

$("button").last().click(function() {
  $("button").first().trigger("click");
});
```

## .triggerHandler()

The `.triggerHandler()` method lets us run all handlers attached to an event for an element.

For example, if we have:

```
<button id="new">.triggerHandler( "focus" )</button><br><br>

<input type="text" value="To Be Focused">
```

Then we can trigger the `focus` event when we click on the button by writing:

```
$("#new").click(function() {
  $("input").triggerHandler("focus");
});

$("input").focus(function() {
  $("<span>Focused!</span>").appendTo("body").fadeOut(1000);
});
```

We show the `Focused!` text when we click on the button as the input is focused.

## .unbind()

The `.unbind()` method removes a previous attached event handler from the elements.

For example, if we have:

```
<button id="bind">Bind Click</button>
<button id="unbind">Unbind Click</button>
<div id="theone"></div>
```

Then we can bind and unbind the click handler for the div with id `theone` by writing:

```
function aClick() {
  $("div").show().fadeOut("slow");
}

$("#bind").click(function() {
  $("#theone")
    .bind("click", aClick)
    .text("Can Click!");
});
$("#unbind").click(function() {
  $("#theone")
    .unbind("click", aClick)
    .text("Does nothing...");
});
```

We bind and unbind the click events on the div in the `click` handlers for the buttons.

## .undelegate()

The `.undelegate()` method removes a handler from the event for all elements which match the current selector which match the current selector based on the root element.

For example, if we have:

```
<button id="bind">Bind Click</button>
<button id="unbind">Unbind Click</button>
<div id="theone"></div>
```

Then we can bind and unbind the `click` handler from the div with ID `theone` by writing:

```
function aClick() {
  $("div").show().fadeOut("slow");
}

$("#bind").click(function() {
  $("body")
    .delegate("#theone", "click", aClick)
    .find("#theone")
    .text("Can Click!");
});

$("#unbind").click(function() {
  $("body")
    .undelegate("#theone", "click", aClick)
    .find("#theone")
    .text("Does nothing...");
});
```

## .unwrap()

The `.unwrap()` method removes the parent of the set of matched elements from the DOM.

For example, if we have:

```
<button>wrap/unwrap</button>
<p>Hello</p>
<p>World</p>
```

We can toggle the wrapping and unwrapping of the div around the `p` elements by writing:

```
const pTags = $("p");
$("button").click(function() {
  if (pTags.parent().is("div")) {
    pTags.unwrap();
  } else {
    pTags.wrap("<div></div>");
  }
})
```

`wrap` all wrap each `p` element in its own div.

## .val()

The `.val()` method gets the current value of the first element in the set of matched elements.

We can also use it to set th value of every matched element.

For example, if we have:

```
<select id="single">
  <option>Single</option>
  <option>Single2</option>
</select>

<select id="multiple" multiple="multiple">
  <option selected="selected">Multiple</option>
  <option>Multiple2</option>
  <option selected="selected">Multiple3</option>
</select>
```

Then we can get the value selected from the `select` element by writing:

```
function displayVals() {
  const singleValues = $("#single").val();
  const multipleValues = $("#multiple").val() || [];
  console.log(singleValues, multipleValues)
}

$("select").change(displayVals);
```

For example, if we have:

```
<input type="text" value="some text">
```

Then we can get the value from the input as we type by writing:

```
$("input")
  .keyup(function() {
    const value = $(this).val();
    console.log(value);
  })
  .keyup();
```

## :visible Selector

The `:visible` selector lets us select all elements that are visible.

For example, if we have the following HTML:

```
<button>Show hidden</button>
<div></div>
<div class="starthidden"></div>
<div></div>
<div></div>
<div style="display:none;"></div>
```

And CSS:

```
div {
  width: 50px;
  height: 40px;
  margin: 5px;
  border: 3px outset green;
  float: left;
}

.starthidden {
  display: none;
}
```

Then we can show all the divs that are hidden when we click on the button by writing:

```
$("div:visible").click(function() {
  $(this).css("background", "yellow");
});
$("button").click(function() {
  $("div:hidden").show("fast");
});
```

And when we click on the visible divs, we see a yellow background.

## .width()

The `.width()` method gets the current computed width for the first element in the set of matched elements or set the width of every matched element.

For example, we can write:

```
console.log($(window).width());
```

to log the width of the window.

To set the widths of the divs given the following HTML:

```
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
<div>d</div>
```

And CSS:

```
div {
  width: 70px;
  height: 50px;
  float: left;
  margin: 5px;
  background: red;
  cursor: pointer;
}
```

We can add click handlers to the divs and change the width inside by writing:

```
const modWidth = 50;
$("div").one("click", function() {
  $(this).width(modWidth)
});
```

## .wrap()

The `.wrap()` method lets us wrap an element with a wrapper element.

For example, if we have:

```
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we can wrap each div with the class `inner` with a div with class `new` by writing:

```
$(".inner").wrap("<div class='new'></div>");
```

## .wrapAll()

The `.wrapAll()` method lets us wrap an HTML structure around all elements in the set of matched elements.

For example, if we have:

```
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we can wrap a div with class `new` around all the divs with class `inner` by writing:

```
$(".inner").wrapAll("<div class='new' />");
```

## .wrapInner()

We can wrap an HTML structure around the content of each element in the set of matched elements with the `wrapInner` method.

For example, if we have:

```
<div class="container">
  <div class="inner">Hello</div>
  <div class="inner">Goodbye</div>
</div>
```

Then we can wrap the content of each div with class `inner` with a div with class `new` by writing:

```
$(".inner").wrapInner("<div class='new'></div>");
```

# Conclusion

JavaScript is one of the most popular programming languages in the world. To use it effectively, we’ve to know about the basics of it.

It has all the basic features of any language.

It's also the language of the web.

We can manipulate the DOM, make Ajax requests, and more with jQuery.